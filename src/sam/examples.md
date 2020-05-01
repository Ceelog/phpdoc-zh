范例
====

**目录**

-   [Connections](/sam/examples.html#Connections)
-   [Messages](/sam/examples.html#Messages)
-   [Messaging operations](/sam/examples.html#Messaging%20operations)
-   [Publish/Subscribe and subscriptions to
    topics](/sam/examples.html#Publish/Subscribe%20and%20subscriptions%20to%20topics)
-   [Error handling](/sam/examples.html#Error%20handling)

Connections
-----------

In order to perform any messaging and queueing functions a connection
must be established with a messaging server by creating a SAMConnection
object and calling its "connect" method, with a set of connection
properties, to connect the PHP script to the messaging server. Until
such time as the SAMConnection object is destroyed the connection will
be maintained and available for use. All SAMConnection objects are
destroyed when the PHP script exits.

A set of default properties may be used in connecting to a messaging
server but as a minimum the PHP script must specify a protocol to be
used.

**示例 \#1 Creating a connection and connecting to a remote WebSphere
MQSeries Messaging Server**

``` php
<?php
$conn = new SAMConnection();
$conn->connect(SAM_WMQ, array(SAM_HOST => 'myhost.mycompany.com',
                              SAM_PORT => 1506,
                              SAM_BROKER => 'mybroker'));
?>
```

**示例 \#2 Creating a connection and connecting to a remote WebSphere
Application Server**

``` php
<?php
$conn = new SAMConnection();
$conn->connect(SAM_WPM, array(SAM_ENDPOINTS => 'localhost:7278:BootstrapBasicMessaging',
                              SAM_BUS => 'Bus1',
                              SAM_TARGETCHAIN => 'InboundBasicMessaging'));
?>
```

**示例 \#3 Creating a connection and connecting to an MQTT server**

``` php
<?php
$conn = new SAMConnection();
$conn->connect(SAM_MQTT, array(SAM_HOST => 'myhost.mycompany.com',
                               SAM_PORT => 1883));
?>
```

Messages
--------

Messages sent to and received from queues are represented by the
SAMMessage object. The SAMMessage object encapsulates the body of the
message (if one exists) and the header properties associated with the
message. A SAMMessage object is either supplied as a parameter to a
messaging operation or returned as a result.

**示例 \#1 Creating a message with a simple text body**

``` php
<?php
$msg = new SAMMessage('This is a simple text message');
?>
```

Messages may have header properties associated with them that provide
control over the transport of the message or further information to the
receiving application. By default message properties are delivered to
the underlying messaging system as strings and in this case they may be
set with the following simple syntax:

**示例 \#2 Setting a text format property using the default syntax**

``` php
<?php
$msg->header->myPropertyName = 'textData';
?>
```

If it is desired to pass type information an alternative syntax may be
used where the value and the type hint are passed in an associative
array:

**示例 \#3 Setting a property using a type hint**

``` php
<?php
$msg->header->myPropertyName = array(3.14159, SAM_FLOAT);
?>
```

Properties may also be extracted from the header of a message.

**示例 \#4 Retrieving a property from a message header**

``` php
<?php
$myProperty = $msg->header->myPropertyName;
?>
```

Messaging operations
--------------------

All messaging operations are performed through calls to methods on the
connection object. To add a message to a queue the "send" method is
used, to obtain a message from a queue the "receive" method is used.
Other methods provide publish and subscribe functionality and control of
transaction boundaries.

**示例 \#1 Adding a message to a queue and receiving a response**

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

Publish/Subscribe and subscriptions to topics
---------------------------------------------

SAM allows messages to be sent either to queues or, for WebSphere MQ and
WPM, to publish/subscribe topics. A topic destination is specified to
SAM in the usual way, i.e. in the form 'topic://fred', rather than the
form 'queue://AQUEUE' used for point to point operation. To use
publish/subscribe it is simply necessary to specify the correct broker
name on the SAMConnect "connect" call and the desired topic in the
destination argument to the SAMConnect "send" and "receive" calls. The
PHP interface is otherwise identical to the point to point model.

By default, SAM creates non-durable subscriptions when using
publish/subscribe. This means that if a client application is inactive
when messages are published to a topic, then it will not receive them
when it subsequently restarted. SAM does also allow durable
subscriptions to be made to topics when using WPM or WebSphere MQ
publish/subscribe. The purpose of these subscriptions is to allow data
to be received by a client application even if that client was not
active at the time the data was published.

Durable subscriptions are specified by using the SAMConnect "subscribe"
call. This method takes the destination topic as an input parameter and
returns a subscription identifier that may be used on subsequent
"receive" calls. When the subscription is no longer required the
SAMConnection "unsubscribe" method should be used to delete the
subscription.

**示例 \#1 Creating a durable subscription to a topic**

``` php
<?php

$subName = $conn->subscribe('topic://A');

if (!$subName) {
   echo "Subscribe failed";
} else {
   # Subscribe was OK
   // ...
}
?>
```

**示例 \#2 Subscribing to a topic using a WebSphere Platform Messaging
(WPM) server**

``` php
<?php
$conn = new SAMConnection();
// Note: For pub/sub on WPM, when connecting the name of a messaging engine
//   to hold the durable subscription (SAM_WPM_DUR_SUB_HOME) must be specified.
$conn->connect(SAM_WMQ, array(SAM_ENDPOINTS => 'localhost:7278:BootstrapBasicMessaging',
                              SAM_BUS => 'Bus1',
                              SAM_TARGETCHAIN => 'InboundBasicMessaging',
                              SAM_WPM_DUR_SUB_HOME => 'MyMachineNode01.server1-Bus1'));

$subName = $conn->subscribe('topic://A');

if (!$subName) {
   echo "Subscribe failed";
} else {
   # Subscribe was OK
   // ...
}
?>
```

**示例 \#3 Receiving published data using a durable subscription**

``` php
<?php

$msg = $conn->receive($subName);
if ($msg) {
   echo "Received a message OK";
} else {
   echo "The receive failed";
}

?>
```

**示例 \#4 Deleting a durable subscription to a topic**

``` php
<?php

if (!$conn->unsubscribe($subName)) {
   echo "Unsubscribe failed";
}

?>
```

Error handling
--------------

All SAMConnection methods that provide access to messaging operations
return **`FALSE`** if an error occurred in processing the request. In
addition the SAMConnection object has two properties, "errno" and
"error", that provide respectively the error number and text description
of the last error to occur on the connection.

**示例 \#1 Handling an error from a method that returns no result**

``` php
<?php
if (!$conn->commit()) {
    // The commit failed!
    echo "Commit failed ($conn->errno) $conn->error";
}
?>
```

**示例 \#2 Handling an error from a method that returns a result**

``` php
<?php
$correlid = $conn->send('queue://send/test', $msg);

if (!$correlid) {
  // The Send failed!
  echo "Send failed ($conn->errno) $conn->error";
} else {
  /* ... */
}
?>
```
