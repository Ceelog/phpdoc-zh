openssl\_cipher\_iv\_length
===========================

获取密码iv长度

### 说明

<span class="type">int</span> <span
class="methodname">openssl\_cipher\_iv\_length</span> ( <span
class="methodparam"><span class="type">string</span> `$method`</span> )

获取密码初始化向量(iv)长度。

### 参数

`method`  
密码的方法，更多值查看 <span
class="function">openssl\_get\_cipher\_methods</span> 函数。

### 返回值

成功，返回密码长度, 失败返回 **`FALSE`** .

### 错误／异常

当密码方法未知时，抛出一个**`E_WARNING`** 级的错误。

### 范例

**示例 \#1 <span class="function">openssl\_cipher\_iv\_length</span>
范例**

``` php
<?php
$method = 'AES-128-CBC';
$ivlen = openssl_cipher_iv_length($method);

echo $ivlen;
?>
```

以上例程的输出类似于：

    16

openssl\_csr\_export\_to\_file
==============================

将CSR导出到文件

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_csr\_export\_to\_file</span> ( <span
class="methodparam"><span class="type">mixed</span> `$csr`</span> ,
<span class="methodparam"><span class="type">string</span>
`$outfilename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$notext`<span class="initializer"> =
true</span></span> \] )

<span class="function">openssl\_csr\_export\_to\_file</span>
获取证书签名请求(`csr`) 并将之保存在以 `outfilename`
命名的PEM格式文件中。

### 参数

`csr`  
See <a href="/openssl/certparams.html" class="link">CSR parameters</a>
for a list of valid values.

`outfilename`  
输出文件的路径。

`notext`  
可选参数 `notext` 影响输出的冗余度。如果设为
**`FALSE`**，输出内容将包含附加的人类可读信息。`notext` 的缺省值为
**`TRUE`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 openssl\_csr\_export\_to\_file() 范例**

``` php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha384') );
openssl_pkey_export_to_file($private_key, 'example-priv.key');
// Along with the subject, the CSR contains the public key corresponding to the private key
openssl_csr_export_to_file($csr, 'example-csr.pem');
?>
```

### 参见

-   <span class="function">openssl\_csr\_export</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_sign</span>

openssl\_csr\_export
====================

将CSR作为字符串导出

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_csr\_export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$csr`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$out`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$notext`<span class="initializer"> =
true</span></span> \] )

<span class="function">openssl\_csr\_export</span>
获取证书签名请求(`csr`)并通过引用保存其 PEM 格式的字符串(`out`)。

### 参数

`csr`  
See <a href="/openssl/certparams.html" class="link">CSR parameters</a>
for a list of valid values.

`out`  
在成功时，该字符串将包含PEM编码的CSR.

`notext`  
可选参数 `notext` 影响输出的冗余度。如果设为
**`FALSE`**，输出内容将包含附加的人类可读信息。`notext` 的缺省值为
**`TRUE`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 openssl\_csr\_export() 范例**

``` php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$configargs = array(
    'digest_alg' => 'sha256WithRSAEncryption'
);
$csr = openssl_csr_new($subject, $private_key, $configargs);
openssl_csr_export($csr, $csr_string);
echo $csr_string;
?>
```

### 参见

-   <span class="function">openssl\_csr\_export\_to\_file</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_sign</span>

openssl\_csr\_get\_public\_key
==============================

返回CSR的公钥

### 说明

<span class="type">resource</span> <span
class="methodname">openssl\_csr\_get\_public\_key</span> ( <span
class="methodparam"><span class="type">mixed</span> `$csr`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$use_shortnames`<span class="initializer"> = true</span></span> \] )

<span class="function">openssl\_csr\_get\_public\_key</span>
从`csr`中提取公钥供其他功能使用。

### 参数

`csr`  
See <a href="/openssl/certparams.html" class="link">CSR parameters</a>
for a list of valid values.

`use_shortnames`  
**Warning**
该参数可以省略。

### 返回值

成功，返回一个私钥标识符，错误则返回FALSE.

### 范例

**示例 \#1 openssl\_csr\_get\_public\_key() example**

``` php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha256') );
$public_key = openssl_csr_get_public_key($csr);
$info = openssl_pkey_get_details($public_key);
echo $info['key'];
?>
```

### 参见

-   <span class="function">openssl\_csr\_get\_subject</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_pkey\_get\_details</span>
-   <span class="function">openssl\_pkey\_export\_to\_file</span>
-   <span class="function">openssl\_pkey\_export</span>

openssl\_csr\_get\_subject
==========================

返回CSR的主题

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_csr\_get\_subject</span> ( <span
class="methodparam"><span class="type">mixed</span> `$csr`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$use_shortnames`<span class="initializer"> = true</span></span> \] )

<span class="function">openssl\_csr\_get\_subject</span>
返回`csr`中专有名称信息的主题，其中包含了通用名称 (CN), 机构名称 (O),
国家名 (C) 等字段。

### 参数

`csr`  
See <a href="/openssl/certparams.html" class="link">CSR parameters</a>
for a list of valid values.

`use_shortnames`  
`shortnames` 控制着数据如何在数组中被索引 - 如果 `shortnames` 为
**`TRUE`** (默认) 将使用简称形式对字段进行索引，否则将使用全称形式 -
比如： CN 就是 commonName 的简称形式。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 openssl\_csr\_get\_subject() 范例**

``` php
<?php
$subject = array(
    "countryName" => "CA",
    "stateOrProvinceName" => "Alberta",
    "localityName" => "Calgary",
    "organizationName" => "XYZ Widgets Inc",
    "organizationalUnitName" => "PHP Documentation Team",
    "commonName" => "Wez Furlong",
    "emailAddress" => "wez@example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$configargs = array(
    'digest_alg' => 'sha512WithRSAEncryption'
);
$csr = openssl_csr_new($subject, $privkey, $configargs);
print_r(openssl_csr_get_subject($csr));
?>
```

以上例程的输出类似于：

    Array
    (
        [C] => CA
        [ST] => Alberta
        [L] => Calgary
        [O] => XYZ Widgets Inc
        [OU] => PHP Documentation Team
        [CN] => Wez Furlong
        [emailAddress] => wez@example.com
    )

### 参见

-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_get\_public\_key</span>
-   <span class="function">openssl\_x509\_parse</span>

openssl\_csr\_new
=================

生成一个 CSR

### 说明

<span class="type">mixed</span> <span
class="methodname">openssl\_csr\_new</span> ( <span
class="methodparam"><span class="type">array</span> `$dn`</span> , <span
class="methodparam"><span class="type">resource</span>
`&$privkey`</span> \[, <span class="methodparam"><span
class="type">array</span> `$configargs`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$extraattribs`</span> \]\] )

<span class="function">openssl\_csr\_new</span>
根据`dn`提供的信息生成新的CSR（证书签名请求）。

> **Note**: <span class="simpara"> 必须安装有效的 `openssl.cnf`
> 以保证此函数正确运行。参考有关<a href="/openssl/setup.html#安装" class="link">安装</a>的说明以获得更多信息。
> </span>

### 参数

`dn`  
在证书中使用的专有名称或主题字段。

`privkey`  
`privkey` 应该被设置为由<span
class="function">openssl\_pkey\_new</span>函数预先生成(或者以其他方式从openssl\_pkey函数集中获得)的私钥。该密钥的相应公共部分将用于签署CSR.

`configargs`  
默认的， 是通过你系统里的*openssl.conf*配置来初始化请求；
您可以通过设置`configargs`的*config\_section\_section*项来指定配置文件部分。
您还可以通过将config键的值设置为您想要使用的文件路径来指定另一个openssl配置文件。如果在`configargs`中存在下列键，它们的行为就像在*openssl.conf*中一样。如下表所示：

| `configargs` 键      | type                              | 等同于 *openssl.conf* | 描述                                                                                                                                                                                      |
|----------------------|-----------------------------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digest\_alg          | <span class="type">string</span>  | default\_md           | 摘要算法或签名哈希算法，通常是 <span class="function">openssl\_get\_md\_methods</span> 之一。                                                                                             |
| x509\_extensions     | <span class="type">string</span>  | x509\_extensions      | 选择在创建x509证书时应该使用哪些扩展                                                                                                                                                      |
| req\_extensions      | <span class="type">string</span>  | req\_extensions       | 创建CSR时，选择使用哪个扩展                                                                                                                                                               |
| private\_key\_bits   | <span class="type">integer</span> | default\_bits         | 指定应该使用多少位来生成私钥                                                                                                                                                              |
| private\_key\_type   | <span class="type">integer</span> | none                  | 选择在创建CSR时应该使用哪些扩展。可选值有 **`OPENSSL_KEYTYPE_DSA`**, **`OPENSSL_KEYTYPE_DH`**, **`OPENSSL_KEYTYPE_RSA`** 或 **`OPENSSL_KEYTYPE_EC`**. 默认值是 **`OPENSSL_KEYTYPE_RSA`**. |
| encrypt\_key         | <span class="type">boolean</span> | encrypt\_key          | 是否应该对导出的密钥（带有密码短语）进行加密?                                                                                                                                             |
| encrypt\_key\_cipher | <span class="type">integer</span> | none                  | <a href="/openssl/constants.html#Ciphers" class="link">cipher constants</a>常量之一。                                                                                                     |
| curve\_name          | <span class="type">string</span>  | none                  | 要求PHP7.1+, <span class="function">openssl\_get\_curve\_names</span>之一。                                                                                                               |
| config               | <span class="type">string</span>  | N/A                   | 自定义 openssl.conf 文件的路径。                                                                                                                                                          |

`extraattribs`  
`extraattribs` 用于为CSR指定额外的配置选项。`dn` 和 `extraattribs`
都是关联数组它们的键被转换成OIDs，并应用到请求的相关部分。

### 返回值

成功，返回CSR 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 创建一个自签名的证书**

``` php
<?php
// for SSL server certificates the commonName is the domain name to be secured
// for S/MIME email certificates the commonName is the owner of the email address
// location and identification fields refer to the owner of domain or email subject to be secured
$dn = array(
    "countryName" => "GB",
    "stateOrProvinceName" => "Somerset",
    "localityName" => "Glastonbury",
    "organizationName" => "The Brain Room Limited",
    "organizationalUnitName" => "PHP Documentation Team",
    "commonName" => "Wez Furlong",
    "emailAddress" => "wez@example.com"
);

// Generate a new private (and public) key pair
$privkey = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));

// Generate a certificate signing request
$csr = openssl_csr_new($dn, $privkey, array('digest_alg' => 'sha256'));

// Generate a self-signed cert, valid for 365 days
$x509 = openssl_csr_sign($csr, null, $privkey, $days=365, array('digest_alg' => 'sha256'));

// Save your private key, CSR and self-signed cert for later use
openssl_csr_export($csr, $csrout) and var_dump($csrout);
openssl_x509_export($x509, $certout) and var_dump($certout);
openssl_pkey_export($privkey, $pkeyout, "mypassword") and var_dump($pkeyout);

// Show any errors that occurred here
while (($e = openssl_error_string()) !== false) {
    echo $e . "\n";
}
?>
```

**示例 \#2 在PHP 7.1+版本中创建一个自签名的ECC证书**

``` php
<?php
$subject = array(
    "commonName" => "docs.php.net",
);

// Generate a new private (and public) key pair
$private_key = openssl_pkey_new(array(
    "private_key_type" => OPENSSL_KEYTYPE_EC,
    "curve_name" => 'prime256v1',
));

// Generate a certificate signing request
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha384'));

// Generate self-signed EC cert
$x509 = openssl_csr_sign($csr, null, $private_key, $days=365, array('digest_alg' => 'sha384'));
openssl_x509_export_to_file($x509, 'ecc-cert.pem');
openssl_pkey_export_to_file($private_key, 'ecc-private.key');
?>
```

### 参见

-   <span class="function">openssl\_csr\_sign</span>

openssl\_csr\_sign
==================

用另一个证书签署 CSR (或者本身) 并且生成一个证书

### 说明

<span class="type">resource</span> <span
class="methodname">openssl\_csr\_sign</span> ( <span
class="methodparam"><span class="type">mixed</span> `$csr`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$cacert`</span> , <span class="methodparam"><span
class="type">mixed</span> `$priv_key`</span> , <span
class="methodparam"><span class="type">int</span> `$days`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$configargs`</span> \[, <span class="methodparam"><span
class="type">int</span> `$serial`<span class="initializer"> =
0</span></span> \]\] )

<span class="function">openssl\_csr\_sign</span> 从给定的 CSR
生成一个x509证书资源

> **Note**: <span class="simpara"> 必须安装有效的 `openssl.cnf`
> 以保证此函数正确运行。参考有关<a href="/openssl/setup.html#安装" class="link">安装</a>的说明以获得更多信息。
> </span>

### 参数

`csr`  
由<span class="function">openssl\_csr\_new</span>函数生成的CSR.
也可以是由类似`file://path/to/csr`格式指定的指向PEM编码的CSR路径，或者是一个由<span
class="function">openssl\_csr\_export</span>函数生成的字符串。

`cacert`  
生成的证书将由`cacert`签名。 如果`cacert` 为 **`NULL`**,
生成的证书将是自签名证书。

`priv_key`  
`priv_key`是`cacert`证书对应的私钥。

`days`  
`days` 指定生成的证书在几天内有效的时间长度。

`configargs`  
你可以通过`configargs`确定CSR签名。 查看<span
class="function">openssl\_csr\_new</span> 方法获取
`configargs`的更多相关信息。

`serial`  
可选的发行证书编号。如果没有指定默认值为0.

### 返回值

成功，返回一个 x509 证书资源，失败则返回 **`FALSE`** .

### 范例

**示例 \#1 <span class="function">openssl\_csr\_sign</span> example -
signing a CSR (how to implement your own CA)**

``` php
<?php
// Let's assume that this script is set to receive a CSR that has
// been pasted into a textarea from another page
$csrdata = $_POST["CSR"];

// We will sign the request using our own "certificate authority"
// certificate.  You can use any certificate to sign another, but
// the process is worthless unless the signing certificate is trusted
// by the software/users that will deal with the newly signed certificate

// We need our CA cert and its private key
$cacert = "file://path/to/ca.crt";
$privkey = array("file://path/to/ca.key", "your_ca_key_passphrase");

$usercert = openssl_csr_sign($csrdata, $cacert, $privkey, 365, array('digest_alg'=>'sha256') );

// Now display the generated certificate so that the user can
// copy and paste it into their local configuration (such as a file
// to hold the certificate for their SSL server)
openssl_x509_export($usercert, $certout);
echo $certout;

// Show any errors that occurred here
while (($e = openssl_error_string()) !== false) {
    echo $e . "\n";
}
?>
```

openssl\_decrypt
================

解密数据

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_decrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$method`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$iv`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$tag`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$aad`<span
class="initializer"> = ""</span></span> \]\]\]\] )

采用原始或base64编码的字符串，并使用给定的方法和密钥对其进行解密。

### 参数

`data`  
将被解密的密文。

`method`  
加密算法，使用<span
class="function">openssl\_get\_cipher\_methods</span>函数获取可用的加密算法列表。

`key`  
密钥。

`options`  
`options` can be one of **`OPENSSL_RAW_DATA`**,
**`OPENSSL_ZERO_PADDING`**.

`iv`  
非空的初始化向量。

`tag`  
AEAD密码模式中的身份验证标签。
如果是错误的，验证失败，函数返回**`FALSE`**.

`aad`  
额外的认证数据。

### 返回值

The decrypted string on success 或者在失败时返回 **`FALSE`**.

### 错误／异常

如果通过`method`参数传递的是一个未知的加密算法，将会抛出一个
**`E_WARNING`** 等级的错误。

如果通过`iv`参数传递的是一个空值，将会抛出一个 **`E_WARNING`**
等级的错误。

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 5.3.3 | 添加 `iv` 参数。                   |
| 5.4.0 | 将 `raw_output` 更改至 `options`。 |
| 7.1.0 | 添加了 `tag` 和 `aad` 参数。       |

### 参见

-   <span class="function">openssl\_encrypt</span>

openssl\_dh\_compute\_key
=========================

计算远程DH密钥(公钥)和本地DH密钥的共享密钥

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_dh\_compute\_key</span> ( <span
class="methodparam"><span class="type">string</span> `$pub_key`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$dh_key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`pub_key`  
公钥

`dh_key`  
DH 密钥

### 返回值

成功，返回计算的密钥， 或者在失败时返回 **`FALSE`**.

openssl\_digest
===============

计算摘要

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_digest</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$method`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$raw_output`<span class="initializer"> =
false</span></span> \] )

使用给定的方法计算给定数据的摘要哈希值，并返回一个原始的或16进制编码的字符串。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`data`  
给定的数据。

`method`  
要使用的摘要方法，比如 "sha256", 查看 <span
class="function">openssl\_get\_md\_methods</span>
函数获取更多可用的摘要方法。

`raw_output`  
为 **`TRUE`** 时将会返回原始输出数据，否则返回值将会是16进制。

### 返回值

成功，返回摘要哈希值， 或者在失败时返回 **`FALSE`**.

### 错误／异常

如果通过`method`参数传递的是一个未知的摘要算法，将会抛出一个**`E_WARNING`**
级的错误。

### 参见

-   <span class="function">openssl\_get\_md\_methods</span>

openssl\_encrypt
================

加密数据

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_encrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$method`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$iv`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `&$tag`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$aad`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag_length`<span
class="initializer"> = 16</span></span> \]\]\]\]\] )

以指定的方式和 key 加密数据，返回原始或 base64 编码后的字符串。

### 参数

`data`  
待加密的明文信息数据。

`method`  
密码学方式。<span class="function">openssl\_get\_cipher\_methods</span>
可获取有效密码方式列表。

`key`  
key。

`options`  
`options` 是以下标记的按位或： **`OPENSSL_RAW_DATA`** 、
**`OPENSSL_ZERO_PADDING`**。

`iv`  
非 NULL 的初始化向量。

`tag`  
使用 AEAD 密码模式（GCM 或 CCM）时传引用的验证标签。

`aad`  
附加的验证数据。

`tag_length`  
验证 `tag` 的长度。GCM 模式时，它的范围是 4 到 16。

### 返回值

成功时返回加密后的字符串， 或者在失败时返回 **`FALSE`**。

### 错误／异常

`method` 传入未知算法时，产生 **`E_WARNING`** 级别的错误。

`iv` 传入空字符串时产生 **`E_WARNING`** 级别的错误。

### 更新日志

| 版本  | 说明                                   |
|-------|----------------------------------------|
| 5.3.3 | 增加 `iv` 参数。                       |
| 5.4.0 | `raw_output` 改到 `options`。          |
| 7.1.0 | 增加了 `tag`、`aad`、`tag_length` 参数 |

### 范例

**示例 \#1 PHP 7.1+ 下 GCM 模式的 AES 认证加密例子**

``` php
<?php
//$key should have been previously generated in a cryptographically safe way, like openssl_random_pseudo_bytes
$plaintext = "message to be encrypted";
$cipher = "aes-128-gcm";
if (in_array($cipher, openssl_get_cipher_methods()))
{
    $ivlen = openssl_cipher_iv_length($cipher);
    $iv = openssl_random_pseudo_bytes($ivlen);
    $ciphertext = openssl_encrypt($plaintext, $cipher, $key, $options=0, $iv, $tag);
    //store $cipher, $iv, and $tag for decryption later
    $original_plaintext = openssl_decrypt($ciphertext, $cipher, $key, $options=0, $iv, $tag);
    echo $original_plaintext."\n";
}
?>
```

**示例 \#2 PHP 5.6+ 的 AES 认证加密例子**

``` php
<?php
//$key previously generated safely, ie: openssl_random_pseudo_bytes
$plaintext = "message to be encrypted";
$ivlen = openssl_cipher_iv_length($cipher="AES-128-CBC");
$iv = openssl_random_pseudo_bytes($ivlen);
$ciphertext_raw = openssl_encrypt($plaintext, $cipher, $key, $options=OPENSSL_RAW_DATA, $iv);
$hmac = hash_hmac('sha256', $ciphertext_raw, $key, $as_binary=true);
$ciphertext = base64_encode( $iv.$hmac.$ciphertext_raw );

//decrypt later....
$c = base64_decode($ciphertext);
$ivlen = openssl_cipher_iv_length($cipher="AES-128-CBC");
$iv = substr($c, 0, $ivlen);
$hmac = substr($c, $ivlen, $sha2len=32);
$ciphertext_raw = substr($c, $ivlen+$sha2len);
$original_plaintext = openssl_decrypt($ciphertext_raw, $cipher, $key, $options=OPENSSL_RAW_DATA, $iv);
$calcmac = hash_hmac('sha256', $ciphertext_raw, $key, $as_binary=true);
if (hash_equals($hmac, $calcmac))//PHP 5.6+ timing attack safe comparison
{
    echo $original_plaintext."\n";
}
?>
```

### 参见

-   <span class="function">openssl\_decrypt</span>

openssl\_error\_string
======================

返回 openSSL 错误消息

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_error\_string</span> ( <span
class="methodparam">void</span> )

<span class="function">openssl\_error\_string</span>
从openSSL库返回最后一个错误。错误消息已被队列化，因此这个函数可以多次调用用来收集所有的信息。最后一个错误将是最近的一个。

### 返回值

成功，返回错误信息字符串，如果没有任何错误信息则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">openssl\_error\_string</span>
example**

``` php
<?php
// lets assume you just called an openssl function that failed
while ($msg = openssl_error_string())
    echo $msg . "<br />\n";
?>
```

openssl\_free\_key
==================

释放密钥资源

### 说明

<span class="type">void</span> <span
class="methodname">openssl\_free\_key</span> ( <span
class="methodparam"><span class="type">resource</span>
`$key_identifier`</span> )

<span class="function">openssl\_free\_key</span> 从内存中释放和指定的
`key_identifier`相关联的密钥。

### 参数

`key_identifier`  

### 返回值

没有返回值。

openssl\_get\_cert\_locations
=============================

检索可用的证书位置

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_get\_cert\_locations</span> ( <span
class="methodparam">void</span> )

<span class="function">openssl\_get\_cert\_locations</span>
返回一个数组，其中包含要搜索SSL证书的可用证书位置的信息。

### 参数

此函数没有参数。

### 返回值

返回一个带有可用证书位置信息的数组。

### 范例

**示例 \#1 <span class="function">openssl\_get\_cert\_locations</span>
范例**

``` php
<?php
var_dump(openssl_get_cert_locations());
?>
```

以上例程会输出：

    array(8) {
      ["default_cert_file"]=>
      string(21) "/usr/lib/ssl/cert.pem"
      ["default_cert_file_env"]=>
      string(13) "SSL_CERT_FILE"
      ["default_cert_dir"]=>
      string(18) "/usr/lib/ssl/certs"
      ["default_cert_dir_env"]=>
      string(12) "SSL_CERT_DIR"
      ["default_private_dir"]=>
      string(20) "/usr/lib/ssl/private"
      ["default_default_cert_area"]=>
      string(12) "/usr/lib/ssl"
      ["ini_cafile"]=>
      string(0) ""
      ["ini_capath"]=>
      string(0) ""
    }

openssl\_get\_cipher\_methods
=============================

获取可用的加密算法

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_get\_cipher\_methods</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$aliases`<span
class="initializer"> = false</span></span> \] )

获取可用的加密算法的列表。

### 参数

`aliases`  
如果密码别名应该包含在返回的<span class="type">array</span>中，则设置为
**`TRUE`**.

### 返回值

一个包含可用加密算法的<span class="type">array</span>。

### 范例

**示例 \#1 <span class="function">openssl\_get\_cipher\_methods</span>
example**

展示了哪些加密算法能被找到，哪些别名可用。

``` php
<?php
$ciphers             = openssl_get_cipher_methods();
$ciphers_and_aliases = openssl_get_cipher_methods(true);
$cipher_aliases      = array_diff($ciphers_and_aliases, $ciphers);

//ECB mode should be avoided
$ciphers = array_filter( $ciphers, function($n) { return stripos($n,"ecb")===FALSE; } );

//At least as early as Aug 2016, Openssl declared the following weak: RC2, RC4, DES, 3DES, MD5 based
$ciphers = array_filter( $ciphers, function($c) { return stripos($c,"des")===FALSE; } );
$ciphers = array_filter( $ciphers, function($c) { return stripos($c,"rc2")===FALSE; } );
$ciphers = array_filter( $ciphers, function($c) { return stripos($c,"rc4")===FALSE; } );
$ciphers = array_filter( $ciphers, function($c) { return stripos($c,"md5")===FALSE; } );
$cipher_aliases = array_filter($cipher_aliases,function($c) { return stripos($c,"des")===FALSE; } );
$cipher_aliases = array_filter($cipher_aliases,function($c) { return stripos($c,"rc2")===FALSE; } );

print_r($ciphers);
print_r($cipher_aliases);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => AES-128-CBC
        [1] => AES-128-CFB
        [2] => AES-128-CFB1
        [3] => AES-128-CFB8
        [5] => AES-128-OFB
        [6] => AES-192-CBC
        [7] => AES-192-CFB
        [8] => AES-192-CFB1
        [9] => AES-192-CFB8
        [11] => AES-192-OFB
        [12] => AES-256-CBC
        [13] => AES-256-CFB
        [14] => AES-256-CFB1
        [15] => AES-256-CFB8
        [17] => AES-256-OFB
        [18] => BF-CBC
        [19] => BF-CFB
        [21] => BF-OFB
        [22] => CAST5-CBC
        [23] => CAST5-CFB
        [25] => CAST5-OFB
        [41] => IDEA-CBC
        [42] => IDEA-CFB
        [44] => IDEA-OFB
        [53] => aes-128-cbc
        [54] => aes-128-cfb
        [55] => aes-128-cfb1
        [56] => aes-128-cfb8
        [58] => aes-128-ofb
        [59] => aes-192-cbc
        [60] => aes-192-cfb
        [61] => aes-192-cfb1
        [62] => aes-192-cfb8
        [64] => aes-192-ofb
        [65] => aes-256-cbc
        [66] => aes-256-cfb
        [67] => aes-256-cfb1
        [68] => aes-256-cfb8
        [70] => aes-256-ofb
        [71] => bf-cbc
        [72] => bf-cfb
        [74] => bf-ofb
        [75] => cast5-cbc
        [76] => cast5-cfb
        [78] => cast5-ofb
        [94] => idea-cbc
        [95] => idea-cfb
        [97] => idea-ofb
    )
    Array
    (
        [18] => AES128
        [19] => AES192
        [20] => AES256
        [21] => BF
        [26] => CAST
        [27] => CAST-cbc
        [50] => IDEA
        [82] => aes128
        [83] => aes192
        [84] => aes256
        [85] => bf
        [90] => blowfish
        [91] => cast
        [92] => cast-cbc
        [115] => idea
    )

### 参见

-   <span class="function">openssl\_get\_md\_methods</span>

openssl\_get\_curve\_names
==========================

获得ECC的可用曲线名称列表

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_get\_curve\_names</span> ( <span
class="methodparam">void</span> )

获取用于公钥/私钥操作的椭圆曲线密码（ECC）中可用曲线名称的列表。两个最广泛的标准化/支持的曲线是*prime256v1*
(NIST P-256) 和 *secp384r1* (NIST P-384).

| AES Symmetric Keysize (Bits) | RSA and DSA Keysize (Bits) | ECC Keysize (Bits) |
|------------------------------|----------------------------|--------------------|
| 80                           | 1024                       | 160                |
| 112                          | 2048                       | 224                |
| 128                          | 3072                       | 256                |
| 192                          | 7680                       | 384                |
| 256                          | 15360                      | 512                |

<a href="http://dx.doi.org/10.6028/NIST.SP.800-57pt1r4" class="link external">» NIST 推荐使用的 ECC 曲线最少为 256 位</a>.

### 参数

此函数没有参数。

### 返回值

一个包含可用曲线名称的<span class="type">数组</span>。

### 范例

**示例 \#1 <span class="function">openssl\_get\_curve\_names</span>
范例**

``` php
<?php
$curve_names = openssl_get_curve_names();
print_r($curve_names);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => secp112r1
        [1] => secp112r2
        [2] => secp128r1
        [3] => secp128r2
        [4] => secp160k1
        [5] => secp160r1
        [6] => secp160r2
        [7] => secp192k1
        [8] => secp224k1
        [9] => secp224r1
        [10] => secp256k1
        [11] => secp384r1
        [12] => secp521r1
        [13] => prime192v1
        [14] => prime192v2
        [15] => prime192v3
        [16] => prime239v1
        [17] => prime239v2
        [18] => prime239v3
        [19] => prime256v1
        [20] => sect113r1
        [21] => sect113r2
        [22] => sect131r1
        [23] => sect131r2
        [24] => sect163k1
        [25] => sect163r1
        [26] => sect163r2
        [27] => sect193r1
        [28] => sect193r2
        [29] => sect233k1
        [30] => sect233r1
        [31] => sect239k1
        [32] => sect283k1
        [33] => sect283r1
        [34] => sect409k1
        [35] => sect409r1
        [36] => sect571k1
        [37] => sect571r1
        [38] => c2pnb163v1
        [39] => c2pnb163v2
        [40] => c2pnb163v3
        [41] => c2pnb176v1
        [42] => c2tnb191v1
        [43] => c2tnb191v2
        [44] => c2tnb191v3
        [45] => c2pnb208w1
        [46] => c2tnb239v1
        [47] => c2tnb239v2
        [48] => c2tnb239v3
        [49] => c2pnb272w1
        [50] => c2pnb304w1
        [51] => c2tnb359v1
        [52] => c2pnb368w1
        [53] => c2tnb431r1
        [54] => wap-wsg-idm-ecid-wtls1
        [55] => wap-wsg-idm-ecid-wtls3
        [56] => wap-wsg-idm-ecid-wtls4
        [57] => wap-wsg-idm-ecid-wtls5
        [58] => wap-wsg-idm-ecid-wtls6
        [59] => wap-wsg-idm-ecid-wtls7
        [60] => wap-wsg-idm-ecid-wtls8
        [61] => wap-wsg-idm-ecid-wtls9
        [62] => wap-wsg-idm-ecid-wtls10
        [63] => wap-wsg-idm-ecid-wtls11
        [64] => wap-wsg-idm-ecid-wtls12
        [65] => Oakley-EC2N-3
        [66] => Oakley-EC2N-4
        [67] => brainpoolP160r1
        [68] => brainpoolP160t1
        [69] => brainpoolP192r1
        [70] => brainpoolP192t1
        [71] => brainpoolP224r1
        [72] => brainpoolP224t1
        [73] => brainpoolP256r1
        [74] => brainpoolP256t1
        [75] => brainpoolP320r1
        [76] => brainpoolP320t1
        [77] => brainpoolP384r1
        [78] => brainpoolP384t1
        [79] => brainpoolP512r1
        [80] => brainpoolP512t1
    )

openssl\_get\_md\_methods
=========================

获取可用的摘要算法

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_get\_md\_methods</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$aliases`<span
class="initializer"> = false</span></span> \] )

获取可用的摘要算法列表

### 参数

`aliases`  
设置为 **`TRUE`** 时，返回的<span
class="type">array</span>中将会包含摘要的别名.

### 返回值

含有可用摘要算法的<span class="type">数组</span>

### 范例

**示例 \#1 <span class="function">openssl\_get\_md\_methods</span>
范例：**

显示了可用的摘要，以及哪些别名可能是可用的。

``` php
<?php
$digests             = openssl_get_md_methods();
$digests_and_aliases = openssl_get_md_methods(true);
$digest_aliases      = array_diff($digests_and_aliases, $digests);

print_r($digests);

print_r($digest_aliases);

?>
```

以上例程的输出类似于：

    Array
    (
        [0] => DSA
        [1] => DSA-SHA
        [2] => MD2
        [3] => MD4
        [4] => MD5
        [5] => RIPEMD160
        [6] => SHA
        [7] => SHA1
        [8] => SHA224
        [9] => SHA256
        [10] => SHA384
        [11] => SHA512
        [12] => dsaEncryption
        [13] => dsaWithSHA
        [14] => ecdsa-with-SHA1
        [15] => md2
        [16] => md4
        [17] => md5
        [18] => ripemd160
        [19] => sha
        [20] => sha1
        [21] => sha224
        [22] => sha256
        [23] => sha384
        [24] => sha512
    )
    Array
    (
        [2] => DSA-SHA1
        [3] => DSA-SHA1-old
        [4] => DSS1
        [9] => RSA-MD2
        [10] => RSA-MD4
        [11] => RSA-MD5
        [12] => RSA-RIPEMD160
        [13] => RSA-SHA
        [14] => RSA-SHA1
        [15] => RSA-SHA1-2
        [16] => RSA-SHA224
        [17] => RSA-SHA256
        [18] => RSA-SHA384
        [19] => RSA-SHA512
        [28] => dsaWithSHA1
        [29] => dss1
        [32] => md2WithRSAEncryption
        [34] => md4WithRSAEncryption
        [36] => md5WithRSAEncryption
        [37] => ripemd
        [39] => ripemd160WithRSA
        [40] => rmd160
        [43] => sha1WithRSAEncryption
        [45] => sha224WithRSAEncryption
        [47] => sha256WithRSAEncryption
        [49] => sha384WithRSAEncryption
        [51] => sha512WithRSAEncryption
        [52] => shaWithRSAEncryption
        [53] => ssl2-md5
        [54] => ssl3-md5
        [55] => ssl3-sha1
    )

### 参见

-   <span class="function">openssl\_digest</span>
-   <span class="function">openssl\_get\_cipher\_methods</span>

openssl\_get\_privatekey
========================

别名 <span class="function">openssl\_pkey\_get\_private</span>

### 说明

此函数是该函数的别名： <span
class="function">openssl\_pkey\_get\_private</span>.

openssl\_get\_publickey
=======================

别名 <span class="function">openssl\_pkey\_get\_public</span>

### 说明

此函数是该函数的别名： <span
class="function">openssl\_pkey\_get\_public</span>.

openssl\_open
=============

打开密封的数据

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_open</span> ( <span
class="methodparam"><span class="type">string</span>
`$sealed_data`</span> , <span class="methodparam"><span
class="type">string</span> `&$open_data`</span> , <span
class="methodparam"><span class="type">string</span> `$env_key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$priv_key_id`</span> \[, <span class="methodparam"><span
class="type">string</span> `$method`<span class="initializer"> =
"RC4"</span></span> \[, <span class="methodparam"><span
class="type">string</span> `&$iv`</span> \]\] )

<span class="function">openssl\_open</span>
使用与密钥标识符`priv_key_id`和信封密钥`env_key`相关联的私钥打开 (解密)
`sealed_data` 数据, 使用解密后的数据填充`open_data`。
当数据被密封时，就生成了信封密钥且只能由一个特定的私钥使用。更多信息参见
<span class="function">openssl\_seal</span> 。

### 参数

`sealed_data`  

`open_data`  
如果调用成功，则在这个参数中返回打开的数据。

`env_key`  

`priv_key_id`  

`method`  
加解密算法。

`iv`  
初始化向量。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 7.0.0 | 添加了 `iv` 参数     |
| 5.3.0 | 添加了 `method` 参数 |

### 范例

**示例 \#1 <span class="function">openssl\_open</span> 范例**

``` php
<?php
// $sealed and $env_key are assumed to contain the sealed data
// and our envelope key, both given to us by the sealer.

// fetch private key from file and ready it
$fp = fopen("/src/openssl-0.9.6/demos/sign/key.pem", "r");
$priv_key = fread($fp, 8192);
fclose($fp);
$pkeyid = openssl_get_privatekey($priv_key);

// decrypt the data and store it in $open
if (openssl_open($sealed, $open, $env_key, $pkeyid)) {
    echo "here is the opened data: ", $open;
} else {
    echo "failed to open data";
}

// free the private key from memory
openssl_free_key($pkeyid);
?>
```

### 参见

-   <span class="function">openssl\_seal</span>

openssl\_pbkdf2
===============

生成一个 PKCS5 v2 PBKDF2 字符串

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_pbkdf2</span> ( <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">string</span>
`$salt`</span> , <span class="methodparam"><span class="type">int</span>
`$key_length`</span> , <span class="methodparam"><span
class="type">int</span> `$iterations`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$digest_algorithm`<span class="initializer"> = "sha1"</span></span> \]
)

<span class="function">openssl\_pbkdf2</span> 计算 PBKDF2
(Password-Based Key Derivation Function 2), 在PKCS5
v2中定义的一个密钥的推导函数.

### 参数

`password`  
派生密钥所生成的密码。

`salt`  
PBKDF2 推荐一个不少于64位(8字节)的密码盐值。

`key_length`  
希望输出密钥的长度。

`iterations`  
需要的迭代次数
<a href="https://pages.nist.gov/800-63-3/sp800-63b.html#sec5" class="link external">» NIST 建议至少10,000次</a>.

`digest_algorithm`  
在<span
class="function">openssl\_get\_md\_methods</span>中可选的散列或摘要算法.默认是
SHA-1.

### 返回值

成功，返回原始二进制字符串 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 openssl\_pbkdf2() 范例**

``` php
<?php
$password = 'yOuR-pAs5w0rd-hERe';
$salt = openssl_random_pseudo_bytes(12);
$keyLength = 40;
$iterations = 10000;
$generated_key = openssl_pbkdf2($password, $salt, $keyLength, $iterations, 'sha256');
echo bin2hex($generated_key)."\n";
echo base64_encode($generated_key)."\n";
?>
```

### 参见

-   <span class="function">hash\_pbkdf2</span>
-   <span class="function">openssl\_get\_md\_methods</span>

openssl\_pkcs12\_export\_to\_file
=================================

输出一个 PKCS\#12 兼容的证书存储文件

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs12\_export\_to\_file</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">mixed</span> `$priv_key`</span> , <span
class="methodparam"><span class="type">string</span> `$pass`</span> \[,
<span class="methodparam"><span class="type">array</span> `$args`</span>
\] )

<span class="function">openssl\_pkcs12\_export\_to\_file</span> 函数以
PKCS\#12 格式将 `x509` 保存至文件名为 `filename` 的文件中。

### 参数

`x509`  
参见<a href="/openssl/certparams.html" class="link">密钥／证书参数</a>以获取有效值列表。

`filename`  
输出文件的路径。

`priv_key`  
PKCS\#12文件的私钥部分。 参见
<a href="/openssl/certparams.html" class="link">公/私钥参数</a>
获取可用值的列表。

`pass`  
用于解锁 PKCS\#12 文件的加密密码。

`args`  
可选数组，其他主键将被忽略。

| Key              | 说明                                            |
|------------------|-------------------------------------------------|
| *"extracerts"*   | PKCS\#12 文件中包含的额外证书或单个证书的数组。 |
| *"friendlyname"* | 被证书和密钥使用的字符串                        |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_pkcs12\_export
=======================

将 PKCS\#12 兼容证书存储文件导出到变量

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs12\_export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$out`</span> , <span class="methodparam"><span
class="type">mixed</span> `$priv_key`</span> , <span
class="methodparam"><span class="type">string</span> `$pass`</span> \[,
<span class="methodparam"><span class="type">array</span> `$args`</span>
\] )

<span class="function">openssl\_pkcs12\_export</span> 以 PKCS\#12
文件格式 将 `x509` 导入到以`out`命名类型为字符串的变量中。

### 参数

`x509`  
参见<a href="/openssl/certparams.html" class="link">密钥／证书参数</a>以获取有效值列表。

`out`  
成功，该字符串将为 PKCS\#12 格式。

`priv_key`  
PKCS\#12 文件的私钥部分file， 参见
<a href="/openssl/certparams.html" class="link">公/私钥参数</a>
获取更多可用列表。

`pass`  
用来解锁 PKCS\#12 文件的解密密码。

`args`  
可选数组，其他主键将被忽略。

| Key              | 说明                                            |
|------------------|-------------------------------------------------|
| *"extracerts"*   | PKCS\#12 文件中包含的额外证书或单个证书的数组。 |
| *"friendlyname"* | 被证书和密钥使用的字符串                        |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_pkcs12\_read
=====================

将 PKCS\#12 证书存储区解析到数组中

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs12\_read</span> ( <span
class="methodparam"><span class="type">string</span> `$pkcs12`</span> ,
<span class="methodparam"><span class="type">array</span>
`&$certs`</span> , <span class="methodparam"><span
class="type">string</span> `$pass`</span> )

<span class="function">openssl\_pkcs12\_read</span>
将`pkcs12`提供的PKCS\#12证书存储区解析到以`certs`命名的变量中。

### 参数

`pkcs12`  
证书存储内容，而不是它的文件名。

`certs`  
成功，将保存证书存储数据

`pass`  
用来解锁 PKCS\#12 文件的解密密码

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">openssl\_pkcs12\_read</span> 范例**

``` php
<?php
if (!$cert_store = file_get_contents("/certs/file.p12")) {
    echo "Error: Unable to read the cert file\n";
    exit;
}

if (openssl_pkcs12_read($cert_store, $cert_info, "my_secret_pass")) {
    echo "Certificate Information\n";
    print_r($cert_info);
} else {
    echo "Error: Unable to read the cert store.\n";
    exit;
}
?>
```

openssl\_pkcs7\_decrypt
=======================

解密一个 S/MIME 加密的消息

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs7\_decrypt</span> ( <span
class="methodparam"><span class="type">string</span>
`$infilename`</span> , <span class="methodparam"><span
class="type">string</span> `$outfilename`</span> , <span
class="methodparam"><span class="type">mixed</span> `$recipcert`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$recipkey`</span> \] )

使用由 `recipcert` 和 `recipkey` 指定的证书和与之关联的私钥解密
`infilename` 文件中包含的 S/MIME 加密消息

### 参数

`infilename`  

`outfilename`  
解密的消息将被存入的文件中，以`outfilename`命名。

`recipcert`  

`recipkey`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">openssl\_pkcs7\_decrypt</span> 范例**

``` php
<?php
// $cert and $key are assumed to contain your personal certificate and private
// key pair, and that you are the recipient of an S/MIME message
$infilename = "encrypted.msg";  // this file holds your encrypted message
$outfilename = "decrypted.msg"; // make sure you can write to this file

if (openssl_pkcs7_decrypt($infilename, $outfilename, $cert, $key)) {
    echo "decrypted!";
} else {
    echo "failed to decrypt!";
}
?>
```

openssl\_pkcs7\_encrypt
=======================

加密一个 S/MIME 消息

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs7\_encrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$infile`</span> ,
<span class="methodparam"><span class="type">string</span>
`$outfile`</span> , <span class="methodparam"><span
class="type">mixed</span> `$recipcerts`</span> , <span
class="methodparam"><span class="type">array</span> `$headers`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$cipherid`<span
class="initializer"> = OPENSSL\_CIPHER\_RC2\_40</span></span> \]\] )

<span class="function">openssl\_pkcs7\_encrypt</span>
获取文件名为`infile`的文件内容并使用 RC2
40位的密码将之加密，以至于他们只能被预期的名为`recipcerts`的接收者阅读。

### 参数

`infile`  

`outfile`  

`recipcerts`  
一个单独的X.509证书，或者一个X.509证书的数组。

`headers`  
`headers` 是包含头信息的数组，在被加密后将对数据进行预处理。

`headers`
可以是以头名为键值的关联数组，也可以是一个索引数组，其中每个元素都包含一个单独的标题行

`flags`  
`flags`用来指定影响编码过程的选项 - 参见
<a href="/openssl/constants.html#PKCS7%20标志/常量" class="link">PKCS7 常量</a>.

`cipherid`  
<a href="/openssl/constants.html#Ciphers" class="link">密码常量</a>之一。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">openssl\_pkcs7\_encrypt</span> 范例**

``` php
<?php
// the message you want to encrypt and send to your secret agent
// in the field, known as nighthawk.  You have his certificate
// in the file nighthawk.pem
$data = <<<EOD
Nighthawk,

Top secret, for your eyes only!

The enemy is closing in! Meet me at the cafe at 8.30am
to collect your forged passport!

HQ
EOD;

// load key
$key = file_get_contents("nighthawk.pem");

// save message to file
$fp = fopen("msg.txt", "w");
fwrite($fp, $data);
fclose($fp);

// encrypt it
if (openssl_pkcs7_encrypt("msg.txt", "enc.txt", $key,
    array("To" => "nighthawk@example.com", // keyed syntax
          "From: HQ <hq@example.com>", // indexed syntax
          "Subject" => "Eyes only"))) {
    // message encrypted - send it!
    exec(ini_get("sendmail_path") . " < enc.txt");
}
?>
```

openssl\_pkcs7\_read
====================

将PKCS7文件导出为PEM格式证书的数组

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs7\_read</span> ( <span
class="methodparam"><span class="type">string</span>
`$infilename`</span> , <span class="methodparam"><span
class="type">array</span> `&$certs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`infilename`  

`certs`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_pkcs7\_sign
====================

对一个 S/MIME 消息进行签名

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkcs7\_sign</span> ( <span
class="methodparam"><span class="type">string</span>
`$infilename`</span> , <span class="methodparam"><span
class="type">string</span> `$outfilename`</span> , <span
class="methodparam"><span class="type">mixed</span> `$signcert`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$privkey`</span> , <span class="methodparam"><span
class="type">array</span> `$headers`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = PKCS7\_DETACHED</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$extracerts`</span> \]\] )

<span
class="function">openssl\_pkcs7\_sign</span>获取名为`infilename`的文件内容，并使用由`signcert`和`privkey`指定的证书和与之匹配的私钥对其进行加密

### 参数

`infilename`  
你打算用来进行数字签名的输入文件。

`outfilename`  
将写入数字签名的文件。

`signcert`  
用来对输入文件进行数字签名的 X.509 证书，参见
<a href="/openssl/certparams.html" class="link">密钥/证书参数</a>获取可用列表。

`privkey`  
`privkey`是对应signcert证书的私钥。 参见
<a href="/openssl/certparams.html" class="link">公/私钥参数</a>获取可用列表。

`headers`  
`headers`是一个包含头信息的数组，在它被签名后，它将被预先对数据进行预处理
(参见 <span class="function">openssl\_pkcs7\_encrypt</span>
获取关于该参数格式的更多信息)。

`flags`  
`flags` 可以用来改变输出 - 参见
<a href="/openssl/constants.html#PKCS7%20标志/常量" class="link">PKCS7常量</a>。

`extracerts`  
`extracerts`
指定一个文件的名称，其中包含一组含有签名的额外的证书，这些证书可以用来帮助接收者验证您使用的证书。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">openssl\_pkcs7\_sign</span> 范例**

``` php
<?php
// the message you want to sign so that recipient can be sure it was you that
// sent it
$data = <<<EOD

You have my authorization to spend $10,000 on dinner expenses.

The CEO
EOD;
// save message to file
$fp = fopen("msg.txt", "w");
fwrite($fp, $data);
fclose($fp);
// encrypt it
if (openssl_pkcs7_sign("msg.txt", "signed.txt", "file://mycert.pem",
    array("file://mycert.pem", "mypassphrase"),
    array("To" => "joes@example.com", // keyed syntax
          "From: HQ <ceo@example.com>", // indexed syntax
          "Subject" => "Eyes only")
    )) {
    // message signed - send it!
    exec(ini_get("sendmail_path") . " < signed.txt");
}
?>
```

openssl\_pkcs7\_verify
======================

校验一个已签名的 S/MIME 消息的签名

### 说明

<span class="type">mixed</span> <span
class="methodname">openssl\_pkcs7\_verify</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">int</span>
`$flags`</span> \[, <span class="methodparam"><span
class="type">string</span> `$outfilename`</span> \[, <span
class="methodparam"><span class="type">array</span> `$cainfo`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$extracerts`</span> \[, <span class="methodparam"><span
class="type">string</span> `$content`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$p7bfilename`</span> \]\]\]\]\] )

<span class="function">openssl\_pkcs7\_verify</span> 读取给定文件中的
S/MIME 消息并且检查数字签名。

### 参数

`filename`  
消息的路径。

`flags`  
`flags` 可以用来影响如何校验签名 - 参见
<a href="/openssl/constants.html#PKCS7%20标志/常量" class="link">PKCS7 常量</a>
获取更多信息。

`outfilename`  
如果已指定 `outfilename`
输出文件，它应该是一个用以保存文件的字符串名称，签名消息的个人证书将以
PEM 的格式保存起来。

`cainfo`  
如果 `cainfo`
被指定了，它应该保存关于受信任的CA证书的信息供在验证过程中使用 - 参见
<a href="/openssl/cert/verification.html" class="link">证书校验</a>
获取关于该参数的更多信息。

`extracerts`  
如果 `extracerts`
被指定了，该文件包含了一堆会被作为不受信任的ca使用的证书。

`content`  
你可以使用 `content`
来指定带有已被验证数据的文件名，该文件内容已去掉了签名信息。

`p7bfilename`  

### 返回值

如果签名已被认证，返回 **`TRUE`**, 如果不正确
(消息已被篡改或者签名证书不可用) 则返回 **`FALSE`**, 或者 - 错误时返回1.

### 更新日志

| 版本  | 说明                      |
|-------|---------------------------|
| 7.2.0 | 新增 `p7bfilename` 参数。 |

### 注释

> **Note**: <span class="simpara"> 正如 RFC 2045 中指定的，`filename`
> 参数最多不可超过 76 个字符串。 </span>

openssl\_pkey\_export\_to\_file
===============================

将密钥导出到文件中

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkey\_export\_to\_file</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$outfilename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passphrase`</span> \[, <span
class="methodparam"><span class="type">array</span> `$configargs`</span>
\]\] )

<span class="function">openssl\_pkey\_export\_to\_file</span> 将 ascii
格式 (PEM编码)的 `key` 保存到名为`outfilename`文件中。

> **Note**: <span class="simpara"> 必须安装有效的 `openssl.cnf`
> 以保证此函数正确运行。参考有关<a href="/openssl/setup.html#安装" class="link">安装</a>的说明以获得更多信息。
> </span>

### 参数

`key`  

`outfilename`  
输出文件的路径。

`passphrase`  
密钥可以通过值为`passphrase`的密码来保护。

`configargs`  
`configargs`
可以用来调整导出流程，通过指定或者覆盖openssl配置文件选项。参见 <span
class="function">openssl\_csr\_new</span> 获取更多关于 `configargs`
的信息。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_pkey\_export
=====================

将一个密钥的可输出表示转换为字符串

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_pkey\_export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$out`</span> \[, <span class="methodparam"><span
class="type">string</span> `$passphrase`</span> \[, <span
class="methodparam"><span class="type">array</span> `$configargs`</span>
\]\] )

<span class="function">openssl\_pkey\_export</span> 将 `key` 当作 PEM
编码字符串导出并且将之保存到`out` (通过引用传递的)中。

> **Note**: <span class="simpara"> 必须安装有效的 `openssl.cnf`
> 以保证此函数正确运行。参考有关<a href="/openssl/setup.html#安装" class="link">安装</a>的说明以获得更多信息。
> </span>

### 参数

`key`  

`out`  

`passphrase`  
密钥可以通过 `passphrase` 来保护。

`configargs`  
`configargs`
可以用来调整导出流程，通过指定或者覆盖openssl配置文件选项。参见 <span
class="function">openssl\_csr\_new</span> 获取更多关于 `configargs`
的信息。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_pkey\_free
===================

释放一个私钥

### 说明

<span class="type">void</span> <span
class="methodname">openssl\_pkey\_free</span> ( <span
class="methodparam"><span class="type">resource</span> `$key`</span> )

该函数释放由<span class="function">openssl\_pkey\_new</span>创建的私钥。

### 参数

`key`  
持有该密钥的资源。

### 返回值

没有返回值。

openssl\_pkey\_get\_details
===========================

返回包含密钥详情的数组

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_pkey\_get\_details</span> ( <span
class="methodparam"><span class="type">resource</span> `$key`</span> )

该函数返回密钥详情(位长度，密钥，类型).

### 参数

`key`  
持有密钥的资源。

### 返回值

成功，返回包含密钥详情的数组，失败返回 **`FALSE`** .
返回的数组中包含了如下索引： *bits* (位数), *key* (表示公钥的字符串) 和
*type* (如下密钥类型之一： **`OPENSSL_KEYTYPE_RSA`**,
**`OPENSSL_KEYTYPE_DSA`**, **`OPENSSL_KEYTYPE_DH`**,
**`OPENSSL_KEYTYPE_EC`** 或者 未知类型返回1).

取决于所使用密钥的类型，可能会返回其他额外的信息。请注意，有些元素可能并不总是可用的。

-   <span class="simpara"> **`OPENSSL_KEYTYPE_RSA`**, 一个额外的键名为
    *"rsa"*的数组，包含了以下密钥数据： </span>
    | Key      | 说明                              |
    |----------|-----------------------------------|
    | *"n"*    | modulus                           |
    | *"e"*    | public exponent                   |
    | *"d"*    | private exponent                  |
    | *"p"*    | prime 1                           |
    | *"q"*    | prime 2                           |
    | *"dmp1"* | exponent1, d mod (p-1)            |
    | *"dmq1"* | exponent2, d mod (q-1)            |
    | *"iqmp"* | coefficient, (inverse of q) mod p |
-   <span class="simpara"> **`OPENSSL_KEYTYPE_DSA`**, 一个额外的键为
    *"dsa"* 的数组， 包含如下的密钥数据。 </span>
    | Key           | 说明                                |
    |---------------|-------------------------------------|
    | *"p"*         | prime number (public)               |
    | *"q"*         | 160-bit subprime, q \| p-1 (public) |
    | *"g"*         | generator of subgroup (public)      |
    | *"priv\_key"* | private key x                       |
    | *"pub\_key"*  | public key y = g^x                  |
-   <span class="simpara"> **`OPENSSL_KEYTYPE_DH`**, 一个额外的键为
    *"dh"* 的数组，包含如下的密钥数据。 </span>
    | Key           | 说明                       |
    |---------------|----------------------------|
    | *"p"*         | prime number (shared)      |
    | *"g"*         | generator of Z\_p (shared) |
    | *"priv\_key"* | private DH value x         |
    | *"pub\_key"*  | public DH value g^x        |
-   <span class="simpara"> **`OPENSSL_KEYTYPE_EC`**, 一个额外的键为
    *"ec"* 的数组,包含如下的密钥数据。 </span>
    | Key             | 说明                                                                        |
    |-----------------|-----------------------------------------------------------------------------|
    | *"curve\_name"* | name of curve, see <span class="function">openssl\_get\_curve\_names</span> |
    | *"curve\_oid"*  | ASN1 Object identifier (OID) for EC curve.                                  |
    | *"x"*           | x coordinate (public)                                                       |
    | *"y"*           | y coordinate (public)                                                       |
    | *"d"*           | private key                                                                 |

openssl\_pkey\_get\_private
===========================

获取私钥

### 说明

<span class="type">resource</span> <span
class="methodname">openssl\_pkey\_get\_private</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$passphrase`<span class="initializer"> = ""</span></span> \] )

<span class="function">openssl\_get\_privatekey</span> 解析 `key`
供其他函数使用。

### 参数

`key`  
`key` 可以是如下密钥之一：

1.  <span class="simpara">如下格式的字符串
    `file://path/to/file.pem`。该文件必须包含 PEM 编码的证书或者私钥
    (可能都包含了). </span>
2.  <span class="simpara">一个PEM格式的私钥。</span>

`passphrase`  
如果指定的密钥已被加密了(受密码保护)，可选参数 `passphrase` 是必须要的。

### 返回值

成功，返回真实的密钥资源标识符，失败，返回 **`FALSE`** .

openssl\_pkey\_get\_public
==========================

从证书中解析公钥，以供使用。

### 说明

<span class="type">resource</span> <span
class="methodname">openssl\_pkey\_get\_public</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$certificate`</span> )

<span class="function">openssl\_get\_publickey</span> 从 `certificate`
中解析公钥，供其他函数使用。

### 参数

`certificate`  
`certificate` 可以是以下之一：

1.  <span class="simpara">一个 X.509 证书资源</span>
2.  <span
    class="simpara">一个`file://path/to/file.pem`格式的字符串。文件名必须包含一个PEM编码的证书或者密钥(也许二者都有).
    </span>
3.  <span class="simpara">一个 PEM 格式的公钥。</span>

### 返回值

成功，返回真实的密钥资源标识符，错误，则返回 **`FALSE`**

openssl\_pkey\_new
==================

生成一个新的私钥

### 说明

<span class="type">resource</span> <span
class="methodname">openssl\_pkey\_new</span> (\[ <span
class="methodparam"><span class="type">array</span> `$configargs`</span>
\] )

<span class="function">openssl\_pkey\_new</span>
生成一个新的私钥和公钥对。通过 <span
class="function">openssl\_pkey\_get\_public</span>
函数获取该密钥的公共组件。

> **Note**: <span class="simpara"> 必须安装有效的 `openssl.cnf`
> 以保证此函数正确运行。参考有关<a href="/openssl/setup.html#安装" class="link">安装</a>的说明以获得更多信息。
> </span>

### 参数

`configargs`  
你可以使用`configargs`参数微调密钥的生成（比如指定位数）。查看<span
class="function">openssl\_csr\_new</span>获取更多关于`configargs`的信息。

### 返回值

成功，返回pkey的资源标识符，错误则返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明                                               |
|-------|----------------------------------------------------|
| 7.1.0 | 添加了 `curve_name` 配置参数使得可以创建 EC 密钥。 |

openssl\_private\_decrypt
=========================

使用私钥解密数据

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_private\_decrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$decrypted`</span> , <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$padding`<span
class="initializer"> = OPENSSL\_PKCS1\_PADDING</span></span> \] )

**Caution**

本函数并不会生成安全加密的值，不应用于加密用途。若需要安全加密的值，考虑使用
<span class="function">random\_int</span>、<span
class="function">random\_bytes</span> 或 <span
class="function">openssl\_random\_pseudo\_bytes</span> 替代。

<span class="function">openssl\_private\_decrypt</span> 解密先前通过
<span class="function">openssl\_public\_encrypt</span> 函数加密的 `data`
并将结果保存至`decrypted`变量中。

你可以用该函数来解密只对你可用的数据。

### 参数

`data`  

`decrypted`  

`key`  
`key` 必须是和用来加密数据所用公钥对应的私钥。

`padding`  
`padding` 可以是如下值： **`OPENSSL_PKCS1_PADDING`**,
**`OPENSSL_SSLV23_PADDING`**, **`OPENSSL_PKCS1_OAEP_PADDING`**,
**`OPENSSL_NO_PADDING`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">openssl\_public\_encrypt</span>
-   <span class="function">openssl\_public\_decrypt</span>

openssl\_private\_encrypt
=========================

使用私钥加密数据

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_private\_encrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$crypted`</span> , <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$padding`<span
class="initializer"> = OPENSSL\_PKCS1\_PADDING</span></span> \] )

<span class="function">openssl\_private\_encrypt</span> 使用私钥 `key`
加密数据 `data` 并且将结果保存至变量
`crypted`中。加密后的数据可以通过<span
class="function">openssl\_public\_decrypt</span>函数来解密。

该函数用来签名数据（或者哈希）让别人相信数据并不是其他人写的。

### 参数

`data`  

`crypted`  

`key`  

`padding`  
`padding` 可以是如下之一： **`OPENSSL_PKCS1_PADDING`**,
**`OPENSSL_NO_PADDING`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">openssl\_public\_encrypt</span>
-   <span class="function">openssl\_public\_decrypt</span>

openssl\_public\_decrypt
========================

使用公钥解密数据

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_public\_decrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$decrypted`</span> , <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$padding`<span
class="initializer"> = OPENSSL\_PKCS1\_PADDING</span></span> \] )

<span class="function">openssl\_public\_decrypt</span> 解密先前由 <span
class="function">openssl\_private\_encrypt</span> 加密的数据 `data`
并且将结果保存至变量 `decrypted`中。

你可以用该函数来校验消息是否是私钥拥有者写的。

### 参数

`data`  

`decrypted`  

`key`  
`key` 必须是和用来加密数据的私钥配对的公钥。

`padding`  
`padding` 可以是如下至 **`OPENSSL_PKCS1_PADDING`**,
**`OPENSSL_NO_PADDING`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">openssl\_private\_encrypt</span>
-   <span class="function">openssl\_private\_decrypt</span>

openssl\_public\_encrypt
========================

使用公钥加密数据

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_public\_encrypt</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$crypted`</span> , <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$padding`<span
class="initializer"> = OPENSSL\_PKCS1\_PADDING</span></span> \] )

<span class="function">openssl\_public\_encrypt</span>
使用公钥`key`解密数据 `data` 并且将结果保存到变量`crypted`中。
加密的数据可以通过<span
class="function">openssl\_private\_decrypt</span>函数解密。

该函数可以用来加密数据，供该公钥匹配的私钥拥有者读取。
它也可以用来在数据库中存储安全数据。

### 参数

`data`  

`crypted`  
这将保存加密的结果。

`key`  
公钥。

`padding`  
`padding` can be one of **`OPENSSL_PKCS1_PADDING`**,
**`OPENSSL_SSLV23_PADDING`**, **`OPENSSL_PKCS1_OAEP_PADDING`**,
**`OPENSSL_NO_PADDING`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">openssl\_private\_encrypt</span>
-   <span class="function">openssl\_private\_decrypt</span>

openssl\_random\_pseudo\_bytes
==============================

生成一个伪随机字节串

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_random\_pseudo\_bytes</span> ( <span
class="methodparam"><span class="type">int</span> `$length`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`&$crypto_strong`</span> \] )

生成一个伪随机字节串 <span class="type">string</span> ，字节数由
`length` 参数指定。

通过 `crypto_strong`
参数可以表示在生成随机字节的过程中是否使用了强加密算法。返回值为**`FALSE`**的情况很少见，但已损坏或老化的有些系统上会出现。

### 参数

`length`  
所需字节串的长度，必须为正整数。PHP会试着将该参数转换为非空整数来使用它。

`crypto_strong`  
如果传递到该函数中，将会保存为一个 <span class="type">boolean</span>
值来表明是否使用了“强加密”，如果被用于GPG和密码之类的将返回**`TRUE`** ,
否则返回 **`FALSE`**

### 返回值

成功，返回生成的字节串 <span class="type">string</span> ，
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">openssl\_random\_pseudo\_bytes</span>
范例：**

``` php
<?php
for ($i = -1; $i <= 4; $i++) {
    $bytes = openssl_random_pseudo_bytes($i, $cstrong);
    $hex   = bin2hex($bytes);

    echo "Lengths: Bytes: $i and Hex: " . strlen($hex) . PHP_EOL;
    var_dump($hex);
    var_dump($cstrong);
    echo PHP_EOL;
}
?>
```

以上例程的输出类似于：

    Lengths: Bytes: -1 and Hex: 0
    string(0) ""
    NULL

    Lengths: Bytes: 0 and Hex: 0
    string(0) ""
    NULL

    Lengths: Bytes: 1 and Hex: 2
    string(2) "42"
    bool(true)

    Lengths: Bytes: 2 and Hex: 4
    string(4) "dc6e"
    bool(true)

    Lengths: Bytes: 3 and Hex: 6
    string(6) "288591"
    bool(true)

    Lengths: Bytes: 4 and Hex: 8
    string(8) "ab86d144"
    bool(true)

### 参见

-   <span class="function">random\_bytes</span>
-   <span class="function">bin2hex</span>
-   <span class="function">crypt</span>
-   <span class="function">mt\_rand</span>
-   <span class="function">uniqid</span>

openssl\_seal
=============

密封 (加密) 数据

### 说明

<span class="type">int</span> <span
class="methodname">openssl\_seal</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$sealed_data`</span> , <span class="methodparam"><span
class="type">array</span> `&$env_keys`</span> , <span
class="methodparam"><span class="type">array</span>
`$pub_key_ids`</span> \[, <span class="methodparam"><span
class="type">string</span> `$method`<span class="initializer"> =
"RC4"</span></span> \[, <span class="methodparam"><span
class="type">string</span> `&$iv`</span> \]\] )

<span class="function">openssl\_seal</span> 使用随机生成的密钥和给定的
`method` 方法密封 (加密) `data` 数据。
密钥用与`pub_key_ids`中的标识符相关联的每个公共密钥加密，并且每个加密密钥在`env_keys`中返回。
这意味着一个人可以将密封的数据发送给多个接收者(如果一个人已经获得了他们的公钥)。每个接收方都必须同时接收加密的数据和用接收方的公钥加密的信封密钥。

### 参数

`data`  
要密封的数据。

`sealed_data`  
被密封后的数据。

`env_keys`  
已被加密的密钥数组。

`pub_key_ids`  
公钥资源标识符组成的数组。

`method`  
加密算法。

`iv`  
初始化向量。

### 返回值

成功，返回密封后数据的长度，错误，返回 **`FALSE`** .
如果密封后的数据成功地通过`sealed_data`变量返回，那么信封密钥也将会通过
`env_keys` 变量返回。

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 7.0.0 | 添加 `iv` 变量。     |
| 5.3.0 | 添加 `method` 变量。 |

### 范例

**示例 \#1 <span class="function">openssl\_seal</span> 范例：**

``` php
<?php
// $data is assumed to contain the data to be sealed

// fetch public keys for our recipients, and ready them
$fp = fopen("/src/openssl-0.9.6/demos/maurice/cert.pem", "r");
$cert = fread($fp, 8192);
fclose($fp);
$pk1 = openssl_get_publickey($cert);
// Repeat for second recipient
$fp = fopen("/src/openssl-0.9.6/demos/sign/cert.pem", "r");
$cert = fread($fp, 8192);
fclose($fp);
$pk2 = openssl_get_publickey($cert);

// seal message, only owners of $pk1 and $pk2 can decrypt $sealed with keys
// $ekeys[0] and $ekeys[1] respectively.
openssl_seal($data, $sealed, $ekeys, array($pk1, $pk2));

// free the keys from memory
openssl_free_key($pk1);
openssl_free_key($pk2);
?>
```

### 参见

-   <span class="function">openssl\_open</span>

openssl\_sign
=============

Generate signature

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_sign</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$signature`</span> , <span class="methodparam"><span
class="type">mixed</span> `$priv_key_id`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$signature_alg`<span class="initializer"> =
OPENSSL\_ALGO\_SHA1</span></span> \] )

<span class="function">openssl\_sign</span> computes a signature for the
specified `data` by generating a cryptographic digital signature using
the private key associated with `priv_key_id`. Note that the data itself
is not encrypted.

### 参数

`data`  
The string of data you wish to sign

`signature`  
If the call was successful the signature is returned in `signature`.

`priv_key_id`  
<span class="type">resource</span> - a key, returned by <span
class="function">openssl\_get\_privatekey</span>

<span class="type">string</span> - a PEM formatted key

`signature_alg`  
<span class="type">int</span> - one of these
<a href="/openssl/constants.html#Signature%20Algorithms" class="link">Signature Algorithms</a>.

<span class="type">string</span> - a valid string returned by <span
class="function">openssl\_get\_md\_methods</span> example,
"sha256WithRSAEncryption" or "sha384".

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">openssl\_sign</span> example**

``` php
<?php
// $data is assumed to contain the data to be signed

// fetch private key from file and ready it
$pkeyid = openssl_pkey_get_private("file://src/openssl-0.9.6/demos/sign/key.pem");

// compute signature
openssl_sign($data, $signature, $pkeyid);

// free the key from memory
openssl_free_key($pkeyid);
?>
```

**示例 \#2 <span class="function">openssl\_sign</span> example**

``` php
<?php
//data you want to sign
$data = 'my data';

//create new private and public key
$new_key_pair = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
openssl_pkey_export($new_key_pair, $private_key_pem);

$details = openssl_pkey_get_details($new_key_pair);
$public_key_pem = $details['key'];

//create signature
openssl_sign($data, $signature, $private_key_pem, OPENSSL_ALGO_SHA256);

//save for later
file_put_contents('private_key.pem', $private_key_pem);
file_put_contents('public_key.pem', $public_key_pem);
file_put_contents('signature.dat', $signature);

//verify signature
$r = openssl_verify($data, $signature, $public_key_pem, "sha256WithRSAEncryption");
var_dump($r);
?>
```

### 参见

-   <span class="function">openssl\_verify</span>

openssl\_spki\_export\_challenge
================================

导出与签名公钥和挑战相关的挑战字符串

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_spki\_export\_challenge</span> ( <span
class="methodparam"><span class="type">string</span> `&$spkac`</span> )

导出与签名公钥和挑战相关的挑战字符串

### 参数

`spkac`  
包含一个可用的签名公钥和挑战

### 返回值

成功，返回相关的挑战字符串，失败返回NULL.

### 错误／异常

如果 `spkac` 传递的是一个不可用的参数，则抛出一个 **`E_WARNING`**
级的错误。

### 范例

**示例 \#1 <span
class="function">openssl\_spki\_export\_challenge</span> 范例：**

成功，提取相关联的挑战字符串，失败则返回 NULL.

``` php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');
$challenge = openssl_spki_export_challenge(preg_replace('/SPKAC=/', '', $spkac));
?>
```

**示例 \#2 <span
class="function">openssl\_spki\_export\_challenge</span> 来自 \<keygen\>
元素的范例：**

从 \<keygen\> 元素中解压相关联的挑战字符串。

``` php
<?php
$challenge = openssl_spki_export_challenge(preg_replace('/SPKAC=/', '', $_POST['spkac']));
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### 参见

-   <span class="function">openssl\_spki\_new</span>
-   <span class="function">openssl\_spki\_verify</span>
-   <span class="function">openssl\_spki\_export</span>
-   <span class="function">openssl\_md\_method</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_sign</span>

openssl\_spki\_export
=====================

通过签名公钥和挑战导出一个可用的PEM格式的公钥

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_spki\_export</span> ( <span
class="methodparam"><span class="type">string</span> `&$spkac`</span> )

从编码的签名公钥和挑战导出PEM格式的公钥。

### 参数

`spkac`  
期望一个有效的签名公钥和挑战字符串。

### 返回值

成功，返回关联的PEM格式的公钥，失败则返回 NULL.

### 错误／异常

如果传递给 `spkac`
参数是一个不可用的参数，则会抛出一个**`E_WARNING`**级的警告。

### 范例

**示例 \#1 <span class="function">openssl\_spki\_export</span> 范例：**

成功，返回关联的PEM格式的公钥，失败则返回 NULL.

``` php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');
$pubKey = openssl_spki_export(preg_replace('/SPKAC=/', '', $spkac));

if ($pubKey) {
    echo $pubKey;
}
?>
```

**示例 \#2 <span class="function">openssl\_spki\_export</span> example
from \<keygen\>**

通过\<keygen\> 元素导出关联的PEM格式的公钥：

``` php
<?php
$spkac = openssl_spki_export(preg_replace('/SPKAC=/', '', $_POST['spkac']));
if ($spkac != NULL) {
    echo $spkac;
} else {
    echo "Extraction of pub key failed";
}
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### 参见

-   <span class="function">openssl\_spki\_new</span>
-   <span class="function">openssl\_spki\_verify</span>
-   <span class="function">openssl\_spki\_export\_challenge</span>
-   <span class="function">openssl\_md\_method</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_sign</span>

openssl\_spki\_new
==================

生成一个新的签名公钥和挑战

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_spki\_new</span> ( <span
class="methodparam"><span class="type">resource</span>
`&$privkey`</span> , <span class="methodparam"><span
class="type">string</span> `&$challenge`</span> \[, <span
class="methodparam"><span class="type">int</span> `$algorithm`<span
class="initializer"> = 0</span></span> \] )

使用指定的哈希算法生成一个新的签名公钥和挑战。

### 参数

`privkey`  
`privkey` 应该被设置为由<span
class="function">openssl\_pkey\_new</span>函数预先生成(或者以其他方式从openssl\_pkey函数集中获得)的私钥。该密钥的相应公共部分将用于签署CSR.

`challenge`  
与SPKAC有关的挑战。

`algorithm`  
摘要算法。参见 openssl\_get\_md\_method()函数。

### 返回值

成功，返回一个签名的公钥和挑战，失败返回 NULL .

### 错误／异常

如果 `algorithm` 参数是一个未知的签名算法，将会抛出一个 **`E_WARNING`**
级的错误。

### 范例

**示例 \#1 <span class="function">openssl\_spki\_new</span> 范例：**

使用默认的摘要算法(MD5)生成一个新的SPKAC

``` php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'testing');

if ($spkac !== NULL) {
    echo $spkac;
} else {
    echo "SPKAC generation failed";
}
?>
```

以上例程的输出类似于：

    MIICRzCCAS8wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDM3V3sS4o4
    mB9dczziRnjGAmSp+JwPrHoYMAFGvDNmZGyiWfU586X4BKs++BAj7e/FsAfno0Hd
    hN9FwpCNFSox30L03nQvLYJE7f/WqigwBeMRT7Op/xvFks4sT70xP2HRYv4KqP9a
    WRcKU6cFH8VxhFhqM2txEIxZKdFLaL28yT7bEDmcglf4JLDdgNMb9rET1dkgtKE6
    dOaJHPGjf1uvnOH4YwkQr7n4sLUR3Kdbh0ZJAFuQVDZulo+LLzxBBkqJJcB6FhF+
    oXCdHTKZnqAhpWDz+NXYytAmevab6IYm5TWPWsJUv1YKJA5lg2mXbbloIZlN9Mgc
    i9fi03bdw+crAgMBAAEWB3Rlc3RpbmcwDQYJKoZIhvcNAQEEBQADggEBALyUvP/o
    pPSoWBlorFyZ2RnGwKf9qMpE0q2IJP7G3oDR4LyK/m933DUiZ+YnqThrH/CWb4Ek
    y5I3OCyl3S4wCuU1ibZZwDVwYShr5ELp0J9PEf7qMQZOhNsizoC7k+Czb2xB6hYW
    sKfsfTKm3cXBtH3fdgc/Z1Z7VSWnAzYo38snqm72NTf5yFRnrQdphNNXi+kn1zHA
    lxXRyFDXHOcYsOnwAWfyXFA4QDHQ0ezz0UoCY8gJXovcZb4GRYqOLUAsF2HcNboy
    29WN8VqE29sL9QxVZFlwMcqyoLcNnyw38GvNvAGqSvzzbnEFP2MAQXJVe0H0hdp/
    MML5G2iNVgNozAo=

### 参见

-   <span class="function">openssl\_spki\_new</span>
-   <span class="function">openssl\_spki\_export\_challenge</span>
-   <span class="function">openssl\_spki\_export</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_sign</span>

openssl\_spki\_verify
=====================

验证签名公钥和挑战。

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_spki\_verify</span> ( <span
class="methodparam"><span class="type">string</span> `&$spkac`</span> )

验证所提供的签名公钥和挑战。

### 参数

`spkac`  
期望一个有效的签名公钥和挑战。

### 返回值

成功，返回true, 失败返回false.

### 错误／异常

如果`spkac`参数不是一个可用的参数，将会抛出一个 **`E_WARNING`**
等级的错误。

### 范例

**示例 \#1 <span class="function">openssl\_spki\_verify</span> 范例：**

验证现有签名公钥和挑战

``` php
<?php
$pkey = openssl_pkey_new('secret password');
$spkac = openssl_spki_new($pkey, 'challenge string');

if (openssl_spki_verify(preg_replace('/SPKAC=/', '', $spkac))) {
    echo $spkac;
} else {
    echo "SPKAC validation failed";
}
?>
```

**示例 \#2 <span class="function">openssl\_spki\_verify</span> example
from \<keygen\>**

通过\<keygen\> 元素验证现有签名公钥和挑战

``` php
<?php
if (openssl_spki_verify(preg_replace('/SPKAC=/', '', $_POST['spkac']))) {
    echo $spkac;
} else {
    echo "SPKAC validation failed";
}
?>
<keygen name="spkac" challenge="challenge string" keytype="RSA">
```

### 参见

-   <span class="function">openssl\_spki\_new</span>
-   <span class="function">openssl\_spki\_export\_challenge</span>
-   <span class="function">openssl\_spki\_export</span>
-   <span class="function">openssl\_md\_method</span>
-   <span class="function">openssl\_csr\_new</span>
-   <span class="function">openssl\_csr\_sign</span>

openssl\_verify
===============

验证签名

### 说明

<span class="type">int</span> <span
class="methodname">openssl\_verify</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$signature`</span> , <span class="methodparam"><span
class="type">mixed</span> `$pub_key_id`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$signature_alg`<span class="initializer"> =
OPENSSL\_ALGO\_SHA1</span></span> \] )

<span class="function">openssl\_verify</span>
使用与`pub_key_id`关联的公钥验证指定数据`data`的签名`signature`是否正确。这必须是与用于签名的私钥相对应的公钥。

### 参数

`data`  
以前用来生成签名的数据字符串。

`signature`  
原始二进制字符串，通过<span
class="function">openssl\_sign</span>或类似的函数生成。

`pub_key_id`  
<span class="type">resource</span> - 一个密钥, 通过 <span
class="function">openssl\_get\_publickey</span> 函数返回。

<span class="type">string</span> - 一个 PEM 格式的密钥, 比如,
"-----BEGIN PUBLIC KEY----- MIIBCgK..."

`signature_alg`  
<span class="type">int</span> -
以下签名算法之一<a href="/openssl/constants.html#Signature%20Algorithms" class="link">Signature Algorithms</a>.

<span class="type">string</span> - 由<span
class="function">openssl\_get\_md\_methods</span>函数返回的可用字符串，比如，
"sha1WithRSAEncryption" 或者 "sha512".

### 返回值

如果签名正确返回 1, 签名错误返回 0, 内部发生错误则返回-1.

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 5.2.0 | 添加了 `signature_alg` 参数。 |

### 范例

**示例 \#1 <span class="function">openssl\_verify</span> 范例：**

``` php
<?php
// $data and $signature are assumed to contain the data and the signature

// fetch public key from certificate and ready it
$pubkeyid = openssl_pkey_get_public("file://src/openssl-0.9.6/demos/sign/cert.pem");

// state whether signature is okay or not
$ok = openssl_verify($data, $signature, $pubkeyid);
if ($ok == 1) {
    echo "good";
} elseif ($ok == 0) {
    echo "bad";
} else {
    echo "ugly, error checking signature";
}
// free the key from memory
openssl_free_key($pubkeyid);
?>
```

**示例 \#2 <span class="function">openssl\_verify</span> 范例：**

``` php
<?php
//data you want to sign
$data = 'my data';

//create new private and public key
$private_key_res = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$details = openssl_pkey_get_details($private_key_res);
$public_key_res = openssl_pkey_get_public($details['key']);

//create signature
openssl_sign($data, $signature, $private_key_res, "sha1WithRSAEncryption");

//verify signature
$ok = openssl_verify($data, $signature, $public_key_res, OPENSSL_ALGO_SHA1);
if ($ok == 1) {
    echo "valid";
} elseif ($ok == 0) {
    echo "invalid";
} else {
    echo "error: ".openssl_error_string();
}
?>
```

### 参见

-   <span class="function">openssl\_sign</span>

openssl\_x509\_check\_private\_key
==================================

检查私钥是否对应于证书

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_x509\_check\_private\_key</span> ( <span
class="methodparam"><span class="type">mixed</span> `$cert`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$key`</span>
)

检查给定的私钥 `key` 是否和证书 `cert` 对应。

**Warning**

这个函数不会检查密钥`key`是否真的是私钥。
它只是比较了和密钥匹配的公共材料 (比如，RSA密钥的指数和模量)
和/或密钥参数(比如，EC密钥的参数)。

这也意味着，比如，提供给`key`赋一个公钥值，该函数可能返回 **`TRUE`**.

### 参数

`cert`  
证书。

`key`  
私钥。

### 返回值

如果给定的私钥 `key` 和证书 `cert`对应， 返回**`TRUE`** 否则返回
**`FALSE`** .

openssl\_x509\_checkpurpose
===========================

验证是否可以为特定目的使用证书

### 说明

<span class="type">int</span> <span
class="methodname">openssl\_x509\_checkpurpose</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509cert`</span> ,
<span class="methodparam"><span class="type">int</span>
`$purpose`</span> \[, <span class="methodparam"><span
class="type">array</span> `$cainfo`<span class="initializer"> =
array()</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$untrustedfile`</span> \]\] )

<span class="function">openssl\_x509\_checkpurpose</span>
检查证书以查看它是否可用于指定目的 `purpose`.

### 参数

`x509cert`  
被检查的证书。

`purpose`  
| 常量名                         | 描述                                   |
|--------------------------------|----------------------------------------|
| X509\_PURPOSE\_SSL\_CLIENT     | 证书是否可以用于SSL连接的客户端?       |
| X509\_PURPOSE\_SSL\_SERVER     | 证书是否可以用于SSL连接的服务器端?     |
| X509\_PURPOSE\_NS\_SSL\_SERVER | 证书是否可以用于Netscape SSL服务器?    |
| X509\_PURPOSE\_SMIME\_SIGN     | 证书是否可以用来签名 S/MIME 邮件?      |
| X509\_PURPOSE\_SMIME\_ENCRYPT  | 正式是否可用用来加密 S/MIME 邮件?      |
| X509\_PURPOSE\_CRL\_SIGN       | 证书是否可以用来签名证书撤销列表(CRL)? |
| X509\_PURPOSE\_ANY             | 证书是否可以用于任何目的?              |

这些选项不是位字段——您只能指定一个字段!

`cainfo`  
`cainfo` 应该是一个受信任的 CA
文件/文件夹组成的数组，如<a href="/openssl/cert/verification.html" class="link">Certificate Verification</a>所描述的一样。

`untrustedfile`  
如果指定，这应该是PEM编码文件的名称，该文件持有证书，可以用来帮助验证证书,尽管从该文件中获得的证书不受信任。

### 返回值

如果证书可以用于预期目的，返回 **`TRUE`**,如果不行，则返回 **`FALSE`**
错误便会返回 -1。

openssl\_x509\_export\_to\_file
===============================

导出证书至文件

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_x509\_export\_to\_file</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509`</span> ,
<span class="methodparam"><span class="type">string</span>
`$outfilename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$notext`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="function">openssl\_x509\_export\_to\_file</span> 将 `x509`
以PEM编码的格式保存到名为 `outfilename` 的文件中。

### 参数

`x509`  
参见<a href="/openssl/certparams.html" class="link">密钥／证书参数</a>以获取有效值列表。

`outfilename`  
输出文件的路径。

`notext`  
可选参数 `notext` 影响输出的冗余度。如果设为
**`FALSE`**，输出内容将包含附加的人类可读信息。`notext` 的缺省值为
**`TRUE`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_x509\_export
=====================

以字符串格式导出证书

### 说明

<span class="type">bool</span> <span
class="methodname">openssl\_x509\_export</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$output`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$notext`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="function">openssl\_x509\_export</span> 将 `x509`
以PEM编码的格式导出到名为 `output` 的字符串类型的变量中。

### 参数

`x509`  
参见<a href="/openssl/certparams.html" class="link">密钥／证书参数</a>以获取有效值列表。

`output`  
成功，将会存储 PEM.

`notext`  
可选参数 `notext` 影响输出的冗余度。如果设为
**`FALSE`**，输出内容将包含附加的人类可读信息。`notext` 的缺省值为
**`TRUE`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

openssl\_x509\_fingerprint
==========================

计算一个给定的x.509证书的指纹或摘要

### 说明

<span class="type">string</span> <span
class="methodname">openssl\_x509\_fingerprint</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$hash_algorithm`<span class="initializer"> = "sha1"</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$raw_output`<span class="initializer"> = **`FALSE`**</span></span> \]\]
)

<span class="function">openssl\_x509\_fingerprint</span>
返回`x509`的字符串类型的摘要。

### 参数

`x509`  
参见<a href="/openssl/certparams.html" class="link">密钥／证书参数</a>以获取有效值列表。

`hash_algorithm`  
使用的摘要方法或散列算法，比如， "sha256", <span
class="function">openssl\_get\_md\_methods</span>摘要算法之一。

`raw_output`  
设置为 **`TRUE`**时，输出原始二进制数据。设置为
**`FALSE`**时，输出小写的16进制字符串。

### 返回值

将包含计算的证书指纹的字符串返回为小写16进制格式，除非将`raw_output`设置为TRUE，在这种情况下会返回消息摘要的原始二进制表示形式。

失败则返回 **`FALSE`** .

openssl\_x509\_free
===================

释放证书资源

### 说明

<span class="type">void</span> <span
class="methodname">openssl\_x509\_free</span> ( <span
class="methodparam"><span class="type">resource</span>
`$x509cert`</span> )

<span class="function">openssl\_x509\_free</span> 从内存中释放和指定
`x509cert`资源相关联的证书。

### 参数

`x509cert`  

### 返回值

没有返回值。

openssl\_x509\_parse
====================

解析一个X509证书并作为一个数组返回信息

### 说明

<span class="type">array</span> <span
class="methodname">openssl\_x509\_parse</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509cert`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$shortnames`<span class="initializer"> = **`TRUE`**</span></span> \] )

<span class="function">openssl\_x509\_parse</span> 返回提供的 `x509cert`
证书的信息， 包括主题名称、发行方名称、目的、有效日期等字段。

### 参数

`x509cert`  

`shortnames`  
`shortnames` 控制数据在数组中的索引 - 如果 `shortnames` 为 **`TRUE`**
(默认) 字段将以短名称的形式被索引， 否则将会使用长名称的形式 - 比如： CN
就是commonName的短名称格式。

### 返回值

*返回的数据的结构是（故意的）还没有文档化，因为它仍然会发生变化。*

openssl\_x509\_read
===================

解析一个x.509证书并返回一个资源标识符

### 说明

<span class="type">resource</span> <span
class="methodname">openssl\_x509\_read</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$x509certdata`</span> )

<span class="function">openssl\_x509\_read</span>
解析`x509certdata`提供的证书，并返回一个资源标识符。

### 参数

`x509certdata`  
X509 证书。参见
<a href="/openssl/certparams.html" class="link">Key/Certificate parameters</a>
获取可用的值。

### 返回值

成功，返回一个资源标识符， 或者在失败时返回 **`FALSE`**.

openssl\_x509\_verify
=====================

Verifies digital signature of x509 certificate against a public key

### 说明

<span class="type">int</span> <span
class="methodname">openssl\_x509\_verify</span> ( <span
class="methodparam"><span class="type">mixed</span> `$x509`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$pub_key_id`</span> )

<span class="function">openssl\_x509\_verify</span> verifies that the
`x509` certificate was signed by the private key corresponding to public
key `pub_key_id`.

### 参数

`x509`  
参见<a href="/openssl/certparams.html" class="link">密钥／证书参数</a>以获取有效值列表。

`pub_key_id`  
<span class="type">resource</span> - a key, returned by <span
class="function">openssl\_get\_publickey</span>

<span class="type">string</span> - a PEM formatted key, example,
"-----BEGIN PUBLIC KEY----- MIIBCgK..."

### 返回值

Returns 1 if the signature is correct, 0 if it is incorrect, and -1 on
error.

### 范例

**示例 \#1 <span class="function">openssl\_x509\_verify</span> example**

``` php
<?php
$hostname = "news.php.net";
$ssloptions = array(
    "capture_peer_cert" => true, 
    "capture_peer_cert_chain" => true, 
    "allow_self_signed"=> false, 
    "CN_match" => $hostname,
    "verify_peer" => true,
    "SNI_enabled" => true,
    "SNI_server_name" => $hostname,
);
 
$ctx = stream_context_create( array("ssl" => $ssloptions) );
$result = stream_socket_client("ssl://$hostname:443", $errno, $errstr, 30, STREAM_CLIENT_CONNECT, $ctx);
$cont = stream_context_get_params($result);
$x509 = $cont["options"]["ssl"]["peer_certificate"];
$certparsed = openssl_x509_parse($x509);

foreach($cont["options"]["ssl"]["peer_certificate_chain"] as $chaincert)
{
    $chainparsed = openssl_x509_parse($chaincert);
    $chain_public_key = openssl_get_publickey($chaincert);
    $r = openssl_x509_verify($x509, $chain_public_key);   
    if ($r==1)
    {
        echo $certparsed['subject']['CN'];
        echo " was digitally signed by ";
        echo $chainparsed['subject']['CN']."\n";
    }
}
?>
```

### 参见

-   <span class="function">openssl\_verify</span>
-   <span class="function">openssl\_get\_publickey</span>

**目录**

-   [openssl\_cipher\_iv\_length](/ref/openssl.html#openssl_cipher_iv_length)
    — 获取密码iv长度
-   [openssl\_csr\_export\_to\_file](/ref/openssl.html#openssl_csr_export_to_file)
    — 将CSR导出到文件
-   [openssl\_csr\_export](/ref/openssl.html#openssl_csr_export) —
    将CSR作为字符串导出
-   [openssl\_csr\_get\_public\_key](/ref/openssl.html#openssl_csr_get_public_key)
    — 返回CSR的公钥
-   [openssl\_csr\_get\_subject](/ref/openssl.html#openssl_csr_get_subject)
    — 返回CSR的主题
-   [openssl\_csr\_new](/ref/openssl.html#openssl_csr_new) — 生成一个
    CSR
-   [openssl\_csr\_sign](/ref/openssl.html#openssl_csr_sign) —
    用另一个证书签署 CSR (或者本身) 并且生成一个证书
-   [openssl\_decrypt](/ref/openssl.html#openssl_decrypt) — 解密数据
-   [openssl\_dh\_compute\_key](/ref/openssl.html#openssl_dh_compute_key)
    — 计算远程DH密钥(公钥)和本地DH密钥的共享密钥
-   [openssl\_digest](/ref/openssl.html#openssl_digest) — 计算摘要
-   [openssl\_encrypt](/ref/openssl.html#openssl_encrypt) — 加密数据
-   [openssl\_error\_string](/ref/openssl.html#openssl_error_string) —
    返回 openSSL 错误消息
-   [openssl\_free\_key](/ref/openssl.html#openssl_free_key) —
    释放密钥资源
-   [openssl\_get\_cert\_locations](/ref/openssl.html#openssl_get_cert_locations)
    — 检索可用的证书位置
-   [openssl\_get\_cipher\_methods](/ref/openssl.html#openssl_get_cipher_methods)
    — 获取可用的加密算法
-   [openssl\_get\_curve\_names](/ref/openssl.html#openssl_get_curve_names)
    — 获得ECC的可用曲线名称列表
-   [openssl\_get\_md\_methods](/ref/openssl.html#openssl_get_md_methods)
    — 获取可用的摘要算法
-   [openssl\_get\_privatekey](/ref/openssl.html#openssl_get_privatekey)
    — 别名 openssl\_pkey\_get\_private
-   [openssl\_get\_publickey](/ref/openssl.html#openssl_get_publickey) —
    别名 openssl\_pkey\_get\_public
-   [openssl\_open](/ref/openssl.html#openssl_open) — 打开密封的数据
-   [openssl\_pbkdf2](/ref/openssl.html#openssl_pbkdf2) — 生成一个 PKCS5
    v2 PBKDF2 字符串
-   [openssl\_pkcs12\_export\_to\_file](/ref/openssl.html#openssl_pkcs12_export_to_file)
    — 输出一个 PKCS\#12 兼容的证书存储文件
-   [openssl\_pkcs12\_export](/ref/openssl.html#openssl_pkcs12_export) —
    将 PKCS\#12 兼容证书存储文件导出到变量
-   [openssl\_pkcs12\_read](/ref/openssl.html#openssl_pkcs12_read) — 将
    PKCS\#12 证书存储区解析到数组中
-   [openssl\_pkcs7\_decrypt](/ref/openssl.html#openssl_pkcs7_decrypt) —
    解密一个 S/MIME 加密的消息
-   [openssl\_pkcs7\_encrypt](/ref/openssl.html#openssl_pkcs7_encrypt) —
    加密一个 S/MIME 消息
-   [openssl\_pkcs7\_read](/ref/openssl.html#openssl_pkcs7_read) —
    将PKCS7文件导出为PEM格式证书的数组
-   [openssl\_pkcs7\_sign](/ref/openssl.html#openssl_pkcs7_sign) —
    对一个 S/MIME 消息进行签名
-   [openssl\_pkcs7\_verify](/ref/openssl.html#openssl_pkcs7_verify) —
    校验一个已签名的 S/MIME 消息的签名
-   [openssl\_pkey\_export\_to\_file](/ref/openssl.html#openssl_pkey_export_to_file)
    — 将密钥导出到文件中
-   [openssl\_pkey\_export](/ref/openssl.html#openssl_pkey_export) —
    将一个密钥的可输出表示转换为字符串
-   [openssl\_pkey\_free](/ref/openssl.html#openssl_pkey_free) —
    释放一个私钥
-   [openssl\_pkey\_get\_details](/ref/openssl.html#openssl_pkey_get_details)
    — 返回包含密钥详情的数组
-   [openssl\_pkey\_get\_private](/ref/openssl.html#openssl_pkey_get_private)
    — 获取私钥
-   [openssl\_pkey\_get\_public](/ref/openssl.html#openssl_pkey_get_public)
    — 从证书中解析公钥，以供使用。
-   [openssl\_pkey\_new](/ref/openssl.html#openssl_pkey_new) —
    生成一个新的私钥
-   [openssl\_private\_decrypt](/ref/openssl.html#openssl_private_decrypt)
    — 使用私钥解密数据
-   [openssl\_private\_encrypt](/ref/openssl.html#openssl_private_encrypt)
    — 使用私钥加密数据
-   [openssl\_public\_decrypt](/ref/openssl.html#openssl_public_decrypt)
    — 使用公钥解密数据
-   [openssl\_public\_encrypt](/ref/openssl.html#openssl_public_encrypt)
    — 使用公钥加密数据
-   [openssl\_random\_pseudo\_bytes](/ref/openssl.html#openssl_random_pseudo_bytes)
    — 生成一个伪随机字节串
-   [openssl\_seal](/ref/openssl.html#openssl_seal) — 密封 (加密) 数据
-   [openssl\_sign](/ref/openssl.html#openssl_sign) — Generate signature
-   [openssl\_spki\_export\_challenge](/ref/openssl.html#openssl_spki_export_challenge)
    — 导出与签名公钥和挑战相关的挑战字符串
-   [openssl\_spki\_export](/ref/openssl.html#openssl_spki_export) —
    通过签名公钥和挑战导出一个可用的PEM格式的公钥
-   [openssl\_spki\_new](/ref/openssl.html#openssl_spki_new) —
    生成一个新的签名公钥和挑战
-   [openssl\_spki\_verify](/ref/openssl.html#openssl_spki_verify) —
    验证签名公钥和挑战。
-   [openssl\_verify](/ref/openssl.html#openssl_verify) — 验证签名
-   [openssl\_x509\_check\_private\_key](/ref/openssl.html#openssl_x509_check_private_key)
    — 检查私钥是否对应于证书
-   [openssl\_x509\_checkpurpose](/ref/openssl.html#openssl_x509_checkpurpose)
    — 验证是否可以为特定目的使用证书
-   [openssl\_x509\_export\_to\_file](/ref/openssl.html#openssl_x509_export_to_file)
    — 导出证书至文件
-   [openssl\_x509\_export](/ref/openssl.html#openssl_x509_export) —
    以字符串格式导出证书
-   [openssl\_x509\_fingerprint](/ref/openssl.html#openssl_x509_fingerprint)
    — 计算一个给定的x.509证书的指纹或摘要
-   [openssl\_x509\_free](/ref/openssl.html#openssl_x509_free) —
    释放证书资源
-   [openssl\_x509\_parse](/ref/openssl.html#openssl_x509_parse) —
    解析一个X509证书并作为一个数组返回信息
-   [openssl\_x509\_read](/ref/openssl.html#openssl_x509_read) —
    解析一个x.509证书并返回一个资源标识符
-   [openssl\_x509\_verify](/ref/openssl.html#openssl_x509_verify) —
    Verifies digital signature of x509 certificate against a public key
