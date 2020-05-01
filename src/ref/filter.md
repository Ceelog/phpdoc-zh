filter\_has\_var
================

检测是否存在指定类型的变量

### 说明

<span class="type">bool</span> <span
class="methodname">filter\_has\_var</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span>
`$variable_name`</span> )

### 参数

`type`  
**`INPUT_GET`**、 **`INPUT_POST`**、 **`INPUT_COOKIE`**、
**`INPUT_SERVER`**、 **`INPUT_ENV`** 里的其中一个。

`variable_name`  
要检查的变量名。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

filter\_id
==========

返回与某个特定名称的过滤器相关联的id

### 说明

<span class="type">int</span> <span class="methodname">filter\_id</span>
( <span class="methodparam"><span class="type">string</span>
`$filtername`</span> )

### 参数

`filtername`  
待获取的过滤器名称

### 返回值

如果获取成功则返回过滤器id，如果过滤器不存在则返回 **`FALSE`** 。

### 参见

-   <span class="function">filter\_list</span>

filter\_input\_array
====================

获取一系列外部变量，并且可以通过过滤器处理它们

### 说明

<span class="type">mixed</span> <span
class="methodname">filter\_input\_array</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$definition`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$add_empty`<span class="initializer"> =
true</span></span> \]\] )

这个函数当需要获取很多变量却不想重复调用<span
class="function">filter\_input</span>时很有用。

### 参数

`type`  
**`INPUT_GET`**, **`INPUT_POST`**, **`INPUT_COOKIE`**,
**`INPUT_SERVER`**, or **`INPUT_ENV`**之一。

`definition`  
一个定义参数的数组。一个有效的键必须是一个包含变量名的<span
class="type">string</span>，一个有效的值要么是一个<a href="/filter/filters.html" class="link">filter type</a>，或者是一个<span
class="type">array</span>
指明了过滤器、标示和选项。如果值是一个数组，那么它的有效的键可以是
*filter*， 用于指明
<a href="/filter/filters.html" class="link">filter type</a>，*flags*
用于指明任何想要用于过滤器的标示，或者 *options*
用于指明任何想要用于过滤器的选项。 参考下面的例子来更好的理解这段说明。

这个参数也可以是一个<a href="/filter/constants.html" class="link">filter constant</a>的整数。那么数组中的所有变量都会被这个过滤器所过滤。

`add_empty`  
在返回值中添加 **`NULL`** 作为不存在的键。

### 返回值

如果成功的话返回一个所请求的变量的数组，如果失败的话返回 **`FALSE`**
。对于数组的值，如果过滤失败则返回 **`FALSE`** ，如果`variable_name`
不存在的话则返回 **`NULL`** 。 如果标示 **`FILTER_NULL_ON_FAILURE`**
被使用了，那么当变量不存在时返回 **`FALSE`** ，当过滤失败时返回
**`NULL`** 。

### 范例

**示例 \#1 一个 <span class="function">filter\_input\_array</span>
的例子**

``` php
<?php
error_reporting(E_ALL | E_STRICT);
/* data actually came from POST
$_POST = array(
    'product_id'    => 'libgd<script>',
    'component'     => '10',
    'versions'      => '2.0.33',
    'testscalar'    => array('2', '23', '10', '12'),
    'testarray'     => '2',
);
*/

$args = array(
    'product_id'   => FILTER_SANITIZE_ENCODED,
    'component'    => array('filter'    => FILTER_VALIDATE_INT,
                            'flags'     => FILTER_REQUIRE_ARRAY, 
                            'options'   => array('min_range' => 1, 'max_range' => 10)
                           ),
    'versions'     => FILTER_SANITIZE_ENCODED,
    'doesnotexist' => FILTER_VALIDATE_INT,
    'testscalar'   => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_REQUIRE_SCALAR,
                           ),
    'testarray'    => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_REQUIRE_ARRAY,
                           )

);

$myinputs = filter_input_array(INPUT_POST, $args);

var_dump($myinputs);
echo "\n";
?>
```

以上例程会输出：

    array(6) {
      ["product_id"]=>
      string(17) "libgd%3Cscript%3E"
      ["component"]=>
      array(1) {
        [0]=>
        int(10)
      }
      ["versions"]=>
      string(6) "2.0.33"
      ["doesnotexist"]=>
      NULL
      ["testscalar"]=>
      bool(false)
      ["testarray"]=>
      array(1) {
        [0]=>
        int(2)
      }
    }

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 5.4.0 | 添加 `add_empty` 参数. |

### 注释

> **Note**:
>
> 在 **`INPUT_SERVER`** 数组中并没有 *REQUEST\_TIME*
> ，因为它是被稍后插入到`$_SERVER` 中的。

### 参见

-   <span class="function">filter\_input</span>
-   <span class="function">filter\_var\_array</span>
-   <a href="/filter/filters.html" class="xref">Types of filters</a>

filter\_input
=============

通过名称获取特定的外部变量，并且可以通过过滤器处理它

### 说明

<span class="type">mixed</span> <span
class="methodname">filter\_input</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span>
`$variable_name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$filter`<span class="initializer"> =
FILTER\_DEFAULT</span></span> \[, <span class="methodparam"><span
class="type">mixed</span> `$options`</span> \]\] )

### 参数

`type`  
**`INPUT_GET`**, **`INPUT_POST`**, **`INPUT_COOKIE`**,
**`INPUT_SERVER`**或 **`INPUT_ENV`**之一。

`variable_name`  
待获取的变量名。

`filter`  
The ID of the filter to apply. The
<a href="/filter/filters.html" class="xref">Types of filters</a> manual
page lists the available filters.

If omitted, **`FILTER_DEFAULT`** will be used, which is equivalent to
<a href="/filter/filters.html#Sanitize%20filters" class="link"><strong><code>FILTER_UNSAFE_RAW</code></strong></a>.
This will result in no filtering taking place by default.

`options`  
一个选项的关联数组，或者按位区分的标示。如果过滤器接受选项，可以通过数组的
"flags" 位去提供这些标示。

### 返回值

如果成功的话返回所请求的变量。如果过滤失败则返回 **`FALSE`**
，如果`variable_name` 不存在的话则返回 **`NULL`** 。 如果标示
**`FILTER_NULL_ON_FAILURE`** 被使用了，那么当变量不存在时返回
**`FALSE`** ，当过滤失败时返回 **`NULL`** 。

### 范例

**示例 \#1 一个 <span class="function">filter\_input</span> 的例子**

``` php
<?php
$search_html = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_SPECIAL_CHARS);
$search_url = filter_input(INPUT_GET, 'search', FILTER_SANITIZE_ENCODED);
echo "You have searched for $search_html.\n";
echo "<a href='?search=$search_url'>Search again.</a>";
?>
```

以上例程的输出类似于：

    You have searched for Me &#38; son.
    <a href='?search=Me%20%26%20son'>Search again.</a>

### 参见

-   <span class="function">filter\_var</span>
-   <span class="function">filter\_input\_array</span>
-   <span class="function">filter\_var\_array</span>
-   <a href="/filter/filters.html" class="xref">Types of filters</a>

filter\_list
============

返回所支持的过滤器列表

### 说明

<span class="type">array</span> <span
class="methodname">filter\_list</span> ( <span
class="methodparam">void</span> )

### 返回值

返回一个所支持的过滤器的名称的列表，如果没有这样子的过滤器的话则返回空数组。这个数组的索引不是过滤器id，
你可以通过 <span class="function">filter\_id</span> 去根据名称获取它们。

### 范例

**示例 \#1 一个 <span class="function">filter\_list</span> 的例子**

``` php
<?php
print_r(filter_list());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => int
        [1] => boolean
        [2] => float
        [3] => validate_regexp
        [4] => validate_url
        [5] => validate_email
        [6] => validate_ip
        [7] => string
        [8] => stripped
        [9] => encoded
        [10] => special_chars
        [11] => unsafe_raw
        [12] => email
        [13] => url
        [14] => number_int
        [15] => number_float
        [16] => magic_quotes
        [17] => callback
    )

filter\_var\_array
==================

获取多个变量并且过滤它们

### 说明

<span class="type">mixed</span> <span
class="methodname">filter\_var\_array</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$definition`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$add_empty`<span class="initializer"> =
true</span></span> \]\] )

不需要重复调用 <span class="function">filter\_var</span>
就能获取多个变量。

### 参数

`data`  
数组，键为字符串，值为待过滤的数据。

`definition`  
一个定义参数的数组。一个有效的键必须是一个包含变量名的<span
class="type">string</span>，一个有效的值要么是一个<a href="/filter/filters.html" class="link">filter type</a>，或者是一个<span
class="type">array</span>
指明了过滤器、标示和选项。如果值是一个数组，那么它的有效的键可以是
*filter*， 用于指明
<a href="/filter/filters.html" class="link">filter type</a>，*flags*
用于指明任何想要用于过滤器的标示，或者 *options*
用于指明任何想要用于过滤器的选项。 参考下面的例子来更好的理解这段说明。

这个参数也可以是一个<a href="/filter/constants.html" class="link">filter constant</a>的整数。那么数组中的所有值都会被这个过滤器所过滤。

`add_empty`  
在返回值中添加 **`NULL`** 作为不存在的键。

### 返回值

如果成功则返回一个包含所请求变量的数组，或者当失败时返回 **`FALSE`** 。
一个数组的值如果过滤失败则为 **`FALSE`** ，或者为 **`NULL`**
如果变量不存在的话。

### 范例

**示例 \#1 一个 <span class="function">filter\_var\_array</span>
的例子**

``` php
<?php
error_reporting(E_ALL | E_STRICT);
$data = array(
    'product_id'    => 'libgd<script>',
    'component'     => '10',
    'versions'      => '2.0.33',
    'testscalar'    => array('2', '23', '10', '12'),
    'testarray'     => '2',
);

$args = array(
    'product_id'   => FILTER_SANITIZE_ENCODED,
    'component'    => array('filter'    => FILTER_VALIDATE_INT,
                            'flags'     => FILTER_FORCE_ARRAY, 
                            'options'   => array('min_range' => 1, 'max_range' => 10)
                           ),
    'versions'     => FILTER_SANITIZE_ENCODED,
    'doesnotexist' => FILTER_VALIDATE_INT,
    'testscalar'   => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_REQUIRE_SCALAR,
                           ),
    'testarray'    => array(
                            'filter' => FILTER_VALIDATE_INT,
                            'flags'  => FILTER_FORCE_ARRAY,
                           )

);

$myinputs = filter_var_array($data, $args);

var_dump($myinputs);
echo "\n";
?>
```

以上例程会输出：

    array(6) {
      ["product_id"]=>
      string(17) "libgd%3Cscript%3E"
      ["component"]=>
      array(1) {
        [0]=>
        int(10)
      }
      ["versions"]=>
      string(6) "2.0.33"
      ["doesnotexist"]=>
      NULL
      ["testscalar"]=>
      bool(false)
      ["testarray"]=>
      array(1) {
        [0]=>
        int(2)
      }
    }

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 5.4.0 | 添加 `add_empty` 参数。 |

### 参见

-   <span class="function">filter\_input\_array</span>
-   <span class="function">filter\_var</span>
-   <span class="function">filter\_input</span>
-   <a href="/filter/filters.html" class="xref">Types of filters</a>

filter\_var
===========

使用特定的过滤器过滤一个变量

### 说明

<span class="type">mixed</span> <span
class="methodname">filter\_var</span> ( <span class="methodparam"><span
class="type">mixed</span> `$variable`</span> \[, <span
class="methodparam"><span class="type">int</span> `$filter`<span
class="initializer"> = FILTER\_DEFAULT</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$options`</span>
\]\] )

### 参数

`variable`  
待过滤的变量。注意：标量的值在过滤前，会被<a href="/language/types/string.html#language.types.string.casting" class="link">转换成字符串</a>。

`filter`  
The ID of the filter to apply. The
<a href="/filter/filters.html" class="xref">Types of filters</a> manual
page lists the available filters.

If omitted, **`FILTER_DEFAULT`** will be used, which is equivalent to
<a href="/filter/filters.html#Sanitize%20filters" class="link"><strong><code>FILTER_UNSAFE_RAW</code></strong></a>.
This will result in no filtering taking place by default.

`options`  
一个选项的关联数组，或者按位区分的标示。如果过滤器接受选项，可以通过数组的
"flags" 位去提供这些标示。 对于回调型的过滤器，应该传入 <span
class="type">callable</span>。这个回调函数必须接受一个参数，即待过滤的值，并且
返回一个在过滤/净化后的值。

``` php
<?php
// for filters that accept options, use this format
$options = array(
    'options' => array(
        'default' => 3, // value to return if the filter fails
        // other options here
        'min_range' => 0
    ),
    'flags' => FILTER_FLAG_ALLOW_OCTAL,
);
$var = filter_var('0755', FILTER_VALIDATE_INT, $options);

// for filter that only accept flags, you can pass them directly
$var = filter_var('oops', FILTER_VALIDATE_BOOLEAN, FILTER_NULL_ON_FAILURE);

// for filter that only accept flags, you can also pass as an array
$var = filter_var('oops', FILTER_VALIDATE_BOOLEAN,
                  array('flags' => FILTER_NULL_ON_FAILURE));

// callback validate filter
function foo($value)
{
    // Expected format: Surname, GivenNames
    if (strpos($value, ", ") === false) return false;
    list($surname, $givennames) = explode(", ", $value, 2);
    $empty = (empty($surname) || empty($givennames));
    $notstrings = (!is_string($surname) || !is_string($givennames));
    if ($empty || $notstrings) {
        return false;
    } else {
        return $value;
    }
}
$var = filter_var('Doe, Jane Sue', FILTER_CALLBACK, array('options' => 'foo'));
?>
```

### 返回值

Returns the filtered data, or **`FALSE`** if the filter fails.

### 范例

**示例 \#1 一个 <span class="function">filter\_var</span> 的例子**

``` php
<?php
var_dump(filter_var('bob@example.com', FILTER_VALIDATE_EMAIL));
var_dump(filter_var('http://example.com', FILTER_VALIDATE_URL, FILTER_FLAG_PATH_REQUIRED));
?>
```

以上例程会输出：

    string(15) "bob@example.com"
    bool(false)

### 参见

-   <span class="function">filter\_var\_array</span>
-   <span class="function">filter\_input</span>
-   <span class="function">filter\_input\_array</span>
-   <a href="/filter/filters.html" class="xref">Types of filters</a>
-   <a href="/language/pseudo-types.html#language.types.callback" class="link">callback</a>
    类型的信息

**目录**

-   [filter\_has\_var](/ref/filter.html#filter_has_var) —
    检测是否存在指定类型的变量
-   [filter\_id](/ref/filter.html#filter_id) —
    返回与某个特定名称的过滤器相关联的id
-   [filter\_input\_array](/ref/filter.html#filter_input_array) —
    获取一系列外部变量，并且可以通过过滤器处理它们
-   [filter\_input](/ref/filter.html#filter_input) —
    通过名称获取特定的外部变量，并且可以通过过滤器处理它
-   [filter\_list](/ref/filter.html#filter_list) —
    返回所支持的过滤器列表
-   [filter\_var\_array](/ref/filter.html#filter_var_array) —
    获取多个变量并且过滤它们
-   [filter\_var](/ref/filter.html#filter_var) —
    使用特定的过滤器过滤一个变量
