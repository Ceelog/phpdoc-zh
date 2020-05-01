安装／配置
==========

**目录**

-   [需求](/sem/setup.html#需求)
-   [安装](/sem/setup.html#安装)
-   [运行时配置](/sem/setup.html#运行时配置)
-   [资源类型](/sem/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

Support for this functions are not enabled by default. To enable System
V semaphore support compile PHP with the option **--enable-sysvsem**. To
enable the System V shared memory support compile PHP with the option
**--enable-sysvshm**. To enable the System V messages support compile
PHP with the option **--enable-sysvmsg**.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                         | 默认  | 可修改范围       | 更新日志 |
|--------------------------------------------------------------|-------|------------------|----------|
| <a href="/sem/setup.html#" class="link">sysvshm.init_mem</a> | 10000 | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`sysvshm.init_mem` <span class="type">int</span>  
A default size of the shared memory segment.

资源类型
--------

此扩展没有定义资源类型。
