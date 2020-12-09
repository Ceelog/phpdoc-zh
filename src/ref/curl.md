curl\_close
===========

关闭 cURL 会话

### 说明

<span class="type">void</span> <span
class="methodname">curl\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> )

关闭 cURL 会话并且释放所有资源。cURL 句柄 `ch` 也会被删除。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

没有返回值。

### 范例

**示例 \#1 初始化新的 cURL 会话，并获取一张网页**

``` php
<?php
// 创建一个新cURL资源
$ch = curl_init();

// 设置URL和相应的选项
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// 抓取URL并把它传递给浏览器
curl_exec($ch);

// 关闭cURL资源，并且释放系统资源
curl_close($ch);
?>
```

### 参见

-   <span class="function">curl\_init</span>
-   <span class="function">curl\_multi\_close</span>

curl\_copy\_handle
==================

复制一个cURL句柄和它的所有选项

### 说明

<span class="type">resource</span> <span
class="methodname">curl\_copy\_handle</span> ( <span
class="methodparam"><span class="type">resource</span> `$ch`</span> )

复制一个cURL句柄并保持相同的选项。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

返回一个新的cURL句柄。

### 范例

**示例 \#1 复制一个cURL句柄**

``` php
<?php
// 创建一个新的cURL资源
$ch = curl_init();

// 设置URL和相应的选项
curl_setopt($ch, CURLOPT_URL, 'http://www.example.com/');
curl_setopt($ch, CURLOPT_HEADER, 0);

// 复制句柄
$ch2 = curl_copy_handle($ch);

// 抓取URL (http://www.example.com/) 并把它传递给浏览器
curl_exec($ch2);

// 关闭cURL资源，并且释放系统资源
curl_close($ch2);
curl_close($ch);
?>
```

curl\_errno
===========

返回最后一次的错误代码

### 说明

<span class="type">int</span> <span
class="methodname">curl\_errno</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> )

返回最后一次 cURL 操作的错误代码。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

返回错误代码或在没有错误发生时返回 *0* (零)。

### 范例

**示例 \#1 <span class="function">curl\_errno</span> 例子**

``` php
<?php
// 创建 cURL 句柄，指向不存在的位置
$ch = curl_init('http://404.php.net/');

// 执行
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_exec($ch);

// 检查是否有错误发生
if(curl_errno($ch))
{
    echo 'Curl error: ' . curl_error($ch);
}

// 关闭句柄
curl_close($ch);
?>
```

### 参见

-   <span class="function">curl\_error</span>
-   <a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» Curl 错误代码</a>

curl\_error
===========

返回当前会话最后一次错误的字符串

### 说明

<span class="type">string</span> <span
class="methodname">curl\_error</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> )

返回最近一次 cURL 操作的文本错误详情。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

返回错误信息，或者如果没有任何错误发生就返回 *''* (空字符串)。

### 范例

**示例 \#1 <span class="function">curl\_error</span> 例子**

``` php
<?php
// 创建 cURL 句柄，指向一个不存在的位置
$ch = curl_init('http://404.php.net/');
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

if(curl_exec($ch) === false)
{
    echo 'Curl error: ' . curl_error($ch);
}
else
{
    echo '操作完成没有任何错误';
}

// 关闭句柄
curl_close($ch);
?>
```

### 参见

-   <span class="function">curl\_errno</span>
-   <a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» Curl 错误代码</a>

curl\_escape
============

使用 URL 编码给定的字符串

### 说明

<span class="type">string</span> <span
class="methodname">curl\_escape</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> , <span
class="methodparam"><span class="type">string</span> `$str`</span> )

该函数使用 URL
根据<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>编码给定的字符串。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

`str`  
需要编码的字符串

### 返回值

返回编码后的字符串 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">curl\_escape</span> 示例**

``` php
<?php
// 创建一个 curl 句柄
$ch = curl_init();

// 把编码后的字符串当做一个 GET 参数
$location = curl_escape($ch, 'Hofbräuhaus / München');
// 结果： Hofbr%C3%A4uhaus%20%2F%20M%C3%BCnchen

// 用编码好的字符串组装一个 URL
$url = "http://example.com/add_location.php?location={$location}";
// 结果： http://example.com/add_location.php?location=Hofbr%C3%A4uhaus%20%2F%20M%C3%BCnchen

// 发送 HTTP 请求并关闭句柄
curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_exec($ch);
curl_close($ch);
?>
```

### 参见

-   <span class="function">curl\_unescape</span>
-   <span class="function">urlencode</span>
-   <span class="function">rawurlencode</span>
-   <a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>

curl\_exec
==========

执行 cURL 会话

### 说明

<span class="type">mixed</span> <span
class="methodname">curl\_exec</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> )

执行给定的 cURL 会话。

这个函数应该在初始化一个 cURL 会话并且全部的选项都被设置后被调用。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。 然而，如果
<a href="/ref/curl.html#curl_setopt" class="link">设置</a>了
**`CURLOPT_RETURNTRANSFER`**
选项，函数执行成功时会返回执行的结果，失败时返回 **`false`** 。

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

> **Note**:
>
> 注意：响应代码是错误码时（例如*404 Not
> found*）也不会被当作失败。这种情况可以使用 <span
> class="function">curl\_getinfo</span> 来检查。

### 范例

**示例 \#1 获取网页**

``` php
<?php
// 创建新的 cURL 资源
$ch = curl_init();

// 设置 URL 和相应的选项
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// 抓取 URL 并把它传递给浏览器
curl_exec($ch);

// 关闭 cURL 资源，并且释放系统资源
curl_close($ch);
?>
```

### 参见

-   <span class="function">curl\_multi\_exec</span>

curl\_file\_create
==================

创建一个 CURLFile 对象

### 说明

此函数是该函数的别名： <span
class="methodname">CURLFile::\_\_construct</span>

curl\_getinfo
=============

获取一个cURL连接资源句柄的信息

### 说明

<span class="type">mixed</span> <span
class="methodname">curl\_getinfo</span> ( <span
class="methodparam"><span class="type">resource</span> `$ch`</span> \[,
<span class="methodparam"><span class="type">int</span> `$opt`<span
class="initializer"> = 0</span></span> \] )

获取最后一次传输的相关信息。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

`opt`  
这个参数可能是以下常量之一:

-   <span class="simpara"> **`CURLINFO_EFFECTIVE_URL`** -
    最后一个有效的URL地址 </span>
-   <span class="simpara"> **`CURLINFO_HTTP_CODE`** -
    最后一个收到的HTTP代码 </span>
-   <span class="simpara"> **`CURLINFO_FILETIME`** -
    远程获取文档的时间，如果无法获取，则返回值为“-1” </span>
-   <span class="simpara"> **`CURLINFO_TOTAL_TIME`** -
    最后一次传输所消耗的时间 </span>
-   <span class="simpara"> **`CURLINFO_NAMELOOKUP_TIME`** -
    名称解析所消耗的时间 </span>
-   <span class="simpara"> **`CURLINFO_CONNECT_TIME`** -
    建立连接所消耗的时间 </span>
-   <span class="simpara"> **`CURLINFO_PRETRANSFER_TIME`** -
    从建立连接到准备传输所使用的时间 </span>
-   <span class="simpara"> **`CURLINFO_STARTTRANSFER_TIME`** -
    从建立连接到传输开始所使用的时间 </span>
-   <span class="simpara"> **`CURLINFO_REDIRECT_TIME`** -
    在事务传输开始前重定向所使用的时间 </span>
-   <span class="simpara"> **`CURLINFO_SIZE_UPLOAD`** -
    以字节为单位返回上传数据量的总值 </span>
-   <span class="simpara"> **`CURLINFO_SIZE_DOWNLOAD`** -
    以字节为单位返回下载数据量的总值 </span>
-   <span class="simpara"> **`CURLINFO_SPEED_DOWNLOAD`** - 平均下载速度
    </span>
-   <span class="simpara"> **`CURLINFO_SPEED_UPLOAD`** - 平均上传速度
    </span>
-   <span class="simpara"> **`CURLINFO_HEADER_SIZE`** - header部分的大小
    </span>
-   <span class="simpara"> **`CURLINFO_HEADER_OUT`** - 发送请求的字符串
    </span>
-   <span class="simpara"> **`CURLINFO_REQUEST_SIZE`** -
    在HTTP请求中有问题的请求的大小 </span>
-   <span class="simpara"> **`CURLINFO_SSL_VERIFYRESULT`** -
    通过设置**`CURLOPT_SSL_VERIFYPEER`**返回的SSL证书验证请求的结果
    </span>
-   <span class="simpara"> **`CURLINFO_CONTENT_LENGTH_DOWNLOAD`** -
    从*Content-Length:* field中读取的下载内容长度 </span>
-   <span class="simpara"> **`CURLINFO_CONTENT_LENGTH_UPLOAD`** -
    上传内容大小的说明 </span>
-   <span class="simpara"> **`CURLINFO_CONTENT_TYPE`** -
    下载内容的*Content-Type:*值，NULL表示服务器没有发送有效的*Content-Type:*
    header </span>

### 返回值

如果 `opt`
被设置，以字符串形式返回它的值。否则，返回返回一个包含下列元素的关联数组(它们分别对应于
`opt`):

-   <span class="simpara"> "url" </span>
-   <span class="simpara"> "content\_type" </span>
-   <span class="simpara"> "http\_code" </span>
-   <span class="simpara"> "header\_size" </span>
-   <span class="simpara"> "request\_size" </span>
-   <span class="simpara"> "filetime" </span>
-   <span class="simpara"> "ssl\_verify\_result" </span>
-   <span class="simpara"> "redirect\_count" </span>
-   <span class="simpara"> "total\_time" </span>
-   <span class="simpara"> "namelookup\_time" </span>
-   <span class="simpara"> "connect\_time" </span>
-   <span class="simpara"> "pretransfer\_time" </span>
-   <span class="simpara"> "size\_upload" </span>
-   <span class="simpara"> "size\_download" </span>
-   <span class="simpara"> "speed\_download" </span>
-   <span class="simpara"> "speed\_upload" </span>
-   <span class="simpara"> "download\_content\_length" </span>
-   <span class="simpara"> "upload\_content\_length" </span>
-   <span class="simpara"> "starttransfer\_time" </span>
-   <span class="simpara"> "redirect\_time" </span>

### 更新日志

| 版本  | 说明                           |
|-------|--------------------------------|
| 5.1.3 | 引入**`CURLINFO_HEADER_OUT`**. |

### 范例

**示例 \#1 <span class="function">curl\_getinfo</span> example**

``` php
<?php
// 创建一个cURL句柄
$ch = curl_init('http://www.yahoo.com/');

// 执行
curl_exec($ch);

// 检查是否有错误发生
if(!curl_errno($ch))
{
 $info = curl_getinfo($ch);

 echo 'Took ' . $info['total_time'] . ' seconds to send a request to ' . $info['url'];
}

// Close handle
curl_close($ch);
?>
```

### 注释

> **Note**:
>
> Information gathered by this function is kept if the handle is
> re-used. This means that unless a statistic is overridden internally
> by this function, the previous info is returned.

curl\_init
==========

初始化 cURL 会话

### 说明

<span class="type">resource</span> <span
class="methodname">curl\_init</span> (\[ <span class="methodparam"><span
class="type">string</span> `$url`<span class="initializer"> =
**`null`**</span></span> \] )

初始化新的会话，返回 cURL 句柄，供<span
class="function">curl\_setopt</span>、 <span
class="function">curl\_exec</span> 和 <span
class="function">curl\_close</span> 函数使用。

### 参数

`url`  
如果提供了该参数，**`CURLOPT_URL`**
选项将会被设置成这个值。你也可以使用<span
class="function">curl\_setopt</span>函数手动地设置这个值。

> **Note**:
>
> 如果设置了
> <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>，*file*
> 协议会被 cURL 禁用。

### 返回值

如果成功，返回 cURL 句柄，出错返回 **`false`**。

### 范例

**示例 \#1 初始化新的 cURL 会话并获取一个网页**

``` php
<?php
// 创建一个新cURL资源
$ch = curl_init();

// 设置URL和相应的选项
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// 抓取URL并把它传递给浏览器
curl_exec($ch);

// 关闭cURL资源，并且释放系统资源
curl_close($ch);
?>
```

### 参见

-   <span class="function">curl\_close</span>
-   <span class="function">curl\_multi\_init</span>

curl\_multi\_add\_handle
========================

向curl批处理会话中添加单独的curl句柄

### 说明

<span class="type">int</span> <span
class="methodname">curl\_multi\_add\_handle</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$ch`</span> )

增加 `ch` 句柄到批处理会话`mh`

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

成功时返回0，失败时返回**`CURLM_XXX`**之一的错误码。

### 范例

**示例 \#1 <span class="function">curl\_multi\_add\_handle</span>
example**

这个范例将会创建2个cURL句柄，把它们加到批处理句柄，然后并行地运行它们。

``` php
<?php
// 创建一对cURL资源
$ch1 = curl_init();
$ch2 = curl_init();

// 设置URL和相应的选项
curl_setopt($ch1, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

// 创建批处理cURL句柄
$mh = curl_multi_init();

// 增加2个句柄
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

$running=null;
// 执行批处理句柄
do {
    curl_multi_exec($mh,$running);
} while($running > 0);

// 关闭全部句柄
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);
?>
```

### 参见

-   <span class="function">curl\_multi\_remove\_handle</span>
-   <span class="function">curl\_multi\_init</span>
-   <span class="function">curl\_init</span>

curl\_multi\_close
==================

关闭一组cURL句柄

### 说明

<span class="type">void</span> <span
class="methodname">curl\_multi\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> )

关闭一组cURL句柄。

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">curl\_multi\_close</span> example**

这个范例将会创建2个cURL句柄，把它们加到批处理句柄，然后并行地运行它们。

``` php
<?php
// 创建一对cURL资源
$ch1 = curl_init();
$ch2 = curl_init();

// 设置URL和相应的选项
curl_setopt($ch1, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

// 创建批处理cURL句柄
$mh = curl_multi_init();

// 增加2个句柄
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

$running=null;
// 执行批处理句柄
do {
    curl_multi_exec($mh,$running);
} while ($running > 0);

// 关闭全部句柄
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);

?>
```

### 参见

-   <span class="function">curl\_multi\_init</span>
-   <span class="function">curl\_close</span>

curl\_multi\_errno
==================

返回上一次 curl 批处理的错误码

### 说明

<span class="type">int</span> <span
class="methodname">curl\_multi\_errno</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> )

返回一个整型数字，为上次 curl 批处理错误码。

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

### 返回值

返回整型数字，包含上次 curl 批处理的错误码， 或者在失败时返回
**`false`**

### 参见

-   <span class="function">curl\_errno</span>

curl\_multi\_exec
=================

运行当前 cURL 句柄的子连接

### 说明

<span class="type">int</span> <span
class="methodname">curl\_multi\_exec</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> ,
<span class="methodparam"><span class="type">int</span>
`&$still_running`</span> )

处理在栈中的每一个句柄。无论该句柄需要读取或写入数据都可调用此方法。

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

`still_running`  
一个用来判断操作是否仍在执行的标识的引用。

### 返回值

一个定义于 cURL
<a href="/curl/constants.html" class="link">预定义常量</a>中的 cURL
代码。

> **Note**:
>
> 该函数仅返回关于整个批处理栈相关的错误。即使返回 **`CURLM_OK`**
> 时单个传输仍可能有问题。

### 范例

**示例 \#1 <span class="function">curl\_multi\_exec</span> example**

这个范例将会创建 2 个 cURL
句柄，把它们加到批处理句柄，然后并行地运行它们。

``` php
<?php
// 创建一对cURL资源
$ch1 = curl_init();
$ch2 = curl_init();

// 设置URL和相应的选项
curl_setopt($ch1, CURLOPT_URL, "http://lxr.php.net/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

// 创建批处理cURL句柄
$mh = curl_multi_init();

// 增加2个句柄
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

$active = null;
// 执行批处理句柄
do {
    $mrc = curl_multi_exec($mh, $active);
} while ($mrc == CURLM_CALL_MULTI_PERFORM);

while ($active && $mrc == CURLM_OK) {
    if (curl_multi_select($mh) != -1) {
        do {
            $mrc = curl_multi_exec($mh, $active);
        } while ($mrc == CURLM_CALL_MULTI_PERFORM);
    }
}

// 关闭全部句柄
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);

?>
```

### 参见

-   <span class="function">curl\_multi\_init</span>
-   <span class="function">curl\_multi\_select</span>
-   <span class="function">curl\_exec</span>

curl\_multi\_getcontent
=======================

如果设置了**`CURLOPT_RETURNTRANSFER`**，则返回获取的输出的文本流

### 说明

<span class="type">string</span> <span
class="methodname">curl\_multi\_getcontent</span> ( <span
class="methodparam"><span class="type">resource</span> `$ch`</span> )

如果**`CURLOPT_RETURNTRANSFER`**作为一个选项被设置到一个具体的句柄，那么这个函数将会以字符串的形式返回那个cURL句柄获取的内容。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

如果设置了**`CURLOPT_RETURNTRANSFER`**，则返回获取的输出的文本流。

### 参见

-   <span class="function">curl\_multi\_init</span>

curl\_multi\_info\_read
=======================

获取当前解析的cURL的相关传输信息

### 说明

<span class="type">array</span> <span
class="methodname">curl\_multi\_info\_read</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> \[,
<span class="methodparam"><span class="type">int</span>
`&$msgs_in_queue`<span class="initializer"> = **`null`**</span></span>
\] )

查询批处理句柄是否单独的传输线程中有消息或信息返回。消息可能包含诸如从单独的传输线程返回的错误码或者只是传输线程有没有完成之类的报告。

重复调用这个函数，它每次都会返回一个新的结果，直到这时没有更多信息返回时，**`false`**
被当作一个信号返回。通过`msgs_in_queue`返回的整数指出将会包含当这次函数被调用后，还剩余的消息数。

**Warning**

返回的资源指向的数据调用<span
class="function">curl\_multi\_remove\_handle</span>后将不会存在。

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

`msgs_in_queue`  
仍在队列中的消息数量。

### 返回值

成功时返回相关信息的数组，失败时返回**`false`**。

| Key:     | Value:                                                                    |
|----------|---------------------------------------------------------------------------|
| *msg*    | **`CURLMSG_DONE`**常量。其他返回值当前不可用。                            |
| *result* | **`CURLE_*`**常量之一。如果一切操作没有问题，将会返回**`CURLE_OK`**常量。 |
| *handle* | cURL资源类型表明它有关的句柄。                                            |

### 范例

**示例 \#1 一个<span
class="function">curl\_multi\_info\_read</span>范例**

``` php
<?php

$urls = array(
   "http://www.cnn.com/",
   "http://www.bbc.co.uk/",
   "http://www.yahoo.com/"
);

$mh = curl_multi_init();

foreach ($urls as $i => $url) {
    $conn[$i] = curl_init($url);
    curl_setopt($conn[$i], CURLOPT_RETURNTRANSFER, 1);
    curl_multi_add_handle($mh, $conn[$i]);
}

do {
    $status = curl_multi_exec($mh, $active);
    $info = curl_multi_info_read($mh);
    if (false !== $info) {
        var_dump($info);
    }
} while ($status === CURLM_CALL_MULTI_PERFORM || $active);

foreach ($urls as $i => $url) {
    $res[$i] = curl_multi_getcontent($conn[$i]);
    curl_close($conn[$i]);
}

var_dump(curl_multi_info_read($mh));

?>
```

以上例程的输出类似于：

    array(3) {
      ["msg"]=>
      int(1)
      ["result"]=>
      int(0)
      ["handle"]=>
      resource(5) of type (curl)
    }
    array(3) {
      ["msg"]=>
      int(1)
      ["result"]=>
      int(0)
      ["handle"]=>
      resource(7) of type (curl)
    }
    array(3) {
      ["msg"]=>
      int(1)
      ["result"]=>
      int(0)
      ["handle"]=>
      resource(6) of type (curl)
    }
    bool(false)

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 5.2.0 | `msgs_in_queue`被加入。 |

### 参见

-   <span class="function">curl\_multi\_init</span>

curl\_multi\_init
=================

返回一个新cURL批处理句柄

### 说明

<span class="type">resource</span> <span
class="methodname">curl\_multi\_init</span> ( <span
class="methodparam">void</span> )

允许并行地处理批处理cURL句柄。

### 参数

此函数没有参数。

### 返回值

成功时返回一个cURL批处理句柄，失败时返回**`false`**。

### 范例

**示例 \#1 <span class="function">curl\_multi\_init</span> example**

这个范例将会创建2个cURL句柄，把它们加到批处理句柄，然后并行地运行它们。

``` php
<?php
// 创建一对cURL资源
$ch1 = curl_init();
$ch2 = curl_init();

// 设置URL和相应的选项
curl_setopt($ch1, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

// 创建批处理cURL句柄
$mh = curl_multi_init();

// 增加2个句柄
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

$running=null;
// 执行批处理句柄
do {
    usleep(10000);
    curl_multi_exec($mh,$running);
} while ($running > 0);

// 关闭全部句柄
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);

?>
```

### 参见

-   <span class="function">curl\_init</span>
-   <span class="function">curl\_multi\_close</span>

curl\_multi\_remove\_handle
===========================

移除cURL批处理句柄资源中的某个句柄资源

### 说明

<span class="type">int</span> <span
class="methodname">curl\_multi\_remove\_handle</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$ch`</span> )

从给定的批处理句柄`mh`中移除`ch`句柄。当`ch`句柄被移除以后，仍然可以合法地用<span
class="function">curl\_exec</span>执行这个句柄。如果要移除的句柄正在被使用，则这个句柄涉及的所有传输任务会被中止。

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

成功时返回0，失败时返回**`CURLM_XXX`**中的一个。

### 参见

-   <span class="function">curl\_init</span>
-   <span class="function">curl\_multi\_init</span>
-   <span class="function">curl\_multi\_add\_handle</span>

curl\_multi\_select
===================

等待所有cURL批处理中的活动连接

### 说明

<span class="type">int</span> <span
class="methodname">curl\_multi\_select</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$timeout`<span class="initializer"> = 1.0</span></span> \] )

阻塞直到cURL批处理连接中有活动连接。

### 参数

`multi_handle`  
由 <span class="function">curl\_multi\_init</span> 返回的 cURL
多个句柄。

`timeout`  
以秒为单位，等待响应的时间。

### 返回值

成功时返回描述符集合中描述符的数量。失败时，select失败时返回-1，否则返回超时(从底层的select系统调用).

### 参见

-   <span class="function">curl\_multi\_init</span>

curl\_multi\_setopt
===================

为 cURL 并行处理设置一个选项

### 说明

<span class="type">bool</span> <span
class="methodname">curl\_multi\_setopt</span> ( <span
class="methodparam"><span class="type">resource</span> `$mh`</span> ,
<span class="methodparam"><span class="type">int</span> `$option`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`mh`  

`option`  
常量 **`CURLMOPT_*`** 之一。

`value`  
将要设置给 `option` 的值。

在 `option` 参数为下列值时 `value` 需要为 <span class="type">int</span>
类型：

| Option 的值                | 将 `value` 设为                                                                                                                                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`CURLMOPT_PIPELINING`**  | 传入 1 来启用或 0 来禁用。 在并行处理时启用管道模式 将会尽可能地使用管线化的 HTTP （译注：HTTP长连接）来 传输，这意味着如果你提交第二个请求，这个请求将会使用 已经存在的链接，第二个请求将会被送入同一个链接的“管 道”中。 |
| **`CURLMOPT_MAXCONNECTS`** | 传入一个数字来指定 libcurl 可以同时缓存的活跃链接的数量。默认值为 10。当缓存写满时， lincurl 将关闭较早创建的链接来创建新的链接。                                                                                         |

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

curl\_multi\_strerror
=====================

返回字符串描述的错误代码

### 说明

<span class="type">string</span> <span
class="methodname">curl\_multi\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errornum`</span> )

返回一个用以描述所给 CURLM 错误代码所对应的错误信息。

### 参数

`errornum`  
<a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» CURLM 错误代码</a>中的常量之一。

### 返回值

返回可用错误代码所对应的错误信息，否则返回 **`null`** 。

### 范例

**示例 \#1 <span class="function">curl\_multi\_strerror</span>
函数的范例：**

``` php
<?php
// Create cURL handles
$ch1 = curl_init("http://example.com"/);
$ch2 = curl_init("http://php.net/");

// Create a cURL multi handle
$mh = curl_multi_init();

// Add the handles to the multi handle
curl_multi_add_handle($mh, $ch1);
curl_multi_add_handle($mh, $ch2);

// Execute the multi handle
do {
    $status = curl_multi_exec($mh, $active);
    // Check for errors
    if($status > 0) {
        // Display error message
        echo "ERROR!\n " . curl_multi_strerror($status);
    }
} while ($status === CURLM_CALL_MULTI_PERFORM || $active);
?>
```

### 参见

-   <span class="function">curl\_strerror</span>
-   <a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» cURL error codes</a>

curl\_pause
===========

暂停和取消暂停一个连接。

### 说明

<span class="type">int</span> <span
class="methodname">curl\_pause</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> , <span
class="methodparam"><span class="type">int</span> `$bitmask`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

`bitmask`  
**`CURLPAUSE_*`** 常量之一。

### 返回值

返回一个错误代码 (如果没有错误则返回**`CURLE_OK`**常量)。

curl\_reset
===========

重置一个 libcurl 会话句柄的所有的选项

### 说明

<span class="type">void</span> <span
class="methodname">curl\_reset</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> )

该函数将给定的 cURL 句柄所有选项重新设置为默认值。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">curl\_reset</span> 示例**

``` php
<?php
// 创建一个url 句柄
$ch = curl_init();

// 设置 CURLOPT_USERAGENT 选项
curl_setopt($ch, CURLOPT_USERAGENT, "My test user-agent");

// 重置所有的预先设置的选项
curl_reset($ch);

// 发送 HTTP 请求
curl_setopt($ch, CURLOPT_URL, 'http://example.com/');
curl_exec($ch); // 预先设置的 user-agent 不会被发送，它已经被 curl_reset 重置掉了

// 关闭句柄
curl_close($ch);
?>
```

### 注释

> **Note**:
>
> <span class="function">curl\_reset</span> also resets the URL given as
> the <span class="function">curl\_init</span> parameter.

### 参见

-   <span class="function">curl\_setopt</span>

curl\_setopt\_array
===================

为 cURL 传输会话批量设置选项

### 说明

<span class="type">bool</span> <span
class="methodname">curl\_setopt\_array</span> ( <span
class="methodparam"><span class="type">resource</span> `$ch`</span> ,
<span class="methodparam"><span class="type">array</span>
`$options`</span> )

为 cURL 传输会话批量设置选项。这个函数对于需要设置大量的 cURL
选项是非常有用的，不需要重复地调用 <span
class="function">curl\_setopt</span>。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

`options`  
一个 <span class="type">array</span>
用来确定将被设置的选项及其值。数组的键值必须是一个有效的<span
class="function">curl\_setopt</span>常量或者是它们对等的整数值。

### 返回值

如果全部的选项都被成功设置，返回**`true`**。如果一个选项不能被成功设置，马上返回**`false`**，忽略其后的任何在`options`数组中的选项。

### 范例

**示例 \#1 初始化新的 cURL 会话并抓取 web 页面**

``` php
<?php
// 创建一个新 cURL 资源
$ch = curl_init();

// 设置 URL 和相应的选项
$options = array(CURLOPT_URL => 'http://www.example.com/',
                 CURLOPT_HEADER => false
                );

curl_setopt_array($ch, $options);

// 抓取 URL 并把它传递给浏览器
curl_exec($ch);

// 关闭 cURL 资源，并且释放系统资源
curl_close($ch);
?>
```

早于PHP 5.1.3这个函数可以做如下模拟：

**示例 \#2 我们对<span
class="function">curl\_setopt\_array</span>的等价实现**

``` php
<?php
if (!function_exists('curl_setopt_array')) {
   function curl_setopt_array(&$ch, $curl_options)
   {
       foreach ($curl_options as $option => $value) {
           if (!curl_setopt($ch, $option, $value)) {
               return false;
           } 
       }
       return true;
   }
}
?>
```

### 注释

> **Note**:
>
> 就<span
> class="function">curl\_setopt</span>来说，传递一个数组到**`CURLOPT_POST`**将会把数据以*multipart/form-data*的方式编码，然而传递一个URL-encoded字符串将会以*application/x-www-form-urlencoded*的方式对数据进行编码。

### 参见

-   <span class="function">curl\_setopt</span>

curl\_setopt
============

设置 cURL 传输选项

### 说明

<span class="type">bool</span> <span
class="methodname">curl\_setopt</span> ( <span class="methodparam"><span
class="type">resource</span> `$ch`</span> , <span
class="methodparam"><span class="type">int</span> `$option`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

为 cURL 会话句柄设置选项。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

`option`  
需要设置的*CURLOPT\_XXX*选项。

`value`  
将设置在`option`选项上的值。

以下 `option` 参数的 `value`应该被设置成 <span class="type">bool</span>
类型：

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>选项</th>
<th>将 <code class="parameter">value</code> 设置为</th>
<th>备注</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>CURLOPT_AUTOREFERER</code></strong></td>
<td><strong><code>true</code></strong> 时将根据 <em>Location:</em> 重定向时，自动设置 header 中的<em>Referer:</em>信息。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_BINARYTRANSFER</code></strong></td>
<td>设为 <strong><code>true</code></strong> ，将在启用 <strong><code>CURLOPT_RETURNTRANSFER</code></strong> 时，返回原生的（Raw）输出。</td>
<td>从 PHP 5.1.3 开始，此选项不再有效果：使用 <strong><code>CURLOPT_RETURNTRANSFER</code></strong> 后总是会返回原生的（Raw）内容。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_COOKIESESSION</code></strong></td>
<td>设为 <strong><code>true</code></strong> 时将开启新的一次 cookie 会话。它将强制 libcurl 忽略之前会话时存的其他 cookie。 libcurl 在默认状况下无论是否为会话，都会储存、加载所有 cookie。会话 cookie 是指没有过期时间，只存活在会话之中。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_CERTINFO</code></strong></td>
<td><strong><code>true</code></strong> 将在安全传输时输出 SSL 证书信息到 <em>STDERR</em>。</td>
<td>在 cURL 7.19.1 中添加。 PHP 5.3.2 后有效。 需要开启 <strong><code>CURLOPT_VERBOSE</code></strong> 才有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_CONNECT_ONLY</code></strong></td>
<td><strong><code>true</code></strong> 将让库执行所有需要的代理、验证、连接过程，但不传输数据。此选项用于 HTTP、SMTP 和 POP3。</td>
<td>在 7.15.2 中添加。 PHP 5.5.0 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_CRLF</code></strong></td>
<td>启用时将Unix的换行符转换成回车换行符。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_DNS_USE_GLOBAL_CACHE</code></strong></td>
<td><strong><code>true</code></strong> 会启用一个全局的DNS缓存。此选项非线程安全的，默认已开启。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FAILONERROR</code></strong></td>
<td>当 HTTP 状态码大于等于 400，<strong><code>true</code></strong> 将将显示错误详情。 默认情况下将返回页面，忽略 HTTP 代码。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSL_FALSESTART</code></strong></td>
<td><strong><code>true</code></strong> 开启 TLS False Start （一种 TLS 握手优化方式）</td>
<td>cURL 7.42.0 中添加。自 PHP 7.0.7 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FILETIME</code></strong></td>
<td><strong><code>true</code></strong> 时，会尝试获取远程文档中的修改时间信息。 信息可通过<span class="function">curl_getinfo</span>函数的<code class="parameter">CURLINFO_FILETIME</code> 选项获取。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FOLLOWLOCATION</code></strong></td>
<td><strong><code>true</code></strong> 时将会根据服务器返回 HTTP 头中的 <em>"Location: "</em> 重定向。（注意：这是递归的，<em>"Location: "</em> 发送几次就重定向几次，除非设置了 <strong><code>CURLOPT_MAXREDIRS</code></strong>，限制最大重定向次数。）。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FORBID_REUSE</code></strong></td>
<td><strong><code>true</code></strong> 在完成交互以后强制明确的断开连接，不能在连接池中重用。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FRESH_CONNECT</code></strong></td>
<td><strong><code>true</code></strong> 强制获取一个新的连接，而不是缓存中的连接。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FTP_USE_EPRT</code></strong></td>
<td><strong><code>true</code></strong> 时，当 FTP 下载时，使用 EPRT (和 LPRT)命令。 设置为 <strong><code>false</code></strong> 时禁用 EPRT 和 LPRT，仅仅使用PORT 命令。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FTP_USE_EPSV</code></strong></td>
<td><strong><code>true</code></strong> 时，在FTP传输过程中，回到 PASV 模式前，先尝试 EPSV 命令。设置为 <strong><code>false</code></strong> 时禁用 EPSV。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FTP_CREATE_MISSING_DIRS</code></strong></td>
<td><strong><code>true</code></strong> 时，当 ftp 操作不存在的目录时将创建它。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FTPAPPEND</code></strong></td>
<td><strong><code>true</code></strong> 为追加写入文件，而不是覆盖。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_TCP_NODELAY</code></strong></td>
<td><strong><code>true</code></strong> 时禁用 TCP 的 Nagle 算法，就是减少网络上的小包数量。</td>
<td>PHP 5.2.1 有效，编译时需要 libcurl 7.11.2 及以上。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FTPASCII</code></strong></td>
<td><strong><code>CURLOPT_TRANSFERTEXT</code></strong> 的别名。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FTPLISTONLY</code></strong></td>
<td><strong><code>true</code></strong> 时只列出 FTP 目录的名字。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_HEADER</code></strong></td>
<td>启用时会将头文件的信息作为数据流输出。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLINFO_HEADER_OUT</code></strong></td>
<td><strong><code>true</code></strong> 时追踪句柄的请求字符串。</td>
<td>从 PHP 5.1.3 开始可用。<strong><code>CURLINFO_</code></strong> 的前缀是有意的(intentional)。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_HTTPGET</code></strong></td>
<td><strong><code>true</code></strong> 时会设置 HTTP 的 method 为 GET，由于默认是 GET，所以只有 method 被修改时才需要这个选项。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_HTTPPROXYTUNNEL</code></strong></td>
<td><strong><code>true</code></strong> 会通过指定的 HTTP 代理来传输。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_MUTE</code></strong></td>
<td><strong><code>true</code></strong> 时将完全静默，无论是何 cURL 函数。</td>
<td>在 cURL 7.15.5 中移出（可以使用 CURLOPT_RETURNTRANSFER 作为代替）</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_NETRC</code></strong></td>
<td><strong><code>true</code></strong> 时，在连接建立时，访问<var class="filename">~/.netrc</var>文件获取用户名和密码来连接远程站点。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_NOBODY</code></strong></td>
<td><strong><code>true</code></strong> 时将不输出 BODY 部分。同时 Mehtod 变成了 HEAD。修改为 <strong><code>false</code></strong> 时不会变成 GET。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_NOPROGRESS</code></strong></td>
<td><p><strong><code>true</code></strong> 时关闭 cURL 的传输进度。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>PHP 默认自动设置此选项为 <strong><code>true</code></strong>，只有为了调试才需要改变设置。</p>
</blockquote></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_NOSIGNAL</code></strong></td>
<td><strong><code>true</code></strong> 时忽略所有的 cURL 传递给 PHP 进行的信号。在 SAPI 多线程传输时此项被默认启用，所以超时选项仍能使用。</td>
<td>cURL 7.10时被加入。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PATH_AS_IS</code></strong></td>
<td><strong><code>true</code></strong> 不处理 dot dot sequences （即 ../ ）</td>
<td>cURL 7.42.0 时被加入。 PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PIPEWAIT</code></strong></td>
<td><strong><code>true</code></strong> 则等待 pipelining/multiplexing。</td>
<td>cURL 7.43.0 时被加入。 PHP 7.0.7 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_POST</code></strong></td>
<td><strong><code>true</code></strong> 时会发送 POST 请求，类型为：<em>application/x-www-form-urlencoded</em>，是 HTML 表单提交时最常见的一种。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PUT</code></strong></td>
<td><strong><code>true</code></strong> 时允许 HTTP 发送文件。要被 PUT 的文件必须在 <strong><code>CURLOPT_INFILE</code></strong>和<strong><code>CURLOPT_INFILESIZE</code></strong> 中设置。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_RETURNTRANSFER</code></strong></td>
<td><strong><code>true</code></strong> 将<span class="function">curl_exec</span>获取的信息以字符串返回，而不是直接输出。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SAFE_UPLOAD</code></strong></td>
<td><strong><code>true</code></strong> 禁用 <em>@</em> 前缀在 <strong><code>CURLOPT_POSTFIELDS</code></strong> 中发送文件。 意味着 <em>@</em> 可以在字段中安全得使用了。 可使用 <span class="classname">CURLFile</span> 作为上传的代替。</td>
<td>PHP 5.5.0 中添加，默认值 <strong><code>false</code></strong>。 PHP 5.6.0 改默认值为 <strong><code>true</code></strong>。. PHP 7 删除了此选项， 必须使用 CURLFile interface 来上传文件。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SASL_IR</code></strong></td>
<td><strong><code>true</code></strong> 开启，收到首包(first packet)后发送初始的响应(initial response)。</td>
<td>cURL 7.31.10 中添加，自 PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSL_ENABLE_ALPN</code></strong></td>
<td><strong><code>false</code></strong> 禁用 SSL 握手中的 ALPN (如果 SSL 后端的 libcurl 内建支持) 用于协商到 http2。</td>
<td>cURL 7.36.0 中增加， PHP 7.0.7 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSL_ENABLE_NPN</code></strong></td>
<td><strong><code>false</code></strong> 禁用 SSL 握手中的 NPN(如果 SSL 后端的 libcurl 内建支持)，用于协商到 http2。</td>
<td>cURL 7.36.0 中增加， PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSL_VERIFYPEER</code></strong></td>
<td><strong><code>false</code></strong> 禁止 cURL 验证对等证书（peer's certificate）。要验证的交换证书可以在 <strong><code>CURLOPT_CAINFO</code></strong> 选项中设置，或在 <strong><code>CURLOPT_CAPATH</code></strong>中设置证书目录。</td>
<td>自cURL 7.10开始默认为 <strong><code>true</code></strong>。从 cURL 7.10开始默认绑定安装。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSL_VERIFYSTATUS</code></strong></td>
<td><strong><code>true</code></strong> 验证证书状态。</td>
<td>cURL 7.41.0 中添加， PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_TCP_FASTOPEN</code></strong></td>
<td><strong><code>true</code></strong> 开启 TCP Fast Open。</td>
<td>cURL 7.49.0 中添加， PHP 7.0.7 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_TFTP_NO_OPTIONS</code></strong></td>
<td><strong><code>true</code></strong> 不发送 TFTP 的 options 请求。</td>
<td>自 cURL 7.48.0 添加， PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_TRANSFERTEXT</code></strong></td>
<td><strong><code>true</code></strong> 对 FTP 传输使用 ASCII 模式。对于LDAP，它检索纯文本信息而非 HTML。在 Windows 系统上，系统不会把 <em>STDOUT</em> 设置成二进制 模式。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_UNRESTRICTED_AUTH</code></strong></td>
<td><strong><code>true</code></strong> 在使用<strong><code>CURLOPT_FOLLOWLOCATION</code></strong>重定向 header 中的多个 location 时继续发送用户名和密码信息，哪怕主机名已改变。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_UPLOAD</code></strong></td>
<td><strong><code>true</code></strong> 准备上传。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_VERBOSE</code></strong></td>
<td><strong><code>true</code></strong> 会输出所有的信息，写入到<em>STDERR</em>，或在<strong><code>CURLOPT_STDERR</code></strong>中指定的文件。</td>
<td></td>
</tr>
</tbody>
</table>

以下 `option`的`value`应该被设置成 <span class="type">integer</span>：

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>选项</th>
<th>设置<code class="parameter">value</code>为</th>
<th>备注</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>CURLOPT_BUFFERSIZE</code></strong></td>
<td>每次读入的缓冲的尺寸。当然不保证每次都会完全填满这个尺寸。</td>
<td>在cURL 7.10中被加入。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_CLOSEPOLICY</code></strong></td>
<td><strong><code>CURLCLOSEPOLICY_*</code></strong> 中的一个。
<blockquote>
<p><strong>Note</strong>:</p>
<p>此选项已被废弃，它不会被实现，永远不会有效果啦。</p>
</blockquote></td>
<td>PHP 5.6.0 中移除。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_CONNECTTIMEOUT</code></strong></td>
<td>在尝试连接时等待的秒数。设置为0，则无限等待。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_CONNECTTIMEOUT_MS</code></strong></td>
<td>尝试连接等待的时间，以毫秒为单位。设置为0，则无限等待。 如果 libcurl 编译时使用系统标准的名称解析器（ standard system name resolver），那部分的连接仍旧使用以秒计的超时解决方案，最小超时时间还是一秒钟。</td>
<td>在 cURL 7.16.2 中被加入。从 PHP 5.2.3 开始可用。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_DNS_CACHE_TIMEOUT</code></strong></td>
<td>设置在内存中缓存 DNS 的时间，默认为120秒（两分钟）。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_EXPECT_100_TIMEOUT_MS</code></strong></td>
<td>超时预计： 100毫秒内的 continue 响应 默认为 1000 毫秒。</td>
<td>cURL 7.36.0 中添加，自 PHP 7.0.7 有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FTPSSLAUTH</code></strong></td>
<td>FTP验证方式（启用的时候）：<em>CURLFTPAUTH_SSL</em> (首先尝试SSL)，<em>CURLFTPAUTH_TLS</em> (首先尝试TLS)或<em>CURLFTPAUTH_DEFAULT</em> (让cURL 自个儿决定)。</td>
<td>在 cURL 7.12.2 中被加入。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_HEADEROPT</code></strong></td>
<td>How to deal with headers. One of the following constants: <span class="simpara"> <strong><code>CURLHEADER_UNIFIED</code></strong>: the headers specified in <strong><code>CURLOPT_HTTPHEADER</code></strong> will be used in requests both to servers and proxies. With this option enabled, <strong><code>CURLOPT_PROXYHEADER</code></strong> will not have any effect. </span> <span class="simpara"> <strong><code>CURLHEADER_SEPARATE</code></strong>: makes <strong><code>CURLOPT_HTTPHEADER</code></strong> headers only get sent to a server and not to a proxy. Proxy headers must be set with <strong><code>CURLOPT_PROXYHEADER</code></strong> to get used. Note that if a non-CONNECT request is sent to a proxy, libcurl will send both server headers and proxy headers. When doing CONNECT, libcurl will send <strong><code>CURLOPT_PROXYHEADER</code></strong> headers only to the proxy and then <strong><code>CURLOPT_HTTPHEADER</code></strong> headers only to the server. </span> <span class="simpara"> Defaults to <strong><code>CURLHEADER_SEPARATE</code></strong> as of cURL 7.42.1, and <strong><code>CURLHEADER_UNIFIED</code></strong> before. </span></td>
<td>Added in cURL 7.37.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_HTTP_VERSION</code></strong></td>
<td><code class="parameter">CURL_HTTP_VERSION_NONE</code> (默认值，让 cURL 自己判断使用哪个版本)，<code class="parameter">CURL_HTTP_VERSION_1_0</code> (强制使用 HTTP/1.0)或<code class="parameter">CURL_HTTP_VERSION_1_1</code> (强制使用 HTTP/1.1)。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_HTTPAUTH</code></strong></td>
<td><p>使用的 HTTP 验证方法。选项有： <code class="parameter">CURLAUTH_BASIC</code>、 <code class="parameter">CURLAUTH_DIGEST</code>、 <code class="parameter">CURLAUTH_GSSNEGOTIATE</code>、 <code class="parameter">CURLAUTH_NTLM</code>、 <code class="parameter">CURLAUTH_ANY</code>和 <code class="parameter">CURLAUTH_ANYSAFE</code>。</p>
<p>可以使用 <em>|</em> 位域(OR)操作符结合多个值，cURL 会让服务器选择受支持的方法，并选择最好的那个。</p>
<p><code class="parameter">CURLAUTH_ANY</code>是 <em>CURLAUTH_BASIC | CURLAUTH_DIGEST | CURLAUTH_GSSNEGOTIATE | CURLAUTH_NTLM</em> 的别名。</p>
<p><code class="parameter">CURLAUTH_ANYSAFE</code> 是 <em>CURLAUTH_DIGEST | CURLAUTH_GSSNEGOTIATE | CURLAUTH_NTLM</em> 的别名。</p></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_INFILESIZE</code></strong></td>
<td>希望传给远程站点的文件尺寸，字节(byte)为单位。 注意无法用这个选项阻止 libcurl 发送更多的数据，确切发送什么取决于 <strong><code>CURLOPT_READFUNCTION</code></strong>。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_LOW_SPEED_LIMIT</code></strong></td>
<td>传输速度，每秒字节（bytes）数，根据<strong><code>CURLOPT_LOW_SPEED_TIME</code></strong>秒数统计是否因太慢而取消传输。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_LOW_SPEED_TIME</code></strong></td>
<td>当传输速度小于<strong><code>CURLOPT_LOW_SPEED_LIMIT</code></strong>时(bytes/sec)，PHP会判断是否因太慢而取消传输。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_MAXCONNECTS</code></strong></td>
<td>允许的最大连接数量。达到限制时，会通过<strong><code>CURLOPT_CLOSEPOLICY</code></strong>决定应该关闭哪些连接。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_MAXREDIRS</code></strong></td>
<td>指定最多的 HTTP 重定向次数，这个选项是和<strong><code>CURLOPT_FOLLOWLOCATION</code></strong>一起使用的。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PORT</code></strong></td>
<td>用来指定连接端口。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_POSTREDIR</code></strong></td>
<td>位掩码， 1 (301 永久重定向), 2 (302 Found) 和 4 (303 See Other) 设置 <strong><code>CURLOPT_FOLLOWLOCATION</code></strong> 时，什么情况下需要再次 HTTP POST 到重定向网址。</td>
<td>cURL 7.19.1 中添加，PHP 5.3.2 开始可用。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PROTOCOLS</code></strong></td>
<td><p><strong><code>CURLPROTO_*</code></strong>的位掩码。 启用时，会限制 libcurl 在传输过程中可使用哪些协议。 这将允许你在编译libcurl时支持众多协议，但是限制只用允许的子集。默认 libcurl 将使用所有支持的协议。 参见<strong><code>CURLOPT_REDIR_PROTOCOLS</code></strong>。</p>
<p>可用的协议选项为： <code class="parameter">CURLPROTO_HTTP</code>、 <code class="parameter">CURLPROTO_HTTPS</code>、 <code class="parameter">CURLPROTO_FTP</code>、 <code class="parameter">CURLPROTO_FTPS</code>、 <code class="parameter">CURLPROTO_SCP</code>、 <code class="parameter">CURLPROTO_SFTP</code>、 <code class="parameter">CURLPROTO_TELNET</code>、 <code class="parameter">CURLPROTO_LDAP</code>、 <code class="parameter">CURLPROTO_LDAPS</code>、 <code class="parameter">CURLPROTO_DICT</code>、 <code class="parameter">CURLPROTO_FILE</code>、 <code class="parameter">CURLPROTO_TFTP</code>、 <code class="parameter">CURLPROTO_ALL</code>。</p></td>
<td>在 cURL 7.19.4 中被加入。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PROXYAUTH</code></strong></td>
<td>HTTP 代理连接的验证方式。使用在<strong><code>CURLOPT_HTTPAUTH</code></strong>中的位掩码。 当前仅仅支持 <code class="parameter">CURLAUTH_BASIC</code>和<code class="parameter">CURLAUTH_NTLM</code>。</td>
<td>在 cURL 7.10.7 中被加入。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PROXYPORT</code></strong></td>
<td>代理服务器的端口。端口也可以在<strong><code>CURLOPT_PROXY</code></strong>中设置。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PROXYTYPE</code></strong></td>
<td>可以是 <strong><code>CURLPROXY_HTTP</code></strong> (默认值) <strong><code>CURLPROXY_SOCKS4</code></strong>、 <strong><code>CURLPROXY_SOCKS5</code></strong>、 <strong><code>CURLPROXY_SOCKS4A</code></strong> 或 <strong><code>CURLPROXY_SOCKS5_HOSTNAME</code></strong>。</td>
<td>在 cURL 7.10 中被加入。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_REDIR_PROTOCOLS</code></strong></td>
<td><strong><code>CURLPROTO_*</code></strong> 值的位掩码。如果被启用，位掩码会限制 libcurl 在 <strong><code>CURLOPT_FOLLOWLOCATION</code></strong>开启时，使用的协议。 默认允许除 FILE 和 SCP 外所有协议。 这和 7.19.4 前的版本无条件支持所有支持的协议不同。关于协议常量，请参照<strong><code>CURLOPT_PROTOCOLS</code></strong>。</td>
<td>在 cURL 7.19.4 中被加入。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_RESUME_FROM</code></strong></td>
<td>在恢复传输时，传递字节为单位的偏移量（用来断点续传）。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSL_OPTIONS</code></strong></td>
<td>Set SSL behavior options, which is a bitmask of any of the following constants: <span class="simpara"> <strong><code>CURLSSLOPT_ALLOW_BEAST</code></strong>: do not attempt to use any workarounds for a security flaw in the SSL3 and TLS1.0 protocols. </span> <span class="simpara"> <strong><code>CURLSSLOPT_NO_REVOKE</code></strong>: disable certificate revocation checks for those SSL backends where such behavior is present. </span></td>
<td>Added in cURL 7.25.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSL_VERIFYHOST</code></strong></td>
<td>设置为 <em>1</em> 是检查服务器SSL证书中是否存在一个公用名(common name)。译者注：公用名(Common Name)一般来讲就是填写你将要申请SSL证书的域名 (domain)或子域名(sub domain)。 设置成 2，会检查公用名是否存在，并且是否与提供的主机名匹配。 <em>0</em> 为不检查名称。 在生产环境中，这个值应该是 <em>2</em>（默认值）。</td>
<td>值 <em>1</em> 的支持在 cURL 7.28.1 中被删除了。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSLVERSION</code></strong></td>
<td><strong><code>CURL_SSLVERSION_DEFAULT</code></strong> (0), <strong><code>CURL_SSLVERSION_TLSv1</code></strong> (1), <strong><code>CURL_SSLVERSION_SSLv2</code></strong> (2), <strong><code>CURL_SSLVERSION_SSLv3</code></strong> (3), <strong><code>CURL_SSLVERSION_TLSv1_0</code></strong> (4), <strong><code>CURL_SSLVERSION_TLSv1_1</code></strong> (5) ， <strong><code>CURL_SSLVERSION_TLSv1_2</code></strong> (6) 中的其中一个。
<blockquote>
<p><strong>Note</strong>:</p>
<p>你最好别设置这个值，让它使用默认值。 设置为 2 或 3 比较危险，在 SSLv2 和 SSLv3 中有弱点存在。</p>
</blockquote></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_STREAM_WEIGHT</code></strong></td>
<td>设置 stream weight 数值 ( 1 和 256 之间的数字).</td>
<td>cURL 7.46.0 中添加，自 PHP 7.0.7 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_TIMECONDITION</code></strong></td>
<td>设置如何对待 <strong><code>CURLOPT_TIMEVALUE</code></strong>。 使用 <code class="parameter">CURL_TIMECOND_IFMODSINCE</code>，仅在页面 <strong><code>CURLOPT_TIMEVALUE</code></strong> 之后修改，才返回页面。没有修改则返回 <em>"304 Not Modified"</em> 头，假设设置了 <strong><code>CURLOPT_HEADER</code></strong> 为 <strong><code>true</code></strong>。<code class="parameter">CURL_TIMECOND_IFUNMODSINCE</code>则起相反的效果。 默认为 <code class="parameter">CURL_TIMECOND_IFMODSINCE</code>。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_TIMEOUT</code></strong></td>
<td>允许 cURL 函数执行的最长秒数。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_TIMEOUT_MS</code></strong></td>
<td>设置cURL允许执行的最长毫秒数。 如果 libcurl 编译时使用系统标准的名称解析器（ standard system name resolver），那部分的连接仍旧使用以秒计的超时解决方案，最小超时时间还是一秒钟。</td>
<td>在 cURL 7.16.2 中被加入。从 PHP 5.2.3 起可使用。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_TIMEVALUE</code></strong></td>
<td>秒数，从 1970年1月1日开始。这个时间会被 <strong><code>CURLOPT_TIMECONDITION</code></strong>使。默认使用<code class="parameter">CURL_TIMECOND_IFMODSINCE</code>。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_MAX_RECV_SPEED_LARGE</code></strong></td>
<td>如果下载速度超过了此速度(以每秒字节数来统计) ，即传输过程中累计的平均数，传输就会降速到这个参数的值。默认不限速。</td>
<td>cURL 7.15.5 中添加， PHP 5.4.0 有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_MAX_SEND_SPEED_LARGE</code></strong></td>
<td>如果上传的速度超过了此速度(以每秒字节数来统计)，即传输过程中累计的平均数 ，传输就会降速到这个参数的值。默认不限速。</td>
<td>cURL 7.15.5 中添加， PHP 5.4.0 有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSH_AUTH_TYPES</code></strong></td>
<td>A bitmask consisting of one or more of <strong><code>CURLSSH_AUTH_PUBLICKEY</code></strong>, <strong><code>CURLSSH_AUTH_PASSWORD</code></strong>, <strong><code>CURLSSH_AUTH_HOST</code></strong>, <strong><code>CURLSSH_AUTH_KEYBOARD</code></strong>. Set to <strong><code>CURLSSH_AUTH_ANY</code></strong> to let libcurl pick one.</td>
<td>cURL 7.16.1 中添加。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_IPRESOLVE</code></strong></td>
<td>允许程序选择想要解析的 IP 地址类别。只有在地址有多种 ip 类别的时候才能用，可以的值有： <strong><code>CURL_IPRESOLVE_WHATEVER</code></strong>、 <strong><code>CURL_IPRESOLVE_V4</code></strong>、 <strong><code>CURL_IPRESOLVE_V6</code></strong>，默认是 <strong><code>CURL_IPRESOLVE_WHATEVER</code></strong>。</td>
<td>cURL 7.10.8 中添加。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_FTP_FILEMETHOD</code></strong></td>
<td>告诉 curl 使用哪种方式来获取 FTP(s) 服务器上的文件。可能的值有： <strong><code>CURLFTPMETHOD_MULTICWD</code></strong>、 <strong><code>CURLFTPMETHOD_NOCWD</code></strong> 和 <strong><code>CURLFTPMETHOD_SINGLECWD</code></strong>。</td>
<td>cURL 7.15.1 中添加， PHP 5.3.0 起有效。</td>
</tr>
</tbody>
</table>

对于下面的这些`option`，`value`应该被设置成 <span
class="type">string</span>：

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>选项</th>
<th>设置的<code class="parameter">value</code></th>
<th>备注</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>CURLOPT_CAINFO</code></strong></td>
<td>一个保存着1个或多个用来让服务端验证的证书的文件名。这个参数仅仅在和<strong><code>CURLOPT_SSL_VERIFYPEER</code></strong>一起使用时才有意义。 .</td>
<td>可能需要绝对路径。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_CAPATH</code></strong></td>
<td>一个保存着多个CA证书的目录。这个选项是和<strong><code>CURLOPT_SSL_VERIFYPEER</code></strong>一起使用的。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_COOKIE</code></strong></td>
<td>设定 HTTP 请求中<em>"Cookie: "</em>部分的内容。多个 cookie 用分号分隔，分号后带一个空格(例如， "<em>fruit=apple; colour=red</em>")。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_COOKIEFILE</code></strong></td>
<td>包含 cookie 数据的文件名，cookie 文件的格式可以是 Netscape 格式，或者只是纯 HTTP 头部风格，存入文件。如果文件名是空的，不会加载 cookie，但 cookie 的处理仍旧启用。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_COOKIEJAR</code></strong></td>
<td>连接结束后，比如，调用 curl_close 后，保存 cookie 信息的文件。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_CUSTOMREQUEST</code></strong></td>
<td><p>HTTP 请求时，使用自定义的 Method 来代替<em>"GET"</em>或<em>"HEAD"</em>。对 <em>"DELETE"</em> 或者其他更隐蔽的 HTTP 请求有用。 有效值如 <em>"GET"</em>，<em>"POST"</em>，<em>"CONNECT"</em>等等；也就是说，不要在这里输入整行 HTTP 请求。例如输入<em>"GET /index.html HTTP/1.0\r\n\r\n"</em>是不正确的。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>不确定服务器支持这个自定义方法则不要使用它。</p>
</blockquote></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_DEFAULT_PROTOCOL</code></strong></td>
<td><p>URL不带协议的时候，使用的默认协议。</p></td>
<td>cURL 7.45.0 中添加，自 PHP 7.0.7 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_DNS_INTERFACE</code></strong></td>
<td><p>Set the name of the network interface that the DNS resolver should bind to. This must be an interface name (not an address).</p></td>
<td>Added in cURL 7.33.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_DNS_LOCAL_IP4</code></strong></td>
<td><p>Set the local IPv4 address that the resolver should bind to. The argument should contain a single numerical IPv4 address as a string.</p></td>
<td>Added in cURL 7.33.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_DNS_LOCAL_IP6</code></strong></td>
<td><p>Set the local IPv6 address that the resolver should bind to. The argument should contain a single numerical IPv6 address as a string.</p></td>
<td>Added in cURL 7.33.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_EGDSOCKET</code></strong></td>
<td>类似<strong><code>CURLOPT_RANDOM_FILE</code></strong>，除了一个Entropy Gathering Daemon套接字。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_ENCODING</code></strong></td>
<td>HTTP请求头中<em>"Accept-Encoding: "</em>的值。 这使得能够解码响应的内容。 支持的编码有<em>"identity"</em>，<em>"deflate"</em>和<em>"gzip"</em>。如果为空字符串<em>""</em>，会发送所有支持的编码类型。</td>
<td>在 cURL 7.10 中被加入。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_FTPPORT</code></strong></td>
<td>这个值将被用来获取供FTP"PORT"指令所需要的IP地址。 "PORT" 指令告诉远程服务器连接到我们指定的IP地址。这个字符串可以是纯文本的IP地址、主机名、一个网络接口名（UNIX下）或者只是一个'-'来使用默认的 IP 地址。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_INTERFACE</code></strong></td>
<td>发送的网络接口（interface），可以是一个接口名、IP 地址或者是一个主机名。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_KEYPASSWD</code></strong></td>
<td>使用 <strong><code>CURLOPT_SSLKEY</code></strong> 或 <strong><code>CURLOPT_SSH_PRIVATE_KEYFILE</code></strong> 私钥时候的密码。</td>
<td>在 cURL 7.16.1 中添加。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_KRB4LEVEL</code></strong></td>
<td>KRB4 (Kerberos 4) 安全级别。下面的任何值都是有效的(从低到高的顺序)：<em>"clear"</em>、<em>"safe"</em>、<em>"confidential"</em>、<em>"private".</em>。如果字符串以上这些，将使用<em>"private"</em>。 这个选项设置为 <strong><code>null</code></strong> 时将禁用 KRB4 安全认证。目前 KRB4 安全认证只能用于 FTP 传输。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_LOGIN_OPTIONS</code></strong></td>
<td>Can be used to set protocol specific login options, such as the preferred authentication mechanism via "AUTH=NTLM" or "AUTH=*", and should be used in conjunction with the <strong><code>CURLOPT_USERNAME</code></strong> option.</td>
<td>Added in cURL 7.34.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PINNEDPUBLICKEY</code></strong></td>
<td>Set the pinned public key. The string can be the file name of your pinned public key. The file format expected is "PEM" or "DER". The string can also be any number of base64 encoded sha256 hashes preceded by "sha256//" and separated by ";".</td>
<td>Added in cURL 7.39.0. Available since PHP 7.0.7.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_POSTFIELDS</code></strong></td>
<td><span class="simpara"> 全部数据使用HTTP协议中的 "POST" 操作来发送。 要发送文件，在文件名前面加上<em>@</em>前缀并使用完整路径。 文件类型可在文件名后以 '<em>;type=mimetype</em>' 的格式指定。 这个参数可以是 urlencoded 后的字符串，类似'<em>para1=val1&amp;para2=val2&amp;...</em>'，也可以使用一个以字段名为键值，字段数据为值的数组。 如果<code class="parameter">value</code>是一个数组，<em>Content-Type</em>头将会被设置成<em>multipart/form-data</em>。 </span> <span class="simpara"> 从 PHP 5.2.0 开始，使用 <em>@</em> 前缀传递文件时，<code class="parameter">value</code> 必须是个数组。 </span> <span class="simpara"> 从 PHP 5.5.0 开始, <em>@</em> 前缀已被废弃，文件可通过 <span class="classname">CURLFile</span> 发送。 设置 <strong><code>CURLOPT_SAFE_UPLOAD</code></strong> 为 <strong><code>true</code></strong> 可禁用 <em>@</em> 前缀发送文件，以增加安全性。 </span></td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PRIVATE</code></strong></td>
<td>Any data that should be associated with this cURL handle. This data can subsequently be retrieved with the <strong><code>CURLINFO_PRIVATE</code></strong> option of <span class="function">curl_getinfo</span>. cURL does nothing with this data. When using a cURL multi handle, this private data is typically a unique key to identify a standard cURL handle.</td>
<td>Added in cURL 7.10.3.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PROXY</code></strong></td>
<td>HTTP 代理通道。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PROXY_SERVICE_NAME</code></strong></td>
<td>代理验证服务的名称。</td>
<td>cURL 7.34.0 中添加，PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PROXYUSERPWD</code></strong></td>
<td>一个用来连接到代理的<em>"[username]:[password]"</em>格式的字符串。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_RANDOM_FILE</code></strong></td>
<td>一个被用来生成 SSL 随机数种子的文件名。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_RANGE</code></strong></td>
<td>以<em>"X-Y"</em>的形式，其中X和Y都是可选项获取数据的范围，以字节计。HTTP传输线程也支持几个这样的重复项中间用逗号分隔如<em>"X-Y,N-M"</em>。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_REFERER</code></strong></td>
<td>在HTTP请求头中<em>"Referer: "</em>的内容。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SERVICE_NAME</code></strong></td>
<td>验证服务的名称</td>
<td>cURL 7.43.0 起添加，自 PHP 7.0.7 有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSH_HOST_PUBLIC_KEY_MD5</code></strong></td>
<td>包含 32 位长的 16 进制数值。这个字符串应该是远程主机公钥（public key） 的 MD5 校验值。在不匹配的时候 libcurl 会拒绝连接。 此选项仅用于 SCP 和 SFTP 的传输。</td>
<td>cURL 7.17.1 中添加。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSH_PUBLIC_KEYFILE</code></strong></td>
<td>The file name for your public key. If not used, libcurl defaults to $HOME/.ssh/id_dsa.pub if the HOME environment variable is set, and just "id_dsa.pub" in the current directory if HOME is not set.</td>
<td>Added in cURL 7.16.1.</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSH_PRIVATE_KEYFILE</code></strong></td>
<td>The file name for your private key. If not used, libcurl defaults to $HOME/.ssh/id_dsa if the HOME environment variable is set, and just "id_dsa" in the current directory if HOME is not set. If the file is password-protected, set the password with <strong><code>CURLOPT_KEYPASSWD</code></strong>.</td>
<td>Added in cURL 7.16.1.</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSL_CIPHER_LIST</code></strong></td>
<td>一个SSL的加密算法列表。例如<em>RC4-SHA</em>和<em>TLSv1</em>都是可用的加密列表。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSLCERT</code></strong></td>
<td>一个包含 PEM 格式证书的文件名。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSLCERTPASSWD</code></strong></td>
<td>使用<strong><code>CURLOPT_SSLCERT</code></strong>证书需要的密码。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSLCERTTYPE</code></strong></td>
<td>证书的类型。支持的格式有<em>"PEM"</em> (默认值), <em>"DER"</em>和<em>"ENG"</em>。</td>
<td>在 cURL 7.9.3中 被加入。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSLENGINE</code></strong></td>
<td>用来在<strong><code>CURLOPT_SSLKEY</code></strong>中指定的SSL私钥的加密引擎变量。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSLENGINE_DEFAULT</code></strong></td>
<td>用来做非对称加密操作的变量。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSLKEY</code></strong></td>
<td>包含 SSL 私钥的文件名。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_SSLKEYPASSWD</code></strong></td>
<td><p>在 <strong><code>CURLOPT_SSLKEY</code></strong>中指定了的SSL私钥的密码。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>由于这个选项包含了敏感的密码信息，记得保证这个PHP脚本的安全。</p>
</blockquote></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_SSLKEYTYPE</code></strong></td>
<td><strong><code>CURLOPT_SSLKEY</code></strong>中规定的私钥的加密类型，支持的密钥类型为<em>"PEM"</em>(默认值)、<em>"DER"</em>和<em>"ENG"</em>。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_UNIX_SOCKET_PATH</code></strong></td>
<td>使用 Unix 套接字作为连接，并用指定的 <span class="type">string</span> 作为路径。</td>
<td>cURL 7.40.0 中添加， PHP 7.0.7 起有效。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_URL</code></strong></td>
<td>需要获取的 URL 地址，也可以在<span class="function">curl_init</span> 初始化会话的时候。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_USERAGENT</code></strong></td>
<td>在HTTP请求中包含一个<em>"User-Agent: "</em>头的字符串。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_USERNAME</code></strong></td>
<td>验证中使用的用户名。</td>
<td>cURL 7.19.1 中添加，PHP 5.5.0 起有效。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_USERPWD</code></strong></td>
<td>传递一个连接中需要的用户名和密码，格式为：<em>"[username]:[password]"</em>。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_XOAUTH2_BEARER</code></strong></td>
<td>指定 OAuth 2.0 access token。</td>
<td>cURL 7.33.0 中添加，自 PHP 7.0.7 添加。</td>
</tr>
</tbody>
</table>

以下`option`，`value`应该被设置成数组：

| 选项                         | 可选`value`值                                                                                                                                                                 | 备注                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| **`CURLOPT_CONNECT_TO`**     | 连接到指定的主机和端口，替换 URL 中的主机和端口。接受指定字符串格式的数组： *HOST:PORT:CONNECT-TO-HOST:CONNECT-TO-PORT*。                                                     | cURL 7.49.0 中添加， PHP 7.0.7 起有效。      |
| **`CURLOPT_HTTP200ALIASES`** | HTTP 200 响应码数组，数组中的响应码被认为是正确的响应，而非错误。                                                                                                             | 在 cURL 7.10.3 中被加入。                    |
| **`CURLOPT_HTTPHEADER`**     | 设置 HTTP 头字段的数组。格式： `              array('Content-type: text/plain', 'Content-length: 100')             `                                                          |                                              |
| **`CURLOPT_POSTQUOTE`**      | 在 FTP 请求执行完成后，在服务器上执行的一组array格式的 FTP 命令。                                                                                                             |                                              |
| **`CURLOPT_PROXYHEADER`**    | 传给代理的自定义 HTTP 头。                                                                                                                                                    | cURL 7.37.0 中添加，自 PHP 7.0.7 添加。      |
| **`CURLOPT_QUOTE`**          | 一组先于 FTP 请求的在服务器上执行的FTP命令。                                                                                                                                  |                                              |
| **`CURLOPT_RESOLVE`**        | 提供自定义地址，指定了主机和端口。 包含主机、端口和 ip 地址的字符串，组成 array 的，每个元素以冒号分隔。格式： `              array("example.com:80:127.0.0.1")             ` | 在 cURL 7.21.3 中添加，自 PHP 5.5.0 起可用。 |

以下 `option`，`value`应该被设置成流资源 （例如使用<span
class="function">fopen</span>）：

| 选项                      | 可选`value`值                           |
|---------------------------|-----------------------------------------|
| **`CURLOPT_FILE`**        | 设置输出文件，默认为*STDOUT* (浏览器)。 |
| **`CURLOPT_INFILE`**      | 上传文件时需要读取的文件。              |
| **`CURLOPT_STDERR`**      | 错误输出的地址，取代默认的*STDERR*。    |
| **`CURLOPT_WRITEHEADER`** | 设置 header 部分内容的写入的文件地址。  |

以下`option` 的 `value`应该是有效的函数或者闭包：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>选项</th>
<th><code class="parameter">value</code>值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><code>CURLOPT_HEADERFUNCTION</code></strong></td>
<td>设置一个回调函数，这个函数有两个参数，第一个是cURL的资源句柄，第二个是输出的 header 数据。header数据的输出必须依赖这个函数，返回已写入的数据大小。</td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_PASSWDFUNCTION</code></strong></td>
<td>设置一个回调函数，有三个参数，第一个是cURL的资源句柄，第二个是一个密码提示符，第三个参数是密码长度允许的最大值。返回密码的值。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_PROGRESSFUNCTION</code></strong></td>
<td><p>设置一个回调函数，有五个参数，第一个是cURL的资源句柄，第二个是预计要下载的总字节（bytes）数。第三个是目前下载的字节数，第四个是预计传输中总上传字节数，第五个是目前上传的字节数。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>只有设置 <strong><code>CURLOPT_NOPROGRESS</code></strong> 选项为 <strong><code>false</code></strong> 时才会调用这个回调函数。</p>
</blockquote>
<p>返回非零值将中断传输。 传输将设置 <strong><code>CURLE_ABORTED_BY_CALLBACK</code></strong> 错误。</p></td>
</tr>
<tr class="even">
<td><strong><code>CURLOPT_READFUNCTION</code></strong></td>
<td>回调函数名。该函数应接受三个参数。第一个是 cURL resource；第二个是通过选项 <strong><code>CURLOPT_INFILE</code></strong> 传给 cURL 的 stream resource；第三个参数是最大可以读取的数据的数量。回 调函数必须返回一个字符串，长度小于或等于请求的数据量（第三个参数）。一般从传入的 stream resource 读取。返回空字符串作为 <em>EOF</em>（文件结束） 信号。</td>
</tr>
<tr class="odd">
<td><strong><code>CURLOPT_WRITEFUNCTION</code></strong></td>
<td>回调函数名。该函数应接受两个参数。第一个是 cURL resource；第二个是要写入的数据字符串。数 据必须在函数中被保存。 函数必须准确返回写入数据的字节数，否则传输会被一个错误所中 断。</td>
</tr>
</tbody>
</table>

其他值：

| Option              | 设置 `value` 为                                                                                 |
|---------------------|-------------------------------------------------------------------------------------------------|
| **`CURLOPT_SHARE`** | <span class="function">curl\_share\_init</span> 返回的结果。 使 cURL 可以处理共享句柄里的数据。 |

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.7 | 引入 **`CURL_HTTP_VERSION_2`**、 **`CURL_HTTP_VERSION_2_PRIOR_KNOWLEDGE`**、 **`CURL_HTTP_VERSION_2TLS`**、 **`CURL_REDIR_POST_301`**、 **`CURL_REDIR_POST_302`**、 **`CURL_REDIR_POST_303`**、 **`CURL_REDIR_POST_ALL`**、 **`CURL_VERSION_KERBEROS5`**、 **`CURL_VERSION_PSL`**、 **`CURL_VERSION_UNIX_SOCKETS`**、 **`CURLAUTH_NEGOTIATE`**、 **`CURLAUTH_NTLM_WB`**、 **`CURLFTP_CREATE_DIR`**、 **`CURLFTP_CREATE_DIR_NONE`**、 **`CURLFTP_CREATE_DIR_RETRY`**、 **`CURLHEADER_SEPARATE`**、 **`CURLHEADER_UNIFIED`**、 **`CURLMOPT_CHUNK_LENGTH_PENALTY_SIZE`**、 **`CURLMOPT_CONTENT_LENGTH_PENALTY_SIZE`**、 **`CURLMOPT_MAX_HOST_CONNECTIONS`**、 **`CURLMOPT_MAX_PIPELINE_LENGTH`**、 **`CURLMOPT_MAX_TOTAL_CONNECTIONS`**、 **`CURLOPT_CONNECT_TO`**、 **`CURLOPT_DEFAULT_PROTOCOL`**、 **`CURLOPT_DNS_INTERFACE`**、 **`CURLOPT_DNS_LOCAL_IP4`**、 **`CURLOPT_DNS_LOCAL_IP6`**、 **`CURLOPT_EXPECT_100_TIMEOUT_MS`**、 **`CURLOPT_HEADEROPT`**、 **`CURLOPT_LOGIN_OPTIONS`**、 **`CURLOPT_PATH_AS_IS`**、 **`CURLOPT_PINNEDPUBLICKEY`**、 **`CURLOPT_PIPEWAIT`**、 **`CURLOPT_PROXY_SERVICE_NAME`**、 **`CURLOPT_PROXYHEADER`**、 **`CURLOPT_SASL_IR`**、 **`CURLOPT_SERVICE_NAME`**、 **`CURLOPT_SSL_ENABLE_ALPN`**、 **`CURLOPT_SSL_ENABLE_NPN`**、 **`CURLOPT_SSL_FALSESTART`**、 **`CURLOPT_SSL_VERIFYSTATUS`**、 **`CURLOPT_STREAM_WEIGHT`**、 **`CURLOPT_TCP_FASTOPEN`**、 **`CURLOPT_TFTP_NO_OPTIONS`**、 **`CURLOPT_UNIX_SOCKET_PATH`**、 **`CURLOPT_XOAUTH2_BEARER`**、 **`CURLPROTO_SMB`**、 **`CURLPROTO_SMBS`**、 **`CURLPROXY_HTTP_1_0`**、 **`CURLSSH_AUTH_AGENT`** 和 **`CURLSSLOPT_NO_REVOKE`**。 |

### 范例

**示例 \#1 初始化一个新的cURL会话并获取一个网页**

``` php
<?php
// 创建一个新cURL资源
$ch = curl_init();

// 设置URL和相应的选项
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, false);

// 抓取URL并把它传递给浏览器
curl_exec($ch);

//关闭cURL资源，并且释放系统资源
curl_close($ch);
?>
```

**示例 \#2 上传文件 (PHP 5.5.0 后被废弃)**

``` php
<?php

/* http://localhost/upload.php:
print_r($_POST);
print_r($_FILES);
*/

$ch = curl_init();

$data = array('name' => 'Foo', 'file' => '@/home/user/test.png');

curl_setopt($ch, CURLOPT_URL, 'http://localhost/upload.php');
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_SAFE_UPLOAD, false); //  PHP 5.6.0 后必须开启
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

curl_exec($ch);
?>
```

以上例程会输出：

    Array
    (
        [name] => Foo
    )
    Array
    (
        [file] => Array
            (
                [name] => test.png
                [type] => image/png
                [tmp_name] => /tmp/phpcpjNeQ
                [error] => 0
                [size] => 279
            )

    )

### 注释

> **Note**:
>
> 传递一个数组到**`CURLOPT_POSTFIELDS`**，cURL会把数据编码成
> *multipart/form-data*，而然传递一个URL-encoded字符串时，数据会被编码成
> *application/x-www-form-urlencoded*。

### 参见

-   <span class="function">curl\_setopt\_array</span>

curl\_share\_close
==================

关闭 cURL 共享句柄

### 说明

<span class="type">void</span> <span
class="methodname">curl\_share\_close</span> ( <span
class="methodparam"><span class="type">resource</span> `$sh`</span> )

关闭一个 cURL 共享句柄并且释放所有的资源。

### 参数

`sh`  
由<span class="function">curl\_share\_init</span>创建的 cURL 共享句柄。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">curl\_share\_setopt</span>
函数范例：**

以下范例将会创建一个 cURL 共享句柄，并且往其中添加两个 cURL
句柄，最后共享这两个 cURL 句柄的 cookie 数据运行。

``` php
<?php
// Create cURL share handle and set it to share cookie data
$sh = curl_share_init();
curl_share_setopt($sh, CURLSHOPT_SHARE, CURL_LOCK_DATA_COOKIE);

// Initialize the first cURL handle and assign the share handle to it
$ch1 = curl_init("http://example.com/");
curl_setopt($ch1, CURLOPT_SHARE, $sh);

// Execute the first cURL handle
curl_exec($ch1);

// Initialize the second cURL handle and assign the share handle to it
$ch2 = curl_init("http://php.net/");
curl_setopt($ch2, CURLOPT_SHARE, $sh);

// Execute the second cURL handle
//  all cookies from $ch1 handle are shared with $ch2 handle
curl_exec($ch2);

// Close the cURL share handle
curl_share_close($sh);

// Close the cURL handles
curl_close($ch1);
curl_close($ch2);
?>
```

### 参见

-   <span class="function">curl\_share\_init</span>

curl\_share\_errno
==================

返回共享 curl 句柄的最后一次错误号

### 说明

<span class="type">int</span> <span
class="methodname">curl\_share\_errno</span> ( <span
class="methodparam"><span class="type">resource</span> `$sh`</span> )

返回一个整数，表示共享 curl 句柄的最后一次错误号

### 参数

`sh`  
由 <span class="function">curl\_share\_init</span> 函数创建的共享 cURL
句柄。

### 返回值

返回一个整数，表示共享 curl 句柄的最后一次错误号， 或者在失败时返回
**`false`**。

### 参见

-   <span class="function">curl\_errno</span>

curl\_share\_init
=================

初始化一个 cURL 共享句柄。

### 说明

<span class="type">resource</span> <span
class="methodname">curl\_share\_init</span> ( <span
class="methodparam">void</span> )

运行在 cURL 句柄之间共享数据。

### 参数

此函数没有参数。

### 返回值

返回类型为"cURL 共享句柄"的资源。

### 范例

**示例 \#1 <span class="function">curl\_share\_init</span>
函数的范例：**

以下范例将会创建一个 cURL 共享句柄，并且往其中添加两个 cURL
句柄，最后用共享的 cookie 数据运行它们。

``` php
<?php
// 创建 cURL 共享句柄，并设置共享 cookie 数据
$sh = curl_share_init();
curl_share_setopt($sh, CURLSHOPT_SHARE, CURL_LOCK_DATA_COOKIE);

// 初始化第一个 cURL 句柄，并将它设置到共享句柄
$ch1 = curl_init("http://example.com/");
curl_setopt($ch1, CURLOPT_SHARE, $sh);

// 执行第一个 cURL 句柄
curl_exec($ch1);

// 初始化第二个 cURL 句柄，并将它设置到共享句柄
$ch2 = curl_init("http://php.net/");
curl_setopt($ch2, CURLOPT_SHARE, $sh);

// 执行第二个 cURL 句柄
//  all cookies from $ch1 handle are shared with $ch2 handle
curl_exec($ch2);

// 关闭 cURL 共享句柄
curl_share_close($sh);

// 关闭 cURL 共享句柄
curl_close($ch1);
curl_close($ch2);
?>
```

### 参见

-   <span class="function">curl\_share\_setopt</span>
-   <span class="function">curl\_share\_close</span>

curl\_share\_setopt
===================

为 cURL 共享句柄设置选项。

### 说明

<span class="type">bool</span> <span
class="methodname">curl\_share\_setopt</span> ( <span
class="methodparam"><span class="type">resource</span> `$sh`</span> ,
<span class="methodparam"><span class="type">int</span> `$option`</span>
, <span class="methodparam"><span class="type">string</span>
`$value`</span> )

为给定的 cURL 共享句柄设置一个选项。

### 参数

`sh`  
一个由<span class="function">curl\_share\_init</span>函数返回的 cURL
共享句柄。

`option`  
| Option                  | Description              |
|-------------------------|--------------------------|
| **`CURLSHOPT_SHARE`**   | 指定要共享的数据类型。   |
| **`CURLSHOPT_UNSHARE`** | 指定不再共享的数据类型。 |

`value`  
| Value                            | Description                                                                                                               |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| **`CURL_LOCK_DATA_COOKIE`**      | 共享 cookie 数据。                                                                                                        |
| **`CURL_LOCK_DATA_DNS`**         | 共享 DNS 缓存。注意，当你使用 cURL 多句柄时，默认所有添加在同一个多句柄的句柄都将会共享 DNS 缓存。                        |
| **`CURL_LOCK_DATA_SSL_SESSION`** | 共享 SSL 的 session ID, 在重连同样的服务器时减少 SSL 握手时间。注意，SSL 的 session ID 在同一个的句柄中默认是重复使用的。 |

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">curl\_share\_setopt</span>
函数的范例：**

以下范例将会创建一个 cURL 共享句柄，并且往其中添加两个 cURL
句柄，最后共享这两个 cURL 句柄的 cookie 数据运行。

``` php
<?php
// Create cURL share handle and set it to share cookie data
$sh = curl_share_init();
curl_share_setopt($sh, CURLSHOPT_SHARE, CURL_LOCK_DATA_COOKIE);

// Initialize the first cURL handle and assign the share handle to it
$ch1 = curl_init("http://example.com/");
curl_setopt($ch1, CURLOPT_SHARE, $sh);

// Execute the first cURL handle
curl_exec($ch1);

// Initialize the second cURL handle and assign the share handle to it
$ch2 = curl_init("http://php.net/");
curl_setopt($ch2, CURLOPT_SHARE, $sh);

// Execute the second cURL handle
//  all cookies from $ch1 handle are shared with $ch2 handle
curl_exec($ch2);

// Close the cURL share handle
curl_share_close($sh);

// Close the cURL handles
curl_close($ch1);
curl_close($ch2);
?>
```

curl\_share\_strerror
=====================

返回错误号对应的错误消息

### 说明

<span class="type">string</span> <span
class="methodname">curl\_share\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errornum`</span> )

返回错误号对应的错误消息。

### 参数

`errornum`  
<a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» cURL error codes</a>
常量。

### 返回值

返回错误消息。如果传入了无效的错误号，返回 **`null`**。

### 参见

-   <span class="function">curl\_share\_errno</span>
-   <span class="function">curl\_strerror</span>

curl\_strerror
==============

返回错误代码的字符串描述

### 说明

<span class="type">string</span> <span
class="methodname">curl\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errornum`</span> )

返回文本错误信息，解释了指定的错误代码。

### 参数

`errornum`  
<a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» cURL 错误代码</a>中的常量之一。

### 返回值

返回错误信息描述，无效的错误代码返回 **`null`** 。

### 范例

**示例 \#1 <span class="function">curl\_errno</span> 函数的范例：**

``` php
<?php
// 以错拼的 URL 协议创建 curl 句柄
$ch = curl_init("htp://example.com/");

// 发送请求
curl_exec($ch);

// 检测错误，显示错误信息
if($errno = curl_errno($ch)) {
    $error_message = curl_strerror($errno);
    echo "cURL error ({$errno}):\n {$error_message}";
}

// 关闭句柄
curl_close($ch);
?>
```

以上例程会输出：

    cURL error (1):
     Unsupported protocol

### 参见

-   <span class="function">curl\_errno</span>
-   <span class="function">curl\_error</span>
-   <a href="http://curl.haxx.se/libcurl/c/libcurl-errors.html" class="link external">» Curl error codes</a>

curl\_unescape
==============

解码给定的 URL 编码的字符串

### 说明

<span class="type">string</span> <span
class="methodname">curl\_unescape</span> ( <span
class="methodparam"><span class="type">resource</span> `$ch`</span> ,
<span class="methodparam"><span class="type">string</span> `$str`</span>
)

该函数解码给定的 URL 编码的字符串。

### 参数

`handle`  
由 <span class="function">curl\_init</span> 返回的 cURL 句柄。

`str`  
需要解码的 URL 编码字符串

### 返回值

返回解码后的字符串 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">curl\_escape</span> 示例**

``` php
<?php
// 创建一个 curl 句柄
$ch = curl_init('http://example.com/redirect.php');

// 发送 HTTP 请求并且遵循重定向
curl_setopt($ch, CURLOPT_FOLLOWLOCATION, 1);
curl_exec($ch);

// 获取最后的有效 URL
$effective_url = curl_getinfo($ch, CURLINFO_EFFECTIVE_URL);
// 结果： "http://example.com/show_location.php?loc=M%C3%BCnchen"

// 解码这个 URL
$effective_url_decoded = curl_unescape($ch, $effective_url);
// "http://example.com/show_location.php?loc=München"

// 关闭句柄
curl_close($ch);
?>
```

### 注释

> **Note**:
>
> <span class="function">curl\_unescape</span> 不会将加号 (+)
> 解码成空格。而 <span class="function">urldecode</span> 会。

### 参见

-   <span class="function">curl\_escape</span>
-   <span class="function">urlencode</span>
-   <span class="function">urldecode</span>
-   <span class="function">rawurlencode</span>
-   <span class="function">rawurldecode</span>

curl\_version
=============

获取 cURL 版本信息

### 说明

<span class="type">array</span> <span
class="methodname">curl\_version</span> (\[ <span
class="methodparam"><span class="type">int</span> `$age`<span
class="initializer"> = CURLVERSION\_NOW</span></span> \] )

返回关于 cURL 版本的信息。

### 参数

`age`  

### 返回值

返回关联数组，包含如下元素：

| 键                   | 值描述                               |
|----------------------|--------------------------------------|
| version\_number      | cURL 24 位版本号                     |
| version              | cURL 版本号，字符串形式              |
| ssl\_version\_number | OpenSSL 24 位版本号                  |
| ssl\_version         | OpenSSL 版本号，字符串形式           |
| libz\_version        | zlib 版本号，字符串形式              |
| host                 | 关于编译cURL主机的信息               |
| age                  |                                      |
| features             | 一个*CURL\_VERSION\_XXX*常量的位掩码 |
| protocols            | 数组，包含 cURL 支持的协议名称       |

### 范例

**示例 \#1 <span class="function">curl\_version</span> 例子**

这个范例将会检查当前 cURL 版本使用<span
class="function">curl\_version</span>返回的 'features'
位掩码中哪些特性是可用的。

``` php
<?php
// 获取cURL版本数组
$version = curl_version();

// 在cURL编译版本中使用位域来检查某些特性
$bitfields = Array(
            'CURL_VERSION_IPV6', 
            'CURL_VERSION_KERBEROS4', 
            'CURL_VERSION_SSL', 
            'CURL_VERSION_LIBZ'
            );


foreach($bitfields as $feature)
{
    echo $feature . ($version['features'] & constant($feature) ? ' matches' : ' does not match');
    echo PHP_EOL;
}
?>
```

**目录**

-   [curl\_close](/ref/curl.html#curl_close) — 关闭 cURL 会话
-   [curl\_copy\_handle](/ref/curl.html#curl_copy_handle) —
    复制一个cURL句柄和它的所有选项
-   [curl\_errno](/ref/curl.html#curl_errno) — 返回最后一次的错误代码
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
-   [curl\_multi\_add\_handle](/ref/curl.html#curl_multi_add_handle) —
    向curl批处理会话中添加单独的curl句柄
-   [curl\_multi\_close](/ref/curl.html#curl_multi_close) —
    关闭一组cURL句柄
-   [curl\_multi\_errno](/ref/curl.html#curl_multi_errno) — 返回上一次
    curl 批处理的错误码
-   [curl\_multi\_exec](/ref/curl.html#curl_multi_exec) — 运行当前 cURL
    句柄的子连接
-   [curl\_multi\_getcontent](/ref/curl.html#curl_multi_getcontent) —
    如果设置了CURLOPT\_RETURNTRANSFER，则返回获取的输出的文本流
-   [curl\_multi\_info\_read](/ref/curl.html#curl_multi_info_read) —
    获取当前解析的cURL的相关传输信息
-   [curl\_multi\_init](/ref/curl.html#curl_multi_init) —
    返回一个新cURL批处理句柄
-   [curl\_multi\_remove\_handle](/ref/curl.html#curl_multi_remove_handle)
    — 移除cURL批处理句柄资源中的某个句柄资源
-   [curl\_multi\_select](/ref/curl.html#curl_multi_select) —
    等待所有cURL批处理中的活动连接
-   [curl\_multi\_setopt](/ref/curl.html#curl_multi_setopt) — 为 cURL
    并行处理设置一个选项
-   [curl\_multi\_strerror](/ref/curl.html#curl_multi_strerror) —
    返回字符串描述的错误代码
-   [curl\_pause](/ref/curl.html#curl_pause) — 暂停和取消暂停一个连接。
-   [curl\_reset](/ref/curl.html#curl_reset) — 重置一个 libcurl
    会话句柄的所有的选项
-   [curl\_setopt\_array](/ref/curl.html#curl_setopt_array) — 为 cURL
    传输会话批量设置选项
-   [curl\_setopt](/ref/curl.html#curl_setopt) — 设置 cURL 传输选项
-   [curl\_share\_close](/ref/curl.html#curl_share_close) — 关闭 cURL
    共享句柄
-   [curl\_share\_errno](/ref/curl.html#curl_share_errno) — 返回共享
    curl 句柄的最后一次错误号
-   [curl\_share\_init](/ref/curl.html#curl_share_init) — 初始化一个
    cURL 共享句柄。
-   [curl\_share\_setopt](/ref/curl.html#curl_share_setopt) — 为 cURL
    共享句柄设置选项。
-   [curl\_share\_strerror](/ref/curl.html#curl_share_strerror) —
    返回错误号对应的错误消息
-   [curl\_strerror](/ref/curl.html#curl_strerror) —
    返回错误代码的字符串描述
-   [curl\_unescape](/ref/curl.html#curl_unescape) — 解码给定的 URL
    编码的字符串
-   [curl\_version](/ref/curl.html#curl_version) — 获取 cURL 版本信息
