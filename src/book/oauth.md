OAuth
=====

**目录**

-   [简介](/intro/oauth.html)
-   [安装／配置](/oauth/setup.html)
    -   [需求](/oauth/setup.html#需求)
    -   [安装](/oauth/setup.html#安装)
    -   [运行时配置](/oauth/setup.html#运行时配置)
    -   [资源类型](/oauth/setup.html#资源类型)
-   [预定义常量](/oauth/constants.html)
-   [范例](/oauth/examples.html)
    -   [FireEagle](/oauth/examples.html#FireEagle)
-   [OAuth 函数](/ref/oauth.html)
    -   [oauth\_get\_sbs](/ref/oauth.html#oauth_get_sbs) —
        生成一个签名字符基串
    -   [oauth\_urlencode](/ref/oauth.html#oauth_urlencode) — 将 URI
        编码为 RFC 3986 规范
-   [OAuth](/class/oauth.html) — OAuth 类
    -   [OAuth::\_\_construct](/class/oauth.html#OAuth::__construct) —
        新建一个 OAuth 对象
    -   [OAuth::\_\_destruct](/class/oauth.html#OAuth::__destruct) —
        析构函数
    -   [OAuth::disableDebug](/class/oauth.html#OAuth::disableDebug) —
        关闭详细的调试
    -   [OAuth::disableRedirects](/class/oauth.html#OAuth::disableRedirects)
        — 关闭重定向
    -   [OAuth::disableSSLChecks](/class/oauth.html#OAuth::disableSSLChecks)
        — 关闭 SSL 检查
    -   [OAuth::enableDebug](/class/oauth.html#OAuth::enableDebug) —
        启用详细调试
    -   [OAuth::enableRedirects](/class/oauth.html#OAuth::enableRedirects)
        — 启用重定向
    -   [OAuth::enableSSLChecks](/class/oauth.html#OAuth::enableSSLChecks)
        — 启用 SSL 检查
    -   [OAuth::fetch](/class/oauth.html#OAuth::fetch) — 获取一个 OAuth
        受保护的资源
    -   [OAuth::generateSignature](/class/oauth.html#OAuth::generateSignature)
        — 生成一个签名
    -   [OAuth::getAccessToken](/class/oauth.html#OAuth::getAccessToken)
        — 获取一个访问令牌
    -   [OAuth::getCAPath](/class/oauth.html#OAuth::getCAPath) — 获取 CA
        信息
    -   [OAuth::getLastResponse](/class/oauth.html#OAuth::getLastResponse)
        — 获取最后一次的响应
    -   [OAuth::getLastResponseHeaders](/class/oauth.html#OAuth::getLastResponseHeaders)
        — 获取最后一次响应的头信息
    -   [OAuth::getLastResponseInfo](/class/oauth.html#OAuth::getLastResponseInfo)
        — 获取关于最后一次响应的 HTTP 信息
    -   [OAuth::getRequestHeader](/class/oauth.html#OAuth::getRequestHeader)
        — 生成 OAuth 头信息字符串签名
    -   [OAuth::getRequestToken](/class/oauth.html#OAuth::getRequestToken)
        — 获取一个请求令牌
    -   [OAuth::setAuthType](/class/oauth.html#OAuth::setAuthType) —
        设置授权类型
    -   [OAuth::setCAPath](/class/oauth.html#OAuth::setCAPath) — 设置 CA
        路径和信息
    -   [OAuth::setNonce](/class/oauth.html#OAuth::setNonce) —
        为后续请求设置现时标志
    -   [OAuth::setRequestEngine](/class/oauth.html#OAuth::setRequestEngine)
        — 设置目标请求引擎
    -   [OAuth::setRSACertificate](/class/oauth.html#OAuth::setRSACertificate)
        — 设置 RSA 证书
    -   [OAuth::setSSLChecks](/class/oauth.html#OAuth::setSSLChecks) —
        调整特定的SSL请求检查
    -   [OAuth::setTimestamp](/class/oauth.html#OAuth::setTimestamp) —
        设置时间戳
    -   [OAuth::setToken](/class/oauth.html#OAuth::setToken) —
        设置令牌和 secret
    -   [OAuth::setVersion](/class/oauth.html#OAuth::setVersion) — 设置
        OAuth 版本
-   [OAuthProvider](/class/oauthprovider.html) — OAuthProvider 类
    -   [OAuthProvider::addRequiredParameter](/class/oauthprovider.html#OAuthProvider::addRequiredParameter)
        — 添加必需的参数
    -   [OAuthProvider::callconsumerHandler](/class/oauthprovider.html#OAuthProvider::callconsumerHandler)
        — 调用 consumerNonceHandler 回调函数
    -   [OAuthProvider::callTimestampNonceHandler](/class/oauthprovider.html#OAuthProvider::callTimestampNonceHandler)
        — 调用 timestampNonceHandler 回调函数
    -   [OAuthProvider::calltokenHandler](/class/oauthprovider.html#OAuthProvider::calltokenHandler)
        — 调用 tokenNonceHandler 回调函数
    -   [OAuthProvider::checkOAuthRequest](/class/oauthprovider.html#OAuthProvider::checkOAuthRequest)
        — 检查一个 oauth 请求
    -   [OAuthProvider::\_\_construct](/class/oauthprovider.html#OAuthProvider::__construct)
        — 新建一个 OAuthProvider 对象
    -   [OAuthProvider::consumerHandler](/class/oauthprovider.html#OAuthProvider::consumerHandler)
        — 设置 consumerHandler 句柄回调函数
    -   [OAuthProvider::generateToken](/class/oauthprovider.html#OAuthProvider::generateToken)
        — 生成一个随机令牌
    -   [OAuthProvider::is2LeggedEndpoint](/class/oauthprovider.html#OAuthProvider::is2LeggedEndpoint)
        — is2LeggedEndpoint
    -   [OAuthProvider::isRequestTokenEndpoint](/class/oauthprovider.html#OAuthProvider::isRequestTokenEndpoint)
        — 设置 isRequestTokenEndpoint
    -   [OAuthProvider::removeRequiredParameter](/class/oauthprovider.html#OAuthProvider::removeRequiredParameter)
        — 移除一个必需的参数
    -   [OAuthProvider::reportProblem](/class/oauthprovider.html#OAuthProvider::reportProblem)
        — 报告问题
    -   [OAuthProvider::setParam](/class/oauthprovider.html#OAuthProvider::setParam)
        — 设置一个参数
    -   [OAuthProvider::setRequestTokenPath](/class/oauthprovider.html#OAuthProvider::setRequestTokenPath)
        — 设置请求令牌路径
    -   [OAuthProvider::timestampNonceHandler](/class/oauthprovider.html#OAuthProvider::timestampNonceHandler)
        — 设置 timestampNonceHandler 句柄回调函数
    -   [OAuthProvider::tokenHandler](/class/oauthprovider.html#OAuthProvider::tokenHandler)
        — 设置 tokenHandler 句柄回调函数
-   [OAuthException](/class/oauthexception.html) — OAuthException 类

简介
----

此 OAuth 扩展提供一个简单接口使用 OAuth HTTP
规范与数据提供者互动，以便保护私有资源。

类摘要
------

**OAuth**

<span class="ooclass"> class **OAuth** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$debug` ;

<span class="modifier">public</span> `$sslChecks` ;

<span class="modifier">public</span> `$debugInfo` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$consumer_key`</span> , <span class="methodparam"><span
class="type">string</span> `$consumer_secret`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$signature_method`<span class="initializer"> =
**`OAUTH_SIG_METHOD_HMACSHA1`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$auth_type`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disableDebug</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disableRedirects</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disableSSLChecks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">enableDebug</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">enableRedirects</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">enableSSLChecks</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">fetch</span> ( <span class="methodparam"><span
class="type">string</span> `$protected_resource_url`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$extra_parameters`</span> \[, <span class="methodparam"><span
class="type">string</span> `$http_method`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$http_headers`</span> \]\]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">generateSignature</span> ( <span
class="methodparam"><span class="type">string</span>
`$http_method`</span> , <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$extra_parameters`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getAccessToken</span> ( <span
class="methodparam"><span class="type">string</span>
`$access_token_url`</span> \[, <span class="methodparam"><span
class="type">string</span> `$auth_session_handle`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$verifier_token`</span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getCAPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLastResponse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLastResponseHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getLastResponseInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getRequestHeader</span> ( <span
class="methodparam"><span class="type">string</span>
`$http_method`</span> , <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$extra_parameters`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getRequestToken</span> ( <span
class="methodparam"><span class="type">string</span>
`$request_token_url`</span> \[, <span class="methodparam"><span
class="type">string</span> `$callback_url`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">setAuthType</span> ( <span
class="methodparam"><span class="type">int</span> `$auth_type`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">setCAPath</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ca_path`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$ca_info`</span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">setNonce</span> ( <span
class="methodparam"><span class="type">string</span> `$nonce`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setRequestEngine</span> ( <span
class="methodparam"><span class="type">int</span> `$reqengine`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">setRSACertificate</span> ( <span
class="methodparam"><span class="type">string</span> `$cert`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSSLChecks</span> ( <span
class="methodparam"><span class="type">int</span> `$sslcheck`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">setTimestamp</span> ( <span
class="methodparam"><span class="type">string</span> `$timestamp`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setToken</span> ( <span
class="methodparam"><span class="type">string</span> `$token`</span> ,
<span class="methodparam"><span class="type">string</span>
`$token_secret`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setVersion</span> ( <span
class="methodparam"><span class="type">string</span> `$version`</span> )

}

属性
----

`debug`  

`sslChecks`  

`debugInfo`  

OAuth::\_\_construct
====================

新建一个 OAuth 对象

### 说明

<span class="modifier">public</span> <span
class="methodname">OAuth::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span>
`$consumer_key`</span> , <span class="methodparam"><span
class="type">string</span> `$consumer_secret`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$signature_method`<span class="initializer"> =
**`OAUTH_SIG_METHOD_HMACSHA1`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$auth_type`<span
class="initializer"> = 0</span></span> \]\] )

新建一个 OAuth 对象

### 参数

`consumer_key`  
由服务提供者提供的 consumer key 。

`consumer_secret`  
由服务提供者提供的 consumer secret 。

`signature_method`  
可选参数，用来定义使用哪种签名方法，默认为
**`OAUTH_SIG_METHOD_HMACSHA1`** （HMAC-SHA1）。

`auth_type`  
可选参数，用来定义如何传递 OAuth
参数给消费方，默认为**`OAUTH_AUTH_TYPE_AUTHORIZATION`** （在
*Authorization* 头部）。

OAuth::\_\_destruct
===================

析构函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuth::\_\_destruct</span> ( <span
class="methodparam">void</span> )

析构函数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">OAuth::\_\_construct</span>

OAuth::disableDebug
===================

关闭详细的调试

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::disableDebug</span> ( <span
class="methodparam">void</span> )

关闭详细的请求信息（默认为关闭）。或者，将
<a href="/class/oauth.html#" class="link">调试</a> 属性设置为
**`false`** 值来关闭调试。

### 参数

此函数没有参数。

### 返回值

**`true`**

### 更新日志

| 版本   | 说明                                                               |
|--------|--------------------------------------------------------------------|
| 0.99.8 | 增加相关 <a href="/class/oauth.html#" class="link">调试</a> 属性。 |

### 参见

-   <span class="methodname">OAuth::enableDebug</span>

OAuth::disableRedirects
=======================

关闭重定向

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::disableRedirects</span> ( <span
class="methodparam">void</span> )

禁用自动跟随其后的重定向，这样，手动重定向请求。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`true`**

### 参见

-   <span class="methodname">OAuth::enableRedirects</span>

OAuth::disableSSLChecks
=======================

关闭 SSL 检查

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::disableSSLChecks</span> ( <span
class="methodparam">void</span> )

关闭通常的 SSL 对等证书和主机检查，但不用于生产环境。或者，设置
`sslChecks` 成员为 **`false`** 来关闭 SSL 检查。

### 参数

此函数没有参数。

### 返回值

**`true`**

### 更新日志

| 版本   | 说明                    |
|--------|-------------------------|
| 0.99.8 | 增加了 `sslChecks` 成员 |

### 参见

-   <span class="methodname">OAuth::enableSSLChecks</span>

OAuth::enableDebug
==================

启用详细调试

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::enableDebug</span> ( <span
class="methodparam">void</span> )

打开用于调试的详细请求信息，调试信息存储在 `debugInfo`
成员中。或者，可以设置 `debug` 成员为一个非 **`false`**
值来打开启用调试。

### 参数

此函数没有参数。

### 返回值

**`true`**

### 更新日志

| 版本   | 说明                               |
|--------|------------------------------------|
| 0.99.8 | 增加了 `debug` 和 `debugInfo` 成员 |

### 参见

-   <span class="methodname">OAuth::disableDebug</span>

OAuth::enableRedirects
======================

启用重定向

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::enableRedirects</span> ( <span
class="methodparam">void</span> )

启用自动重定向，此项默认为启用。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

**`true`**

### 参见

-   <span class="methodname">OAuth::disableRedirects</span>

OAuth::enableSSLChecks
======================

启用 SSL 检查

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::enableSSLChecks</span> ( <span
class="methodparam">void</span> )

启用通常的l SSL 对等证书和主机检查（默认为启用）。或者，可以设置
`sslChecks` 成员为一个非 **`false`** 值来启用 SSL 检查。

### 参数

此函数没有参数。

### 返回值

**`true`**

### 更新日志

| 版本   | 说明                  |
|--------|-----------------------|
| 0.99.8 | 增加 `sslChecks` 成员 |

### 参见

-   <span class="methodname">OAuth::disableSSLChecks</span>

OAuth::fetch
============

获取一个 OAuth 受保护的资源

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">OAuth::fetch</span> ( <span
class="methodparam"><span class="type">string</span>
`$protected_resource_url`</span> \[, <span class="methodparam"><span
class="type">array</span> `$extra_parameters`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$http_method`</span> \[, <span class="methodparam"><span
class="type">array</span> `$http_headers`</span> \]\]\] )

获取一个资源。

### 参数

`protected_resource_url`  
OAuth 受保护资源的URL

`extra_parameters`  
和资源请求一起发送的额外参数。

`http_method`  
**`OAUTH_HTTP_METHOD_*`** 系列
<a href="/oauth/constants.html" class="link">OAUTH 常量</a>之一，GET、POST、PUT、HEAD
或 DELETE 其中的一个。

HEAD （**`OAUTH_HTTP_METHOD_HEAD`** ）可以用于先于请求发现信息（如果
OAuth 证书在 *Authorization* 头部）。

`http_headers`  
HTTP 客户端头信息（像 User-Agent， Accept 等等这样的）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本   | 说明                                            |
|--------|-------------------------------------------------|
| 1.0.0  | 以前失败时返回 **`null`**，而不是 **`false`**。 |
| 0.99.5 | 新增 `http_method` 参数                         |
| 0.99.8 | 新增 `http_headers` 参数                        |

### 范例

**示例 \#1 <span class="function">OAuth::fetch</span> example**

``` php
<?php
try {
    $oauth = new OAuth("consumer_key","consumer_secret",OAUTH_SIG_METHOD_HMACSHA1,OAUTH_AUTH_TYPE_AUTHORIZATION);
    $oauth->setToken("access_token","access_token_secret");

    $oauth->fetch("http://photos.example.net/photo?file=vacation.jpg");

    $response_info = $oauth->getLastResponseInfo();
    header("Content-Type: {$response_info["content_type"]}");
    echo $oauth->getLastResponse();
} catch(OAuthException $E) {
    echo "Exception caught!\n";
    echo "Response: ". $E->lastResponse . "\n";
}
?>
```

### 参见

-   <span class="methodname">OAuth::getLastResponse</span>
-   <span class="methodname">OAuth::getLastResponseInfo</span>
-   <span class="methodname">OAuth::setToken</span>

OAuth::generateSignature
========================

生成一个签名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">OAuth::generateSignature</span> ( <span
class="methodparam"><span class="type">string</span>
`$http_method`</span> , <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$extra_parameters`</span> \] )

生成一个基于最终 HTTP 方法、URL 和 一个字符串/数组参数的签名。

### 参数

`http_method`  
用来请求的 HTTP 方法

`url`  
用来请求的 URL

`extra_parameters`  
字符串或数组的附加参数

### 返回值

一个包含签名的字符串 或者在失败时返回 **`false`**

OAuth::getAccessToken
=====================

获取一个访问令牌

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">OAuth::getAccessToken</span> ( <span
class="methodparam"><span class="type">string</span>
`$access_token_url`</span> \[, <span class="methodparam"><span
class="type">string</span> `$auth_session_handle`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$verifier_token`</span> \]\] )

从服务提供者获取一个访问令牌、secret以及一些附带的响应参数 。

### 参数

`access_token_url`  
用于访问令牌 API 的 URL。

`auth_session_handle`  
授权会话句柄，此参数在 OAuth 规范核心中没有任何引用，
但可能被大的提供者实现。<a href="http://oauth.pbwiki.com/ScalableOAuth/" class="link external">» 参见 ScalableOAuth</a>
获取更多信息。

`verifier_token`  
对于支持 1.0a 的服务提供者， 当交换请求令牌和访问令牌时，必须传递
`verifier_token` 。如果 `verifier_token` 存在于 `$_GET` 或 `$_POST`
中，它将被自动传递，且调用者不需要指定一个 `verifier_token`
（通常如果访问令牌在 oauth\_callback URL 上被交换 ）。
<a href="http://oauth.pbwiki.com/ScalableOAuth/" class="link external">» 参见 ScalableOAuth</a>
获取更多信息。

### 返回值

成功则返回一个包含解析过的 OAuth 响应的数组， 失败则返回 **`false`** 。

### 更新日志

| 版本   | 说明                                            |
|--------|-------------------------------------------------|
| 1.0.0  | 以前失败时返回 **`null`**，而不是 **`false`**。 |
| 0.99.9 | 新增 `verifier_token` 参数                      |

### 范例

**示例 \#1 <span class="function">OAuth::getAccessToken</span> 例子**

``` php
<?php
try {
    $oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
    $oauth->setToken($request_token,$request_token_secret);
    $access_token_info = $oauth->getAccessToken("https://example.com/oauth/access_token");
    if(!empty($access_token_info)) {
        print_r($access_token_info);
    } else {
        print "Failed fetching access token, response was: " . $oauth->getLastResponse();
    }
} catch(OAuthException $E) {
    echo "Response: ". $E->lastResponse . "\n";
}
?>
```

以上例程的输出类似于：

    Array
    (
        [oauth_token] => some_token
        [oauth_token_secret] => some_token_secret
    )

### 参见

-   <span class="methodname">OAuth::getLastResponse</span>
-   <span class="methodname">OAuth::getLastResponseInfo</span>
-   <span class="methodname">OAuth::setToken</span>

OAuth::getCAPath
================

获取 CA 信息

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">OAuth::getCAPath</span> ( <span
class="methodparam">void</span> )

获取证书授权的信息，其中包括通过 <span
class="methodname">OAuth::setCaPath</span> 设置的 ca\_path 和 ca\_info
。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

返回一个证书授权信息的 <span class="type">数组</span>
，在返回的关联数组中明确地包含 *ca\_path* 和 *ca\_info* 键。

### 参见

-   <span class="methodname">OAuth::setCAPath</span>
-   <span class="methodname">OAuth::getLastResponseInfo</span>

OAuth::getLastResponse
======================

获取最后一次的响应

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">OAuth::getLastResponse</span> ( <span
class="methodparam">void</span> )

获取最近一次请求的原始响应。

### 参数

此函数没有参数。

### 返回值

返回一个最后一次响应的字符串。

### 参见

-   <span class="methodname">OAuth::getLastResponseInfo</span>
-   <span class="methodname">OAuth::fetch</span>

OAuth::getLastResponseHeaders
=============================

获取最后一次响应的头信息

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">OAuth::getLastResponseHeaders</span> ( <span
class="methodparam">void</span> )

获取最后一次响应的头信息。

### 参数

此函数没有参数。

### 返回值

返回一个包含最后一次响应头信息的字符串 或者在失败时返回 **`false`** 。

OAuth::getLastResponseInfo
==========================

获取关于最后一次响应的 HTTP 信息

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">OAuth::getLastResponseInfo</span> ( <span
class="methodparam">void</span> )

获取关于最后一次响应的 HTTP 信息。

### 参数

此函数没有参数。

### 返回值

返回一个包含最后一次请求响应信息的数组。可以用到来自 <span
class="function">curl\_getinfo</span> 的常量。

### 参见

-   <span class="methodname">OAuth::fetch</span>
-   <span class="methodname">OAuth::getLastResponse</span>

OAuth::getRequestHeader
=======================

生成 OAuth 头信息字符串签名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">OAuth::getRequestHeader</span> ( <span
class="methodparam"><span class="type">string</span>
`$http_method`</span> , <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">mixed</span>
`$extra_parameters`</span> \] )

生成基于最终 HTTP 方法、URL 和 一个字符串/数组附加参数的 OAuth
头信息字符串签名。

### 参数

`http_method`  
请求的 HTTP 方法。

`url`  
请求的 URL 。

`extra_parameters`  
字符串或数组类型的附带参数。

### 返回值

返回 一个包含生成的请求头信息的字符串 r 或者在失败时返回 **`false`**

OAuth::getRequestToken
======================

获取一个请求令牌

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">OAuth::getRequestToken</span> ( <span
class="methodparam"><span class="type">string</span>
`$request_token_url`</span> \[, <span class="methodparam"><span
class="type">string</span> `$callback_url`</span> \] )

从服务提供者那里获取一个请求令牌、secret 、以及一些附带的响应参数。

### 参数

`request_token_url`  
请求令牌 API 的 URL。

`callback_url`  
OAuth 回调 URL。 如果传递了 `callback_url`
且为空值，则将其设置为“oob”即到 OAuth 2009.1 咨询的地址。

### 返回值

成功则返回一个包含解析过了的 OAuth 响应的数组，失败则返回 **`false`** 。

### 更新日志

| 版本   | 说明                                            |
|--------|-------------------------------------------------|
| 1.0.0  | 以前失败时返回 **`null`**，而不是 **`false`**。 |
| 0.99.9 | 增加 `callback_url` 参数。                      |

### 范例

**示例 \#1 <span class="function">OAuth::getRequestToken</span> 例子**

``` php
<?php
try {
    $oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
    $request_token_info = $oauth->getRequestToken("https://example.com/oauth/request_token");
    if(!empty($request_token_info)) {
        print_r($request_token_info);
    } else {
        print "Failed fetching request token, response was: " . $oauth->getLastResponse();
    }
} catch(OAuthException $E) {
    echo "Response: ". $E->lastResponse . "\n";
}
?>
```

以上例程的输出类似于：

    Array
    (
        [oauth_token] => some_token
        [oauth_token_secret] => some_token_secret
    )

### 参见

-   <span class="methodname">OAuth::getLastResponse</span>
-   <span class="methodname">OAuth::getLastResponseInfo</span>

OAuth::setAuthType
==================

设置授权类型

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">OAuth::setAuthType</span> ( <span
class="methodparam"><span class="type">int</span> `$auth_type`</span> )

设置 OAuth 参数应该放在哪里传递。

### 参数

`auth_type`  
`auth_type`可能是下列标志之一（在 OAuth 1.0 规范的第 5.2
章节中按优先级降序排列）：

**`OAUTH_AUTH_TYPE_AUTHORIZATION`**  
<span class="simpara"> 在 HTTP *Authorization* 头部传递 OAuth 参数。
</span>

**`OAUTH_AUTH_TYPE_FORM`**  
<span class="simpara"> 将 OAuth 参数附加到 HTTP POST 请求主体中。
</span>

**`OAUTH_AUTH_TYPE_URI`**  
<span class="simpara"> 将 OAuth 参数附加到请求的 URI 后面 。 </span>

**`OAUTH_AUTH_TYPE_NONE`**  
<span class="simpara"> 无。 </span>

### 返回值

如果参数设置正确则返回 **`true`** ，否则返回 **`false`**
（比如，传递进一个无效的 `auth_type` ）。

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.0.0 | 以前失败时返回 **`null`**，而不是 **`false`**。 |

OAuth::setCAPath
================

设置 CA 路径和信息

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">OAuth::setCAPath</span> (\[ <span
class="methodparam"><span class="type">string</span> `$ca_path`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$ca_info`</span> \]\] )

设置证书授权中心（CA ）的路径和信息。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ca_path`  
要设置的 CA 路径。

`ca_info`  
要设置的 CA 信息。

### 返回值

成功则返回 **`true`** ，如果 `ca_path` 或 `ca_info`
其中之一被认为无效则返回 **`false`** 。

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.0.0 | 以前失败时返回 **`null`**，而不是 **`false`**。 |

### 参见

-   <span class="methodname">OAuth::getCaPath</span>

OAuth::setNonce
===============

为后续请求设置现时标志

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">OAuth::setNonce</span> ( <span
class="methodparam"><span class="type">string</span> `$nonce`</span> )

为所有后续请求设置现时标志。

### 参数

`nonce`  
oauth\_nonce 的值。

### 返回值

成功返回 **`true`** ，如果 `nonce` 被认为无效，则返回 **`false`** 。

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.0.0 | 以前失败时返回 **`null`**，而不是 **`false`**。 |

### 参见

-   <span class="methodname">OAuth::setToken</span>
-   <span class="methodname">OAuth::setAuthType</span>
-   <span class="methodname">OAuth::setVersion</span>

OAuth::setRequestEngine
=======================

设置目标请求引擎

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuth::setRequestEngine</span> ( <span
class="methodparam"><span class="type">int</span> `$reqengine`</span> )

设置请求引擎，用于发送 HTTP 请求。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`reqengine`  
想要的请求引擎。 设为 **`OAUTH_REQENGINE_STREAMS`** 则使用 PHP 流，设为
**`OAUTH_REQENGINE_CURL`** 则使用
<a href="/book/curl.html" class="link">Curl</a>。

### 返回值

没有返回值。

### 错误／异常

如果选择了一个无效的请求引擎，则发出一个 <span
class="classname">OAuthException</span> 异常。

### 范例

**示例 \#1 <span class="function">OAuth::setRequestEngine</span> 例子**

``` php
<?php
$consumer = new OAuth();

$consumer->setRequestEngine(OAUTH_REQENGINE_STREAMS);
?>
```

### 参见

-   <a href="/book/curl.html" class="link">Curl</a>
-   <a href="/book/stream.html" class="link">PHP 流</a>
-   <span class="classname">OAuthException</span>

OAuth::setRSACertificate
========================

设置 RSA 证书

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">OAuth::setRSACertificate</span> ( <span
class="methodparam"><span class="type">string</span> `$cert`</span> )

设置 RSA 证书。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`cert`  
RSA 证书。

### 返回值

成功则返回 **`true`** ，失败返回 **`false`**
（例如，RSA证书不能被传递）。

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.0.0 | 以前失败时返回 **`null`**，而不是 **`false`**。 |

### 范例

**示例 \#1 一个 <span class="methodname">OAuth::setRsaCertificate</span>
例子**

``` php
<?php
$consume = new OAuth('1234', '', OAUTH_SIG_METHOD_RSASHA1);

$consume->setRSACertificate(file_get_contents('test.pem'));
?>
```

### 参见

-   <span class="methodname">OAuth::setCaPath</span>

OAuth::setSSLChecks
===================

调整特定的SSL请求检查

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::setSSLChecks</span> ( <span
class="methodparam"><span class="type">int</span> `$sslcheck`</span> )

调整特定的SSL请求检查。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`sslcheck`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

OAuth::setTimestamp
===================

设置时间戳

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">OAuth::setTimestamp</span> ( <span
class="methodparam"><span class="type">string</span> `$timestamp`</span>
)

为后续请求设置时间戳。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`timestamp`  
时间戳。

### 返回值

返回 **`true`** ，除非 `timestamp` 无效，则返回 **`false`** 。

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 1.0.0 | 以前失败时返回 **`null`**，而不是 **`false`**。 |

### 参见

-   <span class="methodname">OAuth::setNonce</span>

OAuth::setToken
===============

设置令牌和 secret

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::setToken</span> ( <span
class="methodparam"><span class="type">string</span> `$token`</span> ,
<span class="methodparam"><span class="type">string</span>
`$token_secret`</span> )

为后续请求设置令牌和 secret。

### 参数

`token`  
OAuth 令牌

`token_secret`  
OAuth 令牌 secret。

### 返回值

**`true`**

### 范例

**示例 \#1 <span class="function">OAuth::setToken</span> 例子**

``` php
<?php
$oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
$oauth->setToken("token","token-secret");
?>
```

OAuth::setVersion
=================

设置 OAuth 版本

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">OAuth::setVersion</span> ( <span
class="methodparam"><span class="type">string</span> `$version`</span> )

为随后请求设置 OAuth 版本

### 参数

`version`  
OAuth 版本，默认值为 "1.0"

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

简介
----

管理一个 OAuth 提供者类。

参考一个外部的深入教程
<a href="http://toys.lerdorf.com/archives/55-Writing-an-OAuth-Provider-Service.html" class="link external">» 写一个 OAuth 提供者服务</a>，用来亲自实践提供服务。也可以参考
OAuth 扩展源代码里的
<a href="https://svn.php.net/viewvc/pecl/oauth/trunk/examples" class="link external">» OAuth 提供者例子</a>
。

类摘要
------

**OAuthProvider**

<span class="ooclass"> class **OAuthProvider** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">addRequiredParameter</span> ( <span
class="methodparam"><span class="type">string</span>
`$req_params`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">callconsumerHandler</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">callTimestampNonceHandler</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">calltokenHandler</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">checkOAuthRequest</span> (\[ <span
class="methodparam"><span class="type">string</span> `$uri`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$method`</span> \]\] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span>
`$params_array`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">consumerHandler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback_function`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">generateToken</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$strong`<span
class="initializer"> = false</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">is2LeggedEndpoint</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$params_array`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">isRequestTokenEndpoint</span> ( <span
class="methodparam"><span class="type">bool</span>
`$will_issue_request_token`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">removeRequiredParameter</span> ( <span
class="methodparam"><span class="type">string</span>
`$req_params`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">reportProblem</span> ( <span
class="methodparam"><span class="type">string</span>
`$oauthexception`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$send_headers`<span class="initializer"> =
true</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">setParam</span>
( <span class="methodparam"><span class="type">string</span>
`$param_key`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$param_val`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">setRequestTokenPath</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">timestampNonceHandler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">tokenHandler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback_function`</span> )

}

OAuthProvider::addRequiredParameter
===================================

添加必需的参数

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">OAuthProvider::addRequiredParameter</span> ( <span
class="methodparam"><span class="type">string</span>
`$req_params`</span> )

添加必需的 oauth 提供者参数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`req_params`  
必需的参数。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span
    class="methodname">OAuthProvider::removeRequiredParameter</span>

OAuthProvider::callconsumerHandler
==================================

调用 consumerNonceHandler 回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::callconsumerHandler</span> (
<span class="methodparam">void</span> )

调用注册的消费者句柄回调函数，此回调函数通过 <span
class="methodname">OAuthProvider::consumerHandler</span> 设置。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 错误／异常

如回调函数无法被调用或未被指定，会引发一个 **`E_ERROR`** 级别的错误。

### 参见

-   <span class="methodname">OAuthProvider::consumerHandler</span>

OAuthProvider::callTimestampNonceHandler
========================================

调用 timestampNonceHandler 回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::callTimestampNonceHandler</span>
( <span class="methodparam">void</span> )

调用注册的时间戳句柄回调函数，此回调函数通过 <span
class="methodname">OAuthProvider::timestampNonceHandler</span> 设置。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 错误／异常

如回调函数无法被调用或未被指定，会引发一个 **`E_ERROR`** 级别的错误。

### 参见

-   <span class="methodname">OAuthProvider::timestampNonceHandler</span>

OAuthProvider::calltokenHandler
===============================

调用 tokenNonceHandler 回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::calltokenHandler</span> ( <span
class="methodparam">void</span> )

调用注册的令牌句柄回调函数，此回调函数通过 <span
class="methodname">OAuthProvider::tokenHandler</span> 设置。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 错误／异常

如回调函数无法被调用或未被指定，会引发一个 **`E_ERROR`** 级别的错误。

### 参见

-   <span class="methodname">OAuthProvider::tokenHandler</span>

OAuthProvider::checkOAuthRequest
================================

检查一个 oauth 请求

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::checkOAuthRequest</span> (\[
<span class="methodparam"><span class="type">string</span> `$uri`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$method`</span> \]\] )

检查一个 OAuth 请求。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`uri`  
可选的 URI 或终点。

`method`  
HTTP 方法。 可选 **`OAUTH_HTTP_METHOD_*`**
<a href="/oauth/constants.html" class="link">OAuth 常量</a>
其中之一传递。

### 返回值

没有返回值。

### 错误／异常

如果不能检测到 HTTP 方法，则发出一个 **`E_ERROR`** 级别的错误。

### 参见

-   <span class="methodname">OAuthProvider::reportProblem</span>

OAuthProvider::\_\_construct
============================

新建一个 OAuthProvider 对象

### 说明

<span class="modifier">public</span> <span
class="methodname">OAuthProvider::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span>
`$params_array`</span> \] )

发起一个新的 <span class="classname">OAuthProvider</span> <span
class="type">对象</span>。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`params_array`  
设置限制 <a href="/features/commandline.html" class="link">CLI SAPI</a>
的可选参数。

### 返回值

返回一个 <span class="classname">OAuthProvider</span> <span
class="type">对象</span>。

### 范例

**示例 \#1 <span class="function">OAuthProvider::\_\_construct</span>
例子**

``` php
<?php
try {

    $op = new OAuthProvider();

    // 使用用户定义的回调函数
    $op->consumerHandler(array($this, 'lookupConsumer'));
    $op->timestampNonceHandler(array($this, 'timestampNonceChecker'));
    $op->tokenHandler(array($this, 'myTokenHandler'));

    // 忽略 foo_uri 参数
    $op->setParam('foo_uri', NULL);

    // 对于终点不需要令牌
    $op->setRequestTokenPath('/v1/oauth/request_token');

    $op->checkOAuthRequest();

} catch (OAuthException $e) {

    echo OAuthProvider::reportProblem($e);
}
?>
```

### 参见

-   <span class="methodname">OAuthProvider::setParam</span>

OAuthProvider::consumerHandler
==============================

设置 consumerHandler 句柄回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::consumerHandler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback_function`</span> )

设置消费者句柄回调函数，并将在后面通过 <span
class="methodname">OAuthProvider::callConsumerHandler</span> 被调用。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`callback_function`  
<span class="type">回调类型</span> 函数名。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span
class="methodname">OAuthProvider::consumerHandler</span> 回调的例子**

``` php
<?php
function lookupConsumer($provider) {

    if ($provider->consumer_key === 'unknown') {
        return OAUTH_CONSUMER_KEY_UNKNOWN;
    } else if($provider->consumer_key == 'blacklisted' || $provider->consumer_key === 'throttled') {
        return OAUTH_CONSUMER_KEY_REFUSED;
    }

    $provider->consumer_secret = "the_consumers_secret";

    return OAUTH_OK;
}
?>
```

### 参见

-   <span class="methodname">OAuthProvider::callConsumerHandler</span>

OAuthProvider::generateToken
============================

生成一个随机令牌

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">OAuthProvider::generateToken</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$strong`<span
class="initializer"> = false</span></span> \] )

生成一个伪随机字节的 <span class="type">字符串</span> 。

### 参数

`size`  
想要的令牌长度，单位为字节。

`strong`  
设置为 **`true`** 则意味着将对熵使用 */dev/random* ，否则使用非阻塞的
*/dev/urandom*。在 Windows 平台将忽略此参数。

### 返回值

生成的令牌，一个以字节为单位的 <span class="type">字符串</span> 。

### 错误／异常

如果 `strong` 参数为 **`true`** ， 则当回退到用 <span
class="function">rand</span> 来实现填充剩余的随机字节的时候，将触发一个
**`E_WARNING`** 级别的错误（比如，当最初找不到足够的随机数据的时候）。

### 范例

**示例 \#1 <span class="function">OAuthProvider::generateToken</span>
例子**

``` php
<?php
$p = new OAuthProvider();

$t = $p->generateToken(4);

echo strlen($t),  PHP_EOL;
echo bin2hex($t), PHP_EOL;

?>
```

以上例程的输出类似于：

    4
    b6a82c27

### 注释

> **Note**:
>
> 当系统没有足够的随机数据可用的时候，此函数将使用 PHP 内部的 <span
> class="function">rand</span> 来实现填充剩余的随机字节。

### 参见

-   <span class="function">openssl\_random\_pseudo\_bytes</span>
-   <span class="function">mcrypt\_create\_iv</span>

OAuthProvider::is2LeggedEndpoint
================================

is2LeggedEndpoint

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::is2LeggedEndpoint</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$params_array`</span> )

2-legged 流程，或请求签名。不需要令牌。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`params_array`  

### 返回值

返回一个 <span class="classname">OAuthProvider</span> <span
class="type">对象</span>.

### 范例

**示例 \#1 <span
class="function">OAuthProvider::is2LeggedEndpoint</span> 例子**

``` php
<?php

$provider = new OAuthProvider();

$provider->is2LeggedEndpoint(true);

?>
```

### 参见

-   <span class="methodname">OAuthProvider::\_\_construct</span>

OAuthProvider::isRequestTokenEndpoint
=====================================

设置 isRequestTokenEndpoint

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::isRequestTokenEndpoint</span> (
<span class="methodparam"><span class="type">bool</span>
`$will_issue_request_token`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`will_issue_request_token`  
设置是否发布一个请求令牌，从而决定 <span
class="methodname">OAuthProvider::tokenHandler</span> 是否需要被调用。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">OAuthProvider::setRequestTokenPath</span>
-   <span class="methodname">OAuthProvider::reportProblem</span>

OAuthProvider::removeRequiredParameter
======================================

移除一个必需的参数

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">OAuthProvider::removeRequiredParameter</span> ( <span
class="methodparam"><span class="type">string</span>
`$req_params`</span> )

移除一个必需的参数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`req_params`  
要被移除的必需参数。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="methodname">OAuthProvider::setParam</span>
-   <span class="methodname">OAuthProvider::addRequiredParameter</span>

OAuthProvider::reportProblem
============================

报告问题

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">OAuthProvider::reportProblem</span> ( <span
class="methodparam"><span class="type">string</span>
`$oauthexception`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$send_headers`<span class="initializer"> =
true</span></span> \] )

将问题作为一个 <span class="classname">OAuthException</span>
异常传入，可能出现的问题在
<a href="/oauth/constants.html" class="link">OAuth 常量</a>
章节里已列出。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`oauthexception`  
<span class="classname">OAuthException</span> 类。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">OAuthProvider::checkOAuthRequest</span>
-   <span
    class="methodname">OAuthProvider::isRequestTokenEndpoint</span>

OAuthProvider::setParam
=======================

设置一个参数

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">OAuthProvider::setParam</span> ( <span
class="methodparam"><span class="type">string</span> `$param_key`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$param_val`</span> \] )

设置一个参数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`param_key`  
参数的 key 。

`param_val`  
参数的值，此为可选项。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="methodname">OAuthProvider::addRequiredParameter</span>

OAuthProvider::setRequestTokenPath
==================================

设置请求令牌路径

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">OAuthProvider::setRequestTokenPath</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

设置请求令牌路径。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`path`  
路径。

### 返回值

**`true`**

### 参见

-   <span class="methodname">OAuthProvider::tokenHandler</span>

OAuthProvider::timestampNonceHandler
====================================

设置 timestampNonceHandler 句柄回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::timestampNonceHandler</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback_function`</span> )

设置时间戳 nonce 句柄回调函数，此函数将在后面被 <span
class="methodname">OAuthProvider::callTimestampNonceHandler</span>
调用。跟时间戳/nonce相关的错误将被抛给此回调函数。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`callback_function`  
<span class="type">回调类型</span> 的函数名。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span
class="methodname">OAuthProvider::timestampNonceHandler</span>
回调的例子**

``` php
<?php
function timestampNonceChecker($provider) {

    if ($provider->nonce === 'bad') {
        return OAUTH_BAD_NONCE;
    } elseif ($provider->timestamp == '0') {
        return OAUTH_BAD_TIMESTAMP;
    }
    
    return OAUTH_OK;
}
?>
```

### 参见

-   <span
    class="methodname">OAuthProvider::callTimestampNonceHandler</span>

OAuthProvider::tokenHandler
===========================

设置 tokenHandler 句柄回调函数

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">OAuthProvider::tokenHandler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback_function`</span> )

设置令牌句柄的回调函数，此回调函数将在后面被 <span
class="methodname">OAuthProvider::callTokenHandler</span> 调用。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`callback_function`  
<span class="type">回调类型</span> 的函数名。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">OAuthProvider::tokenHandler</span>
回调的例子**

``` php
<?php
function tokenHandler($provider) {
    
    if ($provider->token === 'rejected') {
        return OAUTH_TOKEN_REJECTED;
    } elseif ($provider->token === 'revoked') {
        return OAUTH_TOKEN_REVOKED;
    }

    $provider->token_secret = "the_tokens_secret";
    return OAUTH_OK;
}
?>
```

### 参见

-   <span class="methodname">OAuthProvider::callTokenHandler</span>

简介
----

当使用 OAuth 扩展发生异常错误时，抛出此异常和包含了一些有用的调试信息。

类摘要
------

**OAuthException**

<span class="ooclass"> class **OAuthException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> `$lastResponse` ;

<span class="modifier">public</span> `$debugInfo` ;

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`lastResponse`  
发生异常时的响应，如果有的话

`debugInfo`  
