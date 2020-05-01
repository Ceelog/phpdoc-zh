pthreads
========

**目录**

-   [简介](/intro/pthreads.html)
-   [安装／配置](/pthreads/setup.html)
    -   [需求](/pthreads/setup.html#需求)
    -   [安装](/pthreads/setup.html#安装)
    -   [运行时配置](/pthreads/setup.html#运行时配置)
-   [预定义常量](/pthreads/constants.html)
-   [Threaded](/class/threaded.html) — Threaded 类
    -   [Threaded::chunk](/class/threaded.html#Threaded::chunk) — 操作
    -   [Threaded::count](/class/threaded.html#Threaded::count) — 操作
    -   [Threaded::extend](/class/threaded.html#Threaded::extend) —
        Runtime Manipulation
    -   [Threaded::from](/class/threaded.html#Threaded::from) — Creation
    -   [Threaded::getTerminationInfo](/class/threaded.html#Threaded::getTerminationInfo)
        — 错误检测
    -   [Threaded::isRunning](/class/threaded.html#Threaded::isRunning)
        — 状态检测
    -   [Threaded::isTerminated](/class/threaded.html#Threaded::isTerminated)
        — 状态检测
    -   [Threaded::isWaiting](/class/threaded.html#Threaded::isWaiting)
        — 状态检测
    -   [Threaded::lock](/class/threaded.html#Threaded::lock) — 同步控制
    -   [Threaded::merge](/class/threaded.html#Threaded::merge) — 操作
    -   [Threaded::notify](/class/threaded.html#Threaded::notify) —
        同步控制
    -   [Threaded::notifyOne](/class/threaded.html#Threaded::notifyOne)
        — Synchronization
    -   [Threaded::pop](/class/threaded.html#Threaded::pop) — 操作
    -   [Threaded::run](/class/threaded.html#Threaded::run) — 执行
    -   [Threaded::shift](/class/threaded.html#Threaded::shift) —
        Manipulation
    -   [Threaded::synchronized](/class/threaded.html#Threaded::synchronized)
        — 同步控制
    -   [Threaded::unlock](/class/threaded.html#Threaded::unlock) —
        同步控制
    -   [Threaded::wait](/class/threaded.html#Threaded::wait) —
        Synchronization
-   [Thread](/class/thread.html) — Thread 类
    -   [Thread::detach](/class/thread.html#Thread::detach) — 执行
    -   [Thread::getCreatorId](/class/thread.html#Thread::getCreatorId)
        — 识别
    -   [Thread::getCurrentThread](/class/thread.html#Thread::getCurrentThread)
        — 识别
    -   [Thread::getCurrentThreadId](/class/thread.html#Thread::getCurrentThreadId)
        — 识别
    -   [Thread::getThreadId](/class/thread.html#Thread::getThreadId) —
        识别
    -   [Thread::globally](/class/thread.html#Thread::globally) — 执行
    -   [Thread::isJoined](/class/thread.html#Thread::isJoined) —
        状态监测
    -   [Thread::isStarted](/class/thread.html#Thread::isStarted) —
        状态检测
    -   [Thread::join](/class/thread.html#Thread::join) — 同步
    -   [Thread::kill](/class/thread.html#Thread::kill) — 执行
    -   [Thread::start](/class/thread.html#Thread::start) — 执行
-   [Worker](/class/worker.html) — Worker 类
    -   [Worker::collect](/class/worker.html#Worker::collect) — Collect
        references to completed tasks
    -   [Worker::getStacked](/class/worker.html#Worker::getStacked) —
        获取剩余的栈大小
    -   [Worker::isShutdown](/class/worker.html#Worker::isShutdown) —
        状态检测
    -   [Worker::isWorking](/class/worker.html#Worker::isWorking) —
        状态检测
    -   [Worker::shutdown](/class/worker.html#Worker::shutdown) — 关闭
        Worker
    -   [Worker::stack](/class/worker.html#Worker::stack) —
        将要执行的任务入栈
    -   [Worker::unstack](/class/worker.html#Worker::unstack) —
        将要执行的任务出栈
-   [Collectable](/class/collectable.html) — The Collectable interface
    -   [Collectable::isGarbage](/class/collectable.html#Collectable::isGarbage)
        — Determine whether an object has been marked as garbage
    -   [Collectable::setGarbage](/class/collectable.html#Collectable::setGarbage)
        — Mark an object as garbage
-   [Modifiers](/pthreads/modifiers.html) — 方法修饰符
-   [Pool](/class/pool.html) — Pool 类
    -   [Pool::collect](/class/pool.html#Pool::collect) —
        回收已完成任务的引用
    -   [Pool::\_\_construct](/class/pool.html#Pool::__construct) —
        创建新的 Worker 对象池
    -   [Pool::resize](/class/pool.html#Pool::resize) — 改变 Pool
        对象的可容纳 Worker 对象的数量
    -   [Pool::shutdown](/class/pool.html#Pool::shutdown) — 停止所有的
        Worker 对象
    -   [Pool::submit](/class/pool.html#Pool::submit) — 提交对象以执行
    -   [Pool::submitTo](/class/pool.html#Pool::submitTo) —
        提交一个任务到特定的 Worker 以执行
-   [Mutex](/class/mutex.html) — Mutex 类
    -   [Mutex::create](/class/mutex.html#Mutex::create) —
        创建一个互斥量
    -   [Mutex::destroy](/class/mutex.html#Mutex::destroy) — 销毁互斥量
    -   [Mutex::lock](/class/mutex.html#Mutex::lock) — 给互斥量加锁
    -   [Mutex::trylock](/class/mutex.html#Mutex::trylock) —
        尝试给互斥量加锁
    -   [Mutex::unlock](/class/mutex.html#Mutex::unlock) —
        释放互斥量上的锁
-   [Cond](/class/cond.html) — Cond 类
    -   [Cond::broadcast](/class/cond.html#Cond::broadcast) —
        广播条件变量
    -   [Cond::create](/class/cond.html#Cond::create) — 创建一个条件变量
    -   [Cond::destroy](/class/cond.html#Cond::destroy) — 销毁条件变量
    -   [Cond::signal](/class/cond.html#Cond::signal) — 发送唤醒信号
    -   [Cond::wait](/class/cond.html#Cond::wait) — 等待
-   [Volatile](/class/volatile.html) — The Volatile class

简介
----

Threaded 对象提供支持 pthreads
操作的基本功能，包括同步方法以及其他对程序员很有帮助的接口。

重要的是，Threaded
提供了隐式的线程安全机制，这个对象中的所有操作都是线程安全的。

类摘要
------

**Threaded**

<span class="ooclass"> class **Threaded** </span> <span
class="oointerface">implements <span
class="interfacename">Collectable</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> <span class="oointerface">, <span
class="interfacename">Countable</span> </span> <span
class="oointerface">, <span class="interfacename">ArrayAccess</span>
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">chunk</span> ( <span class="methodparam"><span
class="type">int</span> `$size`</span> , <span class="methodparam"><span
class="type">bool</span> `$preserve`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">extend</span> ( <span class="methodparam"><span
class="type">string</span> `$class`</span> )

<span class="modifier">public</span> <span class="type">Threaded</span>
<span class="methodname">from</span> ( <span class="methodparam"><span
class="type">Closure</span> `$run`</span> \[, <span
class="methodparam"><span class="type">Closure</span>
`$construct`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getTerminationInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isRunning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isTerminated</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isWaiting</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$from`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$overwrite`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">notify</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">notifyOne</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">run</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">shift</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">synchronized</span> ( <span
class="methodparam"><span class="type">Closure</span> `$block`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">wait</span> (\[ <span class="methodparam"><span
class="type">int</span> `$timeout`</span> \] )

}

Threaded::chunk
===============

操作

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Threaded::chunk</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> , <span
class="methodparam"><span class="type">bool</span> `$preserve`</span> )

获取给定数量的对象属性表，可以选择是否保留键名称。

### 参数

`size`  
要获取的条目数量

`preserve`  
保留成员原有的键名称，默认为 false

### 返回值

数组对象，包含从对象属性表中返回的给定数量的条目。

### 范例

**示例 \#1 获取对象属性表中的部分条目**

``` php
<?php
$safe = new Threaded();

while (count($safe) < 10) {
    $safe[] = count($safe);
}

var_dump($safe->chunk(5));
?>
```

以上例程会输出：

    array(5) {
      [0]=>
      int(0)
      [1]=>
      int(1)
      [2]=>
      int(2)
      [3]=>
      int(3)
      [4]=>
      int(4)
    }

Threaded::count
===============

操作

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Threaded::count</span> ( <span
class="methodparam">void</span> )

返回对象的属性数量

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 计算对象中的属性数量**

``` php
<?php
$safe = new Threaded();

while (count($safe) < 10) {
    $safe[] = count($safe);
}

var_dump(count($safe));
?>
```

以上例程会输出：

    int(10)

Threaded::extend
================

Runtime Manipulation

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::extend</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> )

Makes thread safe standard class at runtime

### 参数

`class`  
The class to extend

### 返回值

A boolean indication of success

### 范例

**示例 \#1 Runtime inheritance**

``` php
<?php
class My {}

Threaded::extend(My::class);

$my = new My();

var_dump($my instanceof Threaded);
?>
```

以上例程会输出：

    bool(true)

Threaded::from
==============

Creation

**Warning**

This method has been removed in pthreads v3. With the introduction of
<a href="/language/oop5/anonymous.html" class="link">anonymous classes</a>
in PHP 7, these can now be used instead.

### 说明

<span class="modifier">public</span> <span class="type">Threaded</span>
<span class="methodname">Threaded::from</span> ( <span
class="methodparam"><span class="type">Closure</span> `$run`</span> \[,
<span class="methodparam"><span class="type">Closure</span>
`$construct`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \]\] )

Creates an anonymous Threaded object from closures

### 参数

`run`  
The closure to use for ::run

`construct`  
The constructor to use for anonymous object

`args`  
The arguments to pass to constructor

### 返回值

A new anonymous Threaded object

### 范例

**示例 \#1 Thread safe objects from closures**

``` php
<?php
$pool = new Pool(4);
$pool->submit(Collectable::from(function(){
    echo "Hello World";
    $this->setGarbage();
}));
/* ... */
$pool->shutdown();
?>
```

以上例程会输出：

    Hello World

Threaded::getTerminationInfo
============================

错误检测

**Warning**

pthreads v3 中已移除此方法。 另外， <span
class="methodname">Threaded::run</span> 中的代码， 应该使用 try...catch
来进行异常检测（因为在 PHP 7 中大部分 error 都改为抛出异常的方式了）。

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Threaded::getTerminationInfo</span> ( <span
class="methodparam">void</span> )

返回对象的终端错误信息

### 参数

此函数没有参数。

### 返回值

包含终端信息的数组对象

### 范例

**示例 \#1 检测线程运行时的致命错误**

``` php
<?php
class My extends Thread {
    public function run() {
        @not_found();
    }
}

$my = new My();
$my->start();
$my->join();

var_dump($my->isTerminated(), $my->getTerminationInfo());
?>
```

以上例程会输出：

    bool(true)
    array(4) {
      ["scope"]=>
      string(2) "My"
      ["function"]=>
      string(3) "run"
      ["file"]=>
      string(29) "/usr/src/pthreads/sandbox.php"
      ["line"]=>
      int(4)
    }

Threaded::isRunning
===================

状态检测

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isRunning</span> ( <span
class="methodparam">void</span> )

对象是否正在运行

### 参数

此函数没有参数。

### 返回值

表示运行状态的布尔值

> **Note**:
>
> 如果对象的 run 方法正在执行，则视该对象为处于运行状态

### 范例

**示例 \#1 检测对象状态**

``` php
<?php
class My extends Thread {
    public function run() {
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
var_dump($my->isRunning());
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
?>
```

以上例程会输出：

    bool(true)

Threaded::isTerminated
======================

状态检测

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isTerminated</span> ( <span
class="methodparam">void</span> )

检测是否因致命错误或未捕获的异常而导致执行过程异常终止

### 参数

此函数没有参数。

### 返回值

布尔值，表示是否异常终止

### 范例

**示例 \#1 检测对象状态**

``` php
<?php
class My extends Thread {
    public function run() {
        i_do_not_exist();
    }
}
$my = new My();
$my->start();
$my->join();
var_dump($my->isTerminated());
?>
```

以上例程会输出：

    bool(true)

Threaded::isWaiting
===================

状态检测

**Warning**

pthreads v3 中已移除此方法。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isWaiting</span> ( <span
class="methodparam">void</span> )

检测对象是否在等待其他线程唤醒

### 参数

此函数没有参数。

### 返回值

布尔值，表示是否处于等待唤醒状态

### 范例

**示例 \#1 检测对象状态**

``` php
<?php
class My extends Thread {
    public function run() {
        $this->synchronized(function($thread){
            if (!$this->done)
                $thread->wait();
        }, $this);
    }
    
    protected $done;
}
$my = new My();
$my->start();
$my->synchronized(function($thread){
    var_dump(
        $thread->isWaiting());
    $thread->done = true;
    $thread->notify();
}, $my);
?>
```

以上例程会输出：

    bool(true)

Threaded::lock
==============

同步控制

**Warning**

pthreads v3 中已移除此方法。 请使用 <span
class="methodname">Threaded::synchronized</span> 方法。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::lock</span> ( <span
class="methodparam">void</span> )

给对象属性表加锁

### 参数

此函数没有参数。

### 返回值

布尔值，表示加锁是否成功

### 范例

**示例 \#1 给对象属性加锁**

``` php
<?php
class My extends Thread {
    public function run() {
        var_dump($this->lock());
        /** 其他线程无法进行读/写操作 **/
        var_dump($this->unlock());
        /** 其他线程可以进行读/写操作 */
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    bool(true)
    bool(true)

Threaded::merge
===============

操作

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$overwrite`</span> \] )

将数据合并到当前对象

### 参数

`from`  
要合并的数据

`overwrite`  
如果现有对象已经存在同键的数据，是否覆盖。默认为 true

### 返回值

布尔值，表示操作是否成功

### 范例

**示例 \#1 合并数据到对象的属性表**

``` php
<?php
$array = [];

while (count($array) < 10)
    $array[] = count($array);

$stdClass = new stdClass();
$stdClass->foo = "foo";
$stdClass->bar = "bar";
$stdClass->baz = "baz";

$safe = new Threaded();
$safe->merge($array);
$safe->merge($stdClass);

var_dump($safe);
?>
```

以上例程会输出：

    object(Threaded)#2 (13) {
      ["0"]=>
      int(0)
      ["1"]=>
      int(1)
      ["2"]=>
      int(2)
      ["3"]=>
      int(3)
      ["4"]=>
      int(4)
      ["5"]=>
      int(5)
      ["6"]=>
      int(6)
      ["7"]=>
      int(7)
      ["8"]=>
      int(8)
      ["9"]=>
      int(9)
      ["foo"]=>
      string(3) "foo"
      ["bar"]=>
      string(3) "bar"
      ["baz"]=>
      string(3) "baz"
    }

Threaded::notify
================

同步控制

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::notify</span> ( <span
class="methodparam">void</span> )

向对象发送唤醒通知

### 参数

此函数没有参数。

### 返回值

布尔值，表示操作是否成功

### 范例

**示例 \#1 等待和唤醒**

``` php
<?php
class My extends Thread {
    public function run() {
        /** 让线程等待 **/
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
/** 向处于等待状态的线程发送唤醒通知 **/
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
var_dump($my->join());
?>
```

以上例程会输出：

    bool(true)

Threaded::notifyOne
===================

Synchronization

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::notifyOne</span> ( <span
class="methodparam">void</span> )

Send notification to the referenced object. This unblocks at least one
of the blocked threads (as opposed to unblocking all of them, as seen
with <span class="methodname">Threaded::notify</span>).

### 参数

此函数没有参数。

### 返回值

A boolean indication of success

### 范例

**示例 \#1 Notifications and Waiting**

``` php
<?php
class My extends Thread {
    public function run() {
        /** cause this thread to wait **/
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
/** send notification to the waiting thread **/
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notifyOne();
}, $my);
var_dump($my->join());
?>
```

以上例程会输出：

    bool(true)

Threaded::pop
=============

操作

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::pop</span> ( <span
class="methodparam">void</span> )

弹出对象属性表中的最后一项数据

### 返回值

对象属性表中最后一项数据

### 范例

**示例 \#1 弹出对象属性表中的最后一项数据**

``` php
<?php
$safe = new Threaded();

while (count($safe) < 10)
    $safe[] = count($safe);

var_dump($safe->pop());
?>
```

以上例程会输出：

    int(9)

Threaded::run
=============

执行

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Threaded::run</span> ( <span
class="methodparam">void</span> )

如果需要在多线程环境下执行代码，必须实现本方法

### 参数

此函数没有参数。

### 返回值

无返回值。即使代码中 run 方法有返回值，也会被忽略

Threaded::shift
===============

Manipulation

### 说明

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">Threaded::shift</span> ( <span
class="methodparam">void</span> )

弹出对象属性表中第一项数据

### 返回值

对象属性表中的第一项数据

### 范例

**示例 \#1 弹出对象属性表中第一项数据**

``` php
<?php
$safe = new Threaded();

while (count($safe) < 10)
    $safe[] = count($safe);

var_dump($safe->shift());
?>
```

以上例程会输出：

    int(0)

Threaded::synchronized
======================

同步控制

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Threaded::synchronized</span> ( <span
class="methodparam"><span class="type">Closure</span> `$block`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

在发起调用的线程上下文中获取对象同步锁，然后同步执行代码块

### 参数

`block`  
要执行的代码块

`...`  
传送给代码块的不定长参数

### 返回值

代码块的返回值

### 范例

**示例 \#1 同步**

``` php
<?php
class My extends Thread {
    public function run() {
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
var_dump($my->join());
?>
```

以上例程会输出：

    bool(true)

Threaded::unlock
================

同步控制

**Warning**

pthreads v3 中已移除此方法。 请使用 <span
class="methodname">Threaded::synchronized</span> 方法。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::unlock</span> ( <span
class="methodparam">void</span> )

从调用上下文中解锁被引用的对象

### 参数

此函数没有参数。

### 返回值

布尔值，表示操作是否成功

### 范例

**示例 \#1 给对象属性表加锁**

``` php
<?php
class My extends Thread {
    public function run() {
        var_dump($this->lock());
        /** 其他线程无法执行读/写操作 **/
        var_dump($this->unlock());
        /** 其他线程可以执行读/写操作 */
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    bool(true)
    bool(true)

Threaded::wait
==============

Synchronization

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::wait</span> (\[ <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \] )

让发起调用的线程上下文进入等待状态，直到收到其他线程的唤醒通知

### 参数

`timeout`  
可选参数，等待时间，以微秒计

### 返回值

布尔值，表示操作是否成功

### 范例

**示例 \#1 等待和唤醒**

``` php
<?php
class My extends Thread {
    public function run() {
        /** 让本线程进入等待状态 **/
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
/** 向处于等待状态的线程发送唤醒通知 **/
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
var_dump($my->join());
?>
```

以上例程会输出：

    bool(true)

简介
----

当调用 Thread 对象的 start 方法时，该对象的 run
方法中的代码将在独立线程中并行执行。

run
方法中的代码执行完毕之后，独立线程立即退出，并且等待合适的时机由创建者线程加入（join）。

**Warning**

依赖于引擎本身的机制检测何时加入线程可能引发非预期的行为，程序员应该尽可能的显式控制线程加入的时机。

类摘要
------

**Thread**

<span class="ooclass"> class **Thread** </span> <span class="ooclass">
<span class="modifier">extends</span> **Threaded** </span> <span
class="oointerface">implements <span
class="interfacename">Countable</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> <span class="oointerface">, <span
class="interfacename">ArrayAccess</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">detach</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getCreatorId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Thread</span> <span
class="methodname">getCurrentThread</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getCurrentThreadId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getThreadId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">globally</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isJoined</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isStarted</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">join</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">kill</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">start</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`</span> \] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Threaded::chunk</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> , <span
class="methodparam"><span class="type">bool</span> `$preserve`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Threaded::count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::extend</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> )

<span class="modifier">public</span> <span class="type">Threaded</span>
<span class="methodname">Threaded::from</span> ( <span
class="methodparam"><span class="type">Closure</span> `$run`</span> \[,
<span class="methodparam"><span class="type">Closure</span>
`$construct`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Threaded::getTerminationInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isRunning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isTerminated</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isWaiting</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$overwrite`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::notify</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::notifyOne</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Threaded::run</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">Threaded::shift</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Threaded::synchronized</span> ( <span
class="methodparam"><span class="type">Closure</span> `$block`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::unlock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::wait</span> (\[ <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \] )

}

Thread::detach
==============

执行

**Warning**

pthreads v3 中已经移除此方法.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Thread::detach</span> ( <span
class="methodparam">void</span> )

从调用上下文中将引用线程分离出来，非常危险！

**Warning**

本方法会引发未定义的、不安全的行为。
通常情况下不会用到本方法，提供这个方法主要是出于完备性以及高级用法的考虑。

### 参数

此函数没有参数。

### 返回值

Thread::getCreatorId
====================

识别

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Thread::getCreatorId</span> ( <span
class="methodparam">void</span> )

返回创建当前线程的线程ID。

### 参数

此函数没有参数。

### 返回值

线程ID，数字格式

### 范例

**示例 \#1 返回创建线程的线程或进程ID**

``` php
<?php
class My extends Thread {
    public function run() {
        printf("%s created by Thread #%lu\n", __CLASS__, $this->getCreatorId());
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    My created by Thread #123456778899

Thread::getCurrentThread
========================

识别

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Thread</span> <span
class="methodname">Thread::getCurrentThread</span> ( <span
class="methodparam">void</span> )

获取当前执行线程的引用。

### 参数

此函数没有参数。

### 返回值

表示当前执行线程的对象。

### 范例

**示例 \#1 获取当前执行线程**

``` php
<?php
class My extends Thread {
    public function run() {
        var_dump(Thread::getCurrentThread());
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    object(My)#2 (0) {
    }

Thread::getCurrentThreadId
==========================

识别

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Thread::getCurrentThreadId</span> ( <span
class="methodparam">void</span> )

返回当前执行线程的ID

### 参数

此函数没有参数。

### 返回值

线程ID，数字格式

### 范例

**示例 \#1 返回当前执行线程的ID**

``` php
<?php
class My extends Thread {
    public function run() {
        printf("%s is Thread #%lu\n", __CLASS__, Thread::getCurrentThreadId());
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    My is Thread #123456778899

Thread::getThreadId
===================

识别

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Thread::getThreadId</span> ( <span
class="methodparam">void</span> )

返回引用线程的ID

### 参数

此函数没有参数。

### 返回值

线程ID，数字格式

### 范例

**示例 \#1 返回引用线程的ID**

``` php
<?php
class My extends Thread {
    public function run() {
        printf("%s is Thread #%lu\n", __CLASS__, $this->getThreadId());
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    My is Thread #123456778899

Thread::globally
================

执行

**Warning**

pthreads v3 中已移除此方法。

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">Thread::globally</span> ( <span
class="methodparam">void</span> )

在全局范围中执行代码块

### 参数

此函数没有参数。

### 返回值

被调用代码块的返回值

### 范例

**示例 \#1 在全局范围执行代码块**

``` php
<?php
class My extends Thread {
    public function run() {
        global $std;
        
        Thread::globally(function(){
            $std = new stdClass;
        });
        
        var_dump($std);
    }
}
$my = new My();
$my->start();
?>
```

以上例程会输出：

    object(stdClass)#3 (0) {
    }

Thread::isJoined
================

状态监测

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::isJoined</span> ( <span
class="methodparam">void</span> )

线程是否已经被加入（join）

### 参数

此函数没有参数。

### 返回值

布尔值，表示是否被加入

### 范例

**示例 \#1 检测线程状态**

``` php
<?php
class My extends Thread {
    public function run() {
        $this->synchronized(function($thread){
            if (!$thread->done)
                $thread->wait();
        }, $this);
    }
}
$my = new My();
$my->start();
var_dump($my->isJoined());
$my->synchronized(function($thread){
    $thread->done = true;
    $thread->notify();
}, $my);
?>
```

以上例程会输出：

    bool(false)

Thread::isStarted
=================

状态检测

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::isStarted</span> ( <span
class="methodparam">void</span> )

线程是否开始执行

### 参数

此函数没有参数。

### 返回值

布尔值，表示线程是否开始执行

### 范例

**示例 \#1 监测线程是否开始执行**

``` php
<?php
$worker = new Worker();
$worker->start();
var_dump($worker->isStarted());
?>
```

以上例程会输出：

    bool(true)

Thread::join
============

同步

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::join</span> ( <span
class="methodparam">void</span> )

让当前执行上下文等待被引用线程执行完毕

### 参数

此函数没有参数。

### 返回值

布尔值，表示操作成功与否

### 范例

**示例 \#1 加入线程**

``` php
<?php
class My extends Thread {
    public function run() {
        /* ... */
    }
}
$my = new My();
$my->start();
/* ... */
var_dump($my->join());
/* ... */
?>
```

以上例程会输出：

    bool(true)

Thread::kill
============

执行

**Warning**

pthreads v3 中已移除此方法。

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Thread::kill</span> ( <span
class="methodparam">void</span> )

强制线程中止

**Warning**

通常情况下，程序员不应该强制杀除线程

### 参数

此函数没有参数。

### 返回值

布尔值，表示操作成功与否

### 范例

**示例 \#1 杀除线程**

``` php
<?php
class T extends Thread {
    public function run() {
        $stdin = fopen("php://stdin", "r");
        while(($line = fgets($stdin))) {
            echo $line;
        }
    }
}

$t = new T();
$t->start();

var_dump($t->kill());
?>
```

以上例程会输出：

    bool(true)

Thread::start
=============

执行

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::start</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`</span> \] )

在独立线程中执行 run 方法

### 参数

`options`  
可选参数，用来控制线程继承。默认值为 PTHREADS\_INHERIT\_ALL

### 返回值

布尔值，表示操作成功与否

### 范例

**示例 \#1 开始线程**

``` php
<?php
class My extends Thread {
    public function run() {
        /** ... **/
    }
}
$my = new My();
var_dump($my->start());
?>
```

以上例程会输出：

    bool(true)

简介
----

Worker 是一个具有持久化上下文的线程对象，通常用来在多个线程中使用。

当一个 Worker 对象开始之后，会执行它的 run 方法，但是即使 run
方法执行完毕，线程本身也不会消亡，除非遇到以下情况：

-   Worker 对象超出作用范围（没有指向它的引用了）

-   代码调用了 Worker 对象的 shutdown 方法

-   整个脚本终止了

这意味着程序员可以在程序执行过程中重用这个线程上下文： 在 Worker
对象的栈中添加对象会激活 Worker 对象执行被加入对象的 run 方法。

类摘要
------

**Worker**

<span class="ooclass"> class **Worker** </span> <span class="ooclass">
<span class="modifier">extends</span> **Thread** </span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> <span class="oointerface">, <span
class="interfacename">ArrayAccess</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">collect</span> (\[ <span class="methodparam"><span
class="type">Callable</span> `$collector`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getStacked</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isShutdown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isWorking</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">shutdown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">stack</span> ( <span class="methodparam"><span
class="type">Threaded</span> `&$work`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">unstack</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Thread::detach</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Thread::getCreatorId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Thread</span> <span
class="methodname">Thread::getCurrentThread</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Thread::getCurrentThreadId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Thread::getThreadId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">Thread::globally</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::isJoined</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::isStarted</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::join</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Thread::kill</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Thread::start</span> (\[ <span
class="methodparam"><span class="type">int</span> `$options`</span> \] )

}

Worker::collect
===============

Collect references to completed tasks

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Worker::collect</span> (\[ <span
class="methodparam"><span class="type">Callable</span>
`$collector`</span> \] )

Allows the worker to collect references determined to be garbage by the
optionally given collector.

### 参数

`collector`  
A Callable collector that returns a boolean on whether the task can be
collected or not. Only in rare cases should a custom collector need to
be used.

### 返回值

The number of remaining tasks on the worker's stack to be collected.

### 范例

**示例 \#1 A basic example of <span
class="methodname">Worker::collect</span>**

``` php
<?php
$worker = new Worker();

echo "There are currently {$worker->collect()} tasks on the stack to be collected\n";

for ($i = 0; $i < 15; ++$i) {
    $worker->stack(new class extends Threaded {});
}

echo "There are {$worker->collect()} tasks remaining on the stack to be collected\n";

$worker->start();

while ($worker->collect()); // blocks until all tasks have finished executing

echo "There are now {$worker->collect()} tasks on the stack to be collected\n";

$worker->shutdown();
```

以上例程会输出：

    There are currently 0 tasks on the stack to be collected
    There are 15 tasks remaining on the stack to be collected
    There are now 0 tasks on the stack to be collected

Worker::getStacked
==================

获取剩余的栈大小

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Worker::getStacked</span> ( <span
class="methodparam">void</span> )

返回栈中剩余的任务数量

### 参数

此函数没有参数。

### 返回值

返回 worker 中等待执行的任务数量

### 范例

**示例 \#1 <span class="classname">Worker::getStacked</span> 基本示例**

``` php
<?php
$worker = new Worker();

for ($i = 0; $i < 5; ++$i) {
    $worker->stack(new class extends Threaded {});
}

echo "There are {$worker->getStacked()} stacked tasks\n";
```

以上例程会输出：

    There are 5 stacked tasks

Worker::isShutdown
==================

状态检测

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Worker::isShutdown</span> ( <span
class="methodparam">void</span> )

Worker 对象是否被关闭

### 参数

此函数没有参数。

### 返回值

布尔值，表示 worker 是否已经被关闭

### 范例

**示例 \#1 检测 Worker 对象状态**

``` php
<?php
$worker = new Worker();
$worker->start();

var_dump($worker->isShutdown());

$worker->shutdown();

var_dump($worker->isShutdown());
```

以上例程会输出：

    bool(false)
    bool(true)

Worker::isWorking
=================

状态检测

**Warning**

pthreads v3 中已移除此方法。 请使用 <span
class="methodname">Worker::getStacked</span> 方法来检测 worker 中是还有
尚待执行的任务。

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Worker::isWorking</span> ( <span
class="methodparam">void</span> )

Worker 对象是否正在执行栈中对象

### 参数

此函数没有参数。

### 返回值

布尔值，表示 Worker 对象是否在执行栈中对象

### 范例

**示例 \#1 检测 Worker 对象状态**

``` php
<?php
$my = new Worker();
$my->start();
/* ... */
if ($my->isWorking()) {
    /* ... the Worker is busy executing another object */
}
?>
```

Worker::shutdown
================

关闭 Worker

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Worker::shutdown</span> ( <span
class="methodparam">void</span> )

在执行完已入栈对象之后，关闭这个 Worker 对象

### 参数

此函数没有参数。

### 返回值

布尔值，表示这个 worker 是否被成功关闭。

### 范例

**示例 \#1 关闭 Worker**

``` php
<?php
$my = new Worker();
$my->start();
/* 入栈和执行任务 */
var_dump($my->shutdown());
```

以上例程会输出：

    bool(true)

Worker::stack
=============

将要执行的任务入栈

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Worker::stack</span> ( <span
class="methodparam"><span class="type">Threaded</span> `&$work`</span> )

将要执行的任务入栈到 Worker 对象

### 参数

`work`  
要被 Worker 执行的 <span class="classname">Threaded</span> 派生对象

### 返回值

入栈之后，Worker 对象栈的大小。

### 范例

**示例 \#1 向 Worker 中入栈任务并执行**

``` php
<?php
$worker = new Worker();
$work = new class extends Threaded {};

var_dump($worker->stack($work));
```

以上例程会输出：

    int(1)

Worker::unstack
===============

将要执行的任务出栈

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Worker::unstack</span> ( <span
class="methodparam">void</span> )

把 Worker 栈顶的（最老的那个）任务从栈中移除。

### 参数

此函数没有参数。

### 返回值

出栈之后，Worker 栈的大小。

### 更新日志

| 版本 | 说明                                            |
|------|-------------------------------------------------|
| v3   | 移除了要出栈的任务参数。 现在只能移除栈顶元素。 |

### 范例

**示例 \#1 从 Worker 栈中移除对象**

``` php
<?php
$my = new Worker();
$work = new class extends Threaded {};

var_dump($my->stack($work));
var_dump($my->unstack());
```

以上例程会输出：

    int(1)
    int(0)

简介
----

**Caution**

<span class="classname">Collectable</span> was previously a class (in
pthreads v2 and below). Now, it is an interface in pthreads v3 that is
implemented by the <span class="classname">Threaded</span> class.

Represents a garbage-collectable object.

接口摘要
--------

**Collectable**

<span class="ooclass"> class **Collectable** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isGarbage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setGarbage</span> ( <span
class="methodparam">void</span> )

}

Collectable::isGarbage
======================

Determine whether an object has been marked as garbage

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Collectable::isGarbage</span> ( <span
class="methodparam">void</span> )

Can be called in <span class="methodname">Pool::collect</span> to
determine if this object is garbage.

### 参见

-   <span class="methodname">Pool::collect</span>

Collectable::setGarbage
=======================

Mark an object as garbage

**Warning**

This method has been removed in pthreads v3.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Collectable::setGarbage</span> ( <span
class="methodparam">void</span> )

Should be called once per object when the object is finished being
executed or referenced.

### 参见

-   <span class="methodname">Collectable::isGarbage</span>

简介
----

Pool 对象是多个 Worker 对象的容器，同时也是它们的控制器。

线程池是对 Worker 功能的高层抽象，包括按照 pthreads
需要的方式来管理应用的功能。

类摘要
------

**Pool**

<span class="ooclass"> class **Pool** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$size` ;

<span class="modifier">protected</span> `$class` ;

<span class="modifier">protected</span> `$workers` ;

<span class="modifier">protected</span> `$ctor` ;

<span class="modifier">protected</span> `$last` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">collect</span> (\[ <span class="methodparam"><span
class="type">Callable</span> `$collector`</span> \] )

<span class="modifier">public</span> <span class="type">Pool</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$class`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ctor`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resize</span> ( <span class="methodparam"><span
class="type">int</span> `$size`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">shutdown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">submit</span> ( <span class="methodparam"><span
class="type">Threaded</span> `$task`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">submitTo</span> ( <span class="methodparam"><span
class="type">int</span> `$worker`</span> , <span
class="methodparam"><span class="type">Threaded</span> `$task`</span> )

}

属性
----

`size`  
Pool 对象可容纳的 Worker 对象的最大数量

`class`  
Worker 的类

`workers`  
指向 Worker 对象的引用

`ctor`  
构造新的 Worker 对象时所需的参数

`last`  
最后使用的 Worker 对象在池中的位置偏移量

Pool::collect
=============

回收已完成任务的引用

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Pool::collect</span> (\[ <span
class="methodparam"><span class="type">Callable</span>
`$collector`</span> \] )

对于视为垃圾的引用，使用给定的垃圾收集器进行收集

### 参数

`collector`  
垃圾收集器，它返回一个布尔值表示这个任务是否可以被进行垃圾收集。
仅在极少的情况下需要一个自定义的垃圾收集器。

### 返回值

池中剩余的待收集的任务数量。

### 更新日志

| 版本 | 说明                                                |
|------|-----------------------------------------------------|
| v3   | `collector` 参数变为可选参数， 并且返回值改为整数。 |

### 范例

**示例 \#1 <span class="methodname">Pool::collect</span> 基本用法示例**

``` php
<?php
$pool = new Pool(4);

for ($i = 0; $i < 15; ++$i) {
    $pool->submit(new class extends Threaded {});
}

while ($pool->collect()); // 直到全部的任务都完成执行之后才会继续下面的代码

$pool->shutdown();
```

Pool::\_\_construct
===================

创建新的 Worker 对象池

### 说明

<span class="modifier">public</span> <span class="type">Pool</span>
<span class="methodname">Pool::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$class`</span> \[, <span class="methodparam"><span
class="type">array</span> `$ctor`</span> \]\] )

创建新的 Worker 对象池，但是所对应的线程是延迟创建的的，也就是说，
直到需要执行任务的时候 才会创建对应的线程。

### 参数

`size`  
此 Pool 对象可创建的 Worker 对象的最大数量

`class`  
新创建的 Worker 对象的类。 如果不指定类，那么会使用默认的 <span
class="classname">Worker</span> 类。

`ctor`  
创建 Worker 对象时所用到的参数，以数组方式传入

### 返回值

新创建的 Pool 对象

### 范例

**示例 \#1 创建 Pool 对象**

``` php
<?php
class MyWorker extends Worker {
    
    public function __construct(Something $something) {
        $this->something = $something;
    }
    
    public function run() {
        /** ... **/
    }
}

$pool = new Pool(8, \MyWorker::class, [new Something()]);

var_dump($pool);
?>
```

以上例程会输出：

    object(Pool)#1 (6) {
      ["size":protected]=>
      int(8)
      ["class":protected]=>
      string(8) "MyWorker"
      ["workers":protected]=>
      NULL
      ["work":protected]=>
      NULL
      ["ctor":protected]=>
      array(1) {
        [0]=>
        object(Something)#2 (0) {
        }
      }
      ["last":protected]=>
      int(0)
    }

Pool::resize
============

改变 Pool 对象的可容纳 Worker 对象的数量

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Pool::resize</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> )

改变 Pool 对象的可容纳 Worker 对象的数量

### 参数

`size`  
此 Pool 对象可创建 Worker 对象的最大数量

### 返回值

void

Pool::shutdown
==============

停止所有的 Worker 对象

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Pool::shutdown</span> ( <span
class="methodparam">void</span> )

停止此 Pool 中所有的 Worker 对象。此方法调用会进入阻塞状态，
直到所有已经提交到这个 Pool 中的任务都执行完毕。

### 参数

此函数没有参数。

### 返回值

无返回值

### 范例

**示例 \#1 完全停止一个 Pool**

``` php
<?php
class Task extends Threaded
{
    public function run()
    {
        usleep(500000);
    }
}

$pool = new Pool(4);

for ($i = 0; $i < 10; ++$i) {
    $pool->submit(new Task());
}

$pool->shutdown(); // 进入阻塞状态，直到所有已经提交到 Pool 中的任务都执行完毕
```

Pool::submit
============

提交对象以执行

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Pool::submit</span> ( <span class="methodparam"><span
class="type">Threaded</span> `$task`</span> )

将任务提交到 Pool 中的下一个 Worker 对象

### 参数

`task`  
要执行的任务

### 返回值

执行新加入对象的 Worker 对象 ID

### 范例

**示例 \#1 提交任务**

``` php
<?php
class MyWork extends Threaded {
    
    public function run() {
        /* ... */
    }
}

class MyWorker extends Worker {
    
    public function __construct(Something $something) {
        $this->something = $something;
    }
    
    public function run() {
        /** ... **/
    }
}

$pool = new Pool(8, \MyWorker::class, [new Something()]);
$pool->submit(new MyWork());
var_dump($pool);
?>
```

以上例程会输出：

    object(Pool)#1 (6) {
      ["size":protected]=>
      int(8)
      ["class":protected]=>
      string(8) "MyWorker"
      ["workers":protected]=>
      array(1) {
        [0]=>
        object(MyWorker)#4 (1) {
          ["something"]=>
          object(Something)#5 (0) {
          }
        }
      }
      ["work":protected]=>
      array(1) {
        [0]=>
        object(MyWork)#3 (1) {
          ["worker"]=>
          object(MyWorker)#5 (1) {
            ["something"]=>
            object(Something)#6 (0) {
            }
          }
        }
      }
      ["ctor":protected]=>
      array(1) {
        [0]=>
        object(Something)#2 (0) {
        }
      }
      ["last":protected]=>
      int(1)
    }

Pool::submitTo
==============

提交一个任务到特定的 Worker 以执行

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Pool::submitTo</span> ( <span
class="methodparam"><span class="type">int</span> `$worker`</span> ,
<span class="methodparam"><span class="type">Threaded</span>
`$task`</span> )

将对象提交到 Pool 中某个特定的 Worker 对象来执行。Worker 的下标从 0
开始， 由于 Pool 中的线程是懒加载机制， 所以 Worker 对象仅在 Pool
需要执行任务的时候才会真正被创建。

### 参数

`worker`  
用来执行任务的 Worker 对象，下标从 *0* 开始。

`task`  
要执行的任务

### 返回值

接受新加入对象的 Worker 对象ID

### 范例

**示例 \#1 提交任务到特定的 Worker**

``` php
<?php
class Task extends Threaded {
    public function run() {
        var_dump(Thread::getCurrentThreadID());
    }
}

$pool = new Pool(2);

$pool->submit(new Task());

for ($i = 0; $i < 5; ++$i) {
    $pool->submitTo(0, new Task()); // 将所有的任务都入栈到下标为 0 的 Worker
}

$pool->submitTo(1, new Task()); // 由于第二个 Worker 尚未存在，所以不可以将任务入栈到第二个 Worker

$pool->shutdown();
```

以上例程会输出：

    int(4475011072)
    int(4475011072)
    int(4475011072)
    int(4475011072)
    int(4475011072)
    int(4475011072)

    Fatal error: Uncaught Exception: The selected worker (1) does not exist in %s:%d

简介
----

**Warning**

pthreads v3 中已经将 <span class="classname">Mutex</span> 类移除。

Mutex 类中包含一些直接访问 Posix 互斥量的静态方法

类摘要
------

**Mutex**

<span class="ooclass"> class **Mutex** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">create</span> (\[ <span class="methodparam"> <span
class="type">bool</span> `$lock` </span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">destroy</span> ( <span class="methodparam">
<span class="type">int</span> `$mutex` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">lock</span> ( <span class="methodparam"> <span
class="type">int</span> `$mutex` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">trylock</span> ( <span class="methodparam">
<span class="type">int</span> `$mutex` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">unlock</span> ( <span class="methodparam">
<span class="type">int</span> `$mutex` </span> \[, <span
class="methodparam"> <span class="type">bool</span> `$destroy` </span>
\] )

}

Mutex::create
=============

创建一个互斥量

**Warning**

pthreads v3 中已经将 <span class="classname">Mutex</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Mutex::create</span> (\[ <span class="methodparam">
<span class="type">bool</span> `$lock` </span> \] )

为调用者创建一个互斥量，同时也可以通过 lock
参数设置是否在创建完成之后立即加锁此互斥量

### 参数

`lock`  
如果设置 lock 参数为
true，表示创建互斥量之后，立即加锁，然后再将互斥量句柄返回给调用者

### 返回值

新创建的互斥量句柄，这个互斥量可能已经处于加锁状态，由 lock 参数控制

### 范例

**示例 \#1 互斥量的创建与销毁**

``` php
<?php
/** 不可以使用 new 关键字，因为互斥量不是 PHP 对象 **/
$mutex = Mutex::create();
/** 你已经持有了这个互斥量的物理地址 **/
var_dump($mutex);
/** 不要忘记销毁你创建的互斥量 **/
Mutex::destroy($mutex);
?>
```

以上例程会输出：

    int(40096976)

Mutex::destroy
==============

销毁互斥量

**Warning**

pthreads v3 中已经将 <span class="classname">Mutex</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Mutex::destroy</span> ( <span
class="methodparam"> <span class="type">int</span> `$mutex` </span> )

当不再使用某个已经创建的互斥量句柄之后，程序员需要显式的销毁它。

### 参数

`mutex`  
通过调用函数 <span class="function">Mutex::create</span>
返回的互斥量句柄。 当调用 <span class="function">Mutex::destroy</span>
函数之后，任何线程都无法再给这个互斥量加锁了。

### 返回值

布尔值，表示操作是否成功

### 范例

**示例 \#1 互斥量的创建与销毁**

``` php
<?php
/** 不可以使用 new 关键字，因为互斥量不是 PHP 对象 **/
$mutex = Mutex::create();
/** 你已经持有了这个互斥量的物理地址 **/
var_dump($mutex);
/** 不要忘记销毁你创建的互斥量 **/
Mutex::destroy($mutex);
?>
```

以上例程会输出：

    int(40096976)

Mutex::lock
===========

给互斥量加锁

**Warning**

pthreads v3 中已经将 <span class="classname">Mutex</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Mutex::lock</span> ( <span class="methodparam">
<span class="type">int</span> `$mutex` </span> )

尝试为调用者给互斥量加锁。

尝试给已经被其他线程加锁的互斥量再次加锁会导致调用者线程进入阻塞状态。

### 参数

`mutex`  
通过调用函数 <span class="function">Mutex::create</span>
产生的互斥量句柄。

### 返回值

布尔值，表示操作是否成功。

### 范例

**示例 \#1 互斥量加锁与解锁**

``` php
<?php
/** 不可以使用 new 关键字，因为互斥量不是 PHP 对象 **/
$mutex = Mutex::create();
/** 现在可以在任何线程上下文中给这个互斥量加锁了 **/
var_dump(Mutex::lock($mutex));
/** 销毁一个处于加锁状态的互斥量的操作是无效的 **/
var_dump(Mutex::unlock($mutex));
/** 永远不要忘记销毁你创建的互斥量 **/
Mutex::destroy($mutex);
?>
```

以上例程会输出：

    bool(true)
    bool(true)

Mutex::trylock
==============

尝试给互斥量加锁

**Warning**

pthreads v3 中已经将 <span class="classname">Mutex</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Mutex::trylock</span> ( <span
class="methodparam"> <span class="type">int</span> `$mutex` </span> )

尝试给一个互斥量加锁，即使这个互斥量已经被其他线程锁定，也不会导致调用者线程进入阻塞状态。

### 参数

`mutex`  
通过调用函数 <span class="function">Mutex::create</span>
产生的互斥量句柄。

### 返回值

布尔值，表示操作是否成功

### 范例

**示例 \#1 互斥量的加锁与解锁**

``` php
<?php
/** 不可以使用 new 关键字，因为互斥量不是 PHP 对象 **/
$mutex = Mutex::create();
/** 现在可以在任何线程上下文中给这个互斥量加锁了 **/
var_dump(Mutex::lock($mutex));
/** 销毁一个处于加锁状态的互斥量的操作是无效的 **/
var_dump(Mutex::unlock($mutex));
/** 永远不要忘记销毁你创建的互斥量 **/
Mutex::destroy($mutex);
?>
```

以上例程会输出：

    bool(true)
    bool(true)

Mutex::unlock
=============

释放互斥量上的锁

**Warning**

pthreads v3 中已经将 <span class="classname">Mutex</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Mutex::unlock</span> ( <span
class="methodparam"> <span class="type">int</span> `$mutex` </span> \[,
<span class="methodparam"> <span class="type">bool</span> `$destroy`
</span> \] )

尝试为互斥量解锁，也可以通过 destroy
参数控制是否在解锁之后同时销毁此互斥量。
只有持有互斥量锁的线程才可以对这个互斥量进行解锁操作。

### 参数

`mutex`  
通过调用函数 <span class="function">Mutex::create</span>
产生的互斥量句柄。

`destroy`  
此参数为 true 表示如果解锁成功，则同时销毁此互斥量。

### 返回值

A boolean indication of success.

### 范例

**示例 \#1 互斥量的加锁与解锁**

``` php
<?php
/** 不可以使用 new 关键字，因为互斥量不是 PHP 对象 **/
$mutex = Mutex::create();
/** 现在可以在任何线程上下文中给这个互斥量加锁了 **/
var_dump(Mutex::lock($mutex));
/** 销毁一个处于加锁状态的互斥量的操作是无效的 **/
var_dump(Mutex::unlock($mutex));
/** 永远不要忘记销毁你创建的互斥量 **/
Mutex::destroy($mutex);
?>
```

以上例程会输出：

    bool(true)
    bool(true)

简介
----

**Warning**

pthreads v3 中已经将 <span class="classname">Cond</span> 类移除。

Cond 类中的静态方法可以用来直接访问 Posix 的条件变量。

类摘要
------

**Cond**

<span class="ooclass"> class **Cond** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">broadcast</span> ( <span class="methodparam">
<span class="type">int</span> `$condition` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">create</span> ( <span class="methodparam">void</span>
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">destroy</span> ( <span class="methodparam">
<span class="type">int</span> `$condition` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">signal</span> ( <span class="methodparam">
<span class="type">int</span> `$condition` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">wait</span> ( <span class="methodparam"> <span
class="type">int</span> `$condition` </span> , <span
class="methodparam"> <span class="type">int</span> `$mutex` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$timeout`
</span> \] )

}

Cond::broadcast
===============

广播条件变量

**Warning**

pthreads v3 中已经将 <span class="classname">Cond</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Cond::broadcast</span> ( <span
class="methodparam"> <span class="type">int</span> `$condition` </span>
)

向所有由于调用 <span class="function">Cond::wait</span>
函数而进入条件阻塞状态的线程发送广播。

### 参数

`condition`  
通过调用函数 <span class="function">Cond::create</span>
获得的条件变量句柄。

### 返回值

布尔值，表示操作是否成功。

### 范例

**示例 \#1 广播条件变量**

``` php
<?php
/** 不可以使用 new 关键字，因为 Cond 不是 PHP 对象 **/
$cond = Cond::create();
/** 调用者必须给关联的互斥量加锁，然后才可以进行广播（调用 broadcast 方法） **/
var_dump(Cond::broadcast($cond));
/** 永远不要忘记销毁你创建的条件变量 **/
Cond::destroy($cond);
?>
```

以上例程会输出：

    bool(true)

Cond::create
============

创建一个条件变量

**Warning**

pthreads v3 中已经将 <span class="classname">Cond</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Cond::create</span> ( <span
class="methodparam">void</span> )

创建一个条件变量。

### 参数

此函数没有参数。

### 返回值

指向条件变量的句柄。

### 范例

**示例 \#1 条件变量的创建与销毁**

``` php
<?php
/** 不可以使用 new 关键字，因为 Cond 不是 PHP 对象 **/
$cond = Cond::create();
/** 现在你可以在任意线程上下文中使用此条件变量 **/
var_dump($cond);
/** 永远不要忘记销毁你创建的条件变量 **/
Cond::destroy($cond);
?>
```

以上例程会输出：

    int(4540682)

Cond::destroy
=============

销毁条件变量

**Warning**

pthreads v3 中已经将 <span class="classname">Cond</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Cond::destroy</span> ( <span
class="methodparam"> <span class="type">int</span> `$condition` </span>
)

当不再需要所创建的条件变量时，程序员必须显式的销毁它。 当调用 <span
class="function">Cond::destroy</span>
函数时，必须保证其他线程没有处于等待此条件变量的阻塞状态（通过调用函数
<span class="function">Cond::wait</span> 进入条件阻塞状态）。

### 参数

`condition`  
通过调用 <span class="function">Cond::create</span>
函数获得的条件变量句柄

### 返回值

布尔值，表示操作是否成功。

### 范例

**示例 \#1 条件变量的创建与销毁**

``` php
<?php
/** 不可以使用 new 关键字，因为 Cond 不是 PHP 对象 **/
$cond = Cond::create();
/** 现在你可以在任意线程上下文中使用此条件变量 **/
var_dump($cond);
/** 永远不要忘记销毁你创建的条件变量 **/
Cond::destroy($cond);
?>
```

以上例程会输出：

    int(4540682)

Cond::signal
============

发送唤醒信号

**Warning**

pthreads v3 中已经将 <span class="classname">Cond</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Cond::signal</span> ( <span
class="methodparam"> <span class="type">int</span> `$condition` </span>
)

### 参数

`condition`  
通过调用 <span class="function">Cond::create</span>
函数获得的条件变量句柄

### 返回值

布尔值，表示操作是否成功。

### 范例

**示例 \#1 发送唤醒信号**

``` php
<?php
/** 不可以使用 new 关键字，因为 Cond 不是 PHP 对象 **/
$cond = Cond::create();
/** 调用者必须持有关联的互斥量锁，然后才可以进行唤醒信号发送（调用 signal 方法）  **/
var_dump(Cond::signal($cond));
/** 永远不要忘记销毁你创建的条件变量 **/
Cond::destroy($cond);
?>
```

以上例程会输出：

    bool(true)

Cond::wait
==========

等待

**Warning**

pthreads v3 中已经将 <span class="classname">Cond</span> 类移除。

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Cond::wait</span> ( <span class="methodparam">
<span class="type">int</span> `$condition` </span> , <span
class="methodparam"> <span class="type">int</span> `$mutex` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$timeout`
</span> \] )

进入条件变量等待状态。通过 timeout 参数可以设置等待超时时间。

### 参数

`condition`  
通过调用 <span class="function">Cond::create</span>
函数获得的条件变量句柄

`mutex`  
通过调用 <span class="function">Mutex::create</span>
函数获得的互斥量，并且已经被调用者线程加锁。

`timeout`  
等待超时，以毫秒为单位。

### 返回值

布尔值，表示操作是否成功。

### 范例

**示例 \#1 等待条件变量**

``` php
<?php
/** 请注意，本示例会导致进程挂起 **/
$mutex = Mutex::create(true);
/** 不可以使用 new 关键字，因为 Cond 不是 PHP 对象 **/
$cond = Cond::create();
/** The caller must lock the associated Mutex before a call to broadcast **/
var_dump(Cond::wait($cond, $mutex));
/** 永远不要忘记销毁你创建的条件变量及互斥量 **/
Cond::destroy($cond);
Mutex::unlock($mutex);
Mutex::destroy($mutex);
?>
```

以上例程会输出：

    int(49685473)

简介
----

The <span class="classname">Volatile</span> class is new to pthreads v3.
Its introduction is a consequence of the new immutability semantics of
<span class="classname">Threaded</span> members of <span
class="classname">Threaded</span> classes. The <span
class="classname">Volatile</span> class enables for mutability of its
<span class="classname">Threaded</span> members, and is also used to
store PHP arrays in <span class="classname">Threaded</span> contexts.

类摘要
------

**Volatile**

<span class="ooclass"> class **Volatile** </span> <span class="ooclass">
<span class="modifier">extends</span> **Threaded** </span> <span
class="oointerface">implements <span
class="interfacename">Collectable</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> {

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Threaded::chunk</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> , <span
class="methodparam"><span class="type">bool</span> `$preserve`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Threaded::count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::extend</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> )

<span class="modifier">public</span> <span class="type">Threaded</span>
<span class="methodname">Threaded::from</span> ( <span
class="methodparam"><span class="type">Closure</span> `$run`</span> \[,
<span class="methodparam"><span class="type">Closure</span>
`$construct`</span> \[, <span class="methodparam"><span
class="type">array</span> `$args`</span> \]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Threaded::getTerminationInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isRunning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isTerminated</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::isWaiting</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$from`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$overwrite`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::notify</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::notifyOne</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Threaded::run</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">Threaded::shift</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Threaded::synchronized</span> ( <span
class="methodparam"><span class="type">Closure</span> `$block`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::unlock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Threaded::wait</span> (\[ <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \] )

}

范例
----

**示例 \#1 New immutability semantics of Threaded**

``` php
<?php

class Task extends Threaded
{
    public function __construct()
    {
        $this->data = new Threaded();

        // attempt to overwrite a Threaded property of a Threaded class (invalid)
        $this->data = new StdClass();
    }
}

var_dump((new Task())->data);
```

以上例程的输出类似于：

    RuntimeException: Threaded members previously set to Threaded objects are immutable, cannot overwrite data in %s:%d

**示例 \#2 Volatile use-case**

``` php
<?php

class Task extends Volatile
{
    public function __construct()
    {
        $this->data = new Threaded();

        // attempt to overwrite a Threaded property of a Volatile class (valid)
        $this->data = new StdClass();
    }
}

var_dump((new Task())->data);
```

以上例程的输出类似于：

    object(stdClass)#3 (0) {
    }
