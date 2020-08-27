不向后兼容的变更
----------------

### 错误和异常处理相关的变更

在 PHP 7 中，很多致命错误以及可恢复的致命错误，都被转换为异常来处理了。
这些异常继承自 <span class="classname">Error</span> 类，此类实现了 <span
class="classname">Throwable</span> 接口
（所有异常都实现了这个基础接口）。

这也意味着，当发生错误的时候，以前代码中的一些错误处理的代码将无法被触发。
因为在 PHP 7 版本中，已经使用抛出异常的错误处理机制了。
（如果代码中没有捕获 <span class="classname">Error</span>
异常，那么会引发致命错误）。

PHP 7 中的错误处理的更完整的描述，请参见
<a href="/language/errors/php7.html" class="link">PHP 7 错误处理</a>。
本迁移指导主要是列出对兼容性有影响的变更。

#### <span class="function">set\_exception\_handler</span> 不再保证收到的一定是 <span class="classname">Exception</span> 对象

抛出 <span class="classname">Error</span> 对象时，如果 <span
class="function">set\_exception\_handler</span>
里的异常处理代码声明了类型 <span class="classname">Exception</span>
，将会导致 fatal error。

想要异常处理器同时支持 PHP5 和
PHP7，应该删掉异常处理器里的类型声明。如果代码仅仅是升级到
PHP7，则可以把类型 <span class="classname">Exception</span> 替换成 <span
class="classname">Throwable</span>。

``` php
<?php
// PHP 5 时代的代码将会出现问题
function handler(Exception $e) { ... }
set_exception_handler('handler');

// 兼容 PHP 5 和 7
function handler($e) { ... }

// 仅支持 PHP 7
function handler(Throwable $e) { ... }
?>
```

#### 当内部构造器失败的时候，总是抛出异常

在之前版本中，如果内部类的构造器出错，会返回 **`NULL`**
或者一个不可用的对象。 从 PHP 7 开始，如果内部类构造器发生错误，
那么会抛出异常。

#### 解析错误会抛出 <span class="classname">ParseError</span> 异常

解析错误会抛出 <span class="classname">ParseError</span> 异常。 对于
<span class="function">eval</span> 函数，需要将其包含到一个
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
代码块中来处理解析错误。

#### E\_STRICT 警告级别变更

原有的 **`E_STRICT`** 警告都被迁移到其他级别。 **`E_STRICT`**
常量会被保留，所以调用 *error\_reporting(E\_ALL\|E\_STRICT)*
不会引发错误。

| 场景                                     | 新的级别/行为        |
|------------------------------------------|----------------------|
| 将资源类型的变量用作键来进行索引         | **`E_NOTICE`**       |
| 抽象静态方法                             | 不再警告，会引发错误 |
| 重复定义构造器函数                       | 不再警告，会引发错误 |
| 在继承的时候，方法签名不匹配             | **`E_WARNING`**      |
| 在两个 trait 中包含相同的（兼容的）属性  | 不再警告，会引发错误 |
| 以非静态调用的方式访问静态属性           | **`E_NOTICE`**       |
| 变量应该以引用的方式赋值                 | **`E_NOTICE`**       |
| 变量应该以引用的方式传递（到函数参数中） | **`E_NOTICE`**       |
| 以静态方式调用实例方法                   | **`E_DEPRECATED`**   |

### 关于变量处理的变化

PHP 7
现在使用了抽象语法树来解析源代码。这使得许多由于之前的PHP的解释器的限制所不可能实现的改进得以实现。
但出于一致性的原因导致了一些特殊例子的变动，而这些变动打破了向后兼容。
在这一章中将详细介绍这些例子。

#### 关于间接使用变量、属性和方法的变化

对变量、属性和方法的间接调用现在将严格遵循从左到右的顺序来解析，而不是之前的混杂着几个特殊案例的情况。
下面这张表说明了这个解析顺序的变化。

| 表达式                | PHP 5 的解析方式        | PHP 7 的解析方式        |
|-----------------------|-------------------------|-------------------------|
| `$$foo['bar']['baz']` | `${$foo['bar']['baz']}` | `($$foo)['bar']['baz']` |
| `$foo->$bar['baz']`   | `$foo->{$bar['baz']}`   | `($foo->$bar)['baz']`   |
| `$foo->$bar['baz']()` | `$foo->{$bar['baz']}()` | `($foo->$bar)['baz']()` |
| `Foo::$bar['baz']()`  | `Foo::{$bar['baz']}()`  | `(Foo::$bar)['baz']()`  |

使用了旧的从右到左的解析顺序的代码必须被重写，明确的使用大括号来表明顺序（参见上表中间一列）。
这样使得代码既保持了与PHP 7.x的前向兼容性，又保持了与PHP
5.x的后向兼容性。

这同样影响了
<a href="/language/variables/scope.html#language.variables.scope.global" class="link"><em>global</em></a>
关键字。如果需要的话可以使用大括号来模拟之前的行为。

``` php
<?php
function f() {
    // Valid in PHP 5 only.
    global $$foo->bar;

    // Valid in PHP 5 and 7.
    global ${$foo->bar};
}
?>
```

#### 关于<span class="function">list</span>处理方式的变更

##### <span class="function">list</span> 不再以反向的顺序来进行赋值

<span class="function">list</span>
现在会按照变量定义的顺序来给他们进行赋值，而非反过来的顺序。
通常来说，这只会影响<span class="function">list</span>
与数组的`[]`操作符一起使用的案例，如下所示：

``` php
<?php
list($a[], $a[], $a[]) = [1, 2, 3];
var_dump($a);
?>
```

以上例程在 PHP 5 中的输出：

    array(3) {
      [0]=>
      int(3)
      [1]=>
      int(2)
      [2]=>
      int(1)
    }

以上例程在 PHP 7 中的输出：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

总之，我们推荐不要依赖<span
class="function">list</span>的赋值顺序，因为这是一个在未来也许会变更的实现细节。

##### 空的<span class="function">list</span>赋值支持已经被移除

<span class="function">list</span>
结构现在不再能是空的。如下的例子不再被允许：

``` php
<?php
list() = $a;
list(,,) = $a;
list($x, list(), $y) = $a;
?>
```

##### <span class="function">list</span>不再能解开<span class="type">string</span>

<span class="function">list</span> 不再能解开字符串（<span
class="type">string</span>）变量。 你可以使用<span
class="function">str\_split</span>来代替它。

#### Array ordering when elements are automatically created during by reference assignments has changed

The order of the elements in an array has changed when those elements
have been automatically created by referencing them in a by reference
assignment. For example:

``` php
<?php
$array = [];
$array["a"] =& $array["b"];
$array["b"] = 1;
var_dump($array);
?>
```

以上例程在 PHP 5 中的输出：

    array(2) {
      ["b"]=>
      &int(1)
      ["a"]=>
      &int(1)
    }

以上例程在 PHP 7 中的输出：

    array(2) {
      ["a"]=>
      &int(1)
      ["b"]=>
      &int(1)
    }

#### 函数参数附近的括号不再影响行为

在 PHP 5中，在以引用方式传递函数参数时，使用冗余的括号对可以隐匿严格标准
的警告。现在，这个警告总会触发。

``` php
<?php
function getArray() {
    return [1, 2, 3];
}

function squareArray(array &$a) {
    foreach ($a as &$v) {
        $v **= 2;
    }
}

// Generates a warning in PHP 7.
squareArray((getArray()));
?>
```

以上例程会输出：

    Notice: Only variables should be passed by reference in /tmp/test.php on line 13

### <a href="/control-structures/foreach.html" class="link">foreach</a>的变化

<a href="/control-structures/foreach.html" class="link">foreach</a>发生了细微的变化，控制结构，
主要围绕阵列的内部数组指针和迭代处理的修改。

#### <a href="/control-structures/foreach.html" class="link">foreach</a>不再改变内部数组指针

在PHP7之前，当数组通过
<a href="/control-structures/foreach.html" class="link">foreach</a>
迭代时，数组指针会移动。现在开始，不再如此，见下面代码

``` php
<?php
$array = [0, 1, 2];
foreach ($array as &$val) {
    var_dump(current($array));
}
?>
```

以上例程在 PHP 5 中的输出：

    int(1)
    int(2)
    bool(false)

以上例程在 PHP 7 中的输出：

    int(0)
    int(0)
    int(0)

#### <a href="/control-structures/foreach.html" class="link">foreach</a> 通过值遍历时，操作的值为数组的副本

当默认使用通过值遍历数组时，<a href="/control-structures/foreach.html" class="link">foreach</a>
实际操作的是数组的迭代副本，而非数组本身。这就意味着，foreach
中的操作不会修改原数组的值。

#### <a href="/control-structures/foreach.html" class="link">foreach</a>通过引用遍历时，有更好的迭代特性

当使用引用遍历数组时，现在
<a href="/control-structures/foreach.html" class="link">foreach</a>
在迭代中能更好的跟踪变化。例如，在迭代中添加一个迭代值到数组中，参考下面的代码：

``` php
<?php
$array = [0];
foreach ($array as &$val) {
    var_dump($val);
    $array[1] = 1;
}
?>
```

以上例程在 PHP 5 中的输出：

    int(0)

以上例程在 PHP 7 中的输出：

    int(0)
    int(1)

#### 非<span class="classname">Traversable</span> 对象的遍历

迭代一个非<span
class="classname">Traversable</span>对象将会与迭代一个引用数组的行为相同。
这将导致在对象添加或删除属性时，<a href="/migration70/incompatible.html#migration70.incompatible.foreach.by-ref" class="link"></a><a href="/control-structures/foreach.html" class="link">foreach</a>通过引用遍历时，有更好的迭代特性也能被应用

### Changes to <span class="type">integer</span> handling

#### 无效的八进制字符（Invalid octal literals）

在之前，一个八进制字符如果含有无效数字，该无效数字将被静默删节(*0128*
将被解析为 *012*). 现在这样的八进制字符将产生解析错误。

#### 负位移运算（Negative bitshifts）

以负数形式进行的位移运算将会抛出一个 <span
class="classname">ArithmeticError</span>：

``` php
<?php
var_dump(1 >> -1);
?>
```

以上例程在 PHP 5 中的输出：

    int(0)

以上例程在 PHP 7 中的输出：

    Fatal error: Uncaught ArithmeticError: Bit shift by negative number in /tmp/test.php:2
    Stack trace:
    #0 {main}
      thrown in /tmp/test.php on line 2

#### 超范围后产生位移

超出 <span class="type">integer</span>
位宽的位移操作（无论哪个方向）将始终得到 0
作为结果。在从前，这一操作是结构依赖的。

### <span class="type">string</span>处理上的调整

#### 十六进制字符串不再被认为是数字

含十六进制字符串不再被认为是数字。例如：

``` php
<?php
var_dump("0x123" == "291");
var_dump(is_numeric("0x123"));
var_dump("0xe" + "0x1");
var_dump(substr("foo", "0x1"));
?>
```

以上例程在 PHP 5 中的输出：

    bool(true)
    bool(true)
    int(15)
    string(2) "oo"

以上例程在 PHP 7 中的输出：

    bool(false)
    bool(false)
    int(0)

    Notice: A non well formed numeric value encountered in /tmp/test.php on line 5
    string(3) "foo"

<span class="function">filter\_var</span> 函数可以用于检查一个 <span
class="type">string</span> 是否含有十六进制数字,并将其转换为<span
class="type">integer</span>:

``` php
<?php
$str = "0xffff";
$int = filter_var($str, FILTER_VALIDATE_INT, FILTER_FLAG_ALLOW_HEX);
if (false === $int) {
    throw new Exception("Invalid integer!");
}
var_dump($int); // int(65535)
?>
```

#### *\\u{* 可能引起错误

由于新的
<a href="/migration70/new-features.html#migration70.new-features.unicode-codepoint-escape-syntax" class="link">Unicode codepoint escape syntax</a>语法，
紧连着无效序列并包含*\\u{* 的字串可能引起致命错误。
为了避免这一报错，应该避免反斜杠开头。

### 被移除的函数（Removed functions）

#### <span class="function">call\_user\_method</span> and <span class="function">call\_user\_method\_array</span>

这两个函数从PHP 4.1.0开始被废弃，应该使用<span
class="function">call\_user\_func</span> 和 <span
class="function">call\_user\_func\_array</span>。 你也可以考虑使用
<a href="/functions/variable-functions.html" class="link">变量函数</a>
或者
<a href="/functions/arguments.html#functions.variable-arg-list.new" class="link"><em>...</em></a>
操作符。

#### 所有的 ereg\* 函数

所有 <a href="/book/regex.html" class="link">ereg</a> 系列函数被删掉了。
<a href="/book/pcre.html" class="link">PCRE</a> 作为推荐的替代品。

#### <a href="/book/mcrypt.html" class="link">mcrypt</a> 别名

已废弃的 <span class="function">mcrypt\_generic\_end</span>
函数已被移除，请使用<span
class="function">mcrypt\_generic\_deinit</span>代替。

此外，已废弃的 <span class="function">mcrypt\_ecb</span>, <span
class="function">mcrypt\_cbc</span>, <span
class="function">mcrypt\_cfb</span> 和 <span
class="function">mcrypt\_ofb</span>
函数已被移除，请配合恰当的**`MCRYPT_MODE_*`** 常量来使用 <span
class="function">mcrypt\_decrypt</span>进行代替。

#### 所有 ext/mysql 函数

所有
<a href="/set/mysqlinfo.html#Mysql（原始）" class="link">ext/mysql</a>
函数已被删掉了。 如何选择不同的 MySQL API，详情请见
<a href="/set/mysqlinfo.html#Choosing%20an%20API" class="link">选择 MySQL API</a>。

#### 所有 ext/mssql 函数

所有 <a href="/book/mssql.html" class="link">ext/mssql</a>
函数已被删掉了。 替代品的列表，参见
<a href="/book/mssql.html#简介" class="link">MSSQL 介绍</a>。

#### <a href="/book/intl.html" class="link">intl</a> 别名

已废弃的 <span class="function">datefmt\_set\_timezone\_id</span> 和
<span class="methodname">IntlDateFormatter::setTimeZoneID</span>
函数已被移除，请使用 <span
class="function">datefmt\_set\_timezone</span> 与 <span
class="methodname">IntlDateFormatter::setTimeZone</span>代替。

#### <span class="function">set\_magic\_quotes\_runtime</span>

<span class="function">set\_magic\_quotes\_runtime</span>, 和它的别名
<span class="function">magic\_quotes\_runtime</span>已被移除. 它们在PHP
5.3.0中已经被废弃,并且
在<a href="/migration54/incompatible.html" class="link">in PHP 5.4.0</a>也由于魔术引号的废弃而失去功能。

#### <span class="function">set\_socket\_blocking</span>

已废弃的 <span class="function">set\_socket\_blocking</span>
函数已被移除，请使用<span
class="function">stream\_set\_blocking</span>代替。

#### <span class="function">dl</span> in PHP-FPM

<span class="function">dl</span>在 PHP-FPM 不再可用，在 CLI 和 embed
SAPIs 中仍可用。

#### <a href="/book/image.html" class="link">GD</a> Type1 functions

Support for PostScript Type1 fonts has been removed from the GD
extension, resulting in the removal of the following functions:

-   <span class="simpara"> <span class="function">imagepsbbox</span>
    </span>
-   <span class="simpara"> <span
    class="function">imagepsencodefont</span> </span>
-   <span class="simpara"> <span
    class="function">imagepsextendfont</span> </span>
-   <span class="simpara"> <span class="function">imagepsfreefont</span>
    </span>
-   <span class="simpara"> <span class="function">imagepsloadfont</span>
    </span>
-   <span class="simpara"> <span
    class="function">imagepsslantfont</span> </span>
-   <span class="simpara"> <span class="function">imagepstext</span>
    </span>

推荐使用 TrueType 字体和相关的函数作为替代。

### 被移除掉的 INI 配置指令

#### 被移除的功能

以下 INI 配置指令已经被移除，同时移除的还有其对应的功能

-   <span class="simpara">
    <a href="/ini/core.html#ini.always-populate-raw-post-data" class="link"><code class="parameter">always_populate_raw_post_data</code></a>
    </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.asp-tags" class="link"><code class="parameter">asp_tags</code></a>
    </span>

#### `xsl.security_prefs`

`xsl.security_prefs` 指令被移除 在预处理的时候，取而代之的方法 <span
class="methodname">XsltProcessor::setSecurityPrefs</span> 应该被调用到

### 其他向后兼容相关的变更

#### new 操作符创建的对象不能以引用方式赋值给变量

<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link"><em>new</em></a>
语句创建的对象不能 以引用的方式赋值给变量。

``` php
<?php
class C {}
$c =& new C;
?>
```

以上例程在 PHP 5 中的输出：

    Deprecated: Assigning the return value of new by reference is deprecated in /tmp/test.php on line 3

以上例程在 PHP 7 中的输出：

    Parse error: syntax error, unexpected 'new' (T_NEW) in /tmp/test.php on line 3

#### 无效的类、接口以及 trait 命名

不能以下列名字来命名类、接口以及 trait：

-   <span class="simpara"><span class="type">bool</span></span>
-   <span class="simpara"><span class="type">int</span></span>
-   <span class="simpara"><span class="type">float</span></span>
-   <span class="simpara"><span class="type">string</span></span>
-   <span class="simpara">**`NULL`**</span>
-   <span class="simpara">**`TRUE`**</span>
-   <span class="simpara">**`FALSE`**</span>

此外，也不要使用下列的名字来命名类、接口以及 trait。虽然在 PHP 7.0 中，
这并不会引发错误， 但是这些名字是保留给将来使用的。

-   <span class="simpara"><span class="type">resource</span></span>
-   <span class="simpara"><span class="type">object</span></span>
-   <span class="simpara"><span class="type">mixed</span></span>
-   <span class="simpara"><span class="type">numeric</span></span>

#### 移除了 ASP 和 script PHP 标签

使用类似 ASP 的标签，以及 script 标签来区分 PHP 代码的方式被移除。
受到影响的标签有：

| 开标签                    | 闭标签      |
|---------------------------|-------------|
| `<%`                      | `%>`        |
| `<%=`                     | `%>`        |
| `<script language="php">` | `</script>` |

#### 从不匹配的上下文发起调用

在不匹配的上下文中以静态方式调用非静态方法，
<a href="/migration56/deprecated.html#migration56.deprecated.incompatible-context" class="link">在 PHP 5.6 中已经废弃</a>，
但是在 PHP 7.0 中， 会导致被调用方法中未定义 *$this*
变量，以及此行为已经废弃的警告。

``` php
<?php
class A {
    public function test() { var_dump($this); }
}

// 注意：并没有从类 A 继承
class B {
    public function callNonStaticMethodOfA() { A::test(); }
}

(new B)->callNonStaticMethodOfA();
?>
```

以上例程在 PHP 5.6 中的输出：

    Deprecated: Non-static method A::test() should not be called statically, assuming $this from incompatible context in /tmp/test.php on line 8
    object(B)#1 (0) {
    }

以上例程在 PHP 7 中的输出：

    Deprecated: Non-static method A::test() should not be called statically in /tmp/test.php on line 8

    Notice: Undefined variable: this in /tmp/test.php on line 3
    NULL

#### <a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a> 变更为右联接运算符

在使用
<a href="/language/generators/syntax.html#control-structures.yield" class="link">yield</a>
关键字的时候，不再需要括号，
并且它变更为右联接操作符，其运算符优先级介于 *print* 和 *=\>* 之间。
这可能导致现有代码的行为发生改变：

``` php
<?php
echo yield -1;
// 在之前版本中会被解释为：
echo (yield) - 1;
// 现在，它将被解释为：
echo yield (-1);

yield $foo or die;
// 在之前版本中会被解释为：
yield ($foo or die);
// 现在，它将被解释为：
(yield $foo) or die;
?>
```

可以通过使用括号来消除歧义。

#### 函数定义不可以包含多个同名参数

在函数定义中，不可以包含两个或多个同名的参数。
例如，下面代码中的函数定义会触发 **`E_COMPILE_ERROR`** 错误：

``` php
<?php
function foo($a, $b, $unused, $unused) {
    //
}
?>
```

#### Switch 语句不可以包含多个 default 块

在 switch 语句中，两个或者多个 default 块的代码已经不再被支持。
例如，下面代码中的 switch 语句会触发 **`E_COMPILE_ERROR`** 错误：

``` php
<?php
switch (1) {
    default:
    break;
    default:
    break;
}
?>
```

#### 在函数中检视参数值会返回 *当前* 的值

当在函数代码中使用 <span class="function">func\_get\_arg</span> 或 <span
class="function">func\_get\_args</span> 函数来检视参数值， 或者使用
<span class="function">debug\_backtrace</span> 函数查看回溯跟踪，
以及在异常回溯中所报告的参数值是指参数当前的值（有可能是已经被函数内的代码改变过的值），
而不再是参数被传入函数时候的原始值了。

``` php
<?php
function foo($x) {
    $x++;
    var_dump(func_get_arg(0));
}
foo(1);?>
```

以上例程在 PHP 5 中的输出：

    1

以上例程在 PHP 7 中的输出：

    2

#### `$HTTP_RAW_POST_DATA` 被移除

不再提供 `$HTTP_RAW_POST_DATA` 变量。 请使用
<a href="/wrappers/php.html#wrappers.php.input" class="link"><em>php://input</em></a>
作为替代。

#### INI 文件中 *\#* 注释格式被移除

在 INI 文件中，不再支持以 *\#* 开始的注释行， 请使用
*;*（分号）来表示注释。 此变更适用于 `php.ini` 以及用 <span
class="function">parse\_ini\_file</span> 和 <span
class="function">parse\_ini\_string</span> 函数来处理的文件。

#### JSON 扩展已经被 JSOND 取代

JSON 扩展已经被 JSOND 扩展取代。 对于数值的处理，有以下两点需要注意的：
第一，数值不能以点号（.）结束 （例如，数值 *34.* 必须写作 *34.0* 或
*34*）。 第二，如果使用科学计数法表示数值，*e* 前面必须不是点号（.）
（例如，*3.e3* 必须写作 *3.0e3* 或 *3e3*）。
另外，空字符串不再被视作有效的 JSON 字符串。

#### 在数值溢出的时候，内部函数将会失败

将浮点数转换为整数的时候，如果浮点数值太大，导致无法以整数表达的情况下，
在之前的版本中，内部函数会直接将整数截断，并不会引发错误。 在 PHP 7.0
中，如果发生这种情况，会引发 E\_WARNING 错误，并且返回 **`NULL`**。

#### 自定义会话处理器的返回值修复

在自定义会话处理器中，如果函数的返回值不是 **`FALSE`**，也不是 *-1*，
会引发致命错误。现在，如果这些函数的返回值不是布尔值，也不是 *-1* 或者
*0*，函数调用结果将被视为失败，并且引发 E\_WARNING 错误。

#### 相等的元素在排序时的顺序问题

由于内部排序算法进行了提升，
可能会导致对比时被视为相等的多个元素之间的顺序不稳定。

> **Note**:
>
> 在对比时被视为相等的多个元素之间的排序顺序是不可信赖的，即使是相等的两个元素，
> 他们的位置也可能被排序算法所改变。

#### 错误的使用 break 和 switch 语句

在循环或者 *switch* 语句之外使用 *break* 和 *continue*
被视为编译型错误（之前视为运行时错误），会引发 **`E_COMPILE_ERROR`**
错误。

#### Mhash 不再是一个单独的扩展了

Mhash 扩展已经被完全整合进
<a href="/book/hash.html" class="link">Hash</a> 扩展了。
因此，不要再使用 <span class="function">extension\_loaded</span>
函数来检测是否支持 MHash 扩展了， 建议使用 <span
class="function">function\_exists</span> 函数来进行检测。 另外，函数
<span class="function">get\_loaded\_extensions</span>
以及相关的特性中，也不再报告 和 MHash 扩展相关的信息了。

#### declare(ticks)

<a href="/control-structures/declare.html#control-structures.declare.ticks" class="link">declare(ticks)</a>
指示符不再泄漏到不同的编译单元中。
