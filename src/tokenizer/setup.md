安装／配置
==========

**目录**

-   [需求](/tokenizer/setup.html#需求)
-   [安装](/tokenizer/setup.html#安装)
-   [运行时配置](/tokenizer/setup.html#运行时配置)
-   [资源类型](/tokenizer/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

从 PHP 4.4.0 开始，这些函数默认是被激活的. 对于旧版本在配置和编译 PHP
是使用 **--enable-tokenizer**选项. 也能使用
**--disable-tokenizer**选项禁用 tokenizer 支持.

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

> **Note**: <span class="simpara"> tokenizer 的内建支持在 PHP 4.3.0
> 后可用 </span>

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
