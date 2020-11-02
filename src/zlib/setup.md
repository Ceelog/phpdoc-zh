安装／配置
==========

**目录**

-   [需求](/zlib/setup.html#需求)
-   [安装](/zlib/setup.html#安装)
-   [运行时配置](/zlib/setup.html#运行时配置)
-   [资源类型](/zlib/setup.html#资源类型)

需求
----

This module uses the functions of
<a href="http://www.zlib.net/" class="link external">» zlib</a> by
Jean-loup Gailly and Mark Adler. You have to use a zlib version \>=
1.0.9 with this module. As of PHP 5.4.0 you have to use zlib \>=
1.2.0.4.

安装
----

Zlib support in PHP is not enabled by default. You will need to
configure PHP **--with-zlib\[=DIR\]**

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

The zlib extension offers the option to transparently compress your
pages on-the-fly, if the requesting browser supports this. Therefore
there are three options in the
<a href="/configuration/file.html" class="link">configuration file</a>
`php.ini`.

| 名字                                                                       | 默认 | 可修改范围    | 更新日志 |
|----------------------------------------------------------------------------|------|---------------|----------|
| <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>       | "0"  | PHP\_INI\_ALL |          |
| <a href="/zlib/setup.html#" class="link">zlib.output_compression_level</a> | "-1" | PHP\_INI\_ALL |          |
| <a href="/zlib/setup.html#" class="link">zlib.output_handler</a>           | ""   | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`zlib.output_compression` <span class="type">bool</span>/<span class="type">int</span>  
Whether to transparently compress pages. If this option is set to "On"
in `php.ini` or the Apache configuration, pages are compressed if the
browser sends an "Accept-Encoding: gzip" or "deflate" header.
"Content-Encoding: gzip" (respectively "deflate") and "Vary:
Accept-Encoding" headers are added to the output. In runtime, it can be
set only before sending any output.

This option also accepts integer values instead of boolean "On"/"Off",
using this you can set the output buffer size (default is 4KB).

> **Note**:
>
> <a href="/outcontrol/setup.html#" class="link">output_handler</a> must
> be empty if this is set 'On' ! Instead you must use
> *zlib.output\_handler*.

`zlib.output_compression_level` <span class="type">int</span>  
Compression level used for transparent output compression. Specify a
value between 0 (no compression) to 9 (most compression). The default
value, -1, lets the server decide which level to use.

`zlib.output_handler` <span class="type">string</span>  
You cannot specify additional output handlers if
zlib.output\_compression is activated here. This setting does the same
as <a href="/outcontrol/setup.html#" class="link">output_handler</a> but
in a different order.

资源类型
--------

This extension defines a file pointer resource returned by <span
class="function">gzopen</span>.
