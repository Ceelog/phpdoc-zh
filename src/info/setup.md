安装／配置
==========

**目录**

-   [需求](/info/setup.html#需求)
-   [安装](/info/setup.html#安装)
-   [运行时配置](/info/setup.html#运行时配置)
-   [资源类型](/info/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                 | 默认 | 可修改范围       | 更新日志                                                   |
|----------------------------------------------------------------------|------|------------------|------------------------------------------------------------|
| <a href="/info/setup.html#" class="link">assert.active</a>           | "1"  | PHP\_INI\_ALL    |                                                            |
| <a href="/info/setup.html#" class="link">assert.bail</a>             | "0"  | PHP\_INI\_ALL    |                                                            |
| <a href="/info/setup.html#" class="link">assert.warning</a>          | "1"  | PHP\_INI\_ALL    |                                                            |
| <a href="/info/setup.html#" class="link">assert.callback</a>         | NULL | PHP\_INI\_ALL    |                                                            |
| <a href="/info/setup.html#" class="link">assert.quiet_eval</a>       | "0"  | PHP\_INI\_ALL    |                                                            |
| <a href="/info/setup.html#" class="link">assert.exception</a>        | "0"  | PHP\_INI\_ALL    | Available since PHP 7.0.0.                                 |
| <a href="/info/setup.html#" class="link">enable_dl</a>               | "1"  | PHP\_INI\_SYSTEM | 本过时特性*将*肯定会在未来被*移除*。                       |
| <a href="/info/setup.html#" class="link">max_execution_time</a>      | "30" | PHP\_INI\_ALL    |                                                            |
| <a href="/info/setup.html#" class="link">max_input_time</a>          | "-1" | PHP\_INI\_PERDIR | 自 PHP 4.3.0 起有效。                                      |
| <a href="/info/setup.html#" class="link">max_input_nesting_level</a> | "64" | PHP\_INI\_PERDIR | 自 PHP 4.4.8 and PHP 5.2.3 起有效。                        |
| <a href="/info/setup.html#" class="link">max_input_vars</a>          | 1000 | PHP\_INI\_PERDIR | 自 PHP 5.3.9 起有效。                                      |
| <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>        | "1"  | PHP\_INI\_PERDIR | 在 PHP \<= 4.2.3 是 PHP\_INI\_ALL，在 PHP 5.4.0 中被移除。 |
| <a href="/info/setup.html#" class="link">magic_quotes_runtime</a>    | "0"  | PHP\_INI\_ALL    | 在 PHP 5.4.0 中移除                                        |
| <a href="/info/setup.html#" class="link">zend.enable_gc</a>          | "1"  | PHP\_INI\_ALL    | 自 PHP 5.3.0 起有效。                                      |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`assert.active` <span class="type">boolean</span>  
激活 <span class="function">assert</span> 断言评测。

`assert.bail` <span class="type">boolean</span>  
失败的断言将中止脚本。

`assert.warning` <span class="type">boolean</span>  
为每个失败的断言产生一条 PHP 警告信息

`assert.callback` <span class="type">string</span>  
失败的断言将调用用户的函数

`assert.quiet_eval` <span class="type">boolean</span>  
在 断言表达式执行时 <span class="function">error\_reporting</span>
使用当前的设置。 如果启用了，在执行时错误将不会被显示（隐式的
error\_reporting(0)）。 如果禁用了，错误将根据 <span
class="function">error\_reporting</span> 的设置来显示。

`assert.exception` <span class="type">boolean</span>  
在断言（assert）失败时产生 <span class="classname">AssertionError</span>
异常。

`enable_dl` <span class="type">boolean</span>  
该指令仅对 Apache 模块版本的 PHP 有效。
你可以针对每个虚拟机或每个目录开启或关闭 <span
class="function">dl</span> 动态加载 PHP 模块。

关闭动态加载的主要原因是为了安全。通过动态加载，有可能忽略所有
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
限制。 默认允许动态加载，除了使用
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>。在
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>，总是无法使用
<span class="function">dl</span>。

`max_execution_time` <span class="type">integer</span>  
这设置了脚本被解析器中止之前允许的最大执行时间，单位秒。
这有助于防止写得不好的脚本占尽服务器资源。 默认设置为 *30*。
从<a href="/features/commandline.html" class="link">命令行</a>运行 PHP
时，默认设置为 *0*。

最大执行时间不会影响系统调用和系统操作等。更多细节参见 <span
class="function">set\_time\_limit</span>。

在
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>
下你不能通过 <span class="function">ini\_set</span> 来修改此设置。
唯一的解决方法是关闭安全模式或者在 `php.ini` 中修改时间限制。

你的 web 服务器也可以有其他超时设置，也有可能中断 PHP 的执行。 Apache
有一个 *Timeout* 指令，IIS 有一个 CGI 超时功能。 他们默认都是 300
秒。更多具体信息参见你的 web 服务器的文档。

`max_input_time` <span class="type">integer</span>  
脚本解析输入数据（类似 POST 和 GET）允许的最大时间，单位是秒。
它从接收所有数据到开始执行脚本进行测量的。

`max_input_nesting_level` <span class="type">integer</span>  
设置<a href="/language/variables/external.html" class="link">输入变量</a>的嵌套深度
(例如 `$_GET`，`$_POST`……)

`max_input_vars` <span class="type">integer</span>  
接受多少
<a href="/language/variables/external.html" class="link">输入的变量</a>（限制分别应用于
$\_GET、$\_POST 和 $\_COOKIE 超全局变量）
指令的使用减轻了以哈希碰撞来进行拒绝服务攻击的可能性。
如有超过指令指定数量的输入变量，将会导致 **`E_WARNING`** 的产生，
更多的输入变量将会从请求中截断。

`magic_quotes_gpc` <span class="type">boolean</span>  
**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

为 GPC (Get/Post/Cookie) 操作设置 magic\_quotes 状态。 当 magic\_quotes
为 on，所有的 ' (单引号)、" (双引号)、\\（反斜杠）和 NUL's
被一个反斜杠自动转义。

> **Note**:
>
> 在 PHP 4，`$_ENV`也会被转义。

> **Note**:
>
> 如果 <a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>
> 也是 ON，它会完全覆盖 magic\_quotes\_gpc。
> 两个指令都启用意味着只有单引号被转义为 *''*。 双引号、反斜杠和 NUL's
> 不会被转义。

See also <span class="function">get\_magic\_quotes\_gpc</span>

`magic_quotes_runtime` <span class="type">boolean</span>  
**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

如果启用了
`magic_quotes_runtime`，大多数返回任何形式外部数据的函数，包括数据库和文本段将会用反斜线转义引号。
如果启用了
<a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>，单引号会被单引号转义而不是反斜线。

受 `magic_quotes_runtime` 影响的函数（不包括 PECL 里的函数）：

-   <span class="function">get\_meta\_tags</span>
-   <span class="function">file\_get\_contents</span>
-   <span class="function">file</span>
-   <span class="function">fgets</span>
-   <span class="function">fwrite</span>
-   <span class="function">fread</span>
-   <span class="function">fputcsv</span>
-   <span class="function">stream\_socket\_recvfrom</span>
-   <span class="function">exec</span>
-   <span class="function">system</span>
-   <span class="function">passthru</span>
-   <span class="function">stream\_get\_contents</span>
-   <span class="function">bzread</span>
-   <span class="function">gzfile</span>
-   <span class="function">gzgets</span>
-   <span class="function">gzwrite</span>
-   <span class="function">gzread</span>
-   <span class="function">exif\_read\_data</span>
-   <span class="function">dba\_insert</span>
-   <span class="function">dba\_replace</span>
-   <span class="function">dba\_fetch</span>
-   <span class="function">ibase\_fetch\_row</span>
-   <span class="function">ibase\_fetch\_assoc</span>
-   <span class="function">ibase\_fetch\_object</span>
-   <span class="function">mssql\_fetch\_row</span>
-   <span class="function">mssql\_fetch\_object</span>
-   <span class="function">mssql\_fetch\_array</span>
-   <span class="function">mssql\_fetch\_assoc</span>
-   <span class="function">mysqli\_fetch\_row</span>
-   <span class="function">mysqli\_fetch\_array</span>
-   <span class="function">mysqli\_fetch\_assoc</span>
-   <span class="function">mysqli\_fetch\_object</span>
-   <span class="function">pg\_fetch\_row</span>
-   <span class="function">pg\_fetch\_assoc</span>
-   <span class="function">pg\_fetch\_array</span>
-   <span class="function">pg\_fetch\_object</span>
-   <span class="function">pg\_fetch\_all</span>
-   <span class="function">pg\_select</span>
-   <span class="function">sybase\_fetch\_object</span>
-   <span class="function">sybase\_fetch\_array</span>
-   <span class="function">sybase\_fetch\_assoc</span>
-   <span class="function">SplFileObject::fgets</span>
-   <span class="function">SplFileObject::fgetcsv</span>
-   <span class="function">SplFileObject::fwrite</span>

`zend.enable_gc` <span class="type">boolean</span>  
启用或禁用循环引用记数搜集器。

资源类型
--------

此扩展没有定义资源类型。
