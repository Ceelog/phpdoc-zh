安装／配置
==========

**目录**

-   [需求](/xsl/setup.html#需求)
-   [安装](/xsl/setup.html#安装)
-   [运行时配置](/xsl/setup.html#运行时配置)
-   [资源类型](/xsl/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--enable-libxml**，尽管这将隐式完成因为 libxml
是缺省开启的。

This extension uses <span class="productname">libxslt</span> which can
be found at
<a href="http://xmlsoft.org/XSLT/" class="link external">» http://xmlsoft.org/XSLT/</a>.
libxslt version 1.1.0 or greater is required.

安装
----

PHP 5 includes the XSL extension by default and can be enabled by adding
the argument **--with-xsl\[=DIR\]** to your configure line (*DIR* being
the libxslt installation directory).

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
