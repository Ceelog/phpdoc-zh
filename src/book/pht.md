pht
===

**目录**

-   [简介](/intro/pht.html)
-   [安装／配置](/pht/setup.html)
    -   [需求](/pht/setup.html#需求)
    -   [安装](/pht/setup.html#安装)
    -   [运行时配置](/pht/setup.html#运行时配置)
-   [pht\\Thread](/class/pht-thread.html) — The Thread class
    -   [pht\\Thread::addClassTask](/class/pht-thread.html#pht\Thread::addClassTask)
        — Class threading
    -   [pht\\Thread::addFileTask](/class/pht-thread.html#pht\Thread::addFileTask)
        — File threading
    -   [pht\\Thread::addFunctionTask](/class/pht-thread.html#pht\Thread::addFunctionTask)
        — Function threading
    -   [pht\\Thread::join](/class/pht-thread.html#pht\Thread::join) —
        Joins a thread
    -   [pht\\Thread::start](/class/pht-thread.html#pht\Thread::start) —
        Starts the new thread
    -   [pht\\Thread::taskCount](/class/pht-thread.html#pht\Thread::taskCount)
        — Gets a thread's task count
-   [pht\\Runnable](/class/pht-runnable.html) — The Runnable interface
    -   [pht\\Runnable::run](/class/pht-runnable.html#pht\Runnable::run)
        — The entry point of a threaded class
-   [pht\\HashTable](/class/pht-hashtable.html) — The HashTable class
    -   [pht\\HashTable::lock](/class/pht-hashtable.html#pht\HashTable::lock)
        — Acquires the hash table's mutex lock
    -   [pht\\HashTable::size](/class/pht-hashtable.html#pht\HashTable::size)
        — Gets the size of the hash table
    -   [pht\\HashTable::unlock](/class/pht-hashtable.html#pht\HashTable::unlock)
        — Releases the hash table's mutex lock
-   [pht\\Vector](/class/pht-vector.html) — The Vector class
    -   [pht\\Vector::\_\_construct](/class/pht-vector.html#pht\Vector::__construct)
        — Vector creation
    -   [pht\\Vector::deleteAt](/class/pht-vector.html#pht\Vector::deleteAt)
        — Deletes a value in the vector
    -   [pht\\Vector::insertAt](/class/pht-vector.html#pht\Vector::insertAt)
        — Inserts a value into the vector
    -   [pht\\Vector::lock](/class/pht-vector.html#pht\Vector::lock) —
        Acquires the vector's mutex lock
    -   [pht\\Vector::pop](/class/pht-vector.html#pht\Vector::pop) —
        Pops a value to the vector
    -   [pht\\Vector::push](/class/pht-vector.html#pht\Vector::push) —
        Pushes a value to the vector
    -   [pht\\Vector::resize](/class/pht-vector.html#pht\Vector::resize)
        — Resizes a vector
    -   [pht\\Vector::shift](/class/pht-vector.html#pht\Vector::shift) —
        Shifts a value from the vector
    -   [pht\\Vector::size](/class/pht-vector.html#pht\Vector::size) —
        Gets the size of the vector
    -   [pht\\Vector::unlock](/class/pht-vector.html#pht\Vector::unlock)
        — Releases the vector's mutex lock
    -   [pht\\Vector::unshift](/class/pht-vector.html#pht\Vector::unshift)
        — Unshifts a value to the vector front
    -   [pht\\Vector::updateAt](/class/pht-vector.html#pht\Vector::updateAt)
        — Updates a value in the vector
-   [pht\\Queue](/class/pht-queue.html) — The Queue class
    -   [pht\\Queue::front](/class/pht-queue.html#pht\Queue::front) —
        Returns the first value from a queue
    -   [pht\\Queue::lock](/class/pht-queue.html#pht\Queue::lock) —
        Acquires the queue's mutex lock
    -   [pht\\Queue::pop](/class/pht-queue.html#pht\Queue::pop) — Pops a
        value off of the front of a queue
    -   [pht\\Queue::push](/class/pht-queue.html#pht\Queue::push) —
        Pushes a value to the end of a queue
    -   [pht\\Queue::size](/class/pht-queue.html#pht\Queue::size) — Gets
        the size of the queue
    -   [pht\\Queue::unlock](/class/pht-queue.html#pht\Queue::unlock) —
        Releases the queue's mutex lock
-   [pht\\AtomicInteger](/class/pht-atomicinteger.html) — The
    AtomicInteger class
    -   [pht\\AtomicInteger::\_\_construct](/class/pht-atomicinteger.html#pht\AtomicInteger::__construct)
        — AtomicInteger creation
    -   [pht\\AtomicInteger::dec](/class/pht-atomicinteger.html#pht\AtomicInteger::dec)
        — Decrements the atomic integer's value by one
    -   [pht\\AtomicInteger::get](/class/pht-atomicinteger.html#pht\AtomicInteger::get)
        — Gets the atomic integer's value
    -   [pht\\AtomicInteger::inc](/class/pht-atomicinteger.html#pht\AtomicInteger::inc)
        — Increments the atomic integer's value by one
    -   [pht\\AtomicInteger::lock](/class/pht-atomicinteger.html#pht\AtomicInteger::lock)
        — Acquires the atomic integer's mutex lock
    -   [pht\\AtomicInteger::set](/class/pht-atomicinteger.html#pht\AtomicInteger::set)
        — Sets the atomic integer's value
    -   [pht\\AtomicInteger::unlock](/class/pht-atomicinteger.html#pht\AtomicInteger::unlock)
        — Releases the atomic integer's mutex lock
-   [pht\\Threaded](/class/pht-threaded.html) — The Threaded interface
    -   [pht\\Threaded::lock](/class/pht-threaded.html#pht\Threaded::lock)
        — Acquires the mutex lock
    -   [pht\\Threaded::unlock](/class/pht-threaded.html#pht\Threaded::unlock)
        — Releases the mutex lock

简介
----

The <span class="classname">pht\\Thread</span> class abstracts away a
native thread. It has an internal task queue, where the methods <span
class="methodname">pht\\Thread::addClassTask</span>, <span
class="methodname">pht\\Thread::addFunctionTask</span>, and <span
class="methodname">pht\\Thread::addFileTask</span> push new tasks onto
this queue. Invoking the <span
class="methodname">pht\\Thread::start</span> method will cause the new
thread to be spawned, where it will then begin working through the task
queue. A thread may be reused for any number of tasks.

类摘要
------

**pht\\Thread**

<span class="ooclass"> class **pht\\Thread** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addClassTask</span> ( <span
class="methodparam"><span class="type">string</span> `$className`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...ctorArgs`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFileTask</span> ( <span
class="methodparam"><span class="type">string</span> `$fileName`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...globals`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFunctionTask</span> ( <span
class="methodparam"><span class="type">callable</span> `$func`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...funcArgs`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">join</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">taskCount</span> ( <span
class="methodparam">void</span> )

}

pht\\Thread::addClassTask
=========================

Class threading

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Thread::addClassTask</span> ( <span
class="methodparam"><span class="type">string</span> `$className`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...ctorArgs`</span> \] )

Adds a new class task to a <span class="classname">pht\\Thread</span>s
internal task queue.

### 参数

`className`  
The name of the class to be threaded. This class must implement the
<span class="interfacename">pht\\Runnable</span> interface.

`...ctorArgs`  
An optional list of arguments for the threaded class' constructor. These
arguments will be serialised (since they are being passed to another
thread).

### 返回值

No return value.

### 范例

**示例 \#1 Adding a new class task to a thread**

``` php
<?php

use pht\{Thread, Runnable};

class Task implements Runnable
{
    private $one;

    public function __construct(int $one)
    {
        $this->one = $one;
    }

    public function run()
    {
        var_dump($this->one);
    }
}

$thread = new Thread();

$thread->addClassTask(Task::class, 1);

$thread->start();
$thread->join();
```

以上例程会输出：

    int(1)

pht\\Thread::addFileTask
========================

File threading

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Thread::addFileTask</span> ( <span
class="methodparam"><span class="type">string</span> `$fileName`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...globals`</span> \] )

Adds a new file task to a <span class="classname">pht\\Thread</span>s
internal task queue.

### 参数

`func`  
The name of the file to be threaded.

`...globals`  
An optional list of arguments for the file. These arguments will be
placed into a *$\_THREAD* superglobal, which will be made available
inside of the threaded file. All arguments will be serialised (since
they are being passed to another thread).

### 返回值

No return value.

### 范例

**示例 \#1 Adding a new file task to a thread**

``` php
<?php

use pht\Thread;

$thread = new Thread();

$thread->addFileTask('file.php', 1, 2, 3);

$thread->start();
$thread->join();
```

file.php:

``` php
<?php

[$one, $two, $three] = $_THREAD;

var_dump($one, $two, $three);
```

以上例程会输出：

    int(1)
    int(2)
    int(3)

pht\\Thread::addFunctionTask
============================

Function threading

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Thread::addFunctionTask</span> ( <span
class="methodparam"><span class="type">callable</span> `$func`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$...funcArgs`</span> \] )

Adds a new function task to a <span
class="classname">pht\\Thread</span>s internal task queue.

### 参数

`func`  
The function to be threaded. If it is bound to an instance, then *$this*
will become **`NULL`**.

`...funcArgs`  
An optional list of arguments for the function. These arguments will be
serialised (since they are being passed to another thread).

### 返回值

No return value.

### 范例

**示例 \#1 Adding a new function task to a thread**

``` php
<?php

use pht\Thread;

class Test
{
    public static function run(){var_dump(5);}
    public static function run2(){var_dump(6);}
}

function aFunc(){var_dump(3);}

$thread = new Thread();

$thread->addFunctionTask(static function($one) {var_dump($one);}, 1);
$thread->addFunctionTask(function() {var_dump(2);});
$thread->addFunctionTask('aFunc');
$thread->addFunctionTask('array_map', function ($n) {var_dump($n);}, [4]);
$thread->addFunctionTask(['Test', 'run']);
$thread->addFunctionTask([new Test, 'run2']);

$thread->start();
$thread->join();
```

以上例程会输出：

    int(1)
    int(2)
    int(3)
    int(4)
    int(5)
    int(6)

pht\\Thread::join
=================

Joins a thread

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Thread::join</span> ( <span
class="methodparam">void</span> )

This method will join the spawned thread (though it will first wait for
that thread's internal task queue to finish). As a matter of good
practice, threads should always be joined. Not joining a thread may lead
to undefined behaviour.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Joining a thread**

``` php
<?php

use pht\Thread;

$thread = new Thread();

$thread->start();
$thread->join();
```

pht\\Thread::start
==================

Starts the new thread

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Thread::start</span> ( <span
class="methodparam">void</span> )

This will cause a new thread to be spawned for the associated <span
class="classname">pht\\Thread</span> object, where its internal task
queue will begin to be processed.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Starting a new thread**

``` php
<?php

use pht\Thread;

$thread = new Thread();

$thread->start();
$thread->join();
```

pht\\Thread::taskCount
======================

Gets a thread's task count

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">pht\\Thread::taskCount</span> ( <span
class="methodparam">void</span> )

Retrieves the current task count of a <span
class="classname">pht\\Thread</span>.

### 参数

此函数没有参数。

### 返回值

The number of tasks remaining to be processed.

### 范例

**示例 \#1 Getting the task count of a thread**

``` php
<?php

use pht\Thread;

$thread = new Thread();

$thread->addFunctionTask(function (){});
$thread->addFunctionTask(function (){});
$thread->addFunctionTask(function (){});

var_dump($thread->taskCount());
```

以上例程会输出：

    int(3)

简介
----

The <span class="interfacename">pht\\Runnable</span> interface enforces
the implementation of a run() method on classes that should be threaded.
This method acts as the entry point of the threaded class.

接口摘要
--------

**pht\\Runnable**

<span class="ooclass"> class **pht\\Runnable** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">run</span> ( <span
class="methodparam">void</span> )

}

pht\\Runnable::run
==================

The entry point of a threaded class

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Runnable::run</span> ( <span
class="methodparam">void</span> )

This method acts as the entry point of execution for a threaded class.
It must be defined by all classes that will be threaded.

### 参数

此函数没有参数。

### 返回值

No return value.

简介
----

The <span class="classname">pht\\HashTable</span> class is one of the
Inter-Thread Communication (ITC) data structures exposed by pht. It can
be safely passed around between threads, and manipulated by multiple
threads using the mutex locks that have been packed in with the data
structure. It is reference-counted across threads, and so it does not
need to be explicitly destroyed.

The <span class="classname">pht\\HashTable</span> class enables for
array access upon its objects (along with the <span
class="function">isset</span> and <span class="function">unset</span>
functions). The <span class="classname">ArrayAccess</span> interface is
not explicitly implemented, however, because it is only needed for such
abilities by userland classes.

类摘要
------

**pht\\HashTable**

<span class="ooclass"> class **pht\\HashTable** </span> <span
class="oointerface">implements <span
class="interfacename">pht\\Threaded</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">size</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

}

pht\\HashTable::lock
====================

Acquires the hash table's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\HashTable::lock</span> ( <span
class="methodparam">void</span> )

This method will acquire the mutex lock associated with the hash table.
The mutex lock should always be acquired when manipulating the hash
table if it is being used by multiple threads.

The mutex locks of the Inter-Thread Communication (ITC) data structures
are not reentrant. Attempting to reacquire an already-acquired mutex
lock by the same thread will therefore cause a deadlock.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Locking a hash table's mutex lock**

``` php
<?php

use pht\{Thread, HashTable};

$thread = new Thread();
$hashTable = new HashTable();

$thread->addFunctionTask(function ($hashTable) {
    $hashTable->lock();
    $hashTable['a'] = 1;
    $hashTable->unlock();
}, $hashTable);

$thread->start();

// $hashTable is currently being used by multiple threads
$hashTable->lock();
$hashTable['b'] = 2;
$hashTable->unlock();

$thread->join();
```

pht\\HashTable::size
====================

Gets the size of the hash table

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">pht\\HashTable::size</span> ( <span
class="methodparam">void</span> )

Returns the current size of the hash table. This operation requires a
<span class="classname">pht\\HashTable</span>'s mutex lock to be held if
it is being used by multiple threads.

### 参数

此函数没有参数。

### 返回值

The size of the hash table.

### 范例

**示例 \#1 Getting a hash table's size**

``` php
<?php

use pht\HashTable;

$hashTable = new HashTable();

$hashTable['a'] = 1;
$hashTable['b'] = 2;

var_dump($hashTable->size());
```

以上例程会输出：

    int(2)

pht\\HashTable::unlock
======================

Releases the hash table's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\HashTable::unlock</span> ( <span
class="methodparam">void</span> )

This method will release the mutex lock associated with the hash table.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Locking a hash table's mutex lock**

``` php
<?php

use pht\{Thread, HashTable};

$thread = new Thread();
$hashTable = new HashTable();

$thread->addFunctionTask(function ($hashTable) {
    $hashTable->lock();
    $hashTable['a'] = 1;
    $hashTable->unlock();
}, $hashTable);

$thread->start();

// $hashTable is currently being used by multiple threads
$hashTable->lock();
$hashTable['b'] = 2;
$hashTable->unlock();

$thread->join();
```

简介
----

The <span class="classname">pht\\Vector</span> class is one of the
Inter-Thread Communication (ITC) data structures exposed by pht. It can
be safely passed around between threads, and manipulated by multiple
threads using the mutex locks that have been packed in with the data
structure. It is reference-counted across threads, and so is does not
need to be explicitly destroyed.

The <span class="classname">pht\\Vector</span> class enables for array
access upon its objects (along with the <span
class="function">isset</span> and <span class="function">unset</span>
functions). The <span class="classname">ArrayAccess</span> interface is
not explicitly implemented, however, because it is only needed for such
abilities by userland classes.

类摘要
------

**pht\\Vector**

<span class="ooclass"> class **pht\\Vector** </span> <span
class="oointerface">implements <span
class="interfacename">pht\\Threaded</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">Vector</span>
<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$size`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$value`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">deleteAt</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">insertAt</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resize</span> ( <span class="methodparam"><span
class="type">int</span> `$size`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$value`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">shift</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">size</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unshift</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">updateAt</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

}

pht\\Vector::\_\_construct
==========================

Vector creation

### 说明

<span class="modifier">public</span> <span class="type">Vector</span>
<span class="methodname">pht\\Vector::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$size`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">mixed</span> `$value`<span
class="initializer"> = 0</span></span> \]\] )

Handles the creation of a new vector.

### 参数

`size`  
The size of the vector that will be created.

`value`  
The value to initialise the empty slots in the vector to.

### 返回值

No return value.

### 范例

**示例 \#1 Creating a new vector**

``` php
<?php

use pht\Vector;

$vector1 = new Vector(1);
$vector2 = new Vector(2, 1);

var_dump($vector1, $vector2);
```

以上例程会输出：

    object(pht\Vector)#1 (1) {
      [0]=>
      int(0)
    }
    object(pht\Vector)#2 (2) {
      [0]=>
      int(1)
      [1]=>
      int(1)
    }

pht\\Vector::deleteAt
=====================

Deletes a value in the vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::deleteAt</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

This method deletes a value at the specified offset in the vector (in
linear time).

Since the <span class="classname">pht\\Vector</span> class supports
array access, deleting values can also be performed using the array
subset notation (*\[\]*) in combination with the <span
class="function">unset</span> function.

### 参数

`offset`  
The offset at which the value will be deleted at. This offset must be
within the 0..(N-1) range (inclusive), where N is the size of the
vector. Attempting to delete at offsets outside of this range will
result in an <span class="classname">Error</span> exception.

### 返回值

No return value.

### 范例

**示例 \#1 Deleting values in a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector[] = 1;
$vector[] = 2;
$vector[] = 3;
$vector[] = 4;

$vector->deleteAt(1);
unset($vector[1]);

var_dump($vector);
```

以上例程会输出：

    object(pht\Vector)#1 (2) {
      [0]=>
      int(1)
      [1]=>
      int(4)
    }

pht\\Vector::insertAt
=====================

Inserts a value into the vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::insertAt</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

This method inserts a value at the specified offset into the vector (in
linear time). The vector will automatically be resized if it is not
large enough.

### 参数

`value`  
The value to be inserted into the vector. This value will be serialised
(since it may be passed around between threads).

`offset`  
The offset at which the value will be inserted at. This offset must be
within the 0..N range (inclusive), where N is the size of the vector.
Inserting at position N is the equivalent of using <span
class="methodname">pht\\Vector::push</span>, and inserting at position 0
is the equivalent of using <span
class="methodname">pht\\Vector::unshift</span>. Attempting to insert at
offsets outside of this range will result in an <span
class="classname">Error</span> exception.

### 返回值

No return value.

### 范例

**示例 \#1 Inserting a value into a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector->insertAt(3, 0); // insert 3 at start
$vector->insertAt(1, 0); // insert 1 at start (before 3)
$vector->insertAt(2, 1); // insert 2 in middle (after 1 and before 3)

var_dump($vector);
```

以上例程会输出：

    object(pht\Vector)#1 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

pht\\Vector::lock
=================

Acquires the vector's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::lock</span> ( <span
class="methodparam">void</span> )

This method will acquire the mutex lock associated with the vector. The
mutex lock should always be acquired when manipulating the vector if it
is being used by multiple threads.

The mutex locks of the Inter-Thread Communication (ITC) data structures
are not reentrant. Attempting to reacquire an already-acquired mutex
lock by the same thread will therefore cause a deadlock.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Locking a vector's mutex lock**

``` php
<?php

use pht\{Thread, Vector};

$thread = new Thread();
$vector = new Vector();

$thread->addFunctionTask(function ($vector) {
    $vector->lock();
    $vector[] = 1;
    $vector->unlock();
}, $vector);

$thread->start();

// $vector is currently being used by multiple threads
$vector->lock();
$vector[] = 2;
$vector->unlock();

$thread->join();
```

pht\\Vector::pop
================

Pops a value to the vector

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pht\\Vector::pop</span> ( <span
class="methodparam">void</span> )

This method pops a value from the end of a vector (in constant time).
Popping a value from an empty vector will result in an <span
class="classname">Error</span> exception.

### 参数

此函数没有参数。

### 返回值

The value from the end of the vector.

### 范例

**示例 \#1 Popping a value from a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector->push(1);
$vector[] = 2;

var_dump($vector->pop());
```

以上例程会输出：

    int(2)

pht\\Vector::push
=================

Pushes a value to the vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::push</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

This method pushes a value onto the end of a vector (in constant time).
The vector will automatically be resized if it is not large enough.

Since the <span class="classname">pht\\Vector</span> class supports
array access, new values can also be pushed onto the vector using the
empty subset notation (*\[\]*).

### 参数

`value`  
The value to be pushed onto the end of the vector. This value will be
serialised (since it may be passed around between threads).

### 返回值

No return value.

### 范例

**示例 \#1 Pushing values to a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector->push(1);
$vector[] = 2;

var_dump($vector);
```

以上例程会输出：

    object(pht\Vector)#1 (2) {
      [0]=>
      int(1)
      [1]=>
      int(2)
    }

pht\\Vector::resize
===================

Resizes a vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::resize</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$value`<span
class="initializer"> = 0</span></span> \] )

Resizes the vector. If it is enlarged, then the `value` parameter will
be used to fill in the new slots. If it is made smaller, then the end
values will be truncated.

### 参数

`size`  
The new size of the vector.

`value`  
The value to initialise the empty vector slots to (only used if the
vector is enlarged).

### 返回值

No return value.

### 范例

**示例 \#1 Resizing a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector(1);
var_dump($vector);
$vector->resize(2, 1);
var_dump($vector);
$vector->resize(1, 2); // unused second arg
var_dump($vector);
```

以上例程会输出：

    object(pht\Vector)#1 (1) {
      [0]=>
      int(0)
    }
    object(pht\Vector)#1 (2) {
      [0]=>
      int(0)
      [1]=>
      int(1)
    }
    object(pht\Vector)#1 (1) {
      [0]=>
      int(0)
    }

pht\\Vector::shift
==================

Shifts a value from the vector

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pht\\Vector::shift</span> ( <span
class="methodparam">void</span> )

This method shifts a value from the front of a vector (in linear time).
Shifting a value from an empty vector will result in an <span
class="classname">Error</span> exception.

### 参数

此函数没有参数。

### 返回值

The value from the front of the vector.

### 范例

**示例 \#1 Shifting a value from a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector->push(1);
$vector[] = 2;

var_dump($vector->shift());
```

以上例程会输出：

    int(1)

pht\\Vector::size
=================

Gets the size of the vector

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">pht\\Vector::size</span> ( <span
class="methodparam">void</span> )

Returns the current size of the vector. This operation requires a <span
class="classname">pht\\Vector</span>'s mutex lock to be held if it is
being used by multiple threads.

### 参数

此函数没有参数。

### 返回值

The size of the vector.

### 范例

**示例 \#1 Getting a vector's size**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector[] = 1;
$vector[] = 2;
$vector[] = 3;

var_dump($vector->size());
```

以上例程会输出：

    int(3)

pht\\Vector::unlock
===================

Releases the vector's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::unlock</span> ( <span
class="methodparam">void</span> )

This method will release the mutex lock associated with the vector.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Locking a vector's mutex lock**

``` php
<?php

use pht\{Thread, Vector};

$thread = new Thread();
$vector = new Vector();

$thread->addFunctionTask(function ($vector) {
    $vector->lock();
    $vector[] = 1;
    $vector->unlock();
}, $vector);

$thread->start();

// $vector is currently being used by multiple threads
$vector->lock();
$vector[] = 2;
$vector->unlock();

$thread->join();
```

pht\\Vector::unshift
====================

Unshifts a value to the vector front

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::unshift</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

This method unshifts a value to the front of a vector (in linear time).
The vector will automatically be resized if it is not large enough.

### 参数

`value`  
The value to be pushed onto the beginning of the vector. This value will
be serialised (since it may be passed around between threads).

### 返回值

No return value.

### 范例

**示例 \#1 Unshifting a value to the front of a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

for ($i = 0; $i < 3; ++$i) {
    $vector->unshift($i); // causes a quadratic runtime, beware
}

var_dump($vector);
```

以上例程会输出：

    object(pht\Vector)#1 (3) {
      [0]=>
      int(2)
      [1]=>
      int(1)
      [2]=>
      int(0)
    }

pht\\Vector::updateAt
=====================

Updates a value in the vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Vector::updateAt</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

This method updates a value at the specified offset in the vector (in
linear time). The vector will automatically be resized if it is not
large enough.

Since the <span class="classname">pht\\Vector</span> class supports
array access, updating values can also be performed using the array
subset notation (*\[\]*).

### 参数

`value`  
The value to be inserted into the vector. This value will be serialised
(since it may be passed around between threads).

`offset`  
The offset at which the value will be updated at. This offset must be
within the 0..(N-1) range (inclusive), where N is the size of the
vector. Attempting to update at offsets outside of this range will
result in an <span class="classname">Error</span> exception.

### 返回值

No return value.

### 范例

**示例 \#1 Updating a value in a vector**

``` php
<?php

use pht\Vector;

$vector = new Vector();

$vector[] = 1;
$vector[] = 2;

$vector->updateAt(3, 0);
$vector[1] = 4;

var_dump($vector);
```

以上例程会输出：

    object(pht\Vector)#1 (2) {
      [0]=>
      int(3)
      [1]=>
      int(4)
    }

简介
----

The <span class="classname">pht\\Queue</span> class is one of the
Inter-Thread Communication (ITC) data structures exposed by pht. It can
be safely passed around between threads, and manipulated by multiple
threads using the mutex locks that have been packed in with the data
structure. It is reference-counted across threads, and so it does not
need to be explicitly destroyed.

类摘要
------

**pht\\Queue**

<span class="ooclass"> class **pht\\Queue** </span> <span
class="oointerface">implements <span
class="interfacename">pht\\Threaded</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">front</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">size</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

}

pht\\Queue::front
=================

Returns the first value from a queue

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pht\\Queue::front</span> ( <span
class="methodparam">void</span> )

This method will remove a value from the front of the queue (in constant
time). Attempting to return the front value from an empty queue will
result in an <span class="classname">Error</span> exception.

**Caution**

Due to the fact that all values in a <span
class="classname">pht\\Queue</span> are serialised, extracting a value
from the queue will require it to be deserialised. This can incur a
noticeable performance hit if the inspection of the queue's front value
is performed within a loop.

### 参数

此函数没有参数。

### 返回值

The value on the front of the queue.

### 范例

**示例 \#1 Retrieving the front value of a queue**

``` php
<?php

use pht\Queue;

$queue = new Queue();

$queue->push(1);

var_dump($queue->front());
```

以上例程会输出：

    int(1)

**示例 \#2 Retrieving the front value in a loop (bad example - don't do
this)**

``` php
<?php

use pht\Queue;

$queue = new Queue();

$queue->push(array_fill(0, 2000, 0));

for ($i = 0; $i < count($queue->front()); ++$i); // quadratic runtime
```

**示例 \#3 Retrieving the front value in a loop (good example)**

``` php
<?php

use pht\Queue;

$queue = new Queue();

$queue->push(array_fill(0, 2000, 0));

$front = $queue->front(); // create a separate variable
for ($i = 0; $i < count($front); ++$i); // linear runtime
```

pht\\Queue::lock
================

Acquires the queue's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Queue::lock</span> ( <span
class="methodparam">void</span> )

This method will acquire the mutex lock associated with the queue. The
mutex lock should always be acquired when manipulating the queue if it
is being used by multiple threads.

The mutex locks of the Inter-Thread Communication (ITC) data structures
are not reentrant. Attempting to reacquire an already-acquired mutex
lock by the same thread will therefore cause a deadlock.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Locking a queue's mutex lock**

``` php
<?php

use pht\{Thread, Queue};

$thread = new Thread();
$queue = new Queue();

$thread->addFunctionTask(function ($queue) {
    $queue->lock();
    $queue->push(1);
    $queue->unlock();
}, $queue);

$thread->start();

// $queue is currently being used by multiple threads
$queue->lock();
$queue->push(1);
$queue->unlock();

$thread->join();

// $queue is only being used in this thread now, so no need to lock it
while ($queue->size()) {
    var_dump($queue->pop());
}
```

以上例程会输出：

    int(1)
    int(1)

pht\\Queue::pop
===============

Pops a value off of the front of a queue

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pht\\Queue::pop</span> ( <span
class="methodparam">void</span> )

This method will remove a value from the front of the queue (in constant
time). Attempting to pop a value from an empty queue will result in an
<span class="classname">Error</span> exception.

### 参数

此函数没有参数。

### 返回值

The value removed from the queue.

### 范例

**示例 \#1 Popping a value from a queue**

``` php
<?php

use pht\Queue;

$queue = new Queue();

$queue->push(1);

var_dump($queue->pop());
```

以上例程会输出：

    int(1)

pht\\Queue::push
================

Pushes a value to the end of a queue

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Queue::push</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

This method will add a value onto the queue.

### 参数

`value`  
The value to be added to a <span class="classname">pht\\Queue</span>.
This value will be serialised (since it may be passed around between
threads).

### 返回值

No return value.

### 范例

**示例 \#1 Pushing a value to a queue**

``` php
<?php

use pht\Queue;

$queue = new Queue();

$queue->push(1);

var_dump($queue);
```

以上例程会输出：

    object(pht\Queue)#1 (1) {
      [0]=>
      int(1)
    }

pht\\Queue::size
================

Gets the size of the queue

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">pht\\Queue::size</span> ( <span
class="methodparam">void</span> )

Returns the current size of the queue. This operation requires a <span
class="classname">pht\\Queue</span>'s mutex lock to be held if it is
being used by multiple threads.

### 参数

此函数没有参数。

### 返回值

The size of the queue.

### 范例

**示例 \#1 Getting a queue's size**

``` php
<?php

use pht\Queue;

$queue = new Queue();

$queue->push(1);
$queue->push(1);

var_dump($queue->size());
```

以上例程会输出：

    int(2)

pht\\Queue::unlock
==================

Releases the queue's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Queue::unlock</span> ( <span
class="methodparam">void</span> )

This method will release the mutex lock associated with the queue.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Locking a queue's mutex lock**

``` php
<?php

use pht\{Thread, Queue};

$thread = new Thread();
$queue = new Queue();

$thread->addFunctionTask(function ($queue) {
    $queue->lock();
    $queue->push(1);
    $queue->unlock();
}, $queue);

$thread->start();

// $queue is currently being used by multiple threads
$queue->lock();
$queue->push(1);
$queue->unlock();

$thread->join();

// $queue is only being used in this thread now, so no need to lock it
while ($queue->size()) {
    var_dump($queue->pop());
}
```

以上例程会输出：

    int(1)
    int(1)

简介
----

The <span class="classname">pht\\AtomicInteger</span> class is currently
the only supported atomic value. It allows for an integer to be safely
passed around between, and manipulated, by multiple threads. The methods
exposed by this class do not need mutex locking, since they will acquire
the internal mutex lock implicitly. <span
class="methodname">pht\\AtomicInteger::lock</span> and <span
class="methodname">pht\\AtomicInteger::unlock</span> are still exposed,
however, for when multiple operations involving the same <span
class="classname">pht\\AtomicInteger</span> object need to be grouped
together.

The mutex locks of the atomic values are reentrant safe.

类摘要
------

**pht\\AtomicInteger**

<span class="ooclass"> class **pht\\AtomicInteger** </span> <span
class="oointerface">implements <span
class="interfacename">pht\\Threaded</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">AtomicInteger</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$value`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dec</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">get</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">inc</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

}

pht\\AtomicInteger::\_\_construct
=================================

AtomicInteger creation

### 说明

<span class="modifier">public</span> <span
class="type">AtomicInteger</span> <span
class="methodname">pht\\AtomicInteger::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$value`<span
class="initializer"> = 0</span></span> \] )

Handles the creation of a new atomic integer.

### 参数

`value`  
The value to initialise the atomic integer to.

### 返回值

No return value.

### 范例

**示例 \#1 Creating a new atomic integer**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger(100);

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(100)

pht\\AtomicInteger::dec
=======================

Decrements the atomic integer's value by one

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\AtomicInteger::dec</span> ( <span
class="methodparam">void</span> )

This method will decrement the atomic integer's value by one.
Internally, the mutex lock of the atomic integer will be acquired, and
so there is no need to manually acquire it (unless this operation needs
to be grouped with other operations on the same atomic integer - see the
example in <span class="methodname">pht\\AtomicInteger::lock</span> for
a demonstration of this).

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Decrementing an atomic integer's value**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger();

$atomicInteger->dec();
$atomicInteger->dec();

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(-2)

pht\\AtomicInteger::get
=======================

Gets the atomic integer's value

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">pht\\AtomicInteger::get</span> ( <span
class="methodparam">void</span> )

This method will fetch the current value of the atomic integer.
Internally, the mutex lock of the atomic integer will be acquired, and
so there is no need to manually acquire it (unless this operation needs
to be grouped with other operations on the same atomic integer - see the
example in <span class="methodname">pht\\AtomicInteger::lock</span> for
a demonstration of this).

### 参数

此函数没有参数。

### 返回值

The current integer value of the atomic integer.

### 范例

**示例 \#1 Getting an atomic integer's value**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger(2);

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(2)

pht\\AtomicInteger::inc
=======================

Increments the atomic integer's value by one

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\AtomicInteger::inc</span> ( <span
class="methodparam">void</span> )

This method will increment the atomic integer's value by one.
Internally, the mutex lock of the atomic integer will be acquired, and
so there is no need to manually acquire it (unless this operation needs
to be grouped with other operations on the same atomic integer - see the
example in <span class="methodname">pht\\AtomicInteger::lock</span> for
a demonstration of this).

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Incrementing an atomic integer's value**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger();

$atomicInteger->inc();
$atomicInteger->inc();

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(2)

pht\\AtomicInteger::lock
========================

Acquires the atomic integer's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\AtomicInteger::lock</span> ( <span
class="methodparam">void</span> )

This method will acquire the mutex lock associated with the atomic
integer. The mutex lock only needs to be acquired when needing to group
together multiple operations.

The mutex locks of the atomic values are reentrant safe. It is therefore
valid for the same thread to reacquire a mutex lock that it has already
acquired.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Grouping together an atomic integer's operations (requiring a
mutex lock)**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger(2);

// assumes $atomicInteger is being used by multiple threads
$atomicInteger->lock();
$atomicInteger->set($atomicInteger->get() * 2); // double the value
$atomicInteger->unlock();

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(4)

pht\\AtomicInteger::set
=======================

Sets the atomic integer's value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\AtomicInteger::set</span> ( <span
class="methodparam"><span class="type">int</span> `$value`</span> )

This method will set the value of the atomic integer. Internally, the
mutex lock of the atomic integer will be acquired, and so there is no
need to manually acquire it (unless this operation needs to be grouped
with other operations on the same atomic integer - see the example in
<span class="methodname">pht\\AtomicInteger::lock</span> for a
demonstration of this).

### 参数

`value`  
The value to set the atomic integer to.

### 返回值

No return value.

### 范例

**示例 \#1 Setting an atomic integer's value**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger();

$atomicInteger->set(20);

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(20)

pht\\AtomicInteger::unlock
==========================

Releases the atomic integer's mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\AtomicInteger::unlock</span> ( <span
class="methodparam">void</span> )

This method will release the mutex lock associated with the atomic
integer.

### 参数

此函数没有参数。

### 返回值

No return value.

### 范例

**示例 \#1 Grouping together an atomic integer's operations (requiring a
mutex lock)**

``` php
<?php

use pht\AtomicInteger;

$atomicInteger = new AtomicInteger(2);

// assumes $atomicInteger is being used by multiple threads
$atomicInteger->lock();
$atomicInteger->set($atomicInteger->get() * 2); // double the value
$atomicInteger->unlock();

var_dump($atomicInteger->get());
```

以上例程会输出：

    int(4)

简介
----

The <span class="interfacename">pht\\Threaded</span> interface is an
internal interface used by the Inter-Thread Communication (ITC) data
structures (<span class="classname">pht\\HashTable</span>, <span
class="classname">pht\\Queue</span>, and <span
class="classname">pht\\Vector</span>). It allows those data structures
to be threaded and ensures that the mutex locking API ( <span
class="methodname">pht\\Threaded::lock</span> and <span
class="methodname">pht\\Threaded::unlock</span>) is implemented by each
of the ITC data structures. It is not implementable by userland classes
(since standalone mutex locks are not exposed).

接口摘要
--------

**pht\\Threaded**

<span class="ooclass"> class **pht\\Threaded** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

}

pht\\Threaded::lock
===================

Acquires the mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Threaded::lock</span> ( <span
class="methodparam">void</span> )

This method will acquire the mutex lock associated with the given class
(either a <span class="classname">pht\\HashTable</span>, <span
class="classname">pht\\Queue</span>, <span
class="classname">pht\\Vector</span>, or <span
class="classname">pht\\AtomicInteger</span>).

### 参数

此函数没有参数。

### 返回值

No return value.

pht\\Threaded::unlock
=====================

Releases the mutex lock

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pht\\Threaded::unlock</span> ( <span
class="methodparam">void</span> )

This method will unlock the mutex lock associated with the given class
(either a <span class="classname">pht\\HashTable</span>, <span
class="classname">pht\\Queue</span>, <span
class="classname">pht\\Vector</span>, or <span
class="classname">pht\\AtomicInteger</span>).

### 参数

此函数没有参数。

### 返回值

No return value.
