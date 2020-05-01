新的特性
--------

### 新增 <a href="/language/generators.html" class="link">Generators</a>

Support for
<a href="/language/generators.html" class="link">generators</a> has been
added via the **yield** keyword. Generators provide an easy way to
implement simple iterators without the overhead or complexity of
implementing a class that implements the <span
class="classname">Iterator</span> interface.

A simple example that reimplements the <span
class="function">range</span> function as a generator (at least for
positive *step* values):

``` php
<?php
function xrange($start, $limit, $step = 1) {
    for ($i = $start; $i <= $limit; $i += $step) {
        yield $i;
    }
}

echo 'Single digit odd numbers: ';

/* 注意保存在内存中的数组绝不会被创建或返回 */ 
foreach (xrange(1, 9, 2) as $number) {
    echo "$number ";
}
?>
```

以上例程会输出：

    Single digit odd numbers: 1 3 5 7 9 

### 新增 <a href="/language/exceptions.html" class="link"><em>finally</em></a> 关键字

*try*-*catch* blocks now support a
<a href="/language/exceptions.html" class="link"><em>finally</em></a>
block for code that should be run regardless of whether an exception has
been thrown or not.

### <a href="/control-structures/foreach.html" class="link"><em>foreach</em></a> 现在支持 <span class="function">list</span>

<a href="/control-structures/foreach.html" class="link">foreach</a>
控制结构现在支持通过 <span class="function">list</span>
构造将嵌套数组分离到单独的变量。例如：

``` php
<?php
$array = [
    [1, 2],
    [3, 4],
];

foreach ($array as list($a, $b)) {
    echo "A: $a; B: $b\n";
}
?>
```

以上例程会输出：

    A: 1; B: 2
    A: 3; B: 4

关于
<a href="/control-structures/foreach.html#control-structures.foreach.list" class="link">foreach</a>
更深入的文档可参考相关手册页面。

### <span class="function">empty</span> 支持任意表达式

<span class="function">empty</span>
现在支持传入一个任意表达式，而不仅是一个变量。例如：

``` php
<?php
function always_false() {
    return false;
}

if (empty(always_false())) {
    echo 'This will be printed.';
}

if (empty(true)) {
    echo 'This will not be printed.';
}
?>
```

以上例程会输出：

    This will be printed.

### <span class="type">array</span> and <span class="type">string</span> literal dereferencing

<span class="type">Array</span> and <span class="type">string</span>
literals can now be dereferenced directly to access individual elements
and characters:

``` php
<?php
echo 'Array dereferencing: ';
echo [1, 2, 3][0];
echo "\n";

echo 'String dereferencing: ';
echo 'PHP'[0];
echo "\n";
?>
```

以上例程会输出：

    Array dereferencing: 1
    String dereferencing: P

### 新的密码哈希 API

A <a href="/book/password.html" class="link">新的密码哈希 API</a> that
makes it easier to securely hash and manage passwords using the same
underlying library as <span class="function">crypt</span> in PHP has
been added. See the documentation for <span
class="function">password\_hash</span> for more detail.

### Apache 2.4 handler supported on Windows

The Apache 2.4 handler SAPI is now supported on Windows.

### 改进 GD

对 GD 扩展做了多方面的改进，包括：

-   <span class="simpara"> 翻转支持使用新的 <span
    class="function">imageflip</span> 函数。 </span>
-   <span class="simpara"> 高级裁剪支持使用 <span
    class="function">imagecrop</span> & <span
    class="function">imagecropauto</span> 函数。 </span>
-   <span class="simpara"> WebP 的读写分别支持使用 <span
    class="function">imagecreatefromwebp</span> & <span
    class="function">imagewebp</span> 。 </span>
