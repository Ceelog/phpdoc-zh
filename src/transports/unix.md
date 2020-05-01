Unix 领域：Unix 和 UDG
----------------------

*unix://*自 PHP 3 起可用， *udg://*自 PHP 5 起可用。

-   <span class="simpara"> *unix:///tmp/mysock* </span>
-   <span class="simpara"> *udg:///tmp/mysock* </span>

*unix://*提供了在 Unix 域中对套接字流连接的访问。
*udg://*提供了替代的传输器以用户数据报协议（UDP）来访问 Unix 域套接字。

Unix 域套接字（UNIX Domain Socket），和 Internet Domain Socket
不同，不期望端口号。在 <span class="function">fsockopen</span>中
`portno`参数应被设为 0。
