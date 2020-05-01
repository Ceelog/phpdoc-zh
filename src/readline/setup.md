安装／配置
==========

**目录**

-   [需求](/readline/setup.html#需求)
-   [安装](/readline/setup.html#安装)
-   [运行时配置](/readline/setup.html#运行时配置)
-   [资源类型](/readline/setup.html#资源类型)

需求
----

如果要使用 readline 函数，你必须安装 libreadline. 你能在 GNU readline
项目主页找到 libreadline.
地址<a href="http://cnswww.cns.cwru.edu/~chet/readline/rltop.html" class="link external">» http://cnswww.cns.cwru.edu/~chet/readline/rltop.html</a>
. 它被 Chet Ramey 维护， 他也是 Bash 的作者

你也能使用非 GPL 的 libedit 库来替代 readline 库， libedit 库是使用 BSD
证书，你可以从<a href="http://www.thrysoee.dk/editline/" class="link external">» http://www.thrysoee.dk/editline/</a>下载.

安装
----

要使用这些函数，你必须在编译 PHP 的 CGI 或者 CLI 版本时启用 readline
支持. 你需要在编译配置 PHP 时使用 **--with-readline\[=DIR\]**选项.
如果你想使用 libedit 来代替 readline , 配置 PHP 时使用
**--with-libedit\[=DIR\]**选项

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                        | 默认            | 可修改范围    | 更新日志           |
|-------------------------------------------------------------|-----------------|---------------|--------------------|
| <a href="/readline/setup.html#" class="link">cli.pager</a>  | ""              | PHP\_INI\_ALL | 自 PHP 5.4.0 可用. |
| <a href="/readline/setup.html#" class="link">cli.prompt</a> | "\\\\b \\\\\> " | PHP\_INI\_ALL | 自 PHP 5.4.0 可用. |

这是配置指令的简短说明。

`cli.pager` <span class="type">string</span>  
External tool to display output from
<a href="/features/commandline.html" class="link">command line</a>.

`cli.prompt` <span class="type">string</span>  
<a href="/features/commandline.html" class="link">命令行</a> 提示.

资源类型
--------

此扩展没有定义资源类型。
