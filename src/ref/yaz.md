yaz\_addinfo
============

Returns additional error information

### 说明

<span class="type">string</span> <span
class="methodname">yaz\_addinfo</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> )

Returns additional error information for the last request on the server.

With some servers, this function may return the same string as <span
class="function">yaz\_error</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

### 返回值

A string containing additional error information or an empty string if
the last operation was successful or if no additional information was
provided by the server.

### 参见

-   <span class="function">yaz\_error</span>
-   <span class="function">yaz\_errno</span>

yaz\_ccl\_conf
==============

Configure CCL parser

### 说明

<span class="type">void</span> <span
class="methodname">yaz\_ccl\_conf</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">array</span>
`$config`</span> )

This function configures the CCL query parser for a server with
definitions of access points (CCL qualifiers) and their mapping to RPN.

To map a specific CCL query to RPN afterwards call the <span
class="function">yaz\_ccl\_parse</span> function.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`config`  
An array of configuration. Each key of the array is the name of a CCL
field and the corresponding value holds a string that specifies a
mapping to RPN.

The mapping is a sequence of attribute-type, attribute-value pairs.
Attribute-type and attribute-value is separated by an equal sign (*=*).
Each pair is separated by white space.

Additional information can be found on the
<a href="http://www.indexdata.dk/yaz/doc/tools.tkl#CCL" class="link external">» CCL</a>
page.

### 返回值

没有返回值。

### 范例

In the example below, the CCL parser is configured to support three CCL
fields: *ti*, *au* and *isbn*. Each field is mapped to their BIB-1
equivalent. It is assumed that variable *$id* is the connection ID.

**示例 \#1 CCL configuration**

``` php
<?php
$fields = array(
  "ti" => "1=4",
  "au"   => "1=1",
  "isbn" => "1=7"
);
yaz_ccl_conf($id, $fields);
?>
```

### 参见

-   <span class="function">yaz\_ccl\_parse</span>

yaz\_ccl\_parse
===============

Invoke CCL Parser

### 说明

<span class="type">bool</span> <span
class="methodname">yaz\_ccl\_parse</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> , <span class="methodparam"><span
class="type">array</span> `&$result`</span> )

This function invokes a CCL parser. It converts a given CCL FIND query
to an RPN query which may be passed to the <span
class="function">yaz\_search</span> function to perform a search.

To define a set of valid CCL fields call <span
class="function">yaz\_ccl\_conf</span> prior to this function.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`query`  
The CCL FIND query.

`result`  
If the function was executed successfully, this will be an array
containing the valid RPN query under the key *rpn*.

Upon failure, three indexes are set in this array to indicate the cause
of failure:

-   *errorcode* - the CCL error code (integer)

-   *errorstring* - the CCL error string

-   *errorpos* - approximate position in query of failure (integer is
    character position)

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 CCL Parsing**

We will try to search using CCL. In the example below, *$ccl* is a CCL
query.

``` php
<?php

yaz_ccl_conf($id, $fields);  // see example for yaz_ccl_conf
if (!yaz_ccl_parse($id, $ccl, &$cclresult)) {
    echo 'Error: ' . $cclresult["errorstring"];
} else {
    $rpn = $cclresult["rpn"];
    yaz_search($id, "rpn", $rpn);
}
?>
```

yaz\_close
==========

Close YAZ connection

### 说明

<span class="type">bool</span> <span
class="methodname">yaz\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> )

Closes the connection given by parameter `id`.

> **Note**:
>
> This function will only close a non-persistent connection opened by
> setting the *persistent* option to **`false`** with <span
> class="function">yaz\_connect</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">yaz\_connect</span>

yaz\_connect
============

Prepares for a connection to a Z39.50 server

### 说明

<span class="type">mixed</span> <span
class="methodname">yaz\_connect</span> ( <span class="methodparam"><span
class="type">string</span> `$zurl`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$options`</span> \]
)

This function returns a connection resource on success, zero on failure.

<span class="function">yaz\_connect</span> prepares for a connection to
a Z39.50 server. This function is non-blocking and does not attempt to
establish a connection - it merely prepares a connect to be performed
later when <span class="function">yaz\_wait</span> is called.

> **Note**:
>
> The
> <a href="http://www.indexdata.dk/yazproxy/" class="link external">» YAZ proxy</a>
> is a freely available Z39.50 proxy.

### 参数

`zurl`  
A string that takes the form *host\[:port\]\[/database\]*. If port is
omitted, port 210 is used. If database is omitted *Default* is used.

`options`  
If given as a string, it is treated as the Z39.50 V2 authentication
string (OpenAuth).

If given as an array, the contents of the array serves as options.

user  
Username for authentication.

group  
Group for authentication.

password  
Password for authentication.

cookie  
Cookie for session (YAZ proxy).

proxy  
Proxy for connection (YAZ proxy).

persistent  
A boolean. If **`true`** the connection is persistent; If **`false`**
the connection is not persistent. By default connections are persistent.

> **Note**:
>
> If you open a persistent connection, you won't be able to close it
> later with <span class="function">yaz\_close</span>.

piggyback  
A boolean. If **`true`** piggyback is enabled for searches; If
**`false`** piggyback is disabled. By default piggyback is enabled.

Enabling piggyback is more efficient and usually saves a
network-round-trip for first time fetches of records. However, a few
Z39.50 servers do not support piggyback or they ignore element set
names. For those, piggyback should be disabled.

charset  
A string that specifies character set to be used in Z39.50 language and
character set negotiation. Use strings such as: *ISO-8859-1*, *UTF-8*,
*UTF-16*.

Most Z39.50 servers do not support this feature (and thus, this is
ignored). Many servers use the ISO-8859-1 encoding for queries and
messages. MARC21/USMARC records are not affected by this setting.

preferredMessageSize  
An integer that specifies the maximum byte size of all records to be
returned by a target during retrieval. See the
<a href="http://www.loc.gov/z3950/agency/markup/04.html#3.2.1.1.4" class="link external">» Z39.50 standard</a>
for more information.

> **Note**:
>
> This option is supported in PECL YAZ 1.0.5 or later.

maximumRecordSize  
An integer that specifies the maximum byte size of a single record to be
returned by a target during retrieval. This entity is referred to as
Exceptional-record-size in the
<a href="http://www.loc.gov/z3950/agency/markup/04.html#3.2.1.1.4" class="link external">» Z39.50 standard</a>.

> **Note**:
>
> This option is supported in PECL YAZ 1.0.5 or later.

### 返回值

A connection resource on success, **`false`** on error.

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 4.1.0 | The parameter `options` was added. |

### 参见

-   <span class="function">yaz\_close</span>

yaz\_database
=============

Specifies the databases within a session

### 说明

<span class="type">bool</span> <span
class="methodname">yaz\_database</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$databases`</span> )

This function allows you to change databases within a session by
specifying one or more databases to be used in search, retrieval, etc. -
overriding databases specified in call to <span
class="function">yaz\_connect</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`databases`  
A string containing one or more databases. Multiple databases are
separated by a plus sign *+*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

yaz\_element
============

Specifies Element-Set Name for retrieval

### 说明

<span class="type">bool</span> <span
class="methodname">yaz\_element</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> , <span
class="methodparam"><span class="type">string</span>
`$elementset`</span> )

This function sets the element set name for retrieval.

Call this function before <span class="function">yaz\_search</span> or
<span class="function">yaz\_present</span> to specify the element set
name for records to be retrieved.

> **Note**:
>
> If this function appears to have no effect, see the description of the
> *piggybacking* option in <span class="function">yaz\_connect</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`elementset`  
Most servers support *F* (for full records) and *B* (for brief records).

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

yaz\_errno
==========

Returns error number

### 说明

<span class="type">int</span> <span class="methodname">yaz\_errno</span>
( <span class="methodparam"><span class="type">resource</span>
`$id`</span> )

Returns an error number for the server (last request) identified by
`id`.

<span class="function">yaz\_errno</span> should be called after network
activity for each server - (after <span
class="function">yaz\_wait</span> returns) to determine the success or
failure of the last operation (e.g. search).

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

### 返回值

Returns an error code. The error code is either a Z39.50 diagnostic code
(usually a Bib-1 diagnostic) or a client side error code which is
generated by PHP/YAZ itself, such as "Connect failed", "Init Rejected",
etc.

### 参见

-   <span class="function">yaz\_error</span>
-   <span class="function">yaz\_addinfo</span>

yaz\_error
==========

Returns error description

### 说明

<span class="type">string</span> <span
class="methodname">yaz\_error</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> )

<span class="function">yaz\_error</span> returns an English text message
corresponding to the last error number as returned by <span
class="function">yaz\_errno</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

### 返回值

Returns an error text message for server (last request), identified by
parameter `id`. An empty string is returned if the last operation was
successful.

### 参见

-   <span class="function">yaz\_errno</span>
-   <span class="function">yaz\_addinfo</span>

yaz\_es\_result
===============

Inspects Extended Services Result

### 说明

<span class="type">array</span> <span
class="methodname">yaz\_es\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> )

This function inspects the last returned Extended Service result from a
server. An Extended Service is initiated by either <span
class="function">yaz\_item\_order</span> or <span
class="function">yaz\_es</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

### 返回值

Returns array with element *targetReference* for the reference for the
extended service operation (generated and returned from the server).

### 参见

-   <span class="function">yaz\_es</span>

yaz\_es
=======

Prepares for an Extended Service Request

### 说明

<span class="type">void</span> <span class="methodname">yaz\_es</span> (
<span class="methodparam"> <span class="type">resource</span> `$id`
</span> , <span class="methodparam"> <span class="type">string</span>
`$type` </span> , <span class="methodparam"> <span
class="type">array</span> `$args` </span> )

This function prepares for an Extended Service Request. Extended
Services is family of various Z39.50 facilities, such as Record Update,
Item Order, Database administration etc.

> **Note**:
>
> Many Z39.50 Servers do not support Extended Services.

The <span class="function">yaz\_es</span> creates an Extended Service
Request packages and puts it into a queue of operations. Use <span
class="function">yaz\_wait</span> to send the request(s) to the server.
After completion of <span class="function">yaz\_wait</span> the result
of the Extended Service operation should be expected with a call to
<span class="function">yaz\_es\_result</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`type`  
A string which represents the type of the Extended Service: *itemorder*
(Item Order), *create* (Create Database), *drop* (Drop Database),
*commit* (Commit Operation), *update* (Update Record), *xmlupdate* (XML
Update). Each type is specified in the following section.

`args`  
An array with extended service options plus package specific options.
The options are identical to those offered in the C API of ZOOM C. Refer
to the ZOOM
<a href="http://www.indexdata.dk/yaz/doc/zoom.tkl" class="link external">» Extended Services</a>.

### 返回值

没有返回值。

### 范例

**示例 \#1 Record Update**

``` php
<?php
$con = yaz_connect("myhost/database");
$args = array (
    "record" => "<gils><title>some title</title></gils>",
    "syntax" => "xml",
    "action" => "specialUpdate"
);
yaz_es($con, "update", $args);
yaz_wait();
$result = yaz_es_result($id);
?>
```

### 参见

-   <span class="function">yaz\_es\_result</span>

yaz\_get\_option
================

Returns value of option for connection

### 说明

<span class="type">string</span> <span
class="methodname">yaz\_get\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

Returns the value of the option specified with `name`.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`name`  
The option name.

### 返回值

Returns the value of the specified option or an empty string if the
option wasn't set.

### 参见

-   The description of <span class="function">yaz\_set\_option</span>
    for available options

yaz\_hits
=========

Returns number of hits for last search

### 说明

<span class="type">int</span> <span class="methodname">yaz\_hits</span>
( <span class="methodparam"><span class="type">resource</span>
`$id`</span> \[, <span class="methodparam"><span
class="type">array</span> `&$searchresult`</span> \] )

<span class="function">yaz\_hits</span> returns the number of hits for
the last search.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`searchresult`  
Result array for detailed search result information.

### 返回值

Returns the number of hits for the last search or 0 if no search was
performed.

The search result array (if supplied) holds information that is returned
by a Z39.50 server in the SearchResult-1 format part of a search
response. The SearchResult-1 format can be used to obtain information
about hit counts for various parts of the query (subquery). In
particular, it is possible to obtain hit counts for the individual
search terms in a query. Information for first subquery is in
$array\[0\], second subquery in $array\[1\], and so forth.

| Element               | Description                           |
|-----------------------|---------------------------------------|
| *id*                  | Sub query ID2 (string)                |
| *count*               | Result count / hits (integer)         |
| *subquery.term*       | Sub query term (string)               |
| *interpretation.term* | Interpretated sub query term (string) |
| *recommendation.term* | Recommended sub query term (string)   |

> **Note**:
>
> The SearchResult facility requires PECL YAZ 1.0.5 or later and YAZ
> 2.1.9 or later.

> **Note**:
>
> Very few Z39.50 implementations support the SearchResult facility.

yaz\_itemorder
==============

Prepares for Z39.50 Item Order with an ILL-Request package

### 说明

<span class="type">void</span> <span
class="methodname">yaz\_itemorder</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">array</span> `$args`</span>
)

This function prepares for an Extended Services request using the
Profile for the Use of Z39.50 Item Order Extended Service to Transport
ILL (Profile/1). See
<a href="http://www.collectionscanada.ca/iso/ill/stanprf.htm" class="link external">» this</a>
and the
<a href="http://www.collectionscanada.ca/iso/ill/document/standard/z-ill-1a.pdf" class="link external">» specification</a>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`args`  
Must be an associative array with information about the Item Order
request to be sent. The key of the hash is the name of the corresponding
ASN.1 tag path. For example, the ISBN below the Item-ID has the key
item-id,ISBN.

The ILL-Request parameters are:

``` literallayout
protocol-version-num
transaction-id,initial-requester-id,person-or-institution-symbol,person
transaction-id,initial-requester-id,person-or-institution-symbol,institution
transaction-id,initial-requester-id,name-of-person-or-institution,name-of-person
transaction-id,initial-requester-id,name-of-person-or-institution,name-of-institution
transaction-id,transaction-group-qualifier
transaction-id,transaction-qualifier
transaction-id,sub-transaction-qualifier
service-date-time,this,date
service-date-time,this,time
service-date-time,original,date
service-date-time,original,time
requester-id,person-or-institution-symbol,person
requester-id,person-or-institution-symbol,institution
requester-id,name-of-person-or-institution,name-of-person
requester-id,name-of-person-or-institution,name-of-institution
responder-id,person-or-institution-symbol,person
responder-id,person-or-institution-symbol,institution
responder-id,name-of-person-or-institution,name-of-person
responder-id,name-of-person-or-institution,name-of-institution
transaction-type
delivery-address,postal-address,name-of-person-or-institution,name-of-person
delivery-address,postal-address,name-of-person-or-institution,name-of-institution
delivery-address,postal-address,extended-postal-delivery-address
delivery-address,postal-address,street-and-number
delivery-address,postal-address,post-office-box
delivery-address,postal-address,city
delivery-address,postal-address,region
delivery-address,postal-address,country
delivery-address,postal-address,postal-code
delivery-address,electronic-address,telecom-service-identifier
delivery-address,electronic-address,telecom-service-addreess
billing-address,postal-address,name-of-person-or-institution,name-of-person
billing-address,postal-address,name-of-person-or-institution,name-of-institution
billing-address,postal-address,extended-postal-delivery-address
billing-address,postal-address,street-and-number
billing-address,postal-address,post-office-box
billing-address,postal-address,city
billing-address,postal-address,region
billing-address,postal-address,country
billing-address,postal-address,postal-code
billing-address,electronic-address,telecom-service-identifier
billing-address,electronic-address,telecom-service-addreess
ill-service-type
requester-optional-messages,can-send-RECEIVED
requester-optional-messages,can-send-RETURNED
requester-optional-messages,requester-SHIPPED
requester-optional-messages,requester-CHECKED-IN
search-type,level-of-service
search-type,need-before-date
search-type,expiry-date
search-type,expiry-flag
place-on-hold
client-id,client-name
client-id,client-status
client-id,client-identifier
item-id,item-type
item-id,call-number
item-id,author
item-id,title
item-id,sub-title
item-id,sponsoring-body
item-id,place-of-publication
item-id,publisher
item-id,series-title-number
item-id,volume-issue
item-id,edition
item-id,publication-date
item-id,publication-date-of-component
item-id,author-of-article
item-id,title-of-article
item-id,pagination
item-id,ISBN
item-id,ISSN
item-id,additional-no-letters
item-id,verification-reference-source
copyright-complicance
retry-flag
forward-flag
requester-note
forward-note
      
```

There are also a few parameters that are part of the Extended Services
Request package and the ItemOrder package:

``` literallayout
package-name
user-id
contact-name
contact-phone
contact-email
itemorder-item
      
```

### 返回值

没有返回值。

yaz\_present
============

Prepares for retrieval (Z39.50 present)

### 说明

<span class="type">bool</span> <span
class="methodname">yaz\_present</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> )

This function prepares for retrieval of records after a successful
search.

The <span class="function">yaz\_range</span> function should be called
prior to this function to specify the range of records to be retrieved.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

yaz\_range
==========

Specifies a range of records to retrieve

### 说明

<span class="type">void</span> <span
class="methodname">yaz\_range</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> , <span
class="methodparam"><span class="type">int</span> `$start`</span> ,
<span class="methodparam"><span class="type">int</span> `$number`</span>
)

Specifies a range of records to retrieve.

This function should be called before <span
class="function">yaz\_search</span> or <span
class="function">yaz\_present</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`start`  
Specifies the position of the first record to be retrieved. The records
numbers goes from 1 to <span class="function">yaz\_hits</span>.

`number`  
Specifies the number of records to be retrieved.

### 返回值

没有返回值。

yaz\_record
===========

Returns a record

### 说明

<span class="type">string</span> <span
class="methodname">yaz\_record</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> , <span
class="methodparam"><span class="type">int</span> `$pos`</span> , <span
class="methodparam"><span class="type">string</span> `$type`</span> )

The <span class="function">yaz\_record</span> function inspects a record
in the current result set at the position specified by parameter `pos`.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`pos`  
The record position. Records positions in a result set are numbered 1,
2, ... $hits where $hits is the count returned by <span
class="function">yaz\_hits</span>.

`type`  
The `type` specifies the form of the returned record.

> **Note**:
>
> It is the application which is responsible for actually ensuring that
> the records are returned from the Z39.50/SRW server in the proper
> format. The type given only specifies a conversion to take place on
> the client side (in PHP/YAZ).

Besides conversion of the transfer record to a string/array, PHP/YAZ it
is also possible to perform a character set conversion of the record.
Especially for USMARC/MARC21 that is recommended since these are
typically returned in the character set MARC-8 that is not supported by
browsers, etc. To specify a conversion, add *; charset=*<span
class="replaceable">from</span>*,* <span class="replaceable">to</span>
where <span class="replaceable">from</span> is the original character
set of the record and <span class="replaceable">to</span> is the
resulting character set (as seen by PHP).

*string*  
The record is returned as a string for simple display. In this mode, all
MARC records are converted to a line-by-line format since ISO2709 is
hardly readable. XML records and SUTRS are returned in their original
format. GRS-1 are returned in a (ugly) line-by-line format.

This format is suitable if records are to be displayed in a quick way -
for debugging - or because it is not feasible to perform proper display.

*xml*  
The record is returned as an XML string if possible. In this mode, all
MARC records are converted to
<a href="http://www.loc.gov/standards/marcxml/" class="link external">» MARCXML</a>.
XML records and SUTRS are returned in their original format. GRS-1 is
not supported.

This format is similar to `string` except that MARC records are
converted to MARCXML

This format is suitable if records are processed by an XML parser or
XSLT processor afterwards.

*raw*  
The record is returned as a string in its original form. This type is
suitable for MARC, XML and SUTRS. It does not work for GRS-1.

MARC records are returned as a ISO2709 string. XML and SUTRS are
returned as strings.

*syntax*  
The syntax of the record is returned as a string, i.e. *USmarc*,
*GRS-1*, *XML*, etc.

*database*  
The name of database associated with record at the position is returned
as a string.

*array*  
The record is returned as an array that reflects the GRS-1 structure.
This type is suitable for MARC and GRS-1. XML, SUTRS are not supported
and if the actual record is XML or SUTRS an empty string will be
returned.

The array returned consists of a list corresponding to each
leaf/internal node of GRS-1. Each list item consists a sub list with
first element *path* and *data* (if data is available).

The path which is a string holds a list of each tree component (of the
structured GRS-1 record) from root to leaf. Each component is a tag
type, tag value pair of the form *(*<span
class="replaceable">type</span>*,* <span
class="replaceable">value</span>

String tags normally has a corresponding tag type 3. MARC can also be
returned as an array (they are converted to GRS-1 internally).

### 返回值

Returns the record at position `pos` or an empty string if no record
exists at the given position.

If no database record exists at the given position an empty string is
returned.

### 范例

**示例 \#1 Array for GRS-1 record**

Consider this GRS-1 record:

``` examples
(4,52)Robert M. Pirsig
(4,70)
      (4,90)
            (2,7)Transworld Publishers, ltd.
```

This record has two nodes at root level. First element at root level is
(4,52) \[tag type 4, tag value 52\], and has data *Robert M. Pirsig*.
Second element at root level (4,70) has a subtree with a single element
(4,90). (4,90) has yet another sub tree (2,7) with data *Transworld
Publishers, ltd.*.

If this record is present at position $p, then

``` php
<?php

$ar = yaz_record($id, $p, "array");
print_r($ar);

?>
```

will output:

    Array
    (
        [0] => Array
            (
                [0] => (4,52)
                [1] => Robert M. Pirsig
            )
        [1] => Array
            (
                [0] => (4,70)
            )
        [2] => Array
            (
                [0] => (4,70)(4,90)
            )
        [3] => Array
            (
                [0] => (4,70)(4,90)(2,7)
                [1] => Transworld Publishers, ltd.
            )
    )      

**示例 \#2 Working with MARCXML**

The following PHP snippet returns a MARC21/USMARC record as MARCXML. The
original record is returned in marc-8 (unknown to most XML parsers), so
we convert it to UTF-8 (which all XML parsers must support).

``` php
<?php
$rec = yaz_record($id, $p, "xml; charset=marc-8,utf-8");
?>
```

The record *$rec* can be processed with the Sablotron XSLT processor as
follows:

``` php
<?php

$xslfile = 'display.xsl';
$processor = xslt_create();
$parms = array('/_xml' => $rec);
$res = xslt_process($processor, 'arg:/_xml', $xslfile, NULL, $parms);
xslt_free($processor);
$res = preg_replace("'</?html[^>]*>'", '', $res);
echo $res;

?>
```

For PHP 5 the <a href="/book/xsl.html" class="link">XSL</a> extension
must be used instead of Sablotron XSLT.

yaz\_scan\_result
=================

Returns Scan Response result

### 说明

<span class="type">array</span> <span
class="methodname">yaz\_scan\_result</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> \[,
<span class="methodparam"><span class="type">array</span>
`&$result`</span> \] )

<span class="function">yaz\_scan\_result</span> returns terms and
associated information as received from the server in the last performed
<span class="function">yaz\_scan</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`result`  
If given, this array will be modified to hold additional information
taken from the Scan Response:

-   *number* - Number of entries returned

-   *stepsize* - Step size

-   *position* - Position of term

-   *status* - Scan status

### 返回值

Returns an array (0..n-1) where n is the number of terms returned. Each
value is a pair where the first item is the term, and the second item is
the result-count.

yaz\_scan
=========

Prepares for a scan

### 说明

<span class="type">void</span> <span class="methodname">yaz\_scan</span>
( <span class="methodparam"><span class="type">resource</span>
`$id`</span> , <span class="methodparam"><span
class="type">string</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$startterm`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$flags`</span> \] )

This function prepares for a Z39.50 Scan Request on the specified
connection.

To actually transfer the Scan Request to the server and receive the Scan
Response, <span class="function">yaz\_wait</span> must be called. Upon
completion of <span class="function">yaz\_wait</span> call <span
class="function">yaz\_error</span> and <span
class="function">yaz\_scan\_result</span> to handle the response.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`type`  
Currently only type *rpn* is supported.

`startterm`  
Starting term point for the scan.

The form in which the starting term is specified is given by parameter
`type`.

The syntax this parameter is similar to the RPN query as described in
<span class="function">yaz\_search</span>. It consists of zero or more
*@attr*-operator specifications, then followed by exactly one token.

`flags`  
This optional parameter specifies additional information to control the
behaviour of the scan request. Three indexes are currently read from the
flags array: *number* (number of terms requested), *position* (preferred
position of term) and *stepSize* (preferred step size).

### 返回值

没有返回值。

### 范例

**示例 \#1 PHP function that scans titles**

``` php
<?php
function scan_titles($id, $startterm) 
{
  yaz_scan($id, "rpn", "@attr 1=4 " . $startterm);
  yaz_wait();
  $errno = yaz_errno($id);
  if ($errno == 0) {
    $ar = yaz_scan_result($id, $options);
    echo 'Scan ok; ';
    foreach ($options as $key => $val) {
      echo "$key = $val &nbsp;";
    }
    echo '<br /><table>';
    while (list($key, list($k, $term, $tcount)) = each($ar)) {
      if (empty($k)) continue;
      echo "<tr><td>$term</td><td>$tcount</td></tr>";
    }
    echo '</table>';
  } else {
    echo "Scan failed. Error: " . yaz_error($id) . "<br />";
  }
}
?>
```

yaz\_schema
===========

Specifies schema for retrieval

### 说明

<span class="type">void</span> <span
class="methodname">yaz\_schema</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> , <span
class="methodparam"><span class="type">string</span> `$schema`</span> )

<span class="function">yaz\_schema</span> specifies the schema for
retrieval.

This function should be called before <span
class="function">yaz\_search</span> or <span
class="function">yaz\_present</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`schema`  
Must be specified as an OID (Object Identifier) in a raw dot-notation
(like *1.2.840.10003.13.4*) or as one of the known registered schemas:
*GILS-schema*, *Holdings*, *Zthes*, ...

### 返回值

没有返回值。

yaz\_search
===========

Prepares for a search

### 说明

<span class="type">bool</span> <span
class="methodname">yaz\_search</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> , <span
class="methodparam"><span class="type">string</span> `$type`</span> ,
<span class="methodparam"><span class="type">string</span>
`$query`</span> )

<span class="function">yaz\_search</span> prepares for a search on the
given connection.

Like <span class="function">yaz\_connect</span> this function is
non-blocking and only prepares for a search to be executed later when
<span class="function">yaz\_wait</span> is called.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`type`  
This parameter represents the query type - only *"rpn"* is supported now
in which case the third argument specifies a Type-1 query in prefix
query notation.

`query`  
The RPN query is a textual representation of the Type-1 query as defined
by the Z39.50 standard. However, in the text representation as used by
YAZ a prefix notation is used, that is the operator precedes the
operands. The query string is a sequence of tokens where white space is
ignored unless surrounded by double quotes. Tokens beginning with an
at-character (*@*) are considered operators, otherwise they are treated
as search terms.

| Construct                        | Description                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *@and* query1 query2             | intersection of query1 and query2                                                                                                                                           |
| *@or* query1 query2              | union of query1 and query2                                                                                                                                                  |
| *@not* query1 query2             | query1 and not query2                                                                                                                                                       |
| *@set* name                      | result set reference                                                                                                                                                        |
| *@attrset* set query             | specifies attribute-set for query. This construction is only allowed once - in the beginning of the whole query                                                             |
| *@attr* \[set\] type=value query | applies attribute to query. The type and value are integers specifying the attribute-type and attribute-value respectively. The set, if given, specifies the attribute-set. |

You can find information about attributes at the
<a href="http://www.loc.gov/z3950/agency/defns/bib1.html" class="link external">» Z39.50 Maintenance Agency</a>
site.

> **Note**:
>
> If you would like to use a more friendly notation, use the CCL
> parser - functions <span class="function">yaz\_ccl\_conf</span> and
> <span class="function">yaz\_ccl\_parse</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Query Examples**

You can search for simple terms, like this:

``` examples
computer
```

which matches documents where "computer" occur. No attributes are
specified.

The query

``` examples
"knuth donald"
```

matches documents where "knuth donald" occur (provided that the server
supports phrase search).

This query applies two attributes for the same phrase.

@attr 1=1003 @attr 4=1 "knuth donald"

First attribute is type 1 (Bib-1 use), attribute value is 1003 (Author).
Second attribute has is type 4 (structure), value 1 (phrase), so this
should match documents where Donald Knuth is author.

The query

``` examples
@and @or a b @not @or c d e
```

would in infix notation look like *(a or b) and ((c or d) not e)*.

Another, more complex, one:

    @attrset gils @and @attr 1=4 art @attr 1=2000 company

The query as a whole uses the GILS attributeset. The query matches
documents where *art* occur in the title (GILS,BIB-1) and in which
*company* occur as Distributor (GILS).

yaz\_set\_option
================

Sets one or more options for connection

### 说明

<span class="type">void</span> <span
class="methodname">yaz\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

<span class="type">void</span> <span
class="methodname">yaz\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span> `$id`</span> ,
<span class="methodparam"><span class="type">array</span>
`$options`</span> )

Sets one or more options on the given connection.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`name` or `options`  
May be either a string or an array.

If given as a string, this will be the name of the option to set. You'll
need to give it's `value`.

If given as an array, this will be an associative array (option name =\>
option value).

| Name                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| implementationName    | implementation name of server                                                                                                                                                                                                                                                                                                                                                                                                             |
| implementationVersion | implementation version of server                                                                                                                                                                                                                                                                                                                                                                                                          |
| implementationId      | implementation ID of server                                                                                                                                                                                                                                                                                                                                                                                                               |
| schema                | schema for retrieval. By default, no schema is used. Setting this option is equivalent to using function <span class="function">yaz\_schema</span>                                                                                                                                                                                                                                                                                        |
| preferredRecordSyntax | record syntax for retrieval. By default, no syntax is used. Setting this option is equivalent to using function <span class="function">yaz\_syntax</span>                                                                                                                                                                                                                                                                                 |
| start                 | offset for first record to be retrieved via <span class="function">yaz\_search</span> or <span class="function">yaz\_present</span>. First record is numbered has a start value of 0. Second record has start value 1. Setting this option in combination with option *count* has the same effect as calling <span class="function">yaz\_range</span> except that records are numbered from 1 in <span class="function">yaz\_range</span> |
| count                 | maximum number of records to be retrieved via <span class="function">yaz\_search</span> or <span class="function">yaz\_present</span>.                                                                                                                                                                                                                                                                                                    |
| elementSetName        | element-set-name for retrieval. Setting this option is equivalent to calling <span class="function">yaz\_element</span>.                                                                                                                                                                                                                                                                                                                  |

`value`  
The new value of the option. Use this only if the previous argument is a
string.

### 返回值

没有返回值。

yaz\_sort
=========

Sets sorting criteria

### 说明

<span class="type">void</span> <span class="methodname">yaz\_sort</span>
( <span class="methodparam"><span class="type">resource</span>
`$id`</span> , <span class="methodparam"><span
class="type">string</span> `$criteria`</span> )

This function sets sorting criteria and enables Z39.50 Sort.

Call this function *before* <span class="function">yaz\_search</span>.
Using this function alone does not have any effect. When used in
conjunction with <span class="function">yaz\_search</span>, a Z39.50
Sort will be sent after a search response has been received and before
any records are retrieved with Z39.50 Present (<span
class="function">yaz\_present</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`criteria`  
A string that takes the form <span class="replaceable">field1 flags1
field2 flags2</span> where field1 specifies the primary attributes for
sort, field2 seconds, etc..

The field specifies either a numerical attribute combinations consisting
of type=value pairs separated by comma (e.g. *1=4,2=1*) ; or the field
may specify a plain string criteria (e.g. *title*. The flags is a
sequence of the following characters which may not be separated by any
white space.

*a*  
Sort ascending

*d*  
Sort descending

*i*  
Case insensitive sorting

*s*  
Case sensitive sorting

### 返回值

没有返回值。

### 范例

**示例 \#1 Sort Criterias**

To sort on Bib1 attribute title, case insensitive, and ascending you
would use the following sort criteria:

``` examples
1=4 ia
```

If the secondary sorting criteria should be author, case sensitive and
ascending you would use:

``` examples
1=4 ia 1=1003 sa
```

yaz\_syntax
===========

Specifies the preferred record syntax for retrieval

### 说明

<span class="type">void</span> <span
class="methodname">yaz\_syntax</span> ( <span class="methodparam"><span
class="type">resource</span> `$id`</span> , <span
class="methodparam"><span class="type">string</span> `$syntax`</span> )

<span class="function">yaz\_syntax</span> specifies the preferred record
syntax for retrieval

This function should be called before <span
class="function">yaz\_search</span> or <span
class="function">yaz\_present</span>.

### 参数

`id`  
The connection resource returned by <span
class="function">yaz\_connect</span>.

`syntax`  
The syntax must be specified as an OID (Object Identifier) in a raw
dot-notation (like *1.2.840.10003.5.10*) or as one of the known
registered record syntaxes (sutrs, usmarc, grs1, xml, etc.).

### 返回值

没有返回值。

yaz\_wait
=========

Wait for Z39.50 requests to complete

### 说明

<span class="type">mixed</span> <span
class="methodname">yaz\_wait</span> (\[ <span class="methodparam"><span
class="type">array</span> `&$options`</span> \] )

This function carries out networked (blocked) activity for outstanding
requests which have been prepared by the functions <span
class="function">yaz\_connect</span>, <span
class="function">yaz\_search</span>, <span
class="function">yaz\_present</span>, <span
class="function">yaz\_scan</span> and <span
class="function">yaz\_itemorder</span>.

<span class="function">yaz\_wait</span> returns when all servers have
either completed all requests or aborted (in case of errors).

### 参数

`options`  
An associative array of options:

*timeout*  
Sets timeout in seconds. If a server has not responded within the
timeout it is considered dead and <span
class="function">yaz\_wait</span> returns. The default value for timeout
is 15 seconds.

*event*  
A boolean.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。 In event mode,
returns resource 或者在失败时返回 **`false`**.

**目录**

-   [yaz\_addinfo](/ref/yaz.html#yaz_addinfo) — Returns additional error
    information
-   [yaz\_ccl\_conf](/ref/yaz.html#yaz_ccl_conf) — Configure CCL parser
-   [yaz\_ccl\_parse](/ref/yaz.html#yaz_ccl_parse) — Invoke CCL Parser
-   [yaz\_close](/ref/yaz.html#yaz_close) — Close YAZ connection
-   [yaz\_connect](/ref/yaz.html#yaz_connect) — Prepares for a
    connection to a Z39.50 server
-   [yaz\_database](/ref/yaz.html#yaz_database) — Specifies the
    databases within a session
-   [yaz\_element](/ref/yaz.html#yaz_element) — Specifies Element-Set
    Name for retrieval
-   [yaz\_errno](/ref/yaz.html#yaz_errno) — Returns error number
-   [yaz\_error](/ref/yaz.html#yaz_error) — Returns error description
-   [yaz\_es\_result](/ref/yaz.html#yaz_es_result) — Inspects Extended
    Services Result
-   [yaz\_es](/ref/yaz.html#yaz_es) — Prepares for an Extended Service
    Request
-   [yaz\_get\_option](/ref/yaz.html#yaz_get_option) — Returns value of
    option for connection
-   [yaz\_hits](/ref/yaz.html#yaz_hits) — Returns number of hits for
    last search
-   [yaz\_itemorder](/ref/yaz.html#yaz_itemorder) — Prepares for Z39.50
    Item Order with an ILL-Request package
-   [yaz\_present](/ref/yaz.html#yaz_present) — Prepares for retrieval
    (Z39.50 present)
-   [yaz\_range](/ref/yaz.html#yaz_range) — Specifies a range of records
    to retrieve
-   [yaz\_record](/ref/yaz.html#yaz_record) — Returns a record
-   [yaz\_scan\_result](/ref/yaz.html#yaz_scan_result) — Returns Scan
    Response result
-   [yaz\_scan](/ref/yaz.html#yaz_scan) — Prepares for a scan
-   [yaz\_schema](/ref/yaz.html#yaz_schema) — Specifies schema for
    retrieval
-   [yaz\_search](/ref/yaz.html#yaz_search) — Prepares for a search
-   [yaz\_set\_option](/ref/yaz.html#yaz_set_option) — Sets one or more
    options for connection
-   [yaz\_sort](/ref/yaz.html#yaz_sort) — Sets sorting criteria
-   [yaz\_syntax](/ref/yaz.html#yaz_syntax) — Specifies the preferred
    record syntax for retrieval
-   [yaz\_wait](/ref/yaz.html#yaz_wait) — Wait for Z39.50 requests to
    complete
