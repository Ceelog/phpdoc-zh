Client URL 库
=============

**目录**

-   [简介](/intro/curl.html)
-   [安装／配置](/curl/setup.html)
    -   [需求](/curl/setup.html#需求)
    -   [安装](/curl/setup.html#安装)
    -   [运行时配置](/curl/setup.html#运行时配置)
    -   [资源类型](/curl/setup.html#资源类型)
-   [预定义常量](/curl/constants.html)
-   [范例](/curl/examples.html)
    -   [curl 基础例子](/curl/examples.html#curl%20基础例子)
-   [cURL 函数](/ref/curl.html)
    -   [curl\_close](/ref/curl.html#curl_close) — 关闭 cURL 会话
    -   [curl\_copy\_handle](/ref/curl.html#curl_copy_handle) —
        复制一个cURL句柄和它的所有选项
    -   [curl\_errno](/ref/curl.html#curl_errno) —
        返回最后一次的错误代码
    -   [curl\_error](/ref/curl.html#curl_error) —
        返回当前会话最后一次错误的字符串
    -   [curl\_escape](/ref/curl.html#curl_escape) — 使用 URL
        编码给定的字符串
    -   [curl\_exec](/ref/curl.html#curl_exec) — 执行 cURL 会话
    -   [curl\_file\_create](/ref/curl.html#curl_file_create) — 创建一个
        CURLFile 对象
    -   [curl\_getinfo](/ref/curl.html#curl_getinfo) —
        获取一个cURL连接资源句柄的信息
    -   [curl\_init](/ref/curl.html#curl_init) — 初始化 cURL 会话
    -   [curl\_multi\_add\_handle](/ref/curl.html#curl_multi_add_handle)
        — 向curl批处理会话中添加单独的curl句柄
    -   [curl\_multi\_close](/ref/curl.html#curl_multi_close) —
        关闭一组cURL句柄
    -   [curl\_multi\_errno](/ref/curl.html#curl_multi_errno) —
        返回上一次 curl 批处理的错误码
    -   [curl\_multi\_exec](/ref/curl.html#curl_multi_exec) — 运行当前
        cURL 句柄的子连接
    -   [curl\_multi\_getcontent](/ref/curl.html#curl_multi_getcontent)
        — 如果设置了CURLOPT\_RETURNTRANSFER，则返回获取的输出的文本流
    -   [curl\_multi\_info\_read](/ref/curl.html#curl_multi_info_read) —
        获取当前解析的cURL的相关传输信息
    -   [curl\_multi\_init](/ref/curl.html#curl_multi_init) —
        返回一个新cURL批处理句柄
    -   [curl\_multi\_remove\_handle](/ref/curl.html#curl_multi_remove_handle)
        — 移除cURL批处理句柄资源中的某个句柄资源
    -   [curl\_multi\_select](/ref/curl.html#curl_multi_select) —
        等待所有cURL批处理中的活动连接
    -   [curl\_multi\_setopt](/ref/curl.html#curl_multi_setopt) — 为
        cURL 并行处理设置一个选项
    -   [curl\_multi\_strerror](/ref/curl.html#curl_multi_strerror) —
        返回字符串描述的错误代码
    -   [curl\_pause](/ref/curl.html#curl_pause) —
        暂停和取消暂停一个连接。
    -   [curl\_reset](/ref/curl.html#curl_reset) — 重置一个 libcurl
        会话句柄的所有的选项
    -   [curl\_setopt\_array](/ref/curl.html#curl_setopt_array) — 为
        cURL 传输会话批量设置选项
    -   [curl\_setopt](/ref/curl.html#curl_setopt) — 设置 cURL 传输选项
    -   [curl\_share\_close](/ref/curl.html#curl_share_close) — 关闭
        cURL 共享句柄
    -   [curl\_share\_errno](/ref/curl.html#curl_share_errno) — 返回共享
        curl 句柄的最后一次错误号
    -   [curl\_share\_init](/ref/curl.html#curl_share_init) — 初始化一个
        cURL 共享句柄。
    -   [curl\_share\_setopt](/ref/curl.html#curl_share_setopt) — 为
        cURL 共享句柄设置选项。
    -   [curl\_share\_strerror](/ref/curl.html#curl_share_strerror) —
        返回错误号对应的错误消息
    -   [curl\_strerror](/ref/curl.html#curl_strerror) —
        返回错误代码的字符串描述
    -   [curl\_unescape](/ref/curl.html#curl_unescape) — 解码给定的 URL
        编码的字符串
    -   [curl\_version](/ref/curl.html#curl_version) — 获取 cURL
        版本信息
-   [CURLFile](/class/curlfile.html) — CURLFile 类
    -   [CURLFile::\_\_construct](/class/curlfile.html#CURLFile::__construct)
        — 创建 CURLFile 对象
    -   [CURLFile::getFilename](/class/curlfile.html#CURLFile::getFilename)
        — 获取被上传文件的 文件名
    -   [CURLFile::getMimeType](/class/curlfile.html#CURLFile::getMimeType)
        — 获取被上传文件的 MIME 类型
    -   [CURLFile::getPostFilename](/class/curlfile.html#CURLFile::getPostFilename)
        — 获取 POST 请求时使用的 文件名
    -   [CURLFile::setMimeType](/class/curlfile.html#CURLFile::setMimeType)
        — 设置被上传文件的 MIME 类型
    -   [CURLFile::setPostFilename](/class/curlfile.html#CURLFile::setPostFilename)
        — 设置 POST 请求时使用的文件名

简介
----

<span class="classname">CURLFile</span> 应该与选项
**`CURLOPT_POSTFIELDS`** 一同使用用于上传文件。

类摘要
------

**CURLFile**

<span class="ooclass"> class **CURLFile** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$name` ;

<span class="modifier">public</span> `$mime` ;

<span class="modifier">public</span> `$postname` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$mimetype`</span> \[, <span class="methodparam"><span
class="type">string</span> `$postname`</span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getFilename</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getMimeType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPostFilename</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMimeType</span> ( <span
class="methodparam"><span class="type">string</span> `$mime`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPostFilename</span> ( <span
class="methodparam"><span class="type">string</span> `$postname`</span>
)

}

属性
----

`name`  
待上传文件的名称

`mime`  
文件的 MIME type（默认是*application/octet-stream*）。

`postname`  
上传数据中的文件名称（默认为属性 `name` ）。

参见
----

-   <span class="function">curl\_setopt</span>

CURLFile::\_\_construct
=======================

curl\_file\_create
==================

创建 CURLFile 对象

### 说明

面向对象风格

<span class="modifier">public</span> <span
class="methodname">CURLFile::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$mimetype`</span> \[, <span class="methodparam"><span
class="type">string</span> `$postname`</span> \]\] )

过程化风格

<span class="type">CURLFile</span> <span
class="methodname">curl\_file\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$mimetype`</span> \[, <span class="methodparam"><span
class="type">string</span> `$postname`</span> \]\] )

创建 <span class="classname">CURLFile</span> 对象，使用
**`CURLOPT_POSTFIELDS`** 选项上传文件。

### 参数

`filename`  
被上传文件的 路径。

`mimetype`  
被上传文件的 MIME 类型。

`postname`  
上传数据里面的文件名。

### 返回值

返回 <span class="classname">CURLFile</span> 对象。

### 范例

**示例 \#1 <span class="function">CURLFile::\_\_construct</span> 示例**

面向对象风格

``` php
<?php
/* http://example.com/upload.php:
<?php var_dump($_FILES); ?>
*/

// Create a cURL handle
$ch = curl_init('http://example.com/upload.php');

// Create a CURLFile object
$cfile = new CURLFile('cats.jpg','image/jpeg','test_name');

// Assign POST data
$data = array('test_file' => $cfile);
curl_setopt($ch, CURLOPT_POST,1);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

// Execute the handle
curl_exec($ch);
?>
```

过程化风格

``` php
<?php
/* http://example.com/upload.php:
<?php var_dump($_FILES); ?>
*/

// Create a cURL handle
$ch = curl_init('http://example.com/upload.php');

// Create a CURLFile object
$cfile = curl_file_create('cats.jpg','image/jpeg','test_name');

// Assign POST data
$data = array('test_file' => $cfile);
curl_setopt($ch, CURLOPT_POST,1);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

// Execute the handle
curl_exec($ch);
?>
```

以上例程会输出：

    array(1) {
      ["test_file"]=>
      array(5) {
        ["name"]=>
        string(9) "test_name"
        ["type"]=>
        string(10) "image/jpeg"
        ["tmp_name"]=>
        string(14) "/tmp/phpPC9Kbx"
        ["error"]=>
        int(0)
        ["size"]=>
        int(46334)
      }
    }

### 参见

-   <span class="function">curl\_setopt</span>

CURLFile::getFilename
=====================

获取被上传文件的 文件名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">CURLFile::getFilename</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回被上传文件的 文件名。

CURLFile::getMimeType
=====================

获取被上传文件的 MIME 类型

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">CURLFile::getMimeType</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回被上传文件的 MIME 类型。

CURLFile::getPostFilename
=========================

获取 POST 请求时使用的 文件名

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">CURLFile::getPostFilename</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回 POST 请求时使用的 文件名。

CURLFile::setMimeType
=====================

设置被上传文件的 MIME 类型

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CURLFile::setMimeType</span> ( <span
class="methodparam"><span class="type">string</span> `$mime`</span> )

### 参数

`mime`  
POST 数据中的 MIME 类型。

### 返回值

没有返回值。

CURLFile::setPostFilename
=========================

设置 POST 请求时使用的文件名

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CURLFile::setPostFilename</span> ( <span
class="methodparam"><span class="type">string</span> `$postname`</span>
)

### 参数

`postname`  
POST 数据里使用的文件名。

### 返回值

没有返回值。
