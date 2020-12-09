Microsoft SQL Server Driver for PHP
===================================

**目录**

-   [简介](/book/sqlsrv.html#简介)
-   [安装／配置](/book/sqlsrv.html#安装／配置)
    -   [需求](/book/sqlsrv.html#需求)
    -   [安装](/book/sqlsrv.html#安装)
    -   [运行时配置](/book/sqlsrv.html#运行时配置)
    -   [资源类型](/book/sqlsrv.html#资源类型)
-   [预定义常量](/book/sqlsrv.html#预定义常量)
-   [SQLSRV 函数](/book/sqlsrv.html#SQLSRV%20函数)
    -   [sqlsrv\_begin\_transaction](/book/sqlsrv.html#sqlsrv_begin_transaction)
        — Begins a database transaction
    -   [sqlsrv\_cancel](/book/sqlsrv.html#sqlsrv_cancel) — Cancels a
        statement
    -   [sqlsrv\_client\_info](/book/sqlsrv.html#sqlsrv_client_info) —
        Returns information about the client and specified connection
    -   [sqlsrv\_close](/book/sqlsrv.html#sqlsrv_close) — Closes an open
        connection and releases resourses associated with the connection
    -   [sqlsrv\_commit](/book/sqlsrv.html#sqlsrv_commit) — Commits a
        transaction that was begun with sqlsrv\_begin\_transaction
    -   [sqlsrv\_configure](/book/sqlsrv.html#sqlsrv_configure) —
        Changes the driver error handling and logging configurations
    -   [sqlsrv\_connect](/book/sqlsrv.html#sqlsrv_connect) — Opens a
        connection to a Microsoft SQL Server database
    -   [sqlsrv\_errors](/book/sqlsrv.html#sqlsrv_errors) — Returns
        error and warning information about the last SQLSRV operation
        performed
    -   [sqlsrv\_execute](/book/sqlsrv.html#sqlsrv_execute) — Executes a
        statement prepared with sqlsrv\_prepare
    -   [sqlsrv\_fetch\_array](/book/sqlsrv.html#sqlsrv_fetch_array) —
        Returns a row as an array
    -   [sqlsrv\_fetch\_object](/book/sqlsrv.html#sqlsrv_fetch_object) —
        Retrieves the next row of data in a result set as an object
    -   [sqlsrv\_fetch](/book/sqlsrv.html#sqlsrv_fetch) — Makes the next
        row in a result set available for reading
    -   [sqlsrv\_field\_metadata](/book/sqlsrv.html#sqlsrv_field_metadata)
        — Retrieves metadata for the fields of a statement prepared by
        sqlsrv\_prepare or sqlsrv\_query
    -   [sqlsrv\_free\_stmt](/book/sqlsrv.html#sqlsrv_free_stmt) — Frees
        all resources for the specified statement
    -   [sqlsrv\_get\_config](/book/sqlsrv.html#sqlsrv_get_config) —
        Returns the value of the specified configuration setting
    -   [sqlsrv\_get\_field](/book/sqlsrv.html#sqlsrv_get_field) — Gets
        field data from the currently selected row
    -   [sqlsrv\_has\_rows](/book/sqlsrv.html#sqlsrv_has_rows) —
        Indicates whether the specified statement has rows
    -   [sqlsrv\_next\_result](/book/sqlsrv.html#sqlsrv_next_result) —
        Makes the next result of the specified statement active
    -   [sqlsrv\_num\_fields](/book/sqlsrv.html#sqlsrv_num_fields) —
        Retrieves the number of fields (columns) on a statement
    -   [sqlsrv\_num\_rows](/book/sqlsrv.html#sqlsrv_num_rows) —
        Retrieves the number of rows in a result set
    -   [sqlsrv\_prepare](/book/sqlsrv.html#sqlsrv_prepare) — Prepares a
        query for execution
    -   [sqlsrv\_query](/book/sqlsrv.html#sqlsrv_query) — Prepares and
        executes a query
    -   [sqlsrv\_rollback](/book/sqlsrv.html#sqlsrv_rollback) — Rolls
        back a transaction that was begun with
        sqlsrv\_begin\_transaction
    -   [sqlsrv\_rows\_affected](/book/sqlsrv.html#sqlsrv_rows_affected)
        — Returns the number of rows modified by the last INSERT,
        UPDATE, or DELETE query executed
    -   [sqlsrv\_send\_stream\_data](/book/sqlsrv.html#sqlsrv_send_stream_data)
        — Sends data from parameter streams to the server
    -   [sqlsrv\_server\_info](/book/sqlsrv.html#sqlsrv_server_info) —
        Returns information about the server

The SQLSRV extension allows you to access Microsoft SQL Server and SQL
Azure databases. The 3.0 release of the driver supports SQL Server,
beginning with SQL Server 2005, including SQL Server 2012 and SQL Server
2012 LocalDB. (For more information about LocalDB, see
<a href="http://msdn.microsoft.com/en-us/library/hh487161.aspx" class="link external">» PHP Driver for SQL Server Support for LocalDB</a>
and
<a href="http://msdn.microsoft.com/en-us/library/hh510202(SQL.110).aspx" class="link external">» SQL Server 2012 Express LocalDB</a>.)

The SQLSRV extension is supported by Microsoft and available for
download here:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx</a>.
SQL Server 2012 LocalDB can be downloaded here:
<a href="http://go.microsoft.com/fwlink/?LinkID=237665" class="link external">» http://go.microsoft.com/fwlink/?LinkID=237665</a>.

安装／配置
==========

**目录**

-   [需求](/book/sqlsrv.html#需求)
-   [安装](/book/sqlsrv.html#安装)
-   [运行时配置](/book/sqlsrv.html#运行时配置)
-   [资源类型](/book/sqlsrv.html#资源类型)

需求
----

The SQLSRV extension can be used on the following operating systems:

-   Windows Vista Service Pack 2 or later
-   Windows Server 2008 Service Pack 2 or later
-   Windows Server 2008 R2
-   Windows 7

The SQLSRV extension requires that the Microsoft SQL Server 2012 Native
Client be installed on the same computer that is running PHP. If the
Microsoft SQL Server 2012 Native Client is not already installed, click
the appropriate link below to download it:

-   <a href="http://go.microsoft.com/fwlink/?LinkID=239647" class="link external">» Download the x86 package</a>
-   <a href="http://go.microsoft.com/fwlink/?LinkID=239648" class="link external">» Download the x64 package</a>

The SQLSRV download comes 8 driver files, four of which are for PDO
support. If you are running non-thread-safe PHP (PHP 5.3), use the
php\_sqlsrv\_53\_nts.dll file. (You should use a non-thread-safe version
if you are using IIS as your web server). If you are running thread-safe
PHP, use the php\_sqlsrv\_53\_ts.dll file. Similarly for PHP 5.4, use
the php\_sqlsrv\_54\_nts.dll or php\_sqlsrv\_54\_ts.dll depending on
whether your PHP installation is non-thread-safe or thread-safe.

The most recent version of the driver is available for download here:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» SQLSRV 4.0 download</a>.
If you need support for PHP 5.2 and/or PHP compiled with VC6, use the
2.0 release of the driver:
<a href="http://download.microsoft.com/download/C/D/B/CDB0A3BB-600E-42ED-8D5E-E4630C905371/SQLSRV20.EXE" class="link external">» SQLSRV 2.0 download</a>.

For more information about SQLSRV requirements, see
<a href="http://msdn.microsoft.com/en-us/library/cc296170.aspx" class="link external">» SQLSRV System Requirements</a>.

安装
----

The SQLSRV extension is enabled by adding appropriate DLL file to your
PHP extension directory and the corresponding entry to the `php.ini`
file. The SQLSRV download comes 8 driver files, four of which are for
PDO support. If you are running non-thread-safe PHP (PHP 5.3), use the
php\_sqlsrv\_53\_nts.dll file. (You should use a non-thread-safe version
if you are using IIS as your web server). If you are running thread-safe
PHP, use the php\_sqlsrv\_53\_ts.dll file. Similarly for PHP 5.4, use
the php\_sqlsrv\_54\_nts.dll or php\_sqlsrv\_54\_ts.dll depending on
whether your PHP installation is non-thread-safe or thread-safe.

The most recent version of the driver is available for download here:
<a href="http://msdn.microsoft.com/en-us/sqlserver/ff657782.aspx" class="link external">» SQLSRV 4.0 download</a>.
If you need support for PHP 5.2 and/or PHP compiled with VC6, use the
2.0 release of the driver:
<a href="http://download.microsoft.com/download/C/D/B/CDB0A3BB-600E-42ED-8D5E-E4630C905371/SQLSRV20.EXE" class="link external">» SQLSRV 2.0 download</a>.

For more information about SQLSRV requirements, see
<a href="http://msdn.microsoft.com/en-us/library/cc296170.aspx" class="link external">» SQLSRV System Requirements</a>.

The SQLSRV extension is only compatible with PHP 5 running on Windows.
Since version 4.0 the SQLSRV extension is compatilbe only with PHP 7.0
running on Linux or Windows.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

The following table lists the configuration options available in the
SQLSRV extension. For more information about these options, see
<a href="http://msdn.microsoft.com/en-us/library/cc626302.aspx" class="link external">» Handling SQLSRV Warnings and Errors</a>.

| 名字                          | 默认           | 可修改范围    | Changelog                  |
|-------------------------------|----------------|---------------|----------------------------|
| sqlsrv.WarningsReturnAsErrors | 1 (**`true`**) | PHP\_INI\_ALL | Available since SQLSRV 1.0 |
| sqlsrv.LogSubsystems          | 0              | PHP\_INI\_ALL | Available since SQLSRV 1.0 |
| sqlsrv.LogSeverity            | 1              | PHP\_INI\_ALL | Available since SQLSRV 1.0 |

资源类型
--------

Connection resource
-------------------

A connection resource returned by <span
class="function">sqlsrv\_connect</span>.

Statement resource
------------------

A statement resource returned by <span
class="function">sqlsrv\_query</span> or by <span
class="function">sqlsrv\_prepare</span>.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SQLSRV_FETCH_ASSOC`** (<span class="type">int</span>)  
<span class="simpara"> Forces <span
class="function">sqlsrv\_fetch\_array</span> to return an associative
array when passed as a parameter. </span>

**`SQLSRV_FETCH_NUMERIC`** (<span class="type">int</span>)  
<span class="simpara"> Forces <span
class="function">sqlsrv\_fetch\_array</span> to return an array with
numeric when passed as a parameter. </span>

**`SQLSRV_FETCH_BOTH`** (<span class="type">int</span>)  
<span class="simpara"> Forces <span
class="function">sqlsrv\_fetch\_array</span> to return an array with
both associative and numeric keys when passed as a parameter (the
default behavior). </span>

**`SQLSRV_ERR_ALL`** (<span class="type">int</span>)  
<span class="simpara"> Forces <span
class="function">sqlsrv\_errors</span> to return both errors and warings
when passed as a parameter (the default behavior). </span>

**`SQLSRV_ERR_ERRORS`** (<span class="type">int</span>)  
<span class="simpara"> Forces <span
class="function">sqlsrv\_errors</span> to return errors only (no
warnings) when passed as a parameter. </span>

**`SQLSRV_ERR_WARNINGS`** (<span class="type">int</span>)  
<span class="simpara"> Forces <span
class="function">sqlsrv\_errors</span> to return warnings only (no
errors) when passed as a parameter. </span>

**`SQLSRV_LOG_SYSTEM_ALL`** (<span class="type">int</span>)  
<span class="simpara"> Turns on logging of all subsystems when passed to
<span class="function">sqlsrv\_configure</span> as a parameter. </span>

**`SQLSRV_LOG_SYSTEM_CONN`** (<span class="type">int</span>)  
<span class="simpara"> Turns on logging of connection activity when
passed to <span class="function">sqlsrv\_configure</span> as a
parameter. </span>

**`SQLSRV_LOG_SYSTEM_INIT`** (<span class="type">int</span>)  
<span class="simpara"> Turns on logging of initialization activity when
passed to <span class="function">sqlsrv\_configure</span> as a
parameter. </span>

**`SQLSRV_LOG_SYSTEM_OFF`** (<span class="type">int</span>)  
<span class="simpara"> Turns off logging of all subsystems when passed
to <span class="function">sqlsrv\_configure</span> as a parameter.
</span>

**`SQLSRV_LOG_SYSTEM_STMT`** (<span class="type">int</span>)  
<span class="simpara"> Turns on logging of statement activity when
passed to <span class="function">sqlsrv\_configure</span> as a
parameter. </span>

**`SQLSRV_LOG_SYSTEM_UTIL`** (<span class="type">int</span>)  
<span class="simpara"> Turns on logging of error function activity when
passed to <span class="function">sqlsrv\_configure</span> as a
parameter. </span>

**`SQLSRV_LOG_SEVERITY_ALL`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that errors, warnings, and notices will
be logged when passed to <span class="function">sqlsrv\_configure</span>
as a parameter. </span>

**`SQLSRV_LOG_SEVERITY_ERROR`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that errors will be logged when passed
to <span class="function">sqlsrv\_configure</span> as a parameter.
</span>

**`SQLSRV_LOG_SEVERITY_NOTICE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that notices will be logged when passed
to <span class="function">sqlsrv\_configure</span> as a parameter.
</span>

**`SQLSRV_LOG_SEVERITY_WARNING`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that warnings will be logged when
passed to <span class="function">sqlsrv\_configure</span> as a
parameter. </span>

**`SQLSRV_NULLABLE_YES`** (<span class="type">int</span>)  
<span class="simpara"> Indicates that a column is nullable. </span>

**`SQLSRV_NULLABLE_NO`** (<span class="type">int</span>)  
<span class="simpara"> Indicates that a column is not nullable. </span>

**`SQLSRV_NULLABLE_UNKNOWN`** (<span class="type">int</span>)  
<span class="simpara"> Indicates that it is not known if a column is
nullable. </span>

**`SQLSRV_PARAM_IN`** (<span class="type">int</span>)  
<span class="simpara"> Indicates an input parameter when passed to <span
class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_prepare</span>. </span>

**`SQLSRV_PARAM_INOUT`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a bidirectional parameter when passed
to <span class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_prepare</span>. </span>

**`SQLSRV_PARAM_OUT`** (<span class="type">int</span>)  
<span class="simpara"> Indicates an output parameter when passed to
<span class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_prepare</span>. </span>

**`SQLSRV_PHPTYPE_INT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies an integer PHP data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_PHPTYPE_DATETIME`** (<span class="type">int</span>)  
<span class="simpara"> Specifies a datetime PHP data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_PHPTYPE_FLOAT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies a float PHP data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_PHPTYPE_STREAM`** (<span class="type">int</span>)  
<span class="simpara"> Specifies a PHP stream. This constant works like
a function and accepts an encoding constant. See the SQLSRV\_ENC\_\*
constants. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_PHPTYPE_STRING`** (<span class="type">int</span>)  
<span class="simpara"> Specifies a string PHP data type. This constant
works like a function and accepts an encoding constant. See the
SQLSRV\_ENC\_\* constants. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_ENC_BINARY`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that data is returned as a raw byte
stream from the server without performing encoding or translation. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_ENC_CHAR`** (<span class="type">int</span>)  
<span class="simpara"> Data is returned in 8-bit characters as specified
in the code page of the Windows locale that is set on the system. Any
multi-byte characters or characters that do not map into this code page
are substituted with a single byte question mark (?) character. This is
the default encoding. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`UTF-8`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that data is returned with UTF-8
encoding. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296208.aspx" class="link external">» How to: Specify PHP Types</a>.
</span>

**`SQLSRV_SQLTYPE_BIGINT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the bigint SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_BINARY`** (<span class="type">int</span>)  
<span class="simpara"> Describes the binary SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_BIT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the bit SQL Server data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_CHAR`** (<span class="type">int</span>)  
<span class="simpara"> Describes the char SQL Server data type. This
constant works like a function and accepts a parameter indicating the
number characters. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_DATE`** (<span class="type">int</span>)  
<span class="simpara"> Describes the date SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_DATETIME`** (<span class="type">int</span>)  
<span class="simpara"> Describes the datetime SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_DATETIME2`** (<span class="type">int</span>)  
<span class="simpara"> Describes the datetime2 SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_DATETIMEOFFSET`** (<span class="type">int</span>)  
<span class="simpara"> Describes the datetimeoffset SQL Server data
type. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_DECIMAL`** (<span class="type">int</span>)  
<span class="simpara"> Describes the decimal SQL Server data type. This
constant works like a function and accepts two parameters indicating (in
order) precision and scale. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_FLOAT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the float SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_IMAGE`** (<span class="type">int</span>)  
<span class="simpara"> Describes the image SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_INT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the int SQL Server data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_MONEY`** (<span class="type">int</span>)  
<span class="simpara"> Describes the money SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_NCHAR`** (<span class="type">int</span>)  
<span class="simpara"> Describes the nchar SQL Server data type. This
constant works like a function and accepts a single parameter indicating
the character count. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_NUMERIC`** (<span class="type">int</span>)  
<span class="simpara"> Describes the numeric SQL Server data type. This
constant works like a function and accepts two parameter indicating (in
order) precision and scale. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_NVARCHAR`** (<span class="type">int</span>)  
<span class="simpara"> Describes the nvarchar SQL Server data type. This
constant works like a function and accepts a single parameter indicating
the character count. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_NVARCHAR`**('max') (<span class="type">int</span>)  
<span class="simpara"> Describes the nvarchar(MAX) SQL Server data type.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_NTEXT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the ntext SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_REAL`** (<span class="type">int</span>)  
<span class="simpara"> Describes the real SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_SMALLDATETIME`** (<span class="type">int</span>)  
<span class="simpara"> Describes the smalldatetime SQL Server data type.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_SMALLINT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the smallint SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_SMALLMONEY`** (<span class="type">int</span>)  
<span class="simpara"> Describes the smallmoney SQL Server data type.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_TEXT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the text SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_TIME`** (<span class="type">int</span>)  
<span class="simpara"> Describes the time SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_TIMESTAMP`** (<span class="type">int</span>)  
<span class="simpara"> Describes the timestamp SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_TINYINT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the tinyint SQL Server data type. For
usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_UNIQUEIDENTIFIER`** (<span class="type">int</span>)  
<span class="simpara"> Describes the uniqueidentifier SQL Server data
type. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_UDT`** (<span class="type">int</span>)  
<span class="simpara"> Describes the UDT SQL Server data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_VARBINARY`** (<span class="type">int</span>)  
<span class="simpara"> Describes the varbinary SQL Server data type.
This constant works like a function and accepts a single parameter
indicating the byte count. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_VARBINARY`**('max') (<span class="type">int</span>)  
<span class="simpara"> Describes the varbinary(MAX) SQL Server data
type. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_VARCHAR`** (<span class="type">int</span>)  
<span class="simpara"> Describes the varchar SQL Server data type. This
constant works like a function and accepts a single parameter indicating
the character count. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_VARCHAR`**('max') (<span class="type">int</span>)  
<span class="simpara"> Describes the varchar(MAX) SQL Server data type.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_SQLTYPE_XML`** (<span class="type">int</span>)  
<span class="simpara"> Describes the XML SQL Server data type. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/cc626305.aspx" class="link external">» How to: Specify SQL Types</a>.
</span>

**`SQLSRV_TXN_READ_UNCOMMITTED`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a transaction isolation level of READ
UNCOMMITTED. This value is used to set the TransactionIsolation level in
the $connectionOptions array passed to <span
class="function">sqlsrv\_connect</span>. </span>

**`SQLSRV_TXN_READ_COMMITTED`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a transaction isolation level of READ
COMMITTED. This value is used to set the TransactionIsolation level in
the $connectionOptions array passed to <span
class="function">sqlsrv\_connect</span>. </span>

**`SQLSRV_TXN_REPEATABLE_READ`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a transaction isolation level of
REPEATABLE READ. This value is used to set the TransactionIsolation
level in the $connectionOptions array passed to <span
class="function">sqlsrv\_connect</span>. </span>

**`SQLSRV_TXN_SNAPSHOT`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a transaction isolation level of
SNAPSHOT. This value is used to set the TransactionIsolation level in
the $connectionOptions array passed to <span
class="function">sqlsrv\_connect</span>. </span>

**`SQLSRV_TXN_READ_SERIALIZABLE`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a transaction isolation level of
SERIALIZABLE. This value is used to set the TransactionIsolation level
in the $connectionOptions array passed to <span
class="function">sqlsrv\_connect</span>. </span>

**`SQLSRV_CURSOR_FORWARD`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a forward-only cursor. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_CURSOR_STATIC`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a static cursor. For usage information,
see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_CURSOR_DYNAMIC`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a dynamic cursor. For usage
information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_CURSOR_KEYSET`** (<span class="type">int</span>)  
<span class="simpara"> Indicates a keyset cursor. For usage information,
see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_CURSOR_BUFFERED`** (<span class="type">int</span>)  
<span class="simpara"> Creates a client-side cursor query. Lets you
access rows in any order. For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_SCROLL_NEXT`** (<span class="type">int</span>)  
<span class="simpara"> Specifies which row to select in a result set.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_SCROLL_PRIOR`** (<span class="type">int</span>)  
<span class="simpara"> Specifies which row to select in a result set.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_SCROLL_FIRST`** (<span class="type">int</span>)  
<span class="simpara"> Specifies which row to select in a result set.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_SCROLL_LAST`** (<span class="type">int</span>)  
<span class="simpara"> Specifies which row to select in a result set.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_SCROLL_ABSOLUTE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies which row to select in a result set.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

**`SQLSRV_SCROLL_RELATIVE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies which row to select in a result set.
For usage information, see
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>.
</span>

sqlsrv\_begin\_transaction
==========================

Begins a database transaction

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_begin\_transaction</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

The transaction begun by <span
class="function">sqlsrv\_begin\_transaction</span> includes all
statements that were executed after the call to <span
class="function">sqlsrv\_begin\_transaction</span> and before calls to
<span class="function">sqlsrv\_rollback</span> or <span
class="function">sqlsrv\_commit</span>. Explicit transactions should be
started and committed or rolled back using these functions instead of
executing SQL statements that begin and commit/roll back transactions.
For more information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296206.aspx" class="link external">» SQLSRV Transactions</a>.

### 参数

`conn`  
The connection resource returned by a call to <span
class="function">sqlsrv\_connect</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_begin\_transaction</span>
example**

The following example demonstrates how to use <span
class="function">sqlsrv\_begin\_transaction</span> together with <span
class="function">sqlsrv\_commit</span> and <span
class="function">sqlsrv\_rollback</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true ));
}

/* Begin the transaction. */
if ( sqlsrv_begin_transaction( $conn ) === false ) {
     die( print_r( sqlsrv_errors(), true ));
}

/* Initialize parameter values. */
$orderId = 1; $qty = 10; $productId = 100;

/* Set up and execute the first query. */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
          VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Set up and execute the second query. */
$sql2 = "UPDATE InventoryTable 
          SET Quantity = (Quantity - ?) 
          WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* If both queries were successful, commit the transaction. */
/* Otherwise, rollback the transaction. */
if( $stmt1 && $stmt2 ) {
     sqlsrv_commit( $conn );
     echo "Transaction committed.<br />";
} else {
     sqlsrv_rollback( $conn );
     echo "Transaction rolled back.<br />";
}
?>
```

以上例程的输出类似于：

### 参见

-   <span class="function">sqlsrv\_commit</span>
-   <span class="function">sqlsrv\_rollback</span>

sqlsrv\_cancel
==============

Cancels a statement

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_cancel</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Cancels a statement. Any results associated with the statement that have
not been consumed are deleted. After <span
class="function">sqlsrv\_cancel</span> has been called, the specified
statement can be re-executed if it was created with <span
class="function">sqlsrv\_prepare</span>. Calling <span
class="function">sqlsrv\_cancel</span> is not necessary if all the
results associated with the statement have been consumed.

### 参数

`stmt`  
The statement resource to be cancelled.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_cancel</span> example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Sales FROM Table_1";

$stmt = sqlsrv_prepare( $conn, $sql);

if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

if( sqlsrv_execute( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

$salesTotal = 0;
$count = 0;

while( ($row = sqlsrv_fetch_array( $stmt)) && $salesTotal <=100000)
{
     $qty = $row[0];
     $price = $row[1];
     $salesTotal += ( $price * $qty);
     $count++;
}

echo "$count sales accounted for the first $$salesTotal in revenue.<br />";

// Cancel the pending results. The statement can be reused.
sqlsrv_cancel( $stmt);
?>
```

### 注释

The main difference between <span class="function">sqlsrv\_cancel</span>
and <span class="function">sqlsrv\_free\_stmt</span> is that a statement
resource cancelled with <span class="function">sqlsrv\_cancel</span> can
be re-executed if it was created with <span
class="function">sqlsrv\_prepare</span>. A statement resource cancelled
with <span class="function">sqlsrv\_free\_statement</span> cannot be
re-executed.

### 参见

-   <span class="function">sqlsrv\_free\_stmt</span>
-   <span class="function">sqlsrv\_prepare</span>

sqlsrv\_client\_info
====================

Returns information about the client and specified connection

### 说明

<span class="type">array</span> <span
class="methodname">sqlsrv\_client\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

Returns information about the client and specified connection

### 参数

`conn`  
The connection about which information is returned.

### 返回值

Returns an associative array with keys described in the table below.
Returns **`false`** otherwise.

| Key           | Description                                     |
|---------------|-------------------------------------------------|
| DriverDllName | SQLNCLI10.DLL                                   |
| DriverODBCVer | ODBC version (xx.yy)                            |
| DriverVer     | SQL Server Native Client DLL version (10.5.xxx) |
| ExtensionVer  | php\_sqlsrv.dll version (2.0.xxx.x)             |

### 范例

**示例 \#1 <span class="function">sqlsrv\_client\_info</span> example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connOptions = array("UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connOptions );

if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

if( $client_info = sqlsrv_client_info( $conn)) {
    foreach( $client_info as $key => $value) {
        echo $key.": ".$value."<br />";
    }
} else {
    echo "Error in retrieving client info.<br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_server\_info</span>

sqlsrv\_close
=============

Closes an open connection and releases resourses associated with the
connection

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

Closes an open connection and releases resourses associated with the
connection.

### 参数

`conn`  
The connection to be closed.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_close</span> example**

``` php
<?php
$serverName = "serverName\sqlexpres";
$connOptions = array("UID"=>"username", "PWD"=>"password", "Database"=>"dbname");
$conn = sqlsrv_connect( $serverName, $connOptions );
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

//-------------------------------------
// Perform database operations here.
//-------------------------------------

// Close the connection.
sqlsrv_close( $conn );
?>
```

### 参见

-   <span class="function">sqlsrv\_connect</span>

sqlsrv\_commit
==============

Commits a transaction that was begun with <span
class="function">sqlsrv\_begin\_transaction</span>

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_commit</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

Commits a transaction that was begun with <span
class="function">sqlsrv\_begin\_transaction</span>. The connection is
returned to auto-commit mode after <span
class="function">sqlsrv\_commit</span> is called. The transaction that
is committed includes all statements that were executed after the call
to <span class="function">sqlsrv\_begin\_transaction</span>. Explicit
transactions should be started and committed or rolled back using these
functions instead of executing SQL statements that begin and commit/roll
back transactions. For more information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296206.aspx" class="link external">» SQLSRV Transactions</a>.

### 参数

`conn`  
The connection on which the transaction is to be committed.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_commit</span> example**

The following example demonstrates how to use <span
class="function">sqlsrv\_commit</span> together with <span
class="function">sqlsrv\_begin\_transaction</span> and <span
class="function">sqlsrv\_rollback</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true ));
}

/* Begin the transaction. */
if ( sqlsrv_begin_transaction( $conn ) === false ) {
     die( print_r( sqlsrv_errors(), true ));
}

/* Initialize parameter values. */
$orderId = 1; $qty = 10; $productId = 100;

/* Set up and execute the first query. */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
         VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Set up and execute the second query. */
$sql2 = "UPDATE InventoryTable 
         SET Quantity = (Quantity - ?) 
         WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* If both queries were successful, commit the transaction. */
/* Otherwise, rollback the transaction. */
if( $stmt1 && $stmt2 ) {
     sqlsrv_commit( $conn );
     echo "Transaction committed.<br />";
} else {
     sqlsrv_rollback( $conn );
     echo "Transaction rolled back.<br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_begin\_transaction</span>
-   <span class="function">sqlsrv\_rollback</span>

sqlsrv\_configure
=================

Changes the driver error handling and logging configurations

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_configure</span> ( <span
class="methodparam"><span class="type">string</span> `$setting`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Changes the driver error handling and logging configurations.

### 参数

`setting`  
The name of the setting to set. The possible values are
"WarningsReturnAsErrors", "LogSubsystems", and "LogSeverity".

`value`  
The value of the specified setting. The following table shows possible
values:

| Setting                | Options                                                                                                                                                                            |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WarningsReturnAsErrors | 1 (**`true`**) or 0 (**`false`**)                                                                                                                                                  |
| LogSubsystems          | SQLSRV\_LOG\_SYSTEM\_ALL (-1) SQLSRV\_LOG\_SYSTEM\_CONN (2) SQLSRV\_LOG\_SYSTEM\_INIT (1) SQLSRV\_LOG\_SYSTEM\_OFF (0) SQLSRV\_LOG\_SYSTEM\_STMT (4) SQLSRV\_LOG\_SYSTEM\_UTIL (8) |
| LogSeverity            | SQLSRV\_LOG\_SEVERITY\_ALL (-1) SQLSRV\_LOG\_SEVERITY\_ERROR (1) SQLSRV\_LOG\_SEVERITY\_NOTICE (4) SQLSRV\_LOG\_SEVERITY\_WARNING (2)                                              |

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <a href="http://msdn.microsoft.com/en-us/library/cc626302.aspx" class="link external">» SQLSRV Error Handling</a>.
-   <a href="http://msdn.microsoft.com/en-us/library/cc296188.aspx" class="link external">» Logging SQLSRV Activity</a>.

sqlsrv\_connect
===============

Opens a connection to a Microsoft SQL Server database

### 说明

<span class="type">resource</span> <span
class="methodname">sqlsrv\_connect</span> ( <span
class="methodparam"><span class="type">string</span>
`$serverName`</span> \[, <span class="methodparam"><span
class="type">array</span> `$connectionInfo`</span> \] )

Opens a connection to a Microsoft SQL Server database. By default, the
connection is attempted using Windows Authentication. To connect using
SQL Server Authentication, include "UID" and "PWD" in the connection
options array.

### 参数

`serverName`  
The name of the server to which a connection is established. To connect
to a specific instance, follow the server name with a backward slash and
the instance name (e.g. serverName\\sqlexpress).

`connectionInfo`  
An associative array that specifies options for connecting to the
server. If values for the UID and PWD keys are not specified, the
connection will be attempted using Windows Authentication. For a
complete list of supported keys, see
<a href="http://msdn.microsoft.com/en-us/library/ff628167.aspx" class="link external">» SQLSRV Connection Options</a>.

### 返回值

A connection resource. If a connection cannot be successfully opened,
**`false`** is returned.

### 范例

**示例 \#1 Connect using Windows Authentication.**

``` php
<?php
$serverName = "serverName\\sqlexpress"; //serverName\instanceName

// Since UID and PWD are not specified in the $connectionInfo array,
// The connection will be attempted using Windows Authentication.
$connectionInfo = array( "Database"=>"dbName");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

if( $conn ) {
     echo "Connection established.<br />";
}else{
     echo "Connection could not be established.<br />";
     die( print_r( sqlsrv_errors(), true));
}
?>
```

**示例 \#2 Connect by specifying a user name and password.**

``` php
<?php
$serverName = "serverName\\sqlexpress"; //serverName\instanceName
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

if( $conn ) {
     echo "Connection established.<br />";
}else{
     echo "Connection could not be established.<br />";
     die( print_r( sqlsrv_errors(), true));
}
?>
```

**示例 \#3 Connect on a specified port.**

``` php
<?php
$serverName = "serverName\\sqlexpress, 1542"; //serverName\instanceName, portNumber (default is 1433)
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

if( $conn ) {
     echo "Connection established.<br />";
}else{
     echo "Connection could not be established.<br />";
     die( print_r( sqlsrv_errors(), true));
}
?>
```

### 注释

By default, the <span class="function">sqlsrv\_connect</span> uses
connection pooling to improve connection performance. To turn off
connection pooling (i.e. force a new connection on each call), set the
"ConnectionPooling" option in the $connectionOptions array to 0 (or
**`false`**). For more information, see
<a href="http://msdn.microsoft.com/en-us/library/cc644930.aspx" class="link external">» SQLSRV Connection Pooling</a>.

The SQLSRV extension does not have a dedicated function for changing
which database is connected to. The target database is specified in the
$connectionOptions array that is passed to sqlsrv\_connect. To change
the database on an open connection, execute the following query "USE
dbName" (e.g. sqlsrv\_query($conn, "USE dbName")).

### 参见

-   <span class="function">sqlsrv\_close</span>
-   <span class="function">sqlsrv\_errors</span>
-   <span class="function">sqlsrv\_query</span>

sqlsrv\_errors
==============

Returns error and warning information about the last SQLSRV operation
performed

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_errors</span> (\[ <span
class="methodparam"><span class="type">int</span>
`$errorsOrWarnings`</span> \] )

Returns error and warning information about the last SQLSRV operation
performed.

### 参数

`errorsOrWarnings`  
Determines whether error information, warning information, or both are
returned. If this parameter is not supplied, both error information and
warning information are returned. The following are the supported values
for this parameter: SQLSRV\_ERR\_ALL, SQLSRV\_ERR\_ERRORS,
SQLSRV\_ERR\_WARNINGS.

### 返回值

If errors and/or warnings occurred on the last sqlsrv operation, an
array of arrays containing error information is returned. If no errors
and/or warnings occurred on the last sqlsrv operation, **`null`** is
returned. The following table describes the structure of the returned
arrays:

| Key      | Description                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SQLSTATE | For errors that originate from the ODBC driver, the SQLSTATE returned by ODBC. For errors that originate from the Microsoft Drivers for PHP for SQL Server, a SQLSTATE of IMSSP. For warnings that originate from the Microsoft Drivers for PHP for SQL Server, a SQLSTATE of 01SSP.                |
| code     | For errors that originate from SQL Server, the native SQL Server error code. For errors that originate from the ODBC driver, the error code returned by ODBC. For errors that originate from the Microsoft Drivers for PHP for SQL Server, the Microsoft Drivers for PHP for SQL Server error code. |
| message  | A description of the error.                                                                                                                                                                                                                                                                         |

### 范例

**示例 \#1 <span class="function">functionname</span> example**

``` php
<?php
$serverName = "serverName/sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

/* Set up a query to select an invalid column name. */
$sql = "SELECT BadColumnName FROM Table_1";

/* Execution of the query will fail because of the bad column name. */
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false ) {
    if( ($errors = sqlsrv_errors() ) != null) {
        foreach( $errors as $error ) {
            echo "SQLSTATE: ".$error[ 'SQLSTATE']."<br />";
            echo "code: ".$error[ 'code']."<br />";
            echo "message: ".$error[ 'message']."<br />";
        }
    }
}
?>
```

### 注释

By default, warnings generated on a call to any SQLSRV function are
treated as errors. This means that if a warning occurs on a call to a
SQLSRV function, the function returns **`false`**. However, warnings
that correspond to SQLSTATE values 01000, 01001, 01003, and 01S02 are
never treated as errors. For information about changing this behavior,
see <span class="function">sqlsrv\_configure</span> and the
WarningsReturnAsErrors setting.

### 参见

-   <span class="function">sqlsrv\_configure</span>

sqlsrv\_execute
===============

Executes a statement prepared with <span
class="function">sqlsrv\_prepare</span>

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_execute</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Executes a statement prepared with <span
class="function">sqlsrv\_prepare</span>. This function is ideal for
executing a prepared statement multiple times with different parameter
values.

### 参数

`stmt`  
A statement resource returned by <span
class="function">sqlsrv\_prepare</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_execute</span> example**

This example demonstrates how to prepare a statement with <span
class="function">sqlsrv\_prepare</span> and re-execute it multiple times
(with different parameter values) using <span
class="function">sqlsrv\_execute</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1
        SET OrderQty = ?
        WHERE SalesOrderID = ?";

// Initialize parameters and prepare the statement. 
// Variables $qty and $id are bound to the statement, $stmt.
$qty = 0; $id = 0;
$stmt = sqlsrv_prepare( $conn, $sql, array( &$qty, &$id));
if( !$stmt ) {
    die( print_r( sqlsrv_errors(), true));
}

// Set up the SalesOrderDetailID and OrderQty information. 
// This array maps the order ID to order quantity in key=>value pairs.
$orders = array( 1=>10, 2=>20, 3=>30);

// Execute the statement for each order.
foreach( $orders as $id => $qty) {
    // Because $id and $qty are bound to $stmt1, their updated
    // values are used with each execution of the statement. 
    if( sqlsrv_execute( $stmt ) === false ) {
          die( print_r( sqlsrv_errors(), true));
    }
}
?>
```

### 注释

When you prepare a statement that uses variables as parameters, the
variables are bound to the statement. This means that if you update the
values of the variables, the next time you execute the statement it will
run with updated parameter values. For statements that you plan to
execute only once, use <span class="function">sqlsrv\_query</span>.

### 参见

-   <span class="function">sqlsrv\_prepare</span>
-   <span class="function">sqlsrv\_query</span>

sqlsrv\_fetch\_array
====================

Returns a row as an array

### 说明

<span class="type">array</span> <span
class="methodname">sqlsrv\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$fetchType`</span> \[, <span class="methodparam"><span
class="type">int</span> `$row`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`</span>
\]\]\] )

Returns the next available row of data as an associative array, a
numeric array, or both (the default).

### 参数

`stmt`  
A statement resource returned by sqlsrv\_query or sqlsrv\_prepare.

`fetchType`  
A predefined constant specifying the type of array to return. Possible
values are **`SQLSRV_FETCH_ASSOC`**, **`SQLSRV_FETCH_NUMERIC`**, and
**`SQLSRV_FETCH_BOTH`** (the default).

A fetch type of SQLSRV\_FETCH\_ASSOC should not be used when consuming a
result set with multiple columns of the same name.

`row`  
Specifies the row to access in a result set that uses a scrollable
cursor. Possible values are **`SQLSRV_SCROLL_NEXT`**,
**`SQLSRV_SCROLL_PRIOR`**, **`SQLSRV_SCROLL_FIRST`**,
**`SQLSRV_SCROLL_LAST`**, **`SQLSRV_SCROLL_ABSOLUTE`** and,
**`SQLSRV_SCROLL_RELATIVE`** (the default). When this parameter is
specified, the `fetchType` must be explicitly defined.

`offset`  
Specifies the row to be accessed if the row parameter is set to
**`SQLSRV_SCROLL_ABSOLUTE`** or **`SQLSRV_SCROLL_RELATIVE`**. Note that
the first row in a result set has index 0.

### 返回值

Returns an array on success, **`null`** if there are no more rows to
return, and **`false`** if an error occurs.

### 范例

**示例 \#1 Retrieving an associative array.**

``` php
<?php
$serverName = "serverName\instanceName";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo );
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT FirstName, LastName FROM SomeTable";
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false) {
    die( print_r( sqlsrv_errors(), true) );
}

while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC) ) {
      echo $row['LastName'].", ".$row['FirstName']."<br />";
}

sqlsrv_free_stmt( $stmt);
?>
```

**示例 \#2 Retrieving a numeric array.**

``` php
<?php
$serverName = "serverName\instanceName";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo );
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT FirstName, LastName FROM SomeTable";
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false) {
    die( print_r( sqlsrv_errors(), true) );
}

while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_NUMERIC) ) {
      echo $row[0].", ".$row[1]."<br />";
}

sqlsrv_free_stmt( $stmt);
?>
```

### 注释

Not specifying the `fetchType` or explicitly using the
**`SQLSRV_FETCH_TYPE`** constant in the examples above will return an
array that has both associative and numeric keys.

If more than one column is returned with the same name, the last column
will take precedence. To avoid field name collisions, use aliases.

If a column with no name is returned, the associative key for the array
element will be an empty string ("").

### 参见

-   <span class="function">sqlsrv\_connect</span>
-   <span class="function">sqlsrv\_query</span>
-   <span class="function">sqlsrv\_errors</span>
-   <span class="function">sqlsrv\_fetch</span>

sqlsrv\_fetch\_object
=====================

Retrieves the next row of data in a result set as an object

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$className`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ctorParams`</span> \[, <span
class="methodparam"><span class="type">int</span> `$row`</span> \[,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
\]\]\]\] )

Retrieves the next row of data in a result set as an instance of the
specified class with properties that match the row field names and
values that correspond to the row field values.

### 参数

`stmt`  
A statement resource created by <span
class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_execute</span>.

`className`  
The name of the class to instantiate. If no class name is specified,
stdClass is instantiated.

`ctorParams`  
Values passed to the constructor of the specified class. If the
constructor of the specified class takes parameters, the ctorParams
array must be supplied.

`row`  
The row to be accessed. This parameter can only be used if the specified
statement was prepared with a scrollable cursor. In that case, this
parameter can take on one of the following values:

-   SQLSRV\_SCROLL\_NEXT
-   SQLSRV\_SCROLL\_PRIOR
-   SQLSRV\_SCROLL\_FIRST
-   SQLSRV\_SCROLL\_LAST
-   SQLSRV\_SCROLL\_ABSOLUTE
-   SQLSRV\_SCROLL\_RELATIVE

`offset`  
Specifies the row to be accessed if the row parameter is set to
**`SQLSRV_SCROLL_ABSOLUTE`** or **`SQLSRV_SCROLL_RELATIVE`**. Note that
the first row in a result set has index 0.

### 返回值

Returns an object on success, **`null`** if there are no more rows to
return, and **`false`** if an error occurs or if the specified class
does not exist.

### 范例

**示例 \#1 <span class="function">sqlsrv\_fetch\_object</span> example**

The following example demonstrates how to retrieve a row as a stdClass
object.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT fName, lName FROM Table_1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Retrieve each row as an object.
// Because no class is specified, each row will be retrieved as a stdClass object.
// Property names correspond to field names.
while( $obj = sqlsrv_fetch_object( $stmt)) {
      echo $obj->fName.", ".$obj->lName."<br />";
}
?>
```

### 注释

If a class name is specified with the optional $className parameter and
the class has properties whose names match the result set field names,
the corresponding result set values are applied to the properties. If a
result set field name does not match a class property, a property with
the result set field name is added to the object and the result set
value is applied to the property. The following rules apply when using
the $className parameter:

-   Field-property name matching is case-sensitive.
-   Field-property matching occurs regardless of access modifiers.
-   Class property data types are ignored when applying a field value to
    a property.
-   If the class does not exist, the function returns **`false`** and
    adds an error to the error collection.

Regardless of whether the $className parameter is supplied, if a field
with no name is returned, the field value will be ignored and a warning
will be added to the error collection.

When consuming a result set that has multiple columns with the same
name, it may be better to use <span
class="function">sqlsrv\_fetch\_array</span> or the combination of <span
class="function">sqlsrv\_fetch</span> and <span
class="function">sqlsrv\_get\_field</span>.

### 参见

-   <span class="function">sqlsrv\_fetch</span>
-   <span class="function">sqlsrv\_fetch\_array</span>

sqlsrv\_fetch
=============

Makes the next row in a result set available for reading

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_fetch</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$row`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`</span> \]\] )

Makes the next row in a result set available for reading. Use <span
class="function">sqlsrv\_get\_field</span> to read the fields of the
row.

### 参数

`stmt`  
A statement resource created by executing <span
class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_execute</span>.

`row`  
The row to be accessed. This parameter can only be used if the specified
statement was prepared with a scrollable cursor. In that case, this
parameter can take on one of the following values:

-   SQLSRV\_SCROLL\_NEXT
-   SQLSRV\_SCROLL\_PRIOR
-   SQLSRV\_SCROLL\_FIRST
-   SQLSRV\_SCROLL\_LAST
-   SQLSRV\_SCROLL\_ABSOLUTE
-   SQLSRV\_SCROLL\_RELATIVE

`offset`  
Specifies the row to be accessed if the row parameter is set to
**`SQLSRV_SCROLL_ABSOLUTE`** or **`SQLSRV_SCROLL_RELATIVE`**. Note that
the first row in a result set has index 0.

### 返回值

Returns **`true`** if the next row of a result set was successfully
retrieved, **`false`** if an error occurs, and **`null`** if there are
no more rows in the result set.

### 范例

**示例 \#1 <span class="function">sqlsrv\_fetch</span> example**

The following example demonstrates how to retrieve a row with <span
class="function">sqlsrv\_fetch</span> and get the row fields with <span
class="function">sqlsrv\_get\_field</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Name, Comment 
        FROM Table_1
        WHERE ReviewID=1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Make the first (and in this case, only) row of the result set available for reading.
if( sqlsrv_fetch( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

// Get the row fields. Field indices start at 0 and must be retrieved in order.
// Retrieving row fields by name is not supported by sqlsrv_get_field.
$name = sqlsrv_get_field( $stmt, 0);
echo "$name: ";

$comment = sqlsrv_get_field( $stmt, 1);
echo $comment;
?>
```

### 参见

-   <span class="function">sqlsrv\_get\_field</span>
-   <span class="function">sqlsrv\_fetch\_array</span>
-   <span class="function">sqlsrv\_fetch\_object</span>

sqlsrv\_field\_metadata
=======================

Retrieves metadata for the fields of a statement prepared by <span
class="function">sqlsrv\_prepare</span> or <span
class="function">sqlsrv\_query</span>

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_field\_metadata</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Retrieves metadata for the fields of a statement prepared by <span
class="function">sqlsrv\_prepare</span> or <span
class="function">sqlsrv\_query</span>. <span
class="function">sqlsrv\_field\_metadata</span> can be called on a
statement before or after statement execution.

### 参数

`stmt`  
The statement resource for which metadata is returned.

### 返回值

Returns an array of arrays on success. Otherwise, **`false`** is
returned. Each returned array is described by the following table:

| Key       | Description                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Name      | The name of the field.                                                                                                               |
| Type      | The numeric value for the SQL type.                                                                                                  |
| Size      | The number of characters for fields of character type, the number of bytes for fields of binary type, or **`null`** for other types. |
| Precision | The precision for types of variable precision, **`null`** for other types.                                                           |
| Scale     | The scale for types of variable scale, **`null`** for other types.                                                                   |
| Nullable  | An enumeration indicating whether the column is nullable, not nullable, or if it is not known.                                       |

For more information, see
<a href="http://msdn.microsoft.com/en-us/library/cc296197.aspx" class="link external">» sqlsrv_field_metadata</a>
in the Microsoft SQLSRV documentation.

### 范例

**示例 \#1 <span class="function">sqlsrv\_field\_metadata</span>
example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"AdventureWorks", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
   die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT * FROM Table_1";
$stmt = sqlsrv_prepare( $conn, $sql );

foreach( sqlsrv_field_metadata( $stmt ) as $fieldMetadata ) {
    foreach( $fieldMetadata as $name => $value) {
       echo "$name: $value<br />";
    }
      echo "<br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_client\_info</span>

sqlsrv\_free\_stmt
==================

Frees all resources for the specified statement

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_free\_stmt</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Frees all resources for the specified statement. The statement cannot be
used after <span class="function">sqlsrv\_free\_stmt</span> has been
called on it. If <span class="function">sqlsrv\_free\_stmt</span> is
called on an in-progress statement that alters server state, statement
execution is terminated and the statement is rolled back.

### 参数

`stmt`  
The statement for which resources are freed. Note that **`null`** is a
valid parameter value. This allows the function to be called multiple
times in a script.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_free\_stmt</span> example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

/*-------------------------------
     Process query results here.
-------------------------------*/

/* Free the statement resources. */
sqlsrv_free_stmt( $stmt);

?>
```

### 注释

The main difference between <span
class="function">sqlsrv\_free\_stmt</span> and <span
class="function">sqlsrv\_cancel</span> is that a statement resource
cancelled with <span class="function">sqlsrv\_cancel</span> can be
re-executed if it was created with <span
class="function">sqlsrv\_prepare</span>. A statement resource cancelled
with <span class="function">sqlsrv\_free\_statement</span> cannot be
re-executed.

### 参见

-   <span class="function">sqlsrv\_cancel</span>

sqlsrv\_get\_config
===================

Returns the value of the specified configuration setting

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_get\_config</span> ( <span
class="methodparam"><span class="type">string</span> `$setting`</span> )

Returns the value of the specified configuration setting.

### 参数

`setting`  
The name of the setting for which the value is returned. For a list of
configurable settings, see <span
class="function">sqlsrv\_configure</span>.

### 返回值

Returns the value of the specified setting. If an invalid setting is
specified, **`false`** is returned.

### 参见

-   <span class="function">sqlsrv\_configure</span>

sqlsrv\_get\_field
==================

Gets field data from the currently selected row

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_get\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> ,
<span class="methodparam"><span class="type">int</span>
`$fieldIndex`</span> \[, <span class="methodparam"><span
class="type">int</span> `$getAsType`</span> \] )

Gets field data from the currently selected row. Fields must be accessed
in order. Field indices start at 0.

### 参数

`stmt`  
A statement resource returned by <span
class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_execute</span>.

`fieldIndex`  
The index of the field to be retrieved. Field indices start at 0. Fields
must be accessed in order. i.e. If you access field index 1, then field
index 0 will not be available.

`getAsType`  
The PHP data type for the returned field data. If this parameter is not
set, the field data will be returned as its default PHP data type. For
information about default PHP data types, see
<a href="http://msdn.microsoft.com/en-us/library/cc296193.aspx" class="link external">» Default PHP Data Types</a>
in the Microsoft SQLSRV documentation.

### 返回值

Returns data from the specified field on success. Returns **`false`**
otherwise.

### 范例

**示例 \#1 <span class="function">sqlsrv\_get\_field</span> example**

The following example demonstrates how to retrieve a row with <span
class="function">sqlsrv\_fetch</span> and get the row fields with <span
class="function">sqlsrv\_get\_field</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Name, Comment 
        FROM Table_1
        WHERE ReviewID=1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Make the first (and in this case, only) row of the result set available for reading.
if( sqlsrv_fetch( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

// Get the row fields. Field indices start at 0 and must be retrieved in order.
// Retrieving row fields by name is not supported by sqlsrv_get_field.
$name = sqlsrv_get_field( $stmt, 0);
echo "$name: ";

$comment = sqlsrv_get_field( $stmt, 1);
echo $comment;
?>
```

### 参见

-   <span class="function">sqlsrv\_fetch</span>
-   <span class="function">sqlsrv\_fetch\_array</span>
-   <span class="function">sqlsrv\_fetch\_object</span>

sqlsrv\_has\_rows
=================

Indicates whether the specified statement has rows

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_has\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Indicates whether the specified statement has rows.

### 参数

`stmt`  
A statement resource returned by <span
class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_execute</span>.

### 返回值

Returns **`true`** if the specified statement has rows and **`false`**
if the statement does not have rows or if an error occurred.

### 范例

**示例 \#1 <span class="function">sqlsrv\_has\_rows</span> example**

``` php
<?php
$server = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" )
$conn = sqlsrv_connect( $server, $connectionInfo );

$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");

if ($stmt) {
   $rows = sqlsrv_has_rows( $stmt );
   if ($rows === true)
      echo "There are rows. <br />";
   else 
      echo "There are no rows. <br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_num\_rows</span>
-   <span class="function">sqlsrv\_query</span>

sqlsrv\_next\_result
====================

Makes the next result of the specified statement active

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_next\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Makes the next result of the specified statement active. Results include
result sets, row counts, and output parameters.

### 参数

`stmt`  
The statement on which the next result is being called.

### 返回值

Returns **`true`** if the next result was successfully retrieved,
**`false`** if an error occurred, and **`null`** if there are no more
results to retrieve.

### 范例

**示例 \#1 <span class="function">sqlsrv\_next\_result</span> example**

The following example executes a batch query that inserts into a table
and then selects from the table. This produces two results on the
statement: one for the rows affected by the INSERT and one for the rows
returned by the SELECT. To get to the rows returned by the SELECT, <span
class="function">sqlsrv\_next\_result</span> must be called to move past
the first result.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array("Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

$query = "INSERT INTO Table_1 (id, data) VALUES (?,?); SELECT * FROM TABLE_1;";
$params = array(1, "some data");
$stmt = sqlsrv_query($conn, $query, $params);

// Consume the first result (rows affected by INSERT) without calling sqlsrv_next_result.
echo "Rows affected: ".sqlsrv_rows_affected($stmt)."<br />";

// Move to the next result and display results.
$next_result = sqlsrv_next_result($stmt);
if( $next_result ) {
   while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC)){
      echo $row['id'].": ".$row['data']."<br />"; 
   }
} elseif( is_null($next_result)) {
     echo "No more results.<br />";
} else {
     die(print_r(sqlsrv_errors(), true));
}
?>
```

### 参见

-   <span class="function">sqlsrv\_query</span>
-   <span class="function">sqlsrv\_fetch\_array</span>
-   <span class="function">sqlsrv\_rows\_affected</span>

sqlsrv\_num\_fields
===================

Retrieves the number of fields (columns) on a statement

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Retrieves the number of fields (columns) on a statement.

### 参数

`stmt`  
The statement for which the number of fields is returned. <span
class="function">sqlsrv\_num\_fields</span> can be called on a statement
before or after statement execution.

### 返回值

Returns the number of fields on success. Returns **`false`** otherwise.

### 范例

**示例 \#1 <span class="function">sqlsrv\_num\_fields</span> example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
   die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT * FROM Table_1";
$stmt = sqlsrv_query($conn, $sql);
if( $stmt === false) {
   die( print_r( sqlsrv_errors(), true));
}

$numFields = sqlsrv_num_fields( $stmt );

while( sqlsrv_fetch( $stmt )) {
   // Iterate through the fields of each row.
   for($i = 0; $i < $numFields; $i++) { 
      echo sqlsrv_get_field($stmt, $i)." ";
   }
   echo "<br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_field\_metadata</span>
-   <span class="function">sqlsrv\_fetch</span>
-   <span class="function">sqlsrv\_get\_field</span>

sqlsrv\_num\_rows
=================

Retrieves the number of rows in a result set

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Retrieves the number of rows in a result set. This function requires
that the statement resource be created with a static or keyset cursor.
For more information, see <span class="function">sqlsrv\_query</span>,
<span class="function">sqlsrv\_prepare</span>, or
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>
in the Microsoft SQLSRV documentation.

### 参数

`stmt`  
The statement for which the row count is returned. The statement
resource must be created with a static or keyset cursor. For more
information, see <span class="function">sqlsrv\_query</span>, <span
class="function">sqlsrv\_prepare</span>, or
<a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a>
in the Microsoft SQLSRV documentation.

### 返回值

Returns the number of rows retrieved on success and **`false`** if an
error occurred. If a forward cursor (the default) or dynamic cursor is
used, **`false`** is returned.

### 范例

**示例 \#1 <span class="function">sqlsrv\_num\_rows</span> example**

``` php
<?php
$server = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $server, $connectionInfo );

$sql = "SELECT * FROM Table_1";
$params = array();
$options =  array( "Scrollable" => SQLSRV_CURSOR_KEYSET );
$stmt = sqlsrv_query( $conn, $sql , $params, $options );

$row_count = sqlsrv_num_rows( $stmt );
   
if ($row_count === false)
   echo "Error in retrieveing row count.";
else
   echo $row_count;
?>
```

### 参见

-   <span class="function">sqlsrv\_has\_rows</span>
-   <span class="function">sqlsrv\_rows\_affected</span>

sqlsrv\_prepare
===============

Prepares a query for execution

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">string</span> `$sql`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$params`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \]\] )

Prepares a query for execution. This function is ideal for preparing a
query that will be executed multiple times with different parameter
values.

### 参数

`conn`  
A connection resource returned by <span
class="function">sqlsrv\_connect</span>.

`sql`  
The string that defines the query to be prepared and executed.

`params`  
An array specifying parameter information when executing a parameterized
query. Array elements can be any of the following:

-   A literal value
-   A PHP variable
-   An array with this structure: array($value \[, $direction \[,
    $phpType \[, $sqlType\]\]\])

The following table describes the elements in the array structure above:

| Element               | Description                                                                                                                                                                          |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $value                | A literal value, a PHP variable, or a PHP by-reference variable.                                                                                                                     |
| $direction (optional) | One of the following SQLSRV constants used to indicate the parameter direction: SQLSRV\_PARAM\_IN, SQLSRV\_PARAM\_OUT, SQLSRV\_PARAM\_INOUT. The default value is SQLSRV\_PARAM\_IN. |
| $phpType (optional)   | A SQLSRV\_PHPTYPE\_\* constant that specifies PHP data type of the returned value.                                                                                                   |
| $sqlType (optional)   | A SQLSRV\_SQLTYPE\_\* constant that specifies the SQL Server data type of the input value.                                                                                           |

`options`  
An array specifying query property options. The supported keys are
described in the following table:

| Key                    | Values                                                                                              | Description                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QueryTimeout           | A positive integer value.                                                                           | Sets the query timeout in seconds. By default, the driver will wait indefinitely for results.                                                                                                                                                            |
| SendStreamParamsAtExec | **`true`** or **`false`** (the default is **`true`**)                                               | Configures the driver to send all stream data at execution (**`true`**), or to send stream data in chunks (**`false`**). By default, the value is set to **`true`**. For more information, see <span class="function">sqlsrv\_send\_stream\_data</span>. |
| Scrollable             | SQLSRV\_CURSOR\_FORWARD, SQLSRV\_CURSOR\_STATIC, SQLSRV\_CURSOR\_DYNAMIC, or SQLSRV\_CURSOR\_KEYSET | See <a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a> in the Microsoft SQLSRV documentation.                                                                       |

### 返回值

Returns a statement resource on success and **`false`** if an error
occurred.

### 范例

**示例 \#1 <span class="function">sqlsrv\_prepare</span> example**

This example demonstrates how to prepare a statement with <span
class="function">sqlsrv\_prepare</span> and re-execute it multiple times
(with different parameter values) using <span
class="function">sqlsrv\_execute</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1
        SET OrderQty = ?
        WHERE SalesOrderID = ?";

// Initialize parameters and prepare the statement. 
// Variables $qty and $id are bound to the statement, $stmt.
$qty = 0; $id = 0;
$stmt = sqlsrv_prepare( $conn, $sql, array( &$qty, &$id));
if( !$stmt ) {
    die( print_r( sqlsrv_errors(), true));
}

// Set up the SalesOrderDetailID and OrderQty information. 
// This array maps the order ID to order quantity in key=>value pairs.
$orders = array( 1=>10, 2=>20, 3=>30);

// Execute the statement for each order.
foreach( $orders as $id => $qty) {
    // Because $id and $qty are bound to $stmt1, their updated
    // values are used with each execution of the statement. 
    if( sqlsrv_execute( $stmt ) === false ) {
          die( print_r( sqlsrv_errors(), true));
    }
}
?>
```

### 注释

When you prepare a statement that uses variables as parameters, the
variables are bound to the statement. This means that if you update the
values of the variables, the next time you execute the statement it will
run with updated parameter values. For statements that you plan to
execute only once, use <span class="function">sqlsrv\_query</span>.

### 参见

-   <span class="function">sqlsrv\_execute</span>
-   <span class="function">sqlsrv\_query</span>

sqlsrv\_query
=============

Prepares and executes a query

### 说明

<span class="type">mixed</span> <span
class="methodname">sqlsrv\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">string</span> `$sql`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$params`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \]\] )

Prepares and executes a query.

### 参数

`conn`  
A connection resource returned by <span
class="function">sqlsrv\_connect</span>.

`sql`  
The string that defines the query to be prepared and executed.

`params`  
An array specifying parameter information when executing a parameterized
query. Array elements can be any of the following:

-   A literal value
-   A PHP variable
-   An array with this structure: array($value \[, $direction \[,
    $phpType \[, $sqlType\]\]\])

The following table describes the elements in the array structure above:

| Element               | Description                                                                                                                                                                          |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $value                | A literal value, a PHP variable, or a PHP by-reference variable.                                                                                                                     |
| $direction (optional) | One of the following SQLSRV constants used to indicate the parameter direction: SQLSRV\_PARAM\_IN, SQLSRV\_PARAM\_OUT, SQLSRV\_PARAM\_INOUT. The default value is SQLSRV\_PARAM\_IN. |
| $phpType (optional)   | A SQLSRV\_PHPTYPE\_\* constant that specifies PHP data type of the returned value.                                                                                                   |
| $sqlType (optional)   | A SQLSRV\_SQLTYPE\_\* constant that specifies the SQL Server data type of the input value.                                                                                           |

`options`  
An array specifying query property options. The supported keys are
described in the following table:

| Key                    | Values                                                                                              | Description                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QueryTimeout           | A positive integer value.                                                                           | Sets the query timeout in seconds. By default, the driver will wait indefinitely for results.                                                                                                                                                            |
| SendStreamParamsAtExec | **`true`** or **`false`** (the default is **`true`**)                                               | Configures the driver to send all stream data at execution (**`true`**), or to send stream data in chunks (**`false`**). By default, the value is set to **`true`**. For more information, see <span class="function">sqlsrv\_send\_stream\_data</span>. |
| Scrollable             | SQLSRV\_CURSOR\_FORWARD, SQLSRV\_CURSOR\_STATIC, SQLSRV\_CURSOR\_DYNAMIC, or SQLSRV\_CURSOR\_KEYSET | See <a href="http://msdn.microsoft.com/en-us/library/ee376927.aspx" class="link external">» Specifying a Cursor Type and Selecting Rows</a> in the Microsoft SQLSRV documentation.                                                                       |

### 返回值

Returns a statement resource on success and **`false`** if an error
occurred.

### 范例

**示例 \#1 <span class="function">sqlsrv\_query</span> example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "INSERT INTO Table_1 (id, data) VALUES (?, ?)";
$params = array(1, "some data");

$stmt = sqlsrv_query( $conn, $sql, $params);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}
?>
```

### 注释

For statements that you plan to execute only once, use <span
class="function">sqlsrv\_query</span>. If you intend to re-execute a
statement with different parameter values, use the combination of <span
class="function">sqlsrv\_prepare</span> and <span
class="function">sqlsrv\_execute</span>.

### 参见

-   <span class="function">sqlsrv\_prepare</span>
-   <span class="function">sqlsrv\_execute</span>

sqlsrv\_rollback
================

Rolls back a transaction that was begun with <span
class="function">sqlsrv\_begin\_transaction</span>

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_rollback</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

Rolls back a transaction that was begun with <span
class="function">sqlsrv\_begin\_transaction</span> and returns the
connection to auto-commit mode.

### 参数

`conn`  
The connection resource returned by a call to <span
class="function">sqlsrv\_connect</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">sqlsrv\_rollback</span> example**

The following example demonstrates how to use <span
class="function">sqlsrv\_begin\_transaction</span> together with <span
class="function">sqlsrv\_commit</span> and <span
class="function">sqlsrv\_rollback</span>.

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true ));
}

/* Begin the transaction. */
if ( sqlsrv_begin_transaction( $conn ) === false ) {
     die( print_r( sqlsrv_errors(), true ));
}

/* Initialize parameter values. */
$orderId = 1; $qty = 10; $productId = 100;

/* Set up and execute the first query. */
$sql1 = "INSERT INTO OrdersTable (ID, Quantity, ProductID)
         VALUES (?, ?, ?)";
$params1 = array( $orderId, $qty, $productId );
$stmt1 = sqlsrv_query( $conn, $sql1, $params1 );

/* Set up and execute the second query. */
$sql2 = "UPDATE InventoryTable 
         SET Quantity = (Quantity - ?) 
         WHERE ProductID = ?";
$params2 = array($qty, $productId);
$stmt2 = sqlsrv_query( $conn, $sql2, $params2 );

/* If both queries were successful, commit the transaction. */
/* Otherwise, rollback the transaction. */
if( $stmt1 && $stmt2 ) {
     sqlsrv_commit( $conn );
     echo "Transaction committed.<br />";
} else {
     sqlsrv_rollback( $conn );
     echo "Transaction rolled back.<br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_begin\_transaction</span>
-   <span class="function">sqlsrv\_commit</span>

sqlsrv\_rows\_affected
======================

Returns the number of rows modified by the last INSERT, UPDATE, or
DELETE query executed

### 说明

<span class="type">int</span> <span
class="methodname">sqlsrv\_rows\_affected</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Returns the number of rows modified by the last INSERT, UPDATE, or
DELETE query executed. For information about the number of rows returned
by a SELECT query, see <span class="function">sqlsrv\_num\_rows</span>.

### 参数

`stmt`  
The executed statement resource for which the number of affected rows is
returned.

### 返回值

Returns the number of rows affected by the last INSERT, UPDATE, or
DELETE query. If no rows were affected, 0 is returned. If the number of
affected rows cannot be determined, -1 is returned. If an error
occurred, **`false`** is returned.

### 范例

**示例 \#1 <span class="function">sqlsrv\_rows\_affected</span>
example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1 SET data = ? WHERE id = ?";

$params = array("updated data", 1);

$stmt = sqlsrv_query( $conn, $sql, $params);

$rows_affected = sqlsrv_rows_affected( $stmt);
if( $rows_affected === false) {
     die( print_r( sqlsrv_errors(), true));
} elseif( $rows_affected == -1) {
      echo "No information available.<br />";
} else {
      echo $rows_affected." rows were updated.<br />";
}
?>
```

### 参见

-   <span class="function">sqlsrv\_num\_rows</span>

sqlsrv\_send\_stream\_data
==========================

Sends data from parameter streams to the server

### 说明

<span class="type">bool</span> <span
class="methodname">sqlsrv\_send\_stream\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$stmt`</span> )

Send data from parameter streams to the server. Up to 8 KB of data is
sent with each call.

### 参数

`stmt`  
A statement resource returned by <span
class="function">sqlsrv\_query</span> or <span
class="function">sqlsrv\_execute</span>.

### 返回值

Returns **`true`** if there is more data to send and **`false`** if
there is not.

### 范例

**示例 \#1 <span class="function">sqlsrv\_send\_stream\_data</span>
example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1 SET data = ( ?) WHERE id = 100";

// Open parameter data as a stream and put it in the $params array.
$data = fopen( "data://text/plain,[ Lengthy content here. ]", "r");
$params = array( &$data);

// Prepare the statement. Use the $options array to turn off the
// default behavior, which is to send all stream data at the time of query
// execution.
$options = array("SendStreamParamsAtExec"=>0);
$stmt = sqlsrv_prepare( $conn, $sql, $params, $options);

sqlsrv_execute( $stmt);

// Send up to 8K of parameter data to the server 
// with each call to sqlsrv_send_stream_data.
$i = 1;
while( sqlsrv_send_stream_data( $stmt)) {
      $i++;
}
echo "$i calls were made.";
?>
```

### 参见

-   <span class="function">sqlsrv\_prepare</span>
-   <span class="function">sqlsrv\_query</span>

sqlsrv\_server\_info
====================

Returns information about the server

### 说明

<span class="type">array</span> <span
class="methodname">sqlsrv\_server\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

Returns information about the server.

### 参数

`conn`  
The connection resource that connects the client and the server.

### 返回值

Returns an array as described in the following table:

| CurrentDatabase  | The connected-to database. |
|------------------|----------------------------|
| SQLServerVersion | The SQL Server version.    |
| SQLServerName    | The name of the server.    |

### 范例

**示例 \#1 <span class="function">sqlsrv\_server\_info</span> example**

``` php
<?php
$serverName = "serverName\sqlexpress";
$conn = sqlsrv_connect( $serverName);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$server_info = sqlsrv_server_info( $conn);
if( $server_info )
{
    foreach( $server_info as $key => $value) {
       echo $key.": ".$value."<br />";
    }
} else {
      die( print_r( sqlsrv_errors(), true));
}
?>
```

### 参见

-   <span class="function">sqlsrv\_client\_info</span>

**目录**

-   [sqlsrv\_begin\_transaction](/book/sqlsrv.html#sqlsrv_begin_transaction)
    — Begins a database transaction
-   [sqlsrv\_cancel](/book/sqlsrv.html#sqlsrv_cancel) — Cancels a
    statement
-   [sqlsrv\_client\_info](/book/sqlsrv.html#sqlsrv_client_info) —
    Returns information about the client and specified connection
-   [sqlsrv\_close](/book/sqlsrv.html#sqlsrv_close) — Closes an open
    connection and releases resourses associated with the connection
-   [sqlsrv\_commit](/book/sqlsrv.html#sqlsrv_commit) — Commits a
    transaction that was begun with sqlsrv\_begin\_transaction
-   [sqlsrv\_configure](/book/sqlsrv.html#sqlsrv_configure) — Changes
    the driver error handling and logging configurations
-   [sqlsrv\_connect](/book/sqlsrv.html#sqlsrv_connect) — Opens a
    connection to a Microsoft SQL Server database
-   [sqlsrv\_errors](/book/sqlsrv.html#sqlsrv_errors) — Returns error
    and warning information about the last SQLSRV operation performed
-   [sqlsrv\_execute](/book/sqlsrv.html#sqlsrv_execute) — Executes a
    statement prepared with sqlsrv\_prepare
-   [sqlsrv\_fetch\_array](/book/sqlsrv.html#sqlsrv_fetch_array) —
    Returns a row as an array
-   [sqlsrv\_fetch\_object](/book/sqlsrv.html#sqlsrv_fetch_object) —
    Retrieves the next row of data in a result set as an object
-   [sqlsrv\_fetch](/book/sqlsrv.html#sqlsrv_fetch) — Makes the next row
    in a result set available for reading
-   [sqlsrv\_field\_metadata](/book/sqlsrv.html#sqlsrv_field_metadata) —
    Retrieves metadata for the fields of a statement prepared by
    sqlsrv\_prepare or sqlsrv\_query
-   [sqlsrv\_free\_stmt](/book/sqlsrv.html#sqlsrv_free_stmt) — Frees all
    resources for the specified statement
-   [sqlsrv\_get\_config](/book/sqlsrv.html#sqlsrv_get_config) — Returns
    the value of the specified configuration setting
-   [sqlsrv\_get\_field](/book/sqlsrv.html#sqlsrv_get_field) — Gets
    field data from the currently selected row
-   [sqlsrv\_has\_rows](/book/sqlsrv.html#sqlsrv_has_rows) — Indicates
    whether the specified statement has rows
-   [sqlsrv\_next\_result](/book/sqlsrv.html#sqlsrv_next_result) — Makes
    the next result of the specified statement active
-   [sqlsrv\_num\_fields](/book/sqlsrv.html#sqlsrv_num_fields) —
    Retrieves the number of fields (columns) on a statement
-   [sqlsrv\_num\_rows](/book/sqlsrv.html#sqlsrv_num_rows) — Retrieves
    the number of rows in a result set
-   [sqlsrv\_prepare](/book/sqlsrv.html#sqlsrv_prepare) — Prepares a
    query for execution
-   [sqlsrv\_query](/book/sqlsrv.html#sqlsrv_query) — Prepares and
    executes a query
-   [sqlsrv\_rollback](/book/sqlsrv.html#sqlsrv_rollback) — Rolls back a
    transaction that was begun with sqlsrv\_begin\_transaction
-   [sqlsrv\_rows\_affected](/book/sqlsrv.html#sqlsrv_rows_affected) —
    Returns the number of rows modified by the last INSERT, UPDATE, or
    DELETE query executed
-   [sqlsrv\_send\_stream\_data](/book/sqlsrv.html#sqlsrv_send_stream_data)
    — Sends data from parameter streams to the server
-   [sqlsrv\_server\_info](/book/sqlsrv.html#sqlsrv_server_info) —
    Returns information about the server
