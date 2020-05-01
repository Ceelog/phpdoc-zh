*foreach*
---------

*foreach* 语法结构提供了遍历数组的简单方式。*foreach*
仅能够应用于数组和对象，如果尝试应用于其他数据类型的变量，或者未初始化的变量将发出错误信息。有两种语法：

    foreach (array_expression as $value)
        statement
    foreach (array_expression as $key => $value)
        statement

第一种格式遍历给定的 *array\_expression*
数组。每次循环中，当前单元的值被赋给 *$value*
并且数组内部的指针向前移一步（因此下一次循环中将会得到下一个单元）。

第二种格式做同样的事，只除了当前单元的键名也会在每次循环中被赋给变量
*$key*。

还能够自定义<a href="/language/oop5/iterations.html" class="link">遍历对象</a>。

> **Note**:
>
> 当 *foreach*
> 开始执行时，数组内部的指针会自动指向第一个单元。这意味着不需要在
> *foreach* 循环之前调用 <span class="function">reset</span>。
>
> 由于 *foreach*
> 依赖内部数组指针，在循环中修改其值将可能导致意外的行为。

可以很容易地通过在 *$value* 之前加上 &
来修改数组的元素。此方法将以<a href="/language/references.html" class="link">引用</a>赋值而不是拷贝一个值。

``` php
<?php
$arr = array(1, 2, 3, 4);
foreach ($arr as &$value) {
    $value = $value * 2;
}
// $arr is now array(2, 4, 6, 8)
unset($value); // 最后取消掉引用
?>
```

*$value*
的引用仅在被遍历的数组可以被引用时才可用（例如是个变量）。以下代码则无法运行：

``` php
<?php
foreach (array(1, 2, 3, 4) as &$value) {
    $value = $value * 2;
}

?>
```

**Warning**

数组最后一个元素的 *$value* 引用在 *foreach* 循环之后仍会保留。建议使用
<span class="function">unset</span> 来将其销毁。

> **Note**:
>
> *foreach* 不支持用“@”来抑制错误信息的能力。

用户可能注意到了以下的代码功能完全相同：

``` php
<?php
$arr = array("one", "two", "three");
reset($arr);
while (list(, $value) = each($arr)) {
    echo "Value: $value<br>\n";
}

foreach ($arr as $value) {
    echo "Value: $value<br />\n";
}
?>
```

以下代码功能也完全相同：

``` php
<?php
$arr = array("one", "two", "three");
reset($arr);
while (list($key, $value) = each($arr)) {
    echo "Key: $key; Value: $value<br />\n";
}

foreach ($arr as $key => $value) {
    echo "Key: $key; Value: $value<br />\n";
}
?>
```

示范用法的更多例子：

``` php
<?php
/* foreach example 1: value only */

$a = array(1, 2, 3, 17);

foreach ($a as $v) {
   echo "Current value of \$a: $v.\n";
}

/* foreach example 2: value (with its manual access notation printed for illustration) */

$a = array(1, 2, 3, 17);

$i = 0; /* for illustrative purposes only */

foreach ($a as $v) {
    echo "\$a[$i] => $v.\n";
    $i++;
}

/* foreach example 3: key and value */

$a = array(
    "one" => 1,
    "two" => 2,
    "three" => 3,
    "seventeen" => 17
);

foreach ($a as $k => $v) {
    echo "\$a[$k] => $v.\n";
}

/* foreach example 4: multi-dimensional arrays */
$a = array();
$a[0][0] = "a";
$a[0][1] = "b";
$a[1][0] = "y";
$a[1][1] = "z";

foreach ($a as $v1) {
    foreach ($v1 as $v2) {
        echo "$v2\n";
    }
}

/* foreach example 5: dynamic arrays */

foreach (array(1, 2, 3, 4, 5) as $v) {
    echo "$v\n";
}
?>
```

### 用 list() 给嵌套的数组解包

PHP 5.5
增添了遍历一个数组的数组的功能并且把嵌套的数组解包到循环变量中，只需将
<span class="function">list</span> 作为值提供。

例如：

``` php
<?php
$array = [
    [1, 2],
    [3, 4],
];

foreach ($array as list($a, $b)) {
    // $a contains the first element of the nested array,
    // and $b contains the second element.
    echo "A: $a; B: $b\n";
}
?>
```

以上例程会输出：

    A: 1; B: 2
    A: 3; B: 4

<span class="function">list</span>
中的单元可以少于嵌套数组的，此时多出来的数组单元将被忽略：

``` php
<?php
$array = [
    [1, 2],
    [3, 4],
];

foreach ($array as list($a)) {
    // Note that there is no $b here.
    echo "$a\n";
}
?>
```

以上例程会输出：

    1
    3

如果 <span class="function">list</span>
中列出的单元多于嵌套数组则会发出一条消息级别的错误信息：

``` php
<?php
$array = [
    [1, 2],
    [3, 4],
];

foreach ($array as list($a, $b, $c)) {
    echo "A: $a; B: $b; C: $c\n";
}
?>
```

以上例程会输出：


    Notice: Undefined offset: 2 in example.php on line 7
    A: 1; B: 2; C: 

    Notice: Undefined offset: 2 in example.php on line 7
    A: 3; B: 4; C: 
