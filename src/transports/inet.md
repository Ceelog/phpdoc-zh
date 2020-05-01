Internet 领域：TCP，UDP，SSL 和 TLS
-----------------------------------

PHP 3，PHP 4，PHP 5。 *ssl://*& *tls://*自 PHP 4.3 起可用。

*sslv2://*& *sslv3://*自 PHP 5.0.2 起可用。

> **Note**: <span class="simpara">如果没有指定传输器，则假定为
> *tcp://*。</span>

-   <span class="simpara"> *127.0.0.1* </span>
-   <span class="simpara"> *fe80::1* </span>
-   <span class="simpara"> *www.example.com* </span>
-   <span class="simpara"> *tcp://127.0.0.1* </span>
-   <span class="simpara"> *tcp://fe80::1* </span>
-   <span class="simpara"> *tcp://www.example.com* </span>
-   <span class="simpara"> *udp://www.example.com* </span>
-   <span class="simpara"> *ssl://www.example.com* </span>
-   <span class="simpara"> *sslv2://www.example.com* </span>
-   <span class="simpara"> *sslv3://www.example.com* </span>
-   <span class="simpara"> *tls://www.example.com* </span>

Internet 领域套接字在目标地址中还期望有一个端口号。在 <span
class="function">fsockopen</span>中在第二个参数中指定，这样就不会影响传输器的
URL。然而在 <span
class="function">stream\_socket\_client</span>和相关的函数中是用传统的
URL，端口号在传输器 URL 后面以冒号分隔而指定。

-   <span class="simpara"> *tcp://127.0.0.1:80* </span>
-   <span class="simpara"> *tcp://\[fe80::1\]:80* </span>
-   <span class="simpara"> *tcp://www.example.com:80* </span>

> **Note**: **带端口号的 IPv6 数字地址**  
> <span class="simpara">在上面的第二个例子中，IPv4
> 和主机名的例子只加了一个冒号和端口号，但 IPv6 的地址被放在方括号中：
> *\[fe80::1\]*。这是为了将 IPv6
> 地址中的冒号和用来分隔端口号的冒号区别开来。</span>

*ssl://*和 *tls://*传输器（仅在 openssl 支持已编译入 PHP 后可用）是
*tcp://*传输器加入 SSL 加密后的扩展。在 PHP 4.3.0 中 OpenSSL
支持必须被静态编译入 PHP，在 PHP 5.0.0 中可以编译为模块或者静态的。

*ssl://*将根据远程服务器的兼容性和参数设置尝试与之建立 SSL V2 或 SSL V3
链接 *sslv2://*和 *sslv3://*将明确的选择 SSL V2 或 SSL V3 协议进行连接。

| 名称                  | 用法                                                                                                                                | 默认值  |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------|
| *verify\_peer*        | &true; 或 &false;。用于 SSL 证书请求验证。                                                                                          | &false; |
| *allow\_self\_signed* | &true; 或 &false;。允许自签名的证书。                                                                                               | &false; |
| *cafile*              | 本地文件系统中证书授权机构文件的位置，应和 *verify\_peer*上下文选项一起使用来认证远端的身份。                                       |         |
| *capath*              | 如果没有指定 *cafile*或者如果该处没找到证书，则在 *capath*指定的目录中搜索相配的证书。 *capath*必须是一个正确的被散列化的证书目录。 |         |
| *local\_cert*         | 文件系统中本地证书文件的路径。必须是一个用 PEM 编码并包含你的证书和私人密钥的文件。可以选择包括发行者的证书链。                     |         |
| *passphrase*          | 你的 *local\_cert*文件编码的 passphrase。                                                                                           |         |
| *CN\_match*           | 所期待的 Common Name。PHP 能进行有限的通配符匹配。如果 Common Name 与此不匹配，连接尝试会失败。                                     |         |

> **Note**: <span class="simpara">因为 *ssl://*是
> <a href="/wrappers/http.html" class="link"><em>https://</em></a> 和
> <a href="/wrappers/ftp.html" class="link"><em>ftps://</em></a>
> 封装协议的底层传输器，适用于 *ssl://*的任何上下文选项也适用于
> *https://*和 *ftps://*。</span>
