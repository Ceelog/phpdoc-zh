可变函数
--------

PHP 支持可变函数的概念。这意味着如果一个变量名后有圆括号，PHP
将寻找与变量的值同名的函数，并且尝试执行它。可变函数可以用来实现包括回调函数，函数表在内的一些用途。

可变函数不能用于例如 <span class="function">echo</span>，<span
class="function">print</span>，<span
class="function">unset</span>，<span
class="function">isset</span>，<span
class="function">empty</span>，<span
class="function">include</span>，<span class="function">require</span>
以及类似的语言结构。需要使用自己的包装函数来将这些结构用作可变函数。

**示例 \#1 可变函数示例**

``` php
<?php
function foo() {
    echo "In foo()<br />\n";
}

function bar($arg = '') {
    echo "In bar(); argument was '$arg'.<br />\n";
}

// 使用 echo 的包装函数
function echoit($string)
{
    echo $string;
}

$func = 'foo';
$func();        // This calls foo()

$func = 'bar';
$func('test');  // This calls bar()

$func = 'echoit';
$func('test');  // This calls echoit()
?>
```

也可以用可变函数的语法来调用一个对象的方法。

**示例 \#2 可变方法范例**

``` php
<?php
class Foo
{
    function Variable()
    {
        $name = 'Bar';
        $this->$name(); // This calls the Bar() method
    }

    function Bar()
    {
        echo "This is Bar";
    }
}

$foo = new Foo();
$funcname = "Variable";
$foo->$funcname();   // This calls $foo->Variable()

?>
```

当调用静态方法时，函数调用要比静态属性优先：

**示例 \#3 Variable 方法和静态属性示例**

``` php
<?php
class Foo
{
    static $variable = 'static property';
    static function Variable()
    {
        echo 'Method Variable called';
    }
}

echo Foo::$variable; // This prints 'static property'. It does need a $variable in this scope.
$variable = "Variable";
Foo::$variable();  // This calls $foo->Variable() reading $variable in this scope.

?>
```

**示例 \#4 Complex callables**

``` php
<?php
class Foo
{
    static function bar()
    {
        echo "bar\n";
    }
    function baz()
    {
        echo "baz\n";
    }
}

$func = array("Foo", "bar");
$func(); // prints "bar"
$func = array(new Foo, "baz");
$func(); // prints "baz"
$func = "Foo::bar";
$func(); // prints "bar"
?>
```

### 参见

-   <span class="function">is\_callable</span>
-   <span class="function">call\_user\_func</span>
-   <span class="function">function\_exists</span>
-   <a href="/language/variables/variable.html" class="link">variable variables</a>
