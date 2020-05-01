oauth\_get\_sbs
===============

生成一个签名字符基串

### 说明

<span class="type">string</span> <span
class="methodname">oauth\_get\_sbs</span> ( <span
class="methodparam"><span class="type">string</span>
`$http_method`</span> , <span class="methodparam"><span
class="type">string</span> `$uri`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$request_parameters`</span> \] )

根据 pecl/oauth 生成一个签名字符基串。

### 参数

`http_method`  
HTTP 方法。

`uri`  
将要编码的 URI 。

`request_parameters`  
请求参数的数组。

### 返回值

返回一个签名字符基串。

oauth\_urlencode
================

将 URI 编码为 RFC 3986 规范

### 说明

<span class="type">string</span> <span
class="methodname">oauth\_urlencode</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> )

将 URI 编码为
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>
规范。

### 参数

`uri`  
将要编码的 URI 。

### 返回值

返回一个
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>
规范的编码字符串。

**目录**

-   [oauth\_get\_sbs](/ref/oauth.html#oauth_get_sbs) —
    生成一个签名字符基串
-   [oauth\_urlencode](/ref/oauth.html#oauth_urlencode) — 将 URI 编码为
    RFC 3986 规范
