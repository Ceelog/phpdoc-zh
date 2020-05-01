Phdfs
=====

**目录**

-   [](/intro/phdfs.html)
-   [安装／配置](/phdfs/setup.html)
    -   [需求](/phdfs/setup.html#需求)
    -   [安装](/phdfs/setup.html#安装)
    -   [](/phdfs/setup.html#)
    -   [资源类型](/phdfs/setup.html#资源类型)
-   [预定义常量](/phdfs/constants.html)
-   [phdfs](/class/phdfs.html) — The phdfs class
    -   [phdfs::connect](/class/phdfs.html#phdfs::connect) — Description
    -   [phdfs::\_\_construct](/class/phdfs.html#phdfs::__construct) —
        Description
    -   [phdfs::copy](/class/phdfs.html#phdfs::copy) — Description
    -   [phdfs::create\_directory](/class/phdfs.html#phdfs::create_directory)
        — Description
    -   [phdfs::delete](/class/phdfs.html#phdfs::delete) — Description
    -   [phdfs::\_\_destruct](/class/phdfs.html#phdfs::__destruct) —
        Description
    -   [phdfs::disconnect](/class/phdfs.html#phdfs::disconnect) —
        Description
    -   [phdfs::exists](/class/phdfs.html#phdfs::exists) — Description
    -   [phdfs::file\_info](/class/phdfs.html#phdfs::file_info) —
        Description
    -   [phdfs::list\_directory](/class/phdfs.html#phdfs::list_directory)
        — Description
    -   [phdfs::read](/class/phdfs.html#phdfs::read) — Description
    -   [phdfs::rename](/class/phdfs.html#phdfs::rename) — Description
    -   [phdfs::tell](/class/phdfs.html#phdfs::tell) — Description
    -   [phdfs::write](/class/phdfs.html#phdfs::write) — Description

简介
----

类摘要
------

**phdfs**

<span class="ooclass"> class **phdfs** </span> {

/\* 属性 \*/

<span class="modifier">static</span> `$host` ;

<span class="modifier">static</span> `$port` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$ip`</span> ,
<span class="methodparam"><span class="type">string</span>
`$port`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">copy</span> ( <span class="methodparam"><span
class="type">string</span> `$source_file`</span> , <span
class="methodparam"><span class="type">string</span>
`$destination_file`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">create\_directory</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delete</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disconnect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exists</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">file\_info</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">list\_directory</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$level`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">read</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">rename</span> ( <span class="methodparam"><span
class="type">string</span> `$old_path`</span> , <span
class="methodparam"><span class="type">string</span> `$new_path`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">tell</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$read_length`<span
class="initializer"> = 1024</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">write</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$buffer`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

}

属性
----

`host`  

`port`  

phdfs::connect
==============

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::connect</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::\_\_construct
====================

Description

### 说明

<span class="modifier">public</span> <span
class="methodname">phdfs::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$ip`</span> ,
<span class="methodparam"><span class="type">string</span>
`$port`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ip`  

`port`  

### 返回值

phdfs::copy
===========

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::copy</span> ( <span
class="methodparam"><span class="type">string</span>
`$source_file`</span> , <span class="methodparam"><span
class="type">string</span> `$destination_file`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`source_file`  

`destination_file`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::create\_directory
========================

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::create\_directory</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::delete
=============

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::delete</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::\_\_destruct
===================

Description

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">phdfs::\_\_destruct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

phdfs::disconnect
=================

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::disconnect</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::exists
=============

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::exists</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::file\_info
=================

Description

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">phdfs::file\_info</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

### 返回值

Returns array on success 或者在失败时返回 **`FALSE`**.

phdfs::list\_directory
======================

Description

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">phdfs::list\_directory</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$level`<span
class="initializer"> = 0</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

`level`  

### 返回值

Returns array on success 或者在失败时返回 **`FALSE`**.

phdfs::read
===========

Description

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">phdfs::read</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = 0</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

`length`  

### 返回值

phdfs::rename
=============

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::rename</span> ( <span
class="methodparam"><span class="type">string</span> `$old_path`</span>
, <span class="methodparam"><span class="type">string</span>
`$new_path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`old_path`  

`new_path`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

phdfs::tell
===========

Description

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">phdfs::tell</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$read_length`<span
class="initializer"> = 1024</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

`read_length`  

### 返回值

phdfs::write
============

Description

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">phdfs::write</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$buffer`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
0</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  

`buffer`  

`mode`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
