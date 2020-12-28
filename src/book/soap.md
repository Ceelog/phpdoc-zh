SOAP
====

**目录**

-   [简介](/intro/soap.html)
-   [安装／配置](/soap/setup.html)
    -   [需求](/soap/setup.html#需求)
    -   [安装](/soap/setup.html#安装)
    -   [运行时配置](/soap/setup.html#运行时配置)
    -   [资源类型](/soap/setup.html#资源类型)
-   [预定义常量](/soap/constants.html)
-   [SOAP 函数](/ref/soap.html)
    -   [is\_soap\_fault](/ref/soap.html#is_soap_fault) — Checks if a
        SOAP call has failed
    -   [use\_soap\_error\_handler](/ref/soap.html#use_soap_error_handler)
        — Set whether to use the SOAP error handler
-   [SoapClient](/class/soapclient.html) — The SoapClient class
    -   [SoapClient::\_\_call](/class/soapclient.html#SoapClient::__call)
        — Calls a SOAP function (deprecated)
    -   [SoapClient::\_\_construct](/class/soapclient.html#SoapClient::__construct)
        — SoapClient constructor
    -   [SoapClient::\_\_doRequest](/class/soapclient.html#SoapClient::__doRequest)
        — Performs a SOAP request
    -   [SoapClient::\_\_getCookies](/class/soapclient.html#SoapClient::__getCookies)
        — Get list of cookies
    -   [SoapClient::\_\_getFunctions](/class/soapclient.html#SoapClient::__getFunctions)
        — Returns list of available SOAP functions
    -   [SoapClient::\_\_getLastRequest](/class/soapclient.html#SoapClient::__getLastRequest)
        — Returns last SOAP request
    -   [SoapClient::\_\_getLastRequestHeaders](/class/soapclient.html#SoapClient::__getLastRequestHeaders)
        — Returns the SOAP headers from the last request
    -   [SoapClient::\_\_getLastResponse](/class/soapclient.html#SoapClient::__getLastResponse)
        — Returns last SOAP response
    -   [SoapClient::\_\_getLastResponseHeaders](/class/soapclient.html#SoapClient::__getLastResponseHeaders)
        — Returns the SOAP headers from the last response
    -   [SoapClient::\_\_getTypes](/class/soapclient.html#SoapClient::__getTypes)
        — Returns a list of SOAP types
    -   [SoapClient::\_\_setCookie](/class/soapclient.html#SoapClient::__setCookie)
        — The \_\_setCookie purpose
    -   [SoapClient::\_\_setLocation](/class/soapclient.html#SoapClient::__setLocation)
        — Sets the location of the Web service to use
    -   [SoapClient::\_\_setSoapHeaders](/class/soapclient.html#SoapClient::__setSoapHeaders)
        — Sets SOAP headers for subsequent calls
    -   [SoapClient::\_\_soapCall](/class/soapclient.html#SoapClient::__soapCall)
        — Calls a SOAP function
    -   [SoapClient::SoapClient](/class/soapclient.html#SoapClient::SoapClient)
        — SoapClient constructor
-   [SoapServer](/class/soapserver.html) — The SoapServer class
    -   [SoapServer::addFunction](/class/soapserver.html#SoapServer::addFunction)
        — 添加一个或多个函数来处理SOAP请求
    -   [SoapServer::addSoapHeader](/class/soapserver.html#SoapServer::addSoapHeader)
        — Add a SOAP header to the response
    -   [SoapServer::\_\_construct](/class/soapserver.html#SoapServer::__construct)
        — SoapServer constructor
    -   [SoapServer::fault](/class/soapserver.html#SoapServer::fault) —
        Issue SoapServer fault indicating an error
    -   [SoapServer::getFunctions](/class/soapserver.html#SoapServer::getFunctions)
        — Returns list of defined functions
    -   [SoapServer::handle](/class/soapserver.html#SoapServer::handle)
        — Handles a SOAP request
    -   [SoapServer::setClass](/class/soapserver.html#SoapServer::setClass)
        — Sets the class which handles SOAP requests
    -   [SoapServer::setObject](/class/soapserver.html#SoapServer::setObject)
        — Sets the object which will be used to handle SOAP requests
    -   [SoapServer::setPersistence](/class/soapserver.html#SoapServer::setPersistence)
        — Sets SoapServer persistence mode
    -   [SoapServer::SoapServer](/class/soapserver.html#SoapServer::SoapServer)
        — SoapServer constructor
-   [SoapFault](/class/soapfault.html) — The SoapFault class
    -   [SoapFault::\_\_construct](/class/soapfault.html#SoapFault::__construct)
        — SoapFault constructor
    -   [SoapFault::SoapFault](/class/soapfault.html#SoapFault::SoapFault)
        — SoapFault constructor
    -   [SoapFault::\_\_toString](/class/soapfault.html#SoapFault::__toString)
        — Obtain a string representation of a SoapFault
-   [SoapHeader](/class/soapheader.html) — The SoapHeader class
    -   [SoapHeader::\_\_construct](/class/soapheader.html#SoapHeader::__construct)
        — SoapHeader constructor
    -   [SoapHeader::SoapHeader](/class/soapheader.html#SoapHeader::SoapHeader)
        — SoapHeader constructor
-   [SoapParam](/class/soapparam.html) — The SoapParam class
    -   [SoapParam::\_\_construct](/class/soapparam.html#SoapParam::__construct)
        — SoapParam constructor
    -   [SoapParam::SoapParam](/class/soapparam.html#SoapParam::SoapParam)
        — SoapParam constructor
-   [SoapVar](/class/soapvar.html) — The SoapVar class
    -   [SoapVar::\_\_construct](/class/soapvar.html#SoapVar::__construct)
        — SoapVar constructor
    -   [SoapVar::SoapVar](/class/soapvar.html#SoapVar::SoapVar) —
        SoapVar constructor

简介
----

The SoapClient class provides a client for
<a href="http://www.w3.org/TR/soap11/" class="link external">» SOAP 1.1</a>,
<a href="http://www.w3.org/TR/soap12/" class="link external">» SOAP 1.2</a>
servers. It can be used in WSDL or non-WSDL mode.

类摘要
------

**SoapClient**

<span class="ooclass"> class **SoapClient** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$wsdl`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
\[\]</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_call</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
)

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">\_\_doRequest</span> ( <span
class="methodparam"><span class="type">string</span> `$request`</span> ,
<span class="methodparam"><span class="type">string</span>
`$location`</span> , <span class="methodparam"><span
class="type">string</span> `$action`</span> , <span
class="methodparam"><span class="type">int</span> `$version`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$oneWay`<span
class="initializer"> = **`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">\_\_getCookies</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">null</span></span> <span
class="methodname">\_\_getFunctions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">\_\_getLastRequest</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">\_\_getLastRequestHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">\_\_getLastResponse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">\_\_getLastResponseHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">null</span></span> <span
class="methodname">\_\_getTypes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_setCookie</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$value`<span class="initializer"> = **`null`**</span></span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">\_\_setLocation</span> (\[ <span
class="methodparam"><span class="type">string</span> `$location`<span
class="initializer"> = ""</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">\_\_setSoapHeaders</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">SoapHeader</span><span class="type">array</span><span
class="type">null</span></span> `$headers`<span class="initializer"> =
**`null`**</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_soapCall</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">array</span><span class="type">null</span></span>
`$options`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">SoapHeader</span><span class="type">array</span><span
class="type">null</span></span> `$inputHeaders`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">array</span>
`&$outputHeaders`<span class="initializer"> = **`null`**</span></span>
\]\]\] )

<span class="modifier">public</span> <span
class="methodname">SoapClient</span> ( <span class="methodparam"><span
class="type">mixed</span> `$wsdl`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

}

SoapClient::\_\_call
====================

Calls a SOAP function (deprecated)

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SoapClient::\_\_call</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
)

Calling this method directly is deprecated. Usually, SOAP functions can
be called as methods of the <span class="classname">SoapClient</span>
object; in situations where this is not possible or additional options
are needed, use <span class="function">SoapClient::\_\_soapCall</span>.

SoapClient::\_\_construct
=========================

SoapClient constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapClient::\_\_construct</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$wsdl`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
\[\]</span></span> \] )

此函数是该函数的别名： <span
class="methodname">SoapClient::SoapClient</span>

SoapClient::\_\_doRequest
=========================

Performs a SOAP request

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_doRequest</span> ( <span
class="methodparam"><span class="type">string</span> `$request`</span> ,
<span class="methodparam"><span class="type">string</span>
`$location`</span> , <span class="methodparam"><span
class="type">string</span> `$action`</span> , <span
class="methodparam"><span class="type">int</span> `$version`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$oneWay`<span
class="initializer"> = **`false`**</span></span> \] )

Performs SOAP request over HTTP.

This method can be overridden in subclasses to implement different
transport layers, perform additional XML processing or other purpose.

### 参数

`request`  
The XML SOAP request.

`location`  
The URL to request.

`action`  
The SOAP action.

`version`  
The SOAP version.

`oneWay`  
If *one\_way* is set to 1, this method returns nothing. Use this where a
response is not expected.

### 返回值

The XML SOAP response.

### 更新日志

| 版本  | 说明                                                                                                       |
|-------|------------------------------------------------------------------------------------------------------------|
| 8.0.0 | The type of `oneWay` is <span class="type">bool</span> now; formerly it was <span class="type">int</span>. |

### 范例

**示例 \#1 <span class="function">SoapClient::\_\_doRequest</span>
example**

``` php
<?php
function Add($x,$y) {
  return $x+$y;
}

class LocalSoapClient extends SoapClient {

  function __construct($wsdl, $options) {
    parent::__construct($wsdl, $options);
    $this->server = new SoapServer($wsdl, $options);
    $this->server->addFunction('Add');
  }

  function __doRequest($request, $location, $action, $version, $one_way = 0) {
    ob_start();
    $this->server->handle($request);
    $response = ob_get_contents();
    ob_end_clean();
    return $response;
  }

}

$x = new LocalSoapClient(NULL,array('location'=>'test://', 
                                   'uri'=>'http://testuri.org')); 
var_dump($x->Add(3,4));
?>
```

SoapClient::\_\_getCookies
==========================

Get list of cookies

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SoapClient::\_\_getCookies</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

SoapClient::\_\_getFunctions
============================

Returns list of available SOAP functions

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_getFunctions</span> ( <span
class="methodparam">void</span> )

Returns an array of functions described in the WSDL for the Web service.

> **Note**:
>
> 此函数仅在 WSDL 模式下生效。

### 参数

此函数没有参数。

### 返回值

The <span class="type">array</span> of SOAP function prototypes,
detailing the return type, the function name and type-hinted parameters.

### 范例

**示例 \#1 <span class="function">SoapClient::\_\_getFunctions</span>
example**

``` php
<?php
$client = new SoapClient('http://soap.amazon.com/schemas3/AmazonWebServices.wsdl');
var_dump($client->__getFunctions());
?>
```

以上例程会输出：

    array(26) {
      [0]=>
      string(70) "ProductInfo KeywordSearchRequest(KeywordRequest $KeywordSearchRequest)"
      [1]=>
      string(79) "ProductInfo TextStreamSearchRequest(TextStreamRequest $TextStreamSearchRequest)"
      [2]=>
      string(64) "ProductInfo PowerSearchRequest(PowerRequest $PowerSearchRequest)"
    ...
      [23]=>
      string(107) "ShoppingCart RemoveShoppingCartItemsRequest(RemoveShoppingCartItemsRequest $RemoveShoppingCartItemsRequest)"
      [24]=>
      string(107) "ShoppingCart ModifyShoppingCartItemsRequest(ModifyShoppingCartItemsRequest $ModifyShoppingCartItemsRequest)"
      [25]=>
      string(118) "GetTransactionDetailsResponse GetTransactionDetailsRequest(GetTransactionDetailsRequest $GetTransactionDetailsRequest)"
    }

### 参见

-   <span class="methodname">SoapClient::SoapClient</span>

SoapClient::\_\_getLastRequest
==============================

Returns last SOAP request

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_getLastRequest</span> ( <span
class="methodparam">void</span> )

Returns the XML sent in the last SOAP request.

> **Note**:
>
> This method works only if the <span
> class="classname">SoapClient</span> object was created with the
> *trace* option set to **`true`**.

### 参数

此函数没有参数。

### 返回值

The last SOAP request, as an XML string.

### 范例

**示例 \#1 SoapClient::\_\_getLastRequest() example**

``` php
<?php
$client = new SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "REQUEST:\n" . $client->__getLastRequest() . "\n";
?>
```

### 参见

-   <span
    class="methodname">SoapClient::\_\_getLastRequestHeaders</span>
-   <span class="methodname">SoapClient::\_\_getLastResponse</span>
-   <span
    class="methodname">SoapClient::\_\_getLastResponseHeaders</span>

SoapClient::\_\_getLastRequestHeaders
=====================================

Returns the SOAP headers from the last request

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_getLastRequestHeaders</span> ( <span
class="methodparam">void</span> )

Returns the SOAP headers from the last request.

> **Note**:
>
> This function only works if the <span
> class="classname">SoapClient</span> object was created with the
> *trace* option set to **`true`**.

### 参数

此函数没有参数。

### 返回值

The last SOAP request headers.

### 范例

**示例 \#1 SoapClient::\_\_getLastRequestHeaders() example**

``` php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "REQUEST HEADERS:\n" . $client->__getLastRequestHeaders() . "\n";
?>
```

### 参见

-   <span
    class="methodname">SoapClient::\_\_getLastResponseHeaders</span>
-   <span class="methodname">SoapClient::\_\_getLastRequest</span>
-   <span class="methodname">SoapClient::\_\_getLastResponse</span>

SoapClient::\_\_getLastResponse
===============================

Returns last SOAP response

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_getLastResponse</span> ( <span
class="methodparam">void</span> )

Returns the XML received in the last SOAP response.

> **Note**:
>
> This method works only if the <span
> class="classname">SoapClient</span> object was created with the
> *trace* option set to **`true`**.

### 参数

此函数没有参数。

### 返回值

The last SOAP response, as an XML string.

### 范例

**示例 \#1 SoapClient::\_\_getLastResponse() example**

``` php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "Response:\n" . $client->__getLastResponse() . "\n";
?>
```

### 参见

-   <span
    class="methodname">SoapClient::\_\_getLastResponseHeaders</span>
-   <span class="methodname">SoapClient::\_\_getLastRequest</span>
-   <span
    class="methodname">SoapClient::\_\_getLastRequestHeaders</span>

SoapClient::\_\_getLastResponseHeaders
======================================

Returns the SOAP headers from the last response

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_getLastResponseHeaders</span> ( <span
class="methodparam">void</span> )

Returns the SOAP headers from the last response.

> **Note**:
>
> This function only works if the <span
> class="classname">SoapClient</span> object was created with the
> *trace* option set to **`true`**.

### 参数

此函数没有参数。

### 返回值

The last SOAP response headers.

### 范例

**示例 \#1 SoapClient::\_\_getLastResponse() example**

``` php
<?php
$client = SoapClient("some.wsdl", array('trace' => 1));
$result = $client->SomeFunction();
echo "RESPONSE HEADERS:\n" . $client->__getLastResponseHeaders() . "\n";
?>
```

### 参见

-   <span
    class="methodname">SoapClient::\_\_getLastRequestHeaders</span>
-   <span class="methodname">SoapClient::\_\_getLastRequest</span>
-   <span class="methodname">SoapClient::\_\_getLastResponse</span>

SoapClient::\_\_getTypes
========================

Returns a list of SOAP types

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_getTypes</span> ( <span
class="methodparam">void</span> )

Returns an array of types described in the WSDL for the Web service.

> **Note**:
>
> 此函数仅在 WSDL 模式下生效。

### 参数

此函数没有参数。

### 返回值

The <span class="type">array</span> of SOAP types, detailing all
structures and types.

### 范例

**示例 \#1 <span class="function">SoapClient::\_\_getTypes</span>
example**

``` php
<?php
$client = new SoapClient('http://soap.amazon.com/schemas3/AmazonWebServices.wsdl');
var_dump($client->__getTypes());
?>
```

以上例程会输出：

    array(88) {
      [0]=>
      string(30) "ProductLine ProductLineArray[]"
      [1]=>
      string(85) "struct ProductLine {
     string Mode;
     string RelevanceRank;
     ProductInfo ProductInfo;
    }"
      [2]=>
      string(105) "struct ProductInfo {
     string TotalResults;
     string TotalPages;
     string ListName;
     DetailsArray Details;
    }"
    ...
      [85]=>
      string(32) "ShortSummary ShortSummaryArray[]"
      [86]=>
      string(121) "struct GetTransactionDetailsRequest {
     string tag;
     string devtag;
     string key;
     OrderIdArray OrderIds;
     string locale;
    }"
      [87]=>
      string(75) "struct GetTransactionDetailsResponse {
     ShortSummaryArray ShortSummaries;
    }"
    }

### 参见

-   <span class="methodname">SoapClient::SoapClient</span>

SoapClient::\_\_setCookie
=========================

The \_\_setCookie purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapClient::\_\_setCookie</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$value`<span class="initializer"> = **`null`**</span></span> \] )

Defines a cookie to be sent along with the SOAP requests.

> **Note**:
>
> Calling this method will affect all following calls to <span
> class="classname">SoapClient</span> methods.

### 参数

`name`  
The name of the cookie.

`value`  
The value of the cookie. If not specified, the cookie will be deleted.

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                     |
|-------|--------------------------|
| 8.0.0 | `value` is now nullable. |

SoapClient::\_\_setLocation
===========================

Sets the location of the Web service to use

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">SoapClient::\_\_setLocation</span> (\[ <span
class="methodparam"><span class="type">string</span> `$location`<span
class="initializer"> = ""</span></span> \] )

Sets the endpoint URL that will be touched by following SOAP requests.
This is equivalent to specifying the *location* option when constructing
the SoapClient.

> **Note**:
>
> Calling this method is optional. The SoapClient uses the endpoint from
> the WSDL file by default.

### 参数

`location`  
The new endpoint URL.

### 返回值

The old endpoint URL.

### 范例

**示例 \#1 <span class="function">SoapClient::\_\_setLocation</span>
example**

``` php
<?php
$client = new SoapClient('http://example.com/webservice.php?wsdl');

$client->__setLocation('http://www.somethirdparty.com');

$old_location = $client->__setLocation(); // unsets the location option

echo $old_location;

?>
```

以上例程的输出类似于：

    http://www.somethirdparty.com

### 参见

-   <span class="methodname">SoapClient::SoapClient</span>

SoapClient::\_\_setSoapHeaders
==============================

Sets SOAP headers for subsequent calls

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SoapClient::\_\_setSoapHeaders</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">SoapHeader</span><span class="type">array</span><span
class="type">null</span></span> `$headers`<span class="initializer"> =
**`null`**</span></span> \] )

Defines headers to be sent along with the SOAP requests.

> **Note**:
>
> Calling this method will replace any previous values.

### 参数

`headers`  
The headers to be set. It could be <span
class="classname">SoapHeader</span> object or array of <span
class="classname">SoapHeader</span> objects. If not specified or set to
**`null`**, the headers will be deleted.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">SoapClient::\_\_setSoapHeaders</span>
example**

``` php
<?php

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$header = new SoapHeader('http://soapinterop.org/echoheader/', 
                            'echoMeStringRequest',
                            'hello world');

$client->__setSoapHeaders($header);

$client->__soapCall("echoVoid", null);
?>
```

**示例 \#2 Set Multiple Headers**

``` php
<?php

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$headers = array();

$headers[] = new SoapHeader('http://soapinterop.org/echoheader/', 
                            'echoMeStringRequest',
                            'hello world');

$headers[] = new SoapHeader('http://soapinterop.org/echoheader/', 
                            'echoMeStringRequest',
                            'hello world again');

$client->__setSoapHeaders($headers);

$client->__soapCall("echoVoid", null);
?>
```

SoapClient::\_\_soapCall
========================

Calls a SOAP function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SoapClient::\_\_soapCall</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">array</span><span class="type">null</span></span>
`$options`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type"><span
class="type">SoapHeader</span><span class="type">array</span><span
class="type">null</span></span> `$inputHeaders`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">array</span>
`&$outputHeaders`<span class="initializer"> = **`null`**</span></span>
\]\]\] )

This is a low level API function that is used to make a SOAP call.
Usually, in WSDL mode, SOAP functions can be called as methods of the
<span class="classname">SoapClient</span> object. This method is useful
in non-WSDL mode when *soapaction* is unknown, *uri* differs from the
default or when sending and/or receiving SOAP Headers.

On error, a call to a SOAP function can cause PHP to throw exceptions or
return a <span class="classname">SoapFault</span> object if exceptions
are disabled. To check if the function call failed to catch the
SoapFault exceptions, check the result with <span
class="function">is\_soap\_fault</span>.

### 参数

`name`  
The name of the SOAP function to call.

`args`  
An array of the arguments to pass to the function. This can be either an
ordered or an associative array. Note that most SOAP servers require
parameter names to be provided, in which case this must be an
associative array.

`options`  
An associative array of options to pass to the client.

The *location* option is the URL of the remote Web service.

The *uri* option is the target namespace of the SOAP service.

The *soapaction* option is the action to call.

`inputHeaders`  
An array of headers to be sent along with the SOAP request.

`outputHeaders`  
If supplied, this array will be filled with the headers from the SOAP
response.

### 返回值

SOAP functions may return one, or multiple values. If only one value is
returned by the SOAP function, the return value of *\_\_soapCall* will
be a simple value (e.g. an integer, a string, etc). If multiple values
are returned, *\_\_soapCall* will return an associative array of named
output parameters.

On error, if the SoapClient object was constructed with the *exceptions*
option set to **`false`**, a SoapFault object will be returned.

### 范例

**示例 \#1 <span class="function">SoapClient::\_\_soapCall</span>
example**

``` php
<?php

$client = new SoapClient("some.wsdl");
$client->SomeFunction($a, $b, $c);

$client->__soapCall("SomeFunction", array($a, $b, $c));
$client->__soapCall("SomeFunction", array($a, $b, $c), NULL,
                    new SoapHeader(), $output_headers);


$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$client->SomeFunction($a, $b, $c);
$client->__soapCall("SomeFunction", array($a, $b, $c));
$client->__soapCall("SomeFunction", array($a, $b, $c),
                    array('soapaction' => 'some_action',
                          'uri'        => 'some_uri'));
?>
```

### 参见

-   <span class="methodname">SoapClient::SoapClient</span>
-   <span class="methodname">SoapParam::SoapParam</span>
-   <span class="methodname">SoapVar::SoapVar</span>
-   <span class="methodname">SoapHeader::SoapHeader</span>
-   <span class="methodname">SoapFault::SoapFault</span>
-   <span class="function">is\_soap\_fault</span>

SoapClient::SoapClient
======================

SoapClient constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapClient::SoapClient</span> ( <span
class="methodparam"><span class="type">mixed</span> `$wsdl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

This constructor creates <span class="classname">SoapClient</span>
objects in *WSDL* or *non-WSDL* mode.

### 参数

`wsdl`  
URI of the *WSDL* file or **`null`** if working in *non-WSDL* mode.

> **Note**:
>
> During development, WSDL caching may be disabled by the use of the
> *soap.wsdl\_cache\_ttl* `php.ini` setting otherwise changes made to
> the WSDL file will have no effect until *soap.wsdl\_cache\_ttl* is
> expired.

`options`  
An array of options. If working in WSDL mode, this parameter is
optional. If working in non-WSDL mode, the *location* and *uri* options
must be set, where *location* is the URL of the SOAP server to send the
request to, and *uri* is the target namespace of the SOAP service.

The *style* and *use* options only work in non-WSDL mode. In WSDL mode,
they come from the WSDL file.

The *soap\_version* option should be one of either **`SOAP_1_1`** or
**`SOAP_1_2`** to select SOAP 1.1 or 1.2, respectively. If omitted, 1.1
is used.

For HTTP authentication, the *login* and *password* options can be used
to supply credentials. For making an HTTP connection through a proxy
server, the options *proxy\_host*, *proxy\_port*, *proxy\_login* and
*proxy\_password* are also available. For HTTPS client certificate
authentication use *local\_cert* and *passphrase* options. An
authentication may be supplied in the *authentication* option. The
authentication method may be either **`SOAP_AUTHENTICATION_BASIC`**
(default) or **`SOAP_AUTHENTICATION_DIGEST`**.

The *compression* option allows to use compression of HTTP SOAP requests
and responses.

The *encoding* option defines internal character encoding. This option
does not change the encoding of SOAP requests (it is always utf-8), but
converts strings into it.

The *trace* option enables tracing of request so faults can be
backtraced. This defaults to **`false`**

The *classmap* option can be used to map some WSDL types to PHP classes.
This option must be an array with WSDL types as keys and names of PHP
classes as values.

Setting the boolean *trace* option enables use of the methods
<a href="/class/soapclient.html#SoapClient::__getLastRequest" class="link">SoapClient-&gt;__getLastRequest</a>,
<a href="/class/soapclient.html#SoapClient::__getLastRequestHeaders" class="link">SoapClient-&gt;__getLastRequestHeaders</a>,
<a href="/class/soapclient.html#SoapClient::__getLastResponse" class="link">SoapClient-&gt;__getLastResponse</a>
and
<a href="/class/soapclient.html#SoapClient::__getLastResponseHeaders" class="link">SoapClient-&gt;__getLastResponseHeaders</a>.

The *exceptions* option is a boolean value defining whether soap errors
throw exceptions of type
<a href="/class/soapfault.html#SoapFault::SoapFault" class="link">SoapFault</a>.

The *connection\_timeout* option defines a timeout in seconds for the
connection to the SOAP service. This option does not define a timeout
for services with slow responses. To limit the time to wait for calls to
finish the
<a href="/filesystem/setup.html#" class="link">default_socket_timeout</a>
setting is available.

The *typemap* option is an array of type mappings. Type mapping is an
array with keys *type\_name*, *type\_ns* (namespace URI), *from\_xml*
(callback accepting one string parameter) and *to\_xml* (callback
accepting one object parameter).

The *cache\_wsdl* option is one of **`WSDL_CACHE_NONE`**,
**`WSDL_CACHE_DISK`**, **`WSDL_CACHE_MEMORY`** or **`WSDL_CACHE_BOTH`**.

The *user\_agent* option specifies string to use in *User-Agent* header.

The *stream\_context* option is a <span class="type">resource</span> for
<a href="/context.html" class="link">context</a>.

The *features* option is a bitmask of **`SOAP_SINGLE_ELEMENT_ARRAYS`**,
**`SOAP_USE_XSI_ARRAY_TYPE`**, **`SOAP_WAIT_ONE_WAY_CALLS`**.

The *keep\_alive* option is a boolean value defining whether to send the
*Connection: Keep-Alive* header or *Connection: close*.

The *ssl\_method* option is one of **`SOAP_SSL_METHOD_TLS`**,
**`SOAP_SSL_METHOD_SSLv2`**, **`SOAP_SSL_METHOD_SSLv3`** or
**`SOAP_SSL_METHOD_SSLv23`**.

### 错误／异常

<span class="methodname">SoapClient::SoapClient</span> will generate an
**`E_ERROR`** error if the *location* and *uri* options aren't provided
in non-WSDL mode.

A <span class="classname">SoapFault</span> exception will be thrown if
the `wsdl` URI cannot be loaded.

### 范例

**示例 \#1 <span class="function">SoapClient::SoapClient</span>
example**

``` php
<?php

$client = new SoapClient("some.wsdl");

$client = new SoapClient("some.wsdl", array('soap_version'   => SOAP_1_2));

$client = new SoapClient("some.wsdl", array('login'          => "some_name",
                                            'password'       => "some_password"));

$client = new SoapClient("some.wsdl", array('proxy_host'     => "localhost",
                                            'proxy_port'     => 8080));

$client = new SoapClient("some.wsdl", array('proxy_host'     => "localhost",
                                            'proxy_port'     => 8080,
                                            'proxy_login'    => "some_name",
                                            'proxy_password' => "some_password"));

$client = new SoapClient("some.wsdl", array('local_cert'     => "cert_key.pem"));

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/",
                                     'style'    => SOAP_DOCUMENT,
                                     'use'      => SOAP_LITERAL));

$client = new SoapClient("some.wsdl", 
  array('compression' => SOAP_COMPRESSION_ACCEPT | SOAP_COMPRESSION_GZIP));

$client = new SoapClient("some.wsdl", array('encoding'=>'ISO-8859-1'));

class MyBook {
    public $title;
    public $author;
}

$client = new SoapClient("books.wsdl", array('classmap' => array('book' => "MyBook")));

?>
```

简介
----

The SoapServer class provides a server for the
<a href="http://www.w3.org/TR/soap11/" class="link external">» SOAP 1.1</a>
and
<a href="http://www.w3.org/TR/soap12/" class="link external">» SOAP 1.2</a>
protocols. It can be used with or without a WSDL service description.

类摘要
------

**SoapServer**

<span class="ooclass"> class **SoapServer** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$wsdl`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
\[\]</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFunction</span> ( <span
class="methodparam"><span class="type">mixed</span> `$functions`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addSoapHeader</span> ( <span
class="methodparam"><span class="type">SoapHeader</span>
`$header`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">fault</span> ( <span class="methodparam"><span
class="type">string</span> `$code`</span> , <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$actor`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$details`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$name`<span
class="initializer"> = ""</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getFunctions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">handle</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$request`<span class="initializer"> = **`null`**</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setClass</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$args`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setObject</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPersistence</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="modifier">public</span> <span
class="methodname">SoapServer</span> ( <span class="methodparam"><span
class="type">mixed</span> `$wsdl`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

}

SoapServer::addFunction
=======================

添加一个或多个函数来处理SOAP请求

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::addFunction</span> ( <span
class="methodparam"><span class="type">mixed</span> `$functions`</span>
)

为远程客户端导出一个或多个函数

### 参数

`functions`  
导出一个函数，将函数名作为字符串传递给这个参数。

导出多个函数，将一组函数名作为数组传递。

导出所有函数，传递特殊常量 **`SOAP_FUNCTIONS_ALL`**.

> **Note**:
>
> `functions` 接收的所有输入参数必须同时和WSDL文件中定义的
> 顺序一样（它们不应该接收任何输出变量作为参数）并且返回一个或多个值。如果要返回多个
> 值，它们必须返回一组被命名的输出参数作为数组。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">SoapServer::addFunction</span>
example**

``` php
<?php

function echoString($inputString)
{
    return $inputString;
}

$server->addFunction("echoString");

function echoTwoStrings($inputString1, $inputString2)
{
    return array("outputString1" => $inputString1,
                 "outputString2" => $inputString2);
}
$server->addFunction(array("echoString", "echoTwoStrings"));

$server->addFunction(SOAP_FUNCTIONS_ALL);

?>
```

### 参见

-   <span class="methodname">SoapServer::SoapServer</span>
-   <span class="methodname">SoapServer::setClass</span>

SoapServer::addSoapHeader
=========================

Add a SOAP header to the response

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::addSoapHeader</span> ( <span
class="methodparam"><span class="type">SoapHeader</span>
`$header`</span> )

Adds a SOAP header to be returned with the response to the current
request.

### 参数

`header`  
The header to be returned.

### 返回值

没有返回值。

SoapServer::\_\_construct
=========================

SoapServer constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapServer::\_\_construct</span> ( <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$wsdl`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
\[\]</span></span> \] )

此函数是该函数的别名： <span
class="methodname">SoapServer::SoapServer</span>

SoapServer::fault
=================

Issue SoapServer fault indicating an error

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::fault</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> ,
<span class="methodparam"><span class="type">string</span>
`$string`</span> \[, <span class="methodparam"><span
class="type">string</span> `$actor`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$details`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$name`<span class="initializer"> =
""</span></span> \]\]\] )

Sends a response to the client of the current request indicating an
error.

> **Note**:
>
> This can only be called when handling a request.

### 参数

`code`  
The error code to return

`string`  
A brief description of the error

`actor`  
A string identifying the actor that caused the fault.

`details`  
More details of the fault

`name`  
The name of the fault. This can be used to select a name from a WSDL
file.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">SoapFault::SoapFault</span>

SoapServer::getFunctions
========================

Returns list of defined functions

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SoapServer::getFunctions</span> ( <span
class="methodparam">void</span> )

Returns a list of the defined functions in the SoapServer object. This
method returns the list of all functions added by <span
class="methodname">SoapServer::addFunction</span> or <span
class="methodname">SoapServer::setClass</span>.

### 参数

此函数没有参数。

### 返回值

An *array* of the defined functions.

### 范例

**示例 \#1 <span class="function">SoapServer::getFunctions</span>
example**

``` php
<?php
$server = new SoapServer(NULL, array("uri" => "http://test-uri"));
$server->addFunction(SOAP_FUNCTIONS_ALL);
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  $server->handle();
} else {
  echo "This SOAP server can handle following functions: ";
  $functions = $server->getFunctions();
  foreach($functions as $func) {
    echo $func . "\n";
  }
}
?>
```

### 参见

-   <span class="methodname">SoapServer::SoapServer</span>
-   <span class="methodname">SoapServer::addFunction</span>
-   <span class="methodname">SoapServer::setClass</span>

SoapServer::handle
==================

Handles a SOAP request

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::handle</span> (\[ <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$request`<span class="initializer"> = **`null`**</span></span> \] )

Processes a SOAP request, calls necessary functions, and sends a
response back.

### 参数

`request`  
The SOAP request. If this argument is omitted, the request is assumed to
be in the raw POST data of the HTTP request.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">SoapServer::handle</span> example**

``` php
<?php
function test($x)
{
    return $x;
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 8.0.0 | `request` is now nullable. |

### 参见

-   <span class="methodname">SoapServer::SoapServer</span>

SoapServer::setClass
====================

Sets the class which handles SOAP requests

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::setClass</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$args`</span>
)

Exports all methods from specified class.

The object can be made persistent across request for a given PHP session
with the <span class="methodname">SoapServer::setPersistence</span>
method.

### 参数

`class`  
The name of the exported class.

`args`  
These optional parameters will be passed to the default class
constructor during object creation.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">SoapServer::SoapServer</span>
-   <span class="methodname">SoapServer::addFunction</span>
-   <span class="methodname">SoapServer::setPersistence</span>

SoapServer::setObject
=====================

Sets the object which will be used to handle SOAP requests

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::setObject</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

This sets a specific object as the handler for SOAP requests, rather
than just a class as in <span
class="methodname">SoapServer::setClass</span>.

### 参数

`object`  
The object to handle the requests.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">SoapServer::setClass</span>

SoapServer::setPersistence
==========================

Sets SoapServer persistence mode

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SoapServer::setPersistence</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

This function allows changing the persistence state of a SoapServer
object between requests. This function allows saving data between
requests utilizing PHP sessions. This method only has an affect on a
SoapServer after it has exported functions utilizing <span
class="methodname">SoapServer::setClass</span>.

> **Note**:
>
> The persistence of **`SOAP_PERSISTENCE_SESSION`** makes only objects
> of the given class persistent, but not the class static data. In this
> case, use `$this->bar` instead of self::$bar.

> **Note**:
>
> **`SOAP_PERSISTENCE_SESSION`** serializes data on the class object
> between requests. In order to properly utilize resources (e.g. <span
> class="classname">PDO</span>),
> <a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
> and
> <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
> magic methods should be utilized.

### 参数

`mode`  
One of the *SOAP\_PERSISTENCE\_XXX* constants.

**`SOAP_PERSISTENCE_REQUEST`** - SoapServer data does not persist
between requests. This is the *default* behavior of any SoapServer
object after setClass is called.

**`SOAP_PERSISTENCE_SESSION`** - SoapServer data persists between
requests. This is accomplished by serializing the SoapServer class data
into `$_SESSION['_bogus_session_name']`, because of this <span
class="function">session\_start</span> must be called before this
persistence mode is set.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">SoapServer::setPersistence</span>
example**

``` php
<?php
 class MyFirstPersistentSoapServer {
     private $resource; // (Such as PDO, mysqli, etc..)
     public $myvar1;
     public $myvar2;

     public function __construct() {
         $this->__wakeup(); // We're calling our wakeup to handle starting our resource
     }

     public function __wakeup() {
         $this->resource = CodeToStartOurResourceUp();
     }

     public function __sleep() {
         // We make sure to leave out $resource here, so our session data remains persistent
         // Failure to do so will result in the failure during the unserialization of data
         // on the next request; thus, our SoapObject would not be persistent across requests.
         return array('myvar1','myvar2');
     }
 }

 try {
     session_start();
     $server = new SoapServer(null, array('uri' => $_SERVER['REQUEST_URI']));
     $server->setClass('MyFirstPersistentSoapServer');
     // setPersistence MUST be called after setClass, because setClass's
     // behavior sets SESSION_PERSISTENCE_REQUEST upon enacting the method.
     $server->setPersistence(SOAP_PERSISTENCE_SESSION);
     $server->handle();
 } catch(SoapFault $e) {
     error_log("SOAP ERROR: ". $e->getMessage());
 }
?>
```

### 参见

-   <span class="methodname">SoapServer::setClass</span>

SoapServer::SoapServer
======================

SoapServer constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapServer::SoapServer</span> ( <span
class="methodparam"><span class="type">mixed</span> `$wsdl`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

This constructor allows the creation of <span
class="classname">SoapServer</span> objects in WSDL or non-WSDL mode.

### 参数

`wsdl`  
To use the SoapServer in WSDL mode, pass the URI of a WSDL file.
Otherwise, pass **`null`** and set the *uri* option to the target
namespace for the server.

`options`  
Allow setting a default SOAP version (*soap\_version*), internal
character encoding (*encoding*), and actor URI (*actor*).

The *classmap* option can be used to map some WSDL types to PHP classes.
This option must be an array with WSDL types as keys and names of PHP
classes as values.

The *typemap* option is an array of type mappings. Type mapping is an
array with keys *type\_name*, *type\_ns* (namespace URI), *from\_xml*
(callback accepting one string parameter) and *to\_xml* (callback
accepting one object parameter).

The *cache\_wsdl* option is one of **`WSDL_CACHE_NONE`**,
**`WSDL_CACHE_DISK`**, **`WSDL_CACHE_MEMORY`** or **`WSDL_CACHE_BOTH`**.

There is also a *features* option which can be set to
**`SOAP_WAIT_ONE_WAY_CALLS`**, **`SOAP_SINGLE_ELEMENT_ARRAYS`**,
**`SOAP_USE_XSI_ARRAY_TYPE`**.

The *send\_errors* option can be set to **`false`** to sent a generic
error message ("Internal error") instead of the specific error message
sent otherwise.

### 范例

**示例 \#1 <span class="function">SoapServer::SoapServer</span>
example**

``` php
<?php

$server = new SoapServer("some.wsdl");

$server = new SoapServer("some.wsdl", array('soap_version' => SOAP_1_2));

$server = new SoapServer("some.wsdl", array('actor' => "http://example.org/ts-tests/C"));

$server = new SoapServer("some.wsdl", array('encoding'=>'ISO-8859-1'));

$server = new SoapServer(null, array('uri' => "http://test-uri/"));

class MyBook {
    public $title;
    public $author;
}

$server = new SoapServer("books.wsdl", array('classmap' => array('book' => "MyBook")));

?>
```

### 参见

-   <span class="methodname">SoapClient::SoapClient</span>

简介
----

Represents a SOAP fault.

类摘要
------

**SoapFault**

<span class="ooclass"> class **SoapFault** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type"><span
class="type">array</span><span class="type">string</span><span
class="type">null</span></span> `$code`</span> , <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$actor`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$details`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$name`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$headerFault`<span
class="initializer"> = **`null`**</span></span> \]\]\]\] )

<span class="methodname">SoapFault</span> ( <span
class="methodparam"><span class="type">string</span> `$faultcode`</span>
, <span class="methodparam"><span class="type">string</span>
`$faultstring`</span> \[, <span class="methodparam"><span
class="type">string</span> `$faultactor`</span> \[, <span
class="methodparam"><span class="type">string</span> `$detail`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$faultname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$headerfault`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

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
<span class="type">mixed</span> <span
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

}

SoapFault::\_\_construct
========================

SoapFault constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapFault::\_\_construct</span> ( <span
class="methodparam"><span class="type"><span
class="type">array</span><span class="type">string</span><span
class="type">null</span></span> `$code`</span> , <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$actor`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$details`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$name`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$headerFault`<span
class="initializer"> = **`null`**</span></span> \]\]\]\] )

此函数是该函数的别名： <span
class="methodname">SoapFault::SoapFault</span>

SoapFault::SoapFault
====================

SoapFault constructor

### 说明

<span class="methodname">SoapFault::SoapFault</span> ( <span
class="methodparam"><span class="type">string</span> `$faultcode`</span>
, <span class="methodparam"><span class="type">string</span>
`$faultstring`</span> \[, <span class="methodparam"><span
class="type">string</span> `$faultactor`</span> \[, <span
class="methodparam"><span class="type">string</span> `$detail`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$faultname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$headerfault`</span> \]\]\]\] )

This class is used to send SOAP fault responses from the PHP handler.
`faultcode`, `faultstring`, `faultactor` and `detail` are standard
elements of a SOAP Fault.

### 参数

`faultcode`  
The error code of the <span class="classname">SoapFault</span>.

`faultstring`  
The error message of the <span class="classname">SoapFault</span>.

`faultactor`  
A string identifying the actor that caused the error.

`detail`  
More details about the cause of the error.

`faultname`  
Can be used to select the proper fault encoding from WSDL.

`headerfault`  
Can be used during SOAP header handling to report an error in the
response header.

### 范例

**示例 \#1 Some examples**

``` php
<?php
function test($x)
{
    return new SoapFault("Server", "Some error message");
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

It is possible to use PHP exception mechanism to throw SOAP Fault.

**示例 \#2 Some examples**

``` php
<?php
function test($x)
{
    throw new SoapFault("Server", "Some error message");
}

$server = new SoapServer(null, array('uri' => "http://test-uri/"));
$server->addFunction("test");
$server->handle();
?>
```

### 参见

-   <span class="methodname">SoapServer::fault</span>
-   <span class="function">is\_soap\_fault</span>

SoapFault::\_\_toString
=======================

Obtain a string representation of a SoapFault

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SoapFault::\_\_toString</span> ( <span
class="methodparam">void</span> )

Returns a string representation of the SoapFault.

### 参数

此函数没有参数。

### 返回值

A string describing the SoapFault.

简介
----

Represents a SOAP header.

类摘要
------

**SoapHeader**

<span class="ooclass"> class **SoapHeader** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$mustunderstand`</span> \[, <span class="methodparam"><span
class="type">string</span> `$actor`</span> \]\]\] )

<span class="methodname">SoapHeader</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$mustunderstand`<span class="initializer"> = **`false`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$actor`</span> \]\]\] )

}

SoapHeader::\_\_construct
=========================

SoapHeader constructor

### 说明

<span class="methodname">SoapHeader::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$mustunderstand`</span> \[, <span class="methodparam"><span
class="type">string</span> `$actor`</span> \]\]\] )

此函数是该函数的别名： <span
class="methodname">SoapHeader::SoapHeader</span>

SoapHeader::SoapHeader
======================

SoapHeader constructor

### 说明

<span class="methodname">SoapHeader::SoapHeader</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$data`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$mustunderstand`<span class="initializer"> = **`false`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$actor`</span> \]\]\] )

Constructs a new SoapHeader object.

### 参数

`namespace`  
The namespace of the SOAP header element.

`name`  
The name of the SoapHeader object.

`data`  
A SOAP header's content. It can be a PHP value or a <span
class="classname">SoapVar</span> object.

`mustUnderstand`  
Value of the *mustUnderstand* attribute of the SOAP header element.

`actor`  
Value of the *actor* attribute of the SOAP header element.

### 范例

**示例 \#1 <span class="function">SoapHeader::SoapHeader</span>
example**

``` php
<?php
$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$client->__soapCall("echoVoid", null, null,
                new SoapHeader('http://soapinterop.org/echoheader/',
                               'echoMeStringRequest',
                               'hello world'));
?>
```

### 参见

-   <span class="methodname">SoapClient::\_\_soapCall</span>
-   <span class="methodname">SoapVar::SoapVar</span>
-   <span class="methodname">SoapParam::SoapParam</span>
-   <span class="methodname">SoapServer::addSoapHeader</span>

简介
----

Represents parameter to a SOAP call.

类摘要
------

**SoapParam**

<span class="ooclass"> class **SoapParam** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="methodname">SoapParam</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

}

SoapParam::\_\_construct
========================

SoapParam constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapParam::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

此函数是该函数的别名： <span
class="methodname">SoapParam::SoapParam</span>

SoapParam::SoapParam
====================

SoapParam constructor

### 说明

<span class="methodname">SoapParam::SoapParam</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Constructs a new <span class="classname">SoapParam</span> object.

### 参数

`data`  
The data to pass or return. This parameter can be passed directly as PHP
value, but in this case it will be named as *paramN* and the SOAP
service may not understand it.

`name`  
The parameter name.

### 范例

**示例 \#1 <span class="function">SoapParam::SoapParam</span> example**

``` php
<?php
$client = new SoapClient(null,array('location' => "http://localhost/soap.php",
                                    'uri'      => "http://test-uri/"));
$client->SomeFunction(new SoapParam($a, "a"),
                      new SoapParam($b, "b"),
                      new SoapParam($c, "c"));
?>
```

### 参见

-   <span class="methodname">SoapClient::\_\_soapCall</span>
-   <span class="methodname">SoapVar::SoapVar</span>

简介
----

A class representing a variable or object for use with SOAP services.

类摘要
------

**SoapVar**

<span class="ooclass"> class **SoapVar** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type"><span
class="type">int</span><span class="type">null</span></span>
`$encoding`</span> \[, <span class="methodparam"><span
class="type">string</span> `$typeName`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$typeNamespace`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$nodeName`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$nodeNamespace`<span class="initializer"> =
""</span></span> \]\]\]\] )

<span class="methodname">SoapVar</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$encoding`</span> \[, <span class="methodparam"><span
class="type">string</span> `$type_name`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$type_namespace`</span> \[, <span class="methodparam"><span
class="type">string</span> `$node_name`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$node_namespace`</span> \]\]\]\] )

}

SoapVar::\_\_construct
======================

SoapVar constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">SoapVar::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type"><span
class="type">int</span><span class="type">null</span></span>
`$encoding`</span> \[, <span class="methodparam"><span
class="type">string</span> `$typeName`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$typeNamespace`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$nodeName`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$nodeNamespace`<span class="initializer"> =
""</span></span> \]\]\]\] )

此函数是该函数的别名： <span class="methodname">SoapVar::SoapVar</span>

SoapVar::SoapVar
================

SoapVar constructor

### 说明

<span class="methodname">SoapVar::SoapVar</span> ( <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">string</span>
`$encoding`</span> \[, <span class="methodparam"><span
class="type">string</span> `$type_name`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$type_namespace`</span> \[, <span class="methodparam"><span
class="type">string</span> `$node_name`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$node_namespace`</span> \]\]\]\] )

Constructs a new <span class="classname">SoapVar</span> object.

### 参数

`data`  
The data to pass or return.

`encoding`  
The encoding ID, one of the *XSD\_...* constants.

`type_name`  
The type name.

`type_namespace`  
The type namespace.

`node_name`  
The XML node name.

`node_namespace`  
The XML node namespace.

### 范例

**示例 \#1 <span class="function">SoapVar::SoapVar</span> example**

``` php
<?php
class SOAPStruct {
    function SOAPStruct($s, $i, $f) 
    {
        $this->varString = $s;
        $this->varInt = $i;
        $this->varFloat = $f;
    }
}
$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));
$struct = new SOAPStruct('arg', 34, 325.325);
$soapstruct = new SoapVar($struct, SOAP_ENC_OBJECT, "SOAPStruct", "http://soapinterop.org/xsd");
$client->echoStruct(new SoapParam($soapstruct, "inputStruct"));
?>
```

### 参见

-   <span class="methodname">SoapClient::\_\_soapCall</span>
-   <span class="methodname">SoapParam::SoapParam</span>
