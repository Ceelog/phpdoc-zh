About buffer event callbacks
============================

An object of <span class="classname">EventBufferEvent</span> class
represents a *buffer event* . The asynchronous nature of I/O performed
by Libevent implies that a socket(or other kind of file descriptor) is
not always available. Event invokes corresponding callbacks when the
resource becomes available for reading or writing, or when some event
occurs(e.g. error, "end of line" etc.).

Read and write callbacks should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span
class="type">EventBufferEvent</span> `$bev` <span class="initializer"> =
**`null`**</span> </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$arg` <span class="initializer"> =
**`null`**</span> </span> \]\] )

`bev`  
Associated <span class="classname">EventBufferEvent</span> object.

`arg`  
Custom variable attached to all callbacks via <span
class="methodname">EventBufferEvent::\_\_construct</span> , or <span
class="methodname">EventBufferEvent::setCallbacks</span> .

Event callback should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span
class="type">EventBufferEvent</span> `$bev` <span class="initializer"> =
**`null`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$events` <span class="initializer"> = 0</span>
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` <span class="initializer"> = **`null`**</span> </span> \]\]\] )

`bev`  
Associated <span class="classname">EventBufferEvent</span> object.

`events`  
Bit mask of events: **`EventBufferEvent::READING`** ,
**`EventBufferEvent::WRITING`** , **`EventBufferEvent::EOL`** ,
**`EventBufferEvent::ERROR`** and **`EventBufferEvent::TIMEOUT`** . See
<a href="/class/eventbufferevent.html#预定义常量" class="link">EventBufferEvent constants</a>

`arg`  
Custom variable attached to all callbacks via <span
class="methodname">EventBufferEvent::\_\_construct</span> , or <span
class="methodname">EventBufferEvent::setCallbacks</span> .
