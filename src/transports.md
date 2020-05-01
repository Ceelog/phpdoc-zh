所支持的套接字传输器（Socket Transports）列表
=============================================

**目录**

-   [Internet 领域：TCP，UDP，SSL 和 TLS](/transports/inet.html)
-   [Unix 领域：Unix 和 UDG](/transports/unix.html)

以下是 PHP 内置用于基于流的套接字函数例如 <span
class="function">fsockopen</span>和 <span
class="function">stream\_socket\_client</span>的各种 URL
风格的套接字传输器。这些传输器 *不适用*于
<a href="/ref/sockets.html" class="link">Sockets 扩展库</a>。

要得到自己的 PHP 版本中所安装的传输器列表，使用 <span
class="function">stream\_get\_transports</span>。
