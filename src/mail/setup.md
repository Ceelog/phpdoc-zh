安装／配置
==========

**目录**

-   [需求](/mail/setup.html#需求)
-   [安装](/mail/setup.html#安装)
-   [运行时配置](/mail/setup.html#运行时配置)
-   [资源类型](/mail/setup.html#资源类型)

需求
----

为了使右键函数正常运行，PHP 必须在编译时访问你系统里的 *sendmail*
可执行文件。 如果你使用了其他邮件程序，例如 <span
class="productname">qmail</span> 或者 <span
class="productname">postfix</span>，请确保它们使用了与 sendmail
适配的包装器。 PHP 首先会在你的 *PATH* 变量里查找
sendmail，然后在下面的路径里查找：
*/usr/bin:/usr/sbin:/usr/etc:/etc:/usr/ucblib:/usr/lib*。 强烈建议
sendmail 在您的 *PATH* 变量里。并且，运行编译后PHP程序的用户也必须有执行
sendmail 的权限。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                           | 默认        | 可修改范围       | 更新日志            |
|----------------------------------------------------------------|-------------|------------------|---------------------|
| <a href="/mail/setup.html#" class="link">mail.add_x_header</a> | "0"         | PHP\_INI\_PERDIR | 自 PHP 5.3.0 起生效 |
| <a href="/mail/setup.html#" class="link">mail.log</a>          | NULL        | PHP\_INI\_PERDIR | 自 PHP 5.3.0 起生效 |
| <a href="/mail/setup.html#" class="link">SMTP</a>              | "localhost" | PHP\_INI\_ALL    |                     |
| <a href="/mail/setup.html#" class="link">smtp_port</a>         | "25"        | PHP\_INI\_ALL    | 自 PHP 4.3.0 起可用 |
| <a href="/mail/setup.html#" class="link">sendmail_from</a>     | NULL        | PHP\_INI\_ALL    |                     |
| <a href="/mail/setup.html#" class="link">sendmail_path</a>     | NULL        | PHP\_INI\_SYSTEM |                     |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`mail.add_x_header` <span class="type">bool</span>  
Add *X-PHP-Originating-Script* that will include UID of the script
followed by the filename.

`mail.log` <span class="type">string</span>  
The path to a log file that will log all <span
class="function">mail</span> calls. Log entries include the full path of
the script, line number, *To* address and headers.

`SMTP` <span class="type">string</span>  
仅用于 Windows：PHP 在 <span class="function">mail</span>
函数中用来发送邮件的 SMTP 服务器的主机名称或者 IP 地址。

`smtp_port` <span class="type">int</span>  
仅用于 Windows：*SMTP* 服务器的端口号，默认为 25。自 PHP 4.3.0 起可用。

`sendmail_from` <span class="type">string</span>  
在 Windows 下用 PHP 发送邮件时的“From:”邮件地址的值。该选项同时设置了
“Return-Path:”头。

`sendmail_path` <span class="type">string</span>  
**sendmail** 程序的路径，通常为 `/usr/sbin/sendmail` 或
`/usr/lib/sendmail`。**configure**
脚本会尝试找到该程序并设定为默认值，但是如果失败的话，可以在这里设定。

不使用 **sendmail** 的系统应将此指令设定为其邮件系统提供的 sendmail
替代程序，如果有的话。例如，<a href="http://cr.yp.to/qmail.html" class="link external">» Qmail</a>
用户通常可以设为 `/var/qmail/bin/sendmail` 或
`/var/qmail/bin/qmail-inject`。

**qmail-inject** 不需要任何选项就能正确处理邮件。

此指令也可用于 Windows。如果设定，`smtp`，`smtp_port` 和 `sendmail_from`
都被忽略并运行指定的命令。

资源类型
--------

此扩展没有定义资源类型。
