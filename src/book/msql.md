mSQL
====

**目录**

-   [简介](/book/msql.html#简介)
-   [安装／配置](/book/msql.html#安装／配置)
    -   [需求](/book/msql.html#需求)
    -   [安装](/book/msql.html#安装)
    -   [运行时配置](/book/msql.html#运行时配置)
    -   [资源类型](/book/msql.html#资源类型)
-   [预定义常量](/book/msql.html#预定义常量)
-   [范例](/book/msql.html#范例)
    -   [Basic usage](/book/msql.html#Basic%20usage)
-   [mSQL 函数](/book/msql.html#mSQL%20函数)
    -   [msql\_affected\_rows](/book/msql.html#msql_affected_rows) —
        Returns number of affected rows
    -   [msql\_close](/book/msql.html#msql_close) — Close mSQL
        connection
    -   [msql\_connect](/book/msql.html#msql_connect) — Open mSQL
        connection
    -   [msql\_create\_db](/book/msql.html#msql_create_db) — Create mSQL
        database
    -   [msql\_createdb](/book/msql.html#msql_createdb) — 别名
        msql\_create\_db
    -   [msql\_data\_seek](/book/msql.html#msql_data_seek) — Move
        internal row pointer
    -   [msql\_db\_query](/book/msql.html#msql_db_query) — Send mSQL
        query
    -   [msql\_dbname](/book/msql.html#msql_dbname) — 别名 msql\_result
    -   [msql\_drop\_db](/book/msql.html#msql_drop_db) — Drop (delete)
        mSQL database
    -   [msql\_error](/book/msql.html#msql_error) — Returns error
        message of last msql call
    -   [msql\_fetch\_array](/book/msql.html#msql_fetch_array) — Fetch
        row as array
    -   [msql\_fetch\_field](/book/msql.html#msql_fetch_field) — Get
        field information
    -   [msql\_fetch\_object](/book/msql.html#msql_fetch_object) — Fetch
        row as object
    -   [msql\_fetch\_row](/book/msql.html#msql_fetch_row) — Get row as
        enumerated array
    -   [msql\_field\_flags](/book/msql.html#msql_field_flags) — Get
        field flags
    -   [msql\_field\_len](/book/msql.html#msql_field_len) — Get field
        length
    -   [msql\_field\_name](/book/msql.html#msql_field_name) — Get the
        name of the specified field in a result
    -   [msql\_field\_seek](/book/msql.html#msql_field_seek) — Set field
        offset
    -   [msql\_field\_table](/book/msql.html#msql_field_table) — Get
        table name for field
    -   [msql\_field\_type](/book/msql.html#msql_field_type) — Get field
        type
    -   [msql\_fieldflags](/book/msql.html#msql_fieldflags) — Alias of
        msql\_field\_flags
    -   [msql\_fieldlen](/book/msql.html#msql_fieldlen) — Alias of
        msql\_field\_len
    -   [msql\_fieldname](/book/msql.html#msql_fieldname) — Alias of
        msql\_field\_name
    -   [msql\_fieldtable](/book/msql.html#msql_fieldtable) — Alias of
        msql\_field\_table
    -   [msql\_fieldtype](/book/msql.html#msql_fieldtype) — Alias of
        msql\_field\_type
    -   [msql\_free\_result](/book/msql.html#msql_free_result) — Free
        result memory
    -   [msql\_list\_dbs](/book/msql.html#msql_list_dbs) — List mSQL
        databases on server
    -   [msql\_list\_fields](/book/msql.html#msql_list_fields) — List
        result fields
    -   [msql\_list\_tables](/book/msql.html#msql_list_tables) — List
        tables in an mSQL database
    -   [msql\_num\_fields](/book/msql.html#msql_num_fields) — Get
        number of fields in result
    -   [msql\_num\_rows](/book/msql.html#msql_num_rows) — Get number of
        rows in result
    -   [msql\_numfields](/book/msql.html#msql_numfields) — Alias of
        msql\_num\_fields
    -   [msql\_numrows](/book/msql.html#msql_numrows) — Alias of
        msql\_num\_rows
    -   [msql\_pconnect](/book/msql.html#msql_pconnect) — Open
        persistent mSQL connection
    -   [msql\_query](/book/msql.html#msql_query) — Send mSQL query
    -   [msql\_regcase](/book/msql.html#msql_regcase) — Alias of
        sql\_regcase
    -   [msql\_result](/book/msql.html#msql_result) — Get result data
    -   [msql\_select\_db](/book/msql.html#msql_select_db) — Select mSQL
        database
    -   [msql\_tablename](/book/msql.html#msql_tablename) — Alias of
        msql\_result
    -   [msql](/book/msql.html#msql) — Alias of msql\_db\_query

These functions allow you to access mSQL database servers. More
information about mSQL can be found at
<a href="http://www.hughes.com.au/" class="link external">» http://www.hughes.com.au/</a>.

> **Note**:
>
> This extension is no longer bundled with PHP as of PHP 5.3.

安装／配置
==========

**目录**

-   [需求](/book/msql.html#需求)
-   [安装](/book/msql.html#安装)
-   [运行时配置](/book/msql.html#运行时配置)
-   [资源类型](/book/msql.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

This extension is no longer bundled with PHP as of PHP 5.3. This
extension is considered unmaintained and dead.

In order to have these functions available, you must compile PHP with
msql support by using the **--with-msql\[=DIR\]** option. DIR is the
mSQL base install directory, defaults to `/usr/local/msql3`.

> **Note**: **Note to Win32 Users**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `msql.dll`

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                              | 默认 | 可修改范围    | 更新日志 |
|-------------------------------------------------------------------|------|---------------|----------|
| <a href="/book/msql.html#" class="link">msql.allow_persistent</a> | "1"  | PHP\_INI\_ALL |          |
| <a href="/book/msql.html#" class="link">msql.max_persistent</a>   | "-1" | PHP\_INI\_ALL |          |
| <a href="/book/msql.html#" class="link">msql.max_links</a>        | "-1" | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`msql.allow_persistent` <span class="type">boolean</span>  
Whether to allow persistent mSQL connections.

`msql.max_persistent` <span class="type">integer</span>  
The maximum number of persistent mSQL connections per process.

`msql.max_links` <span class="type">integer</span>  
The maximum number of mSQL connections per process, including persistent
connections.

资源类型
--------

There are two resource types used in the mSQL module. The first one is
the link identifier for a database connection, the second a resource
which holds the result of a query.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`MSQL_ASSOC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSQL_NUM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSQL_BOTH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

范例
====

**目录**

-   [Basic usage](/book/msql.html#Basic%20usage)

Basic usage
-----------

This simple example shows how to connect, execute a query, print
resulting rows and disconnect from a mSQL database.

**示例 \#1 mSQL usage example**

``` php
<?php
/* Connecting, selecting database */
$link = msql_connect('localhost', 'username', 'password')
    or die('Could not connect : ' . msql_error($link));

msql_select_db('database', $link)
    or die('Could not select database');

/* Issue SQL query */
$query = 'SELECT * FROM my_table';
$result = msql_query($query, $link) or die('Query failed : ' . msql_error());

/* Printing results in HTML */
echo "<table>\n";
while ($row = msql_fetch_array($result, MSQL_ASSOC)) {
    echo "\t<tr>\n";
    foreach ($row as $col_value) {
        echo "\t\t<td>$col_value</td>\n";
    }
    echo "\t</tr>\n";
}
echo "</table>\n";

/* Free result set */
msql_free_result($result);

/* Close connection */
msql_close($link);
?>
```

msql\_affected\_rows
====================

Returns number of affected rows

### 说明

<span class="type">int</span> <span
class="methodname">msql\_affected\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Returns number of affected rows by the last SELECT, UPDATE or DELETE
query associated with `result`.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

### 返回值

Returns the number of affected rows on success, or **`FALSE`** on error.

### 参见

-   <span class="function">msql\_query</span>

msql\_close
===========

Close mSQL connection

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">msql\_close</span> closes the non-persistent
connection to the mSQL server that's associated with the specified link
identifier.

Using <span class="function">msql\_close</span> isn't usually necessary,
as non-persistent open links are automatically closed at the end of the
script's execution. See also
<a href="/language/types/resource.html#language.types.resource.self-destruct" class="link">freeing resources</a>.

### 参数

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">msql\_connect</span>
-   <span class="function">msql\_pconnect</span>

msql\_connect
=============

Open mSQL connection

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
\] )

<span class="function">msql\_connect</span> establishes a connection to
a mSQL server.

If a second call is made to <span class="function">msql\_connect</span>
with the same arguments, no new link will be established, but instead,
the link identifier of the already opened link will be returned.

The link to the server will be closed as soon as the execution of the
script ends, unless it's closed earlier by explicitly calling <span
class="function">msql\_close</span>.

### 参数

`hostname`  
The hostname can also include a port number. e.g. *hostname,port*.

If not specified, the connection is established by the means of a Unix
domain socket, being then more efficient then a localhost TCP socket
connection.

> **Note**:
>
> While this function will accept a colon (*:*) as a host/port
> separator, a comma (*,*) is the preferred method.

### 返回值

Returns a positive mSQL link identifier on success, or **`FALSE`** on
error.

### 参见

-   <span class="function">msql\_pconnect</span>
-   <span class="function">msql\_close</span>

msql\_create\_db
================

Create mSQL database

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_create\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">msql\_create\_db</span> attempts to create a new
database on the mSQL server.

### 参数

`database_name`  
The name of the mSQL database.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">msql\_drop\_db</span>

msql\_createdb
==============

别名 <span class="function">msql\_create\_db</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_create\_db</span>.

msql\_data\_seek
================

Move internal row pointer

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$row_number`</span> )

<span class="function">msql\_data\_seek</span> moves the internal row
pointer of the mSQL result associated with the specified query
identifier to point to the specified row number. The next call to <span
class="function">msql\_fetch\_row</span> would return that row.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

`row_number`  
The seeked row number.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">msql\_fetch\_array</span>
-   <span class="function">msql\_fetch\_object</span>
-   <span class="function">msql\_fetch\_row</span>
-   <span class="function">msql\_result</span>

msql\_db\_query
===============

Send mSQL query

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_db\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$database`</span>
, <span class="methodparam"><span class="type">string</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">msql\_db\_query</span> selects a database and
executes a query on it.

### 参数

`database`  
The name of the mSQL database.

`query`  
The SQL query.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

Returns a positive mSQL query identifier to the query result, or
**`FALSE`** on error.

### 参见

-   <span class="function">msql\_query</span>

msql\_dbname
============

别名 <span class="function">msql\_result</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_result</span>.

msql\_drop\_db
==============

Drop (delete) mSQL database

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_drop\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">msql\_drop\_db</span> attempts to drop (remove) a
database from the mSQL server.

### 参数

`database_name`  
The name of the database.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">msql\_create\_db</span>

msql\_error
===========

Returns error message of last msql call

### 说明

<span class="type">string</span> <span
class="methodname">msql\_error</span> ( <span
class="methodparam">void</span> )

<span class="function">msql\_error</span> returns the last issued error
by the mSQL server. Note that only the last error message is accessible
with <span class="function">msql\_error</span>.

### 返回值

The last error message or an empty string if no error was issued.

msql\_fetch\_array
==================

Fetch row as array

### 说明

<span class="type">array</span> <span
class="methodname">msql\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`</span> \] )

<span class="function">msql\_fetch\_array</span> is an extended version
of <span class="function">msql\_fetch\_row</span>. In addition to
storing the data in the numeric indices of the result array, it also
stores the data in associative indices, using the field names as keys.

An important thing to note is that using <span
class="function">msql\_fetch\_array</span> is NOT significantly slower
than using <span class="function">msql\_fetch\_row</span>, while it
provides a significant added value.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

`result_type`  
A constant that can take the following values: **`MSQL_ASSOC`**,
**`MSQL_NUM`**, and **`MSQL_BOTH`** with **`MSQL_BOTH`** being the
default.

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

### 范例

**示例 \#1 <span class="function">msql\_fetch\_array</span> example**

``` php
<?php
$con = msql_connect();
if (!$con) {
    die('Server connection problem: ' . msql_error());
}

if (!msql_select_db('test', $con)) {
    die('Database connection problem: ' . msql_error());
}

$result = msql_query('SELECT id, name FROM people', $con);
if (!$result) {
    die('Query execution problem: ' . msql_error());
}

while ($row = msql_fetch_array($result, MSQL_ASSOC)) {
    echo $row['id'] . ': ' . $row['name'] . "\n";
}

msql_free_result($result);
?>
```

### 更新日志

| 版本  | 说明                                                                                                                                   |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| 5.0.4 | A bug was fixed when retrieving data from columns containing **`NULL`** values. Such columns were not placed into the resulting array. |

### 参见

-   <span class="function">msql\_fetch\_row</span>
-   <span class="function">msql\_fetch\_object</span>
-   <span class="function">msql\_data\_seek</span>
-   <span class="function">msql\_result</span>

msql\_fetch\_field
==================

Get field information

### 说明

<span class="type">object</span> <span
class="methodname">msql\_fetch\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`<span class="initializer"> = 0</span></span> \] )

<span class="function">msql\_fetch\_field</span> can be used in order to
obtain information about fields in a certain query result.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

`field_offset`  
The field offset. If not specified, the next field that wasn't yet
retrieved by <span class="function">msql\_fetch\_field</span> is
retrieved.

### 返回值

Returns an object containing field information. The properties of the
object are:

-   <span class="property">name</span> - column name

-   <span class="property">table</span> - name of the table the column
    belongs to

-   <span class="property">not\_null</span> - 1 if the column cannot be
    **`NULL`**

-   <span class="property">unique</span> - 1 if the column is a unique
    key

-   <span class="simpara"> type - the type of the column </span>

### 参见

-   <span class="function">msql\_field\_seek</span>

msql\_fetch\_object
===================

Fetch row as object

### 说明

<span class="type">object</span> <span
class="methodname">msql\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">msql\_fetch\_object</span> is similar to <span
class="function">msql\_fetch\_array</span>, with one difference - an
object is returned, instead of an array. Indirectly, that means that you
can only access the data by the field names, and not by their offsets
(numbers are illegal property names).

Speed-wise, the function is identical to <span
class="function">msql\_fetch\_array</span>, and almost as quick as <span
class="function">msql\_fetch\_row</span> (the difference is
insignificant).

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

### 返回值

Returns an object with properties that correspond to the fetched row, or
**`FALSE`** if there are no more rows.

### 范例

**示例 \#1 <span class="function">msql\_fetch\_object</span> example**

``` php
<?php
$con = msql_connect();
if (!$con) {
    die('Server connection problem: ' . msql_error());
}

if (!msql_select_db('test', $con)) {
    die('Database connection problem: ' . msql_error());
}

$result = msql_query('SELECT id, name FROM people', $con);
if (!$result) {
    die('Query execution problem: ' . msql_error());
}

while ($row = msql_fetch_object($result, MSQL_ASSOC)) {
    echo $row->id . ': ' . $row->name . "\n";
}

msql_free_result($result);
?>
```

### 更新日志

| 版本  | 说明                                                                                                                                   |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| 5.0.4 | A bug was fixed when retrieving data from columns containing **`NULL`** values. Such columns were not placed into the resulting array. |

### 参见

-   <span class="function">msql\_fetch\_array</span>
-   <span class="function">msql\_fetch\_row</span>
-   <span class="function">msql\_data\_seek</span>
-   <span class="function">msql\_result</span>

msql\_fetch\_row
================

Get row as enumerated array

### 说明

<span class="type">array</span> <span
class="methodname">msql\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">msql\_fetch\_row</span> fetches one row of data
from the result associated with the specified query identifier. The row
is returned as an array. Each result column is stored in an array
offset, starting at offset 0.

Subsequent call to <span class="function">msql\_fetch\_row</span> would
return the next row in the result set, or **`FALSE`** if there are no
more rows.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

### 范例

**示例 \#1 <span class="function">msql\_fetch\_row</span> example**

``` php
<?php
$con = msql_connect();
if (!$con) {
    die('Server connection problem: ' . msql_error());
}

if (!msql_select_db('test', $con)) {
    die('Database connection problem: ' . msql_error());
}

$result = msql_query('SELECT id, name FROM people', $con);
if (!$result) {
    die('Query execution problem: ' . msql_error());
}

while ($row = msql_fetch_row($result)) {
    echo $row[0] . ': ' . $row[1] . "\n";
}

msql_free_result($result);
?>
```

### 更新日志

| 版本  | 说明                                                                                                                                   |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| 5.0.4 | A bug was fixed when retrieving data from columns containing **`NULL`** values. Such columns were not placed into the resulting array. |

### 参见

-   <span class="function">msql\_fetch\_array</span>
-   <span class="function">msql\_fetch\_object</span>
-   <span class="function">msql\_data\_seek</span>
-   <span class="function">msql\_result</span>

msql\_field\_flags
==================

Get field flags

### 说明

<span class="type">string</span> <span
class="methodname">msql\_field\_flags</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

<span class="function">msql\_field\_flags</span> returns the field flags
of the specified field.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

` field_offset`  
数值型字段偏移量。 `field_offset` 从 *1* 开始。

### 返回值

Returns a string containing the field flags of the specified key. This
can be: *primary key not null*, *not null*, *primary key*, *unique not
null* or *unique*.

msql\_field\_len
================

Get field length

### 说明

<span class="type">int</span> <span
class="methodname">msql\_field\_len</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

<span class="function">msql\_field\_len</span> returns the length of the
specified field.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

` field_offset`  
数值型字段偏移量。 `field_offset` 从 *1* 开始。

### 返回值

Returns the length of the specified field or **`FALSE`** on error.

msql\_field\_name
=================

Get the name of the specified field in a result

### 说明

<span class="type">string</span> <span
class="methodname">msql\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

<span class="function">msql\_field\_name</span> gets the name of the
specified field index.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

` field_offset`  
数值型字段偏移量。 `field_offset` 从 *1* 开始。

### 返回值

The name of the field 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">msql\_field\_len</span>

msql\_field\_seek
=================

Set field offset

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_field\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

Seeks to the specified field offset. If the next call to <span
class="function">msql\_fetch\_field</span> won't include a field offset,
this field would be returned.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

` field_offset`  
数值型字段偏移量。 `field_offset` 从 *1* 开始。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">msql\_fetch\_field</span>

msql\_field\_table
==================

Get table name for field

### 说明

<span class="type">int</span> <span
class="methodname">msql\_field\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

Returns the name of the table that the specified field is in.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

` field_offset`  
数值型字段偏移量。 `field_offset` 从 *1* 开始。

### 返回值

The name of the table on success 或者在失败时返回 **`FALSE`**.

msql\_field\_type
=================

Get field type

### 说明

<span class="type">string</span> <span
class="methodname">msql\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

<span class="function">msql\_field\_type</span> gets the type of the
specified field index.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

` field_offset`  
数值型字段偏移量。 `field_offset` 从 *1* 开始。

### 返回值

The type of the field. One of *int*, *char*, *real*, *ident*, *null* or
*unknown*. This functions will return **`FALSE`** on failure.

msql\_fieldflags
================

Alias of <span class="function">msql\_field\_flags</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_field\_flags</span>.

msql\_fieldlen
==============

Alias of <span class="function">msql\_field\_len</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_field\_len</span>.

msql\_fieldname
===============

Alias of <span class="function">msql\_field\_name</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_field\_name</span>.

msql\_fieldtable
================

Alias of <span class="function">msql\_field\_table</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_field\_table</span>.

msql\_fieldtype
===============

Alias of <span class="function">msql\_field\_type</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_field\_type</span>.

msql\_free\_result
==================

Free result memory

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">msql\_free\_result</span> frees the memory
associated with `query_identifier`. When PHP completes a request, this
memory is freed automatically, so you only need to call this function
when you want to make sure you don't use too much memory while the
script is running.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

msql\_list\_dbs
===============

List mSQL databases on server

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_list\_dbs</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">msql\_list\_tables</span> lists the databases
available on the specified `link_identifier`.

### 参数

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

Returns a result set which may be traversed with any function that
fetches result sets, such as <span
class="function">msql\_fetch\_array</span>. On failure, this function
will return **`FALSE`**.

### 参见

-   <span class="function">msql\_list\_tables</span>
-   <span class="function">msql\_list\_fields</span>

msql\_list\_fields
==================

List result fields

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_list\_fields</span> ( <span
class="methodparam"><span class="type">string</span> `$database`</span>
, <span class="methodparam"><span class="type">string</span>
`$tablename`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">msql\_list\_fields</span> returns information
about the given table.

### 参数

`database`  
The name of the database.

`tablename`  
The name of the table.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

Returns a result set which may be traversed with any function that
fetches result sets, such as <span
class="function">msql\_fetch\_array</span>. On failure, this function
will return **`FALSE`**.

### 参见

-   <span class="function">msql\_list\_tables</span>
-   <span class="function">msql\_list\_dbs</span>

msql\_list\_tables
==================

List tables in an mSQL database

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_list\_tables</span> ( <span
class="methodparam"><span class="type">string</span> `$database`</span>
\[, <span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">msql\_list\_tables</span> lists the tables on the
specified `database`.

### 参数

`database`  
The name of the database.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

Returns a result set which may be traversed with any function that
fetches result sets, such as <span
class="function">msql\_fetch\_array</span>. On failure, this function
will return **`FALSE`**.

### 参见

-   <span class="function">msql\_list\_fields</span>
-   <span class="function">msql\_list\_dbs</span>

msql\_num\_fields
=================

Get number of fields in result

### 说明

<span class="type">int</span> <span
class="methodname">msql\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">msql\_num\_fields</span> returns the number of
fields in a result set.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

### 返回值

Returns the number of fields in the result set.

### 参见

-   <span class="function">msql\_query</span>
-   <span class="function">msql\_fetch\_field</span>
-   <span class="function">msql\_num\_rows</span>

msql\_num\_rows
===============

Get number of rows in result

### 说明

<span class="type">int</span> <span
class="methodname">msql\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span>
`$query_identifier`</span> )

<span class="function">msql\_num\_rows</span> returns the number of rows
in a result set.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

### 返回值

Returns the number of rows in the result set.

### 参见

-   <span class="function">msql\_num\_fields</span>

msql\_numfields
===============

Alias of <span class="function">msql\_num\_fields</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_num\_fields</span>.

msql\_numrows
=============

Alias of <span class="function">msql\_num\_rows</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_num\_rows</span>.

msql\_pconnect
==============

Open persistent mSQL connection

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_pconnect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
\] )

<span class="function">msql\_pconnect</span> acts very much like <span
class="function">msql\_connect</span> with two major differences.

First, when connecting, the function would first try to find a
(persistent) link that's already open with the same host. If one is
found, an identifier for it will be returned instead of opening a new
connection.

Second, the connection to the SQL server will not be closed when the
execution of the script ends. Instead, the link will remain open for
future use (<span class="function">msql\_close</span> will not close
links established by this function).

### 参数

`hostname`  
The hostname can also include a port number. e.g. *hostname,port*.

If not specified, the connection is established by the means of a Unix
domain socket, being more efficient than a localhost TCP socket
connection.

> **Note**: <span class="simpara"> While this function will accept a
> colon (*:*) as a host/port separator, a comma (*,*) is the preferred
> method. </span>

### 返回值

Returns a positive mSQL link identifier on success, or **`FALSE`** on
error.

### 参见

-   <span class="function">msql\_connect</span>
-   <span class="function">msql\_close</span>

msql\_query
===========

Send mSQL query

### 说明

<span class="type">resource</span> <span
class="methodname">msql\_query</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">msql\_query</span> sends a query to the currently
active database on the server that's associated with the specified link
identifier.

### 参数

`query`  
The SQL query.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

Returns a positive mSQL query identifier on success, or **`FALSE`** on
error.

### 范例

**示例 \#1 <span class="function">msql\_query</span> example**

``` php
<?php 
$link = msql_connect("dbserver")
   or die("unable to connect to msql server: " . msql_error());
msql_select_db("db", $link)
   or die("unable to select database 'db': " . msql_error());

$result = msql_query("SELECT * FROM table WHERE id=1", $link);
if (!$result) {
   die("query failed: " . msql_error());
}

while ($row = msql_fetch_array($result)) {
    echo $row["id"];
}
?>
```

### 参见

-   <span class="function">msql\_db\_query</span>
-   <span class="function">msql\_select\_db</span>
-   <span class="function">msql\_connect</span>

msql\_regcase
=============

Alias of <span class="function">sql\_regcase</span>

### 说明

此函数是该函数的别名： <span class="function">sql\_regcase</span>.

msql\_result
============

Get result data

### 说明

<span class="type">string</span> <span
class="methodname">msql\_result</span> ( <span class="methodparam"><span
class="type">resource</span> `$result`</span> , <span
class="methodparam"><span class="type">int</span> `$row`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$field`</span> \] )

<span class="function">msql\_result</span> returns the contents of one
cell from a mSQL result set.

When working on large result sets, you should consider using one of the
functions that fetch an entire row (specified below). As these functions
return the contents of multiple cells in one function call, they are
often much quicker than <span class="function">msql\_result</span>.

Recommended high-performance alternatives: <span
class="function">msql\_fetch\_row</span>, <span
class="function">msql\_fetch\_array</span>, and <span
class="function">msql\_fetch\_object</span>.

### 参数

` result`  
<span class="type">resource</span> 型的结果集。此结果集来自对 <span
class="function">msql\_query</span> 的调用。

`row`  
The row offset.

`field`  
Can be the field's offset, or the field's name, or the field's table dot
field's name (tablename.fieldname.). If the column name has been aliased
('select foo as bar from ...'), use the alias instead of the column
name.

> **Note**:
>
> Specifying a numeric field offset is much quicker than specifying a
> fieldname or tablename.fieldname.

### 返回值

Returns the contents of the cell at the row and offset in the specified
mSQL result set.

msql\_select\_db
================

Select mSQL database

### 说明

<span class="type">bool</span> <span
class="methodname">msql\_select\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">msql\_select\_db</span> sets the current active
database on the server that's associated with the specified
`link_identifier`.

Subsequent calls to <span class="function">msql\_query</span> will be
made on the active database.

### 参数

`database_name`  
The database name.

` link_identifier`  
mSQL 连接。如果不指定，则使用由 <span
class="function">msql\_connect</span>
最近打开的连接。如果没有找到该连接，函数会尝试通过调用 <span
class="function">msql\_connect</span> 建立连接并使用它。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">msql\_connect</span>
-   <span class="function">msql\_pconnect</span>
-   <span class="function">msql\_query</span>

msql\_tablename
===============

Alias of <span class="function">msql\_result</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_result</span>.

msql
====

Alias of <span class="function">msql\_db\_query</span>

### 说明

此函数是该函数的别名： <span class="function">msql\_db\_query</span>.

**目录**

-   [msql\_affected\_rows](/book/msql.html#msql_affected_rows) — Returns
    number of affected rows
-   [msql\_close](/book/msql.html#msql_close) — Close mSQL connection
-   [msql\_connect](/book/msql.html#msql_connect) — Open mSQL connection
-   [msql\_create\_db](/book/msql.html#msql_create_db) — Create mSQL
    database
-   [msql\_createdb](/book/msql.html#msql_createdb) — 别名
    msql\_create\_db
-   [msql\_data\_seek](/book/msql.html#msql_data_seek) — Move internal
    row pointer
-   [msql\_db\_query](/book/msql.html#msql_db_query) — Send mSQL query
-   [msql\_dbname](/book/msql.html#msql_dbname) — 别名 msql\_result
-   [msql\_drop\_db](/book/msql.html#msql_drop_db) — Drop (delete) mSQL
    database
-   [msql\_error](/book/msql.html#msql_error) — Returns error message of
    last msql call
-   [msql\_fetch\_array](/book/msql.html#msql_fetch_array) — Fetch row
    as array
-   [msql\_fetch\_field](/book/msql.html#msql_fetch_field) — Get field
    information
-   [msql\_fetch\_object](/book/msql.html#msql_fetch_object) — Fetch row
    as object
-   [msql\_fetch\_row](/book/msql.html#msql_fetch_row) — Get row as
    enumerated array
-   [msql\_field\_flags](/book/msql.html#msql_field_flags) — Get field
    flags
-   [msql\_field\_len](/book/msql.html#msql_field_len) — Get field
    length
-   [msql\_field\_name](/book/msql.html#msql_field_name) — Get the name
    of the specified field in a result
-   [msql\_field\_seek](/book/msql.html#msql_field_seek) — Set field
    offset
-   [msql\_field\_table](/book/msql.html#msql_field_table) — Get table
    name for field
-   [msql\_field\_type](/book/msql.html#msql_field_type) — Get field
    type
-   [msql\_fieldflags](/book/msql.html#msql_fieldflags) — Alias of
    msql\_field\_flags
-   [msql\_fieldlen](/book/msql.html#msql_fieldlen) — Alias of
    msql\_field\_len
-   [msql\_fieldname](/book/msql.html#msql_fieldname) — Alias of
    msql\_field\_name
-   [msql\_fieldtable](/book/msql.html#msql_fieldtable) — Alias of
    msql\_field\_table
-   [msql\_fieldtype](/book/msql.html#msql_fieldtype) — Alias of
    msql\_field\_type
-   [msql\_free\_result](/book/msql.html#msql_free_result) — Free result
    memory
-   [msql\_list\_dbs](/book/msql.html#msql_list_dbs) — List mSQL
    databases on server
-   [msql\_list\_fields](/book/msql.html#msql_list_fields) — List result
    fields
-   [msql\_list\_tables](/book/msql.html#msql_list_tables) — List tables
    in an mSQL database
-   [msql\_num\_fields](/book/msql.html#msql_num_fields) — Get number of
    fields in result
-   [msql\_num\_rows](/book/msql.html#msql_num_rows) — Get number of
    rows in result
-   [msql\_numfields](/book/msql.html#msql_numfields) — Alias of
    msql\_num\_fields
-   [msql\_numrows](/book/msql.html#msql_numrows) — Alias of
    msql\_num\_rows
-   [msql\_pconnect](/book/msql.html#msql_pconnect) — Open persistent
    mSQL connection
-   [msql\_query](/book/msql.html#msql_query) — Send mSQL query
-   [msql\_regcase](/book/msql.html#msql_regcase) — Alias of
    sql\_regcase
-   [msql\_result](/book/msql.html#msql_result) — Get result data
-   [msql\_select\_db](/book/msql.html#msql_select_db) — Select mSQL
    database
-   [msql\_tablename](/book/msql.html#msql_tablename) — Alias of
    msql\_result
-   [msql](/book/msql.html#msql) — Alias of msql\_db\_query
