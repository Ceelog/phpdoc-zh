LDAP controls
=============

Controls are special objects which may be sent alongside an LDAP request
to alter LDAP server behavior while performing the request. There may
also be controls sent by the server alongside the response to provide
more information, usually to answer a control object from the request.

> **Note**:
>
> Not all controls are supported by all LDAP servers. To know which
> controls are supported by a server, you need to query the root DSE by
> reading an empty dn with the filter (objectClass=\*).
>
> **示例 \#1 Testing support for paged result control**
>
> ``` php
> <?php
>
> // $ds is a valid link identifier for a directory server
>
> $result = ldap_read($ds, '', '(objectClass=*)', ['supportedControl']);
> if (!in_array(LDAP_CONTROL_PAGEDRESULTS, ldap_get_entries($ds, $result)[0]['supportedcontrol'])) {
>   die("This server does not support paged result control");
> }
>
> ?>
> ```

As of PHP 7.3, you can send controls with your request in all request
functions using the serverctrls parameter. When a ext version of a
function exists, you should use it if you want to get access to the full
response object and be able to parse response controls from it using
<span class="function">ldap\_parse\_result</span>.

serverctrls must be an array containing an array for each control to
send, containing the following keys:

oid (<span class="type">string</span>)  
<span class="simpara"> The OID of the control. You should use constants
starting with LDAP\_CONTROL\_ for this. See
<a href="/ldap/constants.html" class="link">LDAP Constants</a>. </span>

iscritical (<span class="type">boolean</span>)  
<span class="simpara"> If a control is noted as critical, the request
will fail if the control is not supported by the server, or if it fails
to be applied. Note that some controls should always be marked as
critical as noted in the RFC introducing them. Defaults to **`FALSE`**.
</span>

value (<span class="type">mixed</span>)  
<span class="simpara"> If applicable, the value of the control. Read
below for more information. </span>

Most control values are sent to the server BER-encoded. You may either
BER-encode the value yourself, or you can instead pass an array with the
correct keys so that the encoding is done for you. Supported controls to
be passed as an array are:

-   **`LDAP_CONTROL_PAGEDRESULTS`** Expected keys are \[size\] and
    \[cookie\]

-   **`LDAP_CONTROL_ASSERT`** Expected key is filter

-   **`LDAP_CONTROL_VALUESRETURNFILTER`** Expected key is filter

-   **`LDAP_CONTROL_PRE_READ`** Expected key is attrs

-   **`LDAP_CONTROL_POST_READ`** Expected key is attrs

-   **`LDAP_CONTROL_SORTREQUEST`** Expects an array of arrays with keys
    attr, \[oid\], \[reverse\].

-   **`LDAP_CONTROL_VLVREQUEST`** Expected keys are before, after,
    attrvalue\|(offset, count), \[context\]

The following controls do not need any value:

-   **`LDAP_CONTROL_PASSWORDPOLICYREQUEST`**

-   **`LDAP_CONTROL_MANAGEDSAIT`**

-   **`LDAP_CONTROL_DONTUSECOPY`**

The control **`LDAP_CONTROL_PROXY_AUTHZ`** is a special case as its
value is not expected to be BER-encoded, so you can directly use a
string for its value.

When controls are parsed by <span
class="function">ldap\_parse\_result</span>, values are turned into an
array if supported. This is supported for:

-   **`LDAP_CONTROL_PASSWORDPOLICYRESPONSE`** Keys are expire, grace,
    \[error\]

-   **`LDAP_CONTROL_PAGEDRESULTS`** Keys are size, cookie

-   **`LDAP_CONTROL_PRE_READ`** Keys are dn and LDAP attributes names

-   **`LDAP_CONTROL_POST_READ`** Keys are dn and LDAP attributes names

-   **`LDAP_CONTROL_SORTRESPONSE`** Keys are errcode, \[attribute\]

-   **`LDAP_CONTROL_VLVRESPONSE`** Keys are target, count, errcode,
    context
