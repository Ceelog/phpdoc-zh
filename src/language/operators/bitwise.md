位运算符
--------

位运算符允许对整型数中指定的位进行求值和操作。

| 例子           | 名称                | 结果                                                         |
|----------------|---------------------|--------------------------------------------------------------|
| **`$a & $b`**  | And（按位与）       | 将把 `$a` 和 `$b` 中都为 1 的位设为 1。                      |
| **`$a | $b`**  | Or（按位或）        | 将把 `$a` 和 `$b` 中任何一个为 1 的位设为 1。                |
| **`$a ^ $b`**  | Xor（按位异或）     | 将把 `$a` 和 `$b` 中一个为 1 另一个为 0 的位设为 1。         |
| **`~ $a`**     | Not（按位取反）     | 将 `$a` 中为 0 的位设为 1，反之亦然。                        |
| **`$a << $b`** | Shift left（左移）  | 将 `$a` 中的位向左移动 `$b` 次（每一次移动都表示“乘以 2”）。 |
| **`$a >> $b`** | Shift right（右移） | 将 `$a` 中的位向右移动 `$b` 次（每一次移动都表示“除以 2”）。 |

位移在 PHP
中是数学运算。向任何方向移出去的位都被丢弃。左移时右侧以零填充，符号位被移走意味着正负号不被保留。右移时左侧以符号位填充，意味着正负号被保留。

要用括号确保想要的<a href="/language/operators/precedence.html" class="link">优先级</a>。例如
*$a & $b == true* 先进行比较再进行按位与；而 *($a & $b) == true*
则先进行按位与再进行比较。

If both operands for the *&*, *\|* and *^* operators are strings, then
the operation will be performed on the ASCII values of the characters
that make up the strings and the result will be a string. In all other
cases, both operands will be
<a href="/language/types/integer.html#language.types.integer.casting" class="link">converted to integers</a>
and the result will be an integer.

If the operand for the *\~* operator is a string, the operation will be
performed on the ASCII values of the characters that make up the string
and the result will be a string, otherwise the operand and the result
will be treated as integers.

Both operands and the result for the *\<\<* and *\>\>* operators are
always treated as integers.

``` literallayout
PHP 的 ini 设定 error_reporting 使用了按位的值，
提供了关闭某个位的真实例子。要显示除了提示级别
之外的所有错误，php.ini 中是这样用的：
E_ALL & ~E_NOTICE
      
```

``` literallayout
具体运作方式是先取得 E_ALL 的值：
00000000000000000111011111111111
再取得 E_NOTICE 的值：
00000000000000000000000000001000
然后通过 ~ 将其取反：
11111111111111111111111111110111
最后再用按位与 AND（&）得到两个值中都设定了（为 1）的位：
00000000000000000111011111110111
      
```

``` literallayout
另外一个方法是用按位异或 XOR（^）来取得只在
其中一个值中设定了的位：
E_ALL ^ E_NOTICE
      
```

``` literallayout
error_reporting 也可用来演示怎样置位。只显示错误和可恢复
错误的方法是：
E_ERROR | E_RECOVERABLE_ERROR
      
```

``` literallayout
也就是将 E_ERROR
00000000000000000000000000000001
和 E_RECOVERABLE_ERROR
00000000000000000001000000000000
用按位或 OR（|）运算符来取得在任何一个值中被置位的结果：
00000000000000000001000000000001
      
```

**示例 \#1 整数的 AND，OR 和 XOR 位运算符**

``` php
<?php
/*
 * Ignore the top section,
 * it is just formatting to make output clearer.
 */

$format = '(%1$2d = %1$04b) = (%2$2d = %2$04b)'
        . ' %3$s (%4$2d = %4$04b)' . "\n";

echo <<<EOH
 ---------     ---------  -- ---------
 result        value      op test
 ---------     ---------  -- ---------
EOH;


/*
 * Here are the examples.
 */

$values = array(0, 1, 2, 4, 8);
$test = 1 + 4;

echo "\n Bitwise AND \n";
foreach ($values as $value) {
    $result = $value & $test;
    printf($format, $result, $value, '&', $test);
}

echo "\n Bitwise Inclusive OR \n";
foreach ($values as $value) {
    $result = $value | $test;
    printf($format, $result, $value, '|', $test);
}

echo "\n Bitwise Exclusive OR (XOR) \n";
foreach ($values as $value) {
    $result = $value ^ $test;
    printf($format, $result, $value, '^', $test);
}
?>
```

以上例程会输出：

     ---------     ---------  -- ---------
     result        value      op test
     ---------     ---------  -- ---------
     Bitwise AND
    ( 0 = 0000) = ( 0 = 0000) & ( 5 = 0101)
    ( 1 = 0001) = ( 1 = 0001) & ( 5 = 0101)
    ( 0 = 0000) = ( 2 = 0010) & ( 5 = 0101)
    ( 4 = 0100) = ( 4 = 0100) & ( 5 = 0101)
    ( 0 = 0000) = ( 8 = 1000) & ( 5 = 0101)

     Bitwise Inclusive OR
    ( 5 = 0101) = ( 0 = 0000) | ( 5 = 0101)
    ( 5 = 0101) = ( 1 = 0001) | ( 5 = 0101)
    ( 7 = 0111) = ( 2 = 0010) | ( 5 = 0101)
    ( 5 = 0101) = ( 4 = 0100) | ( 5 = 0101)
    (13 = 1101) = ( 8 = 1000) | ( 5 = 0101)

     Bitwise Exclusive OR (XOR)
    ( 5 = 0101) = ( 0 = 0000) ^ ( 5 = 0101)
    ( 4 = 0100) = ( 1 = 0001) ^ ( 5 = 0101)
    ( 7 = 0111) = ( 2 = 0010) ^ ( 5 = 0101)
    ( 1 = 0001) = ( 4 = 0100) ^ ( 5 = 0101)
    (13 = 1101) = ( 8 = 1000) ^ ( 5 = 0101)

**示例 \#2 字符串的 XOR 运算符**

``` php
<?php
echo 12 ^ 9; // Outputs '5'

echo "12" ^ "9"; // Outputs the Backspace character (ascii 8)
                 // ('1' (ascii 49)) ^ ('9' (ascii 57)) = #8

echo "hallo" ^ "hello"; // Outputs the ascii values #0 #4 #0 #0 #0
                        // 'a' ^ 'e' = #4

echo 2 ^ "3"; // Outputs 1
              // 2 ^ ((int)"3") == 1

echo "2" ^ 3; // Outputs 1
              // ((int)"2") ^ 3 == 1
?>
```

**示例 \#3 整数的位移**

``` php
<?php
/*
 * Here are the examples.
 */

echo "\n--- BIT SHIFT RIGHT ON POSITIVE INTEGERS ---\n";

$val = 4;
$places = 1;
$res = $val >> $places;
p($res, $val, '>>', $places, 'copy of sign bit shifted into left side');

$val = 4;
$places = 2;
$res = $val >> $places;
p($res, $val, '>>', $places);

$val = 4;
$places = 3;
$res = $val >> $places;
p($res, $val, '>>', $places, 'bits shift out right side');

$val = 4;
$places = 4;
$res = $val >> $places;
p($res, $val, '>>', $places, 'same result as above; can not shift beyond 0');


echo "\n--- BIT SHIFT RIGHT ON NEGATIVE INTEGERS ---\n";

$val = -4;
$places = 1;
$res = $val >> $places;
p($res, $val, '>>', $places, 'copy of sign bit shifted into left side');

$val = -4;
$places = 2;
$res = $val >> $places;
p($res, $val, '>>', $places, 'bits shift out right side');

$val = -4;
$places = 3;
$res = $val >> $places;
p($res, $val, '>>', $places, 'same result as above; can not shift beyond -1');


echo "\n--- BIT SHIFT LEFT ON POSITIVE INTEGERS ---\n";

$val = 4;
$places = 1;
$res = $val << $places;
p($res, $val, '<<', $places, 'zeros fill in right side');

$val = 4;
$places = (PHP_INT_SIZE * 8) - 4;
$res = $val << $places;
p($res, $val, '<<', $places);

$val = 4;
$places = (PHP_INT_SIZE * 8) - 3;
$res = $val << $places;
p($res, $val, '<<', $places, 'sign bits get shifted out');

$val = 4;
$places = (PHP_INT_SIZE * 8) - 2;
$res = $val << $places;
p($res, $val, '<<', $places, 'bits shift out left side');


echo "\n--- BIT SHIFT LEFT ON NEGATIVE INTEGERS ---\n";

$val = -4;
$places = 1;
$res = $val << $places;
p($res, $val, '<<', $places, 'zeros fill in right side');

$val = -4;
$places = (PHP_INT_SIZE * 8) - 3;
$res = $val << $places;
p($res, $val, '<<', $places);

$val = -4;
$places = (PHP_INT_SIZE * 8) - 2;
$res = $val << $places;
p($res, $val, '<<', $places, 'bits shift out left side, including sign bit');


/*
 * Ignore this bottom section,
 * it is just formatting to make output clearer.
 */

function p($res, $val, $op, $places, $note = '') {
    $format = '%0' . (PHP_INT_SIZE * 8) . "b\n";

    printf("Expression: %d = %d %s %d\n", $res, $val, $op, $places);

    echo " Decimal:\n";
    printf("  val=%d\n", $val);
    printf("  res=%d\n", $res);

    echo " Binary:\n";
    printf('  val=' . $format, $val);
    printf('  res=' . $format, $res);

    if ($note) {
        echo " NOTE: $note\n";
    }

    echo "\n";
}
?>
```

以上例程在 32 位机器上的输出:


    --- BIT SHIFT RIGHT ON POSITIVE INTEGERS ---
    Expression: 2 = 4 >> 1
     Decimal:
      val=4
      res=2
     Binary:
      val=00000000000000000000000000000100
      res=00000000000000000000000000000010
     NOTE: copy of sign bit shifted into left side

    Expression: 1 = 4 >> 2
     Decimal:
      val=4
      res=1
     Binary:
      val=00000000000000000000000000000100
      res=00000000000000000000000000000001

    Expression: 0 = 4 >> 3
     Decimal:
      val=4
      res=0
     Binary:
      val=00000000000000000000000000000100
      res=00000000000000000000000000000000
     NOTE: bits shift out right side

    Expression: 0 = 4 >> 4
     Decimal:
      val=4
      res=0
     Binary:
      val=00000000000000000000000000000100
      res=00000000000000000000000000000000
     NOTE: same result as above; can not shift beyond 0


    --- BIT SHIFT RIGHT ON NEGATIVE INTEGERS ---
    Expression: -2 = -4 >> 1
     Decimal:
      val=-4
      res=-2
     Binary:
      val=11111111111111111111111111111100
      res=11111111111111111111111111111110
     NOTE: copy of sign bit shifted into left side

    Expression: -1 = -4 >> 2
     Decimal:
      val=-4
      res=-1
     Binary:
      val=11111111111111111111111111111100
      res=11111111111111111111111111111111
     NOTE: bits shift out right side

    Expression: -1 = -4 >> 3
     Decimal:
      val=-4
      res=-1
     Binary:
      val=11111111111111111111111111111100
      res=11111111111111111111111111111111
     NOTE: same result as above; can not shift beyond -1


    --- BIT SHIFT LEFT ON POSITIVE INTEGERS ---
    Expression: 8 = 4 << 1
     Decimal:
      val=4
      res=8
     Binary:
      val=00000000000000000000000000000100
      res=00000000000000000000000000001000
     NOTE: zeros fill in right side

    Expression: 1073741824 = 4 << 28
     Decimal:
      val=4
      res=1073741824
     Binary:
      val=00000000000000000000000000000100
      res=01000000000000000000000000000000

    Expression: -2147483648 = 4 << 29
     Decimal:
      val=4
      res=-2147483648
     Binary:
      val=00000000000000000000000000000100
      res=10000000000000000000000000000000
     NOTE: sign bits get shifted out

    Expression: 0 = 4 << 30
     Decimal:
      val=4
      res=0
     Binary:
      val=00000000000000000000000000000100
      res=00000000000000000000000000000000
     NOTE: bits shift out left side


    --- BIT SHIFT LEFT ON NEGATIVE INTEGERS ---
    Expression: -8 = -4 << 1
     Decimal:
      val=-4
      res=-8
     Binary:
      val=11111111111111111111111111111100
      res=11111111111111111111111111111000
     NOTE: zeros fill in right side

    Expression: -2147483648 = -4 << 29
     Decimal:
      val=-4
      res=-2147483648
     Binary:
      val=11111111111111111111111111111100
      res=10000000000000000000000000000000

    Expression: 0 = -4 << 30
     Decimal:
      val=-4
      res=0
     Binary:
      val=11111111111111111111111111111100
      res=00000000000000000000000000000000
     NOTE: bits shift out left side, including sign bit

以上例程在 64 位机器上的输出:


    --- BIT SHIFT RIGHT ON POSITIVE INTEGERS ---
    Expression: 2 = 4 >> 1
     Decimal:
      val=4
      res=2
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0000000000000000000000000000000000000000000000000000000000000010
     NOTE: copy of sign bit shifted into left side

    Expression: 1 = 4 >> 2
     Decimal:
      val=4
      res=1
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0000000000000000000000000000000000000000000000000000000000000001

    Expression: 0 = 4 >> 3
     Decimal:
      val=4
      res=0
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0000000000000000000000000000000000000000000000000000000000000000
     NOTE: bits shift out right side

    Expression: 0 = 4 >> 4
     Decimal:
      val=4
      res=0
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0000000000000000000000000000000000000000000000000000000000000000
     NOTE: same result as above; can not shift beyond 0


    --- BIT SHIFT RIGHT ON NEGATIVE INTEGERS ---
    Expression: -2 = -4 >> 1
     Decimal:
      val=-4
      res=-2
     Binary:
      val=1111111111111111111111111111111111111111111111111111111111111100
      res=1111111111111111111111111111111111111111111111111111111111111110
     NOTE: copy of sign bit shifted into left side

    Expression: -1 = -4 >> 2
     Decimal:
      val=-4
      res=-1
     Binary:
      val=1111111111111111111111111111111111111111111111111111111111111100
      res=1111111111111111111111111111111111111111111111111111111111111111
     NOTE: bits shift out right side

    Expression: -1 = -4 >> 3
     Decimal:
      val=-4
      res=-1
     Binary:
      val=1111111111111111111111111111111111111111111111111111111111111100
      res=1111111111111111111111111111111111111111111111111111111111111111
     NOTE: same result as above; can not shift beyond -1


    --- BIT SHIFT LEFT ON POSITIVE INTEGERS ---
    Expression: 8 = 4 << 1
     Decimal:
      val=4
      res=8
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0000000000000000000000000000000000000000000000000000000000001000
     NOTE: zeros fill in right side

    Expression: 4611686018427387904 = 4 << 60
     Decimal:
      val=4
      res=4611686018427387904
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0100000000000000000000000000000000000000000000000000000000000000

    Expression: -9223372036854775808 = 4 << 61
     Decimal:
      val=4
      res=-9223372036854775808
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=1000000000000000000000000000000000000000000000000000000000000000
     NOTE: sign bits get shifted out

    Expression: 0 = 4 << 62
     Decimal:
      val=4
      res=0
     Binary:
      val=0000000000000000000000000000000000000000000000000000000000000100
      res=0000000000000000000000000000000000000000000000000000000000000000
     NOTE: bits shift out left side


    --- BIT SHIFT LEFT ON NEGATIVE INTEGERS ---
    Expression: -8 = -4 << 1
     Decimal:
      val=-4
      res=-8
     Binary:
      val=1111111111111111111111111111111111111111111111111111111111111100
      res=1111111111111111111111111111111111111111111111111111111111111000
     NOTE: zeros fill in right side

    Expression: -9223372036854775808 = -4 << 61
     Decimal:
      val=-4
      res=-9223372036854775808
     Binary:
      val=1111111111111111111111111111111111111111111111111111111111111100
      res=1000000000000000000000000000000000000000000000000000000000000000

    Expression: 0 = -4 << 62
     Decimal:
      val=-4
      res=0
     Binary:
      val=1111111111111111111111111111111111111111111111111111111111111100
      res=0000000000000000000000000000000000000000000000000000000000000000
     NOTE: bits shift out left side, including sign bit

**Warning**

Prior to PHP 7.0, shifting integers by values greater than or equal to
the system long integer width, or by negative numbers, results in
undefined behavior. In other words, if you're using PHP 5.x, don't shift
more than 31 bits on a 32-bit system, and don't shift more than 63 bits
on 64-bit system.

使用 <a href="/book/gmp.html" class="link">gmp</a> 扩展对超出
*PHP\_INT\_MAX* 的数值来进行位操作。

参见 <span class="function">pack</span>, <span
class="function">unpack</span>, <span class="function">gmp\_and</span>,
<span class="function">gmp\_or</span>, <span
class="function">gmp\_xor</span>, <span
class="function">gmp\_testbit</span>, <span
class="function">gmp\_clrbit</span>
