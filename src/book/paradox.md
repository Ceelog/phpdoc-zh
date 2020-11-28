Paradox File Access
===================

**目录**

-   [简介](/book/paradox.html#简介)
-   [安装／配置](/book/paradox.html#安装／配置)
    -   [需求](/book/paradox.html#需求)
    -   [安装](/book/paradox.html#安装)
    -   [运行时配置](/book/paradox.html#运行时配置)
    -   [资源类型](/book/paradox.html#资源类型)
-   [预定义常量](/book/paradox.html#预定义常量)
-   [Paradox 函数](/book/paradox.html#Paradox%20函数)
    -   [px\_close](/book/paradox.html#px_close) — Closes a paradox
        database
    -   [px\_create\_fp](/book/paradox.html#px_create_fp) — Create a new
        paradox database
    -   [px\_date2string](/book/paradox.html#px_date2string) — Converts
        a date into a string
    -   [px\_delete\_record](/book/paradox.html#px_delete_record) —
        Deletes record from paradox database
    -   [px\_delete](/book/paradox.html#px_delete) — Deletes resource of
        paradox database
    -   [px\_get\_field](/book/paradox.html#px_get_field) — Returns the
        specification of a single field
    -   [px\_get\_info](/book/paradox.html#px_get_info) — Return lots of
        information about a paradox file
    -   [px\_get\_parameter](/book/paradox.html#px_get_parameter) — Gets
        a parameter
    -   [px\_get\_record](/book/paradox.html#px_get_record) — Returns
        record of paradox database
    -   [px\_get\_schema](/book/paradox.html#px_get_schema) — Returns
        the database schema
    -   [px\_get\_value](/book/paradox.html#px_get_value) — Gets a value
    -   [px\_insert\_record](/book/paradox.html#px_insert_record) —
        Inserts record into paradox database
    -   [px\_new](/book/paradox.html#px_new) — Create a new paradox
        object
    -   [px\_numfields](/book/paradox.html#px_numfields) — Returns
        number of fields in a database
    -   [px\_numrecords](/book/paradox.html#px_numrecords) — Returns
        number of records in a database
    -   [px\_open\_fp](/book/paradox.html#px_open_fp) — Open paradox
        database
    -   [px\_put\_record](/book/paradox.html#px_put_record) — Stores
        record into paradox database
    -   [px\_retrieve\_record](/book/paradox.html#px_retrieve_record) —
        Returns record of paradox database
    -   [px\_set\_blob\_file](/book/paradox.html#px_set_blob_file) —
        Sets the file where blobs are read from
    -   [px\_set\_parameter](/book/paradox.html#px_set_parameter) — Sets
        a parameter
    -   [px\_set\_tablename](/book/paradox.html#px_set_tablename) — Sets
        the name of a table (deprecated)
    -   [px\_set\_targetencoding](/book/paradox.html#px_set_targetencoding)
        — Sets the encoding for character fields (deprecated)
    -   [px\_set\_value](/book/paradox.html#px_set_value) — Sets a value
    -   [px\_timestamp2string](/book/paradox.html#px_timestamp2string) —
        Converts the timestamp into a string
    -   [px\_update\_record](/book/paradox.html#px_update_record) —
        Updates record in paradox database

This module allows to read and write Paradox databases, primary index
files and blob files. Write support has been proven to be quite
reliable, though due to lack of documentation the produced files may not
in any case be readable by other applications. Encrypted databases can
be read without specifying a password if pxlib \>= 0.5.0 is used.

> **Note**:
>
> This module is also in development and may change, though major
> changes to the API are not expected.

**Warning**

此扩展是*实验性* 的。
此扩展的表象，包括其函数名称以及其他此扩展的相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本扩展风险自担。

安装／配置
==========

**目录**

-   [需求](/book/paradox.html#需求)
-   [安装](/book/paradox.html#安装)
-   [运行时配置](/book/paradox.html#运行时配置)
-   [资源类型](/book/paradox.html#资源类型)

需求
----

You need at least PHP 5.0.0 and pxlib \>= 0.4.4 for the basic set of
functions. Some newer functions are only available with pxlib \>= 0.6.0.
Reading and writing of encrypted databases requires at least pxlib \>=
0.5.0. The paradox library (pxlib) is available at
<a href="http://pxlib.sourceforge.net" class="link external">» http://pxlib.sourceforge.net</a>.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/paradox" class="link external">» https://pecl.php.net/package/paradox</a>

Make sure you have pxlib installed before. If you install pxlib from an
rpm or debian package, do not forget to install the development package
as well.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

<span class="function">px\_new</span> creates a new Paradox object
required by all Paradox functions.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

The following two tables lists all constants defined by the paradox
extension.

| Name                   | Meaning                                                     |
|------------------------|-------------------------------------------------------------|
| PX\_FIELD\_ALPHA       | Character data with fixed length                            |
| PX\_FIELD\_DATE        | Date, number of days since 1.1.0000                         |
| PX\_FIELD\_SHORT       | Short integer (2 Bytes)                                     |
| PX\_FIELD\_LONG        | Long integer (4 Bytes)                                      |
| PX\_FIELD\_CURRENCY    | same as PX\_FIELD\_NUMBER                                   |
| PX\_FIELD\_NUMBER      | Double                                                      |
| PX\_FIELD\_LOGICAL     | Boolean                                                     |
| PX\_FIELD\_MEMOBLOB    | Binary large object                                         |
| PX\_FIELD\_BLOB        | Binary large object (not supported)                         |
| PX\_FIELD\_FMTMEMOBLOB | Binary large object                                         |
| PX\_FIELD\_OLE         | OLE object (basically a blob, not supported)                |
| PX\_FIELD\_GRAPHIC     | Graphic (basically a blob, not supported)                   |
| PX\_FIELD\_TIME        | time, number of milli seconds since midnight                |
| PX\_FIELD\_TIMESTAMP   | timestamp, number of milli seconds since 1.1.0000           |
| PX\_FIELD\_AUTOINC     | Auto incrementing interger (like PX\_FIELD\_LONG)           |
| PX\_FIELD\_BCD         | Decimal number stored in bcd format (not supported)         |
| PX\_FIELD\_BYTES       | Array of Bytes with not more than 255 bytes (not supported) |
| PX\_KEYTOLOWER         | Turn all field names into lower case                        |
| PX\_KEYTOUPPER         | Turn all field names into upper case                        |

| Name                              | Meaning                          |
|-----------------------------------|----------------------------------|
| PX\_FILE\_INDEX\_DB               | Indexed database                 |
| PX\_FILE\_PRIM\_INDEX             | Primary index                    |
| PX\_FILE\_NON\_INDEX\_DB          | None indexed database            |
| PX\_FILE\_NON\_INC\_SEC\_INDEX    | None incremental secondary index |
| PX\_FILE\_SEC\_INDEX              | Secondary index                  |
| PX\_FILE\_INC\_SEC\_INDEX         | Incremental secondary index      |
| PX\_FILE\_NON\_INC\_SEC\_INDEX\_G | Non incremental secondary index  |
| PX\_FILE\_SEC\_INDEX\_G           | Secondary index                  |
| PX\_FILE\_INC\_SEC\_INDEX\_G      | Non incremental secondary index  |

Object oriented API
-------------------

The paradox extension provides also an object oriented API. It consists
of only one class called paradox\_db. Its methods only differ from the
functions in its name and of course the missing first parameter. The
following table will list all methods and its equivalent functions.

| Name of method                                    | Equivalent function                                   |
|---------------------------------------------------|-------------------------------------------------------|
| Constructor                                       | <span class="function">px\_new</span>                 |
| Destructor                                        | <span class="function">px\_delete</span>              |
| <span class="function">open\_fp</span>            | <span class="function">px\_open\_fp</span>            |
| <span class="function">create\_fp</span>          | <span class="function">px\_create\_fp</span>          |
| <span class="function">close</span>               | <span class="function">px\_close</span>               |
| <span class="function">numrecords</span>          | <span class="function">px\_numrecords</span>          |
| <span class="function">numfields</span>           | <span class="function">px\_numfields</span>           |
| <span class="function">get\_record</span>         | <span class="function">px\_get\_record</span>         |
| <span class="function">put\_record</span>         | <span class="function">px\_put\_record</span>         |
| <span class="function">retrieve\_record</span>    | <span class="function">px\_retrieve\_record</span>    |
| <span class="function">delete\_record</span>      | <span class="function">px\_delete\_record</span>      |
| <span class="function">insert\_record</span>      | <span class="function">px\_insert\_record</span>      |
| <span class="function">update\_record</span>      | <span class="function">px\_update\_record</span>      |
| <span class="function">get\_field</span>          | <span class="function">px\_get\_field</span>          |
| <span class="function">get\_schema</span>         | <span class="function">px\_get\_schema</span>         |
| <span class="function">get\_info</span>           | <span class="function">px\_get\_info</span>           |
| <span class="function">set\_parameter</span>      | <span class="function">px\_set\_parameter</span>      |
| <span class="function">get\_parameter</span>      | <span class="function">px\_get\_parameter</span>      |
| <span class="function">set\_value</span>          | <span class="function">px\_set\_value</span>          |
| <span class="function">get\_value</span>          | <span class="function">px\_get\_value</span>          |
| <span class="function">get\_info</span>           | <span class="function">px\_get\_info</span>           |
| <span class="function">set\_targetencoding</span> | <span class="function">px\_set\_targetencoding</span> |
| <span class="function">set\_tablename</span>      | <span class="function">px\_set\_tablename</span>      |
| <span class="function">set\_blob\_file</span>     | <span class="function">px\_set\_blob\_file</span>     |
| <span class="function">date2string</span>         | <span class="function">px\_date2string</span>         |
| <span class="function">timestamp2string</span>    | <span class="function">px\_timestamp2string</span>    |

px\_close
=========

Closes a paradox database

### 说明

<span class="type">bool</span> <span class="methodname">px\_close</span>
( <span class="methodparam"><span class="type">resource</span>
`$pxdoc`</span> )

Closes the paradox database. This function will not close the file. You
will have to call <span class="function">fclose</span> afterwards.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">px\_open\_fp</span>
-   The example at <span class="function">px\_new</span>

px\_create\_fp
==============

Create a new paradox database

### 说明

<span class="type">bool</span> <span
class="methodname">px\_create\_fp</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$file`</span> , <span class="methodparam"><span
class="type">array</span> `$fielddesc`</span> )

Create a new paradox database file. The actual file has to be opened
before with <span class="function">fopen</span>. Make sure the file is
writable.

> **Note**:
>
> Calling this functions issues a warning about an empty tablename which
> can be safely ignored. Just set the tablename afterwards with <span
> class="function">px\_set\_parameter</span>.

> **Note**:
>
> This function is highly experimental, due to insufficient
> documentation of the paradox file format. Database files created with
> this function can be opened by <span
> class="function">px\_open\_fp</span> and has been successfully opened
> by the Paradox software, but your milage may vary.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`file`  
File handle as returned by <span class="function">fopen</span>.

`fielddesc`  
**fielddesc** is an array containing one element for each field
specification. A field specification is an array itself with either two
or three elements.The first element is always a string value used as the
name of the field. It may not be larger than ten characters. The second
element contains the field type which is one of the constants listed in
the table
<a href="/book/paradox.html#Contants%20for%20field%20types" class="link">Constants for field types</a>.
In the case of a character field or bcd field, you will have to provide
a third element specifying the length respectively the precesion of the
field. If your field specification contains blob fields, you will have
to make sure to either make the field large enough for all field values
to fit or specify a blob file with <span
class="function">px\_set\_blob\_file</span> for storing the blobs. If
this is not done the field data is truncated.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Creating a Paradox database with two fields**

``` php
<?php
if(!$pxdoc = px_new()) {
  /* Error handling */
}
$fp = fopen("test.db", "w+");
$fields = array(array("col1", "S"), array("col2", "I"));
if(!px_create_fp($pxdoc, $fp, $fields)) {
  /* Error handling */
}
px_set_parameter($pxdoc, "tablename", "testtable");
for($i=-50; $i<50; $i++) {
  $rec = array($i, -$i);
  px_put_record($pxdoc, $rec);
}   
px_close($pxdoc);
px_delete($pxdoc);
fclose($fp);
?>
```

### 参见

-   <span class="function">px\_new</span>
-   <span class="function">px\_put\_record</span>
-   <span class="function">fopen</span>

px\_date2string
===============

Converts a date into a string

### 说明

<span class="type">string</span> <span
class="methodname">px\_date2string</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
, <span class="methodparam"><span class="type">string</span>
`$format`</span> )

Turns a date as it stored in the paradox file into human readable
format. Paradox dates are the number of days since 1.1.0000. This
function is just for convenience. It can be easily replaced by some math
and the calendar functions as demonstrated in the example below.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`value`  
Value as stored in paradox database field of type PX\_FIELD\_DATE.

`format`  
String format similar to the format used by <span
class="function">date</span>. The placeholders support by this function
is a subset of those supported by <span class="function">date</span> (Y,
y, m, n, d, j, L).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Turn a paradox date into a human readable form**

``` php
<?php
$px = px_new();

/* make up a date as it could be stored in */
/* a date field of a paradox db. */
/* 700000 days since 1.1.0000. */
$days = 700000;

/* Use the calendar functions to print a */
/* human readable format of the date */
echo jdtogregorian($days+1721425)."\n";
/* px_date2string() outputs the same */
echo px_date2string($px, $days, "n/d/Y")."\n";

px_delete($px);
?>
```

以上例程会输出：

    7/15/1917
    7/15/1917

### 参见

-   <span class="function">px\_timestamp2string</span>
-   <span class="function">jdtogregorian</span>

px\_delete\_record
==================

Deletes record from paradox database

### 说明

<span class="type">bool</span> <span
class="methodname">px\_delete\_record</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$num`</span> )

This function deletes a record from the database. It does not free the
space in the database file but just marks it as deleted. Inserting a new
record afterwards will reuse the space.

> **Note**:
>
> This function is only available if pxlib \>= 0.6.0 is used.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`num`  
The record number is an artificial number counting records in the order
as they are stored in the database. The first record has number 0.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

px\_delete
==========

Deletes resource of paradox database

### 说明

<span class="type">bool</span> <span
class="methodname">px\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$pxdoc`</span> )

Deletes the resource of the paradox file and frees all memory.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

px\_get\_field
==============

Returns the specification of a single field

### 说明

<span class="type">array</span> <span
class="methodname">px\_get\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">int</span>
`$fieldno`</span> )

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`fieldno`  
Number of the field. The first field has number 0. Specifying a field
number less than 0 and greater or equal the number of fields will
trigger an error.

### 返回值

Returns the specification of the **fieldno**'th database field as an
associated array. The array contains three fields named *name*, *type*,
and *size*.

px\_get\_info
=============

Return lots of information about a paradox file

### 说明

<span class="type">array</span> <span
class="methodname">px\_get\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> )

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

### 返回值

Returns an associated array with lots of information about a paradox
file. This array is likely to be extended in the future.

fileversion  
Version of file multiplied by 10, e.g. 70.

tablename  
Name of table as stored in the file. If the database was created by
pxlib, then this will be the name of the file without the extension.

numrecords  
Number of records in this table.

numfields  
Number of fields in this table.

headersize  
Number of bytes used for the header. This is usually 0x800.

recordsize  
Number of bytes used for each record. This is the sum of all field sizes
(available since version 1.4.2).

maxtablesize  
This value multiplied by 0x400 is the size of a data block in bytes. The
maximum number of records in a datablock is the integer part of
(maxtablesize \* 0x400 - 8) / recordsize.

numdatablocks  
The number of data blocks in the file. Each data block contains a
certain number of records which depends on the record size and the data
block size (maxtablesize). Data blocks may not necessarily be completely
filled.

numindexfields  
Number of fields used for the primary index. The fields do always start
with field number 1.

codepage  
The DOS codepage which was used for encoding fields with character data.
If the target encoding is not set with <span
class="function">px\_set\_targetencoding</span> this will be the
encoding for character fields when records are being accessed with <span
class="function">px\_get\_record</span> or <span
class="function">px\_retrieve\_record</span>.

### 参见

-   <span class="function">px\_numfields</span>
-   <span class="function">px\_numrecords</span>

px\_get\_parameter
==================

Gets a parameter

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">px\_get\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Gets various parameters.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`name`  
The `name` can be one of the following:

tablename  
The name of the table as it will be stored in the database header.

targetencoding  
The encoding for the output. Data which is being read from character
fields with <span class="function">px\_get\_record</span> or <span
class="function">px\_retrieve\_record</span> is recoded into the
targetencoding. If it is not set, then the data will be delivered as
stored in the database file.

inputencoding  
The encoding of the input data which is to be stored into the database.
When storing data of character fields in the database, the data is
expected to be delivered in this encoding.

### 返回值

Returns the value of the parameter 或者在失败时返回 **`FALSE`**.

px\_get\_record
===============

Returns record of paradox database

### 说明

<span class="type">array</span> <span
class="methodname">px\_get\_record</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$num`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`num`  
The record number is an artificial number counting records in the order
as they are stored in the database. The first record has number 0.

`mode`  
The optional `mode` can be **`PX_KEYTOLOWER`** or **`PX_KEYTOUPPER`** in
order to convert the keys of the returned array into lower or upper
case. If `mode` is not passed or is 0, then the key will be exactly like
the field name. The element values will contain the field values. NULL
values will be retained and are different from 0.0, 0 or the empty
string. Fields of type **`PX_FIELD_TIME`** will be returned as an
integer counting the number of milliseconds starting at midnight. A
timestamp (**`PX_FIELD_TIMESTAMP`**) and date (**`PX_FIELD_DATE`**) are
floating point respectively int values counting milliseconds
respectively days starting at the beginning of julian calendar. Use the
functions <span class="function">px-timestamp2string</span> and <span
class="function">px-date2string</span> to convert them into a character
representation.

### 返回值

Returns the `num`'th record from the paradox database. The record is
returned as an associated array with its keys being the field names.

### 参见

-   <span class="function">px\_retrieve\_record</span>

px\_get\_schema
===============

Returns the database schema

### 说明

<span class="type">array</span> <span
class="methodname">px\_get\_schema</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

<span class="function">px\_get\_schema</span> returns the database
schema.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`mode`  
If the optional `mode` is **`PX_KEYTOLOWER`** or **`PX_KEYTOUPPER`** the
keys of the returned array will be converted to lower or upper case. If
`mode` is 0 or not passed at all, then the key name will be identical to
the field name.

### 返回值

Returns the schema of a database file as an associated array. The key
name is equal to the field name. Each array element is itself an
associated array containing the two fields *type* and *size*. *type* is
one of the constants in table
<a href="/book/paradox.html#Contants%20for%20field%20types" class="link">Constants for field types</a>.
*size* is the number of bytes this field consumes in the record. The
total of all field sizes is equal to the record size as it can be
retrieved with <span class="function">px-get-info</span>.

px\_get\_value
==============

Gets a value

### 说明

<span class="type"><span class="type">float</span><span
class="type">false</span></span> <span
class="methodname">px\_get\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Gets various values.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`name`  
`name` can be one of the following.

numprimkeys  
The number of primary keys. Paradox databases always use the first
*numprimkeys* fields for the primary index.

### 返回值

Returns the value of the parameter 或者在失败时返回 **`FALSE`**.

px\_insert\_record
==================

Inserts record into paradox database

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">px\_insert\_record</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">array</span> `$data`</span>
)

Inserts a new record into the database. The record is not necessarily
inserted at the end of the database, but may be inserted at any position
depending on where the first free slot is found.

The record data is passed as an array of field values. The elements in
the array must correspond to the fields in the database. If the array
has less elements than fields in the database, the remaining fields will
be set to null.

Most field values can be passed as its equivalent php type e.g. a long
value is used for fields of type PX\_FIELD\_LONG, PX\_FIELD\_SHORT and
PX\_FIELD\_AUTOINC, a double values is used for fields of type
PX\_FIELD\_CURRENCY and PX\_FIELD\_NUMBER. Field values for blob and
alpha fields are passed as strings.

Fields of type PX\_FIELD\_TIME and PX\_FIELD\_DATE both require a long
value. In the first case this is the number of milliseconds since
midnight. In the second case this is the number of days since 1.1.0000.
Below there are two examples to convert the current date or timestamp
into a value suitable for one of paradox's date/time fields.

> **Note**:
>
> This function is only available if pxlib \>= 0.6.0 is used.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`data`  
Associated or indexed array containing the field values as e.g. returned
by <span class="function">px\_retrieve\_record</span>.

### 返回值

Returns **`FALSE`** on failure or the record number in case of success.

### 范例

**示例 \#1 Set the date/time fields in a paradox database to the current
date/time**

``` php
<?php
$px = px_new();
$fp = fopen("test.db", "w+");
px_create_fp($px, $fp, array(array("timestamp", "@"), array("time", "T"), array("date", "D")));

$curdate = getdate();
$jd = gregoriantojd($curdate["mon"], $curdate["mday"], $curdate["year"]);
$days = $jd - 1721425; /* Number of days between 1.1.4714 b.c. and 1.1.0000 */
$secs = $curdate["hours"]*3600 + $curdate["minutes"]*60 + $curdate["seconds"];
px_insert_record($px, array($days*86400000.0 + $secs*1000.0, $secs*1000.0, $days));

$curtimestamp = microtime(true);
$days = (int) ($curtimestamp/86400);
$secs = $curtimestamp - ($days * 86400.0);
$days += 2440588; /* Number of days between 1.1.4714 b.c. and 1.1.1970 */
$days -= 1721425; /* Number of days between 1.1.4714 b.c. and 1.1.0000 */
px_insert_record($px, array($days*86400000.0 + $secs*1000.0, $secs*1000.0, $days));
for($i=0; $i<2; $i++) {
    $rec = px_retrieve_record($px, $i);
    echo px_timestamp2string($px, $rec["timestamp"], "n/d/Y H:i:s")."\n";
    echo px_date2string($px, $rec["date"], "n/d/Y")."\n";
}
px_close($px);
px_delete($px);
?>
```

以上例程会输出：

    2/21/2006 21:42:30
    2/21/2006
    2/21/2006 20:42:30
    2/21/2006

The Julian day count as passed to <span
class="function">jdtogregorian</span> has a different base of 1.1.4714
b.c. and must therefore be calculated by adding 1721425 to the day count
used in the paradox file. Turning the day count into a timestamp is
easily done by multiplying with 86400000.0 to obtain milli seconds.

### 参见

<span class="function">px\_update\_record</span>

px\_new
=======

Create a new paradox object

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span class="methodname">px\_new</span>
( <span class="methodparam">void</span> )

Create a new paradox object. You will have to call this function before
any further functions. <span class="function">px\_new</span> does not
create any file on the disk, it just creates an instance of a paradox
object. This function must not be called if the object oriented
interface is used. Use *new paradox\_db()* instead.

### 返回值

Returns **`FALSE`** on failure.

### 范例

**示例 \#1 Opening a Paradox database**

``` php
<?php
if(!$pxdoc = px_new()) {
  /* Error handling */
}
$fp = fopen("test.db", "r");
if(!px_open_fp($pxdoc, $fp)) {
  /* Error handling */
}
// ...
px_close($pxdoc);
px_delete($pxdoc);
fclose($fp);
?>
```

If you prefer the object oriented API, then the above example will look
like the following.

**示例 \#2 Opening a Paradox database**

``` php
<?php
$fp = fopen("test.db", "r");
$pxdoc = new paradox_db();
if(!$pxdoc->open_fp($fp)) {
  /* Error handling */
}
// ...
$pxdoc->close();
fclose($fp);
?>
```

### 参见

-   <span class="function">px\_delete</span>
-   <span class="function">px\_open\_fp</span>

px\_numfields
=============

Returns number of fields in a database

### 说明

<span class="type">int</span> <span
class="methodname">px\_numfields</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> )

Get the number of fields in a database file.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

### 返回值

Returns the number of fields in a database file. The return value of
this function is identical to the element *numfields* in the array
returned by <span class="function">px\_get\_info</span>.

px\_numrecords
==============

Returns number of records in a database

### 说明

<span class="type">int</span> <span
class="methodname">px\_numrecords</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> )

Get the number of records in a database file.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

### 返回值

Returns the number of records in a database file. The return value of
this function is identical to the element *numrecords* in the array
returned by <span class="function">px\_get\_info</span>.

px\_open\_fp
============

Open paradox database

### 说明

<span class="type">bool</span> <span
class="methodname">px\_open\_fp</span> ( <span class="methodparam"><span
class="type">resource</span> `$pxdoc`</span> , <span
class="methodparam"><span class="type">resource</span> `$file`</span> )

Open an existing paradox database file. The actual file has to be opened
before with <span class="function">fopen</span>. This function can also
be used to open primary index files and tread them like a paradox
database. This is supported for those who would like to investigate a
primary index. It cannot be used to accelerate access to a database
file.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`file`  
`file` is the return value from <span class="function">fopen</span> with
the actual database file as parameter. Make sure the database is
writable if you plan to update or insert records.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fopen</span>
-   The example at <span class="function">px\_new</span>

px\_put\_record
===============

Stores record into paradox database

### 说明

<span class="type">bool</span> <span
class="methodname">px\_put\_record</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">array</span>
`$record`</span> \[, <span class="methodparam"><span
class="type">int</span> `$recpos`<span class="initializer"> =
-1</span></span> \] )

Stores a record into a paradox database. The record is always added at
the end of the database, regardless of any free slots. Use <span
class="function">px\_insert\_record</span> to add a new record into the
first free slot found in the database.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`record`  
Associated or indexed array containing the field values as e.g. returned
by <span class="function">px\_retrieve\_record</span>.

`recpos`  
This optional parameter may be used to specify a record number greater
than the current number of records in the database. The function will
add as many empty records as needed. There is hardly any need for this
parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

px\_retrieve\_record
====================

Returns record of paradox database

### 说明

<span class="type">array</span> <span
class="methodname">px\_retrieve\_record</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$num`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

This function is very similar to <span
class="function">px\_get\_record</span> but uses internally a different
approach to retrieve the data. It relies on pxlib for reading each
single field value, which usually results in support for more field
types.

> **Note**:
>
> This function is only available if pxlib \>= 0.6.0 is used.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`num`  
The record number is an artificial number counting records in the order
as they are stored in the database. The first record has number 0.

`mode`  
The optional `mode` can be **`PX_KEYTOLOWER`** or **`PX_KEYTOUPPER`** in
order to convert the keys into lower or upper case. If `mode` is not
passed or is 0, then the key will be exactly like the field name. The
element values will contain the field values. NULL values will be
retained and are different from 0.0, 0 or the empty string. Fields of
type **`PX_FIELD_TIME`** will be returned as an integer counting the
number of milliseconds starting at midnight. A timestamp is a floating
point value also counting milliseconds starting at the beginning of
julian calendar.

### 返回值

Returns the `num`'th record from the paradox database. The record is
returned as an associated array with its keys being the field names.

### 参见

-   <span class="function">px\_get\_record</span>

px\_set\_blob\_file
===================

Sets the file where blobs are read from

### 说明

<span class="type">bool</span> <span
class="methodname">px\_set\_blob\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Sets the name of the file where blobs are going to be read from or
written into. Without calling this function, <span
class="function">px\_get\_record</span> or <span
class="function">px\_retrieve\_record</span> will only return data in
blob fields if the data is part of the record and not stored in the blob
file. Blob data is stored in the record if it is small enough to fit in
the size of the blob field.

Calling <span class="function">px\_put\_record</span>, <span
class="function">px\_insert\_record</span>, or <span
class="function">px\_update\_record</span> without calling <span
class="function">px\_set\_blob\_file</span> will result in truncated
blob fields unless the data fits into the database file.

Calling this function twice will close the first blob file and open the
new one.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`filename`  
The name of the file. Its extension should be *.MB*.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

px\_set\_parameter
==================

Sets a parameter

### 说明

<span class="type">bool</span> <span
class="methodname">px\_set\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Sets various parameters.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`name`  
Depending on the parameter you want to set, `name` can be one of the
following.

tablename  
The name of the table as it will be stored in the database header.

targetencoding  
The encoding for the output. Data which is being read from character
fields is recoded into the targetencoding.

inputencoding  
The encoding of the input data which is to be stored into the database.

`value`  
The value of parameter to set. For inputencoding and targetencoding this
must be the name of the encoding as understood by iconv or recode, e.g.
iso-8859-1, utf-8, cp850.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">px\_get\_info</span> to determine the DOS
    code page.

px\_set\_tablename
==================

Sets the name of a table (deprecated)

### 说明

<span class="type"><span class="type">null</span><span
class="type">false</span></span> <span
class="methodname">px\_set\_tablename</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Sets the table name of a paradox database, which was created with <span
class="function">px\_create\_fp</span>. This function is deprecated use
<span class="function">px\_set\_parameter</span> instead.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`tablename`  
The name of the table. If it is not set explicitly it will be set to the
name of the database file.

### 返回值

Returns **`NULL`** on success 或者在失败时返回 **`FALSE`**.

### 参见

<span class="function">px\_set\_parameter</span>

px\_set\_targetencoding
=======================

Sets the encoding for character fields (deprecated)

### 说明

<span class="type">bool</span> <span
class="methodname">px\_set\_targetencoding</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$encoding`</span> )

Set the encoding for data retrieved from a character field. All
character fields will be recoded to the encoding set by this function.
If the encoding is not set, the character data will be returned in the
DOS code page encoding as specified in the database file. The `encoding`
can be any string identifier known to iconv or recode. On Unix systems
run *iconv -l* for a list of available encodings.

This function is deprecated and should be replaced by calling <span
class="function">px\_set\_parameter</span>.

See also <span class="function">px\_get\_info</span> to determine the
DOS code page as stored in the database file.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`encoding`  
The encoding for the output. Data which is being read from character
fields is recoded into the targetencoding.

### 返回值

Returns **`FALSE`** if the encoding could not be set, e.g. the encoding
is unknown, or pxlib does not support recoding at all. In the second
case a warning will be issued.

### 参见

<span class="function">px\_set\_parameter</span>

px\_set\_value
==============

Sets a value

### 说明

<span class="type">bool</span> <span
class="methodname">px\_set\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">float</span> `$value`</span> )

Sets various values.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`name`  
`name` can be one of the following.

numprimkeys  
The number of primary keys. Paradox databases always use the first
**numprimkeys** fields for the primary index.

`value`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

<span class="function">px\_set\_parameter</span>

px\_timestamp2string
====================

Converts the timestamp into a string

### 说明

<span class="type">string</span> <span
class="methodname">px\_timestamp2string</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$value`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> )

Turns a timestamp as it stored in the paradox file into human readable
format. Paradox timestamps are the number of miliseconds since
0001-01-02. This function is just for convenience. It can be easily
replaced by some math and the calendar functions as demonstrated in the
following example.

### 参数

`pxdoc`  
Resource identifier of the paradox database.

`value`  
Value as stored in paradox database field of type PX\_FIELD\_TIME, or
PX\_FIELD\_TIMESTAMP.

`format`  
String format similar to the format used by <span
class="function">date</span>. The placeholders support by this function
is a subset of those supported by <span class="function">date</span> (Y,
y, m, n, d, j, H, h, G, g, i, s, A, a, L).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Turn a paradox timestamp into a human readable form**

``` php
<?php
$px = px_new();

/* make up a date as it could be stored in */
/* a date field of a paradox db. */
/* 700000 days since 1.1.0000. */
$days = 700000;

/* Use the calendar functions to print a */
/* human readable format of the date */
echo jdtogregorian($days+1721425)."\n";

/* Turn it into a timestamp as it stored in a paradox database */
/* Timestamps are stored in miliseconds since 0001-01-02 */
$stamp = $days * 86400.0 * 1000.0;
/* Add one hour */
$stamp += 3600000.0;
/* The following will output '7/15/1917 01:00:00'. */
echo px_timestamp2string($px, $stamp, "n/d/Y H:i:s")."\n";

px_delete($px);
?>
```

以上例程会输出：

    7/15/1917
    7/15/1917 01:00:00

The Julian day count as passed to <span
class="function">jdtogregorian</span> has a different base of 1.1.4714
b.c. and must therefore be calculated by adding 1721425 to the day count
used in the paradox file. Turning the day count into a timestamp is
easily done by multiplying with 86400000.0 to obtain miliseconds.

### 参见

-   <span class="function">px\_date2string</span>
-   <span class="function">jdtogregorian</span>

px\_update\_record
==================

Updates record in paradox database

### 说明

<span class="type">bool</span> <span
class="methodname">px\_update\_record</span> ( <span
class="methodparam"><span class="type">resource</span> `$pxdoc`</span> ,
<span class="methodparam"><span class="type">array</span> `$data`</span>
, <span class="methodparam"><span class="type">int</span> `$num`</span>
)

Updates an exiting record in the database. The record starts at 0.

The record data is passed as an array of field values. The elements in
the array must correspond to the fields in the database. If the array
has less elements than fields in the database, the remaining fields will
be set to null.

> **Note**:
>
> This function is only available if pxlib \>= 0.6.0 is used.

### 参数

`pxdoc`  
Resource identifier of the paradox database as returned by <span
class="function">px\_new</span>.

`data`  
Associated array containing the field values as returned by <span
class="function">px\_retrieve\_record</span>.

`num`  
The record number is an artificial number counting records in the order
as they are stored in the database. The first record has number 0.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

<span class="function">px\_insert\_record</span>

**目录**

-   [px\_close](/book/paradox.html#px_close) — Closes a paradox database
-   [px\_create\_fp](/book/paradox.html#px_create_fp) — Create a new
    paradox database
-   [px\_date2string](/book/paradox.html#px_date2string) — Converts a
    date into a string
-   [px\_delete\_record](/book/paradox.html#px_delete_record) — Deletes
    record from paradox database
-   [px\_delete](/book/paradox.html#px_delete) — Deletes resource of
    paradox database
-   [px\_get\_field](/book/paradox.html#px_get_field) — Returns the
    specification of a single field
-   [px\_get\_info](/book/paradox.html#px_get_info) — Return lots of
    information about a paradox file
-   [px\_get\_parameter](/book/paradox.html#px_get_parameter) — Gets a
    parameter
-   [px\_get\_record](/book/paradox.html#px_get_record) — Returns record
    of paradox database
-   [px\_get\_schema](/book/paradox.html#px_get_schema) — Returns the
    database schema
-   [px\_get\_value](/book/paradox.html#px_get_value) — Gets a value
-   [px\_insert\_record](/book/paradox.html#px_insert_record) — Inserts
    record into paradox database
-   [px\_new](/book/paradox.html#px_new) — Create a new paradox object
-   [px\_numfields](/book/paradox.html#px_numfields) — Returns number of
    fields in a database
-   [px\_numrecords](/book/paradox.html#px_numrecords) — Returns number
    of records in a database
-   [px\_open\_fp](/book/paradox.html#px_open_fp) — Open paradox
    database
-   [px\_put\_record](/book/paradox.html#px_put_record) — Stores record
    into paradox database
-   [px\_retrieve\_record](/book/paradox.html#px_retrieve_record) —
    Returns record of paradox database
-   [px\_set\_blob\_file](/book/paradox.html#px_set_blob_file) — Sets
    the file where blobs are read from
-   [px\_set\_parameter](/book/paradox.html#px_set_parameter) — Sets a
    parameter
-   [px\_set\_tablename](/book/paradox.html#px_set_tablename) — Sets the
    name of a table (deprecated)
-   [px\_set\_targetencoding](/book/paradox.html#px_set_targetencoding)
    — Sets the encoding for character fields (deprecated)
-   [px\_set\_value](/book/paradox.html#px_set_value) — Sets a value
-   [px\_timestamp2string](/book/paradox.html#px_timestamp2string) —
    Converts the timestamp into a string
-   [px\_update\_record](/book/paradox.html#px_update_record) — Updates
    record in paradox database
