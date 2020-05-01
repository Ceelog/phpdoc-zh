I have at the moment not very much time to further develop this
extension. I will implement more and more features in the near future.

If you have comments, bug fixes, enhancements or want to help developing
this, you can drop me a mail at
<a href="mailto:yohgaki@php.net" class="link external">» yohgaki@php.net</a>.
Any help is very welcome.

session\_pgsql\_add\_error
==========================

Increments error counts and sets last error message

### 说明

<span class="type">bool</span> <span
class="methodname">session\_pgsql\_add\_error</span> ( <span
class="methodparam"><span class="type">int</span> `$error_level`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$error_message`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`error_level`  

`error_message`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">session\_pgsql\_get\_error</span>

session\_pgsql\_get\_error
==========================

Returns number of errors and last error message

### 说明

<span class="type">array</span> <span
class="methodname">session\_pgsql\_get\_error</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$with_error_message`<span class="initializer"> =
**`FALSE`**</span></span> \] )

Get the number of errors and optional the error messages.

### 参数

`with_error_message`  
Set to **`TRUE`** the literal error message for each error is also
returned.

### 返回值

The number of errors are returned as <span class="type">array</span>.

### 参见

-   <span class="function">session\_pgsql\_add\_error</span>

session\_pgsql\_get\_field
==========================

Get custom field value

### 说明

<span class="type">string</span> <span
class="methodname">session\_pgsql\_get\_field</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">session\_pgsql\_set\_field</span>

session\_pgsql\_reset
=====================

Reset connection to session database servers

### 说明

<span class="type">bool</span> <span
class="methodname">session\_pgsql\_reset</span> ( <span
class="methodparam">void</span> )

Reset the connection to the session database servers.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

session\_pgsql\_set\_field
==========================

Set custom field value

### 说明

<span class="type">bool</span> <span
class="methodname">session\_pgsql\_set\_field</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`value`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">session\_pgsql\_get\_field</span>

session\_pgsql\_status
======================

Get current save handler status

### 说明

<span class="type">array</span> <span
class="methodname">session\_pgsql\_status</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

**目录**

-   [session\_pgsql\_add\_error](/ref/session-pgsql.html#session_pgsql_add_error)
    — Increments error counts and sets last error message
-   [session\_pgsql\_get\_error](/ref/session-pgsql.html#session_pgsql_get_error)
    — Returns number of errors and last error message
-   [session\_pgsql\_get\_field](/ref/session-pgsql.html#session_pgsql_get_field)
    — Get custom field value
-   [session\_pgsql\_reset](/ref/session-pgsql.html#session_pgsql_reset)
    — Reset connection to session database servers
-   [session\_pgsql\_set\_field](/ref/session-pgsql.html#session_pgsql_set_field)
    — Set custom field value
-   [session\_pgsql\_status](/ref/session-pgsql.html#session_pgsql_status)
    — Get current save handler status
