用户自定义函数
--------------

一个函数可由以下的语法来定义：

**示例 \#1 展示函数用途的伪代码**

``` php
<?php
function foo($arg_1, $arg_2, /* ..., */ $arg_n)
{
    echo "Example function.\n";
    return $retval;
}
?>
```

任何有效的 PHP 代码都有可能出现在函数内部，甚至包括其它函数和
<a href="/language/oop5/basic.html#language.oop5.basic.class" class="link">类</a>定义。

函数名和 PHP
中的其它标识符命名规则相同。有效的函数名以字母或下划线打头，后面跟字母，数字或下划线。可以用正则表达式表示为:
`^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*$`。

**小贴士**

请参见<a href="/userlandnaming.html" class="xref">用户空间命名指南</a>。

函数无需在调用之前被定义，*除非* 是下面两个例子中函数是有条件被定义时。

当一个函数是有条件被定义时，必须在调用函数 *之前* 定义。

**示例 \#2 有条件的函数**

``` php
<?php

$makefoo = true;

/* 不能在此处调用foo()函数，
   因为它还不存在，但可以调用bar()函数。*/

bar();

if ($makefoo) {
  function foo()
  {
    echo "I don't exist until program execution reaches me.\n";
  }
}

/* 现在可以安全调用函数 foo()了，
   因为 $makefoo 值为真 */

if ($makefoo) foo();

function bar()
{
  echo "I exist immediately upon program start.\n";
}

?>
```

**示例 \#3 函数中的函数**

``` php
<?php
function foo()
{
  function bar()
  {
    echo "I don't exist until foo() is called.\n";
  }
}

/* 现在还不能调用bar()函数，因为它还不存在 */

foo();

/* 现在可以调用bar()函数了，因为foo()函数
   的执行使得bar()函数变为已定义的函数 */

bar();

?>
```

PHP
中的所有函数和类都具有全局作用域，可以定义在一个函数之内而在之外调用，反之亦然。

PHP 不支持函数重载，也不可能取消定义或者重定义已声明的函数。

> **Note**: <span class="simpara"> 从 *A* 到 *Z* 的 ASCII
> 函数名是大小写无关的，不过在调用函数的时候，使用其在定义时相同的形式是个好习惯。
> </span>

PHP 的函数支持
<a href="/functions/arguments.html#functions.variable-arg-list" class="link">可变数量的参数</a>
和
<a href="/functions/arguments.html#functions.arguments.default" class="link">默认参数</a>。参见
<span class="function">func\_num\_args</span>，<span
class="function">func\_get\_arg</span> 和 <span
class="function">func\_get\_args</span>。

在 PHP 中可以调用递归函数。

**示例 \#4 递归函数**

``` php
<?php
function recursion($a)
{
    if ($a < 20) {
        echo "$a\n";
        recursion($a + 1);
    }
}
?>
```

> **Note**: <span class="simpara"> 但是要避免递归函数／方法调用超过
> 100-200 层，因为可能会使堆栈崩溃从而使当前脚本终止。
> 无限递归可视为编程错误。 </span>
