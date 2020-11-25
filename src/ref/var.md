boolval
=======

获取变量的布尔值

### 说明

<span class="type">boolean</span> <span
class="methodname">boolval</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

返回`var`变量的布尔值 .

### 参数

`var`  
标量类型会被转化成<span class="type">布尔</span>类型.

### 返回值

`var`变量的布尔值.

### 范例

**示例 \#1 <span class="function">boolval</span> examples**

``` php
<?php
echo '0:        '.(boolval(0) ? 'true' : 'false')."\n";
echo '42:       '.(boolval(42) ? 'true' : 'false')."\n";
echo '0.0:      '.(boolval(0.0) ? 'true' : 'false')."\n";
echo '4.2:      '.(boolval(4.2) ? 'true' : 'false')."\n";
echo '"":       '.(boolval("") ? 'true' : 'false')."\n";
echo '"string": '.(boolval("string") ? 'true' : 'false')."\n";
echo '"0":      '.(boolval("0") ? 'true' : 'false')."\n";
echo '"1":      '.(boolval("1") ? 'true' : 'false')."\n";
echo '[1, 2]:   '.(boolval([1, 2]) ? 'true' : 'false')."\n";
echo '[]:       '.(boolval([]) ? 'true' : 'false')."\n";
echo 'stdClass: '.(boolval(new stdClass) ? 'true' : 'false')."\n";
?>
```

以上例程会输出：

    0:        false
    42:       true
    0.0:      false
    4.2:      true
    "":       false
    "string": true
    "0":      false
    "1":      true
    [1, 2]:   true
    []:       false
    stdClass: true

### 参见

-   <span class="function">floatval</span>
-   <span class="function">intval</span>
-   <span class="function">strval</span>
-   <span class="function">settype</span>
-   <span class="function">is\_bool</span>
-   <a href="/language/types/type-juggling.html" class="link">Type juggling</a>

debug\_zval\_dump
=================

Dumps a string representation of an internal zend value to output

### 说明

<span class="type">void</span> <span
class="methodname">debug\_zval\_dump</span> ( <span
class="methodparam"><span class="type">mixed</span> `$variable`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$variables`</span> )

Dumps a string representation of an internal zend value to output.

### 参数

`variable`  
The variable to dump.

`variables`  
Further variables to dump.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">debug\_zval\_dump</span> example**

``` php
<?php
$var1 = 'Hello World';
$var2 = '';

$var2 =& $var1;

debug_zval_dump(&$var1);
?>
```

以上例程会输出：

    &string(11) "Hello World" refcount(3)

> **Note**: **Beware the *refcount***  
>
> The *refcount* value returned by this function is non-obvious in
> certain circumstances. For example, a developer might expect the above
> example to indicate a *refcount* of *2*. The third reference is
> created when actually calling <span
> class="function">debug\_zval\_dump</span>.
>
> This behavior is further compounded when a variable is not passed to
> <span class="function">debug\_zval\_dump</span> by reference. To
> illustrate, consider a slightly modified version of the above example:
>
> ``` php
> <?php
> $var1 = 'Hello World';
> $var2 = '';
>
> $var2 =& $var1;
>
> debug_zval_dump($var1); // not passed by reference, this time
> ?>
> ```
>
> 以上例程会输出：
>
>     string(11) "Hello World" refcount(1)
>
> Why *refcount(1)*? Because a copy of *$var1* is being made, when the
> function is called.
>
> This function becomes even *more* confusing when a variable with a
> *refcount* of *1* is passed (by copy/value):
>
> ``` php
> <?php
> $var1 = 'Hello World';
>
> debug_zval_dump($var1);
> ?>
> ```
>
> 以上例程会输出：
>
>     string(11) "Hello World" refcount(2)
>
> A *refcount* of *2*, here, is extremely non-obvious. Especially
> considering the above examples. So what's happening?
>
> When a variable has a single reference (as did *$var1* before it was
> used as an argument to <span
> class="function">debug\_zval\_dump</span>), PHP's engine optimizes the
> manner in which it is passed to a function. Internally, PHP treats
> *$var1* like a reference (in that the *refcount* is increased for the
> scope of this function), with the caveat that *if* the passed
> reference happens to be written to, a copy is made, but only at the
> moment of writing. This is known as "copy on write."
>
> So, if <span class="function">debug\_zval\_dump</span> happened to
> write to its sole parameter (and it doesn't), then a copy would be
> made. Until then, the parameter remains a reference, causing the
> *refcount* to be incremented to *2* for the scope of the function
> call.

### 参见

-   <span class="function">var\_dump</span>
-   <span class="function">debug\_backtrace</span>
-   <a href="/language/references.html" class="link">References Explained</a>
-   <a href="http://derickrethans.nl/php_references_article.php" class="link external">» References Explained (by Derick Rethans)</a>

doubleval
=========

<span class="function">floatval</span> 的别名

### 描述

此函数是 <span class="function">floatval</span> 的别名。

> **Note**:
>
> 此别名是函数改名之后的遗留问题。在 PHP 旧的版本中由于还没有 <span
> class="function">floatval</span> 函数，所以你可能需要用到这个 <span
> class="function">floatval</span> 的别名函数。

empty
=====

检查一个变量是否为空

### 说明

<span class="type">bool</span> <span class="methodname">empty</span> (
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
)

判断一个变量是否被认为是空的。当一个变量并不存在，或者它的值等同于**`FALSE`**，那么它会被认为不存在。如果变量不存在的话，<span
class="function">empty</span>并不会产生警告。

### 参数

`var`  
待检查的变量

> **Note**:
>
> 在 PHP 5.5 之前，<span class="function">empty</span>
> 仅支持变量；任何其他东西将会导致一个解析错误。换言之，下列代码不会生效：
> **empty(trim($name))**。 作为替代，应该使用**trim($name) == false**.

没有警告会产生，哪怕变量并不存在。 这意味着 <span
class="function">empty</span> 本质上与 **!isset($var) \|\| $var ==
false** 等价。

### 返回值

当`var`存在，并且是一个非空非零的值时返回 **`FALSE`** 否则返回
**`TRUE`**.

以下的东西被认为是空的：

-   *""* (空字符串)
-   *0* (作为整数的0)
-   *0.0* (作为浮点数的0)
-   *"0"* (作为字符串的0)
-   **`NULL`**
-   **`FALSE`**
-   *array()* (一个空数组)
-   *$var;* (一个声明了，但是没有值的变量)

### 更新日志

| 版本  | 说明                                                                   |
|-------|------------------------------------------------------------------------|
| 5.5.0 | <span class="function">empty</span> 现在支持表达式了，而不仅仅是变量。 |
| 5.4.0 | 检查非数字的字符串偏移量会返回 **`TRUE`**.                             |

### 范例

**示例 \#1 一个简单的 <span class="function">empty</span> 与 <span
class="function">isset</span> 的比较。**

``` php
<?php
$var = 0;

// Evaluates to true because $var is empty
if (empty($var)) {
    echo '$var is either 0, empty, or not set at all';
}

// Evaluates as true because $var is set
if (isset($var)) {
    echo '$var is set even though it is empty';
}
?>
```

**示例 \#2 在字符串偏移量上使用<span class="function">empty</span>**

PHP 5.4 修改了当传入的是字符串偏移量时， <span
class="function">empty</span> 的行为

``` php
<?php
$expected_array_got_string = 'somestring';
var_dump(empty($expected_array_got_string['some_key']));
var_dump(empty($expected_array_got_string[0]));
var_dump(empty($expected_array_got_string['0']));
var_dump(empty($expected_array_got_string[0.5]));
var_dump(empty($expected_array_got_string['0.5']));
var_dump(empty($expected_array_got_string['0 Mostel']));
?>
```

以上例程在 PHP 5.3 中的输出：

    bool(false)
    bool(false)
    bool(false)
    bool(false)
    bool(false)
    bool(false)

以上例程在 PHP 5.4 中的输出：

    bool(true)
    bool(false)
    bool(false)
    bool(false)
    bool(true)
    bool(true)

### 注释

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

> **Note**:
>
> 当对一个不可见的对象属性使用 <span class="function">empty</span> 时，
> <a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>
> 方法如果存在的话，它将会被调用。

### 参见

-   <span class="function">isset</span>
-   <a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>
-   <span class="function">unset</span>
-   <span class="function">array\_key\_exists</span>
-   <span class="function">count</span>
-   <span class="function">strlen</span>
-   <a href="/types/comparisons.html" class="link">The type comparison tables</a>

floatval
========

获取变量的浮点值

### 描述

<span class="type">float</span> <span class="methodname">floatval</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

返回变量 `var` 的 <span class="type">float</span> 数值。

`var` 可以是任何标量类型。你不能将 <span
class="function">floatval</span> 用于数组或对象。

``` php
<?php
$var = '122.34343The';
$float_value_of_var = floatval ($var);
print $float_value_of_var; // 打印出 122.34343
?>
```

参见 <span class="function">intval</span>、<span
class="function">strval</span>、<span class="function">settype</span> 和
<a href="/language/types/type-juggling.html" class="link">类型戏法</a>。

get\_defined\_vars
==================

返回由所有已定义变量所组成的数组

### 描述

<span class="type">array</span> <span
class="methodname">get\_defined\_vars</span> ( <span
class="methodparam">void</span> )

此函数返回一个包含所有已定义变量列表的多维数组，这些变量包括环境变量、服务器变量和用户定义的变量。

``` php
<?php
$b = array(1,1,2,3,5,8);

$arr = get_defined_vars();

// 打印 $b
print_r($arr["b"]);

// 打印 PHP 解释程序的路径（如果 PHP 作为 CGI 使用的话）
// 例如：/usr/local/bin/php
echo $arr["_"];

// 打印命令行参数（如果有的话）
print_r($arr["argv"]);

// 打印所有服务器变量
print_r($arr["_SERVER"]);

// 打印变量数组的所有可用键值
print_r(array_keys(get_defined_vars()));
?>
```

参见 <span class="function">get\_defined\_functions</span> 和 <span
class="function">get\_defined\_constants</span>。

get\_resource\_id
=================

Returns an integer identifier for the given resource

### 说明

<span class="type">int</span> <span
class="methodname">get\_resource\_id</span> ( <span
class="methodparam"><span class="type">resource</span> `$res`</span> )

This function provides a type-safe way for generating the integer
identifier for a resource.

### 参数

`res`  
The evaluated resource handle.

### 返回值

The <span class="type">int</span> identifier for the given `res`.

This function is essentially an <span class="type">int</span> cast of
`res` to make it easier to retrieve the resource ID.

### 范例

**示例 \#1 <span class="function">get\_resource\_id</span> example**

``` php
<?php
$handle = fopen('./storage/logs/lumen.log', 'rt');

echo (int) $handle . "\n\n";

echo get_resource_id($handle);

?>
```

以上例程会输出：

    698

    698

### 参见

-   <span class="function">get\_resource\_type</span>

get\_resource\_type
===================

返回资源（resource）类型

### 描述

<span class="type">string</span> <span
class="methodname">get\_resource\_type</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

此函数返回一个字符串，用于表示传递给它的 <span
class="type">resource</span> 的类型。如果参数不是合法的 <span
class="type">resource</span>，将产生错误。

``` php
<?php
$c = mysql_connect();
echo get_resource_type($c)."\n";
// 打印：mysql link

$fp = fopen("foo","w");
echo get_resource_type($fp)."\n";
// 打印：file

$doc = new_xmldoc("1.0");
echo get_resource_type($doc->doc)."\n";
// 打印：domxml document
?>
```

gettype
=======

获取变量的类型

### 描述

<span class="type">string</span> <span class="methodname">gettype</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

返回 PHP 变量的类型 `var`.

**Warning**

不要使用 <span class="function">gettype</span>
来测试某种类型，因为其返回的字符串在未来的版本中可能需要改变。此外，由于包含了字符串的比较，它的运行也是较慢的。

使用 *is\_\** 函数代替。

返回的字符串的可能值为：

-   <span class="simpara">“<span class="type">boolean</span>”（从 PHP 4
    起）</span>
-   <span class="simpara">“<span class="type">integer</span>”</span>
-   <span class="simpara">“<span
    class="type">double</span>”（由于历史原因，如果是 <span
    class="type">float</span> 则返回“double”，而不是“float”）</span>
-   <span class="simpara">“<span class="type">string</span>”</span>
-   <span class="simpara">“<span class="type">array</span>”</span>
-   <span class="simpara">“<span class="type">object</span>”</span>
-   <span class="simpara">“<span class="type">resource</span>”（从 PHP 4
    起）</span>
-   <span class="simpara">“<span class="type">NULL</span>”（从 PHP 4
    起）</span>
-   <span class="simpara">“user function”（只用于 PHP
    3，现已停用）</span>
-   <span class="simpara">“unknown type”</span>

对于 PHP 4，你应该使用 <span class="function">function\_exists</span> 和
<span class="function">method\_exists</span> 取代先前将 <span
class="function">gettype</span> 作用于函数的用法。

参见 <span class="function">settype</span>、<span
class="function">is\_array</span>、<span
class="function">is\_bool</span>、<span
class="function">is\_float</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_null</span>、<span
class="function">is\_numeric</span>、<span
class="function">is\_object</span>、<span
class="function">is\_resource</span>、<span
class="function">is\_scalar</span> 和 <span
class="function">is\_string</span>。

intval
======

获取变量的整数值

### 说明

<span class="type">int</span> <span class="methodname">intval</span> (
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
\[, <span class="methodparam"><span class="type">int</span> `$base`<span
class="initializer"> = 10</span></span> \] )

通过使用指定的进制 `base` 转换（默认是十进制），返回变量 `var` 的 <span
class="type">integer</span> 数值。 <span class="function">intval</span>
不能用于 object，否则会产生 **`E_NOTICE`** 错误并返回 1。

### 参数

`var`  
要转换成 integer 的数量值

`base`  
转化所使用的进制

> **Note**:
>
> 如果 `base` 是 0，通过检测 `var` 的格式来决定使用的进制：
>
> -   <span class="simpara"> 如果字符串包括了 "0x" (或 "0X")
>     的前缀，使用 16 进制 (hex)；否则， </span>
> -   <span class="simpara"> 如果字符串以 "0" 开始，使用 8
>     进制(octal)；否则， </span>
> -   <span class="simpara"> 将使用 10 进制 (decimal)。 </span>

### 返回值

成功时返回 `var` 的 integer 值，失败时返回 0。 空的 array 返回 0，非空的
array 返回 1。

最大的值取决于操作系统。 32 位系统最大带符号的 integer 范围是
-2147483648 到 2147483647。举例，在这样的系统上，
*intval('1000000000000')* 会返回 2147483647。64 位系统上，最大带符号的
integer 值是 9223372036854775807。

字符串有可能返回 0，虽然取决于字符串最左侧的字符。 使用
<a href="/language/types/integer.html#language.types.integer.casting" class="link">整型转换</a>
的共同规则。

### 范例

**示例 \#1 <span class="function">intval</span> 例子**

下面的例子运行于 32 位系统上。

``` php
<?php
echo intval(42);                      // 42
echo intval(4.2);                     // 4
echo intval('42');                    // 42
echo intval('+42');                   // 42
echo intval('-42');                   // -42
echo intval(042);                     // 34
echo intval('042');                   // 42
echo intval(1e10);                    // 1410065408
echo intval('1e10');                  // 1
echo intval(0x1A);                    // 26
echo intval(42000000);                // 42000000
echo intval(420000000000000000000);   // 0
echo intval('420000000000000000000'); // 2147483647
echo intval(42, 8);                   // 42
echo intval('42', 8);                 // 34
echo intval(array());                 // 0
echo intval(array('foo', 'bar'));     // 1
echo intval(false);                   // 0
echo intval(true);                    // 1
?>
```

### 注释

> **Note**:
>
> 除非 `var` 是一个字符串，否则 `base` 不会起作用。

### 参见

-   <span class="function">boolval</span>
-   <span class="function">floatval</span>
-   <span class="function">strval</span>
-   <span class="function">settype</span>
-   <span class="function">is\_numeric</span>
-   <a href="/language/types/type-juggling.html" class="link">类型转换的判别</a>
-   <a href="/ref/bc.html" class="link">BCMath 任意精度数学函数</a>

is\_array
=========

检测变量是否是数组

### 描述

<span class="type">bool</span> <span class="methodname">is\_array</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

如果 `var` 是 <span class="type">array</span>，则返回
**`TRUE`**，否则返回 **`FALSE`**。

参见 <span class="function">is\_float</span>、<span
class="function">is\_int</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_string</span> 和 <span
class="function">is\_object</span>。

is\_bool
========

检测变量是否是布尔型

### 描述

<span class="type">bool</span> <span class="methodname">is\_bool</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

如果 `var` 是 <span class="type">boolean</span> 则返回 **`TRUE`**。

**示例 \#1 <span class="function">is\_bool</span> 示例**

``` php
<?php
$a = false;
$b = 0;

// 因为 $a 是布尔型，所以结果为真
if (is_bool($a)) {
    print "Yes, this is a boolean";
}

// 因为 $b 不是布尔型，所以结果为非真
if (is_bool($b)) {
    print "Yes, this is a boolean";
}
?>
```

参见 <span class="function">is\_array</span>、<span
class="function">is\_float</span>、<span
class="function">is\_int</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_string</span> 和 <span
class="function">is\_object</span>。

is\_callable
============

检测参数是否为合法的可调用结构

### 说明

<span class="type">bool</span> <span
class="methodname">is\_callable</span> ( <span class="methodparam"><span
class="type">callable</span> `$name`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$syntax_only`<span
class="initializer"> = false</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`&$callable_name`</span> \]\] )

验证变量的内容能否作为函数调用。
这可以检查包含有效函数名的变量，或者一个数组，包含了正确编码的对象以及函数名。

### 参数

`name`  
要检查的回调函数。

`syntax_only`  
如果设置为 **`TRUE`**，这个函数仅仅验证 `name` 可能是函数或方法。
它仅仅拒绝非字符，或者未包含能用于回调函数的有效结构。有效的应该包含两个元素，第一个是一个对象或者字符，第二个元素是个字符。

`callable_name`  
接受“可调用的名称”。下面的例子是“someClass::someMethod”。 注意，尽管
someClass::SomeMethod()
的含义是可调用的静态方法，但例子的情况并不是这样的。

### 返回值

如果 `name` 可调用则返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">is\_callable</span> 例子**

``` php
<?php
//  How to check a variable to see if it can be called
//  as a function.

//
//  Simple variable containing a function
//

function someFunction() 
{
}

$functionVariable = 'someFunction';

var_dump(is_callable($functionVariable, false, $callable_name));  // bool(true)

echo $callable_name, "\n";  // someFunction

//
//  Array containing a method
//

class someClass {

  function someMethod() 
  {
  }

}

$anObject = new someClass();

$methodVariable = array($anObject, 'someMethod');

var_dump(is_callable($methodVariable, true, $callable_name));  //  bool(true)

echo $callable_name, "\n";  //  someClass::someMethod

?>
```

### 参见

-   <span class="function">function\_exists</span>
-   <span class="function">method\_exists</span>

is\_countable
=============

Verify that the contents of a variable is a countable value

### 说明

<span class="type">bool</span> <span
class="methodname">is\_countable</span> ( <span
class="methodparam"><span class="type">mixed</span> `$var`</span> )

Verify that the contents of a variable is an <span
class="type">array</span> or an object implementing <span
class="classname">Countable</span>

### 参数

`var`  
The value to check

### 返回值

Returns **`TRUE`** if `var` is countable, **`FALSE`** otherwise.

### 更新日志

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 7.3.0 | <span class="function">is\_countable</span> has been added. |

### 范例

**示例 \#1 <span class="function">is\_countable</span> examples**

``` php
<?php
var_dump(is_countable([1, 2, 3])); // bool(true)
var_dump(is_countable(new ArrayIterator(['foo', 'bar', 'baz']))); // bool(true)
var_dump(is_countable(new ArrayIterator())); // bool(true)
var_dump(is_countable(new stdClass())); // bool(false)
```

### 参见

-   <span class="function">is\_array</span>
-   <span class="function">is\_object</span>
-   <span class="function">is\_iterable</span>
-   <span class="function">is\_bool</span>

is\_double
==========

<span class="function">is\_float</span> 的别名

### 描述

此函数是 <span class="function">is\_float</span> 的别名函数。

is\_float
=========

检测变量是否是浮点型

### 描述

<span class="type">bool</span> <span class="methodname">is\_float</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

如果 `var` 是 <span class="type">float</span> 则返回
**`TRUE`**，否则返回 **`FALSE`**。

> **Note**:
>
> 若想测试一个变量是否是数字或数字字符串（如表单输入，它们通常为字符串），必须使用
> <span class="function">is\_numeric</span>。

参见 <span class="function">is\_bool</span>、<span
class="function">is\_int</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_numeric</span>、<span
class="function">is\_string</span>、<span
class="function">is\_array</span> 和 <span
class="function">is\_object</span>。

is\_int
=======

检测变量是否是整数

### 描述

<span class="type">bool</span> <span class="methodname">is\_int</span> (
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
)

如果 `var` 是 <span class="type">integer</span> 则返回
**`TRUE`**，否则返回 **`FALSE`**。

> **Note**:
>
> 若想测试一个变量是否是数字或数字字符串（如表单输入，它们通常为字符串），必须使用
> <span class="function">is\_numeric</span>。

参见 <span class="function">is\_bool</span>、<span
class="function">is\_float</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_numeric</span>、<span
class="function">is\_string</span>、<span
class="function">is\_array</span> 和 <span
class="function">is\_object</span>。

is\_integer
===========

<span class="function">is\_int</span> 的别名

### 描述

此函数是 <span class="function">is\_int</span> 的别名函数。

is\_iterable
============

Verify that the contents of a variable is an iterable value

### 说明

<span class="type">bool</span> <span
class="methodname">is\_iterable</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

Verify that the contents of a variable is accepted by the <span
class="type">iterable</span> pseudo-type, i.e. that it is either an
<span class="type">array</span> or an object implementing <span
class="classname">Traversable</span>

### 参数

`var`  
The value to check

### 返回值

Returns **`TRUE`** if `var` is iterable, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">is\_iterable</span> examples**

``` php
<?php

var_dump(is_iterable([1, 2, 3]));  // bool(true)
var_dump(is_iterable(new ArrayIterator([1, 2, 3])));  // bool(true)
var_dump(is_iterable((function () { yield 1; })()));  // bool(true)
var_dump(is_iterable(1));  // bool(false)
var_dump(is_iterable(new stdClass()));  // bool(false)

?>
```

### 参见

-   <span class="function">is\_array</span>

is\_long
========

<span class="function">is\_int</span> 的别名

### 描述

此函数是 <span class="function">is\_int</span> 的别名函数。

is\_null
========

检测变量是否为 **`NULL`**

### 描述

<span class="type">bool</span> <span class="methodname">is\_null</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

如果 `var` 是 <span class="type">null</span> 则返回 **`TRUE`**，否则返回
**`FALSE`**。

查看
<a href="/language/types/null.html#language.types.null.syntax" class="link"><strong><code>NULL</code></strong></a>
类型获知变量什么时候被认为是 **`NULL`**，而什么时候不是。

参见
<a href="/language/types/null.html#language.types.null.syntax" class="link"><strong><code>NULL</code></strong></a>、<span
class="function">is\_bool</span>、<span
class="function">is\_numeric</span>、<span
class="function">is\_float</span>、<span
class="function">is\_int</span>、<span
class="function">is\_string</span>、<span
class="function">is\_object</span>、<span
class="function">is\_array</span>、<span
class="function">is\_integer</span> 和 <span
class="function">is\_real</span>。

is\_numeric
===========

检测变量是否为数字或数字字符串

### 描述

<span class="type">bool</span> <span
class="methodname">is\_numeric</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

如果 `var` 是数字和数字字符串则返回 **`TRUE`**，否则返回 **`FALSE`**。

参见 <span class="function">is\_bool</span>、<span
class="function">is\_float</span>、<span
class="function">is\_int</span>、<span
class="function">is\_string</span>、<span
class="function">is\_object</span>、<span
class="function">is\_array</span> 和 <span
class="function">is\_integer</span>。

is\_object
==========

检测变量是否是一个对象

### 描述

<span class="type">bool</span> <span
class="methodname">is\_object</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

如果 `var` 是一个 <span class="type">object</span> 则返回
**`TRUE`**，否则返回 **`FALSE`**。

参见 <span class="function">is\_bool</span>、<span
class="function">is\_int</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_float</span>、<span
class="function">is\_string</span> 和 <span
class="function">is\_array</span>。

is\_real
========

<span class="function">is\_float</span> 的别名

### 描述

此函数是 <span class="function">is\_float</span> 的别名函数。

is\_resource
============

检测变量是否为资源类型

### 描述

<span class="type">bool</span> <span
class="methodname">is\_resource</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

如果给出的参数 `var` 是 <span class="type">resource</span> 类型，<span
class="function">is\_resource</span> 返回 **`TRUE`**，否则返回
**`FALSE`**。

查看 <span class="type">resource</span> 类型文档获取更多的信息。

is\_scalar
==========

检测变量是否是一个标量

### 描述

<span class="type">bool</span> <span
class="methodname">is\_scalar</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

如果给出的变量参数 `var` 是一个标量，<span
class="function">is\_scalar</span> 返回 **`TRUE`**，否则返回
**`FALSE`**。

标量变量是指那些包含了 <span class="type">integer</span>、<span
class="type">float</span>、<span class="type">string</span> 或 <span
class="type">boolean</span>的变量，而 <span
class="type">array</span>、<span class="type">object</span> 和 <span
class="type">resource</span> 则不是标量。

``` php
<?php
function show_var($var) {
    if (is_scalar($var)) {
        echo $var;
    } else {
        var_dump($var);
    }
}
$pi = 3.1416;
$proteins = array("hemoglobin", "cytochrome c oxidase", "ferredoxin");

show_var($pi);
// 打印：3.1416

show_var($proteins)
// 打印：
// array(3) {
//   [0]=>
//   string(10) "hemoglobin"
//   [1]=>
//   string(20) "cytochrome c oxidase"
//   [2]=>
//   string(10) "ferredoxin"
// }
?>
```

> **Note**:
>
> 尽管当前的 <span class="type">resource</span> 类型是居于整数的，但
> <span class="function">is\_scalar</span>
> 不会把它们当作是标量，因为资源是抽象数据类型。不能依赖于执行细节，因为它可能会改变。

参见 <span class="function">is\_bool</span>、<span
class="function">is\_numeric</span>、<span
class="function">is\_float</span>、<span
class="function">is\_int</span>、<span
class="function">is\_real</span>、<span
class="function">is\_string</span>、<span
class="function">is\_object</span>、<span
class="function">is\_array</span> 和 <span
class="function">is\_integer</span>。

is\_string
==========

检测变量是否是字符串

### 描述

<span class="type">bool</span> <span
class="methodname">is\_string</span> ( <span class="methodparam"><span
class="type">mixed</span> `$var`</span> )

如果 `var` 是 <span class="type">string</span> 则返回
**`TRUE`**，否则返回 **`FALSE`**。

参见 <span class="function">is\_bool</span>、<span
class="function">is\_int</span>、<span
class="function">is\_integer</span>、<span
class="function">is\_float</span>、<span
class="function">is\_real</span>、<span
class="function">is\_object</span> 和 <span
class="function">is\_array</span>。

isset
=====

检测变量是否已设置并且非 **`NULL`**

### 说明

<span class="type">bool</span> <span class="methodname">isset</span> (
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

检测变量是否设置，并且不是 **`NULL`**。

如果已经使用 <span class="function">unset</span>
释放了一个变量之后，它将不再是 <span
class="function">isset</span>。若使用 <span
class="function">isset</span> 测试一个被设置成 **`NULL`** 的变量，将返回
**`FALSE`**。同时要注意的是 null 字符（*"\\0"*）并不等同于 PHP 的
**`NULL`** 常量。

如果一次传入多个参数，那么 <span class="function">isset</span>
只有在全部参数都以被设置时返回 **`TRUE`**
计算过程从左至右，中途遇到没有设置的变量时就会立即停止。

### 参数

`var`  
要检查的变量。

`...`  
其他变量。

### 返回值

如果 `var` 存在并且值不是 **`NULL`** 则返回 **`TRUE`**，否则返回
**`FALSE`**。

### 更新日志

| 版本  | 说明                                         |
|-------|----------------------------------------------|
| 5.4.0 | 检查字符的非数字偏移量将会返回 **`FALSE`**。 |

### 范例

**示例 \#1 <span class="function">isset</span> 例子**

``` php
<?php

$var = '';

// 结果为 TRUE，所以后边的文本将被打印出来。
if (isset($var)) {
    echo "This var is set so I will print.";
}

// 在后边的例子中，我们将使用 var_dump 输出 isset() 的返回值。
// the return value of isset().

$a = "test";
$b = "anothertest";

var_dump(isset($a));      // TRUE
var_dump(isset($a, $b)); // TRUE

unset ($a);

var_dump(isset($a));     // FALSE
var_dump(isset($a, $b)); // FALSE

$foo = NULL;
var_dump(isset($foo));   // FALSE

?>
```

这对于数组中的元素也同样有效：

``` php
<?php

$a = array ('test' => 1, 'hello' => NULL, 'pie' => array('a' => 'apple'));

var_dump(isset($a['test']));            // TRUE
var_dump(isset($a['foo']));             // FALSE
var_dump(isset($a['hello']));           // FALSE

// 键 'hello' 的值等于 NULL，所以被认为是未置值的。
// 如果想检测 NULL 键值，可以试试下边的方法。 
var_dump(array_key_exists('hello', $a)); // TRUE

// Checking deeper array values
var_dump(isset($a['pie']['a']));        // TRUE
var_dump(isset($a['pie']['b']));        // FALSE
var_dump(isset($a['cake']['a']['b']));  // FALSE

?>
```

**示例 \#2 在字符串位移中使用 <span class="function">isset</span>**

PHP 5.4 改变了传入字符串位移时 <span class="function">isset</span>
的行为。

``` php
<?php
$expected_array_got_string = 'somestring';
var_dump(isset($expected_array_got_string['some_key']));
var_dump(isset($expected_array_got_string[0]));
var_dump(isset($expected_array_got_string['0']));
var_dump(isset($expected_array_got_string[0.5]));
var_dump(isset($expected_array_got_string['0.5']));
var_dump(isset($expected_array_got_string['0 Mostel']));
?>
```

以上例程在 PHP 5.3 中的输出：

    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(true)
    bool(true)

以上例程在 PHP 5.4 中的输出：

    bool(false)
    bool(true)
    bool(true)
    bool(true)
    bool(false)
    bool(false)

### 注释

**Warning**

<span class="function">isset</span>
只能用于变量，因为传递任何其它参数都将造成解析错误。若想检测<a href="/language/constants.html" class="link">常量</a>是否已设置，可使用
<span class="function">defined</span> 函数。

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

> **Note**:
>
> 如果使用 <span class="function">isset</span>
> 来检查对象无法访问的属性，如果
> <a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>
> 方法已经定义则会调用这个重载方法。

### 参见

-   <span class="function">empty</span>
-   <a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>
-   <span class="function">unset</span>
-   <span class="function">defined</span>
-   <a href="/types/comparisons.html" class="link">the type comparison tables</a>
-   <span class="function">array\_key\_exists</span>
-   <span class="function">is\_null</span>
-   错误控制
    <a href="/language/operators/errorcontrol.html" class="link">@</a>
    运算符。

print\_r
========

以易于理解的格式打印变量。

### 说明

<span class="type">mixed</span> <span class="methodname">print\_r</span>
( <span class="methodparam"><span class="type">mixed</span>
`$expression`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="function">print\_r</span>
以人类易读的格式显示一个变量的信息。

<span class="function">print\_r</span>、 <span
class="function">var\_dump</span>、 <span
class="function">var\_export</span> 都会显示对象 protected 和 private
的属性。 Class 的静态属性（static） 则不会显示。

### 参数

`expression`  
要打印的表达式。

`return`  
想要获取 <span class="function">print\_r</span> 输出的内容，使用
`return` 参数。 当此参数为 **`TRUE`**，<span
class="function">print\_r</span> 会直接返回信息，而不是输出。

### 返回值

如果输入的内容是 <span class="type">string</span>、 <span
class="type">integer</span> 或 <span
class="type">float</span>，会直接输出值本身。 如果输入的内容是 <span
class="type">array</span>，展示的格式会显示数组的键和包含的元素。<span
class="type">object</span> 也类似。

当 `return` 参数设置成 **`TRUE`**，本函数会返回 <span
class="type">string</span> 格式。否则返回 **`TRUE`**。

### 注释

> **Note**:
>
> 当使用了`return` 参数时，本函数使用其内部输出缓冲，因此不能在 <span
> class="function">ob\_start</span> 回调函数的内部使用。

### 范例

**示例 \#1 <span class="function">print\_r</span> 例子**

``` php
<pre>
<?php
$a = array ('a' => 'apple', 'b' => 'banana', 'c' => array ('x', 'y', 'z'));
print_r ($a);
?>
</pre>
```

以上例程会输出：

    <pre>
    Array
    (
        [a] => apple
        [b] => banana
        [c] => Array
            (
                [0] => x
                [1] => y
                [2] => z
            )
    )
    </pre>

**示例 \#2 `return` 参数的例子**

``` php
<?php
$b = array ('m' => 'monkey', 'foo' => 'bar', 'x' => array ('x', 'y', 'z'));
$results = print_r($b, true); // $results 包含了 print_r 的输出
?>
```

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">var\_dump</span>
-   <span class="function">var\_export</span>

serialize
=========

产生一个可存储的值的表示

### 描述

<span class="type">string</span> <span
class="methodname">serialize</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="function">serialize</span> 返回字符串，此字符串包含了表示
`value` 的字节流，可以存储于任何地方。

这有利于存储或传递 PHP 的值，同时不丢失其类型和结构。

想要将已序列化的字符串变回 PHP 的值，可使用 <span
class="function">unserialize</span>。<span
class="function">serialize</span> 可处理除了 <span
class="type">resource</span> 之外的任何类型。甚至可以 <span
class="function">serialize</span> 那些包含了指向其自身引用的数组。你正
<span class="function">serialize</span> 的数组／对象中的引用也将被存储。

当序列化对象时，PHP 将试图在序列动作之前调用该对象的成员函数 <span
class="function">\_\_sleep</span>。这样就允许对象在被序列化之前做任何清除操作。类似的，当使用
<span class="function">unserialize</span> 恢复对象时， 将调用 <span
class="function">\_\_wakeup</span> 成员函数。

> **Note**:
>
> 在 PHP 3 中，对象属性将被序列化，但是方法则会丢失。PHP 4
> 打破了此限制，可以同时存储属性和方法。请参见<a href="/language/oop5.html" class="link">类与对象</a>中的<a href="/language/oop5/serialization.html" class="link">序列化对象</a>部分获取更多信息。

**示例 \#1 <span class="function">serialize</span> 示例**

``` php
<?php
// $session_data 是包含了当前用户 session 信息的多维数组。
// 我们使用 serialize() 在请求结束之前将其存储到数据库中。

$conn = odbc_connect ("webdb", "php", "chicken");
$stmt = odbc_prepare ($conn,
      "UPDATE sessions SET data = ? WHERE id = ?");
$sqldata = array (serialize($session_data), $PHP_AUTH_USER);
if (!odbc_execute ($stmt, &$sqldata)) {
    $stmt = odbc_prepare($conn,
     "INSERT INTO sessions (id, data) VALUES(?, ?)");
    if (!odbc_execute($stmt, &$sqldata)) {
    /* 出错 */
    }
}
?>
```

参见：<span class="function">unserialize</span>。

settype
=======

设置变量的类型

### 说明

<span class="type">bool</span> <span class="methodname">settype</span> (
<span class="methodparam"><span class="type">mixed</span> `&$var`</span>
, <span class="methodparam"><span class="type">string</span>
`$type`</span> )

将变量 `var` 的类型设置成 `type`。

### 参数

`var`  
要转换的变量。

`type`  
`type` 的可能值为：

-   <span class="simpara"> “boolean” （或为“bool”，从 PHP 4.2.0 起）
    </span>
-   <span class="simpara"> “integer” （或为“int”，从 PHP 4.2.0 起）
    </span>
-   <span class="simpara"> “float” （只在 PHP 4.2.0
    之后可以使用，对于旧版本中使用的“double”现已停用） </span>
-   <span class="simpara"> "string" </span>
-   <span class="simpara"> "array" </span>
-   <span class="simpara"> "object" </span>
-   <span class="simpara"> “null” （从 PHP 4.2.0 起） </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">settype</span> 示例**

``` php
<?php
$foo = "5bar"; // string
$bar = true;   // boolean

settype($foo, "integer"); // $foo 现在是 5   (integer)
settype($bar, "string");  // $bar 现在是 "1" (string)
?>
```

### 注释

> **Note**:
>
> Maximum value for "int" is **`PHP_INT_MAX`**.

### 参见

-   <span class="function">gettype</span>
-   <a href="/language/types/type-juggling.html#language.types.typecasting" class="link">类型转换</a>
-   <a href="/language/types/type-juggling.html" class="link">类型戏法</a>

strval
======

获取变量的字符串值

### 描述

<span class="type">string</span> <span class="methodname">strval</span>
( <span class="methodparam"><span class="type">mixed</span>
`$var`</span> )

返回 `var` 的 <span class="type">string</span> 值。 参见 <span
class="type">string</span> 文档获取更多关于字符串转换的信息。

`var` 可以是任何标量类型。不能将 <span class="function">strval</span>
用于数组或对象。

参见 <span class="function">floatval</span>、<span
class="function">intval</span>、<span class="function">settype</span>
和<a href="/language/types/type-juggling.html" class="link">类型戏法</a>。

unserialize
===========

从已存储的表示中创建 PHP 的值

### 说明

<span class="type">mixed</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$str`</span> )

<span class="function">unserialize</span>
对单一的已序列化的变量进行操作，将其转换回 PHP 的值。

### 参数

`str`  
序列化后的字符串。

若被解序列化的变量是一个对象，在成功地重新构造对象之后，PHP
会自动地试图去调用
<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
成员函数（如果存在的话）。

> **Note**: **unserialize\_callback\_func 指令**  
>
> 如果在解序列化的时候需要实例化一个未定义类，则可以设置回调函数以供调用（以免得到的是不完整的
> <span class="type">object</span>
> “\_\_PHP\_Incomplete\_Class”）。可通过 `php.ini`、<span
> class="function">ini\_set</span> 或 `.htaccess`
> 定义‘unserialize\_callback\_func’。每次实例化一个未定义类时它都会被调用。若要禁止这个特性，只需置空此设定。

### 返回值

返回的是转换之后的值，可为 <span class="type">integer</span>、<span
class="type">float</span>、<span class="type">string</span>、<span
class="type">array</span> 或 <span class="type">object</span>。

如果传递的字符串不可解序列化，则返回 **`FALSE`**，并产生一个
**`E_NOTICE`**。

### 更新日志

| 版本  | 说明                                      |
|-------|-------------------------------------------|
| 4.2.0 | 添加了 unserialize\_callback\_func 指令。 |

### 范例

**示例 \#1 <span class="function">unserialize</span> 例子**

``` php
<?php
// 这里，我们使用 unserialize() 装载来自数据库的 $session_data 数组中的会话数据。
// 此例是描述 serialize() 的那个例子的补充。

$conn = odbc_connect("webdb", "php", "chicken");
$stmt = odbc_prepare($conn, "SELECT data FROM sessions WHERE id = ?");
$sqldata = array($_SERVER['PHP_AUTH_USER']);
if (!odbc_execute($stmt, $sqldata) || !odbc_fetch_into($stmt, $tmp)) {
    // 如果执行出错或返回错误，则初始化为空数组
    $session_data = array();
} else {
    // 现在我们需要的是 $tmp[0] 中已序列化的数据。
    $session_data = unserialize($tmp[0]);
    if (!is_array($session_data)) {
        // 出错，初始化为空数组
        $session_data = array();
    }
}
?>
```

**示例 \#2 unserialize\_callback\_func 例子**

``` php
<?php
$serialized_object='O:1:"a":1:{s:5:"value";s:3:"100";}';

// unserialize_callback_func 从 PHP 4.2.0 起可用
ini_set('unserialize_callback_func', 'mycallback'); // 设置您的回调函数

function mycallback($classname) 
{
   // 只需包含含有类定义的文件
   // $classname 指出需要的是哪一个类
}
?>
```

### 注释

**Warning**

如果反序列化了 **`FALSE`** 的值，或者在过程中发生了错误，都会返回
**`FALSE`**。 可以通过 `str` 和 *serialize(false)* 进行比较，或者捕捉
**`E_NOTICE`** 错误来判断这种特殊情况。

### 参见

-   <span class="function">serialize</span>
-   <a href="/language/oop5/autoload.html" class="link">自动加载对象</a>
-   <a href="/var/setup.html#" class="link">unserialize_callback_func</a>
-   <a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>

unset
=====

释放给定的变量

### 说明

<span class="type">void</span> <span class="methodname">unset</span> (
<span class="methodparam"><span class="type">mixed</span> `$var`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

<span class="function">unset</span> 销毁指定的变量。

<span class="function">unset</span>
在函数中的行为会依赖于想要销毁的变量的类型而有所不同。

如果在函数中 <span class="function">unset</span>
一个全局变量，则只是局部变量被销毁，而在调用环境中的变量将保持调用 <span
class="function">unset</span> 之前一样的值。

``` php
<?php
function destroy_foo() {
    global $foo;
    unset($foo);
}

$foo = 'bar';
destroy_foo();
echo $foo;
?>
```

以上例程会输出：

    bar

如果您想在函数中 <span class="function">unset</span>
一个全局变量，可使用 `$GLOBALS` 数组来实现：

``` php
<?php
function foo() 
{
    unset($GLOBALS['bar']);
}

$bar = "something";
foo();
?>
```

如果在函数中 <span class="function">unset</span>
一个通过引用传递的变量，则只是局部变量被销毁，而在调用环境中的变量将保持调用
<span class="function">unset</span> 之前一样的值。

``` php
<?php
function foo(&$bar) {
    unset($bar);
    $bar = "blah";
}

$bar = 'something';
echo "$bar\n";

foo($bar);
echo "$bar\n";
?>
```

以上例程会输出：

    something
    something

如果在函数中 <span class="function">unset</span>
一个静态变量，那么在函数内部此静态变量将被销毁。但是，当再次调用此函数时，此静态变量将被复原为上次被销毁之前的值。

``` php
<?php
function foo()
{
    static $bar;
    $bar++;
    echo "Before unset: $bar, ";
    unset($bar);
    $bar = 23;
    echo "after unset: $bar\n";
}

foo();
foo();
foo();
?>
```

以上例程会输出：

    Before unset: 1, after unset: 23
    Before unset: 2, after unset: 23
    Before unset: 3, after unset: 23

### 参数

`var`  
要销毁的变量。

`...`  
其他变量……

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">unset</span> 示例**

``` php
<?php
// 销毁单个变量
unset ($foo);

// 销毁单个数组元素
unset ($bar['quux']);

// 销毁一个以上的变量
unset($foo1, $foo2, $foo3);
?>
```

**示例 \#2 使用 *(unset)* 类型强制转换**

*(unset)* 类型强制转换常常和函数 <span class="function">unset</span>
引起困惑。 为了完整性，*(unset)* 是作为一个 *NULL*
类型的强制转换。它不会改变变量的类型。

``` php
<?php
$name = 'Felipe';

var_dump((unset) $name);
var_dump($name);
?>
```

以上例程会输出：

    NULL
    string(6) "Felipe"

### 注释

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

> **Note**:
>
> It is possible to unset even object properties visible in current
> context.

> **Note**:
>
> 在 PHP 5 之前无法在对象里销毁 *$this*。

> **Note**:
>
> 在 <span class="function">unset</span>
> 一个无法访问的对象属性时，如果定义了
> <a href="/language/oop5/overloading.html#object.unset" class="link">__unset()</a>
> 则对调用这个重载方法。

### 参见

-   <span class="function">isset</span>
-   <span class="function">empty</span>
-   <a href="/language/oop5/overloading.html#object.unset" class="link">__unset()</a>
-   <span class="function">array\_splice</span>

var\_dump
=========

打印变量的相关信息

### 说明

<span class="type">void</span> <span class="methodname">var\_dump</span>
( <span class="methodparam"><span class="type">mixed</span>
`$expression`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \] )

此函数显示关于一个或多个表达式的结构信息，包括表达式的类型与值。数组将递归展开值，通过缩进显示其结构。

In PHP 5 all public, private and protected properties of objects will be
returned in the output.

**小贴士**

和直接将结果输出到浏览器一样，可使用<a href="/book/outcontrol.html" class="link">输出控制函数</a>来捕获当前函数的输出，然后(例如)保存到一个
<span class="type">string</span> 中。

### 参数

`expression`  
你要打印的变量。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">var\_dump</span> 例子**

``` php
<?php
$a = array(1, 2, array("a", "b", "c"));
var_dump($a);
?>
```

以上例程会输出：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      array(3) {
        [0]=>
        string(1) "a"
        [1]=>
        string(1) "b"
        [2]=>
        string(1) "c"
      }
    }

``` php
<?php

$b = 3.1;
$c = true;
var_dump($b, $c);

?>
```

以上例程会输出：

    float(3.1)
    bool(true)

### 参见

-   <span class="function">var\_export</span>
-   <span class="function">print\_r</span>

var\_export
===========

输出或返回一个变量的字符串表示

### 说明

<span class="type">mixed</span> <span
class="methodname">var\_export</span> ( <span class="methodparam"><span
class="type">mixed</span> `$expression`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$return`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="function">var\_export</span>
函数返回关于传递给该函数的变量的结构信息，它和 <span
class="function">var\_dump</span> 函数类似，不同的是其返回的表示是合法的
PHP 代码。

### 参数

`expression`  
想要输出的变量名。

`return`  
此参数为 **`TRUE`** 时，<span class="function">var\_export</span>
将返回一个变量，而不是输出它。

### 返回值

参数 `return` 为 **`TRUE`** 时返回变量，否则返回 **`NULL`**。

### 注释

> **Note**:
>
> 当使用了`return` 参数时，本函数使用其内部输出缓冲，因此不能在 <span
> class="function">ob\_start</span> 回调函数的内部使用。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                                            |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.3.0 | Now exports <span class="classname">stdClass</span> objects as an array cast to an object (`(object) array( ... )`), rather than using the nonexistent method <span class="methodname">stdClass::\_\_setState</span>. The practical effect is that now <span class="classname">stdClass</span> is exportable, and the resulting code will even work on earlier versions of PHP. |

### 范例

**示例 \#1 <span class="function">var\_export</span> 示例**

``` php
<?php
$a = array (1, 2, array ("a", "b", "c"));
var_export($a);
?>
```

以上例程会输出：

    array (
      0 => 1,
      1 => 2,
      2 => 
      array (
        0 => 'a',
        1 => 'b',
        2 => 'c',
      ),
    )

``` php
<?php

$b = 3.1;
$v = var_export($b, true);
echo $v;

?>
```

以上例程会输出：

    3.1

**示例 \#2 输出类 stdClass (自 PHP 7.3.0 起)**

``` php
<?php
$person = new stdClass;
$person->name = 'ElePHPant ElePHPantsdotter';
$person->website = 'https://php.net/elephpant.php';

var_export($person);
```

以上例程会输出：

    (object) array(
       'name' => 'ElePHPant ElePHPantsdotter',
       'website' => 'https://php.net/elephpant.php',
    )

**示例 \#3 输出对象 (自 PHP 5.1.0 起)**

``` php
<?php
class A { public $var; }
$a = new A;
$a->var = 5;
var_export($a);
?>
```

以上例程会输出：

    A::__set_state(array(
       'var' => 5,
    ))

**示例 \#4 使用
<a href="/language/oop5/magic.html#object.set-state" class="link">__set_state()</a>
(自 PHP 5.1.0 起)**

``` php
<?php
class A
{
    public $var1;
    public $var2;

    public static function __set_state($an_array)
    {
        $obj = new A;
        $obj->var1 = $an_array['var1'];
        $obj->var2 = $an_array['var2'];
        return $obj;
    }
}

$a = new A;
$a->var1 = 5;
$a->var2 = 'foo';

eval('$b = ' . var_export($a, true) . ';'); // $b = A::__set_state(array(
                                            //    'var1' => 5,
                                            //    'var2' => 'foo',
                                            // ));
var_dump($b);
?>
```

以上例程会输出：

    object(A)#2 (2) {
      ["var1"]=>
      int(5)
      ["var2"]=>
      string(3) "foo"
    }

### 注释

> **Note**:
>
> 类型为 <span class="type">resource</span> 的变量无法通过此函数输出。

> **Note**:
>
> <span class="function">var\_export</span> does not handle circular
> references as it would be close to impossible to generate parsable PHP
> code for that. If you want to do something with the full
> representation of an array or object, use <span
> class="function">serialize</span>.

**Warning**

When <span class="function">var\_export</span> exports objects, the
leading backslash is not included in the class name of namespaced
classes for maximum compatibility.

> **Note**:
>
> To be able to evaluate the PHP generated by <span
> class="function">var\_export</span>, all processed objects must
> implement the magic
> <a href="/language/oop5/magic.html#object.set-state" class="link">__set_state</a>
> method. The only exception is <span class="classname">stdClass</span>,
> which is exported using an array cast to an object.

### 参见

-   <span class="function">print\_r</span>
-   <span class="function">serialize</span>
-   <span class="function">var\_dump</span>

**目录**

-   [boolval](/ref/var.html#boolval) — 获取变量的布尔值
-   [debug\_zval\_dump](/ref/var.html#debug_zval_dump) — Dumps a string
    representation of an internal zend value to output
-   [doubleval](/ref/var.html#doubleval) — floatval 的别名
-   [empty](/ref/var.html#empty) — 检查一个变量是否为空
-   [floatval](/ref/var.html#floatval) — 获取变量的浮点值
-   [get\_defined\_vars](/ref/var.html#get_defined_vars) —
    返回由所有已定义变量所组成的数组
-   [get\_resource\_id](/ref/var.html#get_resource_id) — Returns an
    integer identifier for the given resource
-   [get\_resource\_type](/ref/var.html#get_resource_type) —
    返回资源（resource）类型
-   [gettype](/ref/var.html#gettype) — 获取变量的类型
-   [intval](/ref/var.html#intval) — 获取变量的整数值
-   [is\_array](/ref/var.html#is_array) — 检测变量是否是数组
-   [is\_bool](/ref/var.html#is_bool) — 检测变量是否是布尔型
-   [is\_callable](/ref/var.html#is_callable) —
    检测参数是否为合法的可调用结构
-   [is\_countable](/ref/var.html#is_countable) — Verify that the
    contents of a variable is a countable value
-   [is\_double](/ref/var.html#is_double) — is\_float 的别名
-   [is\_float](/ref/var.html#is_float) — 检测变量是否是浮点型
-   [is\_int](/ref/var.html#is_int) — 检测变量是否是整数
-   [is\_integer](/ref/var.html#is_integer) — is\_int 的别名
-   [is\_iterable](/ref/var.html#is_iterable) — Verify that the contents
    of a variable is an iterable value
-   [is\_long](/ref/var.html#is_long) — is\_int 的别名
-   [is\_null](/ref/var.html#is_null) — 检测变量是否为 NULL
-   [is\_numeric](/ref/var.html#is_numeric) —
    检测变量是否为数字或数字字符串
-   [is\_object](/ref/var.html#is_object) — 检测变量是否是一个对象
-   [is\_real](/ref/var.html#is_real) — is\_float 的别名
-   [is\_resource](/ref/var.html#is_resource) — 检测变量是否为资源类型
-   [is\_scalar](/ref/var.html#is_scalar) — 检测变量是否是一个标量
-   [is\_string](/ref/var.html#is_string) — 检测变量是否是字符串
-   [isset](/ref/var.html#isset) — 检测变量是否已设置并且非 NULL
-   [print\_r](/ref/var.html#print_r) — 以易于理解的格式打印变量。
-   [serialize](/ref/var.html#serialize) — 产生一个可存储的值的表示
-   [settype](/ref/var.html#settype) — 设置变量的类型
-   [strval](/ref/var.html#strval) — 获取变量的字符串值
-   [unserialize](/ref/var.html#unserialize) — 从已存储的表示中创建 PHP
    的值
-   [unset](/ref/var.html#unset) — 释放给定的变量
-   [var\_dump](/ref/var.html#var_dump) — 打印变量的相关信息
-   [var\_export](/ref/var.html#var_export) —
    输出或返回一个变量的字符串表示
