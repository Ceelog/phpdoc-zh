Judy Arrays
===========

**目录**

-   [简介](/intro/judy.html)
-   [安装／配置](/judy/setup.html)
    -   [需求](/judy/setup.html#需求)
    -   [安装](/judy/setup.html#安装)
    -   [运行时配置](/judy/setup.html#运行时配置)
    -   [资源类型](/judy/setup.html#资源类型)
-   [Judy](/class/judy.html) — The Judy class
    -   [Judy::byCount](/class/judy.html#Judy::byCount) — Locate the Nth
        index present in the Judy array
    -   [Judy::\_\_construct](/class/judy.html#Judy::__construct) —
        Construct a new Judy object
    -   [Judy::count](/class/judy.html#Judy::count) — Count the number
        of elements in the Judy array
    -   [Judy::\_\_destruct](/class/judy.html#Judy::__destruct) —
        Destruct a Judy object
    -   [Judy::first](/class/judy.html#Judy::first) — Search for the
        first index in the Judy array
    -   [Judy::firstEmpty](/class/judy.html#Judy::firstEmpty) — Search
        for the first absent index in the Judy array
    -   [Judy::free](/class/judy.html#Judy::free) — Free the entire Judy
        array
    -   [Judy::getType](/class/judy.html#Judy::getType) — Return the
        type of the current Judy array
    -   [Judy::last](/class/judy.html#Judy::last) — Search for the last
        index in the Judy array
    -   [Judy::lastEmpty](/class/judy.html#Judy::lastEmpty) — Search for
        the last absent index in the Judy array
    -   [Judy::memoryUsage](/class/judy.html#Judy::memoryUsage) — Return
        the memory used by the Judy array
    -   [Judy::next](/class/judy.html#Judy::next) — Search for the next
        index in the Judy array
    -   [Judy::nextEmpty](/class/judy.html#Judy::nextEmpty) — Search for
        the next absent index in the Judy array
    -   [Judy::offsetExists](/class/judy.html#Judy::offsetExists) —
        Whether a offset exists
    -   [Judy::offsetGet](/class/judy.html#Judy::offsetGet) — Offset to
        retrieve
    -   [Judy::offsetSet](/class/judy.html#Judy::offsetSet) — Offset to
        set
    -   [Judy::offsetUnset](/class/judy.html#Judy::offsetUnset) — Offset
        to unset
    -   [Judy::prev](/class/judy.html#Judy::prev) — Search for the
        previous index in the Judy array
    -   [Judy::prevEmpty](/class/judy.html#Judy::prevEmpty) — Search for
        the previous absent index in the Judy array
    -   [Judy::size](/class/judy.html#Judy::size) — Return the size of
        the current Judy array
-   [Judy 函数](/ref/judy.html)
    -   [judy\_type](/ref/judy.html#judy_type) — Return the type of a
        Judy array
    -   [judy\_version](/ref/judy.html#judy_version) — Return or print
        the current PHP Judy version

简介
----

The Judy class implements the
<a href="/class/arrayaccess.html" class="link">ArrayAccess</a> interface
and the <a href="/class/iterator.html" class="link">Iterator</a>
interface. This class, once instantiated, can be accessed like a PHP
<a href="/book/array.html" class="link">array</a>.

A PHP Judy object (or Judy Array) can be one of the following type :

-   <a href="/class/judy.html#" class="link">Judy::BITSET</a>
-   <a href="/class/judy.html#" class="link">Judy::INT_TO_INT</a>
-   <a href="/class/judy.html#" class="link">Judy::INT_TO_MIXED</a>
-   <a href="/class/judy.html#" class="link">Judy::STRING_TO_INT</a>
-   <a href="/class/judy.html#" class="link">Judy::STRING_TO_MIXED</a>

**示例 \#1 Judy array example**

``` php
<?php
    $judy = new Judy(Judy::INT_TO_MIXED);
    $judy[1] = "one";
    $judy[2] = array('a', 'b', 'c');
    $judy[3] = new Judy(Judy::BITSET);
?>
```

类摘要
------

**Judy**

<span class="ooclass"> class **Judy** </span> <span
class="oointerface">implements <span
class="interfacename">ArrayAccess</span> </span> <span
class="oointerface">, <span class="interfacename">Iterator</span>
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`Judy::BITSET` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Judy::INT_TO_INT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Judy::INT_TO_MIXED` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Judy::STRING_TO_INT` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Judy::STRING_TO_MIXED` <span class="initializer"> = 5</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">byCount</span> ( <span class="methodparam"><span
class="type">int</span> `$nth_index`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$judy_type`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> (\[ <span class="methodparam"><span
class="type">int</span> `$index_start`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$index_end`<span class="initializer"> =
-1</span></span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">first</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$index`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">firstEmpty</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$index`<span class="initializer"> =
0</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">free</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">last</span> (\[ <span class="methodparam"><span
class="type">string</span> `$index`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">lastEmpty</span> (\[ <span class="methodparam"><span
class="type">int</span> `$index`<span class="initializer"> =
-1</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">memoryUsage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">next</span> ( <span class="methodparam"><span
class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">nextEmpty</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">prev</span> ( <span class="methodparam"><span
class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">prevEmpty</span> ( <span class="methodparam"><span
class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">size</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`Judy::BITSET`**  
Define the Judy Array as a Bitset with keys as Integer and Values as a
Boolean

**`Judy::INT_TO_INT`**  
Define the Judy Array with key/values as Integer, and Integer only.

**`Judy::INT_TO_MIXED`**  
Define the Judy Array with keys as Integer and Values of any type.

**`Judy::STRING_TO_INT`**  
Define the Judy Array with keys as a String and Values as Integer, and
Integer only.

**`Judy::STRING_TO_MIXED`**  
Define the Judy Array with keys as a String and Values of any type.

Judy::byCount
=============

Locate the Nth index present in the <span class="classname">Judy</span>
array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::byCount</span> ( <span
class="methodparam"><span class="type">int</span> `$nth_index`</span> )

Locate the Nth index present in the <span class="classname">Judy</span>
array.

### 参数

`nth_index`  
Nth index to return. If nth\_index equal 1, then it will return the
first index in the array.

### 返回值

Return the index at the given Nth position.

Judy::\_\_construct
===================

Construct a new <span class="classname">Judy</span> object

### 说明

<span class="modifier">public</span> <span
class="methodname">Judy::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$judy_type`</span> )

Construct a new Judy object. A Judy object can be accessed like a PHP
Array.

### 参数

`judy_type`  
The Judy <a href="/class/judy.html#" class="link">type</a> to be used.

### 返回值

Return the new Judy instance.

Judy::count
===========

Count the number of elements in the <span class="classname">Judy</span>
array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::count</span> (\[ <span
class="methodparam"><span class="type">int</span> `$index_start`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$index_end`<span
class="initializer"> = -1</span></span> \]\] )

Count the number of elements in the <span class="classname">Judy</span>
array.

### 参数

`index_start`  
Start counting from the given index. Default is first index.

`index_end`  
Stop counting when reaching this index. Default is last index.

### 返回值

Return the number of elements.

Judy::\_\_destruct
==================

Destruct a Judy object

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Judy::\_\_destruct</span> ( <span
class="methodparam">void</span> )

Destruct a Judy object.

### 参数

此函数没有参数。

### 返回值

Judy::first
===========

Search for the first index in the <span class="classname">Judy</span>
array

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Judy::first</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$index`</span> \] )

Search (inclusive) for the first index present that is equal to or
greater than the passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::firstEmpty
================

Search for the first absent index in the <span
class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::firstEmpty</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$index`<span
class="initializer"> = 0</span></span> \] )

Search (inclusive) for the first absent index that is equal to or
greater than the passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::free
==========

Free the entire <span class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::free</span> ( <span
class="methodparam">void</span> )

Free the entire <span class="classname">Judy</span> array.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Judy::getType
=============

Return the type of the current <span class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::getType</span> ( <span
class="methodparam">void</span> )

Return an integer corresponding to the Judy
<a href="/class/judy.html#" class="link">type</a> of the current object.

### 参数

此函数没有参数。

### 返回值

Return an integer corresponding to a Judy
<a href="/class/judy.html#" class="link">type</a>.

Judy::last
==========

Search for the last index in the <span class="classname">Judy</span>
array

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Judy::last</span> (\[ <span
class="methodparam"><span class="type">string</span> `$index`</span> \]
)

Search (inclusive) for the last index present that is equal to or less
than the passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::lastEmpty
===============

Search for the last absent index in the <span
class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::lastEmpty</span> (\[ <span
class="methodparam"><span class="type">int</span> `$index`<span
class="initializer"> = -1</span></span> \] )

Search (inclusive) for the last absent index that is equal to or less
than the passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::memoryUsage
=================

Return the memory used by the <span class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::memoryUsage</span> ( <span
class="methodparam">void</span> )

Return the memory used by the <span class="classname">Judy</span> array.

### 参数

此函数没有参数。

### 返回值

Return the memory used in bytes.

Judy::next
==========

Search for the next index in the <span class="classname">Judy</span>
array

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Judy::next</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Search (exclusive) for the next index present that is greater than the
passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::nextEmpty
===============

Search for the next absent index in the <span
class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::nextEmpty</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Search (exclusive) for the next absent index that is greater than the
passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::offsetExists
==================

Whether a offset exists

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Judy::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

Whether or not an offset exists.

### 参数

`offset`  
An offset to check for.

### 返回值

Returns **`TRUE`** on success or **`FALSE`** on failure.

Judy::offsetGet
===============

Offset to retrieve

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Judy::offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

Returns the value at specified offset.

### 参数

`offset`  
The offset to retrieve.

### 返回值

Can return all value types.

Judy::offsetSet
===============

Offset to set

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Judy::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Assigns a value to the specified offset.

### 参数

`offset`  
The offset to assign the value to.

`value`  
The value to set.

### 返回值

No value is returned.

Judy::offsetUnset
=================

Offset to unset

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Judy::offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

Unsets an offset.

### 参数

`offset`  
The offset to unset.

### 返回值

No value is returned.

Judy::prev
==========

Search for the previous index in the <span class="classname">Judy</span>
array

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Judy::prev</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Search (exclusive) for the previous index present that is less than the
passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::prevEmpty
===============

Search for the previous absent index in the <span
class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Judy::prevEmpty</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Search (exclusive) for the previous index absent that is less than the
passed Index.

### 参数

`index`  
The index can be an integer or a string corresponding to the index where
to start the search.

### 返回值

Return the corresponding index in the array.

Judy::size
==========

Return the size of the current <span class="classname">Judy</span> array

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Judy::size</span> ( <span
class="methodparam">void</span> )

此方法是该方法的别名： <span class="methodname">Judy::count</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Return an integer.
