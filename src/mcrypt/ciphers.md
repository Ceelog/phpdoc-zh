Mcrypt 密码
===========

下表是 mcrypt 扩展所支持的密码。 所支持的密码的完整列表请参见 `mcrypt.h`
文件。 在 PHP 中使用 mcrypt-2.2.x 的一个通用规则是你可以使用
MCRYPT\_ciphername 来访问密码。 在 libmcrypt-2.4.x 和 libmcrypt-2.5.x 的
API 中，这些常量依然可用， 但是你也可以把密码模式以字符串的形式传入
<span class="function">mcrypt\_module\_open</span> 函数 来进行访问。

-   <span class="simpara">MCRYPT\_3DES</span>
-   <span class="simpara">MCRYPT\_ARCFOUR\_IV ( 仅 libmcrypt \> 2.4.x
    可用 )</span>
-   <span class="simpara">MCRYPT\_ARCFOUR ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_BLOWFISH</span>
-   <span class="simpara">MCRYPT\_CAST\_128</span>
-   <span class="simpara">MCRYPT\_CAST\_256</span>
-   <span class="simpara">MCRYPT\_CRYPT</span>
-   <span class="simpara">MCRYPT\_DES</span>
-   <span class="simpara">MCRYPT\_DES\_COMPAT ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_ENIGMA ( 仅 libmcrypt \> 2.4.x
    可用，MCRYPT\_CRYPT 的别名)</span>
-   <span class="simpara">MCRYPT\_GOST</span>
-   <span class="simpara">MCRYPT\_IDEA (非免费算法)</span>
-   <span class="simpara">MCRYPT\_LOKI97 ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_MARS ( 仅 libmcrypt \> 2.4.x
    可用，非免费算法)</span>
-   <span class="simpara">MCRYPT\_PANAMA ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_RIJNDAEL\_128 ( 仅 libmcrypt \> 2.4.x
    可用 )</span>
-   <span class="simpara">MCRYPT\_RIJNDAEL\_192 ( 仅 libmcrypt \> 2.4.x
    可用 )</span>
-   <span class="simpara">MCRYPT\_RIJNDAEL\_256 ( 仅 libmcrypt \> 2.4.x
    可用 )</span>
-   <span class="simpara">MCRYPT\_RC2</span>
-   <span class="simpara">MCRYPT\_RC4 ( 仅 libmcrypt 2.2.x 可用 )</span>
-   <span class="simpara">MCRYPT\_RC6 ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_RC6\_128 ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_RC6\_192 ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_RC6\_256 ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_SAFER64</span>
-   <span class="simpara">MCRYPT\_SAFER128</span>
-   <span class="simpara">MCRYPT\_SAFERPLUS ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_SERPENT( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_SERPENT\_128 ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_SERPENT\_192 ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_SERPENT\_256 ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_SKIPJACK ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_TEAN ( 仅 libmcrypt 2.2.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_THREEWAY</span>
-   <span class="simpara">MCRYPT\_TRIPLEDES ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_TWOFISH ( mcrypt 2.x 之前的版本，或者
    2.4.x 之后版本可用 )</span>
-   <span class="simpara">MCRYPT\_TWOFISH128 (TWOFISHxxx 在新的 2.x
    版本可用，但在 2.4.x 版本不可用)</span>
-   <span class="simpara">MCRYPT\_TWOFISH192</span>
-   <span class="simpara">MCRYPT\_TWOFISH256</span>
-   <span class="simpara">MCRYPT\_WAKE ( 仅 libmcrypt \> 2.4.x 可用
    )</span>
-   <span class="simpara">MCRYPT\_XTEA ( 仅 libmcrypt \> 2.4.x 可用
    )</span>

如果使用 **`CFB`** 和 **`OFB`** 模式， 必须提供初始向量（IV）， 如果使用
**`CBC`** 模式， 可以提供一个初始向量。
初始向量必须是唯一的，并且在加密和解密过程中要保持一致。
你可以将初始向量和加密后数据一起存储，
其存储位置可以由一个函数的输出来指定， 例如文件名的 MD5 散列值，
这样你就可以把初始向量和加密后的数据一起传输
（关于本话题的更多信息，请参见 Applied Cryptography by Schneier (ISBN
0-471-11709-9) 9.3 一节）。
