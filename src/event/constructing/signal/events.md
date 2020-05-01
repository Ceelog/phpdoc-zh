Constructing signal events
==========================

Event can also watch for POSIX-style signals. To construct a handler for
a signal, use <span class="methodname">Event::\_\_construct</span>
constructor with **`Event::SIGNAL`** flag, or <span
class="methodname">Event::signal</span> factory method.

**示例 \#1 Handling *SIGTERM* signal**

``` php
<?php
/*
Launch it in a terminal window:

$ php examples/signal.php

In another terminal window find out the pid and send SIGTERM, e.g.:

$ ps aux | grep examp
ruslan    3976  0.2  0.0 139896 11256 pts/1    S+   10:25   0:00 php examples/signal.php
ruslan    3978  0.0  0.0   9572   864 pts/2    S+   10:26   0:00 grep --color=auto examp
$ kill -TERM 3976

At the first terminal window you should catch the following:

Caught signal 15
*/
class MyEventSignal {
    private $base, $ev;

    public function __construct($base) {
        $this->base = $base;
        $this->ev = Event::signal($base, SIGTERM, array($this, 'eventSighandler'));
        $this->ev->add();
    }

    public function eventSighandler($no, $c) {
        echo "Caught signal $no\n";
        $this->base->exit();
    }
}

$base = new EventBase();
$c    = new MyEventSignal($base);

$base->loop();
?>
```

Note that signal callbacks are run in the event loop after the signal
occurs, so it is safe for them to call functions that you are not
supposed to call from a regular POSIX signal handler.

See also
<a href="http://www.wangafu.net/~nickm/libevent-book/Ref4_event.html#_constructing_signal_events" class="link external">» Fast portable non-blocking network programming with Libevent, Constructing Signal Events</a>
.
