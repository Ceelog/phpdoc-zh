安装／配置
==========

**目录**

-   [需求](/intl/setup.html#需求)
-   [安装](/intl/setup.html#安装)
-   [运行时配置](/intl/setup.html#运行时配置)
-   [资源类型](/intl/setup.html#资源类型)

需求
----

To build the extension you need to install the
<a href="http://www.icu-project.org/" class="link external">» ICU</a>
library, version 4.0.0 or newer is required. As of PHP 7.4.0 ICU 50.1 or
newer is required.

This extension is bundled with PHP as of PHP version 5.3.0.
Alternatively, the PECL version of this extension may be used with all
PHP versions greater than 5.2.0 (5.2.4+ recommended).

安装
----

This extension may be installed using the bundled version as of PHP
5.3.0, or as a PECL extension as of PHP 5.2.0. In other words, there are
two methods to install the intl extension.

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/intl" class="link external">» https://pecl.php.net/package/intl</a>.

Alternatively, *--enable-intl* will enable the bundled version while
compiling PHP.

If your ICU is installed to a non-standard directory then you might want
to specify its location in **`LD_LIBRARY_PATH`** environment variable so
that dynamic linker can find it:

$ export LD\_LIBRARY\_PATH=/opt/icu/lib

Otherwise, if PHP and ICU are installed to their default locations, then
the additional options to \`configure' are not needed.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                             | 默认 | 可修改范围    | 更新日志                                 |
|------------------------------------------------------------------|------|---------------|------------------------------------------|
| <a href="/intl/setup.html#" class="link">intl.default_locale</a> |      | PHP\_INI\_ALL |                                          |
| <a href="/intl/setup.html#" class="link">intl.error_level</a>    | 0    | PHP\_INI\_ALL |                                          |
| <a href="/intl/setup.html#" class="link">intl.use_exceptions</a> | 0    | PHP\_INI\_ALL | Available since PHP 5.5 and PECL 3.0.0a1 |

这是配置指令的简短说明。

`intl.default_locale` <span class="type">string</span>  
The locale that will be used in intl functions when none is specified
(either by omitting the corresponding argument or by passing *NULL*).
These are ICU locales, not system locales. The built-in ICU locales and
their data can be explored at
<a href="http://demo.icu-project.org/icu-bin/locexp" class="link external">» http://demo.icu-project.org/icu-bin/locexp</a>.

The default value is empty, which forces the usage of ICU's default
locale. Once set, the ini setting cannot be reset to this default value.
It is not recommended that this default be relied on, as its effective
value depends on the server's environment.

`intl.error_level` <span class="type">int</span>  
The level of the error messages generated when an error occurs in ICU
functions. This is a PHP error level, such as **`E_WARNING`**. It can be
set to *0* in order to inhibit the messages. This does not affect the
return values indicating error or the values returned by <span
class="function">intl\_get\_error\_code</span> or by the class specific
methods for retrieving error codes and messages. Choosing *E\_ERROR*
will terminate the script whenever an error condition is found on intl
classes.

The default value is *0*.

`intl.use_exceptions` <span class="type">int</span>  
If set to true, an exception will be raised whenever an error occurs in
an intl function. The exception will be of type <span
class="classname">IntlException</span>. This is possibly in addition to
the error message generated due to
<a href="/intl/setup.html#" class="link">intl.error_level</a>.

The default value is **`FALSE`**.

资源类型
--------

此扩展没有定义资源类型。
