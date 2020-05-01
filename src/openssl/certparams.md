密钥/证书参数
=============

相当一部分的 openssl
函数需要密钥或者证书参数。可通过以下途径获取这些参数。

-   证书

    1.  <span class="simpara"> 一个由 <span
        class="function">openssl\_x509\_read</span> 返回的 X.509资源
        </span>
    2.  <span class="simpara">如下格式的字符串
        `file://path/to/cert.pem`; 命名文件必须包含一个PEM编码的证书
        </span>
    3.  <span class="simpara">
        一个包含了证书内容的字符串，PEM编码，应该是以 -----BEGIN
        CERTIFICATE----- 开头。 </span>

-   证书签名请求 (CSRs)

    1.  <span class="simpara"> 一个由 <span
        class="function">openssl\_csr\_new</span> 函数返回的 CSR 资源
        </span>
    2.  <span class="simpara">如下格式的字符串`file://path/to/csr.pem`;
        命名文件必须包含一个PEM编码的 CSR </span>
    3.  <span class="simpara"> 一个包含了 CSR
        内容的字符串，PEM编码，应该是以 -----BEGIN CERTIFICATE
        REQUEST----- 开头。 </span>

-   公钥/私钥

    1.  <span class="simpara">一个由 <span
        class="function">openssl\_get\_publickey</span> 或者 <span
        class="function">openssl\_get\_privatekey</span>
        函数返回的密钥资源 </span>
    2.  <span class="simpara">仅限公钥：一个 X.509 资源</span>
    3.  <span class="simpara">如下格式的字符串
        `file://path/to/file.pem` -
        命名文件必须包含一个PEM编码的证书/私钥（必须包含二者） </span>
    4.  <span class="simpara">
        一个包含证书/私钥内容的字符串，PEM编码，应该是以 -----BEGIN
        PUBLIC KEY----- 开头。 </span>
    5.  <span class="simpara"> 对于私钥，应该使用*array($key,
        $passphrase)* 的语法格式，这里的 `$key`
        代表由file://格式的文件或者文本字符表示的密钥, 而 `$passphrase`
        表示一个包含该私钥的密码的字符串。 </span>
