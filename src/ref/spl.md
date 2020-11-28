class\_implements
=================

返回指定的类实现的所有接口。

### 说明

<span class="type">array</span> <span
class="methodname">class\_implements</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$autoload`</span> \] )

本函数返回一个数组，该数组中包含了指定类`class`及其父类所实现的所有接口的名称。

### 参数

`class`  
对象（类实例）或字符串（类名称）。

`autoload`  
是否允许使用<a href="/language/oop5/autoload.html" class="link">__autoload</a>
魔术函数来自动装载该类。默认值为**`TRUE`**。

### 返回值

调用成功则返回一个数组，否则返回**`FALSE`**。

### 更新日志

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 5.1.0 | 增加了允许参数`class`为字符串的选项。增加了`autoload`参数。 |

### 范例

**示例 \#1 <span class="function">class\_implements</span> example**

``` php
<?php

interface foo { }
class bar implements foo {}

print_r(class_implements(new bar));

// since PHP 5.1.0 you may also specify the parameter as a string
print_r(class_implements('bar'));


function __autoload($class_name) {
   require_once $class_name . '.php';
}

// use __autoload to load the 'not_loaded' class
print_r(class_implements('not_loaded', true));

?>
```

以上例程的输出类似于：

    Array
    (
        [foo] => foo
    )

    Array
    (
        [interface_of_not_loaded] => interface_of_not_loaded
    )

### 参见

-   <span class="function">class\_parents</span>
-   <span class="function">get\_declared\_interfaces</span>

class\_parents
==============

返回指定类的父类。

### 说明

<span class="type">array</span> <span
class="methodname">class\_parents</span> ( <span
class="methodparam"><span class="type">mixed</span> `$class`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$autoload`</span> \] )

本函数返回一个包含了指定类`class`父类名称的数组。

### 参数

`class`  
对象（类实例）或字符串（类名称）。

`autoload`  
是否允许使用<a href="/language/oop5/autoload.html" class="link">__autoload</a>
魔术函数来自动装载该类。默认值为**`TRUE`**。

### 返回值

调用成功则返回一个数组，否则返回**`FALSE`**。

### 更新日志

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 5.1.0 | 增加了允许参数`class`为字符串的选项。增加了`autoload`参数。 |

### 范例

**示例 \#1 <span class="function">class\_parents</span> example**

``` php
<?php

class foo { }
class bar extends foo {}

print_r(class_parents(new bar));

// since PHP 5.1.0 you may also specify the parameter as a string
print_r(class_parents('bar'));


function __autoload($class_name) {
   require_once $class_name . '.php';
}

// use __autoload to load the 'not_loaded' class
print_r(class_parents('not_loaded', true));
?>
```

以上例程的输出类似于：

    Array
    (
        [foo] => foo
    )

    Array
    (
        [parent_of_not_loaded] => parent_of_not_loaded
    )

### 参见

-   <span class="function">class\_implements</span>

class\_uses
===========

Return the traits used by the given class

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">class\_uses</span> ( <span class="methodparam"><span
class="type">mixed</span> `$class`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$autoload`<span
class="initializer"> = **`TRUE`**</span></span> \] )

This function returns an array with the names of the traits that the
given `class` uses. This does however not include any traits used by a
parent class.

### 参数

`class`  
An object (class instance) or a string (class name).

`autoload`  
Whether to allow this function to load the class automatically through
the <span class="function">\_\_autoload</span> magic method.

### 返回值

An array on success, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">class\_uses</span> example**

``` php
<?php

trait foo { }
class bar {
  use foo;
}

print_r(class_uses(new bar));

print_r(class_uses('bar'));

function __autoload($class_name) {
   require_once $class_name . '.php';
}

// use __autoload to load the 'not_loaded' class
print_r(class_uses('not_loaded', true));

?>
```

以上例程的输出类似于：

    Array
    (
        [foo] => foo
    )

    Array
    (
        [foo] => foo
    )

    Array
    (
        [trait_of_not_loaded] => trait_of_not_loaded
    )

### 参见

-   <span class="function">class\_parents</span>
-   <span class="function">get\_declared\_traits</span>

iterator\_apply
===============

为迭代器中每个元素调用一个用户自定义函数

### 说明

<span class="type">int</span> <span
class="methodname">iterator\_apply</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> , <span class="methodparam"><span
class="type">callable</span> `$function`</span> \[, <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

循环迭代每个元素时调用某一回调函数。

### 参数

`iterator`  
需要循环迭代的类对象。

`function`  
迭代到每个元素时的调用的回调函数。

> **Note**: <span class="simpara"> 为了遍历 `iterator` 这个函数必须返回
> **`TRUE`**。 </span>

`args`  
传递到回调函数的参数。

### 返回值

返回已迭代的元素个数。

### 范例

**示例 \#1 <span class="function">iterator\_apply</span> example**

``` php
<?php
function print_caps(Iterator $iterator) {
    echo strtoupper($iterator->current()) . "\n";
    return TRUE;
}

$it = new ArrayIterator(array("Apples", "Bananas", "Cherries"));
iterator_apply($it, "print_caps", array($it));
?>
```

以上例程会输出：

    APPLES
    BANANAS
    CHERRIES

### 参见

-   <span class="function">array\_walk</span>

iterator\_count
===============

计算迭代器中元素的个数

### 说明

<span class="type">int</span> <span
class="methodname">iterator\_count</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> )

计算迭代器中的元素个数。

### 参数

`iterator`  
要计数的迭代器。

### 返回值

迭代器`iterator`中的元素个数。

### 范例

**示例 \#1 <span class="function">iterator\_count</span> example**

``` php
<?php
$iterator = new ArrayIterator(array('recipe'=>'pancakes', 'egg', 'milk', 'flour'));
var_dump(iterator_count($iterator));
?>
```

以上例程会输出：

    int(4)

iterator\_to\_array
===================

将迭代器中的元素拷贝到数组

### 说明

<span class="type">array</span> <span
class="methodname">iterator\_to\_array</span> ( <span
class="methodparam"><span class="type">Traversable</span>
`$iterator`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$use_keys`<span class="initializer"> =
true</span></span> \] )

将迭代器中的元素拷贝到数组。

### 参数

`iterator`  
被拷贝的迭代器。

`use_keys`  
是否使用迭代器元素键作为索引。

### 返回值

一个数组，包含迭代器中的元素。

### 更新日志

| 版本  | 说明                     |
|-------|--------------------------|
| 5.2.1 | 添加了 `use_keys` 参数。 |

### 范例

**示例 \#1 <span class="function">iterator\_to\_array</span> example**

``` php
<?php
$iterator = new ArrayIterator(array('recipe'=>'pancakes', 'egg', 'milk', 'flour'));
var_dump(iterator_to_array($iterator, true));
var_dump(iterator_to_array($iterator, false));
?>
```

以上例程会输出：

    array(4) {
      ["recipe"]=>
      string(8) "pancakes"
      [0]=>
      string(3) "egg"
      [1]=>
      string(4) "milk"
      [2]=>
      string(5) "flour"
    }
    array(4) {
      [0]=>
      string(8) "pancakes"
      [1]=>
      string(3) "egg"
      [2]=>
      string(4) "milk"
      [3]=>
      string(5) "flour"
    }

spl\_autoload\_call
===================

尝试调用所有已注册的 \_\_autoload() 函数来装载请求类

### 说明

<span class="type">void</span> <span
class="methodname">spl\_autoload\_call</span> ( <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> )

可以直接在程序中手动调用此函数来使用所有已注册的 \_\_autoload
函数装载类或接口。

### 参数

`class_name`  
搜索的类名。

### 返回值

没有返回值。

spl\_autoload\_extensions
=========================

注册并返回 spl\_autoload 函数使用的默认文件扩展名

### 说明

<span class="type">string</span> <span
class="methodname">spl\_autoload\_extensions</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$file_extensions`</span> \] )

本函数用来修改和检查 <span class="function">\_\_autoload</span>
函数内置的默认实现函数 <span class="function">spl\_autoload</span>
所使用的扩展名。

> **Note**: <span class="simpara"> 在定义的文件扩展名之间不应该有空格。
> </span>

### 参数

`file_extensions`  
当不使用任何参数调用此函数时，它返回当前的文件扩展名的列表，不同的扩展名用逗号分隔。要修改文件扩展名列表，用一个逗号分隔的新的扩展名列表字符串来调用本函数即可。中文注：默认的
spl\_autoload 函数使用的扩展名是 ".inc,.php"。

### 返回值

逗号分隔的 <span class="function">spl\_autoload</span>
函数的默认文件扩展名。

### 范例

**示例 \#1 <span class="function">spl\_autoload\_extensions</span>
示例**

``` php
<?php
spl_autoload_extensions(".php,.inc");
?>
```

spl\_autoload\_functions
========================

返回所有已注册的 \_\_autoload() 函数

### 说明

<span class="type">array</span> <span
class="methodname">spl\_autoload\_functions</span> ( <span
class="methodparam">void</span> )

获取所有已注册的 \_\_autoload() 函数。

### 参数

此函数没有参数。

### 返回值

包含所有已注册的 \_\_autoload 函数的数组（<span
class="type">array</span>）。如果自动装载函数队列未激活，则返回
**`FALSE`**。如果没有已注册的函数，则返回一个空数组。

spl\_autoload\_register
=======================

注册给定的函数作为 \_\_autoload 的实现

### 说明

<span class="type">bool</span> <span
class="methodname">spl\_autoload\_register</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$autoload_function`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$throw`<span class="initializer"> =
true</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$prepend`<span class="initializer"> =
false</span></span> \]\]\] )

将函数注册到SPL
\_\_autoload函数队列中。如果该队列中的函数尚未激活，则激活它们。

如果在你的程序中已经实现了<span
class="function">\_\_autoload</span>函数，它必须显式注册到<span
class="function">\_\_autoload</span>队列中。因为 <span
class="function">spl\_autoload\_register</span>函数会将Zend
Engine中的<span class="function">\_\_autoload</span>函数取代为<span
class="function">spl\_autoload</span>或<span
class="function">spl\_autoload\_call</span>。

如果需要多条 autoload 函数，<span
class="function">spl\_autoload\_register</span> 满足了此类需求。
它实际上创建了 autoload 函数的队列，按定义时的顺序逐个执行。相比之下，
<span class="function">\_\_autoload</span> 只可以定义一次。

### 参数

`autoload_function`  
欲注册的自动装载函数。如果没有提供任何参数，则自动注册 autoload
的默认实现函数<span class="function">spl\_autoload</span>。

`throw`  
此参数设置了 `autoload_function` 无法成功注册时， <span
class="function">spl\_autoload\_register</span>是否抛出异常。

`prepend`  
如果是 true，<span class="function">spl\_autoload\_register</span>
会添加函数到队列之首，而不是队列尾部。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 5.3.0 | 引入了命名空间的支持。  |
| 5.3.0 | 添加了 `prepend` 参数。 |

### 范例

**示例 \#1 <span class="function">spl\_autoload\_register</span> 作为
<span class="function">\_\_autoload</span> 函数的替代**

``` php
<?php

// function __autoload($class) {
//     include 'classes/' . $class . '.class.php';
// }

function my_autoloader($class) {
    include 'classes/' . $class . '.class.php';
}

spl_autoload_register('my_autoloader');

// 或者，自 PHP 5.3.0 起可以使用一个匿名函数
spl_autoload_register(function ($class) {
    include 'classes/' . $class . '.class.php';
});

?>
```

**示例 \#2 class 未能加载的 <span
class="function">spl\_autoload\_register</span> 例子**

``` php
<?php

namespace Foobar;

class Foo {
    static public function test($name) {
        print '[['. $name .']]';
    }
}

spl_autoload_register(__NAMESPACE__ .'\Foo::test'); // 自 PHP 5.3.0 起

new InexistentClass;

?>
```

以上例程的输出类似于：

    [[Foobar\InexistentClass]]
    Fatal error: Class 'Foobar\InexistentClass' not found in ...

### 参见

-   <span class="function">\_\_autoload</span>

spl\_autoload\_unregister
=========================

注销已注册的 \_\_autoload() 函数

### 说明

<span class="type">bool</span> <span
class="methodname">spl\_autoload\_unregister</span> ( <span
class="methodparam"><span class="type">mixed</span>
`$autoload_function`</span> )

从 autoload
自动装载函数队列中移除指定的函数。如果该函数队列处于激活状态，并且在给定函数注销后该队列变为空，则该函数队列将会变为无效。

如果该函数注销后使得自动装载函数队列无效，即使存在有 \_\_autoload
函数它也不会自动激活。

### 参数

`autoload_function`  
要注销的自动装载函数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

spl\_autoload
=============

\_\_autoload()函数的默认实现

### 说明

<span class="type">void</span> <span
class="methodname">spl\_autoload</span> ( <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$file_extensions`</span> \] )

本函数提供了\_\_autoload()的一个默认实现。如果不使用任何参数调用
spl\_autoload\_register() 函数，则以后在进行 \_\_autoload()
调用时会自动使用此函数。

### 参数

`class_name`  

`file_extensions`  
在默认情况下，本函数先将类名转换成小写，再在小写的类名后加上 .inc 或
.php 的扩展名作为文件名，然后在所有的包含路径(include
paths)中检查是否存在该文件。

### 返回值

没有返回值。

spl\_classes
============

返回所有可用的SPL类

### 说明

<span class="type">array</span> <span
class="methodname">spl\_classes</span> ( <span
class="methodparam">void</span> )

本函数返回当前所有可用的 SPL 类的数组。

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">array</span> containing the currently
available SPL classes.

### 范例

**示例 \#1 <span class="function">spl\_classes</span> example**

``` php
<?php

print_r(spl_classes());

?>
```

以上例程的输出类似于：

    Array
    (
        [ArrayObject] => ArrayObject
        [ArrayIterator] => ArrayIterator
        [CachingIterator] => CachingIterator
        [RecursiveCachingIterator] => RecursiveCachingIterator
        [DirectoryIterator] => DirectoryIterator
        [FilterIterator] => FilterIterator
        [LimitIterator] => LimitIterator
        [ParentIterator] => ParentIterator
        [RecursiveDirectoryIterator] => RecursiveDirectoryIterator
        [RecursiveIterator] => RecursiveIterator
        [RecursiveIteratorIterator] => RecursiveIteratorIterator
        [SeekableIterator] => SeekableIterator
        [SimpleXMLIterator] => SimpleXMLIterator
    )

spl\_object\_hash
=================

返回指定对象的hash id

### 说明

<span class="type">string</span> <span
class="methodname">spl\_object\_hash</span> ( <span
class="methodparam"><span class="type">object</span> `$obj`</span> )

本函数为指定对象返回一个唯一标识符。这个标识符可用于作为保存对象或区分不同对象的hash
key。

### 参数

`object`  
Any object.

### 返回值

字符串，对于每个对象它都是唯一的，并且对同一个对象它总是相同。

### 范例

**示例 \#1 A <span class="function">spl\_object\_hash</span> example**

``` php
<?php
$id = spl_object_hash($object);
$storage[$id] = $object;
?>
```

### 注释

> **Note**:
>
> When an object is destroyed, its hash may be reused for other objects.

spl\_object\_id
===============

Return the integer object handle for given object

### 说明

<span class="type">int</span> <span
class="methodname">spl\_object\_id</span> ( <span
class="methodparam"><span class="type">object</span> `$obj`</span> )

This function returns a unique identifier for the object. The object id
is unique for the lifetime of the object. Once the object is destroyed,
its id may be reused for other objects. This behavior is similar to
<span class="function">spl\_object\_hash</span>.

### 参数

`object`  
Any object.

### 返回值

An integer identifier that is unique for each currently existing object
and is always the same for each object.

### 范例

**示例 \#1 A <span class="function">spl\_object\_id</span> example**

``` php
<?php
$id = spl_object_id($object);
$storage[$id] = $object;
?>
```

### 注释

> **Note**:
>
> When an object is destroyed, its id may be reused for other objects.

**目录**

-   [class\_implements](/ref/spl.html#class_implements) —
    返回指定的类实现的所有接口。
-   [class\_parents](/ref/spl.html#class_parents) — 返回指定类的父类。
-   [class\_uses](/ref/spl.html#class_uses) — Return the traits used by
    the given class
-   [iterator\_apply](/ref/spl.html#iterator_apply) —
    为迭代器中每个元素调用一个用户自定义函数
-   [iterator\_count](/ref/spl.html#iterator_count) —
    计算迭代器中元素的个数
-   [iterator\_to\_array](/ref/spl.html#iterator_to_array) —
    将迭代器中的元素拷贝到数组
-   [spl\_autoload\_call](/ref/spl.html#spl_autoload_call) —
    尝试调用所有已注册的 \_\_autoload() 函数来装载请求类
-   [spl\_autoload\_extensions](/ref/spl.html#spl_autoload_extensions) —
    注册并返回 spl\_autoload 函数使用的默认文件扩展名
-   [spl\_autoload\_functions](/ref/spl.html#spl_autoload_functions) —
    返回所有已注册的 \_\_autoload() 函数
-   [spl\_autoload\_register](/ref/spl.html#spl_autoload_register) —
    注册给定的函数作为 \_\_autoload 的实现
-   [spl\_autoload\_unregister](/ref/spl.html#spl_autoload_unregister) —
    注销已注册的 \_\_autoload() 函数
-   [spl\_autoload](/ref/spl.html#spl_autoload) —
    \_\_autoload()函数的默认实现
-   [spl\_classes](/ref/spl.html#spl_classes) — 返回所有可用的SPL类
-   [spl\_object\_hash](/ref/spl.html#spl_object_hash) —
    返回指定对象的hash id
-   [spl\_object\_id](/ref/spl.html#spl_object_id) — Return the integer
    object handle for given object
