预定义类
--------

The XML DAS provides two main classes. The first is SDO\_DAS\_XML which
is the main class used to fetch the data from the XML source and used to
write the data back. The second is the SDO\_DAS\_XML\_Document class,
which represents the data in the XML document.

There are also some exception classes which can be thrown if errors are
found when looking for or parsing the xsd or xml files.

<span class="classname">SDO\_DAS\_XML</span>
--------------------------------------------

This is the main class of the XML DAS, which is used fetch the data from
the xml source and also used to write the data back. Other than the
methods to load and save xml files,

方法
----

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::create" class="link">create</a>
    This is a static method available in the SDO\_DAS\_XML class. Used
    to construct an SDO\_DAS\_XML object.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::addTypes" class="link">addTypes</a>
    Works in much the same way as <span class="function">create</span>
    but used to add the contents of a second or subsequent schema file
    to an XML DAS that has already been created.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::createDataObject" class="link">createDataObject</a>
    Can be used to construct an SDO data object of a given type.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::createDocument" class="link">createDocument</a>
    Can be used to construct an XML Document object from scratch.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::loadFile" class="link">loadFile</a>
    Loads the xml instance document from a file. This file can be at
    local file system or it can be on a remote host.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::loadString" class="link">loadString</a>
    same as the above method. Loads the xml instance which is available
    as string.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::saveFile" class="link">saveFile</a>
    save SDO\_DAS\_XML\_Document object as a xml file.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML::saveString" class="link">saveString</a>
    save SDO\_DAS\_XML\_Document object as a xml string.

<span class="classname">SDO\_DAS\_XML\_Document</span>
------------------------------------------------------

This class can be used to get to the name and namespace of the document
element, and to get to the root data object of the document. Lastly, it
can also be used to set the XML version and encoding of a document on
output.

方法
----

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML_Document::getRootDataObject" class="link">getRootDataObject</a>
    gets the root DataObject.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML_Document::getRootElementName" class="link">getRootElementName</a>
    gets the root DataObject's name.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML_Document::getRootElementURI" class="link">getRootElementURI</a>
    gets the root DataObject's URI.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML_Document::setEncoding" class="link">setEncoding</a>
    sets the encoding string with the given value.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML_Document::setXMLDeclaration" class="link">setXMLDeclaraion</a>
    to set/unset the xml declaration.

-   <a href="/ref/sdo-das-xml.html#SDO_DAS_XML_Document::setXMLVersion" class="link">setXMLVersion</a>
    sets the xml version with the given value.

<span class="classname">SDO\_DAS\_XML\_ParserException</span>
-------------------------------------------------------------

Is a subclass of <span class="classname">SDO\_Exception</span>. Thrown
for any parser errors while loading the xsd/xml file.

<span class="classname">SDO\_DAS\_XML\_FileException</span>
-----------------------------------------------------------

Is a subclass of <span class="classname">SDO\_Exception</span>. Thrown
by any of the methods that load data from a file, when the file cannot
be found.

Limitations compared with SDO 2.0 specification
-----------------------------------------------

The
<a href="https://www.jcp.org/en/jsr/detail?id=235" class="link external">» SDO 2.0 specification</a>
defines the mapping between XML types and SDO types. With Java SDO, this
mapping is implemented by the XMLHelper. With SDO for PHP, this mapping
is implemented by the XML Data Access Service. The XML DAS implements
the mapping described in the SDO 2.0 specification with some
restrictions. A detailed list is of the limitations is:

**XML Simple Types**

1.  Simple Type with sdoJava:instanceClass - no PHP equivalent provided.

2.  Simple Type with sdoJava:extendedInstanceClass - no PHP equivalent
    provided.

3.  Simple Type with list of itemType.

4.  Simple Type with union.

**XML Complex Types**

1.  Complex Type with sdo:aliasName - no PHP support for SDO Type
    aliases.

**XSD Attribute**

1.  Attribute with sdo:aliasName - no PHP support for SDO property
    aliases.

2.  Attribute with default value - no PHP support for SDO property
    defaults.

3.  Attribute with fixed value - no PHP support for SDO read-only
    properties or default values.

4.  Attribute referencing a DataObject with sdo:propertyType - no
    support for sdo:propertyType="...".

5.  Attribute with bi-directional property to a DataObject with
    sdo:oppositeProperty and sdo:propertyType - no PHP support for SDO
    opposite.

**XSD Elements**

1.  Element with sdo:aliasName - no PHP support for SDO property
    aliases.

2.  Element with substitution group.

**XSD Elements with Simple Type**

1.  Element of SimpleType with default - no PHP support for SDO defaults

2.  Element of SimpleType with fixed value - no PHP support for SDO
    read-only properties or default values.

3.  Element of SimpleType with sdo:string - no support for
    sdo:string="true".

4.  Element referencing a DataObject with sdo:propertyType - no support
    for sdo:propertyType="..."

5.  Element with bi-directional reference to a DataObject with
    sdo:oppositeProperty and sdo:propertyType - no PHP support for SDO
    opposite.

SDO\_DAS\_XML::addTypes
=======================

To load a second or subsequent schema file to a SDO\_DAS\_XML object

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_XML::addTypes</span> ( <span
class="methodparam"><span class="type">string</span> `$xsd_file`</span>
)

Load a second or subsequent schema file to an XML DAS that has already
been created with the static method <span
class="function">create</span>. Although the file may be any valid
schema file, a likely reason for using this method is to add a schema
file containing definitions of extra complex types, hence the name. See
Example 4 of the parent document for an example.

### 参数

`xsd_file`  
Path to XSD Schema file.

### 返回值

None if successful, otherwise throws an exception as described below.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if a type is not defined in the underlying model.

`SDO_DAS_XML_ParserException`  
Thrown for any problems while parsing the given XSD File.

`SDO_DAS_XML_FileException`  
Thrown if the specified file cannot be found.

SDO\_DAS\_XML::create
=====================

To create SDO\_DAS\_XML object for a given schema file

### 说明

<span class="type">SDO\_DAS\_XML</span> <span
class="methodname">SDO\_DAS\_XML::create</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$xsd_file`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$key`</span> \]\] )

This is the only static method of SDO\_DAS\_XML class. Used to
instantiate SDO\_DAS\_XML object.

### 参数

`xsd_file`  
Path to XSD Schema file. This is optional. If omitted a DAS will be
created that only has the SDO base types defined. Schema files can then
be loaded with the <span class="function">addTypes</span> method. Can be
string or array of values.

`key`  

### 返回值

Returns SDO\_DAS\_XML object on success otherwise throws an exception as
described below.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if a type is not defined in the underlying model.

`SDO_DAS_XML_ParserException`  
Thrown for any problems while parsing the given XSD File.

`SDO_DAS_XML_FileException`  
Thrown if the specified file cannot be found.

SDO\_DAS\_XML::createDataObject
===============================

Creates SDO\_DataObject for a given namespace URI and type name

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SDO\_DAS\_XML::createDataObject</span> ( <span
class="methodparam"><span class="type">string</span>
`$namespace_uri`</span> , <span class="methodparam"><span
class="type">string</span> `$type_name`</span> )

Creates SDO\_DataObject for a given namespace URI and type name. The
type should be defined in the underlying model otherwise
SDO\_TypeNotFoundException will be thrown.

### 参数

`namespace_uri`  
Namespace URI of the type name.

`type_name`  
Type Name.

### 返回值

Returns SDO\_DataObject on success.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if a type is not defined in the underlying model.

SDO\_DAS\_XML::createDocument
=============================

Creates an XML Document object from scratch, without the need to load a
document from a file or string

### 说明

<span class="type">SDO\_DAS\_XML\_Document</span> <span
class="methodname">SDO\_DAS\_XML::createDocument</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$document_element_name`</span> \] )

<span class="type">SDO\_DAS\_XML\_Document</span> <span
class="methodname">SDO\_DAS\_XML::createDocument</span> ( <span
class="methodparam"><span class="type">string</span>
`$document_element_namespace_URI`</span> , <span
class="methodparam"><span class="type">string</span>
`$document_element_name`</span> \[, <span class="methodparam"><span
class="type">SDO\_DataObject</span> `$dataobject`</span> \] )

Creates an XML Document object. This will contain just one empty root
element on which none of the properties will have been set. The purpose
of this call is to allow an application to create an XML document from
scratch without the need to load a document from a file or string. The
document that is created will be as if a document had been loaded that
contained just a single empty document element with no attributes set or
elements within it.

<span class="function">createDocument</span> may need to be told what
the document element is. This will not be necessary in simple cases.
When there is no ambiguity then no parameter need be passed to the
method. However it is possible to load more than one schema file into
the same XML DAS and in this case there may be more than one possible
document element defined: furthermore it is even possible that there are
two possible document elements that differ only in the namespace. To
cope with these cases it is possible to specify either the document
element name, or both the document element name and namespace to the
method.

### 参数

`document_element_name`  
The name of the document element. Only needed if there is more than one
possibility.

`document_element_namespace_URI`  
The namespace part of the document element name. Only needed if there is
more than one possible document element with the same name.

`dataobject`  

### 返回值

Returns an SDO\_XML\_DAS\_Document object on success.

### 错误／异常

`SDO_UnsupportedOperationException`  
Thrown if an element name or element name and namespace URI is passed,
but not found in the underlying model.

SDO\_DAS\_XML::loadFile
=======================

Returns SDO\_DAS\_XML\_Document object for a given path to xml instance
document

### 说明

<span class="type">SDO\_XMLDocument</span> <span
class="methodname">SDO\_DAS\_XML::loadFile</span> ( <span
class="methodparam"><span class="type">string</span> `$xml_file`</span>
)

Constructs the tree of SDO\_DataObjects from the given address to xml
instance document. Returns SDO\_DAS\_XML\_Document Object. Use
SDO\_DAS\_XML\_Document::getRootDataObject method to get root data
object.

### 参数

`xml_file`  
Path to Instance document. This can be a path to a local file or it can
be a URL.

### 返回值

Returns SDO\_DAS\_XML\_Document object on Success or throws exception as
described.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if a type is not defined by the underlying model.

`SDO_PropertyNotFoundException`  
Thrown if a property within a type is not defined in the underlying
model.

`SDO_DAS_XML_ParserException`  
Thrown for any problems while parsing the given XSD File.

`SDO_DAS_XML_FileException`  
Thrown if the specified file cannot be found.

SDO\_DAS\_XML::loadString
=========================

Returns SDO\_DAS\_XML\_Document for a given xml instance string

### 说明

<span class="type">SDO\_DAS\_XML\_Document</span> <span
class="methodname">SDO\_DAS\_XML::loadString</span> ( <span
class="methodparam"><span class="type">string</span>
`$xml_string`</span> )

Constructs the tree of SDO\_DataObjects from the given xml instance
string. Returns SDO\_DAS\_XML\_Document Object. Use
SDO\_DAS\_XML\_Document::getRootDataObject method to get root data
object.

### 参数

`xml_string`  
xml string.

### 返回值

Returns SDO\_DAS\_XML\_Document object on Success or throws exception as
described.

### 错误／异常

`SDO_TypeNotFoundException`  
Thrown if a type is not defined by the underlying model.

`SDO_PropertyNotFoundException`  
Thrown if the a property within a type is not defined in the underlying
model.

`SDO_DAS_XML_ParserException`  
Thrown for any problems while parsing the given XSD File.

SDO\_DAS\_XML::saveFile
=======================

Saves the SDO\_DAS\_XML\_Document object to a file

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_XML::saveFile</span> ( <span
class="methodparam"><span class="type">SDO\_XMLDocument</span>
`$xdoc`</span> , <span class="methodparam"><span
class="type">string</span> `$xml_file`</span> \[, <span
class="methodparam"><span class="type">int</span> `$indent`</span> \] )

Saves the SDO\_DAS\_XML\_Document object to a file.

### 参数

`xdoc`  
SDO\_DAS\_XML\_Document object.

`xml_file`  
xml file.

`indent`  
Optional argument to specify that the xml should be formatted. A
non-negative integer is the amount to indent each level of the xml. So,
the integer 2, for example, will indent the xml so that each contained
element is two spaces further to the right than its containing element.
The integer 0 will cause the xml to be completely left-aligned. The
integer -1 means no formatting - the xml will come out on one long line.

### 返回值

None.

### 错误／异常

`SDO_DAS_XML_FileException`  
Thrown if the specified file cannot be found.

SDO\_DAS\_XML::saveString
=========================

Saves the SDO\_DAS\_XML\_Document object to a string

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_DAS\_XML::saveString</span> ( <span
class="methodparam"><span class="type">SDO\_XMLDocument</span>
`$xdoc`</span> \[, <span class="methodparam"><span
class="type">int</span> `$indent`</span> \] )

Saves the SDO\_DAS\_XML\_Document object to string.

### 参数

`xdoc`  
SDO\_DAS\_XML\_Document object.

`indent`  
Optional argument to specify that the xml should be formatted. A
non-negative integer is the amount to indent each level of the xml. So,
the integer 2, for example, will indent the xml so that each contained
element is two spaces further to the right than its containing element.
The integer 0 will cause the xml to be completely left-aligned. The
integer -1 means no formatting - the xml will come out on one long line.

### 返回值

xml string.

SDO\_DAS\_XML\_Document::getRootDataObject
==========================================

Returns the root SDO\_DataObject

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SDO\_DAS\_XML\_Document::getRootDataObject</span> (
<span class="methodparam">void</span> )

Returns the root SDO\_DataObject.

### 参数

### 返回值

Returns the root SDO\_DataObject.

SDO\_DAS\_XML\_Document::getRootElementName
===========================================

Returns root element's name

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_DAS\_XML\_Document::getRootElementName</span> (
<span class="methodparam">void</span> )

Returns root element's name.

### 参数

### 返回值

Returns root element's name.

SDO\_DAS\_XML\_Document::getRootElementURI
==========================================

Returns root element's URI string

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_DAS\_XML\_Document::getRootElementURI</span> (
<span class="methodparam">void</span> )

Returns root element's URI string.

### 参数

### 返回值

Returns root element's URI string.

SDO\_DAS\_XML\_Document::setEncoding
====================================

Sets the given string as encoding

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_XML\_Document::setEncoding</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

Sets the given string as encoding.

### 参数

`encoding`  
Encoding string.

### 返回值

None.

SDO\_DAS\_XML\_Document::setXMLDeclaration
==========================================

Sets the xml declaration

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_XML\_Document::setXMLDeclaration</span> (
<span class="methodparam"><span class="type">bool</span>
`$xmlDeclatation`</span> )

Controls whether an XML declaration will be generated at the start of
the XML document. Set to **`true`** to generate the XML declaration, or
**`false`** to suppress it.

### 参数

`xmlDeclatation`  
Boolean value to set the XML declaration.

### 返回值

None.

SDO\_DAS\_XML\_Document::setXMLVersion
======================================

Sets the given string as xml version

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_XML\_Document::setXMLVersion</span> ( <span
class="methodparam"><span class="type">string</span>
`$xmlVersion`</span> )

Sets the given string as xml version.

### 参数

`xmlVersion`  
xml version string.

### 返回值

None.

**目录**

-   [SDO\_DAS\_XML::addTypes](/ref/sdo-das-xml.html#SDO_DAS_XML::addTypes)
    — To load a second or subsequent schema file to a SDO\_DAS\_XML
    object
-   [SDO\_DAS\_XML::create](/ref/sdo-das-xml.html#SDO_DAS_XML::create) —
    To create SDO\_DAS\_XML object for a given schema file
-   [SDO\_DAS\_XML::createDataObject](/ref/sdo-das-xml.html#SDO_DAS_XML::createDataObject)
    — Creates SDO\_DataObject for a given namespace URI and type name
-   [SDO\_DAS\_XML::createDocument](/ref/sdo-das-xml.html#SDO_DAS_XML::createDocument)
    — Creates an XML Document object from scratch, without the need to
    load a document from a file or string
-   [SDO\_DAS\_XML::loadFile](/ref/sdo-das-xml.html#SDO_DAS_XML::loadFile)
    — Returns SDO\_DAS\_XML\_Document object for a given path to xml
    instance document
-   [SDO\_DAS\_XML::loadString](/ref/sdo-das-xml.html#SDO_DAS_XML::loadString)
    — Returns SDO\_DAS\_XML\_Document for a given xml instance string
-   [SDO\_DAS\_XML::saveFile](/ref/sdo-das-xml.html#SDO_DAS_XML::saveFile)
    — Saves the SDO\_DAS\_XML\_Document object to a file
-   [SDO\_DAS\_XML::saveString](/ref/sdo-das-xml.html#SDO_DAS_XML::saveString)
    — Saves the SDO\_DAS\_XML\_Document object to a string
-   [SDO\_DAS\_XML\_Document::getRootDataObject](/ref/sdo-das-xml.html#SDO_DAS_XML_Document::getRootDataObject)
    — Returns the root SDO\_DataObject
-   [SDO\_DAS\_XML\_Document::getRootElementName](/ref/sdo-das-xml.html#SDO_DAS_XML_Document::getRootElementName)
    — Returns root element's name
-   [SDO\_DAS\_XML\_Document::getRootElementURI](/ref/sdo-das-xml.html#SDO_DAS_XML_Document::getRootElementURI)
    — Returns root element's URI string
-   [SDO\_DAS\_XML\_Document::setEncoding](/ref/sdo-das-xml.html#SDO_DAS_XML_Document::setEncoding)
    — Sets the given string as encoding
-   [SDO\_DAS\_XML\_Document::setXMLDeclaration](/ref/sdo-das-xml.html#SDO_DAS_XML_Document::setXMLDeclaration)
    — Sets the xml declaration
-   [SDO\_DAS\_XML\_Document::setXMLVersion](/ref/sdo-das-xml.html#SDO_DAS_XML_Document::setXMLVersion)
    — Sets the given string as xml version
