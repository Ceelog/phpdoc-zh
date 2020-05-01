参考一下 <a href="/ref/posix.html" class="link">POSIX functions</a>
对有助于理解使用。

pcntl\_alarm
============

为进程设置一个alarm闹钟信号

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_alarm</span> ( <span class="methodparam"><span
class="type">int</span> `$seconds`</span> )

创建一个计时器，在指定的秒数后向进程发送一个**`SIGALRM`**信号。每次对
<span
class="function">pcntl\_alarm</span>的调用都会取消之前设置的alarm信号。

### 参数

`seconds`  
等待的秒数。如果`seconds`设置为0,将不会创建alarm信号。

### 返回值

返回上次alarm调度（离alarm信号发送）剩余的秒数，或者之前没有alarm调度（译注：或者之前调度已完成）
时返回*0*。

pcntl\_async\_signals
=====================

Enable/disable asynchronous signal handling or return the old setting

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_async\_signals</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$on`<span
class="initializer"> = **`NULL`**</span></span> \] )

If the `on` parameter is omitted, <span
class="function">pcntl\_async\_signals</span> returns whether
asynchronous signal handling is enabled. Otherwise, asynchronous signal
handling is enabled or disabled.

### 参数

`on`  
Whether asynchronous signal handling should be enabled.

### 返回值

When used as getter (that is without the optional parameter) it returns
whether asynchronous signal handling is enabled. When used as setter
(that is with the optional parameter given), it returns whether
asynchronous signal handling was enabled *before* the function call.

### 参见

-   <a href="/control-structures/declare.html" class="link">declare</a>

pcntl\_errno
============

别名 <span class="function">pcntl\_get\_last\_error</span>

### 说明

此函数是该函数的别名： <span
class="function">pcntl\_get\_last\_error</span>

pcntl\_exec
===========

在当前进程空间执行指定程序

### 说明

<span class="type">void</span> <span
class="methodname">pcntl\_exec</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">array</span> `$args`</span> \[,
<span class="methodparam"><span class="type">array</span> `$envs`</span>
\]\] )

以给定参数执行程序。

### 参数

`path`  
`path`必须时可执行二进制文件路径或一个在文件第一行指定了
一个可执行文件路径标头的脚本（比如文件第一行是\#!/usr/local/bin/perl的perl脚本）。
更多的信息请查看您系统的execve（2）手册。

`args`  
`args`是一个要传递给程序的参数的字符串数组。

`envs`  
`envs`是一个要传递给程序作为环境变量的字符串数组。这个数组是 key =\>
value格式的，key代表要传递的环境变量的名称，value代表该环境变量值。

### 返回值

当发生错误时返回 **`FALSE`** ，没有错误时没有返回。

pcntl\_fork
===========

在当前进程当前位置产生分支（子进程）。译注：fork是创建了一个子进程，父进程和子进程
都从fork的位置开始向下继续执行，不同的是父进程执行过程中，得到的fork返回值为子进程
号，而子进程得到的是0。

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_fork</span> ( <span
class="methodparam">void</span> )

<span
class="function">pcntl\_fork</span>函数创建一个子进程，这个子进程仅PID（进程号）
和PPID（父进程号）与其父进程不同。fork怎样在您的系统工作的详细信息请查阅您的系统
的fork（2）手册。

### 返回值

成功时，在父进程执行线程内返回产生的子进程的PID，在子进程执行线程内返回0。失败时，在
父进程上下文返回-1，不会创建子进程，并且会引发一个PHP错误。

### 范例

**示例 \#1 <span class="function">pcntl\_fork</span> 示例**

``` php
<?php

$pid = pcntl_fork();
//父进程和子进程都会执行下面代码
if ($pid == -1) {
    //错误处理：创建子进程失败时返回-1.
     die('could not fork');
} else if ($pid) {
     //父进程会得到子进程号，所以这里是父进程执行的逻辑
     pcntl_wait($status); //等待子进程中断，防止子进程成为僵尸进程。
} else {
     //子进程得到的$pid为0, 所以这里是子进程执行的逻辑。
}

?>
```

### 参见

-   <span class="function">pcntl\_waitpid</span>
-   <span class="function">pcntl\_signal</span>

pcntl\_get\_last\_error
=======================

Retrieve the error number set by the last pcntl function which failed

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_get\_last\_error</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns error code.

### 参见

-   <span class="function">pcntl\_strerror</span>

pcntl\_getpriority
==================

获取任意进程的优先级

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_getpriority</span> (\[ <span
class="methodparam"><span class="type">int</span> `$pid`<span
class="initializer"> = getmypid()</span></span> \[, <span
class="methodparam"><span class="type">int</span>
`$process_identifier`<span class="initializer"> =
PRIO\_PROCESS</span></span> \]\] )

<span class="function">pcntl\_getpriority</span> 获取进程号为
`pid`的进程的优先级。由于不同的系统类型以及内核版本下
优先级可能不同，因此请参考您系统的getpriority（2）手册以获取详细的规范。

### 参数

`pid`  
如果没有指定，默认是当前进程的进程号。

`process_identifier`  
**`PRIO_PGRP`**（译注：获取进程组优先级）, **`PRIO_USER`**
（译注：获取用户进程优先级）或
**`PRIO_PROCESS（译注：默认值;获取进程优先级）`**三者之一。

### 返回值

<span class="function">pcntl\_getpriority</span>
返回进程的优先级或在错误时返回 **`FALSE`** 。 值越小代表优先级越高。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 参见

-   <span class="function">pcntl\_setpriority</span>

pcntl\_setpriority
==================

修改任意进程的优先级

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_setpriority</span> ( <span
class="methodparam"><span class="type">int</span> `$priority`</span> \[,
<span class="methodparam"><span class="type">int</span> `$pid`<span
class="initializer"> = getmypid()</span></span> \[, <span
class="methodparam"><span class="type">int</span>
`$process_identifier`<span class="initializer"> =
PRIO\_PROCESS</span></span> \]\] )

<span class="function">pcntl\_setpriority</span> 设置进程号为
`pid`的进程的优先级。

### 参数

`priority`  
`priority` 通常时-20至20这个范围内的值。默认优先级是0,值越小代表
优先级越高。由于不同的系统类型以及内核版本下优先级可能不同，因此请参考您系统的setpriority（2）
手册以获取详细的规范。

`pid`  
如果没有指定，默认是当前进程的进程号。

`process_identifier`  
**`PRIO_PGRP`**（译注：获取进程组优先级）, **`PRIO_USER`**
（译注：获取用户进程优先级）或
**`PRIO_PROCESS（译注：默认值;获取进程优先级）`**三者之一。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">pcntl\_getpriority</span>

pcntl\_signal\_dispatch
=======================

调用等待信号的处理器

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_signal\_dispatch</span> ( <span
class="methodparam">void</span> )

函数<span
class="function">pcntl\_signal\_dispatch</span>调用每个等待信号通过<span
class="function">pcntl\_signal</span> 安装的处理器。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pcntl\_signal\_dispatch</span> 示例**

``` php
<?php
echo "安装信号处理器...\n";
pcntl_signal(SIGHUP,  function($signo) {
     echo "信号处理器被调用\n";
});

echo "为自己生成SIGHUP信号...\n";
posix_kill(posix_getpid(), SIGHUP);

echo "分发...\n";
pcntl_signal_dispatch();

echo "完成\n";

?>
```

以上例程的输出类似于：

    安装信号处理器...
    为自己生成SIGHUP信号...
    分发...
    信号处理器被调用
    完成

### 参见

-   <span class="function">pcntl\_signal</span>
-   <span class="function">pcntl\_sigprocmask</span>
-   <span class="function">pcntl\_sigwaitinfo</span>
-   <span class="function">pcntl\_sigtimedwait</span>

pcntl\_signal\_get\_handler
===========================

Get the current handler for specified signal

### 说明

<span class="type">mixed</span> <span
class="methodname">pcntl\_signal\_get\_handler</span> ( <span
class="methodparam"><span class="type">int</span> `$signo`</span> )

The <span class="function">pcntl\_signal\_get\_handler</span> function
will get the current handler for the specified `signo`.

### 参数

`signo`  
The signal number.

### 返回值

This function may return an integer value that refers to **`SIG_DFL`**
or **`SIG_IGN`**. If you set a custom handler a string value containing
the function name is returned.

### 更新日志

| 版本  | 说明                                                                      |
|-------|---------------------------------------------------------------------------|
| 7.1.0 | <span class="function">pcntl\_signal\_get\_handler</span> has been added. |

### 范例

**示例 \#1 <span class="function">pcntl\_signal\_get\_handler</span>
example**

``` php
<?php
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Outputs: int(0)

function pcntl_test($signo) {}
pcntl_signal(SIGUSR1, 'pcntl_test');
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Outputs: string(10) "pcntl_test"

pcntl_signal(SIGUSR1, SIG_DFL);
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Outputs: int(0)

pcntl_signal(SIGUSR1, SIG_IGN);
var_dump(pcntl_signal_get_handler(SIGUSR1)); // Outputs: int(1)
?>
```

### 参见

-   <span class="function">pcntl\_signal</span>

pcntl\_signal
=============

安装一个信号处理器

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_signal</span> ( <span
class="methodparam"><span class="type">int</span> `$signo`</span> ,
<span class="methodparam"><span class="type">callback</span>
`$handler`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$restart_syscalls`<span class="initializer"> =
true</span></span> \] )

函数<span
class="function">pcntl\_signal</span>为`signo`指定的信号安装一个新
的信号处理器。

### 参数

`signo`  
信号编号。

`handler`  
信号处理器可以是用户创建的函数或方法的名字，也可以是系统常量
**`SIG_IGN`**（译注：忽略信号处理程序）或**`SIG_DFL（默认信号处理程序）`**.

> **Note**:
>
> 注意当你使用一个对象方法的时候，该对象的引用计数回增加使得它在你改变为其他处理或脚本结束之前是持久存在的。

`restart_syscalls`  
指定当信号到达时系统调用重启是否可用。（译注：经查资料，此参数意为系统调用被信号打断时，系统调用是否从
开始处重新开始，但根据http://bugs.php.net/bug.php?id=52121，此参数存在bug无效。）

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.3.0 | 增加参数`restart_syscalls`。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 4.3.0 | 对象方法可以作为回调被使用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 4.3.0 | PCNTL现在使用了ticks作为信号处理的回调机制，ticks在速度上远远超过了之前的处理机制。 这个变化与“用户ticks”遵循了相同的语义。您可以使用<span class="function">declare</span> 语句在程序中指定允许发生回调的位置。这使得我们对异步事件处理的开销最小化。在编译PHP时 启用pcntl将始终承担这种开销，不论您的脚本中是否真正使用了pcntl。 PHP 4.3.0使用ticks作为信号处理回调机制，这比以前的机制快了很多。这个变化与 "<a href="/control-structures/declare.html#control-structures.declare.ticks" class="link">用户ticks</a>" 遵循了相同的语义。您可以使用<a href="/control-structures/declare.html" class="link">declare()</a> 语句在程序中指定允许发生回调的位置。 |

### 范例

**示例 \#1 <span class="function">pcntl\_signal</span>示例**

``` php
<?php
//使用ticks需要PHP 4.3.0以上版本
declare(ticks = 1);

//信号处理函数
function sig_handler($signo)
{

     switch ($signo) {
         case SIGTERM:
             // 处理SIGTERM信号
             exit;
             break;
         case SIGHUP:
             //处理SIGHUP信号
             break;
         case SIGUSR1:
             echo "Caught SIGUSR1...\n";
             break;
         default:
             // 处理所有其他信号
     }

}

echo "Installing signal handler...\n";

//安装信号处理器
pcntl_signal(SIGTERM, "sig_handler");
pcntl_signal(SIGHUP,  "sig_handler");
pcntl_signal(SIGUSR1, "sig_handler");

// 或者在PHP 4.3.0以上版本可以使用对象方法
// pcntl_signal(SIGUSR1, array($obj, "do_something");

echo "Generating signal SIGTERM to self...\n";

//向当前进程发送SIGUSR1信号
posix_kill(posix_getpid(), SIGUSR1);

echo "Done\n"

?>
```

### 参见

-   <span class="function">pcntl\_fork</span>
-   <span class="function">pcntl\_waitpid</span>

pcntl\_sigprocmask
==================

设置或检索阻塞信号

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_sigprocmask</span> ( <span
class="methodparam"><span class="type">int</span> `$how`</span> , <span
class="methodparam"><span class="type">array</span> `$set`</span> \[,
<span class="methodparam"><span class="type">array</span>
`&$oldset`</span> \] )

函数<span
class="function">pcntl\_sigprocmask</span>用来增加，删除或设置阻塞信号，具体行为
依赖于参数`how`。

### 参数

`how`  
设置<span class="function">pcntl\_sigprocmask</span>函数的行为。 可选值:

-   **`SIG_BLOCK`**: 把信号加入到当前阻塞信号中。
-   **`SIG_UNBLOCK`**: 从当前阻塞信号中移出信号。
-   **`SIG_SETMASK`**: 用给定的信号列表替换当前阻塞信号列表。

`set`  
信号列表。

`oldset`  
`oldset`是一个输出参数，用来返回之前的阻塞信号列表数组。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">pcntl\_sigprocmask</span> 示例**

``` php
<?php
//将SIGHUP信号加入到阻塞信号中
pcntl_sigprocmask(SIG_BLOCK, array(SIGHUP));
$oldset = array();
//将SIGHUP从阻塞信号列表中移除并返回之前的阻塞信号列表。
pcntl_sigprocmask(SIG_UNBLOCK, array(SIGHUP), $oldset);
?>
```

### 参见

-   <span class="function">pcntl\_sigwaitinfo</span>
-   <span class="function">pcntl\_sigtimedwait</span>

pcntl\_sigtimedwait
===================

带超时机制的信号等待

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_sigtimedwait</span> ( <span
class="methodparam"><span class="type">array</span> `$set`</span> \[,
<span class="methodparam"><span class="type">array</span>
`&$siginfo`</span> \[, <span class="methodparam"><span
class="type">int</span> `$seconds`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$nanoseconds`<span class="initializer"> =
0</span></span> \]\]\] )

函数<span class="function">pcntl\_sigtimedwait</span>实际上与<span
class="function">pcntl\_sigwaitinfo</span>
的行为一致，不同在于它多了两个增强参数`seconds`和
`nanoseconds`，这使得脚本等待的事件有了一个时间的上限。

### 参数

`set`  
要等待的信号列表数组。

`siginfo`  
`siginfo`是一个输出参数，用来返回信号的信息。更详细情况参见 <span
class="function">pcntl\_sigwaitinfo</span>。

`seconds`  
超时秒数。

`nanoseconds`  
超时纳秒数。

### 返回值

成功时，函数<span
class="function">pcntl\_sigtimedwait</span>返回信号编号。

### 参见

-   <span class="function">pcntl\_sigprocmask</span>
-   <span class="function">pcntl\_sigwaitinfo</span>

pcntl\_sigwaitinfo
==================

等待信号

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_sigwaitinfo</span> ( <span
class="methodparam"><span class="type">array</span> `$set`</span> \[,
<span class="methodparam"><span class="type">array</span>
`&$siginfo`</span> \] )

<span
class="function">pcntl\_sigwaitinfo</span>函数暂停调用脚本的执行直到接收到`set`
参数中列出的某个信号。只要其中的一个信号已经在等待状态(比如： 通过 <span
class="function">pcntl\_sigprocmask</span>函数阻塞)， 函数<span
class="function">pcntl\_sigwaitinfo</span>就回立刻返回。

### 参数

`set`  
要等待的信号数组。

`siginfo`  
`siginfo`是一个输出参数，用来返回信号的信息。

以下元素会为所有信号设置：

-   signo: 信号编号
-   errno: 错误编号
-   code: 信号代码

下面元素可能会为**`SIGCHLD`**信号设置:

-   status: 退出的值或信号
-   utime: 用户消耗的时间
-   stime: 系统（内核）消耗的时间
-   pid: 发送进程ID
-   uid: 发送进程的实际用户ID

信号**`SIGILL`**, **`SIGFPE`**, **`SIGSEGV`** 和 **`SIGBUS`**
可能会被设置的元素:

-   addr: 发生故障的内存位置

可能会为**`SIGPOLL`** 信号设置的元素：

-   band: Band event
-   fd: 文件描述符

### 返回值

成功时，函数<span
class="function">pcntl\_sigwaitinfo</span>返回一个信号编号。

### 范例

**示例 \#1 <span class="function">pcntl\_sigwaitinfo</span> example**

``` php
<?php
echo "Blocking SIGHUP signal\n";
pcntl_sigprocmask(SIG_BLOCK, array(SIGHUP));

echo "Sending SIGHUP to self\n";
posix_kill(posix_getpid(), SIGHUP);

echo "Waiting for signals\n";
$info = array();
pcntl_sigwaitinfo(array(SIGHUP), $info);
?>
```

### 参见

-   <span class="function">pcntl\_sigprocmask</span>
-   <span class="function">pcntl\_sigtimedwait</span>

pcntl\_strerror
===============

Retrieve the system error message associated with the given errno

### 说明

<span class="type">string</span> <span
class="methodname">pcntl\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errno`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`errno`  

### 返回值

Returns error description on success 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">pcntl\_get\_last\_error</span>

pcntl\_wait
===========

等待或返回fork的子进程状态

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_wait</span> ( <span class="methodparam"><span
class="type">int</span> `&$status`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

wait函数刮起当前进程的执行直到一个子进程退出或接收到一个信号要求中断当前进程或调用一个信号处理函数。
如果一个子进程在调用此函数时已经退出（俗称僵尸进程），此函数立刻返回。子进程使用的所有系统资源将
被释放。关于wait在您系统上工作的详细规范请查看您系统的wait（2）手册。

> **Note**:
>
> 这个函数等同于以*-1*作为参数`pid` 的值并且没有`options`参数来调用<span
> class="function">pcntl\_waitpid</span> 函数。

### 参数

`status`  
<span class="function">pcntl\_wait</span>将会存储状态信息到`status`
参数上，这个通过`status`参数返回的状态信息可以用以下函数 <span
class="function">pcntl\_wifexited</span>, <span
class="function">pcntl\_wifstopped</span>, <span
class="function">pcntl\_wifsignaled</span>, <span
class="function">pcntl\_wexitstatus</span>, <span
class="function">pcntl\_wtermsig</span>以及 <span
class="function">pcntl\_wstopsig</span>获取其具体的值。

`options`  
如果您的操作系统（多数BSD类系统）允许使用wait3，您可以提供可选的`options`
参数。如果这个参数没有提供，wait将会被用作系统调用。如果wait3不可用，提供参数
`options`不会有任何效果。`options`的值可以是0
或者以下两个常量或两个常量“或运算”结果（即两个常量代表意义都有效）。

|             |                                        |
|-------------|----------------------------------------|
| *WNOHANG*   | 如果没有子进程退出立刻返回。           |
| *WUNTRACED* | 子进程已经退出并且其状态未报告时返回。 |

### 返回值

<span
class="function">pcntl\_wait</span>返回退出的子进程进程号，发生错误时返回-1,如果提供了
**`WNOHANG`**作为option（wait3可用的系统）并且没有可用子进程时返回0。

### 参见

-   <span class="function">pcntl\_fork</span>
-   <span class="function">pcntl\_signal</span>
-   <span class="function">pcntl\_wifexited</span>
-   <span class="function">pcntl\_wifstopped</span>
-   <span class="function">pcntl\_wifsignaled</span>
-   <span class="function">pcntl\_wexitstatus</span>
-   <span class="function">pcntl\_wtermsig</span>
-   <span class="function">pcntl\_wstopsig</span>
-   <span class="function">pcntl\_waitpid</span>

pcntl\_waitpid
==============

等待或返回fork的子进程状态

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_waitpid</span> ( <span
class="methodparam"><span class="type">int</span> `$pid`</span> , <span
class="methodparam"><span class="type">int</span> `&$status`</span> \[,
<span class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \] )

挂起当前进程的执行直到参数`pid`指定的进程号的进程退出，
或接收到一个信号要求中断当前进程或调用一个信号处理函数。

如果`pid`指定的子进程在此函数调用时已经退出（俗称僵尸进程），此函数
将立刻返回。关于waitpid更详细的规范请参见您系统的waitpid（2）手册。

### 参数

`pid`  
参数`pid`的值可以是以下之一：

|         |                                                     |
|---------|-----------------------------------------------------|
| *\< -1* | 等待任意进程组ID等于参数`pid`给定值的绝对值的进程。 |
| *-1*    | 等待任意子进程;与pcntl\_wait函数行为一致。          |
| *0*     | 等待任意与调用进程组ID相同的子进程。                |
| *\> 0*  | 等待进程号等于参数`pid`值的子进程。                 |

> **Note**:
>
> 指定*-1*作为`pid`的值等同于<span class="function">pcntl\_wait</span>
> 提供(负的`options`)。

`status`  
<span class="function">pcntl\_waitpid</span>将会存储状态信息到`status`
参数上，这个通过`status`参数返回的状态信息可以用以下函数 <span
class="function">pcntl\_wifexited</span>, <span
class="function">pcntl\_wifstopped</span>, <span
class="function">pcntl\_wifsignaled</span>, <span
class="function">pcntl\_wexitstatus</span>, <span
class="function">pcntl\_wtermsig</span>以及 <span
class="function">pcntl\_wstopsig</span>获取其具体的值。

`options`  
如果您的操作系统（多数BSD类系统）允许使用wait3，您可以提供可选的`options`
参数。如果这个参数没有提供，wait将会被用作系统调用。如果wait3不可用，提供参数
`options`不会有任何效果。`options`的值可以是0
或者以下两个常量或两个常量“或运算”结果（即两个常量代表意义都有效）。

|             |                                        |
|-------------|----------------------------------------|
| *WNOHANG*   | 如果没有子进程退出立刻返回。           |
| *WUNTRACED* | 子进程已经退出并且其状态未报告时返回。 |

### 返回值

<span
class="function">pcntl\_waitpid</span>返回退出的子进程进程号，发生错误时返回-1,如果提供了
**`WNOHANG`**作为option（wait3可用的系统）并且没有可用子进程时返回0。

### 参见

-   <span class="function">pcntl\_fork</span>
-   <span class="function">pcntl\_signal</span>
-   <span class="function">pcntl\_wifexited</span>
-   <span class="function">pcntl\_wifstopped</span>
-   <span class="function">pcntl\_wifsignaled</span>
-   <span class="function">pcntl\_wexitstatus</span>
-   <span class="function">pcntl\_wtermsig</span>
-   <span class="function">pcntl\_wstopsig</span>

pcntl\_wexitstatus
==================

返回一个中断的子进程的返回代码

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_wexitstatus</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

返回一个中断的子进程的返回代码。这个函数仅在函数<span
class="function">pcntl\_wifexited</span>返回 **`TRUE`**.时有效。

### 参数

`status`  
参数 `status` 是提供给成功调用 <span
class="function">pcntl\_waitpid</span> 时的状态参数。

### 返回值

返回整形的子进程返回代码。

### 参见

-   <span class="function">pcntl\_waitpid</span>
-   <span class="function">pcntl\_wifexited</span>

pcntl\_wifexited
================

检查状态代码是否代表一个正常的退出。

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_wifexited</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

检查子进程状态代码是否代表正常退出。

### 参数

`status`  
参数 `status` 是提供给成功调用 <span
class="function">pcntl\_waitpid</span> 时的状态参数。

### 返回值

当子进程状态代码代表正常退出时返回 **`TRUE`** ，其他情况返回
**`FALSE`**。

### 参见

-   <span class="function">pcntl\_waitpid</span>
-   <span class="function">pcntl\_wexitstatus</span>

pcntl\_wifsignaled
==================

检查子进程状态码是否代表由于某个信号而中断

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_wifsignaled</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

检查子进程是否是由于某个未捕获的信号退出的。

### 参数

`status`  
参数 `status` 是提供给成功调用 <span
class="function">pcntl\_waitpid</span> 时的状态参数。

### 返回值

如果子进程是由于某个未捕获的信号退出的返回 **`TRUE`** ，其他情况返回
**`FALSE`** 。

### 参见

-   <span class="function">pcntl\_waitpid</span>
-   <span class="function">pcntl\_signal</span>

pcntl\_wifstopped
=================

检查子进程当前是否已经停止

### 说明

<span class="type">bool</span> <span
class="methodname">pcntl\_wifstopped</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

仅查子进程当前是否停止; 此函数只有作用于使用了*WUNTRACED*作为
option的<span
class="function">pcntl\_waitpid</span>函数调用产生的status时才有效。

### 参数

`status`  
参数 `status` 是提供给成功调用 <span
class="function">pcntl\_waitpid</span> 时的状态参数。

### 返回值

如果子进程当前是停止的返回 **`TRUE`** ，其他情况返回 **`FALSE`** 。

### 参见

-   <span class="function">pcntl\_waitpid</span>

pcntl\_wstopsig
===============

返回导致子进程停止的信号

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_wstopsig</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

返回导致子进程停止的信号编号。这个函数仅在<span
class="function">pcntl\_wifstopped</span>返回 **`TRUE`** 时有效。

### 参数

`status`  
参数 `status` 是提供给成功调用 <span
class="function">pcntl\_waitpid</span> 时的状态参数。

### 返回值

返回信号编号。

### 参见

-   <span class="function">pcntl\_waitpid</span>
-   <span class="function">pcntl\_wifstopped</span>

pcntl\_wtermsig
===============

返回导致子进程中断的信号

### 说明

<span class="type">int</span> <span
class="methodname">pcntl\_wtermsig</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

返回导致子进程中断的信号编号。这个函数仅在<span
class="function">pcntl\_wifsignaled</span> 返回 **`TRUE`** 时有效。

### 参数

`status`  
参数 `status` 是提供给成功调用 <span
class="function">pcntl\_waitpid</span> 时的状态参数。

### 返回值

返回整型的信号编号。

### 参见

-   <span class="function">pcntl\_waitpid</span>
-   <span class="function">pcntl\_signal</span>
-   <span class="function">pcntl\_wifsignaled</span>

**目录**

-   [pcntl\_alarm](/ref/pcntl.html#pcntl_alarm) —
    为进程设置一个alarm闹钟信号
-   [pcntl\_async\_signals](/ref/pcntl.html#pcntl_async_signals) —
    Enable/disable asynchronous signal handling or return the old
    setting
-   [pcntl\_errno](/ref/pcntl.html#pcntl_errno) — 别名
    pcntl\_get\_last\_error
-   [pcntl\_exec](/ref/pcntl.html#pcntl_exec) —
    在当前进程空间执行指定程序
-   [pcntl\_fork](/ref/pcntl.html#pcntl_fork) —
    在当前进程当前位置产生分支（子进程）。译注：fork是创建了一个子进程，父进程和子进程
    都从fork的位置开始向下继续执行，不同的是父进程执行过程中，得到的fork返回值为子进程
    号，而子进程得到的是0。
-   [pcntl\_get\_last\_error](/ref/pcntl.html#pcntl_get_last_error) —
    Retrieve the error number set by the last pcntl function which
    failed
-   [pcntl\_getpriority](/ref/pcntl.html#pcntl_getpriority) —
    获取任意进程的优先级
-   [pcntl\_setpriority](/ref/pcntl.html#pcntl_setpriority) —
    修改任意进程的优先级
-   [pcntl\_signal\_dispatch](/ref/pcntl.html#pcntl_signal_dispatch) —
    调用等待信号的处理器
-   [pcntl\_signal\_get\_handler](/ref/pcntl.html#pcntl_signal_get_handler)
    — Get the current handler for specified signal
-   [pcntl\_signal](/ref/pcntl.html#pcntl_signal) — 安装一个信号处理器
-   [pcntl\_sigprocmask](/ref/pcntl.html#pcntl_sigprocmask) —
    设置或检索阻塞信号
-   [pcntl\_sigtimedwait](/ref/pcntl.html#pcntl_sigtimedwait) —
    带超时机制的信号等待
-   [pcntl\_sigwaitinfo](/ref/pcntl.html#pcntl_sigwaitinfo) — 等待信号
-   [pcntl\_strerror](/ref/pcntl.html#pcntl_strerror) — Retrieve the
    system error message associated with the given errno
-   [pcntl\_wait](/ref/pcntl.html#pcntl_wait) —
    等待或返回fork的子进程状态
-   [pcntl\_waitpid](/ref/pcntl.html#pcntl_waitpid) —
    等待或返回fork的子进程状态
-   [pcntl\_wexitstatus](/ref/pcntl.html#pcntl_wexitstatus) —
    返回一个中断的子进程的返回代码
-   [pcntl\_wifexited](/ref/pcntl.html#pcntl_wifexited) —
    检查状态代码是否代表一个正常的退出。
-   [pcntl\_wifsignaled](/ref/pcntl.html#pcntl_wifsignaled) —
    检查子进程状态码是否代表由于某个信号而中断
-   [pcntl\_wifstopped](/ref/pcntl.html#pcntl_wifstopped) —
    检查子进程当前是否已经停止
-   [pcntl\_wstopsig](/ref/pcntl.html#pcntl_wstopsig) —
    返回导致子进程停止的信号
-   [pcntl\_wtermsig](/ref/pcntl.html#pcntl_wtermsig) —
    返回导致子进程中断的信号
