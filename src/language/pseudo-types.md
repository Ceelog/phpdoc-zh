本文档中使用的伪类型与变量
--------------------------

伪类型（pseudo-types） 是 PHP 文档里用于指示参数可以使用的类型和值。
请注意，它们不是 PHP 语言里原生类型。
所以不能把伪类型用于自定义函数里的类型约束（typehint）。

### mixed

*mixed* 说明一个参数可以接受多种不同的（但不一定是所有的）类型。

例如 <span class="function">gettype</span> 可以接受所有的 PHP
类型，<span class="function">str\_replace</span> 可以接受字符串和数组。

### number

*number* 说明一个参数可以是 <span class="type">integer</span> 或者 <span
class="type">float</span>。

### array\|object

*array\|object* 意思是参数既可以是 <span class="type">array</span>
也可以是 <span class="type">object</span>。

### void

*void* 作为返回类型意味着函数的返回值是无用的。*void*
作为参数列表意味着函数不接受任何参数。从 PHP 7.1 开始 *void*
接受一个函数为返回类型。

### ...

在函数原型中，`$...`
表示*等等*的意思。当一个函数可以接受任意个参数时使用此变量名。
