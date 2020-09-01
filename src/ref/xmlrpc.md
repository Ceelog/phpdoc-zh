xmlrpc\_decode\_request
=======================

将 XML 译码为 PHP 本身的类型

### 说明

<span class="type">mixed</span> <span
class="methodname">xmlrpc\_decode\_request</span> ( <span
class="methodparam"><span class="type">string</span> `$xml`</span> ,
<span class="methodparam"><span class="type">string</span>
`&$method`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_decode
==============

将 XML 译码为 PHP 本身的类型

### 说明

<span class="type">mixed</span> <span
class="methodname">xmlrpc\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$xml`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> = "iso-8859-1"</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`xml`  
XML response returned by XMLRPC method.

`encoding`  
Input encoding supported by iconv.

### 返回值

Returns either an array, or an integer, or a string, or a boolean
according to the response returned by the XMLRPC method.

### 范例

See example by <span class="function">xmlrpc\_encode\_request</span>.

### 参见

-   <span class="function">xmlrpc\_encode\_request</span>
-   <span class="function">xmlrpc\_is\_fault</span>

xmlrpc\_encode\_request
=======================

为 PHP 的值生成 XML

### 说明

<span class="type">string</span> <span
class="methodname">xmlrpc\_encode\_request</span> ( <span
class="methodparam"><span class="type">string</span> `$method`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$params`</span> \[, <span class="methodparam"><span
class="type">array</span> `$output_options`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`method`  
Name of the method to call.

`params`  
Method parameters compatible with method signature.

`output_options`  
Array specifying output options may contain (default values are
emphasised):

-   output\_type: php, *xml*

-   verbosity: no\_white\_space, newlines\_only, *pretty*

-   escaping: cdata, *non-ascii, non-print, markup* (may be a string
    with one value or an array with multiple values)

-   version: simple, *xmlrpc*, soap 1.1, auto

-   encoding: *iso-8859-1*, other character set supported by iconv

### 返回值

Returns a string containing the XML representation of the request.

### 范例

**示例 \#1 XMLRPC client functions example**

``` php
<?php
$request = xmlrpc_encode_request("method", array(1, 2, 3));
$context = stream_context_create(array('http' => array(
    'method' => "POST",
    'header' => "Content-Type: text/xml",
    'content' => $request
)));
$file = file_get_contents("http://www.example.com/xmlrpc", false, $context);
$response = xmlrpc_decode($file);
if ($response && xmlrpc_is_fault($response)) {
    trigger_error("xmlrpc: $response[faultString] ($response[faultCode])");
} else {
    print_r($response);
}
?>
```

### 参见

-   <span class="function">stream\_context\_create</span>
-   <span class="function">file\_get\_contents</span>
-   <span class="function">xmlrpc\_decode</span>

xmlrpc\_encode
==============

为 PHP 的值生成 XML

### 说明

<span class="type">string</span> <span
class="methodname">xmlrpc\_encode</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_get\_type
=================

为 PHP 的值获取 xmlrpc 的类型

### 说明

<span class="type">string</span> <span
class="methodname">xmlrpc\_get\_type</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

该函数对于 base64 与日期时间字符串特别有用。

### 参数

`value`  
PHP value

### 返回值

Returns the XML-RPC type.

### 范例

**示例 \#1 XML-RPC type example**

``` php
<?php
echo xmlrpc_get_type(null) . "\n"; // base64
echo xmlrpc_get_type(false) . "\n"; // boolean
echo xmlrpc_get_type(1) . "\n"; // int
echo xmlrpc_get_type(1.0) . "\n"; // double
echo xmlrpc_get_type("") . "\n"; // string
echo xmlrpc_get_type(array()) . "\n"; // array
echo xmlrpc_get_type(new stdClass) . "\n"; // array
echo xmlrpc_get_type(STDIN) . "\n"; // int
?>
```

### 参见

-   <span class="function">xmlrpc\_set\_type</span>

xmlrpc\_is\_fault
=================

Determines if an array value represents an XMLRPC fault

### 说明

<span class="type">bool</span> <span
class="methodname">xmlrpc\_is\_fault</span> ( <span
class="methodparam"><span class="type">array</span> `$arg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`arg`  
Array returned by <span class="function">xmlrpc\_decode</span>.

### 返回值

Returns **`TRUE`** if the argument means fault, **`FALSE`** otherwise.
Fault description is available in *$arg\["faultString"\]*, fault code is
in *$arg\["faultCode"\]*.

### 范例

See example by <span class="function">xmlrpc\_encode\_request</span>.

### 参见

-   <span class="function">xmlrpc\_decode</span>

xmlrpc\_parse\_method\_descriptions
===================================

将 XML 译码成方法描述的列表

### 说明

<span class="type">array</span> <span
class="methodname">xmlrpc\_parse\_method\_descriptions</span> ( <span
class="methodparam"><span class="type">string</span> `$xml`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_server\_add\_introspection\_data
========================================

添加自我描述的文档

### 说明

<span class="type">int</span> <span
class="methodname">xmlrpc\_server\_add\_introspection\_data</span> (
<span class="methodparam"><span class="type">resource</span>
`$server`</span> , <span class="methodparam"><span
class="type">array</span> `$desc`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_server\_call\_method
============================

解析 XML 请求同时调用方法

### 说明

<span class="type">string</span> <span
class="methodname">xmlrpc\_server\_call\_method</span> ( <span
class="methodparam"><span class="type">resource</span> `$server`</span>
, <span class="methodparam"><span class="type">string</span>
`$xml`</span> , <span class="methodparam"><span
class="type">mixed</span> `$user_data`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$output_options`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_server\_create
======================

创建一个 xmlrpc 服务端

### 说明

<span class="type">resource</span> <span
class="methodname">xmlrpc\_server\_create</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_server\_destroy
=======================

销毁服务端资源

### 说明

<span class="type">int</span> <span
class="methodname">xmlrpc\_server\_destroy</span> ( <span
class="methodparam"><span class="type">resource</span> `$server`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_server\_register\_introspection\_callback
=================================================

注册一个 PHP 函数用于生成文档

### 说明

<span class="type">bool</span> <span
class="methodname">xmlrpc\_server\_register\_introspection\_callback</span>
( <span class="methodparam"><span class="type">resource</span>
`$server`</span> , <span class="methodparam"><span
class="type">string</span> `$function`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_server\_register\_method
================================

注册一个 PHP 函数用于匹配 xmlrpc 方法名

### 说明

<span class="type">bool</span> <span
class="methodname">xmlrpc\_server\_register\_method</span> ( <span
class="methodparam"><span class="type">resource</span> `$server`</span>
, <span class="methodparam"><span class="type">string</span>
`$method_name`</span> , <span class="methodparam"><span
class="type">string</span> `$function`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

xmlrpc\_set\_type
=================

为一个 PHP 字符串值设置 xmlrpc 的类型、base64 或日期时间

### 说明

<span class="type">bool</span> <span
class="methodname">xmlrpc\_set\_type</span> ( <span
class="methodparam"><span class="type">string</span> `&$value`</span> ,
<span class="methodparam"><span class="type">string</span>
`$type`</span> )

为一个 PHP 字符串值设置 xmlrpc 的类型、base64 或日期时间

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`value`  
Value to set the type

`type`  
'base64' or 'datetime'

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If successful,
`value` is converted to an object.

### 范例

**示例 \#1 A <span class="function">xmlrpc\_set\_type</span> example**

``` php
<?php

$params = date("Ymd\TH:i:s", time());
xmlrpc_set_type($params, 'datetime');
echo xmlrpc_encode($params);

?>
```

以上例程的输出类似于：

    <?xml version="1.0" encoding="utf-8"?>
    <params>
    <param>
     <value>
      <dateTime.iso8601>20090322T23:43:03</dateTime.iso8601>
     </value>
    </param>
    </params>

### 错误／异常

Issues E\_WARNING with type unsupported by XMLRPC.

**目录**

-   [xmlrpc\_decode\_request](/ref/xmlrpc.html#xmlrpc_decode_request) —
    将 XML 译码为 PHP 本身的类型
-   [xmlrpc\_decode](/ref/xmlrpc.html#xmlrpc_decode) — 将 XML 译码为 PHP
    本身的类型
-   [xmlrpc\_encode\_request](/ref/xmlrpc.html#xmlrpc_encode_request) —
    为 PHP 的值生成 XML
-   [xmlrpc\_encode](/ref/xmlrpc.html#xmlrpc_encode) — 为 PHP 的值生成
    XML
-   [xmlrpc\_get\_type](/ref/xmlrpc.html#xmlrpc_get_type) — 为 PHP
    的值获取 xmlrpc 的类型
-   [xmlrpc\_is\_fault](/ref/xmlrpc.html#xmlrpc_is_fault) — Determines
    if an array value represents an XMLRPC fault
-   [xmlrpc\_parse\_method\_descriptions](/ref/xmlrpc.html#xmlrpc_parse_method_descriptions)
    — 将 XML 译码成方法描述的列表
-   [xmlrpc\_server\_add\_introspection\_data](/ref/xmlrpc.html#xmlrpc_server_add_introspection_data)
    — 添加自我描述的文档
-   [xmlrpc\_server\_call\_method](/ref/xmlrpc.html#xmlrpc_server_call_method)
    — 解析 XML 请求同时调用方法
-   [xmlrpc\_server\_create](/ref/xmlrpc.html#xmlrpc_server_create) —
    创建一个 xmlrpc 服务端
-   [xmlrpc\_server\_destroy](/ref/xmlrpc.html#xmlrpc_server_destroy) —
    销毁服务端资源
-   [xmlrpc\_server\_register\_introspection\_callback](/ref/xmlrpc.html#xmlrpc_server_register_introspection_callback)
    — 注册一个 PHP 函数用于生成文档
-   [xmlrpc\_server\_register\_method](/ref/xmlrpc.html#xmlrpc_server_register_method)
    — 注册一个 PHP 函数用于匹配 xmlrpc 方法名
-   [xmlrpc\_set\_type](/ref/xmlrpc.html#xmlrpc_set_type) — 为一个 PHP
    字符串值设置 xmlrpc 的类型、base64 或日期时间
