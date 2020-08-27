安装／配置
==========

**目录**

-   [需求](/ftp/setup.html#需求)
-   [安装](/ftp/setup.html#安装)
-   [运行时配置](/ftp/setup.html#运行时配置)
-   [资源类型](/ftp/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

要使用这些 FTP 相关函数，在编译的时候请添加 **--enable-ftp** 选项。

PHP 5 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

从 PHP 7.0.0 开始的 Windows
版本，默认以动态的方式载入该扩展，使用前需要在 `php.ini` 中开启该扩展。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

本扩展使用一种资源类型，就是由 <span
class="function">ftp\_connect</span> 或 <span
class="function">ftp\_ssl\_connect</span> 函数返回的连接标示符。
