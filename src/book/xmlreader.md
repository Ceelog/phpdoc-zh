XMLReader
=========

**目录**

-   [简介](/intro/xmlreader.html)
-   [安装／配置](/xmlreader/setup.html)
    -   [需求](/xmlreader/setup.html#需求)
    -   [安装](/xmlreader/setup.html#安装)
    -   [运行时配置](/xmlreader/setup.html#运行时配置)
    -   [资源类型](/xmlreader/setup.html#资源类型)
-   [XMLReader](/class/xmlreader.html) — The XMLReader class
    -   [XMLReader::close](/class/xmlreader.html#XMLReader::close) —
        Close the XMLReader input
    -   [XMLReader::expand](/class/xmlreader.html#XMLReader::expand) —
        Returns a copy of the current node as a DOM object
    -   [XMLReader::getAttribute](/class/xmlreader.html#XMLReader::getAttribute)
        — Get the value of a named attribute
    -   [XMLReader::getAttributeNo](/class/xmlreader.html#XMLReader::getAttributeNo)
        — Get the value of an attribute by index
    -   [XMLReader::getAttributeNs](/class/xmlreader.html#XMLReader::getAttributeNs)
        — Get the value of an attribute by localname and URI
    -   [XMLReader::getParserProperty](/class/xmlreader.html#XMLReader::getParserProperty)
        — Indicates if specified property has been set
    -   [XMLReader::isValid](/class/xmlreader.html#XMLReader::isValid) —
        Indicates if the parsed document is valid
    -   [XMLReader::lookupNamespace](/class/xmlreader.html#XMLReader::lookupNamespace)
        — Lookup namespace for a prefix
    -   [XMLReader::moveToAttribute](/class/xmlreader.html#XMLReader::moveToAttribute)
        — Move cursor to a named attribute
    -   [XMLReader::moveToAttributeNo](/class/xmlreader.html#XMLReader::moveToAttributeNo)
        — Move cursor to an attribute by index
    -   [XMLReader::moveToAttributeNs](/class/xmlreader.html#XMLReader::moveToAttributeNs)
        — Move cursor to a named attribute
    -   [XMLReader::moveToElement](/class/xmlreader.html#XMLReader::moveToElement)
        — Position cursor on the parent Element of current Attribute
    -   [XMLReader::moveToFirstAttribute](/class/xmlreader.html#XMLReader::moveToFirstAttribute)
        — Position cursor on the first Attribute
    -   [XMLReader::moveToNextAttribute](/class/xmlreader.html#XMLReader::moveToNextAttribute)
        — Position cursor on the next Attribute
    -   [XMLReader::next](/class/xmlreader.html#XMLReader::next) — Move
        cursor to next node skipping all subtrees
    -   [XMLReader::open](/class/xmlreader.html#XMLReader::open) — Set
        the URI containing the XML to parse
    -   [XMLReader::read](/class/xmlreader.html#XMLReader::read) — Move
        to next node in document
    -   [XMLReader::readInnerXml](/class/xmlreader.html#XMLReader::readInnerXml)
        — Retrieve XML from current node
    -   [XMLReader::readOuterXml](/class/xmlreader.html#XMLReader::readOuterXml)
        — Retrieve XML from current node, including itself
    -   [XMLReader::readString](/class/xmlreader.html#XMLReader::readString)
        — Reads the contents of the current node as a string
    -   [XMLReader::setParserProperty](/class/xmlreader.html#XMLReader::setParserProperty)
        — Set parser options
    -   [XMLReader::setRelaxNGSchema](/class/xmlreader.html#XMLReader::setRelaxNGSchema)
        — Set the filename or URI for a RelaxNG Schema
    -   [XMLReader::setRelaxNGSchemaSource](/class/xmlreader.html#XMLReader::setRelaxNGSchemaSource)
        — Set the data containing a RelaxNG Schema
    -   [XMLReader::setSchema](/class/xmlreader.html#XMLReader::setSchema)
        — Validate document against XSD
    -   [XMLReader::XML](/class/xmlreader.html#XMLReader::XML) — Set the
        data containing the XML to parse

简介
----

The XMLReader extension is an XML Pull parser. The reader acts as a
cursor going forward on the document stream and stopping at each node on
the way.

类摘要
------

**XMLReader**

<span class="ooclass"> class **XMLReader** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::ELEMENT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::ATTRIBUTE` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::TEXT` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::CDATA` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::ENTITY_REF` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::ENTITY` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::PI` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::COMMENT` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::DOC` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::DOC_TYPE` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::DOC_FRAGMENT` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::NOTATION` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::WHITESPACE` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::SIGNIFICANT_WHITESPACE` <span class="initializer"> =
14</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::END_ELEMENT` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::END_ENTITY` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::XML_DECLARATION` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::LOADDTD` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::DEFAULTATTRS` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::VALIDATE` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`XMLReader::SUBST_ENTITIES` <span class="initializer"> = 4</span> ;

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$attributeCount` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$depth`
;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$hasAttributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$hasValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$isDefault` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$isEmptyElement` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$name` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$value` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$xmlLang` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">expand</span> (\[ <span
class="methodparam"><span class="type">DOMNode</span> `$basenode`</span>
\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAttributeNo</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAttributeNs</span> ( <span
class="methodparam"><span class="type">string</span> `$localName`</span>
, <span class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getParserProperty</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isValid</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">lookupNamespace</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">moveToAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">moveToAttributeNo</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">moveToAttributeNs</span> ( <span
class="methodparam"><span class="type">string</span> `$localName`</span>
, <span class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">moveToElement</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">moveToFirstAttribute</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">moveToNextAttribute</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">next</span> (\[ <span class="methodparam"><span
class="type">string</span> `$localname`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">open</span> ( <span class="methodparam"><span
class="type">string</span> `$URI`</span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">read</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">readInnerXml</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">readOuterXml</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">readString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setParserProperty</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> ,
<span class="methodparam"><span class="type">bool</span> `$value`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setRelaxNGSchema</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setRelaxNGSchemaSource</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSchema</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">xml</span> ( <span class="methodparam"><span
class="type">string</span> `$source`</span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \]\] )

}

属性
----

`attributeCount`  
The number of attributes on the node

`baseURI`  
The base URI of the node

`depth`  
Depth of the node in the tree, starting at 0

`hasAttributes`  
Indicates if node has attributes

`hasValue`  
Indicates if node has a text value

`isDefault`  
Indicates if attribute is defaulted from DTD

`isEmptyElement`  
Indicates if node is an empty element tag

`localName`  
The local name of the node

`name`  
The qualified name of the node

`namespaceURI`  
The URI of the namespace associated with the node

`nodeType`  
The node type for the node

`prefix`  
The prefix of the namespace associated with the node

`value`  
The text value of the node

`xmlLang`  
The xml:lang scope which the node resides

预定义常量
----------

XMLReader Node Types
--------------------

**`XMLReader::NONE`**  
No node type

**`XMLReader::ELEMENT`**  
Start element

**`XMLReader::ATTRIBUTE`**  
Attribute node

**`XMLReader::TEXT`**  
Text node

**`XMLReader::CDATA`**  
CDATA node

**`XMLReader::ENTITY_REF`**  
Entity Reference node

**`XMLReader::ENTITY`**  
Entity Declaration node

**`XMLReader::PI`**  
Processing Instruction node

**`XMLReader::COMMENT`**  
Comment node

**`XMLReader::DOC`**  
Document node

**`XMLReader::DOC_TYPE`**  
Document Type node

**`XMLReader::DOC_FRAGMENT`**  
Document Fragment node

**`XMLReader::NOTATION`**  
Notation node

**`XMLReader::WHITESPACE`**  
Whitespace node

**`XMLReader::SIGNIFICANT_WHITESPACE`**  
Significant Whitespace node

**`XMLReader::END_ELEMENT`**  
End Element

**`XMLReader::END_ENTITY`**  
End Entity

**`XMLReader::XML_DECLARATION`**  
XML Declaration node

XMLReader Parser Options
------------------------

**`XMLReader::LOADDTD`**  
Load DTD but do not validate

**`XMLReader::DEFAULTATTRS`**  
Load DTD and default attributes but do not validate

**`XMLReader::VALIDATE`**  
Load DTD and validate while parsing

**`XMLReader::SUBST_ENTITIES`**  
Substitute entities and expand references

XMLReader::close
================

Close the XMLReader input

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::close</span> ( <span
class="methodparam">void</span> )

Closes the input the XMLReader object is currently parsing.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::open</span>
-   <span class="methodname">XMLReader::xml</span>

XMLReader::expand
=================

Returns a copy of the current node as a DOM object

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">XMLReader::expand</span> (\[ <span
class="methodparam"><span class="type">DOMNode</span> `$basenode`</span>
\] )

This method copies the current node and returns the appropriate DOM
object.

### 参数

`basenode`  
A <span class="classname">DOMNode</span> defining the target <span
class="classname">DOMDocument</span> for the created DOM object.

### 返回值

The resulting <span class="classname">DOMNode</span> or **`FALSE`** on
error.

### 更新日志

| 版本  | 说明                                |
|-------|-------------------------------------|
| 5.3.0 | The parameter `basenode` was added. |

XMLReader::getAttribute
=======================

Get the value of a named attribute

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::getAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Returns the value of a named attribute or **`NULL`** if the attribute
does not exist or not positioned on an element node.

### 参数

`name`  
The name of the attribute.

### 返回值

The value of the attribute, or **`NULL`** if no attribute with the given
`name` is found or not positioned on an element node.

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 5.1.3 | Return **`NULL`** if no attribute found. Previously, returned an empty string. |

### 参见

-   <span class="methodname">XMLReader::getAttributeNo</span>
-   <span class="methodname">XMLReader::getAttributeNs</span>

XMLReader::getAttributeNo
=========================

Get the value of an attribute by index

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::getAttributeNo</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Returns the value of an attribute based on its position or an empty
string if attribute does not exist or not positioned on an element node.

### 参数

`index`  
The position of the attribute.

### 返回值

The value of the attribute, or an empty string (before PHP 5.6) or
**`NULL`** (from PHP 5.6 onwards) if no attribute exists at `index` or
is not positioned on the element.

### 更新日志

| 版本  | 说明                                                                                                             |
|-------|------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | <span class="methodname">XMLReader::getAttributeNo</span> now returns **`NULL`** if the attribute doesn't exist. |

### 参见

-   <span class="methodname">XMLReader::getAttribute</span>
-   <span class="methodname">XMLReader::getAttributeNs</span>

XMLReader::getAttributeNs
=========================

Get the value of an attribute by localname and URI

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::getAttributeNs</span> ( <span
class="methodparam"><span class="type">string</span> `$localName`</span>
, <span class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

Returns the value of an attribute by name and namespace URI or an empty
string if attribute does not exist or not positioned on an element node.

### 参数

`localName`  
The local name.

`namespaceURI`  
The namespace URI.

### 返回值

The value of the attribute, or an empty string (before PHP 5.6) or
**`NULL`** (from PHP 5.6 onwards) if no attribute with the given
`localName` and `namespaceURI` is found or not positioned of element.

### 更新日志

| 版本  | 说明                                                                                                             |
|-------|------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | <span class="methodname">XMLReader::getAttributeNS</span> now returns **`NULL`** if the attribute doesn't exist. |

### 参见

-   <span class="methodname">XMLReader::getAttribute</span>
-   <span class="methodname">XMLReader::getAttributeNo</span>

XMLReader::getParserProperty
============================

Indicates if specified property has been set

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::getParserProperty</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> )

Indicates if specified property has been set.

### 参数

`property`  
One of the
<a href="/class/xmlreader.html#预定义常量" class="link">parser option constants</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::setParserProperty</span>

XMLReader::isValid
==================

Indicates if the parsed document is valid

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::isValid</span> ( <span
class="methodparam">void</span> )

Returns a boolean indicating if the document being parsed is currently
valid.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Validating XML**

``` php
<?php
$xml = XMLReader::open('test.xml');

// The validate parser option must be enabled for 
// this method to work properly
$xml->setParserProperty(XMLReader::VALIDATE, true);

var_dump($xml->isValid());
?>
```

### 注释

> **Note**: <span class="simpara"> This checks the current node, not the
> entire document. </span>

### 参见

-   <span class="methodname">XMLReader::setParserProperty</span>
-   <span class="methodname">XMLReader::setRelaxNGSchema</span>
-   <span class="methodname">XMLReader::setRelaxNGSchemaSource</span>
-   <span class="methodname">XMLReader::setSchema</span>

XMLReader::lookupNamespace
==========================

Lookup namespace for a prefix

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::lookupNamespace</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

Lookup in scope namespace for a given prefix.

### 参数

`prefix`  
String containing the prefix.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

XMLReader::moveToAttribute
==========================

Move cursor to a named attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::moveToAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Positions cursor on the named attribute.

### 参数

`name`  
The name of the attribute.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttributeNo</span>
-   <span class="methodname">XMLReader::moveToAttributeNs</span>
-   <span class="methodname">XMLReader::moveToFirstAttribute</span>

XMLReader::moveToAttributeNo
============================

Move cursor to an attribute by index

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::moveToAttributeNo</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Positions cursor on attribute based on its position.

### 参数

`index`  
The position of the attribute.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttribute</span>
-   <span class="methodname">XMLReader::moveToAttributeNs</span>
-   <span class="methodname">XMLReader::moveToFirstAttribute</span>

XMLReader::moveToAttributeNs
============================

Move cursor to a named attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::moveToAttributeNs</span> ( <span
class="methodparam"><span class="type">string</span> `$localName`</span>
, <span class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

Positions cursor on the named attribute in specified namespace.

### 参数

`localName`  
The local name.

`namespaceURI`  
The namespace URI.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttribute</span>
-   <span class="methodname">XMLReader::moveToAttributeNo</span>
-   <span class="methodname">XMLReader::moveToFirstAttribute</span>

XMLReader::moveToElement
========================

Position cursor on the parent Element of current Attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::moveToElement</span> ( <span
class="methodparam">void</span> )

Moves cursor to the parent Element of current Attribute.

### 返回值

Returns **`TRUE`** if successful and **`FALSE`** if it fails or not
positioned on Attribute when this method is called.

### 参见

-   <span class="methodname">XMLReader::moveToAttribute</span>
-   <span class="methodname">XMLReader::moveToAttributeNo</span>
-   <span class="methodname">XMLReader::moveToAttributeNs</span>
-   <span class="methodname">XMLReader::moveToFirstAttribute</span>

XMLReader::moveToFirstAttribute
===============================

Position cursor on the first Attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::moveToFirstAttribute</span> ( <span
class="methodparam">void</span> )

Moves cursor to the first Attribute.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttribute</span>
-   <span class="methodname">XMLReader::moveToAttributeNo</span>
-   <span class="methodname">XMLReader::moveToAttributeNs</span>
-   <span class="methodname">XMLReader::moveToNextAttribute</span>

XMLReader::moveToNextAttribute
==============================

Position cursor on the next Attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::moveToNextAttribute</span> ( <span
class="methodparam">void</span> )

Moves cursor to the next Attribute if positioned on an Attribute or
moves to first attribute if positioned on an Element.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttribute</span>
-   <span class="methodname">XMLReader::moveToAttributeNo</span>
-   <span class="methodname">XMLReader::moveToAttributeNs</span>
-   <span class="methodname">XMLReader::moveToFirstAttribute</span>

XMLReader::next
===============

Move cursor to next node skipping all subtrees

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::next</span> (\[ <span
class="methodparam"><span class="type">string</span> `$localname`</span>
\] )

Positions cursor on the next node skipping all subtrees.

### 参数

`localname`  
The name of the next node to move to.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToNextAttribute</span>
-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttribute</span>

XMLReader::open
===============

Set the URI containing the XML to parse

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::open</span> ( <span
class="methodparam"><span class="type">string</span> `$URI`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \]\] )

Set the URI containing the XML document to be parsed.

### 参数

`URI`  
URI pointing to the document.

`encoding`  
The document encoding or **`NULL`**.

`options`  
A bitmask of the
<a href="/libxml/constants.html" class="link">LIBXML_*</a> constants.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If called
statically, returns an <span class="classname">XMLReader</span>
或者在失败时返回 **`FALSE`**.

### 错误／异常

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 更新日志

| 版本  | 说明                                 |
|-------|--------------------------------------|
| 5.2.0 | `encoding` and `options` were added. |

### 参见

-   <span class="methodname">XMLReader::xml</span>
-   <span class="methodname">XMLReader::close</span>

XMLReader::read
===============

Move to next node in document

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::read</span> ( <span
class="methodparam">void</span> )

Moves cursor to the next node in the document.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::moveToElement</span>
-   <span class="methodname">XMLReader::moveToAttribute</span>
-   <span class="methodname">XMLReader::next</span>

XMLReader::readInnerXml
=======================

Retrieve XML from current node

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::readInnerXml</span> ( <span
class="methodparam">void</span> )

Reads the contents of the current node, including child nodes and
markup.

### 参数

此函数没有参数。

### 返回值

Returns the contents of the current node as a string. Empty string on
failure.

### 注释

**Caution**

此函数仅在 PHP 与 libxml 20620 或以上版本编译时可用。

### 参见

-   <span class="function">XMLReader::readString</span>
-   <span class="function">XMLReader::readOuterXml</span>
-   <span class="function">XMLReader::expand</span>

XMLReader::readOuterXml
=======================

Retrieve XML from current node, including itself

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::readOuterXml</span> ( <span
class="methodparam">void</span> )

Reads the contents of the current node, including the node itself.

### 参数

此函数没有参数。

### 返回值

Returns the contents of current node, including itself, as a string.
Empty string on failure.

### 注释

**Caution**

此函数仅在 PHP 与 libxml 20620 或以上版本编译时可用。

### 参见

-   <span class="function">XMLReader::readString</span>
-   <span class="function">XMLReader::readInnerXml</span>
-   <span class="function">XMLReader::expand</span>

XMLReader::readString
=====================

Reads the contents of the current node as a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">XMLReader::readString</span> ( <span
class="methodparam">void</span> )

Reads the contents of the current node as a string.

### 参数

此函数没有参数。

### 返回值

Returns the content of the current node as a string. Empty string on
failure.

### 注释

**Caution**

此函数仅在 PHP 与 libxml 20620 或以上版本编译时可用。

### 参见

-   <span class="function">XMLReader::readOuterXml</span>
-   <span class="function">XMLReader::readInnerXml</span>
-   <span class="function">XMLReader::expand</span>

XMLReader::setParserProperty
============================

Set parser options

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::setParserProperty</span> ( <span
class="methodparam"><span class="type">int</span> `$property`</span> ,
<span class="methodparam"><span class="type">bool</span> `$value`</span>
)

Set parser options. The options must be set after <span
class="methodname">XMLReader::open</span> or <span
class="methodname">XMLReader::xml</span> are called and before the first
<span class="methodname">XMLReader::read</span> call.

### 参数

`property`  
One of the
<a href="/class/xmlreader.html#预定义常量" class="link">parser option constants</a>.

`value`  
If set to **`TRUE`** the option will be enabled otherwise will be
disabled.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

XMLReader::setRelaxNGSchema
===========================

Set the filename or URI for a RelaxNG Schema

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::setRelaxNGSchema</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Set the filename or URI for the RelaxNG Schema to use for validation.

### 参数

`filename`  
filename or URI pointing to a RelaxNG Schema.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::setRelaxNGSchemaSource</span>
-   <span class="methodname">XMLReader::setSchema</span>
-   <span class="methodname">XMLReader::isValid</span>

XMLReader::setRelaxNGSchemaSource
=================================

Set the data containing a RelaxNG Schema

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::setRelaxNGSchemaSource</span> (
<span class="methodparam"><span class="type">string</span>
`$source`</span> )

Set the data containing a RelaxNG Schema to use for validation.

### 参数

`source`  
String containing the RelaxNG Schema.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">XMLReader::setRelaxNGSchema</span>
-   <span class="methodname">XMLReader::setSchema</span>
-   <span class="methodname">XMLReader::isValid</span>

XMLReader::setSchema
====================

Validate document against XSD

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::setSchema</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Use W3C XSD schema to validate the document as it is processed.
Activation is only possible before the first Read().

### 参数

`filename`  
The filename of the XSD schema.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues **`E_WARNING`** if libxml was built without schema support, the
schema contains errors or if <span
class="function">XMLReader::read</span> has already been called.

### 注释

**Caution**

此函数仅在 PHP 与 libxml 20620 或以上版本编译时可用。

### 参见

-   <span class="methodname">XMLReader::setRelaxNGSchema</span>
-   <span class="methodname">XMLReader::setRelaxNGSchemaSource</span>
-   <span class="methodname">XMLReader::isValid</span>

XMLReader::XML
==============

Set the data containing the XML to parse

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">XMLReader::xml</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
0</span></span> \]\] )

Set the data containing the XML to parse.

### 参数

`source`  
String containing the XML to be parsed.

`encoding`  
The document encoding or **`NULL`**.

`options`  
A bitmask of the
<a href="/libxml/constants.html" class="link">LIBXML_*</a> constants.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If called
statically, returns an <span class="classname">XMLReader</span>
或者在失败时返回 **`FALSE`**.

### 错误／异常

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 更新日志

| 版本  | 说明                                 |
|-------|--------------------------------------|
| 5.2.0 | `encoding` and `options` were added. |

### 参见

-   <span class="methodname">XMLReader::open</span>
-   <span class="methodname">XMLReader::close</span>
