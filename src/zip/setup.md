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

Linux 系统
----------

从 PHP 7.4.0 开始，必须在编译 PHP 时用 **--with-zip** 配置选项来提供 zip
支持。之前的 PHP 版本，需要使用 **--enable-zip** 选项。

从 PHP 5.6.0 开始，添加了一个选项 **--with-libzip=DIR** 用来指定系统的
libzip 目录。要求 libzip 最低版本为 0.11，推荐使用 0.11.2 及以上版本。

从 PHP 7.3.0 开始, 不鼓励使用捆绑的 libzip 进行构建，但通过在配置中添加
**--without-libzip** 参数仍然可以实现。 从 PHP 7.4.0 开始，捆绑的 libzip
被移除。

Windows
-------

PHP 5.3 之后该扩展已经内置。之前的版本，Windows 用户需要在 `php.ini`
里使 `php_zip.dll` 可用，以便使用这些函数。

通过 PECL 安装
--------------

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/zip" class="link external">» https://pecl.php.net/package/zip</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

在 Zip 模块里用到两种资源类型。第一种是 Zip 文档的 Zip
目录，第二种是文档条目的 Zip 条目。
