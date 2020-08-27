apache\_child\_terminate
========================

在本次请求结束后终止 apache 子进程

### 说明

<span class="type">bool</span> <span
class="methodname">apache\_child\_terminate</span> ( <span
class="methodparam">void</span> )

<span class="function">apache\_child\_terminate</span> 将把运行当前 PHP
请求的 Apache 子进程注册为终止状态，一旦结束 PHP
代码的运行此进程将终止。可以用在占用大量内存的脚本后面来终止该进程，因为通常内存只在内部释放而不会还给操作系统。

### 返回值

如果 PHP 以 Apache 1 模块方式运行，且 Apache
的版本是非多线程的，以及激活了 PHP 指令.
<a href="/apache/setup.html#" class="link">child_terminate</a>，则返回
**`TRUE`**。如果不满足上述条件则返回 **`FALSE`** 并生成一条
**`E_WARNING`** 级的错误信息。

### 更新日志

| 版本  | 说明                                                                            |
|-------|---------------------------------------------------------------------------------|
| 5.4.0 | 该函数目前也可以用于FastCGI模式了。以前，它仅在PHP作为Apapche的模块安装时支持。 |

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

### 参见

-   <span class="function">exit</span>

apache\_get\_modules
====================

获得已加载的Apache模块列表

### 说明

<span class="type">array</span> <span
class="methodname">apache\_get\_modules</span> ( <span
class="methodparam">void</span> )

获得已加载的Apache模块列表。

### 返回值

包含已加载的Apache模块的<span class="type">数组</span>.

### 更新日志

| 版本  | 说明                                                                                    |
|-------|-----------------------------------------------------------------------------------------|
| 5.0.0 | 可用于Apache 1或PHP Apache 2 *filter* API。 在此之前, 只可用于 Apache 2 *handler* API。 |

### 范例

**示例 \#1 <span class="function">apache\_get\_modules</span> 示例**

``` php
<?php
print_r(apache_get_modules());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => core
        [1] => http_core
        [2] => mod_so
        [3] => sapi_apache2
        [4] => mod_mime
        [5] => mod_rewrite
    )

apache\_get\_version
====================

获得Apache版本信息

### 说明

<span class="type">string</span> <span
class="methodname">apache\_get\_version</span> ( <span
class="methodparam">void</span> )

获得Apache版本信息。

### 返回值

成功时返回 Apache 版本信息 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 4.3.4 | 可用于 Apache 1.              |
| 5.0.0 | 可用于 Apache 2 *filter* API. |

### 范例

**示例 \#1 <span class="function">apache\_get\_version</span> example**

``` php
<?php
$version = apache_get_version();
echo "$version\n";
?>
```

以上例程的输出类似于：

    Apache/1.3.29 (Unix) PHP/4.3.4 

### 参见

-   <span class="function">phpinfo</span>

apache\_getenv
==============

获取 Apache subprocess\_env 变量

### 说明

<span class="type">string</span> <span
class="methodname">apache\_getenv</span> ( <span
class="methodparam"><span class="type">string</span> `$variable`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$walk_to_top`<span class="initializer"> = false</span></span> \] )

获取 `variable` 指定的环境变量。

此函数需要 Apache 2 否则为 undefined。

### 参数

`variable`  
Apache 环境变量

`walk_to_top`  
是否获取对Apache各层可用的顶层变量

### 返回值

成功时返回 Apache 环境变量值，失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">apache\_getenv</span> example**

该示例显示如何取得 Apache 环境变量 `SERVER_ADDR`的值。

``` php
<?php
$ret = apache_getenv("SERVER_ADDR");
echo $ret;
?>
```

以上例程的输出类似于：

    42.24.42.240

### 参见

-   <span class="function">apache\_setenv</span>
-   <span class="function">getenv</span>
-   <a href="/language/variables/superglobals.html" class="link">Superglobals</a>

apache\_lookup\_uri
===================

对指定的 URI 执行部分请求并返回所有有关信息

### 说明

<span class="type">object</span> <span
class="methodname">apache\_lookup\_uri</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

本函数对一个 URL 执行部分请求。取得所有有关给定资源的重要信息后就停手。

仅在将 PHP 安装在 Netscape/iPlanet/SunONE Web 服务器，并以 Apache
模块运行时，才支持此函数。参考
<a href="/book/nsapi.html" class="link">NSAPI server module</a>。

### 参数

`filename`  
被请求的文件名（URI）。

### 返回值

一个有关 URI 信息的 <span class="type">object</span>。此 <span
class="type">object</span> 的属性有：

-   status
-   the\_request
-   status\_line
-   method
-   content\_type
-   handler
-   uri
-   filename
-   path\_info
-   args
-   boundary
-   no\_cache
-   no\_local\_copy
-   allowed
-   send\_bodyct
-   bytes\_sent
-   byterange
-   clength
-   unparsed\_uri
-   mtime
-   request\_time

### 范例

**示例 \#1 <span class="function">apache\_lookup\_uri</span> 例子**

``` php
<?php
$info = apache_lookup_uri('index.php?var=value');
print_r($info);

if (file_exists($info->filename)) {
    echo 'file exists!';
}
?>
```

以上例程的输出类似于：

    stdClass Object
    (
        [status] => 200
        [the_request] => GET /dir/file.php HTTP/1.1
        [method] => GET
        [mtime] => 0
        [clength] => 0
        [chunked] => 0
        [content_type] => application/x-httpd-php
        [no_cache] => 0
        [no_local_copy] => 1
        [unparsed_uri] => /dir/index.php?var=value
        [uri] => /dir/index.php
        [filename] => /home/htdocs/dir/index.php
        [args] => var=value
        [allowed] => 0
        [sent_bodyct] => 0
        [bytes_sent] => 0
        [request_time] => 1074282764
    )
    file exists!

apache\_note
============

取得或设置 apache 请求记录

### 说明

<span class="type">string</span> <span
class="methodname">apache\_note</span> ( <span class="methodparam"><span
class="type">string</span> `$note_name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$note_value`<span
class="initializer"> = ""</span></span> \] )

这个函数是 Apache *table\_get* 和 *table\_set* 的包装。
它编辑了请求中存在的 notes 表。 这个表的目的是允许 Apache 模块进行通讯。

<span class="function">apache\_note</span>
的主要用途是在同一个请求中，从一个模块传递信息到另一个模块。

### 参数

`note_name`  
note 名。

`note_value`  
note 值。

### 返回值

如果只有一个参数调用，则返回记录 *note\_name*
的当前值。如果用两个参数调用，则将记录 *note\_name* 的值设为
*note\_value* 并返回记录 *note\_name*
的前一个值。如果未能获取记录，则返回 **`FALSE`**。

### 范例

**示例 \#1 Passing information between PHP and Perl**

``` php
<?php

apache_note('name', 'Fredrik Ekengren');

// Call perl script
virtual("/perl/some_script.pl");

$result = apache_note("resultdata");
?>
```

``` perl
# Get Apache request object
my $r = Apache->request()->main();

# Get passed data
my $name = $r->notes('name');

# some processing

# Pass result back to PHP
$r->notes('resultdata', $result);
```

**示例 \#2 Logging values in access.log**

``` php
<?php

apache_note('sessionID', session_id());

?>
```

``` apache
# "%{sessionID}n" can be used in the LogFormat directive
```

### 参见

-   <span class="function">virtual</span>

apache\_request\_headers
========================

获取全部 HTTP 请求头信息

### 说明

<span class="type">array</span> <span
class="methodname">apache\_request\_headers</span> ( <span
class="methodparam">void</span> )

获取当前请求的所有请求头信息

### 返回值

包含当前请求所有头信息的数组，失败返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明                                                             |
|-------|------------------------------------------------------------------|
| 5.5.7 | 此函数可用于 CLI server。                                        |
| 5.4.0 | 此函数可用于 FastCGI。 此前仅在PHP以 Apache 模块方式运行时支持。 |

### 范例

**示例 \#1 <span class="function">apache\_request\_headers</span> 示例**

``` php
<?php
$headers = apache_request_headers();

foreach ($headers as $header => $value) {
    echo "$header: $value <br />\n";
}
?>
```

以上例程的输出类似于：

    Accept: */*
    Accept-Language: en-us
    Accept-Encoding: gzip, deflate
    User-Agent: Mozilla/4.0
    Host: www.example.com
    Connection: Keep-Alive

### 注释

> **Note**:
>
> 你也可以试图从环境变量中读取普通CGI变量，PHP以<span
> class="productname">Apache</span>模块方式运行时有可能无法获得。使用<span
> class="function">phpinfo</span>获得可读取的变量列表。
> <a href="/language/variables/predefined.html" class="link">环境变量</a>.

### 参见

-   <span class="function">apache\_response\_headers</span>

apache\_reset\_timeout
======================

重置 Apache 写入计时器

### 说明

<span class="type">bool</span> <span
class="methodname">apache\_reset\_timeout</span> ( <span
class="methodparam">void</span> )

<span class="function">apache\_reset\_timeout</span> 重置 Apache
写入计时器， 缺省为 300 秒. 通过 *set\_time\_limit(0);
ignore\_user\_abort(true)* 和定期地调用 <span
class="function">apache\_reset\_timeout</span>，Apache理论上可永远运行

此函数需要 Apache 1.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**: <span class="simpara">当 PHP 运行在
> <a href="/features/safe-mode.html" class="link">安全模式</a>
> 时，不能使用此函数。</span>

### 参见

-   <span class="function">set\_time\_limit</span>
-   <span class="function">ignore\_user\_abort</span>

apache\_response\_headers
=========================

获得全部 HTTP 响应头信息

### 说明

<span class="type">array</span> <span
class="methodname">apache\_response\_headers</span> ( <span
class="methodparam">void</span> )

获得全部 HTTP 响应头信息。

### 返回值

成功时返回包含全部 Apache 响应头信息的数组， 或者在失败时返回
**`FALSE`**.

### 更新日志

| 版本  | 说明                                                             |
|-------|------------------------------------------------------------------|
| 5.5.7 | 此函数可用于 CLI server.                                         |
| 5.4.0 | 此函数可用于 FastCGI。 此前仅在PHP以 Apache 模块方式运行时支持。 |
| 4.3.3 |                                                                  |

### 范例

**示例 \#1 <span class="function">apache\_response\_headers</span>
示例**

``` php
<?php
print_r(apache_response_headers());
?>
```

以上例程的输出类似于：

    Array
    (
        [Accept-Ranges] => bytes
        [X-Powered-By] => PHP/4.3.8
    )

### 参见

-   <span class="function">apache\_request\_headers</span>
-   <span class="function">headers\_sent</span>
-   <span class="function">headers\_list</span>

apache\_setenv
==============

设置 Apache 子进程环境变量

### 说明

<span class="type">bool</span> <span
class="methodname">apache\_setenv</span> ( <span
class="methodparam"><span class="type">string</span> `$variable`</span>
, <span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$walk_to_top`<span class="initializer"> =
false</span></span> \] )

<span class="function">apache\_setenv</span> 设置由`variable`指定的
Apache 环境变量值。

> **Note**:
>
> 当设置了某 Apache 环境变量, 相应的 `$_SERVER` 变量不会改变。

### 参数

`variable`  
将被设置的环境变量。

`value`  
新 `variable` 值。

`walk_to_top`  
是否将所设置的顶层变量应用到所有 Apache 层。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 使用 <span class="function">apache\_setenv</span> 设置一个
Apache 环境变量**

``` php
<?php
apache_setenv("EXAMPLE_VAR", "Example Value");
?>
```

### 注释

> **Note**:
>
> <span class="function">apache\_setenv</span> 可与 <span
> class="function">apache\_getenv</span>
> 配合使用，以在不同页面间传递变量，或将 PHP 脚本中已设置变量传入 Server
> Side Includes (.shtml)页面。

### 参见

-   <span class="function">apache\_getenv</span>

getallheaders
=============

获取全部 HTTP 请求头信息

### 说明

<span class="type">array</span> <span
class="methodname">getallheaders</span> ( <span
class="methodparam">void</span> )

获取当前请求的所有请求头信息。

此函数是 <span class="function">apache\_request\_headers</span>的别名。
请阅读 <span class="function">apache\_request\_headers</span>
文档获得更多信息。

### 返回值

包含当前请求所有头信息的数组，失败返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明                                                             |
|-------|------------------------------------------------------------------|
| 5.5.7 | 此函数可用于 CLI server。                                        |
| 5.4.0 | 此函数可用于 FastCGI。 此前仅在PHP以 Apache 模块方式运行时支持。 |
| 4.3.0 | 4.3.0                                                            |

### 范例

**示例 \#1 <span class="function">getallheaders</span> 示例**

``` php
<?php

foreach (getallheaders() as $name => $value) {
    echo "$name: $value\n";
}

?>
```

### 参见

-   <span class="function">apache\_response\_headers</span>

virtual
=======

执行 Apache 子请求

### 说明

<span class="type">bool</span> <span class="methodname">virtual</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

<span class="function">virtual</span> 是一个 Apache 特有函数， 类似于
*mod\_include* 中的 *\<!--\#include virtual...--\>*。 它执行一个 Apache
子请求。可用于包含一个 CGI 脚本或 `.shtml` 文件，或任何其它可通过 Apache
解析的请求。注意对一个 CGI 脚本，该脚本 生成合法的 CGI 头，至少必须
生成*Content-Type* 头。

为运行子请求，所有缓冲将中止并刷新至浏览器，包括头信息。

仅在将 PHP 安装在 Netscape/iPlanet/SunONE Web 服务器，并以 Apache
模块运行时，才支持此函数。参考
<a href="/book/nsapi.html" class="link">NSAPI server module</a>。

### 参数

`filename`  
virtual命令将执行的文件

### 返回值

成功执行 virtual 命令，或失败时返回 **`FALSE`** 。

### 范例

示例请看 <span class="function">apache\_note</span> 。

### 注释

**Warning**

查询字符串可被传递至被包含文件，但是 `$_GET` 是拷贝于父文件，仅有
`$_SERVER['QUERY_STRING']` 将填充传递入的查询字符串。
且此查询字符串只在使用 Apache 2 时被填充。 此请求文件将不会显示在 Apache
访问日志中。

> **Note**:
>
> 在被请求文件中设置的环境变量在原请求文件中不可见。

### 参见

-   <span class="function">apache\_note</span>

**目录**

-   [apache\_child\_terminate](/ref/apache.html#apache_child_terminate)
    — 在本次请求结束后终止 apache 子进程
-   [apache\_get\_modules](/ref/apache.html#apache_get_modules) —
    获得已加载的Apache模块列表
-   [apache\_get\_version](/ref/apache.html#apache_get_version) —
    获得Apache版本信息
-   [apache\_getenv](/ref/apache.html#apache_getenv) — 获取 Apache
    subprocess\_env 变量
-   [apache\_lookup\_uri](/ref/apache.html#apache_lookup_uri) — 对指定的
    URI 执行部分请求并返回所有有关信息
-   [apache\_note](/ref/apache.html#apache_note) — 取得或设置 apache
    请求记录
-   [apache\_request\_headers](/ref/apache.html#apache_request_headers)
    — 获取全部 HTTP 请求头信息
-   [apache\_reset\_timeout](/ref/apache.html#apache_reset_timeout) —
    重置 Apache 写入计时器
-   [apache\_response\_headers](/ref/apache.html#apache_response_headers)
    — 获得全部 HTTP 响应头信息
-   [apache\_setenv](/ref/apache.html#apache_setenv) — 设置 Apache
    子进程环境变量
-   [getallheaders](/ref/apache.html#getallheaders) — 获取全部 HTTP
    请求头信息
-   [virtual](/ref/apache.html#virtual) — 执行 Apache 子请求
