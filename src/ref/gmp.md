参见
----

More mathematical functions can be found in the
<a href="/refs/math.html" class="xref">数学扩展</a> section

gmp\_abs
========

Absolute value

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_abs</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> )

Get the absolute value of a number.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns the absolute value of `a`, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_abs</span> example**

``` php
<?php
$abs1 = gmp_abs("274982683358");
$abs2 = gmp_abs("-274982683358");

echo gmp_strval($abs1) . "\n";
echo gmp_strval($abs2) . "\n";
?>
```

以上例程会输出：

    274982683358
    274982683358

gmp\_add
========

Add numbers

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_add</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Add two numbers.

### 参数

`a`  
The first summand (augent).

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
The second summand (addend).

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

A GMP number representing the sum of the arguments.

### 范例

**示例 \#1 <span class="function">gmp\_add</span> example**

``` php
<?php
$sum = gmp_add("123456789012345", "76543210987655");
echo gmp_strval($sum) . "\n";
?>
```

以上例程会输出：

    200000000000000

gmp\_and
========

Bitwise AND

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_and</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Calculates bitwise AND of two GMP numbers.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

A GMP number representing the bitwise *AND* comparison.

### 范例

**示例 \#1 <span class="function">gmp\_and</span> example**

``` php
<?php
$and1 = gmp_and("0xfffffffff4", "0x4");
$and2 = gmp_and("0xfffffffff4", "0x8");
echo gmp_strval($and1) . "\n";
echo gmp_strval($and2) . "\n";
?>
```

以上例程会输出：

    4
    0

gmp\_binomial
=============

Calculates binomial coefficient

### 说明

<span class="type"><span class="type">GMP</span><span
class="type">false</span></span> <span
class="methodname">gmp\_binomial</span> ( <span
class="methodparam"><span class="type">mixed</span> `$n`</span> , <span
class="methodparam"><span class="type">int</span> `$k`</span> )

Calculates the binomial coefficient C(n, k).

### 参数

`n`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`k`  

### 返回值

Returns the binomial coefficient C(n, k), 或者在失败时返回 **`FALSE`**.

### 错误／异常

Issues E\_WARNING if `k` is negative.

gmp\_clrbit
===========

Clear bit

### 说明

<span class="type">void</span> <span
class="methodname">gmp\_clrbit</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">int</span> `$index`</span> )

Clears (sets to 0) bit `index` in `a`. The index starts at 0.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`index`  
The index of the bit to clear. Index 0 represents the least significant
bit.

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_clrbit</span> example**

``` php
<?php
$a = gmp_init("0xff");
gmp_clrbit($a, 0); // index starts at 0, least significant bit
echo gmp_strval($a) . "\n";
?>
```

以上例程会输出：

    254

### 注释

> **Note**:
>
> Unlike most of the other GMP functions, <span
> class="function">gmp\_clrbit</span> must be called with a GMP resource
> that already exists (using <span class="function">gmp\_init</span> for
> example). One will not be automatically created.

### 参见

-   <span class="function">gmp\_setbit</span>
-   <span class="function">gmp\_testbit</span>

gmp\_cmp
========

Compare numbers

### 说明

<span class="type">int</span> <span class="methodname">gmp\_cmp</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Compares two numbers.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns a positive value if *a \> b*, zero if *a = b* and a negative
value if *a \< b*.

### 范例

**示例 \#1 <span class="function">gmp\_cmp</span> example**

``` php
<?php
$cmp1 = gmp_cmp("1234", "1000"); // greater than
$cmp2 = gmp_cmp("1000", "1234"); // less than
$cmp3 = gmp_cmp("1234", "1234"); // equal to

echo "$cmp1 $cmp2 $cmp3\n";
?>
```

以上例程会输出：

    1 -1 0

gmp\_com
========

Calculates one's complement

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_com</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> )

Returns the one's complement of `a`.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns the one's complement of `a`, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_com</span> example**

``` php
<?php
$com = gmp_com("1234");
echo gmp_strval($com) . "\n";
?>
```

以上例程会输出：

    -1235

gmp\_div\_q
===========

Divide numbers

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_div\_q</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">GMP</span> `$b`</span> \[, <span class="methodparam"><span
class="type">int</span> `$round`<span class="initializer"> =
GMP\_ROUND\_ZERO</span></span> \] )

Divides `a` by `b` and returns the integer result.

### 参数

`a`  
The number being divided.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
The number that `a` is being divided by.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`round`  
The result rounding is defined by the `round`, which can have the
following values:

-   <span class="simpara"> **`GMP_ROUND_ZERO`**: The result is truncated
    towards 0. </span>
-   <span class="simpara"> **`GMP_ROUND_PLUSINF`**: The result is
    rounded towards *+infinity*. </span>
-   <span class="simpara"> **`GMP_ROUND_MINUSINF`**: The result is
    rounded towards *-infinity*. </span>

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_div\_q</span> example**

``` php
<?php
$div1 = gmp_div_q("100", "5");
echo gmp_strval($div1) . "\n";

$div2 = gmp_div_q("1", "3");
echo gmp_strval($div2) . "\n";

$div3 = gmp_div_q("1", "3", GMP_ROUND_PLUSINF);
echo gmp_strval($div3) . "\n";

$div4 = gmp_div_q("-1", "4", GMP_ROUND_PLUSINF);
echo gmp_strval($div4) . "\n";

$div5 = gmp_div_q("-1", "4", GMP_ROUND_MINUSINF);
echo gmp_strval($div5) . "\n";
?>
```

以上例程会输出：

    20
    0
    1
    0
    -1

### 注释

> **Note**:
>
> This function can also be called as <span
> class="function">gmp\_div</span>.

### 参见

-   <span class="function">gmp\_div\_r</span>
-   <span class="function">gmp\_div\_qr</span>

gmp\_div\_qr
============

Divide numbers and get quotient and remainder

### 说明

<span class="type">array</span> <span
class="methodname">gmp\_div\_qr</span> ( <span class="methodparam"><span
class="type">GMP</span> `$n`</span> , <span class="methodparam"><span
class="type">GMP</span> `$d`</span> \[, <span class="methodparam"><span
class="type">int</span> `$round`<span class="initializer"> =
GMP\_ROUND\_ZERO</span></span> \] )

The function divides `n` by `d`.

### 参数

`n`  
The number being divided.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`d`  
The number that `n` is being divided by.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`round`  
See the <span class="function">gmp\_div\_q</span> function for
description of the `round` argument.

### 返回值

Returns an <span class="type">array</span>, with the first element being
*\[n/d\]* (the integer result of the division) and the second being *(n
- \[n/d\] \* d)* (the remainder of the division).

### 范例

**示例 \#1 Division of GMP numbers**

``` php
<?php
$a = gmp_init("0x41682179fbf5");
$res = gmp_div_qr($a, "0xDEFE75");
printf("Result is: q - %s, r - %s",
       gmp_strval($res[0]), gmp_strval($res[1]));
?>
```

### 参见

-   <span class="function">gmp\_div\_q</span>
-   <span class="function">gmp\_div\_r</span>

gmp\_div\_r
===========

Remainder of the division of numbers

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_div\_r</span> ( <span class="methodparam"><span
class="type">GMP</span> `$n`</span> , <span class="methodparam"><span
class="type">GMP</span> `$d`</span> \[, <span class="methodparam"><span
class="type">int</span> `$round`<span class="initializer"> =
GMP\_ROUND\_ZERO</span></span> \] )

Calculates remainder of the integer division of `n` by `d`. The
remainder has the sign of the `n` argument, if not zero.

### 参数

`n`  
The number being divided.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`d`  
The number that `n` is being divided by.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`round`  
See the <span class="function">gmp\_div\_q</span> function for
description of the `round` argument.

### 返回值

The remainder, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_div\_r</span> example**

``` php
<?php
$div = gmp_div_r("105", "20");
echo gmp_strval($div) . "\n";
?>
```

以上例程会输出：

    5

### 参见

-   <span class="function">gmp\_div\_q</span>
-   <span class="function">gmp\_div\_qr</span>

gmp\_div
========

别名 <span class="function">gmp\_div\_q</span>

### 说明

此函数是该函数的别名： <span class="function">gmp\_div\_q</span>.

gmp\_divexact
=============

Exact division of numbers

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_divexact</span> ( <span
class="methodparam"><span class="type">GMP</span> `$n`</span> , <span
class="methodparam"><span class="type">GMP</span> `$d`</span> )

Divides `n` by `d`, using fast "exact division" algorithm. This function
produces correct results only when it is known in advance that `d`
divides `n`.

### 参数

`n`  
The number being divided.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`d`  
The number that `a` is being divided by.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_divexact</span> example**

``` php
<?php
$div1 = gmp_divexact("10", "2");
echo gmp_strval($div1) . "\n";

$div2 = gmp_divexact("10", "3"); // bogus result
echo gmp_strval($div2) . "\n";
?>
```

以上例程会输出：

    5
    2863311534

gmp\_export
===========

Export to a binary string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">gmp\_export</span> ( <span class="methodparam"><span
class="type">GMP</span> `$gmpnumber`</span> \[, <span
class="methodparam"><span class="type">int</span> `$word_size`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = **`GMP_MSW_FIRST`** \|
**`GMP_NATIVE_ENDIAN`**</span></span> \]\] )

Export a GMP number to a binary string

### 参数

`gmpnumber`  
The GMP number being exported

`word_size`  
Default value is 1. The number of bytes in each chunk of binary data.
This is mainly used in conjunction with the options parameter.

`options`  
Default value is GMP\_MSW\_FIRST \| GMP\_NATIVE\_ENDIAN.

### 返回值

Returns a string 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">gmp\_export</span> example**

``` php
<?php
$number = gmp_init(16705);
echo gmp_export($number) . "\n";
?>
```

以上例程会输出：

    AA

### 参见

-   <span class="function">gmp\_import</span>

gmp\_fact
=========

Factorial

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_fact</span>
( <span class="methodparam"><span class="type">mixed</span> `$a`</span>
)

Calculates factorial (*a!*) of `a`.

### 参数

`a`  
The factorial number.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_fact</span> example**

``` php
<?php
$fact1 = gmp_fact(5); // 5 * 4 * 3 * 2 * 1
echo gmp_strval($fact1) . "\n";

$fact2 = gmp_fact(50); // 50 * 49 * 48, ... etc
echo gmp_strval($fact2) . "\n";
?>
```

以上例程会输出：

    120
    30414093201713378043612608166064768844377641568960512000000000000

gmp\_gcd
========

Calculate GCD

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_gcd</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Calculate greatest common divisor of `a` and `b`. The result is always
positive even if either of, or both, input operands are negative.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

A positive GMP number that divides into both `a` and `b`.

### 范例

**示例 \#1 <span class="function">gmp\_gcd</span> example**

``` php
<?php
$gcd = gmp_gcd("12", "21");
echo gmp_strval($gcd) . "\n";
?>
```

以上例程会输出：

    3

### 参见

-   <span class="function">gmp\_lcm</span>

gmp\_gcdext
===========

Calculate GCD and multipliers

### 说明

<span class="type">array</span> <span
class="methodname">gmp\_gcdext</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">GMP</span> `$b`</span> )

Calculates g, s, and t, such that *a\*s + b\*t = g = gcd(a,b)*, where
gcd is the greatest common divisor. Returns an array with respective
elements g, s and t.

This function can be used to solve linear Diophantine equations in two
variables. These are equations that allow only integer solutions and
have the form: *a\*x + b\*y = c*. For more information, go to the
<a href="http://mathworld.wolfram.com/DiophantineEquation.html" class="link external">» "Diophantine Equation" page at MathWorld</a>

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

An <span class="type">array</span> of GMP numbers.

### 范例

**示例 \#1 Solving a linear Diophantine equation**

``` php
<?php
// Solve the equation a*s + b*t = g
// where a = 12, b = 21, g = gcd(12, 21) = 3
$a = gmp_init(12);
$b = gmp_init(21);
$g = gmp_gcd($a, $b);
$r = gmp_gcdext($a, $b);

$check_gcd = (gmp_strval($g) == gmp_strval($r['g']));
$eq_res = gmp_add(gmp_mul($a, $r['s']), gmp_mul($b, $r['t']));
$check_res = (gmp_strval($g) == gmp_strval($eq_res));

if ($check_gcd && $check_res) {
    $fmt = "Solution: %d*%d + %d*%d = %d\n";
    printf($fmt, gmp_strval($a), gmp_strval($r['s']), gmp_strval($b),
    gmp_strval($r['t']), gmp_strval($r['g']));
} else {
    echo "Error while solving the equation\n";
}

// output: Solution: 12*2 + 21*-1 = 3
?>
```

gmp\_hamdist
============

Hamming distance

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_hamdist</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">GMP</span> `$b`</span> )

Returns the hamming distance between `a` and `b`. Both operands should
be non-negative.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

It should be positive.

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

It should be positive.

### 返回值

The hamming distance between `a` and `b`, as an <span
class="type">int</span>.

### 范例

**示例 \#1 <span class="function">gmp\_hamdist</span> example**

``` php
<?php
$ham1 = gmp_init("1001010011", 2);
$ham2 = gmp_init("1011111100", 2);
echo gmp_hamdist($ham1, $ham2) . "\n";

/* hamdist is equivalent to: */
echo gmp_popcount(gmp_xor($ham1, $ham2)) . "\n";
?>
```

以上例程会输出：

    6
    6

### 参见

-   <span class="function">gmp\_popcount</span>
-   <span class="function">gmp\_xor</span>

gmp\_import
===========

Import from a binary string

### 说明

<span class="type"><span class="type">GMP</span><span
class="type">false</span></span> <span
class="methodname">gmp\_import</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$word_size`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = **`GMP_MSW_FIRST`** \|
**`GMP_NATIVE_ENDIAN`**</span></span> \]\] )

Import a GMP number from a binary string

### 参数

`data`  
The binary string being imported

`word_size`  
Default value is 1. The number of bytes in each chunk of binary data.
This is mainly used in conjunction with the options parameter.

`options`  
Default value is GMP\_MSW\_FIRST \| GMP\_NATIVE\_ENDIAN.

### 返回值

Returns a GMP number 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">gmp\_import</span> example**

``` php
<?php
$number = gmp_import("\0");
echo gmp_strval($number) . "\n";

$number = gmp_import("\0\1\2");
echo gmp_strval($number) . "\n";
?>
```

以上例程会输出：

    0
    258

### 参见

-   <span class="function">gmp\_export</span>

gmp\_init
=========

Create GMP number

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_init</span>
( <span class="methodparam"><span class="type">mixed</span>
`$number`</span> \[, <span class="methodparam"><span
class="type">int</span> `$base`<span class="initializer"> =
0</span></span> \] )

Creates a GMP number from an integer or string.

### 参数

`number`  
An integer or a string. The string representation can be decimal,
hexadecimal or octal.

`base`  
The base.

The base may vary from 2 to 36. If base is 0 (default value), the actual
base is determined from the leading characters: if the first two
characters are *0x* or *0X*, hexadecimal is assumed, otherwise if the
first character is "0", octal is assumed, otherwise decimal is assumed.

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 注释

> **Note**:
>
> To use the extended base introduced in PHP 5.3.2, then PHP must be
> compiled against GMP 4.2.0 or greater.

### 范例

**示例 \#1 Creating GMP number**

``` php
<?php
$a = gmp_init(123456);
$b = gmp_init("0xFFFFDEBACDFEDF7200");
?>
```

### 注释

> **Note**:
>
> It is not necessary to call this function in order to use integers or
> strings in place of GMP numbers in GMP functions (such as with <span
> class="function">gmp\_add</span>). Function arguments are
> automatically converted to GMP numbers, if such conversion is possible
> and needed, using the same rules as <span
> class="function">gmp\_init</span>.

gmp\_intval
===========

Convert GMP number to integer

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_intval</span> ( <span class="methodparam"><span
class="type">GMP</span> `$gmpnumber`</span> )

This function converts GMP number into native PHP <span
class="type">int</span>s.

### 参数

`gmpnumber`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

The <span class="type">int</span> value of `gmpnumber`.

### 范例

**示例 \#1 <span class="function">gmp\_intval</span> example**

``` php
<?php
// displays correct result
echo gmp_intval("2147483647") . "\n";

// displays wrong result, above PHP integer limit
echo gmp_intval("2147483648") . "\n";

// displays correct result
echo gmp_strval("2147483648") . "\n";
?>
```

以上例程会输出：

    2147483647
    2147483647
    2147483648

### 注释

**Warning**

This function returns a useful result only if the number actually fits
the PHP integer (i.e., signed long type). To simply print the GMP
number, use <span class="function">gmp\_strval</span>.

gmp\_invert
===========

Inverse by modulo

### 说明

<span class="type"><span class="type">GMP</span><span
class="type">false</span></span> <span
class="methodname">gmp\_invert</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">GMP</span> `$b`</span> )

Computes the inverse of `a` modulo `b`.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

A GMP number on success or **`FALSE`** if an inverse does not exist.

### 范例

**示例 \#1 <span class="function">gmp\_invert</span> example**

``` php
<?php
echo gmp_invert("5", "10"); // no inverse, outputs nothing, result is FALSE
$invert = gmp_invert("5", "11");
echo gmp_strval($invert) . "\n";
?>
```

以上例程会输出：

    9

gmp\_jacobi
===========

Jacobi symbol

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_jacobi</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">GMP</span> `$p`</span> )

Computes
<a href="http://primes.utm.edu/glossary/page.php?sort=JacobiSymbol" class="link external">» Jacobi symbol</a>
of `a` and `p`. `p` should be odd and must be positive.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`p`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

Should be odd and must be positive.

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_jacobi</span> example**

``` php
<?php
echo gmp_jacobi("1", "3") . "\n";
echo gmp_jacobi("2", "3") . "\n";
?>
```

以上例程会输出：

    1
    0

### 参见

-   <span class="function">gmp\_kronecker</span>
-   <span class="function">gmp\_legendre</span>

gmp\_kronecker
==============

Kronecker symbol

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_kronecker</span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span> , <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

This function computes the Kronecker symbol of `a` and `b`.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns the Kronecker symbol of `a` and `b`

### 参见

-   <span class="function">gmp\_jacobi</span>
-   <span class="function">gmp\_legendre</span>

gmp\_lcm
========

Calculate LCM

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_lcm</span> (
<span class="methodparam"><span class="type">mixed</span> `$a`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$b`</span> )

This function computes the least common multiple (lcm) of `a` and `b`.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 参见

-   <span class="function">gmp\_gcd</span>

gmp\_legendre
=============

Legendre symbol

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_legendre</span> ( <span
class="methodparam"><span class="type">GMP</span> `$a`</span> , <span
class="methodparam"><span class="type">GMP</span> `$p`</span> )

Compute the
<a href="http://primes.utm.edu/glossary/page.php?sort=LegendreSymbol" class="link external">»  Legendre symbol</a>
of `a` and `p`. `p` should be odd and must be positive.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`p`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

Should be odd and must be positive.

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_legendre</span> example**

``` php
<?php
echo gmp_legendre("1", "3") . "\n";
echo gmp_legendre("2", "3") . "\n";
?>
```

以上例程会输出：

    1
    0

### 参见

-   <span class="function">gmp\_jacobi</span>
-   <span class="function">gmp\_kronecker</span>

gmp\_mod
========

Modulo operation

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_mod</span> (
<span class="methodparam"><span class="type">GMP</span> `$n`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$d`</span> )

Calculates `n` modulo `d`. The result is always non-negative, the sign
of `d` is ignored.

### 参数

`n`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`d`  
The modulo that is being evaluated.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_mod</span> example**

``` php
<?php
$mod = gmp_mod("8", "3");
echo gmp_strval($mod) . "\n";
?>
```

以上例程会输出：

    2

gmp\_mul
========

Multiply numbers

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_mul</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Multiplies `a` by `b` and returns the result.

### 参数

`a`  
A number that will be multiplied by `b`.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
A number that will be multiplied by `a`.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_mul</span> example**

``` php
<?php
$mul = gmp_mul("12345678", "2000");
echo gmp_strval($mul) . "\n";
?>
```

以上例程会输出：

    24691356000

gmp\_neg
========

Negate number

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_neg</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> )

Returns the negative value of a number.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns -`a`, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_neg</span> example**

``` php
<?php
$neg1 = gmp_neg("1");
echo gmp_strval($neg1) . "\n";
$neg2 = gmp_neg("-1");
echo gmp_strval($neg2) . "\n";
?>
```

以上例程会输出：

    -1
    1

gmp\_nextprime
==============

Find next prime number

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_nextprime</span> ( <span
class="methodparam"><span class="type">int</span> `$a`</span> )

Find next prime number

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Return the next prime number greater than `a`, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_nextprime</span> example**

``` php
<?php
$prime1 = gmp_nextprime(10); // next prime number greater than 10
$prime2 = gmp_nextprime(-1000); // next prime number greater than -1000

echo gmp_strval($prime1) . "\n";
echo gmp_strval($prime2) . "\n";
?>
```

以上例程会输出：

    11
    2

### 注释

> **Note**:
>
> This function uses a probabilistic algorithm to identify primes and
> chances to get a composite number are extremely small.

gmp\_or
=======

Bitwise OR

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_or</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Calculates bitwise inclusive OR of two GMP numbers.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_or</span> example**

``` php
<?php
$or1 = gmp_or("0xfffffff2", "4");
echo gmp_strval($or1, 16) . "\n";
$or2 = gmp_or("0xfffffff2", "2");
echo gmp_strval($or2, 16) . "\n";
?>
```

以上例程会输出：

    fffffff6
    fffffff2

gmp\_perfect\_power
===================

Perfect power check

### 说明

<span class="type">bool</span> <span
class="methodname">gmp\_perfect\_power</span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span> )

Checks whether `a` is a perfect power.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns **`TRUE`** if `a` is a perfect power, **`FALSE`** otherwise.

### 参见

-   <span class="function">gmp\_perfect\_square</span>

gmp\_perfect\_square
====================

Perfect square check

### 说明

<span class="type">bool</span> <span
class="methodname">gmp\_perfect\_square</span> ( <span
class="methodparam"><span class="type">GMP</span> `$a`</span> )

Check if a number is a perfect square.

### 参数

`a`  
The number being checked as a perfect square.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns **`TRUE`** if `a` is a perfect square, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">gmp\_perfect\_square</span> example**

``` php
<?php
// 3 * 3, perfect square
var_dump(gmp_perfect_square("9"));

// not a perfect square
var_dump(gmp_perfect_square("7"));

// 1234567890 * 1234567890, perfect square
var_dump(gmp_perfect_square("1524157875019052100"));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(true)

### 参见

-   <span class="function">gmp\_perfect\_power</span>
-   <span class="function">gmp\_sqrt</span>
-   <span class="function">gmp\_sqrtrem</span>

gmp\_popcount
=============

Population count

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_popcount</span> ( <span
class="methodparam"><span class="type">GMP</span> `$a`</span> )

Get the population count.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

The population count of `a`, as an <span class="type">int</span>.

### 范例

**示例 \#1 <span class="function">gmp\_popcount</span> example**

``` php
<?php
$pop1 = gmp_init("10000101", 2); // 3 1's
echo gmp_popcount($pop1) . "\n";
$pop2 = gmp_init("11111110", 2); // 7 1's
echo gmp_popcount($pop2) . "\n";
?>
```

以上例程会输出：

    3
    7

gmp\_pow
========

Raise number into power

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_pow</span> (
<span class="methodparam"><span class="type">GMP</span> `$base`</span> ,
<span class="methodparam"><span class="type">int</span> `$exp`</span> )

Raise `base` into power `exp`.

### 参数

`base`  
The base number.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`exp`  
The positive power to raise the `base`.

### 返回值

The new (raised) number, as a GMP number. The case of *0^0* yields 1.

### 范例

**示例 \#1 <span class="function">gmp\_pow</span> example**

``` php
<?php
$pow1 = gmp_pow("2", 31);
echo gmp_strval($pow1) . "\n";
$pow2 = gmp_pow("0", 0);
echo gmp_strval($pow2) . "\n";
$pow3 = gmp_pow("2", -1); // Negative exp, generates warning
echo gmp_strval($pow3) . "\n";
?>
```

以上例程会输出：

    2147483648
    1

gmp\_powm
=========

Raise number into power with modulo

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_powm</span>
( <span class="methodparam"><span class="type">GMP</span> `$base`</span>
, <span class="methodparam"><span class="type">GMP</span> `$exp`</span>
, <span class="methodparam"><span class="type">GMP</span> `$mod`</span>
)

Calculate (`base` raised into power `exp`) modulo `mod`. If `exp` is
negative, result is undefined.

### 参数

`base`  
The base number.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`exp`  
The positive power to raise the `base`.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`mod`  
The modulo.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

The new (raised) number, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_powm</span> example**

``` php
<?php
$pow1 = gmp_powm("2", "31", "2147483649");
echo gmp_strval($pow1) . "\n";
?>
```

以上例程会输出：

    2147483648

gmp\_prob\_prime
================

Check if number is "probably prime"

### 说明

<span class="type">int</span> <span
class="methodname">gmp\_prob\_prime</span> ( <span
class="methodparam"><span class="type">GMP</span> `$a`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reps`<span
class="initializer"> = 10</span></span> \] )

The function uses Miller-Rabin's probabilistic test to check if a number
is a prime.

### 参数

`a`  
The number being checked as a prime.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`reps`  
Reasonable values of `reps` vary from 5 to 10 (default being 10); a
higher value lowers the probability for a non-prime to pass as a
"probable" prime.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

If this function returns 0, `a` is definitely not prime. If it returns
1, then `a` is "probably" prime. If it returns 2, then `a` is surely
prime.

### 范例

**示例 \#1 <span class="function">gmp\_prob\_prime</span> example**

``` php
<?php
// definitely not a prime
echo gmp_prob_prime("6") . "\n";

// probably a prime
echo gmp_prob_prime("1111111111111111111") . "\n";

// definitely a prime
echo gmp_prob_prime("11") . "\n";
?>
```

以上例程会输出：

    0
    1
    2

gmp\_random\_bits
=================

Random number

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_random\_bits</span> ( <span
class="methodparam"><span class="type">int</span> `$bits`</span> )

Generate a random number. The number will be between 0 and (2 \*\*
`bits`) - 1.

`bits` must greater than 0, and the maximum value is restricted by
available memory.

### 参数

`bits`  
The number of bits.

### 返回值

A random GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_random\_bits</span> example**

``` php
<?php
$rand1 = gmp_random_bits(3); // random number from 0 to 7
$rand2 = gmp_random_bits(5); // random number from 0 to 31

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

以上例程会输出：

    3
    15

gmp\_random\_range
==================

Random number

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_random\_range</span> ( <span
class="methodparam"><span class="type">GMP</span> `$min`</span> , <span
class="methodparam"><span class="type">GMP</span> `$max`</span> )

Generate a random number. The number will be between `min` and `max`.

`min` and `max` can both be negative but `min` must always be less than
`max`.

### 参数

`min`  
A GMP number representing the lower bound for the random number

`max`  
A GMP number representing the upper bound for the random number

### 返回值

A random GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_random\_range</span> example**

``` php
<?php
$rand1 = gmp_random_range(0, 100);    // random number between 0 and 100
$rand2 = gmp_random_range(-100, -10); // random number between -100 and -10

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

以上例程会输出：

    42
    -67

gmp\_random\_seed
=================

Sets the RNG seed

### 说明

<span class="type"><span class="type">null</span><span
class="type">false</span></span> <span
class="methodname">gmp\_random\_seed</span> ( <span
class="methodparam"><span class="type">mixed</span> `$seed`</span> )

### 参数

`seed`  
The seed to be set for the <span class="function">gmp\_random</span>,
<span class="function">gmp\_random\_bits</span>, and <span
class="function">gmp\_random\_range</span> functions.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

成功时返回 **`NULL`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Issues an **`E_WARNING`** and returns **`FALSE`** if `seed` is not
valid.

### 范例

**示例 \#1 <span class="function">gmp\_random\_seed</span> example**

``` php
<?php
// set the seed
gmp_random_seed(100);

var_dump(gmp_strval(gmp_random(1)));

// set the seed to something else
gmp_random_seed(gmp_init(-100));

var_dump(gmp_strval(gmp_random_bits(10)));

// set the seed to something invalid
var_dump(gmp_random_seed('not a number'));
```

以上例程会输出：

    string(20) "15370156633245019617"
    string(3) "683"

    Warning: gmp_random_seed(): Unable to convert variable to GMP - string is not an integer in %s on line %d
    bool(false)

### 参见

-   <span class="function">gmp\_init</span>
-   <span class="function">gmp\_random</span>
-   <span class="function">gmp\_random\_bits</span>
-   <span class="function">gmp\_random\_range</span>

gmp\_random
===========

Random number

**Warning**

本函数已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本函数。

### 说明

<span class="type">GMP</span> <span
class="methodname">gmp\_random</span> (\[ <span
class="methodparam"><span class="type">int</span> `$limiter`<span
class="initializer"> = 20</span></span> \] )

Generate a random number. The number will be between 0 and (2 \*\* n) -
1, where n is the number of bits per limb multiplied by `limiter`. If
`limiter` is negative, negative numbers are generated.

A limb is an internal GMP mechanism. The number of bits in a limb is not
static, and can vary from system to system. Generally, the number of
bits in a limb is either 32 or 64, but this is not guaranteed.

### 参数

`limiter`  
The limiter.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

A random GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_random</span> example**

``` php
<?php
$rand1 = gmp_random(1); // random number from 0 to 1 * bits per limb
$rand2 = gmp_random(2); // random number from 0 to 2 * bits per limb

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

以上例程会输出：

    1915834968
    8642564075890328087

gmp\_root
=========

Take the integer part of nth root

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_root</span>
( <span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">int</span> `$nth`</span> )

Takes the `nth` root of `a` and returns the integer component of the
result.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`nth`  
The positive root to take of `a`.

### 返回值

The integer component of the resultant root, as a GMP number.

gmp\_rootrem
============

Take the integer part and remainder of nth root

### 说明

<span class="type">array</span> <span
class="methodname">gmp\_rootrem</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">int</span> `$nth`</span> )

Takes the `nth` root of `a` and returns the integer component and
remainder of the result.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`nth`  
The positive root to take of `a`.

### 返回值

A two element array, where the first element is the integer component of
the root, and the second element is the remainder, both represented as
GMP numbers.

gmp\_scan0
==========

Scan for 0

### 说明

<span class="type">int</span> <span class="methodname">gmp\_scan0</span>
( <span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">int</span> `$start`</span>
)

Scans `a`, starting with bit `start`, towards more significant bits,
until the first clear bit is found.

### 参数

`a`  
The number to scan.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`start`  
The starting bit.

### 返回值

Returns the index of the found bit, as an <span class="type">int</span>.
The index starts from 0.

### 范例

**示例 \#1 <span class="function">gmp\_scan0</span> example**

``` php
<?php
// "0" bit is found at position 3. index starts at 0
$s1 = gmp_init("10111", 2);
echo gmp_scan0($s1, 0) . "\n";

// "0" bit is found at position 7. index starts at 5
$s2 = gmp_init("101110000", 2);
echo gmp_scan0($s2, 5) . "\n";
?>
```

以上例程会输出：

    3
    7

gmp\_scan1
==========

Scan for 1

### 说明

<span class="type">int</span> <span class="methodname">gmp\_scan1</span>
( <span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">int</span> `$start`</span>
)

Scans `a`, starting with bit `start`, towards more significant bits,
until the first set bit is found.

### 参数

`a`  
The number to scan.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`start`  
The starting bit.

### 返回值

Returns the index of the found bit, as an <span class="type">int</span>.
If no set bit is found, -1 is returned.

### 范例

**示例 \#1 <span class="function">gmp\_scan1</span> example**

``` php
<?php
// "1" bit is found at position 3. index starts at 0
$s1 = gmp_init("01000", 2);
echo gmp_scan1($s1, 0) . "\n";

// "1" bit is found at position 9. index starts at 5
$s2 = gmp_init("01000001111", 2);
echo gmp_scan1($s2, 5) . "\n";
?>
```

以上例程会输出：

    3
    9

gmp\_setbit
===========

Set bit

### 说明

<span class="type">void</span> <span
class="methodname">gmp\_setbit</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$bit_on`<span
class="initializer"> = **`TRUE`**</span></span> \] )

Sets bit `index` in `a`.

### 参数

`a`  
The value to modify.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`index`  
The index of the bit to set. Index 0 represents the least significant
bit.

`bit_on`  
True to set the bit (set it to 1/on); false to clear the bit (set it to
0/off).

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_setbit</span> example - 0 index**

``` php
<?php
$a = gmp_init("2"); //
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 0); // 0b10 now becomes 0b11
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

以上例程会输出：

    2 -> 0b10
    3 -> 0b11

**示例 \#2 <span class="function">gmp\_setbit</span> example - 1 index**

``` php
<?php
$a = gmp_init("0xfd");
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 1); // index starts at 0
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

以上例程会输出：

    253 -> 0b11111101
    255 -> 0b11111111

**示例 \#3 <span class="function">gmp\_setbit</span> example - clearing
a bit**

``` php
<?php
$a = gmp_init("0xff");
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 0, false); // clear bit at index 0
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

以上例程会输出：

    255 -> 0b11111111
    254 -> 0b11111110

### 注释

> **Note**:
>
> Unlike most of the other GMP functions, <span
> class="function">gmp\_setbit</span> must be called with a GMP resource
> that already exists (using <span class="function">gmp\_init</span> for
> example). One will not be automatically created.

### 参见

-   <span class="function">gmp\_clrbit</span>
-   <span class="function">gmp\_testbit</span>

gmp\_sign
=========

Sign of number

### 说明

<span class="type">int</span> <span class="methodname">gmp\_sign</span>
( <span class="methodparam"><span class="type">GMP</span> `$a`</span> )

Checks the sign of a number.

### 参数

`a`  
Either a GMP number <span class="type">resource</span> in PHP 5.5 and
earlier, a <span class="classname">GMP</span> object in PHP 5.6 and
later, or a numeric string provided that it is possible to convert the
latter to an <span class="type">int</span>.

### 返回值

Returns 1 if `a` is positive, -1 if `a` is negative, and 0 if `a` is
zero.

### 范例

**示例 \#1 <span class="function">gmp\_sign</span> example**

``` php
<?php
// positive
echo gmp_sign("500") . "\n";

// negative
echo gmp_sign("-500") . "\n";

// zero
echo gmp_sign("0") . "\n";
?>
```

以上例程会输出：

    1
    -1
    0

### 参见

-   <span class="function">gmp\_abs</span>
-   <span class="function">abs</span>

gmp\_sqrt
=========

Calculate square root

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_sqrt</span>
( <span class="methodparam"><span class="type">GMP</span> `$a`</span> )

Calculates square root of `a`.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

The integer portion of the square root, as a GMP number.

### 范例

**示例 \#1 <span class="function">gmp\_sqrt</span> example**

``` php
<?php
$sqrt1 = gmp_sqrt("9");
$sqrt2 = gmp_sqrt("7");
$sqrt3 = gmp_sqrt("1524157875019052100");

echo gmp_strval($sqrt1) . "\n";
echo gmp_strval($sqrt2) . "\n";
echo gmp_strval($sqrt3) . "\n";
?>
```

以上例程会输出：

    3
    2
    1234567890

gmp\_sqrtrem
============

Square root with remainder

### 说明

<span class="type">array</span> <span
class="methodname">gmp\_sqrtrem</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> )

Calculate the square root of a number, with remainder.

### 参数

`a`  
The number being square rooted.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

Returns array where first element is the integer square root of `a` and
the second is the remainder (i.e., the difference between `a` and the
first element squared).

### 范例

**示例 \#1 <span class="function">gmp\_sqrtrem</span> example**

``` php
<?php
list($sqrt1, $sqrt1rem) = gmp_sqrtrem("9");
list($sqrt2, $sqrt2rem) = gmp_sqrtrem("7");
list($sqrt3, $sqrt3rem) = gmp_sqrtrem("1048576");

echo gmp_strval($sqrt1) . ", " . gmp_strval($sqrt1rem) . "\n";
echo gmp_strval($sqrt2) . ", " . gmp_strval($sqrt2rem) . "\n";
echo gmp_strval($sqrt3) . ", " . gmp_strval($sqrt3rem) . "\n";
?>
```

以上例程会输出：

    3, 0
    2, 3
    1024, 0

gmp\_strval
===========

Convert GMP number to string

### 说明

<span class="type">string</span> <span
class="methodname">gmp\_strval</span> ( <span class="methodparam"><span
class="type">GMP</span> `$gmpnumber`</span> \[, <span
class="methodparam"><span class="type">int</span> `$base`<span
class="initializer"> = 10</span></span> \] )

Convert GMP number to string representation in base `base`. The default
base is 10.

### 参数

`gmpnumber`  
The GMP number that will be converted to a string.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`base`  
The base of the returned number. The default base is 10. Allowed values
for the base are from 2 to 62 and -2 to -36.

### 返回值

The number, as a <span class="type">string</span>.

### 注释

> **Note**:
>
> To use the extended base introduced in PHP 5.3.2, then PHP must be
> compiled against GMP 4.2.0 or greater.

### 范例

**示例 \#1 Converting a GMP number to a string**

``` php
<?php
$a = gmp_init("0x41682179fbf5");
printf("Decimal: %s, 36-based: %s", gmp_strval($a), gmp_strval($a,36));
?>
```

gmp\_sub
========

Subtract numbers

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_sub</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Subtracts `b` from `a` and returns the result.

### 参数

`a`  
The number being subtracted from.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
The number subtracted from `a`.

PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_sub</span> example**

``` php
<?php
$sub = gmp_sub("281474976710656", "4294967296"); // 2^48 - 2^32
echo gmp_strval($sub) . "\n";
?>
```

以上例程会输出：

    281470681743360

gmp\_testbit
============

Tests if a bit is set

### 说明

<span class="type">bool</span> <span
class="methodname">gmp\_testbit</span> ( <span class="methodparam"><span
class="type">GMP</span> `$a`</span> , <span class="methodparam"><span
class="type">int</span> `$index`</span> )

Tests if the specified bit is set.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`index`  
The bit to test

### 返回值

Returns **`TRUE`** if the bit is set in resource `$a`, otherwise
**`FALSE`**.

### 错误／异常

An **`E_WARNING`** level error is issued when `index` is less than zero,
and **`FALSE`** is returned.

### 范例

**示例 \#1 <span class="function">gmp\_testbit</span> example**

``` php
<?php
$n = gmp_init("1000000");
var_dump(gmp_testbit($n, 1));
gmp_setbit($n, 1);
var_dump(gmp_testbit($n, 1));
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="function">gmp\_setbit</span>
-   <span class="function">gmp\_clrbit</span>

gmp\_xor
========

Bitwise XOR

### 说明

<span class="type">GMP</span> <span class="methodname">gmp\_xor</span> (
<span class="methodparam"><span class="type">GMP</span> `$a`</span> ,
<span class="methodparam"><span class="type">GMP</span> `$b`</span> )

Calculates bitwise exclusive OR (XOR) of two GMP numbers.

### 参数

`a`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

`b`  
PHP 5.5 之前为 GMP 数值<span class="type">资源</span>，PHP 5.6 之后为
<span class="classname">GMP</span> 对象或数字，或可以转为数字的字符串。

### 返回值

PHP 5.5 之前，返回 GMP 数值<span class="type">资源</span>，PHP 5.6
之后，返回 <span class="classname">GMP</span> 对象。

### 范例

**示例 \#1 <span class="function">gmp\_xor</span> example**

``` php
<?php
$xor1 = gmp_init("1101101110011101", 2);
$xor2 = gmp_init("0110011001011001", 2);

$xor3 = gmp_xor($xor1, $xor2);

echo gmp_strval($xor3, 2) . "\n";
?>
```

以上例程会输出：

    1011110111000100

**目录**

-   [gmp\_abs](/ref/gmp.html#gmp_abs) — Absolute value
-   [gmp\_add](/ref/gmp.html#gmp_add) — Add numbers
-   [gmp\_and](/ref/gmp.html#gmp_and) — Bitwise AND
-   [gmp\_binomial](/ref/gmp.html#gmp_binomial) — Calculates binomial
    coefficient
-   [gmp\_clrbit](/ref/gmp.html#gmp_clrbit) — Clear bit
-   [gmp\_cmp](/ref/gmp.html#gmp_cmp) — Compare numbers
-   [gmp\_com](/ref/gmp.html#gmp_com) — Calculates one's complement
-   [gmp\_div\_q](/ref/gmp.html#gmp_div_q) — Divide numbers
-   [gmp\_div\_qr](/ref/gmp.html#gmp_div_qr) — Divide numbers and get
    quotient and remainder
-   [gmp\_div\_r](/ref/gmp.html#gmp_div_r) — Remainder of the division
    of numbers
-   [gmp\_div](/ref/gmp.html#gmp_div) — 别名 gmp\_div\_q
-   [gmp\_divexact](/ref/gmp.html#gmp_divexact) — Exact division of
    numbers
-   [gmp\_export](/ref/gmp.html#gmp_export) — Export to a binary string
-   [gmp\_fact](/ref/gmp.html#gmp_fact) — Factorial
-   [gmp\_gcd](/ref/gmp.html#gmp_gcd) — Calculate GCD
-   [gmp\_gcdext](/ref/gmp.html#gmp_gcdext) — Calculate GCD and
    multipliers
-   [gmp\_hamdist](/ref/gmp.html#gmp_hamdist) — Hamming distance
-   [gmp\_import](/ref/gmp.html#gmp_import) — Import from a binary
    string
-   [gmp\_init](/ref/gmp.html#gmp_init) — Create GMP number
-   [gmp\_intval](/ref/gmp.html#gmp_intval) — Convert GMP number to
    integer
-   [gmp\_invert](/ref/gmp.html#gmp_invert) — Inverse by modulo
-   [gmp\_jacobi](/ref/gmp.html#gmp_jacobi) — Jacobi symbol
-   [gmp\_kronecker](/ref/gmp.html#gmp_kronecker) — Kronecker symbol
-   [gmp\_lcm](/ref/gmp.html#gmp_lcm) — Calculate LCM
-   [gmp\_legendre](/ref/gmp.html#gmp_legendre) — Legendre symbol
-   [gmp\_mod](/ref/gmp.html#gmp_mod) — Modulo operation
-   [gmp\_mul](/ref/gmp.html#gmp_mul) — Multiply numbers
-   [gmp\_neg](/ref/gmp.html#gmp_neg) — Negate number
-   [gmp\_nextprime](/ref/gmp.html#gmp_nextprime) — Find next prime
    number
-   [gmp\_or](/ref/gmp.html#gmp_or) — Bitwise OR
-   [gmp\_perfect\_power](/ref/gmp.html#gmp_perfect_power) — Perfect
    power check
-   [gmp\_perfect\_square](/ref/gmp.html#gmp_perfect_square) — Perfect
    square check
-   [gmp\_popcount](/ref/gmp.html#gmp_popcount) — Population count
-   [gmp\_pow](/ref/gmp.html#gmp_pow) — Raise number into power
-   [gmp\_powm](/ref/gmp.html#gmp_powm) — Raise number into power with
    modulo
-   [gmp\_prob\_prime](/ref/gmp.html#gmp_prob_prime) — Check if number
    is "probably prime"
-   [gmp\_random\_bits](/ref/gmp.html#gmp_random_bits) — Random number
-   [gmp\_random\_range](/ref/gmp.html#gmp_random_range) — Random number
-   [gmp\_random\_seed](/ref/gmp.html#gmp_random_seed) — Sets the RNG
    seed
-   [gmp\_random](/ref/gmp.html#gmp_random) — Random number
-   [gmp\_root](/ref/gmp.html#gmp_root) — Take the integer part of nth
    root
-   [gmp\_rootrem](/ref/gmp.html#gmp_rootrem) — Take the integer part
    and remainder of nth root
-   [gmp\_scan0](/ref/gmp.html#gmp_scan0) — Scan for 0
-   [gmp\_scan1](/ref/gmp.html#gmp_scan1) — Scan for 1
-   [gmp\_setbit](/ref/gmp.html#gmp_setbit) — Set bit
-   [gmp\_sign](/ref/gmp.html#gmp_sign) — Sign of number
-   [gmp\_sqrt](/ref/gmp.html#gmp_sqrt) — Calculate square root
-   [gmp\_sqrtrem](/ref/gmp.html#gmp_sqrtrem) — Square root with
    remainder
-   [gmp\_strval](/ref/gmp.html#gmp_strval) — Convert GMP number to
    string
-   [gmp\_sub](/ref/gmp.html#gmp_sub) — Subtract numbers
-   [gmp\_testbit](/ref/gmp.html#gmp_testbit) — Tests if a bit is set
-   [gmp\_xor](/ref/gmp.html#gmp_xor) — Bitwise XOR
