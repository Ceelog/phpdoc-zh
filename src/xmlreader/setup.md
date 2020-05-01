安装／配置
==========

**目录**

-   [需求](/xmlreader/setup.html#需求)
-   [安装](/xmlreader/setup.html#安装)
-   [运行时配置](/xmlreader/setup.html#运行时配置)
-   [资源类型](/xmlreader/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--enable-libxml**，尽管这将隐式完成因为 libxml
是缺省开启的。

安装
----

The XMLReader extension was initially a PECL extension for PHP 5. It was
later moved to the PHP source (bundled) as of PHP 5.1.0, and later
enabled by default as of PHP 5.1.2.

此扩展默认为启用,编译时可通过下列选项禁用： **--disable-xmlreader**

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
