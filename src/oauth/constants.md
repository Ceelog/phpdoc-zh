预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

这些常量牵涉到的大部分问题也都在官方的 OAuth
<a href="http://wiki.oauth.net/ProblemReporting" class="link external">» 问题报告</a>
文档里有描述。但是要注意，这些常量名是特定于 PHP
的，尽管这些命名规则看上去相似。

**`OAUTH_SIG_METHOD_RSASHA1`** (<span class="type">字符串</span>)  
<span class="simpara"> OAuth *RSA-SHA1* 签名方法。 </span>

**`OAUTH_SIG_METHOD_HMACSHA1`** (<span class="type">字符串</span>)  
OAuth *HMAC-SHA1* 签名方法。

**`OAUTH_SIG_METHOD_HMACSHA256`** (<span class="type">字符串</span>)  
<span class="simpara"> OAuth *HMAC-SHA256* 签名方法。 </span>

**`OAUTH_AUTH_TYPE_AUTHORIZATION`** (<span class="type">字符串</span>)  
此常量代表把 OAuth 参数放在 *Authorization* 头部。

**`OAUTH_AUTH_TYPE_NONE`** (<span class="type">字符串</span>)  
此常量标志着一个 NoAuth OAuth 请求。

**`OAUTH_AUTH_TYPE_URI`** (<span class="type">字符串</span>)  
此常量表示将 OAuth 参数放在请求中。 URI.

**`OAUTH_AUTH_TYPE_FORM`** (<span class="type">字符串</span>)  
此常量表示将 OAuth 参数作为 HTTP POST 主体的一部分。

**`OAUTH_HTTP_METHOD_GET`** (<span class="type">字符串</span>)  
为 OAuth 请求使用 *GET* 方法。

**`OAUTH_HTTP_METHOD_POST`** (<span class="type">字符串</span>)  
为 OAuth 请求使用 *POST* 方法。

**`OAUTH_HTTP_METHOD_PUT`** (<span class="type">字符串</span>)  
为 OAuth 请求使用 *PUT* 方法。

**`OAUTH_HTTP_METHOD_HEAD`** (<span class="type">字符串</span>)  
为 OAuth 请求使用 *HEAD* 方法。

**`OAUTH_HTTP_METHOD_DELETE`** (<span class="type">字符串</span>)  
<span class="simpara"> 为 OAuth 请求使用 *DELETE* 方法。 </span>

**`OAUTH_REQENGINE_STREAMS`** (<span class="type">整型</span>)  
<span class="simpara"> 使用 <span
class="methodname">OAuth::setRequestEngine</span> 来设置引擎为
<a href="/book/stream.html" class="link">PHP 流</a>，与用
**`OAUTH_REQENGINE_CURL`** 的
<a href="/book/curl.html" class="link">Curl</a> 截然相反。 </span>

**`OAUTH_REQENGINE_CURL`** (<span class="type">整型</span>)  
<span class="simpara"> 使用 <span
class="methodname">OAuth::setRequestEngine</span> 来设置引擎为
<a href="/book/curl.html" class="link">Curl</a>，与用
**`OAUTH_REQENGINE_STREAMS`** 的
<a href="/book/stream.html" class="link">PHP 流</a> 截然相反。 </span>

**`OAUTH_OK`** (<span class="type">整型</span>)  
<span class="simpara"> 一切良好。 </span>

**`OAUTH_BAD_NONCE`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_nonce*
值已经用于上一个上一个请求，因此现在不能使用了。 </span>

**`OAUTH_BAD_TIMESTAMP`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_timestamp*
值不能被服务提供者接受。这种情况下，响应应该也包含
*oauth\_acceptable\_timestamps* 参数。 </span>

**`OAUTH_CONSUMER_KEY_UNKNOWN`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_consumer\_key*
暂时不能被服务提供者接受。比如，服务提供者限流了使用者。 </span>

**`OAUTH_CONSUMER_KEY_REFUSED`** (<span class="type">整型</span>)  
<span class="simpara"> 使用者密钥遭拒绝。 </span>

**`OAUTH_INVALID_SIGNATURE`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_signature*
无效，因为和服务提供者的签名计算不匹配。 </span>

**`OAUTH_TOKEN_USED`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_token*
已经被消费。此令牌不能再被使用，因为在上一次请求中已经使用过。 </span>

**`OAUTH_TOKEN_EXPIRED`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_token* 已经过期。 </span>

**`OAUTH_TOKEN_REVOKED`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_token* 已经被撤销，且将决不再接受。
</span>

**`OAUTH_TOKEN_REJECTED`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_token*
被服务提供者拒绝。原因未知，也许是因为令牌从未发布、已经消费、过期、或服务提供者忘记了。
</span>

**`OAUTH_VERIFIER_INVALID`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_verifier* 不正确。 </span>

**`OAUTH_PARAMETER_ABSENT`** (<span class="type">整型</span>)  
<span class="simpara">
一个必需的参数没有接收到。这种情况下，响应也应该包含
*oauth\_parameters\_absent* 参数。 </span>

**`OAUTH_SIGNATURE_METHOD_REJECTED`** (<span class="type">整型</span>)  
<span class="simpara"> *oauth\_signature\_method* 不能被服务提供者接受。
</span>
