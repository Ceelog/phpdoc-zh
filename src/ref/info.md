assert\_options
===============

设置/获取断言的各种标志

### 说明

<span class="type">mixed</span> <span
class="methodname">assert\_options</span> ( <span
class="methodparam"><span class="type">int</span> `$what`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \] )

设置 <span class="function">assert</span>
的各种控制选项，或者是仅仅查询当前的设置。

### 参数

`what`  
| 标志                | INI 设置           | 默认值       | 描述                                           |
|---------------------|--------------------|--------------|------------------------------------------------|
| ASSERT\_ACTIVE      | assert.active      | 1            | 启用 <span class="function">assert</span> 断言 |
| ASSERT\_WARNING     | assert.warning     | 1            | 为每个失败的断言产生一个 PHP 警告（warning）   |
| ASSERT\_BAIL        | assert.bail        | 0            | 在断言失败时中止执行                           |
| ASSERT\_QUIET\_EVAL | assert.quiet\_eval | 0            | 在断言表达式求值时禁用 error\_reporting        |
| ASSERT\_CALLBACK    | assert.callback    | (**`NULL`**) | 断言失败时调用回调函数                         |

`value`  
标志的新值。

### 返回值

返回任意标志的原始设置，出错时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">assert\_options</span> 例子**

``` php
<?php
// 处理断言失败时的函数
function assert_failure()
{
    echo 'Assert failed';
}

// 我们的测试函数
function test_assert($parameter)
{
    assert(is_bool($parameter));
}

// 设置断言标志
assert_options(ASSERT_ACTIVE,   true);
assert_options(ASSERT_BAIL,     true);
assert_options(ASSERT_WARNING,  false);
assert_options(ASSERT_CALLBACK, 'assert_failure');

// 让一个断言会失败
test_assert(1);

// 由于 ASSERT_BAIL 是 true，这里永远也到不了
echo 'Never reached';
?>
```

### 参见

-   <span class="function">assert</span>

assert
======

检查一个断言是否为 **`FALSE`**

### 说明

PHP 5

<span class="type">bool</span> <span class="methodname">assert</span> (
<span class="methodparam"><span class="type">mixed</span>
`$assertion`</span> \[, <span class="methodparam"><span
class="type">string</span> `$description`</span> \] )

PHP 7

<span class="type">bool</span> <span class="methodname">assert</span> (
<span class="methodparam"><span class="type">mixed</span>
`$assertion`</span> \[, <span class="methodparam"><span
class="type">Throwable</span> `$exception`</span> \] )

<span class="function">assert</span> 会检查指定的 `assertion` 并在结果为
**`FALSE`** 时采取适当的行动。

#### Traditional assertions (PHP 5 and 7)

如果 `assertion` 是字符串，它将会被 <span class="function">assert</span>
当做 PHP 代码来执行。 `assertion`
是字符串的优势是当禁用断言时它的开销会更小，并且在断言失败时消息会包含
`assertion` 表达式。 这意味着如果你传入了 boolean 的条件作为
`assertion`，这个条件将不会显示为断言函数的参数；在调用你定义的 <span
class="function">assert\_options</span>
处理函数时，条件会转换为字符串，而布尔值 **`FALSE`**
会被转换成空字符串。

断言这个功能应该只被用来调试。
你应该用于完整性检查时测试条件是否始终应该为
**`TRUE`**，来指示某些程序错误，或者检查具体功能的存在（类似扩展函数或特定的系统限制和功能）。

断言不应该用于普通运行时操作，类似输入参数的检查。
作为一个经验法则，在断言禁用时你的代码也应该能够正确地运行。

<span class="function">assert</span> 的行为可以通过 <span
class="function">assert\_options</span> 来配置，或者手册页面上描述的
.ini 设置。

<span class="function">assert\_options</span> **`ASSERT_CALLBACK`**
配置指令允许设置回调函数来处理失败的断言。

<span class="function">assert</span>
回调函数在构建自动测试套件的时候尤其有用，因为它们允许你简易地捕获传入断言的代码，并包含断言的位置信息。
当信息能够被其他方法捕获，使用断言可以让它更快更方便！

回调函数应该接受三个参数。 第一个参数包括了断言失败所在的文件。
第二个参数包含了断言失败所在的行号，第三个参数包含了失败的表达式（如有任意
— 字面值例如 1 或者 "two" 将不会传递到这个参数）。 PHP 5.4.8
及更高版本的用户也可以提供第四个可选参数，如果设置了，用于将
`description` 指定到 <span class="function">assert</span>。

#### Expectations (PHP 7 only)

<span class="function">assert</span> is a language construct in PHP 7,
allowing for the definition of expectations: assertions that take effect
in development and testing environments, but are optimised away to have
zero cost in production.

While <span class="function">assert\_options</span> can still be used to
control behaviour as described above for backward compatibility reasons,
PHP 7 only code should use the two new configuration directives to
control the behaviour of <span class="function">assert</span> and not
call <span class="function">assert\_options</span>.

<table>
<caption> <strong>PHP 7 configuration directives for <span class="function">assert</span></strong> </caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Directive</th>
<th>Default value</th>
<th>Possible values</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a></td>
<td><em>1</em></td>
<td><ul>
<li><em>1</em>: generate and execute code (development mode)</li>
<li><em>0</em>: generate code but jump around it at runtime</li>
<li><em>-1</em>: do not generate code (production mode)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/info/setup.html#" class="link">assert.exception</a></td>
<td><em>0</em></td>
<td><ul>
<li><em>1</em>: throw when the assertion fails, either by throwing the object provided as the <code class="parameter">exception</code> or by throwing a new <span class="classname">AssertionError</span> object if <code class="parameter">exception</code> wasn't provided</li>
<li><em>0</em>: use or generate a <span class="classname">Throwable</span> as described above, but only generate a warning based on that object rather than throwing it (compatible with PHP 5 behaviour)</li>
</ul></td>
</tr>
</tbody>
</table>

### 参数

`assertion`  
断言。In PHP 5, this must be either a <span class="type">string</span>
to be evaluated or a <span class="type">boolean</span> to be tested. In
PHP 7, this may also be any expression that returns a value, which will
be executed and the result used to indicate whether the assertion
succeeded or failed.

`description`  
如果 `assertion` 失败了，选项 description 将会包括在失败信息里。

`exception`  
In PHP 7, the second parameter can be a <span
class="classname">Throwable</span> object instead of a descriptive <span
class="type">string</span>, in which case this is the object that will
be thrown if the assertion fails and the
<a href="/info/setup.html#" class="link">assert.exception</a>
configuration directive is enabled.

### 返回值

assertion 是 false 则返回 **`FALSE`**，否则是 **`TRUE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                               |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.0 | <span class="function">assert</span> is now a language construct and not a function. <span class="function">assertion</span> can now be an expression. The second parameter is now interpreted either as an `exception` (if a <span class="classname">Throwable</span> object is given), or as the `description` supported from PHP 5.4.8 onwards. |
| 5.4.8 | 增加了参数 `description`。 `description` 现在也作为第四个参数提供给 **`ASSERT_CALLBACK`** 模式里的回调函数。                                                                                                                                                                                                                                       |

### 范例

#### Traditional assertions (PHP 5 and 7)

**示例 \#1 使用自定义处理程序处理失败的断言**

``` php
<?php
// 激活断言，并设置它为 quiet
assert_options(ASSERT_ACTIVE, 1);
assert_options(ASSERT_WARNING, 0);
assert_options(ASSERT_QUIET_EVAL, 1);

//创建处理函数
function my_assert_handler($file, $line, $code)
{
    echo "<hr>Assertion Failed:
        File '$file'<br />
        Line '$line'<br />
        Code '$code'<br /><hr />";
}

// 设置回调函数
assert_options(ASSERT_CALLBACK, 'my_assert_handler');

// 让一则断言失败
assert('mysql_query("")');
?>
```

**示例 \#2 使用自定义处理器打印描述信息**

``` php
<?php
// 激活断言，并设置它为 quiet
assert_options(ASSERT_ACTIVE, 1);
assert_options(ASSERT_WARNING, 0);
assert_options(ASSERT_QUIET_EVAL, 1);

//创建处理函数
function my_assert_handler($file, $line, $code, $desc = null)
{
    echo "Assertion failed at $file:$line: $code";
    if ($desc) {
        echo ": $desc";
    }
    echo "\n";
}

// 设置回调函数
assert_options(ASSERT_CALLBACK, 'my_assert_handler');

// Make an assertion that should fail
assert('2 < 1');
assert('2 < 1', 'Two is less than one');
?>
```

以上例程会输出：

    Assertion failed at test.php:21: 2 < 1
    Assertion failed at test.php:22: 2 < 1: Two is less than one

#### Expectations (PHP 7 only)

**示例 \#3 Expectations without a custom exception**

``` php
<?php
assert(true == false);
echo 'Hi!';
?>
```

With
<a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
set to 0, the above example will output:

    Hi!

With
<a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
set to 1 and
<a href="/info/setup.html#" class="link">assert.exception</a> set to 0,
the above example will output:

    Warning: assert(): assert(true == false) failed in - on line 2
    Hi!

With
<a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
set to 1 and
<a href="/info/setup.html#" class="link">assert.exception</a> set to 1,
the above example will output:

    Fatal error: Uncaught AssertionError: assert(true == false) in -:2
    Stack trace:
    #0 -(2): assert(false, 'assert(true == ...')
    #1 {main}
      thrown in - on line 2

**示例 \#4 Expectations with a custom exception**

``` php
<?php
class CustomError extends AssertionError {}

assert(true == false, new CustomError('True is not false!'));
echo 'Hi!';
?>
```

With
<a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
set to 0, the above example will output:

    Hi!

With
<a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
set to 1 and
<a href="/info/setup.html#" class="link">assert.exception</a> set to 0,
the above example will output:

    Warning: assert(): CustomError: True is not false! in -:4
    Stack trace:
    #0 {main} failed in - on line 4
    Hi!

With
<a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
set to 1 and
<a href="/info/setup.html#" class="link">assert.exception</a> set to 1,
the above example will output:

    Fatal error: Uncaught CustomError: True is not false! in -:4
    Stack trace:
    #0 {main}
      thrown in - on line 4

### 参见

-   <span class="function">assert\_options</span>

cli\_get\_process\_title
========================

Returns the current process title

### 说明

<span class="type">string</span> <span
class="methodname">cli\_get\_process\_title</span> ( <span
class="methodparam">void</span> )

Returns the current process title, as set by <span
class="function">cli\_set\_process\_title</span>. Note that this may not
exactly match what is shown in **ps** or **top**, depending on your
operating system.

This function is available only in
<a href="/features/commandline.html" class="link">CLI</a> mode.

### 参数

此函数没有参数。

### 返回值

Return a string with the current process title or **`NULL`** on error.

### 错误／异常

An **`E_WARNING`** will be generated if the operating system is
unsupported.

### 范例

**示例 \#1 <span class="function">cli\_get\_process\_title</span>
example**

``` php
<?php
echo "Process title: " . cli_get_process_title() . "\n";
?>
```

### 参见

-   <span class="function">cli\_set\_process\_title</span>

cli\_set\_process\_title
========================

Sets the process title

### 说明

<span class="type">bool</span> <span
class="methodname">cli\_set\_process\_title</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> )

Sets the process title visible in tools such as **top** and **ps**. This
function is available only in
<a href="/features/commandline.html" class="link">CLI</a> mode.

### 参数

`title`  
The new title.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

An **`E_WARNING`** will be generated if the operating system is
unsupported.

### 范例

**示例 \#1 <span class="function">cli\_set\_process\_title</span>
example**

``` php
<?php
$title = "My Amazing PHP Script";
$pid = getmypid(); // you can use this to see your process title in ps

if (!cli_set_process_title($title)) {
    echo "Unable to set process title for PID $pid...\n";
    exit(1);
} else {
    echo "The process title '$title' for PID $pid has been set for your process!\n";
    sleep(5);
}
?>
```

### 参见

-   <span class="function">cli\_get\_process\_title</span>
-   <span class="function">setproctitle</span>

dl
==

运行时载入一个 PHP 扩展

### 说明

<span class="type">bool</span> <span class="methodname">dl</span> (
<span class="methodparam"><span class="type">string</span>
`$library`</span> )

载入指定参数 `library` 的 PHP 扩展。

使用 <span class="function">extension\_loaded</span>
来测试指定的扩展是否已经激活。
这既能用于内建的扩展也可以用于动态加载的扩展（既可以通过 `php.ini`
也可以通过 <span class="function">dl</span>）。

**Warning**

在 PHP 5.3 里，此函数被某些 SAPI 移除了。

### 参数

`library`  
此参数*仅仅*是要加载的扩展的文件名，依赖于你的平台。
比如，<a href="/ref/sockets.html" class="link">sockets</a>（作为共享模块编译，而不是默认的！）在
Unix 平台上称为 `sockets.so` 而 在 Windows 平台上是 `php_sockets.dll`。

扩展加载的目录依赖于你的平台：

Windows - 如果没有在 `php.ini` 里明确设置，扩展默认会从 `C:\php5\`
加载。

Unix - 如果没有在 `php.ini` 里明确设置，默认的扩展目录依赖于

-   <span class="simpara"> PHP 是否通过 *--enable-debug* 选项构建
    </span>
-   <span class="simpara"> PHP 是否以（实验性质的）ZTS （Zned
    线程安全）支持构建 </span>
-   <span class="simpara"> 当前的内部 *ZEND\_MODULE\_API\_NO*（Zend
    内部模块 API 数字，基本上是主要模块修改时的日期） </span>

考虑到上述，目录默认为 *\<install-dir\>/lib/php/extensions/
\<debug-or-not\>-\<zts-or-not\>-ZEND\_MODULE\_API\_NO*，例如
`/usr/local/php/lib/php/extensions/debug-non-zts-20010901` 或
`/usr/local/php/lib/php/extensions/no-debug-zts-20010901`。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
如果加载模块的功能是无效或者禁用的（既可以通过设置关闭
<a href="/info/setup.html#" class="link">enable_dl</a>
设置，也可以通过启用 `php.ini` 里的
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>）将导致一个
**`E_ERROR`** 并中断执行。 如果因为指定的库无法加载而导致 <span
class="function">dl</span> 失败，除了返回 **`FALSE`**，还会产生一个
**`E_WARNING`** 的消息。

### 范例

**示例 \#1 <span class="function">dl</span> 例子**

``` php
<?php
// 加载一个扩展的例子，基于操作系统
if (!extension_loaded('sqlite')) {
    if (strtoupper(substr(PHP_OS, 0, 3)) === 'WIN') {
        dl('php_sqlite.dll');
    } else {
        dl('sqlite.so');
    }
}

// 或者，使用常量 PHP_SHLIB_SUFFIX 
if (!extension_loaded('sqlite')) {
    $prefix = (PHP_SHLIB_SUFFIX === 'dll') ? 'php_' : '';
    dl($prefix . 'sqlite.' . PHP_SHLIB_SUFFIX);
}
?>
```

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                        |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.0 | PHP-FPM 模式下已禁用 <span class="function">dl</span>。                                                                                                                                                                     |
| 5.3.9 | 尽管不推荐，但 PHP-FPM 模式下启用了 <span class="function">dl</span>。                                                                                                                                                      |
| 5.3.0 | 由于稳定性，<span class="function">dl</span> 在某些 SAPI 中被禁用。仅仅允许 <span class="function">dl</span> 的 SAPI 为 CLI 和 Embed。 使用 <a href="/ini/core.html#ini.extension" class="link">扩展加载指令</a> 作为替代。 |

### 注释

> **Note**:
>
> 当 PHP 以支持 ZTS 构建时，*不*支持 <span class="function">dl</span>。
> 使用
> <a href="/ini/core.html#ini.extension" class="link">扩展加载指令</a>
> 作为替代。

> **Note**:
>
> 在某些 Unix 平台上，<span class="function">dl</span> 是大小写敏感的。

> **Note**: <span class="simpara">当 PHP 运行在
> <a href="/features/safe-mode.html" class="link">安全模式</a>
> 时，不能使用此函数。</span>

### 参见

-   <a href="/ini/core.html#ini.extension" class="link">扩展加载指令</a>
-   <span class="function">extension\_loaded</span>

extension\_loaded
=================

检查一个扩展是否已经加载

### 说明

<span class="type">bool</span> <span
class="methodname">extension\_loaded</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

检查一个扩展是否已经加载。

### 参数

`name`  
扩展名称，大小写不敏感。

你可以用 <span class="function">phpinfo</span>
来查看一系列扩展名称，而在 *CGI* 或 *CLI* 的 PHP 版本里你可以使用 **-m**
参数来列出所有有效的扩展：

    $ php -m
    [PHP Modules]
    xml
    tokenizer
    standard
    sockets
    session
    posix
    pcre
    overload
    mysql
    mbstring
    ctype

    [Zend Modules]

### 返回值

如果 `name` 指定的扩展已加载，返回**`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">extension\_loaded</span> 例子**

``` php
<?php
if (!extension_loaded('gd')) {
    if (!dl('gd.so')) {
        exit;
    }
}
?>
```

### 参见

-   <span class="function">get\_loaded\_extensions</span>
-   <span class="function">get\_extension\_funcs</span>
-   <span class="function">phpinfo</span>
-   <span class="function">dl</span>
-   <span class="function">function\_exists</span>

gc\_collect\_cycles
===================

强制收集所有现存的垃圾循环周期

### 说明

<span class="type">int</span> <span
class="methodname">gc\_collect\_cycles</span> ( <span
class="methodparam">void</span> )

强制收集所有现存的垃圾循环周期。

### 参数

此函数没有参数。

### 返回值

返回收集的循环数量。

### 参见

-   <a href="/features/gc.html" class="link">垃圾回收机制</a>

gc\_disable
===========

停用循环引用收集器

### 说明

<span class="type">void</span> <span
class="methodname">gc\_disable</span> ( <span
class="methodparam">void</span> )

停用循环引用收集器，设置
<a href="/info/setup.html#" class="link">zend.enable_gc</a> 为 *0*。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <a href="/features/gc.html" class="link">垃圾回收机制</a>

gc\_enable
==========

激活循环引用收集器

### 说明

<span class="type">void</span> <span
class="methodname">gc\_enable</span> ( <span
class="methodparam">void</span> )

设置 <a href="/info/setup.html#" class="link">zend.enable_gc</a> 为
*1*， 激活循环引用收集器。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <a href="/features/gc.html" class="link">垃圾回收机制</a>

gc\_enabled
===========

返回循环引用计数器的状态

### 说明

<span class="type">bool</span> <span
class="methodname">gc\_enabled</span> ( <span
class="methodparam">void</span> )

返回循环引用计数器的状态。

### 参数

此函数没有参数。

### 返回值

如果垃圾收集器已启用则返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 一个 <span class="function">gc\_enabled</span> 例子**

``` php
<?php
if(gc_enabled()) gc_collect_cycles();
?>
```

### 参见

-   <a href="/features/gc.html" class="link">垃圾回收机制</a>

gc\_mem\_caches
===============

Reclaims memory used by the Zend Engine memory manager

### 说明

<span class="type">int</span> <span
class="methodname">gc\_mem\_caches</span> ( <span
class="methodparam">void</span> )

Reclaims memory used by the Zend Engine memory manager.

### 参数

此函数没有参数。

### 返回值

Returns the number of bytes freed.

### 参见

-   <a href="/features/gc.html" class="link">Garbage Collection</a>

gc\_status
==========

Gets information about the garbage collector

### 说明

<span class="type">array</span> <span
class="methodname">gc\_status</span> ( <span
class="methodparam">void</span> )

Gets information about the current state of the garbage collector.

### 参数

此函数没有参数。

### 返回值

Returns an associative array with the following elements:

-   <span class="simpara"> *"runs"* </span>
-   <span class="simpara"> *"collected"* </span>
-   <span class="simpara"> *"threshold"* </span>
-   <span class="simpara"> *"roots"* </span>

### 范例

**示例 \#1 <span class="function">gc\_status</span> Usage**

``` php
<?php

// create object tree that needs gc collection
$a = new stdClass();
$a->b = [];
for ($i = 0; $i < 100000; $i++) {
    $b = new stdClass();
    $b->a = $a;
    $a->b[] = $b;
}
unset($a);
unset($b);
gc_collect_cycles();

var_dump(gc_status());
```

以上例程的输出类似于：

    array(4) {
      ["runs"]=>
      int(5)
      ["collected"]=>
      int(100002)
      ["threshold"]=>
      int(50001)
      ["roots"]=>
      int(0)
    }

### 参见

-   <a href="/features/gc.html" class="link">Garbage Collection</a>

get\_cfg\_var
=============

获取 PHP 配置选项的值

### 说明

<span class="type">string</span> <span
class="methodname">get\_cfg\_var</span> ( <span
class="methodparam"><span class="type">string</span> `$option`</span> )

获取 PHP 配置选项 `option` 的值。

此函数不会返回 PHP 编译的配置信息，或从 Apache 配置文件读取。

检查系统是否使用了一个<a href="/configuration/file.html" class="link">配置文件</a>，并尝试获取
cfg\_file\_path 的配置设置的值。 如果有效，将会使用一个配置文件。

### 参数

`option`  
配置选项的名称。

### 返回值

返回 `option` 指定的当前 PHP 配置变量的值，错误发生时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                               |
|-------|------------------------------------------------------------------------------------|
| 5.3.0 | <span class="function">get\_cfg\_var</span> 被修复，能够返回 "array" 的 ini 选项。 |

### 参见

-   <span class="function">ini\_get</span>
-   <span class="function">ini\_get\_all</span>

get\_current\_user
==================

获取当前 PHP 脚本所有者名称

### 说明

<span class="type">string</span> <span
class="methodname">get\_current\_user</span> ( <span
class="methodparam">void</span> )

返回当前 PHP 脚本所有者名称。

### 返回值

以字符串返回用户名。

### 范例

**示例 \#1 <span class="function">get\_current\_user</span> 例子**

``` php
<?php
echo 'Current script owner: ' . get_current_user();
?>
```

以上例程的输出类似于：

    Current script owner: SYSTEM

### 参见

-   <span class="function">getmyuid</span>
-   <span class="function">getmygid</span>
-   <span class="function">getmypid</span>
-   <span class="function">getmyinode</span>
-   <span class="function">getlastmod</span>

get\_defined\_constants
=======================

返回所有常量的关联数组，键是常量名，值是常量值

### 说明

<span class="type">array</span> <span
class="methodname">get\_defined\_constants</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$categorize`<span
class="initializer"> = false</span></span> \] )

返回当前所有已定义的常量名和值。 这包含 <span
class="function">define</span> 函数所创建的，也包含了所有扩展所创建的。

### 参数

`categorize`  
让此函数返回一个多维数组，分类为第一维的键名，常量和它们的值位于第二维。

``` php
<?php
define("MY_CONSTANT", 1);
print_r(get_defined_constants(true));
?>
```

以上例程的输出类似于：

    Array
    (
        [Core] => Array
            (
                [E_ERROR] => 1
                [E_WARNING] => 2
                [E_PARSE] => 4
                [E_NOTICE] => 8
                [E_CORE_ERROR] => 16
                [E_CORE_WARNING] => 32
                [E_COMPILE_ERROR] => 64
                [E_COMPILE_WARNING] => 128
                [E_USER_ERROR] => 256
                [E_USER_WARNING] => 512
                [E_USER_NOTICE] => 1024
                [E_ALL] => 2047
                [TRUE] => 1
            )

        [pcre] => Array
            (
                [PREG_PATTERN_ORDER] => 1
                [PREG_SET_ORDER] => 2
                [PREG_OFFSET_CAPTURE] => 256
                [PREG_SPLIT_NO_EMPTY] => 1
                [PREG_SPLIT_DELIM_CAPTURE] => 2
                [PREG_SPLIT_OFFSET_CAPTURE] => 4
                [PREG_GREP_INVERT] => 1
            )

        [user] => Array
            (
                [MY_CONSTANT] => 1
            )

    )

### 返回值

返回的数组为 常量名 =\> 常量值，也可以按注册变量的扩展名称来分组。

### 更新日志

| 版本   | 说明                                                                                                                                         |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.1  | 仅作用于 Windows：内核常量归类到 *Core*，之前是 *mhash*。                                                                                    |
| 5.3.0  | 内核常量归类为 *Core*，之前是 *internal*。在 Windows 上，内核常量归类到 *mhash*。                                                            |
| 5.2.11 | `categorize` 参数现在可以合适得被处理。 在此之前，`categorize` 被解释为 *!is\_null($categorize)*，导致任何非 **`NULL`** 的值会强制常量分类。 |

### 范例

**示例 \#1 <span class="function">get\_defined\_constants</span> 例子**

``` php
<?php
print_r(get_defined_constants());
?>
```

以上例程的输出类似于：

    Array
    (
        [E_ERROR] => 1
        [E_WARNING] => 2
        [E_PARSE] => 4
        [E_NOTICE] => 8
        [E_CORE_ERROR] => 16
        [E_CORE_WARNING] => 32
        [E_COMPILE_ERROR] => 64
        [E_COMPILE_WARNING] => 128
        [E_USER_ERROR] => 256
        [E_USER_WARNING] => 512
        [E_USER_NOTICE] => 1024
        [E_ALL] => 2047
        [TRUE] => 1
    )

### 参见

-   <span class="function">defined</span>
-   <span class="function">get\_loaded\_extensions</span>
-   <span class="function">get\_defined\_functions</span>
-   <span class="function">get\_defined\_vars</span>

get\_extension\_funcs
=====================

返回模块函数名称的数组

### 说明

<span class="type">array</span> <span
class="methodname">get\_extension\_funcs</span> ( <span
class="methodparam"><span class="type">string</span>
`$module_name`</span> )

该函数根据 `module_name` 返回模块内定义的所有函数的名称。

### 参数

`module_name`  
模块名称。

> **Note**:
>
> 这个参数必须是*小写（lowercase）*的。

### 返回值

返回包含所有函数名的数组，如果 `module_name` 不是一个有效的扩展则返回
**`FALSE`**。

### 范例

**示例 \#1 打印 XML 函数**

``` php
<?php
print_r(get_extension_funcs("xml"));
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => xml_parser_create
        [1] => xml_parser_create_ns
        [2] => xml_set_object
        [3] => xml_set_element_handler
        [4] => xml_set_character_data_handler
        [5] => xml_set_processing_instruction_handler
        [6] => xml_set_default_handler
        [7] => xml_set_unparsed_entity_decl_handler
        [8] => xml_set_notation_decl_handler
        [9] => xml_set_external_entity_ref_handler
        [10] => xml_set_start_namespace_decl_handler
        [11] => xml_set_end_namespace_decl_handler
        [12] => xml_parse
        [13] => xml_parse_into_struct
        [14] => xml_get_error_code
        [15] => xml_error_string
        [16] => xml_get_current_line_number
        [17] => xml_get_current_column_number
        [18] => xml_get_current_byte_index
        [19] => xml_parser_free
        [20] => xml_parser_set_option
        [21] => xml_parser_get_option
        [22] => utf8_encode
        [23] => utf8_decode
    )

### 参见

-   <span class="function">get\_loaded\_extensions</span>
-   <span class="methodname">ReflectionExtension::getFunctions</span>

get\_include\_path
==================

获取当前的 include\_path 配置选项

### 说明

<span class="type">string</span> <span
class="methodname">get\_include\_path</span> ( <span
class="methodparam">void</span> )

获取当前
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
配置选项的值。

### 返回值

返回字符串的路径。

### 范例

**示例 \#1 <span class="function">get\_include\_path</span> 例子**

``` php
<?php
echo get_include_path();

// 或使用 ini_get()
echo ini_get('include_path');
?>
```

### 参见

-   <span class="function">ini\_get</span>
-   <span class="function">restore\_include\_path</span>
-   <span class="function">set\_include\_path</span>
-   <span class="function">include</span>

get\_included\_files
====================

返回被 include 和 require 文件名的 array

### 说明

<span class="type">array</span> <span
class="methodname">get\_included\_files</span> ( <span
class="methodparam">void</span> )

返回所有被 <span class="function">include</span>、 <span
class="function">include\_once</span>、 <span
class="function">require</span> 和 <span
class="function">require\_once</span> 的文件名。

### 返回值

返回所有文件名称的 array。

脚本最初被称为”被包含的文件“，所以脚本自身也会和 <span
class="function">include</span> 系列函数引用的脚本列在一起。

被多次 include 和 require 的文件在返回的 array 里只会列出一次。

### 范例

**示例 \#1 <span class="function">get\_included\_files</span> 范例**

``` php
<?php
// 本文件是 abc.php

include 'test1.php';
include_once 'test2.php';
require 'test3.php';
require_once 'test4.php';

$included_files = get_included_files();

foreach ($included_files as $filename) {
    echo "$filename\n";
}

?>
```

以上例程会输出：

    /path/to/abc.php
    /path/to/test1.php
    /path/to/test2.php
    /path/to/test3.php
    /path/to/test4.php

### 注释

> **Note**:
>
> 使用 *auto\_prepend\_file*
> 配置指令所包含的文件不会包含在返回的数组里。

### 参见

-   <span class="function">include</span>
-   <span class="function">include\_once</span>
-   <span class="function">require</span>
-   <span class="function">require\_once</span>
-   <span class="function">get\_required\_files</span>

get\_loaded\_extensions
=======================

返回所有编译并加载模块名的 array

### 说明

<span class="type">array</span> <span
class="methodname">get\_loaded\_extensions</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$zend_extensions`<span class="initializer"> = false</span></span> \] )

该函数返回了 PHP 解析器里所有编译并加载的模块名。

### 参数

`zend_extensions`  
只返回 Zend 扩展，并非类似 mysqli 的普通扩展。默认是 **`FALSE`**
(返回普通扩展)。

### 返回值

返回所有模块名的一个索引数组(array)。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 5.2.4 | 添加了可选的 `zend_extensions` 参数。 |

### 范例

**示例 \#1 <span class="function">get\_loaded\_extensions</span> 范例**

``` php
<?php
print_r(get_loaded_extensions());
?>
```

以上例程的输出类似于：

    Array
    (
       [0] => xml
       [1] => wddx
       [2] => standard
       [3] => session
       [4] => posix
       [5] => pgsql
       [6] => pcre
       [7] => gd
       [8] => ftp
       [9] => db
       [10] => calendar
       [11] => bcmath
    )

### 参见

-   <span class="function">get\_extension\_funcs</span>
-   <span class="function">extension\_loaded</span>
-   <span class="function">dl</span>
-   <span class="function">phpinfo</span>

get\_magic\_quotes\_gpc
=======================

获取当前 magic\_quotes\_gpc 的配置选项设置

### 说明

<span class="type">bool</span> <span
class="methodname">get\_magic\_quotes\_gpc</span> ( <span
class="methodparam">void</span> )

返回当前 <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
配置选项的设置

记住，尝试在运行时设置
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
将不会生效。

更多关于 magic\_quotes
的信息参见<a href="/security/magicquotes.html" class="link">安全</a>一章。

### 返回值

如果 magic\_quotes\_gpc 为关闭时返回 0，否则返回 1。在 PHP 5.4.O
起将始终返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                            |
|-------|-----------------------------------------------------------------|
| 5.4.0 | 始终返回 **`FALSE`**，因为这个魔术引号功能已经从 PHP 中移除了。 |

### 范例

**示例 \#1 <span class="function">get\_magic\_quotes\_gpc</span> 例子**

``` php
<?php
// 如果启用了魔术引号
echo $_POST['lastname'];             // O\'reilly
echo addslashes($_POST['lastname']); // O\\\'reilly

// 适用各个 PHP 版本的用法
if (get_magic_quotes_gpc()) {
    $lastname = stripslashes($_POST['lastname']);
}
else {
    $lastname = $_POST['lastname'];
}

// 如果使用 MySQL
$lastname = mysql_real_escape_string($lastname);

echo $lastname; // O\'reilly
$sql = "INSERT INTO lastnames (lastname) VALUES ('$lastname')";
?>
```

### 注释

> **Note**:
>
> 如果指令
> <a href="/book/sybase.html#" class="link">magic_quotes_sybase</a> 为
> ON，它会完全覆盖
> <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>。
> 所以即使 <span class="function">get\_magic\_quotes\_gpc</span> 返回
> **`TRUE`**，双引号、反斜杠或 NUL 都不会被转义。 只有单引号会被转义。
> 这种情况下它们看上去像：*''*

### 参见

-   <span class="function">addslashes</span>
-   <span class="function">stripslashes</span>
-   <span class="function">get\_magic\_quotes\_runtime</span>
-   <span class="function">ini\_get</span>

get\_magic\_quotes\_runtime
===========================

获取当前 magic\_quotes\_runtime 配置选项的激活状态

### 说明

<span class="type">bool</span> <span
class="methodname">get\_magic\_quotes\_runtime</span> ( <span
class="methodparam">void</span> )

返回当前
<a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
配置选项的激活状态。

### 返回值

magic\_quotes\_runtime 在关闭时返回 0，否则返回 1。 自 PHP 5.4.0
起始终返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                      |
|-------|---------------------------------------------------------------------------|
| 5.4.0 | 总是返回 **`FALSE`**，因为魔术引号（magic quotes）功能已经从 PHP 中移除。 |

### 范例

**示例 \#1 <span class="function">get\_magic\_quotes\_runtime</span>
例子**

``` php
<?php
// 检测 magic_quotes_runtime 是否已经激活
if(get_magic_quotes_runtime())
{
    // 关闭功能
    set_magic_quotes_runtime(false);
}
?>
```

### 参见

-   <span class="function">get\_magic\_quotes\_gpc</span>
-   <span class="function">set\_magic\_quotes\_runtime</span>

get\_required\_files
====================

别名 <span class="function">get\_included\_files</span>

### 说明

此函数是该函数的别名： <span
class="function">get\_included\_files</span>.

get\_resources
==============

Returns active resources

### 说明

<span class="type">array</span> <span
class="methodname">get\_resources</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`</span> \] )

Returns an array of all currently active <span
class="type">resource</span>s, optionally filtered by resource type.

### 参数

`type`  
If defined, this will cause <span class="function">get\_resources</span>
to only return resources of the given type.
<a href="/resource.html" class="link">A list of resource types is available.</a>

If the <span class="type">string</span> *Unknown* is provided as the
type, then only resources that are of an unknown type will be returned.

If omitted, all resources will be returned.

### 返回值

Returns an <span class="type">array</span> of currently active
resources, indexed by resource number.

### 范例

**示例 \#1 Unfiltered <span class="function">get\_resources</span>**

``` php
<?php
$fp = tmpfile();
var_dump(get_resources());
?>
```

以上例程的输出类似于：

    array(1) {
      [1]=>
      resource(1) of type (stream)
    }

**示例 \#2 Filtered <span class="function">get\_resources</span>**

``` php
<?php
$fp = tmpfile();
var_dump(get_resources('stream'));
var_dump(get_resources('curl'));
?>
```

以上例程的输出类似于：

    array(1) {
      [1]=>
      resource(1) of type (stream)
    }
    array(0) {
    }

### 参见

-   <span class="function">get\_loaded\_extensions</span>
-   <span class="function">get\_defined\_constants</span>
-   <span class="function">get\_defined\_functions</span>
-   <span class="function">get\_defined\_vars</span>

getenv
======

获取一个环境变量的值

### 说明

<span class="type">string</span> <span class="methodname">getenv</span>
( <span class="methodparam"><span class="type">string</span>
`$varname`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$local_only`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="type">array</span> <span class="methodname">getenv</span> (
<span class="methodparam">void</span> )

获取一个环境变量的值。

使用 <span class="function">phpinfo</span>
你可以看到所有环境变量的列表。 这些变量很多都在
<a href="http://www.faqs.org/rfcs/rfc3875" class="link external">» RFC 3875</a>
的范围之内， 尤其是章节4.1，"Request Meta-Variables"。

### 参数

`varname`  
变量名。

`local_only`  
设置为 true 以仅返回本地环境变量（由操作系统或 <span
class="function">putenv</span> 设置）。

### 返回值

返回环境变量 `varname` 的值， 如果环境变量 `varname` 不存在则返回
**`FALSE`**。 如果省略 `varname`，则所有环境变量都将作为关联数组 <span
class="type">array</span> 返回。

### 更新日志

| 版本                  | 说明                                                                                  |
|-----------------------|---------------------------------------------------------------------------------------|
| 7.1.0                 | 现在可以省略 `varname` 来检索所有环境变量的关联数组 <span class="type">array</span>。 |
| 5.5.38, 5.6.24, 7.0.9 | 添加 `local_only` 参数。                                                              |

### 注释

**Warning**

如果 PHP 在诸如 Fast CGI 之类的 SAPI 中运行，则此函数将始终返回由 SAPI
设置的环境变量的值，即使已使用 <span class="function">putenv</span>
来设置同名的本地环境变量。使用 `local_only`
参数返回本地设置的环境变量的值。

### 范例

**示例 \#1 <span class="function">getenv</span> 例子**

``` php
<?php
// getenv() 使用示例
$ip = getenv('REMOTE_ADDR');

// 或简单仅使用全局变量（$_SERVER 或 $_ENV）
$ip = $_SERVER['REMOTE_ADDR'];

// 安全地获取环境变量，忽略通过 SAPI 或 putenv 修改的值
$ip = getenv('REMOTE_ADDR', true) ?: getenv('REMOTE_ADDR')
?>
```

### 参见

-   <span class="function">putenv</span>
-   <span class="function">apache\_getenv</span>
-   <a href="/language/variables/superglobals.html" class="link">超全局变量</a>

getlastmod
==========

获取页面最后修改的时间

### 说明

<span class="type">int</span> <span class="methodname">getlastmod</span>
( <span class="methodparam">void</span> )

获取执行的主脚本的最后修改时间。

如果你对其他文件的最后修改时间的感兴趣，可考虑使用 <span
class="function">filemtime</span>。

### 返回值

返回当前页面最后修改的时间。这个值是一个 Unix 时间戳，可以传入 <span
class="function">date</span>。 错误时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">getlastmod</span> 例子**

``` php
<?php
// 输出类似 'Last modified: March 04 1998 20:43:59.'
echo "Last modified: " . date ("F d Y H:i:s.", getlastmod());
?>
```

### 参见

-   <span class="function">date</span>
-   <span class="function">getmyuid</span>
-   <span class="function">getmygid</span>
-   <span class="function">get\_current\_user</span>
-   <span class="function">getmyinode</span>
-   <span class="function">getmypid</span>
-   <span class="function">filemtime</span>

getmygid
========

获取当前 PHP 脚本拥有者的 GID

### 说明

<span class="type">int</span> <span class="methodname">getmygid</span> (
<span class="methodparam">void</span> )

获取当前 PHP 脚本拥有者的用户组 ID。

### 返回值

返回当前 PHP 脚本拥有者的用户组 ID，或在错误时返回 **`FALSE`**。

### 参见

-   <span class="function">getmyuid</span>
-   <span class="function">getmypid</span>
-   <span class="function">get\_current\_user</span>
-   <span class="function">getmyinode</span>
-   <span class="function">getlastmod</span>

getmyinode
==========

获取当前脚本的索引节点（inode）

### 说明

<span class="type">int</span> <span class="methodname">getmyinode</span>
( <span class="methodparam">void</span> )

获取当前脚本的索引节点（inode）。

### 返回值

以整型返回当前脚本的索引节点（inode），或在错误时返回 **`FALSE`**。

### 参见

-   <span class="function">getmygid</span>
-   <span class="function">getmyuid</span>
-   <span class="function">getmypid</span>
-   <span class="function">get\_current\_user</span>
-   <span class="function">getlastmod</span>

getmypid
========

获取 PHP 进程的 ID

### 说明

<span class="type">int</span> <span class="methodname">getmypid</span> (
<span class="methodparam">void</span> )

获取当前 PHP 进程 ID。

### 返回值

返回当前 PHP 进程 ID，或在错误时返回 **`FALSE`**。

### 注释

**Warning**

进程 ID 并不是唯一的，所以他们是一个弱熵源。
对安全性有依赖的上下文中我们不推荐依赖于 pid。

### 参见

-   <span class="function">getmygid</span>
-   <span class="function">getmyuid</span>
-   <span class="function">get\_current\_user</span>
-   <span class="function">getmyinode</span>
-   <span class="function">getlastmod</span>

getmyuid
========

获取 PHP 脚本所有者的 UID

### 说明

<span class="type">int</span> <span class="methodname">getmyuid</span> (
<span class="methodparam">void</span> )

获取当前脚本的用户 ID。

### 返回值

返回当前脚本的用户 ID，或在错误时返回 **`FALSE`**。

### 参见

-   <span class="function">getmygid</span>
-   <span class="function">getmypid</span>
-   <span class="function">get\_current\_user</span>
-   <span class="function">getmyinode</span>
-   <span class="function">getlastmod</span>

getopt
======

从命令行参数列表中获取选项

### 说明

<span class="type">array</span> <span class="methodname">getopt</span> (
<span class="methodparam"><span class="type">string</span>
`$options`</span> \[, <span class="methodparam"><span
class="type">array</span> `$longopts`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$optind`</span> \]\]
)

解析传入脚本的选项。

### 参数

`options`  
<span class="simpara">
该字符串中的每个字符会被当做选项字符，匹配传入脚本的选项以单个连字符(-)开头。
</span> <span class="simpara"> 比如，一个选项字符串 *"x"* 识别了一个选项
*-x*。 </span> <span class="simpara"> 只允许 a-z、A-Z 和 0-9。 </span>

`longopts`  
<span class="simpara">
选项数组。此数组中的每个元素会被作为选项字符串，匹配了以两个连字符(*--*)传入到脚本的选项。
</span> <span class="simpara"> 例如，长选项元素 *"opt"* 识别了一个选项
*--opt*。 </span>

`optind`  
<span class="simpara"> If the `optind` parameter is present, then the
index where argument parsing stopped will be written to this variable.
</span>

`options` 可能包含了以下元素：

-   单独的字符（不接受值）
-   后面跟随冒号的字符（此选项需要值）
-   后面跟随两个冒号的字符（此选项的值可选）

选项的值是字符串后的第一个参数。如果需要一个值，它不介意值之前是否有前置的空格，参见以下内容。

> **Note**: <span class="simpara"> 选项的值不接受空格（*"
> "*）作为分隔符。 </span>

> **Note**:
>
> `options` 和 `longopts` 的格式几乎是一样的，唯一的不同之处是
> `longopts` 需要是选项的数组（每个元素为一个选项），而 `options`
> 需要一个字符串（每个字符是个选项）。

### 返回值

此函数会返回选项/参数对， 或者在失败时返回 **`FALSE`**。

> **Note**:
>
> 选项的解析会终止于找到的第一个非选项，之后的任何东西都会被丢弃。

### 更新日志

| 版本  | 说明                                                    |
|-------|---------------------------------------------------------|
| 7.1.0 | 添加 `optind` 参数。                                    |
| 5.3.0 | 支持 "=" 作为 参数和值的分隔符。                        |
| 5.3.0 | 增加了可选值的支持（用"::"指定）。                      |
| 5.3.0 | 参数 `longopts` 在所有系统平台上均可用。                |
| 5.3.0 | 此函数不再依赖于操作系统，现在也能够在 Windows 上运行。 |

### 范例

**示例 \#1 <span class="function">getopt</span> 例子：基本用法**

``` php
<?php
// Script example.php
$options = getopt("f:hp:");
var_dump($options);
?>
```

``` shell
shell> php example.php -fvalue -h
```

以上例程会输出：

    array(2) {
      ["f"]=>
      string(5) "value"
      ["h"]=>
      bool(false)
    }

**示例 \#2 <span class="function">getopt</span> 例子：引入长选项**

``` php
<?php
// Script example.php
$shortopts  = "";
$shortopts .= "f:";  // Required value
$shortopts .= "v::"; // Optional value
$shortopts .= "abc"; // These options do not accept values

$longopts  = array(
    "required:",     // Required value
    "optional::",    // Optional value
    "option",        // No value
    "opt",           // No value
);
$options = getopt($shortopts, $longopts);
var_dump($options);
?>
```

``` shell
shell> php example.php -f "value for f" -v -a --required value --optional="optional value" --option
```

以上例程会输出：

    array(6) {
      ["f"]=>
      string(11) "value for f"
      ["v"]=>
      bool(false)
      ["a"]=>
      bool(false)
      ["required"]=>
      string(5) "value"
      ["optional"]=>
      string(14) "optional value"
      ["option"]=>
      bool(false)
    }

**示例 \#3 <span class="function">getopt</span> 例子：传递同一多个选项**

``` php
<?php
// Script example.php
$options = getopt("abc");
var_dump($options);
?>
```

``` shell
shell> php example.php -aaac
```

以上例程会输出：

    array(2) {
      ["a"]=>
      array(3) {
        [0]=>
        bool(false)
        [1]=>
        bool(false)
        [2]=>
        bool(false)
      }
      ["c"]=>
      bool(false)
    }

**示例 \#4 <span class="function">getopt</span> 例子：使用 `optind`**

``` php
<?php
// Script example.php
$optind = null;
$opts = getopt('a:b:', [], $optind);
$pos_args = array_slice($argv, $optind);
var_dump($pos_args);
```

``` shell
shell> php example.php -a 1 -b 2 -- test
```

以上例程会输出：

    array(1) {
      [0]=>
      string(4) "test"
    }

### 参见

-   <a href="/reserved/variables/argv.html" class="link"><var class="varname">$argv</var></a>

getrusage
=========

获取当前资源使用状况

### 说明

<span class="type">array</span> <span
class="methodname">getrusage</span> (\[ <span class="methodparam"><span
class="type">int</span> `$who`<span class="initializer"> =
0</span></span> \] )

这是 **getrusage(2)** 的接口。它返回了调用自系统的数据。

### 参数

`who`  
如果 `who` 是 1，getrusage 会使用 **`RUSAGE_CHILDREN`** 来调用。

### 返回值

返回了一个包含系统返回数据的关联数组。所以条目均可通过文档中字段的名称来访问。

### 范例

**示例 \#1 <span class="function">getrusage</span> 例子**

``` php
<?php
$dat = getrusage();
echo $dat["ru_nswap"];         // number of swaps
echo $dat["ru_majflt"];        // number of page faults
echo $dat["ru_utime.tv_sec"];  // user time used (seconds)
echo $dat["ru_utime.tv_usec"]; // user time used (microseconds)
?>
```

### 更新日志

| 版本  | 说明                         |
|-------|------------------------------|
| 7.0.0 | 此函数现在开始支持 Windows。 |

### 注释

> **Note**:
>
> 在 Windows 上 <span class="function">getrusage</span>
> 仅会返回以下类型：
>
> -   *"ru\_stime.tv\_sec"*
> -   *"ru\_stime.tv\_usec"*
> -   *"ru\_utime.tv\_sec"*
> -   *"ru\_utime.tv\_usec"*
> -   *"ru\_majflt"* (only if `who` is **`RUSAGE_SELF`**)
> -   *"ru\_maxrss"* (only if `who` is **`RUSAGE_SELF`**)
>
> If <span class="function">getrusage</span> is called with `who` set to
> *1* (**`RUSAGE_CHILDREN`**), then resource usage for threads are
> collected (meaning that internally the function is called with
> **`RUSAGE_THREAD`**).

> **Note**:
>
> 在 BeOS 2000，仅会返回以下类型：
>
> -   *"ru\_stime.tv\_sec"*
> -   *"ru\_stime.tv\_usec"*
> -   *"ru\_utime.tv\_sec"*
> -   *"ru\_utime.tv\_usec"*

### 参见

-   你系统上 **getrusage(2)** 的 man page

ini\_alter
==========

别名 <span class="function">ini\_set</span>

### 说明

此函数是该函数的别名： <span class="function">ini\_set</span>.

ini\_get\_all
=============

获取所有配置选项

### 说明

<span class="type">array</span> <span
class="methodname">ini\_get\_all</span> (\[ <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$details`<span class="initializer"> = true</span></span> \]\] )

获取所有已注册的配置选项

### 参数

`extension`  
可选的扩展名称。如果设置了，此函数仅仅返回指定该扩展的选项。

`details`  
获取详细设置或者仅仅是每个设置的当前值。 默认是
**`TRUE`**（获取详细信息）。

### 返回值

返回一个关联数组，指令名称是数组的键。

当 `details` 为 **`TRUE`**（默认），数组会包含
*global\_value*（`php.ini` 中的设置）、*local\_value*（可能是 <span
class="function">ini\_set</span> 或 `.htaccess` 中的设置） 以及
*access*（访问级别）。

当 `details` 为 **`FALSE`**，这个值会是选项的当前值。

参见<a href="/configuration/changes/modes.html" class="link">手册章节</a>中访问级别含义的信息。

> **Note**:
>
> 指令可以有多个访问级别，这也是为什么 *access* 会显示适当的位掩码。

### 注释

> **Note**:
>
> <span class="function">ini\_get\_all</span> 忽略 "array" 的 ini
> 选项，例如 pdo.dsn.\*。

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 5.3.0 | 增加参数 `details`。 |

### 范例

**示例 \#1 <span class="function">ini\_get\_all</span> 例子**

``` php
<?php
print_r(ini_get_all("pcre"));
print_r(ini_get_all());
?>
```

以上例程的输出类似于：

    Array
    (
        [pcre.backtrack_limit] => Array
            (
                [global_value] => 100000
                [local_value] => 100000
                [access] => 7
            )

        [pcre.recursion_limit] => Array
            (
                [global_value] => 100000
                [local_value] => 100000
                [access] => 7
            )

    )
    Array
    (
        [allow_call_time_pass_reference] => Array
            (
                [global_value] => 0
                [local_value] => 0
                [access] => 6
            )

        [allow_url_fopen] => Array
            (
                [global_value] => 1
                [local_value] => 1
                [access] => 4
            )

        ...

    )

**示例 \#2 禁用 `details`**

``` php
<?php
print_r(ini_get_all("pcre", false)); // Added in PHP 5.3.0
print_r(ini_get_all(null, false)); // Added in PHP 5.3.0
?>
```

以上例程的输出类似于：

    Array
    (
        [pcre.backtrack_limit] => 100000
        [pcre.recursion_limit] => 100000
    )
    Array
    (
        [allow_call_time_pass_reference] => 0
        [allow_url_fopen] => 1
        ...
    )

### 参见

-   <a href="/configuration/changes.html" class="xref">怎样修改配置设定</a>
-   <span class="function">ini\_get</span>
-   <span class="function">ini\_restore</span>
-   <span class="function">ini\_set</span>
-   <span class="function">get\_loaded\_extensions</span>
-   <span class="function">phpinfo</span>
-   <span class="methodname">ReflectionExtension::getINIEntries</span>

ini\_get
========

获取一个配置选项的值

### 说明

<span class="type">string</span> <span
class="methodname">ini\_get</span> ( <span class="methodparam"><span
class="type">string</span> `$varname`</span> )

成功时返回配置选项的值。

### 参数

`varname`  
配置选项名称。

### 返回值

成功是返回配置选项值的字符串，*null*
的值则返回空字符串。如果配置选项不存在，将会返回 **`FALSE`**。

### 范例

**示例 \#1 一些 <span class="function">ini\_get</span> 例子**

``` php
<?php
/*
我们的 php.ini 包含了以下的设置：

display_errors = On
register_globals = Off
post_max_size = 8M
*/

echo 'display_errors = ' . ini_get('display_errors') . "\n";
echo 'register_globals = ' . ini_get('register_globals') . "\n";
echo 'post_max_size = ' . ini_get('post_max_size') . "\n";
echo 'post_max_size+1 = ' . (ini_get('post_max_size')+1) . "\n";
echo 'post_max_size in bytes = ' . return_bytes(ini_get('post_max_size'));

function return_bytes($val) {
    $val = trim($val);
    $last = strtolower($val[strlen($val)-1]);
    switch($last) {
        // 自 PHP 5.1.0 起可以使用修饰符 'G'
        case 'g':
            $val *= 1024;
        case 'm':
            $val *= 1024;
        case 'k':
            $val *= 1024;
    }

    return $val;
}

?>
```

以上例程的输出类似于：


    display_errors = 1
    register_globals = 0
    post_max_size = 8M
    post_max_size+1 = 9
    post_max_size in bytes = 8388608

### 注释

> **Note**: **当查询一个 boolean 值**  
>
> 一个 *off* 的 boolean ini 值将会以空字符串或者 "0" 返回；*on* 的 ini
> 值会以 "1" 返回。 此函数也会返回 INI 值的文字字符串。

> **Note**: **当查询一个内存尺寸的值**  
>
> 许多内存尺寸的 ini 值，类似
> <a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a>
> 是以简写表示法储存在 `php.ini` 文件里。 <span
> class="function">ini\_get</span> 会返回 `php.ini`
> 文件中储存的确切字符串，而*不是*它的等量 <span
> class="type">integer</span>。
> 尝试对这些值使用常规算术运算函数将不会得到预期的结果。
> 以上例子显示了转换简写表示法为字节的一种方式，和 PHP
> 源码所做的比较像。

> **Note**:
>
> <span class="function">ini\_get</span> 无法读取 "array" 的 ini
> 选项，例如 pdo.dsn.\*，在这个例子中会返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明                                                         |
|-------|--------------------------------------------------------------|
| 5.3.0 | 当配置项不存在，之前会返回空字符串，现在会返回 **`FALSE`**。 |

### 参见

-   <span class="function">get\_cfg\_var</span>
-   <span class="function">ini\_get\_all</span>
-   <span class="function">ini\_restore</span>
-   <span class="function">ini\_set</span>

ini\_restore
============

恢复配置选项的值

### 说明

<span class="type">void</span> <span
class="methodname">ini\_restore</span> ( <span class="methodparam"><span
class="type">string</span> `$varname`</span> )

恢复指定的配置选项到它的原始值。

### 参数

`varname`  
配置选项名称。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ini\_restore</span> 例子**

``` php
<?php
$setting = 'y2k_compliance';

echo 'Current value for \'' . $setting . '\': ' . ini_get($setting), PHP_EOL;

ini_set($setting, ini_get($setting) ? 0 : 1);
echo 'New value for \'' . $setting . '\': ' . ini_get($setting), PHP_EOL;

ini_restore($setting);
echo 'Original value for \'' . $setting . '\': ' . ini_get($setting), PHP_EOL;
?>
```

以上例程会输出：

    Current value for 'y2k_compliance': 1
    New value for 'y2k_compliance': 0
    Original value for 'y2k_compliance': 1

### 参见

-   <span class="function">ini\_get</span>
-   <span class="function">ini\_get\_all</span>
-   <span class="function">ini\_set</span>

ini\_set
========

为一个配置选项设置值

### 说明

<span class="type">string</span> <span
class="methodname">ini\_set</span> ( <span class="methodparam"><span
class="type">string</span> `$varname`</span> , <span
class="methodparam"><span class="type">string</span> `$newvalue`</span>
)

设置指定配置选项的值。这个选项会在脚本运行时保持新的值，并在脚本结束时恢复。

### 参数

`varname`  
不是所有有效的选项都能够用 <span class="function">ini\_set</span>
来改变的。
这里有个有效选项的清单<a href="/ini/list.html" class="link">附录</a>。

`newvalue`  
选项新的值。

### 返回值

成功时返回旧的值，失败时返回 **`FALSE`**。

### 范例

**示例 \#1 设置一个 ini 选项**

``` php
<?php
echo ini_get('display_errors');

if (!ini_get('display_errors')) {
    ini_set('display_errors', '1');
}

echo ini_get('display_errors');
?>
```

### 参见

-   <span class="function">get\_cfg\_var</span>
-   <span class="function">ini\_get</span>
-   <span class="function">ini\_get\_all</span>
-   <span class="function">ini\_restore</span>
-   <a href="/configuration/changes.html" class="link">如何改变配置选项</a>

magic\_quotes\_runtime
======================

别名 <span class="function">set\_magic\_quotes\_runtime</span>

**Warning**

This alias was *DEPRECATED* in PHP 5.3.0, and *REMOVED* as of PHP 7.0.0.

### 说明

此函数是该函数的别名： <span
class="function">set\_magic\_quotes\_runtime</span>

main
====

虚拟的<span class="function">main</span>

### 说明

除了在PHP源码里，并没有一个名称为 <span class="function">main</span>
的函数。 在 PHP 4.3.0
的源码里，引入了新的错误处理类型(php\_error\_docref)。 其中一个功能是在
PHP 指令
<a href="/errorfunc/setup.html#" class="link">html_errors</a>(默认为 on)
和
<a href="/errorfunc/setup.html#" class="link">docref_root</a>(默认为on直至
PHP 4.3.2) 被设置时，在错误信息里提供对应的手册链接。

本页存在的原因是因为有时函数 <span class="function">main</span>
错误信息里的手册链接会指到本页。 如果你发现了这样的引用，请
<a href="https://bugs.php.net/" class="link external">» 提交错误报告</a>，
说明 PHP 函数发生了错误，并链接到了 <span class="function">main</span>，
错误会被妥善处理并可能会记录在文档里。

| 函数名                                      | 直到该版本，不会再指到这里 |
|---------------------------------------------|----------------------------|
| <span class="function">include</span>       | 5.1.0                      |
| <span class="function">include\_once</span> | 5.1.0                      |
| <span class="function">require</span>       | 5.1.0                      |
| <span class="function">require\_once</span> | 5.1.0                      |

### 参见

-   <a href="/errorfunc/setup.html#" class="link">html_errors</a>
-   <a href="/errorfunc/setup.html#" class="link">display_errors</a>

memory\_get\_peak\_usage
========================

返回分配给 PHP 内存的峰值

### 说明

<span class="type">int</span> <span
class="methodname">memory\_get\_peak\_usage</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$real_usage`<span
class="initializer"> = false</span></span> \] )

返回分配给你的 PHP 脚本的内存峰值字节数。

### 参数

`real_usage`  
如果设置为 **`TRUE`** 可以获取从系统分配到的真实内存尺寸。
如果未设置，或者设置为 **`FALSE`**，仅会报告 *emalloc()* 使用的内存。

### 返回值

返回内存峰值的字节数。

### 更新日志

| 版本  | 说明                                                                                                               |
|-------|--------------------------------------------------------------------------------------------------------------------|
| 5.2.1 | 使用此函数无需在编译时加上 <a href="/ini/core.html#ini.memory-limit" class="link">--enable-memory-limit</a> 选项。 |
| 5.2.0 | 添加参数 `real_usage`。                                                                                            |

### 参见

-   <span class="function">memory\_get\_usage</span>
-   <a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>

memory\_get\_usage
==================

返回分配给 PHP 的内存量

### 说明

<span class="type">int</span> <span
class="methodname">memory\_get\_usage</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$real_usage`<span
class="initializer"> = false</span></span> \] )

返回当前分配给你的 PHP 脚本的内存量，单位是字节（byte）。

### 参数

`real_usage`  
如果设置为
**`TRUE`**，获取系统分配总的内存尺寸，包括未使用的页。如果未设置或者设置为
**`FALSE`**，仅仅报告实际使用的内存量。

> **Note**:
>
> PHP 不跟踪非*emalloc()* 分配的内存

### 返回值

返回内存量字节数。

### 更新日志

| 版本  | 说明                                                                                                                         |
|-------|------------------------------------------------------------------------------------------------------------------------------|
| 5.2.1 | 不需要在编译时使用 <a href="/ini/core.html#ini.memory-limit" class="link">--enable-memory-limit</a> 选项就能够使用这个函数。 |
| 5.2.0 | 增加了参数 `real_usage`。                                                                                                    |

### 范例

**示例 \#1 一个 <span class="function">memory\_get\_usage</span> 例子**

``` php
<?php
//这只是个例子，下面的数字取决于你的系统

echo memory_get_usage() . "\n"; // 36640

$a = str_repeat("Hello", 4242);

echo memory_get_usage() . "\n"; // 57960

unset($a);

echo memory_get_usage() . "\n"; // 36744

?>
```

### 参见

-   <span class="function">memory\_get\_peak\_usage</span>
-   <a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>

php\_ini\_loaded\_file
======================

取得已加载的 php.ini 文件的路径

### 说明

<span class="type">string</span> <span
class="methodname">php\_ini\_loaded\_file</span> ( <span
class="methodparam">void</span> )

检查是否有加载的 `php.ini` 文件，并取回它的路径。

### 参数

此函数没有参数。

### 返回值

已加载的 `php.ini` 路径，或在没有时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">php\_ini\_loaded\_file</span> 例子**

``` php
<?php
$inipath = php_ini_loaded_file();

if ($inipath) {
    echo 'Loaded php.ini: ' . $inipath;
} else {
    echo 'A php.ini file is not loaded';
}
?>
```

以上例程的输出类似于：

    Loaded php.ini: /usr/local/php/php.ini

### 参见

-   <span class="function">php\_ini\_scanned\_files</span>
-   <span class="function">phpinfo</span>
-   <a href="/configuration/file.html" class="link">配置文件</a>

php\_ini\_scanned\_files
========================

返回从额外 ini 目录里解析的 .ini 文件列表

### 说明

<span class="type">string</span> <span
class="methodname">php\_ini\_scanned\_files</span> ( <span
class="methodparam">void</span> )

<span class="function">php\_ini\_scanned\_files</span> 返回解析的
`php.ini` 后逗号分隔的配置文件列表。 这些文件从编译时
**--with-config-file-scan-dir** 选项里指定的目录里找到。

这些返回的配置文件也包括了 **--with-config-file-scan-dir**
选项里声明的路径。

### 返回值

成功时返回逗号分隔的 .ini 文件字符串。 每个逗号后紧跟新的一行。
如果未设置指令 **--with-config-file-scan-dir** 将会返回 **`FALSE`**。
如果它设置了，并且目录是空的，将会返回一个空字符串。
如果有未识别的文件，此文件也会进入返回的字符串，但是会导致一个 PHP
错误。 此 PHP 错误即会在编译时出现也会在使用 <span
class="function">php\_ini\_scanned\_files</span> 函数时出现。

### 范例

**示例 \#1 列出返回的 ini 文件的简单例子**

``` php
<?php
if ($filelist = php_ini_scanned_files()) {
    if (strlen($filelist) > 0) {
        $files = explode(',', $filelist);

        foreach ($files as $file) {
            echo "<li>" . trim($file) . "</li>\n";
        }
    }
}
?>
```

### 参见

-   <span class="function">ini\_set</span>
-   <span class="function">phpinfo</span>
-   <span class="function">php\_ini\_loaded\_file</span>

php\_logo\_guid
===============

获取 logo 的 guid

### 说明

<span class="type">string</span> <span
class="methodname">php\_logo\_guid</span> ( <span
class="methodparam">void</span> )

此函数能够返回用于显示 PHP logo 内置图像的 ID。 图像仅在
<a href="/ini/core.html#ini.expose-php" class="link">expose_php</a>
启用时显示。

**Warning**

自 PHP 5.5.0 起，已经*废弃*并*移除*此函数。

### 返回值

返回 *PHPE9568F34-D428-11d2-A769-00AA001ACF42*.

### 更新日志

| 版本  | 说明                                                          |
|-------|---------------------------------------------------------------|
| 5.5.0 | <span class="function">php\_logo\_guid</span> 从 PHP 中移除。 |

### 范例

**示例 \#1 <span class="function">php\_logo\_guid</span> 例子**

``` php
<?php

echo '<img src="' . $_SERVER['PHP_SELF'] .
     '?=' . php_logo_guid() . '" alt="PHP Logo !" />';

?>
```

### 参见

-   <span class="function">phpinfo</span>
-   <span class="function">phpversion</span>
-   <span class="function">phpcredits</span>
-   <span class="function">zend\_logo\_guid</span>

php\_sapi\_name
===============

返回 web 服务器和 PHP 之间的接口类型

### 说明

<span class="type">string</span> <span
class="methodname">php\_sapi\_name</span> ( <span
class="methodparam">void</span> )

返回描述 PHP 所使用的接口类型（the Server API, SAPI）的小写字符串。
例如，CLI 的 PHP 下这个字符串会是 "cli"，Apache
下可能会有几个不同的值，取决于具体使用的 SAPI。 以下列出了可能的值。

### 返回值

返回接口类型的小写字符串。

尽管不够全面，可能返回的值包括了 *aolserver*、*apache*、
*apache2filter*、*apache2handler*、 *caudium*、*cgi* （直到 PHP 5.3）,
*cgi-fcgi*、*cli*、 *cli-server*、 *continuity*、*embed*、*fpm-fcgi*、
*isapi*、*litespeed*、 *milter*、*nsapi*、 *phttpd*、*pi3web*、*roxen*、
*thttpd*、*tux* 和 *webjames*。

### 范例

**示例 \#1 <span class="function">php\_sapi\_name</span> 例子**

以下例子检测了子字符串 *cgi*，因为它也有可能会是 *cgi-fcgi*。

``` php
<?php
$sapi_type = php_sapi_name();
if (substr($sapi_type, 0, 3) == 'cgi') {
    echo "You are using CGI PHP\n";
} else {
    echo "You are not using CGI PHP\n";
}
?>
```

### 注释

> **Note**: **另一种方法**  
>
> PHP 常量 **`PHP_SAPI`** 具有和 <span
> class="function">php\_sapi\_name</span> 相同的值。

**小贴士**

定义的 SAPI 可能不够明显，比如它可能定义为 *apache2handler* 或
*apache2filter*，而不是 *apache*

### 参见

-   <a href="/reserved/constants.html#reserved.constants.core" class="link">PHP_SAPI</a>

php\_uname
==========

返回运行 PHP 的系统的有关信息

### 说明

<span class="type">string</span> <span
class="methodname">php\_uname</span> (\[ <span class="methodparam"><span
class="type">string</span> `$mode`<span class="initializer"> =
"a"</span></span> \] )

<span class="function">php\_uname</span> 返回了运行 PHP
的操作系统的描述。 这和 <span class="function">phpinfo</span>
最顶端上输出的是同一个字符串。
如果仅仅要获取操作系统的名称。可以考虑使用常量
**`PHP_OS`**，不过要注意该常量会包含 PHP 构建（*built*）时的操作系统名。

在一些旧的 UNIX
平台，它有可能无法检测到当前系统的信息，然后会还原显示成构建 PHP
时的系统信息。 这仅仅在你的 uname() 函数库不存在或无法运行时发生。

### 参数

`mode`  
`mode` 是单个字符，用于定义要返回什么信息：

-   <span class="simpara"> *'a'*：此为默认。包含序列 *"s n r v m"*
    里的所有模式。 </span>
-   <span class="simpara"> *'s'*：操作系统名称。例如： *FreeBSD*。
    </span>
-   <span class="simpara"> *'n'*：主机名。例如：
    *localhost.example.com*。 </span>
-   <span class="simpara"> *'r'*：版本名称，例如： *5.1.2-RELEASE*。
    </span>
-   <span class="simpara"> *'v'*：版本信息。操作系统之间有很大的不同。
    </span>
-   <span class="simpara"> *'m'*：机器类型。例如：*i386*。 </span>

### 返回值

返回描述字符串。

### 范例

**示例 \#1 一些 <span class="function">php\_uname</span> 的例子**

``` php
<?php
echo php_uname();
echo PHP_OS;

/* 比如有些会输出：
Linux localhost 2.4.21-0.13mdk #1 Fri Mar 14 15:08:06 EST 2003 i686
Linux

FreeBSD localhost 3.2-RELEASE #15: Mon Dec 17 08:46:02 GMT 2001
FreeBSD

Windows NT XN1 5.1 build 2600
WINNT
*/

if (strtoupper(substr(PHP_OS, 0, 3)) === 'WIN') {
    echo 'This is a server using Windows!';
} else {
    echo 'This is a server not using Windows!';
}

?>
```

同样可以方便地使用一些相关的
<a href="/language/constants/predefined.html" class="link">PHP 预定义常量</a>，例如：

**示例 \#2 一些系统相关常量的例子**

``` php
<?php
// *nix
echo DIRECTORY_SEPARATOR; // /
echo PHP_SHLIB_SUFFIX;    // so
echo PATH_SEPARATOR;      // :

// Win*
echo DIRECTORY_SEPARATOR; // \
echo PHP_SHLIB_SUFFIX;    // dll
echo PATH_SEPARATOR;      // ;
?>
```

### 参见

-   <span class="function">phpversion</span>
-   <span class="function">php\_sapi\_name</span>
-   <span class="function">phpinfo</span>

phpcredits
==========

打印 PHP 贡献者名单

### 说明

<span class="type">bool</span> <span
class="methodname">phpcredits</span> (\[ <span class="methodparam"><span
class="type">int</span> `$flag`<span class="initializer"> =
CREDITS\_ALL</span></span> \] )

这个函数打印出了 PHP 开发者、模块等贡献者名单。
它生成了合适、可嵌入信息到页面中的 HTML 代码。

### 参数

`flag`  
生成自定义的贡献者页面，你也许想要使用 `flag` 参数。

| 名称              | 描述                                                                                                                                                                                    |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CREDITS\_ALL      | 所有贡献者，等同于使用： **`CREDITS_DOCS`** + **`CREDITS_GENERAL`** + **`CREDITS_GROUP`** + **`CREDITS_MODULES`** + **`CREDITS_FULLPAGE`**。 它以适当的标签产生了完整独立的 HTML 页面。 |
| CREDITS\_DOCS     | 文档组贡献名单                                                                                                                                                                          |
| CREDITS\_FULLPAGE | 常用于和其他标志进行组合。 表示需要打印包含其他标志表示信息的独立 HTML 页面。                                                                                                           |
| CREDITS\_GENERAL  | 普遍名单：语言设计与理念、PHP作者以及 SAPI 模块。                                                                                                                                       |
| CREDITS\_GROUP    | 核心开发者名单                                                                                                                                                                          |
| CREDITS\_MODULES  | PHP 扩展模块以及它们的作者的清单                                                                                                                                                        |
| CREDITS\_SAPI     | PHP 的服务器 API 模块以及他们的作者的清单                                                                                                                                               |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 打印普遍名单**

``` php
<?php
phpcredits(CREDITS_GENERAL);
?>
```

**示例 \#2 打印核心开发者和文档组**

``` php
<?php
phpcredits(CREDITS_GROUP | CREDITS_DOCS | CREDITS_FULLPAGE);
?>
```

**示例 \#3 打印所有贡献者**

``` php
<html>
 <head>
  <title>My credits page</title>
 </head>
 <body>
<?php
// 一些你自己的代码
phpcredits(CREDITS_ALL - CREDITS_FULLPAGE);
// 一些其他的代码
?>
 </body>
</html>
```

### 注释

> **Note**:
>
> 在 CLI 模式下 <span class="function">phpcredits</span> 输出明文而不是
> HTML。

### 参见

-   <span class="function">phpversion</span>
-   <span class="function">php\_logo\_guid</span>
-   <span class="function">phpinfo</span>

phpinfo
=======

输出关于 PHP 配置的信息

### 说明

<span class="type">bool</span> <span class="methodname">phpinfo</span>
(\[ <span class="methodparam"><span class="type">int</span> `$what`<span
class="initializer"> = INFO\_ALL</span></span> \] )

输出 PHP 当前状态的大量信息，包含了 PHP 编译选项、启用的扩展、PHP
版本、服务器信息和环境变量（如果编译为一个模块的话）、PHP环境变量、操作系统版本信息、path
变量、配置选项的本地值和主值、HTTP 头和PHP授权信息(License)。

因为每个系统安装得有所不同，<span class="function">phpinfo</span>
常用于在系统上检查
<a href="/configuration.html" class="link">配置设置</a>和
<a href="/language/variables/predefined.html" class="link">预定义变量</a>。

<span class="function">phpinfo</span> 同时是个很有价值的、包含所有
EGPCS(Environment, GET, POST, Cookie, Server) 数据的调试工具。

### 参数

`what`  
可以用以下的一个或多个 *constants* 用位运算传递给可选的 `what`
参数来定制输出的信息。 该参数可以把常量相加或者用
<a href="/language/operators/bitwise.html" class="link">or</a>
操作符按位运算。

| Name (constant)     | Value | Description                                                                                                                                |
|---------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| INFO\_GENERAL       | 1     | 配置的命令行、 `php.ini` 的文件位置、建立的时间、Web 服务器、系统及更多其他信息。                                                          |
| INFO\_CREDITS       | 2     | PHP 贡献者名单。参加 <span class="function">phpcredits</span>。                                                                            |
| INFO\_CONFIGURATION | 4     | 当前PHP指令的本地值和主值。参见 <span class="function">ini\_get</span>。                                                                   |
| INFO\_MODULES       | 8     | 已加载的模块和模块相应的设置。参见 <span class="function">get\_loaded\_extensions</span>。                                                 |
| INFO\_ENVIRONMENT   | 16    | 环境变量信息也可以用 `$_ENV` 获取。                                                                                                        |
| INFO\_VARIABLES     | 32    | 显示所有来自 EGPCS (Environment, GET, POST, Cookie, Server) 的 <a href="/language/variables/predefined.html" class="link">预定义变量</a>。 |
| INFO\_LICENSE       | 64    | PHP许可证信息。参见 <a href="https://www.php.net/license/" class="link external">» license FAQ</a>。                                       |
| INFO\_ALL           | -1    | 显示以上所有信息。                                                                                                                         |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

5.5.0

Logo GUIDs were replaced with data URIs, and so turning off expose\_php
now has no effect on the result of phpinfo(). Credits are also now
embedded within the output itself instead of linked.

版本

说明

5.2.2

增加了“已加载的配置文件”信息，之前只存在“配置文件路径(php.ini)"。

### 范例

**示例 \#1 <span class="function">phpinfo</span> 范例**

``` php
<?php

// 显示所有信息，默认显示 INFO_ALL
phpinfo();

// Show just the module information. 仅仅显示PHP模块信息，
// phpinfo(8) 返回同样的结果。
phpinfo(INFO_MODULES);

?>
```

### 注释

> **Note**:
>
> 在 PHP 5.5 之前版本，当
> <a href="/ini/core.html#ini.expose-php" class="link">expose_php</a>
> 设置为 *off* 可以禁用一部分信息。 这包括了 PHP 和 Zend 的
> logo，以及贡献者名单。

> **Note**:
>
> 在命令行（CLI）模式下 <span class="function">phpinfo</span>
> 仅会输出纯文本，而不是HTML。

### 参见

-   <span class="function">phpversion</span>
-   <span class="function">phpcredits</span>
-   <span class="function">php\_logo\_guid</span>
-   <span class="function">ini\_get</span>
-   <span class="function">ini\_set</span>
-   <span class="function">get\_loaded\_extensions</span>
-   <a href="/language/variables/predefined.html" class="link">Predefined Variables</a>

phpversion
==========

获取当前的PHP版本

### 说明

<span class="type">string</span> <span
class="methodname">phpversion</span> (\[ <span class="methodparam"><span
class="type">string</span> `$extension`</span> \] )

返回了包含当前运行 PHP 解释器或扩展版本信息的 string。

### 参数

`extension`  
可选的扩展名。

### 返回值

如果指定了可选参数 `extension`，<span
class="function">phpversion</span>会返回该扩展的版本。
如果没有对应的版本信息，或者该扩展未启用，则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">phpversion</span> 范例**

``` php
<?php
// prints e.g. 'Current PHP version: 4.1.1'
echo 'Current PHP version: ' . phpversion();

// prints e.g. '2.0' or nothing if the extension isn't enabled
echo phpversion('tidy');
?>
```

**示例 \#2 **`PHP_VERSION_ID`** 范例和用法**

``` php
<?php
// PHP_VERSION_ID 自 PHP 5.2.7 起有效，
// 如果我们的版本低于该版本，则用以下代码来模拟 
if (!defined('PHP_VERSION_ID')) {
    $version = explode('.', PHP_VERSION);

    define('PHP_VERSION_ID', ($version[0] * 10000 + $version[1] * 100 + $version[2]));
}

// PHP_VERSION_ID 定义为一个数字，PHP 版本越新，数字越大。
// 它的定义是以下的表达式：
//
// $version_id = $major_version * 10000 + $minor_version * 100 + $release_version;
//
// 现在我们可以通过 PHP_VERSION_ID 来检查 PHP 版本，
// 而不用每次都必须用 version_compare() 来检查 PHP 是否支持某个功能。
//
// 比如，我们在此可以定义一系列 PHP_VERSION_* constants 常量，
// 而在 5.2.7 之前的版本并没有被定义。

if (PHP_VERSION_ID < 50207) {
    define('PHP_MAJOR_VERSION',   $version[0]);
    define('PHP_MINOR_VERSION',   $version[1]);
    define('PHP_RELEASE_VERSION', $version[2]);

    // 等等， ...
}
?>
```

### 注释

> **Note**:
>
> 这些信息也存在于预定义常量 **`PHP_VERSION`**里。
> 更多版本的信息可以使用常量 **`PHP_VERSION_*`**。

### 参见

-   <a href="/reserved/constants.html#reserved.constants.core" class="link">常量 PHP_VERSION</a>
-   <span class="function">version\_compare</span>
-   <span class="function">phpinfo</span>
-   <span class="function">phpcredits</span>
-   <span class="function">php\_logo\_guid</span>
-   <span class="function">zend\_version</span>

putenv
======

设置环境变量的值

### 说明

<span class="type">bool</span> <span class="methodname">putenv</span> (
<span class="methodparam"><span class="type">string</span>
`$setting`</span> )

添加 `setting` 到服务器环境变量。 环境变量仅存活于当前请求期间。
在请求结束时环境会恢复到初始状态。

设置特定的环境变量也有可能是一个潜在的安全漏洞。
*safe\_mode\_allowed\_env\_vars* 包含了一个以逗号分隔的前缀列表。
在安全模式下，用户可以仅能修改用该指令设定的前缀名称的指令。
默认情况下，用户仅能够修改以 *PHP\_* 开头的环境变量（例如
*PHP\_FOO=BAR*）。 注意：如果此指令是空的，PHP允许用户设定任意环境变量！

*safe\_mode\_protected\_env\_vars*
指令包含了逗号分隔的环境变量列表，使用户最终无法通过 <span
class="function">putenv</span> 修改。 即使
*safe\_mode\_allowed\_env\_vars* 设置允许修改，这些变量也会被保护。

### 参数

`setting`  
设置，例如 *"FOO=BAR"*

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 设置一个环境变量**

``` php
<?php
putenv("UNIQID=$uniqid");
?>
```

### 注释

**Warning**

The *safe\_mode\_allowed\_env\_vars* 和
*safe\_mode\_protected\_env\_vars*
指令仅仅在启用<a href="/features/safe-mode.html" class="link">安全模式</a>时有效。

### 参见

-   <span class="function">getenv</span>
-   <span class="function">apache\_setenv</span>

restore\_include\_path
======================

还原 include\_path 配置选项的值

### 说明

<span class="type">void</span> <span
class="methodname">restore\_include\_path</span> ( <span
class="methodparam">void</span> )

还原到 `php.ini` 中设置的
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
主值。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">restore\_include\_path</span> 例子**

``` php
<?php

echo get_include_path();  // .:/usr/local/lib/php

set_include_path('/inc');

echo get_include_path();  // /inc

restore_include_path();

// 或使用 ini_restore
ini_restore('include_path');

echo get_include_path();  // .:/usr/local/lib/php

?>
```

### 参见

-   <span class="function">ini\_restore</span>
-   <span class="function">get\_include\_path</span>
-   <span class="function">set\_include\_path</span>
-   <span class="function">include</span>

set\_include\_path
==================

设置 include\_path 配置选项

### 说明

<span class="type">string</span> <span
class="methodname">set\_include\_path</span> ( <span
class="methodparam"><span class="type">string</span>
`$new_include_path`</span> )

为当前脚本设置
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
运行时的配置选项。

### 参数

`new_include_path`  
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
新的值。

### 返回值

成功时返回旧的
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">set\_include\_path</span> 例子**

``` php
<?php
set_include_path('/usr/lib/pear');

// 或使用 ini_set
ini_set('include_path', '/usr/lib/pear');
?>
```

**示例 \#2 添加到include path**

利用常量 **`PATH_SEPARATOR`** 可跨平台扩展 include path。

这个例子中我们把 `/usr/lib/pear` 添加到了 现有的 *include\_path*
的尾部。

``` php
<?php
$path = '/usr/lib/pear';
set_include_path(get_include_path() . PATH_SEPARATOR . $path);
?>
```

### 参见

-   <span class="function">ini\_set</span>
-   <span class="function">get\_include\_path</span>
-   <span class="function">restore\_include\_path</span>
-   <span class="function">include</span>

set\_magic\_quotes\_runtime
===========================

设置当前 magic\_quotes\_runtime 配置选项的激活状态

**Warning**

This function was *DEPRECATED* in PHP 5.3.0, and *REMOVED* as of PHP
7.0.0.

### 说明

<span class="type">bool</span> <span
class="methodname">set\_magic\_quotes\_runtime</span> ( <span
class="methodparam"><span class="type">bool</span> `$new_setting`</span>
)

设置当前
<a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
配置选项的激活状态。

### 错误／异常

自 PHP 5.3 起，该函数已经被弃用，执行它的时候会抛出 E\_DEPRECATED 异常。
自 PHP 5.4 起，尝试开启 magic quotes 时该函数会产生一个 E\_CORE\_ERROR
错误。

### 参数

`new_setting`  
关闭是 **`FALSE`**，开启是 **`TRUE`**。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">set\_magic\_quotes\_runtime</span>
例子**

``` php
<?php
// 创建临时文件指针
$fp = tmpfile();

// 写入一些数据
fwrite($fp, '\'PHP\' is a Recursive acronym');

// 没有 magic_quotes_runtime
rewind($fp);
set_magic_quotes_runtime(false);

echo 'Without magic_quotes_runtime: ' . fread($fp, 64), PHP_EOL;

// 有 magic_quotes_runtime
rewind($fp);
set_magic_quotes_runtime(true);

echo 'With magic_quotes_runtime: ' . fread($fp, 64), PHP_EOL;

// 清理
fclose($fp);
?>
```

以上例程会输出：

    Without magic_quotes_runtime: 'PHP' is a Recursive acronym
    With magic_quotes_runtime: \'PHP\' is a Recursive acronym

### 参见

-   <span class="function">get\_magic\_quotes\_gpc</span>
-   <span class="function">get\_magic\_quotes\_runtime</span>

set\_time\_limit
================

设置脚本最大执行时间

### 说明

<span class="type">bool</span> <span
class="methodname">set\_time\_limit</span> ( <span
class="methodparam"><span class="type">int</span> `$seconds`</span> )

设置允许脚本运行的时间，单位为秒。如果超过了此设置，脚本返回一个致命的错误。默认值为30秒，或者是在`php.ini`的*max\_execution\_time*被定义的值，如果此值存在。

当此函数被调用时，<span
class="function">set\_time\_limit</span>会从零开始重新启动超时计数器。换句话说，如果超时默认是30秒，在脚本运行了了25秒时调用
*set\_time\_limit(20)*，那么，脚本在超时之前可运行总时间为45秒。

### 参数

`seconds`  
最大的执行时间，单位为秒。如果设置为0（零），没有时间方面的限制。

### 返回值

成功时返回 **`TRUE`**，失败时返回 **`FALSE`** 。

### 注释

**Warning**

当php运行于<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>时，此功能不能生效。除了关闭安全模式或改变`php.ini`中的时间限制，没有别的办法。

> **Note**:
>
> <span
> class="function">set\_time\_limit</span>函数和配置指令<a href="/info/setup.html#" class="link">max_execution_time</a>只影响脚本本身执行的时间。任何发生在诸如使用<span
> class="function">system</span>的系统调用，流操作，数据库操作等的脚本执行的最大时间不包括其中，当该脚本已运行。在测量时间是实值的Windows中，情况就不是如此了。

### 参见

-   <a href="/info/setup.html#" class="link">max_execution_time</a>
-   <a href="/info/setup.html#" class="link">max_input_time</a>

sys\_get\_temp\_dir
===================

返回用于临时文件的目录

### 说明

<span class="type">string</span> <span
class="methodname">sys\_get\_temp\_dir</span> ( <span
class="methodparam">void</span> )

返回 PHP 储存临时文件的默认目录的路径。

### 返回值

返回临时目录的路径。

### 范例

**示例 \#1 <span class="function">sys\_get\_temp\_dir</span> 例子**

``` php
<?php
// 使用 sys_get_temp_dir() 在目录里创建临时文件
$temp_file = tempnam(sys_get_temp_dir(), 'Tux');

echo $temp_file;
?>
```

以上例程的输出类似于：

    C:\Windows\Temp\TuxA318.tmp

### 参见

-   <span class="function">tmpfile</span>
-   <span class="function">tempnam</span>

version\_compare
================

对比两个「PHP 规范化」的版本数字字符串

### 说明

<span class="type">mixed</span> <span
class="methodname">version\_compare</span> ( <span
class="methodparam"><span class="type">string</span> `$version1`</span>
, <span class="methodparam"><span class="type">string</span>
`$version2`</span> \[, <span class="methodparam"><span
class="type">string</span> `$operator`</span> \] )

<span class="function">version\_compare</span> 用于对比两个「PHP
规范化」的版本数字字符串。

此函数首先在版本字符串里用一个点 *.* 替换 *\_*、*-* 和
*+*，也会在任意非数字前后插入一个点 *.*，这样，类似 '4.3.2RC1' 将会变成
'4.3.2.RC.1'。 接下来它会分割结果， 然后它会从左往右对比各个部分。
如果某部分包含了特定的版本字符串，将会用以下顺序处理：
*列表中未找到的任意字符串* \< *dev* \< *alpha* = *a* \< *beta* = *b* \<
*RC* = *rc* \< *\#* \< *pl* = *p*。 这种方式不仅能够对比类似 '4.1' 和
'4.1.2' 那种不同的版本级别，同时也可以指定对比任何包含 PHP
开发状态的版本。

### 参数

`version1`  
第一个版本数。

`version2`  
第二个版本数。

`operator`  
如果你指定了可选的第三个参数 `operator`，你可以测试两者的特定关系。
可以的操作符分别是：*\<*、 *lt*、*\<=*、 *le*、*\>*、 *gt*、*\>=*、
*ge*、*==*、 *=*、*eq*、 *!=*、*\<\>* 和 *ne*。

此参数区分大小写，它的值应该是小写的。

### 返回值

默认情况下，在第一个版本低于第二个时，<span
class="function">version\_compare</span> 返回 *-1*；如果两者相等，返回
*0*；第二个版本更低时则返回 *1*。

当使用了可选参数 `operator` 时，如果关系是操作符所指定的那个，函数将返回
**`TRUE`**，否则返回 **`FALSE`**。

### 范例

下例使用了 **`PHP_VERSION`** 常量，因为它执行的代码包含了 PHP 版本的值。

**示例 \#1 <span class="function">version\_compare</span> examples**

``` php
<?php
if (version_compare(PHP_VERSION, '7.0.0') >= 0) {
    echo 'I am at least PHP version 7.0.0, my version: ' . PHP_VERSION . "\n";
}

if (version_compare(PHP_VERSION, '5.3.0') >= 0) {
    echo 'I am at least PHP version 5.3.0, my version: ' . PHP_VERSION . "\n";
}

if (version_compare(PHP_VERSION, '5.0.0', '>=')) {
    echo 'I am at least PHP version 5.0.0, my version: ' . PHP_VERSION . "\n";
}

if (version_compare(PHP_VERSION, '5.0.0', '<')) {
    echo 'I am still PHP 4, my version: ' . PHP_VERSION . "\n";
}
?>
```

### 注释

> **Note**:
>
> **`PHP_VERSION`** 常量包含了当前 PHP 的版本。

> **Note**:
>
> 注意，类似 5.3.0-dev
> 的预发行版本，被认为是低于它们的最终发行版本（就像 5.3.0）。

> **Note**:
>
> 指定类似 *alpha*、*beta* 的版本字符串是大小写敏感的。
> 版本字符串的来源若不遵循 PHP 标准，可能需要在调用 <span
> class="function">version\_compare</span> 之前先用 <span
> class="function">strtolower</span> 转成小写。

### 参见

-   <span class="function">phpversion</span>
-   <span class="function">php\_uname</span>
-   <span class="function">function\_exists</span>

zend\_logo\_guid
================

获取 Zend guid

### 说明

<span class="type">string</span> <span
class="methodname">zend\_logo\_guid</span> ( <span
class="methodparam">void</span> )

该函数返回了一个 ID，能够使用内置的图像来显示 Zend logo。

**Warning**

自 PHP 5.5.0 起，已经*废弃*并*移除*此函数。

### 返回值

返回 *PHPE9568F35-D428-11d2-A769-00AA001ACF42*.

### 更新日志

| 版本  | 说明                                                             |
|-------|------------------------------------------------------------------|
| 5.5.0 | <span class="function">zend\_logo\_guid</span> 从 PHP 中移除了。 |

### 范例

**示例 \#1 <span class="function">zend\_logo\_guid</span> 例子**

``` php
<?php

echo '<img src="' . $_SERVER['PHP_SELF'] .
     '?=' . zend_logo_guid() . '" alt="Zend Logo !" />';

?>
```

### 参见

-   <span class="function">php\_logo\_guid</span>

zend\_thread\_id
================

返回当前线程的唯一识别符

### 说明

<span class="type">int</span> <span
class="methodname">zend\_thread\_id</span> ( <span
class="methodparam">void</span> )

该函数返回当前线程的唯一识别符。

### 返回值

以整型（integer）返回线程的 ID。

### 范例

**示例 \#1 <span class="function">zend\_thread\_id</span> 例子**

``` php
<?php
$thread_id = zend_thread_id();

echo 'Current thread id is: ' . $thread_id;
?>
```

以上例程的输出类似于：

    Current thread id is: 7864

### 注释

> **Note**:
>
> 该函数仅在以下情况有效：PHP 内置 ZTS（Zend 线程安全）的支持，
> 并开启调试模式（*--enable-debug*）时。

zend\_version
=============

获取当前 Zend 引擎的版本

### 说明

<span class="type">string</span> <span
class="methodname">zend\_version</span> ( <span
class="methodparam">void</span> )

获取当前运行的 Zend 引擎的版本字符串。

### 返回值

获取 Zend 引擎的版本数字的字符串。

### 范例

**示例 \#1 <span class="function">zend\_version</span> 例子**

``` php
<?php
echo "Zend engine version: " . zend_version();
?>
```

以上例程的输出类似于：

    Zend engine version: 2.2.0

### 参见

-   <span class="function">phpinfo</span>
-   <span class="function">phpcredits</span>
-   <span class="function">php\_logo\_guid</span>
-   <span class="function">phpversion</span>

**目录**

-   [assert\_options](/ref/info.html#assert_options) —
    设置/获取断言的各种标志
-   [assert](/ref/info.html#assert) — 检查一个断言是否为 FALSE
-   [cli\_get\_process\_title](/ref/info.html#cli_get_process_title) —
    Returns the current process title
-   [cli\_set\_process\_title](/ref/info.html#cli_set_process_title) —
    Sets the process title
-   [dl](/ref/info.html#dl) — 运行时载入一个 PHP 扩展
-   [extension\_loaded](/ref/info.html#extension_loaded) —
    检查一个扩展是否已经加载
-   [gc\_collect\_cycles](/ref/info.html#gc_collect_cycles) —
    强制收集所有现存的垃圾循环周期
-   [gc\_disable](/ref/info.html#gc_disable) — 停用循环引用收集器
-   [gc\_enable](/ref/info.html#gc_enable) — 激活循环引用收集器
-   [gc\_enabled](/ref/info.html#gc_enabled) — 返回循环引用计数器的状态
-   [gc\_mem\_caches](/ref/info.html#gc_mem_caches) — Reclaims memory
    used by the Zend Engine memory manager
-   [gc\_status](/ref/info.html#gc_status) — Gets information about the
    garbage collector
-   [get\_cfg\_var](/ref/info.html#get_cfg_var) — 获取 PHP 配置选项的值
-   [get\_current\_user](/ref/info.html#get_current_user) — 获取当前 PHP
    脚本所有者名称
-   [get\_defined\_constants](/ref/info.html#get_defined_constants) —
    返回所有常量的关联数组，键是常量名，值是常量值
-   [get\_extension\_funcs](/ref/info.html#get_extension_funcs) —
    返回模块函数名称的数组
-   [get\_include\_path](/ref/info.html#get_include_path) — 获取当前的
    include\_path 配置选项
-   [get\_included\_files](/ref/info.html#get_included_files) — 返回被
    include 和 require 文件名的 array
-   [get\_loaded\_extensions](/ref/info.html#get_loaded_extensions) —
    返回所有编译并加载模块名的 array
-   [get\_magic\_quotes\_gpc](/ref/info.html#get_magic_quotes_gpc) —
    获取当前 magic\_quotes\_gpc 的配置选项设置
-   [get\_magic\_quotes\_runtime](/ref/info.html#get_magic_quotes_runtime)
    — 获取当前 magic\_quotes\_runtime 配置选项的激活状态
-   [get\_required\_files](/ref/info.html#get_required_files) — 别名
    get\_included\_files
-   [get\_resources](/ref/info.html#get_resources) — Returns active
    resources
-   [getenv](/ref/info.html#getenv) — 获取一个环境变量的值
-   [getlastmod](/ref/info.html#getlastmod) — 获取页面最后修改的时间
-   [getmygid](/ref/info.html#getmygid) — 获取当前 PHP 脚本拥有者的 GID
-   [getmyinode](/ref/info.html#getmyinode) —
    获取当前脚本的索引节点（inode）
-   [getmypid](/ref/info.html#getmypid) — 获取 PHP 进程的 ID
-   [getmyuid](/ref/info.html#getmyuid) — 获取 PHP 脚本所有者的 UID
-   [getopt](/ref/info.html#getopt) — 从命令行参数列表中获取选项
-   [getrusage](/ref/info.html#getrusage) — 获取当前资源使用状况
-   [ini\_alter](/ref/info.html#ini_alter) — 别名 ini\_set
-   [ini\_get\_all](/ref/info.html#ini_get_all) — 获取所有配置选项
-   [ini\_get](/ref/info.html#ini_get) — 获取一个配置选项的值
-   [ini\_restore](/ref/info.html#ini_restore) — 恢复配置选项的值
-   [ini\_set](/ref/info.html#ini_set) — 为一个配置选项设置值
-   [magic\_quotes\_runtime](/ref/info.html#magic_quotes_runtime) — 别名
    set\_magic\_quotes\_runtime
-   [main](/ref/info.html#main) — 虚拟的main
-   [memory\_get\_peak\_usage](/ref/info.html#memory_get_peak_usage) —
    返回分配给 PHP 内存的峰值
-   [memory\_get\_usage](/ref/info.html#memory_get_usage) — 返回分配给
    PHP 的内存量
-   [php\_ini\_loaded\_file](/ref/info.html#php_ini_loaded_file) —
    取得已加载的 php.ini 文件的路径
-   [php\_ini\_scanned\_files](/ref/info.html#php_ini_scanned_files) —
    返回从额外 ini 目录里解析的 .ini 文件列表
-   [php\_logo\_guid](/ref/info.html#php_logo_guid) — 获取 logo 的 guid
-   [php\_sapi\_name](/ref/info.html#php_sapi_name) — 返回 web 服务器和
    PHP 之间的接口类型
-   [php\_uname](/ref/info.html#php_uname) — 返回运行 PHP
    的系统的有关信息
-   [phpcredits](/ref/info.html#phpcredits) — 打印 PHP 贡献者名单
-   [phpinfo](/ref/info.html#phpinfo) — 输出关于 PHP 配置的信息
-   [phpversion](/ref/info.html#phpversion) — 获取当前的PHP版本
-   [putenv](/ref/info.html#putenv) — 设置环境变量的值
-   [restore\_include\_path](/ref/info.html#restore_include_path) — 还原
    include\_path 配置选项的值
-   [set\_include\_path](/ref/info.html#set_include_path) — 设置
    include\_path 配置选项
-   [set\_magic\_quotes\_runtime](/ref/info.html#set_magic_quotes_runtime)
    — 设置当前 magic\_quotes\_runtime 配置选项的激活状态
-   [set\_time\_limit](/ref/info.html#set_time_limit) —
    设置脚本最大执行时间
-   [sys\_get\_temp\_dir](/ref/info.html#sys_get_temp_dir) —
    返回用于临时文件的目录
-   [version\_compare](/ref/info.html#version_compare) — 对比两个「PHP
    规范化」的版本数字字符串
-   [zend\_logo\_guid](/ref/info.html#zend_logo_guid) — 获取 Zend guid
-   [zend\_thread\_id](/ref/info.html#zend_thread_id) —
    返回当前线程的唯一识别符
-   [zend\_version](/ref/info.html#zend_version) — 获取当前 Zend
    引擎的版本
