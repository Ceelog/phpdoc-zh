Constant hash database
======================

**目录**

-   [简介](/intro/chdb.html)
-   [安装／配置](/chdb/setup.html)
    -   [需求](/chdb/setup.html#需求)
    -   [安装](/chdb/setup.html#安装)
    -   [运行时配置](/chdb/setup.html#运行时配置)
    -   [资源类型](/chdb/setup.html#资源类型)
-   [预定义常量](/chdb/constants.html)
-   [范例](/chdb/examples.html)
-   [chdb](/class/chdb.html) — The chdb class
    -   [chdb::\_\_construct](/class/chdb.html#chdb::__construct) —
        Creates a chdb instance
    -   [chdb::get](/class/chdb.html#chdb::get) — Gets the value
        associated with a key
-   [chdb 函数](/ref/chdb.html)
    -   [chdb\_create](/ref/chdb.html#chdb_create) — Creates a chdb file

简介
----

Represents a loaded chdb file.

类摘要
------

**chdb**

<span class="ooclass"> class **chdb** </span> {

/\* Methods \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$pathname`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> )

}

chdb::\_\_construct
===================

Creates a <span class="classname">chdb</span> instance

### 说明

<span class="modifier">public</span> <span
class="methodname">chdb::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$pathname`</span>
)

Loads a chdb file, by mapping it into memory.

> **Note**:
>
> While some validity checks are performed on the specified file, they
> are mostly there to avoid the possibility of common mistakes (for
> example, loading a file which is not a chdb database, or that is
> somehow incompatible with the current system). A maliciously crafted
> chdb file can thus be dangerous if loaded, so chdb files should be
> trusted and treated with the same security protections used for PHP
> shared libraries.

### 参数

`pathname`  
The name of the file to load.

### 错误／异常

Throws an exception in case the chdb file hasn't been successfully
loaded.

> **Note**:
>
> A valid chdb file might fail to load in case it was created on an
> architecture with a different endianness, with a different version of
> chdb, or if the file is too big to be mapped into memory (mostly in
> case of huge files and 32-bit architectures). In these cases the load
> will fail by throwing an exception, but otherwise not performing any
> illegal operation.

chdb::get
=========

Gets the value associated with a key

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">chdb::get</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Gets the value associated with a key from a chdb database.

### 参数

`key`  
The key for which to get the value.

### 返回值

Returns a string containing the value associated with the given `key`,
or **`NULL`** if not found.

### 范例

**示例 \#1 <span class="function">chdb::get</span> example**

``` php
<?php

$data = array(
    'key1' => 'value1',
    'key2' => 'value2',
    // ...
);
chdb_create('data.chdb', $data);

$chdb = new chdb('data.chdb');
$value1 = $chdb->get('key1');
$value2 = $chdb->get('key2');

echo $value1, PHP_EOL;
echo $value2, PHP_EOL;

?>
```

以上例程的输出类似于：

    value1
    value2
