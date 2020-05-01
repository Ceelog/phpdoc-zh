范例
====

**目录**

-   [curl 基础例子](/curl/examples.html#curl%20基础例子)

curl 基础例子
-------------

只要你编译完的PHP设置了支持 cURL 扩展，你就可以开始使用cURL函数了。使用
cURL 函数的基本思想是先使用 <span class="function">curl\_init</span>
初始化 cURL会话，接着可以通过 <span class="function">curl\_setopt</span>
设置需要的全部选项，然后使用 <span class="function">curl\_exec</span>
来执行会话，当执行完会话后使用 <span class="function">curl\_close</span>
关闭会话。这是一个使用 cURL 函数获取 example.com 主页保存到文件的例子：

**示例 \#1 使用 PHP cURL 模块获取 example.com 的主页**

``` php
<?php

$ch = curl_init("http://www.example.com/");
$fp = fopen("example_homepage.txt", "w");

curl_setopt($ch, CURLOPT_FILE, $fp);
curl_setopt($ch, CURLOPT_HEADER, 0);

curl_exec($ch);
curl_close($ch);
fclose($fp);
?>
```
