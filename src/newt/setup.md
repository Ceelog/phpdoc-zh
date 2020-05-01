安装／配置
==========

**目录**

-   [需求](/newt/setup.html#需求)
-   [安装](/newt/setup.html#安装)
-   [运行时配置](/newt/setup.html#运行时配置)
-   [资源类型](/newt/setup.html#资源类型)

需求
----

This module uses the functions of the RedHat Newt library. You need
libnewt version \>= 0.51.0.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/newt" class="link external">» https://pecl.php.net/package/newt</a>.

In order to use these functions you must compile CGI or CLI PHP with
newt support by using the **--with-newt\[=DIR\]** configure option.

> **Note**:
>
> This extension is not available for Windows platform.
>
> You may need also *curses* and *slang* libraries, in order to compile
> this extension. To specify locations of these libraries, use the
> following configuration options:
> *--with-curses-dir=/path/to/libcurses*
> *--with-slang-dir=/path/to/libslang*

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension uses two resource types: "newt component" and "newt
grid".

Resource type "newt component" is returned by functions, which create
common newt widgets (for example: <span
class="function">newt\_button</span>)

Resource type "newt grid" is a special link identifier for components,
returned by newt grid factory functions (for example: <span
class="function">newt\_create\_grid</span>)
