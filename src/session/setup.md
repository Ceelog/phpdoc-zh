安装／配置
==========

**目录**

-   [需求](/session/setup.html#需求)
-   [安装](/session/setup.html#安装)
-   [运行时配置](/session/setup.html#运行时配置)
-   [资源类型](/session/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

> **Note**:
>
> 你可以选择使用由 Ralf S. Engelschall 开发的 Shared Memory Allocation
> 来作为会话存储. 你需要到
> <a href="http://www.ossp.org/pkg/lib/mm/" class="link external">» mm</a>
> 然后安装它. 这个可选功能在 Windows 平台不可用.注意 mm
> 的这个会话存储模块无法保证并发访问时相同会话间正确的互锁.
> 它可能更多地是适用与存储会话到文件的使用在基于文件系统(比如
> Solaris/Linux 的tmpfs， 或者 BSD 上的`/dev/md`)
> 的共享内存，因为他们能够正确互锁. 因为会话数据是存储在内存从而当web
> 服务器重启时数据将被删除.

安装
----

会话的支持在 PHP 默认为激活。如果不想在 PHP
中加入会话支持，应在配置时指定 **--disable-session**
选项。要为会话存储使用共享内存分配（mm），配置 PHP 时指定
**--with-mm\[=DIR\]** 。

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

> **Note**:
>
> 默认情况下，所有与特定会话相关的数据都被存储在由 INI 选项
> session.save\_path
> 指定的目录下的一个文件中。对每个会话会建立一个文件（不论是否有数据与该会话相关）。这是由于每打开一个会话即建立一个文件，不论是否有数据写入到该文件中。注意由于和文件系统协同工作的限制，此行为有个副作用，有可能造成用户定制的会话处理器（例如用数据库）丢失了未存储数据的会话。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                             | 默认                               | 可修改范围       | 更新日志                                      |
|----------------------------------------------------------------------------------|------------------------------------|------------------|-----------------------------------------------|
| <a href="/session/setup.html#" class="link">session.save_path</a>                | ""                                 | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.name</a>                     | "PHPSESSID"                        | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.save_handler</a>             | "files"                            | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.auto_start</a>               | "0"                                | PHP\_INI\_PERDIR |                                               |
| <a href="/session/setup.html#" class="link">session.gc_probability</a>           | "1"                                | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.gc_divisor</a>               | "100"                              | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.gc_maxlifetime</a>           | "1440"                             | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.serialize_handler</a>        | "php"                              | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cookie_lifetime</a>          | "0"                                | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cookie_path</a>              | "/"                                | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cookie_domain</a>            | ""                                 | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cookie_secure</a>            | ""                                 | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cookie_httponly</a>          | ""                                 | PHP\_INI\_ALL    | 自 PHP 5.2.0 起有效                           |
| <a href="/session/setup.html#" class="link">session.cookie_samesite</a>          | ""                                 | PHP\_INI\_ALL    | 自 PHP 7.3.0 起有效                           |
| <a href="/session/setup.html#" class="link">session.use_strict_mode</a>          | "0"                                | PHP\_INI\_ALL    | 自 PHP 5.5.2 起有效                           |
| <a href="/session/setup.html#" class="link">session.use_cookies</a>              | "1"                                | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.use_only_cookies</a>         | "1"                                | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.referer_check</a>            | ""                                 | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cache_limiter</a>            | "nocache"                          | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.cache_expire</a>             | "180"                              | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.use_trans_sid</a>            | "0"                                | PHP\_INI\_ALL    |                                               |
| <a href="/session/setup.html#" class="link">session.trans_sid_tags</a>           | "a=href,area=href,frame=src,form=" | PHP\_INI\_ALL    | 自 PHP 7.1.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.trans_sid_hosts</a>          | *$\_SERVER\['HTTP\_HOST'\]*        | PHP\_INI\_ALL    | 自 PHP 7.1.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.sid_length</a>               | "32"                               | PHP\_INI\_ALL    | 自 PHP 7.1.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.sid_bits_per_character</a>   | "4"                                | PHP\_INI\_ALL    | 自 PHP 7.1.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.upload_progress.enabled</a>  | "1"                                | PHP\_INI\_PERDIR | 自 PHP 5.4.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.upload_progress.cleanup</a>  | "1"                                | PHP\_INI\_PERDIR | 自 PHP 5.4.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.upload_progress.prefix</a>   | "upload\_progress\_"               | PHP\_INI\_PERDIR | 自 PHP 5.4.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.upload_progress.name</a>     | "PHP\_SESSION\_UPLOAD\_PROGRESS"   | PHP\_INI\_PERDIR | 自 PHP 5.4.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.upload_progress.freq</a>     | "1%"                               | PHP\_INI\_PERDIR | 自 PHP 5.4.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.upload_progress.min_freq</a> | "1"                                | PHP\_INI\_PERDIR | 自 PHP 5.4.0 起有效。                         |
| <a href="/session/setup.html#" class="link">session.lazy_write</a>               | "1"                                | PHP\_INI\_ALL    | 自 PHP 7.0.0 起有效。                         |
| <a href="/session/setup.html#" class="link">url_rewriter.tags</a>                | "a=href,area=href,frame=src,form=" | PHP\_INI\_ALL    | 自 PHP 7.1.0 起，session 功能不再使用此选项。 |
| <a href="/session/setup.html#" class="link">session.hash_function</a>            | "0"                                | PHP\_INI\_ALL    | 自 PHP 7.1.0 起移除。                         |
| <a href="/session/setup.html#" class="link">session.hash_bits_per_character</a>  | "4"                                | PHP\_INI\_ALL    | 自 PHP 7.1.0 起移除。                         |
| <a href="/session/setup.html#" class="link">session.entropy_file</a>             | ""                                 | PHP\_INI\_ALL    | 自 PHP 7.1.0 起移除。                         |
| <a href="/session/setup.html#" class="link">session.entropy_length</a>           | "0"                                | PHP\_INI\_ALL    | 自 PHP 7.1.0 起移除。                         |
| <a href="/session/setup.html#" class="link">session.bug_compat_42</a>            | "1"                                | PHP\_INI\_ALL    | 自 PHP 5.4.0 起移除。                         |
| <a href="/session/setup.html#" class="link">session.bug_compat_warn</a>          | "1"                                | PHP\_INI\_ALL    | 自 PHP 5.4.0 起移除。                         |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

会话管理系统支持许多配置选项，可以在自己的 `php.ini`
文件中设定。这里只是个简短的概览。

`session.save_handler` <span class="type">string</span>  
<span class="simpara"> *session.save\_handler*
定义了来存储和获取与会话关联的数据的处理器的名字。默认为 *files*。Note
that individual extensions may register their own *save\_handler*s;
registered handlers can be obtained on a per-installation basis by
referring to <span class="function">phpinfo</span>. 参见 <span
class="function">session\_set\_save\_handler</span>。 </span>

`session.save_path` <span class="type">string</span>  
<span class="simpara"> *session.save\_path*
定义了传递给存储处理器的参数。如果选择了默认的 files
文件处理器，则此值是创建文件的路径。默认为 */tmp*。参见 <span
class="function">session\_save\_path</span>。 </span>

此指令还有一个可选的 *N* 参数来决定会话文件分布的目录深度。例如，设定为
*'5;/tmp'* 将使创建的会话文件和路径类似于
*/tmp/4/b/1/e/3/sess\_4b1e384ad74619bd212e236e52a5a174If*。要使用 *N*
参数，必须在使用前先创建好这些目录。在 `ext/session` 目录下有个小的
shell 脚本名叫 `mod_files.sh`，windows 版本是 `mod_files.bat`
可以用来做这件事。此外注意如果使用了 *N* 参数并且大于
0，那么将不会执行自动垃圾回收，更多信息见 `php.ini`。另外如果用了 *N*
参数，要确保将 *session.save\_path* 的值用双引号 "quotes"
括起来，因为分隔符分号（ *;*）在 `php.ini` 中也是注释符号。

文件储存模块默认使用 mode 600 创建文件。通过 修改可选参数 *MODE*
来改变这种默认行为： *N;MODE;/path* ，其中 *MODE* 是 mode 的八进制表示。
*MODE* 设置不影响进程的掩码(umask)。

**Warning**
如果将此设定为一个全局可读的目录，例如
`/tmp`（默认值），服务器上的其他用户有可能通过该目录的文件列表破解会话。

**Caution**
使用以上描述的可选目录层级参数 *N*
时请注意，对于绝大多数站点，大于1或者2的值会不太合适——因为这需要创建大量的目录：例如，值设置为
3 需要在文件系统上创建 *64^3* 个目录，将浪费很多空间和 inode。

仅仅在绝对肯定站点足够大时，才可以设置 *N* 大于2。

> **Note**: <span class="simpara"> 在 PHP 4.3.6 之前，Windows
> 用户必须修改此选项以使用 PHP
> 的会话函数。必须指定一个合法路径，例如：`c:/temp`。 </span>

`session.name` <span class="type">string</span>  
<span class="simpara"> *session.name* 指定会话名以用做 cookie
的名字。只能由字母数字组成，默认为 *PHPSESSID*。参见 <span
class="function">session\_name</span>。 </span>

`session.auto_start` <span class="type">boolean</span>  
<span class="simpara"> *session.auto\_start*
指定会话模块是否在请求开始时自动启动一个会话。默认为 *0*（不启动）。
</span>

`session.serialize_handler` <span class="type">string</span>  
<span class="simpara"> *session.serialize\_handler*
定义用来序列化／解序列化的处理器名字。 当前支持 PHP 序列化格式 (名为
*php\_serialize*)、 PHP PHP 内部格式 (名为 *php* 及 *php\_binary*) 和
WDDX (名为 *wddx*)。 如果 PHP 编译时加入了
<a href="/ref/wddx.html" class="link">WDDX 支持</a>，则只能用 WDDX。 自
PHP 5.5.4 起可以使用 *php\_serialize*。 *php\_serialize*
在内部简单地直接使用 serialize/unserialize 函数，并且不会有 *php* 和
*php\_binary* 所具有的限制。 使用较旧的序列化处理器导致 $\_SESSION
的索引既不能是数字也不能包含特殊字符(*\|* and *!*) 。 使用
*php\_serialize* 避免脚本退出时，数字及特殊字符索引导致出错。 默认使用
*php*。 </span>

`session.gc_probability` <span class="type">integer</span>  
<span class="simpara"> *session.gc\_probability* 与
*session.gc\_divisor* 合起来用来管理 gc（garbage collection
垃圾回收）进程启动的概率。默认为 *1*。详见
<a href="/session/setup.html#" class="link">session.gc_divisor</a>。
</span>

`session.gc_divisor` <span class="type">integer</span>  
<span class="simpara"> *session.gc\_divisor* 与
*session.gc\_probability* 合起来定义了在每个会话初始化时启动 gc（garbage
collection 垃圾回收）进程的概率。此概率用 gc\_probability/gc\_divisor
计算得来。例如 1/100 意味着在每个请求中有 1% 的概率启动 gc
进程。*session.gc\_divisor* 默认为 *100*。 </span>

`session.gc_maxlifetime` <span class="type">integer</span>  
<span class="simpara"> *session.gc\_maxlifetime*
指定过了多少秒之后数据就会被视为“垃圾”并被清除。 垃圾搜集可能会在
session 启动的时候开始（
取决于<a href="/session/setup.html#" class="link">session.gc_probability</a>
和
<a href="/session/setup.html#" class="link">session.gc_divisor</a>）。
</span>

> **Note**:
>
> 如果不同的脚本具有不同的 *session.gc\_maxlifetime*
> 数值但是共享了同一个地方存储会话数据，则具有最小数值的脚本会清理数据。此情况下，与
> <a href="/session/setup.html#" class="link">session.save_path</a>
> 一起使用本指令。

`session.referer_check` <span class="type">string</span>  
<span class="simpara"> *session.referer\_check* 包含有用来检查每个 HTTP
Referer 的子串。如果客户端发送了 Referer
信息但是在其中并未找到该子串，则嵌入的会话 ID
会被标记为无效。默认为空字符串。 </span>

`session.entropy_file` <span class="type">string</span>  
<span class="simpara"> *session.entropy\_file*
给出了一个到外部资源（文件）的路径，该资源将在会话 ID
创建进程中被用作附加的熵值资源。例如在许多 Unix 系统下都可以用
*/dev/random* 或 */dev/urandom*。 </span> <span class="simpara"> 在
Windows 上自 PHP 5.3.3 起加入了此功能。 设置 *session.entropy\_length*
为非零的值将使 PHP 使用 Windows Random API 作为熵值源。 </span>

> **Note**: <span class="simpara"> 自 PHP 5.4.0 起，默认情况下，
> *session.entropy\_file* 在 */dev/urandom* 或 */dev/arandom*
> 可用的时候使用它们。 在 PHP 5.3.0 中此指令默认留空。 </span>

`session.entropy_length` <span class="type">integer</span>  
<span class="simpara"> *session.entropy\_length*
指定了从上面的文件中读取的字节数。默认为 *0*（禁用）。 </span>

`session.use_strict_mode` <span class="type">boolean</span>  
<span class="simpara"> *session.use\_strict\_mode* specifies whether the
module will use strict session id mode. If this mode is enabled, the
module does not accept uninitialized session ID. If uninitialized
session ID is sent from browser, new session ID is sent to browser.
Applications are protected from session fixation via session adoption
with strict mode. Defaults to *0* (disabled). </span>

`session.use_cookies` <span class="type">boolean</span>  
<span class="simpara"> *session.use\_cookies* 指定是否在客户端用 cookie
来存放会话 ID。默认为 *1*（启用）。 </span>

`session.use_only_cookies` <span class="type">boolean</span>  
<span class="simpara"> *session.use\_only\_cookies*
指定是否在客户端*仅仅*使用 cookie 来存放会话
ID。。启用此设定可以防止有关通过 URL 传递会话 ID 的攻击。自PHP
5.3.0开始，默认值为*1*（启用） </span>

`session.cookie_lifetime` <span class="type">integer</span>  
<span class="simpara"> *session.cookie\_lifetime*
以秒数指定了发送到浏览器的 cookie 的生命周期。值为 0
表示“直到关闭浏览器”。默认为 *0*。参见 <span
class="function">session\_get\_cookie\_params</span> 和 <span
class="function">session\_set\_cookie\_params</span>。 </span>

> **Note**:
>
> The expiration timestamp is set relative to the server time, which is
> not necessarily the same as the time in the client's browser.

`session.cookie_path` <span class="type">string</span>  
<span class="simpara"> *session.cookie\_path* 指定了要设定会话 cookie
的路径。默认为 */*。参见 <span
class="function">session\_get\_cookie\_params</span> 和 <span
class="function">session\_set\_cookie\_params</span>。 </span>

`session.cookie_domain` <span class="type">string</span>  
<span class="simpara"> *session.cookie\_domain* 指定了要设定会话 cookie
的域名。默认为无，表示根据 cookie 规范产生 cookie 的主机名。参见 <span
class="function">session\_get\_cookie\_params</span> 和 <span
class="function">session\_set\_cookie\_params</span>。 </span>

`session.cookie_secure` <span class="type">boolean</span>  
<span class="simpara"> *session.cookie\_secure*
指定是否仅通过安全连接发送 cookie。默认为 *off*。此设定是 PHP 4.0.4
添加的。参见 <span class="function">session\_get\_cookie\_params</span>
和 <span class="function">session\_set\_cookie\_params</span>。 </span>

`session.cookie_httponly` <span class="type">boolean</span>  
<span class="simpara"> Marks the cookie as accessible only through the
HTTP protocol. This means that the cookie won't be accessible by
scripting languages, such as JavaScript. This setting can effectively
help to reduce identity theft through XSS attacks (although it is not
supported by all browsers). </span>

`session.cookie_samesite` <span class="type">string</span>  
<span class="simpara"> Allows servers to assert that a cookie ought not
to be sent along with cross-site requests. This assertion allows user
agents to mitigate the risk of cross-origin information leakage, and
provides some protection against cross-site request forgery attacks.
Note that this is not supported by all browsers. An empty value means
that no SameSite cookie attribute will be set. *Lax* and *Strict* mean
that the cookie will not be sent cross-domain for POST requests; *Lax*
will sent the cookie for cross-domain GET requests, while *Strict* will
not. </span>

`session.cache_limiter` <span class="type">string</span>  
<span class="simpara"> *session.cache\_limiter*
指定会话页面所使用的缓冲控制方法（none/nocache/private/private\_no\_expire/public）。默认为
*nocache*。参见 <span class="function">session\_cache\_limiter</span>。
</span>

`session.cache_expire` <span class="type">integer</span>  
<span class="simpara"> *session.cache\_expire*
以分钟数指定缓冲的会话页面的存活期，此设定对 nocache
缓冲控制方法无效。默认为 *180*。参见 <span
class="function">session\_cache\_expire</span>。 </span>

`session.use_trans_sid` <span class="type">boolean</span>  
<span class="simpara"> *session.use\_trans\_sid* 指定是否启用透明 SID
支持。默认为 *0*（禁用）。 </span>

> **Note**: <span class="simpara"> 基于 URL 的会话管理比基于 cookie
> 的会话管理有更多安全风险。例如用户有可能通过 email
> 将一个包含有效的会话 ID 的 URL
> 发给他的朋友，或者用户总是有可能在收藏夹中存有一个包含会话 ID 的 URL
> 来以同样的会话 ID 去访问站点。 </span> <span class="simpara"> 自 PHP
> 7.1.0 开始，透明 SID 开始使用完整的 URL 绝对路径，例如
> https://php.net/。 在此之前 PHP 只会使用相对路径。使用
> <a href="/session/setup.html#" class="link">session.trans_sid_hosts</a>
> 定义重写的目标 host。 </span>

`session.trans_sid_tags` <span class="type">string</span>  
<span class="simpara"> *session.trans\_sid\_tags* specifies which HTML
tags are rewritten to include session id when transparent sid support is
enabled. Defaults to *a=href,area=href,frame=src,input=src,form=*
</span> <span class="simpara"> *form* is special tag. *\<input
hidden="session\_id" name="session\_name"\>* is added as form variable.
</span>

> **Note**: <span class="simpara"> Before PHP 7.1.0,
> <a href="/session/setup.html#" class="link">url_rewriter.tags</a> was
> used for this purpose. Since PHP 7.1.0, *fieldset* is no longer
> considered as special tag. </span>

`session.trans_sid_hosts` <span class="type">string</span>  
<span class="simpara"> *session.trans\_sid\_hosts* specifies which hosts
are rewritten to include session id when transparent sid support is
enabled. Defaults to *$\_SERVER\['HTTP\_HOST'\]* Multiple hosts can be
specified by ",", no space is allowed between hosts. e.g.
*php.net,wiki.php.net,bugs.php.net* </span>

`session.bug_compat_42` <span class="type">boolean</span>  
<span class="simpara"> PHP 4.2.3
以及更低版本有一个未公开的特性／错误，它允许用户在
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
被禁用的情况下在全局范围内初始化一个会话变量。PHP 4.3.0
及更高版本会在使用此特性时并且启用了
<a href="/session/setup.html#" class="link">session.bug_compat_warn</a>
时发出警告。此特性／错误可以通过关闭此选项而禁用。 </span>

> **Note**: <span class="simpara"> PHP 5.4.0 中已经移除。 </span>

`session.bug_compat_warn` <span class="type">boolean</span>  
<span class="simpara"> PHP 4.2.3
以及更低版本有一个未公开的特性／错误，它允许用户在
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
被禁用的情况下在全局范围内初始化一个会话变量。PHP 4.3.0
及更高版本会在使用此特性时并且同时启用了
<a href="/session/setup.html#" class="link">session.bug_compat_42</a> 和
<a href="/session/setup.html#" class="link">session.bug_compat_warn</a>
时发出警告。 </span>

> **Note**: <span class="simpara"> PHP 5.4.0 中已经移除。 </span>

`session.sid_length` <span class="type">integer</span>  
<span class="simpara"> *session.sid\_length* allows you to specify the
length of session ID string. Session ID length can be between 22 to 256.
</span> <span class="simpara"> The default is 32. If you need
compatibility you may specify 32, 40, etc. Longer session ID is harder
to guess. At least 32 chars are recommended. </span>

**小贴士**
Compatibility Note: Use 32 instead of *session.hash\_function*=0 (MD5)
and *session.hash\_bits\_per\_character*=4, *session.hash\_function*=1
(SHA1) and *session.hash\_bits\_per\_character*=6. Use 26 instead of
*session.hash\_function*=0 (MD5) and
*session.hash\_bits\_per\_character*=5. Use 22 instead of
*session.hash\_function*=0 (MD5) and
*session.hash\_bits\_per\_character*=6. You must configure INI values to
have at least 128 bits in session ID. Do not forget to set an
appropriate value for *session.sid\_bits\_per\_character*, otherwise you
will have weaker session ID.

> **Note**: <span class="simpara"> This setting is introduced in PHP
> 7.1.0. </span>

`session.sid_bits_per_character` <span class="type">integer</span>  
<span class="simpara"> *session.sid\_per\_character* allows you to
specify the number of bits in encoded session ID character. The possible
values are '4' (0-9, a-f), '5' (0-9, a-v), and '6' (0-9, a-z, A-Z, "-",
","). </span> <span class="simpara"> The default is 4. The more bits
results in stronger session ID. 5 is recommended value for most
environments. </span>

> **Note**: <span class="simpara"> This setting is introduced in PHP
> 7.1.0. </span>

`url_rewriter.tags` <span class="type">string</span>  
<span class="simpara"> *url\_rewriter.tags* 指定在使用透明 SID
支持时哪些 HTML 标记会被修改以加入会话 ID。默认为
*a=href,area=href,frame=src,input=src,form=fakeentry,fieldset=*。
</span>

> **Note**: <span class="simpara"> 如果要符合 XHTML，去掉 *form*
> 项并在表单字段前后加上 \<fieldset\> 标记。 </span>

`session.hash_function` <span class="type">mixed</span>  
<span class="simpara"> *session.hash\_function* 允许用户指定生成会话 ID
的散列算法。'0' 表示 MD5（128 位），'1' 表示 SHA-1（160 位）。 </span>

Since PHP 5.3.0 it is also possible to specify any of the algorithms
provided by the <a href="/ref/hash.html" class="link">hash extension</a>
(if it is available), like *sha512* or *whirlpool*. A complete list of
supported algorithms can be obtained with the <span
class="function">hash\_algos</span> function.

> **Note**:
>
> 这是 PHP 5 引进的。

`session.hash_bits_per_character` <span class="type">integer</span>  
<span class="simpara"> *session.hash\_bits\_per\_character*
允许用户定义将二进制散列数据转换为可读的格式时每个字符存放多少个比特。可能值为
'4'（0-9，a-f），'5'（0-9，a-v），以及 '6'（0-9，a-z，A-Z，"-"，","）。
</span>

> **Note**:
>
> 这是 PHP 5 引进的。

`session.upload_progress.enabled` <span class="type">boolean</span>  
<span class="simpara"> Enables upload progress tracking, populating the
`$_SESSION` variable. Defaults to 1, enabled. </span>

`session.upload_progress.cleanup` <span class="type">boolean</span>  
<span class="simpara"> Cleanup the progress information as soon as all
POST data has been read (i.e. upload completed). Defaults to 1, enabled.
</span>

> **Note**: <span class="simpara"> It is highly recommended to keep this
> feature enabled. </span>

`session.upload_progress.prefix` <span class="type">string</span>  
<span class="simpara"> A prefix used for the upload progress key in the
`$_SESSION`. This key will be concatenated with the value of
*$\_POST\[ini\_get("session.upload\_progress.name")\]* to provide a
unique index. </span> <span class="simpara"> Defaults to
"upload\_progress\_". </span>

`session.upload_progress.name` <span class="type">string</span>  
<span class="simpara"> The name of the key to be used in `$_SESSION`
storing the progress information. See also
<a href="/session/setup.html#" class="link">session.upload_progress.prefix</a>.
</span> <span class="simpara"> If
*$\_POST\[ini\_get("session.upload\_progress.name")\]* is not passed or
available, upload progressing will not be recorded. </span> <span
class="simpara"> Defaults to "PHP\_SESSION\_UPLOAD\_PROGRESS". </span>

`session.upload_progress.freq` <span class="type">mixed</span>  
<span class="simpara"> Defines how often the upload progress information
should be updated. This can be defined in bytes (i.e. "update progress
information after every 100 bytes"), or in percentages (i.e. "update
progress information after receiving every 1% of the whole filesize").
</span> <span class="simpara"> Defaults to "1%". </span>

`session.upload_progress.min_freq` <span class="type">integer</span>  
<span class="simpara"> The minimum delay between updates, in seconds.
Defaults to "1" (one second). </span>

`session.lazy_write` <span class="type">boolean</span>  
<span class="simpara"> *session.lazy\_write*, when set to 1, means that
session data is only rewritten if it changes. Defaults to 1, enabled.
</span>

<a href="/ini/core.html#ini.register-globals" class="link"><em>register_globals</em></a>
配置选项影响到会话变量是怎样存储和恢复的。

Upload progress will not be registered unless
session.upload\_progress.enabled is enabled, and the
$\_POST\[ini\_get("session.upload\_progress.name")\] variable is set.
See
<a href="/session/upload-progress.html" class="link">Session Upload Progress</a>
for mor details on this functionality.

资源类型
--------

此扩展没有定义资源类型。
