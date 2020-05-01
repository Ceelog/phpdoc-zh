预定义类
--------

<span class="classname">SAMConnection</span>
--------------------------------------------

Object representing a connection to a Messaging Server

构造函数
--------

-   <a href="/ref/sam.html#SAMConnection::__construct" class="link">new SAMConnection</a> -
    construct a new connection object to allow connection to a messaging
    infrastructure.

方法
----

-   <a href="/ref/sam.html#SAMConnection::commit" class="link">commit</a> -
    a method that commits (successfully completes) an in-flight unit of
    work.

-   <a href="/ref/sam.html#SAMConnection::connect" class="link">connect</a> -
    a method that connects a PHP script to a messaging server.

-   <a href="/ref/sam.html#SAMConnection::disconnect" class="link">disconnect</a> -
    a method that disconnects a PHP script from a messaging server.

-   <a href="/ref/sam.html#SAMConnection::isConnected" class="link">isConnected</a> -
    a method that checks whether a PHP script is connected to a
    messaging server.

-   <a href="/ref/sam.html#SAMConnection::peek" class="link">peek</a> -
    a method that receives a message from a queue without removing it
    from the queue.

-   <a href="/ref/sam.html#SAMConnection::peekAll" class="link">peekAll</a> -
    a method that receives one or messages from a queue without removing
    them from the queue.

-   <a href="/ref/sam.html#SAMConnection::receive" class="link">receive</a> -
    a method that receives a message from a queue or subscription.

-   <a href="/ref/sam.html#SAMConnection::remove" class="link">remove</a> -
    a method that removes a message from a queue.

-   <a href="/ref/sam.html#SAMConnection::rollback" class="link">rollback</a> -
    a method that cancels (rolls back) an in-flight unit of work.

-   <a href="/ref/sam.html#SAMConnection::send" class="link">send</a> -
    a method that sends a message to a queue or posts to a topic

-   <a href="/ref/sam.html#SAMConnection::setDebug" class="link">setDebug</a> -
    a method that switches additional debugging output on or off

-   <a href="/ref/sam.html#SAMConnection::subscribe" class="link">subscribe</a> -
    a method that creates a subscription to one or more topics

-   <a href="/ref/sam.html#SAMConnection::unsubscribe" class="link">unsubscribe</a> -
    a method that destroys a subscription to one or more topics

属性
----

-   <a href="/ref/sam.html#SAMConnection::errno" class="link">errno</a> -
    the numeric error code for the last encountered error on this
    connection. This property is set to 0 if the last operation was
    successful.

-   <a href="/ref/sam.html#SAMConnection::error" class="link">error</a> -
    the text description for the last encountered error on this
    connection

<span class="classname">SAMMessage</span>
-----------------------------------------

Object representing a message to be sent or received

构造函数
--------

-   <a href="/ref/sam.html#SAMMessage::__construct" class="link">new SAMMessage</a> -
    construct a new message.

属性
----

-   <a href="/ref/sam.html#SAMMessage::body" class="link">body</a> - the
    body of the message.

-   <a href="/ref/sam.html#SAMMessage::header" class="link">header</a> -
    the header properties of the message.

SAMConnection::commit
=====================

Commits (completes) the current unit of work

### 说明

<span class="type">bool</span> <span
class="methodname">SAMConnection::commit</span> ( <span
class="methodparam">void</span> )

Calling the "commit" method on a Connection object commits (completes)
all in-flight transactions that are part of the current unit of work.

### 返回值

This method returns **`FALSE`** if an error occurs.

### 范例

**示例 \#1 Committing the current unit of work**

``` php
<?php
  if (!$conn->commit()) {
    // The commit failed!
    echo "Commit failed ($conn->errno) $conn->error";
  }
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::rollback" class="xref"></a>

SAMConnection::connect
======================

Establishes a connection to a Messaging Server

### 说明

<span class="type">bool</span> <span
class="methodname">SAMConnection::connect</span> ( <span
class="methodparam"><span class="type">string</span> `$protocol`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$properties`</span> \] )

Calling the "connect" method on a SAMConnection object connects the PHP
script to a messaging server. No messages can be sent or received until
a connection is made.

### 参数

### 返回值

This method returns **`FALSE`** if an error occurs.

### 范例

**示例 \#1 Creating a connection to a Messaging Server using the IBM
MQSeries protocol (WMQ)**

``` php
<?php

$conn->connect(SAM_WMQ, array(SAM_HOST => 'Myhost.myco.com', SAM_PORT => 1506, SAM_BROKER => 'MyBroker'));

?>
```

**示例 \#2 Creating a connection with application transaction control
and default host and port values**

``` php
<?php

$conn->connect(SAM_WMQ, array(SAM_BROKER => 'MyBroker', SAM_TRANSACTIONS => SAM_MANUAL));

?>
```

**示例 \#3 Creating a connection to a Messaging Server using the IBM
WebSphere Platform Messaging protocol (WPM)**

``` php
<?php

$conn->connect(SAM_WPM, array(SAM_ENDPOINTS => 'localhost:7278:BootstrapBasicMessaging',
                              SAM_BUS => 'Bus1', SAM_TARGETCHAIN => 'InboundBasicMessaging'));

?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::isConnected" class="xref"></a>
-   <a href="/ref/sam.html#SAMConnection::disconnect" class="xref"></a>

SAMConnection::\_\_construct
============================

Creates a new connection to a Messaging Server

### 说明

<span class="methodname">SAMConnection::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a new <span class="classname">SAMConnection</span> object.

### 范例

**示例 \#1 Creating a connection object and connecting to a Messaging
Server**

``` php
<?php

$conn = new SAMConnection();
$conn->connect(SAM_WMQ, array(SAM_HOST => localhost, SAM_PORT => 1414, SAM_BROKER => 'bull'));

?>
```

SAMConnection::disconnect
=========================

Disconnects from a Messaging Server

### 说明

<span class="type">bool</span> <span
class="methodname">SAMConnection::disconnect</span> ( <span
class="methodparam">void</span> )

Calling the "disconnect" method on a SAMConnection object disconnects
the PHP script from a messaging server. No messages can be sent or
received after a connection has been disconnected.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Disconnecting from a Messaging Server**

``` php
<?php

$conn->disconnect();

?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::isConnected" class="xref"></a>
-   <a href="/ref/sam.html#SAMConnection::connect" class="xref"></a>

SAMConnection::errno
====================

Contains the unique numeric error code of the last executed SAM
operation

### Description

<span class="type">int</span>`$SAMConnection->errno`;

Contains the numeric error code of the last executed SAM operation on
this connection. If the last operation completed successfully this
property contains 0.

### 返回值

An integer greater than zero indicates the last error type encountered
on the connection. Zero indicates that the last operation on this
connection completed successfully.

### 范例

**示例 \#1 Using the error number and description properties**

``` php
<?php
$conn = new SAMConnection();
$conn->connect(SAM_WMQ, array(SAM_HOST => 'localhost', SAM_PORT => 1506));
$msg = new SAMMessage('This is a simple text item');
if (!$conn->send('topic://test', $msg)) {
    // The Send failed!
    echo "Send failed ($conn->errno) $conn->error";
}
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::error" class="xref"></a>

SAMConnection::error
====================

Contains the text description of the last failed SAM operation

### 说明

<span class="type">string</span>`$SAMConnection->error`;

Contains the text description of the last failed SAM operation on this
connection. If the last operation completed successfully this property
contains an empty string.

### 返回值

A string containing the text description of the last error type
encountered on the connection. An empty string indicates that the last
operation on this connection completed successfully.

### 范例

**示例 \#1 Using the error number and description properties**

``` php
<?php
$conn = new SAMConnection();
$conn->connect(SAM_WMQ, array(SAM_HOST => 'localhost', SAM_PORT => 1506));
$msg = new SAMMessage('This is a simple text item');
if (!$conn->send('topic://test', $msg)) {
    // The Send failed!
    echo "Send failed ($conn->errno) $conn->error";
}
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::errno" class="xref"></a>

SAMConnection::isConnected
==========================

Queries whether a connection is established to a Messaging Server

### 说明

<span class="type">bool</span> <span
class="methodname">SAMConnection::isConnected</span> ( <span
class="methodparam">void</span> )

Calling the "isConnected" method on a Connection object will check
whether the PHP script is connected to a messaging server. No messages
can be sent or received unless a connection has been established with a
Messaging server.

### 返回值

This method returns **`TRUE`** if the SAMConnection object is
successfully connected to a Messaging server or **`FALSE`** otherwise.

### 范例

**示例 \#1 Checking whether there us a connection to a Messaging
Server**

``` php
<?php

if ($conn->isConnected()) {
  echo 'Connection is active.';
} else {
  echo 'No active connection!';
}

?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::disconnect" class="xref"></a>
-   <a href="/ref/sam.html#SAMConnection::connect" class="xref"></a>

SAMConnection::peek
===================

Read a message from a queue without removing it from the queue

### 说明

<span class="type">SAMMessage</span> <span
class="methodname">SAMConnection::peek</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$properties`</span> \] )

### 参数

`target`  
The identity of the queue from which to peek the message.

`properties`  
An optional associative array of properties describing other parameters
to control the peek operation.

| Property name  | Possible values                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| SAM\_CORRELID  | This is the target correlation id string of the message. This would typically have been returned by a "send" request. |
| SAM\_MESSAGEID | This is the message id string of the message which is to be peeked.                                                   |

### 返回值

This method returns a SAMMessage object or **`FALSE`** if an error
occurs.

### 范例

**示例 \#1 Retrieve the next message from a queue without removing it**

``` php
<?php
$msg = $conn->peek('queue://receive/test');

if (!$msg) {
  // The peek failed!
  echo "Peek failed ($conn->errno) $conn->error";
}
?>
```

**示例 \#2 Retrieve a specific message from a queue without removing it
from the queue**

``` php
<?php

$msg = $conn->peek('queue://receive/test', array(SAM_MESSAGEID => $messageId));

?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::peekAll" class="xref"></a>

SAMConnection::peekAll
======================

Read one or more messages from a queue without removing it from the
queue

### 说明

<span class="type">array</span> <span
class="methodname">SAMConnection::peekAll</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$properties`</span> \] )

### 参数

`target`  
The identity of the queue from which messages should be peeked.

`properties`  
An optional associative array of properties describing other parameters
to control the peek operation.

| Property name  | Possible values                                                                                                                 |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| SAM\_CORRELID  | This is the target correlation id string of messages to be peeked. This would typically have been returned by a "send" request. |
| SAM\_MESSAGEID | This is the message id string of a message which is to be peeked.                                                               |

### 返回值

This method returns an array of SAMMessage objects or **`FALSE`** if an
error occurs.

### 范例

**示例 \#1 Retrieve all messages in a queue without removing them**

``` php
<?php
$msgArray = $conn->peekAll('queue://receive/test');
if ($msgArray) {
   foreach ( $msgArray as $key => $msg) {
       echo "Message $key: body = $msg->body\n";
   }
} else {
   echo "PeekAll failed ($conn->errno) $conn->error";
}
?>
```

**示例 \#2 Retrieve all messages from a queue with a matching
correlation id**

``` php
<?php

   $msgArray = $conn->peekAll('queue://receive/test', array(SAM_CORRELID => $correlId ));
   if ($msgArray) {

      foreach ( $msgArray as $key => $msg) {
            echo "Message $key: body = $msg->body\n";
         }
   } else {
      echo "PeekAll failed ($conn->errno) $conn->error";
   }

?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::peek" class="xref"></a>

SAMConnection::receive
======================

Receive a message from a queue or subscription

### 说明

<span class="type">SAMMessage</span> <span
class="methodname">SAMConnection::receive</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$properties`</span> \] )

### 参数

`target`  
The identity of the queue, topic or subscription from which to receive
the message.

`properties`  
An optional associative array of properties describing other parameters
to control the receive operation.

| Property name  | Possible values                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SAM\_CORRELID  | Used to request selection of the message to receive based upon the correlation id string of the message.                                                                                                                                                                                                                                                                                           |
| SAM\_MESSAGEID | Used to request selection of the message to receive based upon the message id string of the message.                                                                                                                                                                                                                                                                                               |
| SAM\_WAIT      | Timeout value in milliseconds to control how long the request should block waiting to receive a message before returning with a failure if no message is available on the queue or topic. The default value is 0 meaning wait indefinitely and should be used with caution as the request may wait until the overall PHP script processing time limit has expired if no message becomes available. |

### 返回值

This method returns a SAMMessage object or **`FALSE`** if an error
occurs.

### 范例

**示例 \#1 Receiving a message from a queue**

``` php
<?php
$msg = $conn->receive('queue://receive/test');

if (!$msg) {
  // The receive failed!
  echo "Receive failed ($conn->errno) $conn->error";
}
?>
```

**示例 \#2 Receiving a message from a queue with options**

In this example the SAM\_CORRELID option is used to specify a
correlation id string to be used to identify the message to receive. A
wait timeout of 10 seconds is also specified.

``` php
<?php

$msg = $conn->receive('queue://receive/test', array(SAM_CORRELID => $token, SAM_WAIT => 10000));

?>
```

**示例 \#3 Receiving a message from a subscription**

In this example we show how to receive a message from a subscription id.

``` php
<?php
$msg = $conn->receive($subscriptionName);

if (!$msg) {
  // The receive failed!
  echo "Receive failed ($conn->errno) $conn->error";
}
?>
```

Please note that $subscriptionName is a subscription id returned from an
earlier subscribe call.

### 参见

-   <a href="/ref/sam.html#SAMConnection::send" class="xref"></a>

SAMConnection::remove
=====================

Remove a message from a queue

### 说明

<span class="type">SAMMessage</span> <span
class="methodname">SAMConnection::remove</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$properties`</span> \] )

Removes a message from a queue.

### 参数

`target`  
The identity of the queue from which to remove the message.

`properties`  
An optional associative array of properties describing other parameters
to control the remove operation.

| Property name  | Possible values                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| SAM\_CORRELID  | This is the target correlation id string of the message. This would typically have been returned by a "send" request. |
| SAM\_MESSAGEID | This is the message id string of the message which is to be removed.                                                  |

### 返回值

This method returns **`FALSE`** if an error occurs.

### 范例

**示例 \#1 Removing a message from a queue by message id**

``` php
<?php
if (!$conn->remove('queue://receive/test', array(SAM_MESSAGEID => $messageId))) {
  // The remove failed!
  echo "Remove failed ($conn->errno) $conn->error";
}
?>
```

SAMConnection::rollback
=======================

Cancels (rolls back) an in-flight unit of work

### 说明

<span class="type">bool</span> <span
class="methodname">SAMConnection::rollback</span> ( <span
class="methodparam">void</span> )

Rolls back an in-flight unit of work.

### 返回值

This method returns **`FALSE`** if an error occurs.

### 范例

**示例 \#1 Cancelling an in-flight unit of work**

``` php
<?php
if (!$conn->rollback()) {
  // The rollback failed!
  echo "Rollback failed ($conn->errno) $conn->error";
}
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::commit" class="xref"></a>

SAMConnection::send
===================

Send a message to a queue or publish an item to a topic

### 说明

<span class="type">string</span> <span
class="methodname">SAMConnection::send</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span> ,
<span class="methodparam"><span class="type">SAMMessage</span>
`$msg`</span> \[, <span class="methodparam"><span
class="type">array</span> `$properties`</span> \] )

The "send" method is used to send a message to a specific queue or to
publish to a specific topic. The method returns a correlation id that
can be used as a selector to identify reply or response messages when
these are requested.

### 参数

`target`  
If sending a message, the identity of the queue (*queue://queuename*) or
if publishing to a topic the identity of the topic (*topic://topicname*)
to which the message is to be delivered.

`msg`  
The message to be sent or published.

`properties`  
An optional associative array of properties describing other parameters
to control the receive operation.

| Property name            | Possible values                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SAM\_DELIVERYMODE        | Indicates whether the messaging server should ensure delivery or whether it is acceptable for messages to be lost in the case of system failures. The value of this property may be set to either **`SAM_PERSISTENT`**, to indicate that message loss is not acceptable, or **`SAM_NON_PERSISTENT`**, if message loss is acceptable. The resulting behaviour of the send will vary depending on the capabilities of the messaging server the PHP script is currently connected to. If the server does not support persistent messages and **`SAM_PERSISTENT`** is specified the send request will fail with an error indication showing the capability is not available. |
| SAM\_PRIORITY            | A numeric value between 0 and 9 indicating the desired message delivery priority. A priority value of 0 indicates the lowest priority while 9 indicates highest priority. If no priority is specified a default will be assigned which is dependent on the messaging server being used.                                                                                                                                                                                                                                                                                                                                                                                  |
| SAM\_CORRELID            | A string to be assigned as a correlation id for this message. If no value is given the messaging server may assign a value automatically.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SAM\_TIMETOLIVE          | A time in milliseconds indicating how long the messaging server should retain the message on a queue before discarding it. The default value is 0 indicating the message should be retained indefinitely.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SAM\_WMQ\_TARGET\_CLIENT | This property is only valid when using WebSphere MQ and indicates whether or not an RFH2 header should be included with the message. This option may be set to either 'jms' or 'mq'. The default is 'jms' which means that an RFH2 header is included. If the value 'mq' is specified then no RFH2 is included with the message.                                                                                                                                                                                                                                                                                                                                         |

### 返回值

A correlation id string that can be used in a subsequent receive call as
a selector to obtain any reply or response that has been requested or
**`FALSE`** if an error occurred.

> **Note**:
>
> A correlation id will only be returned for a successful send to a
> queue destination (*queue://xxxx*) in which case it will reflect the
> message identity of the message on the queue. In the case of a send
> being used to publish data to a topic the return value will be
> **`TRUE`** as no correlation id is available for return.

### 范例

**示例 \#1 Send a message to a queue**

``` php
<?php
$msg = new SAMMessage('This is a simple text message');
$correlId = $conn->send('queue://send/test', $msg);
if (!$correlId) {
    // The send failed!
    echo "Send failed ($conn->errno) $conn->error";
}

?>
```

**示例 \#2 Publish a message to a topic**

``` php
<?php
$msg = new SAMMessage('This is a simple text item');
if (!$conn->send('topic://test', $msg)) {
    // The Send failed!
    echo "Send failed ($conn->errno) $conn->error";
}
?>
```

**示例 \#3 Send a request and receive a response**

``` php
<?php
$msg = new SAMMessage('This is a simple text message');
$msg->header->SAM_REPLY_TO = 'queue://receive/test';
$correlid = $conn->send('queue://send/test', $msg);

if (!$correlid) {
    // The Send failed!
    echo "Send failed ($conn->errno) $conn->error";
} else {
    $resp = $conn->receive('queue://receive/test', array(SAM_CORRELID => $correlid));
}
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::receive" class="xref"></a>

SAMConnection::setDebug
=======================

Turn on or off additional debugging output

### 说明

The "setdebug" method is used to turn on or off additional debugging
output. The SAM framework will provide method/function entry and exit
trace data plus additional information. Protocol specific
implementations also provide extra output.

<span class="type">void</span> <span
class="methodname">SAMConnection::setDebug</span> ( <span
class="methodparam"><span class="type">bool</span> `$switch`</span> )

### 参数

`switch`  
If this parameter is set to **`TRUE`** additional debugging output will
be provided. If the value is set to **`FALSE`** output of additional
information will be stopped.

### 返回值

没有返回值。

### 范例

**示例 \#1 Turn on debugging output**

``` php
<?php
$conn->setdebug(TRUE);
?>
```

**示例 \#2 Turn off debugging output**

``` php
<?php
$conn->setdebug(FALSE);
?>
```

SAMConnection::subscribe
========================

Create a subscription to a specified topic

### 说明

<span class="type">string</span> <span
class="methodname">SAMConnection::subscribe</span> ( <span
class="methodparam"><span class="type">string</span>
`$targetTopic`</span> )

The "subscribe" method is used to create a new subscription to a
specified topic.

### 参数

`targetTopic`  
The identity of the topic (topic://topicname) to subscribe to.

### 返回值

A subscription identifier that can be used in a subsequent receive call
as a selector to obtain any topic data or **`FALSE`** if an error
occurred. The subscription identifier should be used in the receive call
in place of the simple topic name.

### 范例

**示例 \#1 Subscribe to a topic**

``` php
<?php
$subid = $conn->subscribe('topic://A');
if (!$subid) {
  // The subscribe failed!
  echo "Subscribe failed ($conn->errno) $conn->error";
}
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::unsubscribe" class="xref"></a>

SAMConnection::unsubscribe
==========================

Cancel a subscription to a specified topic

### 说明

<span class="type">bool</span> <span
class="methodname">SAMConnection::unsubscribe</span> ( <span
class="methodparam"><span class="type">string</span>
`$subscriptionId`</span> \[, <span class="methodparam"><span
class="type">string</span> `$targetTopic`</span> \] )

The "unsubscribe" method is used to delete an existing subscription to a
specified topic.

### 参数

`subscriptionId`  
The identifier of an existing subscription as returned by a call to the
subscribe method.

### 返回值

This method returns **`FALSE`** if an error occurs.

### 范例

**示例 \#1 Delete a subscription**

``` php
<?php
if (!$conn->unsubscribe($subid)) {
    // The unsubscribe failed!
    echo "Unsubscribe failed ($conn->errno) $conn->error";
}
?>
```

### 参见

-   <a href="/ref/sam.html#SAMConnection::subscribe" class="xref"></a>

SAMMessage::body
================

The body of the message

### 说明

<span class="type">string</span>`$SAMMessage->body`;

The "body" property contains the actual body of the message. It may not
always be set.

### 范例

**示例 \#1 Setting a text string into the body of a message**

``` php
<?php
$msg = new SAMMessage();
$msg->body = 'This is a simple message';

?>
```

### 参见

-   <a href="/ref/sam.html#SAMMessage::header" class="xref"></a>

SAMMessage::\_\_construct
=========================

Creates a new Message object

### 说明

<span class="methodname">SAMMessage::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$body`</span> \] )

Creates a new <span class="classname">SAMMessage</span> object
optionally specifying a message body.

### 参数

`body`  
The optional body for the message.

### 范例

**示例 \#1 Creating a message**

``` php
<?php

$msg = new SAMMessage();

?>
```

**示例 \#2 Creating a message with a simple text payload**

``` php
<?php

$msg = new SAMMessage('This is a simple text message');

?>
```

SAMMessage::header
==================

The header properties of the message

### 说明

<span class="type">object</span>`$SAMMessage->header`;

The *header* property is a container for any system or user properties
that area associated with the message.

Properties may be assigned by the sender of a message to control the way
the messaging systems handles it or may be assigned by the messaging
system itself to tell the recipient extra information about the message
or the way in which it has been handled.

Some properties are understood by SAM in which case constants have been
defined for them. The majority of properties however are ignored by the
SAM implementation and simply passed through to the underlying messaging
systems allowing the application to use messaging specific property
names or to define its own "user" properties.

The SAM defined properties are as follows:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Property name</th>
<th>Possible values</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>SAM_MESSAGEID</code></strong></td>
<td>When a message is received this field contains the unique identifier of the message as allocated by the underlying messaging system. When sending a message this field is ignored.</td>
</tr>
<tr class="even">
<td><strong><code>SAM_REPLY_TO</code></strong></td>
<td>A string providing the identity of the queue on to which responses to this message should be posted.</td>
</tr>
<tr class="odd">
<td><strong><code>SAM_TYPE</code></strong></td>
<td><p>An indication of the type of message to be sent. The value may be <strong><code>SAM_TEXT</code></strong> indicating the contents of the message body is a text string, or <strong><code>SAM_BYTES</code></strong> indicating the contents of the message body are some application defined format.</p>
<p>The way in which this property is used may depend on the underlying messaging server. For instance a messaging server that supports the <em>JMS (Java Message Service)</em> specification may interpret this value and send messages of type "<em>jms_text</em>" and "<em>jms_bytes</em>". In addition, if the <strong><code>SAM_TYPE</code></strong> property is set to <strong><code>SAM_TEXT</code></strong> the data provided for the message body is expected to be a UTF8 encoded string.</p></td>
</tr>
</tbody>
</table>

When setting the values of properties it is often useful to give a hint
as to the format in which the property should be delivered to the
messaging system. By default property values are delivered as text and
the following simple syntax may be used to set a value:

**示例 \#1 Setting a text format property using the default syntax**

``` php
<?php
$msg = new SAMMessage();

$msg->header->myPropertyName = 'textData';
?>
```

If it is desired to pass type information an alternative syntax may be
used where the value and the type hint are passed in an associative
array:

**示例 \#2 Setting a text format property using a type hint**

``` php
<?php
$msg = new SAMMessage();

$msg->header->myPropertyName = array('textData', SAM_STRING);
?>
```

When passing a type hint the type entry should be one of the SAM defined
constant values as defined by the following table:

| Constant          | Type description                                                                                                                                                                                                                                                                                                                                               |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`SAM_BOOLEAN`** | Any value passed will be interpreted as logical true or false. If the value cannot be interpreted as a PHP boolean value the value passed to the messaging system is undefined.                                                                                                                                                                                |
| **`SAM_BYTE`**    | An 8-bit signed integer value. SAM will attempt to convert the property value specified into a single byte value to pass to the messaging system. If a string value is passed an attempt will be made to interpret the string as a numeric value. If the numeric value cannot be expressed as an 8-bit signed binary value data may be lost in the conversion. |
| **`SAM_DOUBLE`**  | A long floating point value. SAM will attempt to convert the property value specified into a floating point value with 15 digits of precision. If a string value is passed an attempt will be made to interpret the string as a numeric value. If the passed value cannot be expressed as a 15 digit floating point value data may be lost in the conversion.  |
| **`SAM_FLOAT`**   | A short floating point value. SAM will attempt to convert the property value specified into a floating point value with 7 digits of precision. If a string value is passed an attempt will be made to interpret the string as a numeric value. If the passed value cannot be expressed as a 7 digit floating point value data may be lost in the conversion.   |
| **`SAM_INT`**     | An 32-bit signed integer value. SAM will attempt to convert the property value specified into a 32-bit value to pass to the messaging system. If a string value is passed an attempt will be made to interpret the string as a numeric value. If the numeric value cannot be expressed as an 32-bit signed binary value data may be lost in the conversion.    |
| **`SAM_LONG`**    | An 64-bit signed integer value. SAM will attempt to convert the property value specified into a 64-bit value to pass to the messaging system. If a string value is passed an attempt will be made to interpret the string as a numeric value. If the numeric value cannot be expressed as an 64-bit signed binary value data may be lost in the conversion.    |
| **`SAM_STRING`**  | SAM will interpret the property value specified as a string and pass it to the messaging system accordingly.                                                                                                                                                                                                                                                   |

### 范例

**示例 \#3 Setting properties as the sender of a message**

``` php
<?php
$msg = new SAMMessage('This is a test message');

// defining SAM specific properties...
$msg->header->SAM_REPLY_TO = 'queue://test/replyQueue';

// defining arbitrary properties...
//
// a default string property
$msg->header->myStringProp1 = 'a string property';
// a string property with a type hint
$msg->header->myStringProp2 = array('another string property', SAM_STRING);

// a boolean property
$msg->header->myBoolProp = array(FALSE, SAM_BOOL);

// numeric format properties
$msg->header->myIntProp = array(32768, SAM_INT);
$msg->header->myLongProp = array(9876543, SAM_LONG);
$msg->header->myByteProp1 = array(123, SAM_BYTE);
$msg->header->myByteProp2 = array('12', SAM_BYTE);
$msg->header->myFloatProp = array(3.141592, SAM_FLOAT);
$msg->header->myDoubleProp = array(3.14159265358979, SAM_DOUBLE);
?>
```

**示例 \#4 Retreiving property values from a message**

``` php
<?php

// accessing an application specific property
$intProp = $msg->header->MyIntProp;

// accessing a messaging system specific property
$encoding = $msg->header->JMS_IBM_Msgtype;

?>
```

### 参见

-   <a href="/ref/sam.html#SAMMessage::body" class="xref"></a>

**目录**

-   [SAMConnection::commit](/ref/sam.html#SAMConnection::commit) —
    Commits (completes) the current unit of work
-   [SAMConnection::connect](/ref/sam.html#SAMConnection::connect) —
    Establishes a connection to a Messaging Server
-   [SAMConnection::\_\_construct](/ref/sam.html#SAMConnection::__construct)
    — Creates a new connection to a Messaging Server
-   [SAMConnection::disconnect](/ref/sam.html#SAMConnection::disconnect)
    — Disconnects from a Messaging Server
-   [SAMConnection::errno](/ref/sam.html#SAMConnection::errno) —
    Contains the unique numeric error code of the last executed SAM
    operation
-   [SAMConnection::error](/ref/sam.html#SAMConnection::error) —
    Contains the text description of the last failed SAM operation
-   [SAMConnection::isConnected](/ref/sam.html#SAMConnection::isConnected)
    — Queries whether a connection is established to a Messaging Server
-   [SAMConnection::peek](/ref/sam.html#SAMConnection::peek) — Read a
    message from a queue without removing it from the queue
-   [SAMConnection::peekAll](/ref/sam.html#SAMConnection::peekAll) —
    Read one or more messages from a queue without removing it from the
    queue
-   [SAMConnection::receive](/ref/sam.html#SAMConnection::receive) —
    Receive a message from a queue or subscription
-   [SAMConnection::remove](/ref/sam.html#SAMConnection::remove) —
    Remove a message from a queue
-   [SAMConnection::rollback](/ref/sam.html#SAMConnection::rollback) —
    Cancels (rolls back) an in-flight unit of work
-   [SAMConnection::send](/ref/sam.html#SAMConnection::send) — Send a
    message to a queue or publish an item to a topic
-   [SAMConnection::setDebug](/ref/sam.html#SAMConnection::setDebug) —
    Turn on or off additional debugging output
-   [SAMConnection::subscribe](/ref/sam.html#SAMConnection::subscribe) —
    Create a subscription to a specified topic
-   [SAMConnection::unsubscribe](/ref/sam.html#SAMConnection::unsubscribe)
    — Cancel a subscription to a specified topic
-   [SAMMessage::body](/ref/sam.html#SAMMessage::body) — The body of the
    message
-   [SAMMessage::\_\_construct](/ref/sam.html#SAMMessage::__construct) —
    Creates a new Message object
-   [SAMMessage::header](/ref/sam.html#SAMMessage::header) — The header
    properties of the message
