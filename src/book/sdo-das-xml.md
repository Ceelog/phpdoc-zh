SDO XML Data Access Service
===========================

**目录**

-   [简介](/intro/sdo-das-xml.html)
-   [安装／配置](/sdo-das-xml/setup.html)
    -   [需求](/sdo-das-xml/setup.html#需求)
    -   [安装](/sdo-das-xml/setup.html#安装)
    -   [运行时配置](/sdo-das-xml/setup.html#运行时配置)
    -   [资源类型](/sdo-das-xml/setup.html#资源类型)
-   [预定义常量](/sdo-das-xml/constants.html)
-   [范例](/sdo-das-xml/examples.html)
-   [SDO DAS XML 函数](/ref/sdo-das-xml.html)
    -   [SDO\_DAS\_XML::addTypes](/ref/sdo-das-xml.html#SDO_DAS_XML::addTypes)
        — To load a second or subsequent schema file to a SDO\_DAS\_XML
        object
    -   [SDO\_DAS\_XML::create](/ref/sdo-das-xml.html#SDO_DAS_XML::create)
        — To create SDO\_DAS\_XML object for a given schema file
    -   [SDO\_DAS\_XML::createDataObject](/ref/sdo-das-xml.html#SDO_DAS_XML::createDataObject)
        — Creates SDO\_DataObject for a given namespace URI and type
        name
    -   [SDO\_DAS\_XML::createDocument](/ref/sdo-das-xml.html#SDO_DAS_XML::createDocument)
        — Creates an XML Document object from scratch, without the need
        to load a document from a file or string
    -   [SDO\_DAS\_XML::loadFile](/ref/sdo-das-xml.html#SDO_DAS_XML::loadFile)
        — Returns SDO\_DAS\_XML\_Document object for a given path to xml
        instance document
    -   [SDO\_DAS\_XML::loadString](/ref/sdo-das-xml.html#SDO_DAS_XML::loadString)
        — Returns SDO\_DAS\_XML\_Document for a given xml instance
        string
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
