intl\_error\_name
=================

Get symbolic name for a given error code

### 说明

<span class="type">string</span> <span
class="methodname">intl\_error\_name</span> ( <span
class="methodparam"><span class="type">int</span> `$error_code`</span> )

Return ICU error code name.

### 参数

`error_code`  
ICU error code.

### 返回值

The returned string will be the same as the name of the error code
constant.

### 范例

**示例 \#1 <span class="function">intl\_error\_name</span> example**

``` php
<?php
$coll     = collator_create( 'en_RU' );
$err_code = collator_get_error_code( $coll );

printf( "Symbolic name for %d is %s\n.", $err_code, intl_error_name( $err_code ) );
?>
```

以上例程的输出类似于：

    Symbolic name for -128 is U_USING_FALLBACK_WARNING.

### 参见

-   <span class="function">intl\_is\_failure</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_get\_error\_message</span>

intl\_get\_error\_code
======================

Get the last error code

### 说明

<span class="type">int</span> <span
class="methodname">intl\_get\_error\_code</span> ( <span
class="methodparam">void</span> )

Useful to handle errors occurred in static methods when there's no
object to get error code from.

### 返回值

Error code returned by the last API function call.

### 范例

**示例 \#1 <span class="function">intl\_get\_error\_code</span>
example**

``` php
<?php
$coll = collator_create( '<bad_param>' );
if( !$coll ) {
    handle_error( intl_get_error_code() );
}
?>
```

### 参见

-   <span class="function">intl\_is\_failure</span>
-   <span class="function">intl\_error\_name</span>
-   <span class="function">intl\_get\_error\_message</span>
-   <span class="function">collator\_get\_error\_code</span>
-   <span class="function">numfmt\_get\_error\_code</span>

intl\_get\_error\_message
=========================

Get description of the last error

### 说明

<span class="type">string</span> <span
class="methodname">intl\_get\_error\_message</span> ( <span
class="methodparam">void</span> )

Get error message from last internationalization function called.

### 返回值

Description of an error occurred in the last API function call.

### 范例

**示例 \#1 <span class="function">intl\_get\_error\_message</span>
example**

``` php
<?php
if( Collator::getAvailableLocales() === false ) {
    show_error( intl_get_error_message() );
}
?>
```

### 参见

-   <span class="function">intl\_error\_name</span>
-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">intl\_is\_failure</span>
-   <span class="function">collator\_get\_error\_message</span>
-   <span class="function">numfmt\_get\_error\_message</span>

intl\_is\_failure
=================

Check whether the given error code indicates failure

### 说明

<span class="type">bool</span> <span
class="methodname">intl\_is\_failure</span> ( <span
class="methodparam"><span class="type">int</span> `$error_code`</span> )

### 参数

`error_code`  
is a value that returned by functions: <span
class="function">intl\_get\_error\_code</span>, <span
class="function">collator\_get\_error\_code</span> .

### 返回值

**`true`** if it the code indicates some failure, and **`false`** in
case of success or a warning.

### 范例

**示例 \#1 <span class="function">intl\_is\_failure</span> example**

``` php
<?php
function check( $err_code )
{
    var_export( intl_is_failure( $err_code ) );
    echo "\n";
}

check( U_ZERO_ERROR );
check( U_USING_FALLBACK_WARNING );
check( U_ILLEGAL_ARGUMENT_ERROR );
?>
```

以上例程的输出类似于：

    false
    false
    true

### 参见

-   <span class="function">intl\_get\_error\_code</span>
-   <span class="function">collator\_get\_error\_code</span>
-   <span class="function">Collator-getErrorCode</span>

**目录**

-   [intl\_error\_name](/ref/intl.html#intl_error_name) — Get symbolic
    name for a given error code
-   [intl\_get\_error\_code](/ref/intl.html#intl_get_error_code) — Get
    the last error code
-   [intl\_get\_error\_message](/ref/intl.html#intl_get_error_message) —
    Get description of the last error
-   [intl\_is\_failure](/ref/intl.html#intl_is_failure) — Check whether
    the given error code indicates failure
