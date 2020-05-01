finfo\_buffer
=============

finfo::buffer
=============

返回一个字符串缓冲区的信息

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">finfo\_buffer</span> ( <span
class="methodparam"><span class="type">resource</span> `$finfo`</span> ,
<span class="methodparam"><span class="type">string</span>
`$string`<span class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">finfo::buffer</span> ( <span
class="methodparam"><span class="type">string</span> `$string`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

本函数用来获取字符串中二进制数据的信息。

### 参数

`finfo`  
<span class="function">finfo\_open</span> 函数返回的 Fileinfo 资源。

`string`  
要检查的文件内容。

`options`  
一个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
或多个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
进行逻辑或运算。

`context`  

### 返回值

返回 `string` 参数所指定内容的类型描述。 发生错误时返回 **`FALSE`** 。

### 范例

**示例 \#1 <span class="function">finfo\_buffer</span> 函数例程**

``` php
<?php
$finfo = new finfo(FILEINFO_MIME);
echo $finfo->buffer($_POST["script"]) . "\n";
?>
```

以上例程的输出类似于：

    application/x-sh; charset=us-ascii

### 参见

-   <span class="function">finfo\_file</span>

finfo\_close
============

关闭 fileinfo 资源

### 说明

<span class="type">bool</span> <span
class="methodname">finfo\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$finfo`</span> )

关闭 <span class="function">finfo\_open</span> 函数所返回的 fileinfo
资源。

### 参数

`finfo`  
<span class="function">finfo\_open</span> 函数所返回的 fileinfo 资源。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

finfo\_file
===========

finfo::file
===========

返回一个文件的信息

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">finfo\_file</span> ( <span class="methodparam"><span
class="type">resource</span> `$finfo`</span> , <span
class="methodparam"><span class="type">string</span> `$file_name`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">finfo::file</span> ( <span
class="methodparam"><span class="type">string</span> `$file_name`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

本函数用来获取一个文件的信息。

### 参数

`finfo`  
<span class="function">finfo\_open</span> 函数所返回的 fileinfo 资源。

`file_name`  
要检查的文件名。

`options`  
一个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
或多个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
进行逻辑或运算。

`context`  
关于 *contexts* 的更多描述，请参考
<a href="/ref/stream.html" class="xref">Stream 函数</a>。

### 返回值

返回 `file_name` 参数指定的文件信息。 发生错误时返回 **`FALSE`** 。

### 范例

**示例 \#1 <span class="function">finfo\_file</span> 例程**

``` php
<?php
$finfo = finfo_open(FILEINFO_MIME_TYPE); // 返回 mime 类型
foreach (glob("*") as $filename) {
    echo finfo_file($finfo, $filename) . "\n";
}
finfo_close($finfo);
?>
```

以上例程的输出类似于：

    text/html
    image/gif
    application/vnd.ms-excel

### 参见

-   <span class="function">finfo\_buffer</span>

finfo\_open
===========

finfo::\_\_construct
====================

创建一个 fileinfo 资源

### 说明

过程化风格

<span class="type">resource</span> <span
class="methodname">finfo\_open</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$magic_file`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

面向对象风格 （构造器）：

<span class="modifier">public</span> <span
class="methodname">finfo::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$magic_file`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

本函数打开一个魔数数据库并且返回它的资源。

### 参数

`options`  
一个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
或多个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
进行逻辑或运算。

`magic_file`  
魔数数据库文件名称， 通常是 `/path/to/magic.mime`。 如果未指定，则使用
*MAGIC* 环境变量。 如果未指定此环境变量， 则使用 PHP 绑定的魔数数据库。

传入 **`NULL`** 或者空字符串，等同于使用默认值。

### 返回值

（仅适用于过程化风格） 如果成功则返回一个表示魔数数据库的资源，
或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

在 PHP 5.3.11 和 5.4.1 中预期的魔数数据库格式发生了变动，
所以，内置的魔数数据库被更新。 如果使用了外部魔数数据库，
可能会由于格式不同导致读取失败。 同时，一些 mime
类型的文字表示也发生了变化， 例如，PHP 文件的 mime 类型由 “"PHP script
text” 变为“PHP script, ASCII text”。

> **Note**:
>
> 通常来说，使用 PHP 绑定的魔数数据库（设置 `magic_file` 参数为空，
> 不设置 *MAGIC* 环境变量）是最好的选择，
> 除非你确实需要一个自定义的魔数数据库。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$finfo = new finfo(FILEINFO_MIME, "/usr/share/misc/magic"); // 返回 mime 类型

/* get mime-type for a specific file */
$filename = "/usr/local/something.txt";
echo $finfo->file($filename);

?>
```

**示例 \#2 过程化风格**

``` php
<?php
$finfo = finfo_open(FILEINFO_MIME, "/usr/share/misc/magic"); // 返回 mime 类型

if (!$finfo) {
    echo "Opening fileinfo database failed";
    exit();
}

/* 获取指定文件的 mime 类型 */
$filename = "/usr/local/something.txt";
echo finfo_file($finfo, $filename);

/* 关闭资源 */
finfo_close($finfo);
?>
```

以上例程会输出：

    text/plain; charset=us-ascii

### 参见

-   <span class="function">finfo\_close</span>

finfo\_set\_flags
=================

finfo::set\_flags
=================

设置 libmagic 配置选项

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">finfo\_set\_flags</span> ( <span
class="methodparam"><span class="type">resource</span> `$finfo`</span> ,
<span class="methodparam"><span class="type">int</span>
`$options`</span> )

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">finfo::set\_flags</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

此函数用来设置 Fileinfo 选项。 这些选项也可以在调用 <span
class="function">finfo\_open</span> 或者其他 Fileinfo 函数时直接指定。

### 参数

`finfo`  
<span class="function">finfo\_open</span> 返回的资源。

`options`  
一个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
或多个 <a href="/fileinfo/constants.html" class="link">Fileinfo 常量</a>
进行逻辑或运算。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

mime\_content\_type
===================

检测文件的 MIME 类型

### 说明

<span class="type">string</span> <span
class="methodname">mime\_content\_type</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

返回通过使用 `magic.mime` 检测到的文件 MIME 类型。

### 参数

`filename`  
要检测的文件名。

### 返回值

返回文件的 MIME 内容类型，例如 *text/plain* 或
*application/octet-stream*。 或者在失败时返回 **`FALSE`**。

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 范例

**示例 \#1 <span class="function">mime\_content\_type</span> 示例**

``` php
<?php
echo mime_content_type('php.gif') . "\n";
echo mime_content_type('test.php');
?>
```

以上例程会输出：

    image/gif
    text/plain

### 参见

-   <span class="function">finfo\_file</span>
-   <span class="function">finfo\_buffer</span>

**目录**

-   [finfo\_buffer](/ref/fileinfo.html#finfo_buffer) —
    返回一个字符串缓冲区的信息
-   [finfo\_close](/ref/fileinfo.html#finfo_close) — 关闭 fileinfo 资源
-   [finfo\_file](/ref/fileinfo.html#finfo_file) — 返回一个文件的信息
-   [finfo\_open](/ref/fileinfo.html#finfo_open) — 创建一个 fileinfo
    资源
-   [finfo\_set\_flags](/ref/fileinfo.html#finfo_set_flags) — 设置
    libmagic 配置选项
-   [mime\_content\_type](/ref/fileinfo.html#mime_content_type) —
    检测文件的 MIME 类型
