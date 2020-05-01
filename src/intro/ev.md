This extension provides inteface to
<a href="http://software.schmorp.de/pkg/libev.html" class="link external">» libev</a>
library - a high performance full-featured event loop written in C.

> **Note**: <span class="simpara">此扩展在 Windows 平台上不可用。</span>

*Libev* is an event loop: one registers interest in certain events (such
as a file descriptor being readable or a timeout occurring), and it will
manage these event sources and provide the program with events.

To do this, it must take more or less complete control over the process
(or thread) by executing the event loop handler, and will then
communicate events via a callback mechanism.

You register interest in certain events by registering so-called event
watchers, and then hand it over to libev by starting the watcher.

For details refer to the
<a href="http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod" class="link external">» documentation of libev</a>
