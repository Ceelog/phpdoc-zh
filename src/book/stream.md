Streams
=======

**目录**

-   [简介](/intro/stream.html)
-   [安装／配置](/stream/setup.html)
    -   [需求](/stream/setup.html#需求)
    -   [安装](/stream/setup.html#安装)
    -   [运行时配置](/stream/setup.html#运行时配置)
    -   [Stream Classes](/stream/setup.html#Stream%20Classes)
-   [预定义常量](/stream/constants.html)
-   [Stream Filters](/stream/filters.html)
-   [Stream Contexts](/stream/contexts.html)
-   [Stream Errors](/stream/errors.html)
-   [范例](/stream/examples.html)
    -   [Example class registered as stream
        wrapper](/stream/examples.html#Example%20class%20registered%20as%20stream%20wrapper)
-   [php\_user\_filter](/class/php-user-filter.html) — The
    php\_user\_filter class
    -   [php\_user\_filter::filter](/class/php-user-filter.html#php_user_filter::filter)
        — Called when applying the filter
    -   [php\_user\_filter::onClose](/class/php-user-filter.html#php_user_filter::onClose)
        — Called when closing the filter
    -   [php\_user\_filter::onCreate](/class/php-user-filter.html#php_user_filter::onCreate)
        — Called when creating the filter
-   [streamWrapper](/class/streamwrapper.html) — The streamWrapper class
    -   [streamWrapper::\_\_construct](/class/streamwrapper.html#streamWrapper::__construct)
        — Constructs a new stream wrapper
    -   [streamWrapper::\_\_destruct](/class/streamwrapper.html#streamWrapper::__destruct)
        — Destructs an existing stream wrapper
    -   [streamWrapper::dir\_closedir](/class/streamwrapper.html#streamWrapper::dir_closedir)
        — Close directory handle
    -   [streamWrapper::dir\_opendir](/class/streamwrapper.html#streamWrapper::dir_opendir)
        — Open directory handle
    -   [streamWrapper::dir\_readdir](/class/streamwrapper.html#streamWrapper::dir_readdir)
        — Read entry from directory handle
    -   [streamWrapper::dir\_rewinddir](/class/streamwrapper.html#streamWrapper::dir_rewinddir)
        — Rewind directory handle
    -   [streamWrapper::mkdir](/class/streamwrapper.html#streamWrapper::mkdir)
        — Create a directory
    -   [streamWrapper::rename](/class/streamwrapper.html#streamWrapper::rename)
        — Renames a file or directory
    -   [streamWrapper::rmdir](/class/streamwrapper.html#streamWrapper::rmdir)
        — Removes a directory
    -   [streamWrapper::stream\_cast](/class/streamwrapper.html#streamWrapper::stream_cast)
        — Retrieve the underlaying resource
    -   [streamWrapper::stream\_close](/class/streamwrapper.html#streamWrapper::stream_close)
        — Close a resource
    -   [streamWrapper::stream\_eof](/class/streamwrapper.html#streamWrapper::stream_eof)
        — Tests for end-of-file on a file pointer
    -   [streamWrapper::stream\_flush](/class/streamwrapper.html#streamWrapper::stream_flush)
        — Flushes the output
    -   [streamWrapper::stream\_lock](/class/streamwrapper.html#streamWrapper::stream_lock)
        — Advisory file locking
    -   [streamWrapper::stream\_metadata](/class/streamwrapper.html#streamWrapper::stream_metadata)
        — Change stream metadata
    -   [streamWrapper::stream\_open](/class/streamwrapper.html#streamWrapper::stream_open)
        — Opens file or URL
    -   [streamWrapper::stream\_read](/class/streamwrapper.html#streamWrapper::stream_read)
        — Read from stream
    -   [streamWrapper::stream\_seek](/class/streamwrapper.html#streamWrapper::stream_seek)
        — Seeks to specific location in a stream
    -   [streamWrapper::stream\_set\_option](/class/streamwrapper.html#streamWrapper::stream_set_option)
        — Change stream options
    -   [streamWrapper::stream\_stat](/class/streamwrapper.html#streamWrapper::stream_stat)
        — Retrieve information about a file resource
    -   [streamWrapper::stream\_tell](/class/streamwrapper.html#streamWrapper::stream_tell)
        — Retrieve the current position of a stream
    -   [streamWrapper::stream\_truncate](/class/streamwrapper.html#streamWrapper::stream_truncate)
        — Truncate stream
    -   [streamWrapper::stream\_write](/class/streamwrapper.html#streamWrapper::stream_write)
        — Write to stream
    -   [streamWrapper::unlink](/class/streamwrapper.html#streamWrapper::unlink)
        — Delete a file
    -   [streamWrapper::url\_stat](/class/streamwrapper.html#streamWrapper::url_stat)
        — Retrieve information about a file
-   [Stream 函数](/ref/stream.html)
    -   [set\_socket\_blocking](/ref/stream.html#set_socket_blocking) —
        别名 stream\_set\_blocking
    -   [stream\_bucket\_append](/ref/stream.html#stream_bucket_append)
        — Append bucket to brigade
    -   [stream\_bucket\_make\_writeable](/ref/stream.html#stream_bucket_make_writeable)
        — Return a bucket object from the brigade for operating on
    -   [stream\_bucket\_new](/ref/stream.html#stream_bucket_new) —
        Create a new bucket for use on the current stream
    -   [stream\_bucket\_prepend](/ref/stream.html#stream_bucket_prepend)
        — Prepend bucket to brigade
    -   [stream\_context\_create](/ref/stream.html#stream_context_create)
        — 创建资源流上下文
    -   [stream\_context\_get\_default](/ref/stream.html#stream_context_get_default)
        — Retrieve the default stream context
    -   [stream\_context\_get\_options](/ref/stream.html#stream_context_get_options)
        — 获取资源流/数据包/上下文的参数
    -   [stream\_context\_get\_params](/ref/stream.html#stream_context_get_params)
        — Retrieves parameters from a context
    -   [stream\_context\_set\_default](/ref/stream.html#stream_context_set_default)
        — Set the default stream context
    -   [stream\_context\_set\_option](/ref/stream.html#stream_context_set_option)
        — 对资源流、数据包或者上下文设置参数
    -   [stream\_context\_set\_params](/ref/stream.html#stream_context_set_params)
        — Set parameters for a stream/wrapper/context
    -   [stream\_copy\_to\_stream](/ref/stream.html#stream_copy_to_stream)
        — Copies data from one stream to another
    -   [stream\_filter\_append](/ref/stream.html#stream_filter_append)
        — Attach a filter to a stream
    -   [stream\_filter\_prepend](/ref/stream.html#stream_filter_prepend)
        — Attach a filter to a stream
    -   [stream\_filter\_register](/ref/stream.html#stream_filter_register)
        — Register a user defined stream filter
    -   [stream\_filter\_remove](/ref/stream.html#stream_filter_remove)
        — 从资源流里移除某个过滤器
    -   [stream\_get\_contents](/ref/stream.html#stream_get_contents) —
        读取资源流到一个字符串
    -   [stream\_get\_filters](/ref/stream.html#stream_get_filters) —
        获取已注册的数据流过滤器列表
    -   [stream\_get\_line](/ref/stream.html#stream_get_line) —
        从资源流里读取一行直到给定的定界符
    -   [stream\_get\_meta\_data](/ref/stream.html#stream_get_meta_data)
        — 从封装协议文件指针中取得报头／元数据
    -   [stream\_get\_transports](/ref/stream.html#stream_get_transports)
        — 获取已注册的套接字传输协议列表
    -   [stream\_get\_wrappers](/ref/stream.html#stream_get_wrappers) —
        获取已注册的流类型
    -   [stream\_is\_local](/ref/stream.html#stream_is_local) — Checks
        if a stream is a local stream
    -   [stream\_isatty](/ref/stream.html#stream_isatty) — Check if a
        stream is a TTY
    -   [stream\_notification\_callback](/ref/stream.html#stream_notification_callback)
        — A callback function for the notification context parameter
    -   [stream\_register\_wrapper](/ref/stream.html#stream_register_wrapper)
        — 别名 stream\_wrapper\_register
    -   [stream\_resolve\_include\_path](/ref/stream.html#stream_resolve_include_path)
        — Resolve filename against the include path
    -   [stream\_select](/ref/stream.html#stream_select) — Runs the
        equivalent of the select() system call on the given arrays of
        streams with a timeout specified by tv\_sec and tv\_usec
    -   [stream\_set\_blocking](/ref/stream.html#stream_set_blocking) —
        为资源流设置阻塞或者阻塞模式
    -   [stream\_set\_chunk\_size](/ref/stream.html#stream_set_chunk_size)
        — 设置资源流区块大小
    -   [stream\_set\_read\_buffer](/ref/stream.html#stream_set_read_buffer)
        — Set read file buffering on the given stream
    -   [stream\_set\_timeout](/ref/stream.html#stream_set_timeout) —
        Set timeout period on a stream
    -   [stream\_set\_write\_buffer](/ref/stream.html#stream_set_write_buffer)
        — Sets write file buffering on the given stream
    -   [stream\_socket\_accept](/ref/stream.html#stream_socket_accept)
        — 接受由 stream\_socket\_server 创建的套接字连接
    -   [stream\_socket\_client](/ref/stream.html#stream_socket_client)
        — Open Internet or Unix domain socket connection
    -   [stream\_socket\_enable\_crypto](/ref/stream.html#stream_socket_enable_crypto)
        — Turns encryption on/off on an already connected socket
    -   [stream\_socket\_get\_name](/ref/stream.html#stream_socket_get_name)
        — 获取本地或者远程的套接字名称
    -   [stream\_socket\_pair](/ref/stream.html#stream_socket_pair) —
        创建一对完全一样的网络套接字连接流
    -   [stream\_socket\_recvfrom](/ref/stream.html#stream_socket_recvfrom)
        — Receives data from a socket, connected or not
    -   [stream\_socket\_sendto](/ref/stream.html#stream_socket_sendto)
        — Sends a message to a socket, whether it is connected or not
    -   [stream\_socket\_server](/ref/stream.html#stream_socket_server)
        — Create an Internet or Unix domain server socket
    -   [stream\_socket\_shutdown](/ref/stream.html#stream_socket_shutdown)
        — Shutdown a full-duplex connection
    -   [stream\_supports\_lock](/ref/stream.html#stream_supports_lock)
        — Tells whether the stream supports locking
    -   [stream\_wrapper\_register](/ref/stream.html#stream_wrapper_register)
        — 注册一个用 PHP 类实现的 URL 封装协议
    -   [stream\_wrapper\_restore](/ref/stream.html#stream_wrapper_restore)
        — Restores a previously unregistered built-in wrapper
    -   [stream\_wrapper\_unregister](/ref/stream.html#stream_wrapper_unregister)
        — Unregister a URL wrapper

简介
----

Children of this class are passed to <span
class="function">stream\_filter\_register</span>.

类摘要
------

**php\_user\_filter**

<span class="ooclass"> class **php\_user\_filter** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$filtername` ;

<span class="modifier">public</span> `$params` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">filter</span> ( <span class="methodparam"><span
class="type">resource</span> `$in`</span> , <span
class="methodparam"><span class="type">resource</span> `$out`</span> ,
<span class="methodparam"><span class="type">int</span>
`&$consumed`</span> , <span class="methodparam"><span
class="type">bool</span> `$closing`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">onClose</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">onCreate</span> ( <span
class="methodparam">void</span> )

}

属性
----

`filtername`  
Name of the filter registered by <span
class="function">stream\_filter\_append</span>.

`params`  

php\_user\_filter::filter
=========================

Called when applying the filter

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">php\_user\_filter::filter</span> ( <span
class="methodparam"><span class="type">resource</span> `$in`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$out`</span> , <span class="methodparam"><span class="type">int</span>
`&$consumed`</span> , <span class="methodparam"><span
class="type">bool</span> `$closing`</span> )

This method is called whenever data is read from or written to the
attached stream (such as with <span class="function">fread</span> or
<span class="function">fwrite</span>).

### 参数

`in`  
`in` is a resource pointing to a *bucket brigade* which contains one or
more *bucket* objects containing data to be filtered.

`out`  
`out` is a resource pointing to a second *bucket brigade* into which
your modified buckets should be placed.

`consumed`  
`consumed`, which must *always* be declared by reference, should be
incremented by the length of the data which your filter reads in and
alters. In most cases this means you will increment `consumed` by
*$bucket-\>datalen* for each *$bucket*.

`closing`  
If the stream is in the process of closing (and therefore this is the
last pass through the filterchain), the `closing` parameter will be set
to **`TRUE`**.

### 返回值

The <span class="methodname">filter</span> method must return one of
three values upon completion.

| Return Value                   | Meaning                                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **`PSFS_PASS_ON`**             | Filter processed successfully with data available in the `out` *bucket brigade*.                                               |
| **`PSFS_FEED_ME`**             | Filter processed successfully, however no data was available to return. More data is required from the stream or prior filter. |
| **`PSFS_ERR_FATAL`** (default) | The filter experienced an unrecoverable error and cannot continue.                                                             |

php\_user\_filter::onClose
==========================

Called when closing the filter

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">php\_user\_filter::onClose</span> ( <span
class="methodparam">void</span> )

This method is called upon filter shutdown (typically, this is also
during stream shutdown), and is executed *after* the *flush* method is
called. If any resources were allocated or initialized during
*onCreate()* this would be the time to destroy or dispose of them.

### 参数

此函数没有参数。

### 返回值

Return value is ignored.

php\_user\_filter::onCreate
===========================

Called when creating the filter

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">php\_user\_filter::onCreate</span> ( <span
class="methodparam">void</span> )

This method is called during instantiation of the filter class object.
If your filter allocates or initializes any other resources (such as a
buffer), this is the place to do it.

When your filter is first instantiated, and *yourfilter-\>onCreate()* is
called, a number of properties will be available as shown in the table
below.

| Property                   | Contents                                                                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *FilterClass-\>filtername* | A string containing the name the filter was instantiated with. Filters may be registered under multiple names or under wildcards. Use this property to determine which name was used. |
| *FilterClass-\>params*     | The contents of the `params` parameter passed to <span class="function">stream\_filter\_append</span> or <span class="function">stream\_filter\_prepend</span>.                       |
| *FilterClass-\>stream*     | The stream resource being filtered. Maybe available only during <span class="methodname">filter</span> calls when the *closing* parameter is set to **`FALSE`**.                      |

### 参数

此函数没有参数。

### 返回值

Your implementation of this method should return **`FALSE`** on failure,
or **`TRUE`** on success.

简介
----

Allows you to implement your own protocol handlers and streams for use
with all the other filesystem functions (such as <span
class="function">fopen</span>, <span class="function">fread</span>
etc.).

> **Note**:
>
> This is *NOT* a real class, only a prototype of how a class defining
> its own protocol should be.

> **Note**:
>
> Implementing the methods in other ways than described here can lead to
> undefined behaviour.

An instance of this class is initialized as soon as a stream function
tries to access the protocol it is associated with.

类摘要
------

**streamWrapper**

<span class="ooclass"> class **<span
class="replaceable">streamWrapper</span>** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">resource</span>
`$context` ;

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">dir\_closedir</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">dir\_opendir</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span>
`$options`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">dir\_readdir</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">dir\_rewinddir</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">mkdir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> , <span
class="methodparam"><span class="type">int</span> `$options`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">rename</span> ( <span class="methodparam"><span
class="type">string</span> `$path_from`</span> , <span
class="methodparam"><span class="type">string</span> `$path_to`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">rmdir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$options`</span> )

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">stream\_cast</span> ( <span
class="methodparam"><span class="type">int</span> `$cast_as`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">stream\_close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_eof</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_lock</span> ( <span
class="methodparam"><span class="type">int</span> `$operation`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_metadata</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$option`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_open</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$mode`</span> , <span class="methodparam"><span class="type">int</span>
`$options`</span> , <span class="methodparam"><span
class="type">string</span> `&$opened_path`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">stream\_read</span> ( <span
class="methodparam"><span class="type">int</span> `$count`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_seek</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$whence` <span
class="initializer"> = SEEK\_SET</span></span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_set\_option</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> ,
<span class="methodparam"><span class="type">int</span> `$arg1`</span> ,
<span class="methodparam"><span class="type">int</span> `$arg2`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">stream\_stat</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">stream\_tell</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stream\_truncate</span> ( <span
class="methodparam"><span class="type">int</span> `$new_size`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">stream\_write</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unlink</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">url\_stat</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
)

}

属性
----

resource `context`  
The current <a href="/context.html" class="link">context</a>, or
**`NULL`** if no context was passed to the caller function.

Use the <span class="function">stream\_context\_get\_options</span> to
parse the context.

> **Note**:
>
> This property *must* be public so PHP can populate it with the actual
> context resource.

参见
----

-   <a href="/stream/examples.html#Example%20class%20registered%20as%20stream%20wrapper" class="xref"></a>
-   <span class="function">stream\_wrapper\_register</span>
-   <span class="function">stream\_wrapper\_unregister</span>
-   <span class="function">stream\_wrapper\_restore</span>

streamWrapper::\_\_construct
============================

Constructs a new stream wrapper

### 说明

<span class="methodname">streamWrapper::\_\_construct</span> ( <span
class="methodparam">void</span> )

Called when opening the stream wrapper, right before <span
class="methodname">streamWrapper::stream\_open</span>.

### 参数

此函数没有参数。

streamWrapper::\_\_destruct
===========================

Destructs an existing stream wrapper

### 说明

<span class="methodname">streamWrapper::\_\_destruct</span> ( <span
class="methodparam">void</span> )

Called when closing the stream wrapper, right before <span
class="methodname">streamWrapper::stream\_flush</span>.

### 参数

此函数没有参数。

streamWrapper::dir\_closedir
============================

Close directory handle

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::dir\_closedir</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span
class="function">closedir</span>.

Any resources which were locked, or allocated, during opening and use of
the directory stream should be released.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">closedir</span>
-   <span class="methodname">streamWrapper::dir\_opendir</span>

streamWrapper::dir\_opendir
===========================

Open directory handle

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::dir\_opendir</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span>
`$options`</span> )

This method is called in response to <span
class="function">opendir</span>.

### 参数

`path`  
Specifies the URL that was passed to <span
class="function">opendir</span>.

> **Note**:
>
> The URL can be broken apart with <span
> class="function">parse\_url</span>.

`options`  
Whether or not to enforce
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>
(0x04).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">opendir</span>
-   <span class="methodname">streamWrapper::dir\_closedir</span>
-   <span class="function">parse\_url</span>

streamWrapper::dir\_readdir
===========================

Read entry from directory handle

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">streamWrapper::dir\_readdir</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span
class="function">readdir</span>.

### 参数

此函数没有参数。

### 返回值

Should return <span class="type">string</span> representing the next
filename, or **`FALSE`** if there is no next file.

> **Note**:
>
> The return value will be casted to <span class="type">string</span>.

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 范例

**示例 \#1 Listing files from tar archives**

``` php
<?php
class streamWrapper {
    protected $fp;

    public function dir_opendir($path, $options) {
        $url = parse_url($path);

        $path = $url["host"] . $url["path"];

        if (!is_readable($path)) {
            trigger_error("$path isn't readable for me", E_USER_NOTICE);
            return false;
        }
        if (!is_file($path)) {
            trigger_error("$path isn't a file", E_USER_NOTICE);
            return false;
        }

        $this->fp = fopen($path, "rb");
        return true;
    }

    public function dir_readdir() {
        // Extract the header for this entry
        $header      = fread($this->fp, 512);
        $data = unpack("a100filename/a8mode/a8uid/a8gid/a12size/a12mtime/a8checksum/a1filetype/a100link/a100linkedfile", $header);

        // Trim the filename and filesize
        $filename    = trim($data["filename"]);

        // No filename? We are the end of the archive
        if (!$filename) {
            return false;
        }

        $octal_bytes = trim($data["size"]);
        // Filesize is defined in octects
        $bytes       = octdec($octal_bytes);

        // tar rounds up filesizes up to multiple of 512 bytes (zero filled)
        $rest        = $bytes % 512;
        if ($rest > 0) {
            $bytes      += 512 - $rest;
        }

        // Seek over the file
        fseek($this->fp, $bytes, SEEK_CUR);

        return $filename;
    }

    public function dir_closedir() {
        return fclose($this->fp);
    }

    public function dir_rewinddir() {
        return fseek($this->fp, 0, SEEK_SET);
    }
}

stream_wrapper_register("tar", "streamWrapper");
$handle = opendir("tar://example.tar");
while (false !== ($file = readdir($handle))) {
    var_dump($file);
}

echo "Rewinding..\n";
rewind($handle);
var_dump(readdir($handle));

closedir($handle);
?>
```

以上例程的输出类似于：

    string(13) "construct.xml"
    string(16) "dir-closedir.xml"
    string(15) "dir-opendir.xml"
    string(15) "dir-readdir.xml"
    string(17) "dir-rewinddir.xml"
    string(9) "mkdir.xml"
    string(10) "rename.xml"
    string(9) "rmdir.xml"
    string(15) "stream-cast.xml"
    string(16) "stream-close.xml"
    string(14) "stream-eof.xml"
    string(16) "stream-flush.xml"
    string(15) "stream-lock.xml"
    string(15) "stream-open.xml"
    string(15) "stream-read.xml"
    string(15) "stream-seek.xml"
    string(21) "stream-set-option.xml"
    string(15) "stream-stat.xml"
    string(15) "stream-tell.xml"
    string(16) "stream-write.xml"
    string(10) "unlink.xml"
    string(12) "url-stat.xml"
    Rewinding..
    string(13) "construct.xml"

### 参见

-   <span class="function">readdir</span>

streamWrapper::dir\_rewinddir
=============================

Rewind directory handle

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::dir\_rewinddir</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span
class="function">rewinddir</span>.

Should reset the output generated by <span
class="methodname">streamWrapper::dir\_readdir</span>. i.e.: The next
call to <span class="methodname">streamWrapper::dir\_readdir</span>
should return the first entry in the location returned by <span
class="methodname">streamWrapper::dir\_opendir</span>.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">rewinddir</span>
-   <span class="methodname">streamWrapper::dir\_readdir</span>

streamWrapper::mkdir
====================

Create a directory

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::mkdir</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$mode`</span> ,
<span class="methodparam"><span class="type">int</span>
`$options`</span> )

This method is called in response to <span
class="function">mkdir</span>.

> **Note**:
>
> In order for the appropriate error message to be returned this method
> should *not* be defined if the wrapper does not support creating
> directories.

### 参数

`path`  
Directory which should be created.

`mode`  
The value passed to <span class="function">mkdir</span>.

`options`  
A bitwise mask of values, such as **`STREAM_MKDIR_RECURSIVE`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 注释

> **Note**:
>
> 当合法的上下文传递给调用函数时，属性 `streamWrapper::$context`
> 会被改变。

### 参见

-   <span class="function">mkdir</span>
-   <span class="methodname">streamwrapper::rmdir</span>

streamWrapper::rename
=====================

Renames a file or directory

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::rename</span> ( <span
class="methodparam"><span class="type">string</span> `$path_from`</span>
, <span class="methodparam"><span class="type">string</span>
`$path_to`</span> )

This method is called in response to <span
class="function">rename</span>.

Should attempt to rename `path_from` to `path_to`

> **Note**:
>
> In order for the appropriate error message to be returned this method
> should *not* be defined if the wrapper does not support renaming
> files.

### 参数

`path_from`  
The URL to the current file.

`path_to`  
The URL which the `path_from` should be renamed to.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 注释

> **Note**:
>
> 当合法的上下文传递给调用函数时，属性 `streamWrapper::$context`
> 会被改变。

### 参见

-   <span class="function">rename</span>

streamWrapper::rmdir
====================

Removes a directory

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::rmdir</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span>
`$options`</span> )

This method is called in response to <span
class="function">rmdir</span>.

> **Note**:
>
> In order for the appropriate error message to be returned this method
> should *not* be defined if the wrapper does not support removing
> directories.

### 参数

`path`  
The directory URL which should be removed.

`options`  
A bitwise mask of values, such as **`STREAM_MKDIR_RECURSIVE`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 注释

> **Note**:
>
> 当合法的上下文传递给调用函数时，属性 `streamWrapper::$context`
> 会被改变。

### 参见

-   <span class="function">rmdir</span>
-   <span class="methodname">streamwrapper::mkdir</span>
-   <span class="methodname">streamwrapper::unlink</span>

streamWrapper::stream\_cast
===========================

Retrieve the underlaying resource

### 说明

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">streamWrapper::stream\_cast</span> ( <span
class="methodparam"><span class="type">int</span> `$cast_as`</span> )

This method is called in response to <span
class="function">stream\_select</span>.

### 参数

`cast_as`  
Can be **`STREAM_CAST_FOR_SELECT`** when <span
class="function">stream\_select</span> is calling <span
class="function">stream\_cast</span> or **`STREAM_CAST_AS_STREAM`** when
<span class="function">stream\_cast</span> is called for other uses.

### 返回值

Should return the underlying stream resource used by the wrapper, or
**`FALSE`**.

### 参见

-   <span class="function">stream\_select</span>

streamWrapper::stream\_close
============================

Close a resource

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">streamWrapper::stream\_close</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span
class="function">fclose</span>.

All resources that were locked, or allocated, by the wrapper should be
released.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="function">fclose</span>
-   <span class="methodname">streamWrapper::dir\_closedir</span>

streamWrapper::stream\_eof
==========================

Tests for end-of-file on a file pointer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_eof</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span class="function">feof</span>.

### 参数

此函数没有参数。

### 返回值

Should return **`TRUE`** if the read/write position is at the end of the
stream and if no more data is available to be read, or **`FALSE`**
otherwise.

### 注释

**Warning**

When reading the whole file (for example, with <span
class="function">file\_get\_contents</span>), PHP will call <span
class="methodname">streamWrapper::stream\_read</span> followed by <span
class="methodname">streamWrapper::stream\_eof</span> in a loop but as
long as <span class="methodname">streamWrapper::stream\_read</span>
returns a non-empty string, the return value of <span
class="methodname">streamWrapper::stream\_eof</span> is ignored.

### 参见

-   <span class="function">feof</span>

streamWrapper::stream\_flush
============================

Flushes the output

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_flush</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span
class="function">fflush</span> and when the stream is being closed while
any unflushed data has been written to it before.

If you have cached data in your stream but not yet stored it into the
underlying storage, you should do so now.

### 参数

此函数没有参数。

### 返回值

Should return **`TRUE`** if the cached data was successfully stored (or
if there was no data to store), or **`FALSE`** if the data could not be
stored.

### 注释

> **Note**:
>
> If not implemented, **`FALSE`** is assumed as the return value.

### 参见

-   <span class="function">fflush</span>

streamWrapper::stream\_lock
===========================

Advisory file locking

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_lock</span> ( <span
class="methodparam"><span class="type">int</span> `$operation`</span> )

This method is called in response to <span
class="function">flock</span>, when <span
class="function">file\_put\_contents</span> (when `flags` contains
**`LOCK_EX`**), <span class="function">stream\_set\_blocking</span> and
when closing the stream (**`LOCK_UN`**).

### 参数

`operation`  
`operation` is one of the following:

-   <span class="simpara"> **`LOCK_SH`** to acquire a shared lock
    (reader). </span>
-   <span class="simpara"> **`LOCK_EX`** to acquire an exclusive lock
    (writer). </span>
-   <span class="simpara"> **`LOCK_UN`** to release a lock (shared or
    exclusive). </span>
-   <span class="simpara"> **`LOCK_NB`** if you don't want <span
    class="function">flock</span> to block while locking. (not supported
    on Windows) </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Emits **`E_WARNING`** if call to this method fails (i.e. not
implemented).

### 参见

-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">flock</span>

streamWrapper::stream\_metadata
===============================

Change stream metadata

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_metadata</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$option`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

This method is called to set metadata on the stream. It is called when
one of the following functions is called on a stream URL:

-   <span class="function">touch</span>
-   <span class="function">chmod</span>
-   <span class="function">chown</span>
-   <span class="function">chgrp</span>

Please note that some of these operations may not be available on your
system.

### 参数

`path`  
The file path or URL to set metadata. Note that in the case of a URL, it
must be a :// delimited URL. Other URL forms are not supported.

`option`  
One of:

-   **`STREAM_META_TOUCH`** (The method was called in response to <span
    class="function">touch</span>)
-   **`STREAM_META_OWNER_NAME`** (The method was called in response to
    <span class="function">chown</span> with string parameter)
-   **`STREAM_META_OWNER`** (The method was called in response to <span
    class="function">chown</span>)
-   **`STREAM_META_GROUP_NAME`** (The method was called in response to
    <span class="function">chgrp</span>)
-   **`STREAM_META_GROUP`** (The method was called in response to <span
    class="function">chgrp</span>)
-   **`STREAM_META_ACCESS`** (The method was called in response to <span
    class="function">chmod</span>)

`value`  
If `option` is

-   **`STREAM_META_TOUCH`**: <span class="type">Array</span> consisting
    of two arguments of the <span class="function">touch</span>
    function.
-   **`STREAM_META_OWNER_NAME`** or **`STREAM_META_GROUP_NAME`**: The
    name of the owner user/group as <span class="type">string</span>.
-   **`STREAM_META_OWNER`** or **`STREAM_META_GROUP`**: The value owner
    user/group argument as <span class="type">integer</span>.
-   **`STREAM_META_ACCESS`**: The argument of the <span
    class="function">chmod</span> as <span class="type">integer</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If `option` is
not implemented, **`FALSE`** should be returned.

### 参见

-   <span class="function">touch</span>
-   <span class="function">chmod</span>
-   <span class="function">chown</span>
-   <span class="function">chgrp</span>

streamWrapper::stream\_open
===========================

Opens file or URL

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_open</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$mode`</span> , <span class="methodparam"><span class="type">int</span>
`$options`</span> , <span class="methodparam"><span
class="type">string</span> `&$opened_path`</span> )

This method is called immediately after the wrapper is initialized (f.e.
by <span class="function">fopen</span> and <span
class="function">file\_get\_contents</span>).

### 参数

`path`  
Specifies the URL that was passed to the original function.

> **Note**:
>
> The URL can be broken apart with <span
> class="function">parse\_url</span>. Note that only URLs delimited by
> :// are supported. : and :/ while technically valid URLs, are not.

`mode`  
The mode used to open the file, as detailed for <span
class="function">fopen</span>.

> **Note**:
>
> Remember to check if the `mode` is valid for the `path` requested.

`options`  
Holds additional flags set by the streams API. It can hold one or more
of the following values OR'd together.

| Flag                       | Description                                                                                                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`STREAM_USE_PATH`**      | If `path` is relative, search for the resource using the include\_path.                                                                                                                                |
| **`STREAM_REPORT_ERRORS`** | If this flag is set, you are responsible for raising errors using <span class="function">trigger\_error</span> during opening of the stream. If this flag is not set, you should not raise any errors. |

`opened_path`  
If the `path` is opened successfully, and **`STREAM_USE_PATH`** is set
in `options`, `opened_path` should be set to the full path of the
file/resource that was actually opened.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 注释

> **Note**:
>
> 当合法的上下文传递给调用函数时，属性 `streamWrapper::$context`
> 会被改变。

### 参见

-   <span class="function">fopen</span>
-   <span class="function">parse\_url</span>

streamWrapper::stream\_read
===========================

Read from stream

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">streamWrapper::stream\_read</span> ( <span
class="methodparam"><span class="type">int</span> `$count`</span> )

This method is called in response to <span class="function">fread</span>
and <span class="function">fgets</span>.

> **Note**:
>
> Remember to update the read/write position of the stream (by the
> number of bytes that were successfully read).

### 参数

`count`  
How many bytes of data from the current position should be returned.

### 返回值

If there are less than `count` bytes available, return as many as are
available. If no more data is available, return either **`FALSE`** or an
empty string.

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

> **Note**:
>
> If the return value is longer then `count` an **`E_WARNING`** error
> will be emitted, and excess data will be lost.

### 注释

> **Note**:
>
> <span class="methodname">streamWrapper::stream\_eof</span> is called
> directly after calling <span
> class="methodname">streamWrapper::stream\_read</span> to check if EOF
> has been reached. If not implemented, EOF is assumed.

**Warning**

When reading the whole file (for example, with <span
class="function">file\_get\_contents</span>), PHP will call <span
class="methodname">streamWrapper::stream\_read</span> followed by <span
class="methodname">streamWrapper::stream\_eof</span> in a loop but as
long as <span class="methodname">streamWrapper::stream\_read</span>
returns a non-empty string, the return value of <span
class="methodname">streamWrapper::stream\_eof</span> is ignored.

### 参见

-   <span class="function">fread</span>
-   <span class="function">fgets</span>

streamWrapper::stream\_seek
===========================

Seeks to specific location in a stream

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_seek</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$whence` <span
class="initializer"> = SEEK\_SET</span></span> )

This method is called in response to <span
class="function">fseek</span>.

The read/write position of the stream should be updated according to the
`offset` and `whence`.

### 参数

`offset`  
The stream offset to seek to.

`whence`  
Possible values:

-   **`SEEK_SET`** - Set position equal to `offset` bytes.
-   **`SEEK_CUR`** - Set position to current location plus `offset`.
-   **`SEEK_END`** - Set position to end-of-file plus `offset`.

### 返回值

Return **`TRUE`** if the position was updated, **`FALSE`** otherwise.

### 注释

> **Note**:
>
> If not implemented, **`FALSE`** is assumed as the return value.

> **Note**:
>
> Upon success, <span
> class="methodname">streamWrapper::stream\_tell</span> is called
> directly after calling <span
> class="methodname">streamWrapper::stream\_seek</span>. If <span
> class="methodname">streamWrapper::stream\_tell</span> fails, the
> return value to the caller function will be set to **`FALSE`**

> **Note**:
>
> Not all seeks operations on the stream will result in this function
> being called. PHP streams have read buffering enabled by default (see
> also <span class="function">stream\_set\_read\_buffer</span>) and
> seeking may be done by merely moving the buffer pointer.

### 参见

-   <span class="function">fseek</span>

streamWrapper::stream\_set\_option
==================================

Change stream options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_set\_option</span> (
<span class="methodparam"><span class="type">int</span> `$option`</span>
, <span class="methodparam"><span class="type">int</span> `$arg1`</span>
, <span class="methodparam"><span class="type">int</span> `$arg2`</span>
)

This method is called to set options on the stream.

### 参数

`option`  
One of:

-   **`STREAM_OPTION_BLOCKING`** (The method was called in response to
    <span class="function">stream\_set\_blocking</span>)
-   **`STREAM_OPTION_READ_TIMEOUT`** (The method was called in response
    to <span class="function">stream\_set\_timeout</span>)
-   **`STREAM_OPTION_WRITE_BUFFER`** (The method was called in response
    to <span class="function">stream\_set\_write\_buffer</span>)

`arg1`  
If `option` is

-   **`STREAM_OPTION_BLOCKING`**: requested blocking mode (1 meaning
    block 0 not blocking).
-   **`STREAM_OPTION_READ_TIMEOUT`**: the timeout in seconds.
-   **`STREAM_OPTION_WRITE_BUFFER`**: buffer mode
    (**`STREAM_BUFFER_NONE`** or **`STREAM_BUFFER_FULL`**).

`arg2`  
If `option` is

-   **`STREAM_OPTION_BLOCKING`**: This option is not set.
-   **`STREAM_OPTION_READ_TIMEOUT`**: the timeout in microseconds.
-   **`STREAM_OPTION_WRITE_BUFFER`**: the requested buffer size.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If `option` is
not implemented, **`FALSE`** should be returned.

### 参见

-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">stream\_set\_timeout</span>
-   <span class="function">stream\_set\_write\_buffer</span>

streamWrapper::stream\_stat
===========================

Retrieve information about a file resource

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">streamWrapper::stream\_stat</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span
class="function">fstat</span>.

### 参数

此函数没有参数。

### 返回值

See <span class="function">stat</span>.

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 参见

-   <span class="function">stat</span>
-   <span class="methodname">streamwrapper::url\_stat</span>

streamWrapper::stream\_tell
===========================

Retrieve the current position of a stream

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">streamWrapper::stream\_tell</span> ( <span
class="methodparam">void</span> )

This method is called in response to <span class="function">fseek</span>
to determine the current position.

### 参数

此函数没有参数。

### 返回值

Should return the current position of the stream.

### 参见

-   <span class="methodname">streamWrapper::stream\_tell</span>

streamWrapper::stream\_truncate
===============================

Truncate stream

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::stream\_truncate</span> ( <span
class="methodparam"><span class="type">int</span> `$new_size`</span> )

Will respond to truncation, e.g., through <span
class="function">ftruncate</span>.

### 参数

`new_size`  
The new size.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ftruncate</span>

streamWrapper::stream\_write
============================

Write to stream

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">streamWrapper::stream\_write</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

This method is called in response to <span
class="function">fwrite</span>.

> **Note**:
>
> Remember to update the current position of the stream by number of
> bytes that were successfully written.

### 参数

`data`  
Should be stored into the underlying stream.

> **Note**:
>
> If there is not enough room in the underlying stream, store as much as
> possible.

### 返回值

Should return the number of bytes that were successfully stored, or 0 if
none could be stored.

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

> **Note**:
>
> If the return value is greater the length of `data`, **`E_WARNING`**
> will be emitted and the return value will truncated to its length.

### 参见

-   <span class="function">fwrite</span>

streamWrapper::unlink
=====================

Delete a file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">streamWrapper::unlink</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

This method is called in response to <span
class="function">unlink</span>.

> **Note**:
>
> In order for the appropriate error message to be returned this method
> should *not* be defined if the wrapper does not support removing
> files.

### 参数

`path`  
The file URL which should be deleted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 注释

> **Note**:
>
> 当合法的上下文传递给调用函数时，属性 `streamWrapper::$context`
> 会被改变。

### 参见

-   <span class="function">unlink</span>
-   <span class="methodname">streamWrapper::rmdir</span>

streamWrapper::url\_stat
========================

Retrieve information about a file

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">streamWrapper::url\_stat</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
)

This method is called in response to all <span
class="function">stat</span> related functions, such as:

-   <span class="function">chmod</span> (only when
    <a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>
    is enabled)
-   <span class="function">copy</span>
-   <span class="function">fileperms</span>
-   <span class="function">fileinode</span>
-   <span class="function">filesize</span>
-   <span class="function">fileowner</span>
-   <span class="function">filegroup</span>
-   <span class="function">fileatime</span>
-   <span class="function">filemtime</span>
-   <span class="function">filectime</span>
-   <span class="function">filetype</span>
-   <span class="function">is\_writable</span>
-   <span class="function">is\_readable</span>
-   <span class="function">is\_executable</span>
-   <span class="function">is\_file</span>
-   <span class="function">is\_dir</span>
-   <span class="function">is\_link</span>
-   <span class="function">file\_exists</span>
-   <span class="function">lstat</span>
-   <span class="function">stat</span>
-   <span class="methodname">SplFileInfo::getPerms</span>
-   <span class="methodname">SplFileInfo::getInode</span>
-   <span class="methodname">SplFileInfo::getSize</span>
-   <span class="methodname">SplFileInfo::getOwner</span>
-   <span class="methodname">SplFileInfo::getGroup</span>
-   <span class="methodname">SplFileInfo::getATime</span>
-   <span class="methodname">SplFileInfo::getMTime</span>
-   <span class="methodname">SplFileInfo::getCTime</span>
-   <span class="methodname">SplFileInfo::getType</span>
-   <span class="methodname">SplFileInfo::isWritable</span>
-   <span class="methodname">SplFileInfo::isReadable</span>
-   <span class="methodname">SplFileInfo::isExecutable</span>
-   <span class="methodname">SplFileInfo::isFile</span>
-   <span class="methodname">SplFileInfo::isDir</span>
-   <span class="methodname">SplFileInfo::isLink</span>
-   <span
    class="methodname">RecursiveDirectoryIterator::hasChildren</span>

### 参数

`path`  
The file path or URL to stat. Note that in the case of a URL, it must be
a :// delimited URL. Other URL forms are not supported.

`flags`  
Holds additional flags set by the streams API. It can hold one or more
of the following values OR'd together.

| Flag                     | Description                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STREAM\_URL\_STAT\_LINK  | For resources with the ability to link to other resource (such as an HTTP Location: forward, or a filesystem symlink). This flag specified that only information about the link itself should be returned, not the resource pointed to by the link. This flag is set in response to calls to <span class="function">lstat</span>, <span class="function">is\_link</span>, or <span class="function">filetype</span>. |
| STREAM\_URL\_STAT\_QUIET | If this flag is set, your wrapper should not raise any errors. If this flag is not set, you are responsible for reporting errors using the <span class="function">trigger\_error</span> function during stating of the path.                                                                                                                                                                                         |

### 返回值

Should return as many elements as <span class="function">stat</span>
does. Unknown or unavailable values should be set to a rational value
(usually **`0`**). Pay special attention to *mode* as documented under
<span class="function">stat</span>.

### 错误／异常

调用此方法失败将给出 **`E_WARNING`**（未实现）。

### 注释

> **Note**:
>
> 当合法的上下文传递给调用函数时，属性 `streamWrapper::$context`
> 会被改变。

### 参见

-   <span class="function">stat</span>
-   <span class="methodname">streamwrapper::stream\_stat</span>
