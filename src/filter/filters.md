Types of filters
================

**目录**

-   [Validate filters](/filter/filters.html#Validate%20filters)
-   [Sanitize filters](/filter/filters.html#Sanitize%20filters)
-   [Other filters](/filter/filters.html#Other%20filters)
-   [Filter flags](/filter/filters.html#Filter%20flags)

Validate filters
----------------

<table>
<caption><strong>Listing of filters for validation</strong></caption>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>ID</th>
<th>Name</th>
<th>Options</th>
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>FILTER_VALIDATE_BOOLEAN</code></strong></td>
<td>"boolean"</td>
<td><code class="parameter">default</code></td>
<td><strong><code>FILTER_NULL_ON_FAILURE</code></strong></td>
<td><p>Returns <strong><code>TRUE</code></strong> for "1", "true", "on" and "yes". Returns <strong><code>FALSE</code></strong> otherwise.</p>
<p>If <strong><code>FILTER_NULL_ON_FAILURE</code></strong> is set, <strong><code>FALSE</code></strong> is returned only for "0", "false", "off", "no", and "", and <strong><code>NULL</code></strong> is returned for all non-boolean values.</p></td>
</tr>
<tr class="even">
<td><strong><code>FILTER_VALIDATE_DOMAIN</code></strong></td>
<td>"validate_domain"</td>
<td><code class="parameter">default</code></td>
<td><strong><code>FILTER_FLAG_HOSTNAME</code></strong></td>
<td><p>Validates whether the domain name label lengths are valid.</p>
<p>Validates domain names against RFC 1034, RFC 1035, RFC 952, RFC 1123, RFC 2732, RFC 2181, and RFC 1123. Optional flag <strong><code>FILTER_FLAG_HOSTNAME</code></strong> adds ability to specifically validate hostnames (they must start with an alphanumeric character and contain only alphanumerics or hyphens).</p></td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_VALIDATE_EMAIL</code></strong></td>
<td>"validate_email"</td>
<td><code class="parameter">default</code></td>
<td><strong><code>FILTER_FLAG_EMAIL_UNICODE</code></strong></td>
<td><p>Validates whether the value is a valid e-mail address.</p>
<p>In general, this validates e-mail addresses against the syntax in RFC 822, with the exceptions that comments and whitespace folding and dotless domain names are not supported.</p></td>
</tr>
<tr class="even">
<td><strong><code>FILTER_VALIDATE_FLOAT</code></strong></td>
<td>"float"</td>
<td><code class="parameter">default</code>, <code class="parameter">decimal</code>, <code class="parameter">min_range</code>, <code class="parameter">max_range</code></td>
<td><strong><code>FILTER_FLAG_ALLOW_THOUSAND</code></strong></td>
<td>Validates value as float, optionally from the specified range, and converts to float on success.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_VALIDATE_INT</code></strong></td>
<td>"int"</td>
<td><code class="parameter">default</code>, <code class="parameter">min_range</code>, <code class="parameter">max_range</code></td>
<td><strong><code>FILTER_FLAG_ALLOW_OCTAL</code></strong>, <strong><code>FILTER_FLAG_ALLOW_HEX</code></strong></td>
<td>Validates value as integer, optionally from the specified range, and converts to int on success.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_VALIDATE_IP</code></strong></td>
<td>"validate_ip"</td>
<td><code class="parameter">default</code></td>
<td><strong><code>FILTER_FLAG_IPV4</code></strong>, <strong><code>FILTER_FLAG_IPV6</code></strong>, <strong><code>FILTER_FLAG_NO_PRIV_RANGE</code></strong>, <strong><code>FILTER_FLAG_NO_RES_RANGE</code></strong></td>
<td>Validates value as IP address, optionally only IPv4 or IPv6 or not from private or reserved ranges.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_VALIDATE_MAC</code></strong></td>
<td>"validate_mac_address"</td>
<td><code class="parameter">default</code></td>
<td> </td>
<td>Validates value as MAC address.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_VALIDATE_REGEXP</code></strong></td>
<td>"validate_regexp"</td>
<td><code class="parameter">default</code>, <code class="parameter">regexp</code></td>
<td> </td>
<td>Validates value against <code class="parameter">regexp</code>, a <a href="/book/pcre.html" class="link">Perl-compatible</a> regular expression.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_VALIDATE_URL</code></strong></td>
<td>"validate_url"</td>
<td><code class="parameter">default</code></td>
<td><strong><code>FILTER_FLAG_SCHEME_REQUIRED</code></strong>, <strong><code>FILTER_FLAG_HOST_REQUIRED</code></strong>, <strong><code>FILTER_FLAG_PATH_REQUIRED</code></strong>, <strong><code>FILTER_FLAG_QUERY_REQUIRED</code></strong></td>
<td>Validates value as URL (according to <a href="http://www.faqs.org/rfcs/rfc2396" class="link external">» http://www.faqs.org/rfcs/rfc2396</a>), optionally with required components. Beware a valid URL may not specify the HTTP protocol <em>http://</em> so further validation may be required to determine the URL uses an expected protocol, e.g. <em>ssh://</em> or <em>mailto:</em>. Note that the function will only find ASCII URLs to be valid; internationalized domain names (containing non-ASCII characters) will fail.</td>
</tr>
</tbody>
</table>

> **Note**:
>
> As of PHP 5.4.11, the numbers +0 and -0 validate as both integers as
> well as floats (using **`FILTER_VALIDATE_FLOAT`** and
> **`FILTER_VALIDATE_INT`**). Before PHP 5.4.11 they only validated as
> floats (using **`FILTER_VALIDATE_FLOAT`**).
>
> When `default` is set to option, `default`'s value is used if value is
> not validated.

| 版本  | 说明                                                                                                                 |
|-------|----------------------------------------------------------------------------------------------------------------------|
| 7.4.0 | Added `min_range` and `max_range` options for **`FILTER_VALIDATE_FLOAT`**.                                           |
| 7.0.0 | Added **`FILTER_FLAG_HOSTNAME`**                                                                                     |
| 5.5.0 | Added **`FILTER_VALIDATE_MAC`**                                                                                      |
| 5.2.1 | **`FILTER_VALIDATE_URL`** now implicitly uses **`FILTER_FLAG_SCHEME_REQUIRED`** and **`FILTER_FLAG_HOST_REQUIRED`**. |

Sanitize filters
----------------

| ID                                       | Name                   | Flags                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`FILTER_SANITIZE_EMAIL`**              | "email"                |                                                                                                                                                                                                                            | Remove all characters except letters, digits and *!\#$%&'\*+-=?^\_\`{\|}\~@.\[\]*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **`FILTER_SANITIZE_ENCODED`**            | "encoded"              | **`FILTER_FLAG_STRIP_LOW`**, **`FILTER_FLAG_STRIP_HIGH`**, **`FILTER_FLAG_STRIP_BACKTICK`**, **`FILTER_FLAG_ENCODE_LOW`**, **`FILTER_FLAG_ENCODE_HIGH`**                                                                   | URL-encode string, optionally strip or encode special characters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **`FILTER_SANITIZE_MAGIC_QUOTES`**       | "magic\_quotes"        |                                                                                                                                                                                                                            | Apply <span class="function">addslashes</span>.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **`FILTER_SANITIZE_NUMBER_FLOAT`**       | "number\_float"        | **`FILTER_FLAG_ALLOW_FRACTION`**, **`FILTER_FLAG_ALLOW_THOUSAND`**, **`FILTER_FLAG_ALLOW_SCIENTIFIC`**                                                                                                                     | Remove all characters except digits, *+-* and optionally *.,eE*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **`FILTER_SANITIZE_NUMBER_INT`**         | "number\_int"          |                                                                                                                                                                                                                            | Remove all characters except digits, plus and minus sign.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **`FILTER_SANITIZE_SPECIAL_CHARS`**      | "special\_chars"       | **`FILTER_FLAG_STRIP_LOW`**, **`FILTER_FLAG_STRIP_HIGH`**, **`FILTER_FLAG_STRIP_BACKTICK`**, **`FILTER_FLAG_ENCODE_HIGH`**                                                                                                 | HTML-escape *'"\<\>&* and characters with ASCII value less than 32, optionally strip or encode other special characters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **`FILTER_SANITIZE_FULL_SPECIAL_CHARS`** | "full\_special\_chars" | **`FILTER_FLAG_NO_ENCODE_QUOTES`**,                                                                                                                                                                                        | Equivalent to calling <span class="function">htmlspecialchars</span> with **`ENT_QUOTES`** set. Encoding quotes can be disabled by setting **`FILTER_FLAG_NO_ENCODE_QUOTES`**. Like <span class="function">htmlspecialchars</span>, this filter is aware of the <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> and if a sequence of bytes is detected that makes up an invalid character in the current character set then the entire string is rejected resulting in a 0-length string. When using this filter as a default filter, see the warning below about setting the default flags to 0. |
| **`FILTER_SANITIZE_STRING`**             | "string"               | **`FILTER_FLAG_NO_ENCODE_QUOTES`**, **`FILTER_FLAG_STRIP_LOW`**, **`FILTER_FLAG_STRIP_HIGH`**, **`FILTER_FLAG_STRIP_BACKTICK`**, **`FILTER_FLAG_ENCODE_LOW`**, **`FILTER_FLAG_ENCODE_HIGH`**, **`FILTER_FLAG_ENCODE_AMP`** | Strip tags, optionally strip or encode special characters.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **`FILTER_SANITIZE_STRIPPED`**           | "stripped"             |                                                                                                                                                                                                                            | Alias of "string" filter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **`FILTER_SANITIZE_URL`**                | "url"                  |                                                                                                                                                                                                                            | Remove all characters except letters, digits and *$-\_.+!\*'(),{}\|\\\\^\~\[\]\`\<\>\#%";/?:@&=*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **`FILTER_UNSAFE_RAW`**                  | "unsafe\_raw"          | **`FILTER_FLAG_STRIP_LOW`**, **`FILTER_FLAG_STRIP_HIGH`**, **`FILTER_FLAG_STRIP_BACKTICK`**, **`FILTER_FLAG_ENCODE_LOW`**, **`FILTER_FLAG_ENCODE_HIGH`**, **`FILTER_FLAG_ENCODE_AMP`**                                     | Do nothing, optionally strip or encode special characters. This filter is also aliased to **`FILTER_DEFAULT`**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Warning**

When using one of these filters as a default filter either through your
ini file or through your web server's configuration, the default flags
is set to **`FILTER_FLAG_NO_ENCODE_QUOTES`**. You need to explicitly set
filter.default\_flags to 0 to have quotes encoded by default. Like this:

**示例 \#1 Configuring the default filter to act like htmlspecialchars**

``` php
filter.default = full_special_chars
filter.default_flags = 0
```

| 版本         | 说明                                                                                |
|--------------|-------------------------------------------------------------------------------------|
| 5.2.11/5.3.1 | Slashes (*/*) are removed by **`FILTER_SANITIZE_EMAIL`**. Prior they were retained. |

Other filters
-------------

| ID                    | Name       | Options                                               | Flags                 | Description                                |
|-----------------------|------------|-------------------------------------------------------|-----------------------|--------------------------------------------|
| **`FILTER_CALLBACK`** | "callback" | <span class="type">callable</span> function or method | All flags are ignored | Call user-defined function to filter data. |

Filter flags
------------

<table>
<caption><strong>List of filter flags</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>ID</th>
<th>Used with</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>FILTER_FLAG_STRIP_LOW</code></strong></td>
<td><strong><code>FILTER_SANITIZE_ENCODED</code></strong>, <strong><code>FILTER_SANITIZE_SPECIAL_CHARS</code></strong>, <strong><code>FILTER_SANITIZE_STRING</code></strong>, <strong><code>FILTER_UNSAFE_RAW</code></strong></td>
<td>Strips characters that have a numerical value &lt;32.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_STRIP_HIGH</code></strong></td>
<td><strong><code>FILTER_SANITIZE_ENCODED</code></strong>, <strong><code>FILTER_SANITIZE_SPECIAL_CHARS</code></strong>, <strong><code>FILTER_SANITIZE_STRING</code></strong>, <strong><code>FILTER_UNSAFE_RAW</code></strong></td>
<td>Strips characters that have a numerical value &gt;127.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_STRIP_BACKTICK</code></strong></td>
<td><strong><code>FILTER_SANITIZE_ENCODED</code></strong>, <strong><code>FILTER_SANITIZE_SPECIAL_CHARS</code></strong>, <strong><code>FILTER_SANITIZE_STRING</code></strong>, <strong><code>FILTER_UNSAFE_RAW</code></strong></td>
<td>Strips backtick characters.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_ALLOW_FRACTION</code></strong></td>
<td><strong><code>FILTER_SANITIZE_NUMBER_FLOAT</code></strong></td>
<td>Allows a period (<em>.</em>) as a fractional separator in numbers.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_ALLOW_THOUSAND</code></strong></td>
<td><strong><code>FILTER_SANITIZE_NUMBER_FLOAT</code></strong>, <strong><code>FILTER_VALIDATE_FLOAT</code></strong></td>
<td>Allows a comma (<em>,</em>) as a thousands separator in numbers.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_ALLOW_SCIENTIFIC</code></strong></td>
<td><strong><code>FILTER_SANITIZE_NUMBER_FLOAT</code></strong></td>
<td>Allows an <em>e</em> or <em>E</em> for scientific notation in numbers.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_NO_ENCODE_QUOTES</code></strong></td>
<td><strong><code>FILTER_SANITIZE_STRING</code></strong></td>
<td>If this flag is present, single (<em>'</em>) and double (<em>"</em>) quotes will not be encoded.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_ENCODE_LOW</code></strong></td>
<td><strong><code>FILTER_SANITIZE_ENCODED</code></strong>, <strong><code>FILTER_SANITIZE_STRING</code></strong>, <strong><code>FILTER_SANITIZE_RAW</code></strong></td>
<td>Encodes all characters with a numerical value &lt;32.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_ENCODE_HIGH</code></strong></td>
<td><strong><code>FILTER_SANITIZE_ENCODED</code></strong>, <strong><code>FILTER_SANITIZE_SPECIAL_CHARS</code></strong>, <strong><code>FILTER_SANITIZE_STRING</code></strong>, <strong><code>FILTER_SANITIZE_RAW</code></strong></td>
<td>Encodes all characters with a numerical value &gt;127.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_ENCODE_AMP</code></strong></td>
<td><strong><code>FILTER_SANITIZE_STRING</code></strong>, <strong><code>FILTER_SANITIZE_RAW</code></strong></td>
<td>Encodes ampersands (<em>&amp;</em>).</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_NULL_ON_FAILURE</code></strong></td>
<td><strong><code>FILTER_VALIDATE_BOOLEAN</code></strong></td>
<td>Returns <strong><code>NULL</code></strong> for unrecognized boolean values.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_ALLOW_OCTAL</code></strong></td>
<td><strong><code>FILTER_VALIDATE_INT</code></strong></td>
<td>Regards inputs starting with a zero (<em>0</em>) as octal numbers. This only allows the succeeding digits to be <em>0-7</em>.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_ALLOW_HEX</code></strong></td>
<td><strong><code>FILTER_VALIDATE_INT</code></strong></td>
<td>Regards inputs starting with <em>0x</em> or <em>0X</em> as hexadecimal numbers. This only allows succeeding characters to be <em>a-fA-F0-9</em>.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_EMAIL_UNICODE</code></strong></td>
<td><strong><code>FILTER_VALIDATE_EMAIL</code></strong></td>
<td>Allows the local part of the email address to contain Unicode characters.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_IPV4</code></strong></td>
<td><strong><code>FILTER_VALIDATE_IP</code></strong></td>
<td>Allows the IP address to be in IPv4 format.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_IPV6</code></strong></td>
<td><strong><code>FILTER_VALIDATE_IP</code></strong></td>
<td>Allows the IP address to be in IPv6 format.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_NO_PRIV_RANGE</code></strong></td>
<td><strong><code>FILTER_VALIDATE_IP</code></strong></td>
<td><p>Fails validation for the following private IPv4 ranges: <em>10.0.0.0/8</em>, <em>172.16.0.0/12</em> and <em>192.168.0.0/16</em>.</p>
<p>Fails validation for the IPv6 addresses starting with <em>FD</em> or <em>FC</em>.</p></td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_NO_RES_RANGE</code></strong></td>
<td><strong><code>FILTER_VALIDATE_IP</code></strong></td>
<td><p>Fails validation for the following reserved IPv4 ranges: <em>0.0.0.0/8</em>, <em>169.254.0.0/16</em>, <em>127.0.0.0/8</em> and <em>240.0.0.0/4</em>.</p>
<p>Fails validation for the following reserved IPv6 ranges: <em>::1/128</em>, <em>::/128</em>, <em>::ffff:0:0/96</em> and <em>fe80::/10</em>.</p></td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_SCHEME_REQUIRED</code></strong></td>
<td><strong><code>FILTER_VALIDATE_URL</code></strong></td>
<td>Requires the URL to contain a scheme part.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_HOST_REQUIRED</code></strong></td>
<td><strong><code>FILTER_VALIDATE_URL</code></strong></td>
<td>Requires the URL to contain a host part.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FLAG_PATH_REQUIRED</code></strong></td>
<td><strong><code>FILTER_VALIDATE_URL</code></strong></td>
<td>Requires the URL to contain a path part.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_FLAG_QUERY_REQUIRED</code></strong></td>
<td><strong><code>FILTER_VALIDATE_URL</code></strong></td>
<td>Requires the URL to contain a query string.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_REQUIRE_SCALAR</code></strong></td>
<td></td>
<td>Requires the value to be scalar.</td>
</tr>
<tr class="even">
<td><strong><code>FILTER_REQUIRE_ARRAY</code></strong></td>
<td></td>
<td>Requires the value to be an array.</td>
</tr>
<tr class="odd">
<td><strong><code>FILTER_FORCE_ARRAY</code></strong></td>
<td></td>
<td>If the value is a scalar, it is treated as array with the scalar value as only element.</td>
</tr>
</tbody>
</table>

| 版本   | 说明                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------|
| 7.3.0  | The explicit usage of **`FILTER_FLAG_SCHEME_REQUIRED`** and **`FILTER_FLAG_HOST_REQUIRED`** has been deprecated. |
| 7.1.0  | **`FILTER_FLAG_EMAIL_UNICODE`** has been added.                                                                  |
| 5.3.2  | **`FILTER_FLAG_STRIP_BACKTICK`** has been added.                                                                 |
| 5.2.10 | **`FILTER_FLAG_NO_RES_RANGE`** supports also IPv6 addresses.                                                     |
