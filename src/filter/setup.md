安装／配置
==========

**目录**

-   [需求](/filter/setup.html#需求)
-   [安装](/filter/setup.html#安装)
-   [运行时配置](/filter/setup.html#运行时配置)
-   [资源类型](/filter/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

The filter extension is enabled by default as of PHP 5.2.0. To disable
the filter extension, use **--disable-filter**.

Before PHP 5.2 an experimental PECL extension was used, however, the
PECL version is no longer recommended or updated.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                | 默认          | 可修改范围       | 更新日志                                                      |
|---------------------------------------------------------------------|---------------|------------------|---------------------------------------------------------------|
| <a href="/filter/setup.html#" class="link">filter.default</a>       | "unsafe\_raw" | PHP\_INI\_PERDIR | PHP\_INI\_ALL in filter \<= 0.9.4. Available since PHP 5.2.0. |
| <a href="/filter/setup.html#" class="link">filter.default_flags</a> | NULL          | PHP\_INI\_PERDIR | PHP\_INI\_ALL in filter \<= 0.9.4. Available since PHP 5.2.0. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`filter.default` <span class="type">string</span>  
Filter all `$_GET`, `$_POST`, `$_COOKIE`, `$_REQUEST` and `$_SERVER`
data by this filter. Original data can be accessed through <span
class="function">filter\_input</span>.

Accepts the name of the filter you like to use by default. See the
existing <a href="/filter/filters.html" class="link">filter list</a> for
the list of the filter names.

> **Note**:
>
> Be careful about the default flags for the default filters. You should
> explicitly set them to the value you want. For example, to configure
> the default filter to behave exactly like <span
> class="function">htmlspecialchars</span> you need to set them default
> flags to 0 as shown below.
>
> **示例 \#1 Configuring the default filter to act like
> htmlspecialchars**
>
> ``` php
> filter.default = full_special_chars
> filter.default_flags = 0
> ```

`filter.default_flags` <span class="type">int</span>  
Default flags to apply when the default filter is set. This is set to
**`FILTER_FLAG_NO_ENCODE_QUOTES`** by default for backwards
compatibility reasons. See the
<a href="/filter/filters.html#Filter%20flags" class="link">flag list</a>
for the list of all the flag names.

资源类型
--------

此扩展没有定义资源类型。
