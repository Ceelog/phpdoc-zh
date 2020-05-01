安装／配置
==========

**目录**

-   [需求](/network/setup.html#需求)
-   [安装](/network/setup.html#安装)
-   [运行时配置](/network/setup.html#运行时配置)
-   [资源类型](/network/setup.html#资源类型)

需求
----

Functions <span class="function">checkdnsrr</span>, <span
class="function">getmxrr</span> and <span
class="function">dns\_get\_record</span> requires Bind on Linux.

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                    | 默认 | 可修改范围    | 更新日志                                       |
|-------------------------------------------------------------------------|------|---------------|------------------------------------------------|
| <a href="/network/setup.html#" class="link">define_syslog_variables</a> | "0"  | PHP\_INI\_ALL | Deprecated in PHP 5.3.0. Removed in PHP 5.4.0. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`define_syslog_variables` <span class="type">boolean</span>  
Whether or not to define the various syslog variables (e.g. $LOG\_PID,
$LOG\_CRON, etc.). Turning it off is a good idea performance-wise. At
runtime, you can define these variables by calling <span
class="function">define\_syslog\_variables</span>.

资源类型
--------

This extension defines a file pointer resource returned by <span
class="function">fsockopen</span> and <span
class="function">pfsockopen</span>.
