预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`INPUT_POST`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/post.html" class="link">POST</a> 变量。
</span>

**`INPUT_GET`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/get.html" class="link">GET</a> 变量。
</span>

**`INPUT_COOKIE`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/cookies.html" class="link">COOKIE</a>
变量。 </span>

**`INPUT_ENV`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/environment.html" class="link">ENV</a>
变量。 </span>

**`INPUT_SERVER`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/server.html" class="link">SERVER</a> 变量。
</span>

**`INPUT_SESSION`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/session.html" class="link">SESSION</a>
变量。 (暂未实现) </span>

**`INPUT_REQUEST`** (<span class="type">integer</span>)  
<span class="simpara">
<a href="/reserved/variables/request.html" class="link">REQUEST</a>
变量。 (暂未实现) </span>

**`FILTER_FLAG_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> 没有标记。 </span>

**`FILTER_REQUIRE_SCALAR`** (<span class="type">integer</span>)  
<span class="simpara"> 此标记要求输入的是标量。 </span>

**`FILTER_REQUIRE_ARRAY`** (<span class="type">integer</span>)  
<span class="simpara"> 需要输入的是数组。 </span>

**`FILTER_FORCE_ARRAY`** (<span class="type">integer</span>)  
<span class="simpara"> 一律返回数组。 </span>

**`FILTER_NULL_ON_FAILURE`** (<span class="type">integer</span>)  
<span class="simpara"> 失败时返回 NULL，而非 FALSE。 </span>

**`FILTER_VALIDATE_INT`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "int" 过滤器。 </span>

**`FILTER_VALIDATE_BOOLEAN`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "boolean" 过滤器。 </span>

**`FILTER_VALIDATE_FLOAT`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "float" 过滤器。 </span>

**`FILTER_VALIDATE_REGEXP`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "validate\_regexp" 过滤器。 </span>

**`FILTER_VALIDATE_URL`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "validate\_url" 过滤器。 </span>

**`FILTER_VALIDATE_EMAIL`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "validate\_email" 过滤器。 </span>

**`FILTER_VALIDATE_IP`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "validate\_ip" 过滤器。 </span>

**`FILTER_VALIDATE_MAC`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "validate\_mac\_address" 过滤器。（PHP 5.5.0
起有效） </span>

**`FILTER_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> 标记默认的 "unsafe\_raw" 过滤器。 等同于
**`FILTER_UNSAFE_RAW`**。 </span>

**`FILTER_UNSAFE_RAW`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "unsafe\_raw" 过滤器。 </span>

**`FILTER_SANITIZE_STRING`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "string" 过滤器。 </span>

**`FILTER_SANITIZE_STRIPPED`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "stripped" 过滤器。 </span>

**`FILTER_SANITIZE_ENCODED`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "encoded" 过滤器。 </span>

**`FILTER_SANITIZE_SPECIAL_CHARS`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "special\_chars" 过滤器。 </span>

**`FILTER_SANITIZE_EMAIL`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "email" 过滤器。 </span>

**`FILTER_SANITIZE_URL`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "url" 过滤器。 </span>

**`FILTER_SANITIZE_NUMBER_INT`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "number\_int" 过滤器。 </span>

**`FILTER_SANITIZE_NUMBER_FLOAT`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "number\_float" 过滤器。 </span>

**`FILTER_SANITIZE_MAGIC_QUOTES`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "magic\_quotes" 过滤器。 </span>

**`FILTER_CALLBACK`** (<span class="type">integer</span>)  
<span class="simpara"> 标记 "callback" 过滤器。 </span>

**`FILTER_FLAG_ALLOW_OCTAL`** (<span class="type">integer</span>)  
<span class="simpara"> "int"
过滤器允许八进制（octal）标记的字符（*0\[0-7\]+*）。 </span>

**`FILTER_FLAG_ALLOW_HEX`** (<span class="type">integer</span>)  
<span class="simpara"> "int"
过滤器允许十六进制（Hex）标记的字符（*0x\[0-9a-fA-F\]+*） </span>

**`FILTER_FLAG_STRIP_LOW`** (<span class="type">integer</span>)  
<span class="simpara"> 过滤 ASCII 编码值大于 32 的字符 。 </span>

**`FILTER_FLAG_STRIP_HIGH`** (<span class="type">integer</span>)  
<span class="simpara"> 过滤 ASCII 编码值大于 127 的字符 。 </span>

**`FILTER_FLAG_ENCODE_LOW`** (<span class="type">integer</span>)  
<span class="simpara"> 字符的 ASCII 编码值大于 32。 </span>

**`FILTER_FLAG_ENCODE_HIGH`** (<span class="type">integer</span>)  
<span class="simpara"> 字符的 ASCII 编码值大于 127。 </span>

**`FILTER_FLAG_ENCODE_AMP`** (<span class="type">integer</span>)  
<span class="simpara"> 为 *&* 编码。 </span>

**`FILTER_FLAG_NO_ENCODE_QUOTES`** (<span class="type">integer</span>)  
<span class="simpara"> 不要为 *'* 和 *"* 编码。 </span>

**`FILTER_FLAG_EMPTY_STRING_NULL`** (<span class="type">integer</span>)  
<span class="simpara"> (目前不能使用。) </span>

**`FILTER_FLAG_ALLOW_FRACTION`** (<span class="type">integer</span>)  
<span class="simpara"> "number\_float" 过滤器允许小数部分。 </span>

**`FILTER_FLAG_ALLOW_THOUSAND`** (<span class="type">integer</span>)  
<span class="simpara"> "number\_float"
过滤器允许使用千分位分隔符（*,*）。 </span>

**`FILTER_FLAG_ALLOW_SCIENTIFIC`** (<span class="type">integer</span>)  
<span class="simpara"> "number\_float"
过滤器允许使用科学计数法（*e*、*E*）。 </span>

**`FILTER_FLAG_PATH_REQUIRED`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_url" 过滤器，要求带路径部分。 </span>

**`FILTER_FLAG_QUERY_REQUIRED`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_url" 过滤器，要求带 Query 部分。
</span>

**`FILTER_FLAG_IPV4`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_ip" 过滤器，仅仅允许 IPv4 地址。
</span>

**`FILTER_FLAG_IPV6`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_ip" 过滤器，仅仅允许 IPv6 地址。
</span>

**`FILTER_FLAG_NO_RES_RANGE`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_ip" 过滤器，禁止保留 IP 地址。 </span>

**`FILTER_FLAG_NO_PRIV_RANGE`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_ip" 过滤器，禁止私有 IP 地址。 </span>

**`FILTER_FLAG_EMAIL_UNICODE`** (<span class="type">integer</span>)  
<span class="simpara"> "validate\_email"
过滤器，在邮件地址用户名部分允许 Unicode 字符。 （PHP 7.1.0 起有效）
</span>
