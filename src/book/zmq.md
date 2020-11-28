ZMQ
===

**目录**

-   [简介](/intro/zmq.html)
-   [安装／配置](/zmq/setup.html)
    -   [需求](/zmq/setup.html#需求)
-   [ZMQ](/class/zmq.html) — The ZMQ class
    -   [ZMQ::\_\_construct](/class/zmq.html#ZMQ::__construct) — ZMQ
        constructor
-   [ZMQContext](/class/zmqcontext.html) — The ZMQContext class
    -   [ZMQContext::\_\_construct](/class/zmqcontext.html#ZMQContext::__construct)
        — Construct a new ZMQContext object
    -   [ZMQContext::getOpt](/class/zmqcontext.html#ZMQContext::getOpt)
        — Get context option
    -   [ZMQContext::getSocket](/class/zmqcontext.html#ZMQContext::getSocket)
        — Create a new socket
    -   [ZMQContext::isPersistent](/class/zmqcontext.html#ZMQContext::isPersistent)
        — Whether the context is persistent
    -   [ZMQContext::setOpt](/class/zmqcontext.html#ZMQContext::setOpt)
        — Set a socket option
-   [ZMQSocket](/class/zmqsocket.html) — The ZMQSocket class
    -   [ZMQSocket::bind](/class/zmqsocket.html#ZMQSocket::bind) — Bind
        the socket
    -   [ZMQSocket::connect](/class/zmqsocket.html#ZMQSocket::connect) —
        Connect the socket
    -   [ZMQSocket::\_\_construct](/class/zmqsocket.html#ZMQSocket::__construct)
        — Construct a new ZMQSocket
    -   [ZMQSocket::disconnect](/class/zmqsocket.html#ZMQSocket::disconnect)
        — Disconnect a socket
    -   [ZMQSocket::getEndpoints](/class/zmqsocket.html#ZMQSocket::getEndpoints)
        — Get list of endpoints
    -   [ZMQSocket::getPersistentId](/class/zmqsocket.html#ZMQSocket::getPersistentId)
        — Get the persistent id
    -   [ZMQSocket::getSocketType](/class/zmqsocket.html#ZMQSocket::getSocketType)
        — Get the socket type
    -   [ZMQSocket::getSockOpt](/class/zmqsocket.html#ZMQSocket::getSockOpt)
        — Get socket option
    -   [ZMQSocket::isPersistent](/class/zmqsocket.html#ZMQSocket::isPersistent)
        — Whether the socket is persistent
    -   [ZMQSocket::recv](/class/zmqsocket.html#ZMQSocket::recv) —
        Receives a message
    -   [ZMQSocket::recvMulti](/class/zmqsocket.html#ZMQSocket::recvMulti)
        — Receives a multipart message
    -   [ZMQSocket::send](/class/zmqsocket.html#ZMQSocket::send) — Sends
        a message
    -   [ZMQSocket::sendmulti](/class/zmqsocket.html#ZMQSocket::sendmulti)
        — Sends a multipart message
    -   [ZMQSocket::setSockOpt](/class/zmqsocket.html#ZMQSocket::setSockOpt)
        — Set a socket option
    -   [ZMQSocket::unbind](/class/zmqsocket.html#ZMQSocket::unbind) —
        Unbind the socket
-   [ZMQPoll](/class/zmqpoll.html) — The ZMQPoll class
    -   [ZMQPoll::add](/class/zmqpoll.html#ZMQPoll::add) — Add item to
        the poll set
    -   [ZMQPoll::clear](/class/zmqpoll.html#ZMQPoll::clear) — Clear the
        poll set
    -   [ZMQPoll::count](/class/zmqpoll.html#ZMQPoll::count) — Count
        items in the poll set
    -   [ZMQPoll::getLastErrors](/class/zmqpoll.html#ZMQPoll::getLastErrors)
        — Get poll errors
    -   [ZMQPoll::poll](/class/zmqpoll.html#ZMQPoll::poll) — Poll the
        items
    -   [ZMQPoll::remove](/class/zmqpoll.html#ZMQPoll::remove) — Remove
        item from poll set
-   [ZMQDevice](/class/zmqdevice.html) — The ZMQDevice class
    -   [ZMQDevice::\_\_construct](/class/zmqdevice.html#ZMQDevice::__construct)
        — Construct a new device
    -   [ZMQDevice::getIdleTimeout](/class/zmqdevice.html#ZMQDevice::getIdleTimeout)
        — Get the idle timeout
    -   [ZMQDevice::getTimerTimeout](/class/zmqdevice.html#ZMQDevice::getTimerTimeout)
        — Get the timer timeout
    -   [ZMQDevice::run](/class/zmqdevice.html#ZMQDevice::run) — Run the
        new device
    -   [ZMQDevice::setIdleCallback](/class/zmqdevice.html#ZMQDevice::setIdleCallback)
        — Set the idle callback function
    -   [ZMQDevice::setIdleTimeout](/class/zmqdevice.html#ZMQDevice::setIdleTimeout)
        — Set the idle timeout
    -   [ZMQDevice::setTimerCallback](/class/zmqdevice.html#ZMQDevice::setTimerCallback)
        — Set the timer callback function
    -   [ZMQDevice::setTimerTimeout](/class/zmqdevice.html#ZMQDevice::setTimerTimeout)
        — Set the timer timeout

简介
----

类摘要
------

**ZMQ**

<span class="ooclass"> class **ZMQ** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_PAIR` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_PUB` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_SUB` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_REQ` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_REP` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_XREQ` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_XREP` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_PUSH` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_PULL` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_ROUTER` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_DEALER` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_XPUB` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_XSUB` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKET_STREAM` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_HWM` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_SNDHWM` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RCVHWM` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_AFFINITY` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_IDENTITY` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_SUBSCRIBE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_UNSUBSCRIBE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RATE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RECOVERY_IVL` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RECONNECT_IVL` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RECONNECT_IVL_MAX` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_MCAST_LOOP` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_SNDBUF` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RCVBUF` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RCVMORE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_TYPE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_LINGER` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_BACKLOG` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_MAXMSGSIZE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_SNDTIMEO` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_RCVTIMEO` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_IPV4ONLY` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_LAST_ENDPOINT` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_TCP_KEEPALIVE_IDLE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_TCP_KEEPALIVE_CNT` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_TCP_KEEPALIVE_INTVL` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_TCP_ACCEPT_FILTER` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_TCP_ACCEPT_FILTER` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_DELAY_ATTACH_ON_CONNECT` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_XPUB_VERBOSE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_ROUTER_RAW` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::SOCKOPT_IPV6` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::CTXOPT_MAX_SOCKETS` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::POLL_IN` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::POLL_OUT` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::MODE_NOBLOCK` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::MODE_DONTWAIT` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::MODE_SNDMORE` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::ERR_INTERNAL` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::ERR_EAGAIN` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::ERR_ENOTSUP` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::ERR_EFSM` ;

<span class="modifier">const</span> <span class="type">int</span>
`ZMQ::ERR_ETERM` ;

/\* Methods \*/

<span class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

ZMQ Constant Types
------------------

**`ZMQ::SOCKET_PAIR`**  
Exclusive pair pattern

**`ZMQ::SOCKET_PUB`**  
Publisher socket

**`ZMQ::SOCKET_SUB`**  
Subscriber socket

**`ZMQ::SOCKET_REQ`**  
Request socket

**`ZMQ::SOCKET_REP`**  
Reply socket

**`ZMQ::SOCKET_XREQ`**  
Alias for SOCKET\_DEALER

**`ZMQ::SOCKET_XREP`**  
Alias for SOCKET\_ROUTER

**`ZMQ::SOCKET_PUSH`**  
Pipeline upstream push socket

**`ZMQ::SOCKET_PULL`**  
Pipeline downstream pull socket

**`ZMQ::SOCKET_ROUTER`**  
Extended REP socket that can route replies to requesters

**`ZMQ::SOCKET_DEALER`**  
Extended REQ socket that load balances to all connected peers

**`ZMQ::SOCKET_XPUB`**  
Similar to SOCKET\_PUB, except you can receive subscriptions as
messages. The subscription message is 0 (unsubscribe) or 1 (subscribe)
followed by the topic.

**`ZMQ::SOCKET_XSUB`**  
Similar to SOCKET\_SUB, except you can send subscriptions as messages.
See SOCKET\_XPUB for format.

**`ZMQ::SOCKET_STREAM`**  
Used to send and receive TCP data from a non-ØMQ peer. Available if
compiled against ZeroMQ 4.x or higher (Value: <span
class="type">int</span>).

**`ZMQ::SOCKOPT_HWM`**  
The high water mark for inbound and outbound messages is a hard limit on
the maximum number of outstanding messages ØMQ shall queue in memory for
any single peer that the specified socket is communicating with. Setting
this option on a socket will only affect connections made after the
option has been set. On ZeroMQ 3.x this is a wrapper for setting both
SNDHWM and RCVHWM. (Value: <span class="type">int</span>).

**`ZMQ::SOCKOPT_SNDHWM`**  
The ZMQ\_SNDHWM option shall set the high water mark for outbound
messages on the specified socket. Available if compiled against ZeroMQ
3.x or higher (Value: <span class="type">int</span>).

**`ZMQ::SOCKOPT_RCVHWM`**  
The SOCKOPT\_RCVHWM option shall set the high water mark for inbound
messages on the specified socket. Available if compiled against ZeroMQ
3.x or higher (Value: <span class="type">int</span>).

**`ZMQ::SOCKOPT_AFFINITY`**  
Set I/O thread affinity (Value: <span class="type">int</span>)

**`ZMQ::SOCKOPT_IDENTITY`**  
Set socket identity (Value: <span class="type">string</span>)

**`ZMQ::SOCKOPT_SUBSCRIBE`**  
Establish message filter. Valid for subscriber socket (Value: <span
class="type">string</span>)

**`ZMQ::SOCKOPT_UNSUBSCRIBE`**  
Remove message filter. Valid for subscriber socket (Value: <span
class="type">string</span>)

**`ZMQ::SOCKOPT_RATE`**  
Set rate for multicast sockets (pgm) (Value: <span
class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_RECOVERY_IVL`**  
Set multicast recovery interval (Value: <span
class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_RECONNECT_IVL`**  
Set the initial reconnection interval (Value: <span
class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_RECONNECT_IVL_MAX`**  
Set the max reconnection interval (Value: <span
class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_MCAST_LOOP`**  
Control multicast loopback (Value: <span class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_SNDBUF`**  
Set kernel transmit buffer size (Value: <span
class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_RCVBUF`**  
Set kernel receive buffer size (Value: <span
class="type">int</span> \>= 0)

**`ZMQ::SOCKOPT_RCVMORE`**  
Receive multi-part messages (Value: <span class="type">int</span>)

**`ZMQ::SOCKOPT_TYPE`**  
Get the socket type. Valid for getSockOpt (Value: <span
class="type">int</span>)

**`ZMQ::SOCKOPT_LINGER`**  
The linger value of the socket. Specifies how long the socket blocks
trying flush messages after it has been closed (Value: <span
class="type">int</span>)

**`ZMQ::SOCKOPT_BACKLOG`**  
The SOCKOPT\_BACKLOG option shall set the maximum length of the queue of
outstanding peer connections for the specified socket; this only applies
to connection-oriented transports. (Value: <span
class="type">int</span>)

**`ZMQ::SOCKOPT_MAXMSGSIZE`**  
Limits the maximum size of the inbound message. Value -1 means no limit.
Available if compiled against ZeroMQ 3.x or higher (Value: <span
class="type">int</span>)

**`ZMQ::SOCKOPT_SNDTIMEO`**  
Sets the timeout for send operation on the socket. Value -1 means no
limit. Available if compiled against ZeroMQ 3.x or higher (Value: <span
class="type">int</span>)

**`ZMQ::SOCKOPT_RCVTIMEO`**  
Sets the timeout for receive operation on the socket. Value -1 means no
limit. Available if compiled against ZeroMQ 3.x or higher (Value: <span
class="type">int</span>)

**`ZMQ::SOCKOPT_IPV4ONLY`**  
Disable IPV6 support if 1. Available if compiled against ZeroMQ 3.x
(Value: <span class="type">int</span>)

**`ZMQ::SOCKOPT_LAST_ENDPOINT`**  
Retrieve the last connected endpoint - for use with \* wildcard ports.
Available if compiled against ZeroMQ 3.x or higher (Value: <span
class="type">string</span>)

**`ZMQ::SOCKOPT_TCP_KEEPALIVE_IDLE`**  
Idle time for TCP keepalive. Available if compiled against ZeroMQ 3.x or
higher (Value: <span class="type">int</span>)

**`ZMQ::SOCKOPT_TCP_KEEPALIVE_CNT`**  
Count time for TCP keepalive. Available if compiled against ZeroMQ 3.x
or higher (Value: <span class="type">int</span>)

**`ZMQ::SOCKOPT_TCP_KEEPALIVE_INTVL`**  
Interval for TCP keepalive. Available if compiled against ZeroMQ 3.x or
higher (Value: <span class="type">int</span>)

**`ZMQ::SOCKOPT_DELAY_ATTACH_ON_CONNECT`**  
Set a CIDR string to match against incoming TCP connections. Available
if compiled against ZeroMQ 3.x or higher (Value: <span
class="type">string</span>)

**`ZMQ::SOCKOPT_TCP_ACCEPT_FILTER`**  
Set a CIDR string to match against incoming TCP connections. Available
if compiled against ZeroMQ 3.x or higher (Value: <span
class="type">string</span>)

**`ZMQ::SOCKOPT_XPUB_VERBOSE`**  
Set the XPUB to receive an application message on each instance of a
subscription. Available if compiled against ZeroMQ 3.x or higher (Value:
<span class="type">string</span>)

**`ZMQ::SOCKOPT_ROUTER_RAW`**  
Sets the raw mode on the ROUTER, when set to 1. In raw mode when using
tcp:// transport the socket will read and write without ZeroMQ framing.
Available if compiled against ZeroMQ 4.0 or higher (Value: <span
class="type">string</span>)

**`ZMQ::SOCKOPT_IPV6`**  
Enable IPV6. Available if compiled against ZeroMQ 4.0 or higher (Value:
<span class="type">string</span>)

**`ZMQ::CTXOPT_MAX_SOCKETS`**  
The socket limit for this context. Available if compiled against ZeroMQ
3.x or higher (Value: <span class="type">int</span>)

**`ZMQ::POLL_IN`**  
Poll for incoming data

**`ZMQ::POLL_OUT`**  
Poll for outgoing data

**`ZMQ::MODE_NOBLOCK`**  
Non-blocking operation. Deprecated, use ZMQ::MODE\_DONTWAIT instead

**`ZMQ::MODE_DONTWAIT`**  
Non-blocking operation

**`ZMQ::MODE_SNDMORE`**  
Send multi-part message

**`ZMQ::DEVICE_FORWARDER`**  
Forwarder device

**`ZMQ::DEVICE_QUEUE`**  
Queue device

**`ZMQ::DEVICE_STREAMER`**  
Streamer device

**`ZMQ::ERR_INTERNAL`**  
ZMQ extension internal error

**`ZMQ::ERR_EAGAIN`**  
Implies that the operation would block when ZMQ::MODE\_DONTWAIT is used

**`ZMQ::ERR_ENOTSUP`**  
The operation is not supported by the socket type

**`ZMQ::ERR_EFSM`**  
The operation can not be executed because the socket is not in correct
state

**`ZMQ::ERR_ETERM`**  
The context has been terminated

ZMQ::\_\_construct
==================

ZMQ constructor

### 说明

<span class="modifier">private</span> <span
class="methodname">ZMQ::\_\_construct</span> ( <span
class="methodparam">void</span> )

Private constructor to prevent direct initialization. This class holds
the constants for ZMQ extension.

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**ZMQContext**

<span class="ooclass"> class **ZMQContext** </span> {

/\* Methods \*/

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$io_threads`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_persistent`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getOpt</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">getSocket</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$persistent_id`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">callable</span>
`$on_new_socket`<span class="initializer"> = **`NULL`**</span></span>
\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPersistent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ZMQContext</span> <span class="methodname">setOpt</span> (
<span class="methodparam"><span class="type">int</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

}

ZMQContext::\_\_construct
=========================

Construct a new ZMQContext object

### 说明

<span class="methodname">ZMQContext::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$io_threads`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_persistent`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

Constructs a new ZMQ context. The context is used to initialize sockets.
A persistent context is required to initialize persistent sockets.

### 参数

`io_threads`  
Number of io-threads in the context.

`is_persistent`  
Whether the context is persistent. Persistent context is stored over
multiple requests and is a requirement for persistent sockets.

### 范例

**示例 \#1 A <span class="function">ZMQContext</span> example**

Construct a new context and allocate request socket from it

``` php
<?php
/* Allocate a new context */
$context = new ZMQContext();

/* Create a new socket */
$socket = $context->getSocket(ZMQ::SOCKET_REQ, 'my sock');

/* Connect the socket */
$socket->connect("tcp://example.com:1234");

/* Send a request */
$socket->send("Hello there");

/* Receive back the response */
$message = $socket->recv();
?>
```

### 返回值

Throws ZMQContextException if context initialization fails.

ZMQContext::getOpt
==================

Get context option

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ZMQContext::getOpt</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Returns the value of a context option.

### 参数

`key`  
An integer representing the option. See the **`ZMQ::CTXOPT_*`**
constants.

### 返回值

Returns either a <span class="type">string</span> or an <span
class="type">int</span> depending on `key`. Throws ZMQContextException
on error.

ZMQContext::getSocket
=====================

Create a new socket

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQContext::getSocket</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$persistent_id`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">callable</span>
`$on_new_socket`<span class="initializer"> = **`NULL`**</span></span>
\]\] )

Shortcut for creating new sockets from the context. If the context is
not persistent the `persistent_id` parameter is ignored and the socket
falls back to being non-persistent. The `on_new_socket` is called only
when a new underlying socket structure is created.

### 参数

`type`  
**`ZMQ::SOCKET_*`** constant to specify socket type.

`persistent_id`  
If `persistent_id` is specified the socket will be persisted over
multiple requests.

`on_new_socket`  
Callback function, which is executed when a new socket structure is
created. This function does not get invoked if the underlying persistent
connection is re-used. The callback takes ZMQSocket and persistent\_id
as two arguments.

### 范例

**示例 \#1 A <span class="function">ZMQContext</span> example**

Basic usage

``` php
<?php
/* Allocate a new context */
$context = new ZMQContext();

/* Create a new socket */
$socket = $context->getSocket(ZMQ::SOCKET_REQ, 'my sock');

/* Connect the socket */
$socket->connect("tcp://example.com:1234");

/* Send a request */
$socket->send("Hello there");

/* Receive back the response */
$message = $socket->recv();
echo "Received message: {$message}\n";
?>
```

### 返回值

Returns a ZMQSocket object on success. Throws ZMQSocketException on
error.

ZMQContext::isPersistent
========================

Whether the context is persistent

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ZMQContext::isPersistent</span> ( <span
class="methodparam">void</span> )

Whether the context is persistent. Persistent context is needed for
persistent connections as each socket is allocated from a context.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the context is persistent and **`FALSE`** if the
context is non-persistent.

ZMQContext::setOpt
==================

Set a socket option

### 说明

<span class="modifier">public</span> <span
class="type">ZMQContext</span> <span
class="methodname">ZMQContext::setOpt</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Sets a ZMQ context option. The type of the `value` depends on the `key`.
See
<a href="/class/zmq.html#预定义常量" class="link">ZMQ Constant Types</a>
for more information.

### 参数

`key`  
One of the **`ZMQ::CTXOPT_*`** constants.

`value`  
The value of the parameter.

### 返回值

Returns the current object. Throws ZMQContextException on error.

简介
----

类摘要
------

**ZMQSocket**

<span class="ooclass"> class **ZMQSocket** </span> {

/\* Methods \*/

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">bind</span> ( <span class="methodparam"><span
class="type">string</span> `$dsn`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$force`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">connect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$force`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">ZMQContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$persistent_id`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">callable</span>
`$on_new_socket`<span class="initializer"> = **`NULL`**</span></span>
\]\] )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">disconnect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getEndpoints</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">getPersistentId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSocketType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getSockOpt</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPersistent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">recv</span> (\[ <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
0</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">recvMulti</span> (\[ <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">send</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">sendmulti</span> ( <span
class="methodparam"><span class="type">array</span> `$message`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">setSockOpt</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">unbind</span> ( <span class="methodparam"><span
class="type">string</span> `$dsn`</span> )

}

ZMQSocket::bind
===============

Bind the socket

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::bind</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$force`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Bind the socket to an endpoint. The endpoint is defined in format
*transport://address* where transport is one of the following: inproc,
ipc, tcp, pgm or epgm.

### 参数

`dsn`  
The bind dsn, for example *transport://address*.

`force`  
Tries to bind even if the socket has already been bound to the given
endpoint.

### 返回值

Returns the current object. Throws ZMQSocketException on error.

ZMQSocket::connect
==================

Connect the socket

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::connect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$force`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Connect the socket to a remote endpoint. The endpoint is defined in
format *transport://address* where transport is one of the following:
inproc, ipc, tcp, pgm or epgm.

### 参数

`dsn`  
The connect dsn, for example *transport://address*.

`force`  
Tries to connect even if the socket has already been connected to given
endpoint.

### 范例

**示例 \#1 A <span class="function">ZMQContext</span> example**

Construct a new context and allocate request socket from it

``` php
<?php
/* Server hostname */
$dsn = "tcp://127.0.0.1:5555";

/* Create a socket */
$socket = new ZMQSocket(new ZMQContext(), ZMQ::SOCKET_REQ, 'my socket');

/* Get list of connected endpoints */
$endpoints = $socket->getEndpoints();

/* Check if the socket is connected */
if (!in_array($dsn, $endpoints['connect'])) {
    echo "<p>Connecting to $dsn</p>";
    $socket->connect($dsn);
} else {
    echo "<p>Already connected to $dsn</p>";
}

/* Send and receive */
$socket->send("Hello!");
$message = $socket->recv();

echo "<p>Server said: {$message}</p>";
?>
```

### 返回值

Returns the current object. Throws ZMQSocketException on error.

ZMQSocket::\_\_construct
========================

Construct a new ZMQSocket

### 说明

<span class="methodname">ZMQSocket::\_\_construct</span> ( <span
class="methodparam"><span class="type">ZMQContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$persistent_id`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">callable</span>
`$on_new_socket`<span class="initializer"> = **`NULL`**</span></span>
\]\] )

Constructs a ZMQSocket object. `persistent_id` parameter can be used to
allocated a persistent socket. A persistent socket has to be allocated
from a persistent context and it stays connected over multiple requests.
The `persistent_id` parameter can be used to recall the same socket over
multiple requests. The `on_new_socket` is called only when a new
underlying socket structure is created.

### 参数

`context`  
ZMQContext object.

`type`  
The socket type. See **`ZMQ::SOCKET_*`** constants.

`persistent_id`  
If `persistent_id` is specified the socket will be persisted over
multiple requests. If `context` is not persistent the socket falls back
to non-persistent mode.

`on_new_socket`  
Callback function, which is executed when a new socket structure is
created. This function does not get invoked if the underlying persistent
connection is re-used.

### 范例

**示例 \#1 A <span class="function">ZMQSocket</span> example**

Using callback the bind/connect socket

``` php
<?php

/*
  The socket is persistent so this function is called only on the 
  first request to the script.
*/
function on_new_socket_cb(ZMQSocket $socket, $persistent_id = null)
{
    if ($persistent_id === 'server') {
        $socket->bind("tcp://localhost:12122");
    } else {
        $socket->connect("tcp://localhost:12122");
    }
}

/* Allocate a new context */
$context = new ZMQContext();

/* Create a new socket */
$socket = $context->getSocket(ZMQ::SOCKET_REP, 'server', 'on_new_socket_cb');

$message = $socket->recv();
echo "Received message: {$message}\n";
?>
```

The callback signature

> **Note**:
>
> function on\_new\_socket\_cb(ZMQSocket $socket, string $persistent\_id
> = null);

### 返回值

Throws ZMQSocketException on error.

ZMQSocket::disconnect
=====================

Disconnect a socket

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::disconnect</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> )

Disconnect the socket from a previously connected remote endpoint. The
endpoint is defined in format *transport://address* where transport is
one of the following: inproc, ipc, tcp, pgm or epgm.

### 参数

`dsn`  
The connect dsn, for example *transport://address*.

### 返回值

Returns the current object. Throws ZMQSocketException on error.

ZMQSocket::getEndpoints
=======================

Get list of endpoints

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ZMQSocket::getEndpoints</span> ( <span
class="methodparam">void</span> )

Returns a list of endpoints where the socket is connected or bound to.

### 参数

此函数没有参数。

### 返回值

Returns an array containing elements 'bind' and 'connect'.

ZMQSocket::getPersistentId
==========================

Get the persistent id

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">ZMQSocket::getPersistentId</span> ( <span
class="methodparam">void</span> )

Returns the persistent id of the socket.

### 参数

此函数没有参数。

### 返回值

Returns the persistent id string assigned of the object and **`NULL`**
if socket is not persistent.

ZMQSocket::getSocketType
========================

Get the socket type

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ZMQSocket::getSocketType</span> ( <span
class="methodparam">void</span> )

Gets the socket type.

### 参数

此函数没有参数。

### 返回值

Returns an integer representing the socket type. The integer can be
compared against **`ZMQ::SOCKET_*`** constants.

ZMQSocket::getSockOpt
=====================

Get socket option

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ZMQSocket::getSockOpt</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Returns the value of a socket option.

### 参数

`key`  
An integer representing the option. See the **`ZMQ::SOCKOPT_*`**
constants.

### 返回值

Returns either a <span class="type">string</span> or an <span
class="type">int</span> depending on `key`. Throws ZMQSocketException on
error.

ZMQSocket::isPersistent
=======================

Whether the socket is persistent

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ZMQSocket::isPersistent</span> ( <span
class="methodparam">void</span> )

Check whether the socket is persistent.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="type">bool</span> based on whether the socket is
persistent or not.

ZMQSocket::recv
===============

Receives a message

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ZMQSocket::recv</span> (\[ <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

Receive a message from a socket. By default receiving will block until a
message is available unless **`ZMQ::MODE_DONTWAIT`** flag is used.
**`ZMQ::SOCKOPT_RCVMORE`** socket option can be used for receiving
multi-part messages. See <span
class="function">ZMQSocket::setSockOpt</span> for more information.

### 参数

`mode`  
Pass mode flags to receive multipart messages or non-blocking operation.
See **`ZMQ::MODE_*`** constants.

### 范例

**示例 \#1 A send/recv example**

Non-blocking send / receive

``` php
<?php

/* Create new queue object, there needs to be a server at the other end */
$queue = new ZMQSocket(new ZMQContext(), ZMQ::SOCKET_REQ);
$queue->connect("tcp://127.0.0.1:5555");

/* Assign socket 1 to the queue, send and receive */
$retries = 5;
$sending = true;

/* Start a loop */
do {
    try {
        /* Try to send / receive */
        if ($sending) {
            echo "Sending message\n";
            $queue->send("This is a message", ZMQ::MODE_DONTWAIT);
            $sending = false;
        } else {
            echo "Got response: " . $queue->recv(ZMQ::MODE_DONTWAIT) . "\n";
            break;
        }
    } catch (ZMQSocketException $e) {
        /* EAGAIN means that the operation would have blocked, retry */
        if ($e->getCode() === ZMQ::ERR_EAGAIN) {
            echo " - Got EAGAIN, retrying ($retries)\n";
        } else {
            die(" - Error: " . $e->getMessage());
        }
    }
    /* Sleep a bit between operations */
    usleep(5);
} while (--$retries);
?>
```

以上例程的输出类似于：

    Sending message
     - Unable to execute operation, retrying (4)
    Got response: This is a message

### 返回值

Returns the message. Throws ZMQSocketException in error. If
**`ZMQ::MODE_DONTWAIT`** is used and the operation would block <span
class="type">bool</span> false shall be returned.

ZMQSocket::recvMulti
====================

Receives a multipart message

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ZMQSocket::recvMulti</span> (\[ <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

Receive an array multipart message from a socket. By default receiving
will block until a message is available unless **`ZMQ::MODE_NOBLOCK`**
flag is used.

### 参数

`mode`  
Pass mode flags to receive multipart messages or non-blocking operation.
See **`ZMQ::MODE_*`** constants.

### 返回值

Returns the array of message parts. Throws ZMQSocketException in error.
If **`ZMQ::MODE_NOBLOCK`** is used and the operation would block <span
class="type">bool</span> false shall be returned.

ZMQSocket::send
===============

Sends a message

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::send</span> ( <span
class="methodparam"><span class="type">string</span> `$message`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

Send a message using the socket. The operation can block unless
**`ZMQ::MODE_NOBLOCK`** is used.

### 参数

`message`  
The message to send.

`mode`  
Pass mode flags to receive multipart messages or non-blocking operation.
See **`ZMQ::MODE_*`** constants.

### 返回值

Returns the current object. Throws ZMQSocketException on error. If
**`ZMQ::MODE_NOBLOCK`** is used and the operation would block <span
class="type">bool</span> false shall be returned.

ZMQSocket::sendmulti
====================

Sends a multipart message

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::sendmulti</span> ( <span
class="methodparam"><span class="type">array</span> `$message`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

Send a multipart message using the socket. The operation can block
unless **`ZMQ::MODE_NOBLOCK`** is used.

### 参数

`message`  
The message to send - an array of strings

`mode`  
Pass mode flags to receive multipart messages or non-blocking operation.
See **`ZMQ::MODE_*`** constants.

### 返回值

Returns the current object. Throws ZMQSocketException on error. If
**`ZMQ::MODE_NOBLOCK`** is used and the operation would block <span
class="type">bool</span> false shall be returned.

ZMQSocket::setSockOpt
=====================

Set a socket option

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::setSockOpt</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Sets a ZMQ socket option. The type of the `value` depends on the `key`.
See
<a href="/class/zmq.html#预定义常量" class="link">ZMQ Constant Types</a>
for more information.

### 参数

`key`  
One of the **`ZMQ::SOCKOPT_*`** constants.

`value`  
The value of the parameter.

### 返回值

Returns the current object. Throws ZMQSocketException on error.

ZMQSocket::unbind
=================

Unbind the socket

### 说明

<span class="modifier">public</span> <span class="type">ZMQSocket</span>
<span class="methodname">ZMQSocket::unbind</span> ( <span
class="methodparam"><span class="type">string</span> `$dsn`</span> )

Unbind the socket from an endpoint. The endpoint is defined in format
*transport://address* where transport is one of the following: inproc,
ipc, tcp, pgm or epgm.

### 参数

`dsn`  
The previously bound dsn, for example *transport://address*.

### 返回值

Returns the current object. Throws ZMQSocketException on error.

简介
----

类摘要
------

**ZMQPoll**

<span class="ooclass"> class **ZMQPoll** </span> {

/\* Methods \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">mixed</span> `$entry`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> )

<span class="modifier">public</span> <span class="type">ZMQPoll</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getLastErrors</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">poll</span> ( <span class="methodparam"><span
class="type">array</span> `&$readable`</span> , <span
class="methodparam"><span class="type">array</span> `&$writable`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`<span class="initializer"> = -1</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">remove</span> ( <span class="methodparam"><span
class="type">mixed</span> `$item`</span> )

}

ZMQPoll::add
============

Add item to the poll set

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ZMQPoll::add</span> ( <span
class="methodparam"><span class="type">mixed</span> `$entry`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> )

Adds a new item to the poll set and returns the internal id of the added
item. The item can be removed from the poll set using the returned
string id.

### 参数

`entry`  
ZMQSocket object or a PHP stream resource

`type`  
Defines what activity the socket is polled for. See **`ZMQ::POLL_IN`**
and **`ZMQ::POLL_OUT`** constants.

### 返回值

Returns a string id of the added item which can be later used to remove
the item. Throws ZMQPollException on error.

ZMQPoll::clear
==============

Clear the poll set

### 说明

<span class="modifier">public</span> <span class="type">ZMQPoll</span>
<span class="methodname">ZMQPoll::clear</span> ( <span
class="methodparam">void</span> )

Clears all elements from the poll set.

### 参数

此函数没有参数。

### 返回值

Returns the current object.

ZMQPoll::count
==============

Count items in the poll set

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ZMQPoll::count</span> ( <span
class="methodparam">void</span> )

Count the items in the poll set.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">int</span> representing the amount of
items in the poll set.

ZMQPoll::getLastErrors
======================

Get poll errors

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ZMQPoll::getLastErrors</span> ( <span
class="methodparam">void</span> )

Returns the ids of the objects that had errors in the last poll.

### 参数

此函数没有参数。

### 返回值

Returns an array containing ids for the items that had errors in the
last poll. Empty array is returned if there were no errors.

ZMQPoll::poll
=============

Poll the items

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ZMQPoll::poll</span> ( <span
class="methodparam"><span class="type">array</span> `&$readable`</span>
, <span class="methodparam"><span class="type">array</span>
`&$writable`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
-1</span></span> \] )

Polls the items in the current poll set. The readable and writable items
are returned in the `readable` and `writable` parameters. <span
class="function">ZMQPoll::getLastErrors</span> can be used to check if
there were errors.

### 参数

`readable`  
Array where readable ZMQSockets/PHP streams are returned. The array will
be cleared at the beginning of the operation.

`writable`  
Array where writable ZMQSockets/PHP streams are returned. The array will
be cleared at the beginning of the operation.

`timeout`  
Timeout for the operation. -1 means that poll waits until at least one
item has activity. Please note that starting from version 1.0.0 the poll
timeout is defined in milliseconds, rather than microseconds.

### 范例

**示例 \#1 A <span class="function">ZMQPoll</span> example**

Create a simple poll server

``` php
<?php

/* Create socket, request-reply pattern (reply socket) */
$context = new ZMQContext();
$server  = $context->getSocket(ZMQ::SOCKET_REP);

/* Bind to port 5555 on 127.0.0.1 */
$server->bind("tcp://127.0.0.1:5555");

/* Create new pollset for incoming/outgoing message */
$poll = new ZMQPoll();

/* Add the object and listen for poll in/out */
$id = $poll->add($server, ZMQ::POLL_IN | ZMQ::POLL_OUT);
echo "Added object with id " . $id . "\n";

/* Initialise readable and writable arrays */
$readable = array();
$writable = array();

while (true) {
   /* Amount of events retrieved */
   $events = 0;

   try {
       /* Poll until there is something to do */
       $events = $poll->poll($readable, $writable, -1);
       $errors = $poll->getLastErrors();

       if (count($errors) > 0) {
           foreach ($errors as $error) {
               echo "Error polling object " . $error . "\n";
           }
       }
   } catch (ZMQPollException $e) {
       echo "poll failed: " . $e->getMessage() . "\n";
   }

   if ($events > 0) {
       /* Loop through readable objects and recv messages */
       foreach ($readable as $r) {
           try {
               echo "Received message: " . $r->recv() . "\n";
           } catch (ZMQException $e) {
               echo "recv failed: " . $e->getMessage() . "\n";
           }
       }

       /* Loop through writable and send back messages */
       foreach ($writable as $w) {
           try {
               $w->send("Got it!");
           } catch (ZMQException $e) {
               echo "send failed: " . $e->getMessage() . "\n";
           }
       }
   }
}
?>
```

### 返回值

Returns an integer representing amount of items with activity. Throws
ZMQPollException on error.

ZMQPoll::remove
===============

Remove item from poll set

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ZMQPoll::remove</span> ( <span
class="methodparam"><span class="type">mixed</span> `$item`</span> )

Remove item from the poll set. The `item` parameter can be ZMQSocket
object, a stream resource or the id returned from <span
class="function">ZMQPoll::add</span> method.

### 参数

`item`  
The ZMQSocket object, PHP stream or <span class="type">string</span> id
of the item.

### 返回值

Returns true if the item was removed and false if the object with given
id does not exist in the poll set.

简介
----

类摘要
------

**ZMQDevice**

<span class="ooclass"> class **ZMQDevice** </span> {

/\* Methods \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">ZMQSocket</span>
`$frontend`</span> , <span class="methodparam"><span
class="type">ZMQSocket</span> `$backend`</span> \[, <span
class="methodparam"><span class="type">ZMQSocket</span>
`$listener`</span> \] )

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">getIdleTimeout</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">getTimerTimeout</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">run</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">setIdleCallback</span> ( <span
class="methodparam"><span class="type">callable</span> `$cb_func`</span>
, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$user_data`</span> \] )

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">setIdleTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">setTimerCallback</span> ( <span
class="methodparam"><span class="type">callable</span> `$cb_func`</span>
, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$user_data`</span> \] )

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">setTimerTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

}

ZMQDevice::\_\_construct
========================

Construct a new device

### 说明

<span class="methodname">ZMQDevice::\_\_construct</span> ( <span
class="methodparam"><span class="type">ZMQSocket</span>
`$frontend`</span> , <span class="methodparam"><span
class="type">ZMQSocket</span> `$backend`</span> \[, <span
class="methodparam"><span class="type">ZMQSocket</span>
`$listener`</span> \] )

"ØMQ devices can do intermediation of addresses, services, queues, or
any other abstraction you care to define above the message and socket
layers." -- zguide

### 参数

`frontend`  
Frontend parameter for the devices. Usually where there messages are
coming.

`backend`  
Backend parameter for the devices. Usually where there messages going
to.

`listener`  
Listener socket, which receives a copy of all messages going both
directions. The type of this socket should be SUB, PULL or DEALER.

### 返回值

Call to this method will prepare the device. Usually devices are very
long running processes so running this method from interactive script is
not recommended. This method throw ZMQDeviceException if the device
cannot be started.

ZMQDevice::getIdleTimeout
=========================

Get the idle timeout

### 说明

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">ZMQDevice::getIdleTimeout</span> ( <span
class="methodparam">void</span> )

Gets the idle callback timeout value. Added in ZMQ extension version
1.1.0.

### 返回值

This method returns the idle callback timeout value.

ZMQDevice::getTimerTimeout
==========================

Get the timer timeout

### 说明

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">ZMQDevice::getTimerTimeout</span> ( <span
class="methodparam">void</span> )

Gets the timer callback timeout value. Added in ZMQ extension version
1.1.0.

### 返回值

This method returns the timer timeout value.

ZMQDevice::run
==============

Run the new device

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ZMQDevice::run</span> ( <span
class="methodparam">void</span> )

Runs the device.

### 参数

此函数没有参数。

### 返回值

Call to this method will block until the device is running. It is not
recommended that devices are used from interactive scripts. On failure
this method will throw ZMQDeviceException.

ZMQDevice::setIdleCallback
==========================

Set the idle callback function

### 说明

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">ZMQDevice::setIdleCallback</span> ( <span
class="methodparam"><span class="type">callable</span> `$cb_func`</span>
, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$user_data`</span> \] )

Sets the idle callback function. If idle timeout is defined the idle
callback function shall be called if the internal poll loop times out
without events. If the callback function returns false or a value that
evaluates to false the device is stopped. The callback function
signature is callback (mixed $user\_data).

### 参数

`cb_func`  
Callback function to invoke when the device is idle. Returning false or
a value that evaluates to false from this function will cause the device
to stop.

`timeout`  
How often to invoke the idle callback in milliseconds. The idle callback
is invoked periodically when there is no activity on the device. The
timeout value guarantees that there is at least this amount of
milliseconds between invocations of the callback function.

`user_data`  
Additional data to pass to the callback function.

### 返回值

On success this method returns the current object.

ZMQDevice::setIdleTimeout
=========================

Set the idle timeout

### 说明

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">ZMQDevice::setIdleTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

Sets the idle callback timeout value. The idle callback is invoked
periodically when the device is idle.

### 参数

`timeout`  
The idle callback timeout value.

### 返回值

On success this method returns the current object.

ZMQDevice::setTimerCallback
===========================

Set the timer callback function

### 说明

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">ZMQDevice::setTimerCallback</span> ( <span
class="methodparam"><span class="type">callable</span> `$cb_func`</span>
, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$user_data`</span> \] )

Sets the timer callback function. The timer callback will be invoked
after timeout has passed. The difference between idle and timer
callbacks are that idle callback is invoked only when the device is
idle. The callback function signature is callback (mixed $user\_data).
Added in ZMQ extension version 1.1.0.

### 参数

`cb_func`  
Callback function to invoke when the device is idle. Returning false or
a value that evaluates to false from this function will cause the device
to stop.

`timeout`  
How often to invoke the idle callback in milliseconds. The idle callback
is invoked periodically when there is no activity on the device. The
timeout value guarantees that there is at least this amount of
milliseconds between invocations of the callback function.

`user_data`  
Additional data to pass to the callback function.

### 返回值

On success this method returns the current object.

ZMQDevice::setTimerTimeout
==========================

Set the timer timeout

### 说明

<span class="modifier">public</span> <span class="type">ZMQDevice</span>
<span class="methodname">ZMQDevice::setTimerTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

Sets the timer callback timeout value. The timer callback is invoked
periodically if it's set. Added in ZMQ extension version 1.1.0.

### 参数

`timeout`  
The timer callback timeout value.

### 返回值

On success this method returns the current object.
