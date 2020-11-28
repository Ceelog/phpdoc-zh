IBM DB2, Cloudscape and Apache Derby
====================================

**目录**

-   [简介](/book/ibm-db2.html#简介)
-   [安装／配置](/book/ibm-db2.html#安装／配置)
    -   [需求](/book/ibm-db2.html#需求)
    -   [安装](/book/ibm-db2.html#安装)
    -   [运行时配置](/book/ibm-db2.html#运行时配置)
    -   [资源类型](/book/ibm-db2.html#资源类型)
-   [预定义常量](/book/ibm-db2.html#预定义常量)
-   [IBM DB2 函数](/book/ibm-db2.html#IBM%20DB2%20函数)
    -   [db2\_autocommit](/book/ibm-db2.html#db2_autocommit) — Returns
        or sets the AUTOCOMMIT state for a database connection
    -   [db2\_bind\_param](/book/ibm-db2.html#db2_bind_param) — Binds a
        PHP variable to an SQL statement parameter
    -   [db2\_client\_info](/book/ibm-db2.html#db2_client_info) —
        Returns an object with properties that describe the DB2 database
        client
    -   [db2\_close](/book/ibm-db2.html#db2_close) — Closes a database
        connection
    -   [db2\_column\_privileges](/book/ibm-db2.html#db2_column_privileges)
        — Returns a result set listing the columns and associated
        privileges for a table
    -   [db2\_columns](/book/ibm-db2.html#db2_columns) — Returns a
        result set listing the columns and associated metadata for a
        table
    -   [db2\_commit](/book/ibm-db2.html#db2_commit) — Commits a
        transaction
    -   [db2\_conn\_error](/book/ibm-db2.html#db2_conn_error) — Returns
        a string containing the SQLSTATE returned by the last connection
        attempt
    -   [db2\_conn\_errormsg](/book/ibm-db2.html#db2_conn_errormsg) —
        Returns the last connection error message and SQLCODE value
    -   [db2\_connect](/book/ibm-db2.html#db2_connect) — Returns a
        connection to a database
    -   [db2\_cursor\_type](/book/ibm-db2.html#db2_cursor_type) —
        Returns the cursor type used by a statement resource
    -   [db2\_escape\_string](/book/ibm-db2.html#db2_escape_string) —
        Used to escape certain characters
    -   [db2\_exec](/book/ibm-db2.html#db2_exec) — Executes an SQL
        statement directly
    -   [db2\_execute](/book/ibm-db2.html#db2_execute) — Executes a
        prepared SQL statement
    -   [db2\_fetch\_array](/book/ibm-db2.html#db2_fetch_array) —
        Returns an array, indexed by column position, representing a row
        in a result set
    -   [db2\_fetch\_assoc](/book/ibm-db2.html#db2_fetch_assoc) —
        Returns an array, indexed by column name, representing a row in
        a result set
    -   [db2\_fetch\_both](/book/ibm-db2.html#db2_fetch_both) — Returns
        an array, indexed by both column name and position, representing
        a row in a result set
    -   [db2\_fetch\_object](/book/ibm-db2.html#db2_fetch_object) —
        Returns an object with properties representing columns in the
        fetched row
    -   [db2\_fetch\_row](/book/ibm-db2.html#db2_fetch_row) — Sets the
        result set pointer to the next row or requested row
    -   [db2\_field\_display\_size](/book/ibm-db2.html#db2_field_display_size)
        — Returns the maximum number of bytes required to display a
        column
    -   [db2\_field\_name](/book/ibm-db2.html#db2_field_name) — Returns
        the name of the column in the result set
    -   [db2\_field\_num](/book/ibm-db2.html#db2_field_num) — Returns
        the position of the named column in a result set
    -   [db2\_field\_precision](/book/ibm-db2.html#db2_field_precision)
        — Returns the precision of the indicated column in a result set
    -   [db2\_field\_scale](/book/ibm-db2.html#db2_field_scale) —
        Returns the scale of the indicated column in a result set
    -   [db2\_field\_type](/book/ibm-db2.html#db2_field_type) — Returns
        the data type of the indicated column in a result set
    -   [db2\_field\_width](/book/ibm-db2.html#db2_field_width) —
        Returns the width of the current value of the indicated column
        in a result set
    -   [db2\_foreign\_keys](/book/ibm-db2.html#db2_foreign_keys) —
        Returns a result set listing the foreign keys for a table
    -   [db2\_free\_result](/book/ibm-db2.html#db2_free_result) — Frees
        resources associated with a result set
    -   [db2\_free\_stmt](/book/ibm-db2.html#db2_free_stmt) — Frees
        resources associated with the indicated statement resource
    -   [db2\_get\_option](/book/ibm-db2.html#db2_get_option) —
        Retrieves an option value for a statement resource or a
        connection resource
    -   [db2\_last\_insert\_id](/book/ibm-db2.html#db2_last_insert_id) —
        Returns the auto generated ID of the last insert query that
        successfully executed on this connection
    -   [db2\_lob\_read](/book/ibm-db2.html#db2_lob_read) — Gets a user
        defined size of LOB files with each invocation
    -   [db2\_next\_result](/book/ibm-db2.html#db2_next_result) —
        Requests the next result set from a stored procedure
    -   [db2\_num\_fields](/book/ibm-db2.html#db2_num_fields) — Returns
        the number of fields contained in a result set
    -   [db2\_num\_rows](/book/ibm-db2.html#db2_num_rows) — Returns the
        number of rows affected by an SQL statement
    -   [db2\_pclose](/book/ibm-db2.html#db2_pclose) — Closes a
        persistent database connection
    -   [db2\_pconnect](/book/ibm-db2.html#db2_pconnect) — Returns a
        persistent connection to a database
    -   [db2\_prepare](/book/ibm-db2.html#db2_prepare) — Prepares an SQL
        statement to be executed
    -   [db2\_primary\_keys](/book/ibm-db2.html#db2_primary_keys) —
        Returns a result set listing primary keys for a table
    -   [db2\_procedure\_columns](/book/ibm-db2.html#db2_procedure_columns)
        — Returns a result set listing stored procedure parameters
    -   [db2\_procedures](/book/ibm-db2.html#db2_procedures) — Returns a
        result set listing the stored procedures registered in a
        database
    -   [db2\_result](/book/ibm-db2.html#db2_result) — Returns a single
        column from a row in the result set
    -   [db2\_rollback](/book/ibm-db2.html#db2_rollback) — Rolls back a
        transaction
    -   [db2\_server\_info](/book/ibm-db2.html#db2_server_info) —
        Returns an object with properties that describe the DB2 database
        server
    -   [db2\_set\_option](/book/ibm-db2.html#db2_set_option) — Set
        options for connection or statement resources
    -   [db2\_special\_columns](/book/ibm-db2.html#db2_special_columns)
        — Returns a result set listing the unique row identifier columns
        for a table
    -   [db2\_statistics](/book/ibm-db2.html#db2_statistics) — Returns a
        result set listing the index and statistics for a table
    -   [db2\_stmt\_error](/book/ibm-db2.html#db2_stmt_error) — Returns
        a string containing the SQLSTATE returned by an SQL statement
    -   [db2\_stmt\_errormsg](/book/ibm-db2.html#db2_stmt_errormsg) —
        Returns a string containing the last SQL statement error message
    -   [db2\_table\_privileges](/book/ibm-db2.html#db2_table_privileges)
        — Returns a result set listing the tables and associated
        privileges in a database
    -   [db2\_tables](/book/ibm-db2.html#db2_tables) — Returns a result
        set listing the tables and associated metadata in a database

These functions enable you to access IBM DB2 Universal Database, IBM
Cloudscape, and Apache Derby databases using the DB2 Call Level
Interface (DB2 CLI).

安装／配置
==========

**目录**

-   [需求](/book/ibm-db2.html#需求)
-   [安装](/book/ibm-db2.html#安装)
-   [运行时配置](/book/ibm-db2.html#运行时配置)
-   [资源类型](/book/ibm-db2.html#资源类型)

需求
----

To connect to IBM DB2 Universal Database for Linux, UNIX, and Windows,
or IBM Cloudscape, or Apache Derby, you must install an IBM DB2
Universal Database client on the same computer on which you are running
PHP. The extension has been developed and tested with DB2 Version 8.2.

To connect to IBM DB2 Universal Database for z/OS or iSeries, you also
require IBM DB2 Connect or the equivalent DRDA gateway software.

Requirements on Linux or Unix
-----------------------------

The user invoking the PHP executable or SAPI must specify the DB2
instance before accessing these functions. You can set the name of the
DB2 instance in `php.ini` using the *ibm\_db2.instance\_name*
configuration option, or you can source the DB2 instance profile before
invoking the PHP executable.

If you created a DB2 instance named *db2inst1* in `/home/db2inst1/`, for
example, you can add the following line to `php.ini`:

    ibm_db2.instance_name=db2inst1

If you do not set this option in `php.ini`, you must issue the following
command to modify your environment variables to enable access to DB2:

    bash$ source /home/db2inst1/sqllib/db2profile

To enable your PHP-enabled Web server to access these functions, you
must either set the *ibm\_db2.instance\_name* configuration option in
`php.ini`, or source the DB2 instance environment in your Web server
start script (typically `/etc/init.d/httpd` or `/etc/init.d/apache`).

安装
----

To build the ibm\_db2 extension, the DB2 application development header
files and libraries must be installed on your system. DB2 does not
install these by default, so you may have to return to your DB2
installer and add this option. The header files are included with the
DB2 Application Development Client freely available for download from
the IBM DB2 Universal Database
<a href="https://www.ibm.com/developerworks/downloads/im/db2express/index.html" class="link external">» support site</a>.

If you add the DB2 application development header files and libraries to
a Linux or Unix operating system on which DB2 was already installed, you
must issue the command **db2iupdt -e** to update the symbolic links to
the header files and libraries in your DB2 instances.

ibm\_db2 is a
<a href="https://pecl.php.net/" class="link external">» PECL</a>
extension, so follow the instructions in
<a href="/install/pecl.html" class="xref">PECL 扩展库安装</a> to install
the ibm\_db2 extension for PHP. Issue the **configure** command to point
to the location of your DB2 header files and libraries as follows:

    bash$ ./configure --with-IBM_DB2=/path/to/DB2

The **configure** command defaults to `/opt/IBM/db2/V8.1`.

> **Note**: **Note for IIS users**  
>
> If you are using the ibm\_db2 driver with Microsoft Internet
> Information Server (IIS) you may have to do the following:
>
> -   Install DB2 with extended operating system security.
> -   Add the PHP binary path to the `PATH` system environment variable
>     (default C:\\php\\).
> -   Create another system environment variable equal to the path where
>     the PHP.INI file is located (eg: PHPRC = C:\\php\\).
> -   Add the IUSR\_COMPUTERNAME to the DB2USERS group.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                    | 默认 | 可修改范围       | Changelog                       |
|-------------------------------------------------------------------------|------|------------------|---------------------------------|
| <a href="/book/ibm-db2.html#" class="link">ibm_db2.binmode</a>          | "1"  | PHP\_INI\_ALL    |                                 |
| <a href="/book/ibm-db2.html#" class="link">ibm_db2.i5_all_pconnect</a>  | "0"  | PHP\_INI\_SYSTEM | Available since ibm\_db2 1.6.5. |
| <a href="/book/ibm-db2.html#" class="link">ibm_db2.i5_allow_commit</a>  | "0"  | PHP\_INI\_SYSTEM | Available since ibm\_db2 1.4.9. |
| <a href="/book/ibm-db2.html#" class="link">ibm_db2.i5_dbcs_alloc</a>    | "0"  | PHP\_INI\_SYSTEM | Available since ibm\_db2 1.5.0. |
| <a href="/book/ibm-db2.html#" class="link">ibm_db2.instance_name</a>    | NULL | PHP\_INI\_SYSTEM | Available since ibm\_db2 1.0.2. |
| <a href="/book/ibm-db2.html#" class="link">ibm_db2.i5_ignore_userid</a> | "0"  | PHP\_INI\_SYSTEM | Available since ibm\_db2 1.8.0. |

这是配置指令的简短说明。

`ibm_db2.binmode` <span class="type">int</span>  
This option controls the mode used for converting to and from binary
data in the PHP application.

-   1 (DB2\_BINARY)

-   2 (DB2\_CONVERT)

-   3 (DB2\_PASSTHRU)

`ibm_db2.i5_all_pconnect` <span class="type">int</span>  
This option overrides i5 <span class="function">db2\_connect</span> full
open and close in the PHP application. When `ibm_db2.i5_all_pconnect` =
1, all db2 connections become persistent (<span
class="function">db2\_pconnect</span>). On i5/OS, <span
class="function">db2\_pconnect</span> performs dramatically better with
lower machine stress over <span class="function">db2\_connect</span>.
This is a convenience override of <span
class="function">db2\_connect</span> to evoke <span
class="function">db2\_pconnect</span> without PHP source code changes.

-   0 <span class="function">db2\_connect</span> default full open and
    close

-   1 <span class="function">db2\_connect</span> override to <span
    class="function">db2\_pconnect</span> for persistent connection only

`ibm_db2.i5_allow_commit` <span class="type">int</span>  
This option controls the isolation mode used for i5 schema collections
in the PHP application (see `i5_commit` for override).

-   0 - commitment control is not used

-   1 - read uncommitted, dirty reads possible.

-   2 - read committed, dirty reads are not possible.

-   3 - repeatable read, dirty reads and non-repeatable reads are not
    possible

-   4 - serializeable, dirty reads, non-repeatable reads, and phantoms
    are not possible

`ibm_db2.i5_dbcs_alloc` <span class="type">int</span>  
This option controls the internal ibm\_db2 allocation scheme for large
DBCS column buffers.

-   0 no expanded allocations (see `i5_dbcs_alloc` for override)

-   1 use expanded allocations (see `i5_dbcs_alloc` for override)

`ibm_db2.instance_name` <span class="type">string</span>  
On Linux and UNIX operating systems, this option defines the name of the
instance to use for cataloged database connections. If this option is
set, its value overrides the DB2INSTANCE environment variable setting.

This option is ignored on Windows operating systems.

`ibm_db2.i5_ignore_userid` <span class="type">int</span>  
This option overrides i5 db2\_(p)connect userid and password in the PHP
application. When `ibm_db2.i5_ignore_userid` = 1, all db2 (p)connections
become null userid and null password. Therefore Apache jobs connect with
the current profile (NOBODY). Use of this override is only for simple
DB2 based websites that never require profile switching and therefore
can avoid all overhead of server mode additional QSQSRVR jobs. This is a
convenience override of db2\_(p)connect to set the userid and password
values to null without PHP source code changes. This override can be
used in combination with `ibm_db2.i5_all_pconnect` = 1.

-   0 db2\_(p)connect with specified userid and password

-   1 db2\_(p)connect override connect with null userid and null
    password

资源类型
--------

The ibm\_db2 extension returns connection resources, statement
resources, and result set resources.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`DB2_BINARY`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that binary data shall be returned as
is. This is the default mode. </span>

**`DB2_CONVERT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that binary data shall be converted to
a hexadecimal encoding and returned as an ASCII string. </span>

**`DB2_PASSTHRU`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that binary data shall be converted to
a **`NULL`** value. </span>

**`DB2_SCROLLABLE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies a scrollable cursor for a statement
resource. This mode enables random access to rows in a result set, but
currently is supported only by IBM DB2 Universal Database. </span>

**`DB2_FORWARD_ONLY`** (<span class="type">int</span>)  
<span class="simpara"> Specifies a forward-only cursor for a statement
resource. This is the default cursor type and is supported on all
database servers. </span>

**`DB2_PARAM_IN`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the PHP variable should be bound as an
IN parameter for a stored procedure. </span>

**`DB2_PARAM_OUT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the PHP variable should be bound as an
OUT parameter for a stored procedure. </span>

**`DB2_PARAM_INOUT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the PHP variable should be bound as an
INOUT parameter for a stored procedure. </span>

**`DB2_PARAM_FILE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that the column should be bound
directly to a file for input. </span>

**`DB2_AUTOCOMMIT_ON`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that autocommit should be turned on.
</span>

**`DB2_AUTOCOMMIT_OFF`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that autocommit should be turned off.
</span>

**`DB2_DOUBLE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that the variable should be bound as a
DOUBLE, FLOAT, or REAL data type. </span>

**`DB2_LONG`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that the variable should be bound as a
SMALLINT, INTEGER, or BIGINT data type. </span>

**`DB2_CHAR`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that the variable should be bound as a
CHAR or VARCHAR data type. </span>

**`DB2_CASE_NATURAL`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that column names will be returned in
their natural case. </span>

**`DB2_CASE_LOWER`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that column names will be returned in
lower case. </span>

**`DB2_CASE_UPPER`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that column names will be returned in
upper case. </span>

**`DB2_DEFERRED_PREPARE_ON`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that deferred prepare should be turned
on for the specified statement resource. </span>

**`DB2_DEFERRED_PREPARE_OFF`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that deferred prepare should be turned
off for the specified statement resource. </span>

db2\_autocommit
===============

Returns or sets the AUTOCOMMIT state for a database connection

### 说明

<span class="type">mixed</span> <span
class="methodname">db2\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$value`</span> \] )

Sets or gets the AUTOCOMMIT behavior of the specified connection
resource.

### 参数

`connection`  
A valid database connection resource variable as returned from <span
class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

`value`  
One of the following constants:

*DB2\_AUTOCOMMIT\_OFF*  
Turns AUTOCOMMIT off.

*DB2\_AUTOCOMMIT\_ON*  
Turns AUTOCOMMIT on.

### 返回值

When <span class="function">db2\_autocommit</span> receives only the
`connection` parameter, it returns the current state of AUTOCOMMIT for
the requested connection as an integer value. A value of
**`DB2_AUTOCOMMIT_OFF`** indicates that AUTOCOMMIT is off, while a value
of **`DB2_AUTOCOMMIT_ON`** indicates that AUTOCOMMIT is on.

When <span class="function">db2\_autocommit</span> receives both the
`connection` parameter and `autocommit` parameter, it attempts to set
the AUTOCOMMIT state of the requested connection to the corresponding
state. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Retrieving the AUTOCOMMIT value for a connection**

In the following example, a connection which has been created with
AUTOCOMMIT turned off is tested with the <span
class="function">db2\_autocommit</span> function.

``` php
<?php
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);
$conn = db2_connect($database, $user, $password, $options);
$ac = db2_autocommit($conn);
if ($ac == DB2_AUTOCOMMIT_OFF) {
    print "$ac -- AUTOCOMMIT is off.";
} else {
    print "$ac -- AUTOCOMMIT is on.";
}
?>
```

以上例程会输出：

    0 -- AUTOCOMMIT is off.

**示例 \#2 Setting the AUTOCOMMIT value for a connection**

In the following example, a connection which was initially created with
AUTOCOMMIT turned off has its behavior changed to turn AUTOCOMMIT on.

``` php
<?php
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);
$conn = db2_connect($database, $user, $password, $options);

// Turn AUTOCOMMIT on
$rc = db2_autocommit($conn, DB2_AUTOCOMMIT_ON);
if ($rc) {
    print "Turning AUTOCOMMIT on succeeded.\n";
}

// Check AUTOCOMMIT state
$ac = db2_autocommit($conn);
if ($ac == DB2_AUTOCOMMIT_OFF) {
    print "$ac -- AUTOCOMMIT is off.";
} else {
    print "$ac -- AUTOCOMMIT is on.";
}
?>
```

以上例程会输出：

    Turning AUTOCOMMIT on succeeded.
    1 -- AUTOCOMMIT is on.

### 参见

-   <span class="function">db2\_connect</span>
-   <span class="function">db2\_pconnect</span>

db2\_bind\_param
================

Binds a PHP variable to an SQL statement parameter

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_bind\_param</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">int</span>
`$parameter_number`</span> , <span class="methodparam"><span
class="type">string</span> `$variable_name`</span> \[, <span
class="methodparam"><span class="type">int</span>
`$parameter_type`</span> \[, <span class="methodparam"><span
class="type">int</span> `$data_type`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$precision`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$scale`<span class="initializer"> =
0</span></span> \]\]\]\] )

Binds a PHP variable to an SQL statement parameter in a statement
resource returned by <span class="function">db2\_prepare</span>. This
function gives you more control over the parameter type, data type,
precision, and scale for the parameter than simply passing the variable
as part of the optional input array to <span
class="function">db2\_execute</span>.

### 参数

`stmt`  
A prepared statement returned from <span
class="function">db2\_prepare</span>.

`parameter_number`  
Specifies the 1-indexed position of the parameter in the prepared
statement.

`variable_name`  
A string specifying the name of the PHP variable to bind to the
parameter specified by `parameter_number`.

`parameter_type`  
A constant specifying whether the PHP variable should be bound to the
SQL parameter as an input parameter (*DB2\_PARAM\_IN*), an output
parameter (*DB2\_PARAM\_OUT*), or as a parameter that accepts input and
returns output (*DB2\_PARAM\_INOUT*). To avoid memory overhead, you can
also specify *DB2\_PARAM\_FILE* to bind the PHP variable to the name of
a file that contains large object (BLOB, CLOB, or DBCLOB) data.

`data_type`  
A constant specifying the SQL data type that the PHP variable should be
bound as: one of *DB2\_BINARY*, *DB2\_CHAR*, *DB2\_DOUBLE*, or
*DB2\_LONG* .

`precision`  
Specifies the precision with which the variable should be bound to the
database. This parameter can also be used for retrieving XML output
values from stored procedures. A non-negative value specifies the
maximum size of the XML data that will be retrieved from the database.
If this parameter is not used, a default of 1MB will be assumed for
retrieving the XML output value from the stored procedure.

`scale`  
Specifies the scale with which the variable should be bound to the
database.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Binding PHP variables to a prepared statement**

The SQL statement in the following example uses two input parameters in
the WHERE clause. We call <span class="function">db2\_bind\_param</span>
to bind two PHP variables to the corresponding SQL parameters. Notice
that the PHP variables do not have to be declared or assigned before the
call to <span class="function">db2\_bind\_param</span>; in the example,
*$lower\_limit* is assigned a value before the call to <span
class="function">db2\_bind\_param</span>, but *$upper\_limit* is
assigned a value after the call to <span
class="function">db2\_bind\_param</span>. The variables must be bound
and, for parameters that accept input, must have any value assigned,
before calling <span class="function">db2\_execute</span>.

``` php
<?php

$sql = 'SELECT name, breed, weight FROM animals
    WHERE weight > ? AND weight < ?';
$conn = db2_connect($database, $user, $password);
$stmt = db2_prepare($conn, $sql);

// We can declare the variable before calling db2_bind_param()
$lower_limit = 1;

db2_bind_param($stmt, 1, "lower_limit", DB2_PARAM_IN);
db2_bind_param($stmt, 2, "upper_limit", DB2_PARAM_IN);

// We can also declare the variable after calling db2_bind_param()
$upper_limit = 15.0;

if (db2_execute($stmt)) {
    while ($row = db2_fetch_array($stmt)) {
        print "{$row[0]}, {$row[1]}, {$row[2]}\n";
    }
}
?>
```

以上例程会输出：

    Pook, cat, 3.2
    Rickety Ride, goat, 9.7
    Peaches, dog, 12.3

**示例 \#2 Calling stored procedures with IN and OUT parameters**

The stored procedure match\_animal in the following example accepts
three different parameters:

1.  an input (IN) parameter that accepts the name of the first animal as
    input

2.  an input-output (INOUT) parameter that accepts the name of the
    second animal as input and returns the string *TRUE* if an animal in
    the database matches that name

3.  an output (OUT) parameter that returns the sum of the weight of the
    two identified animals

In addition, the stored procedure returns a result set consisting of the
animals listed in alphabetic order starting at the animal corresponding
to the input value of the first parameter and ending at the animal
corresponding to the input value of the second parameter.

``` php
<?php

$sql = 'CALL match_animal(?, ?, ?)';
$conn = db2_connect($database, $user, $password);
$stmt = db2_prepare($conn, $sql);

$name = "Peaches";
$second_name = "Rickety Ride";
$weight = 0;

db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
db2_bind_param($stmt, 2, "second_name", DB2_PARAM_INOUT);
db2_bind_param($stmt, 3, "weight", DB2_PARAM_OUT);

print "Values of bound parameters _before_ CALL:\n";
print "  1: {$name} 2: {$second_name} 3: {$weight}\n\n";

if (db2_execute($stmt)) {
    print "Values of bound parameters _after_ CALL:\n";
    print "  1: {$name} 2: {$second_name} 3: {$weight}\n\n";

    print "Results:\n";
    while ($row = db2_fetch_array($stmt)) {
        print "  {$row[0]}, {$row[1]}, {$row[2]}\n";
    }
}
?>
```

以上例程会输出：

    Values of bound parameters _before_ CALL:
      1: Peaches 2: Rickety Ride 3: 0

    Values of bound parameters _after_ CALL:
      1: Peaches 2: TRUE 3: 22

    Results:
      Peaches, dog, 12.3
      Pook, cat, 3.2
      Rickety Ride, goat, 9.7

**示例 \#3 Inserting a binary large object (BLOB) directly from a file**

The data for large objects are typically stored in files, such as XML
documents or audio files. Rather than reading an entire file into a PHP
variable, and then binding that PHP variable into an SQL statement, you
can avoid some memory overhead by binding the file directly to the input
parameter of your SQL statement. The following example demonstrates how
to bind a file directly into a BLOB column.

``` php
<?php
$stmt = db2_prepare($conn, "INSERT INTO animal_pictures(picture) VALUES (?)");

$picture = "/opt/albums/spook/grooming.jpg";
$rc = db2_bind_param($stmt, 1, "picture", DB2_PARAM_FILE);
$rc = db2_execute($stmt);
?>
```

### 参见

-   <span class="function">db2\_execute</span>
-   <span class="function">db2\_prepare</span>

db2\_client\_info
=================

Returns an object with properties that describe the DB2 database client

### 说明

<span class="type"><span class="type">object</span><span
class="type">false</span></span> <span
class="methodname">db2\_client\_info</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

This function returns an object with read-only properties that return
information about the DB2 database client. The following table lists the
DB2 client properties:

<table>
<caption><strong>DB2 client properties</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Property name</th>
<th>Return type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>APPL_CODEPAGE</td>
<td>int</td>
<td>The application code page.</td>
</tr>
<tr class="even">
<td>CONN_CODEPAGE</td>
<td>int</td>
<td>The code page for the current connection.</td>
</tr>
<tr class="odd">
<td>DATA_SOURCE_NAME</td>
<td>string</td>
<td>The data source name (DSN) used to create the current connection to the database.</td>
</tr>
<tr class="even">
<td>DRIVER_NAME</td>
<td>string</td>
<td>The name of the library that implements the DB2 Call Level Interface (CLI) specification.</td>
</tr>
<tr class="odd">
<td>DRIVER_ODBC_VER</td>
<td>string</td>
<td>The version of ODBC that the DB2 client supports. This returns a string "MM.mm" where <var class="varname">MM</var> is the major version and <var class="varname">mm</var> is the minor version. The DB2 client always returns "03.51".</td>
</tr>
<tr class="even">
<td>DRIVER_VER</td>
<td>string</td>
<td>The version of the client, in the form of a string "MM.mm.uuuu" where <var class="varname">MM</var> is the major version, <var class="varname">mm</var> is the minor version, and <var class="varname">uuuu</var> is the update. For example, "08.02.0001" represents major version 8, minor version 2, update 1.</td>
</tr>
<tr class="odd">
<td>ODBC_SQL_CONFORMANCE</td>
<td>string</td>
<td><p>The level of ODBC SQL grammar supported by the client:</p>
<dl>
<dt>MINIMUM</dt>
<dd><p>Supports the minimum ODBC SQL grammar.</p>
</dd>
<dt>CORE</dt>
<dd><p>Supports the core ODBC SQL grammar.</p>
</dd>
<dt>EXTENDED</dt>
<dd><p>Supports extended ODBC SQL grammar.</p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td>ODBC_VER</td>
<td>string</td>
<td>The version of ODBC that the ODBC driver manager supports. This returns a string "MM.mm.rrrr" where <var class="varname">MM</var> is the major version, <var class="varname">mm</var> is the minor version, and <var class="varname">rrrr</var> is the release. The DB2 client always returns "03.01.0000".</td>
</tr>
</tbody>
</table>

### 参数

`connection`  
Specifies an active DB2 client connection.

### 返回值

Returns an object on a successful call. Returns **`FALSE`** on failure.

### 范例

**示例 \#1 A <span class="function">db2\_client\_info</span> example**

To retrieve information about the client, you must pass a valid database
connection resource to <span class="function">db2\_client\_info</span>.

``` php
<?php
$conn = db2_connect( 'SAMPLE', 'db2inst1', 'ibmdb2' );
$client = db2_client_info( $conn );

if ($client) {
    echo "DRIVER_NAME: ";           var_dump( $client->DRIVER_NAME );
    echo "DRIVER_VER: ";            var_dump( $client->DRIVER_VER );
    echo "DATA_SOURCE_NAME: ";      var_dump( $client->DATA_SOURCE_NAME );
    echo "DRIVER_ODBC_VER: ";       var_dump( $client->DRIVER_ODBC_VER );
    echo "ODBC_VER: ";              var_dump( $client->ODBC_VER );
    echo "ODBC_SQL_CONFORMANCE: ";  var_dump( $client->ODBC_SQL_CONFORMANCE );
    echo "APPL_CODEPAGE: ";         var_dump( $client->APPL_CODEPAGE );
    echo "CONN_CODEPAGE: ";         var_dump( $client->CONN_CODEPAGE );
}
else {
    echo "Error retrieving client information.
     Perhaps your database connection was invalid.";
}
db2_close($conn);

?>
```

以上例程会输出：

    DRIVER_NAME: string(8) "libdb2.a"
    DRIVER_VER: string(10) "08.02.0001"
    DATA_SOURCE_NAME: string(6) "SAMPLE"
    DRIVER_ODBC_VER: string(5) "03.51"
    ODBC_VER: string(10) "03.01.0000"
    ODBC_SQL_CONFORMANCE: string(8) "EXTENDED"
    APPL_CODEPAGE: int(819)
    CONN_CODEPAGE: int(819)

### 参见

-   <span class="function">db2\_server\_info</span>

db2\_close
==========

Closes a database connection

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

This function closes a DB2 client connection created with <span
class="function">db2\_connect</span> and returns the corresponding
resources to the database server.

If you attempt to close a persistent DB2 client connection created with
<span class="function">db2\_pconnect</span>, the close request is
ignored and the persistent DB2 client connection remains available for
the next caller.

### 参数

`connection`  
Specifies an active DB2 client connection.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Closing a connection**

The following example demonstrates a successful attempt to close a
connection to an IBM DB2, Cloudscape, or Apache Derby database.

``` php
<?php
$conn = db2_connect('SAMPLE', 'db2inst1', 'ibmdb2');
$rc = db2_close($conn);
if ($rc) {
    echo "Connection was successfully closed.";
}
?>
```

以上例程会输出：

    Connection was successfully closed.

### 参见

-   <span class="function">db2\_connect</span>
-   <span class="function">db2\_pclose</span>
-   <span class="function">db2\_pconnect</span>

db2\_column\_privileges
=======================

Returns a result set listing the columns and associated privileges for a
table

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_column\_privileges</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \[, <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> \[, <span
class="methodparam"><span class="type">string</span> `$schema`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$table-name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$column-name`</span> \]\]\]\] )

Returns a result set listing the columns and associated privileges for a
table.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables. To match all schemas, pass
**`NULL`** or an empty string.

`table-name`  
The name of the table or view. To match all tables in the database, pass
**`NULL`** or an empty string.

`column-name`  
The name of the column. To match all columns in the table, pass
**`NULL`** or an empty string.

### 返回值

Returns a statement resource with a result set containing rows
describing the column privileges for columns matching the specified
parameters. The rows are composed of the following columns:

| Column name   | Description                                                                  |
|---------------|------------------------------------------------------------------------------|
| TABLE\_CAT    | Name of the catalog. The value is NULL if this table does not have catalogs. |
| TABLE\_SCHEM  | Name of the schema.                                                          |
| TABLE\_NAME   | Name of the table or view.                                                   |
| COLUMN\_NAME  | Name of the column.                                                          |
| GRANTOR       | Authorization ID of the user who granted the privilege.                      |
| GRANTEE       | Authorization ID of the user to whom the privilege was granted.              |
| PRIVILEGE     | The privilege for the column.                                                |
| IS\_GRANTABLE | Whether the GRANTEE is permitted to grant this privilege to other users.     |

### 参见

-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_columns
============

Returns a result set listing the columns and associated metadata for a
table

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_columns</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> \[, <span
class="methodparam"><span class="type">string</span> `$qualifier`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$schema`</span> \[, <span class="methodparam"><span
class="type">string</span> `$table-name`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$column-name`</span> \]\]\]\] )

Returns a result set listing the columns and associated metadata for a
table.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables. To match all schemas, pass *'%'*.

`table-name`  
The name of the table or view. To match all tables in the database, pass
**`NULL`** or an empty string.

`column-name`  
The name of the column. To match all columns in the table, pass
**`NULL`** or an empty string.

### 返回值

Returns a statement resource with a result set containing rows
describing the columns matching the specified parameters. The rows are
composed of the following columns:

| Column name         | Description                                                                                                                                                                                                 |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TABLE\_CAT          | Name of the catalog. The value is NULL if this table does not have catalogs.                                                                                                                                |
| TABLE\_SCHEM        | Name of the schema.                                                                                                                                                                                         |
| TABLE\_NAME         | Name of the table or view.                                                                                                                                                                                  |
| COLUMN\_NAME        | Name of the column.                                                                                                                                                                                         |
| DATA\_TYPE          | The SQL data type for the column represented as an integer value.                                                                                                                                           |
| TYPE\_NAME          | A string representing the data type for the column.                                                                                                                                                         |
| COLUMN\_SIZE        | An integer value representing the size of the column.                                                                                                                                                       |
| BUFFER\_LENGTH      | Maximum number of bytes necessary to store data from this column.                                                                                                                                           |
| DECIMAL\_DIGITS     | The scale of the column, or **`NULL`** where scale is not applicable.                                                                                                                                       |
| NUM\_PREC\_RADIX    | An integer value of either *10* (representing an exact numeric data type), *2* (representing an approximate numeric data type), or **`NULL`** (representing a data type for which radix is not applicable). |
| NULLABLE            | An integer value representing whether the column is nullable or not.                                                                                                                                        |
| REMARKS             | Description of the column.                                                                                                                                                                                  |
| COLUMN\_DEF         | Default value for the column.                                                                                                                                                                               |
| SQL\_DATA\_TYPE     | An integer value representing the size of the column.                                                                                                                                                       |
| SQL\_DATETIME\_SUB  | Returns an integer value representing a datetime subtype code, or **`NULL`** for SQL data types to which this does not apply.                                                                               |
| CHAR\_OCTET\_LENGTH | Maximum length in octets for a character data type column, which matches COLUMN\_SIZE for single-byte character set data, or **`NULL`** for non-character data types.                                       |
| ORDINAL\_POSITION   | The 1-indexed position of the column in the table.                                                                                                                                                          |
| IS\_NULLABLE        | A string value where 'YES' means that the column is nullable and 'NO' means that the column is not nullable.                                                                                                |

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_commit
===========

Commits a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_commit</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

Commits an in-progress transaction on the specified connection resource
and begins a new transaction. PHP applications normally default to
AUTOCOMMIT mode, so <span class="function">db2\_commit</span> is not
necessary unless AUTOCOMMIT has been turned off for the connection
resource.

### 参数

`connection`  
A valid database connection resource variable as returned from <span
class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">db2\_autocommit</span>
-   <span class="function">db2\_rollback</span>

db2\_conn\_error
================

Returns a string containing the SQLSTATE returned by the last connection
attempt

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">db2\_conn\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">db2\_conn\_error</span> returns an SQLSTATE value
representing the reason the last attempt to connect to a database
failed. As <span class="function">db2\_connect</span> returns
**`FALSE`** in the event of a failed connection attempt, you do not pass
any parameters to <span class="function">db2\_conn\_error</span> to
retrieve the SQLSTATE value.

If, however, the connection was successful but becomes invalid over
time, you can pass the `connection` parameter to retrieve the SQLSTATE
value for a specific connection.

To learn what the SQLSTATE value means, you can issue the following
command at a DB2 Command Line Processor prompt:
**`db2 '? sqlstate-value`'**. You can also call <span
class="function">db2\_conn\_errormsg</span> to retrieve an explicit
error message and the associated SQLCODE value.

### 参数

`connection`  
A connection resource associated with a connection that initially
succeeded, but which over time became invalid.

### 返回值

Returns the SQLSTATE value resulting from a failed connection attempt.
Returns an empty string if there is no error associated with the last
connection attempt.

### 范例

**示例 \#1 Retrieving an SQLSTATE value for a failed connection
attempt**

The following example demonstrates how to return an SQLSTATE value after
deliberately passing invalid parameters to <span
class="function">db2\_connect</span>.

``` php
<?php
$conn = db2_connect('badname', 'baduser', 'badpassword');
if (!$conn) {
    print "SQLSTATE value: " . db2_conn_error();
}
?>
```

以上例程会输出：

    SQLSTATE value: 08001

### 参见

-   <span class="function">db2\_conn\_errormsg</span>
-   <span class="function">db2\_connect</span>
-   <span class="function">db2\_stmt\_error</span>
-   <span class="function">db2\_stmt\_errormsg</span>

db2\_conn\_errormsg
===================

Returns the last connection error message and SQLCODE value

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">db2\_conn\_errormsg</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">db2\_conn\_errormsg</span> returns an error
message and SQLCODE value representing the reason the last database
connection attempt failed. As <span class="function">db2\_connect</span>
returns **`FALSE`** in the event of a failed connection attempt, do not
pass any parameters to <span class="function">db2\_conn\_errormsg</span>
to retrieve the associated error message and SQLCODE value.

If, however, the connection was successful but becomes invalid over
time, you can pass the `connection` parameter to retrieve the associated
error message and SQLCODE value for a specific connection.

### 参数

`connection`  
A connection resource associated with a connection that initially
succeeded, but which over time became invalid.

### 返回值

Returns a string containing the error message and SQLCODE value
resulting from a failed connection attempt. If there is no error
associated with the last connection attempt, <span
class="function">db2\_conn\_errormsg</span> returns an empty string.

### 范例

**示例 \#1 Retrieving the error message returned by a failed connection
attempt**

The following example demonstrates how to return an error message and
SQLCODE value after deliberately passing invalid parameters to <span
class="function">db2\_connect</span>.

``` php
<?php
$conn = db2_connect('badname', 'baduser', 'badpassword');
if (!$conn) {
    print db2_conn_errormsg();
}
?>
```

以上例程会输出：

    [IBM][CLI Driver] SQL1013N  The database alias name
    or database name "BADNAME" could not be found.  SQLSTATE=42705
     SQLCODE=-1013

### 参见

-   <span class="function">db2\_conn\_error</span>
-   <span class="function">db2\_connect</span>
-   <span class="function">db2\_stmt\_error</span>
-   <span class="function">db2\_stmt\_errormsg</span>

db2\_connect
============

Returns a connection to a database

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">db2\_connect</span> ( <span class="methodparam"><span
class="type">string</span> `$database`</span> , <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \] )

Creates a new connection to an IBM DB2 Universal Database, IBM
Cloudscape, or Apache Derby database.

### 参数

`database`  
For a cataloged connection to a database, `database` represents the
database alias in the DB2 client catalog.

For an uncataloged connection to a database, `database` represents a
complete connection string in the following format:

``` literallayout
DATABASE=database;HOSTNAME=hostname;PORT=port;PROTOCOL=TCPIP;UID=username;PWD=password;
```

where the parameters represent the following values:

`database`  
The name of the database.

`hostname`  
The hostname or IP address of the database server.

`port`  
The TCP/IP port on which the database is listening for requests.

`username`  
The username with which you are connecting to the database.

`password`  
The password with which you are connecting to the database.

`username`  
The username with which you are connecting to the database.

For uncataloged connections, you must pass a **`NULL`** value or empty
string.

`password`  
The password with which you are connecting to the database.

For uncataloged connections, you must pass a **`NULL`** value or empty
string.

`options`  
An associative array of connection options that affect the behavior of
the connection, where valid array keys include:

`autocommit`  
Passing the *DB2\_AUTOCOMMIT\_ON* value turns autocommit on for this
connection handle.

Passing the *DB2\_AUTOCOMMIT\_OFF* value turns autocommit off for this
connection handle.

`DB2_ATTR_CASE`  
Passing the *DB2\_CASE\_NATURAL* value specifies that column names are
returned in natural case.

Passing the *DB2\_CASE\_LOWER* value specifies that column names are
returned in lower case.

Passing the *DB2\_CASE\_UPPER* value specifies that column names are
returned in upper case.

`CURSOR`  
Passing the *DB2\_FORWARD\_ONLY* value specifies a forward-only cursor
for a statement resource. This is the default cursor type and is
supported on all database servers.

Passing the *DB2\_SCROLLABLE* value specifies a scrollable cursor for a
statement resource. This mode enables random access to rows in a result
set, but currently is supported only by IBM DB2 Universal Database.

The following new option is available in ibm\_db2 version 1.7.0 and
later.

`trustedcontext`  
Passing the DB2\_TRUSTED\_CONTEXT\_ENABLE value turns trusted context on
for this connection handle. This parameter cannot be set using <span
class="function">db2\_set\_option</span>.

This key works only if the database is cataloged (even if the database
is local), or if you specify the full DSN when you create the
connection.

To catalog the database, use following commands:

``` literallayout
db2 catalog tcpip node loopback remote <SERVERNAME> server <SERVICENAME>
db2 catalog database <LOCALDBNAME> as <REMOTEDBNAME> at node loopback
db2 "update dbm cfg using svcename <SERVICENAME>"
db2set DB2COMM=TCPIP
```

The following new i5/OS options are available in ibm\_db2 version 1.5.1
and later.

`i5_lib`  
A character value that indicates the default library that will be used
for resolving unqualified file references. This is not valid if the
connection is using system naming mode.

`i5_naming`  
*DB2\_I5\_NAMING\_ON* value turns on DB2 UDB CLI iSeries system naming
mode. Files are qualified using the slash (/) delimiter. Unqualified
files are resolved using the library list for the job.

*DB2\_I5\_NAMING\_OFF* value turns off DB2 UDB CLI default naming mode,
which is SQL naming. Files are qualified using the period (.) delimiter.
Unqualified files are resolved using either the default library or the
current user ID.

`i5_commit`  
The `i5_commit` attribute should be set before the <span
class="function">db2\_connect</span>. If the value is changed after the
connection has been established, and the connection is to a remote data
source, the change does not take effect until the next successful <span
class="function">db2\_connect</span> for the connection handle.

> **Note**:
>
> The php.ini setting `ibm_db2.i5_allow_commit`==0 or
> *DB2\_I5\_TXN\_NO\_COMMIT* is the default, but may be overridden with
> the `i5_commit` option.

*DB2\_I5\_TXN\_NO\_COMMIT* - Commitment control is not used.

*DB2\_I5\_TXN\_READ\_UNCOMMITTED* - Dirty reads, nonrepeatable reads,
and phantoms are possible.

*DB2\_I5\_TXN\_READ\_COMMITTED* - Dirty reads are not possible.
Nonrepeatable reads, and phantoms are possible.

*DB2\_I5\_TXN\_REPEATABLE\_READ* - Dirty reads and nonrepeatable reads
are not possible. Phantoms are possible.

*DB2\_I5\_TXN\_SERIALIZABLE* - Transactions are serializable. Dirty
reads, non-repeatable reads, and phantoms are not possible

`i5_query_optimize`  
*DB2\_FIRST\_IO* All queries are optimized with the goal of returning
the first page of output as fast as possible. This goal works well when
the output is controlled by a user who is most likely to cancel the
query after viewing the first page of output data. Queries coded with an
OPTIMIZE FOR nnn ROWS clause honor the goal specified by the clause.

*DB2\_ALL\_IO* All queries are optimized with the goal of running the
entire query to completion in the shortest amount of elapsed time. This
is a good option when the output of a query is being written to a file
or report, or the interface is queuing the output data. Queries coded
with an OPTIMIZE FOR nnn ROWS clause honor the goal specified by the
clause. This is the default.

`i5_dbcs_alloc`  
*DB2\_I5\_DBCS\_ALLOC\_ON* value turns on DB2 6X allocation scheme for
DBCS translation column size growth.

*DB2\_I5\_DBCS\_ALLOC\_OFF* value turns off DB2 6X allocation scheme for
DBCS translation column size growth.

Note: php.ini setting `ibm_db2.i5_dbcs_alloc`==0 or
*DB2\_I5\_DBCS\_ALLOC\_OFF* is the default, but may be overridden with
the `i5_dbcs_alloc` option.

`i5_date_fmt`  
*DB2\_I5\_FMT\_ISO* - The International Organization for Standardization
(ISO) date format yyyy-mm-dd is used. This is the default.

*DB2\_I5\_FMT\_USA* - The United States date format mm/dd/yyyy is used.

*DB2\_I5\_FMT\_EUR* - The European date format dd.mm.yyyy is used.

*DB2\_I5\_FMT\_JIS* - The Japanese Industrial Standard date format
yyyy-mm-dd is used.

*DB2\_I5\_FMT\_MDY* - The date format mm/dd/yyyy is used.

*DB2\_I5\_FMT\_DMY* - The date format dd/mm/yyyy is used.

*DB2\_I5\_FMT\_YMD* - The date format yy/mm/dd is used.

*DB2\_I5\_FMT\_JUL* - The Julian date format yy/ddd is used.

*DB2\_I5\_FMT\_JOB* - The job default is used.

`i5_date_sep`  
*DB2\_I5\_SEP\_SLASH* - A slash ( / ) is used as the date separator.
This is the default.

*DB2\_I5\_SEP\_DASH* - A dash ( - ) is used as the date separator.

*DB2\_I5\_SEP\_PERIOD* - A period ( . ) is used as the date separator.

*DB2\_I5\_SEP\_COMMA* - A comma ( , ) is used as the date separator.

*DB2\_I5\_SEP\_BLANK* - A blank is used as the date separator.

*DB2\_I5\_SEP\_JOB* - The job default is used

`i5_time_fmt`  
*DB2\_I5\_FMT\_ISO* - The International Organization for Standardization
(ISO) time format hh.mm.ss is used. This is the default.

*DB2\_I5\_FMT\_USA* - The United States time format hh:mmxx is used,
where xx is AM or PM.

*DB2\_I5\_FMT\_EUR* - The European time format hh.mm.ss is used.

*DB2\_I5\_FMT\_JIS* - The Japanese Industrial Standard time format
hh:mm:ss is used.

*DB2\_I5\_FMT\_HMS* - The hh:mm:ss format is used.

`i5_time_sep`  
*DB2\_I5\_SEP\_COLON* - A colon ( : ) is used as the time separator.
This is the default.

*DB2\_I5\_SEP\_PERIOD* - A period ( . ) is used as the time separator.

*DB2\_I5\_SEP\_COMMA* - A comma ( , ) is used as the time separator.

*DB2\_I5\_SEP\_BLANK* - A blank is used as the time separator.

*DB2\_I5\_SEP\_JOB* - The job default is used.

`i5_decimal_sep`  
*DB2\_I5\_SEP\_PERIOD* - A period ( . ) is used as the decimal
separator. This is the default.

*DB2\_I5\_SEP\_COMMA* - A comma ( , ) is used as the decimal separator.

*DB2\_I5\_SEP\_JOB* - The job default is used.

The following new i5/OS option is available in ibm\_db2 version 1.8.0
and later.

`i5_libl`  
A character value that indicates the library list that will be used for
resolving unqualified file references. Specify the library list elements
separated by blanks 'i5\_libl'=\>"MYLIB YOURLIB ANYLIB".

> **Note**:
>
> `i5_libl` calls qsys2/qcmdexc('cmd',cmdlen), which is only available
> in i5/OS V5R4 and later.

### 返回值

Returns a connection handle resource if the connection attempt is
successful. If the connection attempt fails, <span
class="function">db2\_connect</span> returns **`FALSE`**.

### 范例

**示例 \#1 Creating a cataloged connection**

Cataloged connections require you to have previously cataloged the
target database through the DB2 Command Line Processor (CLP) or DB2
Configuration Assistant.

``` php
<?php
$database = 'SAMPLE';
$user = 'db2inst1';
$password = 'ibmdb2';

$conn = db2_connect($database, $user, $password);

if ($conn) {
    echo "Connection succeeded.";
    db2_close($conn);
}
else {
    echo "Connection failed.";
}
?>
```

以上例程会输出：

    Connection succeeded.

**示例 \#2 Creating an uncataloged connection**

An uncataloged connection enables you to dynamically connect to a
database.

``` php
<?php
$database = 'SAMPLE';
$user = 'db2inst1';
$password = 'ibmdb2';
$hostname = 'localhost';
$port = 50000;

$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;" .
  "HOSTNAME=$hostname;PORT=$port;PROTOCOL=TCPIP;UID=$user;PWD=$password;";
$conn = db2_connect($conn_string, '', '');

if ($conn) {
    echo "Connection succeeded.";
    db2_close($conn);
}
else {
    echo "Connection failed.";
}
?>
```

以上例程会输出：

    Connection succeeded.

**示例 \#3 Creating a connection with autocommit off by default**

Passing an array of options to <span
class="function">db2\_connect</span> enables you to modify the default
behavior of the connection handle.

``` php
<?php
$database = 'SAMPLE';
$user = 'db2inst1';
$password = 'ibmdb2';
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF);

$conn = db2_connect($database, $user, $password, $options);

if ($conn) {
    echo "Connection succeeded.\n";
    if (db2_autocommit($conn)) {
         echo "Autocommit is on.\n";
    }
    else {
         echo "Autocommit is off.\n";
    }
    db2_close($conn);
}
else {
    echo "Connection failed.";
}
?>
```

以上例程会输出：

    Connection succeeded.
    Autocommit is off.

**示例 \#4 i5/OS best performance**

To achieve best performance for your i5/OS ibm\_db2 1.5.1 PHP
application use the default host, userid, and password for your <span
class="function">db2\_connect</span>.

``` php
<?php
  $library = "ADC";
  $i5 = db2_connect("", "", "", array("i5_lib"=>"qsys2"));
  $result = db2_exec($i5, 
       "select * from systables where table_schema = '$library'");
  while ($row = db2_fetch_both($result)) {               
     echo $row['TABLE_NAME']."</br>";                     
  }                                                      
  db2_close($i5);
?>
```

以上例程会输出：

    ANIMALS
    NAMES
    PICTURES

**示例 \#5 Using trusted context**

The following example shows how to enable trusted context, switch users,
and get the current user ID.

``` php
<?php

$database = "SAMPLE";
$hostname = "localhost";
$port = 50000;
$authID = "db2inst1";
$auth_pass = "ibmdb2";

$tc_user = "tcuser";
$tc_pass = "tcpassword";

$dsn = "DATABASE=$database;HOSTNAME=$hostname;PORT=$port;
  PROTOCOL=TCPIP;UID=$authID;PWD=$auth_pass;";
$options = array ("trustedcontext" => DB2_TRUSTED_CONTEXT_ENABLE);

$tc_conn = db2_connect($dsn, "", "", $options);
if($tc_conn) {
    echo "Explicit trusted connection succeeded.\n";

    if(db2_get_option($tc_conn, "trustedcontext")) {
        $userBefore = db2_get_option($tc_conn, "trusted_user");
        
        //Do some work as user 1.

        //Switching to trusted user.
        $parameters = array("trusted_user" => $tc_user, 
          "trusted_password" => $tcuser_pass);
        $res = db2_set_option ($tc_conn, $parameters, 1);

        $userAfter = db2_get_option($tc_conn, "trusted_user");
        //Do more work as trusted user.

        if($userBefore != $userAfter) {
            echo "User has been switched." . "\n";    
        }
    }

    db2_close($tc_conn);
}
else {
    echo "Explicit trusted connection failed.\n";
}
?>
```

以上例程会输出：

    Explicit trusted connection succeeded.
    User has been switched.

### 参见

-   <span class="function">db2\_close</span>
-   <span class="function">db2\_pconnect</span>

db2\_cursor\_type
=================

Returns the cursor type used by a statement resource

### 说明

<span class="type">int</span> <span
class="methodname">db2\_cursor\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Returns the cursor type used by a statement resource. Use this to
determine if you are working with a forward-only cursor or scrollable
cursor.

### 参数

`stmt`  
A valid statement resource.

### 返回值

Returns either *DB2\_FORWARD\_ONLY* if the statement resource uses a
forward-only cursor or *DB2\_SCROLLABLE* if the statement resource uses
a scrollable cursor.

### 参见

-   <span class="function">db2\_prepare</span>

db2\_escape\_string
===================

Used to escape certain characters

### 说明

<span class="type">string</span> <span
class="methodname">db2\_escape\_string</span> ( <span
class="methodparam"><span class="type">string</span>
`$string_literal`</span> )

Prepends backslashes to special characters in the string argument.

### 参数

`string_literal`  
The string that contains special characters that need to be modified.
Characters that are prepended with a backslash are *\\x00*, *\\n*,
*\\r*, *\\*, *'*, *"* and *\\x1a*.

### 返回值

Returns `string_literal` with the special characters noted above
prepended with backslashes.

### 范例

**示例 \#1 A <span class="function">db2\_escape\_string</span> example**

Result of using the <span class="function">db2\_escape\_string</span>
function

``` php
<?php

$conn = db2_connect($database, $user, $password);

if ($conn) {
    $str[0] = "All characters: \x00 , \n , \r , \ , ' , \" , \x1a .";
    $str[1] = "Backslash (\). Single quote ('). Double quote (\")";
    $str[2] = "The NULL character \0 must be quoted as well";
    $str[3] = "Intersting characters: \x1a , \x00 .";
    $str[4] = "Nothing to quote";
    $str[5] = 200676;
    $str[6] = "";

    foreach( $str as $string ) {
        echo "db2_escape_string: " . db2_escape_string($string). "\n";
    }
}
?>
```

以上例程会输出：

    db2_escape_string: All characters: \0 , \n , \r , \\ , \' , \" , \Z .
    db2_escape_string: Backslash (\\). Single quote (\'). Double quote (\")
    db2_escape_string: The NULL character \0 must be quoted as well
    db2_escape_string: Intersting characters: \Z , \0 .
    db2_escape_string: Nothing to quote
    db2_escape_string: 200676
    db2_escape_string:

### 参见

-   <span class="function">db2\_prepare</span>

db2\_exec
=========

Executes an SQL statement directly

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">db2\_exec</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span> `$statement`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

Executes an SQL statement directly.

If you plan to interpolate PHP variables into the SQL statement,
understand that this is one of the more common security exposures.
Consider calling <span class="function">db2\_prepare</span> to prepare
an SQL statement with parameter markers for input values. Then you can
call <span class="function">db2\_execute</span> to pass in the input
values and avoid SQL injection attacks.

If you plan to repeatedly issue the same SQL statement with different
parameters, consider calling <span class="function">db2\_prepare</span>
and <span class="function">db2\_execute</span> to enable the database
server to reuse its access plan and increase the efficiency of your
database access.

### 参数

`connection`  
A valid database connection resource variable as returned from <span
class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

`statement`  
An SQL statement. The statement cannot contain any parameter markers.

`options`  
An associative array containing statement options. You can use this
parameter to request a scrollable cursor on database servers that
support this functionality.

For a description of valid statement options, see <span
class="function">db2\_set\_option</span>.

### 返回值

Returns a statement resource if the SQL statement was issued
successfully, or **`FALSE`** if the database failed to execute the SQL
statement.

### 范例

**示例 \#1 Creating a table with <span
class="function">db2\_exec</span>**

The following example uses <span class="function">db2\_exec</span> to
issue a set of DDL statements in the process of creating a table.

``` php
<?php
$conn = db2_connect($database, $user, $password);

// Create the test table
$create = 'CREATE TABLE animals (id INTEGER, breed VARCHAR(32),
    name CHAR(16), weight DECIMAL(7,2))';
$result = db2_exec($conn, $create);
if ($result) {
    print "Successfully created the table.\n";
}

// Populate the test table
$animals = array(
    array(0, 'cat', 'Pook', 3.2),
    array(1, 'dog', 'Peaches', 12.3),
    array(2, 'horse', 'Smarty', 350.0),
    array(3, 'gold fish', 'Bubbles', 0.1),
    array(4, 'budgerigar', 'Gizmo', 0.2),
    array(5, 'goat', 'Rickety Ride', 9.7),
    array(6, 'llama', 'Sweater', 150)
);

foreach ($animals as $animal) {
    $rc = db2_exec($conn, "INSERT INTO animals (id, breed, name, weight)
      VALUES ({$animal[0]}, '{$animal[1]}', '{$animal[2]}', {$animal[3]})");
    if ($rc) {
        print "Insert... ";
    }
}
?>
```

以上例程会输出：

    Successfully created the table.
    Insert... Insert... Insert... Insert... Insert... Insert... Insert... 

**示例 \#2 Executing a SELECT statement with a scrollable cursor**

The following example demonstrates how to request a scrollable cursor
for an SQL statement issued by <span class="function">db2\_exec</span>.

``` php
<?php
$conn = db2_connect($database, $user, $password);
$sql = "SELECT name FROM animals
    WHERE weight < 10.0
    ORDER BY name";
if ($conn) {
    require_once('prepare.inc');
    $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
    while ($row = db2_fetch_array($stmt)) {
        print "$row[0]\n";
    }
} 
?>
```

以上例程会输出：

    Bubbles
    Gizmo
    Pook
    Rickety Ride

**示例 \#3 Returning XML data as an SQL ResultSet**

The following example demonstrates how to work with documents stored in
a XML column using the SAMPLE database. Using some pretty simple
SQL/XML, this example returns some of the nodes in a XML document in an
SQL ResultSet format that most users are familiar with.

``` php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = 'SELECT * FROM XMLTABLE(
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("CUSTOMER.INFO")/customerinfo\'
    COLUMNS
    "CID" VARCHAR (50) PATH \'@Cid\',
    "NAME" VARCHAR (50) PATH \'name\',
    "PHONE" VARCHAR (50) PATH \'phone [ @type = "work"]\'
    ) AS T
    WHERE NAME = \'Kathy Smith\'
    ';
$stmt = db2_exec($conn, $query);

while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE\n");
}
db2_close($conn);

?>
```

以上例程会输出：

    1000     Kathy Smith     416-555-1358
    1001     Kathy Smith     905-555-7258

**示例 \#4 Performing a "JOIN" with XML data**

The following example works with documents stored in 2 different XML
columns in the SAMPLE database. It creates 2 temporary tables from the
XML documents from 2 different columns and returns an SQL ResultSet with
information regarding shipping status for the customer.

``` php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = '
    SELECT A.CID, A.NAME, A.PHONE, C.PONUM, C.STATUS
    FROM
    XMLTABLE(
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("CUSTOMER.INFO")/customerinfo\'
    COLUMNS
    "CID" BIGINT PATH \'@Cid\',
    "NAME" VARCHAR (50) PATH \'name\',
    "PHONE" VARCHAR (50) PATH \'phone [ @type = "work"]\'
    ) as A,
    PURCHASEORDER AS B,
    XMLTABLE (
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("PURCHASEORDER.PORDER")/PurchaseOrder\'
    COLUMNS
    "PONUM"  BIGINT PATH \'@PoNum\',
    "STATUS" VARCHAR (50) PATH \'@Status\'
    ) as C
    WHERE A.CID = B.CUSTID AND
    B.POID = C.PONUM AND
    A.NAME = \'Kathy Smith\'
';

$stmt = db2_exec($conn, $query);

while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE     $row->PONUM     $row->STATUS\n");
}

db2_close($conn);

?>
```

以上例程会输出：

    1001     Kathy Smith     905-555-7258     5002     Shipped

**示例 \#5 Returning SQL data as part of a larger XML document**

The following example works with a portion of the PRODUCT.DESCRIPTION
documents in the SAMPLE database. It creates a XML document containing
product description (XML data) and pricing info (SQL data).

``` php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = '
SELECT
XMLSERIALIZE(
XMLQUERY(\'
    declare boundary-space strip;
    declare default element namespace "http://posample.org";
    <promoList> {
    for $prod in $doc/product
    where $prod/description/price < 10.00
    order by $prod/description/price ascending
    return(
        <promoitem> {
        $prod,
        <startdate> {$start} </startdate>,
        <enddate> {$end} </enddate>,
        <promoprice> {$promo} </promoprice>
        } </promoitem>
    )
    } </promoList>
\' passing by ref DESCRIPTION AS "doc",
PROMOSTART as "start",
PROMOEND as "end",
PROMOPRICE as "promo"
RETURNING SEQUENCE)
AS CLOB (32000))
AS NEW_PRODUCT_INFO
FROM PRODUCT
WHERE PID = \'100-100-01\'
';

$stmt = db2_exec($conn, $query);

while($row = db2_fetch_array($stmt)){
    printf("$row[0]\n");
}
db2_close($conn);

?>
```

以上例程会输出：

    <promoList xmlns="http://posample.org">
        <promoitem>
        <product pid="100-100-01">
            <description>
                <name>Snow Shovel, Basic 22 inch</name>
                <details>Basic Snow Shovel, 22 inches wide, straight handle with D-Grip</details>
                <price>9.99</price>
                <weight>1 kg</weight>
            </description>
        </product>
        <startdate>2004-11-19</startdate>
        <enddate>2004-12-19</enddate>
        <promoprice>7.25</promoprice>
        </promoitem>
    </promoList>

### 参见

-   <span class="function">db2\_execute</span>
-   <span class="function">db2\_prepare</span>

db2\_execute
============

Executes a prepared SQL statement

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_execute</span> ( <span class="methodparam"><span
class="type">resource</span> `$stmt`</span> \[, <span
class="methodparam"><span class="type">array</span> `$parameters`</span>
\] )

<span class="function">db2\_execute</span> executes an SQL statement
that was prepared by <span class="function">db2\_prepare</span>.

If the SQL statement returns a result set, for example, a SELECT
statement or a CALL to a stored procedure that returns one or more
result sets, you can retrieve a row as an array from the *stmt* resource
using <span class="function">db2\_fetch\_assoc</span>, <span
class="function">db2\_fetch\_both</span>, or <span
class="function">db2\_fetch\_array</span>. Alternatively, you can use
<span class="function">db2\_fetch\_row</span> to move the result set
pointer to the next row and fetch a column at a time from that row with
<span class="function">db2\_result</span>.

Refer to <span class="function">db2\_prepare</span> for a brief
discussion of the advantages of using <span
class="function">db2\_prepare</span> and <span
class="function">db2\_execute</span> rather than <span
class="function">db2\_exec</span>.

### 参数

`stmt`  
A prepared statement returned from <span
class="function">db2\_prepare</span>.

`parameters`  
An array of input parameters matching any parameter markers contained in
the prepared statement.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Preparing and executing an SQL statement with parameter
markers**

The following example prepares an INSERT statement that accepts four
parameter markers, then iterates over an array of arrays containing the
input values to be passed to <span class="function">db2\_execute</span>.

``` php
<?php
$pet = array(0, 'cat', 'Pook', 3.2);

$insert = 'INSERT INTO animals (id, breed, name, weight)
    VALUES (?, ?, ?, ?)';

$stmt = db2_prepare($conn, $insert);
if ($stmt) {
    $result = db2_execute($stmt, $pet);
    if ($result) {
        print "Successfully added new pet.";
    }
}
?>
```

以上例程会输出：

    Successfully added new pet.

**示例 \#2 Calling a stored procedure with an OUT parameter**

The following example prepares a CALL statement that accepts one
parameter marker representing an OUT parameter, binds the PHP variable
*$my\_pets* to the parameter using <span
class="function">db2\_bind\_param</span>, then issues <span
class="function">db2\_execute</span> to execute the CALL statement.
After the CALL to the stored procedure has been made, the value of
*$num\_pets* changes to reflect the value returned by the stored
procedure for that OUT parameter.

``` php
<?php
$num_pets = 0;
$res = db2_prepare($conn, "CALL count_my_pets(?)");
$rc = db2_bind_param($res, 1, "num_pets", DB2_PARAM_OUT);
$rc = db2_execute($res);
print "I have $num_pets pets!";
?>
```

以上例程会输出：

    I have 7 pets!

**示例 \#3 Returning XML data as an SQL ResultSet**

The following example demonstrates how to work with documents stored in
a XML column using the SAMPLE database. Using some pretty simple
SQL/XML, this example returns some of the nodes in a XML document in an
SQL ResultSet format that most users are familiar with.

``` php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = 'SELECT * FROM XMLTABLE(
    XMLNAMESPACES (DEFAULT \'http://posample.org\'),
    \'db2-fn:xmlcolumn("CUSTOMER.INFO")/customerinfo\'
    COLUMNS
    "CID" VARCHAR (50) PATH \'@Cid\',
    "NAME" VARCHAR (50) PATH \'name\',
    "PHONE" VARCHAR (50) PATH \'phone [ @type = "work"]\'
    ) AS T
    WHERE NAME = ?
    ';

$stmt = db2_prepare($conn, $query);

$name = 'Kathy Smith';

if ($stmt) {
    db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
    db2_execute($stmt);

    while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE\n");
    }
}
db2_close($conn);

?>
```

以上例程会输出：

    1000     Kathy Smith     416-555-1358
    1001     Kathy Smith     905-555-7258

**示例 \#4 Performing a "JOIN" with XML data**

The following example works with documents stored in 2 different XML
columns in the SAMPLE database. It creates 2 temporary tables from the
XML documents from 2 different columns and returns an SQL ResultSet with
information regarding shipping status for the customer.

``` php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = '
SELECT A.CID, A.NAME, A.PHONE, C.PONUM, C.STATUS
FROM
XMLTABLE(
XMLNAMESPACES (DEFAULT \'http://posample.org\'),
\'db2-fn:xmlcolumn("CUSTOMER.INFO")/customerinfo\'
COLUMNS
"CID" BIGINT PATH \'@Cid\',
"NAME" VARCHAR (50) PATH \'name\',
"PHONE" VARCHAR (50) PATH \'phone [ @type = "work"]\'
) as A,
PURCHASEORDER AS B,
XMLTABLE (
XMLNAMESPACES (DEFAULT \'http://posample.org\'),
\'db2-fn:xmlcolumn("PURCHASEORDER.PORDER")/PurchaseOrder\'
COLUMNS
"PONUM"  BIGINT PATH \'@PoNum\',
"STATUS" VARCHAR (50) PATH \'@Status\'
) as C
WHERE A.CID = B.CUSTID AND
    B.POID = C.PONUM AND
    A.NAME = ?
';

$stmt = db2_prepare($conn, $query);

$name = 'Kathy Smith';

if ($stmt) {
    db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
    db2_execute($stmt);

    while($row = db2_fetch_object($stmt)){
    printf("$row->CID     $row->NAME     $row->PHONE     $row->PONUM     $row->STATUS\n");
    }
}

db2_close($conn);

?>
```

以上例程会输出：

    1001     Kathy Smith     905-555-7258     5002     Shipped

**示例 \#5 Returning SQL data as part of a larger XML document**

The following example works with a portion of the PRODUCT.DESCRIPTION
documents in the SAMPLE database. It creates a XML document containing
product description (XML data) and pricing info (SQL data).

``` php
<?php

$conn = db2_connect("SAMPLE", "db2inst1", "ibmdb2");

$query = '
SELECT
XMLSERIALIZE(
XMLQUERY(\'
    declare boundary-space strip;
    declare default element namespace "http://posample.org";
    <promoList> {
    for $prod in $doc/product
    where $prod/description/price < 10.00
    order by $prod/description/price ascending
    return(
        <promoitem> {
        $prod,
        <startdate> {$start} </startdate>,
        <enddate> {$end} </enddate>,
        <promoprice> {$promo} </promoprice>
            } </promoitem>
    )
    } </promoList>
\' passing by ref DESCRIPTION AS "doc",
PROMOSTART as "start",
PROMOEND as "end",
PROMOPRICE as "promo"
RETURNING SEQUENCE)
AS CLOB (32000))
AS NEW_PRODUCT_INFO
FROM PRODUCT
WHERE PID = ?
';

$stmt = db2_prepare($conn, $query);

$pid = "100-100-01";

if ($stmt) {
    db2_bind_param($stmt, 1, "pid", DB2_PARAM_IN);
    db2_execute($stmt);

    while($row = db2_fetch_array($stmt)){
    printf("$row[0]\n");
    }
}

db2_close($conn);

?>
```

以上例程会输出：

    <promoList xmlns="http://posample.org">
        <promoitem>
        <product pid="100-100-01">
            <description>
                <name>Snow Shovel, Basic 22 inch</name>
                <details>Basic Snow Shovel, 22 inches wide, straight handle with D-Grip</details>
                <price>9.99</price>
                <weight>1 kg</weight>
            </description>
        </product>
        <startdate>2004-11-19</startdate>
        <enddate>2004-12-19</enddate>
        <promoprice>7.25</promoprice>
        </promoitem>
    </promoList>

### 参见

-   <span class="function">db2\_exec</span>
-   <span class="function">db2\_fetch\_array</span>
-   <span class="function">db2\_fetch\_assoc</span>
-   <span class="function">db2\_fetch\_both</span>
-   <span class="function">db2\_fetch\_row</span>
-   <span class="function">db2\_prepare</span>
-   <span class="function">db2\_result</span>

db2\_fetch\_array
=================

Returns an array, indexed by column position, representing a row in a
result set

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">db2\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row_number`<span class="initializer"> = -1</span></span> \] )

Returns an array, indexed by column position, representing a row in a
result set. The columns are 0-indexed.

### 参数

`stmt`  
A valid *stmt* resource containing a result set.

`row_number`  
Requests a specific 1-indexed row from the result set. Passing this
parameter results in a PHP warning if the result set uses a forward-only
cursor.

### 返回值

Returns a 0-indexed array with column values indexed by the column
position representing the next or requested row in the result set.
Returns **`FALSE`** if there are no rows left in the result set, or if
the row requested by `row_number` does not exist in the result set.

### 范例

**示例 \#1 Iterating through a forward-only cursor**

If you call <span class="function">db2\_fetch\_array</span> without a
specific row number, it automatically retrieves the next row in the
result set.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$stmt = db2_prepare($conn, $sql);
$result = db2_execute($stmt);

while ($row = db2_fetch_array($stmt)) {
    printf ("%-5d %-16s %-32s %10s\n", 
        $row[0], $row[1], $row[2], $row[3]);
}
?>
```

以上例程会输出：

    0     Pook             cat                                    3.20
    5     Rickety Ride     goat                                   9.70
    2     Smarty           horse                                350.00

**示例 \#2 Retrieving specific rows with <span
class="function">db2\_fetch\_array</span> from a scrollable cursor**

If your result set uses a scrollable cursor, you can call <span
class="function">db2\_fetch\_array</span> with a specific row number.
The following example retrieves every other row in the result set,
starting with the second row.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$result = db2_exec($stmt, $sql, array('cursor' => DB2_SCROLLABLE));

$i=2;
while ($row = db2_fetch_array($result, $i)) {
    printf ("%-5d %-16s %-32s %10s\n", 
        $row[0], $row[1], $row[2], $row[3]);
    $i = $i + 2;
}
?>
```

以上例程会输出：

    0     Pook             cat                                    3.20
    5     Rickety Ride     goat                                   9.70
    2     Smarty           horse                                350.00

### 参见

-   <span class="function">db2\_fetch\_assoc</span>
-   <span class="function">db2\_fetch\_both</span>
-   <span class="function">db2\_fetch\_object</span>
-   <span class="function">db2\_fetch\_row</span>
-   <span class="function">db2\_result</span>

db2\_fetch\_assoc
=================

Returns an array, indexed by column name, representing a row in a result
set

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">db2\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row_number`<span class="initializer"> = -1</span></span> \] )

Returns an array, indexed by column name, representing a row in a result
set.

### 参数

`stmt`  
A valid *stmt* resource containing a result set.

`row_number`  
Requests a specific 1-indexed row from the result set. Passing this
parameter results in a PHP warning if the result set uses a forward-only
cursor.

### 返回值

Returns an associative array with column values indexed by the column
name representing the next or requested row in the result set. Returns
**`FALSE`** if there are no rows left in the result set, or if the row
requested by `row_number` does not exist in the result set.

### 范例

**示例 \#1 Iterating through a forward-only cursor**

If you call <span class="function">db2\_fetch\_assoc</span> without a
specific row number, it automatically retrieves the next row in the
result set.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$stmt = db2_prepare($conn, $sql);
$result = db2_execute($stmt);

while ($row = db2_fetch_assoc($stmt)) {
    printf ("%-5d %-16s %-32s %10s\n", 
        $row['ID'], $row['NAME'], $row['BREED'], $row['WEIGHT']);
}
?>
```

以上例程会输出：

    0     Pook             cat                                    3.20
    5     Rickety Ride     goat                                   9.70
    2     Smarty           horse                                350.00

**示例 \#2 Retrieving specific rows with <span
class="function">db2\_fetch\_assoc</span> from a scrollable cursor**

If your result set uses a scrollable cursor, you can call <span
class="function">db2\_fetch\_assoc</span> with a specific row number.
The following example retrieves every other row in the result set,
starting with the second row.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$result = db2_exec($stmt, $sql, array('cursor' => DB2_SCROLLABLE));

$i=2;
while ($row = db2_fetch_assoc($result, $i)) {
    printf ("%-5d %-16s %-32s %10s\n", 
        $row['ID'], $row['NAME'], $row['BREED'], $row['WEIGHT']);
    $i = $i + 2;
}
?>
```

以上例程会输出：

    0     Pook             cat                                    3.20
    5     Rickety Ride     goat                                   9.70
    2     Smarty           horse                                350.00

### 参见

-   <span class="function">db2\_fetch\_array</span>
-   <span class="function">db2\_fetch\_both</span>
-   <span class="function">db2\_fetch\_object</span>
-   <span class="function">db2\_fetch\_row</span>
-   <span class="function">db2\_result</span>

db2\_fetch\_both
================

Returns an array, indexed by both column name and position, representing
a row in a result set

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">db2\_fetch\_both</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row_number`<span class="initializer"> = -1</span></span> \] )

Returns an array, indexed by both column name and position, representing
a row in a result set. Note that the row returned by <span
class="function">db2\_fetch\_both</span> requires more memory than the
single-indexed arrays returned by <span
class="function">db2\_fetch\_assoc</span> or <span
class="function">db2\_fetch\_array</span>.

### 参数

`stmt`  
A valid *stmt* resource containing a result set.

`row_number`  
Requests a specific 1-indexed row from the result set. Passing this
parameter results in a PHP warning if the result set uses a forward-only
cursor.

### 返回值

Returns an associative array with column values indexed by both the
column name and 0-indexed column number. The array represents the next
or requested row in the result set. Returns **`FALSE`** if there are no
rows left in the result set, or if the row requested by `row_number`
does not exist in the result set.

### 范例

**示例 \#1 Iterating through a forward-only cursor**

If you call <span class="function">db2\_fetch\_both</span> without a
specific row number, it automatically retrieves the next row in the
result set. The following example accesses columns in the returned array
by both column name and by numeric index.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$stmt = db2_prepare($conn, $sql);
$result = db2_execute($stmt);

while ($row = db2_fetch_both($stmt)) {
    printf ("%-5d %-16s %-32s %10s\n", 
        $row['ID'], $row[0], $row['BREED'], $row[3]);
}
?>
```

以上例程会输出：

    0     Pook             cat                                    3.20
    5     Rickety Ride     goat                                   9.70
    2     Smarty           horse                                350.00

**示例 \#2 Retrieving specific rows with <span
class="function">db2\_fetch\_both</span> from a scrollable cursor**

If your result set uses a scrollable cursor, you can call <span
class="function">db2\_fetch\_both</span> with a specific row number. The
following example retrieves every other row in the result set, starting
with the second row.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$result = db2_exec($stmt, $sql, array('cursor' => DB2_SCROLLABLE));

$i=2;
while ($row = db2_fetch_both($result, $i)) {
    printf ("%-5d %-16s %-32s %10s\n", 
        $row[0], $row['NAME'], $row[2], $row['WEIGHT']);
    $i = $i + 2;
}
?>
```

以上例程会输出：

    0     Pook             cat                                    3.20
    5     Rickety Ride     goat                                   9.70
    2     Smarty           horse                                350.00

### 参见

-   <span class="function">db2\_fetch\_array</span>
-   <span class="function">db2\_fetch\_assoc</span>
-   <span class="function">db2\_fetch\_object</span>
-   <span class="function">db2\_fetch\_row</span>
-   <span class="function">db2\_result</span>

db2\_fetch\_object
==================

Returns an object with properties representing columns in the fetched
row

### 说明

<span class="type"><span class="type">object</span><span
class="type">false</span></span> <span
class="methodname">db2\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row_number`<span class="initializer"> = -1</span></span> \] )

Returns an object in which each property represents a column returned in
the row fetched from a result set.

### 参数

`stmt`  
A valid *stmt* resource containing a result set.

`row_number`  
Requests a specific 1-indexed row from the result set. Passing this
parameter results in a PHP warning if the result set uses a forward-only
cursor.

### 返回值

Returns an object representing a single row in the result set. The
properties of the object map to the names of the columns in the result
set.

The IBM DB2, Cloudscape, and Apache Derby database servers typically
fold column names to upper-case, so the object properties will reflect
that case.

If your SELECT statement calls a scalar function to modify the value of
a column, the database servers return the column number as the name of
the column in the result set. If you prefer a more descriptive column
name and object property, you can use the AS clause to assign a name to
the column in the result set.

Returns **`FALSE`** if no row was retrieved.

### 范例

**示例 \#1 A <span class="function">db2\_fetch\_object</span> example**

The following example issues a SELECT statement with a scalar function,
RTRIM, that removes whitespace from the end of the column. Rather than
creating an object with the properties "BREED" and "2", we use the AS
clause in the SELECT statement to assign the name "name" to the modified
column. The database server folds the column names to upper-case,
resulting in an object with the properties "BREED" and "NAME".

``` php
<?php
$conn = db2_connect($database, $user, $password);

$sql = "SELECT breed, RTRIM(name) AS name
    FROM animals
    WHERE id = ?";

if ($conn) {
    $stmt = db2_prepare($conn, $sql);
    db2_execute($stmt, array(0));

    while ($pet = db2_fetch_object($stmt)) {
        echo "Come here, {$pet->NAME}, my little {$pet->BREED}!";
    }
    db2_close($conn);
}
?>
```

以上例程会输出：

    Come here, Pook, my little cat!

### 参见

-   <span class="function">db2\_fetch\_array</span>
-   <span class="function">db2\_fetch\_assoc</span>
-   <span class="function">db2\_fetch\_both</span>
-   <span class="function">db2\_fetch\_row</span>
-   <span class="function">db2\_result</span>

db2\_fetch\_row
===============

Sets the result set pointer to the next row or requested row

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row_number`</span> \] )

Use <span class="function">db2\_fetch\_row</span> to iterate through a
result set, or to point to a specific row in a result set if you
requested a scrollable cursor.

To retrieve individual fields from the result set, call the <span
class="function">db2\_result</span> function.

Rather than calling <span class="function">db2\_fetch\_row</span> and
<span class="function">db2\_result</span>, most applications will call
one of <span class="function">db2\_fetch\_assoc</span>, <span
class="function">db2\_fetch\_both</span>, or <span
class="function">db2\_fetch\_array</span> to advance the result set
pointer and return a complete row as an array.

### 参数

`stmt`  
A valid *stmt* resource.

`row_number`  
With scrollable cursors, you can request a specific row number in the
result set. Row numbering is 1-indexed.

### 返回值

Returns **`TRUE`** if the requested row exists in the result set.
Returns **`FALSE`** if the requested row does not exist in the result
set.

### 范例

**示例 \#1 Iterating through a result set**

The following example demonstrates how to iterate through a result set
with <span class="function">db2\_fetch\_row</span> and retrieve columns
from the result set with <span class="function">db2\_result</span>.

``` php
<?php
$sql = 'SELECT name, breed FROM animals WHERE weight < ?';
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, array(10));
while (db2_fetch_row($stmt)) {
    $name = db2_result($stmt, 0);
    $breed = db2_result($stmt, 1);
    print "$name $breed";
}
?>
```

以上例程会输出：

    cat Pook
    gold fish Bubbles
    budgerigar Gizmo
    goat Rickety Ride

**示例 \#2 i5/OS recommended alternatives to
db2\_fetch\_row/db2\_result**

On i5/OS it is recommended that you use <span
class="function">db2\_fetch\_both</span>, <span
class="function">db2\_fetch\_array</span>, or <span
class="function">db2\_fetch\_object</span> over <span
class="function">db2\_fetch\_row</span>/<span
class="function">db2\_result</span>. In general <span
class="function">db2\_fetch\_row</span>/<span
class="function">db2\_result</span> have more issues with various column
types in *EBCIDIC* to *ASCII* translation, including possible truncation
in *DBCS* applications. You may also find the performance of <span
class="function">db2\_fetch\_both</span>, <span
class="function">db2\_fetch\_array</span>, and <span
class="function">db2\_fetch\_object</span> to be superior to <span
class="function">db2\_fetch\_row</span>/<span
class="function">db2\_result</span>.

``` php
<?php
  $conn = db2_connect("","","");
  $sql = 'SELECT SPECIFIC_SCHEMA, SPECIFIC_NAME, ROUTINE_SCHEMA, ROUTINE_NAME, ROUTINE_TYPE, ROUTINE_CREATED, ROUTINE_BODY, IN_PARMS, OUT_PARMS, INOUT_PARMS, PARAMETER_STYLE, EXTERNAL_NAME, EXTERNAL_LANGUAGE FROM QSYS2.SYSROUTINES FETCH FIRST 2 ROWS ONLY';
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_both($stmt)){
    echo "<br>db2_fetch_both {$row['SPECIFIC_NAME']} {$row['ROUTINE_CREATED']} {$row[5]}";
  }
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_array($stmt)){
    echo "<br>db2_fetch_array {$row[1]}  {$row[5]}";
  }
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_object($stmt)){
    echo "<br>db2_fetch_object {$row->SPECIFIC_NAME} {$row->ROUTINE_CREATED}";
  }
  db2_close($conn);
?>
```

以上例程会输出：

    db2_fetch_both MATCH_ANIMAL 2006-08-25-17.10.23.775000 2006-08-25-17.10.23.775000
    db2_fetch_both MULTIRESULTS 2006-10-17-10.11.05.308000 2006-10-17-10.11.05.308000
    db2_fetch_array MATCH_ANIMAL 2006-08-25-17.10.23.775000
    db2_fetch_array MULTIRESULTS 2006-10-17-10.11.05.308000
    db2_fetch_object MATCH_ANIMAL 2006-08-25-17.10.23.775000
    db2_fetch_object MULTIRESULTS 2006-10-17-10.11.05.308000

### 参见

-   <span class="function">db2\_fetch\_array</span>
-   <span class="function">db2\_fetch\_assoc</span>
-   <span class="function">db2\_fetch\_both</span>
-   <span class="function">db2\_fetch\_object</span>
-   <span class="function">db2\_result</span>

db2\_field\_display\_size
=========================

Returns the maximum number of bytes required to display a column

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_display\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the maximum number of bytes required to display a column in a
result set.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns an integer value with the maximum number of bytes required to
display the specified column. If the column does not exist in the result
set, <span class="function">db2\_field\_display\_size</span> returns
**`FALSE`**.

### 参见

-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_type</span>
-   <span class="function">db2\_field\_width</span>

db2\_field\_name
================

Returns the name of the column in the result set

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the name of the specified column in the result set.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns a string containing the name of the specified column. If the
specified column does not exist in the result set, <span
class="function">db2\_field\_name</span> returns **`FALSE`**.

### 参见

-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_type</span>
-   <span class="function">db2\_field\_width</span>

db2\_field\_num
===============

Returns the position of the named column in a result set

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_num</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the position of the named column in a result set.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns an integer containing the 0-indexed position of the named column
in the result set. If the specified column does not exist in the result
set, <span class="function">db2\_field\_num</span> returns **`FALSE`**.

### 参见

-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_type</span>
-   <span class="function">db2\_field\_width</span>

db2\_field\_precision
=====================

Returns the precision of the indicated column in a result set

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_precision</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the precision of the indicated column in a result set.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns an integer containing the precision of the specified column. If
the specified column does not exist in the result set, <span
class="function">db2\_field\_precision</span> returns **`FALSE`**.

### 参见

-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_type</span>
-   <span class="function">db2\_field\_width</span>

db2\_field\_scale
=================

Returns the scale of the indicated column in a result set

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_scale</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the scale of the indicated column in a result set.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns an integer containing the scale of the specified column. If the
specified column does not exist in the result set, <span
class="function">db2\_field\_scale</span> returns **`FALSE`**.

### 参见

-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_type</span>
-   <span class="function">db2\_field\_width</span>

db2\_field\_type
================

Returns the data type of the indicated column in a result set

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the data type of the indicated column in a result set.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns a string containing the defined data type of the specified
column. If the specified column does not exist in the result set, <span
class="function">db2\_field\_type</span> returns **`FALSE`**.

### 参见

-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_width</span>

db2\_field\_width
=================

Returns the width of the current value of the indicated column in a
result set

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_field\_width</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column`</span> )

Returns the width of the current value of the indicated column in a
result set. This is the maximum width of the column for a fixed-length
data type, or the actual width of the column for a variable-length data
type.

### 参数

`stmt`  
Specifies a statement resource containing a result set.

`column`  
Specifies the column in the result set. This can either be an integer
representing the 0-indexed position of the column, or a string
containing the name of the column.

### 返回值

Returns an integer containing the width of the specified character or
binary data type column in a result set. If the specified column does
not exist in the result set, <span
class="function">db2\_field\_width</span> returns **`FALSE`**.

### 参见

-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_type</span>

db2\_foreign\_keys
==================

Returns a result set listing the foreign keys for a table

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_foreign\_keys</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> ,
<span class="methodparam"><span class="type">string</span>
`$table-name`</span> )

Returns a result set listing the foreign keys for a table.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables. If `schema` is **`NULL`**, <span
class="function">db2\_foreign\_keys</span> matches the schema for the
current connection.

`table-name`  
The name of the table.

### 返回值

Returns a statement resource with a result set containing rows
describing the foreign keys for the specified table. The result set is
composed of the following columns:

| Column name    | Description                                                                                                                                          |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| PKTABLE\_CAT   | Name of the catalog for the table containing the primary key. The value is NULL if this table does not have catalogs.                                |
| PKTABLE\_SCHEM | Name of the schema for the table containing the primary key.                                                                                         |
| PKTABLE\_NAME  | Name of the table containing the primary key.                                                                                                        |
| PKCOLUMN\_NAME | Name of the column containing the primary key.                                                                                                       |
| FKTABLE\_CAT   | Name of the catalog for the table containing the foreign key. The value is NULL if this table does not have catalogs.                                |
| FKTABLE\_SCHEM | Name of the schema for the table containing the foreign key.                                                                                         |
| FKTABLE\_NAME  | Name of the table containing the foreign key.                                                                                                        |
| FKCOLUMN\_NAME | Name of the column containing the foreign key.                                                                                                       |
| KEY\_SEQ       | 1-indexed position of the column in the key.                                                                                                         |
| UPDATE\_RULE   | Integer value representing the action applied to the foreign key when the SQL operation is UPDATE.                                                   |
| DELETE\_RULE   | Integer value representing the action applied to the foreign key when the SQL operation is DELETE.                                                   |
| FK\_NAME       | The name of the foreign key.                                                                                                                         |
| PK\_NAME       | The name of the primary key.                                                                                                                         |
| DEFERRABILITY  | An integer value representing whether the foreign key deferrability is SQL\_INITIALLY\_DEFERRED, SQL\_INITIALLY\_IMMEDIATE, or SQL\_NOT\_DEFERRABLE. |

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_free\_result
=================

Frees resources associated with a result set

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Frees the system and database resources that are associated with a
result set. These resources are freed implicitly when a script finishes,
but you can call <span class="function">db2\_free\_result</span> to
explicitly free the result set resources before the end of the script.

### 参数

`stmt`  
A valid statement resource.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">db2\_free\_stmt</span>

db2\_free\_stmt
===============

Frees resources associated with the indicated statement resource

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_free\_stmt</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Frees the system and database resources that are associated with a
statement resource. These resources are freed implicitly when a script
finishes, but you can call <span class="function">db2\_free\_stmt</span>
to explicitly free the statement resources before the end of the script.

### 参数

`stmt`  
A valid statement resource.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">db2\_free\_result</span>

db2\_get\_option
================

Retrieves an option value for a statement resource or a connection
resource

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">db2\_get\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$resource`</span> , <span class="methodparam"><span
class="type">string</span> `$option`</span> )

Retrieves the value of a specified option value for a statement resource
or a connection resource.

### 参数

`resource`  
A valid statement resource as returned from <span
class="function">db2\_prepare</span> or a valid connection resource as
returned from <span class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

`option`  
A valid statement or connection options. The following new options are
available as of ibm\_db2 version 1.6.0. They provide useful tracking
information that can be set during execution with <span
class="function">db2\_get\_option</span>.

> **Note**:
>
> Prior versions of ibm\_db2 do not support these new options.
>
> When the value in each option is being set, some servers might not
> handle the entire length provided and might truncate the value.
>
> To ensure that the data specified in each option is converted
> correctly when transmitted to a host system, use only the characters A
> through Z, 0 through 9, and the underscore (\_) or period (.).

`userid`  
*SQL\_ATTR\_INFO\_USERID* - A pointer to a null-terminated character
string used to identify the client user ID sent to the host database
server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 16
> characters. This user-id is not to be confused with the authentication
> user-id, it is for identification purposes only and is not used for
> any authorization.

`acctstr`  
*SQL\_ATTR\_INFO\_ACCTSTR* - A pointer to a null-terminated character
string used to identify the client accounting string sent to the host
database server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 200
> characters.

`applname`  
*SQL\_ATTR\_INFO\_APPLNAME* - A pointer to a null-terminated character
string used to identify the client application name sent to the host
database server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 32
> characters.

`wrkstnname`  
*SQL\_ATTR\_INFO\_WRKSTNNAME* - A pointer to a null-terminated character
string used to identify the client workstation name sent to the host
database server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 18
> characters.

The following table specifies which options are compatible with the
available resource types:

**Resource-Parameter Matrix**

Key

Value

Resource Type

 

 

Connection

Statement

Result Set

userid

*SQL\_ATTR\_INFO\_USERID*

X

X

\-

acctstr

*SQL\_ATTR\_INFO\_ACCTSTR*

X

X

\-

applname

*SQL\_ATTR\_INFO\_APPLNAME*

X

X

\-

wrkstnname

*SQL\_ATTR\_INFO\_WRKSTNNAME*

X

X

\-

### 返回值

Returns the current setting of the connection attribute provided on
success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Setting and retrieving parameters through a connection
resource**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$user     = 'db2inst1';
$password = 'ibmdb2';

/* Obtain Connection Resource */
$conn = db2_connect($database, $user, $password);

echo "Client attributes passed through connection string:\n";

/* Create the associative options array with valid key-value pairs */
/* Assign the attributes through connection string */
/* Access the options specified */
$options1 = array('userid' => 'db2inst1');
$conn1 = db2_connect($database, $user, $password, $options1);
$val = db2_get_option($conn1, 'userid');
echo $val . "\n";

$options2 = array('acctstr' => 'account');
$conn2 = db2_connect($database, $user, $password, $options2);
$val = db2_get_option($conn2, 'acctstr');
echo $val . "\n";

$options3 = array('applname' => 'myapp');
$conn3 = db2_connect($database, $user, $password, $options3);
$val = db2_get_option($conn3, 'applname');
echo $val . "\n";

$options4 = array('wrkstnname' => 'workstation');
$conn4 = db2_connect($database, $user, $password, $options4);
$val = db2_get_option($conn4, 'wrkstnname');
echo $val . "\n";

echo "Client attributes passed post-connection:\n";

/* Create the associative options array with valid key-value pairs */
/* Assign the attributes after a connection is made */
/* Access the options specified */
$options5 = array('userid' => 'db2inst1');
$conn5 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn5, $options5, 1);
$val = db2_get_option($conn5, 'userid');
echo $val . "\n";

$options6 = array('acctstr' => 'account');
$conn6 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn6, $options6, 1);
$val = db2_get_option($conn6, 'acctstr');
echo $val . "\n";

$options7 = array('applname' => 'myapp');
$conn7 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn7, $options7, 1);
$val = db2_get_option($conn7, 'applname');
echo $val . "\n";

$options8 = array('wrkstnname' => 'workstation');
$conn8 = db2_connect($database, $user, $password);
$rc = db2_set_option($conn8, $options8, 1);
$val = db2_get_option($conn8, 'wrkstnname');
echo $val . "\n";
?>
```

以上例程会输出：

    Client attributes passed through connection string:
    db2inst1
    account
    myapp
    workstation
    Client attributes passed post-connection:
    db2inst1
    account
    myapp
    workstation

### 参见

-   <span class="function">db2\_connect</span>
-   <span class="function">db2\_cursor\_type</span>
-   <span class="function">db2\_exec</span>
-   <span class="function">db2\_set\_option</span>
-   <span class="function">db2\_pconnect</span>
-   <span class="function">db2\_prepare</span>

db2\_last\_insert\_id
=====================

Returns the auto generated ID of the last insert query that successfully
executed on this connection

### 说明

<span class="type">string</span> <span
class="methodname">db2\_last\_insert\_id</span> ( <span
class="methodparam"><span class="type">resource</span>
`$resource`</span> )

Returns the auto generated ID of the last insert query that successfully
executed on this connection.

The result of this function is not affected by any of the following:

-   A single row INSERT statement with a VALUES clause for a table
    without an identity column.

-   A multiple row INSERT statement with a VALUES clause.

-   An INSERT statement with a fullselect.

-   A ROLLBACK TO SAVEPOINT statement.

### 参数

`resource`  
A valid connection resource as returned from <span
class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>. The value of this parameter
cannot be a statement resource or result set resource.

### 返回值

Returns the auto generated ID of last insert query that successfully
executed on this connection.

### 范例

**示例 \#1 A <span class="function">db2\_last\_insert\_id</span>
example**

The following example shows how to return the auto generated ID of last
insert query that successfully executed on this connection.

``` php
<?php

$database = "SAMPLE";
$user = "db2inst1";
$password = "ibmdb2";

$conn = db2_connect($database, $user, $password);
if($conn) {
    $createTable = "CREATE TABLE lastInsertID 
      (id integer GENERATED BY DEFAULT AS IDENTITY, name varchar(20))";
    $insertTable = "INSERT INTO lastInsertID (name) VALUES ('Temp Name')";

    $stmt = @db2_exec($conn, $createTable);

    /* Checking for single row inserted. */
    $stmt = db2_exec($conn, $insertTable);
    $ret =  db2_last_insert_id($conn);
    if($ret) {
        echo "Last Insert ID is : " . $ret . "\n";
    } else {
        echo "No Last insert ID.\n";
    }
    
    db2_close($conn);
}
else {
    echo "Connection failed.";
}
?>
```

以上例程会输出：

    Last Insert ID is : 1

db2\_lob\_read
==============

Gets a user defined size of LOB files with each invocation

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">db2\_lob\_read</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">int</span> `$colnum`</span>
, <span class="methodparam"><span class="type">int</span>
`$length`</span> )

Use <span class="function">db2\_lob\_read</span> to iterate through a
specified column of a result set and retrieve a user defined size of LOB
data.

### 参数

`stmt`  
A valid *stmt* resource containing LOB data.

`colnum`  
A valid column number in the result set of the *stmt* resource.

`length`  
The size of the LOB data to be retrieved from the *stmt* resource.

### 返回值

Returns the amount of data the user specifies. Returns **`FALSE`** if
the data cannot be retrieved.

### 范例

**示例 \#1 Iterating through different types of data**

``` php
<?php

/* Database Connection Parameters */
$db = 'SAMPLE';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Obtain Connection Resource */
$conn = db2_connect($db,$username,$password);

if ($conn) {
    $drop = 'DROP TABLE clob_stream';
    $result = @db2_exec( $conn, $drop );

    $create = 'CREATE TABLE clob_stream (id INTEGER, my_clob CLOB)';
    $result = db2_exec( $conn, $create );

    $variable = "";
    $stmt = db2_prepare($conn, "INSERT INTO clob_stream (id,my_clob) VALUES (1, ?)");
    $variable = "THIS IS A CLOB TEST. THIS IS A CLOB TEST.";
    db2_bind_param($stmt, 1, "variable", DB2_PARAM_IN);
    db2_execute($stmt);

    $sql = "SELECT id,my_clob FROM clob_stream";
    $result = db2_prepare($conn, $sql);
    db2_execute($result);
    db2_fetch_row($result);
    $i = 0;
    /* Read LOB data */
    while ($data = db2_lob_read($result, 2, 6)) {
        echo "Loop $i: $data\n";
        $i = $i + 1;
    }

    $drop = 'DROP TABLE blob_stream';
    $result = @db2_exec( $conn, $drop );

    $create = 'CREATE TABLE blob_stream (id INTEGER, my_blob CLOB)';
    $result = db2_exec( $conn, $create );

    $variable = "";
    $stmt = db2_prepare($conn, "INSERT INTO blob_stream (id,my_blob) VALUES (1, ?)");
    $variable = "THIS IS A BLOB TEST. THIS IS A BLOB TEST.";
    db2_bind_param($stmt, 1, "variable", DB2_PARAM_IN);
    db2_execute($stmt);

    $sql = "SELECT id,my_blob FROM blob_stream";
    $result = db2_prepare($conn, $sql);
    db2_execute($result);
    db2_fetch_row($result);
    $i = 0;
    /* Read LOB data */
    while ($data = db2_lob_read($result, 2, 6)) {
        echo "Loop $i: $data\n";
        $i = $i + 1;
    }
} else {
    echo 'no connection: ' . db2_conn_errormsg();
}

?>
```

以上例程会输出：

    Loop 0: THIS I
    Loop 1: S A CL
    Loop 2: OB TES
    Loop 3: T. THI
    Loop 4: S IS A
    Loop 5:  CLOB 
    Loop 6: TEST.
    Loop 0: THIS I
    Loop 1: S A BL
    Loop 2: OB TES
    Loop 3: T. THI
    Loop 4: S IS A
    Loop 5:  BLOB 
    Loop 6: TEST.

### 参见

-   <span class="function">db2\_bind\_param</span>
-   <span class="function">db2\_exec</span>
-   <span class="function">db2\_execute</span>
-   <span class="function">db2\_fetch\_row</span>
-   <span class="function">db2\_prepare</span>
-   <span class="function">db2\_result</span>

db2\_next\_result
=================

Requests the next result set from a stored procedure

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">db2\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

A stored procedure can return zero or more result sets. While you handle
the first result set in exactly the same way you would handle the
results returned by a simple SELECT statement, to fetch the second and
subsequent result sets from a stored procedure you must call the <span
class="function">db2\_next\_result</span> function and return the result
to a uniquely named PHP variable.

### 参数

`stmt`  
A prepared statement returned from <span
class="function">db2\_exec</span> or <span
class="function">db2\_execute</span>.

### 返回值

Returns a new statement resource containing the next result set if the
stored procedure returned another result set. Returns **`FALSE`** if the
stored procedure did not return another result set.

### 范例

**示例 \#1 Calling a stored procedure that returns multiple result
sets**

In the following example, we call a stored procedure that returns three
result sets. The first result set is fetched directly from the same
statement resource on which we invoked the CALL statement, while the
second and third result sets are fetched from statement resources
returned from our calls to the <span
class="function">db2\_next\_result</span> function.

``` php
<?php
$conn = db2_connect($database, $user, $password);

if ($conn) {
  $stmt = db2_exec($conn, 'CALL multiResults()');

  print "Fetching first result set\n";
  while ($row = db2_fetch_array($stmt)) {
    var_dump($row);
  }

  print "\nFetching second result set\n";
  $res = db2_next_result($stmt);
  if ($res) {
    while ($row = db2_fetch_array($res)) {
      var_dump($row);
    }
  }

  print "\nFetching third result set\n";
  $res2 = db2_next_result($stmt);
  if ($res2) {
    while ($row = db2_fetch_array($res2)) {
      var_dump($row);
    }
  }

  db2_close($conn);
}
?>
```

以上例程会输出：

    Fetching first result set
    array(2) {
      [0]=>
      string(16) "Bubbles         "
      [1]=>
      int(3)
    }
    array(2) {
      [0]=>
      string(16) "Gizmo           "
      [1]=>
      int(4)
    }

    Fetching second result set
    array(4) {
      [0]=>
      string(16) "Sweater         "
      [1]=>
      int(6)
      [2]=>
      string(5) "llama"
      [3]=>
      string(6) "150.00"
    }
    array(4) {
      [0]=>
      string(16) "Smarty          "
      [1]=>
      int(2)
      [2]=>
      string(5) "horse"
      [3]=>
      string(6) "350.00"
    }

    Fetching third result set
    array(1) {
      [0]=>
      string(16) "Bubbles         "
    }
    array(1) {
      [0]=>
      string(16) "Gizmo           "
    }

db2\_num\_fields
================

Returns the number of fields contained in a result set

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Returns the number of fields contained in a result set. This is most
useful for handling the result sets returned by dynamically generated
queries, or for result sets returned by stored procedures, where your
application cannot otherwise know how to retrieve and use the results.

### 参数

`stmt`  
A valid statement resource containing a result set.

### 返回值

Returns an integer value representing the number of fields in the result
set associated with the specified statement resource. Returns
**`FALSE`** if the statement resource is not a valid input value.

### 范例

**示例 \#1 Retrieving the number of fields in a result set**

The following example demonstrates how to retrieve the number of fields
returned in a result set.

``` php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, $sql);
$columns = db2_num_fields($stmt);

echo "There are {$columns} columns in the result set.";
?>
```

以上例程会输出：

    There are 4 columns in the result set.

### 参见

-   <span class="function">db2\_execute</span>
-   <span class="function">db2\_field\_display\_size</span>
-   <span class="function">db2\_field\_name</span>
-   <span class="function">db2\_field\_num</span>
-   <span class="function">db2\_field\_precision</span>
-   <span class="function">db2\_field\_scale</span>
-   <span class="function">db2\_field\_type</span>
-   <span class="function">db2\_field\_width</span>

db2\_num\_rows
==============

Returns the number of rows affected by an SQL statement

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">db2\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Returns the number of rows deleted, inserted, or updated by an SQL
statement.

To determine the number of rows that will be returned by a SELECT
statement, issue SELECT COUNT(\*) with the same predicates as your
intended SELECT statement and retrieve the value.

If your application logic checks the number of rows returned by a SELECT
statement and branches if the number of rows is 0, consider modifying
your application to attempt to return the first row with one of <span
class="function">db2\_fetch\_assoc</span>, <span
class="function">db2\_fetch\_both</span>, <span
class="function">db2\_fetch\_array</span>, or <span
class="function">db2\_fetch\_row</span>, and branch if the fetch
function returns **`FALSE`**.

> **Note**:
>
> If you issue a SELECT statement using a scrollable cursor, <span
> class="function">db2\_num\_rows</span> returns the number of rows
> returned by the SELECT statement. However, the overhead associated
> with scrollable cursors significantly degrades the performance of your
> application, so if this is the only reason you are considering using
> scrollable cursors, you should use a forward-only cursor and either
> call SELECT COUNT(\*) or rely on the <span class="type">bool</span>
> return value of the fetch functions to achieve the equivalent
> functionality with much better performance.

### 参数

`stmt`  
A valid *stmt* resource containing a result set.

### 返回值

Returns the number of rows affected by the last SQL statement issued by
the specified statement handle.

db2\_pclose
===========

Closes a persistent database connection

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_pclose</span> ( <span class="methodparam"><span
class="type">resource</span> `$resource`</span> )

This function closes a DB2 client connection created with <span
class="function">db2\_pconnect</span> and returns the corresponding
resources to the database server.

> **Note**:
>
> This function is only available on i5/OS in response to i5/OS system
> administration requests.

If you have a persistent DB2 client connection created with <span
class="function">db2\_pconnect</span>, you may use this function to
close the connection. To avoid substantial connection performance
penalties, this function should only be used in rare cases when the
persistent connection has become unresponsive or the persistent
connection will not be needed for a long period of time.

### 参数

`connection`  
Specifies an active DB2 client connection.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Closing a persistent connection**

The following example demonstrates a successful attempt to close a
connection to an IBM DB2 i5/OS database.

``` php
<?php
$conn = db2_pconnect('', '', '');
$rc = db2_pclose($conn);
if ($rc) {
    echo "Connection was successfully closed.";
}
?>
```

以上例程会输出：

    Connection was successfully closed.

### 参见

-   <span class="function">db2\_close</span>
-   <span class="function">db2\_pconnect</span>

db2\_pconnect
=============

Returns a persistent connection to a database

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">db2\_pconnect</span> ( <span
class="methodparam"><span class="type">string</span> `$database`</span>
, <span class="methodparam"><span class="type">string</span>
`$username`</span> , <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

Returns a persistent connection to an IBM DB2 Universal Database, IBM
Cloudscape, or Apache Derby database.

For more information on persistent connections, refer to
<a href="/features/persistent-connections.html" class="xref">数据库持久连接</a>.

Calling <span class="function">db2\_close</span> on a persistent
connection always returns **`TRUE`**, but the underlying DB2 client
connection remains open and waiting to serve the next matching <span
class="function">db2\_pconnect</span> request.

Users running version 1.9.0 or later of ibm\_db2 should be aware that
the extension will perform a transaction rollback on persistent
connections at the end of a request, thus ending the transaction. This
prevents the transaction block from carrying over to the next request
which uses that connection if script execution ends before the
transaction block does.

### 参数

`database`  
The database alias in the DB2 client catalog.

`username`  
The username with which you are connecting to the database.

`password`  
The password with which you are connecting to the database.

`options`  
An associative array of connection options that affect the behavior of
the connection, where valid array keys include:

`autocommit`  
Passing the *DB2\_AUTOCOMMIT\_ON* value turns autocommit on for this
connection handle.

Passing the *DB2\_AUTOCOMMIT\_OFF* value turns autocommit off for this
connection handle.

`DB2_ATTR_CASE`  
Passing the *DB2\_CASE\_NATURAL* value specifies that column names are
returned in natural case.

Passing the *DB2\_CASE\_LOWER* value specifies that column names are
returned in lower case.

Passing the *DB2\_CASE\_UPPER* value specifies that column names are
returned in upper case.

`CURSOR`  
Passing the *DB2\_FORWARD\_ONLY* value specifies a forward-only cursor
for a statement resource. This is the default cursor type and is
supported on all database servers.

Passing the *DB2\_SCROLLABLE* value specifies a scrollable cursor for a
statement resource. This mode enables random access to rows in a result
set, but currently is supported only by IBM DB2 Universal Database.

The following new option is available in ibm\_db2 version 1.7.0 and
later.

`trustedcontext`  
Passing the DB2\_TRUSTED\_CONTEXT\_ENABLE value turns trusted context on
for this connection handle. This parameter cannot be set using <span
class="function">db2\_set\_option</span>.

This key works only if the database is cataloged (even if the database
is local), or if you specify the full DSN when you create the
connection.

To catalog the database, use following commands:

``` literallayout
db2 catalog tcpip node loopback remote <SERVERNAME> server <SERVICENAME>
db2 catalog database <LOCALDBNAME> as <REMOTEDBNAME> at node loopback
db2 "update dbm cfg using svcename <SERVICENAME>"
db2set DB2COMM=TCPIP
```

The following new i5/OS options are available in ibm\_db2 version 1.5.1
and later.

**小贴士**
Conflicting connection attributes used in conjunction with persistent
connections can produce indeterminate results on i5/OS. Site policies
should be establish for all applications using each persistent
connection user profile. The default DB2\_AUTOCOMMIT\_ON is suggested
when using persistent connections.

`i5_lib`  
A character value that indicates the default library that will be used
for resolving unqualified file references. This is not valid if the
connection is using system naming mode.

`i5_naming`  
*DB2\_I5\_NAMING\_ON* value turns on DB2 UDB CLI iSeries system naming
mode. Files are qualified using the slash (/) delimiter. Unqualified
files are resolved using the library list for the job.

*DB2\_I5\_NAMING\_OFF* value turns off DB2 UDB CLI default naming mode,
which is SQL naming. Files are qualified using the period (.) delimiter.
Unqualified files are resolved using either the default library or the
current user ID.

`i5_commit`  
The `i5_commit` attribute should be set before the <span
class="function">db2\_pconnect</span>. If the value is changed after the
connection has been established, and the connection is to a remote data
source, the change does not take effect until the next successful <span
class="function">db2\_pconnect</span> for the connection handle.

> **Note**:
>
> The php.ini setting `ibm_db2.i5_allow_commit`==0 or
> *DB2\_I5\_TXN\_NO\_COMMIT* is the default, but may be overridden with
> the `i5_commit` option.

*DB2\_I5\_TXN\_NO\_COMMIT* - Commitment control is not used.

*DB2\_I5\_TXN\_READ\_UNCOMMITTED* - Dirty reads, nonrepeatable reads,
and phantoms are possible.

*DB2\_I5\_TXN\_READ\_COMMITTED* - Dirty reads are not possible.
Nonrepeatable reads, and phantoms are possible.

*DB2\_I5\_TXN\_REPEATABLE\_READ* - Dirty reads and nonrepeatable reads
are not possible. Phantoms are possible.

*DB2\_I5\_TXN\_SERIALIZABLE* - Transactions are serializable. Dirty
reads, non-repeatable reads, and phantoms are not possible

`i5_query_optimize`  
*DB2\_FIRST\_IO* All queries are optimized with the goal of returning
the first page of output as fast as possible. This goal works well when
the output is controlled by a user who is most likely to cancel the
query after viewing the first page of output data. Queries coded with an
OPTIMIZE FOR nnn ROWS clause honor the goal specified by the clause.

*DB2\_ALL\_IO* All queries are optimized with the goal of running the
entire query to completion in the shortest amount of elapsed time. This
is a good option when the output of a query is being written to a file
or report, or the interface is queuing the output data. Queries coded
with an OPTIMIZE FOR nnn ROWS clause honor the goal specified by the
clause. This is the default.

`i5_dbcs_alloc`  
*DB2\_I5\_DBCS\_ALLOC\_ON* value turns on DB2 6X allocation scheme for
DBCS translation column size growth.

*DB2\_I5\_DBCS\_ALLOC\_OFF* value turns off DB2 6X allocation scheme for
DBCS translation column size growth.

> **Note**:
>
> The php.ini setting `ibm_db2.i5_dbcs_alloc`==0 or
> *DB2\_I5\_DBCS\_ALLOC\_OFF* is the default, but may be overridden with
> the `i5_dbcs_alloc` option.

`i5_date_fmt`  
*DB2\_I5\_FMT\_ISO* - The International Organization for Standardization
(ISO) date format yyyy-mm-dd is used. This is the default.

*DB2\_I5\_FMT\_USA* - The United States date format mm/dd/yyyy is used.

*DB2\_I5\_FMT\_EUR* - The European date format dd.mm.yyyy is used.

*DB2\_I5\_FMT\_JIS* - The Japanese Industrial Standard date format
yyyy-mm-dd is used.

*DB2\_I5\_FMT\_MDY* - The date format mm/dd/yyyy is used.

*DB2\_I5\_FMT\_DMY* - The date format dd/mm/yyyy is used.

*DB2\_I5\_FMT\_YMD* - The date format yy/mm/dd is used.

*DB2\_I5\_FMT\_JUL* - The Julian date format yy/ddd is used.

*DB2\_I5\_FMT\_JOB* - The job default is used.

`i5_date_sep`  
*DB2\_I5\_SEP\_SLASH* - A slash ( / ) is used as the date separator.
This is the default.

*DB2\_I5\_SEP\_DASH* - A dash ( - ) is used as the date separator.

*DB2\_I5\_SEP\_PERIOD* - A period ( . ) is used as the date separator.

*DB2\_I5\_SEP\_COMMA* - A comma ( , ) is used as the date separator.

*DB2\_I5\_SEP\_BLANK* - A blank is used as the date separator.

*DB2\_I5\_SEP\_JOB* - The job default is used

`i5_time_fmt`  
*DB2\_I5\_FMT\_ISO* - The International Organization for Standardization
(ISO) time format hh.mm.ss is used. This is the default.

*DB2\_I5\_FMT\_USA* - The United States time format hh:mmxx is used,
where xx is AM or PM.

*DB2\_I5\_FMT\_EUR* - The European time format hh.mm.ss is used.

*DB2\_I5\_FMT\_JIS* - The Japanese Industrial Standard time format
hh:mm:ss is used.

*DB2\_I5\_FMT\_HMS* - The hh:mm:ss format is used.

`i5_time_sep`  
*DB2\_I5\_SEP\_COLON* - A colon ( : ) is used as the time separator.
This is the default.

*DB2\_I5\_SEP\_PERIOD* - A period ( . ) is used as the time separator.

*DB2\_I5\_SEP\_COMMA* - A comma ( , ) is used as the time separator.

*DB2\_I5\_SEP\_BLANK* - A blank is used as the time separator.

*DB2\_I5\_SEP\_JOB* - The job default is used.

`i5_decimal_sep`  
*DB2\_I5\_SEP\_PERIOD* - A period ( . ) is used as the decimal
separator. This is the default.

*DB2\_I5\_SEP\_COMMA* - A comma ( , ) is used as the decimal separator.

*DB2\_I5\_SEP\_JOB* - The job default is used.

The following new i5/OS option is available in ibm\_db2 version 1.8.0
and later.

`i5_libl`  
A character value that indicates the library list that will be used for
resolving unqualified file references. Specify the library list elements
separated by blanks 'i5\_libl'=\>"MYLIB YOURLIB ANYLIB".

> **Note**:
>
> i5\_libl calls qsys2/qcmdexc('cmd',cmdlen), which is only available in
> i5/OS V5R4 and later.

### 返回值

Returns a connection handle resource if the connection attempt is
successful. <span class="function">db2\_pconnect</span> tries to reuse
an existing connection resource that exactly matches the `database`,
`username`, and `password` parameters. If the connection attempt fails,
<span class="function">db2\_pconnect</span> returns **`FALSE`**.

### 更新日志

| 版本           | 说明                                                                                                                                                                                                 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ibm\_db2 1.9.0 | Active transactions within a persistent connection will be rolled back at the end of each request.                                                                                                   |
| ibm\_db2 1.8.0 | The `i5_libl` option is available for i5/OS users.                                                                                                                                                   |
| ibm\_db2 1.7.0 | The `trustedcontext` option is available.                                                                                                                                                            |
| ibm\_db2 1.5.1 | The `i5_lib`, `i5_naming`, `i5_commit`, `i5_query_optimize`, `i5_dbcs_alloc`, `i5_date_fmt`, `i5_date_sep`, `i5_time_fmt`, `i5_time_sep` and `i5_decimal_sep` options are available for i5/OS users. |

### 范例

**示例 \#1 A <span class="function">db2\_pconnect</span> example**

In the following example, the first call to <span
class="function">db2\_pconnect</span> returns a new persistent
connection resource. The second call to <span
class="function">db2\_pconnect</span> returns a persistent connection
resource that simply reuses the first persistent connection resource.

``` php
<?php
$database = 'SAMPLE';
$user = 'db2inst1';
$password = 'ibmdb2';

$pconn = db2_pconnect($database, $user, $password);

if ($pconn) {
    echo "Persistent connection succeeded.";
}
else {
    echo "Persistent connection failed.";
}

$pconn2 = db2_pconnect($database, $user, $password);
if ($pconn) {
    echo "Second persistent connection succeeded.";
}
else {
    echo "Second persistent connection failed.";
}
?>
```

以上例程会输出：

    Persistent connection succeeded.
    Second persistent connection succeeded.

**示例 \#2 Using trusted context**

The following example shows how to enable trusted context, switch users,
and get the current user ID.

``` php
<?php

$database = "SAMPLE";
$hostname = "localhost";
$port = 50000;
$authID = "db2inst1";
$auth_pass = "ibmdb2";

$tc_user = "tcuser";
$tc_pass = "tcpassword";

$dsn = "DATABASE=$database;HOSTNAME=$hostname;PORT=$port;
  PROTOCOL=TCPIP;UID=$authID;PWD=$auth_pass;";
$options = array ("trustedcontext" => DB2_TRUSTED_CONTEXT_ENABLE);

$tc_conn = db2_pconnect($dsn, "", "", $options);
if($tc_conn) {
    echo "Explicit trusted connection succeeded.\n";

    if(db2_get_option($tc_conn, "trustedcontext")) {
        $userBefore = db2_get_option($tc_conn, "trusted_user");
        
        //Do some work as user 1.

        //Switching to trusted user.
        $parameters = array("trusted_user" => $tc_user, 
          "trusted_password" => $tcuser_pass);
        $res = db2_set_option ($tc_conn, $parameters, 1);

        $userAfter = db2_get_option($tc_conn, "trusted_user");
        //Do more work as trusted user.

        if($userBefore != $userAfter) {
            echo "User has been switched." . "\n";    
        }
    }

    db2_close($tc_conn);
}
else {
    echo "Explicit trusted connection failed.\n";
}
?>
```

以上例程会输出：

    Explicit trusted connection succeeded.
    User has been switched.

### 参见

-   <span class="function">db2\_connect</span>

db2\_prepare
============

Prepares an SQL statement to be executed

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">db2\_prepare</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span> `$statement`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="function">db2\_prepare</span> creates a prepared SQL
statement which can include 0 or more parameter markers (*?* characters)
representing parameters for input, output, or input/output. You can pass
parameters to the prepared statement using <span
class="function">db2\_bind\_param</span>, or for input values only, as
an array passed to <span class="function">db2\_execute</span>.

There are three main advantages to using prepared statements in your
application:

-   *Performance*: when you prepare a statement, the database server
    creates an optimized access plan for retrieving data with that
    statement. Subsequently issuing the prepared statement with <span
    class="function">db2\_execute</span> enables the statements to reuse
    that access plan and avoids the overhead of dynamically creating a
    new access plan for every statement you issue.

-   *Security*: when you prepare a statement, you can include parameter
    markers for input values. When you execute a prepared statement with
    input values for placeholders, the database server checks each input
    value to ensure that the type matches the column definition or
    parameter definition.

-   *Advanced functionality*: Parameter markers not only enable you to
    pass input values to prepared SQL statements, they also enable you
    to retrieve OUT and INOUT parameters from stored procedures using
    <span class="function">db2\_bind\_param</span>.

### 参数

`connection`  
A valid database connection resource variable as returned from <span
class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

`statement`  
An SQL statement, optionally containing one or more parameter markers..

`options`  
An associative array containing statement options. You can use this
parameter to request a scrollable cursor on database servers that
support this functionality.

For a description of valid statement options, see <span
class="function">db2\_set\_option</span>.

### 返回值

Returns a statement resource if the SQL statement was successfully
parsed and prepared by the database server. Returns **`FALSE`** if the
database server returned an error. You can determine which error was
returned by calling <span class="function">db2\_stmt\_error</span> or
<span class="function">db2\_stmt\_errormsg</span>.

### 范例

**示例 \#1 Preparing and executing an SQL statement with parameter
markers**

The following example prepares an INSERT statement that accepts four
parameter markers, then iterates over an array of arrays containing the
input values to be passed to <span class="function">db2\_execute</span>.

``` php
<?php
$animals = array(
    array(0, 'cat', 'Pook', 3.2),
    array(1, 'dog', 'Peaches', 12.3),
    array(2, 'horse', 'Smarty', 350.0),
);

$insert = 'INSERT INTO animals (id, breed, name, weight)
    VALUES (?, ?, ?, ?)';
$stmt = db2_prepare($conn, $insert);
if ($stmt) {
    foreach ($animals as $animal) {
        $result = db2_execute($stmt, $animal);
    }
}
?>
```

### 参见

-   <span class="function">db2\_bind\_param</span>
-   <span class="function">db2\_execute</span>
-   <span class="function">db2\_stmt\_error</span>
-   <span class="function">db2\_stmt\_errormsg</span>

db2\_primary\_keys
==================

Returns a result set listing primary keys for a table

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_primary\_keys</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> ,
<span class="methodparam"><span class="type">string</span>
`$table-name`</span> )

Returns a result set listing the primary keys for a table.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables. If `schema` is **`NULL`**, <span
class="function">db2\_primary\_keys</span> matches the schema for the
current connection.

`table-name`  
The name of the table.

### 返回值

Returns a statement resource with a result set containing rows
describing the primary keys for the specified table. The result set is
composed of the following columns:

| Column name  | Description                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| TABLE\_CAT   | Name of the catalog for the table containing the primary key. The value is NULL if this table does not have catalogs. |
| TABLE\_SCHEM | Name of the schema for the table containing the primary key.                                                          |
| TABLE\_NAME  | Name of the table containing the primary key.                                                                         |
| COLUMN\_NAME | Name of the column containing the primary key.                                                                        |
| KEY\_SEQ     | 1-indexed position of the column in the key.                                                                          |
| PK\_NAME     | The name of the primary key.                                                                                          |

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_procedure\_columns
=======================

Returns a result set listing stored procedure parameters

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_procedure\_columns</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> ,
<span class="methodparam"><span class="type">string</span>
`$procedure`</span> , <span class="methodparam"><span
class="type">string</span> `$parameter`</span> )

Returns a result set listing the parameters for one or more stored
procedures.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the procedures. This parameter accepts a
search pattern containing *\_* and *%* as wildcards.

`procedure`  
The name of the procedure. This parameter accepts a search pattern
containing *\_* and *%* as wildcards.

`parameter`  
The name of the parameter. This parameter accepts a search pattern
containing *\_* and *%* as wildcards. If this parameter is **`NULL`**,
all parameters for the specified stored procedures are returned.

### 返回值

Returns a statement resource with a result set containing rows
describing the parameters for the stored procedures matching the
specified parameters. The rows are composed of the following columns:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PROCEDURE_CAT</td>
<td>The catalog that contains the procedure. The value is <strong><code>NULL</code></strong> if this table does not have catalogs.</td>
</tr>
<tr class="even">
<td>PROCEDURE_SCHEM</td>
<td>Name of the schema that contains the stored procedure.</td>
</tr>
<tr class="odd">
<td>PROCEDURE_NAME</td>
<td>Name of the procedure.</td>
</tr>
<tr class="even">
<td>COLUMN_NAME</td>
<td>Name of the parameter.</td>
</tr>
<tr class="odd">
<td>COLUMN_TYPE</td>
<td><p>An integer value representing the type of the parameter:</p>
<table>
<thead>
<tr class="header">
<th>Return value</th>
<th>Parameter type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1 (SQL_PARAM_INPUT)</td>
<td>Input (IN) parameter.</td>
</tr>
<tr class="even">
<td>2 (SQL_PARAM_INPUT_OUTPUT)</td>
<td>Input/output (INOUT) parameter.</td>
</tr>
<tr class="odd">
<td>3 (SQL_PARAM_OUTPUT)</td>
<td>Output (OUT) parameter.</td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="even">
<td>DATA_TYPE</td>
<td>The SQL data type for the parameter represented as an integer value.</td>
</tr>
<tr class="odd">
<td>TYPE_NAME</td>
<td>A string representing the data type for the parameter.</td>
</tr>
<tr class="even">
<td>COLUMN_SIZE</td>
<td>An integer value representing the size of the parameter.</td>
</tr>
<tr class="odd">
<td>BUFFER_LENGTH</td>
<td>Maximum number of bytes necessary to store data for this parameter.</td>
</tr>
<tr class="even">
<td>DECIMAL_DIGITS</td>
<td>The scale of the parameter, or <strong><code>NULL</code></strong> where scale is not applicable.</td>
</tr>
<tr class="odd">
<td>NUM_PREC_RADIX</td>
<td>An integer value of either <em>10</em> (representing an exact numeric data type), <em>2</em> (representing an approximate numeric data type), or <strong><code>NULL</code></strong> (representing a data type for which radix is not applicable).</td>
</tr>
<tr class="even">
<td>NULLABLE</td>
<td>An integer value representing whether the parameter is nullable or not.</td>
</tr>
<tr class="odd">
<td>REMARKS</td>
<td>Description of the parameter.</td>
</tr>
<tr class="even">
<td>COLUMN_DEF</td>
<td>Default value for the parameter.</td>
</tr>
<tr class="odd">
<td>SQL_DATA_TYPE</td>
<td>An integer value representing the size of the parameter.</td>
</tr>
<tr class="even">
<td>SQL_DATETIME_SUB</td>
<td>Returns an integer value representing a datetime subtype code, or <strong><code>NULL</code></strong> for SQL data types to which this does not apply.</td>
</tr>
<tr class="odd">
<td>CHAR_OCTET_LENGTH</td>
<td>Maximum length in octets for a character data type parameter, which matches COLUMN_SIZE for single-byte character set data, or <strong><code>NULL</code></strong> for non-character data types.</td>
</tr>
<tr class="even">
<td>ORDINAL_POSITION</td>
<td>The 1-indexed position of the parameter in the CALL statement.</td>
</tr>
<tr class="odd">
<td>IS_NULLABLE</td>
<td>A string value where 'YES' means that the parameter accepts or returns <strong><code>NULL</code></strong> values and 'NO' means that the parameter does not accept or return <strong><code>NULL</code></strong> values.</td>
</tr>
</tbody>
</table>

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_procedures
===============

Returns a result set listing the stored procedures registered in a
database

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_procedures</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> ,
<span class="methodparam"><span class="type">string</span>
`$procedure`</span> )

Returns a result set listing the stored procedures registered in a
database.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the procedures. This parameter accepts a
search pattern containing *\_* and *%* as wildcards.

`procedure`  
The name of the procedure. This parameter accepts a search pattern
containing *\_* and *%* as wildcards.

### 返回值

Returns a statement resource with a result set containing rows
describing the stored procedures matching the specified parameters. The
rows are composed of the following columns:

| Column name         | Description                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------|
| PROCEDURE\_CAT      | The catalog that contains the procedure. The value is **`NULL`** if this table does not have catalogs. |
| PROCEDURE\_SCHEM    | Name of the schema that contains the stored procedure.                                                 |
| PROCEDURE\_NAME     | Name of the procedure.                                                                                 |
| NUM\_INPUT\_PARAMS  | Number of input (IN) parameters for the stored procedure.                                              |
| NUM\_OUTPUT\_PARAMS | Number of output (OUT) parameters for the stored procedure.                                            |
| NUM\_RESULT\_SETS   | Number of result sets returned by the stored procedure.                                                |
| REMARKS             | Any comments about the stored procedure.                                                               |
| PROCEDURE\_TYPE     | Always returns *1*, indicating that the stored procedure does not return a return value.               |

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_result
===========

Returns a single column from a row in the result set

### 说明

<span class="type">mixed</span> <span
class="methodname">db2\_result</span> ( <span class="methodparam"><span
class="type">resource</span> `$stmt`</span> , <span
class="methodparam"><span class="type">mixed</span> `$column`</span> )

Use <span class="function">db2\_result</span> to return the value of a
specified column in the current row of a result set. You must call <span
class="function">db2\_fetch\_row</span> before calling <span
class="function">db2\_result</span> to set the location of the result
set pointer.

### 参数

`stmt`  
A valid *stmt* resource.

`column`  
Either an integer mapping to the 0-indexed field in the result set, or a
string matching the name of the column.

### 返回值

Returns the value of the requested field if the field exists in the
result set. Returns NULL if the field does not exist, and issues a
warning.

### 范例

**示例 \#1 A <span class="function">db2\_result</span> example**

The following example demonstrates how to iterate through a result set
with <span class="function">db2\_fetch\_row</span> and retrieve columns
from the result set with <span class="function">db2\_result</span>.

``` php
<?php
$sql = 'SELECT name, breed FROM animals WHERE weight < ?';
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, array(10));
while (db2_fetch_row($stmt)) {
    $name = db2_result($stmt, 0);
    $breed = db2_result($stmt, 'BREED');
    print "$name $breed";
}
?>
```

以上例程会输出：

    cat Pook
    gold fish Bubbles
    budgerigar Gizmo
    goat Rickety Ride

### 参见

-   <span class="function">db2\_fetch\_array</span>
-   <span class="function">db2\_fetch\_assoc</span>
-   <span class="function">db2\_fetch\_both</span>
-   <span class="function">db2\_fetch\_object</span>
-   <span class="function">db2\_fetch\_row</span>

db2\_rollback
=============

Rolls back a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_rollback</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

Rolls back an in-progress transaction on the specified connection
resource and begins a new transaction. PHP applications normally default
to AUTOCOMMIT mode, so <span class="function">db2\_rollback</span>
normally has no effect unless AUTOCOMMIT has been turned off for the
connection resource.

### 参数

`connection`  
A valid database connection resource variable as returned from <span
class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Rolling back a DELETE statement**

In the following example, we count the number of rows in a table, turn
off AUTOCOMMIT mode on a database connection, delete all of the rows in
the table and return the count of *0* to prove that the rows have been
removed. We then issue <span class="function">db2\_rollback</span> and
return the updated count of rows in the table to show that the number is
the same as before we issued the DELETE statement. The return to the
original state of the table demonstrates that the roll back of the
transaction succeeded.

``` php
<?php
$conn = db2_connect($database, $user, $password);

if ($conn) {
    $stmt = db2_exec($conn, "SELECT count(*) FROM animals");
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";
    
    // Turn AUTOCOMMIT off
    db2_autocommit($conn, DB2_AUTOCOMMIT_OFF);
   
    // Delete all rows from ANIMALS
    db2_exec($conn, "DELETE FROM animals");
    
    $stmt = db2_exec($conn, "SELECT count(*) FROM animals");
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";
    
    // Roll back the DELETE statement
    db2_rollback( $conn );
    
    $stmt = db2_exec( $conn, "SELECT count(*) FROM animals" );
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";
    db2_close($conn);
}
?>
```

以上例程会输出：

    7
    0
    7

### 参见

-   <span class="function">db2\_autocommit</span>
-   <span class="function">db2\_commit</span>

db2\_server\_info
=================

Returns an object with properties that describe the DB2 database server

### 说明

<span class="type"><span class="type">object</span><span
class="type">false</span></span> <span
class="methodname">db2\_server\_info</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

This function returns an object with read-only properties that return
information about the IBM DB2, Cloudscape, or Apache Derby database
server. The following table lists the database server properties:

<table>
<caption><strong>Database server properties</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Property name</th>
<th>Return type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DBMS_NAME</td>
<td>string</td>
<td>The name of the database server to which you are connected. For DB2 servers this is a combination of <em>DB2</em> followed by the operating system on which the database server is running.</td>
</tr>
<tr class="even">
<td>DBMS_VER</td>
<td>string</td>
<td>The version of the database server, in the form of a string "MM.mm.uuuu" where <var class="varname">MM</var> is the major version, <var class="varname">mm</var> is the minor version, and <var class="varname">uuuu</var> is the update. For example, "08.02.0001" represents major version 8, minor version 2, update 1.</td>
</tr>
<tr class="odd">
<td>DB_CODEPAGE</td>
<td>int</td>
<td>The code page of the database to which you are connected.</td>
</tr>
<tr class="even">
<td>DB_NAME</td>
<td>string</td>
<td>The name of the database to which you are connected.</td>
</tr>
<tr class="odd">
<td>DFT_ISOLATION</td>
<td>string</td>
<td><p>The default transaction isolation level supported by the server:</p>
<dl>
<dt>UR</dt>
<dd><p>Uncommitted read: changes are immediately visible by all concurrent transactions.</p>
</dd>
<dt>CS</dt>
<dd><p>Cursor stability: a row read by one transaction can be altered and committed by a second concurrent transaction.</p>
</dd>
<dt>RS</dt>
<dd><p>Read stability: a transaction can add or remove rows matching a search condition or a pending transaction.</p>
</dd>
<dt>RR</dt>
<dd><p>Repeatable read: data affected by pending transaction is not available to other transactions.</p>
</dd>
<dt>NC</dt>
<dd><p>No commit: any changes are visible at the end of a successful operation. Explicit commits and rollbacks are not allowed.</p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td>IDENTIFIER_QUOTE_CHAR</td>
<td>string</td>
<td>The character used to delimit an identifier.</td>
</tr>
<tr class="odd">
<td>INST_NAME</td>
<td>string</td>
<td>The instance on the database server that contains the database.</td>
</tr>
<tr class="even">
<td>ISOLATION_OPTION</td>
<td>array</td>
<td>An array of the isolation options supported by the database server. The isolation options are described in the DFT_ISOLATION property.</td>
</tr>
<tr class="odd">
<td>KEYWORDS</td>
<td>array</td>
<td>An array of the keywords reserved by the database server.</td>
</tr>
<tr class="even">
<td>LIKE_ESCAPE_CLAUSE</td>
<td>bool</td>
<td><strong><code>TRUE</code></strong> if the database server supports the use of <em>%</em> and <em>_</em> wildcard characters. <strong><code>FALSE</code></strong> if the database server does not support these wildcard characters.</td>
</tr>
<tr class="odd">
<td>MAX_COL_NAME_LEN</td>
<td>int</td>
<td>Maximum length of a column name supported by the database server, expressed in bytes.</td>
</tr>
<tr class="even">
<td>MAX_IDENTIFIER_LEN</td>
<td>int</td>
<td>Maximum length of an SQL identifier supported by the database server, expressed in characters.</td>
</tr>
<tr class="odd">
<td>MAX_INDEX_SIZE</td>
<td>int</td>
<td>Maximum size of columns combined in an index supported by the database server, expressed in bytes.</td>
</tr>
<tr class="even">
<td>MAX_PROC_NAME_LEN</td>
<td>int</td>
<td>Maximum length of a procedure name supported by the database server, expressed in bytes.</td>
</tr>
<tr class="odd">
<td>MAX_ROW_SIZE</td>
<td>int</td>
<td>Maximum length of a row in a base table supported by the database server, expressed in bytes.</td>
</tr>
<tr class="even">
<td>MAX_SCHEMA_NAME_LEN</td>
<td>int</td>
<td>Maximum length of a schema name supported by the database server, expressed in bytes.</td>
</tr>
<tr class="odd">
<td>MAX_STATEMENT_LEN</td>
<td>int</td>
<td>Maximum length of an SQL statement supported by the database server, expressed in bytes.</td>
</tr>
<tr class="even">
<td>MAX_TABLE_NAME_LEN</td>
<td>int</td>
<td>Maximum length of a table name supported by the database server, expressed in bytes.</td>
</tr>
<tr class="odd">
<td>NON_NULLABLE_COLUMNS</td>
<td>bool</td>
<td><strong><code>TRUE</code></strong> if the database server supports columns that can be defined as NOT NULL, <strong><code>FALSE</code></strong> if the database server does not support columns defined as NOT NULL.</td>
</tr>
<tr class="even">
<td>PROCEDURES</td>
<td>bool</td>
<td><strong><code>TRUE</code></strong> if the database server supports the use of the CALL statement to call stored procedures, <strong><code>FALSE</code></strong> if the database server does not support the CALL statement.</td>
</tr>
<tr class="odd">
<td>SPECIAL_CHARS</td>
<td>string</td>
<td>A string containing all of the characters other than a-Z, 0-9, and underscore that can be used in an identifier name.</td>
</tr>
<tr class="even">
<td>SQL_CONFORMANCE</td>
<td>string</td>
<td><p>The level of conformance to the ANSI/ISO SQL-92 specification offered by the database server:</p>
<dl>
<dt>ENTRY</dt>
<dd><p>Entry-level SQL-92 compliance.</p>
</dd>
<dt>FIPS127</dt>
<dd><p>FIPS-127-2 transitional compliance.</p>
</dd>
<dt>FULL</dt>
<dd><p>Full level SQL-92 compliance.</p>
</dd>
<dt>INTERMEDIATE</dt>
<dd><p>Intermediate level SQL-92 compliance.</p>
</dd>
</dl></td>
</tr>
</tbody>
</table>

### 参数

`connection`  
Specifies an active DB2 client connection.

### 返回值

Returns an object on a successful call. Returns **`FALSE`** on failure.

### 范例

**示例 \#1 A <span class="function">db2\_server\_info</span> example**

To retrieve information about the server, you must pass a valid database
connection resource to <span class="function">db2\_server\_info</span>.

``` php
<?php

$conn = db2_connect('sample', 'db2inst1', 'ibmdb2');

$server = db2_server_info( $conn );

if ($server) {
    echo "DBMS_NAME: ";                 var_dump( $server->DBMS_NAME );
    echo "DBMS_VER: ";                  var_dump( $server->DBMS_VER );
    echo "DB_CODEPAGE: ";               var_dump( $server->DB_CODEPAGE );
    echo "DB_NAME: ";                   var_dump( $server->DB_NAME );
    echo "INST_NAME: ";                 var_dump( $server->INST_NAME );
    echo "SPECIAL_CHARS: ";             var_dump( $server->SPECIAL_CHARS );
    echo "KEYWORDS: ";                  var_dump( sizeof($server->KEYWORDS) );
    echo "DFT_ISOLATION: ";             var_dump( $server->DFT_ISOLATION );
    echo "ISOLATION_OPTION: ";
    $il = '';
    foreach( $server->ISOLATION_OPTION as $opt )
    {
       $il .= $opt." ";
    }
    var_dump( $il );
    echo "SQL_CONFORMANCE: ";           var_dump( $server->SQL_CONFORMANCE );
    echo "PROCEDURES: ";                var_dump( $server->PROCEDURES );
    echo "IDENTIFIER_QUOTE_CHAR: ";     var_dump( $server->IDENTIFIER_QUOTE_CHAR );
    echo "LIKE_ESCAPE_CLAUSE: ";        var_dump( $server->LIKE_ESCAPE_CLAUSE );
    echo "MAX_COL_NAME_LEN: ";          var_dump( $server->MAX_COL_NAME_LEN );
    echo "MAX_ROW_SIZE: ";              var_dump( $server->MAX_ROW_SIZE );
    echo "MAX_IDENTIFIER_LEN: ";        var_dump( $server->MAX_IDENTIFIER_LEN );
    echo "MAX_INDEX_SIZE: ";            var_dump( $server->MAX_INDEX_SIZE );
    echo "MAX_PROC_NAME_LEN: ";         var_dump( $server->MAX_PROC_NAME_LEN );
    echo "MAX_SCHEMA_NAME_LEN: ";       var_dump( $server->MAX_SCHEMA_NAME_LEN );
    echo "MAX_STATEMENT_LEN: ";         var_dump( $server->MAX_STATEMENT_LEN );
    echo "MAX_TABLE_NAME_LEN: ";        var_dump( $server->MAX_TABLE_NAME_LEN );
    echo "NON_NULLABLE_COLUMNS: ";      var_dump( $server->NON_NULLABLE_COLUMNS );

    db2_close($conn);
}
?>
```

以上例程会输出：

    DBMS_NAME: string(9) "DB2/LINUX"
    DBMS_VER: string(10) "08.02.0000"
    DB_CODEPAGE: int(1208)
    DB_NAME: string(6) "SAMPLE"
    INST_NAME: string(8) "db2inst1"
    SPECIAL_CHARS: string(2) "@#"
    KEYWORDS: int(179)
    DFT_ISOLATION: string(2) "CS"
    ISOLATION_OPTION: string(12) "UR CS RS RR "
    SQL_CONFORMANCE: string(7) "FIPS127"
    PROCEDURES: bool(true)
    IDENTIFIER_QUOTE_CHAR: string(1) """
    LIKE_ESCAPE_CLAUSE: bool(true)
    MAX_COL_NAME_LEN: int(30)
    MAX_ROW_SIZE: int(32677)
    MAX_IDENTIFIER_LEN: int(18)
    MAX_INDEX_SIZE: int(1024)
    MAX_PROC_NAME_LEN: int(128)
    MAX_SCHEMA_NAME_LEN: int(30)
    MAX_STATEMENT_LEN: int(2097152)
    MAX_TABLE_NAME_LEN: int(128)
    NON_NULLABLE_COLUMNS: bool(true)

### 参见

-   <span class="function">db2\_client\_info</span>

db2\_set\_option
================

Set options for connection or statement resources

### 说明

<span class="type">bool</span> <span
class="methodname">db2\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$resource`</span> , <span class="methodparam"><span
class="type">array</span> `$options`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> )

Sets options for a statement resource or a connection resource. You
cannot set options for result set resources.

### 参数

`resource`  
A valid statement resource as returned from <span
class="function">db2\_prepare</span> or a valid connection resource as
returned from <span class="function">db2\_connect</span> or <span
class="function">db2\_pconnect</span>.

`options`  
An associative array containing valid statement or connection options.
This parameter can be used to change autocommit values, cursor types
(scrollable or forward), and to specify the case of the column names
(lower, upper, or natural) that will appear in a result set.

`autocommit`  
Passing *DB2\_AUTOCOMMIT\_ON* turns autocommit on for the specified
connection resource.

Passing *DB2\_AUTOCOMMIT\_OFF* turns autocommit off for the specified
connection resource.

`cursor`  
Passing *DB2\_FORWARD\_ONLY* specifies a forward-only cursor for a
statement resource. This is the default cursor type, and is supported by
all database servers.

Passing *DB2\_SCROLLABLE* specifies a scrollable cursor for a statement
resource. Scrollable cursors enable result set rows to be accessed in
non-sequential order, but are only supported by IBM DB2 Universal
Database databases.

`binmode`  
Passing *DB2\_BINARY* specifies that binary data will be returned as is.
This is the default mode. This is the equivalent of setting
*ibm\_db2.binmode=1* in `php.ini`.

Passing *DB2\_CONVERT* specifies that binary data will be converted to
hexadecimal encoding, and will be returned as such. This is the
equivalent of setting *ibm\_db2.binmode=2* in `php.ini`.

Passing *DB2\_PASSTHRU* specifies that binary data will be converted to
**`NULL`**. This is the equivalent of setting *ibm\_db2.binmode=3* in
`php.ini`.

`db2_attr_case`  
Passing *DB2\_CASE\_LOWER* specifies that column names of the result set
are returned in lower case.

Passing *DB2\_CASE\_UPPER* specifies that column names of the result set
are returned in upper case.

Passing *DB2\_CASE\_NATURAL* specifies that column names of the result
set are returned in natural case.

`deferred_prepare`  
Passing *DB2\_DEFERRED\_PREPARE\_ON* turns deferred prepare on for the
specified statement resource.

Passing *DB2\_DEFERRED\_PREPARE\_OFF* turns deferred prepare off for the
specified statement resource.

The following new i5/OS options are available in ibm\_db2 version 1.5.1
and later. These options apply only when running PHP and ibm\_db2
natively on i5 systems.

`i5_fetch_only`  
*DB2\_I5\_FETCH\_ON* - Cursors are read-only and cannot be used for
positioned updates or deletes. This is the default unless
*SQL\_ATTR\_FOR\_FETCH\_ONLY* environment has been set to *SQL\_FALSE*.

*DB2\_I5\_FETCH\_OFF* - Cursors can be used for positioned updates and
deletes.

The following new option is available in ibm\_db2 version 1.8.0 and
later.

`rowcount`  
*DB2\_ROWCOUNT\_PREFETCH\_ON* - Client can request the full row count
prior to fetching, which means that <span
class="function">db2\_num\_rows</span> returns the number of rows
selected even when a *ROLLFORWARD\_ONLY* cursor is used.

*DB2\_ROWCOUNT\_PREFETCH\_OFF* - Client cannot request the full row
count prior to fetching.

The following new options are available in ibm\_db2 version 1.7.0 and
later.

`trusted_user`  
To switch the user to a trusted user, pass the User ID (String) of the
trusted user as the value of this key. This option can be set on a
connection resource only. To use this option, trusted context must be
enabled on the connection resource.

`trusted_password`  
The password (String) that corresponds to the user specified by the
trusted\_user key.

The following new options are available in ibm\_db2 version 1.6.0 and
later. These options provide useful tracking information that can be
accessed during execution with <span
class="function">db2\_get\_option</span>.

> **Note**:
>
> When the value in each option is being set, some servers might not
> handle the entire length provided and might truncate the value.
>
> To ensure that the data specified in each option is converted
> correctly when transmitted to a host system, use only the characters A
> through Z, 0 through 9, and the underscore (\_) or period (.).

`userid`  
*SQL\_ATTR\_INFO\_USERID* - A pointer to a null-terminated character
string used to identify the client user ID sent to the host database
server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 16
> characters. This user-id is not to be confused with the authentication
> user-id, it is for identification purposes only and is not used for
> any authorization.

`acctstr`  
*SQL\_ATTR\_INFO\_ACCTSTR* - A pointer to a null-terminated character
string used to identify the client accounting string sent to the host
database server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 200
> characters.

`applname`  
*SQL\_ATTR\_INFO\_APPLNAME* - A pointer to a null-terminated character
string used to identify the client application name sent to the host
database server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 32
> characters.

`wrkstnname`  
*SQL\_ATTR\_INFO\_WRKSTNNAME* - A pointer to a null-terminated character
string used to identify the client workstation name sent to the host
database server when using DB2 Connect.

> **Note**:
>
> DB2 for z/OS and OS/390 servers support up to a length of 18
> characters.

`type`  
An integer value that specifies the type of resource that was passed
into the function. The type of resource and this value must correspond.

Passing *1* as the value specifies that a connection resource has been
passed into the function.

Passing any integer not equal to *1* as the value specifies that a
statement resource has been passed into the function.

The following table specifies which options are compatible with the
available resource types:

**Resource-Parameter Matrix**

Key

Value

Resource Type

 

 

Connection

Statement

Result Set

autocommit

*DB2\_AUTOCOMMIT\_ON*

X

\-

\-

autocommit

*DB2\_AUTOCOMMIT\_OFF*

X

\-

\-

cursor

*DB2\_SCROLLABLE*

\-

X

\-

cursor

*DB2\_FORWARD\_ONLY*

\-

X

\-

binmode

*DB2\_BINARY*

X

X

\-

binmode

*DB2\_CONVERT*

X

X

\-

binmode

*DB2\_PASSTHRU*

X

X

\-

db2\_attr\_case

*DB2\_CASE\_LOWER*

X

X

\-

db2\_attr\_case

*DB2\_CASE\_UPPER*

X

X

\-

db2\_attr\_case

*DB2\_CASE\_NATURAL*

X

X

\-

deferred\_prepare

*DB2\_DEFERRED\_PREPARE\_ON*

\-

X

\-

deferred\_prepare

*DB2\_DEFERRED\_PREPARE\_OFF*

\-

X

\-

i5\_fetch\_only

*DB2\_I5\_FETCH\_ON*

\-

X

\-

i5\_fetch\_only

*DB2\_I5\_FETCH\_OFF*

\-

X

\-

rowcount

*DB2\_ROWCOUNT\_PREFETCH\_ON*

\-

X

\-

rowcount

*DB2\_ROWCOUNT\_PREFETCH\_OFF*

\-

X

\-

trusted\_user

*\<USER NAME\> (String)*

X

\-

\-

trusted\_password

*\<PASSWORD\> (String)*

X

\-

\-

userid

*SQL\_ATTR\_INFO\_USERID*

X

X

\-

acctstr

*SQL\_ATTR\_INFO\_ACCTSTR*

X

X

\-

applname

*SQL\_ATTR\_INFO\_APPLNAME*

X

X

\-

wrkstnname

*SQL\_ATTR\_INFO\_WRKSTNNAME*

X

X

\-

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Setting one parameter with a connection resource**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('autocommit' => DB2_AUTOCOMMIT_ON);

/* Call the function using the correct resource, options array, and type values */
$result = db2_set_option($conn, $options, 1);

/* Check if all options could be set correctly */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

以上例程会输出：

    Options Set Successfully

**示例 \#2 Setting multiple parameters with a connection resource**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF, 
                    'binmode' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Call the function using the correct resource, options array, and type values */
$result = db2_set_option($conn, $options, 1);

/* Check if all options could be set correctly */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

以上例程会输出：

    Options Set Successfully

**示例 \#3 Setting multiple parameters with an invalid key**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF, 
             'MY_INVALID_KEY' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Call the function using the correct resource, options array, and type values */
$result = db2_set_option($conn, $options, 1);

/* Check if all options could be set correctly */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

以上例程会输出：

    Could Not Set Options

**示例 \#4 Setting multiple parameters with an invalid value**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF, 
                    'binmode' => 'INVALID_VALUE',
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Call the function using the correct resource, options array, and type values */
$result = db2_set_option($conn, $options, 1);

/* Check if all options could be set correctly */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

以上例程会输出：

    Could Not Set Options

**示例 \#5 Setting multiple parameters with a connection resource and
the wrong type**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF, 
                    'binmode' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

/* Call the function using the correct resource, options array, and the wrong type value */
$result = db2_set_option($conn, $options, 2);

/* Check if all options could be set correctly */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

以上例程会输出：

    Could Not Set Options

**示例 \#6 Setting multiple parameters with the wrong resource**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('autocommit' => DB2_AUTOCOMMIT_OFF, 
                    'binmode' => DB2_PASSTHRU,
              'db2_attr_case' => DB2_CASE_UPPER,
                     'cursor' => DB2_SCROLLABLE);

$stmt = db2_prepare($conn, 'SELECT * FROM EMPLOYEE');

/* Call the function using the wrong resource, and the correct options array, and type values */
$result = db2_set_option($stmt, $options, 1);

/* Check if all options could be set correctly */
if($result)
{
  echo 'Options Set Successfully';
}
else
{
  echo 'Could Not Set Options';
}
?>
```

以上例程会输出：

    Could Not Set Options

**示例 \#7 Putting it all together**

``` php
<?php
/* Database Connection Parameters */
$database = 'SAMPLE';
$hostname = 'localhost';
$port = 50000;
$protocol = 'TCPIP';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Connection String */
$conn_string = "DRIVER={IBM DB2 ODBC DRIVER};DATABASE=$database;";
$conn_string .= "HOSTNAME=$hostname;PORT=$port;PROTOCOL=$protocol;";
$conn_string .= "UID=$username;PWD=$password;";

/* Obtain Connection Resource */
$conn = db2_connect($conn_string, '', '');

/* Create the associative options array with valid key-value pairs */
$options = array('db2_attr_case' => DB2_CASE_LOWER,
                        'cursor' => DB2_SCROLLABLE);

$stmt = db2_prepare($conn, 'SELECT * FROM EMPLOYEE WHERE EMPNO = ? OR EMPNO = ?');

/* Call the function using the correct resource, options array, and type values */
$option_result = db2_set_option($stmt, $options, 2);
$result = db2_execute($stmt, array('000130', '000140'));

/* Get Row 2 before Row 1 since Scrollable Cursor */
print_r(db2_fetch_assoc($stmt, 2));
print '<br /><br />';
print_r(db2_fetch_assoc($stmt, 1));

?>
```

以上例程会输出：

    Array
    (
        [empno] => 000140
        [firstnme] => HEATHER
        [midinit] => A
        [lastname] => NICHOLLS
        [workdept] => C01
        [phoneno] => 1793
        [hiredate] => 1976-12-15
        [job] => ANALYST
        [edlevel] => 18
        [sex] => F
        [birthdate] => 1946-01-19
        [salary] => 28420.00
        [bonus] => 600.00
        [comm] => 2274.00
    )

    Array
    (
        [empno] => 000130
        [firstnme] => DELORES
        [midinit] => M
        [lastname] => QUINTANA
        [workdept] => C01
        [phoneno] => 4578
        [hiredate] => 1971-07-28
        [job] => ANALYST
        [edlevel] => 16
        [sex] => F
        [birthdate] => 1925-09-15
        [salary] => 23800.00
        [bonus] => 500.00
        [comm] => 1904.00
    )

**示例 \#8 i5/OS cursors are read-only**

``` php
<?php
  $conn = db2_connect("", "", "", array("i5_lib"=>"nobody"));
  $stmt = db2_prepare($conn, 'select * from names where first = ?');
  $name = "first2";
  db2_bind_param($stmt, 1, "name", DB2_PARAM_IN);
  $options = array("i5_fetch_only"=>DB2_I5_FETCH_ON);
  db2_set_option($stmt,$options,0);
  if (db2_execute($stmt)) {
    while ($row = db2_fetch_array($stmt)) {
      echo "{$row[0]} {$row[1]}";
    }
  }
?>
```

以上例程会输出：

    first2 last2

### 参见

-   <span class="function">db2\_connect</span>
-   <span class="function">db2\_pconnect</span>
-   <span class="function">db2\_exec</span>
-   <span class="function">db2\_prepare</span>
-   <span class="function">db2\_cursor\_type</span>

db2\_special\_columns
=====================

Returns a result set listing the unique row identifier columns for a
table

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_special\_columns</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> ,
<span class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">int</span> `$scope`</span> )

Returns a result set listing the unique row identifier columns for a
table.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables.

`table_name`  
The name of the table.

`scope`  
Integer value representing the minimum duration for which the unique row
identifier is valid. This can be one of the following values:

| Integer value | SQL constant            | Description                                                             |
|---------------|-------------------------|-------------------------------------------------------------------------|
| 0             | SQL\_SCOPE\_CURROW      | Row identifier is valid only while the cursor is positioned on the row. |
| 1             | SQL\_SCOPE\_TRANSACTION | Row identifier is valid for the duration of the transaction.            |
| 2             | SQL\_SCOPE\_SESSION     | Row identifier is valid for the duration of the connection.             |

### 返回值

Returns a statement resource with a result set containing rows with
unique row identifier information for a table. The rows are composed of
the following columns:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SCOPE</td>
<td><table>
<thead>
<tr class="header">
<th>Integer value</th>
<th>SQL constant</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>SQL_SCOPE_CURROW</td>
<td>Row identifier is valid only while the cursor is positioned on the row.</td>
</tr>
<tr class="even">
<td>1</td>
<td>SQL_SCOPE_TRANSACTION</td>
<td>Row identifier is valid for the duration of the transaction.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>SQL_SCOPE_SESSION</td>
<td>Row identifier is valid for the duration of the connection.</td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="even">
<td>COLUMN_NAME</td>
<td>Name of the unique column.</td>
</tr>
<tr class="odd">
<td>DATA_TYPE</td>
<td>SQL data type for the column.</td>
</tr>
<tr class="even">
<td>TYPE_NAME</td>
<td>Character string representation of the SQL data type for the column.</td>
</tr>
<tr class="odd">
<td>COLUMN_SIZE</td>
<td>An integer value representing the size of the column.</td>
</tr>
<tr class="even">
<td>BUFFER_LENGTH</td>
<td>Maximum number of bytes necessary to store data from this column.</td>
</tr>
<tr class="odd">
<td>DECIMAL_DIGITS</td>
<td>The scale of the column, or <strong><code>NULL</code></strong> where scale is not applicable.</td>
</tr>
<tr class="even">
<td>NUM_PREC_RADIX</td>
<td>An integer value of either <em>10</em> (representing an exact numeric data type), <em>2</em> (representing an approximate numeric data type), or <strong><code>NULL</code></strong> (representing a data type for which radix is not applicable).</td>
</tr>
<tr class="odd">
<td>PSEUDO_COLUMN</td>
<td>Always returns 1.</td>
</tr>
</tbody>
</table>

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_statistics
===============

Returns a result set listing the index and statistics for a table

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_statistics</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> ,
<span class="methodparam"><span class="type">string</span>
`$table-name`</span> , <span class="methodparam"><span
class="type">bool</span> `$unique`</span> )

Returns a result set listing the index and statistics for a table.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema that contains the targeted table. If this parameter is
**`NULL`**, the statistics and indexes are returned for the schema of
the current user.

`table_name`  
The name of the table.

`unique`  
An integer value representing the type of index information to return.

`0`  
Return only the information for unique indexes on the table.

`1`  
Return the information for all indexes on the table.

### 返回值

Returns a statement resource with a result set containing rows
describing the statistics and indexes for the base tables matching the
specified parameters. The rows are composed of the following columns:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TABLE_CAT</td>
<td>The catalog that contains the table. The value is <strong><code>NULL</code></strong> if this table does not have catalogs.</td>
</tr>
<tr class="even">
<td>TABLE_SCHEM</td>
<td>Name of the schema that contains the table.</td>
</tr>
<tr class="odd">
<td>TABLE_NAME</td>
<td>Name of the table.</td>
</tr>
<tr class="even">
<td>NON_UNIQUE</td>
<td><p>An integer value representing whether the index prohibits unique values, or whether the row represents statistics on the table itself:</p>
<table>
<thead>
<tr class="header">
<th>Return value</th>
<th>Parameter type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0 (SQL_FALSE)</td>
<td>The index allows duplicate values.</td>
</tr>
<tr class="even">
<td>1 (SQL_TRUE)</td>
<td>The index values must be unique.</td>
</tr>
<tr class="odd">
<td><strong><code>NULL</code></strong></td>
<td>This row is statistics information for the table itself.</td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td>INDEX_QUALIFIER</td>
<td>A string value representing the qualifier that would have to be prepended to INDEX_NAME to fully qualify the index.</td>
</tr>
<tr class="even">
<td>INDEX_NAME</td>
<td>A string representing the name of the index.</td>
</tr>
<tr class="odd">
<td>TYPE</td>
<td><p>An integer value representing the type of information contained in this row of the result set:</p>
<table>
<thead>
<tr class="header">
<th>Return value</th>
<th>Parameter type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0 (SQL_TABLE_STAT)</td>
<td>The row contains statistics about the table itself.</td>
</tr>
<tr class="even">
<td>1 (SQL_INDEX_CLUSTERED)</td>
<td>The row contains information about a clustered index.</td>
</tr>
<tr class="odd">
<td>2 (SQL_INDEX_HASH)</td>
<td>The row contains information about a hashed index.</td>
</tr>
<tr class="even">
<td>3 (SQL_INDEX_OTHER)</td>
<td>The row contains information about a type of index that is neither clustered nor hashed.</td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="even">
<td>ORDINAL_POSITION</td>
<td>The 1-indexed position of the column in the index. <strong><code>NULL</code></strong> if the row contains statistics information about the table itself.</td>
</tr>
<tr class="odd">
<td>COLUMN_NAME</td>
<td>The name of the column in the index. <strong><code>NULL</code></strong> if the row contains statistics information about the table itself.</td>
</tr>
<tr class="even">
<td>ASC_OR_DESC</td>
<td><em>A</em> if the column is sorted in ascending order, <em>D</em> if the column is sorted in descending order, <strong><code>NULL</code></strong> if the row contains statistics information about the table itself.</td>
</tr>
<tr class="odd">
<td>CARDINALITY</td>
<td><p>If the row contains information about an index, this column contains an integer value representing the number of unique values in the index.</p>
<p>If the row contains information about the table itself, this column contains an integer value representing the number of rows in the table.</p></td>
</tr>
<tr class="even">
<td>PAGES</td>
<td><p>If the row contains information about an index, this column contains an integer value representing the number of pages used to store the index.</p>
<p>If the row contains information about the table itself, this column contains an integer value representing the number of pages used to store the table.</p></td>
</tr>
<tr class="odd">
<td>FILTER_CONDITION</td>
<td>Always returns <strong><code>NULL</code></strong>.</td>
</tr>
</tbody>
</table>

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_table\_privileges</span>
-   <span class="function">db2\_tables</span>

db2\_stmt\_error
================

Returns a string containing the SQLSTATE returned by an SQL statement

### 说明

<span class="type">string</span> <span
class="methodname">db2\_stmt\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> \]
)

Returns a string containing the SQLSTATE value returned by an SQL
statement.

If you do not pass a statement resource as an argument to <span
class="function">db2\_stmt\_error</span>, the driver returns the
SQLSTATE value associated with the last attempt to return a statement
resource, for example, from <span class="function">db2\_prepare</span>
or <span class="function">db2\_exec</span>.

To learn what the SQLSTATE value means, you can issue the following
command at a DB2 Command Line Processor prompt:
**`db2 '? sqlstate-value`'**. You can also call <span
class="function">db2\_stmt\_errormsg</span> to retrieve an explicit
error message and the associated SQLCODE value.

### 参数

`stmt`  
A valid statement resource.

### 返回值

Returns a string containing an SQLSTATE value.

### 参见

-   <span class="function">db2\_conn\_error</span>
-   <span class="function">db2\_conn\_errormsg</span>
-   <span class="function">db2\_stmt\_errormsg</span>

db2\_stmt\_errormsg
===================

Returns a string containing the last SQL statement error message

### 说明

<span class="type">string</span> <span
class="methodname">db2\_stmt\_errormsg</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> \]
)

Returns a string containing the last SQL statement error message.

If you do not pass a statement resource as an argument to <span
class="function">db2\_stmt\_errormsg</span>, the driver returns the
error message associated with the last attempt to return a statement
resource, for example, from <span class="function">db2\_prepare</span>
or <span class="function">db2\_exec</span>.

### 参数

`stmt`  
A valid statement resource.

### 返回值

Returns a string containing the error message and SQLCODE value for the
last error that occurred issuing an SQL statement.

### 参见

-   <span class="function">db2\_conn\_error</span>
-   <span class="function">db2\_conn\_errormsg</span>
-   <span class="function">db2\_stmt\_error</span>

db2\_table\_privileges
======================

Returns a result set listing the tables and associated privileges in a
database

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_table\_privileges</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \[, <span class="methodparam"><span
class="type">string</span> `$qualifier`</span> \[, <span
class="methodparam"><span class="type">string</span> `$schema`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$table_name`</span> \]\]\] )

Returns a result set listing the tables and associated privileges in a
database.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables. This parameter accepts a search
pattern containing *\_* and *%* as wildcards.

`table_name`  
The name of the table. This parameter accepts a search pattern
containing *\_* and *%* as wildcards.

### 返回值

Returns a statement resource with a result set containing rows
describing the privileges for the tables that match the specified
parameters. The rows are composed of the following columns:

| Column name   | Description                                                                                                                   |
|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| TABLE\_CAT    | The catalog that contains the table. The value is **`NULL`** if this table does not have catalogs.                            |
| TABLE\_SCHEM  | Name of the schema that contains the table.                                                                                   |
| TABLE\_NAME   | Name of the table.                                                                                                            |
| GRANTOR       | Authorization ID of the user who granted the privilege.                                                                       |
| GRANTEE       | Authorization ID of the user to whom the privilege was granted.                                                               |
| PRIVILEGE     | The privilege that has been granted. This can be one of ALTER, CONTROL, DELETE, INDEX, INSERT, REFERENCES, SELECT, or UPDATE. |
| IS\_GRANTABLE | A string value of "YES" or "NO" indicating whether the grantee can grant the privilege to other users.                        |

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_tables</span>

db2\_tables
===========

Returns a result set listing the tables and associated metadata in a
database

### 说明

<span class="type">resource</span> <span
class="methodname">db2\_tables</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> \[, <span
class="methodparam"><span class="type">string</span> `$qualifier`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$schema`</span> \[, <span class="methodparam"><span
class="type">string</span> `$table-name`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$table-type`</span> \]\]\]\] )

Returns a result set listing the tables and associated metadata in a
database.

### 参数

`connection`  
A valid connection to an IBM DB2, Cloudscape, or Apache Derby database.

`qualifier`  
A qualifier for DB2 databases running on OS/390 or z/OS servers. For
other databases, pass **`NULL`** or an empty string.

`schema`  
The schema which contains the tables. This parameter accepts a search
pattern containing *\_* and *%* as wildcards.

`table-name`  
The name of the table. This parameter accepts a search pattern
containing *\_* and *%* as wildcards.

`table-type`  
A list of comma-delimited table type identifiers. To match all table
types, pass **`NULL`** or an empty string. Valid table type identifiers
include: ALIAS, HIERARCHY TABLE, INOPERATIVE VIEW, NICKNAME,
MATERIALIZED QUERY TABLE, SYSTEM TABLE, TABLE, TYPED TABLE, TYPED VIEW,
and VIEW.

### 返回值

Returns a statement resource with a result set containing rows
describing the tables that match the specified parameters. The rows are
composed of the following columns:

| Column name  | Description                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| TABLE\_CAT   | The catalog that contains the table. The value is **`NULL`** if this table does not have catalogs. |
| TABLE\_SCHEM | Name of the schema that contains the table.                                                        |
| TABLE\_NAME  | Name of the table.                                                                                 |
| TABLE\_TYPE  | Table type identifier for the table.                                                               |
| REMARKS      | Description of the table.                                                                          |

### 参见

-   <span class="function">db2\_column\_privileges</span>
-   <span class="function">db2\_columns</span>
-   <span class="function">db2\_foreign\_keys</span>
-   <span class="function">db2\_primary\_keys</span>
-   <span class="function">db2\_procedure\_columns</span>
-   <span class="function">db2\_procedures</span>
-   <span class="function">db2\_special\_columns</span>
-   <span class="function">db2\_statistics</span>
-   <span class="function">db2\_table\_privileges</span>

**目录**

-   [db2\_autocommit](/book/ibm-db2.html#db2_autocommit) — Returns or
    sets the AUTOCOMMIT state for a database connection
-   [db2\_bind\_param](/book/ibm-db2.html#db2_bind_param) — Binds a PHP
    variable to an SQL statement parameter
-   [db2\_client\_info](/book/ibm-db2.html#db2_client_info) — Returns an
    object with properties that describe the DB2 database client
-   [db2\_close](/book/ibm-db2.html#db2_close) — Closes a database
    connection
-   [db2\_column\_privileges](/book/ibm-db2.html#db2_column_privileges)
    — Returns a result set listing the columns and associated privileges
    for a table
-   [db2\_columns](/book/ibm-db2.html#db2_columns) — Returns a result
    set listing the columns and associated metadata for a table
-   [db2\_commit](/book/ibm-db2.html#db2_commit) — Commits a transaction
-   [db2\_conn\_error](/book/ibm-db2.html#db2_conn_error) — Returns a
    string containing the SQLSTATE returned by the last connection
    attempt
-   [db2\_conn\_errormsg](/book/ibm-db2.html#db2_conn_errormsg) —
    Returns the last connection error message and SQLCODE value
-   [db2\_connect](/book/ibm-db2.html#db2_connect) — Returns a
    connection to a database
-   [db2\_cursor\_type](/book/ibm-db2.html#db2_cursor_type) — Returns
    the cursor type used by a statement resource
-   [db2\_escape\_string](/book/ibm-db2.html#db2_escape_string) — Used
    to escape certain characters
-   [db2\_exec](/book/ibm-db2.html#db2_exec) — Executes an SQL statement
    directly
-   [db2\_execute](/book/ibm-db2.html#db2_execute) — Executes a prepared
    SQL statement
-   [db2\_fetch\_array](/book/ibm-db2.html#db2_fetch_array) — Returns an
    array, indexed by column position, representing a row in a result
    set
-   [db2\_fetch\_assoc](/book/ibm-db2.html#db2_fetch_assoc) — Returns an
    array, indexed by column name, representing a row in a result set
-   [db2\_fetch\_both](/book/ibm-db2.html#db2_fetch_both) — Returns an
    array, indexed by both column name and position, representing a row
    in a result set
-   [db2\_fetch\_object](/book/ibm-db2.html#db2_fetch_object) — Returns
    an object with properties representing columns in the fetched row
-   [db2\_fetch\_row](/book/ibm-db2.html#db2_fetch_row) — Sets the
    result set pointer to the next row or requested row
-   [db2\_field\_display\_size](/book/ibm-db2.html#db2_field_display_size)
    — Returns the maximum number of bytes required to display a column
-   [db2\_field\_name](/book/ibm-db2.html#db2_field_name) — Returns the
    name of the column in the result set
-   [db2\_field\_num](/book/ibm-db2.html#db2_field_num) — Returns the
    position of the named column in a result set
-   [db2\_field\_precision](/book/ibm-db2.html#db2_field_precision) —
    Returns the precision of the indicated column in a result set
-   [db2\_field\_scale](/book/ibm-db2.html#db2_field_scale) — Returns
    the scale of the indicated column in a result set
-   [db2\_field\_type](/book/ibm-db2.html#db2_field_type) — Returns the
    data type of the indicated column in a result set
-   [db2\_field\_width](/book/ibm-db2.html#db2_field_width) — Returns
    the width of the current value of the indicated column in a result
    set
-   [db2\_foreign\_keys](/book/ibm-db2.html#db2_foreign_keys) — Returns
    a result set listing the foreign keys for a table
-   [db2\_free\_result](/book/ibm-db2.html#db2_free_result) — Frees
    resources associated with a result set
-   [db2\_free\_stmt](/book/ibm-db2.html#db2_free_stmt) — Frees
    resources associated with the indicated statement resource
-   [db2\_get\_option](/book/ibm-db2.html#db2_get_option) — Retrieves an
    option value for a statement resource or a connection resource
-   [db2\_last\_insert\_id](/book/ibm-db2.html#db2_last_insert_id) —
    Returns the auto generated ID of the last insert query that
    successfully executed on this connection
-   [db2\_lob\_read](/book/ibm-db2.html#db2_lob_read) — Gets a user
    defined size of LOB files with each invocation
-   [db2\_next\_result](/book/ibm-db2.html#db2_next_result) — Requests
    the next result set from a stored procedure
-   [db2\_num\_fields](/book/ibm-db2.html#db2_num_fields) — Returns the
    number of fields contained in a result set
-   [db2\_num\_rows](/book/ibm-db2.html#db2_num_rows) — Returns the
    number of rows affected by an SQL statement
-   [db2\_pclose](/book/ibm-db2.html#db2_pclose) — Closes a persistent
    database connection
-   [db2\_pconnect](/book/ibm-db2.html#db2_pconnect) — Returns a
    persistent connection to a database
-   [db2\_prepare](/book/ibm-db2.html#db2_prepare) — Prepares an SQL
    statement to be executed
-   [db2\_primary\_keys](/book/ibm-db2.html#db2_primary_keys) — Returns
    a result set listing primary keys for a table
-   [db2\_procedure\_columns](/book/ibm-db2.html#db2_procedure_columns)
    — Returns a result set listing stored procedure parameters
-   [db2\_procedures](/book/ibm-db2.html#db2_procedures) — Returns a
    result set listing the stored procedures registered in a database
-   [db2\_result](/book/ibm-db2.html#db2_result) — Returns a single
    column from a row in the result set
-   [db2\_rollback](/book/ibm-db2.html#db2_rollback) — Rolls back a
    transaction
-   [db2\_server\_info](/book/ibm-db2.html#db2_server_info) — Returns an
    object with properties that describe the DB2 database server
-   [db2\_set\_option](/book/ibm-db2.html#db2_set_option) — Set options
    for connection or statement resources
-   [db2\_special\_columns](/book/ibm-db2.html#db2_special_columns) —
    Returns a result set listing the unique row identifier columns for a
    table
-   [db2\_statistics](/book/ibm-db2.html#db2_statistics) — Returns a
    result set listing the index and statistics for a table
-   [db2\_stmt\_error](/book/ibm-db2.html#db2_stmt_error) — Returns a
    string containing the SQLSTATE returned by an SQL statement
-   [db2\_stmt\_errormsg](/book/ibm-db2.html#db2_stmt_errormsg) —
    Returns a string containing the last SQL statement error message
-   [db2\_table\_privileges](/book/ibm-db2.html#db2_table_privileges) —
    Returns a result set listing the tables and associated privileges in
    a database
-   [db2\_tables](/book/ibm-db2.html#db2_tables) — Returns a result set
    listing the tables and associated metadata in a database
