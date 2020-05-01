data://
=======

数据（RFC 2397）

### 说明

自 PHP 5.2.0 起
`data:`（<a href="http://www.faqs.org/rfcs/rfc2397" class="link external">» RFC 2397</a>）数据流封装器开始有效。

### 用法

-   <span class="simpara">`data://text/plain;base64,`</span>

### 可选项

| 属性                                                                        | 支持 |
|-----------------------------------------------------------------------------|------|
| 受限于 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a>   | No   |
| 受限于 <a href="/filesystem/setup.html#" class="link">allow_url_include</a> | Yes  |
| 允许读取                                                                    | Yes  |
| 允许写入                                                                    | No   |
| 允许追加                                                                    | No   |
| 允许同时读写                                                                | No   |
| 支持 <span class="function">stat</span>                                     | No   |
| 支持 <span class="function">unlink</span>                                   | No   |
| 支持 <span class="function">rename</span>                                   | No   |
| 支持 <span class="function">mkdir</span>                                    | No   |
| 支持 <span class="function">rmdir</span>                                    | No   |

### 范例

**示例 \#1 打印 data:// 的内容**

``` php
<?php
// 打印 "I love PHP"
echo file_get_contents('data://text/plain;base64,SSBsb3ZlIFBIUAo=');
?>
```

**示例 \#2 获取媒体类型**

``` php
<?php
$fp   = fopen('data://text/plain;base64,', 'r');
$meta = stream_get_meta_data($fp);

// 打印 "text/plain"
echo $meta['mediatype'];
?>
```
