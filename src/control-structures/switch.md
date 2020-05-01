*switch*
--------

*switch* 语句类似于具有同一个表达式的一系列 *if*
语句。很多场合下需要把同一个变量（或表达式）与很多不同的值比较，并根据它等于哪个值来执行不同的代码。这正是
*switch* 语句的用途。

> **Note**: <span class="simpara">
> 注意和其它语言不同，<a href="/control-structures/continue.html" class="link">continue</a>
> 语句作用到 switch 上的作用类似于 *break*。如果在循环中有一个 switch
> 并希望 continue 到外层循环中的下一轮循环，用 *continue 2*。 </span>

> **Note**:
>
> 注意 switch/case
> 作的是<a href="/types/comparisons.html#types.comparisions-loose" class="link">松散比较</a>。

下面两个例子使用两种不同方法实现同样的事，一个用一系列的 *if* 和
*elseif* 语句，另一个用 *switch* 语句：

**示例 \#1 *switch* 结构**

``` php
<?php
if ($i == 0) {
    echo "i equals 0";
} elseif ($i == 1) {
    echo "i equals 1";
} elseif ($i == 2) {
    echo "i equals 2";
}

switch ($i) {
    case 0:
        echo "i equals 0";
        break;
    case 1:
        echo "i equals 1";
        break;
    case 2:
        echo "i equals 2";
        break;
}
?>
```

**示例 \#2 *switch* 结构可以用字符串**

``` php
<?php
switch ($i) {
case "apple":
    echo "i is apple";
    break;
case "bar":
    echo "i is bar";
    break;
case "cake":
    echo "i is cake";
    break;
}
?>
```

为避免错误，理解 *switch* 是怎样执行的非常重要。*switch*
语句一行接一行地执行（实际上是语句接语句）。开始时没有代码被执行。仅当一个
*case* 语句中的值和 *switch* 表达式的值匹配时 PHP 才开始执行语句，直到
*switch* 的程序段结束或者遇到第一个 *break* 语句为止。如果不在 case
的语句段最后写上 *break* 的话，PHP 将继续执行下一个 case
中的语句段。例如：

``` php
<?php
switch ($i) {
    case 0:
        echo "i equals 0";
    case 1:
        echo "i equals 1";
    case 2:
        echo "i equals 2";
}
?>
```

这里如果 `$i` 等于 0，PHP 将执行所有的 echo 语句！如果 `$i` 等于 1，PHP
将执行后面两条 echo 语句。只有当 `$i` 等于 2
时，才会得到“预期”的结果——只显示“i equals 2”。所以，别忘了 *break*
语句就很重要（即使在某些情况下故意想避免提供它们时）。

在 *switch* 语句中条件只求值一次并用来和每个 *case* 语句比较。在
*elseif*
语句中条件会再次求值。如果条件比一个简单的比较要复杂得多或者在一个很多次的循环中，那么用
*switch* 语句可能会快一些。

在一个 case 中的语句也可以为空，这样只不过将控制转移到了下一个 case
中的语句。

``` php
<?php
switch ($i) {
    case 0:
    case 1:
    case 2:
        echo "i is less than 3 but not negative";
        break;
    case 3:
        echo "i is 3";
}
?>
```

一个 case 的特例是 *default*。它匹配了任何和其它 case
都不匹配的情况。例如：

``` php
<?php
switch ($i) {
    case 0:
        echo "i equals 0";
        break;
    case 1:
        echo "i equals 1";
        break;
    case 2:
        echo "i equals 2";
        break;
    default:
        echo "i is not equal to 0, 1 or 2";
}
?>
```

*case*
表达式可以是任何求值为简单类型的表达式，即整型或浮点数以及字符串。不能用数组或对象，除非它们被解除引用成为简单类型。

*switch*
支持替代语法的流程控制。更多信息见<a href="/control-structures/alternative-syntax.html" class="link">流程控制的替代语法</a>一节。

``` php
<?php
switch ($i):
    case 0:
        echo "i equals 0";
        break;
    case 1:
        echo "i equals 1";
        break;
    case 2:
        echo "i equals 2";
        break;
    default:
        echo "i is not equal to 0, 1 or 2";
endswitch;
?>
```

允许使用分号代替 case 语句后的冒号，例如：

``` php
<?php
switch($beer)
{
    case 'tuborg';
    case 'carlsberg';
    case 'heineken';
        echo 'Good choice';
    break;
    default;
        echo 'Please make a new selection...';
    break;
}
?>
```
