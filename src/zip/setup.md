安装／配置
==========

**目录**

-   [需求](/zip/setup.html#需求)
-   [安装](/zip/setup.html#安装)
-   [运行时配置](/zip/setup.html#运行时配置)
-   [资源类型](/zip/setup.html#资源类型)

需求
----

PHP 5.2.0 或更新版本
--------------------

此扩展用到 Jean-loup Gailly 和 Mark Adle 的
<a href="http://www.zlib.net/" class="link external">» zlib</a>
里的函数。

安装
----

PHP 4
-----

> **Note**:
>
> PHP 4.1.0 之前是实验性的支持 ZIP。

**Warning**

因为 PHP4 zip 扩展无人维护，所以我们推荐使用 PECL 扩展来代替绑定的这个。

Linux 系统
----------

为了使用这些函数，必须在编译 PH P时用 **--with-zip\[=DIR\]**
配置选项来提供 zip 支持，其中 \[DIR\]是 ZZIPlib 库安装路径。

Windows
-------

Windows 用户需要在 `php.ini` 里使 `php_zip.dll` 可用，以便使用这些函数。

PHP 5.2.0 以及更新版本
----------------------

Linux 系统
----------

为了使用这些函数，必须在编译 PHP 时用 **--enable-zip** 配置选项来提供
zip 支持。

Windows
-------

Windows 用户需要在 `php.ini` 里使 `php_zip.dll` 可用，以便使用这些函数。

通过 PECL 安装
--------------

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/zip" class="link external">» https://pecl.php.net/package/zip</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

在 PHP 4 中，此 DLL 位于 PHP Windows 二进制下载中的 `extensions/` 目录。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

在 Zip 模块里用到两种资源类型。第一种是 Zip 文档的 Zip
目录，第二种是文档条目的 Zip 条目。
