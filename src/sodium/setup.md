安装／配置
==========

**目录**

-   [需求](/sodium/setup.html#需求)
-   [安装](/sodium/setup.html#安装)
-   [运行时配置](/sodium/setup.html#运行时配置)
-   [资源类型](/sodium/setup.html#资源类型)

需求
----

This extension requires
<a href="https://libsodium.org/" class="link external">» libsodium</a> ≥
1.0.8.

安装
----

As of PHP 7.2.0 this extension is bundled with PHP. For older PHP
versions this extension is available via PECL.

Linux Systems
-------------

In order to use this extension you must compile PHP with sodium support
by using the **--with-sodium\[=DIR\]** configure option.

Windows
-------

In order to use this extension you have to add
*extension=php\_sodium.dll* to `php.ini`.

Installation via PECL
---------------------

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/libsodium" class="link external">» https://pecl.php.net/package/libsodium</a>

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------
