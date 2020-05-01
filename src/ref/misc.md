connection\_aborted
===================

检查客户端是否已经断开

### 说明

<span class="type">int</span> <span
class="methodname">connection\_aborted</span> ( <span
class="methodparam">void</span> )

检查客户端是否已经断开。

### 返回值

如果客户端已经断开则返回1，否则返回0。

### 参见

-   <span class="function">connection\_status</span>
-   <span class="function">ignore\_user\_abort</span>
-   查看<a href="/features/connection-handling.html" class="link">连接处理</a>
    了解PHP处理连接的详情。

connection\_status
==================

返回连接的状态位

### 说明

<span class="type">int</span> <span
class="methodname">connection\_status</span> ( <span
class="methodparam">void</span> )

获得当前连接的状态位。

### 返回值

获得当前连接的状态位, 可以用于与 *CONNECTION\_XXX*
定义的常量来确定连接状态。

### 参见

-   <span class="function">connection\_aborted</span>
-   <span class="function">ignore\_user\_abort</span>
-   查看<a href="/features/connection-handling.html" class="link">连接处理</a>
    了解PHP处理连接的详情。

constant
========

返回一个常量的值

### 说明

<span class="type">mixed</span> <span class="methodname">constant</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> )

通过 `name` 返回常量的值。

当你不知道常量名，却需要获取常量的值时，<span
class="function">constant</span>
就很有用了。也就是常量名储存在一个变量里，或者由函数返回常量名。

该函数也适用
<a href="/language/oop5/constants.html" class="link">class constants</a>。

### 参数

`name`  
常量名。

### 返回值

返回常量的值。如果常量未定义则返回 **`NULL`**。

### 错误／异常

如果常量未定义，会产生一个 **`E_WARNING`** 级别的错误。

### 范例

**示例 \#1 <span class="function">constant</span> 的例子**

``` php
<?php

define("MAXSIZE", 100);

echo MAXSIZE;
echo constant("MAXSIZE"); // same thing as the previous line


interface bar {
    const test = 'foobar!';
}

class foo {
    const test = 'foobar!';
}

$const = 'test';

var_dump(constant('bar::'. $const)); // string(7) "foobar!"
var_dump(constant('foo::'. $const)); // string(7) "foobar!"

?>
```

### 参见

-   <span class="function">define</span>
-   <span class="function">defined</span>
-   <a href="/language/constants.html" class="link">Constants</a> 这一节

define
======

定义一个常量

### 说明

<span class="type">bool</span> <span class="methodname">define</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$case_insensitive`<span class="initializer"> = false</span></span> \] )

在运行时定义一个常量。

### 参数

`name`  
常量名。

`value`  
常量的值；在 PHP 5 中，`value` 必须是标量( <span
class="type">integer</span>、 <span class="type">float</span>、<span
class="type">string</span>、<span
class="type">boolean</span>、**`NULL`**）在 PHP 7 中还允许是个 <span
class="type">array</span> 的值。

**Warning**
常量还可以定义为 <span class="type">resource</span>
类型，但并不推荐这样做，因为可能会有不可预知的行为发生。

`case_insensitive`  
如果设置为 **`TRUE`**，该常量则大小写不敏感。默认是大小写敏感的。比如，
*CONSTANT* 和 *Constant* 代表了不同的值。

> **Note**:
>
> 大小写不敏感的常量以小写的方式储存。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                        |
|-------|---------------------------------------------|
| 7.0.0 | 允许 <span class="type">array</span> 的值。 |

### 范例

**示例 \#1 定义常量**

``` php
<?php
define("CONSTANT", "Hello world.");
echo CONSTANT; // 输出 "Hello world."
echo Constant; // 输出 "Constant" 并导致 Notice

define("GREETING", "Hello you.", true);
echo GREETING; // 输出 "Hello you."
echo Greeting; // 输出 "Hello you."

//  PHP 7 起就可以运行了
define('ANIMALS', array(
    'dog',
    'cat',
    'bird'
));
echo ANIMALS[1]; // 输出 "cat"

?>
```

### 参见

-   <span class="function">defined</span>
-   <span class="function">constant</span>
-   <a href="/language/constants.html" class="link">Constants</a>这一节

defined
=======

检查某个名称的常量是否存在

### 说明

<span class="type">bool</span> <span class="methodname">defined</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

检查该名称的常量是否已定义。

> **Note**:
>
> 如果你要检查一个变量是否存在，请使用 <span
> class="function">isset</span>。 <span class="function">defined</span>
> 函数仅对 <a href="/language/constants.html" class="link">constants</a>
> 有效。如果你要检测某个函数是否存在，使用 <span
> class="function">function\_exists</span>。

### 参数

`name`  
常量的名称。

### 返回值

如果名称 `name` 的常量已定义，返回 **`TRUE`**；未定义则返回
**`FALSE`**。

### 范例

**示例 \#1 检查常量**

``` php
<?php
/* Note the use of quotes, this is important.  This example is checking
 * if the string 'TEST' is the name of a constant named TEST */
if (defined('TEST')) {
    echo TEST;
}
?>
```

### 参见

-   <span class="function">define</span>
-   <span class="function">constant</span>
-   <span class="function">get\_defined\_constants</span>
-   <span class="function">function\_exists</span>
-   章节 <a href="/language/constants.html" class="link">Constants</a>

die
===

等同于 <span class="function">exit</span>

### 说明

语法结构等同于 <span class="function">exit</span>。

eval
====

把字符串作为PHP代码执行

### 说明

<span class="type">mixed</span> <span class="methodname">eval</span> (
<span class="methodparam"><span class="type">string</span>
`$code`</span> )

把字符串 `code` 作为PHP代码执行。

**Caution**

函数<span class="function">eval</span>语言结构是 *非常危险*的，
因为它允许执行任意 PHP 代码。 *它这样用是很危险的。*
如果您仔细的确认过，除了使用此结构以外 别无方法,
请多加注意，*不要允许传入任何由用户 提供的、未经完整验证过的数据* 。

### 参数

`code`  
需要被执行的字符串

代码不能包含打开/关闭
<a href="/language/basic-syntax/phpmode.html" class="link">PHP tags</a>。比如，
*'echo "Hi!";'* 不能这样传入： *'\<?php echo "Hi!";
?\>'*。但仍然可以用合适的 PHP tag 来离开、重新进入 PHP 模式。比如 *'echo
"In PHP mode!"; ?\>In HTML mode!\<?php echo "Back in PHP mode!";'*。

除此之外，传入的必须是有效的 PHP 代码。所有的语句必须以分号结尾。比如
*'echo "Hi!"'* 会导致一个 parse error，而 *'echo "Hi!";'* 则会正常运行。

*return* 语句会立即中止当前字符串的执行。

代码执行的作用域是调用 <span class="function">eval</span>
处的作用域。因此，<span class="function">eval</span>
里任何的变量定义、修改，都会在函数结束后被保留。

### 返回值

<span class="function">eval</span> 返回 **`NULL`**，除非在执行的代码中
*return* 了一个值，函数返回传递给 *return* 的值。 PHP 7
开始，执行的代码里如果有一个 parse error，<span
class="function">eval</span> 会抛出 ParseError 异常。在 PHP 7 之前，
如果在执行的代码中有 parse error，<span class="function">eval</span>
返回 **`FALSE`**，之后的代码将正常执行。无法使用 <span
class="function">set\_error\_handler</span> 捕获 <span
class="function">eval</span> 中的解析错误。

### 范例

**示例 \#1 <span class="function">eval</span> 例子 - 简单的文本合并**

``` php
<?php
$string = 'cup';
$name = 'coffee';
$str = 'This is a $string with my $name in it.';
echo $str. "\n";
eval("\$str = \"$str\";");
echo $str. "\n";
?>
```

以上例程会输出：

    This is a $string with my $name in it.
    This is a cup with my coffee in it.

### 注释

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

**小贴士**

和直接将结果输出到浏览器一样，可使用<a href="/book/outcontrol.html" class="link">输出控制函数</a>来捕获当前函数的输出，然后(例如)保存到一个
<span class="type">string</span> 中。

> **Note**:
>
> 如果在执行的代码中产生了一个致命的错误（fatal
> error），整个脚本会退出。

### 参见

-   <span class="function">call\_user\_func</span>

exit
====

输出一个消息并且退出当前脚本

### 说明

<span class="type">void</span> <span class="methodname">exit</span> (\[
<span class="methodparam"><span class="type">string</span>
`$status`</span> \] )

<span class="type">void</span> <span class="methodname">exit</span> (
<span class="methodparam"><span class="type">int</span> `$status`</span>
)

中止脚本的执行。 尽管调用了 <span class="function">exit</span>，
<a href="/ref/funchand.html#register_shutdown_function" class="link">Shutdown函数</a>
以及
<a href="/language/oop5/decon.html#language.oop5.decon.destructor" class="link">object destructors</a>
总是会被执行。

*exit* 是个语法结构，如果没有 `status` 参数要传入，可以省略圆括号。

### 参数

`status`  
如果 `status` 是一个字符串，在退出之前该函数会打印 `status` 。

如果 `status` 是一个 <span
class="type">integer</span>，该值会作为退出状态码，并且不会被打印输出。
退出状态码应该在范围0至254，不应使用被PHP保留的退出状态码255。
状态码0用于成功中止程序。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">exit</span> 例子**

``` php
<?php

$filename = '/path/to/data-file';
$file = fopen($filename, 'r')
    or exit("unable to open file ($filename)");

?>
```

**示例 \#2 <span class="function">exit</span> 状态码例子**

``` php
<?php

//exit program normally
exit;
exit();
exit(0);

//exit with an error code
exit(1);
exit(0376); //octal

?>
```

**示例 \#3 无论如何，Shutdown函数与析构函数都会被执行**

``` php
<?php
class Foo
{
    public function __destruct()
    {
        echo 'Destruct: ' . __METHOD__ . '()' . PHP_EOL;
    }
}

function shutdown()
{
    echo 'Shutdown: ' . __FUNCTION__ . '()' . PHP_EOL;
}

$foo = new Foo();
register_shutdown_function('shutdown');

exit();
echo 'This will not be output.';
?>
```

以上例程会输出：

     Shutdown: shutdown()
     Destruct: Foo::__destruct()
     

### 注释

> **Note**: <span
> class="simpara">因为是一个语言构造器而不是一个函数，不能被
> <a href="/functions/variable-functions.html" class="link">可变函数</a>
> 调用。 </span>

> **Note**:
>
> 该语法结构等同于 <span class="function">die</span>。

### 参见

-   <span class="function">register\_shutdown\_function</span>

get\_browser
============

获取浏览器具有的功能

### 说明

<span class="type">mixed</span> <span
class="methodname">get\_browser</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$user_agent`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$return_array`<span class="initializer"> =
false</span></span> \]\] )

通过查找 `browscap.ini`
文件中的浏览器信息，尝试检测用户的浏览器所具有的功能。

### 参数

`user_agent`  
要分析的用户代理。默认使用HTTP头中User-Agent的值，不过，你可以通过传递该参数改变User-Agent。(比如查找另一个浏览器的信息)

你可以传递一个 **`NULL`** 来忽略该参数。

`return_array`  
如果设置为 **`TRUE`**，该函数会返回一个 <span
class="type">array</span>，而不是 <span class="type">object</span>。

### 返回值

信息会以包含一系列数据的数组或者对象返回。例如：浏览器的主版本号、次版本号和ID字符串；框架、JavaScript、cookies等功能是否支持
**`TRUE`**/**`FALSE`** 的值。

*cookies*
的值仅意味着浏览器是否具有接收cookies的功能，不代表用户是否已允许启用cookies。
测试的唯一办法，只有通过 <span class="function">setcookie</span>
设置一个cookie，刷新页面并检测该cookie的值。

### 范例

**示例 \#1 列出所有用户浏览器的信息**

``` php
<?php
echo $_SERVER['HTTP_USER_AGENT'] . "\n\n";

$browser = get_browser(null, true);
print_r($browser);
?>
```

以上例程的输出类似于：

    Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.7) Gecko/20040803 Firefox/0.9.3

    Array
    (
        [browser_name_regex] => ^mozilla/5\.0 (windows; .; windows nt 5\.1; .*rv:.*) gecko/.* firefox/0\.9.*$
        [browser_name_pattern] => Mozilla/5.0 (Windows; ?; Windows NT 5.1; *rv:*) Gecko/* Firefox/0.9*
        [parent] => Firefox 0.9
        [platform] => WinXP
        [browser] => Firefox
        [version] => 0.9
        [majorver] => 0
        [minorver] => 9
        [cssversion] => 2
        [frames] => 1
        [iframes] => 1
        [tables] => 1
        [cookies] => 1
        [backgroundsounds] =>
        [vbscript] =>
        [javascript] => 1
        [javaapplets] => 1
        [activexcontrols] =>
        [cdf] =>
        [aol] =>
        [beta] => 1
        [win16] =>
        [crawler] =>
        [stripper] =>
        [wap] =>
        [netclr] =>
    )

### 注释

> **Note**:
>
> 为了能让该函数运作，在 `php.ini` 中配置的
> <a href="/misc/setup.html#" class="link">browscap</a> 必须指向
> `browscap.ini` 文件的正确位置。
>
> `browscap.ini` 并未内置在PHP中，不过你可以在这里找到最新的
> <a href="http://browscap.org/" class="link external">» php_browscap.ini</a>。
>
> `browscap.ini`
> 包含的诸多浏览器信息依赖于用户更新该数据库。该文件的格式不言自明。

\_\_halt\_compiler
==================

中断编译器的执行

### 说明

<span class="type">void</span> <span
class="methodname">\_\_halt\_compiler</span> ( <span
class="methodparam">void</span> )

中断编译器的执行。常用于在PHP脚本内嵌入数据，类似于安装文件。

可以通过常量 **`__COMPILER_HALT_OFFSET__`**
获取数据开始字节所在的位置，且该常量仅被定义于使用了\_\_halt\_compiler的文件。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">\_\_halt\_compiler</span> 例子**

``` php
<?php

// open this file
$fp = fopen(__FILE__, 'r');

// seek file pointer to data
fseek($fp, __COMPILER_HALT_OFFSET__);

// and output it
var_dump(stream_get_contents($fp));

// the end of the script execution
__halt_compiler(); the installation data (eg. tar, gz, PHP, etc.)
```

### 注释

> **Note**:
>
> <span class="function">\_\_halt\_compiler</span> 仅能够在最外层使用。

highlight\_file
===============

语法高亮一个文件

### 说明

<span class="type">mixed</span> <span
class="methodname">highlight\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$return`<span class="initializer"> = false</span></span> \] )

使用PHP内置的语法高亮器所定义的颜色，打印输出或者返回 `filename`
文件中语法高亮版本的代码。

许多服务器配置了自动高亮 *phps* 扩展的文件。 比如，访问 `example.phps`
会显示语法高亮后的文件。 添加以下一行代码到 `httpd.conf` 使此生效：

``` description
AddType application/x-httpd-php-source .phps
```

### 参数

`filename`  
欲高亮文件的路径。

`return`  
设置该参数为 **`TRUE`** 使函数返回高亮后的代码。

### 返回值

如果 `return` 设置为
**`TRUE`**，高亮后的代码不会被打印输出，而是以字符串的形式返回。
高亮成功返回 **`TRUE`**，否则返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                 |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.2.1 | 该函数现在也受 <a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a> 和 <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a> 的限制和影响。 |

### 注释

**Caution**

应当注意在使用 <span class="function">highlight\_file</span>
时，确认没有在不经意间泄漏敏感信息，类似密码或者其他任何具有潜在安全风险的信息。

> **Note**:
>
> 当使用了`return` 参数时，本函数使用其内部输出缓冲，因此不能在 <span
> class="function">ob\_start</span> 回调函数的内部使用。

### 参见

-   <span class="function">highlight\_string</span>
-   <a href="/misc/setup.html#" class="link">Highlighting INI 指令</a>

highlight\_string
=================

字符串的语法高亮

### 说明

<span class="type">mixed</span> <span
class="methodname">highlight\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$str`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$return`<span
class="initializer"> = false</span></span> \] )

使用PHP内置的语法高亮器所定义的颜色，打印输出或者返回输出或者返回语法高亮版本的PHP代码。

### 参数

`str`  
需要高亮的PHP代码，应当包含开始标签。

`return`  
设置该参数为 **`TRUE`** 使函数返回高亮后的代码。

### 返回值

如果 `return` 设置为
**`TRUE`**，高亮后的代码不会被打印输出，而是以字符串的形式返回。
高亮成功返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">highlight\_string</span> 例子**

``` php
<?php
highlight_string('<?php phpinfo(); ?>');
?>
```

以上例程会输出：

    <code><span style="color: #000000">
    <span style="color: #0000BB">&lt;?php phpinfo</span><span style="color: #007700">(); </span><span style="color: #0000BB">?&gt;</span>
    </span>
    </code>

### 注释

> **Note**:
>
> 当使用了`return` 参数时，本函数使用其内部输出缓冲，因此不能在 <span
> class="function">ob\_start</span> 回调函数的内部使用。

产生的 HTML 标记可能会有更改。

### 参见

-   <span class="function">highlight\_file</span>
-   <a href="/misc/setup.html#" class="link">高亮 INI 指令</a>

hrtime
======

Get the system's high resolution time

### 说明

<span class="type">mixed</span> <span class="methodname">hrtime</span>
(\[ <span class="methodparam"><span class="type">bool</span>
`$get_as_number`<span class="initializer"> = **`FALSE`**</span></span>
\] )

Returns the system's high resolution time, counted from an arbitrary
point in time. The delivered timestamp is monotonic and can not be
adjusted.

### 参数

`get_as_number`  
Whether the high resolution time should be returned as <span
class="type">array</span> or number.

### 返回值

Returns an array of integers in the form \[seconds, nanoseconds\], if
the parameter `get_as_number` is false. Otherwise the nanoseconds are
returned as <span class="type">integer</span> (64bit platforms) or <span
class="type">float</span> (32bit platforms).

### 范例

**示例 \#1 <span class="function">hrtime</span> usage**

``` php
<?php
echo hrtime(true), PHP_EOL;
print_r(hrtime());
?>
```

以上例程的输出类似于：

    10444739687370679
    Array
    (
        [0] => 10444739
        [1] => 687464812
    )

### 参见

-   The
    <a href="/book/hrtime.html" class="link">High resolution timing</a>
    extension
-   <span class="function">microtime</span>

ignore\_user\_abort
===================

设置客户端断开连接时是否中断脚本的执行

### 说明

<span class="type">int</span> <span
class="methodname">ignore\_user\_abort</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$value`</span> \] )

设置客户端断开连接时是否中断脚本的执行

PHP 以命令行脚本执行时，当脚本终端结束，脚本不会被立即中止，除非设置
`value` 为 **`TRUE`**，否则脚本输出任意字符时会被中止。

### 参数

`value`  
如果设置了该值，函数会把
<a href="/misc/setup.html#" class="link">ignore_user_abort</a> ini
的值设置为 `value`。
如果未设置该值，函数不会改变设置，仅会返回之前的设置。

### 返回值

以整型返回之前的设置

### 范例

**示例 \#1 <span class="function">ignore\_user\_abort</span>例子**

``` php
<?php
// Ignore user aborts and allow the script
// to run forever
ignore_user_abort(true);
set_time_limit(0);

echo 'Testing connection handling in PHP';

// Run a pointless loop that sometime 
// hopefully will make us click away from 
// page or click the "Stop" button.
while(1)
{
    // Did the connection fail?
    if(connection_status() != CONNECTION_NORMAL)
    {
        break;
    }

    // Sleep for 10 seconds
    sleep(10);
}

// If this is reached, then the 'break' 
// was triggered from inside the while loop

// So here we can log, or perform any other tasks
// we need without actually being dependent on the 
// browser.
?>
```

### 注释

在PHP尝试发送信息到客户端之前，不会检测到用户是否已中断连接。 仅使用
echo 语句不能确保信息已发送，参见 <span class="function">flush</span>
函数。

### 参见

-   <span class="function">connection\_aborted</span>
-   <span class="function">connection\_status</span>
-   <a href="/features/connection-handling.html" class="link">Connection Handling</a>
    关于PHP连接处理的完整描述。

pack
====

将数据打包成二进制字符串

### 说明

<span class="type">string</span> <span class="methodname">pack</span> (
<span class="methodparam"><span class="type">string</span>
`$format`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$args`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...`</span> \]\] )

根据`format`将给地的参数打包成二进制字符串。

这个函数的思想来自Perl，所有格式化代码（`format`）的工作原理都与Perl相同。
但是，缺少了部分格式代码，比如Perl的“u”。

注意，有符号值和无符号值之间的区别只影响函数<span
class="function">unpack</span>,
在那些使用有符号和无符号格式代码的地方<span
class="function">pack</span>函数产生相同的结果。

### 参数

`format`  
`format`字符串由格式代码组成，后面跟着一个可选的重复参数。
重复参数可以是一个整数值或者*\**值来重复到输入数据的末尾。对于a, A, h,
H格式化代码，其后的重复参数指定了给定数据将会被使用几个字符串，对于@,其后的数字表示放置剩余数据的绝对定位（之前的数据将会被空字符串填充），对于其他所有内容，重复数量指定消耗多少数据并将其打包到生成的二进制字符串中。

目前已实现的格式如下：

| 代码 | 描述                                       |
|------|--------------------------------------------|
| a    | 以NUL字节填充字符串                        |
| A    | 以SPACE(空格)填充字符串                    |
| h    | 十六进制字符串，低位在前                   |
| H    | 十六进制字符串，高位在前                   |
| c    | 有符号字符                                 |
| C    | 无符号字符                                 |
| s    | 有符号短整型(16位，主机字节序)             |
| S    | 无符号短整型(16位，主机字节序)             |
| n    | 无符号短整型(16位，大端字节序)             |
| v    | 无符号短整型(16位，小端字节序)             |
| i    | 有符号整型(机器相关大小字节序)             |
| I    | 无符号整型(机器相关大小字节序)             |
| l    | 有符号长整型(32位，主机字节序)             |
| L    | 无符号长整型(32位，主机字节序)             |
| N    | 无符号长整型(32位，大端字节序)             |
| V    | 无符号长整型(32位，小端字节序)             |
| q    | 有符号长长整型(64位，主机字节序)           |
| Q    | 无符号长长整型(64位，主机字节序)           |
| J    | 无符号长长整型(64位，大端字节序)           |
| P    | 无符号长长整型(64位，小端字节序)           |
| f    | 单精度浮点型(机器相关大小)                 |
| g    | 单精度浮点型(机器相关大小，小端字节序)     |
| G    | 单精度浮点型(机器相关大小，大端字节序)     |
| d    | 双精度浮点型(机器相关大小)                 |
| e    | 双精度浮点型(机器相关大小，小端字节序)     |
| E    | 双精度浮点型(机器相关大小，大端字节序)     |
| x    | NUL字节                                    |
| X    | 回退已字节                                 |
| Z    | 以NUL字节填充字符串空白(PHP 5.5中新加入的) |
| @    | NUL填充到绝对位置                          |

`args`  

### 返回值

返回包含数据的二进制字符串。

### 更新日志

| 版本         | 说明                                                                                     |
|--------------|------------------------------------------------------------------------------------------|
| 7.2.0        | <span class="type">float</span> 和 <span class="type">double</span> 类型支持打断和小端。 |
| 7.0.15,7.1.1 | 添加了"e","E","g"和"G"代码以启用float和double的字节顺序支持。                            |
| 5.6.3        | 添加了“q”、“q”、“J”和“P”代码以支持处理64位数字。                                         |
| 5.5.0        | “Z”代码添加了与“a”等效的功能，以实现Perl兼容性。                                         |

### 范例

**示例 \#1 <span class="function">pack</span> 范例**

``` php
<?php
$binarydata = pack("nvc*", 0x1234, 0x5678, 65, 66);
?>
```

The resulting binary string will be 6 bytes long and contain the byte
sequence 0x12, 0x34, 0x78, 0x56, 0x41, 0x42.

### 注释

**Caution**

Note that PHP internally stores <span class="type">integer</span> values
as signed values of a machine-dependent size (C type *long*). Integer
literals and operations that yield numbers outside the bounds of the
<span class="type">integer</span> type will be stored as <span
class="type">float</span>. When packing these floats as integers, they
are first cast into the integer type. This may or may not result in the
desired byte pattern.

The most relevant case is when packing unsigned numbers that would be
representable with the <span class="type">integer</span> type if it were
unsigned. In systems where the <span class="type">integer</span> type
has a 32-bit size, the cast usually results in the same byte pattern as
if the <span class="type">integer</span> were unsigned (although this
relies on implementation-defined unsigned to signed conversions, as per
the C standard). In systems where the <span class="type">integer</span>
type has 64-bit size, the <span class="type">float</span> most likely
does not have a mantissa large enough to hold the value without loss of
precision. If those systems also have a native 64-bit C *int* type (most
UNIX-like systems don't), the only way to use the *I* pack format in the
upper range is to create <span class="type">integer</span> negative
values with the same byte representation as the desired unsigned value.

### 参见

-   <span class="function">unpack</span>

php\_check\_syntax
==================

检查PHP的语法（并执行）指定的文件

### 说明

<span class="type">bool</span> <span
class="methodname">php\_check\_syntax</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`&$error_message`</span> \] )

对指定的 `filename` 进行语法检查，检测脚本的错误。

此函数除了会执行（但不会输出）`filename`，其他与
<a href="/features/commandline.html" class="link">命令行</a>中使用**php
-l** 相似。

例如，如果函数在文件 `filename` 中被定义了，则该函数在执行<span
class="function">php\_check\_syntax</span>后可用。但是`filename`输出内容不会被输出。

> **Note**:
>
> 因为某些技术原因，该函数已被弃用，并且从PHP中移除了。请以<a href="/features/commandline.html" class="link">commandline</a>使用
> *php -l somefile.php*取而代之。

### 参数

`filename`  
需要被检测的文件。

`error_message`  
如果使用了参数 `error_message`，它会包含语法检测出的错误信息。
`error_message` 以
<a href="/language/references.html" class="link">引用</a>方式传递。

### 返回值

如果语法检测通过返回 **`TRUE`**，未通过或者文件无法打开则返回
**`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 5.0.5 | 函数从PHP中移除。                                                                                              |
| 5.0.3 | <span class="function">php\_check\_syntax</span>之后调用 <span class="function">exit</span> 会导致一个段错误。 |
| 5.0.1 | `error_message` 通过引用传递                                                                                   |

### 范例

``` examples
php -l somefile.php
```

以上例程的输出类似于：

``` examples
PHP Parse error: unexpected T_STRING in /tmp/somefile.php on line 81
```

### 参见

-   <span class="function">include</span>
-   <span class="function">is\_readable</span>

php\_strip\_whitespace
======================

返回删除注释和空格后的PHP源码

### 说明

<span class="type">string</span> <span
class="methodname">php\_strip\_whitespace</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

返回删除注释和空格后 `filename`
的PHP源码。这对实际代码数量和注释数量的对比很有用。 此函数与
<a href="/features/commandline.html" class="link">命令行</a> 下执行
**php -w** 相似。

### 参数

`filename`  
PHP文件的路径。

### 返回值

在成功时返回过滤后的代码，或者在失败时返回空字符串。

> **Note**:
>
> 此函数在PHP
> 5.0.1后以所述方式工作。之前它仅会返回一个空字符串。关于更多此BUG的信息与其行为，详见BUG报告
> <a href="https://bugs.php.net/29606" class="link external">» #29606</a>。

### 范例

**示例 \#1 <span class="function">php\_strip\_whitespace</span> 的例子**

``` php
<?php
// PHP comment here

/*
 * Another PHP comment
 */

echo        php_strip_whitespace(__FILE__);
// Newlines are considered whitespace, and are removed too:
do_nothing();
?>
```

以上例程会输出：

    <?php
     echo php_strip_whitespace(__FILE__); do_nothing(); ?>

可以注意到PHP的注释已不存在，成为第一个echo语句前的换行和空格。

sapi\_windows\_cp\_conv
=======================

Convert string from one codepage to another

### 说明

<span class="type">string</span> <span
class="methodname">sapi\_windows\_cp\_conv</span> ( <span
class="methodparam"><span class="type">int\|string</span>
`$in_codepage`</span> , <span class="methodparam"><span
class="type">int\|string</span> `$out_codepage`</span> , <span
class="methodparam"><span class="type">string</span> `$subject`</span> )

Convert string from one codepage to another.

### 参数

`in_codepage`  
The codepage of the `subject` string. Either the codepage name or
identifier.

`out_codepage`  
The codepage to convert the `subject` string to. Either the codepage
name or identifier.

`subject`  
The string to convert.

### 返回值

The `subject` string converted to `out_codepage`, or **`NULL`** on
failure.

### 错误／异常

This function issues E\_WARNING level errors, if invalid codepages are
given, or if the subject is not valid for `in_codepage`.

### 参见

-   <span class="function">sapi\_windows\_cp\_get</span>
-   <span class="function">iconv</span>

sapi\_windows\_cp\_get
======================

Get process codepage

### 说明

<span class="type">int</span> <span
class="methodname">sapi\_windows\_cp\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$kind`</span> )

Get the identifier of the codepage of the current process.

### 参数

`kind`  
The kind of codepage: either *'ansi'* or *'oem'*.

### 返回值

Returns the codepage identifier.

### 参见

-   <span class="function">sapi\_windows\_cp\_set</span>

sapi\_windows\_cp\_is\_utf8
===========================

Indicates whether the codepage is UTF-8 compatible

### 说明

<span class="type">bool</span> <span
class="methodname">sapi\_windows\_cp\_is\_utf8</span> ( <span
class="methodparam">void</span> )

Indicates whether the codepage of the current process is UTF-8
compatible.

### 参数

此函数没有参数。

### 返回值

Returns whether the codepage of the current process is UTF-8 compatible.

### 参见

-   <span class="function">sapi\_windows\_cp\_get</span>

sapi\_windows\_cp\_set
======================

Set process codepage

### 说明

<span class="type">bool</span> <span
class="methodname">sapi\_windows\_cp\_set</span> ( <span
class="methodparam"><span class="type">int</span> `$cp`</span> )

Set the codepage of the current process.

### 参数

`cp`  
A codepage identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">sapi\_windows\_cp\_get</span>

sapi\_windows\_generate\_ctrl\_event
====================================

Send a CTRL event to another process

### 说明

<span class="type">bool</span> <span
class="methodname">sapi\_windows\_generate\_ctrl\_event</span> ( <span
class="methodparam"><span class="type">int</span> `$event`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pid`<span
class="initializer"> = 0</span></span> \] )

Sends a CTRL event to another process in the same process group.

### 参数

`event`  
The *CTRL* even to send; either **`PHP_WINDOWS_EVENT_CTRL_C`** or
**`PHP_WINDOWS_EVENT_CTRL_BREAK`**.

`pid`  
The ID of the process to which to send the event to. If *0* is given,
the event is sent to all processes of the process group.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Basic <span
class="function">sapi\_windows\_generate\_ctrl\_event</span> Usage**

This example shows how to pass along *CTRL+BREAK* events to a child
process. In this case the child process echoes *I'm still alive* every
second, until the user presses *CTRL+BREAK*, what causes only the child
process to be terminated.

``` php
<?php
// forward CTRL+BREAK events to the child process
sapi_windows_set_ctrl_handler('sapi_windows_generate_ctrl_event');

// create a child process which echoes every second
$cmd = ['php', '-r', 'while (true) { echo "I\'m still alive\n"; sleep(1); }'];
$descspec = array(['pipe', 'r'], ['pipe', 'w'], ['pipe', 'w']);
$options = ['create_process_group' => true];
$proc = proc_open($cmd, $descspec, $pipes, null, null, $options);
while (true) {
    echo fgets($pipes[1]);
}
?>
```

### 参见

-   <span class="function">proc\_open</span>
-   <span class="function">sapi\_windows\_set\_ctrl\_handler</span>

sapi\_windows\_set\_ctrl\_handler
=================================

Set or remove a CTRL event handler

### 说明

<span class="type">bool</span> <span
class="methodname">sapi\_windows\_set\_ctrl\_handler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callable`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$add`<span class="initializer"> =
**`TRUE`**</span></span> \] )

Sets or removes a *CTRL* event handler, which allows Windows CLI
processes to intercept or ignore *CTRL+C* and *CTRL+BREAK* events. Note
that in multithreaded environments, this is only possible when called
from the main thread.

### 参数

`callable`  
A callback function to set or remove. If set, this function will be
called whenever a *CTRL+C* or *CTRL+BREAK* event occurs. The function is
supposed to have the following signature:

<span class="type">void</span> <span class="methodname">handler</span> (
<span class="methodparam"><span class="type">int</span> `$event`</span>
)

`event`  
<span class="simpara"> The *CTRL* event which has been received; either
**`PHP_WINDOWS_EVENT_CTRL_C`** or **`PHP_WINDOWS_EVENT_CTRL_BREAK`**.
</span>

Setting a **`NULL`** `callable` causes the process to ignore *CTRL+C*
events, but not *CTRL+BREAK* events.

`add`  
If **`TRUE`**, the handler is set. If **`FALSE`**, the handler is
removed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Basic <span
class="function">sapi\_windows\_set\_ctrl\_handler</span> Usage**

This example shows how to intercept *CTRL* events.

``` php
<?php
function ctrl_handler(int $event)
{
    switch ($event) {
        case PHP_WINDOWS_EVENT_CTRL_C:
            echo "You have pressed CTRL+C\n";
            break;
        case PHP_WINDOWS_EVENT_CTRL_BREAK:
            echo "You have pressed CTRL+BREAK\n";
            break;
    }
}

sapi_windows_set_ctrl_handler('ctrl_handler');
while (true); // infinite loop, so the handler can be triggered
?>
```

### 参见

-   <span class="function">sapi\_windows\_generate\_ctrl\_event</span>

sapi\_windows\_vt100\_support
=============================

Get or set VT100 support for the specified stream associated to an
output buffer of a Windows console.

### 说明

<span class="type">bool</span> <span
class="methodname">sapi\_windows\_vt100\_support</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$enable`</span> \] )

If `enable` is omitted, the function returns **`TRUE`** if the stream
`stream` has VT100 control codes enabled, **`FALSE`** otherwise.

If `enable` is specified, the function will try to enable or disable the
VT100 features of the stream `stream`. If the feature has been
successfully enabled (or disabled), the function will return **`TRUE`**,
or **`FALSE`** otherwise.

At startup, PHP tries to enable the VT100 feature of the
**`STDOUT`**/**`STDERR`** streams. By the way, if those streams are
redirected to a file, the VT100 features may not be enabled.

If VT100 support is enabled, it is possible to use control sequences as
they are known from the VT100 terminal. They allow the modification of
the terminal's output. On Windows these sequences are called Console
Virtual Terminal Sequences.

**Warning**

This function uses the **`ENABLE_VIRTUAL_TERMINAL_PROCESSING`** flag
implemented in the Windows 10 API, so the VT100 feature may not be
available on older Windows versions.

### 参数

`stream`  
The stream on which the function will operate.

`enable`  
If specified, the VT100 feature will be enabled (if **`TRUE`**) or
disabled (if **`FALSE`**).

### 返回值

If `enable` is not specified: returns **`TRUE`** if the VT100 feature is
enabled, **`FALSE`** otherwise.

If `enable` is specified: 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

### 范例

**示例 \#1 <span class="function">sapi\_windows\_vt100\_support</span>
default state**

By default, **`STDOUT`** and **`STDERR`** have the VT100 feature
enabled.

``` sh
php -r "var_export(sapi_windows_vt100_support(STDOUT));echo ' ';var_export(sapi_windows_vt100_support(STDERR));"
```

以上例程的输出类似于：

    true true

By the way, if a stream is redirected, the VT100 feature will not be
enabled:

``` sh
php -r "var_export(sapi_windows_vt100_support(STDOUT));echo ' ';var_export(sapi_windows_vt100_support(STDERR));" 2>NUL
```

以上例程的输出类似于：

  
true false  

**示例 \#2 <span class="function">sapi\_windows\_vt100\_support</span>
changing state**

You won't be able to enable the VT100 feature of **`STDOUT`** or
**`STDERR`** if the stream is redirected.

``` sh
php -r "var_export(sapi_windows_vt100_support(STDOUT, true));echo ' ';var_export(sapi_windows_vt100_support(STDERR, true));" 2>NUL
```

以上例程的输出类似于：

    true false

**示例 \#3 Example usage of VT100 support enabled**

``` php
<?php
$out = fopen('php://stdout','w');
fwrite($out, 'Just forgot a lettr.');
// Moves the cursor two characters backwards
fwrite($out, "\033[2D");
// Inserts one blank, shifting existing text to the right -> Just forgot a lett r.
fwrite($out, "\033[1@");
fwrite($out, 'e');
?>
```

以上例程会输出：

    Just forgot a letter.

show\_source
============

别名 <span class="function">highlight\_file</span>

### 说明

此函数是该函数的别名： <span class="function">highlight\_file</span>.

sleep
=====

延缓执行

### 说明

<span class="type">int</span> <span class="methodname">sleep</span> (
<span class="methodparam"><span class="type">int</span>
`$seconds`</span> )

程序延迟执行指定的 `seconds` 的秒数。

### 参数

`seconds`  
暂停的秒数。

### 返回值

成功时返回 0，错误时返回 **`FALSE`**。

如果函数的调用被一个信号中止，<span class="function">sleep</span>
会返回一个非零的值。在Windows上，该值总是 *192*（即Windows
API常量**`WAIT_IO_COMPLETION`**的值）。其他平台上，该返回值是剩余未sleep的秒数。

### 错误／异常

如果指定的 `seconds` 是负数，该函数会产生一个 **`E_WARNING`**
级别的错误。

### 更新日志

| 版本  | 说明                                                                                                             |
|-------|------------------------------------------------------------------------------------------------------------------|
| 5.3.4 | 在PHP 5.3.4之前，Windows平台下无论 <span class="function">sleep</span> 是否成功调用，总是会返回一个 **`NULL`**。 |

### 范例

**示例 \#1 <span class="function">sleep</span> 的例子**

``` php
<?php

// current time
echo date('h:i:s') . "\n";

// sleep for 10 seconds
sleep(10);

// wake up !
echo date('h:i:s') . "\n";

?>
```

该例子会在休眠10秒后输出。

    05:31:23
    05:31:33

### 参见

-   <span class="function">usleep</span>
-   <span class="function">time\_nanosleep</span>
-   <span class="function">time\_sleep\_until</span>
-   <span class="function">set\_time\_limit</span>

sys\_getloadavg
===============

获取系统的负载（load average）

### 说明

<span class="type">array</span> <span
class="methodname">sys\_getloadavg</span> ( <span
class="methodparam">void</span> )

返回三个系统负载（系统运行队列中的进程数）的样本数据，分别是1分钟、5分钟和15分钟之前。

### 返回值

返回一个包含1分钟、5分钟和15分钟之前采样数据的<span
class="type">array</span>。

### 范例

**示例 \#1 <span class="function">sys\_getloadavg</span> 的例子**

``` php
<?php
$load = sys_getloadavg();
if ($load[0] > 80) {
    header('HTTP/1.1 503 Too busy, try again later');
    die('Server too busy. Please try again later.');
}
?>
```

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

time\_nanosleep
===============

延缓执行若干秒和纳秒

### 说明

<span class="type">mixed</span> <span
class="methodname">time\_nanosleep</span> ( <span
class="methodparam"><span class="type">int</span> `$seconds`</span> ,
<span class="methodparam"><span class="type">int</span>
`$nanoseconds`</span> )

程序延缓执行指定数量的 `seconds` 和 `nanoseconds`。

### 参数

`seconds`  
必须是一个非负整数。

`nanoseconds`  
必须是一个小于1亿的非负整数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

如果延迟被中断，一个关联数组会返回，内容为：

-   <span class="simpara"> *seconds* - 延迟剩余未执行的秒数 </span>
-   <span class="simpara"> *nanoseconds* - 延迟剩余未执行的纳秒数
    </span>

### 更新日志

| 版本  | 说明                                |
|-------|-------------------------------------|
| 5.3.0 | 至此之后该函数在Windows平台下可用。 |

### 范例

**示例 \#1 <span class="function">time\_nanosleep</span> 的例子**

``` php
<?php
// Careful! This won't work as expected if an array is returned
if (time_nanosleep(0, 500000000)) {
    echo "Slept for half a second.\n";
}

// This is better:
if (time_nanosleep(0, 500000000) === true) {
    echo "Slept for half a second.\n";
}

// And this is the best:
$nano = time_nanosleep(2, 100000);

if ($nano === true) {
    echo "Slept for 2 seconds, 100 microseconds.\n";
} elseif ($nano === false) {
    echo "Sleeping failed.\n";
} elseif (is_array($nano)) {
    $seconds = $nano['seconds'];
    $nanoseconds = $nano['nanoseconds'];
    echo "Interrupted by a signal.\n";
    echo "Time remaining: $seconds seconds, $nanoseconds nanoseconds.";
}
?>
```

### 参见

-   <span class="function">sleep</span>
-   <span class="function">usleep</span>
-   <span class="function">time\_sleep\_until</span>
-   <span class="function">set\_time\_limit</span>

time\_sleep\_until
==================

使脚本睡眠到指定的时间为止。

### 说明

<span class="type">bool</span> <span
class="methodname">time\_sleep\_until</span> ( <span
class="methodparam"><span class="type">float</span> `$timestamp`</span>
)

使脚本睡眠到指定的 `timestamp`。

### 参数

`timestamp`  
将脚本唤醒的时间戳。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 5.3.0 | 自此，函数在Windows平台可用。 |

### 错误／异常

如果设定的 `timestamp` 为过去的时间，脚本将会产生一个 **`E_WARNING`**
级别的错误。

### 范例

**示例 \#1 <span class="function">time\_sleep\_until</span> 的一个例子**

``` php
<?php

//returns false and generates a warning
var_dump(time_sleep_until(time()-1));

// may only work on faster computers, will sleep up to 0.2 seconds
var_dump(time_sleep_until(microtime(true)+0.2));

?>
```

### 注释

> **Note**: <span class="simpara"> 所有的信号会被延迟至脚本唤醒以后。
> </span>

### 参见

-   <span class="function">sleep</span>
-   <span class="function">usleep</span>
-   <span class="function">time\_nanosleep</span>
-   <span class="function">set\_time\_limit</span>

uniqid
======

生成一个唯一ID

### 说明

<span class="type">string</span> <span class="methodname">uniqid</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$prefix`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$more_entropy`<span
class="initializer"> = false</span></span> \]\] )

获取一个带前缀、基于当前时间微秒数的唯一ID。

**Caution**

本函数并不会生成安全加密的值，不应用于加密用途。若需要安全加密的值，考虑使用<span
class="function">openssl\_random\_pseudo\_bytes</span>。

**Warning**

此函数不保证返回值的唯一性。 由于绝大多数系统使用 NTP
或者类似服务调整系统的时间，所以系统时间经常发生变化。
此外，进程/线程可能不会返回唯一的 ID。 用 `more_entropy`
来增加唯一性的概率。

### 参数

`prefix`  
有用的参数。例如：如果在多台主机上可能在同一微秒生成唯一ID。

`prefix`为空，则返回的字符串长度为13。`more_entropy` 为
**`TRUE`**，则返回的字符串长度为23。

`more_entropy`  
如果设置为 **`TRUE`**，<span class="function">uniqid</span>
会在返回的字符串结尾增加额外的熵（使用combined linear congruential
generator）。 使得唯一ID更具唯一性。

### 返回值

返回字符串形式的唯一ID。

**Warning**

此函数努力创建唯一识别符，但它不保证返回值得唯一性。

### 范例

**示例 \#1 <span class="function">uniqid</span> 例子**

``` php
<?php
/* A uniqid, like: 4b3403665fea6 */
printf("uniqid(): %s\r\n", uniqid());

/* We can also prefix the uniqid, this the same as 
 * doing:
 *
 * $uniqid = $prefix . uniqid();
 * $uniqid = uniqid($prefix);
 */
printf("uniqid('php_'): %s\r\n", uniqid('php_'));

/* We can also activate the more_entropy parameter, which is 
 * required on some systems, like Cygwin. This makes uniqid()
 * produce a value like: 4b340550242239.64159797
 */
printf("uniqid('', true): %s\r\n", uniqid('', true));
?>
```

### 注释

> **Note**:
>
> 在Cygwin环境下，为了使此函数能够工作，`more_entropy` 必须设置为
> **`TRUE`**。

unpack
======

Unpack data from binary string

### 说明

<span class="type">array</span> <span class="methodname">unpack</span> (
<span class="methodparam"><span class="type">string</span>
`$format`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`<span
class="initializer"> = 0</span></span> \] )

Unpacks from a binary string into an array according to the given
`format`.

The unpacked data is stored in an associative array. To accomplish this
you have to name the different format codes and separate them by a slash
/. If a repeater argument is present, then each of the array keys will
have a sequence number behind the given name.

### 参数

`format`  
See <span class="function">pack</span> for an explanation of the format
codes.

`data`  
The packed data.

`offset`  
The offset to begin unpacking from.

### 返回值

Returns an associative array containing unpacked elements of binary
string.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>7.2.0</td>
<td><span class="type">float</span> and <span class="type">double</span> types supports both Big Endian and Little Endian.</td>
</tr>
<tr class="even">
<td>7.1.0</td>
<td>The optional <code class="parameter">offset</code> has been added.</td>
</tr>
<tr class="odd">
<td>5.5.0</td>
<td><p>Changes were made to bring this function into line with Perl:</p>
<p>The "a" code now retains trailing NULL bytes.</p>
<p>The "A" code now strips all trailing ASCII whitespace (spaces, tabs, newlines, carriage returns, and NULL bytes).</p>
<p>The "Z" code was added for NULL-padded strings, and removes trailing NULL bytes.</p></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span class="function">unpack</span> example**

``` php
<?php
$binarydata = "\x04\x00\xa0\x00";
$array = unpack("cchars/nint", $binarydata);
print_r($array);
?>
```

以上例程会输出：

    Array
    (
        [chars] => 4
        [int] => 160
    )

**示例 \#2 <span class="function">unpack</span> example with a
repeater**

``` php
<?php
$binarydata = "\x04\x00\xa0\x00";
$array = unpack("c2chars/nint", $binarydata);
print_r($array);
?>
```

以上例程会输出：

    Array
    (
        [chars1] => 4
        [chars2] => 0
        [int] => 40960
    )

### 注释

**Caution**

Note that PHP internally stores integral values as signed. If you unpack
a large unsigned long and it is of the same size as PHP internally
stored values the result will be a negative number even though unsigned
unpacking was specified.

**Caution**

If you do not name an element, numeric indices starting from *1* are
used. Be aware that if you have more than one unnamed element, some data
is overwritten because the numbering restarts from *1* for each element.

**示例 \#3 <span class="function">unpack</span> example with unnamed
keys**

``` php
<?php
$binarydata = "\x32\x42\x00\xa0";
$array = unpack("c2/n", $binarydata);
var_dump($array);
?>
```

以上例程会输出：

    array(2) {
      [1]=>
      int(160)
      [2]=>
      int(66)
    }

Note that the first value from the *c* specifier is overwritten by the
first value from the *n* specifier.

### 参见

-   <span class="function">pack</span>

usleep
======

以指定的微秒数延迟执行

### 说明

<span class="type">void</span> <span class="methodname">usleep</span> (
<span class="methodparam"><span class="type">int</span>
`$micro_seconds`</span> )

以指定的微秒数延缓程序的执行。

### 参数

`micro_seconds`  
暂停的时间以微秒计。1微秒（micro second）是百万分之一秒。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">usleep</span>例子**

``` php
<?php

// Current time
echo date('h:i:s') . "\n";

// wait for 2 seconds
usleep(2000000);

// back!
echo date('h:i:s') . "\n";

?>
```

以上例程会输出：

    11:13:28
    11:13:30

### 参见

-   <span class="function">sleep</span>
-   <span class="function">time\_nanosleep</span>
-   <span class="function">time\_sleep\_until</span>
-   <span class="function">set\_time\_limit</span>

**目录**

-   [connection\_aborted](/ref/misc.html#connection_aborted) —
    检查客户端是否已经断开
-   [connection\_status](/ref/misc.html#connection_status) —
    返回连接的状态位
-   [constant](/ref/misc.html#constant) — 返回一个常量的值
-   [define](/ref/misc.html#define) — 定义一个常量
-   [defined](/ref/misc.html#defined) — 检查某个名称的常量是否存在
-   [die](/ref/misc.html#die) — 等同于 exit
-   [eval](/ref/misc.html#eval) — 把字符串作为PHP代码执行
-   [exit](/ref/misc.html#exit) — 输出一个消息并且退出当前脚本
-   [get\_browser](/ref/misc.html#get_browser) — 获取浏览器具有的功能
-   [\_\_halt\_compiler](/ref/misc.html#__halt_compiler) —
    中断编译器的执行
-   [highlight\_file](/ref/misc.html#highlight_file) — 语法高亮一个文件
-   [highlight\_string](/ref/misc.html#highlight_string) —
    字符串的语法高亮
-   [hrtime](/ref/misc.html#hrtime) — Get the system's high resolution
    time
-   [ignore\_user\_abort](/ref/misc.html#ignore_user_abort) —
    设置客户端断开连接时是否中断脚本的执行
-   [pack](/ref/misc.html#pack) — 将数据打包成二进制字符串
-   [php\_check\_syntax](/ref/misc.html#php_check_syntax) —
    检查PHP的语法（并执行）指定的文件
-   [php\_strip\_whitespace](/ref/misc.html#php_strip_whitespace) —
    返回删除注释和空格后的PHP源码
-   [sapi\_windows\_cp\_conv](/ref/misc.html#sapi_windows_cp_conv) —
    Convert string from one codepage to another
-   [sapi\_windows\_cp\_get](/ref/misc.html#sapi_windows_cp_get) — Get
    process codepage
-   [sapi\_windows\_cp\_is\_utf8](/ref/misc.html#sapi_windows_cp_is_utf8)
    — Indicates whether the codepage is UTF-8 compatible
-   [sapi\_windows\_cp\_set](/ref/misc.html#sapi_windows_cp_set) — Set
    process codepage
-   [sapi\_windows\_generate\_ctrl\_event](/ref/misc.html#sapi_windows_generate_ctrl_event)
    — Send a CTRL event to another process
-   [sapi\_windows\_set\_ctrl\_handler](/ref/misc.html#sapi_windows_set_ctrl_handler)
    — Set or remove a CTRL event handler
-   [sapi\_windows\_vt100\_support](/ref/misc.html#sapi_windows_vt100_support)
    — Get or set VT100 support for the specified stream associated to an
    output buffer of a Windows console.
-   [show\_source](/ref/misc.html#show_source) — 别名 highlight\_file
-   [sleep](/ref/misc.html#sleep) — 延缓执行
-   [sys\_getloadavg](/ref/misc.html#sys_getloadavg) —
    获取系统的负载（load average）
-   [time\_nanosleep](/ref/misc.html#time_nanosleep) —
    延缓执行若干秒和纳秒
-   [time\_sleep\_until](/ref/misc.html#time_sleep_until) —
    使脚本睡眠到指定的时间为止。
-   [uniqid](/ref/misc.html#uniqid) — 生成一个唯一ID
-   [unpack](/ref/misc.html#unpack) — Unpack data from binary string
-   [usleep](/ref/misc.html#usleep) — 以指定的微秒数延迟执行
