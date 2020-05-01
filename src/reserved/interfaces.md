预定义接口
==========

**目录**

-   [遍历](/class/traversable.html) — Traversable（遍历）接口
-   [迭代器](/class/iterator.html) — Iterator（迭代器）接口
    -   [Iterator::current](/iterator/current.html) — 返回当前元素
    -   [Iterator::key](/iterator/key.html) — 返回当前元素的键
    -   [Iterator::next](/iterator/next.html) — 向前移动到下一个元素
    -   [Iterator::rewind](/iterator/rewind.html) —
        返回到迭代器的第一个元素
    -   [Iterator::valid](/iterator/valid.html) — 检查当前位置是否有效
-   [聚合式迭代器](/class/iteratoraggregate.html) —
    IteratorAggregate（聚合式迭代器）接口
    -   [IteratorAggregate::getIterator](/iteratoraggregate/getiterator.html)
        — 获取一个外部迭代器
-   [数组式访问](/class/arrayaccess.html) —
    ArrayAccess（数组式访问）接口
    -   [ArrayAccess::offsetExists](/arrayaccess/offsetexists.html) —
        检查一个偏移位置是否存在
    -   [ArrayAccess::offsetGet](/arrayaccess/offsetget.html) —
        获取一个偏移位置的值
    -   [ArrayAccess::offsetSet](/arrayaccess/offsetset.html) —
        设置一个偏移位置的值
    -   [ArrayAccess::offsetUnset](/arrayaccess/offsetunset.html) —
        复位一个偏移位置的值
-   [序列化](/class/serializable.html) — 序列化接口
    -   [Serializable::serialize](/serializable/serialize.html) —
        对象的字符串表示
    -   [Serializable::unserialize](/serializable/unserialize.html) —
        构造对象
-   [Closure](/class/closure.html) — Closure 类
    -   [Closure::\_\_construct](/closure/construct.html) —
        用于禁止实例化的构造函数
    -   [Closure::bind](/closure/bind.html) —
        复制一个闭包，绑定指定的$this对象和类作用域。
    -   [Closure::bindTo](/closure/bindto.html) —
        复制当前闭包对象，绑定指定的$this对象和类作用域。
-   [生成器](/class/generator.html) — 生成器类
    -   [Generator::current](/generator/current.html) — 返回当前产生的值
    -   [Generator::key](/generator/key.html) — 返回当前产生的键
    -   [Generator::next](/generator/next.html) — 生成器继续执行
    -   [Generator::rewind](/generator/rewind.html) — 重置迭代器
    -   [Generator::send](/generator/send.html) — 向生成器中传入一个值
    -   [Generator::throw](/generator/throw.html) —
        向生成器中抛入一个异常
    -   [Generator::valid](/generator/valid.html) — 检查迭代器是否被关闭
    -   [Generator::\_\_wakeup](/generator/wakeup.html) — 序列化回调

参见 <a href="/spl/interfaces.html" class="link">SPL 接口</a> 和
<a href="/reserved/classes.html" class="link">预定义类</a>

简介
----

检测一个类是否可以使用
<a href="/control-structures/foreach.html" class="link">foreach</a>
进行遍历的接口。

无法被单独实现的基本抽象接口。相反它必须由 <span
class="classname">IteratorAggregate</span> 或 <span
class="classname">Iterator</span> 接口实现。

> **Note**:
>
> 实现此接口的内建类可以使用
> <a href="/control-structures/foreach.html" class="link">foreach</a>
> 进行遍历而无需实现 <span class="classname">IteratorAggregate</span> 或
> <span class="classname">Iterator</span> 接口。

> **Note**:
>
> 这是一个无法在 PHP 脚本中实现的内部引擎接口。<span
> class="classname">IteratorAggregate</span> 或 <span
> class="classname">Iterator</span> 接口可以用来代替它。

接口摘要
--------

**Traversable**

<span class="ooclass"> class **Traversable** </span> {

}

这个接口没有任何方法，它的作用仅仅是作为所有可遍历类的基本接口。

简介
----

可在内部迭代自己的外部迭代器或类的接口。

接口摘要
--------

**Iterator**

<span class="ooclass"> class **Iterator** </span> <span class="ooclass">
<span class="modifier">extends</span> **Traversable** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">scalar</span> <span
class="methodname">key</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">next</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">rewind</span> ( <span class="methodparam">void</span>
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">valid</span> ( <span class="methodparam">void</span>
)

}

预定义迭代器
------------

PHP 已经提供了一些用于日常任务的迭代器。 详细列表参见
<a href="/spl/iterators.html" class="link">SPL 迭代器</a>。

范例
----

**示例 \#1 基本用法**

这个例子展示了使用
<a href="/control-structures/foreach.html" class="link">foreach</a>
时，迭代器方法的调用顺序。

``` php
<?php
class myIterator implements Iterator {
    private $position = 0;
    private $array = array(
        "firstelement",
        "secondelement",
        "lastelement",
    );  

    public function __construct() {
        $this->position = 0;
    }

    function rewind() {
        var_dump(__METHOD__);
        $this->position = 0;
    }

    function current() {
        var_dump(__METHOD__);
        return $this->array[$this->position];
    }

    function key() {
        var_dump(__METHOD__);
        return $this->position;
    }

    function next() {
        var_dump(__METHOD__);
        ++$this->position;
    }

    function valid() {
        var_dump(__METHOD__);
        return isset($this->array[$this->position]);
    }
}

$it = new myIterator;

foreach($it as $key => $value) {
    var_dump($key, $value);
    echo "\n";
}
?>
```

以上例程的输出类似于：

    string(18) "myIterator::rewind"
    string(17) "myIterator::valid"
    string(19) "myIterator::current"
    string(15) "myIterator::key"
    int(0)
    string(12) "firstelement"

    string(16) "myIterator::next"
    string(17) "myIterator::valid"
    string(19) "myIterator::current"
    string(15) "myIterator::key"
    int(1)
    string(13) "secondelement"

    string(16) "myIterator::next"
    string(17) "myIterator::valid"
    string(19) "myIterator::current"
    string(15) "myIterator::key"
    int(2)
    string(11) "lastelement"

    string(16) "myIterator::next"
    string(17) "myIterator::valid"

简介
----

创建外部迭代器的接口。

接口摘要
--------

**IteratorAggregate**

<span class="ooclass"> class **IteratorAggregate** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Traversable**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Traversable</span>
<span class="methodname">getIterator</span> ( <span
class="methodparam">void</span> )

}

**示例 \#1 基本用法**

``` php
<?php
class myData implements IteratorAggregate {
    public $property1 = "Public property one";
    public $property2 = "Public property two";
    public $property3 = "Public property three";

    public function __construct() {
        $this->property4 = "last property";
    }

    public function getIterator() {
        return new ArrayIterator($this);
    }
}

$obj = new myData;

foreach($obj as $key => $value) {
    var_dump($key, $value);
    echo "\n";
}
?>
```

以上例程的输出类似于：

    string(9) "property1"
    string(19) "Public property one"

    string(9) "property2"
    string(19) "Public property two"

    string(9) "property3"
    string(21) "Public property three"

    string(9) "property4"
    string(13) "last property"

简介
----

提供像访问数组一样访问对象的能力的接口。

接口摘要
--------

**ArrayAccess**

<span class="ooclass"> class **ArrayAccess** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">boolean</span> <span
class="methodname">offsetExists</span> ( <span class="methodparam"><span
class="type">mixed</span> `$offset`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">offsetGet</span> ( <span class="methodparam"><span
class="type">mixed</span> `$offset`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">offsetSet</span> ( <span class="methodparam"><span
class="type">mixed</span> `$offset`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">offsetUnset</span> ( <span class="methodparam"><span
class="type">mixed</span> `$offset`</span> )

}

**示例 \#1 Basic usage**

``` php
<?php
class obj implements arrayaccess {
    private $container = array();
    public function __construct() {
        $this->container = array(
            "one"   => 1,
            "two"   => 2,
            "three" => 3,
        );
    }
    public function offsetSet($offset, $value) {
        if (is_null($offset)) {
            $this->container[] = $value;
        } else {
            $this->container[$offset] = $value;
        }
    }
    public function offsetExists($offset) {
        return isset($this->container[$offset]);
    }
    public function offsetUnset($offset) {
        unset($this->container[$offset]);
    }
    public function offsetGet($offset) {
        return isset($this->container[$offset]) ? $this->container[$offset] : null;
    }
}

$obj = new obj;

var_dump(isset($obj["two"]));
var_dump($obj["two"]);
unset($obj["two"]);
var_dump(isset($obj["two"]));
$obj["two"] = "A value";
var_dump($obj["two"]);
$obj[] = 'Append 1';
$obj[] = 'Append 2';
$obj[] = 'Append 3';
print_r($obj);
?>
```

以上例程的输出类似于：

    bool(true)
    int(2)
    bool(false)
    string(7) "A value"
    obj Object
    (
        [container:obj:private] => Array
            (
                [one] => 1
                [three] => 3
                [two] => A value
                [0] => Append 1
                [1] => Append 2
                [2] => Append 3
            )

    )

简介
----

自定义序列化的接口。

实现此接口的类将不再支持
<a href="/language/oop5/magic.html#language.oop5.magic.sleep" class="link">__sleep()</a>
和
<a href="/language/oop5/magic.html#language.oop5.magic.sleep" class="link">__wakeup()</a>。不论何时，只要有实例需要被序列化，serialize
方法都将被调用。它将不会调用 \_\_destruct()
或有其他影响，除非程序化地调用此方法。当数据被反序列化时，类将被感知并且调用合适的
unserialize() 方法而不是调用
\_\_construct()。如果需要执行标准的构造器，你应该在这个方法中进行处理。

接口摘要
--------

**Serializable**

<span class="ooclass"> class **Serializable** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

**示例 \#1 Basic usage**

``` php
<?php
class obj implements Serializable {
    private $data;
    public function __construct() {
        $this->data = "My private data";
    }
    public function serialize() {
        return serialize($this->data);
    }
    public function unserialize($data) {
        $this->data = unserialize($data);
    }
    public function getData() {
        return $this->data;
    }
}

$obj = new obj;
$ser = serialize($obj);

$newobj = unserialize($ser);

var_dump($newobj->getData());
?>
```

以上例程的输出类似于：

    string(15) "My private data"

简介
----

用于代表 <a href="/functions/anonymous.html" class="link">匿名函数</a>
的类.

匿名函数（在 PHP 5.3
中被引入）会产生这个类型的对象。在过去，这个类被认为是一个实现细节，但现在可以依赖它做一些事情。自
PHP 5.4 起，这个类带有一些方法，允许在匿名函数创建后对其进行更多的控制。

除了此处列出的方法，还有一个 *\_\_invoke* 方法。这是为了与其他实现了
<a href="/language/oop5/magic.html#language.oop5.magic.invoke" class="link">__invoke()魔术方法</a>
的对象保持一致性，但调用匿名函数的过程与它无关。

类摘要
------

**Closure**

<span class="ooclass"> class **Closure** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Closure</span> <span
class="methodname">bind</span> ( <span class="methodparam"><span
class="type">Closure</span> `$closure`</span> , <span
class="methodparam"><span class="type">object</span> `$newthis`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$newscope` <span class="initializer"> = 'static'</span></span> \] )

<span class="modifier">public</span> <span class="type">Closure</span>
<span class="methodname">bindTo</span> ( <span class="methodparam"><span
class="type">object</span> `$newthis`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$newscope` <span
class="initializer"> = 'static'</span></span> \] )

}

简介
----

<span class="classname">Generator</span> 对象是从
<a href="/language/generators.html" class="link">generators</a>返回的.

**Caution**

<span class="classname">Generator</span> 对象不能通过
<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
实例化.

类摘要
------

**Generator**

<span class="ooclass"> class **Generator** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">next</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">send</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">throw</span> ( <span class="methodparam"><span
class="type">Exception</span> `$exception`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_wakeup</span> ( <span
class="methodparam">void</span> )

}
