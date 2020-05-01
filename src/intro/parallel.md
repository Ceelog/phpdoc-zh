parallel is a parallel concurrency extension for PHP 7.2+.

A brief description of the concepts core to parallel follows, more
detailed information may be found within this section of the manual.

A <span class="classname">parallel\\Runtime</span> represents a PHP
interpreter thread. A <span class="classname">parallel\\Runtime</span>
is configured with an optional bootstrap file passed to <span
class="methodname">parallel\\Runtime::\_\_construct</span>, this is
typically an autoloader, or some other preloading routine: The bootstrap
file will be included before any task is executed.

After construction the <span class="classname">parallel\\Runtime</span>
remains available until it is closed, killed, or destroyed by the normal
scoping rules of PHP objects. <span
class="methodname">parallel\\Runtime::run</span> allows the programmer
to schedule tasks for execution in parallel. A <span
class="classname">parallel\\Runtime</span> has a FIFO schedule, tasks
will be executed in the order that they are scheduled.

parallel implements a functional, higher level API on top of <span
class="classname">parallel\\Runtime</span> that provides a single
function entry point to executing parallel code with automatic
scheduling: <span class="function">parallel\\run</span>.

A task is simply a <span class="classname">Closure</span> intended for
parallel execution. The <span class="classname">Closure</span> may
contain almost any instruction, including nested closures. However,
there are some instructions that are prohibited in tasks:

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

The <span class="classname">parallel\\Future</span> is used to access
the return value from the task, and exposes an API for cancellation of
the task.

A task may be scheduled with arguments, use lexical scope variables
(by-value), and return a value (via a <span
class="classname">parallel\\Future</span>), but these only allow
uni-directional communication: They allow the programmer to send data
into and retrieve data from a task, but do not allow bi-directional
communication between tasks. The <span
class="classname">parallel\\Channel</span> API allows bi-directional
communication between tasks, a <span
class="classname">parallel\\Channel</span> is a socket-like link between
tasks that the programmer can use to send and receive data.

The <span class="classname">parallel\\Events</span> API implements a
native feel (<span class="classname">Traversable</span>) event loop, and
<span class="methodname">parallel\\Events::poll</span> method. It allows
the programmer to work with sets of channels and or futures. The
programmer simply adds channels and futures to the event loop,
optionally setting the input for writes with <span
class="methodname">parallel\\Events::setInput</span>, and enters into a
foreach: parallel will read from and write to objects as they become
available yielding <span
class="classname">parallel\\Events\\Event</span> objects describing the
operations that have occurred.

-   <a href="/philosophy/parallel.html" class="xref">Philosophy</a>
