安装／配置
==========

**目录**

-   [需求](/uopz/setup.html#需求)
-   [安装](/uopz/setup.html#安装)
-   [运行时配置](/uopz/setup.html#运行时配置)
-   [资源类型](/uopz/setup.html#资源类型)

需求
----

uopz 2 requires PHP 5.4+. uopz 5.0 requires PHP 7. As of uopz 5.1, PHP
7.1+ is required.

安装
----

uopz releases are hosted by PECL and the source code by
<a href="https://github.com/krakjoe/uopz" class="link external">» github</a>,
the easiest route to installation is the normal PECL route:
<a href="https://pecl.php.net/package/uopz" class="link external">» https://pecl.php.net/package/uopz</a>.

Windows users can download prebuilt release binaries from the
<a href="https://windows.php.net/downloads/pecl/releases/uopz" class="link external">» PECL</a>
website.

As of uopz 5.0.0 the extension must be loaded as
<a href="/ini/core.html#ini.extension" class="link">extension</a>.
Before this version it must be loaded as
<a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                        | 默认 | 可修改范围       | 更新日志                                              |
|-------------------------------------------------------------|------|------------------|-------------------------------------------------------|
| <a href="/uopz/setup.html#" class="link">uopz.disable</a>   | "0"  | PHP\_INI\_SYSTEM | Available as of uopz 5.0.2                            |
| <a href="/uopz/setup.html#" class="link">uopz.exit</a>      | "0"  | PHP\_INI\_SYSTEM | Available as of uopz 6.0.1                            |
| <a href="/uopz/setup.html#" class="link">uopz.overloads</a> | "1"  | PHP\_INI\_SYSTEM | Available as of uopz 2.0.2. Removed as of uopz 5.0.0. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`uopz.disable` <span class="type">bool</span>  
If enabled, uopz should stop having any effect on the engine.

`uopz.exit` <span class="type">bool</span>  
Whether to allow the execution of exit opcodes or not. This setting can
be overridden during runtime by calling <span
class="function">uopz\_allow\_exit</span>.

`uopz.exit` <span class="type">bool</span>  
Enables the ability to use <span class="function">uopz\_overload</span>.

> **Note**: <span class="simpara"> When running with OPcache enabled, it
> may be necessary to disable all
> <a href="/opcache/setup.html#" class="link">OPcache optimizations</a>
> (`opcache.optimization_level=0`). </span>

资源类型
--------

此扩展没有定义资源类型。
