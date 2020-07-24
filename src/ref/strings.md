更多强大的字符串处理函数，参见
<a href="/ref/pcre.html" class="link">Perl 兼容正则表达式函数</a>。
需要处理多字节字符集，参见
<a href="/ref/mbstring.html" class="link">多字节字符函数</a>。

addcslashes
===========

以 C 语言风格使用反斜线转义字符串中的字符

### 说明

<span class="type">string</span> <span
class="methodname">addcslashes</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> , <span
class="methodparam"><span class="type">string</span> `$charlist`</span>
)

返回字符串，该字符串在属于参数 `charlist` 列表中的字符前都加上了反斜线。

### 参数

`str`  
要转义的字符。

`charlist`  
如果 `charlist` 中包含有 *\\n*，*\\r* 等字符，将以 C
语言风格转换，而其它非字母数字且 ASCII 码低于 32 以及高于 126
的字符均转换成使用八进制表示。

当定义 charlist
参数中的字符序列时，需要确实知道介于自己设置的开始及结束范围之内的都是些什么字符。

``` php
<?php
echo addcslashes('foo[ ]', 'A..z');
// 输出：\f\o\o\[ \]
// 所有大小写字母均被转义
// ... 但 [\]^_` 以及分隔符、换行符、回车符等也一并被转义了。
?>
```

另外，如果设置范围中的结束字符 ASCII
码高于开始字符，则不会创建范围，只是将开始字符、结束字符以及其间的字符逐个转义。可使用
<span class="function">ord</span> 函数获取字符的 ASCII 码值。

``` php
<?php
echo addcslashes("zoo['.']", 'z..A');
// 输出：\zoo['\.']
?>
```

当选择对字符 0，a，b，f，n，r，t 和 v 进行转义时需要小心，它们将被转换成
\\0，\\a，\\b，\\f，\\n，\\r，\\t 和 \\v。在 PHP 中，只有
\\0（NULL），\\r（回车符），\\n（换行符）和
\\t（制表符）是预定义的转义序列， 而在 C
语言中，上述的所有转换后的字符都是预定义的转义序列。

### 返回值

返回转义后的字符。

### 更新日志

| 版本  | 说明                                         |
|-------|----------------------------------------------|
| 5.2.5 | The escape sequences \\v and \\f were added. |

### 范例

`charlist` 参数，如“\\0..\\37”，将转义所有 ASCII 码介于 0 和 31
之间的字符。

**示例 \#1 <span class="function">addcslashes</span> 例子**

``` php
<?php
$escaped = addcslashes($not_escaped, "\0..\37!@\177..\377");
?>
```

### 参见

-   <span class="function">stripcslashes</span>
-   <span class="function">stripslashes</span>
-   <span class="function">addslashes</span>
-   <span class="function">htmlspecialchars</span>
-   <span class="function">quotemeta</span>

addslashes
==========

使用反斜线引用字符串

### 说明

<span class="type">string</span> <span
class="methodname">addslashes</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

返回字符串，该字符串为了数据库查询语句等的需要在某些字符前加上了反斜线。这些字符是单引号（*'*）、双引号（*"*）、反斜线（*\\*）与
NUL（**`NULL`** 字符）。

一个使用 <span class="function">addslashes</span>
的例子是当你要往数据库中输入数据时。 例如，将名字 *O'reilly*
插入到数据库中，这就需要对其进行转义。 强烈建议使用 DBMS 指定的转义函数
（比如 MySQL 是 <span
class="function">mysqli\_real\_escape\_string</span>，PostgreSQL 是
<span class="function">pg\_escape\_string</span>），但是如果你使用的
DBMS 没有一个转义函数，并且使用 *\\*
来转义特殊字符，你可以使用这个函数。
仅仅是为了获取插入数据库的数据，额外的 *\\* 并不会插入。 当 PHP 指令
<a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>
被设置成 *on* 时，意味着插入 *'* 时将使用 *'* 进行转义。

PHP 5.4 之前 PHP 指令
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a> 默认是
*on*， 实际上所有的 GET、POST 和 COOKIE 数据都用被 <span
class="function">addslashes</span> 了。 不要对已经被
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
转义过的字符串使用 <span
class="function">addslashes</span>，因为这样会导致双层转义。
遇到这种情况时可以使用函数 <span
class="function">get\_magic\_quotes\_gpc</span> 进行检测。

### 参数

`str`  
要转义的字符。

### 返回值

返回转义后的字符。

### 范例

**示例 \#1 一个 <span class="function">addslashes</span> 例子**

``` php
<?php
$str = "Is your name O'reilly?";

// 输出： Is your name O\'reilly?
echo addslashes($str);
?>
```

### 参见

-   <span class="function">stripcslashes</span>
-   <span class="function">stripslashes</span>
-   <span class="function">addcslashes</span>
-   <span class="function">htmlspecialchars</span>
-   <span class="function">quotemeta</span>
-   <span class="function">get\_magic\_quotes\_gpc</span>

bin2hex
=======

函数把包含数据的二进制字符串转换为十六进制值

### 说明

<span class="type">string</span> <span class="methodname">bin2hex</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> )

把二进制的参数 `str`
转换为的十六进制的字符串。转换使用字节方式，高四位字节优先。

### 参数

`str`  
二进制字符串。

### 返回值

返回指定字符串十六进制的表示。

### 参见

-   <span class="function">hex2bin</span>
-   <span class="function">pack</span>

chop
====

<span class="function">rtrim</span> 的别名

### 说明

此函数是该函数的别名：<span class="function">rtrim</span>。

### 注释

> **Note**:
>
> <span class="function">chop</span> 与 Perl 的 *chop()*
> 函数有所不同，它会删除字符串的最后一个字符。

chr
===

返回指定的字符

### 说明

<span class="type">string</span> <span class="methodname">chr</span> (
<span class="methodparam"><span class="type">int</span> `$ascii`</span>
)

返回相对应于 `ascii` 所指定的单个字符。

此函数与 <span class="function">ord</span> 是互补的。

### 参数

`ascii`  
Ascii 码。

### 返回值

返回规定的字符。

### 范例

**示例 \#1 <span class="function">chr</span> 例子**

``` php
<?php
$str = "The string ends in escape: ";
$str .= chr(27); /* 在 $str 后边增加换码符 */

/* 通常这样更有用 */

$str = sprintf("The string ends in escape: %c", 27);
?>
```

### 参见

-   <span class="function">sprintf</span> 如何使用格式字符串 *%c*。
-   <span class="function">ord</span>
-   可以在此处找到 ASCII
    码表：<a href="http://www.asciitable.com" class="link external">» http://www.asciitable.com</a>。

chunk\_split
============

将字符串分割成小块

### 说明

<span class="type">string</span> <span
class="methodname">chunk\_split</span> ( <span class="methodparam"><span
class="type">string</span> `$body`</span> \[, <span
class="methodparam"><span class="type">int</span> `$chunklen`<span
class="initializer"> = 76</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$end`<span
class="initializer"> = "\\r\\n"</span></span> \]\] )

使用此函数将字符串分割成小块非常有用。例如将 <span
class="function">base64\_encode</span> 的输出转换成符合 RFC 2045
语义的字符串。它会在每 `chunklen` 个字符后边插入 `end`。

### 参数

`body`  
要分割的字符。

`chunklen`  
分割的尺寸。

`end`  
行尾序列符号。

### 返回值

返回分割后的字符。

### 范例

**示例 \#1 <span class="function">chunk\_split</span> 例子**

``` php
<?php
// 使用 RFC 2045 语义格式化 $data
$new_string = chunk_split(base64_encode($data));
?>
```

### 参见

-   <span class="function">str\_split</span>
-   <span class="function">explode</span>
-   <span class="function">split</span>
-   <span class="function">wordwrap</span>
-   <a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC 2045</a>

convert\_cyr\_string
====================

将字符由一种 Cyrillic 字符转换成另一种

### 说明

<span class="type">string</span> <span
class="methodname">convert\_cyr\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> ,
<span class="methodparam"><span class="type">string</span>
`$from`</span> , <span class="methodparam"><span
class="type">string</span> `$to`</span> )

此函数将给定的字符串从一种 Cyrillic
字符转换成另一种，返回转换之后的字符串。

### 参数

`str`  
要转换的字符。

`from`  
单个字符，代表源 Cyrillic 字符集。

`to`  
单个字符，代表了目标 Cyrillic 字符集。

支持的类型有：

-   <span class="simpara"> k - koi8-r </span>
-   <span class="simpara"> w - windows-1251 </span>
-   <span class="simpara"> i - iso8859-5 </span>
-   <span class="simpara"> a - x-cp866 </span>
-   <span class="simpara"> d - x-cp866 </span>
-   <span class="simpara"> m - x-mac-cyrillic </span>

### 返回值

返回转换后的字符串。

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

convert\_uudecode
=================

解码一个 uuencode 编码的字符串

### 说明

<span class="type">string</span> <span
class="methodname">convert\_uudecode</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">convert\_uudecode</span> 解码一个 uuencode
编码的字符串。

### 参数

`data`  
uuencode 编码后的数据

### 返回值

返回解码后的字符串数据， 或者在失败时返回 **`FALSE`**.。

### 范例

**示例 \#1 <span class="function">convert\_uudecode</span> 例子**

``` php
<?php
/* 你猜会输出啥？:) */
echo convert_uudecode("+22!L;W9E(%!(4\"$`\n`");
?>
```

### 参见

-   <span class="function">convert\_uuencode</span>

convert\_uuencode
=================

使用 uuencode 编码一个字符串

### 说明

<span class="type">string</span> <span
class="methodname">convert\_uuencode</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="function">convert\_uuencode</span> 使用 uuencode
算法对一个字符串进行编码。

uuencode 算法会将所有（含二进制数据）字符串转化为可输出的字符，
并且可以被安全的应用于网络传输。使用 uuencode 编码后的数据
将会比源数据大35%左右

### 参数

`data`  
需要被编码的数据。

### 返回值

返回 uuencode 编码后的数据 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">convert\_uuencode</span> 例子**

``` php
<?php
$some_string = "test\ntext text\r\n";

echo convert_uuencode($some_string);
?>
```

### 参见

-   <span class="function">convert\_uudecode</span>
-   <span class="function">base64\_encode</span>

count\_chars
============

返回字符串所用字符的信息

### 说明

<span class="type">mixed</span> <span
class="methodname">count\_chars</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

统计 `string` 中每个字节值（0..255）出现的次数，使用多种模式返回结果。

### 参数

`string`  
需要统计的字符串。

`mode`  
参见返回的值。

### 返回值

根据不同的 `mode`，<span class="function">count\_chars</span>
返回下列不同的结果：

-   <span class="simpara"> 0 -
    以所有的每个字节值作为键名，出现次数作为值的数组。 </span>
-   <span class="simpara"> 1 - 与 0
    相同，但只列出出现次数大于零的字节值。 </span>
-   <span class="simpara"> 2 - 与 0
    相同，但只列出出现次数等于零的字节值。 </span>
-   <span class="simpara"> 3 - 返回由所有使用了的字节值组成的字符串。
    </span>
-   <span class="simpara"> 4 - 返回由所有未使用的字节值组成的字符串。
    </span>

### 范例

**示例 \#1 <span class="function">count\_chars</span> 示例**

``` php
<?php
$data = "Two Ts and one F.";

foreach (count_chars($data, 1) as $i => $val) {
   echo "There were $val instance(s) of \"" , chr($i) , "\" in the string.\n";
}
?>
```

以上例程会输出：

    There were 4 instance(s) of " " in the string.
    There were 1 instance(s) of "." in the string.
    There were 1 instance(s) of "F" in the string.
    There were 2 instance(s) of "T" in the string.
    There were 1 instance(s) of "a" in the string.
    There were 1 instance(s) of "d" in the string.
    There were 1 instance(s) of "e" in the string.
    There were 2 instance(s) of "n" in the string.
    There were 2 instance(s) of "o" in the string.
    There were 1 instance(s) of "s" in the string.
    There were 1 instance(s) of "w" in the string.

### 参见

-   <span class="function">strpos</span>
-   <span class="function">substr\_count</span>

crc32
=====

计算一个字符串的 crc32 多项式

### 说明

<span class="type">int</span> <span class="methodname">crc32</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
)

生成 `str` 的 32
位循环冗余校验码多项式。这通常用于检查传输的数据是否完整。

**Warning**

由于 PHP 的整数是带符号的，所以在 32 位系统上许多 crc32
校验码将返回负整数。 尽管在 64 位上所有 <span
class="function">crc32</span> 的结果将都是正整数。

因此你需要使用 <span class="function">sprintf</span> 或 <span
class="function">printf</span> 的“%u”格式符来获取表示无符号 crc32
校验码的字符串。

For a hexadecimal representation of the checksum you can either use the
"%x" formatter of <span class="function">sprintf</span> or <span
class="function">printf</span> or the <span
class="function">dechex</span> conversion functions, both of these also
take care of converting the <span class="function">crc32</span> result
to an unsigned integer.

Having 64bit installations also return negative integers for higher
result values was considered but would break the hexadecimal conversion
as negatives would get an extra 0xFFFFFFFF\#\#\#\#\#\#\#\# offset then.
As hexadecimal representation seems to be the most common use case we
decided to not break this even if it breaks direct decimal comparisons
in about 50% of the cases when moving from 32 to 64bits.

In retrospect having the function return an integer maybe wasn't the
best idea and returning a hex string representation right away (as e.g.
<span class="function">md5</span> does) might have been a better plan to
begin with.

For a more portable solution you may also consider the generic <span
class="function">hash</span>. `hash("crc32b", $str)` will return the
same string as `dechex(crc32($str))`.

### 参数

`str`  
要校验的数据。

### 返回值

返回 `str` crc32 校验的整数。

### 范例

**示例 \#1 显示一个 crc32 校验码**

示例中的第二行演示了如何使用 <span class="function">printf</span>
函数转换校验码：

``` php
<?php
$checksum = crc32("The quick brown fox jumped over the lazy dog.");
printf("%u\n", $checksum);
?>
```

### 参见

-   <span class="function">hash</span>
-   <span class="function">md5</span>
-   <span class="function">sha1</span>

crypt
=====

单向字符串散列

### 说明

<span class="type">string</span> <span class="methodname">crypt</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$salt`</span> \] )

<span class="function">crypt</span> 返回一个基于标准 UNIX DES
算法或系统上其他可用的替代算法的散列字符串。

`salt` 参数是可选的。然而，如果没有`salt`的话，<span
class="function">crypt</span>创建出来的会是弱密码。 php
5.6及之后的版本会在没有它的情况下抛出一个 E\_NOTICE
级别的错误。为了更好的安全性，请确保指定一个足够强度的盐值。

<span
class="function">password\_hash</span>使用了一个强的哈希算法，来产生足够强的盐值，并且会自动进行合适的轮次。<span
class="function">password\_hash</span>是<span
class="function">crypt</span>的一个简单封装，并且完全与现有的密码哈希兼容。推荐使用<span
class="function">password\_hash</span>。

有些系统支持不止一种散列类型。实际上，有时候，基于 MD5
的算法被用来替代基于标准 DES 的算法。这种散列类型由盐值参数触发。在 5.3
之前，PHP 在安装时根据系统的 crypt()
决定可用的算法。如果没有提供盐值，PHP 将自动生成一个 2 个字符（DES）或者
12 个字符（MD5）的盐值 ，这取决于 MD5 crypt() 的可用性。PHP
设置了一个名为 **`CRYPT_SALT_LENGTH`**
的常量，用来表示可用散列允许的最长可用盐值。

基于标准 DES 算法的 <span class="function">crypt</span>
在输出内容的开始位置返回两个字符的盐值。它也只使用 `str` 的开始 8
个字符，所以更长的以相同 8
个字符开始的字符串也将生成相同的结果（当使用了相同的盐值时）。

在 crypt()
函数支持多重散列的系统上，下面的常量根据相应的类型是否可用被设置为 0 或
1：

-   <span class="simpara"> **`CRYPT_STD_DES`** - 基于标准 DES
    算法的散列使用 "./0-9A-Za-z"
    字符中的两个字符作为盐值。在盐值中使用非法的字符将导致 crypt()
    失败。 </span>
-   <span class="simpara"> **`CRYPT_EXT_DES`** - 扩展的基于 DES
    算法的散列。其盐值为 9 个字符的字符串，由 1 个下划线后面跟着 4
    字节循环次数和 4 字节盐值组成。它们被编码成可打印字符，每个字符 6
    位，有效位最少的优先。0 到 63 被编码为
    "./0-9A-Za-z"。在盐值中使用非法的字符将导致 crypt() 失败。 </span>
-   <span class="simpara"> **`CRYPT_MD5`** - MD5 散列使用一个以 $1$
    开始的 12 字符的字符串盐值。 </span>
-   <span class="simpara"> **`CRYPT_BLOWFISH`** - Blowfish
    算法使用如下盐值：“$2a$”，一个两位 cost 参数，“$” 以及 64 位由
    “./0-9A-Za-z”
    中的字符组合而成的字符串。在盐值中使用此范围之外的字符将导致 crypt()
    返回一个空字符串。两位 cost 参数是循环次数以 2
    为底的对数，它的范围是 04-31，超出这个范围将导致 crypt() 失败。 PHP
    5.3.7 之前只支持 “$2a$” 作为盐值的前缀，PHP 5.3.7
    开始引入了新的前缀来修正一个在Blowfish实现上的安全风险。可以参考<a href="https://www.php.net/security/crypt_blowfish.php" class="link external">» this document</a>来了解关于这个修复的更多信息。总而言之，开发者如果仅针对
    PHP 5.3.7及之后版本进行开发，那应该使用 “$2y$” 而非 “$2a$” </span>
-   <span class="simpara"> **`CRYPT_SHA256`** - SHA-256 算法使用一个以
    $5$ 开头的 16 字符字符串盐值进行散列。如果盐值字符串以
    “rounds=\<N\>$” 开头，N
    的数字值将被用来指定散列循环的执行次数，这点很像 Blowfish 算法的
    cost 参数。默认的循环次数是 5000，最小是 1000，最大是
    999,999,999。超出这个范围的 N 将会被转换为最接近的值。 </span>
-   <span class="simpara"> **`CRYPT_SHA512`** - SHA-512 算法使用一个以
    $6$ 开头的 16 字符字符串盐值进行散列。如果盐值字符串以
    “rounds=\<N\>$” 开头，N
    的数字值将被用来指定散列循环的执行次数，这点很像 Blowfish 算法的
    cost 参数。默认的循环次数是 5000，最小是 1000，最大是
    999,999,999。超出这个范围的 N 将会被转换为最接近的值。 </span>

> **Note**:
>
> 从 PHP 5.3.0 起，PHP
> 包含了它自己的实现，并将在系统缺乏相应算法支持的时候使用它自己的实现。

### 参数

`str`  
待散列的字符串。

**Caution**
使用 **`CRYPT_BLOWFISH`**
算法将导致`str`被裁剪为一个最长72个字符的字符串。

`salt`  
可选的盐值字符串。如果没有提供，算法行为将由不同的算法实现决定，并可能导致不可预料的结束。

### 返回值

返回散列后的字符串或一个少于 13
字符的字符串，从而保证在失败时与盐值区分开来。

**Warning**

当校验密码时，应该使用一个不容易被时间攻击的字符串比较函数来比较<span
class="function">crypt</span>的输出与之前已知的哈希。出于这个目的，PHP5.6开始提供了<span
class="function">hash\_equals</span>。

### 更新日志

| 版本   | 说明                                                                                                                                                                                                                          |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.5  | When the failure string "\*0" is given as the `salt`, "\*1" will now be returned for consistency with other crypt implementations. Prior to this version, PHP 5.6 would incorrectly return a DES hash.                        |
| 5.6.0  | Raise E\_NOTICE security warning if `salt` is omitted.                                                                                                                                                                        |
| 5.5.21 | When the failure string "\*0" is given as the `salt`, "\*1" will now be returned for consistency with other crypt implementations. Prior to this version, PHP 5.5 (and earlier branches) would incorrectly return a DES hash. |
| 5.3.7  | Added *$2x$* and *$2y$* Blowfish modes to deal with potential high-bit attacks.                                                                                                                                               |
| 5.3.2  | 基于 Ulrich Drepper 的<a href="http://people.redhat.com/drepper/SHA-crypt.txt" class="link external">» 实现</a>，新增基于 SHA-256 算法和 SHA-512 算法的 crypt。                                                               |
| 5.3.2  | 修正了 Blowfish 算法由于非法循环导致的问题，返回“失败”字符串（“\*0” 或 “\*1”）而不是转而使用 DES 算法。                                                                                                                       |
| 5.3.0  | PHP 现在包含了它自己的 MD5 Crypt 实现，包括标准 DES 算法，扩展的 DES 算法以及 Blowfish 算法。如果系统缺乏相应的实现，那么 PHP 将使用它自己的实现。                                                                            |

### 范例

**示例 \#1 <span class="function">crypt</span> 范例**

``` php
<?php
$hashed_password = crypt('mypassword'); // 自动生成盐值

/* 你应当使用 crypt() 得到的完整结果作为盐值进行密码校验，以此来避免使用不同散列算法导致的问题。（如上所述，基于标准 DES 算法的密码散列使用 2 字符盐值，但是基于 MD5 算法的散列使用 12 个字符盐值。）*/
if (hash_equals($hashed_password, crypt($user_input, $hashed_password))) {
   echo "Password verified!";
}
?>
```

**示例 \#2 利用 htpasswd 进行 <span class="function">crypt</span> 加密**

``` php
<?php
// 设置密码
$password = 'mypassword';

// 获取散列值，使用自动盐值
$hash = crypt($password);
?>
```

**示例 \#3 以不同散列类型使用 <span class="function">crypt</span>**

``` php
<?php
if (CRYPT_STD_DES == 1) {
    echo 'Standard DES: ' . crypt('rasmuslerdorf', 'rl') . "\n";
}

if (CRYPT_EXT_DES == 1) {
    echo 'Extended DES: ' . crypt('rasmuslerdorf', '_J9..rasm') . "\n";
}

if (CRYPT_MD5 == 1) {
    echo 'MD5:          ' . crypt('rasmuslerdorf', '$1$rasmusle$') . "\n";
}

if (CRYPT_BLOWFISH == 1) {
    echo 'Blowfish:     ' . crypt('rasmuslerdorf', '$2a$07$usesomesillystringforsalt$') . "\n";
}

if (CRYPT_SHA256 == 1) {
    echo 'SHA-256:      ' . crypt('rasmuslerdorf', '$5$rounds=5000$usesomesillystringforsalt$') . "\n";
}

if (CRYPT_SHA512 == 1) {
    echo 'SHA-512:      ' . crypt('rasmuslerdorf', '$6$rounds=5000$usesomesillystringforsalt$') . "\n";
}
?>
```

以上例程的输出类似于：

    Standard DES: rl.3StKT.4T8M
    Extended DES: _J9..rasmBYk8r9AiWNc
    MD5:          $1$rasmusle$rISCgZzpwk3UhDidwXvin0
    Blowfish:     $2a$07$usesomesillystringfore2uDLvp1Ii2e./U9C8sBjqp8I90dH6hi
    SHA-256:      $5$rounds=5000$usesomesillystri$KqJWpanXZHKq2BOB43TSaYhEWsQ1Lr5QNyPCDH/Tp.6
    SHA-512:      $6$rounds=5000$usesomesillystri$D4IrlXatmP7rx3P3InaxBeoomnAihCKRVQP22JZ6EY47Wc6BkroIuUUBOov1i.S5KPgErtP/EN5mcO.ChWQW21

### 注释

> **Note**: <span class="simpara"> 由于 <span
> class="function">crypt</span> 使用的是单向算法，因此不存在 decrypt
> 函数。 </span>

### 参见

-   <span class="function">hash\_equals</span>
-   <span class="function">password\_hash</span>
-   <span class="function">md5</span>
-   <a href="/ref/mcrypt.html" class="link">Mcrypt</a> 扩展
-   更多关于 crypt 函数的信息，请阅读 Unix man 页面

echo
====

输出一个或多个字符串

### 说明

<span class="type">void</span> <span class="methodname">echo</span> (
<span class="methodparam"><span class="type">string</span>
`$arg1`</span> \[, <span class="methodparam"><span
class="type">string</span> `$...`</span> \] )

输出所有参数。不会换行。

<span class="function">echo</span> 不是一个函数（它是一个语言结构），
因此你不一定要使用小括号来指明参数，单引号，双引号都可以。 <span
class="function">echo</span> （不像其他语言构造）不表现得像一个函数，
所以不能总是使用一个函数的上下文。 另外，如果你想给<span
class="function">echo</span> 传递多个参数， 那么就不能使用小括号。

<span class="function">echo</span>
也有一个快捷用法，你可以在打开标记前直接用一个等号。在 PHP 5.4.0
之前，必须在php.ini 里面启用
<a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tag</a>
才有效。

``` php
I have <?=$foo?> foo.
```

和 *print* 最主要的不同之处是， *echo* 接受参数列表，并且没有返回值。

### 参数

`arg1`  
要输出的参数

`...`  

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">echo</span> 例子**

``` php
<?php
echo "Hello World";

echo "This spans
multiple lines. The newlines will be
output as well";

echo "This spans\nmultiple lines. The newlines will be\noutput as well.";

echo "Escaping characters is done \"Like this\".";

// You can use variables inside of an echo statement
$foo = "foobar";
$bar = "barbaz";

echo "foo is $foo"; // foo is foobar

// You can also use arrays
$baz = array("value" => "foo");

echo "this is {$baz['value']} !"; // this is foo !

// Using single quotes will print the variable name, not the value
echo 'foo is $foo'; // foo is $foo

// If you are not using any other characters, you can just echo variables
echo $foo;          // foobar
echo $foo,$bar;     // foobarbarbaz

// Strings can either be passed individually as multiple arguments or
// concatenated together and passed as a single argument
echo 'This ', 'string ', 'was ', 'made ', 'with multiple parameters.', chr(10);
echo 'This ' . 'string ' . 'was ' . 'made ' . 'with concatenation.' . "\n";

echo <<<END
This uses the "here document" syntax to output
multiple lines with $variable interpolation. Note
that the here document terminator must appear on a
line with just a semicolon. no extra whitespace!
END;

// Because echo does not behave like a function, the following code is invalid.
($some_var) ? echo 'true' : echo 'false';

// However, the following examples will work:
($some_var) ? print 'true' : print 'false'; // print is also a construct, but
                                            // it behaves like a function, so
                                            // it may be used in this context.
echo $some_var ? 'true': 'false'; // changing the statement around
?>
```

### 注释

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

**小贴士**

相对 <span class="function">echo</span>
中拼接字符串而言，传递多个参数比较好，考虑到了 PHP
中连接运算符（“.”）的优先级。 传入多个参数，不需要圆括号保证优先级：

``` php
<?php
echo "Sum: ", 1 + 2;
echo "Hello ", isset($name) ? $name : "John Doe", "!";
```

如果是拼接的，相对于加号和三目元算符，连接运算符（“.”）具有更高优先级。为了正确性，必须使用圆括号：

``` php
<?php
echo 'Sum: ' . (1 + 2);
echo 'Hello ' . (isset($name) ? $name : 'John Doe') . '!';
```

### 参见

-   <span class="function">print</span>
-   <span class="function">printf</span>
-   <span class="function">flush</span>
-   <a href="/language/types/string.html#language.types.string.syntax.heredoc" class="link">Heredoc 语法</a>

explode
=======

使用一个字符串分割另一个字符串

### 说明

<span class="type">array</span> <span class="methodname">explode</span>
( <span class="methodparam"><span class="type">string</span>
`$delimiter`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`</span> \] )

此函数返回由字符串组成的数组，每个元素都是 `string`
的一个子串，它们被字符串 `delimiter` 作为边界点分割出来。

### 参数

`delimiter`  
边界上的分隔字符。

`string`  
输入的字符串。

`limit`  
如果设置了 `limit` 参数并且是正数，则返回的数组包含最多 `limit`
个元素，而最后那个元素将包含 `string` 的剩余部分。

如果 `limit` 参数是负数，则返回除了最后的 -`limit` 个元素外的所有元素。

如果 `limit` 是 0，则会被当做 1。

由于历史原因，虽然 <span class="function">implode</span>
可以接收两种参数顺序，但是 <span class="function">explode</span>
不行。你必须保证 `separator` 参数在 `string` 参数之前才行。

### 返回值

此函数返回由字符串组成的 <span class="type">array</span>，每个元素都是
`string` 的一个子串，它们被字符串 `delimiter` 作为边界点分割出来。

如果 `delimiter` 为空字符串（""），<span class="function">explode</span>
将返回 **`FALSE`**。 如果 `delimiter` 所包含的值在 `string`
中找不到，并且使用了负数的 `limit` ， 那么会返回空的 <span
class="type">array</span>， 否则返回包含 `string` 单个元素的数组。

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 5.1.0 | 支持负数的 `limit` |
| 4.0.1 | 增加了参数 `limit` |

### 范例

**示例 \#1 <span class="function">explode</span> 例子**

``` php
<?php
// 示例 1
$pizza  = "piece1 piece2 piece3 piece4 piece5 piece6";
$pieces = explode(" ", $pizza);
echo $pieces[0]; // piece1
echo $pieces[1]; // piece2

// 示例 2
$data = "foo:*:1023:1000::/home/foo:/bin/sh";
list($user, $pass, $uid, $gid, $gecos, $home, $shell) = explode(":", $data);
echo $user; // foo
echo $pass; // *

?>
```

**示例 \#2 <span class="function">explode</span> return examples**

``` php
<?php
/* A string that doesn't contain the delimiter will simply return a one-length array of the original string. */
$input1 = "hello";
$input2 = "hello,there";
var_dump( explode( ',', $input1 ) );
var_dump( explode( ',', $input2 ) );

?>
```

以上例程会输出：

    array(1)
    (
        [0] => string(5) "hello"
    )
    array(2)
    (
        [0] => string(5) "hello"
        [1] => string(5) "there"
    )

**示例 \#3 `limit` 参数的例子**

``` php
<?php
$str = 'one|two|three|four';

// 正数的 limit
print_r(explode('|', $str, 2));

// 负数的 limit（自 PHP 5.1 起）
print_r(explode('|', $str, -1));
?>
```

以上例程会输出：

    Array
    (
        [0] => one
        [1] => two|three|four
    )
    Array
    (
        [0] => one
        [1] => two
        [2] => three
    )

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">preg\_split</span>
-   <span class="function">str\_split</span>
-   <span class="function">mb\_split</span>
-   <span class="function">str\_word\_count</span>
-   <span class="function">strtok</span>
-   <span class="function">implode</span>

fprintf
=======

将格式化后的字符串写入到流

### 说明

<span class="type">int</span> <span class="methodname">fprintf</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$args`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\]\] )

写入一个根据 `format` 格式化后的字符串到 由 `handle` 句柄打开的流中。

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

`format`  
参见 <span class="function">sprintf</span> 中对 `format` 的描述。

`args`  

`...`  

### 返回值

返回写入的字符串长度。

### 范例

**示例 \#1 <span class="function">fprintf</span>: zero-padded integers**

``` php
<?php
if (!($fp = fopen('date.txt', 'w'))) {
    return;
}

fprintf($fp, "%04d-%02d-%02d", $year, $month, $day);
// will write the formatted ISO date to date.txt
?>
```

**示例 \#2 <span class="function">fprintf</span>: formatting currency**

``` php
<?php
if (!($fp = fopen('currency.txt', 'w'))) {
    return;
}

$money1 = 68.75;
$money2 = 54.35;
$money = $money1 + $money2;
// echo $money will output "123.1";
$len = fprintf($fp, '%01.2f', $money);
// will write "123.10" to currency.txt

echo "wrote $len bytes to currency.txt";
// use the return value of fprintf to determine how many bytes we wrote
?>
```

### 参见

-   <span class="function">printf</span>
-   <span class="function">sprintf</span>
-   <span class="function">sscanf</span>
-   <span class="function">fscanf</span>
-   <span class="function">vsprintf</span>
-   <span class="function">number\_format</span>

get\_html\_translation\_table
=============================

返回使用 <span class="function">htmlspecialchars</span> 和 <span
class="function">htmlentities</span> 后的转换表

### 说明

<span class="type">array</span> <span
class="methodname">get\_html\_translation\_table</span> (\[ <span
class="methodparam"><span class="type">int</span> `$table`<span
class="initializer"> = HTML\_SPECIALCHARS</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = ENT\_COMPAT \| ENT\_HTML401</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> = 'UTF-8'</span></span> \]\]\] )

<span class="function">get\_html\_translation\_table</span> 将返回 <span
class="function">htmlspecialchars</span> 和 <span
class="function">htmlentities</span> 处理后的转换表。

> **Note**:
>
> 特殊字符可以使用多种转换方式。 例如： *"* 可以被转换成 *&quot;*,
> *&\#34;* 或者 *&\#x22*. <span
> class="function">get\_html\_translation\_table</span>
> 返回其中最常用的。

### 参数

`table`  
有两个新的常量 (**`HTML_ENTITIES`**, **`HTML_SPECIALCHARS`**)
允许你指定你想要的表。

`flags`  
A bitmask of one or more of the following flags, which specify which
quotes the table will contain as well as which document type the table
is for. The default is *ENT\_COMPAT \| ENT\_HTML401*.

| Constant Name      | Description                                                                  |
|--------------------|------------------------------------------------------------------------------|
| **`ENT_COMPAT`**   | Table will contain entities for double-quotes, but not for single-quotes.    |
| **`ENT_QUOTES`**   | Table will contain entities for both double and single quotes.               |
| **`ENT_NOQUOTES`** | Table will neither contain entities for single quotes nor for double quotes. |
| **`ENT_HTML401`**  | Table for HTML 4.01.                                                         |
| **`ENT_XML1`**     | Table for XML 1.                                                             |
| **`ENT_XHTML`**    | Table for XHTML.                                                             |
| **`ENT_HTML5`**    | Table for HTML 5.                                                            |

`encoding`  
Encoding to use. If omitted, the default value for this argument is
ISO-8859-1 in versions of PHP prior to 5.4.0, and UTF-8 from PHP 5.4.0
onwards.

支持以下字符集：

| 字符集      | 别名                         | 描述                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISO-8859-1  | ISO8859-1                    | 西欧，Latin-1                                                                                                                                                                                                                                                                                             |
| ISO-8859-5  | ISO8859-5                    | Little used cyrillic charset (Latin/Cyrillic).                                                                                                                                                                                                                                                            |
| ISO-8859-15 | ISO8859-15                   | 西欧，Latin-9。增加欧元符号，法语和芬兰语字母在 Latin-1(ISO-8859-1) 中缺失。                                                                                                                                                                                                                              |
| UTF-8       |                              | ASCII 兼容的多字节 8 位 Unicode。                                                                                                                                                                                                                                                                         |
| cp866       | ibm866, 866                  | DOS 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                   |
| cp1251      | Windows-1251, win-1251, 1251 | Windows 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                               |
| cp1252      | Windows-1252, 1252           | Windows 特有的西欧编码。                                                                                                                                                                                                                                                                                  |
| KOI8-R      | koi8-ru, koi8r               | 俄语。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                                   |
| BIG5        | 950                          | 繁体中文，主要用于中国台湾省。                                                                                                                                                                                                                                                                            |
| GB2312      | 936                          | 简体中文，中国国家标准字符集。                                                                                                                                                                                                                                                                            |
| BIG5-HKSCS  |                              | 繁体中文，附带香港扩展的 Big5 字符集。                                                                                                                                                                                                                                                                    |
| Shift\_JIS  | SJIS, 932                    | 日语                                                                                                                                                                                                                                                                                                      |
| EUC-JP      | EUCJP                        | 日语                                                                                                                                                                                                                                                                                                      |
| MacRoman    |                              | Mac OS 使用的字符串。                                                                                                                                                                                                                                                                                     |
| *''*        |                              | An empty string activates detection from script encoding (Zend multibyte), <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> and current locale (see <span class="function">nl\_langinfo</span> and <span class="function">setlocale</span>), in this order. Not recommended. |

> **Note**: <span class="simpara">
> 其他字符集没有认可。将会使用默认编码并抛出异常。 </span>

### 返回值

将转换表作为一个数组返回。

### 更新日志

| 版本  | 说明                                                                                             |
|-------|--------------------------------------------------------------------------------------------------|
| 5.4.0 | The default value for the `encoding` parameter was changed to UTF-8.                             |
| 5.4.0 | The constants **`ENT_HTML401`**, **`ENT_XML1`**, **`ENT_XHTML`** and **`ENT_HTML5`** were added. |
| 5.3.4 | The `encoding` parameter was added.                                                              |

### 范例

**示例 \#1 Translation Table Example**

``` php
<?php
var_dump(get_html_translation_table(HTML_ENTITIES, ENT_QUOTES | ENT_HTML5));
?>
```

以上例程的输出类似于：

    array(1510) {
      ["
    "]=>
      string(9) "&NewLine;"
      ["!"]=>
      string(6) "&excl;"
      ["""]=>
      string(6) "&quot;"
      ["#"]=>
      string(5) "&num;"
      ["$"]=>
      string(8) "&dollar;"
      ["%"]=>
      string(8) "&percnt;"
      ["&"]=>
      string(5) "&amp;"
      ["'"]=>
      string(6) "&apos;"
      // ...
    }

### 参见

-   <span class="function">htmlspecialchars</span>
-   <span class="function">htmlentities</span>
-   <span class="function">html\_entity\_decode</span>

hebrev
======

将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew）

### 说明

<span class="type">string</span> <span class="methodname">hebrev</span>
( <span class="methodparam"><span class="type">string</span>
`$hebrew_text`</span> \[, <span class="methodparam"><span
class="type">int</span> `$max_chars_per_line`<span class="initializer">
= 0</span></span> \] )

将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew）

函数将会尝试避免破坏单词。

### 参数

`hebrew_text`  
逻辑顺序希伯来文字符串。

`max_chars_per_line`  
可选参数，表示每行可返回的最多字符数。

### 返回值

返回视觉顺序字符串。

### 参见

-   <span class="function">hebrevc</span>

hebrevc
=======

将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew），并且转换换行符

### 说明

<span class="type">string</span> <span class="methodname">hebrevc</span>
( <span class="methodparam"><span class="type">string</span>
`$hebrew_text`</span> \[, <span class="methodparam"><span
class="type">int</span> `$max_chars_per_line`<span class="initializer">
= 0</span></span> \] )

本函数与<span class="function">hebrev</span> 一样，唯一的区别是
本函数会额外将换行符(\\n)转换为"\<br\>\\n"。

函数将会尝试避免破坏单词。

### 参数

`hebrew_text`  
逻辑顺序希伯来文字符串。

`max_chars_per_line`  
可选参数，表示每行可返回的最多字符数。

### 返回值

返回视觉顺序字符串。

### 参见

-   <span class="function">hebrev</span>

hex2bin
=======

转换十六进制字符串为二进制字符串

### 说明

<span class="type">string</span> <span class="methodname">hex2bin</span>
( <span class="methodparam"><span class="type">string</span>
`$data`</span> )

转换十六进制字符串为二进制字符串。

**Caution**

这个函数*不是* 转换十六进制数字为二进制数字。这种转换可以使用<span
class="function">base\_convert</span> 函数。

### 参数

`data`  
十六进制表示的数据

### 返回值

返回给定数据的二进制表示 或者在失败时返回 **`FALSE`**。

### 错误／异常

如果输入的十六进制字符串是奇数长数或者无效的十六进制字符串将会抛出
**`E_WARNING`** 级别的错误。

### 更新日志

| 版本  | 说明                                                                                          |
|-------|-----------------------------------------------------------------------------------------------|
| 5.5.1 | 如果输入的字符串是无效的十六进制字符串则抛出一个警告，                                        |
| 5.4.4 | 如果输入的字符串有多余将抛出异常。 PHP 5.4.0 起字符串将被静默地接受，但是最后的字节会被截断。 |

### 范例

**示例 \#1 <span class="function">hex2bin</span> 例子**

``` php
<?php
$hex = hex2bin("6578616d706c65206865782064617461");
var_dump($hex);
?>
```

以上例程的输出类似于：

    string(16) "example hex data"

### 参见

-   <span class="function">bin2hex</span>
-   <span class="function">unpack</span>

html\_entity\_decode
====================

Convert HTML entities to their corresponding characters

### 说明

<span class="type">string</span> <span
class="methodname">html\_entity\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = ENT\_COMPAT \|
ENT\_HTML401</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
ini\_get("default\_charset")</span></span> \]\] )

<span class="function">html\_entity\_decode</span> is the opposite of
<span class="function">htmlentities</span> in that it converts HTML
entities in the `string` to their corresponding characters.

More precisely, this function decodes all the entities (including all
numeric entities) that a) are necessarily valid for the chosen document
type — i.e., for XML, this function does not decode named entities that
might be defined in some DTD — and b) whose character or characters are
in the coded character set associated with the chosen encoding and are
permitted in the chosen document type. All other entities are left as
is.

### 参数

`string`  
The input string.

`flags`  
A bitmask of one or more of the following flags, which specify how to
handle quotes and which document type to use. The default is
*ENT\_COMPAT \| ENT\_HTML401*.

| Constant Name      | Description                                               |
|--------------------|-----------------------------------------------------------|
| **`ENT_COMPAT`**   | Will convert double-quotes and leave single-quotes alone. |
| **`ENT_QUOTES`**   | Will convert both double and single quotes.               |
| **`ENT_NOQUOTES`** | Will leave both double and single quotes unconverted.     |
| **`ENT_HTML401`**  | Handle code as HTML 4.01.                                 |
| **`ENT_XML1`**     | Handle code as XML 1.                                     |
| **`ENT_XHTML`**    | Handle code as XHTML.                                     |
| **`ENT_HTML5`**    | Handle code as HTML 5.                                    |

`encoding`  
An optional argument defining the encoding used when converting
characters.

If omitted, the default value of the `encoding` varies depending on the
PHP version in use. In PHP 5.6 and later, the
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
configuration option is used as the default value. PHP 5.4 and 5.5 will
use *UTF-8* as the default. Earlier versions of PHP use *ISO-8859-1*.

Although this argument is technically optional, you are highly
encouraged to specify the correct value for your code if you are using
PHP 5.5 or earlier, or if your
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
configuration option may be set incorrectly for the given input.

支持以下字符集：

| 字符集      | 别名                         | 描述                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISO-8859-1  | ISO8859-1                    | 西欧，Latin-1                                                                                                                                                                                                                                                                                             |
| ISO-8859-5  | ISO8859-5                    | Little used cyrillic charset (Latin/Cyrillic).                                                                                                                                                                                                                                                            |
| ISO-8859-15 | ISO8859-15                   | 西欧，Latin-9。增加欧元符号，法语和芬兰语字母在 Latin-1(ISO-8859-1) 中缺失。                                                                                                                                                                                                                              |
| UTF-8       |                              | ASCII 兼容的多字节 8 位 Unicode。                                                                                                                                                                                                                                                                         |
| cp866       | ibm866, 866                  | DOS 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                   |
| cp1251      | Windows-1251, win-1251, 1251 | Windows 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                               |
| cp1252      | Windows-1252, 1252           | Windows 特有的西欧编码。                                                                                                                                                                                                                                                                                  |
| KOI8-R      | koi8-ru, koi8r               | 俄语。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                                   |
| BIG5        | 950                          | 繁体中文，主要用于中国台湾省。                                                                                                                                                                                                                                                                            |
| GB2312      | 936                          | 简体中文，中国国家标准字符集。                                                                                                                                                                                                                                                                            |
| BIG5-HKSCS  |                              | 繁体中文，附带香港扩展的 Big5 字符集。                                                                                                                                                                                                                                                                    |
| Shift\_JIS  | SJIS, 932                    | 日语                                                                                                                                                                                                                                                                                                      |
| EUC-JP      | EUCJP                        | 日语                                                                                                                                                                                                                                                                                                      |
| MacRoman    |                              | Mac OS 使用的字符串。                                                                                                                                                                                                                                                                                     |
| *''*        |                              | An empty string activates detection from script encoding (Zend multibyte), <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> and current locale (see <span class="function">nl\_langinfo</span> and <span class="function">setlocale</span>), in this order. Not recommended. |

> **Note**: <span class="simpara">
> 其他字符集没有认可。将会使用默认编码并抛出异常。 </span>

### 返回值

Returns the decoded string.

### 更新日志

| 版本  | 说明                                                                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | The default value for the `encoding` parameter was changed to be the value of the <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> configuration option. |
| 5.4.0 | Default encoding changed from ISO-8859-1 to UTF-8.                                                                                                                                    |
| 5.4.0 | The constants **`ENT_HTML401`**, **`ENT_XML1`**, **`ENT_XHTML`** and **`ENT_HTML5`** were added.                                                                                      |

### 范例

**示例 \#1 Decoding HTML entities**

``` php
<?php
$orig = "I'll \"walk\" the <b>dog</b> now";

$a = htmlentities($orig);

$b = html_entity_decode($a);

echo $a; // I'll &quot;walk&quot; the &lt;b&gt;dog&lt;/b&gt; now

echo $b; // I'll "walk" the <b>dog</b> now
?>
```

### 注释

> **Note**:
>
> You might wonder why trim(html\_entity\_decode('&nbsp;')); doesn't
> reduce the string to an empty string, that's because the '&nbsp;'
> entity is not ASCII code 32 (which is stripped by <span
> class="function">trim</span>) but ASCII code 160 (0xa0) in the default
> ISO 8859-1 encoding.

### 参见

-   <span class="function">htmlentities</span>
-   <span class="function">htmlspecialchars</span>
-   <span class="function">get\_html\_translation\_table</span>
-   <span class="function">urldecode</span>

htmlentities
============

将字符转换为 HTML 转义字符

### 说明

<span class="type">string</span> <span
class="methodname">htmlentities</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = ENT\_COMPAT \| ENT\_HTML401</span></span> \[,
<span class="methodparam"><span class="type">string</span>
`$encoding`<span class="initializer"> =
ini\_get("default\_charset")</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$double_encode`<span
class="initializer"> = true</span></span> \]\]\] )

本函数各方面都和 <span class="function">htmlspecialchars</span> 一样，
除了 <span class="function">htmlentities</span> 会转换所有具有 HTML
实体的字符。

如果要解码（反向操作），可以使用 <span
class="function">html\_entity\_decode</span>。

### 参数

`string`  
输入字符。

`flags`  
以下一组位掩码标记，用于设置如何处理引号、无效代码序列、使用文档的类型。
默认是 *ENT\_COMPAT \| ENT\_HTML401*。

| 常量名               | 描述                                                                                                                                                                                            |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`ENT_COMPAT`**     | 会转换双引号，不转换单引号。                                                                                                                                                                    |
| **`ENT_QUOTES`**     | 既转换双引号也转换单引号。                                                                                                                                                                      |
| **`ENT_NOQUOTES`**   | 单/双引号都不转换                                                                                                                                                                               |
| **`ENT_IGNORE`**     | 静默丢弃无效的代码单元序列，而不是返回空字符串。 不建议使用此标记， 因为它<a href="http://unicode.org/reports/tr36/#Deletion_of_Noncharacters" class="link external">» 可能有安全影响</a>。     |
| **`ENT_SUBSTITUTE`** | 替换无效的代码单元序列为 Unicode 代替符（Replacement Character）， U+FFFD (UTF-8) 或者 &\#xFFFD; (其他)，而不是返回空字符串。                                                                   |
| **`ENT_DISALLOWED`** | 为文档的无效代码点替换为 Unicode 代替符（Replacement Character）： U+FFFD (UTF-8)，或 &\#xFFFD;（其他），而不是把它们留在原处。 比如以下情况下就很有用：要保证 XML 文档嵌入额外内容时格式合法。 |
| **`ENT_HTML401`**    | 以 HTML 4.01 处理代码。                                                                                                                                                                         |
| **`ENT_XML1`**       | 以 XML 1 处理代码。                                                                                                                                                                             |
| **`ENT_XHTML`**      | 以 XHTML 处理代码。                                                                                                                                                                             |
| **`ENT_HTML5`**      | 以 HTML 5 处理代码。                                                                                                                                                                            |

`encoding`  
An optional argument defining the encoding used when converting
characters.

If omitted, the default value of the `encoding` varies depending on the
PHP version in use. In PHP 5.6 and later, the
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
configuration option is used as the default value. PHP 5.4 and 5.5 will
use *UTF-8* as the default. Earlier versions of PHP use *ISO-8859-1*.

Although this argument is technically optional, you are highly
encouraged to specify the correct value for your code if you are using
PHP 5.5 or earlier, or if your
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
configuration option may be set incorrectly for the given input.

支持以下字符集：

| 字符集      | 别名                         | 描述                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISO-8859-1  | ISO8859-1                    | 西欧，Latin-1                                                                                                                                                                                                                                                                                             |
| ISO-8859-5  | ISO8859-5                    | Little used cyrillic charset (Latin/Cyrillic).                                                                                                                                                                                                                                                            |
| ISO-8859-15 | ISO8859-15                   | 西欧，Latin-9。增加欧元符号，法语和芬兰语字母在 Latin-1(ISO-8859-1) 中缺失。                                                                                                                                                                                                                              |
| UTF-8       |                              | ASCII 兼容的多字节 8 位 Unicode。                                                                                                                                                                                                                                                                         |
| cp866       | ibm866, 866                  | DOS 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                   |
| cp1251      | Windows-1251, win-1251, 1251 | Windows 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                               |
| cp1252      | Windows-1252, 1252           | Windows 特有的西欧编码。                                                                                                                                                                                                                                                                                  |
| KOI8-R      | koi8-ru, koi8r               | 俄语。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                                   |
| BIG5        | 950                          | 繁体中文，主要用于中国台湾省。                                                                                                                                                                                                                                                                            |
| GB2312      | 936                          | 简体中文，中国国家标准字符集。                                                                                                                                                                                                                                                                            |
| BIG5-HKSCS  |                              | 繁体中文，附带香港扩展的 Big5 字符集。                                                                                                                                                                                                                                                                    |
| Shift\_JIS  | SJIS, 932                    | 日语                                                                                                                                                                                                                                                                                                      |
| EUC-JP      | EUCJP                        | 日语                                                                                                                                                                                                                                                                                                      |
| MacRoman    |                              | Mac OS 使用的字符串。                                                                                                                                                                                                                                                                                     |
| *''*        |                              | An empty string activates detection from script encoding (Zend multibyte), <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> and current locale (see <span class="function">nl\_langinfo</span> and <span class="function">setlocale</span>), in this order. Not recommended. |

> **Note**: <span class="simpara">
> 其他字符集没有认可。将会使用默认编码并抛出异常。 </span>

`double_encode`  
关闭 `double_encode` 时，PHP 不会转换现有的 HTML 实体， 默认是全部转换。

### 返回值

返回编码后的字符。

如果指定的编码 `encoding` 里， `string` 包含了无效的代码单元序列，
没有设置 **`ENT_IGNORE`** 或者 **`ENT_SUBSTITUTE`**
标记的情况下，会返回空字符串。

### 更新日志

| 版本  | 说明                                                                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | The default value for the `encoding` parameter was changed to be the value of the <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> configuration option. |
| 5.4.0 | `encoding` 参数的默认值改成 UTF-8。                                                                                                                                                   |
| 5.4.0 | 增加常量 **`ENT_SUBSTITUTE`**、 **`ENT_DISALLOWED`**、 **`ENT_HTML401`**、 **`ENT_XML1`**、 **`ENT_XHTML`**、 **`ENT_HTML5`**。                                                       |
| 5.3.0 | 增加常量 **`ENT_IGNORE`**。                                                                                                                                                           |
| 5.2.3 | 增加参数 `double_encode`。                                                                                                                                                            |

### 范例

**示例 \#1 <span class="function">htmlentities</span> 例子**

``` php
<?php
$str = "A 'quote' is <b>bold</b>";

// 输出: A 'quote' is &lt;b&gt;bold&lt;/b&gt;
echo htmlentities($str);

// 输出: A &#039;quote&#039; is &lt;b&gt;bold&lt;/b&gt;
echo htmlentities($str, ENT_QUOTES);
?>
```

**示例 \#2 **`ENT_IGNORE`** 用法示例**

``` php
<?php
$str = "\x8F!!!";

// 输出空 string
echo htmlentities($str, ENT_QUOTES, "UTF-8");

// 输出 "!!!"
echo htmlentities($str, ENT_QUOTES | ENT_IGNORE, "UTF-8");
?>
```

### 参见

-   <span class="function">html\_entity\_decode</span>
-   <span class="function">get\_html\_translation\_table</span>
-   <span class="function">htmlspecialchars</span>
-   <span class="function">nl2br</span>
-   <span class="function">urlencode</span>

htmlspecialchars\_decode
========================

将特殊的 HTML 实体转换回普通字符

### 说明

<span class="type">string</span> <span
class="methodname">htmlspecialchars\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = ENT\_COMPAT \|
ENT\_HTML401</span></span> \] )

此函数的作用和 <span class="function">htmlspecialchars</span>
刚好相反。它将特殊的HTML实体转换回普通字符。

被转换的实体有： *&amp;*， *&quot;* （没有设置**`ENT_NOQUOTES`** 时）,
*&\#039;* （设置了 **`ENT_QUOTES`** 时）， *&lt;* 以及*&gt;*。

### 参数

`string`  
要解码的字符串

`flags`  
用下列标记中的一个或多个作为一个位掩码，来指定如何处理引号和使用哪种文档类型。默认为
*ENT\_COMPAT \| ENT\_HTML401*。

| 常量名             | 说明                       |
|--------------------|----------------------------|
| **`ENT_COMPAT`**   | 转换双引号，不转换单引号。 |
| **`ENT_QUOTES`**   | 单引号和双引号都转换。     |
| **`ENT_NOQUOTES`** | 单引号和双引号都不转换。   |
| **`ENT_HTML401`**  | 作为HTML 4.01编码处理。    |
| **`ENT_XML1`**     | 作为XML 1编码处理。        |
| **`ENT_XHTML`**    | 作为XHTML编码处理。        |
| **`ENT_HTML5`**    | 作为HTML 5编码处理。       |

### 返回值

返回解码后的字符串。

### 更新日志

| 版本  | 说明                                                                                   |
|-------|----------------------------------------------------------------------------------------|
| 5.4.0 | 增加了 **`ENT_HTML401`**、**`ENT_XML1`**、 **`ENT_XHTML`** 和 **`ENT_HTML5`** 等常量。 |

### 范例

**示例 \#1 一个 <span class="function">htmlspecialchars\_decode</span>
的例子**

``` php
<?php
$str = "<p>this -&gt; &quot;</p>\n";

echo htmlspecialchars_decode($str);

// 注意，这里的引号不会被转换
echo htmlspecialchars_decode($str, ENT_NOQUOTES);
?>
```

以上例程会输出：

    <p>this -> "</p>
    <p>this -> &quot;</p>

### 参见

-   <span class="function">htmlspecialchars</span>
-   <span class="function">html\_entity\_decode</span>
-   <span class="function">get\_html\_translation\_table</span>

htmlspecialchars
================

将特殊字符转换为 HTML 实体

### 说明

<span class="type">string</span> <span
class="methodname">htmlspecialchars</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = ENT\_COMPAT \|
ENT\_HTML401</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
ini\_get("default\_charset")</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$double_encode`<span
class="initializer"> = **`TRUE`**</span></span> \]\]\] )

某类字符在 HTML 中有特殊用处，如需保持原意，需要用 HTML 实体来表达。
本函数会返回字符转义后的表达。
如需转换子字符串中所有关联的名称实体，使用 <span
class="function">htmlentities</span> 代替本函数。

如果传入字符的字符编码和最终的文档是一致的，则用函数处理的输入适合绝大多数
HTML 文档环境。 然而，如果输入的字符编码和最终包含字符的文档是不一样的，
想要保留字符（以数字或名称实体的形式），本函数以及 <span
class="function">htmlentities</span>
（仅编码名称实体对应的子字符串）可能不够用。 这种情况可以使用 <span
class="function">mb\_encode\_numericentity</span> 代替。

| 字符         | 替换后                                                                                                                                           |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| *&* (& 符号) | *&amp;*                                                                                                                                          |
| *"* (双引号) | *&quot;*，除非设置了 **`ENT_NOQUOTES`**                                                                                                          |
| *'* (单引号) | 设置了 **`ENT_QUOTES`** 后， *&\#039;* (如果是 **`ENT_HTML401`**) ，或者 *&apos;* (如果是 **`ENT_XML1`**、 **`ENT_XHTML`** 或 **`ENT_HTML5`**)。 |
| *\<* (小于)  | *&lt;*                                                                                                                                           |
| *\>* (大于)  | *&gt;*                                                                                                                                           |

### 参数

`string`  
待转换的 <span class="type">string</span>。

`flags`  
位掩码，由以下某个或多个标记组成，设置转义处理细节、无效单元序列、文档类型。
默认是 *ENT\_COMPAT \| ENT\_HTML401*。

| 常量名称             | 描述                                                                                                                                                                                            |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`ENT_COMPAT`**     | 会转换双引号，不转换单引号。                                                                                                                                                                    |
| **`ENT_QUOTES`**     | 既转换双引号也转换单引号。                                                                                                                                                                      |
| **`ENT_NOQUOTES`**   | 单/双引号都不转换                                                                                                                                                                               |
| **`ENT_IGNORE`**     | 静默丢弃无效的代码单元序列，而不是返回空字符串。 不建议使用此标记， 因为它<a href="http://unicode.org/reports/tr36/#Deletion_of_Noncharacters" class="link external">» 可能有安全影响</a>。     |
| **`ENT_SUBSTITUTE`** | 替换无效的代码单元序列为 Unicode 代替符（Replacement Character）， U+FFFD (UTF-8) 或者 &\#xFFFD; (其他)，而不是返回空字符串。                                                                   |
| **`ENT_DISALLOWED`** | 为文档的无效代码点替换为 Unicode 代替符（Replacement Character）： U+FFFD (UTF-8)，或 &\#xFFFD;（其他），而不是把它们留在原处。 比如以下情况下就很有用：要保证 XML 文档嵌入额外内容时格式合法。 |
| **`ENT_HTML401`**    | 以 HTML 4.01 处理代码。                                                                                                                                                                         |
| **`ENT_XML1`**       | 以 XML 1 处理代码。                                                                                                                                                                             |
| **`ENT_XHTML`**      | 以 XHTML 处理代码。                                                                                                                                                                             |
| **`ENT_HTML5`**      | 以 HTML 5 处理代码。                                                                                                                                                                            |

`encoding`  
An optional argument defining the encoding used when converting
characters.

If omitted, the default value of the `encoding` varies depending on the
PHP version in use. In PHP 5.6 and later, the
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
configuration option is used as the default value. PHP 5.4 and 5.5 will
use *UTF-8* as the default. Earlier versions of PHP use *ISO-8859-1*.

Although this argument is technically optional, you are highly
encouraged to specify the correct value for your code if you are using
PHP 5.5 or earlier, or if your
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
configuration option may be set incorrectly for the given input.

本函数使用效果上，如果 `string` 对以下字符编码是有效的， *ISO-8859-1*、
*ISO-8859-15*、 *UTF-8*、 *cp866*、 *cp1251*、 *cp1252*、 *KOI8-R*
将具有相同的效果。 也就是说，在这些编码里， 受 <span
class="function">htmlspecialchars</span> 影响的字符会占据相同的位置。

支持以下字符集：

| 字符集      | 别名                         | 描述                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISO-8859-1  | ISO8859-1                    | 西欧，Latin-1                                                                                                                                                                                                                                                                                             |
| ISO-8859-5  | ISO8859-5                    | Little used cyrillic charset (Latin/Cyrillic).                                                                                                                                                                                                                                                            |
| ISO-8859-15 | ISO8859-15                   | 西欧，Latin-9。增加欧元符号，法语和芬兰语字母在 Latin-1(ISO-8859-1) 中缺失。                                                                                                                                                                                                                              |
| UTF-8       |                              | ASCII 兼容的多字节 8 位 Unicode。                                                                                                                                                                                                                                                                         |
| cp866       | ibm866, 866                  | DOS 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                   |
| cp1251      | Windows-1251, win-1251, 1251 | Windows 特有的西里尔编码。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                               |
| cp1252      | Windows-1252, 1252           | Windows 特有的西欧编码。                                                                                                                                                                                                                                                                                  |
| KOI8-R      | koi8-ru, koi8r               | 俄语。本字符集在 4.3.2 版本中得到支持。                                                                                                                                                                                                                                                                   |
| BIG5        | 950                          | 繁体中文，主要用于中国台湾省。                                                                                                                                                                                                                                                                            |
| GB2312      | 936                          | 简体中文，中国国家标准字符集。                                                                                                                                                                                                                                                                            |
| BIG5-HKSCS  |                              | 繁体中文，附带香港扩展的 Big5 字符集。                                                                                                                                                                                                                                                                    |
| Shift\_JIS  | SJIS, 932                    | 日语                                                                                                                                                                                                                                                                                                      |
| EUC-JP      | EUCJP                        | 日语                                                                                                                                                                                                                                                                                                      |
| MacRoman    |                              | Mac OS 使用的字符串。                                                                                                                                                                                                                                                                                     |
| *''*        |                              | An empty string activates detection from script encoding (Zend multibyte), <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> and current locale (see <span class="function">nl\_langinfo</span> and <span class="function">setlocale</span>), in this order. Not recommended. |

> **Note**: <span class="simpara">
> 其他字符集没有认可。将会使用默认编码并抛出异常。 </span>

`double_encode`  
关闭 `double_encode` 时，PHP 不会转换现有的 HTML 实体， 默认是全部转换。

### 返回值

转换后的 <span class="type">string</span>。

如果指定的编码 `encoding` 里， `string` 包含了无效的代码单元序列，
没有设置 **`ENT_IGNORE`** 或者 **`ENT_SUBSTITUTE`**
标记的情况下，会返回空字符串。

### 更新日志

| 版本  | 说明                                                                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.6.0 | The default value for the `encoding` parameter was changed to be the value of the <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a> configuration option. |
| 5.4.0 | `encoding` 参数的默认值改成 UTF-8。                                                                                                                                                   |
| 5.4.0 | 增加常量 **`ENT_SUBSTITUTE`**、 **`ENT_DISALLOWED`**、 **`ENT_HTML401`**、 **`ENT_XML1`**、 **`ENT_XHTML`**、 **`ENT_HTML5`**。                                                       |
| 5.3.0 | 增加常量 **`ENT_IGNORE`**。                                                                                                                                                           |
| 5.2.3 | 增加参数 `double_encode`。                                                                                                                                                            |

### 范例

**示例 \#1 <span class="function">htmlspecialchars</span> 例子**

``` php
<?php
$new = htmlspecialchars("<a href='test'>Test</a>", ENT_QUOTES);
echo $new; // &lt;a href=&#039;test&#039;&gt;Test&lt;/a&gt;
?>
```

### 注释

> **Note**:
>
> 注意，本函数不会转换以上列表以外的实体。 完整转换请参见 <span
> class="function">htmlentities</span>。

> **Note**:
>
> 如果 `flags` 的设置模糊易混淆，将遵循以下规则：
>
> -   <span class="simpara"> 当
>     **`ENT_COMPAT`**、**`ENT_QUOTES`**、**`ENT_NOQUOTES`** 都没设置，
>     默认就是 **`ENT_COMPAT`**。 </span>
> -   <span class="simpara"> 如果设置不止一个 **`ENT_COMPAT`**、
>     **`ENT_QUOTES`**、 **`ENT_NOQUOTES`** ，优先级最高的是
>     **`ENT_QUOTES`**， 其次是 **`ENT_COMPAT`**。 </span>
> -   <span class="simpara"> 当 **`ENT_HTML401`**、 **`ENT_HTML5`**、
>     **`ENT_XHTML`**、 **`ENT_XML1`** 都没设置，默认是
>     **`ENT_HTML401`**。 </span>
> -   <span class="simpara"> 如果设置不止一个 **`ENT_HTML401`**、
>     **`ENT_HTML5`**、 **`ENT_XHTML`**、 **`ENT_XML1`**，
>     优先级最高的是 **`ENT_HTML5`** 其次是 **`ENT_XHTML`** 和
>     **`ENT_HTML401`**。 </span>
> -   <span class="simpara"> 如果设置不止一个 **`ENT_DISALLOWED`**、
>     **`ENT_IGNORE`**、 **`ENT_SUBSTITUTE`**，优先级最高的是
>     **`ENT_IGNORE`**， 其次是 **`ENT_SUBSTITUTE`**。 </span>

### 参见

-   <span class="function">get\_html\_translation\_table</span>
-   <span class="function">htmlspecialchars\_decode</span>
-   <span class="function">strip\_tags</span>
-   <span class="function">htmlentities</span>
-   <span class="function">nl2br</span>

implode
=======

将一个一维数组的值转化为字符串

### 说明

<span class="type">string</span> <span class="methodname">implode</span>
( <span class="methodparam"><span class="type">string</span>
`$glue`</span> , <span class="methodparam"><span
class="type">array</span> `$pieces`</span> )

<span class="type">string</span> <span class="methodname">implode</span>
( <span class="methodparam"><span class="type">array</span>
`$pieces`</span> )

用 `glue` 将一维数组的值连接为一个字符串。

> **Note**:
>
> 因为历史原因，<span class="function">implode</span>
> 可以接收两种参数顺序，但是 <span class="function">explode</span>
> 不行。不过按文档中的顺序可以避免混淆。

### 参数

`glue`  
默认为空的字符串。

`pieces`  
你想要转换的数组。

### 返回值

返回一个字符串，其内容为由 glue 分割开的数组的值。

### 范例

**示例 \#1 <span class="function">implode</span> 例子**

``` php
<?php

$array = array('lastname', 'email', 'phone');
$comma_separated = implode(",", $array);

echo $comma_separated; // lastname,email,phone

// Empty string when using an empty array:
var_dump(implode('hello', array())); // string(0) ""

?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">explode</span>
-   <span class="function">preg\_split</span>
-   <span class="function">http\_build\_query</span>

join
====

别名 <span class="function">implode</span>

### 说明

此函数是该函数的别名： <span class="function">implode</span>.

lcfirst
=======

使一个字符串的第一个字符小写

### 说明

<span class="type">string</span> <span class="methodname">lcfirst</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> )

返回第一个字母小写的 `str` ，如果是字母的话。

需要注意的是“字母”是由当前语言区域决定的。比如，在默认的“C”区域像日耳曼语系中的元音变音a
(ä) 将不会被转换。

### 参数

`str`  
输入的字符串。

### 返回值

返回转换后的字符串。

### 范例

**示例 \#1 <span class="function">lcfirst</span> 例子：**

``` php
<?php
$foo = 'HelloWorld';
$foo = lcfirst($foo);             // helloWorld

$bar = 'HELLO WORLD!';
$bar = lcfirst($bar);             // hELLO WORLD!
$bar = lcfirst(strtoupper($bar)); // hELLO WORLD!
?>
```

### 参见

-   <span class="function">ucfirst</span>
-   <span class="function">strtolower</span>
-   <span class="function">strtoupper</span>
-   <span class="function">ucwords</span>

levenshtein
===========

计算两个字符串之间的编辑距离

### 说明

<span class="type">int</span> <span
class="methodname">levenshtein</span> ( <span class="methodparam"><span
class="type">string</span> `$str1`</span> , <span
class="methodparam"><span class="type">string</span> `$str2`</span> )

<span class="type">int</span> <span
class="methodname">levenshtein</span> ( <span class="methodparam"><span
class="type">string</span> `$str1`</span> , <span
class="methodparam"><span class="type">string</span> `$str2`</span> ,
<span class="methodparam"><span class="type">int</span>
`$cost_ins`</span> , <span class="methodparam"><span
class="type">int</span> `$cost_rep`</span> , <span
class="methodparam"><span class="type">int</span> `$cost_del`</span> )

编辑距离，是指两个字串之间，通过替换、插入、删除等操作将字符串`str1`转换成`str2`所需要操作的最少字符数量。
该算法的复杂度是 *O(m\*n)*，其中 *n* 和 *m* 分别是`str1` 和`str2`的长度
（当和算法复杂度为O(max(n,m)\*\*3)的<span
class="function">similar\_text</span>相比时，此函数还是相当不错的，尽管仍然很耗时。）。

在最简单的形式中，该函数只以两个字符串作为参数，并计算通过插入、替换和删除等操作将`str1`转换成`str2`所需要的操作次数。

第二种变体将采用三个额外的参数来定义插入、替换和删除操作的次数。此变体比第一种更加通用和适应，但效率不高。

### 参数

`str1`  
求编辑距离中的其中一个字符串

`str2`  
求编辑距离中的另一个字符串

`cost_ins`  
定义插入次数

`cost_rep`  
定义替换次数

`cost_del`  
定义删除次数

### 返回值

此函数返回两个字符串参数之间的编辑距离，如果其中一个字符串参数长度大于限制的255个字符时，返回-1。

### 范例

**示例 \#1 <span class="function">levenshtein</span> 例子：**

``` php
<?php
// 输入拼写错误的单词
$input = 'carrrot';

// 要检查的单词数组
$words  = array('apple','pineapple','banana','orange',
                'radish','carrot','pea','bean','potato');

// 目前没有找到最短距离
$shortest = -1;

// 遍历单词来找到最接近的
foreach ($words as $word) {

    // 计算输入单词与当前单词的距离
    $lev = levenshtein($input, $word);

    // 检查完全的匹配
    if ($lev == 0) {

        // 最接近的单词是这个（完全匹配）
        $closest = $word;
        $shortest = 0;

        // 退出循环；我们已经找到一个完全的匹配
        break;
    }

    // 如果此次距离比上次找到的要短
    // 或者还没找到接近的单词
    if ($lev <= $shortest || $shortest < 0) {
        // 设置最接近的匹配以及它的最短距离
        $closest  = $word;
        $shortest = $lev;
    }
}

echo "Input word: $input\n";
if ($shortest == 0) {
    echo "Exact match found: $closest\n";
} else {
    echo "Did you mean: $closest?\n";
}

?>
```

以上例程会输出：

    Input word: carrrot
    Did you mean: carrot?

### 参见

-   <span class="function">soundex</span>
-   <span class="function">similar\_text</span>
-   <span class="function">metaphone</span>

localeconv
==========

Get numeric formatting information

### 说明

<span class="type">array</span> <span
class="methodname">localeconv</span> ( <span
class="methodparam">void</span> )

Returns an associative array containing localized numeric and monetary
formatting information.

### 返回值

<span class="function">localeconv</span> returns data based upon the
current locale as set by <span class="function">setlocale</span>. The
associative array that is returned contains the following fields:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Array element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>decimal_point</td>
<td>Decimal point character</td>
</tr>
<tr class="even">
<td>thousands_sep</td>
<td>Thousands separator</td>
</tr>
<tr class="odd">
<td>grouping</td>
<td>Array containing numeric groupings</td>
</tr>
<tr class="even">
<td>int_curr_symbol</td>
<td>International currency symbol (i.e. USD)</td>
</tr>
<tr class="odd">
<td>currency_symbol</td>
<td>Local currency symbol (i.e. $)</td>
</tr>
<tr class="even">
<td>mon_decimal_point</td>
<td>Monetary decimal point character</td>
</tr>
<tr class="odd">
<td>mon_thousands_sep</td>
<td>Monetary thousands separator</td>
</tr>
<tr class="even">
<td>mon_grouping</td>
<td>Array containing monetary groupings</td>
</tr>
<tr class="odd">
<td>positive_sign</td>
<td>Sign for positive values</td>
</tr>
<tr class="even">
<td>negative_sign</td>
<td>Sign for negative values</td>
</tr>
<tr class="odd">
<td>int_frac_digits</td>
<td>International fractional digits</td>
</tr>
<tr class="even">
<td>frac_digits</td>
<td>Local fractional digits</td>
</tr>
<tr class="odd">
<td>p_cs_precedes</td>
<td><strong><code>TRUE</code></strong> if currency_symbol precedes a positive value, <strong><code>FALSE</code></strong> if it succeeds one</td>
</tr>
<tr class="even">
<td>p_sep_by_space</td>
<td><strong><code>TRUE</code></strong> if a space separates currency_symbol from a positive value, <strong><code>FALSE</code></strong> otherwise</td>
</tr>
<tr class="odd">
<td>n_cs_precedes</td>
<td><strong><code>TRUE</code></strong> if currency_symbol precedes a negative value, <strong><code>FALSE</code></strong> if it succeeds one</td>
</tr>
<tr class="even">
<td>n_sep_by_space</td>
<td><strong><code>TRUE</code></strong> if a space separates currency_symbol from a negative value, <strong><code>FALSE</code></strong> otherwise</td>
</tr>
<tr class="odd">
<td>p_sign_posn</td>
<td><ul>
<li>0 - Parentheses surround the quantity and currency_symbol</li>
<li>1 - The sign string precedes the quantity and currency_symbol</li>
<li>2 - The sign string succeeds the quantity and currency_symbol</li>
<li>3 - The sign string immediately precedes the currency_symbol</li>
<li>4 - The sign string immediately succeeds the currency_symbol</li>
</ul></td>
</tr>
<tr class="even">
<td>n_sign_posn</td>
<td><ul>
<li>0 - Parentheses surround the quantity and currency_symbol</li>
<li>1 - The sign string precedes the quantity and currency_symbol</li>
<li>2 - The sign string succeeds the quantity and currency_symbol</li>
<li>3 - The sign string immediately precedes the currency_symbol</li>
<li>4 - The sign string immediately succeeds the currency_symbol</li>
</ul></td>
</tr>
</tbody>
</table>

The *p\_sign\_posn*, and *n\_sign\_posn* contain a string of formatting
options. Each number representing one of the above listed conditions.

The grouping fields contain arrays that define the way numbers should be
grouped. For example, the monetary grouping field for the nl\_NL locale
(in UTF-8 mode with the euro sign), would contain a 2 item array with
the values 3 and 3. The higher the index in the array, the farther left
the grouping is. If an array element is equal to **`CHAR_MAX`**, no
further grouping is done. If an array element is equal to 0, the
previous element should be used.

### 范例

**示例 \#1 <span class="function">localeconv</span> example**

``` php
<?php
if (false !== setlocale(LC_ALL, 'nl_NL.UTF-8@euro')) {
    $locale_info = localeconv();
    print_r($locale_info);
}
?>
```

以上例程会输出：

    Array
    (
        [decimal_point] => .
        [thousands_sep] =>
        [int_curr_symbol] => EUR
        [currency_symbol] => €
        [mon_decimal_point] => ,
        [mon_thousands_sep] =>
        [positive_sign] =>
        [negative_sign] => -
        [int_frac_digits] => 2
        [frac_digits] => 2
        [p_cs_precedes] => 1
        [p_sep_by_space] => 1
        [n_cs_precedes] => 1
        [n_sep_by_space] => 1
        [p_sign_posn] => 1
        [n_sign_posn] => 2
        [grouping] => Array
            (
            )

        [mon_grouping] => Array
            (
                [0] => 3
                [1] => 3
            )

    )

### 参见

-   <span class="function">setlocale</span>

ltrim
=====

删除字符串开头的空白字符（或其他字符）

### 说明

<span class="type">string</span> <span class="methodname">ltrim</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$character_mask`</span> \] )

删除字符串开头的空白字符（或其他字符）

### 参数

`str`  
输入的字符串。

`character_mask`  
通过参数
`character_mask`，你也可以指定想要删除的字符，简单地列出你想要删除的所有字符即可。使用*..*，可以指定字符的范围。

### 返回值

该函数返回一个删除了 `str` 最左边的空白字符的字符串。
如果不使用第二个参数， <span class="function">ltrim</span>
仅删除以下字符：

-   <span class="simpara"> " " (ASCII *32* (*0x20*))，普通空白字符。
    </span>
-   <span class="simpara"> "\\t" (ASCII *9* (*0x09*))， 制表符. </span>
-   <span class="simpara"> "\\n" (ASCII *10* (*0x0A*))，换行符。 </span>
-   <span class="simpara"> "\\r" (ASCII *13* (*0x0D*))，回车符。 </span>
-   <span class="simpara"> "\\0" (ASCII *0* (*0x00*))， *NUL*空字节符。
    </span>
-   <span class="simpara"> "\\x0B" (ASCII *11* (*0x0B*))，垂直制表符。
    </span>

### 范例

**示例 \#1 <span class="function">ltrim</span>的使用范例**

``` php
<?php

$text = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";


$trimmed = ltrim($text);
var_dump($trimmed);

$trimmed = ltrim($text, " \t.");
var_dump($trimmed);

$trimmed = ltrim($hello, "Hdle");
var_dump($trimmed);

// 删除 $binary 开头的 ASCII 控制字符
// (从 0 到 31，包括 0 和 31)
$clean = ltrim($binary, "\x00..\x1F");
var_dump($clean);

?>
```

以上例程会输出：

    string(32) "        These are a few words :) ...  "
    string(16) "    Example string
    "
    string(11) "Hello World"

    string(30) "These are a few words :) ...  "
    string(30) "These are a few words :) ...  "
    string(7) "o World"
    string(15) "Example string
    "

### 参见

-   <span class="function">trim</span>
-   <span class="function">rtrim</span>

md5\_file
=========

计算指定文件的 MD5 散列值

### 说明

<span class="type">string</span> <span
class="methodname">md5\_file</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$raw_output`<span
class="initializer"> = **`FALSE`**</span></span> \] )

使用
<a href="http://www.faqs.org/rfcs/rfc1321" class="link external">» RSA 数据安全公司的 MD5 报文算法</a>计算
`filename` 文件的 MD5 散列值并返回。该散列值为 32 字符的十六进制数字。

### 参数

`filename`  
文件名

`raw_output`  
如果被设置为 **`TRUE`**，那么报文摘要将以原始的 16 位二进制格式返回。

### 返回值

成功返回字符串，否则返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                          |
|-------|-----------------------------------------------------------------------------------------------|
| 5.1.0 | 函数改用流 API。这意味着能够配合封装器使用该函数，比如 *md5\_file('http://example.com/..')*。 |

### 范例

**示例 \#1 <span class="function">md5\_file</span> 使用范例**

``` php
<?php
$file = 'php-5.3.0alpha2-Win32-VC9-x64.zip';

echo 'MD5 file hash of ' . $file . ': ' . md5_file($file);
?>
```

### 参见

-   <span class="function">md5</span>
-   <span class="function">sha1\_file</span>
-   <span class="function">crc32</span>

md5
===

计算字符串的 MD5 散列值

**Warning**

It is not recommended to use this function to secure passwords, due to
the fast nature of this hashing algorithm. See the
<a href="/faq/passwords.html#faq.passwords.fasthash" class="link">Password Hashing FAQ</a>
for details and best practices.

### 说明

<span class="type">string</span> <span class="methodname">md5</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$raw_output`<span class="initializer"> = **`FALSE`**</span></span> \] )

使用
<a href="http://www.faqs.org/rfcs/rfc1321" class="link external">» RSA 数据安全公司的 MD5 报文算法</a>计算
`str` 的 MD5 散列值。

### 参数

`str`  
原始字符串。

`raw_output`  
如果可选的 `raw_output` 被设置为 **`TRUE`**，那么 MD5
报文摘要将以16字节长度的原始二进制格式返回。

### 返回值

以 32 字符十六进制数字形式返回散列值。

### 范例

**示例 \#1 <span class="function">md5</span> 范例**

``` php
<?php
$str = 'apple';

if (md5($str) === '1f3870be274f6c49b3e31a0c6728957f') {
    echo "Would you like a green or red apple?";
}
?>
```

### 参见

-   <span class="function">md5\_file</span>
-   <span class="function">sha1\_file</span>
-   <span class="function">crc32</span>
-   <span class="function">sha1</span>
-   <span class="function">hash</span>
-   <span class="function">crypt</span>
-   <span class="function">password\_hash</span>

metaphone
=========

Calculate the metaphone key of a string

### 说明

<span class="type">string</span> <span
class="methodname">metaphone</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">int</span> `$phonemes`<span
class="initializer"> = 0</span></span> \] )

Calculates the metaphone key of `str`.

Similar to <span class="function">soundex</span> metaphone creates the
same key for similar sounding words. It's more accurate than <span
class="function">soundex</span> as it knows the basic rules of English
pronunciation. The metaphone generated keys are of variable length.

Metaphone was developed by Lawrence Philips \<lphilips at verity dot
com\>. It is described in \["Practical Algorithms for Programmers",
Binstock & Rex, Addison Wesley, 1995\].

### 参数

`str`  
The input string.

`phonemes`  
This parameter restricts the returned metaphone key to `phonemes`
characters in length. The default value of *0* means no restriction.

### 返回值

Returns the metaphone key as a string, 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">metaphone</span> basic example**

``` php
<?php
var_dump(metaphone('programming'));
var_dump(metaphone('programmer'));
?>
```

以上例程的输出类似于：

    string(7) "PRKRMNK"
    string(6) "PRKRMR"

**示例 \#2 Using the `phonemes` parameter**

``` php
<?php
var_dump(metaphone('programming', 5));
var_dump(metaphone('programmer', 5));
?>
```

以上例程的输出类似于：

    string(5) "PRKRM"
    string(5) "PRKRM"

money\_format
=============

将数字格式化成货币字符串

### 说明

<span class="type">string</span> <span
class="methodname">money\_format</span> ( <span
class="methodparam"><span class="type">string</span> `$format`</span> ,
<span class="methodparam"><span class="type">float</span>
`$number`</span> )

<span class="function">money\_format</span> 返回格式化好的 `number`
版本。 此函数包装了 C 函数库中的 <span
class="function">strfmon</span>，不同之处是：此实现每次只能转化一个数字。

### 参数

`format`  
格式字符串由以下几部分组成：

-   单个 *%* 字符

-   可选的标记（flags）

-   可选的字段宽度

-   可选的，左侧精度

-   可选的，右侧精度

-   必选的，单个转化字符

##### 标记(Flags)

可选多个标记，分别是：

*=*<span class="replaceable">f</span>  
字符：*=*，并紧跟一个字符（单字节） <span
class="replaceable">f</span>，用于数字填充。默认的填充字符是空格。

*^*  
禁用分组字符（比如金额中的逗号。在本地区域设置 locale 中定义）。

*+* or *(*  
正负数字的格式。使用 *+*，将使用区域设置（locale）中相当于 *+* 和 *-*
的符号。 如果使用 *(*，负数将被圆括号围绕。不设置的话，默认为 *+*。

*!*  
不输出货币符号（比如 ¥）。

*-*  
有这个符号的时候，将使字段左对齐（填充到右边），默认是相反的，是右对齐的（填充到左边）。

##### 字段宽度

<span class="replaceable">w</span>  
十进制数值字符串的宽度。字段将右对齐，除非使用了 *-* 标记。默认值 0。

##### 左侧精度

*\#*<span class="replaceable">n</span>  
小数字符（比如小数点）前的最大位数 (<span
class="replaceable">n</span>)。 常用于同一列中的格式对齐。 如果位数小于
<span class="replaceable">n</span> 则使用填充字符填满。 如果实际位数大于
<span class="replaceable">n</span>，此设置将被忽略。

如果没用 *^*
标识禁用分组，分组分隔符会在添加填充字符之前插入（如果有的话）。
分组分隔符不会应用到填充字符里，哪怕填充字符是个数字。

为了保证对齐，出现在之前或者之后的字符，都会填充必要的空格，保证正负情况下长度都一样。

##### 右侧精度

*.*<span class="replaceable">p</span>  
小数点后的一段数字 (<span class="replaceable">p</span>)。 如果 <span
class="replaceable">p</span> 的值是 0（零），小数点右侧的数值将被删除。
如果不使用这个标记，默认展现取决于当前的区域设置。
小数点后指定位数的数字，四舍五入格式化。

##### 转化字符

*i*  
根据国际化区域设置中的货币格式，格式化数值。（比如，locale 是 USA：USD
1,234.56）。

*n*  
根据国际化区域设置中国家的货币格式，格式化数值。（比如，locale 是
de\_DE：EU1.234,56）。

*%*  
返回字符 *%*。

`number`  
需要格式化的数字。

### 返回值

返回格式化后的字符。格式字符串前后的字符将原封不动返回。 传入的 `number`
如果不是数字，将返回 **`NULL`** 并且产生 **`E_WARNING`**。

### 注释

> **Note**:
>
> 具有 strfmon 的系统才有 <span class="function">money\_format</span>
> 函数。 例如 Windows 不具备，所以 Windows 系统上 <span
> class="function">money\_format</span> 未定义。

> **Note**:
>
> locale 设置中， **`LC_MONETARY`** 会影响此函数的行为。
> 在使用函数前，首先要用 <span class="function">setlocale</span>
> 来设置合适的区域设置（locale）。

### 范例

**示例 \#1 <span class="function">money\_format</span> 例子**

使用不同的 locale 和格式字符串，来说明此函数的用法。

``` php
<?php

$number = 1234.56;

// 让我们打印 en_US locale 的国际化格式
setlocale(LC_MONETARY, 'en_US');
echo money_format('%i', $number) . "\n";
// USD 1,234.56

// 意大利国家的格式，带两位浮点小数`
setlocale(LC_MONETARY, 'it_IT');
echo money_format('%.2n', $number) . "\n";
// Eu 1.234,56

// 负数的使用
$number = -1234.5672;

// 美国国家的格式，使用圆括号 () 标记负数。
// 左侧精度使用十位
setlocale(LC_MONETARY, 'en_US');
echo money_format('%(#10n', $number) . "\n";
// ($        1,234.57)

// 相似的格式，添加了右侧两位小数点的精度，同时用 * 来填充
echo money_format('%=*(#10.2n', $number) . "\n";
// ($********1,234.57)

// 让我们左对齐，14位宽，左侧八位，右侧两位，不带分组字符
// de_DE 的国际化格式
setlocale(LC_MONETARY, 'de_DE');
echo money_format('%=*^-14#8.2i', 1234.56) . "\n";
// Eu 1234,56****

// 让我们在格式字符串前后，添加一些简介
setlocale(LC_MONETARY, 'en_GB');
$fmt = 'The final value is %i (after a 10%% discount)';
echo money_format($fmt, 1234.56) . "\n";
// The final value is  GBP 1,234.56 (after a 10% discount)

?>
```

### 参见

-   <span class="function">setlocale</span>
-   <span class="function">sscanf</span>
-   <span class="function">sprintf</span>
-   <span class="function">printf</span>
-   <span class="function">number\_format</span>

nl\_langinfo
============

Query language and locale information

### 说明

<span class="type">string</span> <span
class="methodname">nl\_langinfo</span> ( <span class="methodparam"><span
class="type">int</span> `$item`</span> )

<span class="function">nl\_langinfo</span> is used to access individual
elements of the locale categories. Unlike <span
class="function">localeconv</span>, which returns all of the elements,
<span class="function">nl\_langinfo</span> allows you to select any
specific element.

### 参数

`item`  
`item` may be an integer value of the element or the constant name of
the element. The following is a list of constant names for `item` that
may be used and their description. Some of these constants may not be
defined or hold no value for certain locales.

**nl\_langinfo Constants**

Constant

### 返回值

Returns the element as a string, or **`FALSE`** if `item` is not valid.

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

### 参见

-   <span class="function">setlocale</span>
-   <span class="function">localeconv</span>

nl2br
=====

在字符串所有新行之前插入 HTML 换行标记

### 说明

<span class="type">string</span> <span class="methodname">nl2br</span> (
<span class="methodparam"><span class="type">string</span>
`$string`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_xhtml`<span class="initializer"> =
**`TRUE`**</span></span> \] )

在字符串 `string` 所有新行之前插入 `'<br />'` 或 `'<br>'`，并返回。

### 参数

`string`  
输入字符串。

`is_xhtml`  
是否使用 XHTML 兼容换行符。

### 返回值

返回调整后的字符串。

### 范例

**示例 \#1 <span class="function">nl2br</span> 使用范例**

``` php
<?php
echo nl2br("foo isn't\n bar");
?>
```

以上例程会输出：

    foo isn't<br />
     bar

**示例 \#2 使用 `is_xhtml` 生成合法的 HTML 标记**

``` php
<?php
echo nl2br("Welcome\r\nThis is my HTML document", false);
?>
```

以上例程会输出：

    Welcome<br>
    This is my HTML document

**示例 \#3 各种换行分隔符**

``` php
<?php
$string = "This\r\nis\n\ra\nstring\r";
echo nl2br($string);
?>
```

以上例程会输出：

    This<br />
    is<br />
    a<br />
    string<br />

### 更新日志

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 5.3.0 | 新增可选的 `is_xhtml` 参数。在此之前，总是插入 '\<br /\>'。 |

### 参见

-   <span class="function">htmlspecialchars</span>
-   <span class="function">htmlentities</span>
-   <span class="function">wordwrap</span>
-   <span class="function">str\_replace</span>

number\_format
==============

以千位分隔符方式格式化一个数字

### 说明

<span class="type">string</span> <span
class="methodname">number\_format</span> ( <span
class="methodparam"><span class="type">float</span> `$number`</span> \[,
<span class="methodparam"><span class="type">int</span> `$decimals`<span
class="initializer"> = 0</span></span> \] )

<span class="type">string</span> <span
class="methodname">number\_format</span> ( <span
class="methodparam"><span class="type">float</span> `$number`</span> ,
<span class="methodparam"><span class="type">int</span> `$decimals`<span
class="initializer"> = 0</span></span> , <span class="methodparam"><span
class="type">string</span> `$dec_point`<span class="initializer"> =
"."</span></span> , <span class="methodparam"><span
class="type">string</span> `$thousands_sep`<span class="initializer"> =
","</span></span> )

本函数可以接受1个、2个或者4个参数（注意：不能是3个）:

如果只提供第一个参数，`number`的小数部分会被去掉
并且每个千位分隔符都是英文小写逗号","

如果提供两个参数，`number`将保留小数点后的位数到你设定的值，其余同楼上

如果提供了四个参数，`number` 将保留`decimals`个长度的小数部分,
小数点被替换为`dec_point`，千位分隔符替换为`thousands_sep`

### 参数

`number`  
你要格式化的数字

`decimals`  
要保留的小数位数

`dec_point`  
指定小数点显示的字符

`thousands_sep`  
指定千位分隔符显示的字符

### 返回值

格式化以后的 `number`.

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.4.0 | This function now supports multiple bytes in `dec_point` and `thousands_sep`. Only the first byte of each separator was used in older versions. |

### 范例

**示例 \#1 <span class="function">number\_format</span> Example**

For instance, French notation usually use two decimals, comma (',') as
decimal separator, and space (' ') as thousand separator. The following
example demonstrates various way to format a number:

``` php
<?php

$number = 1234.56;

// english notation (default)
$english_format_number = number_format($number);
// 1,235

// French notation
$nombre_format_francais = number_format($number, 2, ',', ' ');
// 1 234,56

$number = 1234.5678;

// english notation without thousands separator
$english_format_number = number_format($number, 2, '.', '');
// 1234.57

?>
```

### 更新日志

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 7.2.0 | <span class="function">number\_format</span> 现在无法返回 *-0*，之前可能返回 *-0*，因为 `number` 可能会是 *-0.01*。 |

### 参见

-   <span class="function">money\_format</span>
-   <span class="function">sprintf</span>
-   <span class="function">printf</span>
-   <span class="function">sscanf</span>

ord
===

转换字符串第一个字节为 0-255 之间的值

### 说明

<span class="type">int</span> <span class="methodname">ord</span> (
<span class="methodparam"><span class="type">string</span>
`$string`</span> )

解析 `string` 二进制值第一个字节为 0 到 255 范围的无符号整型类型。

如果字符串是 ASCII、 ISO-8859、Windows
1252之类单字节编码，就等于返回该字符在字符集编码表中的位置。
但请注意，本函数不会去检测字符串的编码，尤其是不会识别类似 UTF-8 或
UTF-16 这种多字节字符的 Unicode 代码点（code point）。

该函数是 <span class="function">chr</span> 的互补函数。

### 参数

`string`  
一个字符。

### 返回值

返回 0 - 255 的整型值。

### 范例

**示例 \#1 <span class="function">ord</span> 范例**

``` php
<?php
$str = "\n";
if (ord($str) == 10) {
    echo "The first character of \$str is a line feed.\n";
}
?>
```

**示例 \#2 检查 UTF-8 字符串的每一个字节**

``` php
<?php
declare(encoding='UTF-8');
$str = "🐘";
for ( $pos=0; $pos < strlen($str); $pos ++ ) {
 $byte = substr($str, $pos);
 echo 'Byte ' . $pos . ' of $str has value ' . ord($byte) . PHP_EOL;
}
?>
```

以上例程会输出：

  
Byte 0 of $str has value 240  
Byte 1 of $str has value 159  
Byte 2 of $str has value 144  
Byte 3 of $str has value 152  

### 参见

-   <span class="function">chr</span>
-   <a href="http://www.asciitable.com" class="link external">» ASCII 码表</a>

parse\_str
==========

将字符串解析成多个变量

### 说明

<span class="type">void</span> <span
class="methodname">parse\_str</span> ( <span class="methodparam"><span
class="type">string</span> `$encoded_string`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$result`</span> \]
)

如果 `encoded_string` 是 URL 传递入的查询字符串（query
string），则将它解析为变量并设置到当前作用域（如果提供了 `result`
则会设置到该数组里 ）。

### 参数

`encoded_string`  
输入的字符串。

`result`  
如果设置了第二个变量 `result`，
变量将会以数组元素的形式存入到这个数组，作为替代。

**Warning**
极度*不建议* 在没有 `result` 参数的情况下使用此函数，并且在 PHP 7.2
中将*废弃*不设置参数的行为。

在函数中动态设置变量会和
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
有同样的问题。

阅读「安全」中
<a href="/security/globals.html" class="link">使用 Register Globals</a>
的章节，解释了它为什么是危险的。

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                                                                                                 |
|-------|------------------------------------------------------------------------------------------------------|
| 7.2.0 | 不带第二个参数的情况下使用 <span class="function">parse\_str</span> 会产生 **`E_DEPRECATED`** 警告。 |

### 范例

**示例 \#1 <span class="function">parse\_str</span> 的使用**

``` php
<?php
$str = "first=value&arr[]=foo+bar&arr[]=baz";

// 推荐用法
parse_str($str, $output);
echo $output['first'];  // value
echo $output['arr'][0]; // foo bar
echo $output['arr'][1]; // baz

// 不建议这么用
parse_str($str);
echo $first;  // value
echo $arr[0]; // foo bar
echo $arr[1]; // baz
?>
```

由于 PHP 的变量名不能带「点」和「空格」，所以它们会被转化成下划线。
用本函数带 `result` 参数，也会应用同样规则到数组的键名。

**示例 \#2 <span class="function">parse\_str</span> 名称改写**

``` php
<?php
parse_str("My Value=Something");
echo $My_Value; // Something

parse_str("My Value=Something", $output);
echo $output['My_Value']; // Something
?>
```

### 注释

> **Note**:
>
> 所有创建的变量(或者在设置第二个参数的情况下，返回数组里的值)， 都已经
> <span class="function">urldecode</span> 了。

> **Note**:
>
> 要获取当前的 *QUERY\_STRING*，可以使用 `$_SERVER['QUERY_STRING']`
> 变量。 所以你可能想要阅读
> <a href="/language/variables/external.html" class="link">来自 PHP 之外的变量</a>这个章节。

> **Note**:
>
> 本函数受 <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
> 设置的影响， 和 `$_GET`、 `$_POST` 在 PHP 中填充变量相似， <span
> class="function">parse\_str</span> 也使用了同样的机制。

### 参见

-   <span class="function">parse\_url</span>
-   <span class="function">pathinfo</span>
-   <span class="function">http\_build\_query</span>
-   <span class="function">urldecode</span>

print
=====

输出字符串

### 说明

<span class="type">int</span> <span class="methodname">print</span> (
<span class="methodparam"><span class="type">string</span> `$arg`</span>
)

输出 `arg`。

<span class="function">print</span>
实际上不是函数（而是语言结构），所以可以不用圆括号包围参数列表。

和 *echo* 最主要的区别： *print* 仅支持一个参数，并总是返回 1。

### 参数

`arg`  
输入数据。

### 返回值

总是返回 *1*。

### 范例

**示例 \#1 <span class="function">print</span> 范例**

``` php
<?php
print("Hello World");

print "print() also works without parentheses.";

print "This spans
multiple lines. The newlines will be
output as well";

print "This spans\nmultiple lines. The newlines will be\noutput as well.";

print "escaping characters is done \"Like this\".";

// 可以在打印语句中使用变量
$foo = "foobar";
$bar = "barbaz";

print "foo is $foo"; // foo is foobar

// 也可以使用数组
$bar = array("value" => "foo");

print "this is {$bar['value']} !"; // this is foo !

// 使用单引号将打印变量名，而不是变量的值
print 'foo is $foo'; // foo is $foo

// 如果没有使用任何其他字符，可以仅打印变量
print $foo;          // foobar

print <<<END
This uses the "here document" syntax to output
multiple lines with $variable interpolation. Note
that the here document terminator must appear on a
line with just a semicolon no extra whitespace!
END;
?>
```

### 注释

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

### 参见

-   <span class="function">echo</span>
-   <span class="function">printf</span>
-   <span class="function">flush</span>
-   <a href="/language/types/string.html#language.types.string.syntax.heredoc" class="link">Heredoc syntax</a>

printf
======

输出格式化字符串

### 说明

<span class="type">int</span> <span class="methodname">printf</span> (
<span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$args`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

依据 `format` 格式参数产生输出。

### 参数

`format`  
`format` 描述信息，请参见 <span class="function">sprintf</span>。

`args`  

`...`  

### 返回值

返回输出字符串的长度。

### 参见

-   <span class="function">print</span>
-   <span class="function">sprintf</span>
-   <span class="function">vprintf</span>
-   <span class="function">sscanf</span>
-   <span class="function">fscanf</span>
-   <span class="function">flush</span>

quoted\_printable\_decode
=========================

将 quoted-printable 字符串转换为 8-bit 字符串

### 说明

<span class="type">string</span> <span
class="methodname">quoted\_printable\_decode</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> )

该函数返回 quoted-printable 解码之后的 8-bit 字符串 (参考
<a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>
的6.7章节，而不是
<a href="http://www.faqs.org/rfcs/rfc2821" class="link external">» RFC2821</a>
的4.5.2章节，so additional periods are not stripped from the beginning
of line)

该函数与 <span class="function">imap\_qprint</span>
函数十分相似，但是该函数不需要依赖 IMAP 模块。

### 参数

`str`  
输入的字符串。

### 返回值

返回的 8-bit 二进制字符串。

### 参见

-   <span class="function">quoted\_printable\_encode</span>

quoted\_printable\_encode
=========================

将 8-bit 字符串转换成 quoted-printable 字符串

### 说明

<span class="type">string</span> <span
class="methodname">quoted\_printable\_encode</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> )

返回 quoted-printable 格式的字符，该格式由
<a href="http://www.faqs.org/rfcs/rfc2045" class="link external">» RFC2045</a>
6.7.章节里制定。

该函数与 <span class="function">imap\_8bit</span>
函数十分相似，不同的是该函数不需要 IMAP 模块就能运行。

### 参数

`str`  
输入的字符串。

### 返回值

返回编码之后的字符串。

### 参见

-   <span class="function">quoted\_printable\_decode</span>
-   <span class="function">iconv\_mime\_encode</span>

quotemeta
=========

转义元字符集

### 说明

<span class="type">string</span> <span
class="methodname">quotemeta</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

返回 在下面这些特殊字符前加 反斜线(*\\*) 转义后的字符串。
这些特殊字符包含：

. \\ + \* ? \[ ^ \] ( $ )

### 参数

`str`  
输入字符串

### 返回值

返回 元字符集被转义后的 字符串，如果输入字符串`str`为空， 则返回
**`FALSE`**。

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">addslashes</span>
-   <span class="function">addcslashes</span>
-   <span class="function">htmlentities</span>
-   <span class="function">htmlspecialchars</span>
-   <span class="function">nl2br</span>
-   <span class="function">stripslashes</span>
-   <span class="function">stripcslashes</span>
-   <span class="function">ereg</span>
-   <span class="function">preg\_quote</span>

rtrim
=====

删除字符串末端的空白字符（或者其他字符）

### 说明

<span class="type">string</span> <span class="methodname">rtrim</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$character_mask`</span> \] )

该函数删除 `str` 末端的空白字符（或者其他字符）并返回。

不使用第二个参数，<span class="function">rtrim</span> 仅删除以下字符：

-   <span class="simpara"> " " (ASCII *32* (*0x20*))，普通空白符。
    </span>
-   <span class="simpara"> "\\t" (ASCII *9* (*0x09*))，制表符。 </span>
-   <span class="simpara"> "\\n" (ASCII *10* (*0x0A*))，换行符。 </span>
-   <span class="simpara"> "\\r" (ASCII *13* (*0x0D*))，回车符。 </span>
-   <span class="simpara"> "\\0" (ASCII *0* (*0x00*))，*NUL* 空字节符。
    </span>
-   <span class="simpara"> "\\x0B" (ASCII *11* (*0x0B*))，垂直制表符。
    </span>

### 参数

`str`  
输入字符串。

`character_mask`  
通过指定
`character_mask`，可以指定想要删除的字符列表。简单地列出你想要删除的全部字符。使用
*..* 格式，可以指定一个范围。

### 返回值

返回改变后的字符串。

### 范例

**示例 \#1 <span class="function">rtrim</span> 使用范例**

``` php
<?php

$text = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";

$trimmed = rtrim($text);
var_dump($trimmed);

$trimmed = rtrim($text, " \t.");
var_dump($trimmed);

$trimmed = rtrim($hello, "Hdle");
var_dump($trimmed);

// 删除 $binary 末端的 ASCII 码控制字符
// (包括 0 - 31)
$clean = rtrim($binary, "\x00..\x1F");
var_dump($clean);

?>
```

以上例程会输出：

    string(32) "        These are a few words :) ...  "
    string(16) "    Example string
    "
    string(11) "Hello World"

    string(30) "        These are a few words :) ..."
    string(26) "        These are a few words :)"
    string(9) "Hello Wor"
    string(15) "    Example string"

### 参见

-   <span class="function">trim</span>
-   <span class="function">ltrim</span>

setlocale
=========

设置地区信息

### 说明

<span class="type">string</span> <span
class="methodname">setlocale</span> ( <span class="methodparam"><span
class="type">int</span> `$category`</span> , <span
class="methodparam"><span class="type">string</span> `$locale`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$...`</span> \] )

<span class="type">string</span> <span
class="methodname">setlocale</span> ( <span class="methodparam"><span
class="type">int</span> `$category`</span> , <span
class="methodparam"><span class="type">array</span> `$locale`</span> )

设置地区信息。

### 参数

`category`  
`category` 命名常量指定的受区域设置的功能类别:

-   <span class="simpara"> **`LC_ALL`** 所有的设置 </span>
-   <span class="simpara"> **`LC_COLLATE`** 字符串比较, 详见 <span
    class="function">strcoll</span> </span>
-   <span class="simpara"> **`LC_CTYPE`** 字符串的分类与转换, 参见例子
    <span class="function">strtoupper</span> </span>
-   <span class="simpara"> **`LC_MONETARY`** 等同 <span
    class="function">localeconv</span> </span>
-   <span class="simpara"> **`LC_NUMERIC`** 对于小数点的分隔 (另请参见
    <span class="function">localeconv</span>) </span>
-   <span class="simpara"> **`LC_TIME`** 时间与格式 <span
    class="function">strftime</span> </span>
-   <span class="simpara"> **`LC_MESSAGES`** 系统响应
    (如果PHP使用*libintl*编译) </span>

`locale`  
If `locale` is **`NULL`** or the empty string *""*, the locale names
will be set from the values of environment variables with the same names
as the above categories, or from "LANG".

If `locale` is *"0"*, the locale setting is not affected, only the
current setting is returned.

If `locale` is an array or followed by additional parameters then each
array element or parameter is tried to be set as new locale until
success. This is useful if a locale is known under different names on
different systems or for providing a fallback for a possibly not
available locale.

`...`  
(可使用字符串或数组参数进行尝试直到设置成功。)

> **Note**:
>
> 在Windows中，setlocale(LC\_ALL,
> '')要从系统中的区域/语言设置(通过控制面板访问) 。

### 返回值

Returns the new current locale, or **`FALSE`** if the locale
functionality is not implemented on your platform, the specified locale
does not exist or the category name is invalid.

An invalid category name also causes a warning message. Category/locale
names can be found in
<a href="http://www.faqs.org/rfcs/rfc1766" class="link external">» RFC 1766</a>
and
<a href="http://www.loc.gov/standards/iso639-2/php/code_list.php" class="link external">» ISO 639</a>.
Different systems have different naming schemes for locales.

> **Note**:
>
> The return value of <span class="function">setlocale</span> depends on
> the system that PHP is running. It returns exactly what the system
> *setlocale* function returns.

### 更新日志

| 版本  | 说明                                                                                                                                              |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | This function now throws an **`E_DEPRECATED`** notice if a string is passed to the `category` parameter instead of one of the *LC\_\** constants. |

### 范例

**示例 \#1 <span class="function">setlocale</span> Examples**

``` php
<?php
/* Set locale to Dutch */
setlocale(LC_ALL, 'nl_NL');

/* Output: vrijdag 22 december 1978 */
echo strftime("%A %e %B %Y", mktime(0, 0, 0, 12, 22, 1978));

/* try different possible locale names for german as of PHP 4.3.0 */
$loc_de = setlocale(LC_ALL, 'de_DE@euro', 'de_DE', 'de', 'ge');
echo "Preferred locale for german on this system is '$loc_de'";
?>
```

**示例 \#2 <span class="function">setlocale</span> Examples for
Windows**

``` php
<?php
/* Set locale to Dutch */
setlocale(LC_ALL, 'nld_nld');

/* Output: vrijdag 22 december 1978 */
echo strftime("%A %d %B %Y", mktime(0, 0, 0, 12, 22, 1978));

/* try different possible locale names for german as of PHP 4.3.0 */
$loc_de = setlocale(LC_ALL, 'de_DE@euro', 'de_DE', 'deu_deu');
echo "Preferred locale for german on this system is '$loc_de'";
?>
```

### 注释

**Warning**

The locale information is maintained per process, not per thread. If you
are running PHP on a multithreaded server API like IIS or Apache on
Windows, you may experience sudden changes in locale settings while a
script is running, though the script itself never called <span
class="function">setlocale</span>. This happens due to other scripts
running in different threads of the same process at the same time,
changing the process-wide locale using <span
class="function">setlocale</span>.

**小贴士**

Windows users will find useful information about `locale` strings at
Microsoft's MSDN website. Supported language strings can be found in the
<a href="http://msdn.microsoft.com/en-us/library/39cwe7zf%28v=vs.90%29.aspx" class="link external">» language strings documentation</a>
and supported country/region strings in the
<a href="http://msdn.microsoft.com/en-us/library/cdax410z%28v=vs.90%29.aspx" class="link external">» country/region strings documentation</a>.

sha1\_file
==========

计算文件的 sha1 散列值

### 说明

<span class="type">string</span> <span
class="methodname">sha1\_file</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$raw_output`<span
class="initializer"> = **`FALSE`**</span></span> \] )

利用<a href="http://www.faqs.org/rfcs/rfc3174" class="link external">» 美国安全散列算法 1</a>，计算并返回由
`filename` 指定的文件的 sha1 散列值。该散列值是一个 40
字符长度的十六进制数字。

### 参数

`filename`  
要散列的文件的文件名。

`raw_output`  
如果被设置为 **`TRUE`**，sha1 摘要将以 20 字符长度的原始格式返回。

### 返回值

成功返回一个字符串，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">sha1\_file</span> 范例**

``` php
<?php
foreach(glob('/home/Kalle/myproject/*.php') as $ent)
{
    if(is_dir($ent))
    {
        continue;
    }

    echo $ent . ' (SHA1: ' . sha1_file($ent) . ')', PHP_EOL;
}
?>
```

### 更新日志

| 版本  | 说明                                                                                       |
|-------|--------------------------------------------------------------------------------------------|
| 5.1.0 | 改变函数以使用流 API。这意味着可以使用包装器，比如 *sha1\_file('http://example.com/..')*。 |

### 参见

-   <span class="function">sha1</span>
-   <span class="function">md5\_file</span>
-   <span class="function">crc32</span>

sha1
====

计算字符串的 sha1 散列值

**Warning**

It is not recommended to use this function to secure passwords, due to
the fast nature of this hashing algorithm. See the
<a href="/faq/passwords.html#faq.passwords.fasthash" class="link">Password Hashing FAQ</a>
for details and best practices.

### 说明

<span class="type">string</span> <span class="methodname">sha1</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$raw_output`<span class="initializer"> = false</span></span> \] )

利用<a href="http://www.faqs.org/rfcs/rfc3174" class="link external">» 美国安全散列算法 1</a>
计算字符串的 sha1 散列值。

### 参数

`str`  
输入字符串。

`raw_output`  
如果可选的 `raw_output` 参数被设置为 **`TRUE`**， 那么 sha1 摘要将以 20
字符长度的原始格式返回， 否则返回值是一个 40 字符长度的十六进制数字。

### 返回值

返回 sha1 散列值字符串。

### 范例

**示例 \#1 <span class="function">sha1</span> 范例**

``` php
<?php
$str = 'apple';

if (sha1($str) === 'd0be2dc421be4fcd0172e5afceea3970e2f3d940') {
    echo "Would you like a green or red apple?";
}
?>
```

### 参见

-   <span class="function">sha1\_file</span>
-   <span class="function">crc32</span>
-   <span class="function">md5</span>
-   <span class="function">hash</span>
-   <span class="function">crypt</span>
-   <span class="function">password\_hash</span>

similar\_text
=============

计算两个字符串的相似度

### 说明

<span class="type">int</span> <span
class="methodname">similar\_text</span> ( <span
class="methodparam"><span class="type">string</span> `$first`</span> ,
<span class="methodparam"><span class="type">string</span>
`$second`</span> \[, <span class="methodparam"><span
class="type">float</span> `&$percent`</span> \] )

两个字符串的相似程度计算依据 Programming Classics: Implementing the
World's Best Algorithms by Oliver (ISBN 0-131-00413-1)
的描述进行。注意该实现没有使用 Oliver
虚拟码中的堆栈，但是却进行了递归调用，这个做法可能会导致整个过程变慢或变快。也请注意，该算法的复杂度是
O(N\*\*3)，N 是最长字符串的长度。

### 参数

`first`  
第一个字符串。

`second`  
第二个字符串。

`percent`  
通过引用方式传递第三个参数，<span class="function">similar\_text</span>
将计算相似程度百分数。

### 返回值

返回在两个字符串中匹配字符的数目。

### 参见

-   <span class="function">levenshtein</span>
-   <span class="function">soundex</span>

soundex
=======

Calculate the soundex key of a string

### 说明

<span class="type">string</span> <span class="methodname">soundex</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> )

Calculates the soundex key of `str`.

Soundex keys have the property that words pronounced similarly produce
the same soundex key, and can thus be used to simplify searches in
databases where you know the pronunciation but not the spelling. This
soundex function returns a string 4 characters long, starting with a
letter.

This particular soundex function is one described by Donald Knuth in
"The Art Of Computer Programming, vol. 3: Sorting And Searching",
Addison-Wesley (1973), pp. 391-392.

### 参数

`str`  
The input string.

### 返回值

Returns the soundex key as a <span class="type">string</span>,
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Soundex Examples**

``` php
<?php
soundex("Euler")       == soundex("Ellery");    // E460
soundex("Gauss")       == soundex("Ghosh");     // G200
soundex("Hilbert")     == soundex("Heilbronn"); // H416
soundex("Knuth")       == soundex("Kant");      // K530
soundex("Lloyd")       == soundex("Ladd");      // L300
soundex("Lukasiewicz") == soundex("Lissajous"); // L222
?>
```

### 参见

-   <span class="function">levenshtein</span>
-   <span class="function">metaphone</span>
-   <span class="function">similar\_text</span>

sprintf
=======

Return a formatted string

### 说明

<span class="type">string</span> <span class="methodname">sprintf</span>
( <span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \] )

Returns a string produced according to the formatting string `format`.

### 参数

`format`  
The format string is composed of zero or more directives: ordinary
characters (excluding *%*) that are copied directly to the result and
*conversion specifications*, each of which results in fetching its own
parameter.

A conversion specification follows this prototype:
*%\[argnum$\]\[flags\]\[width\]\[.precision\]specifier*.

##### Argnum

An integer followed by a dollar sign *$*, to specify which number
argument to treat in the conversion.

| Flag      | 说明                                                                                                   |
|-----------|--------------------------------------------------------------------------------------------------------|
| *-*       | Left-justify within the given field width; Right justification is the default                          |
| *+*       | Prefix positive numbers with a plus sign *+*; Default only negative are prefixed with a negative sign. |
|  (space)  | Pads the result with spaces. This is the default.                                                      |
| *0*       | Only left-pads numbers with zeros. With *s* specifiers this can also right-pad with zeros.             |
| *'*(char) | Pads the result with the character (char).                                                             |

##### Width

An integer that says how many characters (minimum) this conversion
should result in.

##### Precision

A period *.* followed by an integer who's meaning depends on the
specifier:

-   <span class="simpara"> For *e*, *E*, *f* and *F* specifiers: this is
    the number of digits to be printed after the decimal point (by
    default, this is 6). </span>
-   <span class="simpara"> For *g* and *G* specifiers: this is the
    maximum number of significant digits to be printed. </span>
-   <span class="simpara"> For *s* specifier: it acts as a cutoff point,
    setting a maximum character limit to the string. </span>

> **Note**: <span class="simpara"> If the period is specified without an
> explicit value for precision, 0 is assumed. </span>

> **Note**: <span class="simpara"> Attempting to use a position
> specifier greater than **`PHP_INT_MAX`** will generate warnings.
> </span>

<table>
<caption><strong>Specifiers</strong></caption>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Specifier</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>%</em></td>
<td>A literal percent character. No argument is required.</td>
</tr>
<tr class="even">
<td><em>b</em></td>
<td>The argument is treated as an integer and presented as a binary number.</td>
</tr>
<tr class="odd">
<td><em>c</em></td>
<td>The argument is treated as an integer and presented as the character with that ASCII.</td>
</tr>
<tr class="even">
<td><em>d</em></td>
<td>The argument is treated as an integer and presented as a (signed) decimal number.</td>
</tr>
<tr class="odd">
<td><em>e</em></td>
<td>The argument is treated as scientific notation (e.g. 1.2e+2). The precision specifier stands for the number of digits after the decimal point since PHP 5.2.1. In earlier versions, it was taken as number of significant digits (one less).</td>
</tr>
<tr class="even">
<td><em>E</em></td>
<td>Like the <em>e</em> specifier but uses uppercase letter (e.g. 1.2E+2).</td>
</tr>
<tr class="odd">
<td><em>f</em></td>
<td>The argument is treated as a float and presented as a floating-point number (locale aware).</td>
</tr>
<tr class="even">
<td><em>F</em></td>
<td>The argument is treated as a float and presented as a floating-point number (non-locale aware). Available as of PHP 5.0.3.</td>
</tr>
<tr class="odd">
<td><em>g</em></td>
<td><p>General format.</p>
<p>Let P equal the precision if nonzero, 6 if the precision is omitted, or 1 if the precision is zero. Then, if a conversion with style E would have an exponent of X:</p>
<p>If P &gt; X ≥ −4, the conversion is with style f and precision P − (X + 1). Otherwise, the conversion is with style e and precision P − 1.</p></td>
</tr>
<tr class="even">
<td><em>G</em></td>
<td>Like the <em>g</em> specifier but uses <em>E</em> and <em>f</em>.</td>
</tr>
<tr class="odd">
<td><em>o</em></td>
<td>The argument is treated as an integer and presented as an octal number.</td>
</tr>
<tr class="even">
<td><em>s</em></td>
<td>The argument is treated and presented as a string.</td>
</tr>
<tr class="odd">
<td><em>u</em></td>
<td>The argument is treated as an integer and presented as an unsigned decimal number.</td>
</tr>
<tr class="even">
<td><em>x</em></td>
<td>The argument is treated as an integer and presented as a hexadecimal number (with lowercase letters).</td>
</tr>
<tr class="odd">
<td><em>X</em></td>
<td>The argument is treated as an integer and presented as a hexadecimal number (with uppercase letters).</td>
</tr>
</tbody>
</table>

**Warning**
The *c* type specifier ignores padding and width

**Warning**
Attempting to use a combination of the string and width specifiers with
character sets that require more than one byte per character may result
in unexpected results

Variables will be co-erced to a suitable type for the specifier:

| Type      | Specifiers                        |
|-----------|-----------------------------------|
| *string*  | *s*                               |
| *integer* | *d*, *u*, *c*, *o*, *x*, *X*, *b* |
| *double*  | *g*, *G*, *e*, *E*, *f*, *F*      |

`...`  

### 返回值

Returns a string produced according to the formatting string `format`,
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 Argument swapping**

The format string supports argument numbering/swapping.

``` php
<?php
$num = 5;
$location = 'tree';

$format = 'There are %d monkeys in the %s';
echo sprintf($format, $num, $location);
?>
```

以上例程会输出：

    There are 5 monkeys in the tree

However imagine we are creating a format string in a separate file,
commonly because we would like to internationalize it and we rewrite it
as:

``` php
<?php
$format = 'The %s contains %d monkeys';
echo sprintf($format, $num, $location);
?>
```

We now have a problem. The order of the placeholders in the format
string does not match the order of the arguments in the code. We would
like to leave the code as is and simply indicate in the format string
which arguments the placeholders refer to. We would write the format
string like this instead:

``` php
<?php
$format = 'The %2$s contains %1$d monkeys';
echo sprintf($format, $num, $location);
?>
```

An added benefit is that placeholders can be repeated without adding
more arguments in the code.

``` php
<?php
$format = 'The %2$s contains %1$d monkeys.
           That\'s a nice %2$s full of %1$d monkeys.';
echo sprintf($format, $num, $location);
?>
```

When using argument swapping, the *n$* *position specifier* must come
immediately after the percent sign (*%*), before any other specifiers,
as shown below.

**示例 \#2 Specifying padding character**

``` php
<?php
echo sprintf("%'.9d\n", 123);
echo sprintf("%'.09d\n", 123);
?>
```

以上例程会输出：

    ......123
    000000123

**示例 \#3 Position specifier with other specifiers**

``` php
<?php
$format = 'The %2$s contains %1$04d monkeys';
echo sprintf($format, $num, $location);
?>
```

以上例程会输出：

    The tree contains 0005 monkeys

**示例 \#4 <span class="function">sprintf</span>: zero-padded integers**

``` php
<?php
$isodate = sprintf("%04d-%02d-%02d", $year, $month, $day);
?>
```

**示例 \#5 <span class="function">sprintf</span>: formatting currency**

``` php
<?php
$money1 = 68.75;
$money2 = 54.35;
$money = $money1 + $money2;
echo $money;
echo "\n";
$formatted = sprintf("%01.2f", $money);
echo $formatted;
?>
```

以上例程会输出：

    123.1
    123.10

**示例 \#6 <span class="function">sprintf</span>: scientific notation**

``` php
<?php
$number = 362525200;

echo sprintf("%.3e", $number);
?>
```

以上例程会输出：

    3.625e+8

### 参见

-   <span class="function">printf</span>
-   <span class="function">fprintf</span>
-   <span class="function">vprintf</span>
-   <span class="function">vsprintf</span>
-   <span class="function">vfprintf</span>
-   <span class="function">sscanf</span>
-   <span class="function">fscanf</span>
-   <span class="function">number\_format</span>
-   <span class="function">date</span>

sscanf
======

根据指定格式解析输入的字符

### 说明

<span class="type">mixed</span> <span class="methodname">sscanf</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
, <span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `&$...`</span> \] )

这个函数 <span class="function">sscanf</span> 输入类似 <span
class="function">printf</span>。 <span class="function">sscanf</span>
读取字符串`str` 然后根据指定格式`format`解析, 格式的描述文档见 <span
class="function">sprintf</span>。

指定的格式字符串中的任意空白匹配输入字符串的任意空白.也就是说即使是格式字符串中的一个制表符
\\t 也能匹配输入 字符串中的一个单一空格字符

### 参数

`str`  
将要被解析的 <span class="type">字符串</span>.

`format`  
The interpreted format for 解析`str`的格式, 除了以下不同外，其余的见
<span class="function">sprintf</span>的描述文档:

-   函数不区分语言地区
-   *F*, *g*, *G* 和 *b* 不被支持.
-   *D* 表示十进制数字.
-   *i* stands for integer with base detection.
-   *n* 代表目前已经处理的字符数。
-   *s* 遇到任意空格字符时停止读取。

`...`  
可以选参数将以引用方式传入，它们的值将被设置为解析匹配的值

### 返回值

如果仅传入了两个参数给这个函数，解析后将返回一个数组，否则，如果可选参数被传入，这个函数将返回被设置了值的个数

如果`format`存在的子字符串比 `str`内可用的多, *-1* 将被返回.

### 范例

**示例 \#1 <span class="function">sscanf</span> 例子**

``` php
<?php
// getting the serial number
list($serial) = sscanf("SN/2350001", "SN/%d");
// and the date of manufacturing
$mandate = "January 01 2000";
list($month, $day, $year) = sscanf($mandate, "%s %d %d");
echo "Item $serial was manufactured on: $year-" . substr($month, 0, 3) . "-$day\n";
?>
```

If optional parameters are passed, the function will return the number
of assigned values.

**示例 \#2 <span class="function">sscanf</span> - using optional
parameters**

``` php
<?php
// get author info and generate DocBook entry
$auth = "24\tLewis Carroll";
$n = sscanf($auth, "%d\t%s %s", $id, $first, $last);
echo "<author id='$id'>
    <firstname>$first</firstname>
    <surname>$last</surname>
</author>\n";
?>
```

### 参见

-   <span class="function">fscanf</span>
-   <span class="function">printf</span>
-   <span class="function">sprintf</span>

str\_getcsv
===========

解析 CSV 字符串为一个数组

### 说明

<span class="type">array</span> <span
class="methodname">str\_getcsv</span> ( <span class="methodparam"><span
class="type">string</span> `$input`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = ","</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$enclosure`<span
class="initializer"> = '"'</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$escape`<span
class="initializer"> = "\\\\"</span></span> \]\]\] )

以 CSV 字段格式解析字符串输入，并返回包含读取字段的数组。

### 参数

`input`  
待解析的字符串。

`delimiter`  
设定字段界定符（仅单个字符）。

`enclosure`  
设定字段包裹字符（仅单个字符）。

`escape`  
设置转义字符（仅单个字符）。默认为反斜线（*\\*）。

### 返回值

返回一个包含读取到的字段的索引数组。

### 参见

-   <span class="function">fgetcsv</span>

str\_ireplace
=============

<span class="function">str\_replace</span> 的忽略大小写版本

### 说明

<span class="type">mixed</span> <span
class="methodname">str\_ireplace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$search`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$replace`</span> , <span class="methodparam"><span
class="type">mixed</span> `$subject`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$count`</span> \] )

该函数返回一个字符串或者数组。该字符串或数组是将 `subject` 中全部的
`search` 都被 `replace`
替换（忽略大小写）之后的结果。如果没有一些特殊的替换规则，你应该使用该函数替换带有
*i* 修正符的 <span class="function">preg\_replace</span> 函数。

### 参数

如果 `search` 和 `replace` 为数组，那么 <span
class="function">str\_ireplace</span> 将对 `subject`
做二者的映射替换。如果 `replace` 的值的个数少于 `search`
的个数，多余的替换将使用空字符串来进行。如果 `search` 是一个数组而
`replace` 是一个字符串，那么 `search`
中每个元素的替换将始终使用这个字符串。

如果 `search` 或 `replace` 是数组，他们的元素将从头到尾一个个处理。

`search`  
要搜索的值，就像是 *needle*。可以使用 array 来提供多个 needle。

`replace`  
`search` 的替换值。一个数组可以被用来指定多重替换。

`subject`  
要被搜索和替换的字符串或数组，就像是 *haystack*。

如果 `subject` 是一个数组，替换操作将遍历整个
`subject`，并且也将返回一个数组。

`count`  
如果被指定，它的值将被设置为替换发生的次数。

### 返回值

返回替换后的字符串或者数组。

### 范例

**示例 \#1 <span class="function">str\_ireplace</span> 范例**

``` php
<?php
$bodytag = str_ireplace("%body%", "black", "<body text=%BODY%>");
echo $bodytag; // <body text=black>
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

**Caution**

Because <span class="function">str\_ireplace</span> replaces left to
right, it might replace a previously inserted value when doing multiple
replacements. Example \#2 in the <span
class="function">str\_replace</span> documentation demonstrates how this
may affect you in practice.

### 参见

-   <span class="function">str\_replace</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">strtr</span>

str\_pad
========

使用另一个字符串填充字符串为指定长度

### 说明

<span class="type">string</span> <span
class="methodname">str\_pad</span> ( <span class="methodparam"><span
class="type">string</span> `$input`</span> , <span
class="methodparam"><span class="type">int</span> `$pad_length`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pad_string`<span class="initializer"> = " "</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pad_type`<span
class="initializer"> = STR\_PAD\_RIGHT</span></span> \]\] )

该函数返回 `input`
被从左端、右端或者同时两端被填充到制定长度后的结果。如果可选的
`pad_string` 参数没有被指定，`input` 将被空格字符填充，否则它将被
`pad_string` 填充到指定长度。

### 参数

`input`  
输入字符串。

`pad_length`  
如果 `pad_length`
的值是负数，小于或者等于输入字符串的长度，不会发生任何填充，并会返回
`input` 。

`pad_string`  
> **Note**:
>
> 如果填充字符的长度不能被 `pad_string` 整除，那么 `pad_string`
> 可能会被缩短。

`pad_type`  
可选的 `pad_type` 参数的可能值为 **`STR_PAD_RIGHT`**，**`STR_PAD_LEFT`**
或 **`STR_PAD_BOTH`**。如果没有指定 `pad_type`，则假定它是
**`STR_PAD_RIGHT`**。

### 返回值

返回填充后的字符串。

### 范例

**示例 \#1 <span class="function">str\_pad</span> 范例**

``` php
<?php
$input = "Alien";
echo str_pad($input, 10);                      // 输出 "Alien     "
echo str_pad($input, 10, "-=", STR_PAD_LEFT);  // 输出 "-=-=-Alien"
echo str_pad($input, 10, "_", STR_PAD_BOTH);   // 输出 "__Alien___"
echo str_pad($input,  6, "___");               // 输出 "Alien_"
echo str_pad($input,  3, "*");                 // 输出 "Alien"
?>
```

str\_repeat
===========

重复一个字符串

### 说明

<span class="type">string</span> <span
class="methodname">str\_repeat</span> ( <span class="methodparam"><span
class="type">string</span> `$input`</span> , <span
class="methodparam"><span class="type">int</span> `$multiplier`</span> )

返回 `input` 重复 `multiplier` 次后的结果。

### 参数

`input`  
待操作的字符串。

`multiplier`  
`input` 被重复的次数。

`multiplier` 必须大于等于 0。如果 `multiplier` 被设置为
0，函数返回空字符串。

### 返回值

返回重复后的字符串。

### 范例

**示例 \#1 <span class="function">str\_repeat</span> 范例**

``` php
<?php
echo str_repeat("-=", 10);
?>
```

以上例程会输出：

    -=-=-=-=-=-=-=-=-=-=

### 参见

-   <a href="/control-structures/for.html" class="link">for</a>
-   <span class="function">str\_pad</span>
-   <span class="function">substr\_count</span>

str\_replace
============

子字符串替换

### 说明

<span class="type">mixed</span> <span
class="methodname">str\_replace</span> ( <span class="methodparam"><span
class="type">mixed</span> `$search`</span> , <span
class="methodparam"><span class="type">mixed</span> `$replace`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$subject`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$count`</span> \] )

该函数返回一个字符串或者数组。该字符串或数组是将 `subject` 中全部的
`search` 都被 `replace` 替换之后的结果。

如果没有一些特殊的替换需求（比如正则表达式），你应该使用该函数替换 <span
class="function">ereg\_replace</span> 和 <span
class="function">preg\_replace</span>。

### 参数

如果 `search` 和 `replace` 为数组，那么 <span
class="function">str\_replace</span> 将对 `subject`
做二者的映射替换。如果 `replace` 的值的个数少于 `search`
的个数，多余的替换将使用空字符串来进行。如果 `search` 是一个数组而
`replace` 是一个字符串，那么 `search`
中每个元素的替换将始终使用这个字符串。该转换不会改变大小写。

如果 `search` 和 `replace` 都是数组，它们的值将会被依次处理。

`search`  
查找的目标值，也就是 *needle*。一个数组可以指定多个目标。

`replace`  
`search` 的替换值。一个数组可以被用来指定多重替换。

`subject`  
执行替换的数组或者字符串。也就是 *haystack*。

如果 `subject` 是一个数组，替换操作将遍历整个
`subject`，返回值也将是一个数组。

`count`  
如果被指定，它的值将被设置为替换发生的次数。

### 返回值

该函数返回替换后的数组或者字符串。

### 范例

**示例 \#1 <span class="function">str\_replace</span> 基本范例**

``` php
<?php
// 赋值: <body text='black'>
$bodytag = str_replace("%body%", "black", "<body text='%body%'>");

// 赋值: Hll Wrld f PHP
$vowels = array("a", "e", "i", "o", "u", "A", "E", "I", "O", "U");
$onlyconsonants = str_replace($vowels, "", "Hello World of PHP");

// 赋值: You should eat pizza, beer, and ice cream every day
$phrase  = "You should eat fruits, vegetables, and fiber every day.";
$healthy = array("fruits", "vegetables", "fiber");
$yummy   = array("pizza", "beer", "ice cream");

$newphrase = str_replace($healthy, $yummy, $phrase);

// 赋值: 2
$str = str_replace("ll", "", "good golly miss molly!", $count);
echo $count;
?>
```

**示例 \#2 可能的 <span class="function">str\_replace</span> 替换范例**

``` php
<?php
// 替换顺序
$str     = "Line 1\nLine 2\rLine 3\r\nLine 4\n";
$order   = array("\r\n", "\n", "\r");
$replace = '<br />';

// 首先替换 \r\n 字符，因此它们不会被两次转换
$newstr = str_replace($order, $replace, $str);

// 输出 F ，因为 A 被 B 替换，B 又被 C 替换，以此类推...
// 由于从左到右依次替换，最终 E 被 F 替换
$search  = array('A', 'B', 'C', 'D', 'E');
$replace = array('B', 'C', 'D', 'E', 'F');
$subject = 'A';
echo str_replace($search, $replace, $subject);

// 输出: apearpearle pear
// 由于上面提到的原因
$letters = array('a', 'p');
$fruit   = array('apple', 'pear');
$text    = 'a p';
$output  = str_replace($letters, $fruit, $text);
echo $output;
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

**Caution**

由于 <span class="function">str\_replace</span>
的替换时从左到右依次进行的，进行多重替换的时候可能会替换掉之前插入的值。参见该文档的范例。

> **Note**:
>
> 该函数区分大小写。使用 <span class="function">str\_ireplace</span>
> 可以进行不区分大小写的替换。

### 参见

-   <span class="function">str\_ireplace</span>
-   <span class="function">substr\_replace</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">strtr</span>

str\_rot13
==========

对字符串执行 ROT13 转换

### 说明

<span class="type">string</span> <span
class="methodname">str\_rot13</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

对 `str` 参数执行 ROT13 编码并将结果字符串返回。

ROT13 编码简单地使用字母表中后面第 13
个字母替换当前字母，同时忽略非字母表中的字符。编码和解码都使用相同的函数，传递一个编码过的字符串作为参数，将得到原始字符串。

### 参数

`str`  
输入字符串。

### 返回值

返回给定字符串的 ROT13 版本。

### 范例

**示例 \#1 <span class="function">str\_rot13</span> 范例**

``` php
<?php

echo str_rot13('PHP 4.3.0'); // CUC 4.3.0

?>
```

str\_shuffle
============

随机打乱一个字符串

### 说明

<span class="type">string</span> <span
class="methodname">str\_shuffle</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

<span class="function">str\_shuffle</span>
函数打乱一个字符串，使用任何一种可能的排序方案。

**Caution**

本函数并不会生成安全加密的值，不应用于加密用途。若需要安全加密的值，考虑使用<span
class="function">openssl\_random\_pseudo\_bytes</span>。

### 参数

`str`  
输入字符串。

### 返回值

返回打乱后的字符串。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                   |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | <a href="/migration71/incompatible.html#migration71.incompatible.rand-srand-aliases" class="link">内置的随机算法从 libc rand 函数改成了</a><a href="http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html" class="link external">» 梅森旋转演</a>伪随机数发生算法。 |

### 范例

**示例 \#1 <span class="function">str\_shuffle</span> 范例**

``` php
<?php
$str = 'abcdef';
$shuffled = str_shuffle($str);

// 输出类似于: bfdaec
echo $shuffled;
?>
```

### 参见

-   <span class="function">shuffle</span>
-   <span class="function">rand</span>

str\_split
==========

将字符串转换为数组

### 说明

<span class="type">array</span> <span
class="methodname">str\_split</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$split_length`<span
class="initializer"> = 1</span></span> \] )

将一个字符串转换为数组。

### 参数

`string`  
输入字符串。

`split_length`  
每一段的长度。

### 返回值

如果指定了可选的 `split_length` 参数，返回数组中的每个元素均为一个长度为
`split_length` 的字符块，否则每个字符块为单个字符。

如果 `split_length` 小于 1，返回 **`FALSE`**。如果 `split_length`
参数超过了 `string` 超过了字符串 `string`
的长度，整个字符串将作为数组仅有的一个元素返回。

### 范例

**示例 \#1 <span class="function">str\_split</span> 使用范例**

``` php
<?php

$str = "Hello Friend";

$arr1 = str_split($str);
$arr2 = str_split($str, 3);

print_r($arr1);
print_r($arr2);

?>
```

以上例程会输出：

    Array
    (
        [0] => H
        [1] => e
        [2] => l
        [3] => l
        [4] => o
        [5] =>
        [6] => F
        [7] => r
        [8] => i
        [9] => e
        [10] => n
        [11] => d
    )

    Array
    (
        [0] => Hel
        [1] => lo
        [2] => Fri
        [3] => end
    )

### 注释

> **Note**:
>
> 在处理多字节字符时，<span class="function">str\_split</span>
> 会按字节数转换，而非字符数。

### 参见

-   <span class="function">chunk\_split</span>
-   <span class="function">preg\_split</span>
-   <span class="function">explode</span>
-   <span class="function">count\_chars</span>
-   <span class="function">str\_word\_count</span>
-   <a href="/control-structures/for.html" class="link">for</a>

str\_word\_count
================

返回字符串中单词的使用情况

### 说明

<span class="type">mixed</span> <span
class="methodname">str\_word\_count</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$format`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$charlist`</span>
\]\] )

统计 `string` 中单词的数量。如果可选的参数 `format`
没有被指定，那么返回值是一个代表单词数量的整型数。如果指定了 `format`
参数，返回值将是一个数组，数组的内容则取决于 `format` 参数。`format`
的可能值和相应的输出结果如下所列。

对于这个函数的目的来说，单词的定义是一个与区域设置相关的字符串。这个字符串可以包含字母字符，也可以包含
"'" 和 "-" 字符（但不能以这两个字符开始）。

### 参数

`string`  
字符串。

`format`  
指定函数的返回值。当前支持的值如下：

-   <span class="simpara"> 0 - 返回单词数量 </span>
-   <span class="simpara"> 1 - 返回一个包含 `string` 中全部单词的数组
    </span>
-   <span class="simpara"> 2 - 返回关联数组。数组的键是单词在 `string`
    中出现的数值位置，数组的值是这个单词 </span>

`charlist`  
附加的字符串列表，其中的字符将被视为单词的一部分。

### 返回值

返回一个数组或整型数，这取决于 `format` 参数的选择。

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 5.1.0 | 新增 `charlist` 参数。 |

### 范例

**示例 \#1 <span class="function">str\_word\_count</span> 范例**

``` php
<?php

$str = "Hello fri3nd, you're
       looking          good today!";

print_r(str_word_count($str, 1));
print_r(str_word_count($str, 2));
print_r(str_word_count($str, 1, 'àáãç3'));

echo str_word_count($str);

?>
```

以上例程会输出：

    Array
    (
        [0] => Hello
        [1] => fri
        [2] => nd
        [3] => you're
        [4] => looking
        [5] => good
        [6] => today
    )

    Array
    (
        [0] => Hello
        [6] => fri
        [10] => nd
        [14] => you're
        [29] => looking
        [46] => good
        [51] => today
    )

    Array
    (
        [0] => Hello
        [1] => fri3nd
        [2] => you're
        [3] => looking
        [4] => good
        [5] => today
    )

    7

### 参见

-   <span class="function">explode</span>
-   <span class="function">preg\_split</span>
-   <span class="function">split</span>
-   <span class="function">count\_chars</span>
-   <span class="function">substr\_count</span>

strcasecmp
==========

二进制安全比较字符串（不区分大小写）

### 说明

<span class="type">int</span> <span class="methodname">strcasecmp</span>
( <span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> )

二进制安全比较字符串（不区分大小写）。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

### 返回值

如果 `str1` 小于 `str2` 返回 \< 0； 如果 `str1` 大于 `str2` 返回 \>
0；如果两者相等，返回 0。

### 范例

**示例 \#1 <span class="function">strcasecmp</span> 范例**

``` php
<?php
$var1 = "Hello";
$var2 = "hello";
if (strcasecmp($var1, $var2) == 0) {
    echo '$var1 is equal to $var2 in a case-insensitive string comparison';
}
?>
```

### 参见

-   <span class="function">strcmp</span>
-   <span class="function">preg\_match</span>
-   <span class="function">substr\_compare</span>
-   <span class="function">strncasecmp</span>
-   <span class="function">stristr</span>
-   <span class="function">substr</span>

strchr
======

别名 <span class="function">strstr</span>

### 说明

此函数是该函数的别名： <span class="function">strstr</span>.

strcmp
======

二进制安全字符串比较

### 说明

<span class="type">int</span> <span class="methodname">strcmp</span> (
<span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> )

注意该比较区分大小写。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

### 返回值

如果 `str1` 小于 `str2` 返回 \< 0； 如果 `str1` 大于 `str2` 返回 \>
0；如果两者相等，返回 0。

### 范例

**示例 \#1 <span class="function">strcmp</span> 例子**

``` php
<?php
$var1 = "Hello";
$var2 = "hello";
if (strcmp($var1, $var2) !== 0) {
    echo '$var1 is not equal to $var2 in a case sensitive string comparison';
}
?>
```

### 参见

-   <span class="function">strcasecmp</span>
-   <span class="function">preg\_match</span>
-   <span class="function">substr\_compare</span>
-   <span class="function">strncmp</span>
-   <span class="function">strstr</span>
-   <span class="function">substr</span>

strcoll
=======

基于区域设置的字符串比较

### 说明

<span class="type">int</span> <span class="methodname">strcoll</span> (
<span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> )

注意该比较区分大小写。和 <span class="function">strcmp</span>
不同，该函数不是二进制安全的。

<span class="function">strcoll</span>
使用当前区域设置进行比较。如果当前区域为 C 或 POSIX，该函数等同于 <span
class="function">strcmp</span>。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

### 返回值

如果 `str1` 小于 `str2` 返回 \< 0； 如果 `str1` 大于 `str2` 返回 \>
0；如果两者相等，返回 0。

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 4.2.3 | 函数在 Win32 平台可用。 |

### 参见

-   <span class="function">preg\_match</span>
-   <span class="function">strcmp</span>
-   <span class="function">strcasecmp</span>
-   <span class="function">substr</span>
-   <span class="function">stristr</span>
-   <span class="function">strncasecmp</span>
-   <span class="function">strncmp</span>
-   <span class="function">strstr</span>
-   <span class="function">setlocale</span>

strcspn
=======

获取不匹配遮罩的起始子字符串的长度

### 说明

<span class="type">int</span> <span class="methodname">strcspn</span> (
<span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> \[, <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\]\] )

返回 `str1` 中，所有字符都*不*存在于 `str2` 范围的起始子字符串的长度。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

`start`  
查找的起始位置。

`length`  
查找的长度。

### 返回值

以整型数返回子串的长度。

### 范例

**示例 \#1 <span class="function">strcspn</span> example**

``` php
<?php
$a = strcspn('abcd',  'apple');
$b = strcspn('abcd',  'banana');
$c = strcspn('hello', 'l');
$d = strcspn('hello', 'world');

var_dump($a);
var_dump($b);
var_dump($c);
var_dump($d);
?>
```

以上例程会输出：

    int(0)
    int(0)
    int(2)
    int(2)

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strspn</span>

strip\_tags
===========

从字符串中去除 HTML 和 PHP 标记

### 说明

<span class="type">string</span> <span
class="methodname">strip\_tags</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$allowable_tags`</span> \] )

该函数尝试返回给定的字符串 `str` 去除空字符、HTML 和 PHP
标记后的结果。它使用与函数 <span class="function">fgetss</span>
一样的机制去除标记。

### 参数

`str`  
输入字符串。

`allowable_tags`  
使用可选的第二个参数指定不被去除的字符列表。

> **Note**:
>
> HTML 注释和 PHP 标签也会被去除。这里是硬编码处理的，所以无法通过
> `allowable_tags` 参数进行改变。

> **Note**:
>
> In PHP 5.3.4 and later, self-closing XHTML tags are ignored and only
> non-self-closing tags should be used in `allowable_tags`. For example,
> to allow both *\<br\>* and *\<br/\>*, you should use:
>
> ``` php
> <?php
> strip_tags($input, '<br>');
> ?>
> ```

### 返回值

返回处理后的字符串。

### 更新日志

| 版本  | 说明                                                                                           |
|-------|------------------------------------------------------------------------------------------------|
| 5.3.4 | <span class="function">strip\_tags</span> ignores self-closing XHTML tags in `allowable_tags`. |
| 5.0.0 | <span class="function">strip\_tags</span> 变为二进制安全的。                                   |

### 范例

**示例 \#1 <span class="function">strip\_tags</span> 范例**

``` php
<?php
$text = '<p>Test paragraph.</p><!-- Comment --> <a href="#fragment">Other text</a>';
echo strip_tags($text);
echo "\n";

// 允许 <p> 和 <a>
echo strip_tags($text, '<p><a>');
?>
```

以上例程会输出：

    Test paragraph. Other text
    <p>Test paragraph.</p> <a href="#fragment">Other text</a>

### 注释

**Warning**

由于 <span class="function">strip\_tags</span> 无法实际验证
HTML，不完整或者破损标签将导致更多的数据被删除。

**Warning**

该函数不会修改 `allowable_tags` 参数中指定的允许标记的任何属性，包括
*style* 和 *onmouseover*
属性，用户可能会在提交的内容中恶意滥用这些属性，从而展示给其他用户。

> **Note**:
>
> 输入 HTML 标签名字如果大于 1023 字节(bytes)将会被认为是无效的，无论
> `allowable_tags` 参数是怎样的。

### 参见

-   <span class="function">htmlspecialchars</span>

stripcslashes
=============

反引用一个使用 <span class="function">addcslashes</span> 转义的字符串

### 说明

<span class="type">string</span> <span
class="methodname">stripcslashes</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> )

返回反转义后的字符串。可识别类似 C 语言的 *\\n*，*\\r*，...
八进制以及十六进制的描述。

### 参数

`str`  
需要反转义的字符串。

### 返回值

返回反转义后的字符串。

### 参见

-   <span class="function">addcslashes</span>

stripos
=======

查找字符串首次出现的位置（不区分大小写）

### 说明

<span class="type">int</span> <span class="methodname">stripos</span> (
<span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">string</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \] )

返回在<span class="type">字符串</span> `haystack` 中 `needle`
首次出现的数字位置。

与 <span class="function">strpos</span> 不同，<span
class="function">stripos</span> 不区分大小写。

### 参数

`haystack`  
在该字符串中查找。

`needle`  
注意 `needle` 可以是一个单字符或者多字符的字符串。

如果 `needle` 不是一个字符串，那么它将被转换为整型并被视为字符顺序值。

`offset`  
可选的 `offset` 参数，从字符此数量的开始位置进行搜索。
如果是负数，就从字符末尾此数量的字符数开始统计。

### 返回值

返回 needle 存在于 `haystack`
字符串开始的位置(独立于偏移量)。同时注意字符串位置起始于 0，而不是 1。

如果未发现 needle 将返回 **`FALSE`**。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本  | 说明                      |
|-------|---------------------------|
| 7.1.0 | 开始支持负数的 `offset`。 |

### 范例

**示例 \#1 <span class="function">stripos</span> 范例**

``` php
<?php
$findme    = 'a';
$mystring1 = 'xyz';
$mystring2 = 'ABC';

$pos1 = stripos($mystring1, $findme);
$pos2 = stripos($mystring2, $findme);

// 'a' 当然不在 'xyz' 中
if ($pos1 === false) {
    echo "The string '$findme' was not found in the string '$mystring1'";
}

// 注意这里使用的是 ===。简单的 == 不能像我们期望的那样工作，
// 因为 'a' 的位置是 0（第一个字符）。
if ($pos2 !== false) {
    echo "We found '$findme' in '$mystring2' at position $pos2";
}
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">mb\_stripos</span>
-   <span class="function">strpos</span>
-   <span class="function">strrpos</span>
-   <span class="function">strripos</span>
-   <span class="function">stristr</span>
-   <span class="function">substr</span>
-   <span class="function">str\_ireplace</span>

stripslashes
============

反引用一个引用字符串

### 说明

<span class="type">string</span> <span
class="methodname">stripslashes</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

反引用一个引用字符串。

> **Note**:
>
> 如果 <a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>
> 项开启，反斜线将被去除，但是两个反斜线将会被替换成一个。

一个使用范例是使用 PHP 检测
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a> 配置项的
*开启*情况（在 PHP 5.4之
前默认是开启的）并且你不需要将数据插入到一个需要转义的位置（例如数据库）。例如，你只是简单地将表单数据直接输出。

### 参数

`str`  
输入字符串。

### 返回值

返回一个去除转义反斜线后的字符串（*\\'* 转换为 *'*
等等）。双反斜线（*\\\\*）被转换为单个反斜线（*\\*）。

### 范例

**示例 \#1 <span class="function">stripslashes</span> 范例**

``` php
<?php
$str = "Is your name O\'reilly?";

// 输出: Is your name O'reilly?
echo stripslashes($str);
?>
```

> **Note**:
>
> <span class="function">stripslashes</span>
> 是非递归的。如果你想要在多维数组中使用该函数，你需要使用递归函数。

**示例 \#2 对数组使用 <span class="function">stripslashes</span>**

``` php
<?php
function stripslashes_deep($value)
{
    $value = is_array($value) ?
                array_map('stripslashes_deep', $value) :
                stripslashes($value);

    return $value;
}

// 范例
$array = array("f\\'oo", "b\\'ar", array("fo\\'o", "b\\'ar"));
$array = stripslashes_deep($array);

// 输出
print_r($array);
?>
```

以上例程会输出：

    Array
    (
        [0] => f'oo
        [1] => b'ar
        [2] => Array
            (
                [0] => fo'o
                [1] => b'ar
            )

    )

### 参见

-   <span class="function">addslashes</span>
-   <span class="function">get\_magic\_quotes\_gpc</span>

stristr
=======

<span class="function">strstr</span> 函数的忽略大小写版本

### 说明

<span class="type">string</span> <span class="methodname">stristr</span>
( <span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">mixed</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$before_needle`<span
class="initializer"> = **`FALSE`**</span></span> \] )

返回 `haystack` 字符串从 `needle` 第一次出现的位置开始到结尾的字符串。

### 参数

`haystack`  
在该字符串中查找。

`needle`  
如果 `needle` 不是一个字符串，那么它将被转换为整型并被视为字符顺序值。

`before_needle`  
若为 **`TRUE`**，<span class="function">strstr</span> 将返回 `needle` 在
`haystack` 中的位置之前的部分(不包括 needle)。

参数 `needle` 和 `haystack` 将以不区分大小写的方式对待。

### 返回值

返回匹配的子字符串。如果 `needle` 未找到，返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                     |
|-------|----------------------------------------------------------|
| 5.3.0 | 新增可选的 `before_needle` 参数。                        |
| 4.3.0 | <span class="function">stristr</span> 变为二进制安全的。 |

### 范例

**示例 \#1 <span class="function">stristr</span> 范例**

``` php
<?php
  $email = 'USER@EXAMPLE.com';
  echo stristr($email, 'e'); // 输出 ER@EXAMPLE.com
  echo stristr($email, 'e', true); // 自 PHP 5.3.0 起，输出 US
?>
```

**示例 \#2 测试字符串的存在与否**

``` php
<?php
  $string = 'Hello World!';
  if(stristr($string, 'earth') === FALSE) {
    echo '"earth" not found in string';
  }
// 输出: "earth" not found in string
?>
```

**示例 \#3 使用非字符串 needle**

``` php
<?php
  $string = 'APPLE';
  echo stristr($string, 97); // 97 = 小写字母 a
// 输出: APPLE
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strstr</span>
-   <span class="function">strrchr</span>
-   <span class="function">stripos</span>
-   <span class="function">strpbrk</span>
-   <span class="function">preg\_match</span>

strlen
======

获取字符串长度

### 说明

<span class="type">int</span> <span class="methodname">strlen</span> (
<span class="methodparam"><span class="type">string</span>
`$string`</span> )

返回给定的字符串 `string` 的长度。

### 参数

`string`  
需要计算长度的<span class="type">字符串</span>。

### 返回值

成功则返回字符串 `string` 的长度；如果 `string` 为空，则返回 0。

### 更新日志

| 版本  | 说明                                                                                                                                   |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | Prior versions treated arrays as the string *Array*, thus returning a string length of *5* and emitting an **`E_NOTICE`** level error. |

### 范例

**示例 \#1 <span class="function">strlen</span> 范例**

``` php
<?php
$str = 'abcdef';
echo strlen($str); // 6

$str = ' ab cd ';
echo strlen($str); // 7
?>
```

### 注释

> **Note**:
>
> <span class="function">strlen</span> returns the number of bytes
> rather than the number of characters in a string.

> **Note**:
>
> <span class="function">strlen</span> returns **`NULL`** when executed
> on arrays, and an **`E_WARNING`** level error is emitted.

### 参见

-   <span class="function">count</span>
-   <span class="function">mb\_strlen</span>

strnatcasecmp
=============

使用“自然顺序”算法比较字符串（不区分大小写）

### 说明

<span class="type">int</span> <span
class="methodname">strnatcasecmp</span> ( <span
class="methodparam"><span class="type">string</span> `$str1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$str2`</span> )

该函数实现了以人类习惯对数字型字符串进行排序的比较算法。除了不区分大小写，该函数的行为与
<span class="function">strnatcmp</span> 类似。更多信息，参见：Martin
Pool
的<a href="http://sourcefrog.net/projects/natsort/" class="link external">» 自然顺序的字符串比较</a>页面。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

### 返回值

与其他字符串比较函数类似，如果 `str1` 小于 `str2` 返回 \< 0； 如果
`str1` 大于 `str2` 返回 \> 0；如果两者相等，返回 0。

### 参见

-   <span class="function">preg\_match</span>
-   <span class="function">strcmp</span>
-   <span class="function">strcasecmp</span>
-   <span class="function">substr</span>
-   <span class="function">stristr</span>
-   <span class="function">strncasecmp</span>
-   <span class="function">strncmp</span>
-   <span class="function">strstr</span>
-   <span class="function">setlocale</span>

strnatcmp
=========

使用自然排序算法比较字符串

### 说明

<span class="type">int</span> <span class="methodname">strnatcmp</span>
( <span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> )

该函数实现了以人类习惯对数字型字符串进行排序的比较算法，这就是“自然顺序”。注意该比较区分大小写。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

### 返回值

与其他字符串比较函数类似，如果 `str1` 小于 `str2` 返回 \< 0； 如果
`str1` 大于 `str2` 返回 \> 0；如果两者相等，返回 0。

### 范例

下面的例子展示了该算法与计算机常规字符串比较算法（ <span
class="function">strcmp</span> 所使用的）的区别：

``` php
<?php
$arr1 = $arr2 = array("img12.png", "img10.png", "img2.png", "img1.png");
echo "Standard string comparison\n";
usort($arr1, "strcmp");
print_r($arr1);
echo "\nNatural order string comparison\n";
usort($arr2, "strnatcmp");
print_r($arr2);
?>
```

以上例程会输出：

    Standard string comparison
    Array
    (
        [0] => img1.png
        [1] => img10.png
        [2] => img12.png
        [3] => img2.png
    )

    Natural order string comparison
    Array
    (
        [0] => img1.png
        [1] => img2.png
        [2] => img10.png
        [3] => img12.png
    )

更多信息，参见：Martin Pool
的<a href="http://sourcefrog.net/projects/natsort/" class="link external">» 自然顺序的字符串比较</a>
page.

### 参见

-   <span class="function">preg\_match</span>
-   <span class="function">strcasecmp</span>
-   <span class="function">substr</span>
-   <span class="function">stristr</span>
-   <span class="function">strcmp</span>
-   <span class="function">strncmp</span>
-   <span class="function">strncasecmp</span>
-   <span class="function">strnatcasecmp</span>
-   <span class="function">strstr</span>
-   <span class="function">natsort</span>
-   <span class="function">natcasesort</span>

strncasecmp
===========

二进制安全比较字符串开头的若干个字符（不区分大小写）

### 说明

<span class="type">int</span> <span
class="methodname">strncasecmp</span> ( <span class="methodparam"><span
class="type">string</span> `$str1`</span> , <span
class="methodparam"><span class="type">string</span> `$str2`</span> ,
<span class="methodparam"><span class="type">int</span> `$len`</span> )

该函数与 <span class="function">strcasecmp</span>
类似，不同之处在于你可以指定两个字符串比较时使用的长度（即最大比较长度）。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

`len`  
最大比较长度。

### 返回值

如果 `str1` 小于 `str2` 返回 \< 0； 如果 `str1` 大于 `str2` 返回 \>
0；如果两者相等，返回 0。

### 参见

-   <span class="function">strncmp</span>
-   <span class="function">preg\_match</span>
-   <span class="function">substr\_compare</span>
-   <span class="function">strcasecmp</span>
-   <span class="function">stristr</span>
-   <span class="function">substr</span>

strncmp
=======

二进制安全比较字符串开头的若干个字符

### 说明

<span class="type">int</span> <span class="methodname">strncmp</span> (
<span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> , <span
class="methodparam"><span class="type">int</span> `$len`</span> )

该函数与 <span class="function">strcmp</span>
类似，不同之处在于你可以指定两个字符串比较时使用的长度（即最大比较长度）。

注意该比较区分大小写。

### 参数

`str1`  
第一个字符串。

`str2`  
第二个字符串。

`len`  
最大比较长度。

### 返回值

如果 `str1` 小于 `str2` 返回 \< 0； 如果 `str1` 大于 `str2` 返回 \>
0；如果两者相等，返回 0。

### 参见

-   <span class="function">strncasecmp</span>
-   <span class="function">preg\_match</span>
-   <span class="function">substr\_compare</span>
-   <span class="function">strcmp</span>
-   <span class="function">strstr</span>
-   <span class="function">substr</span>

strpbrk
=======

在字符串中查找一组字符的任何一个字符

### 说明

<span class="type">string</span> <span class="methodname">strpbrk</span>
( <span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">string</span> `$char_list`</span> )

<span class="function">strpbrk</span> 函数在 `haystack` 字符串中查找
`char_list` 中的字符。

### 参数

`haystack`  
在此字符串中查找 `char_list`。

`char_list`  
该参数区分大小写。

### 返回值

返回一个以找到的字符开始的子字符串。如果没有找到，则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">strpbrk</span> 范例**

``` php
<?php

$text = 'This is a Simple text.';

// 输出 "is is a Simple text."，因为 'i' 先被匹配
echo strpbrk($text, 'mi');

// 输出 "Simple text."，因为字符区分大小写
echo strpbrk($text, 'S');
?>
```

### 参见

-   <span class="function">strpos</span>
-   <span class="function">strstr</span>
-   <span class="function">preg\_match</span>

strpos
======

查找字符串首次出现的位置

### 说明

<span class="type">int</span> <span class="methodname">strpos</span> (
<span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">mixed</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \] )

返回 `needle` 在 `haystack` 中首次出现的数字位置。

### 参数

`haystack`  
在该字符串中进行查找。

`needle`  
如果 `needle` 不是一个字符串，那么它将被转换为整型并被视为字符的顺序值。

`offset`  
如果提供了此参数，搜索会从字符串该字符数的起始位置开始统计。
如果是负数，搜索会从字符串结尾指定字符数开始。

### 返回值

返回 needle 存在于 `haystack` 字符串起始的位置(独立于
offset)。同时注意字符串位置是从0开始，而不是从1开始的。

如果没找到 needle，将返回 **`FALSE`**。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本  | 说明                      |
|-------|---------------------------|
| 7.1.0 | 开始支持负数的 `offset`。 |

### 范例

**示例 \#1 使用 *===***

``` php
<?php
$mystring = 'abc';
$findme   = 'a';
$pos = strpos($mystring, $findme);

// 注意这里使用的是 ===。简单的 == 不能像我们期待的那样工作，
// 因为 'a' 是第 0 位置上的（第一个）字符。
if ($pos === false) {
    echo "The string '$findme' was not found in the string '$mystring'";
} else {
    echo "The string '$findme' was found in the string '$mystring'";
    echo " and exists at position $pos";
}
?>
```

**示例 \#2 使用 !==**

``` php
<?php
$mystring = 'abc';
$findme   = 'a';
$pos = strpos($mystring, $findme);

// 使用 !== 操作符。使用 != 不能像我们期待的那样工作，
// 因为 'a' 的位置是 0。语句 (0 != false) 的结果是 false。
if ($pos !== false) {
     echo "The string '$findme' was found in the string '$mystring'";
         echo " and exists at position $pos";
} else {
     echo "The string '$findme' was not found in the string '$mystring'";
}
?>
```

**示例 \#3 使用位置偏移量**

``` php
<?php
// 忽视位置偏移量之前的字符进行查找
$newstring = 'abcdef abcdef';
$pos = strpos($newstring, 'a', 1); // $pos = 7, 不是 0
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">stripos</span>
-   <span class="function">strrpos</span>
-   <span class="function">strripos</span>
-   <span class="function">strstr</span>
-   <span class="function">strpbrk</span>
-   <span class="function">substr</span>
-   <span class="function">preg\_match</span>

strrchr
=======

查找指定字符在字符串中的最后一次出现

### 说明

<span class="type">string</span> <span class="methodname">strrchr</span>
( <span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">mixed</span> `$needle`</span> )

该函数返回 `haystack` 字符串中的一部分，这部分以 `needle`
的最后出现位置开始，直到 `haystack` 末尾。

### 参数

`haystack`  
在该字符串中查找。

`needle`  
如果 `needle` 包含了不止一个字符，那么仅使用第一个字符。该行为不同于
<span class="function">strstr</span>。

如果 `needle` 不是一个字符串，那么将被转化为整型并被视为字符顺序值。

### 返回值

该函数返回字符串的一部分。如果 `needle` 未被找到，返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 4.3.0 | 该函数是二进制安全的。 |

### 范例

**示例 \#1 <span class="function">strrchr</span> 范例**

``` php
<?php
// 获取 $PATH 中不含磁盘符号的目录
$dir = substr(strrchr($PATH, ":"), 1);

// 获取最后一行内容
$text = "Line 1\nLine 2\nLine 3";
$last = substr(strrchr($text, 10), 1 );
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strstr</span>
-   <span class="function">strrpos</span>

strrev
======

反转字符串

### 说明

<span class="type">string</span> <span class="methodname">strrev</span>
( <span class="methodparam"><span class="type">string</span>
`$string`</span> )

返回 `string` 反转后的字符串。

### 参数

`string`  
待反转的原始字符串。

### 返回值

返回反转后的字符串。

### 范例

**示例 \#1 使用 <span class="function">strrev</span> 反转字符串**

``` php
<?php
echo strrev("Hello world!"); // 输出 "!dlrow olleH"
?>
```

strripos
========

计算指定字符串在目标字符串中最后一次出现的位置（不区分大小写）

### 说明

<span class="type">int</span> <span class="methodname">strripos</span> (
<span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">string</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \] )

以不区分大小写的方式查找指定字符串在目标字符串中最后一次出现的位置。与
<span class="function">strrpos</span> 不同，<span
class="function">strripos</span> 不区分大小写。

### 参数

`haystack`  
在此字符串中进行查找。

`needle`  
注意 `needle` 可以是一个单字符或者多字符的字符串。

`offset`  
参数 `offset` 可以被指定来查找字符串中任意长度的子字符串。

负数偏移量将使得查找从字符串的起始位置开始，到 `offset` 位置为止。

### 返回值

返回 needle 相对于 `haystack`
字符串的位置(和搜索的方向和偏移量无关)。同时注意字符串的起始位置为 0
而非 1。

如果 needle 未被发现，返回 **`FALSE`**。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 <span class="function">strripos</span> 简单范例**

``` php
<?php
$haystack = 'ababcd';
$needle   = 'aB';

$pos      = strripos($haystack, $needle);

if ($pos === false) {
    echo "Sorry, we did not find ($needle) in ($haystack)";
} else {
    echo "Congratulations!\n";
    echo "We found the last ($needle) in ($haystack) at position ($pos)";
}
?>
```

以上例程会输出：

       Congratulations!
       We found the last (aB) in (ababcd) at position (2)

### 参见

-   <span class="function">strpos</span>
-   <span class="function">stripos</span>
-   <span class="function">strrchr</span>
-   <span class="function">substr</span>
-   <span class="function">stristr</span>
-   <span class="function">strstr</span>

strrpos
=======

计算指定字符串在目标字符串中最后一次出现的位置

### 说明

<span class="type">int</span> <span class="methodname">strrpos</span> (
<span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">string</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \] )

返回字符串 `haystack` 中 `needle` 最后一次出现的数字位置。注意 PHP4
中，needle 只能为单个字符。如果 needle
被指定为一个字符串，那么将仅使用第一个字符。

### 参数

`haystack`  
在此字符串中进行查找。

`needle`  
如果 `needle`不是一个字符串，它将被转换为整型并被视为字符的顺序值。

`offset`  
或许会查找字符串中任意长度的子字符串。负数值将导致查找在字符串结尾处开始的计数位置处结束。

### 返回值

返回 needle 存在的位置。如果没有找到，返回 **`FALSE`**。 Also note that
string positions start at 0, and not 1.

Returns **`FALSE`** if the needle was not found.

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本  | 说明                                     |
|-------|------------------------------------------|
| 5.0.0 | 参数 `needle` 可以是一个多字符的字符串。 |
| 5.0.0 | 引入 `offset` 参数。                     |

### 范例

**示例 \#1 检查字串是否存在**

很容易将“在位置 0
处找到”和“未发现字符串”这两种情况搞错。这是检测区别的办法：

``` php
<?php

$pos = strrpos($mystring, "b");
if ($pos === false) { // 注意: 三个等号
    // 未发现...
}

?>
```

**示例 \#2 使用偏移位置进行查找**

``` php
<?php
$foo = "0123456789a123456789b123456789c";

var_dump(strrpos($foo, '7', -5));  // 从尾部第 5 个位置开始查找
                                   // 结果: int(17)

var_dump(strrpos($foo, '7', 20));  // 从第 20 个位置开始查找
                                   // 结果: int(27)

var_dump(strrpos($foo, '7', 28));  // 结果: bool(false)
?>
```

### 参见

-   <span class="function">strpos</span>
-   <span class="function">stripos</span>
-   <span class="function">strripos</span>
-   <span class="function">strrchr</span>
-   <span class="function">substr</span>

strspn
======

计算字符串中全部字符都存在于指定字符集合中的第一段子串的长度。

### 说明

<span class="type">int</span> <span class="methodname">strspn</span> (
<span class="methodparam"><span class="type">string</span>
`$subject`</span> , <span class="methodparam"><span
class="type">string</span> `$mask`</span> \[, <span
class="methodparam"><span class="type">int</span> `$start`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\]\] )

返回 `subject` 中全部字符*仅*存在于 `mask`
中的第一组连续字符(子字符串)的长度。

如果省略了 `start` 和 `length` 参数，则检查整个 `subject`
字符串；如果指定了这两个参数，则效果等同于调用 *strspn(substr($subject,
$start, $length), $mask)*（更多信息，参见
<a href="/ref/strings.html#substr" class="xref"></a> ）。

代码行：

``` php
<?php
$var = strspn("42 is the answer to the 128th question.", "1234567890");
?>
```

`$var` 将被指派为 2，因为 '42' 是 `subject` 中第一段全部字符都存在于
'1234567890' 的连续字符。

### 参数

`subject`  
待检查的字符串。

`mask`  
检查字符列表。

`start`  
`subject` 的开始检查位置。

如果 `start` 被设置并且是非负的，<span class="function">strspn</span>
将从 `subject` 的第 `start` 个位置开始检查。例如，在字符串 '*abcdef*'
中，第 *0* 个位置的字符是 '*a*'，第二个位置的字符是 '*c*'，等等。

如果 `start` 被设置并且为负数，<span class="function">strspn</span> 将从
`subject` 的尾部倒数第 `start` 个位置开始检查 `subject`。

`length`  
`subject` 中检查的长度。

如果 `length` 被设置并且为非负数，那么将从起始位置开始，检查 `subject`
的 `length` 个长度的字符。

如果 `length` 被设置并且为负数，那么将从起始位置开始，直到从 `subject`
尾部开始第 `length` 个位置，对 `subject` 进行检查。

### 返回值

返回 `str1` 中第一段全部字符都存在于 `str2` 范围的字符串的长度。

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 4.3.0 | 新增 `start` 和 `length` 参数。 |

### 范例

**示例 \#1 <span class="function">strspn</span> 范例**

``` php
<?php
echo strspn("foo", "o", 1, 2); // 打印: 2
?>
```

以上例程会输出：

    int(0)
    int(2)
    int(1)

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strcspn</span>

strstr
======

查找字符串的首次出现

### 说明

<span class="type">string</span> <span class="methodname">strstr</span>
( <span class="methodparam"><span class="type">string</span>
`$haystack`</span> , <span class="methodparam"><span
class="type">mixed</span> `$needle`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$before_needle`<span
class="initializer"> = **`FALSE`**</span></span> \] )

返回 `haystack` 字符串从 `needle` 第一次出现的位置开始到 `haystack`
结尾的字符串。

> **Note**:
>
> 该函数区分大小写。如果想要不区分大小写，请使用 <span
> class="function">stristr</span>。

> **Note**:
>
> 如果你仅仅想确定 `needle` 是否存在于 `haystack`
> 中，请使用速度更快、耗费内存更少的 <span
> class="function">strpos</span> 函数。

### 参数

`haystack`  
输入字符串。

`needle`  
如果 `needle`
不是一个字符串，那么它将被转化为整型并且作为字符的序号来使用。

`before_needle`  
若为 **`TRUE`**，<span class="function">strstr</span> 将返回 `needle` 在
`haystack` 中的位置之前的部分。

### 返回值

返回字符串的一部分或者 **`FALSE`**（如果未发现 `needle`）。

### 更新日志

| 版本  | 说明                                                    |
|-------|---------------------------------------------------------|
| 5.3.0 | 新增可选的 `before_needle` 参数。                       |
| 4.3.0 | <span class="function">strstr</span> 成为二进制安全的。 |

### 范例

**示例 \#1 <span class="function">strstr</span> 范例**

``` php
<?php
$email  = 'name@example.com';
$domain = strstr($email, '@');
echo $domain; // 打印 @example.com

$user = strstr($email, '@', true); // 从 PHP 5.3.0 起
echo $user; // 打印 name
?>
```

### 参见

-   <span class="function">preg\_match</span>
-   <span class="function">stristr</span>
-   <span class="function">strpos</span>
-   <span class="function">strrchr</span>
-   <span class="function">substr</span>

strtok
======

标记分割字符串

### 说明

<span class="type">string</span> <span class="methodname">strtok</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> , <span class="methodparam"><span
class="type">string</span> `$token`</span> )

<span class="type">string</span> <span class="methodname">strtok</span>
( <span class="methodparam"><span class="type">string</span>
`$token`</span> )

<span class="function">strtok</span> 将字符串 `str`
分割为若干子字符串，每个子字符串以 `token`
中的字符分割。这也就意味着，如果有个字符串是 "This is an example
string"，你可以使用空格字符将这句话分割成独立的单词。

注意仅第一次调用 strtok 函数时使用 string 参数。后来每次调用
strtok，都将只使用 token 参数，因为它会记住它在字符串 string
中的位置。如果要重新开始分割一个新的字符串，你需要再次使用 string 来调用
strtok 函数，以便完成初始化工作。注意可以在 token
参数中使用多个字符。字符串将被该参数中任何一个字符分割。

### 参数

`str`  
被分成若干子字符串的原始<span class="type">字符串</span>。

`token`  
分割 `str` 时使用的分界字符。

### 返回值

标记后的<span class="type">字符串</span>。

### 范例

**示例 \#1 <span class="function">strtok</span> 范例**

``` php
<?php
$string = "This is\tan example\nstring";
/* 使用制表符和换行符作为分界符 */
$tok = strtok($string, " \n\t");

while ($tok !== false) {
    echo "Word=$tok<br />";
    $tok = strtok(" \n\t");
}
?>
```

**示例 \#2 当存在空的部分时 <span class="function">strtok</span>
的反应**

``` php
<?php
$first_token  = strtok('/something', '/');
$second_token = strtok('/');
var_dump($first_token, $second_token);
?>
```

以上例程会输出：

        string(9) "something"
        bool(false)

### 注释

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 参见

-   <span class="function">split</span>
-   <span class="function">explode</span>

strtolower
==========

将字符串转化为小写

### 说明

<span class="type">string</span> <span
class="methodname">strtolower</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

将 `string` 中所有的字母字符转换为小写并返回。

注意 “字母” 与当前所在区域有关。例如，在默认的 “C” 区域，字符
umlaut-A（ä）就不会被转换。

### 参数

`string`  
输入字符串。

### 返回值

返回转换后的小写字符串。

### 范例

**示例 \#1 <span class="function">strtolower</span> 范例**

``` php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtolower($str);
echo $str; // 打印 mary had a little lamb and she loved it so
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strtoupper</span>
-   <span class="function">ucfirst</span>
-   <span class="function">ucwords</span>
-   <span class="function">mb\_strtolower</span>

strtoupper
==========

将字符串转化为大写

### 说明

<span class="type">string</span> <span
class="methodname">strtoupper</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

将 `string` 中所有的字母字符转换为大写并返回。

注意 “字母” 与当前所在区域有关。例如，在默认的 “C” 区域，字符
umlaut-a（ä）就不会被转换。

### 参数

`string`  
输入字符串。

### 返回值

返回转换后的大写字符串。

### 范例

**示例 \#1 <span class="function">strtoupper</span> 范例**

``` php
<?php
$str = "Mary Had A Little Lamb and She LOVED It So";
$str = strtoupper($str);
echo $str; // 打印 MARY HAD A LITTLE LAMB AND SHE LOVED IT SO
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strtolower</span>
-   <span class="function">ucfirst</span>
-   <span class="function">ucwords</span>
-   <span class="function">mb\_strtoupper</span>

strtr
=====

转换指定字符

### 说明

<span class="type">string</span> <span class="methodname">strtr</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
, <span class="methodparam"><span class="type">string</span>
`$from`</span> , <span class="methodparam"><span
class="type">string</span> `$to`</span> )

<span class="type">string</span> <span class="methodname">strtr</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
, <span class="methodparam"><span class="type">array</span>
`$replace_pairs`</span> )

该函数返回 `str` 的一个副本，并将在 `from` 中指定的字符转换为 `to`
中相应的字符。 比如， *$from\[$n\]*中每次的出现都会被替换为
*$to\[$n\]*，其中 *$n* 是两个参数都有效的位移(offset)。

如果 `from` 与 `to` 长度不相等，那么多余的字符部分将被忽略。 `str`
的长度将会和返回的值一样。

If given two arguments, the second should be an <span
class="type">array</span> in the form *array('from' =\> 'to', ...)*. The
return value is a <span class="type">string</span> where all the
occurrences of the array keys have been replaced by the corresponding
values. The longest keys will be tried first. Once a substring has been
replaced, its new value will not be searched again.

In this case, the keys and the values may have any length, provided that
there is no empty key; additionally, the length of the return value may
differ from that of `str`. However, this function will be the most
efficient when all the keys have the same size.

### 参数

`str`  
待转换的<span class="type">字符串</span>。

`from`  
<span class="type">字符串</span>中与将要被转换的目的字符 `to`
相对应的源字符。

`to`  
<span class="type">字符串</span>中与将要被转换的字符 `from`
相对应的目的字符。

`replace_pairs`  
参数 `replace_pairs` 可以用来取代 `to` 和 `from` 参数，因为它是以
*array('from' =\> 'to', ...)* 格式出现的数组。

### 返回值

返回转换后的<span class="type">字符串</span>。

如果 `replace_pairs` 中包含一个空<span
class="type">字符串</span>（*""*）键，那么将返回 **`FALSE`**。 If the
`str` is not a scalar then it is not typecasted into a string, instead a
warning is raised and **`NULL`** is returned.

### 范例

**示例 \#1 <span class="function">strtr</span> 范例**

``` php
<?php
$addr = strtr($addr, "äåö", "aao");
?>
```

The next example shows the behavior of <span
class="function">strtr</span> when called with only two arguments. Note
the preference of the replacements (*"h"* is not picked because there
are longer matches) and how replaced text was not searched again.

**示例 \#2 使用两个参数的 <span class="function">strtr</span> 范例**

``` php
<?php
$trans = array("hello" => "hi", "hi" => "hello");
echo strtr("hi all, I said hello", $trans);
?>
```

以上例程会输出：

    hello all, I said hi

The two modes of behavior are substantially different. With three
arguments, <span class="function">strtr</span> will replace bytes; with
two, it may replace longer substrings.

**示例 \#3 <span class="function">strtr</span> behavior comparison**

``` php
<?php
echo strtr("baab", "ab", "01"),"\n";

$trans = array("ab" => "01");
echo strtr("baab", $trans);
?>
```

以上例程会输出：

    1001
    ba01

### 参见

-   <span class="function">str\_replace</span>
-   <span class="function">preg\_replace</span>

substr\_compare
===============

二进制安全比较字符串（从偏移位置比较指定长度）

### 说明

<span class="type">int</span> <span
class="methodname">substr\_compare</span> ( <span
class="methodparam"><span class="type">string</span> `$main_str`</span>
, <span class="methodparam"><span class="type">string</span>
`$str`</span> , <span class="methodparam"><span class="type">int</span>
`$offset`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$case_insensitivity`<span class="initializer"> =
**`FALSE`**</span></span> \]\] )

<span class="function">substr\_compare</span> 从偏移位置 `offset`
开始比较 `main_str` 与 `str`，比较长度为 `length` 个字符。

### 参数

`main_str`  
待比较的第一个字符串。

`str`  
待比较的第二个字符串。

`offset`  
比较开始的位置。如果为负数，则从字符串结尾处开始算起。

`length`  
比较的长度。默认值为 `str` 的长度与 `main_str` 的长度减去位置偏移量
`offset` 后二者中的较大者。

`case_insensitivity`  
如果 `case_insensitivity` 为 **`TRUE`**，比较将不区分大小写。

### 返回值

如果 `main_str` 从偏移位置 `offset` 起的子字符串小于 `str`，则返回小于 0
的数；如果大于 `str`，则返回大于 0 的数；如果二者相等，则返回 0。如果
`offset` 大于等于 `main_str` 的长度或 `length` 被设置为小于 1 的值（ PHP
5.5.11 之前的版本），<span class="function">substr\_compare</span>
将打印出一条警告信息并且返回 **`FALSE`**。

### 更新日志

| 版本   | 说明                           |
|--------|--------------------------------|
| 5.5.11 | `length` 可以是 *0*。          |
| 5.1.0  | 允许使用负数的 `offset` 参数。 |

### 范例

**示例 \#1 <span class="function">substr\_compare</span> 范例**

``` php
<?php
echo substr_compare("abcde", "bc", 1, 2); // 0
echo substr_compare("abcde", "de", -2, 2); // 0
echo substr_compare("abcde", "bcg", 1, 2); // 0
echo substr_compare("abcde", "BC", 1, 2, true); // 0
echo substr_compare("abcde", "bc", 1, 3); // 1
echo substr_compare("abcde", "cd", 1, 2); // -1
echo substr_compare("abcde", "abc", 5, 1); // warning
?>
```

### 参见

-   <span class="function">strncmp</span>

substr\_count
=============

计算字串出现的次数

### 说明

<span class="type">int</span> <span
class="methodname">substr\_count</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$length`</span> \]\] )

<span class="function">substr\_count</span> 返回子字符串`needle`
在字符串 `haystack` 中出现的次数。注意 `needle` 区分大小写。

> **Note**:
>
> 该函数不会计算重叠字符串。参见下面的例子。

### 参数

`haystack`  
在此字符串中进行搜索。

`needle`  
要搜索的字符串。

`offset`  
开始计数的偏移位置。如果是负数，就从字符的末尾开始统计。

`length`  
指定偏移位置之后的最大搜索长度。如果偏移量加上这个长度的和大于
`haystack` 的总长度，则打印警告信息。 负数的长度 length 是从 `haystack`
的末尾开始统计的。

### 返回值

该函数返回<span class="type">整型</span>。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.1.0 | 开始支持负数的 `offset` 和 `length`。 |
| 5.1.0 | 新增 `offset` 和 `length` 参数。      |

### 范例

**示例 \#1 <span class="function">substr\_count</span> 范例**

``` php
<?php
$text = 'This is a test';
echo strlen($text); // 14

echo substr_count($text, 'is'); // 2

// 字符串被简化为 's is a test'，因此输出 1
echo substr_count($text, 'is', 3);

// 字符串被简化为 's i'，所以输出 0
echo substr_count($text, 'is', 3, 3);

// 因为 5+10 > 14，所以生成警告
echo substr_count($text, 'is', 5, 10);


// 输出 1，因为该函数不计算重叠字符串
$text2 = 'gcdgcdgcd';
echo substr_count($text2, 'gcdgcd');
?>
```

### 参见

-   <span class="function">count\_chars</span>
-   <span class="function">strpos</span>
-   <span class="function">substr</span>
-   <span class="function">strstr</span>

substr\_replace
===============

替换字符串的子串

### 说明

<span class="type">mixed</span> <span
class="methodname">substr\_replace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$string`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$replacement`</span> , <span class="methodparam"><span
class="type">mixed</span> `$start`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$length`</span> \]
)

<span class="function">substr\_replace</span> 在字符串 `string`
的副本中将由 `start` 和可选的 `length` 参数限定的子字符串使用
`replacement` 进行替换。

### 参数

`string`  
输入字符串。

An <span class="type">array</span> of <span class="type">string</span>s
can be provided, in which case the replacements will occur on each
string in turn. In this case, the `replacement`, `start` and `length`
parameters may be provided either as scalar values to be applied to each
input string in turn, or as <span class="type">array</span>s, in which
case the corresponding array element will be used for each input string.

`replacement`  
替换字符串。

`start`  
如果 `start` 为正数，替换将从 `string` 的 `start` 位置开始。

如果 `start` 为负数，替换将从 `string` 的倒数第 `start` 个位置开始。

`length`  
如果设定了这个参数并且为正数，表示 `string`
中被替换的子字符串的长度。如果设定为负数，它表示待替换的子字符串结尾处距离
`string` 末端的字符个数。如果没有提供此参数，那么它默认为 strlen(
`string` ) （字符串的长度）。当然，如果 `length` 为
0，那么这个函数的功能为将 `replacement` 插入到 `string` 的 `start`
位置处。

### 返回值

返回结果字符串。如果 `string` 是个数组，那么也将返回一个数组。

### 更新日志

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 4.3.3 | All parameters now accept <span class="type">array</span>s. |

### 范例

**示例 \#1 <span class="function">substr\_replace</span> 范例**

``` php
<?php
$var = 'ABCDEFGH:/MNRPQR/';
echo "Original: $var<hr />\n";

/* 这两个例子使用 “bob” 替换整个 $var。*/
echo substr_replace($var, 'bob', 0) . "<br />\n";
echo substr_replace($var, 'bob', 0, strlen($var)) . "<br />\n";

/* 将 “bob” 插入到 $var 的开头处。*/
echo substr_replace($var, 'bob', 0, 0) . "<br />\n";

/* 下面两个例子使用 “bob” 替换 $var 中的 “MNRPQR”。*/
echo substr_replace($var, 'bob', 10, -1) . "<br />\n";
echo substr_replace($var, 'bob', -7, -1) . "<br />\n";

/* 从 $var 中删除 “MNRPQR”。*/
echo substr_replace($var, '', 10, -1) . "<br />\n";
?>
```

**示例 \#2 Using <span class="function">substr\_replace</span> to
replace multiple strings at once**

``` php
<?php
$input = array('A: XXX', 'B: XXX', 'C: XXX');

// A simple case: replace XXX in each string with YYY.
echo implode('; ', substr_replace($input, 'YYY', 3, 3))."\n";

// A more complicated case where each replacement is different.
$replace = array('AAA', 'BBB', 'CCC');
echo implode('; ', substr_replace($input, $replace, 3, 3))."\n";

// Replace a different number of characters each time.
$length = array(1, 2, 3);
echo implode('; ', substr_replace($input, $replace, 3, $length))."\n";
?>
```

以上例程会输出：

    A: YYY; B: YYY; C: YYY
    A: AAA; B: BBB; C: CCC
    A: AAAXX; B: BBBX; C: CCC

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">str\_replace</span>
-   <span class="function">substr</span>
-   <a href="/language/types/string.html#language.types.string.substr" class="link">字符串访问与修改</a>

substr
======

返回字符串的子串

### 说明

<span class="type">string</span> <span class="methodname">substr</span>
( <span class="methodparam"><span class="type">string</span>
`$string`</span> , <span class="methodparam"><span
class="type">int</span> `$start`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

返回字符串 `string` 由 `start` 和 `length` 参数指定的子字符串。

### 参数

`string`  
输入字符串。必须至少有一个字符。

`start`  
如果 `start` 是非负数，返回的字符串将从 `string` 的 `start` 位置开始，从
0 开始计算。例如，在字符串 “*abcdef*” 中，在位置 *0* 的字符是
“*a*”，位置 *2* 的字符串是 “*c*” 等等。

如果 `start` 是负数，返回的字符串将从 `string` 结尾处向前数第 `start`
个字符开始。

如果 `string` 的长度小于 `start`，将返回 **`FALSE`**。

**示例 \#1 使用负数 `start`**

``` php
<?php
$rest = substr("abcdef", -1);    // 返回 "f"
$rest = substr("abcdef", -2);    // 返回 "ef"
$rest = substr("abcdef", -3, 1); // 返回 "d"
?>
```

`length`  
如果提供了正数的 `length`，返回的字符串将从 `start` 处开始最多包括
`length` 个字符（取决于 `string` 的长度）。

如果提供了负数的 `length`，那么 `string` 末尾处的 `length`
个字符将会被省略（若 `start` 是负数则从字符串尾部算起）。如果 `start`
不在这段文本中，那么将返回 **`FALSE`**。

如果提供了值为 *0*，**`FALSE`** 或 **`NULL`** 的
`length`，那么将返回一个空字符串。

如果没有提供 `length`，返回的子字符串将从 `start`
位置开始直到字符串结尾。

**示例 \#2 使用负数 `length`**

``` php
<?php
$rest = substr("abcdef", 0, -1);  // 返回 "abcde"
$rest = substr("abcdef", 2, -1);  // 返回 "cde"
$rest = substr("abcdef", 4, -4);  // 返回 ""
$rest = substr("abcdef", -3, -1); // 返回 "de"
?>
```

### 返回值

返回提取的子字符串， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本          | 说明                                                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.0         | 如果 `string` 的字符串长度与 `start` 相同时将返回一个空字符串。在之前的版本中，这种情况将返回 **`FALSE`** 。                                     |
| 5.2.2 - 5.2.6 | If the `start` parameter indicates the position of a negative truncation or beyond, false is returned. Other versions get the string from start. |

### 范例

**示例 \#3 <span class="function">substr</span> 基本用法**

``` php
<?php
echo substr('abcdef', 1);     // bcdef
echo substr('abcdef', 1, 3);  // bcd
echo substr('abcdef', 0, 4);  // abcd
echo substr('abcdef', 0, 8);  // abcdef
echo substr('abcdef', -1, 1); // f

// 访问字符串中的单个字符
// 也可以使用中括号
$string = 'abcdef';
echo $string[0];                 // a
echo $string[3];                 // d
echo $string[strlen($string)-1]; // f
?>
```

**示例 \#4 <span class="function">substr</span> casting behaviour**

``` php
<?php
class apple {
    public function __toString() {
        return "green";
    }
}

echo "1) ".var_export(substr("pear", 0, 2), true).PHP_EOL;
echo "2) ".var_export(substr(54321, 0, 2), true).PHP_EOL;
echo "3) ".var_export(substr(new apple(), 0, 2), true).PHP_EOL;
echo "4) ".var_export(substr(true, 0, 1), true).PHP_EOL;
echo "5) ".var_export(substr(false, 0, 1), true).PHP_EOL;
echo "6) ".var_export(substr("", 0, 1), true).PHP_EOL;
echo "7) ".var_export(substr(1.2e3, 0, 4), true).PHP_EOL;
?>
```

Output of the above example in PHP 7:

    1) 'pe'
    2) '54'
    3) 'gr'
    4) '1'
    5) false
    6) false
    7) '1200'

Output of the above example in PHP 5:

    1) 'pe'
    2) '54'
    3) 'gr'
    4) '1'
    5) false
    6) false
    7) '1200'

### 错误／异常

错误时返回 **`FALSE`**。

``` php
<?php
var_dump(substr('a', 2)); // bool(false)
?>
```

### 参见

-   <span class="function">strrchr</span>
-   <span class="function">substr\_replace</span>
-   <span class="function">preg\_match</span>
-   <span class="function">trim</span>
-   <span class="function">mb\_substr</span>
-   <span class="function">wordwrap</span>
-   <a href="/language/types/string.html#language.types.string.substr" class="link">字符串访问和修改</a>

trim
====

去除字符串首尾处的空白字符（或者其他字符）

### 说明

<span class="type">string</span> <span class="methodname">trim</span> (
<span class="methodparam"><span class="type">string</span> `$str`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$character_mask`<span class="initializer"> = "
\\t\\n\\r\\0\\x0B"</span></span> \] )

此函数返回字符串 `str`
去除首尾空白字符后的结果。如果不指定第二个参数，<span
class="function">trim</span> 将去除这些字符：

-   <span class="simpara"> " " (ASCII *32* (*0x20*))，普通空格符。
    </span>
-   <span class="simpara"> "\\t" (ASCII *9* (*0x09*))，制表符。 </span>
-   <span class="simpara"> "\\n" (ASCII *10* (*0x0A*))，换行符。 </span>
-   <span class="simpara"> "\\r" (ASCII *13* (*0x0D*))，回车符。 </span>
-   <span class="simpara"> "\\0" (ASCII *0* (*0x00*))，空字节符。
    </span>
-   <span class="simpara"> "\\x0B" (ASCII *11* (*0x0B*))，垂直制表符。
    </span>

### 参数

`str`  
待处理的<span class="type">字符串</span>。

`character_mask`  
可选参数，过滤字符也可由 `character_mask`
参数指定。一般要列出所有希望过滤的字符，也可以使用 “*..*”
列出一个字符范围。

### 返回值

过滤后的字符串。

### 范例

**示例 \#1 <span class="function">trim</span> 使用范例**

``` php
<?php

$text   = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";

$trimmed = trim($text);
var_dump($trimmed);

$trimmed = trim($text, " \t.");
var_dump($trimmed);

$trimmed = trim($hello, "Hdle");
var_dump($trimmed);

// 清除 $binary 首位的 ASCII 控制字符
// （包括 0-31）
$clean = trim($binary, "\x00..\x1F");
var_dump($clean);

?>
```

以上例程会输出：

    string(32) "        These are a few words :) ...  "
    string(16) "    Example string
    "
    string(11) "Hello World"

    string(28) "These are a few words :) ..."
    string(24) "These are a few words :)"
    string(5) "o Wor"
    string(14) "Example string"

**示例 \#2 使用 <span class="function">trim</span> 清理数组值**

``` php
<?php
function trim_value(&$value) 
{ 
    $value = trim($value); 
}

$fruit = array('apple','banana ', ' cranberry ');
var_dump($fruit);

array_walk($fruit, 'trim_value');
var_dump($fruit);

?>
```

以上例程会输出：

    array(3) {
      [0]=>
      string(5) "apple"
      [1]=>
      string(7) "banana "
      [2]=>
      string(11) " cranberry "
    }
    array(3) {
      [0]=>
      string(5) "apple"
      [1]=>
      string(6) "banana"
      [2]=>
      string(9) "cranberry"
    }

### 注释

> **Note**: **Possible gotcha: removing middle characters**  
>
> Because <span class="function">trim</span> trims characters from the
> beginning and end of a <span class="type">string</span>, it may be
> confusing when characters are (or are not) removed from the middle.
> *trim('abc', 'bad')* removes both 'a' and 'b' because it trims 'a'
> thus moving 'b' to the beginning to also be trimmed. So, this is why
> it "works" whereas *trim('abc', 'b')* seemingly does not.

### 参见

-   <span class="function">ltrim</span>
-   <span class="function">rtrim</span>
-   <span class="function">str\_replace</span>

ucfirst
=======

将字符串的首字母转换为大写

### 说明

<span class="type">string</span> <span class="methodname">ucfirst</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> )

将 `str` 的首字符（如果首字符是字母）转换为大写字母，并返回这个字符串。

注意字母的定义取决于当前区域设定。例如，在默认的 “C” 区域，字符
umlaut-a（ä）将不会被转换。

### 参数

`str`  
输入字符串。

### 返回值

返回结果字符串。

### 范例

**示例 \#1 <span class="function">ucfirst</span> 范例**

``` php
<?php
$foo = 'hello world!';
$foo = ucfirst($foo);             // Hello world!

$bar = 'HELLO WORLD!';
$bar = ucfirst($bar);             // HELLO WORLD!
$bar = ucfirst(strtolower($bar)); // Hello world!
?>
```

### 参见

-   <span class="function">lcfirst</span>
-   <span class="function">strtolower</span>
-   <span class="function">strtoupper</span>
-   <span class="function">ucwords</span>

ucwords
=======

将字符串中每个单词的首字母转换为大写

### 说明

<span class="type">string</span> <span class="methodname">ucwords</span>
( <span class="methodparam"><span class="type">string</span>
`$str`</span> \[, <span class="methodparam"> <span
class="type">string</span> `$delimiters`<span class="initializer"> = "
\\t\\r\\n\\f\\v"</span> </span> \] )

将 `str`
中每个单词的首字符（如果首字符是字母）转换为大写字母，并返回这个字符串。

这里单词的定义是紧跟在 `delimiters`
参数（默认：空格符、制表符、换行符、回车符、水平线以及竖线）之后的子字符串。

### 参数

`str`  
输入字符串。

`delimiters`  
可选的 `delimiters`，包含了单词分割字符。

### 返回值

返回转换后的字符串。

### 更新日志

| 版本           | 说明                       |
|----------------|----------------------------|
| 5.4.32, 5.5.16 | 增加了 `delimiters` 参数。 |

### 范例

**示例 \#1 <span class="function">ucwords</span> 范例**

``` php
<?php
$foo = 'hello world!';
$foo = ucwords($foo);             // Hello World!

$bar = 'HELLO WORLD!';
$bar = ucwords($bar);             // HELLO WORLD!
$bar = ucwords(strtolower($bar)); // Hello World!
?>
```

**示例 \#2 <span class="function">ucwords</span> 自定义 delimiters
的例子**

``` php
<?php
$foo = 'hello|world!';
$bar = ucwords($foo);             // Hello|world!

$baz = ucwords($foo, "|");        // Hello|World!
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">strtoupper</span>
-   <span class="function">strtolower</span>
-   <span class="function">ucfirst</span>
-   <span class="function">mb\_convert\_case</span>

vfprintf
========

将格式化字符串写入流

### 说明

<span class="type">int</span> <span class="methodname">vfprintf</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> , <span
class="methodparam"><span class="type">array</span> `$args`</span> )

向由 `handle` 指定的流资源句柄中写入根据 `format` 格式化后的字符串。

作用与 <span class="function">fprintf</span>
函数类似，但是接收一个数组参数，而不是一系列可变数量的参数。

### 参数

`handle`  

`format`  
关于 `format` 的描述，参见 <span class="function">sprintf</span>。

`args`  

### 返回值

返回输出字符串的长度。

### 范例

**示例 \#1 <span class="function">vfprintf</span>: 前导 0 的整数**

``` php
<?php
if (!($fp = fopen('date.txt', 'w')))
    return;

vfprintf($fp, "%04d-%02d-%02d", array($year, $month, $day));
// 将向 date.txt 写入格式化的 ISO 标准日期
?>
```

### 参见

-   <span class="function">printf</span>
-   <span class="function">sprintf</span>
-   <span class="function">sscanf</span>
-   <span class="function">fscanf</span>
-   <span class="function">vsprintf</span>
-   <span class="function">number\_format</span>

vprintf
=======

输出格式化字符串

### 说明

<span class="type">int</span> <span class="methodname">vprintf</span> (
<span class="methodparam"><span class="type">string</span>
`$format`</span> , <span class="methodparam"><span
class="type">array</span> `$args`</span> )

根据 `format` （<span class="function">sprintf</span>
函数文档中有相关描述）参数指定的格式，在一个格式化字符串中显示多个值。

作用与 <span class="function">printf</span>
函数类似，但是接收一个数组参数，而不是一系列可变数量的参数。

### 参数

`format`  
关于 `format` 的描述，参见 <span class="function">sprintf</span>。

`args`  

### 返回值

返回输出字符串的长度。

### 范例

**示例 \#1 <span class="function">vprintf</span>: 前导 0 的整数**

``` php
<?php
vprintf("%04d-%02d-%02d", explode('-', '1988-8-1')); // 1988-08-01
?>
```

### 参见

-   <span class="function">printf</span>
-   <span class="function">sprintf</span>
-   <span class="function">vsprintf</span>

vsprintf
========

返回格式化字符串

### 说明

<span class="type">string</span> <span
class="methodname">vsprintf</span> ( <span class="methodparam"><span
class="type">string</span> `$format`</span> , <span
class="methodparam"><span class="type">array</span> `$args`</span> )

作用与 <span class="function">sprintf</span>
函数类似，但是接收一个数组参数，而不是一系列可变数量的参数。

### 参数

`format`  
关于 `format` 的描述，参见 <span class="function">sprintf</span>。

`args`  

### 返回值

根据 `format` （<span class="function">sprintf</span>
函数文档中有相关描述）参数指定的格式，在一个字符串中返回一系列值。

### 范例

**示例 \#1 <span class="function">vsprintf</span>: 前导 0 的整数**

``` php
<?php
print vsprintf("%04d-%02d-%02d", explode('-', '1988-8-1')); // 1988-08-01
?>
```

### 参见

-   <span class="function">sprintf</span>
-   <span class="function">vprintf</span>

wordwrap
========

打断字符串为指定数量的字串

### 说明

<span class="type">string</span> <span
class="methodname">wordwrap</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`<span
class="initializer"> = 75</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$break`<span
class="initializer"> = "\\n"</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$cut`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\] )

使用字符串断点将字符串打断为指定数量的字串。

### 参数

`str`  
输入字符串。

`width`  
列宽度。

`break`  
使用可选的 `break` 参数打断字符串。

`cut`  
如果 `cut` 设置为 **`TRUE`**，字符串总是在指定的 `width`
或者之前位置被打断。因此，如果有的单词宽度超过了给定的宽度，它将被分隔开来。（参见第二个范例）。
当它是 **`FALSE`** ，函数不会分割单词，哪怕 `width` 小于单词宽度。

### 返回值

返回打断后的字符串。

### 范例

**示例 \#1 <span class="function">wordwrap</span> 范例**

``` php
<?php
$text = "The quick brown fox jumped over the lazy dog.";
$newtext = wordwrap($text, 20, "<br />\n");

echo $newtext;
?>
```

以上例程会输出：

    The quick brown fox<br />
    jumped over the lazy<br />
    dog.

**示例 \#2 <span class="function">wordwrap</span> 范例**

``` php
<?php
$text = "A very long woooooooooooord.";
$newtext = wordwrap($text, 8, "\n", true);

echo "$newtext\n";
?>
```

以上例程会输出：

    A very
    long
    wooooooo
    ooooord.

**示例 \#3 <span class="function">wordwrap</span> 例子**

``` php
<?php
$text = "A very long woooooooooooooooooord. and something";
$newtext = wordwrap($text, 8, "\n", false);

echo "$newtext\n";
?>
```

以上例程会输出：

    A very
    long
    woooooooooooooooooord.
    and
    something

### 参见

-   <span class="function">nl2br</span>
-   <span class="function">chunk\_split</span>

**目录**

-   [addcslashes](/ref/strings.html#addcslashes) — 以 C
    语言风格使用反斜线转义字符串中的字符
-   [addslashes](/ref/strings.html#addslashes) — 使用反斜线引用字符串
-   [bin2hex](/ref/strings.html#bin2hex) —
    函数把包含数据的二进制字符串转换为十六进制值
-   [chop](/ref/strings.html#chop) — rtrim 的别名
-   [chr](/ref/strings.html#chr) — 返回指定的字符
-   [chunk\_split](/ref/strings.html#chunk_split) — 将字符串分割成小块
-   [convert\_cyr\_string](/ref/strings.html#convert_cyr_string) —
    将字符由一种 Cyrillic 字符转换成另一种
-   [convert\_uudecode](/ref/strings.html#convert_uudecode) — 解码一个
    uuencode 编码的字符串
-   [convert\_uuencode](/ref/strings.html#convert_uuencode) — 使用
    uuencode 编码一个字符串
-   [count\_chars](/ref/strings.html#count_chars) —
    返回字符串所用字符的信息
-   [crc32](/ref/strings.html#crc32) — 计算一个字符串的 crc32 多项式
-   [crypt](/ref/strings.html#crypt) — 单向字符串散列
-   [echo](/ref/strings.html#echo) — 输出一个或多个字符串
-   [explode](/ref/strings.html#explode) —
    使用一个字符串分割另一个字符串
-   [fprintf](/ref/strings.html#fprintf) — 将格式化后的字符串写入到流
-   [get\_html\_translation\_table](/ref/strings.html#get_html_translation_table)
    — 返回使用 htmlspecialchars 和 htmlentities 后的转换表
-   [hebrev](/ref/strings.html#hebrev) —
    将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew）
-   [hebrevc](/ref/strings.html#hebrevc) —
    将逻辑顺序希伯来文（logical-Hebrew）转换为视觉顺序希伯来文（visual-Hebrew），并且转换换行符
-   [hex2bin](/ref/strings.html#hex2bin) —
    转换十六进制字符串为二进制字符串
-   [html\_entity\_decode](/ref/strings.html#html_entity_decode) —
    Convert HTML entities to their corresponding characters
-   [htmlentities](/ref/strings.html#htmlentities) — 将字符转换为 HTML
    转义字符
-   [htmlspecialchars\_decode](/ref/strings.html#htmlspecialchars_decode)
    — 将特殊的 HTML 实体转换回普通字符
-   [htmlspecialchars](/ref/strings.html#htmlspecialchars) —
    将特殊字符转换为 HTML 实体
-   [implode](/ref/strings.html#implode) —
    将一个一维数组的值转化为字符串
-   [join](/ref/strings.html#join) — 别名 implode
-   [lcfirst](/ref/strings.html#lcfirst) — 使一个字符串的第一个字符小写
-   [levenshtein](/ref/strings.html#levenshtein) —
    计算两个字符串之间的编辑距离
-   [localeconv](/ref/strings.html#localeconv) — Get numeric formatting
    information
-   [ltrim](/ref/strings.html#ltrim) —
    删除字符串开头的空白字符（或其他字符）
-   [md5\_file](/ref/strings.html#md5_file) — 计算指定文件的 MD5 散列值
-   [md5](/ref/strings.html#md5) — 计算字符串的 MD5 散列值
-   [metaphone](/ref/strings.html#metaphone) — Calculate the metaphone
    key of a string
-   [money\_format](/ref/strings.html#money_format) —
    将数字格式化成货币字符串
-   [nl\_langinfo](/ref/strings.html#nl_langinfo) — Query language and
    locale information
-   [nl2br](/ref/strings.html#nl2br) — 在字符串所有新行之前插入 HTML
    换行标记
-   [number\_format](/ref/strings.html#number_format) —
    以千位分隔符方式格式化一个数字
-   [ord](/ref/strings.html#ord) — 转换字符串第一个字节为 0-255 之间的值
-   [parse\_str](/ref/strings.html#parse_str) — 将字符串解析成多个变量
-   [print](/ref/strings.html#print) — 输出字符串
-   [printf](/ref/strings.html#printf) — 输出格式化字符串
-   [quoted\_printable\_decode](/ref/strings.html#quoted_printable_decode)
    — 将 quoted-printable 字符串转换为 8-bit 字符串
-   [quoted\_printable\_encode](/ref/strings.html#quoted_printable_encode)
    — 将 8-bit 字符串转换成 quoted-printable 字符串
-   [quotemeta](/ref/strings.html#quotemeta) — 转义元字符集
-   [rtrim](/ref/strings.html#rtrim) —
    删除字符串末端的空白字符（或者其他字符）
-   [setlocale](/ref/strings.html#setlocale) — 设置地区信息
-   [sha1\_file](/ref/strings.html#sha1_file) — 计算文件的 sha1 散列值
-   [sha1](/ref/strings.html#sha1) — 计算字符串的 sha1 散列值
-   [similar\_text](/ref/strings.html#similar_text) —
    计算两个字符串的相似度
-   [soundex](/ref/strings.html#soundex) — Calculate the soundex key of
    a string
-   [sprintf](/ref/strings.html#sprintf) — Return a formatted string
-   [sscanf](/ref/strings.html#sscanf) — 根据指定格式解析输入的字符
-   [str\_getcsv](/ref/strings.html#str_getcsv) — 解析 CSV
    字符串为一个数组
-   [str\_ireplace](/ref/strings.html#str_ireplace) — str\_replace
    的忽略大小写版本
-   [str\_pad](/ref/strings.html#str_pad) —
    使用另一个字符串填充字符串为指定长度
-   [str\_repeat](/ref/strings.html#str_repeat) — 重复一个字符串
-   [str\_replace](/ref/strings.html#str_replace) — 子字符串替换
-   [str\_rot13](/ref/strings.html#str_rot13) — 对字符串执行 ROT13 转换
-   [str\_shuffle](/ref/strings.html#str_shuffle) — 随机打乱一个字符串
-   [str\_split](/ref/strings.html#str_split) — 将字符串转换为数组
-   [str\_word\_count](/ref/strings.html#str_word_count) —
    返回字符串中单词的使用情况
-   [strcasecmp](/ref/strings.html#strcasecmp) —
    二进制安全比较字符串（不区分大小写）
-   [strchr](/ref/strings.html#strchr) — 别名 strstr
-   [strcmp](/ref/strings.html#strcmp) — 二进制安全字符串比较
-   [strcoll](/ref/strings.html#strcoll) — 基于区域设置的字符串比较
-   [strcspn](/ref/strings.html#strcspn) —
    获取不匹配遮罩的起始子字符串的长度
-   [strip\_tags](/ref/strings.html#strip_tags) — 从字符串中去除 HTML 和
    PHP 标记
-   [stripcslashes](/ref/strings.html#stripcslashes) — 反引用一个使用
    addcslashes 转义的字符串
-   [stripos](/ref/strings.html#stripos) —
    查找字符串首次出现的位置（不区分大小写）
-   [stripslashes](/ref/strings.html#stripslashes) —
    反引用一个引用字符串
-   [stristr](/ref/strings.html#stristr) — strstr 函数的忽略大小写版本
-   [strlen](/ref/strings.html#strlen) — 获取字符串长度
-   [strnatcasecmp](/ref/strings.html#strnatcasecmp) —
    使用“自然顺序”算法比较字符串（不区分大小写）
-   [strnatcmp](/ref/strings.html#strnatcmp) —
    使用自然排序算法比较字符串
-   [strncasecmp](/ref/strings.html#strncasecmp) —
    二进制安全比较字符串开头的若干个字符（不区分大小写）
-   [strncmp](/ref/strings.html#strncmp) —
    二进制安全比较字符串开头的若干个字符
-   [strpbrk](/ref/strings.html#strpbrk) —
    在字符串中查找一组字符的任何一个字符
-   [strpos](/ref/strings.html#strpos) — 查找字符串首次出现的位置
-   [strrchr](/ref/strings.html#strrchr) —
    查找指定字符在字符串中的最后一次出现
-   [strrev](/ref/strings.html#strrev) — 反转字符串
-   [strripos](/ref/strings.html#strripos) —
    计算指定字符串在目标字符串中最后一次出现的位置（不区分大小写）
-   [strrpos](/ref/strings.html#strrpos) —
    计算指定字符串在目标字符串中最后一次出现的位置
-   [strspn](/ref/strings.html#strspn) —
    计算字符串中全部字符都存在于指定字符集合中的第一段子串的长度。
-   [strstr](/ref/strings.html#strstr) — 查找字符串的首次出现
-   [strtok](/ref/strings.html#strtok) — 标记分割字符串
-   [strtolower](/ref/strings.html#strtolower) — 将字符串转化为小写
-   [strtoupper](/ref/strings.html#strtoupper) — 将字符串转化为大写
-   [strtr](/ref/strings.html#strtr) — 转换指定字符
-   [substr\_compare](/ref/strings.html#substr_compare) —
    二进制安全比较字符串（从偏移位置比较指定长度）
-   [substr\_count](/ref/strings.html#substr_count) — 计算字串出现的次数
-   [substr\_replace](/ref/strings.html#substr_replace) —
    替换字符串的子串
-   [substr](/ref/strings.html#substr) — 返回字符串的子串
-   [trim](/ref/strings.html#trim) —
    去除字符串首尾处的空白字符（或者其他字符）
-   [ucfirst](/ref/strings.html#ucfirst) — 将字符串的首字母转换为大写
-   [ucwords](/ref/strings.html#ucwords) —
    将字符串中每个单词的首字母转换为大写
-   [vfprintf](/ref/strings.html#vfprintf) — 将格式化字符串写入流
-   [vprintf](/ref/strings.html#vprintf) — 输出格式化字符串
-   [vsprintf](/ref/strings.html#vsprintf) — 返回格式化字符串
-   [wordwrap](/ref/strings.html#wordwrap) — 打断字符串为指定数量的字串
