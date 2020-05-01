对象复制
--------

在多数情况下，我们并不需要完全复制一个对象来获得其中属性。但有一个情况下确实需要：如果你有一个
GTK
窗口对象，该对象持有窗口相关的资源。你可能会想复制一个新的窗口，保持所有属性与原来的窗口相同，但必须是一个新的对象（因为如果不是新的对象，那么一个窗口中的改变就会影响到另一个窗口）。还有一种情况：如果对象
A 中保存着对象 B 的引用，当你复制对象 A 时，你想其中使用的对象不再是对象
B 而是 B 的一个副本，那么你必须得到对象 A 的一个副本。

对象复制可以通过 clone 关键字来完成（如果可能，这将调用对象的
<a href="/language/oop5/cloning.html#object.clone" class="link">__clone()</a>
方法）。对象中的
<a href="/language/oop5/cloning.html#object.clone" class="link">__clone()</a>
方法不能被直接调用。

    $copy_of_object = clone $object;

当对象被复制后，PHP 5 会对对象的所有属性执行一个浅复制（shallow
copy）。所有的引用属性 仍然会是一个指向原来的变量的引用。

<span class="type">void</span> <span class="methodname">\_\_clone</span>
( <span class="methodparam">void</span> )

当复制完成时，如果定义了
<a href="/language/oop5/cloning.html#object.clone" class="link">__clone()</a>
方法，则新创建的对象（复制生成的对象）中的
<a href="/language/oop5/cloning.html#object.clone" class="link">__clone()</a>
方法会被调用，可用于修改属性的值（如果有必要的话）。

**示例 \#1 复制一个对象**

``` php
<?php
class SubObject
{
    static $instances = 0;
    public $instance;

    public function __construct() {
        $this->instance = ++self::$instances;
    }

    public function __clone() {
        $this->instance = ++self::$instances;
    }
}

class MyCloneable
{
    public $object1;
    public $object2;

    function __clone()
    {
      
        // 强制复制一份this->object， 否则仍然指向同一个对象
        $this->object1 = clone $this->object1;
    }
}

$obj = new MyCloneable();

$obj->object1 = new SubObject();
$obj->object2 = new SubObject();

$obj2 = clone $obj;


print("Original Object:\n");
print_r($obj);

print("Cloned Object:\n");
print_r($obj2);

?>
```

以上例程会输出：

    Original Object:
    MyCloneable Object
    (
        [object1] => SubObject Object
            (
                [instance] => 1
            )

        [object2] => SubObject Object
            (
                [instance] => 2
            )

    )
    Cloned Object:
    MyCloneable Object
    (
        [object1] => SubObject Object
            (
                [instance] => 3
            )

        [object2] => SubObject Object
            (
                [instance] => 2
            )

    )
