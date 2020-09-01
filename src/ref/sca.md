预定义类
--------

Most of the interface to SCA is through the annotations within SCA
components so there are few public classes and methods. The only SCA
classes that scripts or components can call are the <span
class="classname">SCA</span> class itself, and the proxy classes <span
class="classname">SCA\_LocalProxy</span> and <span
class="classname">SCA\_SoapProxy</span>.

<span class="classname">SCA</span>
----------------------------------

Much of the work of the SCA class is performed when the file `SCA.php`
is included within an SCA component. However, a PHP script may include
`SCA.php` and call the <span class="function">getService</span> method
on the SCA class in order to obtain a proxy for a service. A component
will not need to do this as proxies are obtained instead by defining an
instance variable with the @reference annotation.

Components that need to create an SDO to return to a caller will need a
data factory to call. For this purpose the SCA class supports the <span
class="function">createDataObject</span> method, which will create an
SDO according to the model defined by the component's @types
annotations. The arguments to <span
class="function">createDataObject</span> are the same as those to SDO's
XML Data Access Service.

方法
----

-   <a href="/ref/sca.html#SCA::getService" class="link">getService</a> -
    obtain a proxy for a service

-   <a href="/ref/sca.html#SCA::createDataObject" class="link">createDataObject</a> -
    create an SDO

<span class="classname">SCA\_LocalProxy</span>
----------------------------------------------

When <span class="function">getService</span> is called with the target
of a local PHP component, a local proxy is returned. A local proxy is
also injected into the instance variables of a component that are
defined with an @reference and an @binding.php anotation. When the
script or component makes calls on the local proxy, they are passed on
to the target component itself.

Components that need to create an SDO to pass to a component will need a
data factory to call. For this purpose the SCA\_LocalProxy class
supports the <span class="function">createDataObject</span> method,
which will create an SDO according to the model defined by the
components' @types annotations. The arguments to the <span
class="function">createDataObject</span> are the same as those to SDO's
XML Data Access Service.

方法
----

-   <a href="/ref/sca.html#SCA_LocalProxy::createDataObject" class="link">createDataObject</a> -
    create an SDO

<span class="classname">SCA\_SoapProxy</span>
---------------------------------------------

When <span class="function">getService</span> is called with the target
of a WSDL file, a SOAP proxy is returned. A SOAP proxy is also injected
into the instance variables of a component that are defined with an
@reference and an @binding.soap anotations. When the script or component
makes calls on the SOAP proxy, they are formed into Web service SOAP
requests and passed on to the target component, with the help of the PHP
Soap extension.

Components that need to create an SDO to pass to a component will need a
data factory to call. For this purpose the <span
class="classname">SCA\_SoapProxy</span> class supports the <span
class="function">createDataObject</span> method, which will create an
SDO according to the model defined within the target WSDL. The arguments
to the <span class="function">createDataObject</span> are the same as
those to SDO's XML Data Access Service.

方法
----

-   <a href="/ref/sca.html#SCA_SoapProxy::createDataObject" class="link">createDataObject</a> -
    create an SDO

SCA::createDataObject
=====================

Create an SDO

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SCA::createDataObject</span> ( <span
class="methodparam"> <span class="type">string</span>
`$type_namespace_uri` </span> , <span class="methodparam"> <span
class="type">string</span> `$type_name` </span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

This method is used inside an SCA component that needs to create an SDO
to return. The parameters are the desired SDO's namespace URI and type
name. The namespace and type must be defined in one of the schema files
which are specified on the @types annotation within the component.

### 参数

`type_namespace_uri`  
The namespace of the type.

`type_name`  
The name of the type.

### 返回值

Returns the newly created SDO\_DataObject.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if the namespaceURI and typeName do not correspond to a type in
any of the schema files specified in the @types annotations.

SCA::getService
===============

Obtain a proxy for a service

### 说明

<span class="type">mixed</span> <span
class="methodname">SCA::getService</span> ( <span class="methodparam">
<span class="type">string</span> `$target` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$binding` </span>
\[, <span class="methodparam"> <span class="type">array</span> `$config`
</span> \]\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Examine the target and initialize and return a proxy of the appropriate
sort. If the target is for a local PHP component the returned proxy will
be an SCA\_LocalProxy. If the target is for a WSDL file, the returned
proxy will be a SCA\_SoapProxy.

### 参数

`target`  
An absolute or relative path to the target service or service
description (e.g. a URL to a json-rpc service description, a PHP
component, a WSDL file, and so on.). A relative path, if specified, is
resolved relative to the location of the script issuing the <span
class="function">getService</span> call, and not against the
include\_path or current working directory.

`binding`  
The binding (i.e. protocol) to use to communicate with the service (e.g
binding.jsonrpc for a json-rpc service). Note, some service types can be
deduced from the target parameter (e.g. if the target parameter ends in
.wsdl then SCA will assume binding.soap). Any binding which can be
specified in an annotation can be specified here. For example
'binding.soap' is equivalent to the '@binding.soap' annotation.

`config`  
Any additional configuration properties for the binding (e.g.
array('location' =\> 'http://example.org')). Any binding configuration
which can be specified in an annotation can be specified here. For
example, 'location' is equivalent to the '@location' annotation to
configure the location of a target soap service.

### 返回值

The SCA\_LocalProxy or SCA\_SoapProxy.

### 范例

**示例 \#1 An <span class="function">SCA::getService</span> example**

This example shows how to get a proxy to an email soap service described
by `EmailService.wsdl` and located at `http://example.org`.

``` php
<?php
include 'SCA/SCA.php';
$service = SCA::getService('EmailService.wsdl', 'binding.soap', array('location' => 'http://example.org'));
$service->send(...);
?>
```

以上例程会输出：

SCA\_LocalProxy::createDataObject
=================================

Create an SDO

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SCA\_LocalProxy::createDataObject</span> ( <span
class="methodparam"> <span class="type">string</span>
`$type_namespace_uri` </span> , <span class="methodparam"> <span
class="type">string</span> `$type_name` </span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

This method is used inside either an ordinary PHP script or an SCA
component that needs to create an SDO to pass to a local service. The
parameters are the desired SDO's namespace URI and type name. The
namespace and type must be defined in the interface of the component
that is to be called, so the namespace and type must be defined in one
of the schema files which are specified on the @types annotation within
the component for which the SCA\_LocalProxy object is a proxy.

### 参数

`type_namespace_uri`  
The namespace of the type.

`type_name`  
The name of the type.

### 返回值

Returns the newly created SDO\_DataObject.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if the namespaceURI and typeName do not correspond to a type in
any of the schema files specified in the @types annotations within the
component for which the SCA\_LocalProxy object is a proxy..

SCA\_SoapProxy::createDataObject
================================

Create an SDO

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SCA\_SoapProxy::createDataObject</span> ( <span
class="methodparam"> <span class="type">string</span>
`$type_namespace_uri` </span> , <span class="methodparam"> <span
class="type">string</span> `$type_name` </span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

This method is used inside either an ordinary PHP script or an SCA
component that needs to create an SDO to pass to a web service. The
parameters are the desired SDO's namespace URI and type name. The
namespace and type must be defined in the interface of the component
that is to be called, so the namespace and type must be defined within
the WSDL for the web service. If the web service is also an SCA
component then the types will have been defined within one of the schema
files which are specified on the @types annotation within the component
for which the SCA\_SoapProxy object is a proxy.

### 参数

`type_namespace_uri`  
The namespace of the type.

`type_name`  
The name of the type.

### 返回值

Returns the newly created SDO\_DataObject.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if the namespaceURI and typeName do not correspond to a type
found in the WSDL that was used to initialise this SCA\_SoapProxy.

**目录**

-   [SCA::createDataObject](/ref/sca.html#SCA::createDataObject) —
    Create an SDO
-   [SCA::getService](/ref/sca.html#SCA::getService) — Obtain a proxy
    for a service
-   [SCA\_LocalProxy::createDataObject](/ref/sca.html#SCA_LocalProxy::createDataObject)
    — Create an SDO
-   [SCA\_SoapProxy::createDataObject](/ref/sca.html#SCA_SoapProxy::createDataObject)
    — Create an SDO
