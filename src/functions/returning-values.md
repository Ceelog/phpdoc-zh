返回值
------

值通过使用可选的返回语句返回。可以返回包括数组和对象的任意类型。返回语句会立即中止函数的运行，并且将控制权交回调用该函数的代码行。更多信息见
<span class="function">return</span>。

> **Note**:
>
> 如果省略了 <span class="function">return</span>，则返回值为
> **`NULL`**。

### return 的使用

**示例 \#1 <span class="function">return</span> 的使用**

``` php
<?php
function square($num)
{
    return $num * $num;
}
echo square(4);   // outputs '16'.
?>
```

函数不能返回多个值，但可以通过返回一个数组来得到类似的效果。

**示例 \#2 返回一个数组以得到多个返回值**

``` php
<?php
function small_numbers()
{
    return array (0, 1, 2);
}
list ($zero, $one, $two) = small_numbers();
?>
```

从函数返回一个引用，必须在函数声明和指派返回值给一个变量时都使用引用运算符
&：

**示例 \#3 从函数返回一个引用**

``` php
<?php
function &returns_reference()
{
    return $someref;
}

$newref =& returns_reference();
?>
```

有关引用的更多信息, 请查看
<a href="/language/references.html" class="link">引用的解释</a>。
