Ev
==

**目录**

-   [简介](/intro/ev.html)
-   [安装／配置](/ev/setup.html)
    -   [需求](/ev/setup.html#需求)
    -   [安装](/ev/setup.html#安装)
    -   [运行时配置](/ev/setup.html#运行时配置)
    -   [资源类型](/ev/setup.html#资源类型)
-   [预定义常量](/ev/global/constants.html)
-   [范例](/ev/examples.html)
-   [Watchers](/ev/watchers.html)
-   [Watcher callbacks](/ev/watcher-callbacks.html)
-   [Periodic watcher operation modes](/ev/periodic-modes.html)
-   [Ev](/class/ev.html) — The Ev class
    -   [Ev::backend](/class/ev.html#Ev::backend) — Returns an integer
        describing the backend used by libev
    -   [Ev::depth](/class/ev.html#Ev::depth) — Returns recursion depth
    -   [Ev::embeddableBackends](/class/ev.html#Ev::embeddableBackends)
        — Returns the set of backends that are embeddable in other event
        loops
    -   [Ev::feedSignal](/class/ev.html#Ev::feedSignal) — Feed a signal
        event info Ev
    -   [Ev::feedSignalEvent](/class/ev.html#Ev::feedSignalEvent) — Feed
        signal event into the default loop
    -   [Ev::iteration](/class/ev.html#Ev::iteration) — Return the
        number of times the default event loop has polled for new events
    -   [Ev::now](/class/ev.html#Ev::now) — Returns the time when the
        last iteration of the default event loop has started
    -   [Ev::nowUpdate](/class/ev.html#Ev::nowUpdate) — Establishes the
        current time by querying the kernel, updating the time returned
        by Ev::now in the progress
    -   [Ev::recommendedBackends](/class/ev.html#Ev::recommendedBackends)
        — Returns a bit mask of recommended backends for current
        platform
    -   [Ev::resume](/class/ev.html#Ev::resume) — Resume previously
        suspended default event loop
    -   [Ev::run](/class/ev.html#Ev::run) — Begin checking for events
        and calling callbacks for the default loop
    -   [Ev::sleep](/class/ev.html#Ev::sleep) — Block the process for
        the given number of seconds
    -   [Ev::stop](/class/ev.html#Ev::stop) — Stops the default event
        loop
    -   [Ev::supportedBackends](/class/ev.html#Ev::supportedBackends) —
        Returns the set of backends supported by current libev
        configuration
    -   [Ev::suspend](/class/ev.html#Ev::suspend) — Suspend the default
        event loop
    -   [Ev::time](/class/ev.html#Ev::time) — Returns the current time
        in fractional seconds since the epoch
    -   [Ev::verify](/class/ev.html#Ev::verify) — Performs internal
        consistency checks(for debugging)
-   [EvCheck](/class/evcheck.html) — The EvCheck class
    -   [EvCheck::\_\_construct](/class/evcheck.html#EvCheck::__construct)
        — Constructs the EvCheck watcher object
    -   [EvCheck::createStopped](/class/evcheck.html#EvCheck::createStopped)
        — Create instance of a stopped EvCheck watcher
-   [EvChild](/class/evchild.html) — The EvChild class
    -   [EvChild::\_\_construct](/class/evchild.html#EvChild::__construct)
        — Constructs the EvChild watcher object
    -   [EvChild::createStopped](/class/evchild.html#EvChild::createStopped)
        — Create instance of a stopped EvCheck watcher
    -   [EvChild::set](/class/evchild.html#EvChild::set) — Configures
        the watcher
-   [EvEmbed](/class/evembed.html) — The EvEmbed class
    -   [EvEmbed::\_\_construct](/class/evembed.html#EvEmbed::__construct)
        — Constructs the EvEmbed object
    -   [EvEmbed::createStopped](/class/evembed.html#EvEmbed::createStopped)
        — Create stopped EvEmbed watcher object
    -   [EvEmbed::set](/class/evembed.html#EvEmbed::set) — Configures
        the watcher
    -   [EvEmbed::sweep](/class/evembed.html#EvEmbed::sweep) — Make a
        single, non-blocking sweep over the embedded loop
-   [EvFork](/class/evfork.html) — The EvFork class
    -   [EvFork::\_\_construct](/class/evfork.html#EvFork::__construct)
        — Constructs the EvFork watcher object
    -   [EvFork::createStopped](/class/evfork.html#EvFork::createStopped)
        — Creates a stopped instance of EvFork watcher class
-   [EvIdle](/class/evidle.html) — The EvIdle class
    -   [EvIdle::\_\_construct](/class/evidle.html#EvIdle::__construct)
        — Constructs the EvIdle watcher object
    -   [EvIdle::createStopped](/class/evidle.html#EvIdle::createStopped)
        — Creates instance of a stopped EvIdle watcher object
-   [EvIo](/class/evio.html) — The EvIo class
    -   [EvIo::\_\_construct](/class/evio.html#EvIo::__construct) —
        Constructs EvIo watcher object
    -   [EvIo::createStopped](/class/evio.html#EvIo::createStopped) —
        Create stopped EvIo watcher object
    -   [EvIo::set](/class/evio.html#EvIo::set) — Configures the watcher
-   [EvLoop](/class/evloop.html) — The EvLoop class
    -   [EvLoop::backend](/class/evloop.html#EvLoop::backend) — Returns
        an integer describing the backend used by libev
    -   [EvLoop::check](/class/evloop.html#EvLoop::check) — Creates
        EvCheck object associated with the current event loop instance
    -   [EvLoop::child](/class/evloop.html#EvLoop::child) — Creates
        EvChild object associated with the current event loop
    -   [EvLoop::\_\_construct](/class/evloop.html#EvLoop::__construct)
        — Constructs the event loop object
    -   [EvLoop::defaultLoop](/class/evloop.html#EvLoop::defaultLoop) —
        Returns or creates the default event loop
    -   [EvLoop::embed](/class/evloop.html#EvLoop::embed) — Creates an
        instance of EvEmbed watcher associated with the current EvLoop
        object
    -   [EvLoop::fork](/class/evloop.html#EvLoop::fork) — Creates EvFork
        watcher object associated with the current event loop instance
    -   [EvLoop::idle](/class/evloop.html#EvLoop::idle) — Creates EvIdle
        watcher object associated with the current event loop instance
    -   [EvLoop::invokePending](/class/evloop.html#EvLoop::invokePending)
        — Invoke all pending watchers while resetting their pending
        state
    -   [EvLoop::io](/class/evloop.html#EvLoop::io) — Create EvIo
        watcher object associated with the current event loop instance
    -   [EvLoop::loopFork](/class/evloop.html#EvLoop::loopFork) — Must
        be called after a fork
    -   [EvLoop::now](/class/evloop.html#EvLoop::now) — Returns the
        current "event loop time"
    -   [EvLoop::nowUpdate](/class/evloop.html#EvLoop::nowUpdate) —
        Establishes the current time by querying the kernel, updating
        the time returned by EvLoop::now in the progress
    -   [EvLoop::periodic](/class/evloop.html#EvLoop::periodic) —
        Creates EvPeriodic watcher object associated with the current
        event loop instance
    -   [EvLoop::prepare](/class/evloop.html#EvLoop::prepare) — Creates
        EvPrepare watcher object associated with the current event loop
        instance
    -   [EvLoop::resume](/class/evloop.html#EvLoop::resume) — Resume
        previously suspended default event loop
    -   [EvLoop::run](/class/evloop.html#EvLoop::run) — Begin checking
        for events and calling callbacks for the loop
    -   [EvLoop::signal](/class/evloop.html#EvLoop::signal) — Creates
        EvSignal watcher object associated with the current event loop
        instance
    -   [EvLoop::stat](/class/evloop.html#EvLoop::stat) — Creates EvStat
        watcher object associated with the current event loop instance
    -   [EvLoop::stop](/class/evloop.html#EvLoop::stop) — Stops the
        event loop
    -   [EvLoop::suspend](/class/evloop.html#EvLoop::suspend) — Suspend
        the loop
    -   [EvLoop::timer](/class/evloop.html#EvLoop::timer) — Creates
        EvTimer watcher object associated with the current event loop
        instance
    -   [EvLoop::verify](/class/evloop.html#EvLoop::verify) — Performs
        internal consistency checks(for debugging)
-   [EvPeriodic](/class/evperiodic.html) — The EvPeriodic class
    -   [EvPeriodic::again](/class/evperiodic.html#EvPeriodic::again) —
        Simply stops and restarts the periodic watcher again
    -   [EvPeriodic::at](/class/evperiodic.html#EvPeriodic::at) —
        Returns the absolute time that this watcher is supposed to
        trigger next
    -   [EvPeriodic::\_\_construct](/class/evperiodic.html#EvPeriodic::__construct)
        — Constructs EvPeriodic watcher object
    -   [EvPeriodic::createStopped](/class/evperiodic.html#EvPeriodic::createStopped)
        — Create a stopped EvPeriodic watcher
    -   [EvPeriodic::set](/class/evperiodic.html#EvPeriodic::set) —
        Configures the watcher
-   [EvPrepare](/class/evprepare.html) — The EvPrepare class
    -   [EvPrepare::\_\_construct](/class/evprepare.html#EvPrepare::__construct)
        — Constructs EvPrepare watcher object
    -   [EvPrepare::createStopped](/class/evprepare.html#EvPrepare::createStopped)
        — Creates a stopped instance of EvPrepare watcher
-   [EvSignal](/class/evsignal.html) — The EvSignal class
    -   [EvSignal::\_\_construct](/class/evsignal.html#EvSignal::__construct)
        — Constructs EvSignal watcher object
    -   [EvSignal::createStopped](/class/evsignal.html#EvSignal::createStopped)
        — Create stopped EvSignal watcher object
    -   [EvSignal::set](/class/evsignal.html#EvSignal::set) — Configures
        the watcher
-   [EvStat](/class/evstat.html) — The EvStat class
    -   [EvStat::attr](/class/evstat.html#EvStat::attr) — Returns the
        values most recently detected by Ev
    -   [EvStat::\_\_construct](/class/evstat.html#EvStat::__construct)
        — Constructs EvStat watcher object
    -   [EvStat::createStopped](/class/evstat.html#EvStat::createStopped)
        — Create a stopped EvStat watcher object
    -   [EvStat::prev](/class/evstat.html#EvStat::prev) — Returns the
        previous set of values returned by EvStat::attr
    -   [EvStat::set](/class/evstat.html#EvStat::set) — Configures the
        watcher
    -   [EvStat::stat](/class/evstat.html#EvStat::stat) — Initiates the
        stat call
-   [EvTimer](/class/evtimer.html) — The EvTimer class
    -   [EvTimer::again](/class/evtimer.html#EvTimer::again) — Restarts
        the timer watcher
    -   [EvTimer::\_\_construct](/class/evtimer.html#EvTimer::__construct)
        — Constructs an EvTimer watcher object
    -   [EvTimer::createStopped](/class/evtimer.html#EvTimer::createStopped)
        — Creates EvTimer stopped watcher object
    -   [EvTimer::set](/class/evtimer.html#EvTimer::set) — Configures
        the watcher
-   [EvWatcher](/class/evwatcher.html) — The EvWatcher class
    -   [EvWatcher::clear](/class/evwatcher.html#EvWatcher::clear) —
        Clear watcher pending status
    -   [EvWatcher::\_\_construct](/class/evwatcher.html#EvWatcher::__construct)
        — Abstract constructor of a watcher object
    -   [EvWatcher::feed](/class/evwatcher.html#EvWatcher::feed) — Feeds
        the given revents set into the event loop
    -   [EvWatcher::getLoop](/class/evwatcher.html#EvWatcher::getLoop) —
        Returns the loop responsible for the watcher
    -   [EvWatcher::invoke](/class/evwatcher.html#EvWatcher::invoke) —
        Invokes the watcher callback with the given received events bit
        mask
    -   [EvWatcher::keepalive](/class/evwatcher.html#EvWatcher::keepalive)
        — Configures whether to keep the loop from returning
    -   [EvWatcher::setCallback](/class/evwatcher.html#EvWatcher::setCallback)
        — Sets new callback for the watcher
    -   [EvWatcher::start](/class/evwatcher.html#EvWatcher::start) —
        Starts the watcher
    -   [EvWatcher::stop](/class/evwatcher.html#EvWatcher::stop) — Stops
        the watcher

简介
----

Ev is a static class providing access to the default loop and to some
common operations.

类摘要
------

**Ev**

<span class="ooclass"> <span class="modifier">final</span> class **Ev**
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::FLAG_AUTO` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::FLAG_NOENV` <span class="initializer"> = 16777216</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::FLAG_FORKCHECK` <span class="initializer"> = 33554432</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::FLAG_NOINOTIFY` <span class="initializer"> = 1048576</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::FLAG_SIGNALFD` <span class="initializer"> = 2097152</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::FLAG_NOSIGMASK` <span class="initializer"> = 4194304</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::RUN_NOWAIT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::RUN_ONCE` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BREAK_CANCEL` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BREAK_ONE` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BREAK_ALL` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::MINPRI` <span class="initializer"> = -2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::MAXPRI` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::READ` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::WRITE` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::TIMER` <span class="initializer"> = 256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::PERIODIC` <span class="initializer"> = 512</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::SIGNAL` <span class="initializer"> = 1024</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::CHILD` <span class="initializer"> = 2048</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::STAT` <span class="initializer"> = 4096</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::IDLE` <span class="initializer"> = 8192</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::PREPARE` <span class="initializer"> = 16384</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::CHECK` <span class="initializer"> = 32768</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::EMBED` <span class="initializer"> = 65536</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::CUSTOM` <span class="initializer"> = 16777216</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::ERROR` <span class="initializer"> = 2147483648</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_SELECT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_POLL` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_EPOLL` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_KQUEUE` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_DEVPOLL` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_PORT` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_ALL` <span class="initializer"> = 63</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Ev::BACKEND_MASK` <span class="initializer"> = 65535</span> ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">backend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">depth</span> ( <span class="methodparam">void</span>
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">embeddableBackends</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">feedSignal</span> ( <span class="methodparam">
<span class="type">int</span> `$signum` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">feedSignalEvent</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">iteration</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">float</span>
<span class="methodname">now</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">nowUpdate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">recommendedBackends</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">resume</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">run</span> (\[ <span class="methodparam"> <span
class="type">int</span> `$flags` </span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">sleep</span> ( <span class="methodparam"> <span
class="type">float</span> `$seconds` </span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">stop</span> (\[ <span class="methodparam">
<span class="type">int</span> `$how` </span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">supportedBackends</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">suspend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">float</span>
<span class="methodname">time</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">verify</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

Flags passed to create a loop:

**`Ev::FLAG_AUTO`**  
The default flags value

**`Ev::FLAG_NOENV`**  
If this flag used(or the program runs setuid or setgid), *libev* won't
look at the environment variable `LIBEV_FLAGS` . Otherwise(by default),
`LIBEV_FLAGS` will override the flags completely if it is found. Useful
for performance tests and searching for bugs.

**`Ev::FLAG_FORKCHECK`**  
Makes libev check for a fork in each iteration, instead of calling <span
class="methodname">EvLoop::fork</span> manually. This works by calling
*getpid()* on every iteration of the loop, and thus this might slow down
the event loop with lots of loop iterations, but usually is not
noticeable. This flag setting cannot be overridden or specified in the
`LIBEV_FLAGS` environment variable.

**`Ev::FLAG_NOINOTIFY`**  
When this flag is specified, *libev* won't attempt to use the *inotify*
API for its
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_stat_code_did_the_file_attri" class="link external">» ev_stat</a>
watchers. The flag can be useful to conserve inotify file descriptors,
as otherwise each loop using *ev\_stat* watchers consumes one *inotify*
handle.

**`Ev::FLAG_SIGNALFD`**  
When this flag is specified, *libev* will attempt to use the *signalfd*
API for its
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_signal_code_signal_me_when_a" class="link external">» ev_signal</a>
(and
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_child_code_watch_out_for_pro" class="link external">» ev_child</a>
) watchers. This API delivers signals synchronously, which makes it both
faster and might make it possible to get the queued signal data. It can
also simplify signal handling with threads, as long as signals are
properly blocked in threads. *Signalfd* will not be used by default.

**`Ev::FLAG_NOSIGMASK`**  
When this flag is specified, *libev* will avoid to modify the signal
mask. Specifically, this means having to make sure signals are unblocked
before receiving them.

This behaviour is useful for custom signal handling, or handling signals
only in specific threads.

Flags passed to <span class="methodname">Ev::run</span> , or <span
class="methodname">EvLoop::run</span>

**`Ev::RUN_NOWAIT`**  
Means that event loop will look for new events, will handle those events
and any already outstanding ones, but will not wait and block the
process in case there are no events and will return after one iteration
of the loop. This is sometimes useful to poll and handle new events
while doing lengthy calculations, to keep the program responsive.

**`Ev::RUN_ONCE`**  
Means that event loop will look for new events (waiting if necessary)
and will handle those and any already outstanding ones. It will block
the process until at least one new event arrives (which could be an
event internal to libev itself, so there is no guarantee that a
user-registered callback will be called), and will return after one
iteration of the loop.

Flags passed to <span class="methodname">Ev::stop</span> , or <span
class="methodname">EvLoop::stop</span>

**`Ev::BREAK_CANCEL`**  
Cancel the break operation.

**`Ev::BREAK_ONE`**  
Makes the innermost <span class="methodname">Ev::run</span> (or <span
class="methodname">EvLoop::run</span> ) call return.

**`Ev::BREAK_ALL`**  
Makes all nested <span class="methodname">Ev::run</span> (or <span
class="methodname">EvLoop::run</span> ) calls return.

Watcher priorities:

**`Ev::MINPRI`**  
Minimum allowed watcher priority.

**`Ev::MAXPRI`**  
Maximum allowed watcher priority.

Bit masks of (received) events:

**`Ev::READ`**  
The file descriptor in the <span class="classname">EvIo</span> watcher
has become readable.

**`Ev::WRITE`**  
The file descriptor in the <span class="classname">EvIo</span> watcher
has become writable.

**`Ev::TIMER`**  
<span class="classname">EvTimer</span> watcher has been timed out.

**`Ev::PERIODIC`**  
<span class="classname">EvPeriodic</span> watcher has been timed out.

**`Ev::SIGNAL`**  
A signal specified in <span
class="methodname">EvSignal::\_\_construct</span> has been received.

**`Ev::CHILD`**  
The `pid` specified in <span
class="methodname">EvChild::\_\_construct</span> has received a status
change.

**`Ev::STAT`**  
The path specified in <span class="classname">EvStat</span> watcher
changed its attributes.

**`Ev::IDLE`**  
<span class="classname">EvIdle</span> watcher works when there is
nothing to do with other watchers.

**`Ev::PREPARE`**  
All <span class="classname">EvPrepare</span> watchers are invoked just
before <span class="methodname">Ev::run</span> starts. Thus, <span
class="classname">EvPrepare</span> watchers are the last watchers
invoked before the event loop sleeps or polls for new events.

**`Ev::CHECK`**  
All <span class="classname">EvCheck</span> watchers are queued just
after <span class="methodname">Ev::run</span> has gathered the new
events, but before it queues any callbacks for any received events.
Thus, <span class="classname">EvCheck</span> watchers will be invoked
before any other watchers of the same or lower priority within an event
loop iteration.

**`Ev::EMBED`**  
The embedded event loop specified in the <span
class="classname">EvEmbed</span> watcher needs attention.

**`Ev::CUSTOM`**  
Not ever sent(or otherwise used) by *libev* itself, but can be freely
used by *libev* users to signal watchers (e.g. via <span
class="methodname">EvWatcher::feed</span> ).

**`Ev::ERROR`**  
An unspecified error has occurred, the watcher has been stopped. This
might happen because the watcher could not be properly started because
*libev* ran out of memory, a file descriptor was found to be closed or
any other problem. *Libev* considers these application bugs. See also
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#ANATOMY_OF_A_WATCHER_CONTENT" class="link external">» ANATOMY OF A WATCHER</a>

Backend flags:

**`Ev::BACKEND_SELECT`**  
*select(2) backend*

**`Ev::BACKEND_POLL`**  
*poll(2) backend*

**`Ev::BACKEND_EPOLL`**  
Linux-specific *epoll(7)* backend for both pre- and post-2.6.9 kernels

**`Ev::BACKEND_KQUEUE`**  
*kqueue* backend used on most BSD systems. <span
class="classname">EvEmbed</span> watcher could be used to embed one
loop(with kqueue backend) into another. For instance, one can try to
create an event loop with *kqueue* backend and use it for sockets only.

**`Ev::BACKEND_DEVPOLL`**  
Solaris 8 backend. This is not implemented yet.

**`Ev::BACKEND_PORT`**  
Solaris 10 event port mechanism with a good scaling.

**`Ev::BACKEND_ALL`**  
Try all backends(even currupted ones). It's not recommended to use it
explicitly. Bitwise operators should be applied here(e.g.
**`Ev::BACKEND_ALL`** & \~ **`Ev::BACKEND_KQUEUE`** ) Use <span
class="methodname">Ev::recommendedBackends</span> , or don't specify any
backends at all.

**`Ev::BACKEND_MASK`**  
Not a backend, but a mask to select all backend bits from `flags` value
to mask out any backends(e.g. when modifying the `LIBEV_FLAGS`
environment variable).

> **Note**:
>
> For the default loop during module initialization phase *Ev* registers
> <a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS_CO" class="link external">» ev_loop_fork</a>
> call by means of *pthread\_atfork* (if available).

> **Note**:
>
> There are methods providing access to the *default event loop* in
> <span class="classname">Ev</span> class(e.g. <span
> class="methodname">Ev::iteration</span> , <span
> class="methodname">Ev::depth</span> etc.) For *custom loops* (created
> with <span class="methodname">EvLoop::\_\_construct</span> ) these
> values may be accessed via corresponding properties and methods of the
> <span class="classname">EvLoop</span> class.
>
> The instance of the default event loop itself can be fetched by means
> of <span class="methodname">EvLoop::defaultLoop</span> method.

Ev::backend
===========

Returns an integer describing the backend used by libev

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Ev::backend</span> ( <span
class="methodparam">void</span> )

Returns an integer describing the backend used by *libev* . See
<a href="/class/ev.html#" class="link">Backend flags</a>

### 参数

此函数没有参数。

### 返回值

Returns an integer(bit mask) describing the backend used by *libev* .

### 参见

-   <span class="classname">EvEmbed</span>
-   <span class="methodname">Ev::embeddableBackends</span>
-   <span class="methodname">Ev::recommendedBackends</span>
-   <span class="methodname">Ev::supportedBackends</span>
-   <a href="/class/ev.html#" class="link">Backend flags</a>

Ev::depth
=========

Returns recursion depth

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Ev::depth</span> ( <span
class="methodparam">void</span> )

The number of times <span class="methodname">Ev::run</span> was entered
minus the number of times <span class="methodname">Ev::run</span> was
exited normally, in other words, the recursion depth. Outside <span
class="methodname">Ev::run</span> , this number is **`0`** . In a
callback, this number is **`1`** , unless <span
class="methodname">Ev::run</span> was invoked recursively (or from
another thread), in which case it is higher.

### 参数

此函数没有参数。

### 返回值

<span class="function">ev\_depth</span> returns recursion depth of the
default loop.

### 参见

-   <span class="methodname">Ev::iteration</span>

Ev::embeddableBackends
======================

Returns the set of backends that are embeddable in other event loops

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Ev::embeddableBackends</span> ( <span
class="methodparam">void</span> )

Returns the set of backends that are embeddable in other event loops.

### 参数

此函数没有参数。

### 返回值

Returns a bit mask which can containing
<a href="/class/ev.html#" class="link">backend flags</a> combined using
bitwise *OR* operator.

### 范例

**示例 \#1 Embedding loop created with kqueue backend into the default
loop**

``` php
<?php
/*
* Check if kqueue is available but not recommended and create a kqueue backend
* for use with sockets (which usually work with any kqueue implementation).
* Store the kqueue/socket-only event loop in loop_socket. (One might optionally
* use EVFLAG_NOENV, too)
*
* Example borrowed from
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
 if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
  $embed = new EvEmbed($loop);
 }
}

if (!$socket_loop) {
 $socket_loop = $loop;
}

// Now use $socket_loop for all sockets, and $loop for anything else
?>
```

### 参见

-   <span class="classname">EvEmbed</span>
-   <span class="methodname">Ev::recommendedBackends</span>
-   <span class="methodname">Ev::supportedBackends</span>
-   <a href="/class/ev.html#" class="link">Backend flags</a>
-   <a href="/ev/examples.html" class="link">Examples</a>

Ev::feedSignal
==============

Feed a signal event info Ev

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::feedSignal</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> )

Simulates a signal receive. It is safe to call this function at any
time, from any context, including signal handlers or random threads. Its
main use is to customise signal handling in the process.

Unlike <span class="methodname">Ev::feedSignalEvent</span> , this works
regardless of which loop has registered the signal.

### 参数

`signum`  
Signal number. See *signal(7)* man page for detals. You can use
constants exported by *pcntl* extension.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::feedSignalEvent</span>

Ev::feedSignalEvent
===================

Feed signal event into the default loop

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::feedSignalEvent</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> )

Feed signal event into the default loop. Ev will react to this call as
if the signal specified by `signal` had occurred.

### 参数

`signum`  
Signal number. See *signal(7)* man page for detals. See also constants
exported by *pcntl* extension.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::feedSignal</span>

Ev::iteration
=============

Return the number of times the default event loop has polled for new
events

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Ev::iteration</span> ( <span
class="methodparam">void</span> )

Return the number of times the event loop has polled for new events.
Sometimes useful as a generation counter.

### 参数

此函数没有参数。

### 返回值

Returns number of polls of the default event loop.

### 参见

-   <span class="methodname">Ev::depth</span>

Ev::now
=======

Returns the time when the last iteration of the default event loop has
started

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">float</span>
<span class="methodname">Ev::now</span> ( <span
class="methodparam">void</span> )

Returns the time when the last iteration of the default event loop has
started. This is the time that timers( <span
class="classname">EvTimer</span> and <span
class="classname">EvPeriodic</span> ) are based on, and referring to it
is usually faster then calling <span class="methodname">Ev::time</span>
.

### 参数

此函数没有参数。

### 返回值

Returns number of seconds(fractional) representing the time when the
last iteration of the default event loop has started.

### 参见

-   <span class="methodname">Ev::nowUpdate</span>

Ev::nowUpdate
=============

Establishes the current time by querying the kernel, updating the time
returned by Ev::now in the progress

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::nowUpdate</span> ( <span
class="methodparam">void</span> )

Establishes the current time by querying the kernel, updating the time
returned by <span class="methodname">Ev::now</span> in the progress.
This is a costly operation and is usually done automatically within
<span class="methodname">Ev::run</span> .

This method is rarely useful, but when some event callback runs for a
very long time without entering the event loop, updating *libev* 's
consideration of the current time is a good idea.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::now</span>

Ev::recommendedBackends
=======================

Returns a bit mask of recommended backends for current platform

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Ev::recommendedBackends</span> ( <span
class="methodparam">void</span> )

Returns the set of all backends compiled into this binary of *libev* and
also recommended for this platform, meaning it will work for most file
descriptor types. This set is often smaller than the one returned by
<span class="function">ev\_supported\_backends</span> , as for example
*kqueue* is broken on most *BSD* systems and will not be auto-detected
unless it is requested explicitly. This is the set of backends that
*libev* will probe no backends specified explicitly.

### 参数

此函数没有参数。

### 返回值

Returns a bit mask which can containing
<a href="/class/ev.html#" class="link">backend flags</a> combined using
bitwise *OR* operator.

### 范例

**示例 \#1 Embedding one loop into another**

``` php
<?php
/*
* Try to get an embeddable event loop and embed it into the default event loop.
* If it is impossible, use the default
* loop. The default loop is stored in $loop_hi, while the embeddable loop is
* stored in $loop_lo(which is $loop_hi in the case no embeddable loop can be
* used).
*
* Sample translated to PHP
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop_hi = EvLoop::defaultLoop();
$loop_lo = NULL;
$embed   = NULL;

/*
* See if there is a chance of getting one that works
* (flags' value of 0 means autodetection)
*/
$loop_lo = Ev::embeddableBackends() & Ev::recommendedBackends()
 ? new EvLoop(Ev::embeddableBackends() & Ev::recommendedBackends())
 : 0;

if ($loop_lo) {
 $embed = new EvEmbed($loop_lo, function () {});
} else {
 $loop_lo = $loop_hi;
}
?>
```

### 参见

-   <span class="classname">EvEmbed</span>
-   <span class="methodname">Ev::embeddableBackends</span>
-   <span class="methodname">Ev::supportedBackends</span>
-   <a href="/class/ev.html#" class="link">Backend flags</a>
-   <a href="/ev/examples.html" class="link">Examples</a>

Ev::resume
==========

Resume previously suspended default event loop

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::resume</span> ( <span
class="methodparam">void</span> )

<span class="methodname">Ev::suspend</span> and <span
class="methodname">Ev::resume</span> methods suspend and resume a loop
correspondingly.

All timer watchers will be delayed by the time spend between *suspend*
and *resume* , and all *periodic* watchers will be rescheduled(that is,
they will lose any events that would have occurred while suspended).

After calling <span class="methodname">Ev::suspend</span> it is not
allowed to call any function on the given loop other than <span
class="methodname">Ev::resume</span> . Also it is not allowed to call
<span class="methodname">Ev::resume</span> without a previous call to
<span class="methodname">Ev::suspend</span> .

Calling *suspend* / *resume* has the side effect of updating the event
loop time(see <span class="methodname">Ev::nowUpdate</span> ).

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::suspend</span>

Ev::run
=======

Begin checking for events and calling callbacks for the default loop

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::run</span> (\[ <span class="methodparam">
<span class="type">int</span> `$flags` </span> \] )

Begin checking for events and calling callbacks *for the default loop* .
Returns when a callback calls <span class="methodname">Ev::stop</span>
method, or the flags are nonzero(in which case the return value is true)
or when there are no active watchers which reference the loop( <span
class="methodname">EvWatcher::keepalive</span> is **`TRUE`**), in which
case the return value will be **`FALSE`**. The return value can
generally be interpreted as *if **`TRUE`**, there is more work left to
do* .

### 参数

`flags`  
Optional parameter `flags` can be one of the following:

| `flags`              | Description                                             |
|----------------------|---------------------------------------------------------|
| **`0`**              | The default behavior described above                    |
| **`Ev::RUN_ONCE`**   | Block at most one(wait, but don't loop)                 |
| **`Ev::RUN_NOWAIT`** | Don't block at all(fetch/handle events, but don't wait) |

See <a href="/class/ev.html#" class="link">the run flag constants</a> .

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::stop</span>
-   <span class="methodname">EvLoop::run</span>

Ev::sleep
=========

Block the process for the given number of seconds

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::sleep</span> ( <span class="methodparam">
<span class="type">float</span> `$seconds` </span> )

Block the process for the given number of seconds.

### 参数

`seconds`  
Fractional number of seconds

### 返回值

没有返回值。

Ev::stop
========

Stops the default event loop

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::stop</span> (\[ <span class="methodparam">
<span class="type">int</span> `$how` </span> \] )

Stops the default event loop

### 参数

`how`  
One of *Ev::BREAK\_\**
<a href="/class/ev.html#" class="link">constants</a> .

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::run</span>

Ev::supportedBackends
=====================

Returns the set of backends supported by current libev configuration

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Ev::supportedBackends</span> ( <span
class="methodparam">void</span> )

Returns the set of backends supported by current libev configuration.

### 参数

此函数没有参数。

### 返回值

Returns a bit mask which can containing
<a href="/class/ev.html#" class="link">backend flags</a> combined using
bitwise *OR* operator.

### 范例

**示例 \#1 Embedding loop created with kqueue backend into the default
loop**

``` php
<?php
/*
* Check if kqueue is available but not recommended and create a kqueue backend
* for use with sockets (which usually work with any kqueue implementation).
* Store the kqueue/socket-only event loop in loop_socket. (One might optionally
* use EVFLAG_NOENV, too)
*
* Example borrowed from
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
 if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
  $embed = new EvEmbed($loop);
 }
}

if (!$socket_loop) {
 $socket_loop = $loop;
}

// Now use $socket_loop for all sockets, and $loop for anything else
?>
```

### 参见

-   <span class="classname">EvEmbed</span>
-   <span class="methodname">Ev::recommendedBackends</span>
-   <span class="methodname">Ev::embeddableBackends</span>
-   <a href="/class/ev.html#" class="link">Backend flags</a>
-   <a href="/ev/examples.html" class="link">Examples</a>

Ev::suspend
===========

Suspend the default event loop

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::suspend</span> ( <span
class="methodparam">void</span> )

<span class="methodname">Ev::suspend</span> and <span
class="methodname">Ev::resume</span> methods suspend and resume the
default loop correspondingly.

All timer watchers will be delayed by the time spend between *suspend*
and *resume* , and all *periodic* watchers will be rescheduled(that is,
they will lose any events that would have occurred while suspended).

After calling <span class="methodname">Ev::suspend</span> it is not
allowed to call any function on the given loop other than <span
class="methodname">Ev::resume</span> . Also it is not allowed to call
<span class="methodname">Ev::resume</span> without a previous call to
<span class="methodname">Ev::suspend</span> .

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::resume</span>

Ev::time
========

Returns the current time in fractional seconds since the epoch

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">float</span>
<span class="methodname">Ev::time</span> ( <span
class="methodparam">void</span> )

Returns the current time in fractional seconds since the epoch. Consider
using <span class="methodname">Ev::now</span>

### 参数

此函数没有参数。

### 返回值

Returns the current time in fractional seconds since the epoch.

### 参见

-   <span class="methodname">Ev::now</span>

Ev::verify
==========

Performs internal consistency checks(for debugging)

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Ev::verify</span> ( <span
class="methodparam">void</span> )

Performs internal consistency checks(for debugging *libev* ) and abort
the program if any data structures were found to be corrupted.

### 参数

此函数没有参数。

### 返回值

没有返回值。

简介
----

<span class="classname">EvPrepare</span> and <span
class="classname">EvCheck</span> watchers are usually used in pairs.
<span class="classname">EvPrepare</span> watchers get invoked before the
process blocks, <span class="classname">EvCheck</span> afterwards.

It is not allowed to call <span class="methodname">EvLoop::run</span> or
similar methods or functions that enter the current event loop from
either <span class="classname">EvPrepare</span> or <span
class="classname">EvCheck</span> watchers. Other loops than the current
one are fine, however. The rationale behind this is that one don't need
to check for recursion in those watchers, i.e. the sequence will always
be: <span class="classname">EvPrepare</span> -\> blocking -\> <span
class="classname">EvCheck</span> , so having a watcher of each kind they
will always be called in pairs bracketing the blocking call.

The main purpose is to integrate other event mechanisms into *libev* and
their use is somewhat advanced. They could be used, for example, to
track variable changes, implement custom watchers, integrate net-snmp or
a coroutine library and lots more. They are also occasionally useful to
cache some data and want to flush it before blocking.

It is recommended to give <span class="classname">EvCheck</span>
watchers highest( **`Ev::MAXPRI`** ) priority, to ensure that they are
being run before any other watchers after the poll (this doesn’t matter
for <span class="classname">EvPrepare</span> watchers).

Also, <span class="classname">EvCheck</span> watchers should not
activate/feed events. While *libev* fully supports this, they might get
executed before other <span class="classname">EvCheck</span> watchers
did their job.

类摘要
------

**EvCheck**

<span class="ooclass"> class **EvCheck** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$priority`
</span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

EvCheck::\_\_construct
======================

Constructs the EvCheck watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvCheck::\_\_construct</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` </span> \]\] )

Constructs the <span class="classname">EvCheck</span> watcher object.

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvCheck object on success.

### 参见

-   <span class="classname">EvPrepare</span>
-   <span class="methodname">EvLoop::check</span>

EvCheck::createStopped
======================

Create instance of a stopped EvCheck watcher

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">EvCheck::createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\] )

Create instance of a stopped EvCheck watcher

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvCheck object on success.

### 参见

-   <span class="classname">EvPrepare</span>

简介
----

<span class="classname">EvChild</span> watchers trigger when the process
receives a **`SIGCHLD`** in response to some child status changes (most
typically when a child dies or exits). It is permissible to install an
**`EvChild`** watcher after the child has been forked(which implies it
might have already exited), as long as the event loop isn't entered(or
is continued from a watcher), i.e. forking and then immediately
registering a watcher for the child is fine, but forking and registering
a watcher a few event loop iterations later or in the next callback
invocation is not.

It is allowed to register <span class="classname">EvChild</span>
watchers in the *default loop* only.

类摘要
------

**EvChild**

<span class="ooclass"> class **EvChild** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$pid` ;

<span class="modifier">public</span> `$rpid` ;

<span class="modifier">public</span> `$rstatus` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">int</span> `$pid` </span> , <span
class="methodparam"> <span class="type">bool</span> `$trace` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">int</span> `$pid` </span> ,
<span class="methodparam"> <span class="type">bool</span> `$trace`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">int</span> `$pid` </span> , <span class="methodparam">
<span class="type">bool</span> `$trace` </span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`pid`  
*Readonly* . The process ID this watcher watches out for, or **`0`** ,
meaning any process ID.

`rpid`  
*Readonly* .The process ID that detected a status change.

`rstatus`  
*Readonly* . The process exit status caused by `rpid` .

EvChild::\_\_construct
======================

Constructs the EvChild watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvChild::\_\_construct</span> ( <span
class="methodparam"> <span class="type">int</span> `$pid` </span> ,
<span class="methodparam"> <span class="type">bool</span> `$trace`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Constructs the <span class="classname">EvChild</span> watcher object.

Call the callback when a status change for process ID `pid` (or any
*PID* if `pid` is **`0`** ) has been received(a status change happens
when the process terminates or is killed, or, when `trace` is
**`TRUE`**, additionally when it is stopped or continued). In other
words, when the process receives a **`SIGCHLD`** , *Ev* will fetch the
outstanding exit/wait status for all changed/zombie children and call
the callback.

It is valid to install a child watcher after an <span
class="classname">EvChild</span> has exited but before the event loop
has started its next iteration. For example, first one calls *fork* ,
then the new child process might exit, and only then an <span
class="classname">EvChild</span> watcher is installed in the parent for
the new *PID* .

You can access both exit/tracing status and `pid` by using the `rstatus`
and `rpid` properties of the watcher object.

The number of *PID* watchers per *PID* is unlimited. All of them will be
called.

The <span class="methodname">EvChild::createStopped</span> method
doesn't start(activate) the newly created watcher.

### 参数

`pid`  
Wait for status changes of process PID(or any process if PID is
specified as **`0`** ).

`trace`  
If **`FALSE`**, only activate the watcher when the process terminates.
Otherwise(**`TRUE`**) additionally activate the watcher when the process
is stopped or continued.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvChild object on success.

### 参见

-   <span class="methodname">EvLoop::child</span>

EvChild::createStopped
======================

Create instance of a stopped EvCheck watcher

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">EvChild::createStopped</span> ( <span
class="methodparam"> <span class="type">int</span> `$pid` </span> ,
<span class="methodparam"> <span class="type">bool</span> `$trace`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\] )

The same as <span class="methodname">EvChild::\_\_construct</span> , but
doesn't start the watcher automatically.

### 参数

`pid`  
The same as for <span class="methodname">EvChild::\_\_construct</span>

`trace`  
The same as for <span class="methodname">EvChild::\_\_construct</span>

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

### 参见

-   <span class="methodname">EvChild::\_\_construct</span>
-   <span class="methodname">EvLoop::child</span>

EvChild::set
============

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvChild::set</span> ( <span
class="methodparam"> <span class="type">int</span> `$pid` </span> ,
<span class="methodparam"> <span class="type">bool</span> `$trace`
</span> )

### 参数

`pid`  
The same as for <span class="methodname">EvChild::\_\_construct</span>

`trace`  
The same as for <span class="methodname">EvChild::\_\_construct</span>

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvChild::\_\_construct</span>

简介
----

Used to embed one event loop into another.

类摘要
------

**EvEmbed**

<span class="ooclass"> class **EvEmbed** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$embed` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">object</span> `$other` </span> \[, <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` </span> \]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">object</span> `$other` </span>
\[, <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">object</span> `$other` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sweep</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`is_active`  

`data`  

`is_pending`  

`priority`  

`embed`  

EvEmbed::\_\_construct
======================

Constructs the EvEmbed object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvEmbed::\_\_construct</span> ( <span
class="methodparam"> <span class="type">object</span> `$other` </span>
\[, <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\]\] )

This is a rather advanced watcher type that lets to embed one event loop
into another(currently only IO events are supported in the embedded
loop, other types of watchers might be handled in a delayed or incorrect
fashion and must not be used).

See
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_embed_code_when_one_backend_" class="link external">» the libev documentation</a>
for details.

This watcher is most useful on *BSD* systems without working *kqueue* to
still be able to handle a large number of sockets. See example below.

### 参数

`other`  
Instance of <span class="classname">EvLoop</span> . The loop to embed,
this loop must be embeddable(see <span
class="methodname">Ev::embeddableBackends</span> ).

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvEmbed object on success.

### 范例

**示例 \#1 Embedding loop created with kqueue backend into the default
loop**

``` php
<?php
/*
 * Check if kqueue is available but not recommended and create a kqueue backend
 * for use with sockets (which usually work with any kqueue implementation).
 * Store the kqueue/socket-only event loop in loop_socket. (One might optionally
 * use EVFLAG_NOENV, too)
 *
 * Example borrowed from
 * http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
 */
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
    if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
        $embed = new EvEmbed($loop);
    }
}

if (!$socket_loop) {
    $socket_loop = $loop;
}

// Now use $socket_loop for all sockets, and $loop for anything else
?>
```

### 参见

-   <span class="methodname">Ev::embeddableBackends</span>

EvEmbed::createStopped
======================

Create stopped EvEmbed watcher object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">EvEmbed::createStopped</span> ( <span
class="methodparam"> <span class="type">object</span> `$other` </span>
\[, <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\]\] )

The same as <span class="methodname">EvEmbed::\_\_construct</span> , but
doesn't start the watcher automatically.

### 参数

`other`  
The same as for <span class="methodname">EvEmbed::\_\_construct</span>

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns stopped EvEmbed object on success.

### 参见

-   <span class="methodname">EvEmbed::\_\_construct</span>
-   <span class="methodname">Ev::embeddableBackends</span>

EvEmbed::set
============

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvEmbed::set</span> ( <span
class="methodparam"> <span class="type">object</span> `$other` </span> )

Configures the watcher to use `other` event loop object.

### 参数

`other`  
The same as for <span class="methodname">EvEmbed::\_\_construct</span>

### 返回值

没有返回值。

EvEmbed::sweep
==============

Make a single, non-blocking sweep over the embedded loop

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvEmbed::sweep</span> ( <span
class="methodparam">void</span> )

Make a single, non-blocking sweep over the embedded loop. Works
similarly to the following, but in the most appropriate way for embedded
loops:

``` php
<?php
$other->start(Ev::RUN_NOWAIT);
?>
```

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvWatcher::start</span>

简介
----

Fork watchers are called when a *fork()* was detected (usually because
whoever signalled *libev* about it by calling <span
class="methodname">EvLoop::fork</span> ). The invocation is done before
the event loop blocks next and before <span
class="classname">EvCheck</span> watchers are being called, and only in
the child after the fork. Note, that if whoever calling <span
class="methodname">EvLoop::fork</span> calls it in the wrong process,
the fork handlers will be invoked, too.

类摘要
------

**EvFork**

<span class="ooclass"> class **EvFork** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

EvFork::\_\_construct
=====================

Constructs the EvFork watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvFork::\_\_construct</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Constructs the EvFork watcher object and starts the watcher
automatically.

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvFork object on success.

### 参见

-   <span class="methodname">EvLoop::fork</span>
-   <span class="classname">EvCheck</span>

EvFork::createStopped
=====================

Creates a stopped instance of EvFork watcher class

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">EvFork::createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\] )

The same as <span class="methodname">EvFork::\_\_construct</span> , but
doesn't start the watcher automatically.

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvFork(stopped) object on success.

### 参见

-   <span class="methodname">EvFork::\_\_construct</span>

简介
----

<span class="classname">EvIdle</span> watchers trigger events when no
other events of the same or higher priority are pending ( <span
class="classname">EvPrepare</span> , <span
class="classname">EvCheck</span> and other <span
class="classname">EvIdle</span> watchers do not count as receiving
*events* ).

Thus, as long as the process is busy handling sockets or timeouts(or
even signals) of the same or higher priority it will not be triggered.
But when the process is in idle(or only lower-priority watchers are
pending), the <span class="classname">EvIdle</span> watchers are being
called once per event loop iteration - until stopped, that is, or the
process receives more events and becomes busy again with higher priority
stuff.

Apart from keeping the process non-blocking(which is a useful on its own
sometimes), <span class="classname">EvIdle</span> watchers are a good
place to do *"pseudo-background processing"* , or delay processing stuff
to after the event loop has handled all outstanding events.

The most noticeable effect is that as long as any *idle* watchers are
active, the process will *not* block when waiting for new events.

类摘要
------

**EvIdle**

<span class="ooclass"> class **EvIdle** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$priority`
</span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` </span> \]\] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

EvIdle::\_\_construct
=====================

Constructs the EvIdle watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvIdle::\_\_construct</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` </span> \]\] )

Constructs the EvIdle watcher object and starts the watcher
automatically.

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvIdle object on success.

### 参见

-   <span class="methodname">EvIdle::createStopped</span>
-   <span class="methodname">EvLoop::idle</span>

EvIdle::createStopped
=====================

Creates instance of a stopped EvIdle watcher object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">EvIdle::createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` </span> \]\] )

The same as <span class="methodname">EvIdle::\_\_construct</span> , but
doesn't start the watcher automatically.

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvIdle object on success.

### 参见

-   <span class="methodname">EvIdle::\_\_construct</span>
-   <span class="methodname">EvLoop::idle</span>

简介
----

<span class="classname">EvIo</span> watchers check whether a file
descriptor(or socket, or a stream castable to numeric file descriptor)
is readable or writable in each iteration of the event loop, or, more
precisely, when reading would not block the process and writing would at
least be able to write some data. This behaviour is called
*level-triggering* because events are kept receiving as long as the
condition persists. To stop receiving events just stop the watcher.

The number of read and/or write event watchers per `fd` is unlimited.
Setting all file descriptors to non-blocking mode is also usually a good
idea(but not required).

Another thing to watch out for is that it is quite easy to receive false
readiness notifications, i.e. the callback might be called with
**`Ev::READ`** but a subsequent *read()* will actually block because
there is no data. It is very easy to get into this situation. Thus it is
best to always use non-blocking I/O: An extra *read()* returning
**`EAGAIN`** (or similar) is far preferable to a program hanging until
some data arrives.

If for some reason it is impossible to run the `fd` in non-blocking
mode, then separately re-test whether a file descriptor is really ready.
Some people additionally use **`SIGALRM`** and an interval timer, just
to be sure thry won't block infinitely.

Always consider using non-blocking mode.

类摘要
------

**EvIo**

<span class="ooclass"> class **EvIo** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$fd` ;

<span class="modifier">public</span> `$events` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">mixed</span> `$fd` </span> , <span
class="methodparam"> <span class="type">int</span> `$events` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvIo</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> ,
<span class="methodparam"> <span class="type">int</span> `$events`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">mixed</span> `$fd` </span> , <span class="methodparam">
<span class="type">int</span> `$events` </span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`fd`  

`events`  

EvIo::\_\_construct
===================

Constructs EvIo watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvIo::\_\_construct</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> ,
<span class="methodparam"> <span class="type">int</span> `$events`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \[, <span class="methodparam">
<span class="type">int</span> `$priority` </span> \]\] )

Constructs EvIo watcher object and starts the watcher automatically.

### 参数

`fd`  
Can be a stream opened with <span class="function">fopen</span> or
similar functions, numeric file descriptor, or socket.

`events`  
**`Ev::READ`** and/or **`Ev::WRITE`** . See
<a href="/class/ev.html#" class="link">the bit masks</a> .

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvIo object on success.

### 参见

-   <span class="methodname">EvIo::createStopped</span>
-   <span class="methodname">EvLoop::io</span>

EvIo::createStopped
===================

Create stopped EvIo watcher object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvIo</span>
<span class="methodname">EvIo::createStopped</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> ,
<span class="methodparam"> <span class="type">int</span> `$events`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

The same as <span class="methodname">EvIo::\_\_construct</span> , but
doesn't start the watcher automatically.

### 参数

`fd`  
The same as for <span class="methodname">EvIo::\_\_construct</span>

`events`  
The same as for <span class="methodname">EvIo::\_\_construct</span>

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvIo object on success.

### 参见

-   <span class="methodname">EvIo::\_\_construct</span>
-   <span class="methodname">EvLoop::io</span>

EvIo::set
=========

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvIo::set</span> ( <span class="methodparam">
<span class="type">mixed</span> `$fd` </span> , <span
class="methodparam"> <span class="type">int</span> `$events` </span> )

Configures the EvIo watcher

### 参数

`fd`  
The same as for <span class="methodname">EvIo::\_\_construct</span>

`events`  
The same as for <span class="methodname">EvIo::\_\_construct</span>

### 返回值

没有返回值。

简介
----

Represents an event loop that is always distinct from the *default loop*
. Unlike the *default loop* , it cannot handle <span
class="classname">EvChild</span> watchers.

Having threads we have to create a loop per thread, and use the *default
loop* in the parent thread.

The *default event loop* is initialized automatically by *Ev* . It is
accessible via methods of the <span class="classname">Ev</span> class,
or via <span class="methodname">EvLoop::defaultLoop</span> method.

类摘要
------

**EvLoop**

<span class="ooclass"> <span class="modifier">final</span> class
**EvLoop** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$backend` ;

<span class="modifier">public</span> `$is_default_loop` ;

<span class="modifier">public</span> `$iteration` ;

<span class="modifier">public</span> `$pending` ;

<span class="modifier">public</span> `$io_interval` ;

<span class="modifier">public</span> `$timeout_interval` ;

<span class="modifier">public</span> `$depth` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">backend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvCheck</span> <span class="methodname">check</span>
( <span class="methodparam"> <span class="type">string</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$data` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$priority`
</span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvChild</span> <span class="methodname">child</span>
( <span class="methodparam"> <span class="type">string</span> `$pid`
</span> , <span class="methodparam"> <span class="type">string</span>
`$trace` </span> , <span class="methodparam"> <span
class="type">string</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$data` </span>
\[, <span class="methodparam"> <span class="type">string</span>
`$priority` </span> \]\] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span class="methodparam">
<span class="type">int</span> `$flags` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = NULL</span> </span> \[, <span
class="methodparam"> <span class="type">float</span> `$io_interval`
<span class="initializer"> = 0.0</span> </span> \[, <span
class="methodparam"> <span class="type">float</span> `$timeout_interval`
<span class="initializer"> = 0.0</span> </span> \]\]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">EvLoop</span> <span
class="methodname">defaultLoop</span> (\[ <span class="methodparam">
<span class="type">int</span> `$flags` <span class="initializer"> =
Ev::FLAG\_AUTO</span> </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
NULL</span> </span> \[, <span class="methodparam"> <span
class="type">float</span> `$io_interval` <span class="initializer"> =
0.</span> </span> \[, <span class="methodparam"> <span
class="type">float</span> `$timeout_interval` <span class="initializer">
= 0.</span> </span> \]\]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvEmbed</span> <span class="methodname">embed</span>
( <span class="methodparam"> <span class="type">string</span> `$other`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$data` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$priority`
</span> \]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvFork</span> <span class="methodname">fork</span> (
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvIdle</span> <span class="methodname">idle</span> (
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">invokePending</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvIo</span> <span class="methodname">io</span> (
<span class="methodparam"> <span class="type">mixed</span> `$fd` </span>
, <span class="methodparam"> <span class="type">int</span> `$events`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">loopFork</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">now</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">nowUpdate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvPeriodic</span> <span
class="methodname">periodic</span> ( <span class="methodparam"> <span
class="type">float</span> `$offset` </span> , <span class="methodparam">
<span class="type">float</span> `$interval` </span> , <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvPrepare</span> <span
class="methodname">prepare</span> ( <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resume</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">run</span> (\[ <span class="methodparam"> <span
class="type">int</span> `$flags` <span class="initializer"> = 0</span>
</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvSignal</span> <span
class="methodname">signal</span> ( <span class="methodparam"> <span
class="type">int</span> `$signum` </span> , <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvStat</span> <span class="methodname">stat</span> (
<span class="methodparam"> <span class="type">string</span> `$path`
</span> , <span class="methodparam"> <span class="type">float</span>
`$interval` </span> , <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">stop</span> (\[ <span class="methodparam">
<span class="type">int</span> `$how` </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">suspend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvTimer</span> <span class="methodname">timer</span>
( <span class="methodparam"> <span class="type">float</span> `$after`
</span> , <span class="methodparam"> <span class="type">float</span>
`$repeat` </span> , <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">verify</span> ( <span
class="methodparam">void</span> )

}

属性
----

`data`  
Custom data attached to loop

`backend`  
*Readonly* . The
<a href="/class/ev.html#" class="link">backend flags</a> indicating the
event backend in use.

`is_default_loop`  
*Readonly* . **`TRUE`** if it is the default event loop.

`iteration`  
The current iteration count of the loop. See <span
class="methodname">Ev::iteration</span>

`pending`  
The number of pending watchers. **`0`** indicates that there are no
watchers pending.

`io_interval`  
Higher `io_interval` allows *libev* to spend more time collecting <span
class="classname">EvIo</span> events, so more events can be handled per
iteration, at the cost of increasing latency. Timeouts (both <span
class="classname">EvPeriodic</span> and <span
class="classname">EvTimer</span> ) will not be affected. Setting this to
a non-zero value will introduce an additional *sleep()* call into most
loop iterations. The sleep time ensures that *libev* will not poll for
<span class="classname">EvIo</span> events more often than once per this
interval, on average. Many programs can usually benefit by setting the
`io_interval` to a value near **`0.1`** , which is often enough for
interactive servers(not for games). It usually doesn't make much sense
to set it to a lower value than **`0.01`** , as this approaches the
timing granularity of most systems.

See also
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS" class="link external">» FUNCTIONS CONTROLLING EVENT LOOPS</a>
.

`timeout_interval`  
Higher `timeout_interval` allows *libev* to spend more time collecting
timeouts, at the expense of increased latency/jitter/inexactness(the
watcher callback will be called later). <span
class="classname">EvIo</span> watchers will not be affected. Setting
this to a non-null value will not introduce any overhead in *libev* .
See also
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS" class="link external">» FUNCTIONS CONTROLLING EVENT LOOPS</a>
.

`depth`  
The recursion depth. See <span class="methodname">Ev::depth</span> .

EvLoop::backend
===============

Returns an integer describing the backend used by libev

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvLoop::backend</span> ( <span
class="methodparam">void</span> )

The same as <span class="methodname">Ev::backend</span> , but for the
loop instance.

### 参数

此函数没有参数。

### 返回值

Returns an integer describing the backend used by libev. See <span
class="methodname">Ev::backend</span> .

### 参见

-   <span class="methodname">Ev::backend</span>

EvLoop::check
=============

Creates EvCheck object associated with the current event loop instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvCheck</span> <span
class="methodname">EvLoop::check</span> ( <span class="methodparam">
<span class="type">string</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$data` </span>
\[, <span class="methodparam"> <span class="type">string</span>
`$priority` </span> \]\] )

Creates EvCheck object associated with the current event loop instance.

### 参数

All parameters have the same meaning as for <span
class="methodname">EvCheck::\_\_construct</span>

### 返回值

Returns EvCheck object on success.

### 参见

-   <span class="methodname">EvCheck::\_\_construct</span>

EvLoop::child
=============

Creates EvChild object associated with the current event loop

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvChild</span> <span
class="methodname">EvLoop::child</span> ( <span class="methodparam">
<span class="type">string</span> `$pid` </span> , <span
class="methodparam"> <span class="type">string</span> `$trace` </span> ,
<span class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\] )

Creates EvChild object associated with the current event loop.

### 参数

All parameters have the same meaning as for <span
class="methodname">EvChild::\_\_construct</span>

### 返回值

Returns EvChild object on success.

### 参见

-   <span class="methodname">EvChild::\_\_construct</span>

EvLoop::\_\_construct
=====================

Constructs the event loop object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvLoop::\_\_construct</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$flags` </span> \[,
<span class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = NULL</span> </span> \[, <span
class="methodparam"> <span class="type">float</span> `$io_interval`
<span class="initializer"> = 0.0</span> </span> \[, <span
class="methodparam"> <span class="type">float</span> `$timeout_interval`
<span class="initializer"> = 0.0</span> </span> \]\]\]\] )

Constructs the event loop object.

### 参数

`flags`  
One of the <a href="/class/ev.html#" class="link">event loop flags</a>

`data`  
Custom data associated with the loop.

`io_interval`  
See <a href="/class/evloop.html#" class="link">io_interval</a>

`timeout_interval`  
See <a href="/class/evloop.html#" class="link">timeout_interval</a>

### 返回值

Returns new EvLoop object.

### 参见

-   <span class="methodname">EvLoop::defaultLoop</span>

EvLoop::defaultLoop
===================

Returns or creates the default event loop

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">EvLoop</span> <span
class="methodname">EvLoop::defaultLoop</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$flags` <span
class="initializer"> = Ev::FLAG\_AUTO</span> </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = NULL</span> </span> \[, <span
class="methodparam"> <span class="type">float</span> `$io_interval`
<span class="initializer"> = 0.</span> </span> \[, <span
class="methodparam"> <span class="type">float</span> `$timeout_interval`
<span class="initializer"> = 0.</span> </span> \]\]\]\] )

If the default event loop is not created, <span
class="methodname">EvLoop::defaultLoop</span> creates it with the
specified parameters. Otherwise, it just returns the object representing
previously created instance ignoring all the parameters.

### 参数

`flags`  
One of the <a href="/class/ev.html#" class="link">event loop flags</a>

`data`  
Custom data to associate with the loop.

`io_collect_interval`  
See <a href="/class/evloop.html#" class="link">io_interval</a>

`timeout_collect_interval`  
See <a href="/class/evloop.html#" class="link">timeout_interval</a>

### 返回值

Returns EvLoop object on success.

### 参见

-   <span class="methodname">EvLoop::\_\_construct</span>

EvLoop::embed
=============

Creates an instance of EvEmbed watcher associated with the current
EvLoop object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvEmbed</span> <span
class="methodname">EvLoop::embed</span> ( <span class="methodparam">
<span class="type">string</span> `$other` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\]\] )

Creates an instance of <span class="classname">EvEmbed</span> watcher
associated with the current <span class="classname">EvLoop</span>
object.

### 参数

All parameters have the same meaning as for <span
class="methodname">EvEmbed::\_\_construct</span> .

### 返回值

Returns EvEmbed object on success.

### 参见

-   <span class="methodname">EvEmbed::\_\_construct</span>

EvLoop::fork
============

Creates EvFork watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvFork</span> <span
class="methodname">EvLoop::fork</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Creates EvFork watcher object associated with the current event loop
instance

### 参数

All parameters have the same meaning as for <span
class="methodname">EvFork::\_\_construct</span>

### 返回值

Returns EvFork object on success.

### 参见

-   <span class="methodname">EvFork::\_\_construct</span>

EvLoop::idle
============

Creates EvIdle watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvIdle</span> <span
class="methodname">EvLoop::idle</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Creates EvIdle watcher object associated with the current event loop
instance

### 参数

All the parameters have the same meaning as for <span
class="methodname">EvIdle::\_\_construct</span>

### 返回值

Returns EvIdle object on success.

### 参见

-   <span class="methodname">EvIdle::\_\_construct</span>

EvLoop::invokePending
=====================

Invoke all pending watchers while resetting their pending state

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::invokePending</span> ( <span
class="methodparam">void</span> )

Invoke all pending watchers while resetting their pending state.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EvLoop::io
==========

Create EvIo watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvIo</span> <span
class="methodname">EvLoop::io</span> ( <span class="methodparam"> <span
class="type">mixed</span> `$fd` </span> , <span class="methodparam">
<span class="type">int</span> `$events` </span> , <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Create EvIo watcher object associated with the current event loop
instance.

### 参数

All parameters have the same meaning as for <span
class="methodname">EvIo::\_\_construct</span>

### 返回值

Returns EvIo object on success.

### 参见

-   <span class="methodname">EvIo::\_\_construct</span>

EvLoop::loopFork
================

Must be called after a fork

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::loopFork</span> ( <span
class="methodparam">void</span> )

Must be called after a *fork* in the child, before entering or
continuing the event loop. An alternative is to use
**`Ev::FLAG_FORKCHECK`** which calls this function automatically, at
some performance loss (refer to the
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS" class="link external">» libev documentation</a>
).

### 参数

此函数没有参数。

### 返回值

没有返回值。

EvLoop::now
===========

Returns the current "event loop time"

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">EvLoop::now</span> ( <span
class="methodparam">void</span> )

Returns the current "event loop time", which is the time the event loop
received events and started processing them. This timestamp does not
change as long as callbacks are being processed, and this is also the
base time used for relative timers. You can treat it as the timestamp of
the event occurring(or more correctly, libev finding out about it).

### 参数

此函数没有参数。

### 返回值

Returns time of the event loop in (fractional) seconds.

### 参见

-   <span class="methodname">Ev::now</span>

EvLoop::nowUpdate
=================

Establishes the current time by querying the kernel, updating the time
returned by EvLoop::now in the progress

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::nowUpdate</span> ( <span
class="methodparam">void</span> )

Establishes the current time by querying the kernel, updating the time
returned by <span class="methodname">EvLoop::now</span> in the progress.
This is a costly operation and is usually done automatically within
<span class="methodname">EvLoop::run</span> .

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvLoop::now</span>
-   <span class="methodname">Ev::nowUpdate</span>

EvLoop::periodic
================

Creates EvPeriodic watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvPeriodic</span> <span
class="methodname">EvLoop::periodic</span> ( <span class="methodparam">
<span class="type">float</span> `$offset` </span> , <span
class="methodparam"> <span class="type">float</span> `$interval` </span>
, <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Creates EvPeriodic watcher object associated with the current event loop
instance

### 参数

All parameters have the same maening as for <span
class="methodname">EvPeriodic::\_\_construct</span>

### 返回值

Returns EvPeriodic object on success.

### 参见

-   <span class="methodname">EvPeriodic::\_\_construct</span>

EvLoop::prepare
===============

Creates EvPrepare watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvPrepare</span> <span
class="methodname">EvLoop::prepare</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Creates EvPrepare watcher object associated with the current event loop
instance

### 参数

All parameters have the same maening as for <span
class="methodname">EvPrepare</span>

### 返回值

Returns EvPrepare object on success

### 参见

-   <span class="methodname">EvPrepare::\_\_construct</span>

EvLoop::resume
==============

Resume previously suspended default event loop

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::resume</span> ( <span
class="methodparam">void</span> )

<span class="methodname">EvLoop::suspend</span> and <span
class="methodname">EvLoop::resume</span> methods suspend and resume a
loop correspondingly.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvLoop::suspend</span>
-   <span class="methodname">Ev::resume</span>

EvLoop::run
===========

Begin checking for events and calling callbacks for the loop

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::run</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$flags` <span
class="initializer"> = 0</span> </span> \] )

Begin checking for events and calling callbacks for the current event
loop. Returns when a callback calls <span
class="methodname">Ev::stop</span> method, or the flags are nonzero(in
which case the return value is true) or when there are no active
watchers which reference the loop( <span
class="methodname">EvWatcher::keepalive</span> is **`TRUE`**), in which
case the return value will be **`FALSE`**. The return value can
generally be interpreted as *if **`TRUE`**, there is more work left to
do* .

### 参数

`flags`  
Optional parameter `flags` can be one of the following:

| `flags`              | Description                                             |
|----------------------|---------------------------------------------------------|
| **`0`**              | The default behavior described above                    |
| **`Ev::RUN_ONCE`**   | Block at most one(wait, but don't loop)                 |
| **`Ev::RUN_NOWAIT`** | Don't block at all(fetch/handle events, but don't wait) |

See <a href="/class/ev.html#" class="link">the run flag constants</a> .

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvLoop::stop</span>
-   <span class="methodname">Ev::run</span>

EvLoop::signal
==============

Creates EvSignal watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvSignal</span> <span
class="methodname">EvLoop::signal</span> ( <span class="methodparam">
<span class="type">int</span> `$signum` </span> , <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Creates EvSignal watcher object associated with the current event loop
instance

### 参数

All parameters have the same meaning as for <span
class="methodname">EvSignal::\_\_construct</span>

### 返回值

Returns EvSignal object on success

### 参见

-   <span class="methodname">EvSignal::\_\_construct</span>

EvLoop::stat
============

Creates EvStat watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvStat</span> <span
class="methodname">EvLoop::stat</span> ( <span class="methodparam">
<span class="type">string</span> `$path` </span> , <span
class="methodparam"> <span class="type">float</span> `$interval` </span>
, <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Creates EvStat watcher object associated with the current event loop
instance

### 参数

All parameters have the same meaning as for <span
class="methodname">EvSignal::\_\_construct</span>

### 返回值

Returns EvStat object on success

### 参见

-   <span class="methodname">EvSignal::\_\_construct</span>

EvLoop::stop
============

Stops the event loop

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::stop</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$how` </span> \] )

Stops the event loop

### 参数

`how`  
One of *Ev::BREAK\_\**
<a href="/class/ev.html#" class="link">constants</a> .

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvLoop::run</span>
-   <span class="methodname">Ev::stop</span>

EvLoop::suspend
===============

Suspend the loop

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::suspend</span> ( <span
class="methodparam">void</span> )

<span class="methodname">EvLoop::suspend</span> and <span
class="methodname">EvLoop::resume</span> methods suspend and resume a
loop correspondingly.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvLoop::resume</span>
-   <span class="methodname">Ev::suspend</span>

EvLoop::timer
=============

Creates EvTimer watcher object associated with the current event loop
instance

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">EvTimer</span> <span
class="methodname">EvLoop::timer</span> ( <span class="methodparam">
<span class="type">float</span> `$after` </span> , <span
class="methodparam"> <span class="type">float</span> `$repeat` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Creates EvTimer watcher object associated with the current event loop
instance

### 参数

All parameters have the same meaning as for <span
class="methodname">EvTimer::\_\_construct</span>

### 返回值

Returns EvTimer object on success

### 参见

-   <span class="methodname">EvTimer::\_\_construct</span>

EvLoop::verify
==============

Performs internal consistency checks(for debugging)

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvLoop::verify</span> ( <span
class="methodparam">void</span> )

Performs internal consistency checks(for debugging *libev* ) and abort
the program if any data structures were found to be corrupted.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Ev::verify</span>

简介
----

Periodic watchers are also timers of a kind, but they are very
versatile.

Unlike <span class="classname">EvTimer</span> , <span
class="classname">EvPeriodic</span> watchers are not based on real
time(or relative time, the physical time that passes) but on wall clock
time(absolute time, calendar or clock). The difference is that wall
clock time can run faster or slower than real time, and time jumps are
not uncommon(e.g. when adjusting it).

<span class="classname">EvPeriodic</span> watcher can be configured to
trigger after some specific point in time. For example, if an <span
class="classname">EvPeriodic</span> watcher is configured to trigger
*"in 10 seconds"* (e.g. <span class="methodname">EvLoop::now</span> +
**`10.0`** , i.e. an absolute time, not a delay), and the system clock
is reset to *January of the previous year* , then it will take a year or
more to trigger the event (unlike an <span
class="classname">EvTimer</span> , which would still trigger roughly
**`10`** seconds after starting it as it uses a relative timeout).

As with timers, the callback is guaranteed to be invoked only when the
point in time where it is supposed to trigger has passed. If multiple
timers become ready during the same loop iteration then the ones with
earlier time-out values are invoked before ones with later time-out
values (but this is no longer true when a callback calls <span
class="methodname">EvLoop::run</span> recursively).

类摘要
------

**EvPeriodic**

<span class="ooclass"> class **EvPeriodic** </span> <span
class="ooclass"> <span class="modifier">extends</span> **EvWatcher**
</span> {

/\* 属性 \*/

<span class="modifier">public</span> `$offset` ;

<span class="modifier">public</span> `$interval` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">again</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">at</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">float</span> `$offset` </span> , <span
class="methodparam"> <span class="type">string</span> `$interval`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$reschedule_cb` </span> , <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span
class="type">EvPeriodic</span> <span
class="methodname">createStopped</span> ( <span class="methodparam">
<span class="type">float</span> `$offset` </span> , <span
class="methodparam"> <span class="type">float</span> `$interval` </span>
, <span class="methodparam"> <span class="type">callable</span>
`$reschedule_cb` </span> , <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">float</span> `$offset` </span> , <span class="methodparam">
<span class="type">float</span> `$interval` </span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`offset`  
When repeating, this contains the offset value, otherwise this is the
absolute point in time(the offset value passed to <span
class="methodname">EvPeriodic::set</span> , although *libev* might
modify this value for better numerical stability).

`interval`  
The current interval value. Can be modified any time, but changes only
take effect when the periodic timer fires or <span
class="methodname">EvPeriodic::again</span> is being called.

EvPeriodic::again
=================

Simply stops and restarts the periodic watcher again

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvPeriodic::again</span> ( <span
class="methodparam">void</span> )

Simply stops and restarts the periodic watcher again. This is only
useful when attributes are changed.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvTimer::again</span>

EvPeriodic::at
==============

Returns the absolute time that this watcher is supposed to trigger next

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">EvPeriodic::at</span> ( <span
class="methodparam">void</span> )

When the watcher is active, returns the absolute time that this watcher
is supposed to trigger next. This is not the same as the offset argument
to <span class="methodname">EvPeriodic::set</span> or <span
class="methodname">EvPeriodic::\_\_construct</span> , but indeed works
even in interval mode.

### 参数

此函数没有参数。

### 返回值

Returns the absolute time this watcher is supposed to trigger next in
seconds.

EvPeriodic::\_\_construct
=========================

Constructs EvPeriodic watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvPeriodic::\_\_construct</span> ( <span
class="methodparam"> <span class="type">float</span> `$offset` </span> ,
<span class="methodparam"> <span class="type">string</span> `$interval`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$reschedule_cb` </span> , <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Constructs EvPeriodic watcher object and starts it automatically. <span
class="methodname">EvPeriodic::createStopped</span> method creates
stopped periodic watcher.

### 参数

`offset`  
See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`interval`  
See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`reschedule_cb`  
Reschedule callback. You can pass **`NULL`**. See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvPeriodic object on success.

### 范例

**示例 \#1 Periodic timer. Use reschedule callback**

``` php
<?php
// Tick each 10.5 seconds

function reschedule_cb ($watcher, $now) {
 return $now + (10.5. - fmod($now, 10.5));
}

$w = new EvPeriodic(0., 0., "reschedule_cb", function ($w, $revents) {
 echo time(), PHP_EOL;
});
Ev::run();
?>
```

**示例 \#2 Periodic timer. Tick every 10.5 seconds starting at now**

``` php
<?php
// Tick every 10.5 seconds starting at now
$w = new EvPeriodic(fmod(Ev::now(), 10.5), 10.5, NULL, function ($w, $revents) {
 echo time(), PHP_EOL;
});
Ev::run();
?>
```

**示例 \#3 Hourly watcher**

``` php
<?php
$hourly = EvPeriodic(0, 3600, NULL, function () {
 echo "once per hour\n";
});
?>
```

### 参见

-   <a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>
-   <span class="classname">EvTimer</span>
-   <span class="methodname">EvPeriodic::createStopped</span>

EvPeriodic::createStopped
=========================

Create a stopped EvPeriodic watcher

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span
class="type">EvPeriodic</span> <span
class="methodname">EvPeriodic::createStopped</span> ( <span
class="methodparam"> <span class="type">float</span> `$offset` </span> ,
<span class="methodparam"> <span class="type">float</span> `$interval`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$reschedule_cb` </span> , <span class="methodparam"> <span
class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Create EvPeriodic object. Unlike <span
class="methodname">EvPeriodic::\_\_construct</span> this method doesn't
start the watcher automatically.

### 参数

`offset`  
See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`interval`  
See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`reschedule_cb`  
Reschedule callback. You can pass **`NULL`**. See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvPeriodic watcher object on success.

### 参见

-   <span class="methodname">EvPeriodic::\_\_construct</span>
-   <span class="methodname">EvTimer::createStopped</span>

EvPeriodic::set
===============

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvPeriodic::set</span> ( <span
class="methodparam"> <span class="type">float</span> `$offset` </span> ,
<span class="methodparam"> <span class="type">float</span> `$interval`
</span> )

(Re-)Configures EvPeriodic watcher

### 参数

`offset`  
The same meaning as for <span
class="methodname">EvPeriodic::\_\_construct</span> . See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

`interval`  
The same meaning as for <span
class="methodname">EvPeriodic::\_\_construct</span> . See
<a href="/ev/periodic-modes.html" class="link">Periodic watcher operation modes</a>

### 返回值

没有返回值。

简介
----

<span class="classname">EvPrepare</span> and <span
class="classname">EvCheck</span> watchers are usually used in pairs.
<span class="classname">EvPrepare</span> watchers get invoked before the
process blocks, <span class="classname">EvCheck</span> afterwards.

It is not allowed to call <span class="methodname">EvLoop::run</span> or
similar methods or functions that enter the current event loop from
either <span class="classname">EvPrepare</span> or <span
class="classname">EvCheck</span> watchers. Other loops than the current
one are fine, however. The rationale behind this is that one don't need
to check for recursion in those watchers, i.e. the sequence will always
be: <span class="classname">EvPrepare</span> -\> blocking -\> <span
class="classname">EvCheck</span> , so having a watcher of each kind they
will always be called in pairs bracketing the blocking call.

The main purpose is to integrate other event mechanisms into *libev* and
their use is somewhat advanced. They could be used, for example, to
track variable changes, implement custom watchers, integrate net-snmp or
a coroutine library and lots more. They are also occasionally useful to
cache some data and want to flush it before blocking.

It is recommended to give <span class="classname">EvCheck</span>
watchers highest( **`Ev::MAXPRI`** ) priority, to ensure that they are
being run before any other watchers after the poll (this doesn’t matter
for <span class="classname">EvPrepare</span> watchers).

Also, <span class="classname">EvCheck</span> watchers should not
activate/feed events. While *libev* fully supports this, they might get
executed before other <span class="classname">EvCheck</span> watchers
did their job.

类摘要
------

**EvPrepare**

<span class="ooclass"> class **EvPrepare** </span> <span
class="ooclass"> <span class="modifier">extends</span> **EvWatcher**
</span> {

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">string</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$data` </span>
\[, <span class="methodparam"> <span class="type">string</span>
`$priority` </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvPrepare</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

EvPrepare::\_\_construct
========================

Constructs EvPrepare watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvPrepare::\_\_construct</span> ( <span
class="methodparam"> <span class="type">string</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$data` </span> \[, <span class="methodparam"> <span
class="type">string</span> `$priority` </span> \]\] )

Constructs EvPrepare watcher object. And starts the watcher
automatically. If need a stopped watcher consider using <span
class="methodname">EvPrepare::createStopped</span>

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvPrepare object on success.

### 参见

-   <span class="classname">EvCheck</span>

EvPrepare::createStopped
========================

Creates a stopped instance of EvPrepare watcher

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvPrepare</span>
<span class="methodname">EvPrepare::createStopped</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

Creates a stopped instance of EvPrepare watcher. Unlike <span
class="methodname">EvPrepare::\_\_construct</span> , this method doesn'
start the watcher automatically.

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Return EvPrepare object on success.

### 参见

-   <span class="methodname">EvPrepare::\_\_construct</span>
-   <span class="methodname">EvWatcher::start</span>

简介
----

<span class="classname">EvSignal</span> watchers will trigger an event
when the process receives a specific signal one or more times. Even
though signals are very asynchronous, *libev* will try its best to
deliver signals synchronously, i.e. as part of the normal event
processing, like any other event.

There is no limit for the number of watchers for the same signal, but
only within the same loop, i.e. one can watch for **`SIGINT`** in the
default loop and for **`SIGIO`** in another loop, but it is not allowed
to watch for **`SIGINT`** in both the default loop and another loop at
the same time. At the moment, **`SIGCHLD`** is permanently tied to the
default loop.

If possible and supported, *libev* will install its handlers with
*SA\_RESTART* (or equivalent) behaviour enabled, so system calls should
not be unduly interrupted. In case of a problem with system calls
getting interrupted by signals, all the signals can be blocked in an
<span class="classname">EvCheck</span> watcher and unblocked in a <span
class="classname">EvPrepare</span> watcher.

类摘要
------

**EvSignal**

<span class="ooclass"> class **EvSignal** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$signum` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">int</span> `$signum` </span> , <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$priority` <span
class="initializer"> = 0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvSignal</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">int</span> `$signum` </span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`signum`  
Signal number. See the constants exported by *pcntl* extension. See also
*signal(7)* man page.

EvSignal::\_\_construct
=======================

Constructs EvSignal watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvSignal::\_\_construct</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Constructs EvSignal watcher object and starts it automatically. For a
stopped periodic watcher consider using <span
class="methodname">EvSignal::createStopped</span> method.

### 参数

`signum`  
Signal number. See constants exported by *pcntl* extension. See also
*signal(7)* man page.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvSignal object on success.

### 范例

**示例 \#1 Handle SIGTERM signal**

``` php
<?php
$w = new EvSignal(SIGTERM, function ($watcher) {
    echo "SIGTERM received\n";
    $watcher->stop();
});

Ev::run();
?>
```

### 参见

-   <span class="methodname">EvSignal::createStopped</span>

EvSignal::createStopped
=======================

Create stopped EvSignal watcher object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvSignal</span>
<span class="methodname">EvSignal::createStopped</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Create stopped EvSignal watcher object. Unlike <span
class="methodname">EvSignal::\_\_construct</span> , this method does't
start the watcher automatically.

### 参数

`signum`  
Signal number. See constants exported by *pcntl* extension. See also
*signal(7)* man page.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvSignal object on success.

### 参见

-   <span class="methodname">EvWatcher::start</span>
-   <span class="methodname">EvSignal::\_\_construct</span>

EvSignal::set
=============

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvSignal::set</span> ( <span
class="methodparam"> <span class="type">int</span> `$signum` </span> )

Configures the watcher.

### 参数

`signum`  
Signal number. The same as for <span
class="methodname">EvSignal::\_\_construct</span>

### 返回值

没有返回值。

简介
----

<span class="classname">EvStat</span> monitors a file system path for
attribute changes. It calls *stat()* on that path in regular
intervals(or when the OS signals it changed) and sees if it changed
compared to the last time, invoking the callback if it did.

The path does not need to exist: changing from "path exists" to "path
does not exist" is a status change like any other. The condition "path
does not exist" is signified by the **`'nlink'`** item being 0(returned
by <span class="methodname">EvStat::attr</span> method).

The path must not end in a slash or contain special components such as
**`'.'`** or **`..`** . The path should be absolute: if it is relative
and the working directory changes, then the behaviour is undefined.

Since there is no portable change notification interface available, the
portable implementation simply calls *stat()* regularly on the path to
see if it changed somehow. For this case a recommended polling interval
can be specified. If one specifies a polling interval of **`0.0 `**
(highly recommended) then a suitable, unspecified default value will be
used(which could be expected to be around 5 seconds, although this might
change dynamically). *libev* will also impose a minimum interval which
is currently around **`0.1`** , but that’s usually overkill.

This watcher type is not meant for massive numbers of <span
class="classname">EvStat</span> watchers, as even with OS-supported
change notifications, this can be resource-intensive.

类摘要
------

**EvStat**

<span class="ooclass"> class **EvStat** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$path` ;

<span class="modifier">public</span> `$interval` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">attr</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">string</span> `$path` </span> , <span
class="methodparam"> <span class="type">float</span> `$interval` </span>
, <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$path` </span> ,
<span class="methodparam"> <span class="type">float</span> `$interval`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">prev</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">string</span> `$path` </span> , <span class="methodparam">
<span class="type">float</span> `$interval` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stat</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`interval`  
*Readonly* . Hint on how quickly a change is expected to be detected and
should normally be specified as **`0.0`** to let *libev* choose a
suitable value.

`path`  
*Readonly* . The path to wait for status changes on.

EvStat::attr
============

Returns the values most recently detected by Ev

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">EvStat::attr</span> ( <span
class="methodparam">void</span> )

Returns array of the values most recently detected by Ev

### 参数

此函数没有参数。

### 返回值

Returns array with the values most recently detect by Ev(without actual
*stat* 'ing):

| Key             | Description                     |
|-----------------|---------------------------------|
| **`'dev'`**     | ID of device containing file    |
| **`'ino'`**     | inode number                    |
| **`'mode'`**    | protection                      |
| **`'nlink'`**   | number of hard links            |
| **`'uid'`**     | user ID of owner                |
| **`'size'`**    | total size, in bytes            |
| **`'gid'`**     | group ID of owner               |
| **`'rdev'`**    | device ID (if special file)     |
| **`'blksize'`** | blocksize for file system I/O   |
| **`'blocks'`**  | number of 512B blocks allocated |
| **`'atime'`**   | time of last access             |
| **`'ctime'`**   | time of last status change      |
| **`'mtime'`**   | time of last modification       |

See *stat(2)* man page for details.

### 范例

**示例 \#1 Monitor changes of /var/log/messages**

``` php
<?php
// Use 10 second update interval.
$w = new EvStat("/var/log/messages", 8, function ($w) {
    echo "/var/log/messages changed\n";

    $attr = $w->attr();

    if ($attr['nlink']) {
        printf("Current size: %ld\n", $attr['size']);
        printf("Current atime: %ld\n", $attr['atime']);
        printf("Current mtime: %ld\n", $attr['mtime']);
    } else {
        fprintf(STDERR, "`messages` file is not there!");
        $w->stop();
    }
});

Ev::run();
?>
```

### 参见

-   <span class="methodname">EvStat::prev</span>
-   <span class="methodname">EvStat::stat</span>

EvStat::\_\_construct
=====================

Constructs EvStat watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvStat::\_\_construct</span> ( <span
class="methodparam"> <span class="type">string</span> `$path` </span> ,
<span class="methodparam"> <span class="type">float</span> `$interval`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Constructs EvStat watcher object and starts the watcher automatically.

### 参数

`path`  
The path to wait for status changes on.

`interval`  
Hint on how quickly a change is expected to be detected and should
normally be specified as **`0.0`** to let *libev* choose a suitable
value.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvStat watcher object on succes.

### 范例

**示例 \#1 Monitor changes of /var/log/messages**

``` php
<?php
// Use 10 second update interval.
$w = new EvStat("/var/log/messages", 8, function ($w) {
 echo "/var/log/messages changed\n";

 $attr = $w->attr();

 if ($attr['nlink']) {
  printf("Current size: %ld\n", $attr['size']);
  printf("Current atime: %ld\n", $attr['atime']);
  printf("Current mtime: %ld\n", $attr['mtime']);
 } else {
  fprintf(STDERR, "`messages` file is not there!");
  $w->stop();
 }
});

Ev::run();
?>
```

EvStat::createStopped
=====================

Create a stopped EvStat watcher object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">EvStat::createStopped</span> ( <span
class="methodparam"> <span class="type">string</span> `$path` </span> ,
<span class="methodparam"> <span class="type">float</span> `$interval`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Creates EvStat watcher object, but doesn't start it automatically(unlike
<span class="methodname">EvStat::\_\_construct</span> ).

### 参数

`path`  
The path to wait for status changes on.

`interval`  
Hint on how quickly a change is expected to be detected and should
normally be specified as **`0.0`** to let *libev* choose a suitable
value.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns a stopped EvStat watcher object on success.

### 参见

-   <span class="methodname">EvStat::\_\_construct</span>
-   <span class="methodname">EvWatcher::start</span>

EvStat::prev
============

Returns the previous set of values returned by EvStat::attr

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvStat::prev</span> ( <span
class="methodparam">void</span> )

Just like <span class="methodname">EvStat::attr</span> , but returns the
previous set of values.

### 参数

此函数没有参数。

### 返回值

Returns an array with the same structure as the array returned by <span
class="methodname">EvStat::attr</span> . The array contains previously
detected values.

### 参见

-   <span class="methodname">EvStat::attr</span>
-   <span class="methodname">EvStat::stat</span>

EvStat::set
===========

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvStat::set</span> ( <span class="methodparam">
<span class="type">string</span> `$path` </span> , <span
class="methodparam"> <span class="type">float</span> `$interval` </span>
)

Configures the watcher.

### 参数

`path`  
The path to wait for status changes on.

`interval`  
Hint on how quickly a change is expected to be detected and should
normally be specified as **`0.0`** to let *libev* choose a suitable
value.

### 返回值

没有返回值。

EvStat::stat
============

Initiates the stat call

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvStat::stat</span> ( <span
class="methodparam">void</span> )

Initiates the stat call(updates internal cache). It stats(using *lstat*
) the `path` specified in the watcher and sets to the values found.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if `path` exists. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EvStat::attr</span>
-   <span class="methodname">EvStat::prev</span>

简介
----

<span class="classname">EvTimer</span> watchers are simple relative
timers that generate an event after a given time, and optionally
repeating in regular intervals after that.

The timers are based on real time, that is, if one registers an event
that times out after an hour and resets the system clock to *January
last year* , it will still time out after(roughly) one hour. "Roughly"
because detecting time jumps is hard, and some inaccuracies are
unavoidable.

The callback is guaranteed to be invoked only after its timeout has
passed (not at, so on systems with very low-resolution clocks this might
introduce a small delay). If multiple timers become ready during the
same loop iteration then the ones with earlier time-out values are
invoked before ones of the same priority with later time-out values (but
this is no longer true when a callback calls <span
class="methodname">EvLoop::run</span> recursively).

The timer itself will do a best-effort at avoiding drift, that is, if a
timer is configured to trigger every **`10`** seconds, then it will
normally trigger at exactly **`10`** second intervals. If, however, the
script cannot keep up with the timer because it takes longer than those
**`10`** seconds to do) the timer will not fire more than once per event
loop iteration.

类摘要
------

**EvTimer**

<span class="ooclass"> class **EvTimer** </span> <span class="ooclass">
<span class="modifier">extends</span> **EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$repeat` ;

<span class="modifier">public</span> `$remaining` ;

/\* 继承的属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">again</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">float</span> `$after` </span> , <span
class="methodparam"> <span class="type">float</span> `$repeat` </span> ,
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvTimer</span>
<span class="methodname">createStopped</span> ( <span
class="methodparam"> <span class="type">float</span> `$after` </span> ,
<span class="methodparam"> <span class="type">float</span> `$repeat`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">float</span> `$after` </span> , <span class="methodparam">
<span class="type">float</span> `$repeat` </span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`repeat`  
If repeat is **`0.0`** , then it will automatically be stopped once the
timeout is reached. If it is positive, then the timer will automatically
be configured to trigger again every repeat seconds later, until stopped
manually.

`remaining`  
Returns the remaining time until a timer fires. If the timer is active,
then this time is relative to the current event loop time, otherwise
it's the timeout value currently configured.

That is, after instanciating an <span class="classname">EvTimer</span>
with an `after` value of **`5.0`** and `repeat` value of **`7.0`** ,
`remaining` returns **`5.0`** . When the timer is started and one second
passes, `remaining` will return **`4.0`** . When the timer expires and
is restarted, it will return roughly **`7.0`** (likely slightly less as
callback invocation takes some time too), and so on.

EvTimer::again
==============

Restarts the timer watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvTimer::again</span> ( <span
class="methodparam">void</span> )

This will act as if the timer timed out and restart it again if it is
repeating. The exact semantics are:

1.  if the timer is pending, its pending status is cleared.

2.  if the timer is started but non-repeating, stop it (as if it timed
    out).

3.  if the timer is repeating, either start it if necessary (with the
    `repeat` value), or reset the running timer to the `repeat` value.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvWatcher::stop</span>

EvTimer::\_\_construct
======================

Constructs an EvTimer watcher object

### 说明

<span class="modifier">public</span> <span
class="methodname">EvTimer::\_\_construct</span> ( <span
class="methodparam"> <span class="type">float</span> `$after` </span> ,
<span class="methodparam"> <span class="type">float</span> `$repeat`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Constructs an EvTimer watcher object.

### 参数

`after`  
Configures the timer to trigger after `after` seconds.

`repeat`  
If repeat is **`0.0`** , then it will automatically be stopped once the
timeout is reached. If it is positive, then the timer will automatically
be configured to trigger again every repeat seconds later, until stopped
manually.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvTimer object on success.

### 范例

**示例 \#1 Simple timers**

``` php
<?php
// Create and start timer firing after 2 seconds
$w1 = new EvTimer(2, 0, function () {
    echo "2 seconds elapsed\n";
});

// Create and launch timer firing after 2 seconds repeating each second
// until we manually stop it
$w2 = new EvTimer(2, 1, function ($w) {
    echo "is called every second, is launched after 2 seconds\n";
    echo "iteration = ", Ev::iteration(), PHP_EOL;

    // Stop the watcher after 5 iterations
    Ev::iteration() == 5 and $w->stop();
    // Stop the watcher if further calls cause more than 10 iterations
    Ev::iteration() >= 10 and $w->stop();
});

// Create stopped timer. It will be inactive until we start it ourselves
$w_stopped = EvTimer::createStopped(10, 5, function($w) {
    echo "Callback of a timer created as stopped\n";

    // Stop the watcher after 2 iterations
    Ev::iteration() >= 2 and $w->stop();
});

// Loop until Ev::stop() is called or all of watchers stop
Ev::run();

// Start and look if it works
$w_stopped->start();
echo "Run single iteration\n";
Ev::run(Ev::RUN_ONCE);

echo "Restart the second watcher and try to handle the same events, but don't block\n";
$w2->again();
Ev::run(Ev::RUN_NOWAIT);

$w = new EvTimer(10, 0, function() {});
echo "Running a blocking loop\n";
Ev::run();
echo "END\n";
?>
```

以上例程的输出类似于：

    2 seconds elapsed
    is called every second, is launched after 2 seconds
    iteration = 1
    is called every second, is launched after 2 seconds
    iteration = 2
    is called every second, is launched after 2 seconds
    iteration = 3
    is called every second, is launched after 2 seconds
    iteration = 4
    is called every second, is launched after 2 seconds
    iteration = 5
    Run single iteration
    Callback of a timer created as stopped
    Restart the second watcher and try to handle the same events, but don't block
    Running a blocking loop
    is called every second, is launched after 2 seconds
    iteration = 8
    is called every second, is launched after 2 seconds
    iteration = 9
    is called every second, is launched after 2 seconds
    iteration = 10
    END

### 参见

-   <span class="methodname">EvTimer::createStopped</span>
-   <span class="classname">EvPeriodic</span>
-   <a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_timer_code_relative_and_opti" class="link external">» ev_timer - relative and optionally repeating timeouts</a>
-   <a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Be_smart_about_timeouts" class="link external">» Be smart about timeouts</a>

EvTimer::createStopped
======================

Creates EvTimer stopped watcher object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">EvTimer</span>
<span class="methodname">EvTimer::createStopped</span> ( <span
class="methodparam"> <span class="type">float</span> `$after` </span> ,
<span class="methodparam"> <span class="type">float</span> `$repeat`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$priority` <span class="initializer"> =
0</span> </span> \]\] )

Creates EvTimer stopped watcher object. Unlike <span
class="methodname">EvTimer::\_\_construct</span> , this method doesn't
start the watcher automatically.

### 参数

`after`  
Configures the timer to trigger after `after` seconds.

`repeat`  
If repeat is **`0.0`** , then it will automatically be stopped once the
timeout is reached. If it is positive, then the timer will automatically
be configured to trigger again every repeat seconds later, until stopped
manually.

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

`data`  
Custom data associated with the watcher.

`priority`  
<a href="/class/ev.html#" class="link">Watcher priority</a>

### 返回值

Returns EvTimer watcher object on success.

### 范例

**示例 \#1 Monotor changes of /var/log/messages. Avoid missing updates
by means of one second delay**

``` php
<?php
$timer = EvTimer::createStopped(0., 1.02, function ($w) {
    $w->stop();

    $stat = $w->data;

    // 1 second after the most recent change of the file
    printf("Current size: %ld\n", $stat->attr()['size']);
});

$stat = new EvStat("/var/log/messages", 0., function () use ($timer) {
    // Reset timer watcher
    $timer->again();
});

$timer->data = $stat;

Ev::run();
?>
```

### 参见

-   <span class="methodname">EvTimer::\_\_construct</span>
-   <span class="classname">EvPeriodic</span>

EvTimer::set
============

Configures the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvTimer::set</span> ( <span
class="methodparam"> <span class="type">float</span> `$after` </span> ,
<span class="methodparam"> <span class="type">float</span> `$repeat`
</span> )

Configures the watcher

### 参数

`after`  
Configures the timer to trigger after `after` seconds.

`repeat`  
If repeat is **`0.0`** , then it will automatically be stopped once the
timeout is reached. If it is positive, then the timer will automatically
be configured to trigger again every repeat seconds later, until stopped
manually.

### 返回值

没有返回值。

简介
----

<span class="classname">EvWatcher</span> is a base class for all
watchers( <span class="classname">EvCheck</span> , <span
class="classname">EvChild</span> etc.). Since <span
class="classname">EvWatcher</span> 's constructor is <span
class="modifier">abstract</span> , one can't(and don't need to) create
EvWatcher objects directly.

类摘要
------

**EvWatcher**

<span class="ooclass"> <span class="modifier">abstract</span> class
**EvWatcher** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$is_active` ;

<span class="modifier">public</span> `$data` ;

<span class="modifier">public</span> `$is_pending` ;

<span class="modifier">public</span> `$priority` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">clear</span> ( <span class="methodparam">void</span>
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">feed</span> ( <span class="methodparam"> <span
class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">getLoop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">invoke</span> ( <span class="methodparam">
<span class="type">int</span> `$revents` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">keepalive</span> (\[ <span class="methodparam">
<span class="type">bool</span> `$value` </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCallback</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">stop</span> ( <span
class="methodparam">void</span> )

}

属性
----

`is_active`  
*Readonly* . **`TRUE`** if the watcher is active. **`FALSE`** otherwise.

`data`  
User custom data associated with the watcher

`is_pending`  
*Readonly* .**`TRUE`** if the watcher is pending, i.e. it has
outstanding events, but its callback has not yet been invoked.
**`FALSE`** otherwise. As long, as a watcher is pending(but not active),
one must *not* change its priority.

`priority`  
<span class="type">Integer</span> between **`Ev::MINPRI`** and
**`Ev::MAXPRI`** . Pending watchers with higher priority will be invoked
before watchers with lower priority, but priority will not keep watchers
from being executed(except for <span class="classname">EvIdle</span>
watchers). <span class="classname">EvIdle</span> watchers provide
functionality to suppress invocation when higher priority events are
pending.

EvWatcher::clear
================

Clear watcher pending status

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EvWatcher::clear</span> ( <span
class="methodparam">void</span> )

If the watcher is pending, this method clears its `pending` status and
returns its `revents` bitset(as if its callback was invoked). If the
watcher isn't pending it does nothing and returns **`0`** .

Sometimes it can be useful to "poll" a watcher instead of waiting for
its callback to be invoked, which can be accomplished with this
function.

### 参数

此函数没有参数。

### 返回值

In case if the watcher is pending, returns `revents` bitset as if the
<a href="/ev/watcher-callbacks.html" class="link">watcher callback</a>
had been invoked. Otherwise returns **`0`** .

EvWatcher::\_\_construct
========================

Abstract constructor of a watcher object

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EvWatcher::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="methodname">EvWatcher::\_\_construct</span> is an abstract
constructor of a watcher object implemented in the derived classes.

EvWatcher::feed
===============

Feeds the given revents set into the event loop

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::feed</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

Feeds the given revents set into the event loop, as if the specified
event had happened for the watcher.

### 参数

`revents`  
Bit mask of watcher
<a href="/class/ev.html#" class="link">received events</a> .

### 返回值

没有返回值。

EvWatcher::getLoop
==================

Returns the loop responsible for the watcher

### 说明

<span class="modifier">public</span> <span class="type">EvLoop</span>
<span class="methodname">EvWatcher::getLoop</span> ( <span
class="methodparam">void</span> )

Returns the loop responsible for the watcher

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">EvLoop</span> event loop object
responsible for the watcher.

EvWatcher::invoke
=================

Invokes the watcher callback with the given received events bit mask

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::invoke</span> ( <span
class="methodparam"> <span class="type">int</span> `$revents` </span> )

Invokes the watcher callback with the given received events bit mask.

### 参数

`revents`  
Bit mask of watcher
<a href="/class/ev.html#" class="link">received events</a> .

### 返回值

没有返回值。

EvWatcher::keepalive
====================

Configures whether to keep the loop from returning

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EvWatcher::keepalive</span> (\[ <span
class="methodparam"> <span class="type">bool</span> `$value` </span> \]
)

Configures whether to keep the loop from returning. With keepalive
`value` set to **`FALSE`** the watcher won't keep <span
class="methodname">Ev::run</span> / <span
class="methodname">EvLoop::run</span> from returning even though the
watcher is active.

Watchers have keepalive `value` **`TRUE`** by default.

Clearing keepalive status is useful when returning from <span
class="methodname">Ev::run</span> / <span
class="methodname">EvLoop::run</span> just because of the watcher is
undesirable. It could be a long running UDP socket watcher or so.

### 参数

`value`  
With keepalive `value` set to **`FALSE`** the watcher won't keep <span
class="methodname">Ev::run</span> / <span
class="methodname">EvLoop::run</span> from returning even though the
watcher is active.

### 返回值

Returns the previous state.

### 范例

**示例 \#1 Register an I/O watcher for some UDP socket but do not keep
the event loop from running just because of that watcher.**

``` php
<?php
$udp_socket = ...
$udp_watcher = new EvIo($udp_socket, Ev::READ, function () { /* ... */ });
$udp_watcher->keepalive(FALSE);
?>
```

EvWatcher::setCallback
======================

Sets new callback for the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> )

Sets new callback for the watcher

### 参数

`callback`  
See
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

### 返回值

没有返回值。

EvWatcher::start
================

Starts the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::start</span> ( <span
class="methodparam">void</span> )

Marks the watcher as active. Note that only active watchers will receive
events.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvWatcher::stop</span>

EvWatcher::stop
===============

Stops the watcher

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EvWatcher::stop</span> ( <span
class="methodparam">void</span> )

Marks the watcher as inactive. Note that only active watchers will
receive events.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EvWatcher::start</span>
