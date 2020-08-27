bcadd
=====

2个任意精度数字的加法计算

### 说明

<span class="type">string</span> <span class="methodname">bcadd</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$right_operand`</span> \[, <span
class="methodparam"><span class="type">int</span> `$scale`</span> \] )

`左操作数`和`右操作数`求和

### 参数

`left_operand`  
左操作数，字符串类型

`right_operand`  
右操作数，字符串类型

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

2个操作数求和之后的结果以字符串返回

### 范例

**示例 \#1 <span class="function">bcadd</span> 示例**

``` php
<?php

$a = '1.234';
$b = '5';

echo bcadd($a, $b);     // 6
echo bcadd($a, $b, 4);  // 6.2340

?>
```

### 参见

-   <span class="function">bcsub</span>

bccomp
======

比较两个任意精度的数字

### 说明

<span class="type">int</span> <span class="methodname">bccomp</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$right_operand`</span> \[, <span
class="methodparam"><span class="type">int</span> `$scale`<span
class="initializer"> = int</span></span> \] )

把`right_operand`和`left_operand`作比较, 并且返回一个整数的结果.

### 参数

`left_operand`  
左边的运算数, 是一个字符串.

`right_operand`  
右边的运算数, 是一个字符串.

`scale`  
可选的`scale`参数被用作设置指示数字， 在使用来作比较的小数点部分.

### 返回值

如果两个数相等返回0,
左边的数`left_operand`比较右边的数`right_operand`大返回1, 否则返回-1.

### 范例

**示例 \#1 <span class="function">bccomp</span> example**

``` php
<?php

echo bccomp('1', '2') . "\n";   // -1
echo bccomp('1.00001', '1', 3); // 0
echo bccomp('1.00001', '1', 5); // 1

?>
```

bcdiv
=====

2个任意精度的数字除法计算

### 说明

<span class="type">string</span> <span class="methodname">bcdiv</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$right_operand`</span> \[, <span
class="methodparam"><span class="type">int</span> `$scale`<span
class="initializer"> = int</span></span> \] )

`左操作数`除以`右操作数`

### 参数

`left_operand`  
左操作数，字符串类型

`right_operand`  
右操作数，字符串类型

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

返回结果为字符串类型的结果，如果`右操作数`是0结果为null

### 范例

**示例 \#1 <span class="function">bcdiv</span> 示例**

``` php
<?php

echo bcdiv('105', '6.55957', 3);  // 16.007

?>
```

### 参见

-   <span class="function">bcmul</span>

bcmod
=====

对一个任意精度数字取模

### 说明

<span class="type">string</span> <span class="methodname">bcmod</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$modulus`</span> )

对左操作数使用`系数`取模

### 参数

`left_operand`  
字符串类型的左操作数

`modulus`  
字符串类型系数

### 返回值

返回字符串类型取模后结果，如果系数为0则返回null

### 范例

**示例 \#1 <span class="function">bcmod</span> example**

``` php
<?php
echo bcmod('4', '2'); // 0
echo bcmod('2', '4'); // 2
?>
```

### 参见

-   <span class="function">bcdiv</span>

bcmul
=====

2个任意精度数字乘法计算

### 说明

<span class="type">string</span> <span class="methodname">bcmul</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$right_operand`</span> \[, <span
class="methodparam"><span class="type">int</span> `$scale`<span
class="initializer"> = int</span></span> \] )

`左操作数`乘以`右操作数`

### 参数

`left_operand`  
字符串类型的左操作数.

`right_operand`  
字符串类型的右操作数.

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

返回结果为字符串类型.

### 范例

**示例 \#1 <span class="function">bcmul</span> 示例**

``` php
<?php
echo bcmul('1.34747474747', '35', 3); // 47.161
echo bcmul('2', '4'); // 8
?>
```

### 参见

-   <span class="function">bcdiv</span>

bcpow
=====

任意精度数字的乘方

### 说明

<span class="type">string</span> <span class="methodname">bcpow</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$right_operand`</span> \[, <span
class="methodparam"><span class="type">int</span> `$scale`</span> \] )

`左操作数`的`右操作数`次方运算.

### 参数

`left_operand`  
字符串类型的左操作数.

`right_operand`  
字符串类型的右操作数.

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

返回结果为字符串类型.

### 范例

**示例 \#1 <span class="function">bcpow</span> 示例**

``` php
<?php

echo bcpow('4.2', '3', 2); // 74.08

?>
```

### 注释

> **Note**:
>
> <span class="function">bcpow</span> may return a result with fewer
> digits after the decimal point than the `scale` parameter would
> indicate. This only occurs when the result doesn't require all of the
> precision allowed by the `scale`. For example:
>
> **示例 \#2 <span class="function">bcpow</span> scale example**
>
> ``` php
> <?php
> echo bcpow('5', '2', 2);     // prints "25", not "25.00"
> ?>
> ```

### 参见

-   <span class="function">bcpowmod</span>
-   <span class="function">bcsqrt</span>

bcpowmod
========

Raise an arbitrary precision number to another, reduced by a specified
modulus

### 说明

<span class="type">string</span> <span
class="methodname">bcpowmod</span> ( <span class="methodparam"><span
class="type">string</span> `$base`</span> , <span
class="methodparam"><span class="type">string</span> `$exponent`</span>
, <span class="methodparam"><span class="type">string</span>
`$modulus`</span> \[, <span class="methodparam"><span
class="type">int</span> `$scale`<span class="initializer"> =
0</span></span> \] )

Use the fast-exponentiation method to raise `base` to the power
`exponent` with respect to the modulus `modulus`.

### 参数

`base`  
The base, as an integral string (i.e. the scale has to be zero).

`exponent`  
The exponent, as an non-negative, integral string (i.e. the scale has to
be zero).

`modulus`  
The modulus, as an integral string (i.e. the scale has to be zero).

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

Returns the result as a string, or **`FALSE`** if `modulus` is *0* or
`exponent` is negative.

### 注释

> **Note**:
>
> Because this method uses the modulus operation, numbers which are not
> positive integers may give unexpected results.

### 范例

The following two statements are functionally identical. The <span
class="function">bcpowmod</span> version however, executes in less time
and can accept larger parameters.

``` php
<?php
$a = bcpowmod($x, $y, $mod);

$b = bcmod(bcpow($x, $y), $mod);

// $a and $b are equal to each other.

?>
```

### 参见

-   <span class="function">bcpow</span>
-   <span class="function">bcmod</span>

bcscale
=======

设置所有bc数学函数的默认小数点保留位数

### 说明

<span class="type">bool</span> <span class="methodname">bcscale</span> (
<span class="methodparam"><span class="type">int</span> `$scale`</span>
)

设置所有bc数学函数的未设定情况下得小数点保留位数.

### 参数

`scale`  
小数点保留位数.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bcscale</span> example**

``` php
<?php

// default scale : 3
bcscale(3);
echo bcdiv('105', '6.55957'); // 16.007

// this is the same without bcscale()
echo bcdiv('105', '6.55957', 3); // 16.007

?>
```

bcsqrt
======

任意精度数字的二次方根

### 说明

<span class="type">string</span> <span class="methodname">bcsqrt</span>
( <span class="methodparam"><span class="type">string</span>
`$operand`</span> \[, <span class="methodparam"><span
class="type">int</span> `$scale`</span> \] )

返回`操作数`的二次方根.

### 参数

`operand`  
字符串类型的操作数.

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

返回二次方根的结果为字符串类型，如果操作数是负数则返回null.

### 范例

**示例 \#1 <span class="function">bcsqrt</span> 示例**

``` php
<?php

echo bcsqrt('2', 3); // 1.414

?>
```

### 参见

-   <span class="function">bcpow</span>

bcsub
=====

2个任意精度数字的减法

### 说明

<span class="type">string</span> <span class="methodname">bcsub</span> (
<span class="methodparam"><span class="type">string</span>
`$left_operand`</span> , <span class="methodparam"><span
class="type">string</span> `$right_operand`</span> \[, <span
class="methodparam"><span class="type">int</span> `$scale`<span
class="initializer"> = int</span></span> \] )

`左操作数`减去`右操作数`.

### 参数

`left_operand`  
字符串类型的左操作数.

`right_operand`  
字符串类型的右操作数.

` scale`  
此可选参数用于设置结果中小数点后的小数位数。也可通过使用 <span
class="function">bcscale</span>
来设置全局默认的小数位数，用于所有函数。如果未设置，则默认为 *0*。

### 返回值

返回减法之后结果为字符串类型.

### 范例

**示例 \#1 <span class="function">bcsub</span> example**

``` php
<?php

$a = '1.234';
$b = '5';

echo bcsub($a, $b);     // -3
echo bcsub($a, $b, 4);  // -3.7660

?>
```

### 参见

-   <span class="function">bcadd</span>

**目录**

-   [bcadd](/ref/bc.html#bcadd) — 2个任意精度数字的加法计算
-   [bccomp](/ref/bc.html#bccomp) — 比较两个任意精度的数字
-   [bcdiv](/ref/bc.html#bcdiv) — 2个任意精度的数字除法计算
-   [bcmod](/ref/bc.html#bcmod) — 对一个任意精度数字取模
-   [bcmul](/ref/bc.html#bcmul) — 2个任意精度数字乘法计算
-   [bcpow](/ref/bc.html#bcpow) — 任意精度数字的乘方
-   [bcpowmod](/ref/bc.html#bcpowmod) — Raise an arbitrary precision
    number to another, reduced by a specified modulus
-   [bcscale](/ref/bc.html#bcscale) —
    设置所有bc数学函数的默认小数点保留位数
-   [bcsqrt](/ref/bc.html#bcsqrt) — 任意精度数字的二次方根
-   [bcsub](/ref/bc.html#bcsub) — 2个任意精度数字的减法
