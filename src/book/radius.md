Radius
======

**目录**

-   [简介](/intro/radius.html)
-   [安装／配置](/radius/setup.html)
    -   [需求](/radius/setup.html#需求)
    -   [安装](/radius/setup.html#安装)
    -   [运行时配置](/radius/setup.html#运行时配置)
    -   [资源类型](/radius/setup.html#资源类型)
-   [预定义常量](/radius/constants.html)
    -   [RADIUS Options](/radius/constants.html#RADIUS%20Options)
    -   [RADIUS Packet
        Types](/radius/constants.html#RADIUS%20Packet%20Types)
    -   [RADIUS Attribute
        Types](/radius/constants.html#RADIUS%20Attribute%20Types)
    -   [RADIUS Vendor Specific Attribute
        Types](/radius/constants.html#RADIUS%20Vendor%20Specific%20Attribute%20Types)
-   [范例](/radius/examples.html)
-   [Radius 函数](/ref/radius.html)
    -   [radius\_acct\_open](/ref/radius.html#radius_acct_open) —
        Creates a Radius handle for accounting
    -   [radius\_add\_server](/ref/radius.html#radius_add_server) — Adds
        a server
    -   [radius\_auth\_open](/ref/radius.html#radius_auth_open) —
        Creates a Radius handle for authentication
    -   [radius\_close](/ref/radius.html#radius_close) — Frees all
        ressources
    -   [radius\_config](/ref/radius.html#radius_config) — Causes the
        library to read the given configuration file
    -   [radius\_create\_request](/ref/radius.html#radius_create_request)
        — Create accounting or authentication request
    -   [radius\_cvt\_addr](/ref/radius.html#radius_cvt_addr) — Converts
        raw data to IP-Address
    -   [radius\_cvt\_int](/ref/radius.html#radius_cvt_int) — Converts
        raw data to integer
    -   [radius\_cvt\_string](/ref/radius.html#radius_cvt_string) —
        Converts raw data to string
    -   [radius\_demangle\_mppe\_key](/ref/radius.html#radius_demangle_mppe_key)
        — Derives mppe-keys from mangled data
    -   [radius\_demangle](/ref/radius.html#radius_demangle) — Demangles
        data
    -   [radius\_get\_attr](/ref/radius.html#radius_get_attr) — Extracts
        an attribute
    -   [radius\_get\_tagged\_attr\_data](/ref/radius.html#radius_get_tagged_attr_data)
        — Extracts the data from a tagged attribute
    -   [radius\_get\_tagged\_attr\_tag](/ref/radius.html#radius_get_tagged_attr_tag)
        — Extracts the tag from a tagged attribute
    -   [radius\_get\_vendor\_attr](/ref/radius.html#radius_get_vendor_attr)
        — Extracts a vendor specific attribute
    -   [radius\_put\_addr](/ref/radius.html#radius_put_addr) — Attaches
        an IP address attribute
    -   [radius\_put\_attr](/ref/radius.html#radius_put_attr) — Attaches
        a binary attribute
    -   [radius\_put\_int](/ref/radius.html#radius_put_int) — Attaches
        an integer attribute
    -   [radius\_put\_string](/ref/radius.html#radius_put_string) —
        Attaches a string attribute
    -   [radius\_put\_vendor\_addr](/ref/radius.html#radius_put_vendor_addr)
        — Attaches a vendor specific IP address attribute
    -   [radius\_put\_vendor\_attr](/ref/radius.html#radius_put_vendor_attr)
        — Attaches a vendor specific binary attribute
    -   [radius\_put\_vendor\_int](/ref/radius.html#radius_put_vendor_int)
        — Attaches a vendor specific integer attribute
    -   [radius\_put\_vendor\_string](/ref/radius.html#radius_put_vendor_string)
        — Attaches a vendor specific string attribute
    -   [radius\_request\_authenticator](/ref/radius.html#radius_request_authenticator)
        — Returns the request authenticator
    -   [radius\_salt\_encrypt\_attr](/ref/radius.html#radius_salt_encrypt_attr)
        — Salt-encrypts a value
    -   [radius\_send\_request](/ref/radius.html#radius_send_request) —
        Sends the request and waits for a reply
    -   [radius\_server\_secret](/ref/radius.html#radius_server_secret)
        — Returns the shared secret
    -   [radius\_strerror](/ref/radius.html#radius_strerror) — Returns
        an error message
