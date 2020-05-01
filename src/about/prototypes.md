如何阅读函数的定义（函数原型）
------------------------------

文档中的每个函数都只是快速参考，学会如何阅读和理解文档将使得 PHP
的使用更加简单。和依赖赖于复制／粘贴范例比起来，用户一定更希望知道如何阅读函数的定义（函数原型）：

> **Note**:
> **先决条件，对<a href="/language/types.html" class="link">变量类型</a>的基本理解**  
>
> 尽管 PHP
> 是一种松散类型语言，但<a href="/language/types.html" class="link">变量类型</a>有重要的意义，需要理解它的基本知识。

函数定义告诉我们函数<a href="/functions/returning-values.html" class="link">返回</a>什么类型的值，让我们用函数
<span class="function">strlen</span> 的定义作为第一个范例：

    strlen

    (PHP 4, PHP 5)
    strlen -- 获取字符串长度

    说明
    strlen ( string $string ) : int

    返回给定的字符串 string 的长度。

| 组成部分       | 说明                                                                                                 |
|----------------|------------------------------------------------------------------------------------------------------|
| strlen         | 函数名称。                                                                                           |
| (PHP 4, PHP 5) | strlen() 在 PHP 4 和 PHP 5 的所有版本中都存在。                                                      |
| ( string str ) | 第一个（本例中是唯一的）参数，在该函数中名为 `string`，且类型为 <span class="type">string</span>。   |
| int            | 该函数返回的值的类型，这里为整型 <span class="type">integer</span>（即以数字来衡量的字符串的长度）。 |

可以将以上函数的定义写成一般形式：

              函数名          ( 参数类型           参数名 )        返回类型
          function name    ( parameter type   parameter name ) : returned type

很多函数都有多个变量，例如 <span
class="function">in\_array</span>。其函数原型如下：

          in_array ( mixed $needle, array $haystack [, bool $strict = FALSE ] ) : bool

这是什么意思？<span class="function">in\_array</span>
返回一个“<a href="/language/types/boolean.html" class="link">布尔</a>”值，成功（如果在参数
`haystack` 中能找到参数 `needle`）则返回 **`TRUE`**, 或者在失败时返回
**`FALSE`**（如果在参数 `haystack` 中找不到参数
`needle`）。第一个参数被命名为 `needle`
且其<a href="/language/types.html" class="link">类型</a>不定，因此我们将其称为“*混和*”类型。该混和类型的
`needle`
参数（我们要找的对象）可以是一个标量的值（字符串、整数、或者<a href="/language/types/float.html" class="link">浮点数</a>），或者一个<a href="/language/types/array.html" class="link">数组</a>。`haystack`（我们寻找的范围）是第二个参数。第三个*可选*参数被命名为
`strict`。所有的可选参数都用 *\[* 方括号 *\]* 括起来。手册表明 `strict`
参数默认值为布尔值
**`FALSE`**。需要了解函数工作的细节，请参阅手册中和该函数相关的页面。

函数参数前的 & 符号使参数以
<a href="/language/references/pass.html" class="link">引用</a>
方式传递，如下所见：

     
           preg_match ( string $pattern , string $subject [, array &$matches
          [, int $flags = 0 [, int $offset = 0 ]]] ) : int

在这个例子中，我们可以看到，第三个可选参数 `&$matches`
会意引用方式传递。

有的函数包含更复杂的 PHP 版本信息。我们拿 <span
class="function">html\_entity\_decode</span> 举例：

    (PHP 4 >= 4.3.0, PHP 5)

它意味着该函数只可在 PHP 4.3.0 及以后发布的版本中使用。
