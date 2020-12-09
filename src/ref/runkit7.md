runkit7\_constant\_add
======================

Similar to define(), but allows defining in class definitions as well

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_constant\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$constname`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$newVisibility`</span> \] )

### 参数

`constname`  
Name of constant to declare. Either a string to indicate a global
constant, or *classname::constname* to indicate a class constant.

`value`  
NULL, Bool, Long, Double, String, Array, or Resource value to store in
the new constant.

`newVisibility`  
Visibility of the constant, for class constants. Public by default. One
of the **`RUNKIT7_ACC_*`** constants.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">define</span>
-   <span class="function">runkit7\_constant\_redefine</span>
-   <span class="function">runkit7\_constant\_remove</span>

runkit7\_constant\_redefine
===========================

Redefine an already defined constant

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_constant\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$constname`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$newVisibility`</span> \] )

### 参数

`constname`  
Constant to redefine. Either the name of a global constant, or
*classname::constname* indicating class constant.

`value`  
Value to assign to the constant.

`newVisibility`  
The new visibility of the constant, for class constants. Unchanged by
default. One of the **`RUNKIT7_ACC_*`** constants.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">runkit7\_constant\_add</span>
-   <span class="function">runkit7\_constant\_remove</span>

runkit7\_constant\_remove
=========================

Remove/Delete an already defined constant

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_constant\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$constname`</span>
)

### 参数

`constname`  
Name of the constant to remove. Either the name of a global constant, or
*classname::constname* indicating a class constant.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">define</span>
-   <span class="function">runkit7\_constant\_add</span>
-   <span class="function">runkit7\_constant\_redefine</span>

runkit7\_function\_add
======================

Add a new function, similar to <span
class="function">create\_function</span>

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$arglist`</span> , <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$return_by_reference`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$return_type`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_strict`</span>
\]\]\]\] )

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">Closure</span>
`$closure`</span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$return_type`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$is_strict`</span>
\]\]\] )

### 参数

`funcname`  
Name of the function to be created

`arglist`  
Comma separated argument list

`code`  
Code making up the function

`closure`  
A <span class="classname">closure</span> that defines the function.

`return_by_reference`  
Whether the function should return by reference.

`doc_comment`  
The doc comment of the function.

`return_type`  
The return type of the function.

`is_strict`  
Whether the function should behave as if it were declared in a file with
*strict\_types=1*

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 A <span class="function">runkit7\_function\_add</span>
example**

``` php
<?php
runkit7_function_add('testme','$a,$b','echo "The value of a is $a\n"; echo "The value of b is $b\n";');
testme(1,2);
?>
```

以上例程会输出：

    The value of a is 1
    The value of b is 2

### 参见

-   <span class="function">create\_function</span>
-   <span class="function">runkit7\_function\_redefine</span>
-   <span class="function">runkit7\_function\_copy</span>
-   <span class="function">runkit7\_function\_rename</span>
-   <span class="function">runkit7\_function\_remove</span>
-   <span class="function">runkit7\_method\_add</span>

runkit7\_function\_copy
=======================

Copy a function to a new function name

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_copy</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$targetname`</span> )

### 参数

`funcname`  
Name of the existing function

`targetname`  
Name of the new function to copy the definition to

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 A <span class="function">runkit7\_function\_copy</span>
example**

``` php
<?php
function original() {
  echo "In a function\n";
}
runkit7_function_copy('original','duplicate');
original();
duplicate();
?>
```

以上例程会输出：

    In a function
    In a function

### 参见

-   <span class="function">runkit7\_function\_add</span>
-   <span class="function">runkit7\_function\_redefine</span>
-   <span class="function">runkit7\_function\_rename</span>
-   <span class="function">runkit7\_function\_remove</span>

runkit7\_function\_redefine
===========================

Replace a function definition with a new implementation

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$arglist`</span> , <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$return_by_reference`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$return_type`</span> \[, <span
class="methodparam"><span class="type">string</span> `$is_strict`</span>
\]\]\]\] )

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">Closure</span>
`$closure`</span> \[, <span class="methodparam"><span
class="type">string</span> `$doc_comment`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$return_type`</span> \[, <span
class="methodparam"><span class="type">string</span> `$is_strict`</span>
\]\]\] )

> **Note**: <span
> class="simpara">默认情况下，仅在用户空间可删除，重命名，或者修改函数。为了覆盖内部函数，必须启用
> `php.ini` 中的 *runkit.internal\_override* 设置。</span>

### 参数

`funcname`  
Name of function to redefine

`arglist`  
New list of arguments to be accepted by function

`code`  
New code implementation

`closure`  
A <span class="classname">closure</span> that defines the function.

`return_by_reference`  
Whether the function should return by reference.

`doc_comment`  
The doc comment of the function.

`return_type`  
The return type of the function.

`is_strict`  
Whether the function behaves as if it was declared in a file with
*strict\_types=1*

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 A <span class="function">runkit7\_function\_redefine</span>
example**

``` php
<?php
function testme() {
  echo "Original Testme Implementation\n";
}
testme();
runkit7_function_redefine('testme','','echo "New Testme Implementation\n";');
testme();
?>
```

以上例程会输出：

    Original Testme Implementation
    New Testme Implementation

### 参见

-   <span class="function">runkit7\_function\_add</span>
-   <span class="function">runkit7\_function\_copy</span>
-   <span class="function">runkit7\_function\_rename</span>
-   <span class="function">runkit7\_function\_remove</span>
-   <span class="function">runkit7\_method\_redefine</span>

runkit7\_function\_remove
=========================

Remove a function definition

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
)

> **Note**: <span
> class="simpara">默认情况下，仅在用户空间可删除，重命名，或者修改函数。为了覆盖内部函数，必须启用
> `php.ini` 中的 *runkit.internal\_override* 设置。</span>

### 参数

`funcname`  
Name of the function to be deleted

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">runkit7\_function\_add</span>
-   <span class="function">runkit7\_function\_copy</span>
-   <span class="function">runkit7\_function\_redefine</span>
-   <span class="function">runkit7\_function\_rename</span>

runkit7\_function\_rename
=========================

Change a function's name

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_function\_rename</span> ( <span
class="methodparam"><span class="type">string</span> `$funcname`</span>
, <span class="methodparam"><span class="type">string</span>
`$newname`</span> )

> **Note**: <span
> class="simpara">默认情况下，仅在用户空间可删除，重命名，或者修改函数。为了覆盖内部函数，必须启用
> `php.ini` 中的 *runkit.internal\_override* 设置。</span>

### 参数

`funcname`  
Current function name

`newname`  
New function name

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">runkit7\_function\_add</span>
-   <span class="function">runkit7\_function\_copy</span>
-   <span class="function">runkit7\_function\_redefine</span>
-   <span class="function">runkit7\_function\_remove</span>

runkit7\_import
===============

Process a PHP file importing function and class definitions, overwriting
where appropriate

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_import</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`</span> \] )

Similar to <span class="function">include</span>. However, any code
residing outside of a function or class is simply ignored. Additionally,
depending on the value of `flags`, any functions or classes which
already exist in the currently running environment may be automatically
overwritten by their new definitions.

### 参数

`filename`  
Filename to import function and class definitions from

`flags`  
Bitwise OR of the
<a href="/runkit7/constants.html" class="link"><em>RUNKIT7_IMPORT_*</em> family of constants</a>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

runkit7\_method\_add
====================

Dynamically adds a new method to a given class

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> , <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT7\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$return_type`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_strict`</span> \]\]\]\] )

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">Closure</span> `$closure`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT7\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$return_type`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_strict`</span> \]\]\]\] )

### 参数

`classname`  
The class to which this method will be added

`methodname`  
The name of the method to add

`args`  
Comma-delimited list of arguments for the newly-created method

`code`  
The code to be evaluated when `methodname` is called

`closure`  
A <span class="classname">closure</span> that defines the method.

`flags`  
The type of method to create, can be **`RUNKIT7_ACC_PUBLIC`**,
**`RUNKIT7_ACC_PROTECTED`** or **`RUNKIT7_ACC_PRIVATE`** optionally
combined via bitwise OR with **`RUNKIT7_ACC_STATIC`**

`doc_comment`  
The doc comment of the method.

`return_type`  
The return type of the method.

`is_strict`  
Whether the method behaves as if it were declared in a file with
*strict\_types=1*

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">runkit7\_method\_add</span> example**

``` php
<?php
class Example {
    function foo() {
        echo "foo!\n";
    }
}

// create an Example object
$e = new Example();

// Add a new public method
runkit7_method_add(
    'Example',
    'add',
    '$num1, $num2',
    'return $num1 + $num2;',
    RUNKIT7_ACC_PUBLIC
);

// add 12 + 4
echo $e->add(12, 4);
?>
```

以上例程会输出：

    16

### 参见

-   <span class="function">runkit7\_method\_copy</span>
-   <span class="function">runkit7\_method\_redefine</span>
-   <span class="function">runkit7\_method\_remove</span>
-   <span class="function">runkit7\_method\_rename</span>
-   <span class="function">runkit7\_function\_add</span>

runkit7\_method\_copy
=====================

Copies a method from class to another

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_copy</span> ( <span
class="methodparam"><span class="type">string</span> `$dClass`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dMethod`</span> , <span class="methodparam"><span
class="type">string</span> `$sClass`</span> \[, <span
class="methodparam"><span class="type">string</span> `$sMethod`</span>
\] )

### 参数

`dClass`  
Destination class for copied method

`dMethod`  
Destination method name

`sClass`  
Source class of the method to copy

`sMethod`  
Name of the method to copy from the source class. If this parameter is
omitted, the value of `dMethod` is assumed.

### 返回值

### 范例

**示例 \#1 <span class="function">runkit7\_method\_copy</span> example**

``` php
<?php
class Foo {
    function example() {
        return "foo!\n";
    }
}

class Bar {
    // initially, no methods
}

// copy the example() method from the Foo class to the Bar class, as baz()
runkit7_method_copy('Bar', 'baz', 'Foo', 'example');

// output copied function
echo Bar::baz();
?>
```

以上例程会输出：

    foo!

### 参见

-   <span class="function">runkit7\_method\_add</span>
-   <span class="function">runkit7\_method\_redefine</span>
-   <span class="function">runkit7\_method\_remove</span>
-   <span class="function">runkit7\_method\_rename</span>
-   <span class="function">runkit7\_function\_copy</span>

runkit7\_method\_redefine
=========================

Dynamically changes the code of the given method

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> , <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT7\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$return_type`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_strict`</span> \]\]\]\] )

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">Closure</span> `$closure`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = RUNKIT7\_ACC\_PUBLIC</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$doc_comment`<span
class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$return_type`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$is_strict`</span> \]\]\]\] )

### 参数

`classname`  
The class in which to redefine the method

`methodname`  
The name of the method to redefine

`args`  
Comma-delimited list of arguments for the redefined method

`code`  
The new code to be evaluated when `methodname` is called

`closure`  
A <span class="classname">closure</span> that defines the method.

`flags`  
The redefined method can be **`RUNKIT7_ACC_PUBLIC`**,
**`RUNKIT7_ACC_PROTECTED`** or **`RUNKIT7_ACC_PRIVATE`** optionally
combined via bitwise OR with **`RUNKIT7_ACC_STATIC`**

`doc_comment`  
The doc comment of the method.

`return_type`  
The return type of the method.

`is_strict`  
Whether the method behaves as if it was declared in a file with
*strict\_types=1*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">runkit7\_method\_redefine</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// create an Example object
$e = new Example();

// output Example::foo() (before redefine)
echo "Before: " . $e->foo();

// Redefine the 'foo' method
runkit7_method_redefine(
    'Example',
    'foo',
    '',
    'return "bar!\n";',
    RUNKIT7_ACC_PUBLIC
);

// output Example::foo() (after redefine)
echo "After: " . $e->foo();
?>
```

以上例程会输出：

    Before: foo!
    After: bar!

### 参见

-   <span class="function">runkit7\_method\_add</span>
-   <span class="function">runkit7\_method\_copy</span>
-   <span class="function">runkit7\_method\_remove</span>
-   <span class="function">runkit7\_method\_rename</span>
-   <span class="function">runkit7\_function\_redefine</span>

runkit7\_method\_remove
=======================

Dynamically removes the given method

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

### 参数

`classname`  
The class in which to remove the method

`methodname`  
The name of the method to remove

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">runkit7\_method\_remove</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }

    function bar() {
        return "bar!\n";
    }
}

// Remove the 'foo' method
runkit7_method_remove(
    'Example',
    'foo'
);

echo implode(' ', get_class_methods('Example'));

?>
```

以上例程会输出：

    bar

### 参见

-   <span class="function">runkit7\_method\_add</span>
-   <span class="function">runkit7\_method\_copy</span>
-   <span class="function">runkit7\_method\_redefine</span>
-   <span class="function">runkit7\_method\_rename</span>
-   <span class="function">runkit7\_function\_remove</span>

runkit7\_method\_rename
=======================

Dynamically changes the name of the given method

### 说明

<span class="type">bool</span> <span
class="methodname">runkit7\_method\_rename</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$newname`</span> )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

### 参数

`classname`  
The class in which to rename the method

`methodname`  
The name of the method to rename

`newname`  
The new name to give to the renamed method

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">runkit7\_method\_rename</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// Rename the 'foo' method to 'bar'
runkit7_method_rename(
    'Example',
    'foo',
    'bar'
);

// output renamed function
echo Example::bar();
?>
```

以上例程会输出：

    foo!

### 参见

-   <span class="function">runkit7\_method\_add</span>
-   <span class="function">runkit7\_method\_copy</span>
-   <span class="function">runkit7\_method\_redefine</span>
-   <span class="function">runkit7\_method\_remove</span>
-   <span class="function">runkit7\_function\_rename</span>

runkit7\_object\_id
===================

Return the integer object handle for given object

### 说明

<span class="type">int</span> <span
class="methodname">runkit7\_object\_id</span> ( <span
class="methodparam"><span class="type">object</span> `$obj`</span> )

This function returns a unique identifier for the object. The object id
is unique for the lifetime of the object. Once the object is destroyed,
its id may be reused for other objects. This behavior is similar to
<span class="function">spl\_object\_hash</span>.

### 参数

`obj`  
Any object.

### 返回值

An integer identifier that is unique for each currently existing object
and is always the same for each object.

### 注释

> **Note**:
>
> When an object is destroyed, its id may be reused for other objects.

runkit7\_superglobals
=====================

Return numerically indexed array of registered superglobals

### 说明

<span class="type">array</span> <span
class="methodname">runkit7\_superglobals</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns a numerically indexed array of the currently registered
superglobals. i.e. \_GET, \_POST, \_REQUEST, \_COOKIE, \_SESSION,
\_SERVER, \_ENV, \_FILES

### 参见

-   <a href="/language/variables/scope.html" class="link">Variable Scope</a>

runkit7\_zval\_inspect
======================

Returns information about the passed in value with data types, reference
counts, etc

### 说明

<span class="type">array</span> <span
class="methodname">runkit7\_zval\_inspect</span> ( <span
class="methodparam"><span class="type">string</span> `$value`</span> )

### 参数

`value`  
The value to return the representation of

**目录**

-   [runkit7\_constant\_add](/ref/runkit7.html#runkit7_constant_add) —
    Similar to define(), but allows defining in class definitions as
    well
-   [runkit7\_constant\_redefine](/ref/runkit7.html#runkit7_constant_redefine)
    — Redefine an already defined constant
-   [runkit7\_constant\_remove](/ref/runkit7.html#runkit7_constant_remove)
    — Remove/Delete an already defined constant
-   [runkit7\_function\_add](/ref/runkit7.html#runkit7_function_add) —
    Add a new function, similar to create\_function
-   [runkit7\_function\_copy](/ref/runkit7.html#runkit7_function_copy) —
    Copy a function to a new function name
-   [runkit7\_function\_redefine](/ref/runkit7.html#runkit7_function_redefine)
    — Replace a function definition with a new implementation
-   [runkit7\_function\_remove](/ref/runkit7.html#runkit7_function_remove)
    — Remove a function definition
-   [runkit7\_function\_rename](/ref/runkit7.html#runkit7_function_rename)
    — Change a function's name
-   [runkit7\_import](/ref/runkit7.html#runkit7_import) — Process a PHP
    file importing function and class definitions, overwriting where
    appropriate
-   [runkit7\_method\_add](/ref/runkit7.html#runkit7_method_add) —
    Dynamically adds a new method to a given class
-   [runkit7\_method\_copy](/ref/runkit7.html#runkit7_method_copy) —
    Copies a method from class to another
-   [runkit7\_method\_redefine](/ref/runkit7.html#runkit7_method_redefine)
    — Dynamically changes the code of the given method
-   [runkit7\_method\_remove](/ref/runkit7.html#runkit7_method_remove) —
    Dynamically removes the given method
-   [runkit7\_method\_rename](/ref/runkit7.html#runkit7_method_rename) —
    Dynamically changes the name of the given method
-   [runkit7\_object\_id](/ref/runkit7.html#runkit7_object_id) — Return
    the integer object handle for given object
-   [runkit7\_superglobals](/ref/runkit7.html#runkit7_superglobals) —
    Return numerically indexed array of registered superglobals
-   [runkit7\_zval\_inspect](/ref/runkit7.html#runkit7_zval_inspect) —
    Returns information about the passed in value with data types,
    reference counts, etc
