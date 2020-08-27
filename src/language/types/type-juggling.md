类型转换的判别
--------------

PHP
在变量定义中不需要（或不支持）明确的类型定义；变量类型是根据使用该变量的上下文所决定的。也就是说，如果把一个
<span class="type">string</span> 值赋给变量 `$var`，`$var` 就成了一个
<span class="type">string</span>。如果又把一个<span
class="type">integer</span> 赋给 `$var`，那它就成了一个<span
class="type">integer</span>。

PHP 的自动类型转换的一个例子是乘法运算符“\*”。如果任何一个操作数是<span
class="type">float</span>，则所有的操作数都被当成<span
class="type">float</span>，结果也是<span
class="type">float</span>。否则操作数会被解释为<span
class="type">integer</span>，结果也是<span
class="type">integer</span>。注意这并*没有*改变这些操作数本身的类型；改变的仅是这些操作数如何被求值以及表达式本身的类型。

``` php
<?php
$foo = "1";  // $foo 是字符串 (ASCII 49)
$foo *= 2;   // $foo 现在是一个整数 (2)
$foo = $foo * 1.3;  // $foo 现在是一个浮点数 (2.6)
$foo = 5 * "10 Little Piggies"; // $foo 是整数 (50)
$foo = 5 * "10 Small Pigs";     // $foo 是整数 (50)
?>
```

如果上面两个例子看上去古怪的话，参见<a href="/language/types/string.html#language.types.string.conversion" class="link">字符串转换为数值</a>。

如果要强制将一个变量当作某种类型来求值，参见<a href="/language/types/type-juggling.html#language.types.typecasting" class="link">类型强制转换</a>一节。如果要改变一个变量的类型，参见
<span class="function">settype</span>。

如果想要测试本节中任何例子的话，可以用 <span
class="function">var\_dump</span> 函数。

> **Note**:
>
> 自动转换为 <span class="type">数组</span> 的行为目前没有定义。
>
> 此外，由于 PHP
> 支持使用和数组下标同样的语法访问字符串下标，以下例子在所有 PHP
> 版本中都有效：
>
> ``` php
> <?php
> $a    = 'car'; // $a is a string
> $a[0] = 'b';   // $a is still a string
> echo $a;       // bar
> ?>
> ```
>
> 请参阅<a href="/language/types/string.html#language.types.string.substr" class="link">存取和修改字符串中的字符</a>一节以获取更多信息。

### 类型强制转换

PHP 中的类型强制转换和 C
中的非常像：在要转换的变量之前加上用括号括起来的目标类型。

``` php
<?php
$foo = 10;   // $foo is an integer
$bar = (boolean) $foo;   // $bar is a boolean
?>
```

允许的强制转换有：

-   <span class="simpara">(int), (integer) - 转换为整形 <span
    class="type">integer</span></span>
-   <span class="simpara">(bool), (boolean) - 转换为布尔类型 <span
    class="type">boolean</span></span>
-   <span class="simpara">(float), (double), (real) - 转换为浮点型 <span
    class="type">float</span></span>
-   <span class="simpara">(string) - 转换为字符串 <span
    class="type">string</span></span>
-   <span class="simpara">(array) - 转换为数组 <span
    class="type">array</span></span>
-   <span class="simpara">(object) - 转换为对象 <span
    class="type">object</span></span>
-   <span class="simpara">(unset) - 转换为 <span
    class="type">NULL</span></span>

(binary) 转换和 b 前缀转换支持为 PHP 5.2.1 新增。注意 (binary) 转换和
(string) 基本相同，但是不应该依赖它。

(unset) 转换在 PHP 7.2.0 中已被废弃。请注意 (unset) 转换等于将值赋予
<span class="type">NULL</span>。(unset) 转换将在 PHP 8.0.0 中被移除。

注意在括号内允许有空格和制表符，所以下面两个例子功能相同：

``` php
<?php
$foo = (int) $bar;
$foo = ( int ) $bar;
?>
```

将字符串文字和变量转换为二进制字符串：

``` php
<?php
$binary = (binary)$string;
$binary = b"binary string";
?>
```

> **Note**:
>
> 可以将变量放置在双引号中的方式来代替将变量转换成字符串：
>
> ``` php
> <?php
> $foo = 10;            // $foo 是一个整数
> $str = "$foo";        // $str 是一个字符串
> $fst = (string) $foo; // $fst 也是一个字符串
>
> // 输出 "they are the same"
> if ($fst === $str) {
>     echo "they are the same";
> }
> ?>
> ```

有时在类型之间强制转换时确切地会发生什么可能不是很明显。更多信息见如下小节：

-   <span class="simpara">
    <a href="/language/types/boolean.html#language.types.boolean.casting" class="link">转换为布尔型</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/integer.html#language.types.integer.casting" class="link">转换为整型</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/float.html#language.types.float.casting" class="link">转换为浮点型</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/string.html#language.types.string.casting" class="link">转换为字符串</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/array.html#language.types.array.casting" class="link">转换为数组</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/object.html#language.types.object.casting" class="link">转换为对象</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/resource.html#language.types.resource.casting" class="link">转换为资源</a>
    </span>
-   <span class="simpara">
    <a href="/language/types/null.html#language.types.null.casting" class="link">转换为 NULL</a>
    </span>
-   <span class="simpara">
    <a href="/types/comparisons.html" class="link">类型比较表</a>
    </span>
