安装／配置
==========

**目录**

-   [需求](/misc/setup.html#需求)
-   [安装](/misc/setup.html#安装)
-   [运行时配置](/misc/setup.html#运行时配置)
-   [资源类型](/misc/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                           | 默认       | 可修改范围       | 更新日志             |
|----------------------------------------------------------------|------------|------------------|----------------------|
| <a href="/misc/setup.html#" class="link">ignore_user_abort</a> | "0"        | PHP\_INI\_ALL    |                      |
| <a href="/misc/setup.html#" class="link">highlight.string</a>  | "\#DD0000" | PHP\_INI\_ALL    |                      |
| <a href="/misc/setup.html#" class="link">highlight.comment</a> | "\#FF8000" | PHP\_INI\_ALL    |                      |
| <a href="/misc/setup.html#" class="link">highlight.keyword</a> | "\#007700" | PHP\_INI\_ALL    |                      |
| <a href="/misc/setup.html#" class="link">highlight.bg</a>      | "\#FFFFFF" | PHP\_INI\_ALL    | 在PHP 5.4.0.中已移除 |
| <a href="/misc/setup.html#" class="link">highlight.html</a>    | "\#0000BB" | PHP\_INI\_ALL    |                      |
| <a href="/misc/setup.html#" class="link">highlight.html</a>    | "\#000000" | PHP\_INI\_ALL    |                      |
| <a href="/misc/setup.html#" class="link">browscap</a>          | NULL       | PHP\_INI\_SYSTEM |                      |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`ignore_user_abort` <span class="type">boolean</span>  
默认值为 **`false`** 。 如果设置为 **`true`**
，在客户端断开连接后，脚本不会被中止。

参见 <span class="function">ignore\_user\_abort</span>.

`highlight.bg` <span class="type">string</span>  
`highlight.comment` <span class="type">string</span>  
`highlight.default` <span class="type">string</span>  
`highlight.html` <span class="type">string</span>  
`highlight.keyword` <span class="type">string</span>  
`highlight.string` <span class="type">string</span>  
语法高亮的颜色。可设置为 \<font color="??????"\> 中任何可接受的代码。

`browscap` <span class="type">string</span>  
浏览器功能文件的位置和文件名 (例如 `browscap.ini`)。 参见 <span
class="function">get\_browser</span>。

资源类型
--------

此扩展没有定义资源类型。
