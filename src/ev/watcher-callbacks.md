Watcher callbacks
=================

All watchers can be active(waiting for events) or inactive(paused). Only
active watchers will have their callbacks invoked. All callbacks will be
called with at least two arguments: `watcher` - the watcher, and
`revents` a bitmask of received events.

Watcher callbacks are passed to the watcher constructors (the classes
derived from <span class="classname">EvWatcher</span> - <span
class="methodname">EvCheck::\_\_construct</span> , <span
class="methodname">EvChild::\_\_construct</span> etc.). A watcher
callback should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span class="type">object</span>
`$watcher` <span class="initializer"> = NULL</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$revents` <span
class="initializer"> = NULL</span> </span> \]\] )

`watcher`  
The watcher instance(of a class extending <span
class="classname">EvWatcher</span> ).

`revents`  
<a href="/class/ev.html#" class="link">Watcher received events</a> .

Each watcher type has its associated bit in `revents` , so one can use
the same callback for multiple watchers. The event mask is named after
the type, i.e. <span class="classname">EvChild</span> (or <span
class="methodname">EvLoop::child</span> ) sets **`EV::CHILD`** , <span
class="classname">EvPrepare</span> (or <span
class="methodname">EvLoop::prepare</span> ) sets **`Ev::PREPARE`** ,
<span class="classname">EvPeriodic</span> (or <span
class="methodname">EvLoop::periodic</span> ) sets **`Ev::PERIODIC`** and
so on, with the exception of I/O events (which can set both
**`Ev::READ`** and **`Ev::WRITE`** bits).
