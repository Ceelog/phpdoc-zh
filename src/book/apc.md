Alternative PHP Cache (可选 PHP 缓存)
=====================================

**目录**

-   [简介](/intro/apc.html)
-   [安装／配置](/apc/setup.html)
    -   [需求](/apc/setup.html#需求)
    -   [安装](/apc/setup.html#安装)
    -   [运行时配置](/apc/setup.html#运行时配置)
    -   [资源类型](/apc/setup.html#资源类型)
-   [预定义常量](/apc/constants.html)
-   [APC 函数](/ref/apc.html)
    -   [apc\_add](/ref/apc.html#apc_add) — 缓存一个变量到数据存储
    -   [apc\_bin\_dump](/ref/apc.html#apc_bin_dump) —
        获取给定文件和变量的二进制文件转储。
    -   [apc\_bin\_dumpfile](/ref/apc.html#apc_bin_dumpfile) — Output a
        binary dump of cached files and user variables to a file
    -   [apc\_bin\_load](/ref/apc.html#apc_bin_load) — Load a binary
        dump into the APC file/user cache
    -   [apc\_bin\_loadfile](/ref/apc.html#apc_bin_loadfile) — Load a
        binary dump from a file into the APC file/user cache
    -   [apc\_cache\_info](/ref/apc.html#apc_cache_info) — Retrieves
        cached information from APC's data store
    -   [apc\_cas](/ref/apc.html#apc_cas) — 用新值更新旧值
    -   [apc\_clear\_cache](/ref/apc.html#apc_clear_cache) — 清除APC缓存
    -   [apc\_compile\_file](/ref/apc.html#apc_compile_file) — Stores a
        file in the bytecode cache, bypassing all filters
    -   [apc\_dec](/ref/apc.html#apc_dec) — Decrease a stored number
    -   [apc\_define\_constants](/ref/apc.html#apc_define_constants) —
        Defines a set of constants for retrieval and mass-definition
    -   [apc\_delete\_file](/ref/apc.html#apc_delete_file) — Deletes
        files from the opcode cache
    -   [apc\_delete](/ref/apc.html#apc_delete) —
        从用户缓存中删除某个变量
    -   [apc\_exists](/ref/apc.html#apc_exists) —
        检查APC中是否存在某个或者某些key
    -   [apc\_fetch](/ref/apc.html#apc_fetch) — 从缓存中取出存储的变量
    -   [apc\_inc](/ref/apc.html#apc_inc) — 递增一个储存的数字
    -   [apc\_load\_constants](/ref/apc.html#apc_load_constants) — Loads
        a set of constants from the cache
    -   [apc\_sma\_info](/ref/apc.html#apc_sma_info) — Retrieves APC's
        Shared Memory Allocation information
    -   [apc\_store](/ref/apc.html#apc_store) — Cache a variable in the
        data store
-   [APCIterator](/class/apciterator.html) — APCIterator 类
    -   [APCIterator::\_\_construct](/class/apciterator.html#APCIterator::__construct)
        — 构造一个 APCIterator 迭代器对象
    -   [APCIterator::current](/class/apciterator.html#APCIterator::current)
        — 获取当前项
    -   [APCIterator::getTotalCount](/class/apciterator.html#APCIterator::getTotalCount)
        — 获取总数
    -   [APCIterator::getTotalHits](/class/apciterator.html#APCIterator::getTotalHits)
        — 获取缓存命中数
    -   [APCIterator::getTotalSize](/class/apciterator.html#APCIterator::getTotalSize)
        — 获取所有缓存的尺寸大小
    -   [APCIterator::key](/class/apciterator.html#APCIterator::key) —
        获取迭代器的键
    -   [APCIterator::next](/class/apciterator.html#APCIterator::next) —
        移到下一项
    -   [APCIterator::rewind](/class/apciterator.html#APCIterator::rewind)
        — 倒退迭代器
    -   [APCIterator::valid](/class/apciterator.html#APCIterator::valid)
        — 检查当前位置是否有效

简介
----

<span class="classname">APCIterator</span>
类使得遍历大容量APC缓存更容易，这是很有帮助的因为它允许同时获取已经定义的每个被锁定实例的条目数，因此它释放的其他活动的缓存锁，而不是阻碍整个缓存以完成获取100（默认）个缓存数据的迭代，在大缓存条目。
此外，使用正则匹配效率更高，因为它被改为C级别的实现。

类摘要
------

**APCIterator**

<span class="ooclass"> class **APCIterator** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> {

/\* Methods \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$cache`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$search`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = APC\_ITER\_ALL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$chunk_size`<span
class="initializer"> = 100</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$list`<span
class="initializer"> = APC\_LIST\_ACTIVE</span></span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTotalCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTotalHits</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTotalSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

APCIterator::\_\_construct
==========================

构造一个 APCIterator 迭代器对象

### 说明

<span class="modifier">public</span> <span
class="methodname">APCIterator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$cache`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$search`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = APC\_ITER\_ALL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$chunk_size`<span
class="initializer"> = 100</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$list`<span
class="initializer"> = APC\_LIST\_ACTIVE</span></span> \]\]\]\] )

构造一个 <span class="classname">APCIterator</span> <span
class="type">object</span>.

### 参数

`cache`  
缓存类型，可以是 *user* 或者 *file*。

`search`  
匹配 APC 键名的 <a href="/book/pcre.html" class="link">PCRE</a>
正则表达式，既可以是单个正则表达式 <span
class="type">string</span>，也可以是 <span class="type">array</span>
的正则表达式。或者可以是 **`NULL`** 来略过搜索。

`format`  
需要的格式可以用一个或多个
<a href="/apc/constants.html" class="link">APC_ITER_*</a> 常量。

`chunk_size`  
块的大小。必须是一个大于0的值，默认是100。

`list`  
需要列出的类型。可以是 **`APC_LIST_ACTIVE`** 或 **`APC_LIST_DELETED`**。

### 返回值

成功时返回 <span class="classname">APCIterator</span> <span
class="type">object</span>，失败时返回 **`NULL`**。

### 范例

**示例 \#1 <span class="function">APCIterator::\_\_construct</span>
例子**

``` php
<?php
foreach (new APCIterator('user', '/^counter\./') as $counter) {
    echo "$counter[key]: $counter[value]\n";
    apc_dec($counter['key'], $counter['value']);
}
?>
```

### 参见

-   <span class="function">apc\_exists</span>
-   <span class="function">apc\_cache\_info</span>

APCIterator::current
====================

获取当前项

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">APCIterator::current</span> ( <span
class="methodparam">void</span> )

从 <span class="classname">APCIterator</span> 堆中获取当前项。

### 参数

此函数没有参数。

### 返回值

成功时返回当前项，获取失败、没有更多项或者不存在任何项时返回
**`FALSE`**。

### 参见

-   <span class="methodname">APCIterator::next</span>
-   <span class="methodname">Iterator::current</span>

APCIterator::getTotalCount
==========================

获取总数

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">APCIterator::getTotalCount</span> ( <span
class="methodparam">void</span> )

获取总数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The total count.

### 参见

-   <span class="methodname">APCIterator::getTotalHits</span>
-   <span class="methodname">APCIterator::getTotalSize</span>
-   <span class="function">apc\_cache\_info</span>

APCIterator::getTotalHits
=========================

获取缓存命中数

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">APCIterator::getTotalHits</span> ( <span
class="methodparam">void</span> )

获取缓存命中的总数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

成功时返回命中次数，失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">APCIterator::getTotalCount</span>
-   <span class="methodname">APCIterator::getTotalSize</span>
-   <span class="function">apc\_cache\_info</span>

APCIterator::getTotalSize
=========================

获取所有缓存的尺寸大小

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">APCIterator::getTotalSize</span> ( <span
class="methodparam">void</span> )

获取所有缓存的尺寸大小。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The total cache size.

### 参见

-   <span class="methodname">APCIterator::getTotalCount</span>
-   <span class="methodname">APCIterator::getTotalHits</span>
-   <span class="function">apc\_cache\_info</span>

APCIterator::key
================

获取迭代器的键

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">APCIterator::key</span> ( <span
class="methodparam">void</span> )

获取当前迭代器的键。

### 参数

此函数没有参数。

### 返回值

成功时返回一个键，失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">APCIterator::current</span>
-   <span class="methodname">Iterator::key</span>

APCIterator::next
=================

移到下一项

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">APCIterator::next</span> ( <span
class="methodparam">void</span> )

移动迭代器的指针到下一个元素。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">APCIterator::current</span>
-   <span class="methodname">APCIterator::rewind</span>
-   <span class="methodname">Iterator::next</span>

APCIterator::rewind
===================

倒退迭代器

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">APCIterator::rewind</span> ( <span
class="methodparam">void</span> )

倒退迭代器到第一项。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">APCIterator::next</span>
-   <span class="methodname">Iterator::next</span>

APCIterator::valid
==================

检查当前位置是否有效

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">APCIterator::valid</span> ( <span
class="methodparam">void</span> )

检查当前迭代器的位置是否有效。

### 参数

此函数没有参数。

### 返回值

如果当前迭代器的位置有效返回 **`TRUE`** ，反之则返回 **`FALSE`**。

### 参见

-   <span class="methodname">APCIterator::current</span>
-   <span class="methodname">Iterator::valid</span>
