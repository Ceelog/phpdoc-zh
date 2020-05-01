安装／配置
==========

**目录**

-   [需求](/regex/setup.html#需求)
-   [安装](/regex/setup.html#安装)
-   [运行时配置](/regex/setup.html#运行时配置)
-   [资源类型](/regex/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

**Warning**

除非知道自己在做什么，否则不要改变 TYPE。

要激活 regexp 的支持在配置 PHP 时加上 **--with-regex\[=TYPE\]**。TYPE
可以是 system，apache 或 php 之一。默认使用 php。

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
