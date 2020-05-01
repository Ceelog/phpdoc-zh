Hyperwave API
=============

**目录**

-   [简介](/intro/hwapi.html)
-   [安装／配置](/hwapi/setup.html)
    -   [需求](/hwapi/setup.html#需求)
    -   [安装](/hwapi/setup.html#安装)
    -   [运行时配置](/hwapi/setup.html#运行时配置)
    -   [资源类型](/hwapi/setup.html#资源类型)
-   [预定义常量](/hwapi/constants.html)
-   [Integration with Apache](/hwapi/apache-integration.html)
-   [Hyperwave API 函数](/ref/hwapi.html)
    -   [hw\_api::checkin](/ref/hwapi.html#hw_api::checkin) — Checks in
        an object
    -   [hw\_api::checkout](/ref/hwapi.html#hw_api::checkout) — Checks
        out an object
    -   [hw\_api::children](/ref/hwapi.html#hw_api::children) — Returns
        children of an object
    -   [hw\_api::content](/ref/hwapi.html#hw_api::content) — Returns
        content of an object
    -   [hw\_api::copy](/ref/hwapi.html#hw_api::copy) — Copies
        physically
    -   [hw\_api::dbstat](/ref/hwapi.html#hw_api::dbstat) — Returns
        statistics about database server
    -   [hw\_api::dcstat](/ref/hwapi.html#hw_api::dcstat) — Returns
        statistics about document cache server
    -   [hw\_api::dstanchors](/ref/hwapi.html#hw_api::dstanchors) —
        Returns a list of all destination anchors
    -   [hw\_api::dstofsrcanchor](/ref/hwapi.html#hw_api::dstofsrcanchor)
        — Returns destination of a source anchor
    -   [hw\_api::find](/ref/hwapi.html#hw_api::find) — Search for
        objects
    -   [hw\_api::ftstat](/ref/hwapi.html#hw_api::ftstat) — Returns
        statistics about fulltext server
    -   [hw\_api::hwstat](/ref/hwapi.html#hw_api::hwstat) — Returns
        statistics about Hyperwave server
    -   [hw\_api::identify](/ref/hwapi.html#hw_api::identify) — Log into
        Hyperwave Server
    -   [hw\_api::info](/ref/hwapi.html#hw_api::info) — Returns
        information about server configuration
    -   [hw\_api::insert](/ref/hwapi.html#hw_api::insert) — Inserts a
        new object
    -   [hw\_api::insertanchor](/ref/hwapi.html#hw_api::insertanchor) —
        Inserts a new object of type anchor
    -   [hw\_api::insertcollection](/ref/hwapi.html#hw_api::insertcollection)
        — Inserts a new object of type collection
    -   [hw\_api::insertdocument](/ref/hwapi.html#hw_api::insertdocument)
        — Inserts a new object of type document
    -   [hw\_api::link](/ref/hwapi.html#hw_api::link) — Creates a link
        to an object
    -   [hw\_api::lock](/ref/hwapi.html#hw_api::lock) — Locks an object
    -   [hw\_api::move](/ref/hwapi.html#hw_api::move) — Moves object
        between collections
    -   [hw\_api::object](/ref/hwapi.html#hw_api::object) — Retrieve
        attribute information
    -   [hw\_api::objectbyanchor](/ref/hwapi.html#hw_api::objectbyanchor)
        — Returns the object an anchor belongs to
    -   [hw\_api::parents](/ref/hwapi.html#hw_api::parents) — Returns
        parents of an object
    -   [hw\_api::remove](/ref/hwapi.html#hw_api::remove) — Delete an
        object
    -   [hw\_api::replace](/ref/hwapi.html#hw_api::replace) — Replaces
        an object
    -   [hw\_api::setcommittedversion](/ref/hwapi.html#hw_api::setcommittedversion)
        — Commits version other than last version
    -   [hw\_api::srcanchors](/ref/hwapi.html#hw_api::srcanchors) —
        Returns a list of all source anchors
    -   [hw\_api::srcsofdst](/ref/hwapi.html#hw_api::srcsofdst) —
        Returns source of a destination object
    -   [hw\_api::unlock](/ref/hwapi.html#hw_api::unlock) — Unlocks a
        locked object
    -   [hw\_api::user](/ref/hwapi.html#hw_api::user) — Returns the own
        user object
    -   [hw\_api::userlist](/ref/hwapi.html#hw_api::userlist) — Returns
        a list of all logged in users
    -   [hw\_api\_attribute::key](/ref/hwapi.html#hw_api_attribute::key)
        — Returns key of the attribute
    -   [hw\_api\_attribute::langdepvalue](/ref/hwapi.html#hw_api_attribute::langdepvalue)
        — Returns value for a given language
    -   [hw\_api\_attribute::value](/ref/hwapi.html#hw_api_attribute::value)
        — Returns value of the attribute
    -   [hw\_api\_attribute::values](/ref/hwapi.html#hw_api_attribute::values)
        — Returns all values of the attribute
    -   [hw\_api\_content::mimetype](/ref/hwapi.html#hw_api_content::mimetype)
        — Returns mimetype
    -   [hw\_api\_content::read](/ref/hwapi.html#hw_api_content::read) —
        Read content
    -   [hw\_api\_error::count](/ref/hwapi.html#hw_api_error::count) —
        Returns number of reasons
    -   [hw\_api\_error::reason](/ref/hwapi.html#hw_api_error::reason) —
        Returns reason of error
    -   [hw\_api\_object::assign](/ref/hwapi.html#hw_api_object::assign)
        — Clones object
    -   [hw\_api\_object::attreditable](/ref/hwapi.html#hw_api_object::attreditable)
        — Checks whether an attribute is editable
    -   [hw\_api\_object::count](/ref/hwapi.html#hw_api_object::count) —
        Returns number of attributes
    -   [hw\_api\_object::insert](/ref/hwapi.html#hw_api_object::insert)
        — Inserts new attribute
    -   [hw\_api\_object::remove](/ref/hwapi.html#hw_api_object::remove)
        — Removes attribute
    -   [hw\_api\_object::title](/ref/hwapi.html#hw_api_object::title) —
        Returns the title attribute
    -   [hw\_api\_object::value](/ref/hwapi.html#hw_api_object::value) —
        Returns value of attribute
    -   [hw\_api\_reason::description](/ref/hwapi.html#hw_api_reason::description)
        — Returns description of reason
    -   [hw\_api\_reason::type](/ref/hwapi.html#hw_api_reason::type) —
        Returns type of reason
    -   [hwapi\_attribute\_new](/ref/hwapi.html#hwapi_attribute_new) —
        Creates instance of class hw\_api\_attribute
    -   [hwapi\_content\_new](/ref/hwapi.html#hwapi_content_new) —
        Create new instance of class hw\_api\_content
    -   [hwapi\_hgcsp](/ref/hwapi.html#hwapi_hgcsp) — Returns object of
        class hw\_api
    -   [hwapi\_object\_new](/ref/hwapi.html#hwapi_object_new) — Creates
        a new instance of class hwapi\_object\_new
