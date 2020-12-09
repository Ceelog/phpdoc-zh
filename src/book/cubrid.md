CUBRID
======

**目录**

-   [简介](/book/cubrid.html#简介)
-   [安装／配置](/book/cubrid.html#安装／配置)
    -   [需求](/book/cubrid.html#需求)
    -   [安装](/book/cubrid.html#安装)
    -   [运行时配置](/book/cubrid.html#运行时配置)
    -   [资源类型](/book/cubrid.html#资源类型)
-   [预定义常量](/book/cubrid.html#预定义常量)
-   [范例](/book/cubrid.html#范例)
-   [CUBRID 函数](/book/cubrid.html#CUBRID%20函数)
    -   [cubrid\_bind](/book/cubrid.html#cubrid_bind) — Bind variables
        to a prepared statement as parameters
    -   [cubrid\_close\_prepare](/book/cubrid.html#cubrid_close_prepare)
        — Close the request handle
    -   [cubrid\_close\_request](/book/cubrid.html#cubrid_close_request)
        — Close the request handle
    -   [cubrid\_col\_get](/book/cubrid.html#cubrid_col_get) — Get
        contents of collection type column using OID
    -   [cubrid\_col\_size](/book/cubrid.html#cubrid_col_size) — Get the
        number of elements in collection type column using OID
    -   [cubrid\_column\_names](/book/cubrid.html#cubrid_column_names) —
        Get the column names in result
    -   [cubrid\_column\_types](/book/cubrid.html#cubrid_column_types) —
        Get column types in result
    -   [cubrid\_commit](/book/cubrid.html#cubrid_commit) — Commit a
        transaction
    -   [cubrid\_connect\_with\_url](/book/cubrid.html#cubrid_connect_with_url)
        — Establish the environment for connecting to CUBRID server
    -   [cubrid\_connect](/book/cubrid.html#cubrid_connect) — Open a
        connection to a CUBRID Server
    -   [cubrid\_current\_oid](/book/cubrid.html#cubrid_current_oid) —
        Get OID of the current cursor location
    -   [cubrid\_disconnect](/book/cubrid.html#cubrid_disconnect) —
        Close a database connection
    -   [cubrid\_drop](/book/cubrid.html#cubrid_drop) — Delete an
        instance using OID
    -   [cubrid\_error\_code\_facility](/book/cubrid.html#cubrid_error_code_facility)
        — Get the facility code of error
    -   [cubrid\_error\_code](/book/cubrid.html#cubrid_error_code) — Get
        error code for the most recent function call
    -   [cubrid\_error\_msg](/book/cubrid.html#cubrid_error_msg) — Get
        last error message for the most recent function call
    -   [cubrid\_execute](/book/cubrid.html#cubrid_execute) — Execute a
        prepared SQL statement
    -   [cubrid\_fetch](/book/cubrid.html#cubrid_fetch) — Fetch the next
        row from a result set
    -   [cubrid\_free\_result](/book/cubrid.html#cubrid_free_result) —
        Free the memory occupied by the result data
    -   [cubrid\_get\_autocommit](/book/cubrid.html#cubrid_get_autocommit)
        — Get auto-commit mode of the connection
    -   [cubrid\_get\_charset](/book/cubrid.html#cubrid_get_charset) —
        Return the current CUBRID connection charset
    -   [cubrid\_get\_class\_name](/book/cubrid.html#cubrid_get_class_name)
        — Get the class name using OID
    -   [cubrid\_get\_client\_info](/book/cubrid.html#cubrid_get_client_info)
        — Return the client library version
    -   [cubrid\_get\_db\_parameter](/book/cubrid.html#cubrid_get_db_parameter)
        — Returns the CUBRID database parameters
    -   [cubrid\_get\_query\_timeout](/book/cubrid.html#cubrid_get_query_timeout)
        — Get the query timeout value of the request
    -   [cubrid\_get\_server\_info](/book/cubrid.html#cubrid_get_server_info)
        — Return the CUBRID server version
    -   [cubrid\_get](/book/cubrid.html#cubrid_get) — Get a column using
        OID
    -   [cubrid\_insert\_id](/book/cubrid.html#cubrid_insert_id) —
        Return the ID generated for the last updated AUTO\_INCREMENT
        column
    -   [cubrid\_is\_instance](/book/cubrid.html#cubrid_is_instance) —
        Check whether the instance pointed by OID exists
    -   [cubrid\_lob\_close](/book/cubrid.html#cubrid_lob_close) — Close
        BLOB/CLOB data
    -   [cubrid\_lob\_export](/book/cubrid.html#cubrid_lob_export) —
        Export BLOB/CLOB data to file
    -   [cubrid\_lob\_get](/book/cubrid.html#cubrid_lob_get) — Get
        BLOB/CLOB data
    -   [cubrid\_lob\_send](/book/cubrid.html#cubrid_lob_send) — Read
        BLOB/CLOB data and send straight to browser
    -   [cubrid\_lob\_size](/book/cubrid.html#cubrid_lob_size) — Get
        BLOB/CLOB data size
    -   [cubrid\_lob2\_bind](/book/cubrid.html#cubrid_lob2_bind) — Bind
        a lob object or a string as a lob object to a prepared statement
        as parameters
    -   [cubrid\_lob2\_close](/book/cubrid.html#cubrid_lob2_close) —
        Close LOB object
    -   [cubrid\_lob2\_export](/book/cubrid.html#cubrid_lob2_export) —
        Export the lob object to a file
    -   [cubrid\_lob2\_import](/book/cubrid.html#cubrid_lob2_import) —
        Import BLOB/CLOB data from a file
    -   [cubrid\_lob2\_new](/book/cubrid.html#cubrid_lob2_new) — Create
        a lob object
    -   [cubrid\_lob2\_read](/book/cubrid.html#cubrid_lob2_read) — Read
        from BLOB/CLOB data
    -   [cubrid\_lob2\_seek64](/book/cubrid.html#cubrid_lob2_seek64) —
        Move the cursor of a lob object
    -   [cubrid\_lob2\_seek](/book/cubrid.html#cubrid_lob2_seek) — Move
        the cursor of a lob object
    -   [cubrid\_lob2\_size64](/book/cubrid.html#cubrid_lob2_size64) —
        Get a lob object's size
    -   [cubrid\_lob2\_size](/book/cubrid.html#cubrid_lob2_size) — Get a
        lob object's size
    -   [cubrid\_lob2\_tell64](/book/cubrid.html#cubrid_lob2_tell64) —
        Tell the cursor position of the LOB object
    -   [cubrid\_lob2\_tell](/book/cubrid.html#cubrid_lob2_tell) — Tell
        the cursor position of the LOB object
    -   [cubrid\_lob2\_write](/book/cubrid.html#cubrid_lob2_write) —
        Write to a lob object
    -   [cubrid\_lock\_read](/book/cubrid.html#cubrid_lock_read) — Set a
        read lock on the given OID
    -   [cubrid\_lock\_write](/book/cubrid.html#cubrid_lock_write) — Set
        a write lock on the given OID
    -   [cubrid\_move\_cursor](/book/cubrid.html#cubrid_move_cursor) —
        Move the cursor in the result
    -   [cubrid\_next\_result](/book/cubrid.html#cubrid_next_result) —
        Get result of next query when executing multiple SQL statements
    -   [cubrid\_num\_cols](/book/cubrid.html#cubrid_num_cols) — Return
        the number of columns in the result set
    -   [cubrid\_num\_rows](/book/cubrid.html#cubrid_num_rows) — Get the
        number of rows in the result set
    -   [cubrid\_pconnect\_with\_url](/book/cubrid.html#cubrid_pconnect_with_url)
        — Open a persistent connection to CUBRID server
    -   [cubrid\_pconnect](/book/cubrid.html#cubrid_pconnect) — Open a
        persistent connection to a CUBRID server
    -   [cubrid\_prepare](/book/cubrid.html#cubrid_prepare) — Prepare a
        SQL statement for execution
    -   [cubrid\_put](/book/cubrid.html#cubrid_put) — Update a column
        using OID
    -   [cubrid\_rollback](/book/cubrid.html#cubrid_rollback) — Roll
        back a transaction
    -   [cubrid\_schema](/book/cubrid.html#cubrid_schema) — Get the
        requested schema information
    -   [cubrid\_seq\_drop](/book/cubrid.html#cubrid_seq_drop) — Delete
        an element from sequence type column using OID
    -   [cubrid\_seq\_insert](/book/cubrid.html#cubrid_seq_insert) —
        Insert an element to a sequence type column using OID
    -   [cubrid\_seq\_put](/book/cubrid.html#cubrid_seq_put) — Update
        the element value of sequence type column using OID
    -   [cubrid\_set\_add](/book/cubrid.html#cubrid_set_add) — Insert a
        single element to set type column using OID
    -   [cubrid\_set\_autocommit](/book/cubrid.html#cubrid_set_autocommit)
        — Set autocommit mode of the connection
    -   [cubrid\_set\_db\_parameter](/book/cubrid.html#cubrid_set_db_parameter)
        — Sets the CUBRID database parameters
    -   [cubrid\_set\_drop](/book/cubrid.html#cubrid_set_drop) — Delete
        an element from set type column using OID
    -   [cubrid\_set\_query\_timeout](/book/cubrid.html#cubrid_set_query_timeout)
        — Set the timeout time of query execution
    -   [cubrid\_version](/book/cubrid.html#cubrid_version) — Get the
        CUBRID PHP module's version
-   [CUBRID MySQL
    兼容性函数](/book/cubrid.html#CUBRID%20MySQL%20兼容性函数)
    -   [cubrid\_affected\_rows](/book/cubrid.html#cubrid_affected_rows)
        — Return the number of rows affected by the last SQL statement
    -   [cubrid\_client\_encoding](/book/cubrid.html#cubrid_client_encoding)
        — Return the current CUBRID connection charset
    -   [cubrid\_close](/book/cubrid.html#cubrid_close) — Close CUBRID
        connection
    -   [cubrid\_data\_seek](/book/cubrid.html#cubrid_data_seek) — Move
        the internal row pointer of the CUBRID result
    -   [cubrid\_db\_name](/book/cubrid.html#cubrid_db_name) — Get db
        name from results of cubrid\_list\_dbs
    -   [cubrid\_errno](/book/cubrid.html#cubrid_errno) — Return the
        numerical value of the error message from previous CUBRID
        operation
    -   [cubrid\_error](/book/cubrid.html#cubrid_error) — Get the error
        message
    -   [cubrid\_fetch\_array](/book/cubrid.html#cubrid_fetch_array) —
        Fetch a result row as an associative array, a numeric array, or
        both
    -   [cubrid\_fetch\_assoc](/book/cubrid.html#cubrid_fetch_assoc) —
        Return the associative array that corresponds to the fetched row
    -   [cubrid\_fetch\_field](/book/cubrid.html#cubrid_fetch_field) —
        Get column information from a result and return as an object
    -   [cubrid\_fetch\_lengths](/book/cubrid.html#cubrid_fetch_lengths)
        — Return an array with the lengths of the values of each field
        from the current row
    -   [cubrid\_fetch\_object](/book/cubrid.html#cubrid_fetch_object) —
        Fetch the next row and return it as an object
    -   [cubrid\_fetch\_row](/book/cubrid.html#cubrid_fetch_row) —
        Return a numerical array with the values of the current row
    -   [cubrid\_field\_flags](/book/cubrid.html#cubrid_field_flags) —
        Return a string with the flags of the given field offset
    -   [cubrid\_field\_len](/book/cubrid.html#cubrid_field_len) — Get
        the maximum length of the specified field
    -   [cubrid\_field\_name](/book/cubrid.html#cubrid_field_name) —
        Return the name of the specified field index
    -   [cubrid\_field\_seek](/book/cubrid.html#cubrid_field_seek) —
        Move the result set cursor to the specified field offset
    -   [cubrid\_field\_table](/book/cubrid.html#cubrid_field_table) —
        Return the name of the table of the specified field
    -   [cubrid\_field\_type](/book/cubrid.html#cubrid_field_type) —
        Return the type of the column corresponding to the given field
        offset
    -   [cubrid\_list\_dbs](/book/cubrid.html#cubrid_list_dbs) — Return
        an array with the list of all existing CUBRID databases
    -   [cubrid\_num\_fields](/book/cubrid.html#cubrid_num_fields) —
        Return the number of columns in the result set
    -   [cubrid\_ping](/book/cubrid.html#cubrid_ping) — Ping a server
        connection or reconnect if there is no connection
    -   [cubrid\_query](/book/cubrid.html#cubrid_query) — Send a CUBRID
        query
    -   [cubrid\_real\_escape\_string](/book/cubrid.html#cubrid_real_escape_string)
        — Escape special characters in a string for use in an SQL
        statement
    -   [cubrid\_result](/book/cubrid.html#cubrid_result) — Return the
        value of a specific field in a specific row
    -   [cubrid\_unbuffered\_query](/book/cubrid.html#cubrid_unbuffered_query)
        — Perform a query without fetching the results into memory
-   [CUBRID
    过时的别名和函数](/book/cubrid.html#CUBRID%20过时的别名和函数)
    -   [cubrid\_load\_from\_glo](/book/cubrid.html#cubrid_load_from_glo)
        — Read data from a GLO instance and save it in a file
    -   [cubrid\_new\_glo](/book/cubrid.html#cubrid_new_glo) — Create a
        glo instance
    -   [cubrid\_save\_to\_glo](/book/cubrid.html#cubrid_save_to_glo) —
        Save requested file in a GLO instance
    -   [cubrid\_send\_glo](/book/cubrid.html#cubrid_send_glo) — Read
        data from glo and send it to std output

这些函数可以让你访问CUBRID数据库服务。更多关于CUBRID的信息可以在<a href="http://www.cubrid.org/" class="link external">» CUBRID</a>找到。

在<a href="http://www.cubrid.org/documentation/" class="link external">» CUBRID 参考资料</a>
可以找到关于CUBRID的参考资料。

安装／配置
==========

**目录**

-   [需求](/book/cubrid.html#需求)
-   [安装](/book/cubrid.html#安装)
-   [运行时配置](/book/cubrid.html#运行时配置)
-   [资源类型](/book/cubrid.html#资源类型)

需求
----

为使这些函数可用，必须安装CUBRID和编译CUBRID PHP库，提供CUBRID支持。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/cubrid" class="link external">» https://pecl.php.net/package/cubrid</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

关于在Linux和Windows系统上的安装手册信息，请阅读包含在包中的这个文件`build-guide.html`。

运行时配置
----------

无运行时配置

资源类型
--------

在CUBRID中使用四种资源类型。第一个用于连接数据库的链接标识符，第二个是保存一个查询结果的资源类型，以及最后两个保存BLOB/CLOB查询结果的资源数据类型。

connection 标识符
-----------------

由 <span class="function">cubrid\_connect</span>, <span
class="function">cubrid\_connect\_with\_url</span>, <span
class="function">cubrid\_pconnect</span> 以及 <span
class="function">cubrid\_pconnect\_with\_url</span>返回的一个连接标识符。

request 标识符
--------------

由 <span class="function">cubrid\_prepare</span> 和 <span
class="function">cubrid\_execute</span>返回的一个请求标识符。

LOB 标识符
----------

由<span class="function">cubrid\_lob\_get</span>返回的一个LOB 标识符。

LOB2 标识符
-----------

由 <span
class="function">cubrid\_lob2\_new</span>返回或从结果集中获取的一个LOB
标识符

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

下列常量在执行SQL语句的时候可能被用到。它们可以被传递给<span
class="function">cubrid\_prepare</span> 和 <span
class="function">cubrid\_execute</span>。

| 常量                     | 说明                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------|
| CUBRID\_INCLUDE\_OID     | Determine whether to get OID during query execution.                                                 |
| CUBRID\_ASYNC            | Execute the query in asynchronous mode.                                                              |
| CUBRID\_EXEC\_QUERY\_ALL | Execute the query in synchronous mode. This flag must be set when executing multiple SQL statements. |

The following constants can be used when fetching the results to specify
fetch behaviour. They can be passed to <span
class="function">cubrid\_fetch</span> and <span
class="function">cubrid\_fetch\_array</span>.

| Constant       | Description                                                                                                                                                                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CUBRID\_NUM    | Get query result as a numeric array (0-default).                                                                                                                                                                                                                                                                                                                 |
| CUBRID\_ASSOC  | Get query result as an associative array.                                                                                                                                                                                                                                                                                                                        |
| CUBRID\_BOTH   | Get query result as both numeric and associative arrays (default value).                                                                                                                                                                                                                                                                                         |
| CUBRID\_OBJECT | Get query result an object.                                                                                                                                                                                                                                                                                                                                      |
| CUBRID\_LOB    | The constant CUBRID\_LOB can be used when you want to operate the lob object. It can be passed to <span class="function">cubrid\_fetch</span>, <span class="function">cubrid\_fetch\_row</span>, <span class="function">cubrid\_fetch\_array</span>, <span class="function">cubrid\_fetch\_assoc</span> and <span class="function">cubrid\_fetch\_object</span>. |

The following constants can be used when positioning the cursor in query
results. They can be passed to or returned by <span
class="function">cubrid\_move\_cursor</span>.

| Constant                | Description                                                                                                                              |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| CUBRID\_CURSOR\_FIRST   | Move current cursor to the first position in the result.                                                                                 |
| CUBRID\_CURSOR\_CURRENT | Move current cursor as a default value if the origin is not specified.                                                                   |
| CUBRID\_CURSOR\_LAST    | Move current cursor to the last position in the result.                                                                                  |
| CUBRID\_CURSOR\_SUCCESS | Returned value of <span class="function">cubrid\_move\_cursor</span> function in case of success. This flag has been removed from 8.4.1. |
| CUBRID\_NO\_MORE\_DATA  | Returned value of <span class="function">cubrid\_move\_cursor</span> function in case of failure. This flag has been removed from 8.4.1. |
| CUBRID\_CURSOR\_ERROR   | Returned value of <span class="function">cubrid\_move\_cursor</span> function in case of failure. This flag has been removed from 8.4.1. |

The following constants can be used when setting the auto-commit mode
for the database connection. They can be passed to <span
class="function">cubrid\_set\_autocommit</span> or returned by <span
class="function">cubrid\_get\_autocommit</span>.

| Constant                  | Description                   |
|---------------------------|-------------------------------|
| CUBRID\_AUTOCOMMIT\_TRUE  | Enable the auto-commit mode.  |
| CUBRID\_AUTOCOMMIT\_FALSE | Disable the auto-commit mode. |

The following constants can be used when setting the database parameter.
They can be passed to <span
class="function">cubrid\_set\_db\_parameter</span>.

| Constant                        | Description                                              |
|---------------------------------|----------------------------------------------------------|
| CUBRID\_PARAM\_ISOLATION\_LEVEL | Transaction isolation level for the database connection. |
| CUBRID\_PARAM\_LOCK\_TIMEOUT    | Transaction timeout in seconds.                          |

The following constants can be used when setting the transaction
isolation level. They can be passed to <span
class="function">cubrid\_set\_db\_parameter</span> or returned by <span
class="function">cubrid\_get\_db\_parameter</span>.

| Constant                                | Description                                                                                                                                                |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TRAN\_COMMIT\_CLASS\_UNCOMMIT\_INSTANCE | The lowest isolation level (1). A dirty, non-repeatable or phantom read may occur for the tuple and a non-repeatable read may occur for the table as well. |
| TRAN\_COMMIT\_CLASS\_COMMIT\_INSTANCE   | A relatively low isolation level (2). A dirty read does not occur, but non-repeatable or phantom read may occur.                                           |
| TRAN\_REP\_CLASS\_UNCOMMIT\_INSTANCE    | The default isolation of CUBRID (3). A dirty, non-repeatable or phantom read may occur for the tuple, but repeatable read is ensured for the table.        |
| TRAN\_REP\_CLASS\_COMMIT\_INSTANCE      | A relatively low isolation level (4). A dirty read does not occur, but non-repeatable or phantom read may.                                                 |
| TRAN\_REP\_CLASS\_REP\_INSTANCE         | A relatively high isolation level (5). A dirty or non-repeatable read does not occur, but a phantom read may.                                              |
| TRAN\_SERIALIZABLE                      | The highest isolation level (6). Problems concerning concurrency (e.g. dirty read, non-repeatable read, phantom read, etc.) do not occur.                  |

The following constants can be used when getting schema information.
They can be passed to <span class="function">cubrid\_schema</span>.

| Constant                          | Description                                                                                                                                                                                               |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CUBRID\_SCH\_CLASS                | Get name and type of table in CUBRID.                                                                                                                                                                     |
| CUBRID\_SCH\_VCLASS               | Get name and type of view in CUBRID.                                                                                                                                                                      |
| CUBRID\_SCH\_QUERY\_SPEC          | Get the query definition of view.                                                                                                                                                                         |
| CUBRID\_SCH\_ATTRIBUTE            | Get the attributes of table column.                                                                                                                                                                       |
| CUBRID\_SCH\_CLASS\_ATTRIBUTE     | Get the attributes of table.                                                                                                                                                                              |
| CUBRID\_SCH\_METHOD               | Get the instance method. The instance method is a method called by a class instance. It is used more often than the class method because most operations are executed in the instance.                    |
| CUBRID\_SCH\_CLASS\_METHOD        | Get the class method. The class method is a method called by a class object. It is usually used to create a new class instance or to initialize it. It is also used to access or update class attributes. |
| CUBRID\_SCH\_METHOD\_FILE         | Get the information of the file where the method of the table is defined.                                                                                                                                 |
| CUBRID\_SCH\_SUPERCLASS           | Get the name and type of table which table inherites attributes from.                                                                                                                                     |
| CUBRID\_SCH\_SUBCLASS             | Get the name and type of table which inherites attributes from this table.                                                                                                                                |
| CUBRID\_SCH\_CONSTRAINT           | Get the table constraints.                                                                                                                                                                                |
| CUBRID\_SCH\_TRIGGER              | Get the table triggers.                                                                                                                                                                                   |
| CUBRID\_SCH\_CLASS\_PRIVILEGE     | Get the privilege information of table.                                                                                                                                                                   |
| CUBRID\_SCH\_ATTR\_PRIVILEGE      | Get the privilege information of column.                                                                                                                                                                  |
| CUBRID\_SCH\_DIRECT\_SUPER\_CLASS | Get the direct super table of table.                                                                                                                                                                      |
| CUBRID\_SCH\_PRIMARY\_KEY         | Get the table primary key.                                                                                                                                                                                |
| CUBRID\_SCH\_IMPORTED\_KEYS       | Get imported keys of table.                                                                                                                                                                               |
| CUBRID\_SCH\_EXPORTED\_KEYS       | Get exported keys of table.                                                                                                                                                                               |
| CUBRID\_SCH\_CROSS\_REFERENCE     | Get reference relationship of tow tables.                                                                                                                                                                 |

The following constants can be used when reporting errors.
在报告错误的时候，下列常量可能被用到。它们可能由<span
class="function">cubrid\_error\_code\_facility</span>返回。

| 常量                     | 说明                                     |
|--------------------------|------------------------------------------|
| CUBRID\_FACILITY\_DBMS   | The error occurred in CUBRID dbms.       |
| CUBRID\_FACILITY\_CAS    | The error occurred in CUBRID broker cas. |
| CUBRID\_FACILITY\_CCI    | The error occurred in CUBRID cci.        |
| CUBRID\_FACILITY\_CLIENT | The error occurred in CUBRID PHP client. |

范例
====

下面是一个在PHP和CUBRID建立连接的简单的例子。本节将覆盖最基本和最显著的特性。下面的代码需要连接CUBRID数据库，这意味着
CUBRID服务和 CUBRID Broker已经运行。

下面用demodb数据库作为例子举例。默认在安装时就创建了。确认此数据库已经被创建。

**示例 \#1 数据查询的例子**

``` php
<html>
    <head>
    <meta http-equiv="content-type" content="text/html; charset=euc-kr">
    </head>
    <body>
    <center>
    <table border=2>
    <?php
        /**
         * Set server information for CUBRID connection. host_ip is the IP
         * address where the CUBRID Broker is installed (localhost in this
         * example), and host_port is the port number of the CUBRID Broker.
         * The port number is the default given during the installation.
         * For details, see "Administrator's Guide."
         */
        $host_ip = "localhost";
        $host_port = 33000;
        $db_name = "demodb";
        /**
         * Connect to CUBRID Server. Do not make the actual connection, but
         * only retain the connection information. The reason for not making
         * the actual connection is to handle transaction more efficiently
         * in the 3-tier architecture. 
         */
        $cubrid_con = @cubrid_connect($host_ip, $host_port, $db_name);
 
        if (!$cubrid_con) {
            echo "Database Connection Error";
            exit;
        }
    ?>
    <?php
        $sql = "select sports, count(players) as players from event group by sports";
        /**
         * Request the CUBRID Server for the results of the SQL statement.
         * Now make the actual connection to the CUBRID Server.
         */
        $result = cubrid_execute($cubrid_con, $sql);
 
        if ($result) {
            /**
             * Get the column names from the result set created by the SQL query.
             */
            $columns = cubrid_column_names($result);
            /**
             * Get the number of columns in the result set created by the SQL query.
             */
            $num_fields = cubrid_num_cols($result);
            /**
             * List the column names of the result set on the screen. 
             */
            echo("<tr>");
 
            while (list($key, $colname) = each($columns)) {
                echo("<td align=center>$colname</td>");
            }
 
            echo("</tr>");
 
            /**
             * Get the results from the result set.
             */
            while ($row = cubrid_fetch($result)) {
                echo("<tr>");
 
                for ($i = 0; $i < $num_fields; $i++) {
                    echo("<td align=center>");
                    echo($row[$i]);
                    echo("</td>");
                }
 
                echo("</tr>");
            }
        }
        /**
         * The PHP module in the CUBRID runs in a 3-tier architecture. Even when
         * calling SELECT for transaction processing, it is processed as a part
         * of the transaction. Therefore, the transaction needs to be rolled back
         * by calling commit or rollback even though SELECT was called for smooth
         * performance.
         */
        cubrid_commit($cubrid_con);
        cubrid_disconnect($cubrid_con);
    ?>
    </body>
    </html>
```

**示例 \#2 数据插入的例子**

``` php
<html>
    <head>
    <meta http-equiv="content-type" content="text/html; charset=euc- kr">
    </head>
    <body>
    <center>
    <table border=2>
    <?php
        /**
         * host_ip is the IP address where the CUBRID Broker is installed
         * host_port is the port number of the CUBRID Broker
         * db_name is the name of CUBRID Database
         */
        $host_ip = "localhost";
        $host_port = 33000;
        $db_name = "demodb";
        $cubrid_con = @cubrid_connect($host_ip, $host_port, $db_name);
 
        if (!$cubrid_con) {
            echo "Database Connection Error";
            exit;
        }
    ?>
    <?php
        $sql = "insert into olympic (host_year,host_nation,host_city,"
            . "opening_date,closing_date) values (2008, 'China', 'Beijing',"
            . "to_date('08-08-2008','mm-dd- yyyy'),to_date('08-24-2008','mm-dd-yyyy')) ;"
        $result = cubrid_execute($cubrid_con, $sql);
        if ($result) {
            /**
             * Handled successfully, so commit.
             */
            cubrid_commit($cubrid_con);
            echo("Inserted successfully ");
        } else {
            /**
             * Error occurred, so the error message is output and rollback is called.
             */
            echo(cubrid_error_msg());
            cubrid_rollback($cubrid_con);
        }
        cubrid_disconnect($cubrid_con);
    ?>
    </body>
    </html>
```

cubrid\_bind
============

Bind variables to a prepared statement as parameters

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_bind</span> ( <span class="methodparam"><span
class="type">resource</span> `$req_identifier`</span> , <span
class="methodparam"><span class="type">int</span> `$bind_index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$bind_value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$bind_value_type`</span> \] )

The <span class="function">cubrid\_bind</span> function is used to bind
values to a corresponding named or question mark placeholder in the SQL
statement that was passed to <span
class="function">cubrid\_prepare</span>. If `bind_value_type` is not
given, string will be the default.

> **Note**:
>
> If the type of data to be bound is BLOB/CLOB, CUBRID will try to map
> the data as a PHP stream. If the actually bind value type is not
> stream, CUBRID will convert it to string, and use it as the full path
> and file name of a file on the client filesystem.
>
> If the type of data to be bound explicitly is ENUM, the $bind\_value
> argument should be the enum element which is in string format.
>
> In CUBRID shard envrioment, the $bind\_value\_type must be included in
> the cubrid\_bind function.

The following table shows the types of substitute values.

| Support       | Bind Type         | Corresponding SQL Type |
|---------------|-------------------|------------------------|
| Supported     | STRING            | CHAR, VARCHAR          |
|               | NCHAR             | NCHAR, NVARCHAR        |
|               | BIT               | BIT, VARBIT            |
|               | NUMERIC or NUMBER | SHORT, INT, NUMERIC    |
|               | FLOAT             | FLOAT                  |
|               | DOUBLE            | DOUBLE                 |
|               | TIME              | TIME                   |
|               | DATE              | DATE                   |
|               | TIMESTAMP         | TIMESTAMP              |
|               | OBJECT            | OBJECT                 |
|               | ENUM              | ENUM                   |
|               | BLOB              | BLOB                   |
|               | CLOB              | CLOB                   |
|               | NULL              | NULL                   |
| Not supported | SET               | SET                    |
|               | MULTISET          | MULTISET               |
|               | SEQUENCE          | SEQUENCE               |

### 参数

`req_identifier`  
Request identifier as a result of <span
class="function">cubrid\_prepare</span>.

`bind_index`  
Location of binding parameters. It starts with 1.

`bind_value`  
Actual value for binding.

`bind_value_type`  
A type of the value to bind. (It is omitted by default. Thus, the system
internally uses string by default. However, you need to specify the
exact type of the value as an argument when they are NCHAR, BIT, or
BLOB/CLOB).

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 更新日志

| 版本  | 说明                                |
|-------|-------------------------------------|
| 8.3.1 | Added BLOB/CLOB data types support. |

### 范例

**示例 \#1 <span class="function">cubrid\_bind</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$result = cubrid_execute($conn, "SELECT code FROM event WHERE sports='Basketball' and gender='M'");
$row = cubrid_fetch_array($result, CUBRID_ASSOC);
$event_code = $row["code"];

cubrid_close_request($result);

$game_req = cubrid_prepare($conn, "SELECT athlete_code FROM game WHERE host_year=1992 and event_code=? and nation_code='USA'");
cubrid_bind($game_req, 1, $event_code, "number");
cubrid_execute($game_req);

printf("--- Dream Team (1992 United States men's Olympic basketball team) ---\n");
while ($athlete_code = cubrid_fetch_array($game_req, CUBRID_NUM)) {
    $athlete_req = cubrid_prepare($conn, "SELECT name FROM athlete WHERE code=? AND nation_code='USA' AND event='Basketball' AND gender='M'");
    cubrid_bind($athlete_req, 1, $athlete_code[0], "number");
    cubrid_execute($athlete_req);
    $row = cubrid_fetch_assoc($athlete_req);
    printf("%s\n", $row["name"]);
}

cubrid_close_request($game_req);
cubrid_close_request($athlete_req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    --- Dream Team (1992 United States men's Olympic basketball team) ---
    Stockton John
    Robinson David
    Pippen Scottie
    Mullin C.
    Malone Karl
    Laettner C.
    Jordan Michael
    Johnson Earvin
    Ewing Patrick
    Drexler Clyde
    Bird Larry
    Barkley Charles

**示例 \#2 <span class="function">cubrid\_bind</span> BLOB/CLOB
example**

``` php
<?php
$con = cubrid_connect("localhost", 33000, "demodb", "dba", "");
if ($con) {
    cubrid_execute($con,"DROP TABLE if exists php_cubrid_lob_test");
    cubrid_execute($con,"CREATE TABLE php_cubrid_lob_test (doc_content CLOB)");
    $sql = "INSERT INTO php_cubrid_lob_test(doc_content) VALUES(?)"; 
    $req = cubrid_prepare($con, $sql); 

    $fp = fopen("book.txt", "rb");

    cubrid_bind($req, 1, $fp, "clob"); 
    cubrid_execute($req);  
}
?>
```

**示例 \#3 <span class="function">cubrid\_bind</span> BLOB/CLOB
example**

``` php
<?php
$con = cubrid_connect("localhost", 33000, "demodb", "dba", "");
if ($con) {
    cubrid_execute($con,"DROP TABLE if exists php_cubrid_lob_test");
    cubrid_execute($con,"CREATE TABLE php_cubrid_lob_test (image BLOB)");
    $sql = "INSERT INTO php_cubrid_lob_test(image) VALUES(?)"; 
    $req = cubrid_prepare($con, $sql); 

    cubrid_bind($req, 1, "cubrid_logo.png", "blob"); 
    cubrid_execute($req);  
}
?>
```

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_prepare</span>

cubrid\_close\_prepare
======================

Close the request handle

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_close\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

The <span class="function">cubrid\_close\_prepare</span> function closes
the request handle given by the `req_identifier` argument, and releases
the memory region related to the handle. It is an alias of <span
class="function">cubrid\_close\_request</span>.

### 参数

`req_identifier`  
Request identifier.

### 返回值

Return **`true`** on success.

### 范例

**示例 \#1 <span class="function">cubrid\_close\_prepare</span>
example**

``` php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb", "dba", "");
if ($con) {
   echo "connected successfully";
   $req = cubrid_execute ( $con, "select * from members", 
                           CUBRID_INCLUDE_OID | CUBRID_ASYNC);
   if ($req) {
      while ( list ($id, $name) = cubrid_fetch ($req) ){
         echo $id;
         echo $name;
      } 
      cubrid_close_prepare($req); // or you can use cubrid_close_request($req)
   }
   cubrid_disconnect($con);
}
?>
```

### 参见

-   <span class="function">cubrid\_close\_request</span>

cubrid\_close\_request
======================

Close the request handle

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_close\_request</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

The <span class="function">cubrid\_close\_request</span> function closes
the request handle given by the `req_identifier` argument, and releases
the memory region related to the handle. It is an alias of <span
class="function">cubrid\_close\_prepare</span>.

### 参数

`req_identifier`  
Request identifier.

### 返回值

Return **`true`** on success.

### 范例

**示例 \#1 <span class="function">cubrid\_close\_request</span>
example**

``` php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb", "dba", "");
if ($con) {
   echo "connected successfully";
   $req = cubrid_execute ( $con, "select * from members", 
                           CUBRID_INCLUDE_OID | CUBRID_ASYNC);
   if ($req) {
      while ( list ($id, $name) = cubrid_fetch ($req) ){
         echo $id;
         echo $name;
      } 
      cubrid_close_request($req); // or you can use cubrid_close_prepare($req)
   }
   cubrid_disconnect($con);
}
?>
```

### 参见

-   <span class="function">cubrid\_close\_prepare</span>

cubrid\_col\_get
================

Get contents of collection type column using OID

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_col\_get</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
)

The <span class="function">cubrid\_col\_get</span> function is used to
get contents of the elements of the collection type (set, multiset,
sequence) attribute you requested as an array.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to read.

`attr_name`  
Attribute name that you want to read from the instance.

### 返回值

Array (0-based numerical array) containing the elements you requested,
when process is successful;

**`false`** (to distinguish the error from the situation of attribute
having empty collection or NULL, in case of error, a warning message is
shown; in such case you can check the error by using <span
class="function">cubrid\_error\_code</span>), when process is
unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_col\_get</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

$size = cubrid_col_size($conn, $oid, "b");
var_dump($size);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
    }
    int(3)

cubrid\_col\_size
=================

Get the number of elements in collection type column using OID

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_col\_size</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
)

The <span class="function">cubrid\_col\_size</span> function is used to
get the number of elements in a collection type (set, multiset,
sequence) attribute.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID the instance that you want to work with.

`attr_name`  
Name of the attribute that you want to work with.

### 返回值

Number of elements, when process is successful.

**`false`**, when process is unsuccessful.

### 更新日志

| 版本  | 说明                                                                     |
|-------|--------------------------------------------------------------------------|
| 8.3.1 | Change return value: when process is unsuccessful, return false, not -1. |

### 范例

**示例 \#1 <span class="function">cubrid\_col\_size</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

$size = cubrid_col_size($conn, $oid, "b");
var_dump($size);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
    }
    int(3)

cubrid\_column\_names
=====================

Get the column names in result

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_column\_names</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

The <span class="function">cubrid\_column\_names</span> function is used
to get the column names of the query result by using `req_identifier`.

### 参数

`req_identifier`  
Request identifier.

### 返回值

Array of string values containing the column names, when process is
successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_column\_names</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Column Names", "Column Types", "Column Maxlen");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Column Names                   Column Types                   Column Maxlen  
    host_year                      integer                        11             
    event_code                     integer                        11             
    athlete_code                   integer                        11             
    stadium_code                   integer                        11             
    nation_code                    char                           3              
    medal                          char                           1              
    game_date                      date                           10             

### 参见

-   <span class="function">cubrid\_prepare</span>
-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_column\_types</span>

cubrid\_column\_types
=====================

Get column types in result

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_column\_types</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

The <span class="function">cubrid\_column\_types</span> function gets
column types of query results by using `req_identifier`.

### 参数

`req_identifier`  
Request identifier.

### 返回值

Array of string values containing the column types, when process is
successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_column\_types</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Column Names", "Column Types", "Column Maxlen");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Column Names                   Column Types                   Column Maxlen  
    host_year                      integer                        11             
    event_code                     integer                        11             
    athlete_code                   integer                        11             
    stadium_code                   integer                        11             
    nation_code                    char                           3              
    medal                          char                           1              
    game_date                      date                           10             

### 参见

-   <span class="function">cubrid\_column\_names</span>
-   <span class="function">cubrid\_prepare</span>
-   <span class="function">cubrid\_execute</span>

cubrid\_commit
==============

Commit a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_commit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> )

The <span class="function">cubrid\_commit</span> function is used to
execute commit on the transaction pointed by `conn_identifier`,
currently in progress. Connection to the server is closed after the
<span class="function">cubrid\_commit</span> function is called;
However, the connection handle is still valid.

In CUBRID PHP, auto-commit mode is disabled by default for transaction
management. You can set it by using <span
class="function">cubrid\_set\_autocommit</span>. You can get its status
by using <span class="function">cubrid\_get\_autocommit</span>. Before
you start a transaction, remember to disable the auto-commit mode.

### 参数

`conn_identifier`  
Connection identifier.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_commit</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE publishers");

$sql = <<<EOD
CREATE TABLE publishers(
pub_id CHAR(3), 
pub_name VARCHAR(20), 
city VARCHAR(15), 
state CHAR(2), 
country VARCHAR(15)
)
EOD;
cubrid_set_autocommit($conn,false);
if (!cubrid_execute($conn, $sql)) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n", cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}

$req = cubrid_prepare($conn, "INSERT INTO publishers VALUES(?, ?, ?, ?, ?)");

$id_list = array("P01", "P02", "P03", "P04");
$name_list = array("Abatis Publishers", "Core Dump Books", "Schadenfreude Press", "Tenterhooks Press");
$city_list = array("New York", "San Francisco", "Hamburg", "Berkeley");
$state_list = array("NY", "CA", NULL, "CA");
$country_list = array("USA", "USA", "Germany", "USA");

for ($i = 0, $size = count($id_list); $i < $size; $i++) {
    cubrid_bind($req, 1, $id_list[$i]);
    cubrid_bind($req, 2, $name_list[$i]);
    cubrid_bind($req, 3, $city_list[$i]);
    cubrid_bind($req, 4, $state_list[$i]);
    cubrid_bind($req, 5, $country_list[$i]);

    if (!($ret = cubrid_execute($req))) {
        break;
    }
}

if (!$ret) {
    cubrid_rollback($conn);
} else {
    cubrid_commit($conn);

    $req = cubrid_execute($conn, "SELECT * FROM publishers");
    while ($result = cubrid_fetch_assoc($req)) {
        printf("%-3s %-20s %-15s %-3s %-15s\n", 
            $result["pub_id"], $result["pub_name"], $result["city"], $result["state"], $result["country"]);
    }
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    P01 Abatis Publishers    New York        NY  USA            
    P02 Core Dump Books      San Francisco   CA  USA            
    P03 Schadenfreude Press  Hamburg             Germany        
    P04 Tenterhooks Press    Berkeley        CA  USA            

### 参见

-   <span class="function">cubrid\_rollback</span>
-   <span class="function">cubrid\_get\_autocommit</span>
-   <span class="function">cubrid\_set\_autocommit</span>

cubrid\_connect\_with\_url
==========================

Establish the environment for connecting to CUBRID server

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_connect\_with\_url</span> ( <span
class="methodparam"><span class="type">string</span> `$conn_url`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$userid`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passwd`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$new_link`<span
class="initializer"> = **`false`**</span></span> \]\]\] )

The <span class="function">cubrid\_connect\_with\_url</span> function is
used to establish the environment for connecting to your server by using
connection information passed with an url string argument. If the HA
feature is enabled in CUBRID, you must specify the connection
information of the standby server, which is used for failover when
failure occurs, in the url string argument of this function. If the user
name and password is not given, then the "PUBLIC" connection will be
made by default.

\<url\> ::=
CUBRID:\<host\>:\<db\_name\>:\<db\_user\>:\<db\_password\>:\[?\<properties\>\]

\<properties\> ::= \<property\> \[&\<property\>\]

\<properties\> ::= alhosts=\<alternative\_hosts\>\[ &rctime=\<time\>\]

\<properties\> ::= login\_timeout=\<milli\_sec\>

\<properties\> ::= query\_timeout=\<milli\_sec\>

\<properties\> ::= disconnect\_on\_query\_timeout=true\|false

\<alternative\_hosts\> ::= \<standby\_broker1\_host\>:\<port\>
\[,\<standby\_broker2\_host\>:\<port\>\]

\<host\> := HOSTNAME \| IP\_ADDR

\<time\> := SECOND

\<milli\_sec\> := MILLI SECOND

-   host : A host name or IP address of the master database
-   db\_name : A name of the database
-   db\_user : A name of the database user
-   db\_password : A database user password
-   alhosts : Specifies the broker information of the standby server,
    which is used for failover when it is impossible to connect to the
    active server. You can specify multiple brokers for failover, and
    the connection to the brokers is attempted in the order listed in
    alhosts
-   rctime : An interval between the attempts to connect to the active
    broker in which failure occurred. After a failure occurs, the system
    connects to the broker specified by althosts (failover), terminates
    the transaction, and then attempts to connect to the active broker
    of the master database at every rctime. The default value is 600
    seconds.
-   login\_timeout : Timeout value (unit: msec.) for database login. The
    default value is 0, which means infinite postponement.
-   query\_timeout : Timeout value (unit: msec.) for query request. Upon
    timeout, a message to cancel requesting a query transferred to
    server is sent. The return value can depend on the
    disconnect\_on\_query\_timeout configuration; even though the
    message to cancel a request is sent to server, that request may
    succeed.
-   disconnect\_on\_query\_timeout : Configures a value whether to
    immediately return an error of function being executed upon timeout.
    The default value is false.

> **Note**:
>
> *?* and *:* that are used as identifiers in PHP connection URL can't
> be included in the password. The following is an example of a password
> that is invalid to use as connection URL because it contains "*?:*".
>
> $url = "CUBRID:localhost:33000:tdb:dba:12?:?login\_timeout=100";
>
> Passwords that contain *?* or *:* may be passed as a separate
> parameter.
>
> $url = "CUBRID:localhost:33000:tbd:::?login\_timeout=100";
>
> $conn = cubrid\_connect\_with\_url($url, "dba", "12?");
>
> If user or password is empty,you can't delete "*:*",the following is
> an example.
>
> $url = "CUBRID:localhost:33000:demodb:::";

### 参数

`conn_url`  
A character string that contains server connection information.

`userid`  
User name for the database.

`passwd`  
User password.

`new_link`  
If a second call is made to <span
class="function">cubrid\_connect\_with\_url</span> with the same
arguments, no new connection will be established, but instead, the
connection identifier of the already opened connection will be returned.
The `new_link` parameter modifies this behavior and makes <span
class="function">cubrid\_connect\_with\_url</span> always open a new
connection, even if <span
class="function">cubrid\_connect\_with\_url</span> was called before
with the same parameters.

### 返回值

Connection identifier, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_connect\_with\_url</span> url
without properties example**

``` php
<?php
$conn_url = "CUBRID:localhost:33000:demodb:dba::";
$con = cubrid_connect_with_url($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

**示例 \#2 <span class="function">cubrid\_connect\_with\_url</span> url
with properties example**

``` php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::?login_timeout=100"
$con = cubrid_connect_with_url ($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

### 参见

-   <span class="function">cubrid\_connect</span>
-   <span class="function">cubrid\_pconnect</span>
-   <span class="function">cubrid\_pconnect\_with\_url</span>
-   <span class="function">cubrid\_disconnect</span>
-   <span class="function">cubrid\_close</span>

cubrid\_connect
===============

Open a connection to a CUBRID Server

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_connect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dbname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$userid`</span> \[, <span
class="methodparam"><span class="type">string</span> `$passwd`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$new_link`<span class="initializer"> = **`false`**</span></span> \]\]\]
)

The <span class="function">cubrid\_connect</span> function is used to
establish the environment for connecting to your server by using your
server address, port number, database name, user name, and password. If
the user name and password is not given, then the "PUBLIC" connection
will be made by default.

### 参数

`host`  
Host name or IP address of CUBRID CAS server.

`port`  
Port number of CUBRID CAS server (BROKER\_PORT configured in
$CUBRID/conf/cubrid\_broker.conf).

`dbname`  
Name of database.

`userid`  
User name for the database. If not given, the default value is "public".

`passwd`  
User password. If not given, the default value is "".

`new_link`  
If a second call is made to <span
class="function">cubrid\_connect</span> with the same arguments, no new
connection will be established, but instead, the connection identifier
of the already opened connection will be returned. The `new_link`
parameter modifies this behavior and makes <span
class="function">cubrid\_connect</span> always open a new connection,
even if <span class="function">cubrid\_connect</span> was called before
with the same parameters.

### 返回值

Connection identifier, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_connect</span> example**

``` php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    CUBRID PHP Version:            9.1.0.0001

    PARAM_ISOLATION_LEVEL          3
    LOCK_TIMEOUT                   -1
    MAX_STRING_LENGTH              1073741823
    PARAM_AUTO_COMMIT              1

    Server Info:                   9.1.0.0212
    Client Info:                   9.1.0

    CUBRID Charset:                iso8859-1

### 参见

-   <span class="function">cubrid\_pconnect</span>
-   <span class="function">cubrid\_connect\_with\_url</span>
-   <span class="function">cubrid\_pconnect\_with\_url</span>
-   <span class="function">cubrid\_disconnect</span>
-   <span class="function">cubrid\_close</span>

cubrid\_current\_oid
====================

Get OID of the current cursor location

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_current\_oid</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

The <span class="function">cubrid\_current\_oid</span> function is used
to get the oid of the current cursor location from the query result. To
use <span class="function">cubrid\_current\_oid</span>, the query
executed must be a updatable query, and the CUBRID\_INCLUDE\_OID option
must be included during the query execution.

### 参数

`req_identifier`  
Request identifier.

### 返回值

Oid of current cursor location, when process is successful

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_current\_oid</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code", CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);
$res = cubrid_get($conn, $oid);

print_r($res);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Array
    (
        [s_name] => X
        [f_name] => Mixed
    )

### 参见

-   <span class="function">cubrid\_execute</span>

cubrid\_disconnect
==================

Close a database connection

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_disconnect</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

The <span class="function">cubrid\_disconnect</span> function closes the
connection handle and disconnects from server. If any request handle is
not closed at this point, it will be closed. It is similar to the CUBRID
MySQL compatible function <span class="function">cubrid\_close</span>.

### 参数

`conn_identifier`  
Connection identifier.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_disconnect</span> example**

``` php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb");
if ($con) {
   echo "connected successfully";
   
   $req = cubrid_execute( $con, "create table person(id int,name char(10))");
   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   
   $req = cubrid_execute( $con, "insert into person values(1,'James')");
   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

### 参见

-   <span class="function">cubrid\_close</span>
-   <span class="function">cubrid\_connect</span>
-   <span class="function">cubrid\_connect\_with\_url</span>

cubrid\_drop
============

Delete an instance using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_drop</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$oid`</span> )

The <span class="function">cubrid\_drop</span> function is used to
delete an instance from database by using the `oid` of the instance.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
Oid of the instance that you want to delete.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_drop</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

printf("--- Before Drop: ---\n");
$attr = cubrid_get($conn, $oid);
var_dump($attr);

if (cubrid_drop($conn, $oid)) {
    cubrid_commit($conn);
} else {
    cubrid_rollback($conn);
}

cubrid_close_request($req);

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

printf("\n--- After Drop: ---\n");
$attr = cubrid_get($conn, $oid);
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    --- Before Drop: ---
    array(4) {
      ["a"]=>
      string(1) "1"
      ["b"]=>
      array(3) {
        [0]=>
        string(1) "1"
        [1]=>
        string(1) "2"
        [2]=>
        string(1) "3"
      }
      ["c"]=>
      array(4) {
        [0]=>
        string(2) "11"
        [1]=>
        string(2) "22"
        [2]=>
        string(2) "33"
        [3]=>
        string(3) "333"
      }
      ["d"]=>
      string(10) "a         "
    }

    --- After Drop: ---
    array(4) {
      ["a"]=>
      string(1) "2"
      ["b"]=>
      array(3) {
        [0]=>
        string(1) "4"
        [1]=>
        string(1) "5"
        [2]=>
        string(1) "7"
      }
      ["c"]=>
      array(4) {
        [0]=>
        string(2) "44"
        [1]=>
        string(2) "55"
        [2]=>
        string(2) "66"
        [3]=>
        string(3) "666"
      }
      ["d"]=>
      string(10) "b         "
    }

### 参见

-   <span class="function">cubrid\_is\_instance</span>

cubrid\_error\_code\_facility
=============================

Get the facility code of error

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_error\_code\_facility</span> ( <span
class="methodparam">void</span> )

The <span class="function">cubrid\_error\_code\_facility</span> function
is used to get the facility code (level in which the error occurred)
from the error code of the error that occurred during the API execution.
Usually, you can get the error code when API returns false as its return
value.

### 参数

此函数没有参数。

### 返回值

Facility code of the error code that occurred: CUBRID\_FACILITY\_DBMS,
CUBRID\_FACILITY\_CAS, CUBRID\_FACILITY\_CCI, CUBRID\_FACILITY\_CLIENT

### 范例

**示例 \#1 <span class="function">cubrid\_error\_code\_facility</span>
example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = @cubrid_execute($conn, "SELECT * FROM unknown");
if (!$req) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n", 
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

以上例程会输出：

    Error facility: 1
    Error code: -493
    Error msg: Syntax: In line 1, column 15 before END OF STATEMENT
    Syntax error: unexpected 'unknown'

### 参见

-   <span class="function">cubrid\_error\_code</span>
-   <span class="function">cubrid\_error\_msg</span>

cubrid\_error\_code
===================

Get error code for the most recent function call

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_error\_code</span> ( <span
class="methodparam">void</span> )

The <span class="function">cubrid\_error\_code</span> function is used
to get the error code of the error that occurred during the API
execution. Usually, it gets the error code when API returns false as its
return value.

### 参数

此函数没有参数。

### 返回值

Error code of the error that occurred, or *0* (zero) if no error
occurred.

### 范例

**示例 \#1 <span class="function">cubrid\_error\_code</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_prepare($conn , "SELECT * FROM code WHERE s_name=?");

$req = @cubrid_execute($req);
if (!$req) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n", 
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

以上例程会输出：

    Error facility: 4
    Error code: -30015
    Error msg: Some parameter not binded

### 参见

-   <span class="function">cubrid\_error\_code\_facility</span>
-   <span class="function">cubrid\_error\_msg</span>

cubrid\_error\_msg
==================

Get last error message for the most recent function call

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_error\_msg</span> ( <span
class="methodparam">void</span> )

The <span class="function">cubrid\_error\_msg</span> function is used to
get the error message that occurred during the use of CUBRID API.
Usually, it gets error message when API returns false as its return
value.

### 参数

此函数没有参数。

### 返回值

Error message that occurred.

### 范例

**示例 \#1 <span class="function">cubrid\_error\_msg</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

if (!@cubrid_schema($conn, 100000)) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n", 
        cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}
?>
```

以上例程会输出：

    Error facility: 2
    Error code: -10015
    Error msg: Invalid T_CCI_SCH_TYPE value

### 参见

-   <span class="function">cubrid\_error\_code</span>
-   <span class="function">cubrid\_error\_code\_facility</span>

cubrid\_execute
===============

Execute a prepared SQL statement

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_execute</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$sql`</span> \[, <span
class="methodparam"><span class="type">int</span> `$option`<span
class="initializer"> = 0</span></span> \] )

<span class="type">bool</span> <span
class="methodname">cubrid\_execute</span> ( <span
class="methodparam"><span class="type">resource</span>
`$request_identifier`</span> \[, <span class="methodparam"><span
class="type">int</span> `$option`<span class="initializer"> =
0</span></span> \] )

The <span class="function">cubrid\_execute</span> function is used to
execute the given SQL statement. It executes the query by using
`conn_identifier` and SQL, and then returns the request identifier
created. It is used for simple execution of query, where the parameter
binding is not needed. In addition, the <span
class="function">cubrid\_execute</span> function is used to execute the
prepared statement by means of <span
class="function">cubrid\_prepare</span> and <span
class="function">cubrid\_bind</span>. At this time, you need to specify
arguments of `request_identifier` and `option`.

The `option` is used to determine whether to get OID after query
execution and whether to execute the query in synchronous or
asynchronous mode. CUBRID\_INCLUDE\_OID and CUBRID\_ASYNC (or
CUBRID\_EXEC\_QUERY\_ALL if you want to execute multiple SQL statements)
can be specified by using a bitwise OR operator. If not specified,
neither of them isselected. If the flag CUBRID\_EXEC\_QUERY\_ALL is set,
a synchronous mode (sync\_mode) is used to retrieve query results, and
in such cases the following rules are applied:

-   The return value is the result of the first query.
-   If an error occurs in any query, the execution is processed as a
    failure.
-   In a query composed of q1 q2 q3, if an error occurs in q2 after q1
    succeeds the execution, the result of q1 remains valid. That is, the
    previous successful query executions are not rolled back when an
    error occurs.
-   If a query is executed successfully, the result of the second query
    can be obtained using <span
    class="function">cubrid\_next\_result</span>.

If the first argument is `request_identifier` to execute the <span
class="function">cubrid\_prepare</span> function, you can specify an
option, CUBRID\_ASYNC only.

### 参数

`conn_identifier`  
Connection identifier.

`sql`  
SQL to be executed.

`option`  
Query execution option CUBRID\_INCLUDE\_OID, CUBRID\_ASYNC,
CUBRID\_EXEC\_QUERY\_ALL.

`request_identifier`  
<span class="function">cubrid\_prepare</span> identifier.

### 返回值

Request identifier, when process is successful and first param is
conn\_identifier; **`true`**, when process is successful and first
argument is request\_identifier.

**`false`**, when process is unsuccessful.

### 更新日志

| 版本  | 说明                                     |
|-------|------------------------------------------|
| 8.4.0 | Add new option CUBRID\_EXEC\_QUERY\_ALL. |

### 范例

**示例 \#1 <span class="function">cubrid\_execute</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$result = cubrid_execute($conn, "SELECT code FROM event WHERE name='100m Butterfly' and gender='M'", CUBRID_ASYNC);
$row = cubrid_fetch_array($result, CUBRID_ASSOC);
$event_code = $row["code"];

cubrid_close_request($result);

$history_req = cubrid_prepare($conn, "SELECT * FROM history WHERE event_code=?");
cubrid_bind($history_req, 1, $event_code, "number");
cubrid_execute($history_req);

printf("%-20s %-9s %-10s %-5s\n", "athlete", "host_year", "score", "unit");
while ($row = cubrid_fetch_array($history_req, CUBRID_ASSOC)) {
    printf("%-20s %-9s %-10s %-5s\n", 
        $row["athlete"], $row["host_year"], $row["score"], $row["unit"]);
}

cubrid_close_request($history_req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    athlete              host_year score      unit 
    Phelps Michael       2004      51.25      time 

### 参见

-   <span class="function">cubrid\_prepare</span>
-   <span class="function">cubrid\_bind</span>
-   <span class="function">cubrid\_next\_result</span>
-   <span class="function">cubrid\_close\_request</span>
-   <span class="function">cubrid\_commit</span>
-   <span class="function">cubrid\_rollback</span>

cubrid\_fetch
=============

Fetch the next row from a result set

### 说明

<span class="type">mixed</span> <span
class="methodname">cubrid\_fetch</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = CUBRID\_BOTH</span></span> \] )

The <span class="function">cubrid\_fetch</span> function is used to get
a single row from the query result. The cursor automatically moves to
the next row after getting the result.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`type`  
Array type of the fetched result CUBRID\_NUM, CUBRID\_ASSOC,
CUBRID\_BOTH, CUBRID\_OBJECT. If you want to operate the lob object, you
can use CUBRID\_LOB.

### 返回值

Result array or object, when process is successful.

**`false`**, when there are no more rows; NULL, when process is
unsuccessful.

The result can be received either as an array or as an object, and you
can decide which data type to use by setting the `type` argument. The
`type` variable can be set to one of the following values:

-   CUBRID\_NUM : Numerical array (0-based)
-   CUBRID\_ASSOC : Associative array
-   CUBRID\_BOTH : Numerical & Associative array (default)
-   CUBRID\_OBJECT : object that has the attribute name as the column
    name of query result

When `type` argument is omitted, the result will be received using
CUBRID\_BOTH option as default. When you want to receive query result in
object data type, the column name of the result must obey the naming
rules for identifiers in PHP. For example, column name such as
"count(\*)" cannot be received in object type.

### 范例

**示例 \#1 <span class="function">cubrid\_fetch</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT * FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch($req)) {
    printf("%-40s %-10s %-6s %-20s\n", 
        $row["name"], $row["area"], $row["seats"], $row["address"]);
}

// if you want to operate lob object, you can use cubrid_fetch($req, CUBRID_LOB)

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    name                                     area       seats  address             
    Panathinaiko Stadium                     86300.00   50000  Athens, Greece      
    Olympic Stadium                          54700.00   13000  Athens, Greece      
    Olympic Indoor Hall                      34100.00   18800  Athens, Greece      
    Olympic Hall                             52400.00   21000  Athens, Greece      
    Olympic Aquatic Centre                   42500.00   11500  Athens, Greece      
    Markopoulo Olympic Equestrian Centre     64000.00   15000  Markopoulo, Athens, Greece
    Faliro Coastal Zone Olympic Complex      34650.00   12171  Faliro, Athens, Greece
    Athens Olympic Stadium                   120400.00  71030  Maroussi, Athens, Greece 
    Ano Liossia                              34000.00   12000  Ano Liosia, Athens, Greece

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_fetch\_array</span>
-   <span class="function">cubrid\_fetch\_row</span>
-   <span class="function">cubrid\_fetch\_assoc</span>
-   <span class="function">cubrid\_fetch\_object</span>

cubrid\_free\_result
====================

Free the memory occupied by the result data

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

This function frees the memory occupied by the result data. It returns
TRUE on success or FALSE on failure. Note that it can only frees the
client fetch buffer now, and if you want free all memory, use function
<span class="function">cubrid\_close\_request</span>.

### 参数

`req_identifier`  
This is the request identifier.

### 返回值

**`true`** on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_free\_result</span> example**

``` php
<?php 
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM history WHERE host_year=2004 ORDER BY event_code");
$row = cubrid_fetch_assoc($req);
var_dump($row);

cubrid_free_result($req);
cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(5) {
      ["event_code"]=>
      string(5) "20005"
      ["athlete"]=>
      string(12) "Hayes Joanna"
      ["host_year"]=>
      string(4) "2004"
      ["score"]=>
      string(5) "12.37"
      ["unit"]=>
      string(4) "time"
    }

cubrid\_get\_autocommit
=======================

Get auto-commit mode of the connection

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_get\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> )

The <span class="function">cubrid\_get\_autocommit</span> function is
used to get the status of CUBRID database connection auto-commit mode.

For CUBRID 8.4.0, auto-commit mode is disabled by default for
transaction management.

For CUBRID 8.4.1, auto-commit mode is enabled by default for transaction
management.

### 参数

`conn_identifier`  
Connection identifier.

### 返回值

**`true`**, when auto-commit is on.

**`false`**, when auto-commit is off.

**`null`** on error.

### 参见

-   <span class="function">cubrid\_set\_autocommit</span>
-   <span class="function">cubrid\_commit</span>

cubrid\_get\_charset
====================

Return the current CUBRID connection charset

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_get\_charset</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> )

This function returns the current CUBRID connection charset and is
similar to the CUBRID MySQL compatible function <span
class="function">cubrid\_client\_encoding</span>.

### 参数

`conn_identifier`  
The CUBRID connection.

### 返回值

A string that represents the CUBRID connection charset; on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_get\_charset</span> example**

``` php
<?php

$con = cubrid_connect("localhost", 33000, "demodb");
if (!$con)
{
    die('Could not connect.');
}

printf("CUBRID current charset: %s\n", cubrid_get_charset($con));

?>
```

以上例程会输出：

    CUBRID current charset: iso8859-1

### 参见

-   <span class="function">cubrid\_client\_encoding</span>

cubrid\_get\_class\_name
========================

Get the class name using OID

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_get\_class\_name</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> )

The <span class="function">cubrid\_get\_class\_name</span> function is
used to get the class name from `oid`. It doesn't work when selecting
data from the system tables, for example db\_class.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to check the existence.

### 返回值

Class name when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_get\_class\_name</span>
example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code", CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);
$class_name = cubrid_get_class_name($conn, $oid);

print_r($class_name);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    code

### 参见

-   <span class="function">cubrid\_is\_instance</span>
-   <span class="function">cubrid\_drop</span>

cubrid\_get\_client\_info
=========================

Return the client library version

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_get\_client\_info</span> ( <span
class="methodparam">void</span> )

This function returns a string that represents the client library
version.

### 参数

### 返回值

A string that represents the client library version; on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_get\_client\_info</span>
example**

``` php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);

?>
```

以上例程会输出：

    CUBRID PHP Version:            9.1.0.0001

    PARAM_ISOLATION_LEVEL          3
    LOCK_TIMEOUT                   -1
    MAX_STRING_LENGTH              1073741823
    PARAM_AUTO_COMMIT              1

    Server Info:                   9.1.0.0212
    Client Info:                   9.1.0

    CUBRID Charset:                iso8859-1

cubrid\_get\_db\_parameter
==========================

Returns the CUBRID database parameters

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_get\_db\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> )

This function returns the CUBRID database parameters or it returns FALSE
on failure. It returns an associative array with the values for the
following parameters:

-   **`PARAM_ISOLATION_LEVEL`**
-   **`PARAM_LOCK_TIMEOUT`**
-   **`PARAM_MAX_STRING_LENGTH`**
-   **`PARAM_AUTO_COMMIT`**

| Parameter               | Description                                                                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PARAM\_ISOLATION\_LEVEL | The transaction isolation level.                                                                                                                                                                                                                                                                                  |
| LOCK\_TIMEOUT           | CUBRID provides the lock timeout feature, which sets the waiting time (in seconds) for the lock until the transaction lock setting is allowed. The default value of the lock\_timeout\_in\_secs parameter is -1, which means the application client will wait indefinitely until the transaction lock is allowed. |
| PARAM\_AUTO\_COMMIT     | In CUBRID PHP, auto-commit mode is disabled by default for transaction management. It can be set by using <span class="function">cubrid\_set\_autocommit</span>.                                                                                                                                                  |

The following table shows the isolation levels from 1 to 6. It consists
of table schema (row) and isolation level:

| Name                                                                          | Description                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SERIALIZABLE (6)                                                              | In this isolation level, problems concerning concurrency (e.g. dirty read, non-repeatable read, phantom read, etc.) do not occur.                                                                                                                                                                                                                              |
| REPEATABLE READ CLASS with REPEATABLE READ INSTANCES (5)                      | Another transaction T2 cannot update the schema of table A while transaction T1 is viewing table A. Transaction T1 may experience phantom read for the record R that was inserted by another transaction T2 when it is repeatedly retrieving a specific record.                                                                                                |
| REPEATABLE READ CLASS with READ COMMITTED INSTANCES (or CURSOR STABILITY) (4) | Another transaction T2 cannot update the schema of table A while transaction T1 is viewing table A. Transaction T1 may experience R read (non-repeatable read) that was updated and committed by another transaction T2 when it is repeatedly retrieving the record R.                                                                                         |
| REPEATABLE READ CLASS with READ UNCOMMITTED INSTANCES (3)                     | Default isolation level. Another transaction T2 cannot update the schema of table A while transaction T1 is viewing table A. Transaction T1 may experience R' read (dirty read) for the record that was updated but not committed by another transaction T2.                                                                                                   |
| READ COMMITTED CLASS with READ COMMITTED INSTANCES (2)                        | Transaction T1 may experience A' read (non-repeatable read) for the table that was updated and committed by another transaction T2 while it is viewing table A repeatedly. Transaction T1 may experience R' read (non-repeatable read) for the record that was updated and committed by another transaction T2 while it is retrieving the record R repeatedly. |
| READ COMMITTED CLASS with READ UNCOMMITTED INSTANCES (1)                      | Transaction T1 may experience A' read (non-repeatable read) for the table that was updated and committed by another transaction T2 while it is repeatedly viewing table A. Transaction T1 may experience R' read (dirty read) for the record that was updated but not committed by another transaction T2.                                                     |

### 参数

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last link opened by <span class="function">cubrid\_connect</span> is
assumed.

### 返回值

An associative array with CUBRID database parameters; on success.

**`false`** on failure.

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 8.4.0 | Change LOCK\_TIMEOUT to PARAM\_LOCK\_TIMEOUT, and MAX\_STRING\_LENGTH to PARAM\_MAX\_STRING\_LENGTH in result. |

### 范例

**示例 \#1 <span class="function">cubrid\_get\_db\_parameter</span>
example**

``` php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);

?>
```

以上例程会输出：

    CUBRID PHP Version:            9.1.0.0001

    PARAM_ISOLATION_LEVEL          3
    LOCK_TIMEOUT                   -1
    MAX_STRING_LENGTH              1073741823
    PARAM_AUTO_COMMIT              1

    Server Info:                   9.1.0.0212
    Client Info:                   9.1.0

    CUBRID Charset:                iso8859-1

### 参见

-   <span class="function">cubrid\_set\_db\_parameter</span>
-   <span class="function">cubrid\_get\_autocommit</span>

cubrid\_get\_query\_timeout
===========================

Get the query timeout value of the request

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_get\_query\_timeout</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> )

The <span class="function">cubrid\_get\_query\_timeout</span> function
is used to get the query timeout of the request.

### 参数

`req_identifier`  
Request identifier.

### 返回值

Success: the query timeout value of the current request. Units of msec.

Failure: FALSE

### 范例

**示例 \#1 <span class="function">cubrid\_get\_query\_timeout</span>
example**

``` php
<?php

$host = "localhost";
$port = 33000;
$db = "demodb";

$conn =
cubrid_connect_with_url("CUBRID:$host:$port:$db:::?login_timeout=50000&query_timeout=5000&disconnect_on_query_timeout=yes");

$req = cubrid_prepare($conn, "SELECT * FROM code");

$timeout = cubrid_get_query_timeout($req);
var_dump($timeout);

cubrid_set_query_timeout($req, 1000);
$timeout = cubrid_get_query_timeout($req);
var_dump($timeout);

cubrid_close($conn);
?>
```

以上例程会输出：

    int(5000)
    int(1000)

### 参见

-   <span class="function">cubrid\_set\_query\_timeout</span>

cubrid\_get\_server\_info
=========================

Return the CUBRID server version

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_get\_server\_info</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> )

This function returns a string that represents the CUBRID server
version.

### 参数

`conn_identifier`  
The CUBRID connection.

### 返回值

A string that represents the CUBRID server version; on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_get\_server\_info</span>
example**

``` php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);

?>
```

以上例程会输出：

    CUBRID PHP Version:            9.1.0.0001

    PARAM_ISOLATION_LEVEL          3
    LOCK_TIMEOUT                   -1
    MAX_STRING_LENGTH              1073741823
    PARAM_AUTO_COMMIT              1

    Server Info:                   9.1.0.0212
    Client Info:                   9.1.0

    CUBRID Charset:                iso8859-1

cubrid\_get
===========

Get a column using OID

### 说明

<span class="type">mixed</span> <span
class="methodname">cubrid\_get</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$oid`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$attr`</span>
\] )

The <span class="function">cubrid\_get</span> function is used to get
the attribute of the instance of the given `oid`. You can get single
attribute by using string data type for the `attr` argument, or many
attributes by using array data type for the `attr` argument.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to read.

`attr`  
Name of the attribute that you want to read.

### 返回值

Content of the requested attribute, when process is successful; When
`attr` is set with string data type, the result is returned as a string;
when `attr` is set with array data type (0-based numerical array), then
the result is returned in associative array. When `attr` is omitted,
then all attributes are received in array form.

**`false`** when process is unsuccessful or result is NULL (If error
occurs to distinguish empty string from NULL, then it prints the warning
message. You can check the error by using <span
class="function">cubrid\_error\_code</span>)

### 范例

**示例 \#1 <span class="function">cubrid\_get</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_get($conn, $oid, "b");
var_dump($attr);

$attr = cubrid_get($conn, $oid);
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    string(9) "{1, 2, 3}"
    array(4) {
      ["a"]=>
      string(1) "1"
      ["b"]=>
      array(3) {
        [0]=>
        string(1) "1"
        [1]=>
        string(1) "2"
        [2]=>
        string(1) "3"
      }
      ["c"]=>
      array(4) {
        [0]=>
        string(2) "11"
        [1]=>
        string(2) "22"
        [2]=>
        string(2) "33"
        [3]=>
        string(3) "333"
      }
      ["d"]=>
      string(10) "a         "
    }

### 参见

-   <span class="function">cubrid\_put</span>

cubrid\_insert\_id
==================

Return the ID generated for the last updated **`AUTO_INCREMENT`** column

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_insert\_id</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

The <span class="function">cubrid\_insert\_id</span> function retrieves
the ID generated for the AUTO\_INCREMENT column which is updated by the
previous INSERT query. It returns 0 if the previous query does not
generate new rows, or FALSE on failure.

> **Note**:
>
> CUBRID supports AUTO\_INCREMENT for more than one columns in a table.
> In most cases, there will be a single AUTO\_INCREMENT column in a
> table. If there are multiple AUTO\_INCREMENT columns, this function
> should not be used even if it will return a value.

### 参数

`conn_identifier`  
The connection identifier previously obtained by a call to <span
class="function">cubrid\_connect</span>.

### 返回值

A string representing the ID generated for an AUTO\_INCREMENT column by
the previous query, on success.

0, if the previous query does not generate new rows.

**`false`** on failure.

### 更新日志

| 版本  | 说明                                                                                     |
|-------|------------------------------------------------------------------------------------------|
| 8.4.0 | Change the return value from an array to string; Remove the first parameter class\_name. |

### 范例

**示例 \#1 <span class="function">cubrid\_insert\_id</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

@cubrid_execute($conn, "DROP TABLE cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (d int AUTO_INCREMENT(1, 2), t varchar)");

for ($i = 0; $i < 10; $i++) {
    cubrid_execute($conn, "INSERT INTO cubrid_test(t) VALUES('cubrid_test')");
}

$id = cubrid_insert_id();
var_dump($id);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    string(2) "19"

cubrid\_is\_instance
====================

Check whether the instance pointed by OID exists

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_is\_instance</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> )

The <span class="function">cubrid\_is\_instance</span> function is used
to check whether the instance pointed by the given `oid` exists or not.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to check the existence.

### 返回值

1, if such instance exists;

0, if such instance does not exist;

-1, in case of error

### 范例

**示例 \#1 <span class="function">cubrid\_is\_instance</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$sql = <<<EOD
SELECT host_year, medal, game_date 
FROM game 
WHERE athlete_code IN 
    (SELECT code FROM athlete WHERE name='Thorpe Ian');
EOD;

$req = cubrid_execute($conn, $sql, CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);

$res = cubrid_is_instance ($conn, $oid);
if ($res == 1) {
    echo "Instance pointed by $oid exists.\n";
} else if ($res == 0){
    echo "Instance pointed by $oid doesn't exist.\n";
} else {
    echo "error\n";
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Instance pointed by @0|0|0 doesn't exist.

### 参见

-   <span class="function">cubrid\_drop</span>
-   <span class="function">cubrid\_get\_class\_name</span>

cubrid\_lob\_close
==================

Close BLOB/CLOB data

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob\_close</span> ( <span
class="methodparam"><span class="type">array</span>
`$lob_identifier_array`</span> )

<span class="function">cubrid\_lob\_close</span> is used to close all
BLOB/CLOB returned from <span class="function">cubrid\_lob\_get</span>.

### 参数

`lob_identifier_array`  
LOB identifier array return from cubrid\_lob\_get.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lob\_close</span> example**

``` php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");
echo "Doc size: ".cubrid_lob_size($lobs[0])." bytes";
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob\_get</span>
-   <span class="function">cubrid\_lob\_size</span>
-   <span class="function">cubrid\_lob\_export</span>
-   <span class="function">cubrid\_lob\_send</span>

cubrid\_lob\_export
===================

Export BLOB/CLOB data to file

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob\_export</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$lob_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$path_name`</span>
)

<span class="function">cubrid\_lob\_export</span> is used to get
BLOB/CLOB data from CUBRID database, and saves its contents to a file.
To use this function, you must use <span
class="function">cubrid\_lob\_get</span> first to get BLOB/CLOB info
from CUBRID.

### 参数

`conn_identifier`  
Connection identifier.

`lob_identifier`  
LOB identifier.

`path_name`  
Path name of the file.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lob\_export</span> example**

``` php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");
echo "Doc size: ".cubrid_lob_size($lobs[0])." bytes";
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob\_get</span>
-   <span class="function">cubrid\_lob\_close</span>
-   <span class="function">cubrid\_lob\_size</span>
-   <span class="function">cubrid\_lob\_send</span>

cubrid\_lob\_get
================

Get BLOB/CLOB data

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_lob\_get</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$sql`</span> )

<span class="function">cubrid\_lob\_get</span> is used to get BLOB/CLOB
meta info from CUBRID database, CUBRID gets BLOB/CLOB by executing the
SQL statement, and returns all LOBs as a resource array. Be sure that
the SQL retrieves only one column and its data type is BLOB or CLOB.

Remember to use <span class="function">cubrid\_lob\_close</span> to
release the LOBs if you don't need it any more.

### 参数

`conn_identifier`  
Connection identifier.

`sql`  
SQL statement to be executed.

### 返回值

Return an array of LOB resources, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lob\_get</span> example**

``` php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");
echo "Doc size: ".cubrid_lob_size($lobs[0])." bytes";
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob\_close</span>
-   <span class="function">cubrid\_lob\_size</span>
-   <span class="function">cubrid\_lob\_export</span>
-   <span class="function">cubrid\_lob\_send</span>

cubrid\_lob\_send
=================

Read BLOB/CLOB data and send straight to browser

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob\_send</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$lob_identifier`</span> )

<span class="function">cubrid\_lob\_send</span> reads BLOB/CLOB data and
passes it straight through to the browser. To use this function, you
must use <span class="function">cubrid\_lob\_get</span> first to get
BLOB/CLOB info from CUBRID.

### 参数

`conn_identifier`  
Connection identifier.

`lob_identifier`  
LOB identifier.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lob\_send</span> example**

``` php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");

cubrid_lob_send($conn, $lobs[0]);
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob\_get</span>
-   <span class="function">cubrid\_lob\_close</span>
-   <span class="function">cubrid\_lob\_size</span>
-   <span class="function">cubrid\_lob\_export</span>

cubrid\_lob\_size
=================

Get BLOB/CLOB data size

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_lob\_size</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> )

<span class="function">cubrid\_lob\_size</span> is used to get BLOB/CLOB
data size.

### 参数

`lob_identifier`  
LOB identifier.

### 返回值

A string representing LOB data size, when process is successful.

**`false`**, when process is unsuccessful.

### 更新日志

| 版本  | 说明                                         |
|-------|----------------------------------------------|
| 8.4.0 | Change return value type from int to string. |

### 范例

**示例 \#1 <span class="function">cubrid\_lob\_size</span> example**

``` php
<?php
$lobs = cubrid_lob_get($con, "SELECT doc_content FROM doc WHERE doc_id=5");
echo "Doc size:".cubrid_lob_size($lobs[0]);
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
?>
```

### 参见

-   <span class="function">cubrid\_lob\_get</span>
-   <span class="function">cubrid\_lob\_close</span>
-   <span class="function">cubrid\_lob\_export</span>
-   <span class="function">cubrid\_lob\_send</span>

cubrid\_lob2\_bind
==================

Bind a lob object or a string as a lob object to a prepared statement as
parameters

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_bind</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$bind_index`</span> , <span
class="methodparam"><span class="type">mixed</span> `$bind_value`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$bind_value_type`</span> \] )

The <span class="function">cubrid\_lob2\_bind</span> function is used to
bind BLOB/CLOB datas to a corresponding question mark placeholder in the
SQL statement that was passed to <span
class="function">cubrid\_prepare</span>. If `bind_value_type` is not
given, string will be "BLOB" as the default. But if you use <span
class="function">cubrid\_lob2\_new</span> before, `bind_value_type` will
be consistent with `type` in <span
class="function">cubrid\_lob2\_new</span> as the default.

### 参数

`req_identifier`  
Request identifier as a result of <span
class="function">cubrid\_prepare</span>.

`bind_index`  
Location of binding parameters. It starts with 1.

`bind_value`  
Actual value for binding.

`bind_value_type`  
It must be "BLOB" or "CLOB" and it won't be case-sensitive. If it not be
given, the default value is "BLOB".

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_bind</span> example**

``` php
<?php
// Table: test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES (?, ?)");

cubrid_bind($req,1, 3);

$lob = cubrid_lob2_new($conn, 'CLOB');
cubrid_lob2_bind($req, 2, $lob);

cubrid_execute($req);

cubrid_bind($req, 1, 4);

cubrid_lob2_bind($req, 2, 'CUBRID LOB2 TEST', 'CLOB');

cubrid_execute($req);

cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_new</span>
-   <span class="function">cubrid\_lob2\_close</span>

cubrid\_lob2\_close
===================

Close LOB object

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_close</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> )

The <span class="function">cubrid\_lob2\_close</span> function is used
to close LOB object returned from <span
class="function">cubrid\_lob2\_new</span> or got from the result set.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

### 返回值

**`true`**, on success.

**`false`**, on failure.

### 参见

-   <span class="function">cubrid\_lob2\_new</span>

cubrid\_lob2\_export
====================

Export the lob object to a file

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_export</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$file_name`</span> )

The <span class="function">cubrid\_lob2\_export</span> function is used
to save the contents of BLOB/CLOB data to a file. To use this function,
you must use <span class="function">cubrid\_lob2\_new</span> or fetch a
lob object from CUBRID database first. If the file already exists, the
operation will fail. This function will not influence the cursor
position of the lob object. It operates the entire lob object.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

`filename`  
File name you want to store BLOB/CLOB data. It also supports the path of
the file.

### 返回值

**`true`** if the process is successful and **`false`** for failure.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_export</span> example**

``` php
<?php
// Table: test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$req = cubrid_prepare($conn, "select * from doc");

cubrid_execute($req);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);

$row = cubrid_fetch($req, CUBRID_NUM | CUBRID_LOB);

cubrid_lob2_export($row[1], "doc_3.txt");

cubrid_lob2_close($row[1]);
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_new</span>
-   <span class="function">cubrid\_lob2\_close</span>
-   <span class="function">cubrid\_lob2\_import</span>
-   <span class="function">cubrid\_lob2\_bind</span>

cubrid\_lob2\_import
====================

Import BLOB/CLOB data from a file

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_import</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$file_name`</span> )

The <span class="function">cubrid\_lob2\_import</span> function is used
to save the contents of BLOB/CLOB data from a file. To use this
function, you must use <span class="function">cubrid\_lob2\_new</span>
or fetch a lob object from CUBRID database first. If the file already
exists, the operation will fail. This function will not influence the
cursor position of the lob object. It operates the entire lob object.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

`filename`  
File name you want to import BLOB/CLOB data. It also supports the path
of the file.

### 返回值

**`true`** if the process is successful and **`false`** for failure.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_export</span> example**

``` php
<?php

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");
 
$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES (?, ?)");
cubrid_bind($req, 1, 1);

$lob = cubrid_lob2_new($conn, "clob");
cubrid_lob2_import($lob, "doc_1.txt");
cubrid_lob2_bind($req, 2, $lob, 'CLOB'); // or cubrid_lob2_bind($req, 2, $lob);

cubrid_execute($req);

cubrid_lob2_close($lob);
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_new</span>
-   <span class="function">cubrid\_lob2\_close</span>
-   <span class="function">cubrid\_lob2\_export</span>
-   <span class="function">cubrid\_lob2\_bind</span>

cubrid\_lob2\_new
=================

Create a lob object

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_lob2\_new</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$type`<span class="initializer"> =
"BLOB"</span></span> \]\] )

The <span class="function">cubrid\_lob2\_new</span> function is used to
create a lob object (both BLOB and CLOB). This function should be used
before you bind a lob object.

### 参数

`conn_identifier`  
Connection identifier. If the connection identifier is not specified,
the last connection opened by <span
class="function">cubrid\_connect</span> or <span
class="function">cubrid\_connect\_with\_url</span> is assumed.

`type`  
It may be "BLOB" or "CLOB", it won't be case-sensitive. The default
value is "BLOB".

### 返回值

Lob identifier when it is successful.

**`false`** on failure.

### 参见

-   <span class="function">cubrid\_lob2\_close</span>

cubrid\_lob2\_read
==================

Read from BLOB/CLOB data

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_lob2\_read</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$len`</span> )

The <span class="function">cubrid\_lob2\_read</span> function reads
`len` bytes from the LOB data and returns the bytes read.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

`len`  
Length from buffer you want to read from the lob data.

### 返回值

Returns the contents as a string.

**`false`** when there is no more data.

NULL on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_read</span> example 1**

``` php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "public", "");

$req = cubrid_execute($conn, "select * from test_lob");

$row = cubrid_fetch_row($req, CUBRID_LOB);

print "position now is " . cubrid_lob2_tell($row[1]) . "\n";

cubrid_lob2_seek($row[1], 10, CUBRID_CURSOR_FIRST);

print "\nposition after moving farword is " . cubrid_lob2_tell($row[1]) . "\n";

$data = cubrid_lob2_read($row[1], 12);

print "\nposition after reading is " . cubrid_lob2_tell($row[1]) . "\n";

print $data . "\n";

cubrid_lob2_seek($row[1], 5, CUBRID_CURSOR_CURRENT);

print "\nposition after moving again is " . cubrid_lob2_tell($row[1]) . "\n";

$data = cubrid_lob2_read($row[1], 20);
print $data . "\n";

cubrid_disconnect($conn);
?>
```

**示例 \#2 <span class="function">cubrid\_lob2\_read</span> example 2**

``` php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

$req = cubrid_execute($conn, "select * from test_lob");

$row = cubrid_fetch_row($req, CUBRID_LOB);

while (true) {
    if ($data = cubrid_lob2_read($row[1], 1024)) {
        print $data . "\n";
    }
    elseif ($data === false) {
        print "There is no more data\n";
        break;
    }
    else {
        print "There must some errors\n";
        break;
    }
}

cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lob2\_seek64
====================

Move the cursor of a lob object

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_seek64</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$origin`<span
class="initializer"> = CUBRID\_CURSOR\_CURRENT</span></span> \] )

The <span class="function">cubrid\_lob2\_seek64</span> function is used
to move the cursor position of a lob object by the value set in the
`offset` argument, to the direction set in the `origin` argument. If the
`offset` you want to move is larger than an integer data can be stored,
you can use this function.

To set the `origin` argument, you can use CUBRID\_CURSOR\_FIRST to set
the cursor position moving forward `offset` units from the first
beginning. In this case, `offset` must be a positive value.

If you use CUBRID\_CURSOR\_CURRENT for `origin`, you can move forward or
backward. and `offset` can be positive or negative.

If you use CUBRID\_CURSOR\_LAST for `origin`, you can move backward
`offset` units from the end of LOB object and `offset` only can be
positive.

> **Note**:
>
> If you use this function to move the cursor position of the lob
> object, you should pass `offset` as a string.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

`offset`  
Number of units you want to move the cursor.

`origin`  
This parameter can be the following values:

CUBRID\_CURSOR\_FIRST: move forward from the first beginning.

CUBRID\_CURSOR\_CURRENT: move forward or backward from the current
position.

CUBRID\_CURSOR\_LAST: move backward at the end of LOB object.

### 返回值

**`true`** if the process is successful and **`false`** for failure.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_seek64</span> example**

``` php
<?php
// test_lob (id INT, contents CLOB)
// Data length of doc_1.txt should be greater than 20101029056306120215.

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");
 
$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES (?, ?)");
cubrid_bind($req, 1, 1);

$lob = cubrid_lob2_new($conn, "clob");
cubrid_lob2_import($lob, "doc_1.txt");
cubrid_lob2_bind($req, 2, $lob, 'CLOB'); // or cubrid_lob2_bind($req, 2, $lob);

cubrid_execute($req);

cubrid_lob2_close($lob);

$req = cubrid_execute($conn, "select * from test_lob");
$row = cubrid_fetch_row($req, CUBRID_LOB);
$lob = $row[1];

cubrid_lob2_seek64($lob, "20101029056306120215", CUBRID_CURSOR_FIRST);
$data = cubrid_lob2_read($lob, 20);
echo $data."\n";
cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lob2\_seek
==================

Move the cursor of a lob object

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_seek</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$origin`<span
class="initializer"> = CUBRID\_CURSOR\_CURRENT</span></span> \] )

The <span class="function">cubrid\_lob2\_seek</span> function is used to
move the cursor position of a lob object by the value set in the
`offset` argument, to the direction set in the `origin` argument.

To set the `origin` argument, you can use CUBRID\_CURSOR\_FIRST to set
the cursor position moving forward `offset` units from the first
beginning. In this case, `offset` must be a positive value.

If you use CUBRID\_CURSOR\_CURRENT for `origin`, you can move forward or
backward. and `offset` can be positive or negative.

If you use CUBRID\_CURSOR\_LAST for `origin`, you can move backward
`offset` units from the end of LOB object and `offset` only can be
positive.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

`offset`  
Number of units you want to move the cursor.

`origin`  
This parameter can be the following values:

CUBRID\_CURSOR\_FIRST: move forward from the first beginning.

CUBRID\_CURSOR\_CURRENT: move forward or backward from the current
position.

CUBRID\_CURSOR\_LAST: move backward at the end of LOB object.

### 返回值

**`true`** if the process is successful and **`false`** for failure.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_seek</span> example**

``` php
<?php
// test_lob (id INT, contents CLOB)
$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");
$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES(2, ?)");

$lob = cubrid_lob2_new($conn, 'CLOB');
$len = cubrid_lob2_write($lob, "Hello world");

cubrid_lob2_seek($lob, 0, CUBRID_CURSOR_LAST);
cubrid_lob2_write($lob, "beautiful");

cubrid_lob2_seek($lob, 15, CUBRID_CURSOR_FIRST);
$data = cubrid_lob2_read($lob, 5);

echo $data."\n";

cubrid_lob2_bind($req, 1, $lob);
cubrid_execute($req);

cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lob2\_size64
====================

Get a lob object's size

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_lob2\_size64</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> )

The <span class="function">cubrid\_lob2\_size64</span> function is used
to get the size of a lob object. If the size of a lob object is larger
than an integer data can be stored, you can use this function and it
will return the size as a string.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

### 返回值

It will return the size of the LOB object as a string when it processes
successfully.

**`false`** on failure.

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size</span>

cubrid\_lob2\_size
==================

Get a lob object's size

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_lob2\_size</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> )

The <span class="function">cubrid\_lob2\_size</span> function is used to
get the size of a lob object.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

### 返回值

It will return the size of the LOB object when it processes
successfully.

**`false`** on failure.

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lob2\_tell64
====================

Tell the cursor position of the LOB object

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_lob2\_tell64</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> )

The <span class="function">cubrid\_lob2\_tell64</span> function is used
to tell the cursor position of the LOB object. If the size of a lob
object is larger than an integer data can be stored, you can use this
function and it will return the position information as a string.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

### 返回值

It will return the cursor position on the LOB object as a string when it
processes successfully.

**`false`** on failure.

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_size</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lob2\_tell
==================

Tell the cursor position of the LOB object

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_lob2\_tell</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> )

The <span class="function">cubrid\_lob2\_tell</span> function is used to
tell the cursor position of the LOB object.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

### 返回值

It will return the cursor position on the LOB object when it processes
successfully.

**`false`** on failure.

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_write</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lob2\_write
===================

Write to a lob object

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lob2\_write</span> ( <span
class="methodparam"><span class="type">resource</span>
`$lob_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$buf`</span> )

The <span class="function">cubrid\_lob2\_write</span> function reads as
much as data from `buf` and stores it to the LOB object. Note that this
function can only append characters now.

### 参数

`lob_identifier`  
Lob identifier as a result of <span
class="function">cubrid\_lob2\_new</span> or get from the result set.

`buf`  
Data that need to be written to the lob object.

### 返回值

**`true`** if the process is successful and **`false`** for failure.

### 范例

**示例 \#1 <span class="function">cubrid\_lob2\_write</span> example 1**

``` php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES(2, ?)");

$lob = cubrid_lob2_new($conn, 'CLOB');
$len = cubrid_lob2_write($lob, "Hello world");

cubrid_lob2_bind($req, 1, $lob);
cubrid_execute($req);

cubrid_disconnect($conn);
?>
```

**示例 \#2 <span class="function">cubrid\_lob2\_write</span> example 2**

``` php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES(1, ?)");
$lob1 = cubrid_lob2_new($conn, 'CLOB');
$len = cubrid_lob2_write($lob1, "cubrid php driver");
cubrid_lob2_bind($req, 1, $lob1);
cubrid_execute($req);

$req = cubrid_execute($conn, "select * from test_lob");

$row = cubrid_fetch_row($req, CUBRID_LOB);
$lob2 = $row[1];
cubrid_lob2_seek($lob2, 0, CUBRID_CURSOR_LAST);

$pos = cubrid_lob2_tell($lob2);
print "pos before write: $pos\n";

cubrid_lob2_write($lob2, "Hello world");

$pos = cubrid_lob2_tell($lob2);
print "pos after write: $pos\n";

cubrid_disconnect($conn);
?>
```

### 参见

-   <span class="function">cubrid\_lob2\_read</span>
-   <span class="function">cubrid\_lob2\_seek</span>
-   <span class="function">cubrid\_lob2\_seek64</span>
-   <span class="function">cubrid\_lob2\_tell</span>
-   <span class="function">cubrid\_lob2\_tell64</span>
-   <span class="function">cubrid\_lob2\_size</span>
-   <span class="function">cubrid\_lob2\_size64</span>

cubrid\_lock\_read
==================

Set a read lock on the given OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lock\_read</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> )

The <span class="function">cubrid\_lock\_read</span> function is used to
put read lock on the instance pointed by given `oid`.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to put read lock on.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lock\_read</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

cubrid_lock_read($conn, $oid);

$attr = cubrid_get($conn, $oid, "b");
var_dump($attr);

$attr = cubrid_get($conn, $oid);
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    string(9) "{1, 2, 3}"
    array(4) {
      ["a"]=>
      string(1) "1"
      ["b"]=>
      array(3) {
        [0]=>
        string(1) "1"
        [1]=>
        string(1) "2"
        [2]=>
        string(1) "3"
      }
      ["c"]=>
      array(4) {
        [0]=>
        string(2) "11"
        [1]=>
        string(2) "22"
        [2]=>
        string(2) "33"
        [3]=>
        string(3) "333"
      }
      ["d"]=>
      string(10) "a         "
    }

### 参见

-   <span class="function">cubrid\_lock\_write</span>

cubrid\_lock\_write
===================

Set a write lock on the given OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_lock\_write</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> )

The <span class="function">cubrid\_lock\_write</span> function is used
to put write lock on the instance pointed by the given `oid`.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to put write lock on.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_lock\_write</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

cubrid_lock_write($conn, $oid);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_put($conn, $oid, "b", array(2, 4, 8));

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
    }
    array(3) {
      [0]=>
      string(1) "2"
      [1]=>
      string(1) "4"
      [2]=>
      string(1) "8"
    }

### 参见

-   <span class="function">cubrid\_lock\_read</span>

cubrid\_move\_cursor
====================

Move the cursor in the result

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_move\_cursor</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$origin`<span
class="initializer"> = CUBRID\_CURSOR\_CURRENT</span></span> \] )

The <span class="function">cubrid\_move\_cursor</span> function is used
to move the current cursor location of `req_identifier` by the value set
in the `offset` argument, to the direction set in the `origin` argument.
To set the `origin` argument, you can use CUBRID\_CURSOR\_FIRST for the
first part of the result, CUBRID\_CURSOR\_CURRENT for the current
location of the result, or CUBRID\_CURSOR\_LAST for the last part of the
result. If `origin` argument is not explicitly designated, then the
function uses CUBRID\_CURSOR\_CURRENT as its default value.

If the value of cursor movement range goes over the valid limit, then
the cursor moves to the next location after the valid range for the
cursor. For example, if you move 20 units in the result with the size of
10, then the cursor will move to 11th place and return
CUBRID\_NO\_MORE\_DATA.

### 参数

`req_identifier`  
Request identifier.

`offset`  
Number of units you want to move the cursor.

`origin`  
Location where you want to move the cursor from CUBRID\_CURSOR\_FIRST,
CUBRID\_CURSOR\_CURRENT, CUBRID\_CURSOR\_LAST.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsucceful.

### 范例

**示例 \#1 <span class="function">cubrid\_move\_cursor</span> example**

``` php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");
cubrid_move_cursor($req, 1, CUBRID_CURSOR_LAST);

$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_CURRENT);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      string(1) "G"
      [1]=>
      string(4) "Gold"
    }
    array(2) {
      [0]=>
      string(1) "X"
      [1]=>
      string(5) "Mixed"
    }
    array(2) {
      [0]=>
      string(1) "M"
      [1]=>
      string(3) "Man"
    }

### 参见

-   <span class="function">cubrid\_execute</span>

cubrid\_next\_result
====================

Get result of next query when executing multiple SQL statements

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

The <span class="function">cubrid\_next\_result</span> function is used
to get results of next query if multiple SQL statements are executed and
CUBRID\_EXEC\_QUERY\_ALL flag is set upon <span
class="function">cubrid\_execute</span>.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_next\_result</span> example**

``` php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");

$sql_stmt = "SELECT * FROM code; SELECT * FROM history WHERE host_year=2004 AND event_code=20281";
$res = cubrid_execute($conn, $sql_stmt, CUBRID_EXEC_QUERY_ALL);

get_result_info($res);
cubrid_next_result($res);
get_result_info($res);

function get_result_info($req)
{
    printf("\n------------ get_result_info --------------------\n");

    $row_num = cubrid_num_rows($req);
    $col_num = cubrid_num_cols($req);

    $column_name_list = cubrid_column_names($req);
    $column_type_list = cubrid_column_types($req);

    $column_last_name = cubrid_field_name($req, $col_num - 1);
    $column_last_table = cubrid_field_table($req, $col_num - 1);

    $column_last_type = cubrid_field_type($req, $col_num - 1);
    $column_last_len = cubrid_field_len($req, $col_num - 1);

    $column_1_flags = cubrid_field_flags($req, 1);

    printf("%-30s %d\n", "Row count:", $row_num);
    printf("%-30s %d\n", "Column count:", $col_num);
    printf("\n");

    printf("%-30s %-30s %-15s\n", "Column Names", "Column Types", "Column Len");
    printf("------------------------------------------------------------------------------\n");

    $size = count($column_name_list);
    for($i = 0; $i < $size; $i++) {
        $column_len = cubrid_field_len($req, $i);
        printf("%-30s %-30s %-15s\n", $column_name_list[$i], $column_type_list[$i], $column_len); 
    }
    printf("\n\n");

    printf("%-30s %s\n", "Last Column Name:", $column_last_name);
    printf("%-30s %s\n", "Last Column Table:", $column_last_table);
    printf("%-30s %s\n", "Last Column Type:", $column_last_type);
    printf("%-30s %d\n", "Last Column Len:", $column_last_len);
    printf("%-30s %s\n", "Second Column Flags:", $column_1_flags);

    printf("\n\n");
}
?>
```

以上例程会输出：

    ------------ get_result_info --------------------
    Row count:                     6
    Column count:                  2

    Column Names                   Column Types                   Column Len     
    ------------------------------------------------------------------------------
    s_name                         char                           1              
    f_name                         varchar                        6              


    Last Column Name:              f_name
    Last Column Table:             code
    Last Column Type:              varchar
    Last Column Len:               6
    Second Column Flags:           



    ------------ get_result_info --------------------
    Row count:                     4
    Column count:                  5

    Column Names                   Column Types                   Column Len     
    ------------------------------------------------------------------------------
    event_code                     integer                        11             
    athlete                        varchar                        40             
    host_year                      integer                        11             
    score                          varchar                        10             
    unit                           varchar                        5              


    Last Column Name:              unit
    Last Column Table:             history
    Last Column Type:              varchar
    Last Column Len:               5
    Second Column Flags:           not_null primary_key unique_key

### 参见

-   <span class="function">cubrid\_execute</span>

cubrid\_num\_cols
=================

Return the number of columns in the result set

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_num\_cols</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

The <span class="function">cubrid\_num\_cols</span> function is used to
get the number of columns from the query result. It can only be used
when the query executed is a select statement.

### 参数

`result`  
Result.

### 返回值

Number of columns, when process is successful.

**`false`**, if SQL statement is not SELECT.

### 范例

**示例 \#1 <span class="function">cubrid\_num\_cols</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_cols($req);

printf("Row Num: %d\nColumn Num: %d\n", $row_num, $col_num);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Row Num: 6
    Column Num: 2

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_num\_rows</span>

cubrid\_num\_rows
=================

Get the number of rows in the result set

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

The <span class="function">cubrid\_num\_rows</span> function is used to
get the number of rows from the query result. You can use it only when
the query executed is a select statement. When you want to know such
value for INSERT, UPDATE, or DELETE query, you have to use the <span
class="function">cubrid\_affected\_rows</span> function.

Note: The <span class="function">cubrid\_num\_rows</span> function can
only be used for synchronous query; it returns 0 when it is used for
asynchronous query.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>, <span
class="function">cubrid\_query</span> and <span
class="function">cubrid\_prepare</span>

### 返回值

Number of rows, when process is successful.

0 when the query was done in async mode.

-1, if SQL statement is not SELECT.

**`false`** when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_num\_rows</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_cols($req);

printf("Row Num: %d\nColumn Num: %d\n", $row_num, $col_num);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Row Num: 6
    Column Num: 2

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_num\_cols</span>
-   <span class="function">cubrid\_affected\_rows</span>

cubrid\_pconnect\_with\_url
===========================

Open a persistent connection to CUBRID server

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_pconnect\_with\_url</span> ( <span
class="methodparam"><span class="type">string</span> `$conn_url`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$userid`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passwd`</span> \]\] )

Establishes a persistent connection to a CUBRID server.

<span class="function">cubrid\_pconnect\_with\_url</span> acts very much
like <span class="function">cubrid\_connect\_with\_url</span> with two
major differences.

First, when connecting, the function would first try to find a
(persistent) link that's already open with the same host, port, dbname
and userid. If one is found, an identifier for it will be returned
instead of opening a new connection.

Second, the connection to the SQL server will not be closed when the
execution of the script ends. Instead, the link will remain open for
future use (<span class="function">cubrid\_close</span> or <span
class="function">cubrid\_disconnect</span> will not close links
established by <span
class="function">cubrid\_pconnect\_with\_url</span>).

This type of link is therefore called 'persistent'.

\<url\> ::=
CUBRID:\<host\>:\<db\_name\>:\<db\_user\>:\<db\_password\>:\[?\<properties\>\]

\<properties\> ::= \<property\> \[&\<property\>\]

\<properties\> ::= alhosts=\<alternative\_hosts\>\[ &rctime=\<time\>\]

\<properties\> ::= login\_timeout=\<milli\_sec\>

\<properties\> ::= query\_timeout=\<milli\_sec\>

\<properties\> ::= disconnect\_on\_query\_timeout=true\|false

\<alternative\_hosts\> ::= \<standby\_broker1\_host\>:\<port\>
\[,\<standby\_broker2\_host\>:\<port\>\]

\<host\> := HOSTNAME \| IP\_ADDR

\<time\> := SECOND

\<milli\_sec\> := MILLI SECOND

-   host : A host name or IP address of the master database
-   db\_name : A name of the database
-   db\_user : A name of the database user
-   db\_password : A database user password
-   alhosts : Specifies the broker information of the standby server,
    which is used for failover when it is impossible to connect to the
    active server. You can specify multiple brokers for failover, and
    the connection to the brokers is attempted in the order listed in
    alhosts
-   rctime : An interval between the attempts to connect to the active
    broker in which failure occurred. After a failure occurs, the system
    connects to the broker specified by althosts (failover), terminates
    the transaction, and then attempts to connect to the active broker
    of the master database at every rctime. The default value is 600
    seconds.
-   login\_timeout : Timeout value (unit: msec.) for database login. The
    default value is 0, which means infinite postponement.
-   query\_timeout : Timeout value (unit: msec.) for query request. Upon
    timeout, a message to cancel requesting a query transferred to
    server is sent. The return value can depend on the
    disconnect\_on\_query\_timeout configuration; even though the
    message to cancel a request is sent to server, that request may
    succeed.
-   disconnect\_on\_query\_timeout : Configures a value whether to
    immediately return an error of function being executed upon timeout.
    The default value is false.

> **Note**:
>
> *?* and *:* that are used as identifiers in PHP connection URL can't
> be included in the password. The following is an example of a password
> that is invalid to use as connection URL because it contains "*?:*".
>
> $url = "CUBRID:localhost:33000:tdb:dba:12?:?login\_timeout=100";
>
> Passwords that contain *?* or *:* may be passed as a separate
> parameter.
>
> $url = "CUBRID:localhost:33000:tbd:::?login\_timeout=100";
>
> $conn = cubrid\_pconnect\_with\_url ($url, "dba", "12?");
>
> If user or password is empty,you can't delete "*:*",the following is
> an example.
>
> $url = "CUBRID:localhost:33000:demodb:::";

### 参数

`conn_url`  
A character string that contains server connection information.

`userid`  
User name for the database.

`passwd`  
User password.

### 返回值

Connection identifier, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_pconnect\_with\_url</span> url
without properties example**

``` php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::"
$con = cubrid_pconnect_with_url ($conn_url);

if ($con) {
   echo "connected successfully";
   cubrid_execute($con, "create table person(id int,name char(16))");
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_disconnect ($con);
}
?>
```

**示例 \#2 <span class="function">cubrid\_pconnect\_with\_url</span> url
with properties example**

``` php
<?php
$conn_url = "CUBRID:127.0.0.1:33000:demodb:dba::?althost=10.34.63.132:33088&rctime=100"
$con = cubrid_pconnect_with_url ($conn_url);

if ($con) {
   echo "connected successfully";
   $req =cubrid_execute($con, "insert into person values(1,'James')");

   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_disconnect ($con);
}
?>
```

### 参见

-   <span class="function">cubrid\_connect</span>
-   <span class="function">cubrid\_connect\_with\_url</span>
-   <span class="function">cubrid\_pconnect</span>
-   <span class="function">cubrid\_disconnect</span>
-   <span class="function">cubrid\_close</span>

cubrid\_pconnect
================

Open a persistent connection to a CUBRID server

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_pconnect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dbname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$userid`</span> \[, <span
class="methodparam"><span class="type">string</span> `$passwd`</span>
\]\] )

Establishes a persistent connection to a CUBRID server.

<span class="function">cubrid\_pconnect</span> acts very much like <span
class="function">cubrid\_connect</span> with two major differences.

First, when connecting, the function would first try to find a
(persistent) link that's already open with the same host, port, dbname
and userid. If one is found, an identifier for it will be returned
instead of opening a new connection.

Second, the connection to the SQL server will not be closed when the
execution of the script ends. Instead, the link will remain open for
future use (<span class="function">cubrid\_close</span> or <span
class="function">cubrid\_disconnect</span> will not close links
established by <span class="function">cubrid\_pconnect</span>).

This type of link is therefore called 'persistent'.

### 参数

`host`  
Host name or IP address of CUBRID CAS server.

`port`  
Port number of CUBRID CAS server (BROKER\_PORT configured in
$CUBRID/conf/cubrid\_broker.conf).

`dbname`  
Name of database.

`userid`  
User name for the database.

`passwd`  
User password.

### 返回值

Connection identifier, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_connect</span> example**

``` php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_pconnect("localhost", 33000, "demodb", "dba");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    CUBRID PHP Version:            9.1.0.0001

    PARAM_ISOLATION_LEVEL          3
    LOCK_TIMEOUT                   -1
    MAX_STRING_LENGTH              1073741823
    PARAM_AUTO_COMMIT              1

    Server Info:                   9.1.0.0212
    Client Info:                   9.1.0

    CUBRID Charset:                iso8859-1

### 参见

-   <span class="function">cubrid\_connect</span>
-   <span class="function">cubrid\_connect\_with\_url</span>
-   <span class="function">cubrid\_pconnect\_with\_url</span>
-   <span class="function">cubrid\_disconnect</span>
-   <span class="function">cubrid\_close</span>

cubrid\_prepare
===============

Prepare a SQL statement for execution

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$prepare_stmt`</span> \[, <span
class="methodparam"><span class="type">int</span> `$option`<span
class="initializer"> = 0</span></span> \] )

The <span class="function">cubrid\_prepare</span> function is a sort of
API which represents SQL statements compiled previously to a given
connection handle. This pre-compiled SQL statement will be included in
the <span class="function">cubrid\_prepare</span>.

Accordingly, you can use this statement effectively to execute several
times repeatedly or to process long data. Only a single statement can be
used and a parameter may put a question mark (?) to appropriate area in
the SQL statement. Add a parameter when you bind a value in the VALUES
clause of INSERT statement or in the WHERE clause. Note that it is
allowed to bind a value to a MARK(?) by using the <span
class="function">cubrid\_bind</span> function only.

### 参数

`conn_identifier`  
Connection identifier.

`prepare_stmt`  
Prepare query.

`option`  
OID return option CUBRID\_INCLUDE\_OID.

### 返回值

Request identifier, if process is successful;

**`false`**, if process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_prepare</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$sql = <<<EOD
SELECT g.event_code, e.name 
FROM game g 
JOIN event e ON g.event_code=e.code 
WHERE host_year = ? AND event_code NOT IN (SELECT event_code FROM game WHERE host_year=?) GROUP BY event_code;
EOD;

$req = cubrid_prepare($conn, $sql);

cubrid_bind($req, 1, 2004);
cubrid_bind($req, 2, 2000);
cubrid_execute($req);

$row_num = cubrid_num_rows($req);
printf("There are %d event that exits in 2004 olympic but not in 2000. For example:\n\n", $row_num);

printf("%-15s %s\n", "Event_code", "Event_name");
printf("----------------------------\n");

$row = cubrid_fetch_assoc($req);
printf("%-15d %s\n", $row["event_code"], $row["name"]);
$row = cubrid_fetch_assoc($req);
printf("%-15d %s\n", $row["event_code"], $row["name"]);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    There are 27 event that exits in 2004 olympic but not in 2000. For example:

    Event_code      Event_name
    ----------------------------
    20063           +91kg
    20070           64kg

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_bind</span>

cubrid\_put
===========

Update a column using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_put</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$oid`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$attr`</span> \], <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

The <span class="function">cubrid\_put</span> function is used to update
an attribute of the instance of the given `oid`.

You can update single attribute by using string data type to set `attr`.
In such case, you can use integer, floating point or string type data
for the `value` argument. To update multiple number of attributes, you
can disregard the `attr` argument, and set `value` argument with
associative array data type.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance that you want to update.

`attr`  
Name of the attribute that you want to update.

`value`  
New value that you want to assign to the attribute.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_put</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_put($conn, $oid, "b", array(2, 4, 8));

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
    }
    array(3) {
      [0]=>
      string(1) "2"
      [1]=>
      string(1) "4"
      [2]=>
      string(1) "8"
    }

### 参见

-   <span class="function">cubrid\_get</span>
-   <span class="function">cubrid\_set\_add</span>
-   <span class="function">cubrid\_set\_drop</span>
-   <span class="function">cubrid\_seq\_insert</span>
-   <span class="function">cubrid\_seq\_drop</span>
-   <span class="function">cubrid\_seq\_put</span>

cubrid\_rollback
================

Roll back a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_rollback</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> )

The <span class="function">cubrid\_rollback</span> function executes
rollback on the transaction pointed by `conn_identifier`, currently in
progress.

Connection to server is closed after calling <span
class="function">cubrid\_rollback</span>. Connection handle, however, is
still valid.

### 参数

`conn_identifier`  
Connection identifier.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_rollback</span> example**

``` php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb", "dba");
cubrid_set_autocommit($conn,false);

@cubrid_execute($conn, "DROP TABLE publishers");

$sql = <<<EOD
CREATE TABLE publishers(
pub_id CHAR(3), 
pub_name VARCHAR(20), 
city VARCHAR(15), 
state CHAR(2), 
country VARCHAR(15)
)
EOD;

if (!cubrid_execute($conn, $sql)) {
    printf("Error facility: %d\nError code: %d\nError msg: %s\n", cubrid_error_code_facility(), cubrid_error_code(), cubrid_error_msg());

    cubrid_disconnect($conn);
    exit;
}

$req = cubrid_prepare($conn, "INSERT INTO publishers VALUES(?, ?, ?, ?, ?)");

$id_list = array("P01", "P02", "P03", "P04");
$name_list = array("Abatis Publishers", "Core Dump Books", "Schadenfreude Press", "Tenterhooks Press");
$city_list = array("New York", "San Francisco", "Hamburg", "Berkeley");
$state_list = array("NY", "CA", NULL, "CA");
$country_list = array("USA", "USA", "Germany", "USA");

for ($i = 0, $size = count($id_list); $i < $size; $i++) {
    cubrid_bind($req, 1, $id_list[$i]);
    cubrid_bind($req, 2, $name_list[$i]);
    cubrid_bind($req, 3, $city_list[$i]);
    cubrid_bind($req, 4, $state_list[$i]);
    cubrid_bind($req, 5, $country_list[$i]);

    if (!($ret = cubrid_execute($req))) {
        break;
    }
}

if (!$ret) {
    cubrid_rollback($conn);
} else {
    cubrid_commit($conn);

    $req = cubrid_execute($conn, "SELECT * FROM publishers");
    while ($result = cubrid_fetch_assoc($req)) {
        printf("%-3s %-20s %-15s %-3s %-15s\n", 
            $result["pub_id"], $result["pub_name"], $result["city"], $result["state"], $result["country"]);
    }
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    P01 Abatis Publishers    New York        NY  USA            
    P02 Core Dump Books      San Francisco   CA  USA            
    P03 Schadenfreude Press  Hamburg             Germany        
    P04 Tenterhooks Press    Berkeley        CA  USA            

### 参见

-   <span class="function">cubrid\_commit</span>
-   <span class="function">cubrid\_disconnect</span>

cubrid\_schema
==============

Get the requested schema information

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_schema</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$schema_type`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$attr_name`</span> \]\] )

The <span class="function">cubrid\_schema</span> function is used to get
the requested schema information from database. You have to designate
`class_name`, if you want to get information on certain class,
`attr_name`, if you want to get information on certain attribute (can be
used only with CUBRID\_ SCH\_ATTR\_PRIVILEGE).

The result of the cubrid\_schema function is returned as a
two-dimensional array (column (associative array) \* row (numeric
array)). The following tables shows types of schema and the column
structure of the result array to be returned based on the schema type.

| Schema                                                                                    | Column Number | Column Name              | Value                                             |
|-------------------------------------------------------------------------------------------|---------------|--------------------------|---------------------------------------------------|
| CUBRID\_SCH\_CLASS                                                                        | 1             | NAME                     |                                                   |
|                                                                                           | 2             | TYPE                     | 0:system class 1:vclass 2:class                   |
| CUBRID\_SCH\_VCLASS                                                                       | 1             | NAME                     |                                                   |
|                                                                                           | 2             | TYPE                     | 1:vclass                                          |
| CUBRID\_SCH\_QUERY\_SPEC                                                                  | 1             | QUERY\_SPEC              |                                                   |
| CUBRID\_SCH\_ATTRIBUTE / CUBRID\_SCH\_CLASS\_ATTRIBUTE                                    | 1             | ATTR\_NAME               |                                                   |
|                                                                                           | 2             | DOMAIN                   |                                                   |
|                                                                                           | 3             | SCALE                    |                                                   |
|                                                                                           | 4             | PRECISION                |                                                   |
|                                                                                           | 5             | INDEXED                  | 1:indexed                                         |
|                                                                                           | 6             | NOT NULL                 | 1:not null                                        |
|                                                                                           | 7             | SHARED                   | 1:shared                                          |
|                                                                                           | 8             | UNIQUE                   | 1:unique                                          |
|                                                                                           | 9             | DEFAULT                  |                                                   |
|                                                                                           | 10            | ATTR\_ORDER              | base:1                                            |
|                                                                                           | 11            | CLASS\_NAME              |                                                   |
|                                                                                           | 12            | SOURCE\_CLASS            |                                                   |
|                                                                                           | 13            | IS\_KEY                  | 1:key                                             |
| CUBRID\_SCH\_METHOD / CUBRID\_SCH\_CLASS\_METHOD                                          | 1             | NAME                     |                                                   |
|                                                                                           | 2             | RET\_DOMAIN              |                                                   |
|                                                                                           | 3             | ARG\_DOMAIN              |                                                   |
| CUBRID\_SCH\_METHOD\_FILE                                                                 | 1             | METHOD\_FILE             |                                                   |
| CUBRID\_SCH\_SUPERCLASS / CUBRID\_SCH\_DIRECT\_SUPER\_CLASS / CUBRID\_SCH\_SUBCLASS       | 1             | CLASS\_NAME              |                                                   |
|                                                                                           | 2             | TYPE                     | 0:system class 1:vclass 2:class                   |
| CUBRID\_SCH\_CONSTRAINT                                                                   | 1             | TYPE                     | 0:unique 1:index 2:reverse unique 3:reverse index |
|                                                                                           | 2             | NAME                     |                                                   |
|                                                                                           | 3             | ATTR\_NAME               |                                                   |
|                                                                                           | 4             | NUM\_PAGES               |                                                   |
|                                                                                           | 5             | NUM\_KEYS                |                                                   |
|                                                                                           | 6             | PRIMARY\_KEY             | 1:primary key                                     |
|                                                                                           | 7             | KEY\_ORDER               | base:1                                            |
| CUBRID\_SCH\_TRIGGER                                                                      | 1             | NAME                     |                                                   |
|                                                                                           | 2             | STATUS                   |                                                   |
|                                                                                           | 3             | EVENT                    |                                                   |
|                                                                                           | 4             | TARGET\_CLASS            |                                                   |
|                                                                                           | 5             | TARGET\_ATTR             |                                                   |
|                                                                                           | 6             | ACTION\_TIME             |                                                   |
|                                                                                           | 7             | ACTION                   |                                                   |
|                                                                                           | 8             | PRIORITY                 |                                                   |
|                                                                                           | 9             | CONDITION\_TIME          |                                                   |
|                                                                                           | 10            | CONDITION                |                                                   |
| CUBRID\_SCH\_CLASS\_PRIVILEGE / CUBRID\_SCH\_ATTR\_PRIVILEGE                              | 1             | CLASS\_NAME / ATTR\_NAME |                                                   |
|                                                                                           | 2             | PRIVILEGE                |                                                   |
|                                                                                           | 3             | GRANTABLE                |                                                   |
| CUBRID\_SCH\_PRIMARY\_KEY                                                                 | 1             | CLASS\_NAME              |                                                   |
|                                                                                           | 2             | ATTR\_NAME               |                                                   |
|                                                                                           | 3             | KEY\_SEQ                 | base:1                                            |
|                                                                                           | 4             | KEY\_NAME                |                                                   |
| CUBRID\_SCH\_IMPORTED\_KEYS / CUBRID\_SCH\_EXPORTED\_KEYS / CUBRID\_SCH\_CROSS\_REFERENCE | 1             | PKTABLE\_NAME            |                                                   |
|                                                                                           | 2             | PKCOLUMN\_NAME           |                                                   |
|                                                                                           | 3             | FKTABLE\_NAME            | base:1                                            |
|                                                                                           | 4             | FKCOLUMN\_NAME           |                                                   |
|                                                                                           | 5             | KEY\_SEQ                 | base:1                                            |
|                                                                                           | 6             | UPDATE\_ACTION           | 0:cascade 1:restrict 2:no action 3:set null       |
|                                                                                           | 7             | DELETE\_ACTION           | 0:cascade 1:restrict 2:no action 3:set null       |
|                                                                                           | 8             | FK\_NAME                 |                                                   |
|                                                                                           | 9             | PK\_NAME                 |                                                   |

### 参数

`conn_identifier`  
Connection identifier.

`schema_type`  
Schema data that you want to know.

`class_name`  
Class you want to know the schema of.

`attr_name`  
Attribute you want to know the schema of.

### 返回值

Array containing the schema information, when process is successful;

**`false`**, when process is unsuccessful

### 更新日志

| 版本  | 说明                                                                     |
|-------|--------------------------------------------------------------------------|
| 8.3.1 | Change return value: when process is unsuccessful, return false, not -1. |

### 范例

**示例 \#1 <span class="function">cubrid\_schema</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

printf("\n--- Primary Key ---\n");
$pk = cubrid_schema($conn, CUBRID_SCH_PRIMARY_KEY, "game");
var_dump($pk);

printf("\n--- Foreign Keys ---\n");
$fk = cubrid_schema($conn, CUBRID_SCH_IMPORTED_KEYS, "game");
var_dump($fk);

printf("\n--- Column Attribute ---\n");
$attr = cubrid_schema($conn, CUBRID_SCH_ATTRIBUTE, "stadium", "area");
var_dump($attr);

cubrid_disconnect($conn);
?>
```

以上例程会输出：


    --- Primary Key ---
    array(3) {
      [0]=>
      array(4) {
        ["CLASS_NAME"]=>
        string(4) "game"
        ["ATTR_NAME"]=>
        string(12) "athlete_code"
        ["KEY_SEQ"]=>
        string(1) "3"
        ["KEY_NAME"]=>
        string(41) "pk_game_host_year_event_code_athlete_code"
      }
      [1]=>
      array(4) {
        ["CLASS_NAME"]=>
        string(4) "game"
        ["ATTR_NAME"]=>
        string(10) "event_code"
        ["KEY_SEQ"]=>
        string(1) "2"
        ["KEY_NAME"]=>
        string(41) "pk_game_host_year_event_code_athlete_code"
      }
      [2]=>
      array(4) {
        ["CLASS_NAME"]=>
        string(4) "game"
        ["ATTR_NAME"]=>
        string(9) "host_year"
        ["KEY_SEQ"]=>
        string(1) "1"
        ["KEY_NAME"]=>
        string(41) "pk_game_host_year_event_code_athlete_code"
      }
    }

    --- Foreign Keys ---
    array(2) {
      [0]=>
      array(9) {
        ["PKTABLE_NAME"]=>
        string(7) "athlete"
        ["PKCOLUMN_NAME"]=>
        string(4) "code"
        ["FKTABLE_NAME"]=>
        string(4) "game"
        ["FKCOLUMN_NAME"]=>
        string(12) "athlete_code"
        ["KEY_SEQ"]=>
        string(1) "1"
        ["UPDATE_RULE"]=>
        string(1) "1"
        ["DELETE_RULE"]=>
        string(1) "1"
        ["FK_NAME"]=>
        string(20) "fk_game_athlete_code"
        ["PK_NAME"]=>
        string(15) "pk_athlete_code"
      }
      [1]=>
      array(9) {
        ["PKTABLE_NAME"]=>
        string(5) "event"
        ["PKCOLUMN_NAME"]=>
        string(4) "code"
        ["FKTABLE_NAME"]=>
        string(4) "game"
        ["FKCOLUMN_NAME"]=>
        string(10) "event_code"
        ["KEY_SEQ"]=>
        string(1) "1"
        ["UPDATE_RULE"]=>
        string(1) "1"
        ["DELETE_RULE"]=>
        string(1) "1"
        ["FK_NAME"]=>
        string(18) "fk_game_event_code"
        ["PK_NAME"]=>
        string(13) "pk_event_code"
      }
    }

    --- Column Attribute ---
    array(1) {
      [0]=>
      array(13) {
        ["ATTR_NAME"]=>
        string(4) "area"
        ["DOMAIN"]=>
        string(1) "7"
        ["SCALE"]=>
        string(1) "2"
        ["PRECISION"]=>
        string(2) "10"
        ["INDEXED"]=>
        string(1) "0"
        ["NON_NULL"]=>
        string(1) "0"
        ["SHARED"]=>
        string(1) "0"
        ["UNIQUE"]=>
        string(1) "0"
        ["DEFAULT"]=>
        NULL
        ["ATTR_ORDER"]=>
        string(1) "4"
        ["CLASS_NAME"]=>
        string(7) "stadium"
        ["SOURCE_CLASS"]=>
        string(7) "stadium"
        ["IS_KEY"]=>
        string(1) "0"
      }
    }

cubrid\_seq\_drop
=================

Delete an element from sequence type column using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_seq\_drop</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

The <span class="function">cubrid\_seq\_drop</span> function is used to
delete an element you request from the given sequence type attribute in
the database.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance you want to work with.

`attr_name`  
Name of the attribute that you want to delete an element from.

`index`  
Index of the element that you want to delete (1-based).

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_seq\_drop</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c sequence(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_seq_drop($conn, $oid, "c", 4);

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      string(2) "11"
      [1]=>
      string(2) "22"
      [2]=>
      string(2) "33"
      [3]=>
      string(3) "333"
    }
    array(3) {
      [0]=>
      string(2) "11"
      [1]=>
      string(2) "22"
      [2]=>
      string(2) "33"
    }

### 参见

-   <span class="function">cubrid\_seq\_insert</span>
-   <span class="function">cubrid\_seq\_put</span>

cubrid\_seq\_insert
===================

Insert an element to a sequence type column using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_seq\_insert</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> , <span class="methodparam"><span
class="type">string</span> `$seq_element`</span> )

The <span class="function">cubrid\_col\_insert</span> function is used
to insert an element to a sequence type attribute in a requested
location.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance you want to work with.

`attr_name`  
Name of the attribute you want to insert an instance to.

`index`  
Location of the element, you want to insert the element to (1-based).

`seq_element`  
Content of the element that you want to insert.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_seq\_insert</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c sequence(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_seq_insert($conn, $oid, "c", 5, "44");

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      string(2) "11"
      [1]=>
      string(2) "22"
      [2]=>
      string(2) "33"
      [3]=>
      string(3) "333"
    }
    array(5) {
      [0]=>
      string(2) "11"
      [1]=>
      string(2) "22"
      [2]=>
      string(2) "33"
      [3]=>
      string(3) "333"
      [4]=>
      string(2) "44"
    }

### 参见

-   <span class="function">cubrid\_seq\_drop</span>
-   <span class="function">cubrid\_seq\_put</span>

cubrid\_seq\_put
================

Update the element value of sequence type column using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_seq\_put</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> , <span class="methodparam"><span
class="type">string</span> `$seq_element`</span> )

The <span class="function">cubrid\_seq\_put</span> function is used to
update the content of the requested element in a sequent type attribute
using OID.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance you want to work with.

`attr_name`  
Name of the attribute that you want to update an element.

`index`  
Index (1-based) of the element that you want to update.

`seq_element`  
New content that you want to use for the update.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_seq\_put</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c sequence(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_seq_put($conn, $oid, "c", 1, "111");

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      string(2) "11"
      [1]=>
      string(2) "22"
      [2]=>
      string(2) "33"
      [3]=>
      string(3) "333"
    }
    array(4) {
      [0]=>
      string(3) "111"
      [1]=>
      string(2) "22"
      [2]=>
      string(2) "33"
      [3]=>
      string(3) "333"
    }

### 参见

-   <span class="function">cubrid\_seq\_drop</span>
-   <span class="function">cubrid\_seq\_insert</span>

cubrid\_set\_add
================

Insert a single element to set type column using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_set\_add</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
, <span class="methodparam"><span class="type">string</span>
`$set_element`</span> )

The <span class="function">cubrid\_set\_add</span> function is used to
insert a single element to a set type attribute (set, multiset,
sequence) you requested.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance you want to work with.

`attr_name`  
Name of the attribute you want to insert an element.

`set_element`  
Content of the element you want to insert.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_set\_add</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_set_add($conn, $oid, "b", "4");

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
    }
    array(4) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
      [3]=>
      string(1) "4"
    }

### 参见

-   <span class="function">cubrid\_seq\_drop</span>

cubrid\_set\_autocommit
=======================

Set autocommit mode of the connection

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_set\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">bool</span> `$mode`</span> )

The <span class="function">cubrid\_set\_autocommit</span> function is
used to set the CUBRID database auto-commit mode of the current database
connection.

In CUBRID PHP, auto-commit mode is disabled by default for transaction
management. When auto-commit mode is truned from off to on, any pending
work is automatically committed.

### 参数

`conn_identifier`  
Connection identifier.

`mode`  
Auto-commit mode. The following constants can be used:

-   **`CUBRID_AUTOCOMMIT_FALSE`**
-   **`CUBRID_AUTOCOMMIT_TRUE`**

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 参见

-   <span class="function">cubrid\_get\_autocommit</span>
-   <span class="function">cubrid\_commit</span>

cubrid\_set\_db\_parameter
==========================

Sets the CUBRID database parameters

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_set\_db\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$param_type`</span> , <span
class="methodparam"><span class="type">int</span> `$param_value`</span>
)

The <span class="function">cubrid\_set\_db\_parameter</span> function is
used to set the CUBRID database parameters. It can set the following
CUBRID database parameters:

-   **`PARAM_ISOLATION_LEVEL`**
-   **`PARAM_LOCK_TIMEOUT`**

> **Note**:
>
> The auto-commit mode can be set by using <span
> class="function">cubrid\_set\_autocommit</span>.

### 参数

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last link opened by <span class="function">cubrid\_connect</span> is
assumed.

`param_type`  
Database parameter type.

`param_value`  
Isolation level value (1-6) or lock timeout (in seconds) value.

### 返回值

**`true`** on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_get\_db\_parameter</span>
example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$params = cubrid_get_db_parameter($conn);
var_dump($params);

cubrid_set_autocommit($conn, CUBRID_AUTOCOMMIT_TRUE);
cubrid_set_db_parameter($conn, CUBRID_PARAM_ISOLATION_LEVEL, 2);

$params_new = cubrid_get_db_parameter($conn);
var_dump($params_new);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(4) {
      ["PARAM_ISOLATION_LEVEL"]=>
      int(3)
      ["PARAM_LOCK_TIMEOUT"]=>
      int(-1)
      ["PARAM_MAX_STRING_LENGTH"]=>
      int(1073741823)
      ["PARAM_AUTO_COMMIT"]=>
      int(0)
    }
    array(4) {
      ["PARAM_ISOLATION_LEVEL"]=>
      int(2)
      ["PARAM_LOCK_TIMEOUT"]=>
      int(-1)
      ["PARAM_MAX_STRING_LENGTH"]=>
      int(1073741823)
      ["PARAM_AUTO_COMMIT"]=>
      int(1)
    }

### 参见

-   <span class="function">cubrid\_get\_db\_parameter</span>
-   <span class="function">cubrid\_set\_autocommit</span>

cubrid\_set\_drop
=================

Delete an element from set type column using OID

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_set\_drop</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$attr_name`</span>
, <span class="methodparam"><span class="type">string</span>
`$set_element`</span> )

The <span class="function">cubrid\_set\_drop</span> function is used to
delete an element that you request from the given set type (set,
multiset) attribute of the database.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
OID of the instance you want to work with.

`attr_name`  
Name of the attribute you want to delete an element from.

`set_element`  
Content of the element you want to delete.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_set\_drop</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_set_drop($conn, $oid, "b", "1");

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(1) "1"
      [1]=>
      string(1) "2"
      [2]=>
      string(1) "3"
    }
    array(2) {
      [0]=>
      string(1) "2"
      [1]=>
      string(1) "3"
    }

### 参见

-   <span class="function">cubrid\_set\_add</span>

cubrid\_set\_query\_timeout
===========================

Set the timeout time of query execution

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_set\_query\_timeout</span> ( <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$timeout`</span> )

The <span class="function">cubrid\_set\_query\_timeout</span> function
is used to set the timeout time of query execution.

### 参数

`req_identifier`  
Request identifier.

`timeout`  
Timeout time, unit of msec.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 参见

-   <span class="function">cubrid\_get\_query\_timeout</span>

cubrid\_version
===============

Get the CUBRID PHP module's version

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_version</span> ( <span
class="methodparam">void</span> )

The <span class="function">cubrid\_version</span> function is used to
get the CUBRID PHP module's version.

### 参数

此函数没有参数。

### 返回值

Version information (eg. "8.3.1.0001").

### 范例

**示例 \#1 <span class="function">cubrid\_version</span> example**

``` php
<?php
printf("%-30s %s\n", "CUBRID PHP Version:", cubrid_version());

printf("\n");

$conn = cubrid_connect("localhost", 33088, "demodb", "dba");

if (!$conn) {
    die('Connect Error ('. cubrid_error_code() .')' . cubrid_error_msg());
}

$db_params = cubrid_get_db_parameter($conn);

while (list($param_name, $param_value) = each($db_params)) {
    printf("%-30s %s\n", $param_name, $param_value);
}

printf("\n");

$server_info = cubrid_get_server_info($conn);
$client_info = cubrid_get_client_info();

printf("%-30s %s\n", "Server Info:", $server_info);
printf("%-30s %s\n", "Client Info:", $client_info);

printf("\n");

$charset = cubrid_get_charset($conn);

printf("%-30s %s\n", "CUBRID Charset:", $charset);

cubrid_disconnect($conn);

?>
```

以上例程会输出：

    CUBRID PHP Version:            9.1.0.0001

    PARAM_ISOLATION_LEVEL          3
    LOCK_TIMEOUT                   -1
    MAX_STRING_LENGTH              1073741823
    PARAM_AUTO_COMMIT              1

    Server Info:                   9.1.0.0212
    Client Info:                   9.1.0

    CUBRID Charset:                iso8859-1

### 参见

-   <span class="function">cubrid\_error\_code</span>
-   <span class="function">cubrid\_error\_code\_facility</span>

**目录**

-   [cubrid\_bind](/book/cubrid.html#cubrid_bind) — Bind variables to a
    prepared statement as parameters
-   [cubrid\_close\_prepare](/book/cubrid.html#cubrid_close_prepare) —
    Close the request handle
-   [cubrid\_close\_request](/book/cubrid.html#cubrid_close_request) —
    Close the request handle
-   [cubrid\_col\_get](/book/cubrid.html#cubrid_col_get) — Get contents
    of collection type column using OID
-   [cubrid\_col\_size](/book/cubrid.html#cubrid_col_size) — Get the
    number of elements in collection type column using OID
-   [cubrid\_column\_names](/book/cubrid.html#cubrid_column_names) — Get
    the column names in result
-   [cubrid\_column\_types](/book/cubrid.html#cubrid_column_types) — Get
    column types in result
-   [cubrid\_commit](/book/cubrid.html#cubrid_commit) — Commit a
    transaction
-   [cubrid\_connect\_with\_url](/book/cubrid.html#cubrid_connect_with_url)
    — Establish the environment for connecting to CUBRID server
-   [cubrid\_connect](/book/cubrid.html#cubrid_connect) — Open a
    connection to a CUBRID Server
-   [cubrid\_current\_oid](/book/cubrid.html#cubrid_current_oid) — Get
    OID of the current cursor location
-   [cubrid\_disconnect](/book/cubrid.html#cubrid_disconnect) — Close a
    database connection
-   [cubrid\_drop](/book/cubrid.html#cubrid_drop) — Delete an instance
    using OID
-   [cubrid\_error\_code\_facility](/book/cubrid.html#cubrid_error_code_facility)
    — Get the facility code of error
-   [cubrid\_error\_code](/book/cubrid.html#cubrid_error_code) — Get
    error code for the most recent function call
-   [cubrid\_error\_msg](/book/cubrid.html#cubrid_error_msg) — Get last
    error message for the most recent function call
-   [cubrid\_execute](/book/cubrid.html#cubrid_execute) — Execute a
    prepared SQL statement
-   [cubrid\_fetch](/book/cubrid.html#cubrid_fetch) — Fetch the next row
    from a result set
-   [cubrid\_free\_result](/book/cubrid.html#cubrid_free_result) — Free
    the memory occupied by the result data
-   [cubrid\_get\_autocommit](/book/cubrid.html#cubrid_get_autocommit) —
    Get auto-commit mode of the connection
-   [cubrid\_get\_charset](/book/cubrid.html#cubrid_get_charset) —
    Return the current CUBRID connection charset
-   [cubrid\_get\_class\_name](/book/cubrid.html#cubrid_get_class_name)
    — Get the class name using OID
-   [cubrid\_get\_client\_info](/book/cubrid.html#cubrid_get_client_info)
    — Return the client library version
-   [cubrid\_get\_db\_parameter](/book/cubrid.html#cubrid_get_db_parameter)
    — Returns the CUBRID database parameters
-   [cubrid\_get\_query\_timeout](/book/cubrid.html#cubrid_get_query_timeout)
    — Get the query timeout value of the request
-   [cubrid\_get\_server\_info](/book/cubrid.html#cubrid_get_server_info)
    — Return the CUBRID server version
-   [cubrid\_get](/book/cubrid.html#cubrid_get) — Get a column using OID
-   [cubrid\_insert\_id](/book/cubrid.html#cubrid_insert_id) — Return
    the ID generated for the last updated AUTO\_INCREMENT column
-   [cubrid\_is\_instance](/book/cubrid.html#cubrid_is_instance) — Check
    whether the instance pointed by OID exists
-   [cubrid\_lob\_close](/book/cubrid.html#cubrid_lob_close) — Close
    BLOB/CLOB data
-   [cubrid\_lob\_export](/book/cubrid.html#cubrid_lob_export) — Export
    BLOB/CLOB data to file
-   [cubrid\_lob\_get](/book/cubrid.html#cubrid_lob_get) — Get BLOB/CLOB
    data
-   [cubrid\_lob\_send](/book/cubrid.html#cubrid_lob_send) — Read
    BLOB/CLOB data and send straight to browser
-   [cubrid\_lob\_size](/book/cubrid.html#cubrid_lob_size) — Get
    BLOB/CLOB data size
-   [cubrid\_lob2\_bind](/book/cubrid.html#cubrid_lob2_bind) — Bind a
    lob object or a string as a lob object to a prepared statement as
    parameters
-   [cubrid\_lob2\_close](/book/cubrid.html#cubrid_lob2_close) — Close
    LOB object
-   [cubrid\_lob2\_export](/book/cubrid.html#cubrid_lob2_export) —
    Export the lob object to a file
-   [cubrid\_lob2\_import](/book/cubrid.html#cubrid_lob2_import) —
    Import BLOB/CLOB data from a file
-   [cubrid\_lob2\_new](/book/cubrid.html#cubrid_lob2_new) — Create a
    lob object
-   [cubrid\_lob2\_read](/book/cubrid.html#cubrid_lob2_read) — Read from
    BLOB/CLOB data
-   [cubrid\_lob2\_seek64](/book/cubrid.html#cubrid_lob2_seek64) — Move
    the cursor of a lob object
-   [cubrid\_lob2\_seek](/book/cubrid.html#cubrid_lob2_seek) — Move the
    cursor of a lob object
-   [cubrid\_lob2\_size64](/book/cubrid.html#cubrid_lob2_size64) — Get a
    lob object's size
-   [cubrid\_lob2\_size](/book/cubrid.html#cubrid_lob2_size) — Get a lob
    object's size
-   [cubrid\_lob2\_tell64](/book/cubrid.html#cubrid_lob2_tell64) — Tell
    the cursor position of the LOB object
-   [cubrid\_lob2\_tell](/book/cubrid.html#cubrid_lob2_tell) — Tell the
    cursor position of the LOB object
-   [cubrid\_lob2\_write](/book/cubrid.html#cubrid_lob2_write) — Write
    to a lob object
-   [cubrid\_lock\_read](/book/cubrid.html#cubrid_lock_read) — Set a
    read lock on the given OID
-   [cubrid\_lock\_write](/book/cubrid.html#cubrid_lock_write) — Set a
    write lock on the given OID
-   [cubrid\_move\_cursor](/book/cubrid.html#cubrid_move_cursor) — Move
    the cursor in the result
-   [cubrid\_next\_result](/book/cubrid.html#cubrid_next_result) — Get
    result of next query when executing multiple SQL statements
-   [cubrid\_num\_cols](/book/cubrid.html#cubrid_num_cols) — Return the
    number of columns in the result set
-   [cubrid\_num\_rows](/book/cubrid.html#cubrid_num_rows) — Get the
    number of rows in the result set
-   [cubrid\_pconnect\_with\_url](/book/cubrid.html#cubrid_pconnect_with_url)
    — Open a persistent connection to CUBRID server
-   [cubrid\_pconnect](/book/cubrid.html#cubrid_pconnect) — Open a
    persistent connection to a CUBRID server
-   [cubrid\_prepare](/book/cubrid.html#cubrid_prepare) — Prepare a SQL
    statement for execution
-   [cubrid\_put](/book/cubrid.html#cubrid_put) — Update a column using
    OID
-   [cubrid\_rollback](/book/cubrid.html#cubrid_rollback) — Roll back a
    transaction
-   [cubrid\_schema](/book/cubrid.html#cubrid_schema) — Get the
    requested schema information
-   [cubrid\_seq\_drop](/book/cubrid.html#cubrid_seq_drop) — Delete an
    element from sequence type column using OID
-   [cubrid\_seq\_insert](/book/cubrid.html#cubrid_seq_insert) — Insert
    an element to a sequence type column using OID
-   [cubrid\_seq\_put](/book/cubrid.html#cubrid_seq_put) — Update the
    element value of sequence type column using OID
-   [cubrid\_set\_add](/book/cubrid.html#cubrid_set_add) — Insert a
    single element to set type column using OID
-   [cubrid\_set\_autocommit](/book/cubrid.html#cubrid_set_autocommit) —
    Set autocommit mode of the connection
-   [cubrid\_set\_db\_parameter](/book/cubrid.html#cubrid_set_db_parameter)
    — Sets the CUBRID database parameters
-   [cubrid\_set\_drop](/book/cubrid.html#cubrid_set_drop) — Delete an
    element from set type column using OID
-   [cubrid\_set\_query\_timeout](/book/cubrid.html#cubrid_set_query_timeout)
    — Set the timeout time of query execution
-   [cubrid\_version](/book/cubrid.html#cubrid_version) — Get the CUBRID
    PHP module's version

cubrid\_affected\_rows
======================

Return the number of rows affected by the last SQL statement

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_affected\_rows</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

<span class="type">int</span> <span
class="methodname">cubrid\_affected\_rows</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$req_identifier`</span> \] )

The <span class="function">cubrid\_affected\_rows</span> function is
used to get the number of rows affected by the SQL statement (INSERT,
DELETE, UPDATE).

### 参数

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last link opend by <span class="function">cubrid\_connect</span> is
assumed.

`req_identifier`  
Request Identifier, could be returned from either <span
class="function">cubrid\_prepare</span> or <span
class="function">cubrid\_execute</span>. If the request identifier is
not specified, the last identifier requested by <span
class="function">cubrid\_prepare</span> or <span
class="function">cubrid\_execute</span> is assumed.

### 返回值

Number of rows affected by the SQL statement, when process is
successful.

-1, when SQL statement is not INSERT, DELETE or UPDATE.

**`false`**, when the request identifier is not specified, and there is
no last request.

### 范例

**示例 \#1 <span class="function">cubrid\_affected\_rows</span>
example**

``` php
<?php
$conn = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
cubrid_execute($conn, "DROP TABLE IF EXISTS cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (d varchar)");
$sql_stmt = "INSERT INTO cubrid_test(d) VALUES('php-test')";
$req = cubrid_prepare($conn, $sql_stmt);

for ($i = 0; $i < 10; $i++) {
    cubrid_execute($req);
}
cubrid_commit($conn);

$req = cubrid_execute($conn, "DELETE FROM cubrid_test WHERE d='php-test'", CUBRID_ASYNC);
var_dump(cubrid_affected_rows());
var_dump(cubrid_affected_rows($conn));
var_dump(cubrid_affected_rows($req));

cubrid_disconnect($conn);

print "done!";
?>
```

以上例程会输出：

    Rows deleted: 5

### 参见

-   <span class="function">cubrid\_execute</span>

cubrid\_client\_encoding
========================

Return the current CUBRID connection charset

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_client\_encoding</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

This function returns the current CUBRID connection charset and is
similar to the CUBRID function <span
class="function">cubrid\_get\_charset</span>.

### 参数

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last link opened by <span class="function">cubrid\_connect</span> is
assumed.

### 返回值

A string that represents the CUBRID connection charset; on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_client\_encoding</span>
example**

``` php
<?php

$con = cubrid_connect("localhost", 33000, "demodb");
if (!$con)
{
    die('Could not connect.');
}

printf("CUBRID current charset: %s\n", cubrid_client_encoding($con));

?>
```

以上例程会输出：

    CUBRID current charset: iso8859-1

### 参见

-   <span class="function">cubrid\_get\_charset</span>

cubrid\_close
=============

Close CUBRID connection

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

The <span class="function">cubrid\_close</span> function ends the
transaction currently in process, closes the connection handle and
disconnects from server. If there is any request handles not closed yet
at this point, they will be closed. It is similar to the CUBRID function
<span class="function">cubrid\_disconnect</span>.

### 参数

`conn_identifier`  
The CUBRID connection identifier. If the connection identifier is not
specified, the last connection opened by <span
class="function">cubrid\_connect</span> is assumed.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_close</span> example**

``` php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb");
if ($con) {
   echo "connected successfully";
   $req = cubrid_execute ( $con, "insert into person values(1,'James')");
   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_close ($con);
}
?>
```

### 参见

-   <span class="function">cubrid\_disconnect</span>
-   <span class="function">cubrid\_connect</span>
-   <span class="function">cubrid\_connect\_with\_url</span>

cubrid\_data\_seek
==================

Move the internal row pointer of the CUBRID result

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$row_number`</span> )

This function performs the moving of the internal row pointer of the
CUBRID result (associated with the specified result identifier) to point
to a specific row number. There are functions, such as <span
class="function">cubrid\_fetch\_assoc</span>, which use the current
stored value of `row number`.

### 参数

`result`  
The result.

`row_number`  
This is the desired row number of the new result pointer.

### 返回值

Returns **`true`** on success or **`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_data\_seek</span> example**

``` php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");
cubrid_data_seek($req, 0);

$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_data_seek($req, 2);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_data_seek($req, 4);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(2) {
      [0]=>
      string(1) "X"
      [1]=>
      string(5) "Mixed"
    }
    array(2) {
      [0]=>
      string(1) "M"
      [1]=>
      string(3) "Man"
    }
    array(2) {
      [0]=>
      string(1) "S"
      [1]=>
      string(6) "Silver"
    }

cubrid\_db\_name
================

Get db name from results of cubrid\_list\_dbs

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_db\_name</span> ( <span
class="methodparam"><span class="type">array</span> `$result`</span> ,
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

Retrieve the database name from a call to <span
class="function">cubrid\_list\_dbs</span>.

### 参数

`result`  
The result pointer from a call to <span
class="function">cubrid\_list\_dbs</span>.

`index`  
The index into the result set.

### 返回值

Returns the database name on success, and **`false`** on failure. If
**`false`** is returned, use <span class="function">cubrid\_error</span>
to determine the nature of the error.

### 范例

**示例 \#1 <span class="function">cubrid\_db\_name</span> example**

``` php
<?php
error_reporting(E_ALL);

$conn = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$db_list = cubrid_list_dbs($conn);

$i = 0;
$cnt = count($db_list);
while ($i < $cnt) {
    echo cubrid_db_name($db_list, $i) . "\n";
    $i++;
}
?>
```

以上例程会输出：

    demodb

### 参见

-   <span class="function">cubrid\_list\_dbs</span>

cubrid\_errno
=============

Return the numerical value of the error message from previous CUBRID
operation

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_errno</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

Returns the error number from the last CUBRID function.

The <span class="function">cubrid\_errno</span> function is used to get
the error code of the error that occurred during the API execution.
Usually, it gets the error code when API returns false as its return
value.

### 参数

`conn_identifier`  
The CUBRID connection identifier. If the connection identifier is not
specified, the last connection opened by <span
class="function">cubrid\_connect</span> is assumed.

### 返回值

Returns the error number from the last CUBRID function, or *0* (zero) if
no error occurred.

### 范例

**示例 \#1 <span class="function">cubrid\_errno</span> example**

``` php
<?php
$con = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$req = cubrid_execute($con, "select id, name from person");
if ($req) {
    while (list ($id, $name) = cubrid_fetch($req)) 
    echo $id, $name;
} else {
    echo "Error Code: ", cubrid_errno($con);
    echo "Error Message: ", cubrid_error($con);
}
?>
```

以上例程会输出：

    Error Code: -493 Error Message: Syntax: Unknown class "person". select id, [name] from person

### 参见

-   <span class="function">cubrid\_error</span>
-   <span class="function">cubrid\_error\_code</span>
-   <span class="function">cubrid\_error\_msg</span>

cubrid\_error
=============

Get the error message

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

The <span class="function">cubrid\_error</span> function is used to get
the error message that occurred during the use of CUBRID API. Usually,
it gets error message when API returns false as its return value.

### 参数

`connection`  
The CUBRID connection.

### 返回值

Error message that occurred.

### 范例

**示例 \#1 <span class="function">cubrid\_error</span> example**

``` php
<?php
$con = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$req = cubrid_execute($con, "select id, name from person");
if ($req) {
    while (list ($id, $name) = cubrid_fetch($req)) 
    echo $id, $name;
} else {
    echo "Error Code: ", cubrid_errno($con);
    echo "Error Message: ", cubrid_error($con);
}
?>
```

以上例程会输出：

    Error Code: -493 Error Message: Syntax: Unknown class "person". select id, [name] from person

### 参见

-   <span class="function">cubrid\_errno</span>
-   <span class="function">cubrid\_error\_code</span>
-   <span class="function">cubrid\_error\_msg</span>

cubrid\_fetch\_array
====================

Fetch a result row as an associative array, a numeric array, or both

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = CUBRID\_BOTH</span></span> \] )

The <span class="function">cubrid\_fetch\_array</span> function is used
to get a single row from the query result and returns an array. The
cursor automatically moves to the next row after getting the result.

### 参数

`result`  
`Result` comes from a call to <span
class="function">cubrid\_execute</span>

`type`  
Array type of the fetched result CUBRID\_NUM, CUBRID\_ASSOC,
CUBRID\_BOTH. If you need to operate the lob object, you can use
CUBRID\_LOB.

### 返回值

Returns an array of strings that corresponds to the fetched row, when
process is successful.

**`false`**, when there are no more rows; NULL, when process is
unsuccessful.

The type of returned array depends on how type is defined. By using
CUBRID\_BOTH (default), you'll get an array with both associative and
number indices, and you can decide which data type to use by setting the
`type` argument. The `type` variable can be set to one of the following
values:

-   CUBRID\_NUM : Numerical array (0-based)
-   CUBRID\_ASSOC : Associative array
-   CUBRID\_BOTH : Numerical & Associative array (default)

### 范例

**示例 \#1 <span class="function">cubrid\_fetch\_array</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT name,area,seats,address FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch_array($req, CUBRID_NUM)) {
    printf("%-40s %-10s %-6s %-20s\n", $row[0], $row[1], $row[2], $row[3]);
}

// if you want to operate LOB object, you can use cubrid_fetch_array($req, CUBRID_NUM | CUBRID_LOB)

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    name                                     area       seats  address             
    Panathinaiko Stadium                     86300.00   50000  Athens, Greece      
    Olympic Stadium                          54700.00   13000  Athens, Greece      
    Olympic Indoor Hall                      34100.00   18800  Athens, Greece      
    Olympic Hall                             52400.00   21000  Athens, Greece      
    Olympic Aquatic Centre                   42500.00   11500  Athens, Greece      
    Markopoulo Olympic Equestrian Centre     64000.00   15000  Markopoulo, Athens, Greece
    Faliro Coastal Zone Olympic Complex      34650.00   12171  Faliro, Athens, Greece
    Athens Olympic Stadium                   120400.00  71030  Maroussi, Athens, Greece 
    Ano Liossia                              34000.00   12000  Ano Liosia, Athens, Greece

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_fetch</span>
-   <span class="function">cubrid\_fetch\_row</span>
-   <span class="function">cubrid\_fetch\_assoc</span>
-   <span class="function">cubrid\_fetch\_object</span>

cubrid\_fetch\_assoc
====================

Return the associative array that corresponds to the fetched row

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$type`</span> \] )

This function returns the associative array, that corresponds to the
fetched row, and then moves the internal data pointer ahead, or returns
FALSE when the end is reached.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`type`  
Type can only be CUBRID\_LOB, this parameter will be used only when you
need to operate the lob object.

### 返回值

Associative array, when process is successful.

**`false`**, when there are no more rows; NULL, when process is
unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_fetch\_assoc</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT name,area,seats,address FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch_assoc($req)) {
    printf("%-40s %-10s %-6s %-20s\n", 
        $row["name"], $row["area"], $row["seats"], $row["address"]);
}

// if you want to operate LOB object, you can use cubrid_fetch_assoc($req, CUBRID_LOB)

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    name                                     area       seats  address             
    Panathinaiko Stadium                     86300.00   50000  Athens, Greece      
    Olympic Stadium                          54700.00   13000  Athens, Greece      
    Olympic Indoor Hall                      34100.00   18800  Athens, Greece      
    Olympic Hall                             52400.00   21000  Athens, Greece      
    Olympic Aquatic Centre                   42500.00   11500  Athens, Greece      
    Markopoulo Olympic Equestrian Centre     64000.00   15000  Markopoulo, Athens, Greece
    Faliro Coastal Zone Olympic Complex      34650.00   12171  Faliro, Athens, Greece
    Athens Olympic Stadium                   120400.00  71030  Maroussi, Athens, Greece 
    Ano Liossia                              34000.00   12000  Ano Liosia, Athens, Greece

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_fetch</span>
-   <span class="function">cubrid\_fetch\_row</span>
-   <span class="function">cubrid\_fetch\_array</span>
-   <span class="function">cubrid\_fetch\_object</span>

cubrid\_fetch\_field
====================

Get column information from a result and return as an object

### 说明

<span class="type">object</span> <span
class="methodname">cubrid\_fetch\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`<span class="initializer"> = 0</span></span> \] )

This function returns an object with certain properties of the specific
column. The properties of the object are:

`name`  
column name

`table`  
name of the table that the column belongs to

`def`  
default value of the column

`max_length`  
maximum length of the column

`not_null`  
1 if the column cannot be NULL

`primary_key`  
1 if the column is a primary key

`unique_key`  
1 if the column is an unique key

`multiple_key`  
1 if the column is a non-unique key

`numeric`  
1 if the column is numeric

`blob`  
1 if the column is a BLOB

`type`  
the type of the column

`unsigned`  
1 if the column is unsigned

`zerofill`  
1 if the column is zero-filled

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. If the field offset is not specified, the
next field (that was not yet retrieved by this function) is retrieved.
The `field_offset` starts at 0.

### 返回值

Object with certain properties of the specific column, when process is
successful.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_fetch\_field</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT event_code,athlete_code,nation_code,game_date FROM game WHERE host_year=1988 and event_code=20001;");

var_dump(cubrid_fetch_row($req));

cubrid_field_seek($req, 1);
$field = cubrid_fetch_field($req);

printf("\n--- Field Properties ---\n");
printf("%-30s %s\n", "name:", $field->name);
printf("%-30s %s\n", "table:", $field->table);
printf("%-30s \"%s\"\n", "default value:", $field->def);
printf("%-30s %d\n", "max length:", $field->max_length);
printf("%-30s %d\n", "not null:", $field->not_null);
printf("%-30s %d\n", "primary key:", $field->primary_key);
printf("%-30s %d\n", "unique key:", $field->unique_key);
printf("%-30s %d\n", "multiple key:", $field->multiple_key);
printf("%-30s %d\n", "numeric:", $field->numeric);
printf("%-30s %d\n", "blob:", $field->blob);
printf("%-30s %s\n", "type:", $field->type);
printf("%-30s %d\n", "unsigned:", $field->unsigned);
printf("%-30s %d\n", "zerofill:", $field->zerofill);

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      string(5) "20001"
      [1]=>
      string(5) "16681"
      [2]=>
      string(3) "KOR"
      [3]=>
      string(9) "1988-9-30"
    }

    --- Field Properties ---
    name:                          athlete_code
    table:                         game
    default value:                 ""
    max length:                    0
    not null:                      1
    primary key:                   1
    unique key:                    1
    multiple key:                  0
    numeric:                       1
    blob:                          0
    type:                          integer
    unsigned:                      0
    zerofill:                      0

cubrid\_fetch\_lengths
======================

Return an array with the lengths of the values of each field from the
current row

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_fetch\_lengths</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

This function returns an numeric array with the lengths of the values of
each field from the current row of the result set or it returns FALSE on
failure.

> **Note**:
>
> If field data type is BLOB/CLOB, you should get its length by using
> <span class="function">cubrid\_lob\_size</span>.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

### 返回值

An numeric array, when process is successful.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_fetch\_lengths</span>
example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$row = cubrid_fetch_row($result);
print_r($row);

$lens = cubrid_fetch_lengths($result);
print_r($lens);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Array
    (
        [0] => 2004
        [1] => 20085
        [2] => 15118
        [3] => 30134
        [4] => AUS
        [5] => G
        [6] => 2004-8-20
    )
    Array
    (
        [0] => 4
        [1] => 5
        [2] => 5
        [3] => 5
        [4] => 3
        [5] => 1
        [6] => 10
    )

cubrid\_fetch\_object
=====================

Fetch the next row and return it as an object

### 说明

<span class="type">object</span> <span
class="methodname">cubrid\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$class_name`</span> \[, <span class="methodparam"><span
class="type">array</span> `$params`</span> \[, <span
class="methodparam"><span class="type">int</span> `$type`</span> \]\]\]
)

This function returns an object with the column names of the result set
as properties. The values of these properties are extracted from the
current row of the result.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`class_name`  
The name of the class to instantiate. If not specified, a <span
class="classname">stdClass</span> (stdClass is PHP's generic empty class
that's used when casting other types to objects) object is returned.

`params`  
An optional <span class="type">array</span> of parameters to pass to the
constructor for `class_name` objects.

`type`  
Type can only be CUBRID\_LOB, this parameter will be used only when you
need to operate the lob object.

### 返回值

An object, when process is successful.

**`false`**, when there are no more rows; NULL, when process is
unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_fetch\_object</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$res = cubrid_execute($conn, "SELECT * FROM code");

var_dump(cubrid_fetch_object($res));

// if you want to operate LOB object, you can use cubrid_fetch_object($res, CUBRID_LOB)

class demodb_code {
    public $s_name = null;
    public $f_name = null;

    public function toString() {
        var_dump($this);
    }
}

var_dump(cubrid_fetch_object($res, "demodb_code"));

// if you want to operate LOB object, you can use cubrid_fetch_object($res, "demodb_code", CUBRID_LOB)

class demodb_code_construct extends demodb_code {
    public function __construct($s, $f) {
        $this->s_name = $s; 
        $this->f_name = $f; 
    }   
}

var_dump(cubrid_fetch_object($res, 'demodb_code_construct', array('s_name', 'f_name')));

// if you want to operate LOB object, you can use cubrid_fetch_object($res, 'demodb_code_construct', array('s_name', 'f_name'), CUBRID_LOB)


var_dump(cubrid_fetch_object($res));

cubrid_close_request($res);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    object(stdClass)#1 (2) {
      ["s_name"]=>
      string(1) "X"
      ["f_name"]=>
      string(5) "Mixed"
    }
    object(demodb_code)#1 (2) {
      ["s_name"]=>
      string(1) "W"
      ["f_name"]=>
      string(5) "Woman"
    }
    object(demodb_code_construct)#1 (2) {
      ["s_name"]=>
      string(6) "s_name"
      ["f_name"]=>
      string(6) "f_name"
    }
    object(stdClass)#1 (2) {
      ["s_name"]=>
      string(1) "B"
      ["f_name"]=>
      string(6) "Bronze"
    }

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_fetch</span>
-   <span class="function">cubrid\_fetch\_array</span>
-   <span class="function">cubrid\_fetch\_assoc</span>
-   <span class="function">cubrid\_fetch\_row</span>

cubrid\_fetch\_row
==================

Return a numerical array with the values of the current row

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$type`</span> \] )

This function returns a numerical array with the values of the current
row from the result set, starting from 0, and moves the internal data
pointer ahead.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`type`  
Type can only be CUBRID\_LOB, this parameter will be used only when you
need to operate the lob object.

### 返回值

A numerical array, when process is successful.

**`false`**, when there are no more rows; NULL, when process is
unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_fetch\_row</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT name,area,seats,address FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch_row($req)) {
    printf("%-40s %-10s %-6s %-20s\n", $row[0], $row[1], $row[2], $row[3]);
}

// if you want to operate LOB object, you can use cubrid_fetch_row($req, CUBRID_LOB)

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    name                                     area       seats  address             
    Panathinaiko Stadium                     86300.00   50000  Athens, Greece      
    Olympic Stadium                          54700.00   13000  Athens, Greece      
    Olympic Indoor Hall                      34100.00   18800  Athens, Greece      
    Olympic Hall                             52400.00   21000  Athens, Greece      
    Olympic Aquatic Centre                   42500.00   11500  Athens, Greece      
    Markopoulo Olympic Equestrian Centre     64000.00   15000  Markopoulo, Athens, Greece
    Faliro Coastal Zone Olympic Complex      34650.00   12171  Faliro, Athens, Greece
    Athens Olympic Stadium                   120400.00  71030  Maroussi, Athens, Greece 
    Ano Liossia                              34000.00   12000  Ano Liosia, Athens, Greece

### 参见

-   <span class="function">cubrid\_execute</span>
-   <span class="function">cubrid\_fetch</span>
-   <span class="function">cubrid\_fetch\_array</span>
-   <span class="function">cubrid\_fetch\_assoc</span>
-   <span class="function">cubrid\_fetch\_object</span>

cubrid\_field\_flags
====================

Return a string with the flags of the given field offset

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_field\_flags</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

This function returns a string with the flags of the given field offset
separated by space. You can split the returned value using explode. The
possible flags could be: **`not_null`**, **`primary_key`**,
**`unique_key`**, **`foreign_key`**, **`auto_increment`**, **`shared`**,
**`reverse_index`**, **`reverse_unique`** and **`timestamp`**.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. The `field_offset` starts at 0. If
`field_offset` does not exist, an error of level **`E_WARNING`** is also
issued.

### 返回值

A string with flags, when process is successful.

**`false`** when invalid field\_offset value.

-1 if SQL sentence is not SELECT.

### 范例

**示例 \#1 <span class="function">cubrid\_field\_flags</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$col_num = cubrid_num_cols($result);

printf("%-30s %s\n", "Field Name", "Field Flags");
for($i = 0; $i < $col_num; $i++) {
    printf("%-30s %s\n", cubrid_field_name($result, $i), cubrid_field_flags($result, $i)); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Field Name                     Field Flags
    host_year                      not_null primary_key unique_key
    event_code                     not_null primary_key unique_key foreign_key
    athlete_code                   not_null primary_key unique_key foreign_key
    stadium_code                   not_null
    nation_code                    
    medal                          
    game_date                      

cubrid\_field\_len
==================

Get the maximum length of the specified field

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_field\_len</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

This function returns the maximum length of the specified field on
success, or it returns FALSE on failure.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. The `field_offset` starts at 0. If
`field_offset` does not exist, an error of level **`E_WARNING`** is also
issued.

### 返回值

Maximum length, when process is successful.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_field\_len</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$column_names = cubrid_column_names($result);
$column_types = cubrid_column_types($result);

printf("%-30s %-30s %-15s\n", "Column Names", "Column Types", "Column Maxlen");
for($i = 0, $size = count($column_names); $i < $size; $i++) {
    $column_len = cubrid_field_len($result, $i);
    printf("%-30s %-30s %-15s\n", $column_names[$i], $column_types[$i], $column_len); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Column Names                   Column Types                   Column Maxlen  
    host_year                      integer                        11             
    event_code                     integer                        11             
    athlete_code                   integer                        11             
    stadium_code                   integer                        11             
    nation_code                    char                           3              
    medal                          char                           1              
    game_date                      date                           10                 

cubrid\_field\_name
===================

Return the name of the specified field index

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

This function returns the name of the specified field index on success
or it returns FALSE on failure.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. The `field_offset` starts at 0. If
`field_offset` does not exist, an error of level **`E_WARNING`** is also
issued.

### 返回值

Name of specified field index, on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_field\_name</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$col_num = cubrid_num_cols($result);

printf("%-30s %s\n", "Field Name", "Field Flags");
for($i = 0; $i < $col_num; $i++) {
    printf("%-30s %s\n", cubrid_field_name($result, $i), cubrid_field_flags($result, $i)); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Field Name                     Field Flags
    host_year                      not_null primary_key unique_key
    event_code                     not_null primary_key unique_key foreign_key
    athlete_code                   not_null primary_key unique_key foreign_key
    stadium_code                   not_null
    nation_code                    
    medal                          
    game_date                      

cubrid\_field\_seek
===================

Move the result set cursor to the specified field offset

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_field\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`<span class="initializer"> = 0</span></span> \] )

This function moves the result set cursor to the specified field offset.
This offset is used by <span
class="function">cubrid\_fetch\_field</span> if it doesn't include a
field offset. It returns TRUE on success or FALSE on failure.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. The `field_offset` starts at 0. If
`field_offset` does not exist, an error of level **`E_WARNING`** is also
issued.

### 返回值

**`true`** on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_field\_seek</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT event_code,athlete_code,nation_code,game_date FROM game WHERE host_year=1988 and event_code=20001;");

var_dump(cubrid_fetch_row($req));

cubrid_field_seek($req, 1);
$field = cubrid_fetch_field($req);

printf("\n--- Field Properties ---\n");
printf("%-30s %s\n", "name:", $field->name);
printf("%-30s %s\n", "table:", $field->table);
printf("%-30s \"%s\"\n", "default value:", $field->def);
printf("%-30s %d\n", "max length:", $field->max_length);
printf("%-30s %d\n", "not null:", $field->not_null);
printf("%-30s %d\n", "unique key:", $field->unique_key);
printf("%-30s %d\n", "multiple key:", $field->multiple_key);
printf("%-30s %d\n", "numeric:", $field->numeric);
printf("%-30s %s\n", "type:", $field->type);

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(4) {
      [0]=>
      string(5) "20001"
      [1]=>
      string(5) "16132"
      [2]=>
      string(3) "KOR"
      [3]=>
      string(9) "1988-09-30"
    }

    --- Field Properties ---
    name:                          athlete_code
    table:                         game
    default value:                 ""
    max length:                    0
    not null:                      1
    unique key:                    1
    multiple key:                  0
    numeric:                       1
    type:                          integer

cubrid\_field\_table
====================

Return the name of the table of the specified field

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_field\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

This function returns the name of the table of the specified field. This
is useful when using large select queries with JOINS.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. The `field_offset` starts at 0. If
`field_offset` does not exist, an error of level **`E_WARNING`** is also
issued.

### 返回值

Name of the table of the specified field, on success.

**`false`** when invalid field\_offset value.

-1 if SQL sentence is not SELECT.

### 范例

**示例 \#1 <span class="function">cubrid\_field\_table</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM code");

$col_num = cubrid_num_cols($result);

printf("%-15s %-15s %s\n", "Field Table", "Field Name", "Field Type");
for($i = 0; $i < $col_num; $i++) {
    printf("%-15s %-15s %s\n", 
        cubrid_field_table($result, $i), cubrid_field_name($result, $i), cubrid_field_type($result, $i)); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Field Table     Field Name      Field Type
    code            s_name          char
    code            f_name          varchar

cubrid\_field\_type
===================

Return the type of the column corresponding to the given field offset

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

This function returns the type of the column corresponding to the given
field offset. The returned field type could be one of the following:
"int", "real", "string", etc.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`field_offset`  
The numerical field offset. The `field_offset` starts at 0. If
`field_offset` does not exist, an error of level **`E_WARNING`** is also
issued.

### 返回值

Type of the column, on success.

**`false`** when invalid field\_offset value.

-1 if SQL sentence is not SELECT.

### 范例

**示例 \#1 <span class="function">cubrid\_field\_type</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM code");

$col_num = cubrid_num_cols($result);

printf("%-15s %-15s %s\n", "Field Table", "Field Name", "Field Type");
for($i = 0; $i < $col_num; $i++) {
    printf("%-15s %-15s %s\n", 
        cubrid_field_table($result, $i), cubrid_field_name($result, $i), cubrid_field_type($result, $i)); 
}

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Field Table     Field Name      Field Type
    code            s_name          char
    code            f_name          varchar

cubrid\_list\_dbs
=================

Return an array with the list of all existing CUBRID databases

### 说明

<span class="type">array</span> <span
class="methodname">cubrid\_list\_dbs</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

This function returns an array with the list of all existing Cubrid
databases.

### 参数

`conn_identifier`  
The CUBRID connection.

### 返回值

An numeric array with all existing Cubrid databases; on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_list\_dbs</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$db_list = cubrid_list_dbs($conn);
var_dump($db_list);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(1) {
      [0]=>
      string(6) "demodb"
    }

cubrid\_num\_fields
===================

Return the number of columns in the result set

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

This function returns the number of columns in the result set, on
success, or it returns FALSE on failure.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>, <span
class="function">cubrid\_query</span> and <span
class="function">cubrid\_prepare</span>

### 返回值

Number of columns, on success.

-1 if SQL sentence is not SELECT.

**`false`** when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_num\_fields</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_fields($req);

printf("Row Num: %d\nColumn Num: %d\n", $row_num, $col_num);

cubrid_disconnect($conn);
?>
```

以上例程会输出：

    Row Num: 6
    Column Num: 2

cubrid\_ping
============

Ping a server connection or reconnect if there is no connection

### 说明

<span class="type">bool</span> <span
class="methodname">cubrid\_ping</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

Checks whether or not the connection to the server is working.

### 参数

`conn_identifier`  
The CUBRID connection identifier. If the connection identifier is not
specified, the last connection opened by <span
class="function">cubrid\_connect</span> is assumed.

### 返回值

Returns **`true`** if the connection to the server CUBRID server is
working, otherwise **`false`**.

### 范例

**示例 \#1 <span class="function">cubrid\_ping</span> example**

``` php
<?php
set_time_limit(0);

$conn = cubrid_connect('localhost', 33000, 'demodb');

/* Assuming this query will take a long time */
$sql = "select * from athlete";
$result = cubrid_query($sql);
if (!$result) {
    echo 'Query #1 failed, exiting.';
    exit;
}

/* Make sure the connection is still alive, if not, try to reconnect */
if (!cubrid_ping($conn)) {
    echo 'Lost connection, exiting after query #1';
    exit;
}
cubrid_free_result($result);

/* So the connection is still alive, let's run another query */
$sql2 = "select * from code";
$result2 = cubrid_query($sql2);
?>
```

cubrid\_query
=============

Send a CUBRID query

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

<span class="function">cubrid\_query</span> sends a unique query
(multiple queries are not supported) to the currently active database on
the server that's associated with the specified `conn_identifier`.

### 参数

`query`  
An SQL query

Data inside the query should be
<a href="/book/cubrid.html#cubrid_real_escape_string" class="link">properly escaped</a>.

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last connection opened by <span
class="function">cubrid\_connect</span> is assumed.

### 返回值

For SELECT, SHOW, DESCRIBE, EXPLAIN and other statements returning
resultset, <span class="function">cubrid\_query</span> returns a <span
class="type">resource</span> on success, or **`false`** on error.

For other type of SQL statements, INSERT, UPDATE, DELETE, DROP, etc,
<span class="function">cubrid\_query</span> returns **`true`** on
success or **`false`** on error.

The returned result resource should be passed to <span
class="function">cubrid\_fetch\_array</span>, and other functions for
dealing with result tables, to access the returned data.

Use <span class="function">cubrid\_num\_rows</span> to find out how many
rows were returned for a SELECT statement or <span
class="function">cubrid\_affected\_rows</span> to find out how many rows
were affected by a DELETE, INSERT, REPLACE, or UPDATE statement.

<span class="function">cubrid\_query</span> will also fail and return
**`false`** if the user does not have permission to access the table(s)
referenced by the query.

### 范例

**示例 \#1 Invalid Query**

The following query is syntactically invalid, so <span
class="function">cubrid\_query</span> fails and returns **`false`**.

``` php
<?php
$conn = cubrid_connect('localhost', 33000, 'demodb');

$result = cubrid_query('SELECT * WHERE 1=1');
if (!$result) {
    die('Invalid query: ' . cubrid_error());
}

?>
```

**示例 \#2 Valid Query**

The following query is valid, so <span
class="function">cubrid\_query</span> returns a <span
class="type">resource</span>.

``` php
<?php
// This could be supplied by a user, for example
$firstname = 'fred';
$lastname  = 'fox';

$conn = cubrid_connect('localhost', 33000, 'demodb');

cubrid_execute($conn,"DROP TABLE if exists friends");
cubrid_execute($conn,"create table friends(firstname varchar,lastname varchar,address char(24),age int)");
cubrid_execute($conn,"insert into friends values('fred','fox','home-1','20')");
cubrid_execute($conn,"insert into friends values('blue','cat','home-2','21')");
// Formulate Query
// This is the best way to perform an SQL query
// For more examples, see cubrid_real_escape_string()
$query = sprintf("SELECT firstname, lastname, address, age FROM friends WHERE firstname='%s' AND lastname='%s'",
cubrid_real_escape_string($firstname),
cubrid_real_escape_string($lastname));

// Perform Query
$result = cubrid_query($query);

// Check result
// This shows the actual query sent to CUBRID, and the error. Useful for debugging.
if (!$result) {
    $message  = 'Invalid query: ' . cubrid_error() . "\n";
    $message .= 'Whole query: ' . $query;
    die($message);
}

// Use result
// Attempting to print $result won't allow access to information in the resource
// One of the cubrid result functions must be used
// See also cubrid_result(), cubrid_fetch_array(), cubrid_fetch_row(), etc.
while ($row = cubrid_fetch_assoc($result)) {
    echo $row['firstname'];
    echo $row['lastname'];
    echo $row['address'];
    echo $row['age'];
}

// Free the resources associated with the result set
// This is done automatically at the end of the script
cubrid_free_result($result);
?>
```

### 参见

-   <span class="function">cubrid\_connect</span>
-   <span class="function">cubrid\_error</span>
-   <span class="function">cubrid\_real\_escape\_string</span>
-   <span class="function">cubrid\_result</span>
-   <span class="function">cubrid\_fetch\_assoc</span>
-   <span class="function">cubrid\_unbuffered\_query</span>

cubrid\_real\_escape\_string
============================

Escape special characters in a string for use in an SQL statement

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_real\_escape\_string</span> ( <span
class="methodparam"><span class="type">string</span>
`$unescaped_string`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$conn_identifier`</span> \] )

This function returns the escaped string version of the given string. It
will escape the following characters: **`'`**. In general, single
quotations are used to enclose character string. Double quotations may
be used as well depending on the value of ansi\_quotes, which is a
parameter related to SQL statement. If the ansi\_quotes value is set to
no, character string enclosed by double quotations is handled as
character string, not as an identifier. The default value is yes. If you
want to include a single quote as part of a character string, enter two
single quotes in a row.

### 参数

`unescaped_string`  
The string that is to be escaped.

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last connection opened by <span
class="function">cubrid\_connect</span> is assumed.

### 返回值

Escaped string version of the given string, on success.

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_real\_escape\_string</span>
example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$unescaped_str = ' !"#$%&\'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~';
$escaped_str = cubrid_real_escape_string($unescaped_str);

$len = strlen($unescaped_str);

@cubrid_execute($conn, "DROP TABLE cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (t char($len))");
cubrid_execute($conn, "INSERT INTO cubrid_test (t) VALUES('$escaped_str')");

$req = cubrid_execute($conn, "SELECT * FROM cubrid_test");
$row = cubrid_fetch_assoc($req);

var_dump($row);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    array(1) {
      ["t"]=>
      string(95) " !"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~"
    }

cubrid\_result
==============

Return the value of a specific field in a specific row

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span> `$row`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$field`<span class="initializer"> = 0</span></span> \] )

This function returns the value of a specific field in a specific row
from a result set.

### 参数

`result`  
`result` comes from a call to <span
class="function">cubrid\_execute</span>

`row`  
The row number from the result that is being retrieved. Row numbers
start at 0.

`field`  
The name or offset of the `field` being retrieved. It can be the field's
offset, the field's name, or the field's table dot field name
(tablename.fieldname). If the column name has been aliased ('select foo
as bar from...'), use the alias instead of the column name. If
undefined, the first field is retrieved.

### 返回值

Value of a specific field, on success (NULL if value if null).

**`false`** on failure.

### 范例

**示例 \#1 <span class="function">cubrid\_result</span> example**

``` php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");

$result = cubrid_result($req, 0);
var_dump($result);

$result = cubrid_result($req, 0, 1);
var_dump($result);

$result = cubrid_result($req, 5, "f_name");
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

以上例程会输出：

    string(1) "X"
    string(5) "Mixed"
    string(4) "Gold"

cubrid\_unbuffered\_query
=========================

Perform a query without fetching the results into memory

### 说明

<span class="type">resource</span> <span
class="methodname">cubrid\_unbuffered\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> \] )

This function performs a query without waiting for that all query
results have been complete. It will return when the results are being
generated.

### 参数

`query`  
A SQL query.

`conn_identifier`  
The CUBRID connection. If the connection identifier is not specified,
the last connection opened by <span
class="function">cubrid\_connect</span> is assumed.

### 返回值

For SELECT, SHOW, DESCRIBE or EXPLAIN statements returns a request
identifier resource on success.

For other type of SQL statements, UPDATE, DELETE, DROP, etc, returns
**`true`** on success.

**`false`** on failure.

### 注释

> **Note**:
>
> The benefits of <span
> class="function">cubrid\_unbuffered\_query</span> come at a cost: you
> cannot use <span class="function">cubrid\_num\_rows</span> and <span
> class="function">cubrid\_data\_seek</span> on a result set returned
> from <span class="function">cubrid\_unbuffered\_query</span>.

### 范例

**示例 \#1 <span class="function">cubrid\_unbuffered\_query</span>
example**

``` php
<?php
    $link = cubrid_connect("localhost", 30000, "demodb", "dba", "");
    if (!$link)
    {
        die('Could not connect.');
    }
    $query = "select * from code";
    $result = cubrid_unbuffered_query($query, $link);

    while ($row = cubrid_fetch($result))
    {
        var_dump($row);
    }

    cubrid_close_request($result);
    cubrid_disconnect($link);
?>
```

**目录**

-   [cubrid\_affected\_rows](/book/cubrid.html#cubrid_affected_rows) —
    Return the number of rows affected by the last SQL statement
-   [cubrid\_client\_encoding](/book/cubrid.html#cubrid_client_encoding)
    — Return the current CUBRID connection charset
-   [cubrid\_close](/book/cubrid.html#cubrid_close) — Close CUBRID
    connection
-   [cubrid\_data\_seek](/book/cubrid.html#cubrid_data_seek) — Move the
    internal row pointer of the CUBRID result
-   [cubrid\_db\_name](/book/cubrid.html#cubrid_db_name) — Get db name
    from results of cubrid\_list\_dbs
-   [cubrid\_errno](/book/cubrid.html#cubrid_errno) — Return the
    numerical value of the error message from previous CUBRID operation
-   [cubrid\_error](/book/cubrid.html#cubrid_error) — Get the error
    message
-   [cubrid\_fetch\_array](/book/cubrid.html#cubrid_fetch_array) — Fetch
    a result row as an associative array, a numeric array, or both
-   [cubrid\_fetch\_assoc](/book/cubrid.html#cubrid_fetch_assoc) —
    Return the associative array that corresponds to the fetched row
-   [cubrid\_fetch\_field](/book/cubrid.html#cubrid_fetch_field) — Get
    column information from a result and return as an object
-   [cubrid\_fetch\_lengths](/book/cubrid.html#cubrid_fetch_lengths) —
    Return an array with the lengths of the values of each field from
    the current row
-   [cubrid\_fetch\_object](/book/cubrid.html#cubrid_fetch_object) —
    Fetch the next row and return it as an object
-   [cubrid\_fetch\_row](/book/cubrid.html#cubrid_fetch_row) — Return a
    numerical array with the values of the current row
-   [cubrid\_field\_flags](/book/cubrid.html#cubrid_field_flags) —
    Return a string with the flags of the given field offset
-   [cubrid\_field\_len](/book/cubrid.html#cubrid_field_len) — Get the
    maximum length of the specified field
-   [cubrid\_field\_name](/book/cubrid.html#cubrid_field_name) — Return
    the name of the specified field index
-   [cubrid\_field\_seek](/book/cubrid.html#cubrid_field_seek) — Move
    the result set cursor to the specified field offset
-   [cubrid\_field\_table](/book/cubrid.html#cubrid_field_table) —
    Return the name of the table of the specified field
-   [cubrid\_field\_type](/book/cubrid.html#cubrid_field_type) — Return
    the type of the column corresponding to the given field offset
-   [cubrid\_list\_dbs](/book/cubrid.html#cubrid_list_dbs) — Return an
    array with the list of all existing CUBRID databases
-   [cubrid\_num\_fields](/book/cubrid.html#cubrid_num_fields) — Return
    the number of columns in the result set
-   [cubrid\_ping](/book/cubrid.html#cubrid_ping) — Ping a server
    connection or reconnect if there is no connection
-   [cubrid\_query](/book/cubrid.html#cubrid_query) — Send a CUBRID
    query
-   [cubrid\_real\_escape\_string](/book/cubrid.html#cubrid_real_escape_string)
    — Escape special characters in a string for use in an SQL statement
-   [cubrid\_result](/book/cubrid.html#cubrid_result) — Return the value
    of a specific field in a specific row
-   [cubrid\_unbuffered\_query](/book/cubrid.html#cubrid_unbuffered_query)
    — Perform a query without fetching the results into memory

cubrid\_load\_from\_glo
=======================

Read data from a GLO instance and save it in a file

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_load\_from\_glo</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$file_name`</span>
)

The <span class="function">cubrid\_load\_from\_glo</span> function is
used to read a data from a glo instance, and saves it in a designated
file.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
Oid of the glo instance that you want to read the data from.

`file_name`  
Name of the file where you want to save the data in.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_load\_from\_glo</span>
example**

``` php
<?php
$req = cubrid_execute ($con, "select image from person where id=1");
if ($req) {
   list ($oid) = cubrid_fetch($req);
   cubrid_close_request($req);
   $res = cubrid_load_from_glo ($con, $oid, "output.jpg");
   if ($res) {
      echo "image changed successfully";
   }
}
?>
```

### 注释

> **Note**:
>
> 为了向下兼容，可以使用下列已废弃的别名： <span
> class="function">cubrid\_load\_from\_glo</span>

> **Note**:
>
> This function is removed from CUBRID 3.1.

### 参见

-   <span class="function">cubrid\_new\_glo</span>
-   <span class="function">cubrid\_save\_to\_glo</span>
-   <span class="function">cubrid\_send\_glo</span>

cubrid\_new\_glo
================

Create a glo instance

### 说明

<span class="type">string</span> <span
class="methodname">cubrid\_new\_glo</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$class_name`</span> , <span
class="methodparam"><span class="type">string</span> `$file_name`</span>
)

The <span class="function">cubrid\_new\_glo</span> function is used to
create a glo instance in the requested class (glo class). The glo
created is a LO type, and is stored in the `file_name` file.

### 参数

`conn_identifier`  
Connection identifier.

`class_name`  
Name of the class that you want to create a glo in.

`file_name`  
The file name that you want to save in the newly created glo.

### 返回值

Oid of the instance created, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_new\_glo</span> example**

``` php
<?php
$oid = cubrid_new_glo ($con, "glo", "input.jpg");
if ($oid){
   // the type of column "image" is "object"
   $req = cubrid_execute ($con, "insert into person(image) values($oid)");
   if ($req) {
      echo "image inserted successfully";
      cubrid_close_request ($req);
      cubrid_commit($con);
   }
}
?>
```

### 注释

> **Note**:
>
> 为了向下兼容，可以使用下列已废弃的别名： <span
> class="function">cubrid\_new\_glo</span>

> **Note**:
>
> This function is removed from CUBRID 3.1.

### 参见

-   <span class="function">cubrid\_save\_to\_glo</span>
-   <span class="function">cubrid\_load\_from\_glo</span>
-   <span class="function">cubrid\_send\_glo</span>

cubrid\_save\_to\_glo
=====================

Save requested file in a GLO instance

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_save\_to\_glo</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$file_name`</span>
)

The <span class="function">cubrid\_save\_to\_glo</span> function is used
to save requested file in a glo instance.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
Oid of the glo instance that you want to save a file in.

`file_name`  
The name of the file that you want to save.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_save\_to\_glo</span> example**

``` php
<?php
$req = cubrid_execute ($con, "select image from person where id=1");
if ($req) {
   list ($oid) = cubrid_fetch($req);
   cubrid_close_request($req);
   $res = cubrid_save_to_glo ($con, $oid, "input.jpg");
   if ($res) {
      echo "image changed successfully";
   }
}
?>
```

### 注释

> **Note**:
>
> 为了向下兼容，可以使用下列已废弃的别名： <span
> class="function">cubrid\_save\_to\_glo</span>

> **Note**:
>
> This function is removed from CUBRID 3.1.

### 参见

-   <span class="function">cubrid\_new\_glo</span>
-   <span class="function">cubrid\_load\_from\_glo</span>
-   <span class="function">cubrid\_send\_glo</span>

cubrid\_send\_glo
=================

Read data from glo and send it to std output

### 说明

<span class="type">int</span> <span
class="methodname">cubrid\_send\_glo</span> ( <span
class="methodparam"><span class="type">resource</span>
`$conn_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$oid`</span> )

The <span class="function">cubrid\_send\_glo</span> function is used to
read data from glo instance and sends it to the PHP standard output.

### 参数

`conn_identifier`  
Connection identifier.

`oid`  
Oid of the glo instance that you want to read data from.

### 返回值

**`true`**, when process is successful.

**`false`**, when process is unsuccessful.

### 范例

**示例 \#1 <span class="function">cubrid\_send\_glo</span> example**

``` php
<?php
$req = cubrid_execute ($con, "select image from person where id =1");
if ($req) {
  list ($oid) = cubrid_fetch($req);
  cubrid_close_request($req);
  Header ("Content-type: image/jpeg");
  cubrid_send_glo ($con, $oid);
}
?>
```

### 注释

> **Note**:
>
> 为了向下兼容，可以使用下列已废弃的别名： <span
> class="function">cubrid\_send\_glo</span>

> **Note**:
>
> This function is removed from CUBRID 3.1.

### 参见

-   <span class="function">cubrid\_new\_glo</span>
-   <span class="function">cubrid\_save\_to\_glo</span>
-   <span class="function">cubrid\_load\_from\_glo</span>

**目录**

-   [cubrid\_load\_from\_glo](/book/cubrid.html#cubrid_load_from_glo) —
    Read data from a GLO instance and save it in a file
-   [cubrid\_new\_glo](/book/cubrid.html#cubrid_new_glo) — Create a glo
    instance
-   [cubrid\_save\_to\_glo](/book/cubrid.html#cubrid_save_to_glo) — Save
    requested file in a GLO instance
-   [cubrid\_send\_glo](/book/cubrid.html#cubrid_send_glo) — Read data
    from glo and send it to std output
