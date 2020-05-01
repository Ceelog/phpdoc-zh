安装／配置
==========

**目录**

-   [需求](/fileinfo/setup.html#需求)
-   [安装](/fileinfo/setup.html#安装)
-   [运行时配置](/fileinfo/setup.html#运行时配置)
-   [资源类型](/fileinfo/setup.html#资源类型)

需求
----

PHP 5.3.0 之前的版本，需要 *magic\_open* 库来 构建此扩展。

安装
----

从 PHP 5.3.0 开始，本扩展是默认开启的。 在之前的版本中，fileinfo 是一个
PECL 扩展，但是已经不再持续维护。 5.3+ 之前的版本， 可以使用
<a href="https://pecl.php.net/package/fileinfo" class="link external">» 停止使用的 PECL 扩展</a>。

Windows 用户需要在 `php.ini` 中开启绑定的 `php_fileinfo.dll` DLL
来启用本扩展。

PHP 中绑定了 libmagic 库，某些 PHP 版本变更中也可能包含此库。 在 PHP
fileinfo 扩展的源代码中，有 `libmagic.patch` 文件， 这是 libmagic
库的补丁包文件。

| PHP 版本 | 更新的 libmagic 版本 | 说明 |
|----------|----------------------|------|
| 5.3.2    | 5.03                 |      |
| 5.3.0    | 5.02                 |      |

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

Fileinfo 扩展中用到了 1 个资源： <span
class="function">finfo\_open</span> 函数返回的魔数数据库文件描述符。
