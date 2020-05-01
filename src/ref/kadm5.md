kadm5\_chpass\_principal
========================

Changes the principal's password

### 说明

<span class="type">bool</span> <span
class="methodname">kadm5\_chpass\_principal</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">string</span>
`$principal`</span> , <span class="methodparam"><span
class="type">string</span> `$password`</span> )

<span class="function">kadm5\_chpass\_principal</span> sets the new
password `password` for the `principal`.

### 参数

`handle`  
A KADM5 handle.

`principal`  
The principal.

`password`  
The new password.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Example of changing principal's password**

``` php
<?php

$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

kadm5_chpass_principal($handle, "burbach@GONICUS.LOCAL", "newpassword");

kadm5_destroy($handle);
?>
```

kadm5\_create\_principal
========================

Creates a kerberos principal with the given parameters

### 说明

<span class="type">bool</span> <span
class="methodname">kadm5\_create\_principal</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">string</span>
`$principal`</span> \[, <span class="methodparam"><span
class="type">string</span> `$password`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\] )

Creates a `principal` with the given `password`.

### 参数

`handle`  
A KADM5 handle.

`principal`  
The principal.

`password`  
If `password` is omitted or is **`NULL`**, a random key will be
generated.

`options`  
It is possible to specify several optional parameters within the array
`options`. Allowed are the following options:
**`KADM5_PRINC_EXPIRE_TIME`**, **`KADM5_PW_EXPIRATION`**,
**`KADM5_ATTRIBUTES`**, **`KADM5_MAX_LIFE`**, **`KADM5_KVNO`**,
**`KADM5_POLICY`**, **`KADM5_CLEARPOLICY`**, **`KADM5_MAX_RLIFE`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Example of principal's creation**

``` php
<?php

$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

$attributes = KRB5_KDB_REQUIRES_PRE_AUTH | KRB5_KDB_DISALLOW_PROXIABLE;
$options = array(KADM5_PRINC_EXPIRE_TIME => 0,
                 KADM5_POLICY => "default",
                 KADM5_ATTRIBUTES => $attributes);

kadm5_create_principal($handle, "burbach@GONICUS.LOCAL", "password", $options);

kadm5_destroy($handle);
?>
```

### 参见

-   <span class="function">kadm5\_modify\_principal</span>
-   <span class="function">kadm5\_delete\_principal</span>

kadm5\_delete\_principal
========================

Deletes a kerberos principal

### 说明

<span class="type">bool</span> <span
class="methodname">kadm5\_delete\_principal</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">string</span>
`$principal`</span> )

Removes the `principal` from the Kerberos database.

### 参数

`handle`  
A KADM5 handle.

`principal`  
The removed principal.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">kadm5\_delete\_principal</span>
example**

``` php
<?php

$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

kadm5_delete_principal($handle, "burbach@GONICUS.LOCAL");

kadm5_destroy($handle);
?>
```

### 参见

-   <span class="function">kadm5\_modify\_principal</span>
-   <span class="function">kadm5\_create\_principal</span>

kadm5\_destroy
==============

Closes the connection to the admin server and releases all related
resources

### 说明

<span class="type">bool</span> <span
class="methodname">kadm5\_destroy</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

Closes the connection to the admin server and releases all related
resources.

### 参数

`handle`  
A KADM5 handle.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">kadm5\_init\_with\_password</span>

kadm5\_flush
============

Flush all changes to the Kerberos database

### 说明

<span class="type">bool</span> <span
class="methodname">kadm5\_flush</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> )

Flush all changes to the Kerberos database, leaving the connection to
the Kerberos admin server open.

### 参数

`handle`  
A KADM5 handle.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

kadm5\_get\_policies
====================

Gets all policies from the Kerberos database

### 说明

<span class="type">array</span> <span
class="methodname">kadm5\_get\_policies</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

Gets an array containing the policies's names.

### 参数

`handle`  
A KADM5 handle.

### 返回值

Returns array of policies on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">kadm5\_get\_policies</span> example**

``` php
<?php
$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

print "<h1>get_policies</h1>\n";
foreach (kadm5_get_policies($handle) as $policy) {
    echo "$policy<br />\n";
}

kadm5_destroy($handle);
?>
```

kadm5\_get\_principal
=====================

Gets the principal's entries from the Kerberos database

### 说明

<span class="type">array</span> <span
class="methodname">kadm5\_get\_principal</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">string</span>
`$principal`</span> )

Gets the principal's entries from the Kerberos database.

### 参数

`handle`  
A KADM5 handle.

`principal`  
The principal.

### 返回值

Returns array of options containing the following keys:
KADM5\_PRINCIPAL, KADM5\_PRINC\_EXPIRE\_TIME, KADM5\_PW\_EXPIRATION,
KADM5\_ATTRIBUTES, KADM5\_MAX\_LIFE, KADM5\_MOD\_NAME, KADM5\_MOD\_TIME,
KADM5\_KVNO, KADM5\_POLICY, KADM5\_MAX\_RLIFE, KADM5\_LAST\_SUCCESS,
KADM5\_LAST\_FAILED, KADM5\_FAIL\_AUTH\_COUNT on success
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">kadm5\_get\_principal</span> example**

``` php
<?php
$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

print "<h1>get_principal burbach@GONICUS.LOCAL</h1>\n";

$options = kadm5_get_principal($handle, "burbach@GONICUS.LOCAL" );

foreach ($options as $key => $value) {
    echo "$key: $value<br />\n";
}

kadm5_destroy($handle);
?>
```

### 参见

-   <span class="function">kadm5\_get\_principals</span>

kadm5\_get\_principals
======================

Gets all principals from the Kerberos database

### 说明

<span class="type">array</span> <span
class="methodname">kadm5\_get\_principals</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="function">kadm5\_get\_principals</span> returns an array
containing the principals's names.

### 参数

`handle`  
A KADM5 handle.

### 返回值

Returns array of principals on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">kadm5\_get\_principals</span>
example**

``` php
<?php
$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

print "<h1>get_principals</h1>\n";
foreach (kadm5_get_principals($handle) as $principal) {
    echo "$principal<br />\n";
}

kadm5_destroy($handle);
?>
```

### 参见

-   <span class="function">kadm5\_get\_principal</span>

kadm5\_init\_with\_password
===========================

Opens a connection to the KADM5 library

### 说明

<span class="type">resource</span> <span
class="methodname">kadm5\_init\_with\_password</span> ( <span
class="methodparam"><span class="type">string</span>
`$admin_server`</span> , <span class="methodparam"><span
class="type">string</span> `$realm`</span> , <span
class="methodparam"><span class="type">string</span> `$principal`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> )

Opens a connection with the KADM5 library using the `principal` and the
given `password` to obtain initial credentials from the `admin_server`.

### 参数

`admin_server`  
The server.

`realm`  
Defines the authentication domain for the connection.

`principal`  
The principal.

`password`  
If `password` is omitted or is **`NULL`**, a random key will be
generated.

### 返回值

Returns a KADM5 handle on success 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 KADM5 initialization example**

``` php
<?php

$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

$attributes = KRB5_KDB_REQUIRES_PRE_AUTH | KRB5_KDB_DISALLOW_PROXIABLE;
$options = array(KADM5_PRINC_EXPIRE_TIME => 0,
                 KADM5_POLICY => "default",
                 KADM5_ATTRIBUTES => $attributes);

kadm5_create_principal($handle, "burbach@GONICUS.LOCAL", "password", $options);

kadm5_destroy($handle);
?>
```

### 注释

> **Note**:
>
> Connection should be closed after use with <span
> class="function">kadm5\_destroy</span>.

### 参见

-   <span class="function">kadm5\_destroy</span>

kadm5\_modify\_principal
========================

Modifies a kerberos principal with the given parameters

### 说明

<span class="type">bool</span> <span
class="methodname">kadm5\_modify\_principal</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">string</span>
`$principal`</span> , <span class="methodparam"><span
class="type">array</span> `$options`</span> )

Modifies a `principal` according to the given `options`.

### 参数

`handle`  
A KADM5 handle.

`principal`  
The principal.

`options`  
It is possible to specify several optional parameters within the array
`options`. Allowed are the following options:
**`KADM5_PRINC_EXPIRE_TIME`**, **`KADM5_PW_EXPIRATION`**,
**`KADM5_ATTRIBUTES`**, **`KADM5_MAX_LIFE`**, **`KADM5_KVNO`**,
**`KADM5_POLICY`**, **`KADM5_CLEARPOLICY`**, **`KADM5_MAX_RLIFE`**.
**`KADM5_FAIL_AUTH_COUNT`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Example of modifying principal**

``` php
<?php

$handle = kadm5_init_with_password("afs-1", "GONICUS.LOCAL", "admin/admin", "password");

$attributes = KRB5_KDB_REQUIRES_PRE_AUTH;
$options = array(KADM5_PRINC_EXPIRE_TIME => 3451234,
                 KADM5_POLICY => "gonicus",
                 KADM5_ATTRIBUTES => $attributes);

kadm5_modify_principal($handle, "burbach@GONICUS.LOCAL", $options);

kadm5_destroy($handle);
?>
```

### 参见

-   <span class="function">kadm5\_create\_principal</span>
-   <span class="function">kadm5\_delete\_principal</span>

**目录**

-   [kadm5\_chpass\_principal](/ref/kadm5.html#kadm5_chpass_principal) —
    Changes the principal's password
-   [kadm5\_create\_principal](/ref/kadm5.html#kadm5_create_principal) —
    Creates a kerberos principal with the given parameters
-   [kadm5\_delete\_principal](/ref/kadm5.html#kadm5_delete_principal) —
    Deletes a kerberos principal
-   [kadm5\_destroy](/ref/kadm5.html#kadm5_destroy) — Closes the
    connection to the admin server and releases all related resources
-   [kadm5\_flush](/ref/kadm5.html#kadm5_flush) — Flush all changes to
    the Kerberos database
-   [kadm5\_get\_policies](/ref/kadm5.html#kadm5_get_policies) — Gets
    all policies from the Kerberos database
-   [kadm5\_get\_principal](/ref/kadm5.html#kadm5_get_principal) — Gets
    the principal's entries from the Kerberos database
-   [kadm5\_get\_principals](/ref/kadm5.html#kadm5_get_principals) —
    Gets all principals from the Kerberos database
-   [kadm5\_init\_with\_password](/ref/kadm5.html#kadm5_init_with_password)
    — Opens a connection to the KADM5 library
-   [kadm5\_modify\_principal](/ref/kadm5.html#kadm5_modify_principal) —
    Modifies a kerberos principal with the given parameters
