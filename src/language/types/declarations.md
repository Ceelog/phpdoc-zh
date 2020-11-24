类型声明
--------

类型声明可以用于函数的参数、返回值，PHP 7.4.0
起还可以用于类的属性，来显性的指定需要的类型，如果预期类型在调用时不匹配，则会抛出一个
<span class="classname">TypeError</span> 异常。

> **Note**:
>
> 当子类覆盖父方法时，子类的方法必须匹配父类的类型声明。如果父类没有定义返回类型，那么子方法可以指定自己的返回类型。

### 单一类型

| 类型                               | 说明                                                                                                                                                                               | 版本      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 类/接口 名称                       | 值必须为指定类和接口的实例化对象 <a href="/language/operators/type.html" class="link"><em>instanceof</em></a>                                                                      |           |
| <span class="type">self</span>     | The value must be an <a href="/language/operators/type.html" class="link"><em>instanceof</em></a> the same class as the one the method is defined on. Can only be used in classes. |           |
| <span class="type">array</span>    | 值必须为 <span class="type">array</span>。                                                                                                                                         |           |
| <span class="type">callable</span> | The value must be a valid <span class="type">callable</span>. Cannot be used as a class property type declaration.                                                                 |           |
| <span class="type">bool</span>     | 值必须为一个布尔值。                                                                                                                                                               |           |
| <span class="type">float</span>    | 值必须为一个浮点数字。                                                                                                                                                             |           |
| <span class="type">int</span>      | 值必须为一个整型数字。                                                                                                                                                             |           |
| <span class="type">string</span>   | 值必须为一个 <span class="type">string</span>。                                                                                                                                    |           |
| <span class="type">iterable</span> | 值必须为 <span class="type">array</span> 或 <a href="/language/operators/type.html" class="link"><em>instanceof</em></a> <span class="classname">Traversable</span>。              | PHP 7.1.0 |
| <span class="type">object</span>   | 值必须为<span class="type">object</span>。                                                                                                                                         | PHP 7.2.0 |
| <span class="type">mixed</span>    | 值可以为任何类型。                                                                                                                                                                 | PHP 8.0.0 |

**Warning**

不支持上述标量类型的别名。相反，它们被视为类或接口名。例如，使用
*boolean* 作为类型声明，将要求值是一个
<a href="/language/operators/type.html" class="link"><em>instanceof</em></a>
类或接口 *boolean*，而不能是类型 <span class="type">bool</span>。

``` php
<?php
    function test(boolean $param) {}
    test(true);
?>
```

Output of the above example in PHP 8:

    Warning: "boolean" will be interpreted as a class name. Did you mean "bool"? Write "\boolean" to suppress this warning in /in/9YrUX on line 2

    Fatal error: Uncaught TypeError: test(): Argument #1 ($param) must be of type boolean, bool given, called in - on line 3 and defined in -:2
    Stack trace:
    #0 -(3): test(true)
    #1 {main}
      thrown in - on line 2

#### 范例

**示例 \#1 类型声明在类中的使用**

``` php
<?php
class C {}
class D extends C {}

// This doesn't extend C.
class E {}

function f(C $c) {
    echo get_class($c)."\n";
}

f(new C);
f(new D);
f(new E);
?>
```

Output of the above example in PHP 8:

    C
    D

    Fatal error: Uncaught TypeError: f(): Argument #1 ($c) must be of type C, E given, called in /in/gLonb on line 14 and defined in /in/gLonb:8
    Stack trace:
    #0 -(14): f(Object(E))
    #1 {main}
      thrown in - on line 8

**示例 \#2 类型声明在接口中的使用**

``` php
<?php
interface I { public function f(); }
class C implements I { public function f() {} }

// This doesn't implement I.
class E {}

function f(I $i) {
    echo get_class($i)."\n";
}

f(new C);
f(new E);
?>
```

Output of the above example in PHP 8:

    C

    Fatal error: Uncaught TypeError: f(): Argument #1 ($i) must be of type I, E given, called in - on line 13 and defined in -:8
    Stack trace:
    #0 -(13): f(Object(E))
    #1 {main}
      thrown in - on line 8

**示例 \#3 返回类型声明**

``` php
<?php
function sum($a, $b): float {
    return $a + $b;
}

// Note that a float will be returned.
var_dump(sum(1, 2));
?>
```

以上例程会输出：

    float(3)

**示例 \#4 返回一个对象**

``` php
<?php
class C {}

function getC(): C {
    return new C;
}

var_dump(getC());
?>
```

以上例程会输出：

    object(C)#1 (0) {
    }

### 允许为空的（Nullable）类型

自 PHP 7.1.0 起，类型声明允许前置一个问号 (*?*)
用来声明这个值允许为指定类型，或者为 **`NULL`**。

**示例 \#5 允许为空的参数类型定义**

``` php
<?php
class C {}

function f(?C $c) {
    var_dump($c);
}

f(new C);
f(null);
?>
```

以上例程会输出：

    object(C)#1 (0) {
    }
    NULL

**示例 \#6 允许为空的返回类型定义**

``` php
<?php
function get_item(): ?string {
    if (isset($_GET['item'])) {
        return $_GET['item'];
    } else {
        return null;
    }
}
?>
```

> **Note**:
>
> 在 PHP 7.1.0 之前版本中，可以通过设置参数的默认值为 *null*
> 来实现允许为空的参数。不建议这样做，因为影响到类的继承调用。
>
> **示例 \#7 旧版本中实现允许为空参数的示例**
>
> ``` php
> <?php
> class C {}
>
> function f(C $c = null) {
>     var_dump($c);
> }
>
> f(new C);
> f(null);
> ?>
> ```
>
> 以上例程会输出：
>
>     object(C)#1 (0) {
>     }
>     NULL

### 联合类型

联合类型接受多个不同的类型做为参数。声明联合类型的语法为
*T1\|T2\|...*。联合类型自 PHP 8.0.0 起可用。

#### 允许为空的联合类型

*null* 类型允许在联合类型中使用，例如 *T1\|T2\|null*
代表接受一个空值为参数。已经存在的 *?T*
语法可以视为以下联合类型的一个简写 *T\|null*。

**Caution**

*null* 不能作为一个独立的类型使用。

#### false pseudo-type

The *false* literal type is supported as part of unions, and is included
as for historical reasons many internal functions return *false* instead
of *null* for failures. A classic example of such a function is <span
class="function">strpos</span>.

**Caution**

*false* cannot be used as a standalone type (including nullable
standalone type). As such, all of *false*, *false\|null* and *?false*
are not permitted.

**Caution**

The *true* literal type does *not* exist.

#### Duplicate and redundant types

To catch simple bugs in union type declarations, redundant types that
can be detected without performing class loading will result in a
compile-time error. This includes:

-   <span class="simpara"> Each name-resolved type may only occur once.
    Types such as *int\|string\|INT* result in an error. </span>
-   <span class="simpara"> If <span class="type">bool</span> is used,
    <span class="type">false</span> cannot be used additionally. </span>
-   <span class="simpara"> If <span class="type">object</span> is used,
    class types cannot be used additionally. </span>
-   <span class="simpara"> If <span class="type">iterable</span> is
    used, <span class="type">array</span> and <span
    class="classname">Traversable</span> cannot be used additionally.
    </span>

> **Note**: <span class="simpara"> This does not guarantee that the type
> is “minimal”, because doing so would require loading all used class
> types. </span>

For example, if *A* and *B* are class aliases, then *A\|B* remains a
legal union type, even though it could be reduced to either *A* or *B*.
Similarly, if class `B extends A {}`, then *A\|B* is also a legal union
type, even though it could be reduced to just *A*.

``` php
<?php
function foo(): int|INT {} // Disallowed
function foo(): bool|false {} // Disallowed

use A as B;
function foo(): A|B {} // Disallowed ("use" is part of name resolution)

class_alias('X', 'Y');
function foo(): X|Y {} // Allowed (redundancy is only known at runtime)
?>
```

### Return only types

#### void

*void* is a return type indicating the function does not return a value.
Therefore it cannot be part of a union type declaration. Available as of
PHP 7.1.0.

#### static

The value must be an
<a href="/language/operators/type.html" class="link"><em>instanceof</em></a>
the same class as the one the method is called in. Available as of PHP
8.0.0.

### Strict typing

By default, PHP will coerce values of the wrong type into the expected
scalar type declaration if possible. For example, a function that is
given an <span class="type">int</span> for a parameter that expects a
<span class="type">string</span> will get a variable of type <span
class="type">string</span>.

It is possible to enable strict mode on a per-file basis. In strict
mode, only a value corresponding exactly to the type declaration will be
accepted, otherwise a <span class="classname">TypeError</span> will be
thrown. The only exception to this rule is that an <span
class="type">int</span> value will pass a <span
class="type">float</span> type declaration.

**Warning**

Function calls from within internal functions will not be affected by
the *strict\_types* declaration.

To enable strict mode, the
<a href="/control-structures/declare.html" class="link"><em>declare</em></a>
statement is used with the *strict\_types* declaration:

> **Note**:
>
> Strict typing applies to function calls made from *within* the file
> with strict typing enabled, not to the functions declared within that
> file. If a file without strict typing enabled makes a call to a
> function that was defined in a file with strict typing, the caller's
> preference (coercive typing) will be respected, and the value will be
> coerced.

> **Note**:
>
> Strict typing is only defined for scalar type declarations.

**示例 \#8 Strict typing for arguments values**

``` php
<?php
declare(strict_types=1);

function sum(int $a, int $b) {
    return $a + $b;
}

var_dump(sum(1, 2));
var_dump(sum(1.5, 2.5));
?>
```

Output of the above example in PHP 8:

    int(3)

    Fatal error: Uncaught TypeError: sum(): Argument #1 ($a) must be of type int, float given, called in - on line 9 and defined in -:4
    Stack trace:
    #0 -(9): sum(1.5, 2.5)
    #1 {main}
      thrown in - on line 4

**示例 \#9 Coercive typing for argument values**

``` php
<?php
function sum(int $a, int $b) {
    return $a + $b;
}

var_dump(sum(1, 2));

// These will be coerced to integers: note the output below!
var_dump(sum(1.5, 2.5));
?>
```

以上例程会输出：

    int(3)
    int(3)

**示例 \#10 Strict typing for return values**

``` php
<?php
declare(strict_types=1);

function sum($a, $b): int {
    return $a + $b;
}

var_dump(sum(1, 2));
var_dump(sum(1, 2.5));
?>
```

以上例程会输出：

    int(3)

    Fatal error: Uncaught TypeError: sum(): Return value must be of type int, float returned in -:5
    Stack trace:
    #0 -(9): sum(1, 2.5)
    #1 {main}
      thrown in - on line 5

### Coercive typing with union types

When *strict\_types* is not enabled, scalar type declarations are
subject to limited implicit type coercions. If the exact type of the
value is not part of the union, then the target type is chosen in the
following order of preference:

1.  <span class="simpara"> <span class="type">int</span> </span>
2.  <span class="simpara"> <span class="type">float</span> </span>
3.  <span class="simpara"> <span class="type">string</span> </span>
4.  <span class="simpara"> <span class="type">bool</span> </span>

If the type both exists in the union, and the value can be coerced to
the type under PHPs existing type checking semantics, then the type is
chosen. Otherwise the next type is tried.

**Caution**

As an exception, if the value is a string and both int and float are
part of the union, the preferred type is determined by the existing
“numeric string” semantics. For example, for *"42"* <span
class="type">int</span> is chosen, while for *"42.0"* <span
class="type">float</span> is chosen.

> **Note**:
>
> Types that are not part of the above preference list are not eligible
> targets for implicit coercion. In particular no implicit coercions to
> the *null* and *false* types occur.

**示例 \#11 Example of types being coerced into a type part of the
union**

``` php
<?php
// int|string
42    --> 42          // exact type
"42"  --> "42"        // exact type
new ObjectWithToString --> "Result of __toString()"
                      // object never compatible with int, fall back to string
42.0  --> 42          // float compatible with int
42.1  --> 42          // float compatible with int
1e100 --> "1.0E+100"  // float too large for int type, fall back to string
INF   --> "INF"       // float too large for int type, fall back to string
true  --> 1           // bool compatible with int
[]    --> TypeError   // array not compatible with int or string

// int|float|bool
"45"    --> 45        // int numeric string
"45.0"  --> 45.0      // float numeric string

"45X"   --> true      // not numeric string, fall back to bool
""      --> false     // not numeric string, fall back to bool
"X"     --> true      // not numeric string, fall back to bool
[]      --> TypeError // array not compatible with int, float or bool
?>
```

### Misc

**示例 \#12 Typed pass-by-reference Parameters**

Declared types of reference parameters are checked on function entry,
but not when the function returns, so after the function had returned,
the argument's type may have changed.

``` php
<?php
function array_baz(array &$param)
{
    $param = 1;
}
$var = [];
array_baz($var);
var_dump($var);
array_baz($var);
?>
```

Output of the above example in PHP 8:

    int(1)

    Fatal error: Uncaught TypeError: array_baz(): Argument #1 ($param) must be of type array, int given, called in - on line 9 and defined in -:2
    Stack trace:
    #0 -(9): array_baz(1)
    #1 {main}
      thrown in - on line 2

**示例 \#13 Catching <span class="classname">TypeError</span>**

``` php
<?php
declare(strict_types=1);

function sum(int $a, int $b) {
    return $a + $b;
}

try {
    var_dump(sum(1, 2));
    var_dump(sum(1.5, 2.5));
} catch (TypeError $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

Output of the above example in PHP 8:

    int(3)
    Error: sum(): Argument #1 ($a) must be of type int, float given, called in - on line 10
