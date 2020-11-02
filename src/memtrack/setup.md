安装／配置
==========

**目录**

-   [需求](/memtrack/setup.html#需求)
-   [安装](/memtrack/setup.html#安装)
-   [运行时配置](/memtrack/setup.html#运行时配置)
-   [资源类型](/memtrack/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/memtrack" class="link external">» https://pecl.php.net/package/memtrack</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                              | 默认 | 可修改范围       |
|-------------------------------------------------------------------|------|------------------|
| <a href="/memtrack/setup.html#" class="link">memtrack.enabled</a> | "0"  | PHP\_INI\_SYSTEM |
| memtrack.soft\_limit                                              | "0"  | PHP\_INI\_ALL    |
| memtrack.hard\_limit                                              | "0"  | PHP\_INI\_ALL    |
| memtrack.vm\_limit                                                | "0"  | PHP\_INI\_ALL    |
| memtrack.ignore\_functions                                        | ""   | PHP\_INI\_SYSTEM |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`memtrack.enabled` <span class="type">bool</span>  
Disables or enables the extension. Default value is 0, i.e. disabled.

`memtrack.soft_limit` <span class="type">int</span>  
Soft memory limit.

The extension checks memory consumption before and after executing an
op\_array and produces a warning is the difference between the two
values is equal to or greater than the soft limit, but only if the
function is not ignored.

Setting this option to 0 also disables both soft and hard limit
warnings. Default value is 0, i.e. no warnings is produced.

`memtrack.hard_limit` <span class="type">int</span>  
Hard memory limit.

The extension checks memory consumption before and after executing an
op\_array and produces a warning is the difference between the two
values is equal to or greater than the hard limit, *even if the function
is ignored*. Setting this option to 0 disables hard limit warnings
completely. Default value is 0, i.e. no hard limit warnings is produced.

`memtrack.vm_limit` <span class="type">int</span>  
Virtual memory limit (set on a process).

This limit is checked only on shutdown and a warning is produced if the
value is greater than or equal to the limit.

This option is currently supported only on OSes where mallinfo()
function is available (i.e. Linux).

`memtrack.ignore_functions` <span class="type">string</span>  
A comma or whitespace-separated list of functions which are to be
ignored by soft\_limit. The values are case-insensitive, for class
methods use class::method syntax.

资源类型
--------

此扩展没有定义资源类型。
