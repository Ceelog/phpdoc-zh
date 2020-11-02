安装／配置
==========

**目录**

-   [需求](/nsapi/setup.html#需求)
-   [安装](/nsapi/setup.html#安装)
-   [运行时配置](/nsapi/setup.html#运行时配置)
-   [资源类型](/nsapi/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

For PHP installation on Netscape/iPlanet/Sun webservers see the NSAPI
section (<a href="/install/unix/sun.html" class="link">UNIX</a>,
<a href="/install/windows/legacy/index.html#install.windows.legacy.sun" class="link">Windows</a>)
in the installation chapter.

运行时配置
----------

The behaviour of the NSAPI PHP module is affected by settings in
`php.ini`. Configuration settings from `php.ini` may be overridden by
additional parameters to the *php4\_execute* call in `obj.conf`

| 名字                                                             | 默认 | 可修改范围    | 更新日志 |
|------------------------------------------------------------------|------|---------------|----------|
| <a href="/nsapi/setup.html#" class="link">nsapi.read_timeout</a> | "60" | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`nsapi.read_timeout` <span class="type">int</span>  
Sets the time in seconds the plugin is waiting for POST data from the
client.

资源类型
--------

此扩展没有定义资源类型。
