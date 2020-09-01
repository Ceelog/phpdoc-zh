联系信息
--------

如果你有评论、问题的修复、功能的增强，或者想要帮助开发这头野兽，你可以给我投封邮件
<a href="mailto:alan_k@php.net" class="link external">» alan_k@php.net</a>。
非常欢迎任何您的帮助！

bcompiler\_load\_exe
====================

从一个 bcompiler exe 文件中读取并创建类

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_load\_exe</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

从一个 bcompiler exe 文件中读取数据并根据字节码创建类。

### 参数

`filename`  
exe文件的路径，是一个字符串。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_load\_exe</span> 例子**

``` php
<?php

bcompiler_load_exe("/tmp/example.exe");
print_r(get_defined_classes());

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_load</span>

bcompiler\_load
===============

从一个 bz 压缩过的文件中读取并创建类

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_load</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

从一个 bz 压缩过的文件中读取数据，并根据字节码创建类。

### 参数

`filename`  
bz压缩过的文件路径，是一个字符串。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_load</span> 例子**

``` php
<?php

bcompiler_load("/tmp/example");

print_r(get_defined_classes());

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

> **Note**:
>
> 请使用 include 或 require
> 语句解析字节码，这是种比使用本函数更轻便的方式。
>
> 请注意该函数不会执行字节码文件中包含的脚本主体代码。

### 参见

-   <span class="function">bcompiler\_load\_exe</span>

bcompiler\_parse\_class
=======================

读取一个类的字节码并回调一个用户的函数

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_parse\_class</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$callback`</span> )

读取一个类的字节码并回调一个用户的函数。

### 参数

`class`  
字符串，类名。

`callback`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_parse\_class</span> 例子**

``` php
<?php

function readByteCodes($data) {
    print_r($data);
}

bcompiler_parse_class("DB","readByteCodes");

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

> **Note**:
>
> 自 bcompiler 0.5 起，该函数已从 bcompiler 中删除并不再有效。

bcompiler\_read
===============

从一个文件句柄中读取并创建类

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_read</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> )

从一个打开的文件句柄中读取数据，并从字节码中创建类。

### 参数

`filehandle`  
<span class="function">fopen</span> 返回的文件句柄。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_read</span> 例子**

``` php
<?php
$fh = fopen("/tmp/example","r");
bcompiler_read($fh);
fclose($fh);
print_r(get_defined_classes());

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

> **Note**:
>
> 请使用 include 或 require
> 语句解析字节码，这是种比使用本函数更轻便的方式。
>
> 请注意该函数不会执行字节码文件中包含的脚本主体代码。

bcompiler\_write\_class
=======================

写入定义过的类的字节码

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_class</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">string</span> `$className`</span> \[, <span
class="methodparam"><span class="type">string</span> `$extends`</span>
\] )

从 PHP 读取已存在的类的字节码，并把它们写入打开的文件句柄中。

### 参数

`filehandle`  
<span class="function">fopen</span> 返回的文件句柄。

`className`  
字符串的类名。

`extends`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_class</span> 例子**

``` php
<?php
$fh = fopen("/tmp/example","w");
bcompiler_write_header($fh);
bcompiler_write_class($fh,"DB");
// 你必须先于 DB_mysql 写入 DB_common，因为DB_mysql extends DB_common。
bcompiler_write_class($fh,"DB_common");
bcompiler_write_class($fh,"DB_mysql");
bcompiler_write_footer($fh);
fclose($fh);

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

> **Note**:
>
> 该函数不会执行依赖检查，所以确保你写入类的顺序，防止在加载的时候导致
> *undefined class* 错误。

### 参见

-   <span class="function">bcompiler\_write\_header</span>
-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_constant
==========================

写入定义过的常量的字节码

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_constant</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">string</span> `$constantName`</span> )

从 PHP 读取存在的常量的字节码并把它们写入打开的文件句柄中。

### 参数

`filehandle`  
一个由 <span class="function">fopen</span> 打开并返回的文件句柄。

`constantName`  
定义过的常量名，是一个字符串。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_constant</span>
例子**

``` php
<?php
define("MODULE_MAX", 30);

$fh = fopen("/tmp/example","w");
bcompiler_write_header($fh);
bcompiler_write_constant($fh,"MODULE_MAX");
bcompiler_write_footer($fh);
fclose($fh);

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_header</span>
-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_exe\_footer
=============================

写入开始位置以及 exe 类型文件的结尾信号

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_exe\_footer</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">int</span> `$startpos`</span> )

一个 EXE（或可自执行）文件由 3 部分组成：

-   The *stub* （可执行代码，例如一个编译过的 c 程序） 加载了 PHP
    解释器、bcompiler 扩展、储存的字节码并初始化调用指定函数（例如
    main） 或类的方法（例如 *main::main*）。
-   字节码（仅在那时未压缩）
-   bcompiler 的 EXE 尾部

为了得到适合的 stub 你可以编译位于 bcompiler CVS `examples/embed` 目录里
基于 php\_embed 的 stub `phpe.c`。

### 参数

`filehandle`  
<span class="function">fopen</span>返回的一个文件句柄。

`startpos`  
字节码在文件中开始的位置，可以通过 <span class="function">ftell</span>
获取。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_exe\_footer</span>
例子**

``` php
<?php

/* 创建输出的文件（example.exe） */
$fh = fopen("example.exe", "w");

/* 1) 写入一个 stub （phpe.exe） */
$size = filesize("phpe.exe");
$fr = fopen("phpe.exe", "r");
fwrite($fh, fread($fr, $size), $size);
$startpos = ftell($fh);

/* 2) 写入字节码 */
bcompiler_write_header($fh);
bcompiler_write_class($fh, "myclass");
bcompiler_write_function($fh, "main");
bcompiler_write_footer($fh);

/* 3) 写入 EXE 尾部 */
bcompiler_write_exe_footer($fh, $startpos);

/* 关闭输出的文件 */
fclose($fh);
?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_header</span>
-   <span class="function">bcompiler\_write\_class</span>
-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_file
======================

写入 PHP 源码文件的字节码

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_file</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

这个函数将指定的源码编译成字节码，并将它们写入打开的文件句柄中。

### 参数

`filehandle`  
<span class="function">fopen</span> 返回的一个文件句柄。

`filename`  
源码文件路径，字符串的形式。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_file</span> 例子**

``` php
<?php
$fh = fopen("example.phb", "w");
bcompiler_write_header($fh);
bcompiler_write_file($fh, "example.php");
bcompiler_write_footer($fh);
fclose($fh);
/* 以下是相等的：
include "example.php";
   和
include "example.phb";
*/
?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_header</span>
-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_footer
========================

写入单个字符 \\x00 用于标识编译数据的结尾

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_footer</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> )

写入单个字符 *\\x00* 用于标识编译数据的结尾。

### 参数

`filehandle`  
<span class="function">fopen</span> 打开的一个文件句柄。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_footer</span> 例子**

``` php
<?php
$fh = fopen("/tmp/example","w");
bcompiler_write_header($fh);
bcompiler_write_class($fh,"DB");
bcompiler_write_class($fh,"DB_common");
bcompiler_write_footer($fh);
fclose($fh);

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_header</span>

bcompiler\_write\_function
==========================

以字节码写入定义过的函数

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_function</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">string</span> `$functionName`</span> )

从 PHP
读取现存函数的字节码，并把它们写入打开的文件句柄中。顺序并不重要。
（例如假设函数 b 用到了函数
a，你以下面的例子那样编译它们，将会工作得很好）

### 参数

`filehandle`  
<span class="function">fopen</span> 返回的一个文件句柄。

`functionName`  
函数名，字符串的形式。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_function</span>
例子**

``` php
<?php
$fh = fopen("/tmp/example","w");
bcompiler_write_header($fh);
bcompiler_write_function($fh,"my_function_a");
bcompiler_write_function($fh,"my_function_b");
bcompiler_write_footer($fh);
fclose($fh);

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_header</span>
-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_functions\_from\_file
=======================================

以字节码写入一个文件中定义过的所以函数

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_functions\_from\_file</span> (
<span class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">string</span> `$fileName`</span> )

从给定的文件中搜索定义过的所有函数，并把它们对应的字节码写入打开的文件句柄中。

### 参数

`filehandle`  
<span class="function">fopen</span> 打开并返回的一个文件句柄。

`fileName`  
要编译的文件。你总是必须 inculde 或 require 这个想要编译的文件。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="function">bcompiler\_write\_functions\_from\_file</span> 例子**

``` php
<?php
require('module.php');

$fh = fopen("/tmp/example","w");
bcompiler_write_header($fh);
bcompiler_write_functions_from_file($fh,'module.php');
bcompiler_write_footer($fh);
fclose($fh);

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_header</span>
-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_header
========================

写入 bcompiler 头

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_header</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> \[, <span class="methodparam"><span
class="type">string</span> `$write_ver`</span> \] )

写入一个 bcompiler 文件的头部。

### 参数

`filehandle`  
<span class="function">fopen</span> 返回的一个文件句柄。

`write_ver`  
能够用以前使用的格式写入字节码，这样就可以在较旧的 bcompiler
版本中使用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcompiler\_write\_header</span> 例子**

``` php
<?php
$fh = fopen("/tmp/example","w");
bcompiler_write_header($fh);
bcompiler_write_class($fh,"DB");
bcompiler_write_footer($fh);
fclose($fh);

?>
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">bcompiler\_write\_footer</span>

bcompiler\_write\_included\_filename
====================================

写入一个包含的文件的字节码

### 说明

<span class="type">bool</span> <span
class="methodname">bcompiler\_write\_included\_filename</span> ( <span
class="methodparam"><span class="type">resource</span>
`$filehandle`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**目录**

-   [bcompiler\_load\_exe](/ref/bcompiler.html#bcompiler_load_exe) —
    从一个 bcompiler exe 文件中读取并创建类
-   [bcompiler\_load](/ref/bcompiler.html#bcompiler_load) — 从一个 bz
    压缩过的文件中读取并创建类
-   [bcompiler\_parse\_class](/ref/bcompiler.html#bcompiler_parse_class)
    — 读取一个类的字节码并回调一个用户的函数
-   [bcompiler\_read](/ref/bcompiler.html#bcompiler_read) —
    从一个文件句柄中读取并创建类
-   [bcompiler\_write\_class](/ref/bcompiler.html#bcompiler_write_class)
    — 写入定义过的类的字节码
-   [bcompiler\_write\_constant](/ref/bcompiler.html#bcompiler_write_constant)
    — 写入定义过的常量的字节码
-   [bcompiler\_write\_exe\_footer](/ref/bcompiler.html#bcompiler_write_exe_footer)
    — 写入开始位置以及 exe 类型文件的结尾信号
-   [bcompiler\_write\_file](/ref/bcompiler.html#bcompiler_write_file) —
    写入 PHP 源码文件的字节码
-   [bcompiler\_write\_footer](/ref/bcompiler.html#bcompiler_write_footer)
    — 写入单个字符 \\x00 用于标识编译数据的结尾
-   [bcompiler\_write\_function](/ref/bcompiler.html#bcompiler_write_function)
    — 以字节码写入定义过的函数
-   [bcompiler\_write\_functions\_from\_file](/ref/bcompiler.html#bcompiler_write_functions_from_file)
    — 以字节码写入一个文件中定义过的所以函数
-   [bcompiler\_write\_header](/ref/bcompiler.html#bcompiler_write_header)
    — 写入 bcompiler 头
-   [bcompiler\_write\_included\_filename](/ref/bcompiler.html#bcompiler_write_included_filename)
    — 写入一个包含的文件的字节码
