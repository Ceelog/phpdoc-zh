基础
----

PHP 中的变量用一个美元符号后面跟变量名来表示。变量名是区分大小写的。

变量名与 PHP
中其它的标签一样遵循相同的规则。一个有效的变量名由字母或者下划线开头，后面跟上任意数量的字母，数字，或者下划线。按照正常的正则表达式，它将被表述为：'*\[a-zA-Z\_\\x7f-\\xff\]\[a-zA-Z0-9\_\\x7f-\\xff\]\**'。

> **Note**: <span class="simpara"> 在此所说的字母是 a-z，A-Z，以及 ASCII
> 字符从 127 到 255（*0x7f-0xff*）。 </span>

> **Note**: <span class="simpara"> *$this*
> 是一个特殊的变量，它不能被赋值。 </span>

**小贴士**

请参见<a href="/userlandnaming.html" class="xref">用户空间命名指南</a>。

有关变量的函数信息见<a href="/ref/var.html" class="link">变量函数</a>。

``` php
<?php
$var = 'Bob';
$Var = 'Joe';
echo "$var, $Var";      // 输出 "Bob, Joe"

$4site = 'not yet';     // 非法变量名；以数字开头
$_4site = 'not yet';    // 合法变量名；以下划线开头
$i站点is = 'mansikka';  // 合法变量名；可以用中文
?>
```

变量默认总是传值赋值。那也就是说，当将一个表达式的值赋予一个变量时，整个原始表达式的值被赋值到目标变量。这意味着，例如，当一个变量的值赋予另外一个变量时，改变其中一个变量的值，将不会影响到另外一个变量。有关这种类型的赋值操作，请参阅<a href="/language/expressions.html" class="link">表达式</a>一章。

PHP
也提供了另外一种方式给变量赋值：<a href="/language/references.html" class="link">引用赋值</a>。这意味着新的变量简单的引用（换言之，“成为其别名”
或者 “指向”）了原始变量。改动新的变量将影响到原始变量，反之亦然。

使用引用赋值，简单地将一个 &
符号加到将要赋值的变量前（源变量）。例如，下列代码片断将输出“My name is
Bob”两次：

``` php
<?php
$foo = 'Bob';              // 将 'Bob' 赋给 $foo
$bar = &$foo;              // 通过 $bar 引用 $foo
$bar = "My name is $bar";  // 修改 $bar 变量
echo $bar;
echo $foo;                 // $foo 的值也被修改
?>
```

有一点重要事项必须指出，那就是只有有名字的变量才可以引用赋值。

``` php
<?php
$foo = 25;
$bar = &$foo;      // 合法的赋值
$bar = &(24 * 7);  // 非法; 引用没有名字的表达式

function test()
{
   return 25;
}

$bar = &test();    // 非法
?>
```

虽然在 PHP
中并不需要初始化变量，但对变量进行初始化是个好习惯。未初始化的变量具有其类型的默认值
- 布尔类型的变量默认值是
**`false`**，整形和浮点型变量默认值是零，字符串型变量（例如用于 <span
class="function">echo</span>
中）默认值是空字符串以及数组变量的默认值是空数组。

**示例 \#1 未初始化变量的默认值**

``` php
<?php
// Unset AND unreferenced (no use context) variable; outputs NULL
var_dump($unset_var);

// Boolean usage; outputs 'false' (See ternary operators for more on this syntax)
echo($unset_bool ? "true\n" : "false\n");

// String usage; outputs 'string(3) "abc"'
$unset_str .= 'abc';
var_dump($unset_str);

// Integer usage; outputs 'int(25)'
$unset_int += 25; // 0 + 25 => 25
var_dump($unset_int);

// Float/double usage; outputs 'float(1.25)'
$unset_float += 1.25;
var_dump($unset_float);

// Array usage; outputs array(1) {  [3]=>  string(3) "def" }
$unset_arr[3] = "def"; // array() + array(3 => "def") => array(3 => "def")
var_dump($unset_arr);

// Object usage; creates new stdClass object (see http://www.php.net/manual/en/reserved.classes.php)
// Outputs: object(stdClass)#1 (1) {  ["foo"]=>  string(3) "bar" }
$unset_obj->foo = 'bar';
var_dump($unset_obj);
?>
```

依赖未初始化变量的默认值在某些情况下会有问题，例如把一个文件包含到另一个之中时碰上相同的变量名。另外把
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
打开是一个主要的<a href="/security/globals.html" class="link">安全隐患</a>。使用未初始化的变量会发出
<a href="" class="link">E_NOTICE</a>
错误，但是在向一个未初始化的数组附加单元时不会。<span
class="function">isset</span>
语言结构可以用来检测一个变量是否已被初始化。
