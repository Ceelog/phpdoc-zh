函数的参数
----------

通过参数列表可以传递信息到函数，即以逗号作为分隔符的表达式列表。参数是从左向右求值的。

PHP
支持按值传递参数（默认），<a href="/functions/arguments.html#functions.arguments.by-reference" class="link">通过引用传递参数</a>
以及
<a href="/functions/arguments.html#functions.arguments.default" class="link">默认参数</a>。也支持
<a href="/functions/arguments.html#functions.variable-arg-list" class="link">可变长度参数列表</a>。

**示例 \#1 向函数传递数组**

``` php
<?php
function takes_array($input)
{
    echo "$input[0] + $input[1] = ", $input[0]+$input[1];
}
?>
```

从 PHP 8.0.0
开始，函数参数列表可以包含一个尾部的逗号，这个逗号将被忽略。这在参数列表较长或包含较长的变量名的情况下特别有用，这样可以方便地垂直列出参数。

**示例 \#2 Function Argument List with trailing Comma**

``` php
<?php
function takes_many_args(
    $first_arg,
    $second_arg,
    $a_very_long_argument_name,
    $arg_with_default = 5,
    $again = 'a default string', // 在 8.0.0 之前，这个尾部的逗号是不允许的。
)
{
    // ...
}
?>
```

### 通过引用传递参数

默认情况下，函数参数通过值传递（因而即使在函数内部改变参数的值，它并不会改变函数外部的值）。如果希望允许函数修改它的参数值，必须通过引用传递参数。

如果想要函数的一个参数总是通过引用传递，可以在函数定义中该参数的前面加上符号
&：

**示例 \#3 用引用传递函数参数**

``` php
<?php
function add_some_extra(&$string)
{
    $string .= 'and something extra.';
}
$str = 'This is a string, ';
add_some_extra($str);
echo $str;    // outputs 'This is a string, and something extra.'
?>
```

### 默认参数的值

函数可以定义 C++ 风格的标量参数默认值，如下所示：

**示例 \#4 在函数中使用默认参数**

``` php
<?php
function makecoffee($type = "cappuccino")
{
    return "Making a cup of $type.\n";
}
echo makecoffee();
echo makecoffee(null);
echo makecoffee("espresso");
?>
```

以上例程会输出：

    Making a cup of cappuccino.
    Making a cup of .
    Making a cup of espresso.

PHP 还允许使用数组 <span class="type">array</span> 和特殊类型 **`NULL`**
作为默认参数，例如：

**示例 \#5 使用非标量类型作为默认参数**

``` php
<?php
function makecoffee($types = array("cappuccino"), $coffeeMaker = NULL)
{
    $device = is_null($coffeeMaker) ? "hands" : $coffeeMaker;
    return "Making a cup of ".join(", ", $types)." with $device.\n";
}
echo makecoffee();
echo makecoffee(array("cappuccino", "lavazza"), "teapot");
?>
```

默认值必须是常量表达式，不能是诸如变量，类成员，或者函数调用等。

注意当使用默认参数时，任何默认参数必须放在任何非默认参数的右侧；否则，函数将不会按照预期的情况工作。考虑下面的代码片断：

**示例 \#6 函数默认参数的不正确用法**

``` php
<?php
function makeyogurt($type = "acidophilus", $flavour)
{
    return "Making a bowl of $type $flavour.\n";
}

echo makeyogurt("raspberry");   // won't work as expected
?>
```

以上例程会输出：

    Warning: Missing argument 2 in call to makeyogurt() in 
    /usr/local/etc/httpd/htdocs/phptest/functest.html on line 41
    Making a bowl of raspberry .

现在，比较上面的例子和这个例子：

**示例 \#7 函数默认参数正确的用法**

``` php
<?php
function makeyogurt($flavour, $type = "acidophilus")
{
    return "Making a bowl of $type $flavour.\n";
}

echo makeyogurt("raspberry");   // works as expected
?>
```

以上例程会输出：

    Making a bowl of acidophilus raspberry.

> **Note**: <span class="simpara"> 传引用的参数也可以有默认值。 </span>

### 可变数量的参数列表

PHP 在用户自定义函数中支持可变数量的参数列表。由 *...* 语法实现。

> **Note**: <span class="simpara"> 还可以使用以下函数来获取可变参数
> <span class="function">func\_num\_args</span>、 <span
> class="function">func\_get\_arg</span> 和 <span
> class="function">func\_get\_args</span>，不建议使用此方式，请使用
> *...* 来替代。 </span>

包含 *...* 的参数，会转换为指定参数变量的一个数组，见以下示例：

**示例 \#8 使用 *...* 来访问变量参数**

``` php
<?php
function sum(...$numbers) {
    $acc = 0;
    foreach ($numbers as $n) {
        $acc += $n;
    }
    return $acc;
}

echo sum(1, 2, 3, 4);
?>
```

以上例程会输出：

    10

也可以使用 *...* 语法来传递 <span class="type">array</span> 或 <span
class="classname">Traversable</span> 做为参数到函数中：

**示例 \#9 使用 *...* 来传递参数**

``` php
<?php
function add($a, $b) {
    return $a + $b;
}

echo add(...[1, 2])."\n";

$a = [1, 2];
echo add(...$a);
?>
```

以上例程会输出：

    3
    3

你可以在 *...*
前指定正常的位置参数。在这种情况下，只有不符合位置参数的尾部参数才会被添加到
*...* 生成的数组中。

你也可以在 *...* 标记前添加一个
<a href="/language/types/declarations.html" class="link">类型声明</a>。如果存在这种情况，那么
*...* 捕获的所有参数必须是提示类的对象。

**示例 \#10 输入提示的变量参数**

``` php
<?php
function total_intervals($unit, DateInterval ...$intervals) {
    $time = 0;
    foreach ($intervals as $interval) {
        $time += $interval->$unit;
    }
    return $time;
}

$a = new DateInterval('P1D');
$b = new DateInterval('P2D');
echo total_intervals('d', $a, $b).' days';

// This will fail, since null isn't a DateInterval object.
echo total_intervals('d', null);
?>
```

以上例程会输出：

    3 days
    Catchable fatal error: Argument 2 passed to total_intervals() must be an instance of DateInterval, null given, called in - on line 14 and defined in - on line 2

最后，你还可以给参数传递
<a href="/functions/arguments.html#functions.arguments.by-reference" class="link">引用变量</a>，通过在
*...* 前加上一个 (*&*) 符号来实现。

#### 旧版本的 PHP

不需要特殊的语法来声明一个函数是可变的；但是访问函数的参数必须使用 <span
class="function">func\_num\_args</span>, <span
class="function">func\_get\_arg</span> 和 <span
class="function">func\_get\_args</span> 函数。

上面的第一个例子在早期 PHP 版本中的实现如下：

**示例 \#11 在 PHP 早期版本中访问可变参数**

``` php
<?php
function sum() {
    $acc = 0;
    foreach (func_get_args() as $n) {
        $acc += $n;
    }
    return $acc;
}

echo sum(1, 2, 3, 4);
?>
```

以上例程会输出：

    10
