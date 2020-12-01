安装／配置
==========

**目录**

-   [需求](/errorfunc/setup.html#需求)
-   [安装](/errorfunc/setup.html#安装)
-   [运行时配置](/errorfunc/setup.html#运行时配置)
-   [资源类型](/errorfunc/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                            | 默认        | 可修改范围       | 更新日志                           |
|---------------------------------------------------------------------------------|-------------|------------------|------------------------------------|
| <a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a> | NULL        | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">display_errors</a>                | "1"         | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">display_startup_errors</a>        | "0"         | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">log_errors</a>                    | "0"         | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">log_errors_max_len</a>            | "1024"      | PHP\_INI\_ALL    | Available since PHP 4.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">ignore_repeated_errors</a>        | "0"         | PHP\_INI\_ALL    | Available since PHP 4.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">ignore_repeated_source</a>        | "0"         | PHP\_INI\_ALL    | Available since PHP 4.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">report_memleaks</a>               | "1"         | PHP\_INI\_ALL    | Available since PHP 4.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">track_errors</a>                  | "0"         | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">html_errors</a>                   | "1"         | PHP\_INI\_ALL    | PHP\_INI\_SYSTEM in PHP \<= 4.2.3. |
| <a href="/errorfunc/setup.html#" class="link">xmlrpc_errors</a>                 | "0"         | PHP\_INI\_SYSTEM | Available since PHP 4.1.0.         |
| <a href="/errorfunc/setup.html#" class="link">xmlrpc_error_number</a>           | "0"         | PHP\_INI\_ALL    | Available since PHP 4.1.0.         |
| <a href="/errorfunc/setup.html#" class="link">docref_root</a>                   | ""          | PHP\_INI\_ALL    | Available since PHP 4.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">docref_ext</a>                    | ""          | PHP\_INI\_ALL    | Available since PHP 4.3.2.         |
| <a href="/errorfunc/setup.html#" class="link">error_prepend_string</a>          | NULL        | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">error_append_string</a>           | NULL        | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">error_log</a>                     | NULL        | PHP\_INI\_ALL    |                                    |
| <a href="/errorfunc/setup.html#" class="link">syslog.facility</a>               | "LOG\_USER" | PHP\_INI\_SYSTEM | Available as of PHP 7.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">syslog.filter</a>                 | "no-ctrl"   | PHP\_INI\_ALL    | Available as of PHP 7.3.0.         |
| <a href="/errorfunc/setup.html#" class="link">syslog.ident</a>                  | "php"       | PHP\_INI\_SYSTEM | Available as of PHP 7.3.0.         |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`error_reporting` <span class="type">integer</span>  
设置错误报告的级别。该参数可以是一个任意的表示二进制位字段的整数，或者常数名称。错误级别和常数是在
<a href="/errorfunc/constants.html" class="link">预定义常量</a>定义的，在
`php.ini` 之中也有专门的说明。在程序运行时，还可以通过 <span
class="function">error\_reporting</span> 函数进行设置。请查看
<a href="/errorfunc/setup.html#" class="link">display_errors</a>
了解详情。

在 PHP5.3 及以上版本中，默认值为 **`E_ALL`** & \~**`E_NOTICE`** &
\~**`E_STRICT`** & \~**`E_DEPRECATED`**。 该设置不会显示
**`E_NOTICE`**、 **`E_STRICT`** 、**`E_DEPRECATED`**
级错误提示。在开发时可以把它们显示出来。 在 PHP 5.3.0
以前版本中，默认值是 **`E_ALL`** & \~**`E_NOTICE`** & \~**`E_STRICT`**。
在 PHP 4 中，默认值是 **`E_ALL`** & \~**`E_NOTICE`**。

> **Note**:
>
> 在开发阶段启用 **`E_NOTICE`**
> 会有一些好处。出于调试的目的：通知信息会对代码中可能出现的bug给出警告。例如，使用未预先分配和定义的值，就会给出警告。它对于查找拼写错误非常有用，并且可以节省调试的时间。通知信息也会警告你使用更好的代码风格。例如，*$arr\[item\]*
> 最好写成 *$arr\['item'\]* ，因为 PHP 会试图将 *"item"*
> 当成一个常量。如果它不是一个常量，PHP才会把它当做数组的字符串索引。

> **Note**:
>
> 在PHP 5之中，提供了一个新的错误级别 **`E_STRICT`**。 因为
> **`E_STRICT`** 并不包含在 **`E_ALL`**
> 之中，你必须明确启用才能显示这个类别的错误信息。在开发阶段启用
> **`E_STRICT`**
> 会有一些好处。严格的信息将帮助你使用最新和最好的建议的方法来编写代码，例如它会警告你使用了将被废弃的函数。

> **Note**: **PHP外的PHP常量**  
>
> 在 PHP 以外使用PHP的常量是没有意义的，例如在 `httpd.conf` 之中，
> 你需要使用常量对应的 <span class="type">integer</span>
> 值来取代。因为随着时间的推移和PHP的发展，会有更多的错误级别将被添加，因此错误级别的最大值(为
> **`E_ALL`**)可能会改变 。因此在使用 **`E_ALL`**
> 对应整数值的地方，应该考虑使用较大的数值来涵盖当前和将来需要使用的二进制位字段，例如数值
> *2147483647* (将包含所有错误，而不仅仅是 **`E_ALL`**).

`display_errors` <span class="type">string</span>  
该选项设置是否将错误信息作为输出的一部分显示到屏幕，或者对用户隐藏而不显示。

设置 *"stderr"* 表示发送到 *stderr* 而不是 *stdout*。 *"stderr"*从 PHP
5.2.4 开始可用。在以前的版本中，该配置值的类型为 <span
class="type">boolean</span>.

> **Note**:
>
> 这是一个辅助开发的功能，建议永远不要在生产系统中使用
> (例如系统被连接到互联网对外提供服务)。

> **Note**:
>
> 尽管 display\_errors 也可以在运行时设置 (使用 <span
> class="function">ini\_set</span>)，
> 但是脚本出现致命错误时任何运行时的设置都是无效的。
> 因为在这种情况下预期运行的操作不会被执行。

`display_startup_errors` <span class="type">boolean</span>  
即使 display\_errors 设置为开启, PHP
启动过程中的错误信息也不会被显示。强烈建议除了调试目的以外，将
display\_startup\_errors 设置为关闭。

`log_errors` <span class="type">boolean</span>  
设置是否将脚本运行的错误信息记录到服务器错误日志或者<a href="/errorfunc/setup.html#" class="link">error_log</a>之中。注意，这是与服务器相关的特定配置项。

> **Note**:
>
> 在生产系统中，强烈建议你使用错误日志记录web站点上显示的错误信息。

`log_errors_max_len` <span class="type">integer</span>  
设置 log\_errors 的最大字节数. 在
<a href="/errorfunc/setup.html#" class="link">error_log</a>
会添加有关错误源的信息。默认值为1024，如果设置为0表示不限长度。该长度设置对记录的错误，显示的错误，以及
`$php_errormsg`都会有限制作用。

<span class="simpara">当使用 <span class="type">int</span> 时,
其值以字节来衡量。还可以使用在<a href="/faq/using.html#faq.using.shorthandbytes" class="link">FAQ</a>中描述的速记符。</span>

`ignore_repeated_errors` <span class="type">boolean</span>  
不记录重复的信息。重复的错误必须出现在同一个文件中的同一行代码上，除非
<a href="/errorfunc/setup.html#" class="link">ignore_repeated_source</a>
设置为true。

`ignore_repeated_source` <span class="type">boolean</span>  
忽略重复消息时，也忽略消息的来源。当该设置开启时，重复信息将不会记录它是由不同的文件还是不同的源代码行产生的。

`report_memleaks` <span class="type">boolean</span>  
如果这个参数设置为Off，则内存泄露信息不会显示 (在 stdout
或者日志中)。This report will be send to stderr on Posix platforms. On
Windows, it will be send to the debugger using OutputDebugString(), and
can be viewed with tools like
<a href="http://technet.microsoft.com/en-us/sysinternals/bb896647" class="link external">» DbgView</a>。这只对调试编译有效，而且需要
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
包含了 **`E_WARNING`** 才会起作用

`track_errors` <span class="type">boolean</span>  
如果开启，最后的一个错误将永远存在于变量 `$php_errormsg` 中。

`html_errors` <span class="type">boolean</span>  
在错误信息中关闭HTML标签。这种新的HTML格式的错误信息是可以点击，它引导用户前往描述该错误或者导致该错误发生的函数的参考信息页面。
这些参考与 <a href="/errorfunc/setup.html#" class="link">docref_root</a>
和 <a href="/errorfunc/setup.html#" class="link">docref_ext</a>
的设置有关。

`xmlrpc_errors` <span class="type">boolean</span>  
关闭正常的错误报告，并将错误的格式设置为XML-RPC错误信息的格式。

`xmlrpc_error_number` <span class="type">integer</span>  
用作 XML-RPC faultCode 元素的值。

`docref_root` <span class="type">string</span>  
新的错误信息格式包含了对应的参考页面，该页面对错误进行具体描述，或者描述了导致该错误发生的函数。为了提供手册的页面，你可以在PHP官方站点下载对应语言的手册，并在ini中设置网址到本地对应的地址。如果你的本地手册拷贝可以使用*"/manual/"*
访问，你就可以简单的设置 **`docref_root=/manual/`**。另外你还需要设置
docref\_ext 匹配你本地文件的后缀名
**`docref_ext=.html`**。当然也可以设置一个外部的参考地址。例如你可以设置
**`docref_root=http://manual/en/`** 或者
**`docref_root="http://landonize.it/?how=url&theme=classic&filter=Landon       &url=http%3A%2F%2Fwww.php.net%2F"`**

通常需要在 docref\_root 后面以 *"/"*结尾，
但是在以上的第二种示例情况中不必这么设置。

> **Note**:
>
> 因为这么做可以快速定位和查看到函数的说明，所以它对你的开发会非常有用。建议永远不要再生产系统中使用
> (例如系统被连接到互联网对外提供服务)。

`docref_ext` <span class="type">string</span>  
参见 <a href="/errorfunc/setup.html#" class="link">docref_root</a>.

> **Note**:
>
> docref\_ext的值必须以 *"."* 开头.

`error_prepend_string` <span class="type">string</span>  
错误信息之前输出的内容。

`error_append_string` <span class="type">string</span>  
错误信息之后输出的内容。

`error_log` <span class="type">string</span>  
设置脚本错误将被记录到的文件。该文件必须是web服务器用户可写的。如果特殊值
*syslog*
被设置，则将错误信息发送到系统日志记录器。在Unix以及类似系统上，使用的是
syslog(3) ，而在 Windows NT 类系统上则为事件日志。Windows
95上不支持系统日志记录。参见： <span class="function">syslog</span>.
如果该配置没有设置，则错误信息会被发送到 SAPI
错误记录器。例如，出现在Apache的错误日志中，或者在CLI中发送到 *stderr*。

`syslog.facility` <span class="type">string</span>  
指定记录日志信息的程序类型，仅在
<a href="/errorfunc/setup.html#" class="link">error_log</a> 设置为
"syslog" 时有效。

`syslog.filter` <span class="type">string</span>  
Specifies the filter type to filter the logged messages. Allowed
characters are passed unmodified; all others are written in their
hexadecimal representation prefixed with *\\x*. There are three
supported filter types:

-   <span class="simpara">*all* – all characters</span>
-   <span class="simpara">*no-ctrl* – all characters except control
    characters</span>
-   <span class="simpara">*ascii* – all printable ASCII characters and
    *NL*</span>

仅在 <a href="/errorfunc/setup.html#" class="link">error_log</a> 为
"syslog" 时有效。

`syslog.ident` <span class="type">string</span>  
设置每条日志消息前缀的识别字符串（ident string），仅在
<a href="/errorfunc/setup.html#" class="link">error_log</a> 为 "syslog"
时有效。

资源类型
--------

此扩展没有定义资源类型。
