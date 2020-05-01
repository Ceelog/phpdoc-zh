Event flags
===========

**`Event::READ`** This flag indicates an event that becomes active when
the provided file descriptor (usually a stream resource, or socket) is
ready for reading.

**`Event::WRITE`** flag indicates an event that becomes active when the
provided file descriptor (usually a stream resource, or socket) is ready
for writing.

**`Event::SIGNAL`** used to implement signal detection. See
"Constructing signal events" below.

**`Event::TIMEOUT`** indicates an event that becomes active after a
timeout elapses. The **`Event::TIMEOUT`** flag is ignored when
constructing an event: one can either set a timeout when event is
*added* , or not. It is set in the *$what* argument to the callback
function when a timeout has occurred.

See also
<a href="http://www.wangafu.net/~nickm/libevent-book/Ref4_event.html#_the_event_flags" class="link external">» Fast portable non-blocking network programming with Libevent, Working with events, Event flags</a>
