*else*
------

经常需要在满足某个条件时执行一条语句，而在不满足该条件时执行其它语句，这正是
*else* 的功能。*else* 延伸了 *if* 语句，可以在 *if* 语句中的表达式的值为
**`false`** 时执行语句。例如以下代码在 `$a` 大于 `$b` 时显示 <span
class="computeroutput">a is bigger than b</span>，反之则显示 <span
class="computeroutput">a is NOT bigger than b</span>：

``` php
<?php
if ($a > $b) {
  echo "a is greater than b";
} else {
  echo "a is NOT greater than b";
}
?>
```

*else* 语句仅在 *if* 以及 *elseif*（如果有的话）语句中的表达式的值为
**`false`** 时执行（参见
<a href="/control-structures/elseif.html" class="link">elseif</a>）。
