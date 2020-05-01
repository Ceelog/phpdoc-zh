POST 方法上传
-------------

本特性可以使用户上传文本和二进制文件。用 PHP
的认证和文件操作函数，可以完全控制允许哪些人上传以及文件上传后怎样处理。

PHP 能够接受任何来自符合 RFC-1867 标准的浏览器（包括 <span
class="productname">Netscape Navigator 3</span> 及更高版本，打了补丁的
<span class="productname">Microsoft Internet Explorer 3</span>
或者更高版本）上传的文件。

> **Note**: **相关的设置**  
>
> 请参阅 `php.ini` 的
> <a href="/ini/core.html#ini.file-uploads" class="link">file_uploads</a>，<a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a>，<a href="/ini/core.html#ini.upload-tmp-dir" class="link">upload_tmp_dir</a><a href="/ini/core.html#ini.post-max-size" class="link">post_max_size</a>
> 以及 <a href="/info/setup.html#" class="link">max_input_time</a>
> 设置选项。

请注意 PHP 也支持 PUT 方法的文件上传，<span class="productname">Netscape
Composer</span> 和 W3C 的 <span class="productname">Amaya</span>
客户端使用这种方法。请参阅<a href="/features/file-upload/put-method.html" class="link">对 PUT 方法的支持</a>以获取更多信息。

**示例 \#1 文件上传表单**

可以如下建立一个特殊的表单来支持文件上传：

``` html
<!-- The data encoding type, enctype, MUST be specified as below -->
<form enctype="multipart/form-data" action="__URL__" method="POST">
    <!-- MAX_FILE_SIZE must precede the file input field -->
    <input type="hidden" name="MAX_FILE_SIZE" value="30000" />
    <!-- Name of input element determines name in $_FILES array -->
    Send this file: <input name="userfile" type="file" />
    <input type="submit" value="Send File" />
</form>
```

以上范例中的 *\_\_URL\_\_* 应该被换掉，指向一个真实的 PHP 文件。

*MAX\_FILE\_SIZE*
隐藏字段（单位为字节）必须放在文件输入字段之前，其值为接收文件的最大尺寸。这是对浏览器的一个建议，PHP
也会检查此项。在浏览器端可以简单绕过此设置，因此不要指望用此特性来阻挡大文件。实际上，PHP
设置中的上传文件最大值是不会失效的。但是最好还是在表单中加上此项目，因为它可以避免用户在花时间等待上传大文件之后才发现文件过大上传失败的麻烦。

> **Note**:
>
> 要确保文件上传表单的属性是
> *enctype="multipart/form-data"*，否则文件上传不了。

全局变量
<a href="/reserved/variables/files.html" class="link">$_FILES</a> 自 PHP
4.1.0 起存在（在更早的版本中用 `$HTTP_POST_FILES`
替代）。此数组包含有所有上传的文件信息。

以上范例中
<a href="/reserved/variables/files.html" class="link">$_FILES</a>
数组的内容如下所示。我们假设文件上传字段的名称如上例所示，为
*userfile*。名称可随意命名。

`$_FILES['userfile']['name']`  
客户端机器文件的原名称。

`$_FILES['userfile']['type']`  
文件的 MIME
类型，如果浏览器提供此信息的话。一个例子是“*image/gif*”。不过此 MIME
类型在 PHP 端并不检查，因此不要想当然认为有这个值。

`$_FILES['userfile']['size']`  
已上传文件的大小，单位为字节。

`$_FILES['userfile']['tmp_name']`  
文件被上传后在服务端储存的临时文件名。

`$_FILES['userfile']['error']`  
和该文件上传相关的<a href="/features/file-upload/errors.html" class="link">错误代码</a>。此项目是在
PHP 4.2.0 版本中增加的。

文件被上传后，默认地会被储存到服务端的默认临时目录中，除非 `php.ini`
中的
<a href="/ini/core.html#ini.upload-tmp-dir" class="link">upload_tmp_dir</a>
设置为其它的路径。服务端的默认临时目录可以通过更改 PHP
运行环境的环境变量 `TMPDIR` 来重新设置，但是在 PHP 脚本内部通过运行
<span class="function">putenv</span>
函数来设置是不起作用的。该环境变量也可以用来确认其它的操作也是在上传的文件上进行的。

**示例 \#2 使文件上传生效**

请查阅函数 <span class="function">is\_uploaded\_file</span> 和 <span
class="function">move\_uploaded\_file</span>
以获取进一步的信息。以下范例处理由表单提供的文件上传。

``` php
<?php
// In PHP versions earlier than 4.1.0, $HTTP_POST_FILES should be used instead
// of $_FILES.

$uploaddir = '/var/www/uploads/';
$uploadfile = $uploaddir . basename($_FILES['userfile']['name']);

echo '<pre>';
if (move_uploaded_file($_FILES['userfile']['tmp_name'], $uploadfile)) {
    echo "File is valid, and was successfully uploaded.\n";
} else {
    echo "Possible file upload attack!\n";
}

echo 'Here is some more debugging info:';
print_r($_FILES);

print "</pre>";

?>
```

接受上传文件的 PHP
脚本为了决定接下来要对该文件进行哪些操作，应该实现任何逻辑上必要的检查。例如可以用
`$_FILES['userfile']['size']` 变量来排除过大或过小的文件，也可以通过
`$_FILES['userfile']['type']`
变量来排除文件类型和某种标准不相符合的文件，但只把这个当作一系列检查中的第一步，因为此值完全由客户端控制而在
PHP 端并不检查。自 PHP 4.2.0 起，还可以通过
`$_FILES['userfile']['error']`
变量来根据不同的<a href="/features/file-upload/errors.html" class="link">错误代码</a>来计划下一步如何处理。不管怎样，要么将该文件从临时目录中删除，要么将其移动到其它的地方。

如果表单中没有选择上传的文件，则 PHP 变量 `$_FILES['userfile']['size']`
的值将为 0，`$_FILES['userfile']['tmp_name']` 将为空。

如果该文件没有被移动到其它地方也没有被改名，则该文件将在表单请求结束时被删除。

**示例 \#3 上传一组文件**

PHP 的
<a href="/faq/html.html#faq.html.arrays" class="link">HTML 数组特性</a>甚至支持文件类型。

``` html
<form action="" method="post" enctype="multipart/form-data">
<p>Pictures:
<input type="file" name="pictures[]" />
<input type="file" name="pictures[]" />
<input type="file" name="pictures[]" />
<input type="submit" value="Send" />
</p>
</form>
```

``` php
<?php
foreach ($_FILES["pictures"]["error"] as $key => $error) {
    if ($error == UPLOAD_ERR_OK) {
        $tmp_name = $_FILES["pictures"]["tmp_name"][$key];
        $name = $_FILES["pictures"]["name"][$key];
        move_uploaded_file($tmp_name, "data/$name");
    }
}
?>
```
