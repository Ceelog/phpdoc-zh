**Warning**

This feature was *DEPRECATED* in PHP 5.3.0, and *REMOVED* in PHP 7.0.0.

Alternatives to this feature include:

-   <a href="/book/pcre.html" class="link">PCRE</a>
    （支持完整的正则表达式）
-   <span class="function">fnmatch</span> （支持 shell
    风格通配符的匹配）

ereg\_replace
=============

正则表达式替换

### 说明

<span class="type">string</span> <span
class="methodname">ereg\_replace</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$replacement`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> )

本函数在 `string` 中扫描与 `pattern` 匹配的部分，并将其替换为
`replacement`。

返回替换后的字符串。（如果没有可供替换的匹配项则会返回原字符串。）

如果 `pattern` 包含有括号内的子串，则 `replacement` 可以包含形如
*\\\\<span class="replaceable">digit</span>*
的子串，这些子串将被替换为数字表示的的第几个括号内的子串；*\\\\0*
则包含了字符串的整个内容。最多可以用九个子串。括号可以嵌套，此情形下以左圆括号来计算顺序。

如果未在 `string` 中找到匹配项，则 `string` 将原样返回。

例如，下面的代码片断输出 "This was a test" 三次：

**示例 \#1 <span class="function">ereg\_replace</span> 例子**

``` php
<?php
$string = "This is a test";
echo str_replace(" is", " was", $string);
echo ereg_replace("( )is", "\\1was", $string);
echo ereg_replace("(( )is)", "\\2was", $string);
?>
```

要注意的一点是如果在 `replacement`
参数中使用了整数值，则可能得不到所期望的结果。这是因为 <span
class="function">ereg\_replace</span>
将把数字作为字符的序列值来解释并应用之。例如：

**示例 \#2 <span class="function">ereg\_replace</span> 例子**

``` php
<?php
/* 不能产生出期望的结果 */
$num = 4;
$string = "This string has four words.";
$string = ereg_replace('four', $num, $string);
echo $string;   /* Output: 'This string has   words.' */

/* 本例工作正常 */
$num = '4';
$string = "This string has four words.";
$string = ereg_replace('four', $num, $string);
echo $string;   /* Output: 'This string has 4 words.' */
?>
```

**示例 \#3 将 URL 替换为超连接**

``` php
<?php
$text = ereg_replace("[[:alpha:]]+://[^<>[:space:]]+[[:alnum:]/]",
                     "<a href=\"\\0\">\\0</a>", $text);
?>
```

**小贴士**

<span class="function">preg\_replace</span> 函数使用了 Perl
兼容正则表达式语法，通常是比 <span class="function">ereg\_replace</span>
更快的替代方案。

参见 <span class="function">ereg</span>，<span
class="function">eregi</span>，<span
class="function">eregi\_replace</span>，<span
class="function">str\_replace</span> 和 <span
class="function">preg\_match</span>。

ereg
====

正则表达式匹配

### 说明

<span class="type">int</span> <span class="methodname">ereg</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$regs`</span> \] )

> **Note**:
>
> 使用 Perl 兼容正则表达式语法的 <span
> class="function">preg\_match</span> 函数通常是比 <span
> class="function">ereg</span> 更快的替代方案。

以区分大小写的方式在 `string` 中寻找与给定的正则表达式 `pattern`
所匹配的子串。

如果找到与 `pattern`
中圆括号内的子模式相匹配的子串并且函数调用给出了第三个参数
`regs`，则匹配项将被存入 `regs` 数组中。$regs\[1\]
包含第一个左圆括号开始的子串，$regs\[2\]
包含第二个子串，以此类推。$regs\[0\] 包含整个匹配的字符串。

> **Note**: <span class="simpara"> 直到 PHP 4.1.0 为止，`$regs`
> 将被填充为正好十个单元，即使实际匹配的子串少于十个。这并不影响 <span
> class="function">ereg</span> 匹配更多子串的能力。如果没有找到匹配，则
> *$regs* 不会被 <span class="function">ereg</span> 更改。 </span>

如果在 `string` 中找到 `pattern` 模式的匹配则返回
所匹配字符串的长度，如果没有找到匹配或出错则返回
**`FALSE`**。如果没有传递入可选参数 `regs` 或者所匹配的字符串长度为
0，则本函数返回 1。

以下代码片断接受 ISO 格式的日期（YYYY-MM-DD）然后以 DD.MM.YYYY
格式显示：

**示例 \#1 <span class="function">ereg</span> 例子**

``` php
<?php
if (ereg ("([0-9]{4})-([0-9]{1,2})-([0-9]{1,2})", $date, $regs)) {
    echo "$regs[3].$regs[2].$regs[1]";
} else {
    echo "Invalid date format: $date";
}
?>
```

参见 <span class="function">eregi</span>，<span
class="function">ereg\_replace</span>，<span
class="function">eregi\_replace</span>，<span
class="function">preg\_match</span>，<span
class="function">strpos</span> 和 <span class="function">strstr</span>。

eregi\_replace
==============

不区分大小写的正则表达式替换

### 说明

<span class="type">string</span> <span
class="methodname">eregi\_replace</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$replacement`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> )

本函数和 <span class="function">ereg\_replace</span>
完全相同，只除了在匹配字母字符时忽略大小写的区别。

**示例 \#1 高亮搜索结果**

``` php
<?php
$pattern = '(>[^<]*)('. quotemeta($_GET['search']) .')';
$replacement = '\\1<span class="search">\\2</span>';
$body = eregi_replace($pattern, $replacement, $body);
?>
```

参见 <span class="function">ereg</span>，<span
class="function">eregi</span> 和 <span
class="function">ereg\_replace</span>。

eregi
=====

不区分大小写的正则表达式匹配

### 说明

<span class="type">int</span> <span class="methodname">eregi</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$regs`</span> \] )

本函数和 <span class="function">ereg</span>
完全相同，只除了在匹配字母字符时忽略大小写的区别。

**示例 \#1 <span class="function">eregi</span> 例子**

``` php
<?php
$string = 'XYZ';
   if (eregi('z', $string)) {
    echo "'$string' contains a 'z' or 'Z'!";
}
?>
```

参见 <span class="function">ereg</span>，<span
class="function">ereg\_replace</span>，<span
class="function">eregi\_replace</span>，<span
class="function">stripos</span> 和 <span
class="function">stristr</span>。

split
=====

用正则表达式将字符串分割到数组中

### 说明

<span class="type">array</span> <span class="methodname">split</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`</span> \] )

**小贴士**

<span class="function">preg\_split</span> 函数使用了 Perl
兼容正则表达式语法，通常是比 <span class="function">split</span>
更快的替代方案。如果不需要正则表达式的威力，则使用 <span
class="function">explode</span>
更快，这样就不会招致正则表达式引擎的浪费。

本函数返回一个字符串数组，每个单元为 `string` 经区分大小写的正则表达式
`pattern` 作为边界分割出的子串。如果设定了 `limit`，则返回的数组最多包含
`limit` 个单元，而其中最后一个单元包含了 `string`
中剩余的所有部分。如果出错，则 <span class="function">split</span> 返回
**`FALSE`**。

将 `/etc/passwd` 中的前四个字段分割出来：

**示例 \#1 <span class="function">split</span> 例子**

``` php
<?php
list($user, $pass, $uid, $gid, $extra) =
    split (":", $passwd_line, 5);
?>
```

如果字符串中有 <span class="replaceable">n</span> 个与 `pattern`
匹配的项目，则返回的数组将包含 *<span class="replaceable">n</span>+1*
个单元。例如，如果没有找到
`pattern`，则会返回一个只有一个单元的数组。当然，如果 `string`
为空也是这样。

解析可能用斜线，点，或横线分割的日期：

**示例 \#2 <span class="function">split</span> 例子**

``` php
<?php
// 分隔符可以是斜线，点，或横线
$date = "04/30/1973";
list($month, $day, $year) = split ('[/.-]', $date);
echo "Month: $month; Day: $day; Year: $year<br />\n";
?>
```

想仿效 Perl 中类似的 **@chars = split('', $str)** 行为，请参考 <span
class="function">preg\_split</span> 或 <span
class="function">str\_split</span> 函数中的例子。

注意 `pattern`
是一个正则表达式。如果想要用的分割字符是正则表达式中的特殊字符，要先将其转义。如果觉得
<span class="function">split</span>（或其它任何 regex
函数）行为古怪的话，请阅读包含在 PHP 发行包中 `regex/` 子目录下的
`regex.7` 文件。该文件是手册页面格式，可以用类似 **man
/usr/local/src/regex/regex.7** 的命令来阅读。

参见 <span class="function">preg\_split</span>，<span
class="function">spliti</span>，<span
class="function">str\_split</span>，<span
class="function">explode</span>，<span
class="function">implode</span>，<span
class="function">chunk\_split</span> 和 <span
class="function">wordwrap</span>。

spliti
======

用正则表达式不区分大小写将字符串分割到数组中

### 说明

<span class="type">array</span> <span class="methodname">spliti</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = -1</span></span> \] )

用正则表达式将一个 `string` 分割成数组。

本函数和 <span class="function">split</span>
相同，只除了在匹配字母字符时忽略大小写的区别。

**Warning**

自 PHP 5.3.0 起，已经*废弃*此函数。强烈建议不要应用此函数 。

### 参数

`pattern`  
大小写不敏感的正则表达式。

If you want to split on any of the characters which are considered
special by regular expressions, you'll need to escape them first. If you
think <span class="function">spliti</span> (or any other regex function,
for that matter) is doing something weird, please read the file
`regex.7`, included in the `regex/` subdirectory of the PHP
distribution. It's in manpage format, so you'll want to do something
along the lines of **man /usr/local/src/regex/regex.7** in order to read
it.

`string`  
输入的字符。

`limit`  
如果设置了 `limit`，返回的数组最多会包含 `limit`
个元素，最后一个元素包含了剩下的全部 `string`。

### 返回值

Returns an array of strings, each of which is a substring of `string`
formed by splitting it on boundaries formed by the case insensitive
regular expression `pattern`.

If there are <span class="replaceable">n</span> occurrences of
`pattern`, the returned array will contain *<span
class="replaceable">n</span>+1* items. For example, if there is no
occurrence of `pattern`, an array with only one element will be
returned. Of course, this is also true if `string` is empty. If an error
occurs, <span class="function">spliti</span> returns **`FALSE`**.

### 范例

本例用 'a' 做分隔符来分割一个字符串：

**示例 \#1 <span class="function">spliti</span> 例子**

``` php
<?php
$string = "aBBBaCCCADDDaEEEaGGGA";
$chunks = spliti ("a", $string, 5);
print_r($chunks);
?>
```

以上例程会输出：

    Array
    (
      [0] =>
      [1] => BBB
      [2] => CCC
      [3] => DDD
      [4] => EEEaGGGA
    )

### 注释

> **Note**:
>
> 在 PHP 5.3.0 中，已放弃使用 regex 扩展而建议使用
> <a href="/book/pcre.html" class="link">PCRE 扩展</a>。调用此函数将会发出
> **`E_DEPRECATED`**
> 通知。参见“<a href="/pcre/pattern.html#与%20POSIX%20正则表达式的不同" class="link">差异列表</a>”可帮助你转为使用
> PCRE。

### 参见

-   <span class="function">preg\_split</span>
-   <span class="function">split</span>
-   <span class="function">explode</span>
-   <span class="function">implode</span>

sql\_regcase
============

产生用于不区分大小的匹配的正则表达式

### 说明

<span class="type">string</span> <span
class="methodname">sql\_regcase</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

产生用于不区分大小的匹配的正则表达式

**Warning**

自 PHP 5.3.0 起，已经*废弃*此函数。强烈建议不要应用此函数 。

### 参数

`string`  
输入的字符。

### 返回值

返回与 `string` 相匹配的正则表达式，不论大小写字母。返回的表达式是将
`string`
中的每个字母字符转换为方括号表达式，该方括号表达式包含了该字母的大小写形式。其它字符保留不变。

### 范例

**示例 \#1 <span class="function">sql\_regcase</span> 例子**

``` php
<?php
echo sql_regcase("Foo - bar.");
?>
```

以上例程会输出：

    [Ff][Oo][Oo] - [Bb][Aa][Rr].

可以用于在仅支持区分大小写正则表达式的产品中完成不区分大小写的模式匹配。

### 注释

> **Note**:
>
> 在 PHP 5.3.0 中，已放弃使用 regex 扩展而建议使用
> <a href="/book/pcre.html" class="link">PCRE 扩展</a>。调用此函数将会发出
> **`E_DEPRECATED`**
> 通知。参见“<a href="/pcre/pattern.html#与%20POSIX%20正则表达式的不同" class="link">差异列表</a>”可帮助你转为使用
> PCRE。

**目录**

-   [ereg\_replace](/ref/regex.html#ereg_replace) — 正则表达式替换
-   [ereg](/ref/regex.html#ereg) — 正则表达式匹配
-   [eregi\_replace](/ref/regex.html#eregi_replace) —
    不区分大小写的正则表达式替换
-   [eregi](/ref/regex.html#eregi) — 不区分大小写的正则表达式匹配
-   [split](/ref/regex.html#split) — 用正则表达式将字符串分割到数组中
-   [spliti](/ref/regex.html#spliti) —
    用正则表达式不区分大小写将字符串分割到数组中
-   [sql\_regcase](/ref/regex.html#sql_regcase) —
    产生用于不区分大小的匹配的正则表达式
