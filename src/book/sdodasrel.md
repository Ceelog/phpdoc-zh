SDO Relational Data Access Service
==================================

**目录**

-   [简介](/intro/sdodasrel.html)
-   [安装／配置](/sdodasrel/setup.html)
    -   [需求](/sdodasrel/setup.html#需求)
    -   [安装](/sdodasrel/setup.html#安装)
    -   [运行时配置](/sdodasrel/setup.html#运行时配置)
    -   [资源类型](/sdodasrel/setup.html#资源类型)
-   [预定义常量](/sdodasrel/constants.html)
-   [范例](/sdodasrel/examples.html)
    -   [Creating, retrieving, updating and deleting
        data](/sdodasrel/examples.html#Creating,%20retrieving,%20updating%20and%20deleting%20data)
    -   [Specifying the
        metadata](/sdodasrel/examples.html#Specifying%20the%20metadata)
    -   [One-table
        examples](/sdodasrel/examples.html#One-table%20examples)
    -   [Two-table
        examples](/sdodasrel/examples.html#Two-table%20examples)
    -   [Three-table
        example](/sdodasrel/examples.html#Three-table%20example)
-   [Limitations](/sdodasrel/limitations.html)
-   [SDO-DAS-Relational 函数](/ref/sdodasrel.html)
    -   [SDO\_DAS\_Relational::applyChanges](/ref/sdodasrel.html#SDO_DAS_Relational::applyChanges)
        — Applies the changes made to a data graph back to the database
    -   [SDO\_DAS\_Relational::\_\_construct](/ref/sdodasrel.html#SDO_DAS_Relational::__construct)
        — Creates an instance of a Relational Data Access Service
    -   [SDO\_DAS\_Relational::createRootDataObject](/ref/sdodasrel.html#SDO_DAS_Relational::createRootDataObject)
        — Returns the special root object in an otherwise empty data
        graph. Used when creating a data graph from scratch
    -   [SDO\_DAS\_Relational::executePreparedQuery](/ref/sdodasrel.html#SDO_DAS_Relational::executePreparedQuery)
        — Executes an SQL query passed as a prepared statement, with a
        list of values to substitute for placeholders, and return the
        results as a normalised data graph
    -   [SDO\_DAS\_Relational::executeQuery](/ref/sdodasrel.html#SDO_DAS_Relational::executeQuery)
        — Executes a given SQL query against a relational database and
        returns the results as a normalised data graph
