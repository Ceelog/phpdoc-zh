simplexml\_import\_dom
======================

Get a *SimpleXMLElement* object from a DOM node

### 说明

<span class="type"><span class="type">SimpleXMLElement</span><span
class="type">false</span></span> <span
class="methodname">simplexml\_import\_dom</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$class_name`<span class="initializer"> =
"SimpleXMLElement"</span></span> \] )

This function takes a node of a
<a href="/book/dom.html" class="link">DOM</a> document and makes it into
a SimpleXML node. This new object can then be used as a native SimpleXML
element.

### 参数

`node`  
A <a href="/book/dom.html" class="link">DOM</a> Element node

`class_name`  
You may use this optional parameter so that <span
class="function">simplexml\_import\_dom</span> will return an object of
the specified class. That class should extend the <span
class="type">SimpleXMLElement</span> class.

### 返回值

Returns a <span class="type">SimpleXMLElement</span> 或者在失败时返回
**`false`**.

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 Importing DOM**

``` php
<?php
$dom = new DOMDocument;
$dom->loadXML('<books><book><title>blah</title></book></books>');
if (!$dom) {
    echo 'Error while parsing the document';
    exit;
}

$s = simplexml_import_dom($dom);

echo $s->book[0]->title;
?>
```

以上例程会输出：

    blah

### 参见

-   <span class="function">dom\_import\_simplexml</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

simplexml\_load\_file
=====================

Interprets an XML file into an object

### 说明

<span class="type"><span class="type">SimpleXMLElement</span><span
class="type">false</span></span> <span
class="methodname">simplexml\_load\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$class_name`<span class="initializer"> =
"SimpleXMLElement"</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$ns`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_prefix`<span class="initializer"> =
**`false`**</span></span> \]\]\]\] )

Convert the well-formed XML document in the given file to an object.

### 参数

`filename`  
Path to the XML file

> **Note**:
>
> Libxml 2 unescapes the URI, so if you want to pass e.g. *b&c* as the
> URI parameter *a*, you have to call
> *simplexml\_load\_file(rawurlencode('http://example.com/?a=' .
> urlencode('b&c')))*. Since PHP 5.1.0 you don't need to do this because
> PHP will do it for you.

`class_name`  
You may use this optional parameter so that <span
class="function">simplexml\_load\_file</span> will return an object of
the specified class. That class should extend the <span
class="type">SimpleXMLElement</span> class.

`options`  
Since PHP 5.1.0 and Libxml 2.6.0, you may also use the `options`
parameter to specify
<a href="/libxml/constants.html" class="link">additional Libxml parameters</a>.

`ns`  
Namespace prefix or URI.

`is_prefix`  
**`true`** if `ns` is a prefix, **`false`** if it's a URI; defaults to
**`false`**.

### 返回值

Returns an <span class="type">object</span> of class <span
class="type">SimpleXMLElement</span> with properties containing the data
held within the XML document, 或者在失败时返回 **`false`**.

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 错误／异常

Produces an **`E_WARNING`** error message for each error found in the
XML data.

**小贴士**

Use <span class="function">libxml\_use\_internal\_errors</span> to
suppress all XML errors, and <span
class="function">libxml\_get\_errors</span> to iterate over them
afterwards.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 5.2.0 | The optional parameter `is_prefix` was added. |

### 范例

**示例 \#1 Interpret an XML document**

``` php
<?php
// The file test.xml contains an XML document with a root element
// and at least an element /[root]/title.

if (file_exists('test.xml')) {
    $xml = simplexml_load_file('test.xml');
 
    print_r($xml);
} else {
    exit('Failed to open test.xml.');
}
?>
```

This script will display, on success:

    SimpleXMLElement Object
    (
      [title] => Example Title
      ...
    )

At this point, you can go about using *$xml-\>title* and any other
elements.

### 参见

-   <span class="function">simplexml\_load\_string</span>
-   <span class="methodname">SimpleXMLElement::\_\_construct</span>
-   <a href="/simplexml/examples.html#Dealing%20with%20XML%20errors" class="xref"></a>
-   <span class="function">libxml\_use\_internal\_errors</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

simplexml\_load\_string
=======================

Interprets a string of XML into an object

### 说明

<span class="type"><span class="type">SimpleXMLElement</span><span
class="type">false</span></span> <span
class="methodname">simplexml\_load\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$class_name`<span class="initializer"> =
"SimpleXMLElement"</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$ns`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_prefix`<span class="initializer"> =
**`false`**</span></span> \]\]\]\] )

Takes a well-formed XML string and returns it as an object.

### 参数

`data`  
A well-formed XML string

`class_name`  
You may use this optional parameter so that <span
class="function">simplexml\_load\_string</span> will return an object of
the specified class. That class should extend the <span
class="type">SimpleXMLElement</span> class.

`options`  
Since PHP 5.1.0 and Libxml 2.6.0, you may also use the `options`
parameter to specify
<a href="/libxml/constants.html" class="link">additional Libxml parameters</a>.

`ns`  
Namespace prefix or URI.

`is_prefix`  
**`true`** if `ns` is a prefix, **`false`** if it's a URI; defaults to
**`false`**.

### 返回值

Returns an <span class="type">object</span> of class <span
class="type">SimpleXMLElement</span> with properties containing the data
held within the xml document, 或者在失败时返回 **`false`**.

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 错误／异常

Produces an **`E_WARNING`** error message for each error found in the
XML data.

**小贴士**

Use <span class="function">libxml\_use\_internal\_errors</span> to
suppress all XML errors, and <span
class="function">libxml\_get\_errors</span> to iterate over them
afterwards.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 5.2.0 | The optional parameter `is_prefix` was added. |

### 范例

**示例 \#1 Interpret an XML string**

``` php
<?php
$string = <<<XML
<?xml version='1.0'?> 
<document>
 <title>Forty What?</title>
 <from>Joe</from>
 <to>Jane</to>
 <body>
  I know that's the answer -- but what's the question?
 </body>
</document>
XML;

$xml = simplexml_load_string($string);

print_r($xml);
?>
```

以上例程会输出：

    SimpleXMLElement Object
    (
      [title] => Forty What?
      [from] => Joe
      [to] => Jane
      [body] =>
       I know that's the answer -- but what's the question?
    )

At this point, you can go about using *$xml-\>body* and such.

### 参见

-   <span class="function">simplexml\_load\_file</span>
-   <span class="methodname">SimpleXMLElement::\_\_construct</span>
-   <a href="/simplexml/examples.html#Dealing%20with%20XML%20errors" class="xref"></a>
-   <span class="function">libxml\_use\_internal\_errors</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

**目录**

-   [simplexml\_import\_dom](/ref/simplexml.html#simplexml_import_dom) —
    Get a SimpleXMLElement object from a DOM node
-   [simplexml\_load\_file](/ref/simplexml.html#simplexml_load_file) —
    Interprets an XML file into an object
-   [simplexml\_load\_string](/ref/simplexml.html#simplexml_load_string)
    — Interprets a string of XML into an object
