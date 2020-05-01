*elseif*/*else if*
------------------

*elseif*，和此名称暗示的一样，是 *if* 和 *else* 的组合。和 *else*
一样，它延伸了 *if* 语句，可以在原来的 *if* 表达式值为 **`FALSE`**
时执行不同语句。但是和 *else* 不一样的是，它仅在 *elseif*
的条件表达式值为 **`TRUE`** 时执行语句。例如以下代码将根据条件分别显示
<span class="computeroutput">a is bigger than b</span>，<span
class="computeroutput">a equal to b</span> 或者 <span
class="computeroutput">a is smaller than b</span>：

``` php
<?php
if ($a > $b) {
    echo "a is bigger than b";
} elseif ($a == $b) {
    echo "a is equal to b";
} else {
    echo "a is smaller than b";
}
?>
```

在同一个 *if* 语句中可以有多个 *elseif* 部分，其中第一个表达式值为
**`TRUE`**（如果有的话）的 *elseif* 部分将会执行。在 PHP
中，也可以写成“else
if”（两个单词），它和“elseif”（一个单词）的行为完全一样。句法分析的含义有少许区别（如果你熟悉
C 语言的话，与之行为相同），但是底线是两者会产生完全一样的行为。

*elseif* 的语句仅在之前的 *if* 和所有之前 *elseif* 的表达式值为
**`FALSE`**，并且当前的 *elseif* 表达式值为 **`TRUE`** 时执行。

> **Note**: <span class="simpara"> 必须要注意的是 *elseif* 与 *else if*
> 只有在类似上例中使用花括号的情况下才认为是完全相同。如果用冒号来定义
> *if*/*elseif* 条件，那就不能用两个单词的 *else if*，否则 PHP
> 会产生解析错误。 </span>

``` php
<?php

/* 不正确的使用方法： */
if ($a > $b):
    echo $a." is greater than ".$b;
else if ($a == $b): // 将无法编译
    echo "The above line causes a parse error.";
endif;


/* 正确的使用方法： */
if ($a > $b):
    echo $a." is greater than ".$b;
elseif ($a == $b): // 注意使用了一个单词的 elseif
    echo $a." equals ".$b;
else:
    echo $a." is neither greater than or equal to ".$b;
endif;

?>
```
