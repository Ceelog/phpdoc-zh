mhash\_count
============

Gets the highest available hash ID

### 说明

<span class="type">int</span> <span
class="methodname">mhash\_count</span> ( <span
class="methodparam">void</span> )

Gets the highest available hash ID.

### 返回值

Returns the highest available hash ID. Hashes are numbered from 0 to
this hash ID.

### 范例

**示例 \#1 Traversing all hashes**

``` php
<?php

$nr = mhash_count();

for ($i = 0; $i <= $nr; $i++) {
    echo sprintf("The blocksize of %s is %d\n",
        mhash_get_hash_name($i),
        mhash_get_block_size($i));
}
?>
```

mhash\_get\_block\_size
=======================

Gets the block size of the specified hash

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">mhash\_get\_block\_size</span> ( <span
class="methodparam"><span class="type">int</span> `$algo`</span> )

Gets the size of a block of the specified `algo`.

### 参数

`algo`  
The hash ID. One of the **`MHASH_hashname`** constants.

### 返回值

Returns the size in bytes or **`false`**, if the `algo` does not exist.

### 范例

**示例 \#1 <span class="function">mhash\_get\_block\_size</span>
Example**

``` php
<?php

echo mhash_get_block_size(MHASH_MD5); // 16

?>
```

mhash\_get\_hash\_name
======================

Gets the name of the specified hash

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">mhash\_get\_hash\_name</span> ( <span
class="methodparam"><span class="type">int</span> `$algo`</span> )

Gets the name of the specified `algo`.

### 参数

`algo`  
The hash ID. One of the **`MHASH_hashname`** constants.

### 返回值

Returns the name of the hash or **`false`**, if the hash does not exist.

### 范例

**示例 \#1 <span class="function">mhash\_get\_hash\_name</span>
Example**

``` php
<?php

echo mhash_get_hash_name(MHASH_MD5); // MD5

?>
```

mhash\_keygen\_s2k
==================

Generates a key

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">mhash\_keygen\_s2k</span> ( <span
class="methodparam"><span class="type">int</span> `$algo`</span> , <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">string</span>
`$salt`</span> , <span class="methodparam"><span class="type">int</span>
`$length`</span> )

Generates a key according to the given `algo`, using an user provided
`password`.

This is the Salted S2K algorithm as specified in the OpenPGP document
(<a href="http://www.faqs.org/rfcs/rfc2440" class="link external">» RFC 2440</a>).

Keep in mind that user supplied passwords are not really suitable to be
used as keys in cryptographic algorithms, since users normally choose
keys they can write on keyboard. These passwords use only 6 to 7 bits
per character (or less). It is highly recommended to use some kind of
transformation (like this function) to the user supplied key.

### 参数

`algo`  
The hash ID used to create the key. One of the **`MHASH_hashname`**
constants.

`password`  
An user supplied password.

`salt`  
Must be different and random enough for every key you generate in order
to create different keys. Because `salt` must be known when you check
the keys, it is a good idea to append the key to it. Salt has a fixed
length of 8 bytes and will be padded with zeros if you supply less
bytes.

`length`  
The key length, in bytes.

### 返回值

Returns the generated key as a string, or **`false`** on error.

mhash
=====

Computes hash

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span class="methodname">mhash</span> (
<span class="methodparam"><span class="type">int</span> `$algo`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$key`<span class="initializer"> = **`null`**</span></span> \] )

<span class="function">mhash</span> applies a hash function specified by
`algo` to the `data`.

### 参数

`algo`  
The hash ID. One of the **`MHASH_hashname`** constants.

`data`  
The user input, as a string.

`key`  
If specified, the function will return the resulting HMAC instead. HMAC
is keyed hashing for message authentication, or simply a message digest
that depends on the specified key. Not all algorithms supported in mhash
can be used in HMAC mode.

### 返回值

Returns the resulting hash (also called digest) or HMAC as a string, or
**`false`** on error.

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 8.0.0 | `key` is now nullable. |

**目录**

-   [mhash\_count](/ref/mhash.html#mhash_count) — Gets the highest
    available hash ID
-   [mhash\_get\_block\_size](/ref/mhash.html#mhash_get_block_size) —
    Gets the block size of the specified hash
-   [mhash\_get\_hash\_name](/ref/mhash.html#mhash_get_hash_name) — Gets
    the name of the specified hash
-   [mhash\_keygen\_s2k](/ref/mhash.html#mhash_keygen_s2k) — Generates a
    key
-   [mhash](/ref/mhash.html#mhash) — Computes hash
