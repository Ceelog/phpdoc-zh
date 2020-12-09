可迭代对象
----------

<span class="type">Iterable</span>是 PHP 7.1
中引入的一个伪类型。它接受任何实现了 <span
class="classname">Traversable</span> 接口的 <span
class="type">array</span> 或对象。这些类型都能用
<a href="/control-structures/foreach.html" class="link">foreach</a>
迭代，并且可以与 **yield from** 在一个
<a href="/language/generators.html" class="link">generator</a> 中使用。

### 使用可迭代对象

可迭代对象可以用作参数类型，表示函数需要一组值，
但是不会关心值集的形式，因为它将与
<a href="/control-structures/foreach.html" class="link">foreach</a>
一起使用。如果一个值不是数组或 <span
class="classname">Traversable</span> 的实例，则会抛出一个 <span
class="classname">TypeError</span>。

**示例 \#1 可迭代参数类型示例**

``` php
<?php

function foo(iterable $iterable) {
    foreach ($iterable as $value) {
        // ...
    } 
}

?>
```

声明为可迭代的参数可能会使用 **`null`** 或者一个数组作为默认值。

**示例 \#2 可迭代参数默认值示例**

``` php
<?php

function foo(iterable $iterable = []) {
    // ...
}

?>
```

可迭代对象还可以用作返回类型，表示函数将返回一个可迭代的值。
如果返回值不是数组或 <span class="classname">Traversable</span>
的实例，则会抛出一个 <span class="classname">TypeError</span>。

**示例 \#3 可迭代返回类型示例**

``` php
<?php

function bar(): iterable {
    return [1, 2, 3];
}

?>
```

将可迭代对象声明为返回类型的函数也可能是
<a href="/language/generators.html" class="link">generators</a>。

**示例 \#4 可迭代生成器返回类型的示例**

``` php
<?php

function gen(): iterable {
    yield 1;
    yield 2;
    yield 3;
}

?>
```

### 可迭代类型的类型差异

扩展/实现的类可以把使用 <span class="type">array</span> 或 <span
class="classname">Traversable</span> 作为参数类型扩展为 <span
class="type">iterable</span> ，或者把“狭窄”的返回类型从 <span
class="type">iterable</span> 扩展为 <span class="type">array</span> 或者
<span class="classname">Traversable</span>。

**示例 \#5 可迭代类型差异示例**

``` php
<?php

interface Example {
    public function method(array $array): iterable;
}

class ExampleImplementation implements Example {
    public function method(iterable $iterable): array {
        // Parameter broadened and return type narrowed.
    }
}

?>
```
