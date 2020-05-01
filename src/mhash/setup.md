安装／配置
==========

**目录**

-   [需求](/mhash/setup.html#需求)
-   [安装](/mhash/setup.html#安装)
-   [运行时配置](/mhash/setup.html#运行时配置)
-   [资源类型](/mhash/setup.html#资源类型)

需求
----

To use it, download the mhash distribution from
<a href="http://mhash.sourceforge.net/" class="link external">» its web site</a>
and follow the included installation instructions.

安装
----

You need to compile PHP with the **--with-mhash\[=DIR\]** parameter to
enable this extension. DIR is the mhash installation directory.

As of PHP 5.3.0, the mhash extension is emulated thru the
<a href="/ref/hash.html" class="link">Hash</a> extension. This makes the
mhash installation directory have no effect, and requires the hash
extension enabled to make the mhash support available.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
