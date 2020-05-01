引用传递
--------

可以将一个变量通过引用传递给函数，这样该函数就可以修改其参数的值。语法如下：

``` php
<?php
function foo(&$var)
{
    $var++;
}

$a=5;
foo($a);
// $a is 6 here
?>
```

注意在函数调用时没有引用符号——只有函数定义中有。光是函数定义就足够使参数通过引用来正确传递了。在最近版本的
PHP 中如果把 & 用在 *foo(&$a);* 中会得到一条警告说“Call-time
pass-by-reference”已经过时了。

以下内容可以通过引用传递：

-   <span class="simpara"> 变量，例如 *foo($a)* </span>

-   <span class="simpara"> New 语句，例如 *foo(new foobar())* </span>

-   从函数中返回的引用，例如：

    ``` php
    <?php
    function &bar()
    {
        $a = 5;
        return $a;
    }
    foo(bar());
    ?>
    ```

    详细解释见<a href="/language/references/return.html" class="link">引用返回</a>。

任何其它表达式都不能通过引用传递，结果未定义。例如下面引用传递的例子是无效的：

``` php
<?php
function foo(&$var)
{
    $var++;
}
function bar() // Note the missing &
{
    $a = 5;
    return $a;
}
foo(bar()); // 自 PHP 5.0.5 起导致致命错误，自 PHP 5.1.1 起导致严格模式错误
            // 自 PHP 7.0 起导致 notice 信息
foo($a = 5) // 表达式，不是变量
foo(5) // 导致致命错误
?>
```

这些条件是 PHP 4.0.4 以及以后版本有的。
