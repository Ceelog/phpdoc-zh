The <span class="classname">parallel\\Runtime</span> API provides a
great degree of control to the power PHP programmer, and those
intimately familiar with writing applications that use parallel
concurrency.

The functional API provides less control in exchange for the ability to
make decisions for the programmer:

-   all executing runtimes are bootstrapped identically

-   scheduling is determined by the API, not the programmer

<span class="function">parallel\\run</span> provides the guarantee that
the task will begin to execute in parallel as soon as allowed by
hardware and operating system constraints, without needlessly creating
runtimes. For most applications the functional API should be preferred.

parallel\\bootstrap
===================

Bootstrapping

### 说明

<span class="type">void</span> <span
class="methodname">parallel\\bootstrap</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

Shall use the provided `file` to bootstrap all runtimes created for
automatic scheduling via <span class="function">parallel\\run</span>.

### Exceptions

**Warning**

Shall throw <span
class="type">parallel\\Runtime\\Error\\Bootstrap</span> if previously
called for this process.

**Warning**

Shall throw <span
class="type">parallel\\Runtime\\Error\\Bootstrap</span> if called after
<span class="function">parallel\\run</span>.

### 参见

-   <a href="/class/parallel-runtime.html#parallel\Runtime::run" class="xref"></a>

parallel\\run
=============

Execution

### 说明

<span class="type">?Future</span> <span
class="methodname">parallel\\run</span> ( <span
class="methodparam"><span class="type">Closure</span> `$task`</span> )

Shall schedule `task` for execution in parallel.

<span class="type">?Future</span> <span
class="methodname">parallel\\run</span> ( <span
class="methodparam"><span class="type">Closure</span> `$task`</span> ,
<span class="methodparam"><span class="type">array</span> `$argv`</span>
)

Shall schedule `task` for execution in parallel, passing `argv` at
execution time.

### Automatic Scheduling

If a <span class="classname">\\parallel\\Runtime</span> internally
created and cached by a previous call to <span
class="function">parallel\\run</span> is idle, it will be used to
execute the task. If no <span
class="classname">\\parallel\\Runtime</span> is idle parallel will
create and cache a <span class="classname">\\parallel\\Runtime</span>.

> **Note**:
>
> <span class="classname">\\parallel\\Runtime</span> objects created by
> the programmer are not used for automatic scheduling.

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

### 参见

-   <a href="/class/parallel-runtime.html#parallel\Runtime::run" class="xref"></a>

**目录**

-   [parallel\\bootstrap](/functional/parallel.html#parallel\bootstrap)
    — Bootstrapping
-   [parallel\\run](/functional/parallel.html#parallel\run) — Execution
