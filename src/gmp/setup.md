安装／配置
==========

**目录**

-   [需求](/gmp/setup.html#需求)
-   [安装](/gmp/setup.html#安装)
-   [运行时配置](/gmp/setup.html#运行时配置)
-   [资源类型](/gmp/setup.html#资源类型)

需求
----

The GMP library can be downloaded from
<a href="http://gmplib.org/#DOWNLOAD" class="link external">» http://gmplib.org/#DOWNLOAD</a>.
This site also has the GMP manual available.

At least GMP version 2 is required, with some functions requiring a more
recent version of the GMP library.

安装
----

In order to have these functions available, PHP must be compiled with
GMP support by using the **--with-gmp** option.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

Prior to PHP 5.6, most GMP functions operate on or return GMP number
resources. PHP 5.6 onwards uses <span class="classname">GMP</span>
objects in place of GMP number resources.
