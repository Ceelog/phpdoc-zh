Yac
===

**目录**

-   [简介](/intro/yac.html)
-   [安装／配置](/yac/setup.html)
    -   [需求](/yac/setup.html#需求)
    -   [安装](/yac/setup.html#安装)
    -   [运行时配置](/yac/setup.html#运行时配置)
    -   [资源类型](/yac/setup.html#资源类型)
-   [预定义常量](/yac/constants.html)
-   [Yac](/class/yac.html) — The Yac class
    -   [Yac::add](/class/yac.html#Yac::add) — Store into cache
    -   [Yac::\_\_construct](/class/yac.html#Yac::__construct) —
        Constructor
    -   [Yac::delete](/class/yac.html#Yac::delete) — Remove items from
        cache
    -   [Yac::dump](/class/yac.html#Yac::dump) — Dump cache
    -   [Yac::flush](/class/yac.html#Yac::flush) — Flush the cache
    -   [Yac::get](/class/yac.html#Yac::get) — Retrieve values from
        cache
    -   [Yac::\_\_get](/class/yac.html#Yac::__get) — Getter
    -   [Yac::info](/class/yac.html#Yac::info) — Status of cache
    -   [Yac::set](/class/yac.html#Yac::set) — Store into cache
    -   [Yac::\_\_set](/class/yac.html#Yac::__set) — Setter

简介
----

类摘要
------

**Yac**

<span class="ooclass"> class **Yac** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_prefix` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$prefix`<span
class="initializer"> = ""</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">string</span> `$keys`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">array</span> `$key_vals`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delete</span> ( <span class="methodparam"><span
class="type">string\|array</span> `$keys`</span> \[, <span
class="methodparam"><span class="type">int</span> `$ttl`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">dump</span> ( <span class="methodparam"><span
class="type">int</span> `$$num`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">string\|array</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$cas`<span
class="initializer"> = **`NULL`**</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">info</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">string</span> `$keys`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">array</span> `$key_vals`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$keys`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

}

属性
----

`_prefix`  

Yac::add
========

Store into cache

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yac::add</span> ( <span
class="methodparam"><span class="type">string</span> `$keys`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$ttl`<span class="initializer"> =
0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yac::add</span> ( <span
class="methodparam"><span class="type">array</span> `$key_vals`</span> )

Added a item into cache.

### 参数

`keys`  
<span class="type">string</span> key

`value`  
mixed value, All php value type could be stored except
<a href="/language/types/resource.html" class="link">资源(resource)</a>

`ttl`  
expire time

### 返回值

<span class="type">boolean</span>, **`TRUE`** on success, **`FALSE`** on
failure

> **Note**:
>
> <span class="methodname">Yac::add</span> may fail if cas lock could
> not obtain, so, if you need the value to be stored properly, you may
> write codes like:
>
> **示例 \#1 Make sure the item is stored**
>
> ``` php
> while(!$yac->set("key", "vale));
> ```

Yac::\_\_construct
==================

Constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">Yac::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$prefix`<span
class="initializer"> = ""</span></span> \] )

prefix is used to prepended to keys, this could be used to avoiding
conflicts between apps.

### 参数

`prefix`  
<span class="type">string</span> prefix

Yac::delete
===========

Remove items from cache

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yac::delete</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$keys`</span> \[, <span class="methodparam"><span
class="type">int</span> `$ttl`</span> \] )

remove items from cache

### 参数

`keys`  
string key, or array of multiple keys to be removed

`ttl`  
if delay is set, delete will mark the items to be invalid in ttl second.

### 返回值

Yac::dump
=========

Dump cache

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yac::dump</span> ( <span
class="methodparam"><span class="type">int</span> `$$num`</span> )

Dump values stored in cache

### 参数

`num`  
Maximum number of items should be returned

### 返回值

mixed

Yac::flush
==========

Flush the cache

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yac::flush</span> ( <span
class="methodparam">void</span> )

Remove all cached values

### 参数

此函数没有参数。

### 返回值

bool, always true

Yac::get
========

Retrieve values from cache

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yac::get</span> ( <span
class="methodparam"><span class="type">string\|array</span>
`$key`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$cas`<span class="initializer"> =
**`NULL`**</span></span> \] )

Retrieve values from cache

### 参数

`key`  
<span class="type">string</span> keys, or <span
class="type">array</span> of multiple keys.

`cas`  
if not **`NULL`**, it will be set to the retrieved item's cas.

### 返回值

mixed on success, false on failure

Yac::\_\_get
============

Getter

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yac::\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Retrieve values from cache

### 参数

`key`  
<span class="type">string</span> key

### 返回值

mixed on success, **`NULL`** on failure

Yac::info
=========

Status of cache

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Yac::info</span> ( <span
class="methodparam">void</span> )

Get status of cache system

### 参数

此函数没有参数。

### 返回值

Return an array, consistent with: "memory\_size", "slots\_memory\_size",
"values\_memory\_size", "segment\_size", "segment\_num", "miss", "hits",
"fails", "kicks", "recycles", "slots\_size", "slots\_used"

Yac::set
========

Store into cache

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yac::set</span> ( <span
class="methodparam"><span class="type">string</span> `$keys`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$ttl`<span class="initializer"> =
0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Yac::add</span> ( <span
class="methodparam"><span class="type">array</span> `$key_vals`</span> )

Add a item into cache, it the key is already exists, override it.

### 参数

`keys`  
<span class="type">string</span> key

`value`  
mixed value, All php value type could be stored except
<a href="/language/types/resource.html" class="link">资源(resource)</a>

`ttl`  
expire time

### 返回值

the value self

Yac::\_\_set
============

Setter

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Yac::\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$keys`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

store a item into cache

### 参数

`keys`  
<span class="type">string</span> key

`value`  
mixed value, All php value type could be stored except
<a href="/language/types/resource.html" class="link">资源(resource)</a>

### 返回值

Always return the value self
