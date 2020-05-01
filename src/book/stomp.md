Stomp Client
============

**目录**

-   [简介](/intro/stomp.html)
-   [安装／配置](/stomp/setup.html)
    -   [需求](/stomp/setup.html#需求)
    -   [安装](/stomp/setup.html#安装)
    -   [运行时配置](/stomp/setup.html#运行时配置)
    -   [资源类型](/stomp/setup.html#资源类型)
-   [范例](/stomp/examples.html)
-   [Stomp 函数](/ref/stomp.html)
    -   [stomp\_connect\_error](/ref/stomp.html#stomp_connect_error) —
        Returns a string description of the last connect error
    -   [stomp\_version](/ref/stomp.html#stomp_version) — Gets the
        current stomp extension version
-   [Stomp](/class/stomp.html) — The Stomp class
    -   [Stomp::abort](/class/stomp.html#Stomp::abort) — Rolls back a
        transaction in progress
    -   [Stomp::ack](/class/stomp.html#Stomp::ack) — Acknowledges
        consumption of a message
    -   [Stomp::begin](/class/stomp.html#Stomp::begin) — Starts a
        transaction
    -   [Stomp::commit](/class/stomp.html#Stomp::commit) — Commits a
        transaction in progress
    -   [Stomp::\_\_construct](/class/stomp.html#Stomp::__construct) —
        打开一个连接
    -   [Stomp::\_\_destruct](/class/stomp.html#Stomp::__destruct) —
        Closes stomp connection
    -   [Stomp::error](/class/stomp.html#Stomp::error) — Gets the last
        stomp error
    -   [Stomp::getReadTimeout](/class/stomp.html#Stomp::getReadTimeout)
        — Gets read timeout
    -   [Stomp::getSessionId](/class/stomp.html#Stomp::getSessionId) —
        Gets the current stomp session ID
    -   [Stomp::hasFrame](/class/stomp.html#Stomp::hasFrame) — Indicates
        whether or not there is a frame ready to read
    -   [Stomp::readFrame](/class/stomp.html#Stomp::readFrame) — Reads
        the next frame
    -   [Stomp::send](/class/stomp.html#Stomp::send) — Sends a message
    -   [Stomp::setReadTimeout](/class/stomp.html#Stomp::setReadTimeout)
        — Sets read timeout
    -   [Stomp::subscribe](/class/stomp.html#Stomp::subscribe) —
        Registers to listen to a given destination
    -   [Stomp::unsubscribe](/class/stomp.html#Stomp::unsubscribe) —
        Removes an existing subscription
-   [StompFrame](/class/stompframe.html) — The StompFrame class
    -   [StompFrame::\_\_construct](/class/stompframe.html#StompFrame::__construct)
        — Constructor
-   [StompException](/class/stompexception.html) — The StompException
    class
    -   [StompException::getDetails](/class/stompexception.html#StompException::getDetails)
        — Get exception details

简介
----

Represents a connection between PHP and a Stomp compliant Message
Broker.

类摘要
------

**Stomp**

<span class="ooclass"> class **Stomp** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">abort</span> ( <span class="methodparam"><span
class="type">string</span> `$transaction_id`</span> \[, <span
class="methodparam"><span class="type">array</span> `$headers`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ack</span> ( <span class="methodparam"><span
class="type">mixed</span> `$msg`</span> \[, <span
class="methodparam"><span class="type">array</span> `$headers`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">begin</span> ( <span class="methodparam"><span
class="type">string</span> `$transaction_id`</span> \[, <span
class="methodparam"><span class="type">array</span> `$headers`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">commit</span> ( <span class="methodparam"><span
class="type">string</span> `$transaction_id`</span> \[, <span
class="methodparam"><span class="type">array</span> `$headers`</span> \]
)

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$broker`<span
class="initializer"> =
ini\_get("stomp.default\_broker\_uri")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$username`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$password`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">error</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getReadTimeout</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getSessionId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasFrame</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">stompframe</span> <span class="methodname">readFrame</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$class_name`<span class="initializer"> = "stompFrame"</span></span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">send</span> ( <span class="methodparam"><span
class="type">string</span> `$destination`</span> , <span
class="methodparam"><span class="type">mixed</span> `$msg`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$headers`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setReadTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$seconds`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$microseconds`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">subscribe</span> ( <span
class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unsubscribe</span> ( <span
class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

}

Stomp::abort
============

stomp\_abort
============

Rolls back a transaction in progress

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::abort</span> ( <span
class="methodparam"><span class="type">string</span>
`$transaction_id`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_abort</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">string</span>
`$transaction_id`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

Rolls back a transaction in progress.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`transaction_id`  
The transaction to abort.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

/* begin a transaction */
$stomp->begin('t1');

/* send a message to the queue */
$stomp->send('/queue/foo', 'bar', array('transaction' => 't1'));

/* rollback */
$stomp->abort('t1');

/* close connection */
unset($stomp);
?>
```

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('tcp://localhost:61613');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

/* begin a transaction */
stomp_begin($link, 't1');

/* send a message to the queue 'foo' */
stomp_send($link, '/queue/foo', 'bar', array('transaction' => 't1'));

/* rollback */
stomp_abort($link, 't1');

/* close connection */
stomp_close($link);

?>
```

Stomp::ack
==========

stomp\_ack
==========

Acknowledges consumption of a message

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::ack</span> ( <span
class="methodparam"><span class="type">mixed</span> `$msg`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$headers`</span> \] )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_ack</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">mixed</span> `$msg`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$headers`</span> \] )

Acknowledges consumption of a message from a subscription using client
acknowledgment.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`msg`  
The message/messageId to be acknowledged.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**:
>
> A transaction header may be specified, indicating that the message
> acknowledgment should be part of the named transaction.

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

/* send a message to the queue 'foo' */
$stomp->send($queue, $msg);

/* subscribe to messages from the queue 'foo' */
$stomp->subscribe($queue);

/* read a frame */
$frame = $stomp->readFrame();

if ($frame->body === $msg) {
    /* acknowledge that the frame was received */
    $stomp->ack($frame);
}

/* remove the subscription */
$stomp->unsubscribe($queue);

/* close connection */
unset($stomp);

?>
```

**示例 \#2 过程化风格**

``` php
<?php

$queue  = '/queue/foo';
$msg    = 'bar';

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

/* begin a transaction */
stomp_begin($link, 't1');

/* send a message to the queue 'foo' */
stomp_send($link, $queue, $msg, array('transaction' => 't1'));

/* commit a transaction */
stomp_commit($link, 't1');

/* subscribe to messages from the queue 'foo' */
stomp_subscribe($link, $queue);

/* read a frame */
$frame = stomp_read_frame($link);

if ($frame['body'] === $msg) {
    /* acknowledge that the frame was received */
    stomp_ack($link, $frame['headers']['message-id']);
}

/* remove the subscription */
stomp_unsubscribe($link, $queue);

/* close connection */
stomp_close($link);

?>
```

Stomp::begin
============

stomp\_begin
============

Starts a transaction

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::begin</span> ( <span
class="methodparam"><span class="type">string</span>
`$transaction_id`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_begin</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">string</span>
`$transaction_id`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

Starts a transaction.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`transaction_id`  
The transaction id.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

See <span class="function">stomp\_commit</span> or <span
class="function">stomp\_abort</span>.

Stomp::commit
=============

stomp\_commit
=============

Commits a transaction in progress

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::commit</span> ( <span
class="methodparam"><span class="type">string</span>
`$transaction_id`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_commit</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$transaction_id`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

Commits a transaction in progress.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`transaction_id`  
The transaction id.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

/* begin a transaction */
$stomp->begin('t1');

/* send a message to the queue */
$stomp->send('/queue/foo', 'bar', array('transaction' => 't1'));

/* commit */
$stomp->commit('t1');

/* close connection */
unset($stomp);

?>
```

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('tcp://localhost:61613');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

/* begin a transaction */
stomp_begin($link, 't1');

/* send a message to the queue 'foo' */
stomp_send($link, '/queue/foo', 'bar', array('transaction' => 't1'));

/* commit */
stomp_commit($link, 't1');

/* close connection */
stomp_close($link);

?>
```

Stomp::\_\_construct
====================

stomp\_connect
==============

打开一个连接

### 说明

面向对象风格 (constructor):

<span class="modifier">public</span> <span
class="methodname">Stomp::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$broker`<span
class="initializer"> =
ini\_get("stomp.default\_broker\_uri")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$username`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$password`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \]\]\]\] )

过程化风格:

<span class="type">resource</span> <span
class="methodname">stomp\_connect</span> (\[ <span
class="methodparam"><span class="type">string</span> `$broker`<span
class="initializer"> =
ini\_get("stomp.default\_broker\_uri")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$username`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$password`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \]\]\]\] )

打开一个到兼容stomp通讯协议的消息代理服务器的连接.

### 参数

`broker`  
代理服务器的统一资源标识符（URI）。

`username`  
用户名.

`password`  
密码.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

> **Note**:
>
> A transaction header may be specified, indicating that the message
> acknowledgment should be part of the named transaction.

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 1.0.1 | 增加了`headers` 参数 |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

/* close connection */
unset($stomp);

?>
```

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

/* close connection */
stomp_close($link);

?>
```

Stomp::\_\_destruct
===================

stomp\_close
============

Closes stomp connection

### 说明

面向对象风格 (destructor):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::\_\_destruct</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

Closes a previously opened connection.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

See <span class="function">stomp\_connect</span>.

Stomp::error
============

stomp\_error
============

Gets the last stomp error

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Stomp::error</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">stomp\_error</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> )

Gets the last stomp error.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

### 返回值

Returns an error string or **`FALSE`** if no error occurred.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

var_dump($stomp->error());

if (!$stomp->abort('unknown-transaction', array('receipt' => 'foo'))) {
    var_dump($stomp->error());
}

/* close connection */
unset($stomp);

?>
```

以上例程的输出类似于：

    bool(false)
    string(43) "Invalid transaction id: unknown-transaction"

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

var_dump(stomp_error($link));

if (!stomp_abort($link, 'unknown-transaction', array('receipt' => 'foo'))) {
    var_dump(stomp_error($link));
}

/* close connection */
stomp_close($link);

?>
```

以上例程的输出类似于：

    bool(false)
    string(43) "Invalid transaction id: unknown-transaction"

Stomp::getReadTimeout
=====================

stomp\_get\_read\_timeout
=========================

Gets read timeout

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Stomp::getReadTimeout</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">stomp\_get\_read\_timeout</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

Gets read timeout

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

### 返回值

Returns an array with 2 elements: sec and usec.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

var_dump($stomp->getReadTimeout());

/* close connection */
unset($stomp);

?>
```

以上例程的输出类似于：

    array(2) {
      ["sec"]=>
      int(2)
      ["usec"]=>
      int(0)
    }

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

var_dump(stomp_get_read_timeout($link));

/* close connection */
stomp_close($link);

?>
```

以上例程的输出类似于：

    array(2) {
      ["sec"]=>
      int(2)
      ["usec"]=>
      int(0)
    }

Stomp::getSessionId
===================

stomp\_get\_session\_id
=======================

Gets the current stomp session ID

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Stomp::getSessionId</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">stomp\_get\_session\_id</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

Gets the current stomp session ID.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

### 返回值

<span class="type">string</span> session id on success 或者在失败时返回
**`FALSE`**.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

var_dump($stomp->getSessionId());

/* close connection */
unset($stomp);

?>
```

以上例程的输出类似于：

    string(35) "ID:php.net-52873-1257291895530-4:14"

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

var_dump(stomp_get_session_id($link));

/* close connection */
stomp_close($link);

?>
```

以上例程的输出类似于：

    string(35) "ID:php.net-52873-1257291895530-4:14"

Stomp::hasFrame
===============

stomp\_has\_frame
=================

Indicates whether or not there is a frame ready to read

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::hasFrame</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_has\_frame</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

Indicates whether or not there is a frame ready to read.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

### 返回值

Returns **`TRUE`** if a frame is ready to read, or **`FALSE`**
otherwise.

Stomp::readFrame
================

stomp\_read\_frame
==================

Reads the next frame

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="type">stompframe</span> <span
class="methodname">Stomp::readFrame</span> (\[ <span
class="methodparam"><span class="type">string</span> `$class_name`<span
class="initializer"> = "stompFrame"</span></span> \] )

过程化风格:

<span class="type">array</span> <span
class="methodname">stomp\_read\_frame</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> )

Reads the next frame. It is possible to instantiate an object of a
specific class, and pass parameters to that class's constructor.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`class_name`  
The name of the class to instantiate. If not specified, a stompFrame
object is returned.

### 返回值

> **Note**:
>
> A transaction header may be specified, indicating that the message
> acknowledgment should be part of the named transaction.

### 更新日志

| 版本        | 说明                              |
|-------------|-----------------------------------|
| Stomp 0.4.0 | `class_name` parameter was added. |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

/* subscribe to messages from the queue 'foo' */
$stomp->subscribe('/queue/foo');

/* read a frame */
var_dump($stomp->readFrame());

/* close connection */
unset($stomp);

?>
```

以上例程的输出类似于：

    object(StompFrame)#2 (3) {
      ["command"]=>
      string(7) "MESSAGE"
      ["headers"]=>
      array(5) {
        ["message-id"]=>
        string(41) "ID:php.net-55293-1257226743606-4:2:-1:1:1"
        ["destination"]=>
        string(10) "/queue/foo"
        ["timestamp"]=>
        string(13) "1257226805828"
        ["expires"]=>
        string(1) "0"
        ["priority"]=>
        string(1) "0"
      }
      ["body"]=>
      string(3) "bar"
    }

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

/* subscribe to messages from the queue 'foo' */
stomp_subscribe($link, '/queue/foo');

/* read a frame */
$frame = stomp_read_frame($link);

/* close connection */
stomp_close($link);

?>
```

以上例程的输出类似于：

    array(3) {
      ["command"]=>
      string(7) "MESSAGE"
      ["body"]=>
      string(3) "bar"
      ["headers"]=>
      array(6) {
        ["transaction"]=>
        string(2) "t1"
        ["message-id"]=>
        string(41) "ID:php.net-55293-1257226743606-4:3:-1:1:1"
        ["destination"]=>
        string(10) "/queue/foo"
        ["timestamp"]=>
        string(13) "1257227037059"
        ["expires"]=>
        string(1) "0"
        ["priority"]=>
        string(1) "0"
      }
    }

Stomp::send
===========

stomp\_send
===========

Sends a message

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::send</span> ( <span
class="methodparam"><span class="type">string</span>
`$destination`</span> , <span class="methodparam"><span
class="type">mixed</span> `$msg`</span> \[, <span
class="methodparam"><span class="type">array</span> `$headers`</span> \]
)

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_send</span> ( <span class="methodparam"><span
class="type">resource</span> `$link`</span> , <span
class="methodparam"><span class="type">string</span>
`$destination`</span> , <span class="methodparam"><span
class="type">mixed</span> `$msg`</span> \[, <span
class="methodparam"><span class="type">array</span> `$headers`</span> \]
)

Sends a message to the Message Broker.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`destination`  
Where to send the message

`msg`  
Message to send.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**:
>
> A transaction header may be specified, indicating that the message
> acknowledgment should be part of the named transaction.

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

See <span class="function">stomp\_ack</span>.

Stomp::setReadTimeout
=====================

stomp\_set\_read\_timeout
=========================

Sets read timeout

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Stomp::setReadTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$seconds`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$microseconds`</span> \] )

过程化风格:

<span class="type">void</span> <span
class="methodname">stomp\_set\_read\_timeout</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">int</span>
`$seconds`</span> \[, <span class="methodparam"><span
class="type">int</span> `$microseconds`</span> \] )

Sets read timeout.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`seconds`  
The seconds part of the timeout to be set.

`microseconds`  
The microseconds part of the timeout to be set.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* connection */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Connection failed: ' . $e->getMessage());
}

$stomp->setReadTimeout(10);
    
/* close connection */
unset($stomp);

?>
```

**示例 \#2 过程化风格**

``` php
<?php

/* connection */
$link = stomp_connect('ssl://localhost:61612');

/* check connection */
if (!$link) {
    die('Connection failed: ' . stomp_connect_error());
}

stomp_set_read_timeout($link, 10);
    
/* close connection */
stomp_close($link);

?>
```

Stomp::subscribe
================

stomp\_subscribe
================

Registers to listen to a given destination

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::subscribe</span> ( <span
class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_subscribe</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

Registers to listen to a given destination.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`destination`  
Destination to subscribe to.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

See <span class="function">stomp\_ack</span>.

Stomp::unsubscribe
==================

stomp\_unsubscribe
==================

Removes an existing subscription

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Stomp::unsubscribe</span> ( <span
class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

过程化风格:

<span class="type">bool</span> <span
class="methodname">stomp\_unsubscribe</span> ( <span
class="methodparam"><span class="type">resource</span> `$link`</span> ,
<span class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">array</span> `$headers`</span> \] )

Removes an existing subscription.

### 参数

`link`  
仅对过程化样式：由 <span class="function">stomp\_connect</span> 返回的
stomp 连接标识符。

`destination`  
Subscription to remove.

`headers`  
关联数组包含附加的头信息（例如： receipt）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**小贴士**

Stomp is inherently asynchronous. Synchronous communication can be
implemented adding a receipt header. This will cause methods to not
return anything until the server has acknowledged receipt of the message
or until read timeout was reached.

### 范例

See <span class="function">stomp\_ack</span>.

简介
----

Represents a message which was sent or received from a Stomp compliant
Message Broker.

类摘要
------

**StompFrame**

<span class="ooclass"> class **StompFrame** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$command` ;

<span class="modifier">public</span> `$headers` ;

<span class="modifier">public</span> `$body` ;

/\* 方法 \*/

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$command`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$headers`</span> \[, <span class="methodparam"><span
class="type">string</span> `$body`</span> \]\]\] )

}

属性
----

`command`  
Frame command.

`headers`  
Frame headers (<span class="type">array</span>).

`body`  
Frame body.

StompFrame::\_\_construct
=========================

Constructor

### 说明

<span class="methodname">StompFrame::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$command`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$headers`</span> \[, <span class="methodparam"><span
class="type">string</span> `$body`</span> \]\]\] )

Constructor.

### 参数

`command`  
Frame command

`headers`  
Frame headers (<span class="type">array</span>).

`body`  
Frame body.

简介
----

Represents an error raised by the stomp extension. See
<a href="/language/exceptions.html" class="link">Exceptions</a> for more
information about Exceptions in PHP.

类摘要
------

**StompException**

<span class="ooclass"> class **StompException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDetails</span> ( <span
class="methodparam">void</span> )

}

StompException::getDetails
==========================

Get exception details

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">StompException::getDetails</span> ( <span
class="methodparam">void</span> )

Get exception details.

### 返回值

<span class="type">string</span> containing the error details.
