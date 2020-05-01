Sybase
======

**目录**

-   [简介](/book/sybase.html#简介)
-   [安装／配置](/book/sybase.html#安装／配置)
    -   [需求](/book/sybase.html#需求)
    -   [安装](/book/sybase.html#安装)
    -   [运行时配置](/book/sybase.html#运行时配置)
    -   [资源类型](/book/sybase.html#资源类型)
-   [预定义常量](/book/sybase.html#预定义常量)
-   [Sybase 函数](/book/sybase.html#Sybase%20函数)
    -   [sybase\_affected\_rows](/book/sybase.html#sybase_affected_rows)
        — Gets number of affected rows in last query
    -   [sybase\_close](/book/sybase.html#sybase_close) — Closes a
        Sybase connection
    -   [sybase\_connect](/book/sybase.html#sybase_connect) — Opens a
        Sybase server connection
    -   [sybase\_data\_seek](/book/sybase.html#sybase_data_seek) — Moves
        internal row pointer
    -   [sybase\_deadlock\_retry\_count](/book/sybase.html#sybase_deadlock_retry_count)
        — Sets the deadlock retry count
    -   [sybase\_fetch\_array](/book/sybase.html#sybase_fetch_array) —
        Fetch row as array
    -   [sybase\_fetch\_assoc](/book/sybase.html#sybase_fetch_assoc) —
        Fetch a result row as an associative array
    -   [sybase\_fetch\_field](/book/sybase.html#sybase_fetch_field) —
        Get field information from a result
    -   [sybase\_fetch\_object](/book/sybase.html#sybase_fetch_object) —
        Fetch a row as an object
    -   [sybase\_fetch\_row](/book/sybase.html#sybase_fetch_row) — Get a
        result row as an enumerated array
    -   [sybase\_field\_seek](/book/sybase.html#sybase_field_seek) —
        Sets field offset
    -   [sybase\_free\_result](/book/sybase.html#sybase_free_result) —
        Frees result memory
    -   [sybase\_get\_last\_message](/book/sybase.html#sybase_get_last_message)
        — Returns the last message from the server
    -   [sybase\_min\_client\_severity](/book/sybase.html#sybase_min_client_severity)
        — Sets minimum client severity
    -   [sybase\_min\_error\_severity](/book/sybase.html#sybase_min_error_severity)
        — Sets minimum error severity
    -   [sybase\_min\_message\_severity](/book/sybase.html#sybase_min_message_severity)
        — Sets minimum message severity
    -   [sybase\_min\_server\_severity](/book/sybase.html#sybase_min_server_severity)
        — Sets minimum server severity
    -   [sybase\_num\_fields](/book/sybase.html#sybase_num_fields) —
        Gets the number of fields in a result set
    -   [sybase\_num\_rows](/book/sybase.html#sybase_num_rows) — Get
        number of rows in a result set
    -   [sybase\_pconnect](/book/sybase.html#sybase_pconnect) — Open
        persistent Sybase connection
    -   [sybase\_query](/book/sybase.html#sybase_query) — Sends a Sybase
        query
    -   [sybase\_result](/book/sybase.html#sybase_result) — Get result
        data
    -   [sybase\_select\_db](/book/sybase.html#sybase_select_db) —
        Selects a Sybase database
    -   [sybase\_set\_message\_handler](/book/sybase.html#sybase_set_message_handler)
        — Sets the handler called when a server message is raised
    -   [sybase\_unbuffered\_query](/book/sybase.html#sybase_unbuffered_query)
        — Send a Sybase query and do not block

**Warning**

As of PHP 7.0.0, the sybase\_ct extension has been removed.

安装／配置
==========

**目录**

-   [需求](/book/sybase.html#需求)
-   [安装](/book/sybase.html#安装)
-   [运行时配置](/book/sybase.html#运行时配置)
-   [资源类型](/book/sybase.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

To enable Sybase-DB support configure PHP **--with-sybase\[=DIR\]**. DIR
is the Sybase home directory, defaults to `/home/sybase`. To enable
Sybase-CT support configure PHP **--with-sybase-ct\[=DIR\]**. DIR is the
Sybase home directory, defaults to `/home/sybase`.

> **Note**:
>
> As of PHP 5.3.0, the Sybase extension has been superseded by the
> sybase\_ct extension and is no longer maintained. To continue using
> sybase you must use the sybase\_ct extension.
>
> As of PHP 7.0.0, the sybase\_ct extension has been removed.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                      | 默认                     | 可修改范围       | 更新日志                                                           |
|---------------------------------------------------------------------------|--------------------------|------------------|--------------------------------------------------------------------|
| <a href="/book/sybase.html#" class="link">sybase.allow_persistent</a>     | "1"                      | PHP\_INI\_ALL    | PHP\_INI\_ALL in PHP \<= 4.0.2. PHP\_INI\_SYSTEM in PHP \<= 4.0.3. |
| <a href="/book/sybase.html#" class="link">sybase.max_persistent</a>       | "-1"                     | PHP\_INI\_ALL    | PHP\_INI\_ALL in PHP \<= 4.0.2. PHP\_INI\_SYSTEM in PHP \<= 4.0.3. |
| <a href="/book/sybase.html#" class="link">sybase.max_links</a>            | "-1"                     | PHP\_INI\_ALL    | PHP\_INI\_ALL in PHP \<= 4.0.2. PHP\_INI\_SYSTEM in PHP \<= 4.0.3. |
| sybase.interface\_file                                                    | "/usr/sybase/interfaces" | PHP\_INI\_SYSTEM |                                                                    |
| <a href="/book/sybase.html#" class="link">sybase.min_error_severity</a>   | "10"                     | PHP\_INI\_ALL    |                                                                    |
| <a href="/book/sybase.html#" class="link">sybase.min_message_severity</a> | "10"                     | PHP\_INI\_ALL    |                                                                    |
| sybase.compatability\_mode                                                | "0"                      | PHP\_INI\_ALL    |                                                                    |
| <a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>         | "0"                      | PHP\_INI\_ALL    | Deprecated in PHP 5.3.0. Removed in PHP 5.4.0.                     |

这是配置指令的简短说明。

`sybase.allow_persistent` <span class="type">boolean</span>  
Whether to allow persistent Sybase connections.

`sybase.max_persistent` <span class="type">integer</span>  
The maximum number of persistent Sybase connections per process. -1
means no limit.

`sybase.max_links` <span class="type">integer</span>  
The maximum number of Sybase connections per process, including
persistent connections. -1 means no limit.

`sybase.min_error_severity` <span class="type">integer</span>  
Minimum error severity to display.

`sybase.min_message_severity` <span class="type">integer</span>  
Minimum message severity to display.

`magic_quotes_sybase` <span class="type">boolean</span>  
If `magic_quotes_sybase` is on, a single-quote is escaped with a
single-quote instead of a backslash if
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a> or
<a href="/info/setup.html#" class="link">magic_quotes_runtime</a> are
enabled. This setting is also respected by <span
class="function">addslashes</span> and <span
class="function">stripslashes</span>.

> **Note**:
>
> Note that when `magic_quotes_sybase` is ON it completely overrides
> `magic_quotes_gpc       `. In this case even when `magic_quotes_gpc`
> is enabled neither double quotes, backslashes or NUL's will be
> escaped.

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

| 名字                                                                     | 默认 | 可修改范围    | 更新日志                   |
|--------------------------------------------------------------------------|------|---------------|----------------------------|
| <a href="/book/sybase.html#" class="link">sybct.deadlock_retry_count</a> | "0"  | PHP\_INI\_ALL | Available since PHP 4.3.0. |

这是配置指令的简短说明。

`sybct.login_timeout` <span class="type">integer</span>  
The maximum time in seconds to wait for a connection attempt to succeed
before returning failure. Note that if max\_execution\_time has been
exceeded when a connection attempt times out, your script will be
terminated before it can take action on failure. The default is one
minute.

`sybct.timeout` <span class="type">integer</span>  
The maximum time in seconds to wait for a select\_db or query operation
to succeed before returning failure. Note that if max\_execution\_time
has been exceeded when an operation times out, your script will be
terminated before it can take action on failure. The default is no
limit.

`sybct.deadlock_retry_count` <span class="type">int</span>  
Allows you to define how often deadlocks are to be retried. The default
is 0, value -1 means "forever".

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

资源类型
--------

此扩展没有定义资源类型。

预定义常量
==========

此扩展没有定义常量。

sybase\_affected\_rows
======================

Gets number of affected rows in last query

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">int</span> <span
class="methodname">sybase\_affected\_rows</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">sybase\_affected\_rows</span> returns the number
of rows affected by the last INSERT, UPDATE or DELETE query on the
server associated with the specified link identifier.

This command is not effective for SELECT statements, only on statements
which modify records. To retrieve the number of rows returned from a
SELECT, use <span class="function">sybase\_num\_rows</span>.

### 参数

`link_identifier`  
If the link identifier isn't specified, the last opened link is assumed.

### 返回值

Returns the number of affected rows, as an integer.

### 范例

**示例 \#1 Delete-Query**

``` php
<?php
/* connect to database */
sybase_connect('SYBASE', '', '') or
die("Could not connect");
sybase_select_db("db");

sybase_query("DELETE FROM sometable WHERE id < 10");
printf("Records deleted: %d\n", sybase_affected_rows());
?>
```

以上例程会输出：

    Records deleted: 10

### 参见

-   <span class="function">sybase\_num\_rows</span>

sybase\_close
=============

Closes a Sybase connection

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">sybase\_close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">sybase\_close</span> closes the link to a Sybase
database that's associated with the specified link `link_identifier`.

Note that this isn't usually necessary, as non-persistent open links are
automatically closed at the end of the script's execution.

<span class="function">sybase\_close</span> will not close persistent
links generated by <span class="function">sybase\_pconnect</span>.

### 参数

`link_identifier`  
If the link identifier isn't specified, the last opened link is assumed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">sybase\_connect</span>
-   <span class="function">sybase\_pconnect</span>

sybase\_connect
===============

Opens a Sybase server connection

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">resource</span> <span
class="methodname">sybase\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$servername`</span> \[, <span class="methodparam"><span
class="type">string</span> `$username`</span> \[, <span
class="methodparam"><span class="type">string</span> `$password`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$charset`</span> \[, <span class="methodparam"><span
class="type">string</span> `$appname`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$new`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\]\]\]\] )

<span class="function">sybase\_connect</span> establishes a connection
to a Sybase server.

In case a second call is made to <span
class="function">sybase\_connect</span> with the same arguments, no new
link will be established, but instead, the link identifier of the
already opened link will be returned.

The link to the server will be closed as soon as the execution of the
script ends, unless it's closed earlier by explicitly calling <span
class="function">sybase\_close</span>.

### 参数

`servername`  
The servername argument has to be a valid servername that is defined in
the 'interfaces' file.

`username`  
Sybase user name

`password`  
Password associated with `username`.

`charset`  
Specifies the charset for the connection

`appname`  
Specifies an *appname* for the Sybase connection. This allow you to make
separate connections in the same script to the same database. This may
come handy when you have started a transaction in your current
connection, and you need to be able to do a separate query which cannot
be performed inside this transaction.

`new`  
Whether to open a new connection or use the existing one.

### 返回值

Returns a positive Sybase link identifier on success, or **`FALSE`** on
failure.

### 更新日志

| 版本  | 说明                           |
|-------|--------------------------------|
| 5.3.0 | The `new` parameter was added. |

### 范例

**示例 \#1 <span class="function">sybase\_connect</span> example**

``` php
<?php
$link = sybase_connect('SYBASE', '', '')
        or die("Could not connect !");
echo "Connected successfully";
sybase_close($link);
?>
```

### 参见

-   <span class="function">sybase\_pconnect</span>
-   <span class="function">sybase\_close</span>

sybase\_data\_seek
==================

Moves internal row pointer

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">sybase\_data\_seek</span> ( <span
class="methodparam"><span class="type">resource</span>
`$result_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$row_number`</span> )

<span class="function">sybase\_data\_seek</span> moves the internal row
pointer of the Sybase result associated with the specified result
identifier to pointer to the specified row number. The next call to
<span class="function">sybase\_fetch\_row</span> would return that row.

### 参数

`result_identifier`  

`row_number`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">sybase\_fetch\_row</span>

sybase\_deadlock\_retry\_count
==============================

Sets the deadlock retry count

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">sybase\_deadlock\_retry\_count</span> ( <span
class="methodparam"><span class="type">int</span> `$retry_count`</span>
)

Using <span class="function">sybase\_deadlock\_retry\_count</span>, the
number of retries can be defined in cases of deadlocks. By default,
every deadlock is retried an infinite number of times or until the
process is killed by Sybase, the executing script is killed (for
instance, by <span class="function">set\_time\_limit</span>) or the
query succeeds.

### 参数

`retry_count`  
|     |                         |
|-----|-------------------------|
| -1  | Retry forever (default) |
| 0   | Do not retry            |
| n   | Retry n times           |

### 返回值

没有返回值。

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

sybase\_fetch\_array
====================

Fetch row as array

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">array</span> <span
class="methodname">sybase\_fetch\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">sybase\_fetch\_array</span> is an extended
version of <span class="function">sybase\_fetch\_row</span>. In addition
to storing the data in the numeric indices of the result array, it also
stores the data in associative indices, using the field names as keys.

An important thing to note is that using <span
class="function">sybase\_fetch\_array</span> is NOT significantly slower
than using <span class="function">sybase\_fetch\_row</span>, while it
provides a significant added value.

### 参数

`result`  

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

> **Note**:
>
> When selecting fields with identical names (for instance, in a join),
> the associative indices will have a sequential number prepended. See
> the example for details.

### 范例

**示例 \#1 Identical fieldnames**

``` php
<?php

$dbh = sybase_connect('SYBASE', '', '');
$q = sybase_query('SELECT * FROM p, a WHERE p.person_id= a.person_id');
var_dump(sybase_fetch_array($q));
sybase_close($dbh);
?>
```

The above example would produce the following output (assuming the two
tables only have each one column called "person\_id"):

    array(4) {
      [0]=>
      int(1)
      ["person_id"]=>
      int(1)
      [1]=>
      int(1)
      ["person_id1"]=>
      int(1)
    }

### 参见

-   <span class="function">sybase\_fetch\_row</span>
-   <span class="function">sybase\_fetch\_assoc</span>
-   <span class="function">sybase\_fetch\_object</span>

sybase\_fetch\_assoc
====================

Fetch a result row as an associative array

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">array</span> <span
class="methodname">sybase\_fetch\_assoc</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">sybase\_fetch\_assoc</span> is a version of <span
class="function">sybase\_fetch\_row</span> that uses column names
instead of integers for indices in the result array. Columns from
different tables with the same names are returned as name, name1, name2,
..., nameN.

An important thing to note is that using <span
class="function">sybase\_fetch\_assoc</span> is NOT significantly slower
than using <span class="function">sybase\_fetch\_row</span>, while it
provides a significant added value.

### 参数

`result`  

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows.

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

### 参见

-   <span class="function">sybase\_fetch\_row</span>
-   <span class="function">sybase\_fetch\_array</span>
-   <span class="function">sybase\_fetch\_object</span>

sybase\_fetch\_field
====================

Get field information from a result

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">object</span> <span
class="methodname">sybase\_fetch\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$field_offset`<span class="initializer"> = -1</span></span> \] )

<span class="function">sybase\_fetch\_field</span> can be used in order
to obtain information about fields in a certain query result.

### 参数

`result`  

`field_offset`  
If the field offset isn't specified, the next field that wasn't yet
retrieved by <span class="function">sybase\_fetch\_field</span> is
retrieved.

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
-   <span class="simpara"> type - datatype of the column </span>

### 参见

-   <span class="function">sybase\_field\_seek</span>

sybase\_fetch\_object
=====================

Fetch a row as an object

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">object</span> <span
class="methodname">sybase\_fetch\_object</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$object`</span> \] )

<span class="function">sybase\_fetch\_object</span> is similar to <span
class="function">sybase\_fetch\_assoc</span>, with one difference - an
object is returned, instead of an array.

Speed-wise, the function is identical to <span
class="function">sybase\_fetch\_array</span>, and almost as quick as
<span class="function">sybase\_fetch\_row</span> (the difference is
insignificant).

### 参数

`result`  

`object`  
Use the second `object` to specify the type of object you want to
return. If this parameter is omitted, the object will be of type
stdClass.

### 返回值

Returns an object with properties that correspond to the fetched row, or
**`FALSE`** if there are no more rows.

### 范例

**示例 \#1 <span class="function">sybase\_fetch\_object</span> return as
Foo**

``` php
<?php
    class Foo {
        var $foo, $bar, $baz;
    }

    // {...]
    $qrh= sybase_query('SELECT foo, bar, baz FROM example');
    $foo= sybase_fetch_object($qrh, 'Foo');
    $bar= sybase_fetch_object($qrh, new Foo());
    // {...]
?>
```

### 参见

-   <span class="function">sybase\_fetch\_array</span>
-   <span class="function">sybase\_fetch\_row</span>

sybase\_fetch\_row
==================

Get a result row as an enumerated array

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">array</span> <span
class="methodname">sybase\_fetch\_row</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">sybase\_fetch\_row</span> fetches one row of data
from the result associated with the specified result identifier.

Subsequent call to <span class="function">sybase\_fetch\_row</span>
would return the next row in the result set, or **`FALSE`** if there are
no more rows.

### 参数

`result`  

### 返回值

Returns an array that corresponds to the fetched row, or **`FALSE`** if
there are no more rows. Each result column is stored in an array offset,
starting at offset 0.

| PHP        | Sybase                                                                        |
|------------|-------------------------------------------------------------------------------|
| string     | VARCHAR, TEXT, CHAR, IMAGE, BINARY, VARBINARY, DATETIME                       |
| int        | NUMERIC (w/o precision), DECIMAL (w/o precision), INT, BIT, TINYINT, SMALLINT |
| float      | NUMERIC (w/ precision), DECIMAL (w/ precision), REAL, FLOAT, MONEY            |
| **`NULL`** | NULL                                                                          |

### 参见

-   <span class="function">sybase\_fetch\_array</span>
-   <span class="function">sybase\_fetch\_assoc</span>
-   <span class="function">sybase\_fetch\_object</span>
-   <span class="function">sybase\_data\_seek</span>
-   <span class="function">sybase\_result</span>

sybase\_field\_seek
===================

Sets field offset

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">sybase\_field\_seek</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span>
`$field_offset`</span> )

Seeks to the specified field offset. If the next call to <span
class="function">sybase\_fetch\_field</span> won't include a field
offset, this field would be returned.

### 参数

`result`  

`field_offset`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">sybase\_fetch\_field</span>

sybase\_free\_result
====================

Frees result memory

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">sybase\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">sybase\_free\_result</span> only needs to be
called if you are worried about using too much memory while your script
is running. All result memory will automatically be freed when the
script ends. You may call <span
class="function">sybase\_free\_result</span> with the result identifier
as an argument and the associated result memory will be freed.

### 参数

`result`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

sybase\_get\_last\_message
==========================

Returns the last message from the server

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">string</span> <span
class="methodname">sybase\_get\_last\_message</span> ( <span
class="methodparam">void</span> )

<span class="function">sybase\_get\_last\_message</span> returns the
last message reported by the server.

### 返回值

Returns the message as a string.

### 参见

-   <span class="function">sybase\_min\_message\_severity</span>

sybase\_min\_client\_severity
=============================

Sets minimum client severity

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">sybase\_min\_client\_severity</span> ( <span
class="methodparam"><span class="type">int</span> `$severity`</span> )

<span class="function">sybase\_min\_client\_severity</span> sets the
minimum client severity level.

### 参数

`severity`  

### 返回值

没有返回值。

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

### 参见

-   <span class="function">sybase\_min\_server\_severity</span>

sybase\_min\_error\_severity
============================

Sets minimum error severity

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">sybase\_min\_error\_severity</span> ( <span
class="methodparam"><span class="type">int</span> `$severity`</span> )

<span class="function">sybase\_min\_error\_severity</span> sets the
minimum error severity level.

### 参数

`severity`  

### 返回值

没有返回值。

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

### 参见

-   <span class="function">sybase\_min\_message\_severity</span>

sybase\_min\_message\_severity
==============================

Sets minimum message severity

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">sybase\_min\_message\_severity</span> ( <span
class="methodparam"><span class="type">int</span> `$severity`</span> )

<span class="function">sybase\_min\_message\_severity</span> sets the
minimum message severity level.

### 参数

`severity`  

### 返回值

没有返回值。

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 DB
> 库接口，而不适用于 CT 库。</span>

### 参见

-   <span class="function">sybase\_min\_error\_severity</span>

sybase\_min\_server\_severity
=============================

Sets minimum server severity

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">void</span> <span
class="methodname">sybase\_min\_server\_severity</span> ( <span
class="methodparam"><span class="type">int</span> `$severity`</span> )

<span class="function">sybase\_min\_server\_severity</span> sets the
minimum server severity level.

### 参数

`severity`  

### 返回值

没有返回值。

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

### 参见

-   <span class="function">sybase\_min\_client\_severity</span>

sybase\_num\_fields
===================

Gets the number of fields in a result set

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">int</span> <span
class="methodname">sybase\_num\_fields</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">sybase\_num\_fields</span> returns the number of
fields in a result set.

### 参数

`result`  

### 返回值

Returns the number of fields as an integer.

### 参见

-   <span class="function">sybase\_query</span>
-   <span class="function">sybase\_fetch\_field</span>
-   <span class="function">sybase\_num\_rows</span>

sybase\_num\_rows
=================

Get number of rows in a result set

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">int</span> <span
class="methodname">sybase\_num\_rows</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
)

<span class="function">sybase\_num\_rows</span> returns the number of
rows in a result set.

### 参数

`result`  

### 返回值

Returns the number of rows as an integer.

### 参见

-   <span class="function">sybase\_num\_fields</span>
-   <span class="function">sybase\_query</span>
-   <span class="function">sybase\_fetch\_row</span>

sybase\_pconnect
================

Open persistent Sybase connection

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">resource</span> <span
class="methodname">sybase\_pconnect</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$servername`</span> \[, <span class="methodparam"><span
class="type">string</span> `$username`</span> \[, <span
class="methodparam"><span class="type">string</span> `$password`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$charset`</span> \[, <span class="methodparam"><span
class="type">string</span> `$appname`</span> \]\]\]\]\] )

<span class="function">sybase\_pconnect</span> acts very much like <span
class="function">sybase\_connect</span> with two major differences.

First, when connecting, the function would first try to find a
(persistent) link that's already open with the same host, username and
password. If one is found, an identifier for it will be returned instead
of opening a new connection.

Second, the connection to the SQL server will not be closed when the
execution of the script ends. Instead, the link will remain open for
future use (<span class="function">sybase\_close</span> will not close
links established by <span class="function">sybase\_pconnect</span>).

This type of links is therefore called 'persistent'.

### 参数

`servername`  
The servername argument has to be a valid servername that is defined in
the 'interfaces' file.

`username`  
Sybase user name

`password`  
Password associated with `username`.

`charset`  
Specifies the charset for the connection

`appname`  
Specifies an *appname* for the Sybase connection. This allow you to make
separate connections in the same script to the same database. This may
come handy when you have started a transaction in your current
connection, and you need to be able to do a separate query which cannot
be performed inside this transaction.

### 返回值

Returns a positive Sybase persistent link identifier on success, or
**`FALSE`** on error.

### 参见

-   <span class="function">sybase\_connect</span>

sybase\_query
=============

Sends a Sybase query

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">mixed</span> <span
class="methodname">sybase\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">sybase\_query</span> sends a query to the
currently active database on the server that's associated with the
specified link identifier.

### 参数

`query`  

`link_identifier`  
If the link identifier isn't specified, the last opened link is assumed.
If no link is open, the function tries to establish a link as if <span
class="function">sybase\_connect</span> was called, and use it.

### 返回值

Returns a positive Sybase result identifier on success, **`FALSE`** on
error, or **`TRUE`** if the query was successful but didn't return any
columns.

### 参见

-   <span class="function">sybase\_select\_db</span>
-   <span class="function">sybase\_connect</span>

sybase\_result
==============

Get result data

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">string</span> <span
class="methodname">sybase\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">int</span> `$row`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$field`</span> )

Returns the contents of the cell at the row and offset in the specified
Sybase result set.

When working on large result sets, you should consider using one of the
functions that fetch an entire row (specified below). As these functions
return the contents of multiple cells in one function call, they're MUCH
quicker than sybase\_result(). Also, note that specifying a numeric
offset for the field argument is much quicker than specifying a
fieldname or tablename.fieldname argument.

Recommended high-performance alternatives: <span
class="function">sybase\_fetch\_row</span>, <span
class="function">sybase\_fetch\_array</span> and <span
class="function">sybase\_fetch\_object</span>.

### 参数

`result`  

`row`  

`field`  
The field argument can be the field's offset, or the field's name, or
the field's table dot field's name (tablename.fieldname). If the column
name has been aliased ('select foo as bar from...'), use the alias
instead of the column name.

### 返回值

<span class="function">sybase\_result</span> returns the contents of one
cell from a Sybase result set.

sybase\_select\_db
==================

Selects a Sybase database

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">sybase\_select\_db</span> ( <span
class="methodparam"><span class="type">string</span>
`$database_name`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \] )

<span class="function">sybase\_select\_db</span> sets the current active
database on the server that's associated with the specified link
identifier.

Every subsequent call to <span class="function">sybase\_query</span>
will be made on the active database.

### 参数

`database_name`  

`link_identifier`  
If no link identifier is specified, the last opened link is assumed. If
no link is open, the function will try to establish a link as if <span
class="function">sybase\_connect</span> was called, and use it.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">sybase\_connect</span>
-   <span class="function">sybase\_pconnect</span>
-   <span class="function">sybase\_query</span>

sybase\_set\_message\_handler
=============================

Sets the handler called when a server message is raised

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">sybase\_set\_message\_handler</span> ( <span
class="methodparam"><span class="type">callable</span> `$handler`</span>
\[, <span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \] )

<span class="function">sybase\_set\_message\_handler</span> sets a user
function to handle messages generated by the server. You may specify the
name of a global function, or use an array to specify an object
reference and a method name.

### 参数

`handler`  
The handler expects five arguments in the following order: message
number, severity, state, line number and description. The first four are
integers. The last is a string. If the function returns **`FALSE`**, PHP
generates an ordinary error message.

`link_identifier`  
If the link identifier isn't specified, the last opened link is assumed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">sybase\_set\_message\_handler</span>
callback function**

``` php
<?php
    function msg_handler($msgnumber, $severity, $state, $line, $text)
    {
        var_dump($msgnumber, $severity, $state, $line, $text);
    }

    sybase_set_message_handler('msg_handler');
?>
```

**示例 \#2 <span class="function">sybase\_set\_message\_handler</span>
callback to a class**

``` php
<?php
    class Sybase {
        function handler($msgnumber, $severity, $state, $line, $text)
        {
            var_dump($msgnumber, $severity, $state, $line, $text);
        }
    }

    $sybase= new Sybase();
    sybase_set_message_handler(array($sybase, 'handler'));
?>
```

**示例 \#3 <span class="function">sybase\_set\_message\_handler</span>
unhandled messages**

``` php
<?php
    // Return FALSE from this function to indicate you can't handle
    // this. The error is printed out as a warning, the way you're used
    // to it if there is no handler installed.
    function msg_handler($msgnumber, $severity, $state, $line, $text)
    {
        if (257 == $msgnumber) {
            return false;
        }
        var_dump($msgnumber, $severity, $state, $line, $text);
    }

    sybase_set_message_handler('msg_handler');
?>
```

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

sybase\_unbuffered\_query
=========================

Send a Sybase query and do not block

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 说明

<span class="type">resource</span> <span
class="methodname">sybase\_unbuffered\_query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$store_result`</span> \] )

<span class="function">sybase\_unbuffered\_query</span> sends a query to
the currently active database on the server that's associated with the
specified link identifier. If the link identifier isn't specified, the
last opened link is assumed. If no link is open, the function tries to
establish a link as if <span class="function">sybase\_connect</span> was
called, and use it.

Unlike <span class="function">sybase\_query</span>, <span
class="function">sybase\_unbuffered\_query</span> reads only the first
row of the result set. <span
class="function">sybase\_fetch\_array</span> and similar function read
more rows as needed. <span class="function">sybase\_data\_seek</span>
reads up to the target row. The behavior may produce better performance
for large result sets.

<span class="function">sybase\_num\_rows</span> will only return the
correct number of rows if all result sets have been read. To Sybase, the
number of rows is not known and is therefore computed by the client
implementation.

> **Note**:
>
> If you don't read all of the resultsets prior to executing the next
> query, PHP will raise a warning and cancel all of the pending results.
> To get rid of this, use <span
> class="function">sybase\_free\_result</span> which will cancel pending
> results of an unbuffered query.

### 参数

`query`  

`link_identifier`  

`store_result`  
The optional `store_result` can be **`FALSE`** to indicate the
resultsets shouldn't be fetched into memory, thus minimizing memory
usage which is particularly interesting with very large resultsets.

### 返回值

Returns a positive Sybase result identifier on success, or **`FALSE`**
on error.

### 范例

**示例 \#1 <span class="function">sybase\_unbuffered\_query</span>
example**

``` php
<?php

$dbh = sybase_connect('SYBASE', '', '');
$q = sybase_unbuffered_query('select firstname, lastname from huge_table', $dbh, false);
sybase_data_seek($q, 10000);
$i = 0;

while ($row = sybase_fetch_row($q)) {
    echo $row[0], ' ', $row[1], '<br />';
    if ($i++ > 40000) {
        break;
    }
}

sybase_free_result($q);
sybase_close($dbh);

?>
```

### 注释

> **Note**: <span class="simpara">此函数仅适用于对 Sybase 使用 CT
> 库接口，而不适用于 DB 库。</span>

### 参见

-   <span class="function">sybase\_query</span>

**目录**

-   [sybase\_affected\_rows](/book/sybase.html#sybase_affected_rows) —
    Gets number of affected rows in last query
-   [sybase\_close](/book/sybase.html#sybase_close) — Closes a Sybase
    connection
-   [sybase\_connect](/book/sybase.html#sybase_connect) — Opens a Sybase
    server connection
-   [sybase\_data\_seek](/book/sybase.html#sybase_data_seek) — Moves
    internal row pointer
-   [sybase\_deadlock\_retry\_count](/book/sybase.html#sybase_deadlock_retry_count)
    — Sets the deadlock retry count
-   [sybase\_fetch\_array](/book/sybase.html#sybase_fetch_array) — Fetch
    row as array
-   [sybase\_fetch\_assoc](/book/sybase.html#sybase_fetch_assoc) — Fetch
    a result row as an associative array
-   [sybase\_fetch\_field](/book/sybase.html#sybase_fetch_field) — Get
    field information from a result
-   [sybase\_fetch\_object](/book/sybase.html#sybase_fetch_object) —
    Fetch a row as an object
-   [sybase\_fetch\_row](/book/sybase.html#sybase_fetch_row) — Get a
    result row as an enumerated array
-   [sybase\_field\_seek](/book/sybase.html#sybase_field_seek) — Sets
    field offset
-   [sybase\_free\_result](/book/sybase.html#sybase_free_result) — Frees
    result memory
-   [sybase\_get\_last\_message](/book/sybase.html#sybase_get_last_message)
    — Returns the last message from the server
-   [sybase\_min\_client\_severity](/book/sybase.html#sybase_min_client_severity)
    — Sets minimum client severity
-   [sybase\_min\_error\_severity](/book/sybase.html#sybase_min_error_severity)
    — Sets minimum error severity
-   [sybase\_min\_message\_severity](/book/sybase.html#sybase_min_message_severity)
    — Sets minimum message severity
-   [sybase\_min\_server\_severity](/book/sybase.html#sybase_min_server_severity)
    — Sets minimum server severity
-   [sybase\_num\_fields](/book/sybase.html#sybase_num_fields) — Gets
    the number of fields in a result set
-   [sybase\_num\_rows](/book/sybase.html#sybase_num_rows) — Get number
    of rows in a result set
-   [sybase\_pconnect](/book/sybase.html#sybase_pconnect) — Open
    persistent Sybase connection
-   [sybase\_query](/book/sybase.html#sybase_query) — Sends a Sybase
    query
-   [sybase\_result](/book/sybase.html#sybase_result) — Get result data
-   [sybase\_select\_db](/book/sybase.html#sybase_select_db) — Selects a
    Sybase database
-   [sybase\_set\_message\_handler](/book/sybase.html#sybase_set_message_handler)
    — Sets the handler called when a server message is raised
-   [sybase\_unbuffered\_query](/book/sybase.html#sybase_unbuffered_query)
    — Send a Sybase query and do not block
