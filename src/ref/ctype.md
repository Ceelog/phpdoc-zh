ctype\_alnum
============

做字母和数字字符检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_alnum</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的<span class="type">string</span>,`text`
是否全部为字母和(或)数字字符。

### 参数

`text`  
测试字符串。

### 返回值

如果`text`中所有的字符全部是字母和(或者)数字，返回 **`TRUE`**
否则返回**`FALSE`**

### 范例

**示例 \#1 A <span class="function">ctype\_alnum</span> 示例
(使用默认的区域设置)**

``` php
<?php
$strings = array('AbCd1zyZ9', 'foo!#$bar');
foreach ($strings as $testcase) {
    if (ctype_alnum($testcase)) {
        echo "The string $testcase consists of all letters or digits.\n";
    } else {
        echo "The string $testcase does not consist of all letters or digits.\n";
    }
}
?>
```

以上例程会输出：

    The string AbCd1zyZ9 consists of all letters or digits.
    The string foo!#$bar does not consist of all letters or digits.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_alpha</span>
-   <span class="function">ctype\_digit</span>
-   <span class="function">setlocale</span>

ctype\_alpha
============

做纯字符检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_alpha</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

查看提供的<span
class="type">string</span>，`text`里面的所有字符是否只包含字符。
在标准的 *C* 语言环境下，字母仅仅是指 *\[A-Za-z\]* ， <span
class="function">ctype\_alpha</span> 等同于 *(ctype\_upper($text) \|\|
ctype\_lower($text))* 如果 `text`
是简单的单个字符串还好，但是在其他语言中有些字母被认为既不是大写也不是小写。

### 参数

`text`  
被测试的字符串。

### 返回值

如果在当前语言环境中 `text`
里的每个字符都是一个字母，那么就返回**`TRUE`**，反之则返回**`FALSE`**。

### 范例

**示例 \#1 一个 <span class="function">ctype\_alpha</span>
例子（使用默认的语言环境）**

``` php
<?php
$strings = array('KjgWZC', 'arf12');
foreach ($strings as $testcase) {
    if (ctype_alpha($testcase)) {
        echo "The string $testcase consists of all letters.\n";
    } else {
        echo "The string $testcase does not consist of all letters.\n";
    }
}
?>
```

以上例程会输出：

    The string KjgWZC consists of all letters.
    The string arf12 does not consist of all letters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_upper</span>
-   <span class="function">ctype\_lower</span>
-   <span class="function">setlocale</span>

ctype\_cntrl
============

做控制字符检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_cntrl</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符是不是都是控制字符。 控制字符就是例如：换行、缩进、空格。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果在当前的语言环境下 `text` 里面的每个字符都是控制字符，就返回
**`TRUE`** ；反之就返回 **`FALSE`** 。

### 范例

**示例 \#1 一个 <span class="function">ctype\_cntrl</span> 例子**

``` php
<?php
$strings = array('string1' => "\n\r\t", 'string2' => 'arf12');
foreach ($strings as $name => $testcase) {
    if (ctype_cntrl($testcase)) {
        echo "The string '$name' consists of all control characters.\n";
    } else {
        echo "The string '$name' does not consist of all control characters.\n";
    }
}
?>
```

以上例程会输出：

    The string 'string1' consists of all control characters.
    The string 'string2' does not consist of all control characters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_print</span>

ctype\_digit
============

做纯数字检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_digit</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符是不是都是数字。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果 `text` 字符串是一个十进制数字，就返回 **`TRUE`** ；反之就返回
**`FALSE`** 。

### 更新日志

| 版本  | 说明                                                                          |
|-------|-------------------------------------------------------------------------------|
| 5.1.0 | 在 PHP 5.1.0 之前，当 `text` 是一个空字符串的时候，该函数将返回 **`TRUE`** 。 |

### 范例

**示例 \#1 一个 <span class="function">ctype\_digit</span> 例子**

``` php
<?php
$strings = array('1820.20', '10002', 'wsl!12');
foreach ($strings as $testcase) {
    if (ctype_digit($testcase)) {
        echo "The string $testcase consists of all digits.\n";
    } else {
        echo "The string $testcase does not consist of all digits.\n";
    }
}
?>
```

以上例程会输出：

    The string 1820.20 does not consist of all digits.
    The string 10002 consists of all digits.
    The string wsl!12 does not consist of all digits.

**示例 \#2 一个通过 <span class="function">ctype\_digit</span>
来比对字符和整数的例子。**

``` php
<?php

$numeric_string = '42';
$integer        = 42;

ctype_digit($numeric_string);  // true
ctype_digit($integer);         // false (ASCII 42 is the * character)

is_numeric($numeric_string);   // true
is_numeric($integer);          // true
?>
```

### 注释

> **Note**:
>
> 这个函数的参数要求是一个 <span class="type">string</span>
> 这一点是非常有用的，因此当你传入一个 <span class="type">integer</span>
> 的参数也许不能得到期望的结果。然后，同样需要注意HTML表单将会返回数字字符串而不是一个整型。
> 看下手册的 <a href="/language/types.html" class="link">types</a>
> 章节。

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_alnum</span>
-   <span class="function">ctype\_xdigit</span>
-   <span class="function">is\_numeric</span>
-   <span class="function">is\_int</span>
-   <span class="function">is\_string</span>

ctype\_graph
============

做可打印字符串检测，空格除外

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_graph</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符输出都是可见的。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果 `text` 里面的每个字符都是输出可见的（没有空白），就返回 **`TRUE`**
；反之就返回 **`FALSE`** 。

### 范例

**示例 \#1 一个 <span class="function">ctype\_graph</span> 例子**

``` php
<?php
$strings = array('string1' => "asdf\n\r\t", 'string2' => 'arf12', 'string3' => 'LKA#@%.54');
foreach ($strings as $name => $testcase) {
    if (ctype_graph($testcase)) {
        echo "The string '$name' consists of all (visibly) printable characters.\n";
    } else {
        echo "The string '$name' does not consist of all (visibly) printable characters.\n";
    }
}
?>
```

以上例程会输出：

    The string 'string1' does not consist of all (visibly) printable characters.
    The string 'string2' consists of all (visibly) printable characters.
    The string 'string3' consists of all (visibly) printable characters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_alnum</span>
-   <span class="function">ctype\_print</span>
-   <span class="function">ctype\_punct</span>

ctype\_lower
============

做小写字符检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_lower</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符是不是都是小写字母。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果在当前的语言环境下 `text` 里面的每个字符都是小写字母，就返回
**`TRUE`** ；反之就返回 **`FALSE`** 。

### 范例

**示例 \#1 一个 <span class="function">ctype\_lower</span> 例子
(使用默认的语言环境)**

``` php
<?php
$strings = array('aac123', 'qiutoas', 'QASsdks');
foreach ($strings as $testcase) {
    if (ctype_lower($testcase)) {
        echo "The string $testcase consists of all lowercase letters.\n";
    } else {
        echo "The string $testcase does not consist of all lowercase letters.\n";
    }
}
?>
```

以上例程会输出：

    The string aac123 does not consist of all lowercase letters.
    The string qiutoas consists of all lowercase letters.
    The string QASsdks does not consist of all lowercase letters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_alpha</span>
-   <span class="function">ctype\_upper</span>
-   <span class="function">setlocale</span>

ctype\_print
============

做可打印字符检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_print</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符是不是都是可以打印出来。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果在当前的语言环境下 `text`
里面的每个字符都能被实际输出（包括空白），就返回 **`TRUE`** ；如果
`text` 里面包含控制字符或者那些根本不会有任何输出的字符串，就返回
**`FALSE`** 。

### 范例

**示例 \#1 一个 <span class="function">ctype\_print</span> 例子**

``` php
<?php
$strings = array('string1' => "asdf\n\r\t", 'string2' => 'arf12', 'string3' => 'LKA#@%.54');
foreach ($strings as $name => $testcase) {
    if (ctype_print($testcase)) {
        echo "The string '$name' consists of all printable characters.\n";
    } else {
        echo "The string '$name' does not consist of all printable characters.\n";
    }
}
?>
```

以上例程会输出：

    The string 'string1' does not consist of all printable characters.
    The string 'string2' consists of all printable characters.
    The string 'string3' consists of all printable characters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_cntrl</span>
-   <span class="function">ctype\_graph</span>
-   <span class="function">ctype\_punct</span>

ctype\_punct
============

检测可打印的字符是不是不包含空白、数字和字母

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_punct</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符是不是都是标点符号。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果在 `text`
里面的每个字符都是能打印的，但不是字母、数字，也不是空白，那么就返回
**`TRUE`** ；反之则返回 **`FALSE`** 。

### 范例

**示例 \#1 一个 <span class="function">ctype\_punct</span> 的例子**

``` php
<?php
$strings = array('ABasdk!@!$#', '!@ # $', '*&$()');
foreach ($strings as $testcase) {
    if (ctype_punct($testcase)) {
        echo "The string $testcase consists of all punctuation.\n";
    } else {
        echo "The string $testcase does not consist of all punctuation.\n";
    }
}
?>
```

以上例程会输出：

    The string ABasdk!@!$# does not consist of all punctuation.
    The string !@ # $ does not consist of all punctuation.
    The string *&$() consists of all punctuation.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_cntrl</span>
-   <span class="function">ctype\_graph</span>

ctype\_space
============

做空白字符检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_space</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查提供的 <span class="type">string</span> 和 `text`
里面的字符是否包含空白。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果 `text` 里面的每个字符最终被实际输出的时候都是某种形式的空白，就返回
**`TRUE`** ；否则返回 **`FALSE`** 。
除了空白字符，还包括缩进，垂直制表符，换行符，回车和换页字符。

### 范例

**示例 \#1 一个 <span class="function">ctype\_space</span> 例子**

``` php
<?php
$strings = array('string1' => "\n\r\t", 'string2' => "\narf12", 'string3' => '\n\r\t');
foreach ($strings as $name => $testcase) {
    if (ctype_space($testcase)) {
        echo "The string '$name' consists of all whitespace characters.\n";
    } else {
        echo "The string '$name' does not consist of all whitespace characters.\n";
    }
}
?>
```

以上例程会输出：

    The string 'string1' consists of all whitespace characters.
    The string 'string2' does not consist of all whitespace characters.
    The string 'string3' does not consist of all whitespace characters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_cntrl</span>
-   <span class="function">ctype\_graph</span>
-   <span class="function">ctype\_punct</span>

ctype\_upper
============

做大写字母检测

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_upper</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

检查 <span class="type">string</span> 和 `text`
里面的字符是不是都是大写字母。

### 参数

`text`  
需要被测试的字符串。

### 返回值

在当前语言环境下，如果 `text` 里面的每个字符都是大写字母，就返回
**`TRUE`**。

### 范例

**示例 \#1 一个 <span class="function">ctype\_upper</span> 例子
（使用当前默认语言环境）**

``` php
<?php
$strings = array('AKLWC139', 'LMNSDO', 'akwSKWsm');
foreach ($strings as $testcase) {
    if (ctype_upper($testcase)) {
        echo "The string $testcase consists of all uppercase letters.\n";
    } else {
        echo "The string $testcase does not consist of all uppercase letters.\n";
    }
}
?>
```

以上例程会输出：

    The string AKLWC139 does not consist of all uppercase letters.
    The string LMNSDO consists of all uppercase letters.
    The string akwSKWsm does not consist of all uppercase letters.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_alpha</span>
-   <span class="function">ctype\_lower</span>
-   <span class="function">setlocale</span>

ctype\_xdigit
=============

检测字符串是否只包含十六进制字符

### 说明

<span class="type">bool</span> <span
class="methodname">ctype\_xdigit</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

检查 <span class="type">string</span> 和 `text`
里面的字符是不是都是十六进制字符串。

### 参数

`text`  
需要被测试的字符串。

### 返回值

如果 `text` 里面的每个字符都是十六进制字符。也就是只能包含十进制的树枝和
*\[A-Fa-f\]* 的字母。否则，返回 **`FALSE`** 。

### 范例

**示例 \#1 一个 <span class="function">ctype\_xdigit</span> 的例子**

``` php
<?php
$strings = array('AB10BC99', 'AR1012', 'ab12bc99');
foreach ($strings as $testcase) {
    if (ctype_xdigit($testcase)) {
        echo "The string $testcase consists of all hexadecimal digits.\n";
    } else {
        echo "The string $testcase does not consist of all hexadecimal digits.\n";
    }
}
?>
```

以上例程会输出：

    The string AB10BC99 consists of all hexadecimal digits.
    The string AR1012 does not consist of all hexadecimal digits.
    The string ab12bc99 consists of all hexadecimal digits.

### 注释

> **Note**:
>
> 如果给出一个 -128 到 255 之间(含)的整数,
> 将会被解释为该值对应的ASCII字符 (负值将加上 256 以支持扩展ASCII字符).
> 其它整数将会被解释为该值对应的十进制字符串.

### 参见

-   <span class="function">ctype\_digit</span>

**目录**

-   [ctype\_alnum](/ref/ctype.html#ctype_alnum) — 做字母和数字字符检测
-   [ctype\_alpha](/ref/ctype.html#ctype_alpha) — 做纯字符检测
-   [ctype\_cntrl](/ref/ctype.html#ctype_cntrl) — 做控制字符检测
-   [ctype\_digit](/ref/ctype.html#ctype_digit) — 做纯数字检测
-   [ctype\_graph](/ref/ctype.html#ctype_graph) —
    做可打印字符串检测，空格除外
-   [ctype\_lower](/ref/ctype.html#ctype_lower) — 做小写字符检测
-   [ctype\_print](/ref/ctype.html#ctype_print) — 做可打印字符检测
-   [ctype\_punct](/ref/ctype.html#ctype_punct) —
    检测可打印的字符是不是不包含空白、数字和字母
-   [ctype\_space](/ref/ctype.html#ctype_space) — 做空白字符检测
-   [ctype\_upper](/ref/ctype.html#ctype_upper) — 做大写字母检测
-   [ctype\_xdigit](/ref/ctype.html#ctype_xdigit) —
    检测字符串是否只包含十六进制字符
