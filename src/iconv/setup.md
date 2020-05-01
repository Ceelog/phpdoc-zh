安装／配置
==========

**目录**

-   [需求](/iconv/setup.html#需求)
-   [安装](/iconv/setup.html#安装)
-   [运行时配置](/iconv/setup.html#运行时配置)
-   [资源类型](/iconv/setup.html#资源类型)

需求
----

如果你使用了最新的 POSIX 兼容系统，则不需要安装其他程序，因为系统提供的
C 语言标准函数库肯定支持 iconv。否则，你必须在系统上安装
<a href="http://www.gnu.org/software/libiconv/" class="link external">» libiconv</a>
函数库。

安装
----

默认已激活此扩展，但是它能够在编译时通过 **--without-iconv**
选项被禁用。

选项指令 **--with-iconv-dir** 用于 PHP 编译时指定 *iconv*
在系统里的路径，否则会扫描默认路径。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                  | 默认 | 可修改范围    | 更新日志                                   |
|-----------------------------------------------------------------------|------|---------------|--------------------------------------------|
| <a href="/iconv/setup.html#" class="link">iconv.input_encoding</a>    | ""   | PHP\_INI\_ALL | 自 PHP 4.0.5 起有效。在 PHP 5.6.0 中废弃。 |
| <a href="/iconv/setup.html#" class="link">iconv.output_encoding</a>   | ""   | PHP\_INI\_ALL | 自 PHP 4.0.5 起有效。在 PHP 5.6.0 中废弃。 |
| <a href="/iconv/setup.html#" class="link">iconv.internal_encoding</a> | ""   | PHP\_INI\_ALL | 自 PHP 4.0.5 起有效。在 PHP 5.6.0 中废弃。 |

这是配置指令的简短说明。

**Warning**

有些系统（比如 IBM AIX） 使用 "ISO8859-1" 来代替
"ISO-8859-1"，所以在配置选项和函数参数中必须使用这个值。

`iconv.input_encoding` <span class="type">string</span>  
**Warning**
This feature has been *DEPRECATED* as of PHP 5.6.0. Relying on this
feature is highly discouraged.

PHP 5.6 及以上的用户应该留空并以
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>
取代。

`iconv.output_encoding` <span class="type">string</span>  
**Warning**
This feature has been *DEPRECATED* as of PHP 5.6.0. Relying on this
feature is highly discouraged.

PHP 5.6 及以上的用户应该留空并以
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>
取代。

`iconv.internal_encoding` <span class="type">string</span>  
**Warning**
This feature has been *DEPRECATED* as of PHP 5.6.0. Relying on this
feature is highly discouraged.

PHP 5.6 及以上的用户应该留空并以
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>
取代。

资源类型
--------

此扩展没有定义资源类型。
