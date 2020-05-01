安装／配置
==========

**目录**

-   [需求](/datetime/setup.html#需求)
-   [安装](/datetime/setup.html#安装)
-   [运行时配置](/datetime/setup.html#运行时配置)
-   [资源类型](/datetime/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

> **Note**: **获取最新版的时区数据**  
>
> 可以通过安装 PECL 的
> <a href="https://pecl.php.net/get/timezonedb" class="link external">» timezonedb</a>
> 模块来获取最新的时区数据。

> **Note**: **在 PHP 5.1.x 中支持的试验性时区**  
>
> 虽然 <span class="classname">DateTime</span> 类及其相关函数自 PHP
> 5.2.0 版本开始 就是默认启用的，也可以通过设置
> *CFLAGS=-DEXPERIMENTAL\_DATE\_SUPPORT=1* 参数来配置/编译 PHP 5.1.x
> 版本来实现试验性的支持。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                    | 默认      | 可修改范围    | 更新日志            |
|-------------------------------------------------------------------------|-----------|---------------|---------------------|
| <a href="/datetime/setup.html#" class="link">date.default_latitude</a>  | "31.7667" | PHP\_INI\_ALL | 自 PHP 5.0.0 起可用 |
| <a href="/datetime/setup.html#" class="link">date.default_longitude</a> | "35.2333" | PHP\_INI\_ALL | 自 PHP 5.0.0 起可用 |
| <a href="/datetime/setup.html#" class="link">date.sunrise_zenith</a>    | "90.83"   | PHP\_INI\_ALL | 自 PHP 5.0.0 起可用 |
| <a href="/datetime/setup.html#" class="link">date.sunset_zenith</a>     | "90.83"   | PHP\_INI\_ALL | 自 PHP 5.0.0 起可用 |
| <a href="/datetime/setup.html#" class="link">date.timezone</a>          | ""        | PHP\_INI\_ALL | 自 PHP 5.0.0 起可用 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`date.default_latitude` <span class="type">float</span>  
默认纬度。

`date.default_longitude` <span class="type">float</span>  
默认经度。

`date.sunrise_zenith` <span class="type">float</span>  
默认日出天顶。

`date.sunset_zenith` <span class="type">float</span>  
默认日落天顶。

`date.timezone` <span class="type">string</span>  
在未设定 `TZ` 环境变量时用于所有日期／时间函数的默认时区。优先顺序在
<span class="function">date\_default\_timezone\_get</span>
页面中有说明。 支持的时区可参见
<a href="/timezones.html" class="xref">所支持的时区列表</a>。

> **Note**: <span class="simpara"> 前四个配置选项目前仅用于 <span
> class="function">date\_sunrise</span> 和 <span
> class="function">date\_sunset</span>。 </span>

资源类型
--------

此扩展没有定义资源类型。
