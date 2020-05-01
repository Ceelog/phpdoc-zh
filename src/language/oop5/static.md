Static（静态）关键字
--------------------

**小贴士**

本页说明了用 *static* 关键字来定义静态方法和属性。*static*
也可用于<a href="/language/variables/scope.html#language.variables.scope.static" class="link">定义静态变量</a>以及<a href="/language/oop5/late-static-bindings.html" class="link">后期静态绑定</a>。参见上述页面了解
*static* 在其中的用法。

声明类属性或方法为静态，就可以不实例化类而直接访问。静态属性不能通过一个类已实例化的对象来访问（但静态方法可以）。

为了兼容 PHP
4，如果没有指定<a href="/language/oop5/visibility.html" class="link">访问控制</a>，属性和方法默认为公有。

由于静态方法不需要通过对象即可调用，所以伪变量 `$this`
在静态方法中不可用。

静态属性不可以由对象通过 -\> 操作符来访问。

用静态方式调用一个非静态方法会导致一个 **`E_STRICT`** 级别的错误。

就像其它所有的 PHP
静态变量一样，静态属性只能被初始化为文字或常量，不能使用表达式。所以可以把静态属性初始化为整数或数组，但不能初始化为另一个变量或函数返回值，也不能指向一个对象。

自 PHP 5.3.0 起，可以用一个变量来动态调用类。但该变量的值不能为关键字
*self*，*parent* 或 *static*。

**示例 \#1 静态属性示例**

``` php
<?php
class Foo
{
    public static $my_static = 'foo';

    public function staticValue() {
        return self::$my_static;
    }
}

class Bar extends Foo
{
    public function fooStatic() {
        return parent::$my_static;
    }
}


print Foo::$my_static . "\n";

$foo = new Foo();
print $foo->staticValue() . "\n";
print $foo->my_static . "\n";      // Undefined "Property" my_static 

print $foo::$my_static . "\n";
$classname = 'Foo';
print $classname::$my_static . "\n"; // As of PHP 5.3.0

print Bar::$my_static . "\n";
$bar = new Bar();
print $bar->fooStatic() . "\n";
?>
   </programlisting>
  </example>

  <example>
   <title>静态方法示例</title>
    <programlisting role="php">
<![CDATA[
<?php
class Foo {
    public static function aStaticMethod() {
        // ...
    }
}

Foo::aStaticMethod();
$classname = 'Foo';
$classname::aStaticMethod(); // 自 PHP 5.3.0 起
?>
```
