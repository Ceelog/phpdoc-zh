*do-while*
----------

*do-while* 循环和 *while*
循环非常相似，区别在于表达式的值是在每次循环结束时检查而不是开始时。和一般的
*while* 循环主要的区别是 *do-while*
的循环语句保证会执行一次（表达式的真值在每次循环结束后检查），然而在一般的
*while* 循环中就不一定了（表达式真值在循环开始时检查，如果一开始就为
**`false`** 则整个循环立即终止）。

*do-while* 循环只有一种语法：

``` php
<?php
$i = 0;
do {
   echo $i;
} while ($i > 0);
?>
```

以上循环将正好运行一次，因为经过第一次循环后，当检查表达式的真值时，其值为
**`false`**（`$i` 不大于 0）而导致循环终止。

资深的 C 语言用户可能熟悉另一种不同的 *do-while* 循环用法，把语句放在
*do-while*(0) 之中，在循环内部用
<a href="/control-structures/break.html" class="link"><em>break</em></a>
语句来结束执行循环。以下代码片段示范了此方法：

``` php
<?php
do {
    if ($i < 5) {
        echo "i is not big enough";
        break;
    }
    $i *= $factor;
    if ($i < $minimum_limit) {
        break;
    }
    echo "i is ok";

    /* process i */

} while(0);
?>
```

如果还不能立刻理解也不用担心。即使不用此“特性”也照样可以写出强大的代码来。自
PHP 5.3.0 起，还可以使用
<a href="/control-structures/goto.html" class="link"><em>goto</em></a>
来跳出循环。
