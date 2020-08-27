Boolean 布尔类型
----------------

这是最简单的类型。<span class="type">boolean</span> 表达了真值，可以为
**`TRUE`** 或 **`FALSE`**。

### 语法

要指定一个布尔值，使用常量 **`TRUE`** 或
**`FALSE`**。两个都不区分大小写。

``` php
<?php
$foo = True; // 设置 $foo 为 TRUE
?>
```

通常<a href="/language/operators.html" class="link">运算符</a>所返回的
<span class="type">boolean</span>
值结果会被传递给<a href="/language/control-structures.html" class="link">控制流程</a>。

``` php
<?php
// == 是一个操作符，它检测两个变量是否相等，并返回一个布尔值
if ($action == "show_version") {
    echo "The version is 1.23";
}

// 这样做是不必要的...
if ($show_separators == TRUE) {
    echo "<hr>\n";
}

// ...因为可以使用下面这种简单的方式：
if ($show_separators) {
    echo "<hr>\n";
}
?>
```

### 转换为布尔值

要明确地将一个值转换成 <span class="type">boolean</span>，用 *(bool)*
或者 *(boolean)*
来强制转换。但是很多情况下不需要用强制转换，因为当运算符，函数或者流程控制结构需要一个
<span class="type">boolean</span> 参数时，该值会被自动转换。

参见<a href="/language/types/type-juggling.html" class="link">类型转换的判别</a>。

当转换为 <span class="type">boolean</span> 时，以下值被认为是
**`FALSE`**：

-   <span class="simpara">
    <a href="/language/types/boolean.html" class="link">布尔</a>值
    **`FALSE`** 本身 </span>
-   <span class="simpara">
    <a href="/language/types/integer.html" class="link">整型</a>值
    0（零）及 -0 (零) </span>
-   <span class="simpara">
    <a href="/language/types/float.html" class="link">浮点型</a>值
    0.0（零）-0.0(零) </span>
-   <span class="simpara">
    空<a href="/language/types/string.html" class="link">字符串</a>，以及<a href="/language/types/string.html" class="link">字符串</a>
    "0" </span>
-   <span class="simpara">
    不包括任何元素的<a href="/language/types/array.html" class="link">数组</a>
    </span>
-   <span class="simpara"> 特殊类型
    <a href="/language/types/null.html" class="link">NULL</a>（包括尚未赋值的变量）
    </span>
-   <span class="simpara"> 从空标记生成的
    <a href="/ref/simplexml.html" class="link">SimpleXML</a> 对象
    </span>

所有其它值都被认为是
**`TRUE`**（包括任何<a href="/language/types/resource.html" class="link">资源</a>
和 **`NAN`**）。

**Warning**

*-1* 和其它非零值（不论正负）一样，被认为是 **`TRUE`**！

``` php
<?php
var_dump((bool) "");        // bool(false)
var_dump((bool) 1);         // bool(true)
var_dump((bool) -2);        // bool(true)
var_dump((bool) "foo");     // bool(true)
var_dump((bool) 2.3e5);     // bool(true)
var_dump((bool) array(12)); // bool(true)
var_dump((bool) array());   // bool(false)
var_dump((bool) "false");   // bool(true)
?>
```
