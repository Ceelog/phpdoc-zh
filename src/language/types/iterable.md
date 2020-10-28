Iterables
---------

<span class="type">Iterable</span> is a pseudo-type introduced in PHP
7.1. It accepts any <span class="type">array</span> or object
implementing the <span class="classname">Traversable</span> interface.
Both of these types are iterable using
<a href="/control-structures/foreach.html" class="link">foreach</a> and
can be used with **yield from** within a
<a href="/language/generators.html" class="link">generator</a>.

### Using Iterables

Iterable can be used as a parameter type to indicate that a function
requires a set of values, but does not care about the form of the value
set since it will be used with
<a href="/control-structures/foreach.html" class="link">foreach</a>. If
a value is not an array or instance of <span
class="classname">Traversable</span>, a <span
class="classname">TypeError</span> will be thrown.

**示例 \#1 Iterable parameter type example**

``` php
<?php

function foo(iterable $iterable) {
    foreach ($iterable as $value) {
        // ...
    } 
}

?>
```

Parameters declared as iterable may use **`NULL`** or an array as a
default value.

**示例 \#2 Iterable parameter default value example**

``` php
<?php

function foo(iterable $iterable = []) {
    // ...
}

?>
```

Iterable can also be used as a return type to indicate a function will
return an iterable value. If the returned value is not an array or
instance of <span class="classname">Traversable</span>, a <span
class="classname">TypeError</span> will be thrown.

**示例 \#3 Iterable return type example**

``` php
<?php

function bar(): iterable {
    return [1, 2, 3];
}

?>
```

Functions declaring iterable as a return type may also be
<a href="/language/generators.html" class="link">generators</a>.

**示例 \#4 Iterable generator return type example**

``` php
<?php

function gen(): iterable {
    yield 1;
    yield 2;
    yield 3;
}

?>
```

### Iterable Type Variance

Classes extending/implementing may broaden methods using <span
class="type">array</span> or <span class="classname">Traversable</span>
as parameter types to <span class="type">iterable</span> or narrow
return types from <span class="type">iterable</span> to <span
class="type">array</span> or <span class="classname">Traversable</span>.

**示例 \#5 Iterable type variance example**

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
