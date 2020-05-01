范例
====

Several of the following examples are based on the
<a href="/sdo/examples.html#Working%20with%20Sequenced%20Data%20Objects" class="link">letter example</a>
described in the
<a href="/ref/sdo.html" class="link">SDO documentation</a>. The examples
assume the XML Schema for the letter is contained in a file `letter.xsd`
and the letter instance is in the file `letter.xml`. These two files are
reproduced here:

``` xml
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:letter="http://letterSchema"
  targetNamespace="http://letterSchema">
  <xsd:element name="letters" type="letter:FormLetter"/>
  <xsd:complexType name="FormLetter" mixed="true">
    <xsd:sequence>
      <xsd:element name="date" minOccurs="0" type="xsd:string"/>
      <xsd:element name="firstName" minOccurs="0" type="xsd:string"/>
      <xsd:element name="lastName" minOccurs="0" type="xsd:string"/>
    </xsd:sequence>
  </xsd:complexType>
</xsd:schema>
```

``` xml
<letter:letters xmlns:letter="http://letterSchema">
  <date>March 1, 2005</date>
  Mutual of Omaha
  Wild Kingdom, USA
  Dear
  <firstName>Casy</firstName>
  <lastName>Crocodile</lastName>
  Please buy more shark repellent.
  Your premium is past due.
</letter:letters>
```

**示例 \#1 Loading, altering, and saving an XML document**

The following example shows how an XML document can be loaded from a
file, altered, and written back.

``` php
<?php
/**
 * Load, update, and save an XML document
 */
try {
   $xmldas = SDO_DAS_XML::create("letter.xsd");
   $document = $xmldas->loadFile("letter.xml");
   $root_data_object = $document->getRootDataObject();
   $root_data_object->date = "September 03, 2004";
   $root_data_object->firstName = "Anantoju";
   $root_data_object->lastName = "Madhu";
   $xmldas->saveFile($document, "letter-out.xml");
   echo "New file has been written:\n";
   print file_get_contents("letter-out.xml");
} catch (SDO_Exception $e) {
   print($e->getMessage());
}
?>
```

An instance of the XML DAS is first obtained from the <span
class="function">SDO\_DAS\_XML::create</span> method, which is a static
method of the <span class="classname">SDO\_DAS\_XML</span> class. The
location of the xsd is passed as a parameter. Once we have an instance
of the XML DAS initialised with a given schema, we can use it to load
the instance document using the <span class="function">loadFile</span>
method. There is also a <span class="function">loadString</span> method
if you want to load an XML instance document from a string. If the
instance document loads successfully, you will be returned an object of
type <span class="classname">SDO\_DAS\_XML\_Document</span>, on which
you can call the <span class="function">getRootDataObject</span> method
to get the SDO data object which is the root of the SDO data graph. You
can then use SDO operations to change the graph. In this example we
alter the `date`, `firstName`, and `lastName` properties. Then we use
the <span class="function">saveFile</span> method to write the changed
document back to the file system. The saveFile method has an optional
extra integer argument which if specified will cause the XML DAS to
format the XML, using the integer as the amount to indent by at each
change in level on the document.

This will write the following to `letter-out.xml`.

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<FormLetter xmlns="http://letterSchema" xsi:type="FormLetter" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <date>September 03, 2004</date>
  Mutual of Omaha
  Wild Kingdom, USA
  Dear
  <firstName>Anantoju</firstName>
  <lastName>Madhu</lastName>
  Please buy more shark repellent.
  Your premium is past due.
</FormLetter>
```

**示例 \#2 Creating a new XML document**

The previous example loaded the document from a file. This example shows
how to create an SDO data graph in memory. In this example it is then
saved to an XML string. Furthermore, because the letter contains both
structured and unstructured content, it uses
<a href="/sdo/examples.html#Working%20with%20Sequenced%20Data%20Objects" class="link">the Sequence API</a>
as well assignments to properties to construct the data graph.

``` php
<?php
/**
 * Create an XML document from scratch
 */
try {
   $xmldas = SDO_DAS_XML::create("letter.xsd");
   try {
       $doc = $xmldas->createDocument();
       $rdo = $doc->getRootDataObject();
       $seq = $rdo->getSequence();
       $seq->insert("April 09, 2005", NULL, 'date');
       $seq->insert("Acme Inc. ", NULL, NULL);
       $seq->insert("United Kingdom. ");
       $seq->insert("Dear", NULL, NULL);
       $seq->insert("Tarun", NULL, "firstName");
       $seq->insert("Nayaraaa", NULL, "lastName");
       $rdo->lastName = "Nayar";
       $seq->insert("Please note that your order number ");
       $seq->insert(12345);
       $seq->insert(" has been dispatched today. Thanks for your business with us.");
       print($xmldas->saveString($doc));
   } catch (SDO_Exception $e) {
       print($e);
   }
} catch (SDO_Exception $e) {
   print("Problem creating an XML document: " . $e->getMessage());
}
?>
```

The <span class="function">createDocument</span> method on the XML DAS
returns a document object with a single root data object corresponding
to an empty document element. The element name of the document element
is known from the schema file. If there is any ambiguity about what the
document element is, as there can be when more than one schema has been
loaded into the same XML DAS, the element name and the namespace URI can
be passed to the <span class="function">createDocument</span> method.

This will emit the following output (line breaks have been inserted for
readability):

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<FormLetter xmlns="http://letterSchema" xsi:type="FormLetter" 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
<date>April 09, 2005</date>
Acme Inc. United Kingdom. 
Dear
<firstName>Tarun</firstName>
<lastName>Nayar</lastName>
Please note that your order number 12345 has been 
dispatched today. Thanks for your business with us.
</FormLetter>
```

**示例 \#3 Setting XML document properties**

This third example shows you how to set the XML version and encoding on
the document object. These will be used when the XML is written out. If
no XML declaration is wanted at all (perhaps you want to generate the
XML as a string to embed in something) then you can use the <span
class="function">setXMLDeclaration</span> method to suppress it.

``` php
<?php
/**
 * Illustrate the calls that control the XML declaration
 */
   $xmldas = SDO_DAS_XML::create("letter.xsd");
   $document = $xmldas->loadFile("letter.xml");
   $document->setXMLVersion("1.1");
   $document->setEncoding("ISO-8859-1");
   print($xmldas->saveString($document));
?>
```

The XML version and encoding are set in the XML declaration at the top
of the XML document.

``` xml
<?xml version="1.1" encoding="utf-8"?>
.../...
```

**示例 \#4 Using an open type**

This fourth example illustrates the use of an SDO open type and the use
of the <span class="function">createDataObject</span> method. For this
example we use the following two schema:

``` xml
<schema
  xmlns="http://www.w3.org/2001/XMLSchema">
  
  <element name="jungle">
    <complexType>
      <sequence>
        <any minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </complexType>
  </element>
  
</schema>
```

Note the presence of the `any` element in the definition. This first
schema defines the `jungle` complex type as containing a sequence of any
other type. The other types that the example will use are defined in a
second schema file:

``` xml
<schema xmlns= "http://www.w3.org/2001/XMLSchema">

   <complexType name="snakeType">
     <sequence>
       <element name= "name" type="string"/>
       <element name= "length" type="positiveInteger" />
     </sequence>
   </complexType>

   <complexType name="bearType">
     <sequence>
       <element name= "name" type="string"/>
       <element name= "weight" type="positiveInteger" />
     </sequence>
   </complexType>

   <complexType name="pantherType">
     <sequence>
       <element name= "name" type="string"/>
       <element name= "colour" type="string" />
     </sequence>
   </complexType>

</schema>
```

Here is the example PHP code that uses these two schema files:

``` php
<?php

/**
 * Illustrate open types and the use of the addTypes() method
 */

$xmldas = SDO_DAS_XML::create();
$xmldas->addTypes("jungle.xsd"); // this is an open type i.e. the xsd specifies it can contain "any" type
$xmldas->addTypes('animalTypes.xsd');

$baloo            = $xmldas->createDataObject('','bearType');
$baloo->name      = "Baloo";
$baloo->weight    = 800;

$bagheera         = $xmldas->createDataObject('','pantherType');
$bagheera->name   = "Bagheera";
$bagheera->colour = 'inky black';

$kaa              = $xmldas->createDataObject('','snakeType');
$kaa->name        = "Kaa";
$kaa->length      = 25;

$document         = $xmldas->createDocument();
$do               = $document->getRootDataObject();
$do->bear         = $baloo;
$do->panther      = $bagheera;
$do->snake        = $kaa;

print($xmldas->saveString($document,2));

?>
```

These two schema files are loaded into the XML DAS with first the <span
class="function">create</span> and <span
class="function">addTypes</span> methods. The <span
class="function">createDataObject</span> method is used to create three
separate data objects. In each case the namespaceURI and typename of the
type are passed to the <span class="function">createDataObject</span>
method: in this example the namespace URI is blank because no namespace
is used in the schema. Once the three data objects - representing a
bear, a panther and a snake - have been created, a document object is
created with the <span class="function">createDocument</span> method. In
this case there is no ambiguity about what the document element of the
document should be - as the second schema file only defines complex
types, the document element can only be the global `jungle` element
defined in the first schema. This document will have a single root data
object corresponding to an empty document element `jungle`. As this is
an open type, properties can be added at will. When the first assignment
is made to `$do->bear`, a property `bear` is added to the root data
object: likewise for the next two assignments. When the document is
written out by the <span class="function">saveString</span> method, the
resulting document is:

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<jungle xsi:type="jungle" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <bear xsi:type="bearType">
    <name>Baloo</name>
    <weight>800</weight>
  </bear>
  <panther xsi:type="pantherType">
    <name>Bagheera</name>
    <colour>inky black</colour>
  </panther>
  <snake xsi:type="snakeType">
    <name>Kaa</name>
    <length>25</length>
  </snake>
</jungle>
```

**示例 \#5 Finding out what you can from the document**

This example is intended to illustrate how you can find the element name
and namespace of the document element from the XML Document object, and
the SDO type and namespace from the root data object of the XML data
object, and how they relate to one another. This can be difficult to
understand because there are four method calls: two can be made against
the Document object, and two that can be made against any data object
including the root data object. Because of the rules that define how the
SDO model is derived from the XML model, when the data object concerned
is the root object that represents the document object for the document,
only three possible values can come back from these four method calls.

The two method calls that can be made against the document are <span
class="function">getRootElementName</span> and <span
class="function">getRootEelementURI</span>. These return the element
name and namespace of the document element, respectively.

The two method calls that can be made against any data object are <span
class="function">getTypeName</span> and <span
class="function">getTypeNamespaceURI</span>. These return the SDO type
name and type namespace of the data object, respectively.

Always, calling <span class="function">getRootElementURI</span> on the
document object will return the same value as calling <span
class="function">getNamespaceURI</span> on the root data object.
Essentially, the information is all derived from the first few lines of
the schema file, where there are three distinct pieces of information.
For illustration, here again are the first few lines of the letter.xsd
that we used above.

``` xml
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:letter="http://letterSchema"
            targetNamespace="http://letterSchema">
            
  <xsd:element name="letters" type="letter:FormLetter"/>
  
  <xsd:complexType name="FormLetter" mixed="true">
    .../...
```

The three important values are:

-   `letters`, the name of the document element

-   `FormLetter`, the name of the complex type of the document element.
    This is also the name of the SDO type of the root data object.

-   `http://letterSchema`, the namespace to which the document element
    belongs. This is also the namespaceURI of the SDO type of the root
    data object.

It is part of the XML-SDO mapping rules that when the SDO model is built
from the schema file, the typename and namespaceURI of the SDO types for
the root element are taken from those of the complex type of the
document element, where it exists. Hence in this example the typename of
the root data object is FormLetter. In the event that there is no
separate complex type definition for the document element, when the type
is defined inline and is anonymous, the SDO type name will be the same
as the element name.

The following program loads the letter document and checks the return
values from each of the four calls.

``` php
<?php
/**
 * Finding out what you can about the document and document element
 * This can be quite hard to understand because there are four calls
 * Two calls are made against the document
 * Two calls are made against the root data object and its model
 * Because of the SDO-XML mapping rules and how the SDO model is derived
 * from the XML model, only three possible values can come back from these four calls.
 * Always, $document->getRootElementURI() == (type of root data object)->namespaceURI 
 * Essentially, it all comes form the first few lines of the xsd:
 * <xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 *   xmlns:letter="http://letterSchema"
 *   targetNamespace="http://letterSchema">
 *   <xsd:element name="letters" type="letter:FormLetter"/>
 */

$xmldas = SDO_DAS_XML::create("letter.xsd");
$document = $xmldas->loadFile("letter.xml");
$root_do = $document->getRootDataObject();

/**
 * The "root element name" is the element name of the document element
 * in this case 'letters'
 * This matches the 'name' attribute of the document element in the xsd and matches
 * the element name from the xml
 */
echo "The document element name is " . $document->getRootElementName() . "\n";
assert($document->getRootElementName() == 'letters'); // a property of the document

/**
 * The "root element URI" is the namespace part of the element name of the document element
 * in this case 'http://letterSchema' since 'letters' is in that namespace
 * This is taken from the xsd and matches the namespace picked up from the xml
 */
echo "The document element is in the namespace " . $document->getRootElementURI() . "\n";
assert($document->getRootElementURI() == 'http://letterSchema'); // a property of the document

/**
 * The type name is taken from the SDO model
 * The XML-SDO mapping rules make this either:
 *   The name of the complexType if there is one (in this case there is)
 *   The document element name if there no complexType
 * This is taken from the xsd 
 */
echo "The type name of the root data object is " . $root_do->getTypeName() . "\n";
assert($root_do->getTypeName() == 'FormLetter');  

/**
 * The type's namespaceURI is taken from the SDO model
 * The XML-SDO mapping rules ensure that this will always be the same as 
 * the namepace URI of the document element
 */
echo "The namespaceURI of the root data object is " . $root_do->getTypeNamespaceURI() . "\n";
assert($root_do->getTypeNamespaceURI() == 'http://letterSchema'); 

?>
```

The output from this program is as follows:

``` xml
The document element name is letters
The document element is in the namespace http://letterSchema
The type name of the root data object is FormLetter
The namespaceURI of the root data object is http://letterSchema
```

**示例 \#6 Printing the SDO model**

The XML DAS provides a simple means to see what types and properties
have been loaded. The php "print" or "echo" instruction will print out
the types and properties.

``` php
<?php
/**
 * Illustrate printing out the model
 */

$xmldas = SDO_DAS_XML::create("letter.xsd");
print $xmldas;

?>
```

The output from this program is as follows:

``` xml
object(SDO_XML_DAS)#1 {
18 types have been defined. The types and their properties are::
1. commonj.sdo:BigDecimal
2. commonj.sdo:BigInteger
3. commonj.sdo:Boolean
4. commonj.sdo:Byte
5. commonj.sdo:Bytes
6. commonj.sdo:ChangeSummary
7. commonj.sdo:Character
8. commonj.sdo:DataObject
9. commonj.sdo:Date
10. commonj.sdo:Double
11. commonj.sdo:Float
12. commonj.sdo:Integer
13. commonj.sdo:Long
14. commonj.sdo:Short
15. commonj.sdo:String
16. commonj.sdo:URI
17. http://letterSchema:FormLetter
    - date (commonj.sdo:String)
    - firstName (commonj.sdo:String)
    - lastName (commonj.sdo:String)
18. http://letterSchema:RootType
    - letters (http://letterSchema:FormLetter)
```
