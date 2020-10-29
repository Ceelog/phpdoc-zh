赋值运算符
----------

基本的赋值运算符是“=”。一开始可能会以为它是“等于”，其实不是的。它实际上意味着把右边表达式的值赋给左边的运算数。

赋值运算表达式的值也就是所赋的值。也就是说，“*$a = 3*”的值是
3。这样就可以做一些小技巧：

``` php
<?php

$a = ($b = 4) + 5; // $a 现在成了 9，而 $b 成了 4。

?>
```

在基本赋值运算符之外，还有适合于所有<a href="/language/operators.html" class="link">二元算术</a>，数组集合和字符串运算符的“组合运算符”，这样可以在一个表达式中使用它的值并把表达式的结果赋给它，例如：

``` php
<?php

$a = 3;
$a += 5; // sets $a to 8, as if we had said: $a = $a + 5;
$b = "Hello ";
$b .= "There!"; // sets $b to "Hello There!", just like $b = $b . "There!";

?>
```

注意赋值运算将原变量的值拷贝到新变量中（传值赋值），所以改变其中一个并不影响另一个。这也适合于在密集循环中拷贝一些值例如大数组。

在 PHP 中普通的传值赋值行为有个例外就是碰到对象 <span
class="type">object</span> 时，在 PHP 5 中是以引用赋值的，除非明确使用了
<a href="/language/oop5/cloning.html" class="link">clone</a>
关键字来拷贝。

### 引用赋值

PHP 支持引用赋值，使用“<span class="computeroutput">$var =
&$othervar;</span>”语法。引用赋值意味着两个变量指向了同一个数据，没有拷贝任何东西。

**示例 \#1 引用赋值**

``` php
<?php
$a = 3;
$b = &$a; // $b 是 $a 的引用

print "$a\n"; // 输出 3
print "$b\n"; // 输出 3

$a = 4; // 修改 $a

print "$a\n"; // 输出 4
print "$b\n"; // 也输出 4，因为 $b 是 $a 的引用，因此也被改变
?>
```

<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
运算符自动返回一个引用，因此在 PHP 7.0.0及之后的版本中禁止对
<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
的结果进行引用赋值； PHP 5.3.0 及之后的版本则发出一条 **`E_DEPRECATED`**
错误信息；在更早的版本中发出的是 **`E_STRICT`**。

例如以下代码将产生错误或警告：

``` php
<?php
class C {}

$o = &new C;
?>
```

以上例程在 PHP 7 中的输出：

    Parse error: syntax error, unexpected 'new' (T_NEW) in …

以上例程在 PHP 5.3 中的输出：

    Deprecated: Assigning the return value of new by reference is deprecated in …

以上例程在 PHP 5 中的输出：

    Strict Standards: Assigning the return value of new by reference is deprecated in …

有关引用更多信息参见本手册中<a href="/language/references.html" class="link">引用的解释</a>一章。

### 算术赋值运算符

| 例子      | 等同于        | 操作 |
|-----------|---------------|------|
| $a += $b  | $a = $a + b   | 加法 |
| $a -= $b  | $a = $a - $b  | 减法 |
| $a \*= $b | $a = $a \* $b | 乘法 |
| $a /= $b  | $a = $a / $b  | 除法 |
| $a %= $b  | $a = $a % $b  | 取模 |

### 位赋值运算符

| 例子        | 等同于          | 操作     |
|-------------|-----------------|----------|
| $a &= $b    | $a = $a & $b    | 按位与   |
| $a \|= $b   | $a = $a \| $b   | 按位或   |
| $a ^= $b    | $a = $a ^ $b    | 按位异或 |
| $a \<\<= $b | $a = $a \<\< $b | 左移     |
| $a \>\>= $b | $a = $a \>\> $b | 右移     |

### 其他赋值运算符

| 例子      | 等同于        | 操作       |
|-----------|---------------|------------|
| $a .= $b  | $a = $a . $b  | 字符串拼接 |
| $a ??= $b | $a = $a ?? $b | NULL 合并  |

可参见手册中
<a href="/language/operators/arithmetic.html" class="link">算术运算符</a>、<a href="/language/operators/bitwise.html" class="link">位运算符</a>、
<a href="/language/operators/string.html" class="link">字符串运算符</a>、
<a href="/language/operators/comparison.html#language.operators.comparison.coalesce" class="link">NULL 合并运算符</a>章节。
