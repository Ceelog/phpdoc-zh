运算符
======

**目录**

-   [运算符优先级](/language/operators/precedence.html)
-   [算术运算符](/language/operators/arithmetic.html)
-   [赋值运算符](/language/operators/assignment.html)
-   [位运算符](/language/operators/bitwise.html)
-   [比较运算符](/language/operators/comparison.html)
-   [错误控制运算符](/language/operators/errorcontrol.html)
-   [执行运算符](/language/operators/execution.html)
-   [递增／递减运算符](/language/operators/increment.html)
-   [逻辑运算符](/language/operators/logical.html)
-   [字符串运算符](/language/operators/string.html)
-   [数组运算符](/language/operators/array.html)
-   [类型运算符](/language/operators/type.html)

运算符是可以通过给出的一或多个值（用编程行话来说，表达式）来产生另一个值（因而整个结构成为一个表达式）的东西。

运算符可按照其能接受几个值来分组。一元运算符只能接受一个值，例如
*!*（<a href="/language/operators/logical.html" class="link">逻辑取反运算符</a>）或
*++*（<a href="/language/operators/increment.html" class="link">递增运算符</a>）。
二元运算符可接受两个值，例如熟悉的<a href="/language/operators/arithmetic.html" class="link">算术运算符</a>
*+*（加）和 *-*（减），大多数 PHP
运算符都是这种。最后是唯一的<a href="/language/operators/comparison.html#language.operators.comparison.ternary" class="link">三元运算符</a>
*?
:*，可接受三个值；通常就简单称之为“三元运算符”（尽管称之为条件运算符可能更合适）。

PHP
的运算符完整列表见下节<a href="/language/operators/precedence.html" class="link">运算符优先级</a>。该节也解释了运算符优先级和结合方向，这控制着在表达式包含有若干个不同运算符时究竟怎样对其求值。
