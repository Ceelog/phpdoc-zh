SQLite3
=======

**目录**

-   [简介](/book/sqlite3.html#简介)
-   [安装／配置](/book/sqlite3.html#安装／配置)
    -   [需求](/book/sqlite3.html#需求)
    -   [安装](/book/sqlite3.html#安装)
    -   [运行时配置](/book/sqlite3.html#运行时配置)
    -   [资源类型](/book/sqlite3.html#资源类型)
-   [预定义常量](/book/sqlite3.html#预定义常量)
-   [SQLite3](/book/sqlite3.html#SQLite3) — SQLite3 类
    -   [SQLite3::backup](/book/sqlite3.html#SQLite3::backup) — Backup
        one database to another database
    -   [SQLite3::busyTimeout](/book/sqlite3.html#SQLite3::busyTimeout)
        — Sets the busy connection handler
    -   [SQLite3::changes](/book/sqlite3.html#SQLite3::changes) —
        Returns the number of database rows that were changed (or
        inserted or deleted) by the most recent SQL statement
    -   [SQLite3::close](/book/sqlite3.html#SQLite3::close) — Closes the
        database connection
    -   [SQLite3::\_\_construct](/book/sqlite3.html#SQLite3::__construct)
        — Instantiates an SQLite3 object and opens an SQLite 3 database
    -   [SQLite3::createAggregate](/book/sqlite3.html#SQLite3::createAggregate)
        — Registers a PHP function for use as an SQL aggregate function
    -   [SQLite3::createCollation](/book/sqlite3.html#SQLite3::createCollation)
        — Registers a PHP function for use as an SQL collating function
    -   [SQLite3::createFunction](/book/sqlite3.html#SQLite3::createFunction)
        — Registers a PHP function for use as an SQL scalar function
    -   [SQLite3::enableExceptions](/book/sqlite3.html#SQLite3::enableExceptions)
        — Enable throwing exceptions
    -   [SQLite3::escapeString](/book/sqlite3.html#SQLite3::escapeString)
        — Returns a string that has been properly escaped
    -   [SQLite3::exec](/book/sqlite3.html#SQLite3::exec) — Executes a
        result-less query against a given database
    -   [SQLite3::lastErrorCode](/book/sqlite3.html#SQLite3::lastErrorCode)
        — Returns the numeric result code of the most recent failed
        SQLite request
    -   [SQLite3::lastErrorMsg](/book/sqlite3.html#SQLite3::lastErrorMsg)
        — Returns English text describing the most recent failed SQLite
        request
    -   [SQLite3::lastInsertRowID](/book/sqlite3.html#SQLite3::lastInsertRowID)
        — Returns the row ID of the most recent INSERT into the database
    -   [SQLite3::loadExtension](/book/sqlite3.html#SQLite3::loadExtension)
        — Attempts to load an SQLite extension library
    -   [SQLite3::open](/book/sqlite3.html#SQLite3::open) — Opens an
        SQLite database
    -   [SQLite3::openBlob](/book/sqlite3.html#SQLite3::openBlob) —
        Opens a stream resource to read a BLOB
    -   [SQLite3::prepare](/book/sqlite3.html#SQLite3::prepare) —
        Prepares an SQL statement for execution
    -   [SQLite3::query](/book/sqlite3.html#SQLite3::query) — Executes
        an SQL query
    -   [SQLite3::querySingle](/book/sqlite3.html#SQLite3::querySingle)
        — Executes a query and returns a single result
    -   [SQLite3::version](/book/sqlite3.html#SQLite3::version) —
        Returns the SQLite3 library version as a string constant and as
        a number
-   [SQLite3Stmt](/book/sqlite3.html#SQLite3Stmt) — SQLite3Stmt 类
    -   [SQLite3Stmt::bindParam](/book/sqlite3.html#SQLite3Stmt::bindParam)
        — Binds a parameter to a statement variable
    -   [SQLite3Stmt::bindValue](/book/sqlite3.html#SQLite3Stmt::bindValue)
        — Binds the value of a parameter to a statement variable
    -   [SQLite3Stmt::clear](/book/sqlite3.html#SQLite3Stmt::clear) —
        Clears all current bound parameters
    -   [SQLite3Stmt::close](/book/sqlite3.html#SQLite3Stmt::close) —
        Closes the prepared statement
    -   [SQLite3Stmt::execute](/book/sqlite3.html#SQLite3Stmt::execute)
        — Executes a prepared statement and returns a result set object
    -   [SQLite3Stmt::getSQL](/book/sqlite3.html#SQLite3Stmt::getSQL) —
        Get the SQL of the statement
    -   [SQLite3Stmt::paramCount](/book/sqlite3.html#SQLite3Stmt::paramCount)
        — Returns the number of parameters within the prepared statement
    -   [SQLite3Stmt::readOnly](/book/sqlite3.html#SQLite3Stmt::readOnly)
        — Returns whether a statement is definitely read only
    -   [SQLite3Stmt::reset](/book/sqlite3.html#SQLite3Stmt::reset) —
        Resets the prepared statement
-   [SQLite3Result](/book/sqlite3.html#SQLite3Result) — SQLite3Result 类
    -   [SQLite3Result::columnName](/book/sqlite3.html#SQLite3Result::columnName)
        — Returns the name of the nth column
    -   [SQLite3Result::columnType](/book/sqlite3.html#SQLite3Result::columnType)
        — Returns the type of the nth column
    -   [SQLite3Result::fetchArray](/book/sqlite3.html#SQLite3Result::fetchArray)
        — Fetches a result row as an associative or numerically indexed
        array or both
    -   [SQLite3Result::finalize](/book/sqlite3.html#SQLite3Result::finalize)
        — Closes the result set
    -   [SQLite3Result::numColumns](/book/sqlite3.html#SQLite3Result::numColumns)
        — Returns the number of columns in the result set
    -   [SQLite3Result::reset](/book/sqlite3.html#SQLite3Result::reset)
        — Resets the result set back to the first row

对 SQLite v3 数据库的支持信息。

安装／配置
==========

**目录**

-   [需求](/book/sqlite3.html#需求)
-   [安装](/book/sqlite3.html#安装)
-   [运行时配置](/book/sqlite3.html#运行时配置)
-   [资源类型](/book/sqlite3.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

SQLite3 扩展自 PHP 5.3.0 起已默认启用。 允许在编译时使用
*--without-sqlite3* 禁用之。

Windows 用户必须启用 `php_sqlite3.dll` 方可使用该扩展。自 PHP 5.3.0
起，此扩展的 DLL 文件 已包含于 Windows 版的 PHP 发行包中。

> **Note**:
>
> 该扩展是 PECL 扩展的简化版本， 但后者仅建议用于实验性用途。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                 | 默认 | 可修改范围       | 更新日志                                         |
|----------------------------------------------------------------------|------|------------------|--------------------------------------------------|
| <a href="/book/sqlite3.html#" class="link">sqlite3.extension_dir</a> | ""   | PHP\_INI\_SYSTEM | PHP 5.3.11 起可用                                |
| <a href="/book/sqlite3.html#" class="link">sqlite3.defensive</a>     | 1    | PHP\_INI\_SYSTEM | PHP 7.2.17 和 7.3.4 起可用，libsqlite ≥ 3.26.0。 |

这是配置指令的简短说明。

`sqlite3.extension_dir` <span class="type">string</span>  
Path to the directory where the loadable extensions for SQLite reside.

`sqlite3.defensive` <span class="type">bool</span>  
When the defensive flag is enabled, language features that allow
ordinary SQL to deliberately corrupt the database file are disabled.
This forbids writing directly to the schema, shadow tables (eg. FTS data
tables), or the sqlite\_dbpage virtual table. This `php.ini` setting is
only effective for libsqlite ≥ 3.26.0.

资源类型
--------

此扩展没有定义资源类型。

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SQLITE3_ASSOC`** (<span class="type">integer</span>)  
<span class="simpara"> 指定 <span
class="methodname">Sqlite3Result::fetchArray</span>
方法返回按列名称索引的数组，其中列名即相应结果集返回的列名。 </span>

**`SQLITE3_NUM`** (<span class="type">integer</span>)  
<span class="simpara"> 指定 <span
class="methodname">Sqlite3Result::fetchArray</span>
方法返回按列序号索引的数组，其中列号即相应结果集返回的列号，从第 0
列开始计数。 </span>

**`SQLITE3_BOTH`** (<span class="type">integer</span>)  
<span class="simpara"> 指定 <span
class="methodname">Sqlite3Result::fetchArray</span>
方法返回同时按列名称与列序号索引的数组，其中列名即相应结果集返回的列名，列号即相应结果集返回的列号，从第
0 列开始计数。 </span>

**`SQLITE3_INTEGER`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQLite3 INTEGER (整型) 存储类。 </span>

**`SQLITE3_FLOAT`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQLite3 REAL (FLOAT) (实型) 存储类。 </span>

**`SQLITE3_TEXT`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQLite3 TEXT (文本) 存储类。 </span>

**`SQLITE3_BLOB`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQLite3 BLOB (二进制对象) 存储类。 </span>

**`SQLITE3_NULL`** (<span class="type">integer</span>)  
<span class="simpara"> 表示 SQLite3 NULL 存储类。 </span>

**`SQLITE3_OPEN_READONLY`** (<span class="type">integer</span>)  
<span class="simpara"> 指定 SQLite3 数据库以只读模式打开。 </span>

**`SQLITE3_OPEN_READWRITE`** (<span class="type">integer</span>)  
<span class="simpara"> 指定 SQLite3 数据库以读写模式打开。 </span>

**`SQLITE3_OPEN_CREATE`** (<span class="type">integer</span>)  
<span class="simpara"> 指定 SQLite3 数据库若不存在，则创建并打开。
</span>

简介
----

实现与 SQLite 3 数据库对接的类。

类摘要
------

**SQLite3**

<span class="ooclass"> class **SQLite3** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">backup</span> ( <span class="methodparam"><span
class="type">SQLite3</span> `$destination_db`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$source_dbname`<span class="initializer"> = "main"</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$destination_dbname`<span class="initializer"> = "main"</span></span>
\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">busyTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$msecs`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">changes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = SQLITE3\_OPEN\_READWRITE \|
SQLITE3\_OPEN\_CREATE</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encryption_key`<span class="initializer"> =
""</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">createAggregate</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$step_callback`</span> , <span class="methodparam"><span
class="type">mixed</span> `$final_callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$argument_count`<span
class="initializer"> = -1</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">createCollation</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">createFunction</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$argument_count`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \]\] )

<span class="type">bool</span> <span
class="methodname">enableExceptions</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$enableExceptions`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">escapeString</span> ( <span class="methodparam"><span
class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exec</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">lastErrorCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">lastErrorMsg</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">lastInsertRowID</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">loadExtension</span> ( <span
class="methodparam"><span class="type">string</span>
`$shared_library`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = SQLITE3\_OPEN\_READWRITE \|
SQLITE3\_OPEN\_CREATE</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encryption_key`<span class="initializer"> =
""</span></span> \]\] )

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">openBlob</span> ( <span
class="methodparam"><span class="type">string</span> `$table`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column`</span> , <span class="methodparam"><span
class="type">int</span> `$rowid`</span> \[, <span
class="methodparam"><span class="type">string</span> `$dbname`<span
class="initializer"> = "main"</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = SQLITE3\_OPEN\_READONLY</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">SQLite3Stmt</span> <span class="methodname">prepare</span>
( <span class="methodparam"><span class="type">string</span>
`$query`</span> )

<span class="modifier">public</span> <span
class="type">SQLite3Result</span> <span class="methodname">query</span>
( <span class="methodparam"><span class="type">string</span>
`$query`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">querySingle</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$entire_row`<span class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">version</span> ( <span
class="methodparam">void</span> )

}

SQLite3::backup
===============

Backup one database to another database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::backup</span> ( <span
class="methodparam"><span class="type">SQLite3</span>
`$destination_db`</span> \[, <span class="methodparam"><span
class="type">string</span> `$source_dbname`<span class="initializer"> =
"main"</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$destination_dbname`<span
class="initializer"> = "main"</span></span> \]\] )

<span class="methodname">SQLite3::backup</span> copies the contents of
one database into another, overwriting the contents of the destination
database. It is useful either for creating backups of databases or for
copying in-memory databases to or from persistent files.

### 参数

`destination_db`  
A database connection opened with <span
class="methodname">SQLite3::open</span>.

`source_dbname`  
The database name is *"main"* for the main database, *"temp"* for the
temporary database, or the name specified after the *AS* keyword in an
*ATTACH* statement for an attached database.

`destination_dbname`  
Analogous to `source_dbname` but for the `destination_db`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Backup an existing database**

``` php
<?php
// $conn is a connection to an already opened sqlite3 database

$backup = new SQLite3('backup.sqlite');
$conn->backup($backup);
?>
```

SQLite3::busyTimeout
====================

Sets the busy connection handler

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::busyTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$msecs`</span> )

Sets a busy handler that will sleep until the database is not locked or
the timeout is reached.

### 参数

`msecs`  
The milliseconds to sleep. Setting this value to a value less than or
equal to zero, will turn off an already set timeout handler.

### 返回值

Returns **`TRUE`** on success, 或者在失败时返回 **`FALSE`**.

SQLite3::changes
================

Returns the number of database rows that were changed (or inserted or
deleted) by the most recent SQL statement

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLite3::changes</span> ( <span
class="methodparam">void</span> )

Returns the number of database rows that were changed (or inserted or
deleted) by the most recent SQL statement.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">integer</span> value corresponding to the
number of database rows changed (or inserted or deleted) by the most
recent SQL statement.

### 范例

**示例 \#1 <span class="function">SQLite3::changes</span> example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');

$query = $db->exec('UPDATE counter SET views=0 WHERE page="test"');
if ($query) {
    echo 'Number of rows modified: ', $db->changes();
}
?>
```

SQLite3::close
==============

Closes the database connection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::close</span> ( <span
class="methodparam">void</span> )

Closes the database connection.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">SQLite3::close</span> example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');
$db->close();
?>
```

SQLite3::\_\_construct
======================

Instantiates an SQLite3 object and opens an SQLite 3 database

### 说明

<span class="modifier">public</span> <span
class="methodname">SQLite3::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = SQLITE3\_OPEN\_READWRITE \|
SQLITE3\_OPEN\_CREATE</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encryption_key`<span class="initializer"> =
""</span></span> \]\] )

Instantiates an SQLite3 object and opens a connection to an SQLite 3
database. If the build includes encryption, then it will attempt to use
the key.

### 参数

`filename`  
Path to the SQLite database, or *:memory:* to use in-memory database. If
`filename` is an empty string, then a private, temporary on-disk
database will be created. This private database will be automatically
deleted as soon as the database connection is closed.

`flags`  
Optional flags used to determine how to open the SQLite database. By
default, open uses *SQLITE3\_OPEN\_READWRITE \| SQLITE3\_OPEN\_CREATE*.

-   *SQLITE3\_OPEN\_READONLY*: Open the database for reading only.

-   *SQLITE3\_OPEN\_READWRITE*: Open the database for reading and
    writing.

-   *SQLITE3\_OPEN\_CREATE*: Create the database if it does not exist.

`encryption_key`  
An optional encryption key used when encrypting and decrypting an SQLite
database. If the SQLite encryption module is not installed, this
parameter will have no effect.

### 返回值

Returns an SQLite3 object on success.

### 错误／异常

Throws an <span class="classname">Exception</span> on failure.

### 更新日志

| 版本   | 说明                                                                          |
|--------|-------------------------------------------------------------------------------|
| 7.0.10 | The `filename` can now be empty to use a private, temporary on-disk database. |

### 范例

**示例 \#1 <span class="function">SQLite3::\_\_construct</span>
example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE foo (bar TEXT)');
$db->exec("INSERT INTO foo (bar) VALUES ('This is a test')");

$result = $db->query('SELECT bar FROM foo');
var_dump($result->fetchArray());
?>
```

SQLite3::createAggregate
========================

Registers a PHP function for use as an SQL aggregate function

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::createAggregate</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$step_callback`</span> , <span class="methodparam"><span
class="type">mixed</span> `$final_callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$argument_count`<span
class="initializer"> = -1</span></span> \] )

Registers a PHP function or user-defined function for use as an SQL
aggregate function for use within SQL statements.

### 参数

`name`  
Name of the SQL aggregate to be created or redefined.

`step_callback`  
Callback function called for each row of the result set. Your PHP
function should accumulate the result and store it in the aggregation
context.

This function need to be defined as:

<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">step</span></span> ( <span class="methodparam"><span
class="type">mixed</span> `$context`</span> , <span
class="methodparam"><span class="type">int</span> `$rownumber`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value1`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \] )

`context`  
**`NULL`** for the first row; on subsequent rows it will have the value
that was previously returned from the step function; you should use this
to maintain the aggregate state.

`rownumber`  
The current row number.

`value1`  
The first argument passed to the aggregate.

`...`  
Further arguments passed to the aggregate.

The return value of this function will be used as the `context` argument
in the next call of the step or finalize functions.

`final_callback`  
Callback function to aggregate the "stepped" data from each row. Once
all the rows have been processed, this function will be called and it
should then take the data from the aggregation context and return the
result. This callback function should return a type understood by SQLite
(i.e.
<a href="/language/types/intro.html" class="link">scalar type</a>).

This function need to be defined as:

<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">fini</span></span> ( <span class="methodparam"><span
class="type">mixed</span> `$context`</span> , <span
class="methodparam"><span class="type">int</span> `$rownumber`</span> )

`context`  
Holds the return value from the very last call to the step function.

`rownumber`  
Always *0*.

The return value of this function will be used as the return value for
the aggregate.

`argument_count`  
The number of arguments that the SQL aggregate takes. If this parameter
is negative, then the SQL aggregate may take any number of arguments.

### 返回值

Returns **`TRUE`** upon successful creation of the aggregate,
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 max\_length aggregation function example**

``` php
<?php
$data = array(
   'one',
   'two',
   'three',
   'four',
   'five',
   'six',
   'seven',
   'eight',
   'nine',
   'ten',
   );
$db = new SQLite3(':memory:');
$db->exec("CREATE TABLE strings(a)");
$insert = $db->prepare('INSERT INTO strings VALUES (?)');
foreach ($data as $str) {
    $insert->bindValue(1, $str);
    $insert->execute();
}
$insert = null;

function max_len_step($context, $rownumber, $string)
{
    if (strlen($string) > $context) {
        $context = strlen($string);
    }
    return $context;
}

function max_len_finalize($context, $rownumber)
{
    return $context === null ? 0 : $context;
}

$db->createAggregate('max_len', 'max_len_step', 'max_len_finalize');

var_dump($db->querySingle('SELECT max_len(a) from strings'));
?>
```

以上例程会输出：

    int(5)

In this example, we are creating an aggregating function that will
calculate the length of the longest string in one of the columns of the
table. For each row, the *max\_len\_step* function is called and passed
a *$context* parameter. The context parameter is just like any other PHP
variable and be set to hold an array or even an object value. In this
example, we are simply using it to hold the maximum length we have seen
so far; if the *$string* has a length longer than the current maximum,
we update the context to hold this new maximum length.

After all of the rows have been processed, SQLite calls the
*max\_len\_finalize* function to determine the aggregate result. Here,
we could perform some kind of calculation based on the data found in the
*$context*. In our simple example though, we have been calculating the
result as the query progressed, so we simply need to return the context
value.

**小贴士**

It is NOT recommended for you to store a copy of the values in the
context and then process them at the end, as you would cause SQLite to
use a lot of memory to process the query - just think of how much memory
you would need if a million rows were stored in memory, each containing
a string 32 bytes in length.

**小贴士**

You can use <span class="methodname">SQLite3::createAggregate</span> to
override SQLite native SQL functions.

SQLite3::createCollation
========================

Registers a PHP function for use as an SQL collating function

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::createCollation</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Registers a PHP function or user-defined function for use as a collating
function within SQL statements.

### 参数

`name`  
Name of the SQL collating function to be created or redefined

`callback`  
The name of a PHP function or user-defined function to apply as a
callback, defining the behavior of the collation. It should accept two
values and return as <span class="function">strcmp</span> does, i.e. it
should return -1, 1, or 0 if the first string sorts before, sorts after,
or is equal to the second.

This function need to be defined as:

<span class="type">int</span> <span class="methodname"><span
class="replaceable">collation</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value1`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value2`</span> )

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">SQLite3::createCollation</span>
example**

Register the PHP function <span class="function">strnatcmp</span> as a
collating sequence in the SQLite3 database.

``` php
<?php

$db = new SQLite3(":memory:");
$db->exec("CREATE TABLE test (col1 string)");
$db->exec("INSERT INTO test VALUES ('a1')");
$db->exec("INSERT INTO test VALUES ('a10')");
$db->exec("INSERT INTO test VALUES ('a2')");

$db->createCollation('NATURAL_CMP', 'strnatcmp');

$defaultSort = $db->query("SELECT col1 FROM test ORDER BY col1");
$naturalSort = $db->query("SELECT col1 FROM test ORDER BY col1 COLLATE NATURAL_CMP");

echo "default:\n";
while ($row = $defaultSort->fetchArray()){
    echo $row['col1'], "\n";
}

echo "\nnatural:\n";
while ($row = $naturalSort->fetchArray()){
    echo $row['col1'], "\n";
}

$db->close();

?>
```

以上例程会输出：


    default:
    a1
    a10
    a2

    natural:
    a1
    a2
    a10

### 参见

-   The SQLite collation documentation:
    <a href="http://sqlite.org/datatype3.html#collation" class="link external">» http://sqlite.org/datatype3.html#collation</a>

SQLite3::createFunction
=======================

Registers a PHP function for use as an SQL scalar function

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::createFunction</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$argument_count`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \]\] )

Registers a PHP function or user-defined function for use as an SQL
scalar function for use within SQL statements.

### 参数

`name`  
Name of the SQL function to be created or redefined.

`callback`  
The name of a PHP function or user-defined function to apply as a
callback, defining the behavior of the SQL function.

This function need to be defined as:

<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value1`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

`value1`  
The first argument passed to the SQL function.

`...`  
Further arguments passed to the SQL function.

`argument_count`  
The number of arguments that the SQL function takes. If this parameter
is *-1*, then the SQL function may take any number of arguments.

`flags`  
A bitwise conjunction of flags. Currently, only
**`SQLITE3_DETERMINISTIC`** is supported, which specifies that the
function always returns the same result given the same inputs within a
single SQL statement.

### 返回值

Returns **`TRUE`** upon successful creation of the function, **`FALSE`**
on failure.

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.1.4 | The `flags` parameter has been added. |

### 范例

**示例 \#1 <span class="function">SQLite3::createFunction</span>
example**

``` php
<?php
function my_udf_md5($string) {
    return md5($string);
}

$db = new SQLite3('mysqlitedb.db');
$db->createFunction('my_udf_md5', 'my_udf_md5');

var_dump($db->querySingle('SELECT my_udf_md5("test")'));
?>
```

以上例程的输出类似于：

    string(32) "098f6bcd4621d373cade4e832627b4f6"

SQLite3::enableExceptions
=========================

Enable throwing exceptions

### 说明

<span class="type">bool</span> <span
class="methodname">SQLite3::enableExceptions</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$enableExceptions`<span class="initializer"> =
**`FALSE`**</span></span> \] )

Controls whether the <span class="classname">SQLite3</span> instance
will throw exceptions or warnings on error.

### 参数

`enable`  
When **`TRUE`**, the <span class="classname">SQLite3</span> instance,
and <span class="classname">SQLite3Stmt</span> and <span
class="classname">SQLite3Result</span> instances derived from it, will
throw exceptions on error.

When **`FALSE`**, the <span class="classname">SQLite3</span> instance,
and <span class="classname">SQLite3Stmt</span> and <span
class="classname">SQLite3Result</span> instances derived from it, will
raise warnings on error.

For either mode, the error code and message, if any, will be available
via <span class="methodname">SQLite3::lastErrorCode</span> and <span
class="methodname">SQLite3::lastErrorMsg</span> respectively.

### 返回值

Returns the old value; **`TRUE`** if exceptions were enabled,
**`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="methodname">SQLite3::enableExceptions</span>
example**

``` php
<?php
$sqlite = new SQLite3(':memory:');
try {
    $sqlite->exec('create table foo');
    $sqlite->enableExceptions(true);
    $sqlite->exec('create table bar');
} catch (Exception $e) {
    echo 'Caught exception: ' . $e->getMessage();
}
?>
```

以上例程的输出类似于：

    Warning: SQLite3::exec(): near "foo": syntax error in example.php on line 4
    Caught exception: near "bar": syntax error

SQLite3::escapeString
=====================

Returns a string that has been properly escaped

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">SQLite3::escapeString</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

Returns a string that has been properly escaped for safe inclusion in an
SQL statement.

**Warning**

此函数（还）不能安全地适用于二进制对象！

To properly handle BLOB fields which may contain NUL characters, use
<span class="function">SQLite3Stmt::bindParam</span> instead.

### 参数

`value`  
The string to be escaped.

### 返回值

Returns a properly escaped string that may be used safely in an SQL
statement.

### 注释

**Warning**

<span class="function">addslashes</span> should *NOT* be used to quote
your strings for SQLite queries; it will lead to strange results when
retrieving your data.

SQLite3::exec
=============

Executes a result-less query against a given database

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::exec</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

Executes a result-less query against a given database.

> **Note**: <span class="simpara"> SQLite3 may need to create
> <a href="https://sqlite.org/tempfiles.html" class="link external">» temporary files</a>
> during the execution of queries, so the respective directories may
> have to be writable. </span>

### 参数

`query`  
The SQL query to execute (typically an INSERT, UPDATE, or DELETE query).

### 返回值

Returns **`TRUE`** if the query succeeded, **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">SQLite3::exec</span> example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE bar (bar STRING)');
?>
```

SQLite3::lastErrorCode
======================

Returns the numeric result code of the most recent failed SQLite request

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLite3::lastErrorCode</span> ( <span
class="methodparam">void</span> )

Returns the numeric result code of the most recent failed SQLite
request.

### 参数

此函数没有参数。

### 返回值

Returns an integer value representing the numeric result code of the
most recent failed SQLite request.

SQLite3::lastErrorMsg
=====================

Returns English text describing the most recent failed SQLite request

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SQLite3::lastErrorMsg</span> ( <span
class="methodparam">void</span> )

Returns English text describing the most recent failed SQLite request.

### 参数

此函数没有参数。

### 返回值

Returns an English string describing the most recent failed SQLite
request.

SQLite3::lastInsertRowID
========================

Returns the row ID of the most recent INSERT into the database

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLite3::lastInsertRowID</span> ( <span
class="methodparam">void</span> )

Returns the row ID of the most recent INSERT into the database.

### 参数

此函数没有参数。

### 返回值

Returns the row ID of the most recent INSERT into the database

SQLite3::loadExtension
======================

Attempts to load an SQLite extension library

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3::loadExtension</span> ( <span
class="methodparam"><span class="type">string</span>
`$shared_library`</span> )

Attempts to load an SQLite extension library.

### 参数

`shared_library`  
The name of the library to load. The library must be located in the
directory specified in the configure option sqlite3.extension\_dir.

### 返回值

Returns **`TRUE`** if the extension is successfully loaded, **`FALSE`**
on failure.

### 范例

**示例 \#1 <span class="function">SQLite3::loadExtension</span>
example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');
$db->loadExtension('libagg.so');
?>
```

SQLite3::open
=============

Opens an SQLite database

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SQLite3::open</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = SQLITE3\_OPEN\_READWRITE \|
SQLITE3\_OPEN\_CREATE</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encryption_key`<span class="initializer"> =
""</span></span> \]\] )

Opens an SQLite 3 Database. If the build includes encryption, then it
will attempt to use the key.

### 参数

`filename`  
Path to the SQLite database, or *:memory:* to use in-memory database.

`flags`  
Optional flags used to determine how to open the SQLite database. By
default, open uses *SQLITE3\_OPEN\_READWRITE \| SQLITE3\_OPEN\_CREATE*.

-   *SQLITE3\_OPEN\_READONLY*: Open the database for reading only.

-   *SQLITE3\_OPEN\_READWRITE*: Open the database for reading and
    writing.

-   *SQLITE3\_OPEN\_CREATE*: Create the database if it does not exist.

`encryption_key`  
An optional encryption key used when encrypting and decrypting an SQLite
database. If the SQLite encryption module is not installed, this
parameter will have no effect.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">SQLite3::open</span> example**

``` php
<?php
/**
 * Simple example of extending the SQLite3 class and changing the __construct
 * parameters, then using the open method to initialize the DB.
 */
class MyDB extends SQLite3
{
    function __construct()
    {
        $this->open('mysqlitedb.db');
    }
}

$db = new MyDB();

$db->exec('CREATE TABLE foo (bar STRING)');
$db->exec("INSERT INTO foo (bar) VALUES ('This is a test')");

$result = $db->query('SELECT bar FROM foo');
var_dump($result->fetchArray());
?>
```

SQLite3::openBlob
=================

Opens a stream resource to read a BLOB

### 说明

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">SQLite3::openBlob</span> ( <span
class="methodparam"><span class="type">string</span> `$table`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column`</span> , <span class="methodparam"><span
class="type">int</span> `$rowid`</span> \[, <span
class="methodparam"><span class="type">string</span> `$dbname`<span
class="initializer"> = "main"</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = SQLITE3\_OPEN\_READONLY</span></span> \]\] )

Opens a stream resource to read or write a BLOB, which would be selected
by:

SELECT `column` FROM `dbname`.`table` WHERE rowid = `rowid`

> **Note**: <span class="simpara"> It is not possible to change the size
> of a BLOB by writing to the stream. Instead, an UPDATE statement has
> to be executed, possibly using SQLite's zeroblob() function to set the
> desired BLOB size. </span>

### 参数

`table`  
The table name.

`column`  
The column name.

`rowid`  
The row ID.

`dbname`  
The symbolic name of the DB

`flags`  
Either **`SQLITE3_OPEN_READONLY`** or **`SQLITE3_OPEN_READWRITE`** to
open the stream for reading only, or for reading and writing,
respectively.

### 返回值

Returns a stream resource, 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                                                |
|-------|-----------------------------------------------------------------------------------------------------|
| 7.2.0 | The `flags` parameter has been added, allowing to write BLOBs; formerly only reading was supported. |

### 范例

**示例 \#1 <span class="function">SQLite3::openBlob</span> example**

``` php
<?php
$conn = new SQLite3(':memory:');
$conn->exec('CREATE TABLE test (text text)');
$conn->exec("INSERT INTO test VALUES ('Lorem ipsum')");
$stream = $conn->openBlob('test', 'text', 1);
echo stream_get_contents($stream);
fclose($stream); // mandatory, otherwise the next line would fail
$conn->close();
?>
```

以上例程会输出：

    Lorem ipsum

**示例 \#2 Incrementally writing a BLOB**

``` php
<?php
$conn = new SQLite3(':memory:');
$conn->exec('CREATE TABLE test (text text)');
$conn->exec("INSERT INTO test VALUES (zeroblob(36))");
$stream = $conn->openBlob('test', 'text', 1, 'main', SQLITE3_OPEN_READWRITE);
for ($i = 0; $i < 3; $i++) {
    fwrite($stream,  "Lorem ipsum\n");
}
fclose($stream);
echo $conn->querySingle("SELECT text FROM test");
$conn->close();
?>
```

以上例程会输出：

    Lorem ipsum
    Lorem ipsum
    Lorem ipsum

SQLite3::prepare
================

Prepares an SQL statement for execution

### 说明

<span class="modifier">public</span> <span
class="type">SQLite3Stmt</span> <span
class="methodname">SQLite3::prepare</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

Prepares an SQL statement for execution and returns an <span
class="classname">SQLite3Stmt</span> object.

### 参数

`query`  
The SQL query to prepare.

### 返回值

Returns an <span class="classname">SQLite3Stmt</span> object on success
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">SQLite3::prepare</span> example**

``` php
<?php
unlink('mysqlitedb.db');
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE foo (id INTEGER, bar STRING)');
$db->exec("INSERT INTO foo (id, bar) VALUES (1, 'This is a test')");

$stmt = $db->prepare('SELECT bar FROM foo WHERE id=:id');
$stmt->bindValue(':id', 1, SQLITE3_INTEGER);

$result = $stmt->execute();
var_dump($result->fetchArray());
?>
```

### 参见

-   <span class="methodname">SQLite3Stmt::paramCount</span>
-   <span class="methodname">SQLite3Stmt::bindValue</span>
-   <span class="methodname">SQLite3Stmt::bindParam</span>

SQLite3::query
==============

Executes an SQL query

### 说明

<span class="modifier">public</span> <span
class="type">SQLite3Result</span> <span
class="methodname">SQLite3::query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

Executes an SQL query, returning an <span
class="classname">SQLite3Result</span> object. If the query does not
yield a result (such as DML statements) the returned <span
class="classname">SQLite3Result</span> object is not really usable. Use
<span class="methodname">SQLite3::exec</span> for such queries instead.

### 参数

`query`  
The SQL query to execute.

### 返回值

Returns an <span class="classname">SQLite3Result</span> object,
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">SQLite3::query</span> example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');

$results = $db->query('SELECT bar FROM foo');
while ($row = $results->fetchArray()) {
    var_dump($row);
}
?>
```

SQLite3::querySingle
====================

Executes a query and returns a single result

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SQLite3::querySingle</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$entire_row`<span class="initializer"> = **`FALSE`**</span></span> \] )

Executes a query and returns a single result.

### 参数

`query`  
The SQL query to execute.

`entire_row`  
By default, <span class="function">querySingle</span> returns the value
of the first column returned by the query. If `entire_row` is
**`TRUE`**, then it returns an array of the entire first row.

### 返回值

Returns the value of the first column of results or an array of the
entire first row (if `entire_row` is **`TRUE`**).

If the query is valid but no results are returned, then **`NULL`** will
be returned if `entire_row` is **`FALSE`**, otherwise an empty array is
returned.

Invalid or failing queries will return **`FALSE`**.

### 范例

**示例 \#1 <span class="function">SQLite3::querySingle</span> example**

``` php
<?php
$db = new SQLite3('mysqlitedb.db');

var_dump($db->querySingle('SELECT username FROM user WHERE userid=1'));
print_r($db->querySingle('SELECT username, email FROM user WHERE userid=1', true));
?>
```

以上例程的输出类似于：

    string(5) "Scott"
    Array
    (
        [username] => Scott
        [email] => scott@example.com
    )

SQLite3::version
================

Returns the SQLite3 library version as a string constant and as a number

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">SQLite3::version</span> ( <span
class="methodparam">void</span> )

Returns the SQLite3 library version as a string constant and as a
number.

### 参数

此函数没有参数。

### 返回值

Returns an associative array with the keys "versionString" and
"versionNumber".

### 范例

**示例 \#1 <span class="function">SQLite3::version</span> example**

``` php
<?php
print_r(SQLite3::version());
?>
```

以上例程的输出类似于：

    Array
    (
        [versionString] => 3.5.9
        [versionNumber] => 3005009
    )

简介
----

处理 SQLite 3 扩展语句模板的类。

类摘要
------

**SQLite3Stmt**

<span class="ooclass"> class **SQLite3Stmt** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">bindParam</span> ( <span
class="methodparam"><span class="type">mixed</span> `$sql_param`</span>
, <span class="methodparam"><span class="type">mixed</span>
`&$param`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">bindValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$sql_param`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">SQLite3Result</span> <span
class="methodname">execute</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSQL</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$expanded`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">paramCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">readOnly</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">reset</span> ( <span
class="methodparam">void</span> )

}

SQLite3Stmt::bindParam
======================

Binds a parameter to a statement variable

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Stmt::bindParam</span> ( <span
class="methodparam"><span class="type">mixed</span> `$sql_param`</span>
, <span class="methodparam"><span class="type">mixed</span>
`&$param`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`</span> \] )

Binds a parameter to a statement variable.

**Caution**

Before PHP 7.2.14 and 7.3.0, respectively, <span
class="methodname">SQLite3Stmt::reset</span> must be called after the
first call to <span class="methodname">SQLite3Stmt::execute</span> if
the bound value should be properly updated on following calls to <span
class="methodname">SQLite3Stmt::execute</span>. If <span
class="methodname">SQLite3Stmt::reset</span> is not called, the bound
value will not change, even if the value assigned to the variable passed
to <span class="methodname">SQLite3Stmt::bindParam</span> has changed,
or <span class="methodname">SQLite3Stmt::bindParam</span> has been
called again.

### 参数

`sql_param`  
Either a <span class="type">string</span> (for named parameters) or an
<span class="type">int</span> (for positional parameters) identifying
the statement variable to which the value should be bound. If a named
parameter does not start with a colon (*:*) or an at sign (*@*), a colon
(*:*) is automatically preprended. Positional parameters start with *1*.

`param`  
The parameter to bind to a statement variable.

`type`  
The data type of the parameter to bind.

-   **`SQLITE3_INTEGER`**: The value is a signed integer, stored in 1,
    2, 3, 4, 6, or 8 bytes depending on the magnitude of the value.

-   **`SQLITE3_FLOAT`**: The value is a floating point value, stored as
    an 8-byte IEEE floating point number.

-   **`SQLITE3_TEXT`**: The value is a text string, stored using the
    database encoding (UTF-8, UTF-16BE or UTF-16-LE).

-   **`SQLITE3_BLOB`**: The value is a blob of data, stored exactly as
    it was input.

-   **`SQLITE3_NULL`**: The value is a NULL value.

As of PHP 7.0.7, if `type` is omitted, it is automatically detected from
the type of the `param`: <span class="type">boolean</span> and <span
class="type">integer</span> are treated as **`SQLITE3_INTEGER`**, <span
class="type">float</span> as **`SQLITE3_FLOAT`**, <span
class="type">null</span> as **`SQLITE3_NULL`** and all others as
**`SQLITE3_TEXT`**. Formerly, if `type` has been omitted, it has
defaulted to **`SQLITE3_TEXT`**.

> **Note**:
>
> If `param` is **`NULL`**, it is always treated as **`SQLITE3_NULL`**,
> regardless of the given `type`.

### 返回值

Returns **`TRUE`** if the parameter is bound to the statement variable,
**`FALSE`** on failure.

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 7.4.0 | `sql_param` now also supports the *@param* notation. |

### 范例

**示例 \#1 <span class="function">SQLite3Stmt::bindParam</span> Usage**

This example shows how a single prepared statement with a single
parameter binding can be used to insert multiple rows with different
values.

``` php
<?php
$db = new SQLite3(':memory:');
$db->exec("CREATE TABLE foo (bar TEXT)");

$stmt = $db->prepare("INSERT INTO foo VALUES (:bar)");
$stmt->bindParam(':bar', $bar, SQLITE3_TEXT);

$bar = 'baz';
$stmt->execute();

$bar = 42;
$stmt->execute();

$res = $db->query("SELECT * FROM foo");
while (($row = $res->fetchArray(SQLITE3_ASSOC))) {
    var_dump($row);
}
?>
```

以上例程会输出：

    array(1) {
      ["bar"]=>
      string(3) "baz"
    }
    array(1) {
      ["bar"]=>
      string(2) "42"
    }

### 参见

-   <span class="methodname">SQLite3Stmt::bindValue</span>
-   <span class="methodname">SQLite3::prepare</span>

SQLite3Stmt::bindValue
======================

Binds the value of a parameter to a statement variable

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Stmt::bindValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$sql_param`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$type`</span> \] )

Binds the value of a parameter to a statement variable.

**Caution**

Before PHP 7.2.14 and 7.3.0, respectively, once the statement has been
executed, <span class="methodname">SQLite3Stmt::reset</span> needs to be
called to be able to change the value of bound parameters.

### 参数

`sql_param`  
Either a <span class="type">string</span> (for named parameters) or an
<span class="type">int</span> (for positional parameters) identifying
the statement variable to which the value should be bound. If a named
parameter does not start with a colon (*:*) or an at sign (*@*), a colon
(*:*) is automatically preprended. Positional parameters start with *1*.

`value`  
The value to bind to a statement variable.

`type`  
The data type of the value to bind.

-   **`SQLITE3_INTEGER`**: The value is a signed integer, stored in 1,
    2, 3, 4, 6, or 8 bytes depending on the magnitude of the value.

-   **`SQLITE3_FLOAT`**: The value is a floating point value, stored as
    an 8-byte IEEE floating point number.

-   **`SQLITE3_TEXT`**: The value is a text string, stored using the
    database encoding (UTF-8, UTF-16BE or UTF-16-LE).

-   **`SQLITE3_BLOB`**: The value is a blob of data, stored exactly as
    it was input.

-   **`SQLITE3_NULL`**: The value is a NULL value.

As of PHP 7.0.7, if `type` is omitted, it is automatically detected from
the type of the `value`: <span class="type">boolean</span> and <span
class="type">integer</span> are treated as **`SQLITE3_INTEGER`**, <span
class="type">float</span> as **`SQLITE3_FLOAT`**, <span
class="type">null</span> as **`SQLITE3_NULL`** and all others as
**`SQLITE3_TEXT`**. Formerly, if `type` has been omitted, it has
defaulted to **`SQLITE3_TEXT`**.

> **Note**:
>
> If `value` is **`NULL`**, it is always treated as **`SQLITE3_NULL`**,
> regardless of the given `type`.

### 返回值

Returns **`TRUE`** if the value is bound to the statement variable,
或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 7.4.0 | `sql_param` now also supports the *@param* notation. |

### 范例

**示例 \#1 <span class="function">SQLite3Stmt::bindValue</span>
example**

``` php
<?php
$db = new SQLite3(':memory:');

$db->exec('CREATE TABLE foo (id INTEGER, bar STRING)');
$db->exec("INSERT INTO foo (id, bar) VALUES (1, 'This is a test')");

$stmt = $db->prepare('SELECT bar FROM foo WHERE id=:id');
$stmt->bindValue(':id', 1, SQLITE3_INTEGER);

$result = $stmt->execute();
var_dump($result->fetchArray(SQLITE3_ASSOC));
?>
```

以上例程会输出：

    array(1) {
      ["bar"]=>
      string(14) "This is a test"
    }

### 参见

-   <span class="methodname">SQLite3Stmt::bindParam</span>
-   <span class="methodname">SQLite3::prepare</span>

SQLite3Stmt::clear
==================

Clears all current bound parameters

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Stmt::clear</span> ( <span
class="methodparam">void</span> )

Clears all current bound parameters (sets them to **`NULL`**).

**Caution**

This method needs to be used with <span
class="methodname">SQLite3Stmt::reset</span>. If used alone, any call to
<span class="methodname">SQLite3Stmt::bindValue</span> or <span
class="methodname">SQLite3Stmt::bindParam</span> will be of no effect
and all bound parameters will have the **`NULL`** value.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on successful clearing of bound parameters,
**`FALSE`** on failure.

SQLite3Stmt::close
==================

Closes the prepared statement

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Stmt::close</span> ( <span
class="methodparam">void</span> )

Closes the prepared statement.

> **Note**: <span class="simpara"> Note that all <span
> class="classname">SQLite3Result</span>s that have been retrieved by
> executing this statement will be invalidated when the statement is
> closed. </span>

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`**

SQLite3Stmt::execute
====================

Executes a prepared statement and returns a result set object

### 说明

<span class="modifier">public</span> <span
class="type">SQLite3Result</span> <span
class="methodname">SQLite3Stmt::execute</span> ( <span
class="methodparam">void</span> )

Executes a prepared statement and returns a result set object.

**Caution**

Result set objects retrieved by calling this method on the same
statement object are not independent, but rather share the same
underlying structure. Therefore it is recommended to call <span
class="methodname">SQLite3Result::finalize</span>, before calling <span
class="methodname">SQLite3Stmt::execute</span> on the same statement
object again.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="classname">SQLite3Result</span> object on
successful execution of the prepared statement, **`FALSE`** on failure.

### 参见

-   <span class="methodname">SQLite3::prepare</span>
-   <span class="methodname">SQLite3Stmt::bindValue</span>
-   <span class="methodname">SQLite3Stmt::bindParam</span>

SQLite3Stmt::getSQL
===================

Get the SQL of the statement

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SQLite3Stmt::getSQL</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$expanded`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieves the SQL of the prepared statement. If `expanded` is
**`FALSE`**, the unmodified SQL is retrieved. If `expanded` is
**`TRUE`**, all query parameters are replaced with their bound values,
or with an SQL *NULL*, if not already bound.

### 参数

`expanded`  
Whether to retrieve the expanded SQL. Passing **`TRUE`** is only
supported as of libsqlite 3.14.

### 返回值

Returns the SQL of the prepared statement, 或者在失败时返回 **`FALSE`**.

### 错误／异常

If `expanded` is **`TRUE`**, but the libsqlite version is less than
3.14, an error of level **`E_WARNING`** or an <span
class="classname">Exception</span> is issued, according to <span
class="methodname">SQLite3::enableExceptions</span>.

### 范例

**示例 \#1 Inspecting the expanded SQL**

``` php
<?php
$db = new SQLite3(':memory:');
$stmt = $db->prepare("SELECT :a, ?, :c");
$stmt->bindValue(':a', 'foo');
$answer = 42;
$stmt->bindParam(2, $answer);
var_dump($stmt->getSQL(true));
?>
```

以上例程的输出类似于：

    string(24) "SELECT 'foo', '42', NULL"

SQLite3Stmt::paramCount
=======================

Returns the number of parameters within the prepared statement

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLite3Stmt::paramCount</span> ( <span
class="methodparam">void</span> )

Returns the number of parameters within the prepared statement.

### 参数

此函数没有参数。

### 返回值

Returns the number of parameters within the prepared statement.

### 参见

-   <span class="methodname">SQLite3::prepare</span>

SQLite3Stmt::readOnly
=====================

Returns whether a statement is definitely read only

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Stmt::readOnly</span> ( <span
class="methodparam">void</span> )

Returns whether a statement is definitely read only. A statement is
considered read only, if it makes no *direct* changes to the content of
the database file. Note that user defined SQL functions might change the
database *indirectly* as a side effect.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if a statement is definitely read only, **`FALSE`**
otherwise.

SQLite3Stmt::reset
==================

Resets the prepared statement

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Stmt::reset</span> ( <span
class="methodparam">void</span> )

Resets the prepared statement to its state prior to execution. All
bindings remain intact after reset.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the statement is successfully reset,
或者在失败时返回 **`FALSE`**.

简介
----

处理 SQLite 3 扩展返回结果集的类。

类摘要
------

**SQLite3Result**

<span class="ooclass"> class **SQLite3Result** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">columnName</span> ( <span
class="methodparam"><span class="type">int</span>
`$column_number`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">columnType</span> ( <span class="methodparam"><span
class="type">int</span> `$column_number`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">fetchArray</span> (\[ <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = SQLITE3\_BOTH</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">finalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">numColumns</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">reset</span> ( <span
class="methodparam">void</span> )

}

SQLite3Result::columnName
=========================

Returns the name of the nth column

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SQLite3Result::columnName</span> ( <span
class="methodparam"><span class="type">int</span>
`$column_number`</span> )

Returns the name of the column specified by the `column_number`. Note
that the name of a result column is the value of the *AS* clause for
that column, if there is an *AS* clause. If there is no *AS* clause then
the name of the column is unspecified and may change from one release of
libsqlite3 to the next.

### 参数

`column_number`  
The numeric zero-based index of the column.

### 返回值

Returns the <span class="type">string</span> name of the column
identified by `column_number`.

SQLite3Result::columnType
=========================

Returns the type of the nth column

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLite3Result::columnType</span> ( <span
class="methodparam"><span class="type">int</span>
`$column_number`</span> )

Returns the type of the column identified by `column_number`.

### 参数

`column_number`  
The numeric zero-based index of the column.

### 返回值

Returns the data type index of the column identified by `column_number`
(one of **`SQLITE3_INTEGER`**, **`SQLITE3_FLOAT`**, **`SQLITE3_TEXT`**,
**`SQLITE3_BLOB`**, or **`SQLITE3_NULL`**).

SQLite3Result::fetchArray
=========================

Fetches a result row as an associative or numerically indexed array or
both

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SQLite3Result::fetchArray</span> (\[ <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = SQLITE3\_BOTH</span></span> \] )

Fetches a result row as an associative or numerically indexed array or
both. By default, fetches as both.

### 参数

`mode`  
Controls how the next row will be returned to the caller. This value
must be one of either *SQLITE3\_ASSOC*, *SQLITE3\_NUM*, or
*SQLITE3\_BOTH*.

-   *SQLITE3\_ASSOC*: returns an array indexed by column name as
    returned in the corresponding result set

-   *SQLITE3\_NUM*: returns an array indexed by column number as
    returned in the corresponding result set, starting at column 0

-   *SQLITE3\_BOTH*: returns an array indexed by both column name and
    number as returned in the corresponding result set, starting at
    column 0

### 返回值

Returns a result row as an associatively or numerically indexed array or
both. Alternately will return **`FALSE`** if there are no more rows.

The types of the values of the returned array are mapped from SQLite3
types as follows: integers are mapped to <span
class="type">integer</span> if they fit into the range
**`PHP_INT_MIN`**..**`PHP_INT_MAX`**, and to <span
class="type">string</span> otherwise. Floats are mapped to <span
class="type">float</span>, *NULL* values are mapped to <span
class="type">null</span>, and strings and blobs are mapped to <span
class="type">string</span>.

SQLite3Result::finalize
=======================

Closes the result set

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Result::finalize</span> ( <span
class="methodparam">void</span> )

Closes the result set.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`**.

SQLite3Result::numColumns
=========================

Returns the number of columns in the result set

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLite3Result::numColumns</span> ( <span
class="methodparam">void</span> )

Returns the number of columns in the result set.

### 参数

此函数没有参数。

### 返回值

Returns the number of columns in the result set.

SQLite3Result::reset
====================

Resets the result set back to the first row

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLite3Result::reset</span> ( <span
class="methodparam">void</span> )

Resets the result set back to the first row.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the result set is successfully reset back to the
first row, **`FALSE`** on failure.
