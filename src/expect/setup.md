安装／配置
==========

**目录**

-   [需求](/expect/setup.html#需求)
-   [安装](/expect/setup.html#安装)
-   [运行时配置](/expect/setup.html#运行时配置)
-   [资源类型](/expect/setup.html#资源类型)

需求
----

This module uses the functions of the
<a href="http://expect.nist.gov/" class="link external">» expect</a>
library. You need libexpect version \>= 5.43.0.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/expect" class="link external">» https://pecl.php.net/package/expect</a>.

In order to use these functions you must compile PHP with expect support
by using the **--with-expect\[=DIR\]** configure option.

Windows users will enable `php_expect.dll` inside of `php.ini` in order
to use these functions. PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

In order to configure expect extension, there are configuration options
in the
<a href="/configuration/file.html" class="link">configuration file</a>
`php.ini`.

| 名字                                                            | 默认 | 可修改范围    | Changelog |
|-----------------------------------------------------------------|------|---------------|-----------|
| <a href="/expect/setup.html#" class="link">expect.timeout</a>   | "10" | PHP\_INI\_ALL |           |
| <a href="/expect/setup.html#" class="link">expect.loguser</a>   | "1"  | PHP\_INI\_ALL |           |
| <a href="/expect/setup.html#" class="link">expect.logfile</a>   | ""   | PHP\_INI\_ALL |           |
| <a href="/expect/setup.html#" class="link">expect.match_max</a> | ""   | PHP\_INI\_ALL |           |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`expect.timeout` <span class="type">int</span>  
The timeout period for waiting for the data, when using the <span
class="function">expect\_expectl</span> function.

A value of "-1" disables a timeout from occurring.

> **Note**:
>
> A value of "0" causes the <span
> class="function">expect\_expectl</span> function to return
> immediately.

`expect.loguser` <span class="type">bool</span>  
Whether expect should send any output from the spawned process to
stdout. Since interactive programs typically echo their input, this
usually suffices to show both sides of the conversation.

`expect.logfile` <span class="type">string</span>  
Name of the file, where the output from the spawned process will be
written. If this file doesn't exist, it will be created.

> **Note**:
>
> If this configuration is not empty, the output is written regardless
> of the value of
> <a href="/expect/setup.html#" class="link">expect.loguser</a>.

`expect.match_max` <span class="type">int</span>  
Changes default size (2000 bytes) of the buffer used to match asterisks
in patterns.

资源类型
--------

<span class="function">expect\_popen</span> returns an open PTY stream
used by <span class="function">expect\_expectl</span>.
