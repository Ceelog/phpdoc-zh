引用做什么
----------

PHP 的引用允许用两个变量来指向同一个内容。意思是，当这样做时：

``` php
<?php
$a =& $b;
?>
```

这意味着 `$a` 和 `$b` 指向了同一个变量。

> **Note**:
>
> `$a` 和 `$b` 在这里是完全相同的，这并不是 `$a` 指向了 `$b`
> 或者相反，而是 `$a` 和 `$b` 指向了同一个地方。

> **Note**:
>
> 如果具有引用的数组被拷贝，其值不会解除引用。对于数组传值给函数也是如此。

> **Note**:
>
> 如果对一个未定义的变量进行引用赋值、引用参数传递或引用返回，则会自动创建该变量。
>
> **示例 \#1 对未定义的变量使用引用**
>
> ``` php
> <?php
> function foo(&$var) { }
>
> foo($a); // $a is "created" and assigned to null
>
> $b = array();
> foo($b['b']);
> var_dump(array_key_exists('b', $b)); // bool(true)
>
> $c = new StdClass;
> foo($c->d);
> var_dump(property_exists($c, 'd')); // bool(true)
> ?>
> ```

同样的语法可以用在函数中，它返回引用，以及用在 *new* 运算符中（PHP 4.0.4
以及以后版本）：

``` php
<?php
$bar =& new fooclass();
$foo =& find_var($bar);
?>
```

自 PHP 5
起，<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
自动返回引用，因此在此使用 *=&* 已经过时了并且会产生 E\_STRICT
级别的消息。

> **Note**:
>
> 不用 *&* 运算符导致对象生成了一个拷贝。如果在类中用
> *$this*，它将作用于该类当前的实例。没有用 *&*
> 的赋值将拷贝这个实例（例如对象）并且 *$this*
> 将作用于这个拷贝上，这并不总是想要的结果。由于性能和内存消耗的问题，通常只想工作在一个实例上面。
>
> 尽管可以用 *@* 运算符来*抑制*构造函数中的任何错误信息，例如用
> *@new*，但用 *&new* 语句时这不起效果。这是 Zend
> 引擎的一个限制并且会导致一个解析错误。

**Warning**

如果在一个函数内部给一个声明为 *global*
的变量赋于一个引用，该引用只在函数内部可见。可以通过使用 `$GLOBALS`
数组避免这一点。

**示例 \#2 在函数内引用全局变量**

``` php
<?php
$var1 = "Example variable";
$var2 = "";

function global_references($use_globals)
{
    global $var1, $var2;
    if (!$use_globals) {
        $var2 =& $var1; // visible only inside the function
    } else {
        $GLOBALS["var2"] =& $var1; // visible also in global context
    }
}

global_references(false);
echo "var2 is set to '$var2'\n"; // var2 is set to ''
global_references(true);
echo "var2 is set to '$var2'\n"; // var2 is set to 'Example variable'
?>
```

把 *global $var;* 当成是 *$var =& $GLOBALS\['var'\];*
的简写。从而将其它引用赋给 *$var* 只改变了本地变量的引用。

> **Note**:
>
> 如果在
> <a href="/control-structures/foreach.html" class="link">foreach</a>
> 语句中给一个具有引用的变量赋值，被引用的对象也被改变。
>
> **示例 \#3 引用与 foreach 语句**
>
> ``` php
> <?php
> $ref = 0;
> $row =& $ref;
> foreach (array(1, 2, 3) as $row) {
>     // do something
> }
> echo $ref; // 3 - last element of the iterated array
> ?>
> ```

引用做的第二件事是用引用传递变量。这是通过在函数内建立一个本地变量并且该变量在呼叫范围内引用了同一个内容来实现的。例如：

``` php
<?php
function foo(&$var)
{
    $var++;
}

$a=5;
foo($a);
?>
```

将使 `$a` 变成 6。这是因为在 `foo` 函数中变量 `$var` 指向了和 `$a`
指向的同一个内容。更多详细解释见<a href="/language/references/pass.html" class="link">引用传递</a>。

引用做的第三件事是<a href="/language/references/return.html" class="link">引用返回</a>。
