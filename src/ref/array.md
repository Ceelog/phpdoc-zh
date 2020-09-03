参考 <span class="function">is\_array</span>, <span
class="function">explode</span>, <span class="function">implode</span>,
<span class="function">split</span>, <span
class="function">preg\_split</span>, and <span
class="function">unset</span>.

array\_change\_key\_case
========================

将数组中的所有键名修改为全大写或小写

### 说明

<span class="type">array</span> <span
class="methodname">array\_change\_key\_case</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> \[,
<span class="methodparam"><span class="type">int</span> `$case`<span
class="initializer"> = CASE\_LOWER</span></span> \] )

<span class="function">array\_change\_key\_case</span> 将 `array`
数组中的所有键名改为全小写或大写。本函数不改变数字索引。

### 参数

`array`  
需要操作的数组。

`case`  
可以在这里用两个常量，**`CASE_UPPER`** 或 **`CASE_LOWER`**（默认值）。

### 返回值

返回一个键全是小写或者全是大写的数组；如果输入值（`array`）不是一个数组，那么返回**`FALSE`**

### 错误／异常

如果输入值（`array`）不是一个数组，就会抛出一个错误警告（**`E_WARNING`**）。

### 范例

**示例 \#1 <span class="function">array\_change\_key\_case</span>例一**

``` php
<?php
$input_array = array("FirSt" => 1, "SecOnd" => 4);
print_r(array_change_key_case($input_array, CASE_UPPER));
?>
```

以上例程会输出：

    Array
    (
        [FIRST] => 1
        [SECOND] => 4
    )

### 注释

> **Note**:
>
> 如果一个数组中的多个键名经过本函数后变成一样的话（例如 "*keY*" 和
> "*kEY*"），最后一个值将覆盖其它的值。

array\_chunk
============

将一个数组分割成多个

### 说明

<span class="type">array</span> <span
class="methodname">array\_chunk</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> , <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$preserve_keys`<span class="initializer"> = false</span></span> \] )

将一个数组分割成多个数组，其中每个数组的单元数目由 `size`
决定。最后一个数组的单元数目可能会少于 `size` 个。

### 参数

`array`  
需要操作的数组

`size`  
每个数组的单元数目

`preserve_keys`  
设为 **`TRUE`**，可以使 PHP 保留输入数组中原来的键名。如果你指定了
**`FALSE`**，那每个结果数组将用从零开始的新数字索引。默认值是
**`FALSE`**。

### 返回值

得到的数组是一个多维数组中的单元，其索引从零开始，每一维包含了 `size`
个元素。

### 错误／异常

如果 `size` 小于 1，会抛出一个 **`E_WARNING`** 错误并返回 **`NULL`**。

### 范例

**示例 \#1 <span class="function">array\_chunk</span> 例子**

``` php
<?php
$input_array = array('a', 'b', 'c', 'd', 'e');
print_r(array_chunk($input_array, 2));
print_r(array_chunk($input_array, 2, true));
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [0] => a
                [1] => b
            )

        [1] => Array
            (
                [0] => c
                [1] => d
            )

        [2] => Array
            (
                [0] => e
            )

    )
    Array
    (
        [0] => Array
            (
                [0] => a
                [1] => b
            )

        [1] => Array
            (
                [2] => c
                [3] => d
            )

        [2] => Array
            (
                [4] => e
            )

    )

### 参见

-   <span class="function">array\_slice</span>

array\_column
=============

返回数组中指定的一列

### 说明

<span class="type">array</span> <span
class="methodname">array\_column</span> ( <span
class="methodparam"><span class="type">array</span> `$input`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$column_key`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$index_key`<span class="initializer"> =
null</span></span> \] )

<span class="function">array\_column</span>
返回`input`数组中键值为`column_key`的列，
如果指定了可选参数`index_key`，那么`input`数组中的这一列的值将作为返回数组中对应值的键。

### 参数

`input`  
需要取出数组列的多维数组。 如果提供的是包含一组对象的数组，只有 public
属性会被直接取出。 为了也能取出 private 和 protected 属性，类必须实现
<span class="function">\_\_get</span> 和 <span
class="function">\_\_isset</span> 魔术方法。

`column_key`  
需要返回值的列，它可以是索引数组的列索引，或者是关联数组的列的键，也可以是属性名。
也可以是**`NULL`**，此时将返回整个数组（配合`index_key`参数来重置数组键的时候，非常管用）

`index_key`  
作为返回数组的索引/键的列，它可以是该列的整数索引，或者字符串键值。

### 返回值

从多维数组中返回单列数组。

### 更新日志

| 版本  | 说明                                   |
|-------|----------------------------------------|
| 7.0.0 | `input` 参数现在可以是包含对象的数组。 |

### 范例

**示例 \#1 从结果集中取出first names列**

``` php
<?php
// Array representing a possible record set returned from a database
$records = array(
    array(
        'id' => 2135,
        'first_name' => 'John',
        'last_name' => 'Doe',
    ),
    array(
        'id' => 3245,
        'first_name' => 'Sally',
        'last_name' => 'Smith',
    ),
    array(
        'id' => 5342,
        'first_name' => 'Jane',
        'last_name' => 'Jones',
    ),
    array(
        'id' => 5623,
        'first_name' => 'Peter',
        'last_name' => 'Doe',
    )
);
 
$first_names = array_column($records, 'first_name');
print_r($first_names);
?>
```

以上例程会输出：

    Array
    (
        [0] => John
        [1] => Sally
        [2] => Jane
        [3] => Peter
    )

**示例 \#2 从结果集中总取出last names列，用相应的id作为键值**

``` php
<?php
// Using the $records array from Example #1
$last_names = array_column($records, 'last_name', 'id');
print_r($last_names);
?>
```

以上例程会输出：

    Array
    (
        [2135] => Doe
        [3245] => Smith
        [5342] => Jones
        [5623] => Doe
    )

**示例 \#3 username 列是从对象获取 public 的 "username" 属性**

``` php
<?php

class User
{
    public $username;

    public function __construct(string $username)
    {
        $this->username = $username;
    }
}

$users = [
    new User('user 1'),
    new User('user 2'),
    new User('user 3'),
];

print_r(array_column($users, 'username'));
?>
```

以上例程会输出：

    Array
    (
        [0] => user 1
        [1] => user 2
        [2] => user 3
    )

**示例 \#4 获取 username 列，从对象通过魔术方法 <span
class="function">\_\_get</span> 获取 private 的 "username" 属性。**

``` php
<?php

class Person
{
    private $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    public function __get($prop)
    {
        return $this->$prop;
    }

    public function __isset($prop) : bool
    {
        return isset($this->$prop);
    }
}

$people = [
    new Person('Fred'),
    new Person('Jane'),
    new Person('John'),
];

print_r(array_column($people, 'name'));
?>
```

以上例程会输出：

    Array
    (
        [0] => Fred
        [1] => Jane
        [2] => John
    )

如果不提供<span class="function">\_\_isset</span>，会返回空数组。

### 参见

-   <a href="https://github.com/ramsey/array_column/blob/master/src/array_column.php" class="link external">» Recommended userland implementation for PHP lower than 5.5</a>

array\_combine
==============

创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值

### 说明

<span class="type">array</span> <span
class="methodname">array\_combine</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> ,
<span class="methodparam"><span class="type">array</span>
`$values`</span> )

返回一个 <span class="type">array</span>，用来自 `keys`
数组的值作为键名，来自 `values` 数组的值作为相应的值。

### 参数

`keys`  
将被作为新数组的键。非法的值将会被转换为字符串类型（<span
class="type">string</span>）。

`values`  
将被作为 <span class="type">Array</span> 的值。

### 返回值

返回合并的 <span
class="type">array</span>，如果两个数组的单元数不同则返回 **`FALSE`**。

### 错误／异常

如果作为`keys`的数组和作为`values`的数组的元素个数不一样，将会抛出一个警告错误（**`E_WARNING`**）。

### 更新日志

| 版本  | 说明                                                                       |
|-------|----------------------------------------------------------------------------|
| 5.4.0 | （修复）早期版本中如果是空数组就报**`E_WARNING`**的错并且返回**`FALSE`**。 |

### 范例

**示例 \#1 一个 <span class="function">array\_combine</span>
简单的例子**

``` php
<?php
$a = array('green', 'red', 'yellow');
$b = array('avocado', 'apple', 'banana');
$c = array_combine($a, $b);

print_r($c);
?>
```

以上例程会输出：

    Array
    (
        [green]  => avocado
        [red]    => apple
        [yellow] => banana
    )

### 参见

-   <span class="function">array\_merge</span>
-   <span class="function">array\_walk</span>
-   <span class="function">array\_values</span>

array\_count\_values
====================

统计数组中所有的值

### 说明

<span class="type">array</span> <span
class="methodname">array\_count\_values</span> ( <span
class="methodparam"><span class="type">array</span> `$array` </span> )

<span class="function">array\_count\_values</span> 返回一个数组：
数组的键是 `array` 里单元的值； 数组的值是 `array` 单元的值出现的次数。

### 参数

`input`  
统计这个数组的值

### 返回值

返回一个关联数组，用 `array`
数组中的值作为键名，该值在数组中出现的次数作为值。

### 错误／异常

对数组里面的每个不是 <span class="type">string</span> 和 <span
class="type">integer</span>
类型的元素抛出一个警告错误（**`E_WARNING`**）。

### 范例

**示例 \#1 <span class="function">array\_count\_values</span> 例子**

``` php
<?php
$array = array(1, "hello", 1, "world", "hello");
print_r(array_count_values($array));
?>
```

以上例程会输出：

    Array
    (
        [1] => 2
        [hello] => 2
        [world] => 1
    )

### 参见

-   <span class="function">count</span>
-   <span class="function">array\_unique</span>
-   <span class="function">array\_values</span>
-   <span class="function">count\_chars</span>

array\_diff\_assoc
==================

带索引检查计算数组的差集

### 说明

<span class="type">array</span> <span
class="methodname">array\_diff\_assoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \] )

<span class="function">array\_diff\_assoc</span>
返回一个数组，该数组包括了所有在 `array1`
中但是不在任何其它参数数组中的值。注意和 <span
class="function">array\_diff</span> 不同的是键名也用于比较。

### 参数

`array1`  
从这个数组进行比较

`array2`  
被比较的数组

`...`  
更多被比较的数组

### 返回值

Returns an <span class="type">array</span> containing all the values
from `array1` that are not present in any of the other arrays.

### 范例

**示例 \#1 <span class="function">array\_diff\_assoc</span> 例子**

上面的例子中可以看到键值对 *"a" =\> "green"*
在两个数组中都有，因此不在本函数的输出中。与此不同，键值对 *0 =\> "red"*
出现在输出中是因为第二个参数中的 *"red"* 的键名是 *1*。

``` php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");
$result = array_diff_assoc($array1, $array2);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [b] => brown
        [c] => blue
        [0] => red
    )

**示例 \#2 <span class="function">array\_diff\_assoc</span> example**

键值对 *key =\> value* 中的两个值仅在 *(string) $elem1 === (string)
$elem2* 时被认为相等。也就是说使用了严格检查，字符串的表达必须相同。

``` php
<?php
$array1 = array(0, 1, 2);
$array2 = array("00", "01", "2");
$result = array_diff_assoc($array1, $array2);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [0] => 0
        [1] => 1
        )

### 注释

> **Note**: <span class="simpara">
> 注意本函数只检查了多维数组中的一维。当然可以用
> *array\_diff\_assoc($array1\[0\], $array2\[0\]);* 检查更深的维度。
> </span>

> **Note**: <span class="simpara">
> 使用更多的键比较相似数组时，确保你传入参数的顺序是正确的。
> 新的数组应该是在列表里的第一个。 </span>

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>

array\_diff\_key
================

使用键名比较计算数组的差集

### 说明

<span class="type">array</span> <span
class="methodname">array\_diff\_key</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \] )

根据 `array1` 中的键名和 `array2` 进行比较，返回不同键名的项。 本函数和
<span class="function">array\_diff</span>
相同只除了比较是根据键名而不是值来进行的。

### 参数

`array1`  
从这个数组进行比较

`array2`  
针对此数组进行比较

`...`  
更多比较数组

### 返回值

<span class="function">array\_diff\_key</span>
返回一个数组，该数组包括了所有出现在 `array1`
中但是未出现在任何其它参数数组中的键名的值。

### 范例

**示例 \#1 <span class="function">array\_diff\_key</span> 例**

在 *key =\> value* 对中的两个键名仅在 *(string) $key1 === (string)
$key2*
时被认为相等。换句话说，执行的是严格类型检查，因此字符串的表达必须完全一样。

``` php
<?php
$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_diff_key($array1, $array2));
?>
```

以上例程会输出：

    array(2) {
      ["red"]=>
      int(2)
      ["purple"]=>
      int(4)
    }

### 注释

> **Note**:
>
> 注意本函数只检查了多维数组中的一维。当然，可以用
> *array\_diff\_key($array1\[0\], $array2\[0\]);* 来检查更深的维度。

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_diff\_ukey</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_intersect\_key</span>
-   <span class="function">array\_intersect\_ukey</span>

array\_diff\_uassoc
===================

用用户提供的回调函数做索引检查来计算数组的差集

### 说明

<span class="type">array</span> <span
class="methodname">array\_diff\_uassoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$key_compare_func`</span> )

对比了 `array1` 和 `array2` 并返回不同之处。 注意和 <span
class="function">array\_diff</span> 不同的是键名也用于比较。

和 <span class="function">array\_diff\_assoc</span>
不同的是使用了用户自定义的回调函数，而不是内置的函数。

### 参数

`array1`  
待比较的数组

`array2`  
和这个数组进行比较

`...`  
更多比较的数组

`key_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

返回一个 <span class="type">array</span>，该数组包括了所有在 `array1`
中但是不在任何其它参数数组中的值。

### 范例

**示例 \#1 <span class="function">array\_diff\_uassoc</span> 例子**

上面的例子中 *"a" =\> "green"*
出现在两个数组中因此不在函数的输出中。但是 *0 =\> "red"*
却在输出中，因为第二个参数中的 *"red"* 的键名是 *1*。

``` php
<?php
function key_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b)? 1:-1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");
$result = array_diff_uassoc($array1, $array2, "key_compare_func");
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [b] => brown
        [c] => blue
        [0] => red
    )

The equality of 2 indices is checked by the user supplied callback
function.

### 注释

> **Note**:
>
> 注意本函数只检查了多维数组中的一维。当然可以用
> *array\_diff\_uassoc($array1\[0\], $array2\[0\],
> "key\_compare\_func");* 检查更深的维度。

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_uintersect</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>

array\_diff\_ukey
=================

用回调函数对键名比较计算数组的差集

### 说明

<span class="type">array</span> <span
class="methodname">array\_diff\_ukey</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$key_compare_func`</span> )

<span class="function">array\_diff\_ukey</span>
返回一个数组，该数组包括了所有出现在 `array1`
中但是未出现在任何其它参数数组中的键名的值。注意关联关系保留不变。本函数和
<span class="function">array\_diff</span>
相同只除了比较是根据键名而不是值来进行的。

此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。

### 参数

`array1`  
The array to compare from

`array2`  
An array to compare against

`...`  
More arrays to compare against

`key_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

Returns an <span class="type">array</span> containing all the entries
from `array1` that are not present in any of the other arrays.

### 范例

**示例 \#1 <span class="function">array\_diff\_ukey</span> 例子**

``` php
<?php
function key_compare_func($key1, $key2)
{
    if ($key1 == $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_diff_ukey($array1, $array2, 'key_compare_func'));
?>
```

以上例程会输出：

    array(2) {
      ["red"]=>
      int(2)
      ["purple"]=>
      int(4)
    }

### 注释

> **Note**:
>
> 注意本函数只检查了多维数组中的一维。当然，可以用
> *array\_diff\_ukey($array1\[0\], $array2\[0\], 'callback\_func');*
> 来检查更深的维度。

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_diff\_key</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_intersect\_key</span>
-   <span class="function">array\_intersect\_ukey</span>

array\_diff
===========

计算数组的差集

### 说明

<span class="type">array</span> <span
class="methodname">array\_diff</span> ( <span class="methodparam"><span
class="type">array</span> `$array1`</span> , <span
class="methodparam"><span class="type">array</span> `$array2`</span> \[,
<span class="methodparam"><span class="type">array</span> `$...`</span>
\] )

对比 `array1` 和其他一个或者多个数组，返回在 `array1` 中但是不在其他
array 里的值。

### 参数

`array1`  
要被对比的数组

`array2`  
和这个数组进行比较

`...`  
更多相比较的数组

### 返回值

返回一个数组，该数组包括了所有在 `array1`
中但是不在任何其它参数数组中的值。注意键名保留不变。

### 范例

**示例 \#1 <span class="function">array\_diff</span> 例子**

``` php
<?php
$array1 = array("a" => "green", "red", "blue", "red");
$array2 = array("b" => "green", "yellow", "red");
$result = array_diff($array1, $array2);

print_r($result);
?>
```

在 `$array1` 中多次出现的值一样处理，输出结果为：

    Array
    (
        [1] => blue
    )

### 注释

> **Note**:
>
> 两个单元仅在 *(string) $elem1 === (string) $elem2*
> 时被认为是相同的。也就是说，当字符串的表达是一样的时候。

> **Note**:
>
> 注意本函数只检查了多维数组中的一维。当然可以用
> *array\_diff($array1\[0\], $array2\[0\]);* 检查更深的维度。

### 参见

-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>

array\_fill\_keys
=================

使用指定的键和值填充数组

### 说明

<span class="type">array</span> <span
class="methodname">array\_fill\_keys</span> ( <span
class="methodparam"><span class="type">array</span> `$keys`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

使用 `value` 参数的值作为值，使用 `keys` 数组的值作为键来填充一个数组。

### 参数

`keys`  
使用该数组的值作为键。非法值将被转换为<span class="type">字符串</span>。

`value`  
填充使用的值。

### 返回值

返回填充后的数组。

### 范例

**示例 \#1 <span class="function">array\_fill\_keys</span> 范例**

``` php
<?php
$keys = array('foo', 5, 10, 'bar');
$a = array_fill_keys($keys, 'banana');
print_r($a);
?>
```

以上例程会输出：

    Array
    (
        [foo] => banana
        [5] => banana
        [10] => banana
        [bar] => banana
    )

### 参见

-   <span class="function">array\_fill</span>
-   <span class="function">array\_combine</span>

array\_fill
===========

用给定的值填充数组

### 说明

<span class="type">array</span> <span
class="methodname">array\_fill</span> ( <span class="methodparam"><span
class="type">int</span> `$start_index`</span> , <span
class="methodparam"><span class="type">int</span> `$num`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="function">array\_fill</span> 用 `value`
参数的值将一个数组填充 `num` 个条目，键名由 `start_index`
参数指定的开始。

### 参数

`start_index`  
返回的数组的第一个索引值。

如果 `start_index` 是负数， 那么返回的数组的第一个索引将会是
`start_index` ，而后面索引则从0开始。 (参见
<a href="/ref/array.html#array_fill%20例子" class="link">例子</a>)。

`num`  
插入元素的数量。 必须大于或等于 0。

`value`  
用来填充的值。

### 返回值

返回填充后的数组。

### 错误／异常

如果 `num` 小于零，将会抛出 **`E_WARNING`**。

### 更新日志

| 版本  | 说明                                         |
|-------|----------------------------------------------|
| 5.6.0 | `num` 现在可以是零。 之前 `num` 必须大于零。 |

### 范例

**示例 \#1 <span class="function">array\_fill</span> 例子**

``` php
<?php
$a = array_fill(5, 6, 'banana');
$b = array_fill(-2, 4, 'pear');
print_r($a);
print_r($b);
?>
```

以上例程会输出：

    Array
    (
        [5]  => banana
        [6]  => banana
        [7]  => banana
        [8]  => banana
        [9]  => banana
        [10] => banana
    )
    Array
    (
        [-2] => pear
        [0] => pear
        [1] => pear
        [2] => pear
    )

### 注释

参见手册上 <a href="/language/types/array.html" class="link">数组</a>
一节里关于负数的键的详细解释。

### 参见

-   <span class="function">array\_fill\_keys</span>
-   <span class="function">str\_repeat</span>
-   <span class="function">range</span>

array\_filter
=============

用回调函数过滤数组中的单元

### 说明

<span class="type">array</span> <span
class="methodname">array\_filter</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> \[,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flag`<span class="initializer"> =
0</span></span> \]\] )

依次将 `array` 数组中的每个值传递到 `callback` 函数。如果 `callback`
函数返回 true，则 `array`
数组的当前值会被包含在返回的结果数组中。数组的键名保留不变。

### 参数

`array`  
要循环的数组

`callback`  
使用的回调函数

如果没有提供 `callback` 函数， 将删除 `array` 中所有等值为 **`FALSE`**
的条目。更多信息见<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">转换为布尔值</a>。

`flag`  
决定`callback`接收的参数形式:

-   <span class="simpara">**`ARRAY_FILTER_USE_KEY`** -
    `callback`接受键名作为的唯一参数</span>
-   <span class="simpara">**`ARRAY_FILTER_USE_BOTH`** -
    `callback`同时接受键名和键值</span>

### 返回值

返回过滤后的数组。

### 更新日志

| 版本  | 说明                                                                                        |
|-------|---------------------------------------------------------------------------------------------|
| 5.6.0 | 添加可选的参数 `flag`，以及常量 **`ARRAY_FILTER_USE_KEY`** 和 **`ARRAY_FILTER_USE_BOTH`**。 |

### 范例

**示例 \#1 <span class="function">array\_filter</span> 例子**

``` php
<?php
function odd($var)
{
    // returns whether the input integer is odd
    return($var & 1);
}

function even($var)
{
    // returns whether the input integer is even
    return(!($var & 1));
}

$array1 = array("a"=>1, "b"=>2, "c"=>3, "d"=>4, "e"=>5);
$array2 = array(6, 7, 8, 9, 10, 11, 12);

echo "Odd :\n";
print_r(array_filter($array1, "odd"));
echo "Even:\n";
print_r(array_filter($array2, "even"));
?>
```

以上例程会输出：

    Odd :
    Array
    (
        [a] => 1
        [c] => 3
        [e] => 5
    )
    Even:
    Array
    (
        [0] => 6
        [2] => 8
        [4] => 10
        [6] => 12
    )

**示例 \#2 不使用 `callback` 时的<span
class="function">array\_filter</span>**

``` php
<?php

$entry = array(
             0 => 'foo',
             1 => false,
             2 => -1,
             3 => null,
             4 => ''
          );

print_r(array_filter($entry));
?>
```

以上例程会输出：

    Array
    (
        [0] => foo
        [2] => -1
    )

**示例 \#3 带 `flag` 标记的 <span
class="function">array\_filter</span>**

``` php
<?php

$arr = ['a' => 1, 'b' => 2, 'c' => 3, 'd' => 4];

var_dump(array_filter($arr, function($k) {
    return $k == 'b';
}, ARRAY_FILTER_USE_KEY));

var_dump(array_filter($arr, function($v, $k) {
    return $k == 'b' || $v == 4;
}, ARRAY_FILTER_USE_BOTH));
?>
```

以上例程会输出：

    array(1) {
      ["b"]=>
      int(2)
    }
    array(2) {
      ["b"]=>
      int(2)
      ["d"]=>
      int(4)
    }

### 注释

**Caution**

用户不应在回调函数中修改数组本身。例如增加／删除单元或者对 <span
class="function">array\_filter</span> 正在作用的数组进行
unset。如果数组改变了，此函数的行为将不可预测。

### 参见

-   <span class="function">array\_map</span>
-   <span class="function">array\_reduce</span>
-   <span class="function">array\_walk</span>

array\_flip
===========

交换数组中的键和值

### 说明

<span class="type">array</span> <span
class="methodname">array\_flip</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> )

<span class="function">array\_flip</span> 返回一个反转后的 <span
class="type">array</span>，例如 `array` 中的键名变成了值，而 `array`
中的值成了键名。

注意 `array` 中的值需要能够作为合法的键名（例如需要是 <span
class="type">integer</span> 或者 <span
class="type">string</span>）。如果类型不对，将出现一个警告，并且有问题的键／值对*将不会出现在结果里*。

如果同一个值出现多次，则最后一个键名将作为它的值，其它键会被丢弃。

### 参数

`array`  
要交换键/值对的数组。

### 返回值

成功时返回交换后的数组，如果失败返回 **`NULL`**。

### 范例

**示例 \#1 <span class="function">array\_flip</span> 例子**

``` php
<?php
$input = array("oranges", "apples", "pears");
$flipped = array_flip($input);

print_r($flipped);
?>
```

以上例程会输出：

    Array
    (
        [oranges] => 0
        [apples] => 1
        [pears] => 2
    )

**示例 \#2 <span class="function">array\_flip</span> 例子 : 冲突**

``` php
<?php
$input = array("a" => 1, "b" => 1, "c" => 2);
$flipped = array_flip($input);

print_r($flipped);
?>
```

以上例程会输出：

    Array
    (
        [1] => b
        [2] => c
    )

### 参见

-   <span class="function">array\_values</span>
-   <span class="function">array\_keys</span>
-   <span class="function">array\_reverse</span>

array\_intersect\_assoc
=======================

带索引检查计算数组的交集

### 说明

<span class="type">array</span> <span
class="methodname">array\_intersect\_assoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \] )

<span class="function">array\_intersect\_assoc</span>
返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。注意和 <span
class="function">array\_intersect</span> 不同的是键名也用于比较。

### 参数

`array1`  
要检查的主值。

`array2`  
要比较的数组。

`...`  
要对比的数组变量的列表。

### 返回值

返回数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。

### 范例

**示例 \#1 <span class="function">array\_intersect\_assoc</span> 例子**

``` php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");
$result_array = array_intersect_assoc($array1, $array2);
print_r($result_array);
?>
```

以上例程会输出：

    Array
    (
        [a] => green
    )

上面例子中可以看到只有键值对 *"a" =\> "green"*
在两个数组中都存在从而被返回。值 *"red"* 没有被返回是因为在 `$array1`
中它的键名是 *0* 而在 `$array2` 中 *"red"* 的键名是 *1*，键 *"b"*
没有返回的原因是它的值和其他数组不同。

键值对 *key =\> value* 中的两个值仅在 *(string) $elem1 === (string)
$elem2* 时被认为相等。也就是说使用了严格检查，字符串的表达必须相同。

### 参见

-   <span class="function">array\_intersect</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>
-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_assoc</span>

array\_intersect\_key
=====================

使用键名比较计算数组的交集

### 说明

<span class="type">array</span> <span
class="methodname">array\_intersect\_key</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \] )

<span class="function">array\_intersect\_key</span>
返回一个数组，该数组包含了所有出现在 `array1`
中并同时出现在所有其它参数数组中的键名的值。

### 参数

`array1`  
The array with master keys to check.

`array2`  
An array to compare keys against.

`...`  
A variable list of arrays to compare.

### 返回值

Returns an associative array containing all the entries of `array1`
which have keys that are present in all arguments.

### 范例

**示例 \#1 <span class="function">array\_intersect\_key</span> 例子**

``` php
<?php
$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_intersect_key($array1, $array2));
?>
```

以上例程会输出：

    array(2) {
      ["blue"]=>
      int(1)
      ["green"]=>
      int(3)
    }

上例中可以看到只有 *'blue'* 和 *'green'*
两个键名出现在两个数组中，因此被返回。此外注意 *'blue'* 和 *'green'*
的值在两个数组中是不同的。但因为只检查键名，因此还是匹配。返回的值只是
`array1` 中的。

在 *key =\> value* 对中的两个键名仅在 *(string) $key1 === (string)
$key2*
时被认为相等。换句话说，执行的是严格类型检查，因此字符串的表达必须完全一样。

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_diff\_key</span>
-   <span class="function">array\_diff\_ukey</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_intersect\_ukey</span>

array\_intersect\_uassoc
========================

带索引检查计算数组的交集，用回调函数比较索引

### 说明

<span class="type">array</span> <span
class="methodname">array\_intersect\_uassoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$key_compare_func`</span> )

<span class="function">array\_intersect\_uassoc</span>
返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。注意和 <span
class="function">array\_intersect</span> 不同的是键名也用于比较。

### 参数

`array1`  
Initial array for comparison of the arrays.

`array2`  
First array to compare keys against.

`...`  
Variable list of array arguments to compare values against.

`key_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

Returns the values of `array1` whose values exist in all of the
arguments.

### 范例

**示例 \#1 <span class="function">array\_intersect\_uassoc</span> 例子**

``` php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_intersect_uassoc($array1, $array2, "strcasecmp"));
?>
```

以上例程会输出：

    Array
    (
        [b] => brown
    )

### 参见

-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>
-   <span class="function">array\_intersect\_key</span>
-   <span class="function">array\_intersect\_ukey</span>

array\_intersect\_ukey
======================

用回调函数比较键名来计算数组的交集

### 说明

<span class="type">array</span> <span
class="methodname">array\_intersect\_ukey</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$key_compare_func`</span> )

<span class="function">array\_intersect\_ukey</span>
返回一个数组，该数组包含了所有出现在 `array1`
中并同时出现在所有其它参数数组中的键名的值。

### 参数

`array1`  
Initial array for comparison of the arrays.

`array2`  
First array to compare keys against.

`...`  
Variable list of array arguments to compare keys against.

`key_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

Returns the values of `array1` whose keys exist in all the arguments.

### 范例

**示例 \#1 <span class="function">array\_intersect\_ukey</span> 例子**

``` php
<?php
function key_compare_func($key1, $key2)
{
    if ($key1 == $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_intersect_ukey($array1, $array2, 'key_compare_func'));
?>
```

以上例程会输出：

    array(2) {
      ["blue"]=>
      int(1)
      ["green"]=>
      int(3)
    }

上例中可以看到只有 *'blue'* 和 *'green'*
两个键名出现在两个数组中，因此被返回。此外注意 *'blue'* 和 *'green'*
的值在两个数组中是不同的。但因为只检查键名，因此还是匹配。返回的值只是
`array1` 中的。

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_diff\_key</span>
-   <span class="function">array\_diff\_ukey</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_intersect\_key</span>

array\_intersect
================

计算数组的交集

### 说明

<span class="type">array</span> <span
class="methodname">array\_intersect</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \] )

<span class="function">array\_intersect</span>
返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。注意键名保留不变。

### 参数

`array1`  
要检查的数组，作为主值。

`array2`  
要被对比的数组。

`...`  
要对比的数组列表。

### 返回值

返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。

### 范例

**示例 \#1 <span class="function">array\_intersect</span> 例子**

``` php
<?php
$array1 = array("a" => "green", "red", "blue");
$array2 = array("b" => "green", "yellow", "red");
$result = array_intersect($array1, $array2);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [a] => green
        [0] => red
    )

### 注释

> **Note**: <span class="simpara"> 两个单元仅在 *(string) $elem1 ===
> (string) $elem2*
> 时被认为是相同的。也就是说，当字符串的表达是一样的时候。 </span>

### 参见

-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_assoc</span>

array\_key\_exists
==================

检查数组里是否有指定的键名或索引

### 说明

<span class="type">bool</span> <span
class="methodname">array\_key\_exists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array`</span> )

数组里有键 `key` 时，<span class="function">array\_key\_exists</span>
返回 **`TRUE`**。 `key` 可以是任何能作为数组索引的值。

### 参数

`key`  
要检查的键。

`array`  
一个数组，包含待检查的键。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

> **Note**:
>
> <span class="function">array\_key\_exists</span> 仅仅搜索第一维的键。
> 多维数组里嵌套的键不会被搜索到。

### 范例

**示例 \#1 <span class="function">array\_key\_exists</span> 例子**

``` php
<?php
$search_array = array('first' => 1, 'second' => 4);
if (array_key_exists('first', $search_array)) {
    echo "The 'first' element is in the array";
}
?>
```

**示例 \#2 <span class="function">array\_key\_exists</span> 与 <span
class="function">isset</span> 的对比**

<span class="function">isset</span> 对于数组中为 **`NULL`** 的值不会返回
**`TRUE`**，而 <span class="function">array\_key\_exists</span> 会。

``` php
<?php
$search_array = array('first' => null, 'second' => 4);

// returns false
isset($search_array['first']);

// returns true
array_key_exists('first', $search_array);
?>
```

### 注释

> **Note**:
>
> 由于为了兼容以前版本，如果 <span class="type">object</span> 当做
> `array` 传入 <span class="function">array\_key\_exists</span>，同时
> `key` 是对象的属性，也会返回 **`TRUE`**。 不要依赖这个特性，保证参数
> `array` 类型是数组（<span class="type">array</span>）。
>
> 要检查对象是否有某个属性，应该去用 <span
> class="function">property\_exists</span>。

### 参见

-   <span class="function">isset</span>
-   <span class="function">array\_keys</span>
-   <span class="function">in\_array</span>
-   <span class="function">property\_exists</span>

array\_key\_first
=================

获取指定数组的第一个键值

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_key\_first</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

取得指定数组的 `array` 第一个键值，不影响到原数组的内部指针。

### 参数

`array`  
要操作的数组。

### 返回值

返回 `array` 的第一个键值（如果不为空），否则返回 **`NULL`**。

### 范例

**示例 \#1 <span class="function">array\_key\_first</span> 基本用法**

``` php
<?php
$array = ['a' => 1, 'b' => 2, 'c' => 3];

$firstKey = array_key_first($array);

var_dump($firstKey);
?>
```

以上例程会输出：

    string(1) "a"

### 注释

**小贴士**

在 PHP 7.3.0 之前，有几种方式可以实现该功能。可以使用 <span
class="function">array\_keys</span> 函数，但是性能会比较低。也可以使用
<span class="function">reset</span> 和 <span class="function">key</span>
函数，但这可能会影响内部数组指针。一个用旧函数实现该功能的方式如下:

``` php
<?php
if (!function_exists('array_key_first')) {
    function array_key_first(array $arr) {
        foreach($arr as $key => $unused) {
            return $key;
        }
        return NULL;
    }
}
?>
```

### 参见

-   <span class="function">array\_key\_last</span>
-   <span class="function">reset</span>

array\_key\_last
================

获取一个数组的最后一个键值

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_key\_last</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

取得指定数组的 `array` 最后一个键值，不会影响到原数组的内部指针。

### 参数

`array`  
要操作的数组。

### 返回值

返回 `array` 的最后一个键值（如果不为空），否则返回 **`NULL`**。

### 参见

-   <span class="function">array\_key\_first</span>
-   <span class="function">end</span>

array\_keys
===========

返回数组中部分的或所有的键名

### 说明

<span class="type">array</span> <span
class="methodname">array\_keys</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$search_value`<span
class="initializer"> = null</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$strict`<span
class="initializer"> = false</span></span> \]\] )

<span class="function">array\_keys</span> 返回 `input`
数组中的数字或者字符串的键名。

如果指定了可选参数 `search_value`，则只返回该值的键名。否则 `input`
数组中的所有键名都会被返回。

### 参数

`input`  
一个数组，包含了要返回的键。

`search_value`  
如果指定了这个参数，只有包含这些值的键才会返回。

`strict`  
判断在搜索的时候是否该使用严格的比较（===）。

### 返回值

返回 `input` 里的所有键。

### 范例

**示例 \#1 <span class="function">array\_keys</span> 例子**

``` php
<?php
$array = array(0 => 100, "color" => "red");
print_r(array_keys($array));

$array = array("blue", "red", "green", "blue", "blue");
print_r(array_keys($array, "blue"));

$array = array("color" => array("blue", "red", "green"),
               "size"  => array("small", "medium", "large"));
print_r(array_keys($array));
?>
```

以上例程会输出：

    Array
    (
        [0] => 0
        [1] => color
    )
    Array
    (
        [0] => 0
        [1] => 3
        [2] => 4
    )
    Array
    (
        [0] => color
        [1] => size
    )

### 参见

-   <span class="function">array\_values</span>
-   <span class="function">array\_combine</span>
-   <span class="function">array\_key\_exists</span>
-   <span class="function">array\_search</span>

array\_map
==========

为数组的每个元素应用回调函数

### 说明

<span class="type">array</span> <span
class="methodname">array\_map</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> , <span
class="methodparam"><span class="type">array</span> `$array1`</span> \[,
<span class="methodparam"><span class="type">array</span> `$...`</span>
\] )

<span class="function">array\_map</span>：返回数组，是为 `array1`
每个元素应用 `callback`函数之后的数组。 `callback` 函数形参的数量和传给
<span class="function">array\_map</span> 数组数量，两者必须一样。

### 参数

`callback`  
回调函数，应用到每个数组里的每个元素。

`array1`  
数组，遍历运行 `callback` 函数。

`...`  
数组列表，每个都遍历运行 `callback` 函数。

### 返回值

返回数组，包含 `callback` 函数处理之后 `array1` 的所有元素。

### 范例

**示例 \#1 <span class="function">array\_map</span> 例子**

``` php
<?php
function cube($n)
{
    return($n * $n * $n);
}

$a = array(1, 2, 3, 4, 5);
$b = array_map("cube", $a);
print_r($b);
?>
```

这使得 `$b` 成为：

    Array
    (
        [0] => 1
        [1] => 8
        [2] => 27
        [3] => 64
        [4] => 125
    )

**示例 \#2 <span class="function">array\_map</span> 使用匿名函数 (PHP
5.3.0 起)**

``` php
<?php
$func = function($value) {
    return $value * 2;
};

print_r(array_map($func, range(1, 5)));
?>
```

    Array
    (
        [0] => 2
        [1] => 4
        [2] => 6
        [3] => 8
        [4] => 10
    )

**示例 \#3 <span class="function">array\_map</span>：使用更多的数组**

``` php
<?php
function show_Spanish($n, $m)
{
    return("The number $n is called $m in Spanish");
}

function map_Spanish($n, $m)
{
    return(array($n => $m));
}

$a = array(1, 2, 3, 4, 5);
$b = array("uno", "dos", "tres", "cuatro", "cinco");

$c = array_map("show_Spanish", $a, $b);
print_r($c);

$d = array_map("map_Spanish", $a , $b);
print_r($d);
?>
```

以上例程会输出：

    // printout of $c
    Array
    (
        [0] => The number 1 is called uno in Spanish
        [1] => The number 2 is called dos in Spanish
        [2] => The number 3 is called tres in Spanish
        [3] => The number 4 is called cuatro in Spanish
        [4] => The number 5 is called cinco in Spanish
    )

    // printout of $d
    Array
    (
        [0] => Array
            (
                [1] => uno
            )

        [1] => Array
            (
                [2] => dos
            )

        [2] => Array
            (
                [3] => tres
            )

        [3] => Array
            (
                [4] => cuatro
            )

        [4] => Array
            (
                [5] => cinco
            )

    )

传入两个及以上的数组时，它们元素数量将会相同。因为回调函数会并行地处理相互对应的元素。
如果几个数组的元素数量不一致：空元素会扩展短那个数组，直到长度和最长的数组一样。

此函数有个有趣的用法：传入 **`NULL`**
作为回调函数的名称，将创建多维数组（一个数组，内部包含数组。）

**示例 \#4 多维数组：创建数组，内部包含数组**

``` php
<?php
$a = array(1, 2, 3, 4, 5);
$b = array("one", "two", "three", "four", "five");
$c = array("uno", "dos", "tres", "cuatro", "cinco");

$d = array_map(null, $a, $b, $c);
print_r($d);
?>
```

以上例程会输出：

    Array
    (
        [0] => Array
            (
                [0] => 1
                [1] => one
                [2] => uno
            )

        [1] => Array
            (
                [0] => 2
                [1] => two
                [2] => dos
            )

        [2] => Array
            (
                [0] => 3
                [1] => three
                [2] => tres
            )

        [3] => Array
            (
                [0] => 4
                [1] => four
                [2] => cuatro
            )

        [4] => Array
            (
                [0] => 5
                [1] => five
                [2] => cinco
            )

    )

如果仅传入一个数组，键（key）会保留；传入多个数组，键（key）是整型数字的序列。

**示例 \#5 <span class="function">array\_map</span> 键（key）是 string**

``` php
<?php
$arr = array("stringkey" => "value");
function cb1($a) {
    return array ($a);
}
function cb2($a, $b) {
    return array ($a, $b);
}
var_dump(array_map("cb1", $arr));
var_dump(array_map("cb2", $arr, $arr));
var_dump(array_map(null,  $arr));
var_dump(array_map(null, $arr, $arr));
?>
```

以上例程会输出：

    array(1) {
      ["stringkey"]=>
      array(1) {
        [0]=>
        string(5) "value"
      }
    }
    array(1) {
      [0]=>
      array(2) {
        [0]=>
        string(5) "value"
        [1]=>
        string(5) "value"
      }
    }
    array(1) {
      ["stringkey"]=>
      string(5) "value"
    }
    array(1) {
      [0]=>
      array(2) {
        [0]=>
        string(5) "value"
        [1]=>
        string(5) "value"
      }
    }

### 参见

-   <span class="function">array\_filter</span>
-   <span class="function">array\_reduce</span>
-   <span class="function">array\_walk</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

array\_merge\_recursive
=======================

递归地合并一个或多个数组

### 说明

<span class="type">array</span> <span
class="methodname">array\_merge\_recursive</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> \[,
<span class="methodparam"><span class="type">array</span> `$...`</span>
\] )

<span class="function">array\_merge\_recursive</span>
将一个或多个数组的单元合并起来，一个数组中的值附加在前一个数组的后面。返回作为结果的数组。

如果输入的数组中有相同的字符串键名，则这些值会被合并到一个数组中去，这将递归下去，因此如果一个值本身是一个数组，本函数将按照相应的条目把它合并为另一个数组。需要注意的是，如果数组具有相同的数值键名，后一个值将不会覆盖原来的值，而是附加到后面。

### 参数

`array1`  
要合并的初始数组。

`...`  
数组变量列表，进行递归合并。

### 返回值

一个结果数组，其中的值合并自附加的参数。

### 范例

**示例 \#1 <span class="function">array\_merge\_recursive</span> 例子**

``` php
<?php
$ar1 = array("color" => array("favorite" => "red"), 5);
$ar2 = array(10, "color" => array("favorite" => "green", "blue"));
$result = array_merge_recursive($ar1, $ar2);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [color] => Array
            (
                [favorite] => Array
                    (
                        [0] => red
                        [1] => green
                    )

                [0] => blue
            )

        [0] => 5
        [1] => 10
    )

### 参见

-   <span class="function">array\_merge</span>
-   <span class="function">array\_replace\_recursive</span>

array\_merge
============

合并一个或多个数组

### 说明

<span class="type">array</span> <span
class="methodname">array\_merge</span> (\[ <span
class="methodparam"><span class="type">array</span> `$...`</span> \] )

将一个或多个数组的单元合并起来，一个数组中的值附加在前一个数组的后面。返回作为结果的数组。

如果输入的数组中有相同的字符串键名，则该键名后面的值将覆盖前一个值。然而，如果数组包含数字键名，后面的值将
*不会* 覆盖原来的值，而是附加到后面。

如果输入的数组存在以数字作为索引的内容，则这项内容的键名会以连续方式重新索引。

### 参数

`...`  
要合并的数组。

### 返回值

返回合并后的结果数组。如果参数为空，则返回空 <span
class="type">array</span>。

### 更新日志

| 版本  | 说明                                         |
|-------|----------------------------------------------|
| 7.4.0 | 允许不带参数调用，之前版本至少需要一个参数。 |

### 范例

**示例 \#1 <span class="function">array\_merge</span> 示例**

``` php
<?php
$array1 = array("color" => "red", 2, 4);
$array2 = array("a", "b", "color" => "green", "shape" => "trapezoid", 4);
$result = array_merge($array1, $array2);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [color] => green
        [0] => 2
        [1] => 4
        [2] => a
        [3] => b
        [shape] => trapezoid
        [4] => 4
    )

**示例 \#2 Simple <span class="function">array\_merge</span> 示例**

``` php
<?php
$array1 = array();
$array2 = array(1 => "data");
$result = array_merge($array1, $array2);
?>
```

别忘了数字键名将会被重新编号！

    Array
    (
        [0] => data
    )

如果你想完全保留原有数组并只想新的数组附加到后面，可以使用 *+* 运算符：

``` php
<?php
$array1 = array(0 => 'zero_a', 2 => 'two_a', 3 => 'three_a');
$array2 = array(1 => 'one_b', 3 => 'three_b', 4 => 'four_b');
$result = $array1 + $array2;
var_dump($result);
?>
```

第一个数组的键名将会被保留。在两个数组中存在相同的键名时，第一个数组中的同键名的元素将会被保留，第二个数组中的元素将会被忽略。

    array(5) {
      [0]=>
      string(6) "zero_a"
      [2]=>
      string(5) "two_a"
      [3]=>
      string(7) "three_a"
      [1]=>
      string(5) "one_b"
      [4]=>
      string(6) "four_b"
    }

**示例 \#3 <span class="function">array\_merge</span> 合并非数组的类型**

``` php
<?php
$beginning = 'foo';
$end = array(1 => 'bar');
$result = array_merge((array)$beginning, (array)$end);
print_r($result);
?>
```

以上例程会输出：

        Array
        (
            [0] => foo
            [1] => bar
        )

### 参见

-   <span class="function">array\_merge\_recursive</span>
-   <span class="function">array\_replace</span>
-   <span class="function">array\_combine</span>
-   <a href="/language/operators/array.html" class="link">数组操作符</a>

array\_multisort
================

对多个数组或多维数组进行排序

### 说明

<span class="type">bool</span> <span
class="methodname">array\_multisort</span> ( <span
class="methodparam"><span class="type">array</span> `&$array1`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$array1_sort_order`<span class="initializer"> = SORT\_ASC</span></span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$array1_sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \]\]\] )

<span class="function">array\_multisort</span>
可以用来一次对多个数组进行排序，或者根据某一维或多维对多维数组进行排序。

关联（<span
class="type">string</span>）键名保持不变，但数字键名会被重新索引。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array1`  
要排序的 <span class="type">array</span>。

`array1_sort_order`  
之前 <span class="type">array</span> 参数要排列的顺序。 **`SORT_ASC`**
按照上升顺序排序， **`SORT_DESC`** 按照下降顺序排序。

此参数可以和 `array1_sort_flags` 互换，也可以完全删除，默认是
**`SORT_ASC`** 。

`array1_sort_flags`  
为 <span class="type">array</span> 参数设定选项：

排序类型标志：

-   <span class="simpara">**`SORT_REGULAR`** -
    将项目按照通常方法比较（不修改类型） </span>
-   <span class="simpara">**`SORT_NUMERIC`** - 按照数字大小比较</span>
-   <span class="simpara">**`SORT_STRING`** - 按照字符串比较</span>
-   <span class="simpara"> **`SORT_LOCALE_STRING`** -
    根据当前的本地化设置，按照字符串比较。 它会使用 locale
    信息，可以通过 <span class="function">setlocale</span> 修改此信息。
    </span>
-   <span class="simpara"> **`SORT_NATURAL`** -
    以字符串的"自然排序"，类似 <span class="function">natsort</span>
    </span>
-   <span class="simpara"> **`SORT_FLAG_CASE`** - 可以组合 (按位或 OR)
    **`SORT_STRING`** 或者 **`SORT_NATURAL`**
    大小写不敏感的方式排序字符串。 </span>

参数可以和 `array1_sort_order` 交换或者省略，默认情况下是
**`SORT_REGULAR`**。

`...`  
可选的选项，可提供更多数组，跟随在 sort order 和 sort flag 之后。
提供的数组和之前的数组要有相同数量的元素。
换言之，排序是按字典顺序排列的。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                       |
|-------|----------------------------------------------------------------------------|
| 5.4.0 | `array1_sort_flags` 增加 **`SORT_NATURAL`** 和 **`SORT_FLAG_CASE`** 选项。 |
| 5.3.0 | `array1_sort_flags` 增加选项 **`SORT_LOCALE_STRING`**。                    |

### 范例

**示例 \#1 多个数组排序**

``` php
<?php
$ar1 = array(10, 100, 100, 0);
$ar2 = array(1, 3, 2, 4);
array_multisort($ar1, $ar2);

var_dump($ar1);
var_dump($ar2);
?>
```

这个例子里，排序后，第一个数组会包含 0、 10、 100、 100。
第二个数组会包含 4、1、 2、 3。
第二个数组里的项目对应第一个数组后也进行了排序（100 和 100）。

    array(4) {
      [0]=> int(0)
      [1]=> int(10)
      [2]=> int(100)
      [3]=> int(100)
    }
    array(4) {
      [0]=> int(4)
      [1]=> int(1)
      [2]=> int(2)
      [3]=> int(3)
    }

**示例 \#2 排序多维数组**

``` php
<?php
$ar = array(
       array("10", 11, 100, 100, "a"),
       array(   1,  2, "2",   3,   1)
      );
array_multisort($ar[0], SORT_ASC, SORT_STRING,
                $ar[1], SORT_NUMERIC, SORT_DESC);
var_dump($ar);
?>
```

本例中在排序后，第一个数组将变成
"10"，100，100，11，"a"（被当作字符串以升序排列）。第二个数组将包含 1,
3, "2", 2, 1（被当作数字以降序排列）。

    array(2) {
      [0]=> array(5) {
        [0]=> string(2) "10"
        [1]=> int(100)
        [2]=> int(100)
        [3]=> int(11)
        [4]=> string(1) "a"
      }
      [1]=> array(5) {
        [0]=> int(1)
        [1]=> int(3)
        [2]=> string(1) "2"
        [3]=> int(2)
        [4]=> int(1)
      }
    }

**示例 \#3 对数据库结果进行排序**

本例中 `data`
数组中的每个单元表示一个表中的一行。这是典型的数据库记录的数据集合。

例子中的数据如下：

    volume | edition
    -------+--------
        67 |       2
        86 |       1
        85 |       6
        98 |       2
        86 |       6
        67 |       7

数据全都存放在名为 `data`
的数组中。这通常是通过循环从数据库取得的结果，例如 <span
class="function">mysql\_fetch\_assoc</span>。

``` php
<?php
$data[] = array('volume' => 67, 'edition' => 2);
$data[] = array('volume' => 86, 'edition' => 1);
$data[] = array('volume' => 85, 'edition' => 6);
$data[] = array('volume' => 98, 'edition' => 2);
$data[] = array('volume' => 86, 'edition' => 6);
$data[] = array('volume' => 67, 'edition' => 7);
?>
```

本例中将把 `volume` 降序排列，把 `edition` 升序排列。

现在有了包含有行的数组，但是 <span
class="function">array\_multisort</span>
需要一个包含列的数组，因此用以下代码来取得列，然后排序。

``` php
<?php
// 取得列的列表
foreach ($data as $key => $row) {
    $volume[$key]  = $row['volume'];
    $edition[$key] = $row['edition'];
}

// 将数据根据 volume 降序排列，根据 edition 升序排列
// 把 $data 作为最后一个参数，以通用键排序
array_multisort($volume, SORT_DESC, $edition, SORT_ASC, $data);
?>
```

数据集合现在排好序了，结果如下：

    volume | edition
    -------+--------
        98 |       2
        86 |       1
        86 |       6
        85 |       6
        67 |       2
        67 |       7

**示例 \#4 不区分大小写字母排序**

**`SORT_STRING`** 和 **`SORT_REGULAR`**
都是区分大小写字母的，大写字母会排在小写字母之前。

要进行不区分大小写的排序，就要按照原数组的小写字母拷贝来排序。

``` php
<?php
$array = array('Alpha', 'atomic', 'Beta', 'bank');
$array_lowercase = array_map('strtolower', $array);

array_multisort($array_lowercase, SORT_ASC, SORT_STRING, $array);

print_r($array);
?>
```

以上例程会输出：

    Array
    (
        [0] => Alpha
        [1] => atomic
        [2] => bank
        [3] => Beta
    )

### 参见

-   <span class="function">usort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

array\_pad
==========

以指定长度将一个值填充进数组

### 说明

<span class="type">array</span> <span
class="methodname">array\_pad</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> , <span
class="methodparam"><span class="type">int</span> `$size`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="function">array\_pad</span> 返回 `array` 的一个拷贝，并用
`value` 将其填补到 `size` 指定的长度。如果 `size`
为正，则填补到数组的右侧，如果为负则从左侧开始填补。如果 `size`
的绝对值小于或等于 `array` 数组的长度则没有任何填补。有可能一次最多填补
1048576 个单元。

### 参数

`array`  
需要被填充的原始数组。

`size`  
新数组的长度。

`value`  
将被填充的值，只有在 `array` 的现有长度小于 `size` 的长度时才有效。

### 返回值

返回 `array` 用 `value` 填充到 `size` 指定的长度之后的一个副本。 如果
`size` 为正，则填补到数组的右侧，如果为负则从左侧开始填补。 如果 `size`
的绝对值小于或等于 `array` 数组的长度则没有任何填补。

### 范例

**示例 \#1 <span class="function">array\_pad</span> 例子**

``` php
<?php
$input = array(12, 10, 9);

$result = array_pad($input, 5, 0);
// result is array(12, 10, 9, 0, 0)

$result = array_pad($input, -7, -1);
// result is array(-1, -1, -1, -1, 12, 10, 9)

$result = array_pad($input, 2, "noop");
// not padded
?>
```

### 参见

-   <span class="function">array\_fill</span>
-   <span class="function">range</span>

array\_pop
==========

弹出数组最后一个单元（出栈）

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_pop</span> ( <span class="methodparam"><span
class="type">array</span> `&$array`</span> )

<span class="function">array\_pop</span> 弹出并返回 `array`
数组的最后一个单元，并将数组 `array` 的长度减一。

> **Note**: <span class="simpara">使用此函数后会重置（<span
> class="function">reset</span>）<span class="type">array</span>
> 指针。</span>

### 参数

`array`  
需要弹出栈的数组。

### 返回值

返回 `array` 的最后一个值。如果 `array`
是空（如果不是一个数组），将会返回 **`NULL`** 。

### 错误／异常

调用此函数去处理非数组的值，会产生
<a href="/errorfunc/constants.html" class="link">E_WARNING</a>
级别的错误。

### 范例

**示例 \#1 <span class="function">array\_pop</span> 例子**

``` php
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_pop($stack);
print_r($stack);
?>
```

经过此操作后，`$stack` 将只有 3 个单元：

    Array
    (
        [0] => orange
        [1] => banana
        [2] => apple
    )

并且 *raspberry* 将被赋给 `$fruit`。

### 参见

-   <span class="function">array\_push</span>
-   <span class="function">array\_shift</span>
-   <span class="function">array\_unshift</span>

array\_product
==============

计算数组中所有值的乘积

### 说明

<span class="type">number</span> <span
class="methodname">array\_product</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

<span class="function">array\_product</span>
以整数或浮点数返回一个数组中所有值的乘积。

### 参数

`array`  
这个数组。

### 返回值

以整数或浮点数返回一个数组中所有值的乘积。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.3.6 | 空数组现在会产生 1，而之前此函数处理空数组会产生 0。 |

### 范例

**示例 \#1 <span class="function">array\_product</span> 例子**

``` php
<?php

$a = array(2, 4, 6, 8);
echo "product(a) = " . array_product($a) . "\n";
echo "product(array()) = " . array_product(array()) . "\n";

?>
```

以上例程会输出：

    product(a) = 384
    product(array()) = 1

array\_push
===========

将一个或多个单元压入数组的末尾（入栈）

### 说明

<span class="type">int</span> <span
class="methodname">array\_push</span> ( <span class="methodparam"><span
class="type">array</span> `&$array`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value1`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

<span class="function">array\_push</span> 将 `array`
当成一个栈，并将传入的变量压入 `array` 的末尾。`array`
的长度将根据入栈变量的数目增加。和如下效果相同：

``` php
<?php
$array[] = $var;
?>
```

并对每个传入的值重复以上动作。

> **Note**: <span class="simpara"> 如果用 <span
> class="function">array\_push</span> 来给数组增加一个单元，还不如用
> *$array\[\] =* ，因为这样没有调用函数的额外负担。 </span>

> **Note**: <span class="simpara"> 如果第一个参数不是数组，<span
> class="function">array\_push</span> 将发出一条警告。这和 *$var\[\]*
> 的行为不同，后者会新建一个数组。 </span>

### 参数

`array`  
输入的数组。

`value1`  
要压入 `array` 末尾的第一个值。

### 返回值

返回处理之后数组的元素个数。

### 范例

**示例 \#1 <span class="function">array\_push</span> 例子**

``` php
<?php
$stack = array("orange", "banana");
array_push($stack, "apple", "raspberry");
print_r($stack);
?>
```

以上例程会输出：

    Array
    (
        [0] => orange
        [1] => banana
        [2] => apple
        [3] => raspberry
    )

### 参见

-   <span class="function">array\_pop</span>
-   <span class="function">array\_shift</span>
-   <span class="function">array\_unshift</span>

array\_rand
===========

从数组中随机取出一个或多个单元

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_rand</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> \[, <span
class="methodparam"><span class="type">int</span> `$num`<span
class="initializer"> = 1</span></span> \] )

从数组中取出一个或多个随机的单元，并返回随机条目的一个或多个键。
它使用了伪随机数产生算法，所以不适合密码学场景，

### 参数

`array`  
输入的数组。

`num`  
指明了你想取出多少个单元。

### 返回值

如果只取出一个，<span class="function">array\_rand</span>
返回随机单元的键名。 否则就返回包含随机键名的数组。
完成后，就可以根据随机的键获取数组的随机值。 取出数量如果超过 array
的长度，就会导致 **`E_WARNING`** 错误，并返回 NULL。

### 更新日志

| 版本   | 说明                                                                                                                                                                                                                                                                      |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0  | <a href="/migration71/incompatible.html#migration71.incompatible.rand-srand-aliases" class="link">内置的随机数生成算法从 libc rand 函数改成</a><a href="http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html" class="link external">» 梅森旋转</a> 伪随机数生成算法。 |
| 5.2.10 | The resulting array of keys is no longer shuffled.                                                                                                                                                                                                                        |

### 范例

**示例 \#1 <span class="function">array\_rand</span> 例子**

``` php
<?php
$input = array("Neo", "Morpheus", "Trinity", "Cypher", "Tank");
$rand_keys = array_rand($input, 2);
echo $input[$rand_keys[0]] . "\n";
echo $input[$rand_keys[1]] . "\n";
?>
```

### 参见

-   <span class="function">shuffle</span>

array\_reduce
=============

用回调函数迭代地将数组简化为单一的值

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_reduce</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$initial`<span class="initializer"> =
**`NULL`**</span></span> \] )

<span class="function">array\_reduce</span> 将回调函数 `callback`
迭代地作用到 `array` 数组中的每一个单元中，从而将数组简化为单一的值。

### 参数

`array`  
输入的 array。

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$carry`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$item`</span>
)

`carry`  
携带上次迭代里的值； 如果本次迭代是第一次，那么这个值是 `initial`。

`item`  
携带了本次迭代的值。

`initial`  
如果指定了可选参数
`initial`，该参数将在处理开始前使用，或者当处理结束，数组为空时的最后一个结果。

### 返回值

返回结果值。

`initial` 参数，<span class="function">array\_reduce</span> 返回
**`NULL`**。

### 更新日志

| 版本  | 说明                                                                                                          |
|-------|---------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 修改 `initial` 类型，允许传入 <span class="type">mixed</span>，之前只能是 <span class="type">integer</span>。 |

### 范例

**示例 \#1 <span class="function">array\_reduce</span> 例子**

``` php
<?php
function sum($carry, $item)
{
    $carry += $item;
    return $carry;
}

function product($carry, $item)
{
    $carry *= $item;
    return $carry;
}

$a = array(1, 2, 3, 4, 5);
$x = array();

var_dump(array_reduce($a, "sum")); // int(15)
var_dump(array_reduce($a, "product", 10)); // int(1200), because: 10*1*2*3*4*5
var_dump(array_reduce($x, "sum", "No data to reduce")); // string(17) "No data to reduce"
?>
```

### 参见

-   <span class="function">array\_filter</span>
-   <span class="function">array\_map</span>
-   <span class="function">array\_unique</span>
-   <span class="function">array\_count\_values</span>

array\_replace\_recursive
=========================

使用传递的数组递归替换第一个数组的元素

### 说明

<span class="type">array</span> <span
class="methodname">array\_replace\_recursive</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> \[,
<span class="methodparam"><span class="type">array</span> `$...`</span>
\] )

<span class="function">array\_replace\_recursive</span>
使用后面数组元素的值替换数组 `array1` 的值。
如果一个键存在于第一个数组同时也存在于第二个数组，它的值将被第二个数组中的值替换。
如果一个键存在于第二个数组，但是不存在于第一个数组，则会在第一个数组中创建这个元素。
如果一个键仅存在于第一个数组，它将保持不变。
如果传递了多个替换数组，它们将被按顺序依次处理，后面的数组将覆盖之前的值。

<span class="function">array\_replace\_recursive</span>
是递归的：它将遍历数组并将相同的处理应用到数组的内部值。

如果第一个数组中的值是标量，它的值将被第二个数组中的值替换，它可能是一个标量或者数组。如果第一个数组和第二个数组中的值都是数组，<span
class="function">array\_replace\_recursive</span>
函数将递归地替换它们各自的值。

### 参数

`array1`  
替换该数组的值。

`...`  
可选项。包含要提取元素的数组。

### 返回值

返回一个<span class="type">数组</span>。如果发生错误，将返回
**`NULL`**。

### 范例

**示例 \#1 <span class="function">array\_replace\_recursive</span>
范例**

``` php
<?php
$base = array('citrus' => array( "orange") , 'berries' => array("blackberry", "raspberry"), );
$replacements = array('citrus' => array('pineapple'), 'berries' => array('blueberry'));

$basket = array_replace_recursive($base, $replacements);
print_r($basket);

$basket = array_replace($base, $replacements);
print_r($basket);
?>
```

以上例程会输出：

    Array
    (
        [citrus] => Array
            (
                [0] => pineapple
            )

        [berries] => Array
            (
                [0] => blueberry
                [1] => raspberry
            )

    )
    Array
    (
        [citrus] => Array
            (
                [0] => pineapple
            )

        [berries] => Array
            (
                [0] => blueberry
            )

    )

**示例 \#2 <span class="function">array\_replace\_recursive</span>
及其递归表现**

``` php
<?php
$base = array('citrus' => array("orange") , 'berries' => array("blackberry", "raspberry"), 'others' => 'banana' );
$replacements = array('citrus' => 'pineapple', 'berries' => array('blueberry'), 'others' => array('litchis'));
$replacements2 = array('citrus' => array('pineapple'), 'berries' => array('blueberry'), 'others' => 'litchis');

$basket = array_replace_recursive($base, $replacements, $replacements2);
print_r($basket);

?>
```

以上例程会输出：

    Array
    (
        [citrus] => Array
            (
                [0] => pineapple
            )

        [berries] => Array
            (
                [0] => blueberry
                [1] => raspberry
            )

        [others] => litchis
    )

### 参见

-   <span class="function">array\_replace</span>
-   <span class="function">array\_merge\_recursive</span>

array\_replace
==============

使用传递的数组替换第一个数组的元素

### 说明

<span class="type">array</span> <span
class="methodname">array\_replace</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> \[,
<span class="methodparam"><span class="type">array</span> `$...`</span>
\] )

<span class="function">array\_replace</span> 函数使用后面数组元素相同
key 的值替换 `array1`
数组的值。如果一个键存在于第一个数组同时也存在于第二个数组，它的值将被第二个数组中的值替换。如果一个键存在于第二个数组，但是不存在于第一个数组，则会在第一个数组中创建这个元素。如果一个键仅存在于第一个数组，它将保持不变。如果传递了多个替换数组，它们将被按顺序依次处理，后面的数组将覆盖之前的值。

<span class="function">array\_replace</span>
是非递归的：它将第一个数组的值进行替换而不管第二个数组中是什么类型。

### 参数

`array1`  
替换该数组的值。

`...`  
包含要提取元素的数组。 后面的数组里的值会覆盖前面的值。

### 返回值

返回一个<span class="type">数组</span>。如果发生错误，将返回
**`NULL`**。

### 范例

**示例 \#1 <span class="function">array\_replace</span> 范例**

``` php
<?php
$base = array("orange", "banana", "apple", "raspberry");
$replacements = array(0 => "pineapple", 4 => "cherry");
$replacements2 = array(0 => "grape");

$basket = array_replace($base, $replacements, $replacements2);
print_r($basket);
?>
```

以上例程会输出：

    Array
    (
        [0] => grape
        [1] => banana
        [2] => apple
        [3] => raspberry
        [4] => cherry
    )

### 参见

-   <span class="function">array\_replace\_recursive</span>
-   <span class="function">array\_merge</span>

array\_reverse
==============

返回单元顺序相反的数组

### 说明

<span class="type">array</span> <span
class="methodname">array\_reverse</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$preserve_keys`<span class="initializer"> = **`FALSE`**</span></span>
\] )

<span class="function">array\_reverse</span> 接受数组 `array`
作为输入并返回一个单元为相反顺序的新数组。

### 参数

`array`  
输入的数组。

`preserve_keys`  
如果设置为 **`TRUE`** 会保留数字的键。
非数字的键则不受这个设置的影响，总是会被保留。

### 返回值

返回反转后的数组。

### 范例

**示例 \#1 <span class="function">array\_reverse</span> 例子**

``` php
<?php
$input  = array("php", 4.0, array("green", "red"));
$reversed = array_reverse($input);
$preserved = array_reverse($input, true);

print_r($input);
print_r($reversed);
print_r($preserved);
?>
```

以上例程会输出：

    Array
    (
        [0] => php
        [1] => 4
        [2] => Array
            (
                [0] => green
                [1] => red
            )

    )
    Array
    (
        [0] => Array
            (
                [0] => green
                [1] => red
            )

        [1] => 4
        [2] => php
    )
    Array
    (
        [2] => Array
            (
                [0] => green
                [1] => red
            )

        [1] => 4
        [0] => php
    )

### 参见

-   <span class="function">array\_flip</span>

array\_search
=============

在数组中搜索给定的值，如果成功则返回首个相应的键名

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_search</span> ( <span
class="methodparam"><span class="type">mixed</span> `$needle`</span> ,
<span class="methodparam"><span class="type">array</span>
`$haystack`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$strict`<span class="initializer"> =
false</span></span> \] )

大海捞针，在大海（`haystack`）中搜索针（ `needle` 参数）。

### 参数

`needle`  
搜索的值。

> **Note**:
>
> 如果 `needle` 是字符串，则比较以区分大小写的方式进行。

`haystack`  
这个数组。

`strict`  
如果可选的第三个参数 `strict` 为 **`TRUE`**，则 <span
class="function">array\_search</span> 将在 `haystack`
中检查*完全相同*的元素。 这意味着同样严格比较 `haystack` 里 `needle` 的
<a href="/language/types.html" class="link">类型</a>，并且对象需是同一个实例。

### 返回值

如果找到了 `needle` 则返回它的键，否则返回 **`FALSE`**。

如果 `needle` 在 `haystack`
中出现不止一次，则返回第一个匹配的键。要返回所有匹配值的键，应该用 <span
class="function">array\_keys</span> 加上可选参数 `search_value` 来代替。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本  | 说明                                                                                                                                                   |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | As with all internal PHP functions as of 5.3.0, <span class="function">array\_search</span> returns **`NULL`** if invalid parameters are passed to it. |

### 范例

**示例 \#1 <span class="function">array\_search</span> 例子**

``` php
<?php
$array = array(0 => 'blue', 1 => 'red', 2 => 'green', 3 => 'red');

$key = array_search('green', $array); // $key = 2;
$key = array_search('red', $array);   // $key = 1;
?>
```

### 参见

-   <span class="function">array\_keys</span>
-   <span class="function">array\_values</span>
-   <span class="function">array\_key\_exists</span>
-   <span class="function">in\_array</span>

array\_shift
============

将数组开头的单元移出数组

### 说明

<span class="type">mixed</span> <span
class="methodname">array\_shift</span> ( <span class="methodparam"><span
class="type">array</span> `&$array`</span> )

<span class="function">array\_shift</span> 将 `array`
的第一个单元移出并作为结果返回，将 `array`
的长度减一并将所有其它单元向前移动一位。所有的数字键名将改为从零开始计数，文字键名将不变。

> **Note**: <span class="simpara">使用此函数后会重置（<span
> class="function">reset</span>）<span class="type">array</span>
> 指针。</span>

### 参数

`array`  
输入的数组。

### 返回值

返回移出的值，如果 `array` 为 空或不是一个数组则返回 **`NULL`**。

### 范例

**示例 \#1 <span class="function">array\_shift</span> 例子**

``` php
<?php
$stack = array("orange", "banana", "apple", "raspberry");
$fruit = array_shift($stack);
print_r($stack);
?>
```

以上例程会输出：

    Array
    (
        [0] => banana
        [1] => apple
        [2] => raspberry
    )

并且 *orange* 被赋给了 `$fruit`。

### 参见

-   <span class="function">array\_unshift</span>
-   <span class="function">array\_push</span>
-   <span class="function">array\_pop</span>

array\_slice
============

从数组中取出一段

### 说明

<span class="type">array</span> <span
class="methodname">array\_slice</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> , <span
class="methodparam"><span class="type">int</span> `$offset`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$preserve_keys`<span
class="initializer"> = false</span></span> \]\] )

<span class="function">array\_slice</span> 返回根据 `offset` 和 `length`
参数所指定的 `array` 数组中的一段序列。

### 参数

`array`  
输入的数组。

`offset`  
如果 `offset` 非负，则序列将从 `array` 中的此偏移量开始。如果 `offset`
为负，则序列将从 `array` 中距离末端这么远的地方开始。

`length`  
如果给出了 `length` 并且为正，则序列中将具有这么多的单元。如果给出了
`length`
并且为负，则序列将终止在距离数组末端这么远的地方。如果省略，则序列将从
`offset` 开始一直到 `array` 的末端。

`preserve_keys`  
注意 <span class="function">array\_slice</span>
默认会重新排序并重置数组的数字索引。你可以通过将 `preserve_keys` 设为
**`TRUE`** 来改变此行为。

### 返回值

返回其中一段。 如果 offset 参数大于 array 尺寸，就会返回空的 array。

### 更新日志

| 版本  | 说明                                                                                                                                                          |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.2.4 | `length` 参数默认值改成 *NULL*。 现在 `length` 为 *NULL* 时，意思是说使用 `array` 的长度。 之前的版本里， *NULL* 的 `length` 的意思是长度为零（啥也不返回）。 |
| 5.0.2 | 增加了可选参数 `preserve_keys` 。                                                                                                                             |

### 范例

**示例 \#1 <span class="function">array\_slice</span> 例子**

``` php
<?php
$input = array("a", "b", "c", "d", "e");

$output = array_slice($input, 2);      // returns "c", "d", and "e"
$output = array_slice($input, -2, 1);  // returns "d"
$output = array_slice($input, 0, 3);   // returns "a", "b", and "c"

// note the differences in the array keys
print_r(array_slice($input, 2, -1));
print_r(array_slice($input, 2, -1, true));
?>
```

以上例程会输出：

    Array
    (
        [0] => c
        [1] => d
    )
    Array
    (
        [2] => c
        [3] => d
    )

### 参见

-   <span class="function">array\_splice</span>
-   <span class="function">unset</span>
-   <span class="function">array\_chunk</span>

array\_splice
=============

去掉数组中的某一部分并用其它值取代

### 说明

<span class="type">array</span> <span
class="methodname">array\_splice</span> ( <span
class="methodparam"><span class="type">array</span> `&$input`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$length`<span class="initializer"> = count($input)</span></span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$replacement`<span class="initializer"> = array()</span></span> \]\] )

把 `input` 数组中由 `offset` 和 `length` 指定的单元去掉，如果提供了
`replacement` 参数，则用其中的单元取代。

注意 `input` 中的数字键名不被保留。

> **Note**: <span class="simpara"> 如果 `replacement` 不是数组，会被
> <a href="/language/types/array.html#language.types.array.casting" class="link">类型转换</a>
> 成数组 (例如： `(array) $replacement`)。 当传入的 `replacement`
> 是个对象或者 **`NULL`**，会导致未知的行为出现。 </span>

### 参数

`input`  
输入的数组。

`offset`  
如果 `offset` 为正，则从 `input` 数组中该值指定的偏移量开始移除。如果
`offset` 为负，则从 `input` 末尾倒数该值指定的偏移量开始移除。

`length`  
如果省略 `length`，则移除数组中从 `offset` 到结尾的所有部分。如果指定了
`length` 并且为正值，则移除这么多单元。如果指定了 `length`
并且为负值，则移除从 `offset` 到数组末尾倒数 `length`
为止中间所有的单元。 如果设置了 `length` 为零，不会移除单元。
小窍门：当给出了 `replacement` 时要移除从 `offset`
到数组末尾所有单元时，用 *count($input)* 作为 `length`。

`replacement`  
如果给出了 `replacement` 数组，则被移除的单元被此数组中的单元替代。

如果 `offset` 和 `length` 的组合结果是不会移除任何值，则 `replacement`
数组中的单元将被插入到 `offset` 指定的位置。
注意替换数组中的键名不保留。

如果用来替换 `replacement` 只有一个单元，那么不需要给它加上
*array()*，除非该单元本身就是一个数组、一个对象或者 **`NULL`**。

### 返回值

返回一个包含有被移除单元的数组。

### 范例

**示例 \#1 <span class="function">array\_splice</span> 例子**

``` php
<?php
$input = array("red", "green", "blue", "yellow");
array_splice($input, 2);
// $input is now array("red", "green")

$input = array("red", "green", "blue", "yellow");
array_splice($input, 1, -1);
// $input is now array("red", "yellow")

$input = array("red", "green", "blue", "yellow");
array_splice($input, 1, count($input), "orange");
// $input is now array("red", "orange")

$input = array("red", "green", "blue", "yellow");
array_splice($input, -1, 1, array("black", "maroon"));
// $input is now array("red", "green",
//          "blue", "black", "maroon")

$input = array("red", "green", "blue", "yellow");
array_splice($input, 3, 0, "purple");
// $input is now array("red", "green",
//          "blue", "purple", "yellow");
?>
```

**示例 \#2 <span class="function">array\_splice</span> 例子**

以下表达式以同样方式修改了 `$input`：

``` php
<?php

// 添加两个新元素到 $input
array_push($input, $x, $y);
array_splice($input, count($input), 0, array($x, $y));

// 移除 $input 中的最后一个元素
array_pop($input);
array_splice($input, -1);

// 移除  $input 中第一个元素
array_shift($input);
array_splice($input, 0, 1);

// 在 $input 的开头插入一个元素
array_unshift($input, $x, $y);
array_splice($input, 0, 0, array($x, $y));

// 在 $input  的索引  $x 处替换值
$input[$x] = $y; // 对于键名和偏移量等值的数组
array_splice($input, $x, 1, $y);
?>
```

### 参见

-   <span class="function">array\_slice</span>
-   <span class="function">unset</span>
-   <span class="function">array\_merge</span>

array\_sum
==========

对数组中所有值求和

### 说明

<span class="type">number</span> <span
class="methodname">array\_sum</span> ( <span class="methodparam"><span
class="type">array</span> `$array`</span> )

<span class="function">array\_sum</span>
将数组中的所有值相加，并返回结果。

### 参数

`array`  
输入的数组。

### 返回值

所有值的和以整数或浮点数的结果返回，`array` 为空时则返回 *0*。

### 范例

**示例 \#1 <span class="function">array\_sum</span> 例子**

``` php
<?php
$a = array(2, 4, 6, 8);
echo "sum(a) = " . array_sum($a) . "\n";

$b = array("a" => 1.2, "b" => 2.3, "c" => 3.4);
echo "sum(b) = " . array_sum($b) . "\n";
?>
```

以上例程会输出：

    sum(a) = 20
    sum(b) = 6.9

array\_udiff\_assoc
===================

带索引检查计算数组的差集，用回调函数比较数据

### 说明

<span class="type">array</span> <span
class="methodname">array\_udiff\_assoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$value_compare_func`</span> )

此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。

> **Note**: <span class="simpara">
> 注意本函数只检查了多维数组中的一维。当然，可以用
> *array\_udiff\_assoc($array1\[0\], $array2\[0\],
> "some\_comparison\_func");* 来检查更深的维度。 </span>

### 参数

`array1`  
第一个数组。

`array2`  
第二个数组。

`value_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

<span class="function">array\_udiff\_assoc</span>
返回一个数组，该数组包括了所有在 `array1`
中但是不在任何其它参数数组中的值。注意和 <span
class="function">array\_diff</span> 与 <span
class="function">array\_udiff</span>
不同的是键名也用于比较。数组数据的比较是用用户提供的回调函数进行的。在此方面和
<span class="function">array\_diff\_assoc</span>
的行为正好相反，后者是用内部函数进行比较的。

### 范例

**示例 \#1 <span class="function">array\_udiff\_assoc</span> 例子**

``` php
<?php
class cr {
    private $priv_member;
    function cr($val)
    {
        $this->priv_member = $val;
    }

    static function comp_func_cr($a, $b)
    {
        if ($a->priv_member === $b->priv_member) return 0;
        return ($a->priv_member > $b->priv_member)? 1:-1;
    }
}

$a = array("0.1" => new cr(9), "0.5" => new cr(12), 0 => new cr(23), 1=> new cr(4), 2 => new cr(-15),);
$b = array("0.2" => new cr(9), "0.5" => new cr(22), 0 => new cr(3), 1=> new cr(4), 2 => new cr(-15),);

$result = array_udiff_assoc($a, $b, array("cr", "comp_func_cr"));
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [0.1] => cr Object
            (
                [priv_member:private] => 9
            )

        [0.5] => cr Object
            (
                [priv_member:private] => 12
            )

        [0] => cr Object
            (
                [priv_member:private] => 23
            )
    )

上例中可以看到键值对 *"1" =\> new cr(4)*
同时出现在两个数组中因此不在本函数的输出中。

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_uintersect</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>

array\_udiff\_uassoc
====================

带索引检查计算数组的差集，用回调函数比较数据和索引

### 说明

<span class="type">array</span> <span
class="methodname">array\_udiff\_uassoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$value_compare_func`</span> , <span class="methodparam"><span
class="type">callable</span> `$key_compare_func`</span> )

<span class="function">array\_udiff\_uassoc</span>
返回一个数组，该数组包括了所有在 `array1`
中但是不在任何其它参数数组中的值。

注意和 <span class="function">array\_diff</span> 与 <span
class="function">array\_udiff</span> 不同的是键名也用于比较。

### 参数

`array1`  
第一个数组。

`array2`  
第二个数组。

`value_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

`key_compare_func`  
对键名（索引）的检查也是由回调函数 `key_compare_func` 进行的。这和 <span
class="function">array\_udiff\_assoc</span>
的行为不同，后者是用内部函数比较索引的。

### 返回值

Returns an <span class="type">array</span> containing all the values
from `array1` that are not present in any of the other arguments.

### 范例

**示例 \#1 <span class="function">array\_udiff\_uassoc</span> 例子**

``` php
<?php
class cr {
    private $priv_member;
    function cr($val)
    {
        $this->priv_member = $val;
    }

    static function comp_func_cr($a, $b)
    {
        if ($a->priv_member === $b->priv_member) return 0;
        return ($a->priv_member > $b->priv_member)? 1:-1;
    }

    static function comp_func_key($a, $b)
    {
        if ($a === $b) return 0;
        return ($a > $b)? 1:-1;
    }
}
$a = array("0.1" => new cr(9), "0.5" => new cr(12), 0 => new cr(23), 1=> new cr(4), 2 => new cr(-15),);
$b = array("0.2" => new cr(9), "0.5" => new cr(22), 0 => new cr(3), 1=> new cr(4), 2 => new cr(-15),);

$result = array_udiff_uassoc($a, $b, array("cr", "comp_func_cr"), array("cr", "comp_func_key"));
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [0.1] => cr Object
            (
                [priv_member:private] => 9
            )

        [0.5] => cr Object
            (
                [priv_member:private] => 12
            )

        [0] => cr Object
            (
                [priv_member:private] => 23
            )
    )

在上例中键值对 *"1" =\> new cr(4)*
同时出现在两个数组中，因此不在本函数的输出中。要记住必须提供两个回调函数。

### 注释

> **Note**: <span class="simpara">
> 注意本函数只检查了多维数组中的一维。当然，可以用
> *array\_udiff\_uassoc($array1\[0\], $array2\[0\],
> "data\_compare\_func", "key\_compare\_func");* 来检查更深的维度。
> </span>

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_udiff</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_uintersect</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>

array\_udiff
============

用回调函数比较数据来计算数组的差集

### 说明

<span class="type">array</span> <span
class="methodname">array\_udiff</span> ( <span class="methodparam"><span
class="type">array</span> `$array1`</span> , <span
class="methodparam"><span class="type">array</span> `$array2`</span> \[,
<span class="methodparam"><span class="type">array</span> `$...`</span>
\], <span class="methodparam"><span class="type">callable</span>
`$value_compare_func`</span> )

使用回调函数比较数据，计算数组的不同之处。和 <span
class="function">array\_diff</span>
不同的是，前者使用内置函数进行数据比较。

### 参数

`array1`  
第一个数组。

`array2`  
第二个数组。

`value_compare_func`  
回调对照函数。

在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

返回 `array1` 里没有出现在其他参数里的所有值。

### 范例

**示例 \#1 <span class="function">array\_udiff</span> 使用 stdClass
对象的例子**

``` php
<?php
// Arrays to compare
$array1 = array(new stdclass, new stdclass,
                new stdclass, new stdclass,
               );

$array2 = array(
                new stdclass, new stdclass,
               );

// Set some properties for each object
$array1[0]->width = 11; $array1[0]->height = 3;
$array1[1]->width = 7;  $array1[1]->height = 1;
$array1[2]->width = 2;  $array1[2]->height = 9;
$array1[3]->width = 5;  $array1[3]->height = 7;

$array2[0]->width = 7;  $array2[0]->height = 5;
$array2[1]->width = 9;  $array2[1]->height = 2;

function compare_by_area($a, $b) {
    $areaA = $a->width * $a->height;
    $areaB = $b->width * $b->height;
    
    if ($areaA < $areaB) {
        return -1;
    } elseif ($areaA > $areaB) {
        return 1;
    } else {
        return 0;
    }
}

print_r(array_udiff($array1, $array2, 'compare_by_area'));
?>
```

以上例程会输出：

    Array
    (
        [0] => stdClass Object
            (
                [width] => 11
                [height] => 3
            )

        [1] => stdClass Object
            (
                [width] => 7
                [height] => 1
            )

    )

**示例 \#2 <span class="function">array\_udiff</span> 使用 DateTime
对象的例子**

``` php
<?php
class MyCalendar {
    public $free = array();
    public $booked = array();

    public function __construct($week = 'now') {
        $start = new DateTime($week);
        $start->modify('Monday this week midnight');
        $end = clone $start;
        $end->modify('Friday this week midnight');
        $interval = new DateInterval('P1D');
        foreach (new DatePeriod($start, $interval, $end) as $freeTime) {
            $this->free[] = $freeTime;
        }
    }

    public function bookAppointment(DateTime $date, $note) {
        $this->booked[] = array('date' => $date->modify('midnight'), 'note' => $note);
    }

    public function checkAvailability() {
        return array_udiff($this->free, $this->booked, array($this, 'customCompare'));
    }
    
    public function customCompare($free, $booked) {
        if (is_array($free)) $a = $free['date'];
        else $a = $free;
        if (is_array($booked)) $b = $booked['date'];
        else $b = $booked;
        if ($a == $b) {
            return 0;
        } elseif ($a > $b) {
            return 1;
        } else {
            return -1;
        }
    }
}

// Create a calendar for weekly appointments
$myCalendar = new MyCalendar;

// Book some appointments for this week
$myCalendar->bookAppointment(new DateTime('Monday this week'), "Cleaning GoogleGuy's apartment.");
$myCalendar->bookAppointment(new DateTime('Wednesday this week'), "Going on a snowboarding trip.");
$myCalendar->bookAppointment(new DateTime('Friday this week'), "Fixing buggy code.");

// Check availability of days by comparing $booked dates against $free dates
echo "I'm available on the following days this week...\n\n";
foreach ($myCalendar->checkAvailability() as $free) {
    echo $free->format('l'), "\n"; 
}
echo "\n\n";
echo "I'm busy on the following days this week...\n\n";
foreach ($myCalendar->booked as $booked) {
    echo $booked['date']->format('l'), ": ", $booked['note'], "\n"; 
}
?>
```

以上例程会输出：

    I'm available on the following days this week...

    Tuesday
    Thursday


    I'm busy on the following days this week...

    Monday: Cleaning GoogleGuy's apartment.
    Wednesday: Going on a snowboarding trip.
    Friday: Fixing buggy code.

### 注释

> **Note**: <span class="simpara">
> 注意本函数只检查了多维数组中的一维。当然，可以用
> *array\_udiff($array1\[0\], $array2\[0\], "data\_compare\_func");*
> 来检查更深的维度。 </span>

### 参见

-   <span class="function">array\_diff</span>
-   <span class="function">array\_diff\_assoc</span>
-   <span class="function">array\_diff\_uassoc</span>
-   <span class="function">array\_udiff\_assoc</span>
-   <span class="function">array\_udiff\_uassoc</span>
-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_uintersect</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>

array\_uintersect\_assoc
========================

带索引检查计算数组的交集，用回调函数比较数据

### 说明

<span class="type">array</span> <span
class="methodname">array\_uintersect\_assoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$value_compare_func`</span> )

此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。

注意和 <span class="function">array\_uintersect</span>
不同的是键名也要比较。数据是用回调函数比较的。

### 参数

`array1`  
第一个数组。

`array2`  
第二个数组。

`value_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。

### 范例

**示例 \#1 <span class="function">array\_uintersect\_assoc</span> 例子**

``` php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect_assoc($array1, $array2, "strcasecmp"));
?>
```

以上例程会输出：

    Array
    (
        [a] => green
    )

### 参见

-   <span class="function">array\_uintersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>

array\_uintersect\_uassoc
=========================

带索引检查计算数组的交集，用单独的回调函数比较数据和索引

### 说明

<span class="type">array</span> <span
class="methodname">array\_uintersect\_uassoc</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$value_compare_func`</span> , <span class="methodparam"><span
class="type">callable</span> `$key_compare_func`</span> )

通过额外的索引检查、回调函数比较数据和索引来返回多个数组的交集。

### 参数

`array1`  
第一个数组。

`array2`  
第二个数组。

`value_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

`key_compare_func`  
键名比较的回调函数。

### 返回值

返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。

### 范例

**示例 \#1 <span class="function">array\_uintersect\_uassoc</span>
例子**

``` php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect_uassoc($array1, $array2, "strcasecmp", "strcasecmp"));
?>
```

以上例程会输出：

    Array
    (
        [a] => green
        [b] => brown
    )

### 参见

-   <span class="function">array\_uintersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_intersect\_uassoc</span>
-   <span class="function">array\_uintersect\_assoc</span>

array\_uintersect
=================

计算数组的交集，用回调函数比较数据

### 说明

<span class="type">array</span> <span
class="methodname">array\_uintersect</span> ( <span
class="methodparam"><span class="type">array</span> `$array1`</span> ,
<span class="methodparam"><span class="type">array</span>
`$array2`</span> \[, <span class="methodparam"><span
class="type">array</span> `$...`</span> \], <span
class="methodparam"><span class="type">callable</span>
`$value_compare_func`</span> )

<span class="function">array\_uintersect</span>
返回一个数组，该数组包含了所有在 `array1`
中也同时出现在所有其它参数数组中的值。数据比较是用回调函数进行的。
此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。

### 参数

`array1`  
第一个数组。

`array2`  
第二个数组。

`value_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

Returns an array containing all the values of `array1` that are present
in all the arguments.

### 范例

**示例 \#1 <span class="function">array\_uintersect</span> 例子**

``` php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect($array1, $array2, "strcasecmp"));
?>
```

以上例程会输出：

    Array
    (
        [a] => green
        [b] => brown
        [0] => red
    )

### 参见

-   <span class="function">array\_intersect</span>
-   <span class="function">array\_intersect\_assoc</span>
-   <span class="function">array\_uintersect\_assoc</span>
-   <span class="function">array\_uintersect\_uassoc</span>

array\_unique
=============

移除数组中重复的值

### 说明

<span class="type">array</span> <span
class="methodname">array\_unique</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$sort_flags`<span class="initializer"> = SORT\_STRING</span></span> \]
)

<span class="function">array\_unique</span> 接受 `array`
作为输入并返回没有重复值的新数组。

注意键名保留不变。<span class="function">array\_unique</span>
先将值作为字符串排序，然后对每个值只保留第一个遇到的键名，接着忽略所有后面的键名。这并不意味着在未排序的
`array` 中同一个值的第一个出现的键名会被保留。

> **Note**: <span class="simpara"> 当且仅当 *(string) $elem1 ===
> (string) $elem2* 时两个单元被认为相同。
> 例如，字符串表达一样时，会使用首个元素。 </span>

### 参数

`array`  
输入的数组。

`sort_flags`  
第二个可选参数`sort_flags` 可用于修改排序行为：

排序类型标记：

-   <span class="simpara">**`SORT_REGULAR`** -
    按照通常方法比较（不修改类型）</span>
-   <span class="simpara">**`SORT_NUMERIC`** - 按照数字形式比较</span>
-   <span class="simpara">**`SORT_STRING`** - 按照字符串形式比较</span>
-   <span class="simpara">**`SORT_LOCALE_STRING`** -
    根据当前的本地化设置，按照字符串比较。 </span>

### 返回值

返回过滤后的数组。

### 更新日志

| 版本   | 说明                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------|
| 5.2.10 | 修改回 `sort_flags` 的默认值为 **`SORT_STRING`**。                                                        |
| 5.2.9  | 增加可选选项`sort_flags`，默认值 **`SORT_REGULAR`**。 5.2.9 之前，此函数内部使用 **`SORT_STRING`** 排序。 |

### 范例

**示例 \#1 <span class="function">array\_unique</span> 例子**

``` php
<?php
$input = array("a" => "green", "red", "b" => "green", "blue", "red");
$result = array_unique($input);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [a] => green
        [0] => red
        [1] => blue
    )

**示例 \#2 <span class="function">array\_unique</span> 和类型**

``` php
<?php
$input = array(4, "4", "3", 4, 3, "3");
$result = array_unique($input);
var_dump($result);
?>
```

以上例程会输出：

    array(2) {
      [0] => int(4)
      [2] => string(1) "3"
    }

### 参见

-   <span class="function">array\_count\_values</span>

### 注释

> **Note**: <span class="simpara"> 注意， <span
> class="function">array\_unique</span> 不能应用于多维数组。 </span>

array\_unshift
==============

在数组开头插入一个或多个单元

### 说明

<span class="type">int</span> <span
class="methodname">array\_unshift</span> ( <span
class="methodparam"><span class="type">array</span> `&$array`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\] )

<span class="function">array\_unshift</span> 将传入的单元插入到 `array`
数组的开头。注意单元是作为整体被插入的，因此传入单元将保持同样的顺序。所有的数值键名将修改为从零开始重新计数，所有的文字键名保持不变。

### 参数

`array`  
输入的数组。

`...`  
插入的变量。

### 返回值

返回 `array` 数组新的单元数目。

### 更新日志

| 版本  | 说明                                               |
|-------|----------------------------------------------------|
| 7.3.0 | 现在可以只用一个参数来调用，之前至少需要两个参数。 |

### 范例

**示例 \#1 <span class="function">array\_unshift</span> 例子**

``` php
<?php
$queue = array("orange", "banana");
array_unshift($queue, "apple", "raspberry");
print_r($queue);
?>
```

以上例程会输出：

    Array
    (
        [0] => apple
        [1] => raspberry
        [2] => orange
        [3] => banana
    )

### 参见

-   <span class="function">array\_shift</span>
-   <span class="function">array\_push</span>
-   <span class="function">array\_pop</span>

array\_values
=============

返回数组中所有的值

### 说明

<span class="type">array</span> <span
class="methodname">array\_values</span> ( <span
class="methodparam"><span class="type">array</span> `$array`</span> )

<span class="function">array\_values</span> 返回 `input`
数组中所有的值并给其建立数字索引。

### 参数

`array`  
数组。

### 返回值

返回含所有值的索引数组。

### 范例

**示例 \#1 <span class="function">array\_values</span> 例子**

``` php
<?php
$array = array("size" => "XL", "color" => "gold");
print_r(array_values($array));
?>
```

以上例程会输出：

    Array
    (
        [0] => XL
        [1] => gold
    )

### 参见

-   <span class="function">array\_keys</span>
-   <span class="function">array\_combine</span>

array\_walk\_recursive
======================

对数组中的每个成员递归地应用用户函数

### 说明

<span class="type">bool</span> <span
class="methodname">array\_walk\_recursive</span> ( <span
class="methodparam"><span class="type">array</span> `&$array`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$userdata`<span class="initializer"> =
**`NULL`**</span></span> \] )

将用户自定义函数 `callback` 应用到 `array`
数组中的每个单元。本函数会递归到更深层的数组中去。

### 参数

`array`  
输入的数组。

`callback`  
典型情况下 `callback` 接受两个参数。`array`
参数的值作为第一个，键名作为第二个。

> **Note**:
>
> 如果 `callback` 需要直接作用于数组中的值，则给 `callback`
> 的第一个参数指定为<a href="/language/references.html" class="link">引用</a>。这样任何对这些单元的改变也将会改变原始数组本身。

`userdata`  
如果提供了可选参数 `userdata`，将被作为第三个参数传递给 `callback`。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">array\_walk\_recursive</span> 例子**

``` php
<?php
$sweet = array('a' => 'apple', 'b' => 'banana');
$fruits = array('sweet' => $sweet, 'sour' => 'lemon');

function test_print($item, $key)
{
    echo "$key holds $item\n";
}

array_walk_recursive($fruits, 'test_print');
?>
```

以上例程会输出：

    a holds apple
    b holds banana
    sour holds lemon

注意上例中的键 '*sweet*' 并没有显示出来。任何其值为 <span
class="type">array</span> 的键都不会被传递到回调函数中去。

### 参见

-   <span class="function">array\_walk</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

array\_walk
===========

使用用户自定义函数对数组中的每个元素做回调处理

### 说明

<span class="type">bool</span> <span
class="methodname">array\_walk</span> ( <span class="methodparam"><span
class="type">array</span> `&$array`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$userdata`<span class="initializer"> =
**`NULL`**</span></span> \] )

将用户自定义函数 `funcname` 应用到 `array` 数组中的每个单元。

<span class="function">array\_walk</span> 不会受到 `array`
内部数组指针的影响。<span class="function">array\_walk</span>
会遍历整个数组而不管指针的位置。

### 参数

`array`  
输入的数组。

`callback`  
典型情况下 `callback` 接受两个参数。`array`
参数的值作为第一个，键名作为第二个。

> **Note**:
>
> 如果 `callback` 需要直接作用于数组中的值，则给 `callback`
> 的第一个参数指定为<a href="/language/references.html" class="link">引用</a>。这样任何对这些单元的改变也将会改变原始数组本身。

> **Note**:
>
> 参数数量超过预期，传入内置函数 (例如 <span
> class="function">strtolower</span>)， 将抛出警告，所以不适合当做
> `funcname`。

只有 `array`
的值才可以被改变，用户不应在回调函数中改变该数组本身的结构。例如增加/删除单元，unset
单元等等。如果 <span class="function">array\_walk</span>
作用的数组改变了，则此函数的的行为未经定义，且不可预期。

`userdata`  
如果提供了可选参数 `userdata`，将被作为第三个参数传递给 callback
`funcname`。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

如果 `callback` 函数需要的参数比给出的多，则每次 <span
class="function">array\_walk</span> 调用 `callback` 时都会产生一个
<a href="/errorfunc/constants.html" class="link">E_WARNING</a>
级的错误。

### 范例

**示例 \#1 <span class="function">array\_walk</span> 例子**

``` php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");

function test_alter(&$item1, $key, $prefix)
{
    $item1 = "$prefix: $item1";
}

function test_print($item2, $key)
{
    echo "$key. $item2<br />\n";
}

echo "Before ...:\n";
array_walk($fruits, 'test_print');

array_walk($fruits, 'test_alter', 'fruit');
echo "... and after:\n";

array_walk($fruits, 'test_print');
?>
```

以上例程会输出：

    Before ...:
    d. lemon
    a. orange
    b. banana
    c. apple
    ... and after:
    d. fruit: lemon
    a. fruit: orange
    b. fruit: banana
    c. fruit: apple

### 参见

-   <span class="function">array\_walk\_recursive</span>
-   <span class="function">iterator\_apply</span>
-   <span class="function">list</span>
-   <span class="function">each</span>
-   <span class="function">call\_user\_func\_array</span>
-   <span class="function">array\_map</span>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息
-   <a href="/control-structures/foreach.html" class="link">foreach</a>

array
=====

新建一个数组

### 说明

<span class="type">array</span> <span class="methodname">array</span>
(\[ <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

创建一个数组。关于数组是什么的信息请阅读<a href="/language/types/array.html" class="link">数组</a>一节。

### 参数

`...`  
语法“index =\>
values”，用逗号分开，定义了索引和值。索引可以是字符串或数字。如果省略了索引，会自动产生从
0
开始的整数索引。如果索引是整数，则下一个产生的索引将是目前最大的整数索引 +
1。注意如果定义了两个完全一样的索引，则后面一个会覆盖前一个。

在最后一个定义的数组项目之后加一个逗号虽然不常见，却是合法的语法。

### 返回值

返回根据参数建立的数组。参数可以用 *=\>*
运算符给出索引。关于数组是什么的信息请阅读<a href="/language/types/array.html" class="link">数组</a>一节。

### 范例

下面的例子演示了怎样建立一个二维数组，怎样给相应的数组指定键名，以及怎样在普通数组中略过和继续数字索引。

**示例 \#1 <span class="function">array</span> 例子**

``` php
<?php
$fruits = array (
    "fruits"  => array("a" => "orange", "b" => "banana", "c" => "apple"),
    "numbers" => array(1, 2, 3, 4, 5, 6),
    "holes"   => array("first", 5 => "second", "third")
);
?>
```

**示例 \#2 <span class="function">array</span> 的自动索引**

``` php
<?php
$array = array(1, 1, 1, 1,  1, 8 => 1,  4 => 1, 19, 3 => 13);
print_r($array);
?>
```

以上例程会输出：

    Array
    (
        [0] => 1
        [1] => 1
        [2] => 1
        [3] => 13
        [4] => 1
        [8] => 1
        [9] => 19
    )

注意索引 3 被定义了两次，保留了最后的值 13。索引 4 在 索引 8
之后定义，下一个自动生成的索引（值为 19 那个）为 9，因为最大的索引是 8。

本例建立了从 1 开始的数组。

**示例 \#3 从 1 开始索引的 <span class="function">array</span>**

``` php
<?php
$firstquarter = array(1 => 'January', 'February', 'March');
print_r($firstquarter);
?>
```

以上例程会输出：

    Array
    (
        [1] => January
        [2] => February
        [3] => March
    )

在 Perl 中，可以访问在双引号内的数组的值。但在 PHP
中需要将数组用花括号括起来。

**示例 \#4 访问双引号内的数组**

``` php
<?php

$foo = array('bar' => 'baz');
echo "Hello {$foo['bar']}!"; // Hello baz!

?>
```

### 注释

> **Note**:
>
> <span class="function">array</span>
> 是一个语言结构，用于字面上表示数组，不是常规的函数。

### 参见

-   <span class="function">array\_pad</span>
-   <span class="function">list</span>
-   <span class="function">count</span>
-   <span class="function">range</span>
-   <a href="/control-structures/foreach.html" class="link">foreach</a>
-   The <a href="/language/types/array.html" class="link">array</a> type

arsort
======

对数组进行逆向排序并保持索引关系

### 说明

<span class="type">bool</span> <span class="methodname">arsort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \] )

本函数对数组进行排序，数组的索引保持和单元的关联。

主要用于对那些单元顺序很重要的结合数组进行排序。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的数组。

`sort_flags`  
可以用可选的参数 `sort_flags` 改变排序的行为，详情见 <span
class="function">sort</span>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">arsort</span> 例子**

``` php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
arsort($fruits);
foreach ($fruits as $key => $val) {
    echo "$key = $val\n";
}
?>
```

以上例程会输出：

    a = orange
    d = lemon
    b = banana
    c = apple

fruits 被按照字母顺序逆向排序，并且单元的索引关系不变。

### 参见

-   <span class="function">asort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

asort
=====

对数组进行排序并保持索引关系

### 说明

<span class="type">bool</span> <span class="methodname">asort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \] )

本函数对数组进行排序，数组的索引保持和单元的关联。主要用于对那些单元顺序很重要的结合数组进行排序。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的数组。

`sort_flags`  
可以用可选的参数 `sort_flags` 改变排序的行为，详情见 <span
class="function">sort</span>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">asort</span> 例子**

``` php
<?php
$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");
asort($fruits);
foreach ($fruits as $key => $val) {
    echo "$key = $val\n";
}
?>
```

以上例程会输出：

    c = apple
    b = banana
    d = lemon
    a = orange

fruits 被按照字母顺序排序，并且单元的索引关系不变。

### 参见

-   <span class="function">arsort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

compact
=======

建立一个数组，包括变量名和它们的值

### 说明

<span class="type">array</span> <span class="methodname">compact</span>
( <span class="methodparam"><span class="type">mixed</span>
`$varname1`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \] )

创建一个包含变量与其值的数组。

对每个参数，<span class="function">compact</span>
在当前的符号表中查找该变量名并将它添加到输出的数组中，变量名成为键名而变量的内容成为该键的值。简单说，它做的事和
<span class="function">extract</span>
正好相反。返回将所有变量添加进去后的数组。

> **Note**:
>
> 在 PHP 7.3 之前版本，未设置的字符串会被静默忽略。

### 参数

`varname1`  
<span class="function">compact</span>
接受可变的参数数目。每个参数可以是一个包括变量名的字符串或者是一个包含变量名的数组，该数组中还可以包含其它单元内容为变量名的数组，
<span class="function">compact</span> 可以递归处理。

### 返回值

返回输出的数组，包含了添加的所有变量。

### 错误／异常

如果字符串指向的变量未定义，<span class="function">compact</span> 会产生
E\_NOTICE 级错误。

### 更新日志

| 版本  | 说明                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| 7.3.0 | 现在，如果字符串指向的变量未定义，<span class="function">compact</span> 会产生 E\_NOTICE 级错误。 在此之前，此类问题会静默忽略掉。 |

### 范例

**示例 \#1 <span class="function">compact</span> 例子**

``` php
<?php
$city  = "San Francisco";
$state = "CA";
$event = "SIGGRAPH";

$location_vars = array("city", "state");

$result = compact("event", "nothing_here", $location_vars);
print_r($result);
?>
```

以上例程会输出：

    Array
    (
        [event] => SIGGRAPH
        [city] => San Francisco
        [state] => CA
    )

### 注释

> **Note**: **Gotcha**  
>
> 因为<a href="/language/variables/variable.html" class="link">可变变量</a>也许不能在函数内部用于
> PHP
> 的<a href="/language/variables/superglobals.html" class="link">超全局数组</a>，此时不能将超全局数组传递入
> <span class="function">compact</span> 中。

### 参见

-   <span class="function">extract</span>

count
=====

计算数组中的单元数目，或对象中的属性个数

### 说明

<span class="type">int</span> <span class="methodname">count</span> (
<span class="methodparam"><span class="type">mixed</span>
`$array_or_countable`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
COUNT\_NORMAL</span></span> \] )

统计出数组里的所有元素的数量，或者对象里的东西。

对于对象，如果安装了
<a href="/ref/spl.html" class="link">SPL</a>，可以通过实现 *Countable*
接口对 <span class="function">count</span>挂钩（hook）
。该接口只有一个方法 <span
class="methodname">Countable::count</span>，此方法为 <span
class="function">count</span> 函数返回值。

关于 PHP
中如何实现和使用数组可以参考手册中<a href="/language/types/array.html" class="link">数组</a>章节中的详细描述。

### 参数

`array_or_countable`  
数组或者 <span class="classname">Countable</span> 对象。

`mode`  
如果可选的 `mode` 参数设为 **`COUNT_RECURSIVE`**（或 1），<span
class="function">count</span>
将递归地对数组计数。对计算多维数组的所有单元尤其有用。

**Caution**
<span class="function">count</span>
能检测递归来避免无限循环，但每次出现时会产生 **`E_WARNING`** 错误 （如果
array 不止一次包含了自身）并返回大于预期的统计数字。

### 返回值

返回 `array_or_countable` 中的单元数目。 如果参数既不是数组，也不是实现
*Countable* 接口的对象，将返回 *1*。 有个例外：如果 `array_or_countable`
是 **`NULL`** 则结果是 *0*。

### 范例

**示例 \#1 <span class="function">count</span> 例子**

``` php
<?php
$a[0] = 1;
$a[1] = 3;
$a[2] = 5;
var_dump(count($a));

$b[0]  = 7;
$b[5]  = 9;
$b[10] = 11;
var_dump(count($b));

var_dump(count(null));

var_dump(count(false));
?>
```

以上例程会输出：

    int(3)
    int(3)

    Warning: count(): Parameter must be an array or an object that implements Countable in … on line 12 // PHP 7.2 起
    int(0)

    Warning: count(): Parameter must be an array or an object that implements Countable in … on line 14 // PHP 7.2 起
    int(1)

**示例 \#2 递归 <span class="function">count</span> 例子**

``` php
<?php
$food = array('fruits' => array('orange', 'banana', 'apple'),
              'veggie' => array('carrot', 'collard', 'pea'));

// recursive count
echo count($food, COUNT_RECURSIVE); // output 8

// normal count
echo count($food); // output 2

?>
```

### 更新日志

| 版本  | 说明                                                                                                        |
|-------|-------------------------------------------------------------------------------------------------------------|
| 7.2.0 | 当无效的 countable 类型传递给 `array_or_countable` 参数时，<span class="function">count</span> 会产生警告。 |

### 参见

-   <span class="function">is\_array</span>
-   <span class="function">isset</span>
-   <span class="function">empty</span>
-   <span class="function">strlen</span>
-   <span class="function">is\_countable</span>

current
=======

返回数组中的当前单元

### 说明

<span class="type">mixed</span> <span class="methodname">current</span>
( <span class="methodparam"><span class="type">array</span>
`&$array`</span> )

每个数组中都有一个内部的指针指向它“当前的”单元，初始指向插入到数组中的第一个单元。

### 参数

`array`  
这个数组。

### 返回值

<span class="function">current</span>
函数返回当前被内部指针指向的数组单元的值，并不移动指针。如果内部指针指向超出了单元列表的末端，<span
class="function">current</span> 返回 **`FALSE`**。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 使用 <span class="function">current</span> 系列函数的例子**

``` php
<?php
$transport = array('foot', 'bike', 'car', 'plane');
$mode = current($transport); // $mode = 'foot';
$mode = next($transport);    // $mode = 'bike';
$mode = current($transport); // $mode = 'bike';
$mode = prev($transport);    // $mode = 'foot';
$mode = end($transport);     // $mode = 'plane';
$mode = current($transport); // $mode = 'plane';

$arr = array();
var_dump(current($arr)); // bool(false)

$arr = array(array());
var_dump(current($arr)); // array(0) { }
?>
```

### 注释

> **Note**: <span class="simpara"> 如果数组包含 <span
> class="type">boolean</span> **`FALSE`**
> 的单元则本函数在碰到这个单元时也返回
> **`FALSE`**，使得不可能判断是否到了此数组列表的末端。
> 要正确遍历可能含有空单元的数组，用 <span class="function">each</span>
> 函数。 </span>

### 参见

-   <span class="function">end</span>
-   <span class="function">key</span>
-   <span class="function">each</span>
-   <span class="function">prev</span>
-   <span class="function">reset</span>
-   <span class="function">next</span>

each
====

返回数组中当前的键／值对并将数组指针向前移动一步

**Warning**

本函数已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">array</span> <span class="methodname">each</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

返回数组中当前的键／值对并将数组指针向前移动一步

在执行 <span class="function">each</span>
之后，数组指针将停留在数组中的下一个单元或者当碰到数组结尾时停留在最后一个单元。如果要再用
each 遍历数组，必须使用 <span class="function">reset</span>。

### 参数

`array`  
输入的数组。

### 返回值

返回 `array`
数组中当前指针位置的键／值对并向前移动数组指针。键值对被返回为四个单元的数组，键名为*0*，*1*，*key*和
*value*。单元 *0* 和 *key* 包含有数组单元的键名，*1* 和 *value*
包含有数据。

如果内部指针越过了数组的末端，则 <span class="function">each</span> 返回
**`FALSE`**。

### 范例

**示例 \#1 <span class="function">each</span> 例子**

``` php
<?php
$foo = array("bob", "fred", "jussi", "jouni", "egon", "marliese");
$bar = each($foo);
print_r($bar);
?>
```

`$bar` 现在包含有如下的键／值对：

    Array
    (
        [1] => bob
        [value] => bob
        [0] => 0
        [key] => 0
    )

``` php
<?php
$foo = array("Robert" => "Bob", "Seppo" => "Sepi");
$bar = each($foo);
print_r($bar);
?>
```

`$bar` 现在包含有如下的键／值对：

    Array
    (
        [1] => Bob
        [value] => Bob
        [0] => Robert
        [key] => Robert
    )

<span class="function">each</span> 经常和 <span
class="function">list</span> 结合使用来遍历数组，例如：

**示例 \#2 用 <span class="function">each</span> 遍历数组**

``` php
<?php
$fruit = array('a' => 'apple', 'b' => 'banana', 'c' => 'cranberry');

reset($fruit);
while (list($key, $val) = each($fruit)) {
    echo "$key => $val\n";
}
?>
```

以上例程会输出：

    a => apple
    b => banana
    c => cranberry

**Caution**

因为将一个数组赋值给另一个数组时会重置原来的数组指针，因此在上边的例子中如果我们在循环内部将
`$fruit` 赋给了另一个变量的话将会导致无限循环。

**Warning**

<span class="function">each</span> will also accept objects, but may
return unexpected results. Its therefore not recommended to iterate
though object properties with <span class="function">each</span>.

### 参见

-   <span class="function">key</span>
-   <span class="function">list</span>
-   <span class="function">current</span>
-   <span class="function">reset</span>
-   <span class="function">next</span>
-   <span class="function">prev</span>
-   <a href="/control-structures/foreach.html" class="link">foreach</a>
-   <a href="/language/oop5/iterations.html" class="link">Object Iteration</a>

end
===

将数组的内部指针指向最后一个单元

### 说明

<span class="type">mixed</span> <span class="methodname">end</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

<span class="function">end</span> 将 `array`
的内部指针移动到最后一个单元并返回其值。

### 参数

`array`  
这个数组。 该数组是通过引用传递的，因为它会被这个函数修改。
这意味着你必须传入一个真正的变量，而不是函数返回的数组，因为只有真正的变量才能以引用传递。

### 返回值

返回最后一个元素的值，或者如果是空数组则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">end</span> 例子**

``` php
<?php

$fruits = array('apple', 'banana', 'cranberry');
echo end($fruits); // cranberry

?>
```

### 参见

-   <span class="function">current</span>
-   <span class="function">each</span>
-   <span class="function">prev</span>
-   <span class="function">reset</span>
-   <span class="function">next</span>

extract
=======

从数组中将变量导入到当前的符号表

### 说明

<span class="type">int</span> <span class="methodname">extract</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
EXTR\_OVERWRITE</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$prefix`<span class="initializer"> =
**`NULL`**</span></span> \]\] )

本函数用来将变量从数组中导入到当前的符号表中。

检查每个键名看是否可以作为一个合法的变量名，同时也检查和符号表中已有的变量名的冲突。

### 参数

`array`  
一个关联数组。此函数会将键名当作变量名，值作为变量的值。
对每个键／值对都会在当前的符号表中建立变量，并受到 `flags` 和 `prefix`
参数的影响。

必须使用关联数组，数字索引的数组将不会产生结果，除非用了
**`EXTR_PREFIX_ALL`** 或者 **`EXTR_PREFIX_INVALID`**。

`flags`  
对待非法／数字和冲突的键名的方法将根据取出标记 `flags`
参数决定。可以是以下值之一：

**`EXTR_OVERWRITE`**  
<span class="simpara"> 如果有冲突，覆盖已有的变量。 </span>

**`EXTR_SKIP`**  
<span class="simpara"> 如果有冲突，不覆盖已有的变量。 </span>

**`EXTR_PREFIX_SAME`**  
<span class="simpara">如果有冲突，在变量名前加上前缀 `prefix`。 </span>

**`EXTR_PREFIX_ALL`**  
<span class="simpara"> 给所有变量名加上前缀 `prefix`。 </span>

**`EXTR_PREFIX_INVALID`**  
<span class="simpara"> 仅在非法／数字的变量名前加上前缀 `prefix`。
</span>

**`EXTR_IF_EXISTS`**  
<span class="simpara">
仅在当前符号表中已有同名变量时，覆盖它们的值。其它的都不处理。
举个例子，以下情况非常有用：定义一些有效变量，然后从 `$_REQUEST`
中仅导入这些已定义的变量。 </span>

**`EXTR_PREFIX_IF_EXISTS`**  
<span class="simpara">
仅在当前符号表中已有同名变量时，建立附加了前缀的变量名，其它的都不处理。
</span>

**`EXTR_REFS`**  
<span class="simpara">
将变量作为引用提取。这有力地表明了导入的变量仍然引用了 `array`
参数的值。可以单独使用这个标志或者在 `flags` 中用 OR
与其它任何标志结合使用。 </span>

如果没有指定 `flags`，则被假定为 **`EXTR_OVERWRITE`**。

`prefix`  
注意 `prefix` 仅在 `flags` 的值是
**`EXTR_PREFIX_SAME`**，**`EXTR_PREFIX_ALL`**，**`EXTR_PREFIX_INVALID`**
或 **`EXTR_PREFIX_IF_EXISTS`** 时需要。
如果附加了前缀后的结果不是合法的变量名，将不会导入到符号表中。前缀和数组键名之间会自动加上一个下划线。

### 返回值

返回成功导入到符号表中的变量数目。

### 范例

**示例 \#1 <span class="function">extract</span> 例子**

<span class="function">extract</span> 的一种可能用法是将 <span
class="function">wddx\_deserialize</span>
返回的结合数组中的内容导入到符号表变量中去。

``` php
<?php

/* 假定 $var_array 是 wddx_deserialize 返回的数组*/

$size = "large";
$var_array = array("color" => "blue",
                   "size"  => "medium",
                   "shape" => "sphere");
extract($var_array, EXTR_PREFIX_SAME, "wddx");

echo "$color, $size, $shape, $wddx_size\n";

?>
```

以上例程会输出：

    blue, large, sphere, medium

`$size` 没有被覆盖，因为指定了 **`EXTR_PREFIX_SAME`**，这使得
`$wddx_size` 被建立。如果指定了 **`EXTR_SKIP`**，则 `$wddx_size`
也不会被建立。**`EXTR_OVERWRITE`** 将使 `$size`
的值为“medium”，**`EXTR_PREFIX_ALL`** 将建立新变量
`$wddx_color`，`$wddx_size` 和 `$wddx_shape`。

### 注释

**Warning**

不要对不能信任的数据使用 <span
class="function">extract</span>，例如用户的输入（`$_GET`，
`$_FILES`，...）。如果这样做，举例说，要临时运行依赖于
<a href="/security/globals.html" class="link">register_globals</a>
的老代码，要确保使用不会覆盖的 `extract_type` 值，例如
**`EXTR_SKIP`**，并且要留意应该按照
<a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
在
<a href="/ini.html" class="link"><var class="filename">php.ini</var></a>
里 定义的顺序来提取。

> **Note**:
>
> If you still have
> <a href="/security/globals.html" class="link">register_globals</a> and
> it is turned on, if you use <span class="function">extract</span> on
> `$_FILES` and specify **`EXTR_SKIP`**, you may be surprised at the
> results.
>
> **Warning**
>
> This is not recommended practice and is only documented here for
> completeness. The use of
> <a href="/security/globals.html" class="link">register_globals</a> is
> deprecated and calling <span class="function">extract</span> on
> untrusted data such as `$_FILES` is, as noted above, a potential
> security risk. If you encounter this issue, it means that you are
> using at least two poor coding practices.
>
> ``` php
> <?php
>
> /* Suppose that $testfile is the name of a file upload input
>    and that register_globals is turned on. */
>
> var_dump($testfile);
> extract($_FILES, EXTR_SKIP);
> var_dump($testfile);
> var_dump($testfile['tmp_name']);
>
> ?>
> ```
>
> <span class="simpara"> You might expect to see something like the
> following: </span>
>
>     string(14) "/tmp/phpgCCPX8"
>     array(5) {
>       ["name"]=>
>       string(10) "somefile.txt"
>       ["type"]=>
>       string(24) "application/octet-stream"
>       ["tmp_name"]=>
>       string(14) "/tmp/phpgCCPX8"
>       ["error"]=>
>       int(0)
>       ["size"]=>
>       int(4208)
>     }
>     string(14) "/tmp/phpgCCPX8"
>
> <span class="simpara"> However, you would instead see something like
> this: </span>
>
>     string(14) "/tmp/phpgCCPX8"
>     string(14) "/tmp/phpgCCPX8"
>     string(1) "/"
>
> This is due to the fact that since
> <a href="/security/globals.html" class="link">register_globals</a> is
> turned on, `$testfile` already exists in the global scope when <span
> class="function">extract</span> is called. And since **`EXTR_SKIP`**
> is specified, `$testfile` is not overwritten with the contents of the
> **`$_FILES`** array so `$testfile` remains a string. Because
> <a href="/language/types/string.html#language.types.string.substr" class="link">strings may be accessed using array syntax</a>
> and the non-numeric string *tmp\_name* is interpreted as *0*, PHP sees
> `$testfile['tmp_name']` as `$testfile[0]`.

### 参见

-   <span class="function">compact</span>
-   <span class="function">list</span>

in\_array
=========

检查数组中是否存在某个值

### 说明

<span class="type">bool</span> <span class="methodname">in\_array</span>
( <span class="methodparam"><span class="type">mixed</span>
`$needle`</span> , <span class="methodparam"><span
class="type">array</span> `$haystack`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$strict`<span
class="initializer"> = **`FALSE`**</span></span> \] )

大海捞针，在大海（`haystack`）中搜索针（ `needle`），如果没有设置
`strict` 则使用宽松的比较。

### 参数

`needle`  
待搜索的值。

> **Note**:
>
> 如果 `needle` 是字符串，则比较是区分大小写的。

`haystack`  
待搜索的数组。

`strict`  
如果第三个参数 `strict` 的值为 **`TRUE`** 则 <span
class="function">in\_array</span> 函数还会检查 `needle`
的<a href="/language/types.html" class="link">类型</a>是否和 `haystack`
中的相同。

### 返回值

如果找到 `needle` 则返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">in\_array</span> 例子**

``` php
<?php
$os = array("Mac", "NT", "Irix", "Linux");
if (in_array("Irix", $os)) {
    echo "Got Irix";
}
if (in_array("mac", $os)) {
    echo "Got mac";
}
?>
```

第二个条件失败，因为 <span class="function">in\_array</span>
是区分大小写的，所以以上程序显示为：

    Got Irix

**示例 \#2 <span class="function">in\_array</span> 严格类型检查例子**

``` php
<?php
$a = array('1.10', 12.4, 1.13);

if (in_array('12.4', $a, true)) {
    echo "'12.4' found with strict check\n";
}

if (in_array(1.13, $a, true)) {
    echo "1.13 found with strict check\n";
}
?>
```

以上例程会输出：

    1.13 found with strict check

**示例 \#3 <span class="function">in\_array</span> 中用数组作为 needle**

``` php
<?php
$a = array(array('p', 'h'), array('p', 'r'), 'o');

if (in_array(array('p', 'h'), $a)) {
    echo "'ph' was found\n";
}

if (in_array(array('f', 'i'), $a)) {
    echo "'fi' was found\n";
}

if (in_array('o', $a)) {
    echo "'o' was found\n";
}
?>
```

以上例程会输出：

      'ph' was found
      'o' was found

### 参见

-   <span class="function">array\_search</span>
-   <span class="function">isset</span>
-   <span class="function">array\_key\_exists</span>

key\_exists
===========

别名 <span class="function">array\_key\_exists</span>

### 说明

此函数是该函数的别名： <span class="function">array\_key\_exists</span>.

key
===

从关联数组中取得键名

### 说明

<span class="type">mixed</span> <span class="methodname">key</span> (
<span class="methodparam"><span class="type">array</span>
`$array`</span> )

<span class="function">key</span> 返回数组中当前单元的键名。

### 参数

`array`  
该数组。

### 返回值

<span class="function">key</span>
函数返回数组中内部指针指向的当前单元的键名。
但它不会移动指针。如果内部指针超过了元素列表尾部，或者数组是空的，<span
class="function">key</span> 会返回 **`NULL`**。

### 更新日志

| 版本  | 说明                                                              |
|-------|-------------------------------------------------------------------|
| 7.0.0 | `array` 现在总是会传值。 在此之前，它会尽可能传引用，否则就传值。 |

### 范例

**示例 \#1 <span class="function">key</span> 例子**

``` php
<?php
$array = array(
    'fruit1' => 'apple',
    'fruit2' => 'orange',
    'fruit3' => 'grape',
    'fruit4' => 'apple',
    'fruit5' => 'apple');

// this cycle echoes all associative array
// key where value equals "apple"
while ($fruit_name = current($array)) {
    if ($fruit_name == 'apple') {
        echo key($array).'<br />';
    }
    next($array);
}
?>
```

以上例程会输出：

    fruit1<br />
    fruit4<br />
    fruit5<br />

### 参见

-   <span class="function">current</span>
-   <span class="function">next</span>
-   <a href="/control-structures/foreach.html" class="link">foreach</a>

krsort
======

对数组按照键名逆向排序

### 说明

<span class="type">bool</span> <span class="methodname">krsort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \] )

对数组按照键名逆向排序，保留键名到数据的关联。主要用于结合数组。

### 参数

`array`  
输入的数组。

`sort_flags`  
可以用可选参数 `sort_flags` 改变排序的行为，详情见 <span
class="function">sort</span>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">krsort</span> 例子**

``` php
<?php
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");
krsort($fruits);
foreach ($fruits as $key => $val) {
    echo "$key = $val\n";
}
?>
```

以上例程会输出：

    d = lemon
    c = apple
    b = banana
    a = orange

### 参见

-   <span class="function">arsort</span>
-   <span class="function">ksort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

ksort
=====

对数组按照键名排序

### 说明

<span class="type">bool</span> <span class="methodname">ksort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \] )

对数组按照键名排序，保留键名到数据的关联。本函数主要用于关联数组。

### 参数

`array`  
输入的数组。

`sort_flags`  
可以用可选参数 `sort_flags` 改变排序的行为，详情见 <span
class="function">sort</span>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ksort</span> 例子**

``` php
<?php
$fruits = array("d"=>"lemon", "a"=>"orange", "b"=>"banana", "c"=>"apple");
ksort($fruits);
foreach ($fruits as $key => $val) {
    echo "$key = $val\n";
}
?>
```

以上例程会输出：

    a = orange
    b = banana
    c = apple
    d = lemon

### 参见

-   <span class="function">asort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

list
====

把数组中的值赋给一组变量

### 说明

<span class="type">array</span> <span class="methodname">list</span> (
<span class="methodparam"><span class="type">mixed</span> `$var1`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

像 <span class="function">array</span>
一样，这不是真正的函数，而是语言结构。 <span
class="function">list</span> 可以在单次操作内就为一组变量赋值。

> **Note**:
>
> 在 PHP 7.1.0 之前的版本，<span class="function">list</span>
> 仅能用于数字索引的数组，并假定数字索引从 0 开始。

**Warning**

PHP 5 里，<span class="function">list</span> 从最右边的参数开始赋值；
PHP 7 里，<span class="function">list</span> 从最左边的参数开始赋值。

如果你用单纯的变量，不用担心这一点。
但是如果你用了具有索引的数组，通常你期望得到的结果和在 <span
class="function">list</span> 中写的一样是从左到右的，但在 PHP 5
里实际上不是， 它是以相反顺序赋值的。

通常而言，不建议依赖于操作的顺序，在未来可能会再次发生修改。

### 参数

`var1`  
一个变量。

### 返回值

返回指定的数组。

### 更新日志

| 版本  | 说明                                                                                            |
|-------|-------------------------------------------------------------------------------------------------|
| 7.3.0 | 支持在数组解构时传引用。                                                                        |
| 7.1.0 | 现在可以指定 <span class="function">list</span> 中的键。 这就可以解构非数字键或者无顺序的数组。 |
| 7.0.0 | 赋值操作的顺序发生了变化。                                                                      |
| 7.0.0 | <span class="function">list</span> 表达式不再可以完全为空。                                     |
| 7.0.0 | 字符串无法再被拆包（unpack）。                                                                  |

### 范例

**示例 \#1 <span class="function">list</span> 例子**

``` php
<?php

$info = array('coffee', 'brown', 'caffeine');

// 列出所有变量
list($drink, $color, $power) = $info;
echo "$drink is $color and $power makes it special.\n";

// 列出他们的其中一个
list($drink, , $power) = $info;
echo "$drink has $power.\n";

// 或者让我们跳到仅第三个
list( , , $power) = $info;
echo "I need $power!\n";

// list() 不能对字符串起作用
list($bar) = "abcde";
var_dump($bar); // NULL
?>
```

**示例 \#2 <span class="function">list</span> 用法的一个例子**

``` php
<table>
 <tr>
  <th>Employee name</th>
  <th>Salary</th>
 </tr>

<?php

$result = $pdo->query("SELECT id, name, salary FROM employees");
while (list($id, $name, $salary) = $result->fetch(PDO::FETCH_NUM)) {
    echo " <tr>\n" .
          "  <td><a href=\"info.php?id=$id\">$name</a></td>\n" .
          "  <td>$salary</td>\n" .
          " </tr>\n";
}


?>

</table>
```

**示例 \#3 使用嵌套的 <span class="function">list</span>**

``` php
<?php

list($a, list($b, $c)) = array(1, array(2, 3));

var_dump($a, $b, $c);

?>
```

    int(1)
    int(2)
    int(3)

**示例 \#4 在 <span class="function">list</span> 中使用数组索引**

``` php
<?php

$info = array('coffee', 'brown', 'caffeine');

list($a[0], $a[1], $a[2]) = $info;

var_dump($a);

?>
```

产生如下输出（注意单元顺序和 <span class="function">list</span>
语法中所写的顺序的比较）：

以上例程在 PHP 7 中的输出：

    array(3) {
      [0]=>
      string(6) "coffee"
      [1]=>
      string(5) "brown"
      [2]=>
      string(8) "caffeine"
    }

以上例程在 PHP 5 中的输出：

    array(3) {
      [2]=>
      string(8) "caffeine"
      [1]=>
      string(5) "brown"
      [0]=>
      string(6) "coffee"
    }

**示例 \#5 <span class="function">list</span> 和索引顺序定义**

<span class="function">list</span> 使用 array
索引的顺序和它何时定义无关。

``` php
<?php
$foo = array(2 => 'a', 'foo' => 'b', 0 => 'c');
$foo[1] = 'd';
list($x, $y, $z) = $foo;
var_dump($foo, $x, $y, $z);
```

得到以下输出（注意比较 <span class="function">list</span>
所写的元素顺序）：

    array(4) {
      [2]=>
      string(1) "a"
      ["foo"]=>
      string(1) "b"
      [0]=>
      string(1) "c"
      [1]=>
      string(1) "d"
    }
    string(1) "c"
    string(1) "d"
    string(1) "a"

**示例 \#6 带键的 <span class="function">list</span>**

从 PHP 7.1.0 开始，<span class="function">list</span>
可以包含显式的键，可赋值到任意表达式。
可以混合使用数字和字符串键。但是不能混合有键和无键不能混用。

``` php
<?php
$data = [
    ["id" => 1, "name" => 'Tom'],
    ["id" => 2, "name" => 'Fred'],
];
foreach ($data as ["id" => $id, "name" => $name]) {
    echo "id: $id, name: $name\n";
}
echo PHP_EOL;
list(1 => $second, 3 => $fourth) = [1, 2, 3, 4];
echo "$second, $fourth\n";
```

以上例程会输出：

    id: 1, name: Tom
    id: 2, name: Fred

    2, 4

### 参见

-   <span class="function">each</span>
-   <span class="function">array</span>
-   <span class="function">extract</span>

natcasesort
===========

用“自然排序”算法对数组进行不区分大小写字母的排序

### 说明

<span class="type">bool</span> <span
class="methodname">natcasesort</span> ( <span class="methodparam"><span
class="type">array</span> `&$array`</span> )

<span class="function">natcasesort</span> 是 <span
class="function">natsort</span> 函数的不区分大小写字母的版本。

本函数实现了一个和人们通常对字母数字字符串进行排序的方法一样的排序算法并保持原有键／值的关联，这被称为“自然排序”。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的数组。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">natcasesort</span> 例子**

``` php
<?php
$array1 = $array2 = array('IMG0.png', 'img12.png', 'img10.png', 'img2.png', 'img1.png', 'IMG3.png');

sort($array1);
echo "Standard sorting\n";
print_r($array1);

natcasesort($array2);
echo "\nNatural order sorting (case-insensitive)\n";
print_r($array2);
?>
```

以上例程会输出：

    Standard sorting
    Array
    (
        [0] => IMG0.png
        [1] => IMG3.png
        [2] => img1.png
        [3] => img10.png
        [4] => img12.png
        [5] => img2.png
    )

    Natural order sorting (case-insensitive)
    Array
    (
        [0] => IMG0.png
        [4] => img1.png
        [3] => img2.png
        [5] => IMG3.png
        [2] => img10.png
        [1] => img12.png
    )

更多信息见 Martin Pool 的
<a href="http://sourcefrog.net/projects/natsort/" class="link external">» Natural Order String Comparison</a>
页面。

### 参见

-   <span class="function">natsort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>
-   <span class="function">strnatcmp</span>
-   <span class="function">strnatcasecmp</span>

natsort
=======

用“自然排序”算法对数组排序

### 说明

<span class="type">bool</span> <span class="methodname">natsort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

本函数实现了一个和人们通常对字母数字字符串进行排序的方法一样的排序算法并保持原有键／值的关联，这被称为“自然排序”。本算法和通常的计算机字符串排序算法（用于
<span class="function">sort</span>）的区别见下面示例。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的 array。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本   | 说明                                                                |
|--------|---------------------------------------------------------------------|
| 5.2.10 | 用零填充的数字字符串 (例如 '00005')现在本质上会忽略掉填充的前道零。 |

### 范例

**示例 \#1 <span class="function">natsort</span> 基本用法的操作示例**

``` php
<?php
$array1 = $array2 = array("img12.png", "img10.png", "img2.png", "img1.png");

asort($array1);
echo "Standard sorting\n";
print_r($array1);

natsort($array2);
echo "\nNatural order sorting\n";
print_r($array2);
?>
```

以上例程会输出：

    Standard sorting
    Array
    (
        [3] => img1.png
        [1] => img10.png
        [0] => img12.png
        [2] => img2.png
    )

    Natural order sorting
    Array
    (
        [3] => img1.png
        [2] => img2.png
        [1] => img10.png
        [0] => img12.png
    )

For more information see: Martin Pool's
<a href="http://sourcefrog.net/projects/natsort/" class="link external">» Natural Order String Comparison</a>
page.

**示例 \#2 <span class="function">natsort</span> examples demonstrating
potential gotchas**

``` php
<?php
echo "Negative numbers\n";
$negative = array('-5','3','-2','0','-1000','9','1');
print_r($negative);
natsort($negative);
print_r($negative);

echo "Zero padding\n";
$zeros = array('09', '8', '10', '009', '011', '0'); 
print_r($zeros);
natsort($zeros);
print_r($zeros);
?>
```

以上例程会输出：

    Negative numbers
    Array
    (
        [0] => -5
        [1] => 3
        [2] => -2
        [3] => 0
        [4] => -1000
        [5] => 9
        [6] => 1
    )
    Array
    (
        [2] => -2
        [0] => -5
        [4] => -1000
        [3] => 0
        [6] => 1
        [1] => 3
        [5] => 9
    )

    Zero padding
    Array
    (
        [0] => 09
        [1] => 8
        [2] => 10
        [3] => 009
        [4] => 011
        [5] => 0
    )
    Array
    (
        [5] => 0
        [1] => 8
        [3] => 009
        [0] => 09
        [2] => 10
        [4] => 011
    )

### 参见

-   <span class="function">natcasesort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>
-   <span class="function">strnatcmp</span>
-   <span class="function">strnatcasecmp</span>

next
====

将数组中的内部指针向前移动一位

### 说明

<span class="type">mixed</span> <span class="methodname">next</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

<span class="function">next</span> 和 <span
class="function">current</span>
的行为类似，只有一点区别，在返回值之前将内部指针向前移动一位。这意味着它返回的是下一个数组单元的值并将数组指针向前移动了一位。

### 参数

`array`  
受影响的 <span class="type">array</span> 。

### 返回值

返回数组内部指针指向的下一个单元的值，或当没有更多单元时返回
**`FALSE`**。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 <span class="function">next</span> 及相关函数的用法示例**

``` php
<?php
$transport = array('foot', 'bike', 'car', 'plane');
$mode = current($transport); // $mode = 'foot';
$mode = next($transport);    // $mode = 'bike';
$mode = next($transport);    // $mode = 'car';
$mode = prev($transport);    // $mode = 'bike';
$mode = end($transport);     // $mode = 'plane';
?>
```

### 注释

> **Note**: <span class="simpara"> 你将无法区别包含数组尾以及 <span
> class="type">boolean</span> **`FALSE`**
> 单元的数组。要正确遍历可能含有空单元或者单元值为 0 的数组，参见 <span
> class="function">each</span> 函数。 </span>

### 参见

-   <span class="function">current</span>
-   <span class="function">end</span>
-   <span class="function">prev</span>
-   <span class="function">reset</span>
-   <span class="function">each</span>

pos
===

<span class="function">current</span> 的别名

### 说明

此函数是该函数的别名：<span class="function">current</span>。

prev
====

将数组的内部指针倒回一位

### 说明

<span class="type">mixed</span> <span class="methodname">prev</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

将数组的内部指针倒回一位。

<span class="function">prev</span> 和 <span class="function">next</span>
的行为类似，只除了它将内部指针倒回一位而不是前移一位。

### 参数

`array`  
The input array.

### 返回值

返回数组内部指针指向的前一个单元的值，或当没有更多单元时返回
**`FALSE`**。

### 范例

**示例 \#1 <span class="function">prev</span> 及相关函数用法示例**

``` php
<?php
$transport = array('foot', 'bike', 'car', 'plane');
$mode = current($transport); // $mode = 'foot';
$mode = next($transport);    // $mode = 'bike';
$mode = next($transport);    // $mode = 'car';
$mode = prev($transport);    // $mode = 'bike';
$mode = end($transport);     // $mode = 'plane';
?>
```

### 注释

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

> **Note**: <span class="simpara"> 你会无法区分包含 <span
> class="type">boolean</span> **`FALSE`**
> 单元的数组开头。要正确遍历可能含有空单元或者单元值为 0 的数组，参见
> <span class="function">each</span> 函数。 </span>

### 参见

-   <span class="function">current</span>
-   <span class="function">end</span>
-   <span class="function">next</span>
-   <span class="function">reset</span>
-   <span class="function">each</span>

range
=====

根据范围创建数组，包含指定的元素

### 说明

<span class="type">array</span> <span class="methodname">range</span> (
<span class="methodparam"><span class="type">mixed</span>
`$start`</span> , <span class="methodparam"><span
class="type">mixed</span> `$end`</span> \[, <span
class="methodparam"><span class="type">number</span> `$step`<span
class="initializer"> = 1</span></span> \] )

建立一个包含指定范围单元的数组。

### 参数

`start`  
序列的第一个值。

`end`  
序列结束于 `end` 的值。

`step`  
如果设置了步长 `step`，会被作为单元之间的步进值。`step`
应该为正值。不设置`step` 则默认为 1。

### 返回值

返回的数组中从 `start` 到 `end` （含 start 和 end）的单元。

### 范例

**示例 \#1 <span class="function">range</span> 例子**

``` php
<?php
// array(0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12)
foreach (range(0, 12) as $number) {
    echo $number;
}

//  step 参数
// array(0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100)
foreach (range(0, 100, 10) as $number) {
    echo $number;
}

// 字符序列的使用
// array('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i');
foreach (range('a', 'i') as $letter) {
    echo $letter;
}
// array('c', 'b', 'a');
foreach (range('c', 'a') as $letter) {
    echo $letter;
}
?>
```

### 注释

> **Note**:
>
> 字符序列值仅限单个字符。 如果长度大于1，仅仅使用第一个字符。

### 参见

-   <span class="function">shuffle</span>
-   <span class="function">array\_fill</span>
-   <a href="/control-structures/foreach.html" class="link">foreach</a>

reset
=====

将数组的内部指针指向第一个单元

### 说明

<span class="type">mixed</span> <span class="methodname">reset</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

<span class="function">reset</span> 将 `array`
的内部指针倒回到第一个单元并返回第一个数组单元的值。

### 参数

`array`  
输入的数组。

### 返回值

返回数组第一个单元的值，如果数组为空则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">reset</span> 例子**

``` php
<?php

$array = array('step one', 'step two', 'step three', 'step four');

// by default, the pointer is on the first element
echo current($array) . "<br />\n"; // "step one"

// skip two steps
next($array);
next($array);
echo current($array) . "<br />\n"; // "step three"

// reset pointer, start again on step one
reset($array);
echo current($array) . "<br />\n"; // "step one"

?>
```

### 参见

-   <span class="function">current</span>
-   <span class="function">each</span>
-   <span class="function">end</span>
-   <span class="function">next</span>
-   <span class="function">prev</span>

rsort
=====

对数组逆向排序

### 说明

<span class="type">bool</span> <span class="methodname">rsort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \] )

本函数对数组进行逆向排序（最高到最低）。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的数组。

`sort_flags`  
可以用可选参数 `sort_flags` 改变排序的行为，详情见 <span
class="function">sort</span>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rsort</span> 例**

``` php
<?php
$fruits = array("lemon", "orange", "banana", "apple");
rsort($fruits);
foreach ($fruits as $key => $val) {
    echo "$key = $val\n";
}
?>
```

以上例程会输出：

    0 = orange
    1 = lemon
    2 = banana
    3 = apple

fruits 被按照字母顺序逆向排序。

### 注释

> **Note**: <span class="simpara">此函数为 `array`
> 中的元素赋与新的键名。这将删除原有的键名，而不是仅仅将键名重新排序。</span>

### 参见

-   <span class="function">arsort</span>
-   <span class="function">krsort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

shuffle
=======

打乱数组

### 说明

<span class="type">bool</span> <span class="methodname">shuffle</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> )

本函数打乱（随机排列单元的顺序）一个数组。
它使用的是伪随机数产生器，并不适合密码学的场合。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
待操作的数组。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                      |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | <a href="/migration71/incompatible.html#migration71.incompatible.rand-srand-aliases" class="link">内置的随机数产生算法从 libc rand 函数改成</a> <a href="http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html" class="link external">» 梅森旋转</a>伪随机数生成算法。 |

### 范例

**示例 \#1 <span class="function">shuffle</span> 例子**

``` php
<?php
$numbers = range(1, 20);
shuffle($numbers);
foreach ($numbers as $number) {
    echo "$number ";
}
?>
```

### 注释

> **Note**: <span class="simpara">此函数为 `array`
> 中的元素赋与新的键名。这将删除原有的键名，而不是仅仅将键名重新排序。</span>

### 参见

-   <span class="function">array\_rand</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

sizeof
======

<span class="function">count</span> 的别名

### 说明

此函数是该函数的别名：<span class="function">count</span>。

sort
====

对数组排序

### 说明

<span class="type">bool</span> <span class="methodname">sort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sort_flags`<span class="initializer"> =
SORT\_REGULAR</span></span> \] )

本函数对数组进行排序。当本函数结束时数组单元将被从最低到最高重新安排。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
要排序的数组。

`sort_flags`  
可选的第二个参数 `sort_flags` 可以用以下值改变排序的行为：

排序类型标记：

-   <span class="simpara">**`SORT_REGULAR`** -
    正常比较单元（不改变类型）</span>
-   <span class="simpara">**`SORT_NUMERIC`** -
    单元被作为数字来比较</span>
-   <span class="simpara">**`SORT_STRING`** -
    单元被作为字符串来比较</span>
-   <span class="simpara"> **`SORT_LOCALE_STRING`** -
    根据当前的区域（locale）设置来把单元当作字符串比较，可以用 <span
    class="function">setlocale</span> 来改变。 </span>
-   <span class="simpara">**`SORT_NATURAL`** - 和 <span
    class="function">natsort</span>
    类似对每个单元以“自然的顺序”对字符串进行排序。 PHP 5.4.0
    中新增的。</span>
-   <span class="simpara">**`SORT_FLAG_CASE`** - 能够与
    **`SORT_STRING`** 或 **`SORT_NATURAL`** 合并（OR
    位运算），不区分大小写排序字符串。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                       |
|-------|----------------------------------------------------------------------------|
| 5.4.0 | 添加了 `sort_flags` 内 **`SORT_NATURAL`** 和 **`SORT_FLAG_CASE`** 的支持。 |
| 5.0.2 | 添加了 **`SORT_LOCALE_STRING`**。                                          |

### 范例

**示例 \#1 <span class="function">sort</span> 例子**

``` php
<?php

$fruits = array("lemon", "orange", "banana", "apple");
sort($fruits);
foreach ($fruits as $key => $val) {
    echo "fruits[" . $key . "] = " . $val . "\n";
}

?>
```

以上例程会输出：

    fruits[0] = apple
    fruits[1] = banana
    fruits[2] = lemon
    fruits[3] = orange

fruits 被按照字母顺序排序。

**示例 \#2 使用不区分大小写自然排序的 <span class="function">sort</span>
例子**

``` php
<?php

$fruits = array(
    "Orange1", "orange2", "Orange3", "orange20"
);
sort($fruits, SORT_NATURAL | SORT_FLAG_CASE);
foreach ($fruits as $key => $val) {
    echo "fruits[" . $key . "] = " . $val . "\n";
}

?>
```

以上例程会输出：

    fruits[0] = Orange1
    fruits[1] = orange2
    fruits[2] = Orange3
    fruits[3] = orange20

fruits 排序得像 <span class="function">natcasesort</span> 的结果。

### 注释

> **Note**: <span class="simpara">此函数为 `array`
> 中的元素赋与新的键名。这将删除原有的键名，而不是仅仅将键名重新排序。</span>

> **Note**: <span class="simpara"> 和大多数 PHP 排序函数一样，<span
> class="function">sort</span> 使用了
> <a href="http://en.wikipedia.org/wiki/Quicksort" class="link external">» Quicksort</a>
> 实现的。 The pivot is chosen in the middle of the partition resulting
> in an optimal time for already sorted arrays. This is however an
> implementation detail you shouldn't rely on. </span>

**Warning**

在对含有混合类型值的数组排序时要小心，因为 <span
class="function">sort</span> 可能会产生不可预知的结果。

### 参见

-   <span class="function">asort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

uasort
======

使用用户自定义的比较函数对数组中的值进行排序并保持索引关联

### 说明

<span class="type">bool</span> <span class="methodname">uasort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> , <span class="methodparam"><span
class="type">callable</span> `$value_compare_func`</span> )

本函数对数组排序并保持索引和单元之间的关联。

主要用于对那些单元顺序很重要的结合数组进行排序。比较函数是用户自定义的。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的数组。

`value_compare_func`  
用户自定义比较函数的例子请参考 <span class="function">usort</span> 和
<span class="function">uksort</span>。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">uasort</span> 的基本例子**

``` php
<?php
// Comparison function
function cmp($a, $b) {
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

// Array to be sorted
$array = array('a' => 4, 'b' => 8, 'c' => -1, 'd' => -9, 'e' => 2, 'f' => 5, 'g' => 3, 'h' => -4);
print_r($array);

// Sort and print the resulting array
uasort($array, 'cmp');
print_r($array);
?>
```

以上例程会输出：

    Array
    (
        [a] => 4
        [b] => 8
        [c] => -1
        [d] => -9
        [e] => 2
        [f] => 5
        [g] => 3
        [h] => -4
    )
    Array
    (
        [d] => -9
        [h] => -4
        [c] => -1
        [e] => 2
        [g] => 3
        [a] => 4
        [f] => 5
        [b] => 8
    )

### 参见

-   <span class="function">usort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

uksort
======

使用用户自定义的比较函数对数组中的键名进行排序

### 说明

<span class="type">bool</span> <span class="methodname">uksort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> , <span class="methodparam"><span
class="type">callable</span> `$key_compare_func`</span> )

<span class="function">uksort</span>
函数将使用用户提供的比较函数对数组中的键名进行排序。如果要排序的数组需要用一种不寻常的标准进行排序，那么应该使用此函数。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

### 参数

`array`  
输入的数组。

`key_compare_func`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">uksort</span> 例子**

``` php
<?php
function cmp($a, $b)
{
    $a = preg_replace('@^(a|an|the) @', '', $a);
    $b = preg_replace('@^(a|an|the) @', '', $b);
    return strcasecmp($a, $b);
}

$a = array("John" => 1, "the Earth" => 2, "an apple" => 3, "a banana" => 4);

uksort($a, "cmp");

foreach ($a as $key => $value) {
    echo "$key: $value\n";
}
?>
```

以上例程会输出：

    an apple: 3
    a banana: 4
    the Earth: 2
    John: 1

### 参见

-   <span class="function">usort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

usort
=====

使用用户自定义的比较函数对数组中的值进行排序

### 说明

<span class="type">bool</span> <span class="methodname">usort</span> (
<span class="methodparam"><span class="type">array</span>
`&$array`</span> , <span class="methodparam"><span
class="type">callable</span> `$value_compare_func`</span> )

本函数将用用户自定义的比较函数对一个数组中的值进行排序。
如果要排序的数组需要用一种不寻常的标准进行排序，那么应该使用此函数。

> **Note**:
>
> 如果两个成员完全相同，那么它们在排序数组中的相对顺序是未定义的。

> **Note**: <span class="simpara">此函数为 `array`
> 中的元素赋与新的键名。这将删除原有的键名，而不是仅仅将键名重新排序。</span>

### 参数

`array`  
输入的数组

`cmp_function`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">usort</span> 例子**

``` php
<?php
function cmp($a, $b)
{
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

$a = array(3, 2, 5, 6, 1);

usort($a, "cmp");

foreach ($a as $key => $value) {
    echo "$key: $value\n";
}
?>
```

以上例程会输出：

    0: 1
    1: 2
    2: 3
    3: 5
    4: 6

> **Note**:
>
> 很明显在这个小例子中用 <span class="function">sort</span> 函数更合适。

**示例 \#2 使用多维数组的 <span class="function">usort</span> 例子**

``` php
<?php
function cmp($a, $b)
{
    return strcmp($a["fruit"], $b["fruit"]);
}

$fruits[0]["fruit"] = "lemons";
$fruits[1]["fruit"] = "apples";
$fruits[2]["fruit"] = "grapes";

usort($fruits, "cmp");

while (list($key, $value) = each($fruits)) {
    echo "$fruits[$key]: " . $value["fruit"] . "\n";
}
?>
```

当排序多维数组时，`$a` 和 `$b` 包含到数组第一个索引的引用。

以上例程会输出：

    $fruits[0]: apples
    $fruits[1]: grapes
    $fruits[2]: lemons

**示例 \#3 <span class="function">usort</span> example using a member
function of an object**

``` php
<?php
class TestObj {
    var $name;

    function TestObj($name)
    {
        $this->name = $name;
    }

    /* This is the static comparing function: */
    static function cmp_obj($a, $b)
    {
        $al = strtolower($a->name);
        $bl = strtolower($b->name);
        if ($al == $bl) {
            return 0;
        }
        return ($al > $bl) ? +1 : -1;
    }
}

$a[] = new TestObj("c");
$a[] = new TestObj("b");
$a[] = new TestObj("d");

usort($a, array("TestObj", "cmp_obj"));

foreach ($a as $item) {
    echo $item->name . "\n";
}
?>
```

以上例程会输出：

    b
    c
    d

**示例 \#4 <span class="function">usort</span> example using a
<a href="/functions/anonymous.html" class="link">closure</a> to sort a
multi-dimensional array**

``` php
<?php
$array[0] = array('key_a' => 'z', 'key_b' => 'c');
$array[1] = array('key_a' => 'x', 'key_b' => 'b');
$array[2] = array('key_a' => 'y', 'key_b' => 'a');

function build_sorter($key) {
    return function ($a, $b) use ($key) {
        return strnatcmp($a[$key], $b[$key]);
    };
}

usort($array, build_sorter('key_b'));

foreach ($array as $item) {
    echo $item['key_a'] . ', ' . $item['key_b'] . "\n";
}
?>
```

以上例程会输出：

    y, a
    x, b
    z, c

### 参见

-   <span class="function">uasort</span>
-   <a href="/array/sorting.html" class="link">数组排序函数对比</a>

**目录**

-   [array\_change\_key\_case](/ref/array.html#array_change_key_case) —
    将数组中的所有键名修改为全大写或小写
-   [array\_chunk](/ref/array.html#array_chunk) — 将一个数组分割成多个
-   [array\_column](/ref/array.html#array_column) — 返回数组中指定的一列
-   [array\_combine](/ref/array.html#array_combine) —
    创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值
-   [array\_count\_values](/ref/array.html#array_count_values) —
    统计数组中所有的值
-   [array\_diff\_assoc](/ref/array.html#array_diff_assoc) —
    带索引检查计算数组的差集
-   [array\_diff\_key](/ref/array.html#array_diff_key) —
    使用键名比较计算数组的差集
-   [array\_diff\_uassoc](/ref/array.html#array_diff_uassoc) —
    用用户提供的回调函数做索引检查来计算数组的差集
-   [array\_diff\_ukey](/ref/array.html#array_diff_ukey) —
    用回调函数对键名比较计算数组的差集
-   [array\_diff](/ref/array.html#array_diff) — 计算数组的差集
-   [array\_fill\_keys](/ref/array.html#array_fill_keys) —
    使用指定的键和值填充数组
-   [array\_fill](/ref/array.html#array_fill) — 用给定的值填充数组
-   [array\_filter](/ref/array.html#array_filter) —
    用回调函数过滤数组中的单元
-   [array\_flip](/ref/array.html#array_flip) — 交换数组中的键和值
-   [array\_intersect\_assoc](/ref/array.html#array_intersect_assoc) —
    带索引检查计算数组的交集
-   [array\_intersect\_key](/ref/array.html#array_intersect_key) —
    使用键名比较计算数组的交集
-   [array\_intersect\_uassoc](/ref/array.html#array_intersect_uassoc) —
    带索引检查计算数组的交集，用回调函数比较索引
-   [array\_intersect\_ukey](/ref/array.html#array_intersect_ukey) —
    用回调函数比较键名来计算数组的交集
-   [array\_intersect](/ref/array.html#array_intersect) — 计算数组的交集
-   [array\_key\_exists](/ref/array.html#array_key_exists) —
    检查数组里是否有指定的键名或索引
-   [array\_key\_first](/ref/array.html#array_key_first) —
    获取指定数组的第一个键值
-   [array\_key\_last](/ref/array.html#array_key_last) —
    获取一个数组的最后一个键值
-   [array\_keys](/ref/array.html#array_keys) —
    返回数组中部分的或所有的键名
-   [array\_map](/ref/array.html#array_map) —
    为数组的每个元素应用回调函数
-   [array\_merge\_recursive](/ref/array.html#array_merge_recursive) —
    递归地合并一个或多个数组
-   [array\_merge](/ref/array.html#array_merge) — 合并一个或多个数组
-   [array\_multisort](/ref/array.html#array_multisort) —
    对多个数组或多维数组进行排序
-   [array\_pad](/ref/array.html#array_pad) —
    以指定长度将一个值填充进数组
-   [array\_pop](/ref/array.html#array_pop) —
    弹出数组最后一个单元（出栈）
-   [array\_product](/ref/array.html#array_product) —
    计算数组中所有值的乘积
-   [array\_push](/ref/array.html#array_push) —
    将一个或多个单元压入数组的末尾（入栈）
-   [array\_rand](/ref/array.html#array_rand) —
    从数组中随机取出一个或多个单元
-   [array\_reduce](/ref/array.html#array_reduce) —
    用回调函数迭代地将数组简化为单一的值
-   [array\_replace\_recursive](/ref/array.html#array_replace_recursive)
    — 使用传递的数组递归替换第一个数组的元素
-   [array\_replace](/ref/array.html#array_replace) —
    使用传递的数组替换第一个数组的元素
-   [array\_reverse](/ref/array.html#array_reverse) —
    返回单元顺序相反的数组
-   [array\_search](/ref/array.html#array_search) —
    在数组中搜索给定的值，如果成功则返回首个相应的键名
-   [array\_shift](/ref/array.html#array_shift) —
    将数组开头的单元移出数组
-   [array\_slice](/ref/array.html#array_slice) — 从数组中取出一段
-   [array\_splice](/ref/array.html#array_splice) —
    去掉数组中的某一部分并用其它值取代
-   [array\_sum](/ref/array.html#array_sum) — 对数组中所有值求和
-   [array\_udiff\_assoc](/ref/array.html#array_udiff_assoc) —
    带索引检查计算数组的差集，用回调函数比较数据
-   [array\_udiff\_uassoc](/ref/array.html#array_udiff_uassoc) —
    带索引检查计算数组的差集，用回调函数比较数据和索引
-   [array\_udiff](/ref/array.html#array_udiff) —
    用回调函数比较数据来计算数组的差集
-   [array\_uintersect\_assoc](/ref/array.html#array_uintersect_assoc) —
    带索引检查计算数组的交集，用回调函数比较数据
-   [array\_uintersect\_uassoc](/ref/array.html#array_uintersect_uassoc)
    — 带索引检查计算数组的交集，用单独的回调函数比较数据和索引
-   [array\_uintersect](/ref/array.html#array_uintersect) —
    计算数组的交集，用回调函数比较数据
-   [array\_unique](/ref/array.html#array_unique) — 移除数组中重复的值
-   [array\_unshift](/ref/array.html#array_unshift) —
    在数组开头插入一个或多个单元
-   [array\_values](/ref/array.html#array_values) — 返回数组中所有的值
-   [array\_walk\_recursive](/ref/array.html#array_walk_recursive) —
    对数组中的每个成员递归地应用用户函数
-   [array\_walk](/ref/array.html#array_walk) —
    使用用户自定义函数对数组中的每个元素做回调处理
-   [array](/ref/array.html#array) — 新建一个数组
-   [arsort](/ref/array.html#arsort) — 对数组进行逆向排序并保持索引关系
-   [asort](/ref/array.html#asort) — 对数组进行排序并保持索引关系
-   [compact](/ref/array.html#compact) —
    建立一个数组，包括变量名和它们的值
-   [count](/ref/array.html#count) —
    计算数组中的单元数目，或对象中的属性个数
-   [current](/ref/array.html#current) — 返回数组中的当前单元
-   [each](/ref/array.html#each) —
    返回数组中当前的键／值对并将数组指针向前移动一步
-   [end](/ref/array.html#end) — 将数组的内部指针指向最后一个单元
-   [extract](/ref/array.html#extract) —
    从数组中将变量导入到当前的符号表
-   [in\_array](/ref/array.html#in_array) — 检查数组中是否存在某个值
-   [key\_exists](/ref/array.html#key_exists) — 别名 array\_key\_exists
-   [key](/ref/array.html#key) — 从关联数组中取得键名
-   [krsort](/ref/array.html#krsort) — 对数组按照键名逆向排序
-   [ksort](/ref/array.html#ksort) — 对数组按照键名排序
-   [list](/ref/array.html#list) — 把数组中的值赋给一组变量
-   [natcasesort](/ref/array.html#natcasesort) —
    用“自然排序”算法对数组进行不区分大小写字母的排序
-   [natsort](/ref/array.html#natsort) — 用“自然排序”算法对数组排序
-   [next](/ref/array.html#next) — 将数组中的内部指针向前移动一位
-   [pos](/ref/array.html#pos) — current 的别名
-   [prev](/ref/array.html#prev) — 将数组的内部指针倒回一位
-   [range](/ref/array.html#range) — 根据范围创建数组，包含指定的元素
-   [reset](/ref/array.html#reset) — 将数组的内部指针指向第一个单元
-   [rsort](/ref/array.html#rsort) — 对数组逆向排序
-   [shuffle](/ref/array.html#shuffle) — 打乱数组
-   [sizeof](/ref/array.html#sizeof) — count 的别名
-   [sort](/ref/array.html#sort) — 对数组排序
-   [uasort](/ref/array.html#uasort) —
    使用用户自定义的比较函数对数组中的值进行排序并保持索引关联
-   [uksort](/ref/array.html#uksort) —
    使用用户自定义的比较函数对数组中的键名进行排序
-   [usort](/ref/array.html#usort) —
    使用用户自定义的比较函数对数组中的值进行排序
