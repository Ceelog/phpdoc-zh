预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SAM_AUTO`** (<span class="type">string</span>)  
<span class="simpara"> Automatic behaviour </span>

**`SAM_BOOLEAN`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_BUS`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute used to set the name of the
enterprise service bus to connect to. </span>

**`SAM_BYTE`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_BYTES`** (<span class="type">string</span>)  
<span class="simpara"> Message body type descriptor. </span>

**`SAM_CORRELID`** (<span class="type">string</span>)  
<span class="simpara"> Attribute used on receive, send and remove
requests to identify specific messages. </span>

**`SAM_DELIVERYMODE`** (<span class="type">string</span>)  
<span class="simpara"> Message header property. </span>

**`SAM_DOUBLE`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_ENDPOINTS`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute used to define the possible
endpoints to connect to. </span>

**`SAM_FLOAT`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_HOST`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute used to set the hostname of the
required messaging server. </span>

**`SAM_INT`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_LONG`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_MANUAL`** (<span class="type">string</span>)  
<span class="simpara"> Manual (script controlled) behaviour </span>

**`SAM_MESSAGEID`** (<span class="type">string</span>)  
<span class="simpara"> Attribute used on receive and remove requests to
identify specific messages. </span>

**`SAM_MQTT`** (<span class="type">string</span>)  
<span class="simpara"> Connect protocol definition for selecting the
MQTT (MQ Telemetry Transport) protocol. </span>

**`SAM_MQTT_CLEANSTART`** (<span class="type">bool</span>)  
<span class="simpara"> Optional connect option to indicate to an MQTT
server that all previous connection data for this client should be
removed and that subscriptions should be deleted when the client
disconnects explicitly or unexpectedly. </span>

**`SAM_NON_PERSISTENT`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute value used to request messages
are not made persistent on the messaging server. </span>

**`SAM_PASSWORD`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute used to define the password to
be used for the user account being used to connect to a messaging server
that requires authorisation for connections. </span>

**`SAM_PERSISTENT`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute value used to request messages
are made persistent on the messaging server to protect against loss of
messages in the event of failure. </span>

**`SAM_PORT`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute used to set the port number on
which to communicate with the messaging server. </span>

**`SAM_PRIORITY`** (<span class="type">string</span>)  
<span class="simpara"> Option name used on send requests to specify a
delivery priority value. </span>

**`SAM_REPLY_TO`** (<span class="type">string</span>)  
<span class="simpara"> Message property used to specify the queue
identity on to which the script expects response or reply messages to be
posted. </span>

**`SAM_RTT`** (<span class="type">string</span>)  
<span class="simpara"> Connect protocol definition for selecting the IBM
Realtime Transport protocol for communication with a business
integration messaging server. </span>

**`SAM_STRING`** (<span class="type">string</span>)  
<span class="simpara"> Type specifier used when setting properties on
SAM\_Message objects. </span>

**`SAM_TARGETCHAIN`** (<span class="type">string</span>)  
<span class="simpara"> Connection attribute used to set the required
target chain identifier. </span>

**`SAM_TEXT`** (<span class="type">string</span>)  
<span class="simpara"> Message body type descriptor. </span>

**`SAM_TIMETOLIVE`** (<span class="type">string</span>)  
<span class="simpara"> Message send option name used to specify the
length of time a message should be retained in milliseconds. </span>

**`SAM_TRANSACTIONS`** (<span class="type">string</span>)  
<span class="simpara"> Connection attribute used to set required
transactional behaviour. May be set to SAM\_AUTO (default) or
SAM\_MANUAL. </span>

**`SAM_USERID`** (<span class="type">string</span>)  
<span class="simpara"> Connect attribute used to define the account to
being used to connect to a messaging server that requires authorisation
for connections. </span>

**`SAM_WAIT`** (<span class="type">string</span>)  
<span class="simpara"> Receive property used to specify the wait timeout
to be used when receiving a message from a queue or subscription.
</span>

**`SAM_WMQ`** (<span class="type">string</span>)  
<span class="simpara"> Connect protocol definition for selecting the IBM
WebSphere MQSeries protocol for communication with the desired messaging
server. </span>

**`SAM_WMQ_BINDINGS`** (<span class="type">string</span>)  
<span class="simpara"> Connect protocol definition for selecting the IBM
WebSphere MQSeries protocol for communication with a local messaging
server. </span>

**`SAM_WMQ_CLIENT`** (<span class="type">string</span>)  
<span class="simpara"> Connect protocol definition for selecting the IBM
WebSphere MQSeries protocol for communication with a remote messaging
server. </span>

**`SAM_WMQ_TARGET_CLIENT`** (<span class="type">string</span>)  
<span class="simpara"> Option name used on send requests to specify the
target client mode. This can either be default to 'jms' or 'mq'. The
default is 'jms' which means an RFH2 header is sent with the message
whereas the 'mq' setting means no RFH2 is included. </span>

**`SAM_WPM`** (<span class="type">string</span>)  
<span class="simpara"> Connect protocol definition for selecting the IBM
WebSphere Platform Messaging protocol for communication with a WebSphere
Application Server messaging server. </span>
