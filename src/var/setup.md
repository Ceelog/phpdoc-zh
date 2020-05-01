安装／配置
==========

**目录**

-   [需求](/var/setup.html#需求)
-   [安装](/var/setup.html#安装)
-   [运行时配置](/var/setup.html#运行时配置)
-   [资源类型](/var/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                  | 默认 | 可修改范围    | 更新日志              |
|-----------------------------------------------------------------------|------|---------------|-----------------------|
| <a href="/var/setup.html#" class="link">unserialize_callback_func</a> | NULL | PHP\_INI\_ALL | 自 PHP 4.2.0 起可用。 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`unserialize_callback_func` <span class="type">string</span>  
如果解串行器发现有未定义类要被实例化，将会调用 <span
class="function">unserialize</span>
回调函数（用该未定义类名作为参数）。如果指定函数不存在，或者此函数没有包含／实现该未定义类，则显示警告。所以仅在确实需要实现这样的回调函数时才设置该选项。

参见 <span class="function">unserialize</span> 和
<a href="/language/oop5/autoload.html" class="link">Autoloading Objects</a>.

资源类型
--------

此扩展没有定义资源类型。
