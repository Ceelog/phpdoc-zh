简介
----

PHP 支持 9 种原始数据类型。

四种标量类型：

-   <span class="simpara"> <span class="type">boolean</span>（布尔型）
    </span>
-   <span class="simpara"> <span class="type">integer</span>（整型）
    </span>
-   <span class="simpara"> <span
    class="type">float</span>（浮点型，也称作 <span
    class="type">double</span>) </span>
-   <span class="simpara"> <span class="type">string</span>（字符串）
    </span>

三种复合类型：

-   <span class="simpara"> <span class="type">array</span>（数组）
    </span>
-   <span class="simpara"> <span class="type">object</span>（对象）
    </span>
-   <span class="simpara"> <span class="type">callable</span>（可调用）
    </span>

最后是两种特殊类型：

-   <span class="simpara"> <span class="type">resource</span>（资源）
    </span>
-   <span class="simpara"> <span class="type">NULL</span>（无类型）
    </span>

为了确保代码的易读性，本手册还介绍了一些<a href="/language/pseudo-types.html" class="link">伪类型</a>：

-   <span class="simpara"> <span class="type">mixed</span>（混合类型）
    </span>
-   <span class="simpara"> <span class="type">number</span>（数字类型）
    </span>
-   <span class="simpara"> <span
    class="type">callback</span>（回调类型，又称为 <span
    class="type">callable</span>） </span>
-   <span class="simpara"> <span class="type">array\|object</span>（数组
    \| 对象类型） </span>
-   <span class="simpara"> <span class="type">void</span> （无类型）
    </span>

以及伪变量 `$...`。

可能还会读到一些关于“双精度（double）”类型的参考。实际上 double 和 float
是相同的，由于一些历史的原因，这两个名称同时存在。

变量的类型通常不是由程序员设定的，确切地说，是由 PHP
根据该变量使用的上下文在运行时决定的。

> **Note**: <span class="simpara">
> 如果想查看某个<a href="/language/expressions.html" class="link">表达式</a>的值和类型，用
> <span class="function">var\_dump</span> 函数。 </span>
>
> 如果只是想得到一个易读懂的类型的表达方式用于调试，用 <span
> class="function">gettype</span> 函数。要检验某个类型，*不要*用 <span
> class="function">gettype</span>，而用 *is\_<span
> class="replaceable">type</span>* 函数。以下是一些范例：
>
> ``` php
> <?php
> $a_bool = TRUE;   // 布尔值 boolean
> $a_str  = "foo";  // 字符串 string
> $a_str2 = 'foo';  // 字符串 string
> $an_int = 12;     // 整型 integer
>
> echo gettype($a_bool); // 输出:  boolean
> echo gettype($a_str);  // 输出:  string
>
> // 如果是整型，就加上 4
> if (is_int($an_int)) {
>     $an_int += 4;
> }
>
> // 如果 $bool 是字符串，就打印出来
> // (啥也没打印出来)
> if (is_string($a_bool)) {
>     echo "String: $a_bool";
> }
> ?>
> ```

如果要将一个变量强制转换为某类型，可以对其使用<a href="/language/types/type-juggling.html#language.types.typecasting" class="link">强制转换</a>或者
<span class="function">settype</span> 函数。

注意变量根据其当时的类型在特定场合下会表现出不同的值。更多信息见<a href="/language/types/type-juggling.html" class="link">类型转换的判别</a>。此外，还可以参考
<a href="/types/comparisons.html" class="link">PHP 类型比较表</a>看不同类型相互比较的例子。
