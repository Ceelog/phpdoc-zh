基本概念
--------

### class

每个类的定义都以关键字 *class*
开头，后面跟着类名，后面跟着一对花括号，里面包含有类的属性与方法的定义。

类名可以是任何非 PHP
<a href="/reserved.html" class="link">保留字</a>的合法标签。一个合法类名以字母或下划线开头，后面跟着若干字母，数字或下划线。以正则表达式表示为：*\[a-zA-Z\_\\x7f-\\xff\]\[a-zA-Z0-9\_\\x7f-\\xff\]\**。

一个类可以包含有属于自己的<a href="/language/oop5/constants.html" class="link">常量</a>，<a href="/language/oop5/properties.html" class="link">变量</a>（称为“属性”）以及函数（称为“方法”）。

**示例 \#1 简单的类定义**

``` php
<?php
class SimpleClass
{
    // 声明属性
    public $var = 'a default value';

    // 声明方法
    public function displayVar() {
        echo $this->var;
    }
}
?>
```

当一个方法在类定义内部被调用时，有一个可用的伪变量 `$this`。`$this`
是一个到主叫对象的引用（通常是该方法所从属的对象，但如果是从第二个对象<a href="/language/oop5/static.html" class="link">静态</a>调用时也可能是另一个对象）。

**示例 \#2 `$this` 伪变量的示例**

We're assuming that error\_reporting is disabled for this example;
otherwise the following code would trigger deprecated and strict
notices, respectively, depending on the PHP version.

``` php
<?php
class A
{
    function foo()
    {
        if (isset($this)) {
            echo '$this is defined (';
            echo get_class($this);
            echo ")\n";
        } else {
            echo "\$this is not defined.\n";
        }
    }
}

class B
{
    function bar()
    {
        A::foo();
    }
}

$a = new A();
$a->foo();

A::foo();

$b = new B();
$b->bar();

B::bar();
?>
```

Output of the above example in PHP 5:

    $this is defined (A)
    $this is not defined.
    $this is defined (B)
    $this is not defined.

Output of the above example in PHP 7:

    $this is defined (A)
    $this is not defined.
    $this is not defined.
    $this is not defined.

### new

要创建一个类的实例，必须使用 *new*
关键字。当创建新对象时该对象总是被赋值，除非该对象定义了<a href="/language/oop5/decon.html" class="link">构造函数</a>并且在出错时抛出了一个<a href="/language/exceptions.html" class="link">异常</a>。类应在被实例化之前定义（某些情况下则必须这样）。

如果在 *new* 之后跟着的是一个包含有类名的字符串 <span
class="type">string</span>，则该类的一个实例被创建。如果该类属于一个命名空间，则必须使用其完整名称。

**示例 \#3 创建实例**

``` php
<?php
$instance = new SimpleClass();

// 也可以这样做：
$className = 'Foo';
$instance = new $className(); // Foo()
?>
```

在类定义内部，可以用 *new self* 和 *new parent* 创建新对象。

当把一个对象已经创建的实例赋给一个新变量时，新变量会访问同一个实例，就和用该对象赋值一样。此行为和给函数传递入实例时一样。可以用<a href="/language/oop5/cloning.html" class="link">克隆</a>给一个已创建的对象建立一个新实例。

**示例 \#4 对象赋值**

``` php
<?php

$instance = new SimpleClass();

$assigned   =  $instance;
$reference  =& $instance;

$instance->var = '$assigned will have this value';

$instance = null; // $instance and $reference become null

var_dump($instance);
var_dump($reference);
var_dump($assigned);
?>
```

以上例程会输出：

    NULL
    NULL
    object(SimpleClass)#1 (1) {
       ["var"]=>
         string(30) "$assigned will have this value"
    }

PHP 5.3.0 引进了两个新方法来创建一个对象的实例：

**示例 \#5 创建新对象**

``` php
<?php
class Test
{
    static public function getNew()
    {
        return new static;
    }
}

class Child extends Test
{}

$obj1 = new Test();
$obj2 = new $obj1;
var_dump($obj1 !== $obj2);

$obj3 = Test::getNew();
var_dump($obj3 instanceof Test);

$obj4 = Child::getNew();
var_dump($obj4 instanceof Child);
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(true)

PHP 5.4.0 起，可以通过一个表达式来访问新创建对象的成员：

**示例 \#6 访问新创建对象的成员**

``` php
<?php
echo (new DateTime())->format('Y');
?>
```

以上例程的输出类似于：

    2016

### Properties and methods

Class properties and methods live in separate "namespaces", so it is
possible to have a property and a method with the same name. Referring
to both a property and a method has the same notation, and whether a
property will be accessed or a method will be called, solely depends on
the context, i.e. whether the usage is a variable access or a function
call.

**示例 \#7 Property access vs. method call**

``` php
<?php
class Foo
{
    public $bar = 'property';
    
    public function bar() {
        return 'method';
    }
}

$obj = new Foo();
echo $obj->bar, PHP_EOL, $obj->bar(), PHP_EOL;
```

以上例程会输出：

    property
    method

That means that calling an
<a href="/functions/anonymous.html" class="link">anonymous function</a>
which has been assigned to a property is not directly possible. Instead
the property has to be assigned to a variable first, for instance. As of
PHP 7.0.0 it is possible to call such a property directly by enclosing
it in parentheses.

**示例 \#8 Calling an anonymous function stored in a property**

``` php
<?php
class Foo
{
    public $bar;
    
    public function __construct() {
        $this->bar = function() {
            return 42;
        };
    }
}

$obj = new Foo();

// as of PHP 5.3.0:
$func = $obj->bar;
echo $func(), PHP_EOL;

// alternatively, as of PHP 7.0.0:
echo ($obj->bar)(), PHP_EOL;
```

以上例程会输出：

    42

### extends

一个类可以在声明中用 *extends*
关键字继承另一个类的方法和属性。PHP不支持多重继承，一个类只能继承一个基类。

被继承的方法和属性可以通过用同样的名字重新声明被覆盖。但是如果父类定义方法时使用了
<a href="/language/oop5/final.html" class="link">final</a>，则该方法不可被覆盖。可以通过
<a href="/language/oop5/paamayim-nekudotayim.html" class="link">parent::</a>
来访问被覆盖的方法或属性。

当覆盖方法时，参数必须保持一致否则 PHP 将发出 **`E_STRICT`**
级别的错误信息。但构造函数例外，构造函数可在被覆盖时使用不同的参数。

**示例 \#9 简单的类继承**

``` php
<?php
class ExtendClass extends SimpleClass
{
    // Redefine the parent method
    function displayVar()
    {
        echo "Extending class\n";
        parent::displayVar();
    }
}

$extended = new ExtendClass();
$extended->displayVar();
?>
```

以上例程会输出：

    Extending class
    a default value

### ::class

自 PHP 5.5 起，关键词 *class* 也可用于类名的解析。使用
*ClassName::class* 你可以获取一个字符串，包含了类 *ClassName*
的完全限定名称。这对使用了
<a href="/language/namespaces.html" class="link">命名空间</a>
的类尤其有用。

**示例 \#10 类名的解析**

``` php
<?php
namespace NS {
    class ClassName {
    }
    
    echo ClassName::class;
}
?>
```

以上例程会输出：

    NS\ClassName

> **Note**:
>
> The class name resolution using *::class* is a compile time
> transformation. That means at the time the class name string is
> created no autoloading has happened yet. As a consequence, class names
> are expanded even if the class does not exist. No error is issued in
> that case.
