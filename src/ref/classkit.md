classkit\_import
================

Import new class method definitions from a file

### 说明

<span class="type">array</span> <span
class="methodname">classkit\_import</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`filename`  
The filename of the class method definitions to import

### 返回值

Associative array of imported methods

### 范例

**示例 \#1 <span class="function">classkit\_import</span> example**

``` php
<?php
// file: newclass.php
class Example {
    function foo() {
        return "bar!\n";
    }
}
?>
```

``` php
<?php
// requires newclass.php (see above)
class Example {
    function foo() {
        return "foo!\n";
    }
}

$e = new Example();

// output original
echo $e->foo();

// import replacement method
classkit_import('newclass.php');

// output imported
echo $e->foo();

?>
```

以上例程会输出：

    foo!
    bar!

### 参见

-   <span class="function">classkit\_method\_add</span>
-   <span class="function">classkit\_method\_copy</span>

classkit\_method\_add
=====================

Dynamically adds a new method to a given class

### 说明

<span class="type">bool</span> <span
class="methodname">classkit\_method\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> , <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = CLASSKIT\_ACC\_PUBLIC</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`classname`  
The class to which this method will be added

`methodname`  
The name of the method to add

`args`  
Comma-delimited list of arguments for the newly-created method

`code`  
The code to be evaluated when `methodname` is called

`flags`  
The type of method to create, can be **`CLASSKIT_ACC_PUBLIC`**,
**`CLASSKIT_ACC_PROTECTED`** or **`CLASSKIT_ACC_PRIVATE`**

> **Note**:
>
> This parameter is only used as of PHP 5, because, prior to this, all
> methods were public.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">classkit\_method\_add</span> example**

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
classkit_method_add(
    'Example',
    'add',
    '$num1, $num2',
    'return $num1 + $num2;',
    CLASSKIT_ACC_PUBLIC
);

// add 12 + 4
echo $e->add(12, 4);
?>
```

以上例程会输出：

    16

### 参见

-   <span class="function">classkit\_method\_copy</span>
-   <span class="function">classkit\_method\_redefine</span>
-   <span class="function">classkit\_method\_remove</span>
-   <span class="function">classkit\_method\_rename</span>
-   <span class="function">create\_function</span>

classkit\_method\_copy
======================

Copies a method from class to another

### 说明

<span class="type">bool</span> <span
class="methodname">classkit\_method\_copy</span> ( <span
class="methodparam"><span class="type">string</span> `$dClass`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dMethod`</span> , <span class="methodparam"><span
class="type">string</span> `$sClass`</span> \[, <span
class="methodparam"><span class="type">string</span> `$sMethod`</span>
\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

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

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">classkit\_method\_copy</span>
example**

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
classkit_method_copy('Bar', 'baz', 'Foo', 'example');

// output copied function
echo Bar::baz();
?>
```

以上例程会输出：

    foo!

### 参见

-   <span class="function">classkit\_method\_add</span>
-   <span class="function">classkit\_method\_redefine</span>
-   <span class="function">classkit\_method\_remove</span>
-   <span class="function">classkit\_method\_rename</span>

classkit\_method\_redefine
==========================

Dynamically changes the code of the given method

### 说明

<span class="type">bool</span> <span
class="methodname">classkit\_method\_redefine</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> , <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = CLASSKIT\_ACC\_PUBLIC</span></span> \] )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`classname`  
The class in which to redefine the method

`methodname`  
The name of the method to redefine

`args`  
Comma-delimited list of arguments for the redefined method

`code`  
The new code to be evaluated when `methodname` is called

`flags`  
The redefined method can be **`CLASSKIT_ACC_PUBLIC`**,
**`CLASSKIT_ACC_PROTECTED`** or **`CLASSKIT_ACC_PRIVATE`**

> **Note**:
>
> This parameter is only used as of PHP 5, because, prior to this, all
> methods were public.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">classkit\_method\_redefine</span>
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
classkit_method_redefine(
    'Example',
    'foo',
    '',
    'return "bar!\n";',
    CLASSKIT_ACC_PUBLIC
);

// output Example::foo() (after redefine)
echo "After: " . $e->foo();
?>
```

以上例程会输出：

    Before: foo!
    After: bar!

### 参见

-   <span class="function">classkit\_method\_add</span>
-   <span class="function">classkit\_method\_copy</span>
-   <span class="function">classkit\_method\_remove</span>
-   <span class="function">classkit\_method\_rename</span>

classkit\_method\_remove
========================

Dynamically removes the given method

### 说明

<span class="type">bool</span> <span
class="methodname">classkit\_method\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`classname`  
The class in which to remove the method

`methodname`  
The name of the method to remove

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">classkit\_method\_remove</span>
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
classkit_method_remove(
    'Example',
    'foo'
);

echo implode(' ', get_class_methods('Example'));

?>
```

以上例程会输出：

    bar

### 参见

-   <span class="function">classkit\_method\_add</span>
-   <span class="function">classkit\_method\_copy</span>
-   <span class="function">classkit\_method\_redefine</span>
-   <span class="function">classkit\_method\_rename</span>

classkit\_method\_rename
========================

Dynamically changes the name of the given method

### 说明

<span class="type">bool</span> <span
class="methodname">classkit\_method\_rename</span> ( <span
class="methodparam"><span class="type">string</span> `$classname`</span>
, <span class="methodparam"><span class="type">string</span>
`$methodname`</span> , <span class="methodparam"><span
class="type">string</span> `$newname`</span> )

> **Note**: <span
> class="simpara">此函数不能用来操作当前正常运行（或运行链上）的方法。</span>

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担 。

### 参数

`classname`  
The class in which to rename the method

`methodname`  
The name of the method to rename

`newname`  
The new name to give to the renamed method

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">classkit\_method\_rename</span>
example**

``` php
<?php
class Example {
    function foo() {
        return "foo!\n";
    }
}

// Rename the 'foo' method to 'bar'
classkit_method_rename(
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

-   <span class="function">classkit\_method\_add</span>
-   <span class="function">classkit\_method\_copy</span>
-   <span class="function">classkit\_method\_redefine</span>
-   <span class="function">classkit\_method\_remove</span>

**目录**

-   [classkit\_import](/ref/classkit.html#classkit_import) — Import new
    class method definitions from a file
-   [classkit\_method\_add](/ref/classkit.html#classkit_method_add) —
    Dynamically adds a new method to a given class
-   [classkit\_method\_copy](/ref/classkit.html#classkit_method_copy) —
    Copies a method from class to another
-   [classkit\_method\_redefine](/ref/classkit.html#classkit_method_redefine)
    — Dynamically changes the code of the given method
-   [classkit\_method\_remove](/ref/classkit.html#classkit_method_remove)
    — Dynamically removes the given method
-   [classkit\_method\_rename](/ref/classkit.html#classkit_method_rename)
    — Dynamically changes the name of the given method
