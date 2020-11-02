MaxDB
=====

**目录**

-   [简介](/book/maxdb.html#简介)
-   [安装／配置](/book/maxdb.html#安装／配置)
    -   [需求](/book/maxdb.html#需求)
    -   [安装](/book/maxdb.html#安装)
    -   [运行时配置](/book/maxdb.html#运行时配置)
    -   [资源类型](/book/maxdb.html#资源类型)
-   [预定义常量](/book/maxdb.html#预定义常量)
-   [范例](/book/maxdb.html#范例)
    -   [Basic usage](/book/maxdb.html#Basic%20usage)
-   [MaxDB 函数](/book/maxdb.html#MaxDB%20函数)
    -   [maxdb\_affected\_rows](/book/maxdb.html#maxdb_affected_rows) —
        Gets the number of affected rows in a previous MaxDB operation
    -   [maxdb\_autocommit](/book/maxdb.html#maxdb_autocommit) — Turns
        on or off auto-commiting database modifications
    -   [maxdb\_bind\_param](/book/maxdb.html#maxdb_bind_param) — 别名
        maxdb\_stmt\_bind\_param
    -   [maxdb\_bind\_result](/book/maxdb.html#maxdb_bind_result) — 别名
        maxdb\_stmt\_bind\_result
    -   [maxdb\_change\_user](/book/maxdb.html#maxdb_change_user) —
        Changes the user of the specified database connection
    -   [maxdb\_character\_set\_name](/book/maxdb.html#maxdb_character_set_name)
        — Returns the default character set for the database connection
    -   [maxdb\_client\_encoding](/book/maxdb.html#maxdb_client_encoding)
        — 别名 maxdb\_character\_set\_name
    -   [maxdb\_close\_long\_data](/book/maxdb.html#maxdb_close_long_data)
        — 别名 maxdb\_stmt\_close\_long\_data
    -   [maxdb\_close](/book/maxdb.html#maxdb_close) — Closes a
        previously opened database connection
    -   [maxdb\_commit](/book/maxdb.html#maxdb_commit) — Commits the
        current transaction
    -   [maxdb\_connect\_errno](/book/maxdb.html#maxdb_connect_errno) —
        Returns the error code from last connect call
    -   [maxdb\_connect\_error](/book/maxdb.html#maxdb_connect_error) —
        Returns a string description of the last connect error
    -   [maxdb\_connect](/book/maxdb.html#maxdb_connect) — Open a new
        connection to the MaxDB server
    -   [maxdb\_data\_seek](/book/maxdb.html#maxdb_data_seek) — Adjusts
        the result pointer to an arbitary row in the result
    -   [maxdb\_debug](/book/maxdb.html#maxdb_debug) — Performs
        debugging operations
    -   [maxdb\_disable\_reads\_from\_master](/book/maxdb.html#maxdb_disable_reads_from_master)
        — Disable reads from master
    -   [maxdb\_disable\_rpl\_parse](/book/maxdb.html#maxdb_disable_rpl_parse)
        — Disable RPL parse
    -   [maxdb\_dump\_debug\_info](/book/maxdb.html#maxdb_dump_debug_info)
        — Dump debugging information into the log
    -   [maxdb\_embedded\_connect](/book/maxdb.html#maxdb_embedded_connect)
        — Open a connection to an embedded MaxDB server
    -   [maxdb\_enable\_reads\_from\_master](/book/maxdb.html#maxdb_enable_reads_from_master)
        — Enable reads from master
    -   [maxdb\_enable\_rpl\_parse](/book/maxdb.html#maxdb_enable_rpl_parse)
        — Enable RPL parse
    -   [maxdb\_errno](/book/maxdb.html#maxdb_errno) — Returns the error
        code for the most recent function call
    -   [maxdb\_error](/book/maxdb.html#maxdb_error) — Returns a string
        description of the last error
    -   [maxdb\_escape\_string](/book/maxdb.html#maxdb_escape_string) —
        别名 maxdb\_real\_escape\_string
    -   [maxdb\_execute](/book/maxdb.html#maxdb_execute) — 别名
        maxdb\_stmt\_execute
    -   [maxdb\_fetch\_array](/book/maxdb.html#maxdb_fetch_array) —
        Fetch a result row as an associative, a numeric array, or both
    -   [maxdb\_fetch\_assoc](/book/maxdb.html#maxdb_fetch_assoc) —
        Fetch a result row as an associative array
    -   [maxdb\_fetch\_field\_direct](/book/maxdb.html#maxdb_fetch_field_direct)
        — Fetch meta-data for a single field
    -   [maxdb\_fetch\_field](/book/maxdb.html#maxdb_fetch_field) —
        Returns the next field in the result set
    -   [maxdb\_fetch\_fields](/book/maxdb.html#maxdb_fetch_fields) —
        Returns an array of resources representing the fields in a
        result set
    -   [maxdb\_fetch\_lengths](/book/maxdb.html#maxdb_fetch_lengths) —
        Returns the lengths of the columns of the current row in the
        result set
    -   [maxdb\_fetch\_object](/book/maxdb.html#maxdb_fetch_object) —
        Returns the current row of a result set as an object
    -   [maxdb\_fetch\_row](/book/maxdb.html#maxdb_fetch_row) — Get a
        result row as an enumerated array
    -   [maxdb\_fetch](/book/maxdb.html#maxdb_fetch) — 别名
        maxdb\_stmt\_fetch
    -   [maxdb\_field\_count](/book/maxdb.html#maxdb_field_count) —
        Returns the number of columns for the most recent query
    -   [maxdb\_field\_seek](/book/maxdb.html#maxdb_field_seek) — Set
        result pointer to a specified field offset
    -   [maxdb\_field\_tell](/book/maxdb.html#maxdb_field_tell) — Get
        current field offset of a result pointer
    -   [maxdb\_free\_result](/book/maxdb.html#maxdb_free_result) —
        Frees the memory associated with a result
    -   [maxdb\_get\_client\_info](/book/maxdb.html#maxdb_get_client_info)
        — Returns the MaxDB client version as a string
    -   [maxdb\_get\_client\_version](/book/maxdb.html#maxdb_get_client_version)
        — Get MaxDB client info
    -   [maxdb\_get\_host\_info](/book/maxdb.html#maxdb_get_host_info) —
        Returns a string representing the type of connection used
    -   [maxdb\_get\_metadata](/book/maxdb.html#maxdb_get_metadata) —
        别名 maxdb\_stmt\_result\_metadata
    -   [maxdb\_get\_proto\_info](/book/maxdb.html#maxdb_get_proto_info)
        — Returns the version of the MaxDB protocol used
    -   [maxdb\_get\_server\_info](/book/maxdb.html#maxdb_get_server_info)
        — Returns the version of the MaxDB server
    -   [maxdb\_get\_server\_version](/book/maxdb.html#maxdb_get_server_version)
        — Returns the version of the MaxDB server as an integer
    -   [maxdb\_info](/book/maxdb.html#maxdb_info) — Retrieves
        information about the most recently executed query
    -   [maxdb\_init](/book/maxdb.html#maxdb_init) — Initializes MaxDB
        and returns an resource for use with maxdb\_real\_connect
    -   [maxdb\_insert\_id](/book/maxdb.html#maxdb_insert_id) — Returns
        the auto generated id used in the last query
    -   [maxdb\_kill](/book/maxdb.html#maxdb_kill) — Disconnects from a
        MaxDB server
    -   [maxdb\_master\_query](/book/maxdb.html#maxdb_master_query) —
        Enforce execution of a query on the master in a master/slave
        setup
    -   [maxdb\_more\_results](/book/maxdb.html#maxdb_more_results) —
        Check if there any more query results from a multi query
    -   [maxdb\_multi\_query](/book/maxdb.html#maxdb_multi_query) —
        Performs a query on the database
    -   [maxdb\_next\_result](/book/maxdb.html#maxdb_next_result) —
        Prepare next result from multi\_query
    -   [maxdb\_num\_fields](/book/maxdb.html#maxdb_num_fields) — Get
        the number of fields in a result
    -   [maxdb\_num\_rows](/book/maxdb.html#maxdb_num_rows) — Gets the
        number of rows in a result
    -   [maxdb\_options](/book/maxdb.html#maxdb_options) — Set options
    -   [maxdb\_param\_count](/book/maxdb.html#maxdb_param_count) — 别名
        maxdb\_stmt\_param\_count
    -   [maxdb\_ping](/book/maxdb.html#maxdb_ping) — Pings a server
        connection, or tries to reconnect if the connection has gone
        down
    -   [maxdb\_prepare](/book/maxdb.html#maxdb_prepare) — Prepare an
        SQL statement for execution
    -   [maxdb\_query](/book/maxdb.html#maxdb_query) — Performs a query
        on the database
    -   [maxdb\_real\_connect](/book/maxdb.html#maxdb_real_connect) —
        Opens a connection to a MaxDB server
    -   [maxdb\_real\_escape\_string](/book/maxdb.html#maxdb_real_escape_string)
        — Escapes special characters in a string for use in an SQL
        statement, taking into account the current charset of the
        connection
    -   [maxdb\_real\_query](/book/maxdb.html#maxdb_real_query) —
        Execute an SQL query
    -   [maxdb\_report](/book/maxdb.html#maxdb_report) — Enables or
        disables internal report functions
    -   [maxdb\_rollback](/book/maxdb.html#maxdb_rollback) — Rolls back
        current transaction
    -   [maxdb\_rpl\_parse\_enabled](/book/maxdb.html#maxdb_rpl_parse_enabled)
        — Check if RPL parse is enabled
    -   [maxdb\_rpl\_probe](/book/maxdb.html#maxdb_rpl_probe) — RPL
        probe
    -   [maxdb\_rpl\_query\_type](/book/maxdb.html#maxdb_rpl_query_type)
        — Returns RPL query type
    -   [maxdb\_select\_db](/book/maxdb.html#maxdb_select_db) — Selects
        the default database for database queries
    -   [maxdb\_send\_long\_data](/book/maxdb.html#maxdb_send_long_data)
        — 别名 maxdb\_stmt\_send\_long\_data
    -   [maxdb\_send\_query](/book/maxdb.html#maxdb_send_query) — Send
        the query and return
    -   [maxdb\_server\_end](/book/maxdb.html#maxdb_server_end) — Shut
        down the embedded server
    -   [maxdb\_server\_init](/book/maxdb.html#maxdb_server_init) —
        Initialize embedded server
    -   [maxdb\_set\_opt](/book/maxdb.html#maxdb_set_opt) — 别名
        maxdb\_options
    -   [maxdb\_sqlstate](/book/maxdb.html#maxdb_sqlstate) — Returns the
        SQLSTATE error from previous MaxDB operation
    -   [maxdb\_ssl\_set](/book/maxdb.html#maxdb_ssl_set) — Used for
        establishing secure connections using SSL
    -   [maxdb\_stat](/book/maxdb.html#maxdb_stat) — Gets the current
        system status
    -   [maxdb\_stmt\_affected\_rows](/book/maxdb.html#maxdb_stmt_affected_rows)
        — Returns the total number of rows changed, deleted, or inserted
        by the last executed statement
    -   [maxdb\_stmt\_bind\_param](/book/maxdb.html#maxdb_stmt_bind_param)
        — Binds variables to a prepared statement as parameters
    -   [maxdb\_stmt\_bind\_result](/book/maxdb.html#maxdb_stmt_bind_result)
        — Binds variables to a prepared statement for result storage
    -   [maxdb\_stmt\_close\_long\_data](/book/maxdb.html#maxdb_stmt_close_long_data)
        — Ends a sequence of maxdb\_stmt\_send\_long\_data
    -   [maxdb\_stmt\_close](/book/maxdb.html#maxdb_stmt_close) — Closes
        a prepared statement
    -   [maxdb\_stmt\_data\_seek](/book/maxdb.html#maxdb_stmt_data_seek)
        — Seeks to an arbitray row in statement result set
    -   [maxdb\_stmt\_errno](/book/maxdb.html#maxdb_stmt_errno) —
        Returns the error code for the most recent statement call
    -   [maxdb\_stmt\_error](/book/maxdb.html#maxdb_stmt_error) —
        Returns a string description for last statement error
    -   [maxdb\_stmt\_execute](/book/maxdb.html#maxdb_stmt_execute) —
        Executes a prepared Query
    -   [maxdb\_stmt\_fetch](/book/maxdb.html#maxdb_stmt_fetch) — Fetch
        results from a prepared statement into the bound variables
    -   [maxdb\_stmt\_free\_result](/book/maxdb.html#maxdb_stmt_free_result)
        — Frees stored result memory for the given statement handle
    -   [maxdb\_stmt\_init](/book/maxdb.html#maxdb_stmt_init) —
        Initializes a statement and returns an resource for use with
        maxdb\_stmt\_prepare
    -   [maxdb\_stmt\_num\_rows](/book/maxdb.html#maxdb_stmt_num_rows) —
        Return the number of rows in statements result set
    -   [maxdb\_stmt\_param\_count](/book/maxdb.html#maxdb_stmt_param_count)
        — Returns the number of parameter for the given statement
    -   [maxdb\_stmt\_prepare](/book/maxdb.html#maxdb_stmt_prepare) —
        Prepare an SQL statement for execution
    -   [maxdb\_stmt\_reset](/book/maxdb.html#maxdb_stmt_reset) — Resets
        a prepared statement
    -   [maxdb\_stmt\_result\_metadata](/book/maxdb.html#maxdb_stmt_result_metadata)
        — Returns result set metadata from a prepared statement
    -   [maxdb\_stmt\_send\_long\_data](/book/maxdb.html#maxdb_stmt_send_long_data)
        — Send data in blocks
    -   [maxdb\_stmt\_sqlstate](/book/maxdb.html#maxdb_stmt_sqlstate) —
        Returns SQLSTATE error from previous statement operation
    -   [maxdb\_stmt\_store\_result](/book/maxdb.html#maxdb_stmt_store_result)
        — Transfers a result set from a prepared statement
    -   [maxdb\_store\_result](/book/maxdb.html#maxdb_store_result) —
        Transfers a result set from the last query
    -   [maxdb\_thread\_id](/book/maxdb.html#maxdb_thread_id) — Returns
        the thread ID for the current connection
    -   [maxdb\_thread\_safe](/book/maxdb.html#maxdb_thread_safe) —
        Returns whether thread safety is given or not
    -   [maxdb\_use\_result](/book/maxdb.html#maxdb_use_result) —
        Initiate a result set retrieval
    -   [maxdb\_warning\_count](/book/maxdb.html#maxdb_warning_count) —
        Returns the number of warnings from the last query for the given
        link

The MaxDB PHP extension allows you to access the functionality provided
by MaxDB 7.5.0 and above. More information about the MaxDB Database
server can be found at
<a href="http://www.sdn.sap.com/irj/sdn/maxdb" class="link external">» http://www.sdn.sap.com/irj/sdn/maxdb</a>.

The MaxDB PHP extension is compatible to the MySQL mysqli extension.
There are only minor differences in the behaviour of some functions due
to the differences of the underlying database servers, MaxDB and MySQL.

The main differences to mysqli are in the following functions:

-   <span class="function">maxdb\_character\_set\_name</span> - Returns
    only ascii or unicode.
-   <span class="function">maxdb\_get\_client\_info</span> - Returns a
    different version string.
-   <span class="function">maxdb\_get\_client\_version</span> - Returns
    a different version string.
-   <span class="function">maxdb\_get\_host\_info</span> - Returns
    localhost or hostname.
-   <span class="function">maxdb\_get\_server\_info</span> - Returns a
    different version string.
-   <span class="function">maxdb\_get\_server\_version</span> - Returns
    a different version string.
-   <span class="function">maxdb\_kill</span> - Only disconnects the
    session.
-   <span class="function">maxdb\_multi\_query</span> - Can not handle
    multiple SQL statements.
-   <span class="function">maxdb\_next\_result</span> - Function returns
    always **`FALSE`**.
-   <span class="function">maxdb\_options</span> - Supports a different
    set of options.
-   <span class="function">maxdb\_report</span> - Supports a different
    report mode.
-   <span class="function">maxdb\_stat</span> - Returns a different
    system status string.
-   <span class="function">maxdb\_stmt\_store\_result</span> - Is not
    necessary for MaxDB.
-   <span class="function">maxdb\_store\_result</span> - Is not
    necessary for MaxDB.

Documentation for MaxDB can be found at
<a href="http://maxdb.sap.com/documentation/" class="link external">» http://maxdb.sap.com/documentation/</a>.

安装／配置
==========

**目录**

-   [需求](/book/maxdb.html#需求)
-   [安装](/book/maxdb.html#安装)
-   [运行时配置](/book/maxdb.html#运行时配置)
-   [资源类型](/book/maxdb.html#资源类型)

需求
----

In order to have these functions available, you must compile PHP with
MaxDB support. Additionally, you must have the MaxDB SQLDBC runtime
library available to access the MaxDB server.

Documentation for MaxDB SQLDBC can be found at
<a href="http://maxdb.sap.com/documentation/" class="link external">» http://maxdb.sap.com/documentation/</a>.

Download the MaxDB SQLDBC package from
<a href="http://www.sdn.sap.com/irj/sdn/maxdb-downloads" class="link external">» http://www.sdn.sap.com/irj/sdn/maxdb-downloads</a>.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/maxdb" class="link external">» https://pecl.php.net/package/maxdb</a>.

By using the **--with-maxdb\[=DIR\]** configuration option you enable
PHP to access MaxDB databases. *\[DIR\]* points to the directory that
contains the installed MaxDB SQLDBC package.

Windows users will need to enable `php_maxdb.dll` inside of `php.ini`.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                            | 默认  | 可修改范围    | 更新日志 |
|-----------------------------------------------------------------|-------|---------------|----------|
| <a href="/book/maxdb.html#" class="link">maxdb.default_host</a> | NULL  | PHP\_INI\_ALL |          |
| <a href="/book/maxdb.html#" class="link">maxdb.default_db</a>   | NULL  | PHP\_INI\_ALL |          |
| <a href="/book/maxdb.html#" class="link">maxdb.default_user</a> | NULL  | PHP\_INI\_ALL |          |
| <a href="/book/maxdb.html#" class="link">maxdb.default_pw</a>   | NULL  | PHP\_INI\_ALL |          |
| <a href="/book/maxdb.html#" class="link">maxdb.long_readlen</a> | "200" | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`maxdb.default_host` <span class="type">string</span>  
The default server host to use when connecting to the database server if
no other host is specified.

`maxdb.default_db` <span class="type">string</span>  
The default server database to use when connecting if no other database
is specified.

`maxdb.default_user` <span class="type">string</span>  
The default user name to use when connecting to the database server if
no other name is specified.

`maxdb.default_pw` <span class="type">string</span>  
The default password to use when connecting to the database server if no
other password is specified.

`maxdb.long_readlen` <span class="type">int</span>  
The default maximum length of bytes that is transferred to the client if
long data is retrieved from the MaxDB database server.

资源类型
--------

This extension defines resources.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

The following constants to use with <span
class="function">maxdb\_options</span> are defined. For further
description of these constants see
<a href="http://maxdb.sap.com/documentation/" class="link external">» http://maxdb.sap.com/documentation/</a>.

| 常量                      | 说明                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------|
| MAXDB\_COMPNAME           | The component name used to initialise the SQLDBC runtime environment.                                      |
| MAXDB\_APPLICATION        | The application to be connected to the database.                                                           |
| MAXDB\_APPVERSION         | The version of the application.                                                                            |
| MAXDB\_SQLMODE            | The SQL mode.                                                                                              |
| MAXDB\_UNICODE            | **`TRUE`**, if the connection is an unicode (UCS2) client or **`FALSE`**, if not.                          |
| MAXDB\_TIMEOUT            | The maximum allowed time of inactivity after which the connection to the database is closed by the system. |
| MAXDB\_ISOLATIONLEVEL     | Specifies whether and how shared locks and exclusive locks are implicitly requested or released.           |
| MAXDB\_PACKETCOUNT        | The number of different request packets used for the connection.                                           |
| MAXDB\_STATEMENTCACHESIZE | The number of prepared statements to be cached for the connection for re-use.                              |
| MAXDB\_CURSORPREFIX       | The prefix to use for result tables that are automatically named.                                          |

The function <span class="function">maxdb\_fetch\_array</span> uses a
constant for the different types of result arrays. The following
constants are defined:

| 常量                | 说明                                                                                                                                 |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| MAXDB\_ASSOC        | Columns are returned into the array having the fieldname as the array index.                                                         |
| MAXDB\_ASSOC\_UPPER | Columns are returned into the array having the upper case fieldname as the array index.                                              |
| MAXDB\_ASSOC\_LOWER | Columns are returned into the array having the lower case fieldname as the array index.                                              |
| MAXDB\_BOTH         | Columns are returned into the array having both a numerical index and the fieldname as the array index.                              |
| MAXDB\_NUM          | Columns are returned into the array having a numerical index to the fields. This index starts with 0, the first field in the result. |

范例
====

**目录**

-   [Basic usage](/book/maxdb.html#Basic%20usage)

Basic usage
-----------

All examples in the MaxDB PHP documentation use the HOTELDB demo
database from MaxDB. More about this database can be found at
<a href="http://maxdb.sap.com/doc/7_7/44/d8c25164bb38d0e10000000a1553f7/content.htm" class="link external">» http://maxdb.sap.com/doc/7_7/44/d8c25164bb38d0e10000000a1553f7/content.htm</a>.

To use the examples in the MaxDB PHP documentation, you have to load the
tutorial data into your database. Then you have to set maxdb.default\_db
in `php.ini` to the database that contains the tutorial data.

This simple example shows how to connect, execute a query, print
resulting rows and disconnect from a MaxDB database.

**示例 \#1 MaxDB extension overview example**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");
   
/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Performing SQL query */
$query = "SELECT * FROM hotel.city";
$result = maxdb_query($link, $query) or die("Query failed : " . maxdb_error());

/* Printing results in HTML */
echo "<table>\n";
while ($line = maxdb_fetch_array($result, MAXDB_ASSOC)) {
    echo "  <tr>\n";
    foreach ($line as $col_value) {
        echo "    <td>$col_value</td>\n";
    }
    echo "  </tr>\n";
}
echo "</table>\n";

/* Free resultset */
maxdb_free_result($result);

/* Closing connection */
maxdb_close($link);
?>
```

The following example shows how to bind variables to a SELECT INTO
statement.

**示例 \#2 Example for use of SELECT INTO statements**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}
   
/* Performing SQL query */
$stmt = maxdb_prepare ($link, "SELECT percentage INTO ? FROM hotel.countrylanguage where language = ?");
if (!$stmt) {
  printf ("Prepare failed: %s\n", maxdb_error($link));
}

$name = "Mbundu";

maxdb_stmt_bind_param($stmt, 'ds', $percentage, $name);
maxdb_stmt_execute($stmt);

printf ("%f\n", $percentage);

maxdb_stmt_close ($stmt);
?>
```

The following example shows how to use MaxDB database procedures.

**示例 \#3 Example fore using database procedures**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_report (MAXDB_REPORT_OFF);
maxdb_query($link,"DROP DBPROC test_proc");
maxdb_report (MAXDB_REPORT_ERROR);

$query = "create dbproc test_proc (INOUT e_text char(72)) AS select * from SYSDBA.DUAL; fetch into :e_text;";

maxdb_query($link, $query);

/* Performing SQL query */
$stmt = maxdb_prepare ($link, "CALL test_proc (?)");
if (!$stmt) {
  printf ("Prepare failed: %s\n", maxdb_error($link));
}

maxdb_stmt_bind_param($stmt, 's', $result);
maxdb_stmt_execute($stmt);

printf ("%s\n", $result);

maxdb_stmt_close ($stmt);
?>
```

预定义类
--------

<span class="classname">maxdb</span>
------------------------------------

Represents a connection between PHP and a MaxDB database.

构造函数
--------

-   <a href="/book/maxdb.html#maxdb_connect" class="link">maxdb</a> -
    construct a new maxdb object

方法
----

-   <a href="/book/maxdb.html#maxdb_autocommit" class="link">autocommit</a> -
    turns on or off auto-commiting database modifications

-   <a href="/book/maxdb.html#maxdb_change_user" class="link">change_user</a> -
    changes the user of the specified database connection

-   <a href="/book/maxdb.html#maxdb_character_set_name" class="link">character_set_name</a> -
    returns the default character set for the database connection

-   <a href="/book/maxdb.html#maxdb_close" class="link">close</a> -
    closes a previously opened connection

-   <a href="/book/maxdb.html#maxdb_commit" class="link">commit</a> -
    commits the current transaction

-   <a href="/book/maxdb.html#maxdb_connect" class="link">connect</a> -
    opens a new connection to MaxDB database server

-   <a href="/book/maxdb.html#maxdb_debug" class="link">debug</a> -
    performs debugging operations

-   <a href="/book/maxdb.html#maxdb_dump_debug_info" class="link">dump_debug_info</a> -
    dumps debug information

-   <a href="/book/maxdb.html#maxdb_get_client_info" class="link">get_client_info</a> -
    returns client version

-   <a href="/book/maxdb.html#maxdb_get_host_info" class="link">get_host_info</a> -
    returns type of connection used

-   <a href="/book/maxdb.html#maxdb_get_server_info" class="link">get_server_info</a> -
    returns version of the MaxDB server

-   <a href="/book/maxdb.html#maxdb_get_server_version" class="link">get_server_version</a> -
    returns version of the MaxDB server

-   <a href="/book/maxdb.html#maxdb_init" class="link">init</a> -
    initializes maxdb object

-   <a href="/book/maxdb.html#maxdb_info" class="link">info</a> -
    retrieves information about the most recently executed query

-   <a href="/book/maxdb.html#maxdb_kill" class="link">kill</a> - asks
    the server to kill a MaxDB thread

-   <a href="/book/maxdb.html#maxdb_multi_query" class="link">multi_query</a> -
    performs multiple queries

-   <a href="/book/maxdb.html#maxdb_more_results" class="link">more_results</a> -
    check if more results exist from currently executed multi-query

-   <a href="/book/maxdb.html#maxdb_next_result" class="link">next_result</a> -
    reads next result from currently executed multi-query

-   <a href="/book/maxdb.html#maxdb_options" class="link">options</a> -
    set options

-   <a href="/book/maxdb.html#maxdb_ping" class="link">ping</a> - pings
    a server connection or reconnects if there is no connection

-   <a href="/book/maxdb.html#maxdb_prepare" class="link">prepare</a> -
    prepares an SQL query

-   <a href="/book/maxdb.html#maxdb_query" class="link">query</a> -
    performs a query

-   <a href="/book/maxdb.html#maxdb_real_connect" class="link">real_connect</a> -
    attempts to open a connection to MaxDB database server

-   <a href="/book/maxdb.html#maxdb_real_escape_string" class="link">escape_string</a> -
    escapes special characters in a string for use in an SQL statement,
    taking into account the current charset of the connection

-   <a href="/book/maxdb.html#maxdb_rollback" class="link">rollback</a> -
    rolls back the current transaction

-   <a href="/book/maxdb.html#maxdb_select_db" class="link">select_db</a> -
    selects the default database

-   <a href="/book/maxdb.html#maxdb_ssl_set" class="link">ssl_set</a> -
    sets ssl parameters

-   <a href="/book/maxdb.html#maxdb_stat" class="link">stat</a> - gets
    the current system status

-   <a href="/book/maxdb.html#maxdb_stmt_init" class="link">stmt_init</a>-
    initializes a statement for use with
    <a href="/book/maxdb.html#maxdb_stmt_prepare" class="link">maxdb_stmt_prepare</a>

-   <a href="/book/maxdb.html#maxdb_store_result" class="link">store_result</a> -
    transfers a resultset from last query

-   <a href="/book/maxdb.html#maxdb_use_result" class="link">use_result</a> -
    transfers an unbuffered resultset from last query

-   <a href="/book/maxdb.html#maxdb_thread_safe" class="link">thread-safe</a> -
    returns whether thread safety is given or not

属性
----

-   <a href="/book/maxdb.html#maxdb_affected_rows" class="link">affected_rows</a> -
    gets the number of affected rows in a previous MaxDB operation

-   <a href="/book/maxdb.html#maxdb_get_client_info" class="link">client_info</a> -
    returns the MaxDB client version as a string

-   <a href="/book/maxdb.html#maxdb_get_client_version" class="link">client_version</a> -
    returns the MaxDB client version as an integer

-   <a href="/book/maxdb.html#maxdb_errno" class="link">errno</a> -
    returns the error code for the most recent function call

-   <a href="/book/maxdb.html#maxdb_error" class="link">error</a> -
    returns the error string for the most recent function call

-   <a href="/book/maxdb.html#maxdb_field_count" class="link">field_count</a> -
    returns the number of columns for the most recent query

-   <a href="/book/maxdb.html#maxdb_get_host_info" class="link">host_info</a> -
    returns a string representing the type of connection used

-   <a href="/book/maxdb.html#maxdb_info" class="link">info</a> -
    retrieves information about the most recently executed query

-   <a href="/book/maxdb.html#maxdb_insert_id" class="link">insert_id</a> -
    returns the auto generated id used in the last query

-   <a href="/book/maxdb.html#maxdb_get_proto_info" class="link">protocol_version</a> -
    returns the version of the MaxDB protocol used

-   <a href="/book/maxdb.html#maxdb_sqlstate" class="link">sqlstate</a> -
    returns a string containing the SQLSTATE error code for the last
    error

-   <a href="/book/maxdb.html#maxdb_thread_id" class="link">thread_id</a> -
    returns the thread ID for the current connection

-   <a href="/book/maxdb.html#maxdb_warning_count" class="link">warning_count</a> -
    returns the number of warnings generated during execution of the
    previous SQL statement

<span class="classname">maxdb\_stmt</span>
------------------------------------------

Represents a prepared statement.

方法
----

-   <a href="/book/maxdb.html#maxdb_bind_param" class="link">bind_param</a> -
    binds variables to a prepared statement

-   <a href="/book/maxdb.html#maxdb_bind_result" class="link">bind_result</a> -
    binds variables to a prepared statement for result storage

-   <a href="/book/maxdb.html#maxdb_stmt_close" class="link">close</a> -
    closes a prepared statement

-   <a href="/book/maxdb.html#maxdb_stmt_data_seek" class="link">data-seek</a> -
    seeks to an arbitrary row in a statement result set

-   <a href="/book/maxdb.html#maxdb_execute" class="link">execute</a> -
    executes a prepared statement

-   <a href="/book/maxdb.html#maxdb_fetch" class="link">fetch</a> -
    fetches result from a prepared statement into bound variables

-   <a href="/book/maxdb.html#maxdb_stmt_free_result" class="link">free_result</a> -
    frees stored result memory for the given statement handle

-   <a href="/book/maxdb.html#maxdb_stmt_result_metadata" class="link">result_metadata</a> -
    retrieves a resultset from a prepared statement for metadata
    information

-   <a href="/book/maxdb.html#maxdb_stmt_prepare" class="link">prepare</a> -
    prepares an SQL query

-   <a href="/book/maxdb.html#maxdb_send_long_data" class="link">send_long_data</a> -
    sends data in chunks

-   <a href="/book/maxdb.html#maxdb_stmt_close_long_data" class="link">close_long_data</a> -
    end sending long data

-   <a href="/book/maxdb.html#maxdb_stmt_reset" class="link">reset</a> -
    resets a prepared statement

-   <a href="/book/maxdb.html#maxdb_stmt_store_result" class="link">store_result</a> -
    buffers complete resultset from a prepared statement

属性
----

-   <a href="/book/maxdb.html#maxdb_stmt_affected_rows" class="link">affected_rows</a> -
    returns affected rows from last statement execution

-   <a href="/book/maxdb.html#maxdb_stmt_errno" class="link">errno</a> -
    returns errorcode for last statement function

-   <a href="/book/maxdb.html#maxdb_stmt_error" class="link">errno</a> -
    returns errormessage for last statement function

-   <a href="/book/maxdb.html#maxdb_stmt_param_count" class="link">param_count</a> -
    returns number of parameter for a given prepare statement

-   <a href="/book/maxdb.html#maxdb_stmt_sqlstate" class="link">sqlstate</a> -
    returns a string containing the SQLSTATE error code for the last
    statement function

<span class="classname">maxdb\_result</span>
--------------------------------------------

Represents the result set obtained from a query against the database.

方法
----

-   <a href="/book/maxdb.html#maxdb_free_result" class="link">close</a> -
    closes resultset

-   <a href="/book/maxdb.html#maxdb_data_seek" class="link">data_seek</a> -
    moves internal result pointer

-   <a href="/book/maxdb.html#maxdb_fetch_field" class="link">fetch_field</a> -
    gets column information from a resultset

-   <a href="/book/maxdb.html#maxdb_fetch_fields" class="link">fetch_fields</a> -
    gets information for all columns from a resulset

-   <a href="/book/maxdb.html#maxdb_fetch_field_direct" class="link">fetch_field_direct</a> -
    gets column information for specified column

-   <a href="/book/maxdb.html#maxdb_fetch_array" class="link">fetch_array</a> -
    fetches a result row as an associative array, a numeric array, or
    both.

-   <a href="/book/maxdb.html#maxdb_fetch_assoc" class="link">fetch_assoc</a> -
    fetches a result row as an associative array

-   <a href="/book/maxdb.html#maxdb_fetch_object" class="link">fetch_object</a> -
    fetches a result row as an object

-   <a href="/book/maxdb.html#maxdb_fetch_row" class="link">fetch_row</a> -
    gets a result row as an enumerated array

-   <a href="/book/maxdb.html#maxdb_free_result" class="link">close</a> -
    frees result memory

-   <a href="/book/maxdb.html#maxdb_field_seek" class="link">field_seek</a> -
    set result pointer to a specified field offset

属性
----

-   <a href="/book/maxdb.html#maxdb_field_tell" class="link">current_field</a> -
    returns offset of current fieldpointer

-   <a href="/book/maxdb.html#maxdb_field_count" class="link">field_count</a> -
    returns number of fields in resultset

-   <a href="/book/maxdb.html#maxdb_fetch_lengths" class="link">lengths</a> -
    returns an array of columnlengths

-   <a href="/book/maxdb.html#maxdb_num_rows" class="link">num_rows</a> -
    returns number of rows in resultset

maxdb\_affected\_rows
=====================

maxdb::affected\_rows
=====================

Gets the number of affected rows in a previous MaxDB operation

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_affected\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span>`$maxdb->affected_rows`;

<span class="function">maxdb\_affected\_rows</span> returns the number
of rows affected by the last INSERT, UPDATE, or DELETE query associated
with the provided `link` parameter. If this number cannot be determined,
this function will return -1.

> **Note**:
>
> For SELECT statements <span
> class="function">maxdb\_affected\_rows</span> works like <span
> class="function">maxdb\_num\_rows</span>.

The <span class="function">maxdb\_affected\_rows</span> function only
works with queries which modify a table. In order to return the number
of rows from a SELECT query, use the <span
class="function">maxdb\_num\_rows</span> function instead.

### 返回值

An integer greater than zero indicates the number of rows affected or
retrieved. Zero indicates that no records where updated for an UPDATE
statement, no rows matched the WHERE clause in the query or that no
query has yet been executed. -1 indicates that the number of rows
affected can not be determined.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_report (MAXDB_REPORT_OFF);
$maxdb->query("DROP TABLE mycustomer");
maxdb_report (MAXDB_REPORT_ERROR);

/* Insert rows */
$maxdb->query("CREATE TABLE mycustomer AS SELECT * from hotel.customer");
printf("Affected rows (INSERT): %d\n", $maxdb->affected_rows);

$maxdb->query("ALTER TABLE mycustomer ADD Status int default 0");

/* update rows */
$maxdb->query("UPDATE mycustomer SET Status=1 WHERE cno > 50");
printf("Affected rows (UPDATE): %d\n", $maxdb->affected_rows);

/* delete rows */
$maxdb->query("DELETE FROM mycustomer WHERE cno < 50");
printf("Affected rows (DELETE): %d\n", $maxdb->affected_rows);

/* select all rows */
$result = $maxdb->query("SELECT title FROM mycustomer");
printf("Affected rows (SELECT): %d\n", $maxdb->affected_rows);

$result->close();

/* Delete table Language */
$maxdb->query("DROP TABLE mycustomer");

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

if (!$link) {
   printf("Can't connect to localhost. Error: %s\n", maxdb_connect_error());
   exit();
}

maxdb_report (MAXDB_REPORT_OFF);
maxdb_query($link,"DROP TABLE mycustomer");
maxdb_report (MAXDB_REPORT_ERROR);

/* Insert rows */
maxdb_query($link, "CREATE TABLE mycustomer AS SELECT * from hotel.customer");
printf("Affected rows (INSERT): %d\n", maxdb_affected_rows($link));

maxdb_query($link, "ALTER TABLE mycustomer ADD Status int default 0");

/* update rows */
maxdb_query($link, "UPDATE mycustomer SET Status=1 WHERE cno > 50");
printf("Affected rows (UPDATE): %d\n", maxdb_affected_rows($link));

/* delete rows */
maxdb_query($link, "DELETE FROM mycustomer WHERE cno < 50");
printf("Affected rows (DELETE): %d\n", maxdb_affected_rows($link));

/* select all rows */
$result = maxdb_query($link, "SELECT title FROM mycustomer");
printf("Affected rows (SELECT): %d\n", maxdb_affected_rows($link));

maxdb_free_result($result);

/* Delete table Language */
maxdb_query($link, "DROP TABLE mycustomer");

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Affected rows (INSERT): 15
    Affected rows (UPDATE): 15
    Affected rows (DELETE): 0
    Affected rows (SELECT): 15

### 参见

-   <span class="function">maxdb\_num\_rows</span>
-   <span class="function">maxdb\_info</span>

maxdb\_autocommit
=================

maxdb::auto\_commit
===================

Turns on or off auto-commiting database modifications

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">bool</span> `$mode`</span>
)

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::auto\_commit</span> ( <span
class="methodparam"><span class="type">bool</span> `$mode`</span> )

<span class="function">maxdb\_autocommit</span> is used to turn on or
off auto-commit mode on queries for the database connection represented
by the `link` resource.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* turn autocommit on */
$maxdb->autocommit(TRUE);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

if (!$link) {
   printf("Can't connect to localhost. Error: %s\n", maxdb_connect_error());
   exit();
}

/* turn autocommit on */
maxdb_autocommit($link, TRUE);

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

### 参见

-   <span class="function">maxdb\_commit</span>
-   <span class="function">maxdb\_rollback</span>

maxdb\_bind\_param
==================

别名 <span class="function">maxdb\_stmt\_bind\_param</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_bind\_param</span>

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_bind\_result
===================

别名 <span class="function">maxdb\_stmt\_bind\_result</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_bind\_result</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_change\_user
===================

maxdb::change\_user
===================

Changes the user of the specified database connection

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_change\_user</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$user`</span> , <span class="methodparam"><span
class="type">string</span> `$password`</span> , <span
class="methodparam"><span class="type">string</span> `$database`</span>
)

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::change\_user</span> ( <span
class="methodparam"><span class="type">string</span> `$user`</span> ,
<span class="methodparam"><span class="type">string</span>
`$password`</span> , <span class="methodparam"><span
class="type">string</span> `$database`</span> )

<span class="function">maxdb\_change\_user</span> is used to change the
user of the specified database connection as given by the `link`
parameter and to set the current database to that specified by the
`database` parameter.

In order to successfully change users a valid `username` and `password`
parameters must be provided and that user must have sufficient
permissions to access the desired database. If for any reason
authorization fails, the current user authentication will remain.

> **Note**:
>
> Using this command will always cause the current database connection
> to behave as if was a completely new database connection, regardless
> of if the operation was completed successfully. This reset includes
> performing a rollback on any active transactions, closing all
> temporary tables, and unlocking all locked tables.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connect database test */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($result = $maxdb->query("SELECT * FROM dual")) {
   $row = $result->fetch_row();
   printf("Result: %s\n", $row[0]);
   $result->free();
}

/* reset all and select a new database */
if (!$maxdb->change_user("DBADMIN", "SECRET", "DEMODB")) {
  printf("Database not running\n");
} else {
  printf("Database running\n");
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($result = maxdb_query($link, "SELECT * FROM dual")) {
   $row = maxdb_fetch_row($result);
   printf("Result: %s\n", $row[0]);
   maxdb_free_result($result);
}

/* reset all and select a new database */
if (!maxdb_change_user($link, "DBADMIN", "SECRET", "DEMODB")) {
  printf("Database not running\n");
} else {
  printf("Database running\n");
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Result: a
    Database running

### 参见

-   <span class="function">maxdb\_connect</span>
-   <span class="function">maxdb\_select\_db</span>

maxdb\_character\_set\_name
===========================

maxdb::character\_set\_name
===========================

Returns the default character set for the database connection

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_character\_set\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span> <span
class="methodname">maxdb::character\_set\_name</span> ( <span
class="methodparam">void</span> )

Returns the current character set for the database connection specified
by the `link` parameter.

### 返回值

The default character set for the current connection, either ascii or
unicode.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Print current character set */
$charset = $maxdb->character_set_name();
printf ("Current character set is %s\n", $charset);

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Print current character set */
$charset = maxdb_character_set_name($link);
printf ("Current character set is %s\n",$charset);

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Current character set is ascii

### 参见

-   <span class="function">maxdb\_client\_encoding</span>
-   <span class="function">maxdb\_real\_escape\_string</span>

maxdb\_client\_encoding
=======================

别名 <span class="function">maxdb\_character\_set\_name</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_character\_set\_name</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_close\_long\_data
========================

maxdb::close\_long\_data
========================

别名 <span class="function">maxdb\_stmt\_close\_long\_data</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_close\_long\_data</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_close
============

maxdb::close
============

Closes a previously opened database connection

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::close</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_close</span> function closes a
previously opened database connection specified by the `link` parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">maxdb\_connect</span>
-   <span class="function">maxdb\_init</span>
-   <span class="function">maxdb\_real\_connect</span>

maxdb\_commit
=============

maxdb::commit
=============

Commits the current transaction

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_commit</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::commit</span> ( <span
class="methodparam">void</span> )

Commits the current transaction for the database connection specified by
the `link` parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* set autocommit to off */
$maxdb->autocommit(FALSE);

maxdb_report (MAXDB_REPORT_OFF);
$maxdb->query("DROP TABLE mycustomer");
maxdb_report (MAXDB_REPORT_ERROR);

$maxdb->query("CREATE TABLE mycustomer LIKE hotel.customer");

/* Insert some values */
$maxdb->query("INSERT INTO mycustomer VALUES (3000,'Mrs','Jenny','Porter','10580','1340 N.Ash Street, #3')");
$maxdb->query("INSERT INTO mycustomer VALUES (3100,'Mr','Peter','Brown','48226','1001 34th Str., APT.3')");

/* commit transaction */
$maxdb->commit();

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* set autocommit to off */
maxdb_autocommit($link, FALSE);

maxdb_report (MAXDB_REPORT_OFF);
maxdb_query($link,"DROP TABLE mycustomer");
maxdb_report (MAXDB_REPORT_ERROR);

maxdb_query($link, "CREATE TABLE mycustomer LIKE hotel.customer");

/* Insert some values */
maxdb_query($link, "INSERT INTO mycustomer VALUES (3000,'Mrs','Jenny','Porter','10580','1340 N.Ash Street, #3')");
maxdb_query($link, "INSERT INTO mycustomer VALUES (3100,'Mr','Peter','Brown','48226','1001 34th Str., APT.3')");

/* commit transaction */
maxdb_commit($link);

/* close connection */
maxdb_close($link);
?>
```

The above examples produces no output.

### 参见

-   <span class="function">maxdb\_autocommit</span>
-   <span class="function">maxdb\_rollback</span>

maxdb\_connect\_errno
=====================

Returns the error code from last connect call

### 说明

<span class="type">int</span> <span
class="methodname">maxdb\_connect\_errno</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_connect\_errno</span> function will
return the last error code number for last call to <span
class="function">maxdb\_connect</span>. If no errors have occurred, this
function will return zero.

### 返回值

An error code value for the last call to <span
class="function">maxdb\_connect</span>, if it failed. zero means no
error occurred.

### 范例

**示例 \#1 maxdb\_connect\_errno sample**

``` php
<?php
$link = maxdb_connect("localhost", "XXXXXXXX", "YYYYYYYYY");

if (!$link) {
   printf("Can't connect to localhost. Errorcode: %d\n", maxdb_connect_errno());
}
?>
```

以上例程的输出类似于：

    PHP Warning:  maxdb_connect(): -4008 POS(1) Unknown user name/password combination [08004] <...>
    Can't connect to localhost. Errorcode: -4008

### 参见

-   <span class="function">maxdb\_connect</span>
-   <span class="function">maxdb\_connect\_error</span>
-   <span class="function">maxdb\_errno</span>
-   <span class="function">maxdb\_error</span>
-   <span class="function">maxdb\_sqlstate</span>

maxdb\_connect\_error
=====================

Returns a string description of the last connect error

### 说明

<span class="type">string</span> <span
class="methodname">maxdb\_connect\_error</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_connect\_error</span> function is
identical to the corresponding <span
class="function">maxdb\_connect\_errno</span> function in every way,
except instead of returning an integer error code the <span
class="function">maxdb\_connect\_error</span> function will return a
string representation of the last error to occur for the last <span
class="function">maxdb\_connect</span> call. If no error has occurred,
this function will return an empty string.

### 返回值

A string that describes the error. An empty string if no error occurred.

### 范例

**示例 \#1 maxdb\_connect\_error sample**

``` php
<?php

$link = maxdb_connect("localhost", "nonexisting_user", "");

if (!$link) {
   printf("Can't connect to localhost. Error: %s\n", maxdb_connect_error());
}
?>
```

以上例程的输出类似于：

    PHP Warning:  maxdb_connect(): -4008 POS(1) Unknown user name/password combination <...>
    Can't connect to localhost. Error: POS(1) Unknown user name/password combination

### 参见

-   <span class="function">maxdb\_connect</span>
-   <span class="function">maxdb\_connect\_errno</span>
-   <span class="function">maxdb\_errno</span>
-   <span class="function">maxdb\_error</span>
-   <span class="function">maxdb\_sqlstate</span>

maxdb\_connect
==============

maxdb::\_\_construct
====================

Open a new connection to the MaxDB server

### 说明

过程化风格

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">maxdb\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passwd`</span> \[, <span
class="methodparam"><span class="type">string</span> `$dbname`</span>
\[, <span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$socket`</span>
\]\]\]\]\]\] )

面向对象风格

<span class="methodname">maxdb::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passwd`</span> \[, <span
class="methodparam"><span class="type">string</span> `$dbname`</span>
\[, <span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$socket`</span>
\]\]\]\]\]\] )

The <span class="function">maxdb\_connect</span> function attempts to
open a connection to the MaxDB Server running on `host` which can be
either a host name or an IP address. Passing the string "localhost" to
this parameter, the local host is assumed. If successful, the <span
class="function">maxdb\_connect</span> will return an resource
representing the connection to the database 或者在失败时返回
**`FALSE`**.

The `username` and `password` parameters specify the username and
password under which to connect to the MaxDB server. If the password is
not provided (the **`NULL`** value is passed), the MaxDB server will
attempt to authenticate the user against the `maxdb.default_pw` in
`php.ini`.

The `dbname` parameter if provided will specify the default database to
be used when performing queries. If not provied, the entry
`maxdb.default_db` in `php.ini` is used.

The `port` and `socket` parameters are ignored for the MaxDB server.

### 返回值

Returns a resource which represents the connection to a MaxDB Server or
**`FALSE`** if the connection failed.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

printf("Host information: %s\n", $maxdb->host_info);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

printf("Host information: %s\n", maxdb_get_host_info($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Host information: localhost

maxdb\_data\_seek
=================

maxdb\_result::data\_seek
=========================

Adjusts the result pointer to an arbitary row in the result

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$offset`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_result::data\_seek</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

The <span class="function">maxdb\_data\_seek</span> function seeks to an
arbitrary result pointer specified by the `offset` in the result set
represented by `result`. The `offset` parameter must be between zero and
the total number of rows minus one (0..<span
class="function">maxdb\_num\_rows</span> - 1).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER BY name";
if ($result = $maxdb->query( $query)) {

   /* seek to row no. 10 */
   $result->data_seek(10);

   /* fetch row */
   $row = $result->fetch_row();

   printf ("City: %s  State: %s\n", $row[0], $row[1]);

   /* free result set*/
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER BY name";

if ($result = maxdb_query($link, $query)) {

   /* seek to row no. 400 */
   maxdb_data_seek($result, 10);

   /* fetch row */
   $row = maxdb_fetch_row($result);

   printf ("City: %s  State: %s\n", $row[0], $row[1]);

   /* free result set*/
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    City: Irvine  State: CA

### 参见

-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_fetch\_row</span>
-   <span class="function">maxdb\_num\_rows</span>

maxdb\_debug
============

Performs debugging operations

### 说明

<span class="type">void</span> <span
class="methodname">maxdb\_debug</span> ( <span class="methodparam"><span
class="type">string</span> `$debug`</span> )

The <span class="function">maxdb\_debug</span> can be used to trace the
SQLDBC communication. The following strings can be used as a parameter
to <span class="function">maxdb\_debug</span>:

-   TRACE SHORT ON\|OFF - Enables/disables method call trace.
-   TRACE LONG ON\|OFF - Enables/disables method argument and detail
    debug trace.
-   TRACE PACKET ON\|OFF\|\<size\> - Enables/disables packet trace,
    limiting the size of the traced object to the specified number of
    bytes, or 1000 if no size is specified.
-   TRACE SQL ON\|OFF - Enables/disables high level api trace.
-   TRACE TIMESTAMP ON\|OFF - Enables/disables a timestamp prefix on
    each line that is traced.
-   TRACE SIZE \<size\> - Limits the size of the trace file to \<size\>
    bytes, at least 8192 bytes are required.

### 返回值

<span class="function">maxdb\_debug</span> doesn't return any value.

### 范例

**示例 \#1 过程化风格**

``` php
<?php

maxdb_debug("trace packet 200");

$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* close connection */
maxdb_close($link);
?>
```

The above example produces no output.

maxdb\_disable\_reads\_from\_master
===================================

maxdb::disable\_reads\_from\_master
===================================

Disable reads from master

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_disable\_reads\_from\_master</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">void</span> <span
class="methodname">maxdb::disable\_reads\_from\_master</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_disable\_rpl\_parse
==========================

Disable RPL parse

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_disable\_rpl\_parse</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_dump\_debug\_info
========================

Dump debugging information into the log

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_dump\_debug\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_embedded\_connect
========================

Open a connection to an embedded MaxDB server

### 说明

<span class="type">resource</span> <span
class="methodname">maxdb\_embedded\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$dbname`</span> \]
)

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_enable\_reads\_from\_master
==================================

Enable reads from master

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_enable\_reads\_from\_master</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_enable\_rpl\_parse
=========================

Enable RPL parse

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_enable\_rpl\_parse</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_errno
============

maxdb::errno
============

Returns the error code for the most recent function call

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_errno</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span>`$maxdb->errno`;

The <span class="function">maxdb\_errno</span> function will return the
last error code for the most recent MaxDB function call that can succeed
or fail with respect to the database link defined by the `link`
parameter. If no errors have occurred, this function will return zero.

### 返回值

An error code value for the last call, if it failed. zero means no error
occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if (!$maxdb->query("SELECT xxx FROM hotel.city")) {
   printf("Errorcode: %d\n", $maxdb->errno);
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if (!maxdb_query($link, "SELECT xxx FROM hotel.city")) {
   printf("Errorcode: %d\n", maxdb_errno($link));
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    PHP Warning:  maxdb_query(): -4005 POS(8) Unknown column name:XXX [42000] <...>
    Errorcode: -4005

### 参见

-   <span class="function">maxdb\_connect\_errno</span>
-   <span class="function">maxdb\_connect\_error</span>
-   <span class="function">maxdb\_error</span>
-   <span class="function">maxdb\_sqlstate</span>

maxdb\_error
============

maxdb::error
============

Returns a string description of the last error

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_error</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span>`$maxdb->error`;

The <span class="function">maxdb\_error</span> function is identical to
the corresponding <span class="function">maxdb\_errno</span> function in
every way, except instead of returning an integer error code the <span
class="function">maxdb\_error</span> function will return a string
representation of the last error to occur for the database connection
represented by the `link` parameter. If no error has occurred, this
function will return an empty string.

### 返回值

A string that describes the error. An empty string if no error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if (!$maxdb->query("SELECT xxx FROM hotel.city")) {
   printf("Errormessage: %s\n", $maxdb->error);
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if (!maxdb_query($link, "SELECT xxx FROM hotel.city")) {
   printf("Errormessgae: %s\n", maxdb_error($link));
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    PHP Warning:  maxdb_query(): -4005 POS(8) Unknown column name:XXX [42000]
    Errormessgae: POS(8) Unknown column name:XXX

### 参见

-   <span class="function">maxdb\_connect\_errno</span>
-   <span class="function">maxdb\_connect\_error</span>
-   <span class="function">maxdb\_errno</span>
-   <span class="function">maxdb\_sqlstate</span>

maxdb\_escape\_string
=====================

别名 <span class="function">maxdb\_real\_escape\_string</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_real\_escape\_string</span>.

maxdb\_execute
==============

别名 <span class="function">maxdb\_stmt\_execute</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_execute</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_fetch\_array
===================

maxdb\_result::fetch\_array
===========================

Fetch a result row as an associative, a numeric array, or both

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$resulttype`</span> \] )

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_result::fetch\_array</span> (\[ <span
class="methodparam"><span class="type">int</span> `$resulttype`</span>
\] )

Returns an array that corresponds to the fetched row or **`NULL`** if
there are no more rows for the resultset represented by the `result`
parameter.

<span class="function">maxdb\_fetch\_array</span> is an extended version
of the <span class="function">maxdb\_fetch\_row</span> function. In
addition to storing the data in the numeric indices of the result array,
the <span class="function">maxdb\_fetch\_array</span> function can also
store the data in associative indices, using the field names of the
result set as keys.

> **Note**: <span
> class="simpara">此函数返回的字段名*大小写敏感*。</span>

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

If two or more columns of the result have the same field names, the last
column will take precedence and overwrite the earlier data. In order to
access multiple columns with the same name, the numerically indexed
version of the row must be used.

The optional second argument `resulttype` is a constant indicating what
type of array should be produced from the current row data. The possible
values for this parameter are the constants MAXDB\_ASSOC,
MAXDB\_ASSOC\_UPPER, MAXDB\_ASSOC\_LOWER, MAXDB\_NUM, or MAXDB\_BOTH. By
default the <span class="function">maxdb\_fetch\_array</span> function
will assume MAXDB\_BOTH, which is a combination of MAXDB\_NUM and
MAXDB\_ASSOC for this parameter.

By using the MAXDB\_ASSOC constant this function will behave identically
to the <span class="function">maxdb\_fetch\_assoc</span>, while
MAXDB\_NUM will behave identically to the <span
class="function">maxdb\_fetch\_row</span> function. The final option
MAXDB\_BOTH will create a single array with the attributes of both.

By using the MAXDB\_ASSOC\_UPPER constant, the behaviour of this
function is identical to the use of MAXDB\_ASSOC except the array index
of a column is the fieldname in upper case.

By using the MAXDB\_ASSOC\_LOWER constant, the behaviour of this
function is identical to the use of MAXDB\_ASSOC except the array index
of a column is the fieldname in lower case.

### 返回值

Returns an array that corresponds to the fetched row or **`NULL`** if
there are no more rows in resultset.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";
$result = $maxdb->query($query);

/* numeric array */
$row = $result->fetch_array(MAXDB_NUM);
printf ("%s (%s)\n", $row[0], $row[1]);

/* associative array */
$row = $result->fetch_array(MAXDB_ASSOC);
printf ("%s (%s)\n", $row["NAME"], $row["STATE"]);

/* associative and numeric array */
$row = $result->fetch_array(MAXDB_BOTH);
printf ("%s (%s)\n", $row[0], $row["STATE"]);

/* free result set */
$result->close();

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";
$result = maxdb_query($link, $query);

/* numeric array */
$row = maxdb_fetch_array($result, MAXDB_NUM);
printf ("%s (%s)\n", $row[0], $row[1]);

/* associative array */
$row = maxdb_fetch_array($result, MAXDB_ASSOC);
printf ("%s (%s)\n", $row["NAME"], $row["STATE"]);

/* associative and numeric array */
$row = maxdb_fetch_array($result, MAXDB_BOTH);
printf ("%s (%s)\n", $row[0], $row["STATE"]);

/* free result set */
maxdb_free_result($result);

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    New York (NY)
    New York (NY)
    Long Island (NY)

### 参见

-   <span class="function">maxdb\_fetch\_assoc</span>
-   <span class="function">maxdb\_fetch\_row</span>
-   <span class="function">maxdb\_fetch\_resource</span>

maxdb\_fetch\_assoc
===================

maxdb\_result::fetch\_assoc
===========================

Fetch a result row as an associative array

### 说明

过程化风格

<span class="type">array</span> <span
class="methodname">maxdb\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">array</span> <span
class="methodname">maxdb\_result::fetch\_assoc</span> ( <span
class="methodparam">void</span> )

Returns an associative array that corresponds to the fetched row or
**`NULL`** if there are no more rows.

The <span class="function">maxdb\_fetch\_assoc</span> function is used
to return an associative array representing the next row in the result
set for the result represented by the `result` parameter, where each key
in the array represents the name of one of the result set's columns.

If two or more columns of the result have the same field names, the last
column will take precedence. To access the other column(s) of the same
name, you either need to access the result with numeric indices by using
<span class="function">maxdb\_fetch\_row</span> or add alias names.

> **Note**: <span
> class="simpara">此函数返回的字段名*大小写敏感*。</span>

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 返回值

Returns an array that corresponds to the fetched row or **`NULL`** if
there are no more rows in resultset.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";

if ($result = $maxdb->query($query)) {

   /* fetch associative array */
   while ($row = $result->fetch_assoc()) {
       printf ("%s (%s)\n", $row["NAME"], $row["STATE"]);
   }

   /* free result set */
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";

if ($result = maxdb_query($link, $query)) {

   /* fetch associative array */
   while ($row = maxdb_fetch_assoc($result)) {
       printf ("%s (%s)\n", $row["NAME"], $row["STATE"]);
   }

   /* free result set */
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    New York (NY)
    New York (NY)
    Long Island (NY)
    Albany (NY)
    Washington (DC)
    Washington (DC)
    Washington (DC)
    Silver Spring (MD)
    Daytona Beach (FL)
    Deerfield Beach (FL)
    Clearwater (FL)
    Cincinnati (OH)
    Detroit (MI)
    Rosemont (IL)
    Chicago (IL)
    Chicago (IL)
    New Orleans (LA)
    Dallas (TX)
    Los Angeles (CA)
    Hollywood (CA)
    Long Beach (CA)
    Palm Springs (CA)
    Irvine (CA)
    Santa Clara (CA)
    Portland (OR)

### 参见

-   <span class="function">maxdb\_fetch\_array</span>
-   <span class="function">maxdb\_fetch\_row</span>
-   <span class="function">maxdb\_fetch\_resource</span>

maxdb\_fetch\_field\_direct
===========================

maxdb\_result::fetch\_field\_direct
===================================

Fetch meta-data for a single field

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_fetch\_field\_direct</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$fieldnr`</span> )

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_result::fetch\_field\_direct</span> ( <span
class="methodparam"><span class="type">int</span> `$fieldnr`</span> )

<span class="function">maxdb\_fetch\_field\_direct</span> returns an
resource which contains field definition information from specified
resultset. The value of fieldnr must be in the range from *0* to *number
of fields - 1*.

### 返回值

Returns an resource which contains field definition information or
**`FALSE`** if no field information for specified *fieldnr* is
available.

| Attribute   | Description                                        |
|-------------|----------------------------------------------------|
| name        | The name of the column                             |
| max\_length | The maximum width of the field for the result set. |
| type        | The data type used for this field                  |
| decimals    | The number of decimals used (for integer fields)   |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY name";

if ($result = $maxdb->query($query)) {

   /* Get field information for column 'SurfaceArea' */
   $finfo = $result->fetch_field_direct(1);

   printf("Name:     %s\n", $finfo->name);
   printf("Table:    %s\n", $finfo->table);
   printf("max. Len: %d\n", $finfo->max_length);
   printf("Flags:    %d\n", $finfo->flags);
   printf("Type:     %d\n", $finfo->type);

   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY name";

if ($result = maxdb_query($link, $query)) {

   /* Get field information for column 'cno' */
   $finfo = maxdb_fetch_field_direct($result, 1);

   printf("Name:     %s\n", $finfo->name);
   printf("Table:    %s\n", $finfo->table);
   printf("max. Len: %d\n", $finfo->max_length);
   printf("Flags:    %d\n", $finfo->flags);
   printf("Type:     %d\n", $finfo->type);

   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Name:     CNO
    Table:
    max. Len: 4
    Flags:    -1
    Type:     0

### 参见

-   <span class="function">maxdb\_num\_fields</span>
-   <span class="function">maxdb\_fetch\_field</span>
-   <span class="function">maxdb\_fetch\_fields</span>

maxdb\_fetch\_field
===================

maxdb\_result::fetch\_field
===========================

Returns the next field in the result set

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_fetch\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_result::fetch\_field</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_fetch\_field</span> returns the
definition of one column of a result set as an resource. Call this
function repeatedly to retrieve information about all columns in the
result set. <span class="function">maxdb\_fetch\_field</span> returns
**`FALSE`** when no more fields are left.

### 返回值

Returns an resource which contains field definition information or
**`FALSE`** if no field information is available.

| Property    | Description                                        |
|-------------|----------------------------------------------------|
| name        | The name of the column                             |
| max\_length | The maximum width of the field for the result set. |
| type        | The data type used for this field                  |
| decimals    | The number of decimals used (for integer fields)   |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = $maxdb->query($query)) {

   /* Get field information for all columns */
   while ($finfo = $result->fetch_field()) {

       printf("Name:     %s\n", $finfo->name);
       printf("Table:    %s\n", $finfo->table);
       printf("max. Len: %d\n", $finfo->max_length);
       printf("Flags:    %d\n", $finfo->flags);
       printf("Type:     %d\n\n", $finfo->type);
   }
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = maxdb_query($link, $query)) {

   /* Get field information for all fields */
   while ($finfo = maxdb_fetch_field($result)) {

       printf("Name:     %s\n", $finfo->name);
       printf("Table:    %s\n", $finfo->table);
       printf("max. Len: %d\n", $finfo->max_length);
       printf("Flags:    %d\n", $finfo->flags);
       printf("Type:     %d\n\n", $finfo->type);
   }
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Name:     NAME
    Table:
    max. Len: 10
    Flags:    -1
    Type:     2

    Name:     CNO
    Table:
    max. Len: 4
    Flags:    -1
    Type:     0

### 参见

-   <span class="function">maxdb\_num\_fields</span>
-   <span class="function">maxdb\_fetch\_field\_direct</span>
-   <span class="function">maxdb\_fetch\_fields</span>
-   <span class="function">maxdb\_field\_seek</span>

maxdb\_fetch\_fields
====================

maxdb\_result::fetch\_fields
============================

Returns an array of resources representing the fields in a result set

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_fetch\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_result::fetch\_fields</span> ( <span
class="methodparam">void</span> )

This function serves an identical purpose to the <span
class="function">maxdb\_fetch\_field</span> function with the single
difference that, instead of returning one resource at a time for each
field, the columns are returned as an array of resources.

### 返回值

Returns an array of resources which contains field definition
information or **`FALSE`** if no field information is available.

| Property    | Description                                        |
|-------------|----------------------------------------------------|
| name        | The name of the column                             |
| max\_length | The maximum width of the field for the result set. |
| type        | The data type used for this field                  |
| decimals    | The number of decimals used (for integer fields)   |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = $maxdb->query($query)) {

   /* Get field information for all columns */
   $finfo = $result->fetch_fields();

   foreach ($finfo as $val) {
       printf("Name:     %s\n", $val->name);
       printf("Table:    %s\n", $val->table);
       printf("max. Len: %d\n", $val->max_length);
       printf("Flags:    %d\n", $val->flags);
       printf("Type:     %d\n\n", $val->type);
   }
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = maxdb_query($link, $query)) {

   /* Get field information for all columns */
   $finfo = maxdb_fetch_fields($result);

   foreach ($finfo as $val) {
       printf("Name:     %s\n", $val->name);
       printf("Table:    %s\n", $val->table);
       printf("max. Len: %d\n", $val->max_length);
       printf("Flags:    %d\n", $val->flags);
       printf("Type:     %d\n\n", $val->type);
   }
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Name:     NAME
    Table:
    max. Len: 10
    Flags:    -1
    Type:     2

    Name:     CNO
    Table:
    max. Len: 4
    Flags:    -1
    Type:     0

### 参见

-   <span class="function">maxdb\_num\_fields</span>
-   <span class="function">maxdb\_fetch\_field</span>
-   <span class="function">maxdb\_fetch\_field\_direct</span>

maxdb\_fetch\_lengths
=====================

maxdb\_result::lengths
======================

Returns the lengths of the columns of the current row in the result set

### 说明

过程化风格

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">maxdb\_fetch\_lengths</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">array</span>`$maxdb_result->lengths`;

The <span class="function">maxdb\_fetch\_lengths</span> function returns
an array containing the lengths of every column of the current row
within the result set represented by the `result` parameter. If
successful, a numerically indexed array representing the lengths of each
column is returned 或者在失败时返回 **`FALSE`**.

### 返回值

An array of integers representing the size of each column (not including
any terminating null characters). **`FALSE`** if an error occurred.

<span class="function">maxdb\_fetch\_lengths</span> is valid only for
the current row of the result set. It returns **`FALSE`** if you call it
before calling maxdb\_fetch\_row/array/resource or after retrieving all
rows in the result.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT * from hotel.customer WHERE cno = 3000";

if ($result = $maxdb->query($query)) {

   $row = $result->fetch_row();

   /* display column lengths */
   foreach ($result->lengths as $i => $val) {
       printf("Field %2d has Length %2d\n", $i+1, $val);
   }
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT * from hotel.customer WHERE cno = 3000";

if ($result = maxdb_query($link, $query)) {

   $row = maxdb_fetch_row($result);

   /* display column lengths */
   foreach (maxdb_fetch_lengths($result) as $i => $val) {
       printf("Field %2d has Length %2d\n", $i+1, $val);
   }
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Field  1 has Length  4
    Field  2 has Length  3
    Field  3 has Length  5
    Field  4 has Length  6
    Field  5 has Length  5
    Field  6 has Length 21

maxdb\_fetch\_object
====================

maxdb\_result::fetch\_object
============================

Returns the current row of a result set as an object

### 说明

过程化风格

<span class="type">object</span> <span
class="methodname">maxdb\_fetch\_object</span> ( <span
class="methodparam"><span class="type">object</span> `$result`</span> )

面向对象风格

<span class="type">object</span> <span
class="methodname">maxdb\_result::fetch\_object</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_fetch\_object</span> will return the
current row result set as an object where the attributes of the object
represent the names of the fields found within the result set. If no
more rows exist in the current result set, **`NULL`** is returned.

### 返回值

Returns an object that corresponds to the fetched row or **`NULL`** if
there are no more rows in resultset.

> **Note**: <span
> class="simpara">此函数返回的字段名*大小写敏感*。</span>

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";

if ($result = $maxdb->query($query)) {

   /* fetch object array */
   while ($obj = $result->fetch_object()) {
       printf ("%s (%s)\n", $obj->NAME, $obj->STATE);
   }

   /* free result set */
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";

if ($result = maxdb_query($link, $query)) {

   /* fetch object array */
   while ($obj = maxdb_fetch_object($result)) {
       printf ("%s (%s)\n", $obj->NAME, $obj->STATE);
   }

   /* free result set */
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    New York (NY)
    New York (NY)
    Long Island (NY)
    Albany (NY)
    Washington (DC)
    Washington (DC)
    Washington (DC)
    Silver Spring (MD)
    Daytona Beach (FL)
    Deerfield Beach (FL)
    Clearwater (FL)
    Cincinnati (OH)
    Detroit (MI)
    Rosemont (IL)
    Chicago (IL)
    Chicago (IL)
    New Orleans (LA)
    Dallas (TX)
    Los Angeles (CA)
    Hollywood (CA)
    Long Beach (CA)
    Palm Springs (CA)
    Irvine (CA)
    Santa Clara (CA)
    Portland (OR)

### 参见

-   <span class="function">maxdb\_fetch\_array</span>
-   <span class="function">maxdb\_fetch\_assoc</span>
-   <span class="function">maxdb\_fetch\_row</span>

maxdb\_fetch\_row
=================

maxdb\_result::fetch\_row
=========================

Get a result row as an enumerated array

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_result::fetch\_row</span> ( <span
class="methodparam">void</span> )

Returns an array that corresponds to the fetched row, or **`NULL`** if
there are no more rows.

<span class="function">maxdb\_fetch\_row</span> fetches one row of data
from the result set represented by `result` and returns it as an
enumerated array, where each column is stored in an array offset
starting from 0 (zero). Each subsequent call to the <span
class="function">maxdb\_fetch\_row</span> function will return the next
row within the result set, or **`FALSE`** if there are no more rows.

### 返回值

<span class="function">maxdb\_fetch\_row</span> returns an array that
corresponds to the fetched row or **`NULL`** if there are no more rows
in result set.

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";

if ($result = $maxdb->query($query)) {

   /* fetch enumerated array */
   while ($row = $result->fetch_row()) {
       printf ("%s (%s)\n", $row[0], $row[1]);
   }

   /* free result set */
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, state FROM hotel.city ORDER by zip";

if ($result = maxdb_query($link, $query)) {

   /* fetch enumerated array */
   while ($row = maxdb_fetch_row($result)) {
       printf ("%s (%s)\n", $row[0], $row[1]);
   }

   /* free result set */
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    New York (NY)
    New York (NY)
    Long Island (NY)
    Albany (NY)
    Washington (DC)
    Washington (DC)
    Washington (DC)
    Silver Spring (MD)
    Daytona Beach (FL)
    Deerfield Beach (FL)
    Clearwater (FL)
    Cincinnati (OH)
    Detroit (MI)
    Rosemont (IL)
    Chicago (IL)
    Chicago (IL)
    New Orleans (LA)
    Dallas (TX)
    Los Angeles (CA)
    Hollywood (CA)
    Long Beach (CA)
    Palm Springs (CA)
    Irvine (CA)
    Santa Clara (CA)
    Portland (OR)

### 参见

-   <span class="function">maxdb\_fetch\_array</span>
-   <span class="function">maxdb\_fetch\_assoc</span>
-   <span class="function">maxdb\_fetch\_resource</span>

maxdb\_fetch
============

别名 <span class="function">maxdb\_stmt\_fetch</span>

### 说明

此函数是该函数的别名： <span class="function">maxdb\_stmt\_fetch</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_field\_count
===================

maxdb::field\_count
===================

Returns the number of columns for the most recent query

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_field\_count</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span> <span
class="methodname">maxdb::field\_count</span> ( <span
class="methodparam">void</span> )

Returns the number of columns for the most recent query on the
connection represented by the `link` parameter. This function can be
useful when using the <span class="function">maxdb\_store\_result</span>
function to determine if the query should have produced a non-empty
result set or not without knowing the nature of the query.

### 返回值

An integer representing the number of fields in a result set.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

maxdb_report (MAXDB_REPORT_OFF);
$maxdb->query("DROP TABLE friends");
maxdb_report (MAXDB_REPORT_ERROR);

$maxdb->query( "CREATE TABLE friends (id int, name varchar(20))");

$maxdb->query( "INSERT INTO friends VALUES (1,'Hartmut')");
$maxdb->query( "INSERT INTO friends VALUES (2, 'Ulf')");

if ($maxdb->field_count()) {
   /* this was a select/show or describe query */
   $result = $maxdb->store_result();

   /* process resultset */
   $row = $result->fetch_row();

   /* free resultset */
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

maxdb_report (MAXDB_REPORT_OFF);
maxdb_query($link,"DROP TABLE friends");
maxdb_report (MAXDB_REPORT_ERROR);

maxdb_query($link, "CREATE TABLE friends (id int, name varchar(20))");

maxdb_query($link, "INSERT INTO friends VALUES (1,'Hartmut')");
maxdb_query($link, "INSERT INTO friends VALUES (2, 'Ulf')");

if (maxdb_field_count($link)) {
   /* this was a select/show or describe query */
   $result = maxdb_store_result($link);

   /* process resultset */
   $row = maxdb_fetch_row($result);

   /* free resultset */
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

The above example produces no output.

maxdb\_field\_seek
==================

maxdb\_result::field\_seek
==========================

Set result pointer to a specified field offset

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_field\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$fieldnr`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_result::field\_seek</span> ( <span
class="methodparam"><span class="type">int</span> `$fieldnr`</span> )

Sets the field cursor to the given offset. The next call to <span
class="function">maxdb\_fetch\_field</span> will retrieve the field
definition of the column associated with that offset.

> **Note**:
>
> To seek to the beginning of a row, pass an offset value of zero.

### 返回值

<span class="function">maxdb\_field\_seek</span> returns previuos value
of field cursor.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = $maxdb->query($query)) {

   /* Get field information for 2nd column */
   $result->field_seek(1);
   $finfo = $result->fetch_field();

   printf("Name:     %s\n", $finfo->name);
   printf("Table:    %s\n", $finfo->table);
   printf("max. Len: %d\n", $finfo->max_length);
   printf("Flags:    %d\n", $finfo->flags);
   printf("Type:     %d\n\n", $finfo->type);

   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = maxdb_query($link, $query)) {

   /* Get field information for 2nd column */
   maxdb_field_seek($result, 1);
   $finfo = maxdb_fetch_field($result);

   printf("Name:     %s\n", $finfo->name);
   printf("Table:    %s\n", $finfo->table);
   printf("max. Len: %d\n", $finfo->max_length);
   printf("Flags:    %d\n", $finfo->flags);
   printf("Type:     %d\n\n", $finfo->type);

   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Name:     NAME
    Table:
    max. Len: 10
    Flags:    -1
    Type:     2

### 参见

-   <span class="function">maxdb\_fetch\_field</span>

maxdb\_field\_tell
==================

maxdb\_result::current\_field
=============================

Get current field offset of a result pointer

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_field\_tell</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">int</span>`$maxdb_result->current_field`;

Returns the position of the field cursor used for the last <span
class="function">maxdb\_fetch\_field</span> call. This value can be used
as an argument to <span class="function">maxdb\_field\_seek</span>.

### 返回值

Returns current offset of field cursor.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = $maxdb->query($query)) {

   /* Get field information for all columns */
   while ($finfo = $result->fetch_field()) {

       /* get fieldpointer offset */
       $currentfield = $result->current_field;

       printf("Column    %d:\n", $currentfield);
       printf("Name:     %s\n", $finfo->name);
       printf("Table:    %s\n", $finfo->table);
       printf("max. Len: %d\n", $finfo->max_length);
       printf("Flags:    %d\n", $finfo->flags);
       printf("Type:     %d\n\n", $finfo->type);
   }
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, cno from hotel.customer ORDER BY cno";

if ($result = maxdb_query($link, $query)) {

   /* Get field information for all fields */
   while ($finfo = maxdb_fetch_field($result)) {

       /* get fieldpointer offset */
       $currentfield = maxdb_field_tell($result);

       printf("Column    %d:\n", $currentfield);
       printf("Name:     %s\n", $finfo->name);
       printf("Table:    %s\n", $finfo->table);
       printf("max. Len: %d\n", $finfo->max_length);
       printf("Flags:    %d\n", $finfo->flags);
       printf("Type:     %d\n\n", $finfo->type);
   }
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Column    1:
    Name:     NAME
    Table:
    max. Len: 10
    Flags:    -1
    Type:     2

    Column    2:
    Name:     CNO
    Table:
    max. Len: 4
    Flags:    -1
    Type:     0

### 参见

-   <span class="function">maxdb\_fetch\_field</span>
-   <span class="function">maxdb\_field\_seek</span>

maxdb\_free\_result
===================

maxdb\_result::free
===================

Frees the memory associated with a result

### 说明

过程化风格

<span class="type">void</span> <span
class="methodname">maxdb\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">void</span> <span
class="methodname">maxdb\_result::free</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_free\_result</span> function frees the
memory associated with the result represented by the `result` parameter,
which was allocated by <span class="function">maxdb\_query</span>, <span
class="function">maxdb\_store\_result</span> or <span
class="function">maxdb\_use\_result</span>.

> **Note**:
>
> You should always free your result with <span
> class="function">maxdb\_free\_result</span>, when your result resource
> is not needed anymore.

### 返回值

This function doesn't return any value.

### 参见

-   <span class="function">maxdb\_query</span>
-   <span class="function">maxdb\_stmt\_store\_result</span>
-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_use\_result</span>

maxdb\_get\_client\_info
========================

Returns the MaxDB client version as a string

### 说明

<span class="type">string</span> <span
class="methodname">maxdb\_get\_client\_info</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_get\_client\_info</span> function is
used to return a string representing the client version being used in
the MaxDB extension.

### 返回值

A string that represents the MaxDB client library version

### 范例

**示例 \#1 maxdb\_get\_client\_info**

``` php
<?php

/* We don't need a connection to determine
   the version of MaxDB client library */

printf("Client library version: %s\n", maxdb_get_client_info());
?>
```

以上例程的输出类似于：

    Client library version: libSQLDBC <...>

### 参见

-   <span class="function">maxdb\_get\_client\_version</span>
-   <span class="function">maxdb\_get\_server\_info</span>
-   <span class="function">maxdb\_get\_server\_version</span>

maxdb\_get\_client\_version
===========================

Get MaxDB client info

### 说明

<span class="type">int</span> <span
class="methodname">maxdb\_get\_client\_version</span> ( <span
class="methodparam">void</span> )

Returns client version number as an integer.

### 返回值

A number that represents the MaxDB client library version in format:
*main\_version\*10000 + minor\_version \*100 + sub\_version*. For
example, 7.5.0 is returned as 70500.

This is useful to quickly determine the version of the client library to
know if some capability exists.

### 范例

**示例 \#1 maxdb\_get\_client\_version**

``` php
<?php

/* We don't need a connection to determine
   the version of MaxDB client library */

printf("Client library version: %d\n", maxdb_get_client_version());
?>
```

以上例程的输出类似于：

    Client library version: 7.<...>

### 参见

-   <span class="function">maxdb\_get\_client\_info</span>
-   <span class="function">maxdb\_get\_server\_info</span>
-   <span class="function">maxdb\_get\_server\_version</span>

maxdb\_get\_host\_info
======================

maxdb::get\_host\_info
======================

Returns a string representing the type of connection used

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_get\_host\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span>`$maxdb->host_info`;

The <span class="function">maxdb\_get\_host\_info</span> function
returns a string describing the connection represented by the `link`
parameter is using.

### 返回值

A character string representing the server hostname and the connection
type.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print host information */
printf("Host info: %s\n", $maxdb->host_info);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print host information */
printf("Host info: %s\n", maxdb_get_host_info($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Host info: localhost

### 参见

-   <span class="function">maxdb\_get\_proto\_info</span>

maxdb\_get\_metadata
====================

别名 <span class="function">maxdb\_stmt\_result\_metadata</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_result\_metadata</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_get\_proto\_info
=======================

maxdb::protocol\_version
========================

Returns the version of the MaxDB protocol used

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_get\_proto\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span>`$maxdb->protocol_version`;

Returns an integer representing the MaxDB protocol version used by the
connection represented by the `link` parameter.

### 返回值

Returns an integer representing the protocol version (constant 10).

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print protocol version */
printf("Protocol version: %d\n", $maxdb->protocol_version);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print protocol version */
printf("Protocol version: %d\n", maxdb_get_proto_info($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Protocol version: 10

### 参见

-   <span class="function">maxdb\_get\_host\_info</span>

maxdb\_get\_server\_info
========================

maxdb::server\_info
===================

Returns the version of the MaxDB server

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_get\_server\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span>`$maxdb->server_info`;

Returns a string representing the version of the MaxDB server that the
MaxDB extension is connected to (represented by the `link` parameter).

### 返回值

A character string representing the server version.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print server version */
printf("Server version: %s\n", $maxdb->server_info);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print server version */
printf("Server version: %s\n", maxdb_get_server_info($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Server version: Kernel    7<...>

### 参见

-   <span class="function">maxdb\_get\_client\_info</span>
-   <span class="function">maxdb\_get\_client\_version</span>
-   <span class="function">maxdb\_get\_server\_version</span>

maxdb\_get\_server\_version
===========================

maxdb::server\_version
======================

Returns the version of the MaxDB server as an integer

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_get\_server\_version</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span>`$maxdb->server_version`;

The <span class="function">maxdb\_get\_server\_version</span> function
returns the version of the server connected to (represented by the
`link` parameter) as an integer.

The form of this version number is *main\_version \* 10000 +
minor\_version \* 100 + sub\_version* (i.e. version 7.5.0 is 70500).

### 返回值

An integer representing the server version.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print server version */
printf("Server version: %d\n", $maxdb->server_version);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* print server version */
printf("Server version: %d\n", maxdb_get_server_version($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Server version: 7<...>

### 参见

-   <span class="function">maxdb\_get\_client\_info</span>
-   <span class="function">maxdb\_get\_client\_version</span>
-   <span class="function">maxdb\_get\_server\_info</span>

maxdb\_info
===========

maxdb::info
===========

Retrieves information about the most recently executed query

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_info</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span>`$maxdb->info`;

The <span class="function">maxdb\_info</span> function returns a string
providing information about the last query executed. The nature of this
string is provided below:

| Query type                             | Example result string                        |
|----------------------------------------|----------------------------------------------|
| INSERT INTO...SELECT...                | Records: 100 Duplicates: 0 Warnings: 0       |
| INSERT INTO...VALUES (...),(...),(...) | Records: 3 Duplicates: 0 Warnings: 0         |
| LOAD DATA INFILE ...                   | Records: 1 Deleted: 0 Skipped: 0 Warnings: 0 |
| ALTER TABLE ...                        | Records: 3 Duplicates: 0 Warnings: 0         |
| UPDATE ...                             | Rows matched: 40 Changed: 40 Warnings: 0     |

> **Note**:
>
> Queries which do not fall into one of the above formats are not
> supported. In these situations, <span
> class="function">maxdb\_info</span> will return an empty string.

### 返回值

A character string representing additional information about the most
recently executed query.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.t1 LIKE hotel.city");

/* INSERT INTO .. SELECT */
$maxdb->query("INSERT INTO temp.t1 SELECT * FROM hotel.city");
printf("%s\n", $maxdb->info);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.t1 LIKE hotel.city");

/* INSERT INTO .. SELECT */
maxdb_query($link, "INSERT INTO temp.t1 SELECT * FROM hotel.city");
printf("%s\n", maxdb_info($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Records: 25 Duplicates: 0 Warnings: 0

### 参见

-   <span class="function">maxdb\_affected\_rows</span>
-   <span class="function">maxdb\_warning\_count</span>
-   <span class="function">maxdb\_num\_rows</span>

maxdb\_init
===========

Initializes MaxDB and returns an resource for use with
maxdb\_real\_connect

### 说明

<span class="type">resource</span> <span
class="methodname">maxdb\_init</span> ( <span
class="methodparam">void</span> )

Allocates or initializes a MaxDB resource suitable for <span
class="function">maxdb\_options</span> and <span
class="function">maxdb\_real\_connect</span>.

> **Note**:
>
> Any subsequent calls to any maxdb function (except <span
> class="function">maxdb\_options</span>) will fail until <span
> class="function">maxdb\_real\_connect</span> was called.

### 返回值

Returns an resource.

### 参见

-   <span class="function">maxdb\_options</span>
-   <span class="function">maxdb\_close</span>
-   <span class="function">maxdb\_real\_connect</span>
-   <span class="function">maxdb\_connect</span>

maxdb\_insert\_id
=================

maxdb::insert\_id
=================

Returns the auto generated id used in the last query

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_insert\_id</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">mixed</span>`$maxdb->insert_id`;

The <span class="function">maxdb\_insert\_id</span> function returns the
ID generated by a query on a table with a column having the DEFAULT
SERIAL attribute. If the last query wasn't an INSERT or UPDATE statement
or if the modified table does not have a column with the DEFAULT SERIAL
attribute, this function will return zero.

### 返回值

The value of the *DEFAULT SERIAL* field that was updated by the previous
query. Returns zero if there was no previous query on the connection or
if the query did not update an *DEFAULT\_SERIAL* value.

> **Note**:
>
> If the number is greater than maximal int value, <span
> class="function">maxdb\_insert\_id</span> will return a string.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_report (MAXDB_REPORT_OFF);
$maxdb->query("DROP TABLE mycity");
maxdb_report (MAXDB_REPORT_ERROR);

$maxdb->query("CREATE TABLE mycity LIKE hotel.city");
$maxdb->query("ALTER TABLE mycity ADD id FIXED(11) DEFAULT SERIAL");

$query = "INSERT INTO mycity (zip,name,state) VALUES ('12203','Albany' ,'NY')";
$maxdb->query($query);

printf ("New Record has id %d.\n", $maxdb->insert_id);

/* drop table */
$maxdb->query("DROP TABLE mycity");

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_report (MAXDB_REPORT_OFF);
maxdb_query($link,"DROP TABLE mycity");
maxdb_report (MAXDB_REPORT_ERROR);

maxdb_query($link, "CREATE TABLE mycity LIKE hotel.city");
maxdb_query($link, "ALTER TABLE mycity ADD id FIXED(11) DEFAULT SERIAL");

$query = "INSERT INTO mycity (zip,name,state) VALUES ('12203','Albany' ,'NY')";
maxdb_query($link, $query);

printf ("New Record has id %d.\n", maxdb_insert_id($link));

/* drop table */
maxdb_query($link, "DROP TABLE mycity");

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    New Record has id 1.

maxdb\_kill
===========

maxdb::kill
===========

Disconnects from a MaxDB server

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_kill</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">int</span> `$processid`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::kill</span> ( <span class="methodparam"><span
class="type">int</span> `$processid`</span> )

This function is used to disconnect from a MaxDB server specified by the
`processid` parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* determine our thread id */
$thread_id = $maxdb->thread_id;

/* Kill connection */
$maxdb->kill($thread_id);

/* This should produce an error */
if (!$maxdb->query("CREATE TABLE myCity LIKE City")) {
   printf("Error: %s\n", $maxdb->error);
   exit;
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* determine our thread id */
$thread_id = maxdb_thread_id($link);

/* Kill connection */
maxdb_kill($link, $thread_id);

/* This should produce an error */
if (!maxdb_query($link, "CREATE TABLE myCity LIKE City")) {
   printf("Error: %s\n", maxdb_error($link));
   exit;
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Error: Session not connected

### 参见

-   <span class="function">maxdb\_thread\_id</span>

maxdb\_master\_query
====================

Enforce execution of a query on the master in a master/slave setup

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_master\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_more\_results
====================

maxdb::more\_results
====================

Check if there any more query results from a multi query

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_more\_results</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">maxdb\_more\_results</span> indicates if one or
more result sets are available from a previous call to <span
class="function">maxdb\_multi\_query</span>.

### 返回值

Always **`FALSE`**.

### 范例

See <span class="function">maxdb\_multi\_query</span>.

### 参见

-   <span class="function">maxdb\_multi\_query</span>
-   <span class="function">maxdb\_next\_result</span>
-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_use\_result</span>

maxdb\_multi\_query
===================

maxdb::multi\_query
===================

Performs a query on the database

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_multi\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::multi\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

The <span class="function">maxdb\_multi\_query</span> works like the
function <span class="function">maxdb\_query</span>. Multiple queries
are not yet supported.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query  = "SELECT * FROM dual";

/* execute multi query */
if ($maxdb->multi_query($query)) {
   do {
       /* store first result set */
       if ($result = $maxdb->store_result()) {
           while ($row = $result->fetch_row()) {
               printf("%s\n", $row[0]);
           }
           $result->close();
       }
       /* print divider */
       if ($maxdb->more_results()) {
           printf("-----------------\n");
       }
   } while ($maxdb->next_result());
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT * FROM dual";

/* execute multi query */
if (maxdb_multi_query($link, $query)) {
   do {
       /* store first result set */
       if ($result = maxdb_store_result($link)) {
           while ($row = maxdb_fetch_row($result)) {
               printf("%s\n", $row[0]);
           }
           maxdb_free_result($result);
       }
       /* print divider */
       if (maxdb_more_results($link)) {
           printf("-----------------\n");
       }
   } while (maxdb_next_result($link));
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    a

### 参见

-   <span class="function">maxdb\_use\_result</span>
-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_next\_result</span>
-   <span class="function">maxdb\_more\_results</span>

maxdb\_next\_result
===================

maxdb::next\_result
===================

Prepare next result from multi\_query

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

Since multiple queries are not yet supported, <span
class="function">maxdb\_next\_result</span> returns always **`FALSE`**.

### 返回值

Returns **`FALSE`**.

### 参见

-   <span class="function">maxdb\_multi\_query</span>
-   <span class="function">maxdb\_more\_results</span>
-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_use\_result</span>

maxdb\_num\_fields
==================

maxdb\_result::field\_count
===========================

Get the number of fields in a result

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">int</span>`$maxdb_result->field_count`;

<span class="function">maxdb\_num\_fields</span> returns the number of
fields from specified result set.

### 返回值

The number of fields from a result set

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($result = $maxdb->query("SELECT * FROM hotel.city ORDER BY zip")) {

   /* determine number of fields in result set */
   $field_cnt = $result->field_count;

   printf("Result set has %d fields.\n", $field_cnt);

   /* close result set */
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($result = maxdb_query($link, "SELECT * FROM hotel.city ORDER BY zip")) {

   /* determine number of fields in result set */
   $field_cnt = maxdb_num_fields($result);

   printf("Result set has %d fields.\n", $field_cnt);

   /* close result set */
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Result set has 3 fields.

### 参见

-   <span class="function">maxdb\_fetch\_field</span>

maxdb\_num\_rows
================

maxdb::num\_rows
================

Gets the number of rows in a result

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

面向对象风格

<span class="type">int</span>`$maxdb->num_rows`;

Returns the number of rows in the result set.

The use of <span class="function">maxdb\_num\_rows</span> depends on
whether you use buffered or unbuffered result sets. In case you use
unbuffered resultsets <span class="function">maxdb\_num\_rows</span>
will not correct the correct number of rows until all the rows in the
result have been retrieved.

### 返回值

Returns number of rows in the result set.

> **Note**:
>
> If the number of rows is greater than maximal int value, the number
> will be returned as a string.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($result = $maxdb->query("SELECT cno, name FROM hotel.customer ORDER BY name")) {

   /* determine number of rows result set */
   $row_cnt = $result->num_rows;

   printf("Result set has %d rows.\n", $row_cnt);

   /* close result set */
   $result->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($result = maxdb_query($link, "SELECT cno, name FROM hotel.customer ORDER BY name")) {

   /* determine number of rows result set */
   $row_cnt = maxdb_num_rows($result);

   printf("Result set has %d rows.\n", $row_cnt);

   /* close result set */
   maxdb_free_result($result);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Result set has 15 rows.

### 参见

-   <span class="function">maxdb\_affected\_rows</span>
-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_use\_result</span>
-   <span class="function">maxdb\_query</span>

maxdb\_options
==============

maxdb::options
==============

Set options

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_options</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">int</span> `$option`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::options</span> ( <span
class="methodparam"><span class="type">int</span> `$option`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="function">maxdb\_options</span> can be used to set extra
connect options and affect behavior for a connection.

This function may be called multiple times to set several options.

<span class="function">maxdb\_options</span> should be called after
<span class="function">maxdb\_init</span> and before <span
class="function">maxdb\_real\_connect</span>.

The parameter `option` is the option that you want to set, the `value`
is the value for the option. For detailed description of the options see
<a href="http://maxdb.sap.com/documentation/" class="link external">» http://maxdb.sap.com/documentation/</a>
The parameter `option` can be one of the following values:

| Name                           | Description                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------|
| **`MAXDB_COMPNAME`**           | The component name used to initialise the SQLDBC runtime environment.                                      |
| **`MAXDB_APPLICATION`**        | The application to be connected to the database.                                                           |
| **`MAXDB_APPVERSION`**         | The version of the application.                                                                            |
| **`MAXDB_SQLMODE`**            | The SQL mode.                                                                                              |
| **`MAXDB_UNICODE`**            | TRUE, if the connection is an unicode (UCS2) client or FALSE, if not.                                      |
| **`MAXDB_TIMEOUT`**            | The maximum allowed time of inactivity after which the connection to the database is closed by the system. |
| **`MAXDB_ISOLATIONLEVEL`**     | Specifies whether and how shared locks and exclusive locks are implicitly requested or released.           |
| **`MAXDB_PACKETCOUNT`**        | The number of different request packets used for the connection.                                           |
| **`MAXDB_STATEMENTCACHESIZE`** | The number of prepared statements to be cached for the connection for re-use.                              |
| **`MAXDB_CURSORPREFIX`**       | The prefix to use for result tables that are automatically named.                                          |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

See <span class="function">maxdb\_real\_connect</span>.

### 参见

-   <span class="function">maxdb\_init</span>
-   <span class="function">maxdb\_real\_connect</span>

maxdb\_param\_count
===================

别名 <span class="function">maxdb\_stmt\_param\_count</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_param\_count</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_ping
===========

maxdb::ping
===========

Pings a server connection, or tries to reconnect if the connection has
gone down

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_ping</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::ping</span> ( <span
class="methodparam">void</span> )

Checks whether the connection to the server is working. If it has gone
down, and global option *maxdb.reconnect* is enabled an automatic
reconnection is attempted.

This function can be used by clients that remain idle for a long while,
to check whether the server has closed the connection and reconnect if
necessary.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* check if server is alive */
if ($maxdb->ping()) {
   printf ("Our connection is ok!\n");
} else {
   printf ("Error: %s\n", $maxdb->error);
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* check if server is alive */
if (maxdb_ping($link)) {
   printf ("Our connection is ok!\n");
} else {
   printf ("Error: %s\n", maxdb_error($link));
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Our connection is ok!

maxdb\_prepare
==============

maxdb::prepare
==============

Prepare an SQL statement for execution

### 说明

过程化风格

<span class="type">resource</span> <span
class="methodname">maxdb\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

面向对象风格

<span class="type">maxdb\_stmt</span> <span
class="methodname">maxdb::prepare</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

<span class="function">maxdb\_prepare</span> prepares the SQL query
pointed to by the null-terminated string query, and returns a statement
handle to be used for further operations on the statement. The query
must consist of a single SQL statement.

> **Note**:
>
> You should not add a terminating semicolon or *\\g* to the statement.

The parameter `query` can include one or more parameter markers in the
SQL statement by embedding question mark (*?*) characters at the
appropriate positions.

> **Note**:
>
> The markers are legal only in certain places in SQL statements. For
> example, they are allowed in the VALUES() list of an INSERT statement
> (to specify column values for a row), or in a comparison with a column
> in a WHERE clause to specify a comparison value.
>
> However, they are not allowed for identifiers (such as table or column
> names), in the select list that names the columns to be returned by a
> SELECT statement), or to specify both operands of a binary operator
> such as the *=* equal sign. The latter restriction is necessary
> because it would be impossible to determine the parameter type. In
> general, parameters are legal only in Data Manipulation Languange
> (DML) statements, and not in Data Defination Language (DDL)
> statements.

The parameter markers must be bound to application variables using <span
class="function">maxdb\_stmt\_bind\_param</span> and/or <span
class="function">maxdb\_stmt\_bind\_result</span> before executing the
statement or fetching rows.

### 返回值

<span class="function">maxdb\_prepare</span> returns a statement
resource or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$city = "Rosemont";

/* create a prepared statement */
if ($stmt = $maxdb->prepare("SELECT state FROM hotel.city WHERE name=?")) {

   /* bind parameters for markers */
   $stmt->bind_param("s", $city);

   /* execute query */
   $stmt->execute();

   /* bind result variables */
   $stmt->bind_result($district);

   /* fetch value */
   $stmt->fetch();

   printf("%s is in district %s\n", $city, $district);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$city = "Rosemont";

/* create a prepared statement */
if ($stmt = maxdb_prepare($link, "SELECT state FROM hotel.city WHERE name=?")) {

   /* bind parameters for markers */
   maxdb_stmt_bind_param($stmt, "s", $city);

   /* execute query */
   maxdb_stmt_execute($stmt);

  /* bind result variables */
   maxdb_stmt_bind_result($stmt, $district);

   /* fetch value */
   maxdb_stmt_fetch($stmt);

   printf("%s is in district %s\n", $city, $district);

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Rosemont is in district IL

### 参见

-   <span class="function">maxdb\_stmt\_execute</span>
-   <span class="function">maxdb\_stmt\_fetch</span>
-   <span class="function">maxdb\_stmt\_bind\_param</span>
-   <span class="function">maxdb\_stmt\_bind\_result</span>
-   <span class="function">maxdb\_stmt\_close</span>

maxdb\_query
============

maxdb::query
============

Performs a query on the database

### 说明

过程化风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_query</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$resultmode`</span> \] )

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb::query</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> )

The <span class="function">maxdb\_query</span> function is used to
simplify the act of performing a query against the database represented
by the `link` parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 For *SELECT,
SHOW, DESCRIBE* or *EXPLAIN* <span class="function">maxdb\_query</span>
will return a result resource.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Create table doesn't return a resultset */
if ($maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city") === TRUE) {
   printf("Table mycity successfully created.\n");
}

/* Select queries return a resultset */
if ($result = $maxdb->query("SELECT name FROM hotel.city")) {
   printf("Select returned %d rows.\n", $result->num_rows);

   /* free result set */
   $result->close();
}

/* If we have to retrieve large amount of data we use MAXDB_USE_RESULT */
if ($result = $maxdb->query("SELECT * FROM hotel.city", MAXDB_USE_RESULT)) {
   $result->close();
}

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Create table doesn't return a resultset */
if (maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city") === TRUE) {
   printf("Table mycity successfully created.\n");
}

/* Select queries return a resultset */
if ($result = maxdb_query($link, "SELECT name FROM hotel.city")) {
   printf("Select returned %d rows.\n", maxdb_num_rows($result));

   /* free result set */
   maxdb_free_result($result);
}

/* If we have to retrieve large amount of data we use MAXDB_USE_RESULT */
if ($result = maxdb_query($link, "SELECT * FROM hotel.city", MAXDB_USE_RESULT)) {
   maxdb_free_result($result);
}

maxdb_close($link);
?>
```

以上例程的输出类似于：

    Table mycity successfully created.
    Select returned 25 rows.

### 参见

-   <span class="function">maxdb\_real\_query</span>
-   <span class="function">maxdb\_multi\_query</span>
-   <span class="function">maxdb\_free\_result</span>

maxdb\_real\_connect
====================

maxdb::real\_connect
====================

Opens a connection to a MaxDB server

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_real\_connect</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$hostname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$username`</span> \[, <span
class="methodparam"><span class="type">string</span> `$passwd`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$dbname`</span> \[, <span class="methodparam"><span
class="type">int</span> `$port`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$socket`</span> \]\]\]\]\]\] )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::real\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passwd`</span> \[, <span
class="methodparam"><span class="type">string</span> `$dbname`</span>
\[, <span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$socket`</span>
\]\]\]\]\]\] )

<span class="function">maxdb\_real\_connect</span> attempts to establish
a connection to a MaxDB database engine running on `hostname`.

This function differs from <span class="function">maxdb\_connect</span>:

-   <span class="function">maxdb\_real\_connect</span> needs a valid
    resource which has to be created by function <span
    class="function">maxdb\_init</span>

-   With function <span class="function">maxdb\_options</span> you can
    set various options for connection.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* create a connection object which is not connected */
$maxdb = maxdb_init();

/* set connection options */
$maxdb->options(MAXDB_UNICODE, "FALSE");
$maxdb->options(MAXDB_TIMEOUT, 5);

/* connect to server */
$maxdb->real_connect('localhost', 'MONA', 'RED', 'DEMODB');

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

printf ("Connection: %s\n.", $maxdb->host_info);

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php

/* create a connection object which is not connected */
$link = maxdb_init();

/* set connection options */
maxdb_options($link, MAXDB_UNICODE, "FALSE");
maxdb_options($link, MAXDB_TIMEOUT, 5);

/* connect to server */
maxdb_real_connect($link, 'localhost', 'MONA', 'RED', 'DEMODB');

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

printf ("Connection: %s\n.", maxdb_get_host_info($link));

maxdb_close($link);
?>
```

以上例程的输出类似于：

    Connection: localhost <...>

### 参见

-   <span class="function">maxdb\_connect</span>
-   <span class="function">maxdb\_init</span>
-   <span class="function">maxdb\_options</span>
-   <span class="function">maxdb\_ssl\_set</span>
-   <span class="function">maxdb\_close</span>

maxdb\_real\_escape\_string
===========================

maxdb::real\_escape\_string
===========================

Escapes special characters in a string for use in an SQL statement,
taking into account the current charset of the connection

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_real\_escape\_string</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$escapestr`</span> )

面向对象风格

<span class="type">string</span> <span
class="methodname">maxdb::real\_escape\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$escapestr`</span>
)

This function is used to create a legal SQL string that you can use in
an SQL statement. The string *escapestr* is encoded to an escaped SQL
string, taking into account the current character set of the connection.

Characters encoded are *', "*.

### 返回值

Returns an escaped string.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");

$city = "'s Hertogenbosch";

/* this query will fail, cause we didn't escape $city */
if (!$maxdb->query("INSERT into temp.mycity VALUES ('11111','$city','NY')")) {
   printf("Error: %s\n", $maxdb->sqlstate);
}

$city = $maxdb->real_escape_string($city);

/* this query with escaped $city will work */
if ($maxdb->query("INSERT into temp.mycity VALUES ('22222','$city','NY')")) {
   printf("%d Row inserted.\n", $maxdb->affected_rows);
}

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");

$city = "'s Hertogenbosch";

/* this query will fail, cause we didn't escape $city */
if (!maxdb_query($link, "INSERT into temp.mycity VALUES ('11111','$city','NY')")) {
   printf("Error: %s\n", maxdb_sqlstate($link));
}

$city = maxdb_real_escape_string($link, $city);

/* this query with escaped $city will work */
if (maxdb_query($link, "INSERT into temp.mycity VALUES ('22222','$city','NY')")) {
   printf("%d Row inserted.\n", maxdb_affected_rows($link));
}

maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_query(): -5016 POS(43) Missing delimiter: ) <...>
    Error: 42000
    1 Row inserted.

### 参见

-   <span class="function">maxdb\_character\_set\_name</span>

maxdb\_real\_query
==================

maxdb::real\_query
==================

Execute an SQL query

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_real\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::real\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

The <span class="function">maxdb\_real\_query</span> is functionally
identical with the <span class="function">maxdb\_query</span>.

> **Note**:
>
> In order to determine if a given query should return a result set or
> not, see <span class="function">maxdb\_field\_count</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">maxdb\_query</span>
-   <span class="function">maxdb\_store\_result</span>
-   <span class="function">maxdb\_use\_result</span>

maxdb\_report
=============

Enables or disables internal report functions

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_report</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

### 参数

`flags`  
One of the *MAXDB\_REPORT\_XXX* constants.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 过程化风格**

``` php
<?php
/* activate reporting */
maxdb_report(MAXDB_REPORT_ERROR);

$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* this query should report an error */
$result = maxdb_query($link,"SELECT Name FROM Nonexistingtable WHERE population > 50000");

maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_query(): -4004 POS(18) Unknown table name:NONEXISTINGTABLE <...>

maxdb\_rollback
===============

maxdb::rollback
===============

Rolls back current transaction

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_rollback</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::rollback</span> ( <span
class="methodparam">void</span> )

Rollbacks the current transaction for the database specified by the
`link` parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* disable autocommit */
$maxdb->autocommit(FALSE);

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");
$maxdb->query("INSERT INTO temp.mycity SELECT * FROM hotel.city");

/* commit insert */
$maxdb->commit();

/* delete all rows */
$maxdb->query("DELETE FROM temp.mycity");

if ($result = $maxdb->query("SELECT COUNT(*) FROM temp.mycity")) {
   $row = $result->fetch_row();
   printf("%d rows in table mycity.\n", $row[0]);
   /* Free result */
   $result->close();
}

/* Rollback */
$maxdb->rollback();

if ($result = $maxdb->query("SELECT COUNT(*) FROM temp.mycity")) {
   $row = $result->fetch_row();
   printf("%d rows in table mycity (after rollback).\n", $row[0]);
   /* Free result */
   $result->close();
}

/* Drop table myCity */
$maxdb->query("DROP TABLE temp.mycity");

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* disable autocommit */
maxdb_autocommit($link, FALSE);

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");
maxdb_query($link, "INSERT INTO temp.mycity SELECT * FROM hotel.city");

/* commit insert */
maxdb_commit($link);

/* delete all rows */
maxdb_query($link, "DELETE FROM temp.mycity");

if ($result = maxdb_query($link, "SELECT COUNT(*) FROM temp.mycity")) {
   $row = maxdb_fetch_row($result);
   printf("%d rows in table mycity.\n", $row[0]);
   /* Free result */
   maxdb_free_result($result);
}

/* Rollback */
maxdb_rollback($link);

if ($result = maxdb_query($link, "SELECT COUNT(*) FROM temp.mycity")) {
   $row = maxdb_fetch_row($result);
   printf("%d rows in table mycity (after rollback).\n", $row[0]);
   /* Free result */
   maxdb_free_result($result);
}

/* Drop table myCity */
maxdb_query($link, "DROP TABLE temp.mycity");

maxdb_close($link);
?>
```

以上例程的输出类似于：

    0 rows in table mycity.
    25 rows in table mycity (after rollback).

### 参见

-   <span class="function">maxdb\_commit</span>
-   <span class="function">maxdb\_autocommit</span>

maxdb\_rpl\_parse\_enabled
==========================

Check if RPL parse is enabled

### 说明

<span class="type">int</span> <span
class="methodname">maxdb\_rpl\_parse\_enabled</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_rpl\_probe
=================

RPL probe

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_rpl\_probe</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_rpl\_query\_type
=======================

maxdb::rpl\_query\_type
=======================

Returns RPL query type

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_rpl\_query\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span> <span
class="methodname">maxdb::rpl\_query\_type</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_select\_db
=================

maxdb::select\_db
=================

Selects the default database for database queries

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_select\_db</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dbname`</span> )

The <span class="function">maxdb\_select\_db</span> function selects the
default database (specified by the `dbname` parameter) to be used when
performing queries against the database connection represented by the
`link` parameter.

> **Note**:
>
> This function should only be used to change the default database for
> the connection. You can select the default database with 4th parameter
> in <span class="function">maxdb\_connect</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* return name of current default database */
if ($result = $maxdb->query("SELECT SERVERDB FROM USERS WHERE USERNAME='MONA'")) {
   $row = $result->fetch_row();
   printf("Default database is %s.\n", $row[0]);
   $result->close();
}

/* change db to non existing db */
$maxdb->select_db("XXXXXXXX");

/* return name of current default database */
if ($result = $maxdb->query("SELECT SERVERDB FROM USERS WHERE USERNAME='MONA'")) {
   $row = $result->fetch_row();
   printf("Default database is %s.\n", $row[0]);
   $result->close();
}

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* return name of current default database */
if ($result = maxdb_query($link, "SELECT SERVERDB FROM USERS WHERE USERNAME='MONA'")) {
   $row = maxdb_fetch_row($result);
   printf("Default database is %s.\n", $row[0]);
   maxdb_free_result($result);
}

/* change db to non existing db */
maxdb_select_db($link, "XXXXXXXX");

/* return name of current default database */
if ($result = maxdb_query($link, "SELECT SERVERDB FROM USERS WHERE USERNAME='MONA'")) {
   $row = maxdb_fetch_row($result);
   printf("Default database is %s.\n", $row[0]);
   maxdb_free_result($result);
}

maxdb_close($link);
?>
```

以上例程的输出类似于：

    Default database is <...>.

    Warning: maxdb_select_db(): -10709 Connection failed (RTE:database not running) <...>

    Warning: maxdb_query(): -10821 Session not connected [] <...>

    Warning: maxdb_close(): -10821 Session not connected [] <...>

### 参见

-   <span class="function">maxdb\_connect</span>
-   <span class="function">maxdb\_real\_connect</span>

maxdb\_send\_long\_data
=======================

别名 <span class="function">maxdb\_stmt\_send\_long\_data</span>

### 说明

此函数是该函数的别名： <span
class="function">maxdb\_stmt\_send\_long\_data</span>.

此函数别名已废弃，仅为了向后兼容而保留。不建议使用此函数，因为将来会从
PHP 中移除。

maxdb\_send\_query
==================

maxdb::send\_query
==================

Send the query and return

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_send\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::send\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_server\_end
==================

Shut down the embedded server

### 说明

<span class="type">void</span> <span
class="methodname">maxdb\_server\_end</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_server\_init
===================

Initialize embedded server

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_server\_init</span> (\[ <span
class="methodparam"><span class="type">array</span> `$server`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$groups`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_set\_opt
===============

别名 <span class="function">maxdb\_options</span>

### 说明

此函数是该函数的别名： <span class="function">maxdb\_options</span>.

maxdb\_sqlstate
===============

maxdb::sqlstate
===============

Returns the SQLSTATE error from previous MaxDB operation

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_sqlstate</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span>`$maxdb->sqlstate`;

Returns a string containing the SQLSTATE error code for the last error.
The error code consists of five characters. *'00000'* means no error.
The values are specified by ANSI SQL and ODBC.

> **Note**:
>
> Note that not all MaxDB errors are yet mapped to SQLSTATE's. The value
> *HY000* (general error) is used for unmapped errors.

### 返回值

Returns a string containing the SQLSTATE error code for the last error.
The error code consists of five characters. *'00000'* means no error.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Table City already exists, so we should get an error */
if (!$maxdb->query("CREATE TABLE hotel.city (ID INT, Name VARCHAR(30))")) {
   printf("Error - SQLSTATE %s.\n", $maxdb->sqlstate);
}

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Table City already exists, so we should get an error */
if (!maxdb_query($link, "CREATE TABLE hotel.city (ID INT, Name VARCHAR(30))")) {
   printf("Error - SQLSTATE %s.\n", maxdb_sqlstate($link));
}

maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_query(): -6000 POS(20) Duplicate table name:CITY [I6000] <...>
    Error - SQLSTATE I6000.

### 参见

-   <span class="function">maxdb\_errno</span>
-   <span class="function">maxdb\_error</span>

maxdb\_ssl\_set
===============

maxdb::ssl\_set
===============

Used for establishing secure connections using SSL

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_ssl\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$cert`</span> , <span class="methodparam"><span
class="type">string</span> `$ca`</span> , <span
class="methodparam"><span class="type">string</span> `$capath`</span> ,
<span class="methodparam"><span class="type">string</span>
`$cipher`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb::ssl\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$cert`</span> , <span class="methodparam"><span
class="type">string</span> `$ca`</span> , <span
class="methodparam"><span class="type">string</span> `$capath`</span> ,
<span class="methodparam"><span class="type">string</span>
`$cipher`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_stat
===========

maxdb::stat
===========

Gets the current system status

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_stat</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">string</span> <span
class="methodname">maxdb::stat</span> ( <span
class="methodparam">void</span> )

<span class="function">maxdb\_stat</span> returns a string containing
several information about the MaxDB server running.

### 返回值

A string describing the server status. **`FALSE`** if an error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

printf ("System status: %s\n", $maxdb->stat());

$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

printf("System status: %s\n", maxdb_stat($link));

maxdb_close($link);
?>
```

以上例程的输出类似于：

    System status: Kernel    7<...>

### 参见

-   <span class="function">maxdb\_get\_server\_info</span>

maxdb\_stmt\_affected\_rows
===========================

maxdb\_stmt::affected\_rows
===========================

Returns the total number of rows changed, deleted, or inserted by the
last executed statement

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_stmt\_affected\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">int</span>`$maxdb_stmt->affected_rows`;

<span class="function">maxdb\_stmt\_affected\_rows</span> returns the
number of rows affected by INSERT, UPDATE, or DELETE query. If the last
query was invalid or the number of rows can not determined, this
function will return -1.

### 返回值

An integer greater than zero indicates the number of rows affected or
retrieved. Zero indicates that no records where updated for an
UPDATE/DELETE statement, no rows matched the WHERE clause in the query
or that no query has yet been executed. -1 indicates that the query has
returned an error or the number of rows can not determined.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* create temp table */
$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");

$query = "INSERT INTO temp.mycity SELECT * FROM hotel.city WHERE state LIKE ?";

/* prepare statement */
if ($stmt = $maxdb->prepare($query)) {

   /* Bind variable for placeholder */
   $code = 'N%';
   $stmt->bind_param("s", $code);

   /* execute statement */
   $stmt->execute();

   printf("rows inserted: %d\n", $stmt->affected_rows);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* create temp table */
maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");

$query = "INSERT INTO temp.mycity SELECT * FROM hotel.city WHERE state LIKE ?";

/* prepare statement */
if ($stmt = maxdb_prepare($link, $query)) {

   /* Bind variable for placeholder */
   $code = 'N%';
   maxdb_stmt_bind_param($stmt, "s", $code);

   /* execute statement */
   maxdb_stmt_execute($stmt);

   printf("rows inserted: %d\n", maxdb_stmt_affected_rows($stmt));

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    rows inserted: 4

### 参见

-   <span class="function">maxdb\_stmt\_num\_rows</span>
-   <span class="function">maxdb\_prepare</span>

maxdb\_stmt\_bind\_param
========================

maxdb\_stmt::bind\_param
========================

Binds variables to a prepared statement as parameters

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_bind\_param</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">string</span>
`$types`</span> , <span class="methodparam"><span
class="type">mixed</span> `&$var1`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$...`</span> \] )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::bind\_param</span> ( <span
class="methodparam"><span class="type">string</span> `$types`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`&$var1`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `&$...`</span> \] )

过程化风格 (extended syntax):

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_bind\_param</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">string</span>
`$types`</span> , <span class="methodparam"><span
class="type">array</span> `&$var`</span> )

面向对象风格 (extended syntax):

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::bind\_param</span> ( <span
class="methodparam"><span class="type">string</span> `$types`</span> ,
<span class="methodparam"><span class="type">array</span> `&$var`</span>
)

<span class="function">maxdb\_stmt\_bind\_param</span> is used to bind
variables for the parameter markers in the SQL statement that was passed
to <span class="function">maxdb\_prepare</span>. The string `types`
contains one or more characters which specify the types for the
corresponding bind variables.

The extended syntax of <span
class="function">maxdb\_stmt\_bind\_param</span> allows to give the
parameters as an array instead of a variable list of PHP variables to
the function. If the array variable has not been used before calling
<span class="function">maxdb\_stmt\_bind\_param</span>, it has to be
initialized as an emtpy array. See the examples how to use <span
class="function">maxdb\_stmt\_bind\_param</span> with extended syntax.

Variables for SELECT INTO SQL statements can also be bound using <span
class="function">maxdb\_stmt\_bind\_param</span>. Parameters for
database procedures can be bound using <span
class="function">maxdb\_stmt\_bind\_param</span>. See the examples how
to use <span class="function">maxdb\_stmt\_bind\_param</span> in this
cases.

If a variable bound as INTO variable to an SQL statement was used
before, the content of this variable is overwritten by the data of the
SELECT INTO statement. A reference to this variable will be invalid
after a call to <span class="function">maxdb\_stmt\_bind\_param</span>.

For INOUT parameters of database procedures the content of the bound
INOUT variable is overwritten by the output value of the database
procedure. A reference to this variable will be invalid after a call to
<span class="function">maxdb\_stmt\_bind\_param</span>.

| Character | Description                                                   |
|-----------|---------------------------------------------------------------|
| i         | corresponding variable has type integer                       |
| d         | corresponding variable has type double                        |
| s         | corresponding variable has type string                        |
| b         | corresponding variable is a blob and will be sent in packages |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb('localhost', 'MONA', 'RED', 'DEMODB');

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query ("CREATE TABLE temp.mycity LIKE hotel.city");
$maxdb->query ("INSERT INTO temp.mycity SELECT * FROM hotel.city");

$stmt = $maxdb->prepare("INSERT INTO temp.mycity VALUES (?, ?, ?)");
$stmt->bind_param('sss', $zip, $name, $state);

$zip = '11111';
$name = 'Georgetown';
$state = 'NY';

/* execute prepared statement */
$stmt->execute();

printf("%d Row inserted.\n", $stmt->affected_rows);

/* close statement and connection */
$stmt->close();

/* Clean up table CountryLanguage */
$maxdb->query("DELETE FROM temp.mycity WHERE name='Georgetown'");
printf("%d Row deleted.\n", $maxdb->affected_rows);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query ($link, "CREATE TABLE temp.mycity LIKE hotel.city");
maxdb_query ($link, "INSERT INTO temp.mycity SELECT * FROM hotel.city");

$stmt = maxdb_prepare($link, "INSERT INTO temp.mycity VALUES (?, ?, ?)");
maxdb_stmt_bind_param($stmt, 'sss', $zip, $name, $state);

$zip = '11111';
$name = 'Georgetown';
$state = 'NY';

/* execute prepared statement */
maxdb_stmt_execute($stmt);

printf("%d Row inserted.\n", maxdb_stmt_affected_rows($stmt));

/* close statement and connection */
maxdb_stmt_close($stmt);

/* Clean up table CountryLanguage */
maxdb_query($link, "DELETE FROM temp.mycity WHERE name='Georgetown'");
printf("%d Row deleted.\n", maxdb_affected_rows($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    1 Row inserted.
    1 Row deleted.

**示例 \#3 过程化风格 (SELECT INTO)**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* Performing SQL query */
$stmt = maxdb_prepare ($link, "SELECT price INTO ? FROM hotel.room where hno = ? and type = ?");
if (!$stmt) {
  printf ("Prepare failed: %s\n", maxdb_error($link));
}

$hno = "50";
$rtype = "suite";

maxdb_stmt_bind_param($stmt, 'dss', $price, $hno, $rtype);
maxdb_stmt_execute($stmt);

printf ("%f\n", $price);

maxdb_stmt_close ($stmt);
?>
```

以上例程的输出类似于：

    21.600000

**示例 \#4 过程化风格 (DB procedure)**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_report (MAXDB_REPORT_OFF);
maxdb_query($link,"DROP DBPROC test_proc");
maxdb_report (MAXDB_REPORT_ERROR);

$query = "create dbproc test_proc (INOUT e_text char(72)) AS select * from SYSDBA.DUAL; fetch into :e_text;";

maxdb_query($link, $query);

/* Performing SQL query */
$stmt = maxdb_prepare ($link, "CALL test_proc (?)");
if (!$stmt) {
  printf ("Prepare failed: %s\n", maxdb_error($link));
}

maxdb_stmt_bind_param($stmt, 's', $result);
maxdb_stmt_execute($stmt);

printf ("%s\n", $result);

maxdb_stmt_close ($stmt);
?>
```

以上例程的输出类似于：

    a

**示例 \#5 面向对象风格 (extended syntax)**

``` php
<?php
$maxdb = new maxdb('localhost', 'MONA', 'RED', 'DEMODB');

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query ("CREATE TABLE temp.mycity LIKE hotel.city");
$maxdb->query ("INSERT INTO temp.mycity SELECT * FROM hotel.city");

$stmt = $maxdb->prepare("INSERT INTO temp.mycity VALUES (?, ?, ?)");

$arr = array();

$stmt->bind_param('iss', $arr);

$arr[0] = 11111;
$arr[1] = 'Georgetown';
$arr[2] = 'NY';

/* execute prepared statement */
$stmt->execute();

printf("%d Row inserted.\n", maxdb_stmt_affected_rows($stmt));

$arr[0] = 22222;
$arr[1] = 'New Orleans';
$arr[2] = 'LA';

/* execute prepared statement */
$stmt->execute();

printf("%d Row inserted.\n", $stmt->affected_rows);

/* close statement and connection */
$stmt->close();

$result = $maxdb->query("SELECT * from temp.mycity WHERE zip = '11111' OR zip = '22222'");
if ($result) {
  while ($row = $result->fetch_row()) {
    printf ("%s %s %s\n", $row[0], $row[1], $row[2]);
  }
}

/* Clean up table CountryLanguage */
$maxdb->query("DELETE FROM temp.mycity WHERE name='Georgetown'");
$maxdb->query("DELETE FROM temp.mycity WHERE name='New Orleans'");
printf("%d Rows deleted.\n", $maxdb->affected_rows);

/* close connection */
$maxdb->close();
?>
```

以上例程的输出类似于：

    1 Row inserted.
    1 Row inserted.
    11111 Georgetown NY
    22222 New Orleans LA
    2 Rows deleted.

### 参见

-   <span class="function">maxdb\_stmt\_bind\_result</span>
-   <span class="function">maxdb\_stmt\_execute</span>
-   <span class="function">maxdb\_stmt\_fetch</span>
-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_send\_long\_data</span>
-   <span class="function">maxdb\_stmt\_errno</span>
-   <span class="function">maxdb\_stmt\_error</span>

maxdb\_stmt\_bind\_result
=========================

maxdb\_stmt::bind\_result
=========================

Binds variables to a prepared statement for result storage

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_bind\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`&$var1`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `&$...`</span> \] )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::bind\_result</span> ( <span
class="methodparam"><span class="type">mixed</span> `&$var1`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `&$...`</span>
\] )

<span class="function">maxdb\_stmt\_bind\_result</span> is used to
associate (bind) columns in the result set to variables. When <span
class="function">maxdb\_stmt\_fetch</span> is called to fetch data, the
MaxDB client/server protocol places the data for the bound columns into
the specified variables `var1, ...`.

> **Note**:
>
> Note that all columns must be bound prior to calling <span
> class="function">maxdb\_stmt\_fetch</span>. Depending on column types
> bound variables can silently change to the corresponding PHP type.
>
> A column can be bound or rebound at any time, even after a result set
> has been partially retrieved. The new binding takes effect the next
> time <span class="function">maxdb\_stmt\_fetch</span> is called.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* prepare statement */
if ($stmt = $maxdb->prepare("SELECT zip, name FROM hotel.city ORDER BY name")) {
   $stmt->execute();

   /* bind variables to prepared statement */
   $stmt->bind_result($col1, $col2);

   /* fetch values */
   while ($stmt->fetch()) {
       printf("%s %s\n", $col1, $col2);
   }

   /* close statement */
   $stmt->close();
}
/* close connection */
$maxdb->close();

?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (!$link) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* prepare statement */
if ($stmt = maxdb_prepare($link, "SELECT zip, name FROM hotel.city ORDER BY name")) {
   maxdb_stmt_execute($stmt);

   /* bind variables to prepared statement */
   maxdb_stmt_bind_result($stmt, $col1, $col2);

   /* fetch values */
   while (maxdb_stmt_fetch($stmt)) {
       printf("%s %s\n", $col1, $col2);
   }

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    12203 Albany
    60601 Chicago
    60615 Chicago
    45211 Cincinnati
    33575 Clearwater
    75243 Dallas
    32018 Daytona Beach
    33441 Deerfield Beach
    48226 Detroit
    90029 Hollywood
    92714 Irvine
    90804 Long Beach
    11788 Long Island
    90018 Los Angeles
    70112 New Orleans
    10019 New York
    10580 New York
    92262 Palm Springs
    97213 Portland
    60018 Rosemont
    95054 Santa Clara
    20903 Silver Spring
    20005 Washington
    20019 Washington
    20037 Washington

### 参见

-   <span class="function">maxdb\_stmt\_bind\_param</span>
-   <span class="function">maxdb\_stmt\_execute</span>
-   <span class="function">maxdb\_stmt\_fetch</span>
-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_prepare</span>
-   <span class="function">maxdb\_stmt\_init</span>
-   <span class="function">maxdb\_stmt\_errno</span>
-   <span class="function">maxdb\_stmt\_error</span>

maxdb\_stmt\_close\_long\_data
==============================

maxdb\_stmt::close\_long\_data
==============================

Ends a sequence of <span
class="function">maxdb\_stmt\_send\_long\_data</span>

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_close\_long\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">int</span>
`$param_nr`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::close\_long\_data</span> ( <span
class="methodparam">void</span> )

This function has to be called after a sequence of <span
class="function">maxdb\_stmt\_send\_long\_data</span>, that was started
after <span class="function">maxdb\_execute</span>.

`param_nr` indicates which parameter to associate the end of data with.
Parameters are numbered beginning with 0.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_bind\_param</span>

maxdb\_stmt\_close
==================

maxdb\_stmt::close
==================

Closes a prepared statement

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::close</span> ( <span
class="methodparam">void</span> )

Closes a prepared statement. <span
class="function">maxdb\_stmt\_close</span> also deallocates the
statement handle pointed to by `stmt`. If the current statement has
pending or unread results, this function cancels them so that the next
query can be executed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">maxdb\_prepare</span>

maxdb\_stmt\_data\_seek
=======================

maxdb\_stmt::data\_seek
=======================

Seeks to an arbitray row in statement result set

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span>
`$statement`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::data\_seek</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

The <span class="function">maxdb\_stmt\_data\_seek</span> function seeks
to an arbitrary result pointer specified by the `offset` in the
statement result set represented by `statement`. The `offset` parameter
must be between zero and the total number of rows minus one (0..<span
class="function">maxdb\_stmt\_num\_rows</span> - 1).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, zip FROM hotel.city ORDER BY name";
if ($stmt = $maxdb->prepare($query)) {

   /* execute query */
   $stmt->execute();

   /* bind result variables */
   $stmt->bind_result($name, $code);

   /* store result */
   $stmt->store_result();

   /* seek to row no. 5 */
   $stmt->data_seek(5);

   /* fetch values */
   $stmt->fetch();

   printf ("City: %s  Zip: %s\n", $name, $code);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Open a connection */
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, zip FROM hotel.city ORDER BY name";
if ($stmt = maxdb_prepare($link, $query)) {

   /* execute query */
   maxdb_stmt_execute($stmt);

   /* bind result variables */
   maxdb_stmt_bind_result($stmt, $name, $code);

   /* store result */
   maxdb_stmt_store_result($stmt);

   /* seek to row no. 5 */
   maxdb_stmt_data_seek($stmt, 5);

   /* fetch values */
   maxdb_stmt_fetch($stmt);

   printf ("City: %s  Zip: %s\n", $name, $code);

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    City: Dallas  Zip: 75243

### 参见

-   <span class="function">maxdb\_prepare</span>

maxdb\_stmt\_errno
==================

maxdb\_stmt::errno
==================

Returns the error code for the most recent statement call

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_stmt\_errno</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">int</span>`$maxdb_stmt->errno`;

For the statement specified by *stmt*, <span
class="function">maxdb\_stmt\_errno</span> returns the error code for
the most recently invoked statement function that can succeed or fail.

> **Note**:
>
> For possible error codes see documentation of SQLDBC:
> <a href="http://maxdb.sap.com/documentation/" class="link external">» http://maxdb.sap.com/documentation/</a>.

### 返回值

An error code value. Zero means no error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");
$maxdb->query("INSERT INTO temp.mycity SELECT * FROM hotel.city");


$query = "SELECT name, zip FROM temp.mycity ORDER BY name";
if ($stmt = $maxdb->prepare($query)) {

   /* drop table */
   $maxdb->query("DROP TABLE temp.mycity");

   /* execute query */
   $stmt->execute();

   printf("Error: %d.\n", $stmt->errno);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Open a connection */
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");
maxdb_query($link, "INSERT INTO temp.mycity SELECT * FROM hotel.city");


$query = "SELECT name, zip FROM temp.mycity ORDER BY name";
if ($stmt = maxdb_prepare($link, $query)) {

   /* drop table */
   maxdb_query($link, "DROP TABLE temp.mycity");

   /* execute query */
   maxdb_stmt_execute($stmt);

   printf("Error: %d.\n", maxdb_stmt_errno($stmt));

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_stmt_execute(): -4004 POS(23) Unknown table name:MYCITY [42000] <...>
    Error: -4004.

### 参见

-   <span class="function">maxdb\_stmt\_error</span>
-   <span class="function">maxdb\_stmt\_sqlstate</span>

maxdb\_stmt\_error
==================

maxdb\_stmt::error
==================

Returns a string description for last statement error

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">maxdb\_stmt\_error</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">string</span>`$maxdb_stmt->error`;

For the statement specified by *stmt*, <span
class="function">maxdb\_stmt\_error</span> returns a containing the
error message for the most recently invoked statement function that can
succeed or fail.

### 返回值

A string that describes the error. An empty string if no error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");
$maxdb->query("INSERT INTO temp.mycity SELECT * FROM hotel.city");


$query = "SELECT name, zip FROM temp.mycity ORDER BY name";
if ($stmt = $maxdb->prepare($query)) {

   /* drop table */
   $maxdb->query("DROP TABLE temp.mycity");

   /* execute query */
   $stmt->execute();

   printf("Error: %s.\n", $stmt->error);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Open a connection */
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");
maxdb_query($link, "INSERT INTO temp.mycity SELECT * FROM hotel.city");


$query = "SELECT name, zip FROM temp.mycity ORDER BY name";
if ($stmt = maxdb_prepare($link, $query)) {

   /* drop table */
   maxdb_query($link, "DROP TABLE temp.mycity");

   /* execute query */
   maxdb_stmt_execute($stmt);

   printf("Error: %s.\n", maxdb_stmt_error($stmt));

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_stmt_execute(): -4004 POS(23) Unknown table name:MYCITY [42000] <...>
    Error: POS(23) Unknown table name:MYCITY.

### 参见

-   <span class="function">maxdb\_stmt\_errno</span>
-   <span class="function">maxdb\_stmt\_sqlstate</span>

maxdb\_stmt\_execute
====================

maxdb\_stmt::execute
====================

Executes a prepared Query

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_execute</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::execute</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_stmt\_execute</span> function executes
a query that has been previously prepared using the <span
class="function">maxdb\_prepare</span> function represented by the
`stmt` resource. When executed any parameter markers which exist will
automatically be replaced with the appropriate data.

If the statement is UPDATE, DELETE, or INSERT, the total number of
affected rows can be determined by using the <span
class="function">maxdb\_stmt\_affected\_rows</span> function. Likewise,
if the query yields a result set the <span
class="function">maxdb\_fetch</span> function is used.

> **Note**:
>
> When using <span class="function">maxdb\_stmt\_execute</span>, the
> <span class="function">maxdb\_fetch</span> function must be used to
> fetch the data prior to preforming any additional queries.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");

/* Prepare an insert statement */
$query = "INSERT INTO temp.mycity (zip, name, state) VALUES (?,?,?)";
$stmt = $maxdb->prepare($query);

$stmt->bind_param("sss", $val1, $val2, $val3);

$val1 = '11111';
$val2 = 'Georgetown';
$val3 = 'NY';

/* Execute the statement */
$stmt->execute();

$val1 = '22222';
$val2 = 'Hubbatown';
$val3 = 'CA';

/* Execute the statement */
$stmt->execute();

/* close statement */
$stmt->close();

/* retrieve all rows from myCity */
$query = "SELECT zip, name, state FROM temp.mycity";
if ($result = $maxdb->query($query)) {
   while ($row = $result->fetch_row()) {
       printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
   }
   /* free result set */
   $result->close();
}

/* remove table */
$maxdb->query("DROP TABLE temp.mycity");

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");

/* Prepare an insert statement */
$query = "INSERT INTO temp.mycity (zip, name, state) VALUES (?,?,?)";
$stmt = maxdb_prepare($link, $query);

maxdb_stmt_bind_param($stmt, "sss", $val1, $val2, $val3);

$val1 = '11111';
$val2 = 'Georgetown';
$val3 = 'NY';

/* Execute the statement */
maxdb_stmt_execute($stmt);

$val1 = '22222';
$val2 = 'Hubbatown';
$val3 = 'CA';

/* Execute the statement */
maxdb_stmt_execute($stmt);

/* close statement */
maxdb_stmt_close($stmt);

/* retrieve all rows from myCity */
$query = "SELECT zip, name, state FROM temp.mycity";
if ($result = maxdb_query($link, $query)) {
   while ($row = maxdb_fetch_row($result)) {
       printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
   }
   /* free result set */
   maxdb_free_result($result);
}

/* remove table */
maxdb_query($link, "DROP TABLE temp.mycity");

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    11111 (Georgetown,NY)
    22222 (Hubbatown,CA)

### 参见

-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_bind\_param</span>

maxdb\_stmt\_fetch
==================

maxdb\_stmt::fetch
==================

Fetch results from a prepared statement into the bound variables

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_fetch</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::fetch</span> ( <span
class="methodparam">void</span> )

<span class="function">maxdb\_stmt\_fetch</span> returns row data using
the variables bound by <span
class="function">maxdb\_stmt\_bind\_result</span>.

> **Note**:
>
> Note that all columns must be bound by the application before calling
> <span class="function">maxdb\_stmt\_fetch</span>.

### 返回值

| Value       | Description                    |
|-------------|--------------------------------|
| **`TRUE`**  | Success. Data has been fetched |
| **`FALSE`** | Error occurred                 |
| **`NULL`**  | No more rows/data exists       |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT zip, name FROM hotel.city ORDER by name";

if ($stmt = $maxdb->prepare($query)) {

   /* execute statement */
   $stmt->execute();

   /* bind result variables */
   $stmt->bind_result($name, $code);

   /* fetch values */
   while ($stmt->fetch()) {
       printf ("%s (%s)\n", $name, $code);
   }

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT zip, name FROM hotel.city ORDER by name";

if ($stmt = maxdb_prepare($link, $query)) {

   /* execute statement */
   maxdb_stmt_execute($stmt);

   /* bind result variables */
   maxdb_stmt_bind_result($stmt, $name, $code);

   /* fetch values */
   while (maxdb_stmt_fetch($stmt)) {
       printf ("%s (%s)\n", $name, $code);
   }

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    12203 (Albany)
    60601 (Chicago)
    60615 (Chicago)
    45211 (Cincinnati)
    33575 (Clearwater)
    75243 (Dallas)
    32018 (Daytona Beach)
    33441 (Deerfield Beach)
    48226 (Detroit)
    90029 (Hollywood)
    92714 (Irvine)
    90804 (Long Beach)
    11788 (Long Island)
    90018 (Los Angeles)
    70112 (New Orleans)
    10019 (New York)
    10580 (New York)
    92262 (Palm Springs)
    97213 (Portland)
    60018 (Rosemont)
    95054 (Santa Clara)
    20903 (Silver Spring)
    20005 (Washington)
    20019 (Washington)
    20037 (Washington)

### 参见

-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_errno</span>
-   <span class="function">maxdb\_stmt\_error</span>
-   <span class="function">maxdb\_stmt\_bind\_result</span>

maxdb\_stmt\_free\_result
=========================

maxdb\_stmt::free\_result
=========================

Frees stored result memory for the given statement handle

### 说明

过程化风格

<span class="type">void</span> <span
class="methodname">maxdb\_stmt\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">void</span> <span
class="methodname">maxdb\_stmt::free\_result</span> ( <span
class="methodparam">void</span> )

The <span class="function">maxdb\_stmt\_free\_result</span> function
frees the result memory associated with the statement represented by the
`stmt` parameter, which was allocated by <span
class="function">maxdb\_stmt\_store\_result</span>.

### 返回值

This function doesn't return any value.

### 参见

-   <span class="function">maxdb\_stmt\_store\_result</span>

maxdb\_stmt\_init
=================

maxdb::stmt\_init
=================

Initializes a statement and returns an resource for use with
maxdb\_stmt\_prepare

### 说明

过程化风格

<span class="type">resource</span> <span
class="methodname">maxdb\_stmt\_init</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">object</span> <span
class="methodname">maxdb::stmt\_init</span> ( <span
class="methodparam">void</span> )

Allocates and initializes a statement resource suitable for <span
class="function">maxdb\_stmt\_prepare</span>.

> **Note**:
>
> Any subsequent calls to any maxdb\_stmt function will fail until <span
> class="function">maxdb\_stmt\_prepare</span> was called.

### 返回值

Returns an resource.

### 参见

-   <span class="function">maxdb\_stmt\_prepare</span>

maxdb\_stmt\_num\_rows
======================

maxdb\_stmt::num\_rows
======================

Return the number of rows in statements result set

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_stmt\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">int</span>`$maxdb_stmt->num_rows`;

Returns the number of rows in the result set.

### 返回值

An integer representing the number of rows in result set.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT zip, name FROM hotel.city ORDER BY name";
if ($stmt = $maxdb->prepare($query)) {

   /* execute query */
   $stmt->execute();

   /* store result */
   $stmt->store_result();

   printf("Number of rows: %d.\n", $stmt->num_rows);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Open a connection */
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT zip, name FROM hotel.city ORDER BY name";
if ($stmt = maxdb_prepare($link, $query)) {

   /* execute query */
   maxdb_stmt_execute($stmt);

   /* store result */
   maxdb_stmt_store_result($stmt);

   printf("Number of rows: %d.\n", maxdb_stmt_num_rows($stmt));

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Number of rows: 25.

### 参见

-   <span class="function">maxdb\_stmt\_affected\_rows</span>
-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_store\_result</span>

maxdb\_stmt\_param\_count
=========================

maxdb\_stmt::param\_count
=========================

Returns the number of parameter for the given statement

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_stmt\_param\_count</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">int</span>`$maxdb_stmt->param_count`;

<span class="function">maxdb\_stmt\_param\_count</span> returns the
number of parameter markers present in the prepared statement.

### 返回值

returns an integer representing the number of parameters.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($stmt = $maxdb->prepare("SELECT name FROM hotel.city WHERE name=? OR state=?")) {

   $marker = $stmt->param_count;
   printf("Statement has %d markers.\n", $marker);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

if ($stmt = maxdb_prepare($link, "SELECT name FROM hotel.city WHERE name=? OR state=?")) {

   $marker = maxdb_stmt_param_count($stmt);
   printf("Statement has %d markers.\n", $marker);

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Statement has 2 markers.

### 参见

-   <span class="function">maxdb\_prepare</span>

maxdb\_stmt\_prepare
====================

maxdb\_stmt::prepare
====================

Prepare an SQL statement for execution

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

面向对象风格

<span class="type">mixed</span> <span
class="methodname">maxdb\_stmt::prepare</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

<span class="function">maxdb\_stmt\_prepare</span> prepares the SQL
query pointed to by the null-terminated string query. The statement
resource has to be allocated by <span
class="function">maxdb\_stmt\_init</span>. The query must consist of a
single SQL statement.

> **Note**:
>
> You should not add a terminating semicolon or *\\g* to the statement.

The parameter `query` can include one or more parameter markers in the
SQL statement by embedding question mark (*?*) characters at the
appropriate positions.

> **Note**:
>
> The markers are legal only in certain places in SQL statements. For
> example, they are allowed in the VALUES() list of an INSERT statement
> (to specify column values for a row), or in a comparison with a column
> in a WHERE clause to specify a comparison value.
>
> However, they are not allowed for identifiers (such as table or column
> names), in the select list that names the columns to be returned by a
> SELECT statement), or to specify both operands of a binary operator
> such as the *=* equal sign. The latter restriction is necessary
> because it would be impossible to determine the parameter type. In
> general, parameters are legal only in Data Manipulation Languange
> (DML) statements, and not in Data Defination Language (DDL)
> statements.

The parameter markers must be bound to application variables using <span
class="function">maxdb\_stmt\_bind\_param</span> and/or <span
class="function">maxdb\_stmt\_bind\_result</span> before executing the
statement or fetching rows.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$city = "Portland";

/* create a prepared statement */
$stmt =  $maxdb->stmt_init();
if ($stmt->prepare("SELECT state FROM hotel.city WHERE name=?")) {

   /* bind parameters for markers */
   $stmt->bind_param("s", $city);

   /* execute query */
   $stmt->execute();

   /* bind result variables */
   $stmt->bind_result($district);

   /* fetch value */
   $stmt->fetch();

   printf("%s is in district %s\n", $city, $district);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$city = "Portland";

/* create a prepared statement */
$stmt = maxdb_stmt_init($link);
if (maxdb_stmt_prepare($stmt, "SELECT state FROM hotel.city WHERE name=?")) {

   /* bind parameters for markers */
   maxdb_stmt_bind_param($stmt, "s", $city);

   /* execute query */
   maxdb_stmt_execute($stmt);

   /* bind result variables */
   maxdb_stmt_bind_result($stmt, $district);

   /* fetch value */
   maxdb_stmt_fetch($stmt);

   printf("%s is in district %s\n", $city, $district);

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Portland is in district OR

### 参见

-   <span class="function">maxdb\_stmt\_init</span>
-   <span class="function">maxdb\_stmt\_execute</span>
-   <span class="function">maxdb\_stmt\_fetch</span>
-   <span class="function">maxdb\_stmt\_bind\_param</span>
-   <span class="function">maxdb\_stmt\_bind\_result</span>
-   <span class="function">maxdb\_stmt\_close</span>

maxdb\_stmt\_reset
==================

maxdb\_stmt::reset
==================

Resets a prepared statement

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_reset</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::reset</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

maxdb\_stmt\_result\_metadata
=============================

maxdb\_stmt::result\_metadata
=============================

Returns result set metadata from a prepared statement

### 说明

过程化风格

<span class="type">resource</span> <span
class="methodname">maxdb\_stmt\_result\_metadata</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">resource</span> <span
class="methodname">maxdb\_stmt::result\_metadata</span> ( <span
class="methodparam">void</span> )

If a statement passed to <span class="function">maxdb\_prepare</span> is
one that produces a result set, <span
class="function">maxdb\_stmt\_result\_metadata</span> returns the result
resource that can be used to process the meta information such as total
number of fields and individual field information.

> **Note**:
>
> This result set pointer can be passed as an argument to any of the
> field-based functions that process result set metadata, such as:
>
> -   <span class="function">maxdb\_num\_fields</span>
>
> -   <span class="function">maxdb\_fetch\_field</span>
>
> -   <span class="function">maxdb\_fetch\_field\_direct</span>
>
> -   <span class="function">maxdb\_fetch\_fields</span>
>
> -   <span class="function">maxdb\_field\_count</span>
>
> -   <span class="function">maxdb\_field\_seek</span>
>
> -   <span class="function">maxdb\_field\_tell</span>
>
> -   <span class="function">maxdb\_free\_result</span>

The result set structure should be freed when you are done with it,
which you can do by passing it to <span
class="function">maxdb\_free\_result</span>

> **Note**:
>
> The result set returned by <span
> class="function">maxdb\_stmt\_result\_metadata</span> contains only
> metadata. It does not contain any row results. The rows are obtained
> by using the statement handle with <span
> class="function">maxdb\_fetch</span>.

### 返回值

<span class="function">maxdb\_stmt\_result\_metadata</span> returns a
result resource or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

$maxdb->query("CREATE TABLE temp.friends (id int, name varchar(20))");

$maxdb->query("INSERT INTO temp.friends VALUES (1,'Hartmut')");
$maxdb->query("INSERT INTO temp.friends VALUES (2, 'Ulf')");

$stmt = $maxdb->prepare("SELECT id, name FROM temp.friends");
$stmt->execute();

/* get resultset for metadata */
$result = $stmt->result_metadata();

/* retrieve field information from metadata result set */
$field = $result->fetch_field();

printf("Fieldname: %s\n", $field->name);

/* close resultset */
$result->close();

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

maxdb_query($link, "CREATE TABLE temp.friends (id int, name varchar(20))");

maxdb_query($link, "INSERT INTO temp.friends VALUES (1,'Hartmut')");
maxdb_query($link, "INSERT INTO temp.friends VALUES (2, 'Ulf')");

$stmt = maxdb_prepare($link, "SELECT id, name FROM temp.friends");
maxdb_stmt_execute($stmt);

/* get resultset for metadata */
$result = maxdb_stmt_result_metadata($stmt);

/* retrieve field information from metadata result set */
$field = maxdb_fetch_field($result);

printf("Fieldname: %s\n", $field->name);

/* close resultset */
maxdb_free_result($result);

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Fieldname: ID

### 参见

-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_free\_result</span>

maxdb\_stmt\_send\_long\_data
=============================

maxdb\_stmt::send\_long\_data
=============================

Send data in blocks

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_send\_long\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">int</span>
`$param_nr`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> )

面向对象风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt::stmt\_send\_long\_data</span> ( <span
class="methodparam"><span class="type">int</span> `$param_nr`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

Allows to send parameter data to the server in pieces (or chunks). This
function can be called multiple times to send the parts of a character
or binary data value for a column, which must be one of the TEXT or BLOB
datatypes.

`param_nr` indicates which parameter to associate the data with.
Parameters are numbered beginning with 0. `data` is a string containing
data to be sent.

> **Note**:
>
> For efficiency reasons, this function should be used after calling
> <span class="function">maxdb\_execute</span>. In this case, the data
> is not stored on the client side. The end of the sequence must end
> with a call to <span
> class="function">maxdb\_stmt\_close\_long\_data</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_bind\_param</span>

maxdb\_stmt\_sqlstate
=====================

Returns SQLSTATE error from previous statement operation

### 说明

<span class="type">string</span> <span
class="methodname">maxdb\_stmt\_sqlstate</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Returns a string containing the SQLSTATE error code for the most
recently invoked prepared statement function that can succeed or fail.
The error code consists of five characters. *'00000'* means no error.
The values are specified by ANSI SQL and ODBC.

> **Note**:
>
> Note that not all MaxDB errors are yet mapped to SQLSTATE's. The value
> *HY000* (general error) is used for unmapped errors.

### 返回值

Returns a string containing the SQLSTATE error code for the last error.
The error code consists of five characters. *'00000'* means no error.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");
$maxdb->query("INSERT INTO temp.mycity SELECT * FROM hotel.city");

$query = "SELECT name, zip FROM temp.mycity ORDER BY name";
if ($stmt = $maxdb->prepare($query)) {

   /* drop table */
   $maxdb->query("DROP TABLE temp.mycity");

   /* execute query */
   $stmt->execute();

   printf("Error: %s.\n", $stmt->sqlstate);

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Open a connection */
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");
maxdb_query($link, "INSERT INTO temp.mycity SELECT * FROM hotel.city");

$query = "SELECT name, zip FROM temp.mycity ORDER BY name";
if ($stmt = maxdb_prepare($link, $query)) {

   /* drop table */
   maxdb_query($link, "DROP TABLE temp.mycity");

   /* execute query */
   maxdb_stmt_execute($stmt);

   printf("Error: %s.\n", maxdb_stmt_sqlstate($stmt));

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_stmt_execute(): -4004 POS(23) Unknown table name:MYCITY [42000] <...>
    Error: 42000.

### 参见

-   <span class="function">maxdb\_stmt\_errno</span>
-   <span class="function">maxdb\_stmt\_error</span>

maxdb\_stmt\_store\_result
==========================

maxdb\_stmt::store\_result
==========================

Transfers a result set from a prepared statement

### 说明

过程化风格

<span class="type">bool</span> <span
class="methodname">maxdb\_stmt\_store\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

面向对象风格

<span class="type">object</span> <span
class="methodname">maxdb\_stmt::store\_result</span> ( <span
class="methodparam">void</span> )

<span class="function">maxdb\_stmt\_store\_result</span> has no
functionally effect and should not be used for retrieving data from
MaxDB server.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Open a connection */
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, zip FROM hotel.city ORDER BY name";
if ($stmt = $maxdb->prepare($query)) {

   /* execute query */
   $stmt->execute();

   /* store result */
   $stmt->store_result();

   printf("Number of rows: %d.\n", $stmt->num_rows);

   /* free result */
   $stmt->free_result();

   /* close statement */
   $stmt->close();
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Open a connection */
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query = "SELECT name, zip FROM hotel.city ORDER BY name";
if ($stmt = maxdb_prepare($link, $query)) {

   /* execute query */
   maxdb_stmt_execute($stmt);

   /* store result */
   maxdb_stmt_store_result($stmt);

   printf("Number of rows: %d.\n", maxdb_stmt_num_rows($stmt));

   /* free result */
   maxdb_stmt_free_result($stmt);

   /* close statement */
   maxdb_stmt_close($stmt);
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Number of rows: 25.

### 参见

-   <span class="function">maxdb\_prepare</span>
-   <span class="function">maxdb\_stmt\_result\_metadata</span>
-   <span class="function">maxdb\_fetch</span>

maxdb\_store\_result
====================

maxdb::store\_result
====================

Transfers a result set from the last query

### 说明

过程化风格

<span class="type">resource</span> <span
class="methodname">maxdb\_store\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">object</span> <span
class="methodname">maxdb::store\_result</span> ( <span
class="methodparam">void</span> )

This function has no functionally effect.

### 返回值

Returns a result resource or **`FALSE`** if an error occurred.

### 范例

See <span class="function">maxdb\_multi\_query</span>.

### 参见

-   <span class="function">maxdb\_real\_query</span>
-   <span class="function">maxdb\_use\_result</span>

maxdb\_thread\_id
=================

maxdb::thread\_id
=================

Returns the thread ID for the current connection

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_thread\_id</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span>`$maxdb->thread_id`;

The <span class="function">maxdb\_thread\_id</span> function returns the
thread ID for the current connection which can then be killed using the
<span class="function">maxdb\_kill</span> function. If the connection is
lost and you reconnect with <span class="function">maxdb\_ping</span>,
the thread ID will be other. Therefore you should get the thread ID only
when you need it.

> **Note**:
>
> The thread ID is assigned on a connection-by-connection basis. Hence,
> if the connection is broken and then re-established a new thread ID
> will be assigned.

### 返回值

<span class="function">maxdb\_thread\_id</span> returns the Thread ID
for the current connection.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* determine our thread id */
$thread_id = $maxdb->thread_id;

/* Kill connection */
$maxdb->kill($thread_id);

/* This should produce an error */
if (!$maxdb->query("CREATE TABLE mycity LIKE hotel.city")) {
   printf("Error: %s\n", $maxdb->error);
   exit;
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

/* determine our thread id */
$thread_id = maxdb_thread_id($link);

/* Kill connection */
maxdb_kill($link, $thread_id);

/* This should produce an error */
if (!maxdb_query($link, "CREATE TABLE mycity LIKE hotel.city")) {
   printf("Error: %s\n", maxdb_error($link));
   exit;
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_query(): -10821 Session not connected <...>
    Error: Session not connected

### 参见

-   <span class="function">maxdb\_kill</span>

maxdb\_thread\_safe
===================

Returns whether thread safety is given or not

### 说明

<span class="type">bool</span> <span
class="methodname">maxdb\_thread\_safe</span> ( <span
class="methodparam">void</span> )

<span class="function">maxdb\_thread\_safe</span> indicates whether the
client library is compiled as thread-safe.

### 返回值

**`TRUE`** if the client library is thread-safe, otherwise **`FALSE`**.

maxdb\_use\_result
==================

maxdb::use\_result
==================

Initiate a result set retrieval

### 说明

过程化风格

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">maxdb\_use\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">maxdb::use\_result</span> ( <span
class="methodparam">void</span> )

<span class="function">maxdb\_use\_result</span> has no effect.

### 返回值

Returns result 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query  = "SELECT * FROM DUAL";

/* execute multi query */
if ($maxdb->multi_query($query)) {
   do {
       /* store first result set */
       if ($result = $maxdb->use_result()) {
           while ($row = $result->fetch_row()) {
               printf("%s\n", $row[0]);
           }
           $result->close();
       }
       /* print divider */
       if ($maxdb->more_results()) {
           printf("-----------------\n");
       }
   } while ($maxdb->next_result());
}

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$query  = "SELECT * FROM DUAL";

/* execute multi query */
if (maxdb_multi_query($link, $query)) {
   do {
       /* store first result set */
       if ($result = maxdb_use_result($link)) {
           while ($row = maxdb_fetch_row($result)) {
               printf("%s\n", $row[0]);
           }
           maxdb_free_result($result);
       }
       /* print divider */
       if (maxdb_more_results($link)) {
           printf("-----------------\n");
       }
   } while (maxdb_next_result($link));
}

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    a

### 参见

-   <span class="function">maxdb\_real\_query</span>
-   <span class="function">maxdb\_store\_result</span>

maxdb\_warning\_count
=====================

maxdb::warning\_count
=====================

Returns the number of warnings from the last query for the given link

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">maxdb\_warning\_count</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

面向对象风格

<span class="type">int</span>`$maxdb->warning_count`;

<span class="function">maxdb\_warning\_count</span> returns the number
of warnings from the last query in the connection represented by the
`link` parameter.

### 返回值

Number of warnings or zero if there are no warnings.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$maxdb = new maxdb("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

$maxdb->query("CREATE TABLE temp.mycity LIKE hotel.city");

/* a remarkable city in Wales */
$query = "INSERT INTO temp.mycity (zip, name) VALUES('11111',
       'Llanfairpwllgwyngyllgogerychwyrndrobwllllantysiliogogogoch')";

$maxdb->query($query);

printf ("Number of warning: %d\n", $maxdb->warning_count);

/* close connection */
$maxdb->close();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
$link = maxdb_connect("localhost", "MONA", "RED", "DEMODB");

/* check connection */
if (maxdb_connect_errno()) {
   printf("Connect failed: %s\n", maxdb_connect_error());
   exit();
}

maxdb_query($link, "CREATE TABLE temp.mycity LIKE hotel.city");

/* a remarkable long city name in Wales */
$query = "INSERT INTO temp.mycity (zip, name) VALUES('11111',
       'Llanfairpwllgwyngyllgogerychwyrndrobwllllantysiliogogogoch')";

maxdb_query($link, $query);

printf ("Number of warning: %d\n", maxdb_warning_count($link));

/* close connection */
maxdb_close($link);
?>
```

以上例程的输出类似于：

    Warning: maxdb_query(): -8004 POS(62) Constant must be compatible with column type and length <...>
    Number of warning: 0

### 参见

-   <span class="function">maxdb\_errno</span>
-   <span class="function">maxdb\_error</span>
-   <span class="function">maxdb\_sqlstate</span>

**目录**

-   [maxdb\_affected\_rows](/book/maxdb.html#maxdb_affected_rows) — Gets
    the number of affected rows in a previous MaxDB operation
-   [maxdb\_autocommit](/book/maxdb.html#maxdb_autocommit) — Turns on or
    off auto-commiting database modifications
-   [maxdb\_bind\_param](/book/maxdb.html#maxdb_bind_param) — 别名
    maxdb\_stmt\_bind\_param
-   [maxdb\_bind\_result](/book/maxdb.html#maxdb_bind_result) — 别名
    maxdb\_stmt\_bind\_result
-   [maxdb\_change\_user](/book/maxdb.html#maxdb_change_user) — Changes
    the user of the specified database connection
-   [maxdb\_character\_set\_name](/book/maxdb.html#maxdb_character_set_name)
    — Returns the default character set for the database connection
-   [maxdb\_client\_encoding](/book/maxdb.html#maxdb_client_encoding) —
    别名 maxdb\_character\_set\_name
-   [maxdb\_close\_long\_data](/book/maxdb.html#maxdb_close_long_data) —
    别名 maxdb\_stmt\_close\_long\_data
-   [maxdb\_close](/book/maxdb.html#maxdb_close) — Closes a previously
    opened database connection
-   [maxdb\_commit](/book/maxdb.html#maxdb_commit) — Commits the current
    transaction
-   [maxdb\_connect\_errno](/book/maxdb.html#maxdb_connect_errno) —
    Returns the error code from last connect call
-   [maxdb\_connect\_error](/book/maxdb.html#maxdb_connect_error) —
    Returns a string description of the last connect error
-   [maxdb\_connect](/book/maxdb.html#maxdb_connect) — Open a new
    connection to the MaxDB server
-   [maxdb\_data\_seek](/book/maxdb.html#maxdb_data_seek) — Adjusts the
    result pointer to an arbitary row in the result
-   [maxdb\_debug](/book/maxdb.html#maxdb_debug) — Performs debugging
    operations
-   [maxdb\_disable\_reads\_from\_master](/book/maxdb.html#maxdb_disable_reads_from_master)
    — Disable reads from master
-   [maxdb\_disable\_rpl\_parse](/book/maxdb.html#maxdb_disable_rpl_parse)
    — Disable RPL parse
-   [maxdb\_dump\_debug\_info](/book/maxdb.html#maxdb_dump_debug_info) —
    Dump debugging information into the log
-   [maxdb\_embedded\_connect](/book/maxdb.html#maxdb_embedded_connect)
    — Open a connection to an embedded MaxDB server
-   [maxdb\_enable\_reads\_from\_master](/book/maxdb.html#maxdb_enable_reads_from_master)
    — Enable reads from master
-   [maxdb\_enable\_rpl\_parse](/book/maxdb.html#maxdb_enable_rpl_parse)
    — Enable RPL parse
-   [maxdb\_errno](/book/maxdb.html#maxdb_errno) — Returns the error
    code for the most recent function call
-   [maxdb\_error](/book/maxdb.html#maxdb_error) — Returns a string
    description of the last error
-   [maxdb\_escape\_string](/book/maxdb.html#maxdb_escape_string) — 别名
    maxdb\_real\_escape\_string
-   [maxdb\_execute](/book/maxdb.html#maxdb_execute) — 别名
    maxdb\_stmt\_execute
-   [maxdb\_fetch\_array](/book/maxdb.html#maxdb_fetch_array) — Fetch a
    result row as an associative, a numeric array, or both
-   [maxdb\_fetch\_assoc](/book/maxdb.html#maxdb_fetch_assoc) — Fetch a
    result row as an associative array
-   [maxdb\_fetch\_field\_direct](/book/maxdb.html#maxdb_fetch_field_direct)
    — Fetch meta-data for a single field
-   [maxdb\_fetch\_field](/book/maxdb.html#maxdb_fetch_field) — Returns
    the next field in the result set
-   [maxdb\_fetch\_fields](/book/maxdb.html#maxdb_fetch_fields) —
    Returns an array of resources representing the fields in a result
    set
-   [maxdb\_fetch\_lengths](/book/maxdb.html#maxdb_fetch_lengths) —
    Returns the lengths of the columns of the current row in the result
    set
-   [maxdb\_fetch\_object](/book/maxdb.html#maxdb_fetch_object) —
    Returns the current row of a result set as an object
-   [maxdb\_fetch\_row](/book/maxdb.html#maxdb_fetch_row) — Get a result
    row as an enumerated array
-   [maxdb\_fetch](/book/maxdb.html#maxdb_fetch) — 别名
    maxdb\_stmt\_fetch
-   [maxdb\_field\_count](/book/maxdb.html#maxdb_field_count) — Returns
    the number of columns for the most recent query
-   [maxdb\_field\_seek](/book/maxdb.html#maxdb_field_seek) — Set result
    pointer to a specified field offset
-   [maxdb\_field\_tell](/book/maxdb.html#maxdb_field_tell) — Get
    current field offset of a result pointer
-   [maxdb\_free\_result](/book/maxdb.html#maxdb_free_result) — Frees
    the memory associated with a result
-   [maxdb\_get\_client\_info](/book/maxdb.html#maxdb_get_client_info) —
    Returns the MaxDB client version as a string
-   [maxdb\_get\_client\_version](/book/maxdb.html#maxdb_get_client_version)
    — Get MaxDB client info
-   [maxdb\_get\_host\_info](/book/maxdb.html#maxdb_get_host_info) —
    Returns a string representing the type of connection used
-   [maxdb\_get\_metadata](/book/maxdb.html#maxdb_get_metadata) — 别名
    maxdb\_stmt\_result\_metadata
-   [maxdb\_get\_proto\_info](/book/maxdb.html#maxdb_get_proto_info) —
    Returns the version of the MaxDB protocol used
-   [maxdb\_get\_server\_info](/book/maxdb.html#maxdb_get_server_info) —
    Returns the version of the MaxDB server
-   [maxdb\_get\_server\_version](/book/maxdb.html#maxdb_get_server_version)
    — Returns the version of the MaxDB server as an integer
-   [maxdb\_info](/book/maxdb.html#maxdb_info) — Retrieves information
    about the most recently executed query
-   [maxdb\_init](/book/maxdb.html#maxdb_init) — Initializes MaxDB and
    returns an resource for use with maxdb\_real\_connect
-   [maxdb\_insert\_id](/book/maxdb.html#maxdb_insert_id) — Returns the
    auto generated id used in the last query
-   [maxdb\_kill](/book/maxdb.html#maxdb_kill) — Disconnects from a
    MaxDB server
-   [maxdb\_master\_query](/book/maxdb.html#maxdb_master_query) —
    Enforce execution of a query on the master in a master/slave setup
-   [maxdb\_more\_results](/book/maxdb.html#maxdb_more_results) — Check
    if there any more query results from a multi query
-   [maxdb\_multi\_query](/book/maxdb.html#maxdb_multi_query) — Performs
    a query on the database
-   [maxdb\_next\_result](/book/maxdb.html#maxdb_next_result) — Prepare
    next result from multi\_query
-   [maxdb\_num\_fields](/book/maxdb.html#maxdb_num_fields) — Get the
    number of fields in a result
-   [maxdb\_num\_rows](/book/maxdb.html#maxdb_num_rows) — Gets the
    number of rows in a result
-   [maxdb\_options](/book/maxdb.html#maxdb_options) — Set options
-   [maxdb\_param\_count](/book/maxdb.html#maxdb_param_count) — 别名
    maxdb\_stmt\_param\_count
-   [maxdb\_ping](/book/maxdb.html#maxdb_ping) — Pings a server
    connection, or tries to reconnect if the connection has gone down
-   [maxdb\_prepare](/book/maxdb.html#maxdb_prepare) — Prepare an SQL
    statement for execution
-   [maxdb\_query](/book/maxdb.html#maxdb_query) — Performs a query on
    the database
-   [maxdb\_real\_connect](/book/maxdb.html#maxdb_real_connect) — Opens
    a connection to a MaxDB server
-   [maxdb\_real\_escape\_string](/book/maxdb.html#maxdb_real_escape_string)
    — Escapes special characters in a string for use in an SQL
    statement, taking into account the current charset of the connection
-   [maxdb\_real\_query](/book/maxdb.html#maxdb_real_query) — Execute an
    SQL query
-   [maxdb\_report](/book/maxdb.html#maxdb_report) — Enables or disables
    internal report functions
-   [maxdb\_rollback](/book/maxdb.html#maxdb_rollback) — Rolls back
    current transaction
-   [maxdb\_rpl\_parse\_enabled](/book/maxdb.html#maxdb_rpl_parse_enabled)
    — Check if RPL parse is enabled
-   [maxdb\_rpl\_probe](/book/maxdb.html#maxdb_rpl_probe) — RPL probe
-   [maxdb\_rpl\_query\_type](/book/maxdb.html#maxdb_rpl_query_type) —
    Returns RPL query type
-   [maxdb\_select\_db](/book/maxdb.html#maxdb_select_db) — Selects the
    default database for database queries
-   [maxdb\_send\_long\_data](/book/maxdb.html#maxdb_send_long_data) —
    别名 maxdb\_stmt\_send\_long\_data
-   [maxdb\_send\_query](/book/maxdb.html#maxdb_send_query) — Send the
    query and return
-   [maxdb\_server\_end](/book/maxdb.html#maxdb_server_end) — Shut down
    the embedded server
-   [maxdb\_server\_init](/book/maxdb.html#maxdb_server_init) —
    Initialize embedded server
-   [maxdb\_set\_opt](/book/maxdb.html#maxdb_set_opt) — 别名
    maxdb\_options
-   [maxdb\_sqlstate](/book/maxdb.html#maxdb_sqlstate) — Returns the
    SQLSTATE error from previous MaxDB operation
-   [maxdb\_ssl\_set](/book/maxdb.html#maxdb_ssl_set) — Used for
    establishing secure connections using SSL
-   [maxdb\_stat](/book/maxdb.html#maxdb_stat) — Gets the current system
    status
-   [maxdb\_stmt\_affected\_rows](/book/maxdb.html#maxdb_stmt_affected_rows)
    — Returns the total number of rows changed, deleted, or inserted by
    the last executed statement
-   [maxdb\_stmt\_bind\_param](/book/maxdb.html#maxdb_stmt_bind_param) —
    Binds variables to a prepared statement as parameters
-   [maxdb\_stmt\_bind\_result](/book/maxdb.html#maxdb_stmt_bind_result)
    — Binds variables to a prepared statement for result storage
-   [maxdb\_stmt\_close\_long\_data](/book/maxdb.html#maxdb_stmt_close_long_data)
    — Ends a sequence of maxdb\_stmt\_send\_long\_data
-   [maxdb\_stmt\_close](/book/maxdb.html#maxdb_stmt_close) — Closes a
    prepared statement
-   [maxdb\_stmt\_data\_seek](/book/maxdb.html#maxdb_stmt_data_seek) —
    Seeks to an arbitray row in statement result set
-   [maxdb\_stmt\_errno](/book/maxdb.html#maxdb_stmt_errno) — Returns
    the error code for the most recent statement call
-   [maxdb\_stmt\_error](/book/maxdb.html#maxdb_stmt_error) — Returns a
    string description for last statement error
-   [maxdb\_stmt\_execute](/book/maxdb.html#maxdb_stmt_execute) —
    Executes a prepared Query
-   [maxdb\_stmt\_fetch](/book/maxdb.html#maxdb_stmt_fetch) — Fetch
    results from a prepared statement into the bound variables
-   [maxdb\_stmt\_free\_result](/book/maxdb.html#maxdb_stmt_free_result)
    — Frees stored result memory for the given statement handle
-   [maxdb\_stmt\_init](/book/maxdb.html#maxdb_stmt_init) — Initializes
    a statement and returns an resource for use with
    maxdb\_stmt\_prepare
-   [maxdb\_stmt\_num\_rows](/book/maxdb.html#maxdb_stmt_num_rows) —
    Return the number of rows in statements result set
-   [maxdb\_stmt\_param\_count](/book/maxdb.html#maxdb_stmt_param_count)
    — Returns the number of parameter for the given statement
-   [maxdb\_stmt\_prepare](/book/maxdb.html#maxdb_stmt_prepare) —
    Prepare an SQL statement for execution
-   [maxdb\_stmt\_reset](/book/maxdb.html#maxdb_stmt_reset) — Resets a
    prepared statement
-   [maxdb\_stmt\_result\_metadata](/book/maxdb.html#maxdb_stmt_result_metadata)
    — Returns result set metadata from a prepared statement
-   [maxdb\_stmt\_send\_long\_data](/book/maxdb.html#maxdb_stmt_send_long_data)
    — Send data in blocks
-   [maxdb\_stmt\_sqlstate](/book/maxdb.html#maxdb_stmt_sqlstate) —
    Returns SQLSTATE error from previous statement operation
-   [maxdb\_stmt\_store\_result](/book/maxdb.html#maxdb_stmt_store_result)
    — Transfers a result set from a prepared statement
-   [maxdb\_store\_result](/book/maxdb.html#maxdb_store_result) —
    Transfers a result set from the last query
-   [maxdb\_thread\_id](/book/maxdb.html#maxdb_thread_id) — Returns the
    thread ID for the current connection
-   [maxdb\_thread\_safe](/book/maxdb.html#maxdb_thread_safe) — Returns
    whether thread safety is given or not
-   [maxdb\_use\_result](/book/maxdb.html#maxdb_use_result) — Initiate a
    result set retrieval
-   [maxdb\_warning\_count](/book/maxdb.html#maxdb_warning_count) —
    Returns the number of warnings from the last query for the given
    link
