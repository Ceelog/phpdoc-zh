安装／配置
==========

**目录**

-   [需求](/libxml/setup.html#需求)
-   [安装](/libxml/setup.html#安装)
-   [运行时配置](/libxml/setup.html#运行时配置)
-   [资源类型](/libxml/setup.html#资源类型)

需求
----

This extension requires
<a href="http://www.xmlsoft.org/" class="link external">» libxml</a> \>=
2.6.0.

安装
----

The libxml extension is enabled by default, although it may be disabled
with **--disable-libxml**.

The optional **--with-libxml-dir** directive is used to specify the
location of *libxml* on the system that PHP is being compiled on,
otherwise only the default locations are scanned. The *configure*
process checks for libxml (specifically, *xml2-config*) in the following
order:

1.  The location (\[DIR\]) specified with **--with-libxml-dir**
    (\[DIR\]=`/bin/xml2-config`)

2.  `/usr/local/bin/xml2-config`

3.  `/usr/bin/xml2-config`

If *configure* cannot find `xml2-config` in the directory specified by
**--with-libxml-dir**, then it'll continue on and check the default
locations.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
