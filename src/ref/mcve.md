Additional documentation about MCVE/Monetra's PHP API can be found at
<a href="http://www.mainstreetsoftworks.com/documentation.html" class="link external">» http://www.mainstreetsoftworks.com/documentation.html</a>.
Main Street's documentation is complete and should be the primary
reference for functions.

m\_checkstatus
==============

Check to see if a transaction has completed

### 说明

<span class="type">int</span> <span
class="methodname">m\_checkstatus</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_completeauthorizations
=========================

Number of complete authorizations in queue, returning an array of their
identifiers

### 说明

<span class="type">int</span> <span
class="methodname">m\_completeauthorizations</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span> `&$array`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`array`  
Its description

### 返回值

What the function returns, first on success, then on failure. See also
the &return.success; entity

m\_connect
==========

Establish the connection to MCVE

### 说明

<span class="type">int</span> <span class="methodname">m\_connect</span>
( <span class="methodparam"><span class="type">resource</span>
`$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

m\_connectionerror
==================

Get a textual representation of why a connection failed

### 说明

<span class="type">string</span> <span
class="methodname">m\_connectionerror</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

m\_deletetrans
==============

Delete specified transaction from MCVE\_CONN structure

### 说明

<span class="type">bool</span> <span
class="methodname">m\_deletetrans</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_destroyconn
==============

Destroy the connection and MCVE\_CONN structure

### 说明

<span class="type">bool</span> <span
class="methodname">m\_destroyconn</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

Returns **`TRUE`**.

### 参见

-   <span class="function">m\_initconn</span>

m\_destroyengine
================

Free memory associated with IP/SSL connectivity

### 说明

<span class="type">void</span> <span
class="methodname">m\_destroyengine</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

### 返回值

没有返回值。

m\_getcell
==========

Get a specific cell from a comma delimited response by column name

### 说明

<span class="type">string</span> <span
class="methodname">m\_getcell</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn`</span> , <span
class="methodparam"><span class="type">int</span> `$identifier`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column`</span> , <span class="methodparam"><span
class="type">int</span> `$row`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

`column`  

`row`  

### 返回值

m\_getcellbynum
===============

Get a specific cell from a comma delimited response by column number

### 说明

<span class="type">string</span> <span
class="methodname">m\_getcellbynum</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> , <span class="methodparam"><span
class="type">int</span> `$column`</span> , <span
class="methodparam"><span class="type">int</span> `$row`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

`column`  

`row`  

### 返回值

m\_getcommadelimited
====================

Get the RAW comma delimited data returned from MCVE

### 说明

<span class="type">string</span> <span
class="methodname">m\_getcommadelimited</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_getheader
============

Get the name of the column in a comma-delimited response

### 说明

<span class="type">string</span> <span
class="methodname">m\_getheader</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn`</span> , <span
class="methodparam"><span class="type">int</span> `$identifier`</span> ,
<span class="methodparam"><span class="type">int</span>
`$column_num`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

`column_num`  

### 返回值

m\_initconn
===========

Create and initialize an MCVE\_CONN structure

### 说明

<span class="type">resource</span> <span
class="methodname">m\_initconn</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

Returns an MCVE\_CONN resource.

### 参见

-   <span class="function">m\_destroyconn</span>

m\_initengine
=============

Ready the client for IP/SSL Communication

### 说明

<span class="type">int</span> <span
class="methodname">m\_initengine</span> ( <span
class="methodparam"><span class="type">string</span> `$location`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`location`  

### 返回值

m\_iscommadelimited
===================

Checks to see if response is comma delimited

### 说明

<span class="type">int</span> <span
class="methodname">m\_iscommadelimited</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_maxconntimeout
=================

The maximum amount of time the API will attempt a connection to MCVE

### 说明

<span class="type">bool</span> <span
class="methodname">m\_maxconntimeout</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span> `$secs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`secs`  

### 返回值

m\_monitor
==========

Perform communication with MCVE (send/receive data) Non-blocking

### 说明

<span class="type">int</span> <span class="methodname">m\_monitor</span>
( <span class="methodparam"><span class="type">resource</span>
`$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

m\_numcolumns
=============

Number of columns returned in a comma delimited response

### 说明

<span class="type">int</span> <span
class="methodname">m\_numcolumns</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_numrows
==========

Number of rows returned in a comma delimited response

### 说明

<span class="type">int</span> <span class="methodname">m\_numrows</span>
( <span class="methodparam"><span class="type">resource</span>
`$conn`</span> , <span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_parsecommadelimited
======================

Parse the comma delimited response so m\_getcell, etc will work

### 说明

<span class="type">int</span> <span
class="methodname">m\_parsecommadelimited</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_responsekeys
===============

Returns array of strings which represents the keys that can be used for
response parameters on this transaction

### 说明

<span class="type">array</span> <span
class="methodname">m\_responsekeys</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_responseparam
================

Get a custom response parameter

### 说明

<span class="type">string</span> <span
class="methodname">m\_responseparam</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

`key`  

### 返回值

m\_returnstatus
===============

Check to see if the transaction was successful

### 说明

<span class="type">int</span> <span
class="methodname">m\_returnstatus</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_setblocking
==============

Set blocking/non-blocking mode for connection

### 说明

<span class="type">int</span> <span
class="methodname">m\_setblocking</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span> `$tf`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`tf`  

### 返回值

m\_setdropfile
==============

Set the connection method to Drop-File

### 说明

<span class="type">int</span> <span
class="methodname">m\_setdropfile</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`directory`  

### 返回值

m\_setip
========

Set the connection method to IP

### 说明

<span class="type">int</span> <span class="methodname">m\_setip</span> (
<span class="methodparam"><span class="type">resource</span>
`$conn`</span> , <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`host`  

`port`  

### 返回值

m\_setssl\_cafile
=================

Set SSL CA (Certificate Authority) file for verification of server
certificate

### 说明

<span class="type">int</span> <span
class="methodname">m\_setssl\_cafile</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$cafile`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`cafile`  

### 返回值

m\_setssl\_files
================

Set certificate key files and certificates if server requires client
certificate verification

### 说明

<span class="type">int</span> <span
class="methodname">m\_setssl\_files</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">string</span>
`$sslkeyfile`</span> , <span class="methodparam"><span
class="type">string</span> `$sslcertfile`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`sslkeyfile`  

`sslcertfile`  

### 返回值

m\_setssl
=========

Set the connection method to SSL

### 说明

<span class="type">int</span> <span class="methodname">m\_setssl</span>
( <span class="methodparam"><span class="type">resource</span>
`$conn`</span> , <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`host`  

`port`  

### 返回值

m\_settimeout
=============

Set maximum transaction time (per trans)

### 说明

<span class="type">int</span> <span
class="methodname">m\_settimeout</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$seconds`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`seconds`  

### 返回值

m\_sslcert\_gen\_hash
=====================

Generate hash for SSL client certificate verification

### 说明

<span class="type">string</span> <span
class="methodname">m\_sslcert\_gen\_hash</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filename`  

### 返回值

m\_transactionssent
===================

Check to see if outgoing buffer is clear

### 说明

<span class="type">int</span> <span
class="methodname">m\_transactionssent</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

m\_transinqueue
===============

Number of transactions in client-queue

### 说明

<span class="type">int</span> <span
class="methodname">m\_transinqueue</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

m\_transkeyval
==============

Add key/value pair to a transaction. Replaces deprecated transparam()

### 说明

<span class="type">int</span> <span
class="methodname">m\_transkeyval</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span>
`$identifier`</span> , <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

`key`  

`value`  

### 返回值

m\_transnew
===========

Start a new transaction

### 说明

<span class="type">int</span> <span
class="methodname">m\_transnew</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

### 返回值

m\_transsend
============

Finalize and send the transaction

### 说明

<span class="type">int</span> <span
class="methodname">m\_transsend</span> ( <span class="methodparam"><span
class="type">resource</span> `$conn`</span> , <span
class="methodparam"><span class="type">int</span> `$identifier`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`identifier`  

### 返回值

m\_uwait
========

Wait x microsecs

### 说明

<span class="type">int</span> <span class="methodname">m\_uwait</span> (
<span class="methodparam"><span class="type">int</span>
`$microsecs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`microsecs`  

### 返回值

m\_validateidentifier
=====================

Whether or not to validate the passed identifier on any transaction it
is passed to

### 说明

<span class="type">int</span> <span
class="methodname">m\_validateidentifier</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span> `$tf`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`tf`  

### 返回值

m\_verifyconnection
===================

Set whether or not to PING upon connect to verify connection

### 说明

<span class="type">bool</span> <span
class="methodname">m\_verifyconnection</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span> `$tf`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`tf`  

### 返回值

m\_verifysslcert
================

Set whether or not to verify the server ssl certificate

### 说明

<span class="type">bool</span> <span
class="methodname">m\_verifysslcert</span> ( <span
class="methodparam"><span class="type">resource</span> `$conn`</span> ,
<span class="methodparam"><span class="type">int</span> `$tf`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

` conn`  
由 <span class="function">m\_initengine</span> 返回的 MCVE\_CONN 资源。

`tf`  

### 返回值

**目录**

-   [m\_checkstatus](/ref/mcve.html#m_checkstatus) — Check to see if a
    transaction has completed
-   [m\_completeauthorizations](/ref/mcve.html#m_completeauthorizations)
    — Number of complete authorizations in queue, returning an array of
    their identifiers
-   [m\_connect](/ref/mcve.html#m_connect) — Establish the connection to
    MCVE
-   [m\_connectionerror](/ref/mcve.html#m_connectionerror) — Get a
    textual representation of why a connection failed
-   [m\_deletetrans](/ref/mcve.html#m_deletetrans) — Delete specified
    transaction from MCVE\_CONN structure
-   [m\_destroyconn](/ref/mcve.html#m_destroyconn) — Destroy the
    connection and MCVE\_CONN structure
-   [m\_destroyengine](/ref/mcve.html#m_destroyengine) — Free memory
    associated with IP/SSL connectivity
-   [m\_getcell](/ref/mcve.html#m_getcell) — Get a specific cell from a
    comma delimited response by column name
-   [m\_getcellbynum](/ref/mcve.html#m_getcellbynum) — Get a specific
    cell from a comma delimited response by column number
-   [m\_getcommadelimited](/ref/mcve.html#m_getcommadelimited) — Get the
    RAW comma delimited data returned from MCVE
-   [m\_getheader](/ref/mcve.html#m_getheader) — Get the name of the
    column in a comma-delimited response
-   [m\_initconn](/ref/mcve.html#m_initconn) — Create and initialize an
    MCVE\_CONN structure
-   [m\_initengine](/ref/mcve.html#m_initengine) — Ready the client for
    IP/SSL Communication
-   [m\_iscommadelimited](/ref/mcve.html#m_iscommadelimited) — Checks to
    see if response is comma delimited
-   [m\_maxconntimeout](/ref/mcve.html#m_maxconntimeout) — The maximum
    amount of time the API will attempt a connection to MCVE
-   [m\_monitor](/ref/mcve.html#m_monitor) — Perform communication with
    MCVE (send/receive data) Non-blocking
-   [m\_numcolumns](/ref/mcve.html#m_numcolumns) — Number of columns
    returned in a comma delimited response
-   [m\_numrows](/ref/mcve.html#m_numrows) — Number of rows returned in
    a comma delimited response
-   [m\_parsecommadelimited](/ref/mcve.html#m_parsecommadelimited) —
    Parse the comma delimited response so m\_getcell, etc will work
-   [m\_responsekeys](/ref/mcve.html#m_responsekeys) — Returns array of
    strings which represents the keys that can be used for response
    parameters on this transaction
-   [m\_responseparam](/ref/mcve.html#m_responseparam) — Get a custom
    response parameter
-   [m\_returnstatus](/ref/mcve.html#m_returnstatus) — Check to see if
    the transaction was successful
-   [m\_setblocking](/ref/mcve.html#m_setblocking) — Set
    blocking/non-blocking mode for connection
-   [m\_setdropfile](/ref/mcve.html#m_setdropfile) — Set the connection
    method to Drop-File
-   [m\_setip](/ref/mcve.html#m_setip) — Set the connection method to IP
-   [m\_setssl\_cafile](/ref/mcve.html#m_setssl_cafile) — Set SSL CA
    (Certificate Authority) file for verification of server certificate
-   [m\_setssl\_files](/ref/mcve.html#m_setssl_files) — Set certificate
    key files and certificates if server requires client certificate
    verification
-   [m\_setssl](/ref/mcve.html#m_setssl) — Set the connection method to
    SSL
-   [m\_settimeout](/ref/mcve.html#m_settimeout) — Set maximum
    transaction time (per trans)
-   [m\_sslcert\_gen\_hash](/ref/mcve.html#m_sslcert_gen_hash) —
    Generate hash for SSL client certificate verification
-   [m\_transactionssent](/ref/mcve.html#m_transactionssent) — Check to
    see if outgoing buffer is clear
-   [m\_transinqueue](/ref/mcve.html#m_transinqueue) — Number of
    transactions in client-queue
-   [m\_transkeyval](/ref/mcve.html#m_transkeyval) — Add key/value pair
    to a transaction. Replaces deprecated transparam()
-   [m\_transnew](/ref/mcve.html#m_transnew) — Start a new transaction
-   [m\_transsend](/ref/mcve.html#m_transsend) — Finalize and send the
    transaction
-   [m\_uwait](/ref/mcve.html#m_uwait) — Wait x microsecs
-   [m\_validateidentifier](/ref/mcve.html#m_validateidentifier) —
    Whether or not to validate the passed identifier on any transaction
    it is passed to
-   [m\_verifyconnection](/ref/mcve.html#m_verifyconnection) — Set
    whether or not to PING upon connect to verify connection
-   [m\_verifysslcert](/ref/mcve.html#m_verifysslcert) — Set whether or
    not to verify the server ssl certificate
