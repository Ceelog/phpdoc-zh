语法
----

在PHP 5.3.0 之后的版本中，你可以用 <span class="function">define</span>
函数，或 *const* 两种方法来定义一个常量。函数 <span
class="function">define</span> 允许将常量定义为一个表达式，而 *const*
关键字有一些限制，具体可参见下述章节。一个常量一旦被定义，就不能再改变或者取消定义。

使用 *const* 关键字定义常量时，PHP 5.6 之前只能包含标量数据（<span
class="type">boolean</span>，<span class="type">integer</span>，<span
class="type">float</span> 和 <span class="type">string</span>）。从 PHP
5.6 开始，可以将常量定义为一个表达式，也可以定义为一个 <span
class="type">array</span>。还可以定义 <span class="type">resource</span>
为常量，但应尽量避免，因为可能会造成不可预料的结果。

可以简单的通过指定其名字来取得常量的值，与变量不同，*不应该*在常量前面加上
*$* 符号。如果常量名是动态的，也可以用函数 <span
class="function">constant</span> 来获取常量的值。用 <span
class="function">get\_defined\_constants</span>
可以获得所有已定义的常量列表。

> **Note**: <span class="simpara">
> 常量和（全局）变量在不同的名字空间中。这意味着例如 **`TRUE`** 和
> `$TRUE` 是不同的。 </span>

如果使用了一个未定义的常量，PHP
假定想要的是该常量本身的名字，如同用字符串调用它一样（CONSTANT 对应
"CONSTANT"）。此方法已在 PHP 7.2.0 中被废弃，会抛出一个 **`E_WARNING`**
级错误。（之前版本会发出一个
<a href="/ref/errorfunc.html" class="link">E_NOTICE</a>
级的错误。）参见手册中为什么
<a href="/language/types/array.html#language.types.array.foo-bar" class="link">$foo[bar]</a>
是错误的（除非事先用 <span class="function">define</span> 将 *bar*
定义为一个常量）。这不适用于
<a href="/language/namespaces/rules.html" class="link">(完全)限定的常量</a>，如果未定义，将引发致命错误。如果仅是检查是否定义了某常量，请使用
<span class="function">defined</span> 函数。

常量和变量有如下不同：

-   <span class="simpara"> 常量前面没有美元符号（*$*）； </span>
-   <span class="simpara"> PHP 5.3 之前，常量只能用 <span
    class="function">define</span> 函数定义，而不能通过赋值语句；
    </span>
-   <span class="simpara">
    常量可以不用理会变量的作用域而在任何地方定义和访问； </span>
-   <span class="simpara"> 常量一旦定义就不能被重新定义或者取消定义；
    </span>
-   <span class="simpara"> 常量的值只能是标量值。从 PHP 5.6 开始可以用
    *const* 关键字来定义数组常量，从 PHP 7 开始也可以用 <span
    class="function">define</span>
    函数来定义。你可以在常量标量表达式中使用数组（例如 *const FOO =
    array(1,2,3)\[0\];*），但是要求最终的结果必须是一个允许的类型的值。
    </span>

**示例 \#1 定义常量**

``` php
<?php
define("CONSTANT", "Hello world.");
echo CONSTANT; // outputs "Hello world."
echo Constant; // 输出 "Constant" 并发出一个提示级别错误信息
?>
```

**示例 \#2 使用关键字 *const* 定义常量**

``` php
<?php
// 以下代码在 PHP 5.3.0 后可以正常工作
const CONSTANT = 'Hello World';

echo CONSTANT;

// PHP 5.6.0 后的写法
const ANOTHER_CONST = CONSTANT.'; Goodbye World';
echo ANOTHER_CONST;

const ANIMALS = array('dog', 'cat', 'bird');
echo ANIMALS[1]; // 将输出 "cat"

// PHP 7 中的写法
define('ANIMALS', array(
    'dog',
    'cat',
    'bird'
));
echo ANIMALS[1]; // 将输出 "cat"
?>

?>
```

> **Note**:
>
> 和使用 <span class="function">define</span> 来定义常量相反的是，使用
> *const*
> 关键字定义常量必须处于最顶端的作用区域，因为用此方法是在编译时定义的。这就意味着不能在函数内，循环内以及
> *if* 或 *try*/*catch* 语句之内用 *const* 来定义常量。

> **Note**:
>
> 使用 *const* 关键字定义的常量总是大小写敏感的，而使用 <span
> class="function">define</span> 函数定义的常量可能不区分大小写。

参见<a href="/language/oop5/constants.html" class="link">类常量</a>。
