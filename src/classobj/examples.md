范例
====

在这个例子中，我们首先定义了一个基类和该类的扩展。
这个基类描述了普通的蔬菜，关于它是否可食用及其颜色。 子类 `Spinach`
添加了烹饪的方法和另一个检查是否已烹饪的方法。

**示例 \#1 classes.inc**

``` php
<?php

// base class with member properties and methods
class Vegetable {

   var $edible;
   var $color;

   function __construct($edible, $color="green")
   {
       $this->edible = $edible;
       $this->color = $color;
   }

   function is_edible() 
   {
       return $this->edible;
   }

   function what_color() 
   {
       return $this->color;
   }
   
} // end of class Vegetable

// extends the base class
class Spinach extends Vegetable {

   var $cooked = false;

   function __construct()
   {
       parent::__construct(true, "green");
   }

   function cook_it() 
   {
       $this->cooked = true;
   }

   function is_cooked() 
   {
       return $this->cooked;
   }
   
} // end of class Spinach

?>
```

接下来我们从这些类中实例化了两个对象，并打印了他们的信息，包括了他们类的继承关系。
同时我们也定了一些实用函数，主要为了漂亮地打印出这些变量。

**示例 \#2 test\_script.php**

``` php
<pre>
<?php

include "classes.inc";

// 实用函数

function print_vars($obj) 
{
foreach (get_object_vars($obj) as $prop => $val) {
    echo "\t$prop = $val\n";
}
}

function print_methods($obj) 
{
$arr = get_class_methods(get_class($obj));
foreach ($arr as $method) {
    echo "\tfunction $method()\n";
}
}

function class_parentage($obj, $class) 
{
if (is_subclass_of($GLOBALS[$obj], $class)) {
    echo "Object $obj belongs to class " . get_class($GLOBALS[$obj]);
    echo " a subclass of $class\n";
} else {
    echo "Object $obj does not belong to a subclass of $class\n";
}
}

// 实例化 2 对象

$veggie = new Vegetable(true, "blue");
$leafy = new Spinach();

// 打印这些对象的信息
echo "veggie: CLASS " . get_class($veggie) . "\n";
echo "leafy: CLASS " . get_class($leafy);
echo ", PARENT " . get_parent_class($leafy) . "\n";

// 显示蔬菜的属性
echo "\nveggie: Properties\n";
print_vars($veggie);

// and leafy methods
echo "\nleafy: Methods\n";
print_methods($leafy);

echo "\nParentage:\n";
class_parentage("leafy", "Spinach");
class_parentage("leafy", "Vegetable");
?>
</pre>
```

一个重要的东西是注意在上面的例子中，对象 `$leafy` 是 <span
class="classname">Spinach</span> 的实例（<span
class="classname">Vegetable</span>
的子类），另外脚本的最后部分会输出以下信息：

       [...]
    Parentage:
    Object leafy does not belong to a subclass of Spinach
    Object leafy belongs to class spinach, a subclass of Vegetable
