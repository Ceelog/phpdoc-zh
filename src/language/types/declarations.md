类型声明
--------

类型声明可以用于函数的参数、返回值，PHP 7.4.0
起还可以用于类的属性，来显性的指定需要的类型，如果预期类型在调用时不匹配，则会抛出一个
<span class="classname">TypeError</span> 异常。

> **Note**:
>
> 当子类覆盖父方法时，子类的方法必须匹配父类的类型声明。如果父类没有定义返回类型，那么子方法可以指定自己的返回类型。

### 单一类型

| 类型                               | 说明                                                                                                                                                                  | 版本      |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| 类/接口 名称                       | 值必须为指定类和接口的实例化对象 <a href="/language/operators/type.html" class="link"><em>instanceof</em></a>                                                         |           |
| <span class="type">self</span>     | 值必定是所在方法的类的一个 <a href="/language/operators/type.html" class="link"><em>instanceof</em></a>。 只能在类的内部使用。                                        |           |
| <span class="type">array</span>    | 值必须为 <span class="type">array</span>。                                                                                                                            |           |
| <span class="type">callable</span> | 值必定是一个有效的 <span class="type">callable</span>。 不能用于类属性的类型声明。                                                                                    |           |
| <span class="type">bool</span>     | 值必须为一个布尔值。                                                                                                                                                  |           |
| <span class="type">float</span>    | 值必须为一个浮点数字。                                                                                                                                                |           |
| <span class="type">int</span>      | 值必须为一个整型数字。                                                                                                                                                |           |
| <span class="type">string</span>   | 值必须为一个 <span class="type">string</span>。                                                                                                                       |           |
| <span class="type">iterable</span> | 值必须为 <span class="type">array</span> 或 <a href="/language/operators/type.html" class="link"><em>instanceof</em></a> <span class="classname">Traversable</span>。 | PHP 7.1.0 |
| <span class="type">object</span>   | 值必须为<span class="type">object</span>。                                                                                                                            | PHP 7.2.0 |
| <span class="type">mixed</span>    | 值可以为任何类型。                                                                                                                                                    | PHP 8.0.0 |

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

以上例程在 PHP 8 中的输出：

    Warning: "boolean" will be interpreted as a class name. Did you mean "bool"? Write "\boolean" to suppress this warning in /in/9YrUX on line 2

    Fatal error: Uncaught TypeError: test(): Argument #1 ($param) must be of type boolean, bool given, called in - on line 3 and defined in -:2
    Stack trace:
    #0 -(3): test(true)
    #1 {main}
      thrown in - on line 2

#### 范例

**示例 \#1 在类中使用类型声明**

``` php
<?php
class C {}
class D extends C {}

// 它没有 extend C。
class E {}

function f(C $c) {
    echo get_class($c)."\n";
}

f(new C);
f(new D);
f(new E);
?>
```

以上例程在 PHP 8 中的输出：

    C
    D

    Fatal error: Uncaught TypeError: f(): Argument #1 ($c) must be of type C, E given, called in /in/gLonb on line 14 and defined in /in/gLonb:8
    Stack trace:
    #0 -(14): f(Object(E))
    #1 {main}
      thrown in - on line 8

**示例 \#2 在接口中使用类型声明**

``` php
<?php
interface I { public function f(); }
class C implements I { public function f() {} }

// 它没有 implement I。
class E {}

function f(I $i) {
    echo get_class($i)."\n";
}

f(new C);
f(new E);
?>
```

以上例程在 PHP 8 中的输出：

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

// 注意必须返回一个 float。
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

**示例 \#5 定义可空（Nullable）的参数类型**

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

**示例 \#6 定义可空（Nullable）的返回类型**

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

#### false 伪类型

通过联合类型支持字面类型（Literal Type）*false*，
出于历史原因，很多内部函数在失败时返回了 *false* 而不是 *null*。
这类函数的典型例子是 <span class="function">strpos</span>。

**Caution**

*false* 不能单独作为类型使用（包括可空 nullable 类型）。
因此，*false*、*false\|null*、 *?false* 都是不可以用的。

**Caution**

*true* 字面类型*不存在*。

#### 重复冗余的类型

为了能在联合类型声明中暴露简单的 bug，不需要加载 class
就可以在编译时让重复冗余的类型产生错误。 包含：

-   <span class="simpara"> 解析出来的类型只能出现一次。例如这样的类型
    *int\|string\|INT* 会导致错误。 </span>
-   <span class="simpara"> 使用了 <span class="type">bool</span>
    时就不能再附带使用 <span class="type">false</span>。 </span>
-   <span class="simpara"> 使用了 <span class="type">object</span>
    时就不能再附带使用 class 类型。 </span>
-   <span class="simpara"> 使用了 <span class="type">iterable</span>
    时，<span class="type">array</span>、 <span
    class="classname">Traversable</span> 都不能再附带使用。 </span>

> **Note**: <span class="simpara">
> 不过它不能确保类型最小化，因为要达到这样的效果，还要加载使用类型的
> class。 </span>

例如，假设 *A* 和 *B* 都是一个类的别名， 而 *A\|B*
仍然是有效的，哪怕它可以被简化为 *A* 或 *B*。 同样的，如果
`B extends A {}`，那 *A\|B* 仍然是有效的联合类型，尽管它可以被简化为
*A*。

``` php
<?php
function foo(): int|INT {} // 不允许
function foo(): bool|false {} // 不允许

use A as B;
function foo(): A|B {} // 不允许 ("use" 是名称解析的一部分)

class_alias('X', 'Y');
function foo(): X|Y {} // 允许 (运行时才能知道重复性)
?>
```

### 仅仅返回类型

#### void

*void* 是一个返回类型，用于标识函数没有返回值。
它不能是联合类型的一部分。 PHP 7.1.0 起可用。

#### static

它的值必须是一个 class 的
<a href="/language/operators/type.html" class="link"><em>instanceof</em></a>，该
class 是调用方法所在的同一个类。 PHP 8.0.0 起有效。

### 严格类型

默认如果可能，PHP 会强制转化不合适的类型为想要的标量类型。
比如，参数想要 <span class="type">string</span>，传入的是 <span
class="type">int</span>， 则会获取 <span class="type">string</span>
类型的变量。

可以按文件开启严格模式。
在严格模式下，只能接受完全匹配的类型，否则会抛出 <span
class="classname">TypeError</span>。 唯一的例外是 <span
class="type">int</span> 值也可以传入声明为 <span
class="type">float</span> 的类型。

**Warning**

通过内部函数调用函数时，不会受 *strict\_types* 声明影响。

要开启严格模式，使用
<a href="/control-structures/declare.html" class="link"><em>declare</em></a>
开启 *strict\_types*：

> **Note**:
>
> 文件开启严格类型后的*内部*调用函数将应用严格类型，
> 而不是在声明函数的文件内开启。
> 如果文件没有声明开启严格类型，而被调用的函数所在文件有严格类型声明，
> 那将遵循调用者的设置（开启类型强制转化）， 值也会强制转化。

> **Note**:
>
> 只有为标量类型的声明开启严格类型。

**示例 \#8 参数值的严格类型**

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

以上例程在 PHP 8 中的输出：

    int(3)

    Fatal error: Uncaught TypeError: sum(): Argument #1 ($a) must be of type int, float given, called in - on line 9 and defined in -:4
    Stack trace:
    #0 -(9): sum(1.5, 2.5)
    #1 {main}
      thrown in - on line 4

**示例 \#9 参数值的类型强制转化**

``` php
<?php
function sum(int $a, int $b) {
    return $a + $b;
}

var_dump(sum(1, 2));

// 以下会强制转化为整型，注意以下内容输出！
var_dump(sum(1.5, 2.5));
?>
```

以上例程会输出：

    int(3)
    int(3)

**示例 \#10 返回值的严格类型**

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

### 联合类型的内部隐式强制转化

没有开启 *strict\_types* 时，标量类型可能会限制内部隐式类型转化。
如果值的类型不是联合类型中的一部分，则目标类型会按以下顺序：

1.  <span class="simpara"> <span class="type">int</span> </span>
2.  <span class="simpara"> <span class="type">float</span> </span>
3.  <span class="simpara"> <span class="type">string</span> </span>
4.  <span class="simpara"> <span class="type">bool</span> </span>

如果类型出现在组合中，值可以按 PHP
现有的类型语义检测进行内部隐式强制转化，则会选择该类型。
否则会尝试下一个类型。

**Caution**

有一个例外：当值是字符串，而 int 与 float
同时在组合中，将按现有的“数字字符串”检测语义，识别首选的类型。
例如，*"42"* 会选择 <span class="type">int</span> 类型， 而 *"42.0"*
会选择 <span class="type">float</span> 类型。

> **Note**:
>
> 没有出现在上面列表中的类型则不是有效的内部隐式转化目标。
> 尤其是不会出现内部隐式转化 *null* 和 *false* 类型。

**示例 \#11 类型强制转换为联合类型的例子**

``` php
<?php
// int|string
42    --> 42          // 类型完全匹配
"42"  --> "42"        // 类型完全匹配
new ObjectWithToString --> "__toString() 的结果"
                      // object 不兼容 int，降级到 string
42.0  --> 42          // float 与 int 兼容
42.1  --> 42          // float 与 int 兼容
1e100 --> "1.0E+100"  // float 比 int 大太多了，降级到 string
INF   --> "INF"       // float 比 int 大太多了，降级到 string
true  --> 1           // bool 与 int 兼容
[]    --> TypeError   // array 不兼容 int 或 string

// int|float|bool
"45"    --> 45        // int 的数字字符串
"45.0"  --> 45.0      // float 的数字字符串

"45X"   --> true      // 不是数字字符串，降级到 bool
""      --> false     // 不是数字字符串，降级到 bool
"X"     --> true      // 不是数字字符串，降级到 bool
[]      --> TypeError // array 不兼容 int、float、bool
?>
```

### 其他

**示例 \#12 传引用参数的类型**

仅仅会在函数入口检查传引用的参数类型，而不是在函数返回时检查。
所以函数返回时，参数类型可能会发生变化。

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

以上例程在 PHP 8 中的输出：

    int(1)

    Fatal error: Uncaught TypeError: array_baz(): Argument #1 ($param) must be of type array, int given, called in - on line 9 and defined in -:2
    Stack trace:
    #0 -(9): array_baz(1)
    #1 {main}
      thrown in - on line 2

**示例 \#13 捕获 <span class="classname">TypeError</span>**

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

以上例程在 PHP 8 中的输出：

    int(3)
    Error: sum(): Argument #1 ($a) must be of type int, float given, called in - on line 10
