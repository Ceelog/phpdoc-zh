PostgreSQL
==========

**目录**

-   [简介](/book/pgsql.html#简介)
-   [安装／配置](/book/pgsql.html#安装／配置)
    -   [需求](/book/pgsql.html#需求)
    -   [安装](/book/pgsql.html#安装)
    -   [运行时配置](/book/pgsql.html#运行时配置)
    -   [资源类型](/book/pgsql.html#资源类型)
-   [预定义常量](/book/pgsql.html#预定义常量)
-   [范例](/book/pgsql.html#范例)
    -   [Basic usage](/book/pgsql.html#Basic%20usage)
    -   [Basic usage](/book/pgsql.html#Basic%20usage)
-   [PostgreSQL 函数](/book/pgsql.html#PostgreSQL%20函数)
    -   [pg\_affected\_rows](/book/pgsql.html#pg_affected_rows) —
        返回受影响的记录数目
    -   [pg\_cancel\_query](/book/pgsql.html#pg_cancel_query) —
        取消异步查询
    -   [pg\_client\_encoding](/book/pgsql.html#pg_client_encoding) —
        取得客户端编码方式
    -   [pg\_close](/book/pgsql.html#pg_close) — 关闭一个 PostgreSQL
        连接
    -   [pg\_connect\_poll](/book/pgsql.html#pg_connect_poll) —
        正在进行尝试轮询 PostgreSQL 链接状态。
    -   [pg\_connect](/book/pgsql.html#pg_connect) — 打开一个 PostgreSQL
        连接
    -   [pg\_connection\_busy](/book/pgsql.html#pg_connection_busy) —
        获知连接是否为忙
    -   [pg\_connection\_reset](/book/pgsql.html#pg_connection_reset) —
        重置连接（再次连接）
    -   [pg\_connection\_status](/book/pgsql.html#pg_connection_status)
        — 获得连接状态
    -   [pg\_consume\_input](/book/pgsql.html#pg_consume_input) — Reads
        input on the connection
    -   [pg\_convert](/book/pgsql.html#pg_convert) —
        将关联的数组值转换为适合 SQL 语句的格式。
    -   [pg\_copy\_from](/book/pgsql.html#pg_copy_from) —
        根据数组将记录插入表中
    -   [pg\_copy\_to](/book/pgsql.html#pg_copy_to) —
        将一个表拷贝到数组中
    -   [pg\_dbname](/book/pgsql.html#pg_dbname) — 获得数据库名
    -   [pg\_delete](/book/pgsql.html#pg_delete) — 删除记录
    -   [pg\_end\_copy](/book/pgsql.html#pg_end_copy) — 与 PostgreSQL
        后端同步
    -   [pg\_escape\_bytea](/book/pgsql.html#pg_escape_bytea) — 转义
        bytea 类型的二进制数据
    -   [pg\_escape\_identifier](/book/pgsql.html#pg_escape_identifier)
        — Escape a identifier for insertion into a text field
    -   [pg\_escape\_literal](/book/pgsql.html#pg_escape_literal) —
        Escape a literal for insertion into a text field
    -   [pg\_escape\_string](/book/pgsql.html#pg_escape_string) — 转义
        text/char 类型的字符串
    -   [pg\_execute](/book/pgsql.html#pg_execute) — Sends a request to
        execute a prepared statement with given parameters, and waits
        for the result
    -   [pg\_fetch\_all\_columns](/book/pgsql.html#pg_fetch_all_columns)
        — Fetches all rows in a particular result column as an array
    -   [pg\_fetch\_all](/book/pgsql.html#pg_fetch_all) —
        从结果中提取所有行作为一个数组
    -   [pg\_fetch\_array](/book/pgsql.html#pg_fetch_array) —
        提取一行作为数组
    -   [pg\_fetch\_assoc](/book/pgsql.html#pg_fetch_assoc) —
        提取一行作为关联数组
    -   [pg\_fetch\_object](/book/pgsql.html#pg_fetch_object) —
        提取一行作为对象
    -   [pg\_fetch\_result](/book/pgsql.html#pg_fetch_result) —
        从结果资源中返回值
    -   [pg\_fetch\_row](/book/pgsql.html#pg_fetch_row) —
        提取一行作为枚举数组
    -   [pg\_field\_is\_null](/book/pgsql.html#pg_field_is_null) —
        测试字段是否为 NULL
    -   [pg\_field\_name](/book/pgsql.html#pg_field_name) —
        返回字段的名字
    -   [pg\_field\_num](/book/pgsql.html#pg_field_num) — 返回字段的编号
    -   [pg\_field\_prtlen](/book/pgsql.html#pg_field_prtlen) —
        返回打印出来的长度
    -   [pg\_field\_size](/book/pgsql.html#pg_field_size) —
        返回指定字段占用内部存储空间的大小
    -   [pg\_field\_table](/book/pgsql.html#pg_field_table) — Returns
        the name or oid of the tables field
    -   [pg\_field\_type\_oid](/book/pgsql.html#pg_field_type_oid) —
        Returns the type ID (OID) for the corresponding field number
    -   [pg\_field\_type](/book/pgsql.html#pg_field_type) —
        返回相应字段的类型名称
    -   [pg\_flush](/book/pgsql.html#pg_flush) —
        刷新链接中已处理的数据查询
    -   [pg\_free\_result](/book/pgsql.html#pg_free_result) —
        释放查询结果占用的内存
    -   [pg\_get\_notify](/book/pgsql.html#pg_get_notify) — Ping
        数据库连接
    -   [pg\_get\_pid](/book/pgsql.html#pg_get_pid) — Ping 数据库连接
    -   [pg\_get\_result](/book/pgsql.html#pg_get_result) —
        取得异步查询结果
    -   [pg\_host](/book/pgsql.html#pg_host) — 返回和某连接关联的主机名
    -   [pg\_insert](/book/pgsql.html#pg_insert) — 将数组插入到表中
    -   [pg\_last\_error](/book/pgsql.html#pg_last_error) —
        得到某连接的最后一条错误信息
    -   [pg\_last\_notice](/book/pgsql.html#pg_last_notice) — 返回
        PostgreSQL 服务器最新一条公告信息
    -   [pg\_last\_oid](/book/pgsql.html#pg_last_oid) — 返回上一个对象的
        oid
    -   [pg\_lo\_close](/book/pgsql.html#pg_lo_close) — 关闭一个大型对象
    -   [pg\_lo\_create](/book/pgsql.html#pg_lo_create) —
        新建一个大型对象
    -   [pg\_lo\_export](/book/pgsql.html#pg_lo_export) —
        将大型对象导出到文件
    -   [pg\_lo\_import](/book/pgsql.html#pg_lo_import) —
        将文件导入为大型对象
    -   [pg\_lo\_open](/book/pgsql.html#pg_lo_open) — 打开一个大型对象
    -   [pg\_lo\_read\_all](/book/pgsql.html#pg_lo_read_all) —
        读入整个大型对象并直接发送给浏览器
    -   [pg\_lo\_read](/book/pgsql.html#pg_lo_read) —
        从大型对象中读入数据
    -   [pg\_lo\_seek](/book/pgsql.html#pg_lo_seek) —
        移动大型对象中的指针
    -   [pg\_lo\_tell](/book/pgsql.html#pg_lo_tell) —
        返回大型对象的当前指针位置
    -   [pg\_lo\_truncate](/book/pgsql.html#pg_lo_truncate) — Truncates
        a large object
    -   [pg\_lo\_unlink](/book/pgsql.html#pg_lo_unlink) —
        删除一个大型对象
    -   [pg\_lo\_write](/book/pgsql.html#pg_lo_write) —
        向大型对象写入数据
    -   [pg\_meta\_data](/book/pgsql.html#pg_meta_data) — 获得表的元数据
    -   [pg\_num\_fields](/book/pgsql.html#pg_num_fields) —
        返回字段的数目
    -   [pg\_num\_rows](/book/pgsql.html#pg_num_rows) — 返回行的数目
    -   [pg\_options](/book/pgsql.html#pg_options) —
        获得和连接有关的选项
    -   [pg\_parameter\_status](/book/pgsql.html#pg_parameter_status) —
        Looks up a current parameter setting of the server
    -   [pg\_pconnect](/book/pgsql.html#pg_pconnect) — 打开一个持久的
        PostgreSQL 连接
    -   [pg\_ping](/book/pgsql.html#pg_ping) — Ping 数据库连接
    -   [pg\_port](/book/pgsql.html#pg_port) — 返回该连接的端口号
    -   [pg\_prepare](/book/pgsql.html#pg_prepare) — Submits a request
        to create a prepared statement with the given parameters, and
        waits for completion
    -   [pg\_put\_line](/book/pgsql.html#pg_put_line) — 向 PostgreSQL
        后端发送以 NULL 结尾的字符串
    -   [pg\_query\_params](/book/pgsql.html#pg_query_params) — Submits
        a command to the server and waits for the result, with the
        ability to pass parameters separately from the SQL command text
    -   [pg\_query](/book/pgsql.html#pg_query) — 执行查询
    -   [pg\_result\_error\_field](/book/pgsql.html#pg_result_error_field)
        — Returns an individual field of an error report
    -   [pg\_result\_error](/book/pgsql.html#pg_result_error) —
        获得查询结果的错误信息
    -   [pg\_result\_seek](/book/pgsql.html#pg_result_seek) —
        在结果资源中设定内部行偏移量
    -   [pg\_result\_status](/book/pgsql.html#pg_result_status) —
        获得查询结果的状态
    -   [pg\_select](/book/pgsql.html#pg_select) — 选择记录
    -   [pg\_send\_execute](/book/pgsql.html#pg_send_execute) — Sends a
        request to execute a prepared statement with given parameters,
        without waiting for the result(s)
    -   [pg\_send\_prepare](/book/pgsql.html#pg_send_prepare) — Sends a
        request to create a prepared statement with the given
        parameters, without waiting for completion
    -   [pg\_send\_query\_params](/book/pgsql.html#pg_send_query_params)
        — Submits a command and separate parameters to the server
        without waiting for the result(s)
    -   [pg\_send\_query](/book/pgsql.html#pg_send_query) — 发送异步查询
    -   [pg\_set\_client\_encoding](/book/pgsql.html#pg_set_client_encoding)
        — 设定客户端编码
    -   [pg\_set\_error\_verbosity](/book/pgsql.html#pg_set_error_verbosity)
        — Determines the verbosity of messages returned by
        pg\_last\_error and pg\_result\_error
    -   [pg\_socket](/book/pgsql.html#pg_socket) — Get a read only
        handle to the socket underlying a PostgreSQL connection
    -   [pg\_trace](/book/pgsql.html#pg_trace) — 启动一个 PostgreSQL
        连接的追踪功能
    -   [pg\_transaction\_status](/book/pgsql.html#pg_transaction_status)
        — Returns the current in-transaction status of the server
    -   [pg\_tty](/book/pgsql.html#pg_tty) — 返回该连接的 tty 号
    -   [pg\_unescape\_bytea](/book/pgsql.html#pg_unescape_bytea) — 取消
        bytea 类型中的字符串转义
    -   [pg\_untrace](/book/pgsql.html#pg_untrace) — 关闭 PostgreSQL
        连接的追踪功能
    -   [pg\_update](/book/pgsql.html#pg_update) — 更新表
    -   [pg\_version](/book/pgsql.html#pg_version) — Returns an array
        with client, protocol and server version (when available)

PostgreSQL database is an Open Source product and available without
cost. Postgres, developed originally in the UC Berkeley Computer Science
Department, pioneered many of the object-relational concepts now
becoming available in some commercial databases. It provides SQL92/SQL99
language support, transactions, referential integrity, stored procedures
and type extensibility. PostgreSQL is an open source descendant of this
original Berkeley code.

安装／配置
==========

**目录**

-   [需求](/book/pgsql.html#需求)
-   [安装](/book/pgsql.html#安装)
-   [运行时配置](/book/pgsql.html#运行时配置)
-   [资源类型](/book/pgsql.html#资源类型)

需求
----

To use PostgreSQL support, you need PostgreSQL 6.5 or later, PostgreSQL
8.0 or later to enable all PostgreSQL module features. PostgreSQL
supports many character encodings including multibyte character
encoding. The current version and more information about PostgreSQL is
available at
<a href="http://www.postgresql.org/" class="link external">» http://www.postgresql.org/</a>
and the
<a href="http://www.postgresql.org/docs/current/interactive/" class="link external">» PostgreSQL Documentation</a>.

安装
----

为添加 PostgreSQL 支持，在编译 PHP 时需要加上 **--with-pgsql\[=DIR\]**
选项。如果可以用共享模块方式，PostgreSQL 模块可以在 `php.ini` 用
<a href="/ini/core.html#ini.extension" class="link">extension</a>
指令或者 <span class="function">dl</span> 函数加载。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                     | 默认 | 可修改范围       | 更新日志                |
|--------------------------------------------------------------------------|------|------------------|-------------------------|
| <a href="/book/pgsql.html#" class="link">pgsql.allow_persistent</a>      | "1"  | PHP\_INI\_SYSTEM |                         |
| <a href="/book/pgsql.html#" class="link">pgsql.max_persistent</a>        | "-1" | PHP\_INI\_SYSTEM |                         |
| <a href="/book/pgsql.html#" class="link">pgsql.max_links</a>             | "-1" | PHP\_INI\_SYSTEM |                         |
| <a href="/book/pgsql.html#" class="link">pgsql.auto_reset_persistent</a> | "0"  | PHP\_INI\_SYSTEM | 从 PHP 4.2.0 起开始存在 |
| <a href="/book/pgsql.html#" class="link">pgsql.ignore_notice</a>         | "0"  | PHP\_INI\_ALL    | 从 PHP 4.3.0 起开始存在 |
| <a href="/book/pgsql.html#" class="link">pgsql.log_notice</a>            | "0"  | PHP\_INI\_ALL    | 从 PHP 4.3.0 起开始存在 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`pgsql.allow_persistent` <span class="type">boolean</span>  
是否允许持久的 Postgres 连接。

`pgsql.max_persistent` <span class="type">integer</span>  
每个进程所能有的持久 Postgres 连接数目。

`pgsql.max_links` <span class="type">integer</span>  
每个进程所能有的 Postgres 连接数目，包括持久连接。

`pgsql.auto_reset_persistent` <span class="type">integer</span>  
检测用在 <span class="function">pg\_pconnect</span>
上的中断了的持久连接。需要一些损耗。

`pgsql.ignore_notice` <span class="type">integer</span>  
是否忽略 PostgreSQL 后端的通告。

`pgsql.log_notice` <span class="type">integer</span>  
是否记录 PostgreSQL 后端的通告消息。要记录通告消息日志，PHP 指令
<a href="/book/pgsql.html#" class="link">pgsql.ignore_notice</a> 必须为
off。

资源类型
--------

There are two resource types used in the PostgreSQL module. The first
one is the link identifier for a database connection, the second a
resource which holds the result of a query.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`PGSQL_ASSOC`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_fetch\_array</span>. Return an associative array of
field names and values. </span>

**`PGSQL_NUM`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_fetch\_array</span>. Return a numerically indexed
array of field numbers and values. </span>

**`PGSQL_BOTH`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_fetch\_array</span>. Return an array of field
values that is both numerically indexed (by field number) and associated
(by field name). </span>

**`PGSQL_CONNECT_FORCE_NEW`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_connect</span> to force the creation of a new
connection, rather then re-using an existing identical connection.
</span>

**`PGSQL_CONNECTION_BAD`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_connection\_status</span> indicating that the
database connection is in an invalid state. </span>

**`PGSQL_CONNECTION_OK`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_connection\_status</span> indicating that the
database connection is in a valid state. </span>

**`PGSQL_SEEK_SET`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_lo\_seek</span>. Seek operation is to begin from
the start of the object. </span>

**`PGSQL_SEEK_CUR`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_lo\_seek</span>. Seek operation is to begin from
the current position. </span>

**`PGSQL_SEEK_END`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_lo\_seek</span>. Seek operation is to begin from
the end of the object. </span>

**`PGSQL_EMPTY_QUERY`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. The string sent to the
server was empty. </span>

**`PGSQL_COMMAND_OK`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. Successful completion of a
command returning no data. </span>

**`PGSQL_TUPLES_OK`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. Successful completion of a
command returning data (such as a *SELECT* or *SHOW*). </span>

**`PGSQL_COPY_OUT`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. Copy Out (from server) data
transfer started. </span>

**`PGSQL_COPY_IN`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. Copy In (to server) data
transfer started. </span>

**`PGSQL_BAD_RESPONSE`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. The server's response was
not understood. </span>

**`PGSQL_NONFATAL_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. A nonfatal error (a notice
or warning) occurred. </span>

**`PGSQL_FATAL_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_result\_status</span>. A fatal error occurred.
</span>

**`PGSQL_TRANSACTION_IDLE`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_transaction\_status</span>. Connection is currently
idle, not in a transaction. </span>

**`PGSQL_TRANSACTION_ACTIVE`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_transaction\_status</span>. A command is in
progress on the connection. A query has been sent via the connection and
not yet completed. </span>

**`PGSQL_TRANSACTION_INTRANS`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_transaction\_status</span>. The connection is idle,
in a transaction block. </span>

**`PGSQL_TRANSACTION_INERROR`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_transaction\_status</span>. The connection is idle,
in a failed transaction block. </span>

**`PGSQL_TRANSACTION_UNKNOWN`** (<span class="type">integer</span>)  
<span class="simpara"> Returned by <span
class="function">pg\_transaction\_status</span>. The connection is bad.
</span>

**`PGSQL_DIAG_SEVERITY`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The severity; the
field contents are *ERROR*, *FATAL*, or *PANIC* (in an error message),
or *WARNING*, *NOTICE*, *DEBUG*, *INFO*, or *LOG* (in a notice message),
or a localized translation of one of these. Always present. </span>

**`PGSQL_DIAG_SQLSTATE`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The SQLSTATE code for
the error. The SQLSTATE code identifies the type of error that has
occurred; it can be used by front-end applications to perform specific
operations (such as error handling) in response to a particular database
error. This field is not localizable, and is always present. </span>

**`PGSQL_DIAG_MESSAGE_PRIMARY`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The primary
human-readable error message (typically one line). Always present.
</span>

**`PGSQL_DIAG_MESSAGE_DETAIL`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. Detail: an optional
secondary error message carrying more detail about the problem. May run
to multiple lines. </span>

**`PGSQL_DIAG_MESSAGE_HINT`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. Hint: an optional
suggestion what to do about the problem. This is intended to differ from
detail in that it offers advice (potentially inappropriate) rather than
hard facts. May run to multiple lines. </span>

**`PGSQL_DIAG_STATEMENT_POSITION`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. A string containing a
decimal integer indicating an error cursor position as an index into the
original statement string. The first character has index 1, and
positions are measured in characters not bytes. </span>

**`PGSQL_DIAG_INTERNAL_POSITION`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. This is defined the
same as the **`PG_DIAG_STATEMENT_POSITION`** field, but it is used when
the cursor position refers to an internally generated command rather
than the one submitted by the client. The **`PG_DIAG_INTERNAL_QUERY`**
field will always appear when this field appears. </span>

**`PGSQL_DIAG_INTERNAL_QUERY`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The text of a failed
internally-generated command. This could be, for example, a SQL query
issued by a PL/pgSQL function. </span>

**`PGSQL_DIAG_CONTEXT`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. An indication of the
context in which the error occurred. Presently this includes a call
stack traceback of active procedural language functions and
internally-generated queries. The trace is one entry per line, most
recent first. </span>

**`PGSQL_DIAG_SOURCE_FILE`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The file name of the
PostgreSQL source-code location where the error was reported. </span>

**`PGSQL_DIAG_SOURCE_LINE`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The line number of the
PostgreSQL source-code location where the error was reported. </span>

**`PGSQL_DIAG_SOURCE_FUNCTION`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_error\_field</span>. The name of the
PostgreSQL source-code function reporting the error. </span>

**`PGSQL_ERRORS_TERSE`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_set\_error\_verbosity</span>. Specified that
returned messages include severity, primary text, and position only;
this will normally fit on a single line. </span>

**`PGSQL_ERRORS_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_set\_error\_verbosity</span>. The default mode
produces messages that include the above plus any detail, hint, or
context fields (these may span multiple lines). </span>

**`PGSQL_ERRORS_VERBOSE`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_set\_error\_verbosity</span>. The verbose mode
includes all available fields. </span>

**`PGSQL_STATUS_LONG`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_status</span>. Indicates that numerical
result code is desired. </span>

**`PGSQL_STATUS_STRING`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_result\_status</span>. Indicates that textual
result command tag is desired. </span>

**`PGSQL_CONV_IGNORE_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_convert</span>. Ignore default values in the table
during conversion. </span>

**`PGSQL_CONV_FORCE_NULL`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_convert</span>. Use SQL *NULL* in place of an empty
<span class="type">string</span>. </span>

**`PGSQL_CONV_IGNORE_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> Passed to <span
class="function">pg\_convert</span>. Ignore conversion of **`NULL`**
into SQL *NOT NULL* columns. </span>

范例
====

**目录**

-   [Basic usage](/book/pgsql.html#Basic%20usage)
-   [Basic usage](/book/pgsql.html#Basic%20usage)

Basic usage
-----------

This simple example shows how to connect, execute a query, print
resulting rows and disconnect from a PostgreSQL database.

**示例 \#1 PostgreSQL extension overview example**

``` php
<?php
// Connecting, selecting database
$dbconn = pg_connect("host=localhost dbname=publishing user=www password=foo")
    or die('Could not connect: ' . pg_last_error());

// Performing SQL query
$query = 'SELECT * FROM authors';
$result = pg_query($query) or die('Query failed: ' . pg_last_error());

// Printing results in HTML
echo "<table>\n";
while ($line = pg_fetch_array($result, null, PGSQL_ASSOC)) {
    echo "\t<tr>\n";
    foreach ($line as $col_value) {
        echo "\t\t<td>$col_value</td>\n";
    }
    echo "\t</tr>\n";
}
echo "</table>\n";

// Free resultset
pg_free_result($result);

// Closing connection
pg_close($dbconn);
?>
```

Basic usage
-----------

These examples contain user defined functions similar to legacy MySQL
functions.

**示例 \#1 PostgreSQL user defined functions example**

``` php
<?php
// This function should be needed, since PostgreSQL connection binds database.
function pg_list_dbs($db)
{
    assert(is_resource($db));
    $query = '
SELECT
 d.datname as "Name",
 u.usename as "Owner",
 pg_encoding_to_char(d.encoding) as "Encoding"
FROM
 pg_database d LEFT JOIN pg_user u ON d.datdba = u.usesysid
ORDER BY 1;
';
    return pg_query($db, $query);
}

// List tables.
function pg_list_tables($db)
{
    assert(is_resource($db));
    $query = "
SELECT
 c.relname as \"Name\",
 CASE c.relkind WHEN 'r' THEN 'table' WHEN 'v' THEN 'view' WHEN 'i' THEN 'index' WHEN 'S' THEN 'sequence' WHEN 's' THEN 'special' END as \"Type\",
  u.usename as \"Owner\"
FROM
 pg_class c LEFT JOIN pg_user u ON c.relowner = u.usesysid
WHERE
 c.relkind IN ('r','v','S','')
 AND c.relname !~ '^pg_'
ORDER BY 1;
";
    return pg_query($db, $query);
}

// See also pg_meta_data(). It returns field definition as array.
function pg_list_fields($db, $table)
{
    assert(is_resource($db));
    $query = "
SELECT
 a.attname,
 format_type(a.atttypid, a.atttypmod),
 a.attnotnull,
 a.atthasdef,
 a.attnum
FROM
 pg_class c,
 pg_attribute a
WHERE
 c.relname = '".$table."'
 AND a.attnum > 0 AND a.attrelid = c.oid
ORDER BY a.attnum;
";
    return pg_query($db, $query);
}
?>
```

注释
----

> **Note**:
>
> Not all functions are supported by all builds. It depends on your
> libpq (The PostgreSQL C client library) version and how libpq is
> compiled. If PHP PostgreSQL extensions are missing, then it is because
> your libpq version does not support them.

> **Note**:
>
> Most PostgreSQL functions accept `connection` as the optional first
> parameter. If it is not provided, the last opened connection is used.
> If it doesn't exist, functions return **`FALSE`**.

> **Note**:
>
> PostgreSQL automatically folds all identifiers (e.g. table/column
> names) to lower-case values at object creation time and at query time.
> To force the use of mixed or upper case identifiers, you must escape
> the identifier using double quotes ("").

> **Note**:
>
> PostgreSQL does not have special commands for fetching database schema
> information (eg. all the tables in the current database). Instead,
> there is a standard schema named *information\_schema* in PostgreSQL
> 7.4 and above containing system views with all the necessary
> information, in an easily queryable form. See the
> <a href="http://www.postgresql.org/docs/current/interactive/" class="link external">» PostgreSQL Documentation</a>
> for full details.

pg\_affected\_rows
==================

返回受影响的记录数目

### 说明

<span class="type">int</span> <span
class="methodname">pg\_affected\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_affected\_rows</span> 返回在 <span
class="function">pg\_query</span> 中执行 INSERT，UPDATE 和 DELETE
查询后受到影响的记录数目（包括实例／记录／行）。如果本函数没有影响到任何记录，则返回
0。

**示例 \#1 <span class="function">pg\_affected\_rows</span> 例子**

``` php
<?php
$result = pg_query($conn, "INSERT INTO authors VALUES ('Orwell', 2002, 'Animal Farm')");
$cmdtuples = pg_affected_rows($result);
echo $cmdtuples . " tuples are affected.\n";
?>
```

> **Note**:
>
> 本函数以前被称为 *pg\_cmdtuples()*。

参见 <span class="function">pg\_query</span> 和 <span
class="function">pg\_num\_rows</span>。

pg\_cancel\_query
=================

取消异步查询

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_cancel\_query</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_cancel\_query</span> 取消由 <span
class="function">pg\_send\_query</span> 发送的异步查询。不能取消由 <span
class="function">pg\_query</span> 执行的查询。

参见 <span class="function">pg\_send\_query</span> 和 <span
class="function">pg\_connection\_busy</span>。

pg\_client\_encoding
====================

取得客户端编码方式

### 说明

<span class="type">string</span> <span
class="methodname">pg\_client\_encoding</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_client\_encoding</span>
以字符串形式返回客户端编码。所返回的字符串为以下之一：SQL\_ASCII，EUC\_JP，EUC\_CN，EUC\_KR，EUC\_TW，UNICODE，MULE\_INTERNAL，LATINX
(X=1...9)，KOI8，WIN，ALT，SJIS，BIG5，WIN1250。

> **Note**:
>
> 本函数需要 PHP-4.0.3 或以上版本以及 PostgreSQL-7.0
> 或以上版本。如果在编译 libpq 时没有加入多字节编码支持，则 <span
> class="function">pg\_set\_client\_encoding</span> 总是返回
> "SQL\_ASCII"。所支持的编码方式取决于 PostgreSQL 的版本。详情参见
> PostgreSQL 手册如何加入多字节支持以及所支持的编码方式。
>
> 本函数以前被称为 <span class="function">pg\_clientencoding</span>。

参见 <span class="function">pg\_set\_client\_encoding</span>。

pg\_close
=========

关闭一个 PostgreSQL 连接

### 说明

<span class="type">bool</span> <span class="methodname">pg\_close</span>
(\[ <span class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_close</span> 关闭由所给资源 `connection`
指定的到 PostgreSQL 数据库的非持久连接。

> **Note**:
>
> 使用 <span class="function">pg\_close</span>
> 并不很必要，因为非持久连接在本脚本执行结束后会自动关闭。

如果在此连接中打开了 large object 资源，则在关闭所有 large object
资源之前不要关闭连接。

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_close</span> 例子**

``` php
<?php
$dbconn = pg_connect("host=localhost port=5432 dbname=mary")
   or die("Could not connect");
echo "Connected successfully";
pg_close($dbconn);
?>
```

以上例程会输出：

    Connected successfully

### 参见

-   <span class="function">pg\_connect</span>

pg\_connect\_poll
=================

正在进行尝试轮询 PostgreSQL 链接状态。

### 说明

<span class="type">int</span> <span
class="methodname">pg\_connect\_poll</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_connect\_poll</span> 轮询使用 <span
class="function">pg\_connect</span> 创建的 PostgreSQL 链接状态，根据
**`PGSQL_CONNECT_ASYNC`** 选项

### 参数

`connection`  
PostgreSQL 数据库链接资源

### 返回值

返回常量 **`PGSQL_POLLING_FAILED`**, **`PGSQL_POLLING_READING`**,
**`PGSQL_POLLING_WRITING`**, **`PGSQL_POLLING_OK`**, 或者
**`PGSQL_POLLING_ACTIVE`**.

pg\_connect
===========

打开一个 PostgreSQL 连接

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_connect</span> ( <span class="methodparam"><span
class="type">string</span> `$connection_string`</span> )

<span class="function">pg\_connect</span> 返回其它 PostgreSQL
函数所需要的资源。

<span class="function">pg\_connect</span> 打开一个由 `connection_string`
所指定的 PostgreSQL
数据库的连接。如果成功则返回连接资源，如果不能连接则返回
**`FALSE`**。`connection_string` 应该是用引号引起来的字符串。

**示例 \#1 使用 <span class="function">pg\_connect</span>**

``` php
<?php
$dbconn = pg_connect("dbname=mary");
//connect to a database named "mary"
$dbconn2 = pg_connect("host=localhost port=5432 dbname=mary");
// connect to a database named "mary" on "localhost" at port "5432"
$dbconn3 = pg_connect("host=sheep port=5432 dbname=mary user=lamb password=foo");
//connect to a database named "mary" on the host "sheep" with a username and password

$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";
$dbconn4 = pg_connect($conn_string);
//connect to a database named "test" on the host "sheep" with a username and password
?>
```

`connection_string` 所包括的参数有 `host`，`port`，`tty`,
`options`，`dbname`, `user` 和 `password`。

如果用同样的 `connection_string` 再次调用 <span
class="function">pg\_connect</span>，不会建立新连接，而是返回前面已经打开的连接资源。如果使用不同的连接字符串，则可以和同一个数据库建立多个连接。

旧的多参数语法 **$conn = pg\_connect("host", "port", "options", "tty",
"dbname")** 已经不提倡使用。

参见 <span class="function">pg\_pconnect</span>，<span
class="function">pg\_close</span>，<span
class="function">pg\_host</span>，<span
class="function">pg\_port</span>, <span
class="function">pg\_tty</span>，<span
class="function">pg\_options</span> 和 <span
class="function">pg\_dbname</span>。

pg\_connection\_busy
====================

获知连接是否为忙

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_connection\_busy</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_connection\_busy</span>
在此连接状态为忙的时候返回
**`TRUE`**。如果连接状态为忙，说明前一个查询仍然在执行。如果调用 <span
class="function">pg\_get\_result</span> 函数的话，则会被锁死。

**示例 \#1 <span class="function">pg\_connection\_busy</span> 例子**

``` php
<?php
    $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
    $bs = pg_connection_busy($dbconn);
    if ($bs) {
        echo 'connection is busy';
    }
    else {
       echo 'connection is not busy';
    }
?>
```

参见 <span class="function">pg\_connection\_status</span> 和 <span
class="function">pg\_get\_result</span>。

pg\_connection\_reset
=====================

重置连接（再次连接）

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_connection\_reset</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_connection\_reset</span>
重置一个连接，用于错误恢复。

### 参数

`connection`  
PostgreSQL database connection resource.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_connection\_reset</span> 例子**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
  $dbconn2 = pg_connection_reset($dbconn);
  if ($dbconn2) {
      echo "reset successful\n";
  } else {
      echo "reset failed\n";
  }
?>
```

### 参见

-   <span class="function">pg\_connect</span>
-   <span class="function">pg\_pconnect</span>
-   <span class="function">pg\_connection\_status</span>

pg\_connection\_status
======================

获得连接状态

### 说明

<span class="type">int</span> <span
class="methodname">pg\_connection\_status</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_connection\_status</span>
返回一个连接的状态。可能的状态为 *PGSQL\_CONNECTION\_OK* 和
*PGSQL\_CONNECTION\_BAD*。

**示例 \#1 <span class="function">pg\_connection\_status</span> 例子**

``` php
<?php
    $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
    $stat = pg_connection_status($dbconn);
    echo 'connection_status: '.$stat;
?>
```

**示例 \#2 <span class="function">pg\_connection\_status</span> 例子**

``` php
<?php
    $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
    $stat = pg_connection_status($dbconn);
    echo 'connection_status: '.$stat;
?>
```

参见 <span class="function">pg\_connection\_busy</span>。

pg\_consume\_input
==================

Reads input on the connection

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_consume\_input</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_consume\_input</span> consumes any input
waiting to be read from the database server.

### 参数

`connection`  
PostgreSQL database connection resource.

### 返回值

**`TRUE`** if no error occurred, or **`FALSE`** if there was an error.
Note that **`TRUE`** does not necessarily indicate that input was
waiting to be read.

pg\_convert
===========

将关联的数组值转换为适合 SQL 语句的格式。

### 说明

<span class="type">array</span> <span
class="methodname">pg\_convert</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">array</span> `$assoc_array`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

<span class="function">pg\_convert</span> 检查 *assoc\_array*
中的值并将其转换为为适用于 SQL 语句的值。<span
class="function">pg\_convert</span> 的前提条件是现有的表 *table\_name*
中具有的列至少有 *assoc\_array* 中的单元那么多。*table\_name*
中的字段名以及字段值必须和 *assoc\_array*
中的键名及值匹配。如果成功则返回一个包括转换后的值的数组，否则返回
**`FALSE`**。

> **Note**:
>
> If there are boolean fields in `table_name` don't use the constant
> **`TRUE`** in `assoc_array`. It will be converted to the string 'TRUE'
> which is no valid entry for boolean fields in PostgreSQL. Use one of
> t, true, 1, y, yes instead.

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`connection`  
PostgreSQL database connection resource.

`table_name`  
Name of the table against which to convert types.

`assoc_array`  
Data to be converted.

`options`  
Any number of **`PGSQL_CONV_IGNORE_DEFAULT`**,
**`PGSQL_CONV_FORCE_NULL`** or **`PGSQL_CONV_IGNORE_NOT_NULL`**,
combined.

### 返回值

An <span class="type">array</span> of converted values, or **`FALSE`**
on error.

### 范例

**示例 \#1 <span class="function">pg\_convert</span> example**

``` php
<?php 
  $dbconn = pg_connect('dbname=foo');
  
  $tmp = array(
      'author' => 'Joe Thackery',
      'year' => 2005,
      'title' => 'My Life, by Joe Thackery'
  );
  
  $vals = pg_convert($dbconn, 'authors', $tmp);
?>
```

### 参见

-   <span class="function">pg\_meta\_data</span>

pg\_copy\_from
==============

根据数组将记录插入表中

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_copy\_from</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$table_name`</span> , <span
class="methodparam"><span class="type">array</span> `$rows`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$delimiter`</span> \[, <span class="methodparam"><span
class="type">string</span> `$null_as`</span> \]\] )

<span class="function">pg\_copy\_from</span> 将数组 `rows`
的内容作为记录插入表中。它在内部使用了 *COPY FROM* SQL 命令来插入记录。

### 参数

`connection`  
PostgreSQL database connection resource.

`table_name`  
Name of the table into which to copy the `rows`.

`rows`  
An <span class="type">array</span> of data to be copied into
`table_name`. Each value in `rows` becomes a row in `table_name`. Each
value in `rows` should be a delimited string of the values to insert
into each field. Values should be linefeed terminated.

`delimiter`  
The token that separates values for each field in each element of
`rows`. Default is *TAB*.

`null_as`  
How SQL *NULL* values are represented in the `rows`. Default is \\N
("\\N").

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_copy\_from</span> example**

``` php
<?php
   $db = pg_connect("dbname=publisher") or die("Could not connect");
   
   $rows = pg_copy_to($db, $table_name);
   
   pg_query($db, "DELETE FROM $table_name");
   
   pg_copy_from($db, $table_name, $rows);
?>
```

### 参见

-   <span class="function">pg\_copy\_to</span>

pg\_copy\_to
============

将一个表拷贝到数组中

### 说明

<span class="type">array</span> <span
class="methodname">pg\_copy\_to</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$delimiter`</span> \[, <span
class="methodparam"><span class="type">string</span> `$null_as`</span>
\]\] )

<span class="function">pg\_copy\_to</span>
将一个表拷贝到数组中，该数组作为结果返回。它在内部使用了 *COPY FROM* SQL
命令来插入记录，并返回结果数组。如果失败则返回 **`FALSE`**。

参见 <span class="function">pg\_copy\_from</span>。

pg\_dbname
==========

获得数据库名

### 说明

<span class="type">string</span> <span
class="methodname">pg\_dbname</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

<span class="function">pg\_dbname</span> 返回给定 PostgreSQL
`connection` 资源的数据库名称。如果 `connection` 不是有效的 PostgreSQL
连接资源则返回 **`FALSE`**。

**示例 \#1 <span class="function">pg\_dbname</span> 例子**

``` php
<?php
    error_reporting(E_ALL);

    pg_connect("host=localhost port=5432 dbname=mary");
    echo pg_dbname(); // mary
?>
```

pg\_delete
==========

删除记录

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">array</span> `$assoc_array`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = PGSQL\_DML\_EXEC</span></span> \] )

<span class="function">pg\_delete</span> 删除符合条件的记录，条件在
*assoc\_array* 中以 *field=\>value* 格式给出。如果指定了 *option*，则
<span class="function">pg\_convert</span> 按照该选项作用于
*assoc\_array* 之上。

### 参数

`connection`  
PostgreSQL database connection resource.

`table_name`  
Name of the table from which to delete rows.

`assoc_array`  
An <span class="type">array</span> whose keys are field names in the
table `table_name`, and whose values are the values of those fields that
are to be deleted.

`options`  
Any number of **`PGSQL_CONV_FORCE_NULL`**, **`PGSQL_DML_NO_CONV`**,
**`PGSQL_DML_EXEC`** or **`PGSQL_DML_STRING`** combined. If
**`PGSQL_DML_STRING`** is part of the `options` then query string is
returned.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Returns <span
class="type">string</span> if **`PGSQL_DML_STRING`** is passed via
`options`.

### 范例

**示例 \#1 <span class="function">pg\_delete</span> 例子**

``` php
<?php 
  $db = pg_connect('dbname=foo');
  // This is safe, since $_POST is converted automatically
  $res = pg_delete($db, 'post_log', $_POST);
  if ($res) {
      echo "POST data is deleted: $res\n";
  } else {
      echo "User must have sent wrong inputs\n";
  }
?>
```

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">pg\_convert</span>

pg\_end\_copy
=============

与 PostgreSQL 后端同步

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_end\_copy</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_end\_copy</span> 在处理完 <span
class="function">pg\_put\_line</span> 所执行的拷贝操作之后将 PostgreSQL
前端（通常为 web server 进程）与 PostgreSQL 服务器进行同步。<span
class="function">pg\_end\_copy</span> 必须被调用，否则 PostgreSQL
服务器可能会和前端失去同步并报错。

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_end\_copy</span> 例子**

``` php
<?php 
  $conn = pg_pconnect("dbname=foo");
  pg_query($conn, "create table bar (a int4, b char(16), d float8)");
  pg_query($conn, "copy bar from stdin");
  pg_put_line($conn, "3\thello world\t4.5\n");
  pg_put_line($conn, "4\tgoodbye world\t7.11\n");
  pg_put_line($conn, "\.\n");
  pg_end_copy($conn);
?>
```

### 参见

-   <span class="function">pg\_put\_line</span>

pg\_escape\_bytea
=================

转义 bytea 类型的二进制数据

### 说明

<span class="type">string</span> <span
class="methodname">pg\_escape\_bytea</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">pg\_escape\_bytea</span> 转义 bytea
数据类型的二进制字符串，返回转义后的字符串。

> **Note**:
>
> 当对 bytea 类型字段进行 SELECT 操作时，PostgreSQL 返回前导 \\
> 的八进制字节值（例如 \\032）。用户需要自己将结果转换为二进制格式。
>
> 本函数需要 PostgreSQL 7.2 或以上版本。在 PostgreSQL 7.2.0 和 7.2.1
> 版中，如果使用了多字节支持，bytea 类型必须被强制转换。例如 *INSERT
> INTO test\_table (image) VALUES
> ('$image\_escaped'::bytea);*。PostgreSQL 7.2.2
> 或以上版本不需要强制转换。异常情况是当客户端和后端字符编码不匹配时，可能会有多字节流错误。用户必须强制转换
> bytea 以避免此错误。

参见 <span class="function">pg\_unescape\_bytea</span> 和 <span
class="function">pg\_escape\_string</span>。

pg\_escape\_identifier
======================

Escape a identifier for insertion into a text field

### 说明

<span class="type">string</span> <span
class="methodname">pg\_escape\_identifier</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="function">pg\_escape\_identifier</span> escapes a
identifier (e.g. table, field names) for querying the database. It
returns an escaped identifier string for PostgreSQL server. <span
class="function">pg\_escape\_identifier</span> adds double quotes before
and after data. Users should not add double quotes. Use of this function
is recommended for identifier parameters in query. For SQL literals
(i.e. parameters except bytea), <span
class="function">pg\_escape\_literal</span> or <span
class="function">pg\_escape\_string</span> must be used. For bytea type
fields, <span class="function">pg\_escape\_bytea</span> must be used
instead.

> **Note**:
>
> This function has internal escape code and can also be used with
> PostgreSQL 8.4 or less.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`data`  
A <span class="type">string</span> containing text to be escaped.

### 返回值

A <span class="type">string</span> containing the escaped data.

### 范例

**示例 \#1 <span class="function">pg\_escape\_identifier</span>
example**

``` php
<?php 
  // Connect to the database
  $dbconn = pg_connect('dbname=foo');
  
  // Escape the table name data
  $escaped = pg_escape_identifier($table_name);
  
  // Select rows from $table_name
  pg_query("SELECT * FROM {$escaped};");
?>
```

### 参见

-   <span class="function">pg\_escape\_literal</span>
-   <span class="function">pg\_escape\_bytea</span>
-   <span class="function">pg\_escape\_string</span>

pg\_escape\_literal
===================

Escape a literal for insertion into a text field

### 说明

<span class="type">string</span> <span
class="methodname">pg\_escape\_literal</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="function">pg\_escape\_literal</span> escapes a literal for
querying the PostgreSQL database. It returns an escaped literal in the
PostgreSQL format. <span class="function">pg\_escape\_literal</span>
adds quotes before and after data. Users should not add quotes. Use of
this function is recommended instead of <span
class="function">pg\_escape\_string</span>. If the type of the column is
bytea, <span class="function">pg\_escape\_bytea</span> must be used
instead. For escaping identifiers (e.g. table, field names), <span
class="function">pg\_escape\_identifier</span> must be used.

> **Note**:
>
> This function has internal escape code and can also be used with
> PostgreSQL 8.4 or less.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>. When there is no default
connection, it raises *E\_WARNING* and returns **`FALSE`**.

`data`  
A <span class="type">string</span> containing text to be escaped.

### 返回值

A <span class="type">string</span> containing the escaped data.

### 范例

**示例 \#1 <span class="function">pg\_escape\_literal</span> example**

``` php
<?php 
  // Connect to the database
  $dbconn = pg_connect('dbname=foo');
  
  // Read in a text file (containing apostrophes and backslashes)
  $data = file_get_contents('letter.txt');
  
  // Escape the text data
  $escaped = pg_escape_literal($data);
  
  // Insert it into the database. Note that no quotes around {$escaped}
  pg_query("INSERT INTO correspondence (name, data) VALUES ('My letter', {$escaped})");
?>
```

### 参见

-   <span class="function">pg\_escape\_identifier</span>
-   <span class="function">pg\_escape\_bytea</span>
-   <span class="function">pg\_escape\_string</span>

pg\_escape\_string
==================

转义 text/char 类型的字符串

### 说明

<span class="type">string</span> <span
class="methodname">pg\_escape\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">pg\_escape\_string</span> 转义 text/char
数据类型的字符串，返回转义后的字符串。建议用此函数替代 <span
class="function">addslashes</span>。

> **Note**:
>
> 本函数需要 PostgreSQL 7.2 或以上版本。

参见 <span class="function">pg\_escape\_bytea</span>。

pg\_execute
===========

Sends a request to execute a prepared statement with given parameters,
and waits for the result

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_execute</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$stmtname`</span> , <span
class="methodparam"><span class="type">array</span> `$params`</span> )

Sends a request to execute a prepared statement with given parameters,
and waits for the result.

<span class="function">pg\_execute</span> is like <span
class="function">pg\_query\_params</span>, but the command to be
executed is specified by naming a previously-prepared statement, instead
of giving a query string. This feature allows commands that will be used
repeatedly to be parsed and planned just once, rather than each time
they are executed. The statement must have been prepared previously in
the current session. <span class="function">pg\_execute</span> is
supported only against PostgreSQL 7.4 or higher connections; it will
fail when using earlier versions.

The parameters are identical to <span
class="function">pg\_query\_params</span>, except that the name of a
prepared statement is given instead of a query string.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`stmtname`  
The name of the prepared statement to execute. if "" is specified, then
the unnamed statement is executed. The name must have been previously
prepared using <span class="function">pg\_prepare</span>, <span
class="function">pg\_send\_prepare</span> or a *PREPARE* SQL command.

`params`  
An array of parameter values to substitute for the $1, $2, etc.
placeholders in the original prepared query string. The number of
elements in the array must match the number of placeholders.

**Warning**
Elements are converted to strings by calling this function.

### 返回值

A query result resource on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Using <span class="function">pg\_execute</span>**

``` php
<?php
// Connect to a database named "mary"
$dbconn = pg_connect("dbname=mary");

// Prepare a query for execution
$result = pg_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');

// Execute the prepared query.  Note that it is not necessary to escape
// the string "Joe's Widgets" in any way
$result = pg_execute($dbconn, "my_query", array("Joe's Widgets"));

// Execute the same prepared query, this time with a different parameter
$result = pg_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));

?>
```

### 参见

-   <span class="function">pg\_prepare</span>
-   <span class="function">pg\_send\_prepare</span>
-   <span class="function">pg\_query\_params</span>

pg\_fetch\_all\_columns
=======================

Fetches all rows in a particular result column as an array

### 说明

<span class="type">array</span> <span
class="methodname">pg\_fetch\_all\_columns</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$column`<span class="initializer"> = 0</span></span> \] )

<span class="function">pg\_fetch\_all\_columns</span> returns an array
that contains all rows (records) in a particular column of the result
resource.

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 参数

`result`  
PostgreSQL query result resource, returned by <span
class="function">pg\_query</span>, <span
class="function">pg\_query\_params</span> or <span
class="function">pg\_execute</span> (among others).

`column`  
Column number, zero-based, to be retrieved from the result resource.
Defaults to the first column if not specified.

### 返回值

An <span class="type">array</span> with all values in the result column.

**`FALSE`** is returned if `column` is larger than the number of columns
in the result, or on any other error.

### 范例

**示例 \#1 <span class="function">pg\_fetch\_all\_columns</span>
example**

``` php
<?php 
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "An error occurred.\n";
  exit;
}

$result = pg_query($conn, "SELECT title, name, address FROM authors");
if (!$result) {
  echo "An error occurred.\n";
  exit;
}

// Get an array of all author names
$arr = pg_fetch_all_columns($result, 1);

var_dump($arr);

?>
```

### 参见

-   <span class="function">pg\_fetch\_all</span>

pg\_fetch\_all
==============

从结果中提取所有行作为一个数组

### 说明

<span class="type">array</span> <span
class="methodname">pg\_fetch\_all</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_fetch\_all</span>
从结果资源中返回一个包含有所有的行（元组/记录）的数组。如果没有更多行可供提取，则返回
**`FALSE`**。

**示例 \#1 <span class="function">pg\_fetch\_all</span> 例子**

``` php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "An error occured.\n";
    exit;
}
$result = pg_query($conn, "SELECT * FROM authors");
if (!$result) {
    echo "An error occured.\n";
    exit;
}
$arr = pg_fetch_all($result);
var_dump($arr);
?>
```

参见 <span class="function">pg\_fetch\_row</span>，<span
class="function">pg\_fetch\_array</span>，<span
class="function">pg\_fetch\_object</span> 和 <span
class="function">pg\_fetch\_result</span>。

pg\_fetch\_array
================

提取一行作为数组

### 说明

<span class="type">array</span> <span
class="methodname">pg\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row`</span> \[, <span class="methodparam"><span
class="type">int</span> `$result_type`</span> \]\] )

<span class="function">pg\_fetch\_array</span>
返回一个与所提取的行（元组/记录）相一致的数组。如果没有更多行可供提取，则返回
**`FALSE`**。

<span class="function">pg\_fetch\_array</span> 是 <span
class="function">pg\_fetch\_row</span>
的扩展版本。在返回的数组中不仅以数字索引方式存放数据（字段编号），默认情况下还用字段名做索引存放数据（字段名）。

`row` 是想要取得的行（记录）的编号。第一行为 0。

`result_type` 是可选参数，控制着怎样初始化返回值。`result_type`
是一个常量，可以有以下取值：**`PGSQL_ASSOC`**，**`PGSQL_NUM`** 和
**`PGSQL_BOTH`**。取值为 **`PGSQL_ASSOC`** 时 <span
class="function">pg\_fetch\_array</span>
返回用字段名作为键值索引的关联数组，取值为 **`PGSQL_NUM`**
时用字段编号作为键值，取值为 **`PGSQL_BOTH`**
时则同时用两者作为键值。默认值是 **`PGSQL_BOTH`**。

> **Note**:
>
> `result_type` 是在 PHP 4.0 中才加入的参数。

<span class="function">pg\_fetch\_array</span> 并不明显比使用 <span
class="function">pg\_fetch\_row</span>
慢，而且在使用中提供了更大的方便。

**示例 \#1 <span class="function">pg\_fetch\_array</span>**

``` php
<?php 

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "An error occured.\n";
    exit;
}

$result = pg_query($conn, "SELECT * FROM authors");
if (!$result) {
    echo "An error occured.\n";
    exit;
}

$arr = pg_fetch_array($result, 0, PGSQL_NUM);
echo $arr[0] . " <- array\n";

$arr = pg_fetch_array($result, 1, PGSQL_ASSOC);
echo $arr["author"] . " <- array\n";

?>
```

> **Note**:
>
> 从 4.1.0 开始，`row` 成为可选参数。每次调用 <span
> class="function">pg\_fetch\_array</span>，内部的行计数器都会加一。

参见 <span class="function">pg\_fetch\_row</span> 和 <span
class="function">pg\_fetch\_object</span> 以及 <span
class="function">pg\_fetch\_result</span>。

pg\_fetch\_assoc
================

提取一行作为关联数组

### 说明

<span class="type">array</span> <span
class="methodname">pg\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row`</span> \] )

<span class="function">pg\_fetch\_assoc</span> 和调用 <span
class="function">pg\_fetch\_array</span> 加上第三个可选参数 PGSQL\_ASSOC
是等价的。它只返回一个关联数组。如果需要数字索引，用 <span
class="function">pg\_fetch\_row</span>。

<span class="function">pg\_fetch\_assoc</span> 是 <span
class="function">pg\_fetch\_row</span>
的扩展版本。除了将数据存储在数字索引（字段编号）之外，默认还将数组存储在关联索引（字段名）中。

`row` 是要被提取的行（记录）编号。第一行为 0。

<span class="function">pg\_fetch\_assoc</span> 并不明显比 <span
class="function">pg\_fetch\_row</span> 慢，而且还显著更便于使用。

**示例 \#1 <span class="function">pg\_fetch\_assoc</span> 例子**

``` php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "An error occured.\n";
    exit;
}

$result = pg_query($conn, "SELECT id, author, email FROM authors");
if (!$result) {
    echo "An error occured.\n";
    exit;
}
while ($row = pg_fetch_assoc($result)) {
    echo $row['id'];
    echo $row['author'];
    echo $row['email'];
}
?>
```

参见 <span class="function">pg\_fetch\_row</span>，<span
class="function">pg\_fetch\_array</span>，<span
class="function">pg\_fetch\_object</span> 和 <span
class="function">pg\_fetch\_result</span>。

pg\_fetch\_object
=================

提取一行作为对象

### 说明

<span class="type">object</span> <span
class="methodname">pg\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row`</span> \[, <span class="methodparam"><span
class="type">int</span> `$result_type`</span> \]\] )

<span class="function">pg\_fetch\_object</span>
返回与所提取行的属性相一致的一个对象。如果出错或者没有更多行可供提取时则返回
**`FALSE`**。

<span class="function">pg\_fetch\_object</span> 和 <span
class="function">pg\_fetch\_array</span> 相似，只有一点区别 －
返回一个对象而不是数组。间接的，这意味着只能通过字段名来访问数据而不能通过偏移量来访问（数字是非法的属性名）。

`row` 是想要取得的行（记录）的编号。第一行为 0。

除了速度之外，本函数和 <span class="function">pg\_fetch\_array</span>
完全一样，而且几乎和 <span class="function">pg\_fetch\_row</span>
一样快（速度上的差别很小）。

> **Note**:
>
> 从 4.1.0 版本开始，参数 `row` 变为可选参数。
>
> 从 4.3.0 开始，`result_type` 默认值为 PGSQL\_ASSOC，而旧版本的默认值是
> PGSQL\_BOTH。数字属性在这里没有用处，因为在 PHP
> 中对象的属性不能是数字。
>
> `result_type` 参数在以后的版本中可能会删除。

**示例 \#1 <span class="function">pg\_fetch\_object</span>**

``` php
<?php 

$database = "store";

$db_conn = pg_connect("host=localhost port=5432 dbname=$database");
if (!$db_conn) {
    echo "Failed connecting to postgres database $database\n";
    exit;
}

$qu = pg_query($db_conn, "SELECT * FROM books ORDER BY author");

$row = 0; // postgres needs a row counter 

while ($data = pg_fetch_object($qu, $row)) {
    echo $data->author . " (";
    echo $data->year . "): ";
    echo $data->title . "<br />";
    $row++;
}

pg_free_result ($qu);
pg_close ($db_conn);

?>
```

> **Note**:
>
> 从 4.1.0 开始，`row` 成为可选参数。每次调用 <span
> class="function">pg\_fetch\_object</span>，内部的行计数器都会加一。

参见 <span class="function">pg\_query</span>，<span
class="function">pg\_fetch\_array</span>，<span
class="function">pg\_fetch\_row</span> 和 <span
class="function">pg\_fetch\_result</span>。

pg\_fetch\_result
=================

从结果资源中返回值

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_fetch\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span> `$row`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$field`</span> )

<span class="function">pg\_fetch\_result</span> 根据由 <span
class="function">pg\_query</span> 返回的 `result`
资源返回相应的值。`row` 为整型数。`field`
为字段名（字符串）或字段索引（整数）。`row` 和 `field`
指明了查询结果中的哪个单元被返回。行编号从 0
开始。除了用字段名之外，还可以用不带引号的数字作为字段索引。字段索引从 0
开始。

PostgreSQL 有很多内置的类型，这里只直接支持基本类型。所有形式的 <span
class="type">integer</span>，<span class="type">boolean</span> 和 void
类型都被返回为 <span class="type">integer</span> 值。所有形式的 float 和
real 类型都被返回为 <span class="type">float</span> 值。Boolean
类型被返回为 "t" 或者
"f"。所有其它类型包括数组都被返回为字符串，该字符串的格式和默认的
PostgreSQL 风格一样，可以在 **psql** 程序中看到。

pg\_fetch\_row
==============

提取一行作为枚举数组

### 说明

<span class="type">array</span> <span
class="methodname">pg\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row`</span> \] )

<span class="function">pg\_fetch\_row</span> 根据指定的 `result`
资源提取一行数据（记录）作为数组返回。每个得到的列依次存放在数组中，从偏移量
0 开始。

> **Note**: <span class="simpara">此函数将 NULL 字段设置为 PHP
> **`NULL`** 值。</span>

### 参数

`result`  
PostgreSQL query result resource, returned by <span
class="function">pg\_query</span>, <span
class="function">pg\_query\_params</span> or <span
class="function">pg\_execute</span> (among others).

`row`  
Row number in result to fetch. Rows are numbered from 0 upwards. If
omitted or **`NULL`**, the next row is fetched.

### 返回值

An <span class="type">array</span>, indexed from 0 upwards, with each
value represented as a <span class="type">string</span>. Database *NULL*
values are returned as **`NULL`**.

返回的数组和提取的行相一致。如果没有更多行 `row` 可提取，则返回
**`FALSE`**。

### 更新日志

| 版本  | 说明                      |
|-------|---------------------------|
| 4.1.0 | 参数 `row` 成为可选参数。 |

### 范例

**示例 \#1 <span class="function">pg\_fetch\_row</span> 例子**

``` php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "An error occured.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "An error occured.\n";
  exit;
}

while ($row = pg_fetch_row($result)) {
  echo "Author: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}
 
?>
```

### 参见

-   <span class="function">pg\_query</span>
-   <span class="function">pg\_fetch\_array</span>
-   <span class="function">pg\_fetch\_object</span>
-   <span class="function">pg\_fetch\_result</span>

pg\_field\_is\_null
===================

测试字段是否为 **`NULL`**

### 说明

<span class="type">int</span> <span
class="methodname">pg\_field\_is\_null</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span> `$row`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$field`</span> )

<span class="function">pg\_field\_is\_null</span> 测试字段是否为
**`NULL`**。如果字段在给出的行中为 **`NULL`** 则返回
1，如果字段在给出的行中不是 **`NULL`** 则返回
0。字段可以以列的索引号（数字）方式给出，也可以以字段名（字符串）方式给出。行的编号从
0 开始。

**示例 \#1 <span class="function">pg\_field\_is\_null</span> 例子**

``` php
<?php
    $dbconn = pg_connect("dbname=publisher") or die ("Could not connect");
    $res = pg_query($dbconn, "select * from authors where author = 'Orwell'");
    if ($res) {
        if (pg_field_is_null($res, 0, "year") == 1) {
            echo "The value of the field year is null.\n";
        }
        if (pg_field_is_null($res, 0, "year") == 0) {
            echo "The value of the field year is not null.\n";
      }
   }
?>
```

> **Note**:
>
> 本函数以前的名字为 *pg\_fieldisnull()*。

pg\_field\_name
===============

返回字段的名字

### 说明

<span class="type">string</span> <span
class="methodname">pg\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_number`</span> )

<span class="function">pg\_field\_name</span> 返回给定 PostgreSQL
`result` 资源中的 `field_number` 所代表的字段名。字段编号从 0 开始。

**示例 \#1 获取字段信息**

``` php
<?php
    $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
    $res = pg_query($dbconn, "select * from authors where author = 'Orwell'");
    $i = pg_num_fields($res);
    for ($j = 0; $j < $i; $j++) {
        echo "column $j\n";
        $fieldname = pg_field_name($res, $j);
        echo "fieldname: $fieldname\n";
        echo "printed length: ".pg_field_prtlen($res, $fieldname)." characters\n";
        echo "storage length: ".pg_field_size($res, $j)." bytes\n";
        echo "field type: ".pg_field_type($res, $j)." \n\n";
}
?>
```

上例的输出如下：

    column 0
    fieldname: author
    printed length: 6 characters
    storage length: -1 bytes
    field type: varchar

    column 1
    fieldname: year
    printed length: 4 characters
    storage length: 2 bytes
    field type: int2

    column 2
    fieldname: title
    printed length: 24 characters
    storage length: -1 bytes
    field type: varchar

> **Note**:
>
> 本函数以前的名字为 *pg\_fieldname()*。

参见 <span class="function">pg\_field\_num</span>。

pg\_field\_num
==============

返回字段的编号

### 说明

<span class="type">int</span> <span
class="methodname">pg\_field\_num</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">string</span>
`$field_name`</span> )

<span class="function">pg\_field\_num</span> 返回给定 PostgreSQL
`result` 资源中的 `field_name` 所代表的列（字段）的编号。字段编号从 0
开始。如果出错本函数返回 -1。

例子参见 <span class="function">pg\_field\_name</span> 页。

> **Note**:
>
> 本函数以前的名字为 *pg\_fieldnum()*。

参见 <span class="function">pg\_field\_name</span>。

pg\_field\_prtlen
=================

返回打印出来的长度

### 说明

<span class="type">int</span> <span
class="methodname">pg\_field\_prtlen</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$row_number`</span> , <span class="methodparam"><span
class="type">string</span> `$field_name`</span> )

<span class="function">pg\_field\_prtlen</span> 返回 PostgreSQL `result`
中得到的值实际上打印出来的长度（字符数）。行编号从 0
开始。如果出错本函数返回 -1。

例子参见 <span class="function">pg\_field\_name</span> 页。

> **Note**:
>
> 本函数以前的名字为 *pg\_field\_prtlen()*。

参见 <span class="function">pg\_field\_size</span>。

pg\_field\_size
===============

返回指定字段占用内部存储空间的大小

### 说明

<span class="type">int</span> <span
class="methodname">pg\_field\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_number`</span> )

<span class="function">pg\_field\_size</span> 返回 PostgreSQL `result`
中指定字段占用内部存储空间的大小（字节数）。字段编号从 0
开始。字段大小为 -1 表示可变长度字段。如果出错本函数返回 **`FALSE`**。

参考 <span class="function">pg\_field\_name</span> 页面中的例子。

> **Note**:
>
> 本函数以前的名字为 *pg\_fieldsize()*。

参见 <span class="function">pg\_field\_prtlen</span> 和 <span
class="function">pg\_field\_type</span>。

pg\_field\_table
================

Returns the name or oid of the tables field

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_field\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_number`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$oid_only`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="function">pg\_field\_table</span> returns the name of the
table that field belongs to, or the table's oid if `oid_only` is
**`TRUE`**.

### 参数

`result`  
PostgreSQL query result resource, returned by <span
class="function">pg\_query</span>, <span
class="function">pg\_query\_params</span> or <span
class="function">pg\_execute</span> (among others).

`field_number`  
Field number, starting from 0.

`oid_only`  
By default the tables name that field belongs to is returned but if
`oid_only` is set to **`TRUE`**, then the oid will instead be returned.

### 返回值

On success either the fields table name or oid. Or, **`FALSE`** on
failure.

### 范例

**示例 \#1 Getting table information about a field**

``` php
<?php
$dbconn = pg_connect("dbname=publisher") or die("Could not connect");

$res = pg_query($dbconn, "SELECT bar FROM foo");

echo pg_field_table($res, 0);
echo pg_field_table($res, 0, true);

$res = pg_query($dbconn, "SELECT version()");
var_dump(pg_field_table($res, 0));
?>
```

以上例程的输出类似于：

    foo
    14379580

    bool(false)

### 注释

> **Note**:
>
> Returning the oid is much faster than returning the table name because
> fetching the table name requires a query to the database system table.

### 参见

-   <span class="function">pg\_field\_name</span>
-   <span class="function">pg\_field\_type</span>

pg\_field\_type\_oid
====================

Returns the type ID (OID) for the corresponding field number

### 说明

<span class="type">int</span> <span
class="methodname">pg\_field\_type\_oid</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_number`</span> )

<span class="function">pg\_field\_type\_oid</span> returns an integer
containing the OID of the base type of the given `field_number` in the
given PostgreSQL `result` resource.

You can get more information about the field type by querying
PostgreSQL's *pg\_type* system table using the OID obtained with this
function. The PostgreSQL <span class="function">format\_type</span>
function will convert a type OID into an SQL standard type name.

> **Note**:
>
> If the field uses a PostgreSQL domain (rather than a basic type), it
> is the OID of the domain's underlying type that is returned, rather
> than the OID of the domain itself.

### 参数

`result`  
PostgreSQL query result resource, returned by <span
class="function">pg\_query</span>, <span
class="function">pg\_query\_params</span> or <span
class="function">pg\_execute</span> (among others).

`field_number`  
Field number, starting from 0.

### 返回值

The OID of the field's base type. **`FALSE`** is returned on error.

### 范例

**示例 \#1 Getting information about fields**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Assume 'title' is a varchar type
  $res = pg_query($dbconn, "select title from authors where author = 'Orwell'");

  echo "Title field type OID: ", pg_field_type_oid($res, 0);
?>
```

以上例程会输出：

    Title field type OID: 1043

### 参见

-   <span class="function">pg\_field\_type</span>
-   <span class="function">pg\_field\_prtlen</span>
-   <span class="function">pg\_field\_name</span>

pg\_field\_type
===============

返回相应字段的类型名称

### 说明

<span class="type">string</span> <span
class="methodname">pg\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_number`</span> )

<span class="function">pg\_field\_type</span> 以字符串返回 PostgreSQL
`result` 资源中指定 `field_number` 字段的类型。字段编号从 0 开始。

参考 <span class="function">pg\_field\_name</span> 页面中的例子。

> **Note**:
>
> 本函数以前的名字为 *pg\_fieldtype()*。

参见 <span class="function">pg\_field\_prtlen</span> 和 <span
class="function">pg\_field\_name</span>。

pg\_flush
=========

刷新链接中已处理的数据查询

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_flush</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

<span class="function">pg\_flush</span>
刷新任何已经处理的等待发送到链接的数据查询。

### 参数

`connection`  
PostgreSQL 数据库链接资源

### 返回值

如果刷新成功或者没有数据等待刷新返回 **`TRUE`** ， 如果返回 *0*
为部分刷新或者更多未被刷新,刷新失败为 **`FALSE`**

pg\_free\_result
================

释放查询结果占用的内存

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_free\_result</span>
仅在当你担心脚本执行时占用了过多内存时调用。脚本执行完毕后所有的查询结果占用的内存都会被自动释放。不过如果你确认在脚本中不会再用到查询结果了，你可以用
`result` 作为参数调用 <span class="function">pg\_free\_result</span>
来释放有关的内存。成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

> **Note**:
>
> 本函数以前的名字为 *pg\_freeresult()*。

参见 <span class="function">pg\_query</span>。

### 参数

`result`  
PostgreSQL query result resource, returned by <span
class="function">pg\_query</span>, <span
class="function">pg\_query\_params</span> or <span
class="function">pg\_execute</span> (among others).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_free\_result</span> example**

``` php
<?php
$db = pg_connect("dbname=users user=me") || die();

$res = pg_query($db, "SELECT 1 UNION ALL SELECT 2");

$val = pg_fetch_result($res, 1, 0);

echo "First field in the second row is: ", $val, "\n";

pg_free_result($res);
?>
```

以上例程会输出：

    First field in the second row is: 2

### 参见

-   <span class="function">pg\_query</span>
-   <span class="function">pg\_query\_params</span>
-   <span class="function">pg\_execute</span>

pg\_get\_notify
===============

Ping 数据库连接

### 说明

<span class="type">array</span> <span
class="methodname">pg\_get\_notify</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \[, <span class="methodparam"><span
class="type">int</span> `$result_type`</span> \] )

<span class="function">pg\_get\_notify</span> 取得 SQL 命令 *NOTIFY*
发送的通告消息。要接收通告消息，必须发送 SQL 命令
*LISTEN*。如果连接中有通告消息，则数组包含消息名并且返回后端的
PID。如果没有消息则返回 **`FALSE`**。

参见 <span class="function">pg\_get\_pid</span>。

**示例 \#1 PostgreSQL NOTIFY 消息**

``` php
<?php 
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "An error occured.\n";
    exit;
}

// Listen 'author_updated' message from other processes
pq_query($conn, 'LISTEN author_updated;');
$notify = pg_get_notify($conn);
if (!$notify)
    print("No messages\n");
else
    print_r($notify);
?>
```

pg\_get\_pid
============

Ping 数据库连接

### 说明

<span class="type">int</span> <span
class="methodname">pg\_get\_pid</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

<span class="function">pg\_get\_pid</span>
取得后端（数据库服务器进程）的 PID。PID 用来检查其它进程是否发送了
*NOTIFY* 消息。

**示例 \#1 PostgreSQL 后端 PID**

``` php
<?php 
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "An error occured.\n";
    exit;
}

// Backend process PID. Use PID with pg_get_notify()
$pid = pg_get_pid($conn);
?>
```

参见 <span class="function">pg\_get\_notify</span>。

pg\_get\_result
===============

取得异步查询结果

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_get\_result</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_get\_result</span> 取得执行 <span
class="function">pg\_send\_query</span> 而得到的查询结果资源。<span
class="function">pg\_send\_query</span> 可以向 PostgreSQL 发送多个查询，
<span class="function">pg\_get\_result</span>
则用来逐个得到查询结果。返回值为查询结果资源号。如果没有更多查询结果，则返回
**`FALSE`**。

pg\_host
========

返回和某连接关联的主机名

### 说明

<span class="type">string</span> <span
class="methodname">pg\_host</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

<span class="function">pg\_host</span> 返回指定的 PostgreSQL
`connection` 资源号所连接到的主机名称。

参见 <span class="function">pg\_connect</span> 和 <span
class="function">pg\_pconnect</span>。

pg\_insert
==========

将数组插入到表中

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_insert</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">array</span> `$assoc_array`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = PGSQL\_DML\_EXEC</span></span> \] )

<span class="function">pg\_insert</span> 将 `assoc_array`
数组中的值插入到由 `table_name` 指定的表中。 如果给出了参数 `options`
，则函数 <span class="function">pg\_convert</span>
会按照给定选项被作用到 `assoc_array` 上

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`connection`  
PostgreSQL database connection resource.

`table_name`  
Name of the table into which to insert rows. `table_name`
中的列必须至少要有 *assoc\_array* 中的单元那么多。

`assoc_array`  
*table\_name* 中的字段名以及字段值必须和 <span class="type">array</span>
参数 中的键名及值匹配。

`options`  
Any number of **`PGSQL_CONV_OPTS`**, **`PGSQL_DML_NO_CONV`**,
**`PGSQL_DML_EXEC`**, **`PGSQL_DML_ASYNC`** or **`PGSQL_DML_STRING`**
combined. If **`PGSQL_DML_STRING`** is part of the `options` then query
string is returned.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Returns <span
class="type">string</span> if **`PGSQL_DML_STRING`** is passed via
`options`.

### 范例

**示例 \#1 <span class="function">pg\_insert</span> example**

``` php
<?php 
  $dbconn = pg_connect('dbname=foo');
  // This is safe, since $_POST is converted automatically
  $res = pg_insert($dbconn, 'post_log', $_POST);
  if ($res) {
      echo "POST data is successfully logged\n";
  } else {
      echo "User must have sent wrong inputs\n";
  }
?>
```

### 参见

-   <span class="function">pg\_convert</span>

pg\_last\_error
===============

得到某连接的最后一条错误信息

### 说明

<span class="type">string</span> <span
class="methodname">pg\_last\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_last\_error</span> 返回指定连接 `connection`
的最后一条错误信息。

错误信息可能会被 PostgreSQL(libpq) 的内部函数调用所覆盖。如果 PostgreSQL
的内部模块函数产生了多个错误，则可能不能返回适当的错误信息。

使用 <span class="function">pg\_result\_error</span>，<span
class="function">pg\_result\_status</span> 和 <span
class="function">pg\_connection\_status</span> 来取得更好的错误处理。

> **Note**:
>
> 本函数以前的名字为 *pg\_errormessage()*。

参见 <span class="function">pg\_result\_error</span>。

pg\_last\_notice
================

返回 PostgreSQL 服务器最新一条公告信息

### 说明

<span class="type">string</span> <span
class="methodname">pg\_last\_notice</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_last\_notice</span> 返回由 `connection`
指定的 PostgreSQL 服务器最新的一条公告信息。PostgreSQL
服务器在某些情况下会发送公告信息，例如在表里创建 *SERIAL* 列。

有了 <span
class="function">pg\_last\_notice</span>，只要检查公告是否和该事务有关，就可以避免提交无用的查询。

可以通过在 `php.ini` 中把 *pgsql.ignore\_notice* 置为 1
来使公告信息追踪成为可选项。

可以通过在 `php.ini` 中把 *pgsql.log\_notice* 置为 0
来使公告信息日志成为可选项。 除非 *pgsql.ignore\_notice* 为
0，否则公告信息不能被日志记录。

### 参数

`connection`  
PostgreSQL database connection resource.

### 返回值

A <span class="type">string</span> containing the last notice on the
given `connection`, or **`FALSE`** on error.

### 更新日志

| 版本  | 说明                                                                                                                                                |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.3.0 | 本函数在 PHP 4.3.0 中完全实现。低于 PHP 4.3.0 的版本中都忽略了数据库连接参数。                                                                      |
| 4.3.0 | The *pgsql.ignore\_notice* and *pgsql.log\_notice* `php.ini` directives were added.                                                                 |
| 4.0.6 | PHP 4.0.6 本身在公告信息处理上有问题。即使不使用 <span class="function">pg\_last\_notice</span> 函数，也不推荐在 PHP 4.0.6 中使用 PostgreSQL 模块。 |

### 范例

**示例 \#1 <span class="function">pg\_last\_notice</span> example**

``` php
<?php
  $pgsql_conn = pg_connect("dbname=mark host=localhost");
  
  $res = pg_query("CREATE TABLE test (id SERIAL)");
  
  $notice = pg_last_notice($pgsql_conn);
  
  echo $notice;
?>
```

以上例程会输出：

    CREATE TABLE will create implicit sequence "test_id_seq" for "serial" column "test.id"

### 参见

-   <span class="function">pg\_query</span>
-   <span class="function">pg\_last\_error</span>

pg\_last\_oid
=============

返回上一个对象的 oid

### 说明

<span class="type">int</span> <span
class="methodname">pg\_last\_oid</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_last\_oid</span> 在上一条通过 <span
class="function">pg\_query</span> 发送的命令是 SQL INSERT
的情况下用来取得分配给所插入记录的 `oid`。如果存在有效的 `oid`
则返回一个正整数，如果出错或者上一条通过 <span
class="function">pg\_query</span> 发送的命令不是 INSERT 或者该 INSERT
失败则返回 **`FALSE`**。

从 PostgreSQL 7.2 版开始 OID 字段成为可选项。如果一个表中没有定义 OID
字段，程序员必须用 <span class="function">pg\_result\_status</span>
函数来检查记录是否被成功插入。

> **Note**:
>
> 本函数以前的名字为 *pg\_getlastoid()*。

参见 <span class="function">pg\_query</span> 和 <span
class="function">pg\_result\_status</span>。

pg\_lo\_close
=============

关闭一个大型对象

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_lo\_close</span> ( <span
class="methodparam"><span class="type">resource</span>
`$large_object`</span> )

<span class="function">pg\_lo\_close</span> 关闭一个大型对象。参数
`large_object` 是 <span class="function">pg\_lo\_open</span>
函数所返回的资源号。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_loclose()*。

参见 <span class="function">pg\_lo\_open</span>，<span
class="function">pg\_lo\_create</span> 和 <span
class="function">pg\_lo\_import</span>。

pg\_lo\_create
==============

新建一个大型对象

### 说明

<span class="type">int</span> <span
class="methodname">pg\_lo\_create</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_lo\_create</span>
新建一个大型对象并返回该大型对象的 `oid`。`connection` 指定了由 <span
class="function">pg\_connect</span> 或 <span
class="function">pg\_pconnect</span> 打开的有效的数据库连接号。不支持
PostgreSQL 访问模式 INV\_READ，INV\_WRITE 和
INV\_ARCHIVE，该对象总是以读写方式访问。INV\_ARCHIVE 已经从 PostgreSQL
中删除了（6.3 及以上版本）。本函数返回大型对象的 oid，如果出错则返回
**`FALSE`**。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_locreate()*。

pg\_lo\_export
==============

将大型对象导出到文件

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_lo\_export</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">int</span> `$oid`</span> , <span class="methodparam"><span
class="type">string</span> `$pathname`</span> )

<span class="function">pg\_lo\_export</span> takes a large object in a
PostgreSQL database and saves its contents to a file on the local
filesystem.

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_loexport()*。

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`oid`  
要导出的数据库里的大型对象的 `OID`。

`pathname`  
要导出的数据库里的大型对象的文件在客户端上完整路径和文件名。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_lo\_export</span> example**

``` php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_create($database);
   $handle = pg_lo_open($database, $oid, "w");
   pg_lo_write($handle, "large object data");
   pg_lo_close($handle);
   pg_lo_export($database, $oid, '/tmp/lob.dat');
   pg_query($database, "commit");
?>
```

### 参见

-   <span class="function">pg\_lo\_import</span>

pg\_lo\_import
==============

将文件导入为大型对象

### 说明

<span class="type">int</span> <span
class="methodname">pg\_lo\_import</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$pathname`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$object_id`</span>
\] )

<span class="function">pg\_lo\_import</span> creates a new large object
in the database using a file on the filesystem as its data source.

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**: <span class="simpara">当启用
> <a href="/features/safe-mode.html" class="link">安全模式</a>时， PHP
> 会检查被操作的文件或目录是否与被执行的脚本有相同的
> UID（所有者）。</span>

> **Note**:
>
> 本函数以前的名字为 <span class="function">pg\_loimport</span>。

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`pathname`  
变量指明了要导入为大型对象的文件名。

`object_id`  
If an `object_id` is given the function will try to create a large
object with this id, else a free object id is assigned by the server.
The parameter was added in PHP 5.3 and relies on functionality that
first appeared in PostgreSQL 8.1.

### 返回值

导入成功则返回新建的大型对象的 `OID`，如果出错则返回 **`FALSE`**。

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>5.3.0</td>
<td><p>The optional <code class="parameter">object_id</code> was added.</p></td>
</tr>
<tr class="even">
<td>4.2.0</td>
<td><p>在 PHP 4.2.0 版本之前，本函数语法不一样，见如下定义：</p>
<div class="methodsynopsis dc-description">
<span class="type">int</span> <span class="methodname">pg_lo_import</span> ( <span class="methodparam"><span class="type">string</span> <code class="parameter">$pathname</code></span> [, <span class="methodparam"><span class="type">resource</span> <code class="parameter">$connection</code></span> ] )
</div></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">pg\_lo\_import</span> 例子**

``` php
<?php
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $oid = pg_lo_import($database, '/tmp/lob.dat');
   pg_query($database, "commit");
?>
```

### 参见

-   <span class="function">pg\_lo\_export</span>
-   <span class="function">pg\_lo\_open</span>

pg\_lo\_open
============

打开一个大型对象

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_lo\_open</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">int</span> `$oid`</span> , <span
class="methodparam"><span class="type">string</span> `$mode`</span> )

<span class="function">pg\_lo\_open</span>
打开一个大型对象并返回大型对象资源号。该资源号内封装了连接号。`oid`
指定了有效的大型对象的 oid，`mode` 可以为 "r"，"w" 或者
"rw"。如果失败则返回 **`FALSE`**。

**Warning**

在关闭大型对象资源之前不要关闭数据库连接。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_loopen()*。

参见 <span class="function">pg\_lo\_close</span> 和 <span
class="function">pg\_lo\_create</span>。

pg\_lo\_read\_all
=================

读入整个大型对象并直接发送给浏览器

### 说明

<span class="type">int</span> <span
class="methodname">pg\_lo\_read\_all</span> ( <span
class="methodparam"><span class="type">resource</span>
`$large_object`</span> )

<span class="function">pg\_lo\_read\_all</span>
读入一个大型对象并在（PHP）发送完所有待发的 header
之后将其直接发送给浏览器。主要目的是发送图片或声音等二进制数据。返回值为读入的字节数，如果出错则返回
**`FALSE`**。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_loreadall()*。

参见 <span class="function">pg\_lo\_read</span>。

pg\_lo\_read
============

从大型对象中读入数据

### 说明

<span class="type">string</span> <span
class="methodname">pg\_lo\_read</span> ( <span class="methodparam"><span
class="type">resource</span> `$large_object`</span> , <span
class="methodparam"><span class="type">int</span> `$len`</span> )

<span class="function">pg\_lo\_read</span> 从大型对象中读入最多 `len`
字节的数据并以字符串返回。`large_object`
指定了有效的大型对象的资源号，`len`
则指定了大型对象的段所允许的最大长度。如果出错则返回 **`FALSE`**。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_loread()*。

参见 <span class="function">pg\_lo\_read\_all</span>。

pg\_lo\_seek
============

移动大型对象中的指针

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_lo\_seek</span> ( <span class="methodparam"><span
class="type">resource</span> `$large_object`</span> , <span
class="methodparam"><span class="type">int</span> `$offset`</span> \[,
<span class="methodparam"><span class="type">int</span> `$whence`</span>
\] )

<span class="function">pg\_lo\_seek</span>
在大型对象资源中移动指针位置。`whence` 参数为
PGSQL\_SEEK\_SET，PGSQL\_SEEK\_CUR 或 PGSQL\_SEEK\_END。

参见 <span class="function">pg\_lo\_tell</span>。

pg\_lo\_tell
============

返回大型对象的当前指针位置

### 说明

<span class="type">int</span> <span
class="methodname">pg\_lo\_tell</span> ( <span class="methodparam"><span
class="type">resource</span> `$large_object`</span> )

<span class="function">pg\_lo\_tell</span>
返回当前指针位置（大型对象中从头开始的偏移量）。

参见 <span class="function">pg\_lo\_seek</span>。

pg\_lo\_truncate
================

Truncates a large object

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_lo\_truncate</span> ( <span
class="methodparam"><span class="type">resource</span>
`$large_object`</span> , <span class="methodparam"><span
class="type">int</span> `$size`</span> )

<span class="function">pg\_lo\_truncate</span> truncates a large object
resource.

To use the large object interface, it is necessary to enclose it within
a transaction block.

### 参数

`large_object`  
PostgreSQL large object (LOB) resource, returned by <span
class="function">pg\_lo\_open</span>.

`size`  
The number of bytes to truncate.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_lo\_truncate</span> example**

``` php
<?php
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   $handle = pg_lo_open($database, $doc_oid, "r");
   // Truncate to 0
   pg_lo_truncate($handle, 0);
   pg_query($database, "commit");
   echo $data;
?>
```

### 更新日志

| 版本  | 说明                                                                                                                                                                                |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | Added truncate function. It supports PostgreSQL 9.3's 64bit large object. Both client and server must support PostgreSQL 9.3 and PHP must be 64bit build to use 64bit large object. |

### 参见

-   <span class="function">pg\_lo\_tell</span>

pg\_lo\_unlink
==============

删除一个大型对象

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_lo\_unlink</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">int</span> `$oid`</span> )

<span class="function">pg\_lo\_unlink</span> 删除由 `oid`
指定的大型对象。成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_lo\_unlink()*。

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`oid`  
The `OID` of the large object in the database.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_lo\_unlink</span> example**

``` php
<?php
   // OID of the large object to delete
   $doc_oid = 189762345;
   $database = pg_connect("dbname=jacarta");
   pg_query($database, "begin");
   pg_lo_unlink($database, $doc_oid);
   pg_query($database, "commit");
?>
```

### 参见

-   <span class="function">pg\_lo\_create</span>
-   <span class="function">pg\_lo\_import</span>

pg\_lo\_write
=============

向大型对象写入数据

### 说明

<span class="type">int</span> <span
class="methodname">pg\_lo\_write</span> ( <span
class="methodparam"><span class="type">resource</span>
`$large_object`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="function">pg\_lo\_write</span> 把 `data`
参数中的数据尽可能多地写入大型对象并返回实际写入的字节数。如果出错则返回
**`FALSE`**。`large_object` 参数是 <span
class="function">pg\_lo\_open</span> 函数所返回的大型对象资源号。

要使用大型对象（lo）接口，需要将其放置在事务块中。

> **Note**:
>
> 本函数以前的名字为 *pg\_lo\_write()*。

参见 <span class="function">pg\_lo\_create</span> 和 <span
class="function">pg\_lo\_open</span>。

pg\_meta\_data
==============

获得表的元数据

### 说明

<span class="type">array</span> <span
class="methodname">pg\_meta\_data</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$table_name`</span> )

<span class="function">pg\_metadata</span> 以数组形式返回 *table\_name*
表的定义。

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`connection`  
PostgreSQL database connection resource.

`table_name`  
The name of the table.

### 返回值

以数组 <span class="type">array</span> 形式返回表的定义，如果出错则返回
**`FALSE`**。

### 范例

**示例 \#1 取得表的元数据**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  $meta = pg_meta_data($dbconn, 'authors');
  if (is_array($meta)) {
      echo '<pre>';
      var_dump($meta);
      echo '</pre>';
  }
?>
```

以上例程会输出：

    array(3) {
    ["author"]=>
    array(5) {
      ["num"]=>
      int(1)
      ["type"]=>
      string(7) "varchar"
      ["len"]=>
      int(-1)
      ["not null"]=>
      bool(false)
      ["has default"]=>
      bool(false)
    }
    ["year"]=>
    array(5) {
      ["num"]=>
      int(2)
      ["type"]=>
      string(4) "int2"
      ["len"]=>
      int(2)
      ["not null"]=>
      bool(false)
      ["has default"]=>
      bool(false)
    }
    ["title"]=>
    array(5) {
      ["num"]=>
      int(3)
      ["type"]=>
      string(7) "varchar"
      ["len"]=>
      int(-1)
      ["not null"]=>
      bool(false)
      ["has default"]=>
      bool(false)
    }
    }

### 参见

-   <span class="function">pg\_convert</span>

pg\_num\_fields
===============

返回字段的数目

### 说明

<span class="type">int</span> <span
class="methodname">pg\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_num\_fields</span> 返回 PostgreSQL `result`
中的字段（列）数目。参数是由 <span class="function">pg\_query</span>
函数返回的查询结果资源号。如果出错则返回 -1。

> **Note**:
>
> 本函数以前的名字为 *pg\_numfields()*。

参见 <span class="function">pg\_num\_rows</span> 和 <span
class="function">pg\_affected\_rows</span>。

pg\_num\_rows
=============

返回行的数目

### 说明

<span class="type">int</span> <span
class="methodname">pg\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_num\_rows</span> 返回 PostgreSQL `result`
中的行的数目。`result` 参数是由 <span class="function">pg\_query</span>
函数返回的查询结果资源号。如果出错则返回 -1。

> **Note**:
>
> 用 <span class="function">pg\_affected\_rows</span> 函数获得被
> INSERT，UPDATE 和 DELETE 命令影响到的行的数目。

> **Note**:
>
> 本函数以前的名字为 *pg\_numrows()*。

参见 <span class="function">pg\_num\_fields</span> 和 <span
class="function">pg\_affected\_rows</span>。

pg\_options
===========

获得和连接有关的选项

### 说明

<span class="type">string</span> <span
class="methodname">pg\_options</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

<span class="function">pg\_options</span> 以字符串形式返回指定
PostgreSQL `connection` 资源的连接选项。

pg\_parameter\_status
=====================

Looks up a current parameter setting of the server

### 说明

<span class="type">string</span> <span
class="methodname">pg\_parameter\_status</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$param_name`</span> )

Looks up a current parameter setting of the server.

Certain parameter values are reported by the server automatically at
connection startup or whenever their values change. <span
class="function">pg\_parameter\_status</span> can be used to interrogate
these settings. It returns the current value of a parameter if known, or
**`FALSE`** if the parameter is not known.

Parameters reported as of PostgreSQL 8.0 include *server\_version*,
*server\_encoding*, *client\_encoding*, *is\_superuser*,
*session\_authorization*, *DateStyle*, *TimeZone*, and
*integer\_datetimes*. (*server\_encoding*, *TimeZone*, and
*integer\_datetimes* were not reported by releases before 8.0.) Note
that *server\_version*, *server\_encoding* and *integer\_datetimes*
cannot change after PostgreSQL startup.

PostgreSQL 7.3 or lower servers do not report parameter settings, <span
class="function">pg\_parameter\_status</span> includes logic to obtain
values for *server\_version* and *client\_encoding* anyway. Applications
are encouraged to use <span
class="function">pg\_parameter\_status</span> rather than ad hoc code to
determine these values.

**Caution**

On a pre-7.4 PostgreSQL server, changing *client\_encoding* via *SET*
after connection startup will not be reflected by <span
class="function">pg\_parameter\_status</span>.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`param_name`  
Possible `param_name` values include *server\_version*,
*server\_encoding*, *client\_encoding*, *is\_superuser*,
*session\_authorization*, *DateStyle*, *TimeZone*, and
*integer\_datetimes*. Note that this value is case-sensitive.

### 返回值

A <span class="type">string</span> containing the value of the
parameter, **`FALSE`** on failure or invalid `param_name`.

### 范例

**示例 \#1 <span class="function">pg\_parameter\_status</span> example**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  echo "Server encoding: ", pg_parameter_status($dbconn, "server_encoding");
?>
```

以上例程会输出：

    Server encoding: SQL_ASCII

pg\_pconnect
============

打开一个持久的 PostgreSQL 连接

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_pconnect</span> ( <span class="methodparam"><span
class="type">string</span> `$connection_string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$connect_type`</span>
\] )

<span class="function">pg\_pconnect</span> 打开一个到 PostgreSQL
数据库的持久连接。返回其它 PostgreSQL 函数所需要的连接资源号。

If a second call is made to <span class="function">pg\_pconnect</span>
with the same `connection_string` as an existing connection, the
existing connection will be returned unless you pass
**`PGSQL_CONNECT_FORCE_NEW`** as `connect_type`.

要打开持久连接功能，`php.ini` 中的
<a href="/book/pgsql.html#" class="link">pgsql.allow_persistent</a>
参数必须为 "On"（也是默认值）。 最大持久连接数目由 `php.ini` 中的
<a href="/book/pgsql.html#" class="link">pgsql.max_persistent</a>
参数定义（默认为 -1 表示没有限制）。所有连接的数目可由 `php.ini` 中的
<a href="/book/pgsql.html#" class="link">pgsql.max_links</a> 参数设置。

<span class="function">pg\_close</span> 不能关闭由 <span
class="function">pg\_pconnect</span> 打开的持久连接。

### 参数

`connection_string`  
The `connection_string` can be empty to use all default parameters, or
it can contain one or more parameter settings separated by whitespace.
Each parameter setting is in the form *keyword = value*. Spaces around
the equal sign are optional. To write an empty value or a value
containing spaces, surround it with single quotes, e.g., *keyword = 'a
value'*. Single quotes and backslashes within the value must be escaped
with a backslash, i.e., \\' and \\.

The currently recognized parameter keywords are: `host`, `hostaddr`,
`port`, `dbname`, `user`, `password`, `connect_timeout`, `options`,
`tty` (ignored), `sslmode`, `requiressl` (deprecated in favor of
`sslmode`), and `service`. Which of these arguments exist depends on
your PostgreSQL version.

`connect_type`  
If **`PGSQL_CONNECT_FORCE_NEW`** is passed, then a new connection is
created, even if the `connection_string` is identical to an existing
connection.

### 返回值

PostgreSQL connection resource on success, **`FALSE`** on failure.

### 范例

**示例 \#1 Using <span class="function">pg\_pconnect</span>**

``` php
<?php
$dbconn = pg_pconnect("dbname=mary");
//connect to a database named "mary"

$dbconn2 = pg_pconnect("host=localhost port=5432 dbname=mary");
// connect to a database named "mary" on "localhost" at port "5432"

$dbconn3 = pg_pconnect("host=sheep port=5432 dbname=mary user=lamb password=foo");
//connect to a database named "mary" on the host "sheep" with a username and password

$conn_string = "host=sheep port=5432 dbname=test user=lamb password=bar";
$dbconn4 = pg_pconnect($conn_string);
//connect to a database named "test" on the host "sheep" with a username and password
?>
```

### 参见

-   <span class="function">pg\_connect</span>
-   <a href="/features/persistent-connections.html" class="link">持久数据库连接</a>

pg\_ping
========

Ping 数据库连接

### 说明

<span class="type">bool</span> <span class="methodname">pg\_ping</span>
( <span class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_ping</span> ping
数据库连接，如果中断则尝试重新连接。如果连接在活动状态返回
**`TRUE`**，否则返回 **`FALSE`**。

**示例 \#1 <span class="function">pg\_ping</span>**

``` php
<?php 
$conn = pg_pconnect ("dbname=publisher");
if (!$conn) {
    echo "An error occured.\n";
    exit;
}

if (!pg_ping($conn))
    die("Connection is broken\n");
?>
```

参见 <span class="function">pg\_connection\_status</span> 和 <span
class="function">pg\_connection\_reset</span>。

pg\_port
========

返回该连接的端口号

### 说明

<span class="type">int</span> <span class="methodname">pg\_port</span> (
<span class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_port</span> 返回给定的 PostgreSQL
`connection` 资源所连接的端口号。

pg\_prepare
===========

Submits a request to create a prepared statement with the given
parameters, and waits for completion

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_prepare</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$stmtname`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> )

<span class="function">pg\_prepare</span> creates a prepared statement
for later execution with <span class="function">pg\_execute</span> or
<span class="function">pg\_send\_execute</span>. This feature allows
commands that will be used repeatedly to be parsed and planned just
once, rather than each time they are executed. <span
class="function">pg\_prepare</span> is supported only against PostgreSQL
7.4 or higher connections; it will fail when using earlier versions.

The function creates a prepared statement named `stmtname` from the
`query` string, which must contain a single SQL command. `stmtname` may
be "" to create an unnamed statement, in which case any pre-existing
unnamed statement is automatically replaced; otherwise it is an error if
the statement name is already defined in the current session. If any
parameters are used, they are referred to in the `query` as $1, $2, etc.

Prepared statements for use with <span
class="function">pg\_prepare</span> can also be created by executing SQL
*PREPARE* statements. (But <span class="function">pg\_prepare</span> is
more flexible since it does not require parameter types to be
pre-specified.) Also, although there is no PHP function for deleting a
prepared statement, the SQL *DEALLOCATE* statement can be used for that
purpose.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`stmtname`  
The name to give the prepared statement. Must be unique per-connection.
If "" is specified, then an unnamed statement is created, overwriting
any previously defined unnamed statement.

`query`  
The parameterized SQL statement. Must contain only a single statement.
(multiple statements separated by semi-colons are not allowed.) If any
parameters are used, they are referred to as $1, $2, etc.

### 返回值

A query result resource on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Using <span class="function">pg\_prepare</span>**

``` php
<?php
// Connect to a database named "mary"
$dbconn = pg_connect("dbname=mary");

// Prepare a query for execution
$result = pg_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');

// Execute the prepared query.  Note that it is not necessary to escape
// the string "Joe's Widgets" in any way
$result = pg_execute($dbconn, "my_query", array("Joe's Widgets"));

// Execute the same prepared query, this time with a different parameter
$result = pg_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));

?>
```

### 参见

-   <span class="function">pg\_execute</span>
-   <span class="function">pg\_send\_execute</span>

pg\_put\_line
=============

向 PostgreSQL 后端发送以 NULL 结尾的字符串

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_put\_line</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="function">pg\_put\_line</span> 向 PostgreSQL
后端服务器发送以 NULL 结尾的字符串。例如可以通过 PostgreSQL 的 *COPY*
操作来向表中高速插入数据。结尾的 NULL 字符会自动加入。

*COPY* is a high-speed data loading interface supported by PostgreSQL.
Data is passed in without being parsed, and in a single transaction.

An alternative to using raw <span class="function">pg\_put\_line</span>
commands is to use <span class="function">pg\_copy\_from</span>. This is
a far simpler interface.

> **Note**:
>
> 应用程序必须明确地在 <span class="function">pg\_end\_copy</span>
> 之前最后一行发送两个字符 "\\." 来向后端指明发送数据结束。

**Warning**

Use of the <span class="function">pg\_put\_line</span> causes most large
object operations, including <span class="function">pg\_lo\_read</span>
and <span class="function">pg\_lo\_tell</span>, to subsequently fail.
You can use <span class="function">pg\_copy\_from</span> and <span
class="function">pg\_copy\_to</span> instead.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`data`  
A line of text to be sent directly to the PostgreSQL backend. A *NULL*
terminator is added automatically.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pg\_put\_line</span> 例子**

``` php
<?php 
  $conn = pg_pconnect("dbname=foo");
  pg_query($conn, "create table bar (a int4, b char(16), d float8)");
  pg_query($conn, "copy bar from stdin");
  pg_put_line($conn, "3\thello world\t4.5\n");
  pg_put_line($conn, "4\tgoodbye world\t7.11\n");
  pg_put_line($conn, "\.\n");
  pg_end_copy($conn);
?>
```

### 参见

-   <span class="function">pg\_end\_copy</span>

pg\_query\_params
=================

Submits a command to the server and waits for the result, with the
ability to pass parameters separately from the SQL command text

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_query\_params</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$query`</span> , <span
class="methodparam"><span class="type">array</span> `$params`</span> )

Submits a command to the server and waits for the result, with the
ability to pass parameters separately from the SQL command text.

<span class="function">pg\_query\_params</span> is like <span
class="function">pg\_query</span>, but offers additional functionality:
parameter values can be specified separately from the command string
proper. <span class="function">pg\_query\_params</span> is supported
only against PostgreSQL 7.4 or higher connections; it will fail when
using earlier versions.

If parameters are used, they are referred to in the `query` string as
$1, $2, etc. The same parameter may appear more than once in the
`query`; the same value will be used in that case. `params` specifies
the actual values of the parameters. A **`NULL`** value in this array
means the corresponding parameter is SQL *NULL*.

The primary advantage of <span class="function">pg\_query\_params</span>
over <span class="function">pg\_query</span> is that parameter values
may be separated from the `query` string, thus avoiding the need for
tedious and error-prone quoting and escaping. Unlike <span
class="function">pg\_query</span>, <span
class="function">pg\_query\_params</span> allows at most one SQL command
in the given string. (There can be semicolons in it, but not more than
one nonempty command.)

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`query`  
The parameterized SQL statement. Must contain only a single statement.
(multiple statements separated by semi-colons are not allowed.) If any
parameters are used, they are referred to as $1, $2, etc.

User-supplied values should always be passed as parameters, not
interpolated into the query string, where they form possible
<a href="/security/database/sql-injection.html" class="link">SQL injection</a>
attack vectors and introduce bugs when handling data containing quotes.
If for some reason you cannot use a parameter, ensure that interpolated
values are
<a href="/book/pgsql.html#pg_escape_string" class="link">properly escaped</a>.

`params`  
An array of parameter values to substitute for the $1, $2, etc.
placeholders in the original prepared query string. The number of
elements in the array must match the number of placeholders.

Values intended for *bytea* fields are not supported as parameters. Use
<span class="function">pg\_escape\_bytea</span> instead, or use the
large object functions.

### 返回值

A query result resource on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Using <span class="function">pg\_query\_params</span>**

``` php
<?php
// Connect to a database named "mary"
$dbconn = pg_connect("dbname=mary");

// Find all shops named Joe's Widgets.  Note that it is not necessary to
// escape "Joe's Widgets"
$result = pg_query_params($dbconn, 'SELECT * FROM shops WHERE name = $1', array("Joe's Widgets"));

// Compare against just using pg_query
$str = pg_escape_string("Joe's Widgets");
$result = pg_query($dbconn, "SELECT * FROM shops WHERE name = '{$str}'");

?>
```

### 参见

-   <span class="function">pg\_query</span>

pg\_query
=========

执行查询

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_query</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> )

<span class="function">pg\_query</span>
在查询可以执行时返回查询结果资源号。如果查询失败或者提供的连接号无效则返回
**`FALSE`**。如果连接号有效，则可以用 <span
class="function">pg\_last\_error</span> 函数来提取详细的错误信息。<span
class="function">pg\_query</span> 发送一条 SQL 语句到 `connection`
资源指定的 PostgreSQL 数据库。`connection` 必须是由 <span
class="function">pg\_connect</span> 或 <span
class="function">pg\_pconnect</span>
返回的合法连接号。本函数返回值是一个其它 PostgreSQL 函数例如 <span
class="function">pg\_fetch\_array</span>
可以用来访问查询结果的查询结果资源号。

> **Note**: <span class="simpara"> `connection` 是 <span
> class="function">pg\_query</span> 中的可选参数。如果没有指定
> `connection`，则使用默认连接。默认连接是 <span
> class="function">pg\_connect</span> 或 <span
> class="function">pg\_pconnect</span> 所打开的最后一个连接。 </span>
> <span class="simpara"> 尽管 `connection`
> 参数可以省略，但不推荐这样做。因为这样可能会导致很难发现脚本中的错误。
> </span>

> **Note**:
>
> 本函数以前的名字为 *pg\_exec()*。*pg\_exec()*
> 函数为了兼容性的原因仍然可以使用，但是鼓励用户使用新的名字。

参见 <span class="function">pg\_connect</span>，<span
class="function">pg\_pconnect</span>，<span
class="function">pg\_fetch\_array</span>，<span
class="function">pg\_fetch\_object</span>，<span
class="function">pg\_num\_rows</span> 和 <span
class="function">pg\_affected\_rows</span>。

pg\_result\_error\_field
========================

Returns an individual field of an error report

### 说明

<span class="type">string</span> <span
class="methodname">pg\_result\_error\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$fieldcode`</span> )

<span class="function">pg\_result\_error\_field</span> returns one of
the detailed error message fields associated with `result` resource. It
is only available against a PostgreSQL 7.4 or above server. The error
field is specified by the `fieldcode`.

Because <span class="function">pg\_query</span> and <span
class="function">pg\_query\_params</span> return **`FALSE`** if the
query fails, you must use <span class="function">pg\_send\_query</span>
and <span class="function">pg\_get\_result</span> to get the result
handle.

If you need to get additional error information from failed <span
class="function">pg\_query</span> queries, use <span
class="function">pg\_set\_error\_verbosity</span> and <span
class="function">pg\_last\_error</span> and then parse the result.

### 参数

`result`  
A PostgreSQL query result resource from a previously executed statement.

`fieldcode`  
Possible `fieldcode` values are: **`PGSQL_DIAG_SEVERITY`**,
**`PGSQL_DIAG_SQLSTATE`**, **`PGSQL_DIAG_MESSAGE_PRIMARY`**,
**`PGSQL_DIAG_MESSAGE_DETAIL`**, **`PGSQL_DIAG_MESSAGE_HINT`**,
**`PGSQL_DIAG_STATEMENT_POSITION`**, **`PGSQL_DIAG_INTERNAL_POSITION`**
(PostgreSQL 8.0+ only), **`PGSQL_DIAG_INTERNAL_QUERY`** (PostgreSQL 8.0+
only), **`PGSQL_DIAG_CONTEXT`**, **`PGSQL_DIAG_SOURCE_FILE`**,
**`PGSQL_DIAG_SOURCE_LINE`** or **`PGSQL_DIAG_SOURCE_FUNCTION`**.

### 返回值

A <span class="type">string</span> containing the contents of the error
field, **`NULL`** if the field does not exist or **`FALSE`** on failure.

### 范例

**示例 \#1 <span class="function">pg\_result\_error\_field</span>
example**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }
  
  $res1 = pg_get_result($dbconn);
  echo pg_result_error_field($res1, PGSQL_DIAG_SQLSTATE);
?>
```

### 参见

-   <span class="function">pg\_result\_error</span>

pg\_result\_error
=================

获得查询结果的错误信息

### 说明

<span class="type">string</span> <span
class="methodname">pg\_result\_error</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_result\_error</span> 返回和 `result`
资源关联的错误信息。因此用户更有机会可以得到比 <span
class="function">pg\_last\_error</span> 更好的错误信息。

参见 <span class="function">pg\_query</span>，<span
class="function">pg\_send\_query</span>，<span
class="function">pg\_get\_result</span>，<span
class="function">pg\_last\_error</span> 和 <span
class="function">pg\_last\_notice</span>。

pg\_result\_seek
================

在结果资源中设定内部行偏移量

### 说明

<span class="type">array</span> <span
class="methodname">pg\_result\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$offset`</span> )

<span class="function">pg\_result\_seek</span>
在结果资源中设定内部行偏移量。如果出错则返回 **`FALSE`**。

参见 <span class="function">pg\_fetch\_row</span>，<span
class="function">pg\_fetch\_assoc</span>，<span
class="function">pg\_fetch\_array</span>，<span
class="function">pg\_fetch\_object</span> 和 <span
class="function">pg\_fetch\_result</span>。

pg\_result\_status
==================

获得查询结果的状态

### 说明

<span class="type">int</span> <span
class="methodname">pg\_result\_status</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">pg\_result\_status</span>
返回该查询结果资源的状态。可能的返回值有
PGSQL\_EMPTY\_QUERY，PGSQL\_COMMAND\_OK，PGSQL\_TUPLES\_OK，PGSQL\_COPY\_TO，PGSQL\_COPY\_FROM，PGSQL\_BAD\_RESPONSE，PGSQL\_NONFATAL\_ERROR
和 PGSQL\_FATAL\_ERROR。

参见 <span class="function">pg\_connection\_status</span>。

pg\_select
==========

选择记录

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_select</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">array</span> `$assoc_array`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = PGSQL\_DML\_EXEC</span></span> \] )

<span class="function">pg\_select</span> 根据 *assoc\_array* 数组中的
*field=\>value* 值来选择记录。成功的查询返回和 *assoc\_array*
指定的条件相匹配的包括记录和字段的数组。

如果指定了 *options*，<span class="function">pg\_convert</span>
会按照指定选项作用于 *assoc\_array* 之上。

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`connection`  
PostgreSQL 数据库连接资源。

`table_name`  
Name of the table from which to select rows.

`assoc_array`  
An <span class="type">array</span> whose keys are field names in the
table `table_name`, and whose values are the conditions that a row must
meet to be retrieved.

`options`  
Any number of **`PGSQL_CONV_FORCE_NULL`**, **`PGSQL_DML_NO_CONV`**,
**`PGSQL_DML_EXEC`**, **`PGSQL_DML_ASYNC`** or **`PGSQL_DML_STRING`**
combined. If **`PGSQL_DML_STRING`** is part of the `options` then query
string is returned.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Returns <span
class="type">string</span> if **`PGSQL_DML_STRING`** is passed via
`options`.

### 范例

**示例 \#1 <span class="function">pg\_select</span> example**

``` php
<?php 
  $db = pg_connect('dbname=foo');
  // This is safe, since $_POST is converted automatically
  $rec = pg_select($db, 'post_log', $_POST);
  if ($rec) {
      echo "Records selected\n";
      var_dump($rec);
  } else {
      echo "User must have sent wrong inputs\n";
  }
?>
```

### 参见

-   <span class="function">pg\_convert</span>

pg\_send\_execute
=================

Sends a request to execute a prepared statement with given parameters,
without waiting for the result(s)

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_send\_execute</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$stmtname`</span> , <span
class="methodparam"><span class="type">array</span> `$params`</span> )

Sends a request to execute a prepared statement with given parameters,
without waiting for the result(s).

This is similar to <span
class="function">pg\_send\_query\_params</span>, but the command to be
executed is specified by naming a previously-prepared statement, instead
of giving a query string. The function's parameters are handled
identically to <span class="function">pg\_execute</span>. Like <span
class="function">pg\_execute</span>, it will not work on pre-7.4
versions of PostgreSQL.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`stmtname`  
The name of the prepared statement to execute. if "" is specified, then
the unnamed statement is executed. The name must have been previously
prepared using <span class="function">pg\_prepare</span>, <span
class="function">pg\_send\_prepare</span> or a *PREPARE* SQL command.

`params`  
An array of parameter values to substitute for the $1, $2, etc.
placeholders in the original prepared query string. The number of
elements in the array must match the number of placeholders.

### 返回值

Returns **`TRUE`** on success, **`FALSE`** on failure. Use <span
class="function">pg\_get\_result</span> to determine the query result.

### 范例

**示例 \#1 Using <span class="function">pg\_send\_execute</span>**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Prepare a query for execution
  if (!pg_connection_busy($dbconn)) {
    pg_send_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');
    $res1 = pg_get_result($dbconn);
  }

  // Execute the prepared query.  Note that it is not necessary to escape
  // the string "Joe's Widgets" in any way
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Joe's Widgets"));
    $res2 = pg_get_result($dbconn);
  }
  
  // Execute the same prepared query, this time with a different parameter
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));
    $res3 = pg_get_result($dbconn);
  }
  
?>
```

### 参见

-   <span class="function">pg\_prepare</span>
-   <span class="function">pg\_send\_prepare</span>
-   <span class="function">pg\_execute</span>

pg\_send\_prepare
=================

Sends a request to create a prepared statement with the given
parameters, without waiting for completion

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_send\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$stmtname`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> )

Sends a request to create a prepared statement with the given
parameters, without waiting for completion.

This is an asynchronous version of <span
class="function">pg\_prepare</span>: it returns **`TRUE`** if it was
able to dispatch the request, and **`FALSE`** if not. After a successful
call, call <span class="function">pg\_get\_result</span> to determine
whether the server successfully created the prepared statement. The
function's parameters are handled identically to <span
class="function">pg\_prepare</span>. Like <span
class="function">pg\_prepare</span>, it will not work on pre-7.4
versions of PostgreSQL.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`stmtname`  
The name to give the prepared statement. Must be unique per-connection.
If "" is specified, then an unnamed statement is created, overwriting
any previously defined unnamed statement.

`query`  
The parameterized SQL statement. Must contain only a single statement.
(multiple statements separated by semi-colons are not allowed.) If any
parameters are used, they are referred to as $1, $2, etc.

### 返回值

Returns **`TRUE`** on success, **`FALSE`** on failure. Use <span
class="function">pg\_get\_result</span> to determine the query result.

### 范例

**示例 \#1 Using <span class="function">pg\_send\_prepare</span>**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Prepare a query for execution
  if (!pg_connection_busy($dbconn)) {
    pg_send_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');
    $res1 = pg_get_result($dbconn);
  }

  // Execute the prepared query.  Note that it is not necessary to escape
  // the string "Joe's Widgets" in any way
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Joe's Widgets"));
    $res2 = pg_get_result($dbconn);
  }
  
  // Execute the same prepared query, this time with a different parameter
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));
    $res3 = pg_get_result($dbconn);
  }
  
?>
```

### 参见

-   <span class="function">pg\_connect</span>
-   <span class="function">pg\_pconnect</span>
-   <span class="function">pg\_execute</span>
-   <span class="function">pg\_send\_execute</span>
-   <span class="function">pg\_send\_query\_params</span>

pg\_send\_query\_params
=======================

Submits a command and separate parameters to the server without waiting
for the result(s)

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_send\_query\_params</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$query`</span> , <span
class="methodparam"><span class="type">array</span> `$params`</span> )

Submits a command and separate parameters to the server without waiting
for the result(s).

This is equivalent to <span class="function">pg\_send\_query</span>
except that query parameters can be specified separately from the
`query` string. The function's parameters are handled identically to
<span class="function">pg\_query\_params</span>. Like <span
class="function">pg\_query\_params</span>, it will not work on pre-7.4
PostgreSQL connections, and it allows only one command in the query
string.

### 参数

`connection`  
PostgreSQL database connection resource.

`query`  
The parameterized SQL statement. Must contain only a single statement.
(multiple statements separated by semi-colons are not allowed.) If any
parameters are used, they are referred to as $1, $2, etc.

`params`  
An array of parameter values to substitute for the $1, $2, etc.
placeholders in the original prepared query string. The number of
elements in the array must match the number of placeholders.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

Use <span class="function">pg\_get\_result</span> to determine the query
result.

### 范例

**示例 \#1 Using <span class="function">pg\_send\_query\_params</span>**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Using parameters.  Note that it is not necessary to quote or escape
  // the parameter.
  pg_send_query_params($dbconn, 'select count(*) from authors where city = $1', array('Perth'));
  
  // Compare against basic pg_send_query usage
  $str = pg_escape_string('Perth');
  pg_send_query($dbconn, "select count(*) from authors where city = '${str}'");
?>
```

### 参见

-   <span class="function">pg\_send\_query</span>

pg\_send\_query
===============

发送异步查询

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_send\_query</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$query`</span> )

<span class="type">bool</span> <span
class="methodname">pg\_send\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )

<span class="function">pg\_send\_query</span> 向 `connection`
连接发送异步查询。和 <span class="function">pg\_query</span>
不同，它可以向 PostgreSQL 发送多个查询并用 <span
class="function">pg\_get\_result</span>
依次得到结果。当执行查询时脚本的执行不会被锁定。用 <span
class="function">pg\_connection\_busy</span>
来检查连接连接是否为忙（即查询正在执行中）。调用 <span
class="function">pg\_cancel\_query</span> 则有可能取消查询。

尽管用户可以一次发送多个查询，但用户不能通过正忙的连接发送多个查询。如果向正忙的连接发送了查询，则会等待上一条查询结束并丢弃所有结果。

**示例 \#1 异步查询**

``` php
<?php
    $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
    if (!pg_connection_busy($dbconn)) {
        pg_send_query($dbconn,"select * from authors; select count(*) from authors;");
    }
    $res1 = pg_get_result($dbconn);
    echo "First call to pg_get_result(): $res1\n";
    $rows1 = pg_num_rows($res1);
    echo "$res1 has $rows1 records\n\n";
    $res2 = pg_get_result($dbconn);
    echo "second call to pg_get_result(): $res2\n";
    $rows2 = pg_num_rows($res2);
    echo "$res2 has $rows2 records\n";
?>
```

上例输出如下：

    first call to pg_get_result(): Resource id #3
    Resource id #3 has 3 records

    second call to pg_get_result(): Resource id #4
    Resource id #4 has 1 records

参见 <span class="function">pg\_query</span>，<span
class="function">pg\_cancel\_query</span>，<span
class="function">pg\_get\_result</span> 和 <span
class="function">pg\_connection\_busy</span>。

pg\_set\_client\_encoding
=========================

设定客户端编码

### 说明

<span class="type">int</span> <span
class="methodname">pg\_set\_client\_encoding</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">string</span> `$encoding`</span> )

<span class="function">pg\_set\_client\_encoding</span>
设定客户端编码方式，成功返回 0，出错返回 -1。

`encoding`
是客户端的编码方式，可以为：SQL\_ASCII，EUC\_JP，EUC\_CN，EUC\_KR，EUC\_TW，UNICODE，MULE\_INTERNAL，LATINX
(X=1...9)，KOI8，WIN，ALT，SJIS，BIG5，WIN1250。可用的编码取决于
PostgreSQL 和 libpq 的版本。参考 PostgreSQL 手册查看你的 PostgreSQL
所支持的编码方式。

> **Note**:
>
> 本函数需要 PHP 4.0.3 或以上版本以及 PostgreSQL 7.0
> 或以上版本。所支持的编码方式取决于 PostgreSQL 的版本，详情参考
> PostgreSQL 手册。
>
> 本函数以前的名字为 <span
> class="function">pg\_setclientencoding</span>。

参见 <span class="function">pg\_client\_encoding</span>。

pg\_set\_error\_verbosity
=========================

Determines the verbosity of messages returned by <span
class="function">pg\_last\_error</span> and <span
class="function">pg\_result\_error</span>

### 说明

<span class="type">int</span> <span
class="methodname">pg\_set\_error\_verbosity</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \], <span class="methodparam"><span
class="type">int</span> `$verbosity`</span> )

Determines the verbosity of messages returned by <span
class="function">pg\_last\_error</span> and <span
class="function">pg\_result\_error</span>.

<span class="function">pg\_set\_error\_verbosity</span> sets the
verbosity mode, returning the connection's previous setting. In
**`PGSQL_ERRORS_TERSE`** mode, returned messages include severity,
primary text, and position only; this will normally fit on a single
line. The default mode (**`PGSQL_ERRORS_DEFAULT`**) produces messages
that include the above plus any detail, hint, or context fields (these
may span multiple lines). The **`PGSQL_ERRORS_VERBOSE`** mode includes
all available fields. Changing the verbosity does not affect the
messages available from already-existing result objects, only
subsequently-created ones.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

`verbosity`  
The required verbosity: **`PGSQL_ERRORS_TERSE`**,
**`PGSQL_ERRORS_DEFAULT`** or **`PGSQL_ERRORS_VERBOSE`**.

### 返回值

The previous verbosity level: **`PGSQL_ERRORS_TERSE`**,
**`PGSQL_ERRORS_DEFAULT`** or **`PGSQL_ERRORS_VERBOSE`**.

### 范例

**示例 \#1 <span class="function">pg\_set\_error\_verbosity</span>
example**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }
  
  pg_set_error_verbosity($dbconn, PGSQL_ERRORS_VERBOSE);
  $res1 = pg_get_result($dbconn);
  echo pg_result_error($res1);
?>
```

### 参见

-   <span class="function">pg\_last\_error</span>
-   <span class="function">pg\_result\_error</span>

pg\_socket
==========

Get a read only handle to the socket underlying a PostgreSQL connection

### 说明

<span class="type">resource</span> <span
class="methodname">pg\_socket</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

<span class="function">pg\_socket</span> returns a read only <span
class="type">resource</span> corresponding to the socket underlying the
given PostgreSQL connection.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`connection`  
PostgreSQL database connection resource.

### 返回值

A socket resource on success 或者在失败时返回 **`FALSE`**.

pg\_trace
=========

启动一个 PostgreSQL 连接的追踪功能

### 说明

<span class="type">bool</span> <span class="methodname">pg\_trace</span>
( <span class="methodparam"><span class="type">string</span>
`$pathname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \]\] )

<span class="function">pg\_trace</span> 启动 PostgreSQL
前端／后端通讯的追踪并记录到 `pathname`
指定的文件中。要完全理解结果，用户需要熟悉 PostgreSQL
通讯协议的本质。对不熟悉的用户来说，追踪发送到服务器的查询错误依然有用，例如可以用
**grep '^To backend' trace.log** 来查看哪些查询实际上被发送到了
PostgreSQL 服务器。更多信息参考 PostgreSQL 手册。

参数 `pathname` 和 `mode` 和 <span class="function">fopen</span>(`mode`
默认为 'w') 中的一样。`connection`
指定了要追踪的连接，默认为上一个打开的连接。

如果 `pathname` 可以作为日志文件打开，则 <span
class="function">pg\_trace</span> 返回 **`TRUE`**，否则返回
**`FALSE`**。

参见 <span class="function">fopen</span> 和 <span
class="function">pg\_untrace</span>。

pg\_transaction\_status
=======================

Returns the current in-transaction status of the server

### 说明

<span class="type">int</span> <span
class="methodname">pg\_transaction\_status</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> )

Returns the current in-transaction status of the server.

**Caution**

<span class="function">pg\_transaction\_status</span> will give
incorrect results when using a PostgreSQL 7.3 server that has the
parameter *autocommit* set to off. The server-side autocommit feature
has been deprecated and does not exist in later server versions.

### 参数

`connection`  
PostgreSQL database connection resource.

### 返回值

The status can be **`PGSQL_TRANSACTION_IDLE`** (currently idle),
**`PGSQL_TRANSACTION_ACTIVE`** (a command is in progress),
**`PGSQL_TRANSACTION_INTRANS`** (idle, in a valid transaction block), or
**`PGSQL_TRANSACTION_INERROR`** (idle, in a failed transaction block).
**`PGSQL_TRANSACTION_UNKNOWN`** is reported if the connection is bad.
**`PGSQL_TRANSACTION_ACTIVE`** is reported only when a query has been
sent to the server and not yet completed.

### 范例

**示例 \#1 <span class="function">pg\_transaction\_status</span>
example**

``` php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");
  $stat = pg_transaction_status($dbconn);
  if ($stat === PGSQL_TRANSACTION_UNKNOWN) {
      echo 'Connection is bad';
  } else if ($stat === PGSQL_TRANSACTION_IDLE) {
      echo 'Connection is currently idle';
  } else {
      echo 'Connection is in a transaction state';
  }    
?>
```

pg\_tty
=======

返回该连接的 tty 号

### 说明

<span class="type">string</span> <span class="methodname">pg\_tty</span>
( <span class="methodparam"><span class="type">resource</span>
`$connection`</span> )

<span class="function">pg\_tty</span> 返回指定 PostgreSQL `connection`
资源在服务器端输出调试信息的 tty 号。

pg\_unescape\_bytea
===================

取消 bytea 类型中的字符串转义

### 说明

<span class="type">string</span> <span
class="methodname">pg\_unescape\_bytea</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">pg\_unescape\_bytea</span> 将 bytea
数据类型中的字符串取消转义。返回未转义的字符串（二进制）。

> **Note**:
>
> 当 SELECT bytea 类型，PostgreSQL 返回用 \\ 前导的八进制字节值（例如
> \\032）。用户需要自行将其转换回二进制格式。
>
> 本函数需要 PostgreSQL 7.2 或更新版本。在 PostgreSQL 7.2.0 和 7.2.1
> 中，当激活了多字节支持时必须强制转换为 bytea 类型，例如 *INSERT INTO
> test\_table (image) VALUES ('$image\_escaped'::bytea);*。PostgreSQL
> 7.2.2
> 或更新版本不需要强制转换。例外是当客户端和后端的字符编码不匹配时，有可能出现多字节流错误。用户必须强制转换为
> bytea 来避免此错误。

参见 <span class="function">pg\_escape\_bytea</span> 和 <span
class="function">pg\_escape\_string</span>。

pg\_untrace
===========

关闭 PostgreSQL 连接的追踪功能

### 说明

<span class="type">bool</span> <span
class="methodname">pg\_untrace</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

停止由 <span class="function">pg\_trace</span>
启动的追踪功能。`connection`
指定了被追踪的连接号，默认为上一个打开的连接。

本函数总是返回 **`TRUE`**。

参见 <span class="function">pg\_trace</span>。

pg\_update
==========

更新表

### 说明

<span class="type">mixed</span> <span
class="methodname">pg\_update</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span>
`$table_name`</span> , <span class="methodparam"><span
class="type">array</span> `$data`</span> , <span
class="methodparam"><span class="type">array</span> `$condition`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = PGSQL\_DML\_EXEC</span></span> \]
)

<span class="function">pg\_update</span> 用 *condition*
作为条件查询数据库，用 *data* 中的数据更新符合条件的记录。如果指定了
*options*，则 <span class="function">pg\_convert</span>
会按照指定选项作用到 *data* 上。

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`connection`  
PostgreSQL database connection resource.

`table_name`  
Name of the table into which to update rows.

`data`  
An <span class="type">array</span> whose keys are field names in the
table `table_name`, and whose values are what matched rows are to be
updated to.

`condition`  
An <span class="type">array</span> whose keys are field names in the
table `table_name`, and whose values are the conditions that a row must
meet to be updated.

`options`  
Any number of **`PGSQL_CONV_OPTS`**, **`PGSQL_DML_NO_CONV`**,
**`PGSQL_DML_EXEC`** or **`PGSQL_DML_STRING`** combined. If
**`PGSQL_DML_STRING`** is part of the `options` then query string is
returned.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Returns <span
class="type">string</span> if **`PGSQL_DML_STRING`** is passed via
`options`.

### 范例

**示例 \#1 <span class="function">pg\_update</span> example**

``` php
<?php 
  $db = pg_connect('dbname=foo');
  $data = array('field1'=>'AA', 'field2'=>'BB');
  
  // This is safe, since $_POST is converted automatically
  $res = pg_update($db, 'post_log', $_POST, $data);
  if ($res) {
      echo "Data is updated: $res\n";
  } else {
      echo "User must have sent wrong inputs\n";
  }
?>
```

### 参见

-   <span class="function">pg\_convert</span>

pg\_version
===========

Returns an array with client, protocol and server version (when
available)

### 说明

<span class="type">array</span> <span
class="methodname">pg\_version</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \] )

<span class="function">pg\_version</span> returns an array with the
client, protocol and server version. Protocol and server versions are
only available if PHP was compiled with PostgreSQL 7.4 or later.

For more detailed server information, use <span
class="function">pg\_parameter\_status</span>.

### 参数

`connection`  
PostgreSQL database connection resource. When `connection` is not
present, the default connection is used. The default connection is the
last connection made by <span class="function">pg\_connect</span> or
<span class="function">pg\_pconnect</span>.

### 返回值

Returns an array with *client*, *protocol* and *server* keys and values
(if available). Returns **`FALSE`** on error or invalid connection.

### 范例

**示例 \#1 <span class="function">pg\_version</span> example**

``` php
<?php
  $dbconn = pg_connect("host=localhost port=5432 dbname=mary")
     or die("Could not connect");
     
  $v = pg_version($dbconn);
  
  echo $v['client'];
?>
```

以上例程会输出：

    7.4

### 参见

-   <span class="function">pg\_parameter\_status</span>

**目录**

-   [pg\_affected\_rows](/book/pgsql.html#pg_affected_rows) —
    返回受影响的记录数目
-   [pg\_cancel\_query](/book/pgsql.html#pg_cancel_query) — 取消异步查询
-   [pg\_client\_encoding](/book/pgsql.html#pg_client_encoding) —
    取得客户端编码方式
-   [pg\_close](/book/pgsql.html#pg_close) — 关闭一个 PostgreSQL 连接
-   [pg\_connect\_poll](/book/pgsql.html#pg_connect_poll) —
    正在进行尝试轮询 PostgreSQL 链接状态。
-   [pg\_connect](/book/pgsql.html#pg_connect) — 打开一个 PostgreSQL
    连接
-   [pg\_connection\_busy](/book/pgsql.html#pg_connection_busy) —
    获知连接是否为忙
-   [pg\_connection\_reset](/book/pgsql.html#pg_connection_reset) —
    重置连接（再次连接）
-   [pg\_connection\_status](/book/pgsql.html#pg_connection_status) —
    获得连接状态
-   [pg\_consume\_input](/book/pgsql.html#pg_consume_input) — Reads
    input on the connection
-   [pg\_convert](/book/pgsql.html#pg_convert) —
    将关联的数组值转换为适合 SQL 语句的格式。
-   [pg\_copy\_from](/book/pgsql.html#pg_copy_from) —
    根据数组将记录插入表中
-   [pg\_copy\_to](/book/pgsql.html#pg_copy_to) — 将一个表拷贝到数组中
-   [pg\_dbname](/book/pgsql.html#pg_dbname) — 获得数据库名
-   [pg\_delete](/book/pgsql.html#pg_delete) — 删除记录
-   [pg\_end\_copy](/book/pgsql.html#pg_end_copy) — 与 PostgreSQL
    后端同步
-   [pg\_escape\_bytea](/book/pgsql.html#pg_escape_bytea) — 转义 bytea
    类型的二进制数据
-   [pg\_escape\_identifier](/book/pgsql.html#pg_escape_identifier) —
    Escape a identifier for insertion into a text field
-   [pg\_escape\_literal](/book/pgsql.html#pg_escape_literal) — Escape a
    literal for insertion into a text field
-   [pg\_escape\_string](/book/pgsql.html#pg_escape_string) — 转义
    text/char 类型的字符串
-   [pg\_execute](/book/pgsql.html#pg_execute) — Sends a request to
    execute a prepared statement with given parameters, and waits for
    the result
-   [pg\_fetch\_all\_columns](/book/pgsql.html#pg_fetch_all_columns) —
    Fetches all rows in a particular result column as an array
-   [pg\_fetch\_all](/book/pgsql.html#pg_fetch_all) —
    从结果中提取所有行作为一个数组
-   [pg\_fetch\_array](/book/pgsql.html#pg_fetch_array) —
    提取一行作为数组
-   [pg\_fetch\_assoc](/book/pgsql.html#pg_fetch_assoc) —
    提取一行作为关联数组
-   [pg\_fetch\_object](/book/pgsql.html#pg_fetch_object) —
    提取一行作为对象
-   [pg\_fetch\_result](/book/pgsql.html#pg_fetch_result) —
    从结果资源中返回值
-   [pg\_fetch\_row](/book/pgsql.html#pg_fetch_row) —
    提取一行作为枚举数组
-   [pg\_field\_is\_null](/book/pgsql.html#pg_field_is_null) —
    测试字段是否为 NULL
-   [pg\_field\_name](/book/pgsql.html#pg_field_name) — 返回字段的名字
-   [pg\_field\_num](/book/pgsql.html#pg_field_num) — 返回字段的编号
-   [pg\_field\_prtlen](/book/pgsql.html#pg_field_prtlen) —
    返回打印出来的长度
-   [pg\_field\_size](/book/pgsql.html#pg_field_size) —
    返回指定字段占用内部存储空间的大小
-   [pg\_field\_table](/book/pgsql.html#pg_field_table) — Returns the
    name or oid of the tables field
-   [pg\_field\_type\_oid](/book/pgsql.html#pg_field_type_oid) — Returns
    the type ID (OID) for the corresponding field number
-   [pg\_field\_type](/book/pgsql.html#pg_field_type) —
    返回相应字段的类型名称
-   [pg\_flush](/book/pgsql.html#pg_flush) — 刷新链接中已处理的数据查询
-   [pg\_free\_result](/book/pgsql.html#pg_free_result) —
    释放查询结果占用的内存
-   [pg\_get\_notify](/book/pgsql.html#pg_get_notify) — Ping 数据库连接
-   [pg\_get\_pid](/book/pgsql.html#pg_get_pid) — Ping 数据库连接
-   [pg\_get\_result](/book/pgsql.html#pg_get_result) — 取得异步查询结果
-   [pg\_host](/book/pgsql.html#pg_host) — 返回和某连接关联的主机名
-   [pg\_insert](/book/pgsql.html#pg_insert) — 将数组插入到表中
-   [pg\_last\_error](/book/pgsql.html#pg_last_error) —
    得到某连接的最后一条错误信息
-   [pg\_last\_notice](/book/pgsql.html#pg_last_notice) — 返回
    PostgreSQL 服务器最新一条公告信息
-   [pg\_last\_oid](/book/pgsql.html#pg_last_oid) — 返回上一个对象的 oid
-   [pg\_lo\_close](/book/pgsql.html#pg_lo_close) — 关闭一个大型对象
-   [pg\_lo\_create](/book/pgsql.html#pg_lo_create) — 新建一个大型对象
-   [pg\_lo\_export](/book/pgsql.html#pg_lo_export) —
    将大型对象导出到文件
-   [pg\_lo\_import](/book/pgsql.html#pg_lo_import) —
    将文件导入为大型对象
-   [pg\_lo\_open](/book/pgsql.html#pg_lo_open) — 打开一个大型对象
-   [pg\_lo\_read\_all](/book/pgsql.html#pg_lo_read_all) —
    读入整个大型对象并直接发送给浏览器
-   [pg\_lo\_read](/book/pgsql.html#pg_lo_read) — 从大型对象中读入数据
-   [pg\_lo\_seek](/book/pgsql.html#pg_lo_seek) — 移动大型对象中的指针
-   [pg\_lo\_tell](/book/pgsql.html#pg_lo_tell) —
    返回大型对象的当前指针位置
-   [pg\_lo\_truncate](/book/pgsql.html#pg_lo_truncate) — Truncates a
    large object
-   [pg\_lo\_unlink](/book/pgsql.html#pg_lo_unlink) — 删除一个大型对象
-   [pg\_lo\_write](/book/pgsql.html#pg_lo_write) — 向大型对象写入数据
-   [pg\_meta\_data](/book/pgsql.html#pg_meta_data) — 获得表的元数据
-   [pg\_num\_fields](/book/pgsql.html#pg_num_fields) — 返回字段的数目
-   [pg\_num\_rows](/book/pgsql.html#pg_num_rows) — 返回行的数目
-   [pg\_options](/book/pgsql.html#pg_options) — 获得和连接有关的选项
-   [pg\_parameter\_status](/book/pgsql.html#pg_parameter_status) —
    Looks up a current parameter setting of the server
-   [pg\_pconnect](/book/pgsql.html#pg_pconnect) — 打开一个持久的
    PostgreSQL 连接
-   [pg\_ping](/book/pgsql.html#pg_ping) — Ping 数据库连接
-   [pg\_port](/book/pgsql.html#pg_port) — 返回该连接的端口号
-   [pg\_prepare](/book/pgsql.html#pg_prepare) — Submits a request to
    create a prepared statement with the given parameters, and waits for
    completion
-   [pg\_put\_line](/book/pgsql.html#pg_put_line) — 向 PostgreSQL
    后端发送以 NULL 结尾的字符串
-   [pg\_query\_params](/book/pgsql.html#pg_query_params) — Submits a
    command to the server and waits for the result, with the ability to
    pass parameters separately from the SQL command text
-   [pg\_query](/book/pgsql.html#pg_query) — 执行查询
-   [pg\_result\_error\_field](/book/pgsql.html#pg_result_error_field) —
    Returns an individual field of an error report
-   [pg\_result\_error](/book/pgsql.html#pg_result_error) —
    获得查询结果的错误信息
-   [pg\_result\_seek](/book/pgsql.html#pg_result_seek) —
    在结果资源中设定内部行偏移量
-   [pg\_result\_status](/book/pgsql.html#pg_result_status) —
    获得查询结果的状态
-   [pg\_select](/book/pgsql.html#pg_select) — 选择记录
-   [pg\_send\_execute](/book/pgsql.html#pg_send_execute) — Sends a
    request to execute a prepared statement with given parameters,
    without waiting for the result(s)
-   [pg\_send\_prepare](/book/pgsql.html#pg_send_prepare) — Sends a
    request to create a prepared statement with the given parameters,
    without waiting for completion
-   [pg\_send\_query\_params](/book/pgsql.html#pg_send_query_params) —
    Submits a command and separate parameters to the server without
    waiting for the result(s)
-   [pg\_send\_query](/book/pgsql.html#pg_send_query) — 发送异步查询
-   [pg\_set\_client\_encoding](/book/pgsql.html#pg_set_client_encoding)
    — 设定客户端编码
-   [pg\_set\_error\_verbosity](/book/pgsql.html#pg_set_error_verbosity)
    — Determines the verbosity of messages returned by pg\_last\_error
    and pg\_result\_error
-   [pg\_socket](/book/pgsql.html#pg_socket) — Get a read only handle to
    the socket underlying a PostgreSQL connection
-   [pg\_trace](/book/pgsql.html#pg_trace) — 启动一个 PostgreSQL
    连接的追踪功能
-   [pg\_transaction\_status](/book/pgsql.html#pg_transaction_status) —
    Returns the current in-transaction status of the server
-   [pg\_tty](/book/pgsql.html#pg_tty) — 返回该连接的 tty 号
-   [pg\_unescape\_bytea](/book/pgsql.html#pg_unescape_bytea) — 取消
    bytea 类型中的字符串转义
-   [pg\_untrace](/book/pgsql.html#pg_untrace) — 关闭 PostgreSQL
    连接的追踪功能
-   [pg\_update](/book/pgsql.html#pg_update) — 更新表
-   [pg\_version](/book/pgsql.html#pg_version) — Returns an array with
    client, protocol and server version (when available)
