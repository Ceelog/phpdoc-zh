Generator::send
===============

向生成器中传入一个值

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Generator::send</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

向生成器中传入一个值，并且当做
<a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>
表达式的结果，然后继续执行生成器。

如果当这个方法被调用时，生成器不在
<a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>
表达式，那么在传入值之前，它会先运行到第一个
<a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>
表达式。As such it is not necessary to "prime" PHP generators with a
<span class="methodname">Generator::next</span> call (like it is done in
Python).

### 参数

`value`  
传入生成器的值。这个值将会被作为生成器当前所在的
<a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>
的返回值

### 返回值

返回生成的值。

### 范例

**示例 \#1 用 <span class="methodname">Generator::send</span>
向生成器函数中传值**

``` php
<?php
function printer() {
    while (true) {
        $string = yield;
        echo $string;
    }
}

$printer = printer();
$printer->send('Hello world!');
?>
```

以上例程会输出：

    Hello world!
