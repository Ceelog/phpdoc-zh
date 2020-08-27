安装／配置
==========

**目录**

-   [需求](/cairo/setup.html#需求)
-   [安装](/cairo/setup.html#安装)
-   [运行时配置](/cairo/setup.html#运行时配置)
-   [资源类型](/cairo/setup.html#资源类型)

需求
----

Cairo is only available for PHP 5.2+ and PHP 5.3+ The extension also
requires the cairo graphics library version 1.4 or higher. The cairo
graphics library uses an even and odd numbering scheme to denote stable
and unstable library versions. Both unstable and stable versions can be
used with the extension, but conditional support for new features is
determined by the stable version below the unstable version in use. The
latest cairo release can be found at
<a href="http://cairographics.org/" class="link external">» http://cairographics.org/</a>.

The binary files used for the windows compiles can be found at
<a href="http://cairographics.org/download/" class="link external">» http://cairographics.org/download/</a>
along with the project files used to create them.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/cairo" class="link external">» https://pecl.php.net/package/cairo</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

Notes specific to installation on Windows

Binary builds of the extension can be found at
<a href="http://cairographics.org/download/" class="link external">» http://cairographics.org/download/</a>.
Download the correct zip file, place php\_cairo.dll in the extensions
directory, and enable it via the php.ini file in use. Please be sure the
PHP minor version (5.2, 5.3) match, the thread safety (Thread Safe TS or
Non-Thread Safe NTS), the architecture (x86 or x64), and the compiler
version (VC6 or VC9) match or the extension will not load.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
