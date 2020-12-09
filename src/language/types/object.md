Object 对象
-----------

### 对象初始化

要创建一个新的对象 <span class="type">object</span>，使用 *new*
语句实例化一个类：

``` php
<?php
class foo
{
    function do_foo()
    {
        echo "Doing foo."; 
    }
}

$bar = new foo;
$bar->do_foo();
?>
```

详细讨论参见手册中<a href="/language/oop5.html" class="link">类与对象</a>章节。

### 转换为对象

如果将一个对象转换成对象，它将不会有任何变化。如果其它任何类型的值被转换成对象，将会创建一个内置类
*stdClass* 的实例。如果该值为 **`null`**，则新的实例为空。 <span
class="type">array</span> 转换成 <span class="type">object</span>
将使键名成为属性名并具有相对应的值。注意：在这个例子里， 使用 PHP 7.2.0
之前的版本，数字键只能通过迭代访问。

``` php
<?php
$obj = (object) array('1' => 'foo');
var_dump(isset($obj->{'1'})); // PHP 7.2.0 后输出 'bool(true)'，之前版本会输出 'bool(false)' 
var_dump(key($obj)); // PHP 7.2.0 后输出 'string(1) "1"'，之前版本输出  'int(1)' 
?>
```

对于其他值，会包含进成员变量名 *scalar*。

``` php
<?php
$obj = (object) 'ciao';
echo $obj->scalar;  // outputs 'ciao'
?>
```
