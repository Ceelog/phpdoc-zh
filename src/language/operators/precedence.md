运算符优先级
------------

运算符优先级指定了两个表达式绑定得有多“紧密”。例如，表达式 *1 + 5 \* 3*
的结果是 *16* 而不是 *18*
是因为乘号（“\*”）的优先级比加号（“+”）高。必要时可以用括号来强制改变优先级。例如：*(1
+ 5) \* 3* 的值为 *18*。

如果运算符优先级相同，那运算符的结合方向决定了该如何运算。例如，"-"是左联的，那么
*1 - 2 - 3* 就等同于 *(1 - 2) - 3* 并且结果是 *-4*.
另外一方面，"="是右联的，所以 *$a = $b = $c* 等同于 *$a = ($b = $c)*。

没有结合的相同优先级的运算符不能连在一起使用，例如 *1 \< 2 \> 1*
在PHP是不合法的。但另外一方面表达式 *1 \<= 1 == 1* 是合法的, 因为 *==*
的优先级低于 *\<=*。

括号的使用，哪怕在不是必要的场合下，通过括号的配对来明确标明运算顺序，而非靠运算符优先级和结合性来决定，通常能够增加代码的可读性。

下表按照优先级从高到低列出了运算符。同一行中的运算符具有相同优先级，此时它们的结合方向决定求值顺序。

| 结合方向 | 运算符                                                                           | 附加信息                                                                                                                                             |
|----------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 不适用   | *clone* *new*                                                                    | <a href="/language/oop5/cloning.html" class="link">clone</a> 和 <a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>     |
| 右       | *\*\**                                                                           | <a href="/language/operators/arithmetic.html" class="link">算术运算符</a>                                                                            |
| 不适用   | *++* *--* *\~* *(int)* *(float)* *(string)* *(array)* *(object)* *(bool)* *@*    | <a href="/language/types.html" class="link">类型</a>、<a href="/language/operators/increment.html" class="link">递增／递减</a>                       |
| 左       | *instanceof*                                                                     | <a href="/language/types.html" class="link">类型</a>                                                                                                 |
| 不适用   | *!*                                                                              | <a href="/language/operators/logical.html" class="link">逻辑运算符</a>                                                                               |
| 左       | *\** */* *%*                                                                     | <a href="/language/operators/arithmetic.html" class="link">算术运算符</a>                                                                            |
| 左       | *+* *-* *.*                                                                      | <a href="/language/operators/arithmetic.html" class="link">算术运算符</a> 和 <a href="/language/operators/string.html" class="link">字符串运算符</a> |
| 左       | *\<\<* *\>\>*                                                                    | <a href="/language/operators/bitwise.html" class="link">位运算符</a>                                                                                 |
| 无       | *\<* *\<=* *\>* *\>=*                                                            | <a href="/language/operators/comparison.html" class="link">比较运算符</a>                                                                            |
| 无       | *==* *!=* *===* *!==* *\<\>* *\<=\>*                                             | <a href="/language/operators/comparison.html" class="link">比较运算符</a>                                                                            |
| 左       | *&*                                                                              | <a href="/language/operators/bitwise.html" class="link">位运算符</a> 和 <a href="/language/references.html" class="link">引用</a>                    |
| 左       | *^*                                                                              | <a href="/language/operators/bitwise.html" class="link">位运算符</a>                                                                                 |
| 左       | *\|*                                                                             | <a href="/language/operators/bitwise.html" class="link">位运算符</a>                                                                                 |
| 左       | *&&*                                                                             | <a href="/language/operators/logical.html" class="link">逻辑运算符</a>                                                                               |
| 左       | *\|\|*                                                                           | <a href="/language/operators/logical.html" class="link">逻辑运算符</a>                                                                               |
| 右       | *??*                                                                             | <a href="/language/operators/comparison.html#language.operators.comparison.coalesce" class="link">null 合并运算符</a>                                |
| 左       | *? :*                                                                            | <a href="/language/operators/comparison.html#language.operators.comparison.ternary" class="link">三元运算符</a>                                      |
| 右       | *=* *+=* *-=* *\*=* *\*\*=* */=* *.=* *%=* *&=* *\|=* *^=* *\<\<=* *\>\>=* *??=* | <a href="/language/operators/assignment.html" class="link">赋值运算符</a>                                                                            |
| 不适用   | *yield from*                                                                     | <a href="/language/generators/syntax.html#control-structures.yield.from" class="link">yield from</a>                                                 |
| 不适用   | *yield*                                                                          | <a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>                                                           |
| 不适用   | *print*                                                                          | <span class="function">print</span>                                                                                                                  |
| 左       | *and*                                                                            | <a href="/language/operators/logical.html" class="link">逻辑运算符</a>                                                                               |
| 左       | *xor*                                                                            | <a href="/language/operators/logical.html" class="link">逻辑运算符</a>                                                                               |
| 左       | *or*                                                                             | <a href="/language/operators/logical.html" class="link">逻辑运算符</a>                                                                               |

**示例 \#1 结合方向**

``` php
<?php
$a = 3 * 3 % 5; // (3 * 3) % 5 = 4
// ternary operator associativity differs from C/C++
$a = true ? 0 : true ? 1 : 2; // (true ? 0 : true) ? 1 : 2 = 2

$a = 1;
$b = 2;
$a = $b += 3; // $a = ($b += 3) -> $a = 5, $b = 5
?>
```

Operator precedence and associativity only determine how expressions are
grouped, they do not specify an order of evaluation. PHP does not (in
the general case) specify in which order an expression is evaluated and
code that assumes a specific order of evaluation should be avoided,
because the behavior can change between versions of PHP or depending on
the surrounding code.

**示例 \#2 Undefined order of evaluation**

``` php
<?php
$a = 1;
echo $a + $a++; // may print either 2 or 3

$i = 1;
$array[$i] = $i++; // may set either index 1 or 2
?>
```

**示例 \#3 *+*、*-* 、*.* 具有相同的优先级**

``` php
<?php
$x = 4;
// this line might result in unexpected output:
echo "x minus one equals " . $x-1 . ", or so I hope\n";
// because it is evaluated like this line:
echo (("x minus one equals " . $x) - 1) . ", or so I hope\n";
// the desired precedence can be enforced by using parentheses:
echo "x minus one equals " . ($x-1) . ", or so I hope\n";
?>
```

以上例程会输出：

    -1, or so I hope
    -1, or so I hope
    x minus one equals 3, or so I hope

> **Note**:
>
> 尽管 *=* 比其它大多数的运算符的优先级低，PHP
> 仍旧允许类似如下的表达式：*if (!$a = foo())*，在此例中 *foo()*
> 的返回值被赋给了 `$a`。
