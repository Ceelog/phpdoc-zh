递增／递减运算符
----------------

PHP 支持 C 风格的前／后递增与递减运算符。

> **Note**: <span class="simpara"> 递增／递减运算符不影响布尔值。递减
> **`null`** 值也没有效果，但是递增 **`null`** 的结果是 *1*。 </span>

| 例子 | 名称 | 效果                              |
|------|------|-----------------------------------|
| ++$a | 前加 | `$a` 的值加一，然后返回 `$a`。    |
| $a++ | 后加 | 返回 `$a`，然后将 `$a` 的值加一。 |
| --$a | 前减 | `$a` 的值减一， 然后返回 `$a`。   |
| $a-- | 后减 | 返回 `$a`，然后将 `$a` 的值减一。 |

一个简单的示例脚本：

``` php
<?php
echo "<h3>Postincrement</h3>";
$a = 5;
echo "Should be 5: " . $a++ . "<br />\n";
echo "Should be 6: " . $a . "<br />\n";

echo "<h3>Preincrement</h3>";
$a = 5;
echo "Should be 6: " . ++$a . "<br />\n";
echo "Should be 6: " . $a . "<br />\n";

echo "<h3>Postdecrement</h3>";
$a = 5;
echo "Should be 5: " . $a-- . "<br />\n";
echo "Should be 4: " . $a . "<br />\n";

echo "<h3>Predecrement</h3>";
$a = 5;
echo "Should be 4: " . --$a . "<br />\n";
echo "Should be 4: " . $a . "<br />\n";
?>
```

在处理字符变量的算数运算时，PHP 沿袭了 Perl 的习惯，而非 C 的。例如，在
Perl 中 *$a = 'Z'; $a++;* 将把 *$a* 变成*'AA'*，而在 C 中，*a = 'Z';
a++;* 将把 *a* 变成 *'\['*（*'Z'* 的 ASCII 值是 90，*'\['* 的 ASCII 值是
91）。注意字符变量只能递增，不能递减，并且只支持纯字母（a-z 和
A-Z）。递增／递减其他字符变量则无效，原字符串没有变化。

**示例 \#1 涉及字符变量的算数运算**

``` php
<?php
echo '== Alphabets ==' . PHP_EOL;
$s = 'W';
for ($n=0; $n<6; $n++) {
    echo ++$s . PHP_EOL;
}
// Digit characters behave differently
echo '== Digits ==' . PHP_EOL;
$d = 'A8';
for ($n=0; $n<6; $n++) {
    echo ++$d . PHP_EOL;
}
$d = 'A08';
for ($n=0; $n<6; $n++) {
    echo ++$d . PHP_EOL;
}
?>
```

以上例程会输出：

    == Characters ==
    X
    Y
    Z
    AA
    AB
    AC
    == Digits ==
    A9
    B0
    B1
    B2
    B3
    B4
    A09
    A10
    A11
    A12
    A13
    A14

递增或递减布尔值没有效果。
