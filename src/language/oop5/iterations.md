遍历对象
--------

PHP 5 提供了一种定义对象的方法使其可以通过单元列表来遍历，例如用
<a href="/control-structures/foreach.html" class="link">foreach</a>
语句。默认情况下，所有<a href="/language/oop5/visibility.html" class="link">可见</a>属性都将被用于遍历。

**示例 \#1 简单的对象遍历**

``` php
<?php
class MyClass
{
    public $var1 = 'value 1';
    public $var2 = 'value 2';
    public $var3 = 'value 3';

    protected $protected = 'protected var';
    private   $private   = 'private var';

    function iterateVisible() {
       echo "MyClass::iterateVisible:\n";
       foreach($this as $key => $value) {
           print "$key => $value\n";
       }
    }
}

$class = new MyClass();

foreach($class as $key => $value) {
    print "$key => $value\n";
}
echo "\n";


$class->iterateVisible();

?>
```

以上例程会输出：

    var1 => value 1
    var2 => value 2
    var3 => value 3

    MyClass::iterateVisible:
    var1 => value 1
    var2 => value 2
    var3 => value 3
    protected => protected var
    private => private var

如上所示，<a href="/control-structures/foreach.html" class="link">foreach</a>
遍历了所有其能够访问的<a href="/language/oop5/visibility.html" class="link">可见</a>属性。

更进一步，可以实现 <span class="interfacename">Iterator</span>
<a href="/language/oop5/interfaces.html" class="link">接口</a>。可以让对象自行决定如何遍历以及每次遍历时那些值可用。

**示例 \#2 实现 Iterator 接口的对象遍历**

``` php
<?php
class MyIterator implements Iterator
{
    private $var = array();

    public function __construct($array)
    {
        if (is_array($array)) {
            $this->var = $array;
        }
    }

    public function rewind() {
        echo "rewinding\n";
        reset($this->var);
    }

    public function current() {
        $var = current($this->var);
        echo "current: $var\n";
        return $var;
    }

    public function key() {
        $var = key($this->var);
        echo "key: $var\n";
        return $var;
    }

    public function next() {
        $var = next($this->var);
        echo "next: $var\n";
        return $var;
    }

    public function valid() {
        $var = $this->current() !== false;
        echo "valid: {$var}\n";
        return $var;
    }
}

$values = array(1,2,3);
$it = new MyIterator($values);

foreach ($it as $a => $b) {
    print "$a: $b\n";
}
?>
```

以上例程会输出：

    rewinding
    current: 1
    valid: 1
    current: 1
    key: 0
    0: 1
    next: 2
    current: 2
    valid: 1
    current: 2
    key: 1
    1: 2
    next: 3
    current: 3
    valid: 1
    current: 3
    key: 2
    2: 3
    next:
    current:
    valid:

可以用 <span class="interfacename">IteratorAggregate</span>
<a href="/language/oop5/interfaces.html" class="link">接口</a>以替代实现所有的
<span class="interfacename">Iterator</span> 方法。<span
class="interfacename">IteratorAggregate</span> 只需要实现一个方法 <span
class="methodname">IteratorAggregate::getIterator</span>，其应返回一个实现了
<span class="interfacename">Iterator</span> 的类的实例。

**示例 \#3 通过实现 IteratorAggregate 来遍历对象**

``` php
<?php
class MyCollection implements IteratorAggregate
{
    private $items = array();
    private $count = 0;

    // Required definition of interface IteratorAggregate
    public function getIterator() {
        return new MyIterator($this->items);
    }

    public function add($value) {
        $this->items[$this->count++] = $value;
    }
}

$coll = new MyCollection();
$coll->add('value 1');
$coll->add('value 2');
$coll->add('value 3');

foreach ($coll as $key => $val) {
    echo "key/value: [$key -> $val]\n\n";
}
?>
```

以上例程会输出：

    rewinding
    current: value 1
    valid: 1
    current: value 1
    key: 0
    key/value: [0 -> value 1]

    next: value 2
    current: value 2
    valid: 1
    current: value 2
    key: 1
    key/value: [1 -> value 2]

    next: value 3
    current: value 3
    valid: 1
    current: value 3
    key: 2
    key/value: [2 -> value 3]

    next:
    current:
    valid:

> **Note**:
>
> 更多遍历的示例见
> <a href="/spl/iterators.html" class="link">SPL 扩展</a>。

> **Note**:
>
> PHP 5.5
> 及以后版本的用户也可参考<a href="/language/generators.html" class="link">生成器</a>，其提供了另一方法来定义
> Iterators。
