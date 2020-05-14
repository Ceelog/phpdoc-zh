SimpleXML
=========

**目录**

-   [简介](/intro/simplexml.html)
-   [安装／配置](/simplexml/setup.html)
    -   [需求](/simplexml/setup.html#需求)
    -   [安装](/simplexml/setup.html#安装)
    -   [运行时配置](/simplexml/setup.html#运行时配置)
    -   [资源类型](/simplexml/setup.html#资源类型)
-   [预定义常量](/simplexml/constants.html)
-   [范例](/simplexml/examples.html)
    -   [Basic SimpleXML
        usage](/simplexml/examples.html#Basic%20SimpleXML%20usage)
    -   [Dealing with XML
        errors](/simplexml/examples.html#Dealing%20with%20XML%20errors)
-   [SimpleXMLElement](/class/simplexmlelement.html) — The
    SimpleXMLElement class
    -   [SimpleXMLElement::addAttribute](/class/simplexmlelement.html#SimpleXMLElement::addAttribute)
        — Adds an attribute to the SimpleXML element
    -   [SimpleXMLElement::addChild](/class/simplexmlelement.html#SimpleXMLElement::addChild)
        — Adds a child element to the XML node
    -   [SimpleXMLElement::asXML](/class/simplexmlelement.html#SimpleXMLElement::asXML)
        — Return a well-formed XML string based on SimpleXML element
    -   [SimpleXMLElement::attributes](/class/simplexmlelement.html#SimpleXMLElement::attributes)
        — Identifies an element's attributes
    -   [SimpleXMLElement::children](/class/simplexmlelement.html#SimpleXMLElement::children)
        — Finds children of given node
    -   [SimpleXMLElement::\_\_construct](/class/simplexmlelement.html#SimpleXMLElement::__construct)
        — Creates a new SimpleXMLElement object
    -   [SimpleXMLElement::count](/class/simplexmlelement.html#SimpleXMLElement::count)
        — Counts the children of an element
    -   [SimpleXMLElement::getDocNamespaces](/class/simplexmlelement.html#SimpleXMLElement::getDocNamespaces)
        — Returns namespaces declared in document
    -   [SimpleXMLElement::getName](/class/simplexmlelement.html#SimpleXMLElement::getName)
        — Gets the name of the XML element
    -   [SimpleXMLElement::getNamespaces](/class/simplexmlelement.html#SimpleXMLElement::getNamespaces)
        — Returns namespaces used in document
    -   [SimpleXMLElement::registerXPathNamespace](/class/simplexmlelement.html#SimpleXMLElement::registerXPathNamespace)
        — Creates a prefix/ns context for the next XPath query
    -   [SimpleXMLElement::saveXML](/class/simplexmlelement.html#SimpleXMLElement::saveXML)
        — 别名 SimpleXMLElement::asXML
    -   [SimpleXMLElement::\_\_toString](/class/simplexmlelement.html#SimpleXMLElement::__toString)
        — Returns the string content
    -   [SimpleXMLElement::xpath](/class/simplexmlelement.html#SimpleXMLElement::xpath)
        — Runs XPath query on XML data
-   [SimpleXMLIterator](/class/simplexmliterator.html) — The
    SimpleXMLIterator class
    -   [SimpleXMLIterator::current](/class/simplexmliterator.html#SimpleXMLIterator::current)
        — Returns the current element
    -   [SimpleXMLIterator::getChildren](/class/simplexmliterator.html#SimpleXMLIterator::getChildren)
        — Returns the sub-elements of the current element
    -   [SimpleXMLIterator::hasChildren](/class/simplexmliterator.html#SimpleXMLIterator::hasChildren)
        — Checks whether the current element has sub elements
    -   [SimpleXMLIterator::key](/class/simplexmliterator.html#SimpleXMLIterator::key)
        — Return current key
    -   [SimpleXMLIterator::next](/class/simplexmliterator.html#SimpleXMLIterator::next)
        — Move to next element
    -   [SimpleXMLIterator::rewind](/class/simplexmliterator.html#SimpleXMLIterator::rewind)
        — Rewind to the first element
    -   [SimpleXMLIterator::valid](/class/simplexmliterator.html#SimpleXMLIterator::valid)
        — Check whether the current element is valid
-   [SimpleXML 函数](/ref/simplexml.html)
    -   [simplexml\_import\_dom](/ref/simplexml.html#simplexml_import_dom)
        — Get a SimpleXMLElement object from a DOM node
    -   [simplexml\_load\_file](/ref/simplexml.html#simplexml_load_file)
        — Interprets an XML file into an object
    -   [simplexml\_load\_string](/ref/simplexml.html#simplexml_load_string)
        — Interprets a string of XML into an object

简介
----

Represents an element in an XML document.

类摘要
------

**SimpleXMLElement**

<span class="ooclass"> class **SimpleXMLElement** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$data_is_url`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$ns`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_prefix`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespace`</span> \]\] )

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">addChild</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$namespace`</span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">asXML</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">attributes</span> (\[ <span class="methodparam"><span
class="type">string</span> `$ns`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_prefix`<span class="initializer"> =
**`FALSE`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">children</span> (\[ <span class="methodparam"><span
class="type">string</span> `$ns`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_prefix`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDocNamespaces</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$recursive`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$from_root`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getNamespaces</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$recursive`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">registerXPathNamespace</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> ,
<span class="methodparam"><span class="type">string</span> `$ns`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">xpath</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> )

}

SimpleXMLElement::addAttribute
==============================

Adds an attribute to the SimpleXML element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SimpleXMLElement::addAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespace`</span> \]\] )

Adds an attribute to the SimpleXML element.

### 参数

`name`  
The name of the attribute to add.

`value`  
The value of the attribute.

`namespace`  
If specified, the namespace to which the attribute belongs.

### 返回值

没有返回值。

### 范例

> **Note**:
>
> Listed examples may include *example.php*, which refers to the XML
> string found in the first example of the
> <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="link">basic usage</a>
> guide.

**示例 \#1 Add attributes and children to a SimpleXML element**

``` php
<?php

include 'example.php';
 
$sxe = new SimpleXMLElement($xmlstr);
$sxe->addAttribute('type', 'documentary');

$movie = $sxe->addChild('movie');
$movie->addChild('title', 'PHP2: More Parser Stories');
$movie->addChild('plot', 'This is all about the people who make it work.');

$characters = $movie->addChild('characters');
$character  = $characters->addChild('character');
$character->addChild('name', 'Mr. Parser');
$character->addChild('actor', 'John Doe');

$rating = $movie->addChild('rating', '5');
$rating->addAttribute('type', 'stars');
 
echo $sxe->asXML();

?>
```

以上例程的输出类似于：

    <?xml version="1.0" standalone="yes"?>
    <movies type="documentary">
     <movie>
      <title>PHP: Behind the Parser</title>
      <characters>
       <character>
        <name>Ms. Coder</name>
        <actor>Onlivia Actora</actor>
       </character>
       <character>
        <name>Mr. Coder</name>
        <actor>El Act&#xD3;r</actor>
       </character>
      </characters>
      <plot>
       So, this language. It's like, a programming language. Or is it a
       scripting language? All is revealed in this thrilling horror spoof
       of a documentary.
      </plot>
      <great-lines>
       <line>PHP solves all my web problems</line>
      </great-lines>
      <rating type="thumbs">7</rating>
      <rating type="stars">5</rating>
     </movie>
     <movie>
      <title>PHP2: More Parser Stories</title>
      <plot>This is all about the people who make it work.</plot>
      <characters>
       <character>
        <name>Mr. Parser</name>
        <actor>John Doe</actor>
       </character>
      </characters>
      <rating type="stars">5</rating>
     </movie>
    </movies>

### 参见

-   <span class="methodname">SimpleXMLElement::addChild</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

SimpleXMLElement::addChild
==========================

Adds a child element to the XML node

### 说明

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">SimpleXMLElement::addChild</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespace`</span> \]\] )

Adds a child element to the node and returns a SimpleXMLElement of the
child.

### 参数

`name`  
The name of the child element to add.

`value`  
If specified, the value of the child element.

`namespace`  
If specified, the namespace to which the child element belongs.

### 返回值

The *addChild* method returns a <span
class="type">SimpleXMLElement</span> object representing the child added
to the XML node.

### 范例

> **Note**:
>
> Listed examples may include *example.php*, which refers to the XML
> string found in the first example of the
> <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="link">basic usage</a>
> guide.

**示例 \#1 Add attributes and children to a SimpleXML element**

``` php
<?php

include 'example.php';

$sxe = new SimpleXMLElement($xmlstr);
$sxe->addAttribute('type', 'documentary');

$movie = $sxe->addChild('movie');
$movie->addChild('title', 'PHP2: More Parser Stories');
$movie->addChild('plot', 'This is all about the people who make it work.');

$characters = $movie->addChild('characters');
$character  = $characters->addChild('character');
$character->addChild('name', 'Mr. Parser');
$character->addChild('actor', 'John Doe');

$rating = $movie->addChild('rating', '5');
$rating->addAttribute('type', 'stars');
 
echo $sxe->asXML();

?>
```

以上例程的输出类似于：

    <?xml version="1.0" standalone="yes"?>
    <movies type="documentary">
     <movie>
      <title>PHP: Behind the Parser</title>
      <characters>
       <character>
        <name>Ms. Coder</name>
        <actor>Onlivia Actora</actor>
       </character>
       <character>
        <name>Mr. Coder</name>
        <actor>El Act&#xD3;r</actor>
       </character>
      </characters>
      <plot>
       So, this language. It's like, a programming language. Or is it a
       scripting language? All is revealed in this thrilling horror spoof
       of a documentary.
      </plot>
      <great-lines>
       <line>PHP solves all my web problems</line>
      </great-lines>
      <rating type="thumbs">7</rating>
      <rating type="stars">5</rating>
     </movie>
     <movie>
      <title>PHP2: More Parser Stories</title>
      <plot>This is all about the people who make it work.</plot>
      <characters>
       <character>
        <name>Mr. Parser</name>
        <actor>John Doe</actor>
       </character>
      </characters>
      <rating type="stars">5</rating>
     </movie>
    </movies>

### 参见

-   <span class="methodname">SimpleXMLElement::addAttribute</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

SimpleXMLElement::asXML
=======================

Return a well-formed XML string based on SimpleXML element

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SimpleXMLElement::asXML</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

The *asXML* method formats the parent object's data in XML version 1.0.

### 参数

`filename`  
If specified, the function writes the data to the file rather than
returning it.

### 返回值

If the `filename` isn't specified, this function returns a <span
class="type">string</span> on success and **`FALSE`** on error. If the
parameter is specified, it returns **`TRUE`** if the file was written
successfully and **`FALSE`** otherwise.

### 范例

**示例 \#1 Get XML**

``` php
<?php
$string = <<<XML
<a>
 <b>
  <c>text</c>
  <c>stuff</c>
 </b>
 <d>
  <c>code</c>
 </d>
</a>
XML;

$xml = new SimpleXMLElement($string);

echo $xml->asXML();

?>
```

以上例程会输出：

    <?xml version="1.0"?>
    <a>
     <b>
      <c>text</c>
      <c>stuff</c>
     </b>
     <d>
      <c>code</c>
     </d>
    </a>

*asXML* also works on Xpath results:

**示例 \#2 Using asXML() on <span
class="methodname">SimpleXMLElement::xpath</span> results**

``` php
<?php
// Continued from example XML above.

/* Search for <a><b><c> */
$result = $xml->xpath('/a/b/c');

foreach ($result as $node) {
    echo $node->asXML();
}
?>
```

以上例程会输出：

    <c>text</c><c>stuff</c>

### 参见

-   <span class="methodname">SimpleXMLElement::\_\_toString</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

SimpleXMLElement::attributes
============================

Identifies an element's attributes

### 说明

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">SimpleXMLElement::attributes</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ns`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_prefix`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

This function provides the attributes and values defined within an xml
tag.

> **Note**: <span class="simpara">SimpleXML
> 建起了一个给大多数方法添加迭代属性的规则。不能通过使用 <span
> class="function">var\_dump</span>
> 或任何可检查对象的其它东西来查看。</span>

### 参数

`ns`  
An optional namespace for the retrieved attributes

`is_prefix`  
Default to **`FALSE`**

### 返回值

Returns a <span class="classname">SimpleXMLElement</span> object that
can be iterated over to loop through the attributes on the tag.

Returns **`NULL`** if called on a <span
class="classname">SimpleXMLElement</span> object that already represents
an attribute and not a tag.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 5.2.0 | The optional parameter `is_prefix` was added. |

### 范例

**示例 \#1 Interpret an XML string**

``` php
<?php
$string = <<<XML
<a>
 <foo name="one" game="lonely">1</foo>
</a>
XML;

$xml = simplexml_load_string($string);
foreach($xml->foo[0]->attributes() as $a => $b) {
    echo $a,'="',$b,"\"\n";
}
?>
```

以上例程会输出：

    name="one"
    game="lonely"

### 参见

-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

SimpleXMLElement::children
==========================

Finds children of given node

### 说明

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">SimpleXMLElement::children</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ns`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$is_prefix`<span class="initializer"> = **`FALSE`**</span></span> \]\]
)

This method finds the children of an element. The result follows normal
iteration rules.

> **Note**: <span class="simpara">SimpleXML
> 建起了一个给大多数方法添加迭代属性的规则。不能通过使用 <span
> class="function">var\_dump</span>
> 或任何可检查对象的其它东西来查看。</span>

### 参数

`ns`  
An XML namespace.

`is_prefix`  
If `is_prefix` is **`TRUE`**, `ns` will be regarded as a prefix. If
**`FALSE`**, `ns` will be regarded as a namespace URL.

### 返回值

Returns a <span class="classname">SimpleXMLElement</span> element,
whether the node has children or not.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 5.2.0 | The optional parameter `is_prefix` was added. |

### 范例

**示例 \#1 Traversing a *children()* pseudo-array**

``` php
<?php
$xml = new SimpleXMLElement(
'<person>
 <child role="son">
  <child role="daughter"/>
 </child>
 <child role="daughter">
  <child role="son">
   <child role="son"/>
  </child>
 </child>
</person>');

foreach ($xml->children() as $second_gen) {
    echo ' The person begot a ' . $second_gen['role'];

    foreach ($second_gen->children() as $third_gen) {
        echo ' who begot a ' . $third_gen['role'] . ';';

        foreach ($third_gen->children() as $fourth_gen) {
            echo ' and that ' . $third_gen['role'] .
                ' begot a ' . $fourth_gen['role'];
        }
    }
}
?>
```

以上例程会输出：

    The person begot a son who begot a daughter; The person
    begot a daughter who begot a son; and that son begot a son

**示例 \#2 Using namespaces**

``` php
<?php
$xml = '<example xmlns:foo="my.foo.urn">
  <foo:a>Apple</foo:a>
  <foo:b>Banana</foo:b>
  <c>Cherry</c>
</example>';

$sxe = new SimpleXMLElement($xml);

$kids = $sxe->children('foo');
var_dump(count($kids));

$kids = $sxe->children('foo', TRUE);
var_dump(count($kids));

$kids = $sxe->children('my.foo.urn');
var_dump(count($kids));

$kids = $sxe->children('my.foo.urn', TRUE);
var_dump(count($kids));

$kids = $sxe->children();
var_dump(count($kids));
?>
```

    int(0)
    int(2)
    int(2)
    int(0)
    int(1)

### 注释

<span class="methodname">SimpleXMLElement::children</span> returns a
node object no matter if the current node has children or not. Use <span
class="function">count</span> on the return value to see if there are
any children. As of PHP 5.3.0, <span
class="methodname">SimpleXMLElement::count</span> may be used instead.

### 参见

-   <span class="methodname">SimpleXMLElement::count</span>
-   <span class="function">count</span>

SimpleXMLElement::\_\_construct
===============================

Creates a new SimpleXMLElement object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">SimpleXMLElement::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$data_is_url`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$ns`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_prefix`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\]\] )

Creates a new <span class="classname">SimpleXMLElement</span> object.

### 参数

`data`  
A well-formed XML string or the path or URL to an XML document if
`data_is_url` is **`TRUE`**.

`options`  
Optionally used to specify
<a href="/libxml/constants.html" class="link">additional Libxml parameters</a>,
which affect reading of XML documents. Options which affect the output
of XML documents (e.g. **`LIBXML_NOEMPTYTAG`**) are silently ignored.

> **Note**:
>
> It may be necessary to pass **`LIBXML_PARSEHUGE`** to be able to
> process deeply nested XML or very large text nodes.

`data_is_url`  
By default, `data_is_url` is **`FALSE`**. Use **`TRUE`** to specify that
`data` is a path or URL to an XML document instead of <span
class="type">string</span> data.

`ns`  
Namespace prefix or URI.

`is_prefix`  
**`TRUE`** if `ns` is a prefix, **`FALSE`** if it's a URI; defaults to
**`FALSE`**.

### 返回值

Returns a <span class="type">SimpleXMLElement</span> object representing
`data`.

### 错误／异常

Produces an **`E_WARNING`** error message for each error found in the
XML data and additionally throws an <span
class="classname">Exception</span> if the XML data could not be parsed.

**小贴士**

Use <span class="function">libxml\_use\_internal\_errors</span> to
suppress all XML errors, and <span
class="function">libxml\_get\_errors</span> to iterate over them
afterwards.

### 更新日志

| 版本  | 说明                                              |
|-------|---------------------------------------------------|
| 5.2.0 | Added the `ns` and `is_prefix` parameters.        |
| 5.1.2 | Added the `options` and `data_is_url` parameters. |

### 范例

> **Note**:
>
> Listed examples may include *example.php*, which refers to the XML
> string found in the first example of the
> <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="link">basic usage</a>
> guide.

**示例 \#1 Create a SimpleXMLElement object**

``` php
<?php

include 'example.php';

$sxe = new SimpleXMLElement($xmlstr);
echo $sxe->movie[0]->title;

?>
```

以上例程会输出：

    PHP: Behind the Parser

**示例 \#2 Create a SimpleXMLElement object from a URL**

``` php
<?php

$sxe = new SimpleXMLElement('http://example.org/document.xml', NULL, TRUE);
echo $sxe->asXML();

?>
```

### 参见

-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>
-   <span class="function">simplexml\_load\_string</span>
-   <span class="function">simplexml\_load\_file</span>
-   <a href="/simplexml/examples.html#Dealing%20with%20XML%20errors" class="xref"></a>
-   <span class="function">libxml\_use\_internal\_errors</span>

SimpleXMLElement::count
=======================

Counts the children of an element

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SimpleXMLElement::count</span> ( <span
class="methodparam">void</span> )

This method counts the number of children of an element.

### 返回值

Returns the number of elements of an element.

### 范例

**示例 \#1 Counting the number of children**

``` php
<?php
$xml = <<<EOF
<people>
 <person name="Person 1">
  <child/>
  <child/>
  <child/>
 </person>
 <person name="Person 2">
  <child/>
  <child/>
  <child/>
  <child/>
  <child/>
 </person>
</people>
EOF;

$elem = new SimpleXMLElement($xml);

foreach ($elem as $person) {
    printf("%s has got %d children.\n", $person['name'], $person->count());
}
?>
```

以上例程会输出：

    Person 1 has got 3 children.
    Person 2 has got 5 children.

### 参见

-   <span class="methodname">SimpleXMLElement::children</span>

SimpleXMLElement::getDocNamespaces
==================================

Returns namespaces declared in document

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SimpleXMLElement::getDocNamespaces</span> (\[
<span class="methodparam"><span class="type">bool</span>
`$recursive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$from_root`<span class="initializer"> = **`TRUE`**</span></span> \]\] )

Returns namespaces declared in document

### 参数

`recursive`  
If specified, returns all namespaces declared in parent and child nodes.
Otherwise, returns only namespaces declared in root node.

`from_root`  
Allows you to recursively check namespaces under a child node instead of
from the root of the XML doc.

### 返回值

The *getDocNamespaces* method returns an <span class="type">array</span>
of namespace names with their associated URIs.

### 范例

**示例 \#1 Get document namespaces**

``` php
<?php

$xml = <<<XML
<?xml version="1.0" standalone="yes"?>
<people xmlns:p="http://example.org/ns">
    <p:person id="1">John Doe</p:person>
    <p:person id="2">Susie Q. Public</p:person>
</people>
XML;
 
$sxe = new SimpleXMLElement($xml);

$namespaces = $sxe->getDocNamespaces();
var_dump($namespaces);

?>
```

以上例程会输出：

    array(1) {
       ["p"]=>
       string(21) "http://example.org/ns"
    }

**示例 \#2 Working with multiple namespaces**

``` php
<?php

$xml = <<<XML
<?xml version="1.0" standalone="yes"?>
<people xmlns:p="http://example.org/ns" xmlns:t="http://example.org/test">
    <p:person t:id="1">John Doe</p:person>
    <p:person t:id="2" a:addr="123 Street" xmlns:a="http://example.org/addr">
        Susie Q. Public
    </p:person>
</people>
XML;
 
$sxe = new SimpleXMLElement($xml);

$namespaces = $sxe->getDocNamespaces(TRUE);
var_dump($namespaces);

?>
```

以上例程会输出：

    array(3) {
      ["p"]=>
      string(21) "http://example.org/ns"
      ["t"]=>
      string(23) "http://example.org/test"
      ["a"]=>
      string(23) "http://example.org/addr"
    }

### 更新日志

| 版本  | 说明                         |
|-------|------------------------------|
| 5.4.0 | Added `from_root` parameter. |

### 参见

-   <span class="methodname">SimpleXMLElement::getNamespaces</span>
-   <span
    class="methodname">SimpleXMLElement::registerXPathNamespace</span>

SimpleXMLElement::getName
=========================

Gets the name of the XML element

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SimpleXMLElement::getName</span> ( <span
class="methodparam">void</span> )

Gets the name of the XML element.

### 返回值

The *getName* method returns as a <span class="type">string</span> the
name of the XML tag referenced by the SimpleXMLElement object.

### 范例

> **Note**:
>
> Listed examples may include *example.php*, which refers to the XML
> string found in the first example of the
> <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="link">basic usage</a>
> guide.

**示例 \#1 Get XML element names**

``` php
<?php
include 'example.php';
$sxe = new SimpleXMLElement($xmlstr);

echo $sxe->getName() . "\n";

foreach ($sxe->children() as $child)
{
    echo $child->getName() . "\n";
}

?>
```

以上例程会输出：

    movies
    movie

SimpleXMLElement::getNamespaces
===============================

Returns namespaces used in document

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SimpleXMLElement::getNamespaces</span> (\[
<span class="methodparam"><span class="type">bool</span>
`$recursive`<span class="initializer"> = **`FALSE`**</span></span> \] )

Returns namespaces used in document

### 参数

`recursive`  
If specified, returns all namespaces used in parent and child nodes.
Otherwise, returns only namespaces used in root node.

### 返回值

The *getNamespaces* method returns an <span class="type">array</span> of
namespace names with their associated URIs.

### 范例

**示例 \#1 Get document namespaces in use**

``` php
<?php

$xml = <<<XML
<?xml version="1.0" standalone="yes"?>
<people xmlns:p="http://example.org/ns" xmlns:t="http://example.org/test">
    <p:person id="1">John Doe</p:person>
    <p:person id="2">Susie Q. Public</p:person>
</people>
XML;
 
$sxe = new SimpleXMLElement($xml);

$namespaces = $sxe->getNamespaces(true);
var_dump($namespaces);

?>
```

以上例程会输出：

    array(1) {
      ["p"]=>
      string(21) "http://example.org/ns"
    }

### 参见

-   <span class="methodname">SimpleXMLElement::getDocNamespaces</span>
-   <span
    class="methodname">SimpleXMLElement::registerXPathNamespace</span>

SimpleXMLElement::registerXPathNamespace
========================================

Creates a prefix/ns context for the next XPath query

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SimpleXMLElement::registerXPathNamespace</span>
( <span class="methodparam"><span class="type">string</span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$ns`</span> )

Creates a prefix/ns context for the next XPath query. In particular,
this is helpful if the provider of the given XML document alters the
namespace prefixes. *registerXPathNamespace* will create a prefix for
the associated namespace, allowing one to access nodes in that namespace
without the need to change code to allow for the new prefixes dictated
by the provider.

### 参数

`prefix`  
The namespace prefix to use in the XPath query for the namespace given
in `ns`.

`ns`  
The namespace to use for the XPath query. This must match a namespace in
use by the XML document or the XPath query using `prefix` will not
return any results.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Setting a namespace prefix to use in an XPath query**

``` php
<?php

$xml = <<<EOD
<book xmlns:chap="http://example.org/chapter-title">
    <title>My Book</title>
    <chapter id="1">
        <chap:title>Chapter 1</chap:title>
        <para>Donec velit. Nullam eget tellus vitae tortor gravida scelerisque. 
            In orci lorem, cursus imperdiet, ultricies non, hendrerit et, orci. 
            Nulla facilisi. Nullam velit nisl, laoreet id, condimentum ut, 
            ultricies id, mauris.</para>
    </chapter>
    <chapter id="2">
        <chap:title>Chapter 2</chap:title>
        <para>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Proin 
            gravida. Phasellus tincidunt massa vel urna. Proin adipiscing quam 
            vitae odio. Sed dictum. Ut tincidunt lorem ac lorem. Duis eros 
            tellus, pharetra id, faucibus eu, dapibus dictum, odio.</para>
    </chapter>
</book>
EOD;

$sxe = new SimpleXMLElement($xml);

$sxe->registerXPathNamespace('c', 'http://example.org/chapter-title');
$result = $sxe->xpath('//c:title');

foreach ($result as $title) {
  echo $title . "\n";
}

?>
```

以上例程会输出：

    Chapter 1
    Chapter 2

Notice how the XML document shown in the example sets a namespace with a
prefix of *chap*. Imagine that this document (or another one like it)
may have used a prefix of *c* in the past for the same namespace. Since
it has changed, the XPath query will no longer return the proper results
and the query will require modification. Using *registerXPathNamespace*
avoids future modification of the query even if the provider changes the
namespace prefix.

### 参见

-   <span class="methodname">SimpleXMLElement::xpath</span>
-   <span class="methodname">SimpleXMLElement::getDocNamespaces</span>
-   <span class="methodname">SimpleXMLElement::getNamespaces</span>

SimpleXMLElement::saveXML
=========================

别名 <span class="methodname">SimpleXMLElement::asXML</span>

### 说明

此方法是该方法的别名： <span
class="methodname">SimpleXMLElement::asXML</span>

SimpleXMLElement::\_\_toString
==============================

Returns the string content

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SimpleXMLElement::\_\_toString</span> ( <span
class="methodparam">void</span> )

Returns text content that is directly in this element. Does not return
text content that is inside this element's children.

### 参数

此函数没有参数。

### 返回值

Returns the string content on success or an empty string on failure.

### 范例

**示例 \#1 Get string content**

``` php
<?php
$xml = new SimpleXMLElement('<a>1 <b>2 </b>3</a>');
echo $xml;
?>
```

以上例程会输出：

    1 3

### 参见

-   <span class="methodname">SimpleXMLElement::asXML</span>

SimpleXMLElement::xpath
=======================

Runs XPath query on XML data

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SimpleXMLElement::xpath</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

The *xpath* method searches the SimpleXML node for children matching the
XPath `path`.

### 参数

`path`  
An XPath path

### 返回值

Returns an <span class="type">array</span> of SimpleXMLElement objects
or **`FALSE`** in case of an error.

### 范例

**示例 \#1 Xpath**

``` php
<?php
$string = <<<XML
<a>
 <b>
  <c>text</c>
  <c>stuff</c>
 </b>
 <d>
  <c>code</c>
 </d>
</a>
XML;

$xml = new SimpleXMLElement($string);

/* Search for <a><b><c> */
$result = $xml->xpath('/a/b/c');

while(list( , $node) = each($result)) {
    echo '/a/b/c: ',$node,"\n";
}

/* Relative paths also work... */
$result = $xml->xpath('b/c');

while(list( , $node) = each($result)) {
    echo 'b/c: ',$node,"\n";
}
?>
```

以上例程会输出：

    /a/b/c: text
    /a/b/c: stuff
    b/c: text
    b/c: stuff

Notice that the two results are equal.

### 参见

-   <span
    class="methodname">SimpleXMLElement::registerXPathNamespace</span>
-   <span class="methodname">SimpleXMLElement::getDocNamespaces</span>
-   <span class="methodname">SimpleXMLElement::getNamespaces</span>
-   <a href="/simplexml/examples.html#Basic%20SimpleXML%20usage" class="xref"></a>

简介
----

The SimpleXMLIterator provides recursive iteration over all nodes of a
<span class="classname">SimpleXMLElement</span> object.

类摘要
------

**SimpleXMLIterator**

<span class="ooclass"> class **SimpleXMLIterator** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**SimpleXMLElement** </span> <span class="oointerface">implements <span
class="interfacename">RecursiveIterator</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">SimpleXMLIterator</span> <span
class="methodname">getChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">SimpleXMLElement::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$data_is_url`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$ns`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_prefix`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SimpleXMLElement::addAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespace`</span> \]\] )

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">SimpleXMLElement::addChild</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespace`</span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SimpleXMLElement::asXML</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">SimpleXMLElement::attributes</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ns`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_prefix`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

<span class="modifier">public</span> <span
class="type">SimpleXMLElement</span> <span
class="methodname">SimpleXMLElement::children</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ns`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$is_prefix`<span class="initializer"> = **`FALSE`**</span></span> \]\]
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SimpleXMLElement::count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SimpleXMLElement::getDocNamespaces</span> (\[
<span class="methodparam"><span class="type">bool</span>
`$recursive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$from_root`<span class="initializer"> = **`TRUE`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SimpleXMLElement::getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SimpleXMLElement::getNamespaces</span> (\[
<span class="methodparam"><span class="type">bool</span>
`$recursive`<span class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SimpleXMLElement::registerXPathNamespace</span>
( <span class="methodparam"><span class="type">string</span>
`$prefix`</span> , <span class="methodparam"><span
class="type">string</span> `$ns`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SimpleXMLElement::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SimpleXMLElement::xpath</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

}

SimpleXMLIterator::current
==========================

Returns the current element

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SimpleXMLIterator::current</span> ( <span
class="methodparam">void</span> )

This method returns the current element as a <span
class="classname">SimpleXMLIterator</span> object or **`NULL`**.

### 参数

此函数没有参数。

### 返回值

Returns the current element as a <span
class="classname">SimpleXMLIterator</span> object or **`NULL`** on
failure.

### 范例

**示例 \#1 Return the current element**

``` php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>PHP basics</book><book>XML basics</book></books>');
var_dump($xmlIterator->current());

$xmlIterator->rewind(); // rewind to first element
var_dump($xmlIterator->current());
?>
```

以上例程会输出：

    NULL
    object(SimpleXMLIterator)#2 (1) {
      [0]=>
      string(10) "PHP basics"
    }

### 参见

-   <span class="methodname">SimpleXMLIterator::key</span>
-   <span class="methodname">SimpleXMLIterator::next</span>
-   <span class="methodname">SimpleXMLIterator::rewind</span>
-   <span class="methodname">SimpleXMLIterator::valid</span>
-   <span class="classname">SimpleXMLElement</span>

SimpleXMLIterator::getChildren
==============================

Returns the sub-elements of the current element

### 说明

<span class="modifier">public</span> <span
class="type">SimpleXMLIterator</span> <span
class="methodname">SimpleXMLIterator::getChildren</span> ( <span
class="methodparam">void</span> )

This method returns a <span class="classname">SimpleXMLIterator</span>
object containing sub-elements of the current <span
class="classname">SimpleXMLIterator</span> element.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="classname">SimpleXMLIterator</span> object
containing the sub-elements of the current element.

### 范例

**示例 \#1 Return the sub-elements of the current element**

``` php
<?php
$xml = <<<XML
<books>
    <book>
        <title>PHP Basics</title>
        <author>Jim Smith</author>
    </book>
    <book>XML basics</book>
</books>
XML;

$xmlIterator = new SimpleXMLIterator($xml);
for( $xmlIterator->rewind(); $xmlIterator->valid(); $xmlIterator->next() ) {
    foreach($xmlIterator->getChildren() as $name => $data) {
    echo "The $name is '$data' from the class " . get_class($data) . "\n";
    }
}
?>
```

以上例程会输出：

    The title is 'PHP Basics' from the class SimpleXMLIterator
    The author is 'Jim Smith' from the class SimpleXMLIterator

SimpleXMLIterator::hasChildren
==============================

Checks whether the current element has sub elements

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SimpleXMLIterator::hasChildren</span> ( <span
class="methodparam">void</span> )

This method checks whether the current <span
class="classname">SimpleXMLIterator</span> element has sub-elements.

### 参数

此函数没有参数。

### 返回值

**`TRUE`** if the current element has sub-elements, otherwise
**`FALSE`**

### 范例

**示例 \#1 Check whether the current element has sub-elements**

``` php
<?php
$xml = <<<XML
<books>
    <book>
        <title>PHP Basics</title>
        <author>Jim Smith</author>
    </book>
    <book>XML basics</book>
</books>
XML;

$xmlIterator = new SimpleXMLIterator( $xml );
for( $xmlIterator->rewind(); $xmlIterator->valid(); $xmlIterator->next() ) {
    if($xmlIterator->hasChildren()) {
        var_dump($xmlIterator->current());
    }
}
?>
```

以上例程会输出：

    object(SimpleXMLIterator)#2 (2) {
      ["title"]=>
      string(10) "PHP Basics"
      ["author"]=>
      string(9) "Jim Smith"
    }

SimpleXMLIterator::key
======================

Return current key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SimpleXMLIterator::key</span> ( <span
class="methodparam">void</span> )

This method gets the XML tag name of the current element.

### 参数

此函数没有参数。

### 返回值

Returns the XML tag name of the element referenced by the current <span
class="classname">SimpleXMLIterator</span> object or **`FALSE`**

### 范例

**示例 \#1 Get the current XML tag key**

``` php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>PHP basics</book><book>XML basics</book></books>');

echo var_dump($xmlIterator->key());
$xmlIterator->rewind(); // rewind to the first element
echo var_dump($xmlIterator->key());

?>
```

以上例程会输出：

    bool(false)
    string(4) "book"

SimpleXMLIterator::next
=======================

Move to next element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SimpleXMLIterator::next</span> ( <span
class="methodparam">void</span> )

This method moves the <span class="classname">SimpleXMLIterator</span>
to the next element.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 Move to the next element**

``` php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>PHP Basics</book><book>XML basics</book></books>');
$xmlIterator->rewind(); // rewind to the first element
$xmlIterator->next();

var_dump($xmlIterator->current());
?>
```

以上例程会输出：

    object(SimpleXMLIterator)#2 (1) {
      [0]=>
      string(10) "XML basics"
    }

SimpleXMLIterator::rewind
=========================

Rewind to the first element

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SimpleXMLIterator::rewind</span> ( <span
class="methodparam">void</span> )

This method rewinds the <span class="classname">SimpleXMLIterator</span>
to the first element.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 Rewind to the first element**

``` php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>PHP Basics</book><book>XML Basics</book></books>');
$xmlIterator->rewind();

var_dump($xmlIterator->current());
?>
```

以上例程会输出：

    object(SimpleXMLIterator)#2 (1) {
      [0]=>
      string(10) "PHP Basics"
    }

SimpleXMLIterator::valid
========================

Check whether the current element is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SimpleXMLIterator::valid</span> ( <span
class="methodparam">void</span> )

This method checks if the current element is valid after calls to <span
class="methodname">SimpleXMLIterator::rewind</span> or <span
class="methodname">SimpleXMLIterator::next</span>.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the current element is valid, otherwise
**`FALSE`**

### 范例

**示例 \#1 Check whether the current element is valid**

``` php
<?php
$xmlIterator = new SimpleXMLIterator('<books><book>SQL Basics</book></books>');

$xmlIterator->rewind(); // rewind to the first element
echo var_dump($xmlIterator->valid()); // bool(true)

$xmlIterator->next(); // advance to the next element
echo var_dump($xmlIterator->valid()); // bool(false) because there is only one element
?>
```
