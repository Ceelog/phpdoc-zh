对象比较
--------

PHP 5 中的对象比较要比 PHP 4
中复杂，所期望的结果更符合一个面向对象语言。

当使用比较运算符（*==*）比较两个对象变量时，比较的原则是：如果两个对象的属性和属性值
都相等，而且两个对象是同一个类的实例，那么这两个对象变量相等。

而如果使用全等运算符（*===*），这两个对象变量一定要指向某个类的同一个实例（即同一个对象）。

通过下面的示例可以理解以上原则。

**示例 \#1 PHP 5 的对象比较**

``` php
<?php
function bool2str($bool)
{
    if ($bool === false) {
        return 'FALSE';
    } else {
        return 'TRUE';
    }
}

function compareObjects(&$o1, &$o2)
{
    echo 'o1 == o2 : ' . bool2str($o1 == $o2) . "\n";
    echo 'o1 != o2 : ' . bool2str($o1 != $o2) . "\n";
    echo 'o1 === o2 : ' . bool2str($o1 === $o2) . "\n";
    echo 'o1 !== o2 : ' . bool2str($o1 !== $o2) . "\n";
}

class Flag
{
    public $flag;

    function Flag($flag = true) {
        $this->flag = $flag;
    }
}

class OtherFlag
{
    public $flag;

    function OtherFlag($flag = true) {
        $this->flag = $flag;
    }
}

$o = new Flag();
$p = new Flag();
$q = $o;
$r = new OtherFlag();

echo "Two instances of the same class\n";
compareObjects($o, $p);

echo "\nTwo references to the same instance\n";
compareObjects($o, $q);

echo "\nInstances of two different classes\n";
compareObjects($o, $r);
?>
```

以上例程会输出：

    Two instances of the same class
    o1 == o2 : TRUE
    o1 != o2 : FALSE
    o1 === o2 : FALSE
    o1 !== o2 : TRUE

    Two references to the same instance
    o1 == o2 : TRUE
    o1 != o2 : FALSE
    o1 === o2 : TRUE
    o1 !== o2 : FALSE

    Instances of two different classes
    o1 == o2 : FALSE
    o1 != o2 : TRUE
    o1 === o2 : FALSE
    o1 !== o2 : TRUE

> **Note**:
>
> PHP 扩展中可以自行定义对象比较的原则。
