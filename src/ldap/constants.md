预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`LDAP_DEREF_NEVER`** (<span class="type">integer</span>)  
<span class="simpara"> Alias dereferencing rule - Never. </span>

**`LDAP_DEREF_SEARCHING`** (<span class="type">integer</span>)  
<span class="simpara"> Alias dereferencing rule - Searching. </span>

**`LDAP_DEREF_FINDING`** (<span class="type">integer</span>)  
<span class="simpara"> Alias dereferencing rule - Finding. </span>

**`LDAP_DEREF_ALWAYS`** (<span class="type">integer</span>)  
<span class="simpara"> Alias dereferencing rule - Always. </span>

**`LDAP_OPT_DEREF`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies alternative rules for following aliases
at the server. </span>

**`LDAP_OPT_SIZELIMIT`** (<span class="type">integer</span>)  
Specifies the maximum number of entries that can be returned on a search
operation.

> **Note**: <span class="simpara"> The actual size limit for operations
> is also bounded by the server's configured maximum number of return
> entries. The lesser of these two settings is the actual size limit.
> </span>

**`LDAP_OPT_TIMELIMIT`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the number of seconds to wait for
search results. </span>

> **Note**: <span class="simpara"> The actual time limit for operations
> is also bounded by the server's configured maximum time. The lesser of
> these two settings is the actual time limit. </span>

**`LDAP_OPT_NETWORK_TIMEOUT`** (<span class="type">integer</span>)  
<span class="simpara"> Option for <span
class="function">ldap\_set\_option</span> to allow setting network
timeout. (Available as of PHP 5.3.0) </span>

**`LDAP_OPT_PROTOCOL_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the LDAP protocol to be used (V2 or
V3). </span>

**`LDAP_OPT_ERROR_NUMBER`** (<span class="type">integer</span>)  
<span class="simpara"> Latest session error number. </span>

**`LDAP_OPT_REFERRALS`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies whether to automatically follow
referrals returned by the LDAP server. </span>

**`LDAP_OPT_RESTART`** (<span class="type">integer</span>)  
<span class="simpara"> Determines whether or not the connection should
be implicitly restarted. </span>

**`LDAP_OPT_HOST_NAME`** (<span class="type">integer</span>)  
<span class="simpara"> Sets/gets a space-separated of hosts when trying
to connect. </span>

**`LDAP_OPT_ERROR_STRING`** (<span class="type">integer</span>)  
<span class="simpara"> Alias of **`LDAP_OPT_DIAGNOSTIC_MESSAGE`**.
</span>

**`LDAP_OPT_DIAGNOSTIC_MESSAGE`** (<span class="type">integer</span>)  
<span class="simpara"> Gets the latest session error message. </span>

**`LDAP_OPT_MATCHED_DN`** (<span class="type">integer</span>)  
<span class="simpara"> Sets/gets the matched DN associated with the
connection. </span>

**`LDAP_OPT_SERVER_CONTROLS`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies a default list of server controls to be
sent with each request. </span>

**`LDAP_OPT_CLIENT_CONTROLS`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies a default list of client controls to be
processed with each request. </span>

**`LDAP_OPT_DEBUG_LEVEL`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies a bitwise level for debug traces.
</span>

**`LDAP_OPT_X_KEEPALIVE_IDLE`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the number of seconds a connection
needs to remain idle before TCP starts sending keepalive probes. </span>

**`LDAP_OPT_X_KEEPALIVE_PROBES`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the maximum number of keepalive probes
TCP should send before dropping the connection. </span>

**`LDAP_OPT_X_KEEPALIVE_INTERVAL`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the interval in seconds between
individual keepalive probes. </span>

**`LDAP_OPT_X_TLS_CACERTDIR`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the path of the directory containing CA
certificates. </span>

**`LDAP_OPT_X_TLS_CACERTFILE`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the full-path of the CA certificate
file. </span>

**`LDAP_OPT_X_TLS_CERTFILE`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the full-path of the certificate file.
</span>

**`LDAP_OPT_X_TLS_CIPHER_SUITE`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the allowed cipher suite. </span>

**`LDAP_OPT_X_TLS_CRLCHECK`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the CRL evaluation strategy. This must
be one of: **`LDAP_OPT_X_TLS_CRL_NONE`**,**`LDAP_OPT_X_TLS_CRL_PEER`**,
**`LDAP_OPT_X_TLS_CRL_ALL`**. </span>

> **Note**: <span class="simpara"> This option is only valid for
> OpenSSL. </span>

**`LDAP_OPT_X_TLS_CRLFILE`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the full-path of the CRL file. </span>

> **Note**: <span class="simpara"> This option is only valid for GnuTLS.
> </span>

**`LDAP_OPT_X_TLS_DHFILE`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the full-path of the file containing
the parameters for Diffie-Hellman ephemeral key exchange. </span>

> **Note**: <span class="simpara"> This option is ignored by GnuTLS and
> Mozilla NSS. </span>

**`LDAP_OPT_X_TLS_KEYFILE`** (<span class="type">string</span>)  
<span class="simpara"> Specifies the full-path of the certificate key
file. </span>

**`LDAP_OPT_X_TLS_PROTOCOL_MIN`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the minimum protocol version. This can
be one of:
**`LDAP_OPT_X_TLS_PROTOCOL_SSL2`**,**`LDAP_OPT_X_TLS_PROTOCOL_SSL3`**,
**`LDAP_OPT_X_TLS_PROTOCOL_TLS1_0`**,
**`LDAP_OPT_X_TLS_PROTOCOL_TLS1_1`**,
**`LDAP_OPT_X_TLS_PROTOCOL_TLS1_2`** </span>

**`LDAP_OPT_X_TLS_RANDOM_FILE`** (<span class="type">string</span>)  
<span class="simpara"> Sets/gets the random file when one of the system
default ones are not available. </span>

**`LDAP_OPT_X_TLS_REQUIRE_CERT`** (<span class="type">integer</span>)  
<span class="simpara"> Specifies the certificate checking checking
strategy. This must be one of:
**`LDAP_OPT_X_TLS_NEVER`**,**`LDAP_OPT_X_TLS_HARD`**,
**`LDAP_OPT_X_TLS_DEMAND`**, **`LDAP_OPT_X_TLS_ALLOW`**,
**`LDAP_OPT_X_TLS_TRY`**. (Available as of PHP 7.0.0) </span>

**`GSLC_SSL_NO_AUTH`** (<span class="type">integer</span>)  
<span class="simpara"> SSL Authentication Mode - No authentication
required. (Only for Oracle LDAP) </span>

**`GSLC_SSL_ONEWAY_AUTH`** (<span class="type">integer</span>)  
<span class="simpara"> SSL Authentication Mode - Only server
authentication required. (Only for Oracle LDAP) </span>

**`GSLC_SSL_TWOWAY_AUTH`** (<span class="type">integer</span>)  
<span class="simpara"> SSL Authentication Mode - Both server and client
authentication required. (Only for Oracle LDAP) </span>

**`LDAP_EXOP_START_TLS`** (<span class="type">string</span>)  
<span class="simpara"> Extended Operation constant - Start TLS
(<a href="http://www.faqs.org/rfcs/rfc4511" class="link external">» RFC 4511</a>).
</span>

**`LDAP_EXOP_MODIFY_PASSWD`** (<span class="type">string</span>)  
<span class="simpara"> Extended Operation constant - Modify password
(<a href="http://www.faqs.org/rfcs/rfc3062" class="link external">» RFC 3062</a>).
</span>

**`LDAP_EXOP_REFRESH`** (<span class="type">string</span>)  
<span class="simpara"> Extended Operation Constant - Refresh
(<a href="http://www.faqs.org/rfcs/rfc2589" class="link external">» RFC 2589</a>).
</span>

**`LDAP_EXOP_WHO_AM_I`** (<span class="type">string</span>)  
<span class="simpara"> Extended Operation Constant - WHOAMI
(<a href="http://www.faqs.org/rfcs/rfc4532" class="link external">» RFC 4532</a>).
</span>

**`LDAP_EXOP_TURN`** (<span class="type">string</span>)  
<span class="simpara"> Extended Operation Constant - Turn
(<a href="http://www.faqs.org/rfcs/rfc4531" class="link external">» RFC 4531</a>).
</span>

**`LDAP_CONTROL_MANAGEDSAIT`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Manage DSA IT
(<a href="http://www.faqs.org/rfcs/rfc3296" class="link external">» RFC 3296</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_PROXY_AUTHZ`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Proxied Authorization
(<a href="http://www.faqs.org/rfcs/rfc4730" class="link external">» RFC 4370</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_SUBENTRIES`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Subentries
(<a href="http://www.faqs.org/rfcs/rfc3672" class="link external">» RFC 3672</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_VALUESRETURNFILTER`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Filter returned values
(<a href="http://www.faqs.org/rfcs/rfc3876" class="link external">» RFC 3876</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_ASSERT`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Assertion
(<a href="http://www.faqs.org/rfcs/rfc45282" class="link external">» RFC 4528</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_PRE_READ`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Pre read
(<a href="http://www.faqs.org/rfcs/rfc4527" class="link external">» RFC 4527</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_POST_READ`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Post read
(<a href="http://www.faqs.org/rfcs/rfc4527" class="link external">» RFC 4527</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_SORTREQUEST`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Sort request
(<a href="http://www.faqs.org/rfcs/rfc2891" class="link external">» RFC 2891</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_SORTRESPONSE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Sort response
(<a href="http://www.faqs.org/rfcs/rfc2891" class="link external">» RFC 2891</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_PAGEDRESULTS`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Paged results
(<a href="http://www.faqs.org/rfcs/rfc2696" class="link external">» RFC 2696</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_AUTHZID_REQUEST`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Authorization Identity Request
(<a href="http://www.faqs.org/rfcs/rfc3829" class="link external">» RFC 3829</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_AUTHZID_RESPONSE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Authorization Identity
Response
(<a href="http://www.faqs.org/rfcs/rfc3829" class="link external">» RFC 3829</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_SYNC`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Content Synchronization
Operation
(<a href="http://www.faqs.org/rfcs/rfc4533" class="link external">» RFC 4533</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_SYNC_STATE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Content Synchronization
Operation State
(<a href="http://www.faqs.org/rfcs/rfc4533" class="link external">» RFC 4533</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_SYNC_DONE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Content Synchronization
Operation Done
(<a href="http://www.faqs.org/rfcs/rfc4533" class="link external">» RFC 4533</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_DONTUSECOPY`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Don't Use Copy
(<a href="http://www.faqs.org/rfcs/rfc6171" class="link external">» RFC 6171</a>).
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_PASSWORDPOLICYREQUEST`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Password Policy Request.
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_PASSWORDPOLICYRESPONSE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Password Policy Response.
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_X_INCREMENTAL_VALUES`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Active Directory Incremental
Values. Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_X_DOMAIN_SCOPE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Active Directory Domain Scope.
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_X_PERMISSIVE_MODIFY`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Active Directory Permissive
Modify. Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_X_SEARCH_OPTIONS`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Active Directory Search
Options. Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_X_TREE_DELETE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Active Directory Tree Delete.
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_X_EXTENDED_DN`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Active Directory Extended DN.
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_VLVREQUEST`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Virtual List View Request.
Available as of PHP 7.3.0. </span>

**`LDAP_CONTROL_VLVRESPONSE`** (<span class="type">string</span>)  
<span class="simpara"> Control Constant - Virtual List View Response.
Available as of PHP 7.3.0. </span>
