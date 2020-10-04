dBase
=====

**目录**

-   [简介](/book/dbase.html#简介)
-   [安装／配置](/book/dbase.html#安装／配置)
    -   [需求](/book/dbase.html#需求)
    -   [安装](/book/dbase.html#安装)
    -   [运行时配置](/book/dbase.html#运行时配置)
    -   [资源类型](/book/dbase.html#资源类型)
-   [预定义常量](/book/dbase.html#预定义常量)
-   [dBase 函数](/book/dbase.html#dBase%20函数)
    -   [dbase\_add\_record](/book/dbase.html#dbase_add_record) — Adds a
        record to a database
    -   [dbase\_close](/book/dbase.html#dbase_close) — Closes a database
    -   [dbase\_create](/book/dbase.html#dbase_create) — Creates a
        database
    -   [dbase\_delete\_record](/book/dbase.html#dbase_delete_record) —
        Deletes a record from a database
    -   [dbase\_get\_header\_info](/book/dbase.html#dbase_get_header_info)
        — Gets the header info of a database
    -   [dbase\_get\_record\_with\_names](/book/dbase.html#dbase_get_record_with_names)
        — Gets a record from a database as an associative array
    -   [dbase\_get\_record](/book/dbase.html#dbase_get_record) — Gets a
        record from a database as an indexed array
    -   [dbase\_numfields](/book/dbase.html#dbase_numfields) — Gets the
        number of fields of a database
    -   [dbase\_numrecords](/book/dbase.html#dbase_numrecords) — Gets
        the number of records in a database
    -   [dbase\_open](/book/dbase.html#dbase_open) — Opens a database
    -   [dbase\_pack](/book/dbase.html#dbase_pack) — Packs a database
    -   [dbase\_replace\_record](/book/dbase.html#dbase_replace_record)
        — Replaces a record in a database

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.3.0.

These functions allow you to access records stored in dBase-format (dbf)
databases.

**Warning**

We recommend against using dBase files as your production database. Use
<a href="http://sqlite.org/" class="link external">» SQLite</a> or
choose any real SQL server instead;
<a href="http://www.mysql.com/" class="link external">» MySQL</a> or
<a href="http://www.postgresql.org/" class="link external">» Postgres</a>
are common choices with PHP. dBase support is here to allow you to
import and export data to and from your web database, because the file
format is commonly understood by Windows spreadsheets and organizers.

**Caution**

As of dbase 7.0.0 the databases are automatically locked via <span
class="function">flock</span>. There has been no support for locking
earlier, so two concurrent web server processes modifying the same dBase
file would have very likely ruined your database. This can happen even
with dbase 7.0.0+ on systems which implement the locks at the process
level with multithreaded SAPIs.

dBase files are simple sequential files of fixed length records. Records
are appended to the end of the file and deleted records are kept until
you call <span class="function">dbase\_pack</span>.

Only dbf file levels 3 (dBASE III+) - 5 (dBASE V) are supported. The
types of dBase fields available are:

| Field | dBase Type | Format                                                                        | Additional information                                                                                                                                                                                    |
|-------|------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *M*   | Memo       | n/a                                                                           | This type is not supported by PHP, such field will be ignored                                                                                                                                             |
| *D*   | Date       | *YYYYMMDD*                                                                    | The field length is limited to 8                                                                                                                                                                          |
| *T*   | DateTime   | *YYYYMMDDhhmmss.uuu*                                                          | (FoxPro) No validity checks are done. Available as of dbase 7.0.0.                                                                                                                                        |
| *N*   | Number     | A number                                                                      | You must declare a length and a precision (the number of digits after the decimal point).                                                                                                                 |
| *F*   | Float      | A float number                                                                | Same as *N*. Available as of PHP 5.2.0                                                                                                                                                                    |
| *C*   | String     | A string                                                                      | You must declare a length. When retrieving data, the string will be right-padded with spaces to fit the declared length. Overlong strings will be silently truncated when storing data.                   |
| *L*   | Boolean    | *T* or *Y* for **`TRUE`**, *F* or *N* for **`FALSE`**, *?* for uninitialized. | As of dbase 7.0.0, returned as a <span class="type">bool</span> (**`TRUE`** or **`FALSE`**), or **`NULL`** for uninitialized fields. Formerly, returned as an <span class="type">int</span> (*1* or *0*). |

> **Note**:
>
> As of dbase 7.0.0 nullable fields are supported for
> **`DBASE_TYPE_FOXPRO`** databases. If a field is nullable, passing
> **`NULL`** will set the respective flag, and on later retrieval the
> field value will be **`NULL`**.

> **Note**:
>
> There is no support for indexes or memo fields.

安装／配置
==========

**目录**

-   [需求](/book/dbase.html#需求)
-   [安装](/book/dbase.html#安装)
-   [运行时配置](/book/dbase.html#运行时配置)
-   [资源类型](/book/dbase.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/dbase" class="link external">» https://pecl.php.net/package/dbase</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

As of dbase 7.0.0, the resource type *dbase* is defined, which is
returned by <span class="function">dbase\_open</span> and <span
class="function">dbase\_create</span>.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`DBASE_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> The extension version. (Available as of dbase
7.0.0) </span>

**`DBASE_RDONLY`** (<span class="type">int</span>)  
<span class="simpara"> Open database for reading only. Used with <span
class="function">dbase\_open</span>. (Available as of dbase 7.0.0)
</span>

**`DBASE_RDWR`** (<span class="type">int</span>)  
<span class="simpara"> Open database for reading and writing. Used with
<span class="function">dbase\_open</span>. (Available as of dbase 7.0.0)
</span>

**`DBASE_TYPE_DBASE`** (<span class="type">int</span>)  
<span class="simpara"> Create dBASE style database. Used with <span
class="function">dbase\_create</span>. (Available as of dbase 7.0.0)
</span>

**`DBASE_TYPE_FOXPRO`** (<span class="type">int</span>)  
<span class="simpara"> Create FoxPro style database. Used with <span
class="function">dbase\_create</span>. (Available as of dbase 7.0.0)
</span>

范例
----

Many examples in this reference require a dBase database. We will use
`/tmp/test.dbf` that will be created in the example of <span
class="function">dbase\_create</span>.

dbase\_add\_record
==================

Adds a record to a database

### 说明

<span class="type">bool</span> <span
class="methodname">dbase\_add\_record</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> , <span class="methodparam"><span
class="type">array</span> `$data`</span> )

Adds the given data to the database.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

`data`  
An indexed array of data. The number of items must be equal to the
number of fields in the database, otherwise <span
class="function">dbase\_add\_record</span> will fail.

> **Note**:
>
> If you're using <span class="function">dbase\_get\_record</span>
> return value for this parameter, remember to reset the key named
> *deleted*.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Inserting a record in a dBase database**

``` php
<?php

// open in read-write mode
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  dbase_add_record($db, array(
      date('Ymd'), 
      'Maxim Topolov', 
      '23', 
      'max@example.com',
      'T'));   
  dbase_close($db);
}

?>
```

### 参见

-   <span class="function">dbase\_delete\_record</span>
-   <span class="function">dbase\_replace\_record</span>

dbase\_close
============

Closes a database

### 说明

<span class="type">bool</span> <span
class="methodname">dbase\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$database`</span> )

Closes the given database resource.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Closing a dBase database file**

``` php
<?php

// open in read-only mode
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  // read some data ..
  
  dbase_close($db);
}

?>
```

### 参见

-   <span class="function">dbase\_open</span>
-   <span class="function">dbase\_create</span>

dbase\_create
=============

Creates a database

### 说明

<span class="type">resource</span> <span
class="methodname">dbase\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">array</span>
`$fields`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`<span class="initializer"> =
DBASE\_TYPE\_DBASE</span></span> \] )

<span class="function">dbase\_create</span> creates a dBase database
with the given definition. If the file already exists, it is not
truncated. <span class="function">dbase\_pack</span> can be called to
force truncation.

> **Note**: <span class="simpara">当启用
> <a href="/features/safe-mode.html" class="link">安全模式</a>时， PHP
> 会检查被操作的文件或目录是否与被执行的脚本有相同的
> UID（所有者）。</span>

> **Note**:
>
> 此函数受
> <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
> 影响。

### 参数

`path`  
The path of the database. It can be a relative or absolute path to the
file where dBase will store your data.

`fields`  
An array of arrays, each array describing the format of one field of the
database. Each field consists of a name, a character indicating the
field type, and optionally, a length, a precision and a nullable flag.
The supported field types are listed in the
<a href="/book/dbase.html#简介" class="link">introduction section</a>.

> **Note**:
>
> The fieldnames are limited in length and must not exceed 10 chars.

`type`  
The type of database to be created. Either **`DBASE_TYPE_DBASE`** or
**`DBASE_TYPE_FOXPRO`**.

### 返回值

Returns a database resource if the database is successfully created, or
**`FALSE`** if an error occurred.

### 更新日志

| 版本        | 说明                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | The `type` parameter has been added.                                                                      |
| dbase 7.0.0 | The return value is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Creating a dBase database file**

``` php
<?php

// database "definition"
$def = array(
  array("date",     "D"),
  array("name",     "C",  50),
  array("age",      "N",   3, 0),
  array("email",    "C", 128),
  array("ismember", "L")
);

// creation
if (!dbase_create('/tmp/test.dbf', $def)) {
  echo "Error, can't create the database\n";
}

?>
```

### 参见

-   <span class="function">dbase\_open</span>
-   <span class="function">dbase\_close</span>

dbase\_delete\_record
=====================

Deletes a record from a database

### 说明

<span class="type">bool</span> <span
class="methodname">dbase\_delete\_record</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> , <span class="methodparam"><span
class="type">int</span> `$number`</span> )

Marks the given record to be deleted from the database.

> **Note**:
>
> To actually remove the record from the database, you must also call
> <span class="function">dbase\_pack</span>.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

`number`  
An integer which spans from 1 to the number of records in the database
(as returned by <span class="function">dbase\_numrecords</span>).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 参见

-   <span class="function">dbase\_add\_record</span>
-   <span class="function">dbase\_replace\_record</span>

dbase\_get\_header\_info
========================

Gets the header info of a database

### 说明

<span class="type">array</span> <span
class="methodname">dbase\_get\_header\_info</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> )

Returns information on the column structure of the given database
resource.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

### 返回值

An indexed array with an entry for each column in the database. The
array index starts at 0.

Each array element contains an associative array of column information,
as described here:

name  
<span class="simpara"> The name of the column </span>

type  
<span class="simpara"> The human-readable name for the dbase type of the
column (i.e. date, boolean, etc.) The supported field types are listed
in the
<a href="/book/dbase.html#简介" class="link">introduction section</a>.
</span>

length  
<span class="simpara"> The number of bytes this column can hold </span>

precision  
<span class="simpara"> The number of digits of decimal precision for the
column </span>

format  
<span class="simpara"> A suggested <span class="function">printf</span>
format specifier for the column </span>

offset  
<span class="simpara"> The byte offset of the column from the start of
the row </span>

If the database header information cannot be read, **`FALSE`** is
returned.

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Showing header information for a dBase database file**

``` php
<?php
// Path to dbase file
$db_path = "/tmp/test.dbf";

// Open dbase file
$dbh = dbase_open($db_path, 0)
  or die("Error! Could not open dbase database file '$db_path'.");

// Get column information
$column_info = dbase_get_header_info($dbh);

// Display information
print_r($column_info);
?>
```

dbase\_get\_record\_with\_names
===============================

Gets a record from a database as an associative array

### 说明

<span class="type">array</span> <span
class="methodname">dbase\_get\_record\_with\_names</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> , <span class="methodparam"><span
class="type">int</span> `$number`</span> )

Gets a record from a dBase database as an associative array.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

`_number`  
The index of the record between *1* and
*dbase\_numrecords($dbase\_identifier)*.

### 返回值

An associative array with the record. This will also include a key named
*deleted* which is set to 1 if the record has been marked for deletion
(see <span class="function">dbase\_delete\_record</span>). Therefore it
is not possible to retrieve the value of a field named *deleted* with
this function.

每个字段都会被转换为对应的 PHP 类型，除了以下场景：

-   <span class="simpara"> 日期会被转换成字符串。 </span>
-   <span class="simpara"> DateTime 会被转换成字符串。 </span>
-   <span class="simpara"> 范围之外的整数
    **`PHP_INT_MIN`**..**`PHP_INT_MAX`** 将返回字符串。 </span>
-   <span class="simpara"> dbase 7.0.0 之前的版本， 布尔型 (*L*)
    将被转换为 *1* 或 *0*。 </span>

On error, <span class="function">dbase\_get\_record\_with\_names</span>
will return **`FALSE`**.

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Listing all the registered members in the database**

``` php
<?php
// open in read-only mode
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      $row = dbase_get_record_with_names($db, $i);
      if ($row['ismember'] == 1) {
          echo "Member #$i: " . trim($row['name']) . "\n";
      }
  }
}
?>
```

### 参见

-   <span class="function">dbase\_get\_record</span>

dbase\_get\_record
==================

Gets a record from a database as an indexed array

### 说明

<span class="type">array</span> <span
class="methodname">dbase\_get\_record</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> , <span class="methodparam"><span
class="type">int</span> `$number`</span> )

Gets a record from a database as an indexed array.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

`number`  
The index of the record between *1* and
*dbase\_numrecords($dbase\_identifier)*.

### 返回值

An indexed array with the record. This array will also include an
associative key named *deleted* which is set to 1 if the record has been
marked for deletion (see <span
class="function">dbase\_delete\_record</span>).

每个字段都会被转换为对应的 PHP 类型，除了以下场景：

-   <span class="simpara"> 日期会被转换成字符串。 </span>
-   <span class="simpara"> DateTime 会被转换成字符串。 </span>
-   <span class="simpara"> 范围之外的整数
    **`PHP_INT_MIN`**..**`PHP_INT_MAX`** 将返回字符串。 </span>
-   <span class="simpara"> dbase 7.0.0 之前的版本， 布尔型 (*L*)
    将被转换为 *1* 或 *0*。 </span>

On error, <span class="function">dbase\_get\_record</span> will return
**`FALSE`**.

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 参见

-   <span class="function">dbase\_get\_record\_with\_names</span>

dbase\_numfields
================

Gets the number of fields of a database

### 说明

<span class="type">int</span> <span
class="methodname">dbase\_numfields</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> )

Gets the number of fields (columns) in the specified database.

> **Note**:
>
> Field numbers are between 0 and *dbase\_numfields($db)-1*, while
> record numbers are between 1 and *dbase\_numrecords($db)*.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

### 返回值

The number of fields in the database, or **`FALSE`** if an error occurs.

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 <span class="function">dbase\_numfields</span> Example**

``` php
<?php

$rec = dbase_get_record($db, $recno);
$nf  = dbase_numfields($db);
for ($i = 0; $i < $nf; $i++) {
  echo $rec[$i], "\n";
}

?>
```

### 参见

-   <span class="function">dbase\_numrecords</span>

dbase\_numrecords
=================

Gets the number of records in a database

### 说明

<span class="type">int</span> <span
class="methodname">dbase\_numrecords</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> )

Gets the number of records (rows) in the specified database.

> **Note**:
>
> Records which are marked as deleted are counted as well.

> **Note**:
>
> Record numbers are between 1 and *dbase\_numrecords($db)*, while field
> numbers are between 0 and *dbase\_numfields($db)-1*.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

### 返回值

The number of records in the database, or **`FALSE`** if an error
occurs.

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Looping over all the records of the database**

``` php
<?php

// open in read-only mode
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      $record = dbase_get_record($db, $i);
      if (!$record['deleted']) {
          // do something with the $record
      } else {
          // do something with the deleted $record or ignore it
      }
  }
}

?>
```

### 参见

-   <span class="function">dbase\_numfields</span>

dbase\_open
===========

Opens a database

### 说明

<span class="type">resource</span> <span
class="methodname">dbase\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="function">dbase\_open</span> opens a dBase database with
the given access mode.

> **Note**: <span class="simpara">当启用
> <a href="/features/safe-mode.html" class="link">安全模式</a>时， PHP
> 会检查被操作的文件或目录是否与被执行的脚本有相同的
> UID（所有者）。</span>

> **Note**:
>
> 此函数受
> <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
> 影响。

### 参数

`path`  
The path of the database. It can be a relative or absolute path to the
file where dBase will store your data.

`mode`  
An integer which correspond to those for the **open()** system call
(Typically 0 means read-only, 1 means write-only, and 2 means read and
write).

> **Note**:
>
> You can't open a dBase file in write-only mode as the function will
> fail to read the headers information and thus you can't use 1 as
> `mode`.

As of dbase 7.0.0 you can use **`DBASE_RDONLY`** and **`DBASE_RDWR`**,
respectively, to specify the `mode`.

### 返回值

Returns a database resource on success, 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本        | 说明                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | The return value is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Opening a dBase database file**

``` php
<?php

// open in read-only mode
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  // read some data ..
  
  dbase_close($db);
}

?>
```

### 参见

-   <span class="function">dbase\_create</span>
-   <span class="function">dbase\_close</span>

dbase\_pack
===========

Packs a database

### 说明

<span class="type">bool</span> <span
class="methodname">dbase\_pack</span> ( <span class="methodparam"><span
class="type">resource</span> `$database`</span> )

Packs the specified database by permanently deleting all records marked
for deletion using <span class="function">dbase\_delete\_record</span>.
Note that the file will be truncated after successful packing (contrary
to dBASE III's PACK command).

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Emptying a dBase database**

``` php
<?php

// open in read-write mode
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      dbase_delete_record($db, $i);
  }
  // expunge the database
  dbase_pack($db);
}

?>
```

### 参见

-   <span class="function">dbase\_delete\_record</span>

dbase\_replace\_record
======================

Replaces a record in a database

### 说明

<span class="type">bool</span> <span
class="methodname">dbase\_replace\_record</span> ( <span
class="methodparam"><span class="type">resource</span>
`$database`</span> , <span class="methodparam"><span
class="type">array</span> `$data`</span> , <span
class="methodparam"><span class="type">int</span> `$number`</span> )

Replaces the given record in the database with the given data.

### 参数

`database`  
The database resource, returned by <span
class="function">dbase\_open</span> or <span
class="function">dbase\_create</span>.

`data`  
An indexed array of data. The number of items must be equal to the
number of fields in the database, otherwise <span
class="function">dbase\_replace\_record</span> will fail.

> **Note**:
>
> If you're using <span class="function">dbase\_get\_record</span>
> return value for this parameter, remember to reset the key named
> *deleted*.

`number`  
An integer which spans from 1 to the number of records in the database
(as returned by <span class="function">dbase\_numrecords</span>).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本        | 说明                                                                                                |
|-------------|-----------------------------------------------------------------------------------------------------|
| dbase 7.0.0 | `database` is now a <span class="type">resource</span> instead of an <span class="type">int</span>. |

### 范例

**示例 \#1 Updating a record in the database**

``` php
<?php

// open in read-write mode
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  // gets the old row
  $row = dbase_get_record_with_names($db, 1);
  
  // remove the 'deleted' entry
  unset($row['deleted']);
  
  // Update the date field with the current timestamp
  $row['date'] = date('Ymd');
  
  // convert the row to an indexed array
  $row = array_values($row);

  // Replace the record
  dbase_replace_record($db, $row, 1);
  dbase_close($db);
}

?>
```

### 注释

> **Note**:
>
> Boolean fields result in an <span class="type">integer</span> element
> value (*0* or *1*) when retrieved via <span
> class="function">dbase\_get\_record</span> or <span
> class="function">dbase\_get\_record\_with\_names</span>. If they are
> written back, this results in the value becoming *0*, so care has to
> be taken to properly adjust the values.

### 参见

-   <span class="function">dbase\_add\_record</span>
-   <span class="function">dbase\_delete\_record</span>

**目录**

-   [dbase\_add\_record](/book/dbase.html#dbase_add_record) — Adds a
    record to a database
-   [dbase\_close](/book/dbase.html#dbase_close) — Closes a database
-   [dbase\_create](/book/dbase.html#dbase_create) — Creates a database
-   [dbase\_delete\_record](/book/dbase.html#dbase_delete_record) —
    Deletes a record from a database
-   [dbase\_get\_header\_info](/book/dbase.html#dbase_get_header_info) —
    Gets the header info of a database
-   [dbase\_get\_record\_with\_names](/book/dbase.html#dbase_get_record_with_names)
    — Gets a record from a database as an associative array
-   [dbase\_get\_record](/book/dbase.html#dbase_get_record) — Gets a
    record from a database as an indexed array
-   [dbase\_numfields](/book/dbase.html#dbase_numfields) — Gets the
    number of fields of a database
-   [dbase\_numrecords](/book/dbase.html#dbase_numrecords) — Gets the
    number of records in a database
-   [dbase\_open](/book/dbase.html#dbase_open) — Opens a database
-   [dbase\_pack](/book/dbase.html#dbase_pack) — Packs a database
-   [dbase\_replace\_record](/book/dbase.html#dbase_replace_record) —
    Replaces a record in a database
