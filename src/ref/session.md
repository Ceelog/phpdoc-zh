session\_abort
==============

Discard session array changes and finish session

### 说明

<span class="type">bool</span> <span
class="methodname">session\_abort</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_abort</span> finishes session without
saving data. Thus the original values in session data are kept.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                          |
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | The return type of this function is <span class="type">bool</span> now. Formerly, it has been <span class="type">void</span>. |

### 参见

-   `$_SESSION`
-   The
    <a href="/session/setup.html#" class="link">session.auto_start</a>
    configuration directive
-   <span class="function">session\_start</span>
-   <span class="function">session\_reset</span>
-   <span class="function">session\_commit</span>

session\_cache\_expire
======================

返回当前缓存的到期时间

### 说明

<span class="type">int</span> <span
class="methodname">session\_cache\_expire</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$new_cache_expire`</span> \] )

<span class="function">session\_cache\_expire</span> 返回
*session.cache\_expire* 的设定值。

请求开始的时候，缓存到期时间会被重置为 180，并且保存在
<a href="/session/setup.html#" class="link">session.cache_expire</a>
配置项中。 因此，针对每个请求，需要在 <span
class="function">session\_start</span> 函数调用之前 调用 <span
class="function">session\_cache\_expire</span> 来设置缓存到期时间。

### 参数

`new_cache_expire`  
如果给定 `new_cache_expire` ，就使用 `new_cache_expire`
的值设置当前缓存到期时间。

> **Note**: <span class="simpara"> 仅在 *session.cache\_limiter*
> 的设置值 *不是* *nocache* 的时候， 才可以设置 `new_cache_expire`
> 参数。 </span>

### 返回值

返回 *session.cache\_expire* 的当前设置值， 以分钟为单位，默认值是 180
（分钟）。

### 范例

**示例 \#1 <span class="function">session\_cache\_expire</span> 示例**

``` php
<?php

/* 设置缓存限制为 “private” */

session_cache_limiter('private');
$cache_limiter = session_cache_limiter();

/* 设置缓存过期时间为 30 分钟 */
session_cache_expire(30);
$cache_expire = session_cache_expire();

/* 开始会话 */

session_start();

echo "The cache limiter is now set to $cache_limiter<br />";
echo "The cached session pages expire after $cache_expire minutes";
?>
```

### 参见

-   <a href="/session/setup.html#" class="link">session.cache_expire</a>
-   <a href="/session/setup.html#" class="link">session.cache_limiter</a>
-   <span class="function">session\_cache\_limiter</span>

session\_cache\_limiter
=======================

读取/设置缓存限制器

### 说明

<span class="type">string</span> <span
class="methodname">session\_cache\_limiter</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$cache_limiter`</span> \] )

<span class="function">session\_cache\_limiter</span>
返回当前缓存限制器的名称。

缓存限制器定义了向客户端发送的 HTTP 响应头中的缓存控制策略。
客户端或者代理服务器通过检测这个响应头信息来
确定对于页面内容的缓存规则。 设置缓存限制器为 *nocache*
会进制客户端或者代理服务器缓存内容， *public*
表示允许客户端或代理服务器缓存内容， *private* 表示允许客户端缓存，
但是不允许代理服务器缓存内容。

在 *private* 模式下， 包括 <span class="productname">Mozilla</span>
在内的一些浏览器可能无法正确处理 Expire 响应头， 通过使用
*private\_no\_expire* 模式可以解决这个问题：在这种模式下，
不会向客户端发送 *Expire* 响应头。

设置为 *''* 可以关闭 自动发送缓存策略响应头的功能。

请求开始的时候，缓存限制器会被重置为默认值，并且存储在
<a href="/session/setup.html#" class="link">session.cache_limiter</a>
配置项中。 因此，如果要设置缓存限制器，对于每个请求， 都需要在调用 <span
class="function">session\_start</span> 函数之前， 调用 <span
class="function">session\_cache\_limiter</span> 函数来进行设置。

### 参数

`cache_limiter`  
如果指定了 `cache_limiter` 参数， 将使用指定值作为缓存限制器的值。

<table>
<caption><strong>可选的值</strong></caption>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>发送的响应头</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>public</em></td>
<td><div class="example-contents">
<div class="headercode">
<pre class="header"><code>Expires：（根据 session.cache_expire 的设定计算得出）
Cache-Control： public, max-age=（根据 session.cache_expire 的设定计算得出）
Last-Modified：（会话最后保存时间）</code></pre>
</div>
</div></td>
</tr>
<tr class="even">
<td><em>private_no_expire</em></td>
<td><div class="example-contents">
<div class="headercode">
<pre class="header"><code>Cache-Control: private, max-age=（根据 session.cache_expire 的设定计算得出）, pre-check=（根据 session.cache_expire 的设定计算得出）
Last-Modified: （会话最后保存时间）</code></pre>
</div>
</div></td>
</tr>
<tr class="odd">
<td><em>private</em></td>
<td><div class="example-contents">
<div class="headercode">
<pre class="header"><code>Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: private, max-age=（根据 session.cache_expire 的设定计算得出）, pre-check=（根据 session.cache_expire 的设定计算得出）
Last-Modified: （会话最后保存时间）</code></pre>
</div>
</div></td>
</tr>
<tr class="even">
<td><em>nocache</em></td>
<td><div class="example-contents">
<div class="headercode">
<pre class="header"><code>Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate, post-check=0, pre-check=0
Pragma: no-cache</code></pre>
</div>
</div></td>
</tr>
</tbody>
</table>

### 返回值

返回当前所用的缓存限制器名称。

### 范例

**示例 \#1 <span class="function">session\_cache\_limiter</span> 示例**

``` php
<?php

/* 设置缓存限制器为 'private' */

session_cache_limiter('private');
$cache_limiter = session_cache_limiter();

echo "The cache limiter is now set to $cache_limiter<br />";
?>
```

### 参见

-   <a href="/session/setup.html#" class="link">session.cache_limiter</a>

session\_commit
===============

<span class="function">session\_write\_close</span> 的别名

### 说明

此函数是该函数的别名：<span
class="function">session\_write\_close</span>。

session\_create\_id
===================

Create new session id

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">session\_create\_id</span> (\[ <span
class="methodparam"><span class="type">string</span> `$prefix`<span
class="initializer"> = ""</span></span> \] )

<span class="function">session\_create\_id</span> is used to create new
session id for the current session. It returns collision free session
id.

If session is not active, collision check is omitted.

Session ID is created according to php.ini settings.

It is important to use the same user ID of your web server for GC task
script. Otherwise, you may have permission problems especially with
files save handler.

### 参数

`prefix`  
If `prefix` is specified, new session id is prefixed by `prefix`. Not
all characters are allowed within the session id. Characters in the
range *a-z A-Z 0-9 , (comma) and - (minus)* are allowed.

### 返回值

<span class="function">session\_create\_id</span> returns new collision
free session id for the current session. If it is used without active
session, it omits collision check. On failure, **`false`** is returned.

### 范例

**示例 \#1 <span class="function">session\_create\_id</span> example
with <span class="function">session\_regenerate\_id</span>**

``` php
<?php
// My session start function support timestamp management
function my_session_start() {
    session_start();
    // Do not allow to use too old session ID
    if (!empty($_SESSION['deleted_time']) && $_SESSION['deleted_time'] < time() - 180) {
        session_destroy();
        session_start();
    }
}

// My session regenerate id function
function my_session_regenerate_id() {
    // Call session_create_id() while session is active to 
    // make sure collision free.
    if (session_status() != PHP_SESSION_ACTIVE) {
        session_start();
    }
    // WARNING: Never use confidential strings for prefix!
    $newid = session_create_id('myprefix-');
    // Set deleted timestamp. Session data must not be deleted immediately for reasons.
    $_SESSION['deleted_time'] = time();
    // Finish session
    session_commit();
    // Make sure to accept user defined session ID
    // NOTE: You must enable use_strict_mode for normal operations.
    ini_set('session.use_strict_mode', 0);
    // Set new custom session ID
    session_id($newid);
    // Start with custom session ID
    session_start();
}

// Make sure use_strict_mode is enabled.
// use_strict_mode is mandatory for security reasons.
ini_set('session.use_strict_mode', 1);
my_session_start();

// Session ID must be regenerated when
//  - User logged in
//  - User logged out
//  - Certain period has passed
my_session_regenerate_id();

// Write useful codes
?>
```

### 参见

-   <span class="function">session\_regenerate\_id</span>
-   <span class="function">session\_start</span>
-   <a href="/session/setup.html#" class="link">session.use_strict_mode</a>
-   <span class="methodname">SessionHandler::create\_sid</span>

session\_decode
===============

解码会话数据

### 说明

<span class="type">bool</span> <span
class="methodname">session\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">session\_decode</span> 对 `$data`
参数中的已经序列化的会话数据进行解码， 并且使用解码后的数据填充
$\_SESSION 超级全局变量。

请注意，这里的反序列化方法不同于 <span
class="function">unserialize</span> 函数。 序列化方法是 PHP
内置的，并且可以通过
<a href="/session/setup.html#" class="link">session.serialize_handler</a>
配置项进行修改。

### 参数

`data`  
编码后的数据

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">session\_encode</span>
-   <a href="/session/setup.html#" class="link">session.serialize_handler</a>

session\_destroy
================

销毁一个会话中的全部数据

### 说明

<span class="type">bool</span> <span
class="methodname">session\_destroy</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_destroy</span>
销毁当前会话中的全部数据， 但是不会重置当前会话所关联的全局变量，
也不会重置会话 cookie。 如果需要再次使用会话变量， 必须重新调用 <span
class="function">session\_start</span> 函数。

> **Note**: <span class="simpara"> 通常情况下，在你的代码中不必调用
> <span class="function">session\_destroy</span> 函数， 可以直接清除
> $\_SESSION 数组中的数据来实现会话数据清理。 </span>

为了彻底销毁会话，必须同时重置会话 ID。 如果是通过 cookie 方式传送会话
ID 的，那么同时也需要 调用 <span class="function">setcookie</span>
函数来 删除客户端的会话 cookie。

当启用了
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
配置项的时候，你不需要删除过期会话 ID 对应的 cookie，
因为会话模块已经不再接受携带过期会话 ID 的 cookie 了，
然后它会生成一个新的会话 ID cookie。 建议所有的站点都启用
<a href="/session/setup.html#" class="link">session.use_strict_mode</a>
配置项。

**Warning**

过早的删除会话中的数据可能会导致不可预期的结果。 例如，当存在从
JavaScript 或者 URL 链接过来的并发请求的时候，
某一个请求删除了会话中的数据，会导致其他的并发请求无法使用会话数据。

虽然当前的会话处理模块不会接受为空的会话 ID，
但是由于客户端（浏览器）的处理方式，
立即删除会话中的数据可能会导致生成为空的会话 cookie，
进而导致客户端生成很多不必要的会话 ID cookie。

为了避免这种情况的发生，你需要在 $\_SESSION 中设置一个时间戳，
在这个时间戳之后的对于会话的访问都将被拒绝。
或者，确保你的应用中不存在并发请求。 这个规则同样适用于 <span
class="function">session\_regenerate\_id</span>。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 销毁会话数据以及 `$_SESSION`**

``` php
<?php
// 初始化会话。
// 如果要使用会话，别忘了现在就调用：
session_start();

// 重置会话中的所有变量
$_SESSION = array();

// 如果要清理的更彻底，那么同时删除会话 cookie
// 注意：这样不但销毁了会话中的数据，还同时销毁了会话本身
if (ini_get("session.use_cookies")) {
    $params = session_get_cookie_params();
    setcookie(session_name(), '', time() - 42000,
        $params["path"], $params["domain"],
        $params["secure"], $params["httponly"]
    );
}

// 最后，销毁会话
session_destroy();
?>
```

### 注释

> **Note**:
>
> 对于旧版本中不使用 `$_SESSION` 的代码， 仅能使用 <span
> class="function">session\_unset</span> 来完成会话销毁工作。

### 参见

-   <a href="/session/setup.html#" class="link">session.use_strict_mode</a>
-   <span class="function">session\_reset</span>
-   <span class="function">session\_regenerate\_id</span>
-   <span class="function">unset</span>
-   <span class="function">setcookie</span>

session\_encode
===============

将当前会话数据编码为一个字符串

### 说明

<span class="type">string</span> <span
class="methodname">session\_encode</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_encode</span>
返回一个序列化后的字符串，包含被编码的、储存于 $\_SESSION
超全局变量中的当前会话数据。

请注意，序列方法 和 <span class="function">serialize</span> 是不一样的。
该序列方法是内置于 PHP 的，能够通过设置
<a href="/session/setup.html#" class="link">session.serialize_handler</a>
来设置。

### 返回值

返回当前会话编码后的内容。

### 注释

**Warning**

在调用 <span class="function">session\_decode</span> 之前必须先调用
<span class="function">session\_start</span>。

### 参见

-   <span class="function">session\_decode</span>
-   <a href="/session/setup.html#" class="link">session.serialize_handler</a>

session\_gc
===========

Perform session data garbage collection

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">session\_gc</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_gc</span> is used to perform session
data GC(garbage collection). PHP does probability based session GC by
default.

Probability based GC works somewhat but it has few problems. 1) Low
traffic sites' session data may not be deleted within the preferred
duration. 2) High traffic sites' GC may be too frequent GC. 3) GC is
performed on the user's request and the user will experience a GC delay.

Therefore, it is recommended to execute GC periodically for production
systems using, e.g., "cron" for UNIX-like systems. Make sure to disable
probability based GC by setting
<a href="/session/setup.html#" class="link">session.gc_probability</a>
to 0.

### 返回值

<span class="function">session\_gc</span> returns number of deleted
session data for success, **`false`** for failure.

Old save handlers do not return number of deleted session data, but only
success/failure flag. If this is the case, number of deleted session
data became 1 regardless of actually deleted data.

### 范例

**示例 \#1 <span class="function">session\_gc</span> example for task
managers like cron**

``` php
<?php
// Note: This script should be executed by the same user of web server process.

// Need active session to initialize session data storage access.
session_start();

// Executes GC immediately
session_gc();

// Clean up session ID created by session_gc()
session_destroy();
?>
```

**示例 \#2 <span class="function">session\_gc</span> example for user
accessible script**

``` php
<?php
// Note: session_gc() is recommended to be used by task manager script, but
// it may be used as follows.

// Used for last GC time check
$gc_time = '/tmp/php_session_last_gc';
$gc_period = 1800;

session_start();
// Execute GC only when GC period elapsed. 
// i.e. Calling session_gc() every request is waste of resources. 
if (file_exists($gc_time)) {
    if (filemtime($gc_time) < time() - $gc_period) {
        session_gc();
        touch($gc_time);
    }
} else {
    touch($gc_time);
}
?>
```

### 参见

-   <span class="function">session\_start</span>
-   <span class="function">session\_destroy</span>
-   <a href="/session/setup.html#" class="link">session.gc_probability</a>

session\_get\_cookie\_params
============================

获取会话 cookie 参数

### 说明

<span class="type">array</span> <span
class="methodname">session\_get\_cookie\_params</span> ( <span
class="methodparam">void</span> )

获取会话 cookie 的参数。

### 返回值

返回一个包含当前会话 cookie 信息的数组：

-   <span class="simpara">
    <a href="/session/setup.html#" class="link">"lifetime"</a> - cookie
    的生命周期，以秒为单位。 </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">"path"</a> - cookie
    的访问路径。 </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">"domain"</a> - cookie
    的域。 </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">"secure"</a> -
    仅在使用安全连接时发送 cookie。 </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">"httponly"</a> -
    只能通过 http 协议访问 cookie </span>

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 5.2.0 | 在返回数组中加入 “httponly”。 |
| 4.0.4 | 在返回数组中加入 “secure”。   |

### 参见

-   <a href="/session/setup.html#" class="link">session.cookie_lifetime</a>
-   <a href="/session/setup.html#" class="link">session.cookie_path</a>
-   <a href="/session/setup.html#" class="link">session.cookie_domain</a>
-   <a href="/session/setup.html#" class="link">session.cookie_secure</a>
-   <a href="/session/setup.html#" class="link">session.cookie_httponly</a>
-   <span class="function">session\_set\_cookie\_params</span>

session\_id
===========

获取/设置当前会话 ID

### 说明

<span class="type">string</span> <span
class="methodname">session\_id</span> (\[ <span
class="methodparam"><span class="type">string</span> `$id`</span> \] )

<span class="function">session\_id</span> 可以用来获取/设置 当前会话
ID。

为了能够将会话 ID 很方便的附加到 URL 之后， 你可以使用常量 **`SID`**
获取以字符串格式表达的会话名称和 ID。 请参考
<a href="/ref/session.html" class="link">会话处理</a>。

### 参数

`id`  
如果指定了 `id` 参数的值， 则使用指定值作为会话 ID。 必须在调用 <span
class="function">session\_start</span> 函数之前调用 <span
class="function">session\_id</span> 函数。 不同的会话管理器对于会话 ID
中可以使用的字符有不同的限制。 例如文件会话管理器仅允许会话 ID
中使用以下字符：*a-z A-Z 0-9 , （逗号）和 - （减号）*

> **Note**: <span class="simpara"> 如果使用 cookie 方式传送会话
> ID，并且指定了 `id` 参数， 在调用 <span
> class="function">session\_start</span> 之后都会向客户端发送新的
> cookie， 无论当前的会话 ID 和新指定的会话 ID 是否相同。 </span>

### 返回值

<span class="function">session\_id</span> 返回当前会话ID。
如果当前没有会话，则返回空字符串（*""*）。

### 参见

-   <span class="function">session\_regenerate\_id</span>
-   <span class="function">session\_start</span>
-   <span class="function">session\_set\_save\_handler</span>
-   <a href="/session/setup.html#" class="link">session.save_handler</a>

session\_is\_registered
=======================

检查变量是否在会话中已经注册

### 说明

<span class="type">bool</span> <span
class="methodname">session\_is\_registered</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

检查变量是否已经在会话中注册。

**Warning**

本函数已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

### 参数

`name`  
变量名称。

### 返回值

<span class="function">session\_is\_registered</span> 返回 **`true`**
则表示 `name` 变量已经在当前会话中注册使用，否则返回 **`false`** 。

### 注释

> **Note**:
>
> 如果使用 `$_SESSION` (或 `$HTTP_SESSION_VARS` for PHP 4.0.6 or
> less),可以使用 <span class="function">isset</span> 检查变量是否在
> `$_SESSION` 中注册使用。

**Caution**

如果使用 `$_SESSION` (或 `$HTTP_SESSION_VARS`), 则不要使用 <span
class="function">session\_register</span>, <span
class="function">session\_is\_registered</span> 和 <span
class="function">session\_unregister</span>.

session\_module\_name
=====================

获取/设置会话模块名称

### 说明

<span class="type">string</span> <span
class="methodname">session\_module\_name</span> (\[ <span
class="methodparam"><span class="type">string</span> `$module`</span> \]
)

<span class="function">session\_module\_name</span>
获取或设置会话模块名称，也被称做：<a href="/session/setup.html#" class="link">session.save_handler</a>。

### 参数

`module`  
如果指定 `module` 参数，则使用 指定值作为会话模块。 禁止传入 *"user"*
作为此参数的值， 请使用 <span
class="function">set\_set\_save\_handler</span>
来设置用户自定义的会话处理器。

### 返回值

返回当前所用的会话模块名称。

### 更新日志

| 版本  | 说明                                                                                      |
|-------|-------------------------------------------------------------------------------------------|
| 7.2.0 | 不允许设置模块名称为 *"user"*。 在之前的版本中，如果设置为 "user"，那么会被静默的忽略到。 |

session\_name
=============

读取/设置会话名称

### 说明

<span class="type">string</span> <span
class="methodname">session\_name</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

<span class="function">session\_name</span> 函数返回当前会话名称。
如果指定 `name` 参数， <span class="function">session\_name</span>
函数会更新会话名称， 并返回 *原来的* 会话名称。

如果使用 `name` 指定了新字符串作为会话 cookie 的名字， <span
class="function">session\_name</span> 函数会修改 HTTP 响应中的 cookie
（如果启用了 *session.transid*，还会输出会话 cookie 的内容）。 一旦在
HTTP 响应中发送了 cookie 的内容之后， 调用 <span
class="function">session\_name</span> 函数会产生错误。
所以，一定要在调用 <span class="function">session\_start</span> 函数之前
调用此函数。

请求开始的时候，会话名称会被重置并且存储到 *session.name* 配置项。
因此，要想设置会话名称，那么对于每个请求，都需要在 调用 <span
class="function">session\_start</span> 函数 之前调用 <span
class="function">session\_name</span> 函数。

### 参数

`name`  
用在 cookie 或者 URL 中的会话名称， 例如：*PHPSESSID*。
只能使用字母和数字作为会话名称，建议尽可能的短一些，
并且是望文知意的名字（对于启用了 cookie
警告的用户来说，方便其判断是否要允许此 cookie）。 如果指定了 `name`
参数， 那么当前会话也会使用指定值作为名称。

**Warning**
会话名称至少需要一个字母，不能全部都使用数字，
否则，每次都会生成一个新的会话 ID。

### 返回值

返回当前会话名称。如果指定 `name` 参数，那么此函数会更新会话名称，并且
返回 *原来的* 会话名称。

### 范例

**示例 \#1 <span class="function">session\_name</span> 示例**

``` php
<?php

/* 设置会话名称为 WebsiteID */

$previous_name = session_name("WebsiteID");

echo "The previous session name was $previous_name<br />";
?>
```

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | <span class="function">session\_name</span> 函数会检查会话状态， 之前的版本仅仅检查 cookie 状态。 所以，旧版本的 PHP 允许你在调用 <span class="function">session\_start</span> 函数之后再调用 <span class="function">session\_name</span> 函数， 新版本的 PHP 不再允许这样做了。 |

### 参见

-   <a href="/session/setup.html#" class="link">session.name</a>
    配置指示

session\_regenerate\_id
=======================

使用新生成的会话 ID 更新现有会话 ID

### 说明

<span class="type">bool</span> <span
class="methodname">session\_regenerate\_id</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$delete_old_session`<span class="initializer"> =
**`false`**</span></span> \] )

<span class="function">session\_regenerate\_id</span>
在不修改当前会话中数据的前提下使用新的 ID 替换原有会话 ID。

如果启用了
<a href="/session/setup.html#" class="link">session.use_trans_sid</a>
选项， 那么必须在调用 <span
class="function">session\_regenerate\_id</span>
函数之后开始进行输出工作， 否则会导致使用原有的会话 ID。

**Warning**

当前的 session\_regenerate\_id 并没有很好的处理在诸如移动数据网络和 WiFi
网络不稳定的场景。 因此，调用 session\_regenerate\_id 函数
可能会导致会话丢失。

你不应该直接销毁旧的会话所关联的数据，
而是应该使用时间戳机制来控制对于已经失效的会话 ID 的访问。
否则，可能会在并发访问的场景下导致会话数据不一致、
会话丢失等情况，甚至可能引发客户端（浏览器）创建很多无用的会话 ID。
但是，另外一方面来讲，立即删除会话中的数据 可以防止会话劫持攻击。

### 参数

`delete_old_session`  
是否删除原 ID 所关联的会话存储文件。
如果你需要避免会话并发访问冲突，那么不应该立即删除会话中的数据。
如果你需要防止会话劫持攻击，那么可以立即删除会话数据。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 A <span class="function">session\_regenerate\_id</span>
示例**

``` php
<?php
// 注意：下列不是完整的代码，只是一个示例

session_start();

// 检查会话被销毁的时间戳
if (isset($_SESSION['destroyed'])
    && $_SESSION['destroyed'] < time() - 300) {
    // 通常不会发生这种情况。如果发生，那么可能是由于不稳定的网络状况或者被攻击导致的
    // 移除用户会话中的认证信息
    remove_all_authentication_flag_from_active_sessions($_SESSION['userid']);
    throw(new DestroyedSessionAccessException);
}

$old_sessionid = session_id();

// 设置会话销毁时间戳
$_SESSION['destroyed'] = time(); // 从 PHP 7.0.0 开始, session_regenerate_id() 会自动保存会话数据

// 如果直接调用 session_regenerate_id() 函数可能会导致会话丢失的情况，
// 参见下面的例程
session_regenerate_id();

// 新创建的会话不需要时间戳
unset($_SESSION['destroyed']);

$new_sessionid = session_id();

echo "Old Session: $old_sessionid<br />";
echo "New Session: $new_sessionid<br />";

print_r($_SESSION);
?>
```

当前的会话模块未能很好的处理在网络不稳定的时候导致会话丢失的场景。
你需要自行管理会话 ID 避免调用 session\_regenerate\_id 导致会话丢失。

**示例 \#2 Avoiding lost session by <span
class="function">session\_regenerate\_id</span>**

``` php
<?php
// 注意：下列不是完整的代码，只是一个示例
// my_session_start() 和 my_session_regenerate_id()
// 函数可以避免在网络不稳定的情况下导致会话丢失的问题。
// 并且还可以避免用户会话被攻击者利用

function my_session_start() {
    session_start();
    if (isset($_SESSION['destroyed'])) {
       if ($_SESSION['destroyed'] < time()-300) {
           // 通常不会发生这种情况。如果发生，那么可能是由于不稳定的网络状况或者被攻击导致的
           // 移除用户会话中的认证信息
           remove_all_authentication_flag_from_active_sessions($_SESSION['userid']);
           throw(new DestroyedSessionAccessException);
       }
       if (isset($_SESSION['new_session_id'])) {
           // 尚未完全过期，可能是由于网络不稳定引起的。
           // 尝试再次设置正确的会话 ID cookie。
           // 注意：如果你需要移除认证标记，那么不要尝试再次设置会话 ID。
           session_commit();
           session_id($_SESSION['new_session_id']);
           // 现在有了新的会话 ID 了。
           session_start();
           return;
       }
   }
}

function my_session_regenerate_id() {
    // 如果由于不稳定的网络导致没有创建会话 ID，
    // 那么就创建一个
    $new_session_id = session_create_id();
    $_SESSION['new_session_id'] = $new_session_id;
    
    // 设置销毁时间戳
    $_SESSION['destroyed'] = time();
    
    // 保存并关闭会话
    session_commit();

    // 使用新的会话 ID 开始会话
    session_id($new_session_id);
    ini_set('session.use_strict_mode', 0);
    session_start();
    ini_set('session.use_strict_mode', 1);
    
    // 新的会话不需要这 2 个数据了
    unset($_SESSION['destroyed']);
    unset($_SESSION['new_session_id']);
}
?>
```

### 参见

-   <span class="function">session\_id</span>
-   <span class="function">session\_create\_id</span>
-   <span class="function">session\_start</span>
-   <span class="function">session\_destroy</span>
-   <span class="function">session\_reset</span>
-   <span class="function">session\_name</span>

session\_register\_shutdown
===========================

关闭会话

### 说明

<span class="type">void</span> <span
class="methodname">session\_register\_shutdown</span> ( <span
class="methodparam">void</span> )

将 <span class="function">session\_write\_close</span>
函数注册为关闭会话的函数。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 错误／异常

如果函数调用失败，触发 **`E_WARNING`** 级别的错误。

session\_register
=================

Register one or more global variables with the current session

### 说明

<span class="type">bool</span> <span
class="methodname">session\_register</span> ( <span
class="methodparam"><span class="type">mixed</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$names`</span> )

<span class="function">session\_register</span> accepts a variable
number of arguments, any of which can be either a string holding the
name of a variable or an array consisting of variable names or other
arrays. For each name, <span class="function">session\_register</span>
registers the global variable with that name in the current session.

You can also create a session variable by simply setting the appropriate
member of the `$_SESSION` array.

``` php
<?php
// Use of session_register() is deprecated
$barney = "A big purple dinosaur.";
session_register("barney");

// Use of $_SESSION is preferred
$_SESSION["zim"] = "An invader from another planet.";
?>
```

If <span class="function">session\_start</span> was not called before
this function is called, an implicit call to <span
class="function">session\_start</span> with no parameters will be made.
`$_SESSION` does not mimic this behavior and requires <span
class="function">session\_start</span> before use.

**Warning**

本函数已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

### 参数

`name`  
A string holding the name of a variable or an array consisting of
variable names or other arrays.

`names`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

**Caution**

If you want your script to work regardless of
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>,
you need to instead use the `$_SESSION` array as `$_SESSION` entries are
automatically registered. If your script uses <span
class="function">session\_register</span>, it will not work in
environments where the PHP directive
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
is disabled.

> **Note**: **register\_globals 重要说明：**  
>
> 自 PHP 4.2.0 起，PHP 指令
> <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
> 的默认值为 *off*。PHP 社区鼓励开发者不要依赖于此指令,
> 用其他手段替代，例如<a href="/language/variables/predefined.html" class="link">superglobals</a>。

**Caution**

This registers a *global* variable. If you want to register a session
variable from within a function, you need to make sure to make it global
using the
<a href="/language/variables/scope.html" class="link"><strong>global</strong></a>
keyword or the `$GLOBALS[]` array, or use the special session arrays as
noted below.

**Caution**

If you are using `$_SESSION`, do not use <span
class="function">session\_register</span>, <span
class="function">session\_is\_registered</span>, and <span
class="function">session\_unregister</span>.

> **Note**:
>
> It is currently impossible to register resource variables in a
> session. For example, you cannot create a connection to a database and
> store the connection id as a session variable and expect the
> connection to still be valid the next time the session is restored.
> PHP functions that return a resource are identified by having a return
> type of *resource* in their function definition. A list of functions
> that return resources are available in the
> <a href="/resource.html" class="link">resource types</a> appendix.
>
> If `$_SESSION` is used, assign values to `$_SESSION`. For example:
> $\_SESSION\['var'\] = 'ABC';

### 参见

-   <span class="function">session\_is\_registered</span>
-   <span class="function">session\_unregister</span>
-   `$_SESSION`

session\_reset
==============

Re-initialize session array with original values

### 说明

<span class="type">bool</span> <span
class="methodname">session\_reset</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_reset</span> reinitializes a session
with original values stored in session storage. This function requires
an active session and discards changes in $\_SESSION.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                          |
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | The return type of this function is <span class="type">bool</span> now. Formerly, it has been <span class="type">void</span>. |

### 参见

-   `$_SESSION`
-   The
    <a href="/session/setup.html#" class="link">session.auto_start</a>
    configuration directive
-   <span class="function">session\_start</span>
-   <span class="function">session\_abort</span>
-   <span class="function">session\_commit</span>

session\_save\_path
===================

读取/设置当前会话的保存路径

### 说明

<span class="type">string</span> <span
class="methodname">session\_save\_path</span> (\[ <span
class="methodparam"><span class="type">string</span> `$path`</span> \] )

<span class="function">session\_save\_path</span>
返回当前会话的保存路径。

### 参数

`path`  
指定会话数据保存的路径。 必须在调用 <span
class="function">session\_start</span> 函数之前调用 <span
class="function">session\_save\_path</span> 函数。

> **Note**:
>
> 在某些操作系统上，建议使用可以高效处理
> 大量小尺寸文件的文件系统上的路径来保存会话数据。 例如，在 Linux
> 平台上，对于会话数据保存的工作而言，reiserfs 文件系统会比 ext2fs
> 文件系统能够提供更好的性能。

### 返回值

返回保存会话数据的路径。

### 参见

-   <a href="/session/setup.html#" class="link">session.save_path</a>
    配置指示。

session\_set\_cookie\_params
============================

设置会话 cookie 参数

### 说明

<span class="type">bool</span> <span
class="methodname">session\_set\_cookie\_params</span> ( <span
class="methodparam"><span class="type">int</span> `$lifetime`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">string</span> `$domain`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$secure`<span
class="initializer"> = **`false`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$httponly`<span
class="initializer"> = **`false`**</span></span> \]\]\]\] )

<span class="type">bool</span> <span
class="methodname">session\_set\_cookie\_params</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

Cookie 参数可以在 `php.ini`
文件中定义，本函数仅在当前脚本执行过程中有效。 因此，如果要通过函数修改
cookie 参数，需要对每个请求都要 在调用 <span
class="function">session\_start</span> 函数之前调用 <span
class="function">session\_set\_cookie\_params</span> 函数。

本函数会修改运行期 ini 设置值， 可以通过 <span
class="function">ini\_get</span> 函数获取这些值。

### 参数

`lifetime`  
Cookie 的
<a href="/session/setup.html#" class="link">生命周期</a>，以秒为单位。

`path`  
此 cookie 的有效 <a href="/session/setup.html#" class="link">路径</a>。
on the domain where 设置为“/”表示对于本域上所有的路径此 cookie 都可用。

`domain`  
Cookie 的作用 <a href="/session/setup.html#" class="link">域</a>。
例如：“www.php.net”。 如果要让 cookie
在所有的子域中都可用，此参数必须以点（.）开头，例如：“.php.net”。

`secure`  
设置为 **`true`** 表示 cookie 仅在使用
<a href="/session/setup.html#" class="link">安全</a> 链接时可用。

`httponly`  
设置为 **`true`** 表示 PHP 发送 cookie 的时候会使用
<a href="/session/setup.html#" class="link">httponly</a> 标记。

`options`  
此参数为一个键值对关联 <span class="type">array</span>，可能包含的键有：
*lifetime*，*path*，*domain*, *secure*，*httponly* 以及 *samesite*。
这些键对应的值和上面所述的一样。 *samesite* 键对应的值可以是 *Lax* 或者
*Strict*。 如果可以接受的键在传入的数组中不存在，
那么会采用这些键对应的默认值作为运行时的值。 如果不提供 *samesite* 键，
那么就设置 SameSite cookie 属性。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                         |
|-------|------------------------------------------------------------------------------------------------------------------------------|
| 7.3.0 | 增加 `options` 参数， 可以通过传入一个关联数组对各个选项进行设置。 同时，通过使用这个参数还可以对 SameSite cookie 进行设置。 |
| 7.2.0 | 成功时返回 **`true`**， 或者在失败时返回 **`false`**。 之前版本中是返回 <span class="type">void</span> 的。                  |
| 5.2.0 | 加入 `httponly` 参数。                                                                                                       |

### 参见

-   <a href="/session/setup.html#" class="link">session.cookie_lifetime</a>
-   <a href="/session/setup.html#" class="link">session.cookie_path</a>
-   <a href="/session/setup.html#" class="link">session.cookie_domain</a>
-   <a href="/session/setup.html#" class="link">session.cookie_secure</a>
-   <a href="/session/setup.html#" class="link">session.cookie_httponly</a>
-   <a href="/session/setup.html#" class="link">session.cookie_samesite</a>
-   <span class="function">session\_get\_cookie\_params</span>

session\_set\_save\_handler
===========================

设置用户自定义会话存储函数

### 说明

<span class="type">bool</span> <span
class="methodname">session\_set\_save\_handler</span> ( <span
class="methodparam"><span class="type">callable</span> `$open`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$close`</span> , <span class="methodparam"><span
class="type">callable</span> `$read`</span> , <span
class="methodparam"><span class="type">callable</span> `$write`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$destroy`</span> , <span class="methodparam"><span
class="type">callable</span> `$gc`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$create_sid`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$validate_sid`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$update_timestamp`</span> \]\]\] )

自 PHP 5.4 开始，可以使用下面的方式来注册自定义会话存储函数：

<span class="type">bool</span> <span
class="methodname">session\_set\_save\_handler</span> ( <span
class="methodparam"><span class="type">object</span>
`$sessionhandler`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$register_shutdown`<span class="initializer">
= **`true`**</span></span> \] )

<span class="function">session\_set\_save\_handler</span> 设置用户自定义
会话存储函数。 如果想使用 PHP 内置的会话存储机制之外的方式，
可以使用本函数。 例如，可以自定义会话存储函数来将会话数据存储到数据库。

### 参数

本函数有 2 种原型：

`sessionhandler`  
实现了 <span class="interfacename">SessionHandlerInterface</span>，
<span class="interfacename">SessionIdInterface</span> 和/或 <span
class="interfacename">SessionUpdateTimestampHandlerInterface</span>
接口的对象， 例如 <span class="classname">SessionHandler</span>。 自 PHP
5.4 之后可以使用。

`register_shutdown`  
将函数 <span class="function">session\_write\_close</span> 注册为 <span
class="function">register\_shutdown\_function</span> 函数。

或者

`open(string $savePath, string $sessionName)`  
open 回调函数类似于类的构造函数， 在会话打开的时候会被调用。
这是自动开始会话或者通过调用 <span
class="function">session\_start</span> 手动开始会话
之后第一个被调用的回调函数。 此回调函数操作成功返回 **`true`**，反之返回
**`false`**。

`close()`  
close 回调函数类似于类的析构函数。 在 write 回调函数调用之后调用。
当调用 <span class="function">session\_write\_close</span>
函数之后，也会调用 close 回调函数。 此回调函数操作成功返回
**`true`**，反之返回 **`false`**。

`read(string $sessionId)`  
如果会话中有数据，read
回调函数必须返回将会话数据编码（序列化）后的字符串。
如果会话中没有数据，read 回调函数返回空字符串。

在自动开始会话或者通过调用 <span class="function">session\_start</span>
函数手动开始会话之后，PHP 内部调用 read 回调函数来获取会话数据。 在调用
read 之前，PHP 会调用 open 回调函数。

read 回调返回的序列化之后的字符串格式必须与 `write`
回调函数保存数据时的格式完全一致。 PHP 会自动反序列化返回的字符串并填充
`$_SESSION` 超级全局变量。 虽然数据看起来和 <span
class="function">serialize</span> 函数很相似，
但是需要提醒的是，它们是不同的。 请参考：
<a href="/session/setup.html#" class="link">session.serialize_handler</a>。

`write(string $sessionId, string $data)`  
在会话保存数据时会调用 `write` 回调函数。 此回调函数接收当前会话 ID 以及
`$_SESSION` 中数据序列化之后的字符串作为参数。 序列化会话数据的过程由
PHP 根据
<a href="/session/setup.html#" class="link">session.serialize_handler</a>
设定值来完成。

序列化后的数据将和会话 ID 关联在一起进行保存。 当调用 `read`
回调函数获取数据时，所返回的数据必须要和 传入 `write`
回调函数的数据完全保持一致。

PHP 会在脚本执行完毕或调用 <span
class="function">session\_write\_close</span> 函数之后调用此回调函数。
注意，在调用完此回调函数之后，PHP 内部会调用 `close` 回调函数。

> **Note**:
>
> PHP 会在输出流写入完毕并且关闭之后 才调用 write 回调函数， 所以在
> write 回调函数中的调试信息不会输出到浏览器中。 如果需要在 write
> 回调函数中使用调试输出， 建议将调试输出写入到文件。

`destroy($sessionId)`  
当调用 <span class="function">session\_destroy</span> 函数， 或者调用
<span class="function">session\_regenerate\_id</span> 函数并且设置
destroy 参数为 **`true`** 时， 会调用此回调函数。此回调函数操作成功返回
**`true`**，反之返回 **`false`**。

`gc($lifetime)`  
为了清理会话中的旧数据，PHP 会不时的调用垃圾收集回调函数。 调用周期由
<a href="/session/setup.html#" class="link">session.gc_probability</a>
和 <a href="/session/setup.html#" class="link">session.gc_divisor</a>
参数控制。 传入到此回调函数的 lifetime 参数由
<a href="/session/setup.html#" class="link">session.gc_maxlifetime</a>
设置。 此回调函数操作成功返回 **`true`**，反之返回 **`false`**。

`create_sid()`  
当需要新的会话 ID 时被调用的回调函数。 回调函数被调用时无传入参数，
其返回值应该是一个字符串格式的、有效的会话 ID。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                       |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.0 | 新增可选参数 `validate_sid` 和 `update_timestamp`。                                                                                                                        |
| 5.5.1 | 新增可选参数 `create_sid`。                                                                                                                                                |
| 5.4.0 | 新增用来实现自定义会话处理器的接口 <span class="interfacename">SessionHandlerInterface</span>； 新增 PHP 内部会话处理器类：<span class="classname">SessionHandler</span>。 |

### 范例

**示例 \#1 自定义会话管理器： 完整代码请参见 <span
class="classname">SessionHandlerInterface</span>。**

下列代码适用于 PHP 5.4.0 及以上版本。
这里仅列出了调用方式，完整代码请参见 <span
class="classname">SessionHandlerInterface</span>。

这里使用了 <span class="function">session\_set\_save\_handler</span>
函数的 OOP 原型 并且使用第二个参数来注册 shutdown 函数。
当将对象注册为会话保存管理器时，建议使用这种方式。

``` php
<?php
class MySessionHandler implements SessionHandlerInterface
{
    // 在这里实现接口
}

$handler = new MySessionHandler();
session_set_save_handler($handler, true);
session_start();

// 现在可以使用 $_SESSION 保存以及获取数据了
```

**示例 \#2 使用对象自定义会话保存管理器**

下列代码适用于 PHP 5.4.0 之前的版本。

下例演示了基于文件的会话数据存储， 和 PHP 默认的 `files` 存储器很相似。
通过对此示例代码进行扩展，
你可以很方便的实现使用数据库保存会话数据的功能。

针对于 PHP 5.4.0 之前的版本， 通过调用 <span
class="function">register\_shutdown\_function</span> 函数 来注册 <span
class="function">session\_write\_close</span> 回调函数。
这也是我们建议的方式。

``` php
<?php
class FileSessionHandler
{
    private $savePath;

    function open($savePath, $sessionName)
    {
        $this->savePath = $savePath;
        if (!is_dir($this->savePath)) {
            mkdir($this->savePath, 0777);
        }

        return true;
    }

    function close()
    {
        return true;
    }

    function read($id)
    {
        return (string)@file_get_contents("$this->savePath/sess_$id");
    }

    function write($id, $data)
    {
        return file_put_contents("$this->savePath/sess_$id", $data) === false ? false : true;
    }

    function destroy($id)
    {
        $file = "$this->savePath/sess_$id";
        if (file_exists($file)) {
            unlink($file);
        }

        return true;
    }

    function gc($maxlifetime)
    {
        foreach (glob("$this->savePath/sess_*") as $file) {
            if (filemtime($file) + $maxlifetime < time() && file_exists($file)) {
                unlink($file);
            }
        }

        return true;
    }
}

$handler = new FileSessionHandler();
session_set_save_handler(
    array($handler, 'open'),
    array($handler, 'close'),
    array($handler, 'read'),
    array($handler, 'write'),
    array($handler, 'destroy'),
    array($handler, 'gc')
    );

// 下面这行代码可以防止使用对象作为会话保存管理器时可能引发的非预期行为
register_shutdown_function('session_write_close');

session_start();
// 现在可以使用 $_SESSION 保存以及获取数据了
```

### 注释

**Warning**

在脚本执行完毕之后，PHP 内部会清除对象， 所以有可能不调用 `write` 和
`close` 回调函数。
这样可能会引发非预期的行为，所以当使用对象作为会话保存管理器时，
需要通过注册 shutdown 回调函数来规避风险。 通常，你可以通过调用 <span
class="function">register\_shutdown\_function</span> 函数 来注册
`'session_write_close'` 回调函数。

在 PHP 5.4.0 中，可以调用 <span
class="function">session\_register\_shutdown</span> 函数来注册 shutdown
回调函数。 如果你使用 <span
class="function">session\_set\_save\_handler</span> 的 OOP 原型，
那么仅需设置 “register shutdown” 为 **`true`** 即可。

**Warning**

在 PHP 5.0.5 中，在对象销毁之后才会调用 `write` 和 `close` 回调函数，
所以，在这两个回调函数中不可以使用对象，也不可以抛出异常。
如果在函数中抛出异常，PHP 既不会捕获它，也不会跟踪它，
这样会导致程序异常终止。 但是对象析构函数可以使用会话。

可以在析构函数中调用 <span class="function">session\_write\_close</span>
函数来解决这个问题。 但是注册 shutdown 回调函数才是更加可靠的做法。

**Warning**

如果会话在脚本结束后关闭，对于某些 SAPI
而言，当前工作目录可能已经被改变。 可以调用 <span
class="function">session\_write\_close</span>
函数在脚本执行结束之前关闭会话。

### 参见

-   <a href="/session/setup.html#" class="link">session.save_handler</a>
    配置指示
-   <a href="/session/setup.html#" class="link">session.serialize_handler</a>
    配置指示
-   <span class="function">register\_shutdown\_function</span>
-   <span class="function">session\_register\_shutdown</span> PHP 5.4.0+
-   完整的实现请参考
    <a href="https://github.com/php/php-src/blob/master/ext/session/tests/save_handler.inc" class="link external">» save_handler.inc</a>。

session\_start
==============

启动新会话或者重用现有会话

### 说明

<span class="type">bool</span> <span
class="methodname">session\_start</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="function">session\_start</span>
会创建新会话或者重用现有会话。 如果通过 GET 或者 POST 方式，或者使用
cookie 提交了会话 ID， 则会重用现有会话。

当会话自动开始或者通过 <span class="function">session\_start</span>
手动开始的时候， PHP 内部会调用会话管理器的 open 和 read 回调函数。
会话管理器可能是 PHP 默认的， 也可能是扩展提供的（SQLite 或者 Memcached
扩展）， 也可能是通过 <span
class="function">session\_set\_save\_handler</span>
设定的用户自定义会话管理器。 通过 read
回调函数返回的现有会话数据（使用特殊的序列化格式存储）， PHP
会自动反序列化数据并且填充 $\_SESSION 超级全局变量。

要想使用命名会话，请在调用 <span class="function">session\_start</span>
函数 之前调用 <span class="function">session\_name</span> 函数。

如果启用了
<a href="/session/setup.html#" class="link">session.use_trans_sid</a>
选项， <span class="function">session\_start</span>
函数会注册一个内部输出管理器， 该输出管理器完成 URL 重写的工作。

如果用户联合使用 <span class="function">ob\_start</span> 和
*ob\_gzhandler* 函数， 那么函数的调用顺序会影响输出结果。
例如，必须在开始会话之前调用 *ob\_gzhandler* 函数完成注册。

### 参数

`options`  
此参数是一个关联数组，如果提供，那么会用其中的项目覆盖
<a href="/session/setup.html#运行时配置" class="link">会话配置指示</a>
中的配置项。此数组中的键无需包含 *session.* 前缀。

除了常规的会话配置指示项， 还可以在此数组中包含 *read\_and\_close*
选项。如果将此选项的值设置为 **`true`**，
那么会话文件会在读取完毕之后马上关闭，
因此，可以在会话数据没有变动的时候，避免不必要的文件锁。

### 返回值

成功开始会话返回 **`true`** ，反之返回 **`false`**

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | 当 <span class="function">session\_start</span> 执行失败， 无法开始一个会话的时候，会返回 **`false`**， 并且不会初始化超级变量 `$_SESSION`。 |
| 7.0.0 | 新加 `options` 参数。                                                                                                                        |
| 5.3.0 | 如果函数调用失败返回 **`false`**， 之前版本返回了 **`true`**。                                                                               |

### 范例

#### 基本的会话示例

**示例 \#1 `page1.php`**

``` php
<?php
// page1.php

session_start();

echo 'Welcome to page #1';

$_SESSION['favcolor'] = 'green';
$_SESSION['animal']   = 'cat';
$_SESSION['time']     = time();

// 如果使用 cookie 方式传送会话 ID
echo '<br /><a href="page2.php">page 2</a>';

// 如果不是使用 cookie 方式传送会话 ID，则使用 URL 改写的方式传送会话 ID
echo '<br /><a href="page2.php?' . SID . '">page 2</a>';
?>
```

请求 `page1.php` 页面之后， 第二个页面 `page2.php` 会包含会话数据。
请查阅 <a href="/ref/session.html" class="link">会话参考</a>
获取更多关于
<a href="/session/examples.html#传送会话ID" class="link">会话 ID 传送</a>的信息，
在该参考页面中有关于常量 **`SID`** 的详细说明。

**示例 \#2 `page2.php`**

``` php
<?php
// page2.php

session_start();

echo 'Welcome to page #2<br />';

echo $_SESSION['favcolor']; // green
echo $_SESSION['animal'];   // cat
echo date('Y m d H:i:s', $_SESSION['time']);

// 类似 page1.php 中的代码，你可能需要在这里处理使用 SID 的场景
echo '<br /><a href="page1.php">page 1</a>';
?>
```

#### 调用 <span class="function">session\_start</span> 的时候指定选项

**示例 \#3 覆盖 Cookie 超时时间设定**

``` php
<?php
// 设置 cookie 的有效时间为 1 天
session_start([
    'cookie_lifetime' => 86400,
]);
?>
```

**示例 \#4 读取会话之后立即关闭会话存储文件**

``` php
<?php
// 如果确定不修改会话中的数据，
// 我们可以在会话文件读取完毕之后立即关闭它
// 来避免由于给会话文件加锁导致其他页面阻塞
session_start([
    'cookie_lifetime' => 86400,
    'read_and_close'  => true,
]);
```

### 注释

> **Note**:
>
> 要使用基于 cookie 的会话， 必须在输出开始之前调用 <span
> class="function">session\_start</span> 函数。

> **Note**:
>
> 建议使用
> <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>
> 来替代 <span class="function">ob\_gzhandler</span>。

> **Note**:
>
> 根据配置不同，本函数会发送几个 HTTP 响应头。 参考 <span
> class="function">session\_cache\_limiter</span> 来自定义 HTTP 响应头。

### 参见

-   `$_SESSION`
-   <a href="/session/setup.html#" class="link">session.auto_start</a>
    配置指示
-   <span class="function">session\_id</span>

session\_status
===============

返回当前会话状态

### 说明

<span class="type">int</span> <span
class="methodname">session\_status</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_status</span> 被用于返回当前会话状态。

### 返回值

-   <span class="simpara">**`PHP_SESSION_DISABLED`**
    会话是被禁用的。</span>
-   <span class="simpara">**`PHP_SESSION_NONE`**
    会话是启用的，但不存在当前会话。</span>
-   <span class="simpara">**`PHP_SESSION_ACTIVE`**
    会话是启用的，而且存在当前会话。</span>

### 参见

-   <span class="function">session\_start</span>

session\_unregister
===================

Unregister a global variable from the current session

### 说明

<span class="type">bool</span> <span
class="methodname">session\_unregister</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="function">session\_unregister</span> unregisters the global
variable named `name` from the current session.

**Warning**

本函数已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

### 参数

`name`  
The variable name.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

> **Note**:
>
> If `$_SESSION` is used, use <span class="function">unset</span> to
> unregister a session variable. Do not <span
> class="function">unset</span> `$_SESSION` itself as this will disable
> the special function of the `$_SESSION` superglobal.

**Caution**

This function does not unset the corresponding global variable for
`name`, it only prevents the variable from being saved as part of the
session. You must call <span class="function">unset</span> to remove the
corresponding global variable.

**Caution**

If you are using `$_SESSION` (or `$HTTP_SESSION_VARS`), do not use <span
class="function">session\_register</span>, <span
class="function">session\_is\_registered</span> and <span
class="function">session\_unregister</span>.

session\_unset
==============

释放所有的会话变量

### 说明

<span class="type">void</span> <span
class="methodname">session\_unset</span> ( <span
class="methodparam">void</span> )

<span class="function">session\_unset</span>
会释放当前会话注册的所有会话变量。

### 返回值

没有返回值。

### 注释

> **Note**:
>
> 如果使用的是 `$_SESSION` (或者PHP 4.0.6或更早版本的
> `$HTTP_SESSION_VARS` ) ，请使用 <span class="function">unset</span> 去
> 注销会话变量，即 *unset ($\_SESSION\['varname'\]);*.

**Caution**

请不要使用*unset($\_SESSION)*来释放整个`$_SESSION`，
因为它将会禁用通过全局`$_SESSION`去注册会话变量

session\_write\_close
=====================

Write session data and end session

### 说明

<span class="type">bool</span> <span
class="methodname">session\_write\_close</span> ( <span
class="methodparam">void</span> )

End the current session and store session data.

Session data is usually stored after your script terminated without the
need to call <span class="function">session\_write\_close</span>, but as
session data is locked to prevent concurrent writes only one script may
operate on a session at any time. When using framesets together with
sessions you will experience the frames loading one by one due to this
locking. You can reduce the time needed to load all the frames by ending
the session as soon as all changes to session variables are done.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                          |
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | The return type of this function is <span class="type">bool</span> now. Formerly, it has been <span class="type">void</span>. |

### 参见

-   The <span class="function">session\_register\_shutdown</span>

**目录**

-   [session\_abort](/ref/session.html#session_abort) — Discard session
    array changes and finish session
-   [session\_cache\_expire](/ref/session.html#session_cache_expire) —
    返回当前缓存的到期时间
-   [session\_cache\_limiter](/ref/session.html#session_cache_limiter) —
    读取/设置缓存限制器
-   [session\_commit](/ref/session.html#session_commit) —
    session\_write\_close 的别名
-   [session\_create\_id](/ref/session.html#session_create_id) — Create
    new session id
-   [session\_decode](/ref/session.html#session_decode) — 解码会话数据
-   [session\_destroy](/ref/session.html#session_destroy) —
    销毁一个会话中的全部数据
-   [session\_encode](/ref/session.html#session_encode) —
    将当前会话数据编码为一个字符串
-   [session\_gc](/ref/session.html#session_gc) — Perform session data
    garbage collection
-   [session\_get\_cookie\_params](/ref/session.html#session_get_cookie_params)
    — 获取会话 cookie 参数
-   [session\_id](/ref/session.html#session_id) — 获取/设置当前会话 ID
-   [session\_is\_registered](/ref/session.html#session_is_registered) —
    检查变量是否在会话中已经注册
-   [session\_module\_name](/ref/session.html#session_module_name) —
    获取/设置会话模块名称
-   [session\_name](/ref/session.html#session_name) — 读取/设置会话名称
-   [session\_regenerate\_id](/ref/session.html#session_regenerate_id) —
    使用新生成的会话 ID 更新现有会话 ID
-   [session\_register\_shutdown](/ref/session.html#session_register_shutdown)
    — 关闭会话
-   [session\_register](/ref/session.html#session_register) — Register
    one or more global variables with the current session
-   [session\_reset](/ref/session.html#session_reset) — Re-initialize
    session array with original values
-   [session\_save\_path](/ref/session.html#session_save_path) —
    读取/设置当前会话的保存路径
-   [session\_set\_cookie\_params](/ref/session.html#session_set_cookie_params)
    — 设置会话 cookie 参数
-   [session\_set\_save\_handler](/ref/session.html#session_set_save_handler)
    — 设置用户自定义会话存储函数
-   [session\_start](/ref/session.html#session_start) —
    启动新会话或者重用现有会话
-   [session\_status](/ref/session.html#session_status) —
    返回当前会话状态
-   [session\_unregister](/ref/session.html#session_unregister) —
    Unregister a global variable from the current session
-   [session\_unset](/ref/session.html#session_unset) —
    释放所有的会话变量
-   [session\_write\_close](/ref/session.html#session_write_close) —
    Write session data and end session
