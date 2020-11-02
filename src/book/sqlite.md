SQLite
======

**目录**

-   [简介](/book/sqlite.html#简介)
-   [安装／配置](/book/sqlite.html#安装／配置)
    -   [需求](/book/sqlite.html#需求)
    -   [安装](/book/sqlite.html#安装)
    -   [运行时配置](/book/sqlite.html#运行时配置)
    -   [资源类型](/book/sqlite.html#资源类型)
-   [预定义常量](/book/sqlite.html#预定义常量)
-   [SQLite 函数](/book/sqlite.html#SQLite%20函数)
    -   [sqlite\_array\_query](/book/sqlite.html#sqlite_array_query) —
        Execute a query against a given database and returns an array
    -   [sqlite\_busy\_timeout](/book/sqlite.html#sqlite_busy_timeout) —
        Set busy timeout duration, or disable busy handlers
    -   [sqlite\_changes](/book/sqlite.html#sqlite_changes) — Returns
        the number of rows that were changed by the most recent SQL
        statement
    -   [sqlite\_close](/book/sqlite.html#sqlite_close) — Closes an open
        SQLite database
    -   [sqlite\_column](/book/sqlite.html#sqlite_column) — Fetches a
        column from the current row of a result set
    -   [sqlite\_create\_aggregate](/book/sqlite.html#sqlite_create_aggregate)
        — Register an aggregating UDF for use in SQL statements
    -   [sqlite\_create\_function](/book/sqlite.html#sqlite_create_function)
        — Registers a "regular" User Defined Function for use in SQL
        statements
    -   [sqlite\_current](/book/sqlite.html#sqlite_current) — Fetches
        the current row from a result set as an array
    -   [sqlite\_error\_string](/book/sqlite.html#sqlite_error_string) —
        Returns the textual description of an error code
    -   [sqlite\_escape\_string](/book/sqlite.html#sqlite_escape_string)
        — Escapes a string for use as a query parameter
    -   [sqlite\_exec](/book/sqlite.html#sqlite_exec) — Executes a
        result-less query against a given database
    -   [sqlite\_fetch\_all](/book/sqlite.html#sqlite_fetch_all) —
        Fetches all rows from a result set as an array of arrays
    -   [sqlite\_fetch\_array](/book/sqlite.html#sqlite_fetch_array) —
        Fetches the next row from a result set as an array
    -   [sqlite\_fetch\_single](/book/sqlite.html#sqlite_fetch_single) —
        Fetches the first column of a result set as a string
    -   [sqlite\_fetch\_string](/book/sqlite.html#sqlite_fetch_string) —
        别名 sqlite\_fetch\_single
    -   [sqlite\_field\_name](/book/sqlite.html#sqlite_field_name) —
        Returns the name of a particular field
    -   [sqlite\_has\_more](/book/sqlite.html#sqlite_has_more) — Finds
        whether or not more rows are available
    -   [sqlite\_last\_error](/book/sqlite.html#sqlite_last_error) —
        Returns the error code of the last error for a database
    -   [sqlite\_last\_insert\_rowid](/book/sqlite.html#sqlite_last_insert_rowid)
        — Returns the rowid of the most recently inserted row
    -   [sqlite\_libencoding](/book/sqlite.html#sqlite_libencoding) —
        Returns the encoding of the linked SQLite library
    -   [sqlite\_libversion](/book/sqlite.html#sqlite_libversion) —
        Returns the version of the linked SQLite library
    -   [sqlite\_next](/book/sqlite.html#sqlite_next) — Seek to the next
        row number
    -   [sqlite\_num\_fields](/book/sqlite.html#sqlite_num_fields) —
        Returns the number of fields in a result set
    -   [sqlite\_num\_rows](/book/sqlite.html#sqlite_num_rows) — Returns
        the number of rows in a buffered result set
    -   [sqlite\_open](/book/sqlite.html#sqlite_open) — Opens an SQLite
        database and create the database if it does not exist
    -   [sqlite\_popen](/book/sqlite.html#sqlite_popen) — Opens a
        persistent handle to an SQLite database and create the database
        if it does not exist
    -   [sqlite\_query](/book/sqlite.html#sqlite_query) — Executes a
        query against a given database and returns a result handle
    -   [sqlite\_rewind](/book/sqlite.html#sqlite_rewind) — Seek to the
        first row number
    -   [sqlite\_seek](/book/sqlite.html#sqlite_seek) — Seek to a
        particular row number of a buffered result set
    -   [sqlite\_single\_query](/book/sqlite.html#sqlite_single_query) —
        Executes a query and returns either an array for one single
        column or the value of the first row
    -   [sqlite\_udf\_decode\_binary](/book/sqlite.html#sqlite_udf_decode_binary)
        — Decode binary data passed as parameters to an UDF
    -   [sqlite\_udf\_encode\_binary](/book/sqlite.html#sqlite_udf_encode_binary)
        — Encode binary data before returning it from an UDF
    -   [sqlite\_unbuffered\_query](/book/sqlite.html#sqlite_unbuffered_query)
        — Execute a query that does not prefetch and buffer all data

This is an extension for the SQLite Embeddable SQL Database Engine.
SQLite is a C library that implements an embeddable SQL database engine.
Programs that link with the SQLite library can have SQL database access
without running a separate RDBMS process.

SQLite is not a client library used to connect to a big database server.
SQLite is the server. The SQLite library reads and writes directly to
and from the database files on disk.

> **Note**:
>
> For further information see the SQLite Website
> (<a href="http://sqlite.org/" class="link external">» http://sqlite.org/</a>).

> **Note**: <span class="simpara"> This extension offers support for
> SQLite 2.x. Sqlite 3.x is supported by the
> <a href="/book/sqlite3.html" class="link">SQLite3 extension</a>.
> </span>

安装／配置
==========

**目录**

-   [需求](/book/sqlite.html#需求)
-   [安装](/book/sqlite.html#安装)
-   [运行时配置](/book/sqlite.html#运行时配置)
-   [资源类型](/book/sqlite.html#资源类型)

需求
----

The SQLite extension is enabled by default as of PHP 5.0. Beginning with
PHP 5.4, the SQLite extension is available only via PECL.

安装
----

Since PHP 5.0 this extension was bundled with PHP. Beginning with PHP
5.4, this extension is available only via PECL.

Windows users must enable `php_sqlite.dll` inside of `php.ini` in order
to use these functions. PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

Windows builds must also enable PDO because as of PHP 5.1.0 it depends
on it. So, `php.ini` will end up with something like this:

``` ini
extension=php_pdo.dll
extension=php_sqlite.dll
```

On Linux or Unix operating systems, if you build PDO as a shared
extension, you must build SQLite as a shared extension using the
**--with-sqlite=shared** configure option.

The PHP 5.0.x series of Windows builds enabled this extension by
default, where no DLL file is necessary.

SQLite 3 is supported through
<a href="/book/pdo.html#SQLite%20(PDO)" class="link">PDO SQLite</a>.

> **Note**: **Windows installation for unprivileged accounts**  
>
> On Windows operating systems, unprivileged accounts don't have the
> `TMP` environment variable set by default. This will make sqlite
> create temporary files in the windows directory, which is not
> desirable. So, you should set the `TMP` environment variable for the
> web server or the user account the web server is running under. If
> Apache is your web server, you can accomplish this via a **SetEnv**
> directive in your `httpd.conf` file. For example:
>
> ``` apache-conf
> SetEnv TMP c:/temp
> ```
>
> If you are unable to establish this setting at the server level, you
> can implement the setting in your script:
>
> ``` php
> <?php
> putenv('TMP=C:/temp');
> ?>
> ```
>
> The setting must refer to a directory that the web server has
> permission to create files in and subsequently write to and delete the
> files it created. Otherwise, you may receive the following error
> message: <span class="computeroutput"> malformed database schema -
> unable to open a temporary database file for storing temporary tables
> </span>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                            | 默认 | 可修改范围    | Changelog                  |
|-----------------------------------------------------------------|------|---------------|----------------------------|
| <a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a> | "0"  | PHP\_INI\_ALL | Available since PHP 5.0.0. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`sqlite.assoc_case` <span class="type">int</span>  
Whether to use mixed case (*0*), upper case (*1*) or lower case (*2*)
hash indexes.

This option is primarily useful when you need compatibility with other
database systems, where the names of the columns are always returned as
uppercase or lowercase, regardless of the case of the actual field names
in the database schema.

The <span class="productname">SQLite</span> library returns the column
names in their natural case (that matches the case you used in your
schema). When `sqlite.assoc_case` is set to *0* the natural case will be
preserved. When it is set to *1* or *2*, PHP will apply case folding on
the hash keys to upper- or lower-case the keys, respectively.

Use of this option incurs a slight performance penalty, but is MUCH
faster than performing the case folding yourself using PHP script.

资源类型
--------

There are two resources used in the SQLite Interface. The first one is
the database connection, the second one the result set.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

The functions <span class="function">sqlite\_fetch\_array</span> and
<span class="function">sqlite\_current</span> use a constant for the
different types of result arrays. The following constants are defined:

**`SQLITE_ASSOC`** (<span class="type">int</span>)  
<span class="simpara"> Columns are returned into the array having the
field name as the array index. </span>

**`SQLITE_BOTH`** (<span class="type">int</span>)  
<span class="simpara"> Columns are returned into the array having both a
numerical index and the field name as the array index. </span>

**`SQLITE_NUM`** (<span class="type">int</span>)  
<span class="simpara"> Columns are returned into the array having a
numerical index to the fields. This index starts with 0, the first field
in the result. </span>

A number of functions may return status codes. The following constants
are defined:

**`SQLITE_OK`** (<span class="type">int</span>)  
<span class="simpara"> Successful result. </span>

**`SQLITE_ERROR`** (<span class="type">int</span>)  
<span class="simpara"> SQL error or missing database. </span>

**`SQLITE_INTERNAL`** (<span class="type">int</span>)  
<span class="simpara"> An internal logic error in SQLite. </span>

**`SQLITE_PERM`** (<span class="type">int</span>)  
<span class="simpara"> Access permission denied. </span>

**`SQLITE_ABORT`** (<span class="type">int</span>)  
<span class="simpara"> Callback routine requested an abort. </span>

**`SQLITE_BUSY`** (<span class="type">int</span>)  
<span class="simpara"> The database file is locked. </span>

**`SQLITE_LOCKED`** (<span class="type">int</span>)  
<span class="simpara"> A table in the database is locked. </span>

**`SQLITE_NOMEM`** (<span class="type">int</span>)  
<span class="simpara"> Memory allocation failed. </span>

**`SQLITE_READONLY`** (<span class="type">int</span>)  
<span class="simpara"> Attempt to write a readonly database. </span>

**`SQLITE_INTERRUPT`** (<span class="type">int</span>)  
<span class="simpara"> Operation terminated internally. </span>

**`SQLITE_IOERR`** (<span class="type">int</span>)  
<span class="simpara"> Disk I/O error occurred. </span>

**`SQLITE_NOTADB`** (<span class="type">int</span>)  
<span class="simpara"> File opened that is not a database file. </span>

**`SQLITE_CORRUPT`** (<span class="type">int</span>)  
<span class="simpara"> The database disk image is malformed. </span>

**`SQLITE_FORMAT`** (<span class="type">int</span>)  
<span class="simpara"> Auxiliary database format error. </span>

**`SQLITE_NOTFOUND`** (<span class="type">int</span>)  
<span class="simpara"> (Internal) Table or record not found. </span>

**`SQLITE_FULL`** (<span class="type">int</span>)  
<span class="simpara"> Insertion failed because database is full.
</span>

**`SQLITE_CANTOPEN`** (<span class="type">int</span>)  
<span class="simpara"> Unable to open the database file. </span>

**`SQLITE_PROTOCOL`** (<span class="type">int</span>)  
<span class="simpara"> Database lock protocol error. </span>

**`SQLITE_EMPTY`** (<span class="type">int</span>)  
<span class="simpara"> (Internal) Database table is empty. </span>

**`SQLITE_SCHEMA`** (<span class="type">int</span>)  
<span class="simpara"> The database schema changed. </span>

**`SQLITE_TOOBIG`** (<span class="type">int</span>)  
<span class="simpara"> Too much data for one row of a table. </span>

**`SQLITE_CONSTRAINT`** (<span class="type">int</span>)  
<span class="simpara"> Abort due to constraint violation. </span>

**`SQLITE_MISMATCH`** (<span class="type">int</span>)  
<span class="simpara"> Data type mismatch. </span>

**`SQLITE_MISUSE`** (<span class="type">int</span>)  
<span class="simpara"> Library used incorrectly. </span>

**`SQLITE_NOLFS`** (<span class="type">int</span>)  
<span class="simpara"> Uses of OS features not supported on host.
</span>

**`SQLITE_AUTH`** (<span class="type">int</span>)  
<span class="simpara"> Authorized failed. </span>

**`SQLITE_ROW`** (<span class="type">int</span>)  
<span class="simpara"> Internal process has another row ready. </span>

**`SQLITE_DONE`** (<span class="type">int</span>)  
<span class="simpara"> Internal process has finished executing. </span>

预定义类
--------

<span class="classname">SQLiteDatabase</span>
---------------------------------------------

Represents an opened SQLite database.

构造函数
--------

-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_open" class="link">__construct</a> -
    construct a new SQLiteDatabase object</span>

方法
----

-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_query" class="link">query</a> -
    Execute a query</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_exec" class="link">queryExec</a> -
    Execute a result-less query</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_array_query" class="link">arrayQuery</a> -
    Execute a query and return the result as an array</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_single_query" class="link">singleQuery</a> -
    Execute a query and return either an array for one single column or
    the value of the first row</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_unbuffered_query" class="link">unbufferedQuery</a> -
    Execute an unbuffered query</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_last_insert_rowid" class="link">lastInsertRowid</a> -
    Returns the rowid of the most recently inserted row</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_changes" class="link">changes</a> -
    Returns the number of rows changed by the most recent
    statement</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_create_aggregate" class="link">createAggregate</a> -
    Register an aggregating UDF for use in SQL statements</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_create_function" class="link">createFunction</a> -
    Register a UDF for use in SQL statements</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_busy_timeout" class="link">busyTimeout</a> -
    Sets or disables busy timeout duration</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_last_error" class="link">lastError</a> -
    Returns the last error code of the most recently encountered
    error</span>

<span class="classname">SQLiteResult</span>
-------------------------------------------

Represents a buffered SQLite result set.

方法
----

-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_fetch_array" class="link">fetch</a> -
    Fetches the next row from the result set as an array</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_fetch_single" class="link">fetchSingle</a> -
    Fetches the first column from the result set as a string</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_fetch_all" class="link">fetchAll</a> -
    Fetches all rows from the result set as an array of arrays</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_column" class="link">column</a> -
    Fetches a column from the current row of the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_num_fields" class="link">numFields</a> -
    Returns the number of fields in the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_field_name" class="link">fieldName</a> -
    Returns the name of a particular field in the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_current" class="link">current</a> -
    Fetches the current row from the result set as an array</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_next" class="link">next</a> -
    Seek to the next row number</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_rewind" class="link">rewind</a> -
    Seek to the first row number of the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_num_rows" class="link">numRows</a> -
    Returns the number of rows in the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_seek" class="link">seek</a> -
    Seek to a particular row number</span>

<span class="classname">SQLiteUnbuffered</span>
-----------------------------------------------

Represents an unbuffered SQLite result set. Unbuffered results sets are
sequential, forward-seeking only.

方法
----

-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_fetch_array" class="link">fetch</a> -
    Fetches the next row from the result set as an array</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_fetch_single" class="link">fetchSingle</a> -
    Fetches the first column from the result set as a string</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_fetch_all" class="link">fetchAll</a> -
    Fetches all rows from the result set as an array of arrays</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_column" class="link">column</a> -
    Fetches a column from the current row of the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_num_fields" class="link">numFields</a> -
    Returns the number of fields in the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_field_name" class="link">fieldName</a> -
    Returns the name of a particular field in the result set</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_current" class="link">current</a> -
    Fetches the current row from the result set as an array</span>
-   <span
    class="simpara"><a href="/book/sqlite.html#sqlite_next" class="link">next</a> -
    Seek to the next row number</span>

sqlite\_array\_query
====================

SQLiteDatabase::arrayQuery
==========================

Execute a query against a given database and returns an array

### 说明

<span class="type">array</span> <span
class="methodname">sqlite\_array\_query</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> , <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="type">array</span> <span
class="methodname">sqlite\_array\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$result_type`<span class="initializer"> =
SQLITE\_BOTH</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$decode_binary`<span class="initializer"> =
**`TRUE`**</span></span> \]\] )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SQLiteDatabase::arrayQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = SQLITE\_BOTH</span></span>
\[, <span class="methodparam"><span class="type">bool</span>
`$decode_binary`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

<span class="function">sqlite\_array\_query</span> executes the given
query and returns an array of the entire result set. It is similar to
calling <span class="function">sqlite\_query</span> and then <span
class="function">sqlite\_fetch\_array</span> for each row in the result
set. <span class="function">sqlite\_array\_query</span> is significantly
faster than the aforementioned.

**小贴士**

<span class="function">sqlite\_array\_query</span> is best suited to
queries returning 45 rows or less. If you have more data than that, it
is recommended that you write your scripts to use <span
class="function">sqlite\_unbuffered\_query</span> instead for more
optimal performance.

### 参数

`query`  
The query to be executed.

Data inside the query should be
<a href="/book/sqlite.html#sqlite_escape_string" class="link">properly escaped</a>.

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`result_type`  
可选的 `result_type` 参数接受常量，且决定返回的数组如何被索引。使用
**`SQLITE_ASSOC`** 会仅返回关联索引（已命名字段），而 **`SQLITE_NUM`**
会仅返回数值索引。**`SQLITE_BOTH`**
会同时返回关联和数值索引。**`SQLITE_BOTH`** 是此函数的默认值。

`decode_binary`  
当 `decode_binary` 参数设置为 **`TRUE`**（默认值）时，PHP 会解码那些由
<span class="function">sqlite\_escape\_string</span>
编码后的二进制数据。通常应保留此值为其默认值，除非要与其他使用 SQLlite
的应用程序建立的数据交互。

> **Note**: <span class="simpara">为兼容其他数据库扩展(比如
> MySQL)，支持两种可替代的语法。推荐第一种格式，函数的第一个参数是`dbhandle`。</span>

### 返回值

Returns an array of the entire result set; **`FALSE`** otherwise.

由 **`SQLITE_ASSOC`** 与 **`SQLITE_BOTH`** 返回的列名会依照
<a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a>
配置选项的值决定大小写。

### 范例

**示例 \#1 过程化风格**

``` php
<?php
$dbhandle = sqlite_open('sqlitedb');
$result = sqlite_array_query($dbhandle, 'SELECT name, email FROM users LIMIT 25', SQLITE_ASSOC);
foreach ($result as $entry) {
    echo 'Name: ' . $entry['name'] . '  E-mail: ' . $entry['email'];
}
?>
```

**示例 \#2 Object-oriented style**

``` php
<?php
$dbhandle = new SQLiteDatabase('sqlitedb');
$result = $dbhandle->arrayQuery('SELECT name, email FROM users LIMIT 25', SQLITE_ASSOC);
foreach ($result as $entry) {
    echo 'Name: ' . $entry['name'] . '  E-mail: ' . $entry['email'];
}
?>
```

### 参见

-   <span class="function">sqlite\_query</span>
-   <span class="function">sqlite\_fetch\_array</span>
-   <span class="function">sqlite\_fetch\_string</span>

sqlite\_busy\_timeout
=====================

SQLiteDatabase::busyTimeout
===========================

Set busy timeout duration, or disable busy handlers

### 说明

<span class="type">void</span> <span
class="methodname">sqlite\_busy\_timeout</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> , <span class="methodparam"><span
class="type">int</span> `$milliseconds`</span> )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SQLiteDatabase::busyTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$milliseconds`</span>
)

Set the maximum time, in milliseconds, that SQLite will wait for a
`dbhandle` to become ready for use.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`milliseconds`  
The number of milliseconds. When set to *0*, busy handlers will be
disabled and SQLite will return immediately with a *SQLITE\_BUSY* status
code if another process/thread has the database locked for an update.

PHP sets the default busy timeout to be 60 seconds when the database is
opened.

> **Note**:
>
> There are one thousand (1000) milliseconds in one second.

### 返回值

没有返回值。

### 范例

**示例 \#1 过程化风格**

``` php
<?php
$dbhandle = sqlite_open('sqlitedb');
sqlite_busy_timeout($dbhandle, 10000); // set timeout to 10 seconds
sqlite_busy_timeout($dbhandle, 0); // disable busy handler
?>
```

**示例 \#2 面向对象风格**

``` php
<?php
$dbhandle = new SQLiteDatabase('sqlitedb');
$dbhandle->busyTimeout(10000); // 10 seconds
$dbhandle->busyTimeout(0); // disable
?>
```

### 参见

-   <span class="function">sqlite\_open</span>

sqlite\_changes
===============

SQLiteDatabase::changes
=======================

Returns the number of rows that were changed by the most recent SQL
statement

### 说明

<span class="type">int</span> <span
class="methodname">sqlite\_changes</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLiteDatabase::changes</span> ( <span
class="methodparam">void</span> )

Returns the numbers of rows that were changed by the most recent SQL
statement executed against the `dbhandle` database handle.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

### 返回值

Returns the number of changed rows.

### 范例

**示例 \#1 过程化风格**

``` php
<?php
$dbhandle = sqlite_open('mysqlitedb');
$query = sqlite_query($dbhandle, "UPDATE users SET email='jDoe@example.com' WHERE username='jDoe'");
if (!$query) {
    exit('Error in query.');
} else {
    echo 'Number of rows modified: ', sqlite_changes($dbhandle);
}
?>
```

**示例 \#2 面向对象风格**

``` php
<?php
$dbhandle = new SQLiteDatabase('mysqlitedb');
$query = $dbhandle->query("UPDATE users SET email='jDoe@example.com' WHERE username='jDoe'");
if (!$query) {
    exit('Error in query.');
} else {
    echo 'Number of rows modified: ', $dbhandle->changes();
}
?>
```

### 参见

-   <span class="function">sqlite\_open</span>

sqlite\_close
=============

Closes an open SQLite database

### 说明

<span class="type">void</span> <span
class="methodname">sqlite\_close</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> )

Closes the given `db_handle` database handle. If the database was
persistent, it will be closed and removed from the persistent list.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">sqlite\_close</span> example**

``` php
<?php
$dbhandle = sqlite_open('sqlitedb');
sqlite_close($dbhandle);
?>
```

### 参见

-   <span class="function">sqlite\_open</span>
-   <span class="function">sqlite\_popen</span>

sqlite\_column
==============

SQLiteResult::column
====================

SQLiteUnbuffered::column
========================

Fetches a column from the current row of a result set

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlite\_column</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$index_or_name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$decode_binary`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="type">mixed</span> <span
class="methodname">SQLiteResult::column</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$index_or_name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$decode_binary`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="type">mixed</span> <span
class="methodname">SQLiteUnbuffered::column</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$index_or_name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$decode_binary`<span class="initializer"> =
**`TRUE`**</span></span> \] )

Fetches the value of a column named `index_or_name` (if it is a string),
or of the ordinal column numbered `index_or_name` (if it is an integer)
from the current row of the query result handle `result`.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

`index_or_name`  
The column index or name to fetch.

`decode_binary`  
当 `decode_binary` 参数设置为 **`TRUE`**（默认值）时，PHP 会解码那些由
<span class="function">sqlite\_escape\_string</span>
编码后的二进制数据。通常应保留此值为其默认值，除非要与其他使用 SQLlite
的应用程序建立的数据交互。

### 返回值

Returns the column value.

### 注释

> **Note**:
>
> Use this function when you are iterating a large result set with many
> columns, or with columns that contain large amounts of data.

### 参见

-   <span class="function">sqlite\_fetch\_string</span>

sqlite\_create\_aggregate
=========================

SQLiteDatabase::createAggregate
===============================

Register an aggregating UDF for use in SQL statements

### 说明

<span class="type">void</span> <span
class="methodname">sqlite\_create\_aggregate</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> , <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">callable</span>
`$step_func`</span> , <span class="methodparam"><span
class="type">callable</span> `$finalize_func`</span> \[, <span
class="methodparam"><span class="type">int</span> `$num_args`<span
class="initializer"> = -1</span></span> \] )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SQLiteDatabase::createAggregate</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$step_func`</span> , <span
class="methodparam"><span class="type">callable</span>
`$finalize_func`</span> \[, <span class="methodparam"><span
class="type">int</span> `$num_args`<span class="initializer"> =
-1</span></span> \] )

<span class="function">sqlite\_create\_aggregate</span> is similar to
<span class="function">sqlite\_create\_function</span> except that it
registers functions that can be used to calculate a result aggregated
across all the rows of a query.

The key difference between this function and <span
class="function">sqlite\_create\_function</span> is that two functions
are required to manage the aggregate; `step_func` is called for each row
of the result set. Your PHP function should accumulate the result and
store it into the aggregation context. Once all the rows have been
processed, `finalize_func` will be called and it should then take the
data from the aggregation context and return the result. Callback
functions should return a type understood by SQLite (i.e.
<a href="/language/types/intro.html" class="link">scalar type</a>).

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`function_name`  
The name of the function used in SQL statements.

`step_func`  
Callback function called for each row of the result set. Function
parameters are *&$context, $value, ...*.

`finalize_func`  
Callback function to aggregate the "stepped" data from each row.
Function parameter is *&$context* and the function should return the
final result of aggregation.

`num_args`  
Hint to the SQLite parser if the callback function accepts a
predetermined number of arguments.

### 返回值

没有返回值。

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
$dbhandle = sqlite_open(':memory:');
sqlite_query($dbhandle, "CREATE TABLE strings(a)");
foreach ($data as $str) {
    $str = sqlite_escape_string($str);
    sqlite_query($dbhandle, "INSERT INTO strings VALUES ('$str')");
}

function max_len_step(&$context, $string) 
{
    if (strlen($string) > $context) {
        $context = strlen($string);
    }
}

function max_len_finalize(&$context) 
{
    return $context;
}

sqlite_create_aggregate($dbhandle, 'max_len', 'max_len_step', 'max_len_finalize');

var_dump(sqlite_array_query($dbhandle, 'SELECT max_len(a) from strings'));

?>
```

In this example, we are creating an aggregating function that will
calculate the length of the longest string in one of the columns of the
table. For each row, the *max\_len\_step* function is called and passed
a `context` parameter. The context parameter is just like any other PHP
variable and be set to hold an array or even an object value. In this
example, we are simply using it to hold the maximum length we have seen
so far; if the `string` has a length longer than the current maximum, we
update the context to hold this new maximum length.

After all of the rows have been processed, SQLite calls the
*max\_len\_finalize* function to determine the aggregate result. Here,
we could perform some kind of calculation based on the data found in the
`context`. In our simple example though, we have been calculating the
result as the query progressed, so we simply need to return the context
value.

> **Note**:
>
> The example above will not work correctly if the column contains
> binary data. Take a look at the manual page for <span
> class="function">sqlite\_udf\_decode\_binary</span> for an explanation
> of why this is so, and an example of how to make it respect the binary
> encoding.

**小贴士**

It is NOT recommended for you to store a copy of the values in the
context and then process them at the end, as you would cause SQLite to
use a lot of memory to process the query - just think of how much memory
you would need if a million rows were stored in memory, each containing
a string 32 bytes in length.

**小贴士**

You can use <span class="function">sqlite\_create\_function</span> and
<span class="function">sqlite\_create\_aggregate</span> to override
SQLite native SQL functions.

### 参见

-   <span class="function">sqlite\_create\_function</span>
-   <span class="function">sqlite\_udf\_encode\_binary</span>
-   <span class="function">sqlite\_udf\_decode\_binary</span>

sqlite\_create\_function
========================

SQLiteDatabase::createFunction
==============================

Registers a "regular" User Defined Function for use in SQL statements

### 说明

<span class="type">void</span> <span
class="methodname">sqlite\_create\_function</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> , <span class="methodparam"><span
class="type">string</span> `$function_name`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$num_args`<span class="initializer"> =
-1</span></span> \] )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SQLiteDatabase::createFunction</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$num_args`<span
class="initializer"> = -1</span></span> \] )

<span class="function">sqlite\_create\_function</span> allows you to
register a PHP function with SQLite as an UDF (User Defined Function),
so that it can be called from within your SQL statements.

The UDF can be used in any SQL statement that can call functions, such
as SELECT and UPDATE statements and also in triggers.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`function_name`  
The name of the function used in SQL statements.

`callback`  
Callback function to handle the defined SQL function.

> **Note**: <span class="simpara"> Callback functions should return a
> type understood by SQLite (i.e.
> <a href="/language/types/intro.html" class="link">scalar type</a>).
> </span>

`num_args`  
Hint to the SQLite parser if the callback function accepts a
predetermined number of arguments.

> **Note**: <span class="simpara">为兼容其他数据库扩展(比如
> MySQL)，支持两种可替代的语法。推荐第一种格式，函数的第一个参数是`dbhandle`。</span>

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">sqlite\_create\_function</span>
example**

``` php
<?php
function md5_and_reverse($string) 
{
    return strrev(md5($string));
}

if ($dbhandle = sqlite_open('mysqlitedb', 0666, $sqliteerror)) {
    
    sqlite_create_function($dbhandle, 'md5rev', 'md5_and_reverse', 1);
    
    $sql  = 'SELECT md5rev(filename) FROM files';
    $rows = sqlite_array_query($dbhandle, $sql);
} else {
    echo 'Error opening sqlite db: ' . $sqliteerror;
    exit;
}
?>
```

In this example, we have a function that calculates the md5 sum of a
string, and then reverses it. When the SQL statement executes, it
returns the value of the filename transformed by our function. The data
returned in `$rows` contains the processed result.

The beauty of this technique is that you do not need to process the
result using a
<a href="/control-structures/foreach.html" class="link">foreach</a> loop
after you have queried for the data.

PHP registers a special function named *php* when the database is first
opened. The php function can be used to call any PHP function without
having to register it first.

**示例 \#2 Example of using the PHP function**

``` php
<?php
$rows = sqlite_array_query($dbhandle, "SELECT php('md5', filename) from files");
?>
```

This example will call the <span class="function">md5</span> on each
*filename* column in the database and return the result into `$rows`

> **Note**:
>
> For performance reasons, PHP will not automatically encode/decode
> binary data passed to and from your UDF's. You need to manually
> encode/decode the parameters and return values if you need to process
> binary data in this way. Take a look at <span
> class="function">sqlite\_udf\_encode\_binary</span> and <span
> class="function">sqlite\_udf\_decode\_binary</span> for more details.

**小贴士**

It is not recommended to use UDF's to handle processing of binary data,
unless high performance is not a key requirement of your application.

**小贴士**

You can use <span class="function">sqlite\_create\_function</span> and
<span class="function">sqlite\_create\_aggregate</span> to override
SQLite native SQL functions.

### 参见

-   <span class="function">sqlite\_create\_aggregate</span>

sqlite\_current
===============

SQLiteResult::current
=====================

SQLiteUnbuffered::current
=========================

Fetches the current row from a result set as an array

### 说明

<span class="type">array</span> <span
class="methodname">sqlite\_current</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = SQLITE\_BOTH</span></span>
\[, <span class="methodparam"><span class="type">bool</span>
`$decode_binary`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

面向对象风格 (method):

<span class="type">array</span> <span
class="methodname">SQLiteResult::current</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="type">array</span> <span
class="methodname">SQLiteUnbuffered::current</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="function">sqlite\_current</span> is identical to <span
class="function">sqlite\_fetch\_array</span> except that it does not
advance to the next row prior to returning the data; it returns the data
from the current position only.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

`result_type`  
可选的 `result_type` 参数接受常量，且决定返回的数组如何被索引。使用
**`SQLITE_ASSOC`** 会仅返回关联索引（已命名字段），而 **`SQLITE_NUM`**
会仅返回数值索引。**`SQLITE_BOTH`**
会同时返回关联和数值索引。**`SQLITE_BOTH`** 是此函数的默认值。

`decode_binary`  
当 `decode_binary` 参数设置为 **`TRUE`**（默认值）时，PHP 会解码那些由
<span class="function">sqlite\_escape\_string</span>
编码后的二进制数据。通常应保留此值为其默认值，除非要与其他使用 SQLlite
的应用程序建立的数据交互。

### 返回值

Returns an array of the current row from a result set; **`FALSE`** if
the current position is beyond the final row.

由 **`SQLITE_ASSOC`** 与 **`SQLITE_BOTH`** 返回的列名会依照
<a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a>
配置选项的值决定大小写。

### 参见

-   <span class="function">sqlite\_seek</span>
-   <span class="function">sqlite\_next</span>
-   <span class="function">sqlite\_fetch\_array</span>

sqlite\_error\_string
=====================

Returns the textual description of an error code

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_error\_string</span> ( <span
class="methodparam"><span class="type">int</span> `$error_code`</span> )

Returns a human readable description of the `error_code` returned from
<span class="function">sqlite\_last\_error</span>.

### 参数

`error_code`  
The error code being used, which might be passed in from <span
class="function">sqlite\_last\_error</span>.

### 返回值

Returns a human readable description of the `error_code`, as a <span
class="type">string</span>.

### 参见

-   <span class="function">sqlite\_last\_error</span>

sqlite\_escape\_string
======================

Escapes a string for use as a query parameter

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_escape\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$item`</span> )

<span class="function">sqlite\_escape\_string</span> will correctly
quote the string specified by `item` for use in an SQLite SQL statement.
This includes doubling up single-quote characters (*'*) and checking for
binary-unsafe characters in the query string.

Although the encoding makes it safe to insert the data, it will render
simple text comparisons and *LIKE* clauses in your queries unusable for
the columns that contain the binary data. In practice, this shouldn't be
a problem, as your schema should be such that you don't use such things
on binary columns (in fact, it might be better to store binary data
using other means, such as in files).

### 参数

`item`  
The <span class="type">string</span> being quoted.

If the `item` contains a *NUL* character, or if it begins with a
character whose ordinal value is *0x01*, PHP will apply a binary
encoding scheme so that you can safely store and retrieve binary data.

### 返回值

Returns an escaped <span class="type">string</span> for use in an SQLite
SQL statement.

### 注释

> **Note**: <span class="simpara"> Do not use this function to encode
> the return values from UDF's created using <span
> class="function">sqlite\_create\_function</span> or <span
> class="function">sqlite\_create\_aggregate</span> - use <span
> class="function">sqlite\_udf\_encode\_binary</span> instead. </span>

**Warning**

<span class="function">addslashes</span> should *NOT* be used to quote
your strings for SQLite queries; it will lead to strange results when
retrieving your data.

### 参见

-   <span class="function">sqlite\_udf\_encode\_binary</span>

sqlite\_exec
============

SQLiteDatabase::exec
====================

Executes a result-less query against a given database

### 说明

<span class="type">bool</span> <span
class="methodname">sqlite\_exec</span> ( <span class="methodparam"><span
class="type">resource</span> `$dbhandle`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$error_msg`</span> \] )

<span class="type">bool</span> <span
class="methodname">sqlite\_exec</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> , <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SQLiteDatabase::queryExec</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$error_msg`</span> \] )

Executes an SQL statement given by the `query` against a given database
handle (specified by the `dbhandle` parameter).

**Warning**

SQLite *will* execute multiple queries separated by semicolons, so you
can use it to execute a batch of SQL that you have loaded from a file or
have embedded in a script.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`query`  
The query to be executed.

Data inside the query should be
<a href="/book/sqlite.html#sqlite_escape_string" class="link">properly escaped</a>.

`error_msg`  
The specified variable will be filled if an error occurs. This is
specially important because SQL syntax errors can't be fetched using the
<span class="function">sqlite\_last\_error</span> function.

> **Note**: <span class="simpara">为兼容其他数据库扩展(比如
> MySQL)，支持两种可替代的语法。推荐第一种格式，函数的第一个参数是`dbhandle`。</span>

### 返回值

This function will return a boolean result; **`TRUE`** for success or
**`FALSE`** for failure. If you need to run a query that returns rows,
see <span class="function">sqlite\_query</span>.

由 **`SQLITE_ASSOC`** 与 **`SQLITE_BOTH`** 返回的列名会依照
<a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a>
配置选项的值决定大小写。

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 5.1.0 | Added the `error_msg` parameter |

### 范例

**示例 \#1 Procedural example**

``` php
<?php
$dbhandle = sqlite_open('mysqlitedb');
$query = sqlite_exec($dbhandle, "UPDATE users SET email='jDoe@example.com' WHERE username='jDoe'", $error);
if (!$query) {
    exit("Error in query: '$error'");
} else {
    echo 'Number of rows modified: ', sqlite_changes($dbhandle);
}
?>
```

**示例 \#2 Object-oriented example**

``` php
<?php
$dbhandle = new SQLiteDatabase('mysqlitedb');
$query = $dbhandle->queryExec("UPDATE users SET email='jDoe@example.com' WHERE username='jDoe'", $error);
if (!$query) {
    exit("Error in query: '$error'");
} else {
    echo 'Number of rows modified: ', $dbhandle->changes();
}
?>
```

### 参见

-   <span class="function">sqlite\_query</span>
-   <span class="function">sqlite\_unbuffered\_query</span>
-   <span class="function">sqlite\_array\_query</span>

sqlite\_fetch\_all
==================

SQLiteResult::fetchAll
======================

SQLiteUnbuffered::fetchAll
==========================

Fetches all rows from a result set as an array of arrays

### 说明

<span class="type">array</span> <span
class="methodname">sqlite\_fetch\_all</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = SQLITE\_BOTH</span></span>
\[, <span class="methodparam"><span class="type">bool</span>
`$decode_binary`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

面向对象风格 (method):

<span class="type">array</span> <span
class="methodname">SQLiteResult::fetchAll</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="type">array</span> <span
class="methodname">SQLiteUnbuffered::fetchAll</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="function">sqlite\_fetch\_all</span> returns an array of the
entire result set from the `result` resource. It is similar to calling
<span class="function">sqlite\_query</span> (or <span
class="function">sqlite\_unbuffered\_query</span>) and then <span
class="function">sqlite\_fetch\_array</span> for each row in the result
set.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

`result_type`  
可选的 `result_type` 参数接受常量，且决定返回的数组如何被索引。使用
**`SQLITE_ASSOC`** 会仅返回关联索引（已命名字段），而 **`SQLITE_NUM`**
会仅返回数值索引。**`SQLITE_BOTH`**
会同时返回关联和数值索引。**`SQLITE_BOTH`** 是此函数的默认值。

`decode_binary`  
当 `decode_binary` 参数设置为 **`TRUE`**（默认值）时，PHP 会解码那些由
<span class="function">sqlite\_escape\_string</span>
编码后的二进制数据。通常应保留此值为其默认值，除非要与其他使用 SQLlite
的应用程序建立的数据交互。

### 返回值

Returns an array of the remaining rows in a result set. If called right
after <span class="function">sqlite\_query</span>, it returns all rows.
If called after <span class="function">sqlite\_fetch\_array</span>, it
returns the rest. If there are no rows in a result set, it returns an
empty array.

由 **`SQLITE_ASSOC`** 与 **`SQLITE_BOTH`** 返回的列名会依照
<a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a>
配置选项的值决定大小写。

### 范例

**示例 \#1 Procedural example**

``` php
<?php
$dbhandle = sqlite_open('sqlitedb');
$query = sqlite_query($dbhandle, 'SELECT name, email FROM users LIMIT 25');
$result = sqlite_fetch_all($query, SQLITE_ASSOC);
foreach ($result as $entry) {
    echo 'Name: ' . $entry['name'] . '  E-mail: ' . $entry['email'];
}
?>
```

**示例 \#2 Object-oriented example**

``` php
<?php
$dbhandle = new SQLiteDatabase('sqlitedb');

$query = $dbhandle->query('SELECT name, email FROM users LIMIT 25'); // buffered result set
$query = $dbhandle->unbufferedQuery('SELECT name, email FROM users LIMIT 25'); // unbuffered result set

$result = $query->fetchAll(SQLITE_ASSOC);
foreach ($result as $entry) {
    echo 'Name: ' . $entry['name'] . '  E-mail: ' . $entry['email'];
}
?>
```

### 参见

-   <span class="function">sqlite\_fetch\_array</span>

sqlite\_fetch\_array
====================

SQLiteResult::fetch
===================

SQLiteUnbuffered::fetch
=======================

Fetches the next row from a result set as an array

### 说明

<span class="type">array</span> <span
class="methodname">sqlite\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = SQLITE\_BOTH</span></span>
\[, <span class="methodparam"><span class="type">bool</span>
`$decode_binary`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

面向对象风格 (method):

<span class="type">array</span> <span
class="methodname">SQLiteResult::fetch</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="type">array</span> <span
class="methodname">SQLiteUnbuffered::fetch</span> (\[ <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

Fetches the next row from the given `result` handle. If there are no
more rows, returns **`FALSE`**, otherwise returns an associative array
representing the row data.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

`result_type`  
可选的 `result_type` 参数接受常量，且决定返回的数组如何被索引。使用
**`SQLITE_ASSOC`** 会仅返回关联索引（已命名字段），而 **`SQLITE_NUM`**
会仅返回数值索引。**`SQLITE_BOTH`**
会同时返回关联和数值索引。**`SQLITE_BOTH`** 是此函数的默认值。

`decode_binary`  
当 `decode_binary` 参数设置为 **`TRUE`**（默认值）时，PHP 会解码那些由
<span class="function">sqlite\_escape\_string</span>
编码后的二进制数据。通常应保留此值为其默认值，除非要与其他使用 SQLlite
的应用程序建立的数据交互。

### 返回值

Returns an array of the next row from a result set; **`FALSE`** if the
next position is beyond the final row.

由 **`SQLITE_ASSOC`** 与 **`SQLITE_BOTH`** 返回的列名会依照
<a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a>
配置选项的值决定大小写。

### 范例

**示例 \#1 Procedural example**

``` php
<?php
$dbhandle = sqlite_open('sqlitedb');
$query = sqlite_query($dbhandle, 'SELECT name, email FROM users LIMIT 25');
while ($entry = sqlite_fetch_array($query, SQLITE_ASSOC)) {
    echo 'Name: ' . $entry['name'] . '  E-mail: ' . $entry['email'];
}
?>
```

**示例 \#2 Object-oriented example**

``` php
<?php
$dbhandle = new SQLiteDatabase('sqlitedb');

$query = $dbhandle->query('SELECT name, email FROM users LIMIT 25'); // buffered result set
$query = $dbhandle->unbufferedQuery('SELECT name, email FROM users LIMIT 25'); // unbuffered result set

while ($entry = $query->fetch(SQLITE_ASSOC)) {
    echo 'Name: ' . $entry['name'] . '  E-mail: ' . $entry['email'];
}
?>
```

### 参见

-   <span class="function">sqlite\_array\_query</span>
-   <span class="function">sqlite\_fetch\_string</span>

sqlite\_fetch\_single
=====================

SQLiteResult::fetchSingle
=========================

SQLiteUnbuffered::fetchSingle
=============================

Fetches the first column of a result set as a string

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_fetch\_single</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$decode_binary`<span class="initializer"> = **`TRUE`**</span></span> \]
)

面向对象风格 (method):

<span class="type">string</span> <span
class="methodname">SQLiteResult::fetchSingle</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="type">string</span> <span
class="methodname">SQLiteUnbuffered::fetchSingle</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$decode_binary`<span
class="initializer"> = **`TRUE`**</span></span> \] )

<span class="function">sqlite\_fetch\_single</span> is identical to
<span class="function">sqlite\_fetch\_array</span> except that it
returns the value of the first column of the rowset.

This is the most optimal way to retrieve data when you are only
interested in the values from a single column of data.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

`decode_binary`  
当 `decode_binary` 参数设置为 **`TRUE`**（默认值）时，PHP 会解码那些由
<span class="function">sqlite\_escape\_string</span>
编码后的二进制数据。通常应保留此值为其默认值，除非要与其他使用 SQLlite
的应用程序建立的数据交互。

### 返回值

Returns the first column value, as a string.

### 范例

**示例 \#1 A <span class="function">sqlite\_fetch\_single</span>
example**

``` php
<?php
if ($dbhandle = sqlite_open('mysqlitedb', 0666, $sqliteerror)) {

    $sql = "SELECT id FROM sometable WHERE id = 42";
    $res = sqlite_query($dbhandle, $sql);

    if (sqlite_num_rows($res) > 0) {
        echo sqlite_fetch_single($res); // 42
    }
    
    sqlite_close($dbhandle);
}
?>
```

### 参见

-   <span class="function">sqlite\_fetch\_array</span>

sqlite\_fetch\_string
=====================

别名 <span class="function">sqlite\_fetch\_single</span>

### 说明

此函数是该函数的别名： <span
class="function">sqlite\_fetch\_single</span>.

sqlite\_field\_name
===================

SQLiteResult::fieldName
=======================

SQLiteUnbuffered::fieldName
===========================

Returns the name of a particular field

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_index`</span> )

面向对象风格 (method):

<span class="type">string</span> <span
class="methodname">SQLiteResult::fieldName</span> ( <span
class="methodparam"><span class="type">int</span> `$field_index`</span>
)

<span class="type">string</span> <span
class="methodname">SQLiteUnbuffered::fieldName</span> ( <span
class="methodparam"><span class="type">int</span> `$field_index`</span>
)

Given the ordinal column number, `field_index`, <span
class="function">sqlite\_field\_name</span> returns the name of that
field in the result set `result`.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

`field_index`  
The ordinal column number in the result set.

### 返回值

Returns the name of a field in an SQLite result set, given the ordinal
column number; **`FALSE`** on error.

由 **`SQLITE_ASSOC`** 与 **`SQLITE_BOTH`** 返回的列名会依照
<a href="/book/sqlite.html#" class="link">sqlite.assoc_case</a>
配置选项的值决定大小写。

sqlite\_has\_more
=================

Finds whether or not more rows are available

### 说明

<span class="type">bool</span> <span
class="methodname">sqlite\_has\_more</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Finds whether more rows are available from the given result set.

### 参数

`result`  
The SQLite result resource.

### 返回值

Returns **`TRUE`** if there are more rows available from the `result`
handle, or **`FALSE`** otherwise.

### 参见

-   <span class="function">sqlite\_num\_rows</span>
-   <span class="function">sqlite\_changes</span>

sqlite\_last\_error
===================

SQLiteDatabase::lastError
=========================

Returns the error code of the last error for a database

### 说明

<span class="type">int</span> <span
class="methodname">sqlite\_last\_error</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLiteDatabase::lastError</span> ( <span
class="methodparam">void</span> )

Returns the error code from the last operation performed on `dbhandle`
(the database handle), or *0* when no error occurred. A human readable
description of the error code can be retrieved using <span
class="function">sqlite\_error\_string</span>.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

### 返回值

Returns an error code, or 0 if no error occurred.

### 参见

-   <span class="function">sqlite\_error\_string</span>

sqlite\_last\_insert\_rowid
===========================

SQLiteDatabase::lastInsertRowid
===============================

Returns the rowid of the most recently inserted row

### 说明

<span class="type">int</span> <span
class="methodname">sqlite\_last\_insert\_rowid</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SQLiteDatabase::lastInsertRowid</span> ( <span
class="methodparam">void</span> )

Returns the rowid of the row that was most recently inserted into the
database `dbhandle`, if it was created as an auto-increment field.

**小贴士**

You can create auto-increment fields in SQLite by declaring them as
*INTEGER PRIMARY KEY* in your table schema.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

### 返回值

Returns the row id, as an integer.

sqlite\_libencoding
===================

Returns the encoding of the linked SQLite library

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_libencoding</span> ( <span
class="methodparam">void</span> )

The SQLite library may be compiled in either *ISO-8859-1* or *UTF-8*
compatible modes. This function allows you to determine which encoding
scheme is used by your version of the library.

**Warning**

The default PHP distribution builds `libsqlite` in *ISO-8859-1* encoding
mode. However, this is a misnomer; rather than handling *ISO-8859-1*, it
operates according to your current locale settings for string
comparisons and sort ordering. So, rather than *ISO-8859-1*, you should
think of it as being '*8-bit*' instead.

When compiled with *UTF-8* support, sqlite handles encoding and decoding
of *UTF-8* multi-byte character sequences, but does not yet do a
complete job when working with the data (no normalization is performed
for example), and some comparison operations may still not be carried
out correctly.

**Warning**

It is not recommended that you use PHP in a web-server configuration
with a version of the SQLite library compiled with *UTF-8* support,
since `libsqlite` will abort the process if it detects a problem with
the *UTF-8* encoding.

### 返回值

Returns the library encoding.

### 参见

-   <span class="function">sqlite\_libversion</span>

sqlite\_libversion
==================

Returns the version of the linked SQLite library

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_libversion</span> ( <span
class="methodparam">void</span> )

Returns the version of the linked SQLite library.

### 返回值

Returns the library version, as a string.

### 参见

-   <span class="function">sqlite\_libencoding</span>

sqlite\_next
============

SQLiteResult::next
==================

SQLiteUnbuffered::next
======================

Seek to the next row number

### 说明

<span class="type">bool</span> <span
class="methodname">sqlite\_next</span> ( <span class="methodparam"><span
class="type">resource</span> `$result`</span> )

面向对象风格 (method):

<span class="type">bool</span> <span
class="methodname">SQLiteResult::next</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">SQLiteUnbuffered::next</span> ( <span
class="methodparam">void</span> )

<span class="function">sqlite\_next</span> advances the result handle
`result` to the next row.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

### 返回值

Returns **`TRUE`** on success, or **`FALSE`** if there are no more rows.

### 参见

-   <span class="function">sqlite\_seek</span>
-   <span class="function">sqlite\_current</span>
-   <span class="function">sqlite\_rewind</span>

sqlite\_num\_fields
===================

SQLiteResult::numFields
=======================

SQLiteUnbuffered::numFields
===========================

Returns the number of fields in a result set

### 说明

<span class="type">int</span> <span
class="methodname">sqlite\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格 (method):

<span class="type">int</span> <span
class="methodname">SQLiteResult::numFields</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">SQLiteUnbuffered::numFields</span> ( <span
class="methodparam">void</span> )

Returns the number of fields in the `result` set.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

### 返回值

Returns the number of fields, as an integer.

### 参见

-   <span class="function">sqlite\_changes</span>
-   <span class="function">sqlite\_num\_rows</span>

sqlite\_num\_rows
=================

SQLiteResult::numRows
=====================

Returns the number of rows in a buffered result set

### 说明

<span class="type">int</span> <span
class="methodname">sqlite\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格 (method):

<span class="type">int</span> <span
class="methodname">SQLiteResult::numRows</span> ( <span
class="methodparam">void</span> )

Returns the number of rows in the buffered `result` set.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

> **Note**:
>
> 此函数不能用于未缓冲的结果句柄。

### 返回值

Returns the number of rows, as an integer.

### 范例

**示例 \#1 Procedural example**

``` php
<?php
$db = sqlite_open('mysqlitedb');
$result = sqlite_query($db, "SELECT * FROM mytable WHERE name='John Doe'");
$rows = sqlite_num_rows($result);

echo "Number of rows: $rows";
?>
```

**示例 \#2 Object-oriented example**

``` php
<?php
$db = new SQLiteDatabase('mysqlitedb');
$result = $db->query("SELECT * FROM mytable WHERE name='John Doe'");
$rows = $result->numRows();

echo "Number of rows: $rows";
?>
```

### 参见

-   <span class="function">sqlite\_changes</span>
-   <span class="function">sqlite\_query</span>
-   <span class="function">sqlite\_num\_fields</span>

sqlite\_open
============

Opens an SQLite database and create the database if it does not exist

### 说明

<span class="type">resource</span> <span
class="methodname">sqlite\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0666</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`&$error_message`</span> \]\] )

面向对象风格 (constructor):

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">SQLiteDatabase::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0666</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`&$error_message`</span> \]\] )

Opens an SQLite database or creates the database if it does not exist.

### 参数

`filename`  
The filename of the SQLite database. If the file does not exist, SQLite
will attempt to create it. PHP must have write permissions to the file
if data is inserted, the database schema is modified or to create the
database if it does not exist.

`mode`  
The mode of the file. Intended to be used to open the database in
read-only mode. Presently, this parameter is ignored by the sqlite
library. The default value for mode is the octal value *0666* and this
is the recommended value.

`error_message`  
Passed by reference and is set to hold a descriptive error message
explaining why the database could not be opened if there was an error.

### 返回值

Returns a resource (database handle) on success, **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">sqlite\_open</span> example**

``` php
<?php
if ($db = sqlite_open('mysqlitedb', 0666, $sqliteerror)) { 
    sqlite_query($db, 'CREATE TABLE foo (bar varchar(10))');
    sqlite_query($db, "INSERT INTO foo VALUES ('fnord')");
    $result = sqlite_query($db, 'select bar from foo');
    var_dump(sqlite_fetch_array($result)); 
} else {
    die($sqliteerror);
}
?>
```

### 注释

**小贴士**

On Unix platforms, SQLite is sensitive to scripts that use the fork()
system call. If you do have such a script, it is recommended that you
close the handle prior to forking and then re-open it in the child
and/or parent. For more information on this issue, see
<a href="http://sqlite.org/c_interface.html" class="link external">» The C language interface to the SQLite library</a>
in the section entitled *Multi-Threading And SQLite*.

**小贴士**

It is not recommended to work with SQLite databases mounted on NFS
partitions. Since NFS is notoriously bad when it comes to locking you
may find that you cannot even open the database at all, and if it
succeeds, the locking behaviour may be undefined.

> **Note**: <span class="simpara"> Starting with SQLite library version
> 2.8.2, you can specify *:memory:* as the `filename` to create a
> database that lives only in the memory of the computer. This is useful
> mostly for temporary processing, as the in-memory database will be
> destroyed when the process ends. It can also be useful when coupled
> with the *ATTACH DATABASE* SQL statement to load other databases and
> move and query data between them. </span>

> **Note**: <span class="simpara"> SQLite is open\_basedir aware.
> </span>

### 参见

-   <span class="function">sqlite\_popen</span>
-   <span class="function">sqlite\_close</span>
-   <span class="function">sqlite\_factory</span>

sqlite\_popen
=============

Opens a persistent handle to an SQLite database and create the database
if it does not exist

### 说明

<span class="type">resource</span> <span
class="methodname">sqlite\_popen</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0666</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`&$error_message`</span> \]\] )

This function behaves identically to <span
class="function">sqlite\_open</span> except that is uses the persistent
resource mechanism of PHP. For information about the meaning of the
parameters, read the <span class="function">sqlite\_open</span> manual
page.

<span class="function">sqlite\_popen</span> will first check to see if a
persistent handle has already been opened for the given `filename`. If
it finds one, it returns that handle to your script, otherwise it opens
a fresh handle to the database.

The benefit of this approach is that you don't incur the performance
cost of re-reading the database and index schema on each page hit served
by persistent web server SAPI's (any SAPI except for regular CGI or
CLI).

> **Note**: <span class="simpara"> If you use persistent handles and
> have the database updated by a background process (perhaps via a
> crontab), and that process re-creates the database by overwriting it
> (either by unlinking and rebuilding, or moving the updated version to
> replace the current version), you may experience undefined behaviour
> when a persistent handle on the old version of the database is
> recycled. </span> <span class="simpara"> To avoid this situation, have
> your background processes open the same database file and perform
> their updates in a transaction. </span>

### 参数

`filename`  
The filename of the SQLite database. If the file does not exist, SQLite
will attempt to create it. PHP must have write permissions to the file
if data is inserted, the database schema is modified or to create the
database if it does not exist.

`mode`  
The mode of the file. Intended to be used to open the database in
read-only mode. Presently, this parameter is ignored by the sqlite
library. The default value for mode is the octal value *0666* and this
is the recommended value.

`error_message`  
Passed by reference and is set to hold a descriptive error message
explaining why the database could not be opened if there was an error.

### 返回值

Returns a resource (database handle) on success, **`FALSE`** on error.

### 参见

-   <span class="function">sqlite\_open</span>
-   <span class="function">sqlite\_close</span>
-   <span class="function">sqlite\_factory</span>

sqlite\_query
=============

SQLiteDatabase::query
=====================

Executes a query against a given database and returns a result handle

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">sqlite\_query</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> , <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`&$error_msg`</span> \]\] )

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">sqlite\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$result_type`<span class="initializer"> =
SQLITE\_BOTH</span></span> \[, <span class="methodparam"><span
class="type">string</span> `&$error_msg`</span> \]\] )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type"><span
class="type">SQLiteResult</span><span class="type">false</span></span>
<span class="methodname">SQLiteDatabase::query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = SQLITE\_BOTH</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`&$error_msg`</span> \]\] )

Executes an SQL statement given by the `query` against a given database
handle.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`query`  
The query to be executed.

Data inside the query should be
<a href="/book/sqlite.html#sqlite_escape_string" class="link">properly escaped</a>.

`result_type`  
可选的 `result_type` 参数接受常量，且决定返回的数组如何被索引。使用
**`SQLITE_ASSOC`** 会仅返回关联索引（已命名字段），而 **`SQLITE_NUM`**
会仅返回数值索引。**`SQLITE_BOTH`**
会同时返回关联和数值索引。**`SQLITE_BOTH`** 是此函数的默认值。

`error_msg`  
The specified variable will be filled if an error occurs. This is
specially important because SQL syntax errors can't be fetched using the
<span class="function">sqlite\_last\_error</span> function.

> **Note**: <span class="simpara">为兼容其他数据库扩展(比如
> MySQL)，支持两种可替代的语法。推荐第一种格式，函数的第一个参数是`dbhandle`。</span>

### 返回值

This function will return a result handle 或者在失败时返回 **`FALSE`**.
For queries that return rows, the result handle can then be used with
functions such as <span class="function">sqlite\_fetch\_array</span> and
<span class="function">sqlite\_seek</span>.

Regardless of the query type, this function will return **`FALSE`** if
the query failed.

<span class="function">sqlite\_query</span> returns a buffered, seekable
result handle. This is useful for reasonably small queries where you
need to be able to randomly access the rows. Buffered result handles
will allocate memory to hold the entire result and will not return until
it has been fetched. If you only need sequential access to the data, it
is recommended that you use the much higher performance <span
class="function">sqlite\_unbuffered\_query</span> instead.

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 5.1.0 | Added the `error_msg` parameter |

### 注释

**Warning**

SQLite *will* execute multiple queries separated by semicolons, so you
can use it to execute a batch of SQL that you have loaded from a file or
have embedded in a script. However, this works only when the result of
the function is not used - if it is used, only the first SQL statement
would be executed. Function <span class="function">sqlite\_exec</span>
will always execute multiple SQL statements.

When executing multiple queries, the return value of this function will
be **`FALSE`** if there was an error, but undefined otherwise (it might
be **`TRUE`** for success or it might return a result handle).

### 参见

-   <span class="function">sqlite\_unbuffered\_query</span>
-   <span class="function">sqlite\_array\_query</span>

sqlite\_rewind
==============

SQLiteResult::rewind
====================

Seek to the first row number

### 说明

<span class="type">bool</span> <span
class="methodname">sqlite\_rewind</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格 (method):

<span class="type">bool</span> <span
class="methodname">SQLiteResult::rewind</span> ( <span
class="methodparam">void</span> )

<span class="function">sqlite\_rewind</span> seeks back to the first row
in the given result set.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

> **Note**:
>
> 此函数不能用于未缓冲的结果句柄。

### 返回值

Returns **`FALSE`** if there are no rows in the result set, **`TRUE`**
otherwise.

### 参见

-   <span class="function">sqlite\_next</span>
-   <span class="function">sqlite\_current</span>
-   <span class="function">sqlite\_seek</span>

sqlite\_seek
============

SQLiteResult::seek
==================

Seek to a particular row number of a buffered result set

### 说明

<span class="type">bool</span> <span
class="methodname">sqlite\_seek</span> ( <span class="methodparam"><span
class="type">resource</span> `$result`</span> , <span
class="methodparam"><span class="type">int</span> `$rownum`</span> )

面向对象风格 (method):

<span class="type">bool</span> <span
class="methodname">SQLiteResult::seek</span> ( <span
class="methodparam"><span class="type">int</span> `$rownum`</span> )

<span class="function">sqlite\_seek</span> seeks to the row given by the
parameter `rownum`.

### 参数

`result`  
The SQLite result resource. This parameter is not required when using
the object-oriented method.

> **Note**:
>
> 此函数不能用于未缓冲的结果句柄。

`rownum`  
The ordinal row number to seek to. The row number is zero-based (0 is
the first row).

> **Note**:
>
> 此函数不能用于未缓冲的结果句柄。

### 返回值

Returns **`FALSE`** if the row does not exist, **`TRUE`** otherwise.

### 参见

-   <span class="function">sqlite\_next</span>
-   <span class="function">sqlite\_current</span>
-   <span class="function">sqlite\_rewind</span>

sqlite\_single\_query
=====================

SQLiteDatabase::singleQuery
===========================

Executes a query and returns either an array for one single column or
the value of the first row

### 说明

<span class="type">array</span> <span
class="methodname">sqlite\_single\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$db`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$first_row_only`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$decode_binary`</span> \]\] )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SQLiteDatabase::singleQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$first_row_only`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$decode_binary`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

sqlite\_udf\_decode\_binary
===========================

Decode binary data passed as parameters to an UDF

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_udf\_decode\_binary</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Decodes binary data passed as parameters to a UDF.

You must call this function on parameters passed to your UDF if you need
them to handle binary data, as the binary encoding employed by PHP will
obscure the content and of the parameter in its natural, non-coded form.

PHP does not perform this encode/decode operation automatically as it
would severely impact performance if it did.

### 参数

`data`  
The encoded data that will be decoded, data that was applied by either
<span class="function">sqlite\_udf\_encode\_binary</span> or <span
class="function">sqlite\_escape\_string</span>.

### 返回值

The decoded <span class="type">string</span>.

### 范例

**示例 \#1 binary-safe max\_length aggregation function example**

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
$db = sqlite_open(':memory:');
sqlite_query($db, "CREATE TABLE strings(a)");
foreach ($data as $str) {
    $str = sqlite_escape_string($str);
    sqlite_query($db, "INSERT INTO strings VALUES ('$str')");
}

function max_len_step(&$context, $string) 
{
    $string = sqlite_udf_decode_binary($string);
    if (strlen($string) > $context) {
        $context = strlen($string);
    }
}

function max_len_finalize(&$context) 
{
    return $context;
}

sqlite_create_aggregate($db, 'max_len', 'max_len_step', 'max_len_finalize');

var_dump(sqlite_array_query($db, 'SELECT max_len(a) from strings'));

?>
```

### 参见

-   <span class="function">sqlite\_udf\_encode\_binary</span>
-   <span class="function">sqlite\_create\_function</span>
-   <span class="function">sqlite\_create\_aggregate</span>

sqlite\_udf\_encode\_binary
===========================

Encode binary data before returning it from an UDF

### 说明

<span class="type">string</span> <span
class="methodname">sqlite\_udf\_encode\_binary</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">sqlite\_udf\_encode\_binary</span> applies a
binary encoding to the `data` so that it can be safely returned from
queries (since the underlying `libsqlite` API is not binary safe).

If there is a chance that your data might be binary unsafe (e.g.: it
contains a NUL byte in the middle rather than at the end, or if it has
and *0x01* byte as the first character) then you must call this function
to encode the return value from your UDF.

PHP does not perform this encode/decode operation automatically as it
would severely impact performance if it did.

> **Note**:
>
> Do not use <span class="function">sqlite\_escape\_string</span> to
> quote strings returned from UDF's as it will lead to double-quoting of
> the data. Use <span
> class="function">sqlite\_udf\_encode\_binary</span> instead!

### 参数

`data`  
The <span class="type">string</span> being encoded.

### 返回值

The encoded <span class="type">string</span>.

### 参见

-   <span class="function">sqlite\_udf\_decode\_binary</span>
-   <span class="function">sqlite\_escape\_string</span>
-   <span class="function">sqlite\_create\_function</span>
-   <span class="function">sqlite\_create\_aggregate</span>

sqlite\_unbuffered\_query
=========================

SQLiteDatabase::unbufferedQuery
===============================

Execute a query that does not prefetch and buffer all data

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">sqlite\_unbuffered\_query</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> , <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">int</span> `$result_type`<span
class="initializer"> = SQLITE\_BOTH</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`&$error_msg`</span> \]\] )

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">sqlite\_unbuffered\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$dbhandle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$result_type`<span class="initializer"> =
SQLITE\_BOTH</span></span> \[, <span class="methodparam"><span
class="type">string</span> `&$error_msg`</span> \]\] )

面向对象风格 (method):

<span class="modifier">public</span> <span class="type"><span
class="type">SQLiteUnbuffered</span><span
class="type">false</span></span> <span
class="methodname">SQLiteDatabase::unbufferedQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$result_type`<span class="initializer"> = SQLITE\_BOTH</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`&$error_msg`</span> \]\] )

<span class="function">sqlite\_unbuffered\_query</span> is identical to
<span class="function">sqlite\_query</span> except that the result that
is returned is a sequential forward-only result set that can only be
used to read each row, one after the other.

This function is ideal for generating things such as HTML tables where
you only need to process one row at a time and don't need to randomly
access the row data.

> **Note**:
>
> Functions such as <span class="function">sqlite\_seek</span>, <span
> class="function">sqlite\_rewind</span>, <span
> class="function">sqlite\_next</span>, <span
> class="function">sqlite\_current</span>, and <span
> class="function">sqlite\_num\_rows</span> do not work on result
> handles returned from <span
> class="function">sqlite\_unbuffered\_query</span>.

### 参数

`dbhandle`  
The SQLite Database resource; returned from <span
class="function">sqlite\_open</span> when used procedurally. This
parameter is not required when using the object-oriented method.

`query`  
The query to be executed.

Data inside the query should be
<a href="/book/sqlite.html#sqlite_escape_string" class="link">properly escaped</a>.

`result_type`  
可选的 `result_type` 参数接受常量，且决定返回的数组如何被索引。使用
**`SQLITE_ASSOC`** 会仅返回关联索引（已命名字段），而 **`SQLITE_NUM`**
会仅返回数值索引。**`SQLITE_BOTH`**
会同时返回关联和数值索引。**`SQLITE_BOTH`** 是此函数的默认值。

`error_msg`  
The specified variable will be filled if an error occurs. This is
specially important because SQL syntax errors can't be fetched using the
<span class="function">sqlite\_last\_error</span> function.

> **Note**: <span class="simpara">为兼容其他数据库扩展(比如
> MySQL)，支持两种可替代的语法。推荐第一种格式，函数的第一个参数是`dbhandle`。</span>

### 返回值

Returns a result handle 或者在失败时返回 **`FALSE`**.

<span class="function">sqlite\_unbuffered\_query</span> returns a
sequential forward-only result set that can only be used to read each
row, one after the other.

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 5.1.0 | Added the `error_msg` parameter |

### 参见

-   <span class="function">sqlite\_query</span>

**目录**

-   [sqlite\_array\_query](/book/sqlite.html#sqlite_array_query) —
    Execute a query against a given database and returns an array
-   [sqlite\_busy\_timeout](/book/sqlite.html#sqlite_busy_timeout) — Set
    busy timeout duration, or disable busy handlers
-   [sqlite\_changes](/book/sqlite.html#sqlite_changes) — Returns the
    number of rows that were changed by the most recent SQL statement
-   [sqlite\_close](/book/sqlite.html#sqlite_close) — Closes an open
    SQLite database
-   [sqlite\_column](/book/sqlite.html#sqlite_column) — Fetches a column
    from the current row of a result set
-   [sqlite\_create\_aggregate](/book/sqlite.html#sqlite_create_aggregate)
    — Register an aggregating UDF for use in SQL statements
-   [sqlite\_create\_function](/book/sqlite.html#sqlite_create_function)
    — Registers a "regular" User Defined Function for use in SQL
    statements
-   [sqlite\_current](/book/sqlite.html#sqlite_current) — Fetches the
    current row from a result set as an array
-   [sqlite\_error\_string](/book/sqlite.html#sqlite_error_string) —
    Returns the textual description of an error code
-   [sqlite\_escape\_string](/book/sqlite.html#sqlite_escape_string) —
    Escapes a string for use as a query parameter
-   [sqlite\_exec](/book/sqlite.html#sqlite_exec) — Executes a
    result-less query against a given database
-   [sqlite\_fetch\_all](/book/sqlite.html#sqlite_fetch_all) — Fetches
    all rows from a result set as an array of arrays
-   [sqlite\_fetch\_array](/book/sqlite.html#sqlite_fetch_array) —
    Fetches the next row from a result set as an array
-   [sqlite\_fetch\_single](/book/sqlite.html#sqlite_fetch_single) —
    Fetches the first column of a result set as a string
-   [sqlite\_fetch\_string](/book/sqlite.html#sqlite_fetch_string) —
    别名 sqlite\_fetch\_single
-   [sqlite\_field\_name](/book/sqlite.html#sqlite_field_name) — Returns
    the name of a particular field
-   [sqlite\_has\_more](/book/sqlite.html#sqlite_has_more) — Finds
    whether or not more rows are available
-   [sqlite\_last\_error](/book/sqlite.html#sqlite_last_error) — Returns
    the error code of the last error for a database
-   [sqlite\_last\_insert\_rowid](/book/sqlite.html#sqlite_last_insert_rowid)
    — Returns the rowid of the most recently inserted row
-   [sqlite\_libencoding](/book/sqlite.html#sqlite_libencoding) —
    Returns the encoding of the linked SQLite library
-   [sqlite\_libversion](/book/sqlite.html#sqlite_libversion) — Returns
    the version of the linked SQLite library
-   [sqlite\_next](/book/sqlite.html#sqlite_next) — Seek to the next row
    number
-   [sqlite\_num\_fields](/book/sqlite.html#sqlite_num_fields) — Returns
    the number of fields in a result set
-   [sqlite\_num\_rows](/book/sqlite.html#sqlite_num_rows) — Returns the
    number of rows in a buffered result set
-   [sqlite\_open](/book/sqlite.html#sqlite_open) — Opens an SQLite
    database and create the database if it does not exist
-   [sqlite\_popen](/book/sqlite.html#sqlite_popen) — Opens a persistent
    handle to an SQLite database and create the database if it does not
    exist
-   [sqlite\_query](/book/sqlite.html#sqlite_query) — Executes a query
    against a given database and returns a result handle
-   [sqlite\_rewind](/book/sqlite.html#sqlite_rewind) — Seek to the
    first row number
-   [sqlite\_seek](/book/sqlite.html#sqlite_seek) — Seek to a particular
    row number of a buffered result set
-   [sqlite\_single\_query](/book/sqlite.html#sqlite_single_query) —
    Executes a query and returns either an array for one single column
    or the value of the first row
-   [sqlite\_udf\_decode\_binary](/book/sqlite.html#sqlite_udf_decode_binary)
    — Decode binary data passed as parameters to an UDF
-   [sqlite\_udf\_encode\_binary](/book/sqlite.html#sqlite_udf_encode_binary)
    — Encode binary data before returning it from an UDF
-   [sqlite\_unbuffered\_query](/book/sqlite.html#sqlite_unbuffered_query)
    — Execute a query that does not prefetch and buffer all data
