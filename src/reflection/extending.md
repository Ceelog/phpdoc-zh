扩展
====

如果你想创建内建类的专门版本（比如说，在创建并导出高亮 HTML
时，以易于访问的成员变量来取代方法或使用实用的方法），
你可以继续并扩展它们。

**示例 \#1 扩展内置的类**

``` php
<?php
/**
 * My Reflection_Method class
 */
class My_Reflection_Method extends ReflectionMethod
{
    public $visibility = array();

    public function __construct($o, $m)
    {
        parent::__construct($o, $m);
        $this->visibility = Reflection::getModifierNames($this->getModifiers());
    }
}

/**
 * Demo class #1
 *
 */
class T {
    protected function x() {}
}

/**
 * Demo class #2
 *
 */
class U extends T {
    function x() {}
}

// 输出信息
var_dump(new My_Reflection_Method('U', 'x'));
?>
```

以上例程的输出类似于：

    object(My_Reflection_Method)#1 (3) {
      ["visibility"]=>
      array(1) {
        [0]=>
        string(6) "public"
      }
      ["name"]=>
      string(1) "x"
      ["class"]=>
      string(1) "U"
    }

**Caution**

如果你重写了构造函数，记住在写任何插入的代码之前要先调用父类的构造函数。
不这么做将会导致以下的结果： *Fatal error: Internal error: Failed to
retrieve the reflection object*
