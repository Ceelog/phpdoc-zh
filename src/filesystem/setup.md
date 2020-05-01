安装／配置
==========

**目录**

-   [需求](/filesystem/setup.html#需求)
-   [安装](/filesystem/setup.html#安装)
-   [运行时配置](/filesystem/setup.html#运行时配置)
-   [资源类型](/filesystem/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                        | 默认 | 可修改范围       | 更新日志                                                    |
|-----------------------------|------|------------------|-------------------------------------------------------------|
| allow\_url\_fopen           | "1"  | PHP\_INI\_SYSTEM | 在 PHP \<= 4.3.4 时是 PHP\_INI\_ALL。PHP 4.0.4 版以后可用。 |
| user\_agent                 | NULL | PHP\_INI\_ALL    | PHP 4.3.0 版以后可用。                                      |
| default\_socket\_timeout    | "60" | PHP\_INI\_ALL    | PHP 4.3.0 版以后可用。                                      |
| from                        | ""   | PHP\_INI\_ALL    |                                                             |
| auto\_detect\_line\_endings | "0"  | PHP\_INI\_ALL    | PHP 4.3.0 版以后可用。                                      |

这是配置指令的简短说明。

`allow_url_fopen` <span class="type">boolean</span>  
本选项激活了 URL 形式的 fopen 封装协议使得可以访问 URL
对象例如文件。默认的封装协议提供用 ftp 和 http
协议来访问<a href="/features/remote-files.html" class="link">远程文件</a>，一些扩展库例如
<a href="/ref/zlib.html" class="link">zlib</a>
可能会注册更多的封装协议。

> **Note**:
>
> 出于安全性考虑，此选项只能在 php.ini 中设置。

> **Note**:
>
> 此选项是紧接着版本 4.0.3 发布后引进的。版本 4.0.3
> 以及之前的版本只能在编译时通过配置项
> <a href="/configure/about.html#configure.disable-url-fopen-wrapper" class="link"><code class="parameter">        --disable-url-fopen-wrapper</code></a>
> 来取消此特性。

**Warning**
Windows 版在 PHP 4.3.0 之前，以下函数不支持远程文件访问：<span
class="function">include</span>，<span
class="function">include\_once</span>, <span
class="function">require</span>，<span
class="function">require\_once</span>
和<a href="/ref/image.html" class="xref">GD 和图像处理 函数</a>中的
imagecreatefromXXX 函数。

`allow_url_include` <span class="type">boolean</span>  
This option allows the use of URL-aware fopen wrappers with the
following functions: <span class="function">include</span>, <span
class="function">include\_once</span>, <span
class="function">require</span>, <span
class="function">require\_once</span>.

> **Note**:
>
> This setting requires allow\_url\_fopen to be on.

`user_agent` <span class="type">string</span>  
定义 PHP 发送的 User-Agent。

`default_socket_timeout` <span class="type">integer</span>  
基于 socket 的流的默认超时时间（秒）。

> **Note**: <span class="simpara"> 本配置参数是 PHP 4.3.0 引进的。
> </span>

`from` <span class="type">string</span>  
定义匿名 ftp 的密码（email 地址）。

`auto_detect_line_endings` <span class="type">boolean</span>  
当设为 On 时，PHP 将检查通过 <span class="function">fgets</span> 和
<span class="function">file</span> 取得的数据中的行结束符号是符合
Unix，MS-DOS，还是 Macintosh 的习惯。

这使得 PHP 可以和 Macintosh 系统交互操作，但是默认值是
Off，因为在检测第一行的 EOL 习惯时会有很小的性能损失，而且在 Unix
系统下使用回车符号作为项目分隔符的人们会遭遇向下不兼容的行为。

> **Note**: <span class="simpara"> 本配置参数是 PHP 4.3.0 引进的。
> </span>

资源类型
--------

文件系统使用 *streams* 作为资源类型。 Streams
的文档有专门的章节：<a href="/book/stream.html" class="link">Streams</a>。
