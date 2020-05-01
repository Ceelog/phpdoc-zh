安装／配置
==========

**目录**

-   [需求](/bzip2/setup.html#需求)
-   [安装](/bzip2/setup.html#安装)
-   [运行时配置](/bzip2/setup.html#运行时配置)
-   [资源类型](/bzip2/setup.html#资源类型)

需求
----

本模块使用了 Julian Seward 的
<a href="https://www.sourceware.org/bzip2/" class="link external">» bzip2</a>
库中的函数。本模块需要 bzip2/libbzip2 版本 \>= 1.0.x。

安装
----

PHP 的 Bzip2 支持默认未打开。编译 PHP 时需要 **--with-bz2\[=DIR\]**
配置选项来激活 bzip2 支持。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

本扩展定义了一种资源类型：用于识别和操作 bz2 文件的指针。
