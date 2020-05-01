范例
====

**目录**

-   [Basic usage](/sdo/examples.html#Basic%20usage)
-   [Setting and Getting Property
    Values](/sdo/examples.html#Setting%20and%20Getting%20Property%20Values)
-   [Working with Sequenced Data
    Objects](/sdo/examples.html#Working%20with%20Sequenced%20Data%20Objects)
-   [Reflecting on Service Data
    Objects](/sdo/examples.html#Reflecting%20on%20Service%20Data%20Objects)

Basic usage
-----------

The examples below assume an SDO created with the schema and instance
information shown below, using the XML Data Access Service.

The instance document below describes a single company, called
'MegaCorp', which contains a single department, called 'Advanced
Technologies'. The Advanced Technologies department contains three
employees. The company employeeOfTheMonth is referencing the second
employee, 'Jane Doe'.

``` xml
<?xml version="1.0" encoding="UTF-8" ?> 
<company xmlns="companyNS" name="MegaCorp" 
  employeeOfTheMonth="E0003">
  <departments name="Advanced Technologies" location="NY" number="123">
    <employees name="John Jones" SN="E0001"/>
    <employees name="Jane Doe" SN="E0003"/>
    <employees name="Al Smith" SN="E0004" manager="true"/>
  </departments>
</company>
```

The root element of the schema is a company. The company contains
departments, and each department contains employees. Each element has a
number of attributes to store things like name, serial number, and so
on. Finally, the company also has an IDREF attribute which identifies
one of the employees as the 'employeeOfTheMonth'.

``` xml
<xsd:schema  
  xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:sdo="commonj.sdo"
  xmlns:sdoxml="commonj.sdo/xml"
  xmlns:company="companyNS"
  targetNamespace="companyNS">
  <xsd:element name="company" type="company:CompanyType"/>
  <xsd:complexType name="CompanyType">
    <xsd:sequence>
      <xsd:element name="departments" type="company:DepartmentType" 
        maxOccurs="unbounded"/>
    </xsd:sequence>
    <xsd:attribute name="name" type="xsd:string"/>
    <xsd:attribute name="employeeOfTheMonth" type="xsd:IDREF" 
      sdoxml:propertyType="company:EmployeeType"/> 
  </xsd:complexType>
  <xsd:complexType name="DepartmentType">
    <xsd:sequence>
      <xsd:element name="employees" type="company:EmployeeType"  
        maxOccurs="unbounded"/>
    </xsd:sequence>
    <xsd:attribute name="name" type="xsd:string"/>
    <xsd:attribute name="location" type="xsd:string"/>
    <xsd:attribute name="number" type="xsd:int"/>
  </xsd:complexType>
  <xsd:complexType name="EmployeeType">
    <xsd:attribute name="name" type="xsd:string"/>
    <xsd:attribute name="SN" type="xsd:ID"/>
    <xsd:attribute name="manager" type="xsd:boolean"/>
  </xsd:complexType>
</xsd:schema>
```

The XML Data Access Service maps the schema to an SDO. Attributes such
as "name" become primitive properties, the sequence of employees becomes
a many-valued containment relationship, and so on. Note that the
containment relationships are expressed as one complex type within
another, whereas non-containment references are expressed in terms of ID
and IDREF, with a special **sdoxml:propertyType** attribute specifying
the type of the non-containment reference.

Setting and Getting Property Values
-----------------------------------

The following examples assume **$company** is the root of a tree of data
objects created from the schema and instance document shown above.

**示例 \#1 Access via property name**

Data object properties can be accessed using the object property access
syntax. The following sets the company name to 'Acme'.

``` php
<?php
$company->name = 'Acme';
?>
```

**示例 \#2 Access via property name as array index**

We can also access properties using associative array syntax. The
simplest form of this uses the property name as the array index. For
example, the following sets the company name and gets the
employeeOfTheMonth.

``` php
<?php
$company['name'] = 'UltraCorp';
$eotm = $company['employeeOfTheMonth'];
?>
```

**示例 \#3 Data Object iteration**

We can iterate over the properties of a data object using
<a href="/control-structures/foreach.html" class="link">foreach</a>. The
following iterates over the properties of the employee of the month.

``` php
<?php
  $eotm = $company->employeeOfTheMonth;
  foreach ($eotm as $name => $value) {
      echo "$name: $value\n";
  }
?>
```

which will output:

    name: Jane Doe
    SN: E0003

The 'manager' property is not output, because it has not been set.

**示例 \#4 Access many-valued property by name**

Many-valued data object properties can also be accessed using the object
property name syntax. The following gets the list of departments.

``` php
<?php
$departments = $company->departments;
?>
```

**示例 \#5 Many-valued element access**

We can access individual elements of many-valued properties using array
syntax. The following accesses the first department in the company.

``` php
<?php
$ad_tech_dept = $company->departments[0];
?>
```

**示例 \#6 Many-valued property iteration**

Many-valued properties can also be iterated over using
<a href="/control-structures/foreach.html" class="link">foreach</a>. The
following iterates over the company's departments.

``` php
<?php
  foreach ($company->departments as $department) {
    // ...
  }
?>
```

Each iteration will assign the next department in the list to the
variable **$department**.

**示例 \#7 Chained property access**

We can chain property references on a single line. The following sets
and gets the name of the first department.

``` php
<?php
  $company->departments[0]->name = 'Emerging Technologies';
  $dept_name = $company->departments[0]->name;
?>
```

Using the associative array syntax, this is equivalent to

``` php
<?php
  $company['departments'][0]['name'] = 'Emerging Technologies';
  $dept_name = $company['departments'][0]['name'];
?>
```

In either case, the dept\_name variable is set to 'Emerging
Technologies'.

**示例 \#8 XPath navigation**

The associative array index can be an XPath-like expression. Valid
expressions are defined by an augmented sub-set of XPath.

Two forms of indexing into many-valued properties are supported. The
first is the standard XPath array syntax with the indexing starting at
one, the second is an SDO extension to XPath with an index starting at
zero. The standard syntax is:

``` php
<?php
  $jane_doe = $company["departments[1]/employees[2]"];
?>
```

and the SDO XPath extension syntax is:

``` php
<?php
  $jane_doe = $company["departments.0/employees.1"];
?>
```

Both these examples get the second employee from the first department.

**示例 \#9 XPath querying**

We can use XPath to query and identify parts of a data object based on
instance data. The following retrieves the manager from the 'Advanced
Technologies' department.

``` php
<?php
 $ad_tech_mgr = 
  $company["departments[name='Advanced Technologies']/employees[manager=true]"];
?>
```

**示例 \#10 Creating child data objects**

A data object can be a factory for its child data objects. A child data
object is automatically part of the data graph. The following add a new
employee to the 'Advanced Technologies' department.

``` php
<?php
  $ad_tech_dept = $company["departments[name='Advanced Technologies']"];
  $new_hire = $ad_tech_dept->createDataObject('employees');
  $new_hire->name = 'John Johnson';
  $new_hire->SN = 'E0005';
  $new_hire->manager = false;
?>
```

**示例 \#11 Unset a primitive property**

We can use the <span class="function">isset</span> and <span
class="function">unset</span> functions to test and remove items from
the data object.

The following clears the name of the first department.

``` php
<?php
  unset($company->departments[0]->name);
?>
```

**示例 \#12 Unset a data object**

unset can also be used to remove a data object from the tree. The
following example shows John Jones leaving the company.

``` php
<?php
  unset($company->departments[0]->employees[0]);
?>
```

**示例 \#13 Unset a referenced data object**

The following removes the 'employeeOfTheMonth' from the company. If this
were a containment relationship then the employee would be removed from
the company (probably not a good idea to sack your best employee each
month!), but since this is a non-containment reference, the employee
being referenced will remain in the department in the company, but will
no longer be accessible via the employeeOfTheMonth property.

``` php
<?php
  if (isset($company->employeeOfTheMonth)) {
    unset($company->employeeOfTheMonth);
  }
?>
```

**示例 \#14 Access via property index**

Data object properties can be accessed via their property index using
array syntax. The property index is the position at which the property's
definition appears in the model (in this case the xml schema). We can
see from the schema listing above that the company name attribute is the
second company property (the SDO interface makes no distinction between
XML attributes and elements). The following sets the company name to
'Acme', with the same result as
<a href="/sdo/examples.html#" class="link">Access via property name</a>

``` php
<?php
  $company[1] = 'Acme';
?>
```

Using the index directly in this way is likely to be fragile. Normally
the property name syntax should be preferred, but the property index may
be required in special cases.

Working with Sequenced Data Objects
-----------------------------------

Sequenced data objects are SDOs which can track property ordering across
the properties of a data object. They can also contain unstructured text
elements (text element which do not belong to any of the SDO's
properties). Sequenced data objects are useful for working with XML
documents which allow unstructured text (i.e. mixed=true) or if the
elements can be interleaved (

    <A/><B/><A/>

). This can occur for example when the schema defines maxOccurs\>1 on a
element which is a complexType with a choice order indicator.

The examples below assume an SDO created with the following schema and
instance information, using the XML Data Access Service.

The schema below describes the format of a letter. The letter can
optionally contain three properties; date, firstName, and lastName. The
schema states **mixed="true"** which means that unstructured text can be
interspersed between the three properties.

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

The following is an instance letter document. It contains the three
letter properties; date, firstName and lastName, and has unstructured
text elements for the address and letter body.

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

When loaded, the letter data object will have the sequence and property
indices shown in the table below:

| Sequence Index | Property Index:Name | Value                            |
|----------------|---------------------|----------------------------------|
| 0              | 0:date              | March 1, 2005                    |
| 1              | \-                  | Mutual of Omaha                  |
| 2              | \-                  | Wild Kingdom, USA                |
| 3              | \-                  | Dear                             |
| 4              | 1:firstName         | Casy                             |
| 5              | 2:lastName          | Crocodile                        |
| 6              | \-                  | Please buy more shark repellent. |
| 7              | \-                  | Your premium is past due.        |

To ensure sequence indices are maintained, sequenced data objects should
be manipulated through the SDO\_Sequence interface. This allows the data
object's instance data to be manipulated in terms of the sequence index
as opposed to the property index (shown in the table above). The
following examples assume the letter instance has been loaded into a
data object referenced by the variable **$letter**.

**示例 \#1 Getting the SDO\_Sequence interface**

We obtain a data object's sequence using the <span
class="function">getSequence</span> method. The follow gets the sequence
for the letter data object.

``` php
<?php
  $letter_seq = $letter->getSequence();
?>
```

All subsequent examples assume that the **$letter\_seq** variable has
been assigned the sequence for the letter data object.

**示例 \#2 Get/set sequence values**

We can get and set individual values (including unstructured text) using
the sequence index. The following sets the firstName to 'Snappy' and
gets the last sequence values (the unstructured text, 'Your premium is
past due.').

``` php
<?php
  $letter_seq[4] = 'Snappy';
  $text = $letter_seq[count($letter_seq) - 1];
?>
```

**示例 \#3 Sequence iteration**

We can iterate through the individual sequence values using
<a href="/control-structures/foreach.html" class="link">foreach</a>. The
following runs through the individual values in sequence order.

``` php
<?php
foreach ($letter->getSequence() as $value) {
    // ...
}
?>
```

**示例 \#4 Sequence versus Data Object**

Setting values through the data object interface may result in the value
not being part of the sequence. A value set through the data object will
only be accessible through the sequence if the property was already part
of the sequence. The following example sets the lastName through the
data object and gets it through the sequence. This is fine because
lastName already exists in the sequence. If it had not previously been
set, then lastName would be set to 'Smith', but would not be part of the
sequence.

``` php
<?php
  $letter[2] = 'Smith';
  $last_name = $letter_seq[5];
?>
```

**示例 \#5 Adding to a sequence**

We can add new values to a sequence using the <span
class="function">SDO\_Sequence::insert</span> method. The following
examples assume that the 'firstName' and 'lastName' properties are
initially unset.

``` php
<?php
  // Append a firstName value to the sequence
  // value: 'Smith'
  // sequence index: NULL (append)
  // propertyIdentifier: 1 (firtName property index)
  $letter_seq->insert('Smith', NULL, 1);

  // Append a lastName value to the sequence
  // value: 'Jones'
  // sequence index: NULL (append)
  // propertyIdentifier: 'lastName' (lastName property name)
  $letter_seq->insert('Jones', NULL, 'lastName');

  // Append unstructured text
  // value: 'Cancel Subscription.'
  // sequence index: absent (append)
  // propertyIdentifier: absent (unstructured text)
  $letter_seq->insert('Cancel Subscription.');

  // Insert new unstructured text.  Subsequent sequence values
  // are shifted up.                                       
  // value: 'Care of:'
  // sequence index: 1 (insert as second element)
  // propertyIdentifier: absent (unstructured text)
  $letter_seq->insert('Care of:', 1);
?>
```

**示例 \#6 Removing from a sequence**

We can use the <span class="function">isset</span> and <span
class="function">unset</span> functions to test and remove items from
the sequence (Note: <span class="function">unset</span> currently leaves
the values in the data object, but this behaviour is likely to change to
also remove the data from the data object). A sequence behaves like a
contiguous list; therefore, removing items from the middle will shift
entries at higher indices down. The following example tests to see if
the first sequence element is set and unsets it if is.

``` php
<?php
  if (isset($letter_seq[0])) {
    unset($letter_seq[0]);
  }
?>
```

Reflecting on Service Data Objects
----------------------------------

SDOs have a knowledge of the structure they have been created to
represent (the model). For example, a Company SDO created using
<a href="/sdo/examples.html" class="link">the Company XML schema</a>
above would only be permitted to contain DepartmentType data objects
which in turn could only contain EmployeeType data objects.

Sometimes it is useful to be able to access this model information at
runtime. For example, this could be used to automatically generate a
user interface for populating a data object. The model information is
accessed using reflection.

**示例 \#1 Reflecting on a Data Object**

The following example shows how we can reflect on an empty Employee data
object.

``` php
<?php
  // Create the employee data object (e.g. from an XML Data Access Service)
  $employee = ...;
  $reflection = new SDO_Model_ReflectionDataObject($employee);
  print($reflection);
?>
```

以上例程会输出：

    object(SDO_Model_ReflectionDataObject)#4 { - ROOT OBJECT - Type { 
    companyNS:EmployeeType[3] { commonj.sdo:String $name; 
    commonj.sdo:String $SN; commonj.sdo:Boolean $manager; } }

Using print on the SDO\_Model\_ReflectionDataObject writes out the data
object's model. We can see from the output how the type
companyNS:EmployeeType has three properties and we can see the names of
the properties along with their types. Note, the primitive types are
listed as SDO types (e.g. commonj.sdo namespace, String type). It is
worth noting that this is the SDO model and when these are surfaced to
an application they can be treated as the PHP equivalent types (e.g.
string and boolean).

**示例 \#2 Accessing the type information**

We can query the type information of a data object using reflection. The
following example checks the type corresponds to a data object rather
than a primitive and then iterates through the properties of the type,
writing out the name of each property ($type and $property are
SDO\_Model\_Type and SDO\_Model\_Property objects, respectively).

``` php
<?php
    // Create the employee data object (e.g. from an XML Data Access Service)
    $employee = ...;
    $reflection = new SDO_Model_ReflectionDataObject($employee);
    $type = $reflection->getType();
    if (! $type->isDataType()) {
        foreach ($type->getProperties() as $property) {
            print $property->getName() . "\n";
        }
    }
?>
```

以上例程会输出：

    name
    SN
    manager
