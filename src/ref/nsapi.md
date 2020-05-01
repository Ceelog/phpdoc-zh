NSAPI implements a subset of the functions from the Apache module for
maximum compatibility.

| Apache function (only as alias)                         | NSAPI function                                         | Description                     |
|---------------------------------------------------------|--------------------------------------------------------|---------------------------------|
| <span class="function">apache\_request\_headers</span>  | <span class="function">nsapi\_request\_headers</span>  | Fetch all HTTP request headers  |
| <span class="function">apache\_response\_headers</span> | <span class="function">nsapi\_response\_headers</span> | Fetch all HTTP response headers |
| <span class="function">getallheaders</span>             | <span class="function">nsapi\_request\_headers</span>  | Fetch all HTTP request headers  |
| <span class="function">virtual</span>                   | <span class="function">nsapi\_virtual</span>           | Make NSAPI sub-request          |

nsapi\_request\_headers
=======================

Fetch all HTTP request headers

### 说明

<span class="type">array</span> <span
class="methodname">nsapi\_request\_headers</span> ( <span
class="methodparam">void</span> )

<span class="function">nsapi\_request\_headers</span> gets all the HTTP
headers in the current request. This is only supported when PHP runs as
a <span class="productname">NSAPI</span> module.

> **Note**:
>
> <span class="function">getallheaders</span> is an alias for <span
> class="function">nsapi\_request\_headers</span> if you use the NSAPI
> module.

> **Note**:
>
> You can also get at the value of the common CGI variables by reading
> them from the `$_SERVER` superglobal, which works whether or not you
> are using PHP as a <span class="productname">NSAPI</span> module.

### 返回值

Returns an associative array with all the HTTP headers.

### 范例

**示例 \#1 <span class="function">nsapi\_request\_headers</span>
example**

``` php
<?php
$headers = nsapi_request_headers();

foreach ($headers as $header => $value) {
  echo "$header: $value <br />\n";
}
?>
```

nsapi\_response\_headers
========================

Fetch all HTTP response headers

### 说明

<span class="type">array</span> <span
class="methodname">nsapi\_response\_headers</span> ( <span
class="methodparam">void</span> )

Gets all the NSAPI response headers.

### 返回值

Returns an associative array with all the NSAPI response headers.

### 参见

-   <span class="function">nsapi\_request\_headers</span>
-   <span class="function">headers\_sent</span>

nsapi\_virtual
==============

Perform an NSAPI sub-request

### 说明

<span class="type">bool</span> <span
class="methodname">nsapi\_virtual</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> )

<span class="function">nsapi\_virtual</span> is an NSAPI-specific
function which is equivalent to *\<!--\#include virtual...--\>* in SSI
(`.shtml` files). It does an NSAPI sub-request. It is useful for
including CGI scripts or .shtml files, or anything else that you'd parse
through webserver.

To run the sub-request, all buffers are terminated and flushed to the
browser, pending headers are sent too.

You cannot make recursive requests with this function to other PHP
scripts. If you want to include PHP scripts, use <span
class="function">include</span> or <span
class="function">require</span>.

> **Note**:
>
> This function depends on a undocumented feature of the
> Netscape/iPlanet/Sun webservers. Use <span
> class="function">phpinfo</span> to determine if it is available. In
> the Unix environment it should always work, in Windows it depends on
> the name of a `ns-httpdXX.dll` file.
>
> Read the note about subrequests in the NSAPI section
> (<a href="/install/unix/sun.html#install.unix.sun.notes" class="link">UNIX</a>,
> <a href="/install/windows/legacy/index.html#install.windows.legacy.sun.notes" class="link">Windows</a>)
> if you experience this problem.

### 参数

`uri`  
The URI of the script.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**目录**

-   [nsapi\_request\_headers](/ref/nsapi.html#nsapi_request_headers) —
    Fetch all HTTP request headers
-   [nsapi\_response\_headers](/ref/nsapi.html#nsapi_response_headers) —
    Fetch all HTTP response headers
-   [nsapi\_virtual](/ref/nsapi.html#nsapi_virtual) — Perform an NSAPI
    sub-request
