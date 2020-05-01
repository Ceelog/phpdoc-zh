匿名函数
--------

匿名函数（Anonymous functions），也叫闭包函数（*closures*），允许
临时创建一个没有指定名称的函数。最经常用作回调函数（<a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>）参数的值。当然，也有其它应用的情况。

匿名函数目前是通过
<a href="/class/closure.html" class="link"><span class="classname">Closure</span></a>
类来实现的。

**示例 \#1 匿名函数示例**

``` php
<?php
echo preg_replace_callback('~-([a-z])~', function ($match) {
    return strtoupper($match[1]);
}, 'hello-world');
// 输出 helloWorld
?>
```

闭包函数也可以作为变量的值来使用。PHP 会自动把此种表达式转换成内置类
<span class="classname">Closure</span> 的对象实例。把一个 closure
对象赋值给一个变量的方式与普通变量赋值的语法是一样的，最后也要加上分号：

**示例 \#2 匿名函数变量赋值示例**

``` php
<?php
$greet = function($name)
{
    printf("Hello %s\r\n", $name);
};

$greet('World');
$greet('PHP');
?>
```

闭包可以从父作用域中继承变量。 任何此类变量都应该用 *use*
语言结构传递进去。 PHP 7.1 起，不能传入此类变量：
<a href="/language/variables/predefined.html" class="link">superglobals</a>、
`$this` 或者和参数重名。

**示例 \#3 从父作用域继承变量**

``` php
<?php
$message = 'hello';

// 没有 "use"
$example = function () {
    var_dump($message);
};
echo $example();

// 继承 $message
$example = function () use ($message) {
    var_dump($message);
};
echo $example();

// Inherited variable's value is from when the function
// is defined, not when called
$message = 'world';
echo $example();

// Reset message
$message = 'hello';

// Inherit by-reference
$example = function () use (&$message) {
    var_dump($message);
};
echo $example();

// The changed value in the parent scope
// is reflected inside the function call
$message = 'world';
echo $example();

// Closures can also accept regular arguments
$example = function ($arg) use ($message) {
    var_dump($arg . ' ' . $message);
};
$example("hello");
?>
```

以上例程的输出类似于：

    Notice: Undefined variable: message in /example.php on line 6
    NULL
    string(5) "hello"
    string(5) "hello"
    string(5) "hello"
    string(5) "world"
    string(11) "hello world"

这些变量都必须在函数或类的头部声明。
从父作用域中继承变量与使用全局变量是*不同*的。全局变量存在于一个全局的范围，无论当前在执行的是哪个函数。而
闭包的父作用域是定义该闭包的函数（不一定是调用它的函数）。示例如下：

**示例 \#4 Closures 和作用域**

``` php
<?php
// 一个基本的购物车，包括一些已经添加的商品和每种商品的数量。
// 其中有一个方法用来计算购物车中所有商品的总价格，该方法使
// 用了一个 closure 作为回调函数。
class Cart
{
    const PRICE_BUTTER  = 1.00;
    const PRICE_MILK    = 3.00;
    const PRICE_EGGS    = 6.95;

    protected   $products = array();
    
    public function add($product, $quantity)
    {
        $this->products[$product] = $quantity;
    }
    
    public function getQuantity($product)
    {
        return isset($this->products[$product]) ? $this->products[$product] :
               FALSE;
    }
    
    public function getTotal($tax)
    {
        $total = 0.00;
        
        $callback =
            function ($quantity, $product) use ($tax, &$total)
            {
                $pricePerItem = constant(__CLASS__ . "::PRICE_" .
                    strtoupper($product));
                $total += ($pricePerItem * $quantity) * ($tax + 1.0);
            };
        
        array_walk($this->products, $callback);
        return round($total, 2);;
    }
}

$my_cart = new Cart;

// 往购物车里添加条目
$my_cart->add('butter', 1);
$my_cart->add('milk', 3);
$my_cart->add('eggs', 6);

// 打出出总价格，其中有 5% 的销售税.
print $my_cart->getTotal(0.05) . "\n";
// 最后结果是 54.29
?>
```

**示例 \#5 Automatic binding of *$this***

``` php
<?php

class Test
{
    public function testing()
    {
        return function() {
            var_dump($this);
        };
    }
}

$object = new Test;
$function = $object->testing();
$function();
    
?>
```

以上例程会输出：

    object(Test)#1 (0) {
    }

以上例程在PHP 5.3中的输出：

    Notice: Undefined variable: this in script.php on line 8
    NULL

As of PHP 5.4.0, when declared in the context of a class, the current
class is automatically bound to it, making *$this* available inside of
the function's scope. If this automatic binding of the current class is
not wanted, then
<a href="/functions/anonymous.html#functions.anonymous-functions.static" class="link">static anonymous functions</a>
may be used instead.

### Static anonymous functions

As of PHP 5.4, anonymous functions may be declared statically. This
prevents them from having the current class automatically bound to them.
Objects may also not be bound to them at runtime.

**示例 \#6 Attempting to use *$this* inside a static anonymous
function**

``` php
<?php

class Foo
{
    function __construct()
    {
        $func = static function() {
            var_dump($this);
        };
        $func();
    }
};
new Foo();

?>
```

以上例程会输出：

    Notice: Undefined variable: this in %s on line %d
    NULL

**示例 \#7 Attempting to bind an object to a static anonymous function**

``` php
<?php

$func = static function() {
    // function body
};
$func = $func->bindTo(new StdClass);
$func();

?>
```

以上例程会输出：

    Warning: Cannot bind an instance to a static closure in %s on line %d

### 更新日志

| 版本  | 说明                                                                                                                                                                            |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | Anonymous functions may not close over <a href="/language/variables/predefined.html" class="link">superglobals</a>, `$this`, or any variable with the same name as a parameter. |
| 5.4.0 | `$this` 可用于匿名函数。                                                                                                                                                        |
| 5.3.0 | 可以使用匿名函数。                                                                                                                                                              |

### 注释

> **Note**: <span class="simpara"> 可以在闭包中使用 <span
> class="function">func\_num\_args</span>，<span
> class="function">func\_get\_arg</span> 和 <span
> class="function">func\_get\_args</span>。 </span>
