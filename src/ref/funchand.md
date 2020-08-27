call\_user\_func\_array
=======================

调用回调函数，并把一个数组参数作为回调函数的参数

### 说明

<span class="type">mixed</span> <span
class="methodname">call\_user\_func\_array</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">array</span> `$param_arr`</span> )

把第一个参数作为回调函数（`callback`）调用，把参数数组作（`param_arr`）为回调函数的的参数传入。

### 参数

`callback`  
被调用的回调函数。

`param_arr`  
要被传入回调函数的数组，这个数组得是索引数组。

### 返回值

返回回调函数的结果。如果出错的话就返回**`FALSE`**

### 更新日志

| 版本  | 说明                                                                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 对面向对象里面的关键字的解析有所增强。在此之前，使用两个冒号来连接一个类和里面的一个方法，把它作为参数来作为回调函数的话，将会发出一个**`E_STRICT`**的警告，因为这个传入的参数被视为静态方法。 |

### 范例

**示例 \#1 <span class="function">call\_user\_func\_array</span>例子**

``` php
<?php
function foobar($arg, $arg2) {
    echo __FUNCTION__, " got $arg and $arg2\n";
}
class foo {
    function bar($arg, $arg2) {
        echo __METHOD__, " got $arg and $arg2\n";
    }
}


// Call the foobar() function with 2 arguments
call_user_func_array("foobar", array("one", "two"));

// Call the $foo->bar() method with 2 arguments
$foo = new foo;
call_user_func_array(array($foo, "bar"), array("three", "four"));
?>
```

以上例程的输出类似于：

    foobar got one and two
    foo::bar got three and four

**示例 \#2 <span
class="function">call\_user\_func\_array</span>使用命名空间的情况**

``` php
<?php

namespace Foobar;

class Foo {
    static public function test($name) {
        print "Hello {$name}!\n";
    }
}

// As of PHP 5.3.0
call_user_func_array(__NAMESPACE__ .'\Foo::test', array('Hannes'));

// As of PHP 5.3.0
call_user_func_array(array(__NAMESPACE__ .'\Foo', 'test'), array('Philip'));

?>
```

以上例程的输出类似于：

    Hello Hannes!
    Hello Philip!

**示例 \#3 把完整的函数作为回调传入<span
class="function">call\_user\_func\_array</span>**

``` php
<?php

$func = function($arg1, $arg2) {
    return $arg1 * $arg2;
};

var_dump(call_user_func_array($func, array(2, 4))); /* As of PHP 5.3.0 */

?>
```

以上例程会输出：

    int(8)

**示例 \#4 传引用**

``` php
<?php

function mega(&$a){
    $a = 55;
    echo "function mega \$a=$a\n";
}
$bar = 77;
call_user_func_array('mega',array(&$bar));
echo "global \$bar=$bar\n";

?>
```

以上例程会输出：

    function mega $a=55
    global $bar=55

### 注释

> **Note**:
>
> PHP
> 5.4之前，如果`param_arr`里面的参数是引用传值，那么不管原函数默认的各个参数是不是引用传值，都会以引用方式传入到回调函数。虽然以引用传值这种方式来传递参数给回调函数，不会发出不支持的警告，但是不管怎么说，这样做还是不被支持的。并且在PHP
> 5.4里面被去掉了。而且，这也不适用于内部函数，for which the function
> signature is
> honored。如果回调函数默认设置需要接受的参数是引用传递的时候，按值传递，结果将会输出一个警告。<span
> class="function">call\_user\_func</span> 将会返回 **`FALSE`**（there
> is, however, an exception for passed values with reference count = 1,
> such as in literals, as these can be turned into references without
> ill effects — but also without writes to that value having any effect
> —; do not rely in this behavior, though, as the reference count is an
> implementation detail and the soundness of this behavior is
> questionable）。

> **Note**:
>
> 在函数中注册有多个回调内容时(如使用 <span
> class="function">call\_user\_func</span> 与 <span
> class="function">call\_user\_func\_array</span>)，如在前一个回调中有未捕获的异常，其后的将不再被调用。

### 参见

-   <span class="function">call\_user\_func</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息
-   <span class="methodname">ReflectionFunction::invokeArgs</span>
-   <span class="methodname">ReflectionMethod::invokeArgs</span>

call\_user\_func
================

把第一个参数作为回调函数调用

### 说明

<span class="type">mixed</span> <span
class="methodname">call\_user\_func</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$parameter`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

第一个参数 `callback` 是被调用的回调函数，其余参数是回调函数的参数。

### 参数

`callback`  
将被调用的回调函数（<span class="type">callable</span>）。

`parameter`  
0个或以上的参数，被传入回调函数。

> **Note**:
>
> 请注意，传入<span
> class="function">call\_user\_func</span>的参数不能为引用传递。
>
> **示例 \#1 <span class="function">call\_user\_func</span> 的参考例子**
>
> ``` php
> <?php
> error_reporting(E_ALL);
> function increment(&$var)
> {
>     $var++;
> }
>
> $a = 0;
> call_user_func('increment', $a);
> echo $a."\n";
>
> call_user_func_array('increment', array(&$a)); // You can use this instead before PHP 5.3
> echo $a."\n";
> ?>
> ```
>
> 以上例程会输出：
>
>     0
>     1

### 返回值

返回回调函数的返回值。

### 更新日志

| 版本  | 说明                                                                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 对面向对象里面的关键字的解析有所增强。在此之前，使用两个冒号来连接一个类和里面的一个方法，把它作为参数来作为回调函数的话，将会发出一个**`E_STRICT`**的警告，因为这个传入的参数被视为静态方法。 |

### 范例

**示例 \#2 <span class="function">call\_user\_func</span> 的例子**

``` php
<?php
function barber($type)
{
    echo "You wanted a $type haircut, no problem\n";
}
call_user_func('barber', "mushroom");
call_user_func('barber', "shave");
?>
```

以上例程会输出：

    You wanted a mushroom haircut, no problem
    You wanted a shave haircut, no problem

**示例 \#3 <span class="function">call\_user\_func</span>
命名空间的使用**

``` php
<?php

namespace Foobar;

class Foo {
    static public function test() {
        print "Hello world!\n";
    }
}

call_user_func(__NAMESPACE__ .'\Foo::test'); // As of PHP 5.3.0
call_user_func(array(__NAMESPACE__ .'\Foo', 'test')); // As of PHP 5.3.0

?>
```

以上例程会输出：

    Hello world!
    Hello world!

**示例 \#4 用<span
class="function">call\_user\_func</span>来调用一个类里面的方法**

``` php
<?php

class myclass {
    static function say_hello()
    {
        echo "Hello!\n";
    }
}

$classname = "myclass";

call_user_func(array($classname, 'say_hello'));
call_user_func($classname .'::say_hello'); // As of 5.2.3

$myobject = new myclass();

call_user_func(array($myobject, 'say_hello'));

?>
```

以上例程会输出：

    Hello!
    Hello!
    Hello!

**示例 \#5 把完整的函数作为回调传入<span
class="function">call\_user\_func</span>**

``` php
<?php
call_user_func(function($arg) { print "[$arg]\n"; }, 'test'); /* As of PHP 5.3.0 */
?>
```

以上例程会输出：

    [test]

### 注释

> **Note**:
>
> 在函数中注册有多个回调内容时(如使用 <span
> class="function">call\_user\_func</span> 与 <span
> class="function">call\_user\_func\_array</span>)，如在前一个回调中有未捕获的异常，其后的将不再被调用。

### 参见

-   <span class="function">call\_user\_func\_array</span>
-   <span class="function">is\_callable</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息
-   <span class="methodname">ReflectionFunction::invoke</span>
-   <span class="methodname">ReflectionMethod::invoke</span>

create\_function
================

Create an anonymous (lambda-style) function

### 说明

<span class="type">string</span> <span
class="methodname">create\_function</span> ( <span
class="methodparam"><span class="type">string</span> `$args`</span> ,
<span class="methodparam"><span class="type">string</span>
`$code`</span> )

Creates an anonymous function from the parameters passed, and returns a
unique name for it.

**Caution**

This function internally performs an <span class="function">eval</span>
and as such has the same security issues as <span
class="function">eval</span>. Additionally it has bad performance and
memory usage characteristics.

If you are using PHP 5.3.0 or newer a native
<a href="/functions/anonymous.html" class="link">anonymous function</a>
should be used instead.

### 参数

Usually these parameters will be passed as single quote delimited
strings. The reason for using single quoted strings, is to protect the
variable names from parsing, otherwise, if you use double quotes there
will be a need to escape the variable names, e.g. *\\$avar*.

`args`  
The function arguments.

`code`  
The function code.

### 返回值

Returns a unique function name as a string, or **`FALSE`** on error.

### 范例

**示例 \#1 Creating an anonymous function with <span
class="function">create\_function</span>**

You can use this function, to (for example) create a function from
information gathered at run time:

``` php
<?php
$newfunc = create_function('$a,$b', 'return "ln($a) + ln($b) = " . log($a * $b);');
echo "New anonymous function: $newfunc\n";
echo $newfunc(2, M_E) . "\n";
// outputs
// New anonymous function: lambda_1
// ln(2) + ln(2.718281828459) = 1.6931471805599
?>
```

Or, perhaps to have general handler function that can apply a set of
operations to a list of parameters:

**示例 \#2 Making a general processing function with <span
class="function">create\_function</span>**

``` php
<?php
function process($var1, $var2, $farr)
{
    foreach ($farr as $f) {
        echo $f($var1, $var2) . "\n";
    }
}

// create a bunch of math functions
$f1 = 'if ($a >=0) {return "b*a^2 = ".$b*sqrt($a);} else {return false;}';
$f2 = "return \"min(b^2+a, a^2,b) = \".min(\$a*\$a+\$b,\$b*\$b+\$a);";
$f3 = 'if ($a > 0 && $b != 0) {return "ln(a)/b = ".log($a)/$b; } else { return false; }';
$farr = array(
    create_function('$x,$y', 'return "some trig: ".(sin($x) + $x*cos($y));'),
    create_function('$x,$y', 'return "a hypotenuse: ".sqrt($x*$x + $y*$y);'),
    create_function('$a,$b', $f1),
    create_function('$a,$b', $f2),
    create_function('$a,$b', $f3)
    );

echo "\nUsing the first array of anonymous functions\n";
echo "parameters: 2.3445, M_PI\n";
process(2.3445, M_PI, $farr);

// now make a bunch of string processing functions
$garr = array(
    create_function('$b,$a', 'if (strncmp($a, $b, 3) == 0) return "** \"$a\" '.
    'and \"$b\"\n** Look the same to me! (looking at the first 3 chars)";'),
    create_function('$a,$b', '; return "CRCs: " . crc32($a) . ", ".crc32($b);'),
    create_function('$a,$b', '; return "similar(a,b) = " . similar_text($a, $b, &$p) . "($p%)";')
    );
echo "\nUsing the second array of anonymous functions\n";
process("Twas brilling and the slithy toves", "Twas the night", $garr);
?>
```

以上例程会输出：

    Using the first array of anonymous functions
    parameters: 2.3445, M_PI
    some trig: -1.6291725057799
    a hypotenuse: 3.9199852871011
    b*a^2 = 4.8103313314525
    min(b^2+a, a^2,b) = 8.6382729035898
    ln(a)/b = 0.27122299212594

    Using the second array of anonymous functions
    ** "Twas the night" and "Twas brilling and the slithy toves"
    ** Look the same to me! (looking at the first 3 chars)
    CRCs: -725381282, 342550513
    similar(a,b) = 11(45.833333333333%)

But perhaps the most common use for of lambda-style (anonymous)
functions is to create callback functions, for example when using <span
class="function">array\_walk</span> or <span
class="function">usort</span>

**示例 \#3 Using anonymous functions as callback functions**

``` php
<?php
$av = array("the ", "a ", "that ", "this ");
array_walk($av, create_function('&$v,$k', '$v = $v . "mango";'));
print_r($av);
?>
```

以上例程会输出：

    Array
    (
      [0] => the mango
      [1] => a mango
      [2] => that mango
      [3] => this mango
    )

an array of strings ordered from shorter to longer

``` php
<?php

$sv = array("small", "larger", "a big string", "it is a string thing");
print_r($sv);

?>
```

以上例程会输出：

    Array
    (
      [0] => small
      [1] => larger
      [2] => a big string
      [3] => it is a string thing
    )

sort it from longer to shorter

``` php
<?php

usort($sv, create_function('$a,$b','return strlen($b) - strlen($a);'));
print_r($sv);

?>
```

以上例程会输出：

    Array
    (
      [0] => it is a string thing
      [1] => a big string
      [2] => larger
      [3] => small
    )

### 参见

-   <a href="/functions/anonymous.html" class="link">Anonymous functions</a>

forward\_static\_call\_array
============================

Call a static method and pass the arguments as array

### 说明

<span class="type">mixed</span> <span
class="methodname">forward\_static\_call\_array</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> , <span class="methodparam"><span
class="type">array</span> `$parameters`</span> )

Calls a user defined function or method given by the `function`
parameter. This function must be called within a method context, it
can't be used outside a class. It uses the
<a href="/language/oop5/late-static-bindings.html" class="link">late static binding</a>.
All arguments of the forwarded method are passed as values, and as an
array, similarly to <span
class="function">call\_user\_func\_array</span>.

### 参数

`function`  
The function or method to be called. This parameter may be an <span
class="type">array</span>, with the name of the class, and the method,
or a <span class="type">string</span>, with a function name.

`parameter`  
One parameter, gathering all the method parameter in one array.

> **Note**:
>
> Note that the parameters for <span
> class="function">forward\_static\_call\_array</span> are not passed by
> reference.

### 返回值

Returns the function result, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">forward\_static\_call\_array</span>
example**

``` php
<?php

class A
{
    const NAME = 'A';
    public static function test() {
        $args = func_get_args();
        echo static::NAME, " ".join(',', $args)." \n";
    }
}

class B extends A
{
    const NAME = 'B';

    public static function test() {
        echo self::NAME, "\n";
        forward_static_call_array(array('A', 'test'), array('more', 'args'));
        forward_static_call_array( 'test', array('other', 'args'));
    }
}

B::test('foo');

function test() {
        $args = func_get_args();
        echo "C ".join(',', $args)." \n";
    }

?>
```

以上例程会输出：

    B
    B more,args 
    C other,args

### 参见

-   <span class="function">forward\_static\_call</span>
-   <span class="function">call\_user\_func</span>
-   <span class="function">call\_user\_func\_array</span>
-   <span class="function">is\_callable</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

forward\_static\_call
=====================

Call a static method

### 说明

<span class="type">mixed</span> <span
class="methodname">forward\_static\_call</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$parameter`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

Calls a user defined function or method given by the `function`
parameter, with the following arguments. This function must be called
within a method context, it can't be used outside a class. It uses the
<a href="/language/oop5/late-static-bindings.html" class="link">late static binding</a>.

### 参数

`function`  
The function or method to be called. This parameter may be an array,
with the name of the class, and the method, or a string, with a function
name.

`parameter`  
Zero or more parameters to be passed to the function.

### 返回值

Returns the function result, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">forward\_static\_call</span> example**

``` php
<?php

class A
{
    const NAME = 'A';
    public static function test() {
        $args = func_get_args();
        echo static::NAME, " ".join(',', $args)." \n";
    }
}

class B extends A
{
    const NAME = 'B';

    public static function test() {
        echo self::NAME, "\n";
        forward_static_call(array('A', 'test'), 'more', 'args');
        forward_static_call( 'test', 'other', 'args');
    }
}

B::test('foo');

function test() {
        $args = func_get_args();
        echo "C ".join(',', $args)." \n";
    }

?>
```

以上例程会输出：

    B
    B more,args 
    C other,args

### 参见

-   <span class="function">forward\_static\_call\_array</span>
-   <span class="function">call\_user\_func\_array</span>
-   <span class="function">call\_user\_func</span>
-   <span class="function">is\_callable</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

func\_get\_arg
==============

返回参数列表的某一项

### 说明

<span class="type">mixed</span> <span
class="methodname">func\_get\_arg</span> ( <span
class="methodparam"><span class="type">int</span> `$arg_num`</span> )

从用户自定义函数的参数列表中获取某个指定的参数。

该函数可以配合 <span class="function">func\_get\_args</span> 和 <span
class="function">func\_num\_args</span>
一起使用，从而使得用户自定义函数可以接受自定义个数的参数列表。

### 参数

`arg_num`  
参数的偏移量。函数的参数是从0开始计数的。

### 返回值

返回指定的参数，错误则返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                        |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 该函数可以在参数列表中使用。                                                                                                                                                                                                                                                                                                |
| 5.3.0 | If this function is called from the outermost scope of a file which has been included by calling <span class="function">include</span> or <span class="function">require</span> from within a function in the calling file, it now generates a warning and returns **`FALSE`**. （不知道如何翻译跟好，直接参考例2即可明白） |

### 错误／异常

当在自定义函数的外面调用的该函数的时候会发出一个警告， 或者是当
`arg_num` 比实际传入的参数的数目大的时候也会发出一个警告。

### 范例

**示例 \#1 <span class="function">func\_get\_arg</span> 例子**

``` php
<?php
function foo()
{
     $numargs = func_num_args();
     echo "Number of arguments: $numargs<br />\n";
     if ($numargs >= 2) {
         echo "Second argument is: " . func_get_arg(1) . "<br />\n";
     }
}

foo (1, 2, 3);
?>
```

**示例 \#2 <span class="function">func\_get\_arg</span> PHP 5.3
前后对比的例子**

``` php
test.php
<?php
function foo() {
    include './fga.inc';
}

foo('First arg', 'Second arg');
?>

fga.inc
<?php

$arg = func_get_arg(1);
var_export($arg);

?>
```

PHP 5.3 版本之前的输出：

    'Second arg'

PHP 5.3 和之后的版本的输出:

    Warning: func_get_arg():  Called from the global scope - no function
    context in /home/torben/Desktop/code/ml/fga.inc on line 3
    false

**示例 \#3 <span class="function">func\_get\_arg</span> example of byref
and byval arguments**

``` php
<?php
function byVal($arg) {
    echo 'As passed     : ', var_export(func_get_arg(0)), PHP_EOL;
    $arg = 'baz';
    echo 'After change  : ', var_export(func_get_arg(0)), PHP_EOL;
}

function byRef(&$arg) {
    echo 'As passed     : ', var_export(func_get_arg(0)), PHP_EOL;
    $arg = 'baz';
    echo 'After change  : ', var_export(func_get_arg(0)), PHP_EOL;
}

$arg = 'bar';
byVal($arg);
byRef($arg);
?>
```

以上例程会输出：

  
As passed : 'bar'  
After change : 'bar'  
As passed : 'bar'  
After change : 'baz'  

### 注释

> **Note**:
>
> 因为函数依赖于当前作用域以确定参数的细节，所以在 5.3.0
> 以前的版本中不能用作函数的参数。如必须传递此值时，可将结果赋与一个变量，然后用此变量进行传递。

> **Note**:
>
> 如果参数以引用方式传递，函数对该参数的任何改变将在函数返回后保留。As
> of PHP 7 the current values will also be returned if the arguments are
> passed by value.

> **Note**: <span class="simpara"> This function returns a copy of the
> passed arguments only, and does not account for default (non-passed)
> arguments. </span>

### 参见

-   <span class="function">func\_get\_args</span>
-   <span class="function">func\_num\_args</span>

func\_get\_args
===============

返回一个包含函数参数列表的数组

### 说明

<span class="type">array</span> <span
class="methodname">func\_get\_args</span> ( <span
class="methodparam">void</span> )

获取函数参数列表的数组。

该函数可以配合 <span class="function">func\_get\_arg</span> 和 <span
class="function">func\_num\_args</span>
一起使用，从而使得用户自定义函数可以接受自定义个数的参数列表。

### 返回值

返回一个数组，其中每个元素都是目前用户自定义函数的参数列表的相应元素的副本。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                        |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 该函数可以在参数列表中使用。                                                                                                                                                                                                                                                                                                |
| 5.3.0 | If this function is called from the outermost scope of a file which has been included by calling <span class="function">include</span> or <span class="function">require</span> from within a function in the calling file, it now generates a warning and returns **`FALSE`**. （不知道如何翻译跟好，直接参考例2即可明白） |

### 错误／异常

在用户自定义函数外调用则会出现错误警告。

### 范例

**示例 \#1 <span class="function">func\_get\_args</span> 例子**

``` php
<?php
function foo()
{
    $numargs = func_num_args();
    echo "Number of arguments: $numargs<br />\n";
    if ($numargs >= 2) {
        echo "Second argument is: " . func_get_arg(1) . "<br />\n";
    }
    $arg_list = func_get_args();
    for ($i = 0; $i < $numargs; $i++) {
        echo "Argument $i is: " . $arg_list[$i] . "<br />\n";
    }
}

foo(1, 2, 3);
?>
```

以上例程会输出：

    Number of arguments: 3<br />
    Second argument is: 2<br />
    Argument 0 is: 1<br />
    Argument 1 is: 2<br />
    Argument 2 is: 3<br />

**示例 \#2 PHP 5.3 前后使用 <span
class="function">func\_get\_args</span> 在的对比**

``` php
test.php
<?php
function foo() {
    include './fga.inc';
}

foo('First arg', 'Second arg');
?>

fga.inc
<?php

$args = func_get_args();
var_export($args);

?>
```

PHP 5.3 版本之前的输出：

    array (
      0 => 'First arg',
      1 => 'Second arg',
    )

PHP 5.3 和之后的版本的输出:

    Warning: func_get_args():  Called from the global scope - no function
    context in /home/torben/Desktop/code/ml/fga.inc on line 3
    false

**示例 \#3 <span class="function">func\_get\_args</span> example of
byref and byval arguments**

``` php
<?php
function byVal($arg) {
    echo 'As passed     : ', var_export(func_get_args()), PHP_EOL;
    $arg = 'baz';
    echo 'After change  : ', var_export(func_get_args()), PHP_EOL;
}

function byRef(&$arg) {
    echo 'As passed     : ', var_export(func_get_args()), PHP_EOL;
    $arg = 'baz';
    echo 'After change  : ', var_export(func_get_args()), PHP_EOL;
}

$arg = 'bar';
byVal($arg);
byRef($arg);
?>
```

以上例程会输出：

  
As passed : array (  
0 =\> 'bar',  
)  
After change : array (  
0 =\> 'bar',  
)  
As passed : array (  
0 =\> 'bar',  
)  
After change : array (  
0 =\> 'baz',  
)  

### 注释

> **Note**:
>
> 因为函数依赖于当前作用域以确定参数的细节，所以在 5.3.0
> 以前的版本中不能用作函数的参数。如必须传递此值时，可将结果赋与一个变量，然后用此变量进行传递。

> **Note**:
>
> 如果参数以引用方式传递，函数对该参数的任何改变将在函数返回后保留。As
> of PHP 7 the current values will also be returned if the arguments are
> passed by value.

> **Note**: <span class="simpara">
> 该函数仅仅是返回传递参数的一个副本，并且不包含没有传入的默认参数。
> </span>

### 参见

-   <span class="function">func\_get\_arg</span>
-   <span class="function">func\_num\_args</span>
-   <span
    class="methodname">ReflectionFunctionAbstract::getParameters</span>

func\_num\_args
===============

Returns the number of arguments passed to the function

### 说明

<span class="type">int</span> <span
class="methodname">func\_num\_args</span> ( <span
class="methodparam">void</span> )

Gets the number of arguments passed to the function.

This function may be used in conjunction with <span
class="function">func\_get\_arg</span> and <span
class="function">func\_get\_args</span> to allow user-defined functions
to accept variable-length argument lists.

### 返回值

Returns the number of arguments passed into the current user-defined
function.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                   |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | This function can now be used in parameter lists.                                                                                                                                                                                                                      |
| 5.3.0 | If this function is called from the outermost scope of a file which has been included by calling <span class="function">include</span> or <span class="function">require</span> from within a function in the calling file, it now generates a warning and returns -1. |

### 错误／异常

Generates a warning if called from outside of a user-defined function.

### 范例

**示例 \#1 <span class="function">func\_num\_args</span> example**

``` php
<?php
function foo()
{
    $numargs = func_num_args();
    echo "Number of arguments: $numargs\n";
}

foo(1, 2, 3);   
?>
```

以上例程会输出：

    Number of arguments: 3

**示例 \#2 <span class="function">func\_num\_args</span> example before
and after PHP 5.3**

``` php
test.php
<?php
function foo() {
    include './fna.php';
}

foo('First arg', 'Second arg');
?>

fna.php
<?php

$num_args = func_num_args();
var_export($num_args);

?>
```

Output previous to PHP 5.3:

    2

Output in PHP 5.3 and later will be something similar to:

    Warning: func_num_args():  Called from the global scope - no function
    context in /home/torben/Desktop/code/ml/fna.php on line 3
    -1

### 注释

> **Note**:
>
> 因为函数依赖于当前作用域以确定参数的细节，所以在 5.3.0
> 以前的版本中不能用作函数的参数。如必须传递此值时，可将结果赋与一个变量，然后用此变量进行传递。

### 参见

-   <span class="function">func\_get\_arg</span>
-   <span class="function">func\_get\_args</span>
-   <span
    class="methodname">ReflectionFunctionAbstract::getNumberOfParameters</span>

function\_exists
================

如果给定的函数已经被定义就返回 **`TRUE`**

### 说明

<span class="type">bool</span> <span
class="methodname">function\_exists</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> )

在已经定义的函数列表（包括系统自带的函数和用户自定义的函数）中查找
`function_name`。

### 参数

`function_name`  
函数名，必须为一个字符串。

### 返回值

如果 `function_name` 存在且的确是一个函数就返回 **`TRUE`** ，反之则返回
**`FALSE`** 。

> **Note**:
>
> 对于语法结构的判断，例如 <span class="function">include\_once</span>
> 和 <span class="function">echo</span> 将会返回 **`FALSE`** 。

### 范例

**示例 \#1 <span class="function">function\_exists</span> 的例子**

``` php
<?php
if (function_exists('imap_open')) {
    echo "IMAP functions are available.<br />\n";
} else {
    echo "IMAP functions are not available.<br />\n";
}
?>
```

### 注释

> **Note**:
>
> 当本配置或者编译或编译选项禁用某函数时，该函数名也可能存在（
> <a href="/ref/image.html" class="link">image</a> 就是一个现成的例子）

### 参见

-   <span class="function">method\_exists</span>
-   <span class="function">is\_callable</span>
-   <span class="function">get\_defined\_functions</span>
-   <span class="function">class\_exists</span>
-   <span class="function">extension\_loaded</span>

get\_defined\_functions
=======================

返回所有已定义函数的数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_defined\_functions</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$exclude_disabled`<span class="initializer"> =
**`FALSE`**</span></span> \] )

获取所有已定义函数的数组。

### 参数

`exclude_disabled`  
禁用的函数是否应该在返回的数据里排除。

### 返回值

返回数组，包含了所有已定义的函数，包括内置(internal) 和用户定义的函数。
可通过`$arr["internal"]`来访问系统内置函数，
通过`$arr["user"]`来访问用户自定义函数 (参见示例)。

### 更新日志

| 版本                  | 说明                           |
|-----------------------|--------------------------------|
| PHP 7.0.15, PHP 7.1.1 | 增加 `exclude_disabled` 参数。 |

### 范例

**示例 \#1 <span class="function">get\_defined\_functions</span> 例子**

``` php
<?php
function myrow($id, $data)
{
    return "<tr><th>$id</th><td>$data</td></tr>\n";
}

$arr = get_defined_functions();

print_r($arr);
?>
```

以上例程的输出类似于：

    Array
    (
        [internal] => Array
            (
                [0] => zend_version
                [1] => func_num_args
                [2] => func_get_arg
                [3] => func_get_args
                [4] => strlen
                [5] => strcmp
                [6] => strncmp
                ...
                [750] => bcscale
                [751] => bccomp
            )

        [user] => Array
            (
                [0] => myrow
            )

    )

### 参见

-   <span class="function">function\_exists</span>
-   <span class="function">get\_defined\_vars</span>
-   <span class="function">get\_defined\_constants</span>
-   <span class="function">get\_declared\_classes</span>

register\_shutdown\_function
============================

注册一个会在php中止时执行的函数

### 说明

<span class="type">void</span> <span
class="methodname">register\_shutdown\_function</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$parameter`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

注册一个 `callback` ，它会在脚本执行完成或者 <span
class="function">exit</span> 后被调用。

可以多次调用 <span class="function">register\_shutdown\_function</span>
，这些被注册的回调会按照他们注册时的顺序被依次调用。
如果你在注册的方法内部调用 <span class="function">exit</span>，
那么所有处理会被中止，并且其他注册的中止回调也不会再被调用。

### 参数

`callback`  
待注册的中止回调

中止回调是作为请求的一部分被执行的，因此可以在它们中进行输出或者读取输出缓冲区。

`parameter`  
可以通过传入额外的参数来将参数传给中止函数

`...`  

### 返回值

没有返回值。

### 错误／异常

如果传入的callback不是可调用的，那么将会产生一个 **`E_WARNING`**
级别的错误。

### 范例

**示例 \#1 <span class="function">register\_shutdown\_function</span>
例子**

``` php
<?php
function shutdown()
{
    // This is our shutdown function, in 
    // here we can do any last operations
    // before the script is complete.

    echo 'Script executed with success', PHP_EOL;
}

register_shutdown_function('shutdown');
?>
```

### 注释

> **Note**:
>
> 在某些web
> server（如Apache）上，可以在中止函数内对脚本的工作目录进行修改。

> **Note**:
>
> 如果进程被信号SIGTERM或SIGKILL杀死，那么中止函数将不会被调用。尽管你无法中断SIGKILL，但你可以通过<span
> class="function">pcntl\_signal</span>
> 来捕获SIGTERM，通过在其中调用<span
> class="function">exit</span>来进行一个正常的中止。

### 参见

-   <a href="/ini/core.html#ini.auto-append-file" class="link">auto_append_file</a>
-   <span class="function">exit</span>
-   <a href="/features/connection-handling.html" class="link">连接处理</a>
    章节

register\_tick\_function
========================

Register a function for execution on each tick

### 说明

<span class="type">bool</span> <span
class="methodname">register\_tick\_function</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$arg`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

Registers the given `function` to be executed when a
<a href="/control-structures/declare.html#control-structures.declare.ticks" class="link">tick</a>
is called.

### 参数

`function`  
The function name as a string, or an array consisting of an object and a
method.

`arg`  

`...`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">register\_tick\_function</span>
example**

``` php
<?php
declare(ticks=1);

// using a function as the callback
register_tick_function('my_function', true);

// using an object->method
$object = new my_class();
register_tick_function(array(&$object, 'my_method'), true);
?>
```

### 更新日志

| 版本  | 说明                                                    |
|-------|---------------------------------------------------------|
| 5.3.0 | Ticks are now supported on threaded web server modules. |

### 注释

**Warning**

<span class="function">register\_tick\_function</span> should not be
used with threaded web server modules with PHP 5.2 or lower.

### 参见

-   <a href="/control-structures/declare.html" class="link">declare</a>
-   <span class="function">unregister\_tick\_function</span>

unregister\_tick\_function
==========================

De-register a function for execution on each tick

### 说明

<span class="type">void</span> <span
class="methodname">unregister\_tick\_function</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> )

De-registers the function named by `function_name` so it is no longer
executed when a
<a href="/control-structures/declare.html" class="link">tick</a> is
called.

### 参数

`function_name`  
The function name, as a string.

### 返回值

没有返回值。

### 参见

-   <span class="function">register\_tick\_function</span>

**目录**

-   [call\_user\_func\_array](/ref/funchand.html#call_user_func_array) —
    调用回调函数，并把一个数组参数作为回调函数的参数
-   [call\_user\_func](/ref/funchand.html#call_user_func) —
    把第一个参数作为回调函数调用
-   [create\_function](/ref/funchand.html#create_function) — Create an
    anonymous (lambda-style) function
-   [forward\_static\_call\_array](/ref/funchand.html#forward_static_call_array)
    — Call a static method and pass the arguments as array
-   [forward\_static\_call](/ref/funchand.html#forward_static_call) —
    Call a static method
-   [func\_get\_arg](/ref/funchand.html#func_get_arg) —
    返回参数列表的某一项
-   [func\_get\_args](/ref/funchand.html#func_get_args) —
    返回一个包含函数参数列表的数组
-   [func\_num\_args](/ref/funchand.html#func_num_args) — Returns the
    number of arguments passed to the function
-   [function\_exists](/ref/funchand.html#function_exists) —
    如果给定的函数已经被定义就返回 TRUE
-   [get\_defined\_functions](/ref/funchand.html#get_defined_functions)
    — 返回所有已定义函数的数组
-   [register\_shutdown\_function](/ref/funchand.html#register_shutdown_function)
    — 注册一个会在php中止时执行的函数
-   [register\_tick\_function](/ref/funchand.html#register_tick_function)
    — Register a function for execution on each tick
-   [unregister\_tick\_function](/ref/funchand.html#unregister_tick_function)
    — De-register a function for execution on each tick
