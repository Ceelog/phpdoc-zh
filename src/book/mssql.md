Microsoft SQL Server
====================

**目录**

-   [简介](/book/mssql.html#简介)
-   [安装／配置](/book/mssql.html#安装／配置)
    -   [需求](/book/mssql.html#需求)
    -   [安装](/book/mssql.html#安装)
    -   [运行时配置](/book/mssql.html#运行时配置)
    -   [资源类型](/book/mssql.html#资源类型)
-   [预定义常量](/book/mssql.html#预定义常量)
-   [Mssql 函数](/book/mssql.html#Mssql%20函数)
    -   [mssql\_bind](/book/mssql.html#mssql_bind) — Adds a parameter to
        a stored procedure or a remote stored procedure
    -   [mssql\_close](/book/mssql.html#mssql_close) — 关闭MS SQL
        Server链接
    -   [mssql\_connect](/book/mssql.html#mssql_connect) — 打开MS SQL
        server链接
    -   [mssql\_data\_seek](/book/mssql.html#mssql_data_seek) — Moves
        internal row pointer
    -   [mssql\_execute](/book/mssql.html#mssql_execute) — Executes a
        stored procedure on a MS SQL server database
    -   [mssql\_fetch\_array](/book/mssql.html#mssql_fetch_array) —
        Fetch a result row as an associative array, a numeric array, or
        both
    -   [mssql\_fetch\_assoc](/book/mssql.html#mssql_fetch_assoc) —
        Returns an associative array of the current row in the result
    -   [mssql\_fetch\_batch](/book/mssql.html#mssql_fetch_batch) —
        Returns the next batch of records
    -   [mssql\_fetch\_field](/book/mssql.html#mssql_fetch_field) — Get
        field information
    -   [mssql\_fetch\_object](/book/mssql.html#mssql_fetch_object) —
        Fetch row as object
    -   [mssql\_fetch\_row](/book/mssql.html#mssql_fetch_row) — Get row
        as enumerated array
    -   [mssql\_field\_length](/book/mssql.html#mssql_field_length) —
        Get the length of a field
    -   [mssql\_field\_name](/book/mssql.html#mssql_field_name) — Get
        the name of a field
    -   [mssql\_field\_seek](/book/mssql.html#mssql_field_seek) — Seeks
        to the specified field offset
    -   [mssql\_field\_type](/book/mssql.html#mssql_field_type) — Gets
        the type of a field
    -   [mssql\_free\_result](/book/mssql.html#mssql_free_result) — Free
        result memory
    -   [mssql\_free\_statement](/book/mssql.html#mssql_free_statement)
        — Free statement memory
    -   [mssql\_get\_last\_message](/book/mssql.html#mssql_get_last_message)
        — Returns the last message from the server
    -   [mssql\_guid\_string](/book/mssql.html#mssql_guid_string) —
        Converts a 16 byte binary GUID to a string
    -   [mssql\_init](/book/mssql.html#mssql_init) — Initializes a
        stored procedure or a remote stored procedure
    -   [mssql\_min\_error\_severity](/book/mssql.html#mssql_min_error_severity)
        — Sets the minimum error severity
    -   [mssql\_min\_message\_severity](/book/mssql.html#mssql_min_message_severity)
        — Sets the minimum message severity
    -   [mssql\_next\_result](/book/mssql.html#mssql_next_result) — Move
        the internal result pointer to the next result
    -   [mssql\_num\_fields](/book/mssql.html#mssql_num_fields) — Gets
        the number of fields in result
    -   [mssql\_num\_rows](/book/mssql.html#mssql_num_rows) — Gets the
        number of rows in result
    -   [mssql\_pconnect](/book/mssql.html#mssql_pconnect) — Open
        persistent MS SQL connection
    -   [mssql\_query](/book/mssql.html#mssql_query) — Send MS SQL query
    -   [mssql\_result](/book/mssql.html#mssql_result) — Get result data
    -   [mssql\_rows\_affected](/book/mssql.html#mssql_rows_affected) —
        Returns the number of records affected by the query
    -   [mssql\_select\_db](/book/mssql.html#mssql_select_db) — Select
        MS SQL database

**Warning**

This feature was *REMOVED* in PHP 7.0.0.

Alternatives to this feature include:

-   <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_SQLSRV</a>
-   <a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>
-   <a href="/book/sqlsrv.html" class="link">SQLSRV</a>
-   <a href="/book/uodbc.html" class="link">Unified ODBC API</a>

These functions allow you to access MS SQL Server database.

This extension is not available anymore on Windows with PHP 5.3 or
later.

SQLSRV, an alternative extension for MS SQL connectivity is available
from Microsoft:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx</a>.

安装／配置
==========

**目录**

-   [需求](/book/mssql.html#需求)
-   [安装](/book/mssql.html#安装)
-   [运行时配置](/book/mssql.html#运行时配置)
-   [资源类型](/book/mssql.html#资源类型)

需求
----

Requirements for Win32 platforms.

The extension requires the MS SQL Client Tools to be installed on the
system where PHP is installed. The Client Tools can be installed from
the MS SQL Server CD or by copying `ntwdblib.dll` from `\winnt\system32`
on the server to `\winnt\system32` on the PHP box. Copying
`ntwdblib.dll` will only provide access through named pipes.
Configuration of the client will require installation of all the tools.

This extension is not available anymore on Windows with PHP 5.3 or
later.

SqlSrv, an alternative driver for MS SQL is available from Microsoft:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx</a>.

Requirements for Unix/Linux platforms.

To use the MSSQL extension on Unix/Linux, you first need to build and
install the FreeTDS library. Source code and installation instructions
are available at the FreeTDS home page:
<a href="http://www.freetds.org/" class="link external">» http://www.freetds.org/</a>

> **Note**:
>
> On Windows, the DBLIB from Microsoft is used. Functions that return a
> column name are based on the *dbcolname()* function in DBLIB. DBLIB
> was developed for SQL Server 6.x where the max identifier length is
> 30. For this reason, the maximum column length is 30 characters. On
> platforms where FreeTDS is used (Linux), this is not a problem.

> **Note**:
>
> On Windows, if you're using MSSQL 2005 or greater you must copy the
> *ntwdblib.dll* into the directory where you have installed php and
> overwrite the one thats already in there. This is due to the version
> distributed is old and outdated. Alternatively you can use the
> <a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx</a>,
> <a href="/book/uodbc.html" class="link">ODBC</a>,
> <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_DBLIB</a>
> or
> <a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>
> extensions, to talk to MSSQL.

安装
----

The MSSQL extension is enabled by adding extension=php\_mssql.dll to
`php.ini`.

To get these functions to work, you have to compile PHP with
**--with-mssql\[=DIR\]**, where DIR is the FreeTDS install prefix. And
FreeTDS should be compiled using **--enable-msdblib**.

**Warning**

MS SQL functions are aliases to Sybase functions if PHP is compiled with
<a href="/book/sybase.html" class="link">Sybase</a> extension and
without MS SQL extension.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                         | 默认 | 可修改范围       | 更新日志                                                          |
|------------------------------|------|------------------|-------------------------------------------------------------------|
| mssql.allow\_persistent      | "1"  | PHP\_INI\_SYSTEM |                                                                   |
| mssql.max\_persistent        | "-1" | PHP\_INI\_SYSTEM |                                                                   |
| mssql.max\_links             | "-1" | PHP\_INI\_SYSTEM |                                                                   |
| mssql.min\_error\_severity   | "10" | PHP\_INI\_ALL    |                                                                   |
| mssql.min\_message\_severity | "10" | PHP\_INI\_ALL    |                                                                   |
| mssql.compatibility\_mode    | "0"  | PHP\_INI\_ALL    |                                                                   |
| mssql.connect\_timeout       | "5"  | PHP\_INI\_ALL    |                                                                   |
| mssql.timeout                | "60" | PHP\_INI\_ALL    | Available since PHP 4.1.0.                                        |
| mssql.textsize               | "-1" | PHP\_INI\_ALL    |                                                                   |
| mssql.textlimit              | "-1" | PHP\_INI\_ALL    |                                                                   |
| mssql.batchsize              | "0"  | PHP\_INI\_ALL    | Available since PHP 4.0.4.                                        |
| mssql.datetimeconvert        | "1"  | PHP\_INI\_ALL    | Available since PHP 4.2.0.                                        |
| mssql.secure\_connection     | "0"  | PHP\_INI\_SYSTEM | Available since PHP 4.3.0.                                        |
| mssql.max\_procs             | "-1" | PHP\_INI\_ALL    | Available since PHP 4.3.0.                                        |
| mssql.charset                | ""   | PHP\_INI\_ALL    | Available since PHP 5.1.2 when built with FreeTDS 7.0 or greater. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

资源类型
--------

mssql link
----------

A connection link returned by <span
class="function">mssql\_connect</span> and <span
class="function">mssql\_pconnect</span>.

mssql result
------------

A result handle returned by <span class="function">mssql\_query</span>
on *SELECT* queries.

mssql statement
---------------

A statement handle returned by <span
class="function">mssql\_init</span>.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`MSSQL_ASSOC`** (<span class="type">integer</span>)  
<span class="simpara"> Return an associative array. Used on <span
class="function">mssql\_fetch\_array</span>'s *result\_type* parameter.
</span>

**`MSSQL_NUM`** (<span class="type">integer</span>)  
<span class="simpara"> Return an array with numeric keys. Used on <span
class="function">mssql\_fetch\_array</span>'s *result\_type* parameter.
</span>

**`MSSQL_BOTH`** (<span class="type">integer</span>)  
<span class="simpara"> Return an array with both numeric keys and keys
with their field name. This is the default value for <span
class="function">mssql\_fetch\_array</span>'s *result\_type* parameter.
</span>

**`SQLTEXT`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates the '*TEXT*' type in MSSQL, used by
<span class="function">mssql\_bind</span>'s *type* parameter. </span>

**`SQLVARCHAR`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates the '*VARCHAR*' type in MSSQL, used by
<span class="function">mssql\_bind</span>'s *type* parameter. </span>

**`SQLCHAR`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates the '*CHAR*' type in MSSQL, used by
<span class="function">mssql\_bind</span>'s *type* parameter. </span>

**`SQLINT1`** (<span class="type">integer</span>)  
<span class="simpara"> Represents one byte, with a range of -128 to 127.
</span>

**`SQLINT2`** (<span class="type">integer</span>)  
<span class="simpara"> Represents two bytes, with a range of -32768 to
32767. </span>

**`SQLINT4`** (<span class="type">integer</span>)  
<span class="simpara"> Represents four bytes, with a range of
-2147483648 to 2147483647. </span>

**`SQLBIT`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates the '*BIT*' type in MSSQL, used by
<span class="function">mssql\_bind</span>'s *type* parameter. </span>

**`SQLFLT4`** (<span class="type">integer</span>)  
<span class="simpara"> Represents an four byte float. </span>

**`SQLFLT8`** (<span class="type">integer</span>)  
<span class="simpara"> Represents an eight byte float. </span>

mssql\_bind
===========

Adds a parameter to a stored procedure or a remote stored procedure

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::bindParam</span>
-   <span class="function">PDOStatement::bindValue</span>
-   <span class="function">sqlsrv\_prepare</span>
-   <span class="function">odbc\_prepare</span>

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_bind</span> ( <span class="methodparam"><span
class="type">resource</span> `$stmt`</span> , <span
class="methodparam"><span class="type">string</span>
`$param_name`</span> , <span class="methodparam"><span
class="type">mixed</span> `&$var`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$is_output`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span> `$is_null`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$maxlen`<span
class="initializer"> = -1</span></span> \]\]\] )

Binds a parameter to a stored procedure or a remote stored procedure.

### 参数

`stmt`  
Statement resource, obtained with <span
class="function">mssql\_init</span>.

`param_name`  
The parameter name, as a string.

> **Note**:
>
> You have to include the *@* character, like in the T-SQL syntax. See
> the explanation included in <span
> class="function">mssql\_execute</span>.

`var`  
The PHP variable you'll bind the MSSQL parameter to. It is passed by
reference, to retrieve OUTPUT and RETVAL values after the procedure
execution.

`type`  
One of: **`SQLTEXT`**, **`SQLVARCHAR`**, **`SQLCHAR`**, **`SQLINT1`**,
**`SQLINT2`**, **`SQLINT4`**, **`SQLBIT`**, **`SQLFLT4`**,
**`SQLFLT8`**, **`SQLFLTN`**.

`is_output`  
Whether the value is an OUTPUT parameter or not. If it's an OUTPUT
parameter and you don't mention it, it will be treated as a normal input
parameter and no error will be thrown.

`is_null`  
Whether the parameter is **`NULL`** or not. Passing the **`NULL`** value
as `var` will not do the job.

`maxlen`  
Used with char/varchar values. You have to indicate the length of the
data so if the parameter is a varchar(50), the type must be
**`SQLVARCHAR`** and this value *50*.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mssql\_bind</span> example**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Create a new stored prodecure
$stmt = mssql_init('NewUserRecord');

// Bind the field names
mssql_bind($stmt, '@username',  'Kalle',  SQLVARCHAR,  false,  false,  60);
mssql_bind($stmt, '@name',      'Kalle',  SQLVARCHAR,  false,  false,  60);
mssql_bind($stmt, '@age',       19,       SQLINT1,     false,  false,   3);

// Execute
mssql_execute($stmt);

// Free statement
mssql_free_statement($stmt);
?>
```

### 参见

-   <span class="function">mssql\_execute</span>
-   <span class="function">mssql\_free\_statement</span>
-   <span class="function">mssql\_init</span>

mssql\_close
============

关闭MS SQL Server链接

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

关闭指定的链接标识符相关联的MS SQL
Server数据库链接。如果链接不存在，则试图关闭最后产生的链接。

注：这个操作通常不是必要的，在非持久打开的链接在程序执行结束后会自动关闭链接。

### 参数

`link_identifier`  
一个SQL Server链接, <span class="function">mssql\_connect</span>
的返回值。

这个方法不能关闭由<span class="function">mssql\_pconnect</span>
产生的长链接。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mssql\_close</span> 例子**

``` php
<?php
// Connect to MSSQL
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');

// Do any related operations here

// Close the link to MSSQL
mssql_close($link);
?>
```

### 参见

-   <span class="function">mssql\_connect</span>
-   <span class="function">mssql\_pconnect</span>

mssql\_connect
==============

打开MS SQL server链接

### 说明

<span class="type">resource</span> <span
class="methodname">mssql\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$servername`</span> \[, <span class="methodparam"><span
class="type">string</span> `$username`</span> \[, <span
class="methodparam"><span class="type">string</span> `$password`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$new_link`<span class="initializer"> = false</span></span> \]\]\]\] )

<span class="function">mssql\_connect</span> 建立一个MS SQL server链接。

链接会在程序执行结束之后关闭, 除非在之前已经通过调用<span
class="function">mssql\_close</span>关闭。

### 参数

`servername`  
服务器,它可以包含一个端口号 e.g. *主机:端口号(hostname:port)* (Linux),
或 *主机,端口号(hostname,port)* (Windows).

`username`  
用户名。

`password`  
密码。

`new_link`  
如果第二次调用<span
class="function">mssql\_connect</span>使用相同的参数，
不会建立新的链接，而是将之前已经打开的链接标识返回。对这个参数的值进行修改，则使得调用
<span class="function">mssql\_connect</span>总是会建立新的链接，
即便调用<span
class="function">mssql\_connect</span>使用与之前同样的参数。

### 返回值

返回一个链接视为成功, 或者 **`FALSE`** 和错误信息.

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 5.1.0 | `new_link`参数加入 |

### 范例

**示例 \#1 <span class="function">mssql\_connect</span> 例子**

``` php
<?php
// Server in the this format: <computer>\<instance name> or 
// <server>,<port> when using a non default port number
$server = 'KALLESPC\SQLEXPRESS';

// Connect to MSSQL
$link = mssql_connect($server, 'sa', 'phpfi');

if (!$link) {
    die('Something went wrong while connecting to MSSQL');
}
?>
```

### 参见

-   <span class="function">mssql\_close</span>
-   <span class="function">mssql\_pconnect</span>

mssql\_data\_seek
=================

Moves internal row pointer

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   Using an *OFFSET* clause with a query issued through
    <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_SQLSRV</a>,
    <a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>,
    <a href="/book/sqlsrv.html" class="link">SQLSRV</a>, or the
    <a href="/book/uodbc.html" class="link">unified ODBC driver</a>.

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span>
`$result_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$row_number`</span> )

<span class="function">mssql\_data\_seek</span> moves the internal row
pointer of the MS SQL result associated with the specified result
identifier to point to the specified row number, first row being number
0. The next call to <span class="function">mssql\_fetch\_row</span>
would return that row.

### 参数

`result_identifier`  
The result resource that is being evaluated.

`row_number`  
The desired row number of the new result pointer.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mssql\_data\_seek</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link);

// Select all people
$result = mssql_query('SELECT [name], [age] FROM [persons] WHERE [age] >= 13');

if (!$result) {
    die('Query failed.');
}

// Select every 4th student in the results
for ($i = mssql_num_rows($result) - 1; $i % 4; $i++) {
    if (!mssql_data_seek($result, $i)) {
        continue;
    }

    // Fetch the row ...
}

// Free the query result
mssql_free_result($result);
?>
```

mssql\_execute
==============

Executes a stored procedure on a MS SQL server database

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   Using an *EXEC* query issued through
    <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_SQLSRV</a>,
    <a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>,
    <a href="/book/sqlsrv.html" class="link">SQLSRV</a>, or the
    <a href="/book/uodbc.html" class="link">unified ODBC driver</a>.

### 说明

<span class="type">mixed</span> <span
class="methodname">mssql\_execute</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$skip_results`<span class="initializer"> = **`FALSE`**</span></span> \]
)

Executes a stored procedure on a MS SQL server database

### 参数

`stmt`  
Statement handle obtained with <span
class="function">mssql\_init</span>.

`skip_results`  
Whenever to skip the results or not.

### 范例

**示例 \#1 <span class="function">mssql\_execute</span> example**

``` php
<?php
// Create a new statement
$stmt = mssql_init('NewBlogEntry');

// Some data strings
$title = 'Test of blogging system';
$content = 'If you can read this, then the new system is compatible with MSSQL';

// Bind values
mssql_bind($stmt, '@author',    'Felipe Pena',  SQLVARCHAR,     false,  false,   60);
mssql_bind($stmt, '@date',      '08/10/2008',   SQLVARCHAR,     false,  false,   20);
mssql_bind($stmt, '@title',     $title,         SQLVARCHAR,     false,  false,   60);
mssql_bind($stmt, '@content',   $content,       SQLTEXT);

// Execute the statement
mssql_execute($stmt);

// And we can free it like so:
mssql_free_statement($stmt);
?>
```

### 注释

> **Note**:
>
> If the stored procedure returns parameters or a return value these
> will be available after the call to <span
> class="function">mssql\_execute</span> unless the stored procedure
> returns more than one result set. In that case use <span
> class="function">mssql\_next\_result</span> to shift through the
> results. When the last result has been processed the output parameters
> and return values will be available.

### 参见

-   <span class="function">mssql\_bind</span>
-   <span class="function">mssql\_free\_statement</span>
-   <span class="function">mssql\_init</span>

mssql\_fetch\_array
===================

Fetch a result row as an associative array, a numeric array, or both

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">sqlsrv\_fetch\_array</span>
-   <span class="function">odbc\_fetch\_array</span>

### 说明

<span class="type">array</span> <span
class="methodname">mssql\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = MSSQL\_BOTH</span></span> \]
)

<span class="function">mssql\_fetch\_array</span> is an extended version
of <span class="function">mssql\_fetch\_row</span>. In addition to
storing the data in the numeric indices of the result array, it also
stores the data in associative indices, using the field names as keys.

An important thing to note is that using <span
class="function">mssql\_fetch\_array</span> is NOT significantly slower
than using <span class="function">mssql\_fetch\_row</span>, while it
provides a significant added value.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`result_type`  
The type of array that is to be fetched. It's a constant and can take
the following values: **`MSSQL_ASSOC`**, **`MSSQL_NUM`**, and
**`MSSQL_BOTH`**.

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

### 范例

**示例 \#1 <span class="function">mssql\_fetch\_array</span> example**

``` php
<?php
// Send a select query to MSSQL
$query = mssql_query('SELECT [username], [name] FROM [php].[dbo].[userlist]');

// Check if there were any records
if (!mssql_num_rows($query)) {
    echo 'No records found';
} else {
    // The following is equal to the code below:
    //
    // while ($row = mssql_fetch_row($query)) {

    while ($row = mssql_fetch_array($query, MSSQL_NUM)) {
        // ...
    }
}

// Free the query result
mssql_free_result($query);
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数返回的字段名*大小写敏感*。</span>

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 参见

-   <span class="function">mssql\_fetch\_row</span>

mssql\_fetch\_assoc
===================

Returns an associative array of the current row in the result

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">sqlsrv\_fetch\_array</span>
-   <span class="function">odbc\_fetch\_array</span>

### 说明

<span class="type">array</span> <span
class="methodname">mssql\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span>
`$result_id`</span> )

Returns an associative array that corresponds to the fetched row and
moves the internal data pointer ahead. <span
class="function">mssql\_fetch\_assoc</span> is equivalent to calling
<span class="function">mssql\_fetch\_array</span> with **`MSSQL_ASSOC`**
for the optional second parameter.

### 参数

`result_id`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns an associative array that corresponds to the fetched row, or
**`FALSE`** if there are no more rows.

### 范例

**示例 \#1 <span class="function">mssql\_fetch\_assoc</span> example**

``` php
<?php
// Send a select query to MSSQL
$query = mssql_query('SELECT [username], [name] FROM [php].[dbo].[userlist]');

// Check if there were any records
if (!mssql_num_rows($query)) {
    echo 'No records found';
}
else
{
    // Print a nice list of users in the format of:
    // * name (username)

    echo '<ul>';

    while ($row = mssql_fetch_assoc($query)) {
        echo '<li>' . $row['name'] . ' (' . $row['username'] . ')</li>';
    }

    echo '</ul>';
}

// Free the query result
mssql_free_result($query);
?>
```

mssql\_fetch\_batch
===================

Returns the next batch of records

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">int</span> <span
class="methodname">mssql\_fetch\_batch</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Returns the next batch of records.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns the number of rows in the returned batch.

### 范例

**示例 \#1 <span class="function">mssql\_fetch\_batch</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link);

// Send a query
$result = mssql_query('SELECT * FROM [php].[dbo].[people]', $link, 100);
$records = 10;

while ($records >= 0) {
    while ($row = mssql_fetch_assoc($result)) {
        // Do stuff ...
    }

    --$records;
}

if ($batchsize = mssql_fetch_batch($result)) {
    // $batchsize is the number of records left 
    // in the result, but not shown above
}
?>
```

mssql\_fetch\_field
===================

Get field information

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::getColumnMeta</span>
-   <span class="function">sqlsrv\_field\_metadata</span>
-   The various odbc\_field\_\* functions in the
    <a href="/book/uodbc.html" class="link">unified ODBC driver</a>.

### 说明

<span class="type">object</span> <span
class="methodname">mssql\_fetch\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`<span class="initializer"> = -1</span></span> \] )

<span class="function">mssql\_fetch\_field</span> can be used in order
to obtain information about fields in a certain query result.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`field_offset`  
The numerical field offset. If the field offset is not specified, the
next field that was not yet retrieved by this function is retrieved. The
`field_offset` starts at 0.

### 返回值

Returns an object containing field information.

The properties of the object are:

-   <span class="simpara"> name - column name. if the column is a result
    of a function, this property is set to computed\#N, where \#N is a
    serial number. </span>
-   <span class="simpara"> column\_source - the table from which the
    column was taken </span>
-   <span class="simpara"> max\_length - maximum length of the column
    </span>
-   <span class="simpara"> numeric - 1 if the column is numeric </span>
-   <span class="simpara"> type - the column type. </span>

### 范例

**示例 \#1 <span class="function">mssql\_fetch\_field</span> example**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Send a select query to MSSQL
$query = mssql_query('SELECT * FROM [php].[dbo].[persons]');

// Construct table
echo '<h3>Table structure for \'persons\'</h3>';
echo '<table border="1">';

// Table header
echo '<thead>';
echo '<tr>';
echo '<td>Field name</td>';
echo '<td>Data type</td>';
echo '<td>Max length</td>';
echo '</tr>';
echo '</thead>';

// Dump all fields
echo '<tbody>';

for ($i = 0; $i < mssql_num_fields($query); ++$i) {
    // Fetch the field information
    $field = mssql_fetch_field($query, $i);

    // Print the row
    echo '<tr>';
    echo '<td>' . $field->name . '</td>';
    echo '<td>' . strtoupper($field->type) . '</td>';
    echo '<td>' . $field->max_length . '</td>';
    echo '</tr>';
}

echo '</tbody>';
echo '</table>';

// Free the query result
mssql_free_result($query);
?>
```

### 参见

-   <span class="function">mssql\_field\_seek</span>

mssql\_fetch\_object
====================

Fetch row as object

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::fetchObject</span>
-   <span class="function">sqlsrv\_fetch\_object</span>
-   <span class="function">odbc\_fetch\_object</span>

### 说明

<span class="type">object</span> <span
class="methodname">mssql\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">mssql\_fetch\_object</span> is similar to <span
class="function">mssql\_fetch\_array</span>, with one difference - an
object is returned, instead of an array. Indirectly, that means that you
can only access the data by the field names, and not by their offsets
(numbers are illegal property names).

Speed-wise, the function is identical to <span
class="function">mssql\_fetch\_array</span>, and almost as quick as
<span class="function">mssql\_fetch\_row</span> (the difference is
insignificant).

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns an object with properties that correspond to the fetched row, or
**`FALSE`** if there are no more rows.

### 范例

**示例 \#1 <span class="function">mssql\_fetch\_object</span> example**

``` php
<?php
// Send a select query to MSSQL
$query = mssql_query('SELECT [username], [name] FROM [php].[dbo].[userlist]');

// Check if there were any records
if (!mssql_num_rows($query)) {
    echo 'No records found';
} else {
    // Print a nice list of users in the format of:
    // * name (username)

    echo '<ul>';

    while ($row = mssql_fetch_object($query)) {
        echo '<li>' . $row->name . ' (' . $row->username . ')</li>';
    }

    echo '</ul>';
}

// Free the query result
mssql_free_result($query);
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数返回的字段名*大小写敏感*。</span>

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 参见

-   <span class="function">mssql\_fetch\_array</span>
-   <span class="function">mssql\_fetch\_row</span>

mssql\_fetch\_row
=================

Get row as enumerated array

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::fetch</span>
-   <span class="function">sqlsrv\_fetch\_array</span>
-   <span class="function">odbc\_fetch\_row</span>

### 说明

<span class="type">array</span> <span
class="methodname">mssql\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">mssql\_fetch\_row</span> fetches one row of data
from the result associated with the specified result identifier. The row
is returned as an array. Each result column is stored in an array
offset, starting at offset 0.

Subsequent call to <span class="function">mssql\_fetch\_row</span> would
return the next row in the result set, or **`FALSE`** if there are no
more rows.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

### 范例

**示例 \#1 <span class="function">mssql\_fetch\_row</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link);

// Query to execute
$query = mssql_query('SELECT [id], [quote] FROM [quotes] WHERE [id] = \'42\'', $link);

// Did the query fail?
if (!$query) {
    die('MSSQL error: ' . mssql_get_last_message());
}

// Fetch the row
$row = mssql_fetch_row($query);

// Print the 'quote'
echo 'Quote #' . $row[0] . ': "' . $row[1] . '"';
?>
```

以上例程的输出类似于：

    Quote #42: "The answer to everything..."

### 注释

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 参见

-   <span class="function">mssql\_fetch\_array</span>
-   <span class="function">mssql\_fetch\_object</span>
-   <span class="function">mssql\_data\_seek</span>
-   <span class="function">mssql\_result</span>

mssql\_field\_length
====================

Get the length of a field

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::getColumnMeta</span>
-   <span class="function">sqlsrv\_field\_metadata</span>
-   <span class="function">odbc\_field\_len</span>

### 说明

<span class="type">int</span> <span
class="methodname">mssql\_field\_length</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`<span class="initializer"> = -1</span></span> \] )

Returns the length of field no. `offset` in `result`.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`offset`  
The field offset, starts at 0. If omitted, the current field is used.

### 返回值

The length of the specified field index on success 或者在失败时返回
**`FALSE`**.

### 范例

**示例 \#1 <span class="function">mssql\_field\_length</span> example**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Send a select query to MSSQL
$query = mssql_query('SELECT [name], [age] FROM [php].[dbo].[persons]');

// Print the field length
echo 'The field \'age\' has a data length of ' . mssql_field_length($query, 1);

// Free the query result
mssql_free_result($query);
?>
```

以上例程的输出类似于：

    The field 'age' has a data length of 4

### 注释

> **Note**: **Note to Windows Users**  
>
> Due to a limitation in the underlying API used by PHP (MS DBLib C
> API), the length of *VARCHAR* fields is limited to *255*. If you need
> to store more data, use a *TEXT* field instead.

### 参见

-   <span class="function">mssql\_field\_name</span>
-   <span class="function">mssql\_field\_type</span>

mssql\_field\_name
==================

Get the name of a field

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::getColumnMeta</span>
-   <span class="function">sqlsrv\_field\_metadata</span>
-   <span class="function">odbc\_field\_name</span>

### 说明

<span class="type">string</span> <span
class="methodname">mssql\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`<span class="initializer"> = -1</span></span> \] )

Returns the name of field no. `offset` in `result`.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`offset`  
The field offset, starts at 0. If omitted, the current field is used.

### 返回值

The name of the specified field index on success 或者在失败时返回
**`FALSE`**.

### 范例

**示例 \#1 <span class="function">mssql\_field\_name</span> example**

``` php
<?php
// Send a select query to MSSQL
$query = mssql_query('SELECT [username], [name], [email] FROM [php].[dbo].[userlist]');

echo 'Result set contains the following field(s):', PHP_EOL;

// Dump all field names in result
for ($i = 0; $i < mssql_num_fields($query); ++$i) {
    echo ' - ' . mssql_field_name($query, $i), PHP_EOL;
}

// Free the query result
mssql_free_result($query);
?>
```

以上例程的输出类似于：

    Result set contains the following field(s):
     - username
     - name
     - email

### 参见

-   <span class="function">mssql\_field\_length</span>
-   <span class="function">mssql\_field\_type</span>

mssql\_field\_seek
==================

Seeks to the specified field offset

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_field\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

Seeks to the specified field offset. If the next call to <span
class="function">mssql\_fetch\_field</span> won't include a field
offset, this field would be returned.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`field_offset`  
The field offset, starts at 0.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Using <span class="function">mssql\_field\_seek</span> on the
example for <span class="function">mssql\_fetch\_field</span>**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Send a select query to MSSQL
$query = mssql_query('SELECT * FROM [php].[dbo].[persons]');

// Construct table
echo '<h3>Table structure for \'persons\'</h3>';
echo '<table border="1">';

// Table header
echo '<thead>';
echo '<tr>';
echo '<td>Field name</td>';
echo '<td>Data type</td>';
echo '<td>Max length</td>';
echo '</tr>';
echo '</thead>';

// Dump all fields
echo '<tbody>';

for ($i = 0; $i < mssql_num_fields($query); ++$i) {
    // Fetch the field information, notice the 
    // field_offset parameter is not set. See 
    // the mssql_field_seek call below
    $field = mssql_fetch_field($query);

    // Print the row
    echo '<tr>';
    echo '<td>' . $field->name . '</td>';
    echo '<td>' . strtoupper($field->type) . '</td>';
    echo '<td>' . $field->max_length . '</td>';
    echo '</tr>';

    // Move the internal seek pointer to the next
    // row in the result set
    mssql_field_seek($query, $i + 1);
}

echo '</tbody>';
echo '</table>';

// Free the query result
mssql_free_result($query);
?>
```

### 参见

-   <span class="function">mssql\_fetch\_field</span>

mssql\_field\_type
==================

Gets the type of a field

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::getColumnMeta</span>
-   <span class="function">sqlsrv\_field\_metadata</span>
-   <span class="function">odbc\_field\_type</span>

### 说明

<span class="type">string</span> <span
class="methodname">mssql\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`<span class="initializer"> = -1</span></span> \] )

Returns the type of field no. `offset` in `result`.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`offset`  
The field offset, starts at 0. If omitted, the current field is used.

### 返回值

The type of the specified field index on success 或者在失败时返回
**`FALSE`**.

### 范例

**示例 \#1 <span class="function">mssql\_field\_type</span> example**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Send a select query to MSSQL
$query = mssql_query('SELECT [name] FROM [php].[dbo].[persons]');

// Print the field type and length
echo '\'' . mssql_field_name($query, 0) . '\' is a type of ' . 
     strtoupper(mssql_field_type($query, 0)) . 
     '(' . mssql_field_length($query, 0) . ')';

// Free the query result
mssql_free_result($query);
?>
```

以上例程的输出类似于：

    'name' is a type of CHAR(50)

### 参见

-   <span class="function">mssql\_field\_length</span>
-   <span class="function">mssql\_field\_name</span>

mssql\_free\_result
===================

Free result memory

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">odbc\_free\_result</span>

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">mssql\_free\_result</span> only needs to be
called if you are worried about using too much memory while your script
is running. All result memory will automatically be freed when the
script ends. You may call <span
class="function">mssql\_free\_result</span> with the result identifier
as an argument and the associated result memory will be freed.

### 参数

`result`  
The result resource that is being freed. This result comes from a call
to <span class="function">mssql\_query</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mssql\_free\_result</span> example**

``` php
<?php
// Select some data from a table
$query = mssql_query('SELECT * FROM [php].[dbo].[persons]', $link);

// Handle query result here

// When we're done we free the result by calling
// mssql_free_result like so:
mssql_free_result($query);
?>
```

### 参见

-   <span class="function">mssql\_free\_statement</span>

mssql\_free\_statement
======================

Free statement memory

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">sqlsrv\_free\_stmt</span>

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_free\_statement</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

<span class="function">mssql\_free\_statement</span> only needs to be
called if you are worried about using too much memory while your script
is running. All statement memory will automatically be freed when the
script ends. You may call <span
class="function">mssql\_free\_statement</span> with the statement
identifier as an argument and the associated statement memory will be
freed.

### 参数

`stmt`  
Statement resource, obtained with <span
class="function">mssql\_init</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mssql\_free\_statement</span>
example**

``` php
<?php
// Create a new statement
$stmt = mssql_init('test');

// Bind values here and execute the statement

// once we're done, we clear it from the memory
// using mssql_free_statement like so:
mssql_free_statement($stmt);
?>
```

### 参见

-   <span class="function">mssql\_bind</span>
-   <span class="function">mssql\_execute</span>
-   <span class="function">mssql\_init</span>
-   <span class="function">mssql\_free\_result</span>

mssql\_get\_last\_message
=========================

Returns the last message from the server

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::errorInfo</span>
-   <span class="function">sqlsrv\_errors</span>
-   <span class="function">odbc\_errormsg</span>

### 说明

<span class="type">string</span> <span
class="methodname">mssql\_get\_last\_message</span> ( <span
class="methodparam">void</span> )

Gets the last message from the MS-SQL server

### 参数

此函数没有参数。

### 返回值

Returns last error message from server, or an empty string if no error
messages are returned from MSSQL.

### 范例

**示例 \#1 <span class="function">mssql\_get\_last\_message</span>
example**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Make a query that will fail
$query = @mssql_query('SELECT * FROM [php].[dbo].[not-found]');

if (!$query) {
    // The query has failed, print a nice error message
    // using mssql_get_last_message()
    die('MSSQL error: ' . mssql_get_last_message());
}
?>
```

以上例程的输出类似于：

    MSSQL error: Invalid object name 'php.dbo.not-found'.

### 参见

-   <span class="function">mssql\_min\_error\_severity</span>
-   <span class="function">mssql\_min\_message\_severity</span>

mssql\_guid\_string
===================

Converts a 16 byte binary GUID to a string

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">string</span> <span
class="methodname">mssql\_guid\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$binary`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$short_format`<span class="initializer"> = **`FALSE`**</span></span> \]
)

Converts a 16 byte binary GUID to a string.

### 参数

`binary`  
A 16 byte binary GUID.

`short_format`  
Whenever to use short format.

### 返回值

Returns the converted string on success.

### 范例

**示例 \#1 <span class="function">mssql\_guid\_string</span> example**

``` php
<?php
$binary = '19555081977808608437941339997619274330352755554827939936';

var_dump(mssql_guid_string($binary));
var_dump(mssql_guid_string($binary, true));
?>
```

以上例程会输出：

    string(36) "35353931-3035-3138-3937-373830383630"
    string(32) "31393535353038313937373830383630"

mssql\_init
===========

Initializes a stored procedure or a remote stored procedure

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   Using an *EXEC* query issued through
    <a href="/book/pdo.html#MS%20SQL%20Server%20(PDO)" class="link">PDO_SQLSRV</a>,
    <a href="/book/pdo.html#ODBC%20and%20DB2%20(PDO)" class="link">PDO_ODBC</a>,
    <a href="/book/sqlsrv.html" class="link">SQLSRV</a>, or the
    <a href="/book/uodbc.html" class="link">unified ODBC driver</a>.

### 说明

<span class="type">resource</span> <span
class="methodname">mssql\_init</span> ( <span class="methodparam"><span
class="type">string</span> `$sp_name`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

Initializes a stored procedure or a remote stored procedure.

### 参数

`sp_name`  
Stored procedure name, like *ownew.sp\_name* or
*otherdb.owner.sp\_name*.

`link_identifier`  
A MS SQL link identifier, returned by <span
class="function">mssql\_connect</span>.

### 返回值

Returns a resource identifier "statement", used in subsequent calls to
<span class="function">mssql\_bind</span> and <span
class="function">mssql\_execute</span>, or **`FALSE`** on errors.

### 范例

**示例 \#1 <span class="function">mssql\_init</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link);

// Create a new statement
$stmt = mssql_init('StatementTest', $link);

// Bind values here

// Once values are binded we execute our statement 
// using mssql_execute:
mssql_execute($stmt);

// And we can free it like so:
mssql_free_statement($stmt);
?>
```

### 参见

-   <span class="function">mssql\_bind</span>
-   <span class="function">mssql\_execute</span>
-   <span class="function">mssql\_free\_statement</span>

mssql\_min\_error\_severity
===========================

Sets the minimum error severity

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">mssql\_min\_error\_severity</span> ( <span
class="methodparam"><span class="type">int</span> `$severity`</span> )

Sets the minimum error severity.

### 参数

`severity`  
The new error severity.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mssql\_min\_error\_severity</span>
example**

``` php
<?php
// Connect to MSSQL and select the database
mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Set the minimum error severity to not include SQL 
// syntax errors by setting it to something greater than 
// or equal to 1.
mssql_min_error_severity(1);

// Send a query we know that will cause an syntax error, in
// this case we use the MySQL quote signs instead of wrapping 
// square brackets around the field and table names.
$query = mssql_query('SELECT `syntax`, `error` FROM `MSSQL`');

if (!$query) {
    // Custom error handler ...
}
?>
```

mssql\_min\_message\_severity
=============================

Sets the minimum message severity

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">mssql\_min\_message\_severity</span> ( <span
class="methodparam"><span class="type">int</span> `$severity`</span> )

Sets the minimum message severity.

### 参数

`severity`  
The new message severity.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mssql\_min\_message\_severity</span>
example**

``` php
<?php
// Connect to MSSQL
mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');

// Set the minimum message severity to 17, this
// will not show any messages issued by the underlaying
// API when we select a non-existent database below
mssql_min_message_severity(17);

// Select a non-existent database
mssql_select_db('THIS_DATABASE_DOES_NOT_EXISTS');
?>
```

以上例程会输出：

    mssql_select_db(): Unable to select database:  THIS_DATABASE_DOES_NOT_EXISTS

mssql\_next\_result
===================

Move the internal result pointer to the next result

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::nextRowset</span>
-   <span class="function">sqlsrv\_next\_result</span>
-   <span class="function">odbc\_next\_result</span>

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span>
`$result_id`</span> )

When sending more than one SQL statement to the server or executing a
stored procedure with multiple results, it will cause the server to
return multiple result sets. This function will test for additional
results available form the server. If an additional result set exists it
will free the existing result set and prepare to fetch the rows from the
new result set.

### 参数

`result_id`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns **`TRUE`** if an additional result set was available or
**`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">mssql\_next\_result</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link);

// Send a query to MSSQL
$sql = 'SELECT [name], [age] FROM [php].[dbo].[persons]';
$query = mssql_query($sql, $link);

// Iterate through returned records
do {
    while ($row = mssql_fetch_row($query)) {
        // Handle record ...
    }
} while (mssql_next_result($query));

// Clean up
mssql_free_result($query);
mssql_close($link);
?>
```

mssql\_num\_fields
==================

Gets the number of fields in result

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::columnCount</span>
-   <span class="function">sqlsrv\_num\_fields</span>
-   <span class="function">odbc\_num\_fields</span>

### 说明

<span class="type">int</span> <span
class="methodname">mssql\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">mssql\_num\_fields</span> returns the number of
fields in a result set.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns the number of fields, as an integer.

### 范例

**示例 \#1 <span class="function">mssql\_num\_fields</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link);

// Select some data from our database
$data = mssql_query('SELECT [name], [age] FROM [php].[dbo].[persons]');

// Construct a table
echo '<table border="1">';

$header = false;

// Iterate through returned results
while ($row = mssql_fetch_array($data)) {
    // Build the table header
    if (!$header) {
        echo '<thead>';
        echo '<tr>';

        for ($i = 1; ($i + 1) <= mssql_num_fields($data); ++$i) {
            echo '<td>' . ucfirst($row[$i]) . '</td>';
        }

        echo '</tr>';
        echo '</thead>';
        echo '<tbody>';

        $header = true;
    }

    // Build the row
    echo '<tr>';

    foreach($row as $value) {
        echo '<td>' . $value . '</td>';
    }

    echo '</tr>';
}

// Close table
echo '</tbody>';
echo '</table>';

// Clean up
mssql_free_result($data);
mssql_close($link);
?>
```

### 参见

-   <span class="function">mssql\_query</span>
-   <span class="function">mssql\_fetch\_field</span>
-   <span class="function">mssql\_num\_rows</span>

mssql\_num\_rows
================

Gets the number of rows in result

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::rowCount</span>
-   <span class="function">sqlsrv\_num\_rows</span>
-   <span class="function">odbc\_num\_rows</span>

### 说明

<span class="type">int</span> <span
class="methodname">mssql\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">mssql\_num\_rows</span> returns the number of
rows in a result set.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

### 返回值

Returns the number of rows, as an integer.

### 范例

**示例 \#1 <span class="function">mssql\_num\_rows</span> example**

``` php
<?php
// Connect to MSSQL and select the database
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php');

// Select all our records from a table
$query = mssql_query('SELECT * FROM [php].[dbo].[persons]');

echo 'Total records in database: ' . mssql_num_rows($query);

// Clean up
mssql_free_result($query);
?>
```

### 参见

-   <span class="function">mssql\_query</span>
-   <span class="function">mssql\_fetch\_row</span>

mssql\_pconnect
===============

Open persistent MS SQL connection

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDO::\_\_construct</span>
-   <span class="function">sqlsrv\_connect</span>
-   <span class="function">odbc\_pconnect</span>

### 说明

<span class="type">resource</span> <span
class="methodname">mssql\_pconnect</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$servername`</span> \[, <span class="methodparam"><span
class="type">string</span> `$username`</span> \[, <span
class="methodparam"><span class="type">string</span> `$password`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$new_link`<span class="initializer"> = **`FALSE`**</span></span>
\]\]\]\] )

<span class="function">mssql\_pconnect</span> acts very much like <span
class="function">mssql\_connect</span> with two major differences.

First, when connecting, the function would first try to find a
(persistent) link that's already open with the same host, username and
password. If one is found, an identifier for it will be returned instead
of opening a new connection.

Second, the connection to the SQL server will not be closed when the
execution of the script ends. Instead, the link will remain open for
future use (<span class="function">mssql\_close</span> will not close
links established by <span class="function">mssql\_pconnect</span>).

This type of links is therefore called 'persistent'.

### 参数

`servername`  
The MS SQL server. It can also include a port number. e.g.
*hostname:port*.

`username`  
The username.

`password`  
The password.

`new_link`  
If a second call is made to <span
class="function">mssql\_pconnect</span> with the same arguments, no new
link will be established, but instead, the link identifier of the
already opened link will be returned. This parameter modifies this
behavior and makes <span class="function">mssql\_pconnect</span> always
open a new link, even if <span class="function">mssql\_pconnect</span>
was called before with the same parameters.

### 返回值

Returns a positive MS SQL persistent link identifier on success, or
**`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">mssql\_pconnect</span> using the
`new_link` parameter**

``` php
<?php
// Connect to MSSQL and select the database
$link1 = mssql_pconnect('MANGO\SQLEXPRESS', 'sa', 'phpfi');
mssql_select_db('php', $link1);

// Create a new link
$link2 = mssql_pconnect('MANGO\SQLEXPRESS', 'sa', 'phpfi', true);
mssql_select_db('random', $link2);
?>
```

mssql\_query
============

Send MS SQL query

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDO::query</span>
-   <span class="function">sqlsrv\_query</span>
-   <span class="function">odbc\_exec</span>

### 说明

<span class="type">mixed</span> <span
class="methodname">mssql\_query</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">int</span> `$batch_size`<span class="initializer"> =
0</span></span> \]\] )

<span class="function">mssql\_query</span> sends a query to the
currently active database on the server that's associated with the
specified link identifier.

### 参数

`query`  
An SQL query.

`link_identifier`  
A MS SQL link identifier, returned by <span
class="function">mssql\_connect</span> or <span
class="function">mssql\_pconnect</span>.

If the link identifier isn't specified, the last opened link is assumed.
If no link is open, the function tries to establish a link as if <span
class="function">mssql\_connect</span> was called, and use it.

`batch_size`  
The number of records to batch in the buffer.

### 返回值

Returns a MS SQL result resource on success, **`TRUE`** if no rows were
returned, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">mssql\_query</span> example**

``` php
<?php
// Connect to MSSQL
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');

if (!$link || !mssql_select_db('php', $link)) {
    die('Unable to connect or select database!');
}

// Do a simple query, select the version of 
// MSSQL and print it.
$version = mssql_query('SELECT @@VERSION');
$row = mssql_fetch_array($version);

echo $row[0];

// Clean up
mssql_free_result($version);
?>
```

### 注释

> **Note**:
>
> If the query returns multiple results then it is necessary to fetch
> all results by <span class="function">mssql\_next\_result</span> or
> free the results by <span class="function">mssql\_free\_result</span>
> before executing next query.

### 参见

-   <span class="function">mssql\_select\_db</span>
-   <span class="function">mssql\_connect</span>

mssql\_result
=============

Get result data

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">odbc\_result</span>

### 说明

<span class="type">string</span> <span
class="methodname">mssql\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span> `$row`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$field`</span> )

<span class="function">mssql\_result</span> returns the contents of one
cell from a MS SQL result set.

### 参数

`result`  
The result resource that is being evaluated. This result comes from a
call to <span class="function">mssql\_query</span>.

`row`  
The row number.

`field`  
Can be the field's offset, the field's name or the field's table dot
field's name (tablename.fieldname). If the column name has been aliased
('select foo as bar from...'), it uses the alias instead of the column
name.

> **Note**:
>
> Specifying a numeric offset for the `field` argument is much quicker
> than specifying a *fieldname* or *tablename.fieldname* argument.

### 返回值

Returns the contents of the specified cell.

### 范例

**示例 \#1 <span class="function">mssql\_result</span> example**

``` php
<?php
// Send a select query to MSSQL
$query = mssql_query('SELECT [username] FROM [php].[dbo].[userlist]');

// Check if there were any records
if (!mssql_num_rows($query)) {
    echo 'No records found';
} else {
    for ($i = 0; $i < mssql_num_rows($query); ++$i) {
        echo mssql_result($query, $i, 'username'), PHP_EOL;
    }
}

// Free the query result
mssql_free_result($query);
?>
```

以上例程的输出类似于：

    Kalle
    Felipe
    Emil
    Ross

**示例 \#2 Faster alternative to above example**

``` php
<?php
// Send a select query to MSSQL
$query = mssql_query('SELECT [username] FROM [php].[dbo].[userlist]');

// Check if there were any records
if (!mssql_num_rows($query)) {
    echo 'No records found';
} else {
    while ($row = mssql_fetch_array($query)) {
        echo $row['username'], PHP_EOL;
    }
}

// Free the query result
mssql_free_result($query);
?>
```

### 注释

> **Note**:
>
> When working on large result sets, you should consider using one of
> the functions that fetch an entire row (specified below). As these
> functions return the contents of multiple cells in one function call,
> they're MUCH quicker than <span class="function">mssql\_result</span>.

### 参见

Recommended high-performance alternatives:

-   <span class="function">mssql\_fetch\_row</span>
-   <span class="function">mssql\_fetch\_array</span>
-   <span class="function">mssql\_fetch\_assoc</span>
-   <span class="function">mssql\_fetch\_object</span>

mssql\_rows\_affected
=====================

Returns the number of records affected by the query

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">PDOStatement::rowCount</span>
-   <span class="function">sqlsrv\_rows\_affected</span>

### 说明

<span class="type">int</span> <span
class="methodname">mssql\_rows\_affected</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> )

Returns the number of records affected by the last write query.

### 参数

`link_identifier`  
A MS SQL link identifier, returned by <span
class="function">mssql\_connect</span> or <span
class="function">mssql\_pconnect</span>.

### 返回值

Returns the number of records affected by last operation.

### 范例

**示例 \#1 <span class="function">mssql\_rows\_affected</span> example**

``` php
<?php
// Delete all rows in a table
mssql_query('TRUNCATE TABLE [php].[dbo].[persons]');

echo 'Deleted ' . mssql_rows_affected($link) . ' row(s)';
?>
```

mssql\_select\_db
=================

Select MS SQL database

**Warning**

This function was *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <a href="/book/pdo.html#PDO_SQLSRV%20DSN" class="link">PDO_SQLSRV DSN</a>
-   <a href="/book/pdo.html#PDO_ODBC%20DSN" class="link">PDO_ODBC DSN</a>
-   <span class="function">sqlsrv\_connect</span>
-   <span class="function">odbc\_connect</span>

### 说明

<span class="type">bool</span> <span
class="methodname">mssql\_select\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">mssql\_select\_db</span> sets the current active
database on the server that's associated with the specified link
identifier.

Every subsequent call to <span class="function">mssql\_query</span> will
be made on the active database.

### 参数

`database_name`  
The database name.

To escape the name of a database that contains spaces, hyphens ("-"), or
any other exceptional characters, the database name must be enclosed in
brackets, as is shown in the example, below. This technique must also be
applied when selecting a database name that is also a reserved word
(such as *primary*).

`link_identifier`  
A MS SQL link identifier, returned by <span
class="function">mssql\_connect</span> or <span
class="function">mssql\_pconnect</span>.

If no link identifier is specified, the last opened link is assumed. If
no link is open, the function will try to establish a link as if <span
class="function">mssql\_connect</span> was called, and use it.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mssql\_select\_db</span> example**

``` php
<?php
// Create a link to MSSQL
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');

// Select the database 'php'
mssql_select_db('php', $link);
?>
```

**示例 \#2 Escaping the database name with square brackets**

``` php
<?php
// Create a link to MSSQL
$link = mssql_connect('KALLESPC\SQLEXPRESS', 'sa', 'phpfi');

// Select the database 'my.database-name'
mssql_select_db('[my.database-name]', $link);
?>
```

### 参见

-   <span class="function">mssql\_connect</span>
-   <span class="function">mssql\_pconnect</span>
-   <span class="function">mssql\_query</span>

**目录**

-   [mssql\_bind](/book/mssql.html#mssql_bind) — Adds a parameter to a
    stored procedure or a remote stored procedure
-   [mssql\_close](/book/mssql.html#mssql_close) — 关闭MS SQL Server链接
-   [mssql\_connect](/book/mssql.html#mssql_connect) — 打开MS SQL
    server链接
-   [mssql\_data\_seek](/book/mssql.html#mssql_data_seek) — Moves
    internal row pointer
-   [mssql\_execute](/book/mssql.html#mssql_execute) — Executes a stored
    procedure on a MS SQL server database
-   [mssql\_fetch\_array](/book/mssql.html#mssql_fetch_array) — Fetch a
    result row as an associative array, a numeric array, or both
-   [mssql\_fetch\_assoc](/book/mssql.html#mssql_fetch_assoc) — Returns
    an associative array of the current row in the result
-   [mssql\_fetch\_batch](/book/mssql.html#mssql_fetch_batch) — Returns
    the next batch of records
-   [mssql\_fetch\_field](/book/mssql.html#mssql_fetch_field) — Get
    field information
-   [mssql\_fetch\_object](/book/mssql.html#mssql_fetch_object) — Fetch
    row as object
-   [mssql\_fetch\_row](/book/mssql.html#mssql_fetch_row) — Get row as
    enumerated array
-   [mssql\_field\_length](/book/mssql.html#mssql_field_length) — Get
    the length of a field
-   [mssql\_field\_name](/book/mssql.html#mssql_field_name) — Get the
    name of a field
-   [mssql\_field\_seek](/book/mssql.html#mssql_field_seek) — Seeks to
    the specified field offset
-   [mssql\_field\_type](/book/mssql.html#mssql_field_type) — Gets the
    type of a field
-   [mssql\_free\_result](/book/mssql.html#mssql_free_result) — Free
    result memory
-   [mssql\_free\_statement](/book/mssql.html#mssql_free_statement) —
    Free statement memory
-   [mssql\_get\_last\_message](/book/mssql.html#mssql_get_last_message)
    — Returns the last message from the server
-   [mssql\_guid\_string](/book/mssql.html#mssql_guid_string) — Converts
    a 16 byte binary GUID to a string
-   [mssql\_init](/book/mssql.html#mssql_init) — Initializes a stored
    procedure or a remote stored procedure
-   [mssql\_min\_error\_severity](/book/mssql.html#mssql_min_error_severity)
    — Sets the minimum error severity
-   [mssql\_min\_message\_severity](/book/mssql.html#mssql_min_message_severity)
    — Sets the minimum message severity
-   [mssql\_next\_result](/book/mssql.html#mssql_next_result) — Move the
    internal result pointer to the next result
-   [mssql\_num\_fields](/book/mssql.html#mssql_num_fields) — Gets the
    number of fields in result
-   [mssql\_num\_rows](/book/mssql.html#mssql_num_rows) — Gets the
    number of rows in result
-   [mssql\_pconnect](/book/mssql.html#mssql_pconnect) — Open persistent
    MS SQL connection
-   [mssql\_query](/book/mssql.html#mssql_query) — Send MS SQL query
-   [mssql\_result](/book/mssql.html#mssql_result) — Get result data
-   [mssql\_rows\_affected](/book/mssql.html#mssql_rows_affected) —
    Returns the number of records affected by the query
-   [mssql\_select\_db](/book/mssql.html#mssql_select_db) — Select MS
    SQL database
