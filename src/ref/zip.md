zip\_close
==========

关闭一个ZIP档案文件

### 说明

<span class="type">void</span> <span
class="methodname">zip\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$zip`</span> )

关闭一个指定的ZIP档案文件。

### 参数

`zip`  
一个由<span class="function">zip\_open</span>打开的ZIP文件资源。

### 返回值

没有返回值。

### 参见

-   <span class="function">zip\_open</span>
-   <span class="function">zip\_read</span>

zip\_entry\_close
=================

关闭目录项

### 说明

<span class="type">bool</span> <span
class="methodname">zip\_entry\_close</span> ( <span
class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> )

关闭指定的目录项。

### 参数

`zip_entry`  
一个由<span class="function">zip\_entry\_open</span>打开的项目。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">zip\_entry\_open</span>
-   <span class="function">zip\_entry\_read</span>

zip\_entry\_compressedsize
==========================

检索目录项压缩过后的大小

### 说明

<span class="type">int</span> <span
class="methodname">zip\_entry\_compressedsize</span> ( <span
class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> )

返回指定目录项压缩过后的大小。

### 参数

`zip_entry`  
由函数<span class="function">zip\_read</span> 返回的目录项。

### 返回值

压缩后的大小。

### 参见

-   <span class="function">zip\_open</span>
-   <span class="function">zip\_read</span>

zip\_entry\_compressionmethod
=============================

检索目录实体的压缩方法

### 说明

<span class="type">string</span> <span
class="methodname">zip\_entry\_compressionmethod</span> ( <span
class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> )

返回由函数`zip_entry`确定的目录实体的压缩方法。

### 参数

`zip_entry`  
由函数<span class="function">zip\_read</span> 返回的目录实体。

### 返回值

压缩方法。

### 参见

-   <span class="function">zip\_open</span>
-   <span class="function">zip\_read</span>

zip\_entry\_filesize
====================

检索目录实体的实际大小

### 说明

<span class="type">int</span> <span
class="methodname">zip\_entry\_filesize</span> ( <span
class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> )

返回指定目录实体的实际大小。

### 参数

`zip_entry`  
由函数<span class="function">zip\_read</span> 返回的目录实体。

### 返回值

返回该目录实体的大小。

### 参见

-   <span class="function">zip\_open</span>
-   <span class="function">zip\_read</span>

zip\_entry\_name
================

检索目录项的名称

### 说明

<span class="type">string</span> <span
class="methodname">zip\_entry\_name</span> ( <span
class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> )

返回指定目录项的名称。

### 参数

`zip_entry`  
由函数<span class="function">zip\_read</span> 返回的目录项。

### 返回值

目录项的名称。

### 参见

-   <span class="function">zip\_open</span>
-   <span class="function">zip\_read</span>

zip\_entry\_open
================

打开用于读取的目录实体

### 说明

<span class="type">bool</span> <span
class="methodname">zip\_entry\_open</span> ( <span
class="methodparam"><span class="type">resource</span> `$zip`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> \[, <span class="methodparam"><span
class="type">string</span> `$mode`</span> \] )

打开ZIP文件中的目录实体以便后续读取。

### 参数

`zip`  
由函数<span class="function">zip\_open</span>返回的有效的资源句柄。

`zip_entry`  
由函数<span class="function">zip\_read</span>返回的目录实体。

`mode`  
任何在<span class="function">fopen</span>处理文档中指定的模式。

> **Note**:
>
> 由于ZIP在PHP中只支持读取模式，所以`mode`
> 实际上总是被设置为*"rb"*(其他模式会被忽略)。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

> **Note**:
>
> 与<span class="function">fopen</span>和其他类似的方法不同，<span
> class="function">zip\_entry\_open</span>
> 的返回值只用于标示该操作结果，不需要读取或关闭该目录实体。

### 参见

-   <span class="function">zip\_entry\_close</span>
-   <span class="function">zip\_entry\_read</span>

zip\_entry\_read
================

读取一个打开了的压缩目录实体

### 说明

<span class="type">string</span> <span
class="methodname">zip\_entry\_read</span> ( <span
class="methodparam"><span class="type">resource</span>
`$zip_entry`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`<span class="initializer"> =
1024</span></span> \] )

读取一个打开了的压缩目录实体。

### 参数

`zip_entry`  
由函数<span class="function">zip\_read</span> 返回的目录实体。

`length`  
需要返回的字节数。

> **Note**:
>
> 这字节数应该是你所要读取的未压缩的字节数。

### 返回值

成功的时候返回读取到的数据；到达文件末尾的时候返回一个空的字符串；
读取出错的时候则会返回**`false`**

### 参见

-   <span class="function">zip\_entry\_open</span>
-   <span class="function">zip\_entry\_close</span>
-   <span class="function">zip\_entry\_filesize</span>

zip\_open
=========

打开ZIP存档文件

### 说明

<span class="type">resource</span> <span
class="methodname">zip\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

打开一个新的ZIP归档文件进行读取。

### 参数

`filename`  
待打开ZIP归档的文件名。

### 返回值

成功的时候返回一个资源句柄供函数<span class="function">zip\_read</span>
和 <span class="function">zip\_close</span>后续使用; 如果`filename`
文件不存在或者出现其他错误，则会返回相应的错误码。

### 参见

-   <span class="function">zip\_read</span>
-   <span class="function">zip\_close</span>

zip\_read
=========

读取ZIP存档文件中下一项

### 说明

<span class="type">resource</span> <span
class="methodname">zip\_read</span> ( <span class="methodparam"><span
class="type">resource</span> `$zip`</span> )

读取ZIP存档文件中下一项。

### 参数

`zip`  
一个ZIP压缩文件,该ZIP归档文件之前应由函数 <span
class="function">zip\_open</span> 打开。

### 返回值

成功的时候返回该当前实体资源供*zip\_entry\_...* 系列函数后续使用;
如果没有更多的读取项，则会返回 **`false`**
如果遇到错误则会返回相应的错误码。

### 参见

-   <span class="function">zip\_open</span>
-   <span class="function">zip\_close</span>
-   <span class="function">zip\_entry\_open</span>
-   <span class="function">zip\_entry\_read</span>

**目录**

-   [zip\_close](/ref/zip.html#zip_close) — 关闭一个ZIP档案文件
-   [zip\_entry\_close](/ref/zip.html#zip_entry_close) — 关闭目录项
-   [zip\_entry\_compressedsize](/ref/zip.html#zip_entry_compressedsize)
    — 检索目录项压缩过后的大小
-   [zip\_entry\_compressionmethod](/ref/zip.html#zip_entry_compressionmethod)
    — 检索目录实体的压缩方法
-   [zip\_entry\_filesize](/ref/zip.html#zip_entry_filesize) —
    检索目录实体的实际大小
-   [zip\_entry\_name](/ref/zip.html#zip_entry_name) — 检索目录项的名称
-   [zip\_entry\_open](/ref/zip.html#zip_entry_open) —
    打开用于读取的目录实体
-   [zip\_entry\_read](/ref/zip.html#zip_entry_read) —
    读取一个打开了的压缩目录实体
-   [zip\_open](/ref/zip.html#zip_open) — 打开ZIP存档文件
-   [zip\_read](/ref/zip.html#zip_read) — 读取ZIP存档文件中下一项
