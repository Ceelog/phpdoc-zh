mqseries\_back
==============

MQSeries MQBACK

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_back</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_back</span> (MQBACK) call indicates
to the queue manager that all the message gets and puts that have
occurred since the last syncpoint are to be backed out. Messages put as
part of a unit of work are deleted; messages retrieved as part of a unit
of work are reinstated on the queue.

Using <span class="function">mqseries\_back</span> only works in
conjunction with <span class="function">mqseries\_begin</span> and only
function when connecting directly to a Queueu manager. Not via the
mqclient interface.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_back</span> example**

``` php
<?php
    mqseries_back($conn, $comp_code, $reason);

    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### 注释

> **Note**:
>
> <span class="function">mqseries\_back</span> will not function when
> using MQSeries Client to connect to a Queueu Manager.

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>
-   <span class="function">mqseries\_begin</span>

mqseries\_begin
===============

MQseries MQBEGIN

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_begin</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">array</span>
`$beginOptions`</span> , <span class="methodparam"><span
class="type">resource</span> `&$compCode`</span> , <span
class="methodparam"><span class="type">resource</span> `&$reason`</span>
)

The <span class="function">mqseries\_begin</span> (MQBEGIN) call begins
a unit of work that is coordinated by the queue manager, and that may
involve external resource managers.

Using <span class="function">mqseries\_begin</span> starts the unit of
work. Either <span class="function">mqseries\_back</span> or <span
class="function">mqseries\_cmit</span> ends the unit of work.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_begin</span> example**

``` php
<?php
    $mqbo = array();
    mqseries_begin( $conn, 
                    $mqbo,
                    $comp_code,
                    $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        /* reason code 2121 is a warning for more information see MQSeries reference manual.*/
        if ($reason !== 2121) {
            printf("CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        }
    }
?>
```

### 注释

> **Note**:
>
> <span class="function">mqseries\_begin</span> will not function when
> using MQSeries Client to connect to a Queueu Manager.

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>
-   <span class="function">mqseries\_back</span>
-   <span class="function">mqseries\_cmit</span>

mqseries\_close
===============

MQSeries MQCLOSE

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$hobj`</span> , <span class="methodparam"><span class="type">int</span>
`$options`</span> , <span class="methodparam"><span
class="type">resource</span> `&$compCode`</span> , <span
class="methodparam"><span class="type">resource</span> `&$reason`</span>
)

The <span class="function">mqseries\_close</span> (MQCLOSE) call
relinquishes access to an object, and is the inverse of the <span
class="function">mqseries\_open</span> (MQOPEN) call.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`hObj`  
Object handle.

This handle represents the object to be used.

`options`  

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_close</span> example**

``` php
<?php
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("close CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### 参见

-   <span class="function">mqseries\_open</span>
-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>

mqseries\_cmit
==============

MQSeries MQCMIT

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_cmit</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_cmit</span> (MQCMIT) call indicates
to the queue manager that the application has reached a syncpoint, and
that all of the message gets and puts that have occurred since the last
syncpoint are to be made permanent. Messages put as part of a unit of
work are made available to other applications; messages retrieved as
part of a unit of work are deleted.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_cmit</span> example**

``` php
<?php
    mqseries_cmit($conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("cmit CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### 注释

> **Note**:
>
> <span class="function">mqseries\_back</span> will not function when
> using MQSeries Client to connect to a Queueu Manager.

### 参见

-   <span class="function">mqseries\_begin</span>
-   <span class="function">mqseries\_back</span>
-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>

mqseries\_conn
==============

MQSeries MQCONN

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_conn</span> ( <span
class="methodparam"><span class="type">string</span>
`$qManagerName`</span> , <span class="methodparam"><span
class="type">resource</span> `&$hconn`</span> , <span
class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_conn</span> (MQCONN) call connects
an application program to a queue manager. It provides a queue manager
connection handle, which is used by the application on subsequent
message queuing calls.

### 参数

`qManagerName`  
Name of queue manager.

Name of the queue manager the application wishes to connect.

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_conn</span> example**

``` php
<?php
    mqseries_conn('WMQ1', $conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("conn CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

### 参见

-   <span class="function">mqseries\_disc</span>

mqseries\_connx
===============

MQSeries MQCONNX

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_connx</span> ( <span
class="methodparam"><span class="type">string</span>
`$qManagerName`</span> , <span class="methodparam"><span
class="type">array</span> `&$connOptions`</span> , <span
class="methodparam"><span class="type">resource</span> `&$hconn`</span>
, <span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_connx</span> (MQCONNX) call
connects an application program to a queue manager. It provides a queue
manager connection handle, which is used by the application on
subsequent MQ calls.

The <span class="function">mqseries\_connx</span> call is like the <span
class="function">mqseries\_conn</span> (MQCONN) call, except that
MQCONNX allows options to be specified to control the way that the call
works.

### 参数

`qManagerName`  
Name of queue manager.

Name of the queue manager the application wishes to connect.

`connOps`  
Options that control the action of function

See also the MQCNO structure.

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_connx</span> example**

``` php
<?php
    $mqcno = array(
        'Version' => MQSERIES_MQCNO_VERSION_2,
        'Options' => MQSERIES_MQCNO_STANDARD_BINDING,
        'MQCD' => array('ChannelName' => 'MQNX9420.CLIENT',
        'ConnectionName' => 'localhost',
        'TransportType' => MQSERIES_MQXPT_TCP)
    );

    mqseries_connx('MQNX9420', $mqcno, $conn, $comp_code,$reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("Connx CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
 
?>
```

**示例 \#2 <span class="function">mqseries\_connx</span> example using
SSL connection & OCSP Responder URL**

``` php
<?php
    $mqcno = array(
        'Version' => 4, //MQCNO_VERSION_4
        'Options' => MQSERIES_MQCNO_STANDARD_BINDING,
        'MQCD' => array(
            'Version' => 7, //MQCD_VERSION_7
            'ConnectionName' => 'localhost', 
            'TransportType' => MQSERIES_MQXPT_TCP, 
            'ChannelName' => 'CONNECTIONCHANNEL', 
            'SSLCipherSpec' => 'NULL_SHA'
        ), 
        'MQSCO' => array(
            'KeyRepository' => '/var/mqm/qmgrs/QUEUEMGR/ssl/key', //Local path where the SSL key repository can be found
            'MQAIR' => array(
                'Version' => 2, //MQAIR_VERSION_2
                'AuthInfoType' => 2, //MQAIT_OCSP 
                'OCSPResponderURL' => 'http://dummy.OCSP.responder'
            )
        )
    );

    mqseries_connx('QUEUEMGR', $mqcno, $conn, $comp_code,$reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("Connx CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
 
?>
```

### 参见

-   <span class="function">mqseries\_disc</span>

mqseries\_disc
==============

MQSeries MQDISC

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_disc</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_disc</span> (MQDISC) call breaks
the connection between the queue manager and the application program,
and is the inverse of the <span class="function">mqseries\_conn</span>
(MQCONN) or <span class="function">mqseries\_connx</span> (MQCONNX)
call.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_disc</span> example**

``` php
<?php
    mqseries_disc($conn, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("disc CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }
?>
```

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>

mqseries\_get
=============

MQSeries MQGET

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_get</span> ( <span
class="methodparam"><span class="type">resource</span> `$hConn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$hObj`</span> , <span class="methodparam"><span
class="type">array</span> `&$md`</span> , <span
class="methodparam"><span class="type">array</span> `&$gmo`</span> ,
<span class="methodparam"><span class="type">int</span>
`&$bufferLength`</span> , <span class="methodparam"><span
class="type">string</span> `&$msg`</span> , <span
class="methodparam"><span class="type">int</span> `&$data_length`</span>
, <span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_get</span> (MQGET) call retrieves a
message from a local queue that has been opened using the <span
class="function">mqseries\_open</span> (MQOPEN) call

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`hObj`  
Object handle.

This handle represents the object to be used.

`md`  
Message descriptor (MQMD).

`gmo`  
Get message options (MQGMO).

`bufferLength`  
Expected length of the result buffer

`msg`  
Buffer holding the message that was retrieved from the object.

`data_length`  
Actual buffer length

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_get</span> example**

``` php
<?php
// open connection to the queue manager
    mqseries_conn('WMQ1', $conn, $comp_code, $reason);
// $conn now hold the reference to the connection to the queue manager.

// open the connection to the testq queue
    mqseries_open(
                $conn,
                array('ObjectName' => 'TESTQ'),
                MQSERIES_MQOO_INPUT_AS_Q_DEF | MQSERIES_MQOO_FAIL_IF_QUIESCING | MQSERIES_MQOO_OUTPUT,
                $obj,
                $comp_code,
                $reason);
// $obj now holds the reference to the object (TESTQ)

// setup empty message descriptor.
    $mdg = array();
// setup get message options    
    $gmo = array('Options' => MQSERIES_MQGMO_FAIL_IF_QUIESCING | MQSERIES_MQGMO_WAIT, 'WaitInterval' => 3000);

// get the message from the queue    
    mqseries_get($conn, $obj, $mdg, $gmo, 255, $msg, $data_length, $comp_code, $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("GET CompCode:%d Reason:%d Text:%s<br>", $comp_code, $reason, mqseries_strerror($reason));
    }
    
// close the object reference $obj    
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);

// disconnect from the queue manager.    
    mqseries_disc($conn, $comp_code, $reason);
    
?>
```

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>
-   <span class="function">mqseries\_open</span>
-   <span class="function">mqseries\_put</span>

mqseries\_inq
=============

MQSeries MQINQ

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_inq</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$hobj`</span> , <span class="methodparam"><span class="type">int</span>
`$selectorCount`</span> , <span class="methodparam"><span
class="type">array</span> `$selectors`</span> , <span
class="methodparam"><span class="type">int</span> `$intAttrCount`</span>
, <span class="methodparam"><span class="type">resource</span>
`&$intAttr`</span> , <span class="methodparam"><span
class="type">int</span> `$charAttrLength`</span> , <span
class="methodparam"><span class="type">resource</span>
`&$charAttr`</span> , <span class="methodparam"><span
class="type">resource</span> `&$compCode`</span> , <span
class="methodparam"><span class="type">resource</span> `&$reason`</span>
)

The <span class="function">mqseries\_inq</span> (MQINQ) call returns an
array of integers and a set of character strings containing the
attributes of an object.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`hObj`  
Object handle.

This handle represents the object to be used.

`selectorCount`  
Count of selectors.

`selectors`  
Array of attribute selectors.

`intAttrLength`  
Count of integer attributes.

`intAttr`  
Array of integer attributes.

`charAttrLength`  
Length of character attributes buffer.

`charAttr`  
Character attributes.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_inq</span> example**

``` php
<?php
    $int_attr = array();
    $char_attr = "";
    
    mqseries_inq($conn, $obj, 1, array(MQSERIES_MQCA_Q_MGR_NAME), 0, $int_attr, 48, $char_attr, $comp_code, $reason);
    
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("INQ CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    } else {
        echo "INQ QManager name result ".$char_attr."<br>\n";
    }
?>
```

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>
-   <span class="function">mqseries\_open</span>

mqseries\_open
==============

MQSeries MQOPEN

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_open</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">array</span>
`&$objDesc`</span> , <span class="methodparam"><span
class="type">int</span> `$option`</span> , <span
class="methodparam"><span class="type">resource</span> `&$hobj`</span> ,
<span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_open</span> (MQOPEN) call
establishes access to an object.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`objDesc`  
Object descriptor. (MQOD)

`options`  
Options that control the action of the function.

`hObj`  
Object handle.

This handle represents the object to be used.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_open</span> example**

``` php
<?php
    $mqods = array('ObjectName' => 'TESTQ');
    mqseries_open(
                $conn,
                $mqods,
                MQSERIES_MQOO_INPUT_AS_Q_DEF | MQSERIES_MQOO_FAIL_IF_QUIESCING | MQSERIES_MQOO_OUTPUT,
                $obj,
                $comp_code,
                $reason);
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("open CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

### 参见

-   <span class="function">mqseries\_close</span>

mqseries\_put1
==============

MQSeries MQPUT1

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_put1</span> ( <span
class="methodparam"><span class="type">resource</span> `$hconn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`&$objDesc`</span> , <span class="methodparam"><span
class="type">resource</span> `&$msgDesc`</span> , <span
class="methodparam"><span class="type">resource</span> `&$pmo`</span> ,
<span class="methodparam"><span class="type">string</span>
`$buffer`</span> , <span class="methodparam"><span
class="type">resource</span> `&$compCode`</span> , <span
class="methodparam"><span class="type">resource</span> `&$reason`</span>
)

The <span class="function">mqseries\_put1</span> (MQPUT1) call puts one
message on a queue. The queue need not be open.

You can use both the <span class="function">mqseries\_put</span> and
<span class="function">mqseries\_put1</span> calls to put messages on a
queue; which call to use depends on the circumstances. Use the <span
class="function">mqseries\_put</span> (MQPUT) call to place multiple
messages on the same queue. Use the <span
class="function">mqseries\_put1</span> (MQPUT1) call to put only one
message on a queue. This call encapsulates the MQOPEN, MQPUT, and
MQCLOSE calls into a single call, minimizing the number of calls that
must be issued.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`objDesc`  
Object descriptor. (MQOD)

This is a structure which identifies the queue to which the message is
added.

`msgDesc`  
Message descriptor (MQMD).

`pmo`  
Put message options (MQPMO).

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>
-   <span class="function">mqseries\_open</span>
-   <span class="function">mqseries\_get</span>

mqseries\_put
=============

MQSeries MQPUT

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_put</span> ( <span
class="methodparam"><span class="type">resource</span> `$hConn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$hObj`</span> , <span class="methodparam"><span
class="type">array</span> `&$md`</span> , <span
class="methodparam"><span class="type">array</span> `&$pmo`</span> ,
<span class="methodparam"><span class="type">string</span>
`$message`</span> , <span class="methodparam"><span
class="type">resource</span> `&$compCode`</span> , <span
class="methodparam"><span class="type">resource</span> `&$reason`</span>
)

The <span class="function">mqseries\_put</span> (MQPUT) call puts a
message on a queue or distribution list. The queue or distribution list
must already be open.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`hObj`  
Object handle.

This handle represents the object to be used.

`md`  
Message descriptor (MQMD).

`pmo`  
Put message options (MQPMO).

`message`  
The actual message to put onto the queue.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">mqseries\_put</span> example**

``` php
<?php
// open connection to the queue manager
    mqseries_conn('WMQ1', $conn, $comp_code, $reason);
// $conn now hold the reference to the connection to the queue manager.

// open the connectio to the testq queueu
    mqseries_open(
                $conn,
                array('ObjectName' => 'TESTQ'),
                MQSERIES_MQOO_INPUT_AS_Q_DEF | MQSERIES_MQOO_FAIL_IF_QUIESCING | MQSERIES_MQOO_OUTPUT,
                $obj,
                $comp_code,
                $reason);
// $obj now holds the reference to the object (TESTQ)

// setup the message descriptor array. Check MQSeries reference manuals.
    $md = array(
                'Version' => MQSERIES_MQMD_VERSION_1,
                'Expiry' => MQSERIES_MQEI_UNLIMITED,
                'Report' => MQSERIES_MQRO_NONE,
                'MsgType' => MQSERIES_MQMT_DATAGRAM,
                'Format' => MQSERIES_MQFMT_STRING,
                'Priority' => 1,
                'Persistence' => MQSERIES_MQPER_PERSISTENT);

// setup the put message options.
    $pmo = array('Options' => MQSERIES_MQPMO_NEW_MSG_ID|MQSERIES_MQPMO_SYNCPOINT);
    
// put the message 'Ping' on the queueu.
    mqseries_put($conn, $obj, $md, $pmo, 'Ping', $comp_code, $reason);

    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("put CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
    }

// close the object reference $obj    
    mqseries_close($conn, $obj, MQSERIES_MQCO_NONE, $comp_code, $reason);

// disconnect from the queue manager.    
    mqseries_disc($conn, $comp_code, $reason);
    
?>
```

### 参见

-   <span class="function">mqseries\_conn</span>
-   <span class="function">mqseries\_connx</span>
-   <span class="function">mqseries\_open</span>
-   <span class="function">mqseries\_get</span>

mqseries\_set
=============

MQSeries MQSET

### 说明

<span class="type">void</span> <span
class="methodname">mqseries\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$hConn`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$hObj`</span> , <span class="methodparam"><span class="type">int</span>
`$selectorCount`</span> , <span class="methodparam"><span
class="type">array</span> `$selectors`</span> , <span
class="methodparam"><span class="type">int</span> `$intAttrCount`</span>
, <span class="methodparam"><span class="type">array</span>
`$intAttrs`</span> , <span class="methodparam"><span
class="type">int</span> `$charAttrLength`</span> , <span
class="methodparam"><span class="type">array</span> `$charAttrs`</span>
, <span class="methodparam"><span class="type">resource</span>
`&$compCode`</span> , <span class="methodparam"><span
class="type">resource</span> `&$reason`</span> )

The <span class="function">mqseries\_set</span> (MQSET) call is used to
change the attributes of an object represented by a handle. The object
must be a queue.

### 参数

`hConn`  
Connection handle.

This handle represents the connection to the queue manager.

`hObj`  
Object handle.

This handle represents the object to be used.

`selectorCount`  
Count of selectors.

`selectors`  
Array of attribute selectors.

`intAttrCount`  
Count of integer attributes.

`intAttrs`  
Array of integer attributes.

`charAttrLength`  
Length of character attributes buffer.

`charAttrs`  
Character attributes.

`compCode`  
Completion code.

`reason`  
Reason code qualifying the compCode.

### 返回值

没有返回值。

### 参见

-   <span class="function">mqseries\_inq</span>

mqseries\_strerror
==================

Returns the error message corresponding to a result code (MQRC)

### 说明

<span class="type">string</span> <span
class="methodname">mqseries\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$reason`</span> )

<span class="function">mqseries\_strerror</span> returns the message
that correspond to the reason result code.

### 参数

`reason`  
Reason code qualifying the compCode.

### 返回值

string representation of the reason code message.

### 范例

**示例 \#1 <span class="function">mqseries\_strerror</span> example**

``` php
<?php
    if ($comp_code !== MQSERIES_MQCC_OK) {
        printf("open CompCode:%d Reason:%d Text:%s<br>\n", $comp_code, $reason, mqseries_strerror($reason));
        exit;
    }
?>
```

以上例程会输出：

    Connx CompCode:2 Reason:2059 Text:Queue manager not available for connection.                    

**目录**

-   [mqseries\_back](/ref/mqseries.html#mqseries_back) — MQSeries MQBACK
-   [mqseries\_begin](/ref/mqseries.html#mqseries_begin) — MQseries
    MQBEGIN
-   [mqseries\_close](/ref/mqseries.html#mqseries_close) — MQSeries
    MQCLOSE
-   [mqseries\_cmit](/ref/mqseries.html#mqseries_cmit) — MQSeries MQCMIT
-   [mqseries\_conn](/ref/mqseries.html#mqseries_conn) — MQSeries MQCONN
-   [mqseries\_connx](/ref/mqseries.html#mqseries_connx) — MQSeries
    MQCONNX
-   [mqseries\_disc](/ref/mqseries.html#mqseries_disc) — MQSeries MQDISC
-   [mqseries\_get](/ref/mqseries.html#mqseries_get) — MQSeries MQGET
-   [mqseries\_inq](/ref/mqseries.html#mqseries_inq) — MQSeries MQINQ
-   [mqseries\_open](/ref/mqseries.html#mqseries_open) — MQSeries MQOPEN
-   [mqseries\_put1](/ref/mqseries.html#mqseries_put1) — MQSeries MQPUT1
-   [mqseries\_put](/ref/mqseries.html#mqseries_put) — MQSeries MQPUT
-   [mqseries\_set](/ref/mqseries.html#mqseries_set) — MQSeries MQSET
-   [mqseries\_strerror](/ref/mqseries.html#mqseries_strerror) — Returns
    the error message corresponding to a result code (MQRC)
