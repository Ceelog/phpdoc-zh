安装／配置
==========

**目录**

-   [需求](/wddx/setup.html#需求)
-   [安装](/wddx/setup.html#安装)
-   [运行时配置](/wddx/setup.html#运行时配置)
-   [资源类型](/wddx/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--enable-libxml**，尽管这将隐式完成因为 libxml
是缺省开启的。

In order to use WDDX, you will need to install the expat library (which
comes with Apache 1.3.7 or higher).

安装
----

After installing the required expat library, compile PHP with
**--enable-wddx**, and use **--with-libexpat-dir** for expat.

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines a WDDX packet identifier returned by <span
class="function">wddx\_packet\_start</span>.
