Service Data Objects
====================

**目录**

-   [简介](/intro/sdo.html)
-   [安装／配置](/sdo/setup.html)
    -   [需求](/sdo/setup.html#需求)
    -   [安装](/sdo/setup.html#安装)
    -   [运行时配置](/sdo/setup.html#运行时配置)
    -   [资源类型](/sdo/setup.html#资源类型)
-   [预定义常量](/sdo/constants.html)
-   [Limitations](/sdo/limitations.html)
-   [范例](/sdo/examples.html)
    -   [Basic usage](/sdo/examples.html#Basic%20usage)
    -   [Setting and Getting Property
        Values](/sdo/examples.html#Setting%20and%20Getting%20Property%20Values)
    -   [Working with Sequenced Data
        Objects](/sdo/examples.html#Working%20with%20Sequenced%20Data%20Objects)
    -   [Reflecting on Service Data
        Objects](/sdo/examples.html#Reflecting%20on%20Service%20Data%20Objects)
-   [SDO 函数](/ref/sdo.html)
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
    -   [SDO\_DAS\_Setting::isSet](/ref/sdo.html#SDO_DAS_Setting::isSet)
        — Test whether a property was set prior to being modified
    -   [SDO\_DataFactory::create](/ref/sdo.html#SDO_DataFactory::create)
        — Create an SDO\_DataObject
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
    -   [SDO\_Exception::getCause](/ref/sdo.html#SDO_Exception::getCause)
        — Get the cause of the exception
    -   [SDO\_List::insert](/ref/sdo.html#SDO_List::insert) — Insert
        into a list
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
        — Get the property which defines the containment relationship to
        the data object
    -   [SDO\_Model\_ReflectionDataObject::getInstanceProperties](/ref/sdo.html#SDO_Model_ReflectionDataObject::getInstanceProperties)
        — Get the instance properties of the SDO\_DataObject
    -   [SDO\_Model\_ReflectionDataObject::getType](/ref/sdo.html#SDO_Model_ReflectionDataObject::getType)
        — Get the SDO\_Model\_Type for the SDO\_DataObject
    -   [SDO\_Model\_Type::getBaseType](/ref/sdo.html#SDO_Model_Type::getBaseType)
        — Get the base type for this type
    -   [SDO\_Model\_Type::getName](/ref/sdo.html#SDO_Model_Type::getName)
        — Get the name of the type
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
    -   [SDO\_Sequence::insert](/ref/sdo.html#SDO_Sequence::insert) —
        Insert into a sequence
    -   [SDO\_Sequence::move](/ref/sdo.html#SDO_Sequence::move) — Move
        an item to another sequence position
