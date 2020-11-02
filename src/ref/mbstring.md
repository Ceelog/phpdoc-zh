多字节字符编码方案和他们相关的问题相当复杂，超越了本文档的范围。
关于这些话题的更多信息请参考以下 URL 和其他资源。

-   Unicode materials

    <a href="http://www.unicode.org/" class="link external">» http://www.unicode.org/</a>

-   Japanese/Korean/Chinese 字符信息

    <a href="https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf" class="link external">» https://resources.oreilly.com/examples/9781565922242/blob/master/doc/cjk.inf</a>

mb\_check\_encoding
===================

检查字符串在指定的编码里是否有效

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_check\_encoding</span> (\[ <span
class="methodparam"><span class="type">string</span> `$var`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

检查指定的字节流在指定的编码里是否有效。它能有效避免所谓的“无效编码攻击（Invalid
Encoding Attack）”。

### 参数

`var`  
要检查的字节流。如果省略了这个参数，此函数会检查所有来自最初请求所有的输入。

`encoding`  
期望的编码。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

mb\_chr
=======

Get a specific character

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span class="methodname">mb\_chr</span>
( <span class="methodparam"><span class="type">int</span> `$cp`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`cp`  

`encoding`  

### 返回值

Returns a specific character 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">mb\_ord</span>
-   <span class="function">chr</span>

mb\_convert\_case
=================

对字符串进行大小写转换

### 说明

<span class="type">string</span> <span
class="methodname">mb\_convert\_case</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">int</span> `$mode`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \] )

对一个 <span class="type">string</span> 进行大小写转换，转换模式由
`mode` 指定。

### 参数

`str`  
要被转换的 <span class="type">string</span>。

`mode`  
转换的模式。它可以是 **`MB_CASE_UPPER`**、 **`MB_CASE_LOWER`** 和
**`MB_CASE_TITLE`** 的其中一个。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

按 `mode` 指定的模式转换 `string` 大小写后的版本。

### Unicode

和类似 <span class="function">strtolower</span>、<span
class="function">strtoupper</span> 的标准大小写转换函数相比，
大小写转换的执行根据 Unicode 字符属性的基础。
因此此函数的行为不受语言环境（locale）设置的影响，能够转换任意具有“字母”属性的字符，例如元音变音A（Ä）。

更多关于 Unicode 属性的信息，请查看
<a href="http://www.unicode.org/unicode/reports/tr21/" class="link external">» http://www.unicode.org/unicode/reports/tr21/</a>。

### 范例

**示例 \#1 <span class="function">mb\_convert\_case</span> 例子**

``` php
<?php
$str = "mary had a Little lamb and she loved it so";
$str = mb_convert_case($str, MB_CASE_UPPER, "UTF-8");
echo $str; // 输出 MARY HAD A LITTLE LAMB AND SHE LOVED IT SO
$str = mb_convert_case($str, MB_CASE_TITLE, "UTF-8");
echo $str; // 输出 Mary Had A Little Lamb And She Loved It So
?>
```

**示例 \#2 非拉丁 UTF-8 文本的<span
class="function">mb\_convert\_case</span> 例子**

``` php
<?php
$str = "Τάχιστη αλώπηξ βαφής ψημένη γη, δρασκελίζει υπέρ νωθρού κυνός";
$str = mb_convert_case($str, MB_CASE_UPPER, "UTF-8");
echo $str; // 输出 ΤΆΧΙΣΤΗ ΑΛΏΠΗΞ ΒΑΦΉΣ ΨΗΜΈΝΗ ΓΗ, ΔΡΑΣΚΕΛΊΖΕΙ ΥΠΈΡ ΝΩΘΡΟΎ ΚΥΝΌΣ
$str = mb_convert_case($str, MB_CASE_TITLE, "UTF-8");
echo $str; // 输出 Τάχιστη Αλώπηξ Βαφήσ Ψημένη Γη, Δρασκελίζει Υπέρ Νωθρού Κυνόσ
?>
```

### 参见

-   <span class="function">mb\_strtolower</span>
-   <span class="function">mb\_strtoupper</span>
-   <span class="function">strtolower</span>
-   <span class="function">strtoupper</span>
-   <span class="function">ucfirst</span>
-   <span class="function">ucwords</span>

mb\_convert\_encoding
=====================

转换字符的编码

### 说明

<span class="type">string</span> <span
class="methodname">mb\_convert\_encoding</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">string</span>
`$to_encoding`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$from_encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \] )

将 <span class="type">string</span> 类型 `str` 的字符编码从可选的
`from_encoding` 转换到 `to_encoding`。

### 参数

`str`  
要编码的 <span class="type">string</span>。

`to_encoding`  
`str` 要转换成的编码类型。

`from_encoding`  
在转换前通过字符代码名称来指定。它可以是一个 <span
class="type">array</span> 也可以是逗号分隔的枚举列表。 如果没有提供
`from_encoding`，则会使用内部（internal）编码。

参见<a href="/mbstring/supported-encodings.html" class="link">支持的编码</a>。

### 返回值

编码后的 <span class="type">string</span>。

### 范例

**示例 \#1 <span class="function">mb\_convert\_encoding</span> 例子**

``` php
<?php
/* 转换内部编码为 SJIS */
$str = mb_convert_encoding($str, "SJIS");

/* 将 EUC-JP 转换成 UTF-7 */
$str = mb_convert_encoding($str, "UTF-7", "EUC-JP");

/* 从 JIS, eucjp-win, sjis-win 中自动检测编码，并转换 str 到 UCS-2LE */
$str = mb_convert_encoding($str, "UCS-2LE", "JIS, eucjp-win, sjis-win");

/* "auto" 扩展成 "ASCII,JIS,UTF-8,EUC-JP,SJIS" */
$str = mb_convert_encoding($str, "EUC-JP", "auto");
?>
```

### 参见

-   <span class="function">mb\_detect\_order</span>

mb\_convert\_kana
=================

Convert "kana" one from another ("zen-kaku", "han-kaku" and more)

### 说明

<span class="type">string</span> <span
class="methodname">mb\_convert\_kana</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$option`<span class="initializer"> = "KV"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

Performs a "han-kaku" - "zen-kaku" conversion for <span
class="type">string</span> `str`. This function is only useful for
Japanese.

### 参数

`str`  
The <span class="type">string</span> being converted.

`option`  
The conversion option.

Specify with a combination of following options.

| Option | Meaning                                                                                                                                                       |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *r*    | Convert "zen-kaku" alphabets to "han-kaku"                                                                                                                    |
| *R*    | Convert "han-kaku" alphabets to "zen-kaku"                                                                                                                    |
| *n*    | Convert "zen-kaku" numbers to "han-kaku"                                                                                                                      |
| *N*    | Convert "han-kaku" numbers to "zen-kaku"                                                                                                                      |
| *a*    | Convert "zen-kaku" alphabets and numbers to "han-kaku"                                                                                                        |
| *A*    | Convert "han-kaku" alphabets and numbers to "zen-kaku" (Characters included in "a", "A" options are U+0021 - U+007E excluding U+0022, U+0027, U+005C, U+007E) |
| *s*    | Convert "zen-kaku" space to "han-kaku" (U+3000 -\> U+0020)                                                                                                    |
| *S*    | Convert "han-kaku" space to "zen-kaku" (U+0020 -\> U+3000)                                                                                                    |
| *k*    | Convert "zen-kaku kata-kana" to "han-kaku kata-kana"                                                                                                          |
| *K*    | Convert "han-kaku kata-kana" to "zen-kaku kata-kana"                                                                                                          |
| *h*    | Convert "zen-kaku hira-gana" to "han-kaku kata-kana"                                                                                                          |
| *H*    | Convert "han-kaku kata-kana" to "zen-kaku hira-gana"                                                                                                          |
| *c*    | Convert "zen-kaku kata-kana" to "zen-kaku hira-gana"                                                                                                          |
| *C*    | Convert "zen-kaku hira-gana" to "zen-kaku kata-kana"                                                                                                          |
| *V*    | Collapse voiced sound notation and convert them into a character. Use with "K","H"                                                                            |

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

The converted <span class="type">string</span>.

### 范例

**示例 \#1 <span class="function">mb\_convert\_kana</span> example**

``` php
<?php
/* Convert all "kana" to "zen-kaku" "kata-kana" */
$str = mb_convert_kana($str, "KVC");

/* Convert "han-kaku" "kata-kana" to "zen-kaku" "kata-kana" 
   and "zen-kaku" alphanumeric to "han-kaku" */
$str = mb_convert_kana($str, "KVa");
?>
```

mb\_convert\_variables
======================

转换一个或多个变量的字符编码

### 说明

<span class="type">string</span> <span
class="methodname">mb\_convert\_variables</span> ( <span
class="methodparam"><span class="type">string</span>
`$to_encoding`</span> , <span class="methodparam"><span
class="type">mixed</span> `$from_encoding`</span> , <span
class="methodparam"><span class="type">mixed</span> `&$vars`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `&$...`</span>
\] )

将变量 `vars` 的编码从 `from_encoding` 转换成编码 `to_encoding`。

<span class="function">mb\_convert\_variables</span>
会拼接变量数组或对象中的字符串来检测编码，因为短字符串的检测往往会失败。因此，不能在一个数组或对象中混合使用编码。

### 参数

`to_encoding`  
将 <span class="type">string</span> 转换成这个编码。

`from_encoding`  
`from_encoding` 可以指定为一个 <span class="type">array</span>
或者逗号分隔的 <span class="type">string</span>，它将尝试根据
`from-coding` 来检测编码。 当省略了 `from_encoding`，将使用
*detect\_order*。

`vars`  
`vars` 是要转换的变量的引用。 参数可以接受 String、Array 和 Object
的类型。 <span class="function">mb\_convert\_variables</span>
假设所有的参数都具有同样的编码。

`...`  
额外的 `vars`。

### 返回值

成功时返回转换前的字符编码，失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mb\_convert\_variables</span> 例子**

``` php
<?php
/* 转换变量 $post1、$post2 编码为内部（internal）编码 */
$interenc = mb_internal_encoding();
$inputenc = mb_convert_variables($interenc, "ASCII,UTF-8,SJIS-win", $post1, $post2);
?>
```

mb\_decode\_mimeheader
======================

解码 MIME 头字段中的字符串

### 说明

<span class="type">string</span> <span
class="methodname">mb\_decode\_mimeheader</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> )

解码 MIME 头中编码过的<span class="type">字符串</span> `str`。

### 参数

`str`  
要解码的 <span class="type">string</span>。

### 返回值

以内部（internal）字符编码解码的 <span class="type">string</span>。

### 参见

-   <span class="function">mb\_encode\_mimeheader</span>

mb\_decode\_numericentity
=========================

根据 HTML 数字字符串解码成字符

### 说明

<span class="type">string</span> <span
class="methodname">mb\_decode\_numericentity</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">array</span>
`$convmap`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \] )

将数字<span class="type">字符串</span>的引用`str`
按指定的字符块转换成字符串。

### 参数

`str`  
要解码的 <span class="type">string</span>。

`convmap`  
`convmap` 是一个 <span
class="type">array</span>，指定了要转换的代码区域。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

转换后的<span class="type">字符串</span>。

### 范例

**示例 \#1 `convmap` 例子**

``` php
<?php
$convmap = array (
   int start_code1, int end_code1, int offset1, int mask1,
   int start_code2, int end_code2, int offset2, int mask2,
   ........
   int start_codeN, int end_codeN, int offsetN, int maskN );
// Specify Unicode value for start_codeN and end_codeN
// Add offsetN to value and take bit-wise 'AND' with maskN, 
// then convert value to numeric string reference.
?>
```

### 参见

-   <span class="function">mb\_encode\_numericentity</span>

**示例 \#2 `convmap` 的例子： 编码(escape) JavaScript 字符串**

``` php
<?php
function escape_javascript_string($str) {
  $map = [
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,0,0, // 49
          0,0,0,0,0,0,0,0,1,1,
          1,1,1,1,1,0,0,0,0,0,
          0,0,0,0,0,0,0,0,0,0,
          0,0,0,0,0,0,0,0,0,0,
          0,1,1,1,1,1,1,0,0,0, // 99
          0,0,0,0,0,0,0,0,0,0,
          0,0,0,0,0,0,0,0,0,0,
          0,0,0,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1, // 149
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1, // 199
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1,
          1,1,1,1,1,1,1,1,1,1, // 249
          1,1,1,1,1,1,1, // 255
          ];
  // Char encoding is UTF-8
  $mblen = mb_strlen($str, 'UTF-8');
  $utf32 = bin2hex(mb_convert_encoding($str, 'UTF-32', 'UTF-8'));
  for ($i=0, $encoded=''; $i < $mblen; $i++) {
      $u = substr($utf32, $i*8, 8);
      $v = base_convert($u, 16, 10);
      if ($v < 256 && $map[$v]) {
        $encoded .= '\\x'.substr($u, 6,2);
      } else if ($v == 2028) {
        $encoded .= '\\u2028';
      } else if ($v == 2029) {
        $encoded .= '\\u2029';
      } else {
        $encoded .= mb_convert_encoding(hex2bin($u), 'UTF-8', 'UTF-32');
      }
   }
   return $encoded;
}
 
// Test data
$convmap = [ 0x0, 0xffff, 0, 0xffff ];
$msg = '';
for ($i=0; $i < 1000; $i++) {
  // chr() cannot generate correct UTF-8 data larger value than 128, use mb_decode_numericentity().
  $msg .= mb_decode_numericentity('&#'.$i.';', $convmap, 'UTF-8');
}
 
// var_dump($msg);
var_dump(escape_javascript_string($msg));
```

mb\_detect\_encoding
====================

检测字符的编码

### 说明

<span class="type">string</span> <span
class="methodname">mb\_detect\_encoding</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$encoding_list`<span class="initializer"> =
mb\_detect\_order()</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`<span class="initializer"> =
false</span></span> \]\] )

检测<span class="type">字符串</span> `str` 的编码。

### 参数

`str`  
待检查的<span class="type">字符串</span>。

`encoding_list`  
`encoding_list` 是一个字符编码列表。
编码顺序可以由数组或者逗号分隔的列表字符串指定。

如果省略了 `encoding_list` 将会使用 detect\_order。

`strict`  
`strict` 指定了是否严格地检测编码。 默认是 **`FALSE`**。

### 返回值

检测到的字符编码，或者无法检测指定字符串的编码时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mb\_detect\_encoding</span> 例子**

``` php
<?php
/* 使用当前的 detect_order 来检测字符编码 */
echo mb_detect_encoding($str);

/* "auto" 将根据 mbstring.language 来扩展 */
echo mb_detect_encoding($str, "auto");

/* 通过逗号分隔的列表来指定编码列表 encoding_list */
echo mb_detect_encoding($str, "JIS, eucjp-win, sjis-win");

/* 使用数组来指定编码列表 encoding_list  */
$ary[] = "ASCII";
$ary[] = "JIS";
$ary[] = "EUC-JP";
echo mb_detect_encoding($str, $ary);
?>
```

### 参见

-   <span class="function">mb\_detect\_order</span>

mb\_detect\_order
=================

设置/获取 字符编码的检测顺序

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_detect\_order</span> (\[ <span
class="methodparam"><span class="type">mixed</span>
`$encoding_list`<span class="initializer"> =
mb\_detect\_order()</span></span> \] )

为编码列表 `encoding_list` 设置自动检测字符编码的顺序。

### 参数

`encoding_list`  
`encoding_list` 是一个 <span class="type">array</span>
或者逗号分隔的字符编码列表。
参见<a href="/mbstring/supported-encodings.html" class="link">支持的编码</a>。

如果省略了 `encoding_list` 参数，它将返回当前字符编码检测顺序的数组。

该设置会影响 <span class="function">mb\_detect\_encoding</span> 和 <span
class="function">mb\_send\_mail</span>。

*mbstring* 当前实现了以下编码检测筛选器。
如有以下编码列表的无效字节序列，编码的检测将会失败。

<span class="simpara"> *UTF-8*, *UTF-7*, *ASCII*, *EUC-JP*,*SJIS*,
*eucJP-win*, *SJIS-win*, *JIS*, *ISO-2022-JP* </span>

对于 *ISO-8859-\**，*mbstring* 总是检测为 *ISO-8859-\**。

对于 *UTF-16*、*UTF-32*、 *UCS2* 和 *UCS4*，编码检测总是会失败。

### 返回值

设置编码检测顺序时候，成功时返回 **`TRUE`**，识别时候返回 **`FALSE`**。

在获取编码检测顺序的时候，会返回排序过的编码数组。

### 范例

**示例 \#1 <span class="function">mb\_detect\_order</span> 例子**

``` php
<?php
/* 为检测顺序设置枚举列表 */
mb_detect_order("eucjp-win,sjis-win,UTF-8");

/* 通过数组设置检测顺序 */
$ary[] = "ASCII";
$ary[] = "JIS";
$ary[] = "EUC-JP";
mb_detect_order($ary);

/* 显示当前的检测顺序 */
echo implode(", ", mb_detect_order());
?>
```

**示例 \#2 案例展示了无效的检测顺序**

    ; 总是检测为 ISO-8859-1
    detect_order = ISO-8859-1, UTF-8

    ; 总是检测为 UTF-8，由于 ASCII/UTF-7 的值对  UTF-8 是有效的
    detect_order = UTF-8, ASCII, UTF-7

### 参见

-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">mb\_http\_input</span>
-   <span class="function">mb\_http\_output</span>
-   <span class="function">mb\_send\_mail</span>

mb\_encode\_mimeheader
======================

为 MIME 头编码字符串

### 说明

<span class="type">string</span> <span
class="methodname">mb\_encode\_mimeheader</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$charset`<span class="initializer"> = determined by
mb\_language()</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$transfer_encoding`<span
class="initializer"> = "B"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$linefeed`<span
class="initializer"> = "\\r\\n"</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$indent`<span
class="initializer"> = 0</span></span> \]\]\]\] )

按 MIME 头编码方案将指定的<span class="type">字符串</span> `str`
进行编码。

### 参数

`str`  
要编码的 <span class="type">string</span>。 它的编码应该和 <span
class="function">mb\_internal\_encoding</span> 一样。

`charset`  
`charset` 指定了 `str` 的字符集名。 其默认值由当前的 NLS
设置（*mbstring.language*）来确定。

`transfer_encoding`  
`transfer_encoding` 指定了 MIME 的编码方案。 它可以是
*"B"*（Base64）也可以是 *"Q"*（Quoted-Printable）。 如果未设置，将回退为
*"B"*。

`linefeed`  
`linefeed` 指定了 EOL（行尾）标记，使 <span
class="function">mb\_encode\_mimeheader</span>
执行了一个换行（<a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC</a>
文档中规定，超过长度的一行将换成多行，当前该长度硬式编码为 74 个字符）。
如果没有设定，则回退为 *"\\r\\n"* (CRLF)。

`indent`  
首行缩进（header 里 `str` 前的字符数目）。

### 返回值

转换后的<span class="type">字符串</span>版本以 ASCII 形式表达。

### 范例

**示例 \#1 <span class="function">mb\_encode\_mimeheader</span> 例子**

``` php
<?php
$name = ""; // kanji
$mbox = "kru";
$doma = "gtinn.mon";
$addr = mb_encode_mimeheader($name, "UTF-7", "Q") . " <" . $mbox . "@" . $doma . ">";
echo $addr;
?>
```

### 注释

> **Note**:
>
> 这个函数没有设计成据更高级上下文的中断点来换行（单词边界等）。
> 这个特性将导致意外的空格可能会让原始字符串看上去很乱。

### 参见

-   <span class="function">mb\_decode\_mimeheader</span>

mb\_encode\_numericentity
=========================

Encode character to HTML numeric string reference

### 说明

<span class="type">string</span> <span
class="methodname">mb\_encode\_numericentity</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">array</span>
`$convmap`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_hex`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

Converts specified character codes in <span class="type">string</span>
`str` from character code to HTML numeric character reference.

### 参数

`str`  
The <span class="type">string</span> being encoded.

`convmap`  
`convmap` is array specifies code area to convert.

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

`is_hex`  
Whether the returned entity reference should be in hexadecimal notation
(otherwise it is in decimal notation).

### 返回值

The converted <span class="type">string</span>.

### 范例

**示例 \#1 `convmap` example**

``` php
<?php
$convmap = array (
 int start_code1, int end_code1, int offset1, int mask1,
 int start_code2, int end_code2, int offset2, int mask2,
 ........
 int start_codeN, int end_codeN, int offsetN, int maskN );
// Specify Unicode value for start_codeN and end_codeN
// Add offsetN to value and take bit-wise 'AND' with maskN, then
// it converts value to numeric string reference.
?>
```

### 范例

**示例 \#2 <span class="function">mb\_encode\_numericentity</span>
example**

``` php
<?php
/* Convert Left side of ISO-8859-1 to HTML numeric character reference */
$convmap = array(0x80, 0xff, 0, 0xff);
$str = mb_encode_numericentity($str, $convmap, "ISO-8859-1");

/* Convert user defined SJIS-win code in block 95-104 to numeric
   string reference */
$convmap = array(
       0xe000, 0xe03e, 0x1040, 0xffff,
       0xe03f, 0xe0bb, 0x1041, 0xffff,
       0xe0bc, 0xe0fa, 0x1084, 0xffff,
       0xe0fb, 0xe177, 0x1085, 0xffff,
       0xe178, 0xe1b6, 0x10c8, 0xffff,
       0xe1b7, 0xe233, 0x10c9, 0xffff,
       0xe234, 0xe272, 0x110c, 0xffff,
       0xe273, 0xe2ef, 0x110d, 0xffff,
       0xe2f0, 0xe32e, 0x1150, 0xffff,
       0xe32f, 0xe3ab, 0x1151, 0xffff );
$str = mb_encode_numericentity($str, $convmap, "sjis-win");
?>
```

### 参见

-   <span class="function">mb\_decode\_numericentity</span>

mb\_encoding\_aliases
=====================

Get aliases of a known encoding type

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">mb\_encoding\_aliases</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

Returns an array of aliases for a known `encoding` type.

### 参数

`encoding`  
The encoding type being checked, for aliases.

### 返回值

Returns a numerically indexed array of encoding aliases on success,
或者在失败时返回 **`FALSE`**

### 错误／异常

Emits an **`E_WARNING`** level error if `encoding` is unknown.

### 范例

**示例 \#1 <span class="function">mb\_encoding\_aliases</span> example**

``` php
<?php
$encoding        = 'ASCII';
$known_encodings = mb_list_encodings();

if (in_array($encoding, $known_encodings)) {

    $aliases = mb_encoding_aliases($encoding);
    print_r($aliases);

} else {

    echo "Unknown ($encoding) encoding.\n";

}
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => ANSI_X3.4-1968
        [1] => iso-ir-6
        [2] => ANSI_X3.4-1986
        [3] => ISO_646.irv:1991
        [4] => US-ASCII
        [5] => ISO646-US
        [6] => us
        [7] => IBM367
        [8] => cp367
        [9] => csASCII
    )

### 参见

-   <span class="function">mb\_list\_encodings</span>

mb\_ereg\_match
===============

Regular expression match for multibyte string

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_ereg\_match</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$string`</span> \[, <span class="methodparam"><span
class="type">string</span> `$option`<span class="initializer"> =
"msr"</span></span> \] )

A regular expression match for a multibyte string

### 参数

`pattern`  
The regular expression pattern.

`string`  
The <span class="type">string</span> being evaluated.

`option`  
The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation.

### 返回值

Returns **`TRUE`** if `string` matches the regular expression `pattern`,
**`FALSE`** if not.

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg</span>

mb\_ereg\_replace\_callback
===========================

Perform a regular expression search and replace with multibyte support
using a callback

### 说明

<span class="type">string</span> <span
class="methodname">mb\_ereg\_replace\_callback</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">string</span> `$option`<span
class="initializer"> = "msr"</span></span> \] )

Scans `string` for matches to `pattern`, then replaces the matched text
with the output of `callback` function.

The behavior of this function is almost identical to <span
class="function">mb\_ereg\_replace</span>, except for the fact that
instead of `replacement` parameter, one should specify a `callback`.

### 参数

`pattern`  
The regular expression pattern.

Multibyte characters may be used in `pattern`.

`callback`  
A callback that will be called and passed an array of matched elements
in the `subject` string. The callback should return the replacement
string.

You'll often need the `callback` function for a <span
class="function">mb\_ereg\_replace\_callback</span> in just one place.
In this case you can use an
<a href="/functions/anonymous.html" class="link">anonymous function</a>
to declare the callback within the call to <span
class="function">mb\_ereg\_replace\_callback</span>. By doing it this
way you have all information for the call in one place and do not
clutter the function namespace with a callback function's name not used
anywhere else.

`string`  
The <span class="type">string</span> being checked.

`option`  
The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation.

### 返回值

The resultant <span class="type">string</span> on success, or
**`FALSE`** on error.

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 范例

**示例 \#1 <span class="function">mb\_ereg\_replace\_callback</span>
example**

``` php
<?php
// this text was used in 2002
// we want to get this up to date for 2003
$text = "April fools day is 04/01/2002\n";
$text.= "Last christmas was 12/24/2001\n";
// the callback function
function next_year($matches)
{
  // as usual: $matches[0] is the complete match
  // $matches[1] the match for the first subpattern
  // enclosed in '(...)' and so on
  return $matches[1].($matches[2]+1);
}
echo mb_ereg_replace_callback(
            "(\d{2}/\d{2}/)(\d{4})",
            "next_year",
            $text);

?>
```

以上例程会输出：

    April fools day is 04/01/2003
    Last christmas was 12/24/2002

**示例 \#2 <span class="function">mb\_ereg\_replace\_callback</span>
using anonymous function supported in PHP 5.3.0 or later**

``` php
<?php
// this text was used in 2002
// we want to get this up to date for 2003
$text = "April fools day is 04/01/2002\n";
$text.= "Last christmas was 12/24/2001\n";

echo mb_ereg_replace_callback(
            "(\d{2}/\d{2}/)(\d{4})",
            function ($matches) {
               return $matches[1].($matches[2]+1);
            },
            $text);
?>
```

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_replace</span>
-   <a href="/functions/anonymous.html" class="link">Anonymous functions</a>

mb\_ereg\_replace
=================

Replace regular expression with multibyte support

### 说明

<span class="type">string</span> <span
class="methodname">mb\_ereg\_replace</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$replacement`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">string</span> `$option`<span
class="initializer"> = "msr"</span></span> \] )

Scans `string` for matches to `pattern`, then replaces the matched text
with `replacement`

### 参数

`pattern`  
The regular expression pattern.

Multibyte characters may be used in `pattern`.

`replacement`  
The replacement text.

`string`  
The <span class="type">string</span> being checked.

`option`  
<span class="simpara"> The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation. </span>

### 返回值

The resultant <span class="type">string</span> on success, or
**`FALSE`** on error.

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.1.0 | The *e* modifier has been deprecated. |

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

**Warning**

处理非信任的输入时从不使用 *e* 修饰符，就不会转码（即调用 <span
class="function">preg\_replace</span>）。不注意这些会很可能会导致应用程序引发远程代码执行的漏洞。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_eregi\_replace</span>

mb\_ereg\_search\_getpos
========================

Returns start point for next regular expression match

### 说明

<span class="type">int</span> <span
class="methodname">mb\_ereg\_search\_getpos</span> ( <span
class="methodparam">void</span> )

Returns the start point for the next regular expression match.

### 参数

此函数没有参数。

### 返回值

<span class="function">mb\_ereg\_search\_getpos</span> returns the point
to start regular expression match for <span
class="function">mb\_ereg\_search</span>, <span
class="function">mb\_ereg\_search\_pos</span>, <span
class="function">mb\_ereg\_search\_regs</span>. The position is
represented by bytes from the head of string.

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_setpos</span>

mb\_ereg\_search\_getregs
=========================

Retrieve the result from the last multibyte regular expression match

### 说明

<span class="type">array</span> <span
class="methodname">mb\_ereg\_search\_getregs</span> ( <span
class="methodparam">void</span> )

Retrieve the result from the last multibyte regular expression match

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> including the sub-string of matched
part by last <span class="function">mb\_ereg\_search</span>, <span
class="function">mb\_ereg\_search\_pos</span>, <span
class="function">mb\_ereg\_search\_regs</span>. If there are some
matches, the first element will have the matched sub-string, the second
element will have the first part grouped with brackets, the third
element will have the second part grouped with brackets, and so on. It
returns **`FALSE`** on error;

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_init</span>

mb\_ereg\_search\_init
======================

Setup string and regular expression for a multibyte regular expression
match

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_ereg\_search\_init</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pattern`</span> \[, <span class="methodparam"><span
class="type">string</span> `$option`<span class="initializer"> =
"msr"</span></span> \]\] )

<span class="function">mb\_ereg\_search\_init</span> sets `string` and
`pattern` for a multibyte regular expression. These values are used for
<span class="function">mb\_ereg\_search</span>, <span
class="function">mb\_ereg\_search\_pos</span>, and <span
class="function">mb\_ereg\_search\_regs</span>.

### 参数

`string`  
The search string.

`pattern`  
The search pattern.

`option`  
The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_regs</span>

mb\_ereg\_search\_pos
=====================

Returns position and length of a matched part of the multibyte regular
expression for a predefined multibyte string

### 说明

<span class="type">array</span> <span
class="methodname">mb\_ereg\_search\_pos</span> (\[ <span
class="methodparam"><span class="type">string</span> `$pattern`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$option`<span class="initializer"> = "ms"</span></span> \]\] )

Returns position and length of a matched part of the multibyte regular
expression for a predefined multibyte string

The string for match is specified by <span
class="function">mb\_ereg\_search\_init</span>. If it is not specified,
the previous one will be used.

### 参数

`pattern`  
The search pattern.

`option`  
The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation.

### 返回值

An <span class="type">array</span> containing two elements. The first
element is the offset, in bytes, where the match begins relative to the
start of the search string, and the second element is the length in
bytes of the match.

If an error occurs, **`FALSE`** is returned.

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_init</span>

mb\_ereg\_search\_regs
======================

Returns the matched part of a multibyte regular expression

### 说明

<span class="type">array</span> <span
class="methodname">mb\_ereg\_search\_regs</span> (\[ <span
class="methodparam"><span class="type">string</span> `$pattern`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$option`<span class="initializer"> = "ms"</span></span> \]\] )

Returns the matched part of a multibyte regular expression.

### 参数

`pattern`  
The search pattern.

`option`  
The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation.

### 返回值

<span class="function">mb\_ereg\_search\_regs</span> executes the
multibyte regular expression match, and if there are some matched part,
it returns an <span class="type">array</span> including substring of
matched part as first element, the first grouped part with brackets as
second element, the second grouped part as third element, and so on. It
returns **`FALSE`** on error.

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_init</span>

mb\_ereg\_search\_setpos
========================

Set start point of next regular expression match

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_ereg\_search\_setpos</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

<span class="function">mb\_ereg\_search\_setpos</span> sets the starting
point of a match for <span class="function">mb\_ereg\_search</span>.

### 参数

`position`  
The position to set. If it is negative, it counts from the end of the
string.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                             |
|-------|--------------------------------------------------|
| 7.1.0 | Support for negative `position`s has been added. |

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_init</span>

mb\_ereg\_search
================

Multibyte regular expression match for predefined multibyte string

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_ereg\_search</span> (\[ <span
class="methodparam"><span class="type">string</span> `$pattern`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$option`<span class="initializer"> = "ms"</span></span> \]\] )

Performs a multibyte regular expression match for a predefined multibyte
string.

### 参数

`pattern`  
The search pattern.

`option`  
The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation.

### 返回值

<span class="function">mb\_ereg\_search</span> returns **`TRUE`** if the
multibyte string matches with the regular expression, or **`FALSE`**
otherwise. The <span class="type">string</span> for matching is set by
<span class="function">mb\_ereg\_search\_init</span>. If `pattern` is
not specified, the previous one is used.

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_search\_init</span>

mb\_ereg
========

Regular expression match with multibyte support

### 说明

<span class="type">int</span> <span class="methodname">mb\_ereg</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$regs`</span> \] )

Executes the regular expression match with multibyte support.

### 参数

`pattern`  
The search pattern.

`string`  
The search <span class="type">string</span>.

`regs`  
If matches are found for parenthesized substrings of `pattern` and the
function is called with the third argument `regs`, the matches will be
stored in the elements of the array `regs`. If no matches are found,
`regs` is set to an empty array.

`$regs[1]` will contain the substring which starts at the first left
parenthesis; `$regs[2]` will contain the substring starting at the
second, and so on. `$regs[0]` will contain a copy of the complete string
matched.

### 返回值

Returns the byte length of the matched string if a match for `pattern`
was found in `string`, or **`FALSE`** if no matches were found or an
error occurred.

If the optional parameter `regs` was not passed or the length of the
matched string is *0*, this function returns *1*.

### 更新日志

| 版本  | 说明                                                                                                                                                                        |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | <span class="function">mb\_ereg</span> will now set `regs` to an empty <span class="type">array</span>, if nothing matched. Formerly, `regs` was not modified in that case. |

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_eregi</span>

mb\_eregi\_replace
==================

Replace regular expression with multibyte support ignoring case

### 说明

<span class="type">string</span> <span
class="methodname">mb\_eregi\_replace</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$replace`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">string</span> `$option`<span
class="initializer"> = "msri"</span></span> \] )

Scans `string` for matches to `pattern`, then replaces the matched text
with `replacement`.

### 参数

`pattern`  
The regular expression pattern. Multibyte characters may be used. The
case will be ignored.

`replace`  
The replacement text.

`string`  
The searched <span class="type">string</span>.

`option`  
<span class="simpara"> The search option. See <span
class="function">mb\_regex\_set\_options</span> for explanation. </span>

### 返回值

The resultant <span class="type">string</span> or **`FALSE`** on error.

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.1.0 | The *e* modifier has been deprecated. |

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

**Warning**

处理非信任的输入时从不使用 *e* 修饰符，就不会转码（即调用 <span
class="function">preg\_replace</span>）。不注意这些会很可能会导致应用程序引发远程代码执行的漏洞。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg\_replace</span>

mb\_eregi
=========

Regular expression match ignoring case with multibyte support

### 说明

<span class="type">int</span> <span class="methodname">mb\_eregi</span>
( <span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$regs`</span> \] )

Executes the case insensitive regular expression match with multibyte
support.

### 参数

`pattern`  
The regular expression pattern.

`string`  
The <span class="type">string</span> being searched.

`regs`  
If matches are found for parenthesized substrings of `pattern` and the
function is called with the third argument `regs`, the matches will be
stored in the elements of the array `regs`. If no matches are found,
`regs` is set to an empty array.

`$regs[1]` will contain the substring which starts at the first left
parenthesis; `$regs[2]` will contain the substring starting at the
second, and so on. `$regs[0]` will contain a copy of the complete string
matched.

### 返回值

Returns the byte length of the matched string if a match for `pattern`
was found in `string`, or **`FALSE`** if no matches were found or an
error occurred.

If the optional parameter `regs` was not passed or the length of the
matched string is *0*, this function returns *1*.

### 更新日志

| 版本  | 说明                                                                                                                                                                         |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | <span class="function">mb\_eregi</span> will now set `regs` to an empty <span class="type">array</span>, if nothing matched. Formerly, `regs` was not modified in that case. |

### 注释

> **Note**:
>
> <span class="function">mb\_regex\_encoding</span>
> 指定的内部编码或字符编码将会当作此函数用的字符编码。

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg</span>

mb\_get\_info
=============

获取 mbstring 的内部设置

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_get\_info</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`<span
class="initializer"> = "all"</span></span> \] )

<span class="function">mb\_get\_info</span> 返回 mbstring
参数的内部设定。

### 参数

`type`  
如果没有设定 `type`，或者将其设定为 "all"，将会返回一个 <span
class="type">array</span>，并且包含了以下所有元素："internal\_encoding",
"http\_output", "http\_input", "func\_overload", "mail\_charset",
"mail\_header\_encoding", "mail\_body\_encoding"。

如果 `type` 设定为类似 "http\_output", "http\_input",
"internal\_encoding", "func\_overload"，将返回该参数的设置。

### 返回值

如果没有指定 `type` 将返回类型信息的数组，否则将返回指定 `type` 的信息。

### 更新日志

| 版本  | 说明                                                                                |
|-------|-------------------------------------------------------------------------------------|
| 5.1.3 | 实体 "mail\_charset"、"mail\_header\_encoding" 和 "mail\_body\_encoding" 开始有效。 |
| 5.3.0 | 条目 "http\_output\_conv\_mimetypes" 开始有效。                                     |

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_http\_output</span>

mb\_http\_input
===============

检测 HTTP 输入字符编码

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_http\_input</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`<span
class="initializer"> = ""</span></span> \] )

检测 HTTP 输入字符的编码。

### 参数

`type`  
设置的字符串指定了输入类型。 "G" 是 GET，"P" 是 POST，"C" 是 COOKIE，"S"
是 string，"L" 是 list，以及 "I" 是整个列表（将会返回 <span
class="type">array</span>）。 如果省略了
type，它将返回最后处理的一种输入类型。

### 返回值

每个 `type` 的字符编码名称。 如果 <span
class="function">mb\_http\_input</span> 没有处理过任何指定的 HTTP
输入，它将返回 **`FALSE`**。

### 参见

-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">mb\_http\_output</span>
-   <span class="function">mb\_detect\_order</span>

mb\_http\_output
================

设置/获取 HTTP 输出字符编码

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_http\_output</span> (\[ <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_http\_output()</span></span> \] )

设置/获取 HTTP 输出字符编码。此函数被调用之后输出的内容会被转换成
`encoding`。

### 参数

`encoding`  
如果设置了 `encoding`，<span class="function">mb\_http\_output</span>
设置 HTTP 输出字符编码为 `encoding`。

如果省略了 `encoding`，<span class="function">mb\_http\_output</span>
返回当前的 HTTP 输出字符编码。

### 返回值

如果省略了 `encoding`，<span class="function">mb\_http\_output</span>
返回当前的 HTTP 输出字符编码。 否则成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">mb\_http\_input</span>
-   <span class="function">mb\_detect\_order</span>

mb\_internal\_encoding
======================

设置/获取内部字符编码

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_internal\_encoding</span> (\[ <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \] )

设置/获取内部字符编码

### 参数

`encoding`  
`encoding` 字符编码名称使用于 HTTP 输入字符编码转换、HTTP
输出字符编码转换、mbstring 模块系列函数字符编码转换的默认编码。 You
should notice that the internal encoding is totally different from the
one for multibyte regex.

### 返回值

如果设置了 `encoding`，则成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。 In this case, the character encoding for multibyte regex
is NOT changed. 如果省略了 `encoding`，则返回当前的字符编码名称。

### 范例

**示例 \#1 <span class="function">mb\_internal\_encoding</span> 例子**

``` php
<?php
/* 设置内部字符编码为 UTF-8 */
mb_internal_encoding("UTF-8");

/* 显示当前的内部字符编码*/
echo mb_internal_encoding();
?>
```

### 参见

-   <span class="function">mb\_http\_input</span>
-   <span class="function">mb\_http\_output</span>
-   <span class="function">mb\_detect\_order</span>
-   <span class="function">mb\_regex\_encoding</span>

mb\_language
============

设置/获取当前的语言

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_language</span> (\[ <span
class="methodparam"><span class="type">string</span> `$language`<span
class="initializer"> = mb\_language()</span></span> \] )

设置/获取当前的语言。

### 参数

`language`  
用于编码邮件信息。有效的语言有："Japanese","ja","English","en" 和
"uni"（UTF-8）。 <span class="function">mb\_send\_mail</span>
使用了该设置来对邮件进行编码。

语言和它的设置，日文是 ISO-2022-JP/Base64，uni 是 UTF-8/Base64，英文是
ISO-8859-1/quoted。

### 返回值

如果设置了 `language`，并且 `language` 是有效的，它将返回
**`TRUE`**。否则将返回 **`FALSE`**。 当省略了 `language`
参数，它将返回语言名称的 <span
class="type">string</span>。如果之前没有设置过语言，则将返回
**`FALSE`**。

### 参见

-   <span class="function">mb\_send\_mail</span>

mb\_list\_encodings
===================

返回所有支持编码的数组

### 说明

<span class="type">array</span> <span
class="methodname">mb\_list\_encodings</span> ( <span
class="methodparam">void</span> )

返回所有支持编码的数组。

### 参数

此函数没有参数。

### 返回值

返回一个数字索引数组。

### 错误／异常

该函数不会触发任何错误。

### 范例

**示例 \#1 <span class="function">mb\_list\_encodings</span> 例子**

``` php
<?php

print_r(mb_list_encodings());

?>
```

以上例程的输出类似于：

    Array
    (
        [0] => pass
        [1] => auto
        [2] => wchar
        [3] => byte2be
        [4] => byte2le
        [5] => byte4be
        [6] => byte4le
        [7] => BASE64
        [8] => UUENCODE
        [9] => HTML-ENTITIES
        [10] => Quoted-Printable
        [11] => 7bit
        [12] => 8bit
        [13] => UCS-4
        [14] => UCS-4BE
        [15] => UCS-4LE
        [16] => UCS-2
        [17] => UCS-2BE
        [18] => UCS-2LE
        [19] => UTF-32
        [20] => UTF-32BE
        [21] => UTF-32LE
        [22] => UTF-16
        [23] => UTF-16BE
        [24] => UTF-16LE
        [25] => UTF-8
        [26] => UTF-7
        [27] => UTF7-IMAP
        [28] => ASCII
        [29] => EUC-JP
        [30] => SJIS
        [31] => eucJP-win
        [32] => SJIS-win
        [33] => JIS
        [34] => ISO-2022-JP
        [35] => Windows-1252
        [36] => ISO-8859-1
        [37] => ISO-8859-2
        [38] => ISO-8859-3
        [39] => ISO-8859-4
        [40] => ISO-8859-5
        [41] => ISO-8859-6
        [42] => ISO-8859-7
        [43] => ISO-8859-8
        [44] => ISO-8859-9
        [45] => ISO-8859-10
        [46] => ISO-8859-13
        [47] => ISO-8859-14
        [48] => ISO-8859-15
        [49] => EUC-CN
        [50] => CP936
        [51] => HZ
        [52] => EUC-TW
        [53] => BIG-5
        [54] => EUC-KR
        [55] => UHC
        [56] => ISO-2022-KR
        [57] => Windows-1251
        [58] => CP866
        [59] => KOI8-R
    )

mb\_ord
=======

Get code point of character

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span class="methodname">mb\_ord</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`str`  

`encoding`  

### 返回值

Returns a code point of character 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">mb\_chr</span>
-   <span class="function">ord</span>

mb\_output\_handler
===================

在输出缓冲中转换字符编码的回调函数

### 说明

<span class="type">string</span> <span
class="methodname">mb\_output\_handler</span> ( <span
class="methodparam"><span class="type">string</span> `$contents`</span>
, <span class="methodparam"><span class="type">int</span>
`$status`</span> )

<span class="function">mb\_output\_handler</span> 是一个 <span
class="function">ob\_start</span> 回调函数。 <span
class="function">mb\_output\_handler</span>
将输出缓冲中的字符从内部字符编码转换为 HTTP 输出的字符编码。

### 参数

`contents`  
输出缓冲的内容。

`status`  
输出缓冲的状态。

### 返回值

转换后的 <span class="type">string</span>。

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>4.1.0</td>
<td><p>当遇到以下条件的时候，该函数将添加 HTTP 字符编码头：</p>
<ul>
<li><span class="simpara"> 未使用 <span class="function">header</span> 设置 <em>Content-Type</em>。 </span></li>
<li><span class="simpara"> 默认 MIME 类型以 <em>text/</em> 开始。 </span></li>
<li><span class="simpara"> <a href="/mbstring/setup.html#" class="link">mbstring.http_input</a> 是除 <em>pass</em> 外的任意设置。 </span></li>
</ul></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">mb\_output\_handler</span> 例子**

``` php
<?php
mb_http_output("UTF-8");
ob_start("mb_output_handler");
?>
```

### 注释

> **Note**:
>
> 如果你想要输出二进制数据，比如图片，必须在任何二进制数据发送到客户端之前使用
> <span class="function">header</span> 来设置 Content-Type: 头。（例如
> header("Content-Type: image/png")）。 如果 Content-Type:
> 头已发送，输出字符编码的转换将不会执行。
>
> 注意，如果发送了 'Content-Type:
> text/\*'，则内容被认为是文本，将发生转换。

### 参见

-   <span class="function">ob\_start</span>

mb\_parse\_str
==============

解析 GET/POST/COOKIE 数据并设置全局变量

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_parse\_str</span> ( <span
class="methodparam"><span class="type">string</span>
`$encoded_string`</span> \[, <span class="methodparam"><span
class="type">array</span> `&$result`</span> \] )

解析 GET/POST/COOKIE 数据并设置全局变量。 由于 PHP 不提供原始
POST/COOKIE 数据，目前它仅能够用于 GET 数据。 它解析了 URL
编码过的数据，检测其编码，并转换编码为内部编码，然后设置其值为 <span
class="type">array</span> 的 `result` 或者全局变量。

### 参数

`encoded_string`  
URL 编码过的数据。

`result`  
一个 <span class="type">array</span>，包含解码过的、编码转换后的值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">mb\_detect\_order</span>
-   <span class="function">mb\_internal\_encoding</span>

mb\_preferred\_mime\_name
=========================

获取 MIME 字符串

### 说明

<span class="type">string</span> <span
class="methodname">mb\_preferred\_mime\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

获取指定编码的 MIME 字符 <span class="type">string</span>。

### 参数

`encoding`  
要检查的字符串。

### 返回值

字符编码 `encoding` 的 MIME *charset* <span class="type">string</span>。

### 范例

**示例 \#1 <span class="function">mb\_preferred\_mime\_name</span>
例子**

``` php
<?php
$outputenc = "sjis-win";
mb_http_output($outputenc);
ob_start("mb_output_handler");
header("Content-Type: text/html; charset=" . mb_preferred_mime_name($outputenc));
?>
```

mb\_regex\_encoding
===================

Set/Get character encoding for multibyte regex

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_regex\_encoding</span> (\[ <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_regex\_encoding()</span></span> \] )

Set/Get character encoding for a multibyte regex.

### 参数

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

If `encoding` is set, then 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。 In this case, the internal character encoding is NOT
changed. If `encoding` is omitted, then the current character encoding
name for a multibyte regex is returned.

### 更新日志

| 版本  | 说明                                                            |
|-------|-----------------------------------------------------------------|
| 5.6.0 | Default encoding is changed to UTF-8. It was EUC-JP Previously. |

### 参见

-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">mb\_ereg</span>

mb\_regex\_set\_options
=======================

Set/Get the default options for mbregex functions

### 说明

<span class="type">string</span> <span
class="methodname">mb\_regex\_set\_options</span> (\[ <span
class="methodparam"><span class="type">string</span> `$options`<span
class="initializer"> = mb\_regex\_set\_options()</span></span> \] )

Sets the default options described by `options` for multibyte regex
functions.

### 参数

`options`  
The options to set. This is a string where each character is an option.
To set a mode, the mode character must be the last one set, however
there can only be set one mode but multiple options.

| Option | Meaning                                           |
|--------|---------------------------------------------------|
| i      | Ambiguity match on                                |
| x      | Enables extended pattern form                     |
| m      | *'.'* matches with newlines                       |
| s      | *'^'* -\> *'\\A'*, *'$'* -\> *'\\Z'*              |
| p      | Same as both the *m* and *s* options              |
| l      | Finds longest matches                             |
| n      | Ignores empty matches                             |
| e      | <span class="function">eval</span> resulting code |

| Mode | Meaning                    |
|------|----------------------------|
| j    | Java (Sun java.util.regex) |
| u    | GNU regex                  |
| g    | grep                       |
| c    | Emacs                      |
| r    | Ruby                       |
| z    | Perl                       |
| b    | POSIX Basic regex          |
| d    | POSIX Extended regex       |

### 返回值

The previous options. If `options` is omitted, it returns the <span
class="type">string</span> that describes the current options.

### 更新日志

| 版本  | 说明                                                                                                                          |
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | If the parameter `options` is given, the *previous* options are returned. Formerly, the *current* options have been returned. |

### 参见

-   <span class="function">mb\_split</span>
-   <span class="function">mb\_ereg</span>
-   <span class="function">mb\_eregi</span>

mb\_scrub
=========

Description

### 说明

<span class="type">string</span> <span
class="methodname">mb\_scrub</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`str`  

`encoding`  

### 返回值

mb\_send\_mail
==============

发送编码过的邮件

### 说明

<span class="type">bool</span> <span
class="methodname">mb\_send\_mail</span> ( <span
class="methodparam"><span class="type">string</span> `$to`</span> ,
<span class="methodparam"><span class="type">string</span>
`$subject`</span> , <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$additional_headers`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$additional_parameter`<span
class="initializer"> = **`NULL`**</span></span> \]\] )

发送邮件。邮件头和内容根据 <span class="function">mb\_language</span>
设置来转换编码。 这是 <span class="function">mail</span>
的一个包装器函数，所以详情参见 <span class="function">mail</span>。

### 参数

`to`  
被发送到该邮件地址。可通过逗号分隔地址的 `to` 来指定多个收件人。
该参数不会被自动编码。

`subject`  
邮件标题。

`message`  
邮件消息。

`additional_headers`(可选)  
String to be inserted at the end of the email header.

This is typically used to add extra headers (From, Cc, and Bcc).
Multiple extra headers should be separated with a CRLF (\\r\\n).
Validate parameter not to be injected unwanted headers by attackers.

> **Note**:
>
> When sending mail, the mail *must* contain a *From* header. This can
> be set with the `additional_headers` parameter, or a default can be
> set in `php.ini`.
>
> Failing to do this will result in an error message similar to
> *Warning: mail(): "sendmail\_from" not set in php.ini or custom
> "From:" header missing*. The *From* header sets also *Return-Path*
> under Windows.

> **Note**:
>
> If messages are not received, try using a LF (\\n) only. Some Unix
> mail transfer agents (most notably
> <a href="http://cr.yp.to/qmail.html" class="link external">» qmail</a>)
> replace LF by CRLF automatically (which leads to doubling CR if CRLF
> is used). This should be a last resort, as it does not comply with
> <a href="http://www.faqs.org/rfcs/rfc2822" class="link external">» RFC 2822</a>.

`additional_parameter`  
`additional_parameter` 是一个 MTA 命令行参数。 在使用 sendmail
时对设置正确的返回路径头很有帮助。

This parameter is escaped by <span
class="function">escapeshellcmd</span> internally to prevent command
execution. <span class="function">escapeshellcmd</span> prevents command
execution, but allows to add addtional parameters. For security reason,
this parameter should be validated.

Since <span class="function">escapeshellcmd</span> is applied
automatically, some characters that are allowed as email addresses by
internet RFCs cannot be used. Programs that are required to use these
characters <span class="function">mail</span> cannot be used.

The user that the webserver runs as should be added as a trusted user to
the sendmail configuration to prevent a 'X-Warning' header from being
added to the message when the envelope sender (-f) is set using this
method. For sendmail users, this file is `/etc/mail/trusted-users`.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">mail</span>
-   <span class="function">mb\_encode\_mimeheader</span>
-   <span class="function">mb\_language</span>

mb\_split
=========

使用正则表达式分割多字节字符串

### 说明

<span class="type">array</span> <span
class="methodname">mb\_split</span> ( <span class="methodparam"><span
class="type">string</span> `$pattern`</span> , <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = -1</span></span> \] )

使用正则表达式 `pattern` 分割多字节 `string` 并返回结果 <span
class="type">array</span>。

### 参数

`pattern`  
正则表达式。

`string`  
待分割的 <span class="type">string</span>。

`limit`  
<span class="simpara"> 如果指定了可选参数 `limit`，将最多分割为 `limit`
个元素。 </span>

### 返回值

<span class="type">array</span> 的结果。

### 注释

> **Note**:
>
> The character encoding specified by <span
> class="function">mb\_regex\_encoding</span> will be used as the
> character encoding for this function by default.

### 参见

-   <span class="function">mb\_regex\_encoding</span>
-   <span class="function">mb\_ereg</span>

mb\_str\_split
==============

Given a multibyte string, return an array of its characters

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">mb\_str\_split</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$split_length`<span class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

This function will return an array of strings, it is a version of <span
class="function">str\_split</span> with support for encodings of
variable character size as well as fixed-size encodings of 1,2 or 4 byte
characters. If the `split_length` parameter is specified, the string is
broken down into chunks of the specified length in characters (not
bytes). The `encoding` parameter can be optionally specified and it is
good practice to do so.

### 参数

`string`  
The <span class="type">string</span> to split into characters or chunks.

`split_length`  
If specified, each element of the returned array will be composed of
multiple characters instead of a single character.

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

A string specifying one of the supported encodings.

### 返回值

<span class="function">mb\_str\_split</span> returns an array of
strings, 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">str\_split</span>

mb\_strcut
==========

获取字符的一部分

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strcut</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> , <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_strcut</span> 和 <span
class="function">mb\_substr</span>
类似，都是从字符串中提取子字符串，但是按字节数来执行，而不是字符个数。
如果截断位置位于多字节字符两个字节的中间，将于该字符的第一个字节开始执行。
这也是和 <span class="function">substr</span>
函数的不同之处，后者简单地将字符串在字节之间截断，这将导致一个畸形的字节序列。

### 参数

`str`  
要截断的 <span class="type">string</span>。

`start`  
如果 `start` 不是负数，返回的字符串会从 `str` 的第 `start`
*字节*位置开始，从 0 开始计数。举个例子，字符串 '*abcdef*'，字节位置 *0*
的字符是 '*a*'，字节位置 *2* 的字符是 '*c*'，以此类推。

如果 `start` 是负数，返回的字符串是从 `str` 末尾处第 `start`
个字节开始的。

`length`  
*字节*长度。If omitted or *NULL* is passed, extract all bytes to the end
of the string.

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

<span class="function">mb\_strcut</span> 根据 `start` 和 `length`
参数返回 `str` 的一部分。

### 更新日志

| 版本  | 说明                                                                                                                              |
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| 5.4.8 | Passing *NULL* as `length` extracts all bytes to the end of the string. Prior to this version *NULL* was treated the same as *0*. |

### 参见

-   <span class="function">mb\_substr</span>
-   <span class="function">mb\_internal\_encoding</span>

mb\_strimwidth
==============

获取按指定宽度截断的字符串

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strimwidth</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">int</span> `$start`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> \[, <span class="methodparam"><span
class="type">string</span> `$trimmarker`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \]\] )

按 `width` 将<span class="type">字符串</span> `str` 截短。

### 参数

`str`  
要截短的 <span class="type">string</span>。

`start`  
开始位置的偏移。从这些字符数开始的截取字符串。（默认是 0 个字符） 如果
start 是负数，就是字符串结尾处的字符数。

`width`  
所需修剪的宽度。负数的宽度是从字符串结尾处统计的。

`trimmarker`  
当字符串被截短的时候，将此字符串添加到截短后的末尾。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

截短后的 <span class="type">string</span>。 如果设置了
`trimmarker`，还将结尾处的字符替换为 `trimmarker` ，并符合 `width`
的宽度。

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 7.1.0 | 支持负数的 `start` 和 `width`。 |

### 范例

**示例 \#1 <span class="function">mb\_strimwidth</span> 例子**

``` php
<?php
echo mb_strimwidth("Hello World", 0, 10, "...");
// 输出 Hello W...
?>
```

### 参见

-   <span class="function">mb\_strwidth</span>
-   <span class="function">mb\_internal\_encoding</span>

mb\_stripos
===========

大小写不敏感地查找字符串在另一个字符串中首次出现的位置

### 说明

<span class="type">int</span> <span
class="methodname">mb\_stripos</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_stripos</span> 返回 `needle` 在字符串
`haystack` 中首次出现位置的数值。 和 <span
class="function">mb\_strpos</span> 不同的是，<span
class="function">mb\_stripos</span> 是大小写不敏感的。 如果 `needle`
没找到，它将返回 **`FALSE`**。

### 参数

`haystack`  
在这个字符串中查找获取 `needle` 首次出现的位置

`needle`  
在 `haystack` 中查找这个字符串

`offset`  
`haystack` 里开始搜索的位置。如果是负数，就从字符串的尾部开始统计。

`encoding`  
使用的字符编码名称。 如果省略了它，将使用内部字符编码。

### 返回值

返回字符串 `haystack` 中 `needle` 首次出现位置的数值。 如果没有找到
`needle`，它将返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                     |
|-------|--------------------------|
| 7.1.0 | 支持 `offset` 使用负数。 |

### 参见

-   <span class="function">stripos</span>
-   <span class="function">strpos</span>
-   <span class="function">mb\_strpos</span>

mb\_stristr
===========

大小写不敏感地查找字符串在另一个字符串里的首次出现

### 说明

<span class="type">string</span> <span
class="methodname">mb\_stristr</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$before_needle`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_strstr</span> 查找了 `needle` 在 `haystack`
中首次的出现并返回 `haystack` 的一部分。 和 <span
class="function">mb\_strstr</span> 不同的是，<span
class="function">mb\_stristr</span> 是大小写不敏感的。 如果 `needle`
没有找到，它将返回 **`FALSE`**。

### 参数

`haystack`  
要获取 `needle` 首次出现的字符串。

`needle`  
在 `haystack` 中查找这个字符串。

`before_needle`  
决定这个函数返回 `haystack` 的哪一部分。 如果设置为 **`TRUE`**，它返回
`haystack` 中从开始到 `needle` 出现位置的所有字符（不包括 needle）。
如果设置为 **`FALSE`**，它返回 `haystack` 中 `needle`
出现位置到最后的所有字符（包括了 needle）。

`encoding`  
要使用的字符编码名称。 如果省略该参数，将使用内部字符编码。

### 返回值

返回 `haystack` 的一部分，或者 `needle` 没找到则返回 **`FALSE`**。

### 参见

-   <span class="function">stristr</span>
-   <span class="function">strstr</span>
-   <span class="function">mb\_strstr</span>

mb\_strlen
==========

获取字符串的长度

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_strlen</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \] )

获取一个 <span class="type">string</span> 的长度。

### 参数

`str`  
要检查长度的<span class="type">字符串</span>。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

返回具有 `encoding` 编码的<span class="type">字符串</span> `str`
包含的字符数。 多字节的字符被计为 1。

如果给定的 `encoding` 无效则返回 **`FALSE`**。

### 参见

-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">grapheme\_strlen</span>
-   <span class="function">iconv\_strlen</span>
-   <span class="function">strlen</span>

mb\_strpos
==========

查找字符串在另一个字符串中首次出现的位置

### 说明

<span class="type">int</span> <span class="methodname">mb\_strpos</span>
( <span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">string</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

查找 <span class="type">string</span> 在一个 <span
class="type">string</span> 中首次出现的位置。

基于字符数执行一个多字节安全的 <span class="function">strpos</span>
操作。 第一个字符的位置是 0，第二个字符的位置是 1，以此类推。

### 参数

`haystack`  
要被检查的 <span class="type">string</span>。

`needle`  
在 `haystack` 中查找这个字符串。 和 <span class="function">strpos</span>
不同的是，数字的值不会被当做字符的顺序值。

`offset`  
搜索位置的偏移。如果没有提供该参数，将会使用 0。负数的 offset
会从字符串尾部开始统计。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

返回 <span class="type">string</span> 的 `haystack` 中 `needle`
首次出现位置的数值。 如果没有找到 `needle`，它将返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                  |
|-------|-----------------------|
| 7.1.0 | 支持负数的 `offset`。 |

### 参见

-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">strpos</span>

mb\_strrchr
===========

查找指定字符在另一个字符串中最后一次的出现

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strrchr</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$part`<span class="initializer"> = false</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_strrchr</span> 查找了 `needle` 在 `haystack`
中最后一次出现的位置，并返回 `haystack` 的部分。 如果没有找到
`needle`，它将返回 **`FALSE`**。

### 参数

`haystack`  
在该字符串中查找 `needle` 最后出现的位置

`needle`  
在 `haystack` 中查找这个字符串

`part`  
决定这个函数返回 `haystack` 的哪一部分。 如果设置为
**`TRUE`**，它将返回的字符是从 `haystack` 的开始到 `needle`
最后出现的位置。 如果设置为 **`FALSE`**，它将返回的字符是从 `needle`
最后出现的位置到 `haystack` 的末尾。

`encoding`  
使用的字符编码名称。如果省略了，则将使用内部编码。

### 返回值

返回 `haystack` 的一部分。 或者在没有找到 `needle` 时返回 **`FALSE`**。

### 参见

-   <span class="function">strrchr</span>
-   <span class="function">mb\_strstr</span>
-   <span class="function">mb\_strrichr</span>

mb\_strrichr
============

大小写不敏感地查找指定字符在另一个字符串中最后一次的出现

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strrichr</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$part`<span class="initializer"> = false</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_strrichr</span> 大小写不敏感地查找指定
`needle` 在 `haystack` 中最后一次的出现，并返回 `haystack` 的一部分。 和
<span class="function">mb\_strrchr</span> 不同的是，<span
class="function">mb\_strrichr</span> 是大小写不敏感的。 如果 `needle`
没有找到，它将返回 **`FALSE`**。

### 参数

`haystack`  
在该字符串中查找 `needle` 的最后出现位置

`needle`  
在 `needle` 中查找该字符串

`part`  
决定这个函数返回 `haystack` 的哪一部分。 如果设置为
**`TRUE`**，它将返回的字符是从 `haystack` 的开始到 `needle`
最后出现的位置。 如果设置为 **`FALSE`**，它将返回的字符是从 `needle`
最后出现的位置到 `haystack` 的末尾。

`encoding`  
使用的字符编码名称。如果省略了，则将使用内部编码。

### 返回值

返回 `haystack` 的一部分。 或者在没有找到 `needle` 时返回 **`FALSE`**。

### 参见

-   <span class="function">mb\_stristr</span>
-   <span class="function">mb\_strrchr</span>

mb\_strripos
============

大小写不敏感地在字符串中查找一个字符串最后出现的位置

### 说明

<span class="type">int</span> <span
class="methodname">mb\_strripos</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_strripos</span>
基于字符数执行一个多字节安全的 <span class="function">strripos</span>
操作。 `needle` 的位置是从 `haystack` 的开始进行统计的。
第一个字符的位置是 0，第二个字符的位置是 1。 和 <span
class="function">mb\_strrpos</span> 不同的是，<span
class="function">mb\_strripos</span> 是大小写不敏感的。

### 参数

`haystack`  
查找 `needle` 在这个字符串中最后出现的位置。

`needle`  
在 `haystack` 中查找这个字符串。

`offset`  
在 `haystack` 中开始搜索的位置。

`encoding`  
使用的字符编码名称。如果省略了，则将使用内部编码。

### 返回值

返回字符串 `haystack` 中 `needle` 最后出现位置的数值。 如果没有找到
`needle`，它将返回 **`FALSE`**。

### 参见

-   <span class="function">strripos</span>
-   <span class="function">strrpos</span>
-   <span class="function">mb\_strrpos</span>

mb\_strrpos
===========

查找字符串在一个字符串中最后出现的位置

### 说明

<span class="type">int</span> <span
class="methodname">mb\_strrpos</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

基于字符数执行一个多字节安全的 <span class="function">strrpos</span>
操作。 `needle` 的位置是从 `haystack` 的开始进行统计的。
第一个字符的位置是 0，第二个字符的位置是 1。

### 参数

`haystack`  
查找 `needle` 在这个 <span class="type">string</span> 中最后出现的位置。

`needle`  
在 `haystack` 中查找这个 <span class="type">string</span>。

`offset`  
<span class="simpara"> 可以用于指定 <span class="type">string</span>
里从任意字符数开始进行搜索。 负数的值将导致搜索会终止于指向 <span
class="type">string</span> 末尾的任意点。 </span>

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

返回 <span class="type">string</span> 的 `haystack` 中，`needle`
最后出现位置的数值。 如果没有找到 `needle`，它将返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                      |
|-------|---------------------------|
| 5.2.0 | 增加了可选参数 `offset`。 |

### 注释

> **Note**: <span class="simpara"> 从 PHP 5.2.0 开始，`encoding`
> 参数从第三个位置移到了第四个位置。
> 为实现向后兼容，可以将第三个参数指定为
> `encoding`，但不建议这么做，在将来会移除这个特性。 </span>

### 参见

-   <span class="function">mb\_strpos</span>
-   <span class="function">mb\_internal\_encoding</span>
-   <span class="function">strrpos</span>

mb\_strstr
==========

查找字符串在另一个字符串里的首次出现

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strstr</span> ( <span class="methodparam"><span
class="type">string</span> `$haystack`</span> , <span
class="methodparam"><span class="type">string</span> `$needle`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$before_needle`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \]\] )

<span class="function">mb\_strstr</span> 查找了 `needle` 在 `haystack`
中首次的出现并返回 `haystack` 的一部分。 如果 `needle`
没有找到，它将返回 **`FALSE`**。

### 参数

`haystack`  
要获取 `needle` 首次出现的字符串。

`needle`  
在 `haystack` 中查找这个字符串。

`before_needle`  
决定这个函数返回 `haystack` 的哪一部分。 如果设置为 **`TRUE`**，它返回
`haystack` 中从开始到 `needle` 出现位置的所有字符（不包括 needle）。
如果设置为 **`FALSE`**，它返回 `haystack` 中 `needle`
出现位置到最后的所有字符（包括了 needle）。

`encoding`  
要使用的字符编码名称。 如果省略该参数，将使用内部字符编码。

### 返回值

返回 `haystack` 的一部分，或者 `needle` 没找到则返回 **`FALSE`**。

### 参见

-   <span class="function">stristr</span>
-   <span class="function">strstr</span>
-   <span class="function">mb\_stristr</span>

mb\_strtolower
==============

使字符串小写

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strtolower</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \] )

返回所有字母字符转换成小写的 `str`。

### 参数

`str`  
要被小写的<span class="type">字符串</span>。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

所有字母字符已被转换成小写的 `str`。

### Unicode

更多关于 Unicode 属性的信息，请参见
<a href="http://www.unicode.org/unicode/reports/tr21/" class="link external">» http://www.unicode.org/unicode/reports/tr21/</a>。

和 <span class="function">strtolower</span>
不同的是，“字母”字符的检测是根据字符的 Unicode 属性。
因此函数的行为不会受语言设置的影响，能偶转换任意具有“字母”属性的字符，例如元音变音
A（Ä）。

### 范例

**示例 \#1 <span class="function">mb\_strtolower</span> 例子**

``` php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = mb_strtolower($str);
echo $str; // 输出： mary had a little lamb and she loved it so
?>
```

**示例 \#2 非拉丁 UTF-8 文本的 <span
class="function">mb\_strtolower</span> 例子**

``` php
<?php
$str = "Τάχιστη αλώπηξ βαφής ψημένη γη, δρασκελίζει υπέρ νωθρού κυνός";
$str = mb_strtolower($str, 'UTF-8');
echo $str; // 输出 τάχιστη αλώπηξ βαφής ψημένη γη, δρασκελίζει υπέρ νωθρού κυνός
?>
```

### 参见

-   <span class="function">mb\_strtoupper</span>
-   <span class="function">mb\_convert\_case</span>
-   <span class="function">strtolower</span>

mb\_strtoupper
==============

使字符串大写

### 说明

<span class="type">string</span> <span
class="methodname">mb\_strtoupper</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \] )

将所有的字母字符转化成大写并返回 `str`。

### 参数

`str`  
要大写的 <span class="type">string</span>。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

`str` 里所有的字母都转换成大写的。

### Unicode

更多 Unicode 属性的信息，请参见
<a href="http://www.unicode.org/unicode/reports/tr21/" class="link external">» http://www.unicode.org/unicode/reports/tr21/</a>。

和 <span class="function">strtoupper</span> 不同的是，“字母”是通过
Unicode 字符属性来确定的。
因此这个函数不会受语言环境（locale）设置影响，能够转化任何具有“字母”属性的字符，例如
a 变音符号（ä）。

### 范例

**示例 \#1 <span class="function">mb\_strtoupper</span> 例子**

``` php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = mb_strtoupper($str);
echo $str; // Prints MARY HAD A LITTLE LAMB AND SHE LOVED IT SO
?>
```

**示例 \#2 非拉丁 UTF-8 文本的 <span
class="function">mb\_strtoupper</span> 例子**

``` php
<?php
$str = "Τάχιστη αλώπηξ βαφής ψημένη γη, δρασκελίζει υπέρ νωθρού κυνός";
$str = mb_strtoupper($str, 'UTF-8');
echo $str; // 打印了 ΤΆΧΙΣΤΗ ΑΛΏΠΗΞ ΒΑΦΉΣ ΨΗΜΈΝΗ ΓΗ, ΔΡΑΣΚΕΛΊΖΕΙ ΥΠΈΡ ΝΩΘΡΟΎ ΚΥΝΌΣ
?>
```

### 参见

-   <span class="function">mb\_strtolower</span>
-   <span class="function">mb\_convert\_case</span>
-   <span class="function">strtoupper</span>

mb\_strwidth
============

返回字符串的宽度

### 说明

<span class="type">int</span> <span
class="methodname">mb\_strwidth</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \] )

返回 <span class="type">string</span> 类型 `str` 的宽度。

多字节字符通常是单字节字符的两倍宽度。

| 字符            | 宽度 |
|-----------------|------|
| U+0000 - U+0019 | 0    |
| U+0020 - U+1FFF | 1    |
| U+2000 - U+FF60 | 2    |
| U+FF61 - U+FF9F | 1    |
| U+FFA0 -        | 2    |

### 参数

`str`  
待解码的 <span class="type">string</span>。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

<span class="type">string</span> `str` 的宽度。

### 参见

-   <span class="function">mb\_strimwidth</span>
-   <span class="function">mb\_internal\_encoding</span>

mb\_substitute\_character
=========================

设置/获取替代字符

### 说明

<span class="type">mixed</span> <span
class="methodname">mb\_substitute\_character</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$substchar`<span
class="initializer"> = mb\_substitute\_character()</span></span> \] )

当输入字符的编码是无效的，或者字符代码不存在于输出的字符编码中时，可以为其指定一个替代字符。
无效字符可以被替换为 **`NULL`**（不输出）、<span
class="type">string</span> 或者 <span class="type">integer</span>
值（Unicode 字符代码的值）。

该设置会影响 <span class="function">mb\_convert\_encoding</span>、 <span
class="function">mb\_convert\_variables</span>、 <span
class="function">mb\_output\_handler</span> 和 <span
class="function">mb\_send\_mail</span>。

### 参数

`substchar`  
指定 Unicode 值为一个 <span class="type">integer</span>，或者是以下<span
class="type">字符串</span>中的一个：

-   <span class="simpara"> *"none"*:：不输出 </span>
-   <span class="simpara">
    *"long"*：输出字符代码的值（比如：*U+3000*、*JIS+7E7E*） </span>
-   <span class="simpara">
    *"entity"*：输出字符的实体（比如：*&\#x200;*） </span>

### 返回值

如果设置了 `substchar`，在成功时返回 **`TRUE`**，失败时返回
**`FALSE`**。 如果没有设置 `substchar`，它将返回当前设置。

### 范例

**示例 \#1 <span class="function">mb\_substitute\_character</span>
例子**

``` php
<?php
/* 设置为 Unicode U+3013 (GETA MARK) */
mb_substitute_character(0x3013);

/* 设置十六进制格式 */
mb_substitute_character("long");

/* 显示当前设置 */
echo mb_substitute_character();
?>
```

mb\_substr\_count
=================

统计字符串出现的次数

### 说明

<span class="type">int</span> <span
class="methodname">mb\_substr\_count</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
mb\_internal\_encoding()</span></span> \] )

统计子字符串 `needle` 出现在<span class="type">字符串</span> `haystack`
中的次数。

### 参数

`haystack`  
要检查的<span class="type">字符串</span>。

`needle`  
待查找的<span class="type">字符串</span>。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

子字符串 `needle` 出现在<span class="type">字符串</span> `haystack`
中的次数。

### 范例

**示例 \#1 <span class="function">mb\_substr\_count</span> 例子**

``` php
<?php
echo mb_substr_count("This is a test", "is"); // 输出 2
?>
```

### 参见

-   <span class="function">mb\_strpos</span>
-   <span class="function">mb\_substr</span>
-   <span class="function">substr\_count</span>

mb\_substr
==========

获取部分字符串

### 说明

<span class="type">string</span> <span
class="methodname">mb\_substr</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> , <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = mb\_internal\_encoding()</span></span> \]\] )

根据字符数执行一个多字节安全的 <span class="function">substr</span>
操作。 位置是从 `str` 的开始位置进行计数。 第一个字符的位置是
0。第二个字符的位置是 1，以此类推。

### 参数

`str`  
从该 <span class="type">string</span> 中提取子字符串。

`start`  
如果 `start` 不是负数，返回的字符串会从 `str` 第 `start` 的位置开始，从
0 开始计数。举个例子，字符串 '*abcdef*'，位置 *0* 的字符是 '*a*'，位置
*2* 的字符是 '*c*'，以此类推。

如果 `start` 是负数，返回的字符串是从 `str` 末尾处第 `start`
个字符开始的。

`length`  
`str` 中要使用的最大字符数。如果省略了此参数或者传入了
*NULL*，则会提取到字符串的尾部。

`encoding`  
`encoding` 参数为字符编码。如果省略，则使用内部字符编码。

### 返回值

<span class="function">mb\_substr</span> 函数根据 `start` 和 `length`
参数返回 `str` 中指定的部分。

### 更新日志

| 版本  | 说明                                                                                                  |
|-------|-------------------------------------------------------------------------------------------------------|
| 5.4.8 | `length` 传入 *NULL*，则从 start 提取到字符串的结尾处。 在之前的版本里， *NULL* 会被当作 *0* 来处理。 |

### 参见

-   <span class="function">mb\_strcut</span>
-   <span class="function">mb\_internal\_encoding</span>

**目录**

-   [mb\_check\_encoding](/ref/mbstring.html#mb_check_encoding) —
    检查字符串在指定的编码里是否有效
-   [mb\_chr](/ref/mbstring.html#mb_chr) — Get a specific character
-   [mb\_convert\_case](/ref/mbstring.html#mb_convert_case) —
    对字符串进行大小写转换
-   [mb\_convert\_encoding](/ref/mbstring.html#mb_convert_encoding) —
    转换字符的编码
-   [mb\_convert\_kana](/ref/mbstring.html#mb_convert_kana) — Convert
    "kana" one from another ("zen-kaku", "han-kaku" and more)
-   [mb\_convert\_variables](/ref/mbstring.html#mb_convert_variables) —
    转换一个或多个变量的字符编码
-   [mb\_decode\_mimeheader](/ref/mbstring.html#mb_decode_mimeheader) —
    解码 MIME 头字段中的字符串
-   [mb\_decode\_numericentity](/ref/mbstring.html#mb_decode_numericentity)
    — 根据 HTML 数字字符串解码成字符
-   [mb\_detect\_encoding](/ref/mbstring.html#mb_detect_encoding) —
    检测字符的编码
-   [mb\_detect\_order](/ref/mbstring.html#mb_detect_order) — 设置/获取
    字符编码的检测顺序
-   [mb\_encode\_mimeheader](/ref/mbstring.html#mb_encode_mimeheader) —
    为 MIME 头编码字符串
-   [mb\_encode\_numericentity](/ref/mbstring.html#mb_encode_numericentity)
    — Encode character to HTML numeric string reference
-   [mb\_encoding\_aliases](/ref/mbstring.html#mb_encoding_aliases) —
    Get aliases of a known encoding type
-   [mb\_ereg\_match](/ref/mbstring.html#mb_ereg_match) — Regular
    expression match for multibyte string
-   [mb\_ereg\_replace\_callback](/ref/mbstring.html#mb_ereg_replace_callback)
    — Perform a regular expression search and replace with multibyte
    support using a callback
-   [mb\_ereg\_replace](/ref/mbstring.html#mb_ereg_replace) — Replace
    regular expression with multibyte support
-   [mb\_ereg\_search\_getpos](/ref/mbstring.html#mb_ereg_search_getpos)
    — Returns start point for next regular expression match
-   [mb\_ereg\_search\_getregs](/ref/mbstring.html#mb_ereg_search_getregs)
    — Retrieve the result from the last multibyte regular expression
    match
-   [mb\_ereg\_search\_init](/ref/mbstring.html#mb_ereg_search_init) —
    Setup string and regular expression for a multibyte regular
    expression match
-   [mb\_ereg\_search\_pos](/ref/mbstring.html#mb_ereg_search_pos) —
    Returns position and length of a matched part of the multibyte
    regular expression for a predefined multibyte string
-   [mb\_ereg\_search\_regs](/ref/mbstring.html#mb_ereg_search_regs) —
    Returns the matched part of a multibyte regular expression
-   [mb\_ereg\_search\_setpos](/ref/mbstring.html#mb_ereg_search_setpos)
    — Set start point of next regular expression match
-   [mb\_ereg\_search](/ref/mbstring.html#mb_ereg_search) — Multibyte
    regular expression match for predefined multibyte string
-   [mb\_ereg](/ref/mbstring.html#mb_ereg) — Regular expression match
    with multibyte support
-   [mb\_eregi\_replace](/ref/mbstring.html#mb_eregi_replace) — Replace
    regular expression with multibyte support ignoring case
-   [mb\_eregi](/ref/mbstring.html#mb_eregi) — Regular expression match
    ignoring case with multibyte support
-   [mb\_get\_info](/ref/mbstring.html#mb_get_info) — 获取 mbstring
    的内部设置
-   [mb\_http\_input](/ref/mbstring.html#mb_http_input) — 检测 HTTP
    输入字符编码
-   [mb\_http\_output](/ref/mbstring.html#mb_http_output) — 设置/获取
    HTTP 输出字符编码
-   [mb\_internal\_encoding](/ref/mbstring.html#mb_internal_encoding) —
    设置/获取内部字符编码
-   [mb\_language](/ref/mbstring.html#mb_language) — 设置/获取当前的语言
-   [mb\_list\_encodings](/ref/mbstring.html#mb_list_encodings) —
    返回所有支持编码的数组
-   [mb\_ord](/ref/mbstring.html#mb_ord) — Get code point of character
-   [mb\_output\_handler](/ref/mbstring.html#mb_output_handler) —
    在输出缓冲中转换字符编码的回调函数
-   [mb\_parse\_str](/ref/mbstring.html#mb_parse_str) — 解析
    GET/POST/COOKIE 数据并设置全局变量
-   [mb\_preferred\_mime\_name](/ref/mbstring.html#mb_preferred_mime_name)
    — 获取 MIME 字符串
-   [mb\_regex\_encoding](/ref/mbstring.html#mb_regex_encoding) —
    Set/Get character encoding for multibyte regex
-   [mb\_regex\_set\_options](/ref/mbstring.html#mb_regex_set_options) —
    Set/Get the default options for mbregex functions
-   [mb\_scrub](/ref/mbstring.html#mb_scrub) — Description
-   [mb\_send\_mail](/ref/mbstring.html#mb_send_mail) — 发送编码过的邮件
-   [mb\_split](/ref/mbstring.html#mb_split) —
    使用正则表达式分割多字节字符串
-   [mb\_str\_split](/ref/mbstring.html#mb_str_split) — Given a
    multibyte string, return an array of its characters
-   [mb\_strcut](/ref/mbstring.html#mb_strcut) — 获取字符的一部分
-   [mb\_strimwidth](/ref/mbstring.html#mb_strimwidth) —
    获取按指定宽度截断的字符串
-   [mb\_stripos](/ref/mbstring.html#mb_stripos) —
    大小写不敏感地查找字符串在另一个字符串中首次出现的位置
-   [mb\_stristr](/ref/mbstring.html#mb_stristr) —
    大小写不敏感地查找字符串在另一个字符串里的首次出现
-   [mb\_strlen](/ref/mbstring.html#mb_strlen) — 获取字符串的长度
-   [mb\_strpos](/ref/mbstring.html#mb_strpos) —
    查找字符串在另一个字符串中首次出现的位置
-   [mb\_strrchr](/ref/mbstring.html#mb_strrchr) —
    查找指定字符在另一个字符串中最后一次的出现
-   [mb\_strrichr](/ref/mbstring.html#mb_strrichr) —
    大小写不敏感地查找指定字符在另一个字符串中最后一次的出现
-   [mb\_strripos](/ref/mbstring.html#mb_strripos) —
    大小写不敏感地在字符串中查找一个字符串最后出现的位置
-   [mb\_strrpos](/ref/mbstring.html#mb_strrpos) —
    查找字符串在一个字符串中最后出现的位置
-   [mb\_strstr](/ref/mbstring.html#mb_strstr) —
    查找字符串在另一个字符串里的首次出现
-   [mb\_strtolower](/ref/mbstring.html#mb_strtolower) — 使字符串小写
-   [mb\_strtoupper](/ref/mbstring.html#mb_strtoupper) — 使字符串大写
-   [mb\_strwidth](/ref/mbstring.html#mb_strwidth) — 返回字符串的宽度
-   [mb\_substitute\_character](/ref/mbstring.html#mb_substitute_character)
    — 设置/获取替代字符
-   [mb\_substr\_count](/ref/mbstring.html#mb_substr_count) —
    统计字符串出现的次数
-   [mb\_substr](/ref/mbstring.html#mb_substr) — 获取部分字符串
