箭头函数
--------

箭头函数是 PHP 7.4 的新语法，是一种更简洁的
<a href="/functions/anonymous.html" class="link">匿名函数</a> 写法。

匿名函数和箭头函数都是
<a href="/class/closure.html" class="link"><span class="classname">Closure</span></a>
类的实现。

箭头函数的基本语法为 `fn (argument_list) => expr`。

箭头函数支持与
<a href="/functions/anonymous.html" class="link">匿名函数</a>
相同的功能，只是其父作用域的变量总是自动的。

当表达式中使用的变量是在父作用域中定义的，它将被隐式地按值捕获。在下面的例子中，函数
`$fn1` 和 `$fn2` 的行为是一样的。

**示例 \#1 箭头函数自动捕捉变量的值**

``` php
<?php

$y = 1;
 
$fn1 = fn($x) => $x + $y;
// 相当于 using $y by value:
$fn2 = function ($x) use ($y) {
    return $x + $y;
};

var_export($fn1(3));
?>
```

以上例程会输出：

    4

在箭头函数嵌套的情况下同样有效。

**示例 \#2 箭头函数自动捕捉变量的值，即使在嵌套的情况下**

``` php
<?php

$z = 1;
$fn = fn($x) => fn($y) => $x * $y + $z;
// 输出 51
var_export($fn(5)(10));
?>
```

和匿名函数一样，箭头函数语法同样允许标准的函数声明，包括参数和返回类型、缺省值、变量，以及通过引用传递和返回。以下都是箭头函数的有效例子。

**示例 \#3 合法的箭头函数例子**

``` php
<?php

fn(array $x) => $x;
static fn(): int => $x;
fn($x = 42) => $x;
fn(&$x) => $x;
fn&($x) => $x;
fn($x, ...$rest) => $rest;

?>
```

箭头函数会自动绑定上下文变量，这相当于对箭头函数内部使用的每一个变量
`$x` 执行了一个
`use($x)`。这意味着不可能修改外部作用域的任何值，若要实现对值的修改，可以使用
<a href="/functions/anonymous.html" class="link">匿名函数</a> 来替代。

**示例 \#4 来自外部范围的值不能在箭头函数内修改**

``` php
<?php

$x = 1;
$fn = fn() => $x++; // 不会影响 x 的值
$fn();
var_export($x);  // 输出 1

?>
```

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 7.4.0 | 新增箭头函数语法。 |

### 注释

> **Note**: <span class="simpara"> 可以对箭头函数使用 <span
> class="function">func\_num\_args</span>, <span
> class="function">func\_get\_arg</span>, 和 <span
> class="function">func\_get\_args</span> 函数。 </span>
