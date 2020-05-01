上传多个文件
------------

可以对 *input* 域使用不同的 *name* 来上传多个文件。

PHP
支持同时上传多个文件并将它们的信息自动以数组的形式组织。要完成这项功能，需要在
HTML 表单中对文件上传域使用和多选框与复选框相同的数组式提交语法。

> **Note**:
>
> 对多文件上传的支持是在 PHP 3.0.10 版本添加的。

**示例 \#1 上传多个文件**

``` html
<form action="file-upload.php" method="post" enctype="multipart/form-data">
  Send these files:<br />
  <input name="userfile[]" type="file" /><br />
  <input name="userfile[]" type="file" /><br />
  <input type="submit" value="Send files" />
</form>
```

当以上表单被提交后，数组
`$_FILES['userfile']`，`$_FILES['userfile']['name']` 和
`$_FILES['userfile']['size']` 将被初始化（在 PHP 4.1.0 以前版本是
`$HTTP_POST_FILES`）。如果
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
的设置为
on，则和文件上传相关的全局变量也将被初始化。所有这些提交的信息都将被储存到以数字为索引的数组中。

例如，假设名为 `/home/test/review.html` 和 `/home/test/xwp.out`
的文件被提交，则 `$_FILES['userfile']['name'][0]` 的值将是
`review.html`，而 `$_FILES['userfile']['name'][1]` 的值将是
`xwp.out`。类似的，`$_FILES['userfile']['size'][0]` 将包含文件
`review.html` 的大小，依此类推。

此外也同时设置了
`$_FILES['userfile']['name'][0]`，`$_FILES['userfile']['tmp_name'][0]`，`$_FILES['userfile']['size'][0]`
以及 `$_FILES['userfile']['type'][0]`。
