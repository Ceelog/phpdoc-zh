Data Access Services
--------------------

The table below lists the currently provided SDO Data Access Services:

| DAS Name                                                          | Description                                                                                                                                      |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <a href="/ref/sdo-das-xml.html" class="link">SDO_DAS_XML</a>      | An XML Data Access Service supporting reading/writing SDOs as XML documents.                                                                     |
| <a href="/ref/sdodasrel.html" class="link">SDO_DAS_Relational</a> | A PDO-based Data Access Service supporting reading/writing SDO to relational databases. Implements an optimistic concurrency policy for updates. |

预定义类
--------

SDO consists of three sets of interfaces. The first set covers those
interfaces for use by typical SDO applications. These are identified by
the package prefix 'SDO\_'. The second set is those used to reflect on,
and work with, the model of a data object. These are identified by the
package prefix 'SDO\_Model\_'. Finally, the third set are those use by
Data Access Service implementations and are identified by the package
prefix 'SDO\_DAS\_'. The majority of SDO users will not need to use or
understand the 'SDO\_Model\_' and 'SDO\_DAS\_' interfaces.

SDO Application Programmer Interface
------------------------------------

<span class="classname">SDO\_DataObject</span>
----------------------------------------------

The main interface through which data objects are manipulated. In
addition to the methods below, SDO\_DataObject extends the ArrayAccess,
SDO\_PropertyAccess (defines
<a href="/language/oop5/overloading.html#object.get" class="link">__get()</a>
/
<a href="/language/oop5/overloading.html#object.set" class="link">__set()</a>
methods for property access overloading), Iterator, and Countable
interfaces.

方法
----

-   <a href="/ref/sdo.html#SDO_DataObject::getSequence" class="link">getSequence</a> -
    get the sequence for the data object

-   <a href="/ref/sdo.html#SDO_DataObject::createDataObject" class="link">createDataObject</a> -
    create a child data object

-   <a href="/ref/sdo.html#SDO_DataObject::clear" class="link">clear</a> -
    unset the properties of a data object

-   <a href="/ref/sdo.html#SDO_DataObject::getContainer" class="link">getContainer</a> -
    get the container (also known as 'parent') of this data object

-   <a href="/ref/sdo.html#SDO_DataObject::getTypeName" class="link">getTypeName</a> -
    get the name of the type for this data object

-   <a href="/ref/sdo.html#SDO_DataObject::getTypeNamespaceURI" class="link">getTypeNamespaceURI</a> -
    get the namespace URI of the type for this data object

<span class="classname">SDO\_Sequence</span>
--------------------------------------------

The interface through which sequenced data objects can be accessed to
preserve ordering across a data object's properties and to allow
unstructured text. SDO\_Sequence preserves contiguous indices and
therefore inserting or removing elements may shift other elements up or
down. In addition to the methods below, SDO\_Sequence extends the
ArrayAccess, Iterator and Countable interface.

方法
----

-   <a href="/ref/sdo.html#SDO_Sequence::getProperty" class="link">getProperty</a> -
    get the property for a given sequence index

-   <a href="/ref/sdo.html#SDO_Sequence::move" class="link">move</a> -
    move an element from one property index to another

-   <a href="/ref/sdo.html#SDO_Sequence::insert" class="link">insert</a> -
    insert a new value into the sequence

<span class="classname">SDO\_List</span>
----------------------------------------

The interface through which many-valued properties are manipulated. In
addition to the method defined below, SDO\_List extends ArrayAccess,
Iterator and Countable. SDO\_List preserves contiguous indices and
therefore inserting or removing elements may shift other elements up or
down.

方法
----

-   <a href="/ref/sdo.html#SDO_List::insert" class="link">insert</a> -
    insert a new value into the list

<span class="classname">SDO\_DataFactory</span>
-----------------------------------------------

The interface through which data objects can be created. A Data Access
Service is responsible for populating the model (i.e. configuring the
data factory with the type and structure information for the data
objects it can create.) for the factory and can then optionally return
an instance of, or implement, the SDO\_DataFactory interface.

方法
----

-   <a href="/ref/sdo.html#SDO_DataFactory::create" class="link">create</a> -
    create a new data object

<span class="classname">SDO\_Exception</span>
---------------------------------------------

An SDO\_Exception is thrown when the caller's request cannot be
completed. The subclasses of SDO\_Exception are:

-   SDO\_PropertyNotSetException - the property specified exists but has
    not been set or does not have a default value

-   SDO\_PropertyNotFoundException - the property specified is not part
    of the data object's type

-   SDO\_TypeNotFoundException - the specified namespace URI or type
    name is unknown

-   SDO\_InvalidConversionException - conversion between the types of
    the assignment is not possible

-   SDO\_IndexOutOfBoundsException - the numeric index into a data
    object, sequence or list is not in the valid range

-   SDO\_UnsupportedOperationException - the request cannot be completed
    because it is not allowed, for example an attempt to set a read-only
    property.

方法
----

One method is added to those inherited from the built in
<a href="/language/exceptions/extending.html" class="link">Exception</a>
class:

-   <a href="/ref/sdo.html#SDO_Exception::getCause" class="link">getCause</a> -
    get the cause of this SDO\_Exception

SDO Reflection Application Programmer Interfaces
------------------------------------------------

<span class="classname">SDO\_Model\_ReflectionDataObject</span>
---------------------------------------------------------------

The main interface used to reflect on a data object instance to obtain
its model type and property information. It is designed to follow the
reflection pattern introduced in PHP 5.

构造函数
--------

-   <a href="/ref/sdo.html#SDO_Model_ReflectionDataObject::__construct" class="link">__construct</a> -
    construct a new SDO\_Model\_ReflectionDataObject.

方法
----

-   <a href="/ref/sdo.html#SDO_Model_ReflectionDataObject::export" class="link">export</a> -
    get a string describing the data object.

-   <a href="/ref/sdo.html#SDO_Model_ReflectionDataObject::getType" class="link">getType</a> -
    get the SDO\_Model\_Type for the data object.

-   <a href="/ref/sdo.html#SDO_Model_ReflectionDataObject::getInstanceProperties" class="link">getInstanceProperties</a> -
    get the instance properties of the data object.

-   <a href="/ref/sdo.html#SDO_Model_ReflectionDataObject::getContainmentProperty" class="link">getContainmentProperty</a> -
    get the property which defines the containment relationship to the
    data object.

<span class="classname">SDO\_Model\_Type</span>
-----------------------------------------------

The interface through which a data object's type information can be
retrieved. This interface can be used to find out the type name and
namespace URI of the type, whether the type allow open content, and so
on.

方法
----

-   <a href="/ref/sdo.html#SDO_Model_Type::getName" class="link">getName</a> -
    get the name of the type.

-   <a href="/ref/sdo.html#SDO_Model_Type::getNamespaceURI" class="link">getNamespaceURI</a> -
    get the namespace URI of the type.

-   <a href="/ref/sdo.html#SDO_Model_Type::isInstance" class="link">isInstance</a> -
    test for a data object being an instance of the type.

-   <a href="/ref/sdo.html#SDO_Model_Type::getProperties" class="link">getProperties</a> -
    get the properties of the type.

-   <a href="/ref/sdo.html#SDO_Model_Type::getProperty" class="link">getProperty</a> -
    get a property of the type.

-   <a href="/ref/sdo.html#SDO_Model_Type::isDataType" class="link">isDataType</a> -
    test to see if this type is a primitive scalar type.

-   <a href="/ref/sdo.html#SDO_Model_Type::isSequencedType" class="link">isSequencedType</a> -
    test to see if this is a sequenced type.

-   <a href="/ref/sdo.html#SDO_Model_Type::isOpenType" class="link">isOpenType</a> -
    test to see if this is an open type.

-   <a href="/ref/sdo.html#SDO_Model_Type::isAbstractType" class="link">isAbstractType</a> -
    test to see if this is an abstract type.

-   <a href="/ref/sdo.html#SDO_Model_Type::getBaseType" class="link">getBaseType</a> -
    get the base type of this type (if one exists).

<span class="classname">SDO\_Model\_Property</span>
---------------------------------------------------

The interface through which a data object's property information can be
retrieved. This interface can be used to find out the type of a
property, whether a property has a default value, whether the property
is contained or reference by its parent, its cardinality, and so on.

方法
----

-   <a href="/ref/sdo.html#SDO_Model_Property::getName" class="link">getName</a> -
    get the name of the property.

-   <a href="/ref/sdo.html#SDO_Model_Property::getType" class="link">getType</a> -
    get the type of the property.

-   <a href="/ref/sdo.html#SDO_Model_Property::isMany" class="link">isMany</a> -
    test to see if the property is many-valued.

-   <a href="/ref/sdo.html#SDO_Model_Property::isContainment" class="link">isContainment</a> -
    test to see if the property describes a containment relationship.

-   <a href="/ref/sdo.html#SDO_Model_Property::getContainingType" class="link">getContainingType</a> -
    get the type which contains this property.

-   <a href="/ref/sdo.html#SDO_Model_Property::getDefault" class="link">getDefault</a> -
    get the default value for a property.

SDO Data Access Service Developer Interfaces
--------------------------------------------

<span class="classname">SDO\_DAS\_DataObject</span>
---------------------------------------------------

The interface through which a Data Access Service can access a data
object's
<a href="/ref/sdo.html#SDO_DAS_ChangeSummary" class="link">SDO_DAS_ChangeSummary</a>.
The change summary is used by the Data Access Service to check for
conflicts when applying changes back to a data source.

方法
----

-   <a href="/ref/sdo.html#SDO_DAS_DataObject::getChangeSummary" class="link">getChangeSummary</a> -
    get the change summary for a data object

<span class="classname">SDO\_DAS\_ChangeSummary</span>
------------------------------------------------------

The interface through which the change history of a data object is
accessed. The change summary holds information for any modifications on
a data object which occurred since logging was activated. In the case of
deletions and modifications, the old values are also held in the change
summary.

If logging is no longer active then the change summary only holds
changes made up to the point when logging was deactivated. Reactivating
logging clears the change summary. This is useful when a set of changes
have been written out by a DAS and the data object is to be reused.

方法
----

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::beginLogging" class="link">beginLogging</a> -
    begin logging changes made to a data object

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::endLogging" class="link">endLogging</a> -
    end logging changes made to a data object

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::isLogging" class="link">isLogging</a> -
    test to see if change logging is on

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::getChangedDataObjects" class="link">getChangedDataObjects</a> -
    get a list of the data objects which have been changed

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::getChangeType" class="link">getChangeType</a> -
    get the type of change which has been made to a data object

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::getOldValues" class="link">getOldValues</a> -
    get a list of old values for a data object

-   <a href="/ref/sdo.html#SDO_DAS_ChangeSummary::getOldContainer" class="link">getOldContainer</a> -
    get the old container data object for a deleted data object

<span class="classname">SDO\_DAS\_Setting</span>
------------------------------------------------

The interface through which the old value for a property is accessed. A
list of settings is returned by the change summary method
<a href="/ref/sdo.html#SDO_DAS_ChangeSummary::getOldValues" class="link">getOldValues</a>.

方法
----

-   <a href="/ref/sdo.html#SDO_DAS_Setting::getPropertyIndex" class="link">getPropertyIndex</a> -
    get the property index for the changed property

-   <a href="/ref/sdo.html#SDO_DAS_Setting::getPropertyName" class="link">getPropertyName</a> -
    get the property name for the changed property

-   <a href="/ref/sdo.html#SDO_DAS_Setting::getValue" class="link">getValue</a> -
    get the old value for the changed property

-   <a href="/ref/sdo.html#SDO_DAS_Setting::getListIndex" class="link">getListIndex</a> -
    get the list index for the old value if it was part of a many-valued
    property

-   <a href="/ref/sdo.html#SDO_DAS_Setting::isSet" class="link">isSet</a> -
    test to see if the property was set prior to being modified

<span class="classname">SDO\_DAS\_DataFactory</span>
----------------------------------------------------

The interface for constructing the model for an SDO\_DataObject. The
SDO\_DAS\_DataFactory is an abstract class providing a static method
which returns a concrete data factory implementation. The implementation
is used by Data Access Services to create an SDO model from their model.
For example, a Relational Data Access Service might create and populate
an SDO\_DAS\_DataFactory model based on a schema for a relational
database.

方法
----

-   <a href="/ref/sdo.html#SDO_DAS_DataFactory::getDataFactory" class="link">getDataFactory</a> -
    static methods for getting a concrete data factory instance

<!-- -->

-   <a href="/ref/sdo.html#SDO_DAS_DataFactory::addType" class="link">addType</a> -
    add a new type to the SDO model

<!-- -->

-   <a href="/ref/sdo.html#SDO_DAS_DataFactory::addPropertyToType" class="link">addPropertyToType</a> -
    add a new property to a type definition in the SDO model

SDO\_DAS\_ChangeSummary::beginLogging
=====================================

Begin change logging

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::beginLogging</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Begin logging changes made to the SDO\_DataObject.

### 参数

None.

### 返回值

None.

SDO\_DAS\_ChangeSummary::endLogging
===================================

End change logging

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::endLogging</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

End logging changes made to an SDO\_DataObject.

### 参数

None.

### 返回值

None.

SDO\_DAS\_ChangeSummary::getChangeType
======================================

Get the type of change made to an SDO\_DataObject

### 说明

<span class="type">int</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::getChangeType</span> ( <span
class="methodparam"><span class="type">SDO\_DataObject</span>
`$dataObject`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the type of change which has been made to the supplied
SDO\_DataObject.

### 参数

`dataObject`  
The SDO\_DataObject which has been changed.

### 返回值

The type of change which has been made. The change type is expressed as
an enumeration and will be one of the following four values:

-   SDO\_DAS\_ChangeSummary::NONE

-   SDO\_DAS\_ChangeSummary::MODIFICATION

-   SDO\_DAS\_ChangeSummary::ADDITION

-   SDO\_DAS\_ChangeSummary::DELETION

SDO\_DAS\_ChangeSummary::getChangedDataObjects
==============================================

Get the changed data objects from a change summary

### 说明

<span class="type">SDO\_List</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::getChangedDataObjects</span>
( <span class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get an SDO\_List of the SDO\_DataObjects which have been changed. These
data objects can then be used to identify the types of change made to
each, along with the old values.

### 参数

None.

### 返回值

Returns an SDO\_List of SDO\_DataObjects.

SDO\_DAS\_ChangeSummary::getOldContainer
========================================

Get the old container for a deleted SDO\_DataObject

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::getOldContainer</span> (
<span class="methodparam"><span class="type">SDO\_DataObject</span>
`$data_object`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the old container (SDO\_DataObject) for a deleted SDO\_DataObject.

### 参数

`data_object`  
The SDO\_DataObject which has been deleted and whose container we wish
to identify.

### 返回值

The old containing data object of the deleted SDO\_DataObject.

SDO\_DAS\_ChangeSummary::getOldValues
=====================================

Get the old values for a given changed SDO\_DataObject

### 说明

<span class="type">SDO\_List</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::getOldValues</span> ( <span
class="methodparam"><span class="type">SDO\_DataObject</span>
`$data_object`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get a list of the old values for a given changed SDO\_DataObject.
Returns a list of SDO\_DAS\_Settings describing the old values for the
changed properties of the SDO\_DataObject.

### 参数

`data_object`  
The data object which has been changed.

### 返回值

A list of SDO\_DAS\_Settings describing the old values for the changed
properties of the SDO\_DataObject. If the change type is
SDO\_DAS\_ChangeSummary::ADDITION, this list is empty.

SDO\_DAS\_ChangeSummary::isLogging
==================================

Test to see whether change logging is switched on

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_DAS\_ChangeSummary::isLogging</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see whether change logging is switched on.

### 参数

None.

### 返回值

Returns **`TRUE`** if change logging is on, otherwise returns
**`FALSE`**.

SDO\_DAS\_DataFactory::addPropertyToType
========================================

Adds a property to a type

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_DataFactory::addPropertyToType</span> (
<span class="methodparam"><span class="type">string</span>
`$parent_type_namespace_uri`</span> , <span class="methodparam"><span
class="type">string</span> `$parent_type_name`</span> , <span
class="methodparam"><span class="type">string</span>
`$property_name`</span> , <span class="methodparam"><span
class="type">string</span> `$type_namespace_uri`</span> , <span
class="methodparam"><span class="type">string</span> `$type_name`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Adds a property to a type. The type must already be known to the
SDO\_DAS\_DataFactory (i.e. have been added using addType()). The
property becomes a property of the type. This is how the graph model for
the structure of an SDO\_DataObject is built.

### 参数

`parent_type_namespace_uri`  
The namespace URI for the parent type.

`parent_type_name`  
The type name for the parent type.

`property_name`  
The name by which the property will be known in the parent type.

`type_namespace_uri`  
The namespace URI for the type of the property.

`type_name`  
The type name for the type of the property

`options`  
This array holds one or more key=\>value pairs to set attribute values
for the property. The optional keywords are:

`many`  
A flag to say whether the property is many-valued. A value of 'true'
adds the property as a many-valued property (default is 'false').

`readOnly`  
A flag to say whether the property is read-only. A value of 'true' means
the property value cannot be modified through the SDO application APIs
(default is 'false').

`containment`  
A flag to say whether the property is contained by the parent. A value
of 'true' means the property is contained by the parent. A value of
'false' results in a non-containment reference (default is 'true'). This
flag is only interpreted when adding properties which are data object
types, otherwise it is ignored.

`default`  
A default value for the property. Omitting this key means that the
property does not have a default value. A property can only have a
default value if it is a single-valued data type (primitive).

### 返回值

None.

### 更新日志

| 版本  | 说明                                                                                                   |
|-------|--------------------------------------------------------------------------------------------------------|
| 0.5.2 | Optional parameters `many`, `readOnly`, and `containment` deprecated in favour of the `options` array. |

### 范例

**示例 \#1 A <span
class="function">SDO\_DAS\_DataFactory::addPropertyToType</span>
example**

The following adds an 'addressline' property to a Person type. The
person type is identified by its namespace, 'PersonNS', and type name,
'PersonType'. The type of the 'addressline' property is a many-valued
SDO data type (primitive) with namespace 'commonj.sdo' and type name
'String'.

``` php
<?php
  $df->addPropertyToType('PersonNS', 'PersonType',
    'addressline', 'commonj.sdo', 'String', array('many'=>true));
?>
```

SDO\_DAS\_DataFactory::addType
==============================

Add a new type to a model

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DAS\_DataFactory::addType</span> ( <span
class="methodparam"><span class="type">string</span>
`$type_namespace_uri`</span> , <span class="methodparam"><span
class="type">string</span> `$type_name`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Add a new type to the SDO\_DAS\_DataFactory, defined by its namespace
and type name. The type becomes part of the model of data objects that
the data factory can create.

### 参数

`type_namespace_uri`  
The namespace of the type.

`type_name`  
The name of the type.

`options`  
This array holds one or more key=\>value pairs to set attribute values
for the type. The optional keywords are:

`open`  
A flag to say whether the type is open. An SDO\_DataObject whose type is
open can have properties added to them which are not described by the
type. This capability is used to support working with XML documents
whose schema support open content such as that described by an
\<xsd:any\> element. The default value is 'false'.

`sequenced`  
A flag to say whether the type is sequenced. Sequenced types can have
the ordering across properties preserved and can contain unstructured
text. The default value is 'false'. For more information on sequenced
types see the section on
<a href="/sdo/examples.html#Working%20with%20Sequenced%20Data%20Objects" class="link">Working with Sequenced Data Objects</a>.

`basetype`  
If specified, an array of namespace URI and type name strings for the
type from which this type is derived. An example of the use of base
types is when a type derived in an XML schema inherits from another type
by using \<extension base="..."\>.

### 返回值

None.

### 范例

**示例 \#1 A <span
class="function">SDO\_DAS\_DataFactory::addType</span> example**

The following adds a new data object type of 'CompanyType' where that
type belongs to the namespace 'CompanyNS'.

``` php
<?php
  $df->addType('CompanyNS', 'CompanyType');
?>
```

SDO\_DAS\_DataFactory::getDataFactory
=====================================

Get a data factory instance

### 说明

<span class="type">SDO\_DAS\_DataFactory</span> <span
class="methodname">SDO\_DAS\_DataFactory::getDataFactory</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Static method to get an instance of an SDO\_DAS\_DataFactory. This
instance is initially only configured with the basic SDO types. A Data
Access Service is responsible for populating the data factory model and
then allowing PHP applications to create SDOs based on the model through
the SDO\_DataFactory interface. PHP applications should always obtain a
data factory from a configured Data Access Service, not through this
interface.

### 参数

None.

### 返回值

Returns an SDO\_DAS\_DataFactory.

SDO\_DAS\_DataObject::getChangeSummary
======================================

Get a data object's change summary

### 说明

<span class="type">SDO\_DAS\_ChangeSummary</span> <span
class="methodname">SDO\_DAS\_DataObject::getChangeSummary</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the SDO\_DAS\_ChangeSummary for an SDO\_DAS\_DataObject, or NULL if
it does not have one.

### 参数

None.

### 返回值

Returns the SDO\_DAS\_ChangeSummary for an SDO\_DAS\_DataObject, or NULL
if it does not have one.

SDO\_DAS\_Setting::getListIndex
===============================

Get the list index for a changed many-valued property

### 说明

<span class="type">int</span> <span
class="methodname">SDO\_DAS\_Setting::getListIndex</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the list index for a modification made to an element of a
many-valued property. For example, if we modified the third element of a
many-valued property we could obtain an SDO\_DAS\_Setting from the
change summary corresponding to that modification. A call to <span
class="function">getListIndex</span> on that setting would return the
value 2 (lists are indexed from zero).

### 参数

None.

### 返回值

The list index for the element of the many-valued property which has
been changed.

SDO\_DAS\_Setting::getPropertyIndex
===================================

Get the property index for a changed property

### 说明

<span class="type">int</span> <span
class="methodname">SDO\_DAS\_Setting::getPropertyIndex</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the property index for the changed property. This index
identifies the property which was modified in data object.

### 参数

None.

### 返回值

The property index for a changed property.

SDO\_DAS\_Setting::getPropertyName
==================================

Get the property name for a changed property

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_DAS\_Setting::getPropertyName</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the property name for the changed property. This name identifies
the property which was modified in data object.

### 参数

None.

### 返回值

The property name for a changed property.

SDO\_DAS\_Setting::getValue
===========================

Get the old value for the changed property

### 说明

<span class="type">mixed</span> <span
class="methodname">SDO\_DAS\_Setting::getValue</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the old value for the changed property. This can be used by a
Data Access Service when writing updates to a data source. The DAS uses
the old value to detect conflicts by comparing it with the current value
in the data source. If they do not match, then the data source has been
updated since the data object was originally populated, and therefore
writing any new updates risks compromising the integrity of the data.

### 参数

None.

### 返回值

Returns the old value of the changed property.

SDO\_DAS\_Setting::isSet
========================

Test whether a property was set prior to being modified

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_DAS\_Setting::isSet</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test whether a property was set prior to being modified. If it was set
prior to being modified then the SDO\_DAS\_Setting will also contain the
old value.

### 参数

None.

### 返回值

Returns **`TRUE`** if the property was set prior to being modified,
otherwise returns **`FALSE`**.

SDO\_DataFactory::create
========================

Create an SDO\_DataObject

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DataFactory::create</span> ( <span
class="methodparam"><span class="type">string</span>
`$type_namespace_uri`</span> , <span class="methodparam"><span
class="type">string</span> `$type_name`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Create a new SDO\_DataObject given the data object's namespace URI and
type name.

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
known to this data factory.

SDO\_DataObject::clear
======================

Clear an SDO\_DataObject's properties

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_DataObject::clear</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Clear an SDO\_DataObject's properties. Read-only properties are
unaffected. Subsequent calls to isset() for the data object will return
**`FALSE`**.

### 参数

None.

### 返回值

No return values.

SDO\_DataObject::createDataObject
=================================

Create a child SDO\_DataObject

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SDO\_DataObject::createDataObject</span> ( <span
class="methodparam"><span class="type">mixed</span> `$identifier`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Create a child SDO\_DataObject of the default type for the property
identified. The data object is automatically inserted into the tree and
a reference to it is returned.

### 参数

`identifier`  
Identifies the property for the data object type to be created. Can be
either a property name (string), a property index (int), or an
<a href="/ref/sdo.html#SDO_Model_Property" class="link">SDO_Model_Property</a>.

### 返回值

Returns the newly created SDO\_DataObject.

### 错误／异常

`SDO_PropertyNotFoundException`  
Thrown if the identifier does not correspond to a property of the data
object.

SDO\_DataObject::getContainer
=============================

Get a data object's container

### 说明

<span class="type">SDO\_DataObject</span> <span
class="methodname">SDO\_DataObject::getContainer</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the data object which contains this data object.

### 参数

None.

### 返回值

Returns the SDO\_DataObject which contains this SDO\_DataObject, or
returns NULL if this is a root SDO\_DataObject (i.e. it has no
container).

SDO\_DataObject::getSequence
============================

Get the sequence for a data object

### 说明

<span class="type">SDO\_Sequence</span> <span
class="methodname">SDO\_DataObject::getSequence</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Return the SDO\_Sequence for this SDO\_DataObject. Accessing the
SDO\_DataObject through the SDO\_Sequence interface acts on the same
SDO\_DataObject instance data, but preserves ordering across properties.

### 参数

None.

### 返回值

The SDO\_Sequence for this SDO\_DataObject, or returns NULL if the
SDO\_DataObject is not of a type which can have a sequence.

SDO\_DataObject::getTypeName
============================

Return the name of the type for a data object

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_DataObject::getTypeName</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Return the name of the type for a data object. A convenience method
corresponding to SDO\_Model\_ReflectionDataObject::getType().getName().

### 参数

None.

### 返回值

The name of the type for the data object.

SDO\_DataObject::getTypeNamespaceURI
====================================

Return the namespace URI of the type for a data object

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_DataObject::getTypeNamespaceURI</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Return the namespace URI of the type for a data object. A convenience
method corresponding to
SDO\_Model\_ReflectionDataObject::getType().getNamespaceURI().

### 参数

None.

### 返回值

The namespace URI of the type for the data object.

SDO\_Exception::getCause
========================

Get the cause of the exception

### 说明

<span class="type">mixed</span> <span
class="methodname">SDO\_Exception::getCause</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the cause of this exception or NULL if the cause is nonexistent
or unknown. Typically the cause will be an SDO\_CPPException object,
which may be used to obtain additional diagnostic information.

### 参数

None.

### 返回值

Returns the cause of this exception or NULL if the cause is nonexistent
or unknown.

SDO\_List::insert
=================

Insert into a list

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_List::insert</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$index`</span>
\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Insert a new element at a specified position in the list. All subsequent
list items are moved up.

### 参数

`value`  
The new value to be inserted. This can be either a primitive or an
SDO\_DataObject.

`index`  
The position at which to insert the new element. If this argument is not
specified then the new value will be appended.

### 返回值

None.

### 错误／异常

`SDO_IndexOutOfBoundsException`  
Thrown if the list index is less than zero or greater than the size of
the list.

`SDO_InvalidConversionException`  
Thrown if the type of the new value does not match the type for the list
(e.g. the type of the many-valued property that the list represents).

SDO\_Model\_Property::getContainingType
=======================================

Get the SDO\_Model\_Type which contains this property

### 说明

<span class="type">SDO\_Model\_Type</span> <span
class="methodname">SDO\_Model\_Property::getContainingType</span> (
<span class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the SDO\_Model\_Type which contains this property.

### 参数

None.

### 返回值

Returns the SDO\_Model\_Type which contains this property.

SDO\_Model\_Property::getDefault
================================

Get the default value for the property

### 说明

<span class="type">mixed</span> <span
class="methodname">SDO\_Model\_Property::getDefault</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the default value for the property. Only primitive data type
properties can have default values.

### 参数

None.

### 返回值

Returns the default value for the property.

SDO\_Model\_Property::getName
=============================

Get the name of the SDO\_Model\_Property

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_Model\_Property::getName</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the name of the SDO\_Model\_Property.

### 参数

None.

### 返回值

Returns the name of the SDO\_Model\_Property.

SDO\_Model\_Property::getType
=============================

Get the SDO\_Model\_Type of the property

### 说明

<span class="type">SDO\_Model\_Type</span> <span
class="methodname">SDO\_Model\_Property::getType</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the SDO\_Model\_Type of the property. The SDO\_Model\_Type describes
the type information for the property, such as its type name, namespace
URI, whether it is a primitive data type, and so on.

### 参数

None.

### 返回值

Returns the SDO\_Model\_Type describing the property's type information.

SDO\_Model\_Property::isContainment
===================================

Test to see if the property defines a containment relationship

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Property::isContainment</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see if the property corresponds to a containment relationship.
Returns **`TRUE`** if the property defines a containment relationship,
or **`FALSE`** if it is reference.

### 参数

None.

### 返回值

Returns **`TRUE`** if the property defines a containment relationship,
or **`FALSE`** if it is reference.

SDO\_Model\_Property::isMany
============================

Test to see if the property is many-valued

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Property::isMany</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see if the property is many-valued. Returns **`TRUE`** if this
is a many-valued property, otherwise returns **`FALSE`**.

### 参数

None.

### 返回值

Returns **`TRUE`** if this is a many-valued property, otherwise returns
**`FALSE`**.

SDO\_Model\_ReflectionDataObject::\_\_construct
===============================================

Construct an SDO\_Model\_ReflectionDataObject

### 说明

<span
class="methodname">SDO\_Model\_ReflectionDataObject::\_\_construct</span>
( <span class="methodparam"><span class="type">SDO\_DataObject</span>
`$data_object`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Construct an SDO\_Model\_ReflectionDataObject to reflect on an
SDO\_DataObject. Reflecting on an SDO\_DataObject gives access to
information about its model. The model contains information such as the
data object's type, and whether that type is sequenced (preserves
ordering across properties) or open (each instance can have its model
extended). The model also holds information about the data object's
properties, any default values they may have, and so on.

### 参数

`data_object`  
The SDO\_DataObject being reflected upon.

### 返回值

None.

SDO\_Model\_ReflectionDataObject::export
========================================

Get a string describing the SDO\_DataObject

### 说明

<span class="type">mixed</span> <span
class="methodname">SDO\_Model\_ReflectionDataObject::export</span> (
<span class="methodparam"><span
class="type">SDO\_Model\_ReflectionDataObject</span> `$rdo`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$return`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get a string describing the SDO\_DataObject. The default behaviour is to
print the output, but if **`TRUE`** is specified for return, it is
returned as a string.

### 参数

`rdo`  
An SDO\_Model\_ReflectionDataObject.

`return`  
If **`TRUE`**, return the output as a string, otherwise print it.

### 返回值

Returns the output if TRUE is specified for return, otherwise NULL.

SDO\_Model\_ReflectionDataObject::getContainmentProperty
========================================================

Get the property which defines the containment relationship to the data
object

### 说明

<span class="type">SDO\_Model\_Property</span> <span
class="methodname">SDO\_Model\_ReflectionDataObject::getContainmentProperty</span>
( <span class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the SDO\_Model\_Property that contains the SDO\_DataObject. This
method is used to navigate up to the parent's property which contains
the data object which has been reflected upon.

### 参数

None.

### 返回值

Returns the container's SDO\_Model\_Property which references the
SDO\_DataObject, or **`NULL`** if it is a root SDO\_DataObject.

SDO\_Model\_ReflectionDataObject::getInstanceProperties
=======================================================

Get the instance properties of the SDO\_DataObject

### 说明

<span class="type">array</span> <span
class="methodname">SDO\_Model\_ReflectionDataObject::getInstanceProperties</span>
( <span class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the instance properties for the SDO\_DataObject. The instance
properties consist of all the properties defined on the data object's
type, plus any instance properties from open content (if the data object
is an open type).

### 参数

None.

### 返回值

An array of SDO\_Model\_Property objects.

SDO\_Model\_ReflectionDataObject::getType
=========================================

Get the SDO\_Model\_Type for the SDO\_DataObject

### 说明

<span class="type">SDO\_Model\_Type</span> <span
class="methodname">SDO\_Model\_ReflectionDataObject::getType</span> (
<span class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the SDO\_Model\_Type for the SDO\_DataObject. The
SDO\_Model\_Type holds all the information about the data object's type,
such as namespace URI, type name, whether it is a primitive data type,
and so on.

### 参数

None.

### 返回值

Returns the SDO\_Model\_Type for the SDO\_DataObject.

SDO\_Model\_Type::getBaseType
=============================

Get the base type for this type

### 说明

<span class="type">SDO\_Model\_Type</span> <span
class="methodname">SDO\_Model\_Type::getBaseType</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get the base type for this type. Returns the SDO\_Model\_Type for the
base type if this type inherits from another, otherwise returns
**`NULL`**. An example of when base types occur is when a type defined
in XML schema inherits from another type by using

``` description
<extension base="...">
```

.

### 参数

None.

### 返回值

Returns the SDO\_Model\_Type for the base type if this type inherits
from another, otherwise returns **`NULL`**.

SDO\_Model\_Type::getName
=========================

Get the name of the type

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_Model\_Type::getName</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the name of the type. The combination of type name and namespace
URI is used to uniquely identify the type.

### 参数

None.

### 返回值

Returns the name of the type.

SDO\_Model\_Type::getNamespaceURI
=================================

Get the namespace URI of the type

### 说明

<span class="type">string</span> <span
class="methodname">SDO\_Model\_Type::getNamespaceURI</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the namespace URI of the type. The combination of namespace URI
and type name is used to uniquely identify the type.

### 参数

None.

### 返回值

Returns the namespace URI of the type.

SDO\_Model\_Type::getProperties
===============================

Get the SDO\_Model\_Property objects defined for the type

### 说明

<span class="type">array</span> <span
class="methodname">SDO\_Model\_Type::getProperties</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get an array of SDO\_Model\_Property objects describing the properties
defined for the SDO\_Model\_Type. Each SDO\_Model\_Property holds
information such as the property name, default value, and so on.

### 参数

None.

### 返回值

Returns an array of SDO\_Model\_Property objects.

SDO\_Model\_Type::getProperty
=============================

Get an SDO\_Model\_Property of the type

### 说明

<span class="type">SDO\_Model\_Property</span> <span
class="methodname">SDO\_Model\_Type::getProperty</span> ( <span
class="methodparam"><span class="type">mixed</span> `$identifier`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Get an SDO\_Model\_Property of the type, identified by its property
index or property name.

### 参数

`identifier`  
The property index or property name.

### 返回值

Returns the SDO\_Model\_Property.

SDO\_Model\_Type::isAbstractType
================================

Test to see if this SDO\_Model\_Type is an abstract data type

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Type::isAbstractType</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see if this SDO\_Model\_Type is an abstract data type. Returns
**`TRUE`** if this type is abstract, that is, no SDO\_DataObject of this
type can be instantiated, though other types may inherit from it.

### 参数

None.

### 返回值

Returns **`TRUE`** if this type is an abstract data type, otherwise
returns **`FALSE`**.

SDO\_Model\_Type::isDataType
============================

Test to see if this SDO\_Model\_Type is a primitive data type

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Type::isDataType</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see if this SDO\_Model\_Type is a primitive data type. Returns
**`TRUE`** if this type is a primitive data type, otherwise returns
**`FALSE`**.

### 参数

None.

### 返回值

Returns **`TRUE`** if this type is a primitive data type, otherwise
returns **`FALSE`**.

SDO\_Model\_Type::isInstance
============================

Test for an SDO\_DataObject being an instance of this SDO\_Model\_Type

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Type::isInstance</span> ( <span
class="methodparam"><span class="type">SDO\_DataObject</span>
`$data_object`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test for an SDO\_DataObject being an instance of this SDO\_Model\_Type.
Returns **`TRUE`** if the SDO\_DataObject provided is an instance of
this SDO\_Model\_Type, or a derived type, otherwise returns **`FALSE`**.

### 参数

`data_object`  
The SDO\_DataObject to be tested.

### 返回值

Returns **`TRUE`** if the SDO\_DataObject provided is an instance of
this SDO\_Model\_Type, or a derived type, otherwise returns **`FALSE`**.

SDO\_Model\_Type::isOpenType
============================

Test to see if this type is an open type

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Type::isOpenType</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see if this type is open. Returns **`TRUE`** if this type is
open, otherwise returns **`FALSE`**. An SDO\_DataObject whose type is
open can have properties added to them which are not described by the
type. This capability is used to support working with XML documents
whose schema support open content, such as that defined by an

``` description
<xsd:any>
```

element.

### 参数

None.

### 返回值

Returns **`TRUE`** if this type is open, otherwise returns **`FALSE`**.

SDO\_Model\_Type::isSequencedType
=================================

Test to see if this is a sequenced type

### 说明

<span class="type">bool</span> <span
class="methodname">SDO\_Model\_Type::isSequencedType</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Test to see if this is a sequenced type. Returns **`TRUE`** if this type
is sequence, otherwise returns **`FALSE`**. Sequenced types can have the
ordering across properties preserved and can contain unstructured text.
For more information on sequenced types see the section on
<a href="/sdo/examples.html#Working%20with%20Sequenced%20Data%20Objects" class="link">Working with Sequenced Data Objects</a>.

### 参数

None.

### 返回值

Returns **`TRUE`** if this type is sequence, otherwise return
**`FALSE`**.

SDO\_Sequence::getProperty
==========================

Return the property for the specified sequence index

### 说明

<span class="type">SDO\_Model\_Property</span> <span
class="methodname">SDO\_Sequence::getProperty</span> ( <span
class="methodparam"><span class="type">int</span>
`$sequence_index`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Return the property for the specified sequence index.

### 参数

`sequence_index`  
The position of the element in the sequence.

### 返回值

An SDO\_Model\_Property. A return value of NULL means the sequence
element does not belong to a property and must therefore be unstructured
text.

### 错误／异常

`SDO_IndexOutOfBoundsException`  
Thrown if the sequence index is less than zero or greater than the size
of the sequence.

SDO\_Sequence::insert
=====================

Insert into a sequence

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_Sequence::insert</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$sequenceIndex`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$propertyIdentifier`</span> \]\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Insert a new element at a specified position in the sequence. All
subsequent sequence items are moved up.

### 参数

`value`  
The new value to be inserted. This can be either a primitive or an
SDO\_DataObject.

`sequenceIndex`  
The position at which to insert the new element. Default is NULL, which
results in the new value being appended to the sequence.

`propertyIdentifier`  
Either a property index, a property name, or an
<a href="/ref/sdo.html#SDO_Model_Property" class="link">SDO_Model_Property</a>,
used to identify a property in the sequence's corresponding
SDO\_DataObject. A value of NULL signifies unstructured text.

### 返回值

None.

### 错误／异常

`SDO_IndexOutOfBoundsException`  
Thrown if the sequence index is less than zero or greater than the size
of the sequence.

`SDO_InvalidConversionException`  
Thrown if the type of the new value cannot be juggled to match the type
for the specified data object property.

SDO\_Sequence::move
===================

Move an item to another sequence position

### 说明

<span class="type">void</span> <span
class="methodname">SDO\_Sequence::move</span> ( <span
class="methodparam"> <span class="type">int</span> `$toIndex`</span>,
<span class="methodparam"> <span class="type">int</span>
`$fromIndex`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Modify the position of the item in the sequence, without altering the
value of the property in the SDO\_DataObject.

### 参数

`toIndex`  
The destination sequence index. If this index is less than zero or
greater than the size of the sequence then the value is appended.

`fromIndex`  
The source sequence index.

### 返回值

None.

### 错误／异常

`SDO_IndexOutOfBoundsException`  
Thrown if the fromIndex sequence index is less than zero or greater than
the size of the sequence.

**目录**

-   [SDO\_DAS\_ChangeSummary::beginLogging](/ref/sdo.html#SDO_DAS_ChangeSummary::beginLogging)
    — Begin change logging
-   [SDO\_DAS\_ChangeSummary::endLogging](/ref/sdo.html#SDO_DAS_ChangeSummary::endLogging)
    — End change logging
-   [SDO\_DAS\_ChangeSummary::getChangeType](/ref/sdo.html#SDO_DAS_ChangeSummary::getChangeType)
    — Get the type of change made to an SDO\_DataObject
-   [SDO\_DAS\_ChangeSummary::getChangedDataObjects](/ref/sdo.html#SDO_DAS_ChangeSummary::getChangedDataObjects)
    — Get the changed data objects from a change summary
-   [SDO\_DAS\_ChangeSummary::getOldContainer](/ref/sdo.html#SDO_DAS_ChangeSummary::getOldContainer)
    — Get the old container for a deleted SDO\_DataObject
-   [SDO\_DAS\_ChangeSummary::getOldValues](/ref/sdo.html#SDO_DAS_ChangeSummary::getOldValues)
    — Get the old values for a given changed SDO\_DataObject
-   [SDO\_DAS\_ChangeSummary::isLogging](/ref/sdo.html#SDO_DAS_ChangeSummary::isLogging)
    — Test to see whether change logging is switched on
-   [SDO\_DAS\_DataFactory::addPropertyToType](/ref/sdo.html#SDO_DAS_DataFactory::addPropertyToType)
    — Adds a property to a type
-   [SDO\_DAS\_DataFactory::addType](/ref/sdo.html#SDO_DAS_DataFactory::addType)
    — Add a new type to a model
-   [SDO\_DAS\_DataFactory::getDataFactory](/ref/sdo.html#SDO_DAS_DataFactory::getDataFactory)
    — Get a data factory instance
-   [SDO\_DAS\_DataObject::getChangeSummary](/ref/sdo.html#SDO_DAS_DataObject::getChangeSummary)
    — Get a data object's change summary
-   [SDO\_DAS\_Setting::getListIndex](/ref/sdo.html#SDO_DAS_Setting::getListIndex)
    — Get the list index for a changed many-valued property
-   [SDO\_DAS\_Setting::getPropertyIndex](/ref/sdo.html#SDO_DAS_Setting::getPropertyIndex)
    — Get the property index for a changed property
-   [SDO\_DAS\_Setting::getPropertyName](/ref/sdo.html#SDO_DAS_Setting::getPropertyName)
    — Get the property name for a changed property
-   [SDO\_DAS\_Setting::getValue](/ref/sdo.html#SDO_DAS_Setting::getValue)
    — Get the old value for the changed property
-   [SDO\_DAS\_Setting::isSet](/ref/sdo.html#SDO_DAS_Setting::isSet) —
    Test whether a property was set prior to being modified
-   [SDO\_DataFactory::create](/ref/sdo.html#SDO_DataFactory::create) —
    Create an SDO\_DataObject
-   [SDO\_DataObject::clear](/ref/sdo.html#SDO_DataObject::clear) —
    Clear an SDO\_DataObject's properties
-   [SDO\_DataObject::createDataObject](/ref/sdo.html#SDO_DataObject::createDataObject)
    — Create a child SDO\_DataObject
-   [SDO\_DataObject::getContainer](/ref/sdo.html#SDO_DataObject::getContainer)
    — Get a data object's container
-   [SDO\_DataObject::getSequence](/ref/sdo.html#SDO_DataObject::getSequence)
    — Get the sequence for a data object
-   [SDO\_DataObject::getTypeName](/ref/sdo.html#SDO_DataObject::getTypeName)
    — Return the name of the type for a data object
-   [SDO\_DataObject::getTypeNamespaceURI](/ref/sdo.html#SDO_DataObject::getTypeNamespaceURI)
    — Return the namespace URI of the type for a data object
-   [SDO\_Exception::getCause](/ref/sdo.html#SDO_Exception::getCause) —
    Get the cause of the exception
-   [SDO\_List::insert](/ref/sdo.html#SDO_List::insert) — Insert into a
    list
-   [SDO\_Model\_Property::getContainingType](/ref/sdo.html#SDO_Model_Property::getContainingType)
    — Get the SDO\_Model\_Type which contains this property
-   [SDO\_Model\_Property::getDefault](/ref/sdo.html#SDO_Model_Property::getDefault)
    — Get the default value for the property
-   [SDO\_Model\_Property::getName](/ref/sdo.html#SDO_Model_Property::getName)
    — Get the name of the SDO\_Model\_Property
-   [SDO\_Model\_Property::getType](/ref/sdo.html#SDO_Model_Property::getType)
    — Get the SDO\_Model\_Type of the property
-   [SDO\_Model\_Property::isContainment](/ref/sdo.html#SDO_Model_Property::isContainment)
    — Test to see if the property defines a containment relationship
-   [SDO\_Model\_Property::isMany](/ref/sdo.html#SDO_Model_Property::isMany)
    — Test to see if the property is many-valued
-   [SDO\_Model\_ReflectionDataObject::\_\_construct](/ref/sdo.html#SDO_Model_ReflectionDataObject::__construct)
    — Construct an SDO\_Model\_ReflectionDataObject
-   [SDO\_Model\_ReflectionDataObject::export](/ref/sdo.html#SDO_Model_ReflectionDataObject::export)
    — Get a string describing the SDO\_DataObject
-   [SDO\_Model\_ReflectionDataObject::getContainmentProperty](/ref/sdo.html#SDO_Model_ReflectionDataObject::getContainmentProperty)
    — Get the property which defines the containment relationship to the
    data object
-   [SDO\_Model\_ReflectionDataObject::getInstanceProperties](/ref/sdo.html#SDO_Model_ReflectionDataObject::getInstanceProperties)
    — Get the instance properties of the SDO\_DataObject
-   [SDO\_Model\_ReflectionDataObject::getType](/ref/sdo.html#SDO_Model_ReflectionDataObject::getType)
    — Get the SDO\_Model\_Type for the SDO\_DataObject
-   [SDO\_Model\_Type::getBaseType](/ref/sdo.html#SDO_Model_Type::getBaseType)
    — Get the base type for this type
-   [SDO\_Model\_Type::getName](/ref/sdo.html#SDO_Model_Type::getName) —
    Get the name of the type
-   [SDO\_Model\_Type::getNamespaceURI](/ref/sdo.html#SDO_Model_Type::getNamespaceURI)
    — Get the namespace URI of the type
-   [SDO\_Model\_Type::getProperties](/ref/sdo.html#SDO_Model_Type::getProperties)
    — Get the SDO\_Model\_Property objects defined for the type
-   [SDO\_Model\_Type::getProperty](/ref/sdo.html#SDO_Model_Type::getProperty)
    — Get an SDO\_Model\_Property of the type
-   [SDO\_Model\_Type::isAbstractType](/ref/sdo.html#SDO_Model_Type::isAbstractType)
    — Test to see if this SDO\_Model\_Type is an abstract data type
-   [SDO\_Model\_Type::isDataType](/ref/sdo.html#SDO_Model_Type::isDataType)
    — Test to see if this SDO\_Model\_Type is a primitive data type
-   [SDO\_Model\_Type::isInstance](/ref/sdo.html#SDO_Model_Type::isInstance)
    — Test for an SDO\_DataObject being an instance of this
    SDO\_Model\_Type
-   [SDO\_Model\_Type::isOpenType](/ref/sdo.html#SDO_Model_Type::isOpenType)
    — Test to see if this type is an open type
-   [SDO\_Model\_Type::isSequencedType](/ref/sdo.html#SDO_Model_Type::isSequencedType)
    — Test to see if this is a sequenced type
-   [SDO\_Sequence::getProperty](/ref/sdo.html#SDO_Sequence::getProperty)
    — Return the property for the specified sequence index
-   [SDO\_Sequence::insert](/ref/sdo.html#SDO_Sequence::insert) — Insert
    into a sequence
-   [SDO\_Sequence::move](/ref/sdo.html#SDO_Sequence::move) — Move an
    item to another sequence position
