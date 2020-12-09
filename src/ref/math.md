abs
===

绝对值

### 说明

<span class="type">number</span> <span class="methodname">abs</span> (
<span class="methodparam"><span class="type">mixed</span>
`$number`</span> )

返回参数 `number` 的绝对值。

### 参数

`number`  
要处理的数字值

### 返回值

`number` 的绝对值。 如果参数 `number` 是 <span
class="type">float</span>，则返回的类型也是 <span
class="type">float</span>，否则返回 <span
class="type">integer</span>（因为 <span class="type">float</span> 通常比
<span class="type">integer</span> 有更大的取值范围）。

### 范例

**示例 \#1 <span class="function">abs</span> 例子**

``` php
<?php
$abs = abs(-4.2); // $abs = 4.2; (double/float)
$abs2 = abs(5);   // $abs2 = 5; (integer)
$abs3 = abs(-5);  // $abs3 = 5; (integer)
?>
```

### 参见

-   <span class="function">gmp\_abs</span>
-   <span class="function">gmp\_sign</span>

acos
====

反余弦

### 说明

<span class="type">float</span> <span class="methodname">acos</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的反余弦值，单位是弧度。<span class="function">acos</span> 是
<span class="function">cos</span> 的反函数，它的意思是在 <span
class="function">acos</span> 范围里的每个值都是 *a==cos(acos(a))* 。

### 参数

`arg`  
要处理的参数

### 返回值

`arg` 的反余弦弧度。

### 参见

-   <span class="function">cos</span>
-   <span class="function">acosh</span>
-   <span class="function">asin</span>
-   <span class="function">atan</span>

acosh
=====

反双曲余弦

### 说明

<span class="type">float</span> <span class="methodname">acosh</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的反双曲余弦值，即，其双曲余弦为 `arg` 的那个值。

### 参数

`arg`  
要处理的值

### 返回值

The inverse hyperbolic cosine of `arg`

### 更新日志

| 版本  | 说明                                            |
|-------|-------------------------------------------------|
| 5.3.0 | This function is now available on all platforms |

### 参见

-   <span class="function">cosh</span>
-   <span class="function">acos</span>
-   <span class="function">asinh</span>
-   <span class="function">atanh</span>

asin
====

反正弦

### 说明

<span class="type">float</span> <span class="methodname">asin</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的反正弦值，单位是弧度。<span class="function">asin</span> 是
<span class="function">sin</span> 的反函数，它的意思是在 <span
class="function">asin</span> 范围里的每个值都是 *a==sin(asin(a))* 。

### 参数

`arg`  
待处理的参数

### 返回值

`arg` 的反正弦弧度。

### 参见

-   <span class="function">sin</span>
-   <span class="function">asinh</span>
-   <span class="function">acos</span>
-   <span class="function">atan</span>

asinh
=====

反双曲正弦

### 说明

<span class="type">float</span> <span class="methodname">asinh</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的反双曲正弦值，即，其双曲正弦为 `arg` 的那个值。

### 参数

`arg`  
要处理的参数

### 返回值

返回 `arg` 的反双曲正弦值

### 更新日志

| 版本  | 说明                     |
|-------|--------------------------|
| 5.3.0 | 此函数在所有平台上均可用 |

### 参见

-   <span class="function">sinh</span>
-   <span class="function">asin</span>
-   <span class="function">acosh</span>
-   <span class="function">atanh</span>

atan2
=====

两个参数的反正切

### 说明

<span class="type">float</span> <span class="methodname">atan2</span> (
<span class="methodparam"><span class="type">float</span> `$y`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> )

本函数计算两个变量 `x` 和 `y` 的反正切值。和计算 `y` / `x`
的反正切相似，只除了两个参数的符号是用来确定结果的象限之外。

本函数的结果为弧度，其值在 -PI 和 PI 之间（包括 -PI 和 PI）。

### 参数

`y`  
Dividend parameter

`x`  
Divisor parameter

### 返回值

`x` 和 `y` 的反正切弧度值。

### 参见

-   <span class="function">atan</span>

atan
====

反正切

### 说明

<span class="type">float</span> <span class="methodname">atan</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的反正切值，单位是弧度。<span class="function">atan</span> 是
<span class="function">tan</span> 的反函数，它的意思是在 <span
class="function">atan</span> 范围里的每个值都是 *a==tan(atan(a))*。

### 参数

`arg`  
要处理的参数

### 返回值

`arg` 的反正切弧度。

### 参见

-   <span class="function">tan</span>
-   <span class="function">atanh</span>
-   <span class="function">asin</span>
-   <span class="function">acos</span>

atanh
=====

反双曲正切

### 说明

<span class="type">float</span> <span class="methodname">atanh</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的反双曲正切值，即，其双曲正切为 `arg` 的那个值。

### 参数

`arg`  
要处理的参数

### 返回值

Inverse hyperbolic tangent of `arg`

### 更新日志

| 版本  | 说明                         |
|-------|------------------------------|
| 5.3.0 | 此函数在所有平台上都可以用了 |

### 参见

-   <span class="function">tanh</span>
-   <span class="function">atan</span>
-   <span class="function">asinh</span>
-   <span class="function">acosh</span>

base\_convert
=============

在任意进制之间转换数字

### 说明

<span class="type">string</span> <span
class="methodname">base\_convert</span> ( <span
class="methodparam"><span class="type">string</span> `$number`</span> ,
<span class="methodparam"><span class="type">int</span>
`$frombase`</span> , <span class="methodparam"><span
class="type">int</span> `$tobase`</span> )

返回一字符串，包含 `number` 以 `tobase` 进制的表示。`number`
本身的进制由 `frombase` 指定。`frombase` 和 `tobase` 都只能在 2 和 36
之间（包括 2 和 36）。高于十进制的数字用字母 a-z 表示，例如 a 表示 10，b
表示 11 以及 z 表示 35。

**Warning**

由于使用内部的 "double" 或 "float" 类型，<span
class="function">base\_convert</span>
的操作可能会导致大数值中的精度丢失。请参见本手册的
<a href="/language/types/float.html" class="link">浮点数</a>
章节以便获得更多详细信息。

### 参数

`number`  
要转换的数字

`frombase`  
The base `number` is in

`tobase`  
The base to convert `number` to

### 返回值

`number` converted to base `tobase`

### 范例

**示例 \#1 <span class="function">base\_convert</span> 例子**

``` php
<?php
$hexadecimal = 'A37334';
echo base_convert($hexadecimal, 16, 2);
?>
```

以上例程会输出：

    101000110111001100110100

### 参见

-   <span class="function">intval</span>

bindec
======

二进制转换为十进制

### 说明

<span class="type">number</span> <span class="methodname">bindec</span>
( <span class="methodparam"><span class="type">string</span>
`$binary_string`</span> )

返回 `binary_string` 参数所表示的二进制数的十进制等价值。

<span class="function">bindec</span> 将一个二进制数转换成 <span
class="type">integer</span>，或者出于大小的需要，转换为 <span
class="type">float</span> 类型。

<span class="function">bindec</span> 将所有的 `binary_string`
值解释为无符号整数。这是由于 <span class="function">bindec</span>
函数将其最高有效位视为数量级而非符号位。

### 参数

`binary_string`  
要转换的二进制字符串

**Warning**

参数必须为字符串。使用其他数据类型会导致不可预知的结果。

### 返回值

`binary_string` 的十进制数值

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.1.0 | 本函数如今可以转换超过程序运行平台中 <span class="type">integer</span> 类型最大值的数，此时其值会返回为 <span class="type">float</span> 类型。 |

### 范例

**示例 \#1 <span class="function">bindec</span> 例子**

``` php
<?php
echo bindec('110011') . "\n";
echo bindec('000110011') . "\n";

echo bindec('111');
?>
```

以上例程会输出：

    51
    51
    7

**示例 \#2 <span class="function">bindec</span> 将输入解读为无符号整数**

``` php
<?php
/*
 * The lesson from this example is in the output
 * rather than the PHP code itself.
 */

$magnitude_lower = pow(2, (PHP_INT_SIZE * 8) - 2);
p($magnitude_lower - 1);
p($magnitude_lower, 'See the rollover?  Watch it next time around...');

p(PHP_INT_MAX, 'PHP_INT_MAX');
p(~PHP_INT_MAX, 'interpreted to be one more than PHP_INT_MAX');

if (PHP_INT_SIZE == 4) {
    $note = 'interpreted to be the largest unsigned integer';
} else {
    $note = 'interpreted to be the largest unsigned integer
              (18446744073709551615) but skewed by float precision';
}
p(-1, $note);


function p($input, $note = '') {
    echo "input:        $input\n";

    $format = '%0' . (PHP_INT_SIZE * 8) . 'b';
    $bin = sprintf($format, $input);
    echo "binary:       $bin\n";

    ini_set('precision', 20);  // For readability on 64 bit boxes.
    $dec = bindec($bin);
    echo 'bindec():     ' . $dec . "\n";

    if ($note) {
        echo "NOTE:         $note\n";
    }

    echo "\n";
}
?>
```

以上例程在 32 位机器上的输出:

    input:        1073741823
    binary:       00111111111111111111111111111111
    bindec():     1073741823

    input:        1073741824
    binary:       01000000000000000000000000000000
    bindec():     1073741824
    NOTE:         See the rollover?  Watch it next time around...

    input:        2147483647
    binary:       01111111111111111111111111111111
    bindec():     2147483647
    NOTE:         PHP_INT_MAX

    input:        -2147483648
    binary:       10000000000000000000000000000000
    bindec():     2147483648
    NOTE:         interpreted to be one more than PHP_INT_MAX

    input:        -1
    binary:       11111111111111111111111111111111
    bindec():     4294967295
    NOTE:         interpreted to be the largest unsigned integer

以上例程在 64 位机器上的输出:

    input:        4611686018427387903
    binary:       0011111111111111111111111111111111111111111111111111111111111111
    bindec():     4611686018427387903

    input:        4611686018427387904
    binary:       0100000000000000000000000000000000000000000000000000000000000000
    bindec():     4611686018427387904
    NOTE:         See the rollover?  Watch it next time around...

    input:        9223372036854775807
    binary:       0111111111111111111111111111111111111111111111111111111111111111
    bindec():     9223372036854775807
    NOTE:         PHP_INT_MAX

    input:        -9223372036854775808
    binary:       1000000000000000000000000000000000000000000000000000000000000000
    bindec():     9223372036854775808
    NOTE:         interpreted to be one more than PHP_INT_MAX

    input:        -1
    binary:       1111111111111111111111111111111111111111111111111111111111111111
    bindec():     18446744073709551616
    NOTE:         interpreted to be the largest unsigned integer
                  (18446744073709551615) but skewed by float precision

### 参见

-   <span class="function">decbin</span>
-   <span class="function">octdec</span>
-   <span class="function">hexdec</span>
-   <span class="function">base\_convert</span>

ceil
====

进一法取整

### 说明

<span class="type">float</span> <span class="methodname">ceil</span> (
<span class="methodparam"><span class="type">float</span>
`$value`</span> )

返回不小于 `value` 的下一个整数，`value` 如果有小数部分则进一位。

### 参数

`value`  
要进一法取整的值

### 返回值

返回不小于 `value` 的下一个整数。 <span class="function">ceil</span>
返回的类型仍然是 <span class="type">float</span>，因为 <span
class="type">float</span> 值的范围通常比 <span
class="type">integer</span> 要大。

### 范例

**示例 \#1 <span class="function">ceil</span> 例子**

``` php
<?php
echo ceil(4.3);    // 5
echo ceil(9.999);  // 10
echo ceil(-3.14);  // -3
?>
```

### 参见

-   <span class="function">floor</span>
-   <span class="function">round</span>

cos
===

余弦

### 说明

<span class="type">float</span> <span class="methodname">cos</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

<span class="function">cos</span> 返回参数 `arg` 的余弦值。参数 `arg`
的单位为弧度。

### 参数

`arg`  
以弧度表示的角度

### 返回值

`arg`的余弦值

### 范例

**示例 \#1 <span class="function">cos</span> 例子**

``` php
<?php

echo cos(M_PI); // -1

?>
```

### 参见

-   <span class="function">acos</span>
-   <span class="function">sin</span>
-   <span class="function">tan</span>
-   <span class="function">deg2rad</span>

cosh
====

双曲余弦

### 说明

<span class="type">float</span> <span class="methodname">cosh</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的双曲余弦值，定义为 *(exp(arg) + exp(-arg))/2*。

### 参数

`arg`  
要处理的参数

### 返回值

`arg` 的双曲余弦值。

### 参见

-   <span class="function">cos</span>
-   <span class="function">acosh</span>
-   <span class="function">sinh</span>
-   <span class="function">cosh</span>

decbin
======

十进制转换为二进制

### 说明

<span class="type">string</span> <span class="methodname">decbin</span>
( <span class="methodparam"><span class="type">int</span>
`$number`</span> )

返回一字符串，包含有给定 `number`
参数的二进制表示。所能转换的最大数值为十进制的 4294967295，其结果为 32
个 1 的字符串。

### 参数

`number`  
Decimal value to convert

**Range of inputs on 32-bit machines**

positive `number`

### 返回值

Binary string representation of `number`

### 范例

**示例 \#1 <span class="function">decbin</span> 例子**

``` php
<?php
echo decbin(12) . "\n";
echo decbin(26);
?>
```

以上例程会输出：

    1100
    11010

### 参见

-   <span class="function">bindec</span>
-   <span class="function">decoct</span>
-   <span class="function">dechex</span>
-   <span class="function">base\_convert</span>
-   <span class="function">printf</span>, using *%b*, *%032b* or *%064b*
    as the format
-   <span class="function">sprintf</span>, using *%b*, *%032b* or
    *%064b* as the format

dechex
======

十进制转换为十六进制

### 说明

<span class="type">string</span> <span class="methodname">dechex</span>
( <span class="methodparam"><span class="type">int</span>
`$number`</span> )

返回一字符串，包含有给定 `number` 参数的十六进制表示。

所能转换的最大数值为十进制的 **`PHP_INT_MAX`** *\* 2 + 1* (或 *-1*)：在
32 位平台上是十进制的 *4294967295*，其 <span
class="function">dechex</span> 的结果为 *ffffffff*。

### 参数

`number`  
要转换的十进制值

PHP 的 <span class="type">integer</span> 类型是有符号的，但 <span
class="function">dechex</span> 处理无符号整数，负正数会以无符号处理。

### 返回值

`number` 的16进制表示

### 范例

**示例 \#1 <span class="function">dechex</span> 例子**

``` php
<?php
echo dechex(10) . "\n";
echo dechex(47);
?>
```

以上例程会输出：

    a
    2f

**示例 \#2 大整数的 <span class="function">dechex</span> 例子**

``` php
<?php
// The output below assumes a 32-bit platform.
// Note that the output is the same for all values.
echo dechex(-1)."\n";
echo dechex(PHP_INT_MAX * 2 + 1)."\n";
echo dechex(pow(2, 32) - 1)."\n";
?>
```

以上例程会输出：

    ffffffff
    ffffffff
    ffffffff

### 参见

-   <span class="function">hexdec</span>
-   <span class="function">decbin</span>
-   <span class="function">decoct</span>
-   <span class="function">base\_convert</span>

decoct
======

十进制转换为八进制

### 说明

<span class="type">string</span> <span class="methodname">decoct</span>
( <span class="methodparam"><span class="type">int</span>
`$number`</span> )

返回一字符串，包含有给定 `number`
参数的八进制表示。所能转换的最大数值为十进制的 4294967295，其结果为
"37777777777"。

### 参数

`number`  
待转换的十进制值

### 返回值

`number` 参数八进制表示的字符串。

### 范例

**示例 \#1 <span class="function">decoct</span> 范例**

``` php
<?php
echo decoct(15) . "\n";
echo decoct(264);
?>
```

以上例程会输出：

    17
    410

### 参见

-   <span class="function">octdec</span>
-   <span class="function">decbin</span>
-   <span class="function">dechex</span>
-   <span class="function">base\_convert</span>

deg2rad
=======

将角度转换为弧度

### 说明

<span class="type">float</span> <span class="methodname">deg2rad</span>
( <span class="methodparam"><span class="type">float</span>
`$number`</span> )

本函数把 `number` 从角度转换成弧度。

### 参数

`number`  
以角度为单位的值

### 返回值

`number` 等量的弧度值

### 范例

**示例 \#1 <span class="function">deg2rad</span> 例子**

``` php
<?php

echo deg2rad(45); // 0.785398163397
var_dump(deg2rad(45) === M_PI_4); // bool(true)

?>
```

### 参见

-   <span class="function">rad2deg</span>

exp
===

计算 **`e`** 的指数

### 说明

<span class="type">float</span> <span class="methodname">exp</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 **`e`** 的 `arg` 次方值。

> **Note**:
>
> 用 '**`e`**' 作为自然对数的底 2.718282.

### 参数

`arg`  
要处理的参数

### 返回值

'e' raised to the power of `arg`

### 范例

**示例 \#1 <span class="function">exp</span> 例子**

``` php
<?php
echo exp(12) . "\n";
echo exp(5.7);
?>
```

以上例程会输出：

    1.6275E+005
    298.87

### 参见

-   <span class="function">log</span>
-   <span class="function">pow</span>

expm1
=====

返回 exp(number) - 1，甚至当 number 的值接近零也能计算出准确结果

### 说明

<span class="type">float</span> <span class="methodname">expm1</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

<span class="function">expm1</span> 返回 'exp(`number`) - 1'，甚至当
`number` 的值接近零也能计算出准确结果。但是当两个数值趋近于相等的时候，
'exp (`number`) - 1' 就会变得不太准确。

### 参数

`arg`  
要处理的参数

### 返回值

'e' to the power of `arg` minus one

### 更新日志

| 版本  | 说明                     |
|-------|--------------------------|
| 5.3.0 | 此函数在所有平台上均可用 |

### 参见

-   <span class="function">log1p</span>
-   <span class="function">exp</span>

floor
=====

舍去法取整

### 说明

<span class="type">float</span> <span class="methodname">floor</span> (
<span class="methodparam"><span class="type">float</span>
`$value`</span> )

返回不大于 `value` 的最接近的整数，舍去小数部分取整。

### 参数

`value`  
要取整的数字

### 返回值

返回不大于 `value` 的最接近的整数，将 `value` 的小数部分舍去取整。<span
class="function">floor</span> 返回的类型仍然是 <span
class="type">float</span>，因为 <span class="type">float</span>
值的范围通常比 <span class="type">integer</span> 要大。

### 范例

**示例 \#1 <span class="function">floor</span> 例子**

``` php
<?php
echo floor(4.3);   // 4
echo floor(9.999); // 9
echo floor(-3.14); // -4
?>
```

### 参见

-   <span class="function">ceil</span>
-   <span class="function">round</span>

fmod
====

返回除法的浮点数余数

### 说明

<span class="type">float</span> <span class="methodname">fmod</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

返回被除数（`x`）除以除数（`y`）所得的浮点数余数。余数（`r`）的定义是：x
= i \* y + r，其中 `i` 是整数。如果 `y` 是非零值，则 `r` 和 `x`
的符号相同并且其数量值小于 `y`。

### 参数

`x`  
被除数

`y`  
除数

### 返回值

`x`/`y`的浮点数余数。

### 范例

**示例 \#1 <span class="function">fmod</span> 的使用**

``` php
<?php
$x = 5.7;
$y = 1.3;
$r = fmod($x, $y);
// $r equals 0.5, because 4 * 1.3 + 0.5 = 5.7
?>
```

getrandmax
==========

显示随机数最大的可能值

### 说明

<span class="type">int</span> <span class="methodname">getrandmax</span>
( <span class="methodparam">void</span> )

返回调用 <span class="function">rand</span> 可能返回的最大值。

### 返回值

<span class="function">rand</span> 返回 随机数可能返回的最大值

### 参见

-   <span class="function">rand</span>
-   <span class="function">srand</span>
-   <span class="function">mt\_getrandmax</span>

hexdec
======

十六进制转换为十进制

### 说明

<span class="type">number</span> <span class="methodname">hexdec</span>
( <span class="methodparam"><span class="type">string</span>
`$hex_string`</span> )

返回与 `hex_string` 参数所表示的十六进制数等值的的十进制数。<span
class="function">hexdec</span> 将一个十六进制字符串转换为十进制数。

<span class="function">hexdec</span>
会忽略它遇到的任意非十六进制的字符。

### 参数

`hex_string`  
要转换的十六进制的字符串

### 返回值

`hex_string` 十进制的表示

### 更新日志

| 版本  | 说明                                                                                                                                 |
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| 4.1.0 | PHP 4.1.0 开始，该函数可以处理 <span class="type">integer</span> 大数字，这种情况下，它会返回 <span class="type">float</span> 类型。 |

### 范例

**示例 \#1 <span class="function">hexdec</span> 例子**

``` php
<?php
var_dump(hexdec("See"));
var_dump(hexdec("ee"));
// both print "int(238)"

var_dump(hexdec("that")); // print "int(10)"
var_dump(hexdec("a0")); // print "int(160)"
?>
```

### 参见

-   <span class="function">dechex</span>
-   <span class="function">bindec</span>
-   <span class="function">octdec</span>
-   <span class="function">base\_convert</span>

hypot
=====

计算一直角三角形的斜边长度

### 说明

<span class="type">float</span> <span class="methodname">hypot</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="function">hypot</span> 函数将会跟据直角三角形的两直解边长度
`x` 和 `y` 计算其斜边的长度。或者是从标点 (`x`, `y`)
到原点的距离。该函数的算法等同于 *sqrt(x\*x + y\*y)*。

### 参数

`x`  
第一条边的长度

`y`  
第二条边的长度

### 返回值

计算斜边的长度

intdiv
======

对除法结果取整

### 说明

<span class="type">int</span> <span class="methodname">intdiv</span> (
<span class="methodparam"><span class="type">int</span>
`$dividend`</span> , <span class="methodparam"><span
class="type">int</span> `$divisor`</span> )

返回 `dividend` 除以 `divisor` 商数的整数部分。

### 参数

`dividend`  
被除数。

`divisor`  
除数。

### 返回值

`dividend` 除以 `divisor` 的商，对该商取整。

### 错误／异常

如果 `divisor` 是 *0*，将抛出 <span
class="classname">DivisionByZeroError</span> 异常。 如果 `dividend` 是
**`PHP_INT_MIN`** 并且 `divisor` 是 *-1*，将抛出 <span
class="classname">ArithmeticError</span> 异常.

### 范例

**示例 \#1 <span class="function">intdiv</span> 的一些例子**

``` php
<?php
var_dump(intdiv(3, 2));
var_dump(intdiv(-3, 2));
var_dump(intdiv(3, -2));
var_dump(intdiv(-3, -2));
var_dump(intdiv(PHP_INT_MAX, PHP_INT_MAX));
var_dump(intdiv(PHP_INT_MIN, PHP_INT_MIN));
var_dump(intdiv(PHP_INT_MIN, -1));
var_dump(intdiv(1, 0));
?>
```

    int(1)
    int(-1)
    int(-1)
    int(1)
    int(1)
    int(1)

    Fatal error: Uncaught ArithmeticError: Division of PHP_INT_MIN by -1 is not an integer in %s on line 8
    Fatal error: Uncaught DivisionByZeroError: Division by zero in %s on line 9

is\_finite
==========

判断是否为有限值

### 说明

<span class="type">bool</span> <span
class="methodname">is\_finite</span> ( <span class="methodparam"><span
class="type">float</span> `$val`</span> )

检查 `val` 是否是是本机平台上浮点数所允许范围中的一个合法的有限值。

### 参数

`val`  
要检查的值

### 返回值

如果 `val` 是本机平台上 PHP 浮点数所允许范围中的一个合法的有限值，则返回
**`true`**。

### 参见

-   <span class="function">is\_infinite</span>
-   <span class="function">is\_nan</span>

is\_infinite
============

判断是否为无限值

### 说明

<span class="type">bool</span> <span
class="methodname">is\_infinite</span> ( <span class="methodparam"><span
class="type">float</span> `$val`</span> )

如果 `val` 为无穷大（正的或负的），例如 *log(0)*
的结果或者任何超出本平台的浮点数范围的值，则返回 **`true`**。

### 参数

`val`  
要检查的值

### 返回值

如果 `val` 为无穷大返回 **`true`**，否则返回 **`false`**。

### 参见

-   <span class="function">is\_finite</span>
-   <span class="function">is\_nan</span>

is\_nan
=======

判断是否为合法数值

### 说明

<span class="type">bool</span> <span class="methodname">is\_nan</span> (
<span class="methodparam"><span class="type">float</span> `$val`</span>
)

如果 `val` 为“非数值”，例如 *acos(1.01)* 的结果，则返回 **`true`**。

### 参数

`val`  
要检查的值

### 返回值

如果 `val` 不是一个数字（not a number）返回 **`true`**，否则返回
**`false`**。

### 范例

**示例 \#1 <span class="function">is\_nan</span> 例子**

``` php
<?php
// Invalid calculation, will return a 
// NaN value
$nan = acos(8);

var_dump($nan, is_nan($nan));
?>
```

以上例程会输出：

    float(NAN)
    bool(true)

### 参见

-   <span class="function">is\_finite</span>
-   <span class="function">is\_infinite</span>

lcg\_value
==========

组合线性同余发生器

### 说明

<span class="type">float</span> <span
class="methodname">lcg\_value</span> ( <span
class="methodparam">void</span> )

<span class="function">lcg\_value</span> 返回范围为 (0, 1)
的一个伪随机数。本函数组合了周期为 2^31 - 85 和 2^31 - 249
的两个同余发生器。本函数的周期等于这两个素数的乘积。

### 返回值

范围为 (0, 1) 的伪随机数。

### 参见

-   <span class="function">rand</span>
-   <span class="function">mt\_rand</span>

log10
=====

以 10 为底的对数

### 说明

<span class="type">float</span> <span class="methodname">log10</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回参数 `arg` 以 10 为底的对数。

### 参数

`arg`  
要处理的参数

### 返回值

`arg` 以 10 为底的对数。

### 参见

-   <span class="function">log</span>

log1p
=====

返回 log(1 + number)，甚至当 number 的值接近零也能计算出准确结果

### 说明

<span class="type">float</span> <span class="methodname">log1p</span> (
<span class="methodparam"><span class="type">float</span>
`$number`</span> )

<span class="function">log1p</span> 返回 log(1 + `number`)，甚至当
`number` 的值接近零也能计算出准确结果。 <span
class="function">log</span> might only return log(1) in this case due to
lack of precision.

### 参数

`number`  
要处理的参数

### 返回值

log(1 + `number`)

### 更新日志

| 版本  | 说明                     |
|-------|--------------------------|
| 5.3.0 | 此函数在所有平台上均可用 |

### 参见

-   <span class="function">expm1</span>
-   <span class="function">log</span>
-   <span class="function">log10</span>

log
===

自然对数

### 说明

<span class="type">float</span> <span class="methodname">log</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$base`<span class="initializer"> = M\_E</span></span> \] )

如果指定了可选的参数 `base`，<span class="function">log</span> 返回
log<sub>base</sub> `arg`，否则 <span class="function">log</span>
返回参数 `arg` 的自然对数。

### 参数

`arg`  
要计算对数的值

`base`  
The optional logarithmic base to use (defaults to 'e' and so to the
natural logarithm).

### 返回值

返回 log<sub>base</sub> `arg`，或者它的自然对数。

### 更新日志

| 版本  | 说明                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 4.3.0 | 可选参数 `base`可用。 你可以计算任意以 *b* 为底 *n* 的对数，但其实使用的是数学等式：log<sub>b</sub>(n) = log(n)/log(b)，其中 log 是自然对数。 |

### 参见

-   <span class="function">log10</span>
-   <span class="function">exp</span>
-   <span class="function">pow</span>

max
===

找出最大值

### 说明

<span class="type">mixed</span> <span class="methodname">max</span> (
<span class="methodparam"><span class="type">array</span>
`$values`</span> )

<span class="type">mixed</span> <span class="methodname">max</span> (
<span class="methodparam"><span class="type">mixed</span>
`$value1`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value2`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \] )

如果仅有一个参数且为数组，<span class="function">max</span>
返回该数组中最大的值。如果第一个参数是整数、字符串或浮点数，则至少需要两个参数而
<span class="function">max</span>
会返回这些值中最大的一个。可以比较无限多个值。

> **Note**:
>
> PHP 会将非数值的 <span class="type">string</span> 当成
> *0*，但如果这个正是最大的数值则仍然会返回一个字符串。如果多个参数都求值为
> *0* 且是最大值，<span class="function">max</span> 会返回其中数值的
> *0*，如果参数中没有数值的 *0*，则返回按字母表顺序最大的字符串。

### 参数

`values`  
包含了多个值的数组。

`value1`  
Any
<a href="/language/operators/comparison.html" class="link">comparable</a>
value.

`value2`  
Any
<a href="/language/operators/comparison.html" class="link">comparable</a>
value.

`...`  
Any
<a href="/language/operators/comparison.html" class="link">comparable</a>
value.

### 返回值

<span class="function">max</span> 返回参数中数值最大的值。 If multiple
values can be considered of the same size, the one that is listed first
will be returned.

When <span class="function">max</span> is given multiple <span
class="type">array</span>s, the longest array is returned. If all the
arrays have the same length, <span class="function">max</span> will use
lexicographic ordering to find the return value.

When given a <span class="type">string</span> it will be cast as an
<span class="type">integer</span> when comparing.

### 范例

**示例 \#1 使用 <span class="function">max</span> 的例子**

``` php
<?php
echo max(1, 3, 5, 6, 7);  // 7
echo max(array(2, 4, 5)); // 5

// When 'hello' is cast as integer it will be 0. Both the parameters are equally
// long, so the order they are given in determines the result
echo max(0, 'hello');     // 0
echo max('hello', 0);     // hello

echo max('42', 3); // '42'

// Here 0 > -1, so 'hello' is the return value.
echo max(-1, 'hello');    // hello

// With multiple arrays of different lengths, max returns the longest
$val = max(array(2, 2, 2), array(1, 1, 1, 1)); // array(1, 1, 1, 1)

// 对多个数组，max 从左向右比较。
   // 因此在本例中：2 == 2，但 4 < 5
$val = max(array(2, 4, 8), array(2, 5, 7)); // array(2, 5, 7)

// 如果同时给出数组和非数组作为参数，则总是将数组视为
   // 最大值返回
$val = max('string', array(2, 5, 7), 42);   // array(2, 5, 7)
?>
```

### 参见

-   <span class="function">min</span>
-   <span class="function">count</span>

min
===

找出最小值

### 说明

<span class="type">mixed</span> <span class="methodname">min</span> (
<span class="methodparam"><span class="type">array</span>
`$values`</span> )

<span class="type">mixed</span> <span class="methodname">min</span> (
<span class="methodparam"><span class="type">mixed</span>
`$value1`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value2`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \] )

如果仅有一个参数且为数组，<span class="function">min</span>
返回该数组中最小的值。如果给出了两个或更多参数, <span
class="function">min</span> 会返回这些值中最小的一个。

> **Note**:
>
> PHP 会将非数值的 <span class="type">string</span> 当成
> *0*，但如果这个正是最小的数值则仍然会返回一个字符串。如果多个参数都求值为
> *0* 且是最小值，<span class="function">min</span>
> 会返回按字母表顺序最小的字符串，如果其中没有字符串的话，则返回数值的
> *0*。

### 参数

`values`  
包含值的数组。

`value1`  
Any
<a href="/language/operators/comparison.html" class="link">comparable</a>
value.

`value2`  
Any
<a href="/language/operators/comparison.html" class="link">comparable</a>
value.

`...`  
Any
<a href="/language/operators/comparison.html" class="link">comparable</a>
value.

### 返回值

<span class="function">min</span> 返回参数中数值最小的。

### 范例

**示例 \#1 <span class="function">min</span> 用法的例子**

``` php
<?php
echo min(2, 3, 1, 6, 7);  // 1
echo min(array(2, 4, 5)); // 2

echo min(0, 'hello');     // 0
echo min('hello', 0);     // hello
echo min('hello', -1);    // -1

// 对多个数组，min 从左向右比较。
// 因此在本例中：2 == 2，但 4 < 5
$val = min(array(2, 4, 8), array(2, 5, 1)); // array(2, 4, 8)

// 如果同时给出数组和非数组作为参数，则不可能返回数组，因为
// 数组被视为最大的
$val = min('string', array(2, 5, 7), 42);   // string
?>
```

### 参见

-   <span class="function">max</span>
-   <span class="function">count</span>

mt\_getrandmax
==============

显示随机数的最大可能值

### 说明

<span class="type">int</span> <span
class="methodname">mt\_getrandmax</span> ( <span
class="methodparam">void</span> )

返回调用 <span class="function">mt\_rand</span> 所能返回的最大的随机数。

### 返回值

返回调用 <span class="function">mt\_rand</span> 所能返回的最大的随机数。

### 范例

**示例 \#1 计算一个随机浮点数**

``` php
<?php
function randomFloat($min = 0, $max = 1) {
    return $min + mt_rand() / mt_getrandmax() * ($max - $min);
}

var_dump(randomFloat());
var_dump(randomFloat(2, 20));
?>
```

以上例程的输出类似于：

    float(0.91601131712832)
    float(16.511210331931)

### 参见

-   <span class="function">mt\_rand</span>
-   <span class="function">mt\_srand</span>
-   <span class="function">getrandmax</span>

mt\_rand
========

生成更好的随机数

### 说明

<span class="type">int</span> <span class="methodname">mt\_rand</span> (
<span class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">mt\_rand</span> (
<span class="methodparam"><span class="type">int</span> `$min`</span> ,
<span class="methodparam"><span class="type">int</span> `$max`</span> )

很多老的 libc 的随机数发生器具有一些不确定和未知的特性而且很慢。PHP 的
<span class="function">rand</span> 函数默认使用 libc 随机数发生器。<span
class="function">mt\_rand</span> 函数是非正式用来替换它的。该函数用了
<a href="http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html" class="link external">» Mersenne Twister</a>
中已知的特性作为随机数发生器，它可以产生随机数值的平均速度比 libc 提供的
rand() 快四倍。

如果没有提供可选参数 `min` 和 `max`，<span
class="function">mt\_rand</span> 返回 0 到 <span
class="function">mt\_getrandmax</span> 之间的伪随机数。例如想要 5 到
15（包括 5 和 15）之间的随机数，用 *mt\_rand(5, 15)*。

### 参数

`min`  
可选的、返回的最小值（默认：0）

`max`  
可选的、返回的最大值（默认：<span
class="function">mt\_getrandmax</span>）

### 返回值

返回 `min` （或者 0） 到 `max` （或者是到 <span
class="function">mt\_getrandmax</span> ，包含这个值）之间的随机整数。

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 4.2.0 | 随机数发生器自动进行播种。 |

### 范例

**示例 \#1 <span class="function">mt\_rand</span> 例子**

``` php
<?php
echo mt_rand() . "\n";
echo mt_rand() . "\n";

echo mt_rand(5, 15);
?>
```

以上例程的输出类似于：

    1604716014
    1478613278
    6

### 注释

**Caution**

The distribution of <span class="function">mt\_rand</span> return values
is biased towards even numbers on 64-bit builds of PHP when `max` is
beyond *2^32*.

### 参见

-   <span class="function">mt\_srand</span>
-   <span class="function">mt\_getrandmax</span>
-   <span class="function">rand</span>

mt\_srand
=========

播下一个更好的随机数发生器种子

### 说明

<span class="type">void</span> <span class="methodname">mt\_srand</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$seed`</span> \] )

用 `seed` 来给随机数发生器播种。 没有设定 `seed`
参数时，会被设为随时数。

> **Note**: <span class="simpara">不再需要用 <span
> class="function">srand</span> 或 <span
> class="function">mt\_srand</span>
> 给随机数发生器播种，因为现在是由系统自动完成的。</span>

### 参数

`seed`  
可选的种子值

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.2.0 | The `seed` becomes optional and defaults to a random value if omitted.                                                                                                                                                                                                                              |
| 5.2.1 | The Mersenne Twister implementation in PHP now uses a new seeding algorithm by Richard Wagner. Identical seeds no longer produce the same sequence of values they did in previous versions. This behavior is not expected to change again, but it is considered unsafe to rely upon it nonetheless. |

### 范例

**示例 \#1 <span class="function">mt\_srand</span> 例子**

``` php
<?php
// seed with microseconds
function make_seed()
{
  list($usec, $sec) = explode(' ', microtime());
  return (float) $sec + ((float) $usec * 100000);
}
mt_srand(make_seed());
$randval = mt_rand();
?>
```

### 参见

-   <span class="function">mt\_rand</span>
-   <span class="function">mt\_getrandmax</span>
-   <span class="function">srand</span>

octdec
======

八进制转换为十进制

### 说明

<span class="type">number</span> <span class="methodname">octdec</span>
( <span class="methodparam"><span class="type">string</span>
`$octal_string`</span> )

返回 `octal_string` 参数所表示的八进制数的十进制等值。

### 参数

`octal_string`  
要转换的八进制的字符串

### 返回值

`octal_string` 的十进制的表示

### 更新日志

| 版本  | 说明                                                                                                                 |
|-------|----------------------------------------------------------------------------------------------------------------------|
| 4.1.0 | 该函数可以处理 <span class="type">integer</span> 大数字，这种情况下，它会返回 <span class="type">float</span> 类型。 |

### 范例

**示例 \#1 <span class="function">octdec</span> 例子**

``` php
<?php
echo octdec('77') . "\n";
echo octdec(decoct(45));
?>
```

以上例程会输出：

    63
    45

### 参见

-   <span class="function">decoct</span>
-   <span class="function">bindec</span>
-   <span class="function">hexdec</span>
-   <span class="function">base\_convert</span>

pi
==

得到圆周率值

### 说明

<span class="type">float</span> <span class="methodname">pi</span> (
<span class="methodparam">void</span> )

返回圆周率的近似值。返回值的 <span class="type">float</span> 精度是由
`php.ini` 中的
<a href="/ini/core.html#ini.precision" class="link">precision</a>
指令确定。默认值是 *14*。你也可以使用 **`M_PI`** 常量，该常量产生与
<span class="function">pi</span> 完全相同的结果。

### 返回值

圆周率（pi）的浮点近似值。

### 范例

**示例 \#1 <span class="function">pi</span> 例子**

``` php
<?php
echo pi(); // 3.1415926535898
echo M_PI; // 3.1415926535898
?>
```

pow
===

指数表达式

### 说明

<span class="type">number</span> <span class="methodname">pow</span> (
<span class="methodparam"><span class="type">number</span>
`$base`</span> , <span class="methodparam"><span
class="type">number</span> `$exp`</span> )

返回 `base` 的 `exp` 次方的幂。如果可能，本函数会返回 <span
class="type">integer</span>。

### 参数

`base`  
The base to use

`exp`  
指数

### 返回值

`base` 的 `exp` 次方的幂。 If both arguments are non-negative integers
and the result can be represented as an integer, the result will be
returned with <span class="type">integer</span> type, otherwise it will
be returned as a <span class="type">float</span>.

### 更新日志

| 版本  | 说明                                                                                                                                                                                    |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.2.0 | 如果不能计算幂，将发出一条警告，<span class="function">pow</span> 将返回 **`false`**。<span class="function">pow</span> 开始不产生任何的警告。                                          |
| 4.0.6 | 如果可能函数现在会返回 <span class="type">integer</span> 的结果，之前 总是返回 <span class="type">float</span>，For older versions, you may receive a bogus result for complex numbers. |

### 范例

**示例 \#1 <span class="function">pow</span> 的一些例子**

``` php
<?php

var_dump(pow(2, 8)); // int(256)
echo pow(-1, 20); // 1
echo pow(0, 0); // 1

echo pow(-1, 5.5); // PHP >4.0.6  NAN
echo pow(-1, 5.5); // PHP <=4.0.6 1.#IND
?>
```

### 注释

> **Note**:
>
> 本函数会转换所有输入为数字，即使是非标量值，会导致怪异的（*weird*）结果。

### 参见

-   <span class="function">exp</span>
-   <span class="function">sqrt</span>
-   <span class="function">bcpow</span>
-   <span class="function">gmp\_pow</span>

rad2deg
=======

将弧度数转换为相应的角度数

### 说明

<span class="type">float</span> <span class="methodname">rad2deg</span>
( <span class="methodparam"><span class="type">float</span>
`$number`</span> )

本函数将 `number` 从弧度转换为角度。

### 参数

`number`  
一个弧度值

### 返回值

`number` 相应的角度数

### 范例

**示例 \#1 <span class="function">rad2deg</span> 例子**

``` php
<?php

echo rad2deg(M_PI_4); // 45

?>
```

### 参见

-   <span class="function">deg2rad</span>

rand
====

产生一个随机整数

### 说明

<span class="type">int</span> <span class="methodname">rand</span> (
<span class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">rand</span> (
<span class="methodparam"><span class="type">int</span> `$min`</span> ,
<span class="methodparam"><span class="type">int</span> `$max`</span> )

如果没有提供可选参数 `min` 和 `max`，<span class="function">rand</span>
返回 0 到 <span class="function">getrandmax</span>
之间的伪随机整数。例如想要 5 到 15（包括 5 和 15）之间的随机数，用
*rand(5, 15)*。

> **Note**: <span class="simpara"> 在某些平台下（例如 Windows）<span
> class="function">getrandmax</span> 只有 32767。如果需要的范围大于
> 32767，那么指定 `min` 和 `max` 参数就可以生成更大的数了，或者考虑用
> <span class="function">mt\_rand</span> 来替代之。 </span>

### 参数

`min`  
返回的最低值（默认：0）

`max`  
返回的最高值（默认：<span class="function">getrandmax</span>）

### 返回值

A pseudo random value between `min` (or 0) and `max` (or <span
class="function">getrandmax</span>, inclusive).

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 4.2.0 | 随机数发生器自动进行播种。 |

### 范例

**示例 \#1 <span class="function">rand</span> 例子**

``` php
<?php
echo rand() . "\n";
echo rand() . "\n";

echo rand(5, 15);
?>
```

以上例程的输出类似于：

    7771
    22264
    11

### 参见

-   <span class="function">srand</span>
-   <span class="function">getrandmax</span>
-   <span class="function">mt\_rand</span>

round
=====

对浮点数进行四舍五入

### 说明

<span class="type">float</span> <span class="methodname">round</span> (
<span class="methodparam"><span class="type">float</span> `$val`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$precision`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = PHP\_ROUND\_HALF\_UP</span></span> \]\] )

返回将 `val` 根据指定精度
`precision`（十进制小数点后数字的数目）进行四舍五入的结果。`precision`
也可以是负数或零（默认值）。

> **Note**: <span class="simpara"> PHP 默认不能正确处理类似 *"12,300.2"*
> 的字符串。见<a href="/language/types/string.html#language.types.string.conversion" class="link">字符串转换为数值</a>。
> </span>

### 参数

`val`  
要处理的值

`precision`  
可选的十进制小数点后数字的数目。

`mode`  
以下之一： **`PHP_ROUND_HALF_UP`**、 **`PHP_ROUND_HALF_DOWN`**
**`PHP_ROUND_HALF_EVEN`** 或 **`PHP_ROUND_HALF_ODD`**

### 返回值

四舍五入后的值

### 范例

**示例 \#1 <span class="function">round</span> 例子**

``` php
<?php
echo round(3.4);         // 3
echo round(3.5);         // 4
echo round(3.6);         // 4
echo round(3.6, 0);      // 4
echo round(1.95583, 2);  // 1.96
echo round(1241757, -3); // 1242000
echo round(5.045, 2);    // 5.05
echo round(5.055, 2);    // 5.06
?>
```

**示例 \#2 `mode` 例子**

``` php
<?php
echo round(9.5, 0, PHP_ROUND_HALF_UP);   // 10
echo round(9.5, 0, PHP_ROUND_HALF_DOWN); // 9
echo round(9.5, 0, PHP_ROUND_HALF_EVEN); // 10
echo round(9.5, 0, PHP_ROUND_HALF_ODD);  // 9

echo round(8.5, 0, PHP_ROUND_HALF_UP);   // 9
echo round(8.5, 0, PHP_ROUND_HALF_DOWN); // 8
echo round(8.5, 0, PHP_ROUND_HALF_EVEN); // 8
echo round(8.5, 0, PHP_ROUND_HALF_ODD);  // 9
?>
```

### 更新日志

| 版本  | 说明                                                                |
|-------|---------------------------------------------------------------------|
| 5.3.0 | 引入了 `mode` 参数                                                  |
| 5.2.7 | <span class="function">round</span> 的内部运作修改符合 C99 的标准。 |

### 参见

-   <span class="function">ceil</span>
-   <span class="function">floor</span>
-   <span class="function">number\_format</span>

sin
===

正弦

### 说明

<span class="type">float</span> <span class="methodname">sin</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

<span class="function">sin</span> 返回参数 `arg` 的正弦值。参数 `arg`
的单位为弧度。

### 参数

`arg`  
单位是弧度的值。

### 返回值

`arg` 的正弦值

### 范例

**示例 \#1 <span class="function">sin</span> 例子**

``` php
<?php

// 返回值的精度由配置中的 precision 指示确定
echo sin(deg2rad(60));  //  0.866025403 ...
echo sin(60);           // -0.304810621 ...

?>
```

### 参见

-   <span class="function">asin</span>
-   <span class="function">sinh</span>
-   <span class="function">cos</span>
-   <span class="function">tan</span>
-   <span class="function">deg2rad</span>

sinh
====

双曲正弦

### 说明

<span class="type">float</span> <span class="methodname">sinh</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的双曲正弦值，定义为 *(exp(arg) - exp(-arg))/2*。

### 参数

`arg`  
要处理的参数

### 返回值

`arg` 的双曲正弦值

### 参见

-   <span class="function">sin</span>
-   <span class="function">asinh</span>
-   <span class="function">cosh</span>
-   <span class="function">tanh</span>

sqrt
====

平方根

### 说明

<span class="type">float</span> <span class="methodname">sqrt</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的平方根。

### 参数

`arg`  
要处理的参数

### 返回值

返回 `arg` 的平方根，负数时返回 *NAN*。

### 范例

**示例 \#1 <span class="function">sqrt</span> 例子**

``` php
<?php
// Precision depends on your precision directive
echo sqrt(9); // 3
echo sqrt(10); // 3.16227766 ...
?>
```

### 参见

-   <span class="function">pow</span>

srand
=====

播下随机数发生器种子

### 说明

<span class="type">void</span> <span class="methodname">srand</span> (\[
<span class="methodparam"><span class="type">int</span> `$seed`</span>
\] )

用 `seed` 播下随机数发生器种子。`seed` 参数没有给出时，会被设为随时数。

> **Note**: <span class="simpara">不再需要用 <span
> class="function">srand</span> 或 <span
> class="function">mt\_srand</span>
> 给随机数发生器播种，因为现在是由系统自动完成的。</span>

### 参数

`seed`  
可选的种子值

### 返回值

没有返回值。

### 更新日志

| 版本        | 说明                                      |
|-------------|-------------------------------------------|
| Since 4.2.0 | `seed` 成为可选，省略时会默认使用随机值。 |

### 范例

**示例 \#1 <span class="function">srand</span> 例子**

``` php
<?php
// seed with microseconds
function make_seed()
{
  list($usec, $sec) = explode(' ', microtime());
  return (float) $sec + ((float) $usec * 100000);
}
srand(make_seed());
$randval = rand();
?>
```

### 参见

-   <span class="function">rand</span>
-   <span class="function">getrandmax</span>
-   <span class="function">mt\_srand</span>

tan
===

正切

### 说明

<span class="type">float</span> <span class="methodname">tan</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

<span class="function">tan</span> 返回参数 `arg` 的正切值。参数 `arg`
的单位为弧度。

### 参数

`arg`  
要处理的以弧度为单位的参数

### 返回值

`arg` 的正切值

### 范例

**示例 \#1 <span class="function">tan</span> 例子**

``` php
<?php

echo tan(M_PI_4); // 1

?>
```

### 参见

-   <span class="function">atan</span>
-   <span class="function">atan2</span>
-   <span class="function">sin</span>
-   <span class="function">cos</span>
-   <span class="function">tanh</span>
-   <span class="function">deg2rad</span>

tanh
====

双曲正切

### 说明

<span class="type">float</span> <span class="methodname">tanh</span> (
<span class="methodparam"><span class="type">float</span> `$arg`</span>
)

返回 `arg` 的双曲正切值，定义为 *sinh(arg)/cosh(arg)*。

### 参数

`arg`  
要处理的参数

### 返回值

`arg` 的双曲正切值

### 参见

-   <span class="function">tan</span>
-   <span class="function">atanh</span>
-   <span class="function">sinh</span>
-   <span class="function">cosh</span>

**目录**

-   [abs](/ref/math.html#abs) — 绝对值
-   [acos](/ref/math.html#acos) — 反余弦
-   [acosh](/ref/math.html#acosh) — 反双曲余弦
-   [asin](/ref/math.html#asin) — 反正弦
-   [asinh](/ref/math.html#asinh) — 反双曲正弦
-   [atan2](/ref/math.html#atan2) — 两个参数的反正切
-   [atan](/ref/math.html#atan) — 反正切
-   [atanh](/ref/math.html#atanh) — 反双曲正切
-   [base\_convert](/ref/math.html#base_convert) —
    在任意进制之间转换数字
-   [bindec](/ref/math.html#bindec) — 二进制转换为十进制
-   [ceil](/ref/math.html#ceil) — 进一法取整
-   [cos](/ref/math.html#cos) — 余弦
-   [cosh](/ref/math.html#cosh) — 双曲余弦
-   [decbin](/ref/math.html#decbin) — 十进制转换为二进制
-   [dechex](/ref/math.html#dechex) — 十进制转换为十六进制
-   [decoct](/ref/math.html#decoct) — 十进制转换为八进制
-   [deg2rad](/ref/math.html#deg2rad) — 将角度转换为弧度
-   [exp](/ref/math.html#exp) — 计算 e 的指数
-   [expm1](/ref/math.html#expm1) — 返回 exp(number) - 1，甚至当 number
    的值接近零也能计算出准确结果
-   [floor](/ref/math.html#floor) — 舍去法取整
-   [fmod](/ref/math.html#fmod) — 返回除法的浮点数余数
-   [getrandmax](/ref/math.html#getrandmax) — 显示随机数最大的可能值
-   [hexdec](/ref/math.html#hexdec) — 十六进制转换为十进制
-   [hypot](/ref/math.html#hypot) — 计算一直角三角形的斜边长度
-   [intdiv](/ref/math.html#intdiv) — 对除法结果取整
-   [is\_finite](/ref/math.html#is_finite) — 判断是否为有限值
-   [is\_infinite](/ref/math.html#is_infinite) — 判断是否为无限值
-   [is\_nan](/ref/math.html#is_nan) — 判断是否为合法数值
-   [lcg\_value](/ref/math.html#lcg_value) — 组合线性同余发生器
-   [log10](/ref/math.html#log10) — 以 10 为底的对数
-   [log1p](/ref/math.html#log1p) — 返回 log(1 + number)，甚至当 number
    的值接近零也能计算出准确结果
-   [log](/ref/math.html#log) — 自然对数
-   [max](/ref/math.html#max) — 找出最大值
-   [min](/ref/math.html#min) — 找出最小值
-   [mt\_getrandmax](/ref/math.html#mt_getrandmax) —
    显示随机数的最大可能值
-   [mt\_rand](/ref/math.html#mt_rand) — 生成更好的随机数
-   [mt\_srand](/ref/math.html#mt_srand) —
    播下一个更好的随机数发生器种子
-   [octdec](/ref/math.html#octdec) — 八进制转换为十进制
-   [pi](/ref/math.html#pi) — 得到圆周率值
-   [pow](/ref/math.html#pow) — 指数表达式
-   [rad2deg](/ref/math.html#rad2deg) — 将弧度数转换为相应的角度数
-   [rand](/ref/math.html#rand) — 产生一个随机整数
-   [round](/ref/math.html#round) — 对浮点数进行四舍五入
-   [sin](/ref/math.html#sin) — 正弦
-   [sinh](/ref/math.html#sinh) — 双曲正弦
-   [sqrt](/ref/math.html#sqrt) — 平方根
-   [srand](/ref/math.html#srand) — 播下随机数发生器种子
-   [tan](/ref/math.html#tan) — 正切
-   [tanh](/ref/math.html#tanh) — 双曲正切
