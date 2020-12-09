SSL 上下文选项
==============

SSL 上下文选项清单

### 说明

*ssl://* 和 *tls://* 传输协议上下文选项清单。

### 可选项

`peer_name` <span class="type">string</span>  
要连接的服务器名称。如果未设置，那么服务器名称将根据打开 SSL
流的主机名称猜测得出。

`verify_peer` <span class="type">boolean</span>  
是否需要验证 SSL 证书。

默认值为 **`true`**。

`verify_peer_name` <span class="type">boolean</span>  
是否需要验证 peer name。

默认值为 **`true`**.

`allow_self_signed` <span class="type">boolean</span>  
是否允许自签名证书。需要配合
<a href="/context/ssl.html#context.ssl.verify-peer" class="link"><code class="parameter">verify_peer</code></a>
参数使用（注：当 verify\_peer 参数为 true 时才会根据 allow\_self\_signed
参数值来决定是否允许自签名证书）。

默认值为 **`false`**

`cafile` <span class="type">string</span>  
当设置 *verify\_peer* 为 true 时， 用来验证远端证书所用到的 CA 证书。
本选项值为 CA 证书在本地文件系统的全路径及文件名。

`capath` <span class="type">string</span>  
如果未设置 *cafile*，或者 *cafile* 所指的文件不存在时， 会在 *capath*
所指定的目录搜索适用的证书。 该目录必须是已经经过哈希处理的证书目录。
（注：所谓 hashed certificate 目录是指使用类似 c\_rehash 命令将目录中的
.pem 和 .crt
文件扫描并提取哈希码，然后根据此哈希码创建文件链接，以便于快速查找证书）

`local_cert` <span class="type">string</span>  
本地证书路径。 必须是 PEM 格式，并且包含本地的证书及私钥。
也可以包含证书颁发者证书链。 也可以通过 *local\_pk*
指定包含私钥的独立文件。

`local_pk` <span class="type">string</span>  
如果使用独立的文件来存储证书（*local\_cert*）和私钥，
那么使用此选项来指明私钥文件的路径。

`passphrase` <span class="type">string</span>  
*local\_cert* 文件的密码。

`CN_match` <span class="type">string</span>  
期望远端证书的 CN 名称。 PHP 会进行有限的通配符匹配， 如果服务器给出的
CN 名称和本地访问的名称不匹配，则视为连接失败。

> **Note**: <span class="simpara"> 在PHP 5.6.0中，这个选项已废弃，替换为
> `peer_name`。 </span>

`verify_depth` <span class="type">integer</span>  
如果证书链条层次太深，超过了本选项的设定值，则终止验证。

默认情况下不限制证书链条层次深度。

`ciphers` <span class="type">string</span>  
设置可用的密码列表。 可用的值参见：
<a href="https://www.openssl.org/docs/manmaster/man1/ciphers.html#CIPHER-LIST-FORMAT" class="link external">» ciphers(1)</a>。

默认值为 *DEFAULT*.

`capture_peer_cert` <span class="type">boolean</span>  
如果设置为 **`true`** 将会在上下文中创建 *peer\_certificate* 选项，
该选项中包含远端证书。

`capture_peer_cert_chain` <span class="type">boolean</span>  
如果设置为 **`true`** 将会在上下文中创建 *peer\_certificate\_chain*
选项， 该选项中包含远端证书链条。

`SNI_enabled` <span class="type">boolean</span>  
设置为 **`true`** 将启用服务器名称指示（server name indication）。 启用
SNI 将允许同一 IP 地址使用多个证书。

`SNI_server_name` <span class="type">string</span>  
如果设置此参数，那么其设置值将被视为 SNI 服务器名称。
如果未设置，那么服务器名称将基于打开 SSL 流的主机名称猜测得出。

> **Note**: <span class="simpara"> 在PHP 5.6.0中，这个选项已废弃，替换为
> `peer_name`。 </span>

`disable_compression` <span class="type">boolean</span>  
如果设置，则禁用 TLS 压缩，有助于减轻恶意攻击。

`peer_fingerprint` <span class="type">string</span> \| <span class="type">array</span>  
当远程服务器证书的摘要和指定的散列值不相同的时候， 终止操作。

当使用 <span class="type">string</span> 时，
会根据字符串的长度来检测所使用的散列算法：“md5”（32 字节）还是“sha1”（40
字节）。

当使用 <span class="type">array</span> 时，
数组的键表示散列算法名称，其对应的值是预期的摘要值。

### 更新日志

| 版本   | 说明                                                 |
|--------|------------------------------------------------------|
| 5.6.0  | 新加 `peer_fingerprint` 参数。                       |
| 5.4.13 | 新加 `disable_compression`。 需要 OpenSSL \>= 1.0.0. |
| 5.3.2  | 新加 `SNI_enabled` 和 `SNI_server_name`。            |

### 注释

> **Note**: <span class="simpara"> 因为 *ssl://* 是
> <a href="/wrappers/http.html" class="link"><em>https://</em></a> 和
> <a href="/wrappers/ftp.html" class="link"><em>ftps://</em></a>
> 的底层传输协议， 所以，*ssl://* 的上下文选项也同样适用于 *https://* 和
> *ftps://* 上下文。 </span>

> **Note**: <span class="simpara"> PHP 必须联合 OpenSSL 0.9.8j
> 或以上版本编译才可以支持 SNI， 同时也支持使用
> **`OPENSSL_TLSEXT_SERVER_NAME`** 来探测 SNI 服务器名称。 </span>

### 参见

-   <a href="/context/socket.html" class="xref">套接字上下文选项</a>
