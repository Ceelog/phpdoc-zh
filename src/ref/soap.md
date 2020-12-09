is\_soap\_fault
===============

Checks if a SOAP call has failed

### 说明

<span class="type">bool</span> <span
class="methodname">is\_soap\_fault</span> ( <span
class="methodparam"><span class="type">mixed</span> `$object`</span> )

This function is useful to check if the SOAP call failed, but without
using exceptions. To use it, create a <span
class="classname">SoapClient</span> object with the *exceptions* option
set to zero or **`false`**. In this case, the SOAP method will return a
special <span class="classname">SoapFault</span> object which
encapsulates the fault details (faultcode, faultstring, faultactor and
faultdetails).

If *exceptions* is not set then SOAP call will throw an exception on
error. <span class="function">is\_soap\_fault</span> checks if the given
parameter is a <span class="classname">SoapFault</span> object.

### 参数

`object`  
The object to test.

### 返回值

This will return **`true`** on error, and **`false`** otherwise.

### 范例

**示例 \#1 <span class="function">is\_soap\_fault</span> example**

``` php
<?php
$client = new SoapClient("some.wsdl", array('exceptions' => 0));
$result = $client->SomeFunction();
if (is_soap_fault($result)) {
    trigger_error("SOAP Fault: (faultcode: {$result->faultcode}, faultstring: {$result->faultstring})", E_USER_ERROR);
}
?>
```

**示例 \#2 SOAP's standard method for error reporting is exceptions**

``` php
<?php
try {
    $client = new SoapClient("some.wsdl");
    $result = $client->SomeFunction(/* ... */);
} catch (SoapFault $fault) {
    trigger_error("SOAP Fault: (faultcode: {$fault->faultcode}, faultstring: {$fault->faultstring})", E_USER_ERROR);
}
?>
```

### 参见

-   <span class="methodname">SoapClient::SoapClient</span>
-   <span class="methodname">SoapFault::SoapFault</span>

use\_soap\_error\_handler
=========================

Set whether to use the SOAP error handler

### 说明

<span class="type">bool</span> <span
class="methodname">use\_soap\_error\_handler</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$handler`<span
class="initializer"> = **`true`**</span></span> \] )

This function sets whether or not to use the SOAP error handler in the
SOAP server. It will return the previous value. If set to **`true`**,
details of errors in a <span class="classname">SoapServer</span>
application will be sent to the client as a SOAP fault message. If
**`false`**, the standard PHP error handler is used. The default is to
send error to the client as SOAP fault message.

### 参数

`handler`  
Set to **`true`** to send error details to clients.

### 返回值

Returns the original value.

### 参见

-   <span class="function">set\_error\_handler</span>
-   <span class="function">set\_exception\_handler</span>

**目录**

-   [is\_soap\_fault](/ref/soap.html#is_soap_fault) — Checks if a SOAP
    call has failed
-   [use\_soap\_error\_handler](/ref/soap.html#use_soap_error_handler) —
    Set whether to use the SOAP error handler
