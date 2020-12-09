Session 上传进度
================

> **Note**: <span class="simpara"> 此特性自 PHP 5.4.0 后可用。 </span>

当
<a href="/session/setup.html#" class="link">session.upload_progress.enabled</a>
INI 选项开启时，PHP 能够在每一个文件上传时监测上传进度。
这个信息对上传请求自身并没有什么帮助，但在文件上传时应用可以发送一个POST请求到终端（例如通过XHR）来检查这个状态

当一个上传在处理中，同时POST一个与INI中设置的<a href="/session/setup.html#" class="link">session.upload_progress.name</a>同名变量时，上传进度可以在`$_SESSION`中获得。
当PHP检测到这种POST请求时，它会在`$_SESSION`中添加一组数据, 索引是
<a href="/session/setup.html#" class="link">session.upload_progress.prefix</a>
与
<a href="/session/setup.html#" class="link">session.upload_progress.name</a>连接在一起的值。
通常这些键值可以通过读取INI设置来获得，例如

``` php
<?php
$key = ini_get("session.upload_progress.prefix") . ini_get("session.upload_progress.name");
var_dump($_SESSION[$key]);
?>
```

通过将*$\_SESSION\[$key\]\["cancel\_upload"\]*设置为**`true`**，还可以*取消*一个正在处理中的文件上传。
当在同一个请求中上传多个文件，它仅会取消当前正在处理的文件上传和未处理的文件上传，但是不会移除那些已经完成的上传。
当一个上传请求被这么取消时，`$_FILES`中的*error*将会被设置为
**`UPLOAD_ERR_EXTENSION`**。

<a href="/session/setup.html#" class="link">session.upload_progress.freq</a>
和
<a href="/session/setup.html#" class="link">session.upload_progress.min_freq</a>
INI选项控制了上传进度信息应该多久被重新计算一次。
通过合理设置这两个选项的值，这个功能的开销几乎可以忽略不计。

**示例 \#1 样例信息**

一个上传进度数组的结构的例子

``` html
<form action="upload.php" method="POST" enctype="multipart/form-data">
 <input type="hidden" name="<?php echo ini_get("session.upload_progress.name"); ?>" value="123" />
 <input type="file" name="file1" />
 <input type="file" name="file2" />
 <input type="submit" />
</form>
```

在session中存放的数据看上去是这样子的：

``` php
<?php
$_SESSION["upload_progress_123"] = array(
 "start_time" => 1234567890,   // The request time
 "content_length" => 57343257, // POST content length
 "bytes_processed" => 453489,  // Amount of bytes received and processed
 "done" => false,              // true when the POST handler has finished, successfully or not
 "files" => array(
  0 => array(
   "field_name" => "file1",       // Name of the <input/> field
   // The following 3 elements equals those in $_FILES
   "name" => "foo.avi",
   "tmp_name" => "/tmp/phpxxxxxx",
   "error" => 0,
   "done" => true,                // True when the POST handler has finished handling this file
   "start_time" => 1234567890,    // When this file has started to be processed
   "bytes_processed" => 57343250, // Amount of bytes received and processed for this file
  ),
  // An other file, not finished uploading, in the same request
  1 => array(
   "field_name" => "file2",
   "name" => "bar.avi",
   "tmp_name" => NULL,
   "error" => 0,
   "done" => false,
   "start_time" => 1234567899,
   "bytes_processed" => 54554,
  ),
 )
);
```

**Warning**

为了使这个正常工作，web服务器的请求缓冲区需要禁用，否则
PHP可能仅当文件完全上传完成时才能收到文件上传请求。
已知会缓冲这种大请求的程序有Nginx。

**Caution**

这个进度信息是在任意脚本被执行前写入session的，因此通过 <span
class="function">ini\_set</span>或<span
class="function">session\_name</span>修改session名将会导致一个没有上传进度信息的session。
