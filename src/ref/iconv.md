参见 <a href="/ref/recode.html" class="link">GNU Recode functions</a>。

iconv\_get\_encoding
====================

获取 iconv 扩展的内部配置变量

### 说明

<span class="type">mixed</span> <span
class="methodname">iconv\_get\_encoding</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`<span
class="initializer"> = "all"</span></span> \] )

获取 iconv 扩展的内部配置变量。

### 参数

`type`  
选项 `type` 的值可以是：

-   all
-   input\_encoding
-   output\_encoding
-   internal\_encoding

### 返回值

成功时返回当前内部配置变量的值， 或者在失败时返回 **`false`**。

如果省略了 `type`，或者设置为 "all"，<span
class="function">iconv\_get\_encoding</span>
返回包含所有这些变量的数组。

### 范例

**示例 \#1 <span class="function">iconv\_get\_encoding</span> 例子**

``` php
<pre>
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
var_dump(iconv_get_encoding('all'));
?>
</pre>
```

以上例程会输出：

    Array
    (
        [input_encoding] => ISO-8859-1
        [output_encoding] => ISO-8859-1
        [internal_encoding] => UTF-8
    )

### 参见

-   <span class="function">iconv\_set\_encoding</span>
-   <span class="function">ob\_iconv\_handler</span>

iconv\_mime\_decode\_headers
============================

一次性解码多个 *MIME* 头字段

### 说明

<span class="type">array</span> <span
class="methodname">iconv\_mime\_decode\_headers</span> ( <span
class="methodparam"><span class="type">string</span>
`$encoded_headers`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$charset`<span class="initializer"> =
ini\_get("iconv.internal\_encoding")</span></span> \]\] )

一次性解码多个 *MIME* 头字段。

### 参数

`encoded_headers`  
编码过的头，是一个字符串。

`mode`  
`mode` 决定了 <span class="function">iconv\_mime\_decode\_headers</span>
遇到畸形 *MIME* 头字段时的行为。 你可以指定为以下位掩码的任意组合。

| 值  | 常量                                     | 描述                                                                                                                                                                                                              |
|-----|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | ICONV\_MIME\_DECODE\_STRICT              | 如果设置了，给定的头将会以 <a href="http://www.faqs.org/rfcs/rfc2047" class="link external">» RFC2047</a> 定义的标准完全一致。 这个选项默认禁用，因为大量有问题的邮件用户代理不遵循标准并产生不正确的 *MIME* 头。 |
| 2   | ICONV\_MIME\_DECODE\_CONTINUE\_ON\_ERROR | 如果设置了，<span class="function">iconv\_mime\_decode\_headers</span> 尝试忽略任何语法错误并继续处理指定的头。                                                                                                   |

`charset`  
可选参数 `charset` 指定了字符集结果的表现。 如果省略了，将使用
<a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a>。

### 返回值

成功时返回 `encoded_headers` 指定的 *MIME*
头的整套关联数组，解码时出现错误则返回 **`false`**。

返回元素的每个键代表独立字段名，相应的元素代表一个字段值。
如果有多个同一名称的字段， <span
class="function">iconv\_mime\_decode\_headers</span>
自动将他们按出现顺序结合成数字索引的数组。

### 范例

**示例 \#1 <span class="function">iconv\_mime\_decode\_headers</span>
例子**

``` php
<?php
$headers_string = <<<EOF
Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?=
To: example@example.com
Date: Thu, 1 Jan 1970 00:00:00 +0000
Message-Id: <example@example.com>
Received: from localhost (localhost [127.0.0.1]) by localhost
    with SMTP id example for <example@example.com>;
    Thu, 1 Jan 1970 00:00:00 +0000 (UTC)
    (envelope-from example-return-0000-example=example.com@example.com)
Received: (qmail 0 invoked by uid 65534); 1 Thu 2003 00:00:00 +0000

EOF;

$headers =  iconv_mime_decode_headers($headers_string, 0, "ISO-8859-1");
print_r($headers);
?>
```

以上例程会输出：

    Array
    (
        [Subject] => Prüfung Prüfung
        [To] => example@example.com
        [Date] => Thu, 1 Jan 1970 00:00:00 +0000
        [Message-Id] => <example@example.com>
        [Received] => Array
            (
                [0] => from localhost (localhost [127.0.0.1]) by localhost with SMTP id example for <example@example.com>; Thu, 1 Jan 1970 00:00:00 +0000 (UTC) (envelope-from example-return-0000-example=example.com@example.com)
                [1] => (qmail 0 invoked by uid 65534); 1 Thu 2003 00:00:00 +0000
            )

    )

### 参见

-   <span class="function">iconv\_mime\_decode</span>
-   <span class="function">mb\_decode\_mimeheader</span>
-   <span class="function">imap\_mime\_header\_decode</span>
-   <span class="function">imap\_base64</span>
-   <span class="function">imap\_qprint</span>

iconv\_mime\_decode
===================

解码一个*MIME*头字段

### 说明

<span class="type">string</span> <span
class="methodname">iconv\_mime\_decode</span> ( <span
class="methodparam"><span class="type">string</span>
`$encoded_header`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$charset`<span class="initializer"> =
ini\_get("iconv.internal\_encoding")</span></span> \]\] )

解码一个*MIME*头字段.

### 参数

`encoded_header`  
编码头,是一个字符串.

`mode`  
`模式`决定了当<span
class="function">iconv\_mime\_decode</span>遇到一个不规则的
*MIME*头字段时,对这个事件作出的行为.你可以指定以下位掩码的任意组合.

| 值  | 常量                                     | 描述                                                                                                                                                                                                                                      |
|-----|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | ICONV\_MIME\_DECODE\_STRICT              | 如果使用该位掩码,传入的头字段将会完全一致的按照<a href="http://www.faqs.org/rfcs/rfc2047" class="link external">» RFC2047</a>的标准定义被解码. 这个选项默认是禁用的,因为有很多零散的邮件用户代理商不遵守标准规范并且不生成正确的*MIME*头. |
| 2   | ICONV\_MIME\_DECODE\_CONTINUE\_ON\_ERROR | 如果使用该位掩码,<span class="function">iconv\_mime\_decode\_headers</span> 将会试图忽略任何错误语法,并继续处理传入的头字段.                                                                                                              |

`charset`  
可选的`字符集`参数,用指定的字符集表示结果.如果省略,
<a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a>
将会被默认使用.

### 返回值

如果解码成功,返回一个被解码的*MIME*字段,
如果在解码过程中出现一个错误,将返回**`false`** .

### 范例

**示例 \#1 <span class="function">iconv\_mime\_decode</span>实例**

``` php
<?php
//返回结果: "Subject: Prüfung Prüfung"
echo iconv_mime_decode("Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?=",
                       0, "ISO-8859-1");
?>
```

### 参见

-   <span class="function">iconv\_mime\_decode\_headers</span>
-   <span class="function">mb\_decode\_mimeheader</span>
-   <span class="function">imap\_mime\_header\_decode</span>
-   <span class="function">imap\_base64</span>
-   <span class="function">imap\_qprint</span>

iconv\_mime\_encode
===================

Composes a *MIME* header field

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">iconv\_mime\_encode</span> ( <span
class="methodparam"><span class="type">string</span>
`$field_name`</span> , <span class="methodparam"><span
class="type">string</span> `$field_value`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = \[\]</span></span> \] )

Composes and returns a string that represents a valid *MIME* header
field, which looks like the following:

    Subject: =?ISO-8859-1?Q?Pr=FCfung_f=FCr?= Entwerfen von einer MIME kopfzeile

In the above example, "Subject" is the field name and the portion that
begins with "=?ISO-8859-1?..." is the field value.

### 参数

`field_name`  
The field name.

`field_value`  
The field value.

`options`  
You can control the behaviour of <span
class="function">iconv\_mime\_encode</span> by specifying an associative
array that contains configuration items to the optional third parameter
`options`. The items supported by <span
class="function">iconv\_mime\_encode</span> are listed below. Note that
item names are treated case-sensitive.

| Item             | Type                             | Description                                                                                                                                                                                                                                                                                                                                                                          | Default value                                                                   | Example    |
|------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|------------|
| scheme           | <span class="type">string</span> | Specifies the method to encode a field value by. The value of this item may be either "B" or "Q", where "B" stands for *base64* encoding scheme and "Q" stands for *quoted-printable* encoding scheme.                                                                                                                                                                               | B                                                                               | B          |
| input-charset    | <span class="type">string</span> | Specifies the character set in which the first parameter `field_name` and the second parameter `field_value` are presented. If not given, <span class="function">iconv\_mime\_encode</span> assumes those parameters are presented to it in the <a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a> ini setting.                                         | <a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a> | ISO-8859-1 |
| output-charset   | <span class="type">string</span> | Specifies the character set to use to compose the *MIME* header.                                                                                                                                                                                                                                                                                                                     | <a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a> | UTF-8      |
| line-length      | <span class="type">int</span>    | Specifies the maximum length of the header lines. The resulting header is "folded" to a set of multiple lines in case the resulting header field would be longer than the value of this parameter, according to <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC2822 - Internet Message Format</a>. If not given, the length will be limited to 76 characters. | 76                                                                              | 996        |
| line-break-chars | <span class="type">string</span> | Specifies the sequence of characters to append to each line as an end-of-line sign when "folding" is performed on a long header field. If not given, this defaults to "\\r\\n" (*CR* *LF*). Note that this parameter is always treated as an ASCII string regardless of the value of *input-charset*.                                                                                | \\r\\n                                                                          | \\n        |

### 返回值

Returns an encoded *MIME* field on success, or **`false`** if an error
occurs during the encoding.

### 范例

**示例 \#1 <span class="function">iconv\_mime\_encode</span> example**

``` php
<?php
$preferences = array(
    "input-charset" => "ISO-8859-1",
    "output-charset" => "UTF-8",
    "line-length" => 76,
    "line-break-chars" => "\n"
);
$preferences["scheme"] = "Q";
// This yields "Subject: =?UTF-8?Q?Pr=C3=BCfung=20Pr=C3=BCfung?="
echo iconv_mime_encode("Subject", "Prüfung Prüfung", $preferences);

$preferences["scheme"] = "B";
// This yields "Subject: =?UTF-8?B?UHLDvGZ1bmcgUHLDvGZ1bmc=?="
echo iconv_mime_encode("Subject", "Prüfung Prüfung", $preferences);
?>
```

### 参见

-   <span class="function">imap\_binary</span>
-   <span class="function">mb\_encode\_mimeheader</span>
-   <span class="function">imap\_8bit</span>
-   <span class="function">quoted\_printable\_encode</span>

iconv\_set\_encoding
====================

为字符编码转换设定当前设置

### 说明

<span class="type">bool</span> <span
class="methodname">iconv\_set\_encoding</span> ( <span
class="methodparam"><span class="type">string</span> `$type`</span> ,
<span class="methodparam"><span class="type">string</span>
`$charset`</span> )

将 `type` 设置的值从内部配置变量更改为 `charset`。

### 参数

`type`  
`type` 的值可以是以下其中任意一个：

-   input\_encoding
-   output\_encoding
-   internal\_encoding

`charset`  
字符集。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">iconv\_set\_encoding</span> 例子**

``` php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
?>
```

### 参见

-   <span class="function">iconv\_get\_encoding</span>
-   <span class="function">ob\_iconv\_handler</span>

iconv\_strlen
=============

返回字符串的字符数统计

### 说明

<span class="type">int</span> <span
class="methodname">iconv\_strlen</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$charset`<span class="initializer"> =
ini\_get("iconv.internal\_encoding")</span></span> \] )

和 <span class="function">strlen</span> 不同的是，<span
class="function">iconv\_strlen</span> 统计了给定的字节序列 `str`
中出现字符数的统计，基于指定的字符集，其产生的结果不一定和字符字节数相等。

### 参数

`str`  
该字符串。

`charset`  
如果省略了 `charset` 参数，假设 `str` 的编码为
<a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a>。

### 返回值

返回 `str` 字符数的统计，是整型。

### 参见

-   <span class="function">grapheme\_strlen</span>
-   <span class="function">mb\_strlen</span>
-   <span class="function">strlen</span>

iconv\_strpos
=============

Finds position of first occurrence of a needle within a haystack

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">iconv\_strpos</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$encoding`<span class="initializer"> = **`null`**</span></span> \]\] )

Finds position of first occurrence of a `needle` within a `haystack`.

In contrast to <span class="function">strpos</span>, the return value of
<span class="function">iconv\_strpos</span> is the number of characters
that appear before the needle, rather than the offset in bytes to the
position where the needle has been found. The characters are counted on
the basis of the specified character set `encoding`.

### 参数

`haystack`  
The entire string.

`needle`  
The searched substring.

`offset`  
The optional `offset` parameter specifies the position from which the
search should be performed. If the offset is negative, it is counted
from the end of the string.

`encoding`  
If `encoding` parameter is omitted or **`null`**, `string` are assumed
to be encoded in
<a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a>.

If `haystack` or `needle` is not a string, it is converted to a string
and applied as the ordinal value of a character.

### 返回值

Returns the numeric position of the first occurrence of `needle` in
`haystack`.

If `needle` is not found, <span class="function">iconv\_strpos</span>
will return **`false`**.

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本  | 说明                                           |
|-------|------------------------------------------------|
| 8.0.0 | `encoding` is nullable now.                    |
| 7.1.0 | Support for negative `offset`s has been added. |

### 参见

-   <span class="function">strpos</span>
-   <span class="function">iconv\_strrpos</span>
-   <span class="function">mb\_strpos</span>

iconv\_strrpos
==============

Finds the last occurrence of a needle within a haystack

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">iconv\_strrpos</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">null</span></span>
`$encoding`<span class="initializer"> = **`null`**</span></span> \] )

Finds the last occurrence of a `needle` within a `haystack`.

In contrast to <span class="function">strrpos</span>, the return value
of <span class="function">iconv\_strrpos</span> is the number of
characters that appear before the needle, rather than the offset in
bytes to the position where the needle has been found. The characters
are counted on the basis of the specified character set `encoding`.

### 参数

`haystack`  
The entire string.

`needle`  
The searched substring.

`encoding`  
If `encoding` parameter is omitted or **`null`**, `string` are assumed
to be encoded in
<a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a>.

If `haystack` or `needle` is not a string, it is converted to a string
and applied as the ordinal value of a character.

### 返回值

Returns the numeric position of the last occurrence of `needle` in
`haystack`.

If `needle` is not found, <span class="function">iconv\_strrpos</span>
will return **`false`**.

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本  | 说明                        |
|-------|-----------------------------|
| 8.0.0 | `encoding` is nullable now. |

### 参见

-   <span class="function">strrpos</span>
-   <span class="function">iconv\_strpos</span>
-   <span class="function">mb\_strrpos</span>

iconv\_substr
=============

截取字符串的部分

### 说明

<span class="type">string</span> <span
class="methodname">iconv\_substr</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$length`<span class="initializer"> = iconv\_strlen($str,
$charset)</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$charset`<span class="initializer"> =
ini\_get("iconv.internal\_encoding")</span></span> \]\] )

根据 `offset` 和 `length` 参数指定 `str` 截取的部分。

### 参数

`str`  
原始字符串。

`offset`  
如果 `offset` 是非负数，<span class="function">iconv\_substr</span> 从
`str` 开头第 `offset` 个字符开始截出部分，从 0 开始计数。

如果 `offset` 是负数，<span class="function">iconv\_substr</span> 从
`str` 末尾向前 `offset` 个字符开始截取。

`length`  
如果指定了 `length` 并且是正数，返回的值从 `offset` 截取部分，最多包含
`length` 个字符（取决于 `string` 的长度）。

如果传入了负数的 `length`， <span class="function">iconv\_substr</span>
将从第 `offset` 个字符到离末尾 `length` 个字符截出 `str` 的部分。 如果
`offset` 也是负数，则开始位置计算规则的解释见以上。

`charset`  
如果省略了参数 `charset`，`string` 的编码被认定为
<a href="/iconv/setup.html#运行时配置" class="link">iconv.internal_encoding</a>。

注意，`offset` 和 `length` 参数总是被认为字符表现的偏移，基于 `charset`
检测到的字符集进行统计计算，而相对应的 <span
class="function">substr</span> 则是基于字节的位移来计算。

### 返回值

返回 `offset` 和 `length` 参数指定的 `str` 的部分。

如果 `str` 比 `offset` 字符数更短，将会返回 **`false`**。 如果 `str` 是
`offset` 个字符的长度，将返回空字符串。

### 更新日志

| 版本   | 说明                                                                                                |
|--------|-----------------------------------------------------------------------------------------------------|
| 7.0.11 | 如果 `str` 等长于 `offset` 个字符， 将返回空字符串。之前的版本里，这种情况是会返回 **`false`** 的。 |

### 参见

-   <span class="function">substr</span>
-   <span class="function">mb\_substr</span>
-   <span class="function">mb\_strcut</span>

iconv
=====

字符串按要求的字符编码来转换

### 说明

<span class="type">string</span> <span class="methodname">iconv</span> (
<span class="methodparam"><span class="type">string</span>
`$in_charset`</span> , <span class="methodparam"><span
class="type">string</span> `$out_charset`</span> , <span
class="methodparam"><span class="type">string</span> `$str`</span> )

将字符串 `str` 从 `in_charset` 转换编码到 `out_charset`。

### 参数

`in_charset`  
输入的字符集。

`out_charset`  
输出的字符集。

如果你在 `out_charset` 后添加了字符串
*//TRANSLIT*，将启用转写（transliteration）功能。这个意思是，当一个字符不能被目标字符集所表示时，它可以通过一个或多个形似的字符来近似表达。
如果你添加了字符串 *//IGNORE*，不能以目标字符集表达的字符将被默默丢弃。
否则，会导致一个 **`E_NOTICE`**并返回 **`false`**。

**Caution**
*//TRANSLIT* 运行细节高度依赖于系统的 iconv() 实现（参见
**`ICONV_IMPL`**）。 据悉，某些系统上的实现会直接忽略
*//TRANSLIT*，所以转换也有可能失败，`out_charset` 会是不合格的。

`str`  
要转换的字符串。

### 返回值

返回转换后的字符串， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 5.4.0 | 这个版本起，字符非法时候会返回 **`false`**，除非在输出字符里指定了 *//IGNORE* 。 在之前版本，它会返回一部分字符串。 |

### 范例

**示例 \#1 <span class="function">iconv</span> 例子**

``` php
<?php
$text = "This is the Euro symbol '€'.";

echo 'Original : ', $text, PHP_EOL;
echo 'TRANSLIT : ', iconv("UTF-8", "ISO-8859-1//TRANSLIT", $text), PHP_EOL;
echo 'IGNORE   : ', iconv("UTF-8", "ISO-8859-1//IGNORE", $text), PHP_EOL;
echo 'Plain    : ', iconv("UTF-8", "ISO-8859-1", $text), PHP_EOL;

?>
```

以上例程的输出类似于：

    Original : This is the Euro symbol '€'.
    TRANSLIT : This is the Euro symbol 'EUR'.
    IGNORE   : This is the Euro symbol ''.
    Plain    :
    Notice: iconv(): Detected an illegal character in input string in .\iconv-example.php on line 7

ob\_iconv\_handler
==================

以输出缓冲处理程序转换字符编码

### 说明

<span class="type">string</span> <span
class="methodname">ob\_iconv\_handler</span> ( <span
class="methodparam"><span class="type">string</span> `$contents`</span>
, <span class="methodparam"><span class="type">int</span>
`$status`</span> )

将字符编码从 `internal_encoding` 转换到 `output_encoding`。

`internal_encoding` 和 `output_encoding` 应当在 `php.ini` 文件或 <span
class="function">iconv\_set\_encoding</span> 中定义。

### 参数

关于处理程序参数的信息，参见 <span class="function">ob\_start</span>。

### 返回值

关于处理程序返回值的信息，参见 <span class="function">ob\_start</span>。

### 范例

**示例 \#1 <span class="function">ob\_iconv\_handler</span> 例子：**

``` php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
ob_start("ob_iconv_handler"); // 开始输出缓冲
?>
```

### 参见

-   <span class="function">iconv\_get\_encoding</span>
-   <span class="function">iconv\_set\_encoding</span>
-   <a href="/ref/outcontrol.html" class="link">输出控制函数</a>

**目录**

-   [iconv\_get\_encoding](/ref/iconv.html#iconv_get_encoding) — 获取
    iconv 扩展的内部配置变量
-   [iconv\_mime\_decode\_headers](/ref/iconv.html#iconv_mime_decode_headers)
    — 一次性解码多个 MIME 头字段
-   [iconv\_mime\_decode](/ref/iconv.html#iconv_mime_decode) —
    解码一个MIME头字段
-   [iconv\_mime\_encode](/ref/iconv.html#iconv_mime_encode) — Composes
    a MIME header field
-   [iconv\_set\_encoding](/ref/iconv.html#iconv_set_encoding) —
    为字符编码转换设定当前设置
-   [iconv\_strlen](/ref/iconv.html#iconv_strlen) —
    返回字符串的字符数统计
-   [iconv\_strpos](/ref/iconv.html#iconv_strpos) — Finds position of
    first occurrence of a needle within a haystack
-   [iconv\_strrpos](/ref/iconv.html#iconv_strrpos) — Finds the last
    occurrence of a needle within a haystack
-   [iconv\_substr](/ref/iconv.html#iconv_substr) — 截取字符串的部分
-   [iconv](/ref/iconv.html#iconv) — 字符串按要求的字符编码来转换
-   [ob\_iconv\_handler](/ref/iconv.html#ob_iconv_handler) —
    以输出缓冲处理程序转换字符编码
