预定义常量
==========

**目录**

-   [目的检查标志](/openssl/constants.html#目的检查标志)
-   [非对称加密的填充标志](/openssl/constants.html#非对称加密的填充标志)
-   [密钥类型](/openssl/constants.html#密钥类型)
-   [PKCS7 标志/常量](/openssl/constants.html#PKCS7%20标志/常量)
-   [Signature
    Algorithms](/openssl/constants.html#Signature%20Algorithms)
-   [Ciphers](/openssl/constants.html#Ciphers)
-   [Version constants](/openssl/constants.html#Version%20constants)
-   [Server Name Indication
    constants](/openssl/constants.html#Server%20Name%20Indication%20constants)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

目的检查标志
------------

**`X509_PURPOSE_SSL_CLIENT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`X509_PURPOSE_SSL_SERVER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`X509_PURPOSE_NS_SSL_SERVER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`X509_PURPOSE_SMIME_SIGN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`X509_PURPOSE_SMIME_ENCRYPT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`X509_PURPOSE_CRL_SIGN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`X509_PURPOSE_ANY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

非对称加密的填充标志
--------------------

**`OPENSSL_PKCS1_PADDING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_SSLV23_PADDING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_NO_PADDING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_PKCS1_OAEP_PADDING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

密钥类型
--------

**`OPENSSL_KEYTYPE_RSA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_KEYTYPE_DSA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_KEYTYPE_DH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_KEYTYPE_EC`** (<span class="type">integer</span>)  
<span class="simpara"> 这个常量只有在使用OpenSSL
0.9.8+进行编译时才可用。 </span>

> **Note**:
>
> 这个常量是在5.2.0版本中添加的.
>
> **`OPENSSL_KEYTYPE_EC`**

PKCS7 标志/常量
---------------

S/MIME 函数使用通过一个位阈来表示的标志位，该位阈可包含如下一个或多个值:

| 常量名               | 描述                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`PKCS7_TEXT`**     | 把纯文本类型的header头添加到加密/签名的消息中。如果解密或者验证，将会从输出中剥离这些header头 - 如果这些被解密或验证的消息不是 MIME 类型的纯文本文件将会导致一个错误。                                                                                                                                       |
| **`PKCS7_BINARY`**   | 通常输入消息将被转成以*CR*和*LF*作行末的 "canonical" 格式(S/MIME规范中的声明)。当该选项出现时，消息将不会被转化。 当处理非MIME格式的二进制数据时，这个选项会很有用。                                                                                                                                         |
| **`PKCS7_NOINTERN`** | 在验证消息时，在消息中包含的证书(如果有的话)通常会被搜索签名证书。 对于该选项，只有当 <span class="function">openssl\_pkcs7\_verify</span> 函数的参数`extracerts`指定了的证书才会被使用。然而提供的证书仍然被当做不受信任的证书使用。                                                                        |
| **`PKCS7_NOVERIFY`** | 不要验证签名消息的签名者证书。                                                                                                                                                                                                                                                                               |
| **`PKCS7_NOCHAIN`**  | 不要约束验证签名者证书：不要把签名消息中的证书当做不受信任的证书。                                                                                                                                                                                                                                           |
| **`PKCS7_NOCERTS`**  | 在签署消息时，签名者的证书通常包括在内，但是有了这个选项后，就不需要包括证书了。这将会缩小被签名消息的大小，但是验证人在本地必须有可用的签名者证书副本(比如由<span class="function">openssl\_pkcs7\_verify</span>函数中的`extracerts`参数传递) 。                                                            |
| **`PKCS7_NOATTR`**   | 通常当消息被签名了，一些属性的集合将会包含在内，比如签名时间和支持的对称算法。使用该选项用来设置不包含这些属性。                                                                                                                                                                                             |
| **`PKCS7_DETACHED`** | 当签名消息时，使用 MIME 类型(*"multipart/signed"*)的明文签名。如果你为<span class="function">openssl\_pkcs7\_sign</span>函数没有指定任何`flags`，这个将会是默认的值。 如果你关闭这个选项，消息将使用不透明的签名来签名, 这将会使消息更能抵抗邮件中继的翻译，但是不支持 S/MIME 的邮件客户端将不能读取该消息。 |
| **`PKCS7_NOSIGS`**   | 不要尝试在消息中验证签名                                                                                                                                                                                                                                                                                     |

> **Note**:
>
> 这些常量在 4.0.6 版本中被添加。

Signature Algorithms
--------------------

**`OPENSSL_ALGO_DSS1`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_SHA1`** (<span class="type">integer</span>)  
<span class="simpara"> <span class="function">openssl\_sign</span> 和
<span class="function">openssl\_verify</span> 函数使用的默认算法。
</span>

**`OPENSSL_ALGO_SHA224`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_SHA256`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_SHA384`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_SHA512`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_RMD160`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_MD5`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_MD4`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_ALGO_MD2`** (<span class="type">integer</span>)  
<span class="simpara"> 在PHP 5.2.13和PHP
5.3.2中，只有在使用MD2支持编译PHP时，才可以使用这个常量。
当在编译PHP时需要验证通过 DHAVE\_OPENSSL\_MD2\_H CFLAGP, 当编译 OpenSSL
1.0.0+ 版本时需要启用 enable-md2选项。 </span>

> **Note**:
>
> 这些常量是在5.0.0版本中添加的。
>
> **`OPENSSL_ALGO_MD2`**, **`OPENSSL_ALGO_MD4`**,
> **`OPENSSL_ALGO_MD5`**, **`OPENSSL_ALGO_SHA1`**,
> **`OPENSSL_ALGO_DSS1`**

> **Note**:
>
> 这些常量是在5.4.8版本中添加的。
>
> **`OPENSSL_ALGO_RMD160`**, **`OPENSSL_ALGO_SHA224`**,
> **`OPENSSL_ALGO_SHA256`**, **`OPENSSL_ALGO_SHA384`**,
> **`OPENSSL_ALGO_SHA512`**

Ciphers
-------

**`OPENSSL_CIPHER_RC2_40`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_CIPHER_RC2_128`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_CIPHER_RC2_64`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_CIPHER_DES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_CIPHER_3DES`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

> **Note**:
>
> 这些常量是在4.3.0版本中添加的。

**`OPENSSL_CIPHER_AES_128_CBC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_CIPHER_AES_192_CBC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`OPENSSL_CIPHER_AES_256_CBC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

> **Note**:
>
> 这些常量是在5.4.0版本中添加的。

Version constants
-----------------

**`OPENSSL_VERSION_TEXT`** (<span class="type">string</span>)  
<span class="simpara"> </span>

**`OPENSSL_VERSION_NUMBER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

> **Note**:
>
> 这些常量是在5.2.0版本中添加的。

Server Name Indication constants
--------------------------------

**`OPENSSL_TLSEXT_SERVER_NAME`** (<span class="type">string</span>)  
<span class="simpara"> SNI 支持是否可用。 </span>

> **Note**:
>
> 这个常量是在5.3.2版本中添加的，并且要求PHP是由OpenSSL
> 0.9.8j及以上版本构建的。
