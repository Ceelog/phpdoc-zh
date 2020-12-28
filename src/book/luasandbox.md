LuaSandbox
==========

**目录**

-   [简介](/intro/luasandbox.html)
-   [安装／配置](/luasandbox/setup.html)
    -   [需求](/luasandbox/setup.html#需求)
    -   [安装](/luasandbox/setup.html#安装)
    -   [运行时配置](/luasandbox/setup.html#运行时配置)
    -   [资源类型](/luasandbox/setup.html#资源类型)
-   [Differences from Standard
    Lua](/reference/luasandbox/differences.html)
-   [范例](/luasandbox/examples.html)
    -   [Basic usage for
        LuaSandbox](/luasandbox/examples.html#Basic%20usage%20for%20LuaSandbox)
-   [LuaSandbox](/class/luasandbox.html) — The LuaSandbox class
    -   [LuaSandbox::callFunction](/class/luasandbox.html#LuaSandbox::callFunction)
        — Call a function in a Lua global variable
    -   [LuaSandbox::disableProfiler](/class/luasandbox.html#LuaSandbox::disableProfiler)
        — Disable the profiler
    -   [LuaSandbox::enableProfiler](/class/luasandbox.html#LuaSandbox::enableProfiler)
        — Enable the profiler.
    -   [LuaSandbox::getCPUUsage](/class/luasandbox.html#LuaSandbox::getCPUUsage)
        — Fetch the current CPU time usage of the Lua environment
    -   [LuaSandbox::getMemoryUsage](/class/luasandbox.html#LuaSandbox::getMemoryUsage)
        — Fetch the current memory usage of the Lua environment
    -   [LuaSandbox::getPeakMemoryUsage](/class/luasandbox.html#LuaSandbox::getPeakMemoryUsage)
        — Fetch the peak memory usage of the Lua environment
    -   [LuaSandbox::getProfilerFunctionReport](/class/luasandbox.html#LuaSandbox::getProfilerFunctionReport)
        — Fetch profiler data
    -   [LuaSandbox::getVersionInfo](/class/luasandbox.html#LuaSandbox::getVersionInfo)
        — Return the versions of LuaSandbox and Lua
    -   [LuaSandbox::loadBinary](/class/luasandbox.html#LuaSandbox::loadBinary)
        — Load a precompiled binary chunk into the Lua environment
    -   [LuaSandbox::loadString](/class/luasandbox.html#LuaSandbox::loadString)
        — Load Lua code into the Lua environment
    -   [LuaSandbox::pauseUsageTimer](/class/luasandbox.html#LuaSandbox::pauseUsageTimer)
        — Pause the CPU usage timer
    -   [LuaSandbox::registerLibrary](/class/luasandbox.html#LuaSandbox::registerLibrary)
        — Register a set of PHP functions as a Lua library
    -   [LuaSandbox::setCPULimit](/class/luasandbox.html#LuaSandbox::setCPULimit)
        — Set the CPU time limit for the Lua environment
    -   [LuaSandbox::setMemoryLimit](/class/luasandbox.html#LuaSandbox::setMemoryLimit)
        — Set the memory limit for the Lua environment
    -   [LuaSandbox::unpauseUsageTimer](/class/luasandbox.html#LuaSandbox::unpauseUsageTimer)
        — Unpause the timer paused by LuaSandbox::pauseUsageTimer
    -   [LuaSandbox::wrapPhpFunction](/class/luasandbox.html#LuaSandbox::wrapPhpFunction)
        — Wrap a PHP callable in a LuaSandboxFunction
-   [LuaSandboxFunction](/class/luasandboxfunction.html) — The
    LuaSandboxFunction class
    -   [LuaSandboxFunction::call](/class/luasandboxfunction.html#LuaSandboxFunction::call)
        — Call a Lua function
    -   [LuaSandboxFunction::\_\_construct](/class/luasandboxfunction.html#LuaSandboxFunction::__construct)
        — Unused
    -   [LuaSandboxFunction::dump](/class/luasandboxfunction.html#LuaSandboxFunction::dump)
        — Dump the function as a binary blob
-   [LuaSandboxError](/class/luasandboxerror.html) — The LuaSandboxError
    class
-   [LuaSandboxErrorError](/class/luasandboxerrorerror.html) — The
    LuaSandboxErrorError class
-   [LuaSandboxFatalError](/class/luasandboxfatalerror.html) — The
    LuaSandboxFatalError class
-   [LuaSandboxMemoryError](/class/luasandboxmemoryerror.html) — The
    LuaSandboxMemoryError class
-   [LuaSandboxRuntimeError](/class/luasandboxruntimeerror.html) — The
    LuaSandboxRuntimeError class
-   [LuaSandboxSyntaxError](/class/luasandboxsyntaxerror.html) — The
    LuaSandboxSyntaxError class
-   [LuaSandboxTimeoutError](/class/luasandboxtimeouterror.html) — The
    LuaSandboxTimeoutError class

简介
----

The LuaSandbox class creates a Lua environment and allows for execution
of Lua code.

类摘要
------

**LuaSandbox**

<span class="ooclass"> class **LuaSandbox** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandbox::SAMPLES` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandbox::SECONDS` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandbox::PERCENT` <span class="initializer"> = 2</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">bool</span></span> <span
class="methodname">callFunction</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">mixed</span> `$args`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">disableProfiler</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">enableProfiler</span> (\[ <span
class="methodparam"><span class="type">float</span> `$period`<span
class="initializer"> = 0.02</span></span> \] )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getCPUUsage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMemoryUsage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPeakMemoryUsage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getProfilerFunctionReport</span> (\[ <span
class="methodparam"><span class="type">int</span> `$units`<span
class="initializer"> = LuaSandbox::SECONDS</span></span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getVersionInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">LuaSandboxFunction</span> <span
class="methodname">loadBinary</span> ( <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">string</span> `$chunkName`<span
class="initializer"> = ''</span></span> \] )

<span class="modifier">public</span> <span
class="type">LuaSandboxFunction</span> <span
class="methodname">loadString</span> ( <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">string</span> `$chunkName`<span
class="initializer"> = ''</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">pauseUsageTimer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">registerLibrary</span> ( <span
class="methodparam"><span class="type">string</span> `$libname`</span> ,
<span class="methodparam"><span class="type">array</span>
`$functions`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCPULimit</span> ( <span
class="methodparam"><span class="type"><span
class="type">float</span><span class="type">bool</span></span>
`$limit`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMemoryLimit</span> ( <span
class="methodparam"><span class="type">int</span> `$limit`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unpauseUsageTimer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">LuaSandboxFunction</span> <span
class="methodname">wrapPhpFunction</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> )

}

预定义常量
----------

**`LuaSandbox::SAMPLES`**  
Used with <span
class="methodname">LuaSandbox::getProfilerFunctionReport</span> to
return timings in samples.

**`LuaSandbox::SECONDS`**  
Used with <span
class="methodname">LuaSandbox::getProfilerFunctionReport</span> to
return timings in seconds.

**`LuaSandbox::PERCENT`**  
Used with <span
class="methodname">LuaSandbox::getProfilerFunctionReport</span> to
return timings in percentages of the total.

LuaSandbox::callFunction
========================

Call a function in a Lua global variable

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">bool</span></span> <span
class="methodname">LuaSandbox::callFunction</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$args`</span>
)

Calls a function in a Lua global variable.

If the name contains "." characters, the function is located via
recursive table accesses, as if the name were a Lua expression.

If the variable does not exist, or is not a function, false will be
returned and a warning issued.

For more information about calling Lua functions and the return values,
see <span class="methodname">LuaSandboxFunction::call</span>.

### 参数

`name`  
Lua variable name.

`args`  
Arguments to the function.

### 返回值

Returns an <span class="type">array</span> of values returned by the Lua
function, which may be empty, or *false* in case of failure.

### 范例

**示例 \#1 Calling a Lua function**

``` php
<?php

// create a new LuaSandbox
$sandbox = new LuaSandbox();

// Call Lua's string.match
$captures = $sandbox->callFunction( 'string.match', $string, $pattern );

?>
```

LuaSandbox::disableProfiler
===========================

Disable the profiler

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LuaSandbox::disableProfiler</span> ( <span
class="methodparam">void</span> )

Disables the profiler.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">LuaSandbox::enableProfiler</span>
-   <span
    class="methodname">LuaSandbox::getProfilerFunctionReport</span>

LuaSandbox::enableProfiler
==========================

Enable the profiler.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">LuaSandbox::enableProfiler</span> (\[ <span
class="methodparam"><span class="type">float</span> `$period`<span
class="initializer"> = 0.02</span></span> \] )

Enables the profiler. Profiling will begin when Lua code is entered.

The profiler periodically samples the Lua environment to record the
running function. Testing indicates that at least on Linux, setting a
period less than 1ms will lead to a high overrun count but no
performance problems.

### 参数

`period`  
Sampling period in seconds.

### 返回值

Returns a boolean indicating whether the profiler is enabled.

### 参见

-   <span class="methodname">LuaSandbox::disableProfiler</span>
-   <span
    class="methodname">LuaSandbox::getProfilerFunctionReport</span>

LuaSandbox::getCPUUsage
=======================

Fetch the current CPU time usage of the Lua environment

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">LuaSandbox::getCPUUsage</span> ( <span
class="methodparam">void</span> )

Fetches the current CPU time usage of the Lua environment.

This includes time spent in PHP callbacks.

### 参数

此函数没有参数。

### 返回值

Returns the current CPU time usage in seconds.

> **Note**:
>
> On Windows, this function always returns zero. On operating systems
> that do not support **`CLOCK_THREAD_CPUTIME_ID`**, such as FreeBSD and
> Mac OS X, this function will return the elapsed wall-clock time, not
> CPU time.

### 参见

-   <span class="methodname">LuaSandbox::getMemoryUsage</span>
-   <span class="methodname">LuaSandbox::getPeakMemoryUsage</span>
-   <span class="methodname">LuaSandbox::setCPULimit</span>

LuaSandbox::getMemoryUsage
==========================

Fetch the current memory usage of the Lua environment

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">LuaSandbox::getMemoryUsage</span> ( <span
class="methodparam">void</span> )

Fetches the current memory usage of the Lua environment.

### 参数

此函数没有参数。

### 返回值

Returns the current memory usage in bytes.

### 参见

-   <span class="methodname">LuaSandbox::getPeakMemoryUsage</span>
-   <span class="methodname">LuaSandbox::getCPUUsage</span>
-   <span class="methodname">LuaSandbox::setMemoryLimit</span>

LuaSandbox::getPeakMemoryUsage
==============================

Fetch the peak memory usage of the Lua environment

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">LuaSandbox::getPeakMemoryUsage</span> ( <span
class="methodparam">void</span> )

Fetches the peak memory usage of the Lua environment.

### 参数

此函数没有参数。

### 返回值

Returns the peak memory usage in bytes.

### 参见

-   <span class="methodname">LuaSandbox::getMemoryUsage</span>
-   <span class="methodname">LuaSandbox::getCPUUsage</span>
-   <span class="methodname">LuaSandbox::setMemoryLimit</span>

LuaSandbox::getProfilerFunctionReport
=====================================

Fetch profiler data

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">LuaSandbox::getProfilerFunctionReport</span>
(\[ <span class="methodparam"><span class="type">int</span>
`$units`<span class="initializer"> = LuaSandbox::SECONDS</span></span>
\] )

For a profiling instance previously started by <span
class="methodname">LuaSandbox::enableProfiler</span>, get a report of
the cost of each function.

The measurement unit used for the cost is determined by the `$units`
parameter:

**`LuaSandbox::SAMPLES`**  
Measure in number of samples.

**`LuaSandbox::SECONDS`**  
Measure in seconds of CPU time.

**`LuaSandbox::PERCENT`**  
Measure percentage of CPU time.

### 参数

`units`  
Measurement unit constant.

### 返回值

Returns profiler measurements, sorted in descending order, as an
associative <span class="type">array</span>. Keys are the Lua function
names (with source file and line defined in angle brackets), values are
the measurements as <span class="type">int</span> or <span
class="type">float</span>.

> **Note**:
>
> On Windows, this function always returns an empty array. On operating
> systems that do not support **`CLOCK_THREAD_CPUTIME_ID`**, such as
> FreeBSD and Mac OS X, this function will report the elapsed wall-clock
> time, not CPU time.

### 范例

**示例 \#1 Profiling Lua code**

``` php
<?php

// create a new LuaSandbox
$sandbox = new LuaSandbox();

// Start the profiler
$sandbox->enableProfiler( 0.01 );

// ... Execute some Lua code here ...

// Fetch the profiler data
$data = $sandbox->getProfilerFunctionReport();

?>
```

LuaSandbox::getVersionInfo
==========================

Return the versions of LuaSandbox and Lua

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">LuaSandbox::getVersionInfo</span> ( <span
class="methodparam">void</span> )

Returns the versions of LuaSandbox and Lua.

### 参数

此函数没有参数。

### 返回值

Returns an array with two keys:

| element    | type                             | description                                                                                  |
|------------|----------------------------------|----------------------------------------------------------------------------------------------|
| LuaSandbox | <span class="type">string</span> | The version of the LuaSandbox extension.                                                     |
| Lua        | <span class="type">string</span> | The library name and version as defined by the LUA\_RELEASE macro, for example, "Lua 5.1.5". |

LuaSandbox::loadBinary
======================

Load a precompiled binary chunk into the Lua environment

### 说明

<span class="modifier">public</span> <span
class="type">LuaSandboxFunction</span> <span
class="methodname">LuaSandbox::loadBinary</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$chunkName`<span class="initializer"> = ''</span></span> \] )

Loads data generated by <span
class="methodname">LuaSandboxFunction::dump</span>.

### 参数

`code`  
Data from <span class="methodname">LuaSandboxFunction::dump</span>.

`chunkName`  
Name for the loaded function.

### 返回值

Returns a <span class="classname">LuaSandboxFunction</span>.

### 参见

-   <span class="methodname">LuaSandbox::loadString</span>

LuaSandbox::loadString
======================

Load Lua code into the Lua environment

### 说明

<span class="modifier">public</span> <span
class="type">LuaSandboxFunction</span> <span
class="methodname">LuaSandbox::loadString</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$chunkName`<span class="initializer"> = ''</span></span> \] )

Loads Lua code into the Lua environment.

This is the equivalent of standard Lua's *loadstring()* function.

### 参数

`code`  
Lua code.

`chunkName`  
Name for the loaded chunk, for use in error traces.

### 返回值

Returns a <span class="classname">LuaSandboxFunction</span> which, when
executed, will execute the passed `$code`.

### 范例

**示例 \#1 Loading code into Lua**

``` php
<?php

// create a new LuaSandbox
$sandbox = new LuaSandbox();

// Load the code
$function = $sandbox->loadString(
<<<CODE
    return "Hello, world"
CODE
);

// Execute the loaded code
var_dump( $function->call() );

?>
```

以上例程会输出：

    array(1) {
      [0]=>
      string(12) "Hello, world"
    }

### 参见

-   <span class="methodname">LuaSandbox::registerLibrary</span>
-   <span class="methodname">LuaSandbox::wrapPhpFunction</span>

LuaSandbox::pauseUsageTimer
===========================

Pause the CPU usage timer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">LuaSandbox::pauseUsageTimer</span> ( <span
class="methodparam">void</span> )

Pauses the CPU usage timer.

This only has effect when called from within a callback from Lua. When
execution returns to Lua, the timer will be automatically unpaused. If a
new call into Lua is made, the timer will be unpaused for the duration
of that call.

If a PHP callback calls into Lua again with timer not paused, and then
that Lua function calls into PHP again, the second PHP call will not be
able to pause the timer. The logic is that even though the second PHP
call would avoid counting the CPU usage against the limit, the first
call still counts it.

### 参数

此函数没有参数。

### 返回值

Returns a <span class="type">bool</span> indicating whether the timer is
now paused.

### 范例

**示例 \#1 Manipulating the usage timer**

``` php
<?php

// create a new LuaSandbox and set a CPU limit
$sandbox = new LuaSandbox();
$sandbox->setCPULimit( 1 );

function doWait( $t ) {
    $end = microtime( true ) + $t;
    while ( microtime( true ) < $end ) {
        // waste CPU cycles
    }
}

// Register a PHP callback
$sandbox->registerLibrary( 'php', [
    'test' => function () use ( $sandbox ) {
        $sandbox->pauseUsageTimer();
        doWait( 5 );

        $sandbox->unpauseUsageTimer();
        doWait( 0.1 );
    },
    'test2' => function () use ( $sandbox ) {
        $sandbox->pauseUsageTimer();
        $sandbox->unpauseUsageTimer();
        doWait( 1.1 );
    }
] );

echo "This should not time out...\n";
$sandbox->loadString( 'php.test()' )->call();

echo "This should time out.\n";
try {
    $sandbox->loadString( 'php.test2()' )->call();
    echo "It did not?\n";
} catch ( LuaSandboxTimeoutError $ex ) {
    echo "It did! " . $ex->getMessage() . "\n";
}

?>
```

以上例程会输出：

    This should not time out...
    This should time out.
    It did! The maximum execution time for this script was exceeded

### 参见

-   <span class="methodname">LuaSandbox::setCPULimit</span>
-   <span class="methodname">LuaSandbox::unpauseUsageTimer</span>

LuaSandbox::registerLibrary
===========================

Register a set of PHP functions as a Lua library

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LuaSandbox::registerLibrary</span> ( <span
class="methodparam"><span class="type">string</span> `$libname`</span> ,
<span class="methodparam"><span class="type">array</span>
`$functions`</span> )

Registers a set of PHP functions as a Lua library, so that Lua can call
the relevant PHP code.

For more information about calling Lua functions and the return values,
see <span class="methodname">LuaSandboxFunction::call</span>.

### 参数

`libname`  
The name of the library. In the Lua state, the global variable of this
name will be set to the table of functions. If the table already exists,
the new functions will be added to it.

`functions`  
An <span class="type">array</span>, where each key is a function name,
and each value is a corresponding PHP <span
class="type">callable</span>.

### 返回值

没有返回值。

### 范例

**示例 \#1 Registering PHP functions to call from Lua**

``` php
<?php

// create a new LuaSandbox
$sandbox = new LuaSandbox();

// Register some functions in the Lua environment

function frobnosticate( $v ) {
    return [ $v + 42 ];
}

$sandbox->registerLibrary( 'php', [
    'frobnosticate' => 'frobnosticate',
    'output' => function ( $string ) {
        echo "$string\n";
    },
    'error' => function () {
        throw new LuaSandboxRuntimeError( "Something is wrong" );
    }
] );

?>
```

### 参见

-   <span class="methodname">LuaSandbox::loadString</span>
-   <span class="methodname">LuaSandbox::wrapPhpFunction</span>

LuaSandbox::setCPULimit
=======================

Set the CPU time limit for the Lua environment

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LuaSandbox::setCPULimit</span> ( <span
class="methodparam"><span class="type"><span
class="type">float</span><span class="type">bool</span></span>
`$limit`</span> )

Sets the CPU time limit for the Lua environment.

If the total user and system time used by the environment after the call
to this method exceeds this limit, a <span
class="classname">LuaSandboxTimeoutError</span> exception is thrown.

Time used in PHP callbacks is included in the limit.

Setting the time limit from a callback while Lua is running causes the
timer to be reset, or started if it was not already running.

> **Note**:
>
> On Windows, the CPU limit will be ignored. On operating systems that
> do not support **`CLOCK_THREAD_CPUTIME_ID`**, such as FreeBSD and Mac
> OS X, wall-clock time rather than CPU time will be limited.

### 参数

`limit`  
Limit as a <span class="type">float</span> in seconds, or *false* for no
limit.

### 返回值

没有返回值。

### 范例

**示例 \#1 Calling a Lua function**

``` php
<?php

// create a new LuaSandbox
$sandbox = new LuaSandbox();

// set a time limit
$sandbox->setCPULimit( 2 );

// Run Lua code
$sandbox->loadString( 'while true do end' )->call();

?>
```

以上例程的输出类似于：

    PHP Fatal error:  Uncaught LuaSandboxTimeoutError: The maximum execution time for this script was exceeded

### 参见

-   <span class="methodname">LuaSandbox::getCPUUsage</span>
-   <span class="methodname">LuaSandbox::setMemoryLimit</span>

LuaSandbox::setMemoryLimit
==========================

Set the memory limit for the Lua environment

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LuaSandbox::setMemoryLimit</span> ( <span
class="methodparam"><span class="type">int</span> `$limit`</span> )

Sets the memory limit for the Lua environment.

If this limit is exceeded, a <span
class="classname">LuaSandboxMemoryError</span> exception is thrown.

### 参数

`limit`  
Memory limit in bytes.

### 返回值

没有返回值。

### 范例

**示例 \#1 Calling a Lua function**

``` php
<?php

// create a new LuaSandbox
$sandbox = new LuaSandbox();

// set a memory limit
$sandbox->setMemoryLimit( 50 * 1024 * 1024 );

// Run Lua code
$sandbox->loadString( 'local x = "x"; while true do x = x .. x; end' )->call();

?>
```

以上例程的输出类似于：

    PHP Fatal error:  Uncaught LuaSandboxMemoryError: not enough memory

### 参见

-   <span class="methodname">LuaSandbox::getMemoryUsage</span>
-   <span class="methodname">LuaSandbox::getPeakMemoryUsage</span>
-   <span class="methodname">LuaSandbox::setCPULimit</span>

LuaSandbox::unpauseUsageTimer
=============================

Unpause the timer paused by <span
class="methodname">LuaSandbox::pauseUsageTimer</span>

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">LuaSandbox::unpauseUsageTimer</span> ( <span
class="methodparam">void</span> )

Unpauses the timer paused by <span
class="methodname">LuaSandbox::pauseUsageTimer</span>.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">LuaSandbox::pauseUsageTimer</span>
-   <span class="methodname">LuaSandbox::setCPULimit</span>

LuaSandbox::wrapPhpFunction
===========================

Wrap a PHP callable in a <span
class="classname">LuaSandboxFunction</span>

### 说明

<span class="modifier">public</span> <span
class="type">LuaSandboxFunction</span> <span
class="methodname">LuaSandbox::wrapPhpFunction</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> )

Wraps a PHP callable in a <span
class="classname">LuaSandboxFunction</span>, so it can be passed into
Lua as an anonymous function.

The function must return either an array of values (which may be empty),
or **`null`** which is equivalent to returning the empty array.

Exceptions will be raised as errors in Lua, however only <span
class="classname">LuaSandboxRuntimeError</span> exceptions may be caught
inside Lua with *pcall()* or *xpcall()*.

For more information about calling Lua functions and the return values,
see <span class="methodname">LuaSandboxFunction::call</span>.

### 参数

`function`  
Callable to wrap.

### 返回值

Returns a <span class="classname">LuaSandboxFunction</span>.

### 参见

-   <span class="methodname">LuaSandbox::loadString</span>
-   <span class="methodname">LuaSandbox::registerLibrary</span>

简介
----

Represents a Lua function, allowing it to be called from PHP.

A LuaSandboxFunction may be obtained as a return value from Lua, as a
parameter passed to a callback from Lua, or by using <span
class="methodname">LuaSandbox::wrapPhpFunction</span>, <span
class="methodname">LuaSandbox::loadString</span>, or <span
class="methodname">LuaSandbox::loadBinary</span>.

类摘要
------

**LuaSandboxFunction**

<span class="ooclass"> class **LuaSandboxFunction** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">bool</span></span> <span
class="methodname">call</span> ( <span class="methodparam"><span
class="type">string</span> `$args`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">dump</span> ( <span
class="methodparam">void</span> )

}

LuaSandboxFunction::call
========================

Call a Lua function

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">bool</span></span> <span
class="methodname">LuaSandboxFunction::call</span> ( <span
class="methodparam"><span class="type">string</span> `$args`</span> )

Calls a Lua function.

Errors considered to be the fault of the PHP code will result in the
function returning *false* and **`E_WARNING`** being raised, for
example, a <span class="type">resource</span> type being used as an
argument. Lua errors will result in a <span
class="classname">LuaSandboxRuntimeError</span> exception being thrown.

PHP and Lua types are converted as follows:

-   PHP **`null`** is Lua *nil*, and vice versa.

-   PHP <span class="type">int</span>s and <span
    class="type">float</span>s are converted to Lua numbers. Infinity
    and **`NAN`** are supported.

-   Lua numbers without a fractional part between approximately
    *-2\*\*53* and *2\*\*53* are converted to PHP <span
    class="type">int</span>s, with others being converted to PHP <span
    class="type">float</span>s.

-   PHP <span class="type">bool</span>s are Lua booleans, and vice
    versa.

-   PHP <span class="type">string</span>s are Lua strings, and vice
    versa.

-   Lua functions are PHP <span
    class="classname">LuaSandboxFunction</span> objects, and vice versa.
    General PHP <span class="type">callable</span>s are not supported.

-   PHP <span class="type">array</span>s are converted to Lua tables,
    and vice versa.

    -   Note that Lua typically indexes arrays from 1, while PHP indexes
        arrays from 0. No adjustment is made for these differing
        conventions.

    -   Self-referential arrays are not supported in either direction.

    -   PHP references are dereferenced.

    -   Lua *\_\_pairs* and *\_\_ipairs* are processed. *\_\_index* is
        ignored.

    -   When converting from PHP to Lua, integer keys between *-2\*\*53*
        and *2\*\*53* are represented as Lua numbers. All other keys are
        represented as Lua strings.

    -   When converting from Lua to PHP, keys other than strings and
        numbers will result in an error, as will collisions when
        converting numbers to strings or vice versa (since PHP considers
        things like *$a\[0\]* and *$a\["0"\]* as being equivalent).

-   All other types are unsupported and will raise an error/exception,
    including general PHP <span class="type">object</span>s and Lua
    userdata and thread types.

Lua functions inherently return a list of results. So on success, this
method returns an <span class="type">array</span> containing all of the
values returned by Lua, with <span class="type">int</span> keys starting
from zero. Lua may return no results, in which case an empty array is
returned.

### 参数

`args`  
Arguments passed to the function.

### 返回值

Returns an <span class="type">array</span> of values returned by the
function, which may be empty, or *false* on error.

LuaSandboxFunction::\_\_construct
=================================

Unused

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">LuaSandboxFunction::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="classname">LuaSandboxFunction</span> are obtained as a
return value from Lua, as a parameter passed to a callback from Lua, or
by using <span class="methodname">LuaSandbox::wrapPhpFunction</span>,
<span class="methodname">LuaSandbox::loadString</span>, or <span
class="methodname">LuaSandbox::loadBinary</span>. They cannot be
constructed directly.

### 参数

此函数没有参数。

LuaSandboxFunction::dump
========================

Dump the function as a binary blob

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">LuaSandboxFunction::dump</span> ( <span
class="methodparam">void</span> )

Dumps the function as a binary blob.

### 参数

此函数没有参数。

### 返回值

Returns a string that may be passed to <span
class="methodname">LuaSandbox::loadBinary</span>.

简介
----

Base class for LuaSandbox exceptions

类摘要
------

**LuaSandboxError**

<span class="ooclass"> class **LuaSandboxError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandboxError::RUN` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandboxError::SYNTAX` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandboxError::MEM` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`LuaSandboxError::ERR` <span class="initializer"> = 5</span> ;

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`LuaSandboxError::RUN`**  

**`LuaSandboxError::SYNTAX`**  

**`LuaSandboxError::MEM`**  

**`LuaSandboxError::ERR`**  

简介
----

Exception thrown when Lua encounters an error inside an error handler.

类摘要
------

**LuaSandboxErrorError**

<span class="ooclass"> class **LuaSandboxErrorError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LuaSandboxFatalError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Uncatchable LuaSandbox exceptions.

These may not be caught inside Lua using *pcall()* or *xpcall()*.

类摘要
------

**LuaSandboxFatalError**

<span class="ooclass"> class **LuaSandboxFatalError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LuaSandboxError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Exception thrown when Lua cannot allocate memory.

类摘要
------

**LuaSandboxMemoryError**

<span class="ooclass"> class **LuaSandboxMemoryError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LuaSandboxFatalError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

参见
----

-   <span class="methodname">LuaSandbox::setMemoryLimit</span>

简介
----

Catchable LuaSandbox runtime exceptions.

These may be caught inside Lua using *pcall()* or *xpcall()*.

类摘要
------

**LuaSandboxRuntimeError**

<span class="ooclass"> class **LuaSandboxRuntimeError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LuaSandboxError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Exception thrown when Lua code cannot be parsed.

类摘要
------

**LuaSandboxSyntaxError**

<span class="ooclass"> class **LuaSandboxSyntaxError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LuaSandboxFatalError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Exception thrown when the configured CPU time limit is exceeded.

类摘要
------

**LuaSandboxTimeoutError**

<span class="ooclass"> class **LuaSandboxTimeoutError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LuaSandboxFatalError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

参见
----

-   <span class="methodname">LuaSandbox::setCPULimit</span>
