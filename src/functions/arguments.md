函数的参数
----------

通过参数列表可以传递信息到函数，即以逗号作为分隔符的表达式列表。参数是从左向右求值的。

PHP
支持按值传递参数（默认），<a href="/functions/arguments.html#functions.arguments.by-reference" class="link">通过引用传递参数</a>以及<a href="/functions/arguments.html#functions.arguments.default" class="link">默认参数</a>。也支持<a href="/functions/arguments.html#functions.variable-arg-list" class="link">可变长度参数列表</a>。

**示例 \#1 向函数传递数组**

``` php
<?php
function takes_array($input)
{
    echo "$input[0] + $input[1] = ", $input[0]+$input[1];
}
?>
```

### 通过引用传递参数

默认情况下，函数参数通过值传递（因而即使在函数内部改变参数的值，它并不会改变函数外部的值）。如果希望允许函数修改它的参数值，必须通过引用传递参数。

如果想要函数的一个参数总是通过引用传递，可以在函数定义中该参数的前面加上符号
&：

**示例 \#2 用引用传递函数参数**

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

**示例 \#3 在函数中使用默认参数**

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

**示例 \#4 使用非标量类型作为默认参数**

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

**示例 \#5 函数默认参数的不正确用法**

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

**示例 \#6 函数默认参数正确的用法**

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

> **Note**: <span class="simpara"> 自 PHP 5
> 起，传引用的参数也可以有默认值。 </span>

### 类型声明

> **Note**:
>
> 在PHP 5中，类型声明也被称为类型提示。

类型声明允许函数在调用时要求参数为特定类型。
如果给出的值类型不对，那么将会产生一个错误： 在PHP
5中，这将是一个可恢复的致命错误，而在PHP 7中将会抛出一个<span
class="classname">TypeError</span>异常。

为了指定一个类型声明，类型应该加到参数名前。这个声明可以通过将参数的默认值设为**`NULL`**来实现允许传递**`NULL`**。

#### Valid types

| Type                               | Description                                                                                                                                                                                                    | Minimum PHP version |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| Class/interface name               | The parameter must be an <a href="/language/operators/type.html" class="link"><em>instanceof</em></a> the given class or interface name.                                                                       | PHP 5.0.0           |
| *self*                             | The parameter must be an <a href="/language/operators/type.html" class="link"><em>instanceof</em></a> the same class as the one the method is defined on. This can only be used on class and instance methods. | PHP 5.0.0           |
| <span class="type">array</span>    | The parameter must be an <span class="type">array</span>.                                                                                                                                                      | PHP 5.1.0           |
| <span class="type">callable</span> | The parameter must be a valid <span class="type">callable</span>.                                                                                                                                              | PHP 5.4.0           |
| <span class="type">bool</span>     | The parameter must be a <span class="type">boolean</span> value.                                                                                                                                               | PHP 7.0.0           |
| <span class="type">float</span>    | The parameter must be a <span class="type">float</span>ing point number.                                                                                                                                       | PHP 7.0.0           |
| <span class="type">int</span>      | The parameter must be an <span class="type">integer</span>.                                                                                                                                                    | PHP 7.0.0           |
| <span class="type">string</span>   | The parameter must be a <span class="type">string</span>.                                                                                                                                                      | PHP 7.0.0           |
| *iterable*                         | The parameter must be either an <span class="type">array</span> or an <a href="/language/operators/type.html" class="link"><em>instanceof</em></a> <span class="classname">Traversable</span>.                 | PHP 7.1.0           |
| *object*                           | The parameter must be an <span class="type">object</span>.                                                                                                                                                     | PHP 7.2.0           |

**Warning**

Aliases for the above scalar types are not supported. Instead, they are
treated as class or interface names. For example, using *boolean* as a
parameter or return type will require an argument or return value that
is an
<a href="/language/operators/type.html" class="link"><em>instanceof</em></a>
the class or interface *boolean*, rather than of type <span
class="type">bool</span>:

``` php
<?php
 function test(boolean $param) {}
 test(true);
 ?>
```

以上例程会输出：

     Fatal error: Uncaught TypeError: Argument 1 passed to test() must be an instance of boolean, boolean given, called in - on line 1 and defined in -:1
     

#### 范例

**示例 \#7 Basic class type declaration**

``` php
<?php
class C {}
class D extends C {}

// This doesn't extend C.
class E {}

function f(C $c) {
    echo get_class($c)."\n";
}

f(new C);
f(new D);
f(new E);
?>
```

以上例程会输出：

    C
    D

    Fatal error: Uncaught TypeError: Argument 1 passed to f() must be an instance of C, instance of E given, called in - on line 14 and defined in -:8
    Stack trace:
    #0 -(14): f(Object(E))
    #1 {main}
      thrown in - on line 8

**示例 \#8 Basic interface type declaration**

``` php
<?php
interface I { public function f(); }
class C implements I { public function f() {} }

// This doesn't implement I.
class E {}

function f(I $i) {
    echo get_class($i)."\n";
}

f(new C);
f(new E);
?>
```

以上例程会输出：

    C

    Fatal error: Uncaught TypeError: Argument 1 passed to f() must implement interface I, instance of E given, called in - on line 13 and defined in -:8
    Stack trace:
    #0 -(13): f(Object(E))
    #1 {main}
      thrown in - on line 8

**示例 \#9 Typed pass-by-reference Parameters**

Declared types of reference parameters are checked on function entry,
but not when the function returns, so after the function had returned,
the argument's type may have changed.

``` php
<?php
function array_baz(array &$param)
{
    $param = 1;
}
$var = [];
array_baz($var);
var_dump($var);
array_baz($var);
?>
```

以上例程的输出类似于：

    int(1)

    Fatal error: Uncaught TypeError: Argument 1 passed to array_baz() must be of the type array, int given, called in %s on line %d

**示例 \#10 Nullable type declaration**

``` php
<?php
class C {}

function f(C $c = null) {
    var_dump($c);
}

f(new C);
f(null);
?>
```

以上例程会输出：

    object(C)#1 (0) {
    }
    NULL

#### 严格类型

默认情况下，如果能做到的话，PHP将会强迫错误类型的值转为函数期望的标量类型。
例如，一个函数的一个参数期望是<span
class="type">string</span>，但传入的是<span
class="type">integer</span>，最终函数得到的将会是一个<span
class="type">string</span>类型的值。

可以基于每一个文件开启严格模式。在严格模式中，只有一个与类型声明完全相符的变量才会被接受，否则将会抛出一个<span
class="classname">TypeError</span>。 唯一的一个例外是可以将<span
class="type">integer</span>传给一个期望<span
class="type">float</span>的函数。

使用
<a href="/control-structures/declare.html" class="link"><em>declare</em></a>
语句和*strict\_types* 声明来启用严格模式：

**Caution**

启用严格模式同时也会影响<a href="/functions/returning-values.html#functions.returning-values.type-declaration" class="link">返回值类型声明</a>.

> **Note**:
>
> 严格类型适用于在*启用严格模式的文件内*的函数调用，而不是在那个文件内声明的函数。
> 一个没有启用严格模式的文件内调用了一个在启用严格模式的文件中定义的函数，那么将会遵循调用者的偏好（弱类型），而这个值将会被转换。

> **Note**:
>
> 严格类型仅用于标量类型声明，也正是因为如此，这需要PHP 7.0.0
> 或更新版本，因为标量类型声明也是在那个版本中添加的。

**示例 \#11 Strict typing**

``` php
<?php
declare(strict_types=1);

function sum(int $a, int $b) {
    return $a + $b;
}

var_dump(sum(1, 2));
var_dump(sum(1.5, 2.5));
?>
```

以上例程会输出：

    int(3)

    Fatal error: Uncaught TypeError: Argument 1 passed to sum() must be of the type integer, float given, called in - on line 9 and defined in -:4
    Stack trace:
    #0 -(9): sum(1.5, 2.5)
    #1 {main}
      thrown in - on line 4

**示例 \#12 Weak typing**

``` php
<?php
function sum(int $a, int $b) {
    return $a + $b;
}

var_dump(sum(1, 2));

// These will be coerced to integers: note the output below!
var_dump(sum(1.5, 2.5));
?>
```

以上例程会输出：

    int(3)
    int(3)

**示例 \#13 Catching <span class="classname">TypeError</span>**

``` php
<?php
declare(strict_types=1);

function sum(int $a, int $b) {
    return $a + $b;
}

try {
    var_dump(sum(1, 2));
    var_dump(sum(1.5, 2.5));
} catch (TypeError $e) {
    echo 'Error: '.$e->getMessage();
}
?>
```

以上例程会输出：

    int(3)
    Error: Argument 1 passed to sum() must be of the type integer, float given, called in - on line 10

### 可变数量的参数列表

PHP 在用户自定义函数中支持可变数量的参数列表。在 PHP 5.6
及以上的版本中，由 *...* 语法实现；在 PHP 5.5 及更早版本中，使用函数
<span class="function">func\_num\_args</span>，<span
class="function">func\_get\_arg</span>，和 <span
class="function">func\_get\_args</span> 。

#### *...* in PHP 5.6+

In PHP 5.6 and later, argument lists may include the *...* token to
denote that the function accepts a variable number of arguments. The
arguments will be passed into the given variable as an array; for
example:

**示例 \#14 Using *...* to access variable arguments**

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

You can also use *...* when calling functions to unpack an <span
class="type">array</span> or <span class="classname">Traversable</span>
variable or literal into the argument list:

**示例 \#15 Using *...* to provide arguments**

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

You may specify normal positional arguments before the *...* token. In
this case, only the trailing arguments that don't match a positional
argument will be added to the array generated by *...*.

It is also possible to add a
<a href="/language/oop5/typehinting.html" class="link">type hint</a>
before the *...* token. If this is present, then all arguments captured
by *...* must be objects of the hinted class.

**示例 \#16 Type hinted variable arguments**

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

Finally, you may also pass variable arguments
<a href="/functions/arguments.html#functions.arguments.by-reference" class="link">by reference</a>
by prefixing the *...* with an ampersand (*&*).

#### Older versions of PHP

No special syntax is required to note that a function is variadic;
however access to the function's arguments must use <span
class="function">func\_num\_args</span>, <span
class="function">func\_get\_arg</span> and <span
class="function">func\_get\_args</span>.

The first example above would be implemented as follows in PHP 5.5 and
earlier:

**示例 \#17 Accessing variable arguments in PHP 5.5 and earlier**

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
