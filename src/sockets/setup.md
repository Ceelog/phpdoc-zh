安装／配置
==========

**目录**

-   [需求](/sockets/setup.html#需求)
-   [安装](/sockets/setup.html#安装)
-   [运行时配置](/sockets/setup.html#运行时配置)
-   [资源类型](/sockets/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

这里描述的socket函数只是PHP扩展的一部分，编译PHP时必须在**配置**中添加**--enable-sockets**配置项来启用。

> **Note**: <span class="simpara">在 PHP 5.0.0 开始加入了对 IPv6
> 的支持。</span>

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

<span class="function">socket\_accept</span>, <span
class="function">socket\_create\_listen</span> 和 <span
class="function">socket\_create</span> 返回socket资源类型。
