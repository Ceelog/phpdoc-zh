http://
=======

https://
========

访问 HTTP(s) 网址

### 说明

允许通过 HTTP 1.0 的 GET方法，以只读访问文件或资源。 HTTP 请求会附带一个
*Host:* 头，用于兼容基于域名的虚拟主机。 如果在你的 `php.ini`
文件中或字节流上下文（context）配置了
<a href="/filesystem/setup.html#" class="link">user_agent</a>
字符串，它也会被包含在请求之中。

数据流允许读取资源的 *body*，而 headers 则储存在了
`$http_response_header` 变量里。

如果需要知道文档资源来自哪个 URL（经过所有重定向的处理后），
需要处理数据流返回的系列响应报头（response headers）。

The <a href="/filesystem/setup.html#" class="link">from</a> directive
will be used for the *From:* header if set and not overwritten by the
<a href="/context.html" class="xref">上下文（Context）选项和参数</a>.

### 用法

-   <span class="simpara">`http://example.com`</span>
-   <span
    class="simpara">`http://example.com/file.php?var1=val1&var2=val2`</span>
-   <span class="simpara">`http://user:password@example.com`</span>
-   <span class="simpara">`https://example.com`</span>
-   <span
    class="simpara">`https://example.com/file.php?var1=val1&var2=val2`</span>
-   <span class="simpara">`https://user:password@example.com`</span>

### 可选项

| 属性                                                                       | 支持 |
|----------------------------------------------------------------------------|------|
| 受 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> 限制 | Yes  |
| 允许读取                                                                   | Yes  |
| 允许写入                                                                   | No   |
| 允许添加                                                                   | No   |
| 允许同时读和写                                                             | N/A  |
| 支持 <span class="function">stat</span>                                    | No   |
| 支持 <span class="function">unlink</span>                                  | No   |
| 支持 <span class="function">rename</span>                                  | No   |
| 支持 <span class="function">mkdir</span>                                   | No   |
| 支持 <span class="function">rmdir</span>                                   | No   |

### 更新日志

| 版本  | 说明                                                     |
|-------|----------------------------------------------------------|
| 4.3.7 | 检测 IIS 服务器避免 *"SSL: Fatal Protocol Error"* 错误。 |
| 4.3.0 | 添加 *https://*。                                        |
| 4.0.5 | 增加了对重定向的支持。                                   |

### 范例

**示例 \#1 检测重定向后最终的 URL**

``` php
<?php
$url = 'http://www.example.com/redirecting_page.php';

$fp = fopen($url, 'r');

$meta_data = stream_get_meta_data($fp);
foreach ($meta_data['wrapper_data'] as $response) {

    /* 我们是否被重定向了？ */
    if (strtolower(substr($response, 0, 10)) == 'location: ') {

        /* 更新我们被重定向后的 $url */
        $url = substr($response, 10);
    }

}

?>
```

### 注释

> **Note**: <span class="simpara">
> <a href="/book/openssl.html" class="link">openssl</a>
> 扩展启用后才能够支持 HTTPS 协议。 </span>

HTTP 连接是只读的；还不支持对一个 HTTP 资源进行写数据或者复制文件。

比如发送 *POST* 和 *PUT* 请求， 可以在
<a href="/context/http.html" class="link">HTTP Contexts</a>
的支持下实现。

### 参见

-   <a href="/context/http.html" class="xref">HTTP context 选项</a>
-   `$http_response_header`
-   <span class="function">stream\_get\_meta\_data</span>
