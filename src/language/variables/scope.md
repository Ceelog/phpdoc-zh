变量范围
--------

变量的范围即它定义的上下文背景（也就是它的生效范围）。大部分的 PHP
变量只有一个单独的范围。这个单独的范围跨度同样包含了 include 和 require
引入的文件。例如：

``` php
<?php
$a = 1;
include 'b.inc';
?>
```

这里变量 `$a` 将会在包含文件 `b.inc`
中生效。但是，在用户自定义函数中，一个局部函数范围将被引入。任何用于函数内部的变量按缺省情况将被限制在局部函数范围内。例如：

``` php
<?php
$a = 1; /* global scope */

function Test()
{
    echo $a; /* reference to local scope variable */
}

Test();
?>
```

这个脚本不会有任何输出，因为 echo 语句引用了一个局部版本的变量
`$a`，而且在这个范围内，它并没有被赋值。你可能注意到 PHP 的全局变量和 C
语言有一点点不同，在 C
语言中，全局变量在函数中自动生效，除非被局部变量覆盖。这可能引起一些问题，有些人可能不小心就改变了一个全局变量。PHP
中全局变量在函数中使用时必须声明为 global。

### global 关键字

首先，一个使用 *global* 的例子：

**示例 \#1 使用 global**

``` php
<?php
$a = 1;
$b = 2;

function Sum()
{
    global $a, $b;

    $b = $a + $b;
}

Sum();
echo $b;
?>
```

以上脚本的输出将是“3”。在函数中声明了全局变量 `$a` 和 `$b`
之后，对任一变量的所有引用都会指向其全局版本。对于一个函数能够声明的全局变量的最大个数，PHP
没有限制。

在全局范围内访问变量的第二个办法，是用特殊的 PHP 自定义 `$GLOBALS`
数组。前面的例子可以写成：

**示例 \#2 使用 `$GLOBALS` 替代 global**

``` php
<?php
$a = 1;
$b = 2;

function Sum()
{
    $GLOBALS['b'] = $GLOBALS['a'] + $GLOBALS['b'];
}

Sum();
echo $b;
?>
```

`$GLOBALS`
是一个关联数组，每一个变量为一个元素，键名对应变量名，值对应变量的内容。`$GLOBALS`
之所以在全局范围内存在，是因为 $GLOBALS
是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。以下范例显示了超全局变量的用处：

**示例 \#3 演示超全局变量和作用域的例子**

``` php
<?php
function test_global()
{
    // 大多数的预定义变量并不 "super"，它们需要用 'global' 关键字来使它们在函数的本地区域中有效。
    global $HTTP_POST_VARS;

    echo $HTTP_POST_VARS['name'];

    // Superglobals 在任何范围内都有效，它们并不需要 'global' 声明。Superglobals 是在 PHP 4.1.0 引入的。
    echo $_POST['name'];
}
?>
```

### 使用静态变量

变量范围的另一个重要特性是*静态变量*（static
variable）。静态变量仅在局部函数域中存在，但当程序执行离开此作用域时，其值并不丢失。看看下面的例子：

**示例 \#4 演示需要静态变量的例子**

``` php
<?php
function Test()
{
    $a = 0;
    echo $a;
    $a++;
}
?>
```

本函数没什么用处，因为每次调用时都会将 `$a` 的值设为 *0* 并输出
*0*。将变量加一的 `$a`++ 没有作用，因为一旦退出本函数则变量 `$a`
就不存在了。要写一个不会丢失本次计数值的计数函数，要将变量 `$a`
定义为静态的：

**示例 \#5 使用静态变量的例子**

``` php
<?php
function test()
{
    static $a = 0;
    echo $a;
    $a++;
}
?>
```

现在，变量 `$a` 仅在第一次调用 test() 函数时被初始化，之后每次调用
test() 函数都会输出 `$a` 的值并加一。

静态变量也提供了一种处理递归函数的方法。递归函数是一种调用自己的函数。写递归函数时要小心，因为可能会无穷递归下去。必须确保有充分的方法来中止递归。以下这个简单的函数递归计数到
10，使用静态变量 `$count` 来判断何时停止：

**示例 \#6 静态变量与递归函数**

``` php
<?php
function test()
{
    static $count = 0;

    $count++;
    echo $count;
    if ($count < 10) {
        test();
    }
    $count--;
}
?>
```

> **Note**:
>
> 静态变量可以按照上面的例子声明。如果在声明中用表达式的结果对其赋值会导致解析错误。
>
> **示例 \#7 声明静态变量**
>
> ``` php
> <?php
> function foo(){
>     static $int = 0;          // correct
>     static $int = 1+2;        // wrong  (as it is an expression)
>     static $int = sqrt(121);  // wrong  (as it is an expression too)
>
>     $int++;
>     echo $int;
> }
> ?>
> ```

静态声明是在编译时解析的。

> **Note**:
>
> 在函数之外使用 *global*
> 关键字不算错。可以用于在一个函数之内包含文件时。

### 全局和静态变量的引用

在 Zend 引擎 1 代，它驱动了 PHP4，对于变量的
<a href="/language/variables/scope.html#language.variables.scope.static" class="link">static</a>
和
<a href="/language/variables/scope.html#language.variables.scope.global" class="link">global</a>
定义是以<a href="/language/references.html" class="link">引用</a>的方式实现的。例如，在一个函数域内部用
*global*
语句导入的一个真正的全局变量实际上是建立了一个到全局变量的引用。这有可能导致预料之外的行为，如以下例子所演示的：

``` php
<?php
function test_global_ref() {
    global $obj;
    $obj = &new stdclass;
}

function test_global_noref() {
    global $obj;
    $obj = new stdclass;
}

test_global_ref();
var_dump($obj);
test_global_noref();
var_dump($obj);
?>
```

以上例程会输出：

  
NULL  
object(stdClass)(0) {  
}  

类似的行为也适用于 *static* 语句。引用并不是静态地存储的：

``` php
<?php
function &get_instance_ref() {
    static $obj;

    echo 'Static object: ';
    var_dump($obj);
    if (!isset($obj)) {
        // 将一个引用赋值给静态变量
        $obj = &new stdclass;
    }
    $obj->property++;
    return $obj;
}

function &get_instance_noref() {
    static $obj;

    echo 'Static object: ';
    var_dump($obj);
    if (!isset($obj)) {
        // 将一个对象赋值给静态变量
        $obj = new stdclass;
    }
    $obj->property++;
    return $obj;
}

$obj1 = get_instance_ref();
$still_obj1 = get_instance_ref();
echo "\n";
$obj2 = get_instance_noref();
$still_obj2 = get_instance_noref();
?>
```

以上例程会输出：

  
Static object: NULL  
Static object: NULL  
  
Static object: NULL  
Static object: object(stdClass)(1) {  
\["property"\]=\>  
int(1)  
}  

上例演示了当把一个引用赋值给一个静态变量时，第二次调用
*&get\_instance\_ref()* 函数时其值并没有被*记住*。
