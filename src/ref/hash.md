hash\_algos
===========

返回已注册的哈希算法列表

### 说明

<span class="type">array</span> <span
class="methodname">hash\_algos</span> ( <span
class="methodparam">void</span> )

### 返回值

返回一个数值索引的数组， 包含了受支持的哈希算法名称。

### 更新日志

| 版本  | 说明                                                                                                                                                                            |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | 加入 sha512/224，sha512/256，sha3-224，sha3-256，sha3-384 以及 sha3-512 算法的支持。                                                                                            |
| 5.6.0 | 加入对 gost-crypto 算法的支持。 参照 <a href="http://www.faqs.org/rfcs/rfc4357" class="link external">» RFC 4357，11.2 小节</a> 定义的 CryptoPro S-box 表格实现 GOST 哈希函数。 |
| 5.4.0 | 加入对于 joaat，fnv132 和 fnv164 算法的支持。移除 Salsa10 和 Salsa20 算法。                                                                                                     |
| 5.3.0 | 加入对 md2，ripemd256，ripemd320，salsa10，salsa20，snefru256 和 sha224 哈希算法的支持。                                                                                        |

### 范例

**示例 \#1 <span class="function">hash\_algos</span> 例程**

在 PHP 5.6.0 中，<span class="function">hash\_algos</span>
会返回下表所示的算法清单：

``` php
<?php
print_r(hash_algos());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => md2
        [1] => md4
        [2] => md5
        [3] => sha1
        [4] => sha224
        [5] => sha256
        [6] => sha384
        [7] => sha512
        [8] => ripemd128
        [9] => ripemd160
        [10] => ripemd256
        [11] => ripemd320
        [12] => whirlpool
        [13] => tiger128,3
        [14] => tiger160,3
        [15] => tiger192,3
        [16] => tiger128,4
        [17] => tiger160,4
        [18] => tiger192,4
        [19] => snefru
        [20] => snefru256
        [21] => gost
        [22] => gost-crypto
        [23] => adler32
        [24] => crc32
        [25] => crc32b
        [26] => fnv132
        [27] => fnv1a32
        [28] => fnv164
        [29] => fnv1a64
        [30] => joaat
        [31] => haval128,3
        [32] => haval160,3
        [33] => haval192,3
        [34] => haval224,3
        [35] => haval256,3
        [36] => haval128,4
        [37] => haval160,4
        [38] => haval192,4
        [39] => haval224,4
        [40] => haval256,4
        [41] => haval128,5
        [42] => haval160,5
        [43] => haval192,5
        [44] => haval224,5
        [45] => haval256,5
    )

### 参见

-   <span class="function">hash\_hmac\_algos</span>

hash\_copy
==========

拷贝哈希运算上下文

### 说明

<span class="type">HashContext</span> <span
class="methodname">hash\_copy</span> ( <span class="methodparam"><span
class="type">HashContext</span> `$context`</span> )

### 参数

`context`  
由 <span class="function">hash\_init</span> 函数返回的哈希运算上下文。

### 返回值

返回哈希运算上下文的一个复本。

### 更新日志

| 版本  | 说明                                                                                       |
|-------|--------------------------------------------------------------------------------------------|
| 7.2.0 | 接受的参数以及返回值从资源类型修改为 <span class="classname">HashContext</span> 对象类型。 |

### 范例

**示例 \#1 <span class="function">hash\_copy</span> 例程**

``` php
<?php
$context = hash_init("md5");
hash_update($context, "data");

/* 拷贝上下文资源以便继续使用 */
$copy_context = hash_copy($context);

echo hash_final($context), "\n";

hash_update($copy_context, "data");
echo hash_final($copy_context), "\n";
?>
```

以上例程会输出：

    8d777f385d3dfec8815d20f7496026dc
    511ae0b1c13f95e5f08f1a0dd3da3d93

hash\_equals
============

可防止时序攻击的字符串比较

### 说明

<span class="type">bool</span> <span
class="methodname">hash\_equals</span> ( <span class="methodparam"><span
class="type">string</span> `$known_string`</span> , <span
class="methodparam"><span class="type">string</span>
`$user_string`</span> )

比较两个字符串，无论它们是否相等，本函数的时间消耗是恒定的。

本函数可以用在需要防止时序攻击的字符串比较场景中， 例如，可以用在比较
<span class="function">crypt</span> 密码哈希值的场景。

### 参数

`known_string`  
已知长度的、要参与比较的 <span class="type">string</span>

`user_string`  
用户提供的字符串

### 返回值

当两个字符串相等时返回 **`TRUE`**，否则返回 **`FALSE`**。

### 错误／异常

如果所提供的 2 个参数中任何一个不是字符串， 会导致 **`E_WARNING`**
消息。

### 范例

**示例 \#1 <span class="function">hash\_equals</span> 例程**

``` php
<?php
$expected  = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$correct   = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$incorrect = crypt('apple',  '$2a$07$usesomesillystringforsalt$');

var_dump(hash_equals($expected, $correct));
var_dump(hash_equals($expected, $incorrect));
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### 注释

> **Note**:
>
> 要想成功进行比较，那么所提供的 2 个参数必须是相同长度的字符串。
> 如果所提供的字符串长度不同，那么本函数会立即返回 **`FALSE`**，
> 在时序攻击的场景下，已知字符串的长度可能会被泄露。

> **Note**:
>
> 非常重要的一点是，用户提供的字符串必须是第二个参数。

hash\_file
==========

使用给定文件的内容生成哈希值

### 说明

<span class="type">string</span> <span
class="methodname">hash\_file</span> ( <span class="methodparam"><span
class="type">string</span> `$algo`</span> , <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$raw_output`<span class="initializer"> = **`FALSE`**</span></span> \] )

### 参数

`algo`  
要使用的哈希算法的名称，例如："md5"，"sha256"，"haval160,4" 等。

`filename`  
要进行哈希运算的文件路径。支持 fopen 封装器。

`raw_output`  
设置为 **`TRUE`**，输出格式为原始的二进制数据。 设置为
**`FALSE`**，输出小写的 16 进制字符串。

### 返回值

如果 `raw_output` 设置为 **`TRUE`**，
则返回原始二进制数据表示的信息摘要， 否则返回 16
进制小写字符串格式表示的信息摘要。

### 范例

**示例 \#1 使用 <span class="function">hash\_file</span>**

``` php
<?php
/* 创建一个要计算哈希值的文件 */
file_put_contents('example.txt', 'The quick brown fox jumped over the lazy dog.');

echo hash_file('md5', 'example.txt');
?>
```

以上例程会输出：

    5c6ffbdd40d9556b73a21e63c3e0e904

### 参见

-   <span class="function">hash</span>
-   <span class="function">hash\_hmac\_file</span>
-   <span class="function">hash\_update\_file</span>
-   <span class="function">md5\_file</span>
-   <span class="function">sha1\_file</span>

hash\_final
===========

结束增量哈希，并且返回摘要结果

### 说明

<span class="type">string</span> <span
class="methodname">hash\_final</span> ( <span class="methodparam"><span
class="type">HashContext</span> `$context`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$raw_output`<span
class="initializer"> = **`FALSE`**</span></span> \] )

### 参数

`context`  
<span class="function">hash\_init</span> 函数返回的哈希运算上下文资源。

`raw_output`  
设置为 **`TRUE`**，输出格式为原始的二进制数据。 设置为
**`FALSE`**，输出小写的 16 进制字符串。

### 返回值

如果 `raw_output` 设置为 **`TRUE`**，
则返回原始二进制数据表示的信息摘要， 否则返回 16
进制小写字符串格式表示的信息摘要。

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 7.2.0 | 接收参数从资源类型修改为 <span class="classname">HashContext</span> 对象类型。 |

### 范例

**示例 \#1 <span class="function">hash\_final</span> 例程**

``` php
<?php
$ctx = hash_init('sha1');
hash_update($ctx, 'The quick brown fox jumped over the lazy dog.');
echo hash_final($ctx);
?>
```

以上例程会输出：

    c0854fb9fb03c41cce3802cb0d220529e6eef94e

### 参见

-   <span class="function">hash\_init</span>
-   <span class="function">hash\_update</span>
-   <span class="function">hash\_update\_stream</span>
-   <span class="function">hash\_update\_file</span>

hash\_hkdf
==========

Generate a HKDF key derivation of a supplied key input

### 说明

<span class="type">string</span> <span
class="methodname">hash\_hkdf</span> ( <span class="methodparam"><span
class="type">string</span> `$algo`</span> , <span
class="methodparam"><span class="type">string</span> `$ikm`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$info`<span
class="initializer"> = ''</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$salt`<span
class="initializer"> = ''</span></span> \]\]\] )

### 参数

`algo`  
Name of selected hashing algorithm (i.e. "sha256", "sha512",
"haval160,4", etc..) See <span class="function">hash\_algos</span> for a
list of supported algorithms.

> **Note**:
>
> Non-cryptographic hash functions are not allowed.

`ikm`  
Input keying material (raw binary). Cannot be empty.

`length`  
Desired output length in bytes. Cannot be greater than 255 times the
chosen hash function size.

If `length` is *0*, the output length will default to the chosen hash
function size.

`info`  
Application/context-specific info string.

`salt`  
Salt to use during derivation.

While optional, adding random salt significantly improves the strength
of HKDF.

### 返回值

Returns a string containing a raw binary representation of the derived
key (also known as output keying material - OKM); or **`FALSE`** on
failure.

### 错误／异常

An **`E_WARNING`** will be raised if `ikm` is empty, `algo` is
unknown/non-cryptographic, `length` is less than *0* or too large
(greater than 255 times the size of the hash function).

### 范例

**示例 \#1 <span class="function">hash\_hkdf</span> example**

``` php
<?php
// Generate a random key, and salt to strengthen it during derivation.
$inputKey = random_bytes(32);
$salt = random_bytes(16);

// Derive a pair of separate keys, using the same input created above.
$encryptionKey = hash_hkdf('sha256', $inputKey, 32, 'aes-256-encryption', $salt);
$authenticationKey = hash_hkdf('sha256', $inputKey, 32, 'sha-256-authentication', $salt);

var_dump($encryptionKey !== $authenticationKey); // bool(true)
?>
```

The above example produces a pair of separate keys, suitable for
creation of an encrypt-then-HMAC construct, using AES-256 and SHA-256
for encryption and authentication respectively.

### 参见

-   <span class="function">hash\_pbkdf2</span>
-   <a href="http://www.faqs.org/rfcs/rfc5869" class="link external">» RFC 5869</a>
-   <a href="https://github.com/narfbg/hash_hkdf_compat" class="link external">» userland implementation</a>

hash\_hmac\_algos
=================

Return a list of registered hashing algorithms suitable for hash\_hmac

### 说明

<span class="type">array</span> <span
class="methodname">hash\_hmac\_algos</span> ( <span
class="methodparam">void</span> )

### 返回值

Returns a numerically indexed array containing the list of supported
hashing algorithms suitable for <span
class="function">hash\_hmac</span>.

### 范例

**示例 \#1 <span class="function">hash\_hmac\_algos</span> example**

``` php
<?php
print_r(hash_hmac_algos());
```

以上例程的输出类似于：

    Array
    (
        [0] => md2
        [1] => md4
        [2] => md5
        [3] => sha1
        [4] => sha224
        [5] => sha256
        [6] => sha384
        [7] => sha512/224
        [8] => sha512/256
        [9] => sha512
        [10] => sha3-224
        [11] => sha3-256
        [12] => sha3-384
        [13] => sha3-512
        [14] => ripemd128
        [15] => ripemd160
        [16] => ripemd256
        [17] => ripemd320
        [18] => whirlpool
        [19] => tiger128,3
        [20] => tiger160,3
        [21] => tiger192,3
        [22] => tiger128,4
        [23] => tiger160,4
        [24] => tiger192,4
        [25] => snefru
        [26] => snefru256
        [27] => gost
        [28] => gost-crypto
        [29] => haval128,3
        [30] => haval160,3
        [31] => haval192,3
        [32] => haval224,3
        [33] => haval256,3
        [34] => haval128,4
        [35] => haval160,4
        [36] => haval192,4
        [37] => haval224,4
        [38] => haval256,4
        [39] => haval128,5
        [40] => haval160,5
        [41] => haval192,5
        [42] => haval224,5
        [43] => haval256,5
    )

### 注释

> **Note**:
>
> Before PHP 7.2.0 the only means to get a list of supported hash
> algorithms has been to call <span class="function">hash\_algos</span>
> which also returns hash algorithms that are not suitable for <span
> class="function">hash\_hmac</span>.

### 参见

-   <span class="function">hash\_hmac</span>
-   <span class="function">hash\_algos</span>

hash\_hmac\_file
================

使用 HMAC 方法和给定文件的内容生成带密钥的哈希值

### 说明

<span class="type">string</span> <span
class="methodname">hash\_hmac\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$algo`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$raw_output`<span
class="initializer"> = **`FALSE`**</span></span> \] )

### 参数

`algo`  
要使用的哈希算法名称，例如："md5"，"sha256"，"haval160,4" 等。
如何获取受支持的算法清单，请参见 <span
class="function">hash\_hmac\_algos</span> 函数。

`filename`  
要进行哈希运算的文件路径，支持 fopen 封装器。

`key`  
使用 HMAC 生成信息摘要时所使用的密钥。

`raw_output`  
设置为 **`TRUE`** 输出原始二进制数据， 设置为 **`FALSE`** 输出小写 16
进制字符串。

### 返回值

如果 `raw_output` 设置为 **`TRUE`**，
则返回原始二进制数据表示的信息摘要， 否则返回 16
进制小写字符串格式表示的信息摘要。 如果 `algo`
参数指定的不是受支持的算法，或者无法读取 `filename` 给定的文件，则返回
**`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                          |
|-------|-----------------------------------------------------------------------------------------------|
| 7.2.0 | 不再支持非加密的哈希函数（adler32，crc32，crc32b，fnv132，fnv1a32，fnv164，fnv1a64，joaat）。 |

### 范例

**示例 \#1 <span class="function">hash\_hmac\_file</span> 例程**

``` php
<?php
/* 创建一个要计算哈希值的文件 */
file_put_contents('example.txt', 'The quick brown fox jumped over the lazy dog.');

echo hash_hmac_file('md5', 'example.txt', 'secret');
?>
```

以上例程会输出：

    7eb2b5c37443418fc77c136dd20e859c

### 参见

-   <span class="function">hash\_hmac\_algos</span>
-   <span class="function">hash\_hmac</span>
-   <span class="function">hash\_file</span>

hash\_hmac
==========

使用 HMAC 方法生成带有密钥的哈希值

### 说明

<span class="type">string</span> <span
class="methodname">hash\_hmac</span> ( <span class="methodparam"><span
class="type">string</span> `$algo`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$raw_output`<span class="initializer"> = **`FALSE`**</span></span> \] )

### 参数

`algo`  
要使用的哈希算法名称，例如："md5"，"sha256"，"haval160,4" 等。
如何获取受支持的算法清单，请参见 <span
class="function">hash\_hmac\_algos</span> 函数。

`data`  
要进行哈希运算的消息。

`key`  
使用 HMAC 生成信息摘要时所使用的密钥。

`raw_output`  
设置为 **`TRUE`** 输出原始二进制数据， 设置为 **`FALSE`** 输出小写 16
进制字符串。

### 返回值

如果 `raw_output` 设置为 **`TRUE`**，
则返回原始二进制数据表示的信息摘要， 否则返回 16
进制小写字符串格式表示的信息摘要。 如果 `algo`
参数指定的不是受支持的算法，返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                          |
|-------|-----------------------------------------------------------------------------------------------|
| 7.2.0 | 不再支持非加密的哈希函数（adler32，crc32，crc32b，fnv132，fnv1a32，fnv164，fnv1a64，joaat）。 |

### 范例

**示例 \#1 <span class="function">hash\_hmac</span> 例程**

``` php
<?php
echo hash_hmac('ripemd160', 'The quick brown fox jumped over the lazy dog.', 'secret');
?>
```

以上例程会输出：

    b8e7ae12510bdfb1812e463a7f086122cf37e4f7

### 参见

-   <span class="function">hash</span>
-   <span class="function">hash\_hmac\_algos</span>
-   <span class="function">hash\_init</span>
-   <span class="function">hash\_hmac\_file</span>

hash\_init
==========

初始化增量哈希运算上下文

### 说明

<span class="type">HashContext</span> <span
class="methodname">hash\_init</span> ( <span class="methodparam"><span
class="type">string</span> `$algo`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$key`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

### 参数

`algo`  
要使用的哈希算法名称，例如："md5"，"sha256"，"haval160,4" 等。
如何获取受支持的算法清单，请参见 <span
class="function">hash\_algos</span>。

`options`  
进行哈希运算的可选设置，目前仅支持一个选项：**`HASH_HMAC`**。
当指定此选项的时候，*必须* 指定 `key` 参数。

`key`  
当 `options` 参数为 **`HASH_HMAC`** 时， 使用此参数传入进行 HMAC
哈希运算时的共享密钥。

### 返回值

返回哈希运算上下文对象，以供 <span
class="function">hash\_update</span>， <span
class="function">hash\_update\_stream</span>，<span
class="function">hash\_update\_file</span>, 和 <span
class="function">hash\_final</span> 函数使用。

### 更新日志

| 版本  | 说明                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | 当使用 **`HASH_HMAC`** 选项的时候，不再支持非加密的哈希函数（adler32，crc32，crc32b，fnv132，fnv1a32，fnv164，fnv1a64，joaat）。 |
| 7.2.0 | 返回 <span class="classname">HashContext</span> 对象，不再返回资源类型。                                                         |

### 范例

**示例 \#1 增量哈希运算例程**

``` php
<?php
$ctx = hash_init('md5');
hash_update($ctx, 'The quick brown fox ');
hash_update($ctx, 'jumped over the lazy dog.');
echo hash_final($ctx);
?>
```

以上例程会输出：

    5c6ffbdd40d9556b73a21e63c3e0e904

### 参见

-   <span class="function">hash</span>
-   <span class="function">hash\_algos</span>
-   <span class="function">hash\_file</span>
-   <span class="function">hash\_hmac</span>
-   <span class="function">hash\_hmac\_file</span>

hash\_pbkdf2
============

生成所提供密码的 PBKDF2 密钥导出

### 说明

<span class="type">string</span> <span
class="methodname">hash\_pbkdf2</span> ( <span class="methodparam"><span
class="type">string</span> `$algo`</span> , <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">string</span>
`$salt`</span> , <span class="methodparam"><span class="type">int</span>
`$iterations`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$raw_output`<span class="initializer"> =
**`FALSE`**</span></span> \]\] )

### 参数

`algo`  
哈希算法名称，例如 *md5*，*sha256*，*haval160,4* 等。
受支持的算法清单请参见 <span class="function">hash\_algos</span>。

`password`  
要进行导出的密码。

`salt`  
进行导出时所使用的“盐”，这个值应该是随机生成的。

`iterations`  
进行导出时的迭代次数。

`length`  
密钥导出数据的长度。如果 `raw_output` 为 **`TRUE`**，
此参数为密钥导出数据的字节长度。如果 `raw_output` 为 **`FALSE`**，
此参数为密钥导出数据的字节长度的 2 倍，因为 1 个字节数据对应的 2 个 16
进制的字符。

如果传入 *0*，则使用所选算法的完整输出大小。

`raw_output`  
设置为 **`TRUE`** 输出原始二进制数据， 设置为 **`FALSE`** 输出小写 16
进制字符串。

### 返回值

如果 `raw_output` 设置为 **`TRUE`**，
则返回原始二进制数据表示的信息摘要， 否则返回 16
进制小写字符串格式表示的信息摘要。

### 错误／异常

在以下情况下会产生 **`E_WARNING`**： 指定了未知的算法， `iterations`
小于等于 *0*， `length` 小于等于 *0* 或者 `salt` 过长（大于
**`INT_MAX`** *- 4*）。

### 更新日志

| 版本  | 说明                                                                                          |
|-------|-----------------------------------------------------------------------------------------------|
| 7.2.0 | 不再支持非加密的哈希函数（adler32，crc32，crc32b，fnv132，fnv1a32，fnv164，fnv1a64，joaat）。 |

### 范例

**示例 \#1 <span class="function">hash\_pbkdf2</span> 例程，基础用法**

``` php
<?php
$password = "password";
$iterations = 1000;

// 使用 openssl_random_pseudo_bytes()，random_bytes()，或者其他合适的随机数生成函数
// 来生成随机初始向量
$salt = openssl_random_pseudo_bytes(16, MCRYPT_DEV_URANDOM);

$hash = hash_pbkdf2("sha256", $password, $salt, $iterations, 20);
echo $hash;
?>
```

以上例程的输出类似于：

    120fb6cffcf8b32c43e7

### 注释

**Caution**

为了安全起见，可以使用 PBKDF2 方法对密码明文进行哈希运算后再存储。
但是更好的方案是使用 <span class="function">password\_hash</span> 函数
或者使用 **`CRYPT_BLOWFISH`** 算法调用 <span
class="function">crypt</span> 函数。

### 参见

-   <span class="function">crypt</span>
-   <span class="function">password\_hash</span>
-   <span class="function">hash</span>
-   <span class="function">hash\_algos</span>
-   <span class="function">hash\_init</span>
-   <span class="function">hash\_hmac</span>
-   <span class="function">hash\_hmac\_file</span>
-   <span class="function">openssl\_pbkdf2</span>

hash\_update\_file
==================

从文件向活跃的哈希运算上下文中填充数据

### 说明

<span class="type">bool</span> <span
class="methodname">hash\_update\_file</span> ( <span
class="methodparam"><span class="type">HashContext</span>
`$hcontext`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">resource</span> `$scontext`<span
class="initializer"> = **`NULL`**</span></span> \] )

### 参数

`hcontext`  
由 <span class="function">hash\_init</span> 函数返回的哈希运算上下文。

`filename`  
要进行哈希运算的文件路径，支持 fopen 封装器。

`scontext`  
由 <span class="function">stream\_context\_create</span>
函数返回的流上下文。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 7.2.0 | 接收参数从资源类型修改为 <span class="classname">HashContext</span> 对象类型。 |

### 参见

-   <span class="function">hash\_init</span>
-   <span class="function">hash\_update</span>
-   <span class="function">hash\_update\_stream</span>
-   <span class="function">hash\_final</span>
-   <span class="function">hash</span>
-   <span class="function">hash\_file</span>

hash\_update\_stream
====================

从打开的流向活跃的哈希运算上下文中填充数据

### 说明

<span class="type">int</span> <span
class="methodname">hash\_update\_stream</span> ( <span
class="methodparam"><span class="type">HashContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">resource</span> `$handle`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = -1</span></span> \] )

### 参数

`context`  
由 <span class="function">hash\_init</span> 函数返回的哈希运算上下文。

`handle`  
创建流的函数返回的打开的文件句柄。

`length`  
要从 `handle` 向活跃的哈希运算上下文中拷贝 的最大字符数。

### 返回值

从 `handle` 向哈希运算上下文中实际填充的字节数量。

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 7.2.0 | 接收参数从资源类型修改为 <span class="classname">HashContext</span> 对象类型。 |

### 范例

**示例 \#1 <span class="function">hash\_update\_stream</span> 例程**

``` php
<?php
$fp = tmpfile();
fwrite($fp, 'The quick brown fox jumped over the lazy dog.');
rewind($fp);

$ctx = hash_init('md5');
hash_update_stream($ctx, $fp);
echo hash_final($ctx);
?>
```

以上例程会输出：

    5c6ffbdd40d9556b73a21e63c3e0e904

### 参见

-   <span class="function">hash\_init</span>
-   <span class="function">hash\_update</span>
-   <span class="function">hash\_final</span>
-   <span class="function">hash</span>
-   <span class="function">hash\_file</span>

hash\_update
============

向活跃的哈希运算上下文中填充数据

### 说明

<span class="type">bool</span> <span
class="methodname">hash\_update</span> ( <span class="methodparam"><span
class="type">HashContext</span> `$context`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 参数

`context`  
由 <span class="function">hash\_init</span> 函数返回的哈希运算上下文。

`data`  
要向哈希摘要中追加的数据。

### 返回值

返回 **`TRUE`**。

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 7.2.0 | 接收参数从资源类型修改为 <span class="classname">HashContext</span> 对象类型。 |

### 参见

-   <span class="function">hash\_init</span>
-   <span class="function">hash\_update\_file</span>
-   <span class="function">hash\_update\_stream</span>
-   <span class="function">hash\_final</span>

hash
====

生成哈希值 （消息摘要）

### 说明

<span class="type">string</span> <span class="methodname">hash</span> (
<span class="methodparam"><span class="type">string</span>
`$algo`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$raw_output`<span
class="initializer"> = **`FALSE`**</span></span> \] )

### 参数

`algo`  
要使用的哈希算法，例如："md5"，"sha256"，"haval160,4" 等。

`data`  
要进行哈希运算的消息。

`raw_output`  
设置为 **`TRUE`** 输出原始二进制数据， 设置为 **`FALSE`** 输出小写 16
进制字符串。

### 返回值

如果 `raw_output` 设置为 **`TRUE`**，
则返回原始二进制数据表示的信息摘要， 否则返回 16
进制小写字符串格式表示的信息摘要。

### 更新日志

| 版本  | 说明                                                     |
|-------|----------------------------------------------------------|
| 5.4.0 | tiger 算法使用大端（big-endian）字节序。参见下面的示例。 |

### 范例

**示例 \#1 一个 <span class="function">hash</span> 例程**

``` php
<?php
echo hash('ripemd160', 'The quick brown fox jumped over the lazy dog.');
?>
```

以上例程会输出：

    ec457d0a974c48d5685a7efa03d137dc8bbde7e3

**示例 \#2 使用 PHP 5.4 或者更高版本计算 tiger 哈希值**

``` php
<?php
function old_tiger($data = "", $width=192, $rounds = 3) {
    return substr(
        implode(
            array_map(
                function ($h) {
                    return str_pad(bin2hex(strrev($h)), 16, "0");
                },
                str_split(hash("tiger192,$rounds", $data, true), 8)
            )
        ),
        0, 48-(192-$width)/4
    );
}
echo hash('tiger192,3', 'a-string'), PHP_EOL;
echo old_tiger('a-string'), PHP_EOL;
?>
```

以上例程在PHP 5.3中的输出：

    146a7492719b3564094efe7abbd40a7416fd900179d02773
    64359b7192746a14740ad4bb7afe4e097327d0790190fd16

以上例程在PHP 5.4中的输出：

    64359b7192746a14740ad4bb7afe4e097327d0790190fd16
    146a7492719b3564094efe7abbd40a7416fd900179d02773

### 参见

-   <span class="function">hash\_file</span>
-   <span class="function">hash\_hmac</span>
-   <span class="function">hash\_init</span>
-   <span class="function">md5</span>
-   <span class="function">sha1</span>

**目录**

-   [hash\_algos](/ref/hash.html#hash_algos) — 返回已注册的哈希算法列表
-   [hash\_copy](/ref/hash.html#hash_copy) — 拷贝哈希运算上下文
-   [hash\_equals](/ref/hash.html#hash_equals) —
    可防止时序攻击的字符串比较
-   [hash\_file](/ref/hash.html#hash_file) —
    使用给定文件的内容生成哈希值
-   [hash\_final](/ref/hash.html#hash_final) —
    结束增量哈希，并且返回摘要结果
-   [hash\_hkdf](/ref/hash.html#hash_hkdf) — Generate a HKDF key
    derivation of a supplied key input
-   [hash\_hmac\_algos](/ref/hash.html#hash_hmac_algos) — Return a list
    of registered hashing algorithms suitable for hash\_hmac
-   [hash\_hmac\_file](/ref/hash.html#hash_hmac_file) — 使用 HMAC
    方法和给定文件的内容生成带密钥的哈希值
-   [hash\_hmac](/ref/hash.html#hash_hmac) — 使用 HMAC
    方法生成带有密钥的哈希值
-   [hash\_init](/ref/hash.html#hash_init) — 初始化增量哈希运算上下文
-   [hash\_pbkdf2](/ref/hash.html#hash_pbkdf2) — 生成所提供密码的 PBKDF2
    密钥导出
-   [hash\_update\_file](/ref/hash.html#hash_update_file) —
    从文件向活跃的哈希运算上下文中填充数据
-   [hash\_update\_stream](/ref/hash.html#hash_update_stream) —
    从打开的流向活跃的哈希运算上下文中填充数据
-   [hash\_update](/ref/hash.html#hash_update) —
    向活跃的哈希运算上下文中填充数据
-   [hash](/ref/hash.html#hash) — 生成哈希值 （消息摘要）
