socket\_accept
==============

Accepts a connection on a socket

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_accept</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
)

After the socket `socket` has been created using <span
class="function">socket\_create</span>, bound to a name with <span
class="function">socket\_bind</span>, and told to listen for connections
with <span class="function">socket\_listen</span>, this function will
accept incoming connections on that socket. Once a successful connection
is made, a new socket resource is returned, which may be used for
communication. If there are multiple connections queued on the socket,
the first will be used. If there are no pending connections, <span
class="function">socket\_accept</span> will block until a connection
becomes present. If `socket` has been made non-blocking using <span
class="function">socket\_set\_blocking</span> or <span
class="function">socket\_set\_nonblock</span>, **`FALSE`** will be
returned.

The socket resource returned by <span
class="function">socket\_accept</span> may not be used to accept new
connections. The original listening socket `socket`, however, remains
open and may be reused.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span>.

### 返回值

Returns a new socket resource on success, or **`FALSE`** on error. The
actual error code can be retrieved by calling <span
class="function">socket\_last\_error</span>. This error code may be
passed to <span class="function">socket\_strerror</span> to get a
textual explanation of the error.

### 参见

-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_create</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_strerror</span>

socket\_addrinfo\_bind
======================

Create and bind to a socket from a given addrinfo

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_addrinfo\_bind</span> ( <span
class="methodparam"><span class="type">resource</span> `$addr`</span> )

Create a Socket resource, and bind it to the provided AddrInfo resource.
The return value of this function may be used with <span
class="function">socket\_listen</span>.

### 参数

`addr`  
Resource created from <span
class="function">socket\_addrinfo\_lookup</span>.

### 返回值

Returns a Socket resource on success or **`NULL`** on failure.

### 参见

-   <span class="function">socket\_addrinfo\_connect</span>
-   <span class="function">socket\_addrinfo\_explain</span>
-   <span class="function">socket\_addrinfo\_lookup</span>
-   <span class="function">socket\_listen</span>

socket\_addrinfo\_connect
=========================

Create and connect to a socket from a given addrinfo

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_addrinfo\_connect</span> ( <span
class="methodparam"><span class="type">resource</span> `$addr`</span> )

Create a Socket resource, and connect it to the provided AddrInfo
resource. The return value of this function may be used with the rest of
the socket functions.

### 参数

`addr`  
Resource created from <span
class="function">socket\_addrinfo\_lookup</span>

### 返回值

Returns a Socket resource on success or **`NULL`** on failure.

### 参见

-   <span class="function">socket\_addrinfo\_bind</span>
-   <span class="function">socket\_addrinfo\_explain</span>
-   <span class="function">socket\_addrinfo\_lookup</span>

socket\_addrinfo\_explain
=========================

Get information about addrinfo

### 说明

<span class="type">array</span> <span
class="methodname">socket\_addrinfo\_explain</span> ( <span
class="methodparam"><span class="type">resource</span> `$addr`</span> )

<span class="function">socket\_addrinfo\_explain</span> exposed the
underlying *addrinfo* structure.

### 参数

`addr`  
Resource created from <span
class="function">socket\_addrinfo\_lookup</span>

### 返回值

Returns an array containing the fields in the *addrinfo* structure.

### 参见

-   <span class="function">socket\_addrinfo\_bind</span>
-   <span class="function">socket\_addrinfo\_connect</span>
-   <span class="function">socket\_addrinfo\_lookup</span>

socket\_addrinfo\_lookup
========================

Get array with contents of getaddrinfo about the given hostname

### 说明

<span class="type">array</span> <span
class="methodname">socket\_addrinfo\_lookup</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$service`</span> \[, <span class="methodparam"><span
class="type">array</span> `$hints`</span> \]\] )

Lookup different ways we can connect to `host`. The returned array
contains a set of resources that we can bind to using <span
class="function">socket\_addrinfo\_bind</span>.

### 参数

`host`  
Hostname to search.

`service`  
The service to connect to. If service is a name, it is translated to the
corresponding port number.

`hints`  
Hints provide criteria for selecting addresses returned. You may specify
the hints as defined by getadrinfo.

### 返回值

Returns an array of AddrInfo resource handles that can be used with the
other socket\_addrinfo functions.

### 参见

-   <span class="function">socket\_addrinfo\_bind</span>
-   <span class="function">socket\_addrinfo\_connect</span>
-   <span class="function">socket\_addrinfo\_explain</span>

socket\_bind
============

给套接字绑定名字

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_bind</span> ( <span class="methodparam"><span
class="type">resource</span> `$socket`</span> , <span
class="methodparam"><span class="type">string</span> `$address`</span>
\[, <span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 0</span></span> \] )

绑定 `address` 到 `socket`。 该操作必须是在使用 <span
class="function">socket\_connect</span> 或者 <span
class="function">socket\_listen</span> 建立一个连接之前。

### 参数

`socket`  
用 <span class="function">socket\_create</span>
创建的一个有效的套接字资源。

`address`  
如果套接字是 **`AF_INET`** 族，那么 `address` 必须是一个四点分法的 IP
地址（例如 *127.0.0.1* ）。

如果套接字是 **`AF_UNIX`** 族，那么 `address` 是 Unix 套接字一部分（例如
`/tmp/my.sock` ）。

`port` （可选）  
参数 `port` 仅仅用于 **`AF_INET`**
套接字连接的时候，并且指定连接中需要监听的端口号。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

错误代码会传入 <span class="function">socket\_last\_error</span>
，如果将此参数传入 <span class="function">socket\_strerror</span>
则可以得到错误的文字说明。

### 范例

**示例 \#1 使用 <span class="function">socket\_bind</span>
来设置套接字资源地址**

``` php
<?php
// Create a new socket
$sock = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

// An example list of IP addresses owned by the computer
$sourceips['kevin']    = '127.0.0.1';
$sourceips['madcoder'] = '127.0.0.2';

// Bind the source address
socket_bind($sock, $sourceips['madcoder']);

// Connect to destination address
socket_connect($sock, '127.0.0.1', 80);

// Write
$request = 'GET / HTTP/1.1' . "\r\n" .
           'Host: example.com' . "\r\n\r\n";
socket_write($sock, $request);

// Close
socket_close($sock);

?>
```

### 注释

> **Note**:
>
> 该函数必须在 <span class="function">socket\_connect</span> 之前使用。

> **Note**:
>
> Windows 9x/ME 兼容性注意点:
> 如果尝试绑定套接字资源到一个错误的地址，而这个地址不是本机的地址，那么
> <span class="function">socket\_last\_error</span>
> 可能会返回一个无效的错误代码。

### 参见

-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_create</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_clear\_error
====================

清除套接字或者最后的错误代码上的错误

### 说明

<span class="type">void</span> <span
class="methodname">socket\_clear\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
\] )

这个函数清除给定的套接字上的错误代码或是最后一个全局的套接字如果套接字没有指定的话

这个函数允许明确的重置错误代码值
不论是一个套接字或者最后全局错误代码的扩展，
这对在检测应用的一部分是否有错误发生是十分有用的

### 参数

`socket`  
用<span class="function">socket\_create</span>创建的有效的套接字资源。

### 返回值

没有返回值。

### 参见

-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_close
=============

关闭套接字资源

### 说明

<span class="type">void</span> <span
class="methodname">socket\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
)

<span class="function">socket\_close</span> 会关闭掉给定的 `socket`
资源。 这个函数只针对套接字资源有效，不能用在其他类型的资源类型上。

### 参数

`socket`  
由 <span class="function">socket\_create</span> 或者是 <span
class="function">socket\_accept</span> 创建的有效的套接字资源。

### 返回值

没有返回值。

### 参见

-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_create</span>
-   <span class="function">socket\_strerror</span>

socket\_cmsg\_space
===================

Calculate message buffer size

### 说明

<span class="type">int</span> <span
class="methodname">socket\_cmsg\_space</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span>
\[, <span class="methodparam"><span class="type">int</span> `$n`<span
class="initializer"> = 0</span></span> \] )

Calculates the size of the buffer that should be allocated for receiving
the ancillary data.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`level`  

`type`  

### 返回值

### 参见

-   <span class="function">socket\_recvmsg</span>
-   <span class="function">socket\_sendmsg</span>

socket\_connect
===============

开启一个套接字连接

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_connect</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`$address`</span> \[, <span class="methodparam"><span
class="type">int</span> `$port`<span class="initializer"> =
0</span></span> \] )

用 <span class="function">socket\_create</span>
创建的有效的套接字资源来连接到 `address` 。

### 参数

`socket`  

`address`  
如果参数 `socket` 是 **`AF_INET`** ， 那么参数 `address`
则可以是一个点分四组表示法（例如 *127.0.0.1* ） 的 IPv4 地址； 如果支持
IPv6 并且 `socket` 是 **`AF_INET6`**，那么 `address` 也可以是有效的 IPv6
地址（例如 *::1*）；如果套接字类型为 **`AF_UNIX`** ，那么 `address`
也可以是一个Unix 套接字。

`port`  
参数 `port` 仅仅用于 **`AF_INET`** 和 **`AF_INET6`**
套接字连接的时候，并且是在此情况下是需要强制说明连接对应的远程服务器上的端口号。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 错误代码会传入
<span class="function">socket\_last\_error</span> ，如果将此参数传入
<span class="function">socket\_strerror</span>
则可以得到错误的文字说明。

> **Note**:
>
> If the socket is non-blocking then this function returns **`FALSE`**
> with an error *Operation now in progress*.

### 参见

-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_create</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_create\_listen
======================

Opens a socket on port to accept connections

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_create\_listen</span> ( <span
class="methodparam"><span class="type">int</span> `$port`</span> \[,
<span class="methodparam"><span class="type">int</span> `$backlog`<span
class="initializer"> = 128</span></span> \] )

<span class="function">socket\_create\_listen</span> creates a new
socket resource of type **`AF_INET`** listening on *all* local
interfaces on the given port waiting for new connections.

This function is meant to ease the task of creating a new socket which
only listens to accept new connections.

### 参数

`port`  
The port on which to listen on all interfaces.

`backlog`  
The `backlog` parameter defines the maximum length the queue of pending
connections may grow to. **`SOMAXCONN`** may be passed as `backlog`
parameter, see <span class="function">socket\_listen</span> for more
information.

### 返回值

<span class="function">socket\_create\_listen</span> returns a new
socket resource on success or **`FALSE`** on error. The error code can
be retrieved with <span class="function">socket\_last\_error</span>.
This code may be passed to <span
class="function">socket\_strerror</span> to get a textual explanation of
the error.

### 注释

> **Note**:
>
> If you want to create a socket which only listens on a certain
> interface you need to use <span
> class="function">socket\_create</span>, <span
> class="function">socket\_bind</span> and <span
> class="function">socket\_listen</span>.

### 参见

-   <span class="function">socket\_create</span>
-   <span class="function">socket\_create\_pair</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_create\_pair
====================

Creates a pair of indistinguishable sockets and stores them in an array

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_create\_pair</span> ( <span
class="methodparam"><span class="type">int</span> `$domain`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> ,
<span class="methodparam"><span class="type">int</span>
`$protocol`</span> , <span class="methodparam"><span
class="type">array</span> `&$fd`</span> )

<span class="function">socket\_create\_pair</span> creates two connected
and indistinguishable sockets, and stores them in `fd`. This function is
commonly used in IPC (InterProcess Communication).

### 参数

`domain`  
The `domain` parameter specifies the protocol family to be used by the
socket. See <span class="function">socket\_create</span> for the full
list.

`type`  
The `type` parameter selects the type of communication to be used by the
socket. See <span class="function">socket\_create</span> for the full
list.

`protocol`  
The `protocol` parameter sets the specific protocol within the specified
`domain` to be used when communicating on the returned socket. The
proper value can be retrieved by name by using <span
class="function">getprotobyname</span>. If the desired protocol is TCP,
or UDP the corresponding constants **`SOL_TCP`**, and **`SOL_UDP`** can
also be used.

See <span class="function">socket\_create</span> for the full list of
supported protocols.

`fd`  
Reference to an array in which the two socket resources will be
inserted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.3.0 | This function is now available on Windows platforms. |

### 范例

**示例 \#1 <span class="function">socket\_create\_pair</span> example**

``` php
<?php
$sockets = array();

/* On Windows we need to use AF_INET */
$domain = (strtoupper(substr(PHP_OS, 0, 3)) == 'WIN' ? AF_INET : AF_UNIX);

/* Setup socket pair */
if (socket_create_pair($domain, SOCK_STREAM, 0, $sockets) === false) {
    echo "socket_create_pair failed. Reason: ".socket_strerror(socket_last_error());
}
/* Send and Receive Data */
if (socket_write($sockets[0], "ABCdef123\n", strlen("ABCdef123\n")) === false) {
    echo "socket_write() failed. Reason: ".socket_strerror(socket_last_error($sockets[0]));
}
if (($data = socket_read($sockets[1], strlen("ABCdef123\n"), PHP_BINARY_READ)) === false) {
    echo "socket_read() failed. Reason: ".socket_strerror(socket_last_error($sockets[1]));
}
var_dump($data);

/* Close sockets */
socket_close($sockets[0]);
socket_close($sockets[1]);
?>
```

**示例 \#2 <span class="function">socket\_create\_pair</span> IPC
example**

``` php
<?php
$ary = array();
$strone = 'Message From Parent.';
$strtwo = 'Message From Child.';

if (socket_create_pair(AF_UNIX, SOCK_STREAM, 0, $ary) === false) {
    echo "socket_create_pair() failed. Reason: ".socket_strerror(socket_last_error());
}
$pid = pcntl_fork();
if ($pid == -1) {
    echo 'Could not fork Process.';
} elseif ($pid) {
    /*parent*/
    socket_close($ary[0]);
    if (socket_write($ary[1], $strone, strlen($strone)) === false) {
        echo "socket_write() failed. Reason: ".socket_strerror(socket_last_error($ary[1]));
    }
    if (socket_read($ary[1], strlen($strtwo), PHP_BINARY_READ) == $strtwo) {
        echo "Received $strtwo\n";
    }
    socket_close($ary[1]);
} else {
    /*child*/
    socket_close($ary[1]);
    if (socket_write($ary[0], $strtwo, strlen($strtwo)) === false) {
        echo "socket_write() failed. Reason: ".socket_strerror(socket_last_error($ary[0]));
    }
    if (socket_read($ary[0], strlen($strone), PHP_BINARY_READ) == $strone) {
        echo "Received $strone\n";
    }
    socket_close($ary[0]);
}
?>
```

### 参见

-   <span class="function">socket\_create</span>
-   <span class="function">socket\_create\_listen</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_create
==============

创建一个套接字（通讯节点）

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_create</span> ( <span
class="methodparam"><span class="type">int</span> `$domain`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> ,
<span class="methodparam"><span class="type">int</span>
`$protocol`</span> )

创建并返回一个套接字，也称作一个通讯节点。一个典型的网络连接由 2
个套接字构成，一个运行在客户端，另一个运行在服务器端。

### 参数

`domain`  
`domain` 参数指定哪个协议用在当前套接字上。

| Domain         | 描述                                                   |
|----------------|--------------------------------------------------------|
| **`AF_INET`**  | IPv4 网络协议。TCP 和 UDP 都可使用此协议。             |
| **`AF_INET6`** | IPv6 网络协议。TCP 和 UDP 都可使用此协议。             |
| **`AF_UNIX`**  | 本地通讯协议。具有高性能和低成本的 IPC（进程间通讯）。 |

`type`  
`type` 参数用于选择套接字使用的类型。

| 类型                 | 描述                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------------------------------------------|
| **`SOCK_STREAM`**    | 提供一个顺序化的、可靠的、全双工的、基于连接的字节流。支持数据传送流量控制机制。TCP 协议即基于这种流式套接字。          |
| **`SOCK_DGRAM`**     | 提供数据报文的支持。(无连接，不可靠、固定最大长度).UDP协议即基于这种数据报文套接字。                                    |
| **`SOCK_SEQPACKET`** | 提供一个顺序化的、可靠的、全双工的、面向连接的、固定最大长度的数据通信；数据端通过接收每一个数据段来读取整个数据包。    |
| **`SOCK_RAW`**       | 提供读取原始的网络协议。这种特殊的套接字可用于手工构建任意类型的协议。一般使用这个套接字来实现 ICMP 请求（例如 ping）。 |
| **`SOCK_RDM`**       | 提供一个可靠的数据层，但不保证到达顺序。一般的操作系统都未实现此功能。                                                  |

`protocol`  
`protocol` 参数，是设置指定 `domain` 套接字下的具体协议。这个值可以使用
<span class="function">getprotobyname</span>
函数进行读取。如果所需的协议是 TCP 或 UDP，可以直接使用常量
**`SOL_TCP`** 和 **`SOL_UDP`** 。

| 名称 | 描述                                                                                                                                                                                                                                                                                                                 |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| icmp | Internet Control Message Protocol 主要用于网关和主机报告错误的数据通信。例如“ping”命令（在目前大部分的操作系统中）就是使用 ICMP 协议实现的。                                                                                                                                                                         |
| udp  | User Datagram Protocol 是一个无连接的、不可靠的、具有固定最大长度的报文协议。由于这些特性，UDP 协议拥有最小的协议开销。                                                                                                                                                                                              |
| tcp  | Transmission Control Protocol 是一个可靠的、基于连接的、面向数据流的全双工协议。TCP 能够保障所有的数据包是按照其发送顺序而接收的。如果任意数据包在通讯时丢失，TCP 将自动重发数据包直到目标主机应答已接收。因为可靠性和性能的原因，TCP 在数据传输层使用 8bit 字节边界。因此，TCP 应用程序必须允许传送部分报文的可能。 |

### 返回值

<span class="function">socket\_create</span>
正确时返回一个套接字，失败时返回 **`FALSE`**。要读取错误代码，可以调用
<span class="function">socket\_last\_error</span>。这个错误代码可以通过
<span class="function">socket\_strerror</span> 读取文字的错误说明。

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 5.0.0 | 增加 **`AF_INET6`** 支持。 |

### 错误／异常

如果使用一个无效的 `domain` 或 `type`，<span
class="function">socket\_create</span> 会使用 **`AF_INET`** 和
**`SOCK_STREAM`** 替代无效参数，同时会发出 **`E_WARNING`** 警告信息。

### 参见

-   <span class="function">socket\_accept</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_export\_stream
======================

Export a socket extension resource into a stream that encapsulates a
socket

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_export\_stream</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`socket`  

### 返回值

Return resource 或者在失败时返回 **`FALSE`**.

socket\_get\_option
===================

Gets socket options for the socket

### 说明

<span class="type">mixed</span> <span
class="methodname">socket\_get\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">int</span>
`$level`</span> , <span class="methodparam"><span
class="type">int</span> `$optname`</span> )

The <span class="function">socket\_get\_option</span> function retrieves
the value for the option specified by the `optname` parameter for the
specified `socket`.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

`level`  
The `level` parameter specifies the protocol level at which the option
resides. For example, to retrieve options at the socket level, a `level`
parameter of **`SOL_SOCKET`** would be used. Other levels, such as
**`TCP`**, can be used by specifying the protocol number of that level.
Protocol numbers can be found by using the <span
class="function">getprotobyname</span> function.

`optname`  
<table>
<caption><strong>Available Socket Options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
<th>Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>SO_DEBUG</code></strong></td>
<td>Reports whether debugging information is being recorded.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>SO_BROADCAST</code></strong></td>
<td>Reports whether transmission of broadcast messages is supported.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="odd">
<td><strong><code>SO_REUSEADDR</code></strong></td>
<td>Reports whether local addresses can be reused.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>SO_REUSEPORT</code></strong></td>
<td>Reports whether local ports can be reused.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="odd">
<td><strong><code>SO_KEEPALIVE</code></strong></td>
<td>Reports whether connections are kept active with periodic transmission of messages. If the connected socket fails to respond to these messages, the connection is broken and processes writing to that socket are notified with a SIGPIPE signal.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>SO_LINGER</code></strong></td>
<td><p>Reports whether the <code class="parameter">socket</code> lingers on <span class="function">socket_close</span> if data is present. By default, when the socket is closed, it attempts to send all unsent data. In the case of a connection-oriented socket, <span class="function">socket_close</span> will wait for its peer to acknowledge the data.</p>
<p>If <var class="varname">l_onoff</var> is non-zero and <var class="varname">l_linger</var> is zero, all the unsent data will be discarded and RST (reset) is sent to the peer in the case of a connection-oriented socket.</p>
<p>On the other hand, if <var class="varname">l_onoff</var> is non-zero and <var class="varname">l_linger</var> is non-zero, <span class="function">socket_close</span> will block until all the data is sent or the time specified in <var class="varname">l_linger</var> elapses. If the socket is non-blocking, <span class="function">socket_close</span> will fail and return an error.</p></td>
<td><span class="type">array</span>. The array will contain two keys: <var class="varname">l_onoff</var> and <var class="varname">l_linger</var>.</td>
</tr>
<tr class="odd">
<td><strong><code>SO_OOBINLINE</code></strong></td>
<td>Reports whether the <code class="parameter">socket</code> leaves out-of-band data inline.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>SO_SNDBUF</code></strong></td>
<td>Reports the size of the send buffer.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="odd">
<td><strong><code>SO_RCVBUF</code></strong></td>
<td>Reports the size of the receive buffer.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>SO_ERROR</code></strong></td>
<td>Reports information about error status and clears it.</td>
<td><span class="type">int</span> (cannot be set by <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="odd">
<td><strong><code>SO_TYPE</code></strong></td>
<td>Reports the <code class="parameter">socket</code> type (e.g. <strong><code>SOCK_STREAM</code></strong>).</td>
<td><span class="type">int</span> (cannot be set by <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="even">
<td><strong><code>SO_DONTROUTE</code></strong></td>
<td>Reports whether outgoing messages bypass the standard routing facilities.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="odd">
<td><strong><code>SO_RCVLOWAT</code></strong></td>
<td>Reports the minimum number of bytes to process for <code class="parameter">socket</code> input operations.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>SO_RCVTIMEO</code></strong></td>
<td>Reports the timeout value for input operations.</td>
<td><span class="type">array</span>. The array will contain two keys: <var class="varname">sec</var> which is the seconds part on the timeout value and <var class="varname">usec</var> which is the microsecond part of the timeout value.</td>
</tr>
<tr class="odd">
<td><strong><code>SO_SNDTIMEO</code></strong></td>
<td>Reports the timeout value specifying the amount of time that an output function blocks because flow control prevents data from being sent.</td>
<td><span class="type">array</span>. The array will contain two keys: <var class="varname">sec</var> which is the seconds part on the timeout value and <var class="varname">usec</var> which is the microsecond part of the timeout value.</td>
</tr>
<tr class="even">
<td><strong><code>SO_SNDLOWAT</code></strong></td>
<td>Reports the minimum number of bytes to process for <code class="parameter">socket</code> output operations.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="odd">
<td><strong><code>TCP_NODELAY</code></strong></td>
<td>Reports whether the Nagle TCP algorithm is disabled.</td>
<td><span class="type">int</span></td>
</tr>
<tr class="even">
<td><strong><code>MCAST_JOIN_GROUP</code></strong></td>
<td>Joins a multicast group. (added in PHP 5.4)</td>
<td><span class="type">array</span> with keys <em>"group"</em>, specifying a <span class="type">string</span> with an IPv4 or IPv6 multicast address and <em>"interface"</em>, specifying either an interface number (type <span class="type">int</span>) or a <em>string</em> with the interface name, like <em>"eth0"</em>. <em>0</em> can be specified to indicate the interface should be selected using routing rules. (can only be used in <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="odd">
<td><strong><code>MCAST_LEAVE_GROUP</code></strong></td>
<td>Leaves a multicast group. (added in PHP 5.4)</td>
<td><span class="type">array</span>. See <strong><code>MCAST_JOIN_GROUP</code></strong> for more information. (can only be used in <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="even">
<td><strong><code>MCAST_BLOCK_SOURCE</code></strong></td>
<td>Blocks packets arriving from a specific source to a specific multicast group, which must have been previously joined. (added in PHP 5.4)</td>
<td><span class="type">array</span> with the same keys as <strong><code>MCAST_JOIN_GROUP</code></strong>, plus one extra key, <em>source</em>, which maps to a <span class="type">string</span> specifying an IPv4 or IPv6 address of the source to be blocked. (can only be used in <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="odd">
<td><strong><code>MCAST_UNBLOCK_SOURCE</code></strong></td>
<td>Unblocks (start receiving again) packets arriving from a specific source address to a specific multicast group, which must have been previously joined. (added in PHP 5.4)</td>
<td><span class="type">array</span> with the same format as <strong><code>MCAST_BLOCK_SOURCE</code></strong>. (can only be used in <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="even">
<td><strong><code>MCAST_JOIN_SOURCE_GROUP</code></strong></td>
<td>Receive packets destined to a specific multicast group whose source address matches a specific value. (added in PHP 5.4)</td>
<td><span class="type">array</span> with the same format as <strong><code>MCAST_BLOCK_SOURCE</code></strong>. (can only be used in <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="odd">
<td><strong><code>MCAST_LEAVE_SOURCE_GROUP</code></strong></td>
<td>Stop receiving packets destined to a specific multicast group whose source address matches a specific value. (added in PHP 5.4)</td>
<td><span class="type">array</span> with the same format as <strong><code>MCAST_BLOCK_SOURCE</code></strong>. (can only be used in <span class="function">socket_set_option</span>)</td>
</tr>
<tr class="even">
<td><strong><code>IP_MULTICAST_IF</code></strong></td>
<td>The outgoing interface for IPv4 multicast packets. (added in PHP 5.4)</td>
<td>Either <span class="type">int</span> specifying the interface number or a <span class="type">string</span> with an interface name, like <em>eth0</em>. The value <span class="type">0</span> can be used to indicate the routing table is to used in the interface selection. The function <span class="function">socket_get_option</span> returns an interface index. Note that, unlike the C API, this option does NOT take an IP address. This eliminates the interface difference between <strong><code>IP_MULTICAST_IF</code></strong> and <strong><code>IPV6_MULTICAST_IF</code></strong>.</td>
</tr>
<tr class="odd">
<td><strong><code>IPV6_MULTICAST_IF</code></strong></td>
<td>The outgoing interface for IPv6 multicast packets. (added in PHP 5.4)</td>
<td>The same as <strong><code>IP_MULTICAST_IF</code></strong>.</td>
</tr>
<tr class="even">
<td><strong><code>IP_MULTICAST_LOOP</code></strong></td>
<td>The multicast loopback policy for IPv4 packets, which determines whether multicast packets sent by this socket also reach receivers in the same host that have joined the same multicast group on the outgoing interface used by this socket. This is the case by default. (added in PHP 5.4)</td>
<td><span class="type">int</span> (either <em>0</em> or <em>1</em>). For <span class="function">socket_set_option</span> any value will be accepted and will be converted to a boolean following the usual PHP rules.</td>
</tr>
<tr class="odd">
<td><strong><code>IPV6_MULTICAST_LOOP</code></strong></td>
<td>Analogous to <strong><code>IP_MULTICAST_LOOP</code></strong>, but for IPv6. (added in PHP 5.4)</td>
<td><span class="type">int</span>. See <strong><code>IP_MULTICAST_LOOP</code></strong>.</td>
</tr>
<tr class="even">
<td><strong><code>IP_MULTICAST_TTL</code></strong></td>
<td>The time-to-live of outgoing IPv4 multicast packets. This should be a value between 0 (don't leave the interface) and 255. The default value is 1 (only the local network is reached). (added in PHP 5.4)</td>
<td><span class="type">int</span> between 0 and 255.</td>
</tr>
<tr class="odd">
<td><strong><code>IPV6_MULTICAST_HOPS</code></strong></td>
<td>Analogous to <strong><code>IP_MULTICAST_TTL</code></strong>, but for IPv6 packets. The value -1 is also accepted, meaning the route default should be used. (added in PHP 5.4)</td>
<td><span class="type">int</span> between -1 and 255.</td>
</tr>
</tbody>
</table>

### 返回值

Returns the value of the given option, or **`FALSE`** on errors.

### 范例

**示例 \#1 <span class="function">socket\_get\_option</span> example**

``` php
<?php
$socket = socket_create_listen(1223);

$linger = array('l_linger' => 1, 'l_onoff' => 1);
socket_set_option($socket, SOL_SOCKET, SO_LINGER, $linger);

var_dump(socket_get_option($socket, SOL_SOCKET, SO_REUSEADDR));
?>
```

### 参见

-   <span class="function">socket\_create\_listen</span>
-   <span class="function">socket\_set\_option</span>

socket\_getopt
==============

别名 <span class="function">socket\_get\_option</span>

### 说明

此函数是该函数的别名： <span
class="function">socket\_get\_option</span>.

socket\_getpeername
===================

Queries the remote side of the given socket which may either result in
host/port or in a Unix filesystem path, dependent on its type

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_getpeername</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`&$address`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$port`</span> \] )

Queries the remote side of the given socket which may either result in
host/port or in a Unix filesystem path, dependent on its type.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

`address`  
If the given socket is of type **`AF_INET`** or **`AF_INET6`**, <span
class="function">socket\_getpeername</span> will return the peers
(remote) *IP address* in appropriate notation (e.g. *127.0.0.1* or
*fe80::1*) in the `address` parameter and, if the optional `port`
parameter is present, also the associated port.

If the given socket is of type **`AF_UNIX`**, <span
class="function">socket\_getpeername</span> will return the Unix
filesystem path (e.g. */var/run/daemon.sock*) in the `address`
parameter.

`port`  
If given, this will hold the port associated to `address`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 <span
class="function">socket\_getpeername</span> may also return **`FALSE`**
if the socket type is not any of **`AF_INET`**, **`AF_INET6`**, or
**`AF_UNIX`**, in which case the last socket error code is *not*
updated.

### 注释

> **Note**:
>
> <span class="function">socket\_getpeername</span> should not be used
> with **`AF_UNIX`** sockets created with <span
> class="function">socket\_accept</span>. Only sockets created with
> <span class="function">socket\_connect</span> or a primary server
> socket following a call to <span class="function">socket\_bind</span>
> will return meaningful values.

> **Note**:
>
> For having <span class="function">socket\_getpeername</span> to return
> a meaningful value, the socket it is applied upon must of course be
> one for which the concept of "peer" makes sense.

### 参见

-   <span class="function">socket\_getsockname</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_getsockname
===================

Queries the local side of the given socket which may either result in
host/port or in a Unix filesystem path, dependent on its type

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_getsockname</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`&$addr`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$port`</span> \] )

> **Note**: <span class="simpara"> <span
> class="function">socket\_getsockname</span> should not be used with
> **`AF_UNIX`** sockets created with <span
> class="function">socket\_connect</span>. Only sockets created with
> <span class="function">socket\_accept</span> or a primary server
> socket following a call to <span class="function">socket\_bind</span>
> will return meaningful values. </span>

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

`addr`  
If the given socket is of type **`AF_INET`** or **`AF_INET6`**, <span
class="function">socket\_getsockname</span> will return the local *IP
address* in appropriate notation (e.g. *127.0.0.1* or *fe80::1*) in the
`address` parameter and, if the optional `port` parameter is present,
also the associated port.

If the given socket is of type **`AF_UNIX`**, <span
class="function">socket\_getsockname</span> will return the Unix
filesystem path (e.g. */var/run/daemon.sock*) in the `address`
parameter.

`port`  
If provided, this will hold the associated port.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 <span
class="function">socket\_getsockname</span> may also return **`FALSE`**
if the socket type is not any of **`AF_INET`**, **`AF_INET6`**, or
**`AF_UNIX`**, in which case the last socket error code is *not*
updated.

### 参见

-   <span class="function">socket\_getpeername</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_import\_stream
======================

Import a stream

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_import\_stream</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
)

Imports a stream that encapsulates a socket into a socket extension
resource.

### 参数

`stream`  
The stream resource to import.

### 返回值

Returns **`FALSE`** or **`NULL`** on failure.

### 范例

**示例 \#1 <span class="function">socket\_import\_stream</span>
example**

``` php
<?php
$stream = stream_socket_server("udp://0.0.0.0:58380", $errno, $errstr, STREAM_SERVER_BIND); 
$sock   = socket_import_stream($stream);
?>
```

### 参见

-   <span class="function">stream\_socket\_server</span>

socket\_last\_error
===================

Returns the last error on the socket

### 说明

<span class="type">int</span> <span
class="methodname">socket\_last\_error</span> (\[ <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
\] )

If a socket resource is passed to this function, the last error which
occurred on this particular socket is returned. If the socket resource
is omitted, the error code of the last failed socket function is
returned. The latter is particularly helpful for functions like <span
class="function">socket\_create</span> which don't return a socket on
failure and <span class="function">socket\_select</span> which can fail
for reasons not directly tied to a particular socket. The error code is
suitable to be fed to <span class="function">socket\_strerror</span>
which returns a string describing the given error code.

If no error had occurred, or the error had been cleared with <span
class="function">socket\_clear\_error</span>, the function returns *0*.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span>.

### 返回值

This function returns a socket error code.

### 范例

**示例 \#1 <span class="function">socket\_last\_error</span> example**

``` php
<?php
$socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if ($socket === false) {
    $errorcode = socket_last_error();
    $errormsg = socket_strerror($errorcode);
    
    die("Couldn't create socket: [$errorcode] $errormsg");
}
?>
```

### 注释

> **Note**:
>
> <span class="function">socket\_last\_error</span> does not clear the
> error code, use <span class="function">socket\_clear\_error</span> for
> this purpose.

socket\_listen
==============

Listens for a connection on a socket

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_listen</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$backlog`<span class="initializer"> = 0</span></span> \] )

After the socket `socket` has been created using <span
class="function">socket\_create</span> and bound to a name with <span
class="function">socket\_bind</span>, it may be told to listen for
incoming connections on `socket`.

<span class="function">socket\_listen</span> is applicable only to
sockets of type **`SOCK_STREAM`** or **`SOCK_SEQPACKET`**.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_addrinfo\_bind</span>

`backlog`  
A maximum of `backlog` incoming connections will be queued for
processing. If a connection request arrives with the queue full the
client may receive an error with an indication of *ECONNREFUSED*, or, if
the underlying protocol supports retransmission, the request may be
ignored so that retries may succeed.

> **Note**:
>
> The maximum number passed to the `backlog` parameter highly depends on
> the underlying platform. On Linux, it is silently truncated to
> **`SOMAXCONN`**. On win32, if passed **`SOMAXCONN`**, the underlying
> service provider responsible for the socket will set the backlog to a
> maximum *reasonable* value. There is no standard provision to find out
> the actual backlog value on this platform.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 The error code
can be retrieved with <span class="function">socket\_last\_error</span>.
This code may be passed to <span
class="function">socket\_strerror</span> to get a textual explanation of
the error.

### 参见

-   <span class="function">socket\_accept</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_create</span>
-   <span class="function">socket\_strerror</span>
-   <span class="function">socket\_addrinfo\_bind</span>

socket\_read
============

Reads a maximum of length bytes from a socket

### 说明

<span class="type">string</span> <span
class="methodname">socket\_read</span> ( <span class="methodparam"><span
class="type">resource</span> `$socket`</span> , <span
class="methodparam"><span class="type">int</span> `$length`</span> \[,
<span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = PHP\_BINARY\_READ</span></span> \] )

The function <span class="function">socket\_read</span> reads from the
socket resource `socket` created by the <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span> functions.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

`length`  
The maximum number of bytes read is specified by the `length` parameter.
Otherwise you can use **`\r`**, **`\n`**, or **`\0`** to end reading
(depending on the `type` parameter, see below).

`type`  
Optional `type` parameter is a named constant:

-   <span class="simpara"> **`PHP_BINARY_READ`** (Default) - use the
    system *recv()* function. Safe for reading binary data. </span>
-   <span class="simpara"> **`PHP_NORMAL_READ`** - reading stops at
    *\\n* or *\\r*. </span>

### 返回值

<span class="function">socket\_read</span> returns the data as a string
on success, or **`FALSE`** on error (including if the remote host has
closed the connection). The error code can be retrieved with <span
class="function">socket\_last\_error</span>. This code may be passed to
<span class="function">socket\_strerror</span> to get a textual
representation of the error.

> **Note**:
>
> <span class="function">socket\_read</span> returns a zero length
> string ("") when there is no more data to read.

### 参见

-   <span class="function">socket\_accept</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>
-   <span class="function">socket\_write</span>

socket\_recv
============

从已连接的socket接收数据

### 说明

<span class="type">int</span> <span
class="methodname">socket\_recv</span> ( <span class="methodparam"><span
class="type">resource</span> `$socket`</span> , <span
class="methodparam"><span class="type">string</span> `&$buf`</span> ,
<span class="methodparam"><span class="type">int</span> `$len`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
)

函数 <span class="function">socket\_recv</span> 从 `socket` 中接受长度为
`len` 字节的数据，并保存在 `buf` 中。 <span
class="function">socket\_recv</span>
用于从已连接的socket中接收数据。除此之外，可以设定一个或多个 flags
来控制函数的具体行为。

`buf` 以引用形式传递，因此必须是一个以声明的有效的变量。从 `socket`
中接收到的数据将会保存在 `buf` 中。

### 参数

`socket`  
参数 `socket` 必须是一个由 <span class="function">socket\_create</span>
创建的socket资源。

`buf`  
从socket中获取的数据将被保存在由 `buf` 制定的变量中。
如果有错误发生，如链接被重置，数据不可用等等， `buf` 将被设为
**`NULL`**。

`len`  
长度最多为 `len` 字节的数据将被接收。

`flags`  
`flags` 的值可以为下列任意flag的组合。使用按位或运算符(*\|*)来
组合不同的flag。

| Flag               | 描述                                                                                                                                                           |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`MSG_OOB`**      | 处理超出边界的数据                                                                                                                                             |
| **`MSG_PEEK`**     | 从接受队列的起始位置接收数据，但不将他们从接受队列中移除。                                                                                                     |
| **`MSG_WAITALL`**  | 在接收到至少 `len` 字节的数据之前，造成一个阻塞，并暂停脚本运行（block）。但是， 如果接收到中断信号，或远程服务器断开连接，该函数将返回少于 `len` 字节的数据。 |
| **`MSG_DONTWAIT`** | 如果制定了该flag，函数将不会造成阻塞，即使在全局设置中指定了阻塞设置。                                                                                         |

### 返回值

<span class="function">socket\_recv</span>
返回一个数字，表示接收到的字节数。如果发生了错误，则返回 **`FALSE`**
错误码可使用 <span class="function">socket\_last\_error</span>
接收。也可使用函数 <span class="function">socket\_strerror</span>
来取得关于错误的文字描述。

### 范例

**示例 \#1 <span class="function">socket\_recv</span> 范例**

该范例简单地使用 <span class="function">socket\_recv</span> 重写了
<a href="/sockets/examples.html" class="xref">范例</a> 中的 第一个例子。

``` php
<?php
error_reporting(E_ALL);

echo "<h2>TCP/IP Connection</h2>\n";

/* Get the port for the WWW service. */
$service_port = getservbyname('www', 'tcp');

/* Get the IP address for the target host. */
$address = gethostbyname('www.example.com');

/* Create a TCP/IP socket. */
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
if ($socket === false) {
    echo "socket_create() failed: reason: " . socket_strerror(socket_last_error()) . "\n";
} else {
    echo "OK.\n";
}

echo "Attempting to connect to '$address' on port '$service_port'...";
$result = socket_connect($socket, $address, $service_port);
if ($result === false) {
    echo "socket_connect() failed.\nReason: ($result) " . socket_strerror(socket_last_error($socket)) . "\n";
} else {
    echo "OK.\n";
}

$in = "HEAD / HTTP/1.1\r\n";
$in .= "Host: www.example.com\r\n";
$in .= "Connection: Close\r\n\r\n";
$out = '';

echo "Sending HTTP HEAD request...";
socket_write($socket, $in, strlen($in));
echo "OK.\n";

echo "Reading response:\n\n";
$buf = 'This is my buffer.';
if (false !== ($bytes = socket_recv($socket, $buf, 2048, MSG_WAITALL))) {
    echo "Read $bytes bytes from socket_recv(). Closing socket...";
} else {
    echo "socket_recv() failed; reason: " . socket_strerror(socket_last_error($socket)) . "\n";
}
socket_close($socket);

echo $buf . "\n";
echo "OK.\n\n";
?>
```

The above example will produce something like:

    <h2>TCP/IP Connection</h2>
    OK.
    Attempting to connect to '208.77.188.166' on port '80'...OK.
    Sending HTTP HEAD request...OK.
    Reading response:

    Read 123 bytes from socket_recv(). Closing socket...HTTP/1.1 200 OK
    Date: Mon, 14 Sep 2009 08:56:36 GMT
    Server: Apache/2.2.3 (Red Hat)
    Last-Modified: Tue, 15 Nov 2005 13:24:10 GMT
    ETag: "b80f4-1b6-80bfd280"
    Accept-Ranges: bytes
    Content-Length: 438
    Connection: close
    Content-Type: text/html; charset=UTF-8

    OK.

socket\_recvfrom
================

Receives data from a socket whether or not it is connection-oriented

### 说明

<span class="type">int</span> <span
class="methodname">socket\_recvfrom</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`&$buf`</span> , <span class="methodparam"><span class="type">int</span>
`$len`</span> , <span class="methodparam"><span class="type">int</span>
`$flags`</span> , <span class="methodparam"><span
class="type">string</span> `&$name`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$port`</span> \] )

The <span class="function">socket\_recvfrom</span> function receives
`len` bytes of data in `buf` from `name` on port `port` (if the socket
is not of type **`AF_UNIX`**) using `socket`. <span
class="function">socket\_recvfrom</span> can be used to gather data from
both connected and unconnected sockets. Additionally, one or more flags
can be specified to modify the behaviour of the function.

The `name` and `port` must be passed by reference. If the socket is not
connection-oriented, `name` will be set to the internet protocol address
of the remote host or the path to the UNIX socket. If the socket is
connection-oriented, `name` is **`NULL`**. Additionally, the `port` will
contain the port of the remote host in the case of an unconnected
**`AF_INET`** or **`AF_INET6`** socket.

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参数

`socket`  
The `socket` must be a socket resource previously created by
socket\_create().

`buf`  
The data received will be fetched to the variable specified with `buf`.

`len`  
Up to `len` bytes will be fetched from remote host.

`flags`  
The value of `flags` can be any combination of the following flags,
joined with the binary OR (*\|*) operator.

| Flag               | Description                                                                                                                                |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| **`MSG_OOB`**      | Process out-of-band data.                                                                                                                  |
| **`MSG_PEEK`**     | Receive data from the beginning of the receive queue without removing it from the queue.                                                   |
| **`MSG_WAITALL`**  | Block until at least `len` are received. However, if a signal is caught or the remote host disconnects, the function may return less data. |
| **`MSG_DONTWAIT`** | With this flag set, the function returns even if it would normally have blocked.                                                           |

`name`  
If the socket is of the type **`AF_UNIX`** type, `name` is the path to
the file. Else, for unconnected sockets, `name` is the IP address of,
the remote host, or **`NULL`** if the socket is connection-oriented.

`port`  
This argument only applies to **`AF_INET`** and **`AF_INET6`** sockets,
and specifies the remote port from which the data is received. If the
socket is connection-oriented, `port` will be **`NULL`**.

### 返回值

<span class="function">socket\_recvfrom</span> returns the number of
bytes received, or **`FALSE`** if there was an error. The actual error
code can be retrieved by calling <span
class="function">socket\_last\_error</span>. This error code may be
passed to <span class="function">socket\_strerror</span> to get a
textual explanation of the error.

### 范例

**示例 \#1 <span class="function">socket\_recvfrom</span> example**

``` php
<?php
error_reporting(E_ALL | E_STRICT);

$socket = socket_create(AF_INET, SOCK_DGRAM, SOL_UDP);
socket_bind($socket, '127.0.0.1', 1223);

$from = '';
$port = 0;
socket_recvfrom($socket, $buf, 12, 0, $from, $port);

echo "Received $buf from remote address $from and remote port $port" . PHP_EOL;
?>
```

This example will initiate a UDP socket on port 1223 of 127.0.0.1 and
print at most 12 characters received from a remote host.

### 参见

-   <span class="function">socket\_recv</span>
-   <span class="function">socket\_send</span>
-   <span class="function">socket\_sendto</span>
-   <span class="function">socket\_create</span>

socket\_recvmsg
===============

Read a message

### 说明

<span class="type">int</span> <span
class="methodname">socket\_recvmsg</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">array</span>
`&$message`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`socket`  

`message`  

`flags`  

### 返回值

### 参见

-   <span class="function">socket\_sendmsg</span>
-   <span class="function">socket\_cmsg\_space</span>

socket\_select
==============

Runs the select() system call on the given arrays of sockets with a
specified timeout

### 说明

<span class="type">int</span> <span
class="methodname">socket\_select</span> ( <span
class="methodparam"><span class="type">array</span> `&$read`</span> ,
<span class="methodparam"><span class="type">array</span>
`&$write`</span> , <span class="methodparam"><span
class="type">array</span> `&$except`</span> , <span
class="methodparam"><span class="type">int</span> `$tv_sec`</span> \[,
<span class="methodparam"><span class="type">int</span> `$tv_usec`<span
class="initializer"> = 0</span></span> \] )

<span class="function">socket\_select</span> accepts arrays of sockets
and waits for them to change status. Those coming with BSD sockets
background will recognize that those socket resource arrays are in fact
the so-called file descriptor sets. Three independent arrays of socket
resources are watched.

### 参数

`read`  
The sockets listed in the `read` array will be watched to see if
characters become available for reading (more precisely, to see if a
read will not block - in particular, a socket resource is also ready on
end-of-file, in which case a <span class="function">socket\_read</span>
will return a zero length string).

`write`  
The sockets listed in the `write` array will be watched to see if a
write will not block.

`except`  
The sockets listed in the `except` array will be watched for exceptions.

`tv_sec`  
The `tv_sec` and `tv_usec` together form the *timeout* parameter. The
*timeout* is an upper bound on the amount of time elapsed before <span
class="function">socket\_select</span> return. `tv_sec` may be zero ,
causing <span class="function">socket\_select</span> to return
immediately. This is useful for polling. If `tv_sec` is **`NULL`** (no
timeout), <span class="function">socket\_select</span> can block
indefinitely.

`tv_usec`  

**Warning**

On exit, the arrays are modified to indicate which socket resource
actually changed status.

You do not need to pass every array to <span
class="function">socket\_select</span>. You can leave it out and use an
empty array or **`NULL`** instead. Also do not forget that those arrays
are passed *by reference* and will be modified after <span
class="function">socket\_select</span> returns.

> **Note**:
>
> Due a limitation in the current Zend Engine it is not possible to pass
> a constant modifier like **`NULL`** directly as a parameter to a
> function which expects this parameter to be passed by reference.
> Instead use a temporary variable or an expression with the leftmost
> member being a temporary variable:
>
> **示例 \#1 Using **`NULL`** with <span
> class="function">socket\_select</span>**
>
> ``` php
> <?php
> $e = NULL;
> socket_select($r, $w, $e, 0);
> ?>
> ```

### 返回值

On success <span class="function">socket\_select</span> returns the
number of socket resources contained in the modified arrays, which may
be zero if the timeout expires before anything interesting happens. On
error **`FALSE`** is returned. The error code can be retrieved with
<span class="function">socket\_last\_error</span>.

> **Note**:
>
> Be sure to use the *===* operator when checking for an error. Since
> the <span class="function">socket\_select</span> may return 0 the
> comparison with *==* would evaluate to **`TRUE`**:
>
> **示例 \#2 Understanding <span
> class="function">socket\_select</span>'s result**
>
> ``` php
> <?php
> $e = NULL;
> if (false === socket_select($r, $w, $e, 0)) {
>     echo "socket_select() failed, reason: " .
>         socket_strerror(socket_last_error()) . "\n";
> }
> ?>
> ```

### 范例

**示例 \#3 <span class="function">socket\_select</span> example**

``` php
<?php
/* Prepare the read array */
$read   = array($socket1, $socket2);
$write  = NULL;
$except = NULL;
$num_changed_sockets = socket_select($read, $write, $except, 0);

if ($num_changed_sockets === false) {
    /* Error handling */
} else if ($num_changed_sockets > 0) {
    /* At least at one of the sockets something interesting happened */
}
?>
```

### 注释

> **Note**:
>
> Be aware that some socket implementations need to be handled very
> carefully. A few basic rules:
>
> -   <span class="simpara"> You should always try to use <span
>     class="function">socket\_select</span> without timeout. Your
>     program should have nothing to do if there is no data available.
>     Code that depends on timeouts is not usually portable and
>     difficult to debug. </span>
> -   <span class="simpara"> No socket resource must be added to any set
>     if you do not intend to check its result after the <span
>     class="function">socket\_select</span> call, and respond
>     appropriately. After <span class="function">socket\_select</span>
>     returns, all socket resources in all arrays must be checked. Any
>     socket resource that is available for writing must be written to,
>     and any socket resource available for reading must be read from.
>     </span>
> -   <span class="simpara"> If you read/write to a socket returns in
>     the arrays be aware that they do not necessarily read/write the
>     full amount of data you have requested. Be prepared to even only
>     be able to read/write a single byte. </span>
> -   <span class="simpara"> It's common to most socket implementations
>     that the only exception caught with the `except` array is
>     out-of-bound data received on a socket. </span>

### 参见

-   <span class="function">socket\_read</span>
-   <span class="function">socket\_write</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_strerror</span>

socket\_send
============

Sends data to a connected socket

### 说明

<span class="type">int</span> <span
class="methodname">socket\_send</span> ( <span class="methodparam"><span
class="type">resource</span> `$socket`</span> , <span
class="methodparam"><span class="type">string</span> `$buf`</span> ,
<span class="methodparam"><span class="type">int</span> `$len`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
)

The function <span class="function">socket\_send</span> sends `len`
bytes to the socket `socket` from `buf`.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

`buf`  
A buffer containing the data that will be sent to the remote host.

`len`  
The number of bytes that will be sent to the remote host from `buf`.

`flags`  
The value of `flags` can be any combination of the following flags,
joined with the binary OR (*\|*) operator.

|                     |                                                                                                                                                           |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`MSG_OOB`**       | Send OOB (out-of-band) data.                                                                                                                              |
| **`MSG_EOR`**       | Indicate a record mark. The sent data completes the record.                                                                                               |
| **`MSG_EOF`**       | Close the sender side of the socket and include an appropriate notification of this at the end of the sent data. The sent data completes the transaction. |
| **`MSG_DONTROUTE`** | Bypass routing, use direct interface.                                                                                                                     |

### 返回值

<span class="function">socket\_send</span> returns the number of bytes
sent, or **`FALSE`** on error.

### 参见

-   <span class="function">socket\_sendto</span>

socket\_sendmsg
===============

Send a message

### 说明

<span class="type">int</span> <span
class="methodname">socket\_sendmsg</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">array</span>
`$message`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`socket`  

`message`  

`flags`  

### 返回值

Returns the number of bytes sent, 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">socket\_recvmsg</span>
-   <span class="function">socket\_cmsg\_space</span>

socket\_sendto
==============

Sends a message to a socket, whether it is connected or not

### 说明

<span class="type">int</span> <span
class="methodname">socket\_sendto</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`$buf`</span> , <span class="methodparam"><span class="type">int</span>
`$len`</span> , <span class="methodparam"><span class="type">int</span>
`$flags`</span> , <span class="methodparam"><span
class="type">string</span> `$addr`</span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 0</span></span> \] )

The function <span class="function">socket\_sendto</span> sends `len`
bytes from `buf` through the socket `socket` to the `port` at the
address `addr`.

### 参数

`socket`  
A valid socket resource created using <span
class="function">socket\_create</span>.

`buf`  
The sent data will be taken from buffer `buf`.

`len`  
`len` bytes from `buf` will be sent.

`flags`  
The value of `flags` can be any combination of the following flags,
joined with the binary OR (*\|*) operator.

|                     |                                                                                                                                                           |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`MSG_OOB`**       | Send OOB (out-of-band) data.                                                                                                                              |
| **`MSG_EOR`**       | Indicate a record mark. The sent data completes the record.                                                                                               |
| **`MSG_EOF`**       | Close the sender side of the socket and include an appropriate notification of this at the end of the sent data. The sent data completes the transaction. |
| **`MSG_DONTROUTE`** | Bypass routing, use direct interface.                                                                                                                     |

`addr`  
IP address of the remote host.

`port`  
`port` is the remote port number at which the data will be sent.

### 返回值

<span class="function">socket\_sendto</span> returns the number of bytes
sent to the remote host, or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 <span class="function">socket\_sendto</span> Example**

``` php
<?php
    $sock = socket_create(AF_INET, SOCK_DGRAM, SOL_UDP);

    $msg = "Ping !";
    $len = strlen($msg);

    socket_sendto($sock, $msg, $len, 0, '127.0.0.1', 1223);
    socket_close($sock);
?>
```

### 参见

-   <span class="function">socket\_send</span>

socket\_set\_block
==================

Sets blocking mode on a socket resource

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_set\_block</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
)

The <span class="function">socket\_set\_block</span> function removes
the **`O_NONBLOCK`** flag on the socket specified by the `socket`
parameter.

When an operation (e.g. receive, send, connect, accept, ...) is
performed on a blocking socket, the script will pause its execution
until it receives a signal or it can perform the operation.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">socket\_set\_block</span> example**

``` php
<?php
$socket = socket_create_listen(1223);
socket_set_block($socket);

socket_accept($socket);
?>
```

This example creates a listening socket on all interfaces on port 1223
and sets the socket to **`O_BLOCK`** mode. <span
class="function">socket\_accept</span> will hang until there is a
connection to accept.

### 参见

-   <span class="function">socket\_set\_nonblock</span>
-   <span class="function">socket\_set\_option</span>

socket\_set\_nonblock
=====================

Sets nonblocking mode for file descriptor fd

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_set\_nonblock</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
)

The <span class="function">socket\_set\_nonblock</span> function sets
the **`O_NONBLOCK`** flag on the socket specified by the `socket`
parameter.

When an operation (e.g. receive, send, connect, accept, ...) is
performed on a non-blocking socket, the script will not pause its
execution until it receives a signal or it can perform the operation.
Rather, if the operation would result in a block, the called function
will fail.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">socket\_set\_nonblock</span> example**

``` php
<?php
$socket = socket_create_listen(1223);
socket_set_nonblock($socket);

socket_accept($socket);
?>
```

This example creates a listening socket on all interfaces on port 1223
and sets the socket to **`O_NONBLOCK`** mode. <span
class="function">socket\_accept</span> will immediately fail unless
there is a pending connection exactly at this moment.

### 参见

-   <span class="function">socket\_set\_block</span>
-   <span class="function">socket\_set\_option</span>
-   <span class="function">stream\_set\_blocking</span>

socket\_set\_option
===================

Sets socket options for the socket

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">int</span>
`$level`</span> , <span class="methodparam"><span
class="type">int</span> `$optname`</span> , <span
class="methodparam"><span class="type">mixed</span> `$optval`</span> )

The <span class="function">socket\_set\_option</span> function sets the
option specified by the `optname` parameter, at the specified protocol
`level`, to the value pointed to by the `optval` parameter for the
`socket`.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span> or <span
class="function">socket\_accept</span>.

`level`  
The `level` parameter specifies the protocol level at which the option
resides. For example, to retrieve options at the socket level, a `level`
parameter of **`SOL_SOCKET`** would be used. Other levels, such as TCP,
can be used by specifying the protocol number of that level. Protocol
numbers can be found by using the <span
class="function">getprotobyname</span> function.

`optname`  
The available socket options are the same as those for the <span
class="function">socket\_get\_option</span> function.

`optval`  
The option value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">socket\_set\_option</span> example**

``` php
<?php
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!is_resource($socket)) {
    echo 'Unable to create socket: '. socket_strerror(socket_last_error()) . PHP_EOL;
}

if (!socket_set_option($socket, SOL_SOCKET, SO_REUSEADDR, 1)) {
    echo 'Unable to set option on socket: '. socket_strerror(socket_last_error()) . PHP_EOL;
}

if (!socket_bind($socket, '127.0.0.1', 1223)) {
    echo 'Unable to bind socket: '. socket_strerror(socket_last_error()) . PHP_EOL;
}

$rval = socket_get_option($socket, SOL_SOCKET, SO_REUSEADDR);

if ($rval === false) {
    echo 'Unable to get socket option: '. socket_strerror(socket_last_error()) . PHP_EOL;
} else if ($rval !== 0) {
    echo 'SO_REUSEADDR is set on socket !' . PHP_EOL;
}
?>
```

### 参见

-   <span class="function">socket\_create</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_strerror</span>
-   <span class="function">socket\_last\_error</span>
-   <span class="function">socket\_get\_option</span>

socket\_setopt
==============

别名 <span class="function">socket\_set\_option</span>

### 说明

此函数是该函数的别名： <span
class="function">socket\_set\_option</span>.

socket\_shutdown
================

Shuts down a socket for receiving, sending, or both

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_shutdown</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
\[, <span class="methodparam"><span class="type">int</span> `$how`<span
class="initializer"> = 2</span></span> \] )

The <span class="function">socket\_shutdown</span> function allows you
to stop incoming, outgoing or all data (the default) from being sent
through the `socket`

> **Note**:
>
> The associated buffer, or buffers, may or may not be emptied.

### 参数

`socket`  
A valid socket resource created with <span
class="function">socket\_create</span>.

`how`  
The value of `how` can be one of the following:

|     |                                     |
|-----|-------------------------------------|
| *0* | Shutdown socket reading             |
| *1* | Shutdown socket writing             |
| *2* | Shutdown socket reading and writing |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

socket\_strerror
================

Return a string describing a socket error

### 说明

<span class="type">string</span> <span
class="methodname">socket\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errno`</span> )

<span class="function">socket\_strerror</span> takes as its `errno`
parameter a socket error code as returned by <span
class="function">socket\_last\_error</span> and returns the
corresponding explanatory text.

> **Note**:
>
> Although the error messages generated by the socket extension are in
> English, the system messages retrieved with this function will appear
> depending on the current locale (**`LC_MESSAGES`**).

### 参数

`errno`  
A valid socket error number, likely produced by <span
class="function">socket\_last\_error</span>.

### 返回值

Returns the error message associated with the `errno` parameter.

### 范例

**示例 \#1 <span class="function">socket\_strerror</span> example**

``` php
<?php
if (false == ($socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP))) {
   echo "socket_create() failed: reason: " . socket_strerror(socket_last_error()) . "\n";
}

if (false == (@socket_bind($socket, '127.0.0.1', 80))) {
   echo "socket_bind() failed: reason: " . socket_strerror(socket_last_error($socket)) . "\n";
}
?>
```

The expected output from the above example (assuming the script is not
run with root privileges):

    socket_bind() failed: reason: Permission denied

### 参见

-   <span class="function">socket\_accept</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_create</span>

socket\_write
=============

Write to a socket

### 说明

<span class="type">int</span> <span
class="methodname">socket\_write</span> ( <span
class="methodparam"><span class="type">resource</span> `$socket`</span>
, <span class="methodparam"><span class="type">string</span>
`$buffer`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`<span class="initializer"> =
0</span></span> \] )

The function <span class="function">socket\_write</span> writes to the
`socket` from the given `buffer`.

### 参数

`socket`  

`buffer`  
The buffer to be written.

`length`  
The optional parameter `length` can specify an alternate length of bytes
written to the socket. If this length is greater than the buffer length,
it is silently truncated to the length of the buffer.

### 返回值

Returns the number of bytes successfully written to the socket
或者在失败时返回 **`FALSE`**. The error code can be retrieved with <span
class="function">socket\_last\_error</span>. This code may be passed to
<span class="function">socket\_strerror</span> to get a textual
explanation of the error.

> **Note**:
>
> It is perfectly valid for <span class="function">socket\_write</span>
> to return zero which means no bytes have been written. Be sure to use
> the *===* operator to check for **`FALSE`** in case of an error.

### 注释

> **Note**:
>
> <span class="function">socket\_write</span> does not necessarily write
> all bytes from the given buffer. It's valid that, depending on the
> network buffers etc., only a certain amount of data, even one byte, is
> written though your buffer is greater. You have to watch out so you
> don't unintentionally forget to transmit the rest of your data.

### 参见

-   <span class="function">socket\_accept</span>
-   <span class="function">socket\_bind</span>
-   <span class="function">socket\_connect</span>
-   <span class="function">socket\_listen</span>
-   <span class="function">socket\_read</span>
-   <span class="function">socket\_strerror</span>

socket\_wsaprotocol\_info\_export
=================================

Exports the WSAPROTOCOL\_INFO Structure

### 说明

<span class="type">string</span> <span
class="methodname">socket\_wsaprotocol\_info\_export</span> ( <span
class="methodparam"><span class="type">resource </span> `$socket`</span>
, <span class="methodparam"><span class="type">int </span>
`$target_pid`</span> )

Exports the *WSAPROTOCOL\_INFO* structure into shared memory and returns
an identifier to be used with <span
class="function">socket\_wsaprotocol\_info\_import</span>. The exported
ID is only valid for the given `target_pid`.

> **Note**: <span class="simpara"> This function is available only on
> Windows. </span>

### 参数

`socket`  
A valid socket resource.

`target_pid`  
The ID of the process which will import the socket.

### 返回值

Returns an identifier to be used for the import, 或者在失败时返回
**`FALSE`**

### 参见

-   <span class="function">socket\_wsaprotocol\_info\_import</span>
-   <span class="function">socket\_wsaprotocol\_info\_release</span>

socket\_wsaprotocol\_info\_import
=================================

Imports a Socket from another Process

### 说明

<span class="type">resource</span> <span
class="methodname">socket\_wsaprotocol\_info\_import</span> ( <span
class="methodparam"><span class="type">string</span> `$info_id`</span> )

Imports a socket which has formerly been exported from another process.

> **Note**: <span class="simpara"> This function is available only on
> Windows. </span>

### 参数

`info_id`  
The ID which has been returned by a former call to <span
class="function">socket\_wsaprotocol\_info\_export</span>.

### 返回值

Returns the socket resource, 或者在失败时返回 **`FALSE`**

### 参见

-   <span class="function">socket\_wsaprotocol\_info\_export</span>

socket\_wsaprotocol\_info\_release
==================================

Releases an exported WSAPROTOCOL\_INFO Structure

### 说明

<span class="type">bool</span> <span
class="methodname">socket\_wsaprotocol\_info\_release</span> ( <span
class="methodparam"><span class="type">string</span> `$info_id`</span> )

Releases the shared memory corresponding to the given `info_id`.

> **Note**: <span class="simpara"> This function is available only on
> Windows. </span>

### 参数

`info_id`  
The ID which has been returned by a former call to <span
class="function">socket\_wsaprotocol\_info\_export</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">socket\_wsaprotocol\_info\_export</span>

**目录**

-   [socket\_accept](/ref/sockets.html#socket_accept) — Accepts a
    connection on a socket
-   [socket\_addrinfo\_bind](/ref/sockets.html#socket_addrinfo_bind) —
    Create and bind to a socket from a given addrinfo
-   [socket\_addrinfo\_connect](/ref/sockets.html#socket_addrinfo_connect)
    — Create and connect to a socket from a given addrinfo
-   [socket\_addrinfo\_explain](/ref/sockets.html#socket_addrinfo_explain)
    — Get information about addrinfo
-   [socket\_addrinfo\_lookup](/ref/sockets.html#socket_addrinfo_lookup)
    — Get array with contents of getaddrinfo about the given hostname
-   [socket\_bind](/ref/sockets.html#socket_bind) — 给套接字绑定名字
-   [socket\_clear\_error](/ref/sockets.html#socket_clear_error) —
    清除套接字或者最后的错误代码上的错误
-   [socket\_close](/ref/sockets.html#socket_close) — 关闭套接字资源
-   [socket\_cmsg\_space](/ref/sockets.html#socket_cmsg_space) —
    Calculate message buffer size
-   [socket\_connect](/ref/sockets.html#socket_connect) —
    开启一个套接字连接
-   [socket\_create\_listen](/ref/sockets.html#socket_create_listen) —
    Opens a socket on port to accept connections
-   [socket\_create\_pair](/ref/sockets.html#socket_create_pair) —
    Creates a pair of indistinguishable sockets and stores them in an
    array
-   [socket\_create](/ref/sockets.html#socket_create) —
    创建一个套接字（通讯节点）
-   [socket\_export\_stream](/ref/sockets.html#socket_export_stream) —
    Export a socket extension resource into a stream that encapsulates a
    socket
-   [socket\_get\_option](/ref/sockets.html#socket_get_option) — Gets
    socket options for the socket
-   [socket\_getopt](/ref/sockets.html#socket_getopt) — 别名
    socket\_get\_option
-   [socket\_getpeername](/ref/sockets.html#socket_getpeername) —
    Queries the remote side of the given socket which may either result
    in host/port or in a Unix filesystem path, dependent on its type
-   [socket\_getsockname](/ref/sockets.html#socket_getsockname) —
    Queries the local side of the given socket which may either result
    in host/port or in a Unix filesystem path, dependent on its type
-   [socket\_import\_stream](/ref/sockets.html#socket_import_stream) —
    Import a stream
-   [socket\_last\_error](/ref/sockets.html#socket_last_error) — Returns
    the last error on the socket
-   [socket\_listen](/ref/sockets.html#socket_listen) — Listens for a
    connection on a socket
-   [socket\_read](/ref/sockets.html#socket_read) — Reads a maximum of
    length bytes from a socket
-   [socket\_recv](/ref/sockets.html#socket_recv) —
    从已连接的socket接收数据
-   [socket\_recvfrom](/ref/sockets.html#socket_recvfrom) — Receives
    data from a socket whether or not it is connection-oriented
-   [socket\_recvmsg](/ref/sockets.html#socket_recvmsg) — Read a message
-   [socket\_select](/ref/sockets.html#socket_select) — Runs the
    select() system call on the given arrays of sockets with a specified
    timeout
-   [socket\_send](/ref/sockets.html#socket_send) — Sends data to a
    connected socket
-   [socket\_sendmsg](/ref/sockets.html#socket_sendmsg) — Send a message
-   [socket\_sendto](/ref/sockets.html#socket_sendto) — Sends a message
    to a socket, whether it is connected or not
-   [socket\_set\_block](/ref/sockets.html#socket_set_block) — Sets
    blocking mode on a socket resource
-   [socket\_set\_nonblock](/ref/sockets.html#socket_set_nonblock) —
    Sets nonblocking mode for file descriptor fd
-   [socket\_set\_option](/ref/sockets.html#socket_set_option) — Sets
    socket options for the socket
-   [socket\_setopt](/ref/sockets.html#socket_setopt) — 别名
    socket\_set\_option
-   [socket\_shutdown](/ref/sockets.html#socket_shutdown) — Shuts down a
    socket for receiving, sending, or both
-   [socket\_strerror](/ref/sockets.html#socket_strerror) — Return a
    string describing a socket error
-   [socket\_write](/ref/sockets.html#socket_write) — Write to a socket
-   [socket\_wsaprotocol\_info\_export](/ref/sockets.html#socket_wsaprotocol_info_export)
    — Exports the WSAPROTOCOL\_INFO Structure
-   [socket\_wsaprotocol\_info\_import](/ref/sockets.html#socket_wsaprotocol_info_import)
    — Imports a Socket from another Process
-   [socket\_wsaprotocol\_info\_release](/ref/sockets.html#socket_wsaprotocol_info_release)
    — Releases an exported WSAPROTOCOL\_INFO Structure
