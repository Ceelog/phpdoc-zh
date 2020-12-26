ODBC (Unified)
==============

**目录**

-   [简介](/book/uodbc.html#简介)
-   [安装／配置](/book/uodbc.html#安装／配置)
    -   [需求](/book/uodbc.html#需求)
    -   [安装](/book/uodbc.html#安装)
    -   [运行时配置](/book/uodbc.html#运行时配置)
    -   [资源类型](/book/uodbc.html#资源类型)
-   [预定义常量](/book/uodbc.html#预定义常量)
-   [ODBC 函数](/book/uodbc.html#ODBC%20函数)
    -   [odbc\_autocommit](/book/uodbc.html#odbc_autocommit) — Toggle
        autocommit behaviour
    -   [odbc\_binmode](/book/uodbc.html#odbc_binmode) — Handling of
        binary column data
    -   [odbc\_close\_all](/book/uodbc.html#odbc_close_all) — Close all
        ODBC connections
    -   [odbc\_close](/book/uodbc.html#odbc_close) — Close an ODBC
        connection
    -   [odbc\_columnprivileges](/book/uodbc.html#odbc_columnprivileges)
        — Lists columns and associated privileges for the given table
    -   [odbc\_columns](/book/uodbc.html#odbc_columns) — Lists the
        column names in specified tables
    -   [odbc\_commit](/book/uodbc.html#odbc_commit) — Commit an ODBC
        transaction
    -   [odbc\_connect](/book/uodbc.html#odbc_connect) — Connect to a
        datasource
    -   [odbc\_cursor](/book/uodbc.html#odbc_cursor) — Get cursorname
    -   [odbc\_data\_source](/book/uodbc.html#odbc_data_source) —
        Returns information about available DSNs
    -   [odbc\_do](/book/uodbc.html#odbc_do) — 别名 odbc\_exec
    -   [odbc\_error](/book/uodbc.html#odbc_error) — Get the last error
        code
    -   [odbc\_errormsg](/book/uodbc.html#odbc_errormsg) — Get the last
        error message
    -   [odbc\_exec](/book/uodbc.html#odbc_exec) — Directly execute an
        SQL statement
    -   [odbc\_execute](/book/uodbc.html#odbc_execute) — Execute a
        prepared statement
    -   [odbc\_fetch\_array](/book/uodbc.html#odbc_fetch_array) — Fetch
        a result row as an associative array
    -   [odbc\_fetch\_into](/book/uodbc.html#odbc_fetch_into) — Fetch
        one result row into array
    -   [odbc\_fetch\_object](/book/uodbc.html#odbc_fetch_object) —
        Fetch a result row as an object
    -   [odbc\_fetch\_row](/book/uodbc.html#odbc_fetch_row) — Fetch a
        row
    -   [odbc\_field\_len](/book/uodbc.html#odbc_field_len) — Get the
        length (precision) of a field
    -   [odbc\_field\_name](/book/uodbc.html#odbc_field_name) — Get the
        columnname
    -   [odbc\_field\_num](/book/uodbc.html#odbc_field_num) — Return
        column number
    -   [odbc\_field\_precision](/book/uodbc.html#odbc_field_precision)
        — 别名 odbc\_field\_len
    -   [odbc\_field\_scale](/book/uodbc.html#odbc_field_scale) — Get
        the scale of a field
    -   [odbc\_field\_type](/book/uodbc.html#odbc_field_type) — Datatype
        of a field
    -   [odbc\_foreignkeys](/book/uodbc.html#odbc_foreignkeys) —
        Retrieves a list of foreign keys
    -   [odbc\_free\_result](/book/uodbc.html#odbc_free_result) — Free
        resources associated with a result
    -   [odbc\_gettypeinfo](/book/uodbc.html#odbc_gettypeinfo) —
        Retrieves information about data types supported by the data
        source
    -   [odbc\_longreadlen](/book/uodbc.html#odbc_longreadlen) —
        Handling of LONG columns
    -   [odbc\_next\_result](/book/uodbc.html#odbc_next_result) — Checks
        if multiple results are available
    -   [odbc\_num\_fields](/book/uodbc.html#odbc_num_fields) — Number
        of columns in a result
    -   [odbc\_num\_rows](/book/uodbc.html#odbc_num_rows) — Number of
        rows in a result
    -   [odbc\_pconnect](/book/uodbc.html#odbc_pconnect) — Open a
        persistent database connection
    -   [odbc\_prepare](/book/uodbc.html#odbc_prepare) — Prepares a
        statement for execution
    -   [odbc\_primarykeys](/book/uodbc.html#odbc_primarykeys) — Gets
        the primary keys for a table
    -   [odbc\_procedurecolumns](/book/uodbc.html#odbc_procedurecolumns)
        — Retrieve information about parameters to procedures
    -   [odbc\_procedures](/book/uodbc.html#odbc_procedures) — Get the
        list of procedures stored in a specific data source
    -   [odbc\_result\_all](/book/uodbc.html#odbc_result_all) — Print
        result as HTML table
    -   [odbc\_result](/book/uodbc.html#odbc_result) — Get result data
    -   [odbc\_rollback](/book/uodbc.html#odbc_rollback) — Rollback a
        transaction
    -   [odbc\_setoption](/book/uodbc.html#odbc_setoption) — Adjust ODBC
        settings
    -   [odbc\_specialcolumns](/book/uodbc.html#odbc_specialcolumns) —
        Retrieves special columns
    -   [odbc\_statistics](/book/uodbc.html#odbc_statistics) — Retrieve
        statistics about a table
    -   [odbc\_tableprivileges](/book/uodbc.html#odbc_tableprivileges) —
        Lists tables and the privileges associated with each table
    -   [odbc\_tables](/book/uodbc.html#odbc_tables) — Get the list of
        table names stored in a specific data source

In addition to normal ODBC support, the Unified ODBC functions in PHP
allow you to access several databases that have borrowed the semantics
of the ODBC API to implement their own API. Instead of maintaining
multiple database drivers that were all nearly identical, these drivers
have been unified into a single set of ODBC functions.

The following databases are supported by the Unified ODBC functions:
<a href="http://www.adabas.com/" class="link external">» Adabas D</a>,
<a href="http://www-306.ibm.com/software/data/db2/" class="link external">» IBM DB2</a>,
<a href="http://www.iodbc.org/" class="link external">» iODBC</a>,
<a href="http://www.solidtech.com/" class="link external">» Solid</a>,
and
<a href="http://www.sybase.com/" class="link external">» Sybase SQL Anywhere</a>.

> **Note**:
>
> With the exception of iODBC, there is no ODBC involved when connecting
> to the above databases. The functions that you use to speak natively
> to them just happen to share the same names and syntax as the ODBC
> functions. However, building PHP with iODBC support enables you to use
> any ODBC-compliant drivers with your PHP applications. More
> information on iODBC, is available at
> <a href="http://www.iodbc.org/" class="link external">» www.iodbc.org</a>
> with the alternative unixODBC available at
> <a href="http://www.unixodbc.org/" class="link external">» www.unixodbc.org</a>.

安装／配置
==========

**目录**

-   [需求](/book/uodbc.html#需求)
-   [安装](/book/uodbc.html#安装)
-   [运行时配置](/book/uodbc.html#运行时配置)
-   [资源类型](/book/uodbc.html#资源类型)

需求
----

To access any of the supported databases you need to have the required
libraries installed.

安装
----

**--with-adabas\[=DIR\]**  
Include Adabas D support. DIR is the Adabas base install directory,
defaults to `/usr/local`.

**--with-sapdb\[=DIR\]**  
Include SAP DB support. DIR is SAP DB base install directory, defaults
to `/usr/local`.

**--with-solid\[=DIR\]**  
Include Solid support. DIR is the Solid base install directory, defaults
to `/usr/local/solid`.

**--with-ibm-db2\[=DIR\]**  
Include IBM DB2 support. DIR is the DB2 base install directory, defaults
to `/home/db2inst1/sqllib`.

**--with-empress\[=DIR\]**  
Include Empress support. DIR is the Empress base install directory,
defaults to `$EMPRESSPATH`. This option only supports Empress Version
8.60 and above.

**--with-empress-bcs\[=DIR\]**  
Include *"Empress Local Access"* support. DIR is the Empress base
install directory, defaults to `$EMPRESSPATH`. This option only supports
Empress Version 8.60 and above.

**--with-birdstep\[=DIR\]**  
Include Birdstep support. DIR is the Birdstep base install directory,
defaults to `/usr/local/birdstep`.

**--with-custom-odbc\[=DIR\]**  
Include a user defined ODBC support. The DIR is ODBC install base
directory, which defaults to `/usr/local`. Make sure to define
CUSTOM\_ODBC\_LIBS and have some `odbc.h` in your include dirs. E.g.,
you should define following for Sybase SQL Anywhere 5.5.00 on QNX, prior
to run configure script:

       CPPFLAGS="-DODBC_QNX -DSQLANY_BUG"
       LDFLAGS=-lunix
       CUSTOM_ODBC_LIBS="-ldblib -lodbc".

**--with-iodbc\[=DIR\]**  
Include iODBC support. DIR is the iODBC base install directory, defaults
to `/usr/local`.

**--with-esoob\[=DIR\]**  
Include Easysoft OOB support. DIR is the OOB base install directory,
defaults to `/usr/local/easysoft/oob/client`.

**--with-unixODBC\[=DIR\]**  
Include unixODBC support. DIR is the unixODBC base install directory,
defaults to `/usr/local`.

**--with-openlink\[=DIR\]**  
Include OpenLink ODBC support. DIR is the OpenLink base install
directory, defaults to `/usr/local`. This is the same as iODBC.

**--with-dbmaker\[=DIR\]**  
Include DBMaker support. DIR is the DBMaker base install directory,
defaults to where the latest version of DBMaker is installed (such as
`/home/dbmaker/3.6`).

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

As of PHP 7.0.0, however, Windows users must enable `php_odbc.dll` in
order to use this extension.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                 | 默认   | 可修改范围       | 更新日志                  |
|----------------------------------------------------------------------|--------|------------------|---------------------------|
| <a href="/book/uodbc.html#" class="link">odbc.default_db</a> \*      | NULL   | PHP\_INI\_ALL    |                           |
| <a href="/book/uodbc.html#" class="link">odbc.default_user</a> \*    | NULL   | PHP\_INI\_ALL    |                           |
| <a href="/book/uodbc.html#" class="link">odbc.default_pw</a> \*      | NULL   | PHP\_INI\_ALL    |                           |
| <a href="/book/uodbc.html#" class="link">odbc.allow_persistent</a>   | "1"    | PHP\_INI\_SYSTEM |                           |
| <a href="/book/uodbc.html#" class="link">odbc.check_persistent</a>   | "1"    | PHP\_INI\_SYSTEM |                           |
| <a href="/book/uodbc.html#" class="link">odbc.max_persistent</a>     | "-1"   | PHP\_INI\_SYSTEM |                           |
| <a href="/book/uodbc.html#" class="link">odbc.max_links</a>          | "-1"   | PHP\_INI\_SYSTEM |                           |
| <a href="/book/uodbc.html#" class="link">odbc.defaultlrl</a>         | "4096" | PHP\_INI\_ALL    |                           |
| <a href="/book/uodbc.html#" class="link">odbc.defaultbinmode</a>     | "1"    | PHP\_INI\_ALL    |                           |
| <a href="/book/uodbc.html#" class="link">odbc.default_cursortype</a> | "3"    | PHP\_INI\_ALL    | Available as of PHP 5.3.0 |

> **Note**: <span class="simpara"> Entries marked with \* are not
> implemented yet. </span>

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`odbc.default_db` <span class="type">string</span>  
ODBC data source to use if none is specified in <span
class="function">odbc\_connect</span> or <span
class="function">odbc\_pconnect</span>.

`odbc.default_user` <span class="type">string</span>  
User name to use if none is specified in <span
class="function">odbc\_connect</span> or <span
class="function">odbc\_pconnect</span>.

`odbc.default_pw` <span class="type">string</span>  
Password to use if none is specified in <span
class="function">odbc\_connect</span> or <span
class="function">odbc\_pconnect</span>.

`odbc.allow_persistent` <span class="type">bool</span>  
Whether to allow persistent ODBC connections.

`odbc.check_persistent` <span class="type">bool</span>  
Check that a connection is still valid before reuse.

`odbc.max_persistent` <span class="type">int</span>  
The maximum number of persistent ODBC connections per process.

`odbc.max_links` <span class="type">int</span>  
The maximum number of ODBC connections per process, including persistent
connections.

`odbc.defaultlrl` <span class="type">int</span>  
Handling of LONG fields. Specifies the number of bytes returned to
variables. See <span class="function">odbc\_longreadlen</span> for
details.

<span class="simpara">当使用 <span class="type">int</span> 时,
其值以字节来衡量。还可以使用在<a href="/faq/using.html#faq.using.shorthandbytes" class="link">FAQ</a>中描述的速记符。</span>

`odbc.defaultbinmode` <span class="type">int</span>  
Handling of binary data. See <span class="function">odbc\_binmode</span>
for details.

`odbc.default_cursortype` <span class="type">int</span>  
Controls the ODBC cursor model. Possible values are
**`SQL_CURSOR_FORWARD_ONLY`**, **`SQL_CURSOR_KEYSET_DRIVEN`**,
**`SQL_CURSOR_DYNAMIC`** and **`SQL_CURSOR_STATIC`** (default).

资源类型
--------

This extension defines two resource types: an ODBC connection identifier
and an ODBC result identifier.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`ODBC_TYPE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`ODBC_BINMODE_PASSTHRU`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`ODBC_BINMODE_RETURN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`ODBC_BINMODE_CONVERT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_ODBC_CURSORS`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CUR_USE_DRIVER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CUR_USE_IF_NEEDED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CUR_USE_ODBC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CONCURRENCY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CONCUR_READ_ONLY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CONCUR_LOCK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CONCUR_ROWVER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CONCUR_VALUES`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CURSOR_TYPE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CURSOR_FORWARD_ONLY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CURSOR_KEYSET_DRIVEN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CURSOR_DYNAMIC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CURSOR_STATIC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_KEYSET_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_CHAR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_VARCHAR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_LONGVARCHAR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_DECIMAL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_NUMERIC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_BIT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_TINYINT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_SMALLINT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_INTEGER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_BIGINT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_REAL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_FLOAT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_DOUBLE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_BINARY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_VARBINARY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_LONGVARBINARY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_DATE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_TIME`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_TIMESTAMP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_TYPE_DATE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_TYPE_TIME`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_TYPE_TIMESTAMP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_BEST_ROWID`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_ROWVER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_SCOPE_CURROW`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_SCOPE_TRANSACTION`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_SCOPE_SESSION`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_NO_NULLS`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_NULLABLE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_INDEX_UNIQUE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_INDEX_ALL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_ENSURE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`SQL_QUICK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

odbc\_autocommit
================

Toggle autocommit behaviour

### 说明

<span class="type"><span class="type">int</span><span
class="type">bool</span></span> <span
class="methodname">odbc\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$enable`<span class="initializer"> = **`false`**</span></span> \] )

Toggles autocommit behaviour.

By default, auto-commit is on for a connection. Disabling auto-commit is
equivalent with starting a transaction.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`enable`  
If `enable` is **`true`**, auto-commit is enabled, if it is **`false`**
auto-commit is disabled.

### 返回值

Without the `enable` parameter, this function returns auto-commit status
for `odbc`. Non-zero is returned if auto-commit is on, 0 if it is off,
or **`false`** if an error occurs.

If `enable` is set, this function returns **`true`** on success and
**`false`** on failure.

### 参见

-   <span class="function">odbc\_commit</span>
-   <span class="function">odbc\_rollback</span>

odbc\_binmode
=============

Handling of binary column data

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_binmode</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> )

Controls handling of binary column data. ODBC SQL types affected are
*BINARY*, *VARBINARY*, and *LONGVARBINARY*. The default mode can be set
using the
<a href="/book/uodbc.html#" class="link">uodbc.defaultbinmode</a>
`php.ini` directive.

When binary SQL data is converted to character C data
(**`ODBC_BINMODE_CONVERT`**), each byte (8 bits) of source data is
represented as two ASCII characters. These characters are the ASCII
character representation of the number in its hexadecimal form. For
example, a binary *00000001* is converted to *"01"* and a binary
*11111111* is converted to *"FF"*.

While the handling of *BINARY* and *VARBINARY* columns only depend on
the binmode, the handling of *LONGVARBINARY* columns also depends on the
longreadlen as well:

| binmode                     | longreadlen | result         |
|-----------------------------|-------------|----------------|
| **`ODBC_BINMODE_PASSTHRU`** | 0           | passthru       |
| **`ODBC_BINMODE_RETURN`**   | 0           | passthru       |
| **`ODBC_BINMODE_CONVERT`**  | 0           | passthru       |
| **`ODBC_BINMODE_PASSTHRU`** | \>0         | passthru       |
| **`ODBC_BINMODE_RETURN`**   | \>0         | return as is   |
| **`ODBC_BINMODE_CONVERT`**  | \>0         | return as char |

If <span class="function">odbc\_fetch\_into</span> is used, passthru
means that an empty string is returned for these columns. If <span
class="function">odbc\_result</span> is used, passthru means that the
data are sent directly to the client (i.e. printed).

### 参数

`statement`  
The result identifier.

If `statement` is *0*, the settings apply as default for new results.

`mode`  
Possible values for `mode` are:

-   <span class="simpara"> **`ODBC_BINMODE_PASSTHRU`**: Passthru BINARY
    data </span>
-   <span class="simpara"> **`ODBC_BINMODE_RETURN`**: Return as is
    </span>
-   <span class="simpara"> **`ODBC_BINMODE_CONVERT`**: Convert to char
    and return </span>

> **Note**: <span class="simpara"> Handling of binary long columns is
> also affected by <span class="function">odbc\_longreadlen</span>.
> </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

odbc\_close\_all
================

Close all ODBC connections

### 说明

<span class="type">void</span> <span
class="methodname">odbc\_close\_all</span> ( <span
class="methodparam">void</span> )

<span class="function">odbc\_close\_all</span> will close down all
connections to database server(s).

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 注释

> **Note**:
>
> This function will fail if there are open transactions on a
> connection. This connection will remain open in this case.

odbc\_close
===========

Close an ODBC connection

### 说明

<span class="type">void</span> <span
class="methodname">odbc\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$odbc`</span> )

Closes down the connection to the database server.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

### 返回值

没有返回值。

### 注释

> **Note**:
>
> This function will fail if there are open transactions on this
> connection. The connection will remain open in this case.

odbc\_columnprivileges
======================

Lists columns and associated privileges for the given table

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_columnprivileges</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$schema`</span> , <span
class="methodparam"><span class="type">string</span> `$table`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column`</span> )

Lists columns and associated privileges for the given table.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance). 此参数接受下列查询模式： *%*
来匹配零到多个字符， *\_* 来匹配单个字符。

`table`  
The table name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

`column`  
The column name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

### 返回值

Returns an ODBC result identifier 或者在失败时返回 **`false`**. This
result identifier can be used to fetch a list of columns and associated
privileges.

The result set has the following columns:

-   <span class="simpara">*TABLE\_CAT*</span>
-   <span class="simpara">*TABLE\_SCHEM*</span>
-   <span class="simpara">*TABLE\_NAME*</span>
-   <span class="simpara">*COLUMN\_NAME*</span>
-   <span class="simpara">*GRANTOR*</span>
-   <span class="simpara">*GRANTEE*</span>
-   <span class="simpara">*PRIVILEGE*</span>
-   <span class="simpara">*IS\_GRANTABLE*</span>

Drivers can report additional columns.

The result set is ordered by *TABLE\_CAT*, *TABLE\_SCHEM*,
*TABLE\_NAME*, *COLUMN\_NAME* and *PRIVILEGE*.

### 范例

**示例 \#1 List Privileges for a Column**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$privileges = odbc_columnprivileges($conn, 'TutorialDB', 'dbo', 'test', 'id');
while (($row = odbc_fetch_array($privileges))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [TABLE_CAT] => TutorialDB
        [TABLE_SCHEM] => dbo
        [TABLE_NAME] => test
        [COLUMN_NAME] => id
        [GRANTOR] => dbo
        [GRANTEE] => dbo
        [PRIVILEGE] => INSERT
        [IS_GRANTABLE] => YES
    )

odbc\_columns
=============

Lists the column names in specified tables

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_columns</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$schema`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$table`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$column`<span class="initializer"> = **`null`**</span></span> \]\]\]\]
)

Lists all columns in the requested range.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance). 此参数接受下列查询模式： *%*
来匹配零到多个字符， *\_* 来匹配单个字符。

`table`  
The table name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

`column`  
The column name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

### 返回值

Returns an ODBC result identifier 或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*TABLE\_CAT*</span>
-   <span class="simpara">*TABLE\_SCHEM*</span>
-   <span class="simpara">*TABLE\_NAME*</span>
-   <span class="simpara">*COLUMN\_NAME*</span>
-   <span class="simpara">*DATA\_TYPE*</span>
-   <span class="simpara">*TYPE\_NAME*</span>
-   <span class="simpara">*COLUMN\_SIZE*</span>
-   <span class="simpara">*BUFFER\_LENGTH*</span>
-   <span class="simpara">*DECIMAL\_DIGITS*</span>
-   <span class="simpara">*NUM\_PREC\_RADIX*</span>
-   <span class="simpara">*NULLABLE*</span>
-   <span class="simpara">*REMARKS*</span>
-   <span class="simpara">*COLUMN\_DEF*</span>
-   <span class="simpara">*SQL\_DATA\_TYPE*</span>
-   <span class="simpara">*SQL\_DATETIME\_SUB*</span>
-   <span class="simpara">*CHAR\_OCTET\_LENGTH*</span>
-   <span class="simpara">*ORDINAL\_POSITION*</span>
-   <span class="simpara">*IS\_NULLABLE*</span>

Drivers can report additional columns.

The result set is ordered by *TABLE\_CAT*, *TABLE\_SCHEM*, *TABLE\_NAME*
and *ORDINAL\_POSITION*.

### 更新日志

| 版本  | 说明                                             |
|-------|--------------------------------------------------|
| 8.0.0 | `schema`, `table` and `column` are now nullable. |

### 范例

**示例 \#1 List Columns of a Table**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$columns = odbc_columns($conn, 'TutorialDB', 'dbo', 'test', '%');
while (($row = odbc_fetch_array($columns))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [TABLE_CAT] => TutorialDB
        [TABLE_SCHEM] => dbo
        [TABLE_NAME] => TEST
        [COLUMN_NAME] => id
        [DATA_TYPE] => 4
        [TYPE_NAME] => int
        [COLUMN_SIZE] => 10
        [BUFFER_LENGTH] => 4
        [DECIMAL_DIGITS] => 0
        [NUM_PREC_RADIX] => 10
        [NULLABLE] => 0
        [REMARKS] =>
        [COLUMN_DEF] =>
        [SQL_DATA_TYPE] => 4
        [SQL_DATETIME_SUB] =>
        [CHAR_OCTET_LENGTH] =>
        [ORDINAL_POSITION] => 1
        [IS_NULLABLE] => NO
    )

### 参见

-   <span class="function">odbc\_columnprivileges</span>
-   <span class="function">odbc\_procedurecolumns</span>

odbc\_commit
============

Commit an ODBC transaction

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_commit</span> ( <span class="methodparam"><span
class="type">resource</span> `$odbc`</span> )

Commits all pending transactions on the connection.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

odbc\_connect
=============

Connect to a datasource

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_connect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$user`</span> , <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">int</span> `$cursor_option`<span
class="initializer"> = **`SQL_CUR_USE_DRIVER`**</span></span> \] )

The connection id returned by this functions is needed by other ODBC
functions. You can have multiple connections open at once as long as
they either use different db or different credentials.

With some ODBC drivers, executing a complex stored procedure may fail
with an error similar to: "Cannot open a cursor on a stored procedure
that has anything other than a single select statement in it". Using
SQL\_CUR\_USE\_ODBC may avoid that error. Also, some drivers don't
support the optional row\_number parameter in <span
class="function">odbc\_fetch\_row</span>. SQL\_CUR\_USE\_ODBC might help
in that case, too.

### 参数

`dsn`  
The database source name for the connection. Alternatively, a DSN-less
connection string can be used.

`user`  
The username.

`password`  
The password.

`cursor_option`  
This sets the type of cursor to be used for this connection. This
parameter is not normally needed, but can be useful for working around
problems with some ODBC drivers.

<span class="simpara"> The following constants are defined for
cursortype: </span>

-   <span class="simpara"> SQL\_CUR\_USE\_IF\_NEEDED </span>
-   <span class="simpara"> SQL\_CUR\_USE\_ODBC </span>
-   <span class="simpara"> SQL\_CUR\_USE\_DRIVER </span>

### 返回值

Returns an ODBC connection, 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 DSN-less connections**

``` php
<?php
// Microsoft SQL Server using the SQL Native Client 10.0 ODBC Driver - allows connection to SQL 7, 2000, 2005 and 2008
$connection = odbc_connect("Driver={SQL Server Native Client 10.0};Server=$server;Database=$database;", $user, $password);

// Microsoft Access
$connection = odbc_connect("Driver={Microsoft Access Driver (*.mdb)};Dbq=$mdbFilename", $user, $password);

// Microsoft Excel
$excelFile = realpath('C:/ExcelData.xls');
$excelDir = dirname($excelFile);
$connection = odbc_connect("Driver={Microsoft Excel Driver (*.xls)};DriverId=790;Dbq=$excelFile;DefaultDir=$excelDir" , '', '');
?>
```

### 参见

-   For persistent connections: <span
    class="function">odbc\_pconnect</span>

odbc\_cursor
============

Get cursorname

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">odbc\_cursor</span> ( <span class="methodparam"><span
class="type">resource</span> `$statement`</span> )

Gets the cursorname for the given result\_id.

### 参数

`statement`  
The result identifier.

### 返回值

Returns the cursor name, as a string, 或者在失败时返回 **`false`**.

odbc\_data\_source
==================

Returns information about available DSNs

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">odbc\_data\_source</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type">int</span>
`$fetch_type`</span> )

This function will return the list of available DSN (after calling it
several times).

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`fetch_type`  
The `fetch_type` can be one of two constant types:
**`SQL_FETCH_FIRST`**, **`SQL_FETCH_NEXT`**. Use **`SQL_FETCH_FIRST`**
the first time this function is called, thereafter use the
**`SQL_FETCH_NEXT`**.

### 返回值

Returns **`false`** on error, an <span class="type">array</span> upon
success, and **`null`** after fetching the last available DSN.

### 范例

**示例 \#1 List available DSNs**

``` php
<?php
$conn = odbc_connect('dsn', 'user', 'pass');
$dsn_info = odbc_data_source($conn, SQL_FETCH_FIRST);
while ($dsn_info) {
    print_r($dsn_info);
    $dsn_info = odbc_data_source($conn, SQL_FETCH_NEXT);
}
?>
```

以上例程的输出类似于：

    Array
    (
        [server] => dsn
        [description] => ODBC Driver 17 for SQL Server
    )
    Array
    (
        [server] => other_dsn
        [description] => Microsoft Access Driver (*.mdb, *.accdb)
    )

odbc\_do
========

别名 <span class="function">odbc\_exec</span>

### 说明

此函数是该函数的别名： <span class="function">odbc\_exec</span>.

odbc\_error
===========

Get the last error code

### 说明

<span class="type">string</span> <span
class="methodname">odbc\_error</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">resource</span><span class="type">null</span></span>
`$odbc`<span class="initializer"> = **`null`**</span></span> \] )

Returns a six-digit ODBC state, or an empty string if there has been no
errors.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

### 返回值

If `odbc` is specified, the last state of that connection is returned,
else the last state of any connection is returned.

This function returns meaningful value only if last odbc query failed
(i.e. <span class="function">odbc\_exec</span> returned **`false`**).

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 8.0.0 | `odbc` is nullable now. |

### 参见

-   <span class="function">odbc\_errormsg</span>
-   <span class="function">odbc\_exec</span>

odbc\_errormsg
==============

Get the last error message

### 说明

<span class="type">string</span> <span
class="methodname">odbc\_errormsg</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">resource</span><span class="type">null</span></span>
`$odbc`<span class="initializer"> = **`null`**</span></span> \] )

Returns a string containing the last ODBC error message, or an empty
string if there has been no errors.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

### 返回值

If `odbc` is specified, the last state of that connection is returned,
else the last state of any connection is returned.

This function returns meaningful value only if last odbc query failed
(i.e. <span class="function">odbc\_exec</span> returned **`false`**).

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 8.0.0 | `odbc` is nullable now. |

### 参见

-   <span class="function">odbc\_error</span>
-   <span class="function">odbc\_exec</span>

odbc\_exec
==========

Directly execute an SQL statement

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_exec</span> ( <span class="methodparam"><span
class="type">resource</span> `$odbc`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> )

Sends an SQL statement to the database server.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`query`  
The SQL statement.

### 返回值

Returns an ODBC result identifier if the SQL command was executed
successfully, or **`false`** on error.

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 8.0.0 | `flags` was removed. |

### 参见

-   <span class="function">odbc\_prepare</span>
-   <span class="function">odbc\_execute</span>

odbc\_execute
=============

Execute a prepared statement

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_execute</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> \[, <span class="methodparam"><span
class="type">array</span> `$params`<span class="initializer"> =
\[\]</span></span> \] )

Executes a statement prepared with <span
class="function">odbc\_prepare</span>.

### 参数

`statement`  
The result id <span class="type">resource</span>, from <span
class="function">odbc\_prepare</span>.

`params`  
Parameters in `parameter_array` will be substituted for placeholders in
the prepared statement in order. Elements of this array will be
converted to strings by calling this function.

Any parameters in `parameter_array` which start and end with single
quotes will be taken as the name of a file to read and send to the
database server as the data for the appropriate placeholder.

<span class="simpara"> If you wish to store a string which actually
begins and ends with single quotes, you must add a space or other
non-single-quote character to the beginning or end of the parameter,
which will prevent the parameter from being taken as a file name. If
this is not an option, then you must use another mechanism to store the
string, such as executing the query directly with <span
class="function">odbc\_exec</span>). </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">odbc\_execute</span> and <span
class="function">odbc\_prepare</span> example**

In the following code, `$success` will only be **`true`** if all three
parameters to myproc are IN parameters:

``` php
<?php
$a = 1;
$b = 2;
$c = 3;
$stmt    = odbc_prepare($conn, 'CALL myproc(?,?,?)');
$success = odbc_execute($stmt, array($a, $b, $c));
?>
```

If you need to call a stored procedure using INOUT or OUT parameters,
the recommended workaround is to use a native extension for your
database (for example,
<a href="/book/oci8.html#OCI8%20函数" class="link">oci8</a> for Oracle).

### 参见

-   <span class="function">odbc\_prepare</span>

odbc\_fetch\_array
==================

Fetch a result row as an associative array

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">odbc\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> \[, <span class="methodparam"><span
class="type">int</span> `$row`<span class="initializer"> =
-1</span></span> \] )

Fetch an associative <span class="type">array</span> from an ODBC query.

### 参数

`statement`  
The result resource from <span class="function">odbc\_exec</span>.

`row`  
Optionally choose which row number to retrieve.

### 返回值

Returns an array that corresponds to the fetched row, or **`false`** if
there are no more rows.

### 注释

> **Note**: <span class="simpara"> This function exists when compiled
> with DBMaker, IBM DB2 or UnixODBC support. </span>

### 参见

-   <span class="function">odbc\_fetch\_row</span>
-   <span class="function">odbc\_fetch\_object</span>
-   <span class="function">odbc\_num\_rows</span>

odbc\_fetch\_into
=================

Fetch one result row into array

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">odbc\_fetch\_into</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">array</span> `&$array`</span> \[, <span
class="methodparam"><span class="type">int</span> `$row`<span
class="initializer"> = 0</span></span> \] )

Fetch one result row into <span class="type">array</span>.

### 参数

`statement`  
The result <span class="type">resource</span>.

`array`  
The result <span class="type">array</span> that can be of any type since
it will be converted to type array. The array will contain the column
values starting at array index 0.

`row`  
The row number.

### 返回值

Returns the number of columns in the result; **`false`** on error.

### 范例

**示例 \#1 <span class="function">odbc\_fetch\_into</span> examples**

``` php
<?php
$rc = odbc_fetch_into($res_id, $my_array);
?>
```

or

``` php
<?php
$rc = odbc_fetch_into($res_id, $my_array, 2);
?>
```

odbc\_fetch\_object
===================

Fetch a result row as an object

### 说明

<span class="type"><span class="type">stdClass</span><span
class="type">false</span></span> <span
class="methodname">odbc\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> \[, <span class="methodparam"><span
class="type">int</span> `$row`<span class="initializer"> =
-1</span></span> \] )

Fetch an <span class="type">object</span> from an ODBC query.

### 参数

`statement`  
The result resource from <span class="function">odbc\_exec</span>.

`row`  
Optionally choose which row number to retrieve.

### 返回值

Returns an object that corresponds to the fetched row, or **`false`** if
there are no more rows.

### 注释

> **Note**: <span class="simpara"> This function exists when compiled
> with DBMaker, IBM DB2 or UnixODBC support. </span>

### 参见

-   <span class="function">odbc\_fetch\_row</span>
-   <span class="function">odbc\_fetch\_array</span>
-   <span class="function">odbc\_num\_rows</span>

odbc\_fetch\_row
================

Fetch a row

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> \[, <span class="methodparam"><span
class="type"><span class="type">int</span><span
class="type">null</span></span> `$row`<span class="initializer"> =
**`null`**</span></span> \] )

Fetches a row of the data that was returned by <span
class="function">odbc\_do</span> or <span
class="function">odbc\_exec</span>. After <span
class="function">odbc\_fetch\_row</span> is called, the fields of that
row can be accessed with <span class="function">odbc\_result</span>.

### 参数

`statement`  
The result identifier.

`row`  
If `row` is not specified, <span
class="function">odbc\_fetch\_row</span> will try to fetch the next row
in the result set. Calls to <span
class="function">odbc\_fetch\_row</span> with and without `row` can be
mixed.

To step through the result more than once, you can call <span
class="function">odbc\_fetch\_row</span> with `row` 1, and then continue
doing <span class="function">odbc\_fetch\_row</span> without `row` to
review the result. If a driver doesn't support fetching rows by number,
the `row` parameter is ignored.

### 返回值

Returns **`true`** if there was a row, **`false`** otherwise.

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 8.0.0 | `row` is nullable now. |

odbc\_field\_len
================

Get the length (precision) of a field

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">odbc\_field\_len</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$field`</span> )

Gets the length of the field referenced by number in the given result
identifier.

### 参数

`statement`  
The result identifier.

`field`  
The field number. Field numbering starts at 1.

### 返回值

Returns the field length, or **`false`** on error.

### 参见

-   <span class="function">odbc\_field\_scale</span> to get the scale of
    a floating point number

odbc\_field\_name
=================

Get the columnname

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">odbc\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$field`</span> )

Gets the name of the field occupying the given column number in the
given result identifier.

### 参数

`statement`  
The result identifier.

`field`  
The field number. Field numbering starts at 1.

### 返回值

Returns the field name as a string, or **`false`** on error.

odbc\_field\_num
================

Return column number

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">odbc\_field\_num</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">string</span> `$field`</span> )

Gets the number of the column slot that corresponds to the named field
in the given result identifier.

### 参数

`statement`  
The result identifier.

`field`  
The field name.

### 返回值

Returns the field number as a integer, or **`false`** on error. Field
numbering starts at 1.

odbc\_field\_precision
======================

别名 <span class="function">odbc\_field\_len</span>

### 说明

此函数是该函数的别名： <span class="function">odbc\_field\_len</span>.

### 参见

-   <span class="function">odbc\_field\_scale</span> to get the scale of
    a floating point number.

odbc\_field\_scale
==================

Get the scale of a field

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">odbc\_field\_scale</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$field`</span> )

Gets the scale of the field referenced by number in the given result
identifier.

### 参数

`statement`  
The result identifier.

`field`  
The field number. Field numbering starts at 1.

### 返回值

Returns the field scale as a integer, or **`false`** on error.

odbc\_field\_type
=================

Datatype of a field

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">odbc\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$field`</span> )

Gets the SQL type of the field referenced by number in the given result
identifier.

### 参数

`statement`  
The result identifier.

`field`  
The field number. Field numbering starts at 1.

### 返回值

Returns the field type as a string, or **`false`** on error.

odbc\_foreignkeys
=================

Retrieves a list of foreign keys

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_foreignkeys</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$pk_catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$pk_schema`</span> , <span
class="methodparam"><span class="type">string</span> `$pk_table`</span>
, <span class="methodparam"><span class="type">string</span>
`$fk_catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$fk_schema`</span> , <span
class="methodparam"><span class="type">string</span> `$fk_table`</span>
)

Retrieves a list of foreign keys in the specified table or a list of
foreign keys in other tables that refer to the primary key in the
specified table

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`pk_catalog`  
The catalog ('qualifier' in ODBC 2 parlance) of the primary key table.

`pk_schema`  
The schema ('owner' in ODBC 2 parlance) of the primary key table.

`pk_table`  
The primary key table.

`pk_catalog`  
The catalog ('qualifier' in ODBC 2 parlance) of the foreign key table.

`fk_schema`  
The schema ('owner' in ODBC 2 parlance) of the foreign key table.

`fk_table`  
The foreign key table.

### 返回值

Returns an ODBC result identifier 或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*PKTABLE\_CAT*</span>
-   <span class="simpara">*PKTABLE\_SCHEM*</span>
-   <span class="simpara">*PKTABLE\_NAME*</span>
-   <span class="simpara">*PKCOLUMN\_NAME*</span>
-   <span class="simpara">*FKTABLE\_CAT*</span>
-   <span class="simpara">*FKTABLE\_SCHEM*</span>
-   <span class="simpara">*FKTABLE\_NAME*</span>
-   <span class="simpara">*FKCOLUMN\_NAME*</span>
-   <span class="simpara">*KEY\_SEQ*</span>
-   <span class="simpara">*UPDATE\_RULE*</span>
-   <span class="simpara">*DELETE\_RULE*</span>
-   <span class="simpara">*FK\_NAME*</span>
-   <span class="simpara">*PK\_NAME*</span>
-   <span class="simpara">*DEFERRABILITY*</span>

Drivers can report additional columns.

If the foreign keys associated with a primary key are requested, the
result set is ordered by *FKTABLE\_CAT*, *FKTABLE\_SCHEM*,
*FKTABLE\_NAME* and *KEY\_SEQ*. If the primary keys associated with a
foreign key are requested, the result set is ordered by *PKTABLE\_CAT*,
*PKTABLE\_SCHEM*, *PKTABLE\_NAME* and *KEY\_SEQ*.

If `pk_table` contains a table name, <span
class="function">odbc\_foreignkeys</span> returns a result set
containing the primary key of the specified table and all of the foreign
keys that refer to it.

If `fk_table` contains a table name, <span
class="function">odbc\_foreignkeys</span> returns a result set
containing all of the foreign keys in the specified table and the
primary keys (in other tables) to which they refer.

If both `pk_table` and `fk_table` contain table names, <span
class="function">odbc\_foreignkeys</span> returns the foreign keys in
the table specified in `fk_table` that refer to the primary key of the
table specified in `pk_table`. This should be one key at most.

### 参见

-   <span class="function">odbc\_tables</span>
-   <span class="function">odbc\_primarykeys</span>

odbc\_free\_result
==================

Free resources associated with a result

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> )

Free resources associated with a result.

<span class="function">odbc\_free\_result</span> only needs to be called
if you are worried about using too much memory while your script is
running. All result memory will automatically be freed when the script
is finished.

### 参数

`statement`  
The result identifier.

### 返回值

Always returns **`true`**.

### 注释

> **Note**:
>
> If auto-commit is disabled (see <span
> class="function">odbc\_autocommit</span>) and you call <span
> class="function">odbc\_free\_result</span> before committing, all
> pending transactions are rolled back.

odbc\_gettypeinfo
=================

Retrieves information about data types supported by the data source

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_gettypeinfo</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$data_type`<span class="initializer"> = 0</span></span> \] )

Retrieves information about data types supported by the data source.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`data_type`  
The data type, which can be used to restrict the information to a single
data type.

### 返回值

Returns an ODBC result identifier or **`false`** on failure.

The result set has the following columns:

-   <span class="simpara">TYPE\_NAME</span>
-   <span class="simpara">DATA\_TYPE</span>
-   <span class="simpara">PRECISION</span>
-   <span class="simpara">LITERAL\_PREFIX</span>
-   <span class="simpara">LITERAL\_SUFFIX</span>
-   <span class="simpara">CREATE\_PARAMS</span>
-   <span class="simpara">NULLABLE</span>
-   <span class="simpara">CASE\_SENSITIVE</span>
-   <span class="simpara">SEARCHABLE</span>
-   <span class="simpara">UNSIGNED\_ATTRIBUTE</span>
-   <span class="simpara">MONEY</span>
-   <span class="simpara">AUTO\_INCREMENT</span>
-   <span class="simpara">LOCAL\_TYPE\_NAME</span>
-   <span class="simpara">MINIMUM\_SCALE</span>
-   <span class="simpara">MAXIMUM\_SCALE</span>

The result set is ordered by DATA\_TYPE and TYPE\_NAME.

odbc\_longreadlen
=================

Handling of LONG columns

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_longreadlen</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$length`</span> )

Controls handling of *LONG*, *LONGVARCHAR* and *LONGVARBINARY* columns.
The default length can be set using the
<a href="/book/uodbc.html#" class="link">uodbc.defaultlrl</a> `php.ini`
directive.

### 参数

`statement`  
The result identifier.

`length`  
The number of bytes returned to PHP is controlled by the parameter
length. If it is set to *0*, long column data is passed through to the
client (i.e. printed) when retrieved with <span
class="function">odbc\_result</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

> **Note**:
>
> Handling of *LONGVARBINARY* columns is also affected by <span
> class="function">odbc\_binmode</span>.

odbc\_next\_result
==================

Checks if multiple results are available

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> )

Checks if there are more result sets available as well as allowing
access to the next result set via <span
class="function">odbc\_fetch\_array</span>, <span
class="function">odbc\_fetch\_row</span>, <span
class="function">odbc\_result</span>, etc.

### 参数

`statement`  
The result identifier.

### 返回值

Returns **`true`** if there are more result sets, **`false`** otherwise.

### 范例

**示例 \#1 <span class="function">odbc\_next\_result</span>**

``` php
<?php
$r_Connection = odbc_connect($dsn, $username, $password);

$s_SQL = <<<END_SQL
SELECT 'A'
SELECT 'B'
SELECT 'C'
END_SQL;

$r_Results = odbc_exec($r_Connection, $s_SQL);

$a_Row1 = odbc_fetch_array($r_Results);
$a_Row2 = odbc_fetch_array($r_Results);
echo "Dump first result set";
var_dump($a_Row1, $a_Row2);

echo "Get second results set ";
var_dump(odbc_next_result($r_Results));

$a_Row1 = odbc_fetch_array($r_Results);
$a_Row2 = odbc_fetch_array($r_Results);
echo "Dump second result set ";
var_dump($a_Row1, $a_Row2);

echo "Get third results set ";
var_dump(odbc_next_result($r_Results));

$a_Row1 = odbc_fetch_array($r_Results);
$a_Row2 = odbc_fetch_array($r_Results);
echo "Dump third result set ";
var_dump($a_Row1, $a_Row2);

echo "Try for a fourth result set ";
var_dump(odbc_next_result($r_Results));
?>
```

以上例程会输出：

    Dump first result set array(1) {
      ["A"]=>
      string(1) "A"
    }
    bool(false)
    Get second results set bool(true)
    Dump second result set array(1) {
      ["B"]=>
      string(1) "B"
    }
    bool(false)
    Get third results set bool(true)
    Dump third result set array(1) {
      ["C"]=>
      string(1) "C"
    }
    bool(false)
    Try for a fourth result set bool(false)

odbc\_num\_fields
=================

Number of columns in a result

### 说明

<span class="type">int</span> <span
class="methodname">odbc\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> )

Gets the number of fields (columns) in an ODBC result.

### 参数

`statement`  
The result identifier returned by <span
class="function">odbc\_exec</span>.

### 返回值

Returns the number of fields, or -1 on error.

odbc\_num\_rows
===============

Number of rows in a result

### 说明

<span class="type">int</span> <span
class="methodname">odbc\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> )

Gets the number of rows in a result. For INSERT, UPDATE and DELETE
statements <span class="function">odbc\_num\_rows</span> returns the
number of rows affected. For a SELECT clause this *can* be the number of
rows available.

### 参数

`statement`  
The result identifier returned by <span
class="function">odbc\_exec</span>.

### 返回值

Returns the number of rows in an ODBC result. This function will return
-1 on error.

### 注释

> **Note**:
>
> Using <span class="function">odbc\_num\_rows</span> to determine the
> number of rows available after a SELECT will return -1 with many
> drivers.

odbc\_pconnect
==============

Open a persistent database connection

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_pconnect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$user`</span> , <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">int</span> `$cursor_option`<span
class="initializer"> = **`SQL_CUR_USE_DRIVER`**</span></span> \] )

Opens a persistent database connection.

This function is much like <span class="function">odbc\_connect</span>,
except that the connection is not really closed when the script has
finished. Future requests for a connection with the same `dsn`, `user`,
`password` combination (via <span class="function">odbc\_connect</span>
and <span class="function">odbc\_pconnect</span>) can reuse the
persistent connection.

### 参数

See <span class="function">odbc\_connect</span> for details.

### 返回值

Returns an ODBC connection, 或者在失败时返回 **`false`**. error.

### 注释

> **Note**: <span class="simpara"> Persistent connections have no effect
> if PHP is used as a CGI program. </span>

### 参见

-   <span class="function">odbc\_connect</span>
-   <a href="/features/persistent-connections.html" class="link">Persistent Database Connections</a>

odbc\_prepare
=============

Prepares a statement for execution

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

Prepares a statement for execution. The result identifier can be used
later to execute the statement with <span
class="function">odbc\_execute</span>.

Some databases (such as IBM DB2, MS SQL Server, and Oracle) support
stored procedures that accept parameters of type IN, INOUT, and OUT as
defined by the ODBC specification. However, the Unified ODBC driver
currently only supports parameters of type IN to stored procedures.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`query`  
The query string statement being prepared.

### 返回值

Returns an ODBC result identifier if the SQL command was prepared
successfully. Returns **`false`** on error.

### 范例

**示例 \#1 <span class="function">odbc\_execute</span> and <span
class="function">odbc\_prepare</span> example**

In the following code, `$success` will only be **`true`** if all three
parameters to myproc are IN parameters:

``` php
<?php
$a = 1;
$b = 2;
$c = 3;
$stmt    = odbc_prepare($conn, 'CALL myproc(?,?,?)');
$success = odbc_execute($stmt, array($a, $b, $c));
?>
```

If you need to call a stored procedure using INOUT or OUT parameters,
the recommended workaround is to use a native extension for your
database (for example,
<a href="/book/oci8.html#OCI8%20函数" class="link">oci8</a> for Oracle).

### 参见

-   <span class="function">odbc\_execute</span>

odbc\_primarykeys
=================

Gets the primary keys for a table

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_primarykeys</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$schema`</span> , <span
class="methodparam"><span class="type">string</span> `$table`</span> )

Returns a result identifier that can be used to fetch the column names
that comprise the primary key for a table.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance).

`table`  

### 返回值

Returns an ODBC result identifier 或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*TABLE\_CAT*</span>
-   <span class="simpara">*TABLE\_SCHEM*</span>
-   <span class="simpara">*TABLE\_NAME*</span>
-   <span class="simpara">*COLUMN\_NAME*</span>
-   <span class="simpara">*KEY\_SEQ*</span>
-   <span class="simpara">*PK\_NAME*</span>

Drivers can report additional columns.

The result set is ordered by *TABLE\_CAT*, *TABLE\_SCHEM*, *TABLE\_NAME*
and *KEY\_SEQ*.

### 范例

**示例 \#1 List primary Keys of a Column**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$primarykeys = odbc_primarykeys($conn, 'TutorialDB', 'dbo', 'TEST');
while (($row = odbc_fetch_array($primarykeys))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [TABLE_CAT] => TutorialDB
        [TABLE_SCHEM] => dbo
        [TABLE_NAME] => TEST
        [COLUMN_NAME] => id
        [KEY_SEQ] => 1
        [PK_NAME] => PK__TEST__3213E83FE141F843
    )

### 参见

-   <span class="function">odbc\_tables</span>
-   <span class="function">odbc\_foreignkeys</span>

odbc\_procedurecolumns
======================

Retrieve information about parameters to procedures

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_procedurecolumns</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$schema`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$procedure`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$column`<span class="initializer"> = **`null`**</span></span> \]\]\]\]
)

Retrieve information about parameters to procedures.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance). 此参数接受下列查询模式： *%*
来匹配零到多个字符， *\_* 来匹配单个字符。

`procedure`  
The proc. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

`column`  
The column. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

### 返回值

Returns the list of input and output parameters, as well as the columns
that make up the result set for the specified procedures. Returns an
ODBC result identifier 或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*PROCEDURE\_CAT*</span>
-   <span class="simpara">*PROCEDURE\_SCHEM*</span>
-   <span class="simpara">*PROCEDURE\_NAME*</span>
-   <span class="simpara">*COLUMN\_NAME*</span>
-   <span class="simpara">*COLUMN\_TYPE*</span>
-   <span class="simpara">*DATA\_TYPE*</span>
-   <span class="simpara">*TYPE\_NAME*</span>
-   <span class="simpara">*COLUMN\_SIZE*</span>
-   <span class="simpara">*BUFFER\_LENGTH*</span>
-   <span class="simpara">*DECIMAL\_DIGITS*</span>
-   <span class="simpara">*NUM\_PREC\_RADIX*</span>
-   <span class="simpara">*NULLABLE*</span>
-   <span class="simpara">*REMARKS*</span>
-   <span class="simpara">*COLUMN\_DEF*</span>
-   <span class="simpara">*SQL\_DATA\_TYPE*</span>
-   <span class="simpara">*SQL\_DATETIME\_SUB*</span>
-   <span class="simpara">*CHAR\_OCTET\_LENGTH*</span>
-   <span class="simpara">*ORDINAL\_POSITION*</span>
-   <span class="simpara">*IS\_NULLABLE*</span>

Drivers can report additional columns.

The result set is ordered by *PROCEDURE\_CAT*, *PROCEDURE\_SCHEM*,
*PROCEDURE\_NAME* and *COLUMN\_TYPE*.

### 更新日志

| 版本  | 说明                                                                                        |
|-------|---------------------------------------------------------------------------------------------|
| 8.0.0 | Prior to this version, the function could only be called with either one or five arguments. |

### 范例

**示例 \#1 List Columns of a stored Procedure**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$columns = odbc_procedurecolumns($conn, 'TutorialDB', 'dbo', 'GetEmployeeSalesYTD;1', '%');
while (($row = odbc_fetch_array($columns))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [PROCEDURE_CAT] => TutorialDB
        [PROCEDURE_SCHEM] => dbo
        [PROCEDURE_NAME] => GetEmployeeSalesYTD;1
        [COLUMN_NAME] => @SalesPerson
        [COLUMN_TYPE] => 1
        [DATA_TYPE] => -9
        [TYPE_NAME] => nvarchar
        [COLUMN_SIZE] => 50
        [BUFFER_LENGTH] => 100
        [DECIMAL_DIGITS] =>
        [NUM_PREC_RADIX] =>
        [NULLABLE] => 1
        [REMARKS] =>
        [COLUMN_DEF] =>
        [SQL_DATA_TYPE] => -9
        [SQL_DATETIME_SUB] =>
        [CHAR_OCTET_LENGTH] => 100
        [ORDINAL_POSITION] => 1
        [IS_NULLABLE] => YES
    )

### 参见

-   <span class="function">odbc\_columns</span>

odbc\_procedures
================

Get the list of procedures stored in a specific data source

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_procedures</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$schema`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$procedure`<span class="initializer"> = **`null`**</span></span> \]\]\]
)

Lists all procedures in the requested range.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance). 此参数接受下列查询模式： *%*
来匹配零到多个字符， *\_* 来匹配单个字符。

`procedure`  
The name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

### 返回值

Returns an ODBC result identifier containing the information
或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*PROCEDURE\_CAT*</span>
-   <span class="simpara">*PROCEDURE\_SCHEM*</span>
-   <span class="simpara">*PROCEDURE\_NAME*</span>
-   <span class="simpara">*NUM\_INPUT\_PARAMS*</span>
-   <span class="simpara">*NUM\_OUTPUT\_PARAMS*</span>
-   <span class="simpara">*NUM\_RESULT\_SETS*</span>
-   <span class="simpara">*REMARKS*</span>
-   <span class="simpara">*PROCEDURE\_TYPE*</span>

Drivers can report additional columns.

The result set is ordered by *PROCEDURE\_CAT*, *PROCEDURE\_SCHEMA* and
*PROCEDURE\_NAME*.

### 更新日志

| 版本  | 说明                                                                                        |
|-------|---------------------------------------------------------------------------------------------|
| 8.0.0 | Prior to this version, the function could only be called with either one or four arguments. |

### 范例

**示例 \#1 List stored Procedures of a Database**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$procedures = odbc_procedures($conn, $catalog, $schema, '%');
while (($row = odbc_fetch_array($procedures))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [PROCEDURE_CAT] => TutorialDB
        [PROCEDURE_SCHEM] => dbo
        [PROCEDURE_NAME] => GetEmployeeSalesYTD;1
        [NUM_INPUT_PARAMS] => -1
        [NUM_OUTPUT_PARAMS] => -1
        [NUM_RESULT_SETS] => -1
        [REMARKS] =>
        [PROCEDURE_TYPE] => 2
    )

### 参见

-   <span class="function">odbc\_procedurecolumns</span>
-   <span class="function">odbc\_tables</span>

odbc\_result\_all
=================

Print result as HTML table

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">odbc\_result\_all</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> \[, <span class="methodparam"><span
class="type">string</span> `$format`<span class="initializer"> =
""</span></span> \] )

Prints all rows from a result identifier produced by <span
class="function">odbc\_exec</span>. The result is printed in HTML table
format. The data is *not* escaped.

This function is not supposed to be used in production environments; it
is merely meant for development purposes, to get a result set quickly
rendered.

### 参数

`statement`  
The result identifier.

`format`  
Additional overall table formatting.

### 返回值

Returns the number of rows in the result or **`false`** on error.

odbc\_result
============

Get result data

### 说明

<span class="type"><span class="type">string</span><span
class="type">bool</span><span class="type">null</span></span> <span
class="methodname">odbc\_result</span> ( <span class="methodparam"><span
class="type">resource</span> `$statement`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">int</span></span>
`$field`</span> )

Get result data

### 参数

`statement`  
The ODBC <span class="type">resource</span>.

`field`  
The field name being retrieved. It can either be an integer containing
the column number of the field you want; or it can be a string
containing the name of the field.

### 返回值

Returns the string contents of the field, **`false`** on error,
**`null`** for NULL data, or **`true`** for binary data.

### 范例

The first call to <span class="function">odbc\_result</span> returns the
value of the third field in the current record of the query result. The
second function call to <span class="function">odbc\_result</span>
returns the value of the field whose field name is "val" in the current
record of the query result. An error occurs if a column number parameter
for a field is less than one or exceeds the number of columns (or
fields) in the current record. Similarly, an error occurs if a field
with a name that is not one of the fieldnames of the table(s) that
is(are) being queried.

**示例 \#1 <span class="function">odbc\_result</span> examples**

``` php
<?php
$item_3   = odbc_result($Query_ID, 3);
$item_val = odbc_result($Query_ID, "val");
?>
```

### 注释

Field indices start from 1. Regarding the way binary or long column data
is returned refer to <span class="function">odbc\_binmode</span> and
<span class="function">odbc\_longreadlen</span>.

odbc\_rollback
==============

Rollback a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_rollback</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> )

Rolls back all pending statements on the connection.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

odbc\_setoption
===============

Adjust ODBC settings

### 说明

<span class="type">bool</span> <span
class="methodname">odbc\_setoption</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type">int</span> `$which`</span>
, <span class="methodparam"><span class="type">int</span>
`$option`</span> , <span class="methodparam"><span
class="type">int</span> `$value`</span> )

This function allows fiddling with the ODBC options for a particular
connection or query result. It was written to help find work around to
problems in quirky ODBC drivers. You should probably only use this
function if you are an ODBC programmer and understand the effects the
various options will have. You will certainly need a good ODBC reference
to explain all the different options and values that can be used.
Different driver versions support different options.

Because the effects may vary depending on the ODBC driver, use of this
function in scripts to be made publicly available is strongly
discouraged. Also, some ODBC options are not available to this function
because they must be set before the connection is established or the
query is prepared. However, if on a particular job it can make PHP work
so your boss doesn't tell you to use a commercial product, that's all
that really matters.

### 参数

`odbc`  
Is a connection id or result id on which to change the settings. For
SQLSetConnectOption(), this is a connection id. For SQLSetStmtOption(),
this is a result id.

`which`  
Is the ODBC function to use. The value should be 1 for
SQLSetConnectOption() and 2 for SQLSetStmtOption().

`option`  
The option to set.

`value`  
The value for the given `option`.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">odbc\_setoption</span> examples**

``` php
<?php
// 1. Option 102 of SQLSetConnectOption() is SQL_AUTOCOMMIT.
//    Value 1 of SQL_AUTOCOMMIT is SQL_AUTOCOMMIT_ON.
//    This example has the same effect as
//    odbc_autocommit($conn, true);

odbc_setoption($conn, 1, 102, 1);

// 2. Option 0 of SQLSetStmtOption() is SQL_QUERY_TIMEOUT.
//    This example sets the query to timeout after 30 seconds.

$result = odbc_prepare($conn, $sql);
odbc_setoption($result, 2, 0, 30);
odbc_execute($result);
?>
```

odbc\_specialcolumns
====================

Retrieves special columns

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_specialcolumns</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$schema`</span> , <span
class="methodparam"><span class="type">string</span> `$table`</span> ,
<span class="methodparam"><span class="type">int</span> `$scope`</span>
, <span class="methodparam"><span class="type">int</span>
`$nullable`</span> )

Retrieves either the optimal set of columns that uniquely identifies a
row in the table, or columns that are automatically updated when any
value in the row is updated by a transaction.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`type`  
<span class="simpara"> When the type argument is **`SQL_BEST_ROWID`**,
<span class="function">odbc\_specialcolumns</span> returns the column or
columns that uniquely identify each row in the table. </span> <span
class="simpara"> When the type argument is **`SQL_ROWVER`**, <span
class="function">odbc\_specialcolumns</span> returns the column or
columns in the specified table, if any, that are automatically updated
by the data source when any value in the row is updated by any
transaction. </span>

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance).

`table`  
The table.

`scope`  
The scope, which orders the result set. One of **`SQL_SCOPE_CURROW`**,
**`SQL_SCOPE_TRANSACTION`** or **`SQL_SCOPE_SESSION`**.

`nullable`  
Determines whether to return special columns that can have a NULL value.
One of **`SQL_NO_NULLS`** or **`SQL_NULLABLE `**.

### 返回值

Returns an ODBC result identifier or **`false`** on failure.

The result set has the following columns:

-   <span class="simpara">*SCOPE*</span>
-   <span class="simpara">*COLUMN\_NAME*</span>
-   <span class="simpara">*DATA\_TYPE*</span>
-   <span class="simpara">*TYPE\_NAME*</span>
-   <span class="simpara">*COLUMN\_SIZE*</span>
-   <span class="simpara">*BUFFER\_LENGTH*</span>
-   <span class="simpara">*DECIMAL\_DIGITS*</span>
-   <span class="simpara">*PSEUDO\_COLUMN*</span>

Drivers can report additional columns.

The result set is ordered by *SCOPE*.

### 参见

-   <span class="function">odbc\_tables</span>

odbc\_statistics
================

Retrieve statistics about a table

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_statistics</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$schema`</span> , <span
class="methodparam"><span class="type">string</span> `$table`</span> ,
<span class="methodparam"><span class="type">int</span> `$unique`</span>
, <span class="methodparam"><span class="type">int</span>
`$accuracy`</span> )

Get statistics about a table and its indexes.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance).

`table`  
The table name.

`unique`  
The type of the index. One of **`SQL_INDEX_UNIQUE`** or
**`SQL_INDEX_ALL`**.

`accuracy`  
One of **`SQL_ENSURE`** or **`SQL_QUICK`**. The latter requests that the
driver retrieve the *CARDINALITY* and *PAGES* only if they are readily
available from the server.

### 返回值

Returns an ODBC result identifier 或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*TABLE\_CAT*</span>
-   <span class="simpara">*TABLE\_SCHEM*</span>
-   <span class="simpara">*TABLE\_NAME*</span>
-   <span class="simpara">*NON\_UNIQUE*</span>
-   <span class="simpara">*INDEX\_QUALIFIER*</span>
-   <span class="simpara">*INDEX\_NAME*</span>
-   <span class="simpara">*TYPE*</span>
-   <span class="simpara">*ORDINAL\_POSITION*</span>
-   <span class="simpara">*COLUMN\_NAME*</span>
-   <span class="simpara">*ASC\_OR\_DESC*</span>
-   <span class="simpara">*CARDINALITY*</span>
-   <span class="simpara">*PAGES*</span>
-   <span class="simpara">*FILTER\_CONDITION*</span>

Drivers can report additional columns.

The result set is ordered by *NON\_UNIQUE*, *TYPE*, *INDEX\_QUALIFIER*,
*INDEX\_NAME* and *ORDINAL\_POSITION*.

### 范例

**示例 \#1 List Statistics of a Table**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$statistics = odbc_statistics($conn, 'TutorialDB', 'dbo', 'TEST', SQL_INDEX_UNIQUE, SQL_QUICK);
while (($row = odbc_fetch_array($statistics))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [TABLE_CAT] => TutorialDB
        [TABLE_SCHEM] => dbo
        [TABLE_NAME] => TEST
        [NON_UNIQUE] =>
        [INDEX_QUALIFIER] =>
        [INDEX_NAME] =>
        [TYPE] => 0
        [ORDINAL_POSITION] =>
        [COLUMN_NAME] =>
        [ASC_OR_DESC] =>
        [CARDINALITY] => 15
        [PAGES] => 3
        [FILTER_CONDITION] =>
    )

### 参见

-   <span class="function">odbc\_tables</span>

odbc\_tableprivileges
=====================

Lists tables and the privileges associated with each table

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_tableprivileges</span> ( <span
class="methodparam"><span class="type">resource</span> `$odbc`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`</span> , <span class="methodparam"><span
class="type">string</span> `$schema`</span> , <span
class="methodparam"><span class="type">string</span> `$table`</span> )

Lists tables in the requested range and the privileges associated with
each table.

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance). 此参数接受下列查询模式： *%*
来匹配零到多个字符， *\_* 来匹配单个字符。

`table`  
The name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

### 返回值

An ODBC result identifier 或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*TABLE\_CAT*</span>
-   <span class="simpara">*TABLE\_SCHEM*</span>
-   <span class="simpara">*TABLE\_NAME*</span>
-   <span class="simpara">*GRANTOR*</span>
-   <span class="simpara">*GRANTEE*</span>
-   <span class="simpara">*PRIVILEGE*</span>
-   <span class="simpara">*IS\_GRANTABLE*</span>

Drivers can report additional columns.

The result set is ordered by *TABLE\_CAT*, *TABLE\_SCHEM*,
*TABLE\_NAME*, *PRIVILEGE* and *GRANTEE*.

### 范例

**示例 \#1 List Privileges of a Table**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$privileges = odbc_tableprivileges($conn, 'SalesOrders', 'dbo', 'Orders');
while (($row = odbc_fetch_array($privileges))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [TABLE_CAT] => SalesOrders
        [TABLE_SCHEM] => dbo
        [TABLE_NAME] => Orders
        [GRANTOR] => dbo
        [GRANTEE] => dbo
        [PRIVILEGE] => DELETE
        [IS_GRANTABLE] => YES
    )

### 参见

-   <span class="function">odbc\_tables</span>

odbc\_tables
============

Get the list of table names stored in a specific data source

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">odbc\_tables</span> ( <span class="methodparam"><span
class="type">resource</span> `$odbc`</span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$catalog`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$schema`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$table`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$types`<span class="initializer"> = **`null`**</span></span> \]\]\]\] )

Lists all tables in the requested range.

To support enumeration of qualifiers, owners, and table types, the
following special semantics for the `catalog`, `schema`, `table`, and
`table_type` are available:

-   <span class="simpara"> If `catalog` is a single percent character
    (%) and `schema` and `table` are empty strings, then the result set
    contains a list of valid qualifiers for the data source. (All
    columns except the TABLE\_QUALIFIER column contain NULLs.) </span>
-   <span class="simpara"> If `schema` is a single percent character (%)
    and `catalog` and `table` are empty strings, then the result set
    contains a list of valid owners for the data source. (All columns
    except the TABLE\_OWNER column contain NULLs.) </span>
-   <span class="simpara"> If `table_type` is a single percent character
    (%) and `catalog`, `schema` and `table` are empty strings, then the
    result set contains a list of valid table types for the data source.
    (All columns except the TABLE\_TYPE column contain NULLs.) </span>

### 参数

`odbc`  
ODBC 连接标识符，详见 <span class="function">odbc\_connect</span>。

`catalog`  
The catalog ('qualifier' in ODBC 2 parlance).

`schema`  
The schema ('owner' in ODBC 2 parlance). 此参数接受下列查询模式： *%*
来匹配零到多个字符， *\_* 来匹配单个字符。

`table`  
The name. 此参数接受下列查询模式： *%* 来匹配零到多个字符， *\_*
来匹配单个字符。

`types`  
If `table_type` is not an empty string, it must contain a list of
comma-separated values for the types of interest; each value may be
enclosed in single quotes (*'*) or unquoted. For example,
*'TABLE','VIEW'* or *TABLE, VIEW*. If the data source does not support a
specified table type, <span class="function">odbc\_tables</span> does
not return any results for that type.

### 返回值

Returns an ODBC result identifier containing the information
或者在失败时返回 **`false`**.

The result set has the following columns:

-   <span class="simpara">*TABLE\_CAT*</span>
-   <span class="simpara">*TABLE\_SCHEM*</span>
-   <span class="simpara">*TABLE\_NAME*</span>
-   <span class="simpara">*TABLE\_TYPE*</span>
-   <span class="simpara">*REMARKS*</span>

Drivers can report additional columns.

The result set is ordered by *TABLE\_TYPE*, *TABLE\_CAT*, *TABLE\_SCHEM*
and *TABLE\_NAME*.

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 8.0.0 | `schema`, `table` and `types` are now nullable. |

### 范例

**示例 \#1 List Tables in a Catalog**

``` php
<?php
$conn = odbc_connect($dsn, $user, $pass);
$tables = odbc_tables($conn, 'SalesOrders', 'dbo', '%', 'TABLE');
while (($row = odbc_fetch_array($tables))) {
    print_r($row);
    break; // further rows omitted for brevity
}
?>
```

以上例程的输出类似于：

    Array
    (
        [TABLE_CAT] => SalesOrders
        [TABLE_SCHEM] => dbo
        [TABLE_NAME] => Orders
        [TABLE_TYPE] => TABLE
        [REMARKS] =>
    )

### 参见

-   <span class="function">odbc\_tableprivileges</span>
-   <span class="function">odbc\_columns</span>
-   <span class="function">odbc\_specialcolumns</span>
-   <span class="function">odbc\_statistics</span>
-   <span class="function">odbc\_procedures</span>

**目录**

-   [odbc\_autocommit](/book/uodbc.html#odbc_autocommit) — Toggle
    autocommit behaviour
-   [odbc\_binmode](/book/uodbc.html#odbc_binmode) — Handling of binary
    column data
-   [odbc\_close\_all](/book/uodbc.html#odbc_close_all) — Close all ODBC
    connections
-   [odbc\_close](/book/uodbc.html#odbc_close) — Close an ODBC
    connection
-   [odbc\_columnprivileges](/book/uodbc.html#odbc_columnprivileges) —
    Lists columns and associated privileges for the given table
-   [odbc\_columns](/book/uodbc.html#odbc_columns) — Lists the column
    names in specified tables
-   [odbc\_commit](/book/uodbc.html#odbc_commit) — Commit an ODBC
    transaction
-   [odbc\_connect](/book/uodbc.html#odbc_connect) — Connect to a
    datasource
-   [odbc\_cursor](/book/uodbc.html#odbc_cursor) — Get cursorname
-   [odbc\_data\_source](/book/uodbc.html#odbc_data_source) — Returns
    information about available DSNs
-   [odbc\_do](/book/uodbc.html#odbc_do) — 别名 odbc\_exec
-   [odbc\_error](/book/uodbc.html#odbc_error) — Get the last error code
-   [odbc\_errormsg](/book/uodbc.html#odbc_errormsg) — Get the last
    error message
-   [odbc\_exec](/book/uodbc.html#odbc_exec) — Directly execute an SQL
    statement
-   [odbc\_execute](/book/uodbc.html#odbc_execute) — Execute a prepared
    statement
-   [odbc\_fetch\_array](/book/uodbc.html#odbc_fetch_array) — Fetch a
    result row as an associative array
-   [odbc\_fetch\_into](/book/uodbc.html#odbc_fetch_into) — Fetch one
    result row into array
-   [odbc\_fetch\_object](/book/uodbc.html#odbc_fetch_object) — Fetch a
    result row as an object
-   [odbc\_fetch\_row](/book/uodbc.html#odbc_fetch_row) — Fetch a row
-   [odbc\_field\_len](/book/uodbc.html#odbc_field_len) — Get the length
    (precision) of a field
-   [odbc\_field\_name](/book/uodbc.html#odbc_field_name) — Get the
    columnname
-   [odbc\_field\_num](/book/uodbc.html#odbc_field_num) — Return column
    number
-   [odbc\_field\_precision](/book/uodbc.html#odbc_field_precision) —
    别名 odbc\_field\_len
-   [odbc\_field\_scale](/book/uodbc.html#odbc_field_scale) — Get the
    scale of a field
-   [odbc\_field\_type](/book/uodbc.html#odbc_field_type) — Datatype of
    a field
-   [odbc\_foreignkeys](/book/uodbc.html#odbc_foreignkeys) — Retrieves a
    list of foreign keys
-   [odbc\_free\_result](/book/uodbc.html#odbc_free_result) — Free
    resources associated with a result
-   [odbc\_gettypeinfo](/book/uodbc.html#odbc_gettypeinfo) — Retrieves
    information about data types supported by the data source
-   [odbc\_longreadlen](/book/uodbc.html#odbc_longreadlen) — Handling of
    LONG columns
-   [odbc\_next\_result](/book/uodbc.html#odbc_next_result) — Checks if
    multiple results are available
-   [odbc\_num\_fields](/book/uodbc.html#odbc_num_fields) — Number of
    columns in a result
-   [odbc\_num\_rows](/book/uodbc.html#odbc_num_rows) — Number of rows
    in a result
-   [odbc\_pconnect](/book/uodbc.html#odbc_pconnect) — Open a persistent
    database connection
-   [odbc\_prepare](/book/uodbc.html#odbc_prepare) — Prepares a
    statement for execution
-   [odbc\_primarykeys](/book/uodbc.html#odbc_primarykeys) — Gets the
    primary keys for a table
-   [odbc\_procedurecolumns](/book/uodbc.html#odbc_procedurecolumns) —
    Retrieve information about parameters to procedures
-   [odbc\_procedures](/book/uodbc.html#odbc_procedures) — Get the list
    of procedures stored in a specific data source
-   [odbc\_result\_all](/book/uodbc.html#odbc_result_all) — Print result
    as HTML table
-   [odbc\_result](/book/uodbc.html#odbc_result) — Get result data
-   [odbc\_rollback](/book/uodbc.html#odbc_rollback) — Rollback a
    transaction
-   [odbc\_setoption](/book/uodbc.html#odbc_setoption) — Adjust ODBC
    settings
-   [odbc\_specialcolumns](/book/uodbc.html#odbc_specialcolumns) —
    Retrieves special columns
-   [odbc\_statistics](/book/uodbc.html#odbc_statistics) — Retrieve
    statistics about a table
-   [odbc\_tableprivileges](/book/uodbc.html#odbc_tableprivileges) —
    Lists tables and the privileges associated with each table
-   [odbc\_tables](/book/uodbc.html#odbc_tables) — Get the list of table
    names stored in a specific data source
