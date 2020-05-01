安装／配置
==========

**目录**

-   [需求](/apache/setup.html#需求)
-   [安装](/apache/setup.html#安装)
-   [运行时配置](/apache/setup.html#运行时配置)
-   [资源类型](/apache/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

PHP 安装到 Apache 参见
<a href="/install.html" class="link">installation chapter</a>。

运行时配置
----------

Apache 的 PHP 模块的行为受 `php.ini` 的设置影响。在 `php.ini`
中的设置可以被服务器配置文件或本地的 `.htaccess` 文件中的
<a href="/configuration/changes.html#configuration.changes.apache" class="link">php_flag</a>
设置所覆盖。

**示例 \#1 用 `.htaccess` 禁用一个目录的 PHP 解析**

    php_flag engine off

| 名字                                                           | 默认 | 可修改范围    | 更新日志            |
|----------------------------------------------------------------|------|---------------|---------------------|
| <a href="/apache/setup.html#" class="link">engine</a>          | "1"  | PHP\_INI\_ALL | 自 PHP 4.0.5 起可用 |
| <a href="/apache/setup.html#" class="link">child_terminate</a> | "0"  | PHP\_INI\_ALL | 自 PHP 4.0.5 起可用 |
| <a href="/apache/setup.html#" class="link">last_modified</a>   | "0"  | PHP\_INI\_ALL | 自 PHP 4.0.5 起可用 |
| <a href="/apache/setup.html#" class="link">xbithack</a>        | "0"  | PHP\_INI\_ALL | 自 PHP 4.0.5 起可用 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`engine` <span class="type">boolean</span>  
打开或关闭 PHP 解析。本指令仅在使用 PHP 的 Apache
模块版本时才有用。可以基于目录或者虚拟主机来打开或者关闭 PHP。将
**`engine off`** 放到 `httpd.conf` 文件中适当的位置就可以激活或禁用
PHP。

`child_terminate` <span class="type">boolean</span>  
指定 PHP 脚本在请求结束后是否可以要求终止子进程。参见 <span
class="function">apache\_child\_terminate</span>。

`last_modified` <span class="type">boolean</span>  
在本次请求中发送一个头信息 Last-Modified:，显示 PHP
脚本最后被修改的日期。

`xbithack` <span class="type">boolean</span>  
不管文件结尾是什么，将文件作为 PHP 以可执行位组来解析。

资源类型
--------

此扩展没有定义资源类型。
