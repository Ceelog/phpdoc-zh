mcrypt\_cbc
===========

以 CBC 模式加解密数据

**Warning**

This function was *DEPRECATED* in PHP 5.5.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">mcrypt\_decrypt</span>
-   <span class="function">mcrypt\_encrypt</span>

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_cbc</span> ( <span class="methodparam"><span
class="type">int</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$iv`</span> \] )

<span class="type">string</span> <span
class="methodname">mcrypt\_cbc</span> ( <span class="methodparam"><span
class="type">string</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$iv`</span> \] )

第一个原型是针对 libmcrypt 2.2.x 的， 第二个原型是针对 libmcrypt 2.4.x
及更高版本的。 `mode` 可选值为： **`MCRYPT_ENCRYPT`** 或
**`MCRYPT_DECRYPT`**。

mcrypt\_cfb
===========

以 CFB 模式加解密数据

**Warning**

This function was *DEPRECATED* in PHP 5.5.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">mcrypt\_decrypt</span>
-   <span class="function">mcrypt\_encrypt</span>

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_cfb</span> ( <span class="methodparam"><span
class="type">int</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> , <span class="methodparam"><span
class="type">string</span> `$iv`</span> )

<span class="type">string</span> <span
class="methodname">mcrypt\_cfb</span> ( <span class="methodparam"><span
class="type">string</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$iv`</span> \] )

第一个原型是针对 libmcrypt 2.2.x 的， 第二个原型是针对 libmcrypt 2.4.x
及更高版本的。 `mode` 可选值为： **`MCRYPT_ENCRYPT`** 或
**`MCRYPT_DECRYPT`**。

mcrypt\_create\_iv
==================

从随机源创建初始向量

**Warning**

This function was *DEPRECATED* in PHP 7.1.0, and *REMOVED* in PHP 7.2.0.

Alternatives to this function include:

-   <span class="function">random\_bytes</span>

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_create\_iv</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">int</span> `$source`<span
class="initializer"> = MCRYPT\_DEV\_URANDOM</span></span> \] )

从随机源创建初始向量。

初始向量只是为了给加密算法提供一个可用的种子， 所以它不需要安全保护，
你甚至可以随同密文一起发布初始向量也不会对安全性带来影响。

### 参数

`size`  
初始向量大小。

`source`  
初始向量数据来源。可选值有： **`MCRYPT_RAND`** （系统随机数生成器）,
**`MCRYPT_DEV_RANDOM`** （从 `/dev/random` 文件读取数据） 和
**`MCRYPT_DEV_URANDOM`** （从 `/dev/urandom` 文件读取数据）。 在 Windows
平台，PHP 5.3.0 之前的版本中，仅支持 **`MCRYPT_RAND`**。

请注意，在 PHP 5.6.0 之前的版本中， 此参数的默认值为
**`MCRYPT_DEV_RANDOM`**。

> **Note**: <span class="simpara">
> 需要注意的是，如果没有更多可用的用来产生随机数据的信息，那么
> **`MCRYPT_DEV_RANDOM`** 可能进入阻塞状态。 </span>

### 返回值

返回初始向量。如果发生错误，则返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                               |
|-------|------------------------------------------------------------------------------------|
| 5.6.0 | `source` 参数的默认值是 **`MCRYPT_DEV_URANDOM`**。                                 |
| 5.3.0 | **`MCRYPT_DEV_RANDOM`** 和 **`MCRYPT_DEV_URANDOM`** 在 Windows 平台也可用了。      |
| 5.3.0 | 不再需要提前调用 <span class="function">srand</span> 函数， 由本函数自动完成调用。 |

### 范例

**示例 \#1 <span class="function">mcrypt\_create\_iv</span> 例程**

``` php
<?php
    $size = mcrypt_get_iv_size(MCRYPT_CAST_256, MCRYPT_MODE_CFB);
    $iv = mcrypt_create_iv($size, MCRYPT_DEV_RANDOM);
?>
```

### 参见

-   <a href="http://www.ciphersbyritter.com/GLOSSARY.HTM#IV" class="link external">» http://www.ciphersbyritter.com/GLOSSARY.HTM#IV</a>
-   <a href="http://www.quadibloc.com/crypto/co0409.htm" class="link external">» http://www.quadibloc.com/crypto/co0409.htm</a>
-   Applied Cryptography by Schneier (ISBN 0-471-11709-9) 9.3 节。
-   <span class="function">random\_bytes</span>

mcrypt\_decrypt
===============

使用给定参数解密密文

**Warning**

本函数已自 PHP 7.1.0 起*废弃*并将自 PHP 7.2.0
起*移除*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_decrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$cipher`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span
class="type">string</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">string</span> `$iv`</span> \] )

解密 `data` 并返回明文。

### 参数

`cipher`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`key`  
数据加密密钥。 如果密钥长度不是加解密算法能够支持的有效长度，
那么会产生警告并且返回 **`FALSE`**

`data`  
要使用给定的 `cipher` 和 `mode` 解密的数据。 如果数据大小不是 n \*
分组大小，则在其后追加 '*\\0*' 来补齐。

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

`iv`  
Used for the initialization in CBC, CFB, OFB modes, and in some
algorithms in STREAM mode. If the provided IV size is not supported by
the chaining mode or no IV was provided, but the chaining mode requires
one, the function will emit a warning and return **`FALSE`**.

### 返回值

以字符串格式返回解密后的数据， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | 不再接受无效长度的 `key` and `iv` 参数。 如果参数长度无效，则 <span class="function">mcrypt\_decrypt</span> 函数会产生警告并且返回 **`FALSE`**。 之前版本中，对于长度不足的密钥和初始向量会在其后补齐 '*\\0*' 使其达到有效长度。 |

### 参见

-   <span class="function">mcrypt\_encrypt</span>

mcrypt\_ecb
===========

已废弃：使用 ECB 模式加解密数据

**Warning**

This function was *DEPRECATED* in PHP 5.5.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">mcrypt\_decrypt</span>
-   <span class="function">mcrypt\_encrypt</span>

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_ecb</span> ( <span class="methodparam"><span
class="type">int</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> )

<span class="type">string</span> <span
class="methodname">mcrypt\_ecb</span> ( <span class="methodparam"><span
class="type">string</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$iv`</span> \] )

第一个原型是针对 libmcrypt 2.2.x 的， 第二个原型是针对 libmcrypt 2.4.x
及更高版本的。 `mode` 可选值为： **`MCRYPT_ENCRYPT`** 或
**`MCRYPT_DECRYPT`**。

mcrypt\_enc\_get\_algorithms\_name
==================================

返回打开的算法名称

**Warning**

本函数已自 PHP 7.1.0 起*废弃*并将自 PHP 7.2.0
起*移除*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_enc\_get\_algorithms\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

本函数返回算法名称。

### 参数

`td`  
加密描述符。

### 返回值

以字符串格式返回打开的加密算法名称。

### 范例

**示例 \#1 <span
class="function">mcrypt\_enc\_get\_algorithms\_name</span> 例程**

``` php
<?php
$td = mcrypt_module_open(MCRYPT_CAST_256, '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_algorithms_name($td). "\n";

$td = mcrypt_module_open('cast-256', '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_algorithms_name($td). "\n";
?>
```

以上例程会输出：

    CAST-256
    CAST-256

mcrypt\_enc\_get\_block\_size
=============================

返回打开的算法的分组大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*并将自 PHP 7.2.0
起*移除*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_enc\_get\_block\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

获取打开的算法的分组大小。

### 参数

`td`  
加密描述符。

### 返回值

返回指定算法的分组大小，以字节为单位。

mcrypt\_enc\_get\_iv\_size
==========================

返回打开的算法的初始向量大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_enc\_get\_iv\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

本函数返回由加密描述符指定的算法所使用的初始向量大小， 以字节为单位。 在
cbc，cfb 和 ofb 模式以及某些流模式算法中会用到初始向量。

### 参数

`td`  
加密描述符。

### 返回值

返回初始向量大小。如果算法忽略初始向量，则返回 0。

mcrypt\_enc\_get\_key\_size
===========================

返回打开的模式所能支持的最长密钥

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_enc\_get\_key\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

返回打开的模式所能支持的最长密钥，以字节为单位。

### 参数

`td`  
加密描述符。

### 返回值

返回打开的模式所能支持的最长密钥，以字节为单位。

mcrypt\_enc\_get\_modes\_name
=============================

返回打开的模式的名称

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_enc\_get\_modes\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

返回模式名称。

### 参数

`td`  
加密描述符。

### 返回值

以字符串格式返回模式名称。

### 范例

**示例 \#1 <span class="function">mcrypt\_enc\_get\_modes\_name</span>
例程**

``` php
<?php
$td = mcrypt_module_open (MCRYPT_CAST_256, '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_modes_name($td). "\n";

$td = mcrypt_module_open ('cast-256', '', 'ecb', '');
echo mcrypt_enc_get_modes_name($td). "\n";
?>
```

以上例程会输出：

    CFB
    ECB

mcrypt\_enc\_get\_supported\_key\_sizes
=======================================

以数组方式返回打开的算法所支持的密钥长度

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">array</span> <span
class="methodname">mcrypt\_enc\_get\_supported\_key\_sizes</span> (
<span class="methodparam"><span class="type">resource</span>
`$td`</span> )

获取打开的算法所支持的密钥长度。

### 参数

`td`  
加密描述符。

### 返回值

返回由加密描述符指定的算法所能够支持的密钥长度。 如果该算法支持从 1 到
<span class="function">mcrypt\_enc\_get\_key\_size</span>
之间任意长度的密钥，则返回空数组。

### 范例

**示例 \#1 <span
class="function">mcrypt\_enc\_get\_supported\_key\_sizes</span> 例程**

``` php
<?php
    $td = mcrypt_module_open('rijndael-256', '', 'ecb', '');
    var_dump(mcrypt_enc_get_supported_key_sizes($td));
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      int(16)
      [1]=>
      int(24)
      [2]=>
      int(32)
    }

mcrypt\_enc\_is\_block\_algorithm\_mode
=======================================

检测打开的模式是否支持分组加密

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_enc\_is\_block\_algorithm\_mode</span> (
<span class="methodparam"><span class="type">resource</span>
`$td`</span> )

打开的模式的算法是否支持分组加密 （例如： 如果是流模式，则返回
**`FALSE`**， cbc，cfb，ofb 模式则返回 **`TRUE`**）。

### 参数

`td`  
加密描述符。

### 返回值

如果算法支持分组模式，返回 **`TRUE`**， 反之返回 **`FALSE`**。

mcrypt\_enc\_is\_block\_algorithm
=================================

检测打开模式的算法是否为分组算法

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_enc\_is\_block\_algorithm</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

打开模式的算法是否为分组算法。

### 参数

`td`  
加密描述符。

### 返回值

如果是分组算法，返回 **`TRUE`**， 如果是流模式，返回 **`FALSE`**。

mcrypt\_enc\_is\_block\_mode
============================

检测打开的模式是否以分组方式输出

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_enc\_is\_block\_mode</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

打开的模式是否以分组方式输出 （例如，对于 cbc 和 ecb 模式而言返回
**`TRUE`**，对于 cfb 和流模式而言，返回 **`FALSE`**）。

### 参数

`td`  
加密描述符。

### 返回值

如果模式以字节分组（字节块）方式输出，返回 **`TRUE`**，
如果是以字节方式输出，返回 **`FALSE`**。

mcrypt\_enc\_self\_test
=======================

在打开的模块上进行自检

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_enc\_self\_test</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

在 `td` 指定的算法 上进行自检操作。

### 参数

`td`  
加密描述符。

### 返回值

自检成功返回 *0*，失败则返回一个小于零的<span class="type">int</span>。

mcrypt\_encrypt
===============

使用给定参数加密明文

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_encrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$cipher`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span
class="type">string</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">string</span> `$iv`</span> \] )

加密数据并返回密文。

### 参数

`cipher`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`key`  
加密密钥。
如果密钥长度不是该算法所能够支持的有效长度，则函数将会发出警告并返回
**`FALSE`**

`data`  
使用给定的 `cipher` 和 `mode` 加密的数据。 如果数据长度不是
n\*分组大小，则在其后使用 '*\\0*' 补齐。

返回的密文长度可能比 `data` 更大。

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

`iv`  
Used for the initialization in CBC, CFB, OFB modes, and in some
algorithms in STREAM mode. If the provided IV size is not supported by
the chaining mode or no IV was provided, but the chaining mode requires
one, the function will emit a warning and return **`FALSE`**.

### 返回值

以字符串方式返回密文， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | 不再接受无效长度的 `key` and `iv` 参数。 如果参数长度无效，则 <span class="function">mcrypt\_decrypt</span> 函数会产生警告并且返回 **`FALSE`**。 之前版本中，对于长度不足的密钥和初始向量会在其后补齐 '*\\0*' 使其达到有效长度。 |

### 范例

**示例 \#1 <span class="function">mcrypt\_encrypt</span> 例程**

``` php
<?php
    # --- 加密 ---

    # 密钥应该是随机的二进制数据，
    # 开始使用 scrypt, bcrypt 或 PBKDF2 将一个字符串转换成一个密钥
    # 密钥是 16 进制字符串格式
    $key = pack('H*', "bcb04b7e103a0cd8b54763051cef08bc55abe029fdebae5e1d417e2ffb2a00a3");
    
    # 显示 AES-128, 192, 256 对应的密钥长度：
    #16，24，32 字节。
    $key_size =  strlen($key);
    echo "Key size: " . $key_size . "\n";
    
    $plaintext = "This string was AES-256 / CBC / ZeroBytePadding encrypted.";

    # 为 CBC 模式创建随机的初始向量
    $iv_size = mcrypt_get_iv_size(MCRYPT_RIJNDAEL_128, MCRYPT_MODE_CBC);
    $iv = mcrypt_create_iv($iv_size, MCRYPT_RAND);
    

    # 创建和 AES 兼容的密文（Rijndael 分组大小 = 128）
    # 仅适用于编码后的输入不是以 00h 结尾的
    # （因为默认是使用 0 来补齐数据）
    $ciphertext = mcrypt_encrypt(MCRYPT_RIJNDAEL_128, $key,
                                 $plaintext, MCRYPT_MODE_CBC, $iv);

    # 将初始向量附加在密文之后，以供解密时使用
    $ciphertext = $iv . $ciphertext;
    
    # 对密文进行 base64 编码
    $ciphertext_base64 = base64_encode($ciphertext);

    echo  $ciphertext_base64 . "\n";

    # === 警告 ===

    # 密文并未进行完整性和可信度保护，
    # 所以可能遭受 Padding Oracle 攻击。
    
    # --- 解密 ---
    
    $ciphertext_dec = base64_decode($ciphertext_base64);
    
    # 初始向量大小，可以通过 mcrypt_get_iv_size() 来获得
    $iv_dec = substr($ciphertext_dec, 0, $iv_size);
    
    # 获取除初始向量外的密文
    $ciphertext_dec = substr($ciphertext_dec, $iv_size);

    # 可能需要从明文末尾移除 0
    $plaintext_dec = mcrypt_decrypt(MCRYPT_RIJNDAEL_128, $key,
                                    $ciphertext_dec, MCRYPT_MODE_CBC, $iv_dec);
    
    echo  $plaintext_dec . "\n";
?>
```

以上例程会输出：

    Key size: 32
    ENJW8mS2KaJoNB5E5CoSAAu0xARgsR1bdzFWpEn+poYw45q+73az5kYi4j+0haevext1dGrcW8Qi59txfCBV8BBj3bzRP3dFCp3CPQSJ8eU=
    This string was AES-256 / CBC / ZeroBytePadding encrypted.

### 参见

-   <span class="function">mcrypt\_decrypt</span>
-   <span class="function">mcrypt\_module\_open</span>

mcrypt\_generic\_deinit
=======================

对加密模块进行清理工作

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_generic\_deinit</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

本函数终止由加密描述符（`td`）指定的加密模块，
它会清理缓冲区，但是并不关闭模块。 要想关闭加密模块， 你需要自行调用
<span class="function">mcrypt\_module\_close</span> 函数。 （但是 PHP
会在脚本末尾为你关闭已打开的加密模块）

### 参数

`td`  
加密描述符。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">mcrypt\_module\_open</span>
-   <span class="function">mcrypt\_generic\_init</span>

mcrypt\_generic\_end
====================

终止加密

**Warning**

This function was *DEPRECATED* in PHP 5.3.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">mcrypt\_generic\_deinit</span>

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_generic\_end</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

**Warning**

This alias was *DEPRECATED* in PHP 5.3.0, and *REMOVED* as of PHP 7.0.0.

**Warning**

请使用函数 <span class="function">mcrypt\_generic\_deinit</span>
来替代本函数， 因为当本函数和 <span
class="function">mcrypt\_module\_close</span> 一起使用的时候，
可能会发生由重复释放缓冲区导致的崩溃。

本函数终止由加密描述符（`td`）指定的加密模块。
实际上，它会清理所有的缓冲区，并且关闭已经打开的模块。
如果发生错误，返回 **`FALSE`**， 成功返回 **`TRUE`**。

mcrypt\_generic\_init
=====================

初始化加密所需的缓冲区

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_generic\_init</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$iv`</span> )

在每次调用 <span class="function">mcrypt\_generic</span> 或 <span
class="function">mdecrypt\_generic</span> 函数之前必须调用本函数。

### 参数

`td`  
加密描述符。

`key`  
调用 <span class="function">mcrypt\_enc\_get\_key\_size</span>
函数获得的密钥最大长度。 小于最大长度的数值都被视为非法参数。

`iv`  
通常情况下，向量大小等于算法的分组大小， 但是你应该通过 <span
class="function">mcrypt\_enc\_get\_iv\_size</span> 函数 来获得这个值。在
ECB 模式下，初始向量会被忽略， 在 CFB，CBC，STREAM，nOFB 和 OFB
模式下，必须提供初始向量。
初始向量要求是随机的，并且是唯一的（不需要是安全的）。
加密和解密必须使用相同的初始向量。
如果你不想使用初始向量，请将其设置为全 0 值，但是不建议你这么做。

### 返回值

如果发生错误，将会返回负数： -3 表示密钥长度有误，-4 表示内存分配失败，
其他值表示未知错误， 同时会显示对应的警告信息。 如果传入参数不正确，返回
**`FALSE`**。

### 参见

-   <span class="function">mcrypt\_module\_open</span>

mcrypt\_generic
===============

加密数据

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_generic</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

本函数用来加密数据。 传入数据长度必须是 n \* 分组大小，否则需要后补
"*\\0*"。 本函数返回加密后的数据。 注意，根据数据补齐不同，
返回的数据可能比输入的数据长度有所增加。

如果你需要把加密后的数据保存到数据库， 请确保保存 mcrypt\_generic
返回的完整的字符串， 否则将无法正确解密。 如果原始数据有 10
个字符，分组大小为 8 （使用 <span
class="function">mcrypt\_enc\_get\_block\_size</span> 获取分组大小），
则数据库中至少需要 16 个字符来保存数据。 请注意 <span
class="function">mdecrypt\_generic</span> 函数返回的数据也会是 16
个字符。 使用 rtrim($str, "\\0") 移除字符串末尾的 0 。

如果你在例如 MySQL 这样的数据库中存储数据， 请注意 varchar
类型的字段会在插入数据时自动移除字符串末尾的“空格”。
由于加密后的数据可能是以空格（ASCII 32）结尾， 这种特性会导致数据损坏。
请使用 tinyblob/tinytext（或 larger）字段来存储加密数据。

### 参数

`td`  
加密描述符。

在调用本函数之前， 请使用 <span
class="function">mcrypt\_generic\_init</span> 函数初始化加密句柄。
在加密完成之后， 需要调用 <span
class="function">mcrypt\_generic\_deinit</span> 函数进行必要的清理工作。
请参见 <span class="function">mcrypt\_module\_open</span> 。

`data`  
要加密的数据。

### 返回值

返回加密后的数据。

### 参见

-   <span class="function">mdecrypt\_generic</span>
-   <span class="function">mcrypt\_generic\_init</span>
-   <span class="function">mcrypt\_generic\_deinit</span>

mcrypt\_get\_block\_size
========================

获得加密算法的分组大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_get\_block\_size</span> ( <span
class="methodparam"><span class="type">int</span> `$cipher`</span> )

<span class="type">int</span> <span
class="methodname">mcrypt\_get\_block\_size</span> ( <span
class="methodparam"><span class="type">string</span> `$cipher`</span> ,
<span class="methodparam"><span class="type">string</span>
`$mode`</span> )

第一个原型针对 libmcrypt 2.2.x， 第二个原型针对 libmcrypt 2.4.x 或
2.5.x。

<span class="function">mcrypt\_get\_block\_size</span> 用来获取 `cipher`
（其中包括了加密模式） 加密算法分组大小。

<span class="function">mcrypt\_enc\_get\_block\_size</span>
函数更加有用， 因为它可以使用 <span
class="function">mcrypt\_module\_open</span> 函数所返回的资源。

### 参数

`cipher`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

### 返回值

返回以字节为单位的此算法的分组数据大小。 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mcrypt\_get\_block\_size</span> 例程**

在 libmcrypt 2.4.x 和 2.5.x 下 如何使用本函数。

``` php
<?php

echo mcrypt_get_block_size('tripledes', 'ecb'); // 8

?>
```

### 参见

-   <span class="function">mcrypt\_get\_key\_size</span>
-   <span class="function">mcrypt\_enc\_get\_block\_size</span>
-   <span class="function">mcrypt\_encrypt</span>

mcrypt\_get\_cipher\_name
=========================

获取加密算法名称

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_get\_cipher\_name</span> ( <span
class="methodparam"><span class="type">int</span> `$cipher`</span> )

<span class="type">string</span> <span
class="methodname">mcrypt\_get\_cipher\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$cipher`</span> )

<span class="function">mcrypt\_get\_cipher\_name</span>
用来获取加密算法名称。

libmcrypt 2.2.x 中，<span
class="function">mcrypt\_get\_cipher\_name</span>
接受整数表达的加密算法， libmcrypt 2.4.x
及更高版本中，它接受字符串表达的加密算法名称，
返回的都是字符串表达的名称，如果算法不存在则返回 **`FALSE`**。

### 参数

`cipher`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

### 返回值

本函数返回加密算法名称， 如果算法不存在返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mcrypt\_get\_cipher\_name</span>
例程**

``` php
<?php
   $cipher = MCRYPT_TripleDES;

   echo mcrypt_get_cipher_name($cipher);
?>
```

以上例程会输出：

    3DES

mcrypt\_get\_iv\_size
=====================

返回指定算法/模式组合的初始向量大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_get\_iv\_size</span> ( <span
class="methodparam"><span class="type">string</span> `$cipher`</span> ,
<span class="methodparam"><span class="type">string</span>
`$mode`</span> )

获取由 `cipher`/`mode` 参数指定的初始向量大小。

<span class="function">mcrypt\_enc\_get\_iv\_size</span> 更加有用，
因为它使用由 <span class="function">mcrypt\_module\_open</span>
返回的资源作为参数。

### 参数

`cipher`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

由于 ECB 模式不使用初始向量，所以会忽略它。 在加密和解密的过程中，
你需要使用相同的初始向量（想象成：开始点）。

### 返回值

返回初始向量的大小，以字节为单位。 如果发生错误，返回 **`FALSE`**。
如果指定的算法/模式不需要初始向量，返回 0。

### 范例

**示例 \#1 <span class="function">mcrypt\_get\_iv\_size</span> 例程**

``` php
<?php
    echo mcrypt_get_iv_size(MCRYPT_CAST_256, MCRYPT_MODE_CFB) . "\n";

    echo mcrypt_get_iv_size('des', 'ecb') . "\n";
?>
```

### 参见

-   <span class="function">mcrypt\_get\_block\_size</span>
-   <span class="function">mcrypt\_enc\_get\_iv\_size</span>
-   <span class="function">mcrypt\_create\_iv</span>

mcrypt\_get\_key\_size
======================

获取指定加密算法的密钥大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_get\_key\_size</span> ( <span
class="methodparam"><span class="type">int</span> `$cipher`</span> )

<span class="type">int</span> <span
class="methodname">mcrypt\_get\_key\_size</span> ( <span
class="methodparam"><span class="type">string</span> `$cipher`</span> ,
<span class="methodparam"><span class="type">string</span>
`$mode`</span> )

第一个原型是针对 libmcrypt 2.2.x 的， 第二个原型是针对 libmcrypt 2.4.x
或 2.5.x 的。

<span class="function">mcrypt\_get\_key\_size</span> 用来获取 由
`cipher` 所指定的算法和模式所需的密钥长度。

<span class="function">mcrypt\_enc\_get\_key\_size</span> 更加有用，
因为它使用由 <span class="function">mcrypt\_module\_open</span>
返回的资源。

### 参数

`cipher`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

### 返回值

返回算法所支持的最大密钥大小，以字节为单位。 或者在失败时返回
**`FALSE`**。

### 范例

**示例 \#1 <span class="function">mcrypt\_get\_key\_size</span> 例程**

``` php
<?php
    echo mcrypt_get_key_size('tripledes', 'ecb');
?>
```

在 libmcrypt 2.4.x 或 2.5.x 版本中， 如果使用本函数。

以上例程会输出：

    24

### 参见

-   <span class="function">mcrypt\_get\_block\_size</span>
-   <span class="function">mcrypt\_enc\_get\_key\_size</span>
-   <span class="function">mcrypt\_encrypt</span>

mcrypt\_list\_algorithms
========================

获取支持的加密算法

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">array</span> <span
class="methodname">mcrypt\_list\_algorithms</span> (\[ <span
class="methodparam"><span class="type">string</span> `$lib_dir`<span
class="initializer"> = ini\_get("mcrypt.algorithms\_dir")</span></span>
\] )

获取 `lib_dir` 中 包含的受支持的算法。

### 参数

`lib_dir`  
指定算法所在的位置。 如果未指定，将使用 `php.ini` 中的
*mcrypt.algorithms\_dir* 指示所指定的位置。

### 返回值

以数组方式返回所有受支持的算法。

### 范例

**示例 \#1 <span class="function">mcrypt\_list\_algorithms</span> 例程**

``` php
<?php
$algorithms = mcrypt_list_algorithms();
print_r($algorithms);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => cast-128
        [1] => gost
        [2] => rijndael-128
        [3] => twofish
        [4] => arcfour
        [5] => cast-256
        [6] => loki97
        [7] => rijndael-192
        [8] => saferplus
        [9] => wake
        [10] => blowfish-compat
        [11] => des
        [12] => rijndael-256
        [13] => serpent
        [14] => xtea
        [15] => blowfish
        [16] => enigma
        [17] => rc2
        [18] => tripledes
    )

mcrypt\_list\_modes
===================

获取所支持的模式

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">array</span> <span
class="methodname">mcrypt\_list\_modes</span> (\[ <span
class="methodparam"><span class="type">string</span> `$lib_dir`<span
class="initializer"> = ini\_get("mcrypt.modes\_dir")</span></span> \] )

获取 `lib_dir` 中 包含的受支持的模式。

### 参数

`lib_dir`  
指定模式所在的位置。 如果未指定，将使用 `php.ini` 中的
*mcrypt.modes\_dir* 指示所指定的位置。

### 返回值

以数组形式返回受支持的模式。

### 范例

**示例 \#1 <span class="function">mcrypt\_list\_modes</span> 例程**

``` php
<?php
    $modes = mcrypt_list_modes();

    foreach ($modes as $mode) {
        echo "$mode <br />\n";
    }
?>
```

本例程列出在默认目录中 所有受支持的模式。 如果在 `php.ini` 中未指定
*mcrypt.modes\_dir*， 则使用默认的 mcrypt 库
安装目录（`/usr/local/lib/libmcrypt`）。

mcrypt\_module\_close
=====================

关闭加密模块

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_module\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> )

关闭加密模块。

### 参数

`td`  
加密描述符。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">mcrypt\_module\_open</span>

mcrypt\_module\_get\_algo\_block\_size
======================================

返回指定算法的分组大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_module\_get\_algo\_block\_size</span> ( <span
class="methodparam"><span class="type">string</span> `$algorithm`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$lib_dir`</span> \] )

返回指定算法的分组大小。

### 参数

`algorithm`  
算法名称。

`lib_dir`  
可选参数 `lib_dir` ， 表示在操作系统上包含模式模块的路径。

### 返回值

返回指定算法的分组大小，以字节为单位。

mcrypt\_module\_get\_algo\_key\_size
====================================

获取打开模式所支持的最大密钥大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">int</span> <span
class="methodname">mcrypt\_module\_get\_algo\_key\_size</span> ( <span
class="methodparam"><span class="type">string</span> `$algorithm`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$lib_dir`</span> \] )

获取打开模式所支持的最大密钥大小。

### 参数

`algorithm`  
算法名称。

`lib_dir`  
可选参数， 表示在操作系统上包含模式模块的路径。

### 返回值

本函数返回算法所支持的最大密钥大小， 以字节为单位。

mcrypt\_module\_get\_supported\_key\_sizes
==========================================

以数组形式返回打开的算法所支持的密钥大小

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">array</span> <span
class="methodname">mcrypt\_module\_get\_supported\_key\_sizes</span> (
<span class="methodparam"><span class="type">string</span>
`$algorithm`</span> \[, <span class="methodparam"><span
class="type">string</span> `$lib_dir`</span> \] )

以数组形式返回指定算法所支持的密钥大小。 如果从 1 到 <span
class="function">mcrypt\_module\_get\_algo\_key\_size</span>
的密钥大小都支持，则返回空数组。

### 参数

`algorithm`  
算法名称。

`lib_dir`  
可选参数， 表示在操作系统上包含算法模块的路径。

### 返回值

以数组形式返回指定算法所支持的密钥大小。 如果从 1 到 <span
class="function">mcrypt\_module\_get\_algo\_key\_size</span>
的密钥大小都支持，则返回空数组。

### 参见

-   <span
    class="function">mcrypt\_enc\_get\_supported\_key\_sizes</span>

mcrypt\_module\_is\_block\_algorithm\_mode
==========================================

返回指定模块是否是分组加密模式

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_module\_is\_block\_algorithm\_mode</span> (
<span class="methodparam"><span class="type">string</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$lib_dir`</span> \] )

对于分组加密模式，返回 **`TRUE`**， 反之返回 **`FALSE`**。 （例如，对于
STREAM 模式返回 **`FALSE`**，对于 cbc，cfb，ofb 返回 **`TRUE`**）

### 参数

`mode`  
模式。

`lib_dir`  
可选参数， 表示在操作系统上包含算法模块的路径。

### 返回值

对于分组加密模式，返回 **`TRUE`**， 反之返回 **`FALSE`**。 （例如，对于
STREAM 模式返回 **`FALSE`**，对于 cbc，cfb，ofb 返回 **`TRUE`**）

mcrypt\_module\_is\_block\_algorithm
====================================

检测指定算法是否为分组加密算法

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_module\_is\_block\_algorithm</span> ( <span
class="methodparam"><span class="type">string</span> `$algorithm`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$lib_dir`</span> \] )

如果指定算法是分组加密算法，返回 **`TRUE`**， 反之返回 **`FALSE`**。

### 参数

`algorithm`  
要检测的算法。

`lib_dir`  
可选参数 `lib_dir`， 表示在操作系统上包含算法模块的路径。

### 返回值

如果指定算法是分组加密算法，返回 **`TRUE`**， 反之返回 **`FALSE`**。

mcrypt\_module\_is\_block\_mode
===============================

检测指定模式是否以分组方式输出

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_module\_is\_block\_mode</span> ( <span
class="methodparam"><span class="type">string</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$lib_dir`</span> \] )

如果模式是以字节块（分组）方式输出，则返回 **`TRUE`**，
如果只是以字节方式输出，则返回 **`FALSE`**。 （例如，对于 cbc 和 ecb
模式，返回 **`TRUE`**，对于 cfb 和 stream 模式，返回 **`FALSE`**）

### 参数

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

`lib_dir`  
可选参数 `lib_dir` ， 表示在操作系统上包含模式模块的路径。

### 返回值

如果模式是以字节块（分组）方式输出，则返回 **`TRUE`**，
如果只是以字节方式输出，则返回 **`FALSE`**。 （例如，对于 cbc 和 ecb
模式，返回 **`TRUE`**，对于 cfb 和 stream 模式，返回 **`FALSE`**）

mcrypt\_module\_open
====================

打开算法和模式对应的模块

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">resource</span> <span
class="methodname">mcrypt\_module\_open</span> ( <span
class="methodparam"><span class="type">string</span> `$algorithm`</span>
, <span class="methodparam"><span class="type">string</span>
`$algorithm_directory`</span> , <span class="methodparam"><span
class="type">string</span> `$mode`</span> , <span
class="methodparam"><span class="type">string</span>
`$mode_directory`</span> )

本函数打开指定算法和模式对应的模块。 算法名称可以是字符串，例如
*"twofish"*， 也可以是 **`MCRYPT_ciphername`** 常量。 调用 <span
class="function">mcrypt\_module\_close</span> 函数可以关闭模块。

### 参数

`algorithm`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`algorithm_directory`  
`algorithm_directory` 参数指示加密模块的位置。
如果你提供此参数，则使用你指定的值。
如果将此参数设置为空字符串（*""*），将使用 `php.ini` 中的
*mcrypt.algorithms\_dir* 。 如果不指定此参数，则使用 libmcrypt
的编译路径 （通常是 `/usr/local/lib/libmcrypt`）。

`mode`  
**`MCRYPT_MODE_modename`**
常量中的一个，或以下字符串中的一个："ecb"，"cbc"，"cfb"，"ofb"，"nofb"
和 "stream"。

`mode_directory`  
`algorithm_directory` 参数指示加密模式的位置。
如果你提供此参数，则使用你指定的值。
如果将此参数设置为空字符串（*""*），将使用 `php.ini` 中的
*mcrypt.modes\_dir* 。 如果不指定此参数，则使用 libmcrypt 的编译路径
（通常是 `/usr/local/lib/libmcrypt`）。

### 返回值

成功则返回加密描述符，如果发生错误则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mcrypt\_module\_open</span> 例程**

``` php
<?php
    $td = mcrypt_module_open(MCRYPT_DES, '',
        MCRYPT_MODE_ECB, '/usr/lib/mcrypt-modes');

    $td = mcrypt_module_open('rijndael-256', '', 'ofb', '');
?>
```

例程中的第一行从默认目录打开 *DES* 加密算法， 从 `/usr/lib/mcrypt-modes`
目录打开 *ECB* 模式。 第二个示例中，使用字符串形式表示算法和模式，
这种形式仅适用于 libmcrypt 2.4.x 或 2.5.x 版本。

**示例 \#2 在加密中使用 <span
class="function">mcrypt\_module\_open</span>**

``` php
<?php
    /* 打开加密算法和模式 */
    $td = mcrypt_module_open('rijndael-256', '', 'ofb', '');

    /* 创建初始向量，并且检测密钥长度。 
     * Windows 平台请使用 MCRYPT_RAND。 */
    $iv = mcrypt_create_iv(mcrypt_enc_get_iv_size($td), MCRYPT_DEV_RANDOM);
    $ks = mcrypt_enc_get_key_size($td);

    /* 创建密钥 */
    $key = substr(md5('very secret key'), 0, $ks);

    /* 初始化加密 */
    mcrypt_generic_init($td, $key, $iv);

    /* 加密数据 */
    $encrypted = mcrypt_generic($td, 'This is very important data');

    /* 结束加密，执行清理工作 */
    mcrypt_generic_deinit($td);

    /* 初始化解密模块 */
    mcrypt_generic_init($td, $key, $iv);

    /* 解密数据 */
    $decrypted = mdecrypt_generic($td, $encrypted);

    /* 结束解密，执行清理工作，并且关闭模块 */
    mcrypt_generic_deinit($td);
    mcrypt_module_close($td);

    /* 显示文本 */
    echo trim($decrypted) . "\n";
?>
```

### 参见

-   <span class="function">mcrypt\_module\_close</span>
-   <span class="function">mcrypt\_generic</span>
-   <span class="function">mdecrypt\_generic</span>
-   <span class="function">mcrypt\_generic\_init</span>
-   <span class="function">mcrypt\_generic\_deinit</span>

mcrypt\_module\_self\_test
==========================

在指定模块上执行自检

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">bool</span> <span
class="methodname">mcrypt\_module\_self\_test</span> ( <span
class="methodparam"><span class="type">string</span> `$algorithm`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$lib_dir`</span> \] )

在指定模块上执行自检。

### 参数

`algorithm`  
**`MCRYPT_ciphername`** 常量中的一个，或者是字符串值的算法名称。

`lib_dir`  
可选参数 `lib_dir`， 表示包含加密算法模块的路径。

### 返回值

自检成功返回 **`TRUE`**， 自检失败返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mcrypt\_module\_self\_test</span>
例程**

``` php
<?php
var_dump(mcrypt_module_self_test(MCRYPT_RIJNDAEL_128)) . "\n";
var_dump(mcrypt_module_self_test(MCRYPT_BOGUS_CYPHER));
?>
```

以上例程会输出：

    bool(true)
    bool(false)

mcrypt\_ofb
===========

使用 OFB 模式加密/解密数据

**Warning**

This function was *DEPRECATED* in PHP 5.5.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this function include:

-   <span class="function">mcrypt\_decrypt</span>
-   <span class="function">mcrypt\_encrypt</span>

### 说明

<span class="type">string</span> <span
class="methodname">mcrypt\_ofb</span> ( <span class="methodparam"><span
class="type">int</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> , <span class="methodparam"><span
class="type">string</span> `$iv`</span> )

<span class="type">string</span> <span
class="methodname">mcrypt\_ofb</span> ( <span class="methodparam"><span
class="type">string</span> `$cipher`</span> , <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$iv`</span> \] )

第一个原型是针对 libmcrypt 2.2.x 的， 第二个原型是针对 libmcrypt 2.4.x
及更高版本的。 `mode` 可选值为： **`MCRYPT_ENCRYPT`** 或
**`MCRYPT_DECRYPT`**。

mdecrypt\_generic
=================

解密数据

**Warning**

本函数已自 PHP 7.1.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">string</span> <span
class="methodname">mdecrypt\_generic</span> ( <span
class="methodparam"><span class="type">resource</span> `$td`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

解密数据。 请注意，由于存在数据补齐的情况，
返回字符串的长度可能和明文的长度不相等。

### 参数

`td`  
由 <span class="function">mcrypt\_module\_open</span>
函数创建的加密描述符。

`data`  
密文。

### 范例

**示例 \#1 <span class="function">mdecrypt\_generic</span> 例程**

``` php
<?php
    /* 数据 */
    $key = 'this is a very long key, even too long for the cipher';
    $plain_text = 'very important data';

    /* 打开加密模块，并且创建初始向量 */
    $td = mcrypt_module_open('des', '', 'ecb', '');
    $key = substr($key, 0, mcrypt_enc_get_key_size($td));
    $iv_size = mcrypt_enc_get_iv_size($td);
    $iv = mcrypt_create_iv($iv_size, MCRYPT_RAND);

    /* 初始化加密句柄 */
    if (mcrypt_generic_init($td, $key, $iv) != -1) {

        /* 加密数据 */
        $c_t = mcrypt_generic($td, $plain_text);
        mcrypt_generic_deinit($td);

        /* 为解密重新初始化缓冲区 */
        mcrypt_generic_init($td, $key, $iv);
        $p_t = mdecrypt_generic($td, $c_t);

        /* 执行清理工作 */
        mcrypt_generic_deinit($td);
        mcrypt_module_close($td);
    }

    if (strncmp($p_t, $plain_text, strlen($plain_text)) == 0) {
        echo "ok\n";
    } else {
        echo "error\n";
    }
?>
```

上例中演示了如何检测 解密后的数据是否和原始明文长度一致。
需要着重提醒的是，在对数据进行机密之前， 必须使用 <span
class="function">mcrypt\_generic\_init</span> 函数来重新初始化缓冲区。

调用本函数之前， 必须使用密钥和初始向量来调用 <span
class="function">mcrypt\_generic\_init</span> 函数
对解密句柄进行初始化。 加解密工作完成之后，需要调用 <span
class="function">mcrypt\_generic\_deinit</span> 来释放加解密缓冲区。
例程请参见 <span class="function">mcrypt\_module\_open</span>。

### 参见

-   <span class="function">mcrypt\_generic</span>
-   <span class="function">mcrypt\_generic\_init</span>
-   <span class="function">mcrypt\_generic\_deinit</span>

**目录**

-   [mcrypt\_cbc](/ref/mcrypt.html#mcrypt_cbc) — 以 CBC 模式加解密数据
-   [mcrypt\_cfb](/ref/mcrypt.html#mcrypt_cfb) — 以 CFB 模式加解密数据
-   [mcrypt\_create\_iv](/ref/mcrypt.html#mcrypt_create_iv) —
    从随机源创建初始向量
-   [mcrypt\_decrypt](/ref/mcrypt.html#mcrypt_decrypt) —
    使用给定参数解密密文
-   [mcrypt\_ecb](/ref/mcrypt.html#mcrypt_ecb) — 已废弃：使用 ECB
    模式加解密数据
-   [mcrypt\_enc\_get\_algorithms\_name](/ref/mcrypt.html#mcrypt_enc_get_algorithms_name)
    — 返回打开的算法名称
-   [mcrypt\_enc\_get\_block\_size](/ref/mcrypt.html#mcrypt_enc_get_block_size)
    — 返回打开的算法的分组大小
-   [mcrypt\_enc\_get\_iv\_size](/ref/mcrypt.html#mcrypt_enc_get_iv_size)
    — 返回打开的算法的初始向量大小
-   [mcrypt\_enc\_get\_key\_size](/ref/mcrypt.html#mcrypt_enc_get_key_size)
    — 返回打开的模式所能支持的最长密钥
-   [mcrypt\_enc\_get\_modes\_name](/ref/mcrypt.html#mcrypt_enc_get_modes_name)
    — 返回打开的模式的名称
-   [mcrypt\_enc\_get\_supported\_key\_sizes](/ref/mcrypt.html#mcrypt_enc_get_supported_key_sizes)
    — 以数组方式返回打开的算法所支持的密钥长度
-   [mcrypt\_enc\_is\_block\_algorithm\_mode](/ref/mcrypt.html#mcrypt_enc_is_block_algorithm_mode)
    — 检测打开的模式是否支持分组加密
-   [mcrypt\_enc\_is\_block\_algorithm](/ref/mcrypt.html#mcrypt_enc_is_block_algorithm)
    — 检测打开模式的算法是否为分组算法
-   [mcrypt\_enc\_is\_block\_mode](/ref/mcrypt.html#mcrypt_enc_is_block_mode)
    — 检测打开的模式是否以分组方式输出
-   [mcrypt\_enc\_self\_test](/ref/mcrypt.html#mcrypt_enc_self_test) —
    在打开的模块上进行自检
-   [mcrypt\_encrypt](/ref/mcrypt.html#mcrypt_encrypt) —
    使用给定参数加密明文
-   [mcrypt\_generic\_deinit](/ref/mcrypt.html#mcrypt_generic_deinit) —
    对加密模块进行清理工作
-   [mcrypt\_generic\_end](/ref/mcrypt.html#mcrypt_generic_end) —
    终止加密
-   [mcrypt\_generic\_init](/ref/mcrypt.html#mcrypt_generic_init) —
    初始化加密所需的缓冲区
-   [mcrypt\_generic](/ref/mcrypt.html#mcrypt_generic) — 加密数据
-   [mcrypt\_get\_block\_size](/ref/mcrypt.html#mcrypt_get_block_size) —
    获得加密算法的分组大小
-   [mcrypt\_get\_cipher\_name](/ref/mcrypt.html#mcrypt_get_cipher_name)
    — 获取加密算法名称
-   [mcrypt\_get\_iv\_size](/ref/mcrypt.html#mcrypt_get_iv_size) —
    返回指定算法/模式组合的初始向量大小
-   [mcrypt\_get\_key\_size](/ref/mcrypt.html#mcrypt_get_key_size) —
    获取指定加密算法的密钥大小
-   [mcrypt\_list\_algorithms](/ref/mcrypt.html#mcrypt_list_algorithms)
    — 获取支持的加密算法
-   [mcrypt\_list\_modes](/ref/mcrypt.html#mcrypt_list_modes) —
    获取所支持的模式
-   [mcrypt\_module\_close](/ref/mcrypt.html#mcrypt_module_close) —
    关闭加密模块
-   [mcrypt\_module\_get\_algo\_block\_size](/ref/mcrypt.html#mcrypt_module_get_algo_block_size)
    — 返回指定算法的分组大小
-   [mcrypt\_module\_get\_algo\_key\_size](/ref/mcrypt.html#mcrypt_module_get_algo_key_size)
    — 获取打开模式所支持的最大密钥大小
-   [mcrypt\_module\_get\_supported\_key\_sizes](/ref/mcrypt.html#mcrypt_module_get_supported_key_sizes)
    — 以数组形式返回打开的算法所支持的密钥大小
-   [mcrypt\_module\_is\_block\_algorithm\_mode](/ref/mcrypt.html#mcrypt_module_is_block_algorithm_mode)
    — 返回指定模块是否是分组加密模式
-   [mcrypt\_module\_is\_block\_algorithm](/ref/mcrypt.html#mcrypt_module_is_block_algorithm)
    — 检测指定算法是否为分组加密算法
-   [mcrypt\_module\_is\_block\_mode](/ref/mcrypt.html#mcrypt_module_is_block_mode)
    — 检测指定模式是否以分组方式输出
-   [mcrypt\_module\_open](/ref/mcrypt.html#mcrypt_module_open) —
    打开算法和模式对应的模块
-   [mcrypt\_module\_self\_test](/ref/mcrypt.html#mcrypt_module_self_test)
    — 在指定模块上执行自检
-   [mcrypt\_ofb](/ref/mcrypt.html#mcrypt_ofb) — 使用 OFB
    模式加密/解密数据
-   [mdecrypt\_generic](/ref/mcrypt.html#mdecrypt_generic) — 解密数据
