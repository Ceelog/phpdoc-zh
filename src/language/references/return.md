引用返回
--------

引用返回用在当想用函数找到引用应该被绑定在哪一个变量上面时。*不要*用返回引用来增加性能，引擎足够聪明来自己进行优化。仅在有合理的技术原因时才返回引用！要返回引用，使用此语法：

``` php
<?php
class foo {
    public $value = 42;

    public function &getValue() {
        return $this->value;
    }
}

$obj = new foo;
$myValue = &$obj->getValue(); // $myValue is a reference to $obj->value, which is 42.
$obj->value = 2;
echo $myValue;                // prints the new value of $obj->value, i.e. 2.
?>
```

本例中 `getValue`
函数所返回的对象的属性将被赋值，而不是拷贝，就和没有用引用语法一样。

> **Note**: <span class="simpara">
> 和参数传递不同，这里必须在两个地方都用 *&*
> 符号——指出返回的是一个引用，而不是通常的一个拷贝，同样也指出
> `$myValue` 是作为引用的绑定，而不是通常的赋值。 </span>

> **Note**: <span class="simpara"> 如果试图这样从函数返回引用：*return
> ($this-\>value);*，这将*不会*起作用，因为在试图返回一个*表达式*的结果而不是一个引用的变量。只能从函数返回引用变量——没别的方法。如果代码试图返回一个动态表达式或
> *new* 运算符的结果，自 PHP 4.4.0 和 PHP 5.1.0 起会发出一条
> **`E_NOTICE`** 错误。 </span>
