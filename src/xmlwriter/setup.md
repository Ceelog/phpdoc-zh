安装／配置
==========

**目录**

-   [需求](/xmlwriter/setup.html#需求)
-   [安装](/xmlwriter/setup.html#安装)
-   [运行时配置](/xmlwriter/setup.html#运行时配置)
-   [资源类型](/xmlwriter/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--with-libxml**，或在 PHP 7.4 之前的版本中使用
**--enable-libxml**， 尽管这将隐式完成因为 libxml 是缺省开启的。

安装
----

The XMLWriter extension was initially a PECL extension for PHP 5. It was
later added to the PHP source (bundled) as of PHP 5.1.2. This extension
is enabled by default.

此扩展默认为启用，编译时可通过下列选项禁用： **--disable-xmlwriter**

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

Prior to PHP 8.0.0, there was one resource type used by the procedural
version of the XMLWriter extension: returned by <span
class="function">xmlwriter\_open\_memory</span> or <span
class="function">xmlwriter\_open\_uri</span>.
