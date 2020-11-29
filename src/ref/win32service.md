win32\_continue\_service
========================

Resumes a paused service

### 说明

<span class="type">void</span> <span
class="methodname">win32\_continue\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$machine`</span> \] )

Resumes a paused, named service. Requires administrative privileges or
an account with appropriate rights set in the service's ACL.

### 参数

`servicename`  
The short name of the service.

`machine`  
Optional machine name. If omitted, the local machine is used.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |
| PECL win32service 0.3.0 | This function does not longer require an administrator account if ACL is set for another account.                                                                                                 |

### 参见

-   <span class="function">win32\_start\_service</span>
-   <span class="function">win32\_stop\_service</span>
-   <span class="function">win32\_pause\_service</span>
-   <span class="function">win32\_send\_custom\_control</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_create\_service
======================

Creates a new service entry in the SCM database

### 说明

<span class="type">void</span> <span
class="methodname">win32\_create\_service</span> ( <span
class="methodparam"><span class="type">array</span> `$details`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$machine`</span> \] )

Attempts to add a service into the SCM database. Administrative
privileges are required for this to succeed.

### 参数

`details`  
An array of service details:

`service`  
The short name of the service. This is the name that you will use to
control the service using the *net* command. The service must be unique
(no two services can share the same name), and, ideally, should avoid
having spaces in the name.

`display`  
The display name of the service. This is the name that you will see in
the Services Applet.

`description`  
The long description of the service. This is the description that you
will see in the Services Applet.

`user`  
The name of the user account under which you want the service to run. If
omitted, the service will run as the LocalSystem account. If the
username is specified, you must also provide a password.

`password`  
The password that corresponds to the `user`.

`path`  
The full path to the executable module that will be launched when the
service is started. If omitted, the path to the current PHP process will
be used.

`params`  
Command line parameters to pass to the service when it starts. If you
want to run a PHP script as the service, then the first parameter should
be the full path to the PHP script that you intend to run. If the script
name or path contains spaces, then wrap the full path to the PHP script
with *"*.

`load_order`  
Controls the load\_order. This is not yet fully supported.

`svc_type`  
Sets the service type. If omitted, the default value is
**`WIN32_SERVICE_WIN32_OWN_PROCESS`**. Don't change this unless you know
what you're doing.

`start_type`  
Specifies how the service should be started. The default is
**`WIN32_SERVICE_AUTO_START`** which means the service will be launched
when the machine starts up.

`error_control`  
Informs the SCM what it should do when it detects a problem with the
service. The default is **`WIN32_SERVER_ERROR_IGNORE`**. Changing this
value is not yet fully supported.

`delayed_start`  
If `delayed_start` is set to **`TRUE`**, then this will inform the SCM
that this service should be started after other auto-start services are
started plus a short delay.

Any service can be marked as a delayed auto-start service; however, this
setting has no effect unless the service's `start_type` is
**`WIN32_SERVICE_AUTO_START`**.

This setting is only applicable on Windows Vista and Windows Server 2008
or greater.

`base_priority`  
To reduce the impact on processor utilisation, it may be necessary to
set a base priority lower than normal.

The `base_priority` can be set to one of the constants define in
<a href="/win32service/constants.html#Win32%20Base%20Priority%20Classes" class="link">Win32 Base Priority Classes</a>.

`dependencies`  
To define the dependencies for your service, it may be necessary to set
this parameter to the list of the services names in an array.

`recovery_delay`  
This parameter defines the delay between the fail and the execution of
recovery action. The value is in milliseconds.

The default value is 60000.

`recovery_action_1`  
The action will be executed on first failure. The default value is
**`WIN32_SC_ACTION_NONE`**.

The `recovery_action_1` can be set to one of the constants defined in
<a href="/win32service/constants.html#Win32%20Recovery%20action" class="link">Win32 Recovery action</a>.

`recovery_action_2`  
The action will be executed on second failure. The default value is
**`WIN32_SC_ACTION_NONE`**.

The `recovery_action_2` can be set to one of the constants defined in
<a href="/win32service/constants.html#Win32%20Recovery%20action" class="link">Win32 Recovery action</a>.

`recovery_action_3`  
The action will be executed on next failures. The default value is
**`WIN32_SC_ACTION_NONE`**.

The `recovery_action_3` can be set to one of the constants defined in
<a href="/win32service/constants.html#Win32%20Recovery%20action" class="link">Win32 Recovery action</a>.

`recovery_reset_period`  
The failure count will be reset after the delay defined in the
parameter. The delay is expirement in seconds.

The default value is *86400*.

`recovery_enabled`  
Set this parameter at **`TRUE`** to enable the recovery settings,
**`FALSE`** to disable.

The default value is **`FALSE`**

`recovery_reboot_msg`  
Set this parameter to define the message saved into the Windows Event
Log before the reboot. Used only if one action is set to
**`WIN32_SC_ACTION_REBOOT`**.

`recovery_command`  
Set this parameter to define the command executed when one action is
defined on **`WIN32_SC_ACTION_RUN_COMMAND`**.

`machine`  
The optional machine name on which you want to create a service. If
omitted, it will use the local machine.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`service` parameter is empty.

A <span class="classname">ValueError</span> is thrown if the; value of
`path` parameter is missing or empty.

A <span class="classname">ValueError</span> is thrown if the; value of
`svc_type` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`start_type` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`error_control` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`base_priority` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`recovery_delay` parameter is not between 0 and PHP\_INT\_MAX.

A <span class="classname">ValueError</span> is thrown if the; value of
`recovery_action_1` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`recovery_action_2` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`recovery_action_3` parameter is wrong.

A <span class="classname">ValueError</span> is thrown if the; value of
`recovery_reset_period` parameter is not between 0 and PHP\_INT\_MAX.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 范例

**示例 \#1 A <span class="function">win32\_create\_service</span>
example**

Create a service with the short name 'dummyphp'.

``` php
<?php
$x = win32_create_service(array(
    'service'     => 'dummyphp',                                           // the name of your service
    'display'     => 'sample dummy PHP service',                           // short description
    'description' => 'This is a dummy Windows service created using PHP.', // long description
    'params'      => '"' . __FILE__ . '"  run',                            // path to the script and parameters
));
debug_zval_dump($x);
?>
```

**示例 \#2 A <span class="function">win32\_create\_service</span>
example with dependencies**

Create a service with the short name 'dummyphp' and dependencies.

``` php
<?php
$x = win32_create_service(array(
    'service'      => 'dummyphp',                                           // the name of your service
    'display'      => 'sample dummy PHP service',                           // short description
    'description'  => 'This is a dummy Windows service created using PHP.', // long description
    'params'       => '"' . __FILE__ . '"  run',                            // path to the script and parameters
    'dependencies' => array("Netman"),                                      // The list of the dependencies 
));
debug_zval_dump($x);
?>
```

**示例 \#3 A <span class="function">win32\_create\_service</span>
example with recovery**

Create a service with the short name 'dummyphp' and recovery settings.

``` php
<?php
$x = win32_create_service(array(
    'service'               => 'dummyphp',                                           // the name of your service
    'display'               => 'sample dummy PHP service',                           // short description
    'description'           => 'This is a dummy Windows service created using PHP.', // long description
    'params'                => '"' . __FILE__ . '"  run',                            // path to the script and parameters
    'recovery_delay'        => 120000,                                               // Recovery action is executed after 2 minutes
    'recovery_action_1'     => WIN32_SC_ACTION_RESTART,                              // On first failure, restart the service
    'recovery_action_2'     => WIN32_SC_ACTION_RUN_COMMAND,                          // On second failure, execute the commmand
    'recovery_action_3'     => WIN32_SC_ACTION_NONE,                                 // On other failure, do nothing
    'recovery_reset_period' => 86400,                                                // Reset the fail counter after 1 day
    'recovery_enabled'      => true,                                                 // Enable the recovery parameter
    'recovery_reboot_msg'   => null,                                                 // Do not define a reboot message, it's not needed here
    'recovery_command'      => "c:\clean-service.bat",                               // When the action is WIN32_SC_ACTION_RUN_COMMAND, execute this command
));
debug_zval_dump($x);
?>
```

### 更新日志

| 版本                    | 说明                                                                                                                                                                                                                       |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                                                     |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned.                          |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                                                  |
| PECL win32service 0.4.0 | The `dependencies`, `recovery_delay`, `recovery_action_1`, `recovery_action_2`, `recovery_action_3`, `recovery_reset_period`, `recovery_enabled`, `recovery_reboot_msg` and `recovery_command` parameters have been added. |

### 参见

-   <span class="function">win32\_delete\_service</span>
-   <a href="/win32service/constants.html#Win32%20Base%20Priority%20Classes" class="link">Win32 Base Priority Classes</a>
-   <a href="/win32service/constants.html#Win32%20Recovery%20action" class="link">Win32 Recovery action</a>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_delete\_service
======================

Deletes a service entry from the SCM database

### 说明

<span class="type">void</span> <span
class="methodname">win32\_delete\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$machine`</span> \] )

Attempts to delete a service from the SCM database. Administrative
privileges are required for this to succeed.

This function really just marks the service for deletion. If other
processes (such as the Services Applet) are open, then the deletion will
be deferred until those applications are closed. If a service is marked
for deletion, further attempts to delete it will fail, and attempts to
create a new service with that name will also fail.

### 参数

`servicename`  
The short name of the service.

`machine`  
The optional machine name. If omitted, the local machine will be used.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 范例

**示例 \#1 A <span class="function">win32\_delete\_service</span>
example**

Deletes the dummyphp service.

``` php
<?php
win32_delete_service('dummyphp');
?>
```

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |

### 参见

-   <span class="function">win32\_create\_service</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_get\_last\_control\_message
==================================

Returns the last control message that was sent to this service

### 说明

<span class="type">int</span> <span
class="methodname">win32\_get\_last\_control\_message</span> ( <span
class="methodparam">void</span> )

Returns the control code that was last sent to this service process.
When running as a service you should periodically check this to
determine if your service needs to stop running.

**Caution**

Since version 0.2.0, this function work only in "cli" SAPI. On other
SAPI this function is disabled.

### 返回值

Returns a control constant which will be one of the
<a href="/win32service/constants.html#Win32Service%20Service%20Control%20Message%20Constants" class="link">Win32Service Service Control Message Constants</a>:
**`WIN32_SERVICE_CONTROL_CONTINUE`**,
**`WIN32_SERVICE_CONTROL_DEVICEEVENT`**,
**`WIN32_SERVICE_CONTROL_HARDWAREPROFILECHANGE`**,
**`WIN32_SERVICE_CONTROL_INTERROGATE`**,
**`WIN32_SERVICE_CONTROL_NETBINDADD`**,
**`WIN32_SERVICE_CONTROL_NETBINDDISABLE`**,
**`WIN32_SERVICE_CONTROL_NETBINDENABLE`**,
**`WIN32_SERVICE_CONTROL_NETBINDREMOVE`**,
**`WIN32_SERVICE_CONTROL_PARAMCHANGE`**,
**`WIN32_SERVICE_CONTROL_PAUSE`**,
**`WIN32_SERVICE_CONTROL_POWEREVENT`**,
**`WIN32_SERVICE_CONTROL_PRESHUTDOWN`**,
**`WIN32_SERVICE_CONTROL_SESSIONCHANGE`**,
**`WIN32_SERVICE_CONTROL_SHUTDOWN`**, **`WIN32_SERVICE_CONTROL_STOP`**.

If the value is between 128 and 255, the control code is custom.

### 错误／异常

Prior to version 1.0.0, if the SAPI is not *"cli"*, this function emits
an **`E_ERROR`** level error.

As of version 1.0.0, will throw a <span
class="classname">Win32ServiceException</span> if SAPI is not *"cli"*

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 0.2.0 | This function works only in the *"cli"* SAPI.                                                                                                                                                     |

### 参见

-   <span
    class="function">win32\_start\_service\_ctrl\_dispatcher</span>
-   <span class="function">win32\_set\_service\_status</span>
-   <span class="function">win32\_set\_service\_exit\_mode</span>
-   <span class="function">win32\_set\_service\_exit\_code</span>
-   <a href="/win32service/constants.html#Win32Service%20Service%20Control%20Message%20Constants" class="link">Win32Service Service Control Message Constants</a>

win32\_pause\_service
=====================

Pauses a service

### 说明

<span class="type">void</span> <span
class="methodname">win32\_pause\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$machine`</span> \] )

Pauses a named service. Requires administrative privileges or an account
with appropriate rights set in the service's ACL.

### 参数

`servicename`  
The short name of the service.

`machine`  
Optional machine name. If omitted, the local machine is used.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |
| PECL win32service 0.3.0 | This function does not longer require an administrator account if ACL is set for another account.                                                                                                 |

### 参见

-   <span class="function">win32\_start\_service</span>
-   <span class="function">win32\_stop\_service</span>
-   <span class="function">win32\_continue\_service</span>
-   <span class="function">win32\_send\_custom\_control</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_query\_service\_status
=============================

Queries the status of a service

### 说明

<span class="type">array</span> <span
class="methodname">win32\_query\_service\_status</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$machine`</span> \] )

Queries the current status for a service, returning an array of
information.

### 参数

`servicename`  
The short name of the service.

`machine`  
The optional machine name. If omitted, the local machine will be used.

### 返回值

Returns an array consisting of the following information on success

Prior version 1.0.0，参数错误时返回 **`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

`ServiceType`  
The dwServiceType. See
<a href="/win32service/constants.html#Win32Service%20Service%20Type%20Bitmasks" class="link">Win32Service Service Type Bitmasks</a>.

`CurrentState`  
The dwCurrentState. See
<a href="/win32service/constants.html#Win32Service%20Service%20Status%20Constants" class="link">Win32Service Service Status Constants</a>.

`ControlsAccepted`  
Which service controls are accepted by the service. See
<a href="/win32service/constants.html#Win32Service%20Service%20Control%20Message%20Accepted%20Bitmasks" class="link">Win32Service Service Control Message Accepted Bitmasks</a>.

`Win32ExitCode`  
If the service exited, the return code from the process. This value is
equal to **`WIN32_ERROR_SERVICE_SPECIFIC_ERROR`** if the exit mode is
not gracefuly. See
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32Service error codes</a>
and <span class="function">win32\_set\_service\_exit\_mode</span>

`ServiceSpecificExitCode`  
If the service exited with an error condition, the service specific code
that is logged in the event log is visible here. This value is equal to
the value defined by <span
class="function">win32\_set\_service\_exit\_code</span>

`CheckPoint`  
If the service is shutting down, holds the current check point number.
This is used by the SCM as a kind of heart-beat to detect a wedged
service process. The value of the check point is best interpreted in
conjunction with the WaitHint value.

`WaitHint`  
If the service is shutting down it will set WaitHint to a checkpoint
value that will indicate 100% completion. This can be used to implement
a progress indicator.

`ProcessId`  
The Windows process identifier. If 0, the process is not running.

`ServiceFlags`  
The dwServiceFlags. See
<a href="/win32service/constants.html#Win32Service%20Service%20Flag%20Constants" class="link">Win32Service Service Service Flag Constants</a>.

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">array</span>, previously it was <span class="type">mixed</span>.                                                                                        |

### 参见

-   <a href="/win32service/constants.html" class="link">Win32Service Predefined Constants</a>

win32\_send\_custom\_control
============================

Send a custom control to the service

### 说明

<span class="type">void</span> <span
class="methodname">win32\_send\_custom\_control</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> , <span class="methodparam"><span
class="type">int</span> `$control`</span> \[, <span
class="methodparam"><span class="type">string</span> `$machine`</span>
\] )

See
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/winsvc/nf-winsvc-controlservice" class="link external">» Microsoft ControlService function</a>
for more details

### 参数

`servicename`  
The short name of the service.

`control`  
The custom contole value between 128 and 255.

`machine`  
Optional machine name. If omitted, the local machine is used.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

Prior to version 1.0.0, if the control value is not between 128 and 255,
this function emits an **`E_ERROR`** level error.

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

A <span class="classname">ValueError</span> is thrown if the; value of
`control` parameter is not between 128 and 255.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |

### 参见

-   <span class="function">win32\_start\_service</span>
-   <span class="function">win32\_stop\_service</span>
-   <span class="function">win32\_pause\_service</span>
-   <span class="function">win32\_continue\_service</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_set\_service\_exit\_code
===============================

Define or return the exit code for the current running service

### 说明

<span class="type">int</span> <span
class="methodname">win32\_set\_service\_exit\_code</span> (\[ <span
class="methodparam"><span class="type">int</span> `$exitCode`<span
class="initializer"> = 1</span></span> \] )

Change or return the exit code. The exit code is used only if the exit
mode is not graceful. If the value is not zero, the recovery
configuration can be used after service fail. See
<a href="https://docs.microsoft.com/en-us/windows/desktop/debug/system-error-codes" class="link external">» Microsoft system error codes</a>
for more details

**Caution**

This function work only in "cli" SAPI. On other SAPI this function is
disabled.

### 参数

`exitCode`  
The return code used on exit.

### 返回值

Return the current or old exit code.

### 错误／异常

Prior to version 1.0.0, if the SAPI is not *"cli"*, this function emits
an **`E_ERROR`** level error.

As of version 1.0.0, will throw a <span
class="classname">Win32ServiceException</span> if SAPI is not *"cli"*

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |

### 参见

-   <span
    class="function">win32\_start\_service\_ctrl\_dispatcher</span>
-   <span class="function">win32\_set\_service\_status</span>
-   <span class="function">win32\_set\_service\_exit\_mode</span>

win32\_set\_service\_exit\_mode
===============================

Define or return the exit mode for the current running service

### 说明

<span class="type">bool</span> <span
class="methodname">win32\_set\_service\_exit\_mode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$gracefulMode`<span
class="initializer"> = true</span></span> \] )

If `gracefulMode` parameter is provided, the exit mode is changed. When
the exit mode is not gracefuly, the exit code used can be set with the
<span class="function">win32\_set\_service\_exit\_code</span> function.

**Caution**

This function work only in "cli" SAPI. On other SAPI this function is
disabled.

### 参数

`gracefulMode`  
**`TRUE`** for exit graceful. **`FALSE`** for exit with error.

### 返回值

Return the current or old exit mode.

### 错误／异常

Prior to version 1.0.0, if the SAPI is not *"cli"*, this function emits
an **`E_ERROR`** level error.

As of version 1.0.0, will throw a <span
class="classname">Win32ServiceException</span> if SAPI is not *"cli"*

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |

### 参见

-   <span
    class="function">win32\_start\_service\_ctrl\_dispatcher</span>
-   <span class="function">win32\_set\_service\_status</span>
-   <span class="function">win32\_set\_service\_exit\_code</span>

win32\_set\_service\_status
===========================

Update the service status

### 说明

<span class="type">void</span> <span
class="methodname">win32\_set\_service\_status</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$checkpoint`<span class="initializer"> = 0</span></span> \] )

Informs the SCM of the current status of a running service. This call is
only valid for a running service process.

**Caution**

Since version 0.2.0, this function work only in "cli" SAPI. On other
SAPI this function is disabled.

### 参数

`status`  
The service status code, one of **`WIN32_SERVICE_RUNNING`**,
**`WIN32_SERVICE_STOPPED`**, **`WIN32_SERVICE_STOP_PENDING`**,
**`WIN32_SERVICE_START_PENDING`**, **`WIN32_SERVICE_CONTINUE_PENDING`**,
**`WIN32_SERVICE_PAUSE_PENDING`**, **`WIN32_SERVICE_PAUSED`**.

`checkpoint`  
The checkpoint value the service increments periodically to report its
progress during a lengthy start, stop, pause, or continue operation. For
example, the service should increment this value as it completes each
step of its initialization when it is starting up.

The `checkpoint` is only valid when the `status` is one of
**`WIN32_SERVICE_STOP_PENDING`**, **`WIN32_SERVICE_START_PENDING`**,
**`WIN32_SERVICE_CONTINUE_PENDING`** or
**`WIN32_SERVICE_PAUSE_PENDING`**.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

Prior to version 1.0.0, if the SAPI is not *"cli"*, this function emits
an **`E_ERROR`** level error.

As of version 1.0.0, will throw a <span
class="classname">Win32ServiceException</span> if SAPI is not *"cli"*

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |
| PECL win32service 0.2.0 | This function works only in the *"cli"* SAPI.                                                                                                                                                     |

### 参见

-   <span
    class="function">win32\_start\_service\_ctrl\_dispatcher</span>
-   <span class="function">win32\_get\_last\_control\_message</span>
-   <span class="function">win32\_set\_service\_exit\_mode</span>
-   <span class="function">win32\_set\_service\_exit\_code</span>
-   <a href="/win32service/constants.html#Win32Service%20Service%20Status%20Constants" class="link">Win32Service Service Status Constants</a>

win32\_start\_service\_ctrl\_dispatcher
=======================================

Registers the script with the SCM, so that it can act as the service
with the given name

### 说明

<span class="type">void</span> <span
class="methodname">win32\_start\_service\_ctrl\_dispatcher</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$gracefulMode`<span class="initializer"> =
true</span></span> \] )

When launched via the Service Control Manager, a service process is
required to "check-in" with it to establish service monitoring and
communication facilities. This function performs the check-in by
spawning a thread to handle the lower-level communication with the
service control manager.

Once started, the service process should do 2 things. The first is to
tell the Service Control Manager that the service is running. This is
achieved by calling <span
class="function">win32\_set\_service\_status</span> with the
**`WIN32_SERVICE_RUNNING`** constant. If you need to perform some
lengthy process before the service is actually running, then you can use
the **`WIN32_SERVICE_START_PENDING`** constant. The second is to
continue to check-in with the service control manager so that it can
determine if it should terminate. This is achieved by periodically
calling <span class="function">win32\_get\_last\_control\_message</span>
and handling the return code appropriately.

**Caution**

Since version 0.2.0, this function work only in "cli" SAPI. On other
SAPI this function is disabled.

### 参数

`name`  
The short-name of the service, as registered by <span
class="function">win32\_create\_service</span>.

`gracefulMode`  
**`TRUE`** for exit graceful. **`FALSE`** for exit with error. See <span
class="function">win32\_set\_service\_exit\_mode</span> for more
details.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

Prior to version 1.0.0, if the SAPI is not *"cli"*, this function emits
an **`E_ERROR`** level error.

As of version 1.0.0, will throw a <span
class="classname">Win32ServiceException</span> if SAPI is not *"cli"*

### 范例

**示例 \#1 A <span
class="function">win32\_start\_service\_ctrl\_dispatcher</span>
example**

Check if the service is runnig under the SCM.

``` php
<?php
if (!win32_start_service_ctrl_dispatcher('dummyphp')) {
  die("I'm probably not running under the service control manager");
}

win32_set_service_status(WIN32_SERVICE_START_PENDING);

// Some lengthy process to get this service up and running.

win32_set_service_status(WIN32_SERVICE_RUNNING);

while (WIN32_SERVICE_CONTROL_STOP != win32_get_last_control_message()) {
  # do some work here, trying not to take more than around 30 seconds
  # before coming back into the loop again
}
?>
```

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |
| PECL win32service 0.4.0 | The parameter `gracefulMode` has been added.                                                                                                                                                      |
| PECL win32service 0.2.0 | This function works only in the *"cli"* SAPI.                                                                                                                                                     |

### 参见

-   <span class="function">win32\_set\_service\_status</span>
-   <span class="function">win32\_get\_last\_control\_message</span>
-   <span class="function">win32\_set\_service\_exit\_mode</span>
-   <span class="function">win32\_set\_service\_exit\_code</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_start\_service
=====================

Starts a service

### 说明

<span class="type">void</span> <span
class="methodname">win32\_start\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$machine`</span> \] )

Attempts to start the named service. Requires administrative privileges
or an account with appropriate rights set in the service's ACL.

### 参数

`servicename`  
The short name of the service.

`machine`  
Optional machine name. If omitted, the local machine is used.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |
| PECL win32service 0.3.0 | This function does not longer require an administrator account if ACL is set for another account.                                                                                                 |

### 参见

-   <span class="function">win32\_stop\_service</span>
-   <span class="function">win32\_pause\_service</span>
-   <span class="function">win32\_continue\_service</span>
-   <span class="function">win32\_send\_custom\_control</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

win32\_stop\_service
====================

Stops a service

### 说明

<span class="type">void</span> <span
class="methodname">win32\_stop\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$servicename`</span> \[, <span class="methodparam"><span
class="type">string</span> `$machine`</span> \] )

Stops a named service. Requires administrative privileges or an account
with appropriate rights set in the service's ACL.

### 参数

`servicename`  
The short name of the service.

`machine`  
Optional machine name. If omitted, the local machine is used.

### 返回值

没有返回值。

Prior to version 1.0.0, 成功时返回 **`WIN32_NO_ERROR`**，参数错误时返回
**`FALSE`**，或失败时返回一个
<a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 错误码</a>。

### 错误／异常

A <span class="classname">ValueError</span> is thrown if the; value of
`servicename` parameter is empty.

A <span class="classname">Win32ServiceException</span> is thrown on
error.

### 更新日志

| 版本                    | 说明                                                                                                                                                                                              |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Throws a <span class="classname">ValueError</span> on invalid data in parameters, previously **`FALSE`** was returned.                                                                            |
| PECL win32service 1.0.0 | Throws a <span class="classname">Win32ServiceException</span> on error, previously a <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Code</a> was returned. |
| PECL win32service 1.0.0 | The return type is now <span class="type">void</span>, previously it was <span class="type">mixed</span>.                                                                                         |
| PECL win32service 0.3.0 | This function does not longer require an administrator account if ACL is set for another account.                                                                                                 |

### 参见

-   <span class="function">win32\_start\_service</span>
-   <span class="function">win32\_pause\_service</span>
-   <span class="function">win32\_continue\_service</span>
-   <span class="function">win32\_send\_custom\_control</span>
-   <a href="/win32service/constants.html#Win32%20Error%20Codes" class="link">Win32 Error Codes</a>

**目录**

-   [win32\_continue\_service](/ref/win32service.html#win32_continue_service)
    — Resumes a paused service
-   [win32\_create\_service](/ref/win32service.html#win32_create_service)
    — Creates a new service entry in the SCM database
-   [win32\_delete\_service](/ref/win32service.html#win32_delete_service)
    — Deletes a service entry from the SCM database
-   [win32\_get\_last\_control\_message](/ref/win32service.html#win32_get_last_control_message)
    — Returns the last control message that was sent to this service
-   [win32\_pause\_service](/ref/win32service.html#win32_pause_service)
    — Pauses a service
-   [win32\_query\_service\_status](/ref/win32service.html#win32_query_service_status)
    — Queries the status of a service
-   [win32\_send\_custom\_control](/ref/win32service.html#win32_send_custom_control)
    — Send a custom control to the service
-   [win32\_set\_service\_exit\_code](/ref/win32service.html#win32_set_service_exit_code)
    — Define or return the exit code for the current running service
-   [win32\_set\_service\_exit\_mode](/ref/win32service.html#win32_set_service_exit_mode)
    — Define or return the exit mode for the current running service
-   [win32\_set\_service\_status](/ref/win32service.html#win32_set_service_status)
    — Update the service status
-   [win32\_start\_service\_ctrl\_dispatcher](/ref/win32service.html#win32_start_service_ctrl_dispatcher)
    — Registers the script with the SCM, so that it can act as the
    service with the given name
-   [win32\_start\_service](/ref/win32service.html#win32_start_service)
    — Starts a service
-   [win32\_stop\_service](/ref/win32service.html#win32_stop_service) —
    Stops a service
