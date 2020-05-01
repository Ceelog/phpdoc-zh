**Warning**

This feature was *DEPRECATED* in PHP 7.1.0, and *REMOVED* in PHP 7.2.0.

Alternatives to this feature include:

-   <a href="/book/sodium.html" class="link">Sodium</a> (available as of
    PHP 7.2.0)
-   <a href="/book/openssl.html" class="link">OpenSSL</a>

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。7.2.0.

本扩展是 mcrypt 库的接口，mcrypt 库提供了对多种块算法的支持，
包括：DES，TripleDES，Blowfish （默认），
3-WAY，SAFER-SK64，SAFER-SK128，TWOFISH，TEA，RC2 以及 GOST，并且支持
CBC，OFB，CFB 和 ECB 密码模式。 甚至，它还支持诸如 RC6 和 IDEA
这两种“非免费”的算法。 默认情况下，CFB/OFB 是 8 比特的。
