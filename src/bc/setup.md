安装／配置
==========

**目录**

-   [需求](/bc/setup.html#需求)
-   [安装](/bc/setup.html#安装)
-   [运行时配置](/bc/setup.html#运行时配置)
-   [资源类型](/bc/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

本类函数仅在 PHP 编译时配置了 **--enable-bcmath** 时可用。

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                    | 默认 | 可修改范围    | 更新日志 |
|---------------------------------------------------------|------|---------------|----------|
| <a href="/bc/setup.html#" class="link">bcmath.scale</a> | "0"  | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`bcmath.scale` <span class="type">integer</span>  
所有 bcmath 函数中十进制数字的数目。参见 <span
class="function">bcscale</span>。

资源类型
--------

此扩展没有定义资源类型。
