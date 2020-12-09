PHP 类型比较表
==============

以下的表格显示了 PHP
<a href="/language/types.html" class="link">类型</a> 和
<a href="/language/operators/comparison.html" class="link">比较运算符</a>
在松散和严格比较时的作用。该补充材料还和
<a href="/language/types/type-juggling.html" class="link">类型戏法</a>
的相关章节内容有关。同时，大量的用户注释和
<a href="http://www.blueshoes.org/en/developer/php_cheat_sheet/" class="link external">» BlueShoes</a>
的工作也给该材料提供了帮助。

在使用这些表格之前，需要明白变量类型及它们的意义。例如，*"42"*
是一个<span class="type">字符串</span>而 *42* 是一个<span
class="type">整数</span>。**`false`** 是一个<span
class="type">布尔</span>值而 *"false"* 是一个<span
class="type">字符串</span>。

> **Note**:
>
> HTML
> 表单并不传递整数、浮点数或者布尔值，它们只传递字符串。要想检测一个字符串是不是数字，可以使用
> <span class="function">is\_numeric</span> 函数。

> **Note**:
>
> 在没有定义变量 `$x` 的时候，诸如 *if ($x)* 的用法会导致一个
> **`E_NOTICE`** 级别的错误。所以，可以考虑用 <span
> class="function">empty</span> 或者 <span class="function">isset</span>
> 函数来初始化变量。

> **Note**:
>
> Some numeric operations can result in a value represented by the
> constant **`NAN`**. Any loose or strict comparisons of this value
> against any other value, including itself, but except **`true`**, will
> have a result of **`false`**. (i.e. *NAN != NAN* and *NAN !== NAN*)
> Examples of operations that produce **`NAN`** include *sqrt(-1)*,
> *asin(2)*, and *acosh(0)*.

| 表达式                  | <span class="function">gettype</span> | <span class="function">empty</span> | <span class="function">is\_null</span> | <span class="function">isset</span> | <span class="type">boolean</span> : *if($x)* |
|-------------------------|---------------------------------------|-------------------------------------|----------------------------------------|-------------------------------------|----------------------------------------------|
| *$x = "";*              | <span class="type">string</span>      | **`true`**                          | **`false`**                            | **`true`**                          | **`false`**                                  |
| *$x = null;*            | <span class="type">NULL</span>        | **`true`**                          | **`true`**                             | **`false`**                         | **`false`**                                  |
| *var $x;*               | <span class="type">NULL</span>        | **`true`**                          | **`true`**                             | **`false`**                         | **`false`**                                  |
| `$x` is undefined       | <span class="type">NULL</span>        | **`true`**                          | **`true`**                             | **`false`**                         | **`false`**                                  |
| *$x = array();*         | <span class="type">array</span>       | **`true`**                          | **`false`**                            | **`true`**                          | **`false`**                                  |
| *$x = array('a', 'b');* | <span class="type">array</span>       | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = false;*           | <span class="type">boolean</span>     | **`true`**                          | **`false`**                            | **`true`**                          | **`false`**                                  |
| *$x = true;*            | <span class="type">boolean</span>     | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = 1;*               | <span class="type">integer</span>     | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = 42;*              | <span class="type">integer</span>     | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = 0;*               | <span class="type">integer</span>     | **`true`**                          | **`false`**                            | **`true`**                          | **`false`**                                  |
| *$x = -1;*              | <span class="type">integer</span>     | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = "1";*             | <span class="type">string</span>      | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = "0";*             | <span class="type">string</span>      | **`true`**                          | **`false`**                            | **`true`**                          | **`false`**                                  |
| *$x = "-1";*            | <span class="type">string</span>      | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = "php";*           | <span class="type">string</span>      | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = "true";*          | <span class="type">string</span>      | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |
| *$x = "false";*         | <span class="type">string</span>      | **`false`**                         | **`false`**                            | **`true`**                          | **`true`**                                   |

|             | **`true`**  | **`false`** | *1*         | *0*         | *-1*        | *"1"*       | *"0"*       | *"-1"*      | **`null`**  | *array()*   | *"php"*     | *""*        |
|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **`true`**  | **`true`**  | **`false`** | **`true`**  | **`false`** | **`true`**  | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** |
| **`false`** | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`true`**  | **`true`**  | **`false`** | **`true`**  |
| *1*         | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *0*         | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`true`**  | **`true`**  |
| *-1*        | **`true`**  | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** |
| *"1"*       | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *"0"*       | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *"-1"*      | **`true`**  | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** |
| **`null`**  | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`true`**  | **`false`** | **`true`**  |
| *array()*   | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`true`**  | **`false`** | **`false`** |
| *"php"*     | **`true`**  | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** |
| *""*        | **`false`** | **`true`**  | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`true`**  |

|             | **`true`**  | **`false`** | *1*         | *0*         | *-1*        | *"1"*       | *"0"*       | *"-1"*      | **`null`**  | *array()*   | *"php"*     | *""*        |
|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **`true`**  | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *1*         | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *0*         | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *-1*        | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *"1"*       | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *"0"*       | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** |
| *"-1"*      | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** | **`false`** |
| **`null`**  | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** | **`false`** |
| *array()*   | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** | **`false`** |
| *"php"*     | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  | **`false`** |
| *""*        | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`false`** | **`true`**  |
