类型运算符
----------

*instanceof* 用于确定一个 PHP 变量是否属于某一类
<a href="/language/oop5/basic.html#language.oop5.basic.class" class="link">class</a>
的实例：

**示例 \#1 对类使用 *instanceof***

``` php
<?php
class MyClass
{
}

class NotMyClass
{
}
$a = new MyClass;

var_dump($a instanceof MyClass);
var_dump($a instanceof NotMyClass);
?>
```

以上例程会输出：

    bool(true)
    bool(false)

*instanceof*　也可用来确定一个变量是不是继承自某一父类的子类的实例：

**示例 \#2 对继承类使用 *instanceof***

``` php
<?php
class ParentClass
{
}

class MyClass extends ParentClass
{
}

$a = new MyClass;

var_dump($a instanceof MyClass);
var_dump($a instanceof ParentClass);
?>
```

以上例程会输出：

    bool(true)
    bool(true)

检查一个对象是否*不是*某个类的实例，可以使用<a href="/language/operators/logical.html" class="link">逻辑运算符 <em>not</em></a>。

**示例 \#3 使用 *instanceof* 检查对象*不是*某个类的实例**

``` php
<?php
class MyClass
{
}

$a = new MyClass;
var_dump(!($a instanceof stdClass));
?>
```

以上例程会输出：

    bool(true)

最后，*instanceof*也可用于确定一个变量是不是实现了某个<a href="/language/oop5/interfaces.html" class="link">接口</a>的对象的实例:

**示例 \#4 对接口使用 *instanceof***

``` php
<?php
interface MyInterface
{
}

class MyClass implements MyInterface
{
}

$a = new MyClass;

var_dump($a instanceof MyClass);
var_dump($a instanceof MyInterface);
?>
```

以上例程会输出：

    bool(true)
    bool(true)

虽然 *instanceof* 通常直接与类名一起使用，但也可以使用对象或字符串变量：

**示例 \#5 对其它变量使用 *instanceof***

``` php
<?php
interface MyInterface
{
}

class MyClass implements MyInterface
{
}

$a = new MyClass;
$b = new MyClass;
$c = 'MyClass';
$d = 'NotMyClass';

var_dump($a instanceof $b); // $b is an object of class MyClass
var_dump($a instanceof $c); // $c is a string 'MyClass'
var_dump($a instanceof $d); // $d is a string 'NotMyClass'
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)

如果被检测的变量不是对象，instanceof 并不发出任何错误信息而是返回
**`FALSE`**。PHP 7.3.0 之前不允许用于检测常量。

**示例 \#6 用 *instanceof* 检测其它变量**

``` php
<?php
$a = 1;
$b = NULL;
$c = imagecreate(5, 5);
var_dump($a instanceof stdClass); // $a is an integer
var_dump($b instanceof stdClass); // $b is NULL
var_dump($c instanceof stdClass); // $c is a resource
var_dump(FALSE instanceof stdClass);
?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(false)
    PHP Fatal error:  instanceof expects an object instance, constant given

PHP 7.3.0 起， *instanceof* 操作符的左侧可以放常量。

**示例 \#7 使用 *instanceof* 测试常量**

``` php
<?php
var_dump(FALSE instanceof stdClass);
?>
```

以上例程在 PHP 7.3 中的输出：

    bool(false)

然而 instanceof 的使用还有一些陷阱必须了解。在 PHP 5.1.0
之前，如果要检查的类名称不存在，*instanceof* 会调用 <span
class="function">\_\_autoload</span>。另外，如果该类没有被装载则会产生一个致命错误。可以通过使用动态类引用或用一个包含类名的字符串变量来避开这种问题：

**示例 \#8 避免 PHP 5.0 中 instanceof 引起的类名查找和致命错误问题**

``` php
<?php
$d = 'NotMyClass';
var_dump($a instanceof $d); // no fatal error here
?>
```

以上例程会输出：

    bool(false)

*instanceof* 运算符是 PHP 5 引进的。在此之前用 <span
class="function">is\_a</span>，但是后来 <span
class="function">is\_a</span> 被废弃而用 *instanceof* 替代了。注意自 PHP
5.3.0 起，又恢复使用 <span class="function">is\_a</span> 了。

参见 <span class="function">get\_class</span> 和 <span
class="function">is\_a</span>。
