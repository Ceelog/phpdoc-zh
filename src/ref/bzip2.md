bzclose
=======

关闭一个 bzip2 文件

### 说明

<span class="type">bool</span> <span class="methodname">bzclose</span> (
<span class="methodparam"><span class="type">resource</span>
`$bz`</span> )

关闭给出的 bzip2 文件指针。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">bzopen</span>

bzcompress
==========

把一个字符串压缩成 bzip2 编码数据

### 说明

<span class="type">mixed</span> <span
class="methodname">bzcompress</span> ( <span class="methodparam"><span
class="type">string</span> `$source`</span> \[, <span
class="methodparam"><span class="type">int</span> `$blocksize`<span
class="initializer"> = 4</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$workfactor`<span
class="initializer"> = 0</span></span> \]\] )

<span class="function">bzcompress</span> 压缩了指定的字符串并以 bzip2
编码返回数据。

### 参数

`source`  
待压缩的字符串。

`blocksize`  
指定压缩时使用的块大小，应该是一个 1-9 的数字。9
可以有最高的压缩比，但会使用更多的资源。

`workfactor`  
控制压缩阶段出现最坏的重复性高的情况下输入数据时的行为。 该值可以是在 0
至 250 之间，0是一个特殊的情况。

无论 `workfactor`是什么，产生的输出都是一致的。

### 返回值

压缩后的字符串，或者在出现错误时返回错误号。

### 范例

**示例 \#1 压缩数据**

``` php
<?php
$str = "sample data";
$bzstr = bzcompress($str, 9);
echo $bzstr;
?>
```

### 参见

-   <span class="function">bzdecompress</span>

bzdecompress
============

解压经 bzip2 编码过的数据

### 说明

<span class="type">mixed</span> <span
class="methodname">bzdecompress</span> ( <span class="methodparam"><span
class="type">string</span> `$source`</span> \[, <span
class="methodparam"><span class="type">int</span> `$small`<span
class="initializer"> = 0</span></span> \] )

<span class="function">bzdecompress</span> 解压了包含 bzip2
压缩数据的指定字符串。

### 参数

`source`  
要解压的字符串。

`small`  
如果为
**`TRUE`**，将会使用一种内存开销更小的替代算法（最大内存需求降低至大约
2300K）但速度会降低约一半。

寻找该功能的更多信息可参见
<a href="https://www.sourceware.org/bzip2/" class="link external">» bzip2 文档</a>。

### 返回值

解压后的字符串，如果发生了一个错误则返回一个错误码。

### 范例

**示例 \#1 解压一个字符串**

``` php
<?php
$start_str = "This is not an honest face?";
$bzstr = bzcompress($start_str);

echo "Compressed String: ";
echo $bzstr;
echo "\n<br />\n";

$str = bzdecompress($bzstr);
echo "Decompressed String: ";
echo $str;
echo "\n<br />\n";
?>
```

### 参见

-   <span class="function">bzcompress</span>

bzerrno
=======

返回一个 bzip2 错误码

### 说明

<span class="type">int</span> <span class="methodname">bzerrno</span> (
<span class="methodparam"><span class="type">resource</span>
`$bz`</span> )

返回指定文件指针任意返回的 bzip2 错误的错误码。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

### 返回值

返回 integer 的错误码。

### 参见

-   <span class="function">bzerror</span>
-   <span class="function">bzerrstr</span>

bzerror
=======

返回包含 bzip2 错误号和错误字符串的一个 array

### 说明

<span class="type">array</span> <span class="methodname">bzerror</span>
( <span class="methodparam"><span class="type">resource</span>
`$bz`</span> )

返回文件指针中返回的 bzip2 错误的错误号和错误字符串。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

### 返回值

返回一个关联数组，包含错误码于 *errno* 条目， 以及错误信息于 *errstr*
条目。

### 范例

**示例 \#1 <span class="function">bzerror</span> 范例**

``` php
<?php
$error = bzerror($bz);

echo $error["errno"];
echo $error["errstr"];
?>
```

### 参见

-   <span class="function">bzerrno</span>
-   <span class="function">bzerrstr</span>

bzerrstr
========

返回一个 bzip2 的错误字符串

### 说明

<span class="type">string</span> <span
class="methodname">bzerrstr</span> ( <span class="methodparam"><span
class="type">resource</span> `$bz`</span> )

获取指定文件指针中返回 bzip2 任何错误的错误字符串。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

### 返回值

返回包含错误信息的 string。

### 参见

-   <span class="function">bzerrno</span>
-   <span class="function">bzerror</span>

bzflush
=======

强制写入所有写缓冲区的数据

### 说明

<span class="type">bool</span> <span class="methodname">bzflush</span> (
<span class="methodparam"><span class="type">resource</span>
`$bz`</span> )

强制写入 bzip2 文件指针 `bz` 的所有写缓冲数据。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">bzread</span>
-   <span class="function">bzwrite</span>

bzopen
======

打开 bzip2 压缩文件

### 说明

<span class="type">resource</span> <span
class="methodname">bzopen</span> ( <span class="methodparam"><span
class="type">mixed</span> `$file`</span> , <span
class="methodparam"><span class="type">string</span> `$mode`</span> )

<span class="function">bzopen</span> 打开一个
bzip2（.bz2）文件用于读或写。

### 参数

`file`  
待打开的文件的文件名，或者已经存在的资源流。

`mode`  
支持 'r'（读）和 'w'（写）模式。 其他任何模式都会导致 <span
class="function">bzopen</span> 返回 **`FALSE`**。

### 返回值

如果打开失败，<span class="function">bzopen</span> 会返回
**`FALSE`**，否则返回一个指向最新打开文件的指针。

### 范例

**示例 \#1 <span class="function">bzopen</span> 范例**

``` php
<?php

$file = "/tmp/foo.bz2";
$bz = bzopen($file, "r") or die("Couldn't open $file for reading");

bzclose($bz);

?>
```

### 参见

-   <span class="function">bzclose</span>

bzread
======

bzip2 文件二进制安全地读取

### 说明

<span class="type">string</span> <span class="methodname">bzread</span>
( <span class="methodparam"><span class="type">resource</span>
`$bz`</span> \[, <span class="methodparam"><span class="type">int</span>
`$length`<span class="initializer"> = 1024</span></span> \] )

<span class="function">bzread</span> 从指定的 bzip2 文件指针中读取数据。

读取到 `length`（未经压缩的长度）个字节，或者到文件尾，取决于先到哪个。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

`length`  
如果没有提供， <span class="function">bzread</span> 一次会读入 1024
个字节（未经压缩的长度）。 一次最大可读入 8192 个未压缩的字节。

### 返回值

返回解压的数据，在错误时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bzread</span> 范例**

``` php
<?php

$file = "/tmp/foo.bz2";
$bz = bzopen($file, "r") or die("Couldn't open $file");

$decompressed_file = '';
while (!feof($bz)) {
  $decompressed_file .= bzread($bz, 4096);
}
bzclose($bz);

echo "The contents of $file are: <br />\n";
echo $decompressed_file;

?>
```

### 参见

-   <span class="function">bzwrite</span>
-   <span class="function">feof</span>
-   <span class="function">bzopen</span>

bzwrite
=======

二进制安全地写入 bzip2 文件

### 说明

<span class="type">int</span> <span class="methodname">bzwrite</span> (
<span class="methodparam"><span class="type">resource</span>
`$bz`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

<span class="function">bzwrite</span> 把字符串（string）写入了指定的
bzip2 文件流。

### 参数

`bz`  
文件指针。它必须是有效的并且指向 <span class="function">bzopen</span>
成功打开的文件。

`data`  
要写入的数据。

`length`  
如果提供了这个参数，将仅仅写入 `length`（未压缩）个字节，若 `data`
小于该指定的长度则写入全部数据。

### 返回值

返回写入的数据字节数，错误时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bzwrite</span> 范例**

``` php
<?php
$str = "uncompressed data";
$bz = bzopen("/tmp/foo.bz2", "w");
bzwrite($bz, $str, strlen($str));
bzclose($bz);
?>
```

### 参见

-   <span class="function">bzread</span>
-   <span class="function">bzopen</span>

**目录**

-   [bzclose](/ref/bzip2.html#bzclose) — 关闭一个 bzip2 文件
-   [bzcompress](/ref/bzip2.html#bzcompress) — 把一个字符串压缩成 bzip2
    编码数据
-   [bzdecompress](/ref/bzip2.html#bzdecompress) — 解压经 bzip2
    编码过的数据
-   [bzerrno](/ref/bzip2.html#bzerrno) — 返回一个 bzip2 错误码
-   [bzerror](/ref/bzip2.html#bzerror) — 返回包含 bzip2
    错误号和错误字符串的一个 array
-   [bzerrstr](/ref/bzip2.html#bzerrstr) — 返回一个 bzip2 的错误字符串
-   [bzflush](/ref/bzip2.html#bzflush) — 强制写入所有写缓冲区的数据
-   [bzopen](/ref/bzip2.html#bzopen) — 打开 bzip2 压缩文件
-   [bzread](/ref/bzip2.html#bzread) — bzip2 文件二进制安全地读取
-   [bzwrite](/ref/bzip2.html#bzwrite) — 二进制安全地写入 bzip2 文件
