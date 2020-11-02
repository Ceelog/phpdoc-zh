预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

| Constant                                                        | Value | Description                                                       |
|-----------------------------------------------------------------|-------|-------------------------------------------------------------------|
| **`XML_ELEMENT_NODE`** (<span class="type">int</span>)          | 1     | Node is a <span class="classname">DOMElement</span>               |
| **`XML_ATTRIBUTE_NODE`** (<span class="type">int</span>)        | 2     | Node is a <span class="classname">DOMAttr</span>                  |
| **`XML_TEXT_NODE`** (<span class="type">int</span>)             | 3     | Node is a <span class="classname">DOMText</span>                  |
| **`XML_CDATA_SECTION_NODE`** (<span class="type">int</span>)    | 4     | Node is a <span class="classname">DOMCharacterData</span>         |
| **`XML_ENTITY_REF_NODE`** (<span class="type">int</span>)       | 5     | Node is a <span class="classname">DOMEntityReference</span>       |
| **`XML_ENTITY_NODE`** (<span class="type">int</span>)           | 6     | Node is a <span class="classname">DOMEntity</span>                |
| **`XML_PI_NODE`** (<span class="type">int</span>)               | 7     | Node is a <span class="classname">DOMProcessingInstruction</span> |
| **`XML_COMMENT_NODE`** (<span class="type">int</span>)          | 8     | Node is a <span class="classname">DOMComment</span>               |
| **`XML_DOCUMENT_NODE`** (<span class="type">int</span>)         | 9     | Node is a <span class="classname">DOMDocument</span>              |
| **`XML_DOCUMENT_TYPE_NODE`** (<span class="type">int</span>)    | 10    | Node is a <span class="classname">DOMDocumentType</span>          |
| **`XML_DOCUMENT_FRAG_NODE`** (<span class="type">int</span>)    | 11    | Node is a <span class="classname">DOMDocumentFragment</span>      |
| **`XML_NOTATION_NODE`** (<span class="type">int</span>)         | 12    | Node is a <span class="classname">DOMNotation</span>              |
| **`XML_HTML_DOCUMENT_NODE`** (<span class="type">int</span>)    | 13    |                                                                   |
| **`XML_DTD_NODE`** (<span class="type">int</span>)              | 14    |                                                                   |
| **`XML_ELEMENT_DECL_NODE`** (<span class="type">int</span>)     | 15    |                                                                   |
| **`XML_ATTRIBUTE_DECL_NODE`** (<span class="type">int</span>)   | 16    |                                                                   |
| **`XML_ENTITY_DECL_NODE`** (<span class="type">int</span>)      | 17    |                                                                   |
| **`XML_NAMESPACE_DECL_NODE`** (<span class="type">int</span>)   | 18    |                                                                   |
| **`XML_ATTRIBUTE_CDATA`** (<span class="type">int</span>)       | 1     |                                                                   |
| **`XML_ATTRIBUTE_ID`** (<span class="type">int</span>)          | 2     |                                                                   |
| **`XML_ATTRIBUTE_IDREF`** (<span class="type">int</span>)       | 3     |                                                                   |
| **`XML_ATTRIBUTE_IDREFS`** (<span class="type">int</span>)      | 4     |                                                                   |
| **`XML_ATTRIBUTE_ENTITY`** (<span class="type">int</span>)      | 5     |                                                                   |
| **`XML_ATTRIBUTE_NMTOKEN`** (<span class="type">int</span>)     | 7     |                                                                   |
| **`XML_ATTRIBUTE_NMTOKENS`** (<span class="type">int</span>)    | 8     |                                                                   |
| **`XML_ATTRIBUTE_ENUMERATION`** (<span class="type">int</span>) | 9     |                                                                   |
| **`XML_ATTRIBUTE_NOTATION`** (<span class="type">int</span>)    | 10    |                                                                   |

| Constant                                                              | Value | Description                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`DOM_PHP_ERR`** (<span class="type">int</span>)                     | 0     | Error code not part of the DOM specification. Meant for PHP errors.                                                                                                                           |
| **`DOM_INDEX_SIZE_ERR`** (<span class="type">int</span>)              | 1     | If index or size is negative, or greater than the allowed value.                                                                                                                              |
| **`DOMSTRING_SIZE_ERR`** (<span class="type">int</span>)              | 2     | If the specified range of text does not fit into a <span class="classname">DOMString</span>.                                                                                                  |
| **`DOM_HIERARCHY_REQUEST_ERR`** (<span class="type">int</span>)       | 3     | If any node is inserted somewhere it doesn't belong                                                                                                                                           |
| **`DOM_WRONG_DOCUMENT_ERR`** (<span class="type">int</span>)          | 4     | If a node is used in a different document than the one that created it.                                                                                                                       |
| **`DOM_INVALID_CHARACTER_ERR`** (<span class="type">int</span>)       | 5     | If an invalid or illegal character is specified, such as in a name.                                                                                                                           |
| **`DOM_NO_DATA_ALLOWED_ERR`** (<span class="type">int</span>)         | 6     | If data is specified for a node which does not support data.                                                                                                                                  |
| **`DOM_NO_MODIFICATION_ALLOWED_ERR`** (<span class="type">int</span>) | 7     | If an attempt is made to modify an object where modifications are not allowed.                                                                                                                |
| **`DOM_NOT_FOUND_ERR`** (<span class="type">int</span>)               | 8     | If an attempt is made to reference a node in a context where it does not exist.                                                                                                               |
| **`DOM_NOT_SUPPORTED_ERR`** (<span class="type">int</span>)           | 9     | If the implementation does not support the requested type of object or operation.                                                                                                             |
| **`DOM_INUSE_ATTRIBUTE_ERR`** (<span class="type">int</span>)         | 10    | If an attempt is made to add an attribute that is already in use elsewhere.                                                                                                                   |
| **`DOM_INVALID_STATE_ERR`** (<span class="type">int</span>)           | 11    | If an attempt is made to use an object that is not, or is no longer, usable.                                                                                                                  |
| **`DOM_SYNTAX_ERR`** (<span class="type">int</span>)                  | 12    | If an invalid or illegal string is specified.                                                                                                                                                 |
| **`DOM_INVALID_MODIFICATION_ERR`** (<span class="type">int</span>)    | 13    | If an attempt is made to modify the type of the underlying object.                                                                                                                            |
| **`DOM_NAMESPACE_ERR`** (<span class="type">int</span>)               | 14    | If an attempt is made to create or change an object in a way which is incorrect with regard to namespaces.                                                                                    |
| **`DOM_INVALID_ACCESS_ERR`** (<span class="type">int</span>)          | 15    | If a parameter or an operation is not supported by the underlying object.                                                                                                                     |
| **`DOM_VALIDATION_ERR`** (<span class="type">int</span>)              | 16    | If a call to a method such as insertBefore or removeChild would make the Node invalid with respect to "partial validity", this exception would be raised and the operation would not be done. |
