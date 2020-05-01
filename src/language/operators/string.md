字符串运算符
------------

有两个字符串（<span
class="type">string</span>）运算符。第一个是连接运算符（“.”），它返回其左右参数连接后的字符串。第二个是连接赋值运算符（“*.=*”），它将右边参数附加到左边的参数之后。更多信息见<a href="/language/operators/assignment.html" class="link">赋值运算符</a>。

``` php
<?php
$a = "Hello ";
$b = $a . "World!"; // now $b contains "Hello World!"

$a = "Hello ";
$a .= "World!";     // now $a contains "Hello World!"
?>
```

参见<a href="/language/types/string.html" class="link">字符串类型</a>和<a href="/ref/strings.html" class="link">字符串函数</a>章节。
