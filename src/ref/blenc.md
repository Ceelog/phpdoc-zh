blenc\_encrypt
==============

Encrypt a PHP script with BLENC

### 说明

<span class="type">string</span> <span
class="methodname">blenc\_encrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$plaintext`</span>
, <span class="methodparam"><span class="type">string</span>
`$encodedfile`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encryption_key`</span> \] )

Encrypt the `plaintext` content and write it into `encodedfile`

### 参数

`plaintext`  
A source code to encrypt. Does not need to contain opening/closing PHP
tags

`encodedfile`  
The filename where BLENC will save the encoded source.

`encryption_key`  
The key that BLENC will use to encrypt plaintext content. If not given
BLENC will create a valid key.

### 返回值

BLENC will return the redistributable key that must be saved into
key\_file: the path of key\_file is specified at runtime with the option
blenc.key\_file

### 范例

**示例 \#1 <span class="function">blenc\_encrypt</span> example**

``` php
<?php

/* read the PHP source code */
$source_code = file_get_contents("my_source_to_protect.php");

/* create the encrypted version */
$redistributable_key = blenc_encrypt($source_code, "my_source_encoded.php");

/* read which is the key_file */
$key_file = ini_get('blenc.key_file');

/* save the redistributable key */
file_put_contents($key_file, $redistributable_key, FILE_APPEND);
?>
```

**目录**

-   [blenc\_encrypt](/ref/blenc.html#blenc_encrypt) — Encrypt a PHP
    script with BLENC
