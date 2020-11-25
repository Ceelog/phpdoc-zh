deflate\_add
============

Incrementally deflate data

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">deflate\_add</span> ( <span class="methodparam"><span
class="type">DeflateContext</span> `$context`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$flush_mode`<span class="initializer"> =
**`ZLIB_SYNC_FLUSH`**</span></span> \] )

Incrementally deflates data in the specified context.

### 参数

`context`  
A context created with <span class="function">deflate\_init</span>.

`data`  
A chunk of data to compress.

`flush_mode`  
One of **`ZLIB_BLOCK`**, **`ZLIB_NO_FLUSH`**, **`ZLIB_PARTIAL_FLUSH`**,
**`ZLIB_SYNC_FLUSH`** (default), **`ZLIB_FULL_FLUSH`**,
**`ZLIB_FINISH`**. Normally you will want to set **`ZLIB_NO_FLUSH`** to
maximize compression, and **`ZLIB_FINISH`** to terminate with the last
chunk of data. See the
<a href="http://www.zlib.net/manual.html" class="link external">» zlib manual</a>
for a detailed description of these constants.

### 返回值

Returns a chunk of compressed data, 或者在失败时返回 **`FALSE`**.

### 错误／异常

If invalid arguments are given, an error of level **`E_WARNING`** is
generated.

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `context` expects a <span class="classname">DeflateContext</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">deflate\_init</span>

deflate\_init
=============

Initialize an incremental deflate context

### 说明

<span class="type"><span class="type">DeflateContext</span><span
class="type">false</span></span> <span
class="methodname">deflate\_init</span> ( <span
class="methodparam"><span class="type">int</span> `$encoding`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = \[\]</span></span> \] )

Initializes an incremental deflate context using the specified
`encoding`.

Note that the *window* option here only sets the window size of the
algorithm, differently from the zlib filters where the same parameter
also sets the encoding to use; the encoding must be set with the
`encoding` parameter.

Limitation: there is currently no way to set the header information on a
GZIP compressed stream, which are set as follows: GZIP signature
(*\\x1f\\x8B*); compression method (*\\x08* == DEFLATE); 6 zero bytes;
the operating system set to the current system (*\\x00* = Windows,
*\\x03* = Unix, etc.)

### 参数

`encoding`  
One of the **`ZLIB_ENCODING_*`** constants.

`options`  
An associative array which may contain the following elements:

`level`  
The compression level in range -1..9; defaults to -1.

`memory`  
The compression memory level in range 1..9; defaults to 8.

`window`  
The zlib window size (logarithmic) in range *8*..*15*; defaults to *15*.
zlib changes a window size of *8* to *9*, and as of zlib 1.2.8 fails
with a warning, if a window size of *8* is requested for
**`ZLIB_ENCODING_RAW`** or **`ZLIB_ENCODING_GZIP`**.

`strategy`  
One of **`ZLIB_FILTERED`**, **`ZLIB_HUFFMAN_ONLY`**, **`ZLIB_RLE`**,
**`ZLIB_FIXED`** or **`ZLIB_DEFAULT_STRATEGY`** (the default).

`dictionary`  
A <span class="type">string</span> or an <span class="type">array</span>
of <span class="type">strings</span> of the preset dictionary (default:
no preset dictionary).

### 返回值

Returns a deflate context resource (*zlib.deflate*) on success,
或者在失败时返回 **`FALSE`**.

### 错误／异常

If an invalid option is passed to `options` or the context couldn't be
created, an error of level **`E_WARNING`** is generated.

### 更新日志

| 版本  | 说明                                                                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | On success, this function returns a <span class="classname">DeflateContext</span> instance now; previously, a <span class="type">resource</span> was returned. |

### 参见

-   <span class="function">deflate\_add</span>
-   <span class="function">inflate\_init</span>

gzclose
=======

Close an open gz-file pointer

### 说明

<span class="type">bool</span> <span class="methodname">gzclose</span> (
<span class="methodparam"><span class="type">resource</span>
`$stream`</span> )

Closes the given gz-file pointer.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">gzclose</span> example**

``` php
<?php
$gz = gzopen('somefile.gz','w9');
gzputs ($gz, 'I was added to somefile.gz');
gzclose($gz);
?>
```

### 参见

-   <span class="function">gzopen</span>

gzcompress
==========

Compress a string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gzcompress</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$level`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$encoding`<span
class="initializer"> = **`ZLIB_ENCODING_DEFLATE`**</span></span> \]\] )

This function compresses the given string using the *ZLIB* data format.

For details on the ZLIB compression algorithm see the document
"<a href="http://www.faqs.org/rfcs/rfc1950" class="link external">» ZLIB Compressed Data Format Specification version 3.3</a>"
(RFC 1950).

> **Note**:
>
> This is *not* the same as gzip compression, which includes some header
> data. See <span class="function">gzencode</span> for gzip compression.

### 参数

`data`  
The data to compress.

`level`  
The level of compression. Can be given as 0 for no compression up to 9
for maximum compression.

If -1 is used, the default compression of the zlib library is used which
is 6.

`encoding`  
One of **`ZLIB_ENCODING_*`** constants.

### 返回值

The compressed string or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 <span class="function">gzcompress</span> example**

``` php
<?php
$compressed = gzcompress('Compress me', 9);
echo $compressed;
?>
```

### 参见

-   <span class="function">gzdeflate</span>
-   <span class="function">gzinflate</span>
-   <span class="function">gzuncompress</span>
-   <span class="function">gzencode</span>

gzdecode
========

Decodes a gzip compressed string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gzdecode</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$max_length`<span
class="initializer"> = 0</span></span> \] )

This function returns a decoded version of the input `data`.

### 参数

`data`  
The data to decode, encoded by <span class="function">gzencode</span>.

`max_length`  
The maximum length of data to decode.

### 返回值

The decoded string, or **`FALSE`** if an error occurred.

### 参见

-   <span class="function">gzencode</span>

gzdeflate
=========

Deflate a string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gzdeflate</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$level`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$encoding`<span
class="initializer"> = **`ZLIB_ENCODING_RAW`**</span></span> \]\] )

This function compresses the given string using the *DEFLATE* data
format.

For details on the DEFLATE compression algorithm see the document
"<a href="http://www.faqs.org/rfcs/rfc1951" class="link external">» DEFLATE Compressed Data Format Specification version 1.3</a>"
(RFC 1951).

### 参数

`data`  
The data to deflate.

`level`  
The level of compression. Can be given as 0 for no compression up to 9
for maximum compression. If not given, the default compression level
will be the default compression level of the zlib library.

`encoding`  
One of **`ZLIB_ENCODING_*`** constants.

### 返回值

The deflated string or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 <span class="function">gzdeflate</span> example**

``` php
<?php
$compressed = gzdeflate('Compress me', 9);
echo $compressed;
?>
```

### 参见

-   <span class="function">gzinflate</span>
-   <span class="function">gzcompress</span>
-   <span class="function">gzuncompress</span>
-   <span class="function">gzencode</span>

gzencode
========

Create a gzip compressed string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gzencode</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$level`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$encoding`<span
class="initializer"> = **`ZLIB_ENCODING_GZIP`**</span></span> \]\] )

This function returns a compressed version of the input `data`
compatible with the output of the **gzip** program.

For more information on the GZIP file format, see the document:
<a href="http://www.faqs.org/rfcs/rfc1952" class="link external">» GZIP file format specification version 4.3</a>
(RFC 1952).

### 参数

`data`  
The data to encode.

`level`  
The level of compression. Can be given as 0 for no compression up to 9
for maximum compression. If not given, the default compression level
will be the default compression level of the zlib library.

`encoding`  
The encoding mode. Can be **`FORCE_GZIP`** (the default) or
**`FORCE_DEFLATE`**.

Prior to PHP 5.4.0, using **`FORCE_DEFLATE`** results in a standard zlib
deflated string (inclusive zlib headers) after a gzip file header but
without the trailing crc32 checksum.

In PHP 5.4.0 and later, **`FORCE_DEFLATE`** generates RFC 1950 compliant
output, consisting of a zlib header, the deflated data, and an Adler
checksum.

### 返回值

The encoded string, or **`FALSE`** if an error occurred.

### 范例

The resulting data contains the appropriate headers and data structure
to make a standard .gz file, e.g.:

**示例 \#1 Creating a gzip file**

``` php
<?php
$data = implode("", file("bigfile.txt"));
$gzdata = gzencode($data, 9);
$fp = fopen("bigfile.txt.gz", "w");
fwrite($fp, $gzdata);
fclose($fp);
?>
```

### 参见

-   <span class="function">gzdecode</span>
-   <span class="function">gzdeflate</span>
-   <span class="function">gzinflate</span>
-   <span class="function">gzuncompress</span>
-   <span class="function">gzcompress</span>
-   <a href="http://www.faqs.org/rfcs/rfc1950" class="link external">»  ZLIB Compressed Data Format Specification (RFC 1950)</a>

gzeof
=====

Test for EOF on a gz-file pointer

### 说明

<span class="type">bool</span> <span class="methodname">gzeof</span> (
<span class="methodparam"><span class="type">resource</span>
`$stream`</span> )

Tests the given GZ file pointer for EOF.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

### 返回值

Returns **`TRUE`** if the gz-file pointer is at EOF or an error occurs;
otherwise returns **`FALSE`**.

### 范例

**示例 \#1 <span class="function">gzeof</span> example**

``` php
<?php
$gz = gzopen('somefile.gz', 'r');
while (!gzeof($gz)) {
  echo gzgetc($gz);
}
gzclose($gz);
?>
```

gzfile
======

Read entire gz-file into an array

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span class="methodname">gzfile</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">int</span> `$use_include_path`<span class="initializer"> =
0</span></span> \] )

This function is identical to <span class="function">readgzfile</span>,
except that it returns the file in an array.

### 参数

`filename`  
The file name.

`use_include_path`  
You can set this optional parameter to *1*, if you want to search for
the file in the
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
too.

### 返回值

An array containing the file, one line per cell, empty lines included,
and with newlines still attached, 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">gzfile</span> example**

``` php
<?php
$lines = gzfile('somefile.gz');
foreach ($lines as $line) {
    echo $line;
}
?>
```

### 参见

-   <span class="function">readgzfile</span>
-   <span class="function">gzopen</span>

gzgetc
======

Get character from gz-file pointer

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span class="methodname">gzgetc</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> )

Returns a string containing a single (uncompressed) character read from
the given gz-file pointer.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

### 返回值

The uncompressed character or **`FALSE`** on EOF (unlike <span
class="function">gzeof</span>).

### 范例

**示例 \#1 <span class="function">gzgetc</span> example**

``` php
<?php
$gz = gzopen('somefile.gz', 'r');
while (!gzeof($gz)) {
  echo gzgetc($gz);
}
gzclose($gz);
?>
```

### 参见

-   <span class="function">gzopen</span>
-   <span class="function">gzgets</span>

gzgets
======

Get line from file pointer

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span class="methodname">gzgets</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`<span class="initializer"> =
1024</span></span> \] )

Gets a (uncompressed) string of up to length - 1 bytes read from the
given file pointer. Reading ends when length - 1 bytes have been read,
on a newline, or on EOF (whichever comes first).

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

`length`  
The length of data to get.

### 返回值

The uncompressed string, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">gzgets</span> example**

``` php
<?php
$handle = gzopen('somefile.gz', 'r');
while (!gzeof($handle)) {
   $buffer = gzgets($handle, 4096);
   echo $buffer;
}
gzclose($handle);
?>
```

### 参见

-   <span class="function">gzopen</span>
-   <span class="function">gzgetc</span>
-   <span class="function">gzwrite</span>

gzgetss
=======

Get line from gz-file pointer and strip HTML tags

**Warning**

本函数已自 PHP 7.3.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span class="methodname">gzgetss</span>
( <span class="methodparam"><span class="type">resource</span>
`$zp`</span> , <span class="methodparam"><span class="type">int</span>
`$length`</span> \[, <span class="methodparam"><span
class="type">string</span> `$allowable_tags`</span> \] )

Identical to <span class="function">gzgets</span>, except that <span
class="function">gzgetss</span> attempts to strip any HTML and PHP tags
from the text it reads.

### 参数

`zp`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

`length`  
The length of data to get.

`allowable_tags`  
You can use this optional parameter to specify tags which should not be
stripped.

### 返回值

The uncompressed and stripped string, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">gzgetss</span> example**

``` php
<?php
$handle = gzopen('somefile.gz', 'r');
while (!gzeof($handle)) {
   $buffer = gzgetss($handle, 4096);
   echo $buffer;
}
gzclose($handle);
?>
```

### 参见

-   <span class="function">gzopen</span>
-   <span class="function">gzgets</span>
-   <span class="function">strip\_tags</span>

gzinflate
=========

Inflate a deflated string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gzinflate</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$max_length`<span
class="initializer"> = 0</span></span> \] )

This function inflates a deflated string.

### 参数

`data`  
The data compressed by <span class="function">gzdeflate</span>.

`max_length`  
The maximum length of data to decode.

### 返回值

The original uncompressed data or **`FALSE`** on error.

The function will return an error if the uncompressed data is more than
32768 times the length of the compressed input `data` or more than the
optional parameter `max_length`.

### 范例

**示例 \#1 <span class="function">gzinflate</span> example**

``` php
<?php
$compressed   = gzdeflate('Compress me', 9);
$uncompressed = gzinflate($compressed);
echo $uncompressed;
?>
```

### 参见

-   <span class="function">gzdeflate</span>
-   <span class="function">gzcompress</span>
-   <span class="function">gzuncompress</span>
-   <span class="function">gzencode</span>

gzopen
======

Open gz-file

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span class="methodname">gzopen</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">int</span>
`$use_include_path`<span class="initializer"> = 0</span></span> \] )

Opens a gzip (.gz) file for reading or writing.

<span class="function">gzopen</span> can be used to read a file which is
not in gzip format; in this case <span class="function">gzread</span>
will directly read from the file without decompression.

### 参数

`filename`  
The file name.

`mode`  
As in <span class="function">fopen</span> (*rb* or *wb*) but can also
include a compression level (*wb9*) or a strategy: *f* for filtered data
as in *wb6f*, *h* for *Huffman only compression* as in *wb1h*. (See the
description of *deflateInit2* in `zlib.h` for more information about the
strategy parameter.)

`use_include_path`  
You can set this optional parameter to *1*, if you want to search for
the file in the
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
too.

### 返回值

Returns a file pointer to the file opened, after that, everything you
read from this file descriptor will be transparently decompressed and
what you write gets compressed.

If the open fails, the function returns **`FALSE`**.

### 范例

**示例 \#1 <span class="function">gzopen</span> Example**

``` php
<?php
$fp = gzopen("/tmp/file.gz", "r");
?>
```

### 参见

-   <span class="function">gzclose</span>

gzpassthru
==========

Output all remaining data on a gz-file pointer

### 说明

<span class="type">int</span> <span class="methodname">gzpassthru</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> )

Reads to EOF on the given gz-file pointer from the current position and
writes the (uncompressed) results to standard output.

> **Note**:
>
> You may need to call <span class="function">gzrewind</span> to reset
> the file pointer to the beginning of the file if you have already
> written data to it.

**小贴士**

If you just want to dump the contents of a file to the output buffer,
without first modifying it or seeking to a particular offset, you may
want to use the <span class="function">readgzfile</span> function, which
saves you the <span class="function">gzopen</span> call.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

### 返回值

The number of uncompressed characters read from `gz` and passed through
to the input, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">gzpassthru</span> example**

``` php
<?php
$fp = gzopen('file.gz', 'r');
gzpassthru($fp);
gzclose($fp);
?>
```

gzputs
======

别名 <span class="function">gzwrite</span>

### 说明

此函数是该函数的别名： <span class="function">gzwrite</span>.

gzread
======

Binary-safe gz-file read

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span class="methodname">gzread</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> , <span class="methodparam"><span
class="type">int</span> `$length`</span> )

<span class="function">gzread</span> reads up to `length` bytes from the
given gz-file pointer. Reading stops when `length` (uncompressed) bytes
have been read or EOF is reached, whichever comes first.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

`length`  
The number of bytes to read.

### 返回值

The data that have been read, 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                            |
|-------|---------------------------------------------------------------------------------|
| 7.4.0 | This functions returns **`FALSE`** on failure now; previously *0* was returned. |

### 范例

**示例 \#1 <span class="function">gzread</span> example**

``` php
<?php
// get contents of a gz-file into a string
$filename = "/usr/local/something.txt.gz";
$zd = gzopen($filename, "r");
$contents = gzread($zd, 10000);
gzclose($zd);
?>
```

### 参见

-   <span class="function">gzwrite</span>
-   <span class="function">gzopen</span>
-   <span class="function">gzgets</span>
-   <span class="function">gzgetss</span>
-   <span class="function">gzfile</span>
-   <span class="function">gzpassthru</span>

gzrewind
========

Rewind the position of a gz-file pointer

### 说明

<span class="type">bool</span> <span class="methodname">gzrewind</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> )

Sets the file position indicator of the given gz-file pointer to the
beginning of the file stream.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gzseek</span>
-   <span class="function">gztell</span>

gzseek
======

Seek on a gz-file pointer

### 说明

<span class="type">int</span> <span class="methodname">gzseek</span> (
<span class="methodparam"><span class="type">resource</span>
`$stream`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$whence`<span
class="initializer"> = **`SEEK_SET`**</span></span> \] )

Sets the file position indicator for the given file pointer to the given
offset byte into the file stream. Equivalent to calling (in C)
*gzseek(zp, offset, SEEK\_SET)*.

If the file is opened for reading, this function is emulated but can be
extremely slow. If the file is opened for writing, only forward seeks
are supported; <span class="function">gzseek</span> then compresses a
sequence of zeroes up to the new starting position.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

`offset`  
The seeked offset.

`whence`  
`whence` values are:

-   **`SEEK_SET`** - Set position equal to `offset` bytes.
-   **`SEEK_CUR`** - Set position to current location plus `offset`.

If `whence` is not specified, it is assumed to be **`SEEK_SET`**.

### 返回值

Upon success, returns 0; otherwise, returns -1. Note that seeking past
EOF is not considered an error.

### 范例

**示例 \#1 <span class="function">gzseek</span> example**

``` php
<?php
$gz = gzopen('somefile.gz', 'r');
gzseek($gz,2);
echo gzgetc($gz);
gzclose($gz);
?>
```

### 参见

-   <span class="function">gztell</span>
-   <span class="function">gzrewind</span>

gztell
======

Tell gz-file pointer read/write position

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span class="methodname">gztell</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> )

Gets the position of the given file pointer; i.e., its offset into the
uncompressed file stream.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

### 返回值

The position of the file pointer or **`FALSE`** if an error occurs.

### 参见

-   <span class="function">gzopen</span>
-   <span class="function">gzseek</span>
-   <span class="function">gzrewind</span>

gzuncompress
============

Uncompress a compressed string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gzuncompress</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$max_length`<span
class="initializer"> = 0</span></span> \] )

This function uncompress a compressed string.

### 参数

`data`  
The data compressed by <span class="function">gzcompress</span>.

`max_length`  
The maximum length of data to decode.

### 返回值

The original uncompressed data or **`FALSE`** on error.

The function will return an error if the uncompressed data is more than
32768 times the length of the compressed input `data` or more than the
optional parameter `max_length`.

### 范例

**示例 \#1 <span class="function">gzuncompress</span> example**

``` php
<?php
$compressed   = gzcompress('Compress me', 9);
$uncompressed = gzuncompress($compressed);
echo $uncompressed;
?>
```

### 参见

-   <span class="function">gzcompress</span>
-   <span class="function">gzinflate</span>
-   <span class="function">gzdeflate</span>
-   <span class="function">gzencode</span>

gzwrite
=======

Binary-safe gz-file write

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span class="methodname">gzwrite</span>
( <span class="methodparam"><span class="type">resource</span>
`$stream`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type"><span
class="type">int</span><span class="type">null</span></span>
`$length`<span class="initializer"> = **`NULL`**</span></span> \] )

<span class="function">gzwrite</span> writes the contents of `data` to
the given gz-file.

### 参数

`stream`  
The gz-file pointer. It must be valid, and must point to a file
successfully opened by <span class="function">gzopen</span>.

`data`  
The string to write.

`length`  
The number of uncompressed bytes to write. If supplied, writing will
stop after `length` (uncompressed) bytes have been written or the end of
`data` is reached, whichever comes first.

> **Note**:
>
> Note that if the `length` argument is given, then the
> <a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
> configuration option will be ignored and no slashes will be stripped
> from `data`.

### 返回值

Returns the number of (uncompressed) bytes written to the given gz-file
stream, 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                            |
|-------|---------------------------------------------------------------------------------|
| 8.0.0 | `length` is nullable now; previously, the default was *0*.                      |
| 7.4.0 | This functions returns **`FALSE`** on failure now; previously *0* was returned. |

### 范例

**示例 \#1 <span class="function">gzwrite</span> example**

``` php
<?php
$string = 'Some information to compress';
$gz = gzopen('somefile.gz','w9');
gzwrite($gz, $string);
gzclose($gz);
?>
```

### 参见

-   <span class="function">gzread</span>
-   <span class="function">gzopen</span>

inflate\_add
============

Incrementally inflate encoded data

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">inflate\_add</span> ( <span class="methodparam"><span
class="type">InflateContext</span> `$context`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$flush_mode`<span class="initializer"> =
**`ZLIB_SYNC_FLUSH`**</span></span> \] )

Incrementally inflates encoded data in the specified `context`.

Limitation: header information from GZIP compressed data are not made
available.

### 参数

`context`  
A context created with <span class="function">inflate\_init</span>.

`data`  
A chunk of compressed data.

`flush_mode`  
One of **`ZLIB_BLOCK`**, **`ZLIB_NO_FLUSH`**, **`ZLIB_PARTIAL_FLUSH`**,
**`ZLIB_SYNC_FLUSH`** (default), **`ZLIB_FULL_FLUSH`**,
**`ZLIB_FINISH`**. Normally you will want to set **`ZLIB_NO_FLUSH`** to
maximize compression, and **`ZLIB_FINISH`** to terminate with the last
chunk of data. See the
<a href="http://www.zlib.net/manual.html" class="link external">» zlib manual</a>
for a detailed description of these constants.

### 返回值

Returns a chunk of uncompressed data, 或者在失败时返回 **`FALSE`**.

### 错误／异常

If invalid parameters are given, inflating the data requires a preset
dictionary, but none is specified, the compressed stream is corrupt or
has an invalid checksum, an error of level **`E_WARNING`** is generated.

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `context` expects an <span class="classname">InflateContext</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">inflate\_init</span>

inflate\_get\_read\_len
=======================

Get number of bytes read so far

### 说明

<span class="type">int</span> <span
class="methodname">inflate\_get\_read\_len</span> ( <span
class="methodparam"><span class="type">InflateContext</span>
`$context`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  

### 返回值

Returns number of bytes read so far 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `context` expects an <span class="classname">InflateContext</span> instance now; previously, a <span class="type">resource</span> was expected. |

inflate\_get\_status
====================

Get decompression status

### 说明

<span class="type">int</span> <span
class="methodname">inflate\_get\_status</span> ( <span
class="methodparam"><span class="type">InflateContext</span>
`$context`</span> )

Usually returns either **`ZLIB_OK`** or **`ZLIB_STREAM_END`**.

### 参数

`context`  

### 返回值

Returns decompression status 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `context` expects an <span class="classname">InflateContext</span> instance now; previously, a <span class="type">resource</span> was expected. |

inflate\_init
=============

Initialize an incremental inflate context

### 说明

<span class="type"><span class="type">InflateContext</span><span
class="type">false</span></span> <span
class="methodname">inflate\_init</span> ( <span
class="methodparam"><span class="type">int</span> `$encoding`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = \[\]</span></span> \] )

Initialize an incremental inflate context with the specified `encoding`.

### 参数

`encoding`  
One of the **`ZLIB_ENCODING_*`** constants.

`options`  
An associative array which may contain the following elements:

`level`  
The compression level in range -1..9; defaults to -1.

`memory`  
The compression memory level in range 1..9; defaults to 8.

`window`  
The zlib window size (logarithmic) in range 8..15; defaults to 15.

`strategy`  
One of **`ZLIB_FILTERED`**, **`ZLIB_HUFFMAN_ONLY`**, **`ZLIB_RLE`**,
**`ZLIB_FIXED`** or **`ZLIB_DEFAULT_STRATEGY`** (the default).

`dictionary`  
A <span class="type">string</span> or an <span class="type">array</span>
of <span class="type">strings</span> of the preset dictionary (default:
no preset dictionary).

### 返回值

Returns an inflate context resource (*zlib.inflate*) on success,
或者在失败时返回 **`FALSE`**.

### 错误／异常

If an invalid encoding or option is passed to `options`, or the context
couldn't be created, an error of level **`E_WARNING`** is generated.

### 更新日志

| 版本  | 说明                                                                                                                                                            |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | On success, this function returns an <span class="classname">InflateContext</span> instance now; previously, a <span class="type">resource</span> was returned. |

### 参见

-   <span class="function">inflate\_add</span>
-   <span class="function">deflate\_init</span>

readgzfile
==========

Output a gz-file

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">readgzfile</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span>
`$use_include_path`<span class="initializer"> = 0</span></span> \] )

Reads a file, decompresses it and writes it to standard output.

<span class="function">readgzfile</span> can be used to read a file
which is not in gzip format; in this case <span
class="function">readgzfile</span> will directly read from the file
without decompression.

### 参数

`filename`  
The file name. This file will be opened from the filesystem and its
contents written to standard output.

`use_include_path`  
You can set this optional parameter to *1*, if you want to search for
the file in the
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
too.

### 返回值

Returns the number of (uncompressed) bytes read from the file on
success, 或者在失败时返回 **`FALSE`**

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 参见

-   <span class="function">gzpassthru</span>
-   <span class="function">gzfile</span>
-   <span class="function">gzopen</span>

zlib\_decode
============

Uncompress any raw/gzip/zlib encoded data

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">zlib\_decode</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$max_length`<span
class="initializer"> = 0</span></span> \] )

Uncompress any raw/gzip/zlib encoded data.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`data`  

`max_length`  

### 返回值

Returns the uncompressed data, 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">zlib\_encode</span>

zlib\_encode
============

Compress data with the specified encoding

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">zlib\_encode</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> , <span
class="methodparam"><span class="type">int</span> `$encoding`</span> \[,
<span class="methodparam"><span class="type">int</span> `$level`<span
class="initializer"> = -1</span></span> \] )

Compress data with the specified encoding.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`data`  
The data to compress.

`encoding`  
The compression algorithm. Either **`ZLIB_ENCODING_RAW`**,
**`ZLIB_ENCODING_DEFLATE`** or **`ZLIB_ENCODING_GZIP`**.

`level`  

### 返回值

### 范例

**示例 \#1 <span class="function">zlib\_encode</span> example**

``` php
<?php
$str = 'hello world';
$enc = zlib_encode($str, ZLIB_ENCODING_DEFLATE);
echo bin2hex($enc);
?>
```

以上例程会输出：

    789ccb48cdc9c95728cf2fca4901001a0b045d

### 参见

-   <span class="function">zlib\_decode</span>

zlib\_get\_coding\_type
=======================

Returns the coding type used for output compression

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">zlib\_get\_coding\_type</span> ( <span
class="methodparam">void</span> )

Returns the coding type used for output compression.

### 返回值

Possible return values are *gzip*, *deflate*, or **`FALSE`**.

### 参见

-   The
    <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>
    directive

**目录**

-   [deflate\_add](/ref/zlib.html#deflate_add) — Incrementally deflate
    data
-   [deflate\_init](/ref/zlib.html#deflate_init) — Initialize an
    incremental deflate context
-   [gzclose](/ref/zlib.html#gzclose) — Close an open gz-file pointer
-   [gzcompress](/ref/zlib.html#gzcompress) — Compress a string
-   [gzdecode](/ref/zlib.html#gzdecode) — Decodes a gzip compressed
    string
-   [gzdeflate](/ref/zlib.html#gzdeflate) — Deflate a string
-   [gzencode](/ref/zlib.html#gzencode) — Create a gzip compressed
    string
-   [gzeof](/ref/zlib.html#gzeof) — Test for EOF on a gz-file pointer
-   [gzfile](/ref/zlib.html#gzfile) — Read entire gz-file into an array
-   [gzgetc](/ref/zlib.html#gzgetc) — Get character from gz-file pointer
-   [gzgets](/ref/zlib.html#gzgets) — Get line from file pointer
-   [gzgetss](/ref/zlib.html#gzgetss) — Get line from gz-file pointer
    and strip HTML tags
-   [gzinflate](/ref/zlib.html#gzinflate) — Inflate a deflated string
-   [gzopen](/ref/zlib.html#gzopen) — Open gz-file
-   [gzpassthru](/ref/zlib.html#gzpassthru) — Output all remaining data
    on a gz-file pointer
-   [gzputs](/ref/zlib.html#gzputs) — 别名 gzwrite
-   [gzread](/ref/zlib.html#gzread) — Binary-safe gz-file read
-   [gzrewind](/ref/zlib.html#gzrewind) — Rewind the position of a
    gz-file pointer
-   [gzseek](/ref/zlib.html#gzseek) — Seek on a gz-file pointer
-   [gztell](/ref/zlib.html#gztell) — Tell gz-file pointer read/write
    position
-   [gzuncompress](/ref/zlib.html#gzuncompress) — Uncompress a
    compressed string
-   [gzwrite](/ref/zlib.html#gzwrite) — Binary-safe gz-file write
-   [inflate\_add](/ref/zlib.html#inflate_add) — Incrementally inflate
    encoded data
-   [inflate\_get\_read\_len](/ref/zlib.html#inflate_get_read_len) — Get
    number of bytes read so far
-   [inflate\_get\_status](/ref/zlib.html#inflate_get_status) — Get
    decompression status
-   [inflate\_init](/ref/zlib.html#inflate_init) — Initialize an
    incremental inflate context
-   [readgzfile](/ref/zlib.html#readgzfile) — Output a gz-file
-   [zlib\_decode](/ref/zlib.html#zlib_decode) — Uncompress any
    raw/gzip/zlib encoded data
-   [zlib\_encode](/ref/zlib.html#zlib_encode) — Compress data with the
    specified encoding
-   [zlib\_get\_coding\_type](/ref/zlib.html#zlib_get_coding_type) —
    Returns the coding type used for output compression
