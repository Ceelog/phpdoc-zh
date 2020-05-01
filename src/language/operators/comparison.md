比较运算符
----------

比较运算符，如同它们名称所暗示的，允许对两个值进行比较。还可以参考
<a href="/types/comparisons.html" class="link">PHP 类型比较表</a>看不同类型相互比较的例子。

| 例子        | 名称           | 结果                                                                                                                  |
|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------|
| $a == $b    | 等于           | **`TRUE`**，如果类型转换后 `$a` 等于 `$b`。                                                                           |
| $a === $b   | 全等           | **`TRUE`**，如果 `$a` 等于 `$b`，并且它们的类型也相同。                                                               |
| $a != $b    | 不等           | **`TRUE`**，如果类型转换后 `$a` 不等于 `$b`。                                                                         |
| $a \<\> $b  | 不等           | **`TRUE`**，如果类型转换后 `$a` 不等于 `$b`。                                                                         |
| $a !== $b   | 不全等         | **`TRUE`**，如果 `$a` 不等于 `$b`，或者它们的类型不同。                                                               |
| $a \< $b    | 小与           | **`TRUE`**，如果 `$a` 严格小于 `$b`。                                                                                 |
| $a \> $b    | 大于           | **`TRUE`**，如果 `$a` 严格大于 `$b`。                                                                                 |
| $a \<= $b   | 小于等于       | **`TRUE`**，如果 `$a` 小于或者等于 `$b`。                                                                             |
| $a \>= $b   | 大于等于       | **`TRUE`**，如果 `$a` 大于或者等于 `$b`。                                                                             |
| $a \<=\> $b | 结合比较运算符 | 当`$a`小于、等于、大于than `$b`时 分别返回一个小于、等于、大于0的<span class="type">integer</span> 值。 PHP7开始提供. |

如果比较一个数字和字符串或者比较涉及到数字内容的字符串，则字符串会被<a href="/language/types/string.html#language.types.string.conversion" class="link">转换为数值</a>并且比较按照数值来进行。此规则也适用于
<a href="/control-structures/switch.html" class="link">switch</a>
语句。当用 === 或 !==
进行比较时则不进行类型转换，因为此时类型和数值都要比对。

``` php
<?php
var_dump(0 == "a"); // 0 == 0 -> true
var_dump("1" == "01"); // 1 == 1 -> true
var_dump("10" == "1e1"); // 10 == 10 -> true
var_dump(100 == "1e2"); // 100 == 100 -> true

switch ("a") {
case 0:
    echo "0";
    break;
case "a": // never reached because "a" is already matched with 0
    echo "a";
    break;
}
?>
```

``` php
<?php  
// Integers
echo 1 <=> 1; // 0
echo 1 <=> 2; // -1
echo 2 <=> 1; // 1
 
// Floats
echo 1.5 <=> 1.5; // 0
echo 1.5 <=> 2.5; // -1
echo 2.5 <=> 1.5; // 1
 
// Strings
echo "a" <=> "a"; // 0
echo "a" <=> "b"; // -1
echo "b" <=> "a"; // 1
 
echo "a" <=> "aa"; // -1
echo "zz" <=> "aa"; // 1
 
// Arrays
echo [] <=> []; // 0
echo [1, 2, 3] <=> [1, 2, 3]; // 0
echo [1, 2, 3] <=> []; // 1
echo [1, 2, 3] <=> [1, 2, 1]; // 1
echo [1, 2, 3] <=> [1, 2, 4]; // -1
 
// Objects
$a = (object) ["a" => "b"]; 
$b = (object) ["a" => "b"]; 
echo $a <=> $b; // 0
 
$a = (object) ["a" => "b"]; 
$b = (object) ["a" => "c"]; 
echo $a <=> $b; // -1
 
$a = (object) ["a" => "c"]; 
$b = (object) ["a" => "b"]; 
echo $a <=> $b; // 1
 
// only values are compared
$a = (object) ["a" => "b"]; 
$b = (object) ["b" => "b"]; 
echo $a <=> $b; // 1

?>
```

对于多种类型，比较运算符根据下表比较（按顺序）。

| 运算数 1 类型                                                                                            | 运算数 2 类型                                                                                            | 结果                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span class="type">null</span> 或 <span class="type">string</span>                                       | <span class="type">string</span>                                                                         | 将 **`NULL`** 转换为 ""，进行数字或词汇比较                                                                                                                               |
| <span class="type">bool</span> 或 <span class="type">null</span>                                         | 任何其它类型                                                                                             | 转换为 <span class="type">bool</span>，**`FALSE`** \< **`TRUE`**                                                                                                          |
| <span class="type">object</span>                                                                         | <span class="type">object</span>                                                                         | 内置类可以定义自己的比较，不同类不能比较，相同类和数组同样方式比较属性（PHP 4 中），PHP 5 有其自己的<a href="/language/oop5/object-comparison.html" class="link">说明</a> |
| <span class="type">string</span>，<span class="type">resource</span> 或 <span class="type">number</span> | <span class="type">string</span>，<span class="type">resource</span> 或 <span class="type">number</span> | 将字符串和资源转换成数字，按普通数学比较                                                                                                                                  |
| <span class="type">array</span>                                                                          | <span class="type">array</span>                                                                          | 具有较少成员的数组较小，如果运算数 1 中的键不存在于运算数 2 中则数组无法比较，否则挨个值比较（见下例）                                                                    |
| <span class="type">object</span>                                                                         | 任何其它类型                                                                                             | <span class="type">object</span> 总是更大                                                                                                                                 |
| <span class="type">array</span>                                                                          | 任何其它类型                                                                                             | <span class="type">array</span> 总是更大                                                                                                                                  |

**示例 \#1 Boolean/null comparison**

``` php
<?php
// Bool and null are compared as bool always
var_dump(1 == TRUE);  // TRUE - same as (bool)1 == TRUE
var_dump(0 == FALSE); // TRUE - same as (bool)0 == FALSE
var_dump(100 < TRUE); // FALSE - same as (bool)100 < TRUE
var_dump(-10 < FALSE);// FALSE - same as (bool)-10 < FALSE
var_dump(min(-100, -10, NULL, 10, 100)); // NULL - (bool)NULL < (bool)-100 is FALSE < TRUE
?>
```

**示例 \#2 标准数组比较代码**

``` php
<?php
// 数组是用标准比较运算符这样比较的
function standard_array_compare($op1, $op2)
{
    if (count($op1) < count($op2)) {
        return -1; // $op1 < $op2
    } elseif (count($op1) > count($op2)) {
        return 1; // $op1 > $op2
    }
    foreach ($op1 as $key => $val) {
        if (!array_key_exists($key, $op2)) {
            return null; // uncomparable
        } elseif ($val < $op2[$key]) {
            return -1;
        } elseif ($val > $op2[$key]) {
            return 1;
        }
    }
    return 0; // $op1 == $op2
}
?>
```

参见 <span class="function">strcasecmp</span>，<span
class="function">strcmp</span>，<a href="/language/operators/array.html" class="link">数组运算符</a>和<a href="/language/types.html" class="link">类型</a>章节。

**Warning**

由于浮点数 <span class="type">float</span>
的内部表达方式，不应比较两个浮点数<span
class="type">float</span>是否相等。

更多信息参见 <span class="type">float</span>。

### 三元运算符

另一个条件运算符是“?:”（或三元）运算符 。

**示例 \#3 赋默认值**

``` php
<?php
// 三元运算符的例子
$action = (empty($_POST['action'])) ? 'default' : $_POST['action'];

// 以上等同于以下的  if/else 语句
if (empty($_POST['action'])) {
    $action = 'default';
} else {
    $action = $_POST['action'];
}

?>
```

表达式 *(expr1) ? (expr2) : (expr3)* 在 <span
class="replaceable">expr1</span> 求值为 **`TRUE`** 时的值为 <span
class="replaceable">expr2</span>，在 <span
class="replaceable">expr1</span> 求值为 **`FALSE`** 时的值为 <span
class="replaceable">expr3</span>。

自 PHP 5.3 起，可以省略三元运算符中间那部分。表达式 *expr1 ?: expr3* 在
<span class="replaceable">expr1</span> 求值为 **`TRUE`** 时返回 <span
class="replaceable">expr1</span>，否则返回 <span
class="replaceable">expr3</span>。

> **Note**: <span class="simpara">
> 注意三元运算符是个语句，因此其求值不是变量，而是语句的结果。如果想通过引用返回一个变量这点就很重要。在一个通过引用返回的函数中语句
> *return $var == 42 ? $a : $b;* 将不起作用，以后的 PHP
> 版本会为此发出一条警告。 </span>

> **Note**:
>
> 建议避免将三元运算符堆积在一起使用。当在一条语句中使用多个三元运算符时会造成
> PHP 运算结果不清晰：
>
> **示例 \#4 不清晰的三元运算符行为**
>
> ``` php
> <?php
> // 乍看起来下面的输出是 'true'
> echo (true?'true':false?'t':'f');
>
> // 然而，上面语句的实际输出是't'，因为三元运算符是从左往右计算的
>
> // 下面是与上面等价的语句，但更清晰
> echo ((true ? 'true' : 'false') ? 't' : 'f');
>
> // here, you can see that the first expression is evaluated to 'true', which
> // in turn evaluates to (bool)true, thus returning the true branch of the
> // second ternary expression.
> ?>
> ```

### NULL 合并运算符

PHP 7 开始存在 "??" （NULL 合并）运算符。

**示例 \#5 设置默认值**

``` php
<?php
// NULL 合并运算符的例子
$action = $_POST['action'] ?? 'default';

// 以上例子等同于于以下 if/else 语句
if (isset($_POST['action'])) {
    $action = $_POST['action'];
} else {
    $action = 'default';
}

?>
```

当 <span class="replaceable">expr1</span> 为 **`NULL`**，表达式 *(expr1)
?? (expr2)* 等同于 <span class="replaceable">expr2</span>，否则为 <span
class="replaceable">expr1</span>。

尤其要注意，当不存在左侧的值时，此运算符也和 <span
class="function">isset</span> 一样不会产生警告。 对于 array 键尤其有用。

> **Note**: <span class="simpara"> 请注意：NULL
> 合并运算符是一个表达式，产生的也是表达式结果，而不是变量。
> 返回引用变量时需要强调这一点。
> 因此，在返回引用的函数里就无法使用这样的语句：*return $foo ??
> $bar;*，还会提示警告。 </span>

> **Note**:
>
> 请注意，NULL 合并运算符支持简单的嵌套：
>
> **示例 \#6 嵌套 NULL 合并运算符**
>
> ``` php
> <?php
>
> $foo = null;
> $bar = null;
> $baz = 1;
> $qux = 2;
>
> echo $foo ?? $bar ?? $baz ?? $qux; // 输出 1
>
> ?>
> ```
