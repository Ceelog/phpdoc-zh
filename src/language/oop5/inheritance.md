对象继承
--------

继承已为大家所熟知的一个程序设计特性，PHP
的对象模型也使用了继承。继承将会影响到类与类，对象与对象之间的关系。

比如，当扩展一个类，子类就会继承父类所有公有的和受保护的方法。除非子类覆盖了父类的方法，被继承的方法都会保留其原有功能。

继承对于功能的设计和抽象是非常有用的，而且对于类似的对象增加新功能就无须重新再写这些公用的功能。

> **Note**:
>
> 除非使用了自动加载，否则一个类必须在使用之前被定义。如果一个类扩展了另一个，则父类必须在子类之前被声明。此规则适用于类继承其它类与接口。

**示例 \#1 继承示例**

``` php
<?php

class foo
{
    public function printItem($string) 
    {
        echo 'Foo: ' . $string . PHP_EOL;
    }
    
    public function printPHP()
    {
        echo 'PHP is great.' . PHP_EOL;
    }
}

class bar extends foo
{
    public function printItem($string)
    {
        echo 'Bar: ' . $string . PHP_EOL;
    }
}

$foo = new foo();
$bar = new bar();
$foo->printItem('baz'); // Output: 'Foo: baz'
$foo->printPHP();       // Output: 'PHP is great' 
$bar->printItem('baz'); // Output: 'Bar: baz'
$bar->printPHP();       // Output: 'PHP is great'

?>
```
