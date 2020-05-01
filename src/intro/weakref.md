Weak references provide a non-intrusive gateway to ephemeral objects.
Unlike normal (strong) references, weak references do not prevent the
garbage collector from freeing that object. For this reason, an object
may be destroyed even though a weak reference to that object still
exists. In such conditions, the weak reference seamlessly becomes
invalid.

**示例 \#1 <span class="classname">Weakref</span> usage example**

``` php
<?php
class MyClass {
    public function __destruct() {
        echo "Destroying object!\n";
    }
}

$o1 = new MyClass;

$r1 = new Weakref($o1);

if ($r1->valid()) {
    echo "Object still exists!\n";
    var_dump($r1->get());
} else {
    echo "Object is dead!\n";
}

unset($o1);

if ($r1->valid()) {
    echo "Object still exists!\n";
    var_dump($r1->get());
} else {
    echo "Object is dead!\n";
}
?>
```

以上例程会输出：

    Object still exists!
    object(MyClass)#1 (0) {
    }
    Destroying object!
    Object is dead!
