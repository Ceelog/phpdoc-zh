filePro
=======

**目录**

-   [简介](/book/filepro.html#简介)
-   [安装／配置](/book/filepro.html#安装／配置)
    -   [需求](/book/filepro.html#需求)
    -   [安装](/book/filepro.html#安装)
    -   [运行时配置](/book/filepro.html#运行时配置)
    -   [资源类型](/book/filepro.html#资源类型)
-   [预定义常量](/book/filepro.html#预定义常量)
-   [filePro 函数](/book/filepro.html#filePro%20函数)
    -   [filepro\_fieldcount](/book/filepro.html#filepro_fieldcount) —
        Find out how many fields are in a filePro database
    -   [filepro\_fieldname](/book/filepro.html#filepro_fieldname) —
        Gets the name of a field
    -   [filepro\_fieldtype](/book/filepro.html#filepro_fieldtype) —
        Gets the type of a field
    -   [filepro\_fieldwidth](/book/filepro.html#filepro_fieldwidth) —
        Gets the width of a field
    -   [filepro\_retrieve](/book/filepro.html#filepro_retrieve) —
        Retrieves data from a filePro database
    -   [filepro\_rowcount](/book/filepro.html#filepro_rowcount) — Find
        out how many rows are in a filePro database
    -   [filepro](/book/filepro.html#filepro) — Read and verify the map
        file

These functions allow read-only access to data stored in filePro
databases.

filePro is a registered trademark of fP Technologies, Inc. You can find
more information about filePro at
<a href="http://www.fptech.com/" class="link external">» http://www.fptech.com/</a>.

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.2.0.

安装／配置
==========

**目录**

-   [需求](/book/filepro.html#需求)
-   [安装](/book/filepro.html#安装)
-   [运行时配置](/book/filepro.html#运行时配置)
-   [资源类型](/book/filepro.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

此扩展已被移至
<a href="https://pecl.php.net/" class="link external">» PECL</a>
资源库且不再与 PHP 捆绑。5.2.0

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/filepro" class="link external">» https://pecl.php.net/package/filepro</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。

预定义常量
==========

此扩展没有定义常量。

filepro\_fieldcount
===================

Find out how many fields are in a filePro database

### 说明

<span class="type">int</span> <span
class="methodname">filepro\_fieldcount</span> ( <span
class="methodparam">void</span> )

Returns the number of fields (columns) in the opened filePro database.

### 返回值

Returns the number of fields in the opened filePro database, or
**`FALSE`** on errors.

### 参见

-   <span class="function">filepro</span>

filepro\_fieldname
==================

Gets the name of a field

### 说明

<span class="type">string</span> <span
class="methodname">filepro\_fieldname</span> ( <span
class="methodparam"><span class="type">int</span> `$field_number`</span>
)

Returns the name of the field corresponding to `field_number`.

### 参数

`field_number`  
The field number.

### 返回值

Returns the name of the field as a string, or **`FALSE`** on errors.

filepro\_fieldtype
==================

Gets the type of a field

### 说明

<span class="type">string</span> <span
class="methodname">filepro\_fieldtype</span> ( <span
class="methodparam"><span class="type">int</span> `$field_number`</span>
)

Returns the edit type of the field corresponding to `field_number`.

### 参数

`field_number`  
The field number.

### 返回值

Returns the edit type of the field as a string, or **`FALSE`** on
errors.

filepro\_fieldwidth
===================

Gets the width of a field

### 说明

<span class="type">int</span> <span
class="methodname">filepro\_fieldwidth</span> ( <span
class="methodparam"><span class="type">int</span> `$field_number`</span>
)

Returns the width of the field corresponding to `field_number`.

### 参数

`field_number`  
The field number.

### 返回值

Returns the width of the field as a integer, or **`FALSE`** on errors.

filepro\_retrieve
=================

Retrieves data from a filePro database

### 说明

<span class="type">string</span> <span
class="methodname">filepro\_retrieve</span> ( <span
class="methodparam"><span class="type">int</span> `$row_number`</span> ,
<span class="methodparam"><span class="type">int</span>
`$field_number`</span> )

Returns the data from the specified location in the database.

### 参数

`row_number`  
The row number. Must be between zero and the total number of rows minus
one (0..<span class="function">filepro\_rowcount</span> - 1)

`field_number`  
The field number. Accepts values between zero and the total number of
fields minus one (0..<span class="function">filepro\_fieldcount</span> -
1)

### 返回值

Returns the specified data, or **`FALSE`** on errors.

filepro\_rowcount
=================

Find out how many rows are in a filePro database

### 说明

<span class="type">int</span> <span
class="methodname">filepro\_rowcount</span> ( <span
class="methodparam">void</span> )

Returns the number of rows in the opened filePro database.

### 返回值

Returns the number of rows in the opened filePro database, or
**`FALSE`** on errors.

### 参见

-   <span class="function">filepro</span>

filepro
=======

Read and verify the map file

### 说明

<span class="type">bool</span> <span class="methodname">filepro</span> (
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

This reads and verifies the map file, storing the field count and info.

No locking is done, so you should avoid modifying your filePro database
while it may be opened in PHP.

### 参数

`directory`  
The map directory.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**目录**

-   [filepro\_fieldcount](/book/filepro.html#filepro_fieldcount) — Find
    out how many fields are in a filePro database
-   [filepro\_fieldname](/book/filepro.html#filepro_fieldname) — Gets
    the name of a field
-   [filepro\_fieldtype](/book/filepro.html#filepro_fieldtype) — Gets
    the type of a field
-   [filepro\_fieldwidth](/book/filepro.html#filepro_fieldwidth) — Gets
    the width of a field
-   [filepro\_retrieve](/book/filepro.html#filepro_retrieve) — Retrieves
    data from a filePro database
-   [filepro\_rowcount](/book/filepro.html#filepro_rowcount) — Find out
    how many rows are in a filePro database
-   [filepro](/book/filepro.html#filepro) — Read and verify the map file
