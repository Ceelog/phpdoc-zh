使用远程文件
============

只要在 `php.ini` 文件中激活了 **allow\_url\_fopen**
选项，就可以在大多数需要用文件名作为参数的函数中使用 HTTP 和 FTP 的 URL
来代替文件名。同时，也可以在 <span
class="function">include</span>、<span
class="function">include\_once</span>、<span
class="function">require</span> 及 <span
class="function">require\_once</span> 语句中使用 URL。PHP
所支持协议的更多信息参见<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>。

> **Note**:
>
> 要在 PHP 4.0.3 及其更早的版本中使用 URL 封装协议，需要在编译时用
> **--enable-url-fopen-wrapper** 参数来配置 PHP。

> **Note**:
>
> Windows 版本的 PHP 4.3 版之前不支持以下函数的远程访问：<span
> class="function">include</span>，<span
> class="function">include\_once</span>，<span
> class="function">require</span>，<span
> class="function">require\_once</span>
> 以及<a href="/ref/image.html" class="xref">GD 和图像处理 函数</a>中的
> imagecreatefromXXX 函数。

例如，可以用以下范例来打开远程 web
服务器上的文件，解析需要的输出数据，然后将这些数据用在数据库的检索中，或者简单地以和自己网站其它页面相同的风格输出其内容。

**示例 \#1 获取远程文件的标题**

``` php
<?php
$file = fopen ("http://www.example.com/", "r");
if (!$file) {
    echo "<p>Unable to open remote file.\n";
    exit;
}
while (!feof ($file)) {
    $line = fgets ($file, 1024);
    /* This only works if the title and its tags are on one line */
    if (eregi ("<title>(.*)</title>", $line, $out)) {
        $title = $out[1];
        break;
    }
}
fclose($file);
?>
```

如果有合法的访问权限，以一个用户的身份和某 FTP
服务器建立了链接，还可以向该 FTP
服务器端的文件进行写操作。仅能用该方法来创建新的文件；如果尝试覆盖已经存在的文件，<span
class="function">fopen</span> 函数的调用将会失败。

要以“anonymous”以外的用户名连接服务器，需要指明用户名（可能还有密码），例如“ftp://user:password@ftp.example.com/path/to/file”（也可以在通过需要
Basic 认证的 HTTP 协议访问远程文件时使用相同的语法）。

**示例 \#2 将数据保存到远程服务器**

``` php
<?php
$file = fopen ("ftp://ftp.example.com/incoming/outputfile", "w");
if (!$file) {
    echo "<p>Unable to open remote file for writing.\n";
    exit;
}
/* Write the data here. */
fwrite ($file, $_SERVER['HTTP_USER_AGENT'] . "\n");
fclose ($file);
?>
```

> **Note**:
>
> 或许可以从以上范例中得到启发，用该技术来存储远程日志文件。但是正如以上提到的，在用
> <span class="function">fopen</span> 方式打开的 URL
> 中，仅能对新文件进行写操作。如果远程文件已经存在则 <span
> class="function">fopen</span>
> 函数的操作将会失败。要做类似于分布式日志的事，可以参考 <span
> class="function">syslog</span> 函数。
