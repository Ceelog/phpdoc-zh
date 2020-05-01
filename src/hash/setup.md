安装／配置
==========

**目录**

-   [需求](/hash/setup.html#需求)
-   [安装](/hash/setup.html#安装)
-   [运行时配置](/hash/setup.html#运行时配置)
-   [资源类型](/hash/setup.html#资源类型)

需求
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

安装
----

从 PHP 5.1.2 开始，哈希扩展是内置的，不需要外部库， 并且默认是启用的。

可以通过 --disable-hash 参数来禁用此扩展。 对于更早版本的
PHP，可以通过安装
<a href="https://pecl.php.net/package/hash" class="link external">» PECL 模块</a>
来使用哈希扩展。

从 PHP 7.4.0 开始，Hash 扩展成为 PHP 的核心扩展，所以可以直接使用。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

本扩展中定义了哈希上下文资源类型， 该类型资源由 <span
class="function">hash\_init</span> 函数返回。
