Streams API for PHP Extension Authors
-------------------------------------

> **Note**:
>
> The functions in this chapter are for use in the PHP source code and
> are not PHP functions. Information on userland stream functions can be
> found in the
> <a href="/book/stream.html" class="link">Stream Reference</a>.

### Overview

The PHP Streams API introduces a unified approach to the handling of
files and sockets in PHP extension. Using a single API with standard
functions for common operations, the streams API allows your extension
to access files, sockets, URLs, memory and script-defined objects.
Streams is a run-time extensible API that allows dynamically loaded
modules (and scripts!) to register new streams.

The aim of the Streams API is to make it comfortable for developers to
open files, URLs and other streamable data sources with a unified API
that is easy to understand. The API is more or less based on the ANSI C
stdio family of functions (with identical semantics for most of the main
functions), so C programmers will have a feeling of familiarity with
streams.

The streams API operates on a couple of different levels: at the base
level, the API defines php\_stream objects to represent streamable data
sources. On a slightly higher level, the API defines
php\_stream\_wrapper objects which "wrap" around the lower level API to
provide support for retrieving data and meta-data from URLs. An
additional *context* parameter, accepted by most stream creation
functions, is passed to the wrapper's *stream\_opener* method to
fine-tune the behavior of the wrapper.

Any stream, once opened, can also have any number of *filters* applied
to it, which process data as it is read from/written to the stream.

Streams can be cast (converted) into other types of file-handles, so
that they can be used with third-party libraries without a great deal of
trouble. This allows those libraries to access data directly from URL
sources. If your system has the <span
class="function">fopencookie</span> or <span
class="function">funopen</span> function, you can even pass any PHP
stream to any library that uses ANSI stdio!

### Streams Basics

Using streams is very much like using ANSI stdio functions. The main
difference is in how you obtain the stream handle to begin with. In most
cases, you will use <span
class="function">php\_stream\_open\_wrapper</span> to obtain the stream
handle. This function works very much like fopen, as can be seen from
the example below:

**示例 \#1 simple stream example that displays the PHP home page**

``` c
php_stream * stream = php_stream_open_wrapper("http://www.php.net", "rb", REPORT_ERRORS, NULL);
if (stream) {
    while(!php_stream_eof(stream)) {
        char buf[1024];
        
        if (php_stream_gets(stream, buf, sizeof(buf))) {
            printf(buf);
        } else {
            break;
        }
    }
    php_stream_close(stream);
}
```

The table below shows the Streams equivalents of the more common ANSI
stdio functions. Unless noted otherwise, the semantics of the functions
are identical.

| ANSI Stdio Function | PHP Streams Function       | Notes                                                                                          |
|---------------------|----------------------------|------------------------------------------------------------------------------------------------|
| fopen               | php\_stream\_open\_wrapper | Streams includes additional parameters                                                         |
| fclose              | php\_stream\_close         |                                                                                                |
| fgets               | php\_stream\_gets          |                                                                                                |
| fread               | php\_stream\_read          | The nmemb parameter is assumed to have a value of 1, so the prototype looks more like read(2)  |
| fwrite              | php\_stream\_write         | The nmemb parameter is assumed to have a value of 1, so the prototype looks more like write(2) |
| fseek               | php\_stream\_seek          |                                                                                                |
| ftell               | php\_stream\_tell          |                                                                                                |
| rewind              | php\_stream\_rewind        |                                                                                                |
| feof                | php\_stream\_eof           |                                                                                                |
| fgetc               | php\_stream\_getc          |                                                                                                |
| fputc               | php\_stream\_putc          |                                                                                                |
| fflush              | php\_stream\_flush         |                                                                                                |
| puts                | php\_stream\_puts          | Same semantics as puts, NOT fputs                                                              |
| fstat               | php\_stream\_stat          | Streams has a richer stat structure                                                            |

### Streams as Resources

All streams are registered as resources when they are created. This
ensures that they will be properly cleaned up even if there is some
fatal error. All of the filesystem functions in PHP operate on streams
resources - that means that your extensions can accept regular PHP file
pointers as parameters to, and return streams from their functions. The
streams API makes this process as painless as possible:

**示例 \#2 How to accept a stream as a parameter**

``` c
PHP_FUNCTION(example_write_hello)
{
    zval *zstream;
    php_stream *stream;
    
    if (FAILURE == zend_parse_parameters(ZEND_NUM_ARGS() TSRMLS_CC, "r", &zstream))
        return;
    
    php_stream_from_zval(stream, &zstream);

    /* you can now use the stream.  However, you do not "own" the
        stream, the script does.  That means you MUST NOT close the
        stream, because it will cause PHP to crash! */

    php_stream_write(stream, "hello\n");
        
    RETURN_TRUE();
}
```

**示例 \#3 How to return a stream from a function**

``` c
PHP_FUNCTION(example_open_php_home_page)
{
    php_stream *stream;
    
    stream = php_stream_open_wrapper("http://www.php.net", "rb", REPORT_ERRORS, NULL);
    
    php_stream_to_zval(stream, return_value);

    /* after this point, the stream is "owned" by the script.
        If you close it now, you will crash PHP! */
}
```

Since streams are automatically cleaned up, it's tempting to think that
we can get away with being sloppy programmers and not bother to close
the streams when we are done with them. Although such an approach might
work, it is not a good idea for a number of reasons: streams hold locks
on system resources while they are open, so leaving a file open after
you have finished with it could prevent other processes from accessing
it. If a script deals with a large number of files, the accumulation of
the resources used, both in terms of memory and the sheer number of open
files, can cause web server requests to fail. Sounds bad, doesn't it?
The streams API includes some magic that helps you to keep your code
clean - if a stream is not closed by your code when it should be, you
will find some helpful debugging information in you web server error
log.

> **Note**: <span class="simpara"> Always use a debug build of PHP when
> developing an extension (**--enable-debug** when running configure),
> as a lot of effort has been made to warn you about memory and stream
> leaks. </span>

In some cases, it is useful to keep a stream open for the duration of a
request, to act as a log or trace file for example. Writing the code to
safely clean up such a stream is not difficult, but it's several lines
of code that are not strictly needed. To save yourself the trouble of
writing the code, you can mark a stream as being OK for auto cleanup.
What this means is that the streams API will not emit a warning when it
is time to auto-cleanup a stream. To do this, you can use <span
class="function">php\_stream\_auto\_cleanup</span>.

### Streams open options

These constants affect the operation of stream factory functions.

**`IGNORE_PATH`**  
<span class="simpara"> This is the default option for streams; it
requests that the include\_path is not to be searched for the requested
file. </span>

**`USE_PATH`**  
<span class="simpara"> Requests that the include\_path is to be searched
for the requested file. </span>

**`IGNORE_URL`**  
<span class="simpara"> Requests that registered URL wrappers are to be
ignored when opening the stream. Other non-URL wrappers will be taken
into consideration when decoding the path. There is no opposite form for
this flag; the streams API will use all registered wrappers by default.
</span>

**`IGNORE_URL_WIN`**  
<span class="simpara"> On Windows systems, this is equivalent to
IGNORE\_URL. On all other systems, this flag has no effect. </span>

**`ENFORCE_SAFE_MODE`**  
<span class="simpara"> Requests that the underlying stream
implementation perform safe\_mode checks on the file before opening the
file. Omitting this flag will skip safe\_mode checks and allow opening
of any file that the PHP process has rights to access. </span>

**`REPORT_ERRORS`**  
<span class="simpara"> If this flag is set, and there was an error
during the opening of the file or URL, the streams API will call the
php\_error function for you. This is useful because the path may contain
username/password information that should not be displayed in the
browser output (it would be a security risk to do so). When the streams
API raises the error, it first strips username/password information from
the path, making the error message safe to display in the browser.
</span>

**`STREAM_MUST_SEEK`**  
<span class="simpara"> This flag is useful when your extension really
must be able to randomly seek around in a stream. Some streams may not
be seekable in their native form, so this flag asks the streams API to
check to see if the stream does support seeking. If it does not, it will
copy the stream into temporary storage (which may be a temporary file or
a memory stream) which does support seeking. Please note that this flag
is not useful when you want to seek the stream and write to it, because
the stream you are accessing might not be bound to the actual resource
you requested. </span>

> **Note**: <span class="simpara"> If the requested resource is network
> based, this flag will cause the opener to block until the whole
> contents have been downloaded. </span>

**`STREAM_WILL_CAST`**  
<span class="simpara"> If your extension is using a third-party library
that expects a FILE\* or file descriptor, you can use this flag to
request the streams API to open the resource but avoid buffering. You
can then use <span class="function">php\_stream\_cast</span> to retrieve
the FILE\* or file descriptor that the library requires. </span> <span
class="simpara"> The is particularly useful when accessing HTTP URLs
where the start of the actual stream data is found after an
indeterminate offset into the stream. </span> <span class="simpara">
Since this option disables buffering at the streams API level, you may
experience lower performance when using streams functions on the stream;
this is deemed acceptable because you have told streams that you will be
using the functions to match the underlying stream implementation. Only
use this option when you are sure you need it. </span>
