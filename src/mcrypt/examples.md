范例
====

Mcrypt 支持使用上述的算法来进行加密和解密。 如果你使用 *libmcrypt-2.2.x*
链接编译 PHP， 通过使用最重要的四个函数（<span
class="function">mcrypt\_cfb</span>， <span
class="function">mcrypt\_cbc</span>, <span
class="function">mcrypt\_ecb</span>， 和 <span
class="function">mcrypt\_ofb</span>） 以及 **`MCRYPT_ENCRYPT`** and
**`MCRYPT_DECRYPT`** 来对数据进行加解密。

如果你使用 libmcrypt 2.4.x 或者 2.5.x 版本，以上函数依然可用。
但是建议使用新版本提供的更先进的函数。

**示例 \#1 在 2.4.x 或更高版本，使用 256 比特的密钥，*AES* 算法和 *CBC*
模式来加密输入数据**

``` php
<?php
    $key = hash('sha256', 'this is a secret key', true);
    $input = "Let us meet at 9 o'clock at the secret place.";
    
    $td = mcrypt_module_open('rijndael-128', '', 'cbc', '');
    $iv = mcrypt_create_iv(mcrypt_enc_get_iv_size($td), MCRYPT_DEV_URANDOM);
    mcrypt_generic_init($td, $key, $iv);
    $encrypted_data = mcrypt_generic($td, $input);
    mcrypt_generic_deinit($td);
    mcrypt_module_close($td);
?>
```

本例程将加密后的数据以字符串格式存储于 *$encrypted\_data* 变量。
完整例程请参见 <span class="function">mcrypt\_module\_open</span>。
