yp\_all
=======

Traverse the map and call a function on each entry

### 说明

<span class="type">void</span> <span class="methodname">yp\_all</span> (
<span class="methodparam"><span class="type">string</span>
`$domain`</span> , <span class="methodparam"><span
class="type">string</span> `$map`</span> , <span
class="methodparam"><span class="type">string</span> `$callback`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`domain`  
The NIS domain name.

`map`  
The NIS map.

`callback`  

### 返回值

没有返回值。

yp\_cat
=======

Return an array containing the entire map

### 说明

<span class="type">array</span> <span class="methodname">yp\_cat</span>
( <span class="methodparam"><span class="type">string</span>
`$domain`</span> , <span class="methodparam"><span
class="type">string</span> `$map`</span> )

Returns all map entries.

### 参数

`domain`  
The NIS domain name.

`map`  
The NIS map.

### 返回值

Returns an array of all map entries, the maps key values as array
indices and the maps entries as array data.

yp\_err\_string
===============

Returns the error string associated with the given error code

### 说明

<span class="type">string</span> <span
class="methodname">yp\_err\_string</span> ( <span
class="methodparam"><span class="type">int</span> `$errorcode`</span> )

Returns the error message associated with the given error code. Useful
to indicate what exactly went wrong.

### 参数

`errorcode`  
The error code.

### 返回值

Returns the error message, as a string.

### 范例

**示例 \#1 Example for NIS errors**

``` php
<?php
echo "Error: " . yp_err_string(yp_errno());
?>
```

### 参见

-   <span class="function">yp\_errno</span>

yp\_errno
=========

Returns the error code of the previous operation

### 说明

<span class="type">int</span> <span class="methodname">yp\_errno</span>
( <span class="methodparam">void</span> )

Returns the error code of the previous operation.

### 返回值

Returns one of the *YPERR\_XXX* error constants.

### 参见

-   <span class="function">yp\_err\_string</span>

yp\_first
=========

Returns the first key-value pair from the named map

### 说明

<span class="type">array</span> <span
class="methodname">yp\_first</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$map`</span> )

Gets the first key-value pair from the named `map` in the named
`domain`.

### 参数

`domain`  
The NIS domain name.

`map`  
The NIS map.

### 返回值

Returns the first key-value pair as an array on success, or **`FALSE`**
on errors.

### 范例

**示例 \#1 Example for the NIS first**

``` php
<?php
$entry = yp_first($domain, "passwd.byname");

$key = key($entry);
$value = $entry[$key];

echo "First entry in this map has key " . $key . " and value " . $value;
?>
```

### 参见

-   <span class="function">yp\_next</span>
-   <span class="function">yp\_get\_default\_domain</span>

yp\_get\_default\_domain
========================

Fetches the machine's default NIS domain

### 说明

<span class="type">string</span> <span
class="methodname">yp\_get\_default\_domain</span> ( <span
class="methodparam">void</span> )

Returns the default domain of the node. Can be used as the domain
parameter for successive NIS calls.

A NIS domain can be described a group of NIS maps. Every host that needs
to look up information binds itself to a certain domain. Refer to the
documents mentioned at the beginning for more detailed information.

### 返回值

Returns the default domain of the node or **`FALSE`**. Can be used as
the domain parameter for successive NIS calls.

### 范例

**示例 \#1 Example for the default domain**

``` php
<?php
$domain = yp_get_default_domain();
echo "Default NIS domain is: " . $domain;
?>
```

yp\_master
==========

Returns the machine name of the master NIS server for a map

### 说明

<span class="type">string</span> <span
class="methodname">yp\_master</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$map`</span> )

Returns the machine name of the master NIS server for a `map`.

### 参数

`domain`  
The NIS domain name.

`map`  
The NIS map.

### 返回值

### 范例

**示例 \#1 Example for the NIS master**

``` php
<?php
$number = yp_master($domain, $mapname);
echo "Master for this map is: " . $master;
?>
```

### 参见

-   <span class="function">yp\_get\_default\_domain</span>

yp\_match
=========

Returns the matched line

### 说明

<span class="type">string</span> <span
class="methodname">yp\_match</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$map`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

Returns the value associated with the passed `key` out of the specified
`map`.

### 参数

`domain`  
The NIS domain name.

`map`  
The NIS map.

`key`  
This key must be exact.

### 返回值

Returns the value, or **`FALSE`** on errors.

### 范例

**示例 \#1 Example for NIS match**

``` php
<?php
$entry = yp_match($domain, "passwd.byname", "joe");
echo "Matched entry is: " . $entry;
?>
```

以上例程的输出类似于：

    joe:##joe:11111:100:Joe User:/home/j/joe:/usr/local/bin/bash

### 参见

-   <span class="function">yp\_get\_default\_domain</span>

yp\_next
========

Returns the next key-value pair in the named map

### 说明

<span class="type">array</span> <span class="methodname">yp\_next</span>
( <span class="methodparam"><span class="type">string</span>
`$domain`</span> , <span class="methodparam"><span
class="type">string</span> `$map`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Returns the next key-value pair in the named `map` after the specified
`key`.

### 参数

`domain`  

`map`  

`key`  

### 返回值

Returns the next key-value pair as an array, or **`FALSE`** on errors.

### 范例

**示例 \#1 Example for NIS next**

``` php
<?php
$entry = yp_next($domain, "passwd.byname", "joe");

if (!$entry) {
    echo "No more entries found\n";
    echo "<!--" . yp_errno() . ": " . yp_err_string() . "-->";
}

$key = key($entry);

echo "The next entry after joe has key " . $key
      . " and value " . $entry[$key];
?>
```

### 参见

-   <span class="function">yp\_first</span>
-   <span class="function">yp\_get\_default\_domain</span>

yp\_order
=========

Returns the order number for a map

### 说明

<span class="type">int</span> <span class="methodname">yp\_order</span>
( <span class="methodparam"><span class="type">string</span>
`$domain`</span> , <span class="methodparam"><span
class="type">string</span> `$map`</span> )

Gets the order number for a map.

### 参数

`domain`  

`map`  

### 返回值

Returns the order number for a map or **`FALSE`** on error.

### 范例

**示例 \#1 Example for the NIS order**

``` php
<?php
    $number = yp_order($domain, $mapname);
    echo "Order number for this map is: " . $number;
?>
```

### 参见

-   <span class="function">yp\_get\_default\_domain</span>

**目录**

-   [yp\_all](/ref/nis.html#yp_all) — Traverse the map and call a
    function on each entry
-   [yp\_cat](/ref/nis.html#yp_cat) — Return an array containing the
    entire map
-   [yp\_err\_string](/ref/nis.html#yp_err_string) — Returns the error
    string associated with the given error code
-   [yp\_errno](/ref/nis.html#yp_errno) — Returns the error code of the
    previous operation
-   [yp\_first](/ref/nis.html#yp_first) — Returns the first key-value
    pair from the named map
-   [yp\_get\_default\_domain](/ref/nis.html#yp_get_default_domain) —
    Fetches the machine's default NIS domain
-   [yp\_master](/ref/nis.html#yp_master) — Returns the machine name of
    the master NIS server for a map
-   [yp\_match](/ref/nis.html#yp_match) — Returns the matched line
-   [yp\_next](/ref/nis.html#yp_next) — Returns the next key-value pair
    in the named map
-   [yp\_order](/ref/nis.html#yp_order) — Returns the order number for a
    map
