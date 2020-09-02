chdb\_create
============

新建一个 chdb 文件

### 说明

<span class="type">bool</span> <span
class="methodname">chdb\_create</span> ( <span class="methodparam"><span
class="type">string</span> `$pathname`</span> , <span
class="methodparam"><span class="type">array</span> `$data`</span> )

<span class="function">chdb\_create</span> 创建一个内容包含指定键值对的
chdb 文件。

> **Note**:
>
> chdb
> 文件在小字节序（little-endian）和大字节序（big-endian）环境中是不可移植的。除此以外，它们在不同的架构下是可以移植的。而且不同版本的
> chdb 的兼容性也不能保证。

### 参数

`pathname`  
要创建文件的路径。

如果文件已存在，则会被覆盖。

`data`  
指定键值对的数组。

键值在写入到文件前，会被转换成字符串，因为 chdb
文件仅支持字符串类型。需要注意，二进制字符串同样被支持。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

创建不成功将抛出一个错误。

### 范例

**示例 \#1 <span class="function">chdb\_create</span> 示例**

``` php
<?php

$data = array(
    'key1' => 'value1',
    'key2' => 'value2',
    // ...
);
chdb_create('data.chdb', $data);

?>
```

上例将会生成一个包含 `$data` 数据的文件，文件名为 *data.chdb*。

**目录**

-   [chdb\_create](/ref/chdb.html#chdb_create) — 新建一个 chdb 文件
