MongoDB 驱动（旧版）
====================

**目录**

-   [安装／配置](/book/mongo.html#安装／配置)
    -   [需求](/book/mongo.html#需求)
    -   [安装](/book/mongo.html#安装)
    -   [运行时配置](/book/mongo.html#运行时配置)
-   [预定义常量](/book/mongo.html#预定义常量)
-   [手册](/book/mongo.html#手册)
    -   [教程](/book/mongo.html#教程)
    -   [读取首选项](/book/mongo.html#读取首选项)
    -   [Write Concerns](/book/mongo.html#Write%20Concerns)
    -   [SQL 到 Mongo
        的对应表](/book/mongo.html#SQL%20到%20Mongo%20的对应表)
    -   [链接服务器](/book/mongo.html#链接服务器)
    -   [Stream Context
        Options](/book/mongo.html#Stream%20Context%20Options)
    -   [Writes](/book/mongo.html#Writes)
    -   [Querying](/book/mongo.html#Querying)
    -   [Updates](/book/mongo.html#Updates)
    -   [Security](/book/mongo.html#Security)
    -   [故障排除](/book/mongo.html#故障排除)
    -   [Running the Driver's
        Tests](/book/mongo.html#Running%20the%20Driver's%20Tests)
-   [核心类](/book/mongo.html#核心类)
    -   [MongoClient](/book/mongo.html#MongoClient) — MongoClient 类
    -   [MongoDB](/book/mongo.html#MongoDB) — MongoDB 类
    -   [MongoCollection](/book/mongo.html#MongoCollection) — The
        MongoCollection class
    -   [MongoCursor](/book/mongo.html#MongoCursor) — The MongoCursor
        class
    -   [MongoCursorInterface](/book/mongo.html#MongoCursorInterface) —
        The MongoCursorInterface interface
    -   [MongoCommandCursor](/book/mongo.html#MongoCommandCursor) — The
        MongoCommandCursor class
-   [Types](/book/mongo.html#Types)
    -   [MongoId](/book/mongo.html#MongoId) — MongoId 类
    -   [MongoCode](/book/mongo.html#MongoCode) — The MongoCode class
    -   [MongoDate](/book/mongo.html#MongoDate) — The MongoDate class
    -   [MongoRegex](/book/mongo.html#MongoRegex) — MongoRegex 类
    -   [MongoBinData](/book/mongo.html#MongoBinData) — The MongoBinData
        class
    -   [MongoInt32](/book/mongo.html#MongoInt32) — MongoInt32 类
    -   [MongoInt64](/book/mongo.html#MongoInt64) — MongoInt64 类
    -   [MongoDBRef](/book/mongo.html#MongoDBRef) — MongoDBRef 类
    -   [MongoMinKey](/book/mongo.html#MongoMinKey) — The MongoMinKey
        class
    -   [MongoMaxKey](/book/mongo.html#MongoMaxKey) — The MongoMaxKey
        class
    -   [MongoTimestamp](/book/mongo.html#MongoTimestamp) —
        MongoTimestamp 类
-   [GridFS Classes](/book/mongo.html#GridFS%20Classes)
    -   [MongoGridFS](/book/mongo.html#MongoGridFS) — The MongoGridFS
        class
    -   [MongoGridFSFile](/book/mongo.html#MongoGridFSFile) — The
        MongoGridFSFile class
    -   [MongoGridFSCursor](/book/mongo.html#MongoGridFSCursor) — The
        MongoGridFSCursor class
-   [Miscellaneous](/book/mongo.html#Miscellaneous)
    -   [MongoLog](/book/mongo.html#MongoLog) — The MongoLog class
    -   [MongoPool](/book/mongo.html#MongoPool) — The MongoPool class
    -   [Mongo](/book/mongo.html#Mongo) — The Mongo class \[deprecated\]
-   [Mongo 函数](/book/mongo.html#Mongo%20函数)
    -   [bson\_decode](/book/mongo.html#bson_decode) — 反序列化一个 BSON
        对象为 PHP 数组
    -   [bson\_encode](/book/mongo.html#bson_encode) — 序列化一个 PHP
        变量为 BSON 字符串
-   [Exceptions](/book/mongo.html#Exceptions)
    -   [MongoException](/book/mongo.html#MongoException) — The
        MongoException class
    -   [MongoResultException](/book/mongo.html#MongoResultException) —
        MongoResultException 类
    -   [MongoCursorException](/book/mongo.html#MongoCursorException) —
        The MongoCursorException class
    -   [MongoCursorTimeoutException](/book/mongo.html#MongoCursorTimeoutException)
        — The MongoCursorTimeoutException class
    -   [MongoConnectionException](/book/mongo.html#MongoConnectionException)
        — The MongoConnectionException class
    -   [MongoGridFSException](/book/mongo.html#MongoGridFSException) —
        The MongoGridFSException class
    -   [MongoDuplicateKeyException](/book/mongo.html#MongoDuplicateKeyException)
        — The MongoDuplicateKeyException class
    -   [MongoProtocolException](/book/mongo.html#MongoProtocolException)
        — The MongoProtocolException class
    -   [MongoExecutionTimeoutException](/book/mongo.html#MongoExecutionTimeoutException)
        — The MongoExecutionTimeoutException class
    -   [MongoWriteConcernException](/book/mongo.html#MongoWriteConcernException)
        — The MongoWriteConcernException class
-   [更新日志](/book/mongo.html#更新日志)

安装／配置
==========

**目录**

-   [需求](/book/mongo.html#需求)
-   [安装](/book/mongo.html#安装)
-   [运行时配置](/book/mongo.html#运行时配置)

**Warning**

This extension is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used.

需求
----

构建此扩展不需要其他扩展。

安装
----

**Warning**

This extension is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used.

MongoDB 的 PHP 驱动程序可以工作在几乎任何系统上：Windows、Mac OS X、Unix
和 Linux；大端或小端字节序（little/big-endian）；32位和64位的机器；PHP
5.3-5.6(1.6之前的版本同时支持 PHP5.2)。

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

-   <a href="/book/mongo.html#手动安装" class="xref"></a>
-   <a href="/book/mongo.html#在%20*NIX%20上安装" class="xref"></a>
-   <a href="/book/mongo.html#在%20Windows%20上安装" class="xref"></a>
-   <a href="/book/mongo.html#OS%20X" class="xref"></a>
-   <a href="/book/mongo.html#Gentoo" class="xref"></a>
-   <a href="/book/mongo.html#Red%20Hat" class="xref"></a>
-   <a href="/book/mongo.html#第三方安装说明" class="xref"></a>

手动安装
--------

驱动开发人员和对最新 bug 修复感兴趣的人，可以从
<a href="https://github.com/mongodb/mongo-php-driver-legacy" class="link external">» Github</a>
上获取最新源码来编译驱动。 前往 Github 并点击 "download"
按钮。然后运行：

``` shell
$ tar zxvf mongodb-mongodb-php-driver-<commit_id>.tar.gz
$ cd mongodb-mongodb-php-driver-<commit_id>
$ phpize
$ ./configure
$ make all
$ sudo make install
```

并按以下说明修改 php.ini：

-   确保 *extension\_dir* 变量指向了 *mongo.so* 的位置。
    编译时会显示安装 PHP 驱动的位置，比如输出：

    ``` txt
    Installing '/usr/lib/php/extensions/no-debug-non-zts-20060613/mongo.so'
    ```

    确保和运行的 PHP 是同一个扩展目录：

    ``` shell
    $ php -i | grep extension_dir
      extension_dir => /usr/lib/php/extensions/no-debug-non-zts-20060613 =>
                       /usr/lib/php/extensions/no-debug-non-zts-20060613
    ```

    如果不一致，则需要修改 php.ini 里的 *extension\_dir*，或者把
    *mongo.so* 移过去。

-   要在 PHP 启动的时候加载这个扩展，添加一行：

    ``` ini
    extension=mongo.so
    ```

在 \*NIX 上安装
---------------

执行:

``` shell
$ sudo pecl install mongo
```

将以下内容添加到 php.ini 文件:

``` ini
extension=mongo.so
```

如果 pecl 运行时超出了内存限制，请确认在 php.ini 中的 memory\_limit
的设置至少有 128MB。

在 Windows 上安装
-----------------

针对不同线程安全、VC版本的 PHP 发行版，可从
<a href="https://pecl.php.net/package/mongo" class="link external">» PECL</a>
获取到预编译的二进制文件。 解压，并把 php\_mongo.dll 放到 PHP
扩展目录（默认是 “ext”）。

将以下内容添加到 php.ini 文件:

``` ini
extension=php_mongo.dll
```

> **Note**: **为 Windows 用户添加额外的依赖 DLL**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `libsasl.dll`

OS X
----

大部分情况下，从 pecl 安装最简单：

``` shell
$ sudo pecl install mongo
```

如果用的是
<a href="https://github.com/Homebrew/brew" class="link external">» Homebrew</a>，PHP
包含了驱动安装的方案。比如，安装 PHP 5.6 的驱动，可以使用以下命令：

``` shell
$ brew install php56-mongo
```

如果使用的是
<a href="https://www.apachefriends.org/" class="link external">» XAMPP</a>，请注意它有自己的
pecl 二进制文件和 php.ini 配置。 你可以通过以下命令安装驱动：

``` shell
$ sudo /Applications/XAMPP/xamppfiles/bin/pecl install mongo
```

> **Note**: **在 OS X 上编译时的 Xcode 依赖**  
>
> 在 OS X 上编译驱动需要 Xcode 开发工具，可以通过
> `xcode-select --install` 安装。 如果命令无效，也许应该先安装
> <a href="https://developer.apple.com/downloads/index.action?name=Command%20Line%20Tools" class="link external">» Command Line Tools</a>
> 包。

Gentoo
------

Gentoo 有一个 PHP 驱动的包，叫做
dev-php/pecl-mongo，可以通过以下命令安装：

``` shell
$ sudo emerge -va dev-php5/mongo
```

如果你使用了 PECL，你可能得到 libtool 版本不正确的错误。
从源码编译，你需要运行 aclocal 和 autoconf。

``` shell
$ phpize && aclocal && autoconf && ./configure && make && make install
```

Red Hat
-------

同时包括 Fedora 和 CentOS。

这些系统上默认的 Apache
设置禁止请求产生网络连接，意味着当连接到数据库，驱动会得到一个
"Permission denied" 错误。当遇到这个问题，可以试试运行：

``` shell
$ /usr/sbin/setsebool -P httpd_can_network_connect 1
```

然后重启 Apache。（在 SELinux 下也会产生这个问题。）

第三方安装说明
--------------

很多人撰写了安装 PHP 驱动的极好教程。

-   <a href="http://justinhileman.info/article/reinstalling-php-on-mac-os-x/" class="link external">»  在 Mac OS X 上安装或重装 PHP</a>

    Justin Hileman 撰写的文章详细描述了在 OS X 上使用 Homebrew 安装 PHP
    和额外的扩展（extension）。 此文补充了早些时候此页上用 Homebrew
    安装驱动的说明。

-   <a href="https://www.vimeo.com/8005503" class="link external">»  Ubuntu 9.10 / Apache 2.2 下，附带 Xdebug, MongoDB 和 Lithium 的 PHP 5.3.1。</a>

    Jon Adams 的视频录像演示了如何在 Ubuntu 9.1 的 Apache 下快速设置运行
    PHP 5.3.1，Xdebug 和 MongoDB。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                  | 默认        | 可修改范围    | 更新日志                                                |
|-----------------------------------------------------------------------|-------------|---------------|---------------------------------------------------------|
| <a href="/book/mongo.html#" class="link">mongo.allow_empty_keys</a>   | 0           | PHP\_INI\_ALL |                                                         |
| <a href="/book/mongo.html#" class="link">mongo.allow_persistent</a>   | 1           | PHP\_INI\_ALL | Removed in 1.2.0                                        |
| <a href="/book/mongo.html#" class="link">mongo.chunk_size</a>         | 262144      | PHP\_INI\_ALL |                                                         |
| <a href="/book/mongo.html#" class="link">mongo.cmd</a>                | "$"         | PHP\_INI\_ALL |                                                         |
| <a href="/book/mongo.html#" class="link">mongo.default_host</a>       | "localhost" | PHP\_INI\_ALL |                                                         |
| <a href="/book/mongo.html#" class="link">mongo.default_port</a>       | 27017       | PHP\_INI\_ALL |                                                         |
| <a href="/book/mongo.html#" class="link">mongo.is_master_interval</a> | 15          | PHP\_INI\_ALL | Added in 1.2.10, before 1.3.0 the default value was 60. |
| <a href="/book/mongo.html#" class="link">mongo.long_as_object</a>     | 0           | PHP\_INI\_ALL |                                                         |
| <a href="/book/mongo.html#" class="link">mongo.native_long</a>        | 1           | PHP\_INI\_ALL | Before 1.5.0, the default value was 0.                  |
| <a href="/book/mongo.html#" class="link">mongo.ping_interval</a>      | 5           | PHP\_INI\_ALL | Added in 1.2.10                                         |
| <a href="/book/mongo.html#" class="link">mongo.utf8</a>               | 1           | PHP\_INI\_ALL |                                                         |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`mongo.allow_empty_keys` <span class="type">int</span>  
Added in version 1.0.11.

If empty strings ("") should be allowed as key names. By default, the
driver will throw an exception if you attempt to pass the empty string
as a key to the database. It is extremely easy to do this inavertently
by using double quotes with $-operators, so it is recommended that you
leave this setting as default. However, if you need to save keys that
are empty strings, you can set this option to true and the driver will
allow you to pass empty strings to the database.

`mongo.allow_persistent` <span class="type">int</span>  
If persistent connections are allowed. (Removed in 1.2.0 - all
connections are now persistent).

`mongo.chunk_size` <span class="type">int</span>  
The number of bytes-per-chunk. Used in divvying up GridFS files. This
number must be at least 100 less than 4 megabytes (max: 4194204) and it
is recommended that it be less than that.

`mongo.cmd` <span class="type">string</span>  
A character to be used in place of $ in modifiers and comparisons.

As it is easy to forget to escape the "$", you can also choose your own
special character to use instead of '$'. Choose a character that will
not occur in your key names, e.g. ":":

``` ini
mongo.cmd = ":"
```

Then, to do a comparison, for example:

``` php
<?php

$query = array( "i" => array( ":gt" => 20, ":lte" => 30 ) );

?>
```

You can also change it in your code using *ini\_set("mongo.cmd", ":")*.
Of course, you can also just use single quotes or backslash-escape the
$.

`mongo.default_host` <span class="type">string</span>  
Default hostname when nothing is passed to the constructor.

`mongo.default_port` <span class="type">string</span>  
The default TCP port number to use when connecting to the database
server if no other port is specified. The database's default is *27017*.

`mongo.is_master_interval` <span class="type">int</span>  
Added in version 1.2.10.

For replicaset connections: The minimum interval with which the driver
will send "isMaster" requests to the MongoDB server. If the value is
lower, there will be more requests, but the driver finds faster whether
the topology of the replicaset has been changed.

`mongo.long_as_object` <span class="type">int</span>  
Return a BSON\_LONG as an instance of <span
class="classname">MongoInt64</span> (instead of a primitive type).

`mongo.native_long` <span class="type">int</span>  
*The default behavior for this has been changed to **`TRUE`** in 1.5.0,
so make sure to set this variable to the value you want (probably
**`TRUE`**) so that the driver's behavior doesn't suddenly change when
you upgrade.*

On 64-bit platforms, the *mongo.native\_long* setting allows for 64-bit
integers to be stored in MongoDB. If it is not set, only 32-bits of the
integer will be saved. The MongoDB data type that is used in this case
is the BSON LONG, instead of the BSON INT that is used if this setting
is turned off.

The setting also changes the way how BSON LONGs behave when they are
read back from MongoDB. Without *mongo.native\_long* enabled, the driver
would convert every BSON LONG to a PHP double which can result in a loss
of precision.

On 32-bit platforms, the *mongo.native\_long* setting changes nothing
for storing integers in MongoDB: the integer is stored as a BSON INT as
before. However, when the setting is enabled and a BSON LONG is read
from MongoDB a <span class="classname">MongoCursorException</span> is
thrown alerting you that the data could not be read back without losing
precision.

On 32-bit systems especially, it is recommended that you combine this
with enabling *mongo.long\_as\_object*.

`mongo.ping_interval` <span class="type">int</span>  
Added in version 1.2.10.

For replicaset connections: The minimum interval with which the driver
will send "ping" requests to the MongoDB server. If the value is lower,
there will be more pings, but the driver finds faster whether a node is
no longer reachable from the replicaset.

`mongo.utf8` <span class="type">int</span>  
If an exception should be thrown for non-UTF8 strings. Until version
1.0.4, the PHP driver would ignore non-UTF8 strings, even though you're
not supposed to insert them. As of 1.0.4, the driver throws a <span
class="classname">MongoException</span>. To ease the transition for
applications that insert non-UTF8 strings, you can turn this option off
to emulate the old, non-exception-throwning behavior. This option will
be eliminated and exceptions always thrown for non-UTF8 strings starting
with version 1.1.0.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`MONGO_STREAMS`** (<span class="type">integer</span>)  
<span class="simpara"> Alias of **`MONGO_SUPPORTS_STREAMS`** </span>

**`MONGO_SUPPORTS_STREAMS`** (<span class="type">integer</span>)  
<span class="simpara"> 1 when compiled against PHP Streams (default
since 1.4.0). </span>

**`MONGO_SUPPORTS_SSL`** (<span class="type">integer</span>)  
<span class="simpara"> 1 when
<a href="/book/openssl.html" class="xref">OpenSSL</a> is enabled and
available. </span>

**`MONGO_SUPPORTS_AUTH_MECHANISM_MONGODB_CR`** (<span class="type">integer</span>)  
<span class="simpara"> 1 when MongoDB-Challenge/Reponse authentication
is compiled in. </span>

**`MONGO_SUPPORTS_AUTH_MECHANISM_MONGODB_X509`** (<span class="type">integer</span>)  
<span class="simpara"> 1 when x.509 authentication is compiled in.
</span>

**`MONGO_SUPPORTS_AUTH_MECHANISM_GSSAPI`** (<span class="type">integer</span>)  
<span class="simpara"> 1 when GSSAPI authentication is compiled in.
</span>

**`MONGO_SUPPORTS_AUTH_MECHANISM_PLAIN`** (<span class="type">integer</span>)  
<span class="simpara"> 1 when PLAIN authentication is compiled in.
</span>

**`MONGO_STREAM_NOTIFY_TYPE_IO_INIT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_TYPE_LOG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_IO_READ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_IO_WRITE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_IO_PROGRESS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_IO_COMPLETED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_INSERT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_QUERY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_UPDATE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_DELETE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_GETMORE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_KILLCURSOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_BATCHINSERT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_RESPONSE_HEADER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_WRITE_REPLY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_CMD_INSERT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_CMD_UPDATE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_CMD_DELETE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MONGO_STREAM_NOTIFY_LOG_WRITE_BATCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

手册
====

**目录**

-   [教程](/book/mongo.html#教程)
    -   [连接数据库](/book/mongo.html#连接数据库)
    -   [获取数据库实例](/book/mongo.html#获取数据库实例)
    -   [获取集合实例](/book/mongo.html#获取集合实例)
    -   [插入一个文档](/book/mongo.html#插入一个文档)
    -   [使用 MongoCollection::findOne
        方法](/book/mongo.html#使用%20MongoCollection::findOne%20方法)
    -   [添加多个文档](/book/mongo.html#添加多个文档)
    -   [计算文档数量](/book/mongo.html#计算文档数量)
    -   [使用游标获取所有文档](/book/mongo.html#使用游标获取所有文档)
    -   [设置查询条件](/book/mongo.html#设置查询条件)
    -   [获取一个子集](/book/mongo.html#获取一个子集)
    -   [建立索引](/book/mongo.html#建立索引)
-   [读取首选项](/book/mongo.html#读取首选项)
-   [Write Concerns](/book/mongo.html#Write%20Concerns)
-   [SQL 到 Mongo
    的对应表](/book/mongo.html#SQL%20到%20Mongo%20的对应表)
-   [链接服务器](/book/mongo.html#链接服务器)
    -   [认证](/book/mongo.html#认证)
    -   [复制集合](/book/mongo.html#复制集合)
    -   [Sharding](/book/mongo.html#Sharding)
    -   [Unix Domain
        Socket支持](/book/mongo.html#Unix%20Domain%20Socket支持)
    -   [Connection Pooling (version 1.2.0-1.2.12
        \*only\*)](/book/mongo.html#Connection%20Pooling%20(version%201.2.0-1.2.12%20*only*))
    -   [Persistent Connections (version up to 1.1.4
        \*only\*)](/book/mongo.html#Persistent%20Connections%20(version%20up%20to%201.1.4%20*only*))
-   [Stream Context
    Options](/book/mongo.html#Stream%20Context%20Options)
    -   [log\_cmd\_delete](/book/mongo.html#log_cmd_delete) — Callback
        When Deleting Documents
    -   [log\_cmd\_insert](/book/mongo.html#log_cmd_insert) — Callback
        When Inserting Documents
    -   [log\_cmd\_update](/book/mongo.html#log_cmd_update) — Callback
        When Updating Documents
    -   [log\_getmore](/book/mongo.html#log_getmore) — Callback When
        Retrieving Next Cursor Batch
    -   [log\_killcursor](/book/mongo.html#log_killcursor) — Callback
        When Executing KILLCURSOR operations
    -   [log\_reply](/book/mongo.html#log_reply) — Callback When Reading
        the MongoDB reply
    -   [log\_write\_batch](/book/mongo.html#log_write_batch) — Callback
        When Writing Batches
-   [Writes](/book/mongo.html#Writes)
-   [Querying](/book/mongo.html#Querying)
-   [Updates](/book/mongo.html#Updates)
-   [Security](/book/mongo.html#Security)
-   [故障排除](/book/mongo.html#故障排除)
-   [Running the Driver's
    Tests](/book/mongo.html#Running%20the%20Driver's%20Tests)

**Warning**

This extension is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used.

这个手册详细的描述了如何使用 MongoDB，但是它主要覆盖了 PHP
驱动的使用。关于如何设计一种模式、术语的含义以及如何架设数据库服务器，请查看
<a href="https://www.mongodb.com/" class="link external">» MongoDB 文档</a>。

教程
====

**目录**

-   [连接数据库](/book/mongo.html#连接数据库)
-   [获取数据库实例](/book/mongo.html#获取数据库实例)
-   [获取集合实例](/book/mongo.html#获取集合实例)
-   [插入一个文档](/book/mongo.html#插入一个文档)
-   [使用 MongoCollection::findOne
    方法](/book/mongo.html#使用%20MongoCollection::findOne%20方法)
-   [添加多个文档](/book/mongo.html#添加多个文档)
-   [计算文档数量](/book/mongo.html#计算文档数量)
-   [使用游标获取所有文档](/book/mongo.html#使用游标获取所有文档)
-   [设置查询条件](/book/mongo.html#设置查询条件)
-   [获取一个子集](/book/mongo.html#获取一个子集)
-   [建立索引](/book/mongo.html#建立索引)

**Warning**

This extension is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used.

这是官方的 MongoDB PHP 驱动

这是一个示例程序，它包含
连接数据库、插入文档、查询文档、遍历查询结果、断开链接。
实例中的每一步都有更详细的说明（注释）。

``` php
<?php

// 链接服务器
$m = new MongoClient();

// 选择一个数据库
$db = $m->comedy;

// 选择一个集合（ Mongo 的“集合”相当于关系型数据库的“表”）
$collection = $db->cartoons;

// 插入一个文档（译注：“文档”相当于关系型数据库的“行”）
$document = array( "title" => "Calvin and Hobbes", "author" => "Bill Watterson" );
$collection->insert($document);

// 添加另一个文档，它的结构与之前的不同
$document = array( "title" => "XKCD", "online" => true );
$collection->insert($document);

// 查询集合中的所有文档
$cursor = $collection->find();

// 遍历查询结果
foreach ($cursor as $document) {
    echo $document["title"] . "\n";
}

?>
```

以上例程会输出：

    Calvin and Hobbes
    XKCD

连接数据库
----------

使用下面列出的其中一种方法链接：

``` php
<?php
$connection = new MongoClient(); // 连接到 localhost:27017
$connection = new MongoClient( "mongodb://example.com" ); // 连接到远程服务器 （使用默认端口： 27017）
$connection = new MongoClient( "mongodb://example.com:65432" ); // 链接到远程服务器，使用自定义的端口
?>
```

你并不必须手动从服务器断开连接。这个驱动使用了持久连接，并会在下次试图链接到同一服务器时重用它。

参见
----

<a href="/book/mongo.html#链接服务器" class="link">链接</a>
中的相关章节。来获得更多链接方式的信息。

<span class="classname">MongoClient</span> 类和 <span
class="function">MongoClient::\_\_construct</span>
的文档中有对所有链接方式的详细说明， 并且带有一些例子。

获取数据库实例
--------------

要选择数据库，使用：

``` php
<?php
$connection = new MongoClient();
$db = $connection->dbname;
?>
```

这个数据库不需要提前建好，当你使用它的时候，就会自动建立。

要小心的是，你可能不小心建立了一个新的数据库，然后产生奇怪的错误。
（在下面的例子中，第二次使用“同一个”数据库时 *name* 被错误的拼写成
*anme*）

``` php
<?php
$connection = new MongoClient();

$db = $connection->mybiglongdbname;
// do some stuff

$db = $connection->mybiglongdbanme;
// now connected to a different database! 注意此时选择了另一个数据库！
?>
```

参见
----

<span class="classname">MongoDB</span>
类的文档中有对数据库对象的详细说明。

获取集合实例
------------

获取一个集合的语法与获取数据库时相同：

``` php
<?php
$connection = new MongoClient();
$db = $connection->baz;

// select a collection:
$collection = $db->foobar;

// or, directly selecting a database and collection:
$collection = $connection->baz->foobar;
?>
```

一个集合相当于一张表。（如果你对关系型数据库比较熟悉）

参见
----

<span class="classname">MongoCollection</span>
类的文档中有对集合对象的详细说明。

插入一个文档
------------

关联数组是能插入集合的最基本结构。 一般的“文档”结构可能是这样：

``` php
<?php
$doc = array(
    "name" => "MongoDB",
    "type" => "database",
    "count" => 1,
    "info" => (object)array( "x" => 203, "y" => 102),
    "versions" => array("0.9.7", "0.9.8", "0.9.9")
);
?>
```

注意：你可以嵌套数组、对象。驱动会把关联数组保存为
js对象，从0开始的连续数字下标数组保存为
js数组，不从0开始或有间断的（如0,1,4,5）数组保存为 js对象。
译注：即：只有从0开始的连续数字下标数组保存为数组，其他复杂类型均为对象。

要插入这个文档，使用 <span
class="function">MongoCollection::insert</span> 方法：

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

$collection->insert( $doc );
?>
```

参见
----

<span class="function">MongoCollection::insert</span>
方法的文档中有对插入数据的详细说明。

使用 <span class="function">MongoCollection::findOne</span> 方法
----------------------------------------------------------------

要查看我们上一步插入到数据库的文档，可以简单的使用 <span
class="function">MongoCollection::findOne</span>
方法从即合理获得一个简单的文档。
这个方法在只想查询一个结果的时候很有用。

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

$document = $collection->findOne();
var_dump( $document );
?>
```

以上例程会输出：

    array(6) {
      ["_id"]=>
      object(MongoId)#8 (1) {
        ["$id"]=>
        string(24) "4e2995576803fab768000000"
      }
      ["name"]=>
      string(7) "MongoDB"
      ["type"]=>
      string(8) "database"
      ["count"]=>
      int(1)
      ["info"]=>
      array(2) {
        ["x"]=>
        int(203)
        ["y"]=>
        int(102)
      }
      ["versions"]=>
      array(3) {
        [0]=>
        string(5) "0.9.7"
        [1]=>
        string(5) "0.9.8"
        [2]=>
        string(5) "0.9.9"
      }
    }

注意：有一个 *\_id* 字段被自动添加到你的文档中了。 *\_id*
字段就是集合的“主键”。
如果插入文档的时候你没有手动指定，驱动就会自动帮你添加一个。

如果你所插入的文档定义了 *\_id* 字段，那么它在集合中必须是唯一的。
这是一个例子：

``` php
<?php
$connection = new MongoClient();
$db = $connection->database;

$db->foo->insert(array("_id" => 1));
// this will throw an exception
$db->foo->insert(array("_id" => 1));

// this is fine, as it is a different collection
$db->bar->insert(array("_id" => 1));
?>
```

默认设置时，驱动会在服务器通过了写入请求后返回（译注：“通过”即如果不发生崩溃等情况，待插入的文档就一定会在随后被写入，这并不意味着数据已经写入磁盘）。你可以通过将第二个参数设为
*array("w" =\> 0)*
来改变默认行为。此时你的插入请求会立即返回，并且不会抛出 *\_id*
重复的异常。

参见
----

<span class="function">MongoCollection::findOne</span>
方法的文档中有对查询的详细说明。

唯一ID的信息查看 <span class="classname">MongoId</span>

<a href="/book/mongo.html#Writes" class="link">写入</a>
部分更详细的说明了写操作,
<a href="/book/mongo.html#Write%20Concerns" class="xref"></a>
章节深入解释了一些写操作的选项。

添加多个文档
------------

为了观察更多查询时值得关注的事情，我们来插入很多相似的文档到同一个集合里。这些文档的结构简单的类似于：
*array( "i" =\> <span class="replaceable">value</span> );* 。
通过一个循环，我们可以快速插入这些文档：

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

for ( $i = 0; $i < 100; $i++ )
{
    $collection->insert( array( 'i' => $i, "field{$i}" => $i * 2 ) );
}
?>
```

注意：我们可以把结构（键名）不同的数组插入同一个集合。这正是我们说
MongoDB 是一个“无结构”数据库的原因。在上面的例子中，每个文档都有一个 *i*
字段，但同时也有一个变化的 *field* + *$i* 字段。

计算文档数量
------------

现在我们的集合中有101个文档（100个循环插入的，加上一开始的一个），我们可以通过
<span class="function">MongoCollection::count</span> 方法检查它。

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

echo $collection->count();
?>
```

这会输出 101 。

使用游标获取所有文档
--------------------

要获得集合中的所有文档，我们需要 <span
class="function">MongoCollection::find</span> 方法。 find() 方法返回一个
<span class="classname">MongoCursor</span>
对象，允许我们遍历整个结果集合来读取文档。要查询所有的文档并显示它们，使用：

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

$cursor = $collection->find();
foreach ( $cursor as $id => $value )
{
    echo "$id: ";
    var_dump( $value );
}
?>
```

这样会输出整个集合中的101个文档。 *$id* 是集合的 *\_id*
字段（被转换成字符串）， *$value* 是文档本身。

参见
----

<span class="function">MongoCollection::find</span>
方法的文档中有关于查询的详细信息。

设置查询条件
------------

我们可以建立一个查询，然后传递给 <span
class="function">MongoCollection::find</span> 方法来查询集合的一个子集。
例如：我们要查询 *"i"* 字段等于 *71* 的文档，我们可以使用：

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

$query = array( 'i' => 71 );
$cursor = $collection->find( $query );

while ( $cursor->hasNext() )
{
    var_dump( $cursor->getNext() );
}
?>
```

以上例程会输出：

    array(2) {
      ["_id"]=>
      object(MongoId)#6 (0) {
      }
      ["i"]=>
      int(71)
      ["_ns"]=>
      "testCollection"
    }

获取一个子集
------------

我们可以用查询条件从集合中获得多个文档。 例如：想要获得 *"i"* \> *50*
的文档，我们需要：

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

$query = array( "i" => array( '$gt' => 50 ) ); //note the single quotes around '$gt'
$cursor = $collection->find( $query );

while ( $cursor->hasNext() )
{
    var_dump( $cursor->getNext() );
}
?>
```

将会显示 *"i"* \> *50* 的文档。也可以获得一个范围内的文档，比如 *20 \< i
\<= 30*：

    <?php
    $connection = new MongoClient();
    $collection = $connection->database->collectionName;

    $query = array( 'i' => array( '$gt' => 20, "\$lte" => 30 ) );
    $cursor = $collection->find( $query );

    while ( $cursor->hasNext() )
    {
        var_dump( $cursor->getNext() );
    }
    ?>

要注意美元字符始终都需要转义，或者可以用单引号代替。否则 PHP
会把它解析成对应的变量 `$gt`。

建立索引
--------

MongoDB 支持索引，并且很容易给集合添加索引。你需要指定字段名和排序方向：
升序（1）或降序（-1）。例如：

``` php
<?php
$connection = new MongoClient();
$collection = $connection->database->collectionName;

$collection->ensureIndex( array( "i" => 1 ) );  // create index on "i"
$collection->ensureIndex( array( "i" => -1, "j" => 1 ) );  // index on "i" descending, "j" ascending
?>
```

当你的数据量变得越来越大，创建索引对读取性能有巨大的提升。如果你不了解索引，可以参考
<span class="function">MongoCollection::ensureIndex</span> 文档和
MongoDB 的
<a href="https://docs.mongodb.com/manual/indexes/" class="link external">» MongoDB indexing documentation</a>。

读取首选项
==========

MongoDB 2.2 和 1.3.0 版本的驱动增加了支持
<a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» 读取首选项</a>,
允许你指定怎样查询MongoDB复制集.
读取首选项可能被指定在连接上，或者库上，或者是集合上.
首选项规定默认要自上而下的继承 (举个例子 <span
class="classname">MongoCollection</span> 将继承相应的 <span
class="classname">MongoDB</span> 实例的读取首选项).

读取首选项是模式和标签集相结合的. 模式决定mongod的优先权, 而
<a href="https://docs.mongodb.com/manual/tutorial/configure-replica-set-tag-sets/" class="link external">» 标签集</a>
为mongod实例合格指定了标准。只有那些ping附近的mongd实例时间在15毫秒内的Mongod实例是合格的。

**Warning**

所有的读取首选项都可能返回从节点比主节点延时的的数据，除非你选择*MongoClient::RP\_PRIMARY*。如果你不使用*MongoClient::RP\_PRIMARY*.模式，请确保你的应用可以容忍过时的数据。

-   *MongoClient::RP\_PRIMARY*

    所有的读操作将使用主节点.
    默认是这样，如果主节点不可用，读操作将产生一个异常。

    这个模式和使用标签集相冲突. 一个标签集指定为
    *MongoClient::RP\_PRIMARY* 将产生一个异常。

-   *MongoClient::RP\_PRIMARY\_PREFERRED*

    在大多数情况下, 读取会操作主节点. 但是，如果主节点不可用,
    故障转移期间, 将从从节点读取数据。

    当读取首选项包含一个标签集, 客户端首先从主节点读取,
    如果可用，去从节点匹配标签. 如果从节点没有匹配到标签,
    读操作将产生一个异常。

    **Warning**
    2.2版本的mongos增加了完全支持读取首选项功能。当连接到mongos实例时,
    *MongoClient::RP\_PRIMARY\_PREFERRED*将发送查询到从节点.

-   *MongoClient::RP\_SECONDARY*

    读操作仅仅发送给从节点. 如果没有从节点可用，将产生一个异常.

    大多数复制集至少有一个从节点,
    但是可能没有可用的从节点。举个例子，有一主节点和一从节点,
    还有一个仲裁节点，但是没有其它从节点了，从节点处于故障转移阶段或者不可用的时候。

    当读取首选项包括了标签集,
    客户端试着找到匹配标签的从节点，直接读一个从节点。如果没有匹配标签的从节点，将导致一个异常

-   *MongoClient::RP\_SECONDARY\_PREFERRED*

    大多数情况下，从从节点读取，在只有主节点的情况下，读取主节点

    当读取首选项包括了标签集,
    客户端试着找到匹配标签的从节点，直接读一个从节点。如果没有匹配标签的从节点，将导致一个异常.

-   *MongoClient::RP\_NEAREST*

    驱动*随机*读取一个ping时间低于15毫秒的节点。使用
    *MongoClient::RP\_NEAREST*
    模式的话，读取可能发生在主节点或者从节点。

    采用这个模式的话，读操作会发生在网络延时小的节点，不考虑读取的数据是过时的还是最新的。

    当读取首选项包括了标签集,
    客户端试着找到匹配标签的节点，直接读一个最近组的随机节点。

    > **Note**:
    >
    > 对复制集的读操作都发生在符合特定读首选项的最近的节点。
    > *MongoClient::RP\_NEAREST*
    > 模式会获取主节点和从节点的状态，找到延时低的节点来读取。

<a href="https://docs.mongodb.com/manual/tutorial/configure-replica-set-tag-sets/" class="link external">» 标签集</a>允许你自定义参数，把读操作指向特定的节点。标签集使得下面两种情况成为可能，读操作指向特定的数据节点或者指定的mongod实例给指定类型的操作使用，例如记录日志或者分析日志。

你可以指定标签集用下面的读取首选项模式：

-   *MongoClient::RP\_PRIMARY\_PREFERRED*

-   *MongoClient::RP\_SECONDARY*

-   *MongoClient::RP\_SECONDARY\_PREFERRED*

-   *MongoClient::RP\_NEAREST*

你不能指定标签集用 *MongoClient::RP\_PRIMARY*
读取首选项模式。只有选择了一个从节点，标签才能用，除非是最近模式。

读取首选项可能指定连接URI给 <span
class="function">MongoClient::\_\_construct</span>,
使用查询串语法或者使用标签集的数组语法传递给核心类的设置方法。

当某个读取首选项使用了查询串， 标签集的
*readPreferenceTags*值应该是逗号分隔开的一串冒号连接的键值对。

> **Note**:
>
> 每一个查询串定义的标签集将使用 *readPreferenceTags* 名称.
> 不像php接收URL查询串的方式，*readPreferenceTags*连续的值相互不覆盖。驱动将按照顺序获得标签集。

**Warning**

如果驱动找不到一个匹配的标签集，读取会失败！
你有责任提供合适的回退，像空的 *readPreferenceTags*
值指定“没有标签集首选项”.

**示例 \#1 查询串语法的读取首选项URI链接**

``` php
<?php
// Prefer the nearest server with no tag preference
$uri  = 'mongodb://rs1.example.com,rs2.example.com/';
$uri .= '?readPreference=nearest';
$m = new MongoClient($uri, array('replicaSet' => 'rs'));

// Pick the nearest server in the "east" data center
$uri  = 'mongodb://rs1.example.com,rs2.example.com/';
$uri .= '?readPreference=nearest';
$uri .= '&readPreferenceTags=dc:east';
$m = new MongoClient($uri, array('replicaSet' => 'rs'));

// Prefer the nearest server in the "east" data center also used for reporting,
// but fall back to a server in the "west" data center
$uri  = 'mongodb://rs1.example.com,rs2.example.com/';
$uri .= '?readPreference=nearest';
$uri .= '&readPreferenceTags=dc:east,use:reporting';
$uri .= '&readPreferenceTags=dc:west';
$m = new MongoClient($uri, array('replicaSet' => 'rs'));

// Prefer the nearest server in the "east" data center, then a server in the
// "west" data center, and finally fall back to no tag set preference
$uri  = 'mongodb://rs1.example.com,rs2.example.com/';
$uri .= '?readPreference=nearest';
$uri .= '&readPreferenceTags=dc:east';
$uri .= '&readPreferenceTags=dc:west';
$uri .= '&readPreferenceTags=';
$m = new MongoClient($uri, array('replicaSet' => 'rs'));
?>
```

**示例 \#2 Setting read preferences with array syntax for tag sets**

``` php
<?php

$m = new MongoClient('mongodb://rs1.example.com,rs2.example.com', array(
    'replicaSet' => 'rs',
));

// Prefer the nearest server with no tag preference
$m->setReadPreference(MongoClient::RP_NEAREST, array());

// Pick the nearest server in the "east" data center
$m->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east'),
));

// Prefer the nearest server in the "east" data center also used for reporting,
// but fall back to a server in the "west" data center
$m->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
));

// Prefer the nearest server in the "east" data center, then a server in the
// "west" data center, and finally fall back to no tag set preference
$m->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east'),
    array('dc' => 'west'),
    array(),
));
?>
```

Write Concerns
==============

MongoDB provides several different ways of selecting how durable a write
to the database should be. These ways are called *Write Concerns* and
span everything from completely ignoring all errors, to specifically
targetting which servers are required to confirm the write before
returning the operation.

When a write (such as with <span
class="methodname">MongoCollection::insert</span>, <span
class="methodname">MongoCollection::update</span>, and <span
class="methodname">MongoCollection::remove</span>) is given a Write
Concern option (*"w"*) the driver will send the query to MongoDB and
piggy back a *getLastError* command (GLE) with the Write Concern option
at the same time. The server only returns when the Write Concern
condition is verified to be fulfilled, or the query times out
(controlled with the *"wtimeout"* option, *10000* milliseconds is the
default).

**Warning**

Even though a *getLastError* command times out the data will most likely
have been written to the primary server and will be replicated to all
the secondaries once they have caught up.

The typical reasons for a timeout to happen is if you specify a Write
Concern which requires confirmation from more servers then you currently
have available.

When using acknowledged writes and the replica set has failed over, the
driver will automatically disconnect from the primary, throw an
exception, and attempt to find a new primary on the next operation (your
application must decide whether or not to retry the operation on the new
primary).

When using unacknowledged writes (w=0) and the replica set has failed
over, there will be no way for the driver to know about the change so it
will continue and silently fail to write.

The default Write Concern for the <span
class="classname">MongoClient</span> is *1*: acknowledge write
operations.

| Write Concern | Meaning                          | Description                                                                                                                   |
|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| w=0           | Unacknowledged                   | A write will not be followed up with a GLE call, and therefore not checked ("fire and forget")                                |
| w=1           | Acknowledged                     | The write will be acknowledged by the server (the primary on replica set configuration)                                       |
| w=N           | Replica Set Acknowledged         | The write will be acknowledged by the primary server, and replicated to *N-1* secondaries.                                    |
| w=majority    | Majority Acknowledged            | The write will be acknowledged by the majority of the replica set (including the primary). This is a special reserved string. |
| w=\<tag set\> | Replica Set Tag Set Acknowledged | The write will be acknowledged by members of the entire tag set                                                               |
| j=true        | Journaled                        | The write will be acknowledged by primary and the journal flushed to disk                                                     |

Each of the methods that causes writes ( <span
class="methodname">MongoCollection::insert</span>, <span
class="methodname">MongoCollection::update</span>, <span
class="methodname">MongoCollection::remove</span>, and <span
class="methodname">MongoCollection::batchInsert</span>) allow an
optional argument to send a set of options to the MongoDB server. With
this option array you can set the WriteConcern as the following example
illustrates:

**示例 \#1 Passing a WriteConcern to a write operation**

``` php
<?php
// Setting w=0 for insert:
$collection->insert($someDoc, array("w" => 0));

// Setting w=majority for update:
$collection->update($someDoc, $someUpdates, array("w" => "majority"));

// Setting w=5 and j=true for remove:
$collection->update($someDoc, array("w" => 5, "j" => true));

// Setting w="AllDCs" for batchInsert:
$collection->update(array($someDoc1, $someDoc2), array("w" => "AllDCs"));
?>
```

Besides setting WriteConcerns per operation as an option argument, it is
also possible to set a default WriteConcern in different ways.

The first way is through the
<a href="" class="link">connection string</a>. The connection string
accepts the *journal*, *w*, and *wTimeoutMS* options:

**示例 \#2 Connection string WriteConcerns**

``` php
<?php
$m = new MongoClient("mongodb://localhost/?journal=true&w=majority&wTimeoutMS=20000");
?>
```

Since driver version 1.5 it is also possible to call <span
class="methodname">MongoDB::setWriteConcern</span> and <span
class="methodname">MongoCollection::setWriteConcern</span> to set a
default WriteConcern for all operations created from that specific <span
class="classname">MongoDB</span> or <span
class="classname">MongoCollection</span> object:

**示例 \#3 MongoDB::setWriteConcern and
MongoCollection::setWriteConcern**

``` php
<?php
$m = new MongoClient("mongodb://localhost/");
$d = $m->demoDb;
$c = $d->demoCollection;

// Set w=3 on the database object with a timeout of 25000ms
$d->setWriteConcern(3, 25000);

// Set w=majority on the collection object without changing the timeout
$c->setWriteConcern("majority");
?>
```

By not requiring the server to acknowledge writes the writes can be
performed extremely quickly, but you don't know whether or not they
actually succeeded. Writes can fail for a number of reasons: if there
are network problems, if a database server goes down, or if the write
was simply invalid (e.g., writing to a system collection; or duplicate
key errors).

While developing, you should always use acknowledged writes (to protect
against inadvertent mistakes, such as syntax errors, invalid operators,
duplicate key errors and so on). In production, unacknowledged writes
can be used for "unimportant" data. Unimportant data varies on
application, but it's generally automatically (instead of user
generated) data, such as click tracking or GPS locations, where you can
get thousands of records per second.

It is strongly recommended that you do an acknowledged write at the end
of series of unacknowledged writes. Doing so will not incur in a too
large performance penalty, but still allow you to catch any errors that
may have occurred.

**示例 \#4 Unacknowledged WriteConcern, followed with Acknowledged
Write**

``` php
<?php
$collection->insert($someDoc, array("w" => 0));
$collection->update($criteria, $newObj, array("w" => 0));
$collection->insert($somethingElse, array("w" => 0));
try {
    $collection->remove($something, array("w" => 1));
} catch(MongoCursorException $e) {
    /* Handle the exception.. */
    /* Here we should issue find() queries on the IDs generated for
    $somethingElse and $someDoc to verify they got written to the database and
    attempt to figureout where in the chain something happened. */
}
?>
```

If the last write throws an exception, you know that there's a problem
with your database.

These type of write operations will make sure that the database has
accepted the write operation before returning success. If the write
failed, it will throw a <span
class="classname">MongoCursorException</span> with an explanation of the
failure. The <span class="classname">MongoClient</span> default
behaviour is to acknowledge the write (w=1).

It is possible to specify how many members of an replica set have to
acknowledge the write (i.e. have it replicated) before the write is
deemed acknowledged and the operation returns.

**示例 \#5 Acknowledged Writes**

``` php
<?php
// Force acknowledgement from the primary only
$collection->insert($doc, array("w" => 1));

// Force acknowledgement from the primary, and one other member of the
// replica set
$collection->insert($doc, array("w" => 2));

// Force acknowledgement from the primary, and six other members of the
// replica set (you probably never should do this):
$collection->insert($doc, array("w" => 7));
?>
```

Keep in mind to select your Write Concern carefully. If you have a
replica set with 5 members, and you select Write Concern of *4* you will
risk the write blocking forever when one member of the replica set goes
down for maintenance or a temporary network outage happens.

**Warning**

Passing in a string value for Write Concern has a specific meaning
(Replica Set Tag Set Acknowledged). Please be careful of *NOT* using
string values for numbers (i.e. *array("w" =\> "1")*) as it will be
treated as a tag set name.

Using the special *majority* Write Concern option is the recommended way
for writes that are required to survive the apocalypse, as it will
ensure the majority of your replica set will have the write and will
therefore be guaranteed to survive all usual suspect outage scenarios.

**示例 \#6 Majority Acknowledged Write**

``` php
<?php
$collection->insert($someDoc, array("w" => "majority"));
?>
```

When connecting to a replica set the default Write Concern is only to
have the primary server acknowledge the write. There is however a 100ms
window until the write gets journaled and flushed to disk. It is
possible to force the write to be journaled before acknowledging the
write by setting the *j* option:

**示例 \#7 Acknowledged and Journaled Write**

Forcing journal flush

``` php
<?php
$options = array(
    "w" => 1,
    "j" => true,
);
try {
    $collection->insert($document, $options);
} catch(MongoCursorException $e) {
    /* handle the exception */
}
?>
```

-   <a href="https://docs.mongodb.com/manual/applications/replication/#replica-set-write-concern" class="link external">» MongoDB WriteConcern docs</a>

| 版本  | 说明                                                                                                                                                                                                                                                    |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | <span class="classname">MongoClient</span> was introduced and defaults to <a href="/book/mongo.html#Acknowledged%20Writes" class="link">acknowledged</a> writes. The deprecated <span class="classname">Mongo</span> defaults to unacknowledged writes. |
| 1.3.0 | The *"safe"* write option has been deprecated and is not available with the new <span class="classname">MongoClient</span> class. Use the *"w"* option instead.                                                                                         |

SQL 到 Mongo 的对应表
=====================

这个列表是 PHP 版本的
<a href="https://docs.mongodb.com/manual/reference/sql-comparison/" class="link external">» SQL to Mongo</a>
对应表（在MongoDB官方手册中有更加通用的版本）。

| SQL查询语句                                        | Mongo查询语句                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| *CREATE TABLE USERS (a Number, b Number)*          | 隐式的创建，或 <span class="function">MongoDB::createCollection</span>.                             |
| *INSERT INTO USERS VALUES(1,1)*                    | *$db-\>users-\>insert(array("a" =\> 1, "b" =\> 1));*                                                |
| *SELECT a,b FROM users*                            | *$db-\>users-\>find(array(), array("a" =\> 1, "b" =\> 1));*                                         |
| *SELECT \* FROM users WHERE age=33*                | *$db-\>users-\>find(array("age" =\> 33));*                                                          |
| *SELECT a,b FROM users WHERE age=33*               | *$db-\>users-\>find(array("age" =\> 33), array("a" =\> 1, "b" =\> 1));*                             |
| *SELECT a,b FROM users WHERE age=33 ORDER BY name* | *$db-\>users-\>find(array("age" =\> 33), array("a" =\> 1, "b" =\> 1))-\>sort(array("name" =\> 1));* |
| *SELECT \* FROM users WHERE age\>33*               | *$db-\>users-\>find(array("age" =\> array('$gt' =\> 33)));*                                         |
| *SELECT \* FROM users WHERE age\<33*               | *$db-\>users-\>find(array("age" =\> array('$lt' =\> 33)));*                                         |
| *SELECT \* FROM users WHERE name LIKE "%Joe%"*     | *$db-\>users-\>find(array("name" =\> new MongoRegex("/Joe/")));*                                    |
| *SELECT \* FROM users WHERE name LIKE "Joe%"*      | *$db-\>users-\>find(array("name" =\> new MongoRegex("/^Joe/")));*                                   |
| *SELECT \* FROM users WHERE age\>33 AND age\<=40*  | *$db-\>users-\>find(array("age" =\> array('$gt' =\> 33, '$lte' =\> 40)));*                          |
| *SELECT \* FROM users ORDER BY name DESC*          | *$db-\>users-\>find()-\>sort(array("name" =\> -1));*                                                |
| *CREATE INDEX myindexname ON users(name)*          | *$db-\>users-\>ensureIndex(array("name" =\> 1));*                                                   |
| *CREATE INDEX myindexname ON users(name,ts DESC)*  | *$db-\>users-\>ensureIndex(array("name" =\> 1, "ts" =\> -1));*                                      |
| *SELECT \* FROM users WHERE a=1 and b='q'*         | *$db-\>users-\>find(array("a" =\> 1, "b" =\> "q"));*                                                |
| *SELECT \* FROM users LIMIT 20, 10*                | *$db-\>users-\>find()-\>limit(10)-\>skip(20);*                                                      |
| *SELECT \* FROM users WHERE a=1 or b=2*            | *$db-\>users-\>find(array('$or' =\> array(array("a" =\> 1), array("b" =\> 2))));*                   |
| *SELECT \* FROM users LIMIT 1*                     | *$db-\>users-\>find()-\>limit(1);*                                                                  |
| *EXPLAIN SELECT \* FROM users WHERE z=3*           | *$db-\>users-\>find(array("z" =\> 3))-\>explain()*                                                  |
| *SELECT DISTINCT last\_name FROM users*            | *$db-\>command(array("distinct" =\> "users", "key" =\> "last\_name"));*                             |
| *SELECT COUNT(\*y) FROM users*                     | *$db-\>users-\>count();*                                                                            |
| *SELECT COUNT(\*y) FROM users where AGE \> 30*     | *$db-\>users-\>find(array("age" =\> array('$gt' =\> 30)))-\>count();*                               |
| *SELECT COUNT(AGE) from users*                     | *$db-\>users-\>find(array("age" =\> array('$exists' =\> true)))-\>count();*                         |
| *UPDATE users SET a=1 WHERE b='q'*                 | *$db-\>users-\>update(array("b" =\> "q"), array('$set' =\> array("a" =\> 1)));*                     |
| *UPDATE users SET a=a+2 WHERE b='q'*               | *$db-\>users-\>update(array("b" =\> "q"), array('$inc' =\> array("a" =\> 2)));*                     |
| *DELETE FROM users WHERE z="abc"*                  | *$db-\>users-\>remove(array("z" =\> "abc"));*                                                       |

链接服务器
==========

**目录**

-   [认证](/book/mongo.html#认证)
-   [复制集合](/book/mongo.html#复制集合)
-   [Sharding](/book/mongo.html#Sharding)
-   [Unix Domain
    Socket支持](/book/mongo.html#Unix%20Domain%20Socket支持)
-   [Connection Pooling (version 1.2.0-1.2.12
    \*only\*)](/book/mongo.html#Connection%20Pooling%20(version%201.2.0-1.2.12%20*only*))
-   [Persistent Connections (version up to 1.1.4
    \*only\*)](/book/mongo.html#Persistent%20Connections%20(version%20up%20to%201.1.4%20*only*))

链接到 mongo 服务器非常简单，只需要 *new
MongoClient*，但是还可以改变更多的选项设置。 <span
class="function">MongoClient::\_\_construct</span>
方法的文档中包括了所有的 API
参数。这个页面给出了一些详细说明，和一些实用的案例。

认证
----

如果 MongoDB 服务器启动时使用了 *--auth* 或 *--keyFile*
参数，你就必须在进行任何操作前进行认证。
你可以在连接时进行认证。方法是在链接字符串中指定用户名密码，或者在 <span
class="function">MongoClient::\_\_construct</span> 构造函数中指定
*"username"* 和 *"password"*。

**示例 \#1 针对“admin”数据库的认证**

``` php
<?php
// Specifying the username and password in the connection URI (preferred)
$m = new MongoClient("mongodb://${username}:${password}@localhost");

// Specifying the username and password via the options array (alternative)
$m = new MongoClient("mongodb://localhost", array("username" => $username, "password" => $password));
?>
```

默认状态下，驱动会针对 *admin*
数据库进行认证。认证也可以对其他数据库进行。方法是在连接字符串中指定数据库名，或者
<span class="function">MongoClient::\_\_construct</span> 构造函数中指定
*"db"*。

**示例 \#2 针对一般数据库的认证**

``` php
<?php
// Specifying the authentication database in the connection URI (preferred)
$m = new MongoClient("mongodb://${username}:${password}@localhost/myDatabase");

// Specifying the authentication database via the options array (alternative)
$m = new MongoClient("mongodb://${username}:${password}@localhost", array("db" => "myDatabase"));
?>
```

如果链接中断，驱动会重新尝试链接并会自动重新认证。

复制集合
--------

要链接到一个复制，需要指定复制中的一个或多个成员，并使用 *"replicaSet"*
选项指定复制的名字。多个服务器用逗号分割。

**示例 \#1 链接到一个复制**

``` php
<?php
// Using multiple servers as the seed list (prefered)
$m = new MongoClient("mongodb://rs1.example.com:27017,rs2.example.com:27017/?replicaSet=myReplSetName"));

// Using one server as the seed list
$m = new MongoClient("mongodb://rs1.example.com:27017", array("replicaSet" => "myReplSetName"));

// Using multiple servers as the seed list
$m = new MongoClient("mongodb://rs1.example.com:27017,rs2.example.com:27017", array("replicaSet" => "myReplSetName"));
?>
```

驱动会查询数据库服务器列表，然后找出主服务器。如果可以成功的链接到指定的服务器至少一个，并且可以找到主服务器，链接就会成功。如果它无法链接指定的任何一个服务器，或者找不到主服务器，会抛出一个
<span class="classname">MongoConnectionException</span> 类型的异常

**小贴士**

你应该始终指定多个复制中的服务器。为了达到最大的可用性，你指定的服务器列表应该包含每一个数据中心的服务器至少一台。

如果主服务器变为不可用，会有一台次要服务器通过投票算法自动提升为主服务器（除非“投票”无法选出主服务器）。在一段时间里
（<a href="https://docs.mongodb.com/manual/faq/replica-sets/#how-long-does-replica-set-failover-take" class="link external">» 20-60 秒</a>），链接无法进行写操作，此时写入会导致一个异常。
到次要服务器的链接仍然可以提供读取功能。

> **Note**:
>
> 默认的 <a href="/book/mongo.html#读取首选项" class="link">读取偏好</a>
> 是只从主服务器读取。在自动选择新的主服务器的时间里，读取操作也会失败。
>
> 对于要求很高的读取可用性的应用，推荐使用
> **`MongoClient::RP_PRIMARY_PREFERRED`**
> 读取偏好来确保主服务器出现问题的时候能正确的从次要服务器中读取。

当新的主服务器被选出后，尝试读写操作时，驱动会检测新的主服务器。然后链接到它，继续提供正常的功能。

次要服务器的健康状态每5秒（可以通过
<a href="/book/mongo.html#" class="link">mongo.ping_interval</a>
调整），或5秒后的下一个操作执行时检查一次。驱动会在连接服务器出现错误时重新检查配置。

复制集会每60秒（可以通过
<a href="/book/mongo.html#" class="link">mongo.is_master_interval</a>
调整），或在w=1的写入操作发生错误的时候检查故障并尝试恢复。

**Caution**

次要服务器中的操作相比主服务器有一定延迟，因此如果使用
**`MongoClient::RP_PRIMARY`**
之外的读取偏好，你的程序就必须能够正确处理过时的数据。

要了解更多关于复制集的信息，参考
<a href="https://docs.mongodb.com/manual/replication/" class="link external">» core documentation</a>.

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <a href="/book/mongo.html#Write%20Concerns" class="xref"></a>

| 版本  | 说明                               |
|-------|------------------------------------|
| 1.0.9 | 添加了复制集支持，和自动错误恢复。 |

Sharding
--------

To connect to a shard cluster, specify the address of one or more
*mongos* instances in the connection string. Multiple servers may be
delimited by a comma.

``` php
<?php
// Using one server as the seed list
$m = new MongoClient("mongodb://mongos1.example.com:27017");

// Using multiple servers as the seed list
$m = new MongoClient("mongodb://mongos1.example.com:27017,mongos2.example.com:27017"));
?>
```

Regardless of whether each shard is a stand-alone *mongod* server or a
full replica set, the driver's connection process is the same. All
database communication will be routed through *mongos*.

For more information on sharding with MongoDB, see the
<a href="https://docs.mongodb.com/manual/sharding/" class="link external">» sharding documentation</a>.

Unix Domain Socket支持
----------------------

MongoDB 服务程序内置支持通过 Unix Sockets
链接，并且会在启动时建立socket，默认位置在 `/tmp/mongodb-<port>.sock.`.

要通过socket链接，需要在连接字符串中指定socket路径，如：

``` php
<?php
$m = new MongoClient("mongodb:///tmp/mongo-27017.sock");
?>
```

如果要在通过socket的链接中对数据库进行认证（如上文所述），你需要指定一个端口号
*0* 让链接字符串解析时可以找到 socket路径
的结尾。另外，你可以在链接的时候使用options参数。

``` php
<?php
$m = new MongoClient("mongodb://username:password@/tmp/mongo-27017.sock:0/foo");
?>
```

| 版本  | 说明                       |
|-------|----------------------------|
| 1.0.9 | 添加 Unix Sockets 的支持。 |

Connection Pooling (version 1.2.0-1.2.12 \*only\*)
--------------------------------------------------

> **Note**:
>
> This section is no longer relevant as of the 1.3.0 release of the
> driver and only serves as a historical information on how the pooling
> used to work.
>
> The latest versions of the driver have no concept of pooling anymore
> and will maintain only one connection per process, for each connection
> type (ReplicaSet/standalone/mongos), for each credentials combination.

Creating connections is one of the most heavyweight things that the
driver does. It can take hundreds of milliseconds to set up a connection
correctly, even on a fast network. Thus, the driver tries to minimize
the number of new connections created by reusing connections from a
pool.

When a user creates a new instance of <span
class="classname">MongoClient</span>, all necessary connections will be
taken from their pools (replica sets may require multiple connections,
one for each member of the set). When the <span
class="classname">MongoClient</span> instance goes out of scope, the
connections will be returned to the pool. When the PHP process exits,
all connections in the pools will be closed.

"Why do I have so many open connections?"
-----------------------------------------

Connection pools can generate a large number of connections. This is
expected and, using a little arithmetic, you can figure out how many
connections will be created. There are three factors in determining the
total number of connections:

-   *connections\_per\_pool*

    Each connection pool will create, by default, an unlimited number of
    connections. One might assume that this is a problem: if it can
    create an unlimited number of connections, couldn't it create
    thousands and the server would run out of file descriptors? In
    practice, this is unlikely, as unused connections are returned to
    the pool to be used later, so future connections will use the same
    connection instead of creating a new one. Unless you create
    thousands of connections at once without letting any go out of
    scope, the number of connections open should stay at a reasonable
    number.

    You can see how many connections you have in a pool using the <span
    class="function">MongoPool::info</span> function. Add up the "in
    use" and "in pool" fields for a given server. That is the total
    number of connections for that pool.

-   *pools\_per\_process*

    Each MongoDB server address you're connecting to gets its own
    connection pool. For example, if your local hostname is
    "example.net", connecting to "example.net:27017", "localhost:27017",
    and "/tmp/mongodb-27017.sock" will create three connection pools.
    You can see how many connection pools you have open using <span
    class="function">MongoPool::info</span>.

-   *processes*

    Each PHP process has a separate set of pools. PHP-FPM and Apache
    generally create between 6 and a couple of dozen PHP worker
    children. Check your settings to see what the max number of PHP
    processes is that can be spawned.

    If you are using PHP-FPM, estimating the number of connections can
    be tricky because it will spawn more PHP-FPM workers under heavy
    load. To be on the safe side, look at the *max\_children* parameter
    or add up *spare\_servers* + *start\_servers* (choose whichever
    number is higher). That will indicate how many PHP processes (i.e.
    sets of pools) you should plan for.

The three variables above can be multiplied together to give the max
number of connections expected: *connections\_per\_pool* \*
*pools\_per\_process* \* *processes*. Note that *connections\_per\_pool*
can be different for different pools, so *connections\_per\_pool* should
be the max.

For example, suppose we're getting 30 connections per pool, 10 pools per
PHP process, and 128 PHP processes. Then we can expect 38400 connections
from this machine. Thus, we should set this machine's file descriptor
limit to be high enough to handle all of these connections or it may run
out of file descriptors.

See <span class="classname">MongoPool</span> for more information on
connection pooling.

Persistent Connections (version up to 1.1.4 \*only\*)
-----------------------------------------------------

> **Note**:
>
> This section is not relevant for 1.2.0+. In 1.2.0+, connections are
> always persistent and managed automatically by the driver. If you are
> using a 1.2.x release (but not 1.3.x or later), see <span
> class="classname">MongoPool</span> for more information on pooling.

Creating new connection to the database is very slow. To minimize the
number of connections that you need to make, you can use persistent
connections. A persistent connection is saved by PHP, so you can use the
same connection for multiple requests.

For example, this simple program connects to the database 1000 times:

``` php
<?php

for ($i=0; $i<1000; $i++) {
  $m = new MongoClient();
}

?>
```

It takes approximately 18 seconds to execute. If we change it to use a
persistent connection:

``` php
<?php

for ($i=0; $i<1000; $i++) {
  $m = new MongoClient("localhost:27017", array("persist" => "x"));
}

?>
```

...it takes less than .02 seconds to execute, as it only makes one
database connection.

Persistent connections need an identifier string (which is "x" in the
above example) to uniquely identify them. For a persistent connection to
be used, the hostname, port, persist string, and authentication
credentials (username, password and database, if given) must match an
existing persistent connection. Otherwise, a new connection will be
created with this identifying information.

Persistent connections are *highly recommended* and should always be
used in production unless there is a compelling reason not to. Most of
the reasons that they are not recommended for relational databases are
irrelevant to MongoDB.

The PHP MongoDB extension provides
<a href="/context.html" class="link">Stream Context Support</a> using
the <a href="/context/mongodb.html" class="link">mongodb</a> context.

A stream context must be created with <span
class="function">stream\_context\_create</span> and passed to the <span
class="methodname">MongoClient::\_\_construct</span> before the actual
connection to MongoDB is made. It is not possible to apply a stream
context to already created streams.

Additional context options and parameters, such as
<a href="/context/ssl.html" class="link">ssl</a> and
<a href="/context/params.html" class="link">notification parameters</a>,
are also supported.

The MongoDB context options provide a rich interface to log network
traffic between the driver and the MongoDB servers. This interface can
be used to provide query logging, profiler, debuggers, or anything that
would need to inspect the underlaying commands and protocol options.

-   <a href="/context/ssl.html" class="xref">SSL 上下文选项</a>
-   <a href="/context/socket.html" class="xref">套接字上下文选项</a>
-   <a href="/context/params.html" class="xref">Context 参数</a>

log\_cmd\_delete
================

Callback When Deleting Documents

### 说明

<span class="methodname">log\_cmd\_delete</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span>
`$writeOptions`</span> , <span class="methodparam"><span
class="type">array</span> `$deleteOptions`</span> , <span
class="methodparam"><span class="type">array</span>
`$protocolOptions`</span> )

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-cmd-delete" class="link">log_cmd_delete context option</a>,
when deleteing a document

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`writeOptions`  
| key          | value                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------|
| ordered      | boolean, if the operation (in case of batch operation) must be executed sequentually (ordered=true) |
| writeConcern | An array of writeConcern options (see below)                                                        |

| key      | value                                                                                    |
|----------|------------------------------------------------------------------------------------------|
| fsync    | boolean, force flushing to disk before returning                                         |
| j        | boolean, force journal write before returning                                            |
| wtimeout | integer, milliseconds, maximum time the primary is allowed to wait to verify replication |
| w        | integer=server count, or string=replication-tag                                          |

`deleteOptions`  
| key   | value                                                 |
|-------|-------------------------------------------------------|
| limit | integer, 1 or 0. If 0, delete all matching documents. |
| q     | Array, the search criteria                            |

`protocolOptions`  
| key             | value                                                                       |
|-----------------|-----------------------------------------------------------------------------|
| message\_length | The total size (in bytes) of the encoded message being sent over the wire   |
| request\_id     | The request identifier for this message: *42*                               |
| namespace       | The MongoDB namespace used for the protocol message *dbname.collectionname* |

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.5.0 | Only available when connected to MongoDB 2.6.0+ |

log\_cmd\_insert
================

Callback When Inserting Documents

### 说明

<span class="methodname">log\_cmd\_insert</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span>
`$document`</span> , <span class="methodparam"><span
class="type">array</span> `$writeOptions`</span> , <span
class="methodparam"><span class="type">array</span>
`$protocolOptions`</span> )

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-cmd-insert" class="link">log_cmd_insert context option</a>,
when inserting a document

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`document`  
The document that has been prepared to be inserted

`writeOptions`  
| key          | value                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------|
| ordered      | boolean, if the operation (in case of batch operation) must be executed sequentually (ordered=true) |
| writeConcern | An array of writeConcern options (see below)                                                        |

| key      | value                                                                                    |
|----------|------------------------------------------------------------------------------------------|
| fsync    | boolean, force flushing to disk before returning                                         |
| j        | boolean, force journal write before returning                                            |
| wtimeout | integer, milliseconds, maximum time the primary is allowed to wait to verify replication |
| w        | integer=server count, or string=replication-tag                                          |

`protocolOptions`  
| key             | value                                                                       |
|-----------------|-----------------------------------------------------------------------------|
| message\_length | The total size (in bytes) of the encoded message being sent over the wire   |
| request\_id     | The request identifier for this message: *42*                               |
| namespace       | The MongoDB namespace used for the protocol message *dbname.collectionname* |

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.5.0 | Only available when connected to MongoDB 2.6.0+ |

log\_cmd\_update
================

Callback When Updating Documents

### 说明

<span class="methodname">log\_cmd\_update</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span>
`$writeOptions`</span> , <span class="methodparam"><span
class="type">array</span> `$updateOptions`</span> , <span
class="methodparam"><span class="type">array</span>
`$protocolOptions`</span> )

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-cmd-update" class="link">log_cmd_update context option</a>,
when updateing a document

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`writeOptions`  
| key          | value                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------|
| ordered      | boolean, if the operation (in case of batch operation) must be executed sequentually (ordered=true) |
| writeConcern | An array of writeConcern options (see below)                                                        |

| key      | value                                                                                    |
|----------|------------------------------------------------------------------------------------------|
| fsync    | boolean, force flushing to disk before returning                                         |
| j        | boolean, force journal write before returning                                            |
| wtimeout | integer, milliseconds, maximum time the primary is allowed to wait to verify replication |
| w        | integer=server count, or string=replication-tag                                          |

`updateOptions`  
| key    | value                                                                      |
|--------|----------------------------------------------------------------------------|
| multi  | Boolean, true if this update is allowed to update all matched criteria     |
| upsert | Boolean, true if the document should be created if criteria does not match |
| q      | Array, the search criteria                                                 |
| u      | Array, the new object/modifications                                        |

`protocolOptions`  
| key             | value                                                                       |
|-----------------|-----------------------------------------------------------------------------|
| message\_length | The total size (in bytes) of the encoded message being sent over the wire   |
| request\_id     | The request identifier for this message: *42*                               |
| namespace       | The MongoDB namespace used for the protocol message *dbname.collectionname* |

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.5.0 | Only available when connected to MongoDB 2.6.0+ |

log\_getmore
============

Callback When Retrieving Next Cursor Batch

### 说明

<span class="methodname">log\_getmore</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span> `$info`</span>
)

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-getmore" class="link">log_getmore context option</a>,
when executing a GET\_MORE operation.

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`info`  
| key         | value                                                        |
|-------------|--------------------------------------------------------------|
| request\_id | integer, the driver request identifier                       |
| cursor\_id  | integer, the cursor identifier being used to fetch more data |
| batch\_size | integer, maximum number of documents being requested         |

log\_killcursor
===============

Callback When Executing KILLCURSOR operations

### 说明

<span class="methodname">log\_killcursor</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span> `$info`</span>
)

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-killcursor" class="link">log_killcursor context option</a>,
when reading a killcursor from MongoDB.

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`info`  
| key        | value                                  |
|------------|----------------------------------------|
| cursor\_id | integer, the cursor identifier to kill |

log\_reply
==========

Callback When Reading the MongoDB reply

### 说明

<span class="methodname">log\_reply</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span>
`$messageHeaders`</span> , <span class="methodparam"><span
class="type">array</span> `$operationHeaders`</span> )

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-reply" class="link">log_reply context option</a>,
when reading a reply from MongoDB.

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`messageHeaders`  
| key          | value                                                                |
|--------------|----------------------------------------------------------------------|
| length       | integer, bytes, message reply length                                 |
| request\_id  | integer, the server request identifier                               |
| response\_id | integer, the driver request identifier this message is a response of |
| opcode       | integer, the opcode id                                               |

`operationHeaders`  
| key        | value                                                                                      |
|------------|--------------------------------------------------------------------------------------------|
| flags      | integer, bitmask of protocol flags                                                         |
| cursor\_id | integer, ID of the cursor created on the server (0 if none created, or its been exhausted) |
| start      | The starting offset of this cursor                                                         |
| returned   | integer, how many documents are returned in this trip                                      |

### 参见

-   The
    <a href="https://docs.mongodb.com/meta-driver/latest/legacy/mongodb-wire-protocol/" class="link external">» OP_REPLY definition in the Wire Protocol</a>

log\_write\_batch
=================

Callback When Writing Batches

### 说明

<span class="methodname">log\_write\_batch</span> ( <span
class="methodparam"><span class="type">array</span> `$server`</span> ,
<span class="methodparam"><span class="type">array</span>
`$writeOptions`</span> , <span class="methodparam"><span
class="type">array</span> `$batch`</span> , <span
class="methodparam"><span class="type">array</span>
`$protocolOptions`</span> )

A <span class="type">callable</span> function, used by the
<a href="/context/mongodb.html#context.mongodb.log-write-batch" class="link">log_write_batch context option</a>,
when executing a batch operation.

> **Note**:
>
> This is *not* a real function, only a prototype of how the function
> should be.

### 参数

`server`  
An array containing the basic information about the server that was
picked.

| key                | value                                                                |
|--------------------|----------------------------------------------------------------------|
| hash               | server hash, example: *localhost:27017;-;X;56052*                    |
| type               | Node type (primary/secondary/mongos/arbiter): *2*                    |
| max\_bson\_size    | The maximum BSON Size over the wire this node accepts: *16777216*    |
| max\_message\_size | The maximum Message Size over the wire this node accepts: *48000000* |
| request\_id        | The request identifier for this message: *42*                        |

`writeOptions`  
| key          | value                                                                                               |
|--------------|-----------------------------------------------------------------------------------------------------|
| ordered      | boolean, if the operation (in case of batch operation) must be executed sequentually (ordered=true) |
| writeConcern | An array of writeConcern options (see below)                                                        |

| key      | value                                                                                    |
|----------|------------------------------------------------------------------------------------------|
| fsync    | boolean, force flushing to disk before returning                                         |
| j        | boolean, force journal write before returning                                            |
| wtimeout | integer, milliseconds, maximum time the primary is allowed to wait to verify replication |
| w        | integer=server count, or string=replication-tag                                          |

`batch`  
Array, the actual batch operation.

`protocolOptions`  
| key             | value                                                                       |
|-----------------|-----------------------------------------------------------------------------|
| message\_length | The total size (in bytes) of the encoded message being sent over the wire   |
| request\_id     | The request identifier for this message: *42*                               |
| namespace       | The MongoDB namespace used for the protocol message *dbname.collectionname* |

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.5.0 | Only available when connected to MongoDB 2.6.0+ |

**目录**

-   [log\_cmd\_delete](/book/mongo.html#log_cmd_delete) — Callback When
    Deleting Documents
-   [log\_cmd\_insert](/book/mongo.html#log_cmd_insert) — Callback When
    Inserting Documents
-   [log\_cmd\_update](/book/mongo.html#log_cmd_update) — Callback When
    Updating Documents
-   [log\_getmore](/book/mongo.html#log_getmore) — Callback When
    Retrieving Next Cursor Batch
-   [log\_killcursor](/book/mongo.html#log_killcursor) — Callback When
    Executing KILLCURSOR operations
-   [log\_reply](/book/mongo.html#log_reply) — Callback When Reading the
    MongoDB reply
-   [log\_write\_batch](/book/mongo.html#log_write_batch) — Callback
    When Writing Batches

Writes
======

Updating Nested Objects
-----------------------

Suppose we wish to change the name of a comment's author in this
document:

``` javascript
{ 
    "_id" : ObjectId("4b06c282edb87a281e09dad9"), 
    "content" : "this is a blog post.",
    "comments" : 
    [
        {
            "author" : "Mike",
            "comment" : "I think that blah blah blah...",
        },
        {
            "author" : "John",
            "comment" : "I disagree."
        }
    ]
}
```

In order to change an inner field, we use $set (so that all of the other
fields are not removed!) with the index of comment to change:

``` php
<?php

$blog->update($criteria, array('$set' => array("comments.1" => array("author" => "Jim"))));

?>
```

The Positional Operator
-----------------------

The positional operator *$* is useful for updating objects that are in
arrays. In the example above, for instance, suppose that we did not know
the index of the comment that we needed to change, merely that we needed
to change "John" to "Jim". We can use *$* to do so.

``` php
<?php

$blog->update(
    array('comments.author' => 'John'), 
    array('$set' => array('comments.$.author' => 'Jim')));

?>
```

Querying
========

All queries (reads and writes) are only sent to the primary member of a
replica set by default. This is however easily configurable by using the
<a href="/book/mongo.html#读取首选项" class="link">Read Preferences</a>
which allow you to set some generic read preferences (such as allowing
secondary reads of the nearest server), and also provide ways to
specifically target a server in a specific country, datacenter, or even
hardware, by the use of
<a href="/book/mongo.html#标签集" class="link">replica set tag sets</a>.

Read preferences can be configured at every level of the driver:

-   As a query parameter or option to <span
    class="methodname">MongoClient::\_\_construct</span>
-   Specifically by calling <span
    class="methodname">MongoClient::setReadPreference</span>
-   At the database level with <span
    class="methodname">MongoDB::setReadPreference</span>
-   At the collection level with <span
    class="methodname">MongoCollection::setReadPreference</span>
-   At the cursor level with <span
    class="methodname">MongoCursor::setReadPreference</span> or <span
    class="methodname">MongoCommandCursor::setReadPreference</span>

Each class inherits its read preference setting from the "parent"
context.

**示例 \#1 Inheriting read preferences from the database level down to
the cursor**

``` php
<?php
$db->setReadPreference(MongoClient::RP_SECONDARY_PREFERRED);
$c = $db->myCollection;

$cursor = $c->find();
?>
```

In this example, the query will be executed against a secondary. The
collection inherits **`MongoClient::RP_SECONDARY_PREFERRED`** from the
database and the cursor inherits it from the collection.

Each instance of <span class="classname">MongoClient</span> chooses its
own secondary using the available secondary with the lowest ping time.
So, if we had a PHP client in Europe and one in Australia and we had one
secondary in each of these data centers, we could do:

``` php
<?php
$options = array("replicaSet" => "setName", "readPreference" => MongoClient::RP_SECONDARY_PREFERRED);

// on the Australian client
$m = new MongoClient("mongodb://primary,australianhost.secondary,europeanhost.secondary", $options);
$cursor = $m->foo->bar->find();
$cursor->getNext();
echo "Reading from: ", $cursor->info()["server"], "\n";

// on the European client
$m = new MongoClient("mongodb://primary,australianhost.secondary,europeanhost.secondary", $options);
$cursor = $m->foo->bar->find();
$cursor->getNext();
echo "Reading from: ", $cursor->info()["server"], "\n";
?>
```

以上例程的输出类似于：

    Reading from: australianHost
    Reading from: europeanHost

Note that we have to do a query before a secondary is chosen:
secondaries are chosen lazily by the driver, and for each query
separately.

You can see what the driver thinks is the current status of the set
members by running <span class="methodname">MongoClient::getHosts</span>
or <span class="methodname">MongoClient::getConnections</span>.

If no secondary is readable, the driver will send reads to the primary
as we specified **`MongoClient::RP_SECONDARY_PREFERRED`** which will
fallback to execute a query on a primary if no secondaries are
available. A server is considered readable if its state is 2 (SECONDARY)
and its health is 1. You can check this with <span
class="methodname">MongoClient::getHosts</span> and <span
class="methodname">MongoClient::getConnections</span>.

Writes are always sent to the primary—and by default all reads are sent
to the primary too.

Every object inserted is automatically assigned a unique *\_id* field,
which is often a useful field to use in queries. This works similarly to
"get last insert ID" functionality, except that the *\_id* is chosen by
the *client*.

Suppose that we wish to find the document we just inserted. Inserting
adds an *\_id* field to the document, so we can query by that:

``` php
<?php
$person = array("name" => "joe");

$people->insert($person);

// now $joe has an _id field
$joe = $people->findOne(array("_id" => $person['_id']));
?>
```

Unless the user has specified otherwise, the *\_id* field is a <span
class="classname">MongoId</span>. The most common mistake is attempting
to use a string to match a <span class="classname">MongoId</span>. Keep
in mind that these are two different datatypes, and will not match each
other in the same way that the string "array()" is not the same as an
empty array. For example:

``` php
<?php
$person = array("name" => "joe");

$people->insert($person);

// convert the _id to a string
$pid = $person['_id'] . "";

// FAILS - $pid is a string, not a MongoId
$joe = $people->findOne(array("_id" => $pid));
?>
```

Arrays are special in a couple ways. First, there are two types that
MongoDB uses: "normal" arrays and associative arrays. Associative arrays
can have any mix of key types and values. "Normal" arrays are defined as
arrays with ascending numeric indexes starting at 0 and increasing by
one for each element. These are, typically, just your usual PHP array.

For instance, if you want to save a list of awards in a document, you
could say:

``` php
<?php

$collection->save(array("awards" => array("gold", "silver", "bronze")));

?>
```

Queries can reach into arrays to search for elements. Suppose that we
wish to find all documents with an array element of a given value. For
example, documents with a "gold" award, such as:

    { "_id" : ObjectId("4b06c282edb87a281e09dad9"), "awards" : ["gold", "silver", "bronze"]}

This can be done with a simple query, ignoring the fact that "awards" is
an array:

``` php
<?php

  $cursor = $collection->find(array("awards" => "gold"));

?>
```

Suppose we are querying for a more complex object, if each element of
the array were an object itself, such as:

    {
         "_id" : ObjectId("4b06c282edb87a281e09dad9"),
         "awards" :
         [
            {
                "first place" : "gold"
            },
            {
                "second place" : "silver"
            },
            {
                "third place" :  "bronze"
            }
         ]
    }

Still ignoring that this is an array, we can use dot notation to query
the subobject:

``` php
<?php

$cursor = $collection->find(array("awards.first place" => "gold"));

?>
```

Notice that it doesn't matter that there is a space in the field name
(although it may be best not to use spaces, just to make things more
readable).

You can also use an array to query for a number of possible values. For
instance, if we were looking for documents "gold" or "copper", we could
do:

``` php
<?php

$cursor = $collection->find(array("awards" => array('$in' => array("gold", "copper"))));

?>
```

| 版本  | 说明                                                                                                                                                      |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Introduced the <a href="/book/mongo.html#读取首选项" class="link">Read Preferences</a> framework to allow more fine grained control over secondary reads. |
| 1.3.0 | Deprecated *slaveOkay* usage, the alternative is <a href="/book/mongo.html#读取首选项" class="link">Read Preferences</a>.                                 |
| 1.1.0 | Introduced the possiblity of routing reads to secondaries of replica set members using <span class="methodname">Mongo::setSlaveOkay</span>                |

Updates
=======

Updates can be one of the most complicated operation available with
MongoDB. They combine a query with an action, modifying documents that
match the criteria. They are also extremely powerful, allowing you to
change documents quickly and replace them altogether. They are done
in-place (when possible) with little overhead.

Modifying vs. replacing documents
---------------------------------

There are two types of updates you can use: modifying updates and
replacing updates. Modifying updates contain $-operators and change
fields in a document: they might increment counters, push new elements
onto an array, or change the type of a field.

For example, a modifying update could add a new field to a document.

``` php
<?php
/** suppose documents look like:
 * {"username" : "...", "password" : "...", "email" : "..."}
 */
$coll->update(array("username" => "joe"), array('$set' => array("twitter" => "@joe4153")));

/** now the document will look like:
 * {"username" : "joe", "password" : "...", "email" : "...", "twitter" : "@joe4153"}
 */
?>
```

Replacing updates replace the entire matching document with a new
document. They are generally not as efficient as using $-modifiers, but
can be very usefully for complex operations or updates that can't be
expressed in terms of $-operators.

For example, a replacing update can completely change the structure of a
document.

``` php
<?php
/** suppose documents look like:
 * {"username" : "...", "password" : "...", "email" : "..."}
 */
$coll->update(array("username" => "joe"), array("userId" => 12345, "info" => array(
    "name" => "joe", "twitter" => "@joe4153", "email" => "..."), "likes" => array()));

/** now the document will look like:
 * {
 *     "userId" : 12345, 
 *     "info" : {
 *         "name" : "joe", 
 *         "twitter" : "@joe4153", 
 *         "email" : "..."
 *     },
 *     "likes" : []
 * }
 */
?>
```

Updating Nested Objects
-----------------------

Suppose we wish to change the name of a comment's author in this
document:

``` javascript
{ 
    "_id" : ObjectId("4b06c282edb87a281e09dad9"), 
    "content" : "this is a blog post.",
    "comments" : 
    [
        {
            "author" : "Mike",
            "comment" : "I think that blah blah blah...",
        },
        {
            "author" : "John",
            "comment" : "I disagree."
        }
    ]
}
```

In order to change an inner field, we use $set (so that all of the other
fields are not removed!) with the index of comment to change:

``` php
<?php

$blog->update($criteria, array('$set' => array("comments.1" => array("author" => "Jim"))));

?>
```

The Positional Operator
-----------------------

The positional operator *$* is useful for updating objects that are in
arrays. In the example above, for instance, suppose that we did not know
the index of the comment that we needed to change, merely that we needed
to change "John" to "Jim". We can use *$* to do so.

``` php
<?php

$blog->update(
    array("comments.author" => "John"), 
    array('$set' => array('comments.$.author' => "Jim")));

?>
```

Security
========

Request Injection Attacks
-------------------------

If you are passing *$\_GET* (or *$\_POST*) parameters to your queries,
make sure that they are cast to strings first. Users can insert
associative arrays in GET and POST requests, which could then become
unwanted $-queries.

A fairly innocuous example: suppose you are looking up a user's
information with the request *http://www.example.com?username=bob*. Your
application does the query *$collection-\>find(array("username" =\>
$\_GET\['username'\]))*.

Someone could subvert this by getting
*http://www.example.com?username\[$ne\]=foo*, which PHP will magically
turn into an associative array, turning your query into
*$collection-\>find(array("username" =\> array('$ne' =\> "foo")))*,
which will return all users not named "foo" (all of your users,
probably).

This is a fairly easy attack to defend against: make sure $\_GET and
$\_POST parameters are the type you expect before you send them to the
database (cast them to strings, in this case).

Note that this type of attack can be used with any databases interation
that locates a document, including updates, upserts, find-and-modifies,
and removes.

Thanks to
<a href="https://www.idontplaydarts.com/2010/07/mongodb-is-vulnerable-to-sql-injection-in-php-at-least/" class="link external">» Phil</a>
for pointing this out.

See
<a href="https://docs.mongodb.com/manual/security/" class="link external">» the main documentation</a>
for more information about SQL-injection-like issues with MongoDB.

Script Injection Attacks
------------------------

If you are using JavaScript, make sure that any variables that cross the
PHP- to-JavaScript boundry are passed in the *scope* field of <span
class="classname">MongoCode</span>, not interpolated into the JavaScript
string. This can come up when using <span
class="function">MongoDB::execute</span>, *$where* clauses, MapReduces,
group-bys, and any other time you may pass JavaScript into the database.

> **Note**:
>
> MapReduce ignore the *scope* field of <span
> class="classname">MongoCode</span>, but there is a *scope* option on
> the command that can be used instead.

For example, suppose we have some JavaScript to greet a user in the
database logs. We could do:

``` php
<?php

// don't do this!

$username = $_POST['username'];
$db->execute("print('Hello, $username!');");

?>
```

However, what if a malicious user passes in some JavaScript?

``` php
<?php

// don't do this!

// $username is set to "'); db.users.drop(); print('"
$db->execute("print('Hello, $username!');");

?>
```

Now MongoDB executes the JavaScript string *"print('Hello, ');
db.users.drop(); print('!');"*. This attack is easy to avoid: use
*scope* to pass variables from PHP to JavaScript:

``` php
<?php

$scope = array("user" => $username);
$db->execute(new MongoCode("print('Hello, '+user+'!');", $scope));

?>
```

This adds a variable *user* to the JavaScript scope. Now if someone
tries to send malicious code, MongoDB will harmlessly print *Hello, ');
db.dropDatabase(); print('!*.

Using *scope* helps prevent malicious input from being executed by the
database. However, you must make sure that your code does not turn
around and execute the input anyway! For example, never use the
JavaScript *eval* function on user input:

``` php
<?php

// don't do this!

// $jsShellInput is "db.users.drop();"
$scope = array("input" => $jsShellInput);
$db->execute(new MongoCode("eval(input);", $scope));

?>
```

Always use *scope* and never allow the database to execute user input as
code.

故障排除
========

如果你有问题，这里有一些资源可以访问。

-   IRC

    MongoDB 官方的 IRC 频道是 irc.freenode.net/\#mongodb 。
    这是所有方式中可以最快获得帮助的地方。

-   邮件列表

    <a href="https://groups.google.com/group/mongodb-user/" class="link external">» MongoDB's mailing list</a>
    是提问的好地方（通常回复会比较迅速）。

-   错误追踪

    发现了BUG，希望在 MongoDB 中添加新的功能，有疑问？可以在
    <a href="https://jira.mongodb.org/browse/PHP" class="link external">» PHP driver's bug tracker</a>
    中创建。

你可以让驱动把所有类型的错误记录为 **`E_NOTICE`** 级别的PHP错误。查看
<span class="classname">MongoLog</span> 实例。

Running the Driver's Tests
==========================

The PECL package does not come with the tests, but they are available at
<a href="https://github.com/mongodb/mongo-php-driver-legacy" class="link external">» Github</a>.

.phpt Tests
-----------

.phpt tests are the standard way of testing PHP extensions. After
compiling the MongoDB driver with "make" you can then issue "make test"
to run the tests. These tests require MongoDB to be working, and hence,
you need to configure the test suite itself.

There is more information on running the tests in the contributing
guidelines on
<a href="https://github.com/mongodb/mongo-php-driver/blob/master/CONTRIBUTING.md#running-the-tests" class="link external">» GitHub</a>.

Reporting Errors
----------------

Please report any failures or errors in the
<a href="https://jira.mongodb.org/browse/PHP" class="link external">» bugtracker</a>.
There may be skipped tests, these are normal and can be ignored.

New tests are always welcome! Please feel free to contribute new tests
of any type testing any functionality.

核心类
======

**目录**

-   [MongoClient](/book/mongo.html#MongoClient) — MongoClient 类
    -   [MongoClient::close](/book/mongo.html#MongoClient::close) —
        关闭连接
    -   [MongoClient::connect](/book/mongo.html#MongoClient::connect) —
        连接到数据库服务器
    -   [MongoClient::\_\_construct](/book/mongo.html#MongoClient::__construct)
        — 创建一个新的数据库连接对象
    -   [MongoClient::dropDB](/book/mongo.html#MongoClient::dropDB) —
        删除一个数据库 \[已废弃\]
    -   [MongoClient::\_\_get](/book/mongo.html#MongoClient::__get) —
        取得一个数据库
    -   [MongoClient::getConnections](/book/mongo.html#MongoClient::getConnections)
        — 返回所有已打开连接的信息
    -   [MongoClient::getHosts](/book/mongo.html#MongoClient::getHosts)
        — 更新所有关联主机的状态信息
    -   [MongoClient::getReadPreference](/book/mongo.html#MongoClient::getReadPreference)
        — 获取此连接的读取首选项
    -   [MongoClient::getWriteConcern](/book/mongo.html#MongoClient::getWriteConcern)
        — Get the write concern for this connection
    -   [MongoClient::killCursor](/book/mongo.html#MongoClient::killCursor)
        — Kills a specific cursor on the server
    -   [MongoClient::listDBs](/book/mongo.html#MongoClient::listDBs) —
        列出所有有效数据库
    -   [MongoClient::selectCollection](/book/mongo.html#MongoClient::selectCollection)
        — 获取数据库的文档集
    -   [MongoClient::selectDB](/book/mongo.html#MongoClient::selectDB)
        — 获取一个数据库
    -   [MongoClient::setReadPreference](/book/mongo.html#MongoClient::setReadPreference)
        — 为该连接设置读取选项
    -   [MongoClient::setWriteConcern](/book/mongo.html#MongoClient::setWriteConcern)
        — Set the write concern for this connection
    -   [MongoClient::\_\_toString](/book/mongo.html#MongoClient::__toString)
        — 该连接的字符串表达方式
-   [MongoDB](/book/mongo.html#MongoDB) — MongoDB 类
    -   [MongoDB::authenticate](/book/mongo.html#MongoDB::authenticate)
        — 登录到数据库
    -   [MongoDB::command](/book/mongo.html#MongoDB::command) — 执行一条
        Mongo 指令
    -   [MongoDB::\_\_construct](/book/mongo.html#MongoDB::__construct)
        — 选择一个数据库
    -   [MongoDB::createCollection](/book/mongo.html#MongoDB::createCollection)
        — 创建一个集合
    -   [MongoDB::createDBRef](/book/mongo.html#MongoDB::createDBRef) —
        创建数据库引用
    -   [MongoDB::drop](/book/mongo.html#MongoDB::drop) — 删除数据库
    -   [MongoDB::dropCollection](/book/mongo.html#MongoDB::dropCollection)
        — Drops a collection \[deprecated\]
    -   [MongoDB::execute](/book/mongo.html#MongoDB::execute) —
        在数据库服务器上运行JavaScript
    -   [MongoDB::forceError](/book/mongo.html#MongoDB::forceError) —
        Creates a database error
    -   [MongoDB::\_\_get](/book/mongo.html#MongoDB::__get) — Gets a
        collection
    -   [MongoDB::getCollectionInfo](/book/mongo.html#MongoDB::getCollectionInfo)
        — Returns information about collections in this database
    -   [MongoDB::getCollectionNames](/book/mongo.html#MongoDB::getCollectionNames)
        — Gets an array of names for all collections in this database
    -   [MongoDB::getDBRef](/book/mongo.html#MongoDB::getDBRef) —
        Fetches the document pointed to by a database reference
    -   [MongoDB::getGridFS](/book/mongo.html#MongoDB::getGridFS) —
        Fetches toolkit for dealing with files stored in this database
    -   [MongoDB::getProfilingLevel](/book/mongo.html#MongoDB::getProfilingLevel)
        — Gets this database's profiling level
    -   [MongoDB::getReadPreference](/book/mongo.html#MongoDB::getReadPreference)
        — Get the read preference for this database
    -   [MongoDB::getSlaveOkay](/book/mongo.html#MongoDB::getSlaveOkay)
        — Get slaveOkay setting for this database
    -   [MongoDB::getWriteConcern](/book/mongo.html#MongoDB::getWriteConcern)
        — Get the write concern for this database
    -   [MongoDB::lastError](/book/mongo.html#MongoDB::lastError) —
        Check if there was an error on the most recent db operation
        performed
    -   [MongoDB::listCollections](/book/mongo.html#MongoDB::listCollections)
        — Gets an array of MongoCollection objects for all collections
        in this database
    -   [MongoDB::prevError](/book/mongo.html#MongoDB::prevError) —
        Checks for the last error thrown during a database operation
    -   [MongoDB::repair](/book/mongo.html#MongoDB::repair) — Repairs
        and compacts this database
    -   [MongoDB::resetError](/book/mongo.html#MongoDB::resetError) —
        Clears any flagged errors on the database
    -   [MongoDB::selectCollection](/book/mongo.html#MongoDB::selectCollection)
        — Gets a collection
    -   [MongoDB::setProfilingLevel](/book/mongo.html#MongoDB::setProfilingLevel)
        — Sets this database's profiling level
    -   [MongoDB::setReadPreference](/book/mongo.html#MongoDB::setReadPreference)
        — Set the read preference for this database
    -   [MongoDB::setSlaveOkay](/book/mongo.html#MongoDB::setSlaveOkay)
        — Change slaveOkay setting for this database
    -   [MongoDB::setWriteConcern](/book/mongo.html#MongoDB::setWriteConcern)
        — Set the write concern for this database
    -   [MongoDB::\_\_toString](/book/mongo.html#MongoDB::__toString) —
        The name of this database
-   [MongoCollection](/book/mongo.html#MongoCollection) — The
    MongoCollection class
    -   [MongoCollection::aggregate](/book/mongo.html#MongoCollection::aggregate)
        — Perform an aggregation using the aggregation framework
    -   [MongoCollection::aggregateCursor](/book/mongo.html#MongoCollection::aggregateCursor)
        — Execute an aggregation pipeline command and retrieve results
        through a cursor
    -   [MongoCollection::batchInsert](/book/mongo.html#MongoCollection::batchInsert)
        — Inserts multiple documents into this collection
    -   [MongoCollection::\_\_construct](/book/mongo.html#MongoCollection::__construct)
        — 创建一个新的集合
    -   [MongoCollection::count](/book/mongo.html#MongoCollection::count)
        — 返回集合中的文档数量
    -   [MongoCollection::createDBRef](/book/mongo.html#MongoCollection::createDBRef)
        — 创建一个数据库引用
    -   [MongoCollection::createIndex](/book/mongo.html#MongoCollection::createIndex)
        — Creates an index on the specified field(s) if it does not
        already exist
    -   [MongoCollection::deleteIndex](/book/mongo.html#MongoCollection::deleteIndex)
        — Deletes an index from this collection
    -   [MongoCollection::deleteIndexes](/book/mongo.html#MongoCollection::deleteIndexes)
        — 删除集合的所有索引
    -   [MongoCollection::distinct](/book/mongo.html#MongoCollection::distinct)
        — 获取集合里指定键的不同值的列表。
    -   [MongoCollection::drop](/book/mongo.html#MongoCollection::drop)
        — 删除该集合
    -   [MongoCollection::ensureIndex](/book/mongo.html#MongoCollection::ensureIndex)
        — Creates an index on the specified field(s) if it does not
        already exist
    -   [MongoCollection::find](/book/mongo.html#MongoCollection::find)
        — 查询该集合，并返回结果集的 MongoCursor
    -   [MongoCollection::findAndModify](/book/mongo.html#MongoCollection::findAndModify)
        — Update a document and return it
    -   [MongoCollection::findOne](/book/mongo.html#MongoCollection::findOne)
        — Queries this collection, returning a single element
    -   [MongoCollection::\_\_get](/book/mongo.html#MongoCollection::__get)
        — Gets a collection
    -   [MongoCollection::getDBRef](/book/mongo.html#MongoCollection::getDBRef)
        — Fetches the document pointed to by a database reference
    -   [MongoCollection::getIndexInfo](/book/mongo.html#MongoCollection::getIndexInfo)
        — Returns information about indexes on this collection
    -   [MongoCollection::getName](/book/mongo.html#MongoCollection::getName)
        — 返回这个集合的名称
    -   [MongoCollection::getReadPreference](/book/mongo.html#MongoCollection::getReadPreference)
        — Get the read preference for this collection
    -   [MongoCollection::getSlaveOkay](/book/mongo.html#MongoCollection::getSlaveOkay)
        — Get slaveOkay setting for this collection
    -   [MongoCollection::getWriteConcern](/book/mongo.html#MongoCollection::getWriteConcern)
        — Get the write concern for this collection
    -   [MongoCollection::group](/book/mongo.html#MongoCollection::group)
        — Performs an operation similar to SQL's GROUP BY command
    -   [MongoCollection::insert](/book/mongo.html#MongoCollection::insert)
        — 插入文档到集合中
    -   [MongoCollection::parallelCollectionScan](/book/mongo.html#MongoCollection::parallelCollectionScan)
        — Returns an array of cursors to iterator over a full collection
        in parallel
    -   [MongoCollection::remove](/book/mongo.html#MongoCollection::remove)
        — 从集合中删除记录
    -   [MongoCollection::save](/book/mongo.html#MongoCollection::save)
        — 保存一个文档到集合
    -   [MongoCollection::setReadPreference](/book/mongo.html#MongoCollection::setReadPreference)
        — Set the read preference for this collection
    -   [MongoCollection::setSlaveOkay](/book/mongo.html#MongoCollection::setSlaveOkay)
        — Change slaveOkay setting for this collection
    -   [MongoCollection::setWriteConcern](/book/mongo.html#MongoCollection::setWriteConcern)
        — Set the write concern for this database
    -   [MongoCollection::toIndexString](/book/mongo.html#MongoCollection::toIndexString)
        — Converts keys specifying an index to its identifying string
    -   [MongoCollection::\_\_toString](/book/mongo.html#MongoCollection::__toString)
        — String representation of this collection
    -   [MongoCollection::update](/book/mongo.html#MongoCollection::update)
        — Update records based on a given criteria
    -   [MongoCollection::validate](/book/mongo.html#MongoCollection::validate)
        — Validates this collection
-   [MongoCursor](/book/mongo.html#MongoCursor) — The MongoCursor class
    -   [MongoCursor::addOption](/book/mongo.html#MongoCursor::addOption)
        — Adds a top-level key/value pair to a query
    -   [MongoCursor::awaitData](/book/mongo.html#MongoCursor::awaitData)
        — Sets whether this cursor will wait for a while for a tailable
        cursor to return more data
    -   [MongoCursor::batchSize](/book/mongo.html#MongoCursor::batchSize)
        — Limits the number of elements returned in one batch
    -   [MongoCursor::\_\_construct](/book/mongo.html#MongoCursor::__construct)
        — Create a new cursor
    -   [MongoCursor::count](/book/mongo.html#MongoCursor::count) —
        Counts the number of results for this query
    -   [MongoCursor::current](/book/mongo.html#MongoCursor::current) —
        Returns the current element
    -   [MongoCursor::dead](/book/mongo.html#MongoCursor::dead) — Checks
        if there are results that have not yet been sent from the
        database
    -   [MongoCursor::doQuery](/book/mongo.html#MongoCursor::doQuery) —
        Execute the query
    -   [MongoCursor::explain](/book/mongo.html#MongoCursor::explain) —
        Return an explanation of the query, often useful for
        optimization and debugging
    -   [MongoCursor::fields](/book/mongo.html#MongoCursor::fields) —
        Sets the fields for a query
    -   [MongoCursor::getNext](/book/mongo.html#MongoCursor::getNext) —
        Advances the cursor to the next result, and returns that result
    -   [MongoCursor::getReadPreference](/book/mongo.html#MongoCursor::getReadPreference)
        — Get the read preference for this query
    -   [MongoCursor::hasNext](/book/mongo.html#MongoCursor::hasNext) —
        Checks if there are any more elements in this cursor
    -   [MongoCursor::hint](/book/mongo.html#MongoCursor::hint) — Gives
        the database a hint about the query
    -   [MongoCursor::immortal](/book/mongo.html#MongoCursor::immortal)
        — Sets whether this cursor will timeout
    -   [MongoCursor::info](/book/mongo.html#MongoCursor::info) — Gets
        information about the cursor's creation and iteration
    -   [MongoCursor::key](/book/mongo.html#MongoCursor::key) — Returns
        the current result's \_id, or its index within the result set
    -   [MongoCursor::limit](/book/mongo.html#MongoCursor::limit) —
        Limits the number of results returned
    -   [MongoCursor::maxTimeMS](/book/mongo.html#MongoCursor::maxTimeMS)
        — Sets a server-side timeout for this query
    -   [MongoCursor::next](/book/mongo.html#MongoCursor::next) —
        Advances the cursor to the next result, and returns that result
    -   [MongoCursor::partial](/book/mongo.html#MongoCursor::partial) —
        If this query should fetch partial results from mongos if a
        shard is down
    -   [MongoCursor::reset](/book/mongo.html#MongoCursor::reset) —
        Clears the cursor
    -   [MongoCursor::rewind](/book/mongo.html#MongoCursor::rewind) —
        Returns the cursor to the beginning of the result set
    -   [MongoCursor::setFlag](/book/mongo.html#MongoCursor::setFlag) —
        Sets arbitrary flags in case there is no method available the
        specific flag
    -   [MongoCursor::setReadPreference](/book/mongo.html#MongoCursor::setReadPreference)
        — Set the read preference for this query
    -   [MongoCursor::skip](/book/mongo.html#MongoCursor::skip) — Skips
        a number of results
    -   [MongoCursor::slaveOkay](/book/mongo.html#MongoCursor::slaveOkay)
        — Sets whether this query can be done on a secondary
        \[deprecated\]
    -   [MongoCursor::snapshot](/book/mongo.html#MongoCursor::snapshot)
        — Use snapshot mode for the query
    -   [MongoCursor::sort](/book/mongo.html#MongoCursor::sort) — Sorts
        the results by given fields
    -   [MongoCursor::tailable](/book/mongo.html#MongoCursor::tailable)
        — Sets whether this cursor will be left open after fetching the
        last results
    -   [MongoCursor::timeout](/book/mongo.html#MongoCursor::timeout) —
        Sets a client-side timeout for this query
    -   [MongoCursor::valid](/book/mongo.html#MongoCursor::valid) —
        Checks if the cursor is reading a valid result
-   [MongoCursorInterface](/book/mongo.html#MongoCursorInterface) — The
    MongoCursorInterface interface
    -   [MongoCursorInterface::batchSize](/book/mongo.html#MongoCursorInterface::batchSize)
        — Limits the number of elements returned in one batch
    -   [MongoCursorInterface::dead](/book/mongo.html#MongoCursorInterface::dead)
        — Checks if there are results that have not yet been sent from
        the database
    -   [MongoCursorInterface::getReadPreference](/book/mongo.html#MongoCursorInterface::getReadPreference)
        — Get the read preference for this query
    -   [MongoCursorInterface::info](/book/mongo.html#MongoCursorInterface::info)
        — Gets information about the cursor's creation and iteration
    -   [MongoCursorInterface::setReadPreference](/book/mongo.html#MongoCursorInterface::setReadPreference)
        — Set the read preference for this query
    -   [MongoCursorInterface::timeout](/book/mongo.html#MongoCursorInterface::timeout)
        — Sets a client-side timeout for this query
-   [MongoCommandCursor](/book/mongo.html#MongoCommandCursor) — The
    MongoCommandCursor class
    -   [MongoCommandCursor::batchSize](/book/mongo.html#MongoCommandCursor::batchSize)
        — Limits the number of elements returned in one batch
    -   [MongoCommandCursor::\_\_construct](/book/mongo.html#MongoCommandCursor::__construct)
        — Create a new command cursor
    -   [MongoCommandCursor::createFromDocument](/book/mongo.html#MongoCommandCursor::createFromDocument)
        — Create a new command cursor from an existing command response
        document
    -   [MongoCommandCursor::current](/book/mongo.html#MongoCommandCursor::current)
        — Returns the current element
    -   [MongoCommandCursor::dead](/book/mongo.html#MongoCommandCursor::dead)
        — Checks if there are results that have not yet been sent from
        the database
    -   [MongoCommandCursor::getReadPreference](/book/mongo.html#MongoCommandCursor::getReadPreference)
        — Get the read preference for this command
    -   [MongoCommandCursor::info](/book/mongo.html#MongoCommandCursor::info)
        — Gets information about the cursor's creation and iteration
    -   [MongoCommandCursor::key](/book/mongo.html#MongoCommandCursor::key)
        — Returns the current result's index within the result set
    -   [MongoCommandCursor::next](/book/mongo.html#MongoCommandCursor::next)
        — Advances the cursor to the next result
    -   [MongoCommandCursor::rewind](/book/mongo.html#MongoCommandCursor::rewind)
        — Executes the command and resets the cursor to the start of the
        result set
    -   [MongoCommandCursor::setReadPreference](/book/mongo.html#MongoCommandCursor::setReadPreference)
        — Set the read preference for this command
    -   [MongoCommandCursor::timeout](/book/mongo.html#MongoCommandCursor::timeout)
        — Sets a client-side timeout for this command
    -   [MongoCommandCursor::valid](/book/mongo.html#MongoCommandCursor::valid)
        — Checks if the cursor is reading a valid result

**Warning**

This extension is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used.

核心类是该驱动最重要的部分。

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\Driver\\Manager</span>

简介
----

PHP 和 MongoDB 的连接管理器。

这个类用于创建和管理连接。典型的用法：

**示例 \#1 <span class="classname">MongoClient</span> 基本用法**

``` php
<?php

$m = new MongoClient(); // 连接
$db = $m->foo; // 获取名称为 "foo" 的数据库

?>
```

关于创建连接的更多信息，参见 <span
class="function">MongoClient::\_\_construct</span> 和
<a href="/book/mongo.html#链接服务器" class="link">connecting</a>
的章节。

类摘要
------

**MongoClient**

<span class="ooclass"> class **MongoClient** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::VERSION` ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::DEFAULT_HOST` <span class="initializer"> =
"localhost"</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoClient::DEFAULT_PORT` <span class="initializer"> = 27017</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::RP_PRIMARY` <span class="initializer"> = "primary"</span>
;

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::RP_PRIMARY_PREFERRED` <span class="initializer"> =
"primaryPreferred"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::RP_SECONDARY` <span class="initializer"> =
"secondary"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::RP_SECONDARY_PREFERRED` <span class="initializer"> =
"secondaryPreferred"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoClient::RP_NEAREST` <span class="initializer"> = "nearest"</span>
;

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">boolean</span>
`$connected` <span class="initializer"> = **`FALSE`**</span> ;

<span class="modifier">public</span> <span class="type">string</span>
`$status` <span class="initializer"> = **`NULL`**</span> ;

<span class="modifier">protected</span> <span class="type">string</span>
`$server` <span class="initializer"> = **`NULL`**</span> ;

<span class="modifier">protected</span> <span
class="type">boolean</span> `$persistent` <span class="initializer"> =
**`NULL`**</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$server`<span
class="initializer"> = "mongodb://localhost:27017"</span></span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array("connect" =\>
**`TRUE`**)</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> (\[ <span
class="methodparam"><span class="type">boolean\|string</span>
`$connection`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">dropDB</span> ( <span class="methodparam"><span
class="type">mixed</span> `$db`</span> )

<span class="modifier">public</span> <span class="type">MongoDB</span>
<span class="methodname">\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$dbname`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getConnections</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getHosts</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getWriteConcern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">killCursor</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_hash`</span> , <span class="methodparam"><span
class="type">int\|MongoInt64</span> `$id`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">listDBs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">selectCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span class="type">string</span>
`$collection`</span> )

<span class="modifier">public</span> <span class="type">MongoDB</span>
<span class="methodname">selectDB</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

MongoClient 常量
----------------

**`MongoClient::VERSION`**  
<span class="simpara"> PHP 驱动版本。有可能附加 "dev"，"+" 或 "-"
如果是在两个版本之间。 </span>

**`MongoClient::DEFAULT_HOST`**  
**`"localhost"`**  
<span class="simpara"> 如果没有指定主机，默认连接该主机。 </span>

**`MongoClient::DEFAULT_PORT`**  
**`27017`**  
<span class="simpara"> 如果没有指定端口，默认连接该端口。 </span>

**`MongoClient::RP_PRIMARY`**  
**`"primary"`**  
<span class="simpara">
副本集活跃节点的<a href="/book/mongo.html#读取首选项" class="link">读取选项</a>。
</span>

**`MongoClient::RP_PRIMARY_PREFERRED`**  
**`"primaryPreferred"`**  
<span class="simpara">
副本集活跃节点的<a href="/book/mongo.html#读取首选项" class="link">读取选项</a>。
</span>

**`MongoClient::RP_SECONDARY`**  
**`"secondary"`**  
<span class="simpara">
副本集备份节点的<a href="/book/mongo.html#读取首选项" class="link">读取选项</a>。
</span>

**`MongoClient::RP_SECONDARY_PREFERRED`**  
**`"secondaryPreferred"`**  
<span class="simpara">
副本集备份节点的<a href="/book/mongo.html#读取首选项" class="link">读取选项</a>。
</span>

**`MongoClient::RP_NEAREST`**  
**`"nearest"`**  
<span class="simpara">
副本集最近节点的<a href="/book/mongo.html#读取首选项" class="link">读取选项</a>。
</span>

字段属性
--------

`connected`  
如果我们有一个打开的数据库连接，将会被设置为 **`TRUE`**，否则是
**`FALSE`**。 如果连接副本集（replica
set）里一个节点并匹配当前的读取选项 ，该属性仅会是 **`TRUE`**。
这个属性不考虑账户是否已认证。

版本 1.5.0 后该属性已经废弃（ *deprecated*）。

`status`  
这个属性不会再被使用，将会被设置为 **`NULL`** 在驱动版本 1.1.x
及更早版本中，使用持久连接时这可能会被设置为字符串的值(比如
*"recycled"*， *"new"*)。

版本 1.5.0 后该属性已经废弃（ *deprecated*）。

参见
----

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <a href="/book/mongo.html#Write%20Concerns" class="xref"></a>
-   <a href="/book/mongo.html#链接服务器" class="xref"></a>
-   关于
    <a href="https://docs.mongodb.com/manual/reference/connection-string/" class="link external">» connecting</a>
    的 MongoDB 核心文档

MongoClient::close
==================

关闭连接

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::close</span> (\[ <span
class="methodparam"><span class="type">boolean\|string</span>
`$connection`</span> \] )

<span class="function">MongoClient::close</span>
方法强制关闭一个数据库连接，哪怕使用的是持久连接。
在正常情况下，你*绝不*需要这么做。

### 参数

`connection`  
如果没有指定 connection，或者是
**`FALSE`**，将会选择关闭写作操作的连接。
如果配置为单节点，将会关闭整个连接，但是如果你连接到一个集群， close()
会*仅仅*关闭 primary 节点的连接。

如果 connection 是 **`TRUE`**，连接管理器将会关闭所有由它管理的连接。
这也会包括创建对象时所引用的连接字符串之外的连接。

如果 connection 是一个字符串参数，它将仅仅关闭由该 hash 标识的连接。
Hash 是调用 <span class="function">MongoClient::getConnections</span>
所返回，能够表示一个连接。

### 返回值

返回连接是否成功关闭。

### 范例

**示例 \#1 <span class="function">MongoClient::close</span> 例子**

这个例子演示了如何选择性地仅关闭备份节点的所有连接。

``` php
<?php
// 连接到集群
$a = new MongoClient("mongodb://whisky:13000/?replicaset=seta");

$connections = $a->getConnections();

foreach ( $connections as $con )
{
    // 遍历所有连接，如果类型是 "SECONDARY" 则关闭连接
    if ( $con['connection']['connection_type_desc'] == "SECONDARY" )
    {
        echo "Closing '{$con['hash']}': ";
        $closed = $a->close( $con['hash'] );
        echo $closed ? "ok" : "failed", "\n";
    }
}
?>
```

以上例程会输出：

    Closing 'whisky:13001;X;4948': ok

### 更新日志

| 版本  | 说明                                                                                                                                                                                   |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | 在 1.3.0 版本中，为这个函数添加了 `connection` 参数。 在此之前，直邮写入连接才会被这个方法关闭。                                                                                       |
| 1.2.0 | 在版本 1.2.0 之前，这个驱动默认不会使用持久连接，所有连接会在作用域结束时关闭。 由于版本 1.2.0 情况不再如此，所以调用 close 会是一个坏主意，在服务器有较高负载时可能会造成更高的压力。 |

### 参见

-   <span class="function">MongoClient::getConnections</span>

MongoClient::connect
====================

连接到数据库服务器

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::connect</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

连接是否成功。

### 错误／异常

如果连接失败将会抛出 <span
class="classname">MongoConnectionException</span> 的异常。

MongoClient::\_\_construct
==========================

创建一个新的数据库连接对象

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoClient::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$server`<span
class="initializer"> = "mongodb://localhost:27017"</span></span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array("connect" =\>
**`TRUE`**)</span></span> \]\] )

如果没有传入参数，它会连接到 "localhost:27017"（或者 php.ini 里指定的
<a href="/book/mongo.html#" class="link">mongo.default_host</a> 和
<a href="/book/mongo.html#" class="link">mongo.default_port</a>）。

`server` 应该是这样的形式：

    mongodb://[username:password@]host1[:port1][,host2[:port2:],...]/db

连接字符串总是以 *mongodb://* 开头，表示它是一个连接字符串。

如果指定了 *username* 和
*password*，构造器会在返回前尝试验证连接数据库。
用户名和密码是可选的，需要指定时必须紧随一个 *@*。

至少指定一个主机（端口可选，默认总是
27017），并且可以连接到想要数量的主机。
主机名由逗号分隔，构造器会成功返回，如果连接到了至少一个主机。
如果无法连接到任何主机，它将会抛出一个异常 <span
class="classname">MongoConnectionException</span>。

如果你指定了一个用户名和密码，你可以指定一个要验证的数据库。
如果没有指定 *db*，将会使用 "admin"。

可选的查询字符串可以用于指定额外的选项。 同样参数也支持 `options` 数组。

选项的一部分指示了驱动在集群环境下对备份节点如何读取。
关于读取首选项运行的额外信息可以查找
<a href="/book/mongo.html#读取首选项" class="link">读取首选项</a>
文档页面。

### 参数

`server`  
服务器名。

`options`  
此连接的数组选项。当前有效的选项包括了：

-   *"connect"*

    构造器是否应该在返回前连接。 默认为 **`TRUE`**。当设置为
    **`FALSE`**，驱动会在有查询必要时 *自动* 连接到服务器。
    另外，你也可以用 <span class="function">MongoClient::connect</span>
    手动运行。

    **Warning**
    这个选项不支持通过连接字符串来设置。

-   *"db"*

    要验证的数据库能在这里指定，而不是在主机列表中包含它。
    能够重载主机列表中指定的数据库。

-   *"password"*

    能在这里指定密码，而不是在主机列表中指定。 当密码里有一个 "@"
    的时候尤其有用。 此参数会覆盖主机列表中设置的密码。

-   *"readPreference"*

    指定读取首选项类型。 读取首选项提供了对备份数据读取的控制。

    允许的值有： **`MongoClient::RP_PRIMARY`**、
    **`MongoClient::RP_PRIMARY_PREFERRED`**、
    **`MongoClient::RP_SECONDARY`**、
    **`MongoClient::RP_SECONDARY_PREFERRED`** 和
    **`MongoClient::RP_NEAREST`**。

    更多信息参见<a href="/book/mongo.html#读取首选项" class="link">读取首选项</a>文档。

-   *"readPreferenceTags"*

    以字符串的数组指定读取选项标签。 标签能够控制 *readPreference*
    选项来进一步控制从备份节点数据的读取。

    更多信息参见<a href="/book/mongo.html#读取首选项" class="link">读取首选项</a>文档。

-   *"replicaSet"*

    要连接的集群名称。 如果指定了，活跃节点能够自动检测到。
    这意味着驱动能够最终甚至能够连接到未列出的服务器。
    更多细节参见集群的例子。

-   *"connectTimeoutMS"*

    打开连接超时的时间。

-   *"timeout"*

    "connectTimeoutMS" 废弃的别名。

-   *"socketTimeoutMS"*

    在套接字上发送或接收超时的时间。

    > **Note**: <span class="simpara"> 这是客户端的超时时间。如果一个
    > *insert* 达到了 socketTimeoutMS， 将无法得知服务器是否确实已写入。
    > </span>

-   *"username"*

    能在这里指定用户名，而不是在主机列表中指定。
    当用户名包括一个「:」时尤其有用。 它会覆盖主机列表中的设置。

-   *"w"*

    选项 *w* 指定了驱动的
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concern</a>，决定了驱动在写入时阻塞的时间。
    默认值是 *1*。

    此选项适用于单台服务器或者是集群。
    一个正数值控制了在驱动继续之前，有*多少个*节点必须应答写入的指令。
    值 *1* 将让单台服务器或者活跃节点（在集群里）应答写入操作。 值 *3*
    将阻塞驱动直至写入到活跃节点和其他两个备份节点服务器（在集群里）。

    一个字符串的值用于控制考虑 write concerns 的标签集。 *"majority"*
    是特殊用于确保写入操作被应用于大多数（大于 50%）参与的节点。

-   *"wTimeout"*

    此选项用于和 *"w"* 参数组合使用。 它控制了服务器等待多少毫秒来满足
    write concern。 如果超时了，驱动会抛出 <span
    class="classname">MongoCursorException</span> 异常。

### 返回值

返回一个新的数据库连接对象。

### 错误／异常

如果给出的主机都无法连接，将会抛出 <span
class="classname">MongoConnectionException</span> 异常。
如果提供了无效的用户名和密码将会抛出一个 <span
class="classname">MongoConnnectionException</span>。 参见 <span
class="classname">MongoConnectionException</span>
相关文档获取异常发生的原因。

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.3.4</td>
<td><p>添加了 <em>"connectTimeoutMS"</em> 和 <em>"socketTimeoutMS"</em> 选项。</p></td>
</tr>
<tr class="even">
<td>1.3.0</td>
<td><p>添加了 <em>"readPreference"</em>、 <em>"readPreferenceTags"</em>、<em>"w"</em> 和 <em>"wTimeout"</em> 选项。</p></td>
</tr>
<tr class="odd">
<td>1.2.0</td>
<td><p>添加了 <em>"username"</em> 和 <em>"password"</em> 选项。</p>
<p>移除了 <em>"persist"</em> 选项，所有的连接都是持久的。它仍旧能够使用，但是不起作用。</p>
<dl>
<dt><code class="parameter">"persist"</code></dt>
<dd><p>是否应该是持久连接。如果设置了，连接会是持久连接。 字符形式的值将会用于连接的 ID。所以两个以 <em>array("persist" =&gt; "foobar")</em> 初始化的 <span class="classname">MongoClient</span> 实例会共享一个数据库连接，以 <em>array("persist" =&gt; "barbaz")</em>初始化的实例则使用不同的数据库连接。</p>
</dd>
</dl>
<p><em>"replicaSet"</em> 选项现在支持一个字符串，而不是布尔值。</p></td>
</tr>
<tr class="even">
<td>1.0.9</td>
<td>添加了 <em>"replicaSet"</em> 选项。</td>
</tr>
<tr class="odd">
<td>1.0.2</td>
<td><p>修改构造器支持选修数组。在 1.0.2 之前，构造器接受以下参数：</p>
<dl>
<dt><code class="parameter">server</code></dt>
<dd><p>服务器名。</p>
</dd>
<dt><code class="parameter">connect</code></dt>
<dd><p>可选的 boolean 参数指定了构造器是否应该在返回前连接到数据库。默认为 <strong><code>TRUE</code></strong>。</p>
</dd>
<dt><code class="parameter">persistent</code></dt>
<dd><p>连接是否应该是持久的。</p>
</dd>
<dt><code class="parameter">paired</code></dt>
<dd><p>连接是否应该为 paired 模式。</p>
</dd>
</dl></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">MongoClient::\_\_construct</span>
集群例子**

这个例子显示了如何连接本驱动到一个集群。 它假设了有三个服务器的集群：
sf1.example.com、sf2.example.com 和 ny1.example.com。
活跃节点可能是其中任意一个。

``` php
<?php

// 传递逗号分隔的服务器名称列表到构造器
// 注意我们不需要传入集群的所有成员，驱动能够获取完整的列表
$m1 = new MongoClient("mongodb://sf2.example.com,ny1.example.com", array("replicaSet" => "myReplSet"));

?>
```

如果当前活跃节点连接失败，驱动会计算出备用节点服务器作为新的活跃节点，并自动启用该连接。
如果没有指定 *replicaSet*，自动容错移转将无法正常工作。

在驱动连接的集群种子列表里，起码要有一个种子是在线的。

如果你包含的种子位于两个独立的集群，后面的行为将不可预测。

更多关于集群的信息参见<a href="https://docs.mongodb.com/manual/replication/" class="link external">» 核心文档</a>。

**示例 \#2 连接到一个域套接字（domain socket）**

在 1.0.9+ 版本中，你可以使用一个 UNIX 域套接字来连接到一个本地的 MongoDB
实例。 这可能会比使用网络连接稍微快一点。

在版本 1.5.0，MongoDB 服务器会自动打开 /tmp/mongodb-\<port\>.sock
上的套接字。 你可以在连接字符串中指定位置：

``` php
<?php

// MongoDB 服务器运行在本地 20000 端口上
$m = new MongoClient("mongodb:///tmp/mongodb-20000.sock");

?>
```

你也可以和其他想要的连接组合：

``` php
<?php

// 尝试连接到套接字，失败时使用 localhost 连接
$m = new MongoClient("mongodb:///tmp/mongodb-27017.sock,localhost:27017");

?>
```

**示例 \#3 <span class="function">MongoClient::\_\_construct</span>
验证的例子**

在尝试验证时，用户必须存在于 admin 数据库。 你可以通过终端，用 Mongo
创建一个：

    > use admin
    switched to db admin
    > db.addUser("testUser", "testPass");
    {
            "_id" : ObjectId("4b21272fd9ab21611d19095c"),
            "user" : "testUser",
            "pwd" : "03b9b27e0abf1865e2f6fcbd9845dd59"
    }
    >

创建一个用户后，上面的例子里用户名为 "testUser" 并且密码为
"testPass"，你可以创建一个验证后的连接：

``` php
<?php

$m = new MongoClient("mongodb://testUser:testPass@localhost");

?>
```

**示例 \#4 <span class="function">MongoClient::\_\_construct</span>
读取选项例子**

``` php
<?php

// 首选 "east" 数据中心最近的服务器
$uri  = 'mongodb://rs1.example.com,rs2.example.com/';
$uri .= '?readPreference=nearest';
$uri .= '&readPreferenceTags=dc:east';
$m = new MongoClient($uri, array('replicaSet' => 'rs'));
```

更多信息参见本手册中<a href="/book/mongo.html#读取首选项" class="link">读取选项</a>一节。

MongoClient::dropDB
===================

删除一个数据库 \[已废弃\]

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension, but
there is an alternative in the
<a href="/set/mongodb.html#Architecture" class="link">PHP library</a>:

-   <a href="https://docs.mongodb.com/php-library/master/reference/method/MongoDBClient-dropDatabase/" class="link external">» MongoDB\Client::dropDatabase()</a>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::dropDB</span> ( <span
class="methodparam"><span class="type">mixed</span> `$db`</span> )

**Warning**

请使用 <span class="function">MongoDB::drop</span> 作为替代。

### 参数

`db`  
要函数的数据库。可以是一个 MongoDB对象，或者是数据库名。

### 返回值

返回数据库的回应。

MongoClient::\_\_get
====================

取得一个数据库

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension, but
there is an alternative in the
<a href="/set/mongodb.html#Architecture" class="link">PHP library</a>:

-   <a href="https://docs.mongodb.com/php-library/master/reference/method/MongoDBClient__get/" class="link external">» MongoDB\Client::__get()</a>

### 说明

<span class="modifier">public</span> <span class="type">MongoDB</span>
<span class="methodname">MongoClient::\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$dbname`</span> )

这是获取一个数据库最简洁的方法。
如果数据库名称包含任意特殊字符，需要使用 <span
class="function">MongoClient::selectDB</span>
方法；但是大多数情况下这个方法就可以。

``` php
<?php

$mongo = new MongoClient();

// 以下两行是一样的
$db = $mongo->selectDB("foo");
$db = $mongo->foo;

?>
```

### 参数

`dbname`  
数据库名

### 返回值

返回一个新的 db 对象。

### 错误／异常

如果数据库名无效，将会抛出异常。

MongoClient::getConnections
===========================

返回所有已打开连接的信息

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">MongoClient::getConnections</span> ( <span
class="methodparam">void</span> )

返回所有已打开连接的数组，并且每个服务器的信息

### 参数

此函数没有参数。

### 返回值

打开连接的一个 <span class="type">array</span>。

### 范例

**示例 \#1 <span class="methodname">MongoClient::getConnections</span>
例子**

``` php
<?php
$m = new MongoClient;
var_dump($m->getConnections());
?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      array(3) {
        ["hash"]=>
        string(26) "localhost:27017;-;X;56052"
        ["server"]=>
        array(3) {
          ["host"]=>
          string(10) "localhost"
          ["port"]=>
          int(27017)
          ["pid"]=>
          int(56052)
        }
        ["connection"]=>
        array(8) {
          ["last_ping"]=>
          int(1354076401)
          ["last_ismaster"]=>
          int(0)
          ["ping_ms"]=>
          int(0)
          ["connection_type"]=>
          int(1)
          ["connection_type_desc"]=>
          string(10) "STANDALONE"
          ["max_bson_size"]=>
          int(16777216)
          ["tag_count"]=>
          int(0)
          ["tags"]=>
          array(0) {
          }
        }
      }
    }

MongoClient::getHosts
=====================

更新所有关联主机的状态信息

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this method include:

-   <span class="methodname">MongoDB\\Driver\\Manager::getServers</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::getHosts</span> ( <span
class="methodparam">void</span> )

此方法仅在连接到副本集时有用。
它返回了集群里所有主机的状态。如果没有副本集，它只返回一个元素的数组，包含你当前连接的主机。

参见手册中<a href="/book/mongo.html#Querying" class="link">查询一节</a>关于分布式查询备份节点的信息。

### 参数

此函数没有参数。

### 返回值

返回集群中主机的信息数组。 包含了每个主机的主机名，它的健康程度（1
是很健康），它的状态（1 是活跃节点，2 是备用节点，0 是其他），ping
服务器所需的时间，以及最后一次 ping 的时间。
例如，在具有三个成员的集群中，它看上去可能是这样的：

``` returnvalues
array(3) {
  ["A:27017"]=>
  array(4) {
    ["host"]=>
    "A"
    ["port"]=>
    27017
    ["health"]=>
    int(1)
    ["state"]=>
    int(2)
    ["ping"]=>
    int(369)
    ["lastPing"]=>
    int(1309470644)
  }
  ["B:27017"]=>
  array(4) {
    ["host"]=>
    "B"
    ["port"]=>
    27017
    ["health"]=>
    int(1)
    ["state"]=>
    int(1)
    ["ping"]=>
    int(139)
    ["lastPing"]=>
    int(1309470644)
  }
  ["C:27017"]=>
  array(4) {
    ["host"]=>
    "C"
    ["port"]=>
    27017
    ["health"]=>
    int(1)
    ["state"]=>
    int(2)
    ["ping"]=>
    int(1012)
    ["lastPing"]=>
    int(1309470644)
  }
}
```

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.2.10</td>
<td><p>对非集群的支持。</p>
<p>返回的数组元素现在也包括了 <em>hostname</em> 和 <em>port</em>。</p></td>
</tr>
</tbody>
</table>

### 参见

-   <span class="function">MongoClient::getConnections</span>

MongoClient::getReadPreference
==============================

获取此连接的读取首选项

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::getReadPreference</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the read preference. The array
contains the values *type* for the string read preference mode
(corresponding to the <span class="classname">MongoClient</span>
constants), and *tagsets* containing a list of all tag set criteria. If
no tag sets were specified, *tagsets* will not be present in the array.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.3 | 返回的值修改为兼容 <span class="methodname">MongoClient::setReadPreference</span>。 *type* 的值从数组改成字符串，删除了 *type\_string*，并且 *tagsets* 现在以键值表示的标签而不是冒号分隔的字符串。 |

### 范例

**示例 \#1 <span
class="methodname">MongoClient::getReadPreference</span> 返回值例子**

``` php
<?php

$m = new MongoClient();
$m->setReadPreference(MongoClient::RP_SECONDARY, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
    array(),
));
var_dump($m->getReadPreference());
?>
```

以上例程会输出：

    array(2) {
      ["type"]=>
      string(9) "secondary"
      ["tagsets"]=>
      array(3) {
        [0]=>
        array(2) {
          ["dc"]=>
          string(4) "east"
          ["use"]=>
          string(9) "reporting"
        }
        [1]=>
        array(1) {
          ["dc"]=>
          string(7) "west"
        }
        [2]=>
        array(0) {
        }
      }
    }

### 参见

-   <a href="/book/mongo.html#读取首选项" class="link">读取首选项</a>的文档。
-   <span class="function">MongoClient::setReadPreference</span>

MongoClient::getWriteConcern
============================

Get the write concern for this connection

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::getWriteConcern</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the write concern. The array
contains the values *w* for an integer acknowledgement level or string
mode, and *wtimeout* denoting the maximum number of milliseconds to wait
for the server to satisfy the write concern.

### 范例

**示例 \#1 <span class="methodname">MongoClient::getWriteConcern</span>
return value example**

``` php
<?php

$mc = new MongoClient('mongodb://localhost:27017', array('wTimeoutMS' => 500));
var_dump($mc->getWriteConcern());

$mc->setWriteConcern(1, 1000);
var_dump($mc->getWriteConcern());
?>
```

以上例程会输出：

    array(2) {
      ["w"]=>
      int(1)
      ["wtimeout"]=>
      int(500)
    }
    array(2) {
      ["w"]=>
      int(1)
      ["wtimeout"]=>
      int(1000)
    }

### 参见

-   The
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    documentation.
-   <span class="function">MongoClient::setWriteConcern</span>

MongoClient::killCursor
=======================

Kills a specific cursor on the server

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::killCursor</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_hash`</span> , <span class="methodparam"><span
class="type">int\|MongoInt64</span> `$id`</span> )

In certain situations it might be needed to kill a cursor on the server.
Usually cursors time out after 10 minutes of inactivity, but it is
possible to create an immortal cursor with <span
class="methodname">MongoCursor::immortal</span> that never times out. In
order to be able to kill such an immortal cursor, you can call this
method with the information supplied by <span
class="methodname">MongoCursor::info</span>.

### 参数

`server_hash`  
The server hash that has the cursor. This can be obtained through <span
class="methodname">MongoCursor::info</span>.

`id`  
The ID of the cursor to kill. You can either supply an <span
class="type">int</span> containing the 64 bit cursor ID, or an object of
the <span class="classname">MongoInt64</span> class. The latter is
necessary on 32 bit platforms (and Windows).

### 返回值

Returns **`TRUE`** if the method attempted to kill a cursor, and
**`FALSE`** if there was something wrong with the arguments (such as a
wrong `server_hash`). The return status does *not reflect* where the
cursor was actually killed as the server does not provide that
information.

### 错误／异常

This method displays a warning if the supplied `server_hash` does not
match up with an existing connection. No attempt to kill a cursor is
attempted in that case either.

### 范例

**示例 \#1 <span class="function">MongoClient::killCursor</span>
example**

This example shows how to connect, do a query, obtain the cursor
information and then kill the cursor.

``` php
<?php
$m = new MongoClient();
$c = $m->testdb->collection;
$cursor = $c->find();
$result = $cursor->next();

// Now the cursor is valid, so we can get the hash and ID out:
$info = $cursor->info();

// Kill the cursor
MongoClient::killCursor( $info['server'], $info['id'] );
?>
```

MongoClient::listDBs
====================

列出所有有效数据库

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension, but
there is an alternative in the
<a href="/set/mongodb.html#Architecture" class="link">PHP library</a>:

-   <a href="https://docs.mongodb.com/php-library/master/reference/method/MongoDBClient-listDatabases/" class="link external">» MongoDB\Client::listDatabases()</a>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::listDBs</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回的关联数组包括了三个字段。 第一个字段是
*databases*，里面包含了一个数组。每个元素对应一个数据库，给出数据库名称、尺寸以及是否为空。
另外两个字段是 *totalSize*（单位为字节 bytes）和
*ok*，如果方法成功运行，它会是 1。

### 范例

**示例 \#1 <span class="methodname">MongoClient::listDBs</span> 例子**

例子演示了如何列出数据库，并返回数据的结构。

``` php
<?php

$mongo = new MongoClient();
$dbs = $mongo->listDBs();
print_r($dbs);

?>
```

以上例程的输出类似于：

    Array
    (
        [databases] => Array
            (
                [0] => Array
                    (
                        [name] => doctrine
                        [sizeOnDisk] => 218103808
                        [empty] =>
                    )
            )

        [totalSize] => 218103808
        [ok] => 1
    )

MongoClient::selectCollection
=============================

获取数据库的文档集

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension, but
there is an alternative in the
<a href="/set/mongodb.html#Architecture" class="link">PHP library</a>:

-   <a href="https://docs.mongodb.com/php-library/master/reference/method/MongoDBClient-selectCollection/" class="link external">» MongoDB\Client::selectCollection()</a>

### 说明

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">MongoClient::selectCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span class="type">string</span>
`$collection`</span> )

### 参数

`db`  
数据库名

`collection`  
文档集名。

### 返回值

返回一个新的文档集对象。

### 错误／异常

如果数据库或文档集名称是无效的，抛出 <span
class="classname">Exception</span>。

### 范例

**示例 \#1 <span class="function">MongoClient::selectCollection</span>
例子**

``` php
<?php
$m = new MongoClient();

$c1 = $m->selectCollection("foo", "bar.baz");
// 就等于
$c2 = $m->selectDB("foo")->selectCollection("bar.baz");

// $c1 和 $c2 现在表示的是同一个文档集
?>
```

MongoClient::selectDB
=====================

获取一个数据库

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension, but
there is an alternative in the
<a href="/set/mongodb.html#Architecture" class="link">PHP library</a>:

-   <a href="https://docs.mongodb.com/php-library/master/reference/method/MongoDBClient-selectDatabase/" class="link external">» MongoDB\Client::selectDatabase()</a>

### 说明

<span class="modifier">public</span> <span class="type">MongoDB</span>
<span class="methodname">MongoClient::selectDB</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

### 参数

`name`  
数据库名。

### 返回值

返回一个新的数据库对象。

### 错误／异常

如果数据库名无效，将会抛出 <span class="classname">Exception</span>。

MongoClient::setReadPreference
==============================

为该连接设置读取选项

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

### 参数

`read_preference`  
The read preference mode: **`MongoClient::RP_PRIMARY`**,
**`MongoClient::RP_PRIMARY_PREFERRED`**,
**`MongoClient::RP_SECONDARY`**,
**`MongoClient::RP_SECONDARY_PREFERRED`**, or
**`MongoClient::RP_NEAREST`**.

`tags`  
An array of zero or more tag sets, where each tag set is itself an array
of criteria used to match tags on replica set members.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** otherwise.

### 错误／异常

Emits **`E_WARNING`** if either parameter is invalid, or if one or more
tag sets are provided with the **`MongoClient::RP_PRIMARY`** read
preference mode.

### 范例

**示例 \#1 <span
class="methodname">MongoClient::setReadPreference</span>
标签集数组语法的例子**

``` php
<?php

$m = new MongoClient();

// 首选最近的 "east" 数据中心的服务器，也用于报告，
// 失败时调用 "west" 数据中心的服务器
$m->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
));
?>
```

### 参见

-   <a href="/book/mongo.html#读取首选项" class="link">读取选修</a>的文档。
-   <span class="function">MongoClient::getReadPreference</span>

MongoClient::setWriteConcern
============================

Set the write concern for this connection

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

### 参数

`w`  
The write concern. This may be an integer denoting the number of servers
required to acknowledge the write, or a string mode (e.g. "majority").

`wtimeout`  
The maximum number of milliseconds to wait for the server to satisfy the
write concern.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** otherwise.

### 错误／异常

Emits **`E_WARNING`** if the *w* parameter is not an integer or string
value.

### 范例

**示例 \#1 <span class="methodname">MongoClient::setWriteConcern</span>
example**

``` php
<?php

$mc = new MongoClient('mongodb://rs1.example.com,rs2.example.com');

// Require that the majority of servers in the replica set acknowledge writes
// within three seconds.
$mc->setWriteConcern('majority', 3000);
?>
```

### 参见

-   The
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    documentation.
-   <span class="function">MongoClient::getWriteConcern</span>

MongoClient::\_\_toString
=========================

该连接的字符串表达方式

This extension that defines this method is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoClient::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回此连接的主机名和端口号。

简介
----

该类的实例用于和数据库进行交互。要获取一个数据库：

**示例 \#1 选择一个数据库**

``` php
<?php

$m = new MongoClient(); // 连接
$db = $m->selectDB("example");

?>
```

数据库名可以用 ASCII 范围内的几乎任何字符。 但是，它们不能包括 "
"、"."，或者是空字符串。 名称 "system" 也是被保留的。

个别特殊但有效的数据库名："null"、"\[x,y\]"、"3"、"\\""、 "/"。

不像集合名，数据库名是可以包含 "$" 的。

类摘要
------

**MongoDB**

<span class="ooclass"> class **MongoDB** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`MongoDB::PROFILING_OFF` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoDB::PROFILING_SLOW` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoDB::PROFILING_ON` <span class="initializer"> = 2</span> ;

/\* Fields \*/

<span class="modifier">public</span> <span class="type">integer</span>
`$w` <span class="initializer"> = 1</span> ;

<span class="modifier">public</span> <span class="type">integer</span>
`$wtimeout` <span class="initializer"> = 10000</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">authenticate</span> ( <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">command</span> ( <span
class="methodparam"><span class="type">array</span> `$command`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoClient</span> `$conn`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">createCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">createDBRef</span> ( <span
class="methodparam"><span class="type">string</span>
`$collection`</span> , <span class="methodparam"><span
class="type">mixed</span> `$document_or_id`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">drop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">dropCollection</span> ( <span
class="methodparam"><span class="type">mixed</span> `$coll`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">execute</span> ( <span
class="methodparam"><span class="type">mixed</span> `$code`</span> \[,
<span class="methodparam"><span class="type">array</span> `$args`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">forceError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">\_\_get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getCollectionInfo</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getCollectionNames</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDBRef</span> ( <span
class="methodparam"><span class="type">array</span> `$ref`</span> )

<span class="modifier">public</span> <span
class="type">MongoGridFS</span> <span
class="methodname">getGridFS</span> (\[ <span class="methodparam"><span
class="type">string</span> `$prefix`<span class="initializer"> =
"fs"</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getProfilingLevel</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getSlaveOkay</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getWriteConcern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">lastError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">listCollections</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">prevError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">repair</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$preserve_cloned_files`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$backup_original_files`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">resetError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">selectCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">setProfilingLevel</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSlaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$ok`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

MongoDB 日志级别
----------------

**`MongoDB::PROFILING_OFF`**  
**`0`**  
<span class="simpara"> 关闭了分析器。 </span>

**`MongoDB::PROFILING_SLOW`**  
**`1`**  
<span class="simpara"> 为慢操作开启了分析器（\>100 ms）。 </span>

**`MongoDB::PROFILING_ON`**  
**`2`**  
<span class="simpara"> 为所有操作开启了分析器。 </span>

字段
----

`w`  
1  
在返回成功之前，复制修改到此数量的服务器。 <span
class="classname">MongoCollection</span> 实例的设置从这里继承。 *w*
仅仅在 MongoDB 服务器版本 1.5.1+ 以及本驱动 1.0.8+ 有效。

*w* 用于你需要调整确认级别时 （<span
class="function">MongoCollection::insert</span>、 <span
class="function">MongoCollection::update</span>、 <span
class="function">MongoCollection::remove</span>、 <span
class="function">MongoCollection::save</span> 和 <span
class="function">MongoCollection::ensureIndex</span> 都支持这个选项）。
默认值（1）情况下，只要数据库有操作就会确认。
如果在复制到从服务器前服务器宕机了，它将可能永久丢失本次操作。
所以，你可以为 *w* 指定一个比一更高的数字，
在返回成功之前确保至少一个从服务器完成了操作。

例如，如果 *w* 是 2，主服务器和一个从服务必须记录了本次操作，
否则驱动会抛出 <span class="classname">MongoCursorException</span>。
它尝试写入总计 *w* 个从服务器 +
主服务器，但是如果其中一个从服务器宕机了，
操作也会失败，并会抛出异常，所以通常 *w=2*
是最安全的（主服务器和一个从服务器）。

`wtimeout`  
10000  
等待 *MongoDB::$w* 复制生效的毫秒数。 <span
class="classname">MongoCollection</span> 实例的设置从这里继承。 *w*
仅仅在 MongoDB 服务器版本 1.5.1+ 并且驱动版本 1.0.8+ 有效。

除非设置了 *wtimeout*，服务器会永久等待复制到 *w* 个服务器。
这个驱动默认会等待 10 秒，你可以修改这个值来改变它的行为。

参见
----

MongoDB 关于
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-database" class="link external">» databases</a>
的核心文档。

MongoDB::authenticate
=====================

登录到数据库

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.
>
> 需要把认证信息放在连接字符串里作为代替。

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::authenticate</span> ( <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> )

此方法能够认证它的连接。
如果数据库服务器开启了认证（默认没有开启），在做任何操作之前你需要登录。

通常情况下，你应该使用 <span
class="function">MongoClient::\_\_construct</span>
内置的参数而不是此方法。
如果你对一个连接验证了，然后在会话期间连接掉了然后重连，你会被重新验证。
如果你用这个方法手动验证，然后连接掉了，你必须在重新连接时手动调用这个方法。

该方法等同于运行：

``` php
<?php

$salted = "${username}:mongo:${password}";
$hash = md5($salted);

$nonce = $db->command(array("getnonce" => 1));

$saltedHash = md5($nonce["nonce"]."${username}${hash}");

$result = $db->command(array("authenticate" => 1,
    "user" => $username,
    "nonce" => $nonce["nonce"],
    "key" => $saltedHash
));

?>
```

当一个连接验证后，它仅能够通过 "logout" 数据库命令来登出：

``` php
<?php

$db->command(array("logout" => 1));

?>
```

### 参数

`username`  
用户名。

`password`  
密码（明文格式）。

### 返回值

返回数据库的响应，如果登录成功，它会返回

``` php
<?php
array("ok" => 1);
?>
```

如果出现了什么错误，它会返回

``` php
<?php
array("ok" => 0, "errmsg" => "auth fails");
?>
```

（"auth fails" 可能是另外的信息，取决于数据库版本和发生了什么错误）。

### 参见

MongoDB 关于
<a href="https://docs.mongodb.com/manual/reference/command/authenticate" class="link external">» authenticate</a>
的核心文档。

### 更新日志

| 版本   | 说明                                                       |
|--------|------------------------------------------------------------|
| 1.2.11 | 使用时产生 **`E_DEPRECATED`**。 请将验证细节传入到构造器。 |

MongoDB::command
================

执行一条 Mongo 指令

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::command</span> ( <span
class="methodparam"><span class="type">array</span> `$command`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

几乎所有不属于CRUD操作的事情都可以通过一条“数据库指令”完成。需要知道数据库的版本？有一条指令可以实现。需要进行一次聚合？有一条指令可以实现。想要提高日志级别？有一条指令可以实现。我想你已经领会到了。

该方法等同于：

``` php
<?php

public function command($data) {
    return $this->selectCollection('$cmd')->findOne($data);
}

?>
```

### 参数

`command`  
要发送的指令

`options`  
该参数是一个具有以下形式的关联数组： *array("optionname" =\>
\<boolean\>, ...)*，现在支持的选项有：

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 1.2.0 | 添加 *options* 参数，和一个选项:*"timeout"*。 |

### 返回值

返回数据库响应。每个响应都不会超过一个文档的大小，也就是不会超过16MB。
结果文档的结构与执行的指令有关,但大部分结果都有 *ok*
字段来表示成功还是失败。以及 *results* 字段包含一个结果文档数组。

### 范例

**示例 \#1 <span class="function">MongoDB::command</span>
"distinct"实例**

查找一个键的所有不重复值

``` php
<?php

$people = $db->people;

$people->insert(array("name" => "Joe", "age" => 4));
$people->insert(array("name" => "Sally", "age" => 22));
$people->insert(array("name" => "Dave", "age" => 22));
$people->insert(array("name" => "Molly", "age" => 87));

$ages = $db->command(array("distinct" => "people", "key" => "age"));

foreach ($ages['values'] as $age) {
    echo "$age\n";
}

?>
```

以上例程的输出类似于：

  
4  
22  
87  

**示例 \#2 <span class="function">MongoDB::command</span>
"distinct"实例**

查找一个键的所有不重复值，并且这些值大于等于18

``` php
<?php

$people = $db->people;

$people->insert(array("name" => "Joe", "age" => 4));
$people->insert(array("name" => "Sally", "age" => 22));
$people->insert(array("name" => "Dave", "age" => 22));
$people->insert(array("name" => "Molly", "age" => 87));

$ages = $db->command(
    array(
        "distinct" => "people",
        "key" => "age", 
        "query" => array("age" => array('$gte' => 18))
    )
);  

foreach ($ages['values'] as $age) {
    echo "$age\n";
}

?>
```

以上例程的输出类似于：

  
22  
87  

**示例 \#3 <span class="function">MongoDB::command</span>
MapReduce实例**

获取所有有type=sale这样的"event"的用户，以及他们分别有几个这样的"event"（注:此处的event是一个集合的名字）

``` php
<?php

// sample event document
$events->insert(array("user_id" => $id, 
    "type" => $type, 
    "time" => new MongoDate(), 
    "desc" => $description));

// construct map and reduce functions
$map = new MongoCode("function() { emit(this.user_id,1); }");
$reduce = new MongoCode("function(k, vals) { ".
    "var sum = 0;".
    "for (var i in vals) {".
        "sum += vals[i];". 
    "}".
    "return sum; }");

$sales = $db->command(array(
    "mapreduce" => "events", 
    "map" => $map,
    "reduce" => $reduce,
    "query" => array("type" => "sale"),
    "out" => array("merge" => "eventCounts")));

$users = $db->selectCollection($sales['result'])->find();

foreach ($users as $user) {
    echo "{$user['_id']} had {$user['value']} sale(s).\n";
}

?>
```

以上例程的输出类似于：

  
User 47cc67093475061e3d9536d2 had 3 sale(s).  
User 49902cde5162504500b45c2c had 14 sale(s).  
User 4af467e4fd543cce7b0ea8e2 had 1 sale(s).  

> **Note**: **使用 <span class="classname">MongoCode</span>**  
>
> 这个例子使用了 <span
> class="classname">MongoCode</span>，它还可以接受一个作用域参数。然而，现在
> MongoDB 还不支持在 MapReduce 中使用它，
> 如果你需要在MapReduce函数里用一个客户端参数，那么你可以在使用MapReduce的时候用“optional
> scope”字段把它们添加到全局作用域中，参考
> <a href="https://docs.mongodb.com/manual/core/map-reduce/" class="link external">» MapReduce文档</a>
> 来获得更多信息。

> **Note**: ***out* 参数**  
>
> 1.8.0以前，*out*
> 参数是可选的，如果你不使用它，MapReduce的结果将被写入一个临时集合里，这个临时集合会在连接关闭后删除。
> 1.8.0以后，*out* 参数是必须的，参考
> <a href="https://docs.mongodb.com/manual/core/map-reduce/" class="link external">» MapReduce documentation</a>
> 来获得更多信息。

**示例 \#4 <span class="function">MongoDB::command</span>
"textSearch"实例**

在MongoDB 2.4以上版本中使用全文检索功能（之前的版本不支持全文检索）。

``` php
<?php
$m = new MongoClient();
$d = $m->demo;
$c = $d->planets;

$c->insert(array("name" => "Mercury", "desc" => "Mercury is the smallest and closest to the Sun"));
$c->insert(array("name" => "Venus", "desc" => "Venus is the second planet from the Sun, orbiting it every 224.7 Earth days."));
$c->insert(array("name" => "Earth", "desc" => "Earth is the the densest of the eight planets in the Solar System."));
$c->insert(array("name" => "Mars", "desc" => "Mars is named after the Roman god of war."));

$c->ensureIndex(array('desc' => 'text'));

$r = $d->command(array("text" => "planets", 'search' => "sun" ));
print_r($r);
?>
```

以上例程的输出类似于：

  
Array  
(  
\[queryDebugString\] =\> sun\|\|\|\|\|\|  
\[language\] =\> english  
\[results\] =\> Array  
(  
\[0\] =\> Array  
(  
\[score\] =\> 0.625  
\[obj\] =\> Array  
(  
\[\_id\] =\> MongoId Object  
(  
\[$id\] =\> 517549d944670a4a5cb3059a  
)  
  
\[name\] =\> Mercury  
\[desc\] =\> Mercury is the smallest and closest to the Sun  
)  
  
)  
  
\[1\] =\> Array  
(  
\[score\] =\> 0.55  
\[obj\] =\> Array  
(  
\[\_id\] =\> MongoId Object  
(  
\[$id\] =\> 517549d944670a4a5cb3059b  
)  
  
\[name\] =\> Venus  
\[desc\] =\> Venus is the second planet from the Sun, orbiting it every
224.7 Earth days.  
)  
  
)  
  
)  
  
\[stats\] =\> Array  
(  
\[nscanned\] =\> 2  
\[nscannedObjects\] =\> 0  
\[n\] =\> 2  
\[nfound\] =\> 2  
\[timeMicros\] =\> 95  
)  
  
\[ok\] =\> 1  
)  

**示例 \#5 <span class="function">MongoDB::command</span>
"geoNear"实例**

这个实例说明了如何使用 geoNear 指令。

``` php
<?php
$m = new MongoClient();
$d = $m->demo;
$c = $d->poiConcat;

$r = $d->command(array(
    'geoNear' => "poiConcat",      // 在 poiConcat 集合中
    'near' => array(-0.08, 51.48), // 搜索 51.48°N, 0.08°E 附近
    'spherical' => true,           // 启用特殊搜索
    'num' => 5,                    // 最多返回5个文档
));
print_r($r);
?>
```

### 参见

-   <span class="methodname">MongoCollection::aggregate</span>
-   <span class="methodname">MongoCollection::findAndModify</span>
-   <span class="methodname">MongoCollection::group</span>

MongoDB 核心文档的
<a href="https://docs.mongodb.com/manual/reference/command/" class="link external">» 数据库指令</a>
，以及这些特定指令的文档
<a href="https://docs.mongodb.com/manual/reference/command/findAndModify/" class="link external">» findAndModify</a>、
<a href="https://docs.mongodb.com/manual/reference/command/getLastError/" class="link external">» getLastError</a>、
<a href="https://docs.mongodb.com/manual/reference/command/repairDatabase/" class="link external">» repairDatabase</a>
（还有很多其他指令，这只是一些例子）

MongoDB::\_\_construct
======================

选择一个数据库

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoDB::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoClient</span> `$conn`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> )

这个方法通常不直接调用。推荐的用法是通过 <span
class="function">MongoClient::\_\_get</span> 或 <span
class="function">MongoClient::selectDB</span> 方法获得对象实例。

如果你确实需要直接调用，可以通过以下方式：

``` php
<?php

$m = new MongoClient();
$db = new MongoDB($m, 'mydbname');

?>
```

但这并不好。下面的方式更加美观：

``` php
<?php

$m = new MongoClient();
$db = $m->mydbname;

// 如果数据库名字有保留的字符：

$db = $m->selectDB('my,db:name');

?>
```

### 参数

<span class="type">MongoClient</span> `conn`  
数据库链接

`name`  
数据库名

### 返回值

返回数据库对象。

### 错误／异常

如果数据库名称无效。抛出一个默认类型的异常

MongoDB::createCollection
=========================

创建一个集合

### 说明

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">MongoDB::createCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

这个方法用于创建一个“有限集合”之类需要特殊参数的集合。它相当于执行

``` php
<?php

$collection = $db->command(array(
    "create" => $name,
    "capped" => $options["capped"],
    "size" => $options["size"],
    "max" => $options["max"],
    "autoIndexId" => $options["autoIndexId"],
));

?>
```

参考 <span class="function">MongoDB::command</span>
了解更多关于数据库指令的信息

### 参数

`name`  
集合的名字

`options`  
一个数组，包含集合的选项，具有以下形式： *array("optionname" =\>
"optionvalue", ...)*
。支持的选项跟MongoDB服务器的版本有关。目前支持的选项有：

`capped`  
这个集合是否是固定大小的。

`size`  
如果是固定大小的，指定它的大小（字节）。

`max`  
如果是固定大小的，指定集合中最多存储多少个文档。

`autoIndexId`  
如果 capped 是 **`TRUE`** 你可以显式定义为 **`FALSE`** 来禁用 自增*\_id*
特性。MongoDB 2.2以前， *autoIndexId* 的默认值是**`FALSE`**。

### 返回值

返回新建的集合对象。

### 范例

**示例 \#1 <span class="function">MongoDB::createCollection</span>
固定大小集合 实例**

固定大小（capped）集合是一种磁盘容量或者文档数量固定的特殊集合。当集合“满了”的时候，最老的文档就会被新文档代替。固定大小集合在类似日志记录的应用中非常有用，比如你需要保留一定量的日志，不用担心它们占用过多的空间。

这个例子建立了一个非常小的日志集合，保存10条日志。

``` php
<?php

$log = $db->createCollection(
    "logger",
    array(
        'capped' => true,
        'size' => 10*1024,
        'max' => 10
    )
);

for ($i = 0; $i < 100; $i++) {
    $log->insert(array("level" => WARN, "msg" => "sample log message #$i", "ts" => new MongoDate()));
}

$msgs = $log->find();

foreach ($msgs as $msg) {
    echo $msg['msg']."\n";
}

?>
```

以上例程的输出类似于：

  
sample log message \#90  
sample log message \#91  
sample log message \#92  
sample log message \#93  
sample log message \#94  
sample log message \#95  
sample log message \#96  
sample log message \#97  
sample log message \#98  
sample log message \#99  

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.4.0</td>
<td><p>1.4.0以前的版本里，所有选项都是这个方法的参数。之前版本这个方法的签名是这样的：</p>
<div class="methodsynopsis dc-description">
<span class="modifier">public</span> <span class="type">MongoCollection</span> <span class="methodname">MongoDB::createCollection</span> ( <span class="methodparam"><span class="type">string</span> <code class="parameter">$name</code></span> [, <span class="methodparam"><span class="type">bool</span> <code class="parameter">$capped</code><span class="initializer"> = <strong><code>FALSE</code></strong></span></span> [, <span class="methodparam"><span class="type">int</span> <code class="parameter">$size</code><span class="initializer"> = 0</span></span> [, <span class="methodparam"><span class="type">int</span> <code class="parameter">$max</code><span class="initializer"> = 0</span></span> ]]] )
</div>
<p>参数的意义与现在版本的 <code class="parameter">options</code> 参数相同。</p></td>
</tr>
</tbody>
</table>

MongoDB::createDBRef
====================

创建数据库引用

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::createDBRef</span> ( <span
class="methodparam"><span class="type">string</span>
`$collection`</span> , <span class="methodparam"><span
class="type">mixed</span> `$document_or_id`</span> )

这个方法是一个创建数据库引用的扩展接口（参考<span
class="classname">MongoDBRef</span>）

### 参数

`collection`  
数据库引用指向的集合

`document_or_id`  
如果是一个数组或对象，它的 *\_id* 字段将被用做引用ID，如果是一个 <span
class="classname">MongoId</span> 对象或简单变量，它本身将作为引用ID。

### 返回值

返回一个数据库引用数组。

如果一个没有 *\_id* 字段的数组作为 *document\_or\_id*
参数，**`NULL`**会被返回。

### 范例

**示例 \#1 <span class="function">MongoDB::createDBRef</span>实例**

演示如何从程序中创建文档的数据库引用。

``` php
<?php

$articles = $db->articles;

$article = array(
 'title' => 'Test article',
 'description' => 'Test article description'
);

$articles->insert($article);
$ref = $db->createDBRef('articles', $article);

print_r($article);
print_r($ref);
?>
```

以上例程的输出类似于：

         Array
         (
             [title] => Test article
             [description] => Test article description
             [_id] => MongoId Object
                 (
                 )

         )
         Array
         (
             [$ref] => articles
             [$id] => MongoId Object
                 (
                 )

         )
         

现在$ref可以被保存到另一个文档中，并在之后通过 <span
class="methodname">MongoDB::getDBRef</span>或 <span
class="methodname">MongoCollection::getDBRef</span> 方法取回。

**示例 \#2 <span class="function">MongoDB::createDBRef</span>实例**

演示如何在程序中值通过一个id创建数据库引用。

``` php
<?php

$id = new MongoId('47cc67093475061e3d9536d2');
$ref = $db->createDBRef('articles', $id);
?>
```

MongoDB::drop
=============

删除数据库

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::drop</span> ( <span
class="methodparam">void</span> )

这个方法删除 (drop) 当前使用的整个数据库。

这相当于执行：

``` php
<?php

public function drop() {
    $this->command(array("dropDatabase" => 1));
}

?>
```

### 参数

此函数没有参数。

### 返回值

返回数据库响应

### 范例

**示例 \#1 <span class="function">MongoDB::drop</span> 例子**

这个实例演示如何删除一个数据库，以及通常的响应。

``` php
<?php

$db = $mongo->foo;
$response = $db->drop();
print_r($response);

?>
```

以上例程的输出类似于：

    Array
    (
        [dropped] => foo.$cmd
        [ok] => 1
    )

MongoDB::dropCollection
=======================

Drops a collection \[deprecated\]

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::dropCollection</span> ( <span
class="methodparam"><span class="type">mixed</span> `$coll`</span> )

**Warning**

Use <span class="function">MongoCollection::drop</span> instead.

*This function leaks memory in version 1.0.7 and earlier!*

### 参数

`coll`  
MongoCollection or name of collection to drop.

### 返回值

Returns the database response.

MongoDB::execute
================

在数据库服务器上运行JavaScript

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::execute</span> ( <span
class="methodparam"><span class="type">mixed</span> `$code`</span> \[,
<span class="methodparam"><span class="type">array</span> `$args`<span
class="initializer"> = array()</span></span> \] )

MongoDB服务器运行着一个JavaScript引擎。这个方法允许在服务器上执行任意JavaScript代码。如果你想要利用较少资源处理大量集合，或者在服务器上处理一些结果集以减少网络传输，那么这个方法会有用。

在服务器运行JavaScript代码会创建一个写锁定，这意味着它锁定了其他操作的执行。在运行一段耗时较长的代码之前，请考虑到这一点。

这是一个数据库指令的包装，它简单的说相当于：

``` php
<?php

public function execute($code, $args) {
    return $this->command(array('$eval' => $code, 'args' => $args));
}

?>
```

如果所执行的代码只有一个语句，且只有一行，MongoDB隐含一个return语句。这允许一些直观的行为，比如下面的例子返回"foo"：

``` php
<?php

$db->execute('"foo";');

?>
```

但是下面这两个例子返回**`NULL`**:

``` php
<?php

$db->execute('"bar"; "foo";'); // 多个语句

$db->execute('db.foo.count(
);'); // 多行

?>
```

为了防止意外的行为，最好不要依赖MongoDB决定你的返回值。而是明确的提供一个return语句。上面的例子中，可以把代码改为：

``` php
<?php

$db->execute('"bar"; return "foo";');

$db->execute('return db.foo.count(
);');

?>
```

这样第一个语句会返回"foo"，第二个语句会返回"foo"集合的长度。

### 参数

`code`  
<span class="classname">MongoCode</span>或要执行的字符串

`args`  
给*code*的参数。

### 返回值

返回执行结果

### 范例

**示例 \#1 简单的 <span class="function">MongoDB::execute</span> 实例**

``` php
<?php

$response = $db->execute("function() { return 'Hello, world!'; }");
echo $response['retval'];

?>
```

以上例程的输出类似于：

  
Hello, world!  

**示例 \#2 带参数的 <span class="function">MongoDB::execute</span>
实例**

可选的参数将被传递给JavaScrip函数

``` php
<?php

$response = $db->execute("function(greeting, name) { return greeting+', '+name+'!'; }", array("Good bye", "Joe"));
echo $response['retval'];

?>
```

以上例程的输出类似于：

  
Good bye, Joe!  

**示例 \#3 作用域实例**

如果使用 <span class="classname">MongoCode</span>
对象代替字符串作为第一个参数。可以传递一个作用域到将要执行的JavaScript中。

``` php
<?php

$func = 
    "function(greeting, name) { ".
        "return greeting+', '+name+', says '+greeter;".
    "}";
$scope = array("greeter" => "Fred");

$code = new MongoCode($func, $scope);

$response = $db->execute($code, array("Goodbye", "Joe"));
echo $response['retval'];

?>
```

以上例程的输出类似于：

  
Goodbye, Joe, says Fred  

MongoDB::forceError
===================

Creates a database error

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoDB::forceError</span> ( <span
class="methodparam">void</span> )

This method is not very useful for normal MongoDB use. It forces a
database error to occur. This means that <span
class="function">MongoDB::lastError</span> will return a generic
database error after running this command.

This command is identical to running:

``` php
<?php

public function forceError() {
    return $this->command(array('forceerror' => 1));
}

?>
```

### 参数

此函数没有参数。

### 返回值

Returns the database response.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

MongoDB::\_\_get
================

Gets a collection

### 说明

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">MongoDB::\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

This is the easiest way of getting a collection from a database object.
If a collection name contains strange characters, you may have to use
<span class="function">MongoDB::selectCollection</span> instead.

``` php
<?php

$mongo = new MongoClient();

// the following two lines are equivalent
$collection = $mongo->selectDB("foo")->selectCollection("bar");
$collection = $mongo->foo->bar;

?>
```

### 参数

`name`  
The name of the collection.

### 返回值

Returns the collection.

MongoDB::getCollectionInfo
==========================

Returns information about collections in this database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::getCollectionInfo</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Gets a list of all collections in the database and returns them as an
array of documents, which contain their names and options.

> **Note**: <span class="simpara">This method will use the
> <a href="https://docs.mongodb.com/manual/reference/command/listCollections" class="link external">» listCollections</a>
> database command when communicating with MongoDB 2.8+. For previous
> database versions, the method will query the special
> *system.namespaces* collection.</span>

### 参数

`options`  
An array of options for listing the collections. Currently available
options include:

-   *"filter"*

    Optional query criteria. If provided, this criteria will be used to
    filter the collections included in the result.

    Relevant fields that may be queried include *"name"* (collection
    name as a string, without the database name prefix) and *"options"
    (object containing options used to create the collection).*.

    > **Note**: <span class="simpara">MongoDB 2.6 and earlier versions
    > require the *"name"* criteria, if specified, to be a string value
    > (i.e. equality match). This is because the driver must prefix the
    > value with the database name in order to query the
    > *system.namespaces* collection. Later versions of MongoDB do not
    > have this limitation, as the driver will use the listCollections
    > command.</span>

-   *"includeSystemCollections"*

    Boolean, defaults to **`FALSE`**. Determines whether system
    collections should be included in the result.

The following option may be used with MongoDB 2.8+:

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

### 返回值

This function returns an array where each element is an array describing
a collection. Elements will contain a *name* key denoting the name of
the collection, and optionally contain an *options* key denoting an
array of objects used to create the collection. For example, capped
collections will include *capped* and *size* options.

### 错误／异常

For MongoDB 2.6 and earlier, <span
class="classname">MongoException</span> will be thrown if a non-string
value was specified for the *"filter"* option's *"name"* criteria.

### 范例

**示例 \#1 <span class="function">MongoDB::getCollectionInfo</span>
example**

``` php
<?php
$m = new MongoClient();
$db = $m->selectDB("demo");
var_dump($db->getCollectionInfo());
?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      array(2) {
        ["name"]=>
        string(4) "logs"
        ["options"]=>
        array(2) {
          ["capped"]=>
          bool(true)
          ["size"]=>
          int(10240)
        }
      }
      [1]=>
      array(2) {
        ["name"]=>
        string(5) "users"
        ["options"]=>
        array(1) {
          ["flags"]=>
          int(1)
        }
      }
    }

### 参见

-   <span class="function">MongoDB::getCollectionNames</span>
-   <span class="function">MongoDB::listCollections</span>

MongoDB::getCollectionNames
===========================

Gets an array of names for all collections in this database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::getCollectionNames</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Gets a list of all collections in the database and returns their names
as an array of strings.

> **Note**: <span class="simpara">This method will use the
> <a href="https://docs.mongodb.com/manual/reference/command/listCollections" class="link external">» listCollections</a>
> database command when communicating with MongoDB 2.8+. For previous
> database versions, the method will query the special
> *system.namespaces* collection.</span>

### 参数

`options`  
An array of options for listing the collections. Currently available
options include:

-   *"filter"*

    Optional query criteria. If provided, this criteria will be used to
    filter the collections included in the result.

    Relevant fields that may be queried include *"name"* (collection
    name as a string, without the database name prefix) and *"options"
    (object containing options used to create the collection).*.

    > **Note**: <span class="simpara">MongoDB 2.6 and earlier versions
    > require the *"name"* criteria, if specified, to be a string value
    > (i.e. equality match). This is because the driver must prefix the
    > value with the database name in order to query the
    > *system.namespaces* collection. Later versions of MongoDB do not
    > have this limitation, as the driver will use the listCollections
    > command.</span>

-   *"includeSystemCollections"*

    Boolean, defaults to **`FALSE`**. Determines whether system
    collections should be included in the result.

The following option may be used with MongoDB 2.8+:

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

### 返回值

Returns the collection names as an array of strings.

### 错误／异常

For MongoDB 2.6 and earlier, <span
class="classname">MongoException</span> will be thrown if a non-string
value was specified for the *"filter"* option's *"name"* criteria.

### 更新日志

| 版本  | 说明                                                                                                                                                |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.6.0 | Changed first parameter to be an array of options. Pre-1.6.0, the first parameter was a boolean indicating the *"includeSystemCollections"* option. |

### 范例

**示例 \#1 <span class="function">MongoDB::getCollectionNames</span>
example**

``` php
<?php
$m = new MongoClient();
$db = $m->selectDB("demo");
$collections = $db->getCollectionNames();

foreach ($collections as $collectionName) {
    echo "Found collection: ", $collectionName, "\n";
}
?>
```

以上例程的输出类似于：

    ...
    Found collection: img
    Found collection: beer
    Found collection: collation
    ...

### 参见

-   <span class="function">MongoDB::listCollections</span>
-   <span class="function">MongoDB::getCollectionInfo</span>

MongoDB::getDBRef
=================

Fetches the document pointed to by a database reference

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::getDBRef</span> ( <span
class="methodparam"><span class="type">array</span> `$ref`</span> )

### 参数

`ref`  
A database reference.

### 返回值

Returns the document pointed to by the reference.

### 范例

**示例 \#1 <span class="function">MongoDB::getDBRef</span> example**

Example demonstrating how to get a database reference and what the
expected input is.

``` php
<?php

 $ref = array(
   '$ref' => 'profiles',
   '$id' => new MongoId('47cc67093475061e3d9536d2')
 );
 
 $profile = $db->getDBRef($ref);
 ?>
```

See <span class="function">MongoDB::createDBRef</span> for more
information about how to programatically create DB references.

MongoDB::getGridFS
==================

Fetches toolkit for dealing with files stored in this database

### 说明

<span class="modifier">public</span> <span
class="type">MongoGridFS</span> <span
class="methodname">MongoDB::getGridFS</span> (\[ <span
class="methodparam"><span class="type">string</span> `$prefix`<span
class="initializer"> = "fs"</span></span> \] )

### 参数

`prefix`  
The prefix for the files and chunks collections.

### 返回值

Returns a new gridfs object for this database.

### 范例

**示例 \#1 <span class="function">MongoDB::getGridFS</span> example**

This example demonstrates how get a MongoGridFS instance.

``` php
<?php

$db = $mongo->my_db;

$prefix = 'files';
$collection = $db->getGridFS($prefix);

?>
```

Read more about the <span class="classname">MongoGridFS</span> to learn
how to store files with MongoDB.

MongoDB::getProfilingLevel
==========================

Gets this database's profiling level

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB::getProfilingLevel</span> ( <span
class="methodparam">void</span> )

This returns the current database profiling level.

The database profiler tracks query execution times. If you turn it on
(say, using <span class="function">MongoDB::setProfilingLevel</span> or
the shell), you can see how many queries took longer than a given number
of milliseconds or the timing for all queries.

Note that profiling slows down queries, so it is better to use in
development or testing than in a time-sensitive application.

This function is equivalent to running:

``` php
<?php

public function getProfilingLevel() {
    return $this->command(array('profile' => -1));
}

?>
```

### 参数

此函数没有参数。

### 返回值

Returns the profiling level.

### 参见

-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/tutorial/manage-the-database-profiler/" class="link external">» profiling</a>
-   <span class="methodname">MongoDB::setProfilingLevel</span>

MongoDB::getReadPreference
==========================

Get the read preference for this database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::getReadPreference</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the read preference. The array
contains the values *type* for the string read preference mode
(corresponding to the <span class="classname">MongoClient</span>
constants), and *tagsets* containing a list of all tag set criteria. If
no tag sets were specified, *tagsets* will not be present in the array.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.3 | The return value has changed to be consistent with <span class="methodname">MongoDB::setReadPreference</span>. The *type* value was changed from a number to a string, *type\_string* was removed, and *tagsets* now expresses tags as key/value pairs instead of colon-delimited strings. |

### 范例

**示例 \#1 <span class="methodname">MongoDB::getReadPreference</span>
return value example**

``` php
<?php

$m = new MongoClient();
$db = $m->test;
$db->setReadPreference(MongoClient::RP_SECONDARY, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
    array(),
));
var_dump($db->getReadPreference());
?>
```

以上例程会输出：

    array(2) {
      ["type"]=>
      string(9) "secondary"
      ["tagsets"]=>
      array(3) {
        [0]=>
        array(2) {
          ["dc"]=>
          string(4) "east"
          ["use"]=>
          string(9) "reporting"
        }
        [1]=>
        array(1) {
          ["dc"]=>
          string(7) "west"
        }
        [2]=>
        array(0) {
        }
      }
    }

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoDB::setReadPreference</span>

MongoDB::getSlaveOkay
=====================

Get slaveOkay setting for this database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoDB::getSlaveOkay</span> ( <span
class="methodparam">void</span> )

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

此函数没有参数。

### 返回值

Returns the value of slaveOkay for this instance.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoDB::getReadPreference</span>
-   <span class="methodname">MongoDB::setReadPreference</span>

MongoDB::getWriteConcern
========================

Get the write concern for this database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::getWriteConcern</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the write concern. The array
contains the values *w* for an integer acknowledgement level or string
mode, and *wtimeout* denoting the maximum number of milliseconds to wait
for the server to satisfy the write concern.

### 范例

**示例 \#1 <span class="methodname">MongoDB::getWriteConcern</span>
return value example**

``` php
<?php

$mc = new MongoClient('mongodb://localhost:27017', array('wTimeoutMS' => 500));
$db = $mc->selectDB('test');
var_dump($db->getWriteConcern());

$db->setWriteConcern(1, 1000);
var_dump($db->getWriteConcern());
?>
```

以上例程会输出：

    array(2) {
      ["w"]=>
      int(1)
      ["wtimeout"]=>
      int(500)
    }
    array(2) {
      ["w"]=>
      int(1)
      ["wtimeout"]=>
      int(1000)
    }

### 参见

-   The
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    documentation.
-   <span class="function">MongoDB::setWriteConcern</span>

MongoDB::lastError
==================

Check if there was an error on the most recent db operation performed

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::lastError</span> ( <span
class="methodparam">void</span> )

This method is equivalent to:

``` php
<?php

public function lastError() {
    return $this->command(array('getlasterror' => 1));
}

?>
```

### 参数

此函数没有参数。

### 返回值

Returns the error, if there was one.

### 范例

**示例 \#1 <span class="function">MongoDB::lastError</span> **`NULL`**
error example**

``` php
<?php
$db->resetError();
var_dump($db->lastError());
?>
```

以上例程的输出类似于：

    array(3) {
      ["err"]=>
      NULL
      ["n"]=>
      int(0)
      ["ok"]=>
      float(1)
    }

**示例 \#2 <span class="function">MongoDB::lastError</span> duplicate
key example**

``` php
<?php
$c = $db->selectCollection("foo");

// insert two documents with the same _id
$c->insert(array("_id" => 1));
$c->insert(array("_id" => 1));

var_dump($db->lastError());
?>
```

以上例程的输出类似于：

    array(3) {
      ["err"]=>
      string(64) "E11000 duplicate key errorindex: foo.foo.$_id_  dup key: { : 1 }"
      ["n"]=>
      int(0)
      ["ok"]=>
      float(1)
    }

MongoDB::listCollections
========================

Gets an array of MongoCollection objects for all collections in this
database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::listCollections</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Gets a list of all collections in the database and returns them as an
array of <span class="classname">MongoCollection</span> objects.

> **Note**: <span class="simpara">This method will use the
> <a href="https://docs.mongodb.com/manual/reference/command/listCollections" class="link external">» listCollections</a>
> database command when communicating with MongoDB 2.8+. For previous
> database versions, the method will query the special
> *system.namespaces* collection.</span>

### 参数

`options`  
An array of options for listing the collections. Currently available
options include:

-   *"filter"*

    Optional query criteria. If provided, this criteria will be used to
    filter the collections included in the result.

    Relevant fields that may be queried include *"name"* (collection
    name as a string, without the database name prefix) and *"options"
    (object containing options used to create the collection).*.

    > **Note**: <span class="simpara">MongoDB 2.6 and earlier versions
    > require the *"name"* criteria, if specified, to be a string value
    > (i.e. equality match). This is because the driver must prefix the
    > value with the database name in order to query the
    > *system.namespaces* collection. Later versions of MongoDB do not
    > have this limitation, as the driver will use the listCollections
    > command.</span>

-   *"includeSystemCollections"*

    Boolean, defaults to **`FALSE`**. Determines whether system
    collections should be included in the result.

The following option may be used with MongoDB 2.8+:

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

### 返回值

Returns an array of MongoCollection objects.

### 错误／异常

For MongoDB 2.6 and earlier, <span
class="classname">MongoException</span> will be thrown if a non-string
value was specified for the *"filter"* option's *"name"* criteria.

### 更新日志

| 版本  | 说明                                                                                                                                                |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.6.0 | Changed first parameter to be an array of options. Pre-1.6.0, the first parameter was a boolean indicating the *"includeSystemCollections"* option. |
| 1.3.0 | Added the `includeSystemCollections` parameter.                                                                                                     |

### 范例

**示例 \#1 <span class="function">MongoDB::listCollections</span>
example**

The following example demonstrates running count on each collection in a
database.

``` php
<?php

$m = new MongoClient();
$db = $m->selectDB("demo");
$collections = $db->listCollections();

foreach ($collections as $collection) {
    echo "amount of documents in $collection: ";
    echo $collection->count(), "\n";
}

?>
```

以上例程的输出类似于：

    ...
    amount of documents in demo.pubs: 4
    amount of documents in demo.elephpants: 3
    amount of documents in demo.cities: 22840
    ...

### 参见

-   <span class="function">MongoDB::getCollectionNames</span>
-   <span class="function">MongoDB::getCollectionInfo</span>

MongoDB::prevError
==================

Checks for the last error thrown during a database operation

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::prevError</span> ( <span
class="methodparam">void</span> )

<span class="function">MongoDB::lastError</span> is usually preferred to
this. This method returns the last database error that occurred and how
many operations ago it occurred. It is mostly deprecated.

### 参数

此函数没有参数。

### 返回值

Returns the error and the number of operations ago it occurred.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

MongoDB::repair
===============

Repairs and compacts this database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::repair</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$preserve_cloned_files`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$backup_original_files`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

This creates a fresh copy of all database data. It will remove any
corrupt data and compact and large stretches of free space it finds.
This is a very slow operation on a large database.

This is usually run from the shell or the command line, not the driver.

It is equivalent to the function:

``` php
<?php

public function repair() {
    return $this->command(array('repairDatabase' => 1));
}

?>
```

### 参数

`preserve_cloned_files`  
If cloned files should be kept if the repair fails.

`backup_original_files`  
If original files should be backed up.

### 返回值

Returns db response.

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/reference/command/repairDatabase" class="link external">» repairDatabase</a>.

### 范例

**示例 \#1 <span class="function">MongoDB::repair</span> example**

This example demonstrates how to repare and compact a database.

``` php
<?php

$db = $mongo->foo;

$response = $db->repair();
print_r($response);

?>
```

以上例程的输出类似于：

    Array
    (
        [ok] => 1
    )

MongoDB::resetError
===================

Clears any flagged errors on the database

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoDB::resetError</span> ( <span
class="methodparam">void</span> )

This method is not used in normal operations. It resets the database
error tracker (which can be incremented with <span
class="function">MongoDB::forceError</span>, also not normally used).

It is equivalent to running:

``` php
<?php

public function resetError() {
    return $this->command(array('reseterror' => 1));
}

?>
```

### 参数

此函数没有参数。

### 返回值

Returns the database response.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

MongoDB::selectCollection
=========================

Gets a collection

### 说明

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">MongoDB::selectCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

### 参数

`name`  
The collection name.

### 返回值

Returns a new collection object.

### 错误／异常

Throws <span class="classname">Exception</span> if the collection name
is invalid.

MongoDB::setProfilingLevel
==========================

Sets this database's profiling level

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB::setProfilingLevel</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

This changes the current database profiling level.

This function is equivalent to running:

``` php
<?php

public function setProfilingLevel($level) {
    return $this->command(array('profile' => $level));
}

?>
```

The options for level are 0 (off), 1 (queries \> 100ms), and 2 (all
queries). If you would like to profile queries that take longer than
another time period, use the database command and pass it a second
option, the number of milliseconds. For example, to profile all queries
that take longer than one second, run:

``` php
<?php

$result = $this->command(array('profile' => 1, 'slowms' => 1000));

?>
```

Profiled queries will appear in the *system.profile* collection of this
database.

### 参数

`level`  
Profiling level.

### 返回值

Returns the previous profiling level.

### 参见

-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/tutorial/manage-the-database-profiler/" class="link external">» profiling</a>
-   <span class="methodname">MongoDB::getProfilingLevel</span>

MongoDB::setReadPreference
==========================

Set the read preference for this database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoDB::setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

### 参数

`read_preference`  
The read preference mode: **`MongoClient::RP_PRIMARY`**,
**`MongoClient::RP_PRIMARY_PREFERRED`**,
**`MongoClient::RP_SECONDARY`**,
**`MongoClient::RP_SECONDARY_PREFERRED`**, or
**`MongoClient::RP_NEAREST`**.

`tags`  
An array of zero or more tag sets, where each tag set is itself an array
of criteria used to match tags on replica set members.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** otherwise.

### 错误／异常

Emits **`E_WARNING`** if either parameter is invalid, or if one or more
tag sets are provided with the **`MongoClient::RP_PRIMARY`** read
preference mode.

### 范例

**示例 \#1 <span class="methodname">MongoDB::setReadPreference</span>
tag set array syntax example**

``` php
<?php

$m = new MongoClient();
$db = $m->test;

// Prefer the nearest server in the "east" data center also used for reporting,
// but fall back to a server in the "west" data center
$db->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
));
?>
```

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoDB::getReadPreference</span>

MongoDB::setSlaveOkay
=====================

Change slaveOkay setting for this database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoDB::setSlaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$ok`<span
class="initializer"> = **`TRUE`**</span></span> \] )

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

`ok`  
If reads should be sent to secondary members of a replica set for all
possible queries using this <span class="classname">MongoDB</span>
instance.

### 返回值

Returns the former value of slaveOkay for this instance.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoDB::setReadPreference</span>
-   <span class="methodname">MongoDB::getReadPreference</span>

MongoDB::setWriteConcern
========================

Set the write concern for this database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoDB::setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

### 参数

`w`  
The write concern. This may be an integer denoting the number of servers
required to acknowledge the write, or a string mode (e.g. "majority").

`wtimeout`  
The maximum number of milliseconds to wait for the server to satisfy the
write concern.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** otherwise.

### 错误／异常

Emits **`E_WARNING`** if the *w* parameter is not an integer or string
value.

### 范例

**示例 \#1 <span class="methodname">MongoDB::setWriteConcern</span>
example**

``` php
<?php

$mc = new MongoClient('mongodb://rs1.example.com,rs2.example.com');
$db = $mc->selectDB('test');

// Require that the majority of servers in the replica set acknowledge writes
// within three seconds.
$db->setWriteConcern('majority', 3000);
?>
```

### 参见

-   The
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    documentation.
-   <span class="function">MongoDB::getWriteConcern</span>

MongoDB::\_\_toString
=====================

The name of this database

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoDB::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns this database's name.

简介
----

Represents a MongoDB collection.

Collection names can use any character in the ASCII set. Some valid
collection names are "", "...", "my collection", and "\*&\#@".

User-defined collection names cannot contain the $ symbol. There are
certain system collections which use a $ in their names (e.g.,
local.oplog.$main), but it is a reserved character. If you attempt to
create and use a collection with a $ in the name, MongoDB will assert.

类摘要
------

**MongoCollection**

<span class="ooclass"> class **MongoCollection** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`MongoCollection::ASCENDING` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoCollection::DESCENDING` <span class="initializer"> = -1</span> ;

/\* Fields \*/

<span class="modifier">public</span> <span class="type">MongoDB</span>
`$db` <span class="initializer"> = **`NULL`**</span> ;

<span class="modifier">public</span> <span class="type">integer</span>
`$w` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$wtimeout` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">aggregate</span> ( <span
class="methodparam"><span class="type">array</span> `$pipeline`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">aggregateCursor</span> ( <span
class="methodparam"><span class="type">array</span> `$command`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">batchInsert</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoDB</span> `$db`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> (\[ <span class="methodparam"><span
class="type">array</span> `$query`<span class="initializer"> =
array()</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$limit`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$skip`<span class="initializer"> =
0</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">createDBRef</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$document_or_id`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">createIndex</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">deleteIndex</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$keys`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">deleteIndexes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">distinct</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">drop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ensureIndex</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$key|keys`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">find</span> (\[
<span class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">findAndModify</span> ( <span
class="methodparam"><span class="type">array</span> `$query`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$update`</span> \[, <span class="methodparam"><span
class="type">array</span> `$fields`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">findOne</span> (\[ <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\]\] )

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">\_\_get</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDBRef</span> ( <span
class="methodparam"><span class="type">array</span> `$ref`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getIndexInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getSlaveOkay</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getWriteConcern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">group</span> ( <span class="methodparam"><span
class="type">mixed</span> `$keys`</span> , <span
class="methodparam"><span class="type">array</span> `$initial`</span> ,
<span class="methodparam"><span class="type">MongoCode</span>
`$reduce`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span class="methodname">insert</span> (
<span class="methodparam"><span class="type">array\|object</span>
`$a`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

<span class="modifier">public</span> <span
class="type">array\[MongoCommandCursor\]</span> <span
class="methodname">parallelCollectionScan</span> ( <span
class="methodparam"><span class="type">int</span> `$num_cursors`</span>
)

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span class="methodname">remove</span>
(\[ <span class="methodparam"><span class="type">array</span>
`$criteria`<span class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">save</span> ( <span class="methodparam"><span
class="type">array\|object</span> `$document`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSlaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$ok`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

<span class="modifier">static protected</span> <span
class="type">string</span> <span class="methodname">toIndexString</span>
( <span class="methodparam"><span class="type">mixed</span>
`$keys`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span class="methodname">update</span> (
<span class="methodparam"><span class="type">array</span>
`$criteria`</span> , <span class="methodparam"><span
class="type">array</span> `$new_object`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">validate</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$scan_data`<span
class="initializer"> = **`FALSE`**</span></span> \] )

}

预定义常量
----------

**`MongoCollection::ASCENDING`**  
<span class="simpara"> Ascending direction for sorts and index creation.
</span>

**`MongoCollection::DESCENDING`**  
<span class="simpara"> Descending direction for sorts and index
creation. </span>

Fields
------

`db`  
The "parent" database for this collection.

`w`  
The number of servers to replicate a change to before returning success.
Value is inherited from the parent database. The <span
class="classname">MongoDB</span> class has a more detailed description
of how *w* works.

`wtimeout`  
The number of milliseconds to wait for *$this-\>w* replications to take
place. Value is inherited from the parent database. The <span
class="classname">MongoDB</span> class has a more detailed description
of how *wtimeout* works.

参见
----

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-collection" class="link external">» collections</a>.

MongoCollection::aggregate
==========================

Perform an aggregation using the aggregation framework

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::aggregate</span> ( <span
class="methodparam"><span class="type">array</span> `$pipeline`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::aggregate</span> ( <span
class="methodparam"><span class="type">array</span> `$op`</span> \[,
<span class="methodparam"><span class="type">array</span> `$op`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$...`</span> \]\] )

The MongoDB
<a href="https://docs.mongodb.com/manual/core/aggregation-pipeline/" class="link external">» aggregation framework</a>
provides a means to calculate aggregated values without having to use
MapReduce. While MapReduce is powerful, it is often more difficult than
necessary for many simple aggregation tasks, such as totaling or
averaging field values.

This method accepts either a variable amount of pipeline operators, or a
single array of operators constituting the pipeline.

### 参数

`pipeline`  
An array of pipeline operators.

`options`  
Options for the aggregation command. Valid options include:

-   *"allowDiskUse"*

    Allow aggregation stages to write to temporary files

-   *"cursor"*

    Options controlling the creation of the cursor object. This option
    causes the command to return a result document suitable for
    constructing a <span class="classname">MongoCommandCursor</span>. If
    you need to use this option, you should consider using <span
    class="methodname">MongoCollection::aggregateCursor</span>.

-   *"explain"*

    Return information on the processing of the pipeline.

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

Or

`op`  
First pipeline operator.

`op`  
The second pipeline operator.

`...`  
Additional pipeline operators.

### 返回值

The result of the aggregation as an array. The `ok` will be set to *1*
on success, *0* on failure.

### 错误／异常

When an error occurs an array with the following keys will be returned:

-   <span class="simpara"> `errmsg` - containing the reason for the
    failure </span>
-   <span class="simpara"> `code` - the errorcode of the failure </span>
-   <span class="simpara"> `ok` - will be set to 0. </span>

### 更新日志

| 版本  | 说明                              |
|-------|-----------------------------------|
| 1.5.0 | Added optional `options` argument |

### 范例

**示例 \#1 <span class="methodname">MongoCollection::aggregate</span>
example**

The following example aggregation operation pivots data to create a set
of author names grouped by tags applied to an article. Call the
aggregation framework by issuing the following command:

``` php
<?php
$m = new MongoClient("localhost");
$c = $m->selectDB("examples")->selectCollection("article");
$data = array (
    'title' => 'this is my title',
    'author' => 'bob',
    'posted' => new MongoDate,
    'pageViews' => 5,
    'tags' => array ( 'fun', 'good', 'fun' ),
    'comments' => array (
      array (
        'author' => 'joe',
        'text' => 'this is cool',
      ),
      array (
        'author' => 'sam',
        'text' => 'this is bad',
      ),
    ),
    'other' =>array (
      'foo' => 5,
    ),
);
$d = $c->insert($data, array("w" => 1));

$ops = array(
    array(
        '$project' => array(
            "author" => 1,
            "tags"   => 1,
        )
    ),
    array('$unwind' => '$tags'),
    array(
        '$group' => array(
            "_id" => array("tags" => '$tags'),
            "authors" => array('$addToSet' => '$author'),
        ),
    ),
);
$results = $c->aggregate($ops);
var_dump($results);
?>
```

以上例程会输出：

    array(2) {
      ["result"]=>
      array(2) {
        [0]=>
        array(2) {
          ["_id"]=>
          array(1) {
            ["tags"]=>
            string(4) "good"
          }
          ["authors"]=>
          array(1) {
            [0]=>
            string(3) "bob"
          }
        }
        [1]=>
        array(2) {
          ["_id"]=>
          array(1) {
            ["tags"]=>
            string(3) "fun"
          }
          ["authors"]=>
          array(1) {
            [0]=>
            string(3) "bob"
          }
        }
      }
      ["ok"]=>
      float(1)
    }

The following examples use the
<a href="https://media.mongodb.org/zips.json" class="link external">» zipcode data set</a>.
Use mongoimport to load this data set into your mongod instance.

**示例 \#2 <span class="methodname">MongoCollection::aggregate</span>
example**

To return all states with a population greater than 10 million, use the
following aggregation operation:

``` php
<?php
$m = new MongoClient("localhost");
$c = $m->selectDB("test")->selectCollection("zips");

$pipeline = array(
    array(
        '$group' => array(
            '_id' => array('state' => '$state'),
            'totalPop' => array('$sum' => '$pop')
        )
    ),
    array(
        '$match' => array(
            'totalPop' => array('$gte' => 10 * 1000 * 1000)
        )
    ),
);
$out = $c->aggregate($pipeline);
var_dump($out);
?>
```

以上例程的输出类似于：

    array(2) {
      ["result"]=>
      array(7) {
        [0]=>
        array(2) {
          ["_id"]=>
          string(2) "TX"
          ["totalPop"]=>
          int(16986510)
        }
        [1]=>
        array(2) {
          ["_id"]=>
          string(2) "PA"
          ["totalPop"]=>
          int(11881643)
        }
        [2]=>
        array(2) {
          ["_id"]=>
          string(2) "NY"
          ["totalPop"]=>
          int(17990455)
        }
        [3]=>
        array(2) {
          ["_id"]=>
          string(2) "IL"
          ["totalPop"]=>
          int(11430602)
        }
        [4]=>
        array(2) {
          ["_id"]=>
          string(2) "CA"
          ["totalPop"]=>
          int(29760021)
        }
        [5]=>
        array(2) {
          ["_id"]=>
          string(2) "OH"
          ["totalPop"]=>
          int(10847115)
        }
        [6]=>
        array(2) {
          ["_id"]=>
          string(2) "FL"
          ["totalPop"]=>
          int(12937926)
        }
      }
      ["ok"]=>
      float(1)
    }

**示例 \#3 <span class="methodname">MongoCollection::aggregate</span>
example**

To return the average populations for cities in each state, use the
following aggregation operation:

``` php
<?php
$m = new MongoClient;
$c = $m->selectDB("test")->selectCollection("zips");

$out = $c->aggregate(
    array(
        '$group' => array(
            '_id' => array('state' => '$state', 'city' => '$city' ),
            'pop' => array('$sum' => '$pop' )
        )
    ),
    array(
        '$group' => array(
            '_id' => '$_id.state',
            'avgCityPop' => array('$avg' => '$pop')
        )
    )
);

var_dump($out);
?>
```

以上例程的输出类似于：

    array(2) {
      ["result"]=>
      array(51) {
        [0]=>
        array(2) {
          ["_id"]=>
          string(2) "DC"
          ["avgCityPop"]=>
          float(303450)
        }
        [1]=>
        array(2) {
          ["_id"]=>
          string(2) "DE"
          ["avgCityPop"]=>
          float(14481.913043478)
        }
    ...
        [49]=>
        array(2) {
          ["_id"]=>
          string(2) "WI"
          ["avgCityPop"]=>
          float(7323.0074850299)
        }
        [50]=>
        array(2) {
          ["_id"]=>
          string(2) "WV"
          ["avgCityPop"]=>
          float(2759.1953846154)
        }
      }
      ["ok"]=>
      float(1)
    }

**示例 \#4 <span class="methodname">MongoCollection::aggregate</span>
with command options**

To return information on how the pipeline will be processed we use the
*explain* command option:

``` php
<?php
$m = new MongoClient;
$c = $m->selectDB("test")->selectCollection("zips");

$pipeline = array(
    array(
        '$group' => array(
            '_id' => '$state',
           'totalPop' => array('$sum' => '$pop'),
        ),
    ),
    array(
        '$match' => array(
            'totalPop' => array('$gte' => 10 * 1000 * 1000)
        )
    ),
    array(
        '$sort' => array("totalPop" => -1),
    ),
);

$options = array("explain" => true);
$out = $c->aggregate($pipeline, $options);
var_dump($out);
?>
```

以上例程的输出类似于：

    array(2) {
      ["stages"]=>
      array(4) {
        [0]=>
        array(1) {
          ["$cursor"]=>
          array(3) {
            ["query"]=>
            array(0) {
            }
            ["fields"]=>
            array(3) {
              ["pop"]=>
              int(1)
              ["state"]=>
              int(1)
              ["_id"]=>
              int(0)
            }
            ["plan"]=>
            array(4) {
              ["cursor"]=>
              string(11) "BasicCursor"
              ["isMultiKey"]=>
              bool(false)
              ["scanAndOrder"]=>
              bool(false)
              ["allPlans"]=>
              array(1) {
                [0]=>
                array(3) {
                  ["cursor"]=>
                  string(11) "BasicCursor"
                  ["isMultiKey"]=>
                  bool(false)
                  ["scanAndOrder"]=>
                  bool(false)
                }
              }
            }
          }
        }
        [1]=>
        array(1) {
          ["$group"]=>
          array(2) {
            ["_id"]=>
            string(6) "$state"
            ["totalPop"]=>
            array(1) {
              ["$sum"]=>
              string(4) "$pop"
            }
          }
        }
        [2]=>
        array(1) {
          ["$match"]=>
          array(1) {
            ["totalPop"]=>
            array(1) {
              ["$gte"]=>
              int(10000000)
            }
          }
        }
        [3]=>
        array(1) {
          ["$sort"]=>
          array(1) {
            ["sortKey"]=>
            array(1) {
              ["totalPop"]=>
              int(-1)
            }
          }
        }
      }
      ["ok"]=>
      float(1)
    }

### 参见

-   <span class="methodname">MongoCollection::aggregateCursor</span>
-   The MongoDB
    <a href="https://docs.mongodb.com/manual/core/aggregation-pipeline/" class="link external">» aggregation framework</a>

MongoCollection::aggregateCursor
================================

Execute an aggregation pipeline command and retrieve results through a
cursor

### 说明

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">MongoCollection::aggregateCursor</span> ( <span
class="methodparam"><span class="type">array</span> `$command`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

With this method you can execute Aggregation Framework pipelines and
retrieve the results through a cursor, instead of getting just one
document back as you would with <span
class="methodname">MongoCollection::aggregate</span>. This method
returns a <span class="classname">MongoCommandCursor</span> object. This
cursor object implements the <span class="classname">Iterator</span>
interface just like the <span class="classname">MongoCursor</span>
objects that are returned by the <span
class="methodname">MongoCollection::find</span> method.

> **Note**: <span class="simpara"> The resulting <span
> class="classname">MongoCommandCursor</span> will inherit this
> collection's read preference. <span
> class="methodname">MongoCommandCursor::setReadPreference</span> may be
> used to change the read preference before iterating on the cursor.
> </span>

### 参数

`pipeline`  
The Aggregation Framework pipeline to execute.

`options`  
Options for the aggregation command. Valid options include:

-   *"allowDiskUse"*

    Allow aggregation stages to write to temporary files

-   *"cursor"*

    It is possible to configure how many initial documents the server
    should return with the first result set. The default initial batch
    size is *101*. You can change it by adding the *batchSize* option:

    ``` php
    <?php
    $collection->aggregateCursor( 
        $pipeline,
        [ "cursor" => [ "batchSize" => 4 ] ]
    );
    ```

    This option only configures the size of the first batch. To
    configure the size of future batches, please use the <span
    class="methodname">MongoCommandCursor::batchSize</span> method on
    the returned <span class="classname">MongoCommandCursor</span>
    object.

-   *"explain"*

    Return information on the processing of the pipeline. This option
    may cause the command to return a result document that is unsuitable
    for constructing a <span
    class="classname">MongoCommandCursor</span>. If you need to use this
    option, you should consider using <span
    class="methodname">MongoCollection::aggregate</span>.

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

### 返回值

Returns a <span class="classname">MongoCommandCursor</span> object.
Because this implements the <span class="classname">Iterator</span>
interface you can iterate over each of the results as returned by the
command query. The <span class="classname">MongoCommandCursor</span>
also implements the <span class="classname">MongoCursorInterface</span>
interface which adds the <span
class="methodname">MongoCommandCursor::batchSize</span>, <span
class="methodname">MongoCommandCursor::dead</span>, <span
class="methodname">MongoCommandCursor::info</span> methods.

### 范例

**示例 \#1 <span
class="function">MongoCollection::aggregateCursor</span> example**

Finding all of the distinct values for a key.

``` php
<?php
$m = new MongoClient;
$db = $m->test;
$people = $db->people;
$people->drop();

$people->insert(array("name" => "Joe", "points" => 4));
$people->insert(array("name" => "Molly", "points" => 43));
$people->insert(array("name" => "Sally", "points" => 22));
$people->insert(array("name" => "Joe", "points" => 22));
$people->insert(array("name" => "Molly", "points" => 87));

$ages = $people->aggregateCursor( [
        [ '$group' => [ '_id' => '$name', 'points' => [ '$sum' => '$points' ] ] ],
        [ '$sort' => [ 'points' => -1 ] ],
] );

foreach ($ages as $person) {
    echo "{$person['_id']}: {$person['points']}\n";
}

?>
```

以上例程的输出类似于：

  
Molly: 130  
Joe: 26  
Sally: 22  

**示例 \#2 <span
class="function">MongoCollection::aggregateCursor</span> example with
different initial batch size**

Finding all of the distinct values for a key.

``` php
<?php
$m = new MongoClient;
$db = $m->test;
$people = $db->people;
$people->drop();

/* Insert some sample data */
$people->insert(array("name" => "Joe", "points" => 4));
$people->insert(array("name" => "Molly", "points" => 43));
$people->insert(array("name" => "Sally", "points" => 22));
$people->insert(array("name" => "Joe", "points" => 22));
$people->insert(array("name" => "Molly", "points" => 87));

/* Run the command cursor */
$ages = $people->aggregateCursor(
    [
        [ '$group' => [ '_id' => '$name', 'points' => [ '$sum' => '$points' ] ] ],
        [ '$sort' => [ 'points' => -1 ] ],
    ],
    [ "cursor" => [ "batchSize" => 4 ] ]
);

foreach ($ages as $person) {
    echo "{$person['_id']}: {$person['points']}\n";
}

?>
```

以上例程的输出类似于：

  
Molly: 130  
Joe: 26  
Sally: 22  

### 参见

-   <span class="methodname">MongoDB::command</span>
-   <span class="classname">MongoCommandCursor</span>
-   <span class="methodname">MongoCommandCursor::batchSize</span>
-   <span class="methodname">MongoCollection::aggregate</span>
-   The MongoDB
    <a href="https://docs.mongodb.com/manual/core/aggregation-pipeline/" class="link external">» aggregation framework</a>

MongoCollection::batchInsert
============================

Inserts multiple documents into this collection

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoCollection::batchInsert</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

### 参数

`a`  
An array of arrays or objects. If any objects are used, they may not
have protected or private properties.

> **Note**:
>
> If the documents to insert do not have an *\_id* key or property, a
> new <span class="classname">MongoId</span> instance will be created
> and assigned to it. See <span
> class="function">MongoCollection::insert</span> for additional
> information on this behavior.

`options`  
An array of options for the batch of insert operations. Currently
available options include:

-   *"continueOnError"*

    Boolean, defaults to **`FALSE`**. If set, the database will not stop
    processing a bulk insert if one fails (eg due to duplicate IDs).
    This makes bulk insert behave similarly to a series of single
    inserts, except that calling <span
    class="function">MongoDB::lastError</span> will have an error set if
    any insert fails, not just the last one. If multiple errors occur,
    only the most recent will be reported by <span
    class="function">MongoDB::lastError</span>.

    > **Note**:
    >
    > Please note that *continueOnError* affects errors on the database
    > side only. If you try to insert a document that has errors (for
    > example it contains a key with an empty name), then the document
    > is not even transferred to the database as the driver detects this
    > error and bails out. *continueOnError* has no effect on errors
    > detected in the documents by the driver.

-   *"fsync"*

    Boolean, defaults to **`FALSE`**. If journaling is enabled, it works
    exactly like *"j"*. If journaling is not enabled, the write
    operation blocks until it is synced to database files on disk. If
    **`TRUE`**, an acknowledged insert is implied and this option will
    override setting *"w"* to *0*.

    > **Note**: <span class="simpara">If journaling is enabled, users
    > are strongly encouraged to use the *"j"* option instead of
    > *"fsync"*. Do not use *"fsync"* and *"j"* simultaneously, as that
    > will result in an error.</span>

-   *"j"*

    Boolean, defaults to **`FALSE`**. Forces the write operation to
    block until it is synced to the journal on disk. If **`TRUE`**, an
    acknowledged write is implied and this option will override setting
    *"w"* to *0*.

    > **Note**: <span class="simpara">If this option is used and
    > journaling is disabled, MongoDB 2.6+ will raise an error and the
    > write will fail; older server versions will simply ignore the
    > option.</span>

-   *"socketTimeoutMS"*

    This option specifies the time limit, in milliseconds, for socket
    communication. If the server does not respond within the timeout
    period, a <span class="classname">MongoCursorTimeoutException</span>
    will be thrown and there will be no way to determine if the server
    actually handled the write or not. A value of *-1* may be specified
    to block indefinitely. The default value for <span
    class="classname">MongoClient</span> is *30000* (30 seconds).

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wTimeoutMS"*

    This option specifies the time limit, in milliseconds, for
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    acknowledgement. It is only applicable when *"w"* is greater than
    *1*, as the timeout pertains to replication. If the write concern is
    not satisfied within the time limit, a <span
    class="classname">MongoCursorException</span> will be thrown. A
    value of *0* may be specified to block indefinitely. The default
    value for <span class="classname">MongoClient</span> is *10000* (ten
    seconds).

The following options are deprecated and should no longer be used:

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

### 返回值

If the *w* parameter is set to acknowledge the write, returns an
associative array with the status of the inserts ("ok") and any error
that may have occurred ("err"). Otherwise, returns **`TRUE`** if the
batch insert was successfully sent, **`FALSE`** otherwise.

### 错误／异常

Throws <span class="classname">MongoException</span> if any inserted
documents are empty or if they contains zero-length keys. Attempting to
insert an object with protected and private properties will cause a
zero-length key error.

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.5.0</td>
<td><p>Added the <em>"wTimeoutMS"</em> option, which replaces <em>"wtimeout"</em>. Emits <strong><code>E_DEPRECATED</code></strong> when <em>"wtimeout"</em> is used.</p>
<p>Added the <em>"socketTimeoutMS"</em> option, which replaces <em>"timeout"</em>. Emits <strong><code>E_DEPRECATED</code></strong> when <em>"timeout"</em> is used.</p>
<p>Emits <strong><code>E_DEPRECATED</code></strong> when <em>"safe"</em> is used.</p></td>
</tr>
<tr class="even">
<td>1.3.4</td>
<td>Added <em>"wtimeout"</em> option.</td>
</tr>
<tr class="odd">
<td>1.3.0</td>
<td>Added <em>"w"</em> option.</td>
</tr>
<tr class="even">
<td>1.2.7</td>
<td>Added <em>"continueOnError"</em> option.</td>
</tr>
<tr class="odd">
<td>1.0.9</td>
<td><p>Added ability to pass integers to the <em>"safe"</em> option, which previously only accepted booleans.</p>
<p>Added <em>"fsync"</em> option.</p></td>
</tr>
<tr class="even">
<td>1.0.5</td>
<td>Added <code class="parameter">options</code> parameter.</td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">MongoCollection::batchInsert</span>
example**

Batch insertion is a quick way to add many elements to the database at
once

``` php
<?php

$users = array();
for ($i = 0; $i<100; $i++) {
  $users[] = array('username' => 'user'.$i, 'i' => $i);
}

$mongo = new MongoClient();
$collection = $mongo->my_db->users;
$collection->drop();

$collection->batchInsert($users);

foreach ($users as $user) {
  echo $user['_id']."\n"; // populated with instanceof MongoId
}

$users = $collection->find()->sort(array('i' => 1));
foreach ($users as $user) {
    var_dump($user['username']);
}

?>
```

以上例程的输出类似于：

    4bf43ac68ead0e1971000000
    4bf43ac68ead0e1971010000
    4bf43ac68ead0e1971020000
    ...
    string(5) "user1"
    string(5) "user2"
    string(5) "user3"
    ...

**示例 \#2 <span class="function">MongoCollection::batchInsert</span>
example with ignoring errors**

``` php
<?php

$con = new Mongo;
$db = $con->demo;

$doc1 = array(
        '_id' => new MongoId('4cb4ab6d7addf98506010001'),
        'id' => 1,
        'desc' => "ONE",
);
$doc2 = array(
        '_id' => new MongoId('4cb4ab6d7addf98506010002'),
        'id' => 2,
        'desc' => "TWO",
);
$doc3 = array(
        '_id' => new MongoId('4cb4ab6d7addf98506010002'), // same _id as above
        'id' => 3,
        'desc' => "THREE",
);
$doc4 = array(
        '_id' => new MongoId('4cb4ab6d7addf98506010004'),
        'id' => 4,
        'desc' => "FOUR",
);

$c = $db->selectCollection('c');
$c->batchInsert(
    array($doc1, $doc2, $doc3, $doc4),
    array('continueOnError' => true)
);

$docs = $c->find();
foreach ($docs as $doc) {
    var_dump($doc['desc']);
}
?>
```

以上例程的输出类似于：

    string(3) "ONE"
    string(3) "TWO"
    string(4) "FOUR"

### 参见

-   <span class="function">MongoCollection::insert</span>
-   <span class="function">MongoCollection::update</span>
-   <span class="function">MongoCollection::find</span>
-   <span class="function">MongoCollection::remove</span>
-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/tutorial/insert-documents/" class="link external">» insert</a>.

MongoCollection::\_\_construct
==============================

创建一个新的集合

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoCollection::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoDB</span> `$db`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

### 参数

<span class="type">MongoDB</span> `db`  
所属的父数据库。

<!-- -->

`name`  
集合的名称。

### 返回值

返回一个新的集合对象。

### 错误／异常

如果集合名称无效，将会抛出一个默认的异常。

MongoCollection::count
======================

返回集合中的文档数量

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoCollection::count</span> (\[ <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$skip`<span
class="initializer"> = 0</span></span> \]\]\] )

### 参数

`query`  
关联数组或者对象，含有需要匹配的字段。

`limit`  
指定返回数量的上限。

`skip`  
指定在开始统计前，需要跳过的结果数目。

### 返回值

返回查询匹配到的文档数目。

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 1.0.7 | 添加了 `limit` 和 `skip` 参数。 |

### 范例

**示例 \#1 <span class="function">MongoCollection::count</span> 例子**

``` php
<?php

$collection->insert(array('x'=>1));
$collection->insert(array('x'=>2));
$collection->insert(array('x'=>3));

var_dump($collection->count());
var_dump($collection->count(array('x'=>1)));

?>
```

以上例程的输出类似于：

    int(3)
    int(1)

MongoCollection::createDBRef
============================

创建一个数据库引用

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::createDBRef</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$document_or_id`</span> )

### 参数

`document_or_id`  
If an array or object is given, its *\_id* field will be used as the
reference ID. If a <span class="classname">MongoId</span> or scalar is
given, it will be used as the reference ID.

### 返回值

返回一个数据库的引用数组。

如果提供了不包含 *\_id* 字段的数组当做 *document\_or\_id* 参数，将会返回
**`NULL`**。

### 范例

**示例 \#1 <span class="methodname">MongoCollection::createDBRef</span>
例子**

``` php
<?php

$songs = $db->songs;
$playlists = $db->playlists;

// 为 song 创建引用
$manamana = $songs->findOne(array('title' => 'Ma na ma na'));
$refToSong = $songs->createDBRef($manamana);

// 添加引用到我的播放列表
$playlists->update(array('username' => 'me'), array('$push' => array('songlist' => $refToSong)));

?>
```

### 参见

-   <span class="methodname">MongoCollection::getDBRef</span>

MongoCollection::createIndex
============================

Creates an index on the specified field(s) if it does not already exist

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCollection::createIndex</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

Creates an index on the specified field(s) if it does not already exist.
Fields may be indexed with a direction (e.g. ascending or descending) or
a special type (e.g. text, geospatial, hashed).

> **Note**:
>
> This method will use the
> <a href="https://docs.mongodb.com/manual/reference/command/createIndexes" class="link external">» createIndexes</a>
> database command when communicating with MongoDB 2.6+. For previous
> database versions, the method will perform an insert operation on the
> special *system.indexes* collection.

### 参数

`keys`  
An array specifying the index's fields as its keys. For each field, the
value is either the index direction or
<a href="https://docs.mongodb.com/manual/core/index-types/" class="link external">» index type</a>.
If specifying direction, specify *1* for ascending or *-1* for
descending.

`options`  
An array of options for the index creation. We pass all given options
straight to the server, but a non-exhaustive list of currently available
options include:

-   *"unique"*

    Specify **`TRUE`** to create a unique index. The default value is
    **`FALSE`**. This option applies only to ascending/descending
    indexes.

    > **Note**:
    >
    > When MongoDB indexes a field, if a document does not have a value
    > for the field, a **`NULL`** value is indexed. If multiple
    > documents do not contain a field, a unique index will reject all
    > but the first of those documents. The *"sparse"* option may be
    > used to overcome this, since it will prevent documents without the
    > field from being indexed.

-   *"sparse"*

    Specify **`TRUE`** to create a sparse index, which only indexes
    documents containing a specified field. The default value is
    **`FALSE`**.

-   *"expireAfterSeconds"*

    The value of this option should specify the number of seconds after
    which a document should be considered expired and automatically
    removed from the collection. This option is only compatible with
    single-field indexes where the field will contain <span
    class="classname">MongoDate</span> values.

    > **Note**:
    >
    > This feature is available in MongoDB 2.2+. See
    > <a href="https://docs.mongodb.com/manual/tutorial/expire-data/" class="link external">» Expire Data from Collections by Setting TTL</a>
    > for more information.

-   *"name"*

    A optional name that uniquely identifies the index.

    > **Note**:
    >
    > By default, the driver will generate an index name based on the
    > index's field(s) and ordering or type. For example, a compound
    > index *array("x" =\> 1, "y" =\> -1)* would be named
    > *"x\_1\_y\_-1"* and a geospatial index *array("loc" =\>
    > "2dsphere")* would be named *"loc\_2dsphere"*. For indexes with
    > many fields, it is possible that the generated name might exceed
    > MongoDB's
    > <a href="https://docs.mongodb.com/manual/reference/limits/#Index-Name-Length" class="link external">» limit for index names</a>.
    > The *"name"* option may be used in that case to supply a shorter
    > name.

-   *"background"*

    Builds the index in the background so that building an index does
    *not* block other database activities. Specify **`TRUE`** to build
    in the background. The default value is **`FALSE`**.

    **Warning**
    Prior to MongoDB 2.6.0, index builds on secondaries were executed as
    foreground operations, irrespective of this option. See
    <a href="https://docs.mongodb.com/manual/tutorial/build-indexes-on-replica-sets/" class="link external">» Building Indexes with Replica Sets</a>
    for more information.

-   *"socketTimeoutMS"*

    This option specifies the time limit, in milliseconds, for socket
    communication. If the server does not respond within the timeout
    period, a <span class="classname">MongoCursorTimeoutException</span>
    will be thrown and there will be no way to determine if the server
    actually handled the write or not. A value of *-1* may be specified
    to block indefinitely. The default value for <span
    class="classname">MongoClient</span> is *30000* (30 seconds).

The following option may be used with MongoDB 2.6+:

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

The following options may be used with MongoDB versions before 2.8:

-   *"dropDups"*

    Specify **`TRUE`** to force creation of a unique index where the
    collection may contain duplicate values for a key. MongoDB will
    index the first occurrence of a key and delete all subsequent
    documents from the collection that contain a duplicate value for
    that key. The default value is **`FALSE`**.

    **Warning**
    *"dropDups"* may delete data from your database. Use with extreme
    caution.

    > **Note**:
    >
    > This option is not supported on MongoDB 2.8+. Index creation will
    > fail if the collection contains duplicate values.

The following options may be used with MongoDB versions before 2.6:

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wTimeoutMS"*

    This option specifies the time limit, in milliseconds, for
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    acknowledgement. It is only applicable when *"w"* is greater than
    *1*, as the timeout pertains to replication. If the write concern is
    not satisfied within the time limit, a <span
    class="classname">MongoCursorException</span> will be thrown. A
    value of *0* may be specified to block indefinitely. The default
    value for <span class="classname">MongoClient</span> is *10000* (ten
    seconds).

The following options are deprecated and should no longer be used:

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

### 返回值

Returns an array containing the status of the index creation. The array
contains whether the operation succeeded (*"ok"*), the number of indexes
before and after the operation (*"numIndexesBefore"* and
*"numIndexesAfter"*), and whether the collection that the index belongs
to has been created (*"createdCollectionAutomatically"*). If the index
already existed and did not need to be created, a *"note"* field may be
present in lieu of *"numIndexesAfter"*.

With MongoDB 2.4 and earlier, a status document is only returned if the
<a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
is at least *1*. Otherwise, **`TRUE`** is returned. The fields in the
status document are different, except for the *"ok"* field, which
signals whether the index creation was successful. Additional fields are
described in the documentation for <span
class="function">MongoCollection::insert</span>.

### 错误／异常

Throws <span class="classname">MongoException</span> if the index name
is longer than 128 bytes, or if the index specification is not an array.

Throws <span class="classname">MongoDuplicateKeyException</span> if the
server could not create the unique index due to conflicting documents.

Throws <span class="classname">MongoResultException</span> if the server
could not create the index due to an error.

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 范例

**示例 \#1 <span class="function">MongoCollection::createIndex</span>
example**

``` php
<?php

$c = new MongoCollection($db, 'foo');

// create an index on 'x' ascending
$c->createIndex(array('x' => 1));

// create a unique index on 'y'
$c->createIndex(array('y' => 1), array('unique' => true));

// create a compound index on 'za' ascending and 'zb' descending
$c->createIndex(array('za' => 1, 'zb' => -1));

?>
```

**示例 \#2 Geospatial Indexing**

Mongo supports geospatial indexes, which allow you to search for
documents near a given location or within a shape. The following example
creates a geospatial index on the *"loc"* field:

``` php
<?php

$collection->createIndex(array('loc' => '2dsphere'));

?>
```

**示例 \#3 Drop duplicates example**

``` php
<?php

$collection->insert(array('username' => 'joeschmoe'));
$collection->insert(array('username' => 'joeschmoe'));

/* Index creation fails, since you cannot create a unique index on a field when
 * duplicates exist.
 */
$collection->createIndex(array('username' => 1), array('unique' => 1));

/* MongoDB will one of the conflicting documents and allow the unique index to
 * be created.
 */
$collection->createIndex(array('username' => 1), array('unique' => 1, 'dropDups' => 1));

/* We now have a unique index and subsequent inserts with the same username will
 * fail.
 */
$collection->insert(array('username' => 'joeschmoe'));

?>
```

### 参见

-   <span class="methodname">MongoCollection::deleteIndex</span>
-   <span class="methodname">MongoCollection::deleteIndexes</span>
-   The MongoDB
    <a href="https://docs.mongodb.com/manual/indexes/" class="link external">» index</a>
    and
    <a href="https://docs.mongodb.com/manual/core/index-types/" class="link external">» index type</a>
    documentation.

MongoCollection::deleteIndex
============================

Deletes an index from this collection

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::deleteIndex</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$keys`</span> )

This method is identical to:

``` php
<?php

public function deleteIndexes($keys) {
  $indexName = $this->toIndexString($keys);

  return $this->db->command(array(
    "deleteIndexes" => $this->getName(),
    "index" => $indexName,
  ));
}

?>
```

Each index is given a unique name when it is created. This is often
generated by the driver based on the index key(s) and order/type, but
custom names may also be specified with <span
class="function">MongoCollection::createIndex</span>'s *"name"* option).

Unfortunately, <span
class="function">MongoCollection::deleteIndex</span> cannot delete
custom-named indexes due to a backwards compatibility issue. When a
string argument is provided, it is assumed to be the single field name
in an ascending index (e.g. the name *"x\_1"* would be used for the
argument *"x"*). If an array or object is provided, an index name is
generated just as if that argument was passed to <span
class="function">MongoCollection::createIndex</span>.

In order to delete a custom-named index with the PHP driver, the
*deleteIndexes* database command must be used. For instance, an index
named "myIndex" could be deleted with the PHP driver by running:

``` php
<?php

$db->command(array(
  "deleteIndexes" => $collection->getName(),
  "index" => "myIndex",
));

?>
```

To determine the name of an index with the PHP driver, you can query the
*system.indexes* collection of a database and look for the *"name"*
field of each result. The *"ns"* field will indicate the collection to
which each index belongs.

### 参数

`keys`  
An array specifying the index's fields as its keys. For each field, the
value is either the index direction or
<a href="https://docs.mongodb.com/manual/core/index-types/" class="link external">» index type</a>.
If specifying direction, specify *1* for ascending or *-1* for
descending.

If a string is provided, it is assumed to be the single field name in an
ascending index.

### 返回值

Returns the database response.

### 范例

**示例 \#1 <span class="function">MongoCollection::deleteIndex</span>
example**

This example passes the function string and array parameters.

``` php
<?php

$m = new MongoClient();
$c = $m->example->indices;

// create and remove a simple index
$c->createIndex(array("i"=>1));
$c->deleteIndex("i");

// create and remove a multi-key index
$c->ensureIndex(array("j" => 1, "k" => 1));
$c->deleteIndex(array("j" => 1, "k" => 1));

?>
```

### 参见

-   <span class="methodname">MongoCollection::createIndex</span>
-   <span class="methodname">MongoCollection::deleteIndexes</span>
-   <span class="methodname">MongoCollection::toIndexString</span>
-   The MongoDB
    <a href="https://docs.mongodb.com/manual/indexes/" class="link external">» index</a>
    and
    <a href="https://docs.mongodb.com/manual/core/index-types/" class="link external">» index type</a>
    documentation.

MongoCollection::deleteIndexes
==============================

删除集合的所有索引

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::deleteIndexes</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回数据库的响应。

### 范例

**示例 \#1 <span class="function">MongoCollection::deleteIndexes</span>
例子**

这个例子演示了如何从集合中删除所有索引并得到响应

``` php
<?php

$collection = $mongo->my_db->articles;
$response = $collection->deleteIndexes();
print_r($response);

?>
```

以上例程的输出类似于：

    Array
    (
        [nIndexesWas] => 1
        [msg] => all indexes deleted for collection
        [ok] => 1
    )

### 参见

-   <span class="methodname">MongoCollection::createIndex</span>
-   <span class="methodname">MongoCollection::deleteIndex</span>

MongoCollection::distinct
=========================

获取集合里指定键的不同值的列表。

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::distinct</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$query`</span> \] )

distinct 命令返回集合里给定键不同值的列表。

### 参数

`key`  
要使用的键。

`query`  
一个可选的查询参数

### 返回值

返回不同值的数组， 或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="methodname">MongoCollection::distinct</span>
例子**

``` php
<?php
$m = new Mongo;
$db = $m->selectDB("test");
$db->dropCollection("distinct");
$c = $db->distinct;

$c->insert(array("stuff" => "bar", "zip-code" => 10010));
$c->insert(array("stuff" => "foo", "zip-code" => 10010));
$c->insert(array("stuff" => "bar", "zip-code" => 99701), array("w" => 1));

$retval = $c->distinct("zip-code");
var_dump($retval);

$retval = $c->distinct("zip-code", array("stuff" => "foo"));
var_dump($retval);

$retval = $c->distinct("zip-code", array("stuff" => "bar"));
var_dump($retval);

?>
```

以上例程会输出：

    array(2) {
      [0]=>
      int(10010)
      [1]=>
      int(99701)
    }
    array(1) {
      [0]=>
      int(10010)
    }
    array(2) {
      [0]=>
      int(10010)
      [1]=>
      int(99701)
    }

**示例 \#2 内嵌文档的 <span
class="methodname">MongoCollection::distinct</span> 例子**

``` php
<?php
$c->insert(array("user" => array("points" => 25)));
$c->insert(array("user" => array("points" => 31)));
$c->insert(array("user" => array("points" => 25)));

$retval = $c->distinct("user.points");
var_dump($retval);

$retval = $c->distinct("user.nonexisting");
var_dump($retval);
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      int(25)
      [1]=>
      int(31)
    }
    array(0) {
    }

MongoCollection::drop
=====================

删除该集合

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::drop</span> ( <span
class="methodparam">void</span> )

删除该集合，以及它的索引。

### 参数

此函数没有参数。

### 返回值

返回数据库的响应。

### 范例

**示例 \#1 <span class="function">MongoCollection::drop</span> 例子**

这个例子演示了如何删除一个集合，并且得到想要的回应。

``` php
<?php

$collection = $mongo->my_db->articles;
$response = $collection->drop();
print_r($response);

?>
```

以上例程的输出类似于：

    Array
    (
        [nIndexesWas] => 1
        [msg] => all indexes deleted for collection
        [ns] => my_db.articles
        [ok] => 1
    )

MongoCollection::ensureIndex
============================

Creates an index on the specified field(s) if it does not already exist

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCollection::ensureIndex</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$key|keys`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

**Warning**

This method is deprecated since version 1.5.0. Please use <span
class="methodname">MongoCollection::createIndex</span> instead.

Creates an index on the specified field(s) if it does not already exist.
Fields may be indexed with a direction (e.g. ascending or descending) or
a special type (e.g. text, geospatial, hashed).

> **Note**:
>
> This method will use the
> <a href="https://docs.mongodb.com/manual/reference/command/createIndexes" class="link external">» createIndexes</a>
> database command when communicating with MongoDB 2.6+. For previous
> database versions, the method will perform an insert operation on the
> special *system.indexes* collection.

### 参数

`keys`  
An array specifying the index's fields as its keys. For each field, the
value is either the index direction or
<a href="https://docs.mongodb.com/manual/core/index-types/" class="link external">» index type</a>.
If specifying direction, specify *1* for ascending or *-1* for
descending.

`options`  
An array of options for the index creation. Currently available options
include:

-   *"unique"*

    Specify **`TRUE`** to create a unique index. The default value is
    **`FALSE`**. This option applies only to ascending/descending
    indexes.

    > **Note**:
    >
    > When MongoDB indexes a field, if a document does not have a value
    > for the field, a **`NULL`** value is indexed. If multiple
    > documents do not contain a field, a unique index will reject all
    > but the first of those documents. The *"sparse"* option may be
    > used to overcome this, since it will prevent documents without the
    > field from being indexed.

-   *"sparse"*

    Specify **`TRUE`** to create a sparse index, which only indexes
    documents containing a specified field. The default value is
    **`FALSE`**.

-   *"expireAfterSeconds"*

    The value of this option should specify the number of seconds after
    which a document should be considered expired and automatically
    removed from the collection. This option is only compatible with
    single-field indexes where the field will contain <span
    class="classname">MongoDate</span> values.

    > **Note**:
    >
    > This feature is available in MongoDB 2.2+. See
    > <a href="https://docs.mongodb.com/manual/tutorial/expire-data/" class="link external">» Expire Data from Collections by Setting TTL</a>
    > for more information.

-   *"name"*

    A optional name that uniquely identifies the index.

    > **Note**:
    >
    > By default, the driver will generate an index name based on the
    > index's field(s) and ordering or type. For example, a compound
    > index *array("x" =\> 1, "y" =\> -1)* would be named
    > *"x\_1\_y\_-1"* and a geospatial index *array("loc" =\>
    > "2dsphere")* would be named *"loc\_2dsphere"*. For indexes with
    > many fields, it is possible that the generated name might exceed
    > MongoDB's
    > <a href="https://docs.mongodb.com/manual/reference/limits/#Index-Name-Length" class="link external">» limit for index names</a>.
    > The *"name"* option may be used in that case to supply a shorter
    > name.

-   *"background"*

    Builds the index in the background so that building an index does
    *not* block other database activities. Specify **`TRUE`** to build
    in the background. The default value is **`FALSE`**.

    **Warning**
    Prior to MongoDB 2.6.0, index builds on secondaries were executed as
    foreground operations, irrespective of this option. See
    <a href="https://docs.mongodb.com/manual/tutorial/build-indexes-on-replica-sets/" class="link external">» Building Indexes with Replica Sets</a>
    for more information.

-   *"socketTimeoutMS"*

    This option specifies the time limit, in milliseconds, for socket
    communication. If the server does not respond within the timeout
    period, a <span class="classname">MongoCursorTimeoutException</span>
    will be thrown and there will be no way to determine if the server
    actually handled the write or not. A value of *-1* may be specified
    to block indefinitely. The default value for <span
    class="classname">MongoClient</span> is *30000* (30 seconds).

The following option may be used with MongoDB 2.6+:

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

The following options may be used with MongoDB versions before 2.8:

-   *"dropDups"*

    Specify **`TRUE`** to force creation of a unique index where the
    collection may contain duplicate values for a key. MongoDB will
    index the first occurrence of a key and delete all subsequent
    documents from the collection that contain a duplicate value for
    that key. The default value is **`FALSE`**.

    **Warning**
    *"dropDups"* may delete data from your database. Use with extreme
    caution.

    > **Note**:
    >
    > This option is not supported on MongoDB 2.8+. Index creation will
    > fail if the collection contains duplicate values.

The following options may be used with MongoDB versions before 2.6:

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wTimeoutMS"*

    This option specifies the time limit, in milliseconds, for
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    acknowledgement. It is only applicable when *"w"* is greater than
    *1*, as the timeout pertains to replication. If the write concern is
    not satisfied within the time limit, a <span
    class="classname">MongoCursorException</span> will be thrown. A
    value of *0* may be specified to block indefinitely. The default
    value for <span class="classname">MongoClient</span> is *10000* (ten
    seconds).

The following options are deprecated and should no longer be used:

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

### 返回值

Returns an array containing the status of the index creation. The array
contains whether the operation succeeded (*"ok"*), the number of indexes
before and after the operation (*"numIndexesBefore"* and
*"numIndexesAfter"*), and whether the collection that the index belongs
to has been created (*"createdCollectionAutomatically"*). If the index
already existed and did not need to be created, a *"note"* field may be
present in lieu of *"numIndexesAfter"*.

With MongoDB 2.4 and earlier, a status document is only returned if the
<a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
is at least *1*. Otherwise, **`TRUE`** is returned. The fields in the
status document are different, except for the *"ok"* field, which
signals whether the index creation was successful. Additional fields are
described in the documentation for <span
class="function">MongoCollection::insert</span>.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.5.0</td>
<td><p>Renamed the <em>"wtimeout"</em> option to <em>"wTimeoutMS"</em>. Emits <strong><code>E_DEPRECATED</code></strong> when <em>"wtimeout"</em> is used.</p>
<p>Renamed the <em>"timeout"</em> option to <em>"socketTimeoutMS"</em>. Emits <strong><code>E_DEPRECATED</code></strong> when <em>"timeout"</em> is used.</p>
<p>Emits <strong><code>E_DEPRECATED</code></strong> when <em>"safe"</em> is used.</p></td>
</tr>
<tr class="even">
<td>1.3.4</td>
<td>Added <em>"wtimeout"</em> option.</td>
</tr>
<tr class="odd">
<td>1.3.0</td>
<td><p>Added <em>"w"</em> option.</p>
<p>The <code class="parameter">options</code> parameter no longer accepts a boolean to signify a unique index. Instead, this now has to be done with <em>array('unique' =&gt; true)</em>.</p></td>
</tr>
<tr class="even">
<td>1.2.11</td>
<td>Emits <strong><code>E_DEPRECATED</code></strong> when <code class="parameter">options</code> is <span class="type">scalar</span>.</td>
</tr>
<tr class="odd">
<td>1.2.0</td>
<td>Added <em>"timeout"</em> option.</td>
</tr>
<tr class="even">
<td>1.0.11</td>
<td><p>The <em>"safe"</em> option will trigger a primary failover, if necessary.</p>
<p><span class="classname">MongoException</span> will be thrown if the index name (either generated or set) is longer than 128 bytes.</p></td>
</tr>
<tr class="odd">
<td>1.0.5</td>
<td>Added the <em>"name"</em> option to override index name creation.</td>
</tr>
<tr class="even">
<td>1.0.2</td>
<td>Changed <code class="parameter">options</code> parameter from boolean to array. Pre-1.0.2, the second parameter was an optional boolean value specifying a unique index.</td>
</tr>
</tbody>
</table>

### 错误／异常

Throws <span class="classname">MongoException</span> if the index name
is longer than 128 bytes, or if the index specification is not an array.

Throws <span class="classname">MongoDuplicateKeyException</span> if the
server could not create the unique index due to conflicting documents.

Throws <span class="classname">MongoResultException</span> if the server
could not create the index due to an error.

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 范例

**示例 \#1 <span class="function">MongoCollection::ensureIndex</span>
example**

``` php
<?php

$c = new MongoCollection($db, 'foo');

// create an index on 'x' ascending
$c->ensureIndex(array('x' => 1));

// create a unique index on 'y'
$c->ensureIndex(array('y' => 1), array('unique' => true));

// create a compound index on 'za' ascending and 'zb' descending
$c->ensureIndex(array('za' => 1, 'zb' => -1));

?>
```

**示例 \#2 Geospatial Indexing**

Mongo supports geospatial indexes, which allow you to search for
documents near a given location or within a shape. The following example
creates a geospatial index on the *"loc"* field:

``` php
<?php

$collection->ensureIndex(array('loc' => '2dsphere'));

?>
```

**示例 \#3 Drop duplicates example**

``` php
<?php

$collection->insert(array('username' => 'joeschmoe'));
$collection->insert(array('username' => 'joeschmoe'));

/* Index creation fails, since you cannot create a unique index on a field when
 * duplicates exist.
 */
$collection->ensureIndex(array('username' => 1), array('unique' => 1));

/* MongoDB will one of the conflicting documents and allow the unique index to
 * be created.
 */
$collection->ensureIndex(array('username' => 1), array('unique' => 1, 'dropDups' => 1));

/* We now have a unique index and subsequent inserts with the same username will
 * fail.
 */
$collection->insert(array('username' => 'joeschmoe'));

?>
```

### 参见

-   <span class="methodname">MongoCollection::createIndex</span>
-   <span class="methodname">MongoCollection::deleteIndex</span>
-   <span class="methodname">MongoCollection::deleteIndexes</span>
-   The MongoDB
    <a href="https://docs.mongodb.com/manual/indexes/" class="link external">» index</a>
    and
    <a href="https://docs.mongodb.com/manual/core/index-types/" class="link external">» index type</a>
    documentation.

MongoCollection::find
=====================

查询该集合，并返回结果集的 <span class="classname">MongoCursor</span>

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCollection::find</span> (\[ <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`query`  
要搜索的字段。 MongoDB 的查询语言十分宽泛。 PHP
驱动在几乎所有的情况下会把查询直接传入服务器，所以阅读 MongoDB 关于
<a href="https://docs.mongodb.com/manual/reference/method/db.collection.find/" class="link external">» find</a>
的核心文档是个不错的主意。

**Warning**
请确保所有指定的查询操作符（以 *$* 开头）是用单引号的，这样 PHP
才不会尝试用 *$exists* 变量的值来替换 *"$exists"* 命令。

`fields`  
返回结果的字段。Array 的格式是 *array('fieldname' =\> true, 'fieldname2'
=\> true)*。 *\_id* 字段总会返回。

### 返回值

返回搜索结果的游标。

### 范例

**示例 \#1 <span class="function">MongoCollection::find</span> 例子**

该例子演示了基本的搜索选项。

``` php
<?php

$m = new MongoClient();
$db = $m->selectDB('test');
$collection = new MongoCollection($db, 'produce');

// 搜索水果
$fruitQuery = array('Type' => 'Fruit');

$cursor = $collection->find($fruitQuery);
foreach ($cursor as $doc) {
    var_dump($doc);
}

// 搜索甜的产品 Taste is a child of Details. 
$sweetQuery = array('Details.Taste' => 'Sweet');
echo "Sweet\n";
$cursor = $collection->find($sweetQuery);
foreach ($cursor as $doc) {
    var_dump($doc);
}

?>
```

以上例程会输出：

    array(4) {
      ["_id"]=>
      object(MongoId)#7 (1) {
        ["$id"]=>
        string(24) "50a87dd084f045a19b220dd6"
      }
      ["Name"]=>
      string(5) "Apple"
      ["Type"]=>
      string(5) "Fruit"
      ["Details"]=>
      array(2) {
        ["Taste"]=>
        string(5) "Sweet"
        ["Colour"]=>
        string(3) "Red"
      }
    }
    array(4) {
      ["_id"]=>
      object(MongoId)#8 (1) {
        ["$id"]=>
        string(24) "50a87de084f045a19b220dd7"
      }
      ["Name"]=>
      string(5) "Lemon"
      ["Type"]=>
      string(5) "Fruit"
      ["Details"]=>
      array(2) {
        ["Taste"]=>
        string(4) "Sour"
        ["Colour"]=>
        string(5) "Green"
      }
    }

    Sweet:
    array(4) {
      ["_id"]=>
      object(MongoId)#7 (1) {
        ["$id"]=>
        string(24) "50a87dd084f045a19b220dd6"
      }
      ["Name"]=>
      string(5) "Apple"
      ["Type"]=>
      string(5) "Fruit"
      ["Details"]=>
      array(2) {
        ["Taste"]=>
        string(5) "Sweet"
        ["Colour"]=>
        string(3) "Red"
      }
    }

更多关于游标如何使用的信息，参见 <span
class="classname">MongoCursor</span>。

**示例 \#2 <span class="function">MongoCollection::find</span> 例子**

这个例子演示了如何搜索一个范围。

``` php
<?php

$m = new MongoClient();
$db = $m->selectDB('test');
$collection = new MongoCollection($db, 'phpmanual');

// search for documents where 5 < x < 20
$rangeQuery = array('x' => array( '$gt' => 5, '$lt' => 20 ));

$cursor = $collection->find($rangeQuery);
foreach ($cursor as $doc) {
    var_dump($doc);
}

?>
```

以上例程会输出：

    array(2) {
      ["_id"]=>
      object(MongoId)#10 (1) {
        ["$id"]=>
        string(24) "4ebc3e3710b89f2349000000"
      }
      ["x"]=>
      int(12)
    }
    array(2) {
      ["_id"]=>
      object(MongoId)#11 (1) {
        ["$id"]=>
        string(24) "4ebc3e3710b89f2349000001"
      }
      ["x"]=>
      int(12)
    }

更多关于游标如何使用的信息，参见 <span
class="classname">MongoCursor</span>。

**示例 \#3 使用 $where 的 <span
class="function">MongoCollection::find</span> 例子**

这个例子演示了如何搜索一个集合，并用 javascript 代码来筛选结果集。

``` php
<?php

$m = new MongoClient();
$db = $m->selectDB('test');
$collection = new MongoCollection($db, 'phpmanual');

$js = "function() {
    return this.name == 'Joe' || this.age == 50;
}";
$cursor = $collection->find(array('$where' => $js));
foreach ($cursor as $doc) {
    var_dump($doc);
}

?>
```

以上例程会输出：

    array(3) {
      ["_id"]=>
      object(MongoId)#7 (1) {
        ["$id"]=>
        string(24) "4ebc3e3710b89f2349000002"
      }
      ["name"]=>
      string(3) "Joe"
      ["age"]=>
      int(20)
    }

**示例 \#4 使用 $in 的 <span
class="function">MongoCollection::find</span> 例子**

这个例子演示了使用 $in 操作符来搜索集合。

``` php
<?php

$m = new MongoClient();
$db = $m->selectDB('test');
$collection = new MongoCollection($db, 'phpmanual');

$cursor = $collection->find(array(
    'name' => array('$in' => array('Joe', 'Wendy'))
));

?>
```

以上例程会输出：

    array(3) {
      ["_id"]=>
      object(MongoId)#7 (1) {
        ["$id"]=>
        string(24) "4ebc3e3710b89f2349000002"
      }
      ["name"]=>
      string(3) "Joe"
      ["age"]=>
      int(20)
    }

**示例 \#5 以数组形式获取结果集**

返回 <span class="classname">MongoCursor</span>。
常常在开始的时候，人们更习惯使用数组。 使用 <span
class="function">iterator\_to\_array</span> 将游标转换成一个数组。

``` php
<?php

$m = new MongoClient();
$db = $m->selectDB('test');
$collection = new MongoCollection($db, 'phpmanual');

$cursor = $collection->find();
$array = iterator_to_array($cursor);

?>
```

以上例程会输出：

    array(3) {
      ["4ebc40af10b89f5149000000"]=>
      array(2) {
        ["_id"]=>
        object(MongoId)#6 (1) {
          ["$id"]=>
          string(24) "4ebc40af10b89f5149000000"
        }
        ["x"]=>
        int(12)
      }
      ["4ebc40af10b89f5149000001"]=>
      array(2) {
        ["_id"]=>
        object(MongoId)#11 (1) {
          ["$id"]=>
          string(24) "4ebc40af10b89f5149000001"
        }
        ["x"]=>
        int(12)
      }
      ["4ebc40af10b89f5149000002"]=>
      array(3) {
        ["_id"]=>
        object(MongoId)#12 (1) {
          ["$id"]=>
          string(24) "4ebc40af10b89f5149000002"
        }
        ["name"]=>
        string(3) "Joe"
        ["age"]=>
        int(20)
      }
    }

使用 <span class="function">iterator\_to\_array</span>
会让驱动将强制载入所有搜索结果集到内存，所以对超过内存大小的结果集不要这么做！

同时，有些系统集合不具有 *\_id* 字段。 如果你处理一个可能没有 *\_id*
字段的集合，需要将 **`FALSE`** 传入 <span
class="function">iterator\_to\_array</span>
第二个参数（这样它不会尝试使用不存在的 *\_id* 的值作为数组键）。

### 参见

-   <span class="function">MongoCollection::findOne</span>
-   <span class="function">MongoCollection::insert</span>
-   MongoDB
    <a href="https://docs.mongodb.com/manual/reference/method/db.collection.find/" class="link external">» find</a>
    的核心文档。

MongoCollection::findAndModify
==============================

Update a document and return it

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::findAndModify</span> ( <span
class="methodparam"><span class="type">array</span> `$query`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$update`</span> \[, <span class="methodparam"><span
class="type">array</span> `$fields`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\]\] )

The findAndModify command atomically modifies and returns a single
document. By default, the returned document does not include the
modifications made on the update. To return the document with the
modifications made on the update, use the `new` option.

### 参数

`query`  
The query criteria to search for.

`update`  
The update criteria.

`fields`  
Optionally only return these fields.

`options`  
An array of options to apply, such as remove the match document from the
DB and return it.

| Option                                     | 说明                                                                                                                                                                                                                                                                      |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sort` <span class="type">array</span>     | Determines which document the operation will modify if the query selects multiple documents. findAndModify will modify the first document in the sort order specified by this argument.                                                                                   |
| `remove` <span class="type">boolean</span> | Optional if `update` field exists. When **`TRUE`**, removes the selected document. The default is **`FALSE`**.                                                                                                                                                            |
| `update` <span class="type">array</span>   | Optional if `remove` field exists. Performs an update of the selected document.                                                                                                                                                                                           |
| `new` <span class="type">boolean</span>    | Optional. When **`TRUE`**, returns the modified document rather than the original. The findAndModify method ignores the `new` option for remove operations. The default is **`FALSE`**.                                                                                   |
| `upsert` <span class="type">boolean</span> | Optional. Used in conjunction with the `update` field. When **`TRUE`**, the findAndModify command creates a new document if the query returns no documents. The default is false. In MongoDB 2.2, the findAndModify command returns **`NULL`** when upsert is **`TRUE`**. |
| ``                                         |                                                                                                                                                                                                                                                                           |

### 返回值

Returns the original document, or the modified document when `new` is
set.

### 错误／异常

Throws <span class="classname">MongoResultException</span> on failure.

### 范例

**示例 \#1 <span
class="methodname">MongoCollection::findAndModify</span> example**

``` php
<?php
$m = new Mongo;
$col = $m->selectDB("test")->jobs;

$col->insert(array(
     "name" => "Next promo",
     "inprogress" => false,
     "priority" => 0,
     "tasks" => array( "select product", "add inventory", "do placement"),
) );

$col->insert(array(
     "name" => "Biz report",
     "inprogress" => false,
     "priority" => 1,
     "tasks" => array( "run sales report", "email report" )
) );

$col->insert(array(
     "name" => "Biz report",
     "inprogress" => false,
     "priority" => 2,
     "tasks" => array( "run marketing report", "email report" )
    ),
    array("w" => 1)
);



$retval = $col->findAndModify(
     array("inprogress" => false, "name" => "Biz report"),
     array('$set' => array('inprogress' => true, "started" => new MongoDate())),
     null,
     array(
        "sort" => array("priority" => -1),
        "new" => true,
    )
);

var_dump($retval);
?>
```

以上例程的输出类似于：

    array(6) {
      ["_id"]=>
      object(MongoId)#7 (1) {
        ["$id"]=>
        string(24) "5091b5b244415e8cc3000002"
      }
      ["inprogress"]=>
      bool(true)
      ["name"]=>
      string(10) "Biz report"
      ["priority"]=>
      int(2)
      ["started"]=>
      object(MongoDate)#8 (2) {
        ["sec"]=>
        int(1351726514)
        ["usec"]=>
        int(925000)
      }
      ["tasks"]=>
      array(2) {
        [0]=>
        string(20) "run marketing report"
        [1]=>
        string(12) "email report"
      }
    }

**示例 \#2 <span
class="methodname">MongoCollection::findAndModify</span> error
handling**

``` php
<?php
$m = new Mongo;
$col = $m->selectDB("test")->jobs;
try {
    $retval = $col->findAndModify(
         array("inprogress" => false, "name" => "Next promo"),
         array('$pop' => array("tasks" => -1)),
         array("tasks" => array('$pop' => array("stuff"))),
         array("new" => true)
    );
} catch(MongoResultException $e) {
    echo $e->getCode(), " : ", $e->getMessage(), "\n";
    var_dump($e->getDocument());
}

?>
```

以上例程的输出类似于：

    13097 : exception: Unsupported projection option: $pop
    array(3) {
      ["errmsg"]=>
      string(46) "exception: Unsupported projection option: $pop"
      ["code"]=>
      int(13097)
      ["ok"]=>
      float(0)
    }

### 参见

-   The MongoDB
    <a href="https://docs.mongodb.com/manual/reference/command/findAndModify/" class="link external">» findAndModify command</a>
    docs

MongoCollection::findOne
========================

Queries this collection, returning a single element

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::findOne</span> (\[ <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\]\] )

As opposed to <span class="function">MongoCollection::find</span>, this
method will return only the *first* result from the result set, and not
a <span class="classname">MongoCursor</span> that can be iterated over.

### 参数

`query`  
The fields for which to search. MongoDB's query language is quite
extensive. The PHP driver will in almost all cases pass the query
straight through to the server, so reading the MongoDB core docs on
<a href="https://docs.mongodb.com/manual/reference/method/db.collection.find/" class="link external">» find</a>
is a good idea.

**Warning**
Please make sure that for all special query operaters (starting with
*$*) you use single quotes so that PHP doesn't try to replace
*"$exists"* with the value of the variable *$exists*.

`fields`  
Fields of the results to return. The array is in the format
*array('fieldname' =\> true, 'fieldname2' =\> true)*. The *\_id* field
is always returned.

`options`  
This parameter is an associative array of the form *array("name" =\>
\<value\>, ...)*. Currently supported options are:

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

### 返回值

Returns record matching the search or **`NULL`**.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database.

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 1.5.0 | Added optional `options` argument. |

### 范例

**示例 \#1 <span class="methodname">MongoCollection::findOne</span>
document by its id.**

This example demonstrates how to find a single document in a collection
by its id.

``` php
<?php

$articles = $mongo->my_db->articles;

$article = $articles->findOne(array('_id' => new MongoId('47cc67093475061e3d9536d2')));

?>
```

**示例 \#2 <span class="methodname">MongoCollection::findOne</span>
document by some condition.**

This example demonstrates how to find a single document in a collection
by some condition and limiting the returned fields.

``` php
<?php

$users = $mongo->my_db->users;
$user = $users->findOne(array('username' => 'jwage'), array('password'));
print_r($user);

?>
```

以上例程的输出类似于：

    Array
    (
        [_id] => MongoId Object
            (
            )

        [password] => test
    )

Notice how even though the document does have a username field, we
limited the results to only contain the password field.

### 参见

-   <span class="function">MongoCollection::find</span>
-   <span class="function">MongoCollection::insert</span>
-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/reference/method/db.collection.find/" class="link external">» find</a>.

MongoCollection::\_\_get
========================

Gets a collection

### 说明

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">MongoCollection::\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

A concise syntax for getting a collection with a dot-separated name. If
a collection name contains strange characters, you may have to use <span
class="function">MongoDB::selectCollection</span> instead.

``` php
<?php

$mongo = new MongoClient();

// the following two lines are equivalent
$collection = $mongo->selectDB("foo")->selectCollection("bar.baz");
$collection = $mongo->foo->bar->baz;

?>
```

### 参数

`name`  
The next string in the collection name.

### 返回值

Returns the collection.

MongoCollection::getDBRef
=========================

Fetches the document pointed to by a database reference

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::getDBRef</span> ( <span
class="methodparam"><span class="type">array</span> `$ref`</span> )

### 参数

`ref`  
A database reference.

### 返回值

Returns the database document pointed to by the reference.

### 范例

**示例 \#1 <span class="methodname">MongoCollection::getDBRef</span>
example**

``` php
<?php

$playlists = $db->playlists;

$myList = $playlists->findOne(array('username' => 'me'));

// fetch each song in the playlist
foreach ($myList['songlist'] as $songRef) {
    $song = $playlists->getDBRef($songRef);
    echo $song['title'] . "\n";
}

?>
```

以上例程的输出类似于：

    Dazed and Confused
    Ma na ma na
    Bohemian Rhapsody

  
In the above example each $songRef looks something like the following:  

        Array
        (
            [$ref] => songs
            [$id] => 49902cde5162504500b45c2c
        )
        

### 参见

-   <span class="methodname">MongoCollection::createDBRef</span>

MongoCollection::getIndexInfo
=============================

Returns information about indexes on this collection

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::getIndexInfo</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array in which each element describes an index.
Elements will contain the values *name* for the name of the index, *ns*
for the namespace (a combination of the database and collection name),
and *key* for a list of all fields in the index and their ordering.
Additional values may be present for special indexes, such as *unique*
or *sparse*.

### 范例

**示例 \#1 <span class="function">MongoCollection::getIndexInfo</span>
example**

``` php
<?php

$m = new MongoClient();
$c = $m->selectCollection('test', 'venues');
var_dump($c->getIndexInfo());

?>
```

以上例程的输出类似于：

    array(4) {
      [0]=>
      array(4) {
        ["v"]=>
        int(1)
        ["key"]=>
        array(1) {
          ["_id"]=>
          int(1)
        }
        ["name"]=>
        string(4) "_id_"
        ["ns"]=>
        string(11) "test.venues"
      }
      [1]=>
      array(4) {
        ["v"]=>
        int(1)
        ["key"]=>
        array(1) {
          ["name"]=>
          float(1)
        }
        ["name"]=>
        string(6) "name_1"
        ["ns"]=>
        string(11) "test.venues"
      }
      [2]=>
      array(4) {
        ["v"]=>
        int(1)
        ["key"]=>
        array(2) {
          ["type"]=>
          float(1)
          ["createdAt"]=>
          float(-1)
        }
        ["name"]=>
        string(19) "type_1_createdAt_-1"
        ["ns"]=>
        string(11) "test.venues"
      }
      [3]=>
      array(5) {
        ["v"]=>
        int(1)
        ["key"]=>
        array(1) {
          ["location"]=>
          string(8) "2dsphere"
        }
        ["name"]=>
        string(17) "location_2dsphere"
        ["ns"]=>
        string(11) "test.venues"
        ["2dsphereIndexVersion"]=>
        int(2)
      }
    }

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/indexes/" class="link external">» vanilla indexes</a>
and
<a href="https://docs.mongodb.com/manual/applications/geospatial-indexes/" class="link external">» geospatial indexes</a>.

MongoCollection::getName
========================

返回这个集合的名称

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoCollection::getName</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

获取这个集合的名称。

### 范例

**示例 \#1 <span class="function">MongoCollection::getName</span> 例子**

``` php
<?php

$m = new MongoClient();
$c = $m->foo->bar->baz;

echo "Working with collection " . $c->getName() . ".\n";

// the full namespace is given by the MongoCollection::__toString() method
echo "Working in namespace $c.\n";

?>
```

以上例程的输出类似于：

    Working with collection bar.baz.
    Working in namespace foo.bar.baz.

MongoCollection::getReadPreference
==================================

Get the read preference for this collection

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::getReadPreference</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the read preference. The array
contains the values *type* for the string read preference mode
(corresponding to the <span class="classname">MongoClient</span>
constants), and *tagsets* containing a list of all tag set criteria. If
no tag sets were specified, *tagsets* will not be present in the array.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                               |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.3 | The return value has changed to be consistent with <span class="methodname">MongoCollection::setReadPreference</span>. The *type* value was changed from a number to a string, *type\_string* was removed, and *tagsets* now expresses tags as key/value pairs instead of colon-delimited strings. |

### 范例

**示例 \#1 <span
class="methodname">MongoCollection::getReadPreference</span> return
value example**

``` php
<?php

$m = new MongoClient();
$c = $m->test->users;
$c->setReadPreference(MongoClient::RP_SECONDARY, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
    array(),
));
var_dump($c->getReadPreference());
?>
```

以上例程会输出：

    array(2) {
      ["type"]=>
      string(9) "secondary"
      ["tagsets"]=>
      array(3) {
        [0]=>
        array(2) {
          ["dc"]=>
          string(4) "east"
          ["use"]=>
          string(9) "reporting"
        }
        [1]=>
        array(1) {
          ["dc"]=>
          string(7) "west"
        }
        [2]=>
        array(0) {
        }
      }
    }

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoCollection::setReadPreference</span>

MongoCollection::getSlaveOkay
=============================

Get slaveOkay setting for this collection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCollection::getSlaveOkay</span> ( <span
class="methodparam">void</span> )

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

此函数没有参数。

### 返回值

Returns the value of slaveOkay for this instance.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoCollection::getReadPreference</span>

MongoCollection::getWriteConcern
================================

Get the write concern for this collection

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::getWriteConcern</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the write concern. The array
contains the values *w* for an integer acknowledgement level or string
mode, and *wtimeout* denoting the maximum number of milliseconds to wait
for the server to satisfy the write concern.

### 范例

**示例 \#1 <span
class="methodname">MongoCollection::getWriteConcern</span> return value
example**

``` php
<?php

$mc = new MongoClient('mongodb://localhost:27017', array('wTimeoutMS' => 500));
$coll = $mc->selectCollection('test', 'foo');
var_dump($coll->getWriteConcern());

$coll->setWriteConcern(1, 1000);
var_dump($coll->getWriteConcern());
?>
```

以上例程会输出：

    array(2) {
      ["w"]=>
      int(1)
      ["wtimeout"]=>
      int(500)
    }
    array(2) {
      ["w"]=>
      int(1)
      ["wtimeout"]=>
      int(1000)
    }

### 参见

-   The
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    documentation.
-   <span class="function">MongoCollection::setWriteConcern</span>

MongoCollection::group
======================

Performs an operation similar to SQL's GROUP BY command

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::group</span> ( <span
class="methodparam"><span class="type">mixed</span> `$keys`</span> ,
<span class="methodparam"><span class="type">array</span>
`$initial`</span> , <span class="methodparam"><span
class="type">MongoCode</span> `$reduce`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

### 参数

`keys`  
Fields to group by. If an array or non-code object is passed, it will be
the key used to group results.

1.0.4+: If `keys` is an instance of <span
class="classname">MongoCode</span>, `keys` will be treated as a function
that returns the key to group by (see the "Passing a `keys` function"
example below).

`initial`  
Initial value of the aggregation counter object.

`reduce`  
A function that takes two arguments (the current document and the
aggregation to this point) and does the aggregation.

`options`  
Optional parameters to the group command. Valid options include:

-   *"condition"*

    Criteria for including a document in the aggregation.

-   *"finalize"*

    Function called once per unique key that takes the final output of
    the reduce function.

-   *"maxTimeMS"*

    Specifies a cumulative time limit in milliseconds for processing the
    operation on the server (does not include idle time). If the
    operation is not completed by the server within the timeout period,
    a <span class="classname">MongoExecutionTimeoutException</span> will
    be thrown.

### 返回值

Returns an array containing the result.

### 更新日志

| 版本   | 说明                                                                         |
|--------|------------------------------------------------------------------------------|
| 1.5.0  | Added *"maxTimeMS"* option.                                                  |
| 1.2.11 | Emits **`E_DEPRECATED`** when `options` is <span class="type">scalar</span>. |

### 范例

**示例 \#1 <span class="function">MongoCollection::group</span>
example**

This groups documents by category and creates a list of names within
that category.

``` php
<?php

$collection->insert(array("category" => "fruit", "name" => "apple"));
$collection->insert(array("category" => "fruit", "name" => "peach"));
$collection->insert(array("category" => "fruit", "name" => "banana"));
$collection->insert(array("category" => "veggie", "name" => "corn"));
$collection->insert(array("category" => "veggie", "name" => "broccoli"));

$keys = array("category" => 1);

$initial = array("items" => array());

$reduce = "function (obj, prev) { prev.items.push(obj.name); }";

$g = $collection->group($keys, $initial, $reduce);

echo json_encode($g['retval']);

?>
```

以上例程的输出类似于：

    [{"category":"fruit","items":["apple","peach","banana"]},{"category":"veggie","items":["corn","broccoli"]}]

**示例 \#2 <span class="function">MongoCollection::group</span>
example**

This example doesn't use any key, so every document will be its own
group. It also uses a condition: only documents that match this
condition will be processed by the grouping function.

``` php
<?php

$collection->save(array("a" => 2));
$collection->save(array("b" => 5));
$collection->save(array("a" => 1));

// use all fields
$keys = array();

// set intial values
$initial = array("count" => 0);

// JavaScript function to perform
$reduce = "function (obj, prev) { prev.count++; }";

// only use documents where the "a" field is greater than 1
$condition = array('condition' => array("a" => array( '$gt' => 1)));

$g = $collection->group($keys, $initial, $reduce, $condition);

var_dump($g);

?>
```

以上例程的输出类似于：

    array(4) {
      ["retval"]=>
      array(1) {
        [0]=>
        array(1) {
          ["count"]=>
          float(1)
        }
      }
      ["count"]=>
      float(1)
      ["keys"]=>
      int(1)
      ["ok"]=>
      float(1)
    }

**示例 \#3 Passing a `keys` function**

If you want to group by something other than a field name, you can pass
a function as the first parameter of <span
class="function">MongoCollection::group</span> and it will be run
against each document. The return value of the function will be used as
its grouping value.

This example demonstrates grouping by the num field modulo 4.

``` php
<?php

$c->group(new MongoCode('function(doc) { return {mod : doc.num % 4}; }'),
     array("count" => 0),
     new MongoCode('function(current, total) { total.count++; }'));

?>
```

MongoCollection::insert
=======================

插入文档到集合中

### 说明

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span
class="methodname">MongoCollection::insert</span> ( <span
class="methodparam"><span class="type">array\|object</span> `$a`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`<span class="initializer"> = array()</span></span> \] )

发送到数据库的所有字符串必须是 UTF-8 的。如果有字符串不是
UTF-8，将会抛出 <span class="classname">MongoException</span> 异常。
要插入（或者查询）一个非 UTF-8 的字符串，请使用 <span
class="classname">MongoBinData</span>。

### 参数

`a`  
一个数组或对象。如果使用的是一个对象，它不能有 protected 或 private
的属性。

> **Note**:
>
> 如果参数不具有 *\_id* 键或属性， 将会创建一个新的 <span
> class="classname">MongoId</span> 实例，并赋值给它。
> 这种特殊行为不意味着参数是传引用的。

`options`  
插入的选项。

-   *"fsync"*

    Boolean, defaults to **`FALSE`**. If journaling is enabled, it works
    exactly like *"j"*. If journaling is not enabled, the write
    operation blocks until it is synced to database files on disk. If
    **`TRUE`**, an acknowledged insert is implied and this option will
    override setting *"w"* to *0*.

    > **Note**: <span class="simpara">If journaling is enabled, users
    > are strongly encouraged to use the *"j"* option instead of
    > *"fsync"*. Do not use *"fsync"* and *"j"* simultaneously, as that
    > will result in an error.</span>

-   *"j"*

    Boolean, defaults to **`FALSE`**. Forces the write operation to
    block until it is synced to the journal on disk. If **`TRUE`**, an
    acknowledged write is implied and this option will override setting
    *"w"* to *0*.

    > **Note**: <span class="simpara">If this option is used and
    > journaling is disabled, MongoDB 2.6+ will raise an error and the
    > write will fail; older server versions will simply ignore the
    > option.</span>

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

### 返回值

如果设置了 *"w"* 选项，将会返回包含插入状态的数组。 否则，将会返回一个
**`TRUE`** 代表数组不是空的（空数组将会抛出 <span
class="classname">MongoException</span> ）。

如果返回了一个 array，将会有以下键：

`ok`  
它应该几乎总是 1（除非 last\_error 本身出现错误）。

`err`  
如果这个字段不是 null，说明刚才的操作出现了错误。
如果有这个字段，它将包含一个字符串，用于描述出现的错误信息。

`code`  
如果发生了一个数据库错误，相应的错误码会传到客户端。

`errmsg`  
如果数据库命令出现了错误，将会设置这个字段。同时 *ok* 也会是 0.
例如，设置了 *w* 并且超时了，errmsg 将会是 "timed out waiting for
slaves" 并且 *ok* 是 0。
如果设置了这个字段，它会是发生的错误的字符串描述。

`n`  
如果最后的操作是插入、更新或删除，将会返回受影响的对象数量。对于插入操作，这个值总是
*0*。

`wtimeout`  
等待复制直到超时的时间。

`waited`  
在超时前，要等待操作多久。

`wtime`  
如果设置了 *w* 并且操作成功了，等到复制到 *w* 台服务器的时间。

`upserted`  
如果发生了一次 upsert，这个字段将会包含新记录的 *\_id*。 对于
upsert，不管是该字段还是 *updatedExisting*
都会被保留（除非发生了一个错误）。

`updatedExisting`  
如果一个 upsert 更新了一个存在的元素，这个字段将会是 true。 对于
upsert，无论是这个字段 还是 upserted 都会被保留（除非发生了错误）。

### 错误／异常

如果插入的文档是空的，或者包含零长度的键，将会抛出 <span
class="classname">MongoException</span>。 尝试插入包含 protected 和
private 属性的对象将会导致零长度键（zero-length key）的错误。

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.3.0</td>
<td><code class="parameter">options</code> 参数不再接受 boolean 来标识一个确认的写入。 现在，你可以通过 <em>array('w' =&gt; 1)</em> 设置（ <span class="classname">MongoClient</span> 默认的行为）</td>
</tr>
<tr class="even">
<td>1.2.0</td>
<td>增加了 <em>"timeout"</em> 选项。</td>
</tr>
<tr class="odd">
<td>1.0.11</td>
<td>如果设置了 <em>"safe"</em>，出现 "not master" 错误时断开连接。</td>
</tr>
<tr class="even">
<td>1.0.9</td>
<td><p><em>"safe"</em> 选项接受 integer 值，之前只接受 boolean 值。</p>
<p>增加 <em>"fsync"</em> 选项。</p>
<p>如果设置了 <em>"safe"</em> 选项，返回类型改成包含错误信息的 array。 否则，和之前一样返回 boolean。</p></td>
</tr>
<tr class="odd">
<td>1.0.5</td>
<td>修改第二个参数为选项数组。在 1.0.5 之前，第二个参数是 boolean，指示 <em>"safe"</em> 选项。</td>
</tr>
<tr class="even">
<td>1.0.1</td>
<td>如果设置了 <em>"safe"</em> 选项并且插入失败了，将会抛出 <span class="classname">MongoCursorException</span>。</td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">MongoCollection::insert</span> *\_id*
例子**

如果没有 *\_id*，则会添加一个到插入的文档中。
基于参数传入的方式，在调用代码时可能无法产生有效 *\_id*。

``` php
<?php

$m = new MongoClient();
$collection = $m->selectCollection('test', 'phpmanual');
// 如果使用的是 array 字面语法，将无法成功生成 _id
$collection->insert(array('x' => 1));

// 通过传 array 的变量可以生成 _id
$a = array('x' => 2);
$collection->insert($a);
var_dump($a);

// 通过传引用的 array 无法生成 _id
$b = array('x' => 3);
$ref = &$b;
$collection->insert($ref);
var_dump($ref);

// 没有在包裹的函数中触发 copy-on-write 时 _id 有效
function insert_no_cow($collection, $document)
{
    $collection->insert($document);
}

$c = array('x' => 4);
insert_no_cow($collection, $c);
var_dump($c);

// 在包裹的函数中触发 copy-on-write 时 _id 无效
function insert_cow($collection, $document)
{
    $document['y'] = 1;
    $collection->insert($document);
}

$d = array('x' => 5);
insert_cow($collection, $d);
var_dump($d);

?>
```

以上例程的输出类似于：

    array(2) {
      ["x"]=>
      int(2)
      ["_id"]=>
      object(MongoId)#4 (0) {
      }
    }
    array(1) {
      ["x"]=>
      int(3)
    }
    array(2) {
      ["x"]=>
      int(4)
      ["_id"]=>
      object(MongoId)#5 (0) {
      }
    }
    array(1) {
      ["x"]=>
      int(5)
    }

**示例 \#2 <span class="function">MongoCollection::insert</span>
确认写入的例子**

这个例子显示了设置了 `w` 后，插入两个具有相同 \_id 的元素时，导致抛出
<span class="classname">MongoCursorException</span> 的例子。

``` php
<?php

$person = array("name" => "Joe", "age" => 20);
$collection->insert($person);

// 现在 $person 具有一个 _id 字段，所以我们再次 
// 保存它的时候，将会得到一个异常
try {
    $collection->insert($person, array("w" => 1));
} catch(MongoCursorException $e) {
    echo "Can't save the same person twice!\n";
}

?>
```

### 参见

-   <span class="function">MongoCollection::batchInsert</span>
-   <span class="function">MongoCollection::update</span>
-   <span class="function">MongoCollection::find</span>
-   <span class="function">MongoCollection::remove</span>
-   MongoDB
    <a href="https://docs.mongodb.com/manual/tutorial/insert-documents/" class="link external">» insert</a>
    的核心文档。

MongoCollection::parallelCollectionScan
=======================================

Returns an array of cursors to iterator over a full collection in
parallel

### 说明

<span class="modifier">public</span> <span
class="type">array\[MongoCommandCursor\]</span> <span
class="methodname">MongoCollection::parallelCollectionScan</span> (
<span class="methodparam"><span class="type">int</span>
`$num_cursors`</span> )

This method returns an array of a maximum of *num\_cursors* cursors. An
iteration over one of the returned cursors results in a partial set of
documents for a collection. Iteration over all the returned cursors
results in getting every document back from the collection.

This method is a wrapper for the *parallelCollectionScan* MongoDB
command.

### 参数

`num_cursors`  
The number of cursors to request from the server. Please note, that the
server can return less cursors than you requested.

### 返回值

Returns an array of <span class="classname">MongoCommandCursor</span>
objects.

### 范例

**示例 \#1 <span
class="function">MongoCollection::parallelCollectionScan</span>
example**

Returning all documents in a collection by using multiple cursors.

``` php
<?php
$m = new MongoClient;
$c = $m->demo->cities;

/* Request three cursors */
$cursors = $c->parallelCollectionScan( 3 );

/* Add all the cursors to the MultipleIterator */
$mi = new MultipleIterator( MultipleIterator::MIT_NEED_ANY );
foreach ( $cursors as $cursor )
{
    $mi->attachIterator( $cursor );
}

/* Iterate over all the associated cursors */
foreach ( $mi as $items )
{
    foreach ( $items as $item )
    {
        if ( $item !== NULL )
        {
            echo $item['name'], "\n";
        }
    }
}
?>
```

### 参见

-   <span class="classname">MultipleIterator</span>
-   <span class="classname">MongoCommandCursor</span>
-   <span class="methodname">MongoDB::command</span>

MongoCollection::remove
=======================

从集合中删除记录

### 说明

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span
class="methodname">MongoCollection::remove</span> (\[ <span
class="methodparam"><span class="type">array</span> `$criteria`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`criteria`  
待删除记录的描述。

`options`  
删除的选项。

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"justOne"*

    最多只删除一个匹配的记录。

-   *"fsync"*

    Boolean, defaults to **`FALSE`**. If journaling is enabled, it works
    exactly like *"j"*. If journaling is not enabled, the write
    operation blocks until it is synced to database files on disk. If
    **`TRUE`**, an acknowledged insert is implied and this option will
    override setting *"w"* to *0*.

    > **Note**: <span class="simpara">If journaling is enabled, users
    > are strongly encouraged to use the *"j"* option instead of
    > *"fsync"*. Do not use *"fsync"* and *"j"* simultaneously, as that
    > will result in an error.</span>

-   *"j"*

    Boolean, defaults to **`FALSE`**. Forces the write operation to
    block until it is synced to the journal on disk. If **`TRUE`**, an
    acknowledged write is implied and this option will override setting
    *"w"* to *0*.

    > **Note**: <span class="simpara">If this option is used and
    > journaling is disabled, MongoDB 2.6+ will raise an error and the
    > write will fail; older server versions will simply ignore the
    > option.</span>

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

### 返回值

如果设置了 *"w"* 选项，将会返回包含删除状态的 array。 否则返回
**`TRUE`**。

状态数组字段的解释位于 <span
class="function">MongoCollection::insert</span> 的文档。

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.3.0</td>
<td><code class="parameter">options</code> 参数不再接受 boolean 值来代表 <em>"justOne"</em>。 现在，必须使用 <em>array('justOne' =&gt; true)</em> 作为替代。</td>
</tr>
<tr class="even">
<td>1.2.11</td>
<td>当 <code class="parameter">options</code> 是 <span class="type">scalar</span> 时产生一个 <strong><code>E_DEPRECATED</code></strong> 警告。</td>
</tr>
<tr class="odd">
<td>1.2.0</td>
<td>添加 <em>"timeout"</em> 选项。</td>
</tr>
<tr class="even">
<td>1.0.11</td>
<td>在设置了 <em>"safe"</em> 之后，将在出现 "not master" 错误时断开连接。</td>
</tr>
<tr class="odd">
<td>1.0.9</td>
<td><p>添加了 <em>"safe"</em> 选项对 integer 的支持，之前只接受 boolean 值。</p>
<p>添加了 <em>"fsync"</em> 选项。</p>
<p>当使用了 <em>"safe"</em> 选项时将会返回包含错误信息的数组。 否则和之前一样返回一个 boolean。</p></td>
</tr>
<tr class="even">
<td>1.0.5</td>
<td>修改第二个参数为选项的 array。在 1.0.5 之前，第二个选项是 boolean 值， 代表了 <em>"safe"</em> 选项。</td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">MongoCollection::remove</span> 的
justOne 例子**

``` php
<?php

$radioactive = $db->radioactive;

// 统计那有多少个钚
$remaining = $radioactive->count(array('type' => 94));

$halflife = $remaining/2;

// 删除一半
while ($halflife > 0) {
    $radioactive->remove(array('type' => 94), array("justOne" => true));
    $halflife--;
}

?>
```

### 参见

-   <span class="function">MongoCollection::insert</span>
-   <span class="function">MongoCollection::update</span>
-   MongoDB
    <a href="https://docs.mongodb.com/manual/tutorial/remove-documents/" class="link external">» remove</a>
    的核心文档。

MongoCollection::save
=====================

保存一个文档到集合

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoCollection::save</span> ( <span
class="methodparam"><span class="type">array\|object</span>
`$document`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

如果对象来自数据库，则更新现有的数据库对象，否则插入对象。

### 参数

`document`  
要保存的 Array 或 Object。 如果用的是 Object，它不能有 protected 或
private 的属性。

> **Note**:
>
> 如果参数不具有 *\_id* 的键或者属性，将会创建并赋值一个新的 <span
> class="classname">MongoId</span> 实例。 关于此行为的更多信息，参见
> <span class="function">MongoCollection::insert</span>。

`options`  
此次保存的选项。

-   *"fsync"*

    Boolean, defaults to **`FALSE`**. If journaling is enabled, it works
    exactly like *"j"*. If journaling is not enabled, the write
    operation blocks until it is synced to database files on disk. If
    **`TRUE`**, an acknowledged insert is implied and this option will
    override setting *"w"* to *0*.

    > **Note**: <span class="simpara">If journaling is enabled, users
    > are strongly encouraged to use the *"j"* option instead of
    > *"fsync"*. Do not use *"fsync"* and *"j"* simultaneously, as that
    > will result in an error.</span>

-   *"j"*

    Boolean, defaults to **`FALSE`**. Forces the write operation to
    block until it is synced to the journal on disk. If **`TRUE`**, an
    acknowledged write is implied and this option will override setting
    *"w"* to *0*.

    > **Note**: <span class="simpara">If this option is used and
    > journaling is disabled, MongoDB 2.6+ will raise an error and the
    > write will fail; older server versions will simply ignore the
    > option.</span>

-   *"socketTimeoutMS"*

    This option specifies the time limit, in milliseconds, for socket
    communication. If the server does not respond within the timeout
    period, a <span class="classname">MongoCursorTimeoutException</span>
    will be thrown and there will be no way to determine if the server
    actually handled the write or not. A value of *-1* may be specified
    to block indefinitely. The default value for <span
    class="classname">MongoClient</span> is *30000* (30 seconds).

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

-   *"wTimeoutMS"*

    This option specifies the time limit, in milliseconds, for
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    acknowledgement. It is only applicable when *"w"* is greater than
    *1*, as the timeout pertains to replication. If the write concern is
    not satisfied within the time limit, a <span
    class="classname">MongoCursorException</span> will be thrown. A
    value of *0* may be specified to block indefinitely. The default
    value for <span class="classname">MongoClient</span> is *10000* (ten
    seconds).

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

### 返回值

如果设置了 `w`，返回包含此次保存状态的一个 array。 否则，返回一个
boolean，表示数组是否为空（空数组不会被插入）。

### 错误／异常

如果插入的文档时空的，或者包含零长度的键，将抛出 <span
class="classname">MongoException</span>。 尝试插入包含 protected 和
private 属性的对象将导致零长度键的错误。

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.5.0</td>
<td><p>增加 <em>"wTimeoutMS"</em> 选项来代替 <em>"wtimeout"</em>。 使用 <em>"wtimeout"</em> 时出现 <strong><code>E_DEPRECATED</code></strong> 错误。</p>
<p>新增 <em>"socketTimeoutMS"</em> 选项来代替 <em>"timeout"</em>。 使用 <em>"timeout"</em> 时出现 <strong><code>E_DEPRECATED</code></strong> 错误。</p>
<p>使用 <em>"safe"</em> 时出现 <strong><code>E_DEPRECATED</code></strong> 错误。</p></td>
</tr>
<tr class="even">
<td>1.2.0</td>
<td>增加 <em>"timeout"</em> 选项。</td>
</tr>
<tr class="odd">
<td>1.0.11</td>
<td>设置 <em>"safe"</em> 时，当出现 "not master" 错误时主动断开连接。</td>
</tr>
<tr class="even">
<td>1.0.9</td>
<td><p>增加 <em>"fsync"</em> 选项。</p></td>
</tr>
<tr class="odd">
<td>1.0.5</td>
<td>增加 <code class="parameter">options</code> 参数。</td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">MongoCollection::save</span> 例子**

``` php
<?php

$obj = array('x' => 1);

// 插入 $obj 到 db
$collection->save($obj);
var_dump($obj);

// 增加额外的字段
$obj['foo'] = 'bar';

// $obj 不能被再次插入，导致 duplicate _id 错误
$collection->insert($obj);

// 保存、更新附带新字段的 $obj
$collection->save($obj);

?>
```

以上例程的输出类似于：

    array(2) {
      ["x"]=>
      int(1)
      ["_id"]=>
      object(MongoId)#4 (1) {
        ["$id"]=>
        string(24) "50b6afe544415ed606000000"
      }
    }

MongoCollection::setReadPreference
==================================

Set the read preference for this collection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCollection::setReadPreference</span> (
<span class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

### 参数

`read_preference`  
The read preference mode: **`MongoClient::RP_PRIMARY`**,
**`MongoClient::RP_PRIMARY_PREFERRED`**,
**`MongoClient::RP_SECONDARY`**,
**`MongoClient::RP_SECONDARY_PREFERRED`**, or
**`MongoClient::RP_NEAREST`**.

`tags`  
An array of zero or more tag sets, where each tag set is itself an array
of criteria used to match tags on replica set members.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** otherwise.

### 错误／异常

Emits **`E_WARNING`** if either parameter is invalid, or if one or more
tag sets are provided with the **`MongoClient::RP_PRIMARY`** read
preference mode.

### 范例

**示例 \#1 <span
class="methodname">MongoCollection::setReadPreference</span> tag set
array syntax example**

``` php
<?php

$m = new MongoClient();
$c = $m->test->users;

// Prefer the nearest server in the "east" data center also used for reporting,
// but fall back to a server in the "west" data center
$c->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
));
?>
```

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoCollection::getReadPreference</span>

MongoCollection::setSlaveOkay
=============================

Change slaveOkay setting for this collection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCollection::setSlaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$ok`<span
class="initializer"> = **`TRUE`**</span></span> \] )

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

`ok`  
If reads should be sent to secondary members of a replica set for all
possible queries using this <span
class="classname">MongoCollection</span> instance.

### 返回值

Returns the former value of slaveOkay for this instance.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoCollection::setReadPreference</span>

MongoCollection::setWriteConcern
================================

Set the write concern for this database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCollection::setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

### 参数

`w`  
The write concern. This may be an integer denoting the number of servers
required to acknowledge the write, or a string mode (e.g. "majority").

`wtimeout`  
The maximum number of milliseconds to wait for the server to satisfy the
write concern.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** otherwise.

### 错误／异常

Emits **`E_WARNING`** if the *w* parameter is not an integer or string
value.

### 范例

**示例 \#1 <span class="methodname">MongoDB::setWriteConcern</span>
example**

``` php
<?php

$mc = new MongoClient('mongodb://rs1.example.com,rs2.example.com');
$coll = $mc->selectCollection('test', 'foo');

// Require that the majority of servers in the replica set acknowledge writes
// within three seconds.
$coll->setWriteConcern('majority', 3000);
?>
```

### 参见

-   The
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    documentation.
-   <span class="function">MongoCollection::getWriteConcern</span>

MongoCollection::toIndexString
==============================

Converts keys specifying an index to its identifying string

### 说明

<span class="modifier">static protected</span> <span
class="type">string</span> <span
class="methodname">MongoCollection::toIndexString</span> ( <span
class="methodparam"><span class="type">mixed</span> `$keys`</span> )

**Warning**

This method is deprecated since version 1.5.0.

### 参数

`keys`  
Field or fields to convert to the identifying string

### 返回值

Returns a string that describes the index.

### 范例

**示例 \#1 <span class="function">MongoCollection::toIndexString</span>
example**

This example shows how you can create an index name out of keys. Because
this is a protected (static) method, you need to overload it in a child
class first.

``` php
<?php
// Create inherited class to make the method "public".
class MyCollection extends MongoCollection
{
    static public function toIndexString($a)
    {
        return parent::toIndexString($a);
    }
}

echo MyCollection::toIndexString("foo"), "\n";
// Outputs: foo_1

echo MyCollection::toIndexString(array('name' => 1, 'age' => -1)), "\n";
// Outputs: name_1_age_-1
?>
```

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/indexes/" class="link external">» indexes</a>.

### 更新日志

| 版本  | 说明                             |
|-------|----------------------------------|
| 1.5.0 | This method has been deprecated. |

MongoCollection::\_\_toString
=============================

String representation of this collection

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoCollection::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the full name of this collection.

### 范例

**示例 \#1 <span class="function">MongoCollection::\_\_toString</span>
example**

``` php
<?php

$m = new MongoClient();

$c1 = $m->foo->bar->baz;
echo "Working with collection $c1.";

$c2 = $m->selectCollection('[]', '&');
echo "Working with collection $c2.";

?>
```

以上例程的输出类似于：

    Working with collection foo.bar.baz.
    Working with collection [].&.

MongoCollection::update
=======================

Update records based on a given criteria

### 说明

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span
class="methodname">MongoCollection::update</span> ( <span
class="methodparam"><span class="type">array</span> `$criteria`</span> ,
<span class="methodparam"><span class="type">array</span>
`$new_object`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

### 参数

`criteria`  
Query criteria for the documents to update.

`new_object`  
The object used to update the matched documents. This may either contain
update operators (for modifying specific fields) or be a replacement
document.

`options`  
An array of options for the update operation. Currently available
options include:

-   *"upsert"*

    If no document matches `$criteria`, a new document will be inserted.

    If a new document would be inserted and `$new_object` contains
    atomic modifiers (i.e. *$* operators), those operations will be
    applied to the `$criteria` parameter to create the new document. If
    `$new_object` does not contain atomic modifiers, it will be used
    as-is for the inserted document. See the upsert examples below for
    more information.

-   *"multiple"*

    All documents matching $criteria will be updated. <span
    class="function">MongoCollection::update</span> has exactly the
    opposite behavior of <span
    class="function">MongoCollection::remove</span>: it updates one
    document by default, not all matching documents. *It is recommended
    that you always specify whether you want to update multiple
    documents or a single document*, as the database may change its
    default behavior at some point in the future.

-   *"fsync"*

    Boolean, defaults to **`FALSE`**. If journaling is enabled, it works
    exactly like *"j"*. If journaling is not enabled, the write
    operation blocks until it is synced to database files on disk. If
    **`TRUE`**, an acknowledged insert is implied and this option will
    override setting *"w"* to *0*.

    > **Note**: <span class="simpara">If journaling is enabled, users
    > are strongly encouraged to use the *"j"* option instead of
    > *"fsync"*. Do not use *"fsync"* and *"j"* simultaneously, as that
    > will result in an error.</span>

-   *"j"*

    Boolean, defaults to **`FALSE`**. Forces the write operation to
    block until it is synced to the journal on disk. If **`TRUE`**, an
    acknowledged write is implied and this option will override setting
    *"w"* to *0*.

    > **Note**: <span class="simpara">If this option is used and
    > journaling is disabled, MongoDB 2.6+ will raise an error and the
    > write will fail; older server versions will simply ignore the
    > option.</span>

-   *"socketTimeoutMS"*

    This option specifies the time limit, in milliseconds, for socket
    communication. If the server does not respond within the timeout
    period, a <span class="classname">MongoCursorTimeoutException</span>
    will be thrown and there will be no way to determine if the server
    actually handled the write or not. A value of *-1* may be specified
    to block indefinitely. The default value for <span
    class="classname">MongoClient</span> is *30000* (30 seconds).

-   *"w"*

    See
    <a href="/book/mongo.html#Write%20Concerns" class="link">Write Concerns</a>.
    The default value for <span class="classname">MongoClient</span> is
    *1*.

-   *"wTimeoutMS"*

    This option specifies the time limit, in milliseconds, for
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    acknowledgement. It is only applicable when *"w"* is greater than
    *1*, as the timeout pertains to replication. If the write concern is
    not satisfied within the time limit, a <span
    class="classname">MongoCursorException</span> will be thrown. A
    value of *0* may be specified to block indefinitely. The default
    value for <span class="classname">MongoClient</span> is *10000* (ten
    seconds).

The following options are deprecated and should no longer be used:

-   *"safe"*

    Deprecated. Please use the
    <a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
    *"w"* option.

-   *"timeout"*

    Deprecated alias for *"socketTimeoutMS"*.

-   *"wtimeout"*

    Deprecated alias for *"wTimeoutMS"*.

### 返回值

Returns an array containing the status of the update if the *"w"* option
is set. Otherwise, returns **`TRUE`**.

Fields in the status array are described in the documentation for <span
class="function">MongoCollection::insert</span>.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.5.0</td>
<td><p>Added the <em>"wTimeoutMS"</em> option, which replaces <em>"wtimeout"</em>. Emits <strong><code>E_DEPRECATED</code></strong> when <em>"wtimeout"</em> is used.</p>
<p>Added the <em>"socketTimeoutMS"</em> option, which replaces <em>"timeout"</em>. Emits <strong><code>E_DEPRECATED</code></strong> when <em>"timeout"</em> is used.</p>
<p>Emits <strong><code>E_DEPRECATED</code></strong> when <em>"safe"</em> is used.</p></td>
</tr>
<tr class="even">
<td>1.3.4</td>
<td>Added <em>"wtimeout"</em> option.</td>
</tr>
<tr class="odd">
<td>1.3.0</td>
<td><p>Added <em>"w"</em> option.</p>
<p>The <code class="parameter">options</code> parameter no longer accepts a boolean to signify an upsert. Instead, this now has to be done with <em>array('upsert' =&gt; true)</em>.</p></td>
</tr>
<tr class="even">
<td>1.2.11</td>
<td>Emits <strong><code>E_DEPRECATED</code></strong> when <code class="parameter">options</code> is <span class="type">scalar</span>.</td>
</tr>
<tr class="odd">
<td>1.2.0</td>
<td>Added <em>"timeout"</em> option.</td>
</tr>
<tr class="even">
<td>1.0.11</td>
<td>Disconnects on "not master" errors if <em>"safe"</em> is set.</td>
</tr>
<tr class="odd">
<td>1.0.9</td>
<td><p>Added ability to pass integers to the <em>"safe"</em> option, which previously only accepted booleans.</p>
<p>Added <em>"fsync"</em> option.</p>
<p>The return type was changed to be an array containing error information if the <em>"safe"</em> option is used. Otherwise, a boolean is returned as before.</p></td>
</tr>
<tr class="even">
<td>1.0.5</td>
<td>Added <em>"safe"</em> option.</td>
</tr>
<tr class="odd">
<td>1.0.1</td>
<td>Changed <code class="parameter">options</code> parameter from boolean to array. Pre-1.0.1, the second parameter was an optional boolean value specifying an upsert.</td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">MongoCollection::update</span>**

Adding an address field to a document.

``` php
<?php

$c->insert(array("firstname" => "Bob", "lastname" => "Jones" ));
$newdata = array('$set' => array("address" => "1 Smith Lane"));
$c->update(array("firstname" => "Bob"), $newdata);

var_dump($c->findOne(array("firstname" => "Bob")));

?>
```

以上例程的输出类似于：

    array(4) {
      ["_id"]=>
      object(MongoId)#6 (0) {
      }
      ["firstname"]=>
      string(3) "Bob"
      ["lastname"]=>
      string(5) "Jones"
      ["address"]=>
      string(12) "1 Smith Lane"
    }

**示例 \#2 <span class="function">MongoCollection::update</span> upsert
examples**

Upserts can simplify code, as a single line can create the document if
it does not exist (based on `$criteria`), or update an existing document
if it matches.

In the following example, `$new_object` contains an atomic modifier.
Since the collection is empty and upsert must insert a new document, it
will apply those operations to the `$criteria` parameter in order to
create the document.

``` php
<?php

$c->drop();
$c->update(
    array("uri" => "/summer_pics"),
    array('$inc' => array("page hits" => 1)),
    array("upsert" => true)
);
var_dump($c->findOne());

?>
```

以上例程的输出类似于：

    array(3) {
      ["_id"]=>
      object(MongoId)#9 (0) {
      }
      ["uri"]=>
      string(12) "/summer_pics"
      ["page hits"]=>
      int(1)
    }

If `$new_object` does not contain atomic modifiers (i.e. *$* operators),
upsert will use `$new_object` as-is for the new document. This matches
the behavior of a normal update, where not using atomic modifiers causes
the document to be overwritten.

``` php
<?php

$c->drop();
$c->update(
    array("name" => "joe"),
    array("username" => "joe312", "createdAt" => new MongoDate()), 
    array("upsert" => true)
);
var_dump($c->findOne());

?>
```

以上例程的输出类似于：

    array(3) {
      ["_id"]=>
      object(MongoId)#10 (0) {
      }
      ["username"]=>
      string(6) "joe312"
      ["createdAt"]=>
      object(MongoDate)#4 (0) {
      }
    }

**示例 \#3 <span class="function">MongoCollection::update</span>
multiple example**

By default, <span class="function">MongoCollection::update</span> will
only update the first document matching `$criteria` that it finds. Using
the "multiple" option can override this behavior, if needed.

This example adds a "gift" field to every person whose birthday is in
the next day.

``` php
<?php

$today = array('$gt' => new MongoDate(), '$lt' => new MongoDate(strtotime("+1 day")));
$people->update(
    array("birthday" => $today),
    array('$set' => array('gift' => $surprise)),
    array("multiple" => true)
);

?>
```

### 参见

The
<a href="/book/mongo.html#Updates" class="link">PHP documentation on updates</a>
and the
<a href="https://docs.mongodb.com/manual/tutorial/modify-documents/" class="link external">» MongoDB core docs</a>.

MongoCollection::validate
=========================

Validates this collection

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCollection::validate</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$scan_data`<span
class="initializer"> = **`FALSE`**</span></span> \] )

### 参数

`scan_data`  
Only validate indices, not the base collection.

### 返回值

Returns the database's evaluation of this object.

简介
----

A cursor is used to iterate through the results of a database query. For
example, to query the database and see all results, you could do:

**示例 \#1 <span class="classname">MongoCursor</span> basic usage**

``` php
<?php

$cursor = $collection->find();
var_dump(iterator_to_array($cursor));

?>
```

You don't generally create cursors using the <span
class="classname">MongoCursor</span> constructor, you get a new cursor
by calling <span class="function">MongoCollection::find</span> (as shown
above).

Suppose that, in the example above, *$collection* was a 50GB collection.
We certainly wouldn't want to load that into memory all at once, which
is what a cursor is for: allowing the client to access the collection in
dribs and drabs.

If we have a large result set, we can iterate through it, loading a few
megabytes of results into memory at a time. For example, we could do:

**示例 \#2 Iterating over <span class="classname">MongoCursor</span>**

``` php
<?php

$cursor = $collection->find();

foreach ($cursor as $doc) {
    // do something to each document
}

?>
```

This will go through each document in the collection, loading and
garbage collecting documents as needed.

Note that this means that a cursor does not "contain" the database
results, it just manages them. Thus, if you print a cursor (with, say,
<span class="function">var\_dump</span> or <span
class="function">print\_r</span>), you'll just get the cursor object,
not your documents. To get the documents themselves, you can use one of
the methods shown above.

Cursor Stages
-------------

A <span class="classname">MongoCursor</span> has two "life stages": pre-
and post- query. When a cursor is created, it has not yet contacted the
database, so it is in its pre-query state. In this state, the client can
further specify what they want the query to do, including adding limits,
skips, sorts, and more advanced options.

When the client attempts to get a result (by calling <span
class="function">MongoCursor::next</span>, directly or indirectly), the
cursor moves into the post-query stage. At this point, the query has
been executed by the database and cannot be modified anymore.

**示例 \#3 Adding options to <span
class="classname">MongoCursor</span>**

``` php
<?php

$cursor = $collection->find()->limit(10);

// database has not yet been queried, so more search options can be added
$cursor = $cursor->sort(array("a" => 1));

var_dump($cursor->getNext());
// now database has been queried and more options cannot be added

// so this will throw an exception:
$cursor->skip(4);
?>
```

类摘要
------

**MongoCursor**

<span class="ooclass"> class **MongoCursor** </span> <span
class="oointerface">implements <span
class="interfacename">MongoCursorInterface</span> </span> <span
class="oointerface">, <span class="interfacename">Iterator</span>
</span> {

/\* Static Fields \*/

<span class="modifier">static</span> <span class="type">boolean</span>
`$slaveOkay` <span class="initializer"> = **`FALSE`**</span> ;

<span class="modifier">static</span> <span class="type">integer</span>
`$timeout` <span class="initializer"> = 30000</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">addOption</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">awaitData</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$wait`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">batchSize</span> ( <span class="methodparam"><span
class="type">int</span> `$batchSize`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoClient</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$ns`</span> \[, <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$foundOnly`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">dead</span> ( <span
class="methodparam">void</span> )

<span class="modifier">protected</span> <span class="type">void</span>
<span class="methodname">doQuery</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">explain</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">fields</span> (
<span class="methodparam"><span class="type">array</span> `$f`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getNext</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasNext</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">hint</span> (
<span class="methodparam"><span class="type">mixed</span>
`$index`</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">immortal</span>
(\[ <span class="methodparam"><span class="type">bool</span>
`$liveForever`<span class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">info</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">string\|int</span> <span class="methodname">key</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">limit</span> (
<span class="methodparam"><span class="type">int</span> `$num`</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">maxTimeMS</span> ( <span class="methodparam"><span
class="type">int</span> `$ms`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">partial</span>
(\[ <span class="methodparam"><span class="type">bool</span>
`$okay`<span class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">reset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">setFlag</span>
( <span class="methodparam"><span class="type">int</span> `$flag`</span>
\[, <span class="methodparam"><span class="type">bool</span> `$set`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">skip</span> (
<span class="methodparam"><span class="type">int</span> `$num`</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">slaveOkay</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$okay`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">snapshot</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">sort</span> (
<span class="methodparam"><span class="type">array</span>
`$fields`</span> )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">tailable</span>
(\[ <span class="methodparam"><span class="type">bool</span>
`$tail`<span class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span class="methodname">timeout</span>
( <span class="methodparam"><span class="type">int</span> `$ms`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

Static Variables
----------------

`slaveOkay`  
If the query should have the "slaveOkay" flag set, which allows reads on
the secondary (secondaries are, by default, just for backup and not
queried). Can be overridden with <span
class="function">MongoCursor::slaveOkay</span>.

This functionality is *deprecated*. Please use
<a href="/book/mongo.html#读取首选项" class="xref"></a> instead.

`timeout`  
Set timeout in milliseconds for all database responses. Use *-1* to wait
forever. Can be overridden with <span
class="function">MongoCursor::timeout</span>. This does not cause the
MongoDB server to cancel the operation; it only instructs the driver to
stop waiting for a response and throw a <span
class="classname">MongoCursorTimeoutException</span> after a set time.

参见
----

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/core/cursors/" class="link external">» cursors</a>.

MongoCursor::addOption
======================

Adds a top-level key/value pair to a query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::addOption</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

This is an advanced function and should not be used unless you know what
you're doing.

A query can optionally be nested in a "query" field if other options,
such as a sort or hint, are given. For instance, adding a sort causes
the query to become a subfield of a bigger query object, like:

``` php
<?php

$query = array("query" => $query, "orderby" => $sort);

?>
```

This method is for adding a top-level field to a query. It makes the
query a subobject (if it isn't already) and adds the key/value pair of
your chosing to the top level.

**Warning**

It cannot be used to add extra criteria to a query on the fly. For
instance, this *will not* work:

``` php
<?php

// NOT CORRECT
$cursor = $users->find()->addOption("name", "joe")->addOption("age", 20);

?>
```

This *does not* query for a user named "joe" with an age of 20.

### 参数

`key`  
Fieldname to add.

`value`  
Value to add.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 范例

**示例 \#1 Adding a comment with <span
class="function">MongoCursor::addOption</span> example**

MongoDB supports special options to be send to the server. The shell
uses the *\_addSpecial* option to send a *$comment* to the server. This
comment will show up in the profiling log (for slow queries f.e.). In
the PHP driver, you use the <span
class="function">MongoCursor::addOption</span> method.

``` php
<?php
$m = new MongoClient;
$c = $m->demo->demo;
$cursor = $c->find();
$cursor->addOption('$comment', "This comment will show up in the profiling log");

foreach ($cursor as $document) { /* empty */ }
?>
```

以上例程的输出类似于：

    {
        "op" : "query",
        "ns" : "demo.demo",
        "query" : {
            "$query" : {
                 
            },
            "$comment" : "This comment will show up in the profiling log"
        },
        "cursorid" : 168463566447,
        "ntoreturn" : 0,
        "ntoskip" : 0,
        "nscanned" : 101,
        "nscannedObjects" : 101,
        "keyUpdates" : 0,
        "numYield" : 0,
    …

**示例 \#2 <span class="function">MongoCursor::addOption</span>
example**

Using <span class="function">MongoCursor::skip</span> to skip over
millions of results can become slow. One way around this is to use
*$min* or *$max* options for the query. These can be handy, but they
require an index on exactly the fields being searched for. This is an
example of how to use *$min* as an alternative to <span
class="function">MongoCursor::skip</span>.

``` php
<?php

// make sure we have an index
$c->ensureIndex(array("ts" => 1));

// you may have to modify this to run in a reasonable amount of time on slow 
// machines (should take about 30 seconds on a good machine)
for ($i = 0; $i < 30000000; $i++) {
    $c->insert(array("ts" => new MongoDate(), "i" => $i));
}

$now = strtotime("now");

// find documents inserted in the last 2 seconds
$cursor = $c->find()->addOption('$min', array("ts" => $now-2));

?>
```

MongoCursor::awaitData
======================

Sets whether this cursor will wait for a while for a tailable cursor to
return more data

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::awaitData</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$wait`<span
class="initializer"> = **`TRUE`**</span></span> \] )

This method is to be used with tailable cursors. If we are at the end of
the data, block for a while rather than returning no data. After a
timeout period, we do return as normal.

### 参数

`wait`  
If the cursor should wait for more data to become available.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 范例

**示例 \#1 <span class="function">MongoCursor::awaitData</span>
example**

In this example we tail the "oplog" and instead of sleeping during every
iteration, we set the <span
class="function">MongoCursor::awaitData</span> option. <span
class="function">MongoCursor::hasNext</span> will now block until there
is more data available.

``` php
<?php
$m = new MongoClient( 'mongodb://localhost:13000', array( 'replSet' => 'seta' ) );
$c = $m->local->selectCollection( 'oplog.rs' );
$cursor = $c->find( array( 'ns' => 'demo.article', 'op' => 'i' ) );
$cursor->tailable( true );
$cursor->awaitData( true );

while (true) {
    if (!$cursor->hasNext()) {
        // we've read all the results, exit
        if ($cursor->dead()) {
            break;
        }
    } else {
        var_dump( $cursor->getNext() );
    }
}
?>
```

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/tutorial/create-tailable-cursor/" class="link external">» tailable cursors</a>.

-   <span class="function">MongoCursor::tailable</span>

MongoCursor::batchSize
======================

Limits the number of elements returned in one batch

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::batchSize</span> ( <span
class="methodparam"><span class="type">int</span> `$batchSize`</span> )

A cursor typically fetches a batch of result objects and store them
locally. This method sets the batchSize value to configure the amount of
documents retrieved from the server in one round trip. However, it will
never return more documents than fit in the max batch size limit
(usually 4MB).

### 参数

`batchSize`  
The number of results to return per batch. Each batch requires a
round-trip to the server.

If `batchSize` is *2 or more*, it represents the size of each batch of
objects retrieved. It can be adjusted to optimize performance and limit
data transfer.

If `batchSize` is *1* or negative, it will limit of number returned
documents to the absolute value of batchSize, and the cursor will be
closed. For example if batchSize is *-10*, then the server will return a
maximum of 10 documents and as many as can fit in 4MB, then close the
cursor.

**Warning**
A `batchSize` of *1* is special, and means the same as *-1*, i.e. a
value of *1* makes the cursor only capable of returning *one* document.

Note that this feature is different from <span
class="function">MongoCursor::limit</span> in that documents must fit
within a maximum size, and it removes the need to send a request to
close the cursor server-side. The batch size can be changed even after a
cursor is iterated, in which case the setting will apply on the next
batch retrieval.

This cannot override MongoDB's limit on the amount of data it will
return to the client (i.e., if you set batch size to 1,000,000,000,
MongoDB will still only return 4-16MB of results per batch).

To ensure consistent behavior, the rules of <span
class="function">MongoCursor::batchSize</span> and <span
class="function">MongoCursor::limit</span> behave a little complex but
work "as expected". The rules are: hard limits override soft limits with
preference given to <span class="function">MongoCursor::limit</span>
over <span class="function">MongoCursor::batchSize</span>. After that,
whichever is set and lower than the other will take precedence. See
below. section for some examples.

### 返回值

Returns this cursor.

### 范例

**示例 \#1 <span class="function">MongoCursor::batchSize</span> and
combinations with <span class="function">MongoCursor::limit</span>**

``` php
<?php

// one batch, at most 10 items. The -10 makes the server to return 10 items,
// and then remove the cursor.
$cursor->limit(20)->batchSize(-10);

// first batch: at most 10 items
$cursor->limit(10);

// first batch: at most 10 items
$cursor->limit(10)->batchSize(20);

// results are fetched in batches of 10 each, with a maximum of 20 items
// returned (that means two batches of 10).
$cursor->limit(20)->batchSize(10);

// results are fetched in batches of 7 each, with a maximum of 30 items
// returned (that means that the driver requests 4 batches of 7, and one batch
// of 2).
$cursor->limit(30)->batchSize(7)
?>
```

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/reference/method/cursor.batchSize/" class="link external">» batchSize</a>.

-   <span class="function">MongoCursor::limit</span>
-   <span class="methodname">MongoCursorInterface::batchSize</span>

### 更新日志

| 版本  | 说明                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.5 | Before 1.4.5, this method would throw an <span class="classname">MongoCursorException</span> if the cursor had already started iterating. |

MongoCursor::\_\_construct
==========================

Create a new cursor

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoCursor::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoClient</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$ns`</span> \[, <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`connection`  
Database connection.

`ns`  
Full name of database and collection.

`query`  
Database query.

`fields`  
Fields to return.

### 返回值

Returns the new cursor.

MongoCursor::count
==================

Counts the number of results for this query

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoCursor::count</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$foundOnly`<span
class="initializer"> = **`FALSE`**</span></span> \] )

This method does not affect the state of the cursor: if you haven't
queried yet, you can still apply limits, skips, etc. If you have started
iterating through results, it will not move the current position of the
cursor. If you have exhausted the cursor, it will not reset it.

### 参数

`foundOnly`  
Send cursor limit and skip information to the count function, if
applicable.

### 返回值

The number of documents returned by this cursor's query.

### 范例

**示例 \#1 <span class="function">MongoCursor::count</span> example**

``` php
<?php

$collection->insert(array('x'=>1));
$collection->insert(array('x'=>2));
$collection->insert(array('x'=>3));

$cursor = $collection->find();

var_dump($cursor->count());
var_dump($cursor->count(true));

$cursor->limit(2);

var_dump($cursor->count());
var_dump($cursor->count(true));

?>
```

以上例程的输出类似于：

    int(3)
    int(3)
    int(3)
    int(2)

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database.

MongoCursor::current
====================

Returns the current element

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCursor::current</span> ( <span
class="methodparam">void</span> )

This returns **`NULL`** until <span
class="function">MongoCursor::next</span> is called.

### 参数

此函数没有参数。

### 返回值

The current result document as an associative array. **`NULL`** will be
returned if there is no result.

### 参见

-   <span class="methodname">Iterator::current</span>

MongoCursor::dead
=================

Checks if there are results that have not yet been sent from the
database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCursor::dead</span> ( <span
class="methodparam">void</span> )

The database sends responses in batches of documents, up to 4MB of
documents per response. This method checks if the database has more
batches or if the result set has been exhausted.

A cursor being "dead" does not mean that <span
class="function">MongoCursor::hasNext</span> will return **`FALSE`**, it
only means that the database is done sending results to the client. The
client should continue iterating through results until <span
class="function">MongoCursor::hasNext</span> is **`FALSE`**.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if there are more results that have not yet been sent
to the client, and **`FALSE`** otherwise.

### 参见

-   <span class="methodname">MongoCursorInterface::dead</span>

MongoCursor::doQuery
====================

Execute the query

### 说明

<span class="modifier">protected</span> <span class="type">void</span>
<span class="methodname">MongoCursor::doQuery</span> ( <span
class="methodparam">void</span> )

**Warning**

Please do not use me.

This function actually queries the database. All queries and commands go
through this function. Thus, this function can be overridden to provide
custom query handling.

This handles serializing your query, sending it to the database,
receiving a response, and deserializing it. Thus, if you are planning to
override this, your code should probably call out to the original to use
the existing functionality (see the example below).

### 参数

此函数没有参数。

### 返回值

**`NULL`**.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 范例

**示例 \#1 <span class="function">MongoCursor::doQuery</span> example**

You could override this function to attempt a query on a secondary and,
if that fails, try it again on the primary.

``` php
<?php

class MyCursor extends MongoCursor {

    protected function doQuery() {

        $this->slaveOkay();

        try {
            MongoCursor::doQuery();
        }
        catch(MongoCursorException $e) {
            $this->slaveOkay(false);
            MongoCursor::doQuery();
        }
    }
}

?>
```

MongoCursor::explain
====================

Return an explanation of the query, often useful for optimization and
debugging

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCursor::explain</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an explanation of the query.

### 范例

**示例 \#1 <span class="function">MongoCursor::explain</span> example**

``` php
<?php

$cursor = $collection->find(array("x"=>1), array("y"));
$cursor->sort(array("z" => 1))->limit(4)->skip(5);

var_dump($cursor->explain());

?>
```

以上例程的输出类似于：

    array(8) {
      ["cursor"]=>
      string(15) "BtreeCursor x_1"
      ["startKey"]=>
      array(1) {
        ["x"]=>
        int(1)
      }
      ["endKey"]=>
      array(1) {
        ["x"]=>
        int(1)
      }
      ["nscanned"]=>
      float(4)
      ["n"]=>
      int(4)
      ["scanAndOrder"]=>
      int(1)
      ["millis"]=>
      int(3)
      ["allPlans"]=>
      array(2) {
        [0]=>
        array(3) {
          ["cursor"]=>
          string(15) "BtreeCursor x_1"
          ["startKey"]=>
          array(1) {
            ["x"]=>
            int(1)
          }
          ["endKey"]=>
          array(1) {
            ["x"]=>
            int(1)
          }
        }
        [1]=>
        array(3) {
          ["cursor"]=>
          string(11) "BasicCursor"
          ["startKey"]=>
          array(0) {
          }
          ["endKey"]=>
          array(0) {
          }
        }
      }
    }

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database.

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/reference/method/cursor.explain/" class="link external">» explain</a>.

MongoCursor::fields
===================

Sets the fields for a query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::fields</span> ( <span
class="methodparam"><span class="type">array</span> `$f`</span> )

Fields are specified by *"fieldname" : bool*. **`TRUE`** indicates that
a field should be returned, **`FALSE`** indicates that it should not be
returned. You can also use 1 and 0 instead of **`TRUE`** and
**`FALSE`**.

Thus, to return only the "summary" field, one could say:

``` php
<?php

$cursor->fields(array("summary" => true));

?>
```

To return all fields except the "hidden" field:

``` php
<?php

$cursor->fields(array("hidden" => false));

?>
```

### 参数

`f`  
Fields to return (or not return).

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating or a scalar argument is given.

MongoCursor::getNext
====================

Advances the cursor to the next result, and returns that result

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCursor::getNext</span> ( <span
class="methodparam">void</span> )

> **Note**:
>
> <span class="methodname">MongoCursor::getNext</span> is an alias of
> <span class="methodname">MongoCursor::next</span>.

MongoCursor::getReadPreference
==============================

Get the read preference for this query

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCursor::getReadPreference</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the read preference. The array
contains the values *type* for the string read preference mode
(corresponding to the <span class="classname">MongoClient</span>
constants), and *tagsets* containing a list of all tag set criteria. If
no tag sets were specified, *tagsets* will not be present in the array.

### 范例

**示例 \#1 <span
class="methodname">MongoCursor::getReadPreference</span> return value
example**

``` php
<?php

$m = new MongoClient();
$cursor = $m->test->users->find();
$cursor->setReadPreference(MongoClient::RP_SECONDARY, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
    array(),
));
var_dump($cursor->getReadPreference());
?>
```

以上例程会输出：

    array(2) {
      ["type"]=>
      string(9) "secondary"
      ["tagsets"]=>
      array(3) {
        [0]=>
        array(2) {
          ["dc"]=>
          string(4) "east"
          ["use"]=>
          string(9) "reporting"
        }
        [1]=>
        array(1) {
          ["dc"]=>
          string(7) "west"
        }
        [2]=>
        array(0) {
        }
      }
    }

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoCursor::setReadPreference</span>
-   <span
    class="function">MongoCursorInterface::getReadPreference</span>

MongoCursor::hasNext
====================

Checks if there are any more elements in this cursor

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCursor::hasNext</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns if there is another element.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database and <span
class="classname">MongoCursorTimeoutException</span> if the timeout is
exceeded.

MongoCursor::hint
=================

Gives the database a hint about the query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::hint</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

### 参数

`index`  
Index to use for the query. If a string is passed, it should correspond
to an index name. If an array or object is passed, it should correspond
to the specification used to create the index (i.e. the first argument
to <span class="function">MongoCollection::ensureIndex</span>).

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 更新日志

| 版本  | 说明                                                                                                                                 |
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.0 | The `index` argument now supports index names as string values. In versions before 1.4.0, only array or object values were accepted. |

MongoCursor::immortal
=====================

Sets whether this cursor will timeout

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::immortal</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$liveForever`<span
class="initializer"> = **`TRUE`**</span></span> \] )

After remaining idle on the server for some amount of time, cursors, by
default, "die." This is generally the behavior one wants. The database
cleans up a cursor once all of its results have been sent to the client,
but if the client doesn't request all of the results, the cursor will
languish there, taking up resources. Thus, after a few minutes, the
cursor "times out" and the database assumes the client has gotten
everything it needs and cleans up its the cursor's resources.

If, for some reason, you need a cursor to hang around for a long time,
you can prevent the database from cleaning it up by using this method.
However, if you make a cursor immortal, you need to iterate through all
of its results (or at least until <span
class="methodname">MongoCursor::dead</span> returns **`TRUE`**) or the
cursor will hang around the database *forever*, taking up resources.

### 参数

`liveForever`  
If the cursor should be immortal.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

MongoCursor::info
=================

Gets information about the cursor's creation and iteration

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCursor::info</span> ( <span
class="methodparam">void</span> )

This can be called before or after the cursor has started iterating.

### 参数

此函数没有参数。

### 返回值

Returns the namespace, batch size, limit, skip, flags, query, and
projected fields for this cursor. If the cursor has started iterating,
additional information about iteration and the connection will be
included.

### 更新日志

| 版本   | 说明                                                                                                                                                                                                                                                                                                                                   |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.1.0  | Added a number of other fields, including *id* (the cursor id), *at* (the driver's counter of which document is current), *numReturned* (the number returned by the server in the current batch), and *server* (which server the query was sent to—useful in conjunction with <a href="/book/mongo.html#读取首选项" class="xref"></a>. |
| 1.0.10 | Added *started\_iterating* field, a boolean indicating if cursor is pre- or post-query.                                                                                                                                                                                                                                                |

### 范例

**示例 \#1 <span class="function">MongoCursor::info</span> example**

``` php
<?php
$m = new MongoClient();

$cursor = $m->test->foo->find(array("x" => 4), array("y" => 0));

echo "Before iteration started:\n";
var_dump($cursor->info());

echo "\nAfter iteration started:\n";
$cursor->rewind();
var_dump($cursor->info());

?>
```

以上例程的输出类似于：

    Before iteration started:
    array(8) {
      ["ns"]=>
      string(8) "test.foo"
      ["limit"]=>
      int(0)
      ["batchSize"]=>
      int(0)
      ["skip"]=>
      int(0)
      ["flags"]=>
      int(0)
      ["query"]=>
      array(1) {
        ["x"]=>
        int(4)
      }
      ["fields"]=>
      array(1) {
        ["y"]=>
        int(0)
      }
      ["started_iterating"]=>
      bool(false)
    }

    After iteration started:
    array(15) {
      ["ns"]=>
      string(8) "test.foo"
      ["limit"]=>
      int(0)
      ["batchSize"]=>
      int(0)
      ["skip"]=>
      int(0)
      ["flags"]=>
      int(0)
      ["query"]=>
      array(1) {
        ["x"]=>
        int(4)
      }
      ["fields"]=>
      array(1) {
        ["y"]=>
        int(0)
      }
      ["started_iterating"]=>
      bool(true)
      ["id"]=>
      int(0)
      ["at"]=>
      int(0)
      ["numReturned"]=>
      int(1)
      ["server"]=>
      string(25) "localhost:27017;-;.;26450"
      ["host"]=>
      string(9) "localhost"
      ["port"]=>
      int(27017)
      ["connection_type_desc"]=>
      string(10) "STANDALONE"
    }

### 参见

-   <span class="methodname">MongoCursorInterface::info</span>

MongoCursor::key
================

Returns the current result's \_id, or its index within the result set

### 说明

<span class="modifier">public</span> <span
class="type">string\|int</span> <span
class="methodname">MongoCursor::key</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The current result's *\_id* as a string. If the result has no *\_id*,
its numeric index within the result set will be returned as an integer.

### 参见

-   <span class="methodname">Iterator::key</span>

MongoCursor::limit
==================

Limits the number of results returned

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::limit</span> ( <span
class="methodparam"><span class="type">int</span> `$num`</span> )

### 参数

`num`  
The number of results to return.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 参见

-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/reference/method/cursor.limit/" class="link external">» limit</a>.
-   <span class="function">MongoCursor::batchSize</span>
-   <span class="methodname">MongoCursor::skip</span>

MongoCursor::maxTimeMS
======================

Sets a server-side timeout for this query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::maxTimeMS</span> ( <span
class="methodparam"><span class="type">int</span> `$ms`</span> )

Specifies a cumulative time limit in milliseconds to be allowed by the
server for processing operations on the cursor.

### 参数

`ms`  
Specifies a cumulative time limit in milliseconds to be allowed by the
server for processing operations on the cursor.

### 返回值

This cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

Causes methods that fetch results to throw a <span
class="classname">MongoExecutionTimeoutException</span> if the query
takes longer than the specified number of milliseconds in processing
time.

### 范例

**示例 \#1 <span class="methodname">MongoCursor::maxTimeMS</span>
example**

In the following example, the server will abort the query if the cursor
requires more than two seconds in processing time to return its results.

``` php
<?php

$cursor = $collection->find();
$cursor->maxTimeMS(2000);

try {
    $results = iterator_to_array($cursor);
} catch (MongoExecutionTimeoutException $e) {
    echo "query took too long!";
}

?>
```

### 注释

**Warning**

Unlike <span class="methodname">MongoCursor::timeout</span>, which
specifies a client-side timeout, <span
class="methodname">MongoCursor::maxTimeMS</span> can be used to cause
the MongoDB server to abort long-running queries. This timeout is
cumulative for the lifetime of the cursor (i.e. each batch will
contribute to this time limit). The timeout only considers processing
time; idle time is not considered.

MongoCursor::next
=================

Advances the cursor to the next result, and returns that result

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCursor::next</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the next document.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database and <span
class="classname">MongoCursorTimeoutException</span> if the timeout is
exceeded.

### 参见

-   <span class="methodname">Iterator::next</span>

MongoCursor::partial
====================

If this query should fetch partial results from *mongos* if a shard is
down

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::partial</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$okay`<span
class="initializer"> = **`TRUE`**</span></span> \] )

This option allows *mongos* to send partial query results if a shard is
unreachable. This is only applicable when running a sharded MongoDB
cluster and connecting to a *mongos*.

If a shard goes down and a query needs to be sent to that shard,
*mongos* will return the results (if any) from shards it already
contacted, then an error message that it could not reach the shard (a
<span class="classname">MongoCursorException</span> in PHP). If you
would like to get whatever results *mongos* can provide and no
exception, you can use this method. Note that this means that you won't
have an indication that a shard is down in your query response.

This has no effect on the query if all shards are reachable. This flag
was implemented in MongoDB version 1.7.5, so will only work with that
version and higher.

### 参数

`okay`  
If receiving partial results is okay.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

MongoCursor::reset
==================

Clears the cursor

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MongoCursor::reset</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

**`NULL`**.

MongoCursor::rewind
===================

Returns the cursor to the beginning of the result set

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MongoCursor::rewind</span> ( <span
class="methodparam">void</span> )

This is identical to the function:

``` php
<?php

public function rewind() {
    $this->reset();
    $this->next();
}

?>
```

### 参数

此函数没有参数。

### 返回值

**`NULL`**.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database and <span
class="classname">MongoCursorTimeoutException</span> if the timeout is
exceeded.

### 参见

-   <span class="methodname">Iterator::rewind</span>

MongoCursor::setFlag
====================

Sets arbitrary flags in case there is no method available the specific
flag

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::setFlag</span> ( <span
class="methodparam"><span class="type">int</span> `$flag`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$set`<span
class="initializer"> = **`TRUE`**</span></span> \] )

The <span class="classname">MongoCursor</span> class has several methods
for setting flags on the query object. This method is available in case
the MongoDB wire protocol has acquired a new flag, and the driver has
not been updated with a method for this new flag. In all other cases,
the method should be used. See the "See also" section for available
methods.

### 参数

`flag`  
Which flag to set. You can not set flag 6 (EXHAUST) as the driver does
not know how to handle them. You will get a warning if you try to use
this flag. For available flags, please refer to the wire protocol
<a href="https://docs.mongodb.com/meta-driver/latest/legacy/mongodb-wire-protocol/#MongoWireProtocol-OPQUERY" class="link external">» documentation</a>.

`set`  
Whether the flag should be set (**`TRUE`**) or unset (**`FALSE`**).

### 返回值

Returns this cursor.

### 错误／异常

Shows a warning when an unsupport flag is attempted to be set.

### 更新日志

| 版本  | 说明                                                                                                                          |
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| 1.4.0 | Support for flag 3 (OPLOG\_REPLAY) is added. Versions before 1.4.0 would throw a warning saying that the flag is unsupported. |

### 范例

**示例 \#1 <span class="function">MongoCursor::setFlag</span> example**

``` php
<?php
$m = new MongoClient( 'mongodb://localhost:13000', array( 'replSet' => 'seta' ) );
$c = $m->local->selectCollection( 'oplog.rs' );
$cursor = $c->find( array( 'ns' => 'demo.article', 'op' => 'i' ) );
$cursor->setFlag( 1, true ); // sets the tailable flag
$cursor->setFlag( 5, true ); // sets the await data flag
?>
```

### 参见

-   <span class="function">MongoCursor::tailable</span>
-   <span class="function">MongoCursor::immortal</span>
-   <span class="function">MongoCursor::awaitData</span>
-   <span class="function">MongoCursor::partial</span>
-   MongoDB core docs
    on<a href="https://docs.mongodb.com/meta-driver/latest/legacy/mongodb-wire-protocol/#MongoWireProtocol-OPQUERY" class="link external">» wire protocol query flags</a>

MongoCursor::setReadPreference
==============================

Set the read preference for this query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

### 参数

`read_preference`  
The read preference mode: **`MongoClient::RP_PRIMARY`**,
**`MongoClient::RP_PRIMARY_PREFERRED`**,
**`MongoClient::RP_SECONDARY`**,
**`MongoClient::RP_SECONDARY_PREFERRED`**, or
**`MongoClient::RP_NEAREST`**.

`tags`  
An array of zero or more tag sets, where each tag set is itself an array
of criteria used to match tags on replica set members.

### 返回值

Returns this cursor.

### 错误／异常

Emits **`E_WARNING`** if either parameter is invalid, or if one or more
tag sets are provided with the **`MongoClient::RP_PRIMARY`** read
preference mode.

### 范例

**示例 \#1 <span
class="methodname">MongoCursor::setReadPreference</span> tag set array
syntax example**

``` php
<?php

$m = new MongoClient();
$cursor = $m->test->users->find();

// Prefer the nearest server in the "east" data center also used for reporting,
// but fall back to a server in the "west" data center
$cursor->setReadPreference(MongoClient::RP_NEAREST, array(
    array('dc' => 'east', 'use' => 'reporting'),
    array('dc' => 'west'),
));
?>
```

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoCursor::getReadPreference</span>
-   <span
    class="function">MongoCursorInterface::setReadPreference</span>

MongoCursor::skip
=================

Skips a number of results

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::skip</span> ( <span
class="methodparam"><span class="type">int</span> `$num`</span> )

### 参数

`num`  
The number of results to skip.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 参见

-   <span class="methodname">MongoCursor::limit</span>

MongoCursor::slaveOkay
======================

Sets whether this query can be done on a secondary \[deprecated\]

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::slaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$okay`<span
class="initializer"> = **`TRUE`**</span></span> \] )

**Warning**

This method is deprecated since version 1.5.0. Instead, please use <span
class="methodname">MongoCursor::setReadPreference</span> and
<a href="/book/mongo.html#读取首选项" class="xref"></a>.

Calling this will make the driver route reads to secondaries if:

-   <span class="simpara"> You are using a replica set, and </span>
-   <span class="simpara"> You created a <span
    class="classname">MongoClient</span> instance using the option
    *"replicaSet" =\> "setName"*, and </span>
-   <span class="simpara"> There is a healthy secondary that can be
    reached by the driver. </span>

You can check which server was used for this query by calling <span
class="function">MongoCursor::info</span> after running the query. It's
*server* field will show which server the query was sent to.

Note that you should use this function even if you do not use the
automatic routing to secondaries. If you connect directly to a secondary
in a replica set, you still need to call this function, which basically
tells the database that you are aware that you might be getting older
data and you're okay with that. If you do not call this, you'll get "not
master" errors when you try to query.

This method will override the static class variable
`MongoCursor::$slaveOkay`. It will also override <span
class="function">Mongo::setSlaveOkay</span>, <span
class="function">MongoDB::setSlaveOkay</span> and <span
class="function">MongoCollection::setSlaveOkay</span>.

### 参数

`okay`  
If it is okay to query the secondary.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 范例

**示例 \#1 <span class="function">MongoCursor::slaveOkay</span>
example**

``` php
<?php

MongoCursor::$slaveOkay = false;

// cannot query secondary
$cursor = $collection->find();

// can query secondary
$cursor = $collection->find()->slaveOkay();

MongoCursor::$slaveOkay = true;

// can query secondary
$cursor = $collection->find();

// cannot query secondary
$cursor = $collection->find()->slaveOkay(false);

?>
```

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoCursor::setReadPreference</span>
-   <span class="methodname">MongoCursor::getReadPreference</span>

### 更新日志

| 版本  | 说明                                                                                                                                                                     |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.5.0 | This method has been deprecated in favour of <span class="methodname">MongoCursor::setReadPreference</span> and <a href="/book/mongo.html#读取首选项" class="xref"></a>. |

MongoCursor::snapshot
=====================

Use snapshot mode for the query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::snapshot</span> ( <span
class="methodparam">void</span> )

Use snapshot mode for the query. Snapshot mode ensures that a document
will not be returned more than once because an intervening write
operation results in a move of the document. Documents inserted or
deleted during the lifetime of the cursor may or may not be returned,
irrespective of snapshot mode.

Queries with short responses (less than 1MB) are always effectively
snapshotted.

Snapshot mode may not be used with sorting, explicit hints, or queries
on sharded collections.

### 参数

此函数没有参数。

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/reference/operator/meta/snapshot/" class="link external">» $snapshot operator</a>.

MongoCursor::sort
=================

Sorts the results by given fields

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::sort</span> ( <span
class="methodparam"><span class="type">array</span> `$fields`</span> )

### 参数

`fields`  
An array of fields by which to sort. Each element in the array has as
key the field name, and as value either *1* for ascending sort, or *-1*
for descending sort.

Each result is first sorted on the first field in the array, then (if it
exists) on the second field in the array, etc. This means that the order
of the fields in the `fields` array is important. See also the examples
section.

### 返回值

Returns the same cursor that this method was called on.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 范例

**示例 \#1 <span class="function">MongoCursor::sort</span> example**

``` php
<?php
// Sort on field x, ascending
$cursor->sort(array('x' => 1));

// The order in the associative array is important. For instance, these two
// examples will yield different results:

// Sort on date ascending and age descending
$cursor->sort(array('date' => 1, 'age' => -1));

// Sort on age descending and date ascending
$cursor->sort(array('age' => -1, 'date' => 1));
?>
```

MongoCursor::tailable
=====================

Sets whether this cursor will be left open after fetching the last
results

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::tailable</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$tail`<span
class="initializer"> = **`TRUE`**</span></span> \] )

Mongo has a feature known as tailable cursors which are similar to the
Unix "tail -f" command.

Tailable means cursor is not closed when the last data is retrieved.
Rather, the cursor marks the final object's position. you can resume
using the cursor later, from where it was located, if more data were
received.

Like any "latent cursor", the cursor may become invalid at some point --
for example if that final object it references were deleted. Thus, you
should be prepared to requery if the cursor is <span
class="function">MongoCursor::dead</span>.

### 参数

`tail`  
If the cursor should be tailable.

### 返回值

Returns this cursor.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if this
cursor has started iterating.

### 范例

**示例 \#1 <span class="function">MongoCursor::tailable</span> example**

``` php
<?php

$cursor = $collection->find()->tailable();

$results = array();

while (1) {
    if (!$cursor->hasNext()) {
        // we've read all the results, exit
        if ($cursor->dead()) {
            break;
        }
        // read all results so far, wait for more
        sleep(10);
    }
    else {
        $results[] = $cursor->getNext();
    }
}

?>
```

### 参见

MongoDB core docs on
<a href="https://docs.mongodb.com/manual/tutorial/create-tailable-cursor/" class="link external">» tailable cursors</a>.

-   <span class="function">MongoCursor::awaitData</span>

MongoCursor::timeout
====================

Sets a client-side timeout for this query

### 说明

<span class="modifier">public</span> <span
class="type">MongoCursor</span> <span
class="methodname">MongoCursor::timeout</span> ( <span
class="methodparam"><span class="type">int</span> `$ms`</span> )

A timeout can be set at any time and will affect subsequent queries on
the cursor, including fetching more results from the database.

### 参数

`ms`  
The number of milliseconds for the cursor to wait for a response. Use
*-1* to wait forever. By default, the cursor will wait `30000`
milliseconds (30 seconds).

### 返回值

This cursor.

### 错误／异常

Causes methods that fetch results to throw a <span
class="classname">MongoCursorTimeoutException</span> if the query takes
longer than the specified number of milliseconds.

### 范例

**示例 \#1 <span class="function">MongoCursor::timeout</span> example**

In the following example, the driver will wait forever for the initial
database response, and then wait 100ms for subsequent responses.

``` php
<?php

$cursor = $collection->find();
$cursor->timeout(-1);

/* $cursor->hasNext() executes the query. An infinite timeout has been set, so
 * the driver will wait as long as necessary for a response.
 */
while ($cursor->hasNext()) {
    $cursor->timeout(100);

    /* A timeout has now been set, so if the cursor needs to get more results
     * from the database, it will only wait 100ms for a response.
     */
    try {
        print_r($cursor->getNext());
    } catch (MongoCursorTimeoutException $e) {
        echo "query took too long!";
    }
}

?>
```

### 注释

**Warning**

This does not cause the MongoDB server to cancel long-running
operations; it only instructs the driver to stop waiting for a response
and throw a <span class="classname">MongoCursorTimeoutException</span>
after a set time. If you need to specify a server-side timeout for a
query, consider using <span
class="methodname">MongoCursor::maxTimeMS</span>.

### 参见

-   <span class="methodname">MongoCursorInterface::timeout</span>
-   The *socketTimeoutMS* option for <span
    class="function">MongoClient::\_\_construct</span>

MongoCursor::valid
==================

Checks if the cursor is reading a valid result

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCursor::valid</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current result is not null, and **`FALSE`** otherwise.

### 参见

-   <span class="methodname">Iterator::valid</span>

简介
----

Interface for cursors, which can be used to iterate through results of a
database query or command. This interface is implemented by the <span
class="classname">MongoCursor</span> and <span
class="classname">MongoCommandCursor</span> classes.

> **Note**: <span class="simpara"> Similar to <span
> class="classname">Traversable</span>, this interface cannot be
> implemented in PHP scripts. </span>

类摘要
------

**MongoCursorInterface**

<span class="ooclass"> class **MongoCursorInterface** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Iterator**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">MongoCursorInterface</span> <span
class="methodname">batchSize</span> ( <span class="methodparam"><span
class="type">int</span> `$batchSize`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">dead</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">info</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">MongoCursorInterface</span> <span
class="methodname">setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">MongoCursorInterface</span> <span
class="methodname">timeout</span> ( <span class="methodparam"><span
class="type">int</span> `$ms`</span> )

/\* 继承的方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Iterator::current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">scalar</span> <span
class="methodname">Iterator::key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Iterator::next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Iterator::rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Iterator::valid</span> ( <span
class="methodparam">void</span> )

}

MongoCursorInterface::batchSize
===============================

Limits the number of elements returned in one batch

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">MongoCursorInterface</span> <span
class="methodname">MongoCursorInterface::batchSize</span> ( <span
class="methodparam"><span class="type">int</span> `$batchSize`</span> )

A cursor typically fetches a batch of result objects and stores them
locally. This method sets the batch size value to configure the amount
of documents retrieved from the server in one round trip.

### 参数

`batchSize`  
The number of results to return per batch.

### 返回值

Returns this cursor.

MongoCursorInterface::dead
==========================

Checks if there are results that have not yet been sent from the
database

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">MongoCursorInterface::dead</span> ( <span
class="methodparam">void</span> )

This method checks whether the cursor has been exhausted and the
database has no more results to send to the client. A cursor being
"dead" does not necessarily mean that there are no more results
available for iteration.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if there are more results that have not yet been sent
to the client, and **`FALSE`** otherwise.

MongoCursorInterface::getReadPreference
=======================================

Get the read preference for this query

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">MongoCursorInterface::getReadPreference</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the read preference. The array
contains the values *type* for the string read preference mode
(corresponding to the <span class="classname">MongoClient</span>
constants), and *tagsets* containing a list of all tag set criteria. If
no tag sets were specified, *tagsets* will not be present in the array.

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span
    class="function">MongoCursorInterface::setReadPreference</span>

MongoCursorInterface::info
==========================

Gets information about the cursor's creation and iteration

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">MongoCursorInterface::info</span> ( <span
class="methodparam">void</span> )

Returns information about the cursor's creation and iteration. This can
be called before or after the cursor has started iterating.

### 参数

此函数没有参数。

### 返回值

Returns the namespace, batch size, limit, skip, flags, query, and
projected fields for this cursor. If the cursor has started iterating,
additional information about iteration and the connection will be
included.

MongoCursorInterface::setReadPreference
=======================================

Set the read preference for this query

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">MongoCursorInterface</span> <span
class="methodname">MongoCursorInterface::setReadPreference</span> (
<span class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

### 参数

`read_preference`  
The read preference mode: **`MongoClient::RP_PRIMARY`**,
**`MongoClient::RP_PRIMARY_PREFERRED`**,
**`MongoClient::RP_SECONDARY`**,
**`MongoClient::RP_SECONDARY_PREFERRED`**, or
**`MongoClient::RP_NEAREST`**.

`tags`  
An array of zero or more tag sets, where each tag set is itself an array
of criteria used to match tags on replica set members.

### 返回值

Returns this cursor.

### 错误／异常

Emits **`E_WARNING`** if either parameter is invalid, or if one or more
tag sets are provided with the **`MongoClient::RP_PRIMARY`** read
preference mode.

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span
    class="function">MongoCursorInterface::getReadPreference</span>

MongoCursorInterface::timeout
=============================

Sets a client-side timeout for this query

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="type">MongoCursorInterface</span> <span
class="methodname">MongoCursorInterface::timeout</span> ( <span
class="methodparam"><span class="type">int</span> `$ms`</span> )

A timeout can be set at any time and will affect subsequent data
retrieval associated with this cursor, including fetching more results
from the database.

### 参数

`ms`  
The number of milliseconds for the cursor to wait for a response. Use
*-1* to wait forever. By default, the cursor will wait `30000`
milliseconds (30 seconds).

### 返回值

Returns this cursor.

### 错误／异常

Causes methods that fetch results to throw a <span
class="classname">MongoCursorTimeoutException</span> if the data fetch
takes longer than the specified number of milliseconds.

### 参见

-   The *socketTimeoutMS* option for <span
    class="function">MongoClient::\_\_construct</span>

简介
----

A command cursor is similar to a <span
class="classname">MongoCursor</span> except that you use it for
iterating through the results of a database command instead of a normal
query. Command cursors are useful for iterating over large result sets
that might exceed the document size limit (currently 16MB) of a single
<span class="function">MongoDB::command</span> response.

While you can create command cursors using <span
class="function">MongoCommandCursor::\_\_construct</span> or the <span
class="function">MongoCommandCursor::createFromDocument</span> factory
method, you will generally want to use command-specific helpers such as
<span class="function">MongoCollection::aggregateCursor</span>.

Note that the cursor does not "contain" the database command's results;
it just manages iteration through them. Thus, if you print a cursor
(f.e. with <span class="function">var\_dump</span> or <span
class="function">print\_r</span>), you will see the cursor object but
not the result documents.

Cursor Stages
-------------

A <span class="classname">MongoCommandCursor</span> has two "life
stages": pre- and post- command. When a cursor is created, it has not
yet contacted the database, so it is in its pre-command state. When the
client first attempts to get a result (by calling <span
class="function">MongoCommandCursor::rewind</span>, directly or
indirectly), the cursor moves into the post-command state.

The command cursor's batch size and socket timeout may be configured in
both the pre- and post- command states.

**示例 \#1 Adding options to <span
class="classname">MongoCommandCursor</span>**

``` php
<?php

$cursor = new MongoCommandCursor(...);

$cursor = $cursor->batchSize( 4 );

foreach ($cursor as $result) {
    var_dump($result);
}
?>
```

类摘要
------

**MongoCommandCursor**

<span class="ooclass"> class **MongoCommandCursor** </span> <span
class="oointerface">implements <span
class="interfacename">MongoCursorInterface</span> </span> <span
class="oointerface">, <span class="interfacename">Iterator</span>
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">batchSize</span> ( <span class="methodparam"><span
class="type">int</span> `$batchSize`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoClient</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$ns`</span> , <span
class="methodparam"><span class="type">array</span> `$command`<span
class="initializer"> = array()</span></span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">createFromDocument</span> ( <span
class="methodparam"><span class="type">MongoClient</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$hash`</span> , <span
class="methodparam"><span class="type">array</span> `$document`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">dead</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">info</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">key</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">timeout</span> ( <span class="methodparam"><span
class="type">int</span> `$ms`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

参见
----

-   <span class="methodname">MongoDB::command</span>
-   <span class="methodname">MongoCollection::aggregateCursor</span>

MongoCommandCursor::batchSize
=============================

Limits the number of elements returned in one batch

### 说明

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">MongoCommandCursor::batchSize</span> ( <span
class="methodparam"><span class="type">int</span> `$batchSize`</span> )

A cursor typically fetches a batch of result objects and store them
locally. This method sets the batchSize value to configure the amount of
documents retrieved from the server in one round trip.

### 参数

`batchSize`  
The number of results to return per batch. Each batch requires a
round-trip to the server.

This cannot override MongoDB's limit on the amount of data it will
return to the client (i.e., if you set batch size to 1,000,000,000,
MongoDB will still only return 4-16MB of results per batch).

### 返回值

Returns this cursor.

### 范例

**示例 \#1 <span class="function">MongoCommandCursor::batchSize</span>**

``` php
<?php
$commandCursor->batchSize(20);
?>
```

### 参见

-   <span class="methodname">MongoCursorInterface::batchSize</span>

MongoCommandCursor::\_\_construct
=================================

Create a new command cursor

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoCommandCursor::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoClient</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$ns`</span> , <span
class="methodparam"><span class="type">array</span> `$command`<span
class="initializer"> = array()</span></span> )

Generally, you should not have to construct a <span
class="classname">MongoCommandCursor</span> manually, as there are
helper functions such as <span
class="methodname">MongoCollection::aggregateCursor</span> and <span
class="methodname">MongoCollection::parallelCollectionScan</span>;
however, if the server introduces new commands that can return cursors,
this constructor will be useful in the absence of specific helper
methods. You may also consider using <span
class="methodname">MongoCommandCursor::createFromDocument</span>.

### 参数

`connection`  
Database connection.

`ns`  
Full name of the database and collection (e.g. *"test.foo"*)

`command`  
Database command.

### 返回值

Returns the new cursor.

### 范例

**示例 \#1 <span class="classname">MongoCommandCursor</span> example**

``` php
<?php
$m = new MongoClient;

// Define the aggregation pipeline
$pipeline = [
    [ '$group' => [
        '_id' => '$country_code',
        'timezones' => [ '$addToSet' => '$timezone' ]
    ] ],
    [ '$sort' => [ '_id' => 1 ] ],
];

// Construct a MongoCommandCursor object
$cursor = new MongoCommandCursor(
    $m, // MongoClient object
    'demo.cities', // namespace
    [
        'aggregate' => 'cities',
        'pipeline' => $pipeline,
        'cursor' => [ 'batchSize' => 0 ],
    ]
);

foreach($cursor as $result) {
   …
}
?>
```

### 参见

-   <span class="function">MongoCommandCursor::createFromDocument</span>
-   <span class="function">MongoCollection::aggregateCursor</span>
-   <span
    class="function">MongoCollection::parallelCollectionScan</span>

MongoCommandCursor::createFromDocument
======================================

Create a new command cursor from an existing command response document

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">MongoCommandCursor::createFromDocument</span> ( <span
class="methodparam"><span class="type">MongoClient</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$hash`</span> , <span
class="methodparam"><span class="type">array</span> `$document`</span> )

Use this method if you have a raw command result with cursor information
in it. Note that cursors created with this method cannot be iterated
multiple times, as they will lack the original command necessary for
re-execution.

### 参数

`connection`  
Database connection.

`hash`  
The connection hash, as obtained through the third by-reference argument
to <span class="methodname">MongoDB::command</span>.

`document`  
Document with cursor information in it. This document needs to contain
the *id*, *ns* and *firstBatch* fields. Such a document is obtained by
calling the <span class="methodname">MongoDB::command</span> with
appropriate arguments to return a cursor, and not just an inline result.
See the example below.

### 返回值

Returns the new cursor.

### 范例

**示例 \#1 <span
class="function">MongoCommandCursor::createFromDocument</span>**

``` php
<?php
$m = new MongoClient;
$d = $m->demo;

// Define the aggregation pipeline
$pipeline = [
    [ '$group' => [
        '_id' => '$country_code',
        'timezones' => [ '$addToSet' => '$timezone' ]
    ] ],
    [ '$sort' => [ '_id' => 1 ] ],
];

// Execute the command. The "cursor" option instructs the server to return
// cursor information in the response instead of inline results.
$r = $d->command(
    [
        'aggregate' => 'cities',
        'pipeline' => $pipeline,
        'cursor' => [ 'batchSize' => 1 ],
    ],
    null,
    $hash
);

// Show result and hash
var_dump( $r, $hash );

// Construct the command cursor
$cursor = MongoCommandCursor::createFromDocument( $m, $hash, $r );
?>
```

以上例程的输出类似于：

    array(2) {
      ["cursor"]=>
      array(3) {
        ["id"]=>
        object(MongoInt64)#5 (1) {
          ["value"]=>
          string(12) "392143983421"
        }
        ["ns"]=>
        string(11) "demo.cities"
        ["firstBatch"]=>
        array(1) {
          [0]=>
          array(2) {
            ["_id"]=>
            string(2) "AD"
            ["timezones"]=>
            array(1) {
              [0]=>
              string(14) "Europe/Andorra"
            }
          }
        }
      }
      ["ok"]=>
      float(1)
    }
    string(25) "localhost:27017;-;.;17617"

As you can see, the returned cursor information has the *id*, *ns* and
*firstBatch* fields.

### 参见

-   <span class="function">MongoCommandCursor::\_\_construct</span>

MongoCommandCursor::current
===========================

Returns the current element

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCommandCursor::current</span> ( <span
class="methodparam">void</span> )

This returns **`NULL`** until <span
class="function">MongoCommandCursor::rewind</span> is called.

### 参数

此函数没有参数。

### 返回值

The current result document as an associative array. **`NULL`** will be
returned if there is no result.

### 参见

-   <span class="methodname">Iterator::current</span>

MongoCommandCursor::dead
========================

Checks if there are results that have not yet been sent from the
database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCommandCursor::dead</span> ( <span
class="methodparam">void</span> )

This method checks whether the <span
class="classname">MongoCommandCursor</span> cursor has been exhausted
and the database has no more results to send to the client. A cursor
being "dead" does not necessarily mean that there are no more results
available for iteration.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if there are more results that have not yet been sent
to the client, and **`FALSE`** otherwise.

### 参见

-   <span class="methodname">MongoCursorInterface::dead</span>

MongoCommandCursor::getReadPreference
=====================================

Get the read preference for this command

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCommandCursor::getReadPreference</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

This function returns an array describing the read preference. The array
contains the values *type* for the string read preference mode
(corresponding to the <span class="classname">MongoClient</span>
constants), and *tagsets* containing a list of all tag set criteria. If
no tag sets were specified, *tagsets* will not be present in the array.

### 范例

**示例 \#1 <span
class="methodname">MongoCommandCursor::getReadPreference</span> return
value example**

``` php
<?php

$m = new MongoClient('mongodb://rs1.example.com:27017', array('replicaSet' => 'myReplSetName'));
$collection = $m->selectCollection('test', 'people');

// If a MongoCommandCursor is constructed directly, it will inherit the read
// preference of the MongoClient instance passed to its constructor; however,
// MongoCollection::aggregateCursor() will have the MongoCommandCursor inherit
// the collection's read preference.
$collection->setReadPreference(MongoClient::RP_SECONDARY);

$cursor = $collection->aggregateCursor( [
    [ '$group' => [ '_id' => '$name', 'points' => [ '$sum' => '$points' ] ] ],
    [ '$sort' => [ 'points' => -1 ] ],
] );

var_dump($cursor->getReadPreference());

?>
```

以上例程会输出：

    array(1) {
      ["type"]=>
      string(9) "secondary"
    }

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoCommandCursor::setReadPreference</span>
-   <span
    class="function">MongoCursorInterface::getReadPreference</span>

MongoCommandCursor::info
========================

Gets information about the cursor's creation and iteration

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCommandCursor::info</span> ( <span
class="methodparam">void</span> )

This can be called before or after the cursor has started iterating.

### 参数

此函数没有参数。

### 返回值

Returns the namespace, batch size, limit, skip, flags, query, and
projected fields for this cursor. If the cursor has started iterating,
additional information about iteration and the connection will be
included.

### 范例

**示例 \#1 <span class="function">MongoCommandCursor::info</span>
example**

``` php
<?php
$m = new MongoClient();

$cursor = new MongoCommandCursor(
    $m, // MongoClient object
    'demo.cities', // namespace
    [
        'aggregate' => 'cities',
        'pipeline' => [ [ '$match' => [ '_id' => [ '$exists' => true ] ] ] ],
        'cursor' => [ 'batchSize' => 1 ],
    ]
);

echo "Before iteration started:\n";
var_dump($cursor->info());

echo "\nAfter iteration started:\n";
$cursor->rewind();
var_dump($cursor->info());

?>
```

以上例程的输出类似于：

    Before iteration started:
    array(8) {
      ["ns"]=>
      string(11) "demo.cities"
      ["limit"]=>
      int(0)
      ["batchSize"]=>
      int(0)
      ["skip"]=>
      int(0)
      ["flags"]=>
      int(0)
      ["query"]=>
      array(3) {
        ["aggregate"]=>
        string(6) "cities"
        ["pipeline"]=>
        array(1) {
          [0]=>
          array(1) {
            ["$match"]=>
            array(1) {
              ["_id"]=>
              array(1) {
                ["$exists"]=>
                bool(true)
              }
            }
          }
        }
        ["cursor"]=>
        array(1) {
          ["batchSize"]=>
          int(1)
        }
      }
      ["fields"]=>
      NULL
      ["started_iterating"]=>
      bool(false)
    }

    After iteration started:
    array(17) {
      ["ns"]=>
      string(11) "demo.cities"
      ["limit"]=>
      int(0)
      ["batchSize"]=>
      int(0)
      ["skip"]=>
      int(0)
      ["flags"]=>
      int(0)
      ["query"]=>
      array(3) {
        ["aggregate"]=>
        string(6) "cities"
        ["pipeline"]=>
        array(1) {
          [0]=>
          array(1) {
            ["$match"]=>
            array(1) {
              ["_id"]=>
              array(1) {
                ["$exists"]=>
                bool(true)
              }
            }
          }
        }
        ["cursor"]=>
        array(1) {
          ["batchSize"]=>
          int(1)
        }
      }
      ["fields"]=>
      NULL
      ["started_iterating"]=>
      bool(true)
      ["id"]=>
      int(185840310129)
      ["at"]=>
      int(0)
      ["numReturned"]=>
      int(0)
      ["server"]=>
      string(25) "localhost:27017;-;.;23991"
      ["host"]=>
      string(9) "localhost"
      ["port"]=>
      int(27017)
      ["connection_type_desc"]=>
      string(10) "STANDALONE"
      ["firstBatchAt"]=>
      int(0)
      ["firstBatchNumReturned"]=>
      int(1)
    }

### 参见

-   <span class="methodname">MongoCursorInterface::info</span>

MongoCommandCursor::key
=======================

Returns the current result's index within the result set

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoCommandCursor::key</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The current result's index within the result set.

### 参见

-   <span class="methodname">Iterator::key</span>

MongoCommandCursor::next
========================

Advances the cursor to the next result

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MongoCommandCursor::next</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

**`NULL`**.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database and <span
class="classname">MongoCursorTimeoutException</span> if the timeout is
exceeded.

### 参见

-   <span class="methodname">Iterator::next</span>

MongoCommandCursor::rewind
==========================

Executes the command and resets the cursor to the start of the result
set

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoCommandCursor::rewind</span> ( <span
class="methodparam">void</span> )

If the cursor has already started iteration, the command will be
re-executed.

### 参数

此函数没有参数。

### 返回值

The raw server result document.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
cannot reach the database and <span
class="classname">MongoCursorTimeoutException</span> if the timeout is
exceeded.

Throws <span class="classname">MongoCursorException</span> if the cursor
was created with <span
class="function">MongoCommandCursor::createFromDocument</span> and has
already started iteration. Such cursors cannot be iterated multiple
times, as they lack the original command necessary for re-execution.

### 范例

**示例 \#1 <span class="function">MongoCommandCursor::rewind</span>**

``` php
<?php
$rawResult = $commandCursor->rewind();

// Command cursor is now reset to the start of the result set

var_dump($rawResult);
?>
```

以上例程的输出类似于：

    array(2) {
      ["cursor"]=>
      array(3) {
        ["id"]=>
        object(MongoInt64)#5 (1) {
          ["value"]=>
          string(12) "310050110216"
        }
        ["ns"]=>
        string(9) "demo.test"
        ["firstBatch"]=>
        array(1) {
          [0]=>
          array(2) {
            ["_id"]=>
            object(MongoId)#6 (1) {
              ["$id"]=>
              string(24) "52f5691544670a8077b0dc51"
            }
            ["value"]=>
            string(2) "42"
          }
        }
      }
      ["ok"]=>
      float(1)
    }

### 参见

-   <span class="methodname">Iterator::rewind</span>

MongoCommandCursor::setReadPreference
=====================================

Set the read preference for this command

### 说明

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">MongoCommandCursor::setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

### 参数

`read_preference`  
The read preference mode: **`MongoClient::RP_PRIMARY`**,
**`MongoClient::RP_PRIMARY_PREFERRED`**,
**`MongoClient::RP_SECONDARY`**,
**`MongoClient::RP_SECONDARY_PREFERRED`**, or
**`MongoClient::RP_NEAREST`**.

`tags`  
An array of zero or more tag sets, where each tag set is itself an array
of criteria used to match tags on replica set members.

### 返回值

Returns this cursor.

### 错误／异常

Emits **`E_WARNING`** if either parameter is invalid, or if one or more
tag sets are provided with the **`MongoClient::RP_PRIMARY`** read
preference mode.

### 范例

**示例 \#1 <span
class="methodname">MongoCommandCursor::setReadPreference</span> tag set
array syntax example**

``` php
<?php

$m = new MongoClient('mongodb://rs1.example.com:27017', array('replicaSet' => 'myReplSetName'));
$collection = $m->selectCollection('test', 'people');

$cursor = $collection->aggregateCursor( [
    [ '$group' => [ '_id' => '$name', 'points' => [ '$sum' => '$points' ] ] ],
    [ '$sort' => [ 'points' => -1 ] ],
] );

// Prefer the nearest server in the "east" data center also used for reporting,
// but fall back to a server in the "west" data center
$cursor->setReadPreference(MongoClient::RP_NEAREST, [
    [ 'dc' => 'east', 'use' => 'reporting' ],
    [ 'dc' => 'west' ],
] );

foreach ($cursor as $person) {
    // ...
}

// If the read preference is changed, it will be used the next time the cursor
// is rewound and the command is re-executed.
$cursor->setReadPreference(MongoClient::RP_PRIMARY);

foreach ($cursor as $person) {
    // ...
}

?>
```

### 参见

-   The
    <a href="/book/mongo.html#读取首选项" class="link">read preferences</a>
    documentation.
-   <span class="function">MongoCommandCursor::getReadPreference</span>
-   <span
    class="function">MongoCursorInterface::setReadPreference</span>

MongoCommandCursor::timeout
===========================

Sets a client-side timeout for this command

### 说明

<span class="modifier">public</span> <span
class="type">MongoCommandCursor</span> <span
class="methodname">MongoCommandCursor::timeout</span> ( <span
class="methodparam"><span class="type">int</span> `$ms`</span> )

A timeout can be set at any time and will affect subsequent data
retrieval associated with this cursor, including fetching more results
from the database.

### 参数

`ms`  
The number of milliseconds for the cursor to wait for a response. Use
*-1* to wait forever. By default, the cursor will wait `30000`
milliseconds (30 seconds).

### 返回值

This cursor.

### 错误／异常

Causes methods that fetch results to throw a <span
class="classname">MongoCursorTimeoutException</span> if the data fetch
takes longer than the specified number of milliseconds.

### 范例

**示例 \#1 <span class="function">MongoCommandCursor::timeout</span>
example**

In the following example, the driver will wait for 60 seconds for the
first response from the aggregate command. It will also wait for 60
seconds each time the server needs to be polled for more information.

``` php
<?php

$m = new MongoClient;
$col = $m->database->collection;

$pipeline = [ … ];

$cursor = $col->aggregateCursor( $pipeline );
$cursor->timeout( 60000 ); // for 60 seconds

foreach ( $cursor as $result ) {
   …
}

?>
```

### 注释

**Warning**

This does not cause the MongoDB server to cancel long-running
operations; it only instructs the driver to stop waiting for a response
and throw a <span class="classname">MongoCursorTimeoutException</span>
after a set time. If you need to specify a server-side timeout for a
command, considering passing the *maxTimeMS* option to <span
class="methodname">MongoCollection::aggregateCursor</span>.

### 参见

-   <span class="function">MongoCollection::aggregateCursor</span>
-   <span class="methodname">MongoCursorInterface::timeout</span>
-   The *socketTimeoutMS* option for <span
    class="function">MongoClient::\_\_construct</span>

MongoCommandCursor::valid
=========================

Checks if the cursor is reading a valid result

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoCommandCursor::valid</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current result is not null, and **`FALSE`** otherwise.

### 参见

-   <span class="methodname">Iterator::valid</span>

Types
=====

**目录**

-   [MongoId](/book/mongo.html#MongoId) — MongoId 类
    -   [MongoId::\_\_construct](/book/mongo.html#MongoId::__construct)
        — 创建一个新的id
    -   [MongoId::getHostname](/book/mongo.html#MongoId::getHostname) —
        获取这台机器上 id 所使用的 hostname
    -   [MongoId::getInc](/book/mongo.html#MongoId::getInc) —
        返回用于创建 id 所增加的值
    -   [MongoId::getPID](/book/mongo.html#MongoId::getPID) — 获取进程
        ID
    -   [MongoId::getTimestamp](/book/mongo.html#MongoId::getTimestamp)
        — 获取新纪元时间到 id 创建时的秒数。
    -   [MongoId::isValid](/book/mongo.html#MongoId::isValid) — Check if
        a value is a valid ObjectId
    -   [MongoId::\_\_set\_state](/book/mongo.html#MongoId::__set_state)
        — 创建一个假的 MongoId
    -   [MongoId::\_\_toString](/book/mongo.html#MongoId::__toString) —
        返回该 id 十六进制的表示形式
-   [MongoCode](/book/mongo.html#MongoCode) — The MongoCode class
    -   [MongoCode::\_\_construct](/book/mongo.html#MongoCode::__construct)
        — 创建一个新的代码对象
    -   [MongoCode::\_\_toString](/book/mongo.html#MongoCode::__toString)
        — 返回代码的字符串形式
-   [MongoDate](/book/mongo.html#MongoDate) — The MongoDate class
    -   [MongoDate::\_\_construct](/book/mongo.html#MongoDate::__construct)
        — 创建一个新的日期。
    -   [MongoDate::toDateTime](/book/mongo.html#MongoDate::toDateTime)
        — Returns a DateTime object representing this date
    -   [MongoDate::\_\_toString](/book/mongo.html#MongoDate::__toString)
        — 返回该日期的字符串形式的表达
-   [MongoRegex](/book/mongo.html#MongoRegex) — MongoRegex 类
    -   [MongoRegex::\_\_construct](/book/mongo.html#MongoRegex::__construct)
        — 创建一个新的正则表达式
    -   [MongoRegex::\_\_toString](/book/mongo.html#MongoRegex::__toString)
        — 正则表达式的字符串表达形式
-   [MongoBinData](/book/mongo.html#MongoBinData) — The MongoBinData
    class
    -   [MongoBinData::\_\_construct](/book/mongo.html#MongoBinData::__construct)
        — 创建一个新的二进制数据对象
    -   [MongoBinData::\_\_toString](/book/mongo.html#MongoBinData::__toString)
        — 二进制数据对象的字符串表达形式。
-   [MongoInt32](/book/mongo.html#MongoInt32) — MongoInt32 类
    -   [MongoInt32::\_\_construct](/book/mongo.html#MongoInt32::__construct)
        — 创建一个新的 32位 integer。
    -   [MongoInt32::\_\_toString](/book/mongo.html#MongoInt32::__toString)
        — 返回该 32 位 integer 的字符串表示。
-   [MongoInt64](/book/mongo.html#MongoInt64) — MongoInt64 类
    -   [MongoInt64::\_\_construct](/book/mongo.html#MongoInt64::__construct)
        — 创建一个新的 64 位 integer。
    -   [MongoInt64::\_\_toString](/book/mongo.html#MongoInt64::__toString)
        — 返回该 64 位 integer 的字符串表示形式。
-   [MongoDBRef](/book/mongo.html#MongoDBRef) — MongoDBRef 类
    -   [MongoDBRef::create](/book/mongo.html#MongoDBRef::create) —
        创建一个新的数据库引用
    -   [MongoDBRef::get](/book/mongo.html#MongoDBRef::get) —
        获取引用所指向的对象
    -   [MongoDBRef::isRef](/book/mongo.html#MongoDBRef::isRef) —
        检测数组是否为数据库引用
-   [MongoMinKey](/book/mongo.html#MongoMinKey) — The MongoMinKey class
-   [MongoMaxKey](/book/mongo.html#MongoMaxKey) — The MongoMaxKey class
-   [MongoTimestamp](/book/mongo.html#MongoTimestamp) — MongoTimestamp
    类
    -   [MongoTimestamp::\_\_construct](/book/mongo.html#MongoTimestamp::__construct)
        — 创建一个新的时间戳。
    -   [MongoTimestamp::\_\_toString](/book/mongo.html#MongoTimestamp::__toString)
        — 返回时间戳的字符串表示形式

MongoDB allows programmers to save and query for data expressed in all
of the basic PHP types, compound types (arrays, associative arrays, and
objects), and a half-dozen classes provided by the MongoDB PHP driver
(for regular expressions, dates, and other specialized applications).

Booleans and **`NULL`**
-----------------------

**`TRUE`**, **`FALSE`**, and **`NULL`** can be used as-is.

Numbers
-------

Numbers are distinct from strings in MongoDB: "123" does not match 123.
Thus, if you want to make sure numbers are sorted and matched correctly,
you must make sure that they are actually saved as numbers.

``` php
<?php

$doc = array("a" => 123, "b" => "123");
$collection->insert($doc);

$doc->find(array("a" => 123));   // matches
$doc->find(array("a" => "123")); // doesn't match
$doc->find(array("a" => 123.0)); // matches
$doc->find(array("b" => 123));   // doesn't match
$doc->find(array("b" => "123")); // matches

?>
```

As noted above, floating point numbers do compare with/match integer
numbers as one would expect.

Large Numbers
-------------

By default, on a 32-bit system, numbers are sent to the database as
32-bit integers. On a 64-bit system, they are sent as 64-bit integers.
For backwards compatibility, all systems deserialize 64-bit integers as
floating point numbers. Floating point numbers are not exact. If you
need exact values, you must tweak your
<a href="/book/mongo.html#运行时配置" class="link">php.ini settings</a>.

On a 32-bit system, if *mongo.long\_as\_object* is set, 64-bit integers
will be returns as <span class="classname">MongoInt64</span> objects.
The integer will be stored in the *value* field with perfect precision
(as a string). You can also use <span
class="classname">MongoInt64</span> to save 64-bit integers on 32-bit
machines.

On 64-bit systems, you can either set *mongo.long\_as\_object* or set
*mongo.native\_long*. *mongo.native\_long* will return 64-bit integers
and "normal" PHP integers. You can use <span
class="classname">MongoInt32</span> to save 32-bit integers on 64-bit
machines.

You should set the *mongo.long\_as\_object* and *mongo.native\_long*
behavior that you plan to use, even if it is the default behavior (to
protect against future changes to the defaults).

See also:
<a href="/book/mongo.html#运行时配置" class="link">php.ini Options</a>,
<span class="classname">MongoInt32</span>, <span
class="classname">MongoInt64</span>.

Strings
-------

Strings must be UTF-8. Non-UTF-8 strings must either be converted to
UTF-8 before being sent to the database or saved as binary data.

Regular expressions can be used to match strings, and are expressed
using the <span class="classname">MongoRegex</span> class.

Binary Data
-----------

Non-UTF-8 strings, images, and any other binary data should be sent to
the database using the <span class="classname">MongoBinData</span> type.

Dates
-----

Dates can be created using the <span class="classname">MongoDate</span>
class. They are stored as milliseconds since the epoch.

<span class="classname">MongoTimestamp</span> is not for saving dates or
timestamps, it is used internally by MongoDB. Unless you are creating a
tool that interacts with the internals of replication or sharding, you
should use <span class="classname">MongoDate</span>, *not* <span
class="classname">MongoTimestamp</span>.

Unique Ids
----------

The driver will automatically create an *\_id* field before inserting a
document (unless one is specified by the user). This field is an
instance of <span class="classname">MongoId</span> (called "ObjectId" in
most other languages).

These ids are 12 bytes long and composed of:

-   4 bytes of timestamp

    No two records can have the same id if they were inserted at
    different times.

-   3 bytes machine id

    No two records can have the same id if they were inserted on
    different machines

-   2 bytes thread id

    No two records can have the same id if they were inserted by
    different threads running on the same machine.

-   3 bytes incrementing value

    Each time an id is created, a global counter is incremented and used
    as the increment value of the next id.

Thus, no two records can have the same id unless a single process on a
single machine managed to insert 256^3 (over 16 million) documents in
one second, overflowing the increment field.

JavaScript
----------

MongoDB comes with a JavaScript engine, so you can embed JavaScript in
queries (using a $where clause), send it directly to the database to be
executed, and use it to perform aggregations.

For security, use <span class="classname">MongoCode</span>'s *scope*
field to use PHP variables in JavaScript. Code that does not require
external values can either use <span class="classname">MongoCode</span>
or just be a string. See the
<a href="/book/mongo.html#Security" class="link">section on security</a>
for more information about sending JavaScript to the database.

Arrays and Objects
------------------

Arrays and objects can also be saved to the database. An array with
ascending numeric keys will be saved as a an array, anything else will
be saved as an object.

``` php
<?php

// $scores will be saved as an array
$scores = array(98, 100, 73, 85);
$collection->insert(array("scores" => $scores));

// $scores will be saved as an object
$scores = array("quiz1" => 98, "midterm" => 100, "quiz2" => 73, "final" => 85);
$collection->insert(array("scores" => $scores));

?>
```

If you query for these objects using the database shell, they will look
like:

``` shell
> db.students.find()
{ "_id" : ObjectId("4b06beada9ad6390dab17c43"), "scores" : [ 98, 100, 73, 85 ] }
{ "_id" : ObjectId("4b06bebea9ad6390dab17c44"), "scores" : { "quiz1" : 98, "midterm" : 100, "quiz2" : 73, "final" : 85 } }
```

The database can also save arbitrary PHP objects (although they will be
returned as associative arrays). The fields are used for the key/value
pairs. For example, a blog post might look like:

``` php
<?php

  // the blog post class
  class Post {

  var $author;
  var $content;
  var $comments = array();
  var $date;

  public function __construct($author, $content) {
  $this->author = $author;
$this->content = $content;
    $this->date = new MongoDate();
  }

  public function setTitle($title) {
    $this->title = $title;
  }
}

// create a simple blog post and insert it into the database
$post1 = new Post("Adam", "This is a blog post");

$blog->insert($post1);


// there is nothing restricting the type of the "author" field, so we can make
// it a nested object
$author = array("name" => "Fred", "karma" => 42);
$post2 = new Post($author, "This is another blog post.");

// we create an extra field by setting the title
$post2->setTitle("Second Post");

$blog->insert($post2);

?>
```

From the database shell, this will look something like:

``` shell
> db.blog.find()
{ "_id" : ObjectId("4b06c263edb87a281e09dad8"), "author" : "Adam", "content" : "This is a blog post", "comments" : [ ], "date" : "Fri Nov 20 2009 11:22:59 GMT-0500 (EST)" }
{ "_id" : ObjectId("4b06c282edb87a281e09dad9"), "author" : { "name" : "Fred", "karma" : 42 }, "content" : "This is a blog post", "comments" : [ ], "date" : "Fri Nov 20 2009 11:23:30 GMT-0500 (EST)", "title" : "Second Post" }
```

The driver will not detect reference loops in arrays and objects. For
example, this will give a fatal error:

``` php
<?php

$collection->insert($GLOBALS);

?>
```

``` txt
Fatal error: Nesting level too deep - recursive dependency?
```

If you need to insert documents that may have recursive dependency, you
have to check for it yourself before passing it to the driver.

简介
----

为数据库对象创建的唯一标识符。 如果插入数据库的对象不具有 \_id
字段，将会为 \_id 字段添加一个 <span class="classname">MongoId</span>
实例作为值。 如果数据具有自然的唯一字段（比如说，用户名或
timestamp），用来作为 \_id 字段也不错，它不会被 一个 <span
class="classname">MongoId</span> 替换。

<span class="classname">MongoId</span>
类实例满足了关系数据库中自增列的角色：
如果数据不具有天然的唯一键，则提供一个。
自增列在分布式数据库中不会工作得很好，因为它无法快速找到下一个数字。
这个类能够满足在分布式下快速产生唯一值的条件。

每个 MongoId 具有 12 个字节（使它的字符串形式是 24 个十六进制字符）。
前四个字节是一个时间戳（timestamp），后三个是客户端主机名的 hash
摘要，然后两个是运行脚本的进程 ID， 最后三位是一个自增值。

<span class="classname">MongoId</span> 是可以序列化/反序列化的。
它们序列化后的格式和它们的字符串格式比较像：

    C:7:"MongoId":24:{4af9f23d8ead0e1d32000000}

类摘要
------

**MongoId**

<span class="ooclass"> class **MongoId** </span> {

<span class="modifier">public</span> <span class="type">string</span>
`$id` <span class="initializer"> = **`NULL`**</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string\|MongoId</span> `$id`<span
class="initializer"> = **`NULL`**</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getHostname</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getInc</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPID</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isValid</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">MongoId</span> <span
class="methodname">\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$props`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

Fields
------

`id`  
<span class="simpara"> 这个字段包含了该对象的字符串表达形式。 </span>

参见
----

关于
<a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ids</a>
的 MongoDB 核心文档。

MongoId::\_\_construct
======================

创建一个新的id

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\ObjectID::\_\_construct</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoId::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string\|MongoId</span> `$id`<span
class="initializer"> = **`NULL`**</span></span> \] )

### 参数

`id`  
用于 id 的一个字符串。必须为24个十六进制的字符，或者也可以是 <span
class="classname">MongoId</span> 实例。

### 返回值

返回一个新的 id。

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 1.4.0 | 传入无效字符将抛出异常 |

### 范例

**示例 \#1 <span class="function">MongoId::\_\_construct</span> 例子**

这个例子展示了如何创建一个新的 id。
这很少用到，因为在保存到数据库之前，驱动会为数组自动添加一个id。

``` php
<?php

  $id1 = new MongoId();
  echo "$id1\n";

  $id2 = new MongoId();
  echo "$id2\n";

  ?>
```

以上例程的输出类似于：

    49a7011a05c677b9a916612a
    49a702d5450046d3d515d10d

**示例 \#2 参数的例子**

这个例子展示了如何使用 string 的参数来初始化一个指定值的 MongoId。

``` php
<?php
  $id1 = new MongoId();

  // 从 $id1 创建一个新的 MongoId
  $id2 = new MongoId("$id1");

  // 显示 $id1 和 $id2 具有相同的十六进制值
  var_dump($id1 == $id2);
  ?>
```

以上例程的输出类似于：

    bool(true)

### 参见

-   <span class="methodname">MongoId::\_\_toString</span>
-   <span class="methodname">MongoId::isvalid</span>

MongoId::getHostname
====================

获取这台机器上 id 所使用的 hostname

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">MongoId::getHostname</span> ( <span
class="methodparam">void</span> )

返回的 hostname 用于 <span class="classname">MongoId</span> 产生唯一
id。 这和 <span class="function">gethostname</span> 应该会返回同样的值。

它和以下函数是一样的：

``` php
<?php

public static function getHostname() {
    return gethostname();
}

?>
```

### 参数

此函数没有参数。

### 返回值

返回 hostname。

MongoId::getInc
===============

返回用于创建 id 所增加的值

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoId::getInc</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回增加的值，用于创建 <span class="classname">MongoId</span>。

MongoId::getPID
===============

获取进程 ID

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoId::getPID</span> ( <span
class="methodparam">void</span> )

从 Mongo ID 中提取 pid。

### 参数

此函数没有参数。

### 返回值

返回 <span class="classname">MongoId</span> 里的 PID。

MongoId::getTimestamp
=====================

获取新纪元时间到 id 创建时的秒数。

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoId::getTimestamp</span> ( <span
class="methodparam">void</span> )

返回 id 创建时运行 <span class="function">time</span> 同样的东西。

### 参数

此函数没有参数。

### 返回值

获取新纪元时间到 id 创建时的秒数。 仅储存了四个字节的时间戳，所以 <span
class="classname">MongoDate</span>
是储存更精准、更广范围时间的更佳选择。

MongoId::isValid
================

Check if a value is a valid ObjectId

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">MongoId::isValid</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

This method may be used to check a variable before passing it as an
argument to <span class="function">MongoId::\_\_construct</span>.

### 参数

`value`  
The value to check for validity.

### 返回值

Returns **`TRUE`** if `value` is a <span
class="classname">MongoId</span> instance or a string consisting of
exactly 24 hexadecimal characters; otherwise, **`FALSE`** is returned.

MongoId::\_\_set\_state
=======================

创建一个假的 MongoId

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">MongoId</span> <span
class="methodname">MongoId::\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$props`</span> )

该函数仅被 PHP 内部使用，用户不需要调用它。

它和下面的函数是一样的：

``` php
<?php

public static function __set_state($props) {
    return new MongoId("000000000000000000000000");
}

?>
```

### 参数

`props`  
从理论上讲，要用数组的属性来创建一个新 id。但是 MongoId
示例没有属性，所以这是没用的。

### 返回值

具有 "000000000000000000000000" 的值的 id。

MongoId::\_\_toString
=====================

返回该 id 十六进制的表示形式

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\ObjectID::\_\_toString</span>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoId::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

该 id。

### 范例

**示例 \#1 <span class="function">MongoId::\_\_toString</span> 例子**

``` php
<?php

$m = new MongoClient();
$collection = $m->selectDB("foo")->selectCollection("bar");

$collection->insert(array( "x" => "y" ));
$collection->insert(array( "x" => "y" ));

$cursor = $collection->find();
$r1 = $cursor->next();
$r2 = $cursor->next();

echo $r1["_id"] . "\n";
echo $r2["_id"] . "\n";

?>
```

以上例程的输出类似于：

    49a7011a05c677b9a916612a
    49a702d5450046d3d515d10d

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\BSON\\JavaScript</span>

简介
----

Represents JavaScript code for the database.

MongoCode objects are composed of two parts: a string of code and an
optional scope. The string of code must be valid JavaScript. The scope
is a associative array of variable name/value pairs.

类摘要
------

**MongoCode**

<span class="ooclass"> class **MongoCode** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">array</span> `$scope`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoCode::\_\_construct
========================

创建一个新的代码对象

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\JavaScript::\_\_construct</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoCode::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">array</span> `$scope`<span
class="initializer"> = array()</span></span> \] )

### 参数

`code`  
字符串代码。

`scope`  
使用代码的范围。

### 返回值

返回一个新的代码对象。

### 范例

**示例 \#1 <span class="methodname">MongoCode::\_\_construct</span>
例子**

``` php
<?php

$code = new MongoCode('function() { '.
    'for(i=0;i<10;i++) {'.
        'db.foo.update({z : i}, {z : x});'.
    '}'.
    'return x-1;'.
 '}', array("x" => 4));
var_dump($code);

?>
```

以上例程的输出类似于：

    object(MongoCode)#1 (2) {
      ["scope"]=>
      array(1) {
        ["x"]=>
        int(4)
      }
      ["code"]=>
      string(80) "function() { for(i=0;i<10;i++) { db.foo.update({z : i}, {z : x}); } return x-1; }"
    }

**示例 \#2 使用具有 $where 的 <span class="classname">MongoCode</span>**

这个例子查询了集合里，'x' 字段比 $y 小的元素。 注意，PHP 对象能够传入到
JavaScript 作用域，然后 JavaScript 函数返回一个 boolean。

``` php
<?php

$cursor = $collection->find(array('$where' => new MongoCode('function() { return this.x < y; }', array('y'=>$y))));

?>
```

MongoCode::\_\_toString
=======================

返回代码的字符串形式

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this method in the new extension.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoCode::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

该代码，不会返回作用域。

### 范例

**示例 \#1 <span class="function">MongoCode::\_\_toString</span> 例子**

``` php
<?php

$code = new MongoCode('return x;', array("x"=>"hi"));
echo "$code\n";

$code = new MongoCode('function() { for(i=0;i<10;i++) { db.foo.update({x:i}, {x:i+1}); } }');
echo "$code\n";

?>
```

以上例程的输出类似于：

    return x;
    function() { for(i=0;i<10;i++) { db.foo.update({x:i}, {x:i+1}); } }

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\BSON\\UTCDateTime</span>

简介
----

Represent date objects for the database. This class should be used to
save dates to the database and to query for dates. For example:

**示例 \#1 Storing dates with <span class="classname">MongoDate</span>**

``` php
<?php

// save a date to the database
$collection->save(array("ts" => new MongoDate()));

$start = new MongoDate(strtotime("2010-01-15 00:00:00"));
$end = new MongoDate(strtotime("2010-01-30 00:00:00"));

// find dates between 1/15/2010 and 1/30/2010
$collection->find(array("ts" => array('$gt' => $start, '$lte' => $end)));

?>
```

MongoDB stores dates as milliseconds past the epoch. This means that
dates *do not* contain timezone information. Timezones must be stored in
a separate field if needed. Second, this means that any precision beyond
milliseconds will be lost when the document is sent to/from the
database.

类摘要
------

**MongoDate**

<span class="ooclass"> class **MongoDate** </span> {

/\* Fields \*/

<span class="modifier">public</span> <span class="type">int</span>
`$sec` ;

<span class="modifier">public</span> <span class="type">int</span>
`$usec` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$sec`<span
class="initializer"> = time()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$usec`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">toDateTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDate::\_\_construct
========================

创建一个新的日期。

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\UTCDateTime::\_\_construct</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoDate::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$sec`<span
class="initializer"> = time()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$usec`<span
class="initializer"> = 0</span></span> \]\] )

创建一个新的日期。如果没有指定参数，将会使用当前的时间。

### 参数

`sec`  
自纪元时间以来的秒数(例如 1 Jan 1970 00:00:00.000 UTC)。

`usec`  
微秒。请注意 MongoDB
的解决方案是*毫秒*而不是微秒，这意味着这个值会被截成毫秒的方案。

### 返回值

返回该新的时间。

### 范例

**示例 \#1 <span class="function">MongoDate::\_\_construct</span> 例子**

这个例子演示了用当前时间创建一个新的日期以及给定时间的新日期。

``` php
<?php

$d = new MongoDate();
echo "$d\n";
$d = new MongoDate(1234567890);
echo "$d\n";
$d = new MongoDate(strtotime("2009-05-01 00:00:01"));
echo "$d\n";

?>
```

以上例程的输出类似于：

    0.23660600 1235685067
    0.00000000 1234567890
    0.00000000 1241150401

### 参见

-   <span class="methodname">MongoDate::\_\_toString</span>

MongoDate::toDateTime
=====================

Returns a DateTime object representing this date

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\UTCDateTime::toDateTime</span>

### 说明

<span class="modifier">public</span> <span class="type">DateTime</span>
<span class="methodname">MongoDate::toDateTime</span> ( <span
class="methodparam">void</span> )

Returns the <span class="classname">DateTime</span> representation of
this date. The returned <span class="classname">DateTime</span> will use
the UTC time zone.

### 参数

此函数没有参数。

### 返回值

This date as a <span class="classname">DateTime</span> object.

### 范例

**示例 \#1 <span class="function">MongoDate::toDateTime</span> example**

This example demonstrates creating a DateTime object from a MongoDate
object.

``` php
<?php
$d = new MongoDate(strtotime("2014-11-18 11:01:25"));
var_dump( $d->toDateTime() );
?>
```

以上例程的输出类似于：

    class DateTime#2 (3) {
      public $date =>
      string(26) "2014-11-18 11:01:25.000000"
      public $timezone_type =>
      int(1)
      public $timezone =>
      string(6) "+00:00"
    }

MongoDate::\_\_toString
=======================

返回该日期的字符串形式的表达

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\UTCDateTime::\_\_toString</span>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoDate::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回该日期的字符串表示形式，类似 <span class="function">microtime</span>
返回的表示。

### 参数

此函数没有参数。

### 返回值

该日期。

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\BSON\\Regex</span>

简介
----

这个类用于创建一个正则表达式。
通常这些表达式用于查询数据库中匹配的字符串。不常用的是，它们可以保存到数据库并用于检索。

正则表达式由四部分组成。 首先 */* 作为起始的分隔符，然后是
pattern、另一个 */* 以及最后包含 flag 的字符串。

**示例 \#1 正则表达式**

    /pattern/flags

Mongo 能够识别六种正则表达式标记（flag）：

-   *i*：大小写不敏感

-   *m*：多行

-   *x*：能够包含注释

-   *l*：语言环境

-   *s*：dotall，"." 匹配任何字符，包括换行符。

-   *u*：匹配 Unicode

类摘要
------

**MongoRegex**

<span class="ooclass"> class **MongoRegex** </span> {

/\* 字段 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$regex` ;

<span class="modifier">public</span> <span class="type">string</span>
`$flags` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$regex`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoRegex::\_\_construct
=========================

创建一个新的正则表达式

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\Regex::\_\_construct</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoRegex::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$regex`</span> )

创建一个新的正则表达式。

### 参数

`regex`  
以 */expr/flags* 形式的正则表达式字符串。

### 返回值

返回一个新的正则表达式。

### 范例

**示例 \#1 <span class="function">MongoRegex::\_\_construct</span>
例子**

这个例子使用了正则表达式来查询包含匹配正则表达式的所有文档，用户名字段以
(*^*) 开始，一个 *l* 和一个元音字母 (*\[aeiouy\]*)，大小写不敏感
(*/i*)。

``` php
<?php
$luke_search = new MongoRegex("/^l[aeiouy]/i");
$cursor = $collection->find(array("username" => $luke_search));
?>
```

### 参见

-   <span class="methodname">MongoRegex::\_\_toString</span>

MongoRegex::\_\_toString
========================

正则表达式的字符串表达形式

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span class="methodname">MongoDB\\BSON\\Regex::\_\_toString</span>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoRegex::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回该正则表达式的字符串表示形式。

### 参数

此函数没有参数。

### 返回值

以 "/expr/flags" 形式的正则表达式。

### 范例

**示例 \#1 <span class="function">MongoRegex::\_\_toString</span> 例子**

``` php
<?php

$r = new MongoRegex( "/[a-fA-F0-9]{16}/g" );
echo $r->regex . "\n";
echo $r->flags . "\n";
echo "$r\n";

?>
```

以上例程的输出类似于：

    [a-fA-F0-9]{16}
    g
    /[a-fA-F0-9]{16}/g

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\BSON\\Binary</span>

简介
----

An object that can be used to store or retrieve binary data from the
database.

The maximum size of a single object that can be inserted into the
database is 16MB. For data that is larger than this (movies, music,
Henry Kissinger's autobiography), use <span
class="classname">MongoGridFS</span>. For data that is smaller than
16MB, you may find it easier to embed it within the document using <span
class="classname">MongoBinData</span>.

For example, to embed an image in a document, one could write:

``` php
<?php

$profile = array(
    "username" => "foobity",
    "pic" => new MongoBinData(file_get_contents("gravatar.jpg"), MongoBinData::GENERIC),
);

$users->save($profile);

?>
```

This class contains a `type` field, which currently gives no additional
functionality in the PHP driver or the database. There are seven
predefined types, which are defined as class constants below. For
backwards compatibility, the PHP driver uses
**`MongoBinData::BYTE_ARRAY`** as the default; however, this may change
to **`MongoBinData::GENERIC`** in the future. Users are encouraged to
specify a type in <span
class="function">MongoBinData::\_\_construct</span>.

类摘要
------

**MongoBinData**

<span class="ooclass"> class **MongoBinData** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::GENERIC` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::FUNC` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::BYTE_ARRAY` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::UUID` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::UUID_RFC4122` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::MD5` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoBinData::CUSTOM` <span class="initializer"> = 128</span> ;

/\* Fields \*/

<span class="modifier">public</span> <span class="type">string</span>
`$bin` ;

<span class="modifier">public</span> <span class="type">int</span>
`$type` <span class="initializer"> = 2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

Binary Data Types
-----------------

**`MongoBinData::GENERIC`**  
<span class="simpara"> Generic binary data. </span>

**`MongoBinData::FUNC`**  
<span class="simpara"> Function. </span>

**`MongoBinData::BYTE_ARRAY`**  
<span class="simpara"> Generic binary data (deprecated in favor of
**`MongoBinData::GENERIC`**). </span>

**`MongoBinData::UUID`**  
<span class="simpara"> Universally unique identifier (deprecated in
favor of **`MongoBinData::UUID_RFC4122`**). </span>

**`MongoBinData::UUID_RFC4122`**  
<span class="simpara"> Universally unique identifier (according to
<a href="http://www.faqs.org/rfcs/rfc4122" class="link external">» RFC 4122</a>).
</span>

**`MongoBinData::MD5`**  
<span class="simpara"> MD5. </span>

**`MongoBinData::CUSTOM`**  
<span class="simpara"> User-defined type. </span>

| 版本  | 说明                                                                              |
|-------|-----------------------------------------------------------------------------------|
| 1.5.0 | Added **`MongoBinData::GENERIC`** and **`MongoBinData::UUID_RFC4122`** constants. |

MongoBinData::\_\_construct
===========================

创建一个新的二进制数据对象

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\Binary::\_\_construct</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoBinData::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = 0</span></span> \] )

创建一个新的二进制数据对象。

当前有七种类型的二进制数据能被 BSON
规格所识别，在<a href="/book/mongo.html#Binary%20Data%20Types" class="link">类的常量</a>
中定义。 为了反向兼容性，PHP 默认使用
**`MongoBinData::BYTE_ARRAY`**；不过，未来可能修改成
**`MongoBinData::GENERIC`**。 用户最好指定下类型，而不该依赖默认类型。

### 参数

`data`  
二进制数据。

`type`  
数据类型。

### 返回值

返回一个新的二进制数据对象。

### 更新日志

| 版本   | 说明                                                                                    |
|--------|-----------------------------------------------------------------------------------------|
| 1.5.0  | 默认值从 *2* (**`MongoBinData::BYTE_ARRAY`**) 改成 *0* (**`MongoBinData::GENERIC`**)。  |
| 1.2.11 | 没有使用第二个参数时产生 **`E_DEPRECATED`**。 `type` 的默认值在近期的功能里可能会改变。 |

MongoBinData::\_\_toString
==========================

二进制数据对象的字符串表达形式。

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span class="methodname">MongoDB\\BSON\\Binary::getData</span>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoBinData::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回字符串 "\<Mongo Binary Data\>"。要获取 <span
class="classname">MongoBinData</span> 的内容，使用 *bin* 字段。

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this class in the new extension.

作为替代，新的扩展会根据 Integer 的值选择合适的数据库数据类型。

简介
----

这个类可以在一个 64 位的操作系统上将 32 位的 integer 保存到数据库。

类摘要
------

**MongoInt32**

<span class="ooclass"> class **MongoInt32** </span> {

/\* 字段 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$value` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

字段
----

`value`  
<span class="simpara"> This is the string value of the 64-bit number.
例如，123 的值应该是 "123"。 </span>

MongoInt32::\_\_construct
=========================

创建一个新的 32位 integer。

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 作为替代，新扩展会根据 Integer 的值做合适的数据库类型选择。

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoInt32::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

创建具有指定值的 32 位数字。

### 参数

`value`  
一个数字。

### 返回值

返回新的 integer。

MongoInt32::\_\_toString
========================

返回该 32 位 integer 的字符串表示。

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 作为替代，新扩展会根据 Integer 的值做合适的数据库类型选择。

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoInt32::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回该 integer 字符串形式的表示。

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. There is no equivalent for this class in the new extension.

作为替代，新的扩展会根据 Integer 的值选择合适的数据库数据类型。

简介
----

这个类能够在 32 位的系统上保存一个 64 位的 integer 到数据库。

类摘要
------

**MongoInt64**

<span class="ooclass"> class **MongoInt64** </span> {

/\* 字段 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$value` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

字段
----

`value`  
<span class="simpara"> 64 位数字的字符串值。例如 ，123 的值是 "123"。
</span>

MongoInt64::\_\_construct
=========================

创建一个新的 64 位 integer。

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 作为替代，新扩展会根据 Integer 的值做合适的数据库类型选择。

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoInt64::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

创建具有指定值的新的 64 位数字。

### 参数

`value`  
一个数字。

### 返回值

返回一个新的 integer。

MongoInt64::\_\_toString
========================

返回该 64 位 integer 的字符串表示形式。

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 作为替代，新扩展会根据 Integer 的值做合适的数据库类型选择。

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoInt64::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回该 integer 的字符串表示形式。

简介
----

这个类可以用于创建不同集合中对象间的轻量级的链接。

*Motivation*：如果我们需要引用其他集合中的文档。最简单的方法是在当前文档中创建一个字段。比如，有
"people" 集合和 "addresses" 集合，我们需要“关联”每个 person 和对应的
address ，可以：

**示例 \#1 链接文档**

``` php
<?php

$people = $db->people;
$addresses = $db->addresses;

$myAddress = array("line 1" => "123 Main Street", 
    "line 2" => null,
    "city" => "Springfield",
    "state" => "Vermont",
    "country" => "USA");

// save the address 保存address文档
$addresses->insert($myAddress);

// save a person with a reference to the address 保存一个people，关联刚才的address
$me = array("name" => "Fred", "address" => $myAddress['_id']);
$people->insert($me);

?>
```

然后，我们可以：把保存在 "people" 集合中的 <span
class="classname">MongoId</span> 作为条件，查询 "address"
集合，来获取一个人的地址。

如果我们现在有更加一般性的的情况，我们不知道哪个集合（甚至数据库）中包含我们要引用的文档。
<span class="classname">MongoDBRef</span>
就是个好选择，它是一个更加通用的格式，所有的驱动和数据库都可以处理它。

如果每个“人”有一系列关联到其他多个集合的信息，例如爱好、运动、书籍等，我们可以用数个
<span class="classname">MongoDBRef</span> 对象来跟踪每一个 爱好
来自哪个集合：

**示例 \#2 Creating MongoDBRef links**

``` php
<?php

$people = $db->selectCollection("people");

// model trains are in the "hobbies" collection
$trainRef = MongoDBRef::create("hobbies", $modelTrains['_id']);
// soccer is in the "sports" collection
$soccerRef = MongoDBRef::create("sports", $soccer['_id']);

// now we'll know what collections the items in the "likes" array came from when
// we retrieve this document
//  # 现在当我们读取这个文档的时候，就可以知道“likes”字段里的数组元素分别来自哪个集合了。
$people->insert(array("name" => "Fred", "likes" => array($trainRef, $soccerRef)));

?>
```

数据库引用可以被理解为超链接：它们指定了一个文档的唯一地址，但不会自动读取或者跟踪引用、链接。、

一个数据库引用仅仅是一个普通关联数组，不是 <span
class="classname">MongoDBRef</span>
的实例，所以这个类与其他数据类型有些不同。这个类只包含静态方法，用来操作引用。
译注：上面两段的意思概括为
1.一个数据库引用与超链接相似，复制、删除、修改等操作不会影响原来的文档。
2.读取这个引用可以得知指向的文档的位置，但不能知道文档的内容，要手动解引用。
3.这个“引用”保存到Mongo的时候就是普通数组

类摘要
------

**MongoDBRef**

<span class="ooclass"> class **MongoDBRef** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">create</span> ( <span class="methodparam"><span
class="type">string</span> `$collection`</span> , <span
class="methodparam"><span class="type">mixed</span> `$id`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$database`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">MongoDB</span> `$db`</span> , <span
class="methodparam"><span class="type">array</span> `$ref`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isRef</span> ( <span class="methodparam"><span
class="type">mixed</span> `$ref`</span> )

}

参见
----

MongoDB 官方核心文档
<a href="https://docs.mongodb.com/manual/reference/database-references/" class="link external">» databases references</a>.

MongoDBRef::create
==================

创建一个新的数据库引用

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 数据库引用（database reference） 的概念，并且此类已经被弃用。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">MongoDBRef::create</span> ( <span
class="methodparam"><span class="type">string</span>
`$collection`</span> , <span class="methodparam"><span
class="type">mixed</span> `$id`</span> \[, <span
class="methodparam"><span class="type">string</span> `$database`</span>
\] )

如果没有指定数据库，将会使用当前数据库。

### 参数

`collection`  
集合名称（不包括数据库名）。

`id`  
要链接的对象的 \_id 字段。

`database`  
数据库名。

### 返回值

返回引用。

### 范例

**示例 \#1 <span class="function">MongoDBRef::create</span> 例子**

这个例子为文档创建了一个 *addresses* 的数据库引用。 <span
class="function">MongoCollection::getName</span>
函数返回集合的名字（不包括数据库名）。

``` php
<?php
$addresses = $db->addresses;
$people = $db->people;

// 保存 $address，所以它有一个 _id
$addresses->insert($address);

// 创建引用
$ref = MongoDBRef::create($addresses->getName(), $address['_id']);

//设置 $person 里的字段
$person['address'] = $ref;
$people->save($person);
?>
```

### 参见

-   <span class="methodname">MongoDB::createDBRef</span>
-   <span class="methodname">MongoCollection::createDBRef</span>

MongoDBRef::get
===============

获取引用所指向的对象

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 数据库引用（database reference） 的概念，并且此类已经被弃用。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">MongoDBRef::get</span> ( <span
class="methodparam"><span class="type">MongoDB</span> `$db`</span> ,
<span class="methodparam"><span class="type">array</span> `$ref`</span>
)

### 参数

`db`  
使用的数据库。

`ref`  
要获取的引用。

### 返回值

返回引用指向的文档，如果文档不存在则返回 **`NULL`**（该引用已损坏）。

### 范例

**示例 \#1 <span class="function">MongoCollection::createDBRef</span>
例子**

``` php
<?php

// 从 db 获取 $person。
$person = $people->findOne();

// 解析引用的 address
$address = MongoDBRef::get($people->db, $person['address']);

?>
```

### 参见

-   <span class="methodname">MongoDB::getDBRef</span>
-   <span class="methodname">MongoCollection::getDBRef</span>

MongoDBRef::isRef
=================

检测数组是否为数据库引用

> **Note**:
>
> This extension that defines this class is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. There is no equivalent for this class in the new extension.
>
> 数据库引用（database reference） 的概念，并且此类已经被弃用。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">MongoDBRef::isRef</span> ( <span
class="methodparam"><span class="type">mixed</span> `$ref`</span> )

这个方法没有真正读取引用的数据，所以它无法检测引用是否损坏。 它仅仅检查
`ref` 是否为有效的数据库引用格式（一个对象或数组，并具有 $ref 和 $id
的字段）。

### 参数

`ref`  
要检查的数组或对象。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\BSON\\MinKey</span>

简介
----

<span class="classname">MongoMinKey</span> is an special type used by
the database that compares less than all other possible BSON values.
Thus, if a query is sorted by a given field in ascending order, any
document with a <span class="classname">MongoMinKey</span> as its value
will be returned first.

<span class="classname">MongoMinKey</span> has no associated fields,
methods, or constants. It is merely the "smallest" value that can be
represented in the database.

> **Note**: <span class="simpara"> <span
> class="classname">MongoMinKey</span> is used internally by MongoDB for
> indexing and sharding. There is generally no reason to use this class
> in an application. </span>

类摘要
------

**MongoMinKey**

<span class="ooclass"> class **MongoMinKey** </span> {

}

Using <span class="classname">MongoMinKey</span> as a value
-----------------------------------------------------------

``` php
<?php

$collection->insert(array("task" => "lunch", "doBy" => new MongoMinKey));
$collection->insert(array("task" => "staff meeting", "doBy" => new MongoDate(strtotime("+4 days"))));

$cursor = $collection->find()->sort(array("doBy" => 1));

?>
```

The cursor will return the lunch document followed by the staff meeting
document. The lunch document will always be returned first, regardless
of what else is added to the collection (unless other documents are
added with <span class="classname">MongoMinKey</span> in their "doBy"
field).

-   <span class="classname">MongoMaxKey</span>

**Warning**

This extension that defines this class is deprecated. Instead, the
<a href="/set/mongodb.html" class="link">MongoDB</a> extension should be
used. Alternatives to this class include:

-   <span class="classname">MongoDB\\BSON\\MaxKey</span>

简介
----

<span class="classname">MongoMaxKey</span> is an special type used by
the database that compares greater than all other possible BSON values.
Thus, if a query is sorted by a given field in ascending order, any
document with a <span class="classname">MongoMaxKey</span> as its value
will be returned last.

<span class="classname">MongoMaxKey</span> has no associated fields,
methods, or constants. It is merely the "greatest" value that can be
represented in the database.

> **Note**: <span class="simpara"> <span
> class="classname">MongoMaxKey</span> is used internally by MongoDB for
> indexing and sharding. There is generally no reason to use this class
> in an application. </span>

类摘要
------

**MongoMaxKey**

<span class="ooclass"> class **MongoMaxKey** </span> {

}

Using <span class="classname">MongoMaxKey</span> as a value
-----------------------------------------------------------

``` php
<?php

$collection->insert(array("task" => "dishes", "doBy" => new MongoMaxKey));
$collection->insert(array("task" => "staff meeting", "doBy" => new MongoDate(strtotime("+4 days"))));

$cursor = $collection->find()->sort(array("doBy" => 1));

?>
```

The cursor will return the staff meeting document followed by the dishes
document. The dishes document will always be returned last, regardless
of what else is added to the collection (unless other documents are
added with <span class="classname">MongoMaxKey</span> in their "doBy"
field).

-   <span class="classname">MongoMinKey</span>

简介
----

<span class="classname">MongoTimestamp</span> 用于分片（sharding）。
如果你不是想写分布式工具，你需要的也许是 <span
class="classname">MongoDate</span>。

<span class="classname">MongoTimestamp</span> 是 4
字节的时间戳（自新纪元以来的秒数），和 4 字节的自增长值。

*这个类不用于测量时间、为文档创建时间戳或为一个文档自动增加、更新时间戳。*
除非你写的是关于分片式内部的交互，否则请停下，直接前往 <span
class="classname">MongoDate</span>，
不要再继续研究这个东西。这不是你要找的类。

如果你在写一个分片工具，继续阅读。

类摘要
------

**MongoTimestamp**

<span class="ooclass"> class **MongoTimestamp** </span> {

/\* 字段 \*/

<span class="modifier">public</span> <span class="type">int</span>
`$sec` <span class="initializer"> = 0</span> ;

<span class="modifier">public</span> <span class="type">int</span>
`$inc` <span class="initializer"> = 0</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$sec`<span
class="initializer"> = time()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$inc`</span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoTimestamp::\_\_construct
=============================

创建一个新的时间戳。

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\Timestamp::\_\_construct</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoTimestamp::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$sec`<span
class="initializer"> = time()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$inc`</span> \]\] )

创建一个新的时间戳。如果没有指定参数，将使用当前的时间戳，也会自动提供增量。
模块加载时增量设置为 0，并且在每次调用构造器时自动增加（没有传入 $inc
参数时）。

### 参数

`sec`  
自纪元时间以来的秒数(比如 1 Jan 1970 00:00:00.000 UTC)。

`inc`  
增量。

### 返回值

返回新的 timestamp。

### 参见

-   <span class="methodname">MongoTimestamp::\_\_toString</span>

MongoTimestamp::\_\_toString
============================

返回时间戳的字符串表示形式

> **Note**:
>
> This extension that defines this method is deprecated. Instead, the
> <a href="/set/mongodb.html" class="link">MongoDB</a> extension should
> be used. Alternatives to this method include:
>
> -   <span
>     class="methodname">MongoDB\\BSON\\Timestamp::\_\_toString</span>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoTimestamp::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回时间戳里的秒数字段。

### 参数

此函数没有参数。

### 返回值

该时间戳自新纪元时间以来的秒数。

GridFS Classes
==============

**目录**

-   [MongoGridFS](/book/mongo.html#MongoGridFS) — The MongoGridFS class
    -   [MongoGridFS::\_\_construct](/book/mongo.html#MongoGridFS::__construct)
        — Creates new file collections
    -   [MongoGridFS::delete](/book/mongo.html#MongoGridFS::delete) —
        Remove a file and its chunks from the database
    -   [MongoGridFS::drop](/book/mongo.html#MongoGridFS::drop) — Drops
        the files and chunks collections
    -   [MongoGridFS::find](/book/mongo.html#MongoGridFS::find) —
        Queries for files
    -   [MongoGridFS::findOne](/book/mongo.html#MongoGridFS::findOne) —
        Returns a single file matching the criteria
    -   [MongoGridFS::get](/book/mongo.html#MongoGridFS::get) — Retrieve
        a file from the database
    -   [MongoGridFS::put](/book/mongo.html#MongoGridFS::put) — Stores a
        file in the database
    -   [MongoGridFS::remove](/book/mongo.html#MongoGridFS::remove) —
        Remove files and their chunks from the database
    -   [MongoGridFS::storeBytes](/book/mongo.html#MongoGridFS::storeBytes)
        — Stores a string of bytes in the database
    -   [MongoGridFS::storeFile](/book/mongo.html#MongoGridFS::storeFile)
        — Stores a file in the database
    -   [MongoGridFS::storeUpload](/book/mongo.html#MongoGridFS::storeUpload)
        — Stores an uploaded file in the database
-   [MongoGridFSFile](/book/mongo.html#MongoGridFSFile) — The
    MongoGridFSFile class
    -   [MongoGridfsFile::\_\_construct](/book/mongo.html#MongoGridfsFile::__construct)
        — Create a new GridFS file
    -   [MongoGridFSFile::getBytes](/book/mongo.html#MongoGridFSFile::getBytes)
        — Returns this file's contents as a string of bytes
    -   [MongoGridFSFile::getFilename](/book/mongo.html#MongoGridFSFile::getFilename)
        — Returns this file's filename
    -   [MongoGridFSFile::getResource](/book/mongo.html#MongoGridFSFile::getResource)
        — Returns a resource that can be used to read the stored file
    -   [MongoGridFSFile::getSize](/book/mongo.html#MongoGridFSFile::getSize)
        — Returns this file's size
    -   [MongoGridFSFile::write](/book/mongo.html#MongoGridFSFile::write)
        — Writes this file to the filesystem
-   [MongoGridFSCursor](/book/mongo.html#MongoGridFSCursor) — The
    MongoGridFSCursor class
    -   [MongoGridFSCursor::\_\_construct](/book/mongo.html#MongoGridFSCursor::__construct)
        — Create a new cursor
    -   [MongoGridFSCursor::current](/book/mongo.html#MongoGridFSCursor::current)
        — Returns the current file
    -   [MongoGridFSCursor::getNext](/book/mongo.html#MongoGridFSCursor::getNext)
        — Return the next file to which this cursor points, and advance
        the cursor
    -   [MongoGridFSCursor::key](/book/mongo.html#MongoGridFSCursor::key)
        — Returns the current result's filename

简介
----

Utilities for storing and retrieving files from the database.

GridFS is a storage specification all supported drivers implement.
Basically, it defines two collections: *files*, for file metadata, and
*chunks*, for file content. If the file is large, it will automatically
be split into smaller chunks and each chunk will be saved as a document
in the chunks collection.

Each document in the files collection contains the filename, upload
date, and md5 hash. It also contains a unique *\_id* field, which can be
used to query the chunks collection for the file's content. Each
document in the chunks collection contains a chunk of binary data, a
*files\_id* field that matches its file's *\_id*, and the position of
this chunk in the overall file.

For example, the files document is something like:

``` php
<?php
array("_id" => 123456789, "filename" => "foo.txt", "chunkSize" => 3, "length" => 12);
?>
```

and the chunks documents look like:

``` php
<?php
array("files_id" => 123456789, "n" => 0, "data" => new MongoBinData("abc"));
array("files_id" => 123456789, "n" => 1, "data" => new MongoBinData("def"));
array("files_id" => 123456789, "n" => 2, "data" => new MongoBinData("ghi"));
array("files_id" => 123456789, "n" => 3, "data" => new MongoBinData("jkl"));
?>
```

Of course, the default chunk size is thousands of bytes, but that makes
an unwieldy example.

Inter-Language Compatibility
----------------------------

You should be able to use any files created by MongoGridFS with any
other drivers, and vice versa. However, some drivers expect that all
metadata associated with a file be in a "metadata" field. If you're
going to be using other languages, it's a good idea to wrap info you
might want them to see in a "metadata" field. For example, instead of:

``` php
<?php

$grid->storeFile("somefile.txt", array("date" => new MongoDate()));

?>
```

use something like:

``` php
<?php

$grid->storeFile("somefile.txt", array("metadata" => array("date" => new MongoDate())));

?>
```

The <span class="classname">MongoGridFS</span> Family
-----------------------------------------------------

<span class="classname">MongoGridFS</span> represents the files and
chunks collections. <span class="classname">MongoGridFS</span> extends
MongoCollection, and an instance of <span
class="classname">MongoGridFS</span> has access to all of <span
class="classname">MongoCollection</span> methods, which act on the files
collection:

``` php
<?php

$grid = $db->getGridFS();
$grid->update(array("filename" => "foo"), $newObj); // update on the files collection

?>
```

Another example of manipulating metadata:

``` php
<?php

// save a file
$id = $grid->storeFile("game.tgz");
$game = $grid->findOne();

// add a downloads counter
$game->file['downloads'] = 0;
$grid->save($game->file);

// increment the counter
$grid->update(array("_id" => $id), array('$inc' => array("downloads" => 1)));

?>
```

You can also access the chunks collection from an instance of <span
class="classname">MongoGridFS</span>:

``` php
<?php

  $chunks = $grid->chunks; // $chunks is a normal MongoCollection
$chunks->insert(array("x" => 4));

?>
```

There are some methods for <span class="classname">MongoGridFS</span>
with the same name as <span class="classname">MongoCollection</span>
methods, that behave slightly differently. For example, <span
class="function">MongoGridFS::remove</span> will remove any objects that
match the criteria from the files collection and their content from the
chunks collection.

To store something new in GridFS, there are a couple options. If you
have a filename, you can say:

``` php
<?php

$grid->storeFile($filename, array("whatever" => "metadata", "you" => "want"));

?>
```

If you have a string of bytes that isn't a file, you can also store that
using <span class="function">MongoGridFS::storeBytes</span>:

``` php
<?php

$grid->storeBytes($bytes, array("whatever" => "metadata", "you" => "want"));

?>
```

Querying a <span class="classname">MongoGridFS</span> collection returns
a <span class="classname">MongoGridFSCursor</span>, which behaves like a
normal <span class="classname">MongoCursor</span> except that it returns
<span class="classname">MongoGridFSFiles</span> instead of associative
arrays.

<span class="classname">MongoGridFSFiles</span> can be written back to
disc using <span class="function">MongoGridFSFile::write</span> or
retrieved in memory using <span
class="function">MongoGridFSFile::getBytes</span>. There is currently no
method that automatically streams chunks, but it would be fairly easy to
write by querying the *$grid-\>chunks* collection.

<span class="classname">MongoGridFSFile</span> objects contain a field
file which contains any file metadata.

类摘要
------

**MongoGridFS**

<span class="ooclass"> <span class="modifier">extends</span> class
**MongoCollection** </span> {

/\* Fields \*/

<span class="modifier">public</span> <span
class="type">MongoCollection</span> `$chunks` <span class="initializer">
= **`NULL`**</span> ;

<span class="modifier">protected</span> <span class="type">string</span>
`$filesName` <span class="initializer"> = **`NULL`**</span> ;

<span class="modifier">protected</span> <span class="type">string</span>
`$chunksName` <span class="initializer"> = **`NULL`**</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoDB</span> `$db`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$prefix`<span class="initializer"> = "fs"</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$chunks`<span
class="initializer"> = "fs"</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span class="methodname">delete</span> (
<span class="methodparam"><span class="type">mixed</span> `$id`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">drop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoGridFSCursor</span> <span
class="methodname">find</span> (\[ <span class="methodparam"><span
class="type">array</span> `$query`<span class="initializer"> =
array()</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$fields`<span class="initializer"> =
array()</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">findOne</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$query`<span class="initializer"> =
array()</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$fields`<span class="initializer"> =
array()</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span class="methodname">get</span>
( <span class="methodparam"><span class="type">mixed</span> `$id`</span>
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">put</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">array</span> `$metadata`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span class="methodname">remove</span>
(\[ <span class="methodparam"><span class="type">array</span>
`$criteria`<span class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">storeBytes</span> ( <span
class="methodparam"><span class="type">string</span> `$bytes`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$metadata`<span class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">storeFile</span> ( <span
class="methodparam"><span class="type">string\|resource</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">array</span> `$metadata`<span class="initializer"> =
array()</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">storeUpload</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$metadata`</span> \] )

}

参见
----

-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/core/gridfs/" class="link external">» GridFS</a>
-   LightCube Solutions blog post on
    <a href="http://www.lightcubesolutions.com/blog/?p=209" class="link external">» saving user uploads</a>
-   LightCube Solutions blog post on
    <a href="http://www.lightcubesolutions.com/blog/?p=228" class="link external">» adding metadata to files</a>

MongoGridFS::\_\_construct
==========================

Creates new file collections

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoGridFS::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoDB</span> `$db`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$prefix`<span class="initializer"> = "fs"</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$chunks`<span
class="initializer"> = "fs"</span></span> \]\] )

Files as stored across two collections, the first containing file meta
information, the second containing chunks of the actual file. By
default, fs.files and fs.chunks are the collection names used.

Use one argument to specify a prefix other than "fs":

``` description
$fs = new MongoGridFS($db, "myfiles");
```

uses myfiles.files and myfiles.chunks collections.

### 参数

`db`  
Database.

`files`  
Optional collection name prefix.

MongoGridFS::delete
===================

Remove a file and its chunks from the database

### 说明

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span
class="methodname">MongoGridFS::delete</span> ( <span
class="methodparam"><span class="type">mixed</span> `$id`</span> )

> **Note**:
>
> <span class="methodname">MongoGridFS::delete</span> is a convenience
> method for calling <span class="methodname">MongoGridFS::remove</span>
> with specific `criteria` and default `options` parameters.

### 参数

`id`  
*\_id* of the file to remove.

### 返回值

Returns an array containing the status of the removal (with respect to
the *files* collection) if a
<a href="/book/mongo.html#Write%20Concerns" class="link">write concern</a>
is applied. Otherwise, returns **`TRUE`**.

Fields in the status array are described in the documentation for <span
class="function">MongoCollection::insert</span>.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

MongoGridFS::drop
=================

Drops the files and chunks collections

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoGridFS::drop</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The database response.

MongoGridFS::find
=================

Queries for files

### 说明

<span class="modifier">public</span> <span
class="type">MongoGridFSCursor</span> <span
class="methodname">MongoGridFS::find</span> (\[ <span
class="methodparam"><span class="type">array</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$fields`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`query`  
The query.

`fields`  
Fields to return.

### 返回值

A <span class="classname">MongoGridFSCursor</span>.

MongoGridFS::findOne
====================

Returns a single file matching the criteria

### 说明

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">MongoGridFS::findOne</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$query`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$fields`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`query`  
The filename or criteria for which to search.

### 返回值

Returns a <span class="classname">MongoGridFSFile</span> or **`NULL`**.

### 范例

**示例 \#1 <span class="methodname">MongoGridFS::findOne</span>
example**

Example demonstrating how to find a single file from the MongoGridFS.

``` php
<?php

$downloads = $mongo->my_db->getGridFS('downloads');

$downloads->storeFile('filename.tgz');

$download = $downloads->findOne('filename.tgz'); // instance of MongoGridFSFile

print_r($download);
?>
```

See <span class="classname">MongoGridFSFile</span> for more information
about how to work with files.

以上例程的输出类似于：

    MongoGridFSFile Object
    (
        [file] => Array
            (
                [_id] => MongoId Object
                    (
                    )

                [filename] => filename.tgz
                [uploadDate] => MongoDate Object
                    (
                        [sec] => 1274288014
                        [usec] => 467000
                    )

                [chunkSize] => 262144
                [md5] => d41d8cd98f00b204e9800998ecf8427e
            )

        [gridfs:protected] => MongoGridFS Object
            (
                [chunks] => MongoCollection Object
                    (
                    )

                [filesName:protected] => downloads.files
                [chunksName:protected] => downloads.chunks
            )

    )

MongoGridFS::get
================

Retrieve a file from the database

### 说明

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">MongoGridFS::get</span> ( <span
class="methodparam"><span class="type">mixed</span> `$id`</span> )

### 参数

`id`  
*\_id* of the file to find.

### 返回值

Returns the file, if found, or **`NULL`**.

MongoGridFS::put
================

Stores a file in the database

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoGridFS::put</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$metadata`<span class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

> **Note**:
>
> <span class="methodname">MongoGridFS::put</span> is an alias of <span
> class="methodname">MongoGridFS::storeFile</span>.

### 参数

`filename`  
Name of the file to store.

`metadata`  
Other metadata fields to include in the file document.

> **Note**:
>
> These fields may also overwrite those that would be created
> automatically by the driver, as described in the MongoDB core
> documentation for the
> <a href="https://docs.mongodb.com/manual/core/gridfs/#the-files-collection" class="link external">» files collection</a>.
> Some practical use cases for this behavior would be to specify a
> custom *chunkSize* or *\_id* for the file.

`options`  
An array of options for the insert operations executed against the
*chunks* and *files* collections. See <span
class="function">MongoCollection::insert</span> for documentation on
these these options.

### 返回值

Returns the *\_id* of the saved file document. This will be a generated
<span class="classname">MongoId</span> unless an *\_id* was explicitly
specified in the `metadata` parameter.

### 错误／异常

Throws <span class="classname">MongoGridFSException</span> if there is
an error reading `filename` or inserting into the *chunks* or *files*
collections.

### 参见

-   <span class="function">MongoGridFS::storeBytes</span>
-   <span class="function">MongoGridFS::storeFile</span>
-   <span class="function">MongoGridFS::storeUpload</span>
-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/core/gridfs/" class="link external">» GridFS</a>

MongoGridFS::remove
===================

Remove files and their chunks from the database

### 说明

<span class="modifier">public</span> <span
class="type">bool\|array</span> <span
class="methodname">MongoGridFS::remove</span> (\[ <span
class="methodparam"><span class="type">array</span> `$criteria`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`criteria`  
The filename or criteria for which to search.

`options`  
An array of options for the remove operations executed against the
*chunks* and *files* collections. See <span
class="function">MongoCollection::remove</span> for documentation on
these options.

### 返回值

Returns an array containing the status of the removal (with respect to
the *files* collection) if the *"w"* option is set. Otherwise, returns
**`TRUE`**.

Fields in the status array are described in the documentation for <span
class="function">MongoCollection::insert</span>.

### 错误／异常

Throws <span class="classname">MongoCursorException</span> if the *"w"*
option is set and the write fails.

Throws <span class="classname">MongoCursorTimeoutException</span> if the
*"w"* option is set to a value greater than one and the operation takes
longer than `MongoCursor::$timeout` milliseconds to complete. This does
not kill the operation on the server, it is a client-side timeout. The
operation in `MongoCollection::$wtimeout` is milliseconds.

MongoGridFS::storeBytes
=======================

Stores a string of bytes in the database

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoGridFS::storeBytes</span> ( <span
class="methodparam"><span class="type">string</span> `$bytes`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$metadata`<span class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \]\] )

### 参数

`bytes`  
String of bytes to store.

`metadata`  
Other metadata fields to include in the file document.

> **Note**:
>
> These fields may also overwrite those that would be created
> automatically by the driver, as described in the MongoDB core
> documentation for the
> <a href="https://docs.mongodb.com/manual/core/gridfs/#the-files-collection" class="link external">» files collection</a>.
> Some practical use cases for this behavior would be to specify a
> custom *chunkSize* or *\_id* for the file.

`options`  
An array of options for the insert operations executed against the
*chunks* and *files* collections. See <span
class="function">MongoCollection::insert</span> for documentation on
these these options.

### 返回值

Returns the *\_id* of the saved file document. This will be a generated
<span class="classname">MongoId</span> unless an *\_id* was explicitly
specified in the `metadata` parameter.

### 错误／异常

Throws <span class="classname">MongoGridFSException</span> if there is
an error inserting into the *chunks* or *files* collections.

### 范例

**示例 \#1 <span class="function">MongoGridFS::storeBytes</span> with
additional metadata**

``` php
<?php
$m = new MongoClient();
$gridfs = $m->selectDB('test')->getGridFS();

$bytes = 'abcdefghijklmnopqrstuvwxyz';
$id = $gridfs->storeBytes($bytes, array('_id' => 'alphabet'));
$gridfsFile = $gridfs->get($id);

var_dump($gridfsFile->file);
?>
```

以上例程的输出类似于：

    array(7) {
      ["_id"]=>
      string(8) "alphabet"
      ["uploadDate"]=>
      object(MongoDate)#7 (0) {
      }
      ["length"]=>
      int(26)
      ["chunkSize"]=>
      int(262144)
      ["md5"]=>
      string(32) "c3fcd3d76192e4007dfb496cca67e13b"
    }

### 参见

-   <span class="function">MongoGridFS::put</span>
-   <span class="function">MongoGridFS::storeFile</span>
-   <span class="function">MongoGridFS::storeUpload</span>
-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/core/gridfs/" class="link external">» GridFS</a>

MongoGridFS::storeFile
======================

Stores a file in the database

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoGridFS::storeFile</span> ( <span
class="methodparam"><span class="type">string\|resource</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">array</span> `$metadata`<span class="initializer"> =
array()</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \]\] )

### 参数

`filename`  
Name of the file or a readable stream to store.

`metadata`  
Other metadata fields to include in the file document.

> **Note**:
>
> These fields may also overwrite those that would be created
> automatically by the driver, as described in the MongoDB core
> documentation for the
> <a href="https://docs.mongodb.com/manual/core/gridfs/#the-files-collection" class="link external">» files collection</a>.
> Some practical use cases for this behavior would be to specify a
> custom *chunkSize* or *\_id* for the file.

`options`  
An array of options for the insert operations executed against the
*chunks* and *files* collections. See <span
class="function">MongoCollection::insert</span> for documentation on
these these options.

### 返回值

Returns the *\_id* of the saved file document. This will be a generated
<span class="classname">MongoId</span> unless an *\_id* was explicitly
specified in the `metadata` parameter.

### 错误／异常

Throws <span class="classname">MongoGridFSException</span> if there is
an error reading `filename` or inserting into the *chunks* or *files*
collections.

### 范例

**示例 \#1 <span class="function">MongoGridFS::storeFile</span> with
additional metadata**

``` php
<?php
$m = new MongoClient();
$gridfs = $m->selectDB('test')->getGridFS();

$id = $gridfs->storeFile('example.txt', array('contentType' => 'plain/text'));
$gridfsFile = $gridfs->get($id);

var_dump($gridfsFile->file);
?>
```

以上例程的输出类似于：

    array(7) {
      ["_id"]=>
      object(MongoId)#6 (0) {
      }
      ["contentType"]=>
      string(10) "plain/text"
      ["filename"]=>
      string(11) "example.txt"
      ["uploadDate"]=>
      object(MongoDate)#7 (0) {
      }
      ["length"]=>
      int(26)
      ["chunkSize"]=>
      int(262144)
      ["md5"]=>
      string(32) "c3fcd3d76192e4007dfb496cca67e13b"
    }

### 参见

-   <span class="function">MongoGridFS::put</span>
-   <span class="function">MongoGridFS::storeBytes</span>
-   <span class="function">MongoGridFS::storeUpload</span>
-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/core/gridfs/" class="link external">» GridFS</a>

MongoGridFS::storeUpload
========================

Stores an uploaded file in the database

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoGridFS::storeUpload</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$metadata`</span> \] )

### 参数

`name`  
The name of the uploaded file(s) to store. This should correspond to the
file field's *name* attribute in the HTML form.

`metadata`  
Other metadata fields to include in the file document.

> **Note**:
>
> These fields may also overwrite those that would be created
> automatically by the driver, as described in the MongoDB core
> documentation for the
> <a href="https://docs.mongodb.com/manual/core/gridfs/#the-files-collection" class="link external">» files collection</a>.
> Some practical use cases for this behavior would be to specify a
> custom *chunkSize* or *\_id* for the file.

> **Note**:
>
> The *filename* field will be populated with the client's filename
> (e.g. *$\_FILES\['foo'\]\['name'\]*).

### 返回值

Returns the *\_id* of the saved file document. This will be a generated
<span class="classname">MongoId</span> unless an *\_id* was explicitly
specified in the `metadata` parameter.

> **Note**:
>
> If
> <a href="/features/file-upload/multiple.html" class="link">multiple files are uploaded using the same field name</a>,
> this method will not return anything; however, the files themselves
> will still be processed.

### 错误／异常

Throws <span class="classname">MongoGridFSException</span> if there is
an error reading the uploaded file(s) or inserting into the *chunks* or
*files* collections.

### 更新日志

| 版本  | 说明                                                                                                                              |
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| 1.2.5 | Changed second parameter to an array of metadata. Pre-1.2.5, the second parameter was an optional string overriding the filename. |

### 范例

**示例 \#1 <span class="function">MongoGridFS::storeUpload</span> HTML
form example**

Suppose you have the following HTML form:

``` html
<form method="POST" enctype="multipart/form-data">
    <label for="username">Username:</label>
    <input type="text" name="username" id="username" />

    <label for="pic">Please upload a profile picture:</label>
    <input type="file" name="pic" id="pic" />

    <input type="submit" />
</form>
```

If you wanted to store the uploaded image in MongoDB, you could do the
following in the script handling the form submission:

``` php
<?php
$m = new MongoClient();
$gridfs = $m->selectDB('test')->getGridFS();

$gridfs->storeUpload('pic', array('username' => $_POST['username']));
?>
```

### 参见

-   <span class="function">MongoGridFS::put</span>
-   <span class="function">MongoGridFS::storeBytes</span>
-   <span class="function">MongoGridFS::storeFile</span>
-   MongoDB core docs on
    <a href="https://docs.mongodb.com/manual/core/gridfs/" class="link external">» GridFS</a>

简介
----

A database file object.

类摘要
------

**MongoGridFSFile**

<span class="ooclass"> class **MongoGridFSFile** </span> {

/\* Fields \*/

<span class="modifier">public</span> <span class="type">array</span>
`$file` <span class="initializer"> = **`NULL`**</span> ;

<span class="modifier">protected</span> <span
class="type">MongoGridFS</span> `$gridfs` <span class="initializer"> =
**`NULL`**</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">MongoGridfsFile::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoGridFS</span>
`$gridfs`</span> , <span class="methodparam"><span
class="type">array</span> `$file`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getBytes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getFilename</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">getResource</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">write</span> (\[ <span class="methodparam"><span
class="type">string</span> `$filename`<span class="initializer"> =
**`NULL`**</span></span> \] )

}

MongoGridfsFile::\_\_construct
==============================

Create a new GridFS file

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoGridfsFile::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoGridFS</span>
`$gridfs`</span> , <span class="methodparam"><span
class="type">array</span> `$file`</span> )

### 参数

`gridfs`  
The parent MongoGridFS instance.

`file`  
A file from the database.

### 返回值

Returns a new MongoGridFSFile.

MongoGridFSFile::getBytes
=========================

Returns this file's contents as a string of bytes

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoGridFSFile::getBytes</span> ( <span
class="methodparam">void</span> )

Warning: this will load the file into memory. If the file is bigger than
your memory, this will cause problems!

### 参数

此函数没有参数。

### 返回值

Returns a string of the bytes in the file.

### 范例

**示例 \#1 <span class="methodname">MongoGridFSFile::getBytes</span>
example**

``` php
<?php

$images = $db->my_db->getGridFS('images');

$image = $images->findOne('jwage.png');

header('Content-type: image/png;');
echo $image->getBytes();
?>
```

MongoGridFSFile::getFilename
============================

Returns this file's filename

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoGridFSFile::getFilename</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the filename.

MongoGridFSFile::getResource
============================

Returns a resource that can be used to read the stored file

### 说明

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">MongoGridFSFile::getResource</span> ( <span
class="methodparam">void</span> )

This method returns a stream resource that can be used with all file
functions in PHP that deal with reading files. The contents of the file
are pulled out of MongoDB on the fly, so that the whole file does not
have to be loaded into memory first.

At most two GridFSFile chunks will be loaded in memory.

### 参数

此函数没有参数。

### 返回值

Returns a resource that can be used to read the file with

### 范例

**示例 \#1 <span class="methodname">MongoGridFSFile::getResource</span>
example**

``` php
<?php
$m = new Mongo;
$images = $m->my_db->getGridFS('images');

$image = $images->findOne('mongo.png');

header('Content-type: image/png;');
$stream = $image->getResource();

while (!feof($stream)) {
    echo fread($stream, 8192);
}
?>
```

MongoGridFSFile::getSize
========================

Returns this file's size

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoGridFSFile::getSize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns this file's size

MongoGridFSFile::write
======================

Writes this file to the filesystem

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoGridFSFile::write</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`<span
class="initializer"> = **`NULL`**</span></span> \] )

### 参数

`filename`  
The location to which to write the file. If none is given, the stored
filename will be used.

### 返回值

Returns the number of bytes written.

### 范例

**示例 \#1 <span class="methodname">MongoGridFSFile::write</span>
example**

``` php
<?php

$images = $db->my_db->getGridFS('images');

$image = $images->findOne('jwage.png');
$image->write('/path/to/write/jwage.png');
?>
```

简介
----

Cursor for database file results.

类摘要
------

**MongoGridFSCursor**

<span class="ooclass"> <span class="modifier">extends</span> class
**MongoCursor** </span> {

/\* Fields \*/

<span class="modifier">protected</span> <span
class="type">MongoGridFS</span> `$gridfs` <span class="initializer"> =
**`NULL`**</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoGridFS</span>
`$gridfs`</span> , <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span> `$ns`</span> ,
<span class="methodparam"><span class="type">array</span>
`$query`</span> , <span class="methodparam"><span
class="type">array</span> `$fields`</span> )

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">getNext</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

}

MongoGridFSCursor::\_\_construct
================================

Create a new cursor

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoGridFSCursor::\_\_construct</span> ( <span
class="methodparam"><span class="type">MongoGridFS</span>
`$gridfs`</span> , <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span> `$ns`</span> ,
<span class="methodparam"><span class="type">array</span>
`$query`</span> , <span class="methodparam"><span
class="type">array</span> `$fields`</span> )

### 参数

`gridfs`  
Related GridFS collection.

`connection`  
Database connection.

`ns`  
Full name of database and collection.

`query`  
Database query.

`fields`  
Fields to return.

### 返回值

Returns the new cursor.

MongoGridFSCursor::current
==========================

Returns the current file

### 说明

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">MongoGridFSCursor::current</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The current file.

MongoGridFSCursor::getNext
==========================

Return the next file to which this cursor points, and advance the cursor

### 说明

<span class="modifier">public</span> <span
class="type">MongoGridFSFile</span> <span
class="methodname">MongoGridFSCursor::getNext</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the next file.

MongoGridFSCursor::key
======================

Returns the current result's filename

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoGridFSCursor::key</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The current result's \_id as a string.

### 更新日志

| 版本  | 说明                                                                                                                     |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | The document's *\_id* is returned as a string value, since the key should be unique. Pre-1.3.0, *filename* was returned. |

Miscellaneous
=============

**目录**

-   [MongoLog](/book/mongo.html#MongoLog) — The MongoLog class
    -   [MongoLog::getCallback](/book/mongo.html#MongoLog::getCallback)
        — Gets the previously set callback function
    -   [MongoLog::getLevel](/book/mongo.html#MongoLog::getLevel) — Gets
        the level(s) currently being logged
    -   [MongoLog::getModule](/book/mongo.html#MongoLog::getModule) —
        Gets the module(s) currently being logged
    -   [MongoLog::setCallback](/book/mongo.html#MongoLog::setCallback)
        — Sets a callback function to be invoked for events
    -   [MongoLog::setLevel](/book/mongo.html#MongoLog::setLevel) — Sets
        the level(s) to be logged
    -   [MongoLog::setModule](/book/mongo.html#MongoLog::setModule) —
        Sets the module(s) to be logged
-   [MongoPool](/book/mongo.html#MongoPool) — The MongoPool class
    -   [MongoPool::getSize](/book/mongo.html#MongoPool::getSize) — Get
        pool size for connection pools
    -   [MongoPool::info](/book/mongo.html#MongoPool::info) — Returns
        information about all connection pools
    -   [MongoPool::setSize](/book/mongo.html#MongoPool::setSize) — Set
        the size for future connection pools
-   [Mongo](/book/mongo.html#Mongo) — The Mongo class \[deprecated\]
    -   [Mongo::connectUtil](/book/mongo.html#Mongo::connectUtil) —
        Connects with a database server
    -   [Mongo::\_\_construct](/book/mongo.html#Mongo::__construct) —
        The \_\_construct purpose
    -   [Mongo::getPoolSize](/book/mongo.html#Mongo::getPoolSize) — Get
        pool size for connection pools
    -   [Mongo::getSlave](/book/mongo.html#Mongo::getSlave) — Returns
        the address being used by this for slaveOkay reads
    -   [Mongo::getSlaveOkay](/book/mongo.html#Mongo::getSlaveOkay) —
        Get slaveOkay setting for this connection
    -   [Mongo::poolDebug](/book/mongo.html#Mongo::poolDebug) — Returns
        information about all connection pools
    -   [Mongo::setPoolSize](/book/mongo.html#Mongo::setPoolSize) — Set
        the size for future connection pools
    -   [Mongo::setSlaveOkay](/book/mongo.html#Mongo::setSlaveOkay) —
        Change slaveOkay setting for this connection
    -   [Mongo::switchSlave](/book/mongo.html#Mongo::switchSlave) —
        Choose a new secondary for slaveOkay reads

简介
----

Logging can be used to get detailed information about what the driver is
doing. Logging is disabled by default, but this class allows you to
activate specific levels of logging for various parts of the driver.
Some examples:

``` php
<?php

// print every log message possible
MongoLog::setLevel(MongoLog::ALL); // all log levels
MongoLog::setModule(MongoLog::ALL); // all parts of the driver

// print significant events about replica set failover
MongoLog::setLevel(MongoLog::INFO);
MongoLog::setModule(MongoLog::RS);

// print info- and diagnostic-level events for replica sets and connections
MongoLog::setLevel(MongoLog::INFO|MongoLog::FINE);
MongoLog::setModule(MongoLog::RS|MongoLog::CON);

?>
```

> **Note**:
>
> By default, MongoLog emits all log messages as PHP notices. Depending
> on the SAPI you use, messages may be sent to *stderr* (for CLI) or the
> web server's error log. If, after configuring MongoLog, log messages
> are not appearing as expected, ensure that the **`E_NOTICE`** bit is
> included in
> <a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
> and that
> <a href="/errorfunc/setup.html#" class="link">display_errors</a> is
> on.

类摘要
------

**MongoLog**

<span class="ooclass"> class **MongoLog** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::ALL` <span class="initializer"> = 31</span> ;

level constants {

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::WARNING` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::INFO` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::FINE` <span class="initializer"> = 4</span> ;

module constants {

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::RS` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::POOL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::CON` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::IO` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::SERVER` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`MongoLog::PARSE` <span class="initializer"> = 16</span> ;

/\* Fields \*/

<span class="modifier">private</span> <span
class="modifier">static</span> <span class="type">int</span> `$callback`
;

<span class="modifier">private</span> <span
class="modifier">static</span> <span class="type">int</span> `$level` ;

<span class="modifier">private</span> <span
class="modifier">static</span> <span class="type">int</span> `$module` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">callable</span> <span
class="methodname">getCallback</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getLevel</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getModule</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">setCallback</span> ( <span class="methodparam"><span
class="type">callable</span> `$log_function`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">setLevel</span> ( <span class="methodparam"><span
class="type">int</span> `$level`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">setModule</span> ( <span class="methodparam"><span
class="type">int</span> `$module`</span> )

}

预定义常量
----------

MongoLog Constants
------------------

These constants can be used by both <span
class="function">MongoLog::setLevel</span> and <span
class="function">MongoLog::setModule</span>.

**`MongoLog::NONE`**  
<span class="simpara"> Log nothing. </span>

**`MongoLog::ALL`**  
<span class="simpara"> Log everything. </span>

MongoLog Level Constants
------------------------

These constants can be used by <span
class="function">MongoLog::setLevel</span>.

**`MongoLog::WARNING`**  
<span class="simpara"> Log events that are somewhat exceptional, but not
quite worthy of an actual exception (e.g. recoverable connection
errors). </span>

**`MongoLog::INFO`**  
<span class="simpara"> Log events that may be of interest to
administrators, but are not particularly noteworthy (e.g. option
parsing, authentication steps). </span>

**`MongoLog::FINE`**  
<span class="simpara"> Log most events that the driver performs (e.g.
server selection, socket communication). Depending on the module being
logged, this can be extremely noisy and is primarily useful for
debugging. </span>

MongoLog Module Constants
-------------------------

These constants can be used by <span
class="function">MongoLog::setModule</span>.

**`MongoLog::CON`**  
<span class="simpara"> Log connection activity. Creating new
connections, authentication, pinging, timeouts, etc. </span>

**`MongoLog::IO`**  
<span class="simpara"> Log traffic to/from the database. Unless your
program is trivial, this will create an enormous number of log messages.
</span>

**`MongoLog::PARSE`**  
<span class="simpara"> Log parsing of the connection string and options
when constructing <span class="classname">MongoClient</span>. </span>

**`MongoLog::POOL`**  
<span class="simpara"> Previously used to log connection pool activity.
This option is now a deprecated alias of **`MongoLog::RS`**. </span>

**`MongoLog::RS`**  
<span class="simpara"> Log replica set activity. Failovers, read
preference selection, etc. </span>

**`MongoLog::SERVER`**  
<span class="simpara"> Previously used to log server status changes.
This option is deprecated in favor of **`MongoLog::RS`**. </span>

更新日志
--------

| 版本  | 说明                                                                                      |
|-------|-------------------------------------------------------------------------------------------|
| 1.3.0 | Added **`MongoLog::CON`** and deprecated **`MongoLog::POOL`** and **`MongoLog::SERVER`**. |

MongoLog::getCallback
=====================

Gets the previously set callback function

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">callable</span> <span
class="methodname">MongoLog::getCallback</span> ( <span
class="methodparam">void</span> )

Retrieves the callback function.

### 参数

此函数没有参数。

### 返回值

Returns the callback function, or **`FALSE`** if not set yet.

### 注释

**Caution**

This function is only available with PHP 5.3.0 and later.

MongoLog::getLevel
==================

Gets the level(s) currently being logged

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">MongoLog::getLevel</span> ( <span
class="methodparam">void</span> )

This function can be used to see which log levels are currently enabled.
The returned integer may be compared with the
<a href="/book/mongo.html#MongoLog%20Level%20Constants" class="link">MongoLog level constants</a>
using bitwise operators to check for specific log levels.

``` php
<?php

if (MongoLog::getLevel() & MongoLog::FINE) {
    echo "lots of logs\n";
}

if (MongoLog::getLevel() ^ MongoLog::NONE) {
    echo "logging, at least a little\n";
}

if (MongoLog::getLevel() == MongoLog::ALL) {
    echo "logging at the highest levels\n";
}

?>
```

### 参数

此函数没有参数。

### 返回值

Returns the level(s) currently being logged.

MongoLog::getModule
===================

Gets the module(s) currently being logged

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">MongoLog::getModule</span> ( <span
class="methodparam">void</span> )

This function can be used to see which driver modules are currently
being logged. The returned integer may be compared with the
<a href="/book/mongo.html#MongoLog%20Module%20Constants" class="link">MongoLog module constants</a>
using bitwise operators to check if specific modules are being logged.

``` php
<?php

if (MongoLog::getModule() & MongoLog::RS) {
    echo "logging replica sets\n";
}

if (MongoLog::getModule() ^ MongoLog::NONE) {
    echo "logging something\n";
}

if ((MongoLog::getModule() & MongoLog::IO) == 0) {
    echo "not logging io\n";
}

?>
```

### 参数

此函数没有参数。

### 返回值

Returns the module(s) currently being logged.

MongoLog::setCallback
=====================

Sets a callback function to be invoked for events

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">MongoLog::setCallback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$log_function`</span> )

This function will set a callback function to be invoked for events in
lieu of emitting of PHP notice.

### 参数

`log_function`  
The callback function to be invoked on events. It should have the
following prototype:

<span class="methodname"><span
class="replaceable">log\_function</span></span> ( <span
class="methodparam"><span class="type">int</span> `$module`</span> ,
<span class="methodparam"><span class="type">int</span> `$level`</span>
, <span class="methodparam"><span class="type">string</span>
`$message`</span> )

`module`  
<span class="simpara"> One of the
<a href="/book/mongo.html#MongoLog%20Module%20Constants" class="link">MongoLog module constants</a>.
</span>

`level`  
<span class="simpara"> One of the
<a href="/book/mongo.html#MongoLog%20Level%20Constants" class="link">MongoLog level constants</a>.
</span>

`message`  
<span class="simpara"> The log message itself. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="methodname">MongoLog::setCallback</span>
example**

``` php
<?php

function module2string($module)
{
    switch ($module) {
        case MongoLog::RS: return "REPLSET";
        case MongoLog::CON: return "CON";
        case MongoLog::IO: return "IO";
        case MongoLog::SERVER: return "SERVER";
        case MongoLog::PARSE: return "PARSE";
        default: return "UNKNOWN";
    }
}

function level2string($level)
{
    switch ($level) {
        case MongoLog::WARNING: return "WARN";
        case MongoLog::INFO: return "INFO";
        case MongoLog::FINE: return "FINE";
        default: return "UNKNOWN";
    }
}

function callback($module, $level, $message)
{
    echo date("Y-m-d H:i:s - ");
    printf("%s (%s): %s\n", module2string($module), level2string($level), $message);
}

MongoLog::setLevel(MongoLog::ALL);
MongoLog::setModule(MongoLog::ALL);

// We specify the function name here, but any callable (e.g. anonymous function) will work
MongoLog::setCallback("callback");

new MongoClient();
?>
```

以上例程的输出类似于：

    2013-07-09 09:41:42 - PARSE (INFO): Parsing localhost:27017
    2013-07-09 09:41:42 - PARSE (INFO): - Found node: localhost:27017
    2013-07-09 09:41:42 - PARSE (INFO): - Connection type: STANDALONE
    2013-07-09 09:41:42 - CON (INFO): mongo_get_read_write_connection: finding a STANDALONE connection
    2013-07-09 09:41:42 - CON (INFO): connection_create: creating new connection for localhost:27017
    2013-07-09 09:41:42 - CON (INFO): stream_connect: Not establishing SSL for localhost:27017
    2013-07-09 09:41:42 - CON (INFO): get_server_flags: start
    2013-07-09 09:41:42 - CON (FINE): send_packet: read from header: 36
    2013-07-09 09:41:42 - CON (FINE): send_packet: data_size: 95
    2013-07-09 09:41:42 - CON (FINE): get_server_flags: setting maxBsonObjectSize to 16777216
    2013-07-09 09:41:42 - CON (FINE): get_server_flags: setting maxMessageSizeBytes to 48000000
    2013-07-09 09:41:42 - CON (INFO): is_ping: pinging localhost:27017;-;.;1543
    2013-07-09 09:41:42 - CON (FINE): send_packet: read from header: 36
    2013-07-09 09:41:42 - CON (FINE): send_packet: data_size: 17
    2013-07-09 09:41:42 - CON (INFO): is_ping: last pinged at 1373359302; time: 0ms
    2013-07-09 09:41:42 - REPLSET (FINE): finding candidate servers
    2013-07-09 09:41:42 - REPLSET (FINE): - all servers
    2013-07-09 09:41:42 - REPLSET (FINE): filter_connections: adding connections:
    2013-07-09 09:41:42 - REPLSET (FINE): - connection: type: STANDALONE, socket: 42, ping: 0, hash: localhost:27017;-;.;1543
    2013-07-09 09:41:42 - REPLSET (FINE): filter_connections: done
    2013-07-09 09:41:42 - REPLSET (FINE): limiting by seeded/discovered servers
    2013-07-09 09:41:42 - REPLSET (FINE): - connection: type: STANDALONE, socket: 42, ping: 0, hash: localhost:27017;-;.;1543
    2013-07-09 09:41:42 - REPLSET (FINE): limiting by seeded/discovered servers: done
    2013-07-09 09:41:42 - REPLSET (FINE): limiting by credentials
    2013-07-09 09:41:42 - REPLSET (FINE): - connection: type: STANDALONE, socket: 42, ping: 0, hash: localhost:27017;-;.;1543
    2013-07-09 09:41:42 - REPLSET (FINE): limiting by credentials: done
    2013-07-09 09:41:42 - REPLSET (FINE): sorting servers by priority and ping time
    2013-07-09 09:41:42 - REPLSET (FINE): - connection: type: STANDALONE, socket: 42, ping: 0, hash: localhost:27017;-;.;1543
    2013-07-09 09:41:42 - REPLSET (FINE): sorting servers: done
    2013-07-09 09:41:42 - REPLSET (FINE): selecting near servers
    2013-07-09 09:41:42 - REPLSET (FINE): selecting near servers: nearest is 0ms
    2013-07-09 09:41:42 - REPLSET (FINE): - connection: type: STANDALONE, socket: 42, ping: 0, hash: localhost:27017;-;.;1543
    2013-07-09 09:41:42 - REPLSET (FINE): selecting near server: done
    2013-07-09 09:41:42 - REPLSET (INFO): pick server: random element 0
    2013-07-09 09:41:42 - REPLSET (INFO): - connection: type: STANDALONE, socket: 42, ping: 0, hash: localhost:27017;-;.;1543

### 注释

**Caution**

This function is only available with PHP 5.3.0 and later.

MongoLog::setLevel
==================

Sets the level(s) to be logged

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">MongoLog::setLevel</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

This function can be used to control logging verbosity and the types of
activities that should be logged. The
<a href="/book/mongo.html#MongoLog%20Level%20Constants" class="link">MongoLog level constants</a>
may be used with bitwise operators to specify multiple levels.

``` php
<?php

// first, specify a logging module
MongoLog::setModule(MongoLog::CON);

// log messages for every level
MongoLog::setLevel(MongoLog::ALL);

// log warning and info messages only
MongoLog::setLevel(MongoLog::WARNING|MongoLog::INFO);

// log everything except fine activity
MongoLog::setLevel(MongoLog::ALL & (~MongoLog::FINE));

?>
```

Note that you must also call <span
class="function">MongoLog::setModule</span> to specify which modules(s)
of the driver should log.

### 参数

`level`  
The level(s) you would like to log.

MongoLog::setModule
===================

Sets the module(s) to be logged

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">MongoLog::setModule</span> ( <span
class="methodparam"><span class="type">int</span> `$module`</span> )

This function can be used to set which driver modules should be logged.
The
<a href="/book/mongo.html#MongoLog%20Module%20Constants" class="link">MongoLog module constants</a>
may be used with bitwise operators to specify multiple modules.

``` php
<?php

// first, specify a logging level
MongoLog::setLevel(MongoLog::ALL);

// log replica set activity
MongoLog::setModule(MongoLog::RS);

// log replica sets and connection activity
MongoLog::setModule(MongoLog::RS|MongoLog::CON);

// log everything except IO activity
MongoLog::setModule(MongoLog::ALL & (~MongoLog::IO));

?>
```

Note that you must also call <span
class="function">MongoLog::setLevel</span> to enable logging.

### 参数

`module`  
The module(s) you would like to log.

简介
----

**Warning**

The current (1.3.0+) releases of the driver no longer implements
pooling. This class and its methods are therefore deprecated and should
not be used.

类摘要
------

**MongoPool**

<span class="ooclass"> class **MongoPool** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">info</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setSize</span> ( <span class="methodparam"><span
class="type">int</span> `$size`</span> )

}

更新日志
--------

| 版本   | 说明                                                                                                                                                                                                     |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.0  | This functionality has been removed and no longer does anything other than emit deprecation warnings. This class is only kept around for backwards compatibility and will be removed in the near future. |
| 1.2.11 | Emits **`E_DEPRECATED`** when used.                                                                                                                                                                      |

MongoPool::getSize
==================

Get pool size for connection pools

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">MongoPool::getSize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the current pool size.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 范例

**示例 \#1 Changing pool size**

This returns the default pool size, sets a new pool size, then prints
the new pool size and the pool debugging information. Note that changing
the pool size only affects new connection pools, it does not change old
ones.

``` php
<?php

$connection = new Mongo("host1");

// pool size is -1
echo "pool size is: ".MongoPool::getSize()."\n";

echo "setting pool size to 200\n";

MongoPool::setSize(200);

// pool size is 200
echo "pool size is: ".MongoPool::getSize()."\n";

$conn2 = new Mongo("host2");

// remaining for host1 is -2
// remaining for host2 is 199
var_dump(Mongo::poolDebug());

?>
```

### 参见

-   <span class="function">MongoPool::setSize</span>
-   <span class="function">MongoPool::info</span>
-   The
    <a href="/book/mongo.html#链接服务器" class="link">connection</a>
    documentation.

MongoPool::info
===============

Returns information about all connection pools

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoPool::info</span> ( <span
class="methodparam">void</span> )

Returns an array of information about all connection pools.

### 参数

此函数没有参数。

### 返回值

Each connection pool has an identifier, which starts with the host. For
each pool, this function shows the following fields:

`in use`  
The number of connections currently being used by <span
class="classname">Mongo</span> instances.

`in pool`  
The number of connections currently in the pool (not being used).

`remaining`  
The number of connections that could be created by this pool. For
example, suppose a pool had 5 connections remaining and 3 connections in
the pool. We could create 8 new instances of <span
class="classname">MongoClient</span> before we exhausted this pool
(assuming no instances of <span class="classname">MongoClient</span>
went out of scope, returning their connections to the pool).

A negative number means that this pool will spawn unlimited connections.

Before a pool is created, you can change the max number of connections
by calling <span class="function">Mongo::setPoolSize</span>. Once a pool
is showing up in the output of this function, its size cannot be
changed.

`total`  
The total number of connections allowed for this pool. This should be
greater than or equal to "in use" + "in pool" (or -1).

`timeout`  
The socket timeout for connections in this pool. This is how long
connections in this pool will attempt to connect to a server before
giving up.

`waiting`  
If you have capped the pool size, workers requesting connections from
the pool may block until other workers return their connections. This
field shows how many milliseconds workers have blocked for connections
to be released. If this number keeps increasing, you may want to use
<span class="function">MongoPool::setSize</span> to add more connections
to your pool.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

MongoPool::setSize
==================

Set the size for future connection pools

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">MongoPool::setSize</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> )

Sets the max number of connections new pools will be able to create.

### 参数

`size`  
The max number of connections future pools will be able to create.
Negative numbers mean that the pool will spawn an infinite number of
connections.

### 返回值

Returns the former value of pool size.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 范例

**示例 \#1 <span class="function">Mongo::setPoolSize</span> example**

If you set the pool size to *n* and then create *n* connections,
attempting to create an *n+1*st connection will throw a <span
class="classname">MongoConnectionException</span>.

``` php
<?php

// only allow one connection to a server
MongoPool::setSize(1);

// creates one connection to localhost:27017
$m1 = new Mongo();

// attempt to create a second connection to localhost:27017
// only one connection is allowed, so this will throw an exception
$m2 = new Mongo();

?>
```

以上例程的输出类似于：

    Fatal error: Uncaught exception 'MongoConnectionException' with message 'no more connections in pool' in /path/to/php/script.php:10
    Stack trace:
    #0 /path/to/php/script.php(10): Mongo->__construct()
    #1 {main}
      thrown in /path/to/php/script.php on line 10

### 参见

-   <span class="function">MongoPool::getSize</span>
-   <span class="function">MongoPool::info</span>
-   The
    <a href="/book/mongo.html#链接服务器" class="link">connection</a>
    documentation.

简介
----

A connection between PHP and MongoDB.

This class extends <span class="classname">MongoClient</span> and
provides access to several deprecated methods.

For backwards compatibility, it also defaults the *"w"* option of its
constructor argument to *0*, which does not require write operations to
be acknowledged by the server. See <span
class="function">MongoClient::\_\_construct</span> for more information.

**Warning**

This class has been *DEPRECATED* as of version 1.3.0. Relying on this
feature is highly discouraged. Please use <span
class="classname">MongoClient</span> instead.

类摘要
------

**Mongo**

<span class="ooclass"> class **Mongo** </span> <span class="ooclass">
<span class="modifier">extends</span> **MongoClient** </span> {

/\* 方法 \*/

<span class="modifier">protected</span> <span class="type">bool</span>
<span class="methodname">connectUtil</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getPoolSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSlave</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getSlaveOkay</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">poolDebug</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setPoolSize</span> ( <span class="methodparam"><span
class="type">int</span> `$size`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSlaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$ok`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">switchSlave</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::close</span> (\[ <span
class="methodparam"><span class="type">boolean\|string</span>
`$connection`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::connect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::dropDB</span> ( <span
class="methodparam"><span class="type">mixed</span> `$db`</span> )

<span class="modifier">public</span> <span class="type">MongoDB</span>
<span class="methodname">MongoClient::\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$dbname`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">MongoClient::getConnections</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::getHosts</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::getWriteConcern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::killCursor</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_hash`</span> , <span class="methodparam"><span
class="type">int\|MongoInt64</span> `$id`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoClient::listDBs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">MongoCollection</span> <span
class="methodname">MongoClient::selectCollection</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span class="type">string</span>
`$collection`</span> )

<span class="modifier">public</span> <span class="type">MongoDB</span>
<span class="methodname">MongoClient::selectDB</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::setReadPreference</span> ( <span
class="methodparam"><span class="type">string</span>
`$read_preference`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tags`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">MongoClient::setWriteConcern</span> ( <span
class="methodparam"><span class="type">mixed</span> `$w`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoClient::\_\_toString</span> ( <span
class="methodparam">void</span> )

}

Mongo::connectUtil
==================

Connects with a database server

### 说明

<span class="modifier">protected</span> <span class="type">bool</span>
<span class="methodname">Mongo::connectUtil</span> ( <span
class="methodparam">void</span> )

**Warning**

This is an internal function that you should *never* call yourself.

### 参数

此函数没有参数。

### 返回值

If the connection was successful.

### 错误／异常

Throws <span class="classname">MongoConnectionException</span> if it
fails to connect to the databases.

Mongo::\_\_construct
====================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">Mongo::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$server`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \]\] )

This method overwrites the <span class="classname">MongoClient</span>
constructor and turns off acknowledged writes.

Please see <span class="methodname">MongoClient::\_\_construct</span>
for description of the parameters.

### 返回值

**Warning**

Instanciating this class will emit **`E_DEPRECATED`** warning, and turn
off acknowledged writes.

Please use the <span class="classname">MongoClient</span> instead.

Mongo::getPoolSize
==================

Get pool size for connection pools

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Mongo::getPoolSize</span> ( <span
class="methodparam">void</span> )

**Warning**

This feature has been *DEPRECATED* as of version 1.2.3. Relying on this
feature is highly discouraged. Please use <span
class="function">MongoPool::getSize</span> instead.

### 参数

此函数没有参数。

### 返回值

Returns the current pool size.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 范例

**示例 \#1 Changing pool size**

This returns the default pool size, sets a new pool size, then prints
the new pool size and the pool debugging information. Note that changing
the pool size only affects new connection pools, it does not change old
ones.

``` php
<?php

$connection = new Mongo("host1");

// pool size is -1
echo "pool size is: ".Mongo::getPoolSize()."\n";

echo "setting pool size to 200\n";

Mongo::setPoolSize(200);

// pool size is 200
echo "pool size is: ".Mongo::getPoolSize()."\n";

$conn2 = new Mongo("host2");

// remaining for host1 is -2
// remaining for host2 is 199
var_dump(Mongo::poolDebug());

?>
```

### 参见

-   <span class="function">Mongo::setPoolSize</span>
-   <span class="function">Mongo::poolDebug</span>
-   The
    <a href="/book/mongo.html#链接服务器" class="link">connection</a>
    documentation.

Mongo::getSlave
===============

Returns the address being used by this for slaveOkay reads

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Mongo::getSlave</span> ( <span
class="methodparam">void</span> )

This finds the address of the secondary currently being used for reads.
It is a read-only method: it does not change anything about the internal
state of the object.

When you create a connection to the database, the driver will not
immediately decide on a secondary to use. Thus, after you connect, this
function will return **`NULL`** even if there are secondaries available.
When you first do a query with slaveOkay set, at that point the driver
will choose a secondary for this connection. At that point, this
function will return the chosen secondary.

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

此函数没有参数。

### 返回值

The address of the secondary this connection is using for reads.

This returns **`NULL`** if this is not connected to a replica set or not
yet initialized.

### 错误／异常

Issues **`E_DEPRECATED`** warning

The returned results aren't really useful as the secondary selection
process is done on each query and database command execution.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <span class="function">MongoCursor::info</span>

Mongo::getSlaveOkay
===================

Get slaveOkay setting for this connection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Mongo::getSlaveOkay</span> ( <span
class="methodparam">void</span> )

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

此函数没有参数。

### 返回值

Returns the value of slaveOkay for this instance.

### 错误／异常

Issues **`E_DEPRECATED`** warning

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoClient::getReadPreference</span>

Mongo::poolDebug
================

Returns information about all connection pools

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Mongo::poolDebug</span> ( <span
class="methodparam">void</span> )

**Warning**

This feature has been *DEPRECATED* as of version 1.2.3. Relying on this
feature is highly discouraged. Please use <span
class="function">MongoPool::info</span> instead.

Returns an array of information about all connection pools.

### 参数

此函数没有参数。

### 返回值

Each connection pool has an identifier, which starts with the host. For
each pool, this function shows the following fields:

`in use`  
The number of connections currently being used by <span
class="classname">MongoClient</span> instances.

`in pool`  
The number of connections currently in the pool (not being used).

`remaining`  
The number of connections that could be created by this pool. For
example, suppose a pool had 5 connections remaining and 3 connections in
the pool. We could create 8 new instances of <span
class="classname">MongoClient</span> before we exhausted this pool
(assuming no instances of <span class="classname">MongoClient</span>
went out of scope, returning their connections to the pool).

A negative number means that this pool will spawn unlimited connections.

Before a pool is created, you can change the max number of connections
by calling <span class="function">Mongo::setPoolSize</span>. Once a pool
is showing up in the output of this function, its size cannot be
changed.

`timeout`  
The socket timeout for connections in this pool. This is how long
connections in this pool will attempt to connect to a server before
giving up.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

Mongo::setPoolSize
==================

Set the size for future connection pools

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Mongo::setPoolSize</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> )

**Warning**

This method has been *DEPRECATED* as of version 1.2.3. Relying on this
feature is highly discouraged. Please use <span
class="function">MongoPool::setSize</span> instead.

Sets the max number of connections new pools will be able to create.

### 参数

`size`  
The max number of connections future pools will be able to create.
Negative numbers mean that the pool will spawn an infinite number of
connections.

### 返回值

Returns the former value of pool size.

### 范例

**示例 \#1 <span class="function">Mongo::setPoolSize</span> example**

If you set the pool size to *n* and then create *n* connections,
attempting to create an *n+1*st connection will throw a <span
class="classname">MongoConnectionException</span>.

``` php
<?php

// only allow one connection to a server
Mongo::setPoolSize(1);

// creates one connection to localhost:27017
$m1 = new Mongo();

// attempt to create a second connection to localhost:27017
// only one connection is allowed, so this will throw an exception
$m2 = new Mongo();

?>
```

以上例程的输出类似于：

    Fatal error: Uncaught exception 'MongoConnectionException' with message 'no more connections in pool' in /path/to/php/script.php:10
    Stack trace:
    #0 /path/to/php/script.php(10): Mongo->__construct()
    #1 {main}
      thrown in /path/to/php/script.php on line 10

### 参见

-   <span class="function">Mongo::getPoolSize</span>
-   <span class="function">Mongo::poolDebug</span>
-   The
    <a href="/book/mongo.html#链接服务器" class="link">connection</a>
    documentation.

Mongo::setSlaveOkay
===================

Change slaveOkay setting for this connection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Mongo::setSlaveOkay</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$ok`<span
class="initializer"> = **`TRUE`**</span></span> \] )

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

`ok`  
If reads should be sent to secondary members of a replica set for all
possible queries using this <span class="classname">MongoClient</span>
instance.

### 返回值

Returns the former value of slaveOkay for this instance.

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>
-   <span class="methodname">MongoClient::setReadPreference</span>

Mongo::switchSlave
==================

Choose a new secondary for slaveOkay reads

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Mongo::switchSlave</span> ( <span
class="methodparam">void</span> )

This choses a random secondary for a connection to read from. It is
called automatically by the driver and should not need to be used. It
calls <span class="function">MongoClient::getHosts</span> (to refresh
the status of hosts) and <span class="function">Mongo::getSlave</span>
(to get the return value).

See
<a href="/book/mongo.html#Querying" class="link">the query section</a>
of this manual for information on distributing reads to secondaries.

### 参数

此函数没有参数。

### 返回值

The address of the secondary this connection is using for reads. This
may be the same as the previous address as addresses are randomly
chosen. It may return only one address if only one secondary (or only
the primary) is available.

For example, if we had a three member replica set with a primary,
secondary, and arbiter this method would always return the address of
the secondary. If the secondary became unavailable, this method would
always return the address of the primary. If the primary also became
unavailable, this method would throw an exception, as an arbiter cannot
handle reads.

### 错误／异常

Throws a <span class="classname">MongoException</span> (error code 15)
if it is called on a non-replica-set connection. It will also throw
<span class="classname">MongoException</span>s if it cannot find anyone
(primary or secondary) to read from (error code 16).

### 更新日志

| 版本   | 说明                                |
|--------|-------------------------------------|
| 1.2.11 | Emits **`E_DEPRECATED`** when used. |

### 参见

-   <a href="/book/mongo.html#读取首选项" class="xref"></a>

bson\_decode
============

反序列化一个 BSON 对象为 PHP 数组

### 说明

<span class="type">array</span> <span
class="methodname">bson\_decode</span> ( <span class="methodparam"><span
class="type">string</span> `$bson`</span> )

这个函数非常不正式，对 99% 的用户是完全没用的。
仅仅在做着一些不寻常的事的情况下有用，比如在 PHP
驱动的基础上编写自己的驱动。

### 参数

`bson`  
要反序列化的 BSON。

### 返回值

返回反序列化后的 BSON 对象。

bson\_encode
============

序列化一个 PHP 变量为 BSON 字符串

### 说明

<span class="type">string</span> <span
class="methodname">bson\_encode</span> ( <span class="methodparam"><span
class="type">mixed</span> `$anything`</span> )

这个函数非常不正式，对 99% 的用户是完全没用的。
仅仅在做着一些不寻常的事的情况下有用，比如在 PHP
驱动的基础上编写自己的驱动。

### 参数

`anything`  
要序列化的变量。

### 返回值

返回序列化后的字符串。

**目录**

-   [bson\_decode](/book/mongo.html#bson_decode) — 反序列化一个 BSON
    对象为 PHP 数组
-   [bson\_encode](/book/mongo.html#bson_encode) — 序列化一个 PHP 变量为
    BSON 字符串

Exceptions
==========

**目录**

-   [MongoException](/book/mongo.html#MongoException) — The
    MongoException class
-   [MongoResultException](/book/mongo.html#MongoResultException) —
    MongoResultException 类
    -   [MongoResultException::getDocument](/book/mongo.html#MongoResultException::getDocument)
        — 获取完整的结果文档
-   [MongoCursorException](/book/mongo.html#MongoCursorException) — The
    MongoCursorException class
    -   [MongoCursorException::getHost](/book/mongo.html#MongoCursorException::getHost)
        — 遇到该错误的服务器的 hostname
-   [MongoCursorTimeoutException](/book/mongo.html#MongoCursorTimeoutException)
    — The MongoCursorTimeoutException class
-   [MongoConnectionException](/book/mongo.html#MongoConnectionException)
    — The MongoConnectionException class
-   [MongoGridFSException](/book/mongo.html#MongoGridFSException) — The
    MongoGridFSException class
-   [MongoDuplicateKeyException](/book/mongo.html#MongoDuplicateKeyException)
    — The MongoDuplicateKeyException class
-   [MongoProtocolException](/book/mongo.html#MongoProtocolException) —
    The MongoProtocolException class
-   [MongoExecutionTimeoutException](/book/mongo.html#MongoExecutionTimeoutException)
    — The MongoExecutionTimeoutException class
-   [MongoWriteConcernException](/book/mongo.html#MongoWriteConcernException)
    — The MongoWriteConcernException class
    -   [MongoWriteConcernException::getDocument](/book/mongo.html#MongoWriteConcernException::getDocument)
        — Get the error document

VMWare Oddities
---------------

If you are running VMWare on Windows and are using CIFS, pausing the VM
will cause CIFS to go out of sync and cause weird errors on un-pausing
it ("The Mongo object has not been correctly initialized by its
constructor"). Permanently mounting the Windows shares will fix this and
you'll be able to pause and unpause at will.

To permanently mount the Windows shares, run:

``` shell
$ sudo update-rc.d -f umountnfs.sh remove
$ sudo update-rc.d umountnfs.sh stop 15 0 6 .
```

See
<a href="https://help.ubuntu.com/community/MountWindowsSharesPermanently" class="link external">» the Ubuntu docs</a>
for the most up-to-date instructions.

简介
----

Default Mongo exception.

This covers a bunch of different error conditions that may eventually be
moved to more specific exceptions, but will always extend <span
class="classname">MongoException</span>.

-   *The MongoSomething object has not been correctly initialized by its
    constructor*

    Code: 0

    Probably your Mongo object is not connected to a database server.

-   *zero-length keys are not allowed, did you use $ with double
    quotes?*

    Code: 1

    You tried to save "" as a key. You generally should not do this. ""
    can mess up subobject access and is used by MongoDB internally.
    However, if you really want, you can set
    <a href="/book/mongo.html#" class="link">mongo.allow_empty_keys</a>
    to true in your php.ini file to override this sanity check. If you
    override this, it is highly recommended that you set error checking
    to strict to avoid string interpolation errors.

-   *'.' not allowed in key: \<key\>*

    Code: 2

    You attempted to write a key with '.' in it, which is prohibited.

-   *insert too large: \<size\>, max: \<max\>*

    Code: 3

    You're attempting to send too much data to the database at once: the
    database will only accept inserts up to a certain size (currently 16
    MB).

-   *no elements in doc*

    Code: 4

    You're attempting to save a document with no fields.

-   *size of BSON doc is \<size\> bytes, max \<max\>MB*

    Code: 5

    You're attempting to save a document that is larger than MongoDB can
    save.

-   *no documents given*

    Code: 6

    You're attempting to batch insert an empty array of documents.

-   *MongoCollection::group takes an array, object, or MongoCode key*

    Code: 7

    Wrong type parameter send to <span
    class="function">MongoCollection::group</span>.

-   *field names must be strings*

    Code: 8

    You should format field selectors as *array("field1" =\> 1, "field2"
    =\> 1, ..., "fieldN" =\> 1)*.

-   *invalid regex*

    Code: 9

    The regex passed to <span class="classname">MongoRegex</span> is not
    of the correct form.

-   *MongoDBRef::get: $ref field must be a string*

    Code: 10

-   *MongoDBRef::get: $db field must be a string*

    Code: 11

-   *non-utf8 string: \<str\>*

    Code: 12

    This error occurs if you attempt to send a non-utf8 string to the
    database. All strings going into the database should be UTF8. See
    php.ini options for the transition option of quieting this
    exception.

-   *mutex error: \<err\>*

    Code: 13

    The driver uses mutexes for synchronizing requests and responses in
    multithreaded environments. This is a fairly serious error and may
    not have a stack trace. It's unusual and should be reported to
    maintainers with any system information and steps to reproduce that
    you can provide.

-   *index name too long: \<len\>, max \<max\> characters*

    Code: 14

    Indexes with names longer than 128 characters cannot be created. If
    you get this error, you should use <span
    class="function">MongoCollection::ensureIndex</span>'s "name" option
    to create a shorter name for your index.

类摘要
------

**MongoException**

<span class="ooclass"> class **MongoException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

}

简介
----

MongoResultException 由几个助手命令（例如 <span
class="methodname">MongoCollection::findAndModify</span>）在发生失败事件时抛出。
原始的结果文档可以通过 <span
class="methodname">MongoResultException::getDocument</span> 获取。

类摘要
------

**MongoResultException**

<span class="ooclass"> class **MongoResultException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoException** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$document` ;

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDocument</span> ( <span
class="methodparam">void</span> )

}

属性
----

`document`  
array 的原始结果文档。

MongoResultException::getDocument
=================================

获取完整的结果文档

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoResultException::getDocument</span> (
<span class="methodparam">void</span> )

获取完整的错误结果文档。

### 参数

此函数没有参数。

### 返回值

完整的结果文档数组，包括是否有效的部分数据以及额外的键。

### 范例

**示例 \#1 <span
class="methodname">MongoResultException::getDocument</span> 例子**

``` php
<?php
$mc = new MongoClient("localhost");
$c = $mc->selectCollection("test", "test");

$c->insert(array(
     "name" => "Next promo",
     "inprogress" => false,
     "priority" => 0,
     "tasks" => array( "select product", "add inventory", "do placement"),
) );

$c->insert(array(
     "name" => "Biz report",
     "inprogress" => false,
     "priority" => 1,
     "tasks" => array( "run sales report", "email report" )
) );

$c->insert(array(
     "name" => "Biz report",
     "inprogress" => false,
     "priority" => 2,
     "tasks" => array( "run marketing report", "email report" )
    ),
    array("w" => true)
);

try {
    $retval = $c->findAndModify(
         array("inprogress" => false, "name" => "Biz report"),
         array('$set' => array('$set' => array('inprogress' => true, "started" => new MongoDate()))),
         null,
         array(
            "sort" => array("priority" => -1),
            "new" => true,
        )
    );
} catch(MongoResultException $e) {
    echo $e->getMessage(), "\n";
    $res = $e->getDocument();
    var_dump($res);
}
?>
```

以上例程的输出类似于：

    $set is not valid for storage.
    array(3) {
      ["lastErrorObject"]=>
      array(5) {
        ["connectionId"]=>
        int(6)
        ["err"]=>
        string(30) "$set is not valid for storage."
        ["code"]=>
        int(52)
        ["n"]=>
        int(0)
        ["ok"]=>
        float(1)
      }
      ["ok"]=>
      float(0)
      ["errmsg"]=>
      string(30) "$set is not valid for storage."
    }

简介
----

Caused by accessing a cursor incorrectly or a error receiving a reply.
Note that this can be thrown by any database request that receives a
reply, not just queries. Writes, commands, and any other operation that
sends information to the database and waits for a response can throw a
<span class="classname">MongoCursorException</span>. The only exception
is *new MongoClient()* (creating a new connection), which will only
throw <span class="classname">MongoConnectionException</span>s.

This returns a specific error message to help diagnose the problem and a
numeric error code associated with the cause of the exception.

For example, suppose you tried to insert two documents with the same
\_id:

``` php
<?php

try {
    $collection->insert(array("_id" => 1), array("w" => 1));
    $collection->insert(array("_id" => 1), array("w" => 1));
}
catch (MongoCursorException $e) {
    echo "error message: ".$e->getMessage()."\n";
    echo "error code: ".$e->getCode()."\n";
}

?>
```

This would produce output like:

``` txt
error message: E11000 duplicate key error index: foo.bar.$_id_  dup key: { : 1 }
error code: 11000
```

Note that the MongoDB error code (11000) is used for the PHP error code.
The PHP driver uses the "native" error code wherever possible.

The following is a list of common errors, codes, and causes. Exact
errors are in italics, errors where the message can vary are described
in obliques.

-   *cannot modify cursor after beginning iteration*

    Code: 0

    You are calling a method that sets up the query after executing the
    query. Reset the cursor and try again.

    An example:

    ``` php
    <?php

    try {
        $cursor = $collection->find();
        var_dump($cursor->getNext());

        // getNext() queried the database, it's too late to set a limit
        $cursor->limit(1);
    }
    catch (MongoCursorException $e) {
        echo "error message: ".$e->getMessage()."\n";
        echo "error code: ".$e->getCode()."\n";
    }

    // this will work, though:
    $cursor->getNext();
    $cursor->reset();
    $cursor->limit(1);

    ?>
    ```

-   Get next batch send errors

    Code: 1

    Could not send the query to the database. Make sure the database is
    still up and the network is okay.

-   *cursor not found*

    Code: 2

    The driver was trying to fetch more results from the database, but
    the database did not have a record of the query. This usually means
    that the cursor timed out on the server side: after a few minutes of
    inactivity, the database will kill a cursor (see <span
    class="function">MongoCursor::immortal</span> for information on
    preventing this).

    An example:

    ``` php
    <?php

    try {
        $cursor = $collection->find();
        $cursor->getNext();

        // sleep for 15 minutes
        sleep(60*15);

        while ($cursor->hasNext()) {
            $cursor->getNext();
        }
    }
    catch (MongoCursorException $e) {
        echo "error message: ".$e->getMessage()."\n";
        echo "error code: ".$e->getCode()."\n";
    }

    ?>
    ```

-   *cursor-\>buf.pos is null*

    Code: 3

    This may indicate you are out of RAM or some other extraordinary
    circumstance.

-   *couldn't get response header*

    Code: 4

    A common error if the database or network goes down. This means that
    the driver couldn't get a response from the connection.

-   *no db response*

    Code: 5

    This may not even be an error, for example, the database command
    "shutdown" returns no response. However, if you were expecting a
    response, this means the database didn't give one.

-   *bad response length: %d, did the db assert?*

    Code: 6

    This means that the database said that its response was less than 0.
    This error probably indicates a network error or database
    corruption.

-   *incomplete header*

    Code: 7

    Highly unusual. Occurs if the database response started out
    correctly, but broke off in the middle. Probably indicates a network
    problem.

-   *incomplete response*

    Code: 8

    Highly unusual. Occurs if the database response started out
    correctly, but broke off in the middle. Probably indicates a network
    problem.

-   *couldn't find a response*

    Code: 9

    If the response was cached and now cannot be located.

-   *error getting socket*

    Code: 10

    The socket was closed or encountered an error. The driver should
    automatically reconnect (if possible) on the next operation.

-   *couldn't find reply, please try again*

    Code: 11

    The driver saves any database responses it cannot immediately match
    with a request. This exception occurs if the driver has already
    passed your request's response and cannot find your response in its
    cache.

-   *error getting database response: errstr*

    *WSA error getting database response: errstr*

    "errstr" is an io error reported directly from the C socket
    subsystem. On Windows, the error message is prefixed with "WSA".

-   *Timeout error*

    Code: 13

    If there was an error while waiting for a query to complete.

-   *couldn't send query: \<various\>*

    Code: 14

    C socket error on send.

-   *max number of retries exhausted, couldn't send query*

    Code: 19

    The driver will automatically retry "plain" queries (not commands) a
    couple of times if the first attempt failed for certain reasons.
    This is to cause fewer exceptions during replica set failover
    (although you will probably still have to deal with some) and gloss
    over transient network issues.

    This can also be caused by the driver not being able to reconnect at
    all to the database (if, for example, the database is unreachable).

    Version 1.2.2+.

Errors passed through by the database
-------------------------------------

Database errors should always trigger <span
class="classname">MongoCursorExceptions</span> on queries. Error
messages and codes are sent directly from the database and you should be
able to see matching errors in the database log.

A few common database errors are listed below:

-   *E11000 duplicate key error index: foo.bar.$X dup key: { /\* ... \*/
    }*

    Code: 11000

    Database error for duplicate keys.

-   *not master*

    Codes: 10107, 13435, and 10058

    Not master errors, piped through by the database. ach of these will
    cause the driver to disconnect and attempt to find a new primary.
    The actual error you get on failover may not be a "not master"
    error, depending on when the change in primary occurs.

类摘要
------

**MongoCursorException**

<span class="ooclass"> class **MongoCursorException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoException** </span> {

}

MongoCursorException::getHost
=============================

遇到该错误的服务器的 hostname

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoCursorException::getHost</span> ( <span
class="methodparam">void</span> )

返回发送查询到该服务器的 hostname。

### 参数

此函数没有参数。

### 返回值

返回 hostname，如果 hostname 是未知的则是 <span
class="type">NULL</span>。

简介
----

Caused by a query timing out. You can set the length of time to wait
before this exception is thrown by calling <span
class="function">MongoCursor::timeout</span> on the cursor or setting
*MongoCursor::$timeout*. The static variable is useful for queries such
as database commands and <span
class="function">MongoCollection::findOne</span>, both of which
implicitly use cursors.

类摘要
------

**MongoCursorTimeoutException**

<span class="ooclass"> class **MongoCursorTimeoutException** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**MongoCursorException** </span> {

}

简介
----

Thrown when the driver fails to connect to the database.

There are a number of possible error messages to help you diagnose the
connection problem. These are:

-   *No candidate servers found*

    Thrown when the driver cannot establish a connection to MongoDB
    (fulfilling the ReadPreferences, if specified).

-   *No server name given.*

    This error occurs if you pass in "" as the server name, probably
    because of an typo with string interpolation, e.g., "$servr" instead
    of "$server".

-   *failed to get host \[hostname\] or port \[portnum\] from
    \[server\].*

    This indicated that the server string was malformed. "\[hostname\]"
    and "\[portnum\]" will be as much as the driver could dicipher of
    it.

-   *Operation in progress*

    Connecting to the database timed out.

-   *Transport endpoint is not connected*

    Generally means that the connection string isn't correct, the driver
    couldn't even find the database server.

-   *couldn't determine master*

    No server in a replica set connection was identified as the primary.

-   *couldn't get host info for \[server\]*

    This indicated that DNS could not resolve the server address you
    gave. This could easily be caused by a typo, for example, "server"
    instead of "$server".

-   *Invalid Argument*

    This can be caused by attempting to connect to a machine that is up
    but that the database isn't actually running on. Make sure that
    you've started the database server before connecting.

-   *Permission denied*

    This means that the socket could not be opened due to permissions
    issues. On Red Hat variants, this can be caused by a default setting
    that does not allow Apache to create network connections. You can
    override this setting by running:

    ``` shell
    $ /usr/sbin/setsebool -P httpd_can_network_connect 1
    ```

    then restarting Apache.

If the error message is not listed above, it is probably an error from
the C socket, and you can search the web for its usual cause.

类摘要
------

**MongoConnectionException**

<span class="ooclass"> class **MongoConnectionException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoException** </span> {

}

简介
----

Thrown when there are errors reading or writing files to or from the
database.

类摘要
------

**MongoGridFSException**

<span class="ooclass"> class **MongoGridFSException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoException** </span> {

}

Error codes
-----------

| Code | Message                                                                        | Reason                                                 |
|------|--------------------------------------------------------------------------------|--------------------------------------------------------|
| 3    | Could not open file `$filename`                                                | Attempting to store an invalid file, such as directory |
| 4    | File `$filename` is too large: `$filesize` bytes                               | Maximum filesize in GridFS is 4GB                      |
| 5    | could not find filehandle                                                      | Resource doesn't have a filehandle                     |
| 6    | no file is associate with this filehandle                                      | Resource isn't a file resource                         |
| 7    | error setting up file: `$filename`s                                            | Could not open file for reading                        |
| 9    | error reading file `$filename`s                                                | Failed reading file                                    |
| 10   | error reading filehandle                                                       | Failed reading from a resource                         |
| 11   | could not find uploaded file %s                                                | Filename doesn't seem to be uploaded file              |
| 12   | Couldn't find tmp\_name in the $\_FILES array. Are you sure the upload worked? | Uploaded filename probably failed                      |
| 13   | tmp\_name was not a string or an array                                         | Invalid filename given                                 |
| 14   | couldn't find file size                                                        | The `length` property is missing                       |
| 15   | Cannot find filename                                                           | No filename provided, and no `filename` property set   |
| 16   | could not open destination file %s                                             | Destination filename not writable                      |
| 17   | error reading chunk of file                                                    | Chunk corruption                                       |
| 18   | couldn't create a php\_stream                                                  | Couldn't create a stream resource                      |
| 19   | couldn't find `property`                                                       | Chunk corruption                                       |
| 20   | chunk `number` has wrong size (`size`) when the max is `maxchunksize`          | Chunk larger then expected                             |
| 21   | chunk has wrong format                                                         | Chunk corruption                                       |

简介
----

Thrown when attempting to insert a document into a collection which
already contains the same values for the
<a href="/book/mongo.html#MongoCollection::ensureIndex" class="link">unique keys</a>.

类摘要
------

**MongoDuplicateKeyException**

<span class="ooclass"> class **MongoDuplicateKeyException** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**MongoWriteConcernException** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoWriteConcernException::getDocument</span>
( <span class="methodparam">void</span> )

}

范例
----

**示例 \#1 Catching MongoDuplicateKeyException**

``` php
<?php
$mc = new MongoClient("localhost");

$c = $mc->selectCollection("test", "test");

$c->insert(array('_id' => 1));
try {
    $c->insert(array('_id' => 1));
} catch (MongoWriteConcernException $e) {
    echo $e->getMessage(), "\n";
}
?>
```

以上例程的输出类似于：

    localhost:27017: insertDocument :: caused by :: 11000 E11000 duplicate key error index: test.test.$_id_  dup key: { : 1 }

简介
----

When talking to MongoDB 2.6.0, and later, certain operations (such as
writes) may throw MongoProtocolException when the response from the
server did not make sense - for example during network failure (we could
read the entire response) or data corruption.

This exception is also thrown when attempting to talk newer protocols
then the server supports, for example using the <span
class="classname">MongoWriteBatch</span> when talking to a MongoDB
server prior to 2.6.0.

类摘要
------

**MongoProtocolException**

<span class="ooclass"> class **MongoProtocolException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoException** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

}

范例
----

**示例 \#2 Catching MongoProtocolException**

Running the following example against MongoDB prior to 2.6.0 will throw
an MongoProtocolException

``` php
<?php
$mc = new MongoClient("localhost");
$c = $mc->selectCollection("test", "test");

try {
    $batch = new MongoInsertBatch($c);
} catch(MongoProtocolException $e) {
    echo $e->getMessage();
}
?>
```

以上例程的输出类似于：

    Current primary does not have a Write API

简介
----

Thrown when a operation times out server side (i.e. in MongoDB).

To configure the operation timeout threshold, use <span
class="methodname">MongoCursor::maxTimeMS</span> or the *"maxTimeMS"*
command option.

类摘要
------

**MongoExecutionTimeoutException**

<span class="ooclass"> class **MongoExecutionTimeoutException** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**MongoException** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

}

简介
----

MongoWriteConcernException is thrown when a write fails. See
<a href="/book/mongo.html#Write%20Concerns" class="xref"></a> for how to
set failure thresholds.

Prior to MongoDB 2.6.0, the
<a href="https://docs.mongodb.com/manual/reference/command/getLastError" class="link external">» getLastError</a>
command would determine whether a write failed.

类摘要
------

**MongoWriteConcernException**

<span class="ooclass"> class **MongoWriteConcernException** </span>
<span class="ooclass"> <span class="modifier">extends</span>
**MongoCursorException** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDocument</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">MongoCursorException::getHost</span> ( <span
class="methodparam">void</span> )

}

MongoWriteConcernException::getDocument
=======================================

Get the error document

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">MongoWriteConcernException::getDocument</span>
( <span class="methodparam">void</span> )

Returns the actual response from the server that was interperated as an
error.

### 参数

此函数没有参数。

### 返回值

A MongoDB document, if available, as an array.

更新日志
========

对本扩展的类／函数／方法有以下更新。

It supports all new features for MongoDB 2.6, including:

-   Aggregate can now return a cursor
-   Aggregation pipelines can now be explained
-   Possible to set maxTimeMS for commands and queries
-   Transparent support for the new command-based MongoDB write API
-   New MongoWriteBatch classes (using the new MongoDB write API)
-   Support for MongoDB Enterprise features (e.g. Kerberos, LDAP, X509)
-   Option to tune acceptable server latency for secondary reads
    (secondaryAcceptableLatencyMS)

With this release, some driver functionality which was previously
documented as deprecated will now formally raise deprecation notices.
This includes:

-   Instantiating the Mongo class
-   Calling MongoCursor::slaveOkay()
-   "wtimeout" and "safe" options for MongoCollection write operations
-   Manipulating public properties on core classes (such as
    $collection-\>w)

> **Note**:
>
> No previously deprecated features have been removed.

Changes in behaviour:

-   Setting the mongo.native\_long INI setting now raises an error on
    32-bit platforms, and now defaults to true for 64-bit platforms.

The 1.4 series introduced fundemental changes in how connections are
created to the MongoDB servers. The driver now utilizes PHP native
streams, so all normal PHP stream options apply. Furthermore, an
experimental Stream Context Support was added.

The 1.4.x series also added support for MongoDB 2.4.x.

The most important improvements however deal with the handling of
replica sets, especially nodes that timeout and nodes that are
unreachable for various reasons. Besides the improvements to replica set
handling, this release addresses issues with read preferences through
mongos nodes. It also adds support for SSL enabled connections as well
as journal and fsync connection string options.

The 1.3 series introduced several major changes to the extension such as
completely rewritten
<a href="/book/mongo.html#链接服务器" class="link">connection handling</a>
(and removal of the pooling mechanism), support for
<a href="/book/mongo.html#读取首选项" class="link">ReadPreferences</a>
and change the default
<a href="/book/mongo.html#Writes" class="link">WriteConcerns</a> to be
*acknowledged* by introducing a new class
<a href="/book/mongo.html#MongoClient" class="link">MongoClient</a>
which serves as a replacement class for the now deprecated <span
class="classname">Mongo</span> class.

The driver now also supports connecting to multiple mongos instances
(the Mongo Shard router) for loadbalancing.

Other enhancements include improved logging for easier connection
handling debugging with <span class="classname">MongoLog</span> and
support for the
<a href="https://docs.mongodb.com/manual/core/aggregation-pipeline/" class="link external">» Aggregation Framework</a>
via the <span class="methodname">MongoCollection::aggregate</span>
method.

Following is a list of all improvements to existing methods since their
inception.
