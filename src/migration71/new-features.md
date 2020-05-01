新特性
------

### 可为空（Nullable）类型

参数以及返回值的类型现在可以通过在类型前加上一个问号使之允许为空。
当启用这个特性时，传入的参数或者函数返回的结果要么是给定的类型，要么是
<span class="type">null</span> 。

``` php
<?php

function testReturn(): ?string
{
    return 'elePHPant';
}

var_dump(testReturn());

function testReturn(): ?string
{
    return null;
}

var_dump(testReturn());

function test(?string $name)
{
    var_dump($name);
}

test('elePHPant');
test(null);
test();
```

以上例程会输出：

    string(10) "elePHPant"
    NULL
    string(10) "elePHPant"
    NULL
    Uncaught Error: Too few arguments to function test(), 0 passed in...

### Void 函数

一个新的返回值类型<span class="type">void</span>被引入。 返回值声明为
void 类型的方法要么干脆省去 return 语句，要么使用一个空的 return 语句。
对于 void 函数来说，**`NULL`** 不是一个合法的返回值。

``` php
<?php
function swap(&$left, &$right) : void
{
    if ($left === $right) {
        return;
    }

    $tmp = $left;
    $left = $right;
    $right = $tmp;
}

$a = 1;
$b = 2;
var_dump(swap($a, $b), $a, $b);
```

以上例程会输出：

    null
    int(2)
    int(1)

试图去获取一个 void 方法的返回值会得到 **`NULL`**
，并且不会产生任何警告。这么做的原因是不想影响更高层次的方法。

### Symmetric array destructuring

短数组语法（*\[\]*）现在作为<span
class="function">list</span>语法的一个备选项，可以用于将数组的值赋给一些变量（包括在*foreach*中）。

``` php
<?php
$data = [
    [1, 'Tom'],
    [2, 'Fred'],
];

// list() style
list($id1, $name1) = $data[0];

// [] style
[$id1, $name1] = $data[0];

// list() style
foreach ($data as list($id, $name)) {
    // logic here with $id and $name
}

// [] style
foreach ($data as [$id, $name]) {
    // logic here with $id and $name
}
```

### 类常量可见性

现在起支持设置类常量的可见性。

``` php
<?php
class ConstDemo
{
    const PUBLIC_CONST_A = 1;
    public const PUBLIC_CONST_B = 2;
    protected const PROTECTED_CONST = 3;
    private const PRIVATE_CONST = 4;
}
```

### <span class="type">iterable</span> 伪类

现在引入了一个新的被称为<span class="type">iterable</span>的伪类
(与<span class="type">callable</span>类似)。
这可以被用在参数或者返回值类型中，它代表接受数组或者实现了<span
class="classname">Traversable</span>接口的对象。
至于子类，当用作参数时，子类可以收紧父类的<span
class="type">iterable</span>类型到<span class="type">array</span>
或一个实现了<span
class="classname">Traversable</span>的对象。对于返回值，子类可以拓宽父类的
<span class="type">array</span>或对象返回值类型到<span
class="type">iterable</span>。

``` php
<?php
function iterator(iterable $iter)
{
    foreach ($iter as $val) {
        //
    }
}
```

### 多异常捕获处理

一个catch语句块现在可以通过管道字符(*\|*)来实现多个异常的捕获。
这对于需要同时处理来自不同类的不同异常时很有用。

``` php
<?php
try {
    // some code
} catch (FirstException | SecondException $e) {
    // handle first and second exceptions
}
```

### <span class="function">list</span>现在支持键名

现在<span
class="function">list</span>和它的新的*\[\]*语法支持在它内部去指定键名。这意味着它可以将任意类型的数组
都赋值给一些变量（与短数组语法类似）

``` php
<?php
$data = [
    ["id" => 1, "name" => 'Tom'],
    ["id" => 2, "name" => 'Fred'],
];

// list() style
list("id" => $id1, "name" => $name1) = $data[0];

// [] style
["id" => $id1, "name" => $name1] = $data[0];

// list() style
foreach ($data as list("id" => $id, "name" => $name)) {
    // logic here with $id and $name
}

// [] style
foreach ($data as ["id" => $id, "name" => $name]) {
    // logic here with $id and $name
}
```

### 支持为负的字符串偏移量

现在所有支持偏移量的<a href="/book/strings.html" class="link">字符串操作函数</a>
都支持接受负数作为偏移量，包括通过*\[\]*或*{}*操作<a href="/language/types/string.html#language.types.string.substr" class="link">字符串下标</a>。在这种情况下，一个负数的偏移量会被理解为一个从字符串结尾开始的偏移量。

``` php
<?php
var_dump("abcdef"[-2]);
var_dump(strpos("aabbcc", "b", -3));
```

以上例程会输出：

    string (1) "e"
    int(3)

Negative string and array offsets are now also supported in the simple
variable parsing syntax inside of strings.

``` php
<?php
$string = 'bar';
echo "The last character of '$string' is '$string[-1]'.\n";
?>
```

以上例程会输出：

    The last character of 'bar' is 'r'.

### ext/openssl 支持 AEAD

通过给<span class="function">openssl\_encrypt</span>和<span
class="function">openssl\_decrypt</span> 添加额外参数，现在支持了AEAD
(模式 GCM and CCM)。

### 通过 <span class="methodname">Closure::fromCallable</span> 将callables转为闭包

<span class="classname">Closure</span>新增了一个静态方法，用于将<span
class="type">callable</span>快速地 转为一个<span
class="classname">Closure</span> 对象。

``` php
<?php
class Test
{
    public function exposeFunction()
    {
        return Closure::fromCallable([$this, 'privateFunction']);
    }

    private function privateFunction($param)
    {
        var_dump($param);
    }
}

$privFunc = (new Test)->exposeFunction();
$privFunc('some value');
```

以上例程会输出：

    string(10) "some value"

### 异步信号处理

一个新的名为 <span class="function">pcntl\_async\_signals</span>
的方法现在被引入， 用于启用无需 ticks
（这会带来很多额外的开销）的异步信号处理。

``` php
<?php
pcntl_async_signals(true); // turn on async signals

pcntl_signal(SIGHUP,  function($sig) {
    echo "SIGHUP\n";
});

posix_kill(posix_getpid(), SIGHUP);
```

以上例程会输出：

    SIGHUP

### HTTP/2 server push support in ext/curl

对服务器推送的支持现在已经被加入到 CURL 扩展中（ 需要版本 7.46
或更高）。这个可以通过 <span class="function">curl\_multi\_setopt</span>
函数与新的常量 **`CURLMOPT_PUSHFUNCTION`** 来进行调节。常量
**`CURL_PUST_OK`** 和 **`CURL_PUSH_DENY`**
也已经被添加进来，以便服务器推送的回调函数来表明自己会同意或拒绝处理。
