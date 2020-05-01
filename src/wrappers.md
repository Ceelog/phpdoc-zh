PHP 带有很多内置 URL 风格的封装协议，可用于类似 <span
class="function">fopen</span>、 <span class="function">copy</span>、
<span class="function">file\_exists</span> 和 <span
class="function">filesize</span> 的文件系统函数。
除了这些封装协议，还能通过 <span
class="function">stream\_wrapper\_register</span>
来注册自定义的封装协议。

> **Note**: <span class="simpara"> 用于描述一个封装协议的 URL 语法仅支持
> *scheme://...* 的语法。 *scheme:/* 和 *scheme:* 语法是不支持的。
> </span>

**目录**

-   [file://](/wrappers/file.html) — 访问本地文件系统
-   [http://](/wrappers/http.html) — 访问 HTTP(s) 网址
-   [ftp://](/wrappers/ftp.html) — 访问 FTP(s) URLs
-   [php://](/wrappers/php.html) — 访问各个输入/输出流（I/O streams）
-   [zlib://](/wrappers/compression.html) — 压缩流
-   [data://](/wrappers/data.html) — 数据（RFC 2397）
-   [glob://](/wrappers/glob.html) — 查找匹配的文件路径模式
-   [phar://](/wrappers/phar.html) — PHP 归档
-   [ssh2://](/wrappers/ssh2.html) — Secure Shell 2
-   [rar://](/wrappers/rar.html) — RAR
-   [ogg://](/wrappers/audio.html) — 音频流
-   [expect://](/wrappers/expect.html) — 处理交互式的流
