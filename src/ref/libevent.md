event\_add
==========

Add an event to the set of monitored events

### 说明

<span class="type">bool</span> <span
class="methodname">event\_add</span> ( <span class="methodparam"><span
class="type">resource</span> `$event`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = -1</span></span> \] )

<span class="function">event\_add</span> schedules the execution of the
`event` when the event specified in <span
class="function">event\_set</span> occurs or in at least the time
specified by the `timeout` argument. If `timeout` was not specified, not
timeout is set. The `event` must be already initalized by <span
class="function">event\_set</span> and <span
class="function">event\_base\_set</span> functions. If the `event`
already has a timeout set, it is replaced by the new one.

### 参数

`event`  
Valid event resource.

`timeout`  
Optional timeout (in microseconds).

### 返回值

<span class="function">event\_add</span> returns **`TRUE`** on success
or **`FALSE`** on error.

event\_base\_free
=================

Destroy event base

### 说明

<span class="type">void</span> <span
class="methodname">event\_base\_free</span> ( <span
class="methodparam"><span class="type">resource</span>
`$event_base`</span> )

Destroys the specified `event_base` and frees all the resources
associated. Note that it's not possible to destroy an event base with
events attached to it.

### 参数

`event_base`  
Valid event base resource.

event\_base\_loop
=================

Handle events

### 说明

<span class="type">int</span> <span
class="methodname">event\_base\_loop</span> ( <span
class="methodparam"><span class="type">resource</span>
`$event_base`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \] )

Starts event loop for the specified event base.

### 参数

`event_base`  
Valid event base resource.

`flags`  
Optional parameter, which can take any combination of **`EVLOOP_ONCE`**
and **`EVLOOP_NONBLOCK`**.

### 返回值

<span class="function">event\_base\_loop</span> returns 0 on success, -1
on error and 1 if no events were registered.

event\_base\_loopbreak
======================

Abort event loop

### 说明

<span class="type">bool</span> <span
class="methodname">event\_base\_loopbreak</span> ( <span
class="methodparam"><span class="type">resource</span>
`$event_base`</span> )

Abort the active event loop immediately. The behaviour is similar to
*break* statement.

### 参数

`event_base`  
Valid event base resource.

### 返回值

<span class="function">event\_base\_loopbreak</span> returns **`TRUE`**
on success or **`FALSE`** on error.

event\_base\_loopexit
=====================

Exit loop after a time

### 说明

<span class="type">bool</span> <span
class="methodname">event\_base\_loopexit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$event_base`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
-1</span></span> \] )

The next event loop iteration after the given timer expires will
complete normally, then exit without blocking for events again.

### 参数

`event_base`  
Valid event base resource.

`timeout`  
Optional timeout parameter (in microseconds).

### 返回值

<span class="function">event\_base\_loopexit</span> returns **`TRUE`**
on success or **`FALSE`** on error.

event\_base\_new
================

Create and initialize new event base

### 说明

<span class="type">resource</span> <span
class="methodname">event\_base\_new</span> ( <span
class="methodparam">void</span> )

Returns new event base, which can be used later in <span
class="function">event\_base\_set</span>, <span
class="function">event\_base\_loop</span> and other functions.

### 参数

此函数没有参数。

### 返回值

<span class="function">event\_base\_new</span> returns valid event base
resource on success or **`FALSE`** on error.

event\_base\_priority\_init
===========================

Set the number of event priority levels

### 说明

<span class="type">bool</span> <span
class="methodname">event\_base\_priority\_init</span> ( <span
class="methodparam"><span class="type">resource</span>
`$event_base`</span> , <span class="methodparam"><span
class="type">int</span> `$npriorities`</span> )

Sets the number of different event priority levels.

By default all events are scheduled with the same priority
(`npriorities`/2). Using <span
class="function">event\_base\_priority\_init</span> you can change the
number of event priority levels and then set a desired priority for each
event.

### 参数

`event_base`  
Valid event base resource.

`npriorities`  
The number of event priority levels.

### 返回值

<span class="function">event\_base\_priority\_init</span> returns
**`TRUE`** on success or **`FALSE`** on error.

event\_base\_reinit
===================

Reinitialize the event base after a fork

### 说明

<span class="type">bool</span> <span
class="methodname">event\_base\_reinit</span> ( <span
class="methodparam"><span class="type">resource</span>
`$event_base`</span> )

Some event mechanisms do not survive across fork. The `event_base` needs
to be reinitialized with this function.

### 参数

`event_base`  
Valid event base resource that needs to be re-initialized.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

event\_base\_set
================

Associate event base with an event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_base\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$event`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$event_base`</span> )

Associates the `event_base` with the `event`.

### 参数

`event`  
Valid event resource.

`event_base`  
Valid event base resource.

### 返回值

<span class="function">event\_base\_set</span> returns **`TRUE`** on
success or **`FALSE`** on error.

event\_buffer\_base\_set
========================

Associate buffered event with an event base

### 说明

<span class="type">bool</span> <span
class="methodname">event\_buffer\_base\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">resource</span>
`$event_base`</span> )

Assign the specified `bevent` to the `event_base`.

### 参数

`bevent`  
Valid buffered event resource.

`event_base`  
Valid event base resource.

### 返回值

<span class="function">event\_buffer\_base\_set</span> returns
**`TRUE`** on success or **`FALSE`** on error.

event\_buffer\_disable
======================

Disable a buffered event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_buffer\_disable</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">int</span>
`$events`</span> )

Disables the specified buffered event.

### 参数

`bevent`  
Valid buffered event resource.

`events`  
Any combination of **`EV_READ`** and **`EV_WRITE`**.

### 返回值

<span class="function">event\_buffer\_disable</span> returns **`TRUE`**
on success or **`FALSE`** on error.

event\_buffer\_enable
=====================

Enable a buffered event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_buffer\_enable</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">int</span>
`$events`</span> )

Enables the specified buffered event.

### 参数

`bevent`  
Valid buffered event resource.

`events`  
Any combination of **`EV_READ`** and **`EV_WRITE`**.

### 返回值

<span class="function">event\_buffer\_enable</span> returns **`TRUE`**
on success or **`FALSE`** on error.

event\_buffer\_fd\_set
======================

Change a buffered event file descriptor

### 说明

<span class="type">void</span> <span
class="methodname">event\_buffer\_fd\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">resource</span>
`$fd`</span> )

Changes the file descriptor on which the buffered event operates.

### 参数

`bevent`  
Valid buffered event resource.

`fd`  
Valid PHP stream, must be castable to file descriptor.

event\_buffer\_free
===================

Destroy buffered event

### 说明

<span class="type">void</span> <span
class="methodname">event\_buffer\_free</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
)

Destroys the specified buffered event and frees all the resources
associated.

### 参数

`bevent`  
Valid buffered event resource.

event\_buffer\_new
==================

Create new buffered event

### 说明

<span class="type">resource</span> <span
class="methodname">event\_buffer\_new</span> ( <span
class="methodparam"><span class="type">resource</span> `$stream`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$readcb`</span> , <span class="methodparam"><span
class="type">mixed</span> `$writecb`</span> , <span
class="methodparam"><span class="type">mixed</span> `$errorcb`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$arg`</span> \] )

Libevent provides an abstraction layer on top of the regular event API.
Using buffered event you don't need to deal with the I/O manually,
instead it provides input and output buffers that get filled and drained
automatically.

### 参数

`stream`  
Valid PHP stream resource. Must be castable to file descriptor.

`readcb`  
Callback to invoke where there is data to read, or <span
class="type">NULL</span> if no callback is desired.

`writecb`  
Callback to invoke where the descriptor is ready for writing, or <span
class="type">NULL</span> if no callback is desired.

`errorcb`  
Callback to invoke where there is an error on the descriptor, cannot be
<span class="type">NULL</span>.

`arg`  
An argument that will be passed to each of the callbacks (optional).

### 返回值

<span class="function">event\_buffer\_new</span> returns new buffered
event resource on success or **`FALSE`** on error.

event\_buffer\_priority\_set
============================

Assign a priority to a buffered event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_buffer\_priority\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">int</span>
`$priority`</span> )

Assign a priority to the `bevent`.

### 参数

`bevent`  
Valid buffered event resource.

`priority`  
Priority level. Cannot be less than zero and cannot exceed maximum
priority level of the event base (see <span
class="function">event\_base\_priority\_init</span>).

### 返回值

<span class="function">event\_buffer\_priority\_set</span> returns
**`TRUE`** on success or **`FALSE`** on error.

event\_buffer\_read
===================

Read data from a buffered event

### 说明

<span class="type">string</span> <span
class="methodname">event\_buffer\_read</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">int</span>
`$data_size`</span> )

Reads data from the input buffer of the buffered event.

### 参数

`bevent`  
Valid buffered event resource.

`data_size`  
Data size in bytes.

event\_buffer\_set\_callback
============================

Set or reset callbacks for a buffered event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_buffer\_set\_callback</span> ( <span
class="methodparam"><span class="type">resource</span> `$event`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$readcb`</span> , <span class="methodparam"><span
class="type">mixed</span> `$writecb`</span> , <span
class="methodparam"><span class="type">mixed</span> `$errorcb`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$arg`</span> \] )

Sets or changes existing callbacks for the buffered `event`.

### 参数

`event`  
Valid buffered event resource.

`readcb`  
Callback to invoke where there is data to read, or <span
class="type">NULL</span> if no callback is desired.

`writecb`  
Callback to invoke where the descriptor is ready for writing, or <span
class="type">NULL</span> if no callback is desired.

`errorcb`  
Callback to invoke where there is an error on the descriptor, cannot be
<span class="type">NULL</span>.

`arg`  
An argument that will be passed to each of the callbacks (optional).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

event\_buffer\_timeout\_set
===========================

Set read and write timeouts for a buffered event

### 说明

<span class="type">void</span> <span
class="methodname">event\_buffer\_timeout\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">int</span>
`$read_timeout`</span> , <span class="methodparam"><span
class="type">int</span> `$write_timeout`</span> )

Sets the read and write timeouts for the specified buffered event.

### 参数

`bevent`  
Valid buffered event resource.

`read_timeout`  
Read timeout (in seconds).

`write_timeout`  
Write timeout (in seconds).

event\_buffer\_watermark\_set
=============================

Set the watermarks for read and write events

### 说明

<span class="type">void</span> <span
class="methodname">event\_buffer\_watermark\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">int</span>
`$events`</span> , <span class="methodparam"><span
class="type">int</span> `$lowmark`</span> , <span
class="methodparam"><span class="type">int</span> `$highmark`</span> )

Sets the watermarks for read and write events. Libevent does not invoke
read callback unless there is at least `lowmark` bytes in the input
buffer; if the read buffer is beyond the `highmark`, reading is stopped.
On output, the write callback is invoked whenever the buffered data
falls below the `lowmark`.

### 参数

`bevent`  
Valid buffered event resource.

`events`  
Any combination of **`EV_READ`** and **`EV_WRITE`**.

`lowmark`  
Low watermark.

`highmark`  
High watermark.

event\_buffer\_write
====================

Write data to a buffered event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_buffer\_write</span> ( <span
class="methodparam"><span class="type">resource</span> `$bevent`</span>
, <span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">int</span> `$data_size`<span class="initializer"> =
-1</span></span> \] )

Writes data to the specified buffered event. The data is appended to the
output buffer and written to the descriptor when it becomes available
for writing.

### 参数

`bevent`  
Valid buffered event resource.

`data`  
The data to be written.

`data_size`  
Optional size parameter. <span
class="function">event\_buffer\_write</span> writes all the `data` by
default.

### 返回值

<span class="function">event\_buffer\_write</span> returns **`TRUE`** on
success or **`FALSE`** on error.

event\_del
==========

Remove an event from the set of monitored events

### 说明

<span class="type">bool</span> <span
class="methodname">event\_del</span> ( <span class="methodparam"><span
class="type">resource</span> `$event`</span> )

Cancels the `event`.

### 参数

`event`  
Valid event resource.

### 返回值

<span class="function">event\_del</span> returns **`TRUE`** on success
or **`FALSE`** on error.

event\_free
===========

Free event resource

### 说明

<span class="type">void</span> <span
class="methodname">event\_free</span> ( <span class="methodparam"><span
class="type">resource</span> `$event`</span> )

Frees previously created event resource.

### 参数

`event`  
Valid event resource.

event\_new
==========

Create new event

### 说明

<span class="type">resource</span> <span
class="methodname">event\_new</span> ( <span
class="methodparam">void</span> )

Creates and returns a new event resource.

### 返回值

<span class="function">event\_new</span> returns a new event resource on
success or **`FALSE`** on error.

event\_priority\_set
====================

Assign a priority to an event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_priority\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$event`</span> ,
<span class="methodparam"><span class="type">int</span>
`$priority`</span> )

Assign a priority to the `event`.

### 参数

`event`  
Valid event resource.

`priority`  
Priority level. Cannot be less than zero and cannot exceed maximum
priority level of the event base (see <span
class="function">event\_base\_priority\_init</span>).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

event\_set
==========

Prepare an event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_set</span> ( <span class="methodparam"><span
class="type">resource</span> `$event`</span> , <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$events`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$arg`</span> \] )

Prepares the event to be used in <span
class="function">event\_add</span>. The event is prepared to call the
function specified by the `callback` on the events specified in
parameter `events`, which is a set of the following flags:
**`EV_TIMEOUT`**, **`EV_SIGNAL`**, **`EV_READ`**, **`EV_WRITE`** and
**`EV_PERSIST`**.

If **`EV_SIGNAL`** bit is set in parameter `events`, the `fd` is
interpreted as signal number.

After initializing the event, use <span
class="function">event\_base\_set</span> to associate the event with its
event base.

In case of matching event, these three arguments are passed to the
`callback` function:

`fd`  
Signal number or resource indicating the stream.

`events`  
A flag indicating the event. Consists of the following flags:
**`EV_TIMEOUT`**, **`EV_SIGNAL`**, **`EV_READ`**, **`EV_WRITE`** and
**`EV_PERSIST`**.

`arg`  
Optional parameter, previously passed to <span
class="function">event\_set</span> as `arg`.

### 参数

`event`  
Valid event resource.

`fd`  
Valid PHP stream resource. The stream must be castable to file
descriptor, so you most likely won't be able to use any of filtered
streams.

`events`  
A set of flags indicating the desired event, can be **`EV_READ`** and/or
**`EV_WRITE`**. The additional flag **`EV_PERSIST`** makes the event to
persist until <span class="function">event\_del</span> is called,
otherwise the callback is invoked only once.

`callback`  
Callback function to be called when the matching event occurs.

`arg`  
Optional callback parameter.

### 返回值

<span class="function">event\_set</span> returns **`TRUE`** on success
or **`FALSE`** on error.

### 更新日志

| 版本  | 说明                               |
|-------|------------------------------------|
| 0.0.4 | **`EV_SIGNAL`** support was added. |

event\_timer\_add
=================

别名 <span class="function">event\_add</span>

### 说明

此函数是该函数的别名： <span class="function">event\_add</span>.

event\_timer\_del
=================

别名 <span class="function">event\_del</span>

### 说明

此函数是该函数的别名： <span class="function">event\_del</span>.

event\_timer\_new
=================

别名 <span class="function">event\_new</span>

### 说明

此函数是该函数的别名： <span class="function">event\_new</span>.

event\_timer\_set
=================

Prepare a timer event

### 说明

<span class="type">bool</span> <span
class="methodname">event\_timer\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$event`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$arg`</span> \] )

Prepares the timer event to be used in <span
class="function">event\_add</span>. The event is prepared to call the
function specified by the `callback` when the event timeout elapses.

After initializing the event, use <span
class="function">event\_base\_set</span> to associate the event with its
event base.

In case of matching event, these three arguments are passed to the
`callback` function:

`fd`  
Signal number or resource indicating the stream.

`events`  
A flag indicating the event. This will always be **`EV_TIMEOUT`** for
timer events.

`arg`  
Optional parameter, previously passed to <span
class="function">event\_timer\_set</span> as `arg`.

### 参数

`event`  
Valid event resource.

`callback`  
Callback function to be called when the matching event occurs.

`arg`  
Optional callback parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**目录**

-   [event\_add](/ref/libevent.html#event_add) — Add an event to the set
    of monitored events
-   [event\_base\_free](/ref/libevent.html#event_base_free) — Destroy
    event base
-   [event\_base\_loop](/ref/libevent.html#event_base_loop) — Handle
    events
-   [event\_base\_loopbreak](/ref/libevent.html#event_base_loopbreak) —
    Abort event loop
-   [event\_base\_loopexit](/ref/libevent.html#event_base_loopexit) —
    Exit loop after a time
-   [event\_base\_new](/ref/libevent.html#event_base_new) — Create and
    initialize new event base
-   [event\_base\_priority\_init](/ref/libevent.html#event_base_priority_init)
    — Set the number of event priority levels
-   [event\_base\_reinit](/ref/libevent.html#event_base_reinit) —
    Reinitialize the event base after a fork
-   [event\_base\_set](/ref/libevent.html#event_base_set) — Associate
    event base with an event
-   [event\_buffer\_base\_set](/ref/libevent.html#event_buffer_base_set)
    — Associate buffered event with an event base
-   [event\_buffer\_disable](/ref/libevent.html#event_buffer_disable) —
    Disable a buffered event
-   [event\_buffer\_enable](/ref/libevent.html#event_buffer_enable) —
    Enable a buffered event
-   [event\_buffer\_fd\_set](/ref/libevent.html#event_buffer_fd_set) —
    Change a buffered event file descriptor
-   [event\_buffer\_free](/ref/libevent.html#event_buffer_free) —
    Destroy buffered event
-   [event\_buffer\_new](/ref/libevent.html#event_buffer_new) — Create
    new buffered event
-   [event\_buffer\_priority\_set](/ref/libevent.html#event_buffer_priority_set)
    — Assign a priority to a buffered event
-   [event\_buffer\_read](/ref/libevent.html#event_buffer_read) — Read
    data from a buffered event
-   [event\_buffer\_set\_callback](/ref/libevent.html#event_buffer_set_callback)
    — Set or reset callbacks for a buffered event
-   [event\_buffer\_timeout\_set](/ref/libevent.html#event_buffer_timeout_set)
    — Set read and write timeouts for a buffered event
-   [event\_buffer\_watermark\_set](/ref/libevent.html#event_buffer_watermark_set)
    — Set the watermarks for read and write events
-   [event\_buffer\_write](/ref/libevent.html#event_buffer_write) —
    Write data to a buffered event
-   [event\_del](/ref/libevent.html#event_del) — Remove an event from
    the set of monitored events
-   [event\_free](/ref/libevent.html#event_free) — Free event resource
-   [event\_new](/ref/libevent.html#event_new) — Create new event
-   [event\_priority\_set](/ref/libevent.html#event_priority_set) —
    Assign a priority to an event
-   [event\_set](/ref/libevent.html#event_set) — Prepare an event
-   [event\_timer\_add](/ref/libevent.html#event_timer_add) — 别名
    event\_add
-   [event\_timer\_del](/ref/libevent.html#event_timer_del) — 别名
    event\_del
-   [event\_timer\_new](/ref/libevent.html#event_timer_new) — 别名
    event\_new
-   [event\_timer\_set](/ref/libevent.html#event_timer_set) — Prepare a
    timer event
