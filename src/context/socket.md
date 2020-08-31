套接字上下文选项
================

套接字上下文选项列表

### 说明

套接字上下文选项可用于所有工作在套接字上的封装协议，像 *tcp*, *http* 和
*ftp*。

### 可选项

`bindto`  
用户 PHP 访问网络的指定的 IP 地址（IPv4 或 IPv6 其中的一个）和/或
端口号，这个语法是 *ip:port*. Setting the IP or the port to *0* will let
the system choose the IP and/or port.

> **Note**:
>
> As FTP creates two socket connections during normal operation, the
> port number cannot be specified using this option.

`backlog`  
Used to limit the number of outstanding connections in the socket's
listen queue.

> **Note**:
>
> This is only applicable to <span
> class="function">stream\_socket\_server</span>.

`ipv6_v6only`  
Overrides the OS default regarding mapping IPv4 into IPv6.

> **Note**:
>
> This is important in particular when trying to listen on IPv4
> addresses separately while there exists a binding on *\[::\]*.
>
> This is only applicable to <span
> class="function">stream\_socket\_server</span>.

`so_reuseport`  
Allows multiple bindings to a same ip:port pair, even from separate
processes.

> **Note**:
>
> This is only applicable to <span
> class="function">stream\_socket\_server</span>.

`so_broadcast`  
Enables sending and receiving data to/from broadcast addresses.

> **Note**:
>
> This is only applicable to <span
> class="function">stream\_socket\_server</span>.

`tcp_nodelay`  
Setting this option to **`TRUE`** will set *SOL\_TCP,NO\_DELAY=1*
appropriately, thus disabling the TCP Nagle algorithm.

### 更新日志

| 版本  | 说明                  |
|-------|-----------------------|
| 7.1.0 | Added `tcp_nodelay`.  |
| 7.0.1 | Added `ipv6_v6only`.  |
| 7.0.0 | Added `so_broadcast`. |
| 7.0.0 | Added `so_reuseport`. |
| 5.3.3 | Added `backlog`.      |
| 5.1.0 | Added *bindto*.       |

### 范例

**示例 \#1 Basic `bindto` usage example**

``` php
<?php
// connect to the internet using the '192.168.0.100' IP
$opts = array(
    'socket' => array(
        'bindto' => '192.168.0.100:0',
    ),
);


// connect to the internet using the '192.168.0.100' IP and port '7000'
$opts = array(
    'socket' => array(
        'bindto' => '192.168.0.100:7000',
    ),
);


// connect to the internet using the '2001:db8::1' IPv6 address
// and port '7000'
$opts = array(
    'socket' => array(
        'bindto' => '[2001:db8::1]:7000',
    ),
);


// connect to the internet using port '7000'
$opts = array(
    'socket' => array(
        'bindto' => '0:7000',
    ),
);


// create the context...
$context = stream_context_create($opts);

// ...and use it to fetch the data
echo file_get_contents('http://www.example.com', false, $context);

?>
```
