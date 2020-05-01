pht is a new threading extension for PHP. It enables for classes,
functions, and even entire files to be threaded. Currently, pht can only
be used with PHP 7.2. This is due to ZTS mode being unsafe in PHP 7.0
and 7.1. Support for PHP \>7.2 is coming soon.

**Warning**

The pht extension should not be used in a web server environment.
Threading should be restricted to CLI-based applications only.

The approach to threading that pht takes is to abstract away the thread
itself behind a dedicated object (<span
class="classname">pht\\Thread</span>). Tasks are then added to the
thread's internal task queue, where they are processed when the thread
is started (via <span class="methodname">pht\\Thread::start</span>).

All thread tasks will execute in isolation inside of the newly spawned
thread. For class tasks, this means the spawned objects cannot be passed
around between threads. By keeping the threading contexts completely
separate from one-another, there becomes no need to serialise the
properties of threaded objects (which is a necessary evil if such
objects have to operate in multiple threads).

The isolation of threading contexts makes the passing around of data
between them somewhat problematic. To solve this problem, threadable
data structures (<span class="classname">pht\\HashTable</span>, <span
class="classname">pht\\Vector</span>, and <span
class="classname">pht\\Queue</span>) have been implemented to allow for
a two-way communication style between threads, where they expose mutex
locks to control their integrity. These data structures can be safely
passed around between threads, and manipulated by multiple threads using
the mutex locks that have been packed in with them. They are
reference-counted across threads, and so they do not need to be
explicitly destroyed. This approach to threading means that only the
given built-in data structures need to be safely passed around between
threads.

Atomic values are also supported by pht. Currently, only an <span
class="classname">pht\\AtomicInteger</span> class exists. Like the
threaded data structures, it too can safely be passed around between
threads.
