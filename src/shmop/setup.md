安装／配置
==========

**目录**

-   [需求](/shmop/setup.html#需求)
-   [安装](/shmop/setup.html#安装)
-   [运行时配置](/shmop/setup.html#运行时配置)
-   [资源类型](/shmop/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

To use shmop you will need to compile PHP with the **--enable-shmop**
parameter in your configure line.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

Prior to PHP 8.0.0, this extension defined the resource type *shmop*
which is a handle to a shared memory block.
