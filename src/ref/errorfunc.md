参见 <span class="function">syslog</span>.

debug\_backtrace
================

产生一条回溯跟踪(backtrace)

### 说明

<span class="type">array</span> <span
class="methodname">debug\_backtrace</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = DEBUG\_BACKTRACE\_PROVIDE\_OBJECT</span></span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = 0</span></span> \]\] )

<span class="function">debug\_backtrace</span> 产生一条 PHP
的回溯跟踪(backtrace)。

### 参数

`options`  
截至 5.3.6，这个参数是以下选项的位掩码：

|                                   |                                                                               |
|-----------------------------------|-------------------------------------------------------------------------------|
| DEBUG\_BACKTRACE\_PROVIDE\_OBJECT | 是否填充 "object" 的索引。                                                    |
| DEBUG\_BACKTRACE\_IGNORE\_ARGS    | 是否忽略 "args" 的索引，包括所有的 function/method 的参数，能够节省内存开销。 |

在 5.3.6 之前，仅仅能使用的值是 **`TRUE`** 或者
**`FALSE`**，分别等于是否设置 **`DEBUG_BACKTRACE_PROVIDE_OBJECT`**
选项。

`limit`  
截至 5.4.0，这个参数能够用于限制返回堆栈帧的数量。 默认为 (`limit`=*0*)
，返回所有的堆栈帧。

### 返回值

返回一个包含众多关联数组的 <span class="type">array</span>。
以下为有可能返回的元素：

| 名字     | 类型                              | 说明                                                                                                                                            |
|----------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| function | <span class="type">string</span>  | 当前的函数名，参见： <a href="/language/constants/predefined.html" class="link">__FUNCTION__</a>。                                              |
| line     | <span class="type">integer</span> | 当前的行号。参见： <a href="/language/constants/predefined.html" class="link">__LINE__</a>。                                                    |
| file     | <span class="type">string</span>  | 当前的文件名。参见： <a href="/language/constants/predefined.html" class="link">__FILE__</a>。                                                  |
| class    | <span class="type">string</span>  | 当前 <a href="/language/oop5.html" class="link">class</a> 的名称。参见 <a href="/language/constants/predefined.html" class="link">__CLASS__</a> |
| object   | <span class="type">object</span>  | 当前的 <a href="/language/oop5.html" class="link">object</a>。                                                                                  |
| type     | <span class="type">string</span>  | 当前调用的类型。如果是一个方法，会返回 "-\>"。如果是一个静态方法，会返回 "::"。 如果是一个函数调用，则返回空。                                  |
| args     | <span class="type">array</span>   | 如果在一个函数里，这会列出函数的参数。 如果是在一个被包含的文件里，会列出包含的文件名。                                                         |

### 更新日志

| 版本  | 说明                                                                                         |
|-------|----------------------------------------------------------------------------------------------|
| 5.4.0 | 添加了可选的参数 `limit`。                                                                   |
| 5.3.6 | 参数 `provide_object` 改成 `options`，并且增加了可选参数 **`DEBUG_BACKTRACE_IGNORE_ARGS`**。 |
| 5.2.5 | 添加了可选参数 `provide_object`。                                                            |
| 5.1.1 | 添加了当前的 <span class="type">object</span> 为可能返回的元素。                             |

### 范例

**示例 \#1 <span class="function">debug\_backtrace</span> 范例**

``` php
<?php
// filename: /tmp/a.php

function a_test($str)
{
    echo "\nHi: $str";
    var_dump(debug_backtrace());
}

a_test('friend');
?>

<?php
// filename: /tmp/b.php
include_once '/tmp/a.php';
?>
```

执行 `/tmp/b.php` 返回的结果类似于以下：

    Hi: friend
    array(2) {
    [0]=>
    array(4) {
        ["file"] => string(10) "/tmp/a.php"
        ["line"] => int(10)
        ["function"] => string(6) "a_test"
        ["args"]=>
        array(1) {
          [0] => &string(6) "friend"
        }
    }
    [1]=>
    array(4) {
        ["file"] => string(10) "/tmp/b.php"
        ["line"] => int(2)
        ["args"] =>
        array(1) {
          [0] => string(10) "/tmp/a.php"
        }
        ["function"] => string(12) "include_once"
      }
    }

### 参见

-   <span class="function">trigger\_error</span>
-   <span class="function">debug\_print\_backtrace</span>

debug\_print\_backtrace
=======================

打印一条回溯。

### 说明

<span class="type">void</span> <span
class="methodname">debug\_print\_backtrace</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$limit`<span
class="initializer"> = 0</span></span> \]\] )

<span class="function">debug\_print\_backtrace</span> 打印了一条 PHP
回溯。它打印了函数调用、被 included/required 的文件和 <span
class="function">eval</span> 的代码。

### 参数

`options`  
从 5.3.6 开始，这个参数是以下选项的位掩码：

|                                |                                                                               |
|--------------------------------|-------------------------------------------------------------------------------|
| DEBUG\_BACKTRACE\_IGNORE\_ARGS | 是否忽略 "args" 的索引，包括所有的 function/method 的参数，能够节省内存开销。 |

`limit`  
从 5.4.0 开始，这个参数能够用于限制返回堆栈帧的数量。 默认为
(`limit`=*0*) ，返回所有的堆栈帧。

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                         |
|-------|------------------------------|
| 5.4.0 | 添加了可选的参数 `limit`。   |
| 5.3.6 | 添加了可选的参数 `options`。 |

### 范例

**示例 \#1 <span class="function">debug\_print\_backtrace</span> 范例**

``` php
<?php
// include.php file

function a() {
    b();
}

function b() {
    c();
}

function c(){
    debug_print_backtrace();
}

a();

?>
```

``` php
<?php
// 文件 test.php
// 这是你应该运行的文件

include 'include.php';
?>
```

以上例程的输出类似于：

    #0  c() called at [/tmp/include.php:10]
    #1  b() called at [/tmp/include.php:6]
    #2  a() called at [/tmp/include.php:17]
    #3  include(/tmp/include.php) called at [/tmp/test.php:3]

### 参见

-   <span class="function">debug\_backtrace</span>

error\_clear\_last
==================

清除最近一次错误

### 说明

<span class="type">void</span> <span
class="methodname">error\_clear\_last</span> ( <span
class="methodparam">void</span> )

### 返回值

清除最近一次错误，使它无法通过 <span
class="function">error\_get\_last</span> 获取。

### 范例

**示例 \#1 <span class="function">error\_clear\_last</span> 例子**

``` php
<?php
var_dump(error_get_last());
error_clear_last();
var_dump(error_get_last());

@$a = $b;

var_dump(error_get_last());
error_clear_last();
var_dump(error_get_last());
?>
```

以上例程的输出类似于：

    NULL
    NULL
    array(4) {
      ["type"]=>
      int(8)
      ["message"]=>
      string(21) "Undefined variable: b"
      ["file"]=>
      string(9) "%s"
      ["line"]=>
      int(6)
    }
    NULL

### 参见

-   <a href="/errorfunc/constants.html" class="link">Error 常量</a>

error\_get\_last
================

获取最后发生的错误

### 说明

<span class="type">array</span> <span
class="methodname">error\_get\_last</span> ( <span
class="methodparam">void</span> )

获取关于最后一个发生的错误的信息。

### 返回值

返回了一个关联数组，描述了最后错误的信息，以该错误的 "type"、
"message"、"file" 和 "line" 为数组的键。 如果该错误由 PHP
内置函数导致的，"message"会以该函数名开头。 如果还没有错误则返回
**`NULL`**。

### 范例

**示例 \#1 An <span class="function">error\_get\_last</span> 范例**

``` php
<?php
echo $a;
print_r(error_get_last());
?>
```

以上例程的输出类似于：

    Array
    (
        [type] => 8
        [message] => Undefined variable: a
        [file] => C:\WWW\index.php
        [line] => 2
    )

### 参见

-   <a href="/errorfunc/constants.html" class="link">Error 常量</a>
-   `$php_errormsg` 变量
-   <span class="function">error\_clear\_last</span>
-   <a href="/errorfunc/setup.html#" class="link"><code class="parameter">display_errors</code> 指令</a>
-   <a href="/errorfunc/setup.html#" class="link"><code class="parameter">html_errors</code> 指令</a>
-   <a href="/errorfunc/setup.html#" class="link"><code class="parameter">xmlrpc_errors</code> 指令</a>

error\_log
==========

发送错误信息到某个地方

### 说明

<span class="type">bool</span> <span
class="methodname">error\_log</span> ( <span class="methodparam"><span
class="type">string</span> `$message`</span> \[, <span
class="methodparam"><span class="type">int</span> `$message_type`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span>
`$destination`</span> \[, <span class="methodparam"><span
class="type">string</span> `$extra_headers`</span> \]\]\] )

把错误信息发送到 web 服务器的错误日志，或者到一个文件里。

### 参数

`message`  
应该被记录的错误信息。

`message_type`  
设置错误应该发送到何处。可能的信息类型有以下几个：

|     |                                                                                                                                                                              |
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0   | `message` 发送到 PHP 的系统日志，使用 操作系统的日志机制或者一个文件，取决于 <a href="/errorfunc/setup.html#" class="link">error_log</a> 指令设置了什么。 这是个默认的选项。 |
| 1   | `message` 发送到参数 `destination` 设置的邮件地址。 第四个参数 `extra_headers` 只有在这个类型里才会被用到。                                                                  |
| 2   | 不再是一个选项。                                                                                                                                                             |
| 3   | `message` 被发送到位置为 `destination` 的文件里。 字符 `message` 不会默认被当做新的一行。                                                                                    |
| 4   | `message` 直接发送到 SAPI 的日志处理程序中。                                                                                                                                 |

`destination`  
目标。它的含义描述于以上，由 `message_type` 参数所决定。

`extra_headers`  
额外的头。当 `message_type` 设置为 *1* 的时候使用。 该信息类型使用了
<span class="function">mail</span> 的同一个内置函数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

<span class="function">error\_log</span> 并非二进制安全的。null
字符可能截断 `message`。

**小贴士**

`message` 不能包含 null 字符。 注意，`message`
可能会发送到文件、邮件、syslog 等。 所以在调用 <span
class="function">error\_log</span> 前需要使用适合的转换/转义函数： <span
class="function">base64\_encode</span>、 <span
class="function">rawurlencode</span> 或 <span
class="function">addslashes</span>。

### 范例

**示例 \#1 <span class="function">error\_log</span> 范例**

``` php
<?php
// 如果无法连接到数据库，发送通知到服务器日志
if (!Ora_Logon($username, $password)) {
    error_log("Oracle database not available!", 0);
}

// 如果用尽了 FOO，通过邮件通知管理员
if (!($foo = allocate_new_foo())) {
    error_log("Big trouble, we're all out of FOOs!", 1,
               "operator@example.com");
}

// 调用 error_log() 的另一种方式:
error_log("You messed up!", 3, "/var/tmp/my-errors.log");
?>
```

### 更新日志

| 版本  | 说明                                 |
|-------|--------------------------------------|
| 5.2.7 | 可能的值：4添加到了 `message_type`。 |

error\_reporting
================

设置应该报告何种 PHP 错误

### 说明

<span class="type">int</span> <span
class="methodname">error\_reporting</span> (\[ <span
class="methodparam"><span class="type">int</span> `$level`</span> \] )

<span class="function">error\_reporting</span> 函数能够在运行时设置
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
指令。 PHP 有诸多错误级别，使用该函数可以设置在脚本运行时的级别。
如果没有设置可选参数 `level`， <span
class="function">error\_reporting</span> 仅会返回当前的错误报告级别。

### 参数

`level`  
新的
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
级别。 可以是一个位掩码也可以是一个已命名的常量。
强烈建议使用已命名的常量，以确保兼容将来的版本。
由于错误级别的添加、整数取值范围的增加，
较久的基于整数的错误级别不会总是和预期的表现一致。

可用的错误级别常量及其实际含义描述在了
<a href="/errorfunc/constants.html" class="link">predefined constants</a>
中。

### 返回值

返回旧的
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
级别，或者在 `level` 参数未给出时返回当前的级别。

### 更新日志

| 版本  | 说明                                                 |
|-------|------------------------------------------------------|
| 5.4.0 | **`E_STRICT`** 成为 **`E_ALL`** 的一部分             |
| 5.3.0 | 引入 **`E_DEPRECATED`** 和 **`E_USER_DEPRECATED`**。 |
| 5.2.0 | 引入 **`E_RECOVERABLE_ERROR`**。                     |

### 范例

**示例 \#1 <span class="function">error\_reporting</span> 范例**

``` php
<?php

// 关闭所有PHP错误报告
error_reporting(0);

// Report simple running errors
error_reporting(E_ERROR | E_WARNING | E_PARSE);

// 报告 E_NOTICE也挺好 (报告未初始化的变量
// 或者捕获变量名的错误拼写)
error_reporting(E_ERROR | E_WARNING | E_PARSE | E_NOTICE);

// 除了 E_NOTICE，报告其他所有错误
error_reporting(E_ALL ^ E_NOTICE);

// 报告所有 PHP 错误 (参见 changelog)
error_reporting(E_ALL);

// 报告所有 PHP 错误
error_reporting(-1);

// 和 error_reporting(E_ALL); 一样
ini_set('error_reporting', E_ALL);

?>
```

### 注释

**Warning**

虽然
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
增强了 包含 **`E_STRICT`** 错误的能力（反之亦然），但大多数
**`E_STRICT`** 的错误是在编译时被评估的， 所以不会在文件中被报告。

**小贴士**

传入 *-1* 的值将尽可能显示所有错误， 甚至包括将来 PHP
可能加入的新的错误级别和常量。 至 PHP 5.4，常量 **`E_ALL`**
有同样的行为。

### 参见

-   <a href="/errorfunc/setup.html#" class="link">display_errors</a>
    指令
-   <a href="/errorfunc/setup.html#" class="link">html_errors</a> 指令
-   <a href="/errorfunc/setup.html#" class="link">xmlrpc_errors</a> 指令
-   <span class="function">ini\_set</span>

restore\_error\_handler
=======================

还原之前的错误处理函数

### 说明

<span class="type">bool</span> <span
class="methodname">restore\_error\_handler</span> ( <span
class="methodparam">void</span> )

在使用 <span class="function">set\_error\_handler</span>
改变错误处理函数之后，此函数可以
用于还原之前的错误处理程序(可以是内置的或者也可以是用户所定义的函数)。

### 返回值

该函数总是返回 **`TRUE`**。

### 范例

**示例 \#1 <span class="function">restore\_error\_handler</span> 范例**

如果是 <span class="function">unserialize</span> 导致了一个错误，接下来
会恢复原来的错误处理函数。

``` php
<?php
function unserialize_handler($errno, $errstr)
{
    echo "Invalid serialized value.\n";
}

$serialized = 'foo';
set_error_handler('unserialize_handler');
$original = unserialize($serialized);
restore_error_handler();
?>
```

以上例程会输出：

    Invalid serialized value.

### 参见

-   <span class="function">error\_reporting</span>
-   <span class="function">set\_error\_handler</span>
-   <span class="function">restore\_exception\_handler</span>
-   <span class="function">trigger\_error</span>

restore\_exception\_handler
===========================

恢复之前定义过的异常处理函数。

### 说明

<span class="type">bool</span> <span
class="methodname">restore\_exception\_handler</span> ( <span
class="methodparam">void</span> )

在使用 <span class="function">set\_exception\_handler</span>
改变异常处理函数之后，此函数可以
用于还原之前的异常处理程序(可以是内置的或者也可以是用户所定义的函数)。

### 返回值

该函数总是返回 **`TRUE`**。

### 范例

**示例 \#1 <span class="function">restore\_exception\_handler</span>
范例**

``` php
<?php
    function exception_handler_1(Exception $e)
    {
        echo '[' . __FUNCTION__ . '] ' . $e->getMessage();
    }

    function exception_handler_2(Exception $e)
    {
        echo '[' . __FUNCTION__ . '] ' . $e->getMessage();
    }

    set_exception_handler('exception_handler_1');
    set_exception_handler('exception_handler_2');

    restore_exception_handler();

    throw new Exception('This triggers the first exception handler...');
?>
```

以上例程会输出：

    [exception_handler_1] This triggers the first exception handler...

### 参见

-   <span class="function">set\_exception\_handler</span>
-   <span class="function">set\_error\_handler</span>
-   <span class="function">restore\_error\_handler</span>
-   <span class="function">error\_reporting</span>

set\_error\_handler
===================

设置用户自定义的错误处理函数

### 说明

<span class="type">mixed</span> <span
class="methodname">set\_error\_handler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$error_handler`</span> \[, <span class="methodparam"><span
class="type">int</span> `$error_types`<span class="initializer"> =
E\_ALL \| E\_STRICT</span></span> \] )

设置用户的函数 (`error_handler`) 来处理脚本中出现的错误。

本函数可以用你自己定义的方式来处理运行中的错误，
例如，在应用程序中严重错误发生时，或者在特定条件下触发了一个错误(使用
<span
class="function">trigger\_error</span>)，你需要对数据/文件做清理回收。

重要的是要记住 `error_types` 里指定的错误类型都会绕过 PHP
标准错误处理程序， 除非回调函数返回了 **`FALSE`**。 <span
class="function">error\_reporting</span>
设置将不会起到作用而你的错误处理函数继续会被调用 —— 不过你仍然可以获取
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
的当前值，并做适当处理。 需要特别注意的是带
<a href="/language/operators/errorcontrol.html" class="link">@ error-control operator</a>
前缀的语句发生错误时，这个值会是 0。

同时注意，在需要时你有责任使用 <span class="function">die</span>。
如果错误处理程序返回了，脚本将会继续执行发生错误的后一行。

以下级别的错误不能由用户定义的函数来处理，独立于发生错误的地方：
**`E_ERROR`**、 **`E_PARSE`**、 **`E_CORE_ERROR`**、
**`E_CORE_WARNING`**、 **`E_COMPILE_ERROR`**、
**`E_COMPILE_WARNING`**，和在 调用 <span
class="function">set\_error\_handler</span> 函数所在文件中产生的大多数
**`E_STRICT`**。

如果错误发生在脚本执行之前（比如文件上传时），将不会
调用自定义的错误处理程序因为它尚未在那时注册。

### 参数

`error_handler`  
以下格式的回调（callback）： 可以传入 **`NULL`**
重置处理程序到默认状态。
除了可以传入函数名，还可以传入引用对象和对象方法名的数组。

<span class="type">bool</span> <span class="methodname"><span
class="replaceable">handler</span></span> ( <span
class="methodparam"><span class="type">int</span> `$errno`</span> ,
<span class="methodparam"><span class="type">string</span>
`$errstr`</span> \[, <span class="methodparam"><span
class="type">string</span> `$errfile`</span> \[, <span
class="methodparam"><span class="type">int</span> `$errline`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$errcontext`</span> \]\]\] )

`errno`  
<span class="simpara"> 第一个参数 `errno`，包含了错误的级别，是一个
integer。 </span>

`errstr`  
<span class="simpara"> 第二个参数 `errstr`，包含了错误的信息，是一个
string。 </span>

`errfile`  
<span class="simpara"> 第三个参数是可选的，`errfile`，
包含了发生错误的文件名，是一个 string。 </span>

`errline`  
<span class="simpara"> 第四个参数是一个可选项， `errline`，
包含了错误发生的行号，是一个 integer。 </span>

`errcontext`  
<span class="simpara"> 第五个可选参数， `errcontext`，
是一个指向错误发生时活动符号表的 array。 也就是说，`errcontext`
会包含错误触发处作用域内所有变量的数组。
用户的错误处理程序不应该修改错误上下文（context）。 </span>

**Warning**
PHP 7.2.0 后此参数被*弃用*了。 极其不建议依赖它。

如果函数返回 **`FALSE`**，标准错误处理处理程序将会继续调用。

`error_types`  
就像<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
的 ini 设置能够控制错误的显示一样， 此参数能够用于屏蔽 `error_handler`
的触发。 如果没有该掩码， 无论
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
是如何设置的， `error_handler` 都会在每个错误发生时被调用。

### 返回值

如果之前有定义过错误处理程序，则返回该程序名称的
string；如果是内置的错误处理程序，则返回 **`NULL`**。
如果你指定了一个无效的回调函数，同样会返回 **`NULL`**。
如果之前的错误处理程序是一个类的方法，此函数会返回一个带类和方法名的索引数组(indexed
array)。

### 更新日志

| 版本  | 说明                                                               |
|-------|--------------------------------------------------------------------|
| 7.2.0 | `errcontext` 被废弃。 使用此参数时会导致 **`E_DEPRECATED`** 提醒。 |

### 范例

**示例 \#1 用 <span class="function">set\_error\_handler</span> 和 <span
class="function">trigger\_error</span> 进行错误处理**

以下示例展示了通过触发错误并以用户自定义的程序来进行内部异常的处理。

``` php
<?php
// error handler function
function myErrorHandler($errno, $errstr, $errfile, $errline)
{
    if (!(error_reporting() & $errno)) {
        // This error code is not included in error_reporting, so let it fall
        // through to the standard PHP error handler
        return false;
    }

    // $errstr may need to be escaped:
    $errstr = htmlspecialchars($errstr);

    switch ($errno) {
    case E_USER_ERROR:
        echo "<b>My ERROR</b> [$errno] $errstr<br />\n";
        echo "  Fatal error on line $errline in file $errfile";
        echo ", PHP " . PHP_VERSION . " (" . PHP_OS . ")<br />\n";
        echo "Aborting...<br />\n";
        exit(1);

    case E_USER_WARNING:
        echo "<b>My WARNING</b> [$errno] $errstr<br />\n";
        break;

    case E_USER_NOTICE:
        echo "<b>My NOTICE</b> [$errno] $errstr<br />\n";
        break;

    default:
        echo "Unknown error type: [$errno] $errstr<br />\n";
        break;
    }

    /* Don't execute PHP internal error handler */
    return true;
}

// function to test the error handling
function scale_by_log($vect, $scale)
{
    if (!is_numeric($scale) || $scale <= 0) {
        trigger_error("log(x) for x <= 0 is undefined, you used: scale = $scale", E_USER_ERROR);
    }

    if (!is_array($vect)) {
        trigger_error("Incorrect input vector, array of values expected", E_USER_WARNING);
        return null;
    }

    $temp = array();
    foreach($vect as $pos => $value) {
        if (!is_numeric($value)) {
            trigger_error("Value at position $pos is not a number, using 0 (zero)", E_USER_NOTICE);
            $value = 0;
        }
        $temp[$pos] = log($scale) * $value;
    }

    return $temp;
}

// set to the user defined error handler
$old_error_handler = set_error_handler("myErrorHandler");

// trigger some errors, first define a mixed array with a non-numeric item
echo "vector a\n";
$a = array(2, 3, "foo", 5.5, 43.3, 21.11);
print_r($a);

// now generate second array
echo "----\nvector b - a notice (b = log(PI) * a)\n";
/* Value at position $pos is not a number, using 0 (zero) */
$b = scale_by_log($a, M_PI);
print_r($b);

// this is trouble, we pass a string instead of an array
echo "----\nvector c - a warning\n";
/* Incorrect input vector, array of values expected */
$c = scale_by_log("not array", 2.3);
var_dump($c); // NULL

// this is a critical error, log of zero or negative number is undefined
echo "----\nvector d - fatal error\n";
/* log(x) for x <= 0 is undefined, you used: scale = $scale" */
$d = scale_by_log($a, -2.5);
var_dump($d); // Never reached
?>
```

以上例程的输出类似于：

    vector a
    Array
    (
        [0] => 2
        [1] => 3
        [2] => foo
        [3] => 5.5
        [4] => 43.3
        [5] => 21.11
    )
    ----
    vector b - a notice (b = log(PI) * a)
    <b>My NOTICE</b> [1024] Value at position 2 is not a number, using 0 (zero)<br />
    Array
    (
        [0] => 2.2894597716988
        [1] => 3.4341896575482
        [2] => 0
        [3] => 6.2960143721717
        [4] => 49.566804057279
        [5] => 24.165247890281
    )
    ----
    vector c - a warning
    <b>My WARNING</b> [512] Incorrect input vector, array of values expected<br />
    NULL
    ----
    vector d - fatal error
    <b>My ERROR</b> [256] log(x) for x <= 0 is undefined, you used: scale = -2.5<br />
      Fatal error on line 35 in file trigger_error.php, PHP 5.2.1 (FreeBSD)<br />
    Aborting...<br />

### 参见

-   <span class="classname">ErrorException</span>
-   <span class="function">error\_reporting</span>
-   <span class="function">restore\_error\_handler</span>
-   <span class="function">trigger\_error</span>
-   <a href="/errorfunc/constants.html" class="link">error level constants</a>

set\_exception\_handler
=======================

设置用户自定义的异常处理函数

### 说明

<span class="type">callable</span> <span
class="methodname">set\_exception\_handler</span> ( <span
class="methodparam"><span class="type">callable</span>
`$exception_handler`</span> )

设置默认的异常处理程序，用于没有用 try/catch 块来捕获的异常。 在
`exception_handler` 调用后异常会中止。

### 参数

`exception_handler`  
当一个未捕获的异常发生时所调用函数的名称。
该处理函数需要接受一个参数，该参数是一个抛出的异常对象。 PHP 7
以前的异常处理程序签名：

<span class="type">void</span> <span class="methodname"><span
class="replaceable">handler</span></span> ( <span
class="methodparam"><span class="type">Exception</span> `$ex`</span> )

自 PHP 7 以来，大多数错误抛出 <span class="classname">Error</span>
异常，也能被捕获。 <span class="classname">Error</span> 和 <span
class="classname">Exception</span> 都实现了 <span
class="classname">Throwable</span> 接口。 PHP 7 起，处理程序的签名：

<span class="type">void</span> <span class="methodname"><span
class="replaceable">handler</span></span> ( <span
class="methodparam"><span class="type">Throwable</span> `$ex`</span> )

也可以传递 **`NULL`** 值用于重置异常处理函数为默认值。

**Caution**
注意，如果在用户回调里将 `ex` 参数的类型明确约束为<span
class="classname">Exception</span>， PHP 7
中由于异常类型的变化，将会产生问题。

### 返回值

返回之前定义的异常处理程序的名称，或者在错误时返回 **`NULL`**。
如果之前没有定义错误处理程序，也会返回 **`NULL`**。

### 更新日志

| 版本  | 说明                                                                                                                     |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| 7.0.0 | 传入 `exception_handler` 的参数从 <span class="classname">Exception</span> 改为 <span class="classname">Throwable</span> |
| 5.5.0 | 之前版本里，如果传入 **`NULL`** ，函数会返回 **`TRUE`**。 自 PHP 5.5.0 后，会返回上一次的异常处理器。                    |

### 范例

**示例 \#1 <span class="function">set\_exception\_handler</span> 范例**

``` php
<?php
function exception_handler($exception) {
  echo "Uncaught exception: " , $exception->getMessage(), "\n";
}

set_exception_handler('exception_handler');

throw new Exception('Uncaught Exception');
echo "Not Executed\n";
?>
```

### 参见

-   <span class="function">restore\_exception\_handler</span>
-   <span class="function">restore\_error\_handler</span>
-   <span class="function">error\_reporting</span>
-   <a href="/language/exceptions.html" class="link">PHP 5 异常</a>

trigger\_error
==============

产生一个用户级别的 error/warning/notice 信息

### 说明

<span class="type">bool</span> <span
class="methodname">trigger\_error</span> ( <span
class="methodparam"><span class="type">string</span> `$error_msg`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$error_type`<span class="initializer"> = E\_USER\_NOTICE</span></span>
\] )

用于触发一个用户级别的错误条件，它能结合内置的错误处理器所关联，或者可以使用用户定义的函数作为新的错误处理程序(<span
class="function">set\_error\_handler</span>)。

该函数在你运行出现异常时，需要产生一个特定的响应时非常有用。

### 参数

`error_msg`  
该 error 的特定错误信息，长度限制在了 1024 个字节。超过 1024
字节的字符都会被截断。

`error_type`  
该 error 所特定的错误类型。仅 E\_USER 系列常量对其有效，默认是
**`E_USER_NOTICE`**。

### 返回值

如果指定了错误的 `error_type` 会返回 **`FALSE`** ，正确则返回
**`TRUE`**。

### 范例

**示例 \#1 <span class="function">trigger\_error</span> 示例**

<span class="function">set\_error\_handler</span> 可见到更多详细的例子。

``` php
<?php
if ($divisor == 0) {
    trigger_error("Cannot divide by zero", E_USER_ERROR);
}
?>
```

### 注释

**Warning**

在 `error_msg` 里的HTML实体 并不会被转义。
如果错误消息要显示在浏览器里，需要对错误消息使用 <span
class="function">htmlentities</span>。

### 参见

-   <span class="function">error\_reporting</span>
-   <span class="function">set\_error\_handler</span>
-   <span class="function">restore\_error\_handler</span>
-   The
    <a href="/errorfunc/constants.html" class="link">错误级别常量</a>

user\_error
===========

<span class="function">trigger\_error</span> 的别名

### 说明

此函数是该函数的别名： <span class="function">trigger\_error</span>.

**目录**

-   [debug\_backtrace](/ref/errorfunc.html#debug_backtrace) —
    产生一条回溯跟踪(backtrace)
-   [debug\_print\_backtrace](/ref/errorfunc.html#debug_print_backtrace)
    — 打印一条回溯。
-   [error\_clear\_last](/ref/errorfunc.html#error_clear_last) —
    清除最近一次错误
-   [error\_get\_last](/ref/errorfunc.html#error_get_last) —
    获取最后发生的错误
-   [error\_log](/ref/errorfunc.html#error_log) — 发送错误信息到某个地方
-   [error\_reporting](/ref/errorfunc.html#error_reporting) —
    设置应该报告何种 PHP 错误
-   [restore\_error\_handler](/ref/errorfunc.html#restore_error_handler)
    — 还原之前的错误处理函数
-   [restore\_exception\_handler](/ref/errorfunc.html#restore_exception_handler)
    — 恢复之前定义过的异常处理函数。
-   [set\_error\_handler](/ref/errorfunc.html#set_error_handler) —
    设置用户自定义的错误处理函数
-   [set\_exception\_handler](/ref/errorfunc.html#set_exception_handler)
    — 设置用户自定义的异常处理函数
-   [trigger\_error](/ref/errorfunc.html#trigger_error) —
    产生一个用户级别的 error/warning/notice 信息
-   [user\_error](/ref/errorfunc.html#user_error) — trigger\_error
    的别名
