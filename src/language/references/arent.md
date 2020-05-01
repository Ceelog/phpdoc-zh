引用不是什么
------------

如前所述，引用不是指针。这意味着下面的结构不会产生预期的效果：

``` php
<?php
function foo(&$var)
{
    $var =& $GLOBALS["baz"];
}
foo($bar);
?>
```

这将使 `foo` 函数中的 `$var` 变量在函数调用时和 `$bar`
绑定在一起，但接着又被重新绑定到了 `$GLOBALS["baz"]`
上面。不可能通过引用机制将 `$bar`
在函数调用范围内绑定到别的变量上面，因为在函数 `foo` 中并没有变量
`$bar`（它被表示为 `$var`，但是 `$var`
只有变量内容而没有调用符号表中的名字到值的绑定）。可以使用<a href="/language/references/return.html" class="link">引用返回</a>来引用被函数选择的变量。
