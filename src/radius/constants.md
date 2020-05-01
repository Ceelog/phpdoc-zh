预定义常量
==========

**目录**

-   [RADIUS Options](/radius/constants.html#RADIUS%20Options)
-   [RADIUS Packet
    Types](/radius/constants.html#RADIUS%20Packet%20Types)
-   [RADIUS Attribute
    Types](/radius/constants.html#RADIUS%20Attribute%20Types)
-   [RADIUS Vendor Specific Attribute
    Types](/radius/constants.html#RADIUS%20Vendor%20Specific%20Attribute%20Types)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`RADIUS_MPPE_KEY_LEN`** (<span class="type">integer</span>)  
<span class="simpara"> The maximum length of MPPE keys. </span>

RADIUS Options
--------------

Several RADIUS functions accept option flags as bitmasks. The constants
representing those flags are listed below.

**`RADIUS_OPTION_SALT`** (<span class="type">integer</span>)  
When set, this option will result in the attribute value being
salt-encrypted.

**`RADIUS_OPTION_TAGGED`** (<span class="type">integer</span>)  
When set, this option will result in the attribute value being tagged
with the value of the tag parameter.

RADIUS Packet Types
-------------------

RADIUS packets, whether requests or responses, always include a type.
These constants are provided to make it easier to specify types when
using <span class="function">radius\_create\_request</span> and when
comparing the result of <span
class="function">radius\_send\_request</span>.

**`RADIUS_ACCESS_REQUEST`** (<span class="type">integer</span>)  
An Access-Request, used to authenticate a user against a RADIUS server.
Access request packets must include a
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_NAS_IP_ADDRESS</code></strong></a>
or a
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_NAS_IDENTIFIER</code></strong></a>
attribute, must also include a
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_USER_PASSWORD</code></strong></a>,
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_CHAP_PASSWORD</code></strong></a>
or a
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_STATE</code></strong></a>
attribute, and should include a
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_USER_NAME</code></strong></a>
attribute.

**`RADIUS_ACCESS_ACCEPT`** (<span class="type">integer</span>)  
An Access-Accept response to an Access-Request indicating that the
RADIUS server authenticated the user successfully.

**`RADIUS_ACCESS_REJECT`** (<span class="type">integer</span>)  
An Access-Reject response to an Access-Request indicating that the
RADIUS server could not authenticate the user.

**`RADIUS_ACCESS_CHALLENGE`** (<span class="type">integer</span>)  
An Access-Challenge response to an Access-Request indicating that the
RADIUS server requires further information in another Access-Request
before authenticating the user.

**`RADIUS_ACCOUNTING_REQUEST`** (<span class="type">integer</span>)  
An Accounting-Request, used to convey accounting information for a
service to the RADIUS server.

**`RADIUS_ACCOUNTING_RESPONSE`** (<span class="type">integer</span>)  
An Accounting-Response response to an Accounting-Request.

**`RADIUS_COA_REQUEST`** (<span class="type">integer</span>)  
A CoA-Request, sent from the RADIUS server to indicate that the
authorisations within the user session have changed. A response must be
sent in the form of a CoA-ACK or a CoA-NAK.

This constant is available in PECL radius 1.3.0 and later.

**`RADIUS_COA_ACK`** (<span class="type">integer</span>)  
A CoA-ACK, sent to the RADIUS server to indicate that the user
authorisations have been updated.

This constant is available in PECL radius 1.3.0 and later.

**`RADIUS_COA_NAK`** (<span class="type">integer</span>)  
A CoA-NAK, sent to the RADIUS server to indicate that the user
authorisations could not be updated.

This constant is available in PECL radius 1.3.0 and later.

**`RADIUS_DISCONNECT_REQUEST`** (<span class="type">integer</span>)  
A Disconnect-Request, sent from the RADIUS server to indicate that the
user session must be terminated.

This constant is available in PECL radius 1.3.0 and later.

**`RADIUS_DISCONNECT_ACK`** (<span class="type">integer</span>)  
A Disconnect-ACK, sent to the RADIUS server to indicate that the user
session has been terminated.

This constant is available in PECL radius 1.3.0 and later.

**`RADIUS_DISCONNECT_NAK`** (<span class="type">integer</span>)  
A Disconnect-NAK, sent to the RADIUS server to indicate that the user
session could not be terminated.

This constant is available in PECL radius 1.3.0 and later.

RADIUS Attribute Types
----------------------

These constants define RADIUS attribute types that can be used with
<span class="function">radius\_put\_addr</span>, <span
class="function">radius\_put\_attr</span>, <span
class="function">radius\_put\_int</span> and <span
class="function">radius\_put\_string</span>.

**`RADIUS_USER_NAME`** (<span class="type">integer</span>)  
The User-Name attribute. The attribute value is expected to be a <span
class="type">string</span> containing the name of the user being
authenticated, and can be set using <span
class="function">radius\_put\_attr</span>.

**`RADIUS_USER_PASSWORD`** (<span class="type">integer</span>)  
The User-Password attribute. The attribute value is expected to be a
<span class="type">string</span> containing the user's password, and can
be set using <span class="function">radius\_put\_attr</span>. This value
will be obfuscated on transmission as described in
<a href="http://www.faqs.org/rfcs/rfc2865" class="link external">» section 5.2 of RFC 2865</a>.

**`RADIUS_CHAP_PASSWORD`** (<span class="type">integer</span>)  
The Chap-Password attribute. The attribute value is expected to be a
<span class="type">string</span> with the first byte containing the CHAP
identifier, and the subsequent 16 bytes containing the MD5 hash of the
CHAP identifier, the plaintext password and the CHAP challenge value
concatenated together. Note that the CHAP challenge value should also be
sent separately in a
<a href="/radius/constants.html#" class="link"><strong><code>RADIUS_CHAP_CHALLENGE</code></strong></a>
attribute.

**示例 \#1 Using CHAP passwords**

``` php
<?php
// Firstly, we'll create an authentication handle and request.
$radh = radius_auth_open();
radius_add_server($radh, $server, $port, $secret, 3, 3);
radius_create_request($radh, RADIUS_ACCESS_REQUEST);

// Assuming $password contains the plaintext password, we now:

// Generate a challenge.
$challenge = mt_rand();

// Specify a CHAP identifier.
$ident = 1;

// Add the Chap-Password attribute.
$cp = md5(pack('Ca*', $ident, $password.$challenge), true);
radius_put_attr($radh, RADIUS_CHAP_PASSWORD, pack('C', $ident).$cp);

// Add the Chap-Challenge attribute.
radius_put_attr($radh, RADIUS_CHAP_CHALLENGE, $challenge);

/* From here, you would add the remaining attributes and
 * call radius_send_request(). */
?>
```

**`RADIUS_NAS_IP_ADDRESS`** (<span class="type">integer</span>)  
The NAS-IP-Address attribute. The attribute value is expected to the IP
address of the RADIUS client encoded as an <span
class="type">integer</span>, which can be set using <span
class="function">radius\_put\_addr</span>.

**`RADIUS_NAS_PORT`** (<span class="type">integer</span>)  
The NAS-Port attribute. The attribute value is expected to be the
physical port of the user on the RADIUS client encoded as an <span
class="type">integer</span>, which can be set using <span
class="function">radius\_put\_int</span>.

**`RADIUS_SERVICE_TYPE`** (<span class="type">integer</span>)  
The Service-Type attribute. The attribute value indicates the service
type the user is requesting, and is expected to be an <span
class="type">integer</span>, which can be set using <span
class="function">radius\_put\_int</span>.

A number of constants are provided to represent the possible values of
this attribute. They include:

-   **`RADIUS_LOGIN`**
-   **`RADIUS_FRAMED`**
-   **`RADIUS_CALLBACK_LOGIN`**
-   **`RADIUS_CALLBACK_FRAMED`**
-   **`RADIUS_OUTBOUND`**
-   **`RADIUS_ADMINISTRATIVE`**
-   **`RADIUS_NAS_PROMPT`**
-   **`RADIUS_AUTHENTICATE_ONLY`**
-   **`RADIUS_CALLBACK_NAS_PROMPT`**

**`RADIUS_FRAMED_PROTOCOL`** (<span class="type">integer</span>)  
The Framed-Protocol attribute. The attribute value is expected to be an
<span class="type">integer</span> indicating the framing to be used for
framed access, and can be set using <span
class="function">radius\_put\_int</span>. The possible attribute values
include these constants:

-   **`RADIUS_PPP`**
-   **`RADIUS_SLIP`**
-   **`RADIUS_ARAP`**
-   **`RADIUS_GANDALF`**
-   **`RADIUS_XYLOGICS`**

**`RADIUS_FRAMED_IP_ADDRESS`** (<span class="type">integer</span>)  
The Framed-IP-Address attribute. The attribute value is expected to be
the address of the user's network encoded as an <span
class="type">integer</span>, which can be set using <span
class="function">radius\_put\_addr</span> and retrieved using <span
class="function">radius\_cvt\_addr</span>.

**`RADIUS_FRAMED_IP_NETMASK`** (<span class="type">integer</span>)  
The Framed-IP-Netmask attribute. The attribute value is expected to be
the netmask of the user's network encoded as an <span
class="type">integer</span>, which can be set using <span
class="function">radius\_put\_addr</span> and retrieved using <span
class="function">radius\_cvt\_addr</span>.

**`RADIUS_FRAMED_ROUTING`** (<span class="type">integer</span>)  
The Framed-Routing attribute. The attribute value is expected to be an
<span class="type">integer</span> indicating the routing method for the
user, which can be set using <span
class="function">radius\_put\_int</span>.

Possible values include:

-   *0*: No routing
-   *1*: Send routing packets
-   *2*: Listen for routing packets
-   *3*: Send and listen

**`RADIUS_FILTER_ID`** (<span class="type">integer</span>)  
The Filter-ID attribute. The attribute value is expected to be an
implementation-specific, human-readable <span class="type">string</span>
of filters, which can be set using <span
class="function">radius\_put\_attr</span>.

**`RADIUS_FRAMED_MTU`** (<span class="type">integer</span>)  
The Framed-MTU attribute. The attribute value is expected to be an <span
class="type">integer</span> indicating the MTU to be configured for the
user, and can be set using <span
class="function">radius\_put\_int</span>.

**`RADIUS_FRAMED_COMPRESSION`** (<span class="type">integer</span>)  
The Framed-Compression attribute. The attribute value is expected to be
an <span class="type">integer</span> indicating the compression protocol
to be used, and can be set using <span
class="function">radius\_put\_int</span>. Possible values include these
constants:

-   **`RADIUS_COMP_NONE`**: No compression
-   **`RADIUS_COMP_VJ`**: VJ TCP/IP header compression
-   **`RADIUS_COMP_IPXHDR`**: IPX header compression
-   **`RADIUS_COMP_STAC_LZS`**: Stac-LZS compression (added in PECL
    radius 1.3.0b2)

**`RADIUS_LOGIN_IP_HOST`** (<span class="type">integer</span>)  
The Login-IP-Host attribute. The attribute value is expected to the IP
address to connect the user to, encoded as an <span
class="type">integer</span>, which can be set using <span
class="function">radius\_put\_addr</span>.

**`RADIUS_LOGIN_SERVICE`** (<span class="type">integer</span>)  
The Login-Service attribute. The attribute value is an <span
class="type">integer</span> indicating the service to connect the user
to on the login host. The value can be converted to a PHP integer via
<span class="function">radius\_cvt\_int</span>.

**`RADIUS_LOGIN_TCP_PORT`** (<span class="type">integer</span>)  
The Login-TCP-Port attribute. The attribute value is an <span
class="type">integer</span> indicating the port to connect the user to
on the login host. The value can be converted to a PHP integer via <span
class="function">radius\_cvt\_int</span>.

**`RADIUS_REPLY_MESSAGE`** (<span class="type">integer</span>)  
The Reply-Message attribute. The attribute value is a <span
class="type">string</span> containing text that may be displayed to the
user in response to an access request.

**`RADIUS_CALLBACK_NUMBER`** (<span class="type">integer</span>)  
The Callback-Number attribute. The attribute value is a <span
class="type">string</span> containing the dialing string to use for
callback.

**`RADIUS_CALLBACK_ID`** (<span class="type">integer</span>)  
The Callback-Id attribute. The attribute value is a <span
class="type">string</span> containing an implementation-specific name of
the place to be called.

**`RADIUS_FRAMED_ROUTE`** (<span class="type">integer</span>)  
The Framed-Route attribute. The attribute value is a <span
class="type">string</span> containing an implementation-specific set of
routes to be configured for the user.

**`RADIUS_FRAMED_IPX_NETWORK`** (<span class="type">integer</span>)  
The Framed-IPX-Network attribute. The attribute value is an <span
class="type">integer</span> containing the IPX network to be configured
for the user, or *0xFFFFFFFE* to indicate that the RADIUS client should
select the network, and can be accessed via <span
class="function">radius\_cvt\_int</span>.

**`RADIUS_STATE`** (<span class="type">integer</span>)  
The State attribute. The attribute value is an implementation-defined
<span class="type">string</span> included in an Access-Challenge from a
server that must be included in the subsequent Access-Request, and can
be set using <span class="function">radius\_put\_attr</span>.

**`RADIUS_CLASS`** (<span class="type">integer</span>)  
The Class attribute. The attribute value is an arbitrary <span
class="type">string</span> included in an Access-Accept message that
should then be sent to the accounting server in Accounting-Request
messages, and can be set using <span
class="function">radius\_put\_attr</span>.

**`RADIUS_VENDOR_SPECIFIC`** (<span class="type">integer</span>)  
The Vendor-Specific attribute. In general, vendor attribute values
should be set using <span
class="function">radius\_put\_vendor\_addr</span>, <span
class="function">radius\_put\_vendor\_attr</span>, <span
class="function">radius\_put\_vendor\_int</span> and <span
class="function">radius\_put\_vendor\_string</span>, rather than
directly.

This constant is mostly useful when interpreting vendor specific
attributes in responses from a RADIUS server; when a vendor specific
attribute is received, the <span
class="function">radius\_get\_vendor\_attr</span> function should be
used to access the vendor ID, attribute type and attribute value.

**`RADIUS_SESSION_TIMEOUT`** (<span class="type">integer</span>)  
Session timeout

**`RADIUS_IDLE_TIMEOUT`** (<span class="type">integer</span>)  
Idle timeout

**`RADIUS_TERMINATION_ACTION`** (<span class="type">integer</span>)  
Termination action

**`RADIUS_CALLED_STATION_ID`** (<span class="type">integer</span>)  
Called Station Id

**`RADIUS_CALLING_STATION_ID`** (<span class="type">integer</span>)  
Calling Station Id

**`RADIUS_NAS_IDENTIFIER`** (<span class="type">integer</span>)  
NAS ID

**`RADIUS_PROXY_STATE`** (<span class="type">integer</span>)  
Proxy State

**`RADIUS_LOGIN_LAT_SERVICE`** (<span class="type">integer</span>)  
Login LAT Service

**`RADIUS_LOGIN_LAT_NODE`** (<span class="type">integer</span>)  
Login LAT Node

**`RADIUS_LOGIN_LAT_GROUP`** (<span class="type">integer</span>)  
Login LAT Group

**`RADIUS_FRAMED_APPLETALK_LINK`** (<span class="type">integer</span>)  
Framed Appletalk Link

**`RADIUS_FRAMED_APPLETALK_NETWORK`** (<span class="type">integer</span>)  
Framed Appletalk Network

**`RADIUS_FRAMED_APPLETALK_ZONE`** (<span class="type">integer</span>)  
Framed Appletalk Zone

**`RADIUS_CHAP_CHALLENGE`** (<span class="type">integer</span>)  
Challenge

**`RADIUS_NAS_PORT_TYPE`** (<span class="type">integer</span>)  
NAS port type, one of:

-   **`RADIUS_ASYNC`**
-   **`RADIUS_SYNC`**
-   **`RADIUS_ISDN_SYNC`**
-   **`RADIUS_ISDN_ASYNC_V120`**
-   **`RADIUS_ISDN_ASYNC_V110`**
-   **`RADIUS_VIRTUAL`**
-   **`RADIUS_PIAFS`**
-   **`RADIUS_HDLC_CLEAR_CHANNEL`**
-   **`RADIUS_X_25`**
-   **`RADIUS_X_75`**
-   **`RADIUS_G_3_FAX`**
-   **`RADIUS_SDSL`**
-   **`RADIUS_ADSL_CAP`**
-   **`RADIUS_ADSL_DMT`**
-   **`RADIUS_IDSL`**
-   **`RADIUS_ETHERNET`**
-   **`RADIUS_XDSL`**
-   **`RADIUS_CABLE`**
-   **`RADIUS_WIRELESS_OTHER`**
-   **`RADIUS_WIRELESS_IEEE_802_11`**

**`RADIUS_PORT_LIMIT`** (<span class="type">integer</span>)  
Port Limit

**`RADIUS_LOGIN_LAT_PORT`** (<span class="type">integer</span>)  
Login LAT Port

**`RADIUS_CONNECT_INFO`** (<span class="type">integer</span>)  
Connect info

**`RADIUS_ACCT_STATUS_TYPE`** (<span class="type">integer</span>)  
Accounting status type, one of:

-   **`RADIUS_START`**
-   **`RADIUS_STOP`**
-   **`RADIUS_ACCOUNTING_ON`**
-   **`RADIUS_ACCOUNTING_OFF`**

**`RADIUS_ACCT_DELAY_TIME`** (<span class="type">integer</span>)  
Accounting delay time

**`RADIUS_ACCT_INPUT_OCTETS`** (<span class="type">integer</span>)  
Accounting input bytes

**`RADIUS_ACCT_OUTPUT_OCTETS`** (<span class="type">integer</span>)  
Accounting output bytes

**`RADIUS_ACCT_SESSION_ID`** (<span class="type">integer</span>)  
Accounting session ID

**`RADIUS_ACCT_AUTHENTIC`** (<span class="type">integer</span>)  
Accounting authentic, one of:

-   **`RADIUS_AUTH_RADIUS`**
-   **`RADIUS_AUTH_LOCAL`**
-   **`RADIUS_AUTH_REMOTE`**

**`RADIUS_ACCT_SESSION_TIME`** (<span class="type">integer</span>)  
Accounting session time

**`RADIUS_ACCT_INPUT_PACKETS`** (<span class="type">integer</span>)  
Accounting input packets

**`RADIUS_ACCT_OUTPUT_PACKETS`** (<span class="type">integer</span>)  
Accounting output packets

**`RADIUS_ACCT_TERMINATE_CAUSE`** (<span class="type">integer</span>)  
Accounting terminate cause, one of:

-   **`RADIUS_TERM_USER_REQUEST`**
-   **`RADIUS_TERM_LOST_CARRIER`**
-   **`RADIUS_TERM_LOST_SERVICE`**
-   **`RADIUS_TERM_IDLE_TIMEOUT`**
-   **`RADIUS_TERM_SESSION_TIMEOUT`**
-   **`RADIUS_TERM_ADMIN_RESET`**
-   **`RADIUS_TERM_ADMIN_REBOOT`**
-   **`RADIUS_TERM_PORT_ERROR`**
-   **`RADIUS_TERM_NAS_ERROR`**
-   **`RADIUS_TERM_NAS_REQUEST`**
-   **`RADIUS_TERM_NAS_REBOOT`**
-   **`RADIUS_TERM_PORT_UNNEEDED`**
-   **`RADIUS_TERM_PORT_PREEMPTED`**
-   **`RADIUS_TERM_PORT_SUSPENDED`**
-   **`RADIUS_TERM_SERVICE_UNAVAILABLE`**
-   **`RADIUS_TERM_CALLBACK`**
-   **`RADIUS_TERM_USER_ERROR`**
-   **`RADIUS_TERM_HOST_REQUEST`**

**`RADIUS_ACCT_MULTI_SESSION_ID`** (<span class="type">integer</span>)  
Accounting multi session ID

**`RADIUS_ACCT_LINK_COUNT`** (<span class="type">integer</span>)  
Accounting link count

RADIUS Vendor Specific Attribute Types
--------------------------------------

**`RADIUS_VENDOR_MICROSOFT`** (<span class="type">integer</span>)  
Microsoft specific vendor attributes
(<a href="http://www.faqs.org/rfcs/rfc2548" class="link external">» RFC 2548</a>),
one of:

-   **`RADIUS_MICROSOFT_MS_CHAP_RESPONSE`**
-   **`RADIUS_MICROSOFT_MS_CHAP_ERROR`**
-   **`RADIUS_MICROSOFT_MS_CHAP_PW_1`**
-   **`RADIUS_MICROSOFT_MS_CHAP_PW_2`**
-   **`RADIUS_MICROSOFT_MS_CHAP_LM_ENC_PW`**
-   **`RADIUS_MICROSOFT_MS_CHAP_NT_ENC_PW`**
-   **`RADIUS_MICROSOFT_MS_MPPE_ENCRYPTION_POLICY`**
-   **`RADIUS_MICROSOFT_MS_MPPE_ENCRYPTION_TYPES`**
-   **`RADIUS_MICROSOFT_MS_RAS_VENDOR`**
-   **`RADIUS_MICROSOFT_MS_CHAP_DOMAIN`**
-   **`RADIUS_MICROSOFT_MS_CHAP_CHALLENGE`**
-   **`RADIUS_MICROSOFT_MS_CHAP_MPPE_KEYS`**
-   **`RADIUS_MICROSOFT_MS_BAP_USAGE`**
-   **`RADIUS_MICROSOFT_MS_LINK_UTILIZATION_THRESHOLD`**
-   **`RADIUS_MICROSOFT_MS_LINK_DROP_TIME_LIMIT`**
-   **`RADIUS_MICROSOFT_MS_MPPE_SEND_KEY`**
-   **`RADIUS_MICROSOFT_MS_MPPE_RECV_KEY`**
-   **`RADIUS_MICROSOFT_MS_RAS_VERSION`**
-   **`RADIUS_MICROSOFT_MS_OLD_ARAP_PASSWORD`**
-   **`RADIUS_MICROSOFT_MS_NEW_ARAP_PASSWORD`**
-   **`RADIUS_MICROSOFT_MS_ARAP_PASSWORD_CHANGE_REASON`**
-   **`RADIUS_MICROSOFT_MS_FILTER`**
-   **`RADIUS_MICROSOFT_MS_ACCT_AUTH_TYPE`**
-   **`RADIUS_MICROSOFT_MS_ACCT_EAP_TYPE`**
-   **`RADIUS_MICROSOFT_MS_CHAP2_RESPONSE`**
-   **`RADIUS_MICROSOFT_MS_CHAP2_SUCCESS`**
-   **`RADIUS_MICROSOFT_MS_CHAP2_PW`**
-   **`RADIUS_MICROSOFT_MS_PRIMARY_DNS_SERVER`**
-   **`RADIUS_MICROSOFT_MS_SECONDARY_DNS_SERVER`**
-   **`RADIUS_MICROSOFT_MS_PRIMARY_NBNS_SERVER`**
-   **`RADIUS_MICROSOFT_MS_SECONDARY_NBNS_SERVER`**
-   **`RADIUS_MICROSOFT_MS_ARAP_CHALLENGE`**
