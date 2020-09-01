Memcached
=========

**目录**

-   [简介](/intro/memcached.html)
-   [安装／配置](/memcached/setup.html)
    -   [需求](/memcached/setup.html#需求)
    -   [安装](/memcached/setup.html#安装)
    -   [运行时配置](/memcached/setup.html#运行时配置)
    -   [资源类型](/memcached/setup.html#资源类型)
-   [预定义常量](/memcached/constants.html)
-   [超时时间](/memcached/expiration.html)
-   [回调](/memcached/callbacks.html)
    -   [结果回调](/memcached/callbacks.html#结果回调)
    -   [通读缓存回调](/memcached/callbacks.html#通读缓存回调)
-   [Sessions支持](/memcached/sessions.html)
-   [Memcached](/class/memcached.html) — Memcached类
    -   [Memcached::add](/class/memcached.html#Memcached::add) —
        向一个新的key下面增加一个元素
    -   [Memcached::addByKey](/class/memcached.html#Memcached::addByKey)
        — 在指定服务器上的一个新的key下增加一个元素
    -   [Memcached::addServer](/class/memcached.html#Memcached::addServer)
        — 向服务器池中增加一个服务器
    -   [Memcached::addServers](/class/memcached.html#Memcached::addServers)
        — 向服务器池中增加多台服务器
    -   [Memcached::append](/class/memcached.html#Memcached::append) —
        向已存在元素后追加数据
    -   [Memcached::appendByKey](/class/memcached.html#Memcached::appendByKey)
        — 向指定服务器上已存在元素后追加数据
    -   [Memcached::cas](/class/memcached.html#Memcached::cas) —
        比较并交换值
    -   [Memcached::casByKey](/class/memcached.html#Memcached::casByKey)
        — 在指定服务器上比较并交换值
    -   [Memcached::\_\_construct](/class/memcached.html#Memcached::__construct)
        — 创建一个Memcached实例
    -   [Memcached::decrement](/class/memcached.html#Memcached::decrement)
        — 减小数值元素的值
    -   [Memcached::decrementByKey](/class/memcached.html#Memcached::decrementByKey)
        — Decrement numeric item's value, stored on a specific server
    -   [Memcached::delete](/class/memcached.html#Memcached::delete) —
        删除一个元素
    -   [Memcached::deleteByKey](/class/memcached.html#Memcached::deleteByKey)
        — 从指定的服务器删除一个元素
    -   [Memcached::deleteMulti](/class/memcached.html#Memcached::deleteMulti)
        — Delete multiple items
    -   [Memcached::deleteMultiByKey](/class/memcached.html#Memcached::deleteMultiByKey)
        — Delete multiple items from a specific server
    -   [Memcached::fetch](/class/memcached.html#Memcached::fetch) —
        抓取下一个结果
    -   [Memcached::fetchAll](/class/memcached.html#Memcached::fetchAll)
        — 抓取所有剩余的结果
    -   [Memcached::flush](/class/memcached.html#Memcached::flush) —
        作废缓存中的所有元素
    -   [Memcached::get](/class/memcached.html#Memcached::get) —
        检索一个元素
    -   [Memcached::getAllKeys](/class/memcached.html#Memcached::getAllKeys)
        — Gets the keys stored on all the servers
    -   [Memcached::getByKey](/class/memcached.html#Memcached::getByKey)
        — 从特定的服务器检索元素
    -   [Memcached::getDelayed](/class/memcached.html#Memcached::getDelayed)
        — 请求多个元素
    -   [Memcached::getDelayedByKey](/class/memcached.html#Memcached::getDelayedByKey)
        — 从指定的服务器上请求多个元素
    -   [Memcached::getMulti](/class/memcached.html#Memcached::getMulti)
        — 检索多个元素
    -   [Memcached::getMultiByKey](/class/memcached.html#Memcached::getMultiByKey)
        — 从特定服务器检索多个元素
    -   [Memcached::getOption](/class/memcached.html#Memcached::getOption)
        — 获取Memcached的选项值
    -   [Memcached::getResultCode](/class/memcached.html#Memcached::getResultCode)
        — 返回最后一次操作的结果代码
    -   [Memcached::getResultMessage](/class/memcached.html#Memcached::getResultMessage)
        — 返回最后一次操作的结果描述消息
    -   [Memcached::getServerByKey](/class/memcached.html#Memcached::getServerByKey)
        — 获取一个key所映射的服务器信息
    -   [Memcached::getServerList](/class/memcached.html#Memcached::getServerList)
        — 获取服务器池中的服务器列表
    -   [Memcached::getStats](/class/memcached.html#Memcached::getStats)
        — 获取服务器池的统计信息
    -   [Memcached::getVersion](/class/memcached.html#Memcached::getVersion)
        — 获取服务器池中所有服务器的版本信息
    -   [Memcached::increment](/class/memcached.html#Memcached::increment)
        — 增加数值元素的值
    -   [Memcached::incrementByKey](/class/memcached.html#Memcached::incrementByKey)
        — Increment numeric item's value, stored on a specific server
    -   [Memcached::isPersistent](/class/memcached.html#Memcached::isPersistent)
        — Check if a persitent connection to memcache is being used
    -   [Memcached::isPristine](/class/memcached.html#Memcached::isPristine)
        — Check if the instance was recently created
    -   [Memcached::prepend](/class/memcached.html#Memcached::prepend) —
        向一个已存在的元素前面追加数据
    -   [Memcached::prependByKey](/class/memcached.html#Memcached::prependByKey)
        — Prepend data to an existing item on a specific server
    -   [Memcached::quit](/class/memcached.html#Memcached::quit) —
        关闭所有打开的链接。
    -   [Memcached::replace](/class/memcached.html#Memcached::replace) —
        替换已存在key下的元素
    -   [Memcached::replaceByKey](/class/memcached.html#Memcached::replaceByKey)
        — Replace the item under an existing key on a specific server
    -   [Memcached::resetServerList](/class/memcached.html#Memcached::resetServerList)
        — Clears all servers from the server list
    -   [Memcached::set](/class/memcached.html#Memcached::set) —
        存储一个元素
    -   [Memcached::setByKey](/class/memcached.html#Memcached::setByKey)
        — Store an item on a specific server
    -   [Memcached::setMulti](/class/memcached.html#Memcached::setMulti)
        — 存储多个元素
    -   [Memcached::setMultiByKey](/class/memcached.html#Memcached::setMultiByKey)
        — Store multiple items on a specific server
    -   [Memcached::setOption](/class/memcached.html#Memcached::setOption)
        — 设置一个memcached选项
    -   [Memcached::setOptions](/class/memcached.html#Memcached::setOptions)
        — Set Memcached options
    -   [Memcached::setSaslAuthData](/class/memcached.html#Memcached::setSaslAuthData)
        — Set the credentials to use for authentication
    -   [Memcached::touch](/class/memcached.html#Memcached::touch) — Set
        a new expiration on an item
    -   [Memcached::touchByKey](/class/memcached.html#Memcached::touchByKey)
        — Set a new expiration on an item on a specific server

简介
----

表征到memcached服务集群的连接。

类摘要
------

**Memcached**

<span class="ooclass"> class **Memcached** </span> {

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$persistent_id`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServer</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$weight`<span class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServers</span> ( <span
class="methodparam"><span class="type">array</span> `$servers`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">append</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">appendByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">cas</span> ( <span class="methodparam"><span
class="type">float</span> `$cas_token`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">casByKey</span> ( <span
class="methodparam"><span class="type">float</span> `$cas_token`</span>
, <span class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">decrement</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">decrementByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$initial_value`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$expiry`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delete</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">deleteByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">deleteMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">deleteMultiByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">fetch</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">fetchAll</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">flush</span> (\[ <span
class="methodparam"><span class="type">int</span> `$delay`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">callback</span>
`$cache_cb`</span> \[, <span class="methodparam"><span
class="type">float</span> `&$cas_token`</span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getAllKeys</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">callback</span>
`$cache_cb`</span> \[, <span class="methodparam"><span
class="type">float</span> `&$cas_token`</span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getDelayed</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_cas`</span> \[, <span class="methodparam"><span
class="type">callback</span> `$value_cb`</span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getDelayedByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$with_cas`</span>
\[, <span class="methodparam"><span class="type">callback</span>
`$value_cb`</span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getMultiByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">string</span>
`&$cas_tokens`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`</span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getOption</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getResultCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getResultMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getServerByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getServerList</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getStats</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">increment</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">incrementByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$initial_value`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$expiry`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPersistent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPristine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">prepend</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">prependByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">quit</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">replace</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">replaceByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">resetServerList</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$items`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setMultiByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$items`</span> \[, <span
class="methodparam"><span class="type">int</span> `$expiration`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOption</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOptions</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSaslAuthData</span> ( <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">touch</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">int</span> `$expiration`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">touchByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">int</span> `$expiration`</span> )

}

Memcached::add
==============

向一个新的key下面增加一个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::add</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expiration`</span> \] )

<span class="function">Memcached::add</span>与 <span
class="methodname">Memcached::set</span>类似，但是如果
`key`已经在服务端存在，此操作会失败。

### 参数

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key已经存在，
<span
class="methodname">Memcached::getResultCode</span>方法将会返回**`Memcached::RES_NOTSTORED`**。

### 参见

-   <span class="methodname">Memcached::addByKey</span>
-   <span class="methodname">Memcached::set</span>
-   <span class="methodname">Memcached::replace</span>

Memcached::addByKey
===================

在指定服务器上的一个新的key下增加一个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::addByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="function">Memcached::addByKey</span>在功能上等同于 <span
class="methodname">Memcached::add</span>，
不过这种方式可以自由的指定`server_key`用于将`key`
映射到特定的服务器。这在你需要将一些相关联的key保存在一个特定的服务器时非常有用。(译注:
$server\_key也是一个普通的key, \*ByKey系列接口的工作过程是: 首先,
对$server\_key进行hash, 得到$server\_key应该存储的服务器,
然后将相应的操作在 $server\_key所在的服务器上进行.)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key已经存在，
<span
class="methodname">Memcached::getResultCode</span>方法将会返回**`Memcached::RES_NOTSTORED`**。

### 参见

-   <span class="methodname">Memcached::add</span>
-   <span class="methodname">Memcached::set</span>
-   <span class="methodname">Memcached::replace</span>

Memcached::addServer
====================

向服务器池中增加一个服务器

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::addServer</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$weight`<span class="initializer"> = 0</span></span> \] )

<span
class="function">Memcached::addServer</span>增加指定服务器到服务器池中。此时不会建立与服务端的连接，
但是，如果你使用一致性key分布选项（**`Memcached::DISTRIBUTION_CONSISTENT`**或
**`Memcached::OPT_LIBKETAMA_COMPATIBLE`**），一些内部的数据结构将会被更新。
因此，如果你需要增加多台服务器，更好的方式是使用 <span
class="methodname">Memcached::addServers</span>
以确保这种更新只发生一次。

同一台服务器可以在服务器池中多次出现，因为这里没有做重复检测。但这是不推荐的做法，对于期望提高某台服务器
权重的需求，请使用`weight`参数。

### 参数

`host`  
memcached服务端主机名。如果主机名无效，相关的数据操作的返回代码将被设置为**`Memcached::RES_HOST_LOOKUP_FAILURE`**。

`port`  
memcached服务端端口号，通常是*11211*。

`weight`  
此服务器相对于服务器池中所有服务器的权重。此参数用来控制服务器在操作时被选种的概率。这个仅用于一致性
分布选项，并且这个值通常是由服务端分配的内存来设置的。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcached::addServer</span> example**

``` php
<?php
$m = new Memcached();

/* Add 2 servers, so that the second one
   is twice as likely to be selected. */
$m->addServer('mem1.domain.com', 11211, 33);
$m->addServer('mem2.domain.com', 11211, 67);
?>
```

### 参见

-   <span class="methodname">Memcached::addServers</span>

Memcached::addServers
=====================

向服务器池中增加多台服务器

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::addServers</span> ( <span
class="methodparam"><span class="type">array</span> `$servers`</span> )

<span
class="function">Memcached::addServers</span>向服务器池中增加`servers`参数指定的服务器。
`servers`中的每一条都是一个包含主机名，端口以及可选的权重等服务器参数。此时并不会与这些服务端建立
连接。

同一台服务器可以在服务器池中多次出现，因为这里没有做重复检测。但这是不推荐的做法，对于期望提高某台服务器
权重的需求，请使用`weight`参数。

### 参数

`array`  
将要增加到池中的服务器列表数组。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcached::addServers</span>示例**

``` php
<?php
$m = new Memcached();

$servers = array(
    array('mem1.domain.com', 11211, 33),
    array('mem2.domain.com', 11211, 67)
);
$m->addServers($servers);
?>
```

### 参见

-   <span class="methodname">Memcached::addServer</span>

Memcached::append
=================

向已存在元素后追加数据

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::append</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span
class="function">Memcached::append</span>向已经存在的元素后追加`value`参数对应的字符串值。
`value`被强制转换成字符串类型主要是因为对于mix类型的追加没有很好的定义。

> **Note**:
>
> 如果**`Memcached::OPT_COMPRESSION`**常量开启，这个操作会失败，并引发一个警告，因为向压缩数据
> 后追加数据可能会导致解压不了。

### 参数

`key`  
用于存储值的键名。

`value`  
将要追加的值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>将返回**`Memcached::RES_NOTSTORED`**。

### 范例

**示例 \#1 <span class="function">Memcached::append</span>示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$m->setOption(Memcached::OPT_COMPRESSION, false);

$m->set('foo', 'abc');
$m->append('foo', 'def');
var_dump($m->get('foo'));
?>
```

以上例程会输出：

    string(6) "abcdef"

### 参见

-   <span class="methodname">Memcached::appendByKey</span>
-   <span class="methodname">Memcached::prepend</span>

Memcached::appendByKey
======================

向指定服务器上已存在元素后追加数据

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::appendByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

除了可以使用`server_key`自由的将`key`映射到指定服务器外， <span
class="function">Memcached::appendByKey</span>在功能上等同于 <span
class="methodname">Memcached::append</span>。 (译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
用于存储值的键名。

`value`  
要追加的字符串。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span class="methodname">Memcached::getResultCode</span>将返回
**`Memcached::RES_NOTSTORED`**。

### 参见

-   <span class="methodname">Memcached::append</span>
-   <span class="methodname">Memcached::prepend</span>

Memcached::cas
==============

比较并交换值

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::cas</span> ( <span
class="methodparam"><span class="type">float</span> `$cas_token`</span>
, <span class="methodparam"><span class="type">string</span>
`$key`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$expiration`</span>
\] )

<span
class="function">Memcached::cas</span>执行一个“检查并设置”的操作，因此，它仅在当前客户端最后一次取值后，该key
对应的值没有被其他客户端修改的情况下，
才能够将值写入。检查是通过`cas_token`参数进行的，
这个参数是Memcach指定给已经存在的元素的一个唯一的64位值，
怎样获取这个值请查看 <span class="methodname">Memcached::get\*</span>
系列方法的文档。注意：这个值作为double类型是因为PHP的整型空间限制。

译注：这是Memcached扩展比Memcache扩展一个非常重要的优势，
在这样一个系统级（Memcache自身提供）的冲突检测机制（乐观锁）下，
我们才能保证高并发下的数据安全。

### 参数

`cas_token`  
与已存在元素关联的唯一的值，由Memcache生成。

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
如果在元素尝试存储时发现在本客户端最后一次获取后被其他客户端修改， <span
class="methodname">Memcached::getResultCode</span>
将返回**`Memcached::RES_DATA_EXISTS`**。

### 范例

**示例 \#1 <span class="function">Memcached::cas</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

do {
    /* 获取ip列表以及它的标记 */
    $ips = $m->get('ip_block', null, $cas);
    /* 如果列表不存在， 创建并进行一个原子添加（如果其他客户端已经添加， 这里就返回false）*/
    if ($m->getResultCode() == Memcached::RES_NOTFOUND) {
        $ips = array($_SERVER['REMOTE_ADDR']);
        $m->add('ip_block', $ips);
    /* 其他情况下，添加ip到列表中， 并以cas方式去存储， 这样当其他客户端修改过， 则返回false */
    } else { 
        $ips[] = $_SERVER['REMOTE_ADDR'];
        $m->cas($cas, 'ip_block', $ips);
    }   
} while ($m->getResultCode() != Memcached::RES_SUCCESS);

?>
```

### 参见

-   <span class="methodname">Memcached::casByKey</span>

Memcached::casByKey
===================

在指定服务器上比较并交换值

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::casByKey</span> ( <span
class="methodparam"><span class="type">float</span> `$cas_token`</span>
, <span class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

除了可以使用`server_key`将`key`自由的映射到指定服务器外， <span
class="function">Memcached::casByKey</span>和 <span
class="methodname">Memcached::cas</span>在功能上是等同的。
这通常用于你需要保持一批相关的key在一个中心服务器上的情况。(译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`cas_token`  
与已存在元素关联的唯一的值，由Memcache生成。

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
如果在元素尝试存储时发现在本客户端最后一次获取后被其他客户端修改， <span
class="methodname">Memcached::getResultCode</span>
将返回**`Memcached::RES_DATA_EXISTS`**。

### 参见

-   <span class="methodname">Memcached::cas</span>

Memcached::\_\_construct
========================

创建一个Memcached实例

### 说明

<span class="methodname">Memcached::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$persistent_id`</span> \] )

创建一个代表到Memcached服务端连接的Memcached实例。

### 参数

`persistent_id`  
默认情况下，Memcached实例在请求结束后会被销毁。但可以在创建时通过`persistent_id`为每个实例指定唯一的ID，
在请求间共享实例。所有通过相同的`persistent_id`值创建的实例共享同一个连接。

### 返回值

一个Memcached对象。

### 范例

**示例 \#1 创建一个Memcached对象**

``` php
<?php
/* 创建一个普通的对象 */
$m1 = new Memcached();
echo get_class($m);

/* 创建持久化对象 */
$m2 = new Memcached('story_pool');
$m3 = new Memcached('story_pool');

/* 现在$m2和$m3共享相同的连接 */
?>
```

Memcached::decrement
====================

减小数值元素的值

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Memcached::decrement</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \] )

<span
class="function">Memcached::decrement</span>减小一个数值元素的值，减小多少由参数`offset`决定。
如果元素的值不是数值，以0值对待。如果减小后的值小于0,则新的值被设置为0.如果元素不存在，<span
class="function">Memcached::decrement</span> 失败。

### 参数

`key`  
将要减小值的元素的key。

`offset`  
要将减小指定元素的值减小多少。

### 返回值

成功时返回元素新的值， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTFOUND`**。

### 范例

**示例 \#1 <span class="function">Memcached::decrement</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('counter', 5);
$m->decrement('counter');
var_dump($m->get('counter'));

$m->decrement('counter', 10);
var_dump($m->get('counter'));
?>
```

以上例程会输出：

    int(4)
    int(0)

### 参见

-   <span class="methodname">Memcached::increment</span>

Memcached::decrementByKey
=========================

Decrement numeric item's value, stored on a specific server

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Memcached::decrementByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$initial_value`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$expiry`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="function">Memcached::decrementByKey</span> decrements a
numeric item's value by the specified `offset`. If the item's value is
not numeric, an error will result. If the operation would decrease the
value below 0, the new value will be 0. <span
class="function">Memcached::decrementByKey</span> will set the item to
the `initial_value` parameter if the key doesn't exist.

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
The key of the item to decrement.

`offset`  
The amount by which to decrement the item's value.

`initial_value`  
The value to set the item to if it doesn't currently exist.

`expiry`  
The expiry time to set on the item.

### 返回值

Returns item's new value on success 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">Memcached::decrement</span>
-   <span class="methodname">Memcached::increment</span>
-   <span class="methodname">Memcached::incrementByKey</span>

Memcached::delete
=================

删除一个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::delete</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span
class="function">Memcached::delete</span>从服务端删除`key`对应的元素.
参数`time`是一个秒为单位的时间(或一个UNIX时间戳表明直到那个时间),
用来表明 客户端希望服务端在这段时间拒绝对这个key的*add*和*replace*命令.
由于这个时间段的存在, 元素被放入一个删除队列,
表明它不可以通过*get*命令获取到值, 但是同时
*add*和*replace*命令也会失败(无论如何*set*命令都会成功).
在这段时间过去后,
元素最终被从服务端内存删除.`time`参数默认0(表明元素会被立即删除并且之后对这个
key的存储命令也会成功).

### 参数

`key`  
要删除的key

`time`  
服务端等待删除该元素的总时间(或一个Unix时间戳表明的实际删除时间).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在,
<span
class="methodname">Memcached::getResultCode</span>将会返回**`Memcached::RES_NOTFOUND`**.

### 范例

**示例 \#1 <span class="function">Memcached::delete</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->delete('key1');
?>
```

### 参见

-   <span class="methodname">Memcached::deleteByKey</span>

Memcached::deleteByKey
======================

从指定的服务器删除一个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::deleteByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span
class="function">Memcached::deleteByKey</span>除了可以通过`server_key`参数自由的指定`key`
所映射的服务器外， 在功能上等同于 <span
class="methodname">Memcached::delete</span>。(译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
要删除的key。

`time`  
服务端等待删除该元素的总时间(或一个Unix时间戳表明的实际删除时间).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTFOUND`**。

### 参见

-   <span class="methodname">Memcached::delete</span>

Memcached::deleteMulti
======================

Delete multiple items

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::deleteMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span class="function">Memcached::deleteMulti</span> deletes the array
of `keys` from the server. The `time` parameter is the amount of time in
seconds (or Unix time until which) the client wishes the server to
refuse *add* and *replace* commands for these keys. For this amount of
time, the item is put into a delete queue, which means that it won't be
possible to retrieve it by the *get* command, but *add* and *replace*
command with these keys will also fail (the *set* command will succeed,
however). After the time passes, the item is finally deleted from server
memory. The parameter `time` defaults to 0 (which means that the item
will be deleted immediately and further storage commands with these keys
will succeed).

### 参数

`keys`  
The keys to be deleted.

`time`  
The amount of time the server will wait to delete the items.

### 返回值

Returns array indexed by `keys` and where values are indicating whether
operation succeeded or not. The <span
class="methodname">Memcached::getResultCode</span> will return
**`Memcached::RES_NOTFOUND`** if the key does not exist.

### 参见

-   <span class="methodname">Memcached::delete</span>
-   <span class="methodname">Memcached::deleteByKey</span>
-   <span class="methodname">Memcached::deleteMultiByKey</span>

Memcached::deleteMultiByKey
===========================

Delete multiple items from a specific server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::deleteMultiByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">int</span> `$time`<span
class="initializer"> = 0</span></span> \] )

<span class="function">Memcached::deleteMultiByKey</span> is
functionally equivalent to <span
class="methodname">Memcached::deleteMulti</span>, except that the
free-form `server_key` can be used to map the `keys` to a specific
server.

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`keys`  
The keys to be deleted.

`time`  
The amount of time the server will wait to delete the items.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 The <span
class="methodname">Memcached::getResultCode</span> will return
**`Memcached::RES_NOTFOUND`** if the key does not exist.

### 参见

-   <span class="methodname">Memcached::delete</span>
-   <span class="methodname">Memcached::deleteByKey</span>
-   <span class="methodname">Memcached::deleteMulti</span>

Memcached::fetch
================

抓取下一个结果

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::fetch</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::fetch</span>从最后一次请求中抓取下一个结果。

### 参数

此函数没有参数。

### 返回值

返回下一个结果或其他情况下返回**`FALSE`**。 如果结果集已经抓取完毕，
<span
class="methodname">Memcached::getResultCode</span>将返回**`Memcached::RES_END`**。

### 范例

**示例 \#1 <span class="function">Memcached::fetch</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));

//延迟的获取int和array这两个key的值
$m->getDelayed(array('int', 'array'), true);
//循环抓取上面的延迟抓取得到的结果
while ($result = $m->fetch()) {
    var_dump($result);
}
?>
```

以上例程的输出类似于：

    array(3) {
      ["key"]=>
      string(3) "int"
      "value"]=>
      int(99)
      ["cas"]=>
      float(2363)
    }
    array(3) {
      ["key"]=>
      string(5) "array"
      ["value"]=>
      array(2) {
        [0]=>
        int(11)
        [1]=>
        int(12)
      }
      ["cas"]=>
      float(2365)
    }

### 参见

-   <span class="methodname">Memcached::fetchAll</span>
-   <span class="methodname">Memcached::getDelayed</span>

Memcached::fetchAll
===================

抓取所有剩余的结果

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::fetchAll</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::fetchAll</span>抓取最后一次请求的结果集中剩余的所有结果。需要注意的是fetchAll和fetch的返回不同，
因为fetchAll抓取的是结果集中剩余所有元素， 所以比fetch的结果多一个维度。

### 参数

此函数没有参数。

### 返回值

返回结果集 或者在失败时返回 **`FALSE`**. 如需要则使用 <span
class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::getDelayed</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));

//延迟抓取int和array两个key的值
$m->getDelayed(array('int', 'array'), true);
//抓取上面delay抓取的所有结果
var_dump($m->fetchAll());
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      array(3) {
        ["key"]=>
        string(3) "int"
        ["value"]=>
        int(99)
        ["cas"]=>
        float(2363)
      }
      [1]=>
      array(3) {
        ["key"]=>
        string(5) "array"
        ["value"]=>
        array(2) {
          [0]=>
          int(11)
          [1]=>
          int(12)
        }
        ["cas"]=>
        float(2365)
      }
    }

### 参见

-   <span class="methodname">Memcached::fetch</span>
-   <span class="methodname">Memcached::getDelayed</span>

Memcached::flush
================

作废缓存中的所有元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::flush</span> (\[ <span
class="methodparam"><span class="type">int</span> `$delay`<span
class="initializer"> = 0</span></span> \] )

<span
class="function">Memcached::flush</span>立即（默认）或者在`delay`延迟后作废所有缓存中已经存在的元素。
在作废之后检索命令将不会有任何返回（除非在执行<span
class="function">Memcached::flush</span>作废之后，该key下被重新存储过）。flush不会
真正的释放已有元素的内存， 而是逐渐的存入新元素重用那些内存。

### 参数

`delay`  
在作废所有元素之前等待的时间（单位秒）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::flush</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

/* 10秒内清除所有元素 */
$m->flush(10);
?>
```

Memcached::get
==============

检索一个元素

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Memcached::get</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">callback</span>
`$cache_cb`</span> \[, <span class="methodparam"><span
class="type">float</span> `&$cas_token`</span> \]\] )

<span
class="function">Memcached::get</span>返回之前存储在`key`下的元素。如果元素被找到，并且提供
了`cas_token`参数，
这个参数（译注：这个参数在函数定义中是引用参数，用来传出元素的版本标记，原理
可以查阅乐观锁资料）将会包含该元素的CAS标记值。关于CAS标记值的使用，请查看
<span class="methodname">Memcached::cas</span>的说明。
另外，可以通过`cache_cb`参数设置<a href="/memcached/callbacks.html" class="link">Read-through caching callback</a>。

### 参数

`key`  
要检索的元素的key。

`cache_cb`  
通读缓存回掉函数或**`NULL`**.

`cas_token`  
检索的元素的CAS标记值。

### 返回值

返回存储在服务端的元素的值或者在其他情况下返回**`FALSE`**。
如果key不存在， <span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTFOUND`**。

### 范例

**示例 \#1 <span class="function">Memcached::get</span> 示例 \#1**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('foo', 100);
var_dump($m->get('foo'));
?>
```

以上例程会输出：

    int(100)

**示例 \#2 <span class="function">Memcached::get</span> 示例 \#2**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

if (!($ip = $m->get('ip_block'))) {
    if ($m->getResultCode() == Memcached::RES_NOTFOUND) {
        $ip = array();
        $m->set('ip_block', $ip);
    } else {
        /* log error */
        /* ...       */
    }
}
?>
```

### 参见

-   <span class="methodname">Memcached::getByKey</span>
-   <span class="methodname">Memcached::getMulti</span>
-   <span class="methodname">Memcached::getDelayed</span>

Memcached::getAllKeys
=====================

Gets the keys stored on all the servers

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::getAllKeys</span> ( <span
class="methodparam">void</span> )

<span class="function">Memcached::getAllKeys</span> queries each
memcache server and retrieves an array of all keys stored on them at
that point in time. This is not an atomic operation, so it isn't a truly
consistent snapshot of the keys at point in time. As memcache doesn't
guarantee to return all keys you also cannot assume that all keys have
been returned.

### 参数

此函数没有参数。

### 返回值

Returns the keys stored on all the servers on success 或者在失败时返回
**`FALSE`**.

Memcached::getByKey
===================

从特定的服务器检索元素

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Memcached::getByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">callback</span>
`$cache_cb`</span> \[, <span class="methodparam"><span
class="type">float</span> `&$cas_token`</span> \]\] )

<span
class="function">Memcached::getByKey</span>除了可以通过`server_key`参数自由的指定`key`
所映射的服务器外， 在功能上等同于 <span
class="methodname">Memcached::get</span>。(译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
要抓取的元素的key。

`cache_cb`  
通读缓存回掉函数或**`NULL`**.

`cas_token`  
检索的元素的CAS标记值。

### 返回值

返回存储在服务端的元素的值或者在其他情况下返回**`FALSE`**。
如果key不存在， <span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTFOUND`**。

### 参见

-   <span class="methodname">Memcached::get</span>
-   <span class="methodname">Memcached::getMulti</span>
-   <span class="methodname">Memcached::getDelayed</span>

Memcached::getDelayed
=====================

请求多个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::getDelayed</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_cas`</span> \[, <span class="methodparam"><span
class="type">callback</span> `$value_cb`</span> \]\] )

<span
class="function">Memcached::getDelayed</span>向Memcached服务端发出一个检索`keys`指定的多个
key对应元素的请求。这个方法不会等待响应而是立即返回。当你需要收集元素值时，
调用 <span class="methodname">Memcached::fetch</span>或 <span
class="methodname">Memcached::fetchAll</span>。如果`with_cas`设置为true，会同时请求每个元素的CAS标记。

可以通过参数`value_cb`指定一个<a href="/memcached/callbacks.html" class="link">result callback</a>来替代明确的抓取结果（fetch或fetchAll为明确抓取方式）。

### 参数

`keys`  
要请求的key的数组。

`with_cas`  
是否同时请求CAS标记。

`value_cb`  
结果回掉函数或**`NULL`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::getDelayed</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));

$m->getDelayed(array('int', 'array'), true);
var_dump($m->fetchAll());
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      array(3) {
        ["key"]=>
        string(3) "int"
        ["value"]=>
        int(99)
        ["cas"]=>
        float(2363)
      }
      [1]=>
      array(3) {
        ["key"]=>
        string(5) "array"
        ["value"]=>
        array(2) {
          [0]=>
          int(11)
          [1]=>
          int(12)
        }
        ["cas"]=>
        float(2365)
      }
    }

### 参见

-   <span class="methodname">Memcached::getDelayedByKey</span>
-   <span class="methodname">Memcached::fetch</span>
-   <span class="methodname">Memcached::fetchAll</span>

Memcached::getDelayedByKey
==========================

从指定的服务器上请求多个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::getDelayedByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$with_cas`</span>
\[, <span class="methodparam"><span class="type">callback</span>
`$value_cb`</span> \]\] )

<span
class="function">Memcached::getDelayedByKey</span>除了可以通过`server_key`参数自由的指定`key`
所映射的服务器外， 在功能上等同于 <span
class="methodname">Memcached::getDelayed</span>。(译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`keys`  
要请求的key的数组。

`with_cas`  
是否同时请求CAS标记。

`value_cb`  
结果回掉函数或**`NULL`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 参见

-   <span class="methodname">Memcached::getDelayed</span>
-   <span class="methodname">Memcached::fetch</span>
-   <span class="methodname">Memcached::fetchAll</span>

Memcached::getMulti
===================

检索多个元素

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Memcached::getMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\] )

<span class="function">Memcached::getMulti</span> 与 <span
class="methodname">Memcached::get</span> 类似，但是这个方法用来检索
`keys` 数组指定的多个 key 对应的元素。

> **Note**:
>
> 在 v3.0 之前，使用的第二个参数是 `&cas_tokens`。 它会填充进元素的 CAS
> token 值。 在本扩展里，`&cas_tokens` 参数在 v3.0 中已经移除。
> 它被新的附加选项（flag） **`Memcached::GET_EXTENDED`** 代替，需要在
> `flags` 值里使用。

`flags`参数可以用做指定<span
class="function">Memcached::getMulti</span>的附加选项。
当前，仅可以指定为**`Memcached::GET_PRESERVE_ORDER`**以保证返回的key的顺序和请求时一致。
**`Memcached::GET_EXTENDED`** 可以确保同时返回了 CAS token 信息。

### 参数

`keys`  
要检索的key的数组。

`flags`  
Get 操作的附加选项。

### 返回值

返回检索到的元素的数组 或者在失败时返回 **`FALSE`**. 如需要则使用 <span
class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::getMulti</span> 的
Memcached v3 示例**

``` php
<?php
// 扩展版本 v3 有效

$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$result = $m->getMulti(array('key1', 'key3', 'badkey'));
var_dump($result);
?>
```

以上例程的输出类似于：

    array(2) {
      ["key1"]=>
      string(6) "value1"
      ["key3"]=>
      string(6) "value3"
    }

**示例 \#2 <span class="function">Memcached::getMulti</span> 的
Memcached v1 和 v2 示例**

``` php
<?php
// 仅在扩展版本 v1 和 v2 中有效

$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$result = $m->getMulti(array('key1', 'key3', 'badkey'), $cas);
var_dump($result, $cas);
?>
```

以上例程的输出类似于：

    array(2) {
      ["key1"]=>
      string(6) "value1"
      ["key3"]=>
      string(6) "value3"
    }
    array(2) {
      ["key1"]=>
      float(2360)
      ["key3"]=>
      float(2362)
    }

**示例 \#3 **`Memcached::GET_PRESERVE_ORDER`** 的 Memcached v3 示例**

``` php
<?php
//  v3 扩展有效

$m = new Memcached();
$m->addServer('localhost', 11211);

$data = array(
    'foo' => 'foo-data',
    'bar' => 'bar-data',
    'baz' => 'baz-data',
    'lol' => 'lol-data',
    'kek' => 'kek-data',
);

$m->setMulti($data, 3600);

$keys = array_keys($data);
$keys[] = 'zoo';
$got = $m->getMulti($keys, Memcached::GET_PRESERVE_ORDER);

foreach ($got as $k => $v) {
    echo "$k $v\n";
}
?>
```

以上例程的输出类似于：

    foo foo-data
    bar bar-data
    baz baz-data
    lol lol-data
    kek kek-data
    zoo 

**示例 \#4 **`Memcached::GET_PRESERVE_ORDER`** 的 Memcached v1 和 v2
示例**

``` php
<?php
// 在扩展版本 v1 和 v2  中有效

$m = new Memcached();
$m->addServer('localhost', 11211);

$data = array(
    'foo' => 'foo-data',
    'bar' => 'bar-data',
    'baz' => 'baz-data',
    'lol' => 'lol-data',
    'kek' => 'kek-data',
);

$m->setMulti($data, 3600);

$null = null;
$keys = array_keys($data);
$keys[] = 'zoo';
$got = $m->getMulti($keys, $null, Memcached::GET_PRESERVE_ORDER);

foreach ($got as $k => $v) {
    echo "$k $v\n";
}
?>
```

以上例程的输出类似于：

    foo foo-data
    bar bar-data
    baz baz-data
    lol lol-data
    kek kek-data
    zoo 

### 更新日志

| 版本  | 说明                                                                                                     |
|-------|----------------------------------------------------------------------------------------------------------|
| 3.0.0 | 移出参数 `&cas_tokens`。 添加 **`Memcached::GET_EXTENDED`**，当需要获取 CAS token 信息时，传入 flag 中。 |

### 参见

-   <span class="methodname">Memcached::getMultiByKey</span>
-   <span class="methodname">Memcached::get</span>
-   <span class="methodname">Memcached::getDelayed</span>

Memcached::getMultiByKey
========================

从特定服务器检索多个元素

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::getMultiByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">string</span>
`&$cas_tokens`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`</span> \]\] )

<span
class="function">Memcached::getMultiByKey</span>除了可以通过`server_key`参数自由的指定`key`
所映射的服务器外， 在功能上等同于 <span
class="methodname">Memcached::getMulti</span>。(译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`keys`  
要检索的key的数组。

`cas_tokens`  
用来存储检索到的元素的CAS标记。

`flags`  
get操作的附加选项。

### 返回值

返回检索到的元素的数组 或者在失败时返回 **`FALSE`**. 如需要则使用 <span
class="methodname">Memcached::getResultCode</span>。

### 参见

-   <span class="methodname">Memcached::getMulti</span>
-   <span class="methodname">Memcached::get</span>
-   <span class="methodname">Memcached::getDelayed</span>

Memcached::getOption
====================

获取Memcached的选项值

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Memcached::getOption</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> )

这个方法返回`option`指定的Memcached选项的值。一些选项是和libmemcached中相对应的，
也有一些特殊的选项仅仅是扩展自身的。关于选项的更多信息请查看<a href="/memcached/constants.html" class="link">Memcached Constants</a>。

### 参数

`option`  
*Memcached::OPT\_\**系列常量中的一个。

### 返回值

返回请求的选项的值，或者在发生错误时返回*FALSE*。

### 范例

**示例 \#1 获取Memcached选项**

``` php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_COMPRESSION));
var_dump($m->getOption(Memcached::OPT_POLL_TIMEOUT));
?>
```

以上例程的输出类似于：

    bool(true)
    int(1000)

### 参见

-   <span class="methodname">Memcached::setOption</span>
-   <a href="/memcached/constants.html" class="link">Memcached Constants</a>

Memcached::getResultCode
========================

返回最后一次操作的结果代码

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Memcached::getResultCode</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::getResultCode</span>返回**`Memcached::RES_*`**系列常量中的一个来表明最后一次执行Memcached方法的结果。

### 参数

此函数没有参数。

### 返回值

最后一次Memcached操作的结果代码。

### 范例

**示例 \#1 <span class="function">Memcached::getResultCode</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->add('foo', 'bar');
if ($m->getResultCode() == Memcached::RES_NOTSTORED) {
    /* ... */
}
?>
```

Memcached::getResultMessage
===========================

返回最后一次操作的结果描述消息

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Memcached::getResultMessage</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::getResultMessage</span>返回一个字符串来描述最后一次Memcached方法执行的结果。

### 参数

此函数没有参数。

### 返回值

最后一次Memcached操作结果的描述消息。

### 范例

**示例 \#1 <span class="function">Memcached::getResultMessage</span>
示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->add('foo', 'bar'); // first time should succeed
$m->add('foo', 'bar');
echo $m->getResultMessage(),"\n";
?>
```

以上例程会输出：

    NOT STORED

Memcached::getServerByKey
=========================

获取一个key所映射的服务器信息

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::getServerByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> )

<span
class="function">Memcached::getServerByKey</span>返回`server_key`所映射的服务器,
<span
class="function">Memcached::\*ByKey</span>系列方法的中的`server_key`参数,
实际上就是用来获取 操作的服务器的.(译注: 可以这样理解,
\*ByKey系列函数首先调用<span
class="function">Memcached::getServerByKey</span>获取服务器,
然后在此服务器上进行操作.)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::getServerByKey</span>
示例**

``` php
<?php
$m = new Memcached();
$m->addServers(array(
    array('mem1.domain.com', 11211, 40),
    array('mem2.domain.com', 11211, 40),
    array('mem3.domain.com', 11211, 20),
));

$m->setOption(Memcached::OPT_LIBKETAMA_COMPATIBLE, true);

var_dump($m->getServerByKey('user'));
var_dump($m->getServerByKey('log'));
var_dump($m->getServerByKey('ip'));
?>
```

以上例程的输出类似于：

    array(3) {
      ["host"]=>
      string(15) "mem3.domain.com"
      ["port"]=>
      int(11211)
      ["weight"]=>
      int(20)
    }
    array(3) {
      ["host"]=>
      string(15) "mem2.domain.com"
      ["port"]=>
      int(11211)
      ["weight"]=>
      int(40)
    }
    array(3) {
      ["host"]=>
      string(15) "mem2.domain.com"
      ["port"]=>
      int(11211)
      ["weight"]=>
      int(40)
    }

Memcached::getServerList
========================

获取服务器池中的服务器列表

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::getServerList</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::getServerList</span>返回服务器池中所有服务器列表.

### 参数

此函数没有参数。

### 返回值

服务器池中所有服务器列表.

### 范例

**示例 \#1 <span class="function">Memcached::getServerList</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServers(array(
    array('mem1.domain.com', 11211, 20),
    array('mem2.domain.com', 11311, 80),
));
var_dump($m->getServerList());
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      array(3) {
        ["host"]=>
        string(15) "mem1.domain.com"
        ["port"]=>
        int(11211)
        ["weight"]=>
        int(20)
      }
      [1]=>
      array(3) {
        ["host"]=>
        string(15) "mem2.domain.com"
        ["port"]=>
        int(11311)
        ["weight"]=>
        int(80)
      }
    }

Memcached::getStats
===================

获取服务器池的统计信息

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::getStats</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::getStats</span>返回一个包含所有可用memcache服务器状态的数组.
返回的统计信息的详细描述参见<a href="http://code.sixapart.com/svn/memcached/trunk/server/doc/protocol.txt" class="link external">» memcache protocol</a>。
（译注：经实验，服务器池中有不可用服务器时，返回false）

### 参数

此函数没有参数。

### 返回值

服务器统计信息数组， 每个服务器一项。

### 范例

**示例 \#1 <span class="function">Memcached::getStats</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

print_r($m->getStats());
?>
```

以上例程的输出类似于：

    Array
    (
        [localhost:11211] => Array
            (
                [pid] => 4933
                [uptime] => 786123
                [threads] => 1
                [time] => 1233868010
                [pointer_size] => 32
                [rusage_user_seconds] => 0
                [rusage_user_microseconds] => 140000
                [rusage_system_seconds] => 23
                [rusage_system_microseconds] => 210000
                [curr_items] => 145
                [total_items] => 2374
                [limit_maxbytes] => 67108864
                [curr_connections] => 2
                [total_connections] => 151
                [connection_structures] => 3
                [bytes] => 20345
                [cmd_get] => 213343
                [cmd_set] => 2381
                [get_hits] => 204223
                [get_misses] => 9120
                [evictions] => 0
                [bytes_read] => 9092476
                [bytes_written] => 15420512
                [version] => 1.2.6
            )

    )

Memcached::getVersion
=====================

获取服务器池中所有服务器的版本信息

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Memcached::getVersion</span> ( <span
class="methodparam">void</span> )

<span
class="function">Memcached::getVersion</span>返回一个包含所有可用memcached服务器版本信息的数组。
（译注：经实验，服务器池中有不可用服务器时，返回false）

### 参数

此函数没有参数。

### 返回值

服务器版本信息的数组，每个服务器占一项。

### 范例

**示例 \#1 <span class="function">Memcached::getVersion</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

print_r($m->getVersion());
?>
```

以上例程的输出类似于：

    Array
    (
        [localhost:11211] => 1.2.6
    )

Memcached::increment
====================

增加数值元素的值

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Memcached::increment</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \] )

<span class="function">Memcached::increment</span>
将一个数值元素增加参数 `offset`
指定的大小。如果元素的值不是数值类型，将返回错误。如果元素不存在， <span
class="function">Memcached::increment</span> 会将元素设置成
`initial_value` 指定的值。

### 参数

`key`  
要增加值的元素的 key。

`offset`  
要将元素的值增加的大小。

`initial_value`  
如果元素不存在，要设置的默认值。

`expiry`  
设置元素值的过期时间。

### 返回值

成功时返回元素的新值 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">Memcached::increment</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('counter', 0);
$m->increment('counter');
$n = $m->increment('counter', 10);
var_dump($n);

$m->set('counter', 'abc');
$n = $m->increment('counter');
// ^ will fail due to item value not being numeric
var_dump($n);
?>
```

以上例程会输出：

    int(11)
    bool(false)

### 参见

-   <span class="methodname">Memcached::decrement</span>
-   <span class="methodname">Memcached::decrementByKey</span>
-   <span class="methodname">Memcached::incrementByKey</span>

Memcached::incrementByKey
=========================

Increment numeric item's value, stored on a specific server

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Memcached::incrementByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$initial_value`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$expiry`<span
class="initializer"> = 0</span></span> \]\]\] )

<span class="function">Memcached::incrementByKey</span> increments a
numeric item's value by the specified `offset`. If the item's value is
not numeric, an error will result. <span
class="function">Memcached::incrementByKey</span> will set the item to
the `initial_value` parameter if the key doesn't exist.

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
The key of the item to increment.

`offset`  
The amount by which to increment the item's value.

`initial_value`  
The value to set the item to if it doesn't currently exist.

`expiry`  
The expiry time to set on the item.

### 返回值

Returns new item's value on success 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="methodname">Memcached::decrement</span>
-   <span class="methodname">Memcached::decrementByKey</span>
-   <span class="methodname">Memcached::increment</span>

Memcached::isPersistent
=======================

Check if a persitent connection to memcache is being used

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::isPersistent</span> ( <span
class="methodparam">void</span> )

<span class="function">Memcached::isPersistent</span> checks if the
connections to the memcache servers are persistent connections.

### 参数

此函数没有参数。

### 返回值

Returns true if Memcache instance uses a persistent connection, false
otherwise.

### 参见

-   <span class="methodname">Memcached::isPristine</span>

Memcached::isPristine
=====================

Check if the instance was recently created

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::isPristine</span> ( <span
class="methodparam">void</span> )

<span class="function">Memcached::isPristine</span> checks if the
Memcache instance was recently created.

### 参数

此函数没有参数。

### 返回值

Returns the true if instance is recently created, false otherwise.

### 参见

-   <span class="methodname">Memcached::isPersistent</span>

Memcached::prepend
==================

向一个已存在的元素前面追加数据

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::prepend</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span
class="function">Memcached::prepend</span>向已存在元素的字符串值前追加`value`。
`value`被强制转换成字符串类型主要是因为对于mix类型的追加没有很好的定义。

> **Note**:
>
> 如果**`Memcached::OPT_COMPRESSION`**常量开启，这个操作会失败，并引发一个警告，因为向压缩数据
> 后追加数据可能会导致解压不了。

### 参数

`key`  
要向前追加数据的元素的key。

`value`  
要追加的字符串。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTSTORED`**。

### 范例

**示例 \#1 <span class="function">Memcached::prepend</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$m->setOption(Memcached::OPT_COMPRESSION, false);

$m->set('foo', 'abc');
$m->prepend('foo', 'def');
var_dump($m->get('foo'));
?>
```

以上例程会输出：

    string(6) "defabc"

### 参见

-   <span class="methodname">Memcached::prependByKey</span>
-   <span class="methodname">Memcached::append</span>

Memcached::prependByKey
=======================

Prepend data to an existing item on a specific server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::prependByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

除了可以使用`server_key`自由的将`key`映射到指定服务器外， <span
class="function">Memcached::prependByKey</span>在功能上等同于 <span
class="methodname">Memcached::prepend</span>。 (译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
要向前追加数据的元素的key。

`value`  
要追加的字符串。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTSTORED`**。

### 参见

-   <span class="methodname">Memcached::prepend</span>
-   <span class="methodname">Memcached::append</span>

Memcached::quit
===============

关闭所有打开的链接。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::quit</span> ( <span
class="methodparam">void</span> )

<span class="function">Memcached::quit</span>
关闭所有memcache服务器的链接。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

Memcached::replace
==================

替换已存在key下的元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::replace</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expiration`</span> \] )

<span class="function">Memcached::replace</span>和 <span
class="methodname">Memcached::set</span>类似，但是如果
服务端不存在`key`， 操作将失败。

### 参数

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTSTORED`**。

### 参见

-   <span class="methodname">Memcached::replaceByKey</span>
-   <span class="methodname">Memcached::set</span>
-   <span class="methodname">Memcached::add</span>

Memcached::replaceByKey
=======================

Replace the item under an existing key on a specific server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::replaceByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

除了可以使用`server_key`自由的将`key`映射到指定服务器外， <span
class="function">Memcached::replaceByKey</span>在功能上等同于 <span
class="methodname">Memcached::replace</span>。 (译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)。

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果key不存在，
<span
class="methodname">Memcached::getResultCode</span>返回**`Memcached::RES_NOTSTORED`**。

### 参见

-   <span class="methodname">Memcached::replace</span>
-   <span class="methodname">Memcached::set</span>
-   <span class="methodname">Memcached::add</span>

Memcached::resetServerList
==========================

Clears all servers from the server list

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::resetServerList</span> ( <span
class="methodparam">void</span> )

<span class="function">Memcached::resetserverlist</span> removes all
memcache servers from the known server list, resetting it back to empty.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">Memcached::addServer</span>
-   <span class="methodname">Memcached::addServers</span>

Memcached::set
==============

存储一个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::set</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$expiration`</span> \] )

<span class="function">Memcached::set</span>将`value`
存储在一个memcached服务器上的`key`下。`expiration`参数
用于控制值的过期时间。

值可以是任何有效的非资源型php类型，
因为资源类型不能被序列化存储。如果**`Memcached::OPT_COMPRESSION`**
选项开启， 序列化的值同样会被压缩存储。

### 参数

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::set</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$m->set('int', 99);
$m->set('string', 'a simple string');
$m->set('array', array(11, 12));
/* 'object'这个key将在5分钟后过期 */
$m->set('object', new stdclass, time() + 300);


var_dump($m->get('int'));
var_dump($m->get('string'));
var_dump($m->get('array'));
var_dump($m->get('object'));
?>
```

以上例程的输出类似于：

    int(99)
    string(15) "a simple string"
    array(2) {
      [0]=>
      int(11)
      [1]=>
      int(12)
    }
    object(stdClass)#1 (0) {
    }

### 参见

-   <span class="methodname">Memcached::setByKey</span>
-   <span class="methodname">Memcached::add</span>
-   <span class="methodname">Memcached::replace</span>

Memcached::setByKey
===================

Store an item on a specific server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::setByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

除了可以使用`server_key`自由的将`key`映射到指定服务器外， <span
class="function">Memcached::setByKey</span>在功能上等同于 <span
class="methodname">Memcached::set</span>。 (译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)。

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
用于存储值的键名。

`value`  
存储的值。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::setByKey</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

/* 保证block-ip系列key的存储在同一台服务器上。*/
$m->setByKey('api-cache', 'block-ip:169.254.253.252', 1);
$m->setByKey('api-cache', 'block-ip:169.127.127.202', 1);
?>
```

### 参见

-   <span class="methodname">Memcached::set</span>

Memcached::setMulti
===================

存储多个元素

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::setMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$items`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> \] )

<span class="function">Memcached::setMulti</span>类似于 <span
class="methodname">Memcached::set</span>， 但是使用了
参数`items`指定多个元素来替代单独的key/value设置以便于对多个元素的操作。`expiration`
参数指定的时候一次应用到所有的元素上。

### 参数

`items`  
存放在服务器上的键／值对数组。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 范例

**示例 \#1 <span class="function">Memcached::setMulti</span> 示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items, time() + 300);
?>
```

### 参见

-   <span class="methodname">Memcached::setMultiByKey</span>
-   <span class="methodname">Memcached::set</span>

Memcached::setMultiByKey
========================

Store multiple items on a specific server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::setMultiByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">array</span> `$items`</span> \[, <span
class="methodparam"><span class="type">int</span> `$expiration`</span>
\] )

除了可以使用`server_key`自由的将`key`映射到指定服务器外， <span
class="function">Memcached::setMultiByKey</span>在功能上等同于 <span
class="methodname">Memcached::setMulti</span>。 (译注:
关于\*ByKey系列方法及$server\_key的工作原理请参照addByKey方法文档)。

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`items`  
存放在服务器上的键／值对数组。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 参见

-   <span class="methodname">Memcached::setMulti</span>
-   <span class="methodname">Memcached::set</span>

Memcached::setOption
====================

设置一个memcached选项

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::setOption</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

这个方法用来设置Memcached
`option`的值。一些选项和libmemcached中定义的类似， 还有一些则是
扩展所特有的。关于选项的更多信息请参阅<a href="/memcached/constants.html" class="link">Memcached Constants</a>。

下面的选项列表需要通过特定的常量指定值。

-   *Memcached::OPT\_HASH*需要*Memcached::HASH\_\**系列常量值。

-   *Memcached::OPT\_DISTRIBUTION*需要*Memcached::DISTRIBUTION\_\**系列常量值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 设置一个memcached选项值**

``` php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);
$m->setOption(Memcached::OPT_HASH, Memcached::HASH_MURMUR);
$m->setOption(Memcached::OPT_PREFIX_KEY, "widgets");
echo "Prefix key is now: ", $m->getOption(Memcached::OPT_PREFIX_KEY), "\n";
?>
```

以上例程会输出：

    bool(true)
    Prefix key is now: widgets

### 参见

-   <span class="methodname">Memcached::getOption</span>

Memcached::setOptions
=====================

Set Memcached options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::setOptions</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

<span class="function">Memcached::setOptions</span> is a variation of
the <span class="methodname">Memcached::setOption</span> that takes an
array of options to be set.

### 参数

`options`  
An associative array of options where the key is the option to set and
the value is the new value for the option.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Setting Memcached options**

``` php
<?php
$m = new Memcached();
var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);

$m->setOptions(array(Memcached::OPT_HASH => Memcached::HASH_MURMUR, Memcached::OPT_PREFIX_KEY => "widgets"));

var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);
echo "Prefix key is now: ", $m->getOption(Memcached::OPT_PREFIX_KEY), "\n";
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    Prefix key is now: widgets

### 参见

-   <span class="methodname">Memcached::getOption</span>
-   <span class="methodname">Memcached::setOption</span>
-   <a href="/memcached/constants.html" class="link">Memcached Constants</a>

Memcached::setSaslAuthData
==========================

Set the credentials to use for authentication

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Memcached::setSaslAuthData</span> ( <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> )

<span class="function">Memcached::setSaslAuthData</span> sets the
username and password that should be used for SASL authentication with
the memcache servers.

*This method is only available when the memcached extension is built
with SASL support.* Please refer to
<a href="/memcached/setup.html" class="link">Memcached setup</a> for how
to do this.

### 参数

`username`  
The username to use for authentication.

`password`  
The password to use for authentication.

### 返回值

没有返回值。

Memcached::touch
================

Set a new expiration on an item

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::touch</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">int</span>
`$expiration`</span> )

<span class="function">Memcached::touch</span> sets a new expiration
value on the given key.

### 参数

`key`  
用于存储值的键名。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 参见

-   <span class="methodname">Memcached::touchByKey</span>

Memcached::touchByKey
=====================

Set a new expiration on an item on a specific server

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Memcached::touchByKey</span> ( <span
class="methodparam"><span class="type">string</span>
`$server_key`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">int</span> `$expiration`</span> )

<span class="function">Memcached::touchByKey</span> is functionally
equivalent to <span class="methodname">Memcached::touch</span>, except
that the free-form `server_key` can be used to map the `key` to a
specific server.

### 参数

`server_key`  
本键名用于识别储存和读取值的服务器。没有将实际的键名散列到具体的项目，而是在决定与哪一个
memcached
服务器通信时将其散列为服务器键名。这使得关联的项目在单一的服务上被组合起来以提高多重操作的效率。

`key`  
用于存储值的键名。

`expiration`  
到期时间，默认为 0。
更多信息请参见<a href="/memcached/expiration.html" class="link">到期时间</a>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如需要则使用
<span class="methodname">Memcached::getResultCode</span>。

### 参见

-   <span class="methodname">Memcached::touch</span>
