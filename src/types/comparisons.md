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
class="type">整数</span>。**`FALSE`** 是一个<span
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
> against any other value, including itself, but except **`TRUE`**, will
> have a result of **`FALSE`**. (i.e. *NAN != NAN* and *NAN !== NAN*)
> Examples of operations that produce **`NAN`** include *sqrt(-1)*,
> *asin(2)*, and *acosh(0)*.

| 表达式                  | <span class="function">gettype</span> | <span class="function">empty</span> | <span class="function">is\_null</span> | <span class="function">isset</span> | <span class="type">boolean</span> : *if($x)* |
|-------------------------|---------------------------------------|-------------------------------------|----------------------------------------|-------------------------------------|----------------------------------------------|
| *$x = "";*              | <span class="type">string</span>      | **`TRUE`**                          | **`FALSE`**                            | **`TRUE`**                          | **`FALSE`**                                  |
| *$x = null;*            | <span class="type">NULL</span>        | **`TRUE`**                          | **`TRUE`**                             | **`FALSE`**                         | **`FALSE`**                                  |
| *var $x;*               | <span class="type">NULL</span>        | **`TRUE`**                          | **`TRUE`**                             | **`FALSE`**                         | **`FALSE`**                                  |
| `$x` is undefined       | <span class="type">NULL</span>        | **`TRUE`**                          | **`TRUE`**                             | **`FALSE`**                         | **`FALSE`**                                  |
| *$x = array();*         | <span class="type">array</span>       | **`TRUE`**                          | **`FALSE`**                            | **`TRUE`**                          | **`FALSE`**                                  |
| *$x = array('a', 'b');* | <span class="type">array</span>       | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = false;*           | <span class="type">boolean</span>     | **`TRUE`**                          | **`FALSE`**                            | **`TRUE`**                          | **`FALSE`**                                  |
| *$x = true;*            | <span class="type">boolean</span>     | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = 1;*               | <span class="type">integer</span>     | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = 42;*              | <span class="type">integer</span>     | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = 0;*               | <span class="type">integer</span>     | **`TRUE`**                          | **`FALSE`**                            | **`TRUE`**                          | **`FALSE`**                                  |
| *$x = -1;*              | <span class="type">integer</span>     | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = "1";*             | <span class="type">string</span>      | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = "0";*             | <span class="type">string</span>      | **`TRUE`**                          | **`FALSE`**                            | **`TRUE`**                          | **`FALSE`**                                  |
| *$x = "-1";*            | <span class="type">string</span>      | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = "php";*           | <span class="type">string</span>      | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = "true";*          | <span class="type">string</span>      | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |
| *$x = "false";*         | <span class="type">string</span>      | **`FALSE`**                         | **`FALSE`**                            | **`TRUE`**                          | **`TRUE`**                                   |

|             | **`TRUE`**  | **`FALSE`** | *1*         | *0*         | *-1*        | *"1"*       | *"0"*       | *"-1"*      | **`NULL`**  | *array()*   | *"php"*     | *""*        |
|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **`TRUE`**  | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** |
| **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`TRUE`**  | **`FALSE`** | **`TRUE`**  |
| *1*         | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *0*         | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`TRUE`**  |
| *-1*        | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *"1"*       | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *"0"*       | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *"-1"*      | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| **`NULL`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`TRUE`**  | **`FALSE`** | **`TRUE`**  |
| *array()*   | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`TRUE`**  | **`FALSE`** | **`FALSE`** |
| *"php"*     | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** |
| *""*        | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`TRUE`**  |

|             | **`TRUE`**  | **`FALSE`** | *1*         | *0*         | *-1*        | *"1"*       | *"0"*       | *"-1"*      | **`NULL`**  | *array()*   | *"php"*     | *""*        |
|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|-------------|
| **`TRUE`**  | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *1*         | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *0*         | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *-1*        | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *"1"*       | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *"0"*       | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *"-1"*      | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| **`NULL`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** | **`FALSE`** |
| *array()*   | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** | **`FALSE`** |
| *"php"*     | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  | **`FALSE`** |
| *""*        | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`FALSE`** | **`TRUE`**  |
