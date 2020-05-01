错误信息说明
------------

从 PHP 4.2.0 开始，PHP
将随文件信息数组一起返回一个对应的错误代码。该代码可以在文件上传时生成的文件数组中的
*error* 字段中被找到，也就是 `$_FILES['userfile']['error']`。

**`UPLOAD_ERR_OK`**  
其值为 0，没有错误发生，文件上传成功。

**`UPLOAD_ERR_INI_SIZE`**  
其值为 1，上传的文件超过了 `php.ini` 中
<a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a>
选项限制的值。

**`UPLOAD_ERR_FORM_SIZE`**  
其值为 2，上传文件的大小超过了 HTML 表单中 *MAX\_FILE\_SIZE*
选项指定的值。

**`UPLOAD_ERR_PARTIAL`**  
其值为 3，文件只有部分被上传。

**`UPLOAD_ERR_NO_FILE`**  
其值为 4，没有文件被上传。

**`UPLOAD_ERR_NO_TMP_DIR`**  
其值为 6，找不到临时文件夹。PHP 4.3.10 和 PHP 5.0.3 引进。

**`UPLOAD_ERR_CANT_WRITE`**  
其值为 7，文件写入失败。PHP 5.1.0 引进。

> **Note**:
>
> 以上值在 PHP 4.3.0 之后变成了 PHP 常量。
