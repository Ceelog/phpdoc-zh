preg\_filter
============

执行一个正则表达式搜索和替换

### 说明

<span class="type">mixed</span> <span
class="methodname">preg\_filter</span> ( <span class="methodparam"><span
class="type">mixed</span> `$pattern`</span> , <span
class="methodparam"><span class="type">mixed</span>
`$replacement`</span> , <span class="methodparam"><span
class="type">mixed</span> `$subject`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$count`</span> \]\]
)

<span class="function">preg\_filter</span>等价于<span
class="function">preg\_replace</span>
除了它仅仅返回(可能经过转化)与目标匹配的结果.
这个函数怎样工作的更详细信息请阅读 <span
class="function">preg\_replace</span>文档.

### 返回值

如果`subject`是一个<span class="type">数组</span>，返回一个<span
class="type">数组</span>， 其他情况返回一个<span
class="type">字符串</span>。

如果没有找到匹配或者发生了错误，当`subject`是<span
class="type">数组</span> 时返回一个空<span
class="type">数组</span>，其他情况返回**`NULL`**。

### 范例

**示例 \#1 比较<span class="function">preg\_filter</span> 和<span
class="function">preg\_replace</span>的示例**

``` php
<?php
$subject = array('1', 'a', '2', 'b', '3', 'A', 'B', '4'); 
$pattern = array('/\d/', '/[a-z]/', '/[1a]/'); 
$replace = array('A:$0', 'B:$0', 'C:$0'); 

echo "preg_filter returns\n";
print_r(preg_filter($pattern, $replace, $subject)); 

echo "preg_replace returns\n";
print_r(preg_replace($pattern, $replace, $subject)); 
?>
```

以上例程会输出：

    preg_filter returns
    Array
    (
        [0] => A:C:1
        [1] => B:C:a
        [2] => A:2
        [3] => B:b
        [4] => A:3
        [7] => A:4
    )
    preg_replace returns
    Array
    (
        [0] => A:C:1
        [1] => B:C:a
        [2] => A:2
        [3] => B:b
        [4] => A:3
        [5] => A
        [6] => B
        [7] => A:4
    )

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_replace\_callback</span>
-   <span class="function">preg\_grep</span>
-   <span class="function">preg\_last\_error</span>

preg\_grep
==========

返回匹配模式的数组条目

### 说明

<span class="type">array</span> <span
class="methodname">preg\_grep</span> ( <span class="methodparam"><span
class="type">string</span> `$pattern`</span> , <span
class="methodparam"><span class="type">array</span> `$input`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

返回给定数组`input`中与模式`pattern` 匹配的元素组成的数组.

### 参数

`pattern`  
要搜索的模式, 字符串形式.

`input`  
输入数组.

`flags`  
如果设置为**`PREG_GREP_INVERT`**, 这个函数返回输入数组中与
给定模式`pattern`*不*匹配的元素组成的数组.

### 返回值

返回使用`input`中key做索引的数组.

### 范例

**示例 \#1 <span class="function">preg\_grep</span> 示例**

``` php
<?php
// 返回所有包含浮点数的元素
$fl_array = preg_grep("/^(\d+)?\.\d+$/", $array);
?>
```

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_match\_all</span>
-   <span class="function">preg\_filter</span>
-   <span class="function">preg\_last\_error</span>

preg\_last\_error
=================

返回最后一个PCRE正则执行产生的错误代码

### 说明

<span class="type">int</span> <span
class="methodname">preg\_last\_error</span> ( <span
class="methodparam">void</span> )

返回最后一次PCRE正则执行的错误代码。

**示例 \#1 <span class="function">preg\_last\_error</span> 示例**

``` php
<?php

preg_match('/(?:\D+|<\d+>)*[!?]/', 'foobar foobar foobar');

if (preg_last_error() == PREG_BACKTRACK_LIMIT_ERROR) {
    print 'Backtrack limit was exhausted!';
}

?>
```

以上例程会输出：

    Backtrack limit was exhausted!

### 返回值

返回下面常量中的一个(<a href="/pcre/constants.html" class="link">查看它们自身的解释</a>):

-   **`PREG_NO_ERROR`**
-   **`PREG_INTERNAL_ERROR`**
-   **`PREG_BACKTRACK_LIMIT_ERROR`** （参见
    <a href="/pcre/setup.html#" class="link">pcre.backtrack_limit</a>）
-   **`PREG_RECURSION_LIMIT_ERROR`** （参见
    <a href="/pcre/setup.html#" class="link">pcre.recursion_limit</a>）
-   **`PREG_BAD_UTF8_ERROR`**
-   **`PREG_BAD_UTF8_OFFSET_ERROR`** （自 PHP 5.3.0 起）
-   **`PREG_JIT_STACKLIMIT_ERROR`** (自 PHP 7.0.0 起)

preg\_match\_all
================

执行一个全局正则表达式匹配

### 说明

<span class="type">int</span> <span
class="methodname">preg\_match\_all</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">string</span>
`$subject`</span> \[, <span class="methodparam"><span
class="type">array</span> `&$matches`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = **`PREG_PATTERN_ORDER`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \]\]\] )

搜索`subject`中所有匹配`pattern`给定正则表达式
的匹配结果并且将它们以`flag`指定顺序输出到`matches`中.

在第一个匹配找到后, 子序列继续从最后一次匹配位置搜索.

### 参数

`pattern`  
要搜索的模式，字符串形式。

`subject`  
输入字符串。

`matches`  
多维数组，作为输出参数输出所有匹配结果, 数组排序通过`flags`指定。

`flags`  
可以结合下面标记使用(注意不能同时使用**`PREG_PATTERN_ORDER`**和
**`PREG_SET_ORDER`**)：

**`PREG_PATTERN_ORDER`**  
结果排序为`$matches[0]`保存完整模式的所有匹配, `$matches[1]`
保存第一个子组的所有匹配，以此类推。

``` php
<?php
preg_match_all("|<[^>]+>(.*)</[^>]+>|U",
    "<b>example: </b><div align=left>this is a test</div>",
    $out, PREG_PATTERN_ORDER);
echo $out[0][0] . ", " . $out[0][1] . "\n";
echo $out[1][0] . ", " . $out[1][1] . "\n";
?>
```

以上例程会输出：

    <b>example: </b>, <div align=left>this is a test</div>
    example: , this is a test

因此, `$out[0]`是包含匹配完整模式的字符串的数组，
`$out[1]`是包含闭合标签内的字符串的数组。

如果正则表达式包含了带名称的子组，`$matches` 额外包含了带名称子组的键。

如果正则表达式里，子组名称重名了，则仅最右侧的自组储存在
`$matches[NAME]` 中。

``` php
<?php
preg_match_all(
    '/(?J)(?<match>foo)|(?<match>bar)/',
    'foo bar',
    $matches,
    PREG_PATTERN_ORDER
);
print_r($matches['match']);
?>
```

以上例程会输出：

    Array
    (
        [0] => 
        [1] => bar
    )

**`PREG_SET_ORDER`**  
结果排序为`$matches[0]`包含第一次匹配得到的所有匹配(包含子组)，
`$matches[1]`是包含第二次匹配到的所有匹配(包含子组)的数组，以此类推。

``` php
<?php
preg_match_all("|<[^>]+>(.*)</[^>]+>|U",
    "<b>example: </b><div align=\"left\">this is a test</div>",
    $out, PREG_SET_ORDER);
echo $out[0][0] . ", " . $out[0][1] . "\n";
echo $out[1][0] . ", " . $out[1][1] . "\n";
?>
```

以上例程会输出：

    <b>example: </b>, example:
    <div align="left">this is a test</div>, this is a test

**`PREG_OFFSET_CAPTURE`**  
如果这个标记被传递，每个发现的匹配返回时会增加它相对目标字符串的偏移量。
注意这会改变`matches`中的每一个匹配结果字符串元素，使其
成为一个第*0*个元素为匹配结果字符串，第*1*个元素为
匹配结果字符串在`subject`中的偏移量。

``` php
<?php
preg_match_all('/(foo)(bar)(baz)/', 'foobarbaz', $matches, PREG_OFFSET_CAPTURE);
print_r($matches);
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [0] => Array
                    (
                        [0] => foobarbaz
                        [1] => 0
                    )

            )

        [1] => Array
            (
                [0] => Array
                    (
                        [0] => foo
                        [1] => 0
                    )

            )

        [2] => Array
            (
                [0] => Array
                    (
                        [0] => bar
                        [1] => 3
                    )

            )

        [3] => Array
            (
                [0] => Array
                    (
                        [0] => baz
                        [1] => 6
                    )

            )

    )

如果没有给定排序标记，假定设置为**`PREG_PATTERN_ORDER`**。

`offset`  
通常， 查找时从目标字符串的开始位置开始。可选参数`offset`用于
从目标字符串中指定位置开始搜索(单位是字节)。

> **Note**:
>
> 使用 `offset` 参数不同于传递 *substr($subject, $offset)* 的 结果到
> <span class="function">preg\_match\_all</span> 作为目标字符串，因为
> `pattern` 可以包含断言比如*^*， *$* 或者 *(?\<=x)* 。 示例查看 <span
> class="function">preg\_match</span>。

### 返回值

返回完整匹配次数（可能是0），或者如果发生错误返回**`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                       |
|-------|------------------------------------------------------------------------------------------------------------|
| 5.4.0 | 参数`matches`成为可选的。                                                                                  |
| 5.3.6 | 如果 `offset` 大于 `subject` 的程度，将返回 **`FALSE`**。                                                  |
| 5.2.2 | 子命名分组语法可以接受*(?\<name\>)*，*(?'name')*以及 *(?P\<name\>)*了。 之前版本仅接受*(?P\<name\>)*方式。 |

### 范例

**示例 \#1 查找所有文本中的电话号码。**

``` php
<?php
preg_match_all("/\(?  (\d{3})?  \)?  (?(1)  [\-\s] ) \d{3}-\d{4}/x",
                "Call 555-1212 or 1-800-555-1212", $phones);
?>
```

**示例 \#2 查找匹配的HTML标签（贪婪）**

``` php
<?php
//\\2是一个后向引用的示例. 这会告诉pcre它必须匹配正则表达式中第二个圆括号(这里是([\w]+))
//匹配到的结果. 这里使用两个反斜线是因为这里使用了双引号.
$html = "<b>bold text</b><a href=howdy.html>click me</a>";

preg_match_all("/(<([\w]+)[^>]*>)(.*?)(<\/\\2>)/", $html, $matches, PREG_SET_ORDER);

foreach ($matches as $val) {
    echo "matched: " . $val[0] . "\n";
    echo "part 1: " . $val[1] . "\n";
    echo "part 2: " . $val[2] . "\n";
    echo "part 3: " . $val[3] . "\n";
    echo "part 4: " . $val[4] . "\n\n";
}
?>
```

以上例程会输出：

    matched: <b>bold text</b>
    part 1: <b>
    part 2: b
    part 3: bold text
    part 4: </b>

    matched: <a href=howdy.html>click me</a>
    part 1: <a href=howdy.html>
    part 2: a
    part 3: click me
    part 4: </a>

**示例 \#3 使用子命名组**

``` php
<?php

$str = <<<FOO
a: 1
b: 2
c: 3
FOO;

preg_match_all('/(?P<name>\w+): (?P<digit>\d+)/', $str, $matches);

/* 下面代码在php 5.2.2(pcre 7.0)或更高版本下工作, 不过, 为了向后兼容
 * 推荐使用上面的方式. */
// preg_match_all('/(?<name>\w+): (?<digit>\d+)/', $str, $matches);

print_r($matches);

?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [0] => a: 1
                [1] => b: 2
                [2] => c: 3
            )

        [name] => Array
            (
                [0] => a
                [1] => b
                [2] => c
            )

        [1] => Array
            (
                [0] => a
                [1] => b
                [2] => c
            )

        [digit] => Array
            (
                [0] => 1
                [1] => 2
                [2] => 3
            )

        [2] => Array
            (
                [0] => 1
                [1] => 2
                [2] => 3
            )

    )

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 匹配</a>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_match</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_split</span>
-   <span class="function">preg\_last\_error</span>

preg\_match
===========

执行匹配正则表达式

### 说明

<span class="type">int</span> <span
class="methodname">preg\_match</span> ( <span class="methodparam"><span
class="type">string</span> `$pattern`</span> , <span
class="methodparam"><span class="type">string</span> `$subject`</span>
\[, <span class="methodparam"><span class="type">array</span>
`&$matches`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \]\]\] )

搜索`subject`与`pattern`给定的正则表达式的一个匹配.

### 参数

`pattern`  
要搜索的模式，字符串类型。

`subject`  
输入字符串。

`matches`  
如果提供了参数`matches`，它将被填充为搜索结果。
`$matches[0]`将包含完整模式匹配到的文本， `$matches[1]`
将包含第一个捕获子组匹配到的文本，以此类推。

`flags`  
`flags`可以被设置为以下标记值：

**`PREG_OFFSET_CAPTURE`**  
如果传递了这个标记，对于每一个出现的匹配返回时会附加字符串偏移量(相对于目标字符串的)。
注意：这会改变填充到`matches`参数的数组，使其每个元素成为一个由
第*0*个元素是匹配到的字符串，第*1*个元素是该匹配字符串
在目标字符串`subject`中的偏移量。

``` php
<?php
preg_match('/(foo)(bar)(baz)/', 'foobarbaz', $matches, PREG_OFFSET_CAPTURE);
print_r($matches);
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [0] => foobarbaz
                [1] => 0
            )

        [1] => Array
            (
                [0] => foo
                [1] => 0
            )

        [2] => Array
            (
                [0] => bar
                [1] => 3
            )

        [3] => Array
            (
                [0] => baz
                [1] => 6
            )

    )

`offset`  
通常，搜索从目标字符串的开始位置开始。可选参数 `offset` 用于
指定从目标字符串的某个位置开始搜索(单位是字节)。

> **Note**:
>
> 使用`offset`参数不同于向<span class="function">preg\_match</span>
> 传递按照位置通过*substr($subject, $offset)*截取目标字符串结果，
> 因为`pattern`可以包含断言比如*^*， *$* 或者*(?\<=x)*。 比较：
>
> ``` php
> <?php
> $subject = "abcdef";
> $pattern = '/^def/';
> preg_match($pattern, $subject, $matches, PREG_OFFSET_CAPTURE, 3);
> print_r($matches);
> ?>
> ```
>
> 以上例程会输出：
>
>     Array
>     (
>     )
>
> 当这个示例使用截取后传递时
>
> ``` php
> <?php
> $subject = "abcdef";
> $pattern = '/^def/';
> preg_match($pattern, substr($subject,3), $matches, PREG_OFFSET_CAPTURE);
> print_r($matches);
> ?>
> ```
>
> 将会产生匹配
>
>     Array
>     (
>         [0] => Array
>             (
>                 [0] => def
>                 [1] => 0
>             )
>
>     )

### 返回值

<span class="function">preg\_match</span>返回 `pattern` 的匹配次数。
它的值将是0次（不匹配）或1次，因为<span
class="function">preg\_match</span>在第一次匹配后 将会停止搜索。<span
class="function">preg\_match\_all</span>不同于此，它会一直搜索`subject`
直到到达结尾。 如果发生错误<span class="function">preg\_match</span>返回
**`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                   |
|-------|--------------------------------------------------------------------------------------------------------|
| 5.3.6 | 如果 `offset` 比 `subject` 的长度还要大则返回 **`FALSE`**。                                            |
| 5.2.2 | 命名子组可以接受*(?\<name\>)*， *(?'name')* 以及*(?P\<name\>)*语法。之前版本仅接受*(?P\<name\>)*语法。 |

### 范例

**示例 \#1 查找文本字符串"php"**

``` php
<?php
//模式分隔符后的"i"标记这是一个大小写不敏感的搜索
if (preg_match("/php/i", "PHP is the web scripting language of choice.")) {
    echo "A match was found.";
} else {
    echo "A match was not found.";
}
?>
```

**示例 \#2 查找单词"word"**

``` php
<?php
/* 模式中的\b标记一个单词边界，所以只有独立的单词"web"会被匹配，而不会匹配
 * 单词的部分内容比如"webbing" 或 "cobweb" */
if (preg_match("/\bweb\b/i", "PHP is the web scripting language of choice.")) {
    echo "A match was found.";
} else {
    echo "A match was not found.";
}

if (preg_match("/\bweb\b/i", "PHP is the website scripting language of choice.")) {
    echo "A match was found.";
} else {
    echo "A match was not found.";
}
?>
```

**示例 \#3 获取URL中的域名**

``` php
<?php
//从URL中获取主机名称
preg_match('@^(?:http://)?([^/]+)@i',
    "http://www.php.net/index.html", $matches);
$host = $matches[1];

//获取主机名称的后面两部分
preg_match('/[^.]+\.[^.]+$/', $host, $matches);
echo "domain name is: {$matches[0]}\n";
?>
```

以上例程会输出：

    domain name is: php.net

**示例 \#4 使用命名子组**

``` php
<?php

$str = 'foobar: 2008';

preg_match('/(?P<name>\w+): (?P<digit>\d+)/', $str, $matches);

/* 下面例子在php 5.2.2(pcre 7.0)或更新版本下工作, 然而, 为了后向兼容, 上面的方式是推荐写法. */
// preg_match('/(?<name>\w+): (?<digit>\d+)/', $str, $matches);

print_r($matches);

?>
```

以上例程会输出：

    Array
    (
        [0] => foobar: 2008
        [name] => foobar
        [1] => foobar
        [digit] => 2008
        [2] => 2008
    )

### 注释

**小贴士**

如果你仅仅想要检查某个字符串是否包含另外一个字符串，不要使用<span
class="function">preg\_match</span>。 使用 <span
class="function">strpos</span> 会更快。

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_match\_all</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_split</span>
-   <span class="function">preg\_last\_error</span>

preg\_quote
===========

转义正则表达式字符

### 说明

<span class="type">string</span> <span
class="methodname">preg\_quote</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = **`NULL`**</span></span> \] )

<span class="function">preg\_quote</span>需要参数 `str` 并向其中
每个正则表达式语法中的字符前增加一个反斜线。
这通常用于你有一些运行时字符串 需要作为正则表达式进行匹配的时候。

正则表达式特殊字符有： *. \\ + \* ? \[ ^ \] $ ( ) { } = ! \< \> \| : -*

注意 */* 不是正则表达式特殊字符。

> **Note**:
>
> 注意：<span class="function">preg\_quote</span> 的应用场景不是用于
> <span class="function">preg\_replace</span> 的 $replacement
> 字符串参数。

### 参数

`str`  
输入字符串

`delimiter`  
如果指定了可选参数 `delimiter`，它也会被转义。这通常用于
转义PCRE函数使用的分隔符。 */* 是最常见的分隔符。

### 返回值

返回转义后的字符串。

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 5.3.0 | 字符 *-* 被增加为需要转义的。 |

### 范例

**示例 \#1 <span class="function">preg\_quote</span>示例**

``` php
<?php
$keywords = '$40 for a g3/400';
$keywords = preg_quote($keywords, '/');
echo $keywords; // 返回 \$40 for a g3\/400
?>
```

**示例 \#2 将文本中的单词替换为斜体**

``` php
<?php
//在这个例子中，preg_quote($word) 用于保持星号原文涵义，使其不使用正则表达式中的特殊语义。

$textbody = "This book is *very* difficult to find.";
$word = "*very*";
$textbody = preg_replace ("/" . preg_quote($word, '/') . "/",
                          "<i>" . $word . "</i>",
                          $textbody);
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">escapeshellcmd</span>

preg\_replace\_callback\_array
==============================

Perform a regular expression search and replace using callbacks

### 说明

<span class="type">mixed</span> <span
class="methodname">preg\_replace\_callback\_array</span> ( <span
class="methodparam"><span class="type">array</span>
`$patterns_and_callbacks`</span> , <span class="methodparam"><span
class="type">mixed</span> `$subject`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$count`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\]\] )

The behavior of this function is similar to <span
class="function">preg\_replace\_callback</span>, except that callbacks
are executed on a per-pattern basis.

### 参数

`patterns_and_callbacks`  
An associative array mapping patterns (keys) to callbacks (values).

`subject`  
The string or an array with strings to search and replace.

`limit`  
The maximum possible replacements for each pattern in each `subject`
string. Defaults to *-1* (no limit).

`count`  
If specified, this variable will be filled with the number of
replacements done.

`flags`  
`flags` can be a combination of the **`PREG_OFFSET_CAPTURE`** and
**`PREG_UNMATCHED_AS_NULL`** flags, which influence the format of the
matches array. See the description in <span
class="function">preg\_match</span> for more details.

### 返回值

<span class="function">preg\_replace\_callback\_array</span> returns an
array if the `subject` parameter is an array, or a string otherwise. On
errors the return value is **`NULL`**

If matches are found, the new subject will be returned, otherwise
`subject` will be returned unchanged.

### 更新日志

| 版本  | 说明                             |
|-------|----------------------------------|
| 7.4.0 | The `flags` parameter was added. |

### 范例

**示例 \#1 <span class="function">preg\_replace\_callback\_array</span>
example**

``` php
<?php
$subject = 'Aaaaaa Bbb';

preg_replace_callback_array(
    [
        '~[a]+~i' => function ($match) {
            echo strlen($match[0]), ' matches for "a" found', PHP_EOL;
        },
        '~[b]+~i' => function ($match) {
            echo strlen($match[0]), ' matches for "b" found', PHP_EOL;
        }
    ],
    $subject
);
?>
```

以上例程会输出：

    6 matches for "a" found
    3 matches for "b" found

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE Patterns</a>
-   <span class="function">preg\_replace\_callback</span>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_last\_error</span>
-   <a href="/functions/anonymous.html" class="link">Anonymous functions</a>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

preg\_replace\_callback
=======================

执行一个正则表达式搜索并且使用一个回调进行替换

### 说明

<span class="type">mixed</span> <span
class="methodname">preg\_replace\_callback</span> ( <span
class="methodparam"><span class="type">mixed</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">mixed</span> `$subject`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$count`</span> \]\]
)

这个函数的行为除了可以指定一个 `callback` 替代 `replacement`
进行替换字符串的计算，其他方面等同于 <span
class="function">preg\_replace</span>。

### 参数

`pattern`  
要搜索的模式，可以是字符串或一个字符串数组。

`callback`  
一个回调函数，在每次需要替换时调用，调用时函数得到的参数是从 `subject`
中匹配到的结果。回调函数返回真正参与替换的字符串。这是该回调函数的签名：

<span class="type">string</span> <span class="methodname"><span
class="replaceable">handler</span></span> ( <span
class="methodparam"><span class="type">array</span> `$matches`</span> )

经常会需要 `callback` 函数而仅用于 <span
class="function">preg\_replace\_callback</span>
一个地方的调用。在这种情况下，你可以使用
<a href="/functions/anonymous.html" class="link">匿名函数</a>
来定义一个匿名函数作为 <span
class="function">preg\_replace\_callback</span> 调用时的回调。
这样做你可以保留所有调用信息在同一个位置并且不会因为一个不在任何其他地方使用的回调函数名称而污染函数名称空间。

**示例 \#1 <span class="function">preg\_replace\_callback</span> 和
匿名函数**

``` php
<?php
/* 一个unix样式的命令行过滤器，用于将段落开始部分的大写字母转换为小写。 */
$fp = fopen("php://stdin", "r") or die("can't read stdin");
while (!feof($fp)) {
    $line = fgets($fp);
    $line = preg_replace_callback(
        '|<p>\s*\w|',
        function ($matches) {
            return strtolower($matches[0]);
        },
        $line
    );
    echo $line;
}
fclose($fp);
?>
```

`subject`  
要搜索替换的目标字符串或字符串数组。

`limit`  
对于每个模式用于每个 `subject` 字符串的最大可替换次数。 默认是
*-1*（无限制）。

`count`  
如果指定，这个变量将被填充为替换执行的次数。

### 返回值

如果 `subject` 是一个数组， <span
class="function">preg\_replace\_callback</span>
返回一个数组，其他情况返回字符串。错误发生时返回 **`NULL`**。

如果查找到了匹配，返回替换后的目标字符串（或字符串数组），其他情况
`subject` 将会无变化返回。

### 更新日志

| 版本  | 说明                |
|-------|---------------------|
| 7.4.0 | 新增 `flags` 参数。 |

### 范例

**示例 \#2 <span class="function">preg\_replace\_callback</span>示例**

``` php
<?php
// 将文本中的年份增加一年.
$text = "April fools day is 04/01/2002\n";
$text.= "Last christmas was 12/24/2001\n";
// 回调函数
function next_year($matches)
{
  // 通常: $matches[0]是完成的匹配
  // $matches[1]是第一个捕获子组的匹配
  // 以此类推
  return $matches[1].($matches[2]+1);
}
echo preg_replace_callback(
            "|(\d{2}/\d{2}/)(\d{4})|",
            "next_year",
            $text);

?>
```

以上例程会输出：

    April fools day is 04/01/2003
    Last christmas was 12/24/2002

**示例 \#3 <span class="function">preg\_replace\_callback</span>
使用递归构造处理 BB 码的封装**

``` php
<?php
$input = "plain [indent] deep [indent] deeper [/indent] deep [/indent] plain";

function parseTagsRecursive($input)
{
     /* 译注: 对此正则表达式分段分析
     * 首尾两个#是正则分隔符
     * \[indent] 匹配一个原文的[indent]
     * ((?:[^[]|\[(?!/?indent])|(?R))+)分析:
     *   (?:[^[]|\[(?!/?indent])分析:
     *  首先它是一个非捕获子组
     *   两个可选路径, 一个是非[字符, 另一个是[字符但后面紧跟着不是/indent或indent.
     *   (?R) 正则表达式递归
     *     \[/indent] 匹配结束的[/indent]
     * /

    $regex = '#\[indent]((?:[^[]|\[(?!/?indent])|(?R))+)\[/indent]#';

    if (is_array($input)) {
        $input = '<div style="margin-left: 10px">'.$input[1].'</div>';
    }

    return preg_replace_callback($regex, 'parseTagsRecursive', $input);
}

$output = parseTagsRecursive($input);

echo $output;
?>
```

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">preg\_replace\_callback\_array</span>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_last\_error</span>
-   <a href="/functions/anonymous.html" class="link">匿名函数</a>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

preg\_replace
=============

执行一个正则表达式的搜索和替换

### 说明

<span class="type">mixed</span> <span
class="methodname">preg\_replace</span> ( <span
class="methodparam"><span class="type">mixed</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$replacement`</span> , <span class="methodparam"><span
class="type">mixed</span> `$subject`</span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$count`</span> \]\]
)

搜索 `subject` 中匹配 `pattern` 的部分，以 `replacement` 进行替换。

### 参数

`pattern`  
要搜索的模式。可以使一个字符串或字符串数组。

可以使用一些
<a href="/pcre/pattern.html#正则表达式模式中可用的模式修饰符" class="link">PCRE 修饰符</a>。

`replacement`  
用于替换的字符串或字符串数组。如果这个参数是一个字符串，并且 `pattern`
是一个数组，那么所有的模式都使用这个字符串进行替换。如果 `pattern` 和
`replacement` 都是数组，每个 `pattern` 使用 `replacement`
中对应的元素进行替换。如果 `replacement` 中的元素比 `pattern`
中的少，多出来的 `pattern` 使用空字符串进行替换。

`replacement` 中可以包含后向引用 *\\\\<span
class="replaceable">n</span>* 或 *$<span
class="replaceable">n</span>*，语法上首选后者。
每个这样的引用将被匹配到的第 <span class="replaceable">n</span>
个捕获子组捕获到的文本替换。 <span class="replaceable">n</span>
可以是0-99，*\\\\0* 和 *$0*
代表完整的模式匹配文本。捕获子组的序号计数方式为：代表捕获子组的左括号从左到右，
从1开始数。如果要在 `replacement` 中使用反斜线，必须使用 4
个(*"\\\\\\\\"*，译注：因为这首先是 PHP
的字符串，经过转义后，是两个，再经过正则表达式引擎后才被认为是一个原文反斜线)。

当在替换模式下工作并且后向引用后面紧跟着需要是另外一个数字
(比如：在一个匹配模式后紧接着增加一个原文数字)，不能使用 *\\\\1*
这样的语法来描述后向引用。比如，*\\\\11*将会使<span
class="function">preg\_replace</span> 不能理解你希望的是一个 *\\\\1*
后向引用紧跟一个原文 *1*，还是一个 *\\\\11* 后向引用后面不跟任何东西。
这种情况下解决方案是使用 *${1}1*。这创建了一个独立的 *$1* 后向引用,
一个独立的原文 *1*。

当使用被弃用的 *e* 修饰符时, 这个函数会转义一些字符 (即：*'*、*"*、 *\\*
和 NULL)
然后进行后向引用替换。当这些完成后请确保后向引用解析完后没有单引号或双引号引起的语法错误
(比如： *'strlen(\\'$1\\')+strlen("$2")'*)。确保符合 PHP 的
<a href="/language/types/string.html" class="link">字符串语法</a>，并且符合
eval 语法。因为在完成替换后，引擎会将结果字符串作为 PHP 代码使用 eval
方式进行评估并将返回值作为最终参与替换的字符串。

`subject`  
要进行搜索和替换的字符串或字符串数组。

如果 `subject` 是一个数组，搜索和替换回在 `subject` 的每一个元素上进行,
并且返回值也会是一个数组。

`limit`  
每个模式在每个 `subject` 上进行替换的最大次数。默认是 *-1*(无限)。

`count`  
如果指定，将会被填充为完成的替换次数。

### 返回值

如果 `subject` 是一个数组，<span class="function">preg\_replace</span>
返回一个数组，其他情况下返回一个字符串。

如果匹配被查找到，替换后的 `subject` 被返回，其他情况下返回没有改变的
`subject`。如果发生错误，返回 **`NULL`** 。

### 错误／异常

PHP 5.5.0 起， 传入 "\\e" 修饰符的时候，会产生一个 **`E_DEPRECATED`**
错误； PHP 7.0.0 起，会产生 **`E_WARNING`** 错误，同时 "\\e"
也无法起效。

### 范例

**示例 \#1 使用后向引用紧跟数值原文**

``` php
<?php
$string = 'April 15, 2003';
$pattern = '/(\w+) (\d+), (\d+)/i';
$replacement = '${1}1,$3';
echo preg_replace($pattern, $replacement, $string);
?>
```

以上例程会输出：

    April1,2003

**示例 \#2 <span class="function">preg\_replace</span>
中使用基于索引的数组**

``` php
<?php
$string = 'The quick brown fox jumps over the lazy dog.';
$patterns = array();
$patterns[0] = '/quick/';
$patterns[1] = '/brown/';
$patterns[2] = '/fox/';
$replacements = array();
$replacements[2] = 'bear';
$replacements[1] = 'black';
$replacements[0] = 'slow';
echo preg_replace($patterns, $replacements, $string);
?>
```

以上例程会输出：

    The bear black slow jumps over the lazy dog.

对模式和替换内容按 key 进行排序我们可以得到期望的结果。

``` php
<?php
ksort($patterns);
ksort($replacements);
echo preg_replace($patterns, $replacements, $string);
?>
```

以上例程会输出：

    The slow black bear jumps over the lazy dog.

**示例 \#3 替换一些值**

``` php
<?php
$patterns = array ('/(19|20)(\d{2})-(\d{1,2})-(\d{1,2})/',
                   '/^\s*{(\w+)}\s*=/');
$replace = array ('\3/\4/\1\2', '$\1 =');
echo preg_replace($patterns, $replace, '{startDate} = 1999-5-27');
?>
```

以上例程会输出：

    $startDate = 5/27/1999

**示例 \#4 剥离空白字符**

这个例子剥离多余的空白字符

``` php
<?php
$str = 'foo   o';
$str = preg_replace('/\s\s+/', ' ', $str);
// 将会改变为'foo o'
echo $str;
?>
```

**示例 \#5 使用参数 `count`**

``` php
<?php
$count = 0;

echo preg_replace(array('/\d/', '/\s/'), '*', 'xp 4 to', -1 , $count);
echo $count; //3
?>
```

以上例程会输出：

    xp***to
    3

### 注释

> **Note**:
>
> 当使用数组形式的`pattern`和`replacement`时,
> 将会按照key在数组中出现的顺序进行处理. 这*不一定*和数组的索引顺序一致.
> 如果你期望使用索引对等方式用`replacement`对`pattern` 进行替换,
> 你可以在调用<span
> class="function">preg\_replace</span>之前对两个数组各进行一次<span
> class="function">ksort</span>排序.

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">preg\_quote</span>
-   <span class="function">preg\_filter</span>
-   <span class="function">preg\_match</span>
-   <span class="function">preg\_replace\_callback</span>
-   <span class="function">preg\_split</span>
-   <span class="function">preg\_last\_error</span>

preg\_split
===========

通过一个正则表达式分隔字符串

### 说明

<span class="type">array</span> <span
class="methodname">preg\_split</span> ( <span class="methodparam"><span
class="type">string</span> `$pattern`</span> , <span
class="methodparam"><span class="type">string</span> `$subject`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

通过一个正则表达式分隔给定字符串.

### 参数

`pattern`  
用于搜索的模式，字符串形式。

`subject`  
输入字符串

`limit`  
如果指定，将限制分隔得到的子串最多只有`limit`个，返回的最后一个
子串将包含所有剩余部分。`limit`值为-1， 0或null时都代表"不限制"，
作为php的标准，你可以使用null跳过对`flags`的设置。

`flags`  
`flags `可以是任何下面标记的组合(以位或运算 *\|* 组合)：

**`PREG_SPLIT_NO_EMPTY`**  
<span class="simpara"> 如果这个标记被设置， <span
class="function">preg\_split</span> 将仅返回分隔后的非空部分。 </span>

**`PREG_SPLIT_DELIM_CAPTURE`**  
<span class="simpara">
如果这个标记设置了，用于分隔的模式中的括号表达式将被捕获并返回。 </span>

**`PREG_SPLIT_OFFSET_CAPTURE`**  
如果这个标记被设置, 对于每一个出现的匹配返回时将会附加字符串偏移量.
注意：这将会改变返回数组中的每一个元素, 使其每个元素成为一个由第*0*
个元素为分隔后的子串，第*1*个元素为该子串在`subject`
中的偏移量组成的数组。

### 返回值

返回一个使用 `pattern` 边界分隔 `subject` 后得到 的子串组成的数组，
或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="function">preg\_split</span>示例：获取搜索字符串的部分**

``` php
<?php
//使用逗号或空格(包含" ", \r, \t, \n, \f)分隔短语
$keywords = preg_split("/[\s,]+/", "hypertext language, programming");
print_r($keywords);
?>
```

以上例程会输出：

    Array
    (
        [0] => hypertext
        [1] => language
        [2] => programming
    )

**示例 \#2 将一个字符串分隔为组成它的字符**

``` php
<?php
$str = 'string';
$chars = preg_split('//', $str, -1, PREG_SPLIT_NO_EMPTY);
print_r($chars);
?>
```

以上例程会输出：

    Array
    (
        [0] => s
        [1] => t
        [2] => r
        [3] => i
        [4] => n
        [5] => g
    )

**示例 \#3 分隔一个字符串并获取每部分的偏移量**

``` php
<?php
$str = 'hypertext language programming';
$chars = preg_split('/ /', $str, -1, PREG_SPLIT_OFFSET_CAPTURE);
print_r($chars);
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [0] => hypertext
                [1] => 0
            )

        [1] => Array
            (
                [0] => language
                [1] => 10
            )

        [2] => Array
            (
                [0] => programming
                [1] => 19
            )

    )

### 注释

**小贴士**

如果你不需要正则表达式功能，可以有更快(并且更简单)的选择比如 <span
class="function">explode</span> 或 <span
class="function">str\_split</span>。

**小贴士**

如果没有成功匹配，将会返回一个数组，包含了单个元素，即输入的字符串。

### 参见

-   <a href="/pcre/pattern.html" class="link">PCRE 模式</a>
-   <span class="function">preg\_quote</span>
-   <span class="function">implode</span>
-   <span class="function">preg\_match</span>
-   <span class="function">preg\_match\_all</span>
-   <span class="function">preg\_replace</span>
-   <span class="function">preg\_last\_error</span>

**目录**

-   [preg\_filter](/ref/pcre.html#preg_filter) —
    执行一个正则表达式搜索和替换
-   [preg\_grep](/ref/pcre.html#preg_grep) — 返回匹配模式的数组条目
-   [preg\_last\_error](/ref/pcre.html#preg_last_error) —
    返回最后一个PCRE正则执行产生的错误代码
-   [preg\_match\_all](/ref/pcre.html#preg_match_all) —
    执行一个全局正则表达式匹配
-   [preg\_match](/ref/pcre.html#preg_match) — 执行匹配正则表达式
-   [preg\_quote](/ref/pcre.html#preg_quote) — 转义正则表达式字符
-   [preg\_replace\_callback\_array](/ref/pcre.html#preg_replace_callback_array)
    — Perform a regular expression search and replace using callbacks
-   [preg\_replace\_callback](/ref/pcre.html#preg_replace_callback) —
    执行一个正则表达式搜索并且使用一个回调进行替换
-   [preg\_replace](/ref/pcre.html#preg_replace) —
    执行一个正则表达式的搜索和替换
-   [preg\_split](/ref/pcre.html#preg_split) —
    通过一个正则表达式分隔字符串
