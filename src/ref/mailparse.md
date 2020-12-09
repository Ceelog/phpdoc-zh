mailparse\_determine\_best\_xfer\_encoding
==========================================

Gets the best way of encoding

### 说明

<span class="type">string</span> <span
class="methodname">mailparse\_determine\_best\_xfer\_encoding</span> (
<span class="methodparam"><span class="type">resource</span>
`$fp`</span> )

Figures out the best way of encoding the content read from the given
file pointer.

### 参数

`fp`  
A valid file pointer, which must be seek-able.

### 返回值

Returns one of the character encodings supported by the
<a href="/ref/mbstring.html" class="link">mbstring</a> module.

### 范例

**示例 \#1 <span
class="function">mailparse\_determine\_best\_xfer\_encoding</span>
example**

``` php
<?php

$fp = fopen('somemail.eml', 'r');
echo 'Best encoding: ' . mailparse_determine_best_xfer_encoding($fp);

?>
```

以上例程的输出类似于：

    Best encoding: 7bit

mailparse\_msg\_create
======================

Create a mime mail resource

### 说明

<span class="type">resource</span> <span
class="methodname">mailparse\_msg\_create</span> ( <span
class="methodparam">void</span> )

Create a *MIME* mail resource.

### 返回值

Returns a handle that can be used to parse a message.

### 参见

-   <span class="function">mailparse\_msg\_free</span>
-   <span class="function">mailparse\_msg\_parse\_file</span>

mailparse\_msg\_extract\_part\_file
===================================

Extracts/decodes a message section

### 说明

<span class="type">string</span> <span
class="methodname">mailparse\_msg\_extract\_part\_file</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> , <span class="methodparam"><span
class="type">mixed</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$callbackfunc`</span> \] )

Extracts/decodes a message section from the supplied filename.

The contents of the section will be decoded according to their transfer
encoding - base64, quoted-printable and uuencoded text are supported.

### 参数

`mimemail`  
A valid *MIME* resource, created with <span
class="function">mailparse\_msg\_create</span>.

`filename`  
Can be a file name or a valid stream resource.

`callbackfunc`  
If set, this must be either a valid callback that will be passed the
extracted section, or **`null`** to make this function return the
extracted section.

If not specified, the contents will be sent to "stdout".

### 返回值

If `callbackfunc` is not **`null`** returns **`true`** on success.

If `callbackfunc` is set to **`null`**, returns the extracted section as
a string.

Returns **`false`** on error.

### 参见

-   <span class="function">mailparse\_msg\_extract\_part</span>
-   <span
    class="function">mailparse\_msg\_extract\_whole\_part\_file</span>

mailparse\_msg\_extract\_part
=============================

Extracts/decodes a message section

### 说明

<span class="type">void</span> <span
class="methodname">mailparse\_msg\_extract\_part</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> , <span class="methodparam"><span
class="type">string</span> `$msgbody`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$callbackfunc`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`mimemail`  
A valid *MIME* resource.

`msgbody`  

`callbackfunc`  

### 返回值

没有返回值。

### 参见

-   <span class="function">mailparse\_msg\_extract\_part\_file</span>
-   <span
    class="function">mailparse\_msg\_extract\_whole\_part\_file</span>

mailparse\_msg\_extract\_whole\_part\_file
==========================================

Extracts a message section including headers without decoding the
transfer encoding

### 说明

<span class="type">string</span> <span
class="methodname">mailparse\_msg\_extract\_whole\_part\_file</span> (
<span class="methodparam"><span class="type">resource</span>
`$mimemail`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$callbackfunc`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`mimemail`  
A valid *MIME* resource.

`filename`  

`callbackfunc`  

### 返回值

### 参见

-   <span class="function">mailparse\_msg\_extract\_part</span>
-   <span class="function">mailparse\_msg\_extract\_part\_file</span>

mailparse\_msg\_free
====================

Frees a MIME resource

### 说明

<span class="type">bool</span> <span
class="methodname">mailparse\_msg\_free</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> )

Frees a *MIME* resource.

### 参数

`mimemail`  
A valid *MIME* resource allocated by <span
class="function">mailparse\_msg\_create</span> or <span
class="function">mailparse\_msg\_parse\_file</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">mailparse\_msg\_create</span>
-   <span class="function">mailparse\_msg\_parse\_file</span>

mailparse\_msg\_get\_part\_data
===============================

Returns an associative array of info about the message

### 说明

<span class="type">array</span> <span
class="methodname">mailparse\_msg\_get\_part\_data</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`mimemail`  
A valid *MIME* resource.

mailparse\_msg\_get\_part
=========================

Returns a handle on a given section in a mimemessage

### 说明

<span class="type">resource</span> <span
class="methodname">mailparse\_msg\_get\_part</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> , <span class="methodparam"><span
class="type">string</span> `$mimesection`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`mimemail`  
A valid *MIME* resource.

`mimesection`  

mailparse\_msg\_get\_structure
==============================

Returns an array of mime section names in the supplied message

### 说明

<span class="type">array</span> <span
class="methodname">mailparse\_msg\_get\_structure</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`mimemail`  
A valid *MIME* resource.

mailparse\_msg\_parse\_file
===========================

Parses a file

### 说明

<span class="type">resource</span> <span
class="methodname">mailparse\_msg\_parse\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Parses a file. This is the optimal way of parsing a mail file that you
have on disk.

### 参数

`filename`  
Path to the file holding the message. The file is opened and streamed
through the parser.

> **Note**:
>
> The message contained in `filename` is supposed to end with a newline
> (*CRLF*); otherwise the last line of the message will not be parsed.

### 返回值

Returns a *MIME* resource representing the structure, or **`false`** on
error.

### 参见

-   <span class="function">mailparse\_msg\_free</span>
-   <span class="function">mailparse\_msg\_create</span>

mailparse\_msg\_parse
=====================

Incrementally parse data into buffer

### 说明

<span class="type">bool</span> <span
class="methodname">mailparse\_msg\_parse</span> ( <span
class="methodparam"><span class="type">resource</span>
`$mimemail`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> )

Incrementally parse data into the supplied mime mail resource.

This function allow you to stream portions of a file at a time, rather
than read and parse the whole thing.

### 参数

`mimemail`  
A valid *MIME* resource.

`data`  
> **Note**:
>
> The final chunk of `data` is supposed to end with a newline (*CRLF*);
> otherwise the last line of the message will not be parsed.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

mailparse\_rfc822\_parse\_addresses
===================================

Parse RFC 822 compliant addresses

### 说明

<span class="type">array</span> <span
class="methodname">mailparse\_rfc822\_parse\_addresses</span> ( <span
class="methodparam"><span class="type">string</span> `$addresses`</span>
)

Parses a
<a href="http://www.faqs.org/rfcs/rfc822" class="link external">» RFC 822</a>
compliant recipient list, such as that found in the *To:* header.

### 参数

`addresses`  
A string containing addresses, like in: *Wez Furlong
\<wez@example.com\>, doe@example.com*

> **Note**:
>
> This string must not include the header name.

### 返回值

Returns an array of associative arrays with the following keys for each
recipient:

|             |                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------|
| *display*   | The recipient name, for display purpose. If this part is not set for a recipient, this key will hold the same value as *address*. |
| *address*   | The email address                                                                                                                 |
| *is\_group* | **`true`** if the recipient is a newsgroup, **`false`** otherwise.                                                                |

### 范例

**示例 \#1 <span
class="function">mailparse\_rfc822\_parse\_addresses</span> example**

``` php
<?php

$to = 'Wez Furlong <wez@example.com>, doe@example.com';
var_dump(mailparse_rfc822_parse_addresses($to));

?>
```

以上例程会输出：

    array(2) {
      [0]=>
      array(3) {
        ["display"]=>
        string(11) "Wez Furlong"
        ["address"]=>
        string(15) "wez@example.com"
        ["is_group"]=>
        bool(false)
      }
      [1]=>
      array(3) {
        ["display"]=>
        string(15) "doe@example.com"
        ["address"]=>
        string(15) "doe@example.com"
        ["is_group"]=>
        bool(false)
      }
    }

mailparse\_stream\_encode
=========================

Streams data from source file pointer, apply encoding and write to
destfp

### 说明

<span class="type">bool</span> <span
class="methodname">mailparse\_stream\_encode</span> ( <span
class="methodparam"><span class="type">resource</span>
`$sourcefp`</span> , <span class="methodparam"><span
class="type">resource</span> `$destfp`</span> , <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

Streams data from the source file pointer, apply `encoding` and write to
the destination file pointer.

### 参数

`sourcefp`  
A valid file handle. The file is streamed through the parser.

`destfp`  
The destination file handle in which the encoded data will be written.

`encoding`  
One of the character encodings supported by the
<a href="/ref/mbstring.html" class="link">mbstring</a> module.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">mailparse\_stream\_encode</span>
example**

``` php
<?php

// email.eml contents: hello, this is some text=hello.
$fp = fopen('email.eml', 'r');

$dest = tmpfile();

mailparse_stream_encode($fp, $dest, "quoted-printable");

rewind($dest);

// Display new file contents
fpassthru($dest);

?>
```

以上例程会输出：

    hello, this is some text=3Dhello.

mailparse\_uudecode\_all
========================

Scans the data from fp and extract each embedded uuencoded file

### 说明

<span class="type">array</span> <span
class="methodname">mailparse\_uudecode\_all</span> ( <span
class="methodparam"><span class="type">resource</span> `$fp`</span> )

Scans the data from the given file pointer and extract each embedded
uuencoded file into a temporary file.

### 参数

`fp`  
A valid file pointer.

### 返回值

Returns an array of associative arrays listing filename information.

|                |                                                 |
|----------------|-------------------------------------------------|
| *filename*     | Path to the temporary file name created         |
| *origfilename* | The original filename, for uuencoded parts only |

The first filename entry is the message body. The next entries are the
decoded uuencoded files.

### 范例

**示例 \#1 <span class="function">mailparse\_uudecode\_all</span>
example**

``` php
<?php

$text = <<<EOD
To: fred@example.com

hello, this is some text hello.
blah blah blah.

begin 644 test.txt
/=&AI<R!I<R!A('1E<W0*
`
end

EOD;

$fp = tmpfile();
fwrite($fp, $text);

$data = mailparse_uudecode_all($fp);

echo "BODY\n";
readfile($data[0]["filename"]);
echo "UUE ({$data[1]['origfilename']})\n";
readfile($data[1]["filename"]);

// Clean up
unlink($data[0]["filename"]);
unlink($data[1]["filename"]);

?>
```

以上例程会输出：

    BODY
    To: fred@example.com

    hello, this is some text hello.
    blah blah blah.

    UUE (test.txt)
    this is a test

**目录**

-   [mailparse\_determine\_best\_xfer\_encoding](/ref/mailparse.html#mailparse_determine_best_xfer_encoding)
    — Gets the best way of encoding
-   [mailparse\_msg\_create](/ref/mailparse.html#mailparse_msg_create) —
    Create a mime mail resource
-   [mailparse\_msg\_extract\_part\_file](/ref/mailparse.html#mailparse_msg_extract_part_file)
    — Extracts/decodes a message section
-   [mailparse\_msg\_extract\_part](/ref/mailparse.html#mailparse_msg_extract_part)
    — Extracts/decodes a message section
-   [mailparse\_msg\_extract\_whole\_part\_file](/ref/mailparse.html#mailparse_msg_extract_whole_part_file)
    — Extracts a message section including headers without decoding the
    transfer encoding
-   [mailparse\_msg\_free](/ref/mailparse.html#mailparse_msg_free) —
    Frees a MIME resource
-   [mailparse\_msg\_get\_part\_data](/ref/mailparse.html#mailparse_msg_get_part_data)
    — Returns an associative array of info about the message
-   [mailparse\_msg\_get\_part](/ref/mailparse.html#mailparse_msg_get_part)
    — Returns a handle on a given section in a mimemessage
-   [mailparse\_msg\_get\_structure](/ref/mailparse.html#mailparse_msg_get_structure)
    — Returns an array of mime section names in the supplied message
-   [mailparse\_msg\_parse\_file](/ref/mailparse.html#mailparse_msg_parse_file)
    — Parses a file
-   [mailparse\_msg\_parse](/ref/mailparse.html#mailparse_msg_parse) —
    Incrementally parse data into buffer
-   [mailparse\_rfc822\_parse\_addresses](/ref/mailparse.html#mailparse_rfc822_parse_addresses)
    — Parse RFC 822 compliant addresses
-   [mailparse\_stream\_encode](/ref/mailparse.html#mailparse_stream_encode)
    — Streams data from source file pointer, apply encoding and write to
    destfp
-   [mailparse\_uudecode\_all](/ref/mailparse.html#mailparse_uudecode_all)
    — Scans the data from fp and extract each embedded uuencoded file
