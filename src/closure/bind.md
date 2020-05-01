Closure::bind
=============

复制一个闭包，绑定指定的$this对象和类作用域。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Closure</span> <span
class="methodname">Closure::bind</span> ( <span
class="methodparam"><span class="type">Closure</span> `$closure`</span>
, <span class="methodparam"><span class="type">object</span>
`$newthis`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$newscope` <span class="initializer"> =
'static'</span></span> \] )

这个方法是 <span class="methodname">Closure::bindTo</span>
的静态版本。查看它的文档获取更多信息。

### 参数

`closure`  
需要绑定的匿名函数。

`newthis`  
需要绑定到匿名函数的对象，或者 **`NULL`** 创建未绑定的闭包。

`newscope`  
想要绑定给闭包的类作用域，或者 'static'
表示不改变。如果传入一个对象，则使用这个对象的类型名。
类作用域用来决定在闭包中 $this 对象的 私有、保护方法 的可见性。 The
class scope to which associate the closure is to be associated, or
'static' to keep the current one. If an object is given, the type of the
object will be used instead. This determines the visibility of protected
and private methods of the bound object.

### 返回值

返回一个新的 <span class="classname">Closure</span> 对象
或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">Closure::bind</span> 实例**

``` php
<?php
class A {
    private static $sfoo = 1;
    private $ifoo = 2;
}
$cl1 = static function() {
    return A::$sfoo;
};
$cl2 = function() {
    return $this->ifoo;
};

$bcl1 = Closure::bind($cl1, null, 'A');
$bcl2 = Closure::bind($cl2, new A(), 'A');
echo $bcl1(), "\n";
echo $bcl2(), "\n";
?>
```

以上例程的输出类似于：

    1
    2

### 参见

-   <a href="/functions/anonymous.html" class="link">匿名函数</a>
-   <span class="methodname">Closure::bindTo</span>
