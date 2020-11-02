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

### 返回值类型声明

PHP 7 增加了对返回值类型声明的支持。 就如
<a href="/functions/arguments.html#functions.arguments.type-declaration" class="link">类型声明</a>
一样, 返回值类型声明将指定该函数返回值的类型。同样，返回值类型声明也与
<a href="/functions/arguments.html#functions.arguments.type-declaration.types" class="link">有效类型</a>
中可用的参数类型声明一致。

<a href="/functions/arguments.html#functions.arguments.type-declaration.strict" class="link">严格类型声明</a>
也会影响返回值类型声明。在默认情况下，如果返回值与返回值的类型不一致，则会被强制转换为返回值声明的类型，在强制转换失败的情况下才会抛出
<span class="classname">TypeError</span> 异常（例如：函数预期返回 <span
class="type">array</span> 实际返回 <span class="type">int</span>
的情况，无法强制转换）。而在严格类型声明模式中，返回值的类型必须与预期一致，否则将会直接抛出
<span class="classname">TypeError</span> 异常。

从 PHP 7.1.0 开始，不指定类型的返回语句会导致一个 **`E_COMPILE_ERROR`**
错误，除非指定了返回类型为 <span
class="type">void</span>，在此情况下，带有指定类型的返回会触发此错误。

从 7.1.0 开始，返回值可以通过在类型前添加问号 (*?*)
来标记为允许返回空值。这表示该函数将返回指定类型或 **`NULL`**。

> **Note**:
>
> 当覆盖一个父类方法时，子类方法的返回值类型声明必须与父类一致。如果父类方法没有定义返回类型，那么子类方法可以定义任意的返回值类型声明。

#### 范例

**示例 \#4 基础返回值类型声明**

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

**示例 \#5 严格模式下执行**

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

    Fatal error: Uncaught TypeError: Return value of sum() must be of the type integer, float returned in - on line 5 in -:5
    Stack trace:
    #0 -(9): sum(1, 2.5)
    #1 {main}
      thrown in - on line 5

**示例 \#6 返回一个对象**

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

**示例 \#7 指定可选返回空值 (PHP 7.1.0 起可用)**

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
