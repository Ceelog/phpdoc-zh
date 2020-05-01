数组运算符
----------

| 例子       | 名称   | 结果                                                                      |
|------------|--------|---------------------------------------------------------------------------|
| $a + $b    | 联合   | `$a` 和 `$b` 的联合。                                                     |
| $a == $b   | 相等   | 如果 `$a` 和 `$b` 具有相同的键／值对则为 **`TRUE`**。                     |
| $a === $b  | 全等   | 如果 `$a` 和 `$b` 具有相同的键／值对并且顺序和类型都相同则为 **`TRUE`**。 |
| $a != $b   | 不等   | 如果 `$a` 不等于 `$b` 则为 **`TRUE`**。                                   |
| $a \<\> $b | 不等   | 如果 `$a` 不等于 `$b` 则为 **`TRUE`**。                                   |
| $a !== $b  | 不全等 | 如果 `$a` 不全等于 `$b` 则为 **`TRUE`**。                                 |

*+*
运算符把右边的数组元素附加到左边的数组后面，两个数组中都有的键名，则只用左边数组中的，右边的被忽略。

``` php
<?php
$a = array("a" => "apple", "b" => "banana");
$b = array("a" => "pear", "b" => "strawberry", "c" => "cherry");

$c = $a + $b; // Union of $a and $b
echo "Union of \$a and \$b: \n";
var_dump($c);

$c = $b + $a; // Union of $b and $a
echo "Union of \$b and \$a: \n";
var_dump($c);

$a += $b; // Union of $a += $b is $a and $b
echo "Union of \$a += \$b: \n";
var_dump($a);
?>
```

执行后，此脚本会显示：

    Union of $a and $b:
    array(3) {
      ["a"]=>
      string(5) "apple"
      ["b"]=>
      string(6) "banana"
      ["c"]=>
      string(6) "cherry"
    }
    Union of $b and $a:
    array(3) {
      ["a"]=>
      string(4) "pear"
      ["b"]=>
      string(10) "strawberry"
      ["c"]=>
      string(6) "cherry"
    }
    Union of $a += $b:
    array(3) {
      'a' =>
      string(5) "apple"
      'b' =>
      string(6) "banana"
      'c' =>
      string(6) "cherry"
    }

数组中的单元如果具有相同的键名和值则比较时相等。

**示例 \#1 比较数组**

``` php
<?php
$a = array("apple", "banana");
$b = array(1 => "banana", "0" => "apple");

var_dump($a == $b); // bool(true)
var_dump($a === $b); // bool(false)
?>
```

参见<a href="/language/types/array.html" class="link">数组类型</a>和<a href="/ref/array.html" class="link">数组函数</a>章节。
