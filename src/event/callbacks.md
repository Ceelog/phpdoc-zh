Event callbacks
===============

If a callback is registered for an event, it will be called when the
event becomes active. To associate a callback with event one can pass a
<span class="type">callable</span> to either <span
class="methodname">Event::\_\_construct</span> , or <span
class="methodname">Event::set</span> , or one of the factory methods
like <span class="methodname">Event::timer</span> .

An event callback should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span class="type">mixed</span> `$fd`
<span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$what` </span> \[,
<span class="methodparam"> <span class="type">mixed</span> `$arg` <span
class="initializer"> = **`NULL`**</span> </span> \]\]\] )

`fd`  
The file descriptor, stream resource or socket associated with the
event. For signal event `fd` is equal to the signal number.

`what`  
Bit mask of *all* events triggered.

`arg`  
User custom data.

<span class="methodname">Event::timer</span> expects the callback to
match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span class="type">mixed</span> `$arg`
<span class="initializer"> = **`NULL`**</span> </span> \] )

`arg`  
User custom data.

<span class="methodname">Event::signal</span> expects the callback to
match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span class="type">int</span> `$signum`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` <span class="initializer"> = **`NULL`**</span> </span> \]\] )

`signum`  
The number of the triggered signal(e.g. **`SIGTERM`** ).

`arg`  
User custom data.
