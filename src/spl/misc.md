各种类及接口
============

**目录**

-   [ArrayObject](/spl/misc.html#ArrayObject) — The ArrayObject class
    -   [ArrayObject::append](/spl/misc.html#ArrayObject::append) —
        追加新的值作为最后一个元素。
    -   [ArrayObject::asort](/spl/misc.html#ArrayObject::asort) — Sort
        the entries by value
    -   [ArrayObject::\_\_construct](/spl/misc.html#ArrayObject::__construct)
        — Construct a new array object
    -   [ArrayObject::count](/spl/misc.html#ArrayObject::count) — 统计
        ArrayObject 内 public 属性的数量
    -   [ArrayObject::exchangeArray](/spl/misc.html#ArrayObject::exchangeArray)
        — Exchange the array for another one
    -   [ArrayObject::getArrayCopy](/spl/misc.html#ArrayObject::getArrayCopy)
        — Creates a copy of the ArrayObject
    -   [ArrayObject::getFlags](/spl/misc.html#ArrayObject::getFlags) —
        Gets the behavior flags
    -   [ArrayObject::getIterator](/spl/misc.html#ArrayObject::getIterator)
        — Create a new iterator from an ArrayObject instance
    -   [ArrayObject::getIteratorClass](/spl/misc.html#ArrayObject::getIteratorClass)
        — Gets the iterator classname for the ArrayObject
    -   [ArrayObject::ksort](/spl/misc.html#ArrayObject::ksort) — Sort
        the entries by key
    -   [ArrayObject::natcasesort](/spl/misc.html#ArrayObject::natcasesort)
        — Sort an array using a case insensitive "natural order"
        algorithm
    -   [ArrayObject::natsort](/spl/misc.html#ArrayObject::natsort) —
        Sort entries using a "natural order" algorithm
    -   [ArrayObject::offsetExists](/spl/misc.html#ArrayObject::offsetExists)
        — Returns whether the requested index exists
    -   [ArrayObject::offsetGet](/spl/misc.html#ArrayObject::offsetGet)
        — Returns the value at the specified index
    -   [ArrayObject::offsetSet](/spl/misc.html#ArrayObject::offsetSet)
        — 为指定索引设定新的值
    -   [ArrayObject::offsetUnset](/spl/misc.html#ArrayObject::offsetUnset)
        — Unsets the value at the specified index
    -   [ArrayObject::serialize](/spl/misc.html#ArrayObject::serialize)
        — Serialize an ArrayObject
    -   [ArrayObject::setFlags](/spl/misc.html#ArrayObject::setFlags) —
        Sets the behavior flags
    -   [ArrayObject::setIteratorClass](/spl/misc.html#ArrayObject::setIteratorClass)
        — Sets the iterator classname for the ArrayObject
    -   [ArrayObject::uasort](/spl/misc.html#ArrayObject::uasort) — Sort
        the entries with a user-defined comparison function and maintain
        key association
    -   [ArrayObject::uksort](/spl/misc.html#ArrayObject::uksort) — Sort
        the entries by keys using a user-defined comparison function
    -   [ArrayObject::unserialize](/spl/misc.html#ArrayObject::unserialize)
        — Unserialize an ArrayObject
-   [SplObserver](/spl/misc.html#SplObserver) — The SplObserver
    interface
    -   [SplObserver::update](/spl/misc.html#SplObserver::update) —
        Receive update from subject
-   [SplSubject](/spl/misc.html#SplSubject) — The SplSubject interface
    -   [SplSubject::attach](/spl/misc.html#SplSubject::attach) — Attach
        an SplObserver
    -   [SplSubject::detach](/spl/misc.html#SplSubject::detach) — Detach
        an observer
    -   [SplSubject::notify](/spl/misc.html#SplSubject::notify) — Notify
        an observer

无法归入其它 SPL 分类的类和接口。

简介
----

This class allows objects to work as arrays.

类摘要
------

**ArrayObject**

<span class="ooclass"> class **ArrayObject** </span> <span
class="oointerface">implements <span
class="interfacename">IteratorAggregate</span> </span> <span
class="oointerface">, <span class="interfacename">ArrayAccess</span>
</span> <span class="oointerface">, <span
class="interfacename">Serializable</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`STD_PROP_LIST` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`ARRAY_AS_PROPS` <span class="initializer"> = 2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$input`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$iterator_class`<span class="initializer"> =
"ArrayIterator"</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">append</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">asort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">exchangeArray</span> ( <span
class="methodparam"><span class="type">mixed</span> `$input`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getArrayCopy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ArrayIterator</span> <span
class="methodname">getIterator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getIteratorClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ksort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">natcasesort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">natsort</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setIteratorClass</span> ( <span
class="methodparam"><span class="type">string</span>
`$iterator_class`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">uasort</span> ( <span class="methodparam"><span
class="type">callable</span> `$cmp_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">uksort</span> ( <span class="methodparam"><span
class="type">callable</span> `$cmp_function`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

}

预定义常量
----------

ArrayObject Flags
-----------------

**`ArrayObject::STD_PROP_LIST`**  
Properties of the object have their normal functionality when accessed
as list (var\_dump, foreach, etc.).

**`ArrayObject::ARRAY_AS_PROPS`**  
Entries can be accessed as properties (read and write).

更新日志
--------

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 5.3.0 | Implements <span class="interfacename">Serializable</span>. |

ArrayObject::append
===================

追加新的值作为最后一个元素。

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::append</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

追加新的值作为最后一个元素。

> **Note**:
>
> 当 <span class="classname">ArrayObject</span> 从 object
> 初始化时不能调用此方法。使用 <span
> class="methodname">ArrayObject::offsetSet</span> 代替。

### 参数

`value`  
将要被追加的值

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">ArrayObject::append</span> 例子**

``` php
<?php
$arrayobj = new ArrayObject(array('first','second','third'));
$arrayobj->append('fourth');
$arrayobj->append(array('five', 'six'));
var_dump($arrayobj);
?>
```

以上例程会输出：

    object(ArrayObject)#1 (5) {
      [0]=>
      string(5) "first"
      [1]=>
      string(6) "second"
      [2]=>
      string(5) "third"
      [3]=>
      string(6) "fourth"
      [4]=>
      array(2) {
        [0]=>
        string(4) "five"
        [1]=>
        string(3) "six"
      }
    }

### 参见

-   <span class="methodname">ArrayObject::offsetSet</span>

ArrayObject::asort
==================

Sort the entries by value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::asort</span> ( <span
class="methodparam">void</span> )

Sorts the entries such that the keys maintain their correlation with the
entries they are associated with. This is used mainly when sorting
associative arrays where the actual element order is significant.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::asort</span> example**

``` php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
$fruitArrayObject = new ArrayObject($fruits);
$fruitArrayObject->asort();

foreach ($fruitArrayObject as $key => $val) {
    echo "$key = $val\n";
}
?>
```

以上例程会输出：

    c = apple
    b = banana
    d = lemon
    a = orange

The fruits have been sorted in alphabetical order, and the key
associated with each entry has been maintained.

### 参见

-   <span class="methodname">ArrayObject::ksort</span>
-   <span class="methodname">ArrayObject::natsort</span>
-   <span class="methodname">ArrayObject::natcasesort</span>
-   <span class="methodname">ArrayObject::uasort</span>
-   <span class="methodname">ArrayObject::uksort</span>

ArrayObject::\_\_construct
==========================

Construct a new array object

### 说明

<span class="modifier">public</span> <span
class="methodname">ArrayObject::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$input`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$iterator_class`<span class="initializer"> =
"ArrayIterator"</span></span> \]\]\] )

This constructs a new array <span class="type">object</span>.

### 参数

`input`  
The `input` parameter accepts an <span class="type">array</span> or an
<span class="type">Object</span>.

`flags`  
Flags to control the behaviour of the <span
class="classname">ArrayObject</span> object. See <span
class="methodname">ArrayObject::setFlags</span>.

`iterator_class`  
Specify the class that will be used for iteration of the <span
class="classname">ArrayObject</span> object.

### 返回值

Returns an ArrayObject object on success.

### 错误／异常

Throws <span class="classname">InvalidArgumentException</span> when:

-   <span class="simpara"> `input` is not an array or object </span>
-   <span class="simpara"> `flags` is not an integer </span>
-   <span class="simpara"> `iterator_class` is not an object that
    implements <span class="classname">Iterator</span> </span>

### 范例

**示例 \#1 <span class="function">ArrayObject::\_\_construct</span>
example**

``` php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

var_dump($arrayobject);
?>
```

以上例程会输出：

    object(ArrayObject)#1 (3) {
      [1]=>
      string(3) "one"
      [2]=>
      string(3) "two"
      [3]=>
      string(5) "three"
    }

### 参见

-   <span class="methodname">ArrayObject::setflags</span>

ArrayObject::count
==================

统计 ArrayObject 内 public 属性的数量

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ArrayObject::count</span> ( <span
class="methodparam">void</span> )

获取 <span class="classname">ArrayObject</span> 的 public 属性数量

### 参数

此函数没有参数。

### 返回值

对象 <span class="classname">ArrayObject</span> 的 public 属性数量

> **Note**:
>
> 当对象 <span class="classname">ArrayObject</span>
> 是从数组构造而来时，所有属性都是 public 的。

### 范例

**示例 \#1 <span class="methodname">ArrayObject::count</span> 例子**

``` php
<?php
class Example {
    public $public = 'prop:public';
    private $prv   = 'prop:private';
    protected $prt = 'prop:protected';
}

$arrayobj = new ArrayObject(new Example());
var_dump($arrayobj->count());

$arrayobj = new ArrayObject(array('first','second','third'));
var_dump($arrayobj->count());
?>
```

以上例程会输出：

    int(1)
    int(3)

ArrayObject::exchangeArray
==========================

Exchange the array for another one

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ArrayObject::exchangeArray</span> ( <span
class="methodparam"><span class="type">mixed</span> `$input`</span> )

Exchange the current <span class="type">array</span> with another <span
class="type">array</span> or <span class="type">object</span>.

### 参数

`input`  
The new <span class="type">array</span> or <span
class="type">object</span> to exchange with the current array.

### 返回值

Returns the old <span class="type">array</span>.

### 范例

**示例 \#1 <span class="function">ArrayObject::exchangeArray</span>
example**

``` php
<?php
// Array of available fruits
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);
// Array of locations in Europe
$locations = array('Amsterdam', 'Paris', 'London');

$fruitsArrayObject = new ArrayObject($fruits);

// Now exchange fruits for locations
$old = $fruitsArrayObject->exchangeArray($locations);
print_r($old);
print_r($fruitsArrayObject);

?>
```

以上例程会输出：

    Array
    (
        [lemons] => 1
        [oranges] => 4
        [bananas] => 5
        [apples] => 10
    )
    ArrayObject Object
    (
        [0] => Amsterdam
        [1] => Paris
        [2] => London
    )

ArrayObject::getArrayCopy
=========================

Creates a copy of the ArrayObject

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">ArrayObject::getArrayCopy</span> ( <span
class="methodparam">void</span> )

Exports the <span class="classname">ArrayObject</span> to an array.

### 参数

此函数没有参数。

### 返回值

Returns a copy of the array. When the <span
class="classname">ArrayObject</span> refers to an object, an array of
the public properties of that object will be returned.

### 范例

**示例 \#1 <span class="function">ArrayObject::getArrayCopy</span>
example**

``` php
<?php
// Array of available fruits
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);
$fruitsArrayObject['pears'] = 4;

// create a copy of the array
$copy = $fruitsArrayObject->getArrayCopy();
print_r($copy);

?>
```

以上例程会输出：

    Array
    (
        [lemons] => 1
        [oranges] => 4
        [bananas] => 5
        [apples] => 10
        [pears] => 4
    )

ArrayObject::getFlags
=====================

Gets the behavior flags

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ArrayObject::getFlags</span> ( <span
class="methodparam">void</span> )

Gets the behavior flags of the <span
class="classname">ArrayObject</span>. See the
<a href="/spl/misc.html#ArrayObject::setFlags" class="link">ArrayObject::setFlags</a>
method for a list of the available flags.

### 参数

此函数没有参数。

### 返回值

Returns the behavior flags of the ArrayObject.

### 范例

**示例 \#1 <span class="function">ArrayObject::getFlags</span> example**

``` php
<?php
// Array of available fruits
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Get the current flags
$flags = $fruitsArrayObject->getFlags();
var_dump($flags);

// Set new flags
$fruitsArrayObject->setFlags(ArrayObject::ARRAY_AS_PROPS);

// Get the new flags
$flags = $fruitsArrayObject->getFlags();
var_dump($flags);
?>
```

以上例程会输出：

    int(0)
    int(2)

### 参见

-   <span class="methodname">ArrayObject::setFlags</span>

ArrayObject::getIterator
========================

Create a new iterator from an ArrayObject instance

### 说明

<span class="modifier">public</span> <span
class="type">ArrayIterator</span> <span
class="methodname">ArrayObject::getIterator</span> ( <span
class="methodparam">void</span> )

Create a new iterator from an <span class="classname">ArrayObject</span>
instance.

### 参数

此函数没有参数。

### 返回值

An iterator from an <span class="classname">ArrayObject</span>.

### 范例

**示例 \#1 <span class="function">ArrayObject::getIterator</span>
example**

``` php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

$iterator = $arrayobject->getIterator();

while($iterator->valid()) {
    echo $iterator->key() . ' => ' . $iterator->current() . "\n";

    $iterator->next();
}
?>
```

以上例程会输出：

    1 => one
    2 => two
    3 => three

ArrayObject::getIteratorClass
=============================

Gets the iterator classname for the ArrayObject

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ArrayObject::getIteratorClass</span> ( <span
class="methodparam">void</span> )

Gets the class name of the array iterator that is used by
<a href="/spl/misc.html#ArrayObject::getIterator" class="link">ArrayObject::getIterator()</a>.

### 参数

此函数没有参数。

### 返回值

Returns the iterator class name that is used to iterate over this
object.

### 范例

**示例 \#1 <span class="function">ArrayObject::getIteratorClass</span>
example**

``` php
<?php
// Custom ArrayIterator (inherits from ArrayIterator)
class MyArrayIterator extends ArrayIterator {
    // custom implementation
}

// Array of available fruits
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Get the current class name
$className = $fruitsArrayObject->getIteratorClass();
var_dump($className);

// Set new classname
$fruitsArrayObject->setIteratorClass('MyArrayIterator');

// Get the new iterator classname
$className = $fruitsArrayObject->getIteratorClass();
var_dump($className);
?>
```

以上例程会输出：

    string(13) "ArrayIterator"
    string(15) "MyArrayIterator"

### 参见

-   The
    <a href="/spl/misc.html#ArrayObject::setIteratorClass" class="link">ArrayObject::setIteratorClass</a>
    method

ArrayObject::ksort
==================

Sort the entries by key

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::ksort</span> ( <span
class="methodparam">void</span> )

Sorts the entries by key, maintaining key to entry correlations. This is
useful mainly for associative arrays.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::ksort</span> example**

``` php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
$fruitArrayObject = new ArrayObject($fruits);
$fruitArrayObject->ksort();

foreach ($fruitArrayObject as $key => $val) {
    echo "$key = $val\n";
}
 ?>
```

以上例程会输出：

    a = orange
    b = banana
    c = apple
    d = lemon

### 参见

-   <span class="methodname">ArrayObject::asort</span>
-   <span class="methodname">ArrayObject::natsort</span>
-   <span class="methodname">ArrayObject::natcasesort</span>
-   <span class="methodname">ArrayObject::uasort</span>
-   <span class="methodname">ArrayObject::uksort</span>

ArrayObject::natcasesort
========================

Sort an array using a case insensitive "natural order" algorithm

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::natcasesort</span> ( <span
class="methodparam">void</span> )

This method is a case insensitive version of
<a href="/spl/misc.html#ArrayObject::natsort" class="link">ArrayObject::natsort</a>.

This method implements a sort algorithm that orders alphanumeric strings
in the way a human being would while maintaining key/value associations.
This is described as a "natural ordering".

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::natcasesort</span>
example**

``` php
<?php
$array = array('IMG0.png', 'img12.png', 'img10.png', 'img2.png', 'img1.png', 'IMG3.png');

$arr1 = new ArrayObject($array);
$arr2 = clone $arr1;

$arr1->asort();
echo "Standard sorting\n";
print_r($arr1);

$arr2->natcasesort();
echo "\nNatural order sorting (case-insensitive)\n";
print_r($arr2);
?>
```

以上例程会输出：

    Standard sorting
    ArrayObject Object
    (
        [0] => IMG0.png
        [5] => IMG3.png
        [4] => img1.png
        [2] => img10.png
        [1] => img12.png
        [3] => img2.png
    )

    Natural order sorting (case-insensitive)
    ArrayObject Object
    (
        [0] => IMG0.png
        [4] => img1.png
        [3] => img2.png
        [5] => IMG3.png
        [2] => img10.png
        [1] => img12.png
    )

For more information see: Martin Pool's
<a href="http://sourcefrog.net/projects/natsort/" class="link external">» Natural Order String Comparison</a>
page.

### 参见

-   <span class="methodname">ArrayObject::asort</span>
-   <span class="methodname">ArrayObject::ksort</span>
-   <span class="methodname">ArrayObject::natsort</span>
-   <span class="methodname">ArrayObject::uasort</span>
-   <span class="methodname">ArrayObject::uksort</span>

ArrayObject::natsort
====================

Sort entries using a "natural order" algorithm

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::natsort</span> ( <span
class="methodparam">void</span> )

This method implements a sort algorithm that orders alphanumeric strings
in the way a human being would while maintaining key/value associations.
This is described as a "natural ordering". An example of the difference
between this algorithm and the regular computer string sorting
algorithms (used in
<a href="/spl/misc.html#ArrayObject::asort" class="link">ArrayObject::asort</a>)
method can be seen in the example below.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::natsort</span> example**

``` php
<?php
$array = array("img12.png", "img10.png", "img2.png", "img1.png");

$arr1 = new ArrayObject($array);
$arr2 = clone $arr1;

$arr1->asort();
echo "Standard sorting\n";
print_r($arr1);

$arr2->natsort();
echo "\nNatural order sorting\n";
print_r($arr2);
?>
```

以上例程会输出：

    Standard sorting
    ArrayObject Object
    (
        [3] => img1.png
        [1] => img10.png
        [0] => img12.png
        [2] => img2.png
    )

    Natural order sorting
    ArrayObject Object
    (
        [3] => img1.png
        [2] => img2.png
        [1] => img10.png
        [0] => img12.png
    )

For more information see: Martin Pool's
<a href="http://sourcefrog.net/projects/natsort/" class="link external">» Natural Order String Comparison</a>
page.

### 参见

-   <span class="methodname">ArrayObject::asort</span>
-   <span class="methodname">ArrayObject::ksort</span>
-   <span class="methodname">ArrayObject::natcasesort</span>
-   <span class="methodname">ArrayObject::uasort</span>
-   <span class="methodname">ArrayObject::uksort</span>

ArrayObject::offsetExists
=========================

Returns whether the requested index exists

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">ArrayObject::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

### 参数

`index`  
The index being checked.

### 返回值

**`TRUE`** if the requested index exists, otherwise **`FALSE`**

### 范例

**示例 \#1 <span class="methodname">ArrayObject::offsetExists</span>
example**

``` php
<?php
$arrayobj = new ArrayObject(array('zero', 'one', 'example'=>'e.g.'));
var_dump($arrayobj->offsetExists(1));
var_dump($arrayobj->offsetExists('example'));
var_dump($arrayobj->offsetExists('notfound'));
?>
```

以上例程会输出：

    bool(true)
    bool(true)
    bool(false)

ArrayObject::offsetGet
======================

Returns the value at the specified index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">ArrayObject::offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

### 参数

`index`  
The index with the value.

### 返回值

The value at the specified index or **`NULL`**.

### 错误／异常

Produces an **`E_NOTICE`** error message when the specified index does
not exist.

### 范例

**示例 \#1 <span class="methodname">ArrayObject::offsetGet</span>
example**

``` php
<?php
$arrayobj = new ArrayObject(array('zero', 7, 'example'=>'e.g.'));
var_dump($arrayobj->offsetGet(1));
var_dump($arrayobj->offsetGet('example'));
var_dump($arrayobj->offsetExists('notfound'));
?>
```

以上例程会输出：

    int(7)
    string(4) "e.g."
    bool(false)

ArrayObject::offsetSet
======================

为指定索引设定新的值

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$newval`</span> )

设置指定的索引为新的值

### 参数

`index`  
将要被设置的索引

`newval`  
参数 `index` 所对应的新值。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">ArrayObject::offsetSet</span> 例子**

``` php
<?php
class Example {
    public $property = 'prop:public';
}
$arrayobj = new ArrayObject(new Example());
$arrayobj->offsetSet(4, 'four');
$arrayobj->offsetSet('group', array('g1', 'g2'));
var_dump($arrayobj);

$arrayobj = new ArrayObject(array('zero','one'));
$arrayobj->offsetSet(null, 'last');
var_dump($arrayobj);
?>
```

以上例程会输出：

    object(ArrayObject)#1 (3) {
      ["property"]=>
      string(11) "prop:public"
      [4]=>
      string(4) "four"
      ["group"]=>
      array(2) {
        [0]=>
        string(2) "g1"
        [1]=>
        string(2) "g2"
      }
    }
    object(ArrayObject)#3 (3) {
      [0]=>
      string(4) "zero"
      [1]=>
      string(3) "one"
      [2]=>
      string(4) "last"
    }

### 参见

-   <span class="methodname">ArrayObject::append</span>

ArrayObject::offsetUnset
========================

Unsets the value at the specified index

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::offsetUnset</span> ( <span
class="methodparam"><span class="type">mixed</span> `$index`</span> )

Unsets the value at the specified index.

### 参数

`index`  
The index being unset.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">ArrayObject::offsetUnset</span>
example**

``` php
<?php
$arrayobj = new ArrayObject(array(0=>'zero',2=>'two'));
$arrayobj->offsetUnset(2);
var_dump($arrayobj);
?>
```

以上例程会输出：

    object(ArrayObject)#1 (1) {
      [0]=>
      string(4) "zero"
    }

ArrayObject::serialize
======================

Serialize an ArrayObject

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">ArrayObject::serialize</span> ( <span
class="methodparam">void</span> )

Serializes an <span class="classname">ArrayObject</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

The serialized representation of the <span
class="classname">ArrayObject</span>.

### 范例

**示例 \#1 <span class="methodname">ArrayObject::serialize</span>
example**

``` php
<?php
$o = new ArrayObject();

$s1 = serialize($o);
$s2 = $o->serialize();

var_dump($s1);
var_dump($s2);
?>
```

以上例程会输出：

    string(45) "C:11:"ArrayObject":21:{x:i:0;a:0:{};m:a:0:{}}"
    string(21) "x:i:0;a:0:{};m:a:0:{}"

### 参见

-   <span class="methodname">ArrayObject::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

ArrayObject::setFlags
=====================

Sets the behavior flags

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::setFlags</span> ( <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

Set the flags that change the behavior of the ArrayObject.

### 参数

`flags`  
The new ArrayObject behavior. It takes on either a bitmask, or named
constants. Using named constants is strongly encouraged to ensure
compatibility for future versions.

The available behavior flags are listed below. The actual meanings of
these flags are described in the
<a href="/spl/misc.html#预定义常量" class="link">predefined constants</a>.

| value | constant                                                               |
|-------|------------------------------------------------------------------------|
| 1     | <a href="/spl/misc.html#" class="link">ArrayObject::STD_PROP_LIST</a>  |
| 2     | <a href="/spl/misc.html#" class="link">ArrayObject::ARRAY_AS_PROPS</a> |

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::setFlags</span> example**

``` php
<?php
// Array of available fruits
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Try to use array key as property
var_dump($fruitsArrayObject->lemons);
// Set the flag so that the array keys can be used as properties of the ArrayObject
$fruitsArrayObject->setFlags(ArrayObject::ARRAY_AS_PROPS);
// Try it again
var_dump($fruitsArrayObject->lemons);
?>
```

以上例程会输出：

    NULL
    int(1)

ArrayObject::setIteratorClass
=============================

Sets the iterator classname for the ArrayObject

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::setIteratorClass</span> ( <span
class="methodparam"><span class="type">string</span>
`$iterator_class`</span> )

Sets the classname of the array iterator that is used by
<a href="/spl/misc.html#ArrayObject::getIterator" class="link">ArrayObject::getIterator()</a>.

### 参数

`iterator_class`  
The classname of the array iterator to use when iterating over this
object.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::setIteratorClass</span>
example**

``` php
<?php
// Custom ArrayIterator (inherits from ArrayIterator)
class MyArrayIterator extends ArrayIterator {
    // custom implementation
}

// Array of available fruits
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Set the iterator classname to the newly
$fruitsArrayObject->setIteratorClass('MyArrayIterator');
print_r($fruitsArrayObject->getIterator());

?>
```

以上例程会输出：

    MyArrayIterator Object
    (
        [lemons] => 1
        [oranges] => 4
        [bananas] => 5
        [apples] => 10
    )

ArrayObject::uasort
===================

Sort the entries with a user-defined comparison function and maintain
key association

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::uasort</span> ( <span
class="methodparam"><span class="type">callable</span>
`$cmp_function`</span> )

This function sorts the entries such that keys maintain their
correlation with the entry that they are associated with, using a
user-defined comparison function.

This is used mainly when sorting associative arrays where the actual
element order is significant.

### 参数

`cmp_function`  
Function `cmp_function` should accept two parameters which will be
filled by pairs of entries. The comparison function must return an
integer less than, equal to, or greater than zero if the first argument
is considered to be respectively less than, equal to, or greater than
the second.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::uasort</span> example**

``` php
<?php
// Comparison function
function cmp($a, $b) {
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

// Array to be sorted
$array = array('a' => 4, 'b' => 8, 'c' => -1, 'd' => -9, 'e' => 2, 'f' => 5, 'g' => 3, 'h' => -4);
$arrayObject = new ArrayObject($array);
print_r($arrayObject);

// Sort and print the resulting array
$arrayObject->uasort('cmp');
print_r($arrayObject);
?>
```

以上例程会输出：

    Array
    (
        [a] => 4
        [b] => 8
        [c] => -1
        [d] => -9
        [e] => 2
        [f] => 5
        [g] => 3
        [h] => -4
    )
    Array
    (
        [d] => -9
        [h] => -4
        [c] => -1
        [e] => 2
        [g] => 3
        [a] => 4
        [f] => 5
        [b] => 8
    )

### 参见

-   <span class="methodname">ArrayObject::asort</span>
-   <span class="methodname">ArrayObject::ksort</span>
-   <span class="methodname">ArrayObject::natsort</span>
-   <span class="methodname">ArrayObject::natcasesort</span>
-   <span class="methodname">ArrayObject::uksort</span>

ArrayObject::uksort
===================

Sort the entries by keys using a user-defined comparison function

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::uksort</span> ( <span
class="methodparam"><span class="type">callable</span>
`$cmp_function`</span> )

This function sorts the keys of the entries using a user-supplied
comparison function. The key to entry correlations will be maintained.

### 参数

`cmp_function`  
The callback comparison function.

Function `cmp_function` should accept two parameters which will be
filled by pairs of entry keys. The comparison function must return an
integer less than, equal to, or greater than zero if the first argument
is considered to be respectively less than, equal to, or greater than
the second.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ArrayObject::uksort</span> example**

``` php
<?php
function cmp($a, $b) {
    $a = preg_replace('@^(a|an|the) @', '', $a);
    $b = preg_replace('@^(a|an|the) @', '', $b);
    return strcasecmp($a, $b);
}

$array = array("John" => 1, "the Earth" => 2, "an apple" => 3, "a banana" => 4);
$arrayObject = new ArrayObject($array);
$arrayObject->uksort('cmp');

foreach ($arrayObject as $key => $value) {
    echo "$key: $value\n";
}
?>
```

以上例程会输出：

    an apple: 3
    a banana: 4
    the Earth: 2
    John: 1

### 参见

-   <span class="methodname">ArrayObject::asort</span>
-   <span class="methodname">ArrayObject::ksort</span>
-   <span class="methodname">ArrayObject::natsort</span>
-   <span class="methodname">ArrayObject::natcasesort</span>
-   <span class="methodname">ArrayObject::uasort</span>

ArrayObject::unserialize
========================

Unserialize an ArrayObject

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ArrayObject::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

Unserializes a serialized <span class="classname">ArrayObject</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`serialized`  
The serialized <span class="classname">ArrayObject</span>.

### 返回值

The unserialized <span class="classname">ArrayObject</span>.

### 参见

-   <span class="methodname">ArrayIterator::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

The <span class="classname">SplObserver</span> interface is used
alongside <span class="classname">SplSubject</span> to implement the
Observer Design Pattern.

接口摘要
--------

**SplObserver**

<span class="ooclass"> class **SplObserver** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">update</span> ( <span class="methodparam"><span
class="type">SplSubject</span> `$subject`</span> )

}

SplObserver::update
===================

Receive update from subject

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">SplObserver::update</span> ( <span
class="methodparam"><span class="type">SplSubject</span>
`$subject`</span> )

This method is called when any <span class="classname">SplSubject</span>
to which the observer is attached calls <span
class="methodname">SplSubject::notify</span>.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`subject`  
The <span class="classname">SplSubject</span> notifying the observer of
an update.

### 返回值

没有返回值。

简介
----

The <span class="classname">SplSubject</span> interface is used
alongside <span class="classname">SplObserver</span> to implement the
Observer Design Pattern.

接口摘要
--------

**SplSubject**

<span class="ooclass"> class **SplSubject** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">attach</span> ( <span class="methodparam"><span
class="type">SplObserver</span> `$observer`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">detach</span> ( <span class="methodparam"><span
class="type">SplObserver</span> `$observer`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">notify</span> ( <span class="methodparam">void</span>
)

}

SplSubject::attach
==================

Attach an SplObserver

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">SplSubject::attach</span> ( <span
class="methodparam"><span class="type">SplObserver</span>
`$observer`</span> )

Attaches an <span class="classname">SplObserver</span> so that it can be
notified of updates.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`observer`  
The <span class="classname">SplObserver</span> to attach.

### 返回值

没有返回值。

SplSubject::detach
==================

Detach an observer

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">SplSubject::detach</span> ( <span
class="methodparam"><span class="type">SplObserver</span>
`$observer`</span> )

Detaches an observer from the subject to no longer notify it of updates.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`observer`  
The <span class="classname">SplObserver</span> to detach.

### 返回值

没有返回值。

SplSubject::notify
==================

Notify an observer

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">SplSubject::notify</span> ( <span
class="methodparam">void</span> )

Notifies all attached observers.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。
