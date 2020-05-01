Memcache
========

**目录**

-   [简介](/intro/memcache.html)
-   [安装／配置](/memcache/setup.html)
    -   [需求](/memcache/setup.html#需求)
    -   [安装](/memcache/setup.html#安装)
    -   [运行时配置](/memcache/setup.html#运行时配置)
    -   [资源类型](/memcache/setup.html#资源类型)
-   [预定义常量](/memcache/constants.html)
-   [范例](/memcache/examples.html)
    -   [](/memcache/examples.html#)
-   [Memcache](/class/memcache.html) — Memcache类
    -   [Memcache::add](/class/memcache.html#Memcache::add) —
        增加一个条目到缓存服务器
    -   [Memcache::addServer](/class/memcache.html#Memcache::addServer)
        — 向连接池中添加一个memcache服务器
    -   [Memcache::close](/class/memcache.html#Memcache::close) —
        关闭memcache连接
    -   [Memcache::connect](/class/memcache.html#Memcache::connect) —
        打开一个memcached服务端连接
    -   [Memcache::decrement](/class/memcache.html#Memcache::decrement)
        — 减小元素的值
    -   [Memcache::delete](/class/memcache.html#Memcache::delete) —
        从服务端删除一个元素
    -   [Memcache::flush](/class/memcache.html#Memcache::flush) —
        清洗（删除）已经存储的所有的元素
    -   [Memcache::get](/class/memcache.html#Memcache::get) —
        从服务端检回一个元素
    -   [Memcache::getExtendedStats](/class/memcache.html#Memcache::getExtendedStats)
        — 缓存服务器池中所有服务器统计信息
    -   [Memcache::getServerStatus](/class/memcache.html#Memcache::getServerStatus)
        — 用于获取一个服务器的在线/离线状态
    -   [Memcache::getStats](/class/memcache.html#Memcache::getStats) —
        获取服务器统计信息
    -   [Memcache::getVersion](/class/memcache.html#Memcache::getVersion)
        — 返回服务器版本信息
    -   [Memcache::increment](/class/memcache.html#Memcache::increment)
        — 增加一个元素的值
    -   [Memcache::pconnect](/class/memcache.html#Memcache::pconnect) —
        打开一个到服务器的持久化连接
    -   [Memcache::replace](/class/memcache.html#Memcache::replace) —
        替换已经存在的元素的值
    -   [Memcache::set](/class/memcache.html#Memcache::set) — Store data
        at the server
    -   [Memcache::setCompressThreshold](/class/memcache.html#Memcache::setCompressThreshold)
        — 开启大值自动压缩
    -   [Memcache::setServerParams](/class/memcache.html#Memcache::setServerParams)
        — 运行时修改服务器参数和状态
-   [Memcache 函数](/ref/memcache.html)
    -   [memcache\_debug](/ref/memcache.html#memcache_debug) —
        转换调试输出的开/关

简介
----

表示连接到一个服务器组的连接。

类摘要
------

**Memcache**

<span class="ooclass"> class **Memcache** </span> {

<span class="type">bool</span> <span class="methodname">add</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$var`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flag`</span> \[, <span
class="methodparam"><span class="type">int</span> `$expire`</span> \]\]
)

<span class="type">bool</span> <span class="methodname">addServer</span>
( <span class="methodparam"><span class="type">string</span>
`$host`</span> \[, <span class="methodparam"><span
class="type">int</span> `$port`<span class="initializer"> =
11211</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$persistent`</span> \[, <span
class="methodparam"><span class="type">int</span> `$weight`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$retry_interval`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$status`</span> \[,
<span class="methodparam"><span class="type">callback</span>
`$failure_callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeoutms`</span> \]\]\]\]\]\]\]\] )

<span class="type">bool</span> <span class="methodname">close</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">connect</span> (
<span class="methodparam"><span class="type">string</span>
`$host`</span> \[, <span class="methodparam"><span
class="type">int</span> `$port`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \]\]
)

<span class="type">int</span> <span class="methodname">decrement</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> \[, <span class="methodparam"><span
class="type">int</span> `$value`<span class="initializer"> =
1</span></span> \] )

<span class="type">bool</span> <span class="methodname">delete</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`<span class="initializer"> = 0</span></span> \] )

<span class="type">bool</span> <span class="methodname">flush</span> (
<span class="methodparam">void</span> )

<span class="type">string</span> <span class="methodname">get</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
\[, <span class="methodparam"><span class="type">int</span>
`&$flags`</span> \] )

<span class="type">array</span> <span
class="methodname">getExtendedStats</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`</span> \[,
<span class="methodparam"><span class="type">int</span> `$slabid`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = 100</span></span> \]\]\] )

<span class="type">int</span> <span
class="methodname">getServerStatus</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 11211</span></span> \] )

<span class="type">array</span> <span class="methodname">getStats</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$type`</span> \[, <span class="methodparam"><span
class="type">int</span> `$slabid`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = 100</span></span> \]\]\] )

<span class="type">string</span> <span
class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">increment</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> \[, <span class="methodparam"><span
class="type">int</span> `$value`<span class="initializer"> =
1</span></span> \] )

<span class="type">mixed</span> <span class="methodname">pconnect</span>
( <span class="methodparam"><span class="type">string</span>
`$host`</span> \[, <span class="methodparam"><span
class="type">int</span> `$port`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \]\]
)

<span class="type">bool</span> <span class="methodname">replace</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$var`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flag`</span> \[, <span
class="methodparam"><span class="type">int</span> `$expire`</span> \]\]
)

<span class="type">bool</span> <span class="methodname">set</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$var`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flag`</span> \[, <span
class="methodparam"><span class="type">int</span> `$expire`</span> \]\]
)

<span class="type">bool</span> <span
class="methodname">setCompressThreshold</span> ( <span
class="methodparam"><span class="type">int</span> `$threshold`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$min_savings`</span> \] )

<span class="type">bool</span> <span
class="methodname">setServerParams</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 11211</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$retry_interval`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$status`</span> \[, <span class="methodparam"><span
class="type">callback</span> `$failure_callback`</span> \]\]\]\]\] )

}

Memcache::add
=============

增加一个条目到缓存服务器

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::add</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flag`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expire`</span> \]\] )

<span
class="function">Memcache::add</span>方法在缓存服务器之前不存在`key`时，
以`key`作为key存储一个变量`var`到缓存服务器。 同样可以使用函数<span
class="function">memcache\_add</span>。

### 参数

`key`  
将要分配给变量的key。

`var`  
将要被存储的变量。字符串和整型被以原文存储，其他类型序列化后存储。

`flag`  
使用**`MEMCACHE_COMPRESSED`**标记对数据进行压缩(使用zlib)。

`expire`  
当前写入缓存的数据的失效时间。如果此值设置为0表明此数据永不过期。你可以设置一个UNIX时间戳或
以秒为单位的整数（从当前算起的时间差）来说明此数据的过期时间，但是在后一种设置方式中，不能超过
2592000秒（30天）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
如果这个key已经存在返回**`FALSE`**。 <span
class="function">Memcache::add</span>方法的其他行为类似 <span
class="function">Memcache::set</span>。

### 范例

**示例 \#1 <span class="function">Memcache::add</span>示例**

``` php
<?php

$memcache_obj = memcache_connect("localhost", 11211);

/* 面向过程编程 API */
memcache_add($memcache_obj, 'var_key', 'test variable', false, 30);

/* 面向对象编程 API */
$memcache_obj->add('var_key', 'test variable', false, 30);

?>
```

### 参见

-   <span class="function">Memcache::set</span>
-   <span class="function">Memcache::replace</span>

Memcache::addServer
===================

向连接池中添加一个memcache服务器

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::addServer</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 11211</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$persistent`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$weight`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`</span> \[, <span
class="methodparam"><span class="type">int</span>
`$retry_interval`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$status`</span> \[, <span
class="methodparam"><span class="type">callback</span>
`$failure_callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeoutms`</span> \]\]\]\]\]\]\]\] )

<span
class="function">Memcache::addServer</span>增加一个服务器到连接池中。通过<span
class="function">Memcache::addServer</span>
打开的连接将会在脚本执行结束后自动关闭，也可以使用<span
class="function">Memcache::close</span>进行手动关闭。 您也可以使用<span
class="function">memcache\_add\_server</span>来添加服务器。

当使用这个方法的时候(与<span
class="function">Memcache::connect</span>和<span
class="function">Memcache::pconnect</span>相反)
网络连接并不会立刻建立，而是直到真正使用的时候才建立。
因此在加入大量服务器到连接池中时也是没有开销的，因为它们可能并不会被使用。

故障转移可能在方法的任何一个层次发生，通常只要其他服务器可用用户就不会感受到。任何的socket或memcache服务器级别的错误
（比如内存溢出）都可能导致故障转移。而一般的客户端错误比如使用Memcache::add尝试增加一个已经存在的key则不会导致故障转移。

> **Note**:
>
> 这个方法在2.0.0版本加入Memcache。

### 参数

`host`  
要连接的memcached服务端监听的主机位置。这个参数通常指定其他类型的传输比如Unix域套接字使用
*unix:///path/to/memcached.sock*，这种情况下参数`port` 必须设置为*0*。

`port`  
要连接的memcached服务端监听的端口。当使用UNIX域套接字连接时设置为*0*。

`persistent`  
控制是否使用持久化连接。默认**`TRUE`**。

`weight`  
为此服务器创建的桶的数量，用来控制此服务器被选中的权重，单个服务器被选中的概率是相对于所有服务器weight总和而言的。

`timeout`  
连接持续（超时）时间（单位秒），默认值1秒，修改此值之前请三思，过长的连接持续时间可能会导致失去所有的缓存优势。

`retry_interval`  
服务器连接失败时重试的间隔时间，默认值15秒。如果此参数设置为-1表示不重试。此参数和`persistent`参数在扩展以
<span class="function">dl</span>函数动态加载的时候无效。

每个失败的连接结构有自己的超时时间，并且在它失效之前选择后端服务请求时该结构会被跳过。一旦一个连接失效，
它将会被成功重新连接或被标记为失败连接以在下一个`retry_interval`秒重连。
典型的影响是每个web服务子进程在服务于一个页面时将会每`retry_interval`秒
尝试重新连接一次。

`status`  
控制此服务器是否可以被标记为在线状态。设置此参数值为**`FALSE`**并且`retry_interval`参数
设置为-1时允许将失败的服务器保留在一个池中以免影响key的分配算法。对于这个服务器的请求会进行故障转移或者立即失败，
这受限于`memcache.allow_failover`参数的设置。该参数默认**`TRUE`**，表明允许进行故障转移。

`failure_callback`  
允许用户指定一个运行时发生错误后的回调函数。回调函数会在故障转移之前运行。回调函数会接受到两个参数，分别是失败主机的
主机名和端口号。

`timeoutms`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::addServer</span> 示例**

``` php
<?php

/* OO API */

$memcache = new Memcache;
$memcache->addServer('memcache_host', 11211);
$memcache->addServer('memcache_host2', 11211);

/* procedural API */

$memcache_obj = memcache_connect('memcache_host', 11211);
memcache_add_server($memcache_obj, 'memcache_host2', 11211);

?>
```

### 参见

-   <span class="function">Memcache::connect</span>
-   <span class="function">Memcache::pconnect</span>
-   <span class="function">Memcache::close</span>
-   <span class="function">Memcache::setServerParams</span>
-   <span class="function">Memcache::getServerStatus</span>

Memcache::close
===============

关闭memcache连接

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::close</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcache::close</span>关闭到memcached服务端的连接。这个函数不会关闭持久化连接，
持久化连接仅仅会在web服务器关机/重启时关闭。与之对应的，你也可以使用<span
class="function">memcache\_close</span>函数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::close</span>示例**

``` php
<?php

/* 面向过程 API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/* 
do something here ..
*/
memcache_close($memcache_obj);

/* 面向对象 API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/* 
do something here ..
*/
$memcache_obj->close();

?>
```

### 参见

-   <span class="function">Memcache::connect</span>
-   <span class="function">Memcache::pconnect</span>

Memcache::connect
=================

打开一个memcached服务端连接

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::connect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \]\] )

<span
class="function">Memcache::connect</span>建立一个到memcached服务端的连接。
使用方法 <span
class="function">Memcache::connect</span>打开的连接在脚本执行结束后会自动关闭。当然，你也可以使用方法
<span class="function">Memcache::close</span>来主动关闭。
同时你也可以使用<span
class="function">memcache\_connect</span>函数来获取一个连接。

### 参数

`host`  
memcached服务端监听主机地址。这个参数也可以指定为其他传输方式比如*unix:///path/to/memcached.sock*
来使用Unix域socket，在这种方式下，`port`参数必须设置为*0*。

`port`  
memcached服务端监听端口。当使用Unix域socket的时候要设置此参数为*0*。

`timeout`  
连接持续（超时）时间，单位秒。默认值1秒，修改此值之前请三思，过长的连接持续时间可能会导致失去所有的缓存优势。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::connect</span> example**

``` php
<?php

/* procedural API */

$memcache_obj = memcache_connect('memcache_host', 11211);

/* OO API */

$memcache = new Memcache;
$memcache->connect('memcache_host', 11211);

?>
```

### 参见

-   <span class="function">Memcache::pconnect</span>
-   <span class="function">Memcache::close</span>

Memcache::decrement
===================

减小元素的值

### 说明

<span class="type">int</span> <span
class="methodname">Memcache::decrement</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$value`<span
class="initializer"> = 1</span></span> \] )

<span
class="function">Memcache::decrement</span>方法将元素的值减小`value`。
类似于 <span
class="function">Memcache::increment</span>方法，首先将元素当前值转换成数值然后减去`value`。

> **Note**:
>
> 新的元素的值不会小于0。

> **Note**:
>
> 不要将<span
> class="function">Memcache::decrement</span>方法用于压缩存储的元素，那样作会导致
> <span class="function">Memcache::get</span>方法获取值会失败。

<span
class="function">Memcache::decrement</span>在元素不存在时*不能*创建它。
同样可以使用<span
class="function">memcache\_decrement</span>函数来完成相同的工作。

### 参数

`key`  
要减小值的元素的key。

`value`  
`value`参数指要将指定元素的值减小多少。

### 返回值

成功的时候返回元素的新值 或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">Memcache::decrement</span> example**

``` php
<?php

/* procedural API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/* 将test_item对应的值减小2 */
$new_value = memcache_decrement($memcache_obj, 'test_item', 2);

/* OO API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/* decrement item by 3 */
$new_value = $memcache_obj->decrement('test_item', 3);
?>
```

### 参见

-   <span class="function">Memcache::increment</span>
-   <span class="function">Memcache::replace</span>

Memcache::delete
================

从服务端删除一个元素

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::delete</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 0</span></span> \] )

<span
class="function">Memcache::delete</span>函数通过`key`删除一个元素。
如果参数`timeout`指定，该元素会在`timeout`秒后失效。 同样也可以使用<span
class="function">memcache\_delete</span>函数完成同样功能。

### 参数

`key`  
要删除的元素的key。

`timeout`  
删除该元素的执行时间。如果值为0,则该元素立即删除，如果值为30,元素会在30秒内被删除。

### 更新日志

| 版本    | 说明                                                                                                                                                                                                              |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unknown | It's not recommended to use the `timeout` parameter. The behavior differs between memcached versions, but setting to *0* is safe. Other values for this deprecated feature may cause the memcache delete to fail. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::delete</span> example**

``` php
<?php

/* procedural API */
$memcache_obj = memcache_connect('memcache_host', 11211);

/* 10秒后key_to_delete对应的值会被从服务端删除 */
memcache_delete($memcache_obj, 'key_to_delete', 10);

/* OO API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);

$memcache_obj->delete('key_to_delete', 10);

?>
```

### 参见

-   <span class="function">Memcache::set</span>
-   <span class="function">Memcache::replace</span>

Memcache::flush
===============

清洗（删除）已经存储的所有的元素

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::flush</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcache::flush</span>立即使所有已经存在的元素失效。方法<span
class="function">Memcache::flush</span>
并不会真正的释放任何资源，而是仅仅标记所有元素都失效了，因此已经被使用的内存会被新的元素复写。
同样你也可以使用函数<span
class="function">memcache\_flush</span>完成相同功能。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::flush</span>示例**

``` php
<?php

/* procedural API */
$memcache_obj = memcache_connect('memcache_host', 11211);

memcache_flush($memcache_obj);

/* OO API */

$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);

$memcache_obj->flush();

?>
```

Memcache::get
=============

从服务端检回一个元素

### 说明

<span class="type">string</span> <span
class="methodname">Memcache::get</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `&$flags`</span>
\] )

<span class="type">array</span> <span
class="methodname">Memcache::get</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">array</span>
`&$flags`</span> \] )

如果服务端之前有以`key`作为key存储的元素，<span
class="function">Memcache::get</span>方法此时返回之前存储的值。

你可以给<span
class="function">Memcache::get</span>方法传递一个数组（多个key）来获取一个数组的元素值，返回的数组仅仅包含从
服务端查找到的key-value对。

### 参数

`key`  
要获取值的key或key数组。

`flags`  
如果给定这个参数（以引用方式传递），该参数会被写入一些key对应的信息。这些标记和<span
class="function">Memcache::set</span>方法中的同名参数
意义相同。用int值的低位保留了pecl/memcache的内部用法（比如：用来说明压缩和序列化状态）。（译注：最后一位表明是否序列化，倒数第二位表明是否经过压缩，
比如：如果此值为1表示经过序列化，但未经过压缩，2表明压缩而未序列化，3表明压缩并且序列化，0表明未经过压缩和序列化，具体算法可查找linux文件权限算法相关资料）

### 返回值

返回`key`对应的存储元素的字符串值或者在失败或`key`未找到的时候返回**`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::get</span> 示例**

``` php
<?php

/* procedural API */
$memcache_obj = memcache_connect('memcache_host', 11211);
$var = memcache_get($memcache_obj, 'some_key');

/* OO API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
$var = $memcache_obj->get('some_key');

/* 
你同样可以使用数组key作为参数，如果某个元素没有在服务端发现，结果数组中将不会包含这些key。
*/

/* procedural API */
$memcache_obj = memcache_connect('memcache_host', 11211);
$var = memcache_get($memcache_obj, Array('some_key', 'another_key'));

/* OO API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
$var = $memcache_obj->get(Array('some_key', 'second_key'));

?>
```

Memcache::getExtendedStats
==========================

缓存服务器池中所有服务器统计信息

### 说明

<span class="type">array</span> <span
class="methodname">Memcache::getExtendedStats</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`</span> \[,
<span class="methodparam"><span class="type">int</span> `$slabid`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = 100</span></span> \]\]\] )

<span class="function">Memcache::getExtendedStats</span>
返回一个二维关联数据的服务器统计信息。数组的key由host:port方式
组成，无效的服务器返回的统计信息被设置为false，同样的，你可以使用函数<span
class="function">memcache\_get\_extended\_stats</span>。

> **Note**:
>
> 这个函数在Memcache2.0.0版本加入。

> **Note**:
>
> (译注)获取Memcache内所有数据方法：首先使用getExtendedStats('slabs')获取到每个服务器上活动slabs分块的id，
> 然后 使用getExtendedStats('cachedump', $slabid,
> $limit)来获取每个slab里面缓存的项，其中$slabid是slab分块id， $limit指
> 期望获取其中的多少条记录。

### 参数

`type`  
期望抓取的统计信息类型，可以使用的值有{reset, malloc, maps, cachedump,
slabs, items, sizes}。
通过memcached协议指定这些附加参数是为了方便memcache开发者(检查其中的变动)。

`slabid`  
用于与参数`type`联合从指定slab分块拷贝数据，cachedump命令会完全占用服务器通常用于
比较严格的调试。

`limit`  
用于和参数`type`联合来设置cachedump时从服务端获取的实体条数。

### 返回值

返回一个二维关联数组的服务器统计信息或者在失败时返回**`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::getExtendedStats</span>
示例**

``` php
<?php
    $memcache_obj = new Memcache;
    $memcache_obj->addServer('memcache_host', 11211);
    $memcache_obj->addServer('failed_host', 11211);
    
    $stats = $memcache_obj->getExtendedStats();
    print_r($stats);
?>
```

以上例程会输出：

    Array
    (
        [memcache_host:11211] => Array
            (
                [pid] => 3756
                [uptime] => 603011
                [time] => 1133810435
                [version] => 1.1.12
                [rusage_user] => 0.451931
                [rusage_system] => 0.634903
                [curr_items] => 2483
                [total_items] => 3079
                [bytes] => 2718136
                [curr_connections] => 2
                [total_connections] => 807
                [connection_structures] => 13
                [cmd_get] => 9748
                [cmd_set] => 3096
                [get_hits] => 5976
                [get_misses] => 3772
                [bytes_read] => 3448968
                [bytes_written] => 2318883
                [limit_maxbytes] => 33554432
            )

        [failed_host:11211] => false
    )

### 参见

-   <span class="function">Memcache::getVersion</span>
-   <span class="function">Memcache::getStats</span>

Memcache::getServerStatus
=========================

用于获取一个服务器的在线/离线状态

### 说明

<span class="type">int</span> <span
class="methodname">Memcache::getServerStatus</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 11211</span></span> \] )

<span
class="function">Memcache::getServerStatus</span>返回一个服务器的在线/离线状态，你也同样可以使用
函数<span class="function">memcache\_get\_server\_status</span>。

> **Note**:
>
> 这个函数在memcache2.1.0版本加入。

### 参数

`host`  
主机监听地址。

`port`  
主机监听端口，默认11211.

### 返回值

返回一个服务器的状态，0表示服务器离线，非0表示在线。

### 范例

**示例 \#1 <span class="function">Memcache::getServerStatus</span>
示例**

``` php
<?php

/* OO API */
$memcache = new Memcache;
$memcache->addServer('memcache_host', 11211);
echo $memcache->getServerStatus('memcache_host', 11211);

/* procedural API */
$memcache = memcache_connect('memcache_host', 11211);
echo memcache_get_server_status($memcache, 'memcache_host', 11211);

?>
```

### 参见

-   <span class="function">Memcache::addServer</span>
-   <span class="function">Memcache::setServerParams</span>

Memcache::getStats
==================

获取服务器统计信息

### 说明

<span class="type">array</span> <span
class="methodname">Memcache::getStats</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`</span> \[,
<span class="methodparam"><span class="type">int</span> `$slabid`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = 100</span></span> \]\]\] )

<span
class="function">Memcache::getStats</span>返回一个关联数据的服务器统计信息。数组key是统计信息名，
值就是统计信息的值。同样你可以使用函数<span
class="function">memcache\_get\_stats</span>。

### 参数

`type`  
期望抓取的统计信息类型，可以使用的值有{reset, malloc, maps, cachedump,
slabs, items, sizes}。
通过memcached协议指定这些附加参数是为了方便memcache开发者(检查其中的变动)。

`slabid`  
用于与参数`type`联合从指定slab分块拷贝数据，cachedump命令会完全占用服务器通常用于
比较严格的调试。

`limit`  
用于和参数`type`联合来设置cachedump时从服务端获取的实体条数。

### 返回值

返回关联数组表示的服务器统计信息 或者在失败时返回 **`FALSE`**

### 参见

-   <span class="function">Memcache::getVersion</span>
-   <span class="function">Memcache::getExtendedStats</span>

Memcache::getVersion
====================

返回服务器版本信息

### 说明

<span class="type">string</span> <span
class="methodname">Memcache::getVersion</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcache::getVersion</span>返回一个字符串表示的服务端版本号。
同样你也可以使用函数<span
class="function">memcache\_get\_version</span>。

### 返回值

返回服务端版本号 或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">Memcache::getVersion</span> 示例**

``` php
<?php

/* OO API */
$memcache = new Memcache;
$memcache->connect('memcache_host', 11211);
echo $memcache->getVersion();

/* procedural API */
$memcache = memcache_connect('memcache_host', 11211);
echo memcache_get_version($memcache);

?>
```

### 参见

-   <span class="function">Memcache::getExtendedStats</span>
-   <span class="function">Memcache::getStats</span>

Memcache::increment
===================

增加一个元素的值

### 说明

<span class="type">int</span> <span
class="methodname">Memcache::increment</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$value`<span
class="initializer"> = 1</span></span> \] )

<span
class="function">Memcache::increment</span>将指定元素的值增加`value`。如果指定的`key`
对应的元素不是数值类型并且不能被转换为数值， 会将此值修改为`value`.
<span class="function">Memcache::increment</span>
*不会*在key对应元素不存在时创建元素。

> **Note**:
>
> 不要在经过压缩存储的元素上使用<span
> class="function">Memcache::increment</span>，因为这样作会导致后续对<span
> class="function">Memcache::get</span>的调用失败。

同样你也可以使用函数<span class="function">memcache\_increment</span>。

### 参数

`key`  
将要增加值的元素的key。

`value`  
参数`value`表明要将指定元素值增加多少。

### 返回值

成功时返回新的元素值 或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">Memcache::increment</span>示例**

``` php
<?php

/* procedural API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/* increment counter by 2 */
$current_value = memcache_increment($memcache_obj, 'counter', 2);

/* OO API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/* increment counter by 3 */
$current_value = $memcache_obj->increment('counter', 3);

?>
```

### 参见

-   <span class="function">Memcache::decrement</span>
-   <span class="function">Memcache::replace</span>

Memcache::pconnect
==================

打开一个到服务器的持久化连接

### 说明

<span class="type">mixed</span> <span
class="methodname">Memcache::pconnect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \]\] )

<span class="function">Memcache::pconnect</span>和 <span
class="function">Memcache::connect</span>非常类似，不同点在于这里建立的连接是持久化的。
这个连接不会在脚本执行结束后或者<span
class="function">Memcache::close</span>被调用后关闭。
同样你也可以使用函数<span class="function">memcache\_pconnect</span>。

### 参数

`host`  
服务端监听的主机地址。这个参数还可以指定为其他传输方式比如*unix:///path/to/memcached.sock*
来使用Unix域套接字，使用这种方式`port`参数必须设置为*0*。

`port`  
服务端监听的端口号。使用Unix域套接字的时候需要将这个参数设置为*0*。

`timeout`  
连接持续（超时）时间，单位秒。默认值1秒，修改此值之前请三思，过长的连接持续时间可能会导致失去所有的缓存优势。

### 返回值

返回一个 Memcache 对象 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">Memcache::pconnect</span>示例**

``` php
<?php

/* procedural API */
$memcache_obj = memcache_pconnect('memcache_host', 11211);

/* OO API */

$memcache_obj = new Memcache;
$memcache_obj->pconnect('memcache_host', 11211);

?>
```

### 参见

-   <span class="function">Memcache::connect</span>

Memcache::replace
=================

替换已经存在的元素的值

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::replace</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flag`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expire`</span> \]\] )

<span
class="function">Memcache::replace</span>通过`key`来查找元素并替换其值。当key
对应的元素不存在时，<span
class="function">Memcache::replace</span>返回**`FALSE`**。其他方面<span
class="function">Memcache::replace</span> 的行为和<span
class="function">Memcache::set</span>一样。 同样你也可以使用函数<span
class="function">memcache\_replace</span>。

### 参数

`key`  
期望替换值的元素的key。

`var`  
将要存储的新的值，字符串和数值直接存储，其他类型序列化后存储。

`flag`  
使用**`MEMCACHE_COMPRESSED`**指定对值进行压缩(使用zlib)。

`expire`  
当前写入缓存的数据的失效时间。如果此值设置为0表明此数据永不过期。你可以设置一个UNIX时间戳或
以秒为单位的整数（从当前算起的时间差）来说明此数据的过期时间，但是在后一种设置方式中，不能超过
2592000秒（30天）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::replace</span>示例**

``` php
<?php

$memcache_obj = memcache_connect('memcache_host', 11211);

/* procedural API */
memcache_replace($memcache_obj, "test_key", "some variable", false, 30);

/* OO API */
$memcache_obj->replace("test_key", "some variable", false, 30);

?>
```

### 参见

-   <span class="function">Memcache::set</span>
-   <span class="function">Memcache::add</span>

Memcache::set
=============

Store data at the server

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::set</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flag`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expire`</span> \]\] )

<span class="function">Memcache::set</span>向`key`存储一个元素值为
`var`。参数`expire`是以秒为单位的失效时间，
如果设置为0表明该元素永不过期（但是它可能会因为为了给其他项分配空间而被删除）。如果你希望存储的元素
经过压缩（使用zlib），你可以设置`flag`的值为**`MEMCACHE_COMPRESSED`**。

> **Note**:
>
> 谨记：资源类型变量（比如文件或连接）不能被存储在缓存中，因为它们在序列化状态不能被完整描述。

同样你也可以使用函数<span class="function">memcache\_set</span>。

### 参数

`key`  
要设置值的key。

`var`  
要存储的值，字符串和数值直接存储，其他类型序列化后存储。

`flag`  
使用**`MEMCACHE_COMPRESSED`**指定对值进行压缩(使用zlib)。

`expire`  
当前写入缓存的数据的失效时间。如果此值设置为0表明此数据永不过期。你可以设置一个UNIX时间戳或
以秒为单位的整数（从当前算起的时间差）来说明此数据的过期时间，但是在后一种设置方式中，不能超过
2592000秒（30天）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::set</span> 示例**

``` php
<?php
/* procedural API */

/* connect to memcached server */
$memcache_obj = memcache_connect('memcache_host', 11211);

/*
设置'var_key'对应存储的值
flag参数使用0,值没有经过压缩
失效时间为30秒
*/
memcache_set($memcache_obj, 'var_key', 'some variable', 0, 30);

echo memcache_get($memcache_obj, 'var_key');

?>
```

**示例 \#2 <span class="function">Memcache::set</span> 示例**

``` php
<?php
/* OO API */

$memcache_obj = new Memcache;

/* connect to memcached server */
$memcache_obj->connect('memcache_host', 11211);

/*
设置'var_key'对应值，使用即时压缩
失效时间为50秒
*/
$memcache_obj->set('var_key', 'some really big variable', MEMCACHE_COMPRESSED, 50);

echo $memcache_obj->get('var_key');

?>
```

### 参见

-   <span class="function">Memcache::add</span>
-   <span class="function">Memcache::replace</span>

Memcache::setCompressThreshold
==============================

开启大值自动压缩

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::setCompressThreshold</span> ( <span
class="methodparam"><span class="type">int</span> `$threshold`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$min_savings`</span> \] )

<span
class="function">Memcache::setCompressThreshold</span>开启对于大值的自动压缩。
同样你也可以使用函数<span
class="function">memcache\_set\_compress\_threshold</span>。

> **Note**:
>
> 此函数在memcache2.0.0加入。

### 参数

`threshold`  
控制多大值进行自动压缩的阈值。

`min_saving`  
指定经过压缩实际存储的值的压缩率，支持的值必须在0和1之间。默认值是0.2表示20%压缩率。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::setCompressThreshold</span>
示例**

``` php
<?php

/* OO API */

$memcache_obj = new Memcache;
$memcache_obj->addServer('memcache_host', 11211);
$memcache_obj->setCompressThreshold(20000, 0.2);

/* procedural API */

$memcache_obj = memcache_connect('memcache_host', 11211);
memcache_set_compress_threshold($memcache_obj, 20000, 0.2);

?>
```

Memcache::setServerParams
=========================

运行时修改服务器参数和状态

### 说明

<span class="type">bool</span> <span
class="methodname">Memcache::setServerParams</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 11211</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$retry_interval`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$status`</span> \[, <span class="methodparam"><span
class="type">callback</span> `$failure_callback`</span> \]\]\]\]\] )

<span
class="function">Memcache::setServerParams</span>用于运行时修改服务器参数。
同样你可以使用函数<span
class="function">memcache\_set\_server\_params</span>。

> **Note**:
>
> 在memcache2.1.0加入。

### 参数

`host`  
服务端监听地址。

`port`  
服务端监听端口。

`timeout`  
连接持续（超时）时间（单位秒），默认值1秒，修改此值之前请三思，过长的连接持续时间可能会导致失去所有的缓存优势。

`retry_interval`  
服务器连接失败时重试的间隔时间，默认值15秒。如果此参数设置为-1表示不重试。此参数和`persistent`参数在扩展以
<span class="function">dl</span>函数动态加载的时候无效。

`status`  
控制此服务器是否可以被标记为在线状态。设置此参数值为**`FALSE`**并且`retry_interval`参数
设置为-1时允许将失败的服务器保留在一个池中以免影响key的分配算法。对于这个服务器的请求会进行故障转移或者立即失败，
这受限于`memcache.allow_failover`参数的设置。该参数默认**`TRUE`**，表明允许进行故障转移。

`failure_callback`  
允许用户指定一个运行时发生错误后的回调函数。回调函数会在故障转移之前运行。回调函数会接受到两个参数，分别是失败主机的
主机名和端口号。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcache::setServerParams</span>
示例**

``` php
<?php

function _callback_memcache_failure($host, $port) {
    print "memcache '$host:$port' failed";
}

/* OO API */

$memcache = new Memcache;

// 增加一台离线服务器
$memcache->addServer('memcache_host', 11211, false, 1, 1, -1, false);

// 使该服务器变为在线状态
$memcache->setServerParams('memcache_host', 11211, 1, 15, true, '_callback_memcache_failure');

/* procedural API */

$memcache_obj = memcache_connect('memcache_host', 11211);
memcache_set_server_params($memcache_obj, 'memcache_host', 11211, 1, 15, true, '_callback_memcache_failure');

?>
```

### 参见

-   <span class="function">Memcache::addServer</span>
-   <span class="function">Memcache::getServerStatus</span>
