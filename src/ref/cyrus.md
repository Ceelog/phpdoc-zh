cyrus\_authenticate
===================

Authenticate against a Cyrus IMAP server

### 说明

<span class="type">void</span> <span
class="methodname">cyrus\_authenticate</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> \[, <span class="methodparam"><span
class="type">string</span> `$mechlist`</span> \[, <span
class="methodparam"><span class="type">string</span> `$service`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$user`</span> \[, <span class="methodparam"><span
class="type">int</span> `$minssf`</span> \[, <span
class="methodparam"><span class="type">int</span> `$maxssf`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$authname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \]\]\]\]\]\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

cyrus\_bind
===========

Bind callbacks to a Cyrus IMAP connection

### 说明

<span class="type">bool</span> <span
class="methodname">cyrus\_bind</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">array</span> `$callbacks`</span>
)

Binds callbacks to a Cyrus IMAP connection.

### 参数

`connection`  
The connection handle.

`callbacks`  
An array of callbacks.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

cyrus\_close
============

Close connection to a Cyrus IMAP server

### 说明

<span class="type">bool</span> <span
class="methodname">cyrus\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> )

Closes the connection to a Cyrus IMAP server.

### 参数

`connection`  
The connection handle.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

cyrus\_connect
==============

Connect to a Cyrus IMAP server

### 说明

<span class="type">resource</span> <span
class="methodname">cyrus\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$port`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`</span> \]\]\] )

Connects to a Cyrus IMAP server.

### 参数

`host`  
The Cyrus IMAP host name.

`port`  
The port number.

`flags`  

### 返回值

Returns a connection handler on success 或者在失败时返回 **`FALSE`**.

cyrus\_query
============

Send a query to a Cyrus IMAP server

### 说明

<span class="type">array</span> <span
class="methodname">cyrus\_query</span> ( <span class="methodparam"><span
class="type">resource</span> `$connection`</span> , <span
class="methodparam"><span class="type">string</span> `$query`</span> )

Sends a query to a Cyrus IMAP server.

### 参数

`connection`  
The connection handle.

`query`  
The query string.

### 返回值

Returns an associative array with the following keys: *text*, *msgno*,
and *keyword*.

cyrus\_unbind
=============

Unbind ...

### 说明

<span class="type">bool</span> <span
class="methodname">cyrus\_unbind</span> ( <span
class="methodparam"><span class="type">resource</span>
`$connection`</span> , <span class="methodparam"><span
class="type">string</span> `$trigger_name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`connection`  
The connection handle.

`trigger_name`  
The trigger name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**目录**

-   [cyrus\_authenticate](/ref/cyrus.html#cyrus_authenticate) —
    Authenticate against a Cyrus IMAP server
-   [cyrus\_bind](/ref/cyrus.html#cyrus_bind) — Bind callbacks to a
    Cyrus IMAP connection
-   [cyrus\_close](/ref/cyrus.html#cyrus_close) — Close connection to a
    Cyrus IMAP server
-   [cyrus\_connect](/ref/cyrus.html#cyrus_connect) — Connect to a Cyrus
    IMAP server
-   [cyrus\_query](/ref/cyrus.html#cyrus_query) — Send a query to a
    Cyrus IMAP server
-   [cyrus\_unbind](/ref/cyrus.html#cyrus_unbind) — Unbind ...
