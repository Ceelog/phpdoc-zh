套接字上下文选项
================

套接字上下文选项列表

### 说明

套接字上下文选项可用于所有工作在套接字上的封装协议，像 *tcp*, *http* 和
*ftp*.

### 可选项

`bindto`  
用户PHP访问网络的指定的IP地址（IPv4或IPv6其中的一个）和/或
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

### 更新日志

| 版本  | 说明             |
|-------|------------------|
| 5.1.0 | Added *bindto*.  |
| 5.3.3 | Added *backlog*. |

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
