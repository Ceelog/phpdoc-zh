安装／配置
==========

**目录**

-   [需求](/memcached/setup.html#需求)
-   [安装](/memcached/setup.html#安装)
-   [运行时配置](/memcached/setup.html#运行时配置)
-   [资源类型](/memcached/setup.html#资源类型)

需求
----

这个扩展需要<a href="http://libmemcached.org/libMemcached.html" class="link external">» libmemcached</a>客户端库（版本大于等于
1.0.0）。链接memcached服务器时使用SASL认证，需要libmemcached
必须开启SASL选项。

Memcached从0.2.0开始，要求PHP版本大于等于5.2.0。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/memcached" class="link external">» https://pecl.php.net/package/memcached</a>.

如果libmemcached被安装在一个非标准路径，使用**--with-libmemcached-dir=DIR**
来指定路径，DIR就是libmemcached安装时的prefix参数。这个路径需要包含文件`include/libmemcached/memcached.h`。

如果要支持压缩就需要zlib。对于非标准安装的zlib库，使用**--with-zlib-dir=DIR**
来指定zlib安装路径，DIR就是zib安装时的prefix参数。

session处理器的支持默认是开启的。如果要关闭它，使用选项**--disable-memcached-session**。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                                    | 默认           | 可修改范围       | 更新日志 |
|-----------------------------------------------------------------------------------------|----------------|------------------|----------|
| <a href="/memcached/setup.html#" class="link">memcached.sess_locking</a>                | 1              | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_consistent_hash</a>        | 0              | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_binary</a>                 | 0              | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_lock_wait</a>              | 150000         | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_prefix</a>                 | memc.sess.key. | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_number_of_replicas</a>     | 0              | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_randomize_replica_read</a> | 0              | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.sess_remove_failed</a>          | 0              | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.compression_type</a>            | fastlz         | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.compression_factor</a>          | 1.3            | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.compression_threshold</a>       | 2000           | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.serializer</a>                  | php            | PHP\_INI\_ALL    |          |
| <a href="/memcached/setup.html#" class="link">memcached.use_sasl</a>                    | 0              | PHP\_INI\_SYSTEM |          |

这是配置指令的简短说明。

`memcached.sess_locking` <span class="type">integer</span>  
开启session支持。有效值: On, Off, 默认值 On.

`memcached.sess_consistent_hash` <span class="type">integer</span>  
Memcached
是否使用一致性哈希保存session。如果为On，session数据保存则使用一致性哈希模式。
使用一致性哈希，可以保证你在增加或删除memcached服务器节点的时候不会导致session大规模的失效。
默认此项是关闭的。

`memcached.sess_binary` <span class="type">integer</span>  
Memcached session是否使用二进制模式。如果Libmemcached
开启二进制模式。默认值是 Off.

`memcached.sess_lock_wait` <span class="type">integer</span>  
Session
自旋锁等待时间（微秒）。请小心设置此值。值的类型是整数，当此值被设置为0的时候，lock
wait的时间将会使用系统默认值，Memcached扩展中默认值是150000。

`memcached.sess_prefix` <span class="type">string</span>  
设置memcached session
key的前缀。session前缀最长为219字节长的字符串。默认值是“memc.sess.key.”。

`memcached.sess_number_of_replicas` <span class="type">integer</span>  
使用memcached写session多少个副本。

`memcached.sess_randomize_replica_read` <span class="type">integer</span>  
Memcached session 是否随机复制读。默认值0

`memcached.sess_remove_failed` <span class="type">integer</span>  
是否允许自动剔除出故障的memcached服务器。默认值0

`memcached.compression_type` <span class="type">string</span>  
设置memcached的压缩类型，允许的值为fastlz,
zlib。默认值是fastlz（快速无损压缩，性能不错）。

`memcached.compression_factor` <span class="type">float</span>  
压缩因子. 保存时压缩因子超过设置的极限才会将数据压缩存储。存储压缩条件：
plain\_len \> comp\_len \* factor。默认是1.3 （节省23%的空间）。

`memcached.compression_threshold` <span class="type">integer</span>  
压缩阈值。不压缩的序列化值低于此阈值。默认值是2000字节。

`memcached.serializer` <span class="type">string</span>  
设置缓存对象的默认序列化程序。有效值： php, igbinary, json, json\_array.

json  
标准的PHP
JSON编码。此序列化程序快速而且是压缩后的数据，但是处理UTF-8编码数据时会不完全实现序列化。请查看JSON扩展。

json\_array  
json序列化，但是反序列化的时候返回数组。

php  
PHP标准序列化

igbinary  
二进制序列化

如果二进制序列化可用，则优先使用二进制序列化，否则使用php标准序列化。

`memcached.use_sasl` <span class="type">integer</span>  
链接memcached服务器时启用SASL认证。有效值On, Off。默认值是Off。

资源类型
--------

此扩展没有定义资源类型。
