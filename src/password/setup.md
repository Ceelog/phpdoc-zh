安装／配置
==========

**目录**

-   [需求](/password/setup.html#需求)
-   [安装](/password/setup.html#安装)
-   [运行时配置](/password/setup.html#运行时配置)
-   [资源类型](/password/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

为了支持 Argon2 密码哈希，需要
<a href="https://github.com/P-H-C/phc-winner-argon2" class="link external">» libargon2</a>。
PHP 7.3.0 起，需要 libargon2 为 20161029 或更高的版本。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

为了使用 Argon2 密码哈希，PHP 必须用 **--with-password-argon2\[=DIR\]**
配置选项和 libargon2 构建。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
