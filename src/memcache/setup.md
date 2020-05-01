安装／配置
==========

**目录**

-   [需求](/memcache/setup.html#需求)
-   [安装](/memcache/setup.html#安装)
-   [运行时配置](/memcache/setup.html#运行时配置)
-   [资源类型](/memcache/setup.html#资源类型)

需求
----

此模块使用了函数
<a href="http://www.zlib.net/" class="link external">» zlib</a>
来支持数据压缩，因此安装此模块需要安装 Zlib 模块。

PHP 4.3.3 及以后版本需要使用 memcache 扩展。

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/memcache" class="link external">» https://pecl.php.net/package/memcache</a>.

> **Note**:
>
> 可以关闭memcache session处理器的支持。使用pecl
> install进行安装时，在静态编译到php中时使用选项
> **--disable-memcache-session**可以关闭memcache的session
> 支持（默认时开启的）。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                            | 默认       | 可修改范围      | 更新日志                        |
|---------------------------------------------------------------------------------|------------|-----------------|---------------------------------|
| <a href="/memcache/setup.html#" class="link">memcache.allow_failover</a>        | "1"        | PHP\_INI\_ALL   | Available since memcache 2.0.2. |
| <a href="/memcache/setup.html#" class="link">memcache.max_failover_attempts</a> | "20"       | PHP\_INI\_ALL   | Available since memcache 2.1.0. |
| <a href="/memcache/setup.html#" class="link">memcache.chunk_size</a>            | "8192"     | PHP\_INI\_ALL   | Available since memcache 2.0.2. |
| <a href="/memcache/setup.html#" class="link">memcache.default_port</a>          | "11211"    | PHP\_INI\_ALL   | Available since memcache 2.0.2. |
| <a href="/memcache/setup.html#" class="link">memcache.hash_strategy</a>         | "standard" | PHP\_INI\_ALL   | Available since memcache 2.2.0. |
| <a href="/memcache/setup.html#" class="link">memcache.hash_function</a>         | "crc32"    | PHP\_INI\_ALL   | Available since memcache 2.2.0. |
| <a href="/session/setup.html#" class="link">session.save_handler</a>            | "files"    | PHP\_INI\_ALL   | Supported since memcache 2.1.2  |
| <a href="/session/setup.html#" class="link">session.save_path</a>               | ""         | PHP\_INI\_ALL   | Supported since memcache 2.1.2  |
| <a href="/memcache/setup.html#" class="link">memcache.protocol</a>              | ascii      | \>PHP\_INI\_ALL | Supported since memcache 3.0.0  |
| <a href="/memcache/setup.html#" class="link">memcache.redundancy</a>            | 1          | \>PHP\_INI\_ALL | Supported since memcache 3.0.0  |
| <a href="/memcache/setup.html#" class="link">memcache.session_redundancy</a>    | 2          | \>PHP\_INI\_ALL | Supported since memcache 3.0.0  |
| <a href="/memcache/setup.html#" class="link">memcache.compress_threshold</a>    | 20000      | \>PHP\_INI\_ALL | Supported since memcache 3.0.3  |
| <a href="/memcache/setup.html#" class="link">memcache.lock_timeout</a>          | 15         | \>PHP\_INI\_ALL | Supported since memcache 3.0.4  |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`memcache.allow_failover` <span class="type">boolean</span>  
是否在发生错误时（对用户）透明的转移到其他服务器。

`memcache.max_failover_attempts` <span class="type">integer</span>  
定义在写入和获取数据时最多尝试的服务器次数（即：故障转移最大尝试数），仅和
memcache.allow\_failover结合使用。

`memcache.chunk_size` <span class="type">integer</span>  
数据传输块大小，这个值越小网络I/O次数越多，如果发现莫名的速度降低，
可以尝试将此值调至32768。

`memcache.default_port` <span class="type">string</span>  
在尝试连接memcache的时候如果没有单独指定端口默认使用的TCP端口号。

`memcache.hash_strategy` <span class="type">string</span>  
控制key到服务器的映射（分布式）策略。值
*consistent*允许服务器增减而不会（大量）导致健的重新映射
（译注：参见http://tech.idv2.com/2008/07/24/memcached-004/），设置为
*standard*则使用余数方式进行key的映射。

`memcache.hash_function` <span class="type">string</span>  
控制在key-server映射时使用哪个hash函数*crc32*
标明使用标准CRC32进行hash，*fnv*则说明使用FNV-1a。

`session.save_handler` <span class="type">string</span>  
当值为*memcache*时标记使用memcache作为session处理器。

`session.save_path` <span class="type">string</span>  
定义一个逗号分割的用于session存储的服务器url列表，例如：
*"tcp://host1:11211, tcp://host2:11211"*.

每个url可以包含参数，这些参数于方法<span
class="function">Memcache::addServer</span>的参数相同。比如：
*"tcp://host1:11211?persistent=1&weight=1&timeout=1&retry\_interval=15"*

`memcache.protocol` <span class="type">string</span>  

`memcache.redundancy` <span class="type">integer</span>  

`memcache.session_redundancy` <span class="type">integer</span>  

`memcache.compress_threshold` <span class="type">integer</span>  

`memcache.lock_timeout` <span class="type">integer</span>  

资源类型
--------

在memcache 模块中只有一个资源类型 -
它就是到一个缓存服务器连接的链接标识符。
