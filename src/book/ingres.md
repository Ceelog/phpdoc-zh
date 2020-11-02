Ingres DBMS, EDBC, and Enterprise Access Gateways
=================================================

**目录**

-   [简介](/book/ingres.html#简介)
-   [安装／配置](/book/ingres.html#安装／配置)
    -   [需求](/book/ingres.html#需求)
    -   [安装](/book/ingres.html#安装)
    -   [运行时配置](/book/ingres.html#运行时配置)
    -   [资源类型](/book/ingres.html#资源类型)
-   [预定义常量](/book/ingres.html#预定义常量)
-   [范例](/book/ingres.html#范例)
    -   [Basic usage](/book/ingres.html#Basic%20usage)
-   [Ingres 函数](/book/ingres.html#Ingres%20函数)
    -   [ingres\_autocommit\_state](/book/ingres.html#ingres_autocommit_state)
        — Test if the connection is using autocommit
    -   [ingres\_autocommit](/book/ingres.html#ingres_autocommit) —
        Switch autocommit on or off
    -   [ingres\_charset](/book/ingres.html#ingres_charset) — Returns
        the installation character set
    -   [ingres\_close](/book/ingres.html#ingres_close) — Close an
        Ingres database connection
    -   [ingres\_commit](/book/ingres.html#ingres_commit) — Commit a
        transaction
    -   [ingres\_connect](/book/ingres.html#ingres_connect) — Open a
        connection to an Ingres database
    -   [ingres\_cursor](/book/ingres.html#ingres_cursor) — Get a cursor
        name for a given result resource
    -   [ingres\_errno](/book/ingres.html#ingres_errno) — Get the last
        Ingres error number generated
    -   [ingres\_error](/book/ingres.html#ingres_error) — Get a
        meaningful error message for the last error generated
    -   [ingres\_errsqlstate](/book/ingres.html#ingres_errsqlstate) —
        Get the last SQLSTATE error code generated
    -   [ingres\_escape\_string](/book/ingres.html#ingres_escape_string)
        — Escape special characters for use in a query
    -   [ingres\_execute](/book/ingres.html#ingres_execute) — Execute a
        prepared query
    -   [ingres\_fetch\_array](/book/ingres.html#ingres_fetch_array) —
        Fetch a row of result into an array
    -   [ingres\_fetch\_assoc](/book/ingres.html#ingres_fetch_assoc) —
        Fetch a row of result into an associative array
    -   [ingres\_fetch\_object](/book/ingres.html#ingres_fetch_object) —
        Fetch a row of result into an object
    -   [ingres\_fetch\_proc\_return](/book/ingres.html#ingres_fetch_proc_return)
        — Get the return value from a procedure call
    -   [ingres\_fetch\_row](/book/ingres.html#ingres_fetch_row) — Fetch
        a row of result into an enumerated array
    -   [ingres\_field\_length](/book/ingres.html#ingres_field_length) —
        Get the length of a field
    -   [ingres\_field\_name](/book/ingres.html#ingres_field_name) — Get
        the name of a field in a query result
    -   [ingres\_field\_nullable](/book/ingres.html#ingres_field_nullable)
        — Test if a field is nullable
    -   [ingres\_field\_precision](/book/ingres.html#ingres_field_precision)
        — Get the precision of a field
    -   [ingres\_field\_scale](/book/ingres.html#ingres_field_scale) —
        Get the scale of a field
    -   [ingres\_field\_type](/book/ingres.html#ingres_field_type) — Get
        the type of a field in a query result
    -   [ingres\_free\_result](/book/ingres.html#ingres_free_result) —
        Free the resources associated with a result identifier
    -   [ingres\_next\_error](/book/ingres.html#ingres_next_error) — Get
        the next Ingres error
    -   [ingres\_num\_fields](/book/ingres.html#ingres_num_fields) — Get
        the number of fields returned by the last query
    -   [ingres\_num\_rows](/book/ingres.html#ingres_num_rows) — Get the
        number of rows affected or returned by a query
    -   [ingres\_pconnect](/book/ingres.html#ingres_pconnect) — Open a
        persistent connection to an Ingres database
    -   [ingres\_prepare](/book/ingres.html#ingres_prepare) — Prepare a
        query for later execution
    -   [ingres\_query](/book/ingres.html#ingres_query) — Send an SQL
        query to Ingres
    -   [ingres\_result\_seek](/book/ingres.html#ingres_result_seek) —
        Set the row position before fetching data
    -   [ingres\_rollback](/book/ingres.html#ingres_rollback) — Roll
        back a transaction
    -   [ingres\_set\_environment](/book/ingres.html#ingres_set_environment)
        — Set environment features controlling output options
    -   [ingres\_unbuffered\_query](/book/ingres.html#ingres_unbuffered_query)
        — Send an unbuffered SQL query to Ingres

The Ingres driver for PHP enables you to connect to and query the Ingres
DBMS, EDBC, and Enterprise Access Gateways.

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.1.0.

安装／配置
==========

**目录**

-   [需求](/book/ingres.html#需求)
-   [安装](/book/ingres.html#安装)
-   [运行时配置](/book/ingres.html#运行时配置)
-   [资源类型](/book/ingres.html#资源类型)

需求
----

To use or build the PHP extension for Ingres you must have a working
Ingres client environment. You can download the client software for
Ingres from
<a href="http://esd.ingres.com/" class="link external">» http://esd.ingres.com/</a>.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/ingres" class="link external">» https://pecl.php.net/package/ingres</a>.

You can download the DLL for this PECL extension from
<a href="http://esd.ingres.com/product/drivers/PHP/" class="link external">» http://esd.ingres.com/product/drivers/PHP/</a>.

To have these functions available, you must
<a href="https://pecl.php.net/package/ingres" class="link external">» download</a>
and compile this extension, enabling Ingres support using the
**--with-ingres\[=DIR\]** option, where DIR is the Ingres base
directory. If the `II_SYSTEM` environment variable is not set correctly
you may need to use **--with-ingres=DIR** to specify your Ingres
installation directory.

PHP code written for version 2.x and later is not backward-compatible
with earlier versions of this PHP extension. However, it is possible to
run two incompatible releases within the same PHP environment using the
**--enable-ingres2** option. This configuration option renames the
extension to ingres2, changing function names, configuration settings,
and constants. For example, with this option enabled, <span
class="function">ingres\_connect</span> becomes <span
class="function">ingres2\_connect</span>.

To use this extension the system environment variable II\_SYSTEM must be
defined. Linux and UNIX users will also need to define the shared
library search path, for example, `LD_LIBRARY_PATH`. When used with the
Apache web server these variables must be set explicitly in the startup
script for Apache. In addition, the *PassEnv* directive is required for
the Ingres extension to load the correct shared libraries. For example:

**示例 \#1 Example usage of PassEnv for Ingres**

    <IfModule mod_env.c>
        PassEnv II_SYSTEM
        PassEnv LD_LIBRARY_PATH
    </IfModule>

> **Note**:
>
> For example configurations for different web servers and operating
> systems see
> <a href="http://community.ingres.com/wiki/Ingres_Articles#Ingres_and_Web_Servers" class="link external">» http://community.ingres.com/wiki/Ingres_Articles#Ingres_and_Web_Servers</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                     | 默认   | 可修改范围       | 更新日志                      |
|--------------------------------------------------------------------------|--------|------------------|-------------------------------|
| <a href="/book/ingres.html#" class="link">ingres.allow_persistent</a>    | "1"    | PHP\_INI\_SYSTEM | Available since ingres 1.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>   | "1"    | PHP\_INI\_ALL    | Available since ingres 1.4.0. |
| <a href="/book/ingres.html#" class="link">ingres.auto</a>                | "1"    | PHP\_INI\_ALL    | Available since ingres 2.0.0. |
| <a href="/book/ingres.html#" class="link">ingres.blob_segment_length</a> | "4096" | PHP\_INI\_ALL    | Available since ingres 1.2.0. |
| <a href="/book/ingres.html#" class="link">ingres.cursor_mode</a>         | "0"    | PHP\_INI\_ALL    | Available since ingres 1.1.0. |
| <a href="/book/ingres.html#" class="link">ingres.default_database</a>    | NULL   | PHP\_INI\_ALL    | Available since ingres 1.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.default_password</a>    | NULL   | PHP\_INI\_ALL    | Available since ingres 1.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.default_user</a>        | NULL   | PHP\_INI\_ALL    | Available since ingres 1.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.describe</a>            | 1      | PHP\_INI\_ALL    | Available since ingres 2.1.0  |
| <a href="/book/ingres.html#" class="link">ingres.fetch_buffer_size</a>   | 100    | PHP\_INI\_ALL    | Available since ingres 2.1.0  |
| <a href="/book/ingres.html#" class="link">ingres.max_links</a>           | "-1"   | PHP\_INI\_SYSTEM | Available since ingres 1.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.max_persistent</a>      | "-1"   | PHP\_INI\_SYSTEM | Available since ingres 1.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.reuse_connection</a>    | "1"    | PHP\_INI\_ALL    | Available since ingres 2.0.0  |
| <a href="/book/ingres.html#" class="link">ingres.scrollable</a>          | "1"    | PHP\_INI\_ALL    | Available since ingres 2.0.0. |
| <a href="/book/ingres.html#" class="link">ingres.trace</a>               | "0"    | PHP\_INI\_ALL    | Available since ingres 2.0.0. |
| <a href="/book/ingres.html#" class="link">ingres.trace_connect</a>       | "0"    | PHP\_INI\_ALL    | Available since ingres 1.2.1. |
| <a href="/book/ingres.html#" class="link">ingres.utf8</a>                | "1"    | PHP\_INI\_ALL    | Available since ingres 2.0.0. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`ingres.allow_persistent` <span class="type">bool</span>  
Specifies whether to allow
<a href="/features/persistent-connections.html" class="link">persistent connections</a>
to Ingres

`ingres.array_index_start` <span class="type">int</span>  
Specifies the start value for an integer key for arrays generated by
<span class="function">ingres\_fetch\_row</span> or <span
class="function">ingres\_fetch\_array</span>. By default
`ingres.array_index_start` is set to 1. If you wish to make the ingres
extension behave like other database extensions set this configuration
option to 0.

`ingres.auto` <span class="type">bool</span>  
Enables or disables autocommit emulation. Ingres cannot have multiple
cursors open with autocommit enabled. When enabled, the driver emulates
autocommit.

`ingres.blob_segment_length` <span class="type">int</span>  
Specifies the amount of memory to use when reading BLOB data, in bytes

`ingres.cursor_mode` <span class="type">int</span>  
Specifies the default mode for cursors opened with ingres\_prepare().
Valid values are **`INGRES_CURSOR_UPDATE`** or
**`INGRES_CURSOR_READONLY`**.

`ingres.default_database` <span class="type">string</span>  
Specifies the default database name to use when connecting to the
database server if no other name is specified. Does not apply in
<a href="/ini/core.html#ini.sql.safe-mode" class="link">SQL 安全模式</a>.

`ingres.default_password` <span class="type">string</span>  
Specifies the default password to use when connecting to the database
server if no other name is specified. Does not apply in
<a href="/ini/core.html#ini.sql.safe-mode" class="link">SQL 安全模式</a>.

`ingres.default_user` <span class="type">string</span>  
Specifies the default user name to use when connecting to the database
server if no other name is specified. Does not apply in
<a href="/ini/core.html#ini.sql.safe-mode" class="link">SQL 安全模式</a>.

`ingres.describe` <span class="type">bool</span>  
Enables the use of *DESCRIBE INPUT* to determine the expected data types
for queries that use parameters. Available with Ingres 9.1.0 and later.
When disabled, queries that have parameters passed may need to manually
describe the types of those parameters using the
<a href="/book/ingres.html#" class="link">types</a> parameter in <span
class="function">ingres\_query</span>.

> **Note**:
>
> Enabling this feature with <span class="function">ingres\_query</span>
> will cause additional communications traffic between this extension
> and the server. To minimize this additional traffic, use <span
> class="function">ingres\_prepare</span> and <span
> class="function">ingres\_execute</span>.

`ingres.fetch_buffer_size` <span class="type">int</span>  
Specifies the number of pre-fetch rows that <span
class="function">ingres\_fetch\_array</span>, <span
class="function">ingres\_fetch\_object</span> and <span
class="function">ingres\_fetch\_row</span> will try and fetch in one
fetch operation.

`ingres.max_links` <span class="type">int</span>  
Specifies the maximum number of Ingres sessions allowed per process or
thread. The number of sessions should not exceed the total number of
connected sessions configured within Ingres.

`ingres.max_persistent` <span class="type">int</span>  
Specifies the maximum number of persistent Ingres sessions allowed per
process or thread. The number of sessions should not exceed the total
number of connected sessions configured within Ingres.

`ingres.reuse_connection` <span class="type">bool</span>  
Reuses an existing active connection if connecting to the same database
with the same user name

`ingres.scrollable` <span class="type">bool</span>  
Enables support for scrollable cursors. When fetching CLOB or BLOB data,
this should be set to **`FALSE`**. Available with Ingres 9.2.0 or later.

`ingres.trace` <span class="type">bool</span>  
Enables simple tracing using **`E_NOTICE`** messages

`ingres.trace_connect` <span class="type">bool</span>  
Prints **`E_NOTICE`** messages during <span
class="function">ingres\_connect</span> or <span
class="function">ingres\_pconnect</span> calls

`ingres.utf8` <span class="type">bool</span>  
Assumes that strings being passed to National Character column types
(*NVARCHAR* or *NCHAR*) are using UTF8 encoding and converts them to
UTF16 for the server

资源类型
--------

<span class="function">ingres\_connect</span> and <span
class="function">ingres\_pconnect</span> return an Ingres link
identifier.

<span class="function">ingres\_query</span> and <span
class="function">ingres\_unbuffered\_query</span> return an Ingres
result identifier.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`INGRES_ASSOC`** (<span class="type">int</span>)  
<span class="simpara"> Columns are returned into the array having the
fieldname as the array index. Used with <span
class="function">ingres\_fetch\_array</span>. </span>

**`INGRES_NUM`** (<span class="type">int</span>)  
<span class="simpara"> Columns are returned into the array having a
numerical index to the fields. By default this index starts at 1, the
first field in the result. To change this value, see
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
Used with <span class="function">ingres\_fetch\_array</span>. </span>

**`INGRES_BOTH`** (<span class="type">int</span>)  
<span class="simpara"> Columns are returned into the array having both a
numerical index and the fieldname as the array index. Used with <span
class="function">ingres\_fetch\_array</span>. </span>

**`INGRES_EXT_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the version of the Ingres Extension.
Available since version 1.2.0 of the PECL extension. </span>

**`INGRES_API_VERSION`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the version of Ingres OpenAPI that the
extension was built against. Available since version 1.2.0 of the PECL
extension. </span>

**`INGRES_CURSOR_READONLY`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that Ingres cursors should be opened in
"readonly" mode. Available since version 1.2.0 of the PECL extension.
Used with
<a href="/book/ingres.html#" class="link">ingres.cursor_mode</a>.
</span>

**`INGRES_CURSOR_UPDATE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies that Ingres cursors should be opened
"for update." Available since version 1.2.0 of the PECL extension. Used
with <a href="/book/ingres.html#" class="link">ingres.cursor_mode</a>.
</span>

**`INGRES_DATE_MULTINATIONAL`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
MULTINATIONAL. Available since version 1.2.0 of the PECL extension. Used
with <span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_MULTINATIONAL4`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
MULTINATIONAL4. Available since version 1.2.0 of the PECL extension.
Used with <span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_FINNISH`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
FINNISH. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_ISO`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
ISO. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_ISO4`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
ISO4. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_GERMAN`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
GERMAN. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_MDY`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
MDY. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_DMY`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
DMY. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_DATE_YMD`** (<span class="type">int</span>)  
<span class="simpara"> Equivalent to the II\_DATE\_FORMAT setting of
YMD. Available since version 1.2.0 of the PECL extension. Used with
<span class="function">ingres\_connect</span>, <span
class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_MONEY_LEADING`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the currency character that should be
placed at the start of a money value. Equivalent to setting
II\_MONEY\_FORMAT to "L:". Available since version 1.2.0 of the PECL
extension. Used with <span class="function">ingres\_connect</span>,
<span class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_MONEY_TRAILING`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the currency character that should be
placed at the end of a money value. Equivalent to setting
II\_MONEY\_FORMAT to "T:". Available since version 1.2.0 of the PECL
extension. Used with <span class="function">ingres\_connect</span>,
<span class="function">ingres\_pconnect</span> and <span
class="function">ingres\_set\_environment</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_set\_environment</span>. </span>

**`INGRES_STRUCTURE_BTREE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table or index structure to
BTREE when used in combination with the options or index\_structure
option when connecting. Available since version 1.4.0 of the PECL
extension. Used with <span class="function">ingres\_connect</span> and
<span class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_CBTREE`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table or index structure to
COMPRESSED BTREE when used in combination with the options or
index\_structure option when connecting. Available since version 1.4.0
of the PECL extension. Used with <span
class="function">ingres\_connect</span> and <span
class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_HASH`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table or index structure to
HASH when used in combination with the options or index\_structure
option when connecting. Available since version 1.4.0 of the PECL
extension. Used with <span class="function">ingres\_connect</span> and
<span class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_CHASH`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table or index structure to
COMPRESSED HASH when used in combination with the options or
index\_structure option when connecting. Available since version 1.4.0
of the PECL extension. Used with <span
class="function">ingres\_connect</span> and <span
class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_HEAP`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table structure to HEAP
when used in combination with the options option when connecting.
Available since version 1.4.0 of the PECL extension. Used with <span
class="function">ingres\_connect</span> and <span
class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_CHEAP`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table structure to
COMPRESSED HEAP when used in combination with the options option when
connecting. Available since version 1.4.0 of the PECL extension. Used
with <span class="function">ingres\_connect</span> and <span
class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_ISAM`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table or index structure to
ISAM when used in combination with the options or index\_structure
option when connecting. Available since version 1.4.0 of the PECL
extension. Used with <span class="function">ingres\_connect</span> and
<span class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

**`INGRES_STRUCTURE_CISAM`** (<span class="type">int</span>)  
<span class="simpara"> Specifies the default table or index structure to
COMPRESSED ISAM when used in combination with the options or
index\_structure option when connecting. Available since version 1.4.0
of the PECL extension. Used with <span
class="function">ingres\_connect</span> and <span
class="function">ingres\_pconnect</span>. See
<a href="/book/ingres.html#" class="link">options</a> in <span
class="function">ingres\_connect</span>. </span>

范例
====

**目录**

-   [Basic usage](/book/ingres.html#Basic%20usage)

Basic usage
-----------

The following simple example shows how to connect to an Ingres database,
execute a query, print resulting rows and disconnect from the database.

**示例 \#1 Simple Ingres Example**

``` php
<?php
// Connecting, selecting database
$link = ingres_connect("database", "user", "password")
    or die("Could not connect: " . ingres_error($link));
echo "Connected successfully";

// Select from a table that exists in all Ingres databases
$query = "SELECT * FROM iitables";
$result = ingres_query($link,$query) or die("Query failed: " .
ingres_error($link));

// Print results in HTML
// relid - table name
// relowner - table owner
echo "<table>\n";
while ($iitables = ingres_fetch_object($result)) {
    echo "\t<tr>\n";
    echo "\t\t<td>" . $iitables->relid . "</td>\n";
    echo "\t\t<td>" . $iitables->relowner . "</td>\n";
    echo "\t</tr>\n";
}
echo "</table>\n";

// Free results
ingres_free_result($result);

// Commit transaction
ingres_commit($link);

// Closing connection
ingres_close($link);
?>
```

ingres\_autocommit\_state
=========================

Test if the connection is using autocommit

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_autocommit\_state</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">ingres\_autocommit\_state</span> is called to
determine whether the current link has autocommit enabled or not.

### 参数

`link`  
The connection link identifier

### 返回值

Returns **`TRUE`** if autocommit is enabled or **`FALSE`** when
autocommit is disabled

### 参见

-   <span class="function">ingres\_autocommit</span>
-   <span class="function">ingres\_query</span>

ingres\_autocommit
==================

Switch autocommit on or off

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_autocommit</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">ingres\_autocommit</span> is called before
opening a transaction (before the first call to <span
class="function">ingres\_query</span> or just after a call to <span
class="function">ingres\_rollback</span> or <span
class="function">ingres\_commit</span>) to switch the autocommit mode of
the server on or off (when the script begins the autocommit mode is
off).

When autocommit mode is on, every query is automatically committed by
the server, as if <span class="function">ingres\_commit</span> was
called after every call to <span class="function">ingres\_query</span>.
To see if autocommit is enabled use, <span
class="function">ingres\_autocommit\_state</span>.

By default Ingres will rollback any uncommitted transactions at the end
of a request. Use this function or <span
class="function">ingres\_commit</span> to ensure your data is committed
to the database.

### 参数

`link`  
The connection link identifier

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ingres\_autocommit\_state</span>
-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_rollback</span>
-   <span class="function">ingres\_commit</span>

ingres\_charset
===============

Returns the installation character set

### 说明

<span class="type">string</span> <span
class="methodname">ingres\_charset</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">ingres\_charset</span> is called to determine the
character set being used by the Ingres client, from II\_CHARSETxx (where
xx is the installation code).

> **Note**:
>
> You can override the value returned by using the function <span
> class="function">putenv</span>. Changing the value of II\_CHARSETxx in
> a running Ingres installation can cause data corruption.

### 参数

`link`  
The connection link identifier

### 返回值

Returns a string with the value for II\_CHARSETxx or returns NULL if the
value could not be determined.

### 范例

**示例 \#1 <span class="function">ingres\_charset</span> - Get the
installation character set**

``` php
<?php
$link = ingres_connect($database, $user, $password);

echo ingres_charset($link) . "\n";

ingres_close($link);
?>
```

### 参见

-   <span class="function">ingres\_connect</span>
-   <span class="function">ingres\_query</span>

ingres\_close
=============

Close an Ingres database connection

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">ingres\_close</span> closes the connection to the
Ingres server that is associated with the specified link.

<span class="function">ingres\_close</span> is usually unnecessary, as
it will not close persistent connections and all non-persistent
connections are automatically closed at the end of the script.

### 参数

`link`  
The connection link identifier

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ingres\_connect</span>
-   <span class="function">ingres\_pconnect</span>

ingres\_commit
==============

Commit a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_commit</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">ingres\_commit</span> commits the currently open
transaction, making all changes made to the database permanent.

This closes the transaction. A new transaction can be opened by sending
a query with <span class="function">ingres\_query</span>.

You can also have the server commit automatically after every query by
calling <span class="function">ingres\_autocommit</span> before opening
the transaction.

By default Ingres will roll back any uncommitted transactions at the end
of a request. Use this function or <span
class="function">ingres\_autocommit</span> to ensure your that data is
committed to the database.

### 参数

`link`  
The connection link identifier

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_rollback</span>
-   <span class="function">ingres\_autocommit</span>

ingres\_connect
===============

Open a connection to an Ingres database

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">ingres\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$database`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\]\]\] )

<span class="function">ingres\_connect</span> opens a connection with
the given Ingres `database`.

The connection is closed when the script ends or when <span
class="function">ingres\_close</span> is called on this link.

### 参数

If some parameters are missing, <span
class="function">ingres\_connect</span> uses the values in `php.ini` for
`ingres.default_database`, `ingres.default_user` and
`ingres.default_password`.

`database`  
The database name. Must follow the syntax:

`[vnode::]dbname[/svr_class]`

`username`  
The Ingres user name

`password`  
The password associated with `username`

`options`  
<span class="function">ingres\_connect</span> options

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Option name</th>
<th>Option type</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>date_century_boundary</td>
<td><span class="type">int</span></td>
<td>The threshold by which a 2-digit year is determined to be in the current century or in the next century. Equivalent to II_DATE_CENTURY_BOUNDARY.</td>
<td>50</td>
</tr>
<tr class="even">
<td>group</td>
<td><span class="type">string</span></td>
<td>Specifies the group ID of the user, equivalent to the "-G" flag</td>
<td>payroll</td>
</tr>
<tr class="odd">
<td>role</td>
<td><span class="type">string</span></td>
<td>The role ID of the application. If a role password is required, the parameter value should be specified as "role/password"</td>
<td></td>
</tr>
<tr class="even">
<td>effective_user</td>
<td><span class="type">string</span></td>
<td>The ingres user account being impersonated, equivalent to the "-u" flag</td>
<td>another_user</td>
</tr>
<tr class="odd">
<td>dbms_password</td>
<td><span class="type">string</span></td>
<td>The internal database password for the user connecting to Ingres</td>
<td>s3cr3t</td>
</tr>
<tr class="even">
<td>table_structure</td>
<td><span class="type">string</span></td>
<td><p>The default structure for new tables. Valid values for table_structure are:</p>
<ul>
<li><span class="simpara">INGRES_STRUCTURE_BTREE</span></li>
<li><span class="simpara">INGRES_STRUCTURE_HASH</span></li>
<li><span class="simpara">INGRES_STRUCTURE_HEAP</span></li>
<li><span class="simpara">INGRES_STRUCTURE_ISAM</span></li>
<li><span class="simpara">INGRES_STRUCTURE_CBTREE</span></li>
<li><span class="simpara">INGRES_STRUCTURE_CISAM</span></li>
<li><span class="simpara">INGRES_STRUCTURE_CHASH</span></li>
<li><span class="simpara">INGRES_STRUCTURE_CHEAP</span></li>
</ul></td>
<td>INGRES_STRUCTURE_BTREE</td>
</tr>
<tr class="odd">
<td>index_structure</td>
<td><span class="type">string</span></td>
<td><p>The default structure for new secondary indexes. Valid values for index_structure are:</p>
<ul>
<li><span class="simpara">INGRES_STRUCTURE_CBTREE</span></li>
<li><span class="simpara">INGRES_STRUCTURE_CISAM</span></li>
<li><span class="simpara">INGRES_STRUCTURE_CHASH</span></li>
<li><span class="simpara">INGRES_STRUCTURE_BTREE</span></li>
<li><span class="simpara">INGRES_STRUCTURE_HASH</span></li>
<li><span class="simpara">INGRES_STRUCTURE_ISAM</span></li>
</ul></td>
<td>INGRES_STRUCTURE_HASH</td>
</tr>
<tr class="even">
<td>login_local</td>
<td><span class="type">bool</span></td>
<td>Determines how the connection user ID and password are used when a VNODE is included in the target database string. If set to TRUE, the user ID and password are used to locally access the VNODE, and the VNODE login information is used to establish the DBMS connection. If set to FALSE, the process user ID is used to access the VNODE, and the connection user ID and password are used in place of the VNODE login information to establish the DBMS connection. This parameter is ignored if no VNODE is included in the target database string. The default is FALSE.</td>
<td>TRUE</td>
</tr>
<tr class="odd">
<td>timezone</td>
<td><span class="type">string</span></td>
<td>Controls the timezone of the session. If not set it will default to the value defined by II_TIMEZONE_NAME. If II_TIMEZONE_NAME is not defined, NA-PACIFIC (GMT-8 with Daylight Savings) is used.</td>
<td></td>
</tr>
<tr class="even">
<td>date_format</td>
<td><span class="type">int</span></td>
<td><p>Sets the allowable input and output format for Ingres dates. Defaults to the value defined by II_DATE_FORMAT. If II_DATE_FORMAT is not set the default date format is US, e.g. mm/dd/yy. Valid values for date_format are:</p>
<ul>
<li><span class="simpara">INGRES_DATE_DMY</span></li>
<li><span class="simpara">INGRES_DATE_FINISH</span></li>
<li><span class="simpara">INGRES_DATE_GERMAN</span></li>
<li><span class="simpara">INGRES_DATE_ISO</span></li>
<li><span class="simpara">INGRES_DATE_ISO4</span></li>
<li><span class="simpara">INGRES_DATE_MDY</span></li>
<li><span class="simpara">INGRES_DATE_MULTINATIONAL</span></li>
<li><span class="simpara">INGRES_DATE_MULTINATIONAL4</span></li>
<li><span class="simpara">INGRES_DATE_YMD</span></li>
<li><span class="simpara">INGRES_DATE_US</span></li>
</ul></td>
<td>INGRES_DATE_MULTINATIONAL4</td>
</tr>
<tr class="odd">
<td>decimal_separator</td>
<td><span class="type">string</span></td>
<td>The character identifier for decimal data</td>
<td>","</td>
</tr>
<tr class="even">
<td>money_lort</td>
<td><span class="type">int</span></td>
<td><p>Leading or trailing currency sign. Valid values for money_lort are:</p>
<ul>
<li><span class="simpara">INGRES_MONEY_LEADING</span></li>
<li><span class="simpara">INGRES_MONEY_TRAILING</span></li>
</ul></td>
<td>INGRES_MONEY_TRAILING</td>
</tr>
<tr class="odd">
<td>money_sign</td>
<td><span class="type">string</span></td>
<td>The currency symbol to be used with the MONEY datatype</td>
<td>€</td>
</tr>
<tr class="even">
<td>money_precision</td>
<td><span class="type">int</span></td>
<td>The precision of the MONEY datatype</td>
<td>3</td>
</tr>
<tr class="odd">
<td>float4_precision</td>
<td><span class="type">int</span></td>
<td>Precision of the FLOAT4 datatype</td>
<td>10</td>
</tr>
<tr class="even">
<td>float8_precision</td>
<td><span class="type">int</span></td>
<td>Precision of the FLOAT8 data</td>
<td>10</td>
</tr>
<tr class="odd">
<td>blob_segment_length</td>
<td><span class="type">int</span></td>
<td>The amount of data in bytes to fetch at a time when retrieving BLOB or CLOB data, defaults to 4096 bytes when not explicitly set</td>
<td>8192</td>
</tr>
</tbody>
</table>

### 返回值

Returns a Ingres link resource on success 或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 Open a connection to an Ingres database**

``` php
<?php
$link = ingres_connect("mydb", "user", "pass")
    or die("Could not connect");
echo "Connected successfully";
ingres_close($link);
?>
```

### 参见

-   <span class="function">ingres\_pconnect</span>
-   <span class="function">ingres\_close</span>

ingres\_cursor
==============

Get a cursor name for a given result resource

### 说明

<span class="type">string</span> <span
class="methodname">ingres\_cursor</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

Returns a string with the active cursor name. If no cursor is active
then NULL is returned.

### 参数

`result`  
The query result identifier

### 返回值

Returns a string containing the active cursor name. If no cursor is
active then NULL is returned.

### 范例

**示例 \#1 Get cursor name for a query resource**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_prepare($link, "select * from table");

$cursor_name = ingres_cursor($result);

echo $cursor_name;

?>
```

### 参见

-   <span class="function">ingres\_prepare</span>
-   <span class="function">ingres\_execute</span>

ingres\_errno
=============

Get the last Ingres error number generated

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_errno</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$link`</span> \]
)

Returns an integer containing the last error number. If no error was
reported 0 is returned.

If a `link` resource is passed to <span
class="function">ingres\_errno</span> it returns the last error recorded
for the link. If no link is passed, then <span
class="function">ingres\_errno</span> returns the last error reported
using the default link.

The function, <span class="function">ingres\_errno</span>, should always
be called after executing a database query. Calling another function
before <span class="function">ingres\_errno</span> is called will reset
or change any error code from the last Ingres function call.

### 参数

`link`  
The connection link identifier

### 返回值

Returns an integer containing the last error number. If no error was
reported, 0 is returned.

### 范例

**示例 \#1 Get the last Ingres error number generated**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link, "select * from table");

$error_code = ingres_errno($link);

if ( $error_code != 0 ) {
   echo "An error occurred - " . $error_code;
}
?>
```

### 参见

-   <span class="function">ingres\_error</span>
-   <span class="function">ingres\_errsqlstate</span>
-   <span class="function">ingres\_next\_error</span>

ingres\_error
=============

Get a meaningful error message for the last error generated

### 说明

<span class="type">string</span> <span
class="methodname">ingres\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$link`</span> \]
)

Returns a string containing the last error, or NULL if no error has
occurred.

If a `link` resource is passed to <span
class="function">ingres\_error</span>, it returns the last error
recorded for the link. If no link is passed then <span
class="function">ingres\_error</span> returns the last error reported
using the default link.

The function, <span class="function">ingres\_error</span>, should always
be called after executing any database query. Calling another function
before <span class="function">ingres\_error</span> is called will reset
or change any error message from the last Ingres function call.

### 参数

`link`  
The connection link identifier

### 返回值

Returns a string containing the last error, or NULL if no error has
occurred.

### 范例

**示例 \#1 Get a message for the last error generated**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link, "select * from table");

$error_text = ingres_error();

if (!is_null($error_text)) {
   echo "An error occurred - " . $error_text;
}
?>
```

### 参见

-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_errsqlstate</span>
-   <span class="function">ingres\_next\_error</span>

ingres\_errsqlstate
===================

Get the last SQLSTATE error code generated

### 说明

<span class="type">string</span> <span
class="methodname">ingres\_errsqlstate</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$link`</span> \]
)

Returns a string containing the last SQLSTATE, or NULL if no error has
occurred.

If a `link` resource is passed to <span
class="function">ingres\_errsqlstate</span>, it returns the last error
recorded for the link. If no link is passed, then <span
class="function">ingres\_errsqlstate</span> returns the last error
reported using the default link.

The function, <span class="function">ingres\_errsqlstate</span>, should
always be called after executing any database query. Calling another
function before <span class="function">ingres\_errsqlstate</span> is
called will reset or change any error message from the last Ingres
function call.

### 参数

`link`  
The connection link identifier

### 返回值

Returns a string containing the last SQLSTATE, or NULL if no error has
occurred.

### 范例

**示例 \#1 Get the last SQLSTATE error code generated**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link, "select * from table");

$error_sqlstate = ingres_errsqlstate($link);

if (!is_null($error_sqlstate)) {
   echo "An error occurred - " . $error_sqlstate;
}
?>
```

### 参见

-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_error</span>
-   <span class="function">ingres\_next\_error</span>

ingres\_escape\_string
======================

Escape special characters for use in a query

### 说明

<span class="type">string</span> <span
class="methodname">ingres\_escape\_string</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$source_string`</span> )

<span class="function">ingres\_escape\_string</span> is used to escape
certain characters within a string before it is sent to the database
server.

### 参数

`link`  
The connection link identifier

`source_string`  
The source string to be parsed

### 返回值

Returns a string containing the escaped data.

### 范例

**示例 \#1 Escape special characters for use in a query**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$last_name = "O'Connor";

$sql = sprintf("select * from user_profile where up_last = '%s'", ingres_escape_string( $link, $last_name));

$result = ingres_query($link, $sql);

while ($user = ingres_fetch_object($result))
{
  echo $user->up_first . '<BR/>';
}

ingres_commit($link);

ingres_close($link);

?>
```

### 参见

-   <span class="function">ingres\_query</span>

ingres\_execute
===============

Execute a prepared query

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_execute</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$params`</span> \[, <span class="methodparam"><span
class="type">string</span> `$types`</span> \]\] )

Execute a query prepared using <span
class="function">ingres\_prepare</span>.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.describe</a>,
> <a href="/book/ingres.html#" class="link">ingres.scrollable</a> and
> <a href="/book/ingres.html#" class="link">ingres.utf8</a> directives
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`result`  
The result query identifier

`params`  
An array of parameter values to be used with the query

`types`  
A string containing a sequence of types for the parameter values passed.
See the <a href="/book/ingres.html#" class="link">types</a> parameter in
<span class="function">ingres\_query</span> for the list of type codes.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ingres\_unbuffered\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>
-   <span class="function">ingres\_commit</span>
-   <span class="function">ingres\_rollback</span>
-   <span class="function">ingres\_autocommit</span>
-   <span class="function">ingres\_set\_environment</span>
-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_error</span>

ingres\_fetch\_array
====================

Fetch a row of result into an array

### 说明

<span class="type">array</span> <span
class="methodname">ingres\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`</span> \] )

This function is an extended version of <span
class="function">ingres\_fetch\_row</span>. In addition to storing the
data in the numeric indices of the result array, it also stores the data
in associative indices, using the field names as keys.

If two or more columns of the result have the same field names, the last
column will take precedence. To access the another column or columns of
the same name, you must use the numeric index of the column or make an
alias for the column. For example:

``` php
<?php

$result = ingres_query($link, "select ap_place as city, ap_ccode as country from airport where ap_iatacode = 'VLL'"); 
$result = ingres_fetch_array($result);
$foo = $result["city"];
$bar = $result["country"];

?>
```

With regard to speed, the function is identical to <span
class="function">ingres\_fetch\_object</span>, and almost as quick as
<span class="function">ingres\_fetch\_row</span> (the difference is
insignificant).

By default, arrays created by <span
class="function">ingres\_fetch\_array</span> start from position 1 and
not 0 as with other DBMS extensions. The starting position can be
adjusted to 0 using the configuration parameter
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>,
> <a href="/book/ingres.html#" class="link">ingres.fetch_buffer_size</a>
> and <a href="/book/ingres.html#" class="link">ingres.utf8</a>
> directives in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`result`  
The query result identifier

`result_type`  
The result type. This `result_type` can be **`INGRES_NUM`** for
enumerated array, **`INGRES_ASSOC`** for associative array, or
**`INGRES_BOTH`** (default).

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows

### 范例

**示例 \#1 Fetch a row of result into an array**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link,"select * from table");
while ($row = ingres_fetch_array($result)) {
    echo $row["user_id"];  // using associative array
    echo $row["fullname"];
    echo $row[1];          // using enumerated array
    echo $row[2];
}
?>
```

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_num\_fields</span>
-   <span class="function">ingres\_field\_name</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_fetch\_assoc
====================

Fetch a row of result into an associative array

### 说明

<span class="type">array</span> <span
class="methodname">ingres\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

This function is stores the data fetched from a query executed using
<span class="function">ingres\_query</span> in an associative array,
using the field names as keys.

With regard to speed, the function is identical to <span
class="function">ingres\_fetch\_object</span>, and almost as quick as
<span class="function">ingres\_fetch\_row</span> (the difference is
insignificant).

By default, arrays created by <span
class="function">ingres\_fetch\_assoc</span> start from position 1 and
not 0 as with other DBMS extensions. The starting position can be
adjusted to 0 using the configuration parameter
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>,
> <a href="/book/ingres.html#" class="link">ingres.fetch_buffer_size</a>
> and <a href="/book/ingres.html#" class="link">ingres.utf8</a>
> directives in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`result`  
The query result identifier

### 返回值

Returns an associative array that corresponds to the fetched row, or
**`FALSE`** if there are no more rows

### 范例

**示例 \#1 Fetch a row into an associative array**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link,"select * from table");
while ($row = ingres_fetch_assoc($result)) {
    echo $row["user_id"];  // using associative array
    echo $row["fullname"];
}
?>
```

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_num\_fields</span>
-   <span class="function">ingres\_field\_name</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_fetch\_object
=====================

Fetch a row of result into an object

### 说明

<span class="type">object</span> <span
class="methodname">ingres\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$result_type`</span> \] )

This function is similar to <span
class="function">ingres\_fetch\_array</span>, with one difference - an
object is returned instead of an array. Indirectly, this means that you
can access the data only by the field names and not by their offsets
(numbers are illegal property names).

With regard to speed, the function is identical to <span
class="function">ingres\_fetch\_array</span>, and almost as quick as
<span class="function">ingres\_fetch\_row</span> (the difference is
insignificant).

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.fetch_buffer_size</a>
> and <a href="/book/ingres.html#" class="link">ingres.utf8</a>
> directives in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`link`  
The query result identifier

`result_type`  
(Optional argument.) `result_type` is a constant and can take the
following values: **`INGRES_ASSOC`**, **`INGRES_NUM`**, and
**`INGRES_BOTH`**.

### 返回值

Returns an object that corresponds to the fetched row, or **`FALSE`** if
there are no more rows

### 范例

**示例 \#1 Fetch a row into an object**

``` php
<?php
$link = ingres_connect($database, $user, $password);
$result = ingres_query($link, "select * from table");
while ($row = ingres_fetch_object($result)) {
    echo $row->user_id;
    echo $row->fullname;
}
?>
```

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_num\_fields</span>
-   <span class="function">ingres\_field\_name</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_fetch\_proc\_return
===========================

Get the return value from a procedure call

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_fetch\_proc\_return</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

This function is used to retrieve the return value following the
execution of an Ingres database procedure (stored procedure).

> **Note**:
>
> If used with a row-producing procedure, this function should be called
> after all the rows from the procedure have been fetched using <span
> class="function">ingres\_fetch\_array</span>, <span
> class="function">ingres\_fetch\_object</span> or <span
> class="function">ingres\_fetch\_row</span>. This function will
> eliminate any rows yet to be fetched should there be any left over.

### 参数

`result`  
The result identifier for a query

### 返回值

Returns an <span class="type">int</span> if there is a return value
otherwise it will return **`NULL`**.

### 范例

**示例 \#1 Get the return value from a procedure call**

``` php
<?php

$link = ingres_connect($database);

if ( ingres_errno() != 0 ) {
    $error_text = ingres_error();
    die($error_text);
}

$result = ingres_query($link, "execute procedure php_proc (value = 1000)");

if ( ingres_errno() != 0 ) {
    $error_text = ingres_error();
    die($error_text);
}

echo "return value - " . ingres_fetch_proc_return($result) . "\n";

ingres_close($link);

?>
```

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_fetch\_row
==================

Fetch a row of result into an enumerated array

### 说明

<span class="type">array</span> <span
class="methodname">ingres\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">ingres\_fetch\_row</span> returns an array that
corresponds to the fetched row, or **`FALSE`** if there are no more
rows. Each result column is stored in an array offset, starting at
offset 1.

Subsequent calls to <span class="function">ingres\_fetch\_row</span>
return the next row in the result set, or **`FALSE`** if there are no
more rows.

By default, arrays created by <span
class="function">ingres\_fetch\_row</span> start from position 1 and not
0 as with other DBMS extensions. The starting position can be adjusted
to 0 using the configuration parameter
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>,
> <a href="/book/ingres.html#" class="link">ingres.fetch_buffer_size</a>
> and <a href="/book/ingres.html#" class="link">ingres.utf8</a>
> directives in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`result`  
The query result identifier

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows

### 范例

**示例 \#1 Fetch a row of result into an enumerated array**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link, "select * from table");
while ($row = ingres_fetch_row($result)) {
    echo $row[1];
    echo $row[2];
}
?>
```

### 参见

-   <span class="function">ingres\_num\_fields</span>
-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>

ingres\_field\_length
=====================

Get the length of a field

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_field\_length</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

<span class="function">ingres\_field\_length</span> returns the length
of a field. This is the number of bytes the server uses to store the
field. For detailed information, see the Ingres *OpenAPI User Guide*,
Appendix *"Data Types"* in the Ingres documentation.

> **Note**: **Related Configurations**  
>
> See
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`result`  
The query result identifier

`index`  
`index` is the column number whose length will be retrieved.

The possible values of `index` depend upon the value of
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *1* (the default) then `index` must be between *1* and the value
returned by <span class="function">ingres\_num\_fields</span>. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *0* then `index` must be between *0* and <span
class="function">ingres\_num\_fields</span> *- 1*.

### 返回值

Returns the length of a field.

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_field\_name
===================

Get the name of a field in a query result

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">ingres\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

<span class="function">ingres\_field\_name</span> returns the name of a
field in a query result.

> **Note**: **Related Configurations**  
>
> See
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`result`  
The query result identifier

`index`  
`index` is the field whose name will be retrieved.

The possible values of `index` depend upon the value of
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *1* (the default) then `index` must be between *1* and the value
returned by <span class="function">ingres\_num\_fields</span>. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *0* then `index` must be between *0* and <span
class="function">ingres\_num\_fields</span> *- 1*.

### 返回值

Returns the name of a field in a query result 或者在失败时返回
**`FALSE`**

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_field\_nullable
=======================

Test if a field is nullable

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_field\_nullable</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

Test if a field is nullable.

> **Note**: **Related Configurations**  
>
> See
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`result`  
The query result identifier

`index`  
`index` is the field whose nullability will be retrieved.

The possible values of `index` depend upon the value of
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *1* (the default) then `index` must be between *1* and the value
returned by <span class="function">ingres\_num\_fields</span>. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *0* then `index` must be between *0* and <span
class="function">ingres\_num\_fields</span> *- 1*.

### 返回值

<span class="function">ingres\_field\_nullable</span> returns **`TRUE`**
if the field can be set to the **`NULL`** value and **`FALSE`** if it
cannot

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_field\_precision
========================

Get the precision of a field

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_field\_precision</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

<span class="function">ingres\_field\_precision</span> returns the
precision of a field. This value is used only for decimal, float, and
money SQL data types. For detailed information, see the Ingres *OpenAPI
User Guide*, Appendix "Data Types" in the Ingres documentation.

> **Note**: **Related Configurations**  
>
> See
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`result`  
The query result identifier

`index`  
`index` is the field whose precision will be retrieved.

The possible values of `index` depend upon the value of
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *1* (the default) then `index` must be between *1* and the value
returned by <span class="function">ingres\_num\_fields</span>. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *0* then `index` must be between *0* and <span
class="function">ingres\_num\_fields</span> *- 1*.

### 返回值

Returns the field precision as an integer

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_field\_scale
====================

Get the scale of a field

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_field\_scale</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

<span class="function">ingres\_field\_scale</span> returns the scale of
a field. This value is used only for the decimal SQL data type. For
detailed information, see the Ingres *OpenAPI User Guide*, Appendix
*"Data Types"* in the Ingres documentation.

> **Note**: **Related Configurations**  
>
> See
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`result`  
The query result identifier

`index`  
`index` is the field whose scale will be retrieved.

The possible values of `index` depend upon the value of
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *1* (the default) then `index` must be between *1* and the value
returned by <span class="function">ingres\_num\_fields</span>. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *0* then `index` must be between *0* and <span
class="function">ingres\_num\_fields</span> *- 1*.

### 返回值

Returns the scale of the field, as an integer

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_field\_type
===================

Get the type of a field in a query result

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">ingres\_field\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> )

Get the type of a field in a query result.

> **Note**: **Related Configurations**  
>
> See
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`result`  
The query result identifier

`index`  
`index` is the field whose type will be retrieved.

The possible values of `index` depend upon the value of
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>.
If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *1* (the default) then `index` must be between *1* and the value
returned by <span class="function">ingres\_num\_fields</span>. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is *0* then `index` must be between *0* and <span
class="function">ingres\_num\_fields</span> *- 1*.

### 返回值

<span class="function">ingres\_field\_type</span> returns the type of a
field in a query result 或者在失败时返回 **`FALSE`**. Examples of types
returned are *IIAPI\_BYTE\_TYPE*, *IIAPI\_CHA\_TYPE*,
*IIAPI\_DTE\_TYPE*, *IIAPI\_FLT\_TYPE*, *IIAPI\_INT\_TYPE*,
*IIAPI\_VCH\_TYPE*. Some of these types can map to more than one SQL
type depending on the length of the field (see <span
class="function">ingres\_field\_length</span>). For example
IIAPI\_FLT\_TYPE can be a float4 or a float8. For detailed information,
see the Ingres *OpenAPI User Guide*, Appendix "Data Types" in the Ingres
documentation.

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_free\_result
====================

Free the resources associated with a result identifier

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

### 参数

`result`  
The query result identifier

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Free a result resource**

``` php
<?php
$link = ingres_connect($database, $user, $password);

$result = ingres_query($link, "select * from table");

while ($row = ingres_fetch_row($result)) {
    echo $row[1];
    echo $row[2];
}
ingres_free_result($result);

ingres_close($link)

?>
```

### 参见

-   <span class="function">ingres\_query</span>

ingres\_next\_error
===================

Get the next Ingres error

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_next\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$link`</span> \]
)

Get the next Ingres error for the last executed query. Each call to
<span class="function">ingres\_next\_error</span> can be followed by a
call to <span class="function">ingres\_errno</span>, <span
class="function">ingres\_error</span> or <span
class="function">ingres\_errsqlstate</span> to get the respective error
number, error text, or SQL STATE. While <span
class="function">ingres\_next\_error</span> returns **`TRUE`**, there
are more errors to fetch.

### 参数

`link`  
The connection link identifier

### 返回值

<span class="function">ingres\_next\_error</span> returns **`TRUE`** if
there is another error to retrieve or **`FALSE`** when there are no more
errors

### 参见

-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_error</span>
-   <span class="function">ingres\_errsqlstate</span>

ingres\_num\_fields
===================

Get the number of fields returned by the last query

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">ingres\_num\_fields</span> returns the number of
fields in the results returned by the Ingres server after a call to
<span class="function">ingres\_query</span>.

### 参数

`result`  
The query result identifier

### 返回值

Returns the number of fields

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_num\_rows
=================

Get the number of rows affected or returned by a query

### 说明

<span class="type">int</span> <span
class="methodname">ingres\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

This function primarily is meant to get the number of rows modified in
the database. However, it can be used to retrieve the number of rows to
fetch for a SELECT statement.

> **Note**:
>
> If <a href="/book/ingres.html#" class="link">scrollable cursors</a>
> are disabled and this function is called before using <span
> class="function">ingres\_fetch\_array</span>, <span
> class="function">ingres\_fetch\_object</span>, or <span
> class="function">ingres\_fetch\_row</span>, the server will delete the
> result's data and the script will be unable to get them.
>
> Instead, you should retrieve the result's data using one of these
> fetch functions in a loop until it returns **`FALSE`**, indicating
> that no more results are available.

### 参数

`result`  
The result identifier for a query

### 返回值

For delete, insert, or update queries, <span
class="function">ingres\_num\_rows</span> returns the number of rows
affected by the query. For other queries, <span
class="function">ingres\_num\_rows</span> returns the number of rows in
the query's result.

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_pconnect
================

Open a persistent connection to an Ingres database

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">ingres\_pconnect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$database`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$username`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\]\]\] )

Open a persistent connection to an Ingres database.

There are only two differences between this function and <span
class="function">ingres\_connect</span>: First, when connecting, the
function will initially try to find a (persistent) link that is already
opened with the same parameters. If one is found, an identifier for it
will be returned instead of opening a new connection. Second, the
connection to the Ingres server will not be closed when the execution of
the script ends. Instead, the link will remain open for future use
(<span class="function">ingres\_close</span> will not close links
established by <span class="function">ingres\_pconnect</span>). This
type of link is therefore called "persistent".

### 参数

`database`  
The database name. Must follow the syntax:

`[vnode::]dbname[/svr_class]`

`username`  
The Ingres user name

`password`  
The password associated with `username`

`options`  
See <span class="function">ingres\_connect</span> for the list of
options that can be passed

### 返回值

Returns an Ingres link resource on success 或者在失败时返回 **`FALSE`**

### 参见

-   <span class="function">ingres\_connect</span>
-   <span class="function">ingres\_close</span>

ingres\_prepare
===============

Prepare a query for later execution

### 说明

<span class="type">mixed</span> <span
class="methodname">ingres\_prepare</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

Prepares a query for execution by <span
class="function">ingres\_execute</span>.

The query becomes part of the currently open transaction. If there is no
open transaction, <span class="function">ingres\_query</span> opens a
new transaction. To close the transaction, you can call either <span
class="function">ingres\_commit</span> to commit the changes made to the
database or <span class="function">ingres\_rollback</span> to cancel
these changes. When the script ends, any open transaction is rolled back
(by calling <span class="function">ingres\_rollback</span>). You can
also use <span class="function">ingres\_autocommit</span> before opening
a new transaction to have every SQL query immediately committed.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.describe</a>,
> <a href="/book/ingres.html#" class="link">ingres.scrollable</a> and
> <a href="/book/ingres.html#" class="link">ingres.utf8</a> directives
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`link`  
The connection link identifier

`query`  
A valid SQL query (see the Ingres *SQL reference guide*) in the Ingres
documentation. See the
<a href="/book/ingres.html#" class="link">query</a> parameter in <span
class="function">ingres\_query</span> for a list of SQL statements which
cannot be executed using <span class="function">ingres\_prepare</span>

### 返回值

<span class="function">ingres\_prepare</span> returns a query result
identifier that is used with <span
class="function">ingres\_execute</span> to execute the query. To see if
an error occurred, use <span class="function">ingres\_errno</span>,
<span class="function">ingres\_error</span>, or <span
class="function">ingres\_errsqlstate</span>.

### 参见

-   <span class="function">ingres\_unbuffered\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>
-   <span class="function">ingres\_commit</span>
-   <span class="function">ingres\_rollback</span>
-   <span class="function">ingres\_autocommit</span>
-   <span class="function">ingres\_set\_environment</span>
-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_error</span>

ingres\_query
=============

Send an SQL query to Ingres

### 说明

<span class="type">mixed</span> <span
class="methodname">ingres\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">array</span> `$params`</span> \[, <span
class="methodparam"><span class="type">string</span> `$types`</span>
\]\] )

<span class="function">ingres\_query</span> sends the given `query` to
the Ingres server.

The query becomes part of the currently open transaction. If there is no
open transaction, <span class="function">ingres\_query</span> opens a
new transaction. To close the transaction, you can call either <span
class="function">ingres\_commit</span> to commit the changes made to the
database or <span class="function">ingres\_rollback</span> to cancel
these changes. When the script ends, any open transaction is rolled back
(by calling <span class="function">ingres\_rollback</span>). You can
also use <span class="function">ingres\_autocommit</span> before opening
a new transaction to have every SQL query immediately committed.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.describe</a>,
> <a href="/book/ingres.html#" class="link">ingres.scrollable</a> and
> <a href="/book/ingres.html#" class="link">ingres.utf8</a> directives
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>

### 参数

`link`  
The connection link identifier.

`query`  
A valid SQL query (see the Ingres *SQL reference guide*) in the Ingres
documentation.

Data inside the query should be
<a href="/book/ingres.html#ingres_escape_string" class="link">properly escaped</a>.

The following types of SQL queries cannot be sent with this function:

-   <span class="simpara"> *close* (see <span
    class="function">ingres\_close</span>) </span>
-   <span class="simpara"> *commit* (see <span
    class="function">ingres\_commit</span>) </span>
-   <span class="simpara"> *connect* (see <span
    class="function">ingres\_connect</span>) </span>
-   <span class="simpara"> *disconnect* (see <span
    class="function">ingres\_close</span>) </span>
-   <span class="simpara">*get dbevent*</span>
-   <span class="simpara">*prepare to commit*</span>
-   <span class="simpara"> *rollback* (see <span
    class="function">ingres\_rollback</span>) </span>
-   <span class="simpara">*savepoint*</span>
-   <span class="simpara"> *set autocommit* (see <span
    class="function">ingres\_autocommit</span>) </span>
-   <span class="simpara">all cursor-related queries are
    unsupported</span>

`params`  
An array of parameter values to be used with the query

`types`  
A string containing a sequence of types for the parameter values passed.
When <a href="/book/ingres.html#" class="link">ingres.describe</a> is
enabled, this parameter can be ignored as the driver automatically
fetches the expected parameter types from the server.

| Type code | Ingres type                                            |
|-----------|--------------------------------------------------------|
| a         | <span class="type">bool</span>                         |
| b         | <span class="type">BYTE</span>                         |
| B         | <span class="type">LONG BYTE/BLOB</span>               |
| c         | <span class="type">CHAR</span>                         |
| d         | <span class="type">DATE/ANSIDATE/TIMESTAMP/TIME</span> |
| f         | <span class="type">FLOAT</span>                        |
| i         | <span class="type">int</span>                          |
| L         | <span class="type">LONG TEXT</span>                    |
| m         | <span class="type">MONEY</span>                        |
| M         | <span class="type">LONG NVARCHAR</span>                |
| n         | <span class="type">NCHAR</span>                        |
| N         | <span class="type">NVARCHAR</span>                     |
| t         | <span class="type">TEXT</span>                         |
| v         | <span class="type">VARCHAR</span>                      |
| V         | <span class="type">LONG VARCHAR</span>                 |

### 返回值

<span class="function">ingres\_query</span> returns a query result
identifier on success else it returns **`FALSE`**. To see if an error
occurred use <span class="function">ingres\_errno</span>, <span
class="function">ingres\_error</span> or <span
class="function">ingres\_errsqlstate</span>.

### 范例

**示例 \#1 Send a simple select**

``` php
<?php
$link = ingres_connect("demodb");

$result = ingres_query($link, "select * from user_profile");
while ($row = ingres_fetch_row($result)) {
    echo $row[1];
    echo $row[2];
}
?>
```

**示例 \#2 Passing query parameters to <span
class="function">ingres\_query</span>**

``` php
<?php
$link = ingres_connect("demodb");

$params[] = "Emma";
$query = "select * from user_profile where up_first = ?";
$result = ingres_query($link, $query, $params);
while ($row = ingres_fetch_row($result)) {
    echo $row[1];
    echo $row[2];
}
?>
```

**示例 \#3 Inserting a BLOB with parameter types**

``` php
<?php
$link = ingres_connect("demodb");

//Open a photo
$fh = fopen("photo.jpg","r");
$blob_data = stream_get_contents($fh);
fclose($fh);

//Prepare parameters
$params[] = $blob_data;
$params[] = 1201;

//Define parameter types
$param_types = "Bi";

$query = "update user_profile set up_image = ? where up_id = ?";
$result = ingres_query($link, $query , $params, $param_types);

if (ingres_errno())
{
    echo ingres_errno() . "-" . ingres_error() . "\n";
}

ingres_commit($link);

ingres_close($link);
?>
```

### 参见

-   <span class="function">ingres\_unbuffered\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>
-   <span class="function">ingres\_commit</span>
-   <span class="function">ingres\_rollback</span>
-   <span class="function">ingres\_autocommit</span>
-   <span class="function">ingres\_set\_environment</span>
-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_error</span>

ingres\_result\_seek
====================

Set the row position before fetching data

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_result\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$position`</span> )

This function is used to position the cursor associated with the result
resource before issuing a fetch. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is set to 0 then the first row is 0 else it is 1. <span
class="function">ingres\_result\_seek</span> can be used only with
queries that make use of
<a href="/book/ingres.html#" class="link">scrollable cursors</a>. It
cannot be used with <span
class="function">ingres\_unbuffered\_query</span>.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.scrollable</a> and
> <a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
> directives in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`result`  
The result identifier for a query

`position`  
The row to position the cursor on. If
<a href="/book/ingres.html#" class="link">ingres.array_index_start</a>
is set to 0, then the first row is 0, else it is 1

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Position the cursor on the 3rd row**

``` php
<?php

$result=ingres_query($link, "select * from airport where ap_ccode = 'ES' order by ap_place asc");

/* goto row 3 */
if (!ingres_result_seek($result, 3))
{
    echo ingres_errno() . " - " . ingres_error . "\n";
    die("i died");
}
else
{
    $airport = ingres_fetch_object ($result);
    {
        echo $airport->ap_iatacode . " - " .  $airport->ap_name . "\n";
    }
}

ingres_commit($link);

?>
```

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>

ingres\_rollback
================

Roll back a transaction

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_rollback</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

<span class="function">ingres\_rollback</span> rolls back the currently
open transaction, actually cancelling all changes made to the database
during the transaction.

This closes the transaction. A new transaction can be opened by sending
a query with <span class="function">ingres\_query</span>.

### 参数

`link`  
The connection link identifier

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_commit</span>
-   <span class="function">ingres\_autocommit</span>

ingres\_set\_environment
========================

Set environment features controlling output options

### 说明

<span class="type">bool</span> <span
class="methodname">ingres\_set\_environment</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">array</span>
`$options`</span> )

<span class="function">ingres\_set\_environment</span> is called to set
environmental options that affect the output of certain values from
Ingres, such as the timezone, date format, decimal character separator,
and float precision.

### 参数

`link`  
The connection link identifier

`options`  
An enumerated <span class="type">array</span> of option name/value
pairs. The following table lists the option name and the expected type

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Option name</th>
<th>Option type</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>date_century_boundary</td>
<td><span class="type">int</span></td>
<td>The threshold by which a 2-digit year is determined to be in the current century or in the next century. Equivalent to II_DATE_CENTURY_BOUNDARY</td>
<td>50</td>
</tr>
<tr class="even">
<td>timezone</td>
<td><span class="type">string</span></td>
<td>Controls the timezone of the session. If not set, it will default the value defined by II_TIMEZONE_NAME. If II_TIMEZONE_NAME is not defined, NA-PACIFIC (GMT-8 with Daylight Savings) is used.</td>
<td>UNITED-KINGDOM</td>
</tr>
<tr class="odd">
<td>date_format</td>
<td><span class="type">int</span></td>
<td><p>Sets the allowable input and output format for Ingres dates. Defaults to the value defined by II_DATE_FORMAT. If II_DATE_FORMAT is not set, the default date format is US, for example mm/dd/yy. Valid values for date_format are:</p>
<ul>
<li><span class="simpara">INGRES_DATE_DMY</span></li>
<li><span class="simpara">INGRES_DATE_FINISH</span></li>
<li><span class="simpara">INGRES_DATE_GERMAN</span></li>
<li><span class="simpara">INGRES_DATE_ISO</span></li>
<li><span class="simpara">INGRES_DATE_ISO4</span></li>
<li><span class="simpara">INGRES_DATE_MDY</span></li>
<li><span class="simpara">INGRES_DATE_MULTINATIONAL</span></li>
<li><span class="simpara">INGRES_DATE_MULTINATIONAL4</span></li>
<li><span class="simpara">INGRES_DATE_YMD</span></li>
<li><span class="simpara">INGRES_DATE_US</span></li>
</ul></td>
<td>INGRES_DATE_ISO4</td>
</tr>
<tr class="even">
<td>decimal_separator</td>
<td><span class="type">string</span></td>
<td>The character identifier for decimal data</td>
<td>","</td>
</tr>
<tr class="odd">
<td>money_lort</td>
<td><span class="type">int</span></td>
<td><p>Leading or trailing currency sign. Valid values for money_lort are:</p>
<ul>
<li><span class="simpara">INGRES_MONEY_LEADING</span></li>
<li><span class="simpara">INGRES_MONEY_TRAILING</span></li>
</ul></td>
<td>INGRES_MONEY_LEADING</td>
</tr>
<tr class="even">
<td>money_sign</td>
<td><span class="type">string</span></td>
<td>The currency symbol to be used with the MONEY datatype</td>
<td>€</td>
</tr>
<tr class="odd">
<td>money_precision</td>
<td><span class="type">int</span></td>
<td>The precision of the MONEY datatype</td>
<td>2</td>
</tr>
<tr class="even">
<td>float4_precision</td>
<td><span class="type">int</span></td>
<td>Precision of the FLOAT4 datatype</td>
<td>10</td>
</tr>
<tr class="odd">
<td>float8_precision</td>
<td><span class="type">int</span></td>
<td>Precision of the FLOAT8 data</td>
<td>10</td>
</tr>
<tr class="even">
<td>blob_segment_length</td>
<td><span class="type">int</span></td>
<td>The amount of data in bytes to fetch at a time when retrieving BLOB or CLOB data. Defaults to 4096 bytes when not set explicitly</td>
<td>8192</td>
</tr>
</tbody>
</table>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Set date\_format to ISO4**

``` php
<?php
$options = array( "date_format" => INGRES_DATE_ISO4 );

if (ingres_set_environment($link, $options))
{
    $result=ingres_query($link,"select date('now') as date");

    while ( $object = ingres_fetch_object ($result) ) {
        echo $object->date."\n";
    }
}
?>
```

**示例 \#2 Set timezone to HONG-KONG**

``` php
<?php

$options = array( "timezone" => "HONG-KONG");

if (ingres_set_environment($link, $options))
{
    $result=ingres_query($link,"select date('now') as date");

    while ( $object = ingres_fetch_object ($result) ) {
        echo $object->date."\n";
    }
}
?>
```

### 参见

-   <span class="function">ingres\_connect</span>
-   <span class="function">ingres\_query</span>

ingres\_unbuffered\_query
=========================

Send an unbuffered SQL query to Ingres

### 说明

<span class="type">mixed</span> <span
class="methodname">ingres\_unbuffered\_query</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">array</span> `$params`</span> \[, <span
class="methodparam"><span class="type">string</span> `$types`</span>
\]\] )

<span class="function">ingres\_unbuffered\_query</span> sends the given
`query` to the Ingres server.

The query becomes part of the currently open transaction. If there is no
open transaction, <span
class="function">ingres\_unbuffered\_query</span> opens a new
transaction. To close the transaction, you can call either <span
class="function">ingres\_commit</span> to commit the changes made to the
database or <span class="function">ingres\_rollback</span> to cancel
these changes. When the script ends, any open transaction is rolled back
(by calling <span class="function">ingres\_rollback</span>). You can
also use <span class="function">ingres\_autocommit</span> before opening
a new transaction to have every SQL query immediately committed. Ingres
allows only a single unbuffered statement to be active at any one time.
The extension will close any active unbuffered statements before
executing any SQL. In addition you cannot use <span
class="function">ingres\_result\_seek</span> to position the row before
fetching.

> **Note**: **Related Configurations**  
>
> See also the
> <a href="/book/ingres.html#" class="link">ingres.describe</a> and
> <a href="/book/ingres.html#" class="link">ingres.utf8</a> directives
> in
> <a href="/book/ingres.html#运行时配置" class="link">Runtime Configuration</a>.

### 参数

`link`  
The connection link identifier

`query`  
A valid SQL query (see the Ingres *SQL reference guide*) in the Ingres
documentation. See the
<a href="/book/ingres.html#" class="link">query</a> parameter in <span
class="function">ingres\_query</span> for a list of SQL statements that
cannot be executed via <span
class="function">ingres\_unbuffered\_query</span>.

Data inside the query should be
<a href="/book/ingres.html#ingres_escape_string" class="link">properly escaped</a>.

`params`  
An array of parameter values to be used with the query

`types`  
A string containing a sequence of types for the parameter values passed.
See the <a href="/book/ingres.html#" class="link">types</a> parameter in
<span class="function">ingres\_query</span> for the list of type codes.

### 返回值

<span class="function">ingres\_unbuffered\_query</span> returns a query
result identifier when there are rows to fetch; else it returns
**`FALSE`** when there are no rows, as is the case of an INSERT, UPDATE,
or DELETE statement. To see if an error occurred, use <span
class="function">ingres\_errno</span>, <span
class="function">ingres\_error</span>, or <span
class="function">ingres\_errsqlstate</span>.

### 范例

**示例 \#1 Issue a simple un-buffered select**

``` php
<?php
$link = ingres_connect("demodb");

$result = ingres_unbuffered_query($link, "select * from user_profile");
while ($row = ingres_fetch_row($result)) {
    echo $row[1];
    echo $row[2];
}
?>
```

**示例 \#2 Passing query parameters to <span
class="function">ingres\_unbuffered\_query</span>**

``` php
<?php
$link = ingres_connect("demodb");

$params[] = "Emma";
$query = "select * from user_profile where up_first = ?";
$result = ingres_unbuffered_query($link, $query, $params);
while ($row = ingres_fetch_row($result)) {
    echo $row[1];
    echo $row[2];
}
?>
```

**示例 \#3 Inserting a BLOB with parameter types**

``` php
<?php
$link = ingres_connect("demodb");

//Open a photo
$fh = fopen("photo.jpg","r");
$blob_data = stream_get_contents($fh);
fclose($fh);

//Prepare parameters
$params[] = $blob_data;
$params[] = 1201;

//Define parameter types
$param_types = "Bi";

$query = "update user_profile set up_image = ? where up_id = ?";
$result = ingres_unbuffered_query($link, $query , $params, $param_types);

if (ingres_errno())
{
    echo ingres_errno() . "-" . ingres_error() . "\n";
}
?>
```

### 参见

-   <span class="function">ingres\_query</span>
-   <span class="function">ingres\_fetch\_array</span>
-   <span class="function">ingres\_fetch\_assoc</span>
-   <span class="function">ingres\_fetch\_object</span>
-   <span class="function">ingres\_fetch\_row</span>
-   <span class="function">ingres\_commit</span>
-   <span class="function">ingres\_rollback</span>
-   <span class="function">ingres\_autocommit</span>
-   <span class="function">ingres\_set\_environment</span>
-   <span class="function">ingres\_errno</span>
-   <span class="function">ingres\_error</span>

**目录**

-   [ingres\_autocommit\_state](/book/ingres.html#ingres_autocommit_state)
    — Test if the connection is using autocommit
-   [ingres\_autocommit](/book/ingres.html#ingres_autocommit) — Switch
    autocommit on or off
-   [ingres\_charset](/book/ingres.html#ingres_charset) — Returns the
    installation character set
-   [ingres\_close](/book/ingres.html#ingres_close) — Close an Ingres
    database connection
-   [ingres\_commit](/book/ingres.html#ingres_commit) — Commit a
    transaction
-   [ingres\_connect](/book/ingres.html#ingres_connect) — Open a
    connection to an Ingres database
-   [ingres\_cursor](/book/ingres.html#ingres_cursor) — Get a cursor
    name for a given result resource
-   [ingres\_errno](/book/ingres.html#ingres_errno) — Get the last
    Ingres error number generated
-   [ingres\_error](/book/ingres.html#ingres_error) — Get a meaningful
    error message for the last error generated
-   [ingres\_errsqlstate](/book/ingres.html#ingres_errsqlstate) — Get
    the last SQLSTATE error code generated
-   [ingres\_escape\_string](/book/ingres.html#ingres_escape_string) —
    Escape special characters for use in a query
-   [ingres\_execute](/book/ingres.html#ingres_execute) — Execute a
    prepared query
-   [ingres\_fetch\_array](/book/ingres.html#ingres_fetch_array) — Fetch
    a row of result into an array
-   [ingres\_fetch\_assoc](/book/ingres.html#ingres_fetch_assoc) — Fetch
    a row of result into an associative array
-   [ingres\_fetch\_object](/book/ingres.html#ingres_fetch_object) —
    Fetch a row of result into an object
-   [ingres\_fetch\_proc\_return](/book/ingres.html#ingres_fetch_proc_return)
    — Get the return value from a procedure call
-   [ingres\_fetch\_row](/book/ingres.html#ingres_fetch_row) — Fetch a
    row of result into an enumerated array
-   [ingres\_field\_length](/book/ingres.html#ingres_field_length) — Get
    the length of a field
-   [ingres\_field\_name](/book/ingres.html#ingres_field_name) — Get the
    name of a field in a query result
-   [ingres\_field\_nullable](/book/ingres.html#ingres_field_nullable) —
    Test if a field is nullable
-   [ingres\_field\_precision](/book/ingres.html#ingres_field_precision)
    — Get the precision of a field
-   [ingres\_field\_scale](/book/ingres.html#ingres_field_scale) — Get
    the scale of a field
-   [ingres\_field\_type](/book/ingres.html#ingres_field_type) — Get the
    type of a field in a query result
-   [ingres\_free\_result](/book/ingres.html#ingres_free_result) — Free
    the resources associated with a result identifier
-   [ingres\_next\_error](/book/ingres.html#ingres_next_error) — Get the
    next Ingres error
-   [ingres\_num\_fields](/book/ingres.html#ingres_num_fields) — Get the
    number of fields returned by the last query
-   [ingres\_num\_rows](/book/ingres.html#ingres_num_rows) — Get the
    number of rows affected or returned by a query
-   [ingres\_pconnect](/book/ingres.html#ingres_pconnect) — Open a
    persistent connection to an Ingres database
-   [ingres\_prepare](/book/ingres.html#ingres_prepare) — Prepare a
    query for later execution
-   [ingres\_query](/book/ingres.html#ingres_query) — Send an SQL query
    to Ingres
-   [ingres\_result\_seek](/book/ingres.html#ingres_result_seek) — Set
    the row position before fetching data
-   [ingres\_rollback](/book/ingres.html#ingres_rollback) — Roll back a
    transaction
-   [ingres\_set\_environment](/book/ingres.html#ingres_set_environment)
    — Set environment features controlling output options
-   [ingres\_unbuffered\_query](/book/ingres.html#ingres_unbuffered_query)
    — Send an unbuffered SQL query to Ingres
