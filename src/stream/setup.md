安装／配置
==========

**目录**

-   [需求](/stream/setup.html#需求)
-   [安装](/stream/setup.html#安装)
-   [运行时配置](/stream/setup.html#运行时配置)
-   [Stream Classes](/stream/setup.html#Stream%20Classes)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

Stream Classes
--------------

User designed wrappers can be registered via <span
class="function">stream\_wrapper\_register</span>, using the class
definition shown on that manual page.

Class <span class="classname">php\_user\_filter</span> is predefined and
is an abstract baseclass for use with user defined filters. See the
manual page for <span class="function">stream\_filter\_register</span>
for details on implementing user defined filters.
