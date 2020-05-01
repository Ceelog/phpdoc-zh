流程控制的替代语法
------------------

PHP 提供了一些流程控制的替代语法，包括 *if*，*while*，*for*，*foreach*
和
*switch*。替代语法的基本形式是把左花括号（{）换成冒号（:），把右花括号（}）分别换成
*endif;*，*endwhile;*，*endfor;*，*endforeach;* 以及 *endswitch;*。

``` php
<?php if ($a == 5): ?>
A is equal to 5
<?php endif; ?>
```

在上面的例子中，HTML 内容“A is equal to 5”用替代语法嵌套在 *if*
语句中。该 HTML 的内容仅在 `$a` 等于 5 时显示。

替代语法同样可以用在 *else* 和 *elseif* 中。下面是一个包括 *elseif* 和
*else* 的 *if* 结构用替代语法格式写的例子：

``` php
<?php
if ($a == 5):
    echo "a equals 5";
    echo "...";
elseif ($a == 6):
    echo "a equals 6";
    echo "!!!";
else:
    echo "a is neither 5 nor 6";
endif;
?>
```

> **Note**:
>
> 不支持在同一个控制块内混合使用两种语法。

**Warning**

*switch* 和第一个 *case*
之间的任何输出（含空格）将导致语法错误。例如，这样是无效的：

``` php
<?php switch ($foo): ?>
    <?php case 1: ?>
    ...
<?php endswitch ?>
```

而这样是有效的，因为 *switch* 之后的换行符被认为是结束标记 *?\>*
的一部分，所以在 *switch* 和 *case* 之间不能有任何输出：

``` php
<?php switch ($foo): ?>
<?php case 1: ?>
    ...
<?php endswitch ?>
```

更多例子参见
<a href="/control-structures/while.html" class="link">while</a>，<a href="/control-structures/for.html" class="link">for</a>
和 <a href="/control-structures/if.html" class="link">if</a>。
