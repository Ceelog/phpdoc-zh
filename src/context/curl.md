CURL context options
====================

CURL 上下文选项列表

### 说明

CURL 上下文选项在 <a href="/intro/curl.html" class="link">CURL</a>
扩展被编译（通过 **--with-curlwrappers** configure选项）时可用

### 可选项

`method` <span class="type">string</span>  
**`GET`**，**`POST`**，或者其他远程服务器支持的 HTTP 方法。

默认为 **`GET`**.

`header` <span class="type">string</span>  
额外的请求标头。这个值会覆盖通过其他选项设定的值（如：
*User-agent:*，*Host:*， ，*Authentication:*）。

`user_agent` <span class="type">string</span>  
设置请求时 User-Agent 标头的值。

默认为 `php.ini` 中的
<a href="/filesystem/setup.html#" class="link">user_agent</a> 设定。

`content` <span class="type">string</span>  
在头部之后发送的额外数据。这个选项在 **`GET`** 和 **`HEAD`**
请求中不使用。

`proxy` <span class="type">string</span>  
URI，用于指定代理服务器的地址（例如 *tcp://proxy.example.com:5100*）。

`max_redirects` <span class="type">integer</span>  
最大重定向次数。*1* 或者更小则代表不会跟随重定向。

默认为 *20*.

`curl_verify_ssl_host` <span class="type">boolean</span>  
校验服务器。

默认为 **`false`**

> **Note**:
>
> 这个选项在 HTTP 和 FTP 协议中均可使用。

`curl_verify_ssl_peer` <span class="type">boolean</span>  
要求对使用的SSL证书进行校验。

默认为 **`false`**

> **Note**:
>
> 这个选项在 HTTP 和 FTP 协议中均可使用。

### 范例

**示例 \#1 获取一个页面，并以POST发送数据**

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

### 参见

-   <a href="/context/socket.html" class="xref">套接字上下文选项</a>
