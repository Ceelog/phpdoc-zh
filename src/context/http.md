HTTP context 选项
=================

HTTP context 的选项列表

### 说明

提供给 *http://* 和 *https://* 传输协议的 context 选项。 transports.

### 可选项

`method` <span class="type">string</span>  
远程服务器支持的 **`GET`**，**`POST`** 或其它 HTTP 方法。

默认值是 **`GET`**。

`header` <span class="type">string</span>  
请求期间发送的额外 header 。在此选项的值将覆盖其他值 （诸如
*User-agent:*， *Host:* 和 *Authentication:*）。

`user_agent` <span class="type">string</span>  
要发送的 header *User-Agent:* 的值。如果在上面的 *header* context
选项中没有指定 user-agent，此值将被使用。

默认使用 `php.ini` 中设置的
<a href="/filesystem/setup.html#" class="link">user_agent</a>。

`content` <span class="type">string</span>  
在 header 后面要发送的额外数据。通常使用POST或PUT请求。

`proxy` <span class="type">string</span>  
URI 指定的代理服务器的地址。(e.g. *tcp://proxy.example.com:5100*).

`request_fulluri` <span class="type">boolean</span>  
当设置为 **`true`** 时，在构建请求时将使用整个 URI 。(i.e. *GET
http://www.example.com/path/to/file.html HTTP/1.0*)。
虽然这是一个非标准的请求格式，但某些代理服务器需要它。

默认值是 **`false`**.

`follow_location` <span class="type">integer</span>  
跟随 *Location* header 的重定向。设置为 *0* 以禁用。

默认值是 *1*。

`max_redirects` <span class="type">integer</span>  
跟随重定向的最大次数。值为 *1* 或更少则意味不跟随重定向。

默认值是 *20*。

`protocol_version` <span class="type">float</span>  
HTTP 协议版本。

默认值是 *1.0*。

> **Note**:
>
> PHP 5.3.0 以前的版本没有实现分块传输解码。 如果此值设置为 *1.1* ，与
> *1.1* 的兼容将是你的责任。

`timeout` <span class="type">float</span>  
读取超时时间，单位为秒（s），用 <span class="type">float</span>
指定(e.g. *10.5*)。

默认使用 `php.ini` 中设置的
<a href="/filesystem/setup.html#" class="link">default_socket_timeout</a>。

`ignore_errors` <span class="type">boolean</span>  
即使是故障状态码依然获取内容。

默认值为 **`false`**.

### 更新日志

| 版本   | 说明                                                                         |
|--------|------------------------------------------------------------------------------|
| 5.3.4  | 添加 `follow_location`。                                                     |
| 5.3.0  | 当 `protocol_version` 设置为 *1.1* 时支持分块传输解码。                      |
| 5.2.10 | 添加 `ignore_errors`。                                                       |
| 5.2.10 | `header` 现在可以是一个数字索引的 <span class="type">array</span>。          |
| 5.2.1  | 添加 `timeout`。                                                             |
| 5.1.0  | Added HTTPS proxying through HTTP proxies. 添加经由 HTTP 代理的 HTTPS 代理。 |
| 5.1.0  | 添加 `max_redirects`。                                                       |
| 5.1.0  | 添加 `protocol_version`。                                                    |

### 范例

**示例 \#1 获取一个页面并发送 POST 数据**

``` php
<?php

$postdata = http_build_query(
    array(
        'var1' => 'some content',
        'var2' => 'doh'
    )
);

$opts = array('http' =>
    array(
        'method'  => 'POST',
        'header'  => 'Content-type: application/x-www-form-urlencoded',
        'content' => $postdata
    )
);

$context = stream_context_create($opts);

$result = file_get_contents('http://example.com/submit.php', false, $context);

?>
```

**示例 \#2 忽略重定向并获取 header 和内容**

``` php
<?php

$url = "http://www.example.org/header.php";

$opts = array('http' =>
    array(
        'method' => 'GET',
        'max_redirects' => '0',
        'ignore_errors' => '1'
    )
);

$context = stream_context_create($opts);
$stream = fopen($url, 'r', false, $context);

// header information as well as meta data
// about the stream
var_dump(stream_get_meta_data($stream));

// actual data at $url
var_dump(stream_get_contents($stream));
fclose($stream);
?>
```

### 注释

> **Note**: **Underlying socket stream context options**  
> <span class="simpara"> Additional context options may be supported by
> the
> <a href="/transports/inet.html" class="link">underlying transport</a>
> For *http://* streams, refer to context options for the *tcp://*
> transport. For *https://* streams, refer to context options for the
> *ssl://* transport. </span>

> **Note**: **HTTP status line**  
> <span class="simpara"> When this stream wrapper follows a redirect,
> the *wrapper\_data* returned by <span
> class="function">stream\_get\_meta\_data</span> might not necessarily
> contain the HTTP status line that actually applies to the content data
> at index *0*. </span>
>
>     array (
>       'wrapper_data' =>
>       array (
>         0 => 'HTTP/1.0 301 Moved Permantenly',
>         1 => 'Cache-Control: no-cache',
>         2 => 'Connection: close',
>         3 => 'Location: http://example.com/foo.jpg',
>         4 => 'HTTP/1.1 200 OK',
>         ...
>
> <span class="simpara"> The first request returned a *301* (permanent
> redirect), so the stream wrapper automatically followed the redirect
> to get a *200* response (index = *4*). </span>

### 参见

-   <a href="/wrappers/http.html" class="xref">http://</a>
-   <a href="/context/socket.html" class="xref">套接字上下文选项</a>
-   <a href="/context/ssl.html" class="xref">SSL 上下文选项</a>
