Document Object Model
=====================

**目录**

-   [简介](/intro/dom.html)
-   [安装／配置](/dom/setup.html)
    -   [需求](/dom/setup.html#需求)
    -   [安装](/dom/setup.html#安装)
    -   [运行时配置](/dom/setup.html#运行时配置)
    -   [资源类型](/dom/setup.html#资源类型)
-   [预定义常量](/dom/constants.html)
-   [范例](/dom/examples.html)
-   [DOMAttr](/class/domattr.html) — The DOMAttr class
    -   [DOMAttr::\_\_construct](/class/domattr.html#DOMAttr::__construct)
        — Creates a new DOMAttr object
    -   [DOMAttr::isId](/class/domattr.html#DOMAttr::isId) — Checks if
        attribute is a defined ID
-   [DOMCdataSection](/class/domcdatasection.html) — The DOMCdataSection
    class
    -   [DOMCdataSection::\_\_construct](/class/domcdatasection.html#DOMCdataSection::__construct)
        — Constructs a new DOMCdataSection object
-   [DOMCharacterData](/class/domcharacterdata.html) — The
    DOMCharacterData class
    -   [DOMCharacterData::appendData](/class/domcharacterdata.html#DOMCharacterData::appendData)
        — Append the string to the end of the character data of the node
    -   [DOMCharacterData::deleteData](/class/domcharacterdata.html#DOMCharacterData::deleteData)
        — Remove a range of characters from the node
    -   [DOMCharacterData::insertData](/class/domcharacterdata.html#DOMCharacterData::insertData)
        — Insert a string at the specified 16-bit unit offset
    -   [DOMCharacterData::replaceData](/class/domcharacterdata.html#DOMCharacterData::replaceData)
        — Replace a substring within the DOMCharacterData node
    -   [DOMCharacterData::substringData](/class/domcharacterdata.html#DOMCharacterData::substringData)
        — Extracts a range of data from the node
-   [DOMComment](/class/domcomment.html) — The DOMComment class
    -   [DOMComment::\_\_construct](/class/domcomment.html#DOMComment::__construct)
        — Creates a new DOMComment object
-   [DOMDocument](/class/domdocument.html) — The DOMDocument class
    -   [DOMDocument::\_\_construct](/class/domdocument.html#DOMDocument::__construct)
        — Creates a new DOMDocument object
    -   [DOMDocument::createAttribute](/class/domdocument.html#DOMDocument::createAttribute)
        — Create new attribute
    -   [DOMDocument::createAttributeNS](/class/domdocument.html#DOMDocument::createAttributeNS)
        — Create new attribute node with an associated namespace
    -   [DOMDocument::createCDATASection](/class/domdocument.html#DOMDocument::createCDATASection)
        — Create new cdata node
    -   [DOMDocument::createComment](/class/domdocument.html#DOMDocument::createComment)
        — Create new comment node
    -   [DOMDocument::createDocumentFragment](/class/domdocument.html#DOMDocument::createDocumentFragment)
        — Create new document fragment
    -   [DOMDocument::createElement](/class/domdocument.html#DOMDocument::createElement)
        — Create new element node
    -   [DOMDocument::createElementNS](/class/domdocument.html#DOMDocument::createElementNS)
        — Create new element node with an associated namespace
    -   [DOMDocument::createEntityReference](/class/domdocument.html#DOMDocument::createEntityReference)
        — Create new entity reference node
    -   [DOMDocument::createProcessingInstruction](/class/domdocument.html#DOMDocument::createProcessingInstruction)
        — Creates new PI node
    -   [DOMDocument::createTextNode](/class/domdocument.html#DOMDocument::createTextNode)
        — Create new text node
    -   [DOMDocument::getElementById](/class/domdocument.html#DOMDocument::getElementById)
        — Searches for an element with a certain id
    -   [DOMDocument::getElementsByTagName](/class/domdocument.html#DOMDocument::getElementsByTagName)
        — Searches for all elements with given local tag name
    -   [DOMDocument::getElementsByTagNameNS](/class/domdocument.html#DOMDocument::getElementsByTagNameNS)
        — Searches for all elements with given tag name in specified
        namespace
    -   [DOMDocument::importNode](/class/domdocument.html#DOMDocument::importNode)
        — Import node into current document
    -   [DOMDocument::load](/class/domdocument.html#DOMDocument::load) —
        Load XML from a file
    -   [DOMDocument::loadHTML](/class/domdocument.html#DOMDocument::loadHTML)
        — Load HTML from a string
    -   [DOMDocument::loadHTMLFile](/class/domdocument.html#DOMDocument::loadHTMLFile)
        — Load HTML from a file
    -   [DOMDocument::loadXML](/class/domdocument.html#DOMDocument::loadXML)
        — Load XML from a string
    -   [DOMDocument::normalizeDocument](/class/domdocument.html#DOMDocument::normalizeDocument)
        — Normalizes the document
    -   [DOMDocument::registerNodeClass](/class/domdocument.html#DOMDocument::registerNodeClass)
        — Register extended class used to create base node type
    -   [DOMDocument::relaxNGValidate](/class/domdocument.html#DOMDocument::relaxNGValidate)
        — Performs relaxNG validation on the document
    -   [DOMDocument::relaxNGValidateSource](/class/domdocument.html#DOMDocument::relaxNGValidateSource)
        — Performs relaxNG validation on the document
    -   [DOMDocument::save](/class/domdocument.html#DOMDocument::save) —
        Dumps the internal XML tree back into a file
    -   [DOMDocument::saveHTML](/class/domdocument.html#DOMDocument::saveHTML)
        — Dumps the internal document into a string using HTML
        formatting
    -   [DOMDocument::saveHTMLFile](/class/domdocument.html#DOMDocument::saveHTMLFile)
        — Dumps the internal document into a file using HTML formatting
    -   [DOMDocument::saveXML](/class/domdocument.html#DOMDocument::saveXML)
        — Dumps the internal XML tree back into a string
    -   [DOMDocument::schemaValidate](/class/domdocument.html#DOMDocument::schemaValidate)
        — Validates a document based on a schema
    -   [DOMDocument::schemaValidateSource](/class/domdocument.html#DOMDocument::schemaValidateSource)
        — Validates a document based on a schema
    -   [DOMDocument::validate](/class/domdocument.html#DOMDocument::validate)
        — Validates the document based on its DTD
    -   [DOMDocument::xinclude](/class/domdocument.html#DOMDocument::xinclude)
        — Substitutes XIncludes in a DOMDocument Object
-   [DOMDocumentFragment](/class/domdocumentfragment.html) — The
    DOMDocumentFragment class
    -   [DOMDocumentFragment::appendXML](/class/domdocumentfragment.html#DOMDocumentFragment::appendXML)
        — Append raw XML data
-   [DOMDocumentType](/class/domdocumenttype.html) — The DOMDocumentType
    class
-   [DOMElement](/class/domelement.html) — The DOMElement class
    -   [DOMElement::\_\_construct](/class/domelement.html#DOMElement::__construct)
        — Creates a new DOMElement object
    -   [DOMElement::getAttribute](/class/domelement.html#DOMElement::getAttribute)
        — Returns value of attribute
    -   [DOMElement::getAttributeNode](/class/domelement.html#DOMElement::getAttributeNode)
        — Returns attribute node
    -   [DOMElement::getAttributeNodeNS](/class/domelement.html#DOMElement::getAttributeNodeNS)
        — Returns attribute node
    -   [DOMElement::getAttributeNS](/class/domelement.html#DOMElement::getAttributeNS)
        — Returns value of attribute
    -   [DOMElement::getElementsByTagName](/class/domelement.html#DOMElement::getElementsByTagName)
        — Gets elements by tagname
    -   [DOMElement::getElementsByTagNameNS](/class/domelement.html#DOMElement::getElementsByTagNameNS)
        — Get elements by namespaceURI and localName
    -   [DOMElement::hasAttribute](/class/domelement.html#DOMElement::hasAttribute)
        — Checks to see if attribute exists
    -   [DOMElement::hasAttributeNS](/class/domelement.html#DOMElement::hasAttributeNS)
        — Checks to see if attribute exists
    -   [DOMElement::removeAttribute](/class/domelement.html#DOMElement::removeAttribute)
        — Removes attribute
    -   [DOMElement::removeAttributeNode](/class/domelement.html#DOMElement::removeAttributeNode)
        — Removes attribute
    -   [DOMElement::removeAttributeNS](/class/domelement.html#DOMElement::removeAttributeNS)
        — Removes attribute
    -   [DOMElement::setAttribute](/class/domelement.html#DOMElement::setAttribute)
        — Adds new attribute
    -   [DOMElement::setAttributeNode](/class/domelement.html#DOMElement::setAttributeNode)
        — Adds new attribute node to element
    -   [DOMElement::setAttributeNodeNS](/class/domelement.html#DOMElement::setAttributeNodeNS)
        — Adds new attribute node to element
    -   [DOMElement::setAttributeNS](/class/domelement.html#DOMElement::setAttributeNS)
        — Adds new attribute
    -   [DOMElement::setIdAttribute](/class/domelement.html#DOMElement::setIdAttribute)
        — Declares the attribute specified by name to be of type ID
    -   [DOMElement::setIdAttributeNode](/class/domelement.html#DOMElement::setIdAttributeNode)
        — Declares the attribute specified by node to be of type ID
    -   [DOMElement::setIdAttributeNS](/class/domelement.html#DOMElement::setIdAttributeNS)
        — Declares the attribute specified by local name and namespace
        URI to be of type ID
-   [DOMEntity](/class/domentity.html) — The DOMEntity class
-   [DOMEntityReference](/class/domentityreference.html) — The
    DOMEntityReference class
    -   [DOMEntityReference::\_\_construct](/class/domentityreference.html#DOMEntityReference::__construct)
        — Creates a new DOMEntityReference object
-   [DOMException](/class/domexception.html) — The DOMException class
-   [DOMImplementation](/class/domimplementation.html) — The
    DOMImplementation class
    -   [DOMImplementation::\_\_construct](/class/domimplementation.html#DOMImplementation::__construct)
        — Creates a new DOMImplementation object
    -   [DOMImplementation::createDocument](/class/domimplementation.html#DOMImplementation::createDocument)
        — Creates a DOMDocument object of the specified type with its
        document element
    -   [DOMImplementation::createDocumentType](/class/domimplementation.html#DOMImplementation::createDocumentType)
        — Creates an empty DOMDocumentType object
    -   [DOMImplementation::hasFeature](/class/domimplementation.html#DOMImplementation::hasFeature)
        — Test if the DOM implementation implements a specific feature
-   [DOMNamedNodeMap](/class/domnamednodemap.html) — The DOMNamedNodeMap
    class
    -   [DOMNamedNodeMap::count](/class/domnamednodemap.html#DOMNamedNodeMap::count)
        — Get number of nodes in the map
    -   [DOMNamedNodeMap::getNamedItem](/class/domnamednodemap.html#DOMNamedNodeMap::getNamedItem)
        — Retrieves a node specified by name
    -   [DOMNamedNodeMap::getNamedItemNS](/class/domnamednodemap.html#DOMNamedNodeMap::getNamedItemNS)
        — Retrieves a node specified by local name and namespace URI
    -   [DOMNamedNodeMap::item](/class/domnamednodemap.html#DOMNamedNodeMap::item)
        — Retrieves a node specified by index
-   [DOMNode](/class/domnode.html) — The DOMNode class
    -   [DOMNode::appendChild](/class/domnode.html#DOMNode::appendChild)
        — Adds new child at the end of the children
    -   [DOMNode::C14N](/class/domnode.html#DOMNode::C14N) —
        Canonicalize nodes to a string
    -   [DOMNode::C14NFile](/class/domnode.html#DOMNode::C14NFile) —
        Canonicalize nodes to a file
    -   [DOMNode::cloneNode](/class/domnode.html#DOMNode::cloneNode) —
        Clones a node
    -   [DOMNode::getLineNo](/class/domnode.html#DOMNode::getLineNo) —
        Get line number for a node
    -   [DOMNode::getNodePath](/class/domnode.html#DOMNode::getNodePath)
        — Get an XPath for a node
    -   [DOMNode::hasAttributes](/class/domnode.html#DOMNode::hasAttributes)
        — Checks if node has attributes
    -   [DOMNode::hasChildNodes](/class/domnode.html#DOMNode::hasChildNodes)
        — Checks if node has children
    -   [DOMNode::insertBefore](/class/domnode.html#DOMNode::insertBefore)
        — Adds a new child before a reference node
    -   [DOMNode::isDefaultNamespace](/class/domnode.html#DOMNode::isDefaultNamespace)
        — Checks if the specified namespaceURI is the default namespace
        or not
    -   [DOMNode::isSameNode](/class/domnode.html#DOMNode::isSameNode) —
        Indicates if two nodes are the same node
    -   [DOMNode::isSupported](/class/domnode.html#DOMNode::isSupported)
        — Checks if feature is supported for specified version
    -   [DOMNode::lookupNamespaceUri](/class/domnode.html#DOMNode::lookupNamespaceUri)
        — Gets the namespace URI of the node based on the prefix
    -   [DOMNode::lookupPrefix](/class/domnode.html#DOMNode::lookupPrefix)
        — Gets the namespace prefix of the node based on the namespace
        URI
    -   [DOMNode::normalize](/class/domnode.html#DOMNode::normalize) —
        Normalizes the node
    -   [DOMNode::removeChild](/class/domnode.html#DOMNode::removeChild)
        — Removes child from list of children
    -   [DOMNode::replaceChild](/class/domnode.html#DOMNode::replaceChild)
        — Replaces a child
-   [DOMNodeList](/class/domnodelist.html) — The DOMNodeList class
    -   [DOMNodeList::count](/class/domnodelist.html#DOMNodeList::count)
        — Get number of nodes in the list
    -   [DOMNodeList::item](/class/domnodelist.html#DOMNodeList::item) —
        Retrieves a node specified by index
-   [DOMNotation](/class/domnotation.html) — The DOMNotation class
-   [DOMProcessingInstruction](/class/domprocessinginstruction.html) —
    The DOMProcessingInstruction class
    -   [DOMProcessingInstruction::\_\_construct](/class/domprocessinginstruction.html#DOMProcessingInstruction::__construct)
        — Creates a new DOMProcessingInstruction object
-   [DOMText](/class/domtext.html) — The DOMText class
    -   [DOMText::\_\_construct](/class/domtext.html#DOMText::__construct)
        — Creates a new DOMText object
    -   [DOMText::isElementContentWhitespace](/class/domtext.html#DOMText::isElementContentWhitespace)
        — Returns whether this text node contains whitespace in element
        content
    -   [DOMText::isWhitespaceInElementContent](/class/domtext.html#DOMText::isWhitespaceInElementContent)
        — Indicates whether this text node contains whitespace
    -   [DOMText::splitText](/class/domtext.html#DOMText::splitText) —
        Breaks this node into two nodes at the specified offset
-   [DOMXPath](/class/domxpath.html) — The DOMXPath class
    -   [DOMXPath::\_\_construct](/class/domxpath.html#DOMXPath::__construct)
        — Creates a new DOMXPath object
    -   [DOMXPath::evaluate](/class/domxpath.html#DOMXPath::evaluate) —
        Evaluates the given XPath expression and returns a typed result
        if possible
    -   [DOMXPath::query](/class/domxpath.html#DOMXPath::query) —
        Evaluates the given XPath expression
    -   [DOMXPath::registerNamespace](/class/domxpath.html#DOMXPath::registerNamespace)
        — Registers the namespace with the DOMXPath object
    -   [DOMXPath::registerPhpFunctions](/class/domxpath.html#DOMXPath::registerPhpFunctions)
        — Register PHP functions as XPath functions
-   [DOM 函数](/ref/dom.html)
    -   [dom\_import\_simplexml](/ref/dom.html#dom_import_simplexml) —
        Gets a DOMElement object from a SimpleXMLElement object

简介
----

<span class="classname">DOMAttr</span> represents an attribute in the
<span class="classname">DOMElement</span> object.

类摘要
------

**DOMAttr**

<span class="ooclass"> class **DOMAttr** </span> <span class="ooclass">
<span class="modifier">extends</span> **DOMNode** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$name` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMElement</span>
`$ownerElement` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$schemaTypeInfo` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$specified` ;

<span class="modifier">public</span> <span class="type">string</span>
`$value` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isId</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`name`  
The name of the attribute

`ownerElement`  
The element which contains the attribute

`schemaTypeInfo`  
Not implemented yet, always is **`NULL`**

`specified`  
Not implemented yet, always is **`NULL`**

`value`  
The value of the attribute

参见
----

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-637646024" class="link external">» W3C specification of Attr</a>

DOMAttr::\_\_construct
======================

Creates a new <span class="classname">DOMAttr</span> object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMAttr::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

Creates a new DOMAttr object. This object is read only. It may be
appended to a document, but additional nodes may not be appended to this
node until the node is associated with a document. To create a writable
node, use
<a href="/class/domdocument.html#DOMDocument::createAttribute" class="xref"></a>.

### 参数

`name`  
The tag name of the attribute.

`value`  
The value of the attribute.

### 范例

**示例 \#1 Creating a new <span class="classname">DOMAttr</span>
object**

``` php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$attr = $element->setAttributeNode(new DOMAttr('attr', 'attrvalue'));
echo $dom->saveXML(); 

?>
```

以上例程会输出：

    <?xml version="1.0" encoding="utf-8"?>
    <root attr="attrvalue" />

### 参见

-   <span class="methodname">DOMDocument::createAttribute</span>

DOMAttr::isId
=============

Checks if attribute is a defined ID

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMAttr::isId</span> ( <span
class="methodparam">void</span> )

This function checks if the attribute is a defined ID.

According to the DOM standard this requires a DTD which defines the
attribute ID to be of type ID. You need to validate your document with
<a href="/class/domdocument.html#DOMDocument::validate" class="xref"></a>
or *DOMDocument::validateOnParse* before using this function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 DOMAttr::isId() Example**

``` php
<?php

$doc = new DomDocument;

// We need to validate our document before referring to the id
$doc->validateOnParse = true;
$doc->Load('book.xml');

// We retrieve the attribute named id of the chapter element
$attr = $doc->getElementsByTagName('chapter')->item(0)->getAttributeNode('id');

var_dump($attr->isId()); // bool(true)

?>
```

简介
----

The <span class="classname">DOMCdataSection</span> inherits from <span
class="classname">DOMText</span> for textural representation of CData
constructs.

类摘要
------

**DOMCdataSection**

<span class="ooclass"> class **DOMCdataSection** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMText**
</span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$wholeText` ;

<span class="modifier">public</span> <span class="type">string</span>
`$data` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* Methods \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

/\* Inherited methods \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMText::isElementContentWhitespace</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMText::isWhitespaceInElementContent</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMText</span>
<span class="methodname">DOMText::splitText</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::appendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::deleteData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::insertData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::replaceData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMCharacterData::substringData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

DOMCdataSection::\_\_construct
==============================

Constructs a new DOMCdataSection object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMCdataSection::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

Constructs a new CDATA node. This works like the <span
class="classname">DOMText</span> class.

### 参数

`value`  
The value of the CDATA node. If not supplied, an empty CDATA node is
created.

### 范例

**示例 \#1 Creating a new DOMCdataSection object**

``` php
<?php

$dom = new DOMDocument('1.0', 'utf-8');
$element = $dom->appendChild(new DOMElement('root'));
$text = $element->appendChild(new DOMCdataSection('root value'));
echo $dom->saveXML();

?>
```

以上例程会输出：

    <?xml version="1.0" encoding="utf-8"?>
    <root><![CDATA[root value]]></root>

### 参见

-   <span class="methodname">DOMText::\_\_construct</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

简介
----

Represents nodes with character data. No nodes directly correspond to
this class, but other nodes do inherit from it.

类摘要
------

**DOMCharacterData**

<span class="ooclass"> class **DOMCharacterData** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$data` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">appendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">deleteData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">insertData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">replaceData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">substringData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`data`  
The contents of the node.

`length`  
The length of the contents.

参见
----

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-FF21A306" class="link external">» W3C specification of CharacterData</a>

DOMCharacterData::appendData
============================

Append the string to the end of the character data of the node

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::appendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Append the string `data` to the end of the character data of the node.

### 参数

`data`  
The string to append.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">DOMCharacterData::deleteData</span>
-   <span class="methodname">DOMCharacterData::insertData</span>
-   <span class="methodname">DOMCharacterData::replaceData</span>
-   <span class="methodname">DOMCharacterData::substringData</span>

DOMCharacterData::deleteData
============================

Remove a range of characters from the node

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::deleteData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

Deletes `count` characters starting from position `offset`.

### 参数

`offset`  
The offset from which to start removing.

`count`  
The number of characters to delete. If the sum of `offset` and `count`
exceeds the length, then all characters to the end of the data are
deleted.

### 返回值

没有返回值。

### 错误／异常

**`DOM_INDEX_SIZE_ERR`**  
Raised if `offset` is negative or greater than the number of 16-bit
units in data, or if `count` is negative.

### 参见

-   <span class="methodname">DOMCharacterData::appendData</span>
-   <span class="methodname">DOMCharacterData::insertData</span>
-   <span class="methodname">DOMCharacterData::replaceData</span>
-   <span class="methodname">DOMCharacterData::substringData</span>

DOMCharacterData::insertData
============================

Insert a string at the specified 16-bit unit offset

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::insertData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

Inserts string `data` at position `offset`.

### 参数

`offset`  
The character offset at which to insert.

`data`  
The string to insert.

### 返回值

没有返回值。

### 错误／异常

**`DOM_INDEX_SIZE_ERR`**  
Raised if `offset` is negative or greater than the number of 16-bit
units in data.

### 参见

-   <span class="methodname">DOMCharacterData::appendData</span>
-   <span class="methodname">DOMCharacterData::deleteData</span>
-   <span class="methodname">DOMCharacterData::replaceData</span>
-   <span class="methodname">DOMCharacterData::substringData</span>

DOMCharacterData::replaceData
=============================

Replace a substring within the DOMCharacterData node

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::replaceData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> )

Replace `count` characters starting from position `offset` with `data`.

### 参数

`offset`  
The offset from which to start replacing.

`count`  
The number of characters to replace. If the sum of `offset` and `count`
exceeds the length, then all characters to the end of the data are
replaced.

`data`  
The string with which the range must be replaced.

### 返回值

没有返回值。

### 错误／异常

**`DOM_INDEX_SIZE_ERR`**  
Raised if `offset` is negative or greater than the number of 16-bit
units in data, or if `count` is negative.

### 参见

-   <span class="methodname">DOMCharacterData::appendData</span>
-   <span class="methodname">DOMCharacterData::deleteData</span>
-   <span class="methodname">DOMCharacterData::insertData</span>
-   <span class="methodname">DOMCharacterData::substringData</span>

DOMCharacterData::substringData
===============================

Extracts a range of data from the node

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMCharacterData::substringData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

Returns the specified substring.

### 参数

`offset`  
Start offset of substring to extract.

`count`  
The number of characters to extract.

### 返回值

The specified substring. If the sum of `offset` and `count` exceeds the
length, then all 16-bit units to the end of the data are returned.

### 错误／异常

**`DOM_INDEX_SIZE_ERR`**  
Raised if `offset` is negative or greater than the number of 16-bit
units in data, or if `count` is negative.

### 参见

-   <span class="methodname">DOMCharacterData::appendData</span>
-   <span class="methodname">DOMCharacterData::deleteData</span>
-   <span class="methodname">DOMCharacterData::insertData</span>
-   <span class="methodname">DOMCharacterData::replaceData</span>

简介
----

Represents comment nodes, characters delimited by `<!--` and `-->`.

类摘要
------

**DOMComment**

<span class="ooclass"> class **DOMComment** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**DOMCharacterData** </span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$data` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::appendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::deleteData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::insertData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::replaceData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMCharacterData::substringData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

参见
----

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-1728279322" class="link external">» W3C specification of Comment</a>

DOMComment::\_\_construct
=========================

Creates a new DOMComment object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMComment::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

Creates a new <span class="classname">DOMComment</span> object. This
object is read only. It may be appended to a document, but additional
nodes may not be appended to this node until the node is associated with
a document. To create a writeable node, use
<a href="/class/domdocument.html#DOMDocument::createComment" class="xref"></a>.

### 参数

`value`  
The value of the comment.

### 范例

**示例 \#1 Creating a new DOMComment**

``` php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$comment = $element->appendChild(new DOMComment('root comment'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root><!--root comment--></root> */

?>
```

### 参见

-   <span class="methodname">DOMDocument::createComment</span>

简介
----

Represents an entire HTML or XML document; serves as the root of the
document tree.

类摘要
------

**DOMDocument**

<span class="ooclass"> class **DOMDocument** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$actualEncoding` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMConfiguration</span> `$config` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMDocumentType</span> `$doctype` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMElement</span>
`$documentElement` ;

<span class="modifier">public</span> <span class="type">string</span>
`$documentURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$encoding` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$formatOutput` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMImplementation</span> `$implementation` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$preserveWhiteSpace` <span class="initializer"> = **`TRUE`**</span> ;

<span class="modifier">public</span> <span class="type">bool</span>
`$recover` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$resolveExternals` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$standalone` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$strictErrorChecking` <span class="initializer"> = **`TRUE`**</span> ;

<span class="modifier">public</span> <span class="type">bool</span>
`$substituteEntities` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$validateOnParse` <span class="initializer"> = **`FALSE`**</span> ;

<span class="modifier">public</span> <span class="type">string</span>
`$version` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$xmlEncoding` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$xmlStandalone` ;

<span class="modifier">public</span> <span class="type">string</span>
`$xmlVersion` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$version`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> \]\] )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">createAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">createAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifiedName`</span> )

<span class="modifier">public</span> <span
class="type">DOMCDATASection</span> <span
class="methodname">createCDATASection</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">DOMComment</span> <span
class="methodname">createComment</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">DOMDocumentFragment</span> <span
class="methodname">createDocumentFragment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">DOMElement</span> <span
class="methodname">createElement</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

<span class="modifier">public</span> <span
class="type">DOMElement</span> <span
class="methodname">createElementNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifiedName`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

<span class="modifier">public</span> <span
class="type">DOMEntityReference</span> <span
class="methodname">createEntityReference</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="type">DOMProcessingInstruction</span> <span
class="methodname">createProcessingInstruction</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$data`</span> \] )

<span class="modifier">public</span> <span class="type">DOMText</span>
<span class="methodname">createTextNode</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

<span class="modifier">public</span> <span
class="type">DOMElement</span> <span
class="methodname">getElementById</span> ( <span
class="methodparam"><span class="type">string</span> `$elementId`</span>
)

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">getElementsByTagName</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">getElementsByTagNameNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">importNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span>
`$importedNode`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$deep`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">load</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">loadHTML</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">loadHTMLFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">loadXML</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">normalizeDocument</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">registerNodeClass</span> ( <span
class="methodparam"><span class="type">string</span> `$baseclass`</span>
, <span class="methodparam"><span class="type">string</span>
`$extendedclass`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">relaxNGValidate</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">relaxNGValidateSource</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">save</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">saveHTML</span> (\[ <span
class="methodparam"><span class="type">DOMNode</span> `$node`<span
class="initializer"> = NULL</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">saveHTMLFile</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">saveXML</span> (\[ <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">schemaValidate</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">schemaValidateSource</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">validate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">xinclude</span> (\[ <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
0</span></span> \] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`actualEncoding`  
*Deprecated*. Actual encoding of the document, is a readonly equivalent
to `encoding`.

`config`  
*Deprecated*. Configuration used when <span
class="function">DOMDocument::normalizeDocument</span> is invoked.

`doctype`  
The Document Type Declaration associated with this document.

`documentElement`  
This is a convenience attribute that allows direct access to the child
node that is the document element of the document.

`documentURI`  
The location of the document or **`NULL`** if undefined.

`encoding`  
Encoding of the document, as specified by the XML declaration. This
attribute is not present in the final DOM Level 3 specification, but is
the only way of manipulating XML document encoding in this
implementation.

`formatOutput`  
Nicely formats output with indentation and extra space.

`implementation`  
The <span class="classname">DOMImplementation</span> object that handles
this document.

`preserveWhiteSpace`  
Do not remove redundant white space. Default to **`TRUE`**.

`recover`  
*Proprietary*. Enables recovery mode, i.e. trying to parse non-well
formed documents. This attribute is not part of the DOM specification
and is specific to libxml.

`resolveExternals`  
Set it to **`TRUE`** to load external entities from a doctype
declaration. This is useful for including character entities in your XML
document.

`standalone`  
*Deprecated*. Whether or not the document is standalone, as specified by
the XML declaration, corresponds to `xmlStandalone`.

`strictErrorChecking`  
Throws <span class="classname">DOMException</span> on errors. Default to
**`TRUE`**.

`substituteEntities`  
*Proprietary*. Whether or not to substitute entities. This attribute is
not part of the DOM specification and is specific to libxml.

**Caution**
Enabling entity substitution may facilitate XML External Entity (XXE)
attacks.

`validateOnParse`  
Loads and validates against the DTD. Default to **`FALSE`**.

`version`  
*Deprecated*. Version of XML, corresponds to `xmlVersion`.

`xmlEncoding`  
An attribute specifying, as part of the XML declaration, the encoding of
this document. This is **`NULL`** when unspecified or when it is not
known, such as when the Document was created in memory.

`xmlStandalone`  
An attribute specifying, as part of the XML declaration, whether this
document is standalone. This is **`FALSE`** when unspecified.

`xmlVersion`  
An attribute specifying, as part of the XML declaration, the version
number of this document. If there is no declaration and if this document
supports the "XML" feature, the value is "1.0".

注释
----

> **Note**:
>
> 此 DOM 扩展采用 UTF-8 编码。在 ISO-8859-1 编码下，使用 <span
> class="function">utf8\_encode</span> 和 <span
> class="function">utf8\_decode</span> 来处理，其它编码下使用
> <a href="/ref/iconv.html" class="link">iconv</a> 函数处理。

> **Note**:
>
> When using <span class="function">json\_encode</span> on a <span
> class="classname">DOMDocument</span> object the result will be that of
> encoding an empty object.

参见
----

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-i-Document" class="link external">» W3C specification for Document</a>

DOMDocument::\_\_construct
==========================

Creates a new DOMDocument object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMDocument::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$version`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> \]\] )

Creates a new <span class="classname">DOMDocument</span> object.

### 参数

`version`  
The version number of the document as part of the XML declaration.

`encoding`  
The encoding of the document as part of the XML declaration.

### 范例

**示例 \#1 Creating a new DOMDocument**

``` php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');

echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?> */

?>
```

### 参见

-   <span class="methodname">DOMImplementation::createDocument</span>

DOMDocument::createAttribute
============================

Create new attribute

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMDocument::createAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

This function creates a new instance of class <span
class="classname">DOMAttr</span>. 此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`name`  
The name of the attribute.

### 返回值

The new <span class="classname">DOMAttr</span> or **`FALSE`** if an
error occurred.

### 错误／异常

**`DOM_INVALID_CHARACTER_ERR`**  
Raised if `name` contains an invalid character.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createAttributeNS
==============================

Create new attribute node with an associated namespace

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMDocument::createAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifiedName`</span> )

This function creates a new instance of class <span
class="classname">DOMAttr</span>. 此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`namespaceURI`  
The URI of the namespace.

`qualifiedName`  
The tag name and prefix of the attribute, as *prefix:tagname*.

### 返回值

The new <span class="classname">DOMAttr</span> or **`FALSE`** if an
error occurred.

### 错误／异常

**`DOM_INVALID_CHARACTER_ERR`**  
Raised if `qualifiedName` contains an invalid character.

**`DOM_NAMESPACE_ERR`**  
Raised if `qualifiedName` is a malformed qualified name, or if
`qualifiedName` has a prefix and `namespaceURI` is **`NULL`**.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createCDATASection
===============================

Create new cdata node

### 说明

<span class="modifier">public</span> <span
class="type">DOMCDATASection</span> <span
class="methodname">DOMDocument::createCDATASection</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

This function creates a new instance of class <span
class="classname">DOMCDATASection</span>.
此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`data`  
The content of the cdata.

### 返回值

The new <span class="classname">DOMCDATASection</span> or **`FALSE`** if
an error occurred.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createComment
==========================

Create new comment node

### 说明

<span class="modifier">public</span> <span
class="type">DOMComment</span> <span
class="methodname">DOMDocument::createComment</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

This function creates a new instance of class <span
class="classname">DOMComment</span>. 此节点出现在文档中，除非是用诸如
<span class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`data`  
The content of the comment.

### 返回值

The new <span class="classname">DOMComment</span> or **`FALSE`** if an
error occurred.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createDocumentFragment
===================================

Create new document fragment

### 说明

<span class="modifier">public</span> <span
class="type">DOMDocumentFragment</span> <span
class="methodname">DOMDocument::createDocumentFragment</span> ( <span
class="methodparam">void</span> )

This function creates a new instance of class <span
class="classname">DOMDocumentFragment</span>.
此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 返回值

The new <span class="classname">DOMDocumentFragment</span> or
**`FALSE`** if an error occurred.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createElement
==========================

Create new element node

### 说明

<span class="modifier">public</span> <span
class="type">DOMElement</span> <span
class="methodname">DOMDocument::createElement</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

This function creates a new instance of class <span
class="classname">DOMElement</span>. 此节点出现在文档中，除非是用诸如
<span class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`name`  
The tag name of the element.

`value`  
The value of the element. By default, an empty element will be created.
The value can also be set later with
<a href="/class/domnode.html#" class="link">DOMElement::$nodeValue</a>.

The value is used verbatim except that the \< and \> entity references
will escaped. Note that & has to be manually escaped; otherwise it is
regarded as starting an entity reference. Also " won't be escaped.

### 返回值

Returns a new instance of class <span
class="classname">DOMElement</span> or **`FALSE`** if an error occurred.

### 错误／异常

**`DOM_INVALID_CHARACTER_ERR`**  
Raised if `name` contains an invalid character.

### 范例

**示例 \#1 Creating a new element and inserting it as root**

``` php
<?php

$dom = new DOMDocument('1.0', 'utf-8');

$element = $dom->createElement('test', 'This is the root element!');

// We insert the new element as root (child of the document)
$dom->appendChild($element);

echo $dom->saveXML();
?>
```

以上例程会输出：

    <?xml version="1.0" encoding="utf-8"?>
    <test>This is the root element!</test>

**示例 \#2 Passing text containing an unescaped & as `value`**

``` php
<?php
$dom = new DOMDocument('1.0', 'utf-8');
$element = $dom->createElement('foo', 'me & you');
$dom->appendChild($element);
echo $dom->saveXML();
?>
```

以上例程的输出类似于：

    Warning: DOMDocument::createElement(): unterminated entity reference             you in /in/BjTCg on line 4
    <?xml version="1.0" encoding="utf-8"?>
    <foo/>

### 注释

> **Note**:
>
> The `value` will *not* be escaped. Use <span
> class="methodname">DOMDocument::createTextNode</span> to create a text
> node with *escaping support*.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createElementNS
============================

Create new element node with an associated namespace

### 说明

<span class="modifier">public</span> <span
class="type">DOMElement</span> <span
class="methodname">DOMDocument::createElementNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifiedName`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

This function creates a new element node with an associated namespace.
此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`namespaceURI`  
The URI of the namespace.

`qualifiedName`  
The qualified name of the element, as *prefix:tagname*.

`value`  
The value of the element. By default, an empty element will be created.
You can also set the value later with
<a href="/class/domnode.html#" class="link">DOMElement::$nodeValue</a>.

### 返回值

The new <span class="classname">DOMElement</span> or **`FALSE`** if an
error occurred.

### 错误／异常

**`DOM_INVALID_CHARACTER_ERR`**  
Raised if `qualifiedName` contains an invalid character.

**`DOM_NAMESPACE_ERR`**  
Raised if `qualifiedName` is a maformed qualified name.

### 范例

**示例 \#1 Creating a new element and inserting it as root**

``` php
<?php

$dom = new DOMDocument('1.0', 'utf-8');

$element = $dom->createElementNS('http://www.example.com/XFoo', 'xfoo:test', 'This is the root element!');

// We insert the new element as root (child of the document)
$dom->appendChild($element);

echo $dom->saveXML();
?>
```

以上例程会输出：

    <?xml version="1.0" encoding="utf-8"?>
    <xfoo:test xmlns:xfoo="http://www.example.com/XFoo">This is the root element!</xfoo:test>

**示例 \#2 A namespace prefix example**

``` php
<?php
$doc  = new DOMDocument('1.0', 'utf-8');
$doc->formatOutput = true;
$root = $doc->createElementNS('http://www.w3.org/2005/Atom', 'element');
$doc->appendChild($root);
$root->setAttributeNS('http://www.w3.org/2000/xmlns/' ,'xmlns:g', 'http://base.google.com/ns/1.0');
$item = $doc->createElementNS('http://base.google.com/ns/1.0', 'g:item_type', 'house');
$root->appendChild($item);

echo $doc->saveXML(), "\n";

echo $item->namespaceURI, "\n"; // Outputs: http://base.google.com/ns/1.0
echo $item->prefix, "\n";       // Outputs: g
echo $item->localName, "\n";    // Outputs: item_type
?>
```

以上例程会输出：

    <?xml version="1.0" encoding="utf-8"?>
    <element xmlns="http://www.w3.org/2005/Atom" xmlns:g="http://base.google.com/ns/1.0">
      <g:item_type>house</g:item_type>
    </element>

    http://base.google.com/ns/1.0
    g
    item_type

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createEntityReference
==================================

Create new entity reference node

### 说明

<span class="modifier">public</span> <span
class="type">DOMEntityReference</span> <span
class="methodname">DOMDocument::createEntityReference</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

This function creates a new instance of class <span
class="classname">DOMEntityReference</span>.
此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`name`  
The content of the entity reference, e.g. the entity reference minus the
leading *&* and the trailing *;* characters.

### 返回值

The new <span class="classname">DOMEntityReference</span> or **`FALSE`**
if an error occurred.

### 错误／异常

**`DOM_INVALID_CHARACTER_ERR`**  
Raised if `name` contains an invalid character.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createProcessingInstruction
========================================

Creates new PI node

### 说明

<span class="modifier">public</span> <span
class="type">DOMProcessingInstruction</span> <span
class="methodname">DOMDocument::createProcessingInstruction</span> (
<span class="methodparam"><span class="type">string</span>
`$target`</span> \[, <span class="methodparam"><span
class="type">string</span> `$data`</span> \] )

This function creates a new instance of class <span
class="classname">DOMProcessingInstruction</span>.
此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`target`  
The target of the processing instruction.

`data`  
The content of the processing instruction.

### 返回值

The new <span class="classname">DOMProcessingInstruction</span> or
**`FALSE`** if an error occurred.

### 错误／异常

**`DOM_INVALID_CHARACTER_ERR`**  
Raised if `target` contains an invalid character.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span class="methodname">DOMDocument::createTextNode</span>

DOMDocument::createTextNode
===========================

Create new text node

### 说明

<span class="modifier">public</span> <span class="type">DOMText</span>
<span class="methodname">DOMDocument::createTextNode</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

This function creates a new instance of class <span
class="classname">DOMText</span>. 此节点出现在文档中，除非是用诸如 <span
class="function">DOMNode-\>appendChild</span> 等函数来将其插入。

### 参数

`content`  
The content of the text.

### 返回值

The new <span class="classname">DOMText</span> or **`FALSE`** if an
error occurred.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMDocument::createAttribute</span>
-   <span class="methodname">DOMDocument::createAttributeNS</span>
-   <span class="methodname">DOMDocument::createCDATASection</span>
-   <span class="methodname">DOMDocument::createComment</span>
-   <span class="methodname">DOMDocument::createDocumentFragment</span>
-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>
-   <span class="methodname">DOMDocument::createEntityReference</span>
-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>

DOMDocument::getElementById
===========================

Searches for an element with a certain id

### 说明

<span class="modifier">public</span> <span
class="type">DOMElement</span> <span
class="methodname">DOMDocument::getElementById</span> ( <span
class="methodparam"><span class="type">string</span> `$elementId`</span>
)

This function is similar to
<a href="/class/domdocument.html#DOMDocument::getElementsByTagName" class="xref"></a>
but searches for an element with a given id.

For this function to work, you will need either to set some ID
attributes with
<a href="/class/domelement.html#DOMElement::setIdAttribute" class="xref"></a>
or a DTD which defines an attribute to be of type ID. In the later case,
you will need to validate your document with
<a href="/class/domdocument.html#DOMDocument::validate" class="xref"></a>
or
<a href="/class/domdocument.html#" class="link">DOMDocument::$validateOnParse</a>
before using this function.

### 参数

`elementId`  
The unique id value for an element.

### 返回值

Returns the <span class="classname">DOMElement</span> or **`NULL`** if
the element is not found.

### 范例

**示例 \#1 DOMDocument::getElementById() Example**

以下范例使用了 `book.xml`，其内容如下：

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE books [
  <!ELEMENT books   (book+)>
  <!ELEMENT book    (title, author+, xhtml:blurb?)>
  <!ELEMENT title   (#PCDATA)>
  <!ELEMENT blurb   (#PCDATA)>
  <!ELEMENT author  (#PCDATA)>
  <!ATTLIST books   xmlns        CDATA  #IMPLIED>
  <!ATTLIST books   xmlns:xhtml  CDATA  #IMPLIED>
  <!ATTLIST book    id           ID     #IMPLIED>
  <!ATTLIST author  email        CDATA  #IMPLIED>
]>
<?xml-stylesheet type="text/xsl" href="style.xsl"?>
<books xmlns="http://books.php/" xmlns:xhtml="http://www.w3.org/1999/xhtml">
  <book id="php-basics">
    <title>PHP Basics</title>
    <author email="jim.smith@basics.php">Jim Smith</author>
    <author email="jane.smith@basics.php">Jane Smith</author>
    <xhtml:blurb><![CDATA[
<p><em>PHP Basics</em> provides an introduction to PHP.</p>
]]></xhtml:blurb>
  </book>
  <book id="php-advanced">
    <title>PHP Advanced Programming</title>
    <author email="jon.doe@advanced.php">Jon Doe</author>
  </book>
</books>
```

``` php
<?php

$doc = new DomDocument;

// We need to validate our document before referring to the id
$doc->validateOnParse = true;
$doc->Load('book.xml');

echo "The element whose id is 'php-basics' is: " . $doc->getElementById('php-basics')->tagName . "\n";

?>
```

以上例程会输出：

    The element whose id is 'php-basics' is: book 

### 参见

-   <span class="methodname">DOMDocument::getElementsByTagName</span>

DOMDocument::getElementsByTagName
=================================

Searches for all elements with given local tag name

### 说明

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">DOMDocument::getElementsByTagName</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

This function returns a new instance of class <span
class="classname">DOMNodeList</span> containing all the elements with a
given local tag name.

### 参数

`name`  
The local name (without namespace) of the tag to match on. The special
value *\** matches all tags.

### 返回值

A new <span class="classname">DOMNodeList</span> object containing all
the matched elements.

### 范例

**示例 \#1 Basic Usage Example**

``` php
<?php
$xml = <<< XML
<?xml version="1.0" encoding="utf-8"?>
<books>
 <book>Patterns of Enterprise Application Architecture</book>
 <book>Design Patterns: Elements of Reusable Software Design</book>
 <book>Clean Code</book>
</books>
XML;

$dom = new DOMDocument;
$dom->loadXML($xml);
$books = $dom->getElementsByTagName('book');
foreach ($books as $book) {
    echo $book->nodeValue, PHP_EOL;
}
?>
```

以上例程会输出：

    Patterns of Enterprise Application Architecture
    Design Patterns: Elements of Reusable Software Design
    Clean Code

### 参见

-   <span class="methodname">DOMDocument::getElementsByTagNameNS</span>

DOMDocument::getElementsByTagNameNS
===================================

Searches for all elements with given tag name in specified namespace

### 说明

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">DOMDocument::getElementsByTagNameNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

Returns a <span class="classname">DOMNodeList</span> of all elements
with a given local name and a namespace URI.

### 参数

`namespaceURI`  
The namespace URI of the elements to match on. The special value *\**
matches all namespaces.

`localName`  
The local name of the elements to match on. The special value *\**
matches all local names.

### 返回值

A new <span class="classname">DOMNodeList</span> object containing all
the matched elements.

### 范例

**示例 \#1 Get all the XInclude elements**

``` php
<?php

$xml = <<<EOD
<?xml version="1.0" ?>
<chapter xmlns:xi="http://www.w3.org/2001/XInclude">
<title>Books of the other guy..</title>
<para>
 <xi:include href="book.xml">
  <xi:fallback>
   <error>xinclude: book.xml not found</error>
  </xi:fallback>
 </xi:include>
 <include>
  This is another namespace
 </include>
</para>
</chapter>
EOD;
$dom = new DOMDocument;

// load the XML string defined above
$dom->loadXML($xml);

foreach ($dom->getElementsByTagNameNS('http://www.w3.org/2001/XInclude', '*') as $element) {
    echo 'local name: ', $element->localName, ', prefix: ', $element->prefix, "\n";
}
?>
```

以上例程会输出：

    local name: include, prefix: xi
    local name: fallback, prefix: xi

### 参见

-   <span class="methodname">DOMDocument::getElementsByTagName</span>

DOMDocument::importNode
=======================

Import node into current document

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMDocument::importNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span>
`$importedNode`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$deep`<span class="initializer"> =
**`FALSE`**</span></span> \] )

This function returns a copy of the node to import and associates it
with the current document.

### 参数

`importedNode`  
The node to import.

`deep`  
If set to **`TRUE`**, this method will recursively import the subtree
under the `importedNode`.

> **Note**:
>
> To copy the nodes attributes `deep` needs to be set to **`TRUE`**

### 返回值

The copied node or **`FALSE`**, if it cannot be copied.

### 错误／异常

<span class="classname">DOMException</span> is thrown if node cannot be
imported.

### 范例

**示例 \#1 <span class="function">DOMDocument::importNode</span>
example**

Copying nodes between documents.

``` php
<?php

$orgdoc = new DOMDocument;
$orgdoc->loadXML("<root><element><child>text in child</child></element></root>");

// The node we want to import to a new document
$node = $orgdoc->getElementsByTagName("element")->item(0);


// Create a new document
$newdoc = new DOMDocument;
$newdoc->formatOutput = true;

// Add some markup
$newdoc->loadXML("<root><someelement>text in some element</someelement></root>");

echo "The 'new document' before copying nodes into it:\n";
echo $newdoc->saveXML();

// Import the node, and all its children, to the document
$node = $newdoc->importNode($node, true);
// And then append it to the "<root>" node
$newdoc->documentElement->appendChild($node);

echo "\nThe 'new document' after copying the nodes into it:\n";
echo $newdoc->saveXML();
?>
```

以上例程会输出：

    The 'new document' before copying nodes into it:
    <?xml version="1.0"?>
    <root>
      <someelement>text in some element</someelement>
    </root>

    The 'new document' after copying the nodes into it:
    <?xml version="1.0"?>
    <root>
      <someelement>text in some element</someelement>
      <element>
        <child>text in child</child>
      </element>
    </root>

DOMDocument::load
=================

Load XML from a file

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">DOMDocument::load</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Loads an XML document from a file.

**Warning**

Unix style paths with forward slashes can cause significant performance
degradation on Windows systems; be sure to call <span
class="function">realpath</span> in such a case.

### 参数

`filename`  
The path to the XML document.

`options`  
<a href="/language/operators/bitwise.html" class="link">Bitwise <em>OR</em></a>
of the
<a href="/libxml/constants.html" class="link">libxml option constants</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If called
statically, returns a <span class="classname">DOMDocument</span>
或者在失败时返回 **`FALSE`**.

### 错误／异常

If an empty string is passed as the `filename` or an empty file is
named, a warning will be generated. This warning is not generated by
libxml and cannot be handled using libxml's error handling functions.

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 范例

**示例 \#1 Creating a Document**

``` php
<?php
$doc = new DOMDocument();
$doc->load('book.xml');
echo $doc->saveXML();
?>
```

### 参见

-   <span class="methodname">DOMDocument::loadXML</span>
-   <span class="methodname">DOMDocument::save</span>
-   <span class="methodname">DOMDocument::saveXML</span>

DOMDocument::loadHTML
=====================

Load HTML from a string

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::loadHTML</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

The function parses the HTML contained in the string `source`. Unlike
loading XML, HTML does not have to be well-formed to load. This function
may also be called statically to load and create a <span
class="classname">DOMDocument</span> object. The static invocation may
be used when no <span class="classname">DOMDocument</span> properties
need to be set prior to loading.

### 参数

`source`  
The HTML string.

`options`  
Since PHP 5.4.0 and Libxml 2.6.0, you may also use the `options`
parameter to specify
<a href="/libxml/constants.html" class="link">additional Libxml parameters</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If called
statically, returns a <span class="classname">DOMDocument</span>
或者在失败时返回 **`FALSE`**.

### 错误／异常

If an empty string is passed as the `source`, a warning will be
generated. This warning is not generated by libxml and cannot be handled
using libxml's error handling functions.

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

尽管非正确格式化的 HTML 仍应该被成功调入，但此函数会在遇到错误标记时产生
**`E_WARNING`**
错误。<a href="/ref/libxml.html#libxml_use_internal_errors" class="link">libxml 错误处理函数</a>可以用来处理这类错误。

### 范例

**示例 \#1 Creating a Document**

``` php
<?php
$doc = new DOMDocument();
$doc->loadHTML("<html><body>Test<br></body></html>");
echo $doc->saveHTML();
?>
```

### 参见

-   <span class="methodname">DOMDocument::loadHTMLFile</span>
-   <span class="methodname">DOMDocument::saveHTML</span>
-   <span class="methodname">DOMDocument::saveHTMLFile</span>

DOMDocument::loadHTMLFile
=========================

Load HTML from a file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::loadHTMLFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

The function parses the HTML document in the file named `filename`.
Unlike loading XML, HTML does not have to be well-formed to load.

### 参数

`filename`  
The path to the HTML file.

`options`  
Since PHP 5.4.0 and Libxml 2.6.0, you may also use the `options`
parameter to specify
<a href="/libxml/constants.html" class="link">additional Libxml parameters</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If called
statically, returns a <span class="classname">DOMDocument</span>
或者在失败时返回 **`FALSE`**.

### 错误／异常

If an empty string is passed as the `filename` or an empty file is
named, a warning will be generated. This warning is not generated by
libxml and cannot be handled using
<a href="/ref/libxml.html#libxml_use_internal_errors" class="link">libxml's error handling functions</a>.

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

尽管非正确格式化的 HTML 仍应该被成功调入，但此函数会在遇到错误标记时产生
**`E_WARNING`**
错误。<a href="/ref/libxml.html#libxml_use_internal_errors" class="link">libxml 错误处理函数</a>可以用来处理这类错误。

### 范例

**示例 \#1 Creating a Document**

``` php
<?php
$doc = new DOMDocument();
$doc->loadHTMLFile("filename.html");
echo $doc->saveHTML();
?>
```

### 参见

-   <span class="methodname">DOMDocument::loadHTML</span>
-   <span class="methodname">DOMDocument::saveHTML</span>
-   <span class="methodname">DOMDocument::saveHTMLFile</span>

DOMDocument::loadXML
====================

Load XML from a string

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">DOMDocument::loadXML</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Loads an XML document from a string.

### 参数

`source`  
The string containing the XML.

`options`  
<a href="/language/operators/bitwise.html" class="link">Bitwise <em>OR</em></a>
of the
<a href="/libxml/constants.html" class="link">libxml option constants</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If called
statically, returns a <span class="classname">DOMDocument</span>
或者在失败时返回 **`FALSE`**.

### 错误／异常

If an empty string is passed as the `source`, a warning will be
generated. This warning is not generated by libxml and cannot be handled
using libxml's error handling functions.

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 范例

**示例 \#1 Creating a Document**

``` php
<?php
$doc = new DOMDocument();
$doc->loadXML('<root><node/></root>');
echo $doc->saveXML();
?>
```

**示例 \#2 Static invocation of *loadXML***

``` php
<?php
// Issues an E_STRICT error
$doc = DOMDocument::loadXML('<root><node/></root>');
echo $doc->saveXML();
?>
```

### 参见

-   <span class="methodname">DOMDocument::load</span>
-   <span class="methodname">DOMDocument::save</span>
-   <span class="methodname">DOMDocument::saveXML</span>

DOMDocument::normalizeDocument
==============================

Normalizes the document

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMDocument::normalizeDocument</span> ( <span
class="methodparam">void</span> )

This method acts as if you saved and then loaded the document, putting
the document in a "normal" form.

### 返回值

没有返回值。

### 参见

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-Document3-normalizeDocument" class="link external">» The DOM Specification</a>
-   <span class="methodname">DOMNode::normalize</span>

DOMDocument::registerNodeClass
==============================

Register extended class used to create base node type

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::registerNodeClass</span> ( <span
class="methodparam"><span class="type">string</span> `$baseclass`</span>
, <span class="methodparam"><span class="type">string</span>
`$extendedclass`</span> )

This method allows you to register your own extended DOM class to be
used afterward by the PHP DOM extension.

This method is not part of the DOM standard.

### 参数

`baseclass`  
The DOM class that you want to extend. You can find a list of these
classes in the
<a href="/book/dom.html" class="link">chapter introduction</a>.

`extendedclass`  
Your extended class name. If **`NULL`** is provided, any previously
registered class extending `baseclass` will be removed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Adding a new method to DOMElement to ease our code**

``` php
<?php

class myElement extends DOMElement {
   function appendElement($name) { 
      return $this->appendChild(new myElement($name));
   }
}

class myDocument extends DOMDocument {
   function setRoot($name) { 
      return $this->appendChild(new myElement($name));
   }
}

$doc = new myDocument();
$doc->registerNodeClass('DOMElement', 'myElement');

// From now on, adding an element to another costs only one method call ! 
$root = $doc->setRoot('root');
$child = $root->appendElement('child');
$child->setAttribute('foo', 'bar');

echo $doc->saveXML();

?>
```

以上例程会输出：

    <?xml version="1.0"?>
    <root><child foo="bar"/></root>

**示例 \#2 Retrieving elements as custom class**

``` php
<?php
class myElement extends DOMElement {
    public function __toString() {
        return $this->nodeValue;
    }
}

$doc = new DOMDocument;
$doc->loadXML("<root><element><child>text in child</child></element></root>");
$doc->registerNodeClass("DOMElement", "myElement");

$element = $doc->getElementsByTagName("child")->item(0);
var_dump(get_class($element));

// And take advantage of the __toString method..
echo $element;
?>
```

以上例程会输出：

    string(9) "myElement"
    text in child

**示例 \#3 Retrieving owner document**

When instantiating a custom <span class="classname">DOMDocument</span>
the `ownerDocument` property will refer to the instantiated class,
meaning there is no need (and in fact not possible) to use <span
class="function">DOMDocument::registerNodeClass</span> with <span
class="classname">DOMDocument</span>

``` php
<?php
class myDOMDocument extends DOMDocument {
}

class myOtherDOMDocument extends DOMDocument {
}

// Create myDOMDocument with some XML
$doc = new myDOMDocument;
$doc->loadXML("<root><element><child>text in child</child></element></root>");

$child = $doc->getElementsByTagName("child")->item(0);

// The current owner of the node is myDOMDocument
var_dump(get_class($child->ownerDocument));

// Import a node from myDOMDocument
$newdoc = new myOtherDOMDocument;
$child = $newdoc->importNode($child);

// The new owner of the node has changed to myOtherDOMDocument
var_dump(get_class($child->ownerDocument));
?>
```

以上例程会输出：

    string(13) "myDOMDocument"
    string(18) "myOtherDOMDocument"

DOMDocument::relaxNGValidate
============================

Performs relaxNG validation on the document

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::relaxNGValidate</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Performs
<a href="http://www.relaxng.org/" class="link external">» relaxNG</a>
validation on the document based on the given RNG schema.

### 参数

`filename`  
The RNG file.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMDocument::relaxNGValidateSource</span>
-   <span class="methodname">DOMDocument::schemaValidate</span>
-   <span class="methodname">DOMDocument::schemaValidateSource</span>
-   <span class="methodname">DOMDocument::validate</span>

DOMDocument::relaxNGValidateSource
==================================

Performs relaxNG validation on the document

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::relaxNGValidateSource</span> (
<span class="methodparam"><span class="type">string</span>
`$source`</span> )

Performs
<a href="http://www.relaxng.org/" class="link external">» relaxNG</a>
validation on the document based on the given RNG source.

### 参数

`source`  
A string containing the RNG schema.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMDocument::relaxNGValidate</span>
-   <span class="methodname">DOMDocument::schemaValidate</span>
-   <span class="methodname">DOMDocument::schemaValidateSource</span>
-   <span class="methodname">DOMDocument::validate</span>

DOMDocument::save
=================

Dumps the internal XML tree back into a file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMDocument::save</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = 0</span></span> \] )

Creates an XML document from the DOM representation. This function is
usually called after building a new dom document from scratch as in the
example below.

### 参数

`filename`  
The path to the saved XML document.

`options`  
Additional Options. Currently only
<a href="/libxml/constants.html" class="link">LIBXML_NOEMPTYTAG</a> is
supported.

### 返回值

Returns the number of bytes written or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 Saving a DOM tree into a file**

``` php
<?php

$doc = new DOMDocument('1.0');
// we want a nice output
$doc->formatOutput = true;

$root = $doc->createElement('book');
$root = $doc->appendChild($root);

$title = $doc->createElement('title');
$title = $root->appendChild($title);

$text = $doc->createTextNode('This is the title');
$text = $title->appendChild($text);

echo 'Wrote: ' . $doc->save("/tmp/test.xml") . ' bytes'; // Wrote: 72 bytes

?>
```

### 参见

-   <span class="methodname">DOMDocument::saveXML</span>
-   <span class="methodname">DOMDocument::load</span>
-   <span class="methodname">DOMDocument::loadXML</span>

DOMDocument::saveHTML
=====================

Dumps the internal document into a string using HTML formatting

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMDocument::saveHTML</span> (\[ <span
class="methodparam"><span class="type">DOMNode</span> `$node`<span
class="initializer"> = NULL</span></span> \] )

Creates an HTML document from the DOM representation. This function is
usually called after building a new dom document from scratch as in the
example below.

### 参数

`node`  
Optional parameter to output a subset of the document.

### 返回值

Returns the HTML, or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 Saving a HTML tree into a string**

``` php
<?php

$doc = new DOMDocument('1.0');

$root = $doc->createElement('html');
$root = $doc->appendChild($root);

$head = $doc->createElement('head');
$head = $root->appendChild($head);

$title = $doc->createElement('title');
$title = $head->appendChild($title);

$text = $doc->createTextNode('This is the title');
$text = $title->appendChild($text);

echo $doc->saveHTML();

?>
```

### 参见

-   <span class="methodname">DOMDocument::saveHTMLFile</span>
-   <span class="methodname">DOMDocument::loadHTML</span>
-   <span class="methodname">DOMDocument::loadHTMLFile</span>

DOMDocument::saveHTMLFile
=========================

Dumps the internal document into a file using HTML formatting

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMDocument::saveHTMLFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Creates an HTML document from the DOM representation. This function is
usually called after building a new dom document from scratch as in the
example below.

### 参数

`filename`  
The path to the saved HTML document.

### 返回值

Returns the number of bytes written or **`FALSE`** if an error occurred.

### 范例

**示例 \#1 Saving a HTML tree into a file**

``` php
<?php

$doc = new DOMDocument('1.0');
// we want a nice output
$doc->formatOutput = true;

$root = $doc->createElement('html');
$root = $doc->appendChild($root);

$head = $doc->createElement('head');
$head = $root->appendChild($head);

$title = $doc->createElement('title');
$title = $head->appendChild($title);

$text = $doc->createTextNode('This is the title');
$text = $title->appendChild($text);

echo 'Wrote: ' . $doc->saveHTMLFile("/tmp/test.html") . ' bytes'; // Wrote: 129 bytes

?>
```

### 参见

-   <span class="methodname">DOMDocument::saveHTML</span>
-   <span class="methodname">DOMDocument::loadHTML</span>
-   <span class="methodname">DOMDocument::loadHTMLFile</span>

DOMDocument::saveXML
====================

Dumps the internal XML tree back into a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMDocument::saveXML</span> (\[ <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \]\] )

Creates an XML document from the DOM representation. This function is
usually called after building a new dom document from scratch as in the
example below.

### 参数

`node`  
Use this parameter to output only a specific node without XML
declaration rather than the entire document.

`options`  
Additional Options. Currently only
<a href="/libxml/constants.html" class="link">LIBXML_NOEMPTYTAG</a> is
supported.

### 返回值

Returns the XML, or **`FALSE`** if an error occurred.

### 错误／异常

**`DOM_WRONG_DOCUMENT_ERR`**  
Raised if `node` is from another document.

### 范例

**示例 \#1 Saving a DOM tree into a string**

``` php
<?php

$doc = new DOMDocument('1.0');
// we want a nice output
$doc->formatOutput = true;

$root = $doc->createElement('book');
$root = $doc->appendChild($root);

$title = $doc->createElement('title');
$title = $root->appendChild($title);

$text = $doc->createTextNode('This is the title');
$text = $title->appendChild($text);

echo "Saving all the document:\n";
echo $doc->saveXML() . "\n";

echo "Saving only the title part:\n";
echo $doc->saveXML($title);

?>
```

以上例程会输出：

    Saving all the document:
    <?xml version="1.0"?>
    <book>
      <title>This is the title</title>
    </book>

    Saving only the title part:
    <title>This is the title</title>

### 参见

-   <span class="methodname">DOMDocument::save</span>
-   <span class="methodname">DOMDocument::load</span>
-   <span class="methodname">DOMDocument::loadXML</span>

DOMDocument::schemaValidate
===========================

Validates a document based on a schema

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::schemaValidate</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = 0</span></span> \] )

Validates a document based on the given schema file.

### 参数

`filename`  
The path to the schema.

`flags`  
A bitmask of Libxml schema validation flags. Currently the only
supported value is
<a href="/libxml/constants.html" class="link">LIBXML_SCHEMA_CREATE</a>.
Available since PHP 5.5.2 and Libxml 2.6.14.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                        |
|-------|-----------------------------|
| 5.5.2 | Added the `flags` parameter |

### 参见

-   <span class="methodname">DOMDocument::schemaValidateSource</span>
-   <span class="methodname">DOMDocument::relaxNGValidate</span>
-   <span class="methodname">DOMDocument::relaxNGValidateSource</span>
-   <span class="methodname">DOMDocument::validate</span>

DOMDocument::schemaValidateSource
=================================

Validates a document based on a schema

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::schemaValidateSource</span> (
<span class="methodparam"><span class="type">string</span>
`$source`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`</span> \] )

Validates a document based on a schema defined in the given string.

### 参数

`source`  
A string containing the schema.

`flags`  
A bitmask of Libxml schema validation flags. Currently the only
supported value is
<a href="/libxml/constants.html" class="link">LIBXML_SCHEMA_CREATE</a>.
Available since PHP 5.5.2 and Libxml 2.6.14.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                        |
|-------|-----------------------------|
| 5.5.2 | Added the `flags` parameter |

### 参见

-   <span class="methodname">DOMDocument::schemaValidate</span>
-   <span class="methodname">DOMDocument::relaxNGValidate</span>
-   <span class="methodname">DOMDocument::relaxNGValidateSource</span>
-   <span class="methodname">DOMDocument::validate</span>

DOMDocument::validate
=====================

Validates the document based on its DTD

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocument::validate</span> ( <span
class="methodparam">void</span> )

Validates the document based on its DTD.

You can also use the *validateOnParse* property of <span
class="classname">DOMDocument</span> to make a DTD validation.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 If the document
has no DTD attached, this method will return **`FALSE`**.

### 范例

**示例 \#1 Example of DTD validation**

``` php
<?php
$dom = new DOMDocument;
$dom->load('book.xml');
if ($dom->validate()) {
    echo "This document is valid!\n";
}
?>
```

You can also validate your XML file while loading it:

``` php
<?php
$dom = new DOMDocument;
$dom->validateOnParse = true;
$dom->load('book.xml');
?>
```

### 参见

-   <span class="methodname">DOMDocument::schemaValidate</span>
-   <span class="methodname">DOMDocument::schemaValidateSource</span>
-   <span class="methodname">DOMDocument::relaxNGValidate</span>
-   <span class="methodname">DOMDocument::relaxNGValidateSource</span>

DOMDocument::xinclude
=====================

Substitutes XIncludes in a DOMDocument Object

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMDocument::xinclude</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

This method substitutes
<a href="http://www.w3.org/TR/xinclude/" class="link external">» XIncludes</a>
in a DOMDocument object.

> **Note**:
>
> Due to libxml2 automatically resolving entities, this method will
> produce unexpected results if the included XML file have an attached
> DTD.

### 参数

`options`  
<a href="/libxml/constants.html" class="link">libxml parameters</a>.
Available since PHP 5.1.0 and Libxml 2.6.7.

### 返回值

Returns the number of XIncludes in the document, -1 if some processing
failed, or **`FALSE`** if there were no substitutions.

### 范例

**示例 \#1 DOMDocument::xinclude() example**

``` php
<?php

$xml = <<<EOD
<?xml version="1.0" ?>
<chapter xmlns:xi="http://www.w3.org/2001/XInclude">
 <title>Books of the other guy..</title>
 <para>
  <xi:include href="book.xml">
   <xi:fallback>
    <error>xinclude: book.xml not found</error>
   </xi:fallback>
  </xi:include>
 </para>
</chapter>
EOD;

$dom = new DOMDocument;

// let's have a nice output
$dom->preserveWhiteSpace = false;
$dom->formatOutput = true;

// load the XML string defined above
$dom->loadXML($xml);

// substitute xincludes
$dom->xinclude();

echo $dom->saveXML();

?>
```

以上例程的输出类似于：

    <?xml version="1.0"?>
    <chapter xmlns:xi="http://www.w3.org/2001/XInclude">
      <title>Books of the other guy..</title>
      <para>
        <row xml:base="/home/didou/book.xml">
           <entry>The Grapes of Wrath</entry>
           <entry>John Steinbeck</entry>
           <entry>en</entry>
           <entry>0140186409</entry>
          </row>
        <row xml:base="/home/didou/book.xml">
           <entry>The Pearl</entry>
           <entry>John Steinbeck</entry>
           <entry>en</entry>
           <entry>014017737X</entry>
          </row>
        <row xml:base="/home/didou/book.xml">
           <entry>Samarcande</entry>
           <entry>Amine Maalouf</entry>
           <entry>fr</entry>
           <entry>2253051209</entry>
          </row>
      </para>
    </chapter>

类摘要
------

**DOMDocumentFragment**

<span class="ooclass"> class **DOMDocumentFragment** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">appendXML</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

DOMDocumentFragment::appendXML
==============================

Append raw XML data

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMDocumentFragment::appendXML</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Appends raw XML data to a DOMDocumentFragment.

This method is not part of the DOM standard. It was created as a simpler
approach for appending an XML DocumentFragment in a DOMDocument.

If you want to stick to the standards, you will have to create a
temporary DOMDocument with a dummy root and then loop through the child
nodes of the root of your XML data to append them.

### 参数

`data`  
XML to append.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Appending XML data to your document**

``` php
<?php
$doc = new DOMDocument();
$doc->loadXML("<root/>");
$f = $doc->createDocumentFragment();
$f->appendXML("<foo>text</foo><bar>text2</bar>");
$doc->documentElement->appendChild($f);
echo $doc->saveXML(); 
?>
```

以上例程会输出：

    <?xml version="1.0"?>
    <root><foo>text</foo><bar>text2</bar></root>

简介
----

Each <span class="classname">DOMDocument</span> has a *doctype*
attribute whose value is either **`NULL`** or a <span
class="classname">DOMDocumentType</span> object.

类摘要
------

**DOMDocumentType**

<span class="ooclass"> class **DOMDocumentType** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$publicId` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$systemId` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$name` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$entities` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$notations` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$internalSubset` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`publicId`  
The public identifier of the external subset.

`systemId`  
The system identifier of the external subset. This may be an absolute
URI or not.

`name`  
The name of DTD; i.e., the name immediately following the *DOCTYPE*
keyword.

`entities`  
A <span class="classname">DOMNamedNodeMap</span> containing the general
entities, both external and internal, declared in the DTD.

`notations`  
A <span class="classname">DOMNamedNodeMap</span> containing the
notations declared in the DTD.

`internalSubset`  
The internal subset as a string, or null if there is none. This does not
contain the delimiting square brackets.

类摘要
------

**DOMElement**

<span class="ooclass"> class **DOMElement** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$schemaTypeInfo` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$tagName` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespaceURI`</span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">getAttributeNode</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">getAttributeNodeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">getElementsByTagName</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">getElementsByTagNameNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">removeAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">removeAttributeNode</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">removeAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">setAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">setAttributeNode</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$attr`</span> )

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">setAttributeNodeNS</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$attr`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifiedName`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setIdAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">bool</span> `$isId`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setIdAttributeNode</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$attr`</span> ,
<span class="methodparam"><span class="type">bool</span> `$isId`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setIdAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> , <span
class="methodparam"><span class="type">bool</span> `$isId`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`schemaTypeInfo`  
Not implemented yet, always return **`NULL`**

`tagName`  
The element name

注释
----

> **Note**:
>
> 此 DOM 扩展采用 UTF-8 编码。在 ISO-8859-1 编码下，使用 <span
> class="function">utf8\_encode</span> 和 <span
> class="function">utf8\_decode</span> 来处理，其它编码下使用
> <a href="/ref/iconv.html" class="link">iconv</a> 函数处理。

DOMElement::\_\_construct
=========================

Creates a new DOMElement object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMElement::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$namespaceURI`</span> \]\] )

Creates a new <span class="classname">DOMElement</span> object. This
object is read only. It may be appended to a document, but additional
nodes may not be appended to this node until the node is associated with
a document. To create a writeable node, use
<a href="/class/domdocument.html#DOMDocument::createElement" class="xref"></a>
or
<a href="/class/domdocument.html#DOMDocument::createElementNS" class="xref"></a>.

### 参数

`name`  
The tag name of the element. When also passing in namespaceURI, the
element name may take a prefix to be associated with the URI.

`value`  
The value of the element.

`namespaceURI`  
A namespace URI to create the element within a specific namespace.

### 范例

**示例 \#1 Creating a new DOMElement**

``` php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$element_ns = new DOMElement('pr:node1', 'thisvalue', 'http://xyz');
$element->appendChild($element_ns);
echo $dom->saveXML(); /* <?xml version="1.0" encoding="utf-8"?>
<root><pr:node1 xmlns:pr="http://xyz">thisvalue</pr:node1></root> */

?>
```

### 参见

-   <span class="methodname">DOMDocument::createElement</span>
-   <span class="methodname">DOMDocument::createElementNS</span>

DOMElement::getAttribute
========================

Returns value of attribute

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMElement::getAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Gets the value of the attribute with name `name` for the current node.

### 参数

`name`  
The name of the attribute.

### 返回值

The value of the attribute, or an empty string if no attribute with the
given `name` is found.

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::setAttribute</span>
-   <span class="methodname">DOMElement::removeAttribute</span>

DOMElement::getAttributeNode
============================

Returns attribute node

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMElement::getAttributeNode</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Returns the attribute node with name `name` for the current element.

### 参数

`name`  
The name of the attribute.

### 返回值

The attribute node. Note that for XML namespace declarations (*xmlns*
and *xmlns:\** attributes) an instance of <span
class="classname">DOMNameSpaceNode</span> is returned instead of a <span
class="classname">DOMAttr</span>.

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::setAttributeNode</span>
-   <span class="methodname">DOMElement::removeAttributeNode</span>

DOMElement::getAttributeNodeNS
==============================

Returns attribute node

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMElement::getAttributeNodeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

Returns the attribute node in namespace `namespaceURI` with local name
`localName` for the current node.

### 参数

`namespaceURI`  
The namespace URI.

`localName`  
The local name.

### 返回值

The attribute node. Note that for XML namespace declarations (*xmlns*
and *xmlns:\** attributes) an instance of <span
class="classname">DOMNameSpaceNode</span> is returned instead of a <span
class="classname">DOMAttr</span> object.

### 参见

-   <span class="methodname">DOMElement::hasAttributeNS</span>
-   <span class="methodname">DOMElement::setAttributeNodeNS</span>
-   <span class="methodname">DOMElement::removeAttributeNode</span>

DOMElement::getAttributeNS
==========================

Returns value of attribute

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMElement::getAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

Gets the value of the attribute in namespace `namespaceURI` with local
name `localName` for the current node.

### 参数

`namespaceURI`  
The namespace URI.

`localName`  
The local name.

### 返回值

The value of the attribute, or an empty string if no attribute with the
given `localName` and `namespaceURI` is found.

### 参见

-   <span class="methodname">DOMElement::hasAttributeNS</span>
-   <span class="methodname">DOMElement::setAttributeNS</span>
-   <span class="methodname">DOMElement::removeAttributeNS</span>

DOMElement::getElementsByTagName
================================

Gets elements by tagname

### 说明

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">DOMElement::getElementsByTagName</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

This function returns a new instance of the class <span
class="classname">DOMNodeList</span> of all descendant elements with a
given tag `name`, in the order in which they are encountered in a
preorder traversal of this element tree.

### 参数

`name`  
The tag name. Use *\** to return all elements within the element tree.

### 返回值

This function returns a new instance of the class <span
class="classname">DOMNodeList</span> of all matched elements.

### 参见

-   <span class="methodname">DOMElement::getElementsByTagNameNS</span>

DOMElement::getElementsByTagNameNS
==================================

Get elements by namespaceURI and localName

### 说明

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">DOMElement::getElementsByTagNameNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

This function fetch all the descendant elements with a given `localName`
and `namespaceURI`.

### 参数

`namespaceURI`  
The namespace URI.

`localName`  
The local name. Use *\** to return all elements within the element tree.

### 返回值

This function returns a new instance of the class <span
class="classname">DOMNodeList</span> of all matched elements in the
order in which they are encountered in a preorder traversal of this
element tree.

### 参见

-   <span class="methodname">DOMElement::getElementsByTagName</span>

DOMElement::hasAttribute
========================

Checks to see if attribute exists

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMElement::hasAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Indicates whether attribute named `name` exists as a member of the
element.

### 参数

`name`  
The attribute name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMElement::hasAttributeNS</span>
-   <span class="methodname">DOMElement::getAttribute</span>
-   <span class="methodname">DOMElement::setAttribute</span>
-   <span class="methodname">DOMElement::removeAttribute</span>

DOMElement::hasAttributeNS
==========================

Checks to see if attribute exists

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMElement::hasAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

Indicates whether attribute in namespace `namespaceURI` named
`localName` exists as a member of the element.

### 参数

`namespaceURI`  
The namespace URI.

`localName`  
The local name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::getAttributeNS</span>
-   <span class="methodname">DOMElement::setAttributeNS</span>
-   <span class="methodname">DOMElement::removeAttributeNS</span>

DOMElement::removeAttribute
===========================

Removes attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMElement::removeAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Removes attribute named `name` from the element.

### 参数

`name`  
The name of the attribute.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::getAttribute</span>
-   <span class="methodname">DOMElement::setAttribute</span>

DOMElement::removeAttributeNode
===============================

Removes attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMElement::removeAttributeNode</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$oldnode`</span>
)

Removes attribute `oldnode` from the element.

### 参数

`oldnode`  
The attribute node.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

**`DOM_NOT_FOUND_ERROR`**  
Raised if `oldnode` is not an attribute of the element.

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::getAttributeNode</span>
-   <span class="methodname">DOMElement::setAttributeNode</span>

DOMElement::removeAttributeNS
=============================

Removes attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMElement::removeAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

Removes attribute `localName` in namespace `namespaceURI` from the
element.

### 参数

`namespaceURI`  
The namespace URI.

`localName`  
The local name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

### 参见

-   <span class="methodname">DOMElement::hasAttributeNS</span>
-   <span class="methodname">DOMElement::getAttributeNS</span>
-   <span class="methodname">DOMElement::setAttributeNS</span>

DOMElement::setAttribute
========================

Adds new attribute

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMElement::setAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

Sets an attribute with name `name` to the given value. If the attribute
does not exist, it will be created.

### 参数

`name`  
The name of the attribute.

`value`  
The value of the attribute.

### 返回值

The new <span class="classname">DOMAttr</span> or **`FALSE`** if an
error occurred.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

### 范例

**示例 \#1 Setting an attribute**

``` php
<?php
$doc = new DOMDocument("1.0");
$node = $doc->createElement("para");
$newnode = $doc->appendChild($node);
$newnode->setAttribute("align", "left");
?>
```

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::getAttribute</span>
-   <span class="methodname">DOMElement::removeAttribute</span>

DOMElement::setAttributeNode
============================

Adds new attribute node to element

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMElement::setAttributeNode</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$attr`</span> )

Adds new attribute node `attr` to element.

### 参数

`attr`  
The attribute node.

### 返回值

Returns old node if the attribute has been replaced or **`NULL`**.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

### 参见

-   <span class="methodname">DOMElement::hasAttribute</span>
-   <span class="methodname">DOMElement::getAttributeNode</span>
-   <span class="methodname">DOMElement::removeAttributeNode</span>

DOMElement::setAttributeNodeNS
==============================

Adds new attribute node to element

### 说明

<span class="modifier">public</span> <span class="type">DOMAttr</span>
<span class="methodname">DOMElement::setAttributeNodeNS</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$attr`</span> )

Adds new attribute node `attr` to element.

### 参数

`attr`  
The attribute node.

### 返回值

Returns the old node if the attribute has been replaced.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

### 参见

-   <span class="methodname">DOMElement::hasAttributeNS</span>
-   <span class="methodname">DOMElement::getAttributeNodeNS</span>
-   <span class="methodname">DOMElement::removeAttributeNode</span>

DOMElement::setAttributeNS
==========================

Adds new attribute

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMElement::setAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$qualifiedName`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

Sets an attribute with namespace `namespaceURI` and name `name` to the
given value. If the attribute does not exist, it will be created.

### 参数

`namespaceURI`  
The namespace URI.

`qualifiedName`  
The qualified name of the attribute, as *prefix:tagname*.

`value`  
The value of the attribute.

### 返回值

没有返回值。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

**`DOM_NAMESPACE_ERR`**  
Raised if `qualifiedName` is a malformed qualified name, or if
`qualifiedName` has a prefix and `namespaceURI` is **`NULL`**.

### 参见

-   <span class="methodname">DOMElement::hasAttributeNS</span>
-   <span class="methodname">DOMElement::getAttributeNS</span>
-   <span class="methodname">DOMElement::removeAttributeNS</span>

DOMElement::setIdAttribute
==========================

Declares the attribute specified by name to be of type ID

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMElement::setIdAttribute</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">bool</span> `$isId`</span>
)

Declares the attribute `name` to be of type ID.

### 参数

`name`  
The name of the attribute.

`isId`  
Set it to **`TRUE`** if you want `name` to be of type ID, **`FALSE`**
otherwise.

### 返回值

没有返回值。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

**`DOM_NOT_FOUND`**  
Raised if `name` is not an attribute of this element.

### 参见

-   <span class="methodname">DOMDocument::getElementById</span>
-   <span class="methodname">DOMElement::setIdAttributeNode</span>
-   <span class="methodname">DOMElement::setIdAttributeNS</span>

DOMElement::setIdAttributeNode
==============================

Declares the attribute specified by node to be of type ID

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMElement::setIdAttributeNode</span> ( <span
class="methodparam"><span class="type">DOMAttr</span> `$attr`</span> ,
<span class="methodparam"><span class="type">bool</span> `$isId`</span>
)

Declares the attribute specified by `attr` to be of type ID.

### 参数

`attr`  
The attribute node.

`isId`  
Set it to **`TRUE`** if you want `name` to be of type ID, **`FALSE`**
otherwise.

### 返回值

没有返回值。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

**`DOM_NOT_FOUND`**  
Raised if `name` is not an attribute of this element.

### 参见

-   <span class="methodname">DOMDocument::getElementById</span>
-   <span class="methodname">DOMElement::setIdAttribute</span>
-   <span class="methodname">DOMElement::setIdAttributeNS</span>

DOMElement::setIdAttributeNS
============================

Declares the attribute specified by local name and namespace URI to be
of type ID

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMElement::setIdAttributeNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> , <span
class="methodparam"><span class="type">bool</span> `$isId`</span> )

Declares the attribute specified by `localName` and `namespaceURI` to be
of type ID.

### 参数

`namespaceURI`  
The namespace URI of the attribute.

`localName`  
The local name of the attribute, as *prefix:tagname*.

`isId`  
Set it to **`TRUE`** if you want `name` to be of type ID, **`FALSE`**
otherwise.

### 返回值

没有返回值。

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if the node is readonly.

**`DOM_NOT_FOUND`**  
Raised if `name` is not an attribute of this element.

### 参见

-   <span class="methodname">DOMDocument::getElementById</span>
-   <span class="methodname">DOMElement::setIdAttribute</span>
-   <span class="methodname">DOMElement::setIdAttributeNode</span>

简介
----

This interface represents a known entity, either parsed or unparsed, in
an XML document.

类摘要
------

**DOMEntity**

<span class="ooclass"> class **DOMEntity** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$publicId` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$systemId` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$notationName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$actualEncoding` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$encoding` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$version` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`publicId`  
The public identifier associated with the entity if specified, and
**`NULL`** otherwise.

`systemId`  
The system identifier associated with the entity if specified, and
**`NULL`** otherwise. This may be an absolute URI or not.

`notationName`  
For unparsed entities, the name of the notation for the entity. For
parsed entities, this is **`NULL`**.

`actualEncoding`  
An attribute specifying the encoding used for this entity at the time of
parsing, when it is an external parsed entity. This is **`NULL`** if it
an entity from the internal subset or if it is not known.

`encoding`  
An attribute specifying, as part of the text declaration, the encoding
of this entity, when it is an external parsed entity. This is **`NULL`**
otherwise.

`version`  
An attribute specifying, as part of the text declaration, the version
number of this entity, when it is an external parsed entity. This is
**`NULL`** otherwise.

类摘要
------

**DOMEntityReference**

<span class="ooclass"> class **DOMEntityReference** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

DOMEntityReference::\_\_construct
=================================

Creates a new DOMEntityReference object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMEntityReference::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Creates a new <span class="classname">DOMEntityReference</span> object.

### 参数

`name`  
The name of the entity reference.

### 范例

**示例 \#1 Creating a new DOMEntityReference**

``` php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$entity = $element->appendChild(new DOMEntityReference('nbsp'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root>&nbsp;</root> */

?>
```

### 参见

-   <span class="methodname">DOMDocument::createEntityReference</span>

简介
----

DOM operations raise exceptions under particular circumstances, i.e.,
when an operation is impossible to perform for logical reasons.

See also <a href="/language/exceptions.html" class="xref">异常处理</a>.

类摘要
------

**DOMException**

<span class="ooclass"> class **DOMException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$code` ;

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

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
<span class="type">int</span> <span
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

属性
----

`code`  
An integer indicating the type of error generated

简介
----

The <span class="classname">DOMImplementation</span> class provides a
number of methods for performing operations that are independent of any
particular instance of the document object model.

类摘要
------

**DOMImplementation**

<span class="ooclass"> class **DOMImplementation** </span> {

/\* 属性 \*/

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">DOMDocument</span> <span
class="methodname">createDocument</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$qualifiedName`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">DOMDocumentType</span>
`$doctype`<span class="initializer"> = **`NULL`**</span></span> \]\]\] )

<span class="modifier">public</span> <span
class="type">DOMDocumentType</span> <span
class="methodname">createDocumentType</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$qualifiedName`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$publicId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$systemId`<span class="initializer"> = **`NULL`**</span></span> \]\]\]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasFeature</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

}

DOMImplementation::\_\_construct
================================

Creates a new DOMImplementation object

### 说明

<span class="methodname">DOMImplementation::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a new <span class="classname">DOMImplementation</span> object.

DOMImplementation::createDocument
=================================

Creates a DOMDocument object of the specified type with its document
element

### 说明

<span class="modifier">public</span> <span
class="type">DOMDocument</span> <span
class="methodname">DOMImplementation::createDocument</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$qualifiedName`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">DOMDocumentType</span>
`$doctype`<span class="initializer"> = **`NULL`**</span></span> \]\]\] )

Creates a <span class="classname">DOMDocument</span> object of the
specified type with its document element.

### 参数

`namespaceURI`  
The namespace URI of the document element to create.

`qualifiedName`  
The qualified name of the document element to create.

`doctype`  
The type of document to create or **`NULL`**.

### 返回值

A new <span class="classname">DOMDocument</span> object. If
`namespaceURI`, `qualifiedName`, and `doctype` are null, the returned
<span class="classname">DOMDocument</span> is empty with no document
element

### 错误／异常

**`DOM_WRONG_DOCUMENT_ERR`**  
Raised if `doctype` has already been used with a different document or
was created from a different implementation.

**`DOM_NAMESPACE_ERR`**  
Raised if there is an error with the namespace, as determined by
`namespaceURI` and `qualifiedName`.

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 参见

-   <span class="methodname">DOMDocument::\_\_construct</span>
-   <span
    class="methodname">DOMImplementation::createDocumentType</span>

DOMImplementation::createDocumentType
=====================================

Creates an empty DOMDocumentType object

### 说明

<span class="modifier">public</span> <span
class="type">DOMDocumentType</span> <span
class="methodname">DOMImplementation::createDocumentType</span> (\[
<span class="methodparam"><span class="type">string</span>
`$qualifiedName`<span class="initializer"> = **`NULL`**</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$publicId`<span class="initializer"> = **`NULL`**</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$systemId`<span class="initializer"> = **`NULL`**</span></span> \]\]\]
)

Creates an empty <span class="classname">DOMDocumentType</span> object.
Entity declarations and notations are not made available. Entity
reference expansions and default attribute additions do not occur.

### 参数

`qualifiedName`  
The qualified name of the document type to create.

`publicId`  
The external subset public identifier.

`systemId`  
The external subset system identifier.

### 返回值

A new <span class="classname">DOMDocumentType</span> node with its
*ownerDocument* set to **`NULL`**.

### 错误／异常

**`DOM_NAMESPACE_ERR`**  
Raised if there is an error with the namespace, as determined by
`qualifiedName`.

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 范例

**示例 \#1 Creating a document with an attached DTD**

``` php
<?php

// Creates an instance of the DOMImplementation class
$imp = new DOMImplementation;

// Creates a DOMDocumentType instance
$dtd = $imp->createDocumentType('graph', '', 'graph.dtd');

// Creates a DOMDocument instance
$dom = $imp->createDocument("", "", $dtd);

// Set other properties
$dom->encoding = 'UTF-8';
$dom->standalone = false;

// Create an empty element
$element = $dom->createElement('graph');

// Append the element
$dom->appendChild($element);

// Retrieve and print the document
echo $dom->saveXML();

?>
```

以上例程会输出：

    <?xml version="1.0" encoding="UTF-8" standalone="no"?>
    <!DOCTYPE graph SYSTEM "graph.dtd">
    <graph/>

### 参见

-   <span class="methodname">DOMImplementation::createDocument</span>

DOMImplementation::hasFeature
=============================

Test if the DOM implementation implements a specific feature

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMImplementation::hasFeature</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

Test if the DOM implementation implements a specific `feature`.

You can find a list of all features in the
<a href="http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/introduction.html#ID-Conformance" class="link external">» Conformance</a>
section of the DOM specification.

### 参数

`feature`  
The feature to test.

`version`  
The version number of the `feature` to test. In level 2, this can be
either *2.0* or *1.0*.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

此方法*可以*被静态调用,但会抛出一个 **`E_STRICT`** 错误。

### 范例

**示例 \#1 Testing your DOM Implementation**

``` php
<?php

$features = array(
  'Core'           => 'Core module',
  'XML'            => 'XML module',
  'HTML'           => 'HTML module',
  'Views'          => 'Views module',
  'Stylesheets'    => 'Style Sheets module',
  'CSS'            => 'CSS module',
  'CSS2'           => 'CSS2 module',
  'Events'         => 'Events module',
  'UIEvents'       => 'User interface Events module',
  'MouseEvents'    => 'Mouse Events module',
  'MutationEvents' => 'Mutation Events module',
  'HTMLEvents'     => 'HTML Events module',
  'Range'          => 'Range module',
  'Traversal'      => 'Traversal module'
);
               
foreach ($features as $key => $name) {
  if (DOMImplementation::hasFeature($key, '2.0')) {
    echo "Has feature $name\n";
  } else {
    echo "Missing feature $name\n";
  }
}

?>
```

### 参见

-   <span class="methodname">DOMNode::isSupported</span>

类摘要
------

**DOMNamedNodeMap**

<span class="ooclass"> class **DOMNamedNodeMap** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="type">DOMNode</span> <span
class="methodname">getNamedItem</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="type">DOMNode</span> <span
class="methodname">getNamedItemNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

<span class="type">DOMNode</span> <span class="methodname">item</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

}

属性
----

`length`  
The number of nodes in the map. The range of valid child node indices is
*0* to *length - 1* inclusive.

DOMNamedNodeMap::count
======================

Get number of nodes in the map

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNamedNodeMap::count</span> ( <span
class="methodparam">void</span> )

Gets the number of nodes in the map.

### 参数

此函数没有参数。

### 返回值

Returns the number of nodes in the map, which is identical to the
<a href="/class/domnamednodemap.html#" class="link">length</a> property.

DOMNamedNodeMap::getNamedItem
=============================

Retrieves a node specified by name

### 说明

<span class="type">DOMNode</span> <span
class="methodname">DOMNamedNodeMap::getNamedItem</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Retrieves a node specified by its *nodeName*.

### 参数

`name`  
The *nodeName* of the node to retrieve.

### 返回值

A node (of any type) with the specified *nodeName*, or **`NULL`** if no
node is found.

### 参见

-   <span class="methodname">DOMNamedNodeMap::getNamedItemNS</span>

DOMNamedNodeMap::getNamedItemNS
===============================

Retrieves a node specified by local name and namespace URI

### 说明

<span class="type">DOMNode</span> <span
class="methodname">DOMNamedNodeMap::getNamedItemNS</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> , <span class="methodparam"><span
class="type">string</span> `$localName`</span> )

Retrieves a node specified by `localName` and `namespaceURI`.

### 参数

`namespaceURI`  
The namespace URI of the node to retrieve.

`localName`  
The local name of the node to retrieve.

### 返回值

A node (of any type) with the specified local name and namespace URI, or
**`NULL`** if no node is found.

### 参见

-   <span class="methodname">DOMNamedNodeMap::getNamedItem</span>

DOMNamedNodeMap::item
=====================

Retrieves a node specified by index

### 说明

<span class="type">DOMNode</span> <span
class="methodname">DOMNamedNodeMap::item</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Retrieves a node specified by `index` within the <span
class="classname">DOMNamedNodeMap</span> object.

### 参数

`index`  
Index into this map.

### 返回值

The node at the `index`th position in the map, or **`NULL`** if that is
not a valid index (greater than or equal to the number of nodes in this
map).

类摘要
------

**DOMNode**

<span class="ooclass"> class **DOMNode** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">C14N</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$exclusive`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">C14NFile</span> ( <span class="methodparam"><span
class="type">string</span> `$uri`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$exclusive`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$with_comments`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$xpath`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`nodeName`  
Returns the most accurate name for the current node type

`nodeValue`  
The value of this node, depending on its type. Contrary to the W3C
specification, the node value of <span
class="classname">DOMElement</span> nodes is equal to
<a href="/class/domnode.html#" class="link">DOMNode::textContent</a>
instead of **`NULL`**.

`nodeType`  
Gets the type of the node. One of the predefined
<a href="/dom/constants.html" class="link">XML_xxx_NODE constants</a>

`parentNode`  
The parent of this node. If there is no such node, this returns
**`NULL`**.

`childNodes`  
A <span class="classname">DOMNodeList</span> that contains all children
of this node. If there are no children, this is an empty <span
class="classname">DOMNodeList</span>.

`firstChild`  
The first child of this node. If there is no such node, this returns
**`NULL`**.

`lastChild`  
The last child of this node. If there is no such node, this returns
**`NULL`**.

`previousSibling`  
The node immediately preceding this node. If there is no such node, this
returns **`NULL`**.

`nextSibling`  
The node immediately following this node. If there is no such node, this
returns **`NULL`**.

`attributes`  
A <span class="classname">DOMNamedNodeMap</span> containing the
attributes of this node (if it is a <span
class="classname">DOMElement</span>) or **`NULL`** otherwise.

`ownerDocument`  
The <span class="classname">DOMDocument</span> object associated with
this node, or **`NULL`** if this node is a <span
class="classname">DOMDOcument</span>

`namespaceURI`  
The namespace URI of this node, or **`NULL`** if it is unspecified.

`prefix`  
The namespace prefix of this node, or **`NULL`** if it is unspecified.

`localName`  
Returns the local part of the qualified name of this node.

`baseURI`  
The absolute base URI of this node or **`NULL`** if the implementation
wasn't able to obtain an absolute URI.

`textContent`  
The text content of this node and its descendants.

注释
----

> **Note**:
>
> 此 DOM 扩展采用 UTF-8 编码。在 ISO-8859-1 编码下，使用 <span
> class="function">utf8\_encode</span> 和 <span
> class="function">utf8\_decode</span> 来处理，其它编码下使用
> <a href="/ref/iconv.html" class="link">iconv</a> 函数处理。

更新日志
--------

| 版本  | 说明                                                                             |
|-------|----------------------------------------------------------------------------------|
| 5.6.1 | The textContent property has been made writable (formerly it has been readonly). |

参见
----

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-1950641247" class="link external">» W3C specification of Node</a>

DOMNode::appendChild
====================

Adds new child at the end of the children

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

This function appends a child to an existing list of children or creates
a new list of children. The child can be created with e.g. <span
class="methodname">DOMDocument::createElement</span>, <span
class="methodname">DOMDocument::createTextNode</span> etc. or simply by
using any other node.

### 参数

`newnode`  
The appended child.

### 返回值

The node added.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if this node is readonly or if the previous parent of the node
being inserted is readonly.

**`DOM_HIERARCHY_REQUEST_ERR`**  
Raised if this node is of a type that does not allow children of the
type of the `newnode` node, or if the node to append is one of this
node's ancestors or this node itself.

**`DOM_WRONG_DOCUMENT_ERR`**  
Raised if `newnode` was created from a different document than the one
that created this node.

### 范例

The following example will add a new element node to a fresh document.

**示例 \#1 Adding a child**

``` php
<?php

$doc = new DOMDocument;

$node = $doc->createElement("para");
$newnode = $doc->appendChild($node);

echo $doc->saveXML();
?>
```

**示例 \#2 Nested children**

``` php
<?php

$doc = new DOMDocument;

$headNode = $doc->createElement("head");
$doc->appendChild($headNode);

$titleNode = $doc->createElement("title");
$headNode->appendChild($titleNode);

echo $doc->saveXML();
?>
```

### 参见

-   <span class="methodname">DOMNode::insertBefore</span>
-   <span class="methodname">DOMNode::removeChild</span>
-   <span class="methodname">DOMNode::replaceChild</span>

DOMNode::C14N
=============

Canonicalize nodes to a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

Canonicalize nodes to a string

### 参数

`exclusive`  
Enable exclusive parsing of only the nodes matched by the provided xpath
or namespace prefixes.

`with_comments`  
Retain comments in output.

`xpath`  
An array of *xpath*s to filter the nodes by.

`ns_prefixes`  
An array of namespace prefixes to filter the nodes by.

### 返回值

Returns canonicalized nodes as a string 或者在失败时返回 **`FALSE`**

### 参见

-   <span class="methodname">DOMNode::C14NFile</span>

DOMNode::C14NFile
=================

Canonicalize nodes to a file

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

Canonicalize nodes to a file.

### 参数

`uri`  
Path to write the output to.

`exclusive`  
Enable exclusive parsing of only the nodes matched by the provided xpath
or namespace prefixes.

`with_comments`  
Retain comments in output.

`xpath`  
An array of *xpath*s to filter the nodes by.

`ns_prefixes`  
An array of namespace prefixes to filter the nodes by.

### 返回值

Number of bytes written 或者在失败时返回 **`FALSE`**

### 参见

-   <span class="methodname">DOMNode::C14N</span>

DOMNode::cloneNode
==================

Clones a node

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

Creates a copy of the node.

### 参数

`deep`  
Indicates whether to copy all descendant nodes. This parameter is
defaulted to **`FALSE`**.

### 返回值

The cloned node.

DOMNode::getLineNo
==================

Get line number for a node

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

Gets line number for where the node is defined.

### 参数

此函数没有参数。

### 返回值

Always returns the line number where the node was defined in.

### 范例

**示例 \#1 <span class="methodname">DOMNode::getLineNo</span> example**

``` php
<?php
// XML dump for below example
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <node />
</root>
XML;

// Create a new DOMDocument instance
$dom = new DOMDocument;

// Load the XML
$dom->loadXML($xml);

// Print where the line where the 'node' element was defined in
printf('The <node> tag is defined on line %d', $dom->getElementsByTagName('node')->item(0)->getLineNo());
?>
```

以上例程会输出：

    The <node> tag is defined in line 3

DOMNode::getNodePath
====================

Get an XPath for a node

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

Gets an XPath location path for the node.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="type">string</span> containing the XPath, or
**`NULL`** in case of an error.

### 范例

**示例 \#1 <span class="methodname">DOMNode::getNodePath</span>
example**

``` php
<?php
// Create a new DOMDocument instance
$dom = new DOMDocument;

// Load the XML
$dom->loadXML('
<fruits>
 <apples>
  <apple>braeburn</apple>
  <apple>granny smith</apple>
 </apples>
 <pears>
  <pear>conference</pear>
 </pears>
</fruits>
');

// Print XPath for each element
foreach ($dom->getElementsByTagName('*') as $node) {
    echo $node->getNodePath() . "\n";
}
?>
```

以上例程会输出：

    /fruits
    /fruits/apples
    /fruits/apples/apple[1]
    /fruits/apples/apple[2]
    /fruits/pears
    /fruits/pears/pear

### 参见

-   <span class="classname">DOMXPath</span>

DOMNode::hasAttributes
======================

Checks if node has attributes

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

This method checks if the node has attributes. The tested node has to be
an **`XML_ELEMENT_NODE`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMNode::hasChildNodes</span>

DOMNode::hasChildNodes
======================

Checks if node has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

This function checks if the node has children.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMNode::hasAttributes</span>

DOMNode::insertBefore
=====================

Adds a new child before a reference node

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

This function inserts a new node right before the reference node. If you
plan to do further modifications on the appended child you must use the
returned node.

### 参数

`newnode`  
The new node.

`refnode`  
The reference node. If not supplied, `newnode` is appended to the
children.

### 返回值

The inserted node.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if this node is readonly or if the previous parent of the node
being inserted is readonly.

**`DOM_HIERARCHY_REQUEST_ERR`**  
Raised if this node is of a type that does not allow children of the
type of the `newnode` node, or if the node to append is one of this
node's ancestors or this node itself.

**`DOM_WRONG_DOCUMENT_ERR`**  
Raised if `newnode` was created from a different document than the one
that created this node.

**`DOM_NOT_FOUND`**  
Raised if `refnode` is not a child of this node.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>

DOMNode::isDefaultNamespace
===========================

Checks if the specified namespaceURI is the default namespace or not

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

Tells whether `namespaceURI` is the default namespace.

### 参数

`namespaceURI`  
The namespace URI to look for.

### 返回值

Return **`TRUE`** if `namespaceURI` is the default namespace,
**`FALSE`** otherwise.

DOMNode::isSameNode
===================

Indicates if two nodes are the same node

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

This function indicates if two nodes are the same node. The comparison
is *not* based on content

### 参数

`node`  
The compared node.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

DOMNode::isSupported
====================

Checks if feature is supported for specified version

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

Checks if the asked `feature` is supported for the specified `version`.

### 参数

`feature`  
The feature to test. See the example of <span
class="methodname">DOMImplementation::hasFeature</span> for a list of
features.

`version`  
The version number of the `feature` to test.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="methodname">DOMImplementation::hasFeature</span>

DOMNode::lookupNamespaceUri
===========================

Gets the namespace URI of the node based on the prefix

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

Gets the namespace URI of the node based on the `prefix`.

### 参数

`prefix`  
The prefix of the namespace.

### 返回值

The namespace URI of the node.

### 参见

-   <span class="methodname">DOMNode::lookupPrefix</span>

DOMNode::lookupPrefix
=====================

Gets the namespace prefix of the node based on the namespace URI

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

Gets the namespace prefix of the node based on the namespace URI.

### 参数

`namespaceURI`  
The namespace URI.

### 返回值

The prefix of the namespace.

### 参见

-   <span class="methodname">DOMNode::lookupNamespaceUri</span>

DOMNode::normalize
==================

Normalizes the node

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

Remove empty text nodes and merge adjacent text nodes in this node and
all its children.

### 返回值

没有返回值。

### 参见

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-normalize" class="link external">» The DOM Specification</a>
-   <span class="methodname">DOMDocument::normalizeDocument</span>

DOMNode::removeChild
====================

Removes child from list of children

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

This functions removes a child from a list of children.

### 参数

`oldnode`  
The removed child.

### 返回值

If the child could be removed the function returns the old child.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if this node is readonly.

**`DOM_NOT_FOUND`**  
Raised if `oldnode` is not a child of this node.

### 范例

The following example will delete the *chapter* element of our XML
document.

**示例 \#1 Removing a child**

``` php
<?php

$doc = new DOMDocument;
$doc->load('book.xml');

$book = $doc->documentElement;

// we retrieve the chapter and remove it from the book
$chapter = $book->getElementsByTagName('chapter')->item(0);
$oldchapter = $book->removeChild($chapter);

echo $doc->saveXML();
?>
```

以上例程会输出：

    <?xml version="1.0" encoding="utf-8"?>
    <!DOCTYPE book PUBLIC "-//OASIS//DTD DocBook XML V4.1.2//EN" 
              "http://www.oasis-open.org/docbook/xml/4.1.2/docbookx.dtd">
    <book id="listing">
     <title>My lists</title>
     
    </book>

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMNode::replaceChild</span>

DOMNode::replaceChild
=====================

Replaces a child

### 说明

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

This function replaces the child `oldnode` with the passed new node. If
the `newnode` is already a child it will not be added a second time. If
the replacement succeeds the old node is returned.

### 参数

`newnode`  
The new node. It must be a member of the target document, i.e. created
by one of the DOMDocument-\>createXXX() methods or imported in the
document by
<a href="/class/domdocument.html#DOMDocument::importNode" class="xref"></a>.

`oldnode`  
The old node.

### 返回值

The old node or **`FALSE`** if an error occur.

### 错误／异常

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**  
Raised if this node is readonly or if the previous parent of the node
being inserted is readonly.

**`DOM_HIERARCHY_REQUEST_ERR`**  
Raised if this node is of a type that does not allow children of the
type of the `newnode` node, or if the node to put in is one of this
node's ancestors or this node itself.

**`DOM_WRONG_DOCUMENT_ERR`**  
Raised if `newnode` was created from a different document than the one
that created this node.

**`DOM_NOT_FOUND`**  
Raised if `oldnode` is not a child of this node.

### 参见

-   <span class="methodname">DOMNode::appendChild</span>
-   <span class="methodname">DOMNode::removeChild</span>

类摘要
------

**DOMNodeList**

<span class="ooclass"> class **DOMNodeList** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="type">DOMNode</span> <span class="methodname">item</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

}

属性
----

`length`  
The number of nodes in the list. The range of valid child node indices
is 0 to *length - 1* inclusive.

更新日志
--------

| 版本  | 说明                                                                                                                                                                    |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | The <span class="classname">Countable</span> interface is implemented and returns the value of the <a href="/class/domnodelist.html#" class="link">length</a> property. |

参见
----

-   <a href="http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-536297177" class="link external">» W3C specification of NodeList</a>

DOMNodeList::count
==================

Get number of nodes in the list

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNodeList::count</span> ( <span
class="methodparam">void</span> )

Gets the number of nodes in the list.

### 参数

此函数没有参数。

### 返回值

Returns the number of nodes in the list, which is identical to the
<a href="/class/domnodelist.html#" class="link">length</a> property.

DOMNodeList::item
=================

Retrieves a node specified by index

### 说明

<span class="type">DOMNode</span> <span
class="methodname">DOMNodeList::item</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Retrieves a node specified by `index` within the <span
class="classname">DOMNodeList</span> object.

**小贴士**

If you need to know the number of nodes in the collection, use the
*length* property of the <span class="classname">DOMNodeList</span>
object.

### 参数

`index`  
Index of the node into the collection.

### 返回值

The node at the `index`th position in the <span
class="classname">DOMNodeList</span>, or **`NULL`** if that is not a
valid index.

### 范例

**示例 \#1 Traversing all the entries of the table**

``` php
<?php

$doc = new DOMDocument;
$doc->load('book.xml');

$items = $doc->getElementsByTagName('entry');

for ($i = 0; $i < $items->length; $i++) {
    echo $items->item($i)->nodeValue . "\n";
}

?>
```

Alternatively, you can use
<a href="/control-structures/foreach.html" class="link">foreach</a>,
which is a much more convenient way:

``` php
<?php

foreach ($items as $item) {
    echo $item->nodeValue . "\n";
}

?>
```

以上例程会输出：

    Title
    Author
    Language
    ISBN
    The Grapes of Wrath
    John Steinbeck
    en
    0140186409
    The Pearl
    John Steinbeck
    en
    014017737X
    Samarcande
    Amine Maalouf
    fr
    2253051209

类摘要
------

**DOMNotation**

<span class="ooclass"> class **DOMNotation** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$publicId` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$systemId` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`publicId`  

`systemId`  

类摘要
------

**DOMProcessingInstruction**

<span class="ooclass"> class **DOMProcessingInstruction** </span> <span
class="ooclass"> <span class="modifier">extends</span> **DOMNode**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$target` ;

<span class="modifier">public</span> <span class="type">string</span>
`$data` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`target`  

`data`  

DOMProcessingInstruction::\_\_construct
=======================================

Creates a new <span class="classname">DOMProcessingInstruction</span>
object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMProcessingInstruction::\_\_construct</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$value`</span> \] )

Creates a new <span class="classname">DOMProcessingInstruction</span>
object. This object is read only. It may be appended to a document, but
additional nodes may not be appended to this node until the node is
associated with a document. To create a writeable node, use
<a href="/class/domdocument.html#DOMDocument::createProcessingInstruction" class="xref"></a>.

### 参数

`name`  
The tag name of the processing instruction.

`value`  
The value of the processing instruction.

### 范例

**示例 \#1 Creating a new <span
class="classname">DOMProcessingInstruction</span> object**

``` php
<?php

$dom = new DOMDocument('1.0', 'UTF-8');
$html = $dom->appendChild(new DOMElement('html'));
$body = $html->appendChild(new DOMElement('body'));
$pinode = new DOMProcessingInstruction('php', 'echo "Hello World"; ');
$body->appendChild($pinode);
echo $dom->saveXML(); 

?>
```

以上例程会输出：

    <?xml version="1.0" encoding="UTF-8"?>
    <html><body><?php echo "Hello World"; ?></body></html>

### 参见

-   <span
    class="methodname">DOMDocument::createProcessingInstruction</span>

简介
----

The <span class="classname">DOMText</span> class inherits from <span
class="classname">DOMCharacterData</span> and represents the textual
content of a <span class="classname">DOMElement</span> or <span
class="classname">DOMAttr</span>.

类摘要
------

**DOMText**

<span class="ooclass"> class **DOMText** </span> <span class="ooclass">
<span class="modifier">extends</span> **DOMCharacterData** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$wholeText` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$data` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$nodeName` ;

<span class="modifier">public</span> <span class="type">string</span>
`$nodeValue` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$nodeType` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$parentNode` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNodeList</span>
`$childNodes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$firstChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$lastChild` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$previousSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMNode</span>
`$nextSibling` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span
class="type">DOMNamedNodeMap</span> `$attributes` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">DOMDocument</span>
`$ownerDocument` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$namespaceURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$prefix` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$localName` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">string</span>
`$baseURI` ;

<span class="modifier">public</span> <span class="type">string</span>
`$textContent` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isElementContentWhitespace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isWhitespaceInElementContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMText</span>
<span class="methodname">splitText</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::appendData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::deleteData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::insertData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMCharacterData::replaceData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMCharacterData::substringData</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::appendChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
)

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::C14N</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$exclusive`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$with_comments`</span> \[, <span class="methodparam"><span
class="type">array</span> `$xpath`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::C14NFile</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$exclusive`<span class="initializer"> = **`FALSE`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span>
`$with_comments`<span class="initializer"> = **`FALSE`**</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$xpath`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ns_prefixes`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::cloneNode</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$deep`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">DOMNode::getLineNo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::getNodePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasAttributes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::hasChildNodes</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::insertBefore</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
\[, <span class="methodparam"><span class="type">DOMNode</span>
`$refnode`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isDefaultNamespace</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSameNode</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$node`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMNode::isSupported</span> ( <span
class="methodparam"><span class="type">string</span> `$feature`</span> ,
<span class="methodparam"><span class="type">string</span>
`$version`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupNamespaceUri</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">DOMNode::lookupPrefix</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMNode::normalize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::removeChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$oldnode`</span>
)

<span class="modifier">public</span> <span class="type">DOMNode</span>
<span class="methodname">DOMNode::replaceChild</span> ( <span
class="methodparam"><span class="type">DOMNode</span> `$newnode`</span>
, <span class="methodparam"><span class="type">DOMNode</span>
`$oldnode`</span> )

}

属性
----

`wholeText`  
Holds all the text of logically-adjacent (not separated by Element,
Comment or Processing Instruction) Text nodes.

DOMText::\_\_construct
======================

Creates a new <span class="classname">DOMText</span> object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMText::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

Creates a new <span class="classname">DOMText</span> object.

### 参数

`value`  
The value of the text node. If not supplied an empty text node is
created.

### 范例

**示例 \#1 Creating a new DOMText**

``` php
<?php

$dom = new DOMDocument('1.0', 'iso-8859-1');
$element = $dom->appendChild(new DOMElement('root'));
$text = $element->appendChild(new DOMText('root value'));
echo $dom->saveXML(); /* <?xml version="1.0" encoding="iso-8859-1"?><root>root value</root> */

?>
```

### 参见

-   <span class="methodname">DOMDocument::createTextNode</span>

DOMText::isElementContentWhitespace
===================================

Returns whether this text node contains whitespace in element content

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMText::isElementContentWhitespace</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

DOMText::isWhitespaceInElementContent
=====================================

Indicates whether this text node contains whitespace

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMText::isWhitespaceInElementContent</span> (
<span class="methodparam">void</span> )

Indicates whether this text node contains only whitespace or it is
empty. The text node is determined to contain whitespace in element
content during the load of the document.

### 返回值

Returns **`TRUE`** if node contains zero or more whitespace characters
and nothing else. Returns **`FALSE`** otherwise.

DOMText::splitText
==================

Breaks this node into two nodes at the specified offset

### 说明

<span class="modifier">public</span> <span class="type">DOMText</span>
<span class="methodname">DOMText::splitText</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

Breaks this node into two nodes at the specified `offset`, keeping both
in the tree as siblings.

After being split, this node will contain all the content up to the
`offset`. If the original node had a parent node, the new node is
inserted as the next sibling of the original node. When the `offset` is
equal to the length of this node, the new node has no data.

### 参数

`offset`  
The offset at which to split, starting from 0.

### 返回值

The new node of the same type, which contains all the content at and
after the `offset`.

简介
----

Supports XPath 1.0

类摘要
------

**DOMXPath**

<span class="ooclass"> class **DOMXPath** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="type">DOMDocument</span> `$document` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">DOMDocument</span> `$doc`</span>
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">evaluate</span> ( <span
class="methodparam"><span class="type">string</span>
`$expression`</span> \[, <span class="methodparam"><span
class="type">DOMNode</span> `$contextnode`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$registerNodeNS`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span class="methodname">query</span> (
<span class="methodparam"><span class="type">string</span>
`$expression`</span> \[, <span class="methodparam"><span
class="type">DOMNode</span> `$contextnode`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$registerNodeNS`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">registerNamespace</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> ,
<span class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">registerPhpFunctions</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$restrict`</span>
\] )

}

属性
----

`document`  

DOMXPath::\_\_construct
=======================

Creates a new <span class="classname">DOMXPath</span> object

### 说明

<span class="modifier">public</span> <span
class="methodname">DOMXPath::\_\_construct</span> ( <span
class="methodparam"><span class="type">DOMDocument</span> `$doc`</span>
)

Creates a new <span class="classname">DOMXPath</span> object.

### 参数

`doc`  
The <span class="classname">DOMDocument</span> associated with the <span
class="classname">DOMXPath</span>.

DOMXPath::evaluate
==================

Evaluates the given XPath expression and returns a typed result if
possible

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">DOMXPath::evaluate</span> ( <span
class="methodparam"><span class="type">string</span>
`$expression`</span> \[, <span class="methodparam"><span
class="type">DOMNode</span> `$contextnode`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$registerNodeNS`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

Executes the given XPath `expression` and returns a typed result if
possible.

### 参数

`expression`  
The XPath expression to execute.

`contextnode`  
The optional `contextnode` can be specified for doing relative XPath
queries. By default, the queries are relative to the root element.

`registerNodeNS`  
The optional `registerNodeNS` can be specified to disable automatic
registration of the context node.

### 返回值

Returns a typed result if possible or a <span
class="classname">DOMNodeList</span> containing all nodes matching the
given XPath `expression`.

If the `expression` is malformed or the `contextnode` is invalid, <span
class="methodname">DOMXPath::evaluate</span> returns **`FALSE`**.

### 范例

**示例 \#1 Getting the count of all the english books**

``` php
<?php

$doc = new DOMDocument;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

$tbody = $doc->getElementsByTagName('tbody')->item(0);

// our query is relative to the tbody node
$query = 'count(row/entry[. = "en"])';

$entries = $xpath->evaluate($query, $tbody);
echo "There are $entries english books\n";

?>
```

以上例程会输出：

    There are 2 english books

### 参见

-   <span class="methodname">DOMXPath::query</span>

DOMXPath::query
===============

Evaluates the given XPath expression

### 说明

<span class="modifier">public</span> <span
class="type">DOMNodeList</span> <span
class="methodname">DOMXPath::query</span> ( <span
class="methodparam"><span class="type">string</span>
`$expression`</span> \[, <span class="methodparam"><span
class="type">DOMNode</span> `$contextnode`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$registerNodeNS`<span class="initializer"> = **`TRUE`**</span></span>
\]\] )

Executes the given XPath `expression`.

### 参数

`expression`  
The XPath expression to execute.

`contextnode`  
The optional `contextnode` can be specified for doing relative XPath
queries. By default, the queries are relative to the root element.

`registerNodeNS`  
The optional `registerNodeNS` can be specified to disable automatic
registration of the context node.

### 返回值

Returns a <span class="classname">DOMNodeList</span> containing all
nodes matching the given XPath `expression`. Any expression which does
not return nodes will return an empty <span
class="classname">DOMNodeList</span>.

If the `expression` is malformed or the `contextnode` is invalid, <span
class="methodname">DOMXPath::query</span> returns **`FALSE`**.

### 范例

**示例 \#1 Getting all the english books**

``` php
<?php

$doc = new DOMDocument;

// We don't want to bother with white spaces
$doc->preserveWhiteSpace = false;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

// We start from the root element
$query = '//book/chapter/para/informaltable/tgroup/tbody/row/entry[. = "en"]';

$entries = $xpath->query($query);

foreach ($entries as $entry) {
    echo "Found {$entry->previousSibling->previousSibling->nodeValue}," .
         " by {$entry->previousSibling->nodeValue}\n";
}
?>
```

以上例程会输出：

    Found The Grapes of Wrath, by John Steinbeck
    Found The Pearl, by John Steinbeck

We can also use the `contextnode` parameter to shorten our expression:

``` php
<?php

$doc = new DOMDocument;
$doc->preserveWhiteSpace = false;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

$tbody = $doc->getElementsByTagName('tbody')->item(0);

// our query is relative to the tbody node
$query = 'row/entry[. = "en"]';

$entries = $xpath->query($query, $tbody);

foreach ($entries as $entry) {
    echo "Found {$entry->previousSibling->previousSibling->nodeValue}," .
         " by {$entry->previousSibling->nodeValue}\n";
}
?>
```

### 参见

-   <span class="methodname">DOMXPath::evaluate</span>

DOMXPath::registerNamespace
===========================

Registers the namespace with the <span class="classname">DOMXPath</span>
object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">DOMXPath::registerNamespace</span> ( <span
class="methodparam"><span class="type">string</span> `$prefix`</span> ,
<span class="methodparam"><span class="type">string</span>
`$namespaceURI`</span> )

Registers the `namespaceURI` and `prefix` with the DOMXPath object.

### 参数

`prefix`  
The prefix.

`namespaceURI`  
The URI of the namespace.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

DOMXPath::registerPhpFunctions
==============================

Register PHP functions as XPath functions

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">DOMXPath::registerPhpFunctions</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$restrict`</span>
\] )

This method enables the ability to use PHP functions within XPath
expressions.

### 参数

`restrict`  
Use this parameter to only allow certain functions to be called from
XPath.

This parameter can be either a <span class="type">string</span> (a
function name) or an <span class="type">array</span> of function names.

### 返回值

没有返回值。

### 范例

The following examples use `book.xml` which contains the following:

**示例 \#1 book.xml**

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<books>
 <book>
  <title>PHP Basics</title>
  <author>Jim Smith</author>
  <author>Jane Smith</author>
 </book>
 <book>
  <title>PHP Secrets</title>
  <author>Jenny Smythe</author>
 </book>
 <book>
  <title>XML basics</title>
  <author>Joe Black</author>
 </book>
</books>
```

**示例 \#2 <span
class="methodname">DOMXPath::registerPHPFunctions</span> with
*php:functionString***

``` php
<?php
$doc = new DOMDocument;
$doc->load('book.xml');

$xpath = new DOMXPath($doc);

// Register the php: namespace (required)
$xpath->registerNamespace("php", "http://php.net/xpath");

// Register PHP functions (no restrictions)
$xpath->registerPHPFunctions();

// Call substr function on the book title
$nodes = $xpath->query('//book[php:functionString("substr", title, 0, 3) = "PHP"]');

echo "Found {$nodes->length} books starting with 'PHP':\n";
foreach ($nodes as $node) {
    $title  = $node->getElementsByTagName("title")->item(0)->nodeValue;
    $author = $node->getElementsByTagName("author")->item(0)->nodeValue;
    echo "$title by $author\n";
}

?>
```

以上例程的输出类似于：

    Found 2 books starting with 'PHP':
    PHP Basics by Jim Smith
    PHP Secrets by Jenny Smythe

**示例 \#3 <span
class="methodname">DOMXPath::registerPHPFunctions</span> with
*php:function***

``` php
<?php
$doc = new DOMDocument;
$doc->load('book.xml');

$xpath = new DOMXPath($doc);

// Register the php: namespace (required)
$xpath->registerNamespace("php", "http://php.net/xpath");

// Register PHP functions (has_multiple only)
$xpath->registerPHPFunctions("has_multiple");
 
function has_multiple($nodes) {
    // Return true if more than one author
    return count($nodes) > 1;
}
// Filter books with multiple authors
$books = $xpath->query('//book[php:function("has_multiple", author)]');

echo "Books with multiple authors:\n";
foreach ($books as $book) {
    echo $book->getElementsByTagName("title")->item(0)->nodeValue . "\n";
}

?>
```

以上例程的输出类似于：

    Books with multiple authors:
    PHP Basics

### 参见

-   <span class="methodname">DOMXPath::registerNamespace</span>
-   <span class="methodname">DOMXPath::query</span>
-   <span class="methodname">DOMXPath::evaluate</span>
