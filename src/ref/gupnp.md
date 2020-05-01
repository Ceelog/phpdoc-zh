gupnp\_context\_get\_host\_ip
=============================

Get the IP address

### 说明

<span class="type">string</span> <span
class="methodname">gupnp\_context\_get\_host\_ip</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
)

Get the IP address we advertise ourselves as using.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

### 返回值

Returns the IP address for the current context and **`FALSE`** on error.

### 范例

**示例 \#1 Create new UPnP context and get IP address of the host**

``` php
<?php

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* Get IP address for the UPnP context */
$ip = gupnp_context_get_host_ip($context);
echo $ip;

?>
```

### 参见

-   <span class="function">gupnp\_context\_new</span>
-   <span class="function">gupnp\_context\_get\_port</span>

gupnp\_context\_get\_port
=========================

Get the port

### 说明

<span class="type">int</span> <span
class="methodname">gupnp\_context\_get\_port</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
)

Get the port that the SOAP server is running on.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

### 返回值

Returns the port number for the current context and **`FALSE`** on
error.

### 范例

**示例 \#1 Create new UPnP context and get port number**

``` php
<?php

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* Get the port number for the UPnP context */
$port = gupnp_context_get_port($context);
echo $port;

?>
```

### 参见

-   <span class="function">gupnp\_context\_new</span>
-   <span class="function">gupnp\_context\_get\_host\_ip</span>

gupnp\_context\_get\_subscription\_timeout
==========================================

Get the event subscription timeout

### 说明

<span class="type">int</span> <span
class="methodname">gupnp\_context\_get\_subscription\_timeout</span> (
<span class="methodparam"><span class="type">resource</span>
`$context`</span> )

Get the event subscription timeout (in seconds), or 0 meaning there is
no timeout.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

### 返回值

The event subscription timeout in seconds.

### 参见

-   <span class="function">gupnp\_context\_new</span>
-   <span
    class="function">gupnp\_context\_set\_subscription\_timeout</span>

gupnp\_context\_host\_path
==========================

Start hosting

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_context\_host\_path</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
, <span class="methodparam"><span class="type">string</span>
`$local_path`</span> , <span class="methodparam"><span
class="type">string</span> `$server_path`</span> )

Start hosting `local_path` at `server_path`. Files with the path
`local_path`.LOCALE (if they exist) will be served up when LOCALE is
specified in the request's Accept-Language header.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

`local_path`  
Path to the local file or folder to be hosted.

`server_path`  
Web server path where `local_path` should be hosted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Create new UPnP context and set host path**

``` php
<?php

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* Host current directory */
gupnp_context_host_path($context, "./web", "");

?>
```

### 参见

-   <span class="function">gupnp\_context\_new</span>
-   <span class="function">gupnp\_context\_unhost\_path</span>

gupnp\_context\_new
===================

Create a new context

### 说明

<span class="type">resource</span> <span
class="methodname">gupnp\_context\_new</span> (\[ <span
class="methodparam"><span class="type">string</span> `$host_ip`</span>
\[, <span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 0</span></span> \]\] )

Create a new context with the specified host\_ip and port.

### 参数

`host_ip`  
The local host's IP address, or NULL to use the IP address of the first
non-loopback network interface.

`port`  
Port to run on, or 0 if you don't care what port is used.

### 返回值

A context identifier.

### 范例

**示例 \#1 Create new UPnP context**

``` php
<?php

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

?>
```

### 错误／异常

Issues **`E_WARNING`** with unable to create context.

gupnp\_context\_set\_subscription\_timeout
==========================================

Sets the event subscription timeout

### 说明

<span class="type">void</span> <span
class="methodname">gupnp\_context\_set\_subscription\_timeout</span> (
<span class="methodparam"><span class="type">resource</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$timeout`</span> )

Sets the event subscription timeout (in seconds) to time out. Note that
any client side subscriptions will automatically be renewed.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

`timeout`  
The event subscription timeout in seconds. Use 0 if you don't want
subscriptions to time out.

### 返回值

没有返回值。

### 参见

-   <span class="function">gupnp\_context\_new</span>
-   <span
    class="function">gupnp\_context\_get\_subscription\_timeout</span>

gupnp\_context\_timeout\_add
============================

Sets a function to be called at regular intervals

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_context\_timeout\_add</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> , <span class="methodparam"><span
class="type">mixed</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \] )

Sets a function to be called at regular intervals.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

`timeout`  
A timeout in miliseconds.

`callback`  
The callback function calling every `timeout` period of time. Typically,
callback function takes on `arg` parameter.

`arg`  
User data for `callback`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Create new UPnP context and set callback**

``` php
<?php

$user_data = "user data";

function timeout_cb($arg)
{
    printf("Call timeout_cb, user data: '%s'", $arg);
    return true;
}

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* Create root device */
$dev = gupnp_root_device_new($context, "/devicedesc.xml");

/* Set callback for timeout */
gupnp_context_timeout_add($context, 5000, "timeout_cb", $user_data);

/* Run the main loop */
gupnp_root_device_start($dev);

?>
```

### 错误／异常

Issues E\_WARNING with not valid callback function.

### 参见

-   <span class="function">gupnp\_context\_new</span>

gupnp\_context\_unhost\_path
============================

Stop hosting

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_context\_unhost\_path</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
, <span class="methodparam"><span class="type">string</span>
`$server_path`</span> )

Stop hosting the file or folder at `server_path`.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

`server_path`  
Web server path where the file or folder is hosted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_context\_new</span>
-   <span class="function">gupnp\_context\_host\_path</span>

gupnp\_control\_point\_browse\_start
====================================

Start browsing

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_control\_point\_browse\_start</span> ( <span
class="methodparam"><span class="type">resource</span> `$cpoint`</span>
)

Start the search and calls user-defined callback.

### 参数

`cpoint`  
A control point identifier, returned by <span
class="function">gupnp\_control\_point\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Create new UPnP context and start browsing**

``` php
<?php

function device_proxy_available_cb($proxy, $arg)
{
    $info = gupnp_device_info_get($proxy);

    $type = $info['device_type'];
    $location = $info['location'];

    printf("Device available:\n");
    printf("type:     %s\n", $type);
    printf("location: %s\n", $location);
}

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* We're interested in everything */
$cp = gupnp_control_point_new($context, "ssdp:all");

gupnp_control_point_callback_set($cp, 
    GUPNP_SIGNAL_DEVICE_PROXY_AVAILABLE, 'device_proxy_available_cb');

/* Start for browsing */
gupnp_control_point_browse_start($cp);

?>
```

### 参见

-   <span class="function">gupnp\_control\_point\_new</span>
-   <span class="function">gupnp\_control\_point\_browse\_stop</span>

gupnp\_control\_point\_browse\_stop
===================================

Stop browsing

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_control\_point\_browse\_stop</span> ( <span
class="methodparam"><span class="type">resource</span> `$cpoint`</span>
)

Stop the search and calls user-defined callback.

### 参数

`cpoint`  
A control point identifier, returned by <span
class="function">gupnp\_control\_point\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_control\_point\_new</span>
-   <span class="function">gupnp\_control\_point\_browse\_start</span>

gupnp\_control\_point\_callback\_set
====================================

Set control point callback

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_control\_point\_callback\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$cpoint`</span>
, <span class="methodparam"><span class="type">int</span>
`$signal`</span> , <span class="methodparam"><span
class="type">mixed</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \] )

Set control point callback function for signal.

### 参数

`cpoint`  
A control point identifier, returned by <span
class="function">gupnp\_control\_point\_new</span>.

`signal`  
The value of signal. Signal can be one of the following values:

**`GUPNP_SIGNAL_DEVICE_PROXY_AVAILABLE`**  
<span class="simpara"> Emitted whenever a new device has become
available. </span>

**`GUPNP_SIGNAL_DEVICE_PROXY_UNAVAILABLE`**  
<span class="simpara"> Emitted whenever a device is not available any
more. </span>

**`GUPNP_SIGNAL_SERVICE_PROXY_AVAILABLE`**  
<span class="simpara"> Emitted whenever a new service has become
available. </span>

**`GUPNP_SIGNAL_SERVICE_PROXY_UNAVAILABLE`**  
<span class="simpara"> Emitted whenever a service is not available any
more. </span>

`callback`  
The callback function for the certain signal. Typically, callback
function takes on two parameters. The `proxy` parameter's identifier
being the first, and the `arg` second.

`arg`  
User data for `callback`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Create new UPnP context and start browsing**

``` php
<?php

function device_proxy_available_cb($proxy, $arg)
{
    $info = gupnp_device_info_get($proxy);

    $type = $info['device_type'];
    $location = $info['location'];

    printf("Device available:\n");
    printf("type:     %s\n", $type);
    printf("location: %s\n", $location);
}

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* We're interested in everything */
$cp = gupnp_control_point_new($context, "ssdp:all");

gupnp_control_point_callback_set($cp, 
    GUPNP_SIGNAL_DEVICE_PROXY_AVAILABLE, 'device_proxy_available_cb');

/* Start for browsing */
gupnp_control_point_browse_start($cp);

?>
```

### 错误／异常

Issues E\_WARNING with not valid callback function.

### 参见

-   <span class="function">gupnp\_control\_point\_new</span>
-   <span class="function">gupnp\_control\_point\_browse\_start</span>

gupnp\_control\_point\_new
==========================

Create a new control point

### 说明

<span class="type">resource</span> <span
class="methodname">gupnp\_control\_point\_new</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
, <span class="methodparam"><span class="type">string</span>
`$target`</span> )

Create a new control point with the specified target.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

`target`  
The search target. `target` should be a service or device name, such as
urn:schemas-upnp-org:service:WANIPConnection:1 or
urn:schemas-upnp-org:device:MediaRenderer:1.

### 返回值

A control point identifier.

gupnp\_device\_action\_callback\_set
====================================

Set device callback function

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_device\_action\_callback\_set</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> , <span class="methodparam"><span
class="type">int</span> `$signal`</span> , <span
class="methodparam"><span class="type">string</span>
`$action_name`</span> , <span class="methodparam"><span
class="type">mixed</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \] )

Set device callback function for signal and action.

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

`signal`  
The value of signal. Signal can be one of the following values:

**`GUPNP_SIGNAL_ACTION_INVOKED`**  
<span class="simpara"> Emitted whenever an action is invoked. Handler
should process action and must call either <span
class="function">gupnp\_service\_action\_return</span> or <span
class="function">gupnp\_service\_action\_return\_error</span>. </span>

**`GUPNP_SIGNAL_NOTIFY_FAILED`**  
<span class="simpara"> Emitted whenever notification of a client fails.
</span>

`action_name`  
The name of action.

`callback`  
The callback function for the certain signal. Typically, callback
function takes on three parameters. The `service` parameter's identifier
being the first, `action` parameter's identifier (in case
GUPNP\_SIGNAL\_ACTION\_INVOKED signal) or `error` parameter's message
(in case GUPNP\_SIGNAL\_NOTIFY\_FAILED signal) being the second, and the
`arg` is third.

`arg`  
User data for `callback`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues E\_WARNING either with not valid callback function or with not
valid signal.

### 参见

-   <span class="function">gupnp\_root\_device\_new</span>

gupnp\_device\_info\_get\_service
=================================

Get the service with type

### 说明

<span class="type">resource</span> <span
class="methodname">gupnp\_device\_info\_get\_service</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> , <span class="methodparam"><span
class="type">string</span> `$type`</span> )

Get the service with type or false if no such device was found.

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

`type`  
The type of the service to be retrieved.

### 返回值

A service identifier.

### 范例

**示例 \#1 Create new UPnP context and get device info service**

``` php
<?php

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* Create root device */
$location = "/BinaryLight1.xml";
$dev = gupnp_root_device_new($context, $location);

/* Set root device is available */
gupnp_root_device_set_available($dev, true);

/* Get the switch service from the root device */
$service_type = "urn:schemas-upnp-org:service:SwitchPower:1";
$service = gupnp_device_info_get_service($dev, $service_type);
if (!$service) {
    die("Cannot get SwitchPower1 service\n");
}

?>
```

gupnp\_device\_info\_get
========================

Get info of root device

### 说明

<span class="type">array</span> <span
class="methodname">gupnp\_device\_info\_get</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> )

Get info of root device.

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

### 返回值

Return array wich contains the information of the root device (like
location, url, udn and etc).

gupnp\_root\_device\_get\_available
===================================

Check whether root device is available

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_root\_device\_get\_available</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> )

Get whether or not `root_device` is available (announcing its presence).

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_root\_device\_set\_available</span>

gupnp\_root\_device\_get\_relative\_location
============================================

Get the relative location of root device

### 说明

<span class="type">string</span> <span
class="methodname">gupnp\_root\_device\_get\_relative\_location</span> (
<span class="methodparam"><span class="type">resource</span>
`$root_device`</span> )

Get the relative location of root device.

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

### 返回值

The relative location of root device

gupnp\_root\_device\_new
========================

Create a new root device

### 说明

<span class="type">resource</span> <span
class="methodname">gupnp\_root\_device\_new</span> ( <span
class="methodparam"><span class="type">resource</span> `$context`</span>
, <span class="methodparam"><span class="type">string</span>
`$location`</span> , <span class="methodparam"><span
class="type">string</span> `$description_dir`</span> )

Create a new root device, automatically downloading and parsing
location.

### 参数

`context`  
A context identifier, returned by <span
class="function">gupnp\_context\_new</span>.

`location`  
Location of the description file for this device, relative to the HTTP
root

### 返回值

A root device identifier.

### 范例

**示例 \#1 Create new UPnP context and get device info service**

``` php
<?php

/* Create the UPnP context */
$context = gupnp_context_new();

if (!$context) {
 die("Error creating the GUPnP context\n");
}

/* Create root device */
$location = "/BinaryLight1.xml";
$dev = gupnp_root_device_new($context, $location);

?>
```

### 参见

-   <span class="function">gupnp\_root\_device\_set\_available</span>
-   <span class="function">gupnp\_root\_device\_start</span>
-   <span class="function">gupnp\_root\_device\_stop</span>

gupnp\_root\_device\_set\_available
===================================

Set whether or not root\_device is available

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_root\_device\_set\_available</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> , <span class="methodparam"><span
class="type">bool</span> `$available`</span> )

Controls whether or not root\_device is available (announcing its
presence).

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

`available`  
Set **`TRUE`** if `root_device` should be available.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_root\_device\_get\_available</span>

gupnp\_root\_device\_start
==========================

Start main loop

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_root\_device\_start</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> )

Start root server's main loop.

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_root\_device\_stop</span>

gupnp\_root\_device\_stop
=========================

Stop main loop

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_root\_device\_stop</span> ( <span
class="methodparam"><span class="type">resource</span>
`$root_device`</span> )

Stop root server's main loop.

### 参数

`root_device`  
A root device identifier, returned by <span
class="function">gupnp\_root\_device\_new</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_root\_device\_start</span>

gupnp\_service\_action\_get
===========================

Retrieves the specified action arguments

### 说明

<span class="type">mixed</span> <span
class="methodname">gupnp\_service\_action\_get</span> ( <span
class="methodparam"><span class="type">resource</span> `$action`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span class="type">int</span>
`$type`</span> )

Retrieves the specified action arguments.

### 参数

`action`  
A service action identifier.

`name`  
The name of the variable to retrieve.

`type`  
The type of the variable to retrieve. Type can be one of the following
values:

**`GUPNP_TYPE_BOOLEAN`**  
<span class="simpara"> Type of the variable is boolean. </span>

**`GUPNP_TYPE_INT`**  
<span class="simpara"> Type of the variable is integer. </span>

**`GUPNP_TYPE_LONG`**  
<span class="simpara"> Type of the variable is long. </span>

**`GUPNP_TYPE_DOUBLE`**  
<span class="simpara"> Type of the variable is double. </span>

**`GUPNP_TYPE_FLOAT`**  
<span class="simpara"> Type of the variable is float. </span>

**`GUPNP_TYPE_STRING`**  
<span class="simpara"> Type of the variable is string. </span>

### 返回值

The value of the variable.

### 错误／异常

Issues E\_WARNING with not correctly defined type of the variable.

### 参见

-   <span class="function">gupnp\_service\_action\_set</span>

gupnp\_service\_action\_return\_error
=====================================

Return error code

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_action\_return\_error</span> ( <span
class="methodparam"><span class="type">resource</span> `$action`</span>
, <span class="methodparam"><span class="type">int</span>
`$error_code`</span> \[, <span class="methodparam"><span
class="type">string</span> `$error_description`</span> \] )

Return error code.

### 参数

`action`  
A service action identifier.

`error_code`  
The error code. Signal can be one of the following values or user
defined:

**`GUPNP_CONTROL_ERROR_INVALID_ACTION`**  
<span class="simpara"> The action name was invalid. </span>

**`GUPNP_CONTROL_ERROR_INVALID_ARGS`**  
<span class="simpara"> The action arguments were invalid. </span>

**`GUPNP_CONTROL_ERROR_OUT_OF_SYNC`**  
<span class="simpara"> Out of sync (deprecated). </span>

**`GUPNP_CONTROL_ERROR_ACTION_FAILED`**  
<span class="simpara"> The action failed. </span>

`error_description`  
The error description.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_action\_return</span>

gupnp\_service\_action\_return
==============================

Return successfully

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_action\_return</span> ( <span
class="methodparam"><span class="type">resource</span> `$action`</span>
)

Return successfully.

### 参数

`action`  
A service action identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_action\_return\_error</span>

gupnp\_service\_action\_set
===========================

Sets the specified action return values

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_action\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$action`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span class="type">int</span>
`$type`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

Sets the specified action return values.

### 参数

`action`  
A service action identifier.

`name`  
The name of the variable to retrieve.

`type`  
The type of the variable to retrieve. Type can be one of the following
values:

**`GUPNP_TYPE_BOOLEAN`**  
<span class="simpara"> Type of the variable is boolean. </span>

**`GUPNP_TYPE_INT`**  
<span class="simpara"> Type of the variable is integer. </span>

**`GUPNP_TYPE_LONG`**  
<span class="simpara"> Type of the variable is long. </span>

**`GUPNP_TYPE_DOUBLE`**  
<span class="simpara"> Type of the variable is double. </span>

**`GUPNP_TYPE_FLOAT`**  
<span class="simpara"> Type of the variable is float. </span>

**`GUPNP_TYPE_STRING`**  
<span class="simpara"> Type of the variable is string. </span>

`value`  
The value of the variable to retrieve.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues E\_WARNING with neither not correctly defined type of the
variable or the value is not corresponding to the defined type.

### 参见

-   <span class="function">gupnp\_service\_action\_get</span>

gupnp\_service\_freeze\_notify
==============================

Freeze new notifications

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_freeze\_notify</span> ( <span
class="methodparam"><span class="type">resource</span> `$service`</span>
)

Causes new notifications to be queued up until <span
class="function">gupnp\_service\_thaw\_notify</span> is called.

### 参数

`service`  
A service identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_notify</span>
-   <span class="function">gupnp\_service\_thaw\_notify</span>

gupnp\_service\_info\_get\_introspection
========================================

Get resource introspection of service

### 说明

<span class="type">mixed</span> <span
class="methodname">gupnp\_service\_info\_get\_introspection</span> (
<span class="methodparam"><span class="type">resource</span>
`$proxy`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \]\] )

Get resource introspection of service or register callback if
corresponding parameter was passed.

### 参数

`proxy`  
A service proxy identifier.

`callback`  
The callback function to be called when introspection object is ready.
Typically, callback function takes on three parameters. The
`introspection` parameter's identifier being the first, `error`
parameter's message being the second, and the `arg` is third.

`arg`  
User data for `callback`.

### 返回值

Return true if callback function was defined. Return introspection
identifier if callback function was omited.

### 错误／异常

Issues E\_WARNING with not valid callback function.

gupnp\_service\_info\_get
=========================

Get full info of service

### 说明

<span class="type">array</span> <span
class="methodname">gupnp\_service\_info\_get</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> )

Get full info of service.

### 参数

`proxy`  
A service proxy identifier.

### 返回值

Return array wich contains the information of the service (like
location, url, udn and etc).

gupnp\_service\_introspection\_get\_state\_variable
===================================================

Returns the state variable data

### 说明

<span class="type">array</span> <span
class="methodname">gupnp\_service\_introspection\_get\_state\_variable</span>
( <span class="methodparam"><span class="type">resource</span>
`$introspection`</span> , <span class="methodparam"><span
class="type">string</span> `$variable_name`</span> )

Returns the state variable data by the name `variable_name` in this
service.

### 参数

`introspection`  
A introspection identifier.

`variable_name`  
The name of the variable to retreive.

### 返回值

Return the state variable data or **`FALSE`**.

gupnp\_service\_notify
======================

Notifies listening clients

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_notify</span> ( <span
class="methodparam"><span class="type">resource</span> `$service`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span class="type">int</span>
`$type`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

Notifies listening clients that the property have changed to the
specified values.

### 参数

`service`  
A service identifier.

`name`  
The name of the variable.

`type`  
The type of the variable. Type can be one of the following values:

**`GUPNP_TYPE_BOOLEAN`**  
<span class="simpara"> Type of the variable is boolean. </span>

**`GUPNP_TYPE_INT`**  
<span class="simpara"> Type of the variable is integer. </span>

**`GUPNP_TYPE_LONG`**  
<span class="simpara"> Type of the variable is long. </span>

**`GUPNP_TYPE_DOUBLE`**  
<span class="simpara"> Type of the variable is double. </span>

**`GUPNP_TYPE_FLOAT`**  
<span class="simpara"> Type of the variable is float. </span>

**`GUPNP_TYPE_STRING`**  
<span class="simpara"> Type of the variable is string. </span>

`value`  
The value of the variable.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues E\_WARNING with either not correctly defined type of the variable
or the value is not corresponding to the defined type.

### 参见

-   <span class="function">gupnp\_service\_freeze\_notify</span>
-   <span class="function">gupnp\_service\_thaw\_notify</span>

gupnp\_service\_proxy\_action\_get
==================================

Send action to the service and get value

### 说明

<span class="type">mixed</span> <span
class="methodname">gupnp\_service\_proxy\_action\_get</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">string</span>
`$action`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> )

Send action with parameters to the service exposed by proxy
synchronously and get value.

### 参数

`proxy`  
A service proxy identifier.

`action`  
An action.

`name`  
The action name.

`type`  
The type of the variable to retrieve. Type can be one of the following
values:

**`GUPNP_TYPE_BOOLEAN`**  
<span class="simpara"> Type of the variable is boolean. </span>

**`GUPNP_TYPE_INT`**  
<span class="simpara"> Type of the variable is integer. </span>

**`GUPNP_TYPE_LONG`**  
<span class="simpara"> Type of the variable is long. </span>

**`GUPNP_TYPE_DOUBLE`**  
<span class="simpara"> Type of the variable is double. </span>

**`GUPNP_TYPE_FLOAT`**  
<span class="simpara"> Type of the variable is float. </span>

**`GUPNP_TYPE_STRING`**  
<span class="simpara"> Type of the variable is string. </span>

### 返回值

Return value of the action.

### 错误／异常

Issues E\_WARNING with either not correctly defined type of the action
or unable to send action.

### 参见

-   <span class="function">gupnp\_service\_proxy\_action\_set</span>
-   <span class="function">gupnp\_service\_proxy\_send\_action</span>

gupnp\_service\_proxy\_action\_set
==================================

Send action to the service and set value

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_proxy\_action\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">string</span>
`$action`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> )

Send action with parameters to the service exposed by proxy
synchronously and set value.

### 参数

`proxy`  
A service proxy identifier.

`action`  
An action.

`name`  
The action name.

`value`  
The action value.

`type`  
The type of the action. Type can be one of the following values:

**`GUPNP_TYPE_BOOLEAN`**  
<span class="simpara"> Type of the variable is boolean. </span>

**`GUPNP_TYPE_INT`**  
<span class="simpara"> Type of the variable is integer. </span>

**`GUPNP_TYPE_LONG`**  
<span class="simpara"> Type of the variable is long. </span>

**`GUPNP_TYPE_DOUBLE`**  
<span class="simpara"> Type of the variable is double. </span>

**`GUPNP_TYPE_FLOAT`**  
<span class="simpara"> Type of the variable is float. </span>

**`GUPNP_TYPE_STRING`**  
<span class="simpara"> Type of the variable is string. </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues E\_WARNING with either not correctly defined type of the action
or unable to send action.

### 参见

-   <span class="function">gupnp\_service\_proxy\_action\_get</span>
-   <span class="function">gupnp\_service\_proxy\_send\_action</span>

gupnp\_service\_proxy\_add\_notify
==================================

Sets up callback for variable change notification

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_proxy\_add\_notify</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">mixed</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$arg`</span> \] )

Sets up callback to be called whenever a change notification for
variable is recieved.

### 参数

`proxy`  
A service proxy identifier.

`value`  
The variable to add notification for.

`type`  
The type of the variable. Type can be one of the following values:

**`GUPNP_TYPE_BOOLEAN`**  
<span class="simpara"> Type of the variable is boolean. </span>

**`GUPNP_TYPE_INT`**  
<span class="simpara"> Type of the variable is integer. </span>

**`GUPNP_TYPE_LONG`**  
<span class="simpara"> Type of the variable is long. </span>

**`GUPNP_TYPE_DOUBLE`**  
<span class="simpara"> Type of the variable is double. </span>

**`GUPNP_TYPE_FLOAT`**  
<span class="simpara"> Type of the variable is float. </span>

**`GUPNP_TYPE_STRING`**  
<span class="simpara"> Type of the variable is string. </span>

`callback`  
The callback to call when variable changes. Typically, callback function
takes on three parameters. The `variable` parameter being the first,
`value` parameter being the second, and the `arg` is third.

`arg`  
User data for `callback`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_proxy\_remove\_notify</span>

gupnp\_service\_proxy\_callback\_set
====================================

Set service proxy callback for signal

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_proxy\_callback\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">int</span> `$signal`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$arg`</span> \] )

Set service proxy callback for signal.

### 参数

`proxy`  
A service proxy identifier.

`signal`  
The value of signal.

**`GUPNP_SIGNAL_SUBSCRIPTION_LOST`**  
<span class="simpara"> Emitted whenever the subscription to this service
has been lost due to an error condition. </span>

`callback`  
The callback function for the certain signal. Typically, callback
function takes on two parameters. `error` parameter's message being the
first, and the `arg` is second.

`arg`  
User data for `callback`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues E\_WARNING either with not valid callback function or with not
valid signal.

gupnp\_service\_proxy\_get\_subscribed
======================================

Check whether subscription is valid to the service

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_proxy\_get\_subscribed</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> )

Check whether subscription is valid to the service.

### 参数

`proxy`  
A service proxy identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_proxy\_set\_subscribed</span>

gupnp\_service\_proxy\_remove\_notify
=====================================

Cancels the variable change notification

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_proxy\_remove\_notify</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

Cancels the variable change notification.

### 参数

`proxy`  
A service proxy identifier.

`value`  
The variable to add notification for.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_proxy\_add\_notify</span>

gupnp\_service\_proxy\_send\_action
===================================

Send action with multiple parameters synchronously

### 说明

<span class="type">array</span> <span
class="methodname">gupnp\_service\_proxy\_send\_action</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">string</span>
`$action`</span> , <span class="methodparam"><span
class="type">array</span> `$in_params`</span> , <span
class="methodparam"><span class="type">array</span> `$out_params`</span>
)

Send action with parameters `in_params` to the service exposed by proxy
synchronously and return `out_params` with values or **`FALSE`** on
error.

### 参数

`proxy`  
A service proxy identifier.

`action`  
An action.

`in_params`  
An array of in parameters. Each entry in `in_params` is supposed to an
array containing name, type and value of the parameters.

`out_params`  
An array of out parameters. Each entry in `out_params` is supposed to an
array containing name and type of the parameters.

### 返回值

Return `out_params` array with values or **`FALSE`** on error.

### 错误／异常

Issues E\_WARNING with either not correctly defined `in_params` and
`out_params` or unable to send action.

### 参见

-   <span class="function">gupnp\_service\_proxy\_action\_get</span>
-   <span class="function">gupnp\_service\_proxy\_action\_set</span>

gupnp\_service\_proxy\_set\_subscribed
======================================

(Un)subscribes to the service

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_proxy\_set\_subscribed</span> ( <span
class="methodparam"><span class="type">resource</span> `$proxy`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$subscribed`</span> )

(Un)subscribes to the service.

### 参数

`proxy`  
A service proxy identifier.

`subscribed`  
Set **`TRUE`** to subscribe to this service.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_proxy\_get\_subscribed</span>

gupnp\_service\_thaw\_notify
============================

Sends out any pending notifications and stops queuing of new ones

### 说明

<span class="type">bool</span> <span
class="methodname">gupnp\_service\_thaw\_notify</span> ( <span
class="methodparam"><span class="type">resource</span> `$service`</span>
)

Sends out any pending notifications and stops queuing of new ones.

### 参数

`service`  
A service identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">gupnp\_service\_notify</span>
-   <span class="function">gupnp\_service\_freeze\_notify</span>

**目录**

-   [gupnp\_context\_get\_host\_ip](/ref/gupnp.html#gupnp_context_get_host_ip)
    — Get the IP address
-   [gupnp\_context\_get\_port](/ref/gupnp.html#gupnp_context_get_port)
    — Get the port
-   [gupnp\_context\_get\_subscription\_timeout](/ref/gupnp.html#gupnp_context_get_subscription_timeout)
    — Get the event subscription timeout
-   [gupnp\_context\_host\_path](/ref/gupnp.html#gupnp_context_host_path)
    — Start hosting
-   [gupnp\_context\_new](/ref/gupnp.html#gupnp_context_new) — Create a
    new context
-   [gupnp\_context\_set\_subscription\_timeout](/ref/gupnp.html#gupnp_context_set_subscription_timeout)
    — Sets the event subscription timeout
-   [gupnp\_context\_timeout\_add](/ref/gupnp.html#gupnp_context_timeout_add)
    — Sets a function to be called at regular intervals
-   [gupnp\_context\_unhost\_path](/ref/gupnp.html#gupnp_context_unhost_path)
    — Stop hosting
-   [gupnp\_control\_point\_browse\_start](/ref/gupnp.html#gupnp_control_point_browse_start)
    — Start browsing
-   [gupnp\_control\_point\_browse\_stop](/ref/gupnp.html#gupnp_control_point_browse_stop)
    — Stop browsing
-   [gupnp\_control\_point\_callback\_set](/ref/gupnp.html#gupnp_control_point_callback_set)
    — Set control point callback
-   [gupnp\_control\_point\_new](/ref/gupnp.html#gupnp_control_point_new)
    — Create a new control point
-   [gupnp\_device\_action\_callback\_set](/ref/gupnp.html#gupnp_device_action_callback_set)
    — Set device callback function
-   [gupnp\_device\_info\_get\_service](/ref/gupnp.html#gupnp_device_info_get_service)
    — Get the service with type
-   [gupnp\_device\_info\_get](/ref/gupnp.html#gupnp_device_info_get) —
    Get info of root device
-   [gupnp\_root\_device\_get\_available](/ref/gupnp.html#gupnp_root_device_get_available)
    — Check whether root device is available
-   [gupnp\_root\_device\_get\_relative\_location](/ref/gupnp.html#gupnp_root_device_get_relative_location)
    — Get the relative location of root device
-   [gupnp\_root\_device\_new](/ref/gupnp.html#gupnp_root_device_new) —
    Create a new root device
-   [gupnp\_root\_device\_set\_available](/ref/gupnp.html#gupnp_root_device_set_available)
    — Set whether or not root\_device is available
-   [gupnp\_root\_device\_start](/ref/gupnp.html#gupnp_root_device_start)
    — Start main loop
-   [gupnp\_root\_device\_stop](/ref/gupnp.html#gupnp_root_device_stop)
    — Stop main loop
-   [gupnp\_service\_action\_get](/ref/gupnp.html#gupnp_service_action_get)
    — Retrieves the specified action arguments
-   [gupnp\_service\_action\_return\_error](/ref/gupnp.html#gupnp_service_action_return_error)
    — Return error code
-   [gupnp\_service\_action\_return](/ref/gupnp.html#gupnp_service_action_return)
    — Return successfully
-   [gupnp\_service\_action\_set](/ref/gupnp.html#gupnp_service_action_set)
    — Sets the specified action return values
-   [gupnp\_service\_freeze\_notify](/ref/gupnp.html#gupnp_service_freeze_notify)
    — Freeze new notifications
-   [gupnp\_service\_info\_get\_introspection](/ref/gupnp.html#gupnp_service_info_get_introspection)
    — Get resource introspection of service
-   [gupnp\_service\_info\_get](/ref/gupnp.html#gupnp_service_info_get)
    — Get full info of service
-   [gupnp\_service\_introspection\_get\_state\_variable](/ref/gupnp.html#gupnp_service_introspection_get_state_variable)
    — Returns the state variable data
-   [gupnp\_service\_notify](/ref/gupnp.html#gupnp_service_notify) —
    Notifies listening clients
-   [gupnp\_service\_proxy\_action\_get](/ref/gupnp.html#gupnp_service_proxy_action_get)
    — Send action to the service and get value
-   [gupnp\_service\_proxy\_action\_set](/ref/gupnp.html#gupnp_service_proxy_action_set)
    — Send action to the service and set value
-   [gupnp\_service\_proxy\_add\_notify](/ref/gupnp.html#gupnp_service_proxy_add_notify)
    — Sets up callback for variable change notification
-   [gupnp\_service\_proxy\_callback\_set](/ref/gupnp.html#gupnp_service_proxy_callback_set)
    — Set service proxy callback for signal
-   [gupnp\_service\_proxy\_get\_subscribed](/ref/gupnp.html#gupnp_service_proxy_get_subscribed)
    — Check whether subscription is valid to the service
-   [gupnp\_service\_proxy\_remove\_notify](/ref/gupnp.html#gupnp_service_proxy_remove_notify)
    — Cancels the variable change notification
-   [gupnp\_service\_proxy\_send\_action](/ref/gupnp.html#gupnp_service_proxy_send_action)
    — Send action with multiple parameters synchronously
-   [gupnp\_service\_proxy\_set\_subscribed](/ref/gupnp.html#gupnp_service_proxy_set_subscribed)
    — (Un)subscribes to the service
-   [gupnp\_service\_thaw\_notify](/ref/gupnp.html#gupnp_service_thaw_notify)
    — Sends out any pending notifications and stops queuing of new ones
