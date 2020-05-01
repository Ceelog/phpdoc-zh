Closure::bindTo
===============

复制当前闭包对象，绑定指定的$this对象和类作用域。

### 说明

<span class="modifier">public</span> <span class="type">Closure</span>
<span class="methodname">Closure::bindTo</span> ( <span
class="methodparam"><span class="type">object</span> `$newthis`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$newscope` <span class="initializer"> = 'static'</span></span> \] )

创建并返回一个
<a href="/functions/anonymous.html" class="link">匿名函数</a>，
它与当前对象的函数体相同、绑定了同样变量，但可以绑定不同的对象，也可以绑定新的类作用域。

“绑定的对象”决定了函数体中的 *$this*
的取值，“类作用域”代表一个类型、决定在这个匿名函数中能够调用哪些 私有 和
保护 的方法。 也就是说，此时 $this 可以调用的方法，与 `newscope`
类的成员函数是相同的。

静态闭包不能有绑定的对象（ `newthis` 参数的值应该设为
**`NULL`**）不过仍然可以用 bubdTo 方法来改变它们的类作用域。

This function will ensure that for a non-static closure, having a bound
instance will imply being scoped and vice-versa. To this end, non-static
closures that are given a scope but a **`NULL`** instance are made
static and non-static non-scoped closures that are given a non-null
instance are scoped to an unspecified class.

> **Note**:
>
> 如果你只是想要复制一个匿名函数，可以用
> <a href="/language/oop5/cloning.html" class="link">cloning</a> 代替。

### 参数

`newthis`  
绑定给匿名函数的一个对象，或者 **`NULL`** 来取消绑定。

`newscope`  
关联到匿名函数的类作用域，或者 'static'
保持当前状态。如果是一个对象，则使用这个对象的类型为心得类作用域。
这会决定绑定的对象的 保护、私有成员 方法的可见性。

### 返回值

返回新创建的 <span class="classname">Closure</span> 对象
或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">Closure::bindTo</span> 实例**

``` php
<?php

class A {
    function __construct($val) {
        $this->val = $val;
    }
    function getClosure() {
        //returns closure bound to this object and scope
        return function() { return $this->val; };
    }
}

$ob1 = new A(1);
$ob2 = new A(2);

$cl = $ob1->getClosure();
echo $cl(), "\n";
$cl = $cl->bindTo($ob2);
echo $cl(), "\n";
?>
```

以上例程的输出类似于：

    1
    2

### 参见

-   <a href="/functions/anonymous.html" class="link">匿名函数</a>
-   <span class="methodname">Closure::bind</span>
