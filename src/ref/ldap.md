ldap\_8859\_to\_t61
===================

Translate 8859 characters to t61 characters

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_8859\_to\_t61</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

Translate *ISO-8859* characters to *t61* characters.

This function is useful if you have to talk to a legacy *LDAPv2* server.

### 参数

`value`  
The text to be translated.

### 返回值

Return the *t61* translation of `value`.

### 参见

-   <span class="function">ldap\_t61\_to\_8859</span>

ldap\_add\_ext
==============

Add entries to LDAP directory

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_add\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Does the same thing as <span class="function">ldap\_add</span> but
returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_add</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">ldap\_add</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_add
=========

Add entries to LDAP directory

### 说明

<span class="type">bool</span> <span class="methodname">ldap\_add</span>
( <span class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Add entries in the LDAP directory.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`entry`  
An array that specifies the information about the entry. The values in
the entries are indexed by individual attributes. In case of multiple
values for an attribute, they are indexed using integers starting
with 0.

``` php
<?php
$entry["attribute1"] = "value";
$entry["attribute2"][0] = "value1";
$entry["attribute2"][1] = "value2";
?>
```

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

**示例 \#1 Complete example with authenticated bind**

``` php
<?php
$ds = ldap_connect("localhost");  // assuming the LDAP server is on this host

if ($ds) {
    // bind with appropriate dn to give update access
    $r = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");

    // prepare data
    $info["cn"] = "John Jones";
    $info["sn"] = "Jones";
    $info["objectclass"] = "person";

    // add data to directory
    $r = ldap_add($ds, "cn=John Jones, o=My Company, c=US", $info);

    ldap_close($ds);
} else {
    echo "Unable to connect to LDAP server";
}
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">ldap\_add\_ext</span>
-   <span class="function">ldap\_delete</span>

ldap\_bind\_ext
===============

Bind to LDAP directory

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_bind\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> \[, <span class="methodparam"><span
class="type">string</span> `$bind_rdn`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$bind_password`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$serverctrls`<span class="initializer"> =
array()</span></span> \]\]\] )

Does the same thing as <span class="function">ldap\_bind</span> but
returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_bind</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_bind</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_bind
==========

绑定 LDAP 目录

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_bind</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> \[, <span
class="methodparam"><span class="type">string</span> `$bind_rdn`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$bind_password`<span class="initializer"> = **`NULL`**</span></span>
\]\] )

使用指定的 RDN 和密码绑定到 LDAP 目录。

### 参数

`link_identifier`  
通过 <span class="function">ldap\_connect</span> 连接之后返回的 LDAP
连接标识。

`bind_rdn`  

`bind_password`  

如果没有指定 `bind_rdn` 和 `bind_password` ，将会以匿名身份绑定。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 使用 LDAP Bind**

``` php
<?php

// using ldap bind
$ldaprdn  = 'uname';     // ldap rdn or dn
$ldappass = 'password';  // associated password

// connect to ldap server
$ldapconn = ldap_connect("ldap.example.com")
    or die("Could not connect to LDAP server.");

if ($ldapconn) {

    // binding to ldap server
    $ldapbind = ldap_bind($ldapconn, $ldaprdn, $ldappass);

    // verify binding
    if ($ldapbind) {
        echo "LDAP bind successful...";
    } else {
        echo "LDAP bind failed...";
    }

}

?>
```

**示例 \#2 Using LDAP Bind Anonymously**

``` php
<?php

//using ldap bind anonymously

// connect to ldap server
$ldapconn = ldap_connect("ldap.example.com")
    or die("Could not connect to LDAP server.");

if ($ldapconn) {

    // binding anonymously
    $ldapbind = ldap_bind($ldapconn);

    if ($ldapbind) {
        echo "LDAP bind anonymous successful...";
    } else {
        echo "LDAP bind anonymous failed...";
    }

}

?>
```

### 参见

-   <span class="function">ldap\_unbind</span>

ldap\_close
===========

别名 <span class="function">ldap\_unbind</span>

### 说明

此函数是该函数的别名： <span class="function">ldap\_unbind</span>.

ldap\_compare
=============

Compare value of attribute found in entry specified with DN

### 说明

<span class="type">mixed</span> <span
class="methodname">ldap\_compare</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">array</span> `$serverctrls`<span class="initializer"> =
array()</span></span> \] )

Compare `value` of `attribute` with value of same attribute in an LDAP
directory entry.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`attribute`  
The attribute name.

`value`  
The compared value.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

Returns **`TRUE`** if `value` matches otherwise returns **`FALSE`**.
Returns -1 on error.

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

The following example demonstrates how to check whether or not given
password matches the one defined in DN specified entry.

**示例 \#1 Complete example of password check**

``` php
<?php

$ds=ldap_connect("localhost");  // assuming the LDAP server is on this host

if ($ds) {

    // bind
    if (ldap_bind($ds)) {

        // prepare data
        $dn = "cn=Matti Meikku, ou=My Unit, o=My Company, c=FI";
        $value = "secretpassword";
        $attr = "password";

        // compare value
        $r=ldap_compare($ds, $dn, $attr, $value);

        if ($r === -1) {
            echo "Error: " . ldap_error($ds);
        } elseif ($r === true) {
            echo "Password correct.";
        } elseif ($r === false) {
            echo "Wrong guess! Password incorrect.";
        }

    } else {
        echo "Unable to bind to LDAP server.";
    }

    ldap_close($ds);

} else {
    echo "Unable to connect to LDAP server.";
}
?>
```

### 注释

**Warning**

<span class="function">ldap\_compare</span> can NOT be used to compare
BINARY values!

ldap\_connect
=============

Connect to an LDAP server

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ldap_uri`<span
class="initializer"> = **`NULL`**</span></span> \] )

**Warning**

The *following* signature is still supported for backwards
compatibility, but is considered deprecated and should not be used
anymore!

<span class="type">resource</span> <span
class="methodname">ldap\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 389</span></span> \]\] )

Creates an LDAP link identifier and checks whether the given `host` and
`port` are plausible.

> **Note**: <span class="simpara"> This function does *not* open a
> connection. It checks whether the given parameters are plausible and
> can be used to open a connection as soon as one is needed. </span>

### 参数

`ldap_uri`  
A full LDAP URI of the form *ldap://hostname:port* or
*ldaps://hostname:port* for SSL encryption.

You can also provide multiple LDAP-URIs separated by a space as one
string

Note that *hostname:port* is not a supported LDAP URI as the schema is
missing.

`host`  
The hostname to connect to.

`port`  
The port to connect to.

### 返回值

Returns a positive LDAP link identifier when the provided LDAP URI seems
plausible. It's a syntactic check of the provided parameter but the
server(s) will not be contacted! If the syntactic check fails it returns
**`FALSE`**. <span class="function">ldap\_connect</span> will otherwise
return a <span class="type">resource</span> as it does not actually
connect but just initializes the connecting parameters. The actual
connect happens with the next calls to ldap\_\* funcs, usually with
<span class="function">ldap\_bind</span>.

If no argument is specified then the link identifier of the already
opened link will be returned.

### 范例

**示例 \#1 Example of connecting to LDAP server.**

``` php
<?php

// LDAP variables
$ldapuri = "ldap://ldap.example.com:389";  // your ldap-uri

// Connecting to LDAP
$ldapconn = ldap_connect($ldapuri)
          or die("That LDAP-URI was not parseable");

?>
```

**示例 \#2 Example of connecting securely to LDAP server.**

``` php
<?php

// make sure your host is the correct one
// that you issued your secure certificate to
$ldaphost = "ldaps://ldap.example.com/";

// Connecting to LDAP
$ldapconn = ldap_connect($ldaphost)
          or die("That LDAP-URI was not parseable");

?>
```

### 参见

-   <span class="function">ldap\_bind</span>

ldap\_control\_paged\_result\_response
======================================

Retrieve the LDAP pagination cookie

**Warning**

This function has been *DEPRECATED* as of PHP 7.4.0. Relying on this
function is highly discouraged.

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_control\_paged\_result\_response</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$result`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$cookie`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$estimated`</span>
\]\] )

Retrieve the pagination information send by the server.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result`  

`cookie`  
An opaque structure sent by the server.

`estimated`  
The estimated number of entries to retrieve.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 7.4.0 | This function has been deprecated. |

### 参见

-   <span class="function">ldap\_control\_paged\_result</span>
-   <a href="http://www.faqs.org/rfcs/rfc2696" class="link external">» RFC2696 : LDAP Control Extension for Simple Paged Results Manipulation</a>

ldap\_control\_paged\_result
============================

Send LDAP pagination control

**Warning**

This function has been *DEPRECATED* as of PHP 7.4.0. Relying on this
function is highly discouraged.

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_control\_paged\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$iscritical`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$cookie`<span class="initializer"> =
""</span></span> \]\] )

Enable LDAP pagination by sending the pagination control (page size,
cookie...).

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`pagesize`  
The number of entries by page.

`iscritical`  
Indicates whether the pagination is critical or not. If true and if the
server doesn't support pagination, the search will return no result.

`cookie`  
An opaque structure sent by the server (<span
class="function">ldap\_control\_paged\_result\_response</span>).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 7.4.0 | This function has been deprecated. |

### 范例

The example below show the retrieval of the first page of a search
paginated with one entry by page.

**示例 \#1 LDAP pagination**

``` php
<?php
     // $ds is a valid link identifier (see ldap_connect)
     ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3);

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     // enable pagination with a page size of 1.
     ldap_control_paged_result($ds, 1);

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     $info = ldap_get_entries($ds, $sr);

     echo $info['count'] . ' entries returned' . PHP_EOL;
```

The example below show the retrieval of all the result paginated with
100 entries by page.

**示例 \#2 LDAP pagination**

``` php
<?php
     // $ds is a valid link identifier (see ldap_connect)
     ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3);

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     // enable pagination with a page size of 100.
     $pageSize = 100;

     $cookie = '';
     do {
         ldap_control_paged_result($ds, $pageSize, true, $cookie);

         $result  = ldap_search($ds, $dn, $filter, $justthese);
         $entries = ldap_get_entries($ds, $result);
             
         foreach ($entries as $e) {
             echo $e['dn'] . PHP_EOL;
         }

         ldap_control_paged_result_response($ds, $result, $cookie);
       
     } while($cookie !== null && $cookie != '');
```

### 注释

> **Note**:
>
> Pagination control is a LDAPv3 protocol feature.

### 参见

-   <span class="function">ldap\_control\_paged\_result\_response</span>
-   <a href="http://www.faqs.org/rfcs/rfc2696" class="link external">» RFC2696 : LDAP Control Extension for Simple Paged Results Manipulation</a>

ldap\_count\_entries
====================

Count the number of entries in a search

### 说明

<span class="type">int</span> <span
class="methodname">ldap\_count\_entries</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_identifier`</span> )

Returns the number of entries stored in the result of previous search
operations.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_identifier`  
The internal LDAP result.

### 返回值

Returns number of entries in the result or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">ldap-count-entries</span> example**

Retrieve number of entries in the result.

``` php
// $ds is a valid link identifier (see ldap_connect)

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     var_dump(ldap_count_entries($ds, $sr));
```

以上例程的输出类似于：

         int(1)
         

ldap\_delete\_ext
=================

Delete an entry from a directory

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_delete\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> \[, <span
class="methodparam"><span class="type">array</span> `$serverctrls`<span
class="initializer"> = array()</span></span> \] )

Does the same thing as <span class="function">ldap\_delete</span> but
returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_delete</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_delete</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_delete
============

Delete an entry from a directory

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$dn`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Deletes a particular entry in LDAP directory.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 参见

-   <span class="function">ldap\_delete\_ext</span>
-   <span class="function">ldap\_add</span>

ldap\_dn2ufn
============

Convert DN to User Friendly Naming format

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_dn2ufn</span> ( <span class="methodparam"><span
class="type">string</span> `$dn`</span> )

Turns the specified `dn`, into a more user-friendly form, stripping off
type names.

### 参数

`dn`  
The distinguished name of an LDAP entity.

### 返回值

Returns the user friendly name.

ldap\_err2str
=============

Convert LDAP error number into string error message

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_err2str</span> ( <span
class="methodparam"><span class="type">int</span> `$errno`</span> )

Returns the string error message explaining the error number `errno`.
While LDAP errno numbers are standardized, different libraries return
different or even localized textual error messages. Never check for a
specific error message text, but always use an error number to check.

### 参数

`errno`  
The error number.

### 返回值

Returns the error message, as a string.

### 范例

**示例 \#1 Enumerating all LDAP error messages**

``` php
<?php
  for ($i=0; $i<100; $i++) {
    printf("Error $i: %s<br />\n", ldap_err2str($i));
  }
?>
```

### 参见

-   <span class="function">ldap\_errno</span>
-   <span class="function">ldap\_error</span>

ldap\_errno
===========

Return the LDAP error number of the last LDAP command

### 说明

<span class="type">int</span> <span
class="methodname">ldap\_errno</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> )

Returns the standardized error number returned by the last LDAP command.
This number can be converted into a textual error message using <span
class="function">ldap\_err2str</span>.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

### 返回值

Return the LDAP error number of the last LDAP command for this link.

### 范例

Unless you lower your warning level in your `php.ini` sufficiently or
prefix your LDAP commands with @ (at) characters to suppress warning
output, the errors generated will also show up in your HTML output.

**示例 \#1 Generating and catching an error**

``` php
<?php
// This example contains an error, which we will catch.
$ld = ldap_connect("localhost");
$bind = ldap_bind($ld);
// syntax error in filter expression (errno 87),
// must be "objectclass=*" to work.
$res =  @ldap_search($ld, "o=Myorg, c=DE", "objectclass");
if (!$res) {
    echo "LDAP-Errno: " . ldap_errno($ld) . "<br />\n";
    echo "LDAP-Error: " . ldap_error($ld) . "<br />\n";
    die("Argh!<br />\n");
}
$info = ldap_get_entries($ld, $res);
echo $info["count"] . " matching entries.<br />\n";
?>
```

### 参见

-   <span class="function">ldap\_err2str</span>
-   <span class="function">ldap\_error</span>

ldap\_error
===========

Return the LDAP error message of the last LDAP command

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_error</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> )

Returns the string error message explaining the error generated by the
last LDAP command for the given `link_identifier`. While LDAP errno
numbers are standardized, different libraries return different or even
localized textual error messages. Never check for a specific error
message text, but always use an error number to check.

Unless you lower your warning level in your `php.ini` sufficiently or
prefix your LDAP commands with *@* (at) characters to suppress warning
output, the errors generated will also show up in your HTML output.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

### 返回值

Returns string error message.

### 参见

-   <span class="function">ldap\_err2str</span>
-   <span class="function">ldap\_errno</span>

ldap\_escape
============

Escape a string for use in an LDAP filter or DN

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_escape</span> ( <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">string</span> `$ignore`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

Escapes `value` for use in the context implied by `flags`.

### 参数

`value`  
The value to escape.

`ignore`  
Characters to ignore when escaping.

`flags`  
The context the escaped string will be used in: **`LDAP_ESCAPE_FILTER`**
for filters to be used with <span class="function">ldap\_search</span>,
or **`LDAP_ESCAPE_DN`** for DNs. If neither flag is passed, all chars
are escaped.

### 返回值

Returns the escaped string.

### 范例

When building an LDAP filter, you should use ldap\_escape with
LDAP\_ESCAPE\_FILTER flag.

**示例 \#1 Searching for an email address**

``` php
<?php
// $ds is a valid link identifier for a directory server

// $mail is an email address provided by the user in a form

$base   = "o=My Company, c=US";
$filter = "(mail=".ldap_escape($mail, "", LDAP_ESCAPE_FILTER).")";

$sr = ldap_search($ds, $base, $filter, array("sn", "givenname", "mail"));

$info = ldap_get_entries($ds, $sr);

echo $info["count"]." entries returned\n";
?>
```

ldap\_exop\_passwd
==================

PASSWD extended operation helper

### 说明

<span class="type">mixed</span> <span
class="methodname">ldap\_exop\_passwd</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$user`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$oldpw`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$newpw`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">array</span>
`&$serverctrls`</span> \]\]\]\] )

Performs a PASSWD extended operation.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`user`  
dn of the user to change the password of.

`oldpw`  
The old password of this user. May be ommited depending of server
configuration.

`newpw`  
The new password for this user. May be omitted or empty to have a
generated password.

`serverctrls`  
If provided, a password policy request control is send with the request
and this is filled with an array of
<a href="/ldap/controls.html" class="link">LDAP Controls</a> returned
with the request.

### 返回值

Returns the generated password if `newpw` is empty or omitted. Otherwise
returns **`TRUE`** on success and **`FALSE`** on failure.

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

**示例 \#1 PASSWD extended operation**

``` php
<?php
$ds = ldap_connect("localhost");  // assuming the LDAP server is on this host

if ($ds) {
    // bind with appropriate dn to give update access
    $bind = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");
    if (!$bind) {
      echo "Unable to bind to LDAP server";
      exit;
    }

    // use PASSWD EXOP to change the user password for a generated one
    $genpw = ldap_exop_passwd($ds, "cn=root, o=My Company, c=US", "secret");
    if ($genpw) {
      // use the generated password to bind
      $bind = ldap_bind($ds, "cn=root, o=My Company, c=US", $genpw);
    }

    // set the password back to "secret"
    ldap_exop_passwd($ds, "cn=root, o=My Company, c=US", $genpw, "secret");

    ldap_close($ds);
} else {
    echo "Unable to connect to LDAP server";
}
?>
```

### 参见

-   <span class="function">ldap\_exop</span>
-   <span class="function">ldap\_parse\_exop</span>

ldap\_exop\_refresh
===================

Refresh extended operation helper

### 说明

<span class="type">int</span> <span
class="methodname">ldap\_exop\_refresh</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span> `$dn`</span>
, <span class="methodparam"><span class="type">int</span> `$ttl`</span>
)

Performs a Refresh extended operation and returns the data.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
dn of the entry to refresh.

`ttl`  
Time in seconds (between 1 and 31557600) that the client requests that
the entry exists in the directory before being automatically removed.

### 返回值

From RFC: The responseTtl field is the time in seconds which the server
chooses to have as the time-to-live field for that entry. It must not be
any smaller than that which the client requested, and it may be larger.
However, to allow servers to maintain a relatively accurate directory,
and to prevent clients from abusing the dynamic extensions, servers are
permitted to shorten a client-requested time-to-live value, down to a
minimum of 86400 seconds (one day). **`FALSE`** will be returned on
error.

### 参见

-   <span class="function">ldap\_exop</span>

ldap\_exop\_whoami
==================

WHOAMI extended operation helper

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_exop\_whoami</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

Performs a WHOAMI extended operation and returns the data.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

### 返回值

The data returned by the server, or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_exop</span>

ldap\_exop
==========

Performs an extended operation

### 说明

<span class="type">mixed</span> <span
class="methodname">ldap\_exop</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">string</span> `$reqoid`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$reqdata`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`&$retdata`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$retoid`</span> \]\]\]\] )

Performs an extended operation on the specified `link` with `reqoid` the
OID of the operation and `reqdata` the data.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`reqoid`  
The extended operation request OID. You may use one of
**`LDAP_EXOP_START_TLS`**, **`LDAP_EXOP_MODIFY_PASSWD`**,
**`LDAP_EXOP_REFRESH`**, **`LDAP_EXOP_WHO_AM_I`**, **`LDAP_EXOP_TURN`**,
or a string with the OID of the operation you want to send.

`reqdata`  
The extended operation request data. May be NULL for some operations
like **`LDAP_EXOP_WHO_AM_I`**, may also need to be BER encoded.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

`retdata`  
Will be filled with the extended operation response data if provided. If
not provided you may use ldap\_parse\_exop on the result object later to
get this data.

`retoid`  
Will be filled with the response OID if provided, usually equal to the
request OID.

### 返回值

When used with `retdata`, returns **`TRUE`** on success or **`FALSE`**
on error. When used without `retdata`, returns a result identifier or
**`FALSE`** on error.

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

**示例 \#1 Whoami extended operation**

``` php
<?php
$ds = ldap_connect("localhost");  // assuming the LDAP server is on this host

if ($ds) {
    // bind with appropriate dn to give update access
    $bind = ldap_bind($ds, "cn=root, o=My Company, c=US", "secret");
    if (!$bind) {
      echo "Unable to bind to LDAP server";
      exit;
    }

    // Call WHOAMI EXOP
    $r = ldap_exop($ds, LDAP_EXOP_WHO_AM_I);

    // Parse the result object
    ldap_parse_exop($ds, $r, $retdata);
    // Output: string(31) "dn:cn=root, o=My Company, c=US"
    var_dump($retdata);

    // Same thing using $retdata parameter
    $success = ldap_exop($ds, LDAP_EXOP_WHO_AM_I, NULL, NULL, $retdata, $retoid);
    if ($success) {
      var_dump($retdata);
    }

    ldap_close($ds);
} else {
    echo "Unable to connect to LDAP server";
}
?>
```

### 参见

-   <span class="function">ldap\_parse\_result</span>
-   <span class="function">ldap\_parse\_exop</span>
-   <span class="function">ldap\_exop\_whoami</span>
-   <span class="function">ldap\_exop\_refresh</span>
-   <span class="function">ldap\_exop\_passwd</span>

ldap\_explode\_dn
=================

Splits DN into its component parts

### 说明

<span class="type">array</span> <span
class="methodname">ldap\_explode\_dn</span> ( <span
class="methodparam"><span class="type">string</span> `$dn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$with_attrib`</span> )

Splits the DN returned by <span class="function">ldap\_get\_dn</span>
and breaks it up into its component parts. Each part is known as
Relative Distinguished Name, or RDN.

### 参数

`dn`  
The distinguished name of an LDAP entity.

`with_attrib`  
Used to request if the RDNs are returned with only values or their
attributes as well. To get RDNs with the attributes (i.e. in
attribute=value format) set `with_attrib` to 0 and to get only values
set it to 1.

### 返回值

Returns an array of all DN components, 或者在失败时返回 **`FALSE`**. The
first element in the array has *count* key and represents the number of
returned values, next elements are numerically indexed DN components.

ldap\_first\_attribute
======================

Return first attribute

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_first\_attribute</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> )

Gets the first attribute in the given entry. Remaining attributes are
retrieved by calling <span class="function">ldap\_next\_attribute</span>
successively.

Similar to reading entries, attributes are also read one by one from a
particular entry.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

`ber_identifier`  
`ber_identifier` is the identifier to internal memory location pointer.
It is passed by reference. The same `ber_identifier` is passed to <span
class="function">ldap\_next\_attribute</span> , which modifies that
pointer.

> **Note**:
>
> This parameter is no longer used as this is now handled automatically
> by PHP. For backwards compatibility PHP will not throw an error if
> this parameter is passed.

### 返回值

Returns the first attribute in the entry on success and **`FALSE`** on
error.

### 更新日志

| 版本  | 说明                                                                        |
|-------|-----------------------------------------------------------------------------|
| 5.2.4 | The `ber_identifier` was removed. This is now handled automatically by PHP. |

### 参见

-   <span class="function">ldap\_next\_attribute</span>
-   <span class="function">ldap\_get\_attributes</span>

ldap\_first\_entry
==================

Return first result id

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_first\_entry</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_identifier`</span> )

Returns the entry identifier for first entry in the result. This entry
identifier is then supplied to <span
class="function">ldap\_next\_entry</span> routine to get successive
entries from the result.

Entries in the LDAP result are read sequentially using the <span
class="function">ldap\_first\_entry</span> and <span
class="function">ldap\_next\_entry</span> functions.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_identifier`  

### 返回值

Returns the result entry identifier for the first entry on success and
**`FALSE`** on error.

### 参见

-   <span class="function">ldap\_get\_entries</span>

ldap\_first\_reference
======================

Return first reference

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_first\_reference</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$result`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ldap\_free\_result
==================

Free result memory

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_free\_result</span> ( <span
class="methodparam"><span class="type">resource</span>
`$result_identifier`</span> )

Frees up the memory allocated internally to store the result. All result
memory will be automatically freed when the script terminates.

Typically all the memory allocated for the LDAP result gets freed at the
end of the script. In case the script is making successive searches
which return large result sets, <span
class="function">ldap\_free\_result</span> could be called to keep the
runtime memory usage by the script low.

### 参数

`result_identifier`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

ldap\_get\_attributes
=====================

Get attributes from a search result entry

### 说明

<span class="type">array</span> <span
class="methodname">ldap\_get\_attributes</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> )

Reads attributes and values from an entry in the search result.

Having located a specific entry in the directory, you can find out what
information is held for that entry by using this call. You would use
this call for an application which "browses" directory entries and/or
where you do not know the structure of the directory entries. In many
applications you will be searching for a specific attribute such as an
email address or a surname, and won't care what other data is held.

    return_value["count"] = number of attributes in the entry
    return_value[0] = first attribute
    return_value[n] = nth attribute

    return_value["attribute"]["count"] = number of values for attribute
    return_value["attribute"][0] = first value of the attribute
    return_value["attribute"][i] = (i+1)th value of the attribute

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

### 返回值

Returns a complete entry information in a multi-dimensional array on
success and **`FALSE`** on error.

### 范例

**示例 \#1 Show the list of attributes held for a particular directory
entry**

``` php
<?php
// $ds is the link identifier for the directory

// $sr is a valid search result from a prior call to
// one of the ldap directory search calls

$entry = ldap_first_entry($ds, $sr);

$attrs = ldap_get_attributes($ds, $entry);

echo $attrs["count"] . " attributes held for this entry:<p>";

for ($i=0; $i < $attrs["count"]; $i++) {
    echo $attrs[$i] . "<br />";
}
?>
```

### 参见

-   <span class="function">ldap\_first\_attribute</span>
-   <span class="function">ldap\_next\_attribute</span>

ldap\_get\_dn
=============

Get the DN of a result entry

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_get\_dn</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> )

Finds out the DN of an entry in the result.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

### 返回值

Returns the DN of the result entry and **`FALSE`** on error.

ldap\_get\_entries
==================

Get all result entries

### 说明

<span class="type">array</span> <span
class="methodname">ldap\_get\_entries</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_identifier`</span> )

Reads multiple entries from the given result, and then reading the
attributes and multiple values.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_identifier`  

### 返回值

Returns a complete result information in a multi-dimensional array on
success and **`FALSE`** on error.

The structure of the array is as follows. The attribute index is
converted to lowercase. (Attributes are case-insensitive for directory
servers, but not when used as array indices.)

    return_value["count"] = number of entries in the result
    return_value[0] : refers to the details of first entry

    return_value[i]["dn"] =  DN of the ith entry in the result

    return_value[i]["count"] = number of attributes in ith entry
    return_value[i][j] = NAME of the jth attribute in the ith entry in the result

    return_value[i]["attribute"]["count"] = number of values for
                                            attribute in ith entry
    return_value[i]["attribute"][j] = jth value of attribute in ith entry

### 参见

-   <span class="function">ldap\_first\_entry</span>
-   <span class="function">ldap\_next\_entry</span>

ldap\_get\_option
=================

Get the current value for given option

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_get\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$option`</span> , <span
class="methodparam"><span class="type">mixed</span> `&$retval`</span> )

Sets `retval` to the value of the specified option.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`option`  
The parameter `option` can be one of:

| Option                              | Type    | since |
|-------------------------------------|---------|-------|
| **`LDAP_OPT_DEREF`**                | integer |       |
| **`LDAP_OPT_SIZELIMIT`**            | integer |       |
| **`LDAP_OPT_TIMELIMIT`**            | integer |       |
| **`LDAP_OPT_NETWORK_TIMEOUT`**      | integer |       |
| **`LDAP_OPT_PROTOCOL_VERSION`**     | integer |       |
| **`LDAP_OPT_ERROR_NUMBER`**         | integer |       |
| **`LDAP_OPT_DIAGNOSTIC_MESSAGE`**   | integer |       |
| **`LDAP_OPT_REFERRALS`**            | bool    |       |
| **`LDAP_OPT_RESTART`**              | bool    |       |
| **`LDAP_OPT_HOST_NAME`**            | string  |       |
| **`LDAP_OPT_ERROR_STRING`**         | string  |       |
| **`LDAP_OPT_MATCHED_DN`**           | string  |       |
| **`LDAP_OPT_SERVER_CONTROLS`**      | array   |       |
| **`LDAP_OPT_CLIENT_CONTROLS`**      | array   |       |
| **`LDAP_OPT_X_KEEPALIVE_IDLE`**     | int     | 7.1   |
| **`LDAP_OPT_X_KEEPALIVE_PROBES`**   | int     | 7.1   |
| **`LDAP_OPT_X_KEEPALIVE_INTERVAL`** | int     | 7.1   |
| **`LDAP_OPT_X_TLS_CACERTDIR`**      | string  | 7.1   |
| **`LDAP_OPT_X_TLS_CACERTFILE`**     | string  | 7.1   |
| **`LDAP_OPT_X_TLS_CERTFILE`**       | string  | 7.1   |
| **`LDAP_OPT_X_TLS_CIPHER_SUITE`**   | string  | 7.1   |
| **`LDAP_OPT_X_TLS_CRLCHECK`**       | integer | 7.1   |
| **`LDAP_OPT_X_TLS_CRL_NONE`**       | integer | 7.1   |
| **`LDAP_OPT_X_TLS_CRL_PEER`**       | integer | 7.1   |
| **`LDAP_OPT_X_TLS_CRL_ALL`**        | integer | 7.1   |
| **`LDAP_OPT_X_TLS_CRLFILE`**        | string  | 7.1   |
| **`LDAP_OPT_X_TLS_DHFILE`**         | string  | 7.1   |
| **`LDAP_OPT_X_TLS_KEYILE`**         | string  | 7.1   |
| **`LDAP_OPT_X_TLS_PACKAGE`**        | string  | 7.1   |
| **`LDAP_OPT_X_TLS_PROTOCOL_MIN`**   | integer | 7.1   |
| **`LDAP_OPT_X_TLS_RANDOM_FILE`**    | string  | 7.1   |
| **`LDAP_OPT_X_TLS_REQUIRE_CERT`**   | integer |       |

`retval`  
This will be set to the option value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Check protocol version**

``` php
<?php
// $ds is a valid link identifier for a directory server
if (ldap_get_option($ds, LDAP_OPT_PROTOCOL_VERSION, $version)) {
    echo "Using protocol version $version\n";
} else {
    echo "Unable to determine protocol version\n";
}
?>
```

### 注释

> **Note**:
>
> This function is only available when using OpenLDAP 2.x.x OR Netscape
> Directory SDK x.x.

### 参见

-   <span class="function">ldap\_set\_option</span>

ldap\_get\_values\_len
======================

Get all binary values from a result entry

### 说明

<span class="type">array</span> <span
class="methodname">ldap\_get\_values\_len</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
)

Reads all the values of the attribute in the entry in the result.

This function is used exactly like <span
class="function">ldap\_get\_values</span> except that it handles binary
data and not string data.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

`attribute`  

### 返回值

Returns an array of values for the attribute on success and **`FALSE`**
on error. Individual values are accessed by integer index in the array.
The first index is 0. The number of values can be found by indexing
"count" in the resultant array.

### 参见

-   <span class="function">ldap\_get\_values</span>

ldap\_get\_values
=================

Get all values from a result entry

### 说明

<span class="type">array</span> <span
class="methodname">ldap\_get\_values</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
)

Reads all the values of the attribute in the entry in the result.

This call needs a `result_entry_identifier`, so needs to be preceded by
one of the ldap search calls and one of the calls to get an individual
entry.

You application will either be hard coded to look for certain attributes
(such as "surname" or "mail") or you will have to use the <span
class="function">ldap\_get\_attributes</span> call to work out what
attributes exist for a given entry.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

`attribute`  

### 返回值

Returns an array of values for the attribute on success and **`FALSE`**
on error. The number of values can be found by indexing "count" in the
resultant array. Individual values are accessed by integer index in the
array. The first index is 0.

LDAP allows more than one entry for an attribute, so it can, for
example, store a number of email addresses for one person's directory
entry all labeled with the attribute "mail"

``` literallayout
    return_value["count"] = number of values for attribute
    return_value[0] = first value of attribute
    return_value[i] = ith value of attribute
    
```

### 范例

**示例 \#1 List all values of the "mail" attribute for a directory
entry**

``` php
<?php
// $ds is a valid link identifier for a directory server

// $sr is a valid search result from a prior call to
//     one of the ldap directory search calls

// $entry is a valid entry identifier from a prior call to
//        one of the calls that returns a directory entry

$values = ldap_get_values($ds, $entry, "mail");

echo $values["count"] . " email addresses for this entry.<br />";

for ($i=0; $i < $values["count"]; $i++) {
    echo $values[$i] . "<br />";
}
?>
```

### 参见

-   <span class="function">ldap\_get\_values\_len</span>

ldap\_list
==========

Single-level search

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_list</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$base_dn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filter`</span> \[, <span class="methodparam"><span
class="type">array</span> `$attributes`<span class="initializer"> =
array("\*")</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$attrsonly`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$sizelimit`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$timelimit`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$deref`<span class="initializer"> =
LDAP\_DEREF\_NEVER</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$serverctrls`<span class="initializer"> =
array()</span></span> \]\]\]\]\]\] )

Performs the search for a specified `filter` on the directory with the
scope **`LDAP_SCOPE_ONELEVEL`**.

**`LDAP_SCOPE_ONELEVEL`** means that the search should only return
information that is at the level immediately below the `base_dn` given
in the call. (Equivalent to typing "**ls**" and getting a list of files
and folders in the current working directory.)

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`base_dn`  
The base DN for the directory.

`filter`  

`attributes`  
An array of the required attributes, e.g. array("mail", "sn", "cn").
Note that the "dn" is always returned irrespective of which attributes
types are requested.

Using this parameter is much more efficient than the default action
(which is to return all attributes and their associated values). The use
of this parameter should therefore be considered good practice.

`attrsonly`  
Should be set to 1 if only attribute types are wanted. If set to 0 both
attributes types and attribute values are fetched which is the default
behaviour.

`sizelimit`  
Enables you to limit the count of entries fetched. Setting this to 0
means no limit.

> **Note**:
>
> This parameter can NOT override server-side preset sizelimit. You can
> set it lower though.
>
> Some directory server hosts will be configured to return no more than
> a preset number of entries. If this occurs, the server will indicate
> that it has only returned a partial results set. This also occurs if
> you use this parameter to limit the count of fetched entries.

`timelimit`  
Sets the number of seconds how long is spend on the search. Setting this
to 0 means no limit.

> **Note**:
>
> This parameter can NOT override server-side preset timelimit. You can
> set it lower though.

`deref`  
Specifies how aliases should be handled during the search. It can be one
of the following:

-   <span class="simpara"> **`LDAP_DEREF_NEVER`** - (default) aliases
    are never dereferenced. </span>
-   <span class="simpara"> **`LDAP_DEREF_SEARCHING`** - aliases should
    be dereferenced during the search but not when locating the base
    object of the search. </span>
-   <span class="simpara"> **`LDAP_DEREF_FINDING`** - aliases should be
    dereferenced when locating the base object but not during the
    search. </span>
-   <span class="simpara"> **`LDAP_DEREF_ALWAYS`** - aliases should be
    dereferenced always. </span>

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

Returns a search result identifier or **`FALSE`** on error.

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

**示例 \#1 Produce a list of all organizational units of an
organization**

``` php
<?php
// $ds is a valid link identifier for a directory server

$basedn = "o=My Company, c=US";
$justthese = array("ou");

$sr = ldap_list($ds, $basedn, "ou=*", $justthese);

$info = ldap_get_entries($ds, $sr);

for ($i=0; $i < $info["count"]; $i++) {
    echo $info[$i]["ou"][0];
}
?>
```

### 参见

-   <span class="function">ldap\_search</span>

ldap\_mod\_add\_ext
===================

Add attribute values to current attributes

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_mod\_add\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Does the same thing as <span class="function">ldap\_mod\_add</span> but
returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_mod\_add</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_mod\_add</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_mod\_add
==============

Add attribute values to current attributes

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_mod\_add</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Adds one or more attribute values to the specified `dn`. To add a whole
new object see <span class="function">ldap\_add</span> function.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`entry`  
An associative array listing the attirbute values to add. If an
attribute was not existing yet it will be added. If an attribute is
existing you can only add values to it if it supports multiple values.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">ldap\_mod\_add\_ext</span>
-   <span class="function">ldap\_mod\_del</span>
-   <span class="function">ldap\_mod\_replace</span>
-   <span class="function">ldap\_modify\_batch</span>

ldap\_mod\_del\_ext
===================

Delete attribute values from current attributes

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_mod\_del\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Does the same thing as <span class="function">ldap\_mod\_del</span> but
returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_mod\_del</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_mod\_del</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_mod\_del
==============

Delete attribute values from current attributes

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_mod\_del</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Removes one or more attribute values from the specified `dn`. Object
deletions are done by the <span class="function">ldap\_delete</span>
function.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`entry`  

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 参见

-   <span class="function">ldap\_mod\_del\_ext</span>
-   <span class="function">ldap\_mod\_add</span>
-   <span class="function">ldap\_mod\_replace</span>
-   <span class="function">ldap\_modify\_batch</span>

ldap\_mod\_replace\_ext
=======================

Replace attribute values with new ones

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_mod\_replace\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Does the same thing as <span class="function">ldap\_mod\_replace</span>
but returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_mod\_replace</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_mod\_replace</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_mod\_replace
==================

Replace attribute values with new ones

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_mod\_replace</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Replaces one or more attributes from the specified `dn`. It may also add
or remove attributes.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`entry`  
An associative array listing the attributes to replace. Sending an empty
array as value will remove the attribute, while sending an attribute not
existing yet on this entry will add it.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">ldap\_mod\_replace\_ext</span>
-   <span class="function">ldap\_mod\_del</span>
-   <span class="function">ldap\_mod\_add</span>
-   <span class="function">ldap\_modify\_batch</span>

ldap\_modify\_batch
===================

Batch and execute modifications on an LDAP entry

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_modify\_batch</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">array</span> `$entry`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$serverctrls`<span class="initializer"> = array()</span></span> \] )

Modifies an existing entry in the LDAP directory. Allows detailed
specification of the modifications to perform.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`entry`  
An array that specifies the modifications to make. Each entry in this
array is an associative array with two or three keys: *attrib* maps to
the name of the attribute to modify, *modtype* maps to the type of
modification to perform, and (depending on the type of modification)
*values* maps to an array of attribute values relevant to the
modification.

Possible values for *modtype* include:

**`LDAP_MODIFY_BATCH_ADD`**  
Each value specified through *values* is added (as an additional value)
to the attribute named by *attrib*.

**`LDAP_MODIFY_BATCH_REMOVE`**  
Each value specified through *values* is removed from the attribute
named by *attrib*. Any value of the attribute not contained in the
*values* array will remain untouched.

**`LDAP_MODIFY_BATCH_REMOVE_ALL`**  
All values are removed from the attribute named by *attrib*. A *values*
entry must not be provided.

**`LDAP_MODIFY_BATCH_REPLACE`**  
All current values of the attribute named by *attrib* are replaced with
the values specified through *values*.

Note that any value for *attrib* must be a string, any value for
*values* must be an array of strings, and any value for *modtype* must
be one of the LDAP\_MODIFY\_BATCH\_\* constants listed above.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

**示例 \#1 Add a telephone number to a contact**

``` php
<?php
$dn = "cn=John Smith,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "telephoneNumber",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => ["+1 555 555 1717"],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
?>
```

**示例 \#2 Rename a user**

``` php
<?php
$dn = "cn=John Smith,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "sn",
        "modtype" => LDAP_MODIFY_BATCH_REPLACE,
        "values"  => ["Smith-Jones"],
    ],
    [
        "attrib"  => "givenName",
        "modtype" => LDAP_MODIFY_BATCH_REPLACE,
        "values"  => ["Jack"],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
ldap_rename($connection, $dn, "cn=Jack Smith-Jones", NULL, TRUE);
?>
```

**示例 \#3 Add two e-mail addresses to a user**

``` php
<?php
$dn = "cn=Jack Smith-Jones,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "mail",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => [
            "jack.smith@example.com",
            "jack.smith-jones@example.com",
        ],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
?>
```

**示例 \#4 Change a user's password**

``` php
<?php
$dn = "cn=Jack Smith-Jones,ou=Wizards,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "userPassword",
        "modtype" => LDAP_MODIFY_BATCH_REMOVE,
        "values"  => ["Tr0ub4dor&3"],
    ],
    [
        "attrib"  => "userPassword",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => ["correct horse battery staple"],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
?>
```

**示例 \#5 Change a user's password (Active Directory)**

``` php
<?php
function adifyPw($pw)
{
    return iconv("UTF-8", "UTF-16LE", '"' . $pw . '"');
}

$dn = "cn=Jack Smith-Jones,ou=Wizards,dc=ad,dc=example,dc=com";
$modifs = [
    [
        "attrib"  => "unicodePwd",
        "modtype" => LDAP_MODIFY_BATCH_REMOVE,
        "values"  => [adifyPw("Tr0ub4dor&3")],
    ],
    [
        "attrib"  => "unicodePwd",
        "modtype" => LDAP_MODIFY_BATCH_ADD,
        "values"  => [adifyPw("correct horse battery staple")],
    ],
];
ldap_modify_batch($connection, $dn, $modifs);
```

ldap\_modify
============

别名 <span class="function">ldap\_mod\_replace</span>

### 说明

此函数是该函数的别名： <span class="function">ldap\_mod\_replace</span>.

### 参见

-   <span class="function">ldap\_rename</span>

ldap\_next\_attribute
=====================

Get the next attribute in result

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_next\_attribute</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> )

Retrieves the attributes in an entry. The first call to <span
class="function">ldap\_next\_attribute</span> is made with the
`result_entry_identifier` returned from <span
class="function">ldap\_first\_attribute</span>.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

`ber_identifier`  
The internal state of the pointer is maintained by this parameter.

> **Note**:
>
> This parameter is no longer used as this is now handled automatically
> by PHP. For backwards compatibility PHP will not throw an error if
> this parameter is passed.

### 返回值

Returns the next attribute in an entry on success and **`FALSE`** on
error.

### 更新日志

| 版本  | 说明                                                                        |
|-------|-----------------------------------------------------------------------------|
| 5.2.4 | The `ber_identifier` was removed. This is now handled automatically by PHP. |

### 参见

-   <span class="function">ldap\_get\_attributes</span>

ldap\_next\_entry
=================

Get next result entry

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_next\_entry</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">resource</span> `$result_entry_identifier`</span> )

Retrieve the entries stored in the result. Successive calls to the <span
class="function">ldap\_next\_entry</span> return entries one by one till
there are no more entries. The first call to <span
class="function">ldap\_next\_entry</span> is made after the call to
<span class="function">ldap\_first\_entry</span> with the
`result_entry_identifier` as returned from the <span
class="function">ldap\_first\_entry</span>.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_entry_identifier`  

### 返回值

Returns entry identifier for the next entry in the result whose entries
are being read starting with <span
class="function">ldap\_first\_entry</span>. If there are no more entries
in the result then it returns **`FALSE`**.

### 参见

-   <span class="function">ldap\_get\_entries</span>

ldap\_next\_reference
=====================

Get next reference

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_next\_reference</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$entry`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ldap\_parse\_exop
=================

Parse result object from an LDAP extended operation

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_parse\_exop</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$result`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$retdata`</span> \[, <span
class="methodparam"><span class="type">string</span> `&$retoid`</span>
\]\] )

Parse LDAP extended operation data from result object `result`

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result`  
An LDAP result resource, returned by <span
class="function">ldap\_exop</span>.

`retdata`  
Will be filled by the response data.

`retoid`  
Will be filled by the response OID.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ldap\_exop</span>

ldap\_parse\_reference
======================

Extract information from reference entry

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_parse\_reference</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$entry`</span> , <span class="methodparam"><span
class="type">array</span> `&$referrals`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ldap\_parse\_result
===================

Extract information from result

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_parse\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$result`</span> , <span class="methodparam"><span
class="type">int</span> `&$errcode`</span> \[, <span
class="methodparam"><span class="type">string</span>
`&$matcheddn`</span> \[, <span class="methodparam"><span
class="type">string</span> `&$errmsg`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$referrals`</span>
\[, <span class="methodparam"><span class="type">array</span>
`&$serverctrls`</span> \]\]\]\] )

Parses an LDAP search result.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result_identifier`  
An LDAP result resource, returned by <span
class="function">ldap\_list</span> or <span
class="function">ldap\_search</span>.

`errcode`  
A reference to a variable that will be set to the LDAP error code in the
result, or *0* if no error occurred.

`matcheddn`  
A reference to a variable that will be set to a matched DN if one was
recognised within the request, otherwise it will be set to **`NULL`**.

`errmsg`  
A reference to a variable that will be set to the LDAP error message in
the result, or an empty string if no error occurred.

`referrals`  
A reference to a variable that will be set to an <span
class="type">array</span> set to all of the referral strings in the
result, or an empty array if no referrals were returned.

`serverctrls`  
An <span class="type">array</span> of LDAP Controls which have been sent
with the response.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

**示例 \#1 <span class="function">ldap\_parse\_result</span> example**

``` php
<?php
$result = ldap_search($link, "cn=userref,dc=my-domain,dc=com", "(cn=user*)");
$errcode = $dn = $errmsg = $refs =  null;
if (ldap_parse_result($link, $result, $errcode, $dn, $errmsg, $refs)) {
    // do something with $errcode, $dn, $errmsg and $refs
}
?>
```

ldap\_read
==========

Read an entry

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_read</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$base_dn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filter`</span> \[, <span class="methodparam"><span
class="type">array</span> `$attributes`<span class="initializer"> =
array("\*")</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$attrsonly`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$sizelimit`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$timelimit`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$deref`<span class="initializer"> =
LDAP\_DEREF\_NEVER</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$serverctrls`<span class="initializer"> =
array()</span></span> \]\]\]\]\]\] )

Performs the search for a specified `filter` on the directory with the
scope **`LDAP_SCOPE_BASE`**. So it is equivalent to reading an entry
from the directory.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`base_dn`  
The base DN for the directory.

`filter`  
An empty filter is not allowed. If you want to retrieve absolutely all
information for this entry, use a filter of *objectClass=\**. If you
know which entry types are used on the directory server, you might use
an appropriate filter such as *objectClass=inetOrgPerson*.

`attributes`  
An array of the required attributes, e.g. array("mail", "sn", "cn").
Note that the "dn" is always returned irrespective of which attributes
types are requested.

Using this parameter is much more efficient than the default action
(which is to return all attributes and their associated values). The use
of this parameter should therefore be considered good practice.

`attrsonly`  
Should be set to 1 if only attribute types are wanted. If set to 0 both
attributes types and attribute values are fetched which is the default
behaviour.

`sizelimit`  
Enables you to limit the count of entries fetched. Setting this to 0
means no limit.

> **Note**:
>
> This parameter can NOT override server-side preset sizelimit. You can
> set it lower though.
>
> Some directory server hosts will be configured to return no more than
> a preset number of entries. If this occurs, the server will indicate
> that it has only returned a partial results set. This also occurs if
> you use this parameter to limit the count of fetched entries.

`timelimit`  
Sets the number of seconds how long is spend on the search. Setting this
to 0 means no limit.

> **Note**:
>
> This parameter can NOT override server-side preset timelimit. You can
> set it lower though.

`deref`  
Specifies how aliases should be handled during the search. It can be one
of the following:

-   <span class="simpara"> **`LDAP_DEREF_NEVER`** - (default) aliases
    are never dereferenced. </span>
-   <span class="simpara"> **`LDAP_DEREF_SEARCHING`** - aliases should
    be dereferenced during the search but not when locating the base
    object of the search. </span>
-   <span class="simpara"> **`LDAP_DEREF_FINDING`** - aliases should be
    dereferenced when locating the base object but not during the
    search. </span>
-   <span class="simpara"> **`LDAP_DEREF_ALWAYS`** - aliases should be
    dereferenced always. </span>

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

Returns a search result identifier or **`FALSE`** on error.

### 更新日志

| 版本  | 说明                                                                                             |
|-------|--------------------------------------------------------------------------------------------------|
| 4.0.5 | Parallel searches support was added. See <span class="function">ldap\_search</span> for details. |
| 7.3   | Support for `serverctrls` added                                                                  |

ldap\_rename\_ext
=================

Modify the name of an entry

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_rename\_ext</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$dn`</span> , <span
class="methodparam"><span class="type">string</span> `$newrdn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$newparent`</span> , <span class="methodparam"><span
class="type">bool</span> `$deleteoldrdn`</span> \[, <span
class="methodparam"><span class="type">array</span> `$serverctrls`<span
class="initializer"> = array()</span></span> \] )

Does the same thing as <span class="function">ldap\_rename</span> but
returns the LDAP result resource to be parsed with <span
class="function">ldap\_parse\_result</span>.

### 参数

See <span class="function">ldap\_rename</span>

### 返回值

Returns an LDAP result identifier or **`FALSE`** on error.

### 参见

-   <span class="function">ldap\_rename</span>
-   <span class="function">ldap\_parse\_result</span>

ldap\_rename
============

Modify the name of an entry

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_rename</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$dn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$newrdn`</span> , <span class="methodparam"><span
class="type">string</span> `$newparent`</span> , <span
class="methodparam"><span class="type">bool</span>
`$deleteoldrdn`</span> \[, <span class="methodparam"><span
class="type">array</span> `$serverctrls`<span class="initializer"> =
array()</span></span> \] )

The entry specified by `dn` is renamed/moved.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`dn`  
The distinguished name of an LDAP entity.

`newrdn`  
The new RDN.

`newparent`  
The new parent/superior entry.

`deleteoldrdn`  
If **`TRUE`** the old RDN value(s) is removed, else the old RDN value(s)
is retained as non-distinguished values of the entry.

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 注释

> **Note**:
>
> This function currently only works with LDAPv3. You may have to use
> <span class="function">ldap\_set\_option</span> prior to binding to
> use LDAPv3. This function is only available when using OpenLDAP 2.x.x
> OR Netscape Directory SDK x.x.

### 参见

-   <span class="function">ldap\_rename\_ext</span>
-   <span class="function">ldap\_modify</span>

ldap\_sasl\_bind
================

Bind to LDAP directory using SASL

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_sasl\_bind</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$binddn`<span class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$sasl_mech`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$sasl_realm`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$sasl_authc_id`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$sasl_authz_id`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$props`<span class="initializer"> = **`NULL`**</span></span>
\]\]\]\]\]\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**: **Requirement**  
> <span class="simpara"> <span class="function">ldap\_sasl\_bind</span>
> requires SASL support (`sasl.h`). Be sure *--with-ldap-sasl* is used
> when configuring PHP otherwise this function will be undefined.
> </span>

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 5.3.3 | Support on Windows was added. |

ldap\_search
============

Search LDAP tree

### 说明

<span class="type">resource</span> <span
class="methodname">ldap\_search</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> , <span
class="methodparam"><span class="type">string</span> `$base_dn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filter`</span> \[, <span class="methodparam"><span
class="type">array</span> `$attributes`<span class="initializer"> =
array("\*")</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$attrsonly`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$sizelimit`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$timelimit`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$deref`<span class="initializer"> =
LDAP\_DEREF\_NEVER</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$serverctrls`<span class="initializer"> =
array()</span></span> \]\]\]\]\]\] )

Performs the search for a specified filter on the directory with the
scope of **`LDAP_SCOPE_SUBTREE`**. This is equivalent to searching the
entire directory.

From 4.0.5 on it's also possible to do parallel searches. To do this you
use an array of link identifiers, rather than a single identifier, as
the first argument. If you don't want the same base DN and the same
filter for all the searches, you can also use an array of base DNs
and/or an array of filters. Those arrays must be of the same size as the
link identifier array since the first entries of the arrays are used for
one search, the second entries are used for another, and so on. When
doing parallel searches an array of search result identifiers is
returned, except in case of error, then the entry corresponding to the
search will be **`FALSE`**. This is very much like the value normally
returned, except that a result identifier is always returned when a
search was made. There are some rare cases where the normal search
returns **`FALSE`** while the parallel search returns an identifier.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`base_dn`  
The base DN for the directory.

`filter`  
The search filter can be simple or advanced, using boolean operators in
the format described in the LDAP documentation (see the
<a href="https://wiki.mozilla.org/Mozilla_LDAP_SDK_Programmer%27s_Guide/Searching_the_Directory_With_LDAP_C_SDK" class="link external">» Netscape Directory SDK</a>
or
<a href="http://www.faqs.org/rfcs/rfc4515" class="link external">» RFC4515</a>
for full information on filters).

`attributes`  
An array of the required attributes, e.g. *array("mail", "sn", "cn")*.
Note that the "dn" is always returned irrespective of which attributes
types are requested.

Using this parameter is much more efficient than the default action
(which is to return all attributes and their associated values). The use
of this parameter should therefore be considered good practice.

`attrsonly`  
Should be set to 1 if only attribute types are wanted. If set to 0 both
attributes types and attribute values are fetched which is the default
behaviour.

`sizelimit`  
Enables you to limit the count of entries fetched. Setting this to 0
means no limit.

> **Note**:
>
> This parameter can NOT override server-side preset sizelimit. You can
> set it lower though.
>
> Some directory server hosts will be configured to return no more than
> a preset number of entries. If this occurs, the server will indicate
> that it has only returned a partial results set. This also occurs if
> you use this parameter to limit the count of fetched entries.

`timelimit`  
Sets the number of seconds how long is spend on the search. Setting this
to 0 means no limit.

> **Note**:
>
> This parameter can NOT override server-side preset timelimit. You can
> set it lower though.

`deref`  
Specifies how aliases should be handled during the search. It can be one
of the following:

-   <span class="simpara"> **`LDAP_DEREF_NEVER`** - (default) aliases
    are never dereferenced. </span>
-   <span class="simpara"> **`LDAP_DEREF_SEARCHING`** - aliases should
    be dereferenced during the search but not when locating the base
    object of the search. </span>
-   <span class="simpara"> **`LDAP_DEREF_FINDING`** - aliases should be
    dereferenced when locating the base object but not during the
    search. </span>
-   <span class="simpara"> **`LDAP_DEREF_ALWAYS`** - aliases should be
    dereferenced always. </span>

`serverctrls`  
Array of <a href="/ldap/controls.html" class="link">LDAP Controls</a> to
send with the request.

### 返回值

Returns a search result identifier or **`FALSE`** on error.

### 更新日志

| 版本 | 说明                            |
|------|---------------------------------|
| 7.3  | Support for `serverctrls` added |

### 范例

The example below retrieves the organizational unit, surname, given name
and email address for all people in "My Company" where the surname or
given name contains the substring `$person`. This example uses a boolean
filter to tell the server to look for information in more than one
attribute.

**示例 \#1 LDAP search**

``` php
<?php
// $ds is a valid link identifier for a directory server

// $person is all or part of a person's name, eg "Jo"

$dn = "o=My Company, c=US";
$filter="(|(sn=$person*)(givenname=$person*))";
$justthese = array("ou", "sn", "givenname", "mail");

$sr=ldap_search($ds, $dn, $filter, $justthese);

$info = ldap_get_entries($ds, $sr);

echo $info["count"]." entries returned\n";
?>
```

ldap\_set\_option
=================

Set the value of the given option

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$link_identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$option`</span> , <span
class="methodparam"><span class="type">mixed</span> `$newval`</span> )

Sets the value of the specified option to be `newval`.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`option`  
The parameter `option` can be one of:

| Option                              | Type    | Available since |
|-------------------------------------|---------|-----------------|
| **`LDAP_OPT_DEREF`**                | integer |                 |
| **`LDAP_OPT_SIZELIMIT`**            | integer |                 |
| **`LDAP_OPT_TIMELIMIT`**            | integer |                 |
| **`LDAP_OPT_NETWORK_TIMEOUT`**      | integer | PHP 5.3.0       |
| **`LDAP_OPT_PROTOCOL_VERSION`**     | integer |                 |
| **`LDAP_OPT_ERROR_NUMBER`**         | integer |                 |
| **`LDAP_OPT_REFERRALS`**            | bool    |                 |
| **`LDAP_OPT_RESTART`**              | bool    |                 |
| **`LDAP_OPT_HOST_NAME`**            | string  |                 |
| **`LDAP_OPT_ERROR_STRING`**         | string  |                 |
| **`LDAP_OPT_DIAGNOSTIC_MESSAGE`**   | string  |                 |
| **`LDAP_OPT_MATCHED_DN`**           | string  |                 |
| **`LDAP_OPT_SERVER_CONTROLS`**      | array   |                 |
| **`LDAP_OPT_CLIENT_CONTROLS`**      | array   |                 |
| **`LDAP_OPT_X_KEEPALIVE_IDLE`**     | int     | PHP 7.1.0       |
| **`LDAP_OPT_X_KEEPALIVE_PROBES`**   | int     | PHP 7.1.0       |
| **`LDAP_OPT_X_KEEPALIVE_INTERVAL`** | int     | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_CACERTDIR`**      | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_CACERTFILE`**     | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_CERTFILE`**       | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_CIPHER_SUITE`**   | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_CRLCHECK`**       | integer | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_CRLFILE`**        | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_DHFILE`**         | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_KEYFILE`**        | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_PROTOCOL_MIN`**   | integer | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_RANDOM_FILE`**    | string  | PHP 7.1.0       |
| **`LDAP_OPT_X_TLS_REQUIRE_CERT`**   | integer | PHP 7.0.5       |

**`LDAP_OPT_SERVER_CONTROLS`** and **`LDAP_OPT_CLIENT_CONTROLS`**
require a list of controls, this means that the value must be an array
of controls. A control consists of an *oid* identifying the control, an
optional *value*, and an optional flag for *criticality*. In PHP a
control is given by an array containing an element with the key *oid*
and string value, and two optional elements. The optional elements are
key *value* with string value and key *iscritical* with boolean value.
*iscritical* defaults to ***`FALSE`*** if not supplied. See
<a href="http://www.openldap.org/devel/cvsweb.cgi/~checkout~/doc/drafts/draft-ietf-ldapext-ldap-c-api-xx.txt" class="link external">» draft-ietf-ldapext-ldap-c-api-xx.txt</a>
for details. See also the second example below.

`newval`  
The new value for the specified `option`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Set protocol version**

``` php
<?php
// $ds is a valid link identifier for a directory server
if (ldap_set_option($ds, LDAP_OPT_PROTOCOL_VERSION, 3)) {
    echo "Using LDAPv3";
} else {
    echo "Failed to set protocol version to 3";
}
?>
```

**示例 \#2 Set server controls**

``` php
<?php
// $ds is a valid link identifier for a directory server
// control with no value
$ctrl1 = array("oid" => "1.2.752.58.10.1", "iscritical" => true);
// iscritical defaults to FALSE
$ctrl2 = array("oid" => "1.2.752.58.1.10", "value" => "magic");
// try to set both controls
if (!ldap_set_option($ds, LDAP_OPT_SERVER_CONTROLS, array($ctrl1, $ctrl2))) {
    echo "Failed to set server controls";
}
?>
```

### 注释

> **Note**:
>
> This function is only available when using OpenLDAP 2.x.x OR Netscape
> Directory SDK x.x.

### 参见

-   <span class="function">ldap\_get\_option</span>

ldap\_set\_rebind\_proc
=======================

Set a callback function to do re-binds on referral chasing

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_set\_rebind\_proc</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ldap\_sort
==========

Sort LDAP result entries on the client side

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_sort</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">resource</span> `$result`</span>
, <span class="methodparam"><span class="type">string</span>
`$sortfilter`</span> )

Sort the result of a LDAP search, returned by <span
class="function">ldap\_search</span>.

As this function sorts the returned values on the client side it is
possible that you might not get the expected results in case you reach
the `sizelimit` either of the server or defined within <span
class="function">ldap\_search</span>.

**Warning**

This feature has been *DEPRECATED* as of PHP 7.0.0. Relying on this
feature is highly discouraged.

### 参数

`link`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

`result`  
An search result identifier, returned by <span
class="function">ldap\_search</span>.

`sortfilter`  
The attribute to use as a key in the sort.

### 范例

Sorting the result of a search.

**示例 \#1 LDAP sort**

``` php
<?php
     // $ds is a valid link identifier (see ldap_connect)

     $dn        = 'ou=example,dc=org';
     $filter    = '(|(sn=Doe*)(givenname=John*))';
     $justthese = array('ou', 'sn', 'givenname', 'mail');

     $sr = ldap_search($ds, $dn, $filter, $justthese);

     // Sort
     ldap_sort($ds, $sr, 'sn');

     // Retrieving the data
     $info = ldap_get_entries($ds, $sr);
```

ldap\_start\_tls
================

Start TLS

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_start\_tls</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ldap\_t61\_to\_8859
===================

Translate t61 characters to 8859 characters

### 说明

<span class="type">string</span> <span
class="methodname">ldap\_t61\_to\_8859</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ldap\_unbind
============

Unbind from LDAP directory

### 说明

<span class="type">bool</span> <span
class="methodname">ldap\_unbind</span> ( <span class="methodparam"><span
class="type">resource</span> `$link_identifier`</span> )

Unbinds from the LDAP directory.

### 参数

`link_identifier`  
An LDAP link identifier, returned by <span
class="function">ldap\_connect</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">ldap\_bind</span>

**目录**

-   [ldap\_8859\_to\_t61](/ref/ldap.html#ldap_8859_to_t61) — Translate
    8859 characters to t61 characters
-   [ldap\_add\_ext](/ref/ldap.html#ldap_add_ext) — Add entries to LDAP
    directory
-   [ldap\_add](/ref/ldap.html#ldap_add) — Add entries to LDAP directory
-   [ldap\_bind\_ext](/ref/ldap.html#ldap_bind_ext) — Bind to LDAP
    directory
-   [ldap\_bind](/ref/ldap.html#ldap_bind) — 绑定 LDAP 目录
-   [ldap\_close](/ref/ldap.html#ldap_close) — 别名 ldap\_unbind
-   [ldap\_compare](/ref/ldap.html#ldap_compare) — Compare value of
    attribute found in entry specified with DN
-   [ldap\_connect](/ref/ldap.html#ldap_connect) — Connect to an LDAP
    server
-   [ldap\_control\_paged\_result\_response](/ref/ldap.html#ldap_control_paged_result_response)
    — Retrieve the LDAP pagination cookie
-   [ldap\_control\_paged\_result](/ref/ldap.html#ldap_control_paged_result)
    — Send LDAP pagination control
-   [ldap\_count\_entries](/ref/ldap.html#ldap_count_entries) — Count
    the number of entries in a search
-   [ldap\_delete\_ext](/ref/ldap.html#ldap_delete_ext) — Delete an
    entry from a directory
-   [ldap\_delete](/ref/ldap.html#ldap_delete) — Delete an entry from a
    directory
-   [ldap\_dn2ufn](/ref/ldap.html#ldap_dn2ufn) — Convert DN to User
    Friendly Naming format
-   [ldap\_err2str](/ref/ldap.html#ldap_err2str) — Convert LDAP error
    number into string error message
-   [ldap\_errno](/ref/ldap.html#ldap_errno) — Return the LDAP error
    number of the last LDAP command
-   [ldap\_error](/ref/ldap.html#ldap_error) — Return the LDAP error
    message of the last LDAP command
-   [ldap\_escape](/ref/ldap.html#ldap_escape) — Escape a string for use
    in an LDAP filter or DN
-   [ldap\_exop\_passwd](/ref/ldap.html#ldap_exop_passwd) — PASSWD
    extended operation helper
-   [ldap\_exop\_refresh](/ref/ldap.html#ldap_exop_refresh) — Refresh
    extended operation helper
-   [ldap\_exop\_whoami](/ref/ldap.html#ldap_exop_whoami) — WHOAMI
    extended operation helper
-   [ldap\_exop](/ref/ldap.html#ldap_exop) — Performs an extended
    operation
-   [ldap\_explode\_dn](/ref/ldap.html#ldap_explode_dn) — Splits DN into
    its component parts
-   [ldap\_first\_attribute](/ref/ldap.html#ldap_first_attribute) —
    Return first attribute
-   [ldap\_first\_entry](/ref/ldap.html#ldap_first_entry) — Return first
    result id
-   [ldap\_first\_reference](/ref/ldap.html#ldap_first_reference) —
    Return first reference
-   [ldap\_free\_result](/ref/ldap.html#ldap_free_result) — Free result
    memory
-   [ldap\_get\_attributes](/ref/ldap.html#ldap_get_attributes) — Get
    attributes from a search result entry
-   [ldap\_get\_dn](/ref/ldap.html#ldap_get_dn) — Get the DN of a result
    entry
-   [ldap\_get\_entries](/ref/ldap.html#ldap_get_entries) — Get all
    result entries
-   [ldap\_get\_option](/ref/ldap.html#ldap_get_option) — Get the
    current value for given option
-   [ldap\_get\_values\_len](/ref/ldap.html#ldap_get_values_len) — Get
    all binary values from a result entry
-   [ldap\_get\_values](/ref/ldap.html#ldap_get_values) — Get all values
    from a result entry
-   [ldap\_list](/ref/ldap.html#ldap_list) — Single-level search
-   [ldap\_mod\_add\_ext](/ref/ldap.html#ldap_mod_add_ext) — Add
    attribute values to current attributes
-   [ldap\_mod\_add](/ref/ldap.html#ldap_mod_add) — Add attribute values
    to current attributes
-   [ldap\_mod\_del\_ext](/ref/ldap.html#ldap_mod_del_ext) — Delete
    attribute values from current attributes
-   [ldap\_mod\_del](/ref/ldap.html#ldap_mod_del) — Delete attribute
    values from current attributes
-   [ldap\_mod\_replace\_ext](/ref/ldap.html#ldap_mod_replace_ext) —
    Replace attribute values with new ones
-   [ldap\_mod\_replace](/ref/ldap.html#ldap_mod_replace) — Replace
    attribute values with new ones
-   [ldap\_modify\_batch](/ref/ldap.html#ldap_modify_batch) — Batch and
    execute modifications on an LDAP entry
-   [ldap\_modify](/ref/ldap.html#ldap_modify) — 别名 ldap\_mod\_replace
-   [ldap\_next\_attribute](/ref/ldap.html#ldap_next_attribute) — Get
    the next attribute in result
-   [ldap\_next\_entry](/ref/ldap.html#ldap_next_entry) — Get next
    result entry
-   [ldap\_next\_reference](/ref/ldap.html#ldap_next_reference) — Get
    next reference
-   [ldap\_parse\_exop](/ref/ldap.html#ldap_parse_exop) — Parse result
    object from an LDAP extended operation
-   [ldap\_parse\_reference](/ref/ldap.html#ldap_parse_reference) —
    Extract information from reference entry
-   [ldap\_parse\_result](/ref/ldap.html#ldap_parse_result) — Extract
    information from result
-   [ldap\_read](/ref/ldap.html#ldap_read) — Read an entry
-   [ldap\_rename\_ext](/ref/ldap.html#ldap_rename_ext) — Modify the
    name of an entry
-   [ldap\_rename](/ref/ldap.html#ldap_rename) — Modify the name of an
    entry
-   [ldap\_sasl\_bind](/ref/ldap.html#ldap_sasl_bind) — Bind to LDAP
    directory using SASL
-   [ldap\_search](/ref/ldap.html#ldap_search) — Search LDAP tree
-   [ldap\_set\_option](/ref/ldap.html#ldap_set_option) — Set the value
    of the given option
-   [ldap\_set\_rebind\_proc](/ref/ldap.html#ldap_set_rebind_proc) — Set
    a callback function to do re-binds on referral chasing
-   [ldap\_sort](/ref/ldap.html#ldap_sort) — Sort LDAP result entries on
    the client side
-   [ldap\_start\_tls](/ref/ldap.html#ldap_start_tls) — Start TLS
-   [ldap\_t61\_to\_8859](/ref/ldap.html#ldap_t61_to_8859) — Translate
    t61 characters to 8859 characters
-   [ldap\_unbind](/ref/ldap.html#ldap_unbind) — Unbind from LDAP
    directory
