base64\_decode
==============

对使用 MIME base64 编码的数据进行解码

### 说明

<span class="type">string</span> <span
class="methodname">base64\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$strict`<span
class="initializer"> = false</span></span> \] )

对 base64 编码的 `data` 进行解码。

### 参数

`data`  
编码过的数据。

`strict`  
当设置 `strict` 为 **`true`** 时，一旦输入的数据超出了 base64
字母表，将返回 **`false`**。 否则会静默丢弃无效的字符。

### 返回值

返回原始数据， 或者在失败时返回 **`false`**。返回的数据可能是二进制的。

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 5.2.0 | 增加了 `strict` 。 |

### 范例

**示例 \#1 <span class="function">base64\_decode</span> 示例**

``` php
<?php
$str = 'VGhpcyBpcyBhbiBlbmNvZGVkIHN0cmluZw==';
echo base64_decode($str);
?>
```

以上例程会输出：

    This is an encoded string

### 参见

-   <span class="function">base64\_encode</span>
-   <a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC 2045</a>
    的 6.8 章节。

base64\_encode
==============

使用 MIME base64 对数据进行编码

### 说明

<span class="type">string</span> <span
class="methodname">base64\_encode</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

使用 base64 对 `data` 进行编码。

设计此种编码是为了使二进制数据可以通过非纯 8-bit
的传输层传输，例如电子邮件的主体。

Base64-encoded 数据要比原始数据多占用 33% 左右的空间。

### 参数

`data`  
要编码的数据。

### 返回值

编码后的字符串数据， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">base64\_encode</span> 示例**

``` php
<?php
$str = 'This is an encoded string';
echo base64_encode($str);
?>
```

以上例程会输出：

    VGhpcyBpcyBhbiBlbmNvZGVkIHN0cmluZw==

### 参见

-   <span class="function">base64\_decode</span>
-   <span class="function">chunk\_split</span>
-   <span class="function">convert\_uuencode</span>
-   <a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC 2045</a>
    6.8 章节

get\_headers
============

取得服务器响应一个 HTTP 请求所发送的所有标头

### 说明

<span class="type">array</span> <span
class="methodname">get\_headers</span> ( <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 0</span></span> \] )

<span class="function">get\_headers</span>
返回一个数组，包含有服务器响应一个 HTTP 请求所发送的标头。

### 参数

`url`  
目标 URL。

`format`  
如果将可选的 `format` 参数设为 1，则 <span
class="function">get\_headers</span> 会解析相应的信息并设定数组的键名。

### 返回值

返回包含有服务器响应一个 HTTP
请求所发送标头的索引或关联数组，如果失败则返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                           |
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| 5.1.3 | 自 PHP 5.1.3 起本函数使用默认的流上下文，其可以用 <span class="function">stream\_context\_get\_default</span> 函数设定和修改。 |

### 范例

**示例 \#1 <span class="function">get\_headers</span> 例子**

``` php
<?php
$url = 'http://www.example.com';

print_r(get_headers($url));

print_r(get_headers($url, 1));
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => HTTP/1.1 200 OK
        [1] => Date: Sat, 29 May 2004 12:28:13 GMT
        [2] => Server: Apache/1.3.27 (Unix)  (Red-Hat/Linux)
        [3] => Last-Modified: Wed, 08 Jan 2003 23:11:55 GMT
        [4] => ETag: "3f80f-1b6-3e1cb03b"
        [5] => Accept-Ranges: bytes
        [6] => Content-Length: 438
        [7] => Connection: close
        [8] => Content-Type: text/html
    )

    Array
    (
        [0] => HTTP/1.1 200 OK
        [Date] => Sat, 29 May 2004 12:28:14 GMT
        [Server] => Apache/1.3.27 (Unix)  (Red-Hat/Linux)
        [Last-Modified] => Wed, 08 Jan 2003 23:11:55 GMT
        [ETag] => "3f80f-1b6-3e1cb03b"
        [Accept-Ranges] => bytes
        [Content-Length] => 438
        [Connection] => close
        [Content-Type] => text/html
    )

**示例 \#2 <span class="function">get\_headers</span> using HEAD
example**

``` php
<?php
// By default get_headers uses a GET request to fetch the headers. If you
// want to send a HEAD request instead, you can do so using a stream context:
stream_context_set_default(
    array(
        'http' => array(
            'method' => 'HEAD'
        )
    )
);
$headers = get_headers('http://example.com');
?>
```

### 参见

-   <span class="function">apache\_request\_headers</span>

get\_meta\_tags
===============

从一个文件中提取所有的 meta 标签 content 属性，返回一个数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_meta\_tags</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> = false</span></span> \] )

打开 `filename` 逐行解析文件中的 \<meta\> 标签。解析工作将在 *\</head\>*
处停止。

### 参数

`filename`  
HTML 文件的路径字符串。 此参数可以是本地文件也可以是一个 URL。

**示例 \#1 <span class="function">get\_meta\_tags</span> 解析了什么**

``` html
<meta name="author" content="name">
<meta name="keywords" content="php documentation">
<meta name="DESCRIPTION" content="a php manual">
<meta name="geo.position" content="49.33;-86.59">
</head> <!-- 解析工作在此处停止 -->
```

（注意回车换行 － PHP 使用一个本地函数来解析输入，所以 Mac
上的文件将不能在 Unix 上正常工作）。

`use_include_path`  
将 `use_include_path` 设置为 **`true`** 将使 PHP 尝试按照
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
标准包含路径中的每个指向去打开文件。这只用于本地文件，不适用于 URL。

### 返回值

返回一个数组，包含所有解析过的 meta 标签。

返回的关联数组以属性 name 的值作为键，属性 content
的值作为值，所以你可以很容易地使用标准数组函数遍历此关联数组或访问某个值。
属性 name 中的特殊字符将使用‘\_’替换，而其它字符则转换成小写。如果有两个
meta 标签拥有相同的 name，则只返回最后出现的那一个。

### 更新日志

| 版本  | 说明                                     |
|-------|------------------------------------------|
| 4.0.5 | 开始支持没有使用引号括起来的 HTML 属性。 |

### 范例

**示例 \#2 <span class="function">get\_meta\_tags</span> 返回什么些**

``` php
<?php
// 假设上边的标签是在 www.example.com 中
$tags = get_meta_tags('http://www.example.com/');

// 注意所有的键（key）均为小写，而键中的‘.’则转换成了‘_’。
echo $tags['author'];       // name
echo $tags['keywords'];     // php documentation
echo $tags['description'];  // a php manual
echo $tags['geo_position']; // 49.33;-86.59
?>
```

### 注释

> **Note**:
>
> 只有包含 name 属性的 meta 标签才会被解析。

### 参见

-   <span class="function">htmlentities</span>
-   <span class="function">urlencode</span>

http\_build\_query
==================

生成 URL-encode 之后的请求字符串

### 说明

<span class="type">string</span> <span
class="methodname">http\_build\_query</span> ( <span
class="methodparam"><span class="type">mixed</span> `$query_data`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$numeric_prefix`</span> \[, <span class="methodparam"><span
class="type">string</span> `$arg_separator`</span> \[, <span
class="methodparam"><span class="type">int</span> `$enc_type`<span
class="initializer"> = **`PHP_QUERY_RFC1738`**</span></span> \]\]\] )

使用给出的关联（或下标）数组生成一个经过 URL-encode 的请求字符串。

### 参数

`query_data`  
可以是数组或包含属性的对象。

一个 `query_data`
数组可以是简单的一维结构，也可以是由数组组成的数组（其依次可以包含其它数组）。

如果 `query_data` 是一个对象，只有 public 的属性会加入结果。

`numeric_prefix`  
如果在基础数组中使用了数字下标同时给出了该参数，此参数值将会作为基础数组中的数字下标元素的前缀。

这是为了让 PHP 或其它 CGI 程序在稍后对数据进行解码时获取合法的变量名。

`arg_separator`  
除非指定并使用了这个参数，否则会用
<a href="/ini/core.html#ini.arg-separator.output" class="link">arg_separator.output</a>
来分隔参数。

`enc_type`  
默认使用 **`PHP_QUERY_RFC1738`**。

如果 `enc_type` 是 **`PHP_QUERY_RFC1738`**，则编码将会以
<a href="http://www.faqs.org/rfcs/rfc1738" class="link external">» RFC 1738</a>
标准和 *application/x-www-form-urlencoded*
媒体类型进行编码，空格会被编码成加号（*+*）。

如果 `enc_type` 是 **`PHP_QUERY_RFC3986`**，将根据
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>
编码，空格会被百分号编码（*%20*）。

### 返回值

返回一个 URL 编码后的字符串。

### 更新日志

| 版本  | 说明                         |
|-------|------------------------------|
| 5.4.0 | 加入了 `enc_type` 参数。     |
| 5.1.3 | 方括号也会被转义。           |
| 5.1.2 | 加入了参数 `arg_separator`。 |

### 范例

**示例 \#1 <span class="function">http\_build\_query</span> 使用示例**

``` php
<?php
$data = array('foo'=>'bar',
              'baz'=>'boom',
              'cow'=>'milk',
              'php'=>'hypertext processor');

echo http_build_query($data) . "\n";
echo http_build_query($data, '', '&amp;');

?>
```

以上例程会输出：

    foo=bar&baz=boom&cow=milk&php=hypertext+processor
    foo=bar&amp;baz=boom&amp;cow=milk&amp;php=hypertext+processor

**示例 \#2 <span class="function">http\_build\_query</span>
使用数字下标的元素**

``` php
<?php
$data = array('foo', 'bar', 'baz', 'boom', 'cow' => 'milk', 'php' =>'hypertext processor');

echo http_build_query($data) . "\n";
echo http_build_query($data, 'myvar_');
?>
```

以上例程会输出：

    0=foo&1=bar&2=baz&3=boom&cow=milk&php=hypertext+processor
    myvar_0=foo&myvar_1=bar&myvar_2=baz&myvar_3=boom&cow=milk&php=hypertext+processor

**示例 \#3 <span class="function">http\_build\_query</span>
使用复杂的数组**

``` php
<?php
$data = array('user'=>array('name'=>'Bob Smith',
                            'age'=>47,
                            'sex'=>'M',
                            'dob'=>'5/12/1956'),
              'pastimes'=>array('golf', 'opera', 'poker', 'rap'),
              'children'=>array('bobby'=>array('age'=>12,
                                               'sex'=>'M'),
                                'sally'=>array('age'=>8,
                                               'sex'=>'F')),
              'CEO');

echo http_build_query($data, 'flags_');
?>
```

这会输出：（为了可读性，字已经换行了）

    user%5Bname%5D=Bob+Smith&user%5Bage%5D=47&user%5Bsex%5D=M&
    user%5Bdob%5D=5%2F12%2F1956&pastimes%5B0%5D=golf&pastimes%5B1%5D=opera&
    pastimes%5B2%5D=poker&pastimes%5B3%5D=rap&children%5Bbobby%5D%5Bage%5D=12&
    children%5Bbobby%5D%5Bsex%5D=M&children%5Bsally%5D%5Bage%5D=8&
    children%5Bsally%5D%5Bsex%5D=F&flags_0=CEO

> **Note**:
>
> 只有基础数组中的数字下标元素“CEO”才获取了前缀，其它数字下标元素（如
> pastimes 下的元素）则不需要为了合法的变量名而加上前缀。

**示例 \#4 <span class="function">http\_build\_query</span> 使用对象**

``` php
<?php
class parentClass {
    public    $pub      = 'publicParent';
    protected $prot     = 'protectedParent';
    private   $priv     = 'privateParent';
    public    $pub_bar  = Null;
    protected $prot_bar = Null;
    private   $priv_bar = Null;

    public function __construct(){
        $this->pub_bar  = new childClass();
        $this->prot_bar = new childClass();
        $this->priv_bar = new childClass();
    }
}

class childClass {
    public    $pub  = 'publicChild';
    protected $prot = 'protectedChild';
    private   $priv = 'privateChild';
}

$parent = new parentClass();

echo http_build_query($parent);
?>
```

以上例程会输出：

    pub=publicParent&pub_bar%5Bpub%5D=publicChild

### 参见

-   <span class="function">parse\_str</span>
-   <span class="function">parse\_url</span>
-   <span class="function">urlencode</span>
-   <span class="function">array\_walk</span>

parse\_url
==========

解析 URL，返回其组成部分

### 说明

<span class="type">mixed</span> <span
class="methodname">parse\_url</span> ( <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">int</span> `$component`<span
class="initializer"> = -1</span></span> \] )

本函数解析一个 URL 并返回一个关联数组，包含在 URL 中出现的各种组成部分。

本函数*不是*用来验证给定 URL
的合法性的，只是将其分解为下面列出的部分。不完整的 URL 也被接受，<span
class="function">parse\_url</span> 会尝试尽量正确地将其解析。

### 参数

`url`  
要解析的 URL。无效字符将使用 *\_* 来替换。

<!-- -->

`component`  
指定 **`PHP_URL_SCHEME`**、 **`PHP_URL_HOST`**、 **`PHP_URL_PORT`**、
**`PHP_URL_USER`**、 **`PHP_URL_PASS`**、 **`PHP_URL_PATH`**、
**`PHP_URL_QUERY`** 或 **`PHP_URL_FRAGMENT`** 的其中一个来获取 URL
中指定的部分的 <span class="type">string</span>。 （除了指定为
**`PHP_URL_PORT`** 后，将返回一个 <span class="type">integer</span>
的值）。

### 返回值

对严重不合格的 URL，<span class="function">parse\_url</span> 可能会返回
**`false`**。

如果省略了 `component` 参数，将返回一个关联数组 <span
class="type">array</span>，在目前至少会有一个元素在该数组中。数组中可能的键有以下几种：

-   <span class="simpara"> `scheme` - 如 http </span>
-   <span class="simpara"> `host` </span>
-   <span class="simpara"> `port` </span>
-   <span class="simpara"> `user` </span>
-   <span class="simpara"> `pass` </span>
-   <span class="simpara"> `path` </span>
-   <span class="simpara"> `query` - 在问号 *?* 之后 </span>
-   <span class="simpara"> `fragment` - 在散列符号 *\#* 之后 </span>

如果指定了 `component` 参数， <span class="function">parse\_url</span>
返回一个 <span class="type">string</span> （或在指定为
**`PHP_URL_PORT`** 时返回一个 <span class="type">integer</span>）而不是
<span class="type">array</span>。如果 URL
中指定的组成部分不存在，将会返回 **`null`**。

### 更新日志

| 版本  | 说明                                                     |
|-------|----------------------------------------------------------|
| 5.4.7 | 修复了 *host* 在 *协议* 省略时的识别。                   |
| 5.3.3 | 在 URL 解析失败时将不会产生 **`E_WARNING`** 级别的错误。 |
| 5.1.2 | 增加了参数 `component`。                                 |

### 范例

**示例 \#1 <span class="function">parse\_url</span> 例子**

``` php
<?php
$url = 'http://username:password@hostname/path?arg=value#anchor';

print_r(parse_url($url));

echo parse_url($url, PHP_URL_PATH);
?>
```

以上例程会输出：

    Array
    (
        [scheme] => http
        [host] => hostname
        [user] => username
        [pass] => password
        [path] => /path
        [query] => arg=value
        [fragment] => anchor
    )
    /path

**示例 \#2 <span class="function">parse\_url</span> 解析丢失协议的例子**

``` php
<?php
$url = '//www.example.com/path?googleguy=googley';

// 在 5.4.7 之前这会输出路径 "//www.example.com/path"
var_dump(parse_url($url));
?>
```

以上例程会输出：

    array(3) {
      ["host"]=>
      string(15) "www.example.com"
      ["path"]=>
      string(5) "/path"
      ["query"]=>
      string(17) "googleguy=googley"
    }

### 注释

> **Note**:
>
> 本函数不能用于相对 URL。

> **Note**:
>
> <span class="function">parse\_url</span> 是专门用来解析 URL 而不是 URI
> 的。不过为遵从 PHP 向后兼容的需要有个例外，对 file://
> 协议允许三个斜线（file:///...）。其它任何协议都不能这样。

### 参见

-   <span class="function">pathinfo</span>
-   <span class="function">parse\_str</span>
-   <span class="function">http\_build\_query</span>
-   <span class="function">http\_build\_url</span>
-   <span class="function">dirname</span>
-   <span class="function">basename</span>
-   <a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>

rawurldecode
============

对已编码的 URL 字符串进行解码

### 说明

<span class="type">string</span> <span
class="methodname">rawurldecode</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

返回字符串，此字符串中百分号（*%*）后跟两位十六进制数的序列都将被替换成原义字符。

### 参数

`str`  
要解码的 URL。

### 返回值

返回解码后的 URL 字符串。

### 范例

**示例 \#1 <span class="function">rawurldecode</span> 示例**

``` php
<?php

echo rawurldecode('foo%20bar%40baz'); // foo bar@baz

?>
```

### 注释

> **Note**:
>
> <span class="function">rawurldecode</span>
> 不会把加号（'+'）解码为空格，而 <span
> class="function">urldecode</span> 可以。

### 参见

-   <span class="function">rawurlencode</span>
-   <span class="function">urldecode</span>
-   <span class="function">urlencode</span>
-   <a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>

rawurlencode
============

按照 RFC 3986 对 URL 进行编码

### 说明

<span class="type">string</span> <span
class="methodname">rawurlencode</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

根据
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>
编码指定的字符。

### 参数

`str`  
要编码的 URL。

### 返回值

返回字符串，此字符串中除了 *-\_.*
之外的所有非字母数字字符都将被替换成百分号（*%*）后跟两位十六进制数。这是在
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>
中描述的编码，是为了保护原义字符以免其被解释为特殊的 URL
定界符，同时保护 URL
格式以免其被传输媒体（像一些邮件系统）使用字符转换时弄乱。

> **Note**:
>
> 在 PHP 5.3.0 之前，rawurlencode 根据
> <a href="http://www.faqs.org/rfcs/rfc1738" class="link external">» RFC 1738</a>
> 来编码波浪线（*\~*）。

### 更新日志

| 版本  | 说明                                                                                        |
|-------|---------------------------------------------------------------------------------------------|
| 5.3.4 | 因为 <span class="function">rawurlencode</span> 使用了 EBCDIC，所以波浪线字符不会再被编码。 |
| 5.3.0 | 现在符合了<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>。 |

### 范例

**示例 \#1 在 FTP URL 里包含一个密码**

``` php
<?php
echo '<a href="ftp://user:', rawurlencode('foo @+%/'),
     '@ftp.example.com/x.txt">';
?>
```

以上例程会输出：

    <a href="ftp://user:foo%20%40%2B%25%2F@ftp.example.com/x.txt">

或者，如果你想通过 URL 的 PATH\_INFO 构成部分去传递信息：

**示例 \#2 <span class="function">rawurlencode</span> 示例 2**

``` php
<?php
echo '<a href="http://example.com/department_list_script/',
    rawurlencode('sales and marketing/Miami'), '">';
?>
```

以上例程会输出：

    <a href="http://example.com/department_list_script/sales%20and%20marketing%2FMiami">

### 参见

-   <span class="function">rawurldecode</span>
-   <span class="function">urldecode</span>
-   <span class="function">urlencode</span>
-   <a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>

urldecode
=========

解码已编码的 URL 字符串

### 说明

<span class="type">string</span> <span
class="methodname">urldecode</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

解码给出的已编码字符串中的任何 *%<span
class="replaceable">\#\#</span>*。 加号（'*+*'）被解码成一个空格字符。

### 参数

`str`  
要解码的字符串。

### 返回值

返回解码后的字符串。

### 范例

**示例 \#1 <span class="function">urldecode</span> 示例**

``` php
<?php
$query = "my=apples&are=green+and+red";

foreach (explode('&', $query) as $chunk) {
    $param = explode("=", $chunk);

    if ($param) {
        printf("Value for parameter \"%s\" is \"%s\"<br/>\n", urldecode($param[0]), urldecode($param[1]));
    }
}
?>
```

### 注释

**Warning**

超全局变量 `$_GET` 和 `$_REQUEST` 已经被解码了。对 `$_GET` 或
`$_REQUEST` 里的元素使用 <span class="function">urldecode</span>
将会导致不可预计和危险的结果。

### 参见

-   <span class="function">urlencode</span>
-   <span class="function">rawurlencode</span>
-   <span class="function">rawurldecode</span>
-   <a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>

urlencode
=========

编码 URL 字符串

### 说明

<span class="type">string</span> <span
class="methodname">urlencode</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

此函数便于将字符串编码并将其用于 URL
的请求部分，同时它还便于将变量传递给下一页。

### 参数

`str`  
要编码的字符串。

### 返回值

返回字符串，此字符串中除了 *-\_.*
之外的所有非字母数字字符都将被替换成百分号（*%*）后跟两位十六进制数，空格则编码为加号（*+*）。此编码与
WWW 表单 POST 数据的编码方式是一样的，同时与
*application/x-www-form-urlencoded*
的媒体类型编码方式一样。由于历史原因，此编码在将空格编码为加号（+）方面与
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC3986</a>
编码（参见 <span class="function">rawurlencode</span>）不同。

### 范例

**示例 \#1 <span class="function">urlencode</span> 例子**

``` php
<?php
echo '<a href="mycgi?foo=', urlencode($userinput), '">';
?>
```

**示例 \#2 <span class="function">urlencode</span> 与 <span
class="function">htmlentities</span> 例子**

``` php
<?php
$query_string = 'foo=' . urlencode($foo) . '&bar=' . urlencode($bar);
echo '<a href="mycgi?' . htmlentities($query_string) . '">';
?>
```

### 注释

> **Note**:
>
> 注意：小心与 HTML 实体相匹配的变量。像 &amp、&copy 和 &pound
> 都将被浏览器解析，并使用实际实体替代所期待的变量名。这是明显的混乱，W3C
> 已经告诫人们好几年了。参考地址：<a href="http://www.w3.org/TR/html4/appendix/notes.html#h-B.2.2" class="link external">» http://www.w3.org/TR/html4/appendix/notes.html#h-B.2.2</a>。
>
> PHP 通过 arg\_separator.ini 指令，支持将参数分割符变成 W3C
> 所建议的分号。不幸的是大多数用户代理并不发送分号分隔符格式的表单数据。较为简单的解决办法是使用
> &amp; 代替 & 作为分隔符。你不需要为此修改 PHP 的
> arg\_separator。让它仍为 &，而仅使用 <span
> class="function">htmlentities</span> 或 <span
> class="function">htmlspecialchars</span> 对你的 URL 进行编码。

### 参见

-   <span class="function">urldecode</span>
-   <span class="function">htmlentities</span>
-   <span class="function">rawurlencode</span>
-   <span class="function">rawurldecode</span>
-   <a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>

**目录**

-   [base64\_decode](/ref/url.html#base64_decode) — 对使用 MIME base64
    编码的数据进行解码
-   [base64\_encode](/ref/url.html#base64_encode) — 使用 MIME base64
    对数据进行编码
-   [get\_headers](/ref/url.html#get_headers) — 取得服务器响应一个 HTTP
    请求所发送的所有标头
-   [get\_meta\_tags](/ref/url.html#get_meta_tags) —
    从一个文件中提取所有的 meta 标签 content 属性，返回一个数组
-   [http\_build\_query](/ref/url.html#http_build_query) — 生成
    URL-encode 之后的请求字符串
-   [parse\_url](/ref/url.html#parse_url) — 解析 URL，返回其组成部分
-   [rawurldecode](/ref/url.html#rawurldecode) — 对已编码的 URL
    字符串进行解码
-   [rawurlencode](/ref/url.html#rawurlencode) — 按照 RFC 3986 对 URL
    进行编码
-   [urldecode](/ref/url.html#urldecode) — 解码已编码的 URL 字符串
-   [urlencode](/ref/url.html#urlencode) — 编码 URL 字符串
