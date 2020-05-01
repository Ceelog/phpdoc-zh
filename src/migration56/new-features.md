新特性
------

### 使用表达式定义常量

在之前的 PHP 版本中，
必须使用静态值来定义常量，声明属性以及指定函数参数默认值。
现在你可以使用包括数值、字符串字面量以及其他常量在内的数值表达式来
定义常量、声明属性以及设置函数参数默认值。

``` php
<?php
const ONE = 1;
const TWO = ONE * 2;

class C {
    const THREE = TWO + 1;
    const ONE_THIRD = ONE / self::THREE;
    const SENTENCE = 'The value of THREE is '.self::THREE;

    public function f($a = ONE + self::THREE) {
        return $a;
    }
}

echo (new C)->f()."\n";
echo C::SENTENCE;
?>
```

以上例程会输出：

    4
    The value of THREE is 3

现在可以通过 *const* 关键字来定义类型为 <span class="type">array</span>
的常量。

``` php
<?php
const ARR = ['a', 'b'];

echo ARR[0];
?>
```

以上例程会输出：

    a

### 使用 *...* 运算符定义变长参数函数

现在可以不依赖 <span class="function">func\_get\_args</span>， 使用
*...* 运算符 来实现
<a href="/functions/arguments.html#functions.variable-arg-list" class="link">变长参数函数</a>。

``` php
<?php
function f($req, $opt = null, ...$params) {
    // $params 是一个包含了剩余参数的数组
    printf('$req: %d; $opt: %d; number of params: %d'."\n",
           $req, $opt, count($params));
}

f(1);
f(1, 2);
f(1, 2, 3);
f(1, 2, 3, 4);
f(1, 2, 3, 4, 5);
?>
```

以上例程会输出：

    $req: 1; $opt: 0; number of params: 0
    $req: 1; $opt: 2; number of params: 0
    $req: 1; $opt: 2; number of params: 1
    $req: 1; $opt: 2; number of params: 2
    $req: 1; $opt: 2; number of params: 3

### 使用 *...* 运算符进行参数展开

在调用函数的时候，使用 *...* 运算符， 将
<a href="/language/types/array.html" class="link">数组</a> 和 <span
class="interfacename">可遍历</span> 对象展开为函数参数。
在其他编程语言，比如 Ruby中，这被称为连接运算符，。

``` php
<?php
function add($a, $b, $c) {
    return $a + $b + $c;
}

$operators = [2, 3];
echo add(1, ...$operators);
?>
```

以上例程会输出：

    6

### 使用 *\*\** 进行幂运算

加入右连接运算符 *\*\** 来进行幂运算。 同时还支持简写的 *\*\*=*
运算符，表示进行幂运算并赋值。

``` php
<?php
printf("2 ** 3 ==      %d\n", 2 ** 3);
printf("2 ** 3 ** 2 == %d\n", 2 ** 3 ** 2);

$a = 2;
$a **= 3;
printf("a ==           %d\n", $a);
?>
```

以上例程会输出：

    2 ** 3 ==      8
    2 ** 3 ** 2 == 512
    a ==           8

### *use function* 以及 *use const*

<a href="/language/namespaces/importing.html" class="link"><em>use</em></a>
运算符 被进行了扩展以支持在类中导入外部的函数和常量。 对应的结构为 *use
function* 和 *use const*。

``` php
<?php
namespace Name\Space {
    const FOO = 42;
    function f() { echo __FUNCTION__."\n"; }
}

namespace {
    use const Name\Space\FOO;
    use function Name\Space\f;

    echo FOO."\n";
    f();
}
?>
```

以上例程会输出：

    42
    Name\Space\f

### phpdbg

PHP 的 SAPI 模块中实现了一个 交互式调试器，叫做 phpdbg。更多信息，请访问
<a href="/book/phpdbg.html" class="link">phpdbg documentation</a>。

### 默认字符编码

对于一些字符编码相关的函数，例如 <span
class="function">htmlentities</span>， <span
class="function">html\_entity\_decode</span> 以及 <span
class="function">htmlspecialchars</span> 使用
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
作为默认字符集。请注意，对于 iconv（现已废弃） 和 mbstring 相关的函数，
如果分别设置了他们的编码， 那么这些对应设置的优先级高于
default\_charset。

default\_charset 的默认值是 *UTF-8*。

### <a href="/wrappers/php.html#wrappers.php.input" class="link"><em>php://input</em></a> 是可重用的了

只要你需要，你可以多次打开并读取
<a href="/wrappers/php.html#wrappers.php.input" class="link"><em>php://input</em></a>。
同时，这个特性使得在处理 POST 的数据的时候，
可以明显降低对于内存的需求量。

### 大文件上传

现在可以支持大于 2GB 的文件上传。

### <a href="/book/gmp.html" class="link">GMP</a> 支持运算符重载

<a href="/book/gmp.html" class="link">GMP</a> 支持运算符重载，
并且造型成数值类型。 这使得使用 GMP 的代码更加直观。

``` php
<?php
$a = gmp_init(42);
$b = gmp_init(17);

if (version_compare(PHP_VERSION, '5.6', '<')) {
    echo gmp_intval(gmp_add($a, $b)), PHP_EOL;
    echo gmp_intval(gmp_add($a, 17)), PHP_EOL;
    echo gmp_intval(gmp_add(42, $b)), PHP_EOL;
} else {
    echo $a + $b, PHP_EOL;
    echo $a + 17, PHP_EOL;
    echo 42 + $b, PHP_EOL;
}
?>
```

以上例程会输出：

    59
    59
    59

### 使用 <span class="function">hash\_equals</span> 比较字符串避免时序攻击

加入 <span class="function">hash\_equals</span> 函数，
以恒定的时间消耗来进行字符串比较， 以避免时序攻击。 比如当比较 <span
class="function">crypt</span> 密码散列值的时候，就可以使用此函数。
（假定你不能使用 <span class="function">password\_hash</span> 和 <span
class="function">password\_verify</span>，
这两个函数也可以抵抗时序攻击）

``` php
<?php
$expected  = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$correct   = crypt('12345', '$2a$07$usesomesillystringforsalt$');
$incorrect = crypt('1234',  '$2a$07$usesomesillystringforsalt$');

var_dump(hash_equals($expected, $correct));
var_dump(hash_equals($expected, $incorrect));
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### *\_\_debugInfo()*

加入
<a href="/language/oop5/magic.html#language.oop5.magic.debuginfo" class="link">__debugInfo()</a>，
当使用 <span class="function">var\_dump</span> 输出对象的时候，
可以用来控制要输出的属性和值。

``` php
<?php
class C {
    private $prop;

    public function __construct($val) {
        $this->prop = $val;
    }

    public function __debugInfo() {
        return [
            'propSquared' => $this->prop ** 2,
        ];
    }
}

var_dump(new C(42));
?>
```

以上例程会输出：

    object(C)#1 (1) {
      ["propSquared"]=>
      int(1764)
    }

### gost-crypto 散列算法

加入 *gost-crypto* 散列算法。 它使用
<a href="http://www.faqs.org/rfcs/rfc4357" class="link external">» RFC 4357, 11.2 小节</a>
定义的 CryptoPro S-box 表实现了 GOST 散列函数。

### SSL/TLS 提升

在 PHP 5.6 中对 SSL/TLS 的支持进行了大幅度的提升。 这其中包括
<a href="/migration56/incompatible.html#migration56.incompatible.peer-verification" class="link">默认启用端点验证</a>
选项来支持证书指纹比对， 以避免 TLS 重新协商攻击。 还增加了很多
<a href="/context/ssl.html" class="link">SSL 上下文选项</a>，
以便在使用加密流的时候， 能够更好的控制协议和验证的相关设置。

这些变动在
<a href="/migration56/openssl.html" class="link">PHP 5.6.x 中的 OpenSSL 变更</a>
中有详细描述。

### <a href="/book/pgsql.html" class="link">pgsql</a> 异步支持

<a href="/book/pgsql.html" class="link">pgsql</a> 扩展现在支持
异步方式连接数据库及执行查询， 也即可以使用非阻塞的方式和 PostgreSQL
数据库进行交互。 使用 **`PGSQL_CONNECT_ASYNC`** 常量可以
建立异步连接，<span class="function">pg\_connect\_poll</span>， <span
class="function">pg\_socket</span>， <span
class="function">pg\_consume\_input</span> 和 <span
class="function">pg\_flush</span> 函数 可以用来处理异步连接和查询。
