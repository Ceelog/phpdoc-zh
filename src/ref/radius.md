radius\_acct\_open
==================

Creates a Radius handle for accounting

### 说明

<span class="type">resource</span> <span
class="methodname">radius\_acct\_open</span> ( <span
class="methodparam">void</span> )

### 返回值

Returns a handle on success, **`FALSE`** on error. This function only
fails if insufficient memory is available.

### 范例

**示例 \#1 <span class="function">radius\_acct\_open</span> example**

``` php
<?php
$res = radius_acct_open ()
    or die ("Could not create handle");
print("Handle successfully created");
?>
```

radius\_add\_server
===================

Adds a server

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_add\_server</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">string</span> `$hostname`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">string</span> `$secret`</span> ,
<span class="methodparam"><span class="type">int</span>
`$timeout`</span> , <span class="methodparam"><span
class="type">int</span> `$max_tries`</span> )

<span class="function">radius\_add\_server</span> may be called multiple
times, and it may be used together with <span
class="function">radius\_config</span>. At most 10 servers may be
specified. When multiple servers are given, they are tried in
round-robin fashion until a valid response is received, or until each
server's `max_tries` limit has been reached.

### 参数

`radius_handle`  

`hostname`  
The `hostname` parameter specifies the server host, either as a fully
qualified domain name or as a dotted-quad IP address in text form.

`port`  
The `port` specifies the UDP port to contact on the server. If port is
given as 0, the library looks up the `radius/udp` or `radacct/udp`
service in the network services database, and uses the port found there.
If no entry is found, the library uses the standard Radius ports, 1812
for authentication and 1813 for accounting.

`secret`  
The shared secret for the server host is passed to the `secret`
parameter. The Radius protocol ignores all but the leading 128 bytes of
the shared secret.

`timeout`  
The timeout for receiving replies from the server is passed to the
`timeout` parameter, in units of seconds.

`max_tries`  
The maximum number of repeated requests to make before giving up is
passed into the `max_tries`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">radius\_add\_server</span> example**

``` php
<?php
if (!radius_add_server($res, 'radius.example.com', 1812, 'testing123', 3, 3)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br>";
    exit;
}
?>
```

### 参见

-   <span class="function">radius\_config</span>

radius\_auth\_open
==================

Creates a Radius handle for authentication

### 说明

<span class="type">resource</span> <span
class="methodname">radius\_auth\_open</span> ( <span
class="methodparam">void</span> )

### 返回值

Returns a handle on success, **`FALSE`** on error. This function only
fails if insufficient memory is available.

### 范例

**示例 \#1 <span class="function">radius\_auth\_open</span> example**

``` php
<?php
$radh = radius_auth_open()
    or die ("Could not create handle");
echo "Handle successfully created";
?>
```

radius\_close
=============

Frees all ressources

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_close</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> )

It is not needed to call this function because php frees all resources
at the end of each request.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

radius\_config
==============

Causes the library to read the given configuration file

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_config</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">string</span> `$file`</span> )

Before issuing any Radius requests, the library must be made aware of
the servers it can contact. The easiest way to configure the library is
to call <span class="function">radius\_config</span>. <span
class="function">radius\_config</span> causes the library to read a
configuration file whose format is described in
<a href="http://www.freebsd.org/cgi/man.cgi?query=radius.conf" class="link external">» radius.conf</a>.

### 参数

`radius_handle`  

`file`  
The pathname of the configuration file is passed as the file argument to
<span class="function">radius\_config</span>. The library can also be
configured programmatically by calls to <span
class="function">radius\_add\_server</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">radius\_add\_server</span>

radius\_create\_request
=======================

Create accounting or authentication request

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_create\_request</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> )

A Radius request consists of a code specifying the kind of request, and
zero or more attributes which provide additional information. To begin
constructing a new request, call <span
class="function">radius\_create\_request</span>.

> **Note**: <span class="simpara"> Attention: You must call this
> function, before you can put any attribute! </span>

### 参数

`radius_handle`  

`type`  
Type is **`RADIUS_ACCESS_REQUEST`** or **`RADIUS_ACCOUNTING_REQUEST`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">radius\_create\_request</span>
example**

``` php
<?php
if (!radius_create_request($res, RADIUS_ACCESS_REQUEST)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### 参见

-   <span class="function">radius\_send\_request</span>

radius\_cvt\_addr
=================

Converts raw data to IP-Address

### 说明

<span class="type">string</span> <span
class="methodname">radius\_cvt\_addr</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 范例

**示例 \#1 <span class="function">radius\_cvt\_addr</span> example**

``` php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    
    switch ($attr) {

    case RADIUS_FRAMED_IP_ADDRESS:
        $ip = radius_cvt_addr($data);
        echo "IP: $ip<br>\n";
        break;

    case RADIUS_FRAMED_IP_NETMASK:
        $mask = radius_cvt_addr($data);
        echo "MASK: $mask<br>\n";
        break;
    }
}
?>
```

### 参见

-   <span class="function">radius\_cvt\_int</span>
-   <span class="function">radius\_cvt\_string</span>

radius\_cvt\_int
================

Converts raw data to integer

### 说明

<span class="type">int</span> <span
class="methodname">radius\_cvt\_int</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 范例

**示例 \#1 <span class="function">radius\_cvt\_int</span> example**

``` php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    
    switch ($attr) {

    case RADIUS_FRAMED_MTU:
        $mtu = radius_cvt_int($data);
        echo "MTU: $mtu<br>\n";
        break;
    }
}
?>
```

### 参见

-   <span class="function">radius\_cvt\_addr</span>
-   <span class="function">radius\_cvt\_string</span>

radius\_cvt\_string
===================

Converts raw data to string

### 说明

<span class="type">string</span> <span
class="methodname">radius\_cvt\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 范例

**示例 \#1 <span class="function">radius\_cvt\_string</span> example**

``` php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    
    switch ($attr) {

    case RADIUS_FILTER_ID:
        $id = radius_cvt_string($data);
        echo "Filter ID: $id<br>\n";
        break;
    }
}
?>
```

### 参见

-   <span class="function">radius\_cvt\_addr</span>
-   <span class="function">radius\_cvt\_int</span>

radius\_demangle\_mppe\_key
===========================

Derives mppe-keys from mangled data

### 说明

<span class="type">string</span> <span
class="methodname">radius\_demangle\_mppe\_key</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">string</span> `$mangled`</span> )

When using MPPE with MS-CHAPv2, the send- and recv-keys are mangled (see
<a href="http://www.faqs.org/rfcs/rfc2548" class="link external">» RFC 2548</a>),
however this function is useless, because I don't think that there is or
will be a PPTP-MPPE implementation in PHP.

### 返回值

Returns the demangled string, or **`FALSE`** on error.

radius\_demangle
================

Demangles data

### 说明

<span class="type">string</span> <span
class="methodname">radius\_demangle</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">string</span> `$mangled`</span> )

Some data (Passwords, MS-CHAPv1 MPPE-Keys) is mangled for security
reasons, and must be demangled before you can use them.

### 返回值

Returns the demangled string, or **`FALSE`** on error.

radius\_get\_attr
=================

Extracts an attribute

### 说明

<span class="type">mixed</span> <span
class="methodname">radius\_get\_attr</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> )

Like Radius requests, each response may contain zero or more attributes.
After a response has been received successfully by <span
class="function">radius\_send\_request</span>, its attributes can be
extracted one by one using <span
class="function">radius\_get\_attr</span>. Each time <span
class="function">radius\_get\_attr</span> is called, it gets the next
attribute from the current response.

### 返回值

Returns an associative array containing the attribute-type and the data,
or error number \<= 0.

### 范例

**示例 \#1 <span class="function">radius\_get\_attr</span> example**

``` php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    printf("Got Attr:%d %d Bytes %s\n", $attr, strlen($data), bin2hex($data));
}
?>
```

### 参见

-   <span class="function">radius\_put\_attr</span>
-   <span class="function">radius\_get\_vendor\_attr</span>
-   <span class="function">radius\_put\_vendor\_attr</span>
-   <span class="function">radius\_send\_request</span>

radius\_get\_tagged\_attr\_data
===============================

Extracts the data from a tagged attribute

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">radius\_get\_tagged\_attr\_data</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

If a tagged attribute has been returned from <span
class="function">radius\_get\_attr</span>, <span
class="function">radius\_get\_tagged\_attr\_data</span> will return the
data from the attribute.

### 参数

`data`  
The tagged attribute to be decoded.

### 返回值

Returns the data from the tagged attribute 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">radius\_get\_tagged\_attr\_data</span>
example**

``` php
<?php
while ($resa = radius_get_attr($res)) {
    if (!is_array($resa)) {
        printf ("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    $tag = radius_get_tagged_attr_tag($data);
    $value = radius_get_tagged_attr_data($data);

    printf("Got tagged attribute with tag %d and value %s\n", $tag, $value);
}
?>
```

### 参见

-   <span class="function">radius\_get\_attr</span>
-   <span class="function">radius\_get\_tagged\_attr\_tag</span>

radius\_get\_tagged\_attr\_tag
==============================

Extracts the tag from a tagged attribute

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">radius\_get\_tagged\_attr\_tag</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

If a tagged attribute has been returned from <span
class="function">radius\_get\_attr</span>, <span
class="function">radius\_get\_tagged\_attr\_data</span> will return the
tag from the attribute.

### 参数

`data`  
The tagged attribute to be decoded.

### 返回值

Returns the tag from the tagged attribute 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">radius\_get\_tagged\_attr\_tag</span>
example**

``` php
<?php
while ($resa = radius_get_attr($res)) {
    if (!is_array($resa)) {
        printf ("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];

    $tag = radius_get_tagged_attr_tag($data);
    $value = radius_get_tagged_attr_data($data);

    printf("Got tagged attribute with tag %d and value %s\n", $tag, $value);
}
?>
```

### 参见

-   <span class="function">radius\_get\_attr</span>
-   <span class="function">radius\_get\_tagged\_attr\_data</span>

radius\_get\_vendor\_attr
=========================

Extracts a vendor specific attribute

### 说明

<span class="type">array</span> <span
class="methodname">radius\_get\_vendor\_attr</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

If <span class="function">radius\_get\_attr</span> returns
**`RADIUS_VENDOR_SPECIFIC`**, <span
class="function">radius\_get\_vendor\_attr</span> may be called to
determine the vendor.

### 返回值

Returns an associative array containing the attribute-type, vendor and
the data, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">radius\_get\_vendor\_attr</span>
example**

``` php
<?php
while ($resa = radius_get_attr($res)) {

    if (!is_array($resa)) {
        printf ("Error getting attribute: %s\n",  radius_strerror($res));
        exit;
    }

    $attr = $resa['attr'];
    $data = $resa['data'];
    printf("Got Attr:%d %d Bytes %s\n", $attr, strlen($data), bin2hex($data));
    if ($attr == RADIUS_VENDOR_SPECIFIC) {

        $resv = radius_get_vendor_attr($data);
        if (is_array($resv)) {
            $vendor = $resv['vendor'];
            $attrv = $resv['attr'];
            $datav = $resv['data'];    
            printf("Got Vendor Attr:%d %d Bytes %s\n", $attrv, strlen($datav), bin2hex($datav));
        }
        
    }
}
?>
```

### 参见

-   <span class="function">radius\_get\_attr</span>
-   <span class="function">radius\_put\_vendor\_attr</span>

radius\_put\_addr
=================

Attaches an IP address attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_addr</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">string</span> `$addr`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches an IP address attribute to the current RADIUS request.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`type`  
The attribute type.

`addr`  
An IPv4 address in string form, such as *10.0.0.1*.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

radius\_put\_attr
=================

Attaches a binary attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_attr</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches a binary attribute to the current RADIUS request.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`type`  
The attribute type.

`value`  
The attribute value, which will be treated as a raw binary string.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">radius\_put\_attr</span> example**

``` php
<?php
mt_srand(time());
$chall = mt_rand();
$chapval = md5(pack('Ca*',1 , 'sepp' . $chall));
$pass = pack('CH*', 1, $chapval);
if (!radius_put_attr($res, RADIUS_CHAP_PASSWORD, $pass)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

### 参见

-   <span class="function">radius\_get\_attr</span>
-   <span class="function">radius\_get\_vendor\_attr</span>
-   <span class="function">radius\_put\_vendor\_attr</span>

radius\_put\_int
================

Attaches an integer attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_int</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">int</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches an integer attribute to the current RADIUS request.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`type`  
The attribute type.

`value`  
The attribute value.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

### 范例

**示例 \#1 <span class="function">radius\_put\_int</span> example**

``` php
<?php
if (!radius_put_int($res, RAD_FRAMED_PROTOCOL, RAD_PPP)) {
   echo 'RadiusError:' . radius_strerror($res). "\n<br />";
   exit;
}
?>
```

### 参见

-   <span class="function">radius\_put\_string</span>
-   <span class="function">radius\_put\_vendor\_int</span>
-   <span class="function">radius\_put\_vendor\_string</span>

radius\_put\_string
===================

Attaches a string attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_string</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches a string attribute to the current RADIUS request. In general,
<span class="function">radius\_put\_attr</span> is a more useful
function for attaching string attributes, as it is binary safe.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`type`  
The attribute type.

`value`  
The attribute value. This value is expected by the underlying library to
be null terminated, therefore this parameter is not binary safe.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

### 范例

**示例 \#1 <span class="function">radius\_put\_string</span> example**

``` php
<?php
if (!radius_put_string($res, RADIUS_USER_NAME, 'billy')) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### 参见

-   <span class="function">radius\_put\_int</span>
-   <span class="function">radius\_put\_vendor\_int</span>
-   <span class="function">radius\_put\_vendor\_string</span>

radius\_put\_vendor\_addr
=========================

Attaches a vendor specific IP address attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_vendor\_addr</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$vendor`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$addr`</span> )

Attaches an IP address vendor specific attribute to the current RADIUS
request.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`vendor`  
The vendor ID.

`type`  
The attribute type.

`addr`  
An IPv4 address in string form, such as *10.0.0.1*.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

radius\_put\_vendor\_attr
=========================

Attaches a vendor specific binary attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_vendor\_attr</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$vendor`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches a vendor specific binary attribute to the current RADIUS
request.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`vendor`  
The vendor ID.

`type`  
The attribute type.

`value`  
The attribute value, which will be treated as a raw binary string.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

### 范例

**示例 \#1 <span class="function">radius\_put\_vendor\_attr</span>
example**

``` php
<?php
if (!radius_put_vendor_attr($res, RADIUS_VENDOR_MICROSOFT, RAD_MICROSOFT_MS_CHAP_CHALLENGE, $challenge)) {
    echo 'RadiusError:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### 参见

-   <span class="function">radius\_get\_vendor\_attr</span>

radius\_put\_vendor\_int
========================

Attaches a vendor specific integer attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_vendor\_int</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$vendor`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">int</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches a vendor specific integer attribute to the current RADIUS
request.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`vendor`  
The vendor ID.

`type`  
The attribute type.

`value`  
The attribute value.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

### 参见

-   <span class="function">radius\_put\_vendor\_string</span>

radius\_put\_vendor\_string
===========================

Attaches a vendor specific string attribute

### 说明

<span class="type">bool</span> <span
class="methodname">radius\_put\_vendor\_string</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">int</span> `$vendor`</span> , <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$tag`</span> \]\] )

Attaches a vendor specific string attribute to the current RADIUS
request. In general, <span
class="function">radius\_put\_vendor\_attr</span> is a more useful
function for attaching string attributes, as it is binary safe.

> **Note**:
>
> A request must be created via <span
> class="function">radius\_create\_request</span> before this function
> can be called.

### 参数

`radius_handle`  
The RADIUS resource.

`vendor`  
The vendor ID.

`type`  
The attribute type.

`value`  
The attribute value. This value is expected by the underlying library to
be null terminated, therefore this parameter is not binary safe.

`options`  
A bitmask of the attribute options. The available options include
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
and
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_SALT</code></strong></a>.

`tag`  
The attribute tag. This parameter is ignored unless the
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_OPTION_TAGGED</code></strong></a>
option is set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本              | 说明                                           |
|-------------------|------------------------------------------------|
| PECL radius 1.3.0 | The `options` and `tag` parameters were added. |

### 参见

-   <span class="function">radius\_put\_vendor\_int</span>

radius\_request\_authenticator
==============================

Returns the request authenticator

### 说明

<span class="type">string</span> <span
class="methodname">radius\_request\_authenticator</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> )

The request authenticator is needed for demangling mangled data like
passwords and encryption-keys.

### 返回值

Returns the request authenticator as string, or **`FALSE`** on error.

### 参见

-   <span class="function">radius\_demangle</span>

radius\_salt\_encrypt\_attr
===========================

Salt-encrypts a value

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">radius\_salt\_encrypt\_attr</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> )

Applies the RADIUS salt-encryption algorithm to the given value.

In general, this is achieved automatically by providing the
**`RADIUS_OPTION_SALT`** option to an attribute setter function, but
this function can be used if low-level request construction is required.

### 参数

`data`  
The data to be salt-encrypted.

### 返回值

Returns the salt-encrypted data 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">radius\_put\_addr</span>
-   <span class="function">radius\_put\_attr</span>
-   <span class="function">radius\_put\_int</span>
-   <span class="function">radius\_put\_string</span>

radius\_send\_request
=====================

Sends the request and waits for a reply

### 说明

<span class="type">int</span> <span
class="methodname">radius\_send\_request</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> )

After the Radius request has been constructed, it is sent by <span
class="function">radius\_send\_request</span>.

The <span class="function">radius\_send\_request</span> function sends
the request and waits for a valid reply, retrying the defined servers in
round-robin fashion as necessary.

### 返回值

If a valid response is received, <span
class="function">radius\_send\_request</span> returns the Radius code
which specifies the type of the response. This will typically be
**`RADIUS_ACCESS_ACCEPT`**, **`RADIUS_ACCESS_REJECT`**, or
**`RADIUS_ACCESS_CHALLENGE`**. If no valid response is received, <span
class="function">radius\_send\_request</span> returns **`FALSE`**.

### 参见

-   <span class="function">radius\_create\_request</span>

radius\_server\_secret
======================

Returns the shared secret

### 说明

<span class="type">string</span> <span
class="methodname">radius\_server\_secret</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> )

The shared secret is needed as salt for demangling mangled data like
passwords and encryption-keys.

### 返回值

Returns the server's shared secret as string, or **`FALSE`** on error.

radius\_strerror
================

Returns an error message

### 说明

<span class="type">string</span> <span
class="methodname">radius\_strerror</span> ( <span
class="methodparam"><span class="type">resource</span>
`$radius_handle`</span> )

If Radius-functions fail then they record an error message. This error
message can be retrieved with this function.

### 返回值

Returns error messages as string from failed radius functions.

**目录**

-   [radius\_acct\_open](/ref/radius.html#radius_acct_open) — Creates a
    Radius handle for accounting
-   [radius\_add\_server](/ref/radius.html#radius_add_server) — Adds a
    server
-   [radius\_auth\_open](/ref/radius.html#radius_auth_open) — Creates a
    Radius handle for authentication
-   [radius\_close](/ref/radius.html#radius_close) — Frees all
    ressources
-   [radius\_config](/ref/radius.html#radius_config) — Causes the
    library to read the given configuration file
-   [radius\_create\_request](/ref/radius.html#radius_create_request) —
    Create accounting or authentication request
-   [radius\_cvt\_addr](/ref/radius.html#radius_cvt_addr) — Converts raw
    data to IP-Address
-   [radius\_cvt\_int](/ref/radius.html#radius_cvt_int) — Converts raw
    data to integer
-   [radius\_cvt\_string](/ref/radius.html#radius_cvt_string) — Converts
    raw data to string
-   [radius\_demangle\_mppe\_key](/ref/radius.html#radius_demangle_mppe_key)
    — Derives mppe-keys from mangled data
-   [radius\_demangle](/ref/radius.html#radius_demangle) — Demangles
    data
-   [radius\_get\_attr](/ref/radius.html#radius_get_attr) — Extracts an
    attribute
-   [radius\_get\_tagged\_attr\_data](/ref/radius.html#radius_get_tagged_attr_data)
    — Extracts the data from a tagged attribute
-   [radius\_get\_tagged\_attr\_tag](/ref/radius.html#radius_get_tagged_attr_tag)
    — Extracts the tag from a tagged attribute
-   [radius\_get\_vendor\_attr](/ref/radius.html#radius_get_vendor_attr)
    — Extracts a vendor specific attribute
-   [radius\_put\_addr](/ref/radius.html#radius_put_addr) — Attaches an
    IP address attribute
-   [radius\_put\_attr](/ref/radius.html#radius_put_attr) — Attaches a
    binary attribute
-   [radius\_put\_int](/ref/radius.html#radius_put_int) — Attaches an
    integer attribute
-   [radius\_put\_string](/ref/radius.html#radius_put_string) — Attaches
    a string attribute
-   [radius\_put\_vendor\_addr](/ref/radius.html#radius_put_vendor_addr)
    — Attaches a vendor specific IP address attribute
-   [radius\_put\_vendor\_attr](/ref/radius.html#radius_put_vendor_attr)
    — Attaches a vendor specific binary attribute
-   [radius\_put\_vendor\_int](/ref/radius.html#radius_put_vendor_int) —
    Attaches a vendor specific integer attribute
-   [radius\_put\_vendor\_string](/ref/radius.html#radius_put_vendor_string)
    — Attaches a vendor specific string attribute
-   [radius\_request\_authenticator](/ref/radius.html#radius_request_authenticator)
    — Returns the request authenticator
-   [radius\_salt\_encrypt\_attr](/ref/radius.html#radius_salt_encrypt_attr)
    — Salt-encrypts a value
-   [radius\_send\_request](/ref/radius.html#radius_send_request) —
    Sends the request and waits for a reply
-   [radius\_server\_secret](/ref/radius.html#radius_server_secret) —
    Returns the shared secret
-   [radius\_strerror](/ref/radius.html#radius_strerror) — Returns an
    error message
