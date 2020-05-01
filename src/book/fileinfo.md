文件信息
========

**目录**

-   [简介](/intro/fileinfo.html)
-   [安装／配置](/fileinfo/setup.html)
    -   [需求](/fileinfo/setup.html#需求)
    -   [安装](/fileinfo/setup.html#安装)
    -   [运行时配置](/fileinfo/setup.html#运行时配置)
    -   [资源类型](/fileinfo/setup.html#资源类型)
-   [预定义常量](/fileinfo/constants.html)
-   [Fileinfo 函数](/ref/fileinfo.html)
    -   [finfo\_buffer](/ref/fileinfo.html#finfo_buffer) —
        返回一个字符串缓冲区的信息
    -   [finfo\_close](/ref/fileinfo.html#finfo_close) — 关闭 fileinfo
        资源
    -   [finfo\_file](/ref/fileinfo.html#finfo_file) —
        返回一个文件的信息
    -   [finfo\_open](/ref/fileinfo.html#finfo_open) — 创建一个 fileinfo
        资源
    -   [finfo\_set\_flags](/ref/fileinfo.html#finfo_set_flags) — 设置
        libmagic 配置选项
    -   [mime\_content\_type](/ref/fileinfo.html#mime_content_type) —
        检测文件的 MIME 类型
-   [finfo](/class/finfo.html) — finfo 类
    -   [finfo::buffer](/class/finfo.html#finfo::buffer) — 别名
        finfo\_buffer()
    -   [finfo::\_\_construct](/class/finfo.html#finfo::__construct) —
        别名 finfo\_open
    -   [finfo::file](/class/finfo.html#finfo::file) — 别名
        finfo\_file()
    -   [finfo::set\_flags](/class/finfo.html#finfo::set_flags) — 别名
        finfo\_set\_flags()

简介
----

该类在 fileinfo 函数集中提供了一个面向对象的接口。

类摘要
------

**finfo**

<span class="ooclass"> class **finfo** </span> {

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$magic_file`<span
class="initializer"> = ""</span></span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">buffer</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">file</span> ( <span class="methodparam"><span
class="type">string</span> `$file_name`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set\_flags</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

}

finfo::buffer
=============

别名
<a href="/ref/fileinfo.html#finfo_buffer" class="link">finfo_buffer()</a>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">finfo::buffer</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = FILEINFO\_NONE</span></span> \[,
<span class="methodparam"><span class="type">resource</span>
`$context`</span> \]\] )

此函数是该函数的别名：
<a href="/ref/fileinfo.html#finfo_buffer" class="link">finfo_buffer()</a>

finfo::\_\_construct
====================

别名 <span class="function">finfo\_open</span>

### 说明

<span class="modifier">public</span> <span
class="methodname">finfo::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = FILEINFO\_NONE</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$magic_file`<span
class="initializer"> = ""</span></span> \]\] )

此函数是该函数的别名： <span class="function">finfo\_open</span>

finfo::file
===========

别名
<a href="/ref/fileinfo.html#finfo_file" class="link">finfo_file()</a>

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">finfo::file</span> ( <span
class="methodparam"><span class="type">string</span> `$file_name`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = FILEINFO\_NONE</span></span> \[,
<span class="methodparam"><span class="type">resource</span>
`$context`</span> \]\] )

此函数是该函数的别名：
<a href="/ref/fileinfo.html#finfo_file" class="link">finfo_file()</a>

finfo::set\_flags
=================

别名
<a href="/ref/fileinfo.html#finfo_set_flags" class="link">finfo_set_flags()</a>

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">finfo::set\_flags</span> ( <span
class="methodparam"><span class="type">int</span> `$options`</span> )

此函数是该函数的别名：
<a href="/ref/fileinfo.html#finfo_set_flags" class="link">finfo_set_flags()</a>
