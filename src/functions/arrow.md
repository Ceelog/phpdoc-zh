Arrow Functions
---------------

Arrow functions were introduced in PHP 7.4 as a more concise syntax for
<a href="/functions/anonymous.html" class="link">anonymous functions</a>.

Both anonymous functions and arrow functions are implemented using the
<a href="/class/closure.html" class="link"><span class="classname">Closure</span></a>
class.

Arrow functions have the basic form `fn (argument_list) => expr`.

Arrow functions support the same features as
<a href="/functions/anonymous.html" class="link">anonymous functions</a>,
except that using variables from the parent scope is always automatic.

When a variable used in the expression is defined in the parent scope it
will be implicitly captured by-value. In the following example, the
functions `$fn1` and `$fn2` behave the same way.

**示例 \#1 Arrow functions capture variables by value automatically**

``` php
<?php

$y = 1;
 
$fn1 = fn($x) => $x + $y;
// equivalent to using $y by value:
$fn2 = function ($x) use ($y) {
    return $x + $y;
};

var_export($fn1(3));
?>
```

以上例程会输出：

    4

This also works if the arrow functions are nested:

**示例 \#2 Arrow functions capture variables by value automatically,
even when nested**

``` php
<?php

$z = 1;
$fn = fn($x) => fn($y) => $x * $y + $z;
// Outputs 51
var_export($fn(5)(10));
?>
```

Similarly to anonymous functions, the arrow function syntax allows
arbitrary function signatures, including parameter and return types,
default values, variadics, as well as by-reference passing and
returning. All of the following are valid examples of arrow functions:

**示例 \#3 Examples of arrow functions**

``` php
<?php

fn(array $x) => $x;
static fn(): int => $x;
fn($x = 42) => $x;
fn(&$x) => $x;
fn&($x) => $x;
fn($x, ...$rest) => $rest;

?>
```

Arrow functions use by-value variable binding. This is roughly
equivalent to performing a `use($x)` for every variable `$x` used inside
the arrow function. A by-value binding means that it is not possible to
modify any values from the outer scope.
<a href="/functions/anonymous.html" class="link">Anonymous functions</a>
can be used instead for by-ref bindings.

**示例 \#4 Values from the outer scope cannot be modified by arrow
functions**

``` php
<?php

$x = 1;
$fn = fn() => $x++; // Has no effect
$fn();
var_export($x);  // Outputs 1

?>
```

### 更新日志

| 版本  | 说明                              |
|-------|-----------------------------------|
| 7.4.0 | Arrow functions became available. |

### 注释

> **Note**: <span class="simpara"> It is possible to use <span
> class="function">func\_num\_args</span>, <span
> class="function">func\_get\_arg</span>, and <span
> class="function">func\_get\_args</span> from within an arrow function.
> </span>
