对 PUT 方法的支持
-----------------

PHP 3 和 PHP 4 对 PUT 方法的支持有所不同。在 PHP 4
中，必须使用标准的输入流来读取一个 HTTP PUT 的内容。

**示例 \#1 用 PHP 4 来保存 HTTP PUT 文件**

``` php
<?php
/* PUT data comes in on the stdin stream */
$putdata = fopen("php://stdin", "r");

/* Open a file for writing */
$fp = fopen("myputfile.ext", "w");

/* Read the data 1 KB at a time
   and write to the file */
while ($data = fread($putdata, 1024))
  fwrite($fp, $data);

/* Close the streams */
fclose($fp);
fclose($putdata);
?>
```

> **Note**:
>
> 以下文档的内容仅对 PHP 3 适用。

PHP 提供对诸如 <span class="productname">Netscape Composer</span> 和 W3C
<span class="productname">Amaya</span> 等客户端使用的 HTTP PUT
方法的支持。PUT 请求比文件上传要简单的多，它们一般的形式为：

``` HTTP
PUT /path/filename.html HTTP/1.1
```

这通常意味着远程客户端会将其中的 `/path/filename.html` 存储到 web
目录树。让 Apache 或者 PHP 自动允许所有人覆盖 web
目录树下的任何文件显然是很不明智的。因此，要处理类似的请求，必须先告诉
web 服务器需要用特定的 PHP 脚本来处理该请求。在 Apache 下，可以用
*Script* 选项来设置。它可以被放置到 Apache
配置文件中几乎所有的位置。通常我们把它放置在 \<Directory\> 区域或者
\<Virtualhost\> 区域。可以用如下一行来完成该设置：

    Script PUT /put.php

这将告诉 Apache 将所有对 URI 的 PUT 请求全部发送到 put.php 脚本，这些
URI 必须和 PUT 命令中的内容相匹配。当然，这是建立在 PHP 支持 .php
扩展名，并且 PHP 已经在运行的假设之上。

在 put.php 文件中，可以作如下操作：

``` php
<?php copy($PHP_UPLOADED_FILE_NAME, $DOCUMENT_ROOT . $REQUEST_URI); ?>
```

这将会把文件拷贝到远程客户端请求的位置。可能希望在文件拷贝之前进行一些检查或者对用户认证之类的操作。这里唯一的问题是，当
PHP 接受到 PUT 方法的请求时，它将会把上传的文件储存到和其它用
<a href="/features/file-upload/post-method.html" class="link">POST 方法</a>处理过的文件相同的临时目录。在请求结束时，临时文件将被删除。因此，用来处理
PUT 的 PHP
脚本必须将该文件拷贝到其它的地方。该临时文件的文件名被储存在变量
`$PHP_PUT_FILENAME` 中，也可以通过 `$REQUEST_URI`
变量获得建议的目标文件名（在非 Apache web
服务器上可能会有较大的变化）。该目标文件名是由远程客户端指定的。也可以不听从改客户端的信息，而把所有上传的文件存储到一个特殊的上传目录下。
