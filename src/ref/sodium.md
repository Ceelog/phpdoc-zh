sodium\_add
===========

Add large numbers

### 说明

<span class="type">void</span> <span
class="methodname">sodium\_add</span> ( <span class="methodparam"><span
class="type">string</span> `&$val`</span> , <span
class="methodparam"><span class="type">string</span> `$addv`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`val`  

`addv`  

### 返回值

没有返回值。

sodium\_base642bin
==================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_base642bin</span> ( <span
class="methodparam"><span class="type">string</span> `$b64`</span> ,
<span class="methodparam"><span class="type">int</span> `$id`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$ignore`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`b64`  

`id`  

`ignore`  

### 返回值

sodium\_bin2base64
==================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_bin2base64</span> ( <span
class="methodparam"><span class="type">string</span> `$bin`</span> ,
<span class="methodparam"><span class="type">int</span> `$id`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`bin`  

`id`  

### 返回值

sodium\_bin2hex
===============

Encode to hexadecimal

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_bin2hex</span> ( <span
class="methodparam"><span class="type">string</span> `$bin`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`bin`  

### 返回值

sodium\_compare
===============

Compare large numbers

### 说明

<span class="type">int</span> <span
class="methodname">sodium\_compare</span> ( <span
class="methodparam"><span class="type">string</span> `$buf1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$buf2`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`buf1`  

`buf2`  

### 返回值

sodium\_crypto\_aead\_aes256gcm\_decrypt
========================================

Decrypt in combined mode with precalculation

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_aes256gcm\_decrypt</span> (
<span class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_aes256gcm\_encrypt
========================================

Encrypt in combined mode with precalculation

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_aes256gcm\_encrypt</span> (
<span class="methodparam"><span class="type">string</span> `$msg`</span>
, <span class="methodparam"><span class="type">string</span>
`$ad`</span> , <span class="methodparam"><span
class="type">string</span> `$nonce`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_aes256gcm\_is\_available
==============================================

Check if hardware supports AES256-GCM

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_aead\_aes256gcm\_is\_available</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_aead\_aes256gcm\_keygen
=======================================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_aes256gcm\_keygen</span> (
<span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_aead\_chacha20poly1305\_decrypt
===============================================

Verify that the ciphertext includes a valid tag

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_chacha20poly1305\_decrypt</span>
( <span class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_chacha20poly1305\_encrypt
===============================================

Encrypt a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_chacha20poly1305\_encrypt</span>
( <span class="methodparam"><span class="type">string</span>
`$msg`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt
=====================================================

Verify that the ciphertext includes a valid tag

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt</span>
( <span class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt
=====================================================

Encrypt a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt</span>
( <span class="methodparam"><span class="type">string</span>
`$msg`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen
====================================================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_aead\_chacha20poly1305\_keygen
==============================================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_chacha20poly1305\_keygen</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt
======================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt</span>
( <span class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt
======================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt</span>
( <span class="methodparam"><span class="type">string</span>
`$msg`</span> , <span class="methodparam"><span
class="type">string</span> `$ad`</span> , <span
class="methodparam"><span class="type">string</span> `$nonce`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`ad`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen
=====================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_auth\_keygen
============================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_auth\_keygen</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_auth\_verify
============================

Verifies that the tag is valid for the message

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_auth\_verify</span> ( <span
class="methodparam"><span class="type">string</span> `$signature`</span>
, <span class="methodparam"><span class="type">string</span>
`$msg`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`signature`  

`msg`  

`key`  

### 返回值

sodium\_crypto\_auth
====================

Compute a tag for the message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_auth</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`key`  

### 返回值

sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey
=============================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey</span>
( <span class="methodparam"><span class="type">string</span>
`$secret_key`</span> , <span class="methodparam"><span
class="type">string</span> `$public_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`secret_key`  

`public_key`  

### 返回值

sodium\_crypto\_box\_keypair
============================

Randomly generate a secret key and a corresponding public key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_keypair</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_box\_open
=========================

Verify and decrypt a ciphertext

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_open</span> ( <span
class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$nonce`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_box\_publickey\_from\_secretkey
===============================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_publickey\_from\_secretkey</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_box\_publickey
==============================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_publickey</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_box\_seal\_open
===============================

Decrypt the ciphertext

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_seal\_open</span> ( <span
class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`key`  

### 返回值

sodium\_crypto\_box\_seal
=========================

Encrypt a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_seal</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`key`  

### 返回值

sodium\_crypto\_box\_secretkey
==============================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_secretkey</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_box\_seed\_keypair
==================================

Deterministically derive the key pair from a single key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box\_seed\_keypair</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_box
===================

Encrypt a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_box</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span>
`$nonce`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_generichash\_final
==================================

Complete the hash

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_generichash\_final</span> ( <span
class="methodparam"><span class="type">string</span> `&$state`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$length`<span class="initializer"> =
SODIUM\_CRYPTO\_GENERICHASH\_BYTES</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`state`  

`length`  

### 返回值

sodium\_crypto\_generichash\_init
=================================

Initialize a hash

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_generichash\_init</span> (\[ <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = SODIUM\_CRYPTO\_GENERICHASH\_BYTES</span></span>
\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

`length`  

### 返回值

sodium\_crypto\_generichash\_keygen
===================================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_generichash\_keygen</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_generichash\_update
===================================

Add message to a hash

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_generichash\_update</span> ( <span
class="methodparam"><span class="type">string</span> `&$state`</span> ,
<span class="methodparam"><span class="type">string</span> `$msg`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`state`  

`msg`  

### 返回值

sodium\_crypto\_generichash
===========================

Get a hash of the message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_generichash</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> \[,
<span class="methodparam"><span class="type">string</span> `$key`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$length`<span class="initializer"> =
SODIUM\_CRYPTO\_GENERICHASH\_BYTES</span></span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`key`  

`length`  

### 返回值

sodium\_crypto\_kdf\_derive\_from\_key
======================================

Derive a subkey

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_kdf\_derive\_from\_key</span> ( <span
class="methodparam"><span class="type">int</span> `$subkey_len`</span> ,
<span class="methodparam"><span class="type">int</span>
`$subkey_id`</span> , <span class="methodparam"><span
class="type">string</span> `$context`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`subkey_len`  

`subkey_id`  

`context`  

`key`  

### 返回值

sodium\_crypto\_kdf\_keygen
===========================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_kdf\_keygen</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_kx\_client\_session\_keys
=========================================

Description

### 说明

<span class="type">array</span> <span
class="methodname">sodium\_crypto\_kx\_client\_session\_keys</span> (
<span class="methodparam"><span class="type">string</span>
`$client_keypair`</span> , <span class="methodparam"><span
class="type">string</span> `$server_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`client_keypair`  

`server_key`  

### 返回值

sodium\_crypto\_kx\_keypair
===========================

Creates a new sodium keypair

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_kx\_keypair</span> ( <span
class="methodparam">void</span> )

Create a new sodium keypair consisting of the secret key (32 bytes)
followed by the public key (32 bytes). The keys can be retrieved by
calling <span class="function">sodium\_crypto\_kx\_secretkey</span> and
<span class="function">sodium\_crypto\_kx\_publickey</span>,
respectively.

### 参数

此函数没有参数。

### 返回值

Returns the new keypair on success; throws an exception otherwise.

### 范例

**示例 \#1 <span class="function">sodium\_crypto\_kx\_keypair</span>
usage**

Create a new keypair and retrieve the secret and the public key from it.

``` php
<?php
$keypair = sodium_crypto_kx_keypair();
$secret = sodium_crypto_kx_secretkey($keypair);
$public = sodium_crypto_kx_publickey($keypair);
printf("secret: %s\npublic: %s", bin2hex($secret), bin2hex($public));
?>
```

以上例程的输出类似于：

    secret: e7c5c918fdc40762e6000542c0118f4368ce8fd242b0e48c1e17202797a25daf
    public: d1f59fda8652caf40ed1a01d2b6f3802b60846986372cd8fa337b7c12c428b18

sodium\_crypto\_kx\_publickey
=============================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_kx\_publickey</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_kx\_secretkey
=============================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_kx\_secretkey</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_kx\_seed\_keypair
=================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_kx\_seed\_keypair</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`string`  

### 返回值

sodium\_crypto\_kx\_server\_session\_keys
=========================================

Description

### 说明

<span class="type">array</span> <span
class="methodname">sodium\_crypto\_kx\_server\_session\_keys</span> (
<span class="methodparam"><span class="type">string</span>
`$server_keypair`</span> , <span class="methodparam"><span
class="type">string</span> `$client_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`server_keypair`  

`client_key`  

### 返回值

sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify
=========================================================

Verify that the password is a valid password verification string

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify</span>
( <span class="methodparam"><span class="type">string</span>
`$hash`</span> , <span class="methodparam"><span
class="type">string</span> `$password`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`hash`  

`password`  

### 返回值

sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str
=================================================

Get an ASCII encoded hash

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str</span>
( <span class="methodparam"><span class="type">string</span>
`$password`</span> , <span class="methodparam"><span
class="type">int</span> `$opslimit`</span> , <span
class="methodparam"><span class="type">int</span> `$memlimit`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`password`  

`opslimit`  

`memlimit`  

### 返回值

sodium\_crypto\_pwhash\_scryptsalsa208sha256
============================================

Derives a key from a password

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_pwhash\_scryptsalsa208sha256</span> (
<span class="methodparam"><span class="type">int</span> `$length`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> , <span class="methodparam"><span
class="type">string</span> `$salt`</span> , <span
class="methodparam"><span class="type">int</span> `$opslimit`</span> ,
<span class="methodparam"><span class="type">int</span>
`$memlimit`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`length`  

`password`  

`salt`  

`opslimit`  

`memlimit`  

### 返回值

sodium\_crypto\_pwhash\_str\_needs\_rehash
==========================================

Description

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_pwhash\_str\_needs\_rehash</span> (
<span class="methodparam"><span class="type">string</span>
`$password`</span> , <span class="methodparam"><span
class="type">int</span> `$opslimit`</span> , <span
class="methodparam"><span class="type">int</span> `$memlimit`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`password`  

`opslimit`  

`memlimit`  

### 返回值

sodium\_crypto\_pwhash\_str\_verify
===================================

Verifies that a password matches a hash

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_pwhash\_str\_verify</span> ( <span
class="methodparam"><span class="type">string</span> `$hash`</span> ,
<span class="methodparam"><span class="type">string</span>
`$password`</span> )

Checks that a password hash created using <span
class="function">sodium\_crypto\_pwhash\_str</span> matches a given
plain-text password. Note that the parameters are in the opposite order
to the same parameters in the similar <span
class="function">password\_hash</span> function.

### 参数

`hash`  
一个由 <span class="function">password\_hash</span> 创建的散列值。

`password`  
用户的密码。

### 返回值

Returns **`TRUE`** if the password and hash match, or **`FALSE`**
otherwise.

### 注释

> **Note**:
>
> Hashes are calculated using the Argon2ID algorithm, providing
> resistance to both GPU and side-channel attacks.

### 参见

-   <span class="function">sodium\_crypto\_pwhash\_str</span>
-   <span class="function">password\_hash</span>
-   <span class="function">password\_verify</span>

sodium\_crypto\_pwhash\_str
===========================

Get an ASCII-encoded hash

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_pwhash\_str</span> ( <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">int</span>
`$opslimit`</span> , <span class="methodparam"><span
class="type">int</span> `$memlimit`</span> )

Uses a CPU- and memory-hard hash algorithm along with a
randomly-generated salt, and memory and CPU limits to generate an
ASCII-encoded hash suitable for password storage.

### 参数

`password`  
<span class="type">string</span>; The password to generate a hash for.

`opslimit`  
Represents a maximum amount of computations to perform. Raising this
number will make the function require more CPU cycles to compute a key.
There are constants available to set the operations limit to appropriate
values depending on intended use, in order of strength:
**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE`**,
**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_MODERATE`** and
**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_SENSITIVE`**.

`memlimit`  
The maximum amount of RAM that the function will use, in bytes. There
are constants to help you choose an appropriate value, in order of size:
**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE`**,
**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_MODERATE`**, and
**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_SENSITIVE`**. Typically these should be
paired with the matching opslimit values.

### 返回值

Returns the hashed password, 或者在失败时返回 **`FALSE`**.

In order to produce the same password hash from the same password, the
same values for `opslimit` and `memlimit` must be used. These are
embedded within the generated hash, so everything that's needed to
verify the hash is included. This allows the <span
class="function">sodium\_crypto\_pwhash\_str\_verify</span> function to
verify the hash without needing separate storage for the other
parameters.

### 注释

> **Note**:
>
> Hashes are calculated using the Argon2ID algorithm, providing
> resistance to both GPU and side-channel attacks. In contrast to the
> <span class="function">password\_hash</span> function, there is no
> salt parameter (a salt is generated automatically), and the `opslimit`
> and `memlimit` parameters are not optional.

### 范例

**示例 \#1 <span class="function">password\_hash</span> example**

``` php
<?php
$password = 'password';
echo sodium_crypto_pwhash_str(
    $password,
    SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE,
    SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE
);
```

以上例程的输出类似于：

    $argon2id$v=19$m=65536,t=2,p=1$oWIfdaXwWwhVmovOBc2NAQ$EbsZ+JnZyyavkafS0hoc4HdaOB0ILWZESAZ7kVGa+Iw

### 参见

-   <span class="function">sodium\_crypto\_pwhash\_str\_verify</span>
-   <span class="function">sodium\_crypto\_pwhash</span>
-   <span class="function">password\_hash</span>
-   <span class="function">password\_verify</span>
-   <a href="https://download.libsodium.org/doc/password_hashing/the_argon2i_function.html" class="link external">» Libsodium Argon2 docs</a>

sodium\_crypto\_pwhash
======================

Derive a key from a password

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_pwhash</span> ( <span
class="methodparam"><span class="type">int</span> `$length`</span> ,
<span class="methodparam"><span class="type">string</span>
`$password`</span> , <span class="methodparam"><span
class="type">string</span> `$salt`</span> , <span
class="methodparam"><span class="type">int</span> `$opslimit`</span> ,
<span class="methodparam"><span class="type">int</span>
`$memlimit`</span> \[, <span class="methodparam"><span
class="type">int</span> `$alg`</span> \] )

This function provides low-level access to libsodium's crypto\_pwhash
key derivation function. Unless you have specific reason to use this
function, you should use <span
class="function">sodium\_crypto\_pwhash\_str</span> or <span
class="function">password\_hash</span> functions instead.

### 参数

`length`  
<span class="type">integer</span>; The length of the password hash to
generate, in bytes.

`password`  
<span class="type">string</span>; The password to generate a hash for.

`salt`  
<span class="type">string</span> A salt to add to the password before
hashing. The salt should be unpredictable, ideally generated from a good
random mumber source such as <span
class="function">random\_bytes</span>, and have a length of at least
**`SODIUM_CRYPTO_PWHASH_SALTBYTES`** bytes.

`opslimit`  
Represents a maximum amount of computations to perform. Raising this
number will make the function require more CPU cycles to compute a key.
There are some constants available to set the operations limit to
appropriate values depending on intended use, in order of strength:
**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE`**,
**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_MODERATE`** and
**`SODIUM_CRYPTO_PWHASH_OPSLIMIT_SENSITIVE`**.

`memlimit`  
The maximum amount of RAM that the function will use, in bytes. There
are constants to help you choose an appropriate value, in order of size:
**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE`**,
**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_MODERATE`**, and
**`SODIUM_CRYPTO_PWHASH_MEMLIMIT_SENSITIVE`**. Typically these should be
paired with the matching `opslimit` values.

`alg`  
<span class="type">integer</span> A number indicating the hash algorithm
to use. By default **`SODIUM_CRYPTO_PWHASH_ALG_DEFAULT`** (the currently
recommended algorithm, which can change from one version of libsodium to
another), or explicitly using **`SODIUM_CRYPTO_PWHASH_ALG_ARGON2ID13`**,
representing the Argon2id algorithm version 1.3.

### 返回值

Returns the derived key, 或者在失败时返回 **`FALSE`**. The return value
is a binary string of the hash, not an ASCII-encoded representation, and
does not contain additional information about the parameters used to
create the hash, so you will need to keep that information if you are
ever going to verify the password in future. Use <span
class="function">sodium\_crypto\_pwhash\_str</span> to avoid needing to
do all that.

### 范例

**示例 \#1 <span class="function">password\_hash</span> example**

``` php
<?php
//Need to keep the salt if we're ever going to be able to check this password
$salt = random_bytes(SODIUM_CRYPTO_PWHASH_SALTBYTES);
//Using bin2hex to keep output readable
echo bin2hex(
    sodium_crypto_pwhash(
        16, // == 128 bits
        'password',
        $salt,
        SODIUM_CRYPTO_PWHASH_OPSLIMIT_INTERACTIVE,
        SODIUM_CRYPTO_PWHASH_MEMLIMIT_INTERACTIVE,
        SODIUM_CRYPTO_PWHASH_ALG_ARGON2ID13
    )
);
?>
```

以上例程的输出类似于：

    a18f346ba57992eb7e4ae6abf3fd30ee

sodium\_crypto\_scalarmult\_base
================================

别名 <span
class="function">sodium\_crypto\_box\_publickey\_from\_secretkey</span>

### 说明

此函数是该函数的别名： <span
class="function">sodium\_crypto\_box\_publickey\_from\_secretkey</span>.

sodium\_crypto\_scalarmult
==========================

Compute a shared secret given a user's secret key and another user's
public key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_scalarmult</span> ( <span
class="methodparam"><span class="type">string</span> `$n`</span> , <span
class="methodparam"><span class="type">string</span> `$p`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`n`  

`p`  

### 返回值

sodium\_crypto\_secretbox\_keygen
=================================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_secretbox\_keygen</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_secretbox\_open
===============================

Verify and decrypt a ciphertext

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_secretbox\_open</span> ( <span
class="methodparam"><span class="type">string</span>
`$ciphertext`</span> , <span class="methodparam"><span
class="type">string</span> `$nonce`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ciphertext`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_secretbox
=========================

Encrypt a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_secretbox</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> ,
<span class="methodparam"><span class="type">string</span>
`$nonce`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`string`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_pull
===========================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_pull</span>
( <span class="methodparam"><span class="type">string</span>
`$header`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`header`  

`key`  

### 返回值

sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_push
===========================================================

Description

### 说明

<span class="type">array</span> <span
class="methodname">sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_push</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_secretstream\_xchacha20poly1305\_keygen
=======================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_secretstream\_xchacha20poly1305\_keygen</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_secretstream\_xchacha20poly1305\_pull
=====================================================

Description

### 说明

<span class="type">array</span> <span
class="methodname">sodium\_crypto\_secretstream\_xchacha20poly1305\_pull</span>
( <span class="methodparam"><span class="type">string</span>
`&$state`</span> , <span class="methodparam"><span
class="type">string</span> `$c`</span> \[, <span
class="methodparam"><span class="type">string</span> `$ad`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`state`  

`c`  

`ad`  

### 返回值

sodium\_crypto\_secretstream\_xchacha20poly1305\_push
=====================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_secretstream\_xchacha20poly1305\_push</span>
( <span class="methodparam"><span class="type">string</span>
`&$state`</span> , <span class="methodparam"><span
class="type">string</span> `$msg`</span> \[, <span
class="methodparam"><span class="type">string</span> `$ad`</span> \[,
<span class="methodparam"><span class="type">int</span> `$tag`</span>
\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`state`  

`msg`  

`ad`  

`tag`  

### 返回值

sodium\_crypto\_secretstream\_xchacha20poly1305\_rekey
======================================================

Description

### 说明

<span class="type">void</span> <span
class="methodname">sodium\_crypto\_secretstream\_xchacha20poly1305\_rekey</span>
( <span class="methodparam"><span class="type">string</span>
`&$state`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`state`  

### 返回值

sodium\_crypto\_shorthash\_keygen
=================================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_shorthash\_keygen</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_shorthash
=========================

Compute a fixed-size fingerprint for the message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_shorthash</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`key`  

### 返回值

sodium\_crypto\_sign\_detached
==============================

Sign the message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_detached</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span>
`$secretkey`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`secretkey`  

### 返回值

sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519
=================================================

Convert an Ed25519 public key to a Curve25519 public key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519
=================================================

Convert an Ed25519 secret key to a Curve25519 secret key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey
==============================================================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey</span>
( <span class="methodparam"><span class="type">string</span>
`$secret_key`</span> , <span class="methodparam"><span
class="type">string</span> `$public_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`secret_key`  

`public_key`  

### 返回值

sodium\_crypto\_sign\_keypair
=============================

Randomly generate a secret key and a corresponding public key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_keypair</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_sign\_open
==========================

Check that the signed message has a valid signature

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_open</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> ,
<span class="methodparam"><span class="type">string</span>
`$public_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`string`  

`public_key`  

### 返回值

sodium\_crypto\_sign\_publickey\_from\_secretkey
================================================

Extract the public key from the secret key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_publickey\_from\_secretkey</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_sign\_publickey
===============================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_publickey</span> ( <span
class="methodparam"><span class="type">string</span> `$keypair`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`keypair`  

### 返回值

sodium\_crypto\_sign\_secretkey
===============================

Description

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_secretkey</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_sign\_seed\_keypair
===================================

Deterministically derive the key pair from a single key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign\_seed\_keypair</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`key`  

### 返回值

sodium\_crypto\_sign\_verify\_detached
======================================

Verify signature for the message

### 说明

<span class="type">bool</span> <span
class="methodname">sodium\_crypto\_sign\_verify\_detached</span> ( <span
class="methodparam"><span class="type">string</span> `$signature`</span>
, <span class="methodparam"><span class="type">string</span>
`$msg`</span> , <span class="methodparam"><span
class="type">string</span> `$public_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`signature`  

`msg`  

`public_key`  

### 返回值

sodium\_crypto\_sign
====================

Sign a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_sign</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span>
`$secret_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`secret_key`  

### 返回值

sodium\_crypto\_stream\_keygen
==============================

Get random bytes for key

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_stream\_keygen</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

sodium\_crypto\_stream\_xor
===========================

Encrypt a message

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_stream\_xor</span> ( <span
class="methodparam"><span class="type">string</span> `$msg`</span> ,
<span class="methodparam"><span class="type">string</span>
`$nonce`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`msg`  

`nonce`  

`key`  

### 返回值

sodium\_crypto\_stream
======================

Generate a deterministic sequence of bytes from a seed

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_crypto\_stream</span> ( <span
class="methodparam"><span class="type">int</span> `$length`</span> ,
<span class="methodparam"><span class="type">string</span>
`$nonce`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`length`  

`nonce`  

`key`  

### 返回值

sodium\_hex2bin
===============

Decodes a hexadecimally encoded binary string

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_hex2bin</span> ( <span
class="methodparam"><span class="type">string</span> `$hex`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$ignore`</span> \] )

Decodes a hexadecimally encoded binary string.

Like <span class="function">sodium\_bin2hex</span>, <span
class="function">sodium\_hex2bin</span> is resistant to side-channel
attacks while <span class="function">hex2bin</span> is not.

### 参数

`hex`  
Hexadecimal representation of data.

`ignore`  
Optional string argument for characters to ignore.

### 返回值

Returns the binary representation of the given `hex` data.

sodium\_increment
=================

Increment large number

### 说明

<span class="type">void</span> <span
class="methodname">sodium\_increment</span> ( <span
class="methodparam"><span class="type">string</span> `&$val`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`val`  

### 返回值

sodium\_memcmp
==============

Test for equality in constant-time

### 说明

<span class="type">int</span> <span
class="methodname">sodium\_memcmp</span> ( <span
class="methodparam"><span class="type">string</span> `$buf1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$buf2`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`buf1`  

`buf2`  

### 返回值

sodium\_memzero
===============

Overwrite buf with zeros

### 说明

<span class="type">void</span> <span
class="methodname">sodium\_memzero</span> ( <span
class="methodparam"><span class="type">string</span> `&$buf`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`buf`  

### 返回值

sodium\_pad
===========

Add padding data

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_pad</span> ( <span class="methodparam"><span
class="type">string</span> `$unpadded`</span> , <span
class="methodparam"><span class="type">int</span> `$length`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`unpadded`  

`length`  

### 返回值

sodium\_unpad
=============

Remove padding data

### 说明

<span class="type">string</span> <span
class="methodname">sodium\_unpad</span> ( <span
class="methodparam"><span class="type">string</span> `$padded`</span> ,
<span class="methodparam"><span class="type">int</span> `$length`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`padded`  

`length`  

### 返回值

**目录**

-   [sodium\_add](/ref/sodium.html#sodium_add) — Add large numbers
-   [sodium\_base642bin](/ref/sodium.html#sodium_base642bin) —
    Description
-   [sodium\_bin2base64](/ref/sodium.html#sodium_bin2base64) —
    Description
-   [sodium\_bin2hex](/ref/sodium.html#sodium_bin2hex) — Encode to
    hexadecimal
-   [sodium\_compare](/ref/sodium.html#sodium_compare) — Compare large
    numbers
-   [sodium\_crypto\_aead\_aes256gcm\_decrypt](/ref/sodium.html#sodium_crypto_aead_aes256gcm_decrypt)
    — Decrypt in combined mode with precalculation
-   [sodium\_crypto\_aead\_aes256gcm\_encrypt](/ref/sodium.html#sodium_crypto_aead_aes256gcm_encrypt)
    — Encrypt in combined mode with precalculation
-   [sodium\_crypto\_aead\_aes256gcm\_is\_available](/ref/sodium.html#sodium_crypto_aead_aes256gcm_is_available)
    — Check if hardware supports AES256-GCM
-   [sodium\_crypto\_aead\_aes256gcm\_keygen](/ref/sodium.html#sodium_crypto_aead_aes256gcm_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_aead\_chacha20poly1305\_decrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_decrypt)
    — Verify that the ciphertext includes a valid tag
-   [sodium\_crypto\_aead\_chacha20poly1305\_encrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_encrypt)
    — Encrypt a message
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_ietf_decrypt)
    — Verify that the ciphertext includes a valid tag
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_ietf_encrypt)
    — Encrypt a message
-   [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_ietf_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_aead\_chacha20poly1305\_keygen](/ref/sodium.html#sodium_crypto_aead_chacha20poly1305_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt](/ref/sodium.html#sodium_crypto_aead_xchacha20poly1305_ietf_decrypt)
    — Description
-   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt](/ref/sodium.html#sodium_crypto_aead_xchacha20poly1305_ietf_encrypt)
    — Description
-   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen](/ref/sodium.html#sodium_crypto_aead_xchacha20poly1305_ietf_keygen)
    — Description
-   [sodium\_crypto\_auth\_keygen](/ref/sodium.html#sodium_crypto_auth_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_auth\_verify](/ref/sodium.html#sodium_crypto_auth_verify)
    — Verifies that the tag is valid for the message
-   [sodium\_crypto\_auth](/ref/sodium.html#sodium_crypto_auth) —
    Compute a tag for the message
-   [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey](/ref/sodium.html#sodium_crypto_box_keypair_from_secretkey_and_publickey)
    — Description
-   [sodium\_crypto\_box\_keypair](/ref/sodium.html#sodium_crypto_box_keypair)
    — Randomly generate a secret key and a corresponding public key
-   [sodium\_crypto\_box\_open](/ref/sodium.html#sodium_crypto_box_open)
    — Verify and decrypt a ciphertext
-   [sodium\_crypto\_box\_publickey\_from\_secretkey](/ref/sodium.html#sodium_crypto_box_publickey_from_secretkey)
    — Description
-   [sodium\_crypto\_box\_publickey](/ref/sodium.html#sodium_crypto_box_publickey)
    — Description
-   [sodium\_crypto\_box\_seal\_open](/ref/sodium.html#sodium_crypto_box_seal_open)
    — Decrypt the ciphertext
-   [sodium\_crypto\_box\_seal](/ref/sodium.html#sodium_crypto_box_seal)
    — Encrypt a message
-   [sodium\_crypto\_box\_secretkey](/ref/sodium.html#sodium_crypto_box_secretkey)
    — Description
-   [sodium\_crypto\_box\_seed\_keypair](/ref/sodium.html#sodium_crypto_box_seed_keypair)
    — Deterministically derive the key pair from a single key
-   [sodium\_crypto\_box](/ref/sodium.html#sodium_crypto_box) — Encrypt
    a message
-   [sodium\_crypto\_generichash\_final](/ref/sodium.html#sodium_crypto_generichash_final)
    — Complete the hash
-   [sodium\_crypto\_generichash\_init](/ref/sodium.html#sodium_crypto_generichash_init)
    — Initialize a hash
-   [sodium\_crypto\_generichash\_keygen](/ref/sodium.html#sodium_crypto_generichash_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_generichash\_update](/ref/sodium.html#sodium_crypto_generichash_update)
    — Add message to a hash
-   [sodium\_crypto\_generichash](/ref/sodium.html#sodium_crypto_generichash)
    — Get a hash of the message
-   [sodium\_crypto\_kdf\_derive\_from\_key](/ref/sodium.html#sodium_crypto_kdf_derive_from_key)
    — Derive a subkey
-   [sodium\_crypto\_kdf\_keygen](/ref/sodium.html#sodium_crypto_kdf_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_kx\_client\_session\_keys](/ref/sodium.html#sodium_crypto_kx_client_session_keys)
    — Description
-   [sodium\_crypto\_kx\_keypair](/ref/sodium.html#sodium_crypto_kx_keypair)
    — Creates a new sodium keypair
-   [sodium\_crypto\_kx\_publickey](/ref/sodium.html#sodium_crypto_kx_publickey)
    — Description
-   [sodium\_crypto\_kx\_secretkey](/ref/sodium.html#sodium_crypto_kx_secretkey)
    — Description
-   [sodium\_crypto\_kx\_seed\_keypair](/ref/sodium.html#sodium_crypto_kx_seed_keypair)
    — Description
-   [sodium\_crypto\_kx\_server\_session\_keys](/ref/sodium.html#sodium_crypto_kx_server_session_keys)
    — Description
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str\_verify](/ref/sodium.html#sodium_crypto_pwhash_scryptsalsa208sha256_str_verify)
    — Verify that the password is a valid password verification string
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256\_str](/ref/sodium.html#sodium_crypto_pwhash_scryptsalsa208sha256_str)
    — Get an ASCII encoded hash
-   [sodium\_crypto\_pwhash\_scryptsalsa208sha256](/ref/sodium.html#sodium_crypto_pwhash_scryptsalsa208sha256)
    — Derives a key from a password
-   [sodium\_crypto\_pwhash\_str\_needs\_rehash](/ref/sodium.html#sodium_crypto_pwhash_str_needs_rehash)
    — Description
-   [sodium\_crypto\_pwhash\_str\_verify](/ref/sodium.html#sodium_crypto_pwhash_str_verify)
    — Verifies that a password matches a hash
-   [sodium\_crypto\_pwhash\_str](/ref/sodium.html#sodium_crypto_pwhash_str)
    — Get an ASCII-encoded hash
-   [sodium\_crypto\_pwhash](/ref/sodium.html#sodium_crypto_pwhash) —
    Derive a key from a password
-   [sodium\_crypto\_scalarmult\_base](/ref/sodium.html#sodium_crypto_scalarmult_base)
    — 别名 sodium\_crypto\_box\_publickey\_from\_secretkey
-   [sodium\_crypto\_scalarmult](/ref/sodium.html#sodium_crypto_scalarmult)
    — Compute a shared secret given a user's secret key and another
    user's public key
-   [sodium\_crypto\_secretbox\_keygen](/ref/sodium.html#sodium_crypto_secretbox_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_secretbox\_open](/ref/sodium.html#sodium_crypto_secretbox_open)
    — Verify and decrypt a ciphertext
-   [sodium\_crypto\_secretbox](/ref/sodium.html#sodium_crypto_secretbox)
    — Encrypt a message
-   [sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_pull](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_init_pull)
    — Description
-   [sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_push](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_init_push)
    — Description
-   [sodium\_crypto\_secretstream\_xchacha20poly1305\_keygen](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_keygen)
    — Description
-   [sodium\_crypto\_secretstream\_xchacha20poly1305\_pull](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_pull)
    — Description
-   [sodium\_crypto\_secretstream\_xchacha20poly1305\_push](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_push)
    — Description
-   [sodium\_crypto\_secretstream\_xchacha20poly1305\_rekey](/ref/sodium.html#sodium_crypto_secretstream_xchacha20poly1305_rekey)
    — Description
-   [sodium\_crypto\_shorthash\_keygen](/ref/sodium.html#sodium_crypto_shorthash_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_shorthash](/ref/sodium.html#sodium_crypto_shorthash)
    — Compute a fixed-size fingerprint for the message
-   [sodium\_crypto\_sign\_detached](/ref/sodium.html#sodium_crypto_sign_detached)
    — Sign the message
-   [sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519](/ref/sodium.html#sodium_crypto_sign_ed25519_pk_to_curve25519)
    — Convert an Ed25519 public key to a Curve25519 public key
-   [sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519](/ref/sodium.html#sodium_crypto_sign_ed25519_sk_to_curve25519)
    — Convert an Ed25519 secret key to a Curve25519 secret key
-   [sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey](/ref/sodium.html#sodium_crypto_sign_keypair_from_secretkey_and_publickey)
    — Description
-   [sodium\_crypto\_sign\_keypair](/ref/sodium.html#sodium_crypto_sign_keypair)
    — Randomly generate a secret key and a corresponding public key
-   [sodium\_crypto\_sign\_open](/ref/sodium.html#sodium_crypto_sign_open)
    — Check that the signed message has a valid signature
-   [sodium\_crypto\_sign\_publickey\_from\_secretkey](/ref/sodium.html#sodium_crypto_sign_publickey_from_secretkey)
    — Extract the public key from the secret key
-   [sodium\_crypto\_sign\_publickey](/ref/sodium.html#sodium_crypto_sign_publickey)
    — Description
-   [sodium\_crypto\_sign\_secretkey](/ref/sodium.html#sodium_crypto_sign_secretkey)
    — Description
-   [sodium\_crypto\_sign\_seed\_keypair](/ref/sodium.html#sodium_crypto_sign_seed_keypair)
    — Deterministically derive the key pair from a single key
-   [sodium\_crypto\_sign\_verify\_detached](/ref/sodium.html#sodium_crypto_sign_verify_detached)
    — Verify signature for the message
-   [sodium\_crypto\_sign](/ref/sodium.html#sodium_crypto_sign) — Sign a
    message
-   [sodium\_crypto\_stream\_keygen](/ref/sodium.html#sodium_crypto_stream_keygen)
    — Get random bytes for key
-   [sodium\_crypto\_stream\_xor](/ref/sodium.html#sodium_crypto_stream_xor)
    — Encrypt a message
-   [sodium\_crypto\_stream](/ref/sodium.html#sodium_crypto_stream) —
    Generate a deterministic sequence of bytes from a seed
-   [sodium\_hex2bin](/ref/sodium.html#sodium_hex2bin) — Decodes a
    hexadecimally encoded binary string
-   [sodium\_increment](/ref/sodium.html#sodium_increment) — Increment
    large number
-   [sodium\_memcmp](/ref/sodium.html#sodium_memcmp) — Test for equality
    in constant-time
-   [sodium\_memzero](/ref/sodium.html#sodium_memzero) — Overwrite buf
    with zeros
-   [sodium\_pad](/ref/sodium.html#sodium_pad) — Add padding data
-   [sodium\_unpad](/ref/sodium.html#sodium_unpad) — Remove padding data
