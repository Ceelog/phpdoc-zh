*if*
----

*if* 结构是很多语言包括 PHP
在内最重要的特性之一，它允许按照条件执行代码片段。PHP 的 *if* 结构和 C
语言相似：

    <?php
    if (expr)
      statement
    ?>

如同在<a href="/language/expressions.html" class="link">表达式</a>一章中定义的，<span
class="replaceable">expr</span> 按照布尔求值。如果 <span
class="replaceable">expr</span> 的值为 **`true`**，PHP 将执行 <span
class="replaceable">statement</span>，如果值为 **`false`** ——将忽略
<span class="replaceable">statement</span>。有关哪些值被视为 **`false`**
的更多信息参见<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">转换为布尔值</a>一节。

如果 `$a` 大于 `$b`，则以下例子将显示 <span class="computeroutput">a is
bigger than b</span>：

``` php
<?php
if ($a > $b)
  echo "a is bigger than b";
?>
```

经常需要按照条件执行不止一条语句，当然并不需要给每条语句都加上一个 *if*
子句。可以将这些语句放入语句组中。例如，如果 `$a` 大于
`$b`，以下代码将显示 <span class="computeroutput">a is bigger than
b</span> 并且将 `$a` 的值赋给 `$b`：

``` php
<?php
if ($a > $b) {
  echo "a is bigger than b";
  $b = $a;
}
?>
```

*if* 语句可以无限层地嵌套在其它 *if*
语句中，这给程序的不同部分的条件执行提供了充分的弹性。
