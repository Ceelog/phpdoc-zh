parallel
========

**目录**

-   [简介](/intro/parallel.html)
-   [Installation](/parallel/setup.html)
-   [Philosophy](/philosophy/parallel.html)
-   [Functional API](/functional/parallel.html)
    -   [parallel\\bootstrap](/functional/parallel.html#parallel\bootstrap)
        — Bootstrapping
    -   [parallel\\run](/functional/parallel.html#parallel\run) —
        Execution
-   [parallel\\Runtime](/class/parallel-runtime.html) — The
    parallel\\Runtime class
    -   [parallel\\Runtime::\_\_construct](/class/parallel-runtime.html#parallel\Runtime::__construct)
        — Runtime Construction
    -   [parallel\\Runtime::run](/class/parallel-runtime.html#parallel\Runtime::run)
        — Execution
    -   [parallel\\Runtime::close](/class/parallel-runtime.html#parallel\Runtime::close)
        — Runtime Graceful Join
    -   [parallel\\Runtime::kill](/class/parallel-runtime.html#parallel\Runtime::kill)
        — Runtime Join
-   [parallel\\Future](/class/parallel-future.html) — The
    parallel\\Future class
    -   [parallel\\Future::cancel](/class/parallel-future.html#parallel\Future::cancel)
        — Cancellation
    -   [parallel\\Future::cancelled](/class/parallel-future.html#parallel\Future::cancelled)
        — State Detection
    -   [parallel\\Future::done](/class/parallel-future.html#parallel\Future::done)
        — State Detection
    -   [parallel\\Future::value](/class/parallel-future.html#parallel\Future::value)
        — Resolution
-   [parallel\\Channel](/class/parallel-channel.html) — The
    parallel\\Channel class
    -   [parallel\\Channel::\_\_construct](/class/parallel-channel.html#parallel\Channel::__construct)
        — Channel Construction
    -   [parallel\\Channel::make](/class/parallel-channel.html#parallel\Channel::make)
        — Access
    -   [parallel\\Channel::open](/class/parallel-channel.html#parallel\Channel::open)
        — Access
    -   [parallel\\Channel::recv](/class/parallel-channel.html#parallel\Channel::recv)
        — Sharing
    -   [parallel\\Channel::send](/class/parallel-channel.html#parallel\Channel::send)
        — Sharing
    -   [parallel\\Channel::close](/class/parallel-channel.html#parallel\Channel::close)
        — Closing
-   [parallel\\Events](/class/parallel-events.html) — The
    parallel\\Events class
    -   [parallel\\Events::setBlocking](/class/parallel-events.html#parallel\Events::setBlocking)
        — Behaviour
    -   [parallel\\Events::setTimeout](/class/parallel-events.html#parallel\Events::setTimeout)
        — Behaviour
    -   [parallel\\Events::setInput](/class/parallel-events.html#parallel\Events::setInput)
        — Input
    -   [parallel\\Events::addChannel](/class/parallel-events.html#parallel\Events::addChannel)
        — Targets
    -   [parallel\\Events::addFuture](/class/parallel-events.html#parallel\Events::addFuture)
        — Targets
    -   [parallel\\Events::remove](/class/parallel-events.html#parallel\Events::remove)
        — Targets
    -   [parallel\\Events::poll](/class/parallel-events.html#parallel\Events::poll)
        — Polling
-   [parallel\\Events\\Input](/class/parallel-events-input.html) — The
    parallel\\Events\\Input class
    -   [parallel\\Events\\Input::add](/class/parallel-events-input.html#parallel\Events\Input::add)
        — Inputs
    -   [parallel\\Events\\Input::clear](/class/parallel-events-input.html#parallel\Events\Input::clear)
        — Inputs
    -   [parallel\\Events\\Input::remove](/class/parallel-events-input.html#parallel\Events\Input::remove)
        — Inputs
-   [parallel\\Events\\Event](/class/parallel-events-event.html) — The
    parallel\\Events\\Event class
-   [parallel\\Events\\Event\\Type](/class/parallel-events-event-type.html)
    — The parallel\\Events\\Event\\Type class
-   [parallel\\Sync](/class/parallel-sync.html) — The parallel\\Sync
    class
    -   [parallel\\Sync::\_\_construct](/class/parallel-sync.html#parallel\Sync::__construct)
        — Construction
    -   [parallel\\Sync::get](/class/parallel-sync.html#parallel\Sync::get)
        — Access
    -   [parallel\\Sync::set](/class/parallel-sync.html#parallel\Sync::set)
        — Access
    -   [parallel\\Sync::wait](/class/parallel-sync.html#parallel\Sync::wait)
        — Synchronization
    -   [parallel\\Sync::notify](/class/parallel-sync.html#parallel\Sync::notify)
        — Synchronization
    -   [parallel\\Sync::\_\_invoke](/class/parallel-sync.html#parallel\Sync::__invoke)
        — Synchronization

Runtime Objects
---------------

Each runtime represents a single PHP thread, the thread is created (and
bootstrapped) upon construction. The thread then waits for tasks to be
scheduled: Scheduled tasks will be executed FIFO and then the thread
will resume waiting until more tasks are scheduled, or it's closed,
killed, or destroyed by the normal scoping rules of PHP objects.

**Warning**

When a runtime is destroyed by the normal scoping rules of PHP objects,
it will first execute all of the tasks that were scheduled, and block
while doing so.

Runtime Bootstrapping
---------------------

When a new runtime is created, it does not share code with the thread
(or process) that created it. This means it doesn't have the same
classes and functions loaded, nor the same autoloader set. In some
cases, a very lightweight runtime is desirable because the tasks that
will be scheduled do not need access to the code in the parent thread.
In those cases where the tasks do need to access the same code, it is
enough to set an autoloader as the bootstrap.

> **Note**:
>
> preloading may be used in conjunction with parallel, in this case
> preloaded code is available without bootstrapping

类摘要
------

**parallel\\Runtime**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Runtime** </span> {

/\* Create \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$bootstrap`</span>
)

/\* Execute \*/

<span class="modifier">public</span> <span class="type"><span
class="type">Future</span><span class="type">null</span></span> <span
class="methodname">run</span> ( <span class="methodparam"><span
class="type">Closure</span> `$task`</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">Future</span><span class="type">null</span></span> <span
class="methodname">run</span> ( <span class="methodparam"><span
class="type">Closure</span> `$task`</span> , <span
class="methodparam"><span class="type">array</span> `$argv`</span> )

/\* Join \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">kill</span> ( <span
class="methodparam">void</span> )

}

parallel\\Runtime::\_\_construct
================================

Runtime Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Runtime::\_\_construct</span> ( <span
class="methodparam">void</span> )

Shall construct a new runtime without bootstrapping.

<span class="modifier">public</span> <span
class="methodname">parallel\\Runtime::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$bootstrap`</span>
)

Shall construct a bootstrapped runtime.

### 参数

`bootstrap`  
The location of a bootstrap file, generally an autoloader.

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Runtime\\Error</span> if thread
could not be created

**Warning**

Shall throw <span class="type">parallel\\Runtime\\Bootstrap</span> if
bootstrapping failed

parallel\\Runtime::run
======================

Execution

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">Future</span><span class="type">null</span></span> <span
class="methodname">parallel\\Runtime::run</span> ( <span
class="methodparam"><span class="type">Closure</span> `$task`</span> )

Shall schedule `task` for execution in parallel.

<span class="modifier">public</span> <span class="type"><span
class="type">Future</span><span class="type">null</span></span> <span
class="methodname">parallel\\Runtime::run</span> ( <span
class="methodparam"><span class="type">Closure</span> `$task`</span> ,
<span class="methodparam"><span class="type">array</span> `$argv`</span>
)

Shall schedule `task` for execution in parallel, passing `argv` at
execution time.

### 参数

`task`  
A <span class="classname">Closure</span> with specific characteristics.

`argv`  
An <span class="type">array</span> of arguments with specific
characteristics to be passed to `task` at execution time.

### Task Characteristics

Closures scheduled for parallel execution must not:

-   accept or return by reference
-   accept or return internal objects (see notes)
-   execute a limited set of instructions

Instructions prohibited in Closures intended for parallel execution are:

-   yield
-   use by-reference
-   declare class
-   declare named function

> **Note**:
>
> Nested closures may yield or use by-reference, but must not contain
> class or named function declarations.

> **Note**:
>
> No instructions are prohibited in the files which the task may
> include.

### Arguments Characteristics

Arguments must not:

-   contain references
-   contain resources
-   contain internal objects (see notes)

> **Note**:
>
> In the case of file stream resources, the resource will be cast to the
> file descriptor and passed as <span class="type">int</span> where
> possible, this is unsupported on Windows.

### Internal Objects Notes

Internal objects generally use a custom structure which cannot be copied
by value safely, PHP currently lacks the mechanics to do this (without
serialization) and so only objects that do not use a custom structure
may be shared.

Some internal objects do not use a custom structure, for example <span
class="classname">parallel\\Events\\Event</span> and so may be shared.

Closures are a special kind of internal object and support being copied
by value, and so may be shared.

Channels are central to writing parallel code and support concurrent
access and execution by necessity, and so may be shared.

**Warning**

A user class that extends an internal class may use a custom structure
as defined by the internal class, in which case they cannot be copied by
value safely, and so may not be shared.

### 返回值

**Warning**

The return <span class="type">parallel\\Future</span> must not be
ignored when the task contains a return or throw statement.

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Runtime\\Error\\Closed</span>
if <span class="type">parallel\\Runtime</span> was closed.

**Warning**

Shall throw <span
class="type">parallel\\Runtime\\Error\\IllegalFunction</span> if `task`
is a closure created from an internal function.

**Warning**

Shall throw <span
class="type">parallel\\Runtime\\Error\\IllegalInstruction</span> if
`task` contains illegal instructions.

**Warning**

Shall throw <span
class="type">parallel\\Runtime\\Error\\IllegalParameter</span> if `task`
accepts or `argv` contains illegal variables.

**Warning**

Shall throw <span
class="type">parallel\\Runtime\\Error\\IllegalReturn</span> if `task`
returns illegally.

parallel\\Runtime::close
========================

Runtime Graceful Join

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Runtime::close</span> ( <span
class="methodparam">void</span> )

Shall request that the runtime shutsdown.

> **Note**:
>
> Tasks scheduled for execution will be executed before the shutdown
> occurs.

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Runtime\\Error\\Closed</span>
if <span class="type">Runtime</span> was already closed.

parallel\\Runtime::kill
=======================

Runtime Join

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Runtime::kill</span> ( <span
class="methodparam">void</span> )

Shall attempt to force the runtime to shutdown.

> **Note**:
>
> Tasks scheduled for execution will not be executed, the currently
> running task shall be interrupted.

**Warning**

Internal function calls in progress cannot be interrupted.

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Runtime\\Error\\Closed</span>
if <span class="type">Runtime</span> was closed.

Futures
-------

A Future represents the return value or uncaught exception from a task,
and exposes an API for cancellation.

**示例 \#1 Example showing Future as return value**

``` php
<?php
$runtime = new \parallel\Runtime;
$future  = $runtime->run(function(){
    return "World";
});
printf("Hello %s\n", $future->value());
?>
```

以上例程的输出类似于：

    Hello World

The behaviour of a future also allows it to be used as a simple
synchronization point even where the task does not return a value
explicitly.

**示例 \#2 Example showing Future as synchronization point**

``` php
<?php
$runtime = new \parallel\Runtime;
$future  = $runtime->run(function(){
    echo "in child ";
    for ($i = 0; $i < 500; $i++) {
        if ($i % 10 == 0) {
            echo ".";
        }
    }
    echo " leaving child";
});

$future->value();
echo "\nparent continues\n";
?>
```

以上例程的输出类似于：

    in child .................................................. leaving child
    parent continues

类摘要
------

**parallel\\Future**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Future** </span> {

/\* Resolution \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">value</span> ( <span
class="methodparam">void</span> )

/\* State \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">cancelled</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">done</span> ( <span
class="methodparam">void</span> )

/\* Cancellation \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">cancel</span> ( <span
class="methodparam">void</span> )

}

parallel\\Future::cancel
========================

Cancellation

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">parallel\\Future::cancel</span> ( <span
class="methodparam">void</span> )

Shall try to cancel the task

> **Note**:
>
> If task is running, it will be interrupted.

**Warning**

Internal function calls in progress cannot be interrupted.

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Future\\Error\\Killed</span> if
<span class="type">parallel\\Runtime</span> executing task was killed.

**Warning**

Shall throw <span class="type">parallel\\Future\\Error\\Cancelled</span>
if task was already cancelled.

parallel\\Future::cancelled
===========================

State Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">parallel\\Future::cancelled</span> ( <span
class="methodparam">void</span> )

Shall indicate if the task was cancelled

parallel\\Future::done
======================

State Detection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">parallel\\Future::done</span> ( <span
class="methodparam">void</span> )

Shall indicate if the task is completed

parallel\\Future::value
=======================

Resolution

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">parallel\\Future::value</span> ( <span
class="methodparam">void</span> )

Shall return (and if necessary wait for) return from task

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Future\\Error</span> if waiting
failed (internal error).

**Warning**

Shall throw <span class="type">parallel\\Future\\Error\\Killed</span> if
<span class="type">parallel\\Runtime</span> executing task was killed.

**Warning**

Shall throw <span class="type">parallel\\Future\\Error\\Cancelled</span>
if task was cancelled.

**Warning**

Shall throw <span class="type">parallel\\Future\\Error\\Foreign</span>
if task raised an unrecognized uncaught exception.

**Warning**

Shall rethrow <span class="type">Throwable</span> uncaught in task

Unbuffered Channels
-------------------

An unbuffered channel will block on calls to <span
class="methodname">parallel\\Channel::send</span> until there is a
receiver, and block on calls to <span
class="methodname">parallel\\Channel::recv</span> until there is a
sender. This means an unbuffered channel is not only a way to share data
among tasks but also a simple method of synchronization.

An unbuffered channel is the fastest way to share data among tasks,
requiring the least copying.

Buffered Channels
-----------------

A buffered channel will not block on calls to <span
class="methodname">parallel\\Channel::send</span> until capacity is
reached, calls to <span
class="methodname">parallel\\Channel::recv</span> will block until there
is data in the buffer.

Closures over Channels
----------------------

A powerful feature of parallel channels is that they allow the exchange
of closures between tasks (and runtimes).

When a closure is sent over a channel the closure is buffered, it
doesn't change the buffering of the channel transmitting the closure,
but it does effect the static scope inside the closure: The same closure
sent to different runtimes, or the same runtime, will not share their
static scope.

This means that whenever a closure is executed that was transmitted by a
channel, static state will be as it was when the closure was buffered.

Anonymous Channels
------------------

The anonymous channel constructor allows the programmer to avoid
assigning names to every channel: parallel will generate a unique name
for anonymous channels.

类摘要
------

**parallel\\Channel**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Channel** </span> {

/\* Anonymous Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

/\* Access \*/

<span class="modifier">public</span> <span class="type">Channel</span>
<span class="methodname">make</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">Channel</span>
<span class="methodname">make</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">Channel</span>
<span class="methodname">open</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> )

/\* Sharing \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">recv</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">send</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

/\* Closing \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

/\* Constant for Infinitely Buffered \*/

<span class="modifier">const</span> `Infinite` ;

}

parallel\\Channel::\_\_construct
================================

Channel Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Channel::\_\_construct</span> ( <span
class="methodparam">void</span> )

Shall make an anonymous unbuffered channel

<span class="modifier">public</span> <span
class="methodname">parallel\\Channel::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Shall make an anonymous buffered channel with the given capacity

### 参数

`capacity`  
May be <span class="type">Channel::Infinite</span> or a positive integer

parallel\\Channel::make
=======================

Access

### 说明

<span class="modifier">public</span> <span class="type">Channel</span>
<span class="methodname">parallel\\Channel::make</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Shall make an unbuffered channel with the given name

<span class="modifier">public</span> <span class="type">Channel</span>
<span class="methodname">parallel\\Channel::make</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">int</span>
`$capacity`</span> )

Shall make a buffered channel with the given name and capacity

### 参数

`name`  
The name of the channel.

`capacity`  
May be <span class="type">Channel::Infinite</span> or a positive integer

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Channel\\Error\\Existence</span> if channel
already exists.

parallel\\Channel::open
=======================

Access

### 说明

<span class="modifier">public</span> <span class="type">Channel</span>
<span class="methodname">parallel\\Channel::open</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Shall open the channel with the given name

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Channel\\Error\\Existence</span> if channel does
not exist.

parallel\\Channel::recv
=======================

Sharing

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">parallel\\Channel::recv</span> ( <span
class="methodparam">void</span> )

Shall recv a value from this channel

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Channel\\Error\\Closed</span>
if channel is closed.

parallel\\Channel::send
=======================

Sharing

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Channel::send</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Shall send the given value on this channel

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Channel\\Error\\Closed</span>
if channel is closed.

**Warning**

Shall throw <span
class="type">parallel\\Channel\\Error\\IllegalValue</span> if value is
illegal.

parallel\\Channel::close
========================

Closing

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Channel::close</span> ( <span
class="methodparam">void</span> )

Shall close this channel

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Channel\\Error\\Closed</span>
if channel is closed.

The Event Loop
--------------

The Event loop monitors the state of sets of futures and or channels
(targets) in order to perform read ( <span
class="methodname">parallel\\Future::value</span>, <span
class="methodname">parallel\\Channel::recv</span>) and write ( <span
class="methodname">parallel\\Channel::send</span>) operations as the
targets become available and the operations may be performed without
blocking the event loop.

类摘要
------

**parallel\\Events**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Events** </span> <span class="oointerface">implements <span
class="interfacename">Countable</span> </span> <span
class="oointerface">, <span class="interfacename">Traversable</span>
</span> {

/\* Input \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setInput</span> ( <span
class="methodparam"><span class="type">Input</span> `$input`</span> )

/\* Targets \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addChannel</span> ( <span
class="methodparam"><span class="type">parallel\\Channel</span>
`$channel`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFuture</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">parallel\\Future</span>
`$future`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">remove</span> ( <span class="methodparam"><span
class="type">string</span> `$target`</span> )

/\* Behaviour \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setBlocking</span> ( <span
class="methodparam"><span class="type">bool</span> `$blocking`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

/\* Polling \*/

<span class="modifier">public</span> <span class="type"><span
class="type">Event</span><span class="type">null</span></span> <span
class="methodname">poll</span> ( <span class="methodparam">void</span> )

}

parallel\\Events::setBlocking
=============================

Behaviour

### 说明

By default when events are polled for, blocking will occur (at the PHP
level) until the first event can be returned: Setting blocking mode to
false will cause poll to return control if the first target polled is
not ready.

This differs from setting a timeout of 0 with <span
class="methodname">parallel\\Events::setTimeout</span>, since a timeout
of 0, while allowed, will cause an exception to be raised, which may be
extremely slow or wasteful if what is really desired is non-blocking
behaviour.

A non-blocking loop effects the return value of <span
class="methodname">parallel\\Events::poll</span>, such that it may be
null before all events have been processed.

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events::setBlocking</span> ( <span
class="methodparam"><span class="type">bool</span> `$blocking`</span> )

Shall set blocking mode

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Events\\Error</span> if loop
has timeout set.

parallel\\Events::setTimeout
============================

Behaviour

### 说明

By default when events are polled for, blocking will occur (at the PHP
level) until the first event can be returned: Setting the timeout causes
an exception to be thrown when the timeout is reached.

This differs from setting blocking mode to false with <span
class="methodname">parallel\\Events::setBlocking</span>, which will not
cause an exception to be thrown.

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events::setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

Shall set the timeout in microseconds

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Events\\Error</span> if loop is
non-blocking.

parallel\\Events::setInput
==========================

Input

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events::setInput</span> ( <span
class="methodparam"><span class="type">Input</span> `$input`</span> )

Shall set `input` for this event loop

parallel\\Events::addChannel
============================

Targets

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events::addChannel</span> ( <span
class="methodparam"><span class="type">parallel\\Channel</span>
`$channel`</span> )

Shall watch for events on the given `channel`

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Events\\Error\\Existence</span>
if channel was already added.

parallel\\Events::addFuture
===========================

Targets

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events::addFuture</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">parallel\\Future</span>
`$future`</span> )

Shall watch for events on the given `future`

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Events\\Error\\Existence</span>
if target with the given name was already added.

parallel\\Events::remove
========================

Targets

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events::remove</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span> )

Shall remove the given `target`

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Events\\Error\\Existence</span>
if target with the given name was not found.

parallel\\Events::poll
======================

Polling

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">Event</span><span class="type">null</span></span> <span
class="methodname">parallel\\Events::poll</span> ( <span
class="methodparam">void</span> )

Shall poll for the next event

### 返回值

Should there be no targets remaining, null shall be returned

Should this be a non-blocking loop, and blocking would occur, null shall
be returned

Otherwise, the <span class="classname">parallel\\Events\\Event</span>
returned describes the event.

### Exceptions

**Warning**

Shall throw <span class="type">parallel\\Events\\Error\\Timeout</span>
if timeout is used and reached.

Events Input
------------

An Input object is a container for data that the <span
class="classname">parallel\\Events</span> object will write to <span
class="classname">parallel\\Channel</span> objects as they become
available. Multiple event loops may share an Input container - parallel
does not verify the contents of the container when it is set as the
input for a <span class="classname">parallel\\Events</span> object.

> **Note**:
>
> When a <span class="classname">parallel\\Events</span> object performs
> a write, the target is removed from the input object as if <span
> class="methodname">parallel\\Events\\Input::remove</span> were called.

类摘要
------

**parallel\\Events\\Input**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Events\\Input** </span> {

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">string</span> `$target`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">remove</span> ( <span class="methodparam"><span
class="type">string</span> `$target`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

}

parallel\\Events\\Input::add
============================

Inputs

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events\\Input::add</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Shall set input for the given target

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Events\\Input\\Error\\Existence</span> if input
for target already exists.

**Warning**

Shall throw <span
class="type">parallel\\Events\\Input\\Error\\IllegalValue</span> if
value is illegal (object, null).

parallel\\Events\\Input::clear
==============================

Inputs

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events\\Input::clear</span> ( <span
class="methodparam">void</span> )

Shall remove input for all targets

parallel\\Events\\Input::remove
===============================

Inputs

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">parallel\\Events\\Input::remove</span> ( <span
class="methodparam"><span class="type">string</span> `$target`</span> )

Shall remove input for the given target

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Events\\Input\\Error\\Existence</span> if input
for target does not exist.

Event Objects
-------------

When an Event is returned, `Event::$object` shall be removed from the
loop that returned it, should the event be a write event the <span
class="classname">Input</span> for `Event::$source` shall also be
removed.

类摘要
------

**parallel\\Events\\Event**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Events\\Event** </span> {

/\* Shall be one of <span class="classname">Event\\Type</span> constants
\*/

<span class="modifier">public</span> <span class="type">int</span>
`$type` ;

/\* Shall be the source of the event (target name) \*/

<span class="modifier">public</span> <span class="type">string</span>
`$source` ;

/\* Shall be either Future or Channel \*/

<span class="modifier">public</span> <span class="type">object</span>
`$object` ;

/\* Shall be set for Read/Error events \*/

<span class="modifier">public</span> `$value` ;

}

类摘要
------

**parallel\\Events\\Event\\Type**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Events\\Event\\Type** </span> {

/\* Event::$object was read into Event::$value \*/

<span class="modifier">const</span> `Read` ;

/\* Input for Event::$source written to Event::$object \*/

<span class="modifier">const</span> `Write` ;

/\* Event::$object (Channel) was closed \*/

<span class="modifier">const</span> `Close` ;

/\* Event::$object (Future) was cancelled \*/

<span class="modifier">const</span> `Cancel` ;

/\* Runtime executing Event::$object (Future) was killed \*/

<span class="modifier">const</span> `Kill` ;

/\* Event::$object (Future) raised error \*/

<span class="modifier">const</span> `Error` ;

}

Low Level Synchronization
-------------------------

The <span class="classname">parallel\\Sync</span> class provides access
to low level synchronization primitives, mutex, condition variables, and
allows the implementation of semaphores.

Synchronization for most applications is much better implemented using
channels, however, in some cases authors of low level code may find it
useful to be able to access these lower level mechanisms.

类摘要
------

**parallel\\Sync**

<span class="ooclass"> <span class="modifier">final</span> class
**parallel\\Sync** </span> {

/\* Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">scalar</span> `$value`</span> )

/\* Access \*/

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">get</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="methodname">set</span>
( <span class="methodparam"><span class="type">scalar</span>
`$value`</span> )

/\* Synchronization \*/

<span class="modifier">public</span> <span
class="methodname">wait</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">notify</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$all`</span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_invoke</span> ( <span class="methodparam"><span
class="type">callable</span> `$critical`</span> )

}

parallel\\Sync::\_\_construct
=============================

Construction

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Sync::\_\_construct</span> ( <span
class="methodparam">void</span> )

Shall construct a new synchronization object with no value

<span class="modifier">public</span> <span
class="methodname">parallel\\Sync::\_\_construct</span> ( <span
class="methodparam"><span class="type">scalar</span> `$value`</span> )

Shall construct a new synchronization object containing the given scalar
value

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Sync\\Error\\IllegalValue</span> if `value` is
non-scalar.

parallel\\Sync::get
===================

Access

### 说明

<span class="modifier">public</span> <span class="type">scalar</span>
<span class="methodname">parallel\\Sync::get</span> ( <span
class="methodparam">void</span> )

Shall atomically return the syncrhonization objects value

parallel\\Sync::set
===================

Access

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Sync::set</span> ( <span
class="methodparam"><span class="type">scalar</span> `$value`</span> )

Shall atomically set the value of the synchronization object

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Sync\\Error\\IllegalValue</span> if `value` is
non-scalar.

parallel\\Sync::wait
====================

Synchronization

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Sync::wait</span> ( <span
class="methodparam">void</span> )

Shall wait for notification on this synchronization object

parallel\\Sync::notify
======================

Synchronization

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Sync::notify</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$all`</span> \] )

Shall notify one (by default) or all threads waiting on the
synchronization object

parallel\\Sync::\_\_invoke
==========================

Synchronization

### 说明

<span class="modifier">public</span> <span
class="methodname">parallel\\Sync::\_\_invoke</span> ( <span
class="methodparam"><span class="type">callable</span>
`$critical`</span> )

Shall exclusively enter into the critical code
