\_\_autoload
============

尝试加载未定义的类

**Warning**

本特性已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本特性。

### 说明

<span class="type">void</span> <span
class="methodname">\_\_autoload</span> ( <span class="methodparam"><span
class="type">string</span> `$class`</span> )

你可以通过定义这个函数来启用<a href="/language/oop5/autoload.html" class="link">类的自动加载</a>。

### 参数

`class`  
待加载的类名。

### 返回值

没有返回值。

### 参见

-   <span class="function">spl\_autoload\_register</span>

class\_alias
============

为一个类创建别名

### 说明

<span class="type">bool</span> <span
class="methodname">class\_alias</span> ( <span class="methodparam"><span
class="type">string</span> `$original`</span> , <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$autoload`<span class="initializer"> = **`true`**</span></span> \] )

基于用户定义的类 `original` 创建别名 `alias`。
这个别名类和原有的类完全相同。

### 参数

`original`  
原有的类。

`alias`  
类的别名。

`autoload`  
如果原始类没有加载，是否使用自动加载（autoload）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">class\_alias</span> 例子**

``` php
<?php

class foo { }

class_alias('foo', 'bar');

$a = new foo;
$b = new bar;

// the objects are the same
var_dump($a == $b, $a === $b);
var_dump($a instanceof $b);

// the classes are the same
var_dump($a instanceof foo);
var_dump($a instanceof bar);

var_dump($b instanceof foo);
var_dump($b instanceof bar);

?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(true)

### 参见

-   <span class="function">get\_parent\_class</span>
-   <span class="function">is\_subclass\_of</span>

class\_exists
=============

检查类是否已定义

### 说明

<span class="type">bool</span> <span
class="methodname">class\_exists</span> ( <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$autoload`<span class="initializer"> =
true</span></span> \] )

检查指定的类是否已定义。

### 参数

`class_name`  
类名。名字的匹配是不分区大小写的。

`autoload`  
是否默认调用
<a href="/language/oop5/autoload.html" class="link">__autoload</a>。

### 返回值

如果由 `class_name` 所指的类已经定义，此函数返回 **`true`**，否则返回
**`false`**。

### 范例

**示例 \#1 <span class="function">class\_exists</span> 例子**

``` php
<?php
// 使用前检查类是否存在
if (class_exists('MyClass')) {
    $myclass = new MyClass();
}

?>
```

**示例 \#2 `autoload` parameter 例子**

``` php
<?php
function __autoload($class)
{
    include($class . '.php');

    // Check to see whether the include declared the class
    if (!class_exists($class, false)) {
        trigger_error("Unable to load class: $class", E_USER_WARNING);
    }
}

if (class_exists('MyClass')) {
    $myclass = new MyClass();
}

?>
```

### 参见

-   <span class="function">function\_exists</span>
-   <span class="function">interface\_exists</span>
-   <span class="function">get\_declared\_classes</span>

get\_called\_class
==================

后期静态绑定（"Late Static Binding"）类的名称

### 说明

<span class="type">string</span> <span
class="methodname">get\_called\_class</span> ( <span
class="methodparam">void</span> )

获取静态方法调用的类名。

### 返回值

返回类的名称，如果不是在类中调用则返回 **`false`**。

### 范例

**示例 \#1 <span class="function">get\_called\_class</span> 的使用**

``` php
<?php

class foo {
    static public function test() {
        var_dump(get_called_class());
    }
}

class bar extends foo {
}

foo::test();
bar::test();

?>
```

以上例程会输出：

    string(3) "foo"
    string(3) "bar"

### 参见

-   <span class="function">get\_parent\_class</span>
-   <span class="function">get\_class</span>
-   <span class="function">is\_subclass\_of</span>

get\_class\_methods
===================

返回由类的方法名组成的数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_class\_methods</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class_name`</span>
)

返回由类的方法名组成的数组。

### 参数

`class_name`  
类名或者对象实例。

### 返回值

返回由 `class_name` 指定的类中定义的方法名所组成的数组。如果出错，则返回
**`null`**。

### 范例

**示例 \#1 <span class="function">get\_class\_methods</span> 示例**

``` php
<?php

class myclass {
    // constructor
    function myclass()
    {
        return(true);
    }

    // method 1
    function myfunc1()
    {
        return(true);
    }

    // method 2
    function myfunc2()
    {
        return(true);
    }
}

$class_methods = get_class_methods('myclass');
// or
$class_methods = get_class_methods(new myclass());

foreach ($class_methods as $method_name) {
    echo "$method_name\n";
}

?>
```

以上例程会输出：

    myclass
    myfunc1
    myfunc2

### 参见

-   <span class="function">get\_class</span>
-   <span class="function">get\_class\_vars</span>
-   <span class="function">get\_object\_vars</span>

get\_class\_vars
================

返回由类的默认属性组成的数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_class\_vars</span> ( <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> )

返回由类的默认公有属性组成的关联数组。

### 参数

`class_name`  
类名

### 返回值

Returns an associative array of declared properties visible from the
current scope, with their default value. The resulting array elements
are in the form of *varname =\> value*. In case of an error, it returns
**`false`**.

### 范例

**示例 \#1 <span class="function">get\_class\_vars</span> example**

``` php
<?php

class myclass {

    var $var1; // this has no default value...
    var $var2 = "xyz";
    var $var3 = 100;
    private $var4;

    // constructor
    function __construct() {
        // change some properties
        $this->var1 = "foo";
        $this->var2 = "bar";
        return true;
    }

}

$my_class = new myclass();

$class_vars = get_class_vars(get_class($my_class));

foreach ($class_vars as $name => $value) {
    echo "$name : $value\n";
}

?>
```

以上例程会输出：

    var1 :
    var2 : xyz
    var3 : 100

**示例 \#2 <span class="function">get\_class\_vars</span> and scoping
behaviour**

``` php
<?php
function format($array)
{
    return implode('|', array_keys($array)) . "\r\n";
}

class TestCase
{
    public $a    = 1;
    protected $b = 2;
    private $c   = 3;

    public static function expose()
    {
        echo format(get_class_vars(__CLASS__));
    }
}

TestCase::expose();
echo format(get_class_vars('TestCase'));
?>
```

以上例程会输出：

    // 5.0.0
    a| * b| TestCase c
    a| * b| TestCase c

    // 5.0.1 - 5.0.2
    a|b|c
    a|b|c

    // 5.0.3 +
    a|b|c
    a

### 参见

-   <span class="function">get\_class\_methods</span>
-   <span class="function">get\_object\_vars</span>

get\_class
==========

返回对象的类名

### 说明

<span class="type">string</span> <span
class="methodname">get\_class</span> (\[ <span class="methodparam"><span
class="type">object</span> `$object`<span class="initializer"> =
**`null`**</span></span> \] )

返回对象实例 `object` 所属类的名字。

### 参数

`object`  
要测试的对象。如果在类里，此参数可以省略。

### 返回值

返回对象实例 `object` 所属类的名字。 如果 `object` 不是一个对象则返回
**`false`**。

如果在一个类里，省略了参数 `object`， 则返回当前所在类的名称。

如果 `object` 是命名空间中某个类的实例，则会返回带上命名空间的类名。

### 错误／异常

如果用其他类型调用 <span
class="function">get\_class</span>，而不是一个对象的话，就会产生
**`E_WARNING`** 级别的错误。

### 更新日志

| 版本     | 说明                                                                                                      |
|----------|-----------------------------------------------------------------------------------------------------------|
| 5.3.0 起 | `object` 默认参数现在是 **`null`** ，所以，现在传入 **`null`** 到 `object` 参数时，和没传参数的结果一样。 |

### 范例

**示例 \#1 使用 <span class="function">get\_class</span>**

``` php
<?php

class foo {
    function name()
    {
        echo "My name is " , get_class($this) , "\n";
    }
}

// create an object
$bar = new foo();

// external call
echo "Its name is " , get_class($bar) , "\n";

// internal call
$bar->name();

?>
```

以上例程会输出：

    Its name is foo
    My name is foo

**示例 \#2 超类中使用 <span class="function">get\_class</span>**

``` php
<?php

abstract class bar {
    public function __construct()
    {
        var_dump(get_class($this));
        var_dump(get_class());
    }
}

class foo extends bar {
}

new foo;

?>
```

以上例程会输出：

    string(3) "foo"
    string(3) "bar"

**示例 \#3 命名空间中的类使用 <span class="function">get\_class</span>**

``` php
<?php

namespace Foo\Bar;

class Baz {
    public function __construct()
    {

    }
}

$baz = new \Foo\Bar\Baz;

var_dump(get_class($baz));
?>
```

以上例程会输出：

    string(11) "Foo\Bar\Baz"

### 参见

-   <span class="function">get\_called\_class</span>
-   <span class="function">get\_parent\_class</span>
-   <span class="function">gettype</span>
-   <span class="function">is\_subclass\_of</span>

get\_declared\_classes
======================

返回由已定义类的名字所组成的数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_declared\_classes</span> ( <span
class="methodparam">void</span> )

返回由当前脚本中已定义类的名字组成的数组。

### 返回值

返回由当前脚本中已定义类的名字组成的数组。

> **Note**:
>
> 需要注意的是额外类的出现依赖于你已编译到 PHP
> 中的库。这意味着你不能使用这些类名定义自己的类。在附录的
> <a href="/reserved/classes.html" class="link">预定义类</a>
> 部分有预定义类的列表。

### 范例

**示例 \#1 <span class="function">get\_declared\_classes</span> 例子**

``` php
<?php
print_r(get_declared_classes());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => stdClass
        [1] => __PHP_Incomplete_Class
        [2] => Directory
    )

### 参见

-   <span class="function">class\_exists</span>
-   <span class="function">get\_declared\_interfaces</span>
-   <span class="function">get\_defined\_functions</span>

get\_declared\_interfaces
=========================

返回一个数组包含所有已声明的接口

### 说明

<span class="type">array</span> <span
class="methodname">get\_declared\_interfaces</span> ( <span
class="methodparam">void</span> )

返回一个数组包含所有已声明的接口。

### 返回值

本函数返回一个数组，其内容是当前脚本中所有已声明的接口的名字。

### 范例

**示例 \#1 <span class="function">get\_declared\_interfaces</span>
例子**

``` php
<?php
print_r(get_declared_interfaces());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Traversable
        [1] => IteratorAggregate
        [2] => Iterator
        [3] => ArrayAccess
        [4] => reflector
        [5] => RecursiveIterator
        [6] => SeekableIterator
    )

### 参见

-   <span class="function">interface\_exists</span>
-   <span class="function">get\_declared\_classes</span>
-   <span class="function">class\_implements</span>

get\_declared\_traits
=====================

返回所有已定义的 traits 的数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_declared\_traits</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

返回一个数组，其值包含了所有已定义的 traits 的名称。 在失败的情况下返回
**`null`**。

### 参见

-   <span class="function">class\_uses</span>
-   <span class="function">trait\_exists</span>

get\_object\_vars
=================

返回由对象属性组成的关联数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_object\_vars</span> ( <span
class="methodparam"><span class="type">object</span> `$obj`</span> )

返回由 `obj` 指定的对象中定义的属性组成的关联数组。

> **Note**:
>
> 在 PHP 4.2.0 之前的版本中，如果在 `obj`
> 对象实例中声明的变量没有被赋值，则它们将不会在返回的数组中。而在 PHP
> 4.2.0 之后，这些变量作为键名将被赋予 **`null`** 值。

**示例 \#1 使用 <span class="function">get\_object\_vars</span>**

``` php
<?php
class Point2D {
    var $x, $y;
    var $label;

    function Point2D($x, $y)
    {
        $this->x = $x;
        $this->y = $y;
    }

    function setLabel($label)
    {
        $this->label = $label;
    }

    function getPoint()
    {
        return array("x" => $this->x,
                     "y" => $this->y,
                     "label" => $this->label);
    }
}

// "$label" is declared but not defined
$p1 = new Point2D(1.233, 3.445);
print_r(get_object_vars($p1));

$p1->setLabel("point #1");
print_r(get_object_vars($p1));

?>
```

以上例程会输出：

     Array
     (
         [x] => 1.233
         [y] => 3.445
         [label] =>
     )

     Array
     (
         [x] => 1.233
         [y] => 3.445
         [label] => point #1
     )

参见 <span class="function">get\_class\_methods</span> 和 <span
class="function">get\_class\_vars</span>。

### 参数

`object`  
An object instance.

### 返回值

Returns an associative array of defined object accessible non-static
properties for the specified `object` in scope. If a property have not
been assigned a value, it will be returned with a **`null`** value.

### 更新日志

| 版本           | 说明                                                                                                                                                 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0          | This function now returns <span class="type">NULL</span> if the `object` isn't an object.                                                            |
| prior to 5.3.0 | If the `object` isn't an object, then <span class="function">get\_object\_vars</span> would return **`false`**                                       |
| prior to 4.2.0 | If the variables declared in the class of which the `object` is an instance, have not been assigned a value, those will not be returned in the array |

### 范例

**示例 \#2 Use of <span class="function">get\_object\_vars</span>**

``` php
<?php

class foo {
    private $a;
    public $b = 1;
    public $c;
    private $d;
    static $e;
   
    public function test() {
        var_dump(get_object_vars($this));
    }
}

$test = new foo;
var_dump(get_object_vars($test));

$test->test();

?>
```

以上例程会输出：

    array(2) {
      ["b"]=>
      int(1)
      ["c"]=>
      NULL
    }
    array(4) {
      ["a"]=>
      NULL
      ["b"]=>
      int(1)
      ["c"]=>
      NULL
      ["d"]=>
      NULL
    }

### 参见

-   <span class="function">get\_class\_methods</span>
-   <span class="function">get\_class\_vars</span>

get\_parent\_class
==================

返回对象或类的父类名

### 说明

<span class="type">string</span> <span
class="methodname">get\_parent\_class</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$obj`</span> \] )

如果 `obj` 是对象，则返回对象实例 `obj` 所属类的父类名。

如果 `obj` 是字符串，则返回以此字符串为名的类的父类名。此功能是在 PHP
4.0.5 中增加的。

> **Note**:
>
> 自 PHP 5 起，如果在对象的方法内调用，则 `obj` 为可选项。

**示例 \#1 使用 <span class="function">get\_parent\_class</span>**

``` php
<?php

class dad {
    function dad()
    {
    // implements some logic
    }
}

class child extends dad {
    function child()
    {
        echo "I'm " , get_parent_class($this) , "'s son\n";
    }
}

class child2 extends dad {
    function child2()
    {
        echo "I'm " , get_parent_class('child2') , "'s son too\n";
    }
}

$foo = new child();
$bar = new child2();

?>
```

以上例程会输出：

    I'm dad's son
    I'm dad's son too

参见 <span class="function">get\_class</span> 和 <span
class="function">is\_subclass\_of</span>。

### 参数

`object`  
The tested object or class name

### 返回值

Returns the name of the parent class of the class of which `object` is
an instance or the name.

> **Note**:
>
> If the object does not have a parent or the class given does not exist
> **`false`** will be returned.

If called without parameter outside object, this function returns
**`false`**.

### 更新日志

| 版本         | 说明                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|
| Before 5.1.0 | If called without parameter outside object, this function would have returned **`null`** with a warning. |
| Since 5.0.0  | The `object` parameter is optional if called from the object's method.                                   |
| Since 4.0.5  | If `object` is a string, returns the name of the parent class of the class with that name.               |

### 范例

**示例 \#2 Using <span class="function">get\_parent\_class</span>**

``` php
<?php

class dad {
    function dad()
    {
    // implements some logic
    }
}

class child extends dad {
    function child()
    {
        echo "I'm " , get_parent_class($this) , "'s son\n";
    }
}

class child2 extends dad {
    function child2()
    {
        echo "I'm " , get_parent_class('child2') , "'s son too\n";
    }
}

$foo = new child();
$bar = new child2();

?>
```

以上例程会输出：

    I'm dad's son
    I'm dad's son too

### 参见

-   <span class="function">get\_class</span>
-   <span class="function">is\_subclass\_of</span>

interface\_exists
=================

检查接口是否已被定义

### 说明

<span class="type">bool</span> <span
class="methodname">interface\_exists</span> ( <span
class="methodparam"><span class="type">string</span>
`$interface_name`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$autoload`<span class="initializer"> =
true</span></span> \] )

检查接口是否已被定义。

### 参数

`interface_name`  
接口名。

`autoload`  
默认是否调用
<a href="/language/oop5/autoload.html" class="link">__autoload</a>。

### 返回值

本函数在由 `interface_name` 给出的接口已定义时返回 **`true`**，否则返回
**`false`**。

### 范例

**示例 \#1 <span class="function">interface\_exists</span> 例子**

``` php
<?php
// 在尝试使用前先检查接口是否存在
if (interface_exists('MyInterface')) {
    class MyClass implements MyInterface
    {
        // Methods
    }
}

?>
```

### 参见

-   <span class="function">get\_declared\_interfaces</span>
-   <span class="function">class\_implements</span>
-   <span class="function">class\_exists</span>

is\_a
=====

如果对象属于该类或该类是此对象的父类则返回 **`true`**

### 说明

<span class="type">bool</span> <span class="methodname">is\_a</span> (
<span class="methodparam"><span class="type">mixed</span>
`$object`</span> , <span class="methodparam"><span
class="type">string</span> `$class_name`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$allow_string`<span
class="initializer"> = **`false`**</span></span> \] )

如果 `object` 是该类或该类是此对象的父类。

### 参数

`object`  
类名或者实例对象。

`class_name`  
类名

`allow_string`  
如果本参数设置为 **`false`**，`object` 就不允许传入字符串类名。
这也会在类不存在时，阻止调用自动加载器（autoloader）。

### 返回值

如果对象属于该类或该类是此对象的父类时返回 **`true`**，否则返回
**`false`**。

### 范例

**示例 \#1 <span class="function">is\_a</span> 例子**

``` php
<?php
// define a class
class WidgetFactory
{
  var $oink = 'moo';
}

// create a new object
$WF = new WidgetFactory();

if (is_a($WF, 'WidgetFactory')) {
  echo "yes, \$WF is still a WidgetFactory\n";
}
?>
```

**示例 \#2 在 PHP 5 中使用 *instanceof* 运算符**

``` php
<?php
if ($WF instanceof WidgetFactory) {
    echo 'Yes, $WF is a WidgetFactory';
}
?>
```

### 参见

-   <span class="function">get\_class</span>
-   <span class="function">get\_parent\_class</span>
-   <span class="function">is\_subclass\_of</span>

is\_subclass\_of
================

如果此对象是该类的子类，则返回 **`true`**

### 说明

<span class="type">bool</span> <span
class="methodname">is\_subclass\_of</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> ,
<span class="methodparam"><span class="type">string</span>
`$class_name`</span> )

如果对象 `object` 所属类是类 `class_name` 的子类，则返回
**`true`**，否则返回 **`false`**。

> **Note**:
>
> 自 PHP 5.0.3 起也可以用一个字符串来指定 `object` 参数（类名）。

**示例 \#1 <span class="function">is\_subclass\_of</span> 例子**

``` php
<?php
// define a class
class WidgetFactory
{
  var $oink = 'moo';
}

// define a child class
class WidgetFactory_Child extends WidgetFactory
{
  var $oink = 'oink';
}

// create a new object
$WF = new WidgetFactory();
$WFC = new WidgetFactory_Child();

if (is_subclass_of($WFC, 'WidgetFactory')) {
  echo "yes, \$WFC is a subclass of WidgetFactory\n";
} else {
  echo "no, \$WFC is not a subclass of WidgetFactory\n";
}

if (is_subclass_of($WF, 'WidgetFactory')) {
  echo "yes, \$WF is a subclass of WidgetFactory\n";
} else {
  echo "no, \$WF is not a subclass of WidgetFactory\n";
}

// usable only since PHP 5.0.3
if (is_subclass_of('WidgetFactory_Child', 'WidgetFactory')) {
  echo "yes, WidgetFactory_Child is a subclass of WidgetFactory\n";
} else {
  echo "no, WidgetFactory_Child is not a subclass of WidgetFactory\n";
}
?>
```

以上例程会输出：

    yes, $WFC is a subclass of WidgetFactory
    no, $WF is not a subclass of WidgetFactory
    yes, WidgetFactory_Child is a subclass of WidgetFactory

参见 <span class="function">get\_class</span>、 <span
class="function">get\_parent\_class</span> 和 <span
class="function">is\_a</span>。

### 参数

`object`  
A class name or an object instance

`class_name`  
The class name

`allow_string`  
If this parameter set to false, string class name as `object` is not
allowed. This also prevents from calling autoloader if the class doesn't
exist.

### 返回值

This function returns **`true`** if the object `object`, belongs to a
class which is a subclass of `class_name`, **`false`** otherwise.

### 范例

**示例 \#2 <span class="function">is\_subclass\_of</span> example**

``` php
<?php
// define a class
class WidgetFactory
{
  var $oink = 'moo';
}

// define a child class
class WidgetFactory_Child extends WidgetFactory
{
  var $oink = 'oink';
}

// create a new object
$WF = new WidgetFactory();
$WFC = new WidgetFactory_Child();

if (is_subclass_of($WFC, 'WidgetFactory')) {
  echo "yes, $WFC is a subclass of WidgetFactory\n";
} else {
  echo "no, $WFC is not a subclass of WidgetFactory\n";
}


if (is_subclass_of($WF, 'WidgetFactory')) {
  echo "yes, $WF is a subclass of WidgetFactory\n";
} else {
  echo "no, $WF is not a subclass of WidgetFactory\n";
}


// usable only since PHP 5.0.3
if (is_subclass_of('WidgetFactory_Child', 'WidgetFactory')) {
  echo "yes, WidgetFactory_Child is a subclass of WidgetFactory\n";
} else {
  echo "no, WidgetFactory_Child is not a subclass of WidgetFactory\n";
}
?>
```

以上例程会输出：

    yes, $WFC is a subclass of WidgetFactory
    no, $WF is not a subclass of WidgetFactory
    yes, WidgetFactory_Child is a subclass of WidgetFactory

### 注释

> **Note**:
>
> 如果此类不是已知类，使用此函数会使用任何已注册的
> <a href="/language/oop5/autoload.html" class="link">autoloader</a>。

### 参见

-   <span class="function">get\_class</span>
-   <span class="function">get\_parent\_class</span>
-   <span class="function">is\_a</span>
-   <span class="function">class\_parents</span>

method\_exists
==============

检查类的方法是否存在

### 说明

<span class="type">bool</span> <span
class="methodname">method\_exists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$object`</span> ,
<span class="methodparam"><span class="type">string</span>
`$method_name`</span> )

检查类的方法是否存在于指定的 `object`中。

### 参数

`object`  
对象示例或者类名。

`method_name`  
方法名。

### 返回值

如果 `method_name` 所指的方法在 `object` 所指的对象类中已定义，则返回
**`true`**，否则返回 **`false`**。

### 注释

> **Note**:
>
> 如果此类不是已知类，使用此函数会使用任何已注册的
> <a href="/language/oop5/autoload.html" class="link">autoloader</a>。

### 范例

**示例 \#1 <span class="function">method\_exists</span> 例子**

``` php
<?php
$directory = new Directory('.');
var_dump(method_exists($directory,'read'));
?>
```

以上例程会输出：

    bool(true)

**示例 \#2 Static <span class="function">method\_exists</span> 例子**

``` php
<?php
var_dump(method_exists('Directory','read'));
?>
```

以上例程会输出：

    bool(true)

### 参见

-   <span class="function">function\_exists</span>
-   <span class="function">is\_callable</span>
-   <span class="function">class\_exists</span>

property\_exists
================

检查对象或类是否具有该属性

### 说明

<span class="type">bool</span> <span
class="methodname">property\_exists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$property`</span> )

本函数检查给出的 `property`
是否存在于指定的类中（以及是否能在当前范围内访问）。

> **Note**:
>
> As opposed with <span class="function">isset</span>, <span
> class="function">property\_exists</span> returns **`true`** even if
> the property has the value **`null`**.

### 参数

`class`  
字符串形式的类名或要检查的类的一个对象

`property`  
属性的名字

### 返回值

如果该属性存在则返回 **`true`**，如果不存在则返回 **`false`**，出错返回
**`null`**。

### 注释

> **Note**:
>
> 如果此类不是已知类，使用此函数会使用任何已注册的
> <a href="/language/oop5/autoload.html" class="link">autoloader</a>。

> **Note**:
>
> The <span class="function">property\_exists</span> function cannot
> detect properties that are magically accessible using the
> <a href="/language/oop5/overloading.html#language.oop5.overloading.members" class="link"><em>__get</em></a>
> magic method.

### 更新日志

| 版本  | 说明                                                                           |
|-------|--------------------------------------------------------------------------------|
| 5.3.0 | This function checks the existence of a property independent of accessibility. |

### 范例

**示例 \#1 A <span class="function">property\_exists</span> example**

``` php
<?php

class myClass {
    public $mine;
    private $xpto;
    static protected $test;

    static function test() {
        var_dump(property_exists('myClass', 'xpto')); //true
    }
}

var_dump(property_exists('myClass', 'mine'));   //true
var_dump(property_exists(new myClass, 'mine')); //true
var_dump(property_exists('myClass', 'xpto'));   //true, as of PHP 5.3.0
var_dump(property_exists('myClass', 'bar'));    //false
var_dump(property_exists('myClass', 'test'));   //true, as of PHP 5.3.0
myClass::test();

?>
```

### 参见

-   <span class="function">method\_exists</span>

trait\_exists
=============

检查指定的 trait 是否存在

### 说明

<span class="type">bool</span> <span
class="methodname">trait\_exists</span> ( <span
class="methodparam"><span class="type">string</span> `$traitname`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$autoload`</span> \] )

### 参数

`traitname`  
待检查的 trait 的名称

`autoload`  
如果尚未加载，是否使用自动加载（autoload）。

### 返回值

如果 trait 存在返回 **`true`**，不存在则返回
**`false`**。发生错误的时候返回 **`null`**。

**目录**

-   [\_\_autoload](/ref/classobj.html#__autoload) — 尝试加载未定义的类
-   [class\_alias](/ref/classobj.html#class_alias) — 为一个类创建别名
-   [class\_exists](/ref/classobj.html#class_exists) — 检查类是否已定义
-   [get\_called\_class](/ref/classobj.html#get_called_class) —
    后期静态绑定（"Late Static Binding"）类的名称
-   [get\_class\_methods](/ref/classobj.html#get_class_methods) —
    返回由类的方法名组成的数组
-   [get\_class\_vars](/ref/classobj.html#get_class_vars) —
    返回由类的默认属性组成的数组
-   [get\_class](/ref/classobj.html#get_class) — 返回对象的类名
-   [get\_declared\_classes](/ref/classobj.html#get_declared_classes) —
    返回由已定义类的名字所组成的数组
-   [get\_declared\_interfaces](/ref/classobj.html#get_declared_interfaces)
    — 返回一个数组包含所有已声明的接口
-   [get\_declared\_traits](/ref/classobj.html#get_declared_traits) —
    返回所有已定义的 traits 的数组
-   [get\_object\_vars](/ref/classobj.html#get_object_vars) —
    返回由对象属性组成的关联数组
-   [get\_parent\_class](/ref/classobj.html#get_parent_class) —
    返回对象或类的父类名
-   [interface\_exists](/ref/classobj.html#interface_exists) —
    检查接口是否已被定义
-   [is\_a](/ref/classobj.html#is_a) —
    如果对象属于该类或该类是此对象的父类则返回 true
-   [is\_subclass\_of](/ref/classobj.html#is_subclass_of) —
    如果此对象是该类的子类，则返回 true
-   [method\_exists](/ref/classobj.html#method_exists) —
    检查类的方法是否存在
-   [property\_exists](/ref/classobj.html#property_exists) —
    检查对象或类是否具有该属性
-   [trait\_exists](/ref/classobj.html#trait_exists) — 检查指定的 trait
    是否存在
