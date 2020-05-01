FrontBase
=========

**目录**

-   [简介](/book/fbsql.html#简介)
-   [安装／配置](/book/fbsql.html#安装／配置)
    -   [需求](/book/fbsql.html#需求)
    -   [安装](/book/fbsql.html#安装)
    -   [运行时配置](/book/fbsql.html#运行时配置)
    -   [资源类型](/book/fbsql.html#资源类型)
-   [预定义常量](/book/fbsql.html#预定义常量)
-   [FrontBase 函数](/book/fbsql.html#FrontBase%20函数)
    -   [fbsql\_affected\_rows](/book/fbsql.html#fbsql_affected_rows) —
        Get number of affected rows in previous FrontBase operation
    -   [fbsql\_autocommit](/book/fbsql.html#fbsql_autocommit) — Enable
        or disable autocommit
    -   [fbsql\_blob\_size](/book/fbsql.html#fbsql_blob_size) — Get the
        size of a BLOB
    -   [fbsql\_change\_user](/book/fbsql.html#fbsql_change_user) —
        Change logged in user of the active connection
    -   [fbsql\_clob\_size](/book/fbsql.html#fbsql_clob_size) — Get the
        size of a CLOB
    -   [fbsql\_close](/book/fbsql.html#fbsql_close) — Close FrontBase
        connection
    -   [fbsql\_commit](/book/fbsql.html#fbsql_commit) — Commits a
        transaction to the database
    -   [fbsql\_connect](/book/fbsql.html#fbsql_connect) — Open a
        connection to a FrontBase Server
    -   [fbsql\_create\_blob](/book/fbsql.html#fbsql_create_blob) —
        Create a BLOB
    -   [fbsql\_create\_clob](/book/fbsql.html#fbsql_create_clob) —
        Create a CLOB
    -   [fbsql\_create\_db](/book/fbsql.html#fbsql_create_db) — Create a
        FrontBase database
    -   [fbsql\_data\_seek](/book/fbsql.html#fbsql_data_seek) — Move
        internal result pointer
    -   [fbsql\_database\_password](/book/fbsql.html#fbsql_database_password)
        — Sets or retrieves the password for a FrontBase database
    -   [fbsql\_database](/book/fbsql.html#fbsql_database) — Get or set
        the database name used with a connection
    -   [fbsql\_db\_query](/book/fbsql.html#fbsql_db_query) — Send a
        FrontBase query
    -   [fbsql\_db\_status](/book/fbsql.html#fbsql_db_status) — Get the
        status for a given database
    -   [fbsql\_drop\_db](/book/fbsql.html#fbsql_drop_db) — Drop
        (delete) a FrontBase database
    -   [fbsql\_errno](/book/fbsql.html#fbsql_errno) — Returns the error
        number from previous operation
    -   [fbsql\_error](/book/fbsql.html#fbsql_error) — Returns the error
        message from previous operation
    -   [fbsql\_fetch\_array](/book/fbsql.html#fbsql_fetch_array) —
        Fetch a result row as an associative array, a numeric array, or
        both
    -   [fbsql\_fetch\_assoc](/book/fbsql.html#fbsql_fetch_assoc) —
        Fetch a result row as an associative array
    -   [fbsql\_fetch\_field](/book/fbsql.html#fbsql_fetch_field) — Get
        column information from a result and return as an object
    -   [fbsql\_fetch\_lengths](/book/fbsql.html#fbsql_fetch_lengths) —
        Get the length of each output in a result
    -   [fbsql\_fetch\_object](/book/fbsql.html#fbsql_fetch_object) —
        Fetch a result row as an object
    -   [fbsql\_fetch\_row](/book/fbsql.html#fbsql_fetch_row) — Get a
        result row as an enumerated array
    -   [fbsql\_field\_flags](/book/fbsql.html#fbsql_field_flags) — Get
        the flags associated with the specified field in a result
    -   [fbsql\_field\_len](/book/fbsql.html#fbsql_field_len) — Returns
        the length of the specified field
    -   [fbsql\_field\_name](/book/fbsql.html#fbsql_field_name) — Get
        the name of the specified field in a result
    -   [fbsql\_field\_seek](/book/fbsql.html#fbsql_field_seek) — Set
        result pointer to a specified field offset
    -   [fbsql\_field\_table](/book/fbsql.html#fbsql_field_table) — Get
        name of the table the specified field is in
    -   [fbsql\_field\_type](/book/fbsql.html#fbsql_field_type) — Get
        the type of the specified field in a result
    -   [fbsql\_free\_result](/book/fbsql.html#fbsql_free_result) — Free
        result memory
    -   [fbsql\_get\_autostart\_info](/book/fbsql.html#fbsql_get_autostart_info)
        — 说明
    -   [fbsql\_hostname](/book/fbsql.html#fbsql_hostname) — Get or set
        the host name used with a connection
    -   [fbsql\_insert\_id](/book/fbsql.html#fbsql_insert_id) — Get the
        id generated from the previous INSERT operation
    -   [fbsql\_list\_dbs](/book/fbsql.html#fbsql_list_dbs) — List
        databases available on a FrontBase server
    -   [fbsql\_list\_fields](/book/fbsql.html#fbsql_list_fields) — List
        FrontBase result fields
    -   [fbsql\_list\_tables](/book/fbsql.html#fbsql_list_tables) — List
        tables in a FrontBase database
    -   [fbsql\_next\_result](/book/fbsql.html#fbsql_next_result) — Move
        the internal result pointer to the next result
    -   [fbsql\_num\_fields](/book/fbsql.html#fbsql_num_fields) — Get
        number of fields in result
    -   [fbsql\_num\_rows](/book/fbsql.html#fbsql_num_rows) — Get number
        of rows in result
    -   [fbsql\_password](/book/fbsql.html#fbsql_password) — Get or set
        the user password used with a connection
    -   [fbsql\_pconnect](/book/fbsql.html#fbsql_pconnect) — Open a
        persistent connection to a FrontBase Server
    -   [fbsql\_query](/book/fbsql.html#fbsql_query) — Send a FrontBase
        query
    -   [fbsql\_read\_blob](/book/fbsql.html#fbsql_read_blob) — Read a
        BLOB from the database
    -   [fbsql\_read\_clob](/book/fbsql.html#fbsql_read_clob) — Read a
        CLOB from the database
    -   [fbsql\_result](/book/fbsql.html#fbsql_result) — Get result data
    -   [fbsql\_rollback](/book/fbsql.html#fbsql_rollback) — Rollback a
        transaction to the database
    -   [fbsql\_rows\_fetched](/book/fbsql.html#fbsql_rows_fetched) —
        Get the number of rows affected by the last statement
    -   [fbsql\_select\_db](/book/fbsql.html#fbsql_select_db) — Select a
        FrontBase database
    -   [fbsql\_set\_characterset](/book/fbsql.html#fbsql_set_characterset)
        — Change input/output character set
    -   [fbsql\_set\_lob\_mode](/book/fbsql.html#fbsql_set_lob_mode) —
        Set the LOB retrieve mode for a FrontBase result set
    -   [fbsql\_set\_password](/book/fbsql.html#fbsql_set_password) —
        Change the password for a given user
    -   [fbsql\_set\_transaction](/book/fbsql.html#fbsql_set_transaction)
        — Set the transaction locking and isolation
    -   [fbsql\_start\_db](/book/fbsql.html#fbsql_start_db) — Start a
        database on local or remote server
    -   [fbsql\_stop\_db](/book/fbsql.html#fbsql_stop_db) — Stop a
        database on local or remote server
    -   [fbsql\_table\_name](/book/fbsql.html#fbsql_table_name) — Get
        table name of field
    -   [fbsql\_tablename](/book/fbsql.html#fbsql_tablename) — 别名
        fbsql\_table\_name
    -   [fbsql\_username](/book/fbsql.html#fbsql_username) — Get or set
        the username for the connection
    -   [fbsql\_warnings](/book/fbsql.html#fbsql_warnings) — Enable or
        disable FrontBase warnings

These functions allow you to access FrontBase database servers. More
information about FrontBase can be found at
<a href="http://www.frontbase.com/" class="link external">» http://www.frontbase.com/</a>.

Documentation for FrontBase can be found at
<a href="http://www.frontbase.com/cgi-bin/WebObjects/FBWebSite.woa" class="link external">» http://www.frontbase.com/cgi-bin/WebObjects/FBWebSite.woa</a>.

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.3.0.

安装／配置
==========

**目录**

-   [需求](/book/fbsql.html#需求)
-   [安装](/book/fbsql.html#安装)
-   [运行时配置](/book/fbsql.html#运行时配置)
-   [资源类型](/book/fbsql.html#资源类型)

需求
----

You must install the FrontBase database server or at least the fbsql
client libraries to use this functions. You can get FrontBase from
<a href="http://www.frontbase.com/" class="link external">» http://www.frontbase.com/</a>.

安装
----

In order to have these functions available, you must compile PHP with
fbsql support by using the **--with-fbsql\[=DIR\]** option. If you use
this option without specifying the path to fbsql, PHP will search for
the fbsql client libraries in the default installation location for the
platform. Users who installed FrontBase in a non standard directory
should always specify the path to fbsql:
**--with-fbsql=/path/to/fbsql**. This will force PHP to use the client
libraries installed by FrontBase, avoiding any conflicts.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                              | 默认       | 可修改范围       | 更新日志              |
|-----------------------------------|------------|------------------|-----------------------|
| fbsql.allow\_persistent           | "1"        | PHP\_INI\_SYSTEM |                       |
| fbsql.generate\_warnings          | "0"        | PHP\_INI\_SYSTEM |                       |
| fbsql.autocommit                  | "1"        | PHP\_INI\_SYSTEM |                       |
| fbsql.max\_persistent             | "-1"       | PHP\_INI\_SYSTEM |                       |
| fbsql.max\_links                  | "128"      | PHP\_INI\_SYSTEM |                       |
| fbsql.max\_connections            | "128"      | PHP\_INI\_SYSTEM |                       |
| fbsql.max\_results                | "128"      | PHP\_INI\_SYSTEM |                       |
| fbsql.batchSize                   | "1000"     | PHP\_INI\_SYSTEM | Removed in PHP 5.1.0. |
| fbsql.default\_host               | NULL       | PHP\_INI\_SYSTEM |                       |
| fbsql.default\_user               | "\_SYSTEM" | PHP\_INI\_SYSTEM |                       |
| fbsql.default\_password           | ""         | PHP\_INI\_SYSTEM |                       |
| fbsql.default\_database           | ""         | PHP\_INI\_SYSTEM |                       |
| fbsql.default\_database\_password | ""         | PHP\_INI\_SYSTEM |                       |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

资源类型
--------

此扩展没有定义资源类型。

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`FBSQL_ASSOC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_NUM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_BOTH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_LOCK_DEFERRED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_LOCK_OPTIMISTIC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_LOCK_PESSIMISTIC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_ISO_READ_UNCOMMITTED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_ISO_READ_COMMITTED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_ISO_REPEATABLE_READ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_ISO_SERIALIZABLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_ISO_VERSIONED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_UNKNOWN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_STOPPED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_STARTING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_RUNNING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_STOPPING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_NOEXEC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_LOB_DIRECT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FBSQL_LOB_HANDLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

fbsql\_affected\_rows
=====================

Get number of affected rows in previous FrontBase operation

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_affected\_rows</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">fbsql\_affected\_rows</span> returns the number
of rows affected by the last INSERT, UPDATE or DELETE query associated
with `link_identifier`.

> **Note**:
>
> If you are using transactions, you need to call <span
> class="function">fbsql\_affected\_rows</span> after your INSERT,
> UPDATE, or DELETE query, not after the commit.

If the last query was a DELETE query with no WHERE clause, all of the
records will have been deleted from the table but this function will
return zero.

> **Note**:
>
> When using UPDATE, FrontBase will not update columns where the new
> value is the same as the old value. This creates the possibility that
> <span class="function">fbsql\_affected\_rows</span> may not actually
> equal the number of rows matched, only the number of rows that were
> literally affected by the query.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

If the last query failed, this function will return -1.

### 参见

-   <span class="function">fbsql\_num\_rows</span>

fbsql\_autocommit
=================

Enable or disable autocommit

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$OnOff`</span> \] )

Returns the current autocommit status.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`OnOff`  
If this optional parameter is given the auto commit status will be
changed.

With `OnOff` set to **`TRUE`** each statement will be committed
automatically, if no errors was found.

With OnOff set to **`FALSE`** the user must commit or rollback the
transaction using either <span class="function">fbsql\_commit</span> or
<span class="function">fbsql\_rollback</span>.

### 返回值

Returns the current autocommit status, as a boolean.

### 参见

-   <span class="function">fbsql\_commit</span>
-   <span class="function">fbsql\_rollback</span>

fbsql\_blob\_size
=================

Get the size of a BLOB

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_blob\_size</span> ( <span
class="methodparam"><span class="type">string</span>
`$blob_handle`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Returns the size of the given BLOB.

### 参数

`blob_handle`  
A BLOB handle, returned by <span
class="function">fbsql\_create\_blob</span>.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns the BLOB size as an integer, or **`FALSE`** on error.

### 参见

-   <span class="function">fbsql\_clob\_size</span>

fbsql\_change\_user
===================

Change logged in user of the active connection

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_change\_user</span> ( <span
class="methodparam"><span class="type">string</span> `$user`</span> ,
<span class="methodparam"><span class="type">string</span>
`$password`</span> \[, <span class="methodparam"><span
class="type">string</span> `$database`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \]\] )

<span class="function">fbsql\_change\_user</span> changes the logged in
user of the specified connection. If the new user and password
authorization fails, the current connected user stays active.

### 参数

`user`  
The new user name.

`password`  
The new user password.

`database`  
If specified, this will be the default or current database after the
user has been changed.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

fbsql\_clob\_size
=================

Get the size of a CLOB

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_clob\_size</span> ( <span
class="methodparam"><span class="type">string</span>
`$clob_handle`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Returns the size of the given CLOB.

### 参数

`clob_handle`  
A CLOB handle, returned by <span
class="function">fbsql\_create\_clob</span>.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns the CLOB size as an integer, or **`FALSE`** on error.

### 参见

-   <span class="function">fbsql\_blob\_size</span>

fbsql\_close
============

Close FrontBase connection

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Closes the connection to the FrontBase server that's associated with the
specified link identifier.

Using <span class="function">fbsql\_close</span> isn't usually
necessary, as non-persistent open links are automatically closed at the
end of the script's execution.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">fbsql\_close</span> example**

``` php
<?php
$link = fbsql_connect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
echo "Connected successfully";
fbsql_close($link);
?>
```

### 参见

-   <span class="function">fbsql\_connect</span>
-   <span class="function">fbsql\_pconnect</span>

fbsql\_commit
=============

Commits a transaction to the database

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_commit</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Ends the current transaction by writing all inserts, updates and deletes
to the disk and unlocking all row and table locks held by the
transaction. This command is only needed if autocommit is set to false.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_autocommit</span>
-   <span class="function">fbsql\_rollback</span>

fbsql\_connect
==============

Open a connection to a FrontBase Server

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$hostname`<span
class="initializer"> = ini\_get("fbsql.default\_host")</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$username`<span class="initializer"> =
ini\_get("fbsql.default\_user")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = ini\_get("fbsql.default\_password")</span></span>
\]\]\] )

<span class="function">fbsql\_connect</span> establishes a connection to
a FrontBase server.

If a second call is made to <span class="function">fbsql\_connect</span>
with the same arguments, no new link will be established, but instead,
the link identifier of the already opened link will be returned.

The link to the server will be closed as soon as the execution of the
script ends, unless it's closed earlier by explicitly calling <span
class="function">fbsql\_close</span>.

### 参数

`hostname`  
The server host name.

`username`  
The user name for the connection.

`password`  
The password for the connection.

### 返回值

Returns a positive FrontBase link identifier on success, or **`FALSE`**
on errors.

### 范例

**示例 \#1 <span class="function">fbsql\_connect</span> example**

``` php
<?php

$link = fbsql_connect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
echo "Connected successfully";
fbsql_close($link);

?>
```

### 参见

-   <span class="function">fbsql\_pconnect</span>
-   <span class="function">fbsql\_close</span>

fbsql\_create\_blob
===================

Create a BLOB

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_create\_blob</span> ( <span
class="methodparam"><span class="type">string</span> `$blob_data`</span>
\[, <span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Creates a BLOB from the given data.

### 参数

`blob_data`  
The BLOB data.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a resource handle to the newly created BLOB, which can be used
with insert and update commands to store the BLOB in the database.

### 范例

**示例 \#1 <span class="function">fbsql\_create\_blob</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
$filename = "blobfile.bin";
$fp = fopen($filename, "rb");
$blobdata = fread($fp, filesize($filename));
fclose($fp);

$blobHandle = fbsql_create_blob($blobdata, $link);

$sql = "INSERT INTO BLOB_TABLE (BLOB_COLUMN) VALUES ($blobHandle);";
$rs = fbsql_query($sql, $link);
?>
```

### 参见

-   <span class="function">fbsql\_create\_clob</span>
-   <span class="function">fbsql\_read\_blob</span>
-   <span class="function">fbsql\_read\_clob</span>
-   <span class="function">fbsql\_set\_lob\_mode</span>

fbsql\_create\_clob
===================

Create a CLOB

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_create\_clob</span> ( <span
class="methodparam"><span class="type">string</span> `$clob_data`</span>
\[, <span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Creates a CLOB from the given data.

### 参数

`clob_data`  
The CLOB data.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a resource handle to the newly created CLOB, which can be used
with insert and update commands to store the CLOB in the database.

### 范例

**示例 \#1 <span class="function">fbsql\_create\_clob</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
$filename = "clob_file.txt";
$fp = fopen($filename, "rb");
$clobdata = fread($fp, filesize($filename));
fclose($fp);

$clobHandle = fbsql_create_clob($clobdata, $link);

$sql = "INSERT INTO CLOB_TABLE (CLOB_COLUMN) VALUES ($clobHandle);";
$rs = fbsql_query($sql, $link);
?>
```

### 参见

-   <span class="function">fbsql\_create\_blob</span>
-   <span class="function">fbsql\_read\_blob</span>
-   <span class="function">fbsql\_read\_clob</span>
-   <span class="function">fbsql\_set\_lob\_mode</span>

fbsql\_create\_db
=================

Create a FrontBase database

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_create\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$database_options`</span> \]\] )

Attempts to create a new database on the specified server.

### 参数

`database_name`  
The database name, as a string.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`database_options`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">fbsql\_create\_db</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
if (fbsql_create_db("my_db")) {
    echo "Database created successfully\n";
} else {
    printf("Error creating database: %s\n", fbsql_error());
}
?>
```

### 参见

-   <span class="function">fbsql\_drop\_db</span>

fbsql\_data\_seek
=================

Move internal result pointer

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$row_number`</span> )

Moves the internal row pointer of the FrontBase result associated with
the specified result identifier to point to the specified row number.

The next call to <span class="function">fbsql\_fetch\_row</span> would
return that row.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`row_number`  
The row number. Starts at 0.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">fbsql\_data\_seek</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");

fbsql_select_db("samp_db")
    or die("Could not select database");

$query = "SELECT last_name, first_name FROM friends;";
$result = fbsql_query($query)
    or die("Query failed");

// fetch rows in reverse order

for ($i = fbsql_num_rows($result) - 1; $i >=0; $i--) {
    if (!fbsql_data_seek($result, $i)) {
        printf("Cannot seek to row %d\n", $i);
        continue;
    }

    if (!($row = fbsql_fetch_object($result)))
        continue;

    echo $row->last_name . $row->first_name . "<br />\n";
}

fbsql_free_result($result);
?>
```

fbsql\_database\_password
=========================

Sets or retrieves the password for a FrontBase database

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_database\_password</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$database_password`</span> \] )

Sets and retrieves the database password used by the connection. If a
database is protected by a database password, the user must call this
function before calling <span class="function">fbsql\_select\_db</span>.

If no link is open, the function will try to establish a link as if
<span class="function">fbsql\_connect</span> was called, and use it.

This function does not change the database password in the database nor
can it be used to retrieve the database password for a database.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`database_password`  
The database password, as a string. If given, the function sets the
database password for the specified link identifier.

### 返回值

Returns the database password associated with the link identifier.

### 范例

**示例 \#1 <span class="function">fbsql\_create\_clob</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
fbsql_database_password($link, "secret db password");
fbsql_select_db($database, $link);
?>
```

### 参见

-   <span class="function">fbsql\_connect</span>
-   <span class="function">fbsql\_pconnect</span>
-   <span class="function">fbsql\_select\_db</span>

fbsql\_database
===============

Get or set the database name used with a connection

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_database</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$database`</span> \] )

Get or set the database name used with the connection.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`database`  
The database name. If given, the default database of the connexion will
be changed to `database`.

### 返回值

Returns the name of the database used with this connection.

fbsql\_db\_query
================

Send a FrontBase query

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_db\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$database`</span>
, <span class="methodparam"><span class="type">string</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Selects a database and executes a query on it.

### 参数

`database`  
The database to be selected.

`query`  
The SQL query to be executed.

> **Note**:
>
> The query string shall always end with a semicolon.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a positive FrontBase result identifier to the query result, or
**`FALSE`** on error.

### 参见

-   <span class="function">fbsql\_query</span>
-   <span class="function">fbsql\_connect</span>

fbsql\_db\_status
=================

Get the status for a given database

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_db\_status</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Gets the current status of the specified database.

### 参数

`database_name`  
The database name.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns an integer value with the current status. This can be one of the
following constants:

-   <span class="simpara"> **`FALSE`** - The exec handler for the host
    was invalid. This error will occur when the `link_identifier`
    connects directly to a database by using a port number. FBExec can
    be available on the server but no connection has been made for it.
    </span>
-   <span class="simpara"> **`FBSQL_UNKNOWN`** - The Status is unknown.
    </span>
-   <span class="simpara"> **`FBSQL_STOPPED`** - The database is not
    running. Use <span class="function">fbsql\_start\_db</span> to start
    the database. </span>
-   <span class="simpara"> **`FBSQL_STARTING`** - The database is
    starting. </span>
-   <span class="simpara"> **`FBSQL_RUNNING`** - The database is running
    and can be used to perform SQL operations. </span>
-   <span class="simpara"> **`FBSQL_STOPPING`** - The database is
    stopping. </span>
-   <span class="simpara"> **`FBSQL_NOEXEC`** - FBExec is not running on
    the server and it is not possible to get the status of the database.
    </span>

### 参见

-   <span class="function">fbsql\_start\_db</span>
-   <span class="function">fbsql\_stop\_db</span>

fbsql\_drop\_db
===============

Drop (delete) a FrontBase database

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_drop\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">fbsql\_drop\_db</span> attempts to drop (remove)
an entire database from the server associated with the specified link
identifier.

### 参数

`database_name`  
The database name, as a string.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_create\_db</span>

fbsql\_errno
============

Returns the error number from previous operation

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_errno</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Returns the numerical value of the error message from previous FrontBase
operation.

Errors coming back from the fbsql database backend don't issue warnings.
Instead, use <span class="function">fbsql\_errno</span> to retrieve the
error code. Note that this function only returns the error code from the
most recently executed fbsql function (not including <span
class="function">fbsql\_error</span> and <span
class="function">fbsql\_errno</span>), so if you want to use it, make
sure you check the value before calling another fbsql function.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns the error number from the last fbsql function, or *0* (zero) if
no error occurred.

### 范例

**示例 \#1 <span class="function">fbsql\_errno</span> Example**

``` php
<?php
fbsql_connect("marliesle");
echo fbsql_errno() . ": " . fbsql_error() . "<br />";
fbsql_select_db("nonexistentdb");
echo fbsql_errno() . ": " . fbsql_error() . "<br />";
$conn = fbsql_query("SELECT * FROM nonexistenttable;");
echo fbsql_errno() . ": " . fbsql_error() . "<br />";
?>
```

### 参见

-   <span class="function">fbsql\_error</span>
-   <span class="function">fbsql\_warnings</span>

fbsql\_error
============

Returns the error message from previous operation

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Returns the error message from previous FrontBase operation.

Errors coming back from the fbsql database backend don't issue warnings.
Instead, use <span class="function">fbsql\_error</span> to retrieve the
error text. Note that this function only returns the error code from the
most recently executed fbsql function (not including <span
class="function">fbsql\_error</span> and <span
class="function">fbsql\_errno</span>), so if you want to use it, make
sure you check the value before calling another fbsql function.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns the error text from the last fbsql function, or *''* (the empty
string) if no error occurred.

### 范例

**示例 \#1 <span class="function">fbsql\_error</span> Example**

``` php
<?php
fbsql_connect("marliesle");
echo fbsql_errno() . ": " . fbsql_error() . "<br />";
fbsql_select_db("nonexistentdb");
echo fbsql_errno() . ": " . fbsql_error() . "<br />";
$conn = fbsql_query("SELECT * FROM nonexistenttable;");
echo fbsql_errno() . ": " . fbsql_error() . "<br />";
?>
```

### 参见

-   <span class="function">fbsql\_errno</span>
-   <span class="function">fbsql\_warnings</span>

fbsql\_fetch\_array
===================

Fetch a result row as an associative array, a numeric array, or both

### 说明

<span class="type">array</span> <span
class="methodname">fbsql\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`</span> \] )

<span class="function">fbsql\_fetch\_array</span> is a combination of
<span class="function">fbsql\_fetch\_row</span> and <span
class="function">fbsql\_fetch\_assoc</span>.

An important thing to note is that using <span
class="function">fbsql\_fetch\_array</span> is NOT significantly slower
than using <span class="function">fbsql\_fetch\_row</span>, while it
provides a significant added value.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`result_type`  
A constant and can take the following values: **`FBSQL_ASSOC`**,
**`FBSQL_NUM`**, or **`FBSQL_BOTH`**.

When using **`FBSQL_BOTH`**, in addition to storing the data in the
numeric indices of the result array, it also stores the data in
associative indices, using the field names as keys.

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

If two or more columns of the result have the same field names, the last
column will take precedence. To access the other column(s) of the same
name, you must the numeric index of the column or make an alias for the
column.

``` sql
select t1.f1 as foo t2.f1 as bar from t1, t2
```

### 范例

**示例 \#1 <span class="function">fbsql\_fetch\_array</span> example**

``` php
<?php
fbsql_connect($host, $user, $password);
$result = fbsql_db_query("database", "select user_id, fullname from table");
while ($row = fbsql_fetch_array($result)) {
    echo "user_id: " . $row["user_id"] . "<br />\n";
    echo "user_id: " . $row[0] . "<br />\n";
    echo "fullname: " . $row["fullname"] . "<br />\n";
    echo "fullname: " . $row[1] . "<br />\n";
}
fbsql_free_result($result);
?>
```

### 参见

-   <span class="function">fbsql\_fetch\_row</span>
-   <span class="function">fbsql\_fetch\_assoc</span>
-   <span class="function">fbsql\_fetch\_object</span>

fbsql\_fetch\_assoc
===================

Fetch a result row as an associative array

### 说明

<span class="type">array</span> <span
class="methodname">fbsql\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Calling <span class="function">fbsql\_fetch\_assoc</span> is equivalent
to calling <span class="function">fbsql\_fetch\_array</span> with
**`FBSQL_ASSOC`** as second parameter. It only returns an associative
array.

This is the way <span class="function">fbsql\_fetch\_array</span>
originally worked. If you need the numeric indices as well as the
associative, use <span class="function">fbsql\_fetch\_array</span>.

An important thing to note is that using <span
class="function">fbsql\_fetch\_assoc</span> is NOT significantly slower
than using <span class="function">fbsql\_fetch\_row</span>, while it
provides a significant added value.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns an associative array that corresponds to the fetched row, or
**`FALSE`** if there are no more rows.

If two or more columns of the result have the same field names, the last
column will take precedence. To access the other column(s) of the same
name, you must use <span class="function">fbsql\_fetch\_array</span> and
have it return the numeric indices as well.

### 范例

**示例 \#1 <span class="function">fbsql\_fetch\_assoc</span> example**

``` php
<?php
fbsql_connect($host, $user, $password);
$result = fbsql_db_query("database", "select * from table");
while ($row = fbsql_fetch_assoc($result)) {
    echo $row["user_id"];
    echo $row["fullname"];
}
fbsql_free_result($result);
?>
```

### 参见

-   <span class="function">fbsql\_fetch\_row</span>
-   <span class="function">fbsql\_fetch\_array</span>
-   <span class="function">fbsql\_fetch\_object</span>

fbsql\_fetch\_field
===================

Get column information from a result and return as an object

### 说明

<span class="type">object</span> <span
class="methodname">fbsql\_fetch\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> \] )

Used in order to obtain information about fields in a certain query
result.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`field_offset`  
The numerical offset of the field. The field index starts at 0. If not
specified, the next field that wasn't yet retrieved by <span
class="function">fbsql\_fetch\_field</span> is retrieved.

### 返回值

Returns an object containing field information, or **`FALSE`** on
errors.

The properties of the object are:

-   <span class="simpara"> name - column name </span>
-   <span class="simpara"> table - name of the table the column belongs
    to </span>
-   <span class="simpara"> max\_length - maximum length of the column
    </span>
-   <span class="simpara"> not\_null - 1 if the column cannot be
    **`NULL`** </span>
-   <span class="simpara"> type - the type of the column </span>

### 范例

**示例 \#1 <span class="function">fbsql\_fetch\_field</span> example**

``` php
<?php
fbsql_connect($host, $user, $password)
    or die("Could not connect");
$result = fbsql_db_query("database", "select * from table")
    or die("Query failed");
# get column metadata
$i = 0;
while ($i < fbsql_num_fields($result)) {
    echo "Information for column $i:<br />\n";
    $meta = fbsql_fetch_field($result);
    if (!$meta) {
        echo "No information available<br />\n";
    }
    echo "<pre>
max_length:   $meta->max_length
name:         $meta->name
not_null:     $meta->not_null
table:        $meta->table
type:         $meta->type
</pre>";
    $i++;
}
fbsql_free_result($result);
?>
```

### 参见

-   <span class="function">fbsql\_field\_seek</span>

fbsql\_fetch\_lengths
=====================

Get the length of each output in a result

### 说明

<span class="type">array</span> <span
class="methodname">fbsql\_fetch\_lengths</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Stores the lengths of each result column in the last row returned by
<span class="function">fbsql\_fetch\_row</span>, <span
class="function">fbsql\_fetch\_array</span> and <span
class="function">fbsql\_fetch\_object</span> in an array.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns an array, starting at offset 0, that corresponds to the lengths
of each field in the last row fetched by <span
class="function">fbsql\_fetch\_row</span>, or **`FALSE`** on error.

### 参见

-   <span class="function">fbsql\_fetch\_row</span>

fbsql\_fetch\_object
====================

Fetch a result row as an object

### 说明

<span class="type">object</span> <span
class="methodname">fbsql\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">fbsql\_fetch\_object</span> is similar to <span
class="function">fbsql\_fetch\_array</span>, with one difference - an
object is returned, instead of an array. Indirectly, that means that you
can only access the data by the field names, and not by their offsets
(numbers are illegal property names).

Speed-wise, the function is identical to <span
class="function">fbsql\_fetch\_array</span>, and almost as quick as
<span class="function">fbsql\_fetch\_row</span> (the difference is
insignificant).

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns an object with properties that correspond to the fetched row, or
**`FALSE`** if there are no more rows.

### 范例

**示例 \#1 <span class="function">fbsql\_fetch\_object</span> example**

``` php
<?php
fbsql_connect($host, $user, $password);
$result = fbsql_db_query("database", "select * from table");
while ($row = fbsql_fetch_object($result)) {
    echo $row->user_id;
    echo $row->fullname;
}
fbsql_free_result($result);
?>
```

### 参见

-   <span class="function">fbsql\_fetch\_array</span>
-   <span class="function">fbsql\_fetch\_row</span>
-   <span class="function">fbsql\_fetch\_assoc</span>

fbsql\_fetch\_row
=================

Get a result row as an enumerated array

### 说明

<span class="type">array</span> <span
class="methodname">fbsql\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">fbsql\_fetch\_row</span> fetches one row of data
from the result associated with the specified result identifier.

Subsequent call to <span class="function">fbsql\_fetch\_row</span> would
return the next row in the result set, or **`FALSE`** if there are no
more rows.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns an array that corresponds to the fetched row where each result
column is stored in an offset, starting at offset 0, or **`FALSE`** if
there are no more rows.

### 参见

-   <span class="function">fbsql\_fetch\_array</span>
-   <span class="function">fbsql\_fetch\_assoc</span>
-   <span class="function">fbsql\_fetch\_object</span>
-   <span class="function">fbsql\_data\_seek</span>
-   <span class="function">fbsql\_fetch\_lengths</span>
-   <span class="function">fbsql\_result</span>

fbsql\_field\_flags
===================

Get the flags associated with the specified field in a result

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_field\_flags</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> \] )

Gets the flags associated with the specified field in a result.

### 参数

`result`  
A result pointer returned by <span
class="function">fbsql\_list\_fields</span>.

`field_offset`  
The numerical offset of the field. The field index starts at 0.

### 返回值

Returns the field flags of the specified field as a single word per flag
separated by a single space, so that you can split the returned value
using <span class="function">explode</span>.

fbsql\_field\_len
=================

Returns the length of the specified field

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_field\_len</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> \] )

Returns the length of the specified field.

### 参数

`result`  
A result pointer returned by <span
class="function">fbsql\_list\_fields</span>.

`field_offset`  
The numerical offset of the field. The field index starts at 0.

### 返回值

Returns the length of the specified field.

fbsql\_field\_name
==================

Get the name of the specified field in a result

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_index`</span> \] )

Returns the name of the specified field index.

### 参数

`result`  
A result pointer returned by <span
class="function">fbsql\_list\_fields</span>.

`field_index`  
The numerical offset of the field. The field index starts at 0.

### 返回值

Returns the name as a string, or **`FALSE`** if the field doesn't exist.

### 范例

**示例 \#1 <span class="function">fbsql\_field\_name</span> example**

``` php
<?php
// The users table consists of three fields:
//   user_id
//   username
//   password.

$res = fbsql_db_query("users", "select * from users", $link);

echo fbsql_field_name($res, 0) . "\n";
echo fbsql_field_name($res, 2);
?>
```

以上例程会输出：

    user_id
    password

### 参见

-   <span class="function">fbsql\_field\_type</span>

fbsql\_field\_seek
==================

Set result pointer to a specified field offset

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_field\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> \] )

Seeks to the specified field offset. If the next call to <span
class="function">fbsql\_fetch\_field</span> doesn't include a field
offset, the field offset specified in <span
class="function">fbsql\_field\_seek</span> will be returned.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`field_offset`  
The numerical offset of the field. The field index starts at 0.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_fetch\_field</span>

fbsql\_field\_table
===================

Get name of the table the specified field is in

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_field\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> \] )

Returns the name of the table that the specified field is in.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`field_offset`  
The numerical offset of the field. The field index starts at 0.

### 返回值

Returns the name of the table, as a string.

fbsql\_field\_type
==================

Get the type of the specified field in a result

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> \] )

<span class="function">fbsql\_field\_type</span> is similar to the <span
class="function">fbsql\_field\_name</span> function, but the field type
is returned instead.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`field_offset`  
The numerical offset of the field. The field index starts at 0.

### 返回值

Returns the field type, as a string.

This can be one of *int*, *real*, *string*, *blob*, and others as
detailed in the
<a href="http://www.frontbase.com/cgi-bin/WebObjects/FBWebSite.woa" class="link external">» FrontBase documentation</a>.

### 范例

**示例 \#1 <span class="function">fbsql\_field\_type</span> example**

``` php
<?php

fbsql_connect("localhost", "_SYSTEM", "");
fbsql_select_db("wisconsin");
$result = fbsql_query("SELECT * FROM onek;");
$fields = fbsql_num_fields($result);
$rows   = fbsql_num_rows($result);
$i = 0;
$table = fbsql_field_table($result, $i);
echo "Your '" . $table . "' table has " . $fields . " fields and " . $rows . " records <br />";
echo "The table has the following fields <br />";
while ($i < $fields) {
    $type  = fbsql_field_type($result, $i);
    $name  = fbsql_field_name($result, $i);
    $len   = fbsql_field_len($result, $i);
    $flags = fbsql_field_flags($result, $i);
    echo $type . " " . $name . " " . $len . " " . $flags . "<br />";
    $i++;
}
fbsql_close();

?>
```

### 参见

-   <span class="function">fbsql\_field\_name</span>

fbsql\_free\_result
===================

Free result memory

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Frees all memory associated with the given `result` identifier.

<span class="function">fbsql\_free\_result</span> only needs to be
called if you are concerned about how much memory is being used for
queries that return large result sets. All associated result memory is
automatically freed at the end of the script's execution.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

fbsql\_get\_autostart\_info
===========================

### 说明

<span class="type">array</span> <span
class="methodname">fbsql\_get\_autostart\_info</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

fbsql\_hostname
===============

Get or set the host name used with a connection

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_hostname</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$host_name`</span> \] )

Gets or sets the host name used with a connection.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`host_name`  
If provided, this will be the new connection host name.

### 返回值

Returns the current host name used for the connection.

### 参见

-   <span class="function">fbsql\_username</span>
-   <span class="function">fbsql\_password</span>

fbsql\_insert\_id
=================

Get the id generated from the previous INSERT operation

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_insert\_id</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Gets the id generated from the previous INSERT operation which created a
DEFAULT UNIQUE value.

> **Note**:
>
> The value of the FrontBase SQL function <span
> class="function">fbsql\_insert\_id</span> always contains the most
> recently generated DEFAULT UNIQUE value, and is not reset between
> queries.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns the ID generated from the previous INSERT query, or 0 if the
previous query does not generate an DEFAULT UNIQUE value.

If you need to save the value for later, be sure to call this function
immediately after the query that generates the value.

### 参见

-   <span class="function">fbsql\_affected\_rows</span>

fbsql\_list\_dbs
================

List databases available on a FrontBase server

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_list\_dbs</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Return a result pointer containing the databases available from the
current fbsql daemon. Use the <span
class="function">fbsql\_tablename</span> to traverse this result
pointer.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a result pointer or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">fbsql\_list\_dbs</span> example**

``` php
<?php
$link = fbsql_connect('localhost', 'myname', 'secret');
$db_list = fbsql_list_dbs($link);

while ($row = fbsql_fetch_object($db_list)) {
    echo $row->Database . "\n";
}
?>
```

以上例程的输出类似于：

    database1
    database2
    database3
    ...

> **Note**:
>
> The above code would just as easily work with <span
> class="function">fbsql\_fetch\_row</span> or other similar functions.

### 参见

-   <span class="function">fbsql\_list\_fields</span>
-   <span class="function">fbsql\_list\_tables</span>

fbsql\_list\_fields
===================

List FrontBase result fields

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_list\_fields</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> , <span class="methodparam"><span
class="type">string</span> `$table_name`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Retrieves information about the given table.

### 参数

`database_name`  
The database name.

`table_name`  
The table name.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a result pointer which can be used with the *fbsql\_field\_xxx*
functions, or **`FALSE`** on error.

### 错误／异常

A string describing the error will be placed in *$phperrmsg*, and unless
the function was called as *@fbsql()* then this error string will also
be printed out.

### 范例

**示例 \#1 <span class="function">fbsql\_list\_fields</span> example**

``` php
<?php
$link = fbsql_connect('localhost', 'myname', 'secret');

$fields = fbsql_list_fields("database1", "table1", $link);
$columns = fbsql_num_fields($fields);

for ($i = 0; $i < $columns; $i++) {
    echo fbsql_field_name($fields, $i) . "\n";;
}
?>
```

以上例程的输出类似于：

    field1
    field2
    field3
    ...

### 参见

-   <span class="function">fbsql\_field\_len</span>
-   <span class="function">fbsql\_field\_name</span>
-   <span class="function">fbsql\_field\_type</span>
-   <span class="function">fbsql\_field\_flags</span>

fbsql\_list\_tables
===================

List tables in a FrontBase database

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_list\_tables</span> ( <span
class="methodparam"><span class="type">string</span> `$database`</span>
\[, <span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Returns a result pointer describing the `database`.

### 参数

`database`  
The database name.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a result pointer which can be used with the <span
class="function">fbsql\_tablename</span> function to read the actual
table names, or **`FALSE`** on error.

### 参见

-   <span class="function">fbsql\_list\_fields</span>
-   <span class="function">fbsql\_list\_dbs</span>

fbsql\_next\_result
===================

Move the internal result pointer to the next result

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

When sending more than one SQL statement to the server or executing a
stored procedure with multiple results will cause the server to return
multiple result sets. This function will test for additional results
available form the server. If an additional result set exists it will
free the existing result set and prepare to fetch the words from the new
result set.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns **`TRUE`** if an additional result set was available or
**`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">fbsql\_next\_result</span> example**

``` php
<?php
$link = fbsql_connect("localhost", "_SYSTEM", "secret");
fbsql_select_db("MyDB", $link);
$SQL = "Select * from table1; select * from table2;";
$rs = fbsql_query($SQL, $link);
do {
    while ($row = fbsql_fetch_row($rs)) {
    }
} while (fbsql_next_result($rs));
fbsql_free_result($rs);
fbsql_close($link);
?>
```

fbsql\_num\_fields
==================

Get number of fields in result

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Returns the number of fields in the given `result` set.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns the number of fields, as an integer.

### 参见

-   <span class="function">fbsql\_db\_query</span>
-   <span class="function">fbsql\_query</span>
-   <span class="function">fbsql\_fetch\_field</span>
-   <span class="function">fbsql\_num\_rows</span>

fbsql\_num\_rows
================

Get number of rows in result

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Gets the number of rows in the given `result` set.

This function is only valid for SELECT statements. To retrieve the
number of rows returned from a INSERT, UPDATE or DELETE query, use <span
class="function">fbsql\_affected\_rows</span>.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns the number of rows returned by the last SELECT statement.

### 范例

**示例 \#1 <span class="function">fbsql\_num\_rows</span> example**

``` php
<?php

$link = fbsql_connect("localhost", "username", "password");
fbsql_select_db("database", $link);

$result = fbsql_query("SELECT * FROM table1;", $link);
$num_rows = fbsql_num_rows($result);

echo "$num_rows Rows\n";

?>
```

### 参见

-   <span class="function">fbsql\_affected\_rows</span>
-   <span class="function">fbsql\_connect</span>
-   <span class="function">fbsql\_select\_db</span>
-   <span class="function">fbsql\_query</span>

fbsql\_password
===============

Get or set the user password used with a connection

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_password</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \] )

Get or set the user password used with a connection.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`password`  
If provided, this will be the new connection password.

### 返回值

Returns the current password used for the connection.

### 参见

-   <span class="function">fbsql\_username</span>
-   <span class="function">fbsql\_hostname</span>

fbsql\_pconnect
===============

Open a persistent connection to a FrontBase Server

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_pconnect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$hostname`<span
class="initializer"> = ini\_get("fbsql.default\_host")</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$username`<span class="initializer"> =
ini\_get("fbsql.default\_user")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = ini\_get("fbsql.default\_password")</span></span>
\]\]\] )

Establishes a persistent connection to a FrontBase server.

To set the server port number, use <span
class="function">fbsql\_select\_db</span>.

<span class="function">fbsql\_pconnect</span> acts very much like <span
class="function">fbsql\_connect</span> with two major differences:

First, when connecting, the function would first try to find a
(persistent) link that's already open with the same host, username and
password. If one is found, an identifier for it will be returned instead
of opening a new connection.

Second, the connection to the SQL server will not be closed when the
execution of the script ends. Instead, the link will remain open for
future use.

This type of links is therefore called 'persistent'.

### 参数

`hostname`  
The server host name.

`username`  
The user name for the connection.

`password`  
The password for the connection.

### 返回值

Returns a positive FrontBase persistent link identifier on success, or
**`FALSE`** on error.

### 参见

-   <span class="function">fbsql\_connect</span>

fbsql\_query
============

Send a FrontBase query

### 说明

<span class="type">resource</span> <span
class="methodname">fbsql\_query</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">int</span> `$batch_size`</span> \]\] )

Sends a `query` to the currently active database on the server.

If the query succeeds, you can call <span
class="function">fbsql\_num\_rows</span> to find out how many rows were
returned for a SELECT statement or <span
class="function">fbsql\_affected\_rows</span> to find out how many rows
were affected by a DELETE, INSERT, REPLACE, or UPDATE statement.

### 参数

`query`  
The SQL query to be executed.

> **Note**:
>
> The query string shall always end with a semicolon.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`batch_size`  

### 返回值

<span class="function">fbsql\_query</span> returns **`TRUE`** (non-zero)
or **`FALSE`** to indicate whether or not the query succeeded. A return
value of **`TRUE`** means that the query was legal and could be executed
by the server. It does not indicate anything about the number of rows
affected or returned. It is perfectly possible for a query to succeed
but affect no rows or return no rows.

For SELECT statements, <span class="function">fbsql\_query</span>
returns a new result identifier that you can pass to <span
class="function">fbsql\_result</span>.

<span class="function">fbsql\_query</span> will also fail and return
**`FALSE`** if you don't have permission to access the table(s)
referenced by the query.

### 范例

The following query is syntactically invalid, so <span
class="function">fbsql\_query</span> fails and returns **`FALSE`**:

**示例 \#1 <span class="function">fbsql\_query</span> example**

``` php
<?php
$result = fbsql_query("SELECT * WHERE 1=1")
    or die ("Invalid query");
?>
```

The following query is semantically invalid if *my\_col* is not a column
in the table *my\_tbl*, so <span class="function">fbsql\_query</span>
fails and returns **`FALSE`**:

**示例 \#2 <span class="function">fbsql\_query</span> example**

``` php
<?php
$result = fbsql_query ("SELECT my_col FROM my_tbl;")
    or die ("Invalid query");
?>
```

### 参见

-   <span class="function">fbsql\_affected\_rows</span>
-   <span class="function">fbsql\_db\_query</span>
-   <span class="function">fbsql\_free\_result</span>
-   <span class="function">fbsql\_result</span>
-   <span class="function">fbsql\_select\_db</span>
-   <span class="function">fbsql\_connect</span>

fbsql\_read\_blob
=================

Read a BLOB from the database

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_read\_blob</span> ( <span
class="methodparam"><span class="type">string</span>
`$blob_handle`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Reads BLOB data from the database.

If a select statement contains BLOB and/or CLOB columns FrontBase will
return the data directly when data is fetched. This default behavior can
be changed with <span class="function">fbsql\_set\_lob\_mode</span> so
the fetch functions will return handles to BLOB and CLOB data. If a
handle is fetched a user must call <span
class="function">fbsql\_read\_blob</span> to get the actual BLOB data
from the database.

### 参数

`blob_handle`  
A BLOB handle, returned by <span
class="function">fbsql\_create\_blob</span>.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a string containing the specified BLOB data.

### 范例

**示例 \#1 <span class="function">fbsql\_read\_blob</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
$sql = "SELECT BLOB_COLUMN FROM BLOB_TABLE;";
$rs = fbsql_query($sql, $link);
$row_data = fbsql_fetch_row($rs);
// $row_data[0] will now contain the blob data for the first row
fbsql_free_result($rs);

$rs = fbsql_query($sql, $link);
fbsql_set_lob_mode($rs, FBSQL_LOB_HANDLE);
$row_data = fbsql_fetch_row($rs);
// $row_data[0] will now contain a handle to the BLOB data in the first row
$blob_data = fbsql_read_blob($row_data[0]);
fbsql_free_result($rs);

?>
```

### 参见

-   <span class="function">fbsql\_create\_blob</span>
-   <span class="function">fbsql\_read\_clob</span>
-   <span class="function">fbsql\_set\_lob\_mode</span>

fbsql\_read\_clob
=================

Read a CLOB from the database

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_read\_clob</span> ( <span
class="methodparam"><span class="type">string</span>
`$clob_handle`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Reads CLOB data from the database.

If a select statement contains BLOB and/or CLOB columns FrontBase will
return the data directly when data is fetched. This default behavior can
be changed with <span class="function">fbsql\_set\_lob\_mode</span> so
the fetch functions will return handles to BLOB and CLOB data. If a
handle is fetched a user must call <span
class="function">fbsql\_read\_clob</span> to get the actual CLOB data
from the database.

### 参数

`clob_handle`  
A CLOB handle, returned by <span
class="function">fbsql\_create\_clob</span>.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

Returns a string containing the specified CLOB data.

### 范例

**示例 \#1 <span class="function">fbsql\_read\_clob</span> example**

``` php
<?php
$link = fbsql_pconnect("localhost", "_SYSTEM", "secret")
    or die("Could not connect");
$sql = "SELECT CLOB_COLUMN FROM CLOB_TABLE;";
$rs = fbsql_query($sql, $link);
$row_data = fbsql_fetch_row($rs);
// $row_data[0] will now contain the clob data for the first row
fbsql_free_result($rs);

$rs = fbsql_query($sql, $link);
fbsql_set_lob_mode($rs, FBSQL_LOB_HANDLE);
$row_data = fbsql_fetch_row($rs);
// $row_data[0] will now contain a handle to the CLOB data in the first row
$clob_data = fbsql_read_clob($row_data[0]);
fbsql_free_result($rs);

?>
```

### 参见

-   <span class="function">fbsql\_create\_clob</span>
-   <span class="function">fbsql\_read\_blob</span>
-   <span class="function">fbsql\_set\_lob\_mode</span>

fbsql\_result
=============

Get result data

### 说明

<span class="type">mixed</span> <span
class="methodname">fbsql\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$field`</span> \]\] )

Returns the contents of one cell from a FrontBase `result` set.

When working on large result sets, you should consider using one of the
functions that fetch an entire row (specified below). As these functions
return the contents of multiple cells in one function call, they're MUCH
quicker than <span class="function">fbsql\_result</span>.

Calls to <span class="function">fbsql\_result</span> should not be mixed
with calls to other functions that deal with the result set.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`row`  

`field`  
Can be the field's offset, or the field's name, or the field's table dot
field's name (tablename.fieldname).

If the column name has been aliased ('select foo as bar from...'), use
the alias instead of the column name.

> **Note**:
>
> Specifying a numeric offset for the field argument is much quicker
> than specifying a fieldname or tablename.fieldname argument.

### 返回值

### 参见

Recommended high-performance alternatives:

-   <span class="function">fbsql\_fetch\_row</span>
-   <span class="function">fbsql\_fetch\_array</span>
-   <span class="function">fbsql\_fetch\_assoc</span>
-   <span class="function">fbsql\_fetch\_object</span>

fbsql\_rollback
===============

Rollback a transaction to the database

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_rollback</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Ends the current transaction by rolling back all statements issued since
last commit.

This command is only needed if autocommit is set to false.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_autocommit</span>
-   <span class="function">fbsql\_commit</span>

fbsql\_rows\_fetched
====================

Get the number of rows affected by the last statement

### 说明

<span class="type">int</span> <span
class="methodname">fbsql\_rows\_fetched</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Gets the number of rows affected by the last statement.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

### 返回值

Returns the number of rows, as an integer.

fbsql\_select\_db
=================

Select a FrontBase database

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_select\_db</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \]\] )

Sets the current active database on the given link identifier.

The client contacts FBExec to obtain the port number to use for the
connection to the database. If the database name is a number the system
will use that as a port number and it will not ask FBExec for the port
number. The FrontBase server can be stared as FRontBase -FBExec=No
-port=\<port number\> \<database name\>.

Every subsequent call to <span class="function">fbsql\_query</span> will
be made on the active database.

### 参数

`database_name`  
The name of the database to be selected.

If the database is protected with a database password, the you must call
<span class="function">fbsql\_database\_password</span> before selecting
the database.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_connect</span>
-   <span class="function">fbsql\_pconnect</span>
-   <span class="function">fbsql\_database\_password</span>
-   <span class="function">fbsql\_query</span>

fbsql\_set\_characterset
========================

Change input/output character set

### 说明

<span class="type">void</span> <span
class="methodname">fbsql\_set\_characterset</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$characterset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$in_out_both`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

fbsql\_set\_lob\_mode
=====================

Set the LOB retrieve mode for a FrontBase result set

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_set\_lob\_mode</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$lob_mode`</span> )

Sets the mode for retrieving LOB data from the database.

When BLOB and CLOB data is retrieved in FrontBase it can be retrieved
direct or indirect. Direct retrieved LOB data will always be fetched no
matter the setting of the lob mode. If the LOB data is less than 512
bytes it will always be retrieved directly.

### 参数

` result`  
由 <span class="function">fbsql\_query</span> 或 <span
class="function">fbsql\_db\_query</span> 返回的结果标识符。

`lob_mode`  
Can be one of:

-   <span class="simpara"> **`FBSQL_LOB_DIRECT`** - LOB data is
    retrieved directly. When data is fetched from the database with
    <span class="function">fbsql\_fetch\_row</span>, and other fetch
    functions, all CLOB and BLOB columns will be returned as ordinary
    columns. This is the default value on a new FrontBase result.
    </span>
-   <span class="simpara"> **`FBSQL_LOB_HANDLE`** - LOB data is
    retrieved as handles to the data. When data is fetched from the
    database with <span class="function">fbsql\_fetch\_row</span>, and
    other fetch functions, LOB data will be returned as a handle to the
    data if the data is stored indirect or the data if it is stored
    direct. If a handle is returned it will be a 27 byte string
    formatted as *@'000000000000000000000000'*. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_create\_blob</span>
-   <span class="function">fbsql\_create\_clob</span>
-   <span class="function">fbsql\_read\_blob</span>
-   <span class="function">fbsql\_read\_clob</span>

fbsql\_set\_password
====================

Change the password for a given user

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_set\_password</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$user`</span> , <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">string</span>
`$old_password`</span> )

Changes the password for the given `user`.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`user`  
The user name.

`password`  
The new password to be set.

`old_password`  
The old password to be replaced.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

fbsql\_set\_transaction
=======================

Set the transaction locking and isolation

### 说明

<span class="type">void</span> <span
class="methodname">fbsql\_set\_transaction</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$locking`</span> , <span
class="methodparam"><span class="type">int</span> `$isolation`</span> )

Sets the transaction `locking` and `isolation`.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`locking`  
The type of locking to be set. It can be one of the following constants:
**`FBSQL_LOCK_DEFERRED`**, **`FBSQL_LOCK_OPTIMISTIC`**, or
**`FBSQL_LOCK_PESSIMISTIC`**.

`isolation`  
The type of isolation to be set. It can be one of the following
constants: **`FBSQL_ISO_READ_UNCOMMITTED`**,
**`FBSQL_ISO_READ_COMMITTED`**, **`FBSQL_ISO_REPEATABLE_READ`**,
**`FBSQL_ISO_SERIALIZABLE`**, or **`FBSQL_ISO_VERSIONED`**.

### 返回值

没有返回值。

fbsql\_start\_db
================

Start a database on local or remote server

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_start\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$database_options`</span> \]\] )

Start a database on local or remote server.

### 参数

`database_name`  
The database name.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`database_options`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_db\_status</span>
-   <span class="function">fbsql\_stop\_db</span>

fbsql\_stop\_db
===============

Stop a database on local or remote server

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_stop\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

Stops a database on local or remote server.

### 参数

`database_name`  
The database name.

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fbsql\_db\_status</span>
-   <span class="function">fbsql\_start\_db</span>

fbsql\_table\_name
==================

Get table name of field

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_table\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

<span class="function">fbsql\_table\_name</span> gets the name of the
current table in the given `result` set.

The <span class="function">fbsql\_num\_rows</span> function may be used
to determine the number of tables in the result pointer.

### 参数

`result`  
A result pointer returned by <span
class="function">fbsql\_list\_tables</span>.

`index`  
Integer index for the current table.

### 返回值

Returns the name of the table, as a string.

### 范例

**示例 \#1 <span class="function">fbsql\_table\_name</span> example**

``` php
<?php
fbsql_connect("localhost", "_SYSTEM", "");
$result = fbsql_list_tables("wisconsin");
$i = 0;
while ($i < fbsql_num_rows($result)) {
    $tb_names[$i] = fbsql_table_name($result, $i);
    echo $tb_names[$i] . "<br />";
    $i++;
}
?>
```

fbsql\_tablename
================

别名 <span class="function">fbsql\_table\_name</span>

### 说明

此函数是该函数的别名： <span class="function">fbsql\_table\_name</span>.

fbsql\_username
===============

Get or set the username for the connection

### 说明

<span class="type">string</span> <span
class="methodname">fbsql\_username</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$username`</span> \] )

Get or set the username used for the connection.

### 参数

` link_identifier`  
由 <span class="function">fbsql\_connect</span> 或 <span
class="function">fbsql\_pconnect</span> 返回的 FrontBase 链接标识符.

如可选并未指定，函数会尝试查找一个到 FrontBase
服务器的开放链接，且如没有找到这样的链接，会尝试通过不带参数调用 <span
class="function">fbsql\_connect</span> 来创建一个。

`username`  
If provided, this is the new username to set.

### 返回值

Returns the current username used with the connection, as a string.

### 参见

-   <span class="function">fbsql\_password</span>
-   <span class="function">fbsql\_hostname</span>

fbsql\_warnings
===============

Enable or disable FrontBase warnings

### 说明

<span class="type">bool</span> <span
class="methodname">fbsql\_warnings</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$OnOff`</span> \] )

Enables or disables FrontBase warnings.

### 参数

`OnOff`  
Whether to enable warnings or no.

### 返回值

Returns **`TRUE`** if warnings is turned on, **`FALSE`** otherwise.

### 参见

-   <span class="function">fbsql\_errno</span>
-   <span class="function">fbsql\_error</span>

**目录**

-   [fbsql\_affected\_rows](/book/fbsql.html#fbsql_affected_rows) — Get
    number of affected rows in previous FrontBase operation
-   [fbsql\_autocommit](/book/fbsql.html#fbsql_autocommit) — Enable or
    disable autocommit
-   [fbsql\_blob\_size](/book/fbsql.html#fbsql_blob_size) — Get the size
    of a BLOB
-   [fbsql\_change\_user](/book/fbsql.html#fbsql_change_user) — Change
    logged in user of the active connection
-   [fbsql\_clob\_size](/book/fbsql.html#fbsql_clob_size) — Get the size
    of a CLOB
-   [fbsql\_close](/book/fbsql.html#fbsql_close) — Close FrontBase
    connection
-   [fbsql\_commit](/book/fbsql.html#fbsql_commit) — Commits a
    transaction to the database
-   [fbsql\_connect](/book/fbsql.html#fbsql_connect) — Open a connection
    to a FrontBase Server
-   [fbsql\_create\_blob](/book/fbsql.html#fbsql_create_blob) — Create a
    BLOB
-   [fbsql\_create\_clob](/book/fbsql.html#fbsql_create_clob) — Create a
    CLOB
-   [fbsql\_create\_db](/book/fbsql.html#fbsql_create_db) — Create a
    FrontBase database
-   [fbsql\_data\_seek](/book/fbsql.html#fbsql_data_seek) — Move
    internal result pointer
-   [fbsql\_database\_password](/book/fbsql.html#fbsql_database_password)
    — Sets or retrieves the password for a FrontBase database
-   [fbsql\_database](/book/fbsql.html#fbsql_database) — Get or set the
    database name used with a connection
-   [fbsql\_db\_query](/book/fbsql.html#fbsql_db_query) — Send a
    FrontBase query
-   [fbsql\_db\_status](/book/fbsql.html#fbsql_db_status) — Get the
    status for a given database
-   [fbsql\_drop\_db](/book/fbsql.html#fbsql_drop_db) — Drop (delete) a
    FrontBase database
-   [fbsql\_errno](/book/fbsql.html#fbsql_errno) — Returns the error
    number from previous operation
-   [fbsql\_error](/book/fbsql.html#fbsql_error) — Returns the error
    message from previous operation
-   [fbsql\_fetch\_array](/book/fbsql.html#fbsql_fetch_array) — Fetch a
    result row as an associative array, a numeric array, or both
-   [fbsql\_fetch\_assoc](/book/fbsql.html#fbsql_fetch_assoc) — Fetch a
    result row as an associative array
-   [fbsql\_fetch\_field](/book/fbsql.html#fbsql_fetch_field) — Get
    column information from a result and return as an object
-   [fbsql\_fetch\_lengths](/book/fbsql.html#fbsql_fetch_lengths) — Get
    the length of each output in a result
-   [fbsql\_fetch\_object](/book/fbsql.html#fbsql_fetch_object) — Fetch
    a result row as an object
-   [fbsql\_fetch\_row](/book/fbsql.html#fbsql_fetch_row) — Get a result
    row as an enumerated array
-   [fbsql\_field\_flags](/book/fbsql.html#fbsql_field_flags) — Get the
    flags associated with the specified field in a result
-   [fbsql\_field\_len](/book/fbsql.html#fbsql_field_len) — Returns the
    length of the specified field
-   [fbsql\_field\_name](/book/fbsql.html#fbsql_field_name) — Get the
    name of the specified field in a result
-   [fbsql\_field\_seek](/book/fbsql.html#fbsql_field_seek) — Set result
    pointer to a specified field offset
-   [fbsql\_field\_table](/book/fbsql.html#fbsql_field_table) — Get name
    of the table the specified field is in
-   [fbsql\_field\_type](/book/fbsql.html#fbsql_field_type) — Get the
    type of the specified field in a result
-   [fbsql\_free\_result](/book/fbsql.html#fbsql_free_result) — Free
    result memory
-   [fbsql\_get\_autostart\_info](/book/fbsql.html#fbsql_get_autostart_info)
    — 说明
-   [fbsql\_hostname](/book/fbsql.html#fbsql_hostname) — Get or set the
    host name used with a connection
-   [fbsql\_insert\_id](/book/fbsql.html#fbsql_insert_id) — Get the id
    generated from the previous INSERT operation
-   [fbsql\_list\_dbs](/book/fbsql.html#fbsql_list_dbs) — List databases
    available on a FrontBase server
-   [fbsql\_list\_fields](/book/fbsql.html#fbsql_list_fields) — List
    FrontBase result fields
-   [fbsql\_list\_tables](/book/fbsql.html#fbsql_list_tables) — List
    tables in a FrontBase database
-   [fbsql\_next\_result](/book/fbsql.html#fbsql_next_result) — Move the
    internal result pointer to the next result
-   [fbsql\_num\_fields](/book/fbsql.html#fbsql_num_fields) — Get number
    of fields in result
-   [fbsql\_num\_rows](/book/fbsql.html#fbsql_num_rows) — Get number of
    rows in result
-   [fbsql\_password](/book/fbsql.html#fbsql_password) — Get or set the
    user password used with a connection
-   [fbsql\_pconnect](/book/fbsql.html#fbsql_pconnect) — Open a
    persistent connection to a FrontBase Server
-   [fbsql\_query](/book/fbsql.html#fbsql_query) — Send a FrontBase
    query
-   [fbsql\_read\_blob](/book/fbsql.html#fbsql_read_blob) — Read a BLOB
    from the database
-   [fbsql\_read\_clob](/book/fbsql.html#fbsql_read_clob) — Read a CLOB
    from the database
-   [fbsql\_result](/book/fbsql.html#fbsql_result) — Get result data
-   [fbsql\_rollback](/book/fbsql.html#fbsql_rollback) — Rollback a
    transaction to the database
-   [fbsql\_rows\_fetched](/book/fbsql.html#fbsql_rows_fetched) — Get
    the number of rows affected by the last statement
-   [fbsql\_select\_db](/book/fbsql.html#fbsql_select_db) — Select a
    FrontBase database
-   [fbsql\_set\_characterset](/book/fbsql.html#fbsql_set_characterset)
    — Change input/output character set
-   [fbsql\_set\_lob\_mode](/book/fbsql.html#fbsql_set_lob_mode) — Set
    the LOB retrieve mode for a FrontBase result set
-   [fbsql\_set\_password](/book/fbsql.html#fbsql_set_password) — Change
    the password for a given user
-   [fbsql\_set\_transaction](/book/fbsql.html#fbsql_set_transaction) —
    Set the transaction locking and isolation
-   [fbsql\_start\_db](/book/fbsql.html#fbsql_start_db) — Start a
    database on local or remote server
-   [fbsql\_stop\_db](/book/fbsql.html#fbsql_stop_db) — Stop a database
    on local or remote server
-   [fbsql\_table\_name](/book/fbsql.html#fbsql_table_name) — Get table
    name of field
-   [fbsql\_tablename](/book/fbsql.html#fbsql_tablename) — 别名
    fbsql\_table\_name
-   [fbsql\_username](/book/fbsql.html#fbsql_username) — Get or set the
    username for the connection
-   [fbsql\_warnings](/book/fbsql.html#fbsql_warnings) — Enable or
    disable FrontBase warnings
