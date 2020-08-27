安装／配置
==========

**目录**

-   [需求](/xmlrpc/setup.html#需求)
-   [安装](/xmlrpc/setup.html#安装)
-   [运行时配置](/xmlrpc/setup.html#运行时配置)
-   [资源类型](/xmlrpc/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--with-libxml**，或在 PHP 7.4 之前的版本中使用
**--enable-libxml**， 尽管这将隐式完成因为 libxml 是缺省开启的。

安装
----

默认情况下在 PHP 中是不能使用 XML-RPC 支持的。你需要使用
**--with-xmlrpc\[=DIR\]** 配置选项编译 PHP 才能够使用 XML-RPC 支持。从
PHP 4.1.0 开始附带了此扩展。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines a XML-RPC server resource returned by <span
class="function">xmlrpc\_server\_create</span>.
