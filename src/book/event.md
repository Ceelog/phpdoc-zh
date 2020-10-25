Event
=====

**目录**

-   [简介](/intro/event.html)
-   [安装／配置](/event/setup.html)
    -   [需求](/event/setup.html#需求)
    -   [安装](/event/setup.html#安装)
    -   [运行时配置](/event/setup.html#运行时配置)
    -   [资源类型](/event/setup.html#资源类型)
-   [范例](/event/examples.html)
-   [Event flags](/event/flags.html)
-   [About event persistence](/event/persistence.html)
-   [Event callbacks](/event/callbacks.html)
-   [Constructing signal events](/event/constructing/signal/events.html)
-   [Event](/class/event.html) — The Event class
    -   [Event::add](/class/event.html#Event::add) — Makes event pending
    -   [Event::addSignal](/class/event.html#Event::addSignal) — Makes
        signal event pending
    -   [Event::addTimer](/class/event.html#Event::addTimer) — Makes
        timer event pending
    -   [Event::\_\_construct](/class/event.html#Event::__construct) —
        Constructs Event object
    -   [Event::del](/class/event.html#Event::del) — Makes event
        non-pending
    -   [Event::delSignal](/class/event.html#Event::delSignal) — Makes
        signal event non-pending
    -   [Event::delTimer](/class/event.html#Event::delTimer) — Makes
        timer event non-pending
    -   [Event::free](/class/event.html#Event::free) — Make event
        non-pending and free resources allocated for this event
    -   [Event::getSupportedMethods](/class/event.html#Event::getSupportedMethods)
        — Returns array with of the names of the methods supported in
        this version of Libevent
    -   [Event::pending](/class/event.html#Event::pending) — Detects
        whether event is pending or scheduled
    -   [Event::set](/class/event.html#Event::set) — Re-configures event
    -   [Event::setPriority](/class/event.html#Event::setPriority) — Set
        event priority
    -   [Event::setTimer](/class/event.html#Event::setTimer) —
        Re-configures timer event
    -   [Event::signal](/class/event.html#Event::signal) — Constructs
        signal event object
    -   [Event::timer](/class/event.html#Event::timer) — Constructs
        timer event object
-   [EventBase](/class/eventbase.html) — The EventBase class
    -   [EventBase::\_\_construct](/class/eventbase.html#EventBase::__construct)
        — Constructs EventBase object
    -   [EventBase::dispatch](/class/eventbase.html#EventBase::dispatch)
        — Dispatch pending events
    -   [EventBase::exit](/class/eventbase.html#EventBase::exit) — Stop
        dispatching events
    -   [EventBase::free](/class/eventbase.html#EventBase::free) — Free
        resources allocated for this event base
    -   [EventBase::getFeatures](/class/eventbase.html#EventBase::getFeatures)
        — Returns bitmask of features supported
    -   [EventBase::getMethod](/class/eventbase.html#EventBase::getMethod)
        — Returns event method in use
    -   [EventBase::getTimeOfDayCached](/class/eventbase.html#EventBase::getTimeOfDayCached)
        — Returns the current event base time
    -   [EventBase::gotExit](/class/eventbase.html#EventBase::gotExit) —
        Checks if the event loop was told to exit
    -   [EventBase::gotStop](/class/eventbase.html#EventBase::gotStop) —
        Checks if the event loop was told to exit
    -   [EventBase::loop](/class/eventbase.html#EventBase::loop) —
        Dispatch pending events
    -   [EventBase::priorityInit](/class/eventbase.html#EventBase::priorityInit)
        — Sets number of priorities per event base
    -   [EventBase::reInit](/class/eventbase.html#EventBase::reInit) —
        Re-initialize event base(after a fork)
    -   [EventBase::stop](/class/eventbase.html#EventBase::stop) — Tells
        event\_base to stop dispatching events
-   [EventBuffer](/class/eventbuffer.html) — The EventBuffer class
    -   [EventBuffer::add](/class/eventbuffer.html#EventBuffer::add) —
        Append data to the end of an event buffer
    -   [EventBuffer::addBuffer](/class/eventbuffer.html#EventBuffer::addBuffer)
        — Move all data from a buffer provided to the current instance
        of EventBuffer
    -   [EventBuffer::appendFrom](/class/eventbuffer.html#EventBuffer::appendFrom)
        — Moves the specified number of bytes from a source buffer to
        the end of the current buffer
    -   [EventBuffer::\_\_construct](/class/eventbuffer.html#EventBuffer::__construct)
        — Constructs EventBuffer object
    -   [EventBuffer::copyout](/class/eventbuffer.html#EventBuffer::copyout)
        — Copies out specified number of bytes from the front of the
        buffer
    -   [EventBuffer::drain](/class/eventbuffer.html#EventBuffer::drain)
        — Removes specified number of bytes from the front of the buffer
        without copying it anywhere
    -   [EventBuffer::enableLocking](/class/eventbuffer.html#EventBuffer::enableLocking)
        — 说明
    -   [EventBuffer::expand](/class/eventbuffer.html#EventBuffer::expand)
        — Reserves space in buffer
    -   [EventBuffer::freeze](/class/eventbuffer.html#EventBuffer::freeze)
        — Prevent calls that modify an event buffer from succeeding
    -   [EventBuffer::lock](/class/eventbuffer.html#EventBuffer::lock) —
        Acquires a lock on buffer
    -   [EventBuffer::prepend](/class/eventbuffer.html#EventBuffer::prepend)
        — Prepend data to the front of the buffer
    -   [EventBuffer::prependBuffer](/class/eventbuffer.html#EventBuffer::prependBuffer)
        — Moves all data from source buffer to the front of current
        buffer
    -   [EventBuffer::pullup](/class/eventbuffer.html#EventBuffer::pullup)
        — Linearizes data within buffer and returns it's contents as a
        string
    -   [EventBuffer::read](/class/eventbuffer.html#EventBuffer::read) —
        Read data from an evbuffer and drain the bytes read
    -   [EventBuffer::readFrom](/class/eventbuffer.html#EventBuffer::readFrom)
        — Read data from a file onto the end of the buffer
    -   [EventBuffer::readLine](/class/eventbuffer.html#EventBuffer::readLine)
        — Extracts a line from the front of the buffer
    -   [EventBuffer::search](/class/eventbuffer.html#EventBuffer::search)
        — Scans the buffer for an occurrence of a string
    -   [EventBuffer::searchEol](/class/eventbuffer.html#EventBuffer::searchEol)
        — Scans the buffer for an occurrence of an end of line
    -   [EventBuffer::substr](/class/eventbuffer.html#EventBuffer::substr)
        — Substracts a portion of the buffer data
    -   [EventBuffer::unfreeze](/class/eventbuffer.html#EventBuffer::unfreeze)
        — Re-enable calls that modify an event buffer
    -   [EventBuffer::unlock](/class/eventbuffer.html#EventBuffer::unlock)
        — Releases lock acquired by EventBuffer::lock
    -   [EventBuffer::write](/class/eventbuffer.html#EventBuffer::write)
        — Write contents of the buffer to a file or socket
-   [EventBufferEvent](/class/eventbufferevent.html) — The
    EventBufferEvent class
    -   [EventBufferEvent::close](/class/eventbufferevent.html#EventBufferEvent::close)
        — Closes file descriptor associated with the current buffer
        event
    -   [EventBufferEvent::connect](/class/eventbufferevent.html#EventBufferEvent::connect)
        — Connect buffer event's file descriptor to given address or
        UNIX socket
    -   [EventBufferEvent::connectHost](/class/eventbufferevent.html#EventBufferEvent::connectHost)
        — Connects to a hostname with optionally asyncronous DNS
        resolving
    -   [EventBufferEvent::\_\_construct](/class/eventbufferevent.html#EventBufferEvent::__construct)
        — Constructs EventBufferEvent object
    -   [EventBufferEvent::createPair](/class/eventbufferevent.html#EventBufferEvent::createPair)
        — Creates two buffer events connected to each other
    -   [EventBufferEvent::disable](/class/eventbufferevent.html#EventBufferEvent::disable)
        — Disable events read, write, or both on a buffer event
    -   [EventBufferEvent::enable](/class/eventbufferevent.html#EventBufferEvent::enable)
        — Enable events read, write, or both on a buffer event
    -   [EventBufferEvent::free](/class/eventbufferevent.html#EventBufferEvent::free)
        — Free a buffer event
    -   [EventBufferEvent::getDnsErrorString](/class/eventbufferevent.html#EventBufferEvent::getDnsErrorString)
        — Returns string describing the last failed DNS lookup attempt
    -   [EventBufferEvent::getEnabled](/class/eventbufferevent.html#EventBufferEvent::getEnabled)
        — Returns bitmask of events currently enabled on the buffer
        event
    -   [EventBufferEvent::getInput](/class/eventbufferevent.html#EventBufferEvent::getInput)
        — Returns underlying input buffer associated with current buffer
        event
    -   [EventBufferEvent::getOutput](/class/eventbufferevent.html#EventBufferEvent::getOutput)
        — Returns underlying output buffer associated with current
        buffer event
    -   [EventBufferEvent::read](/class/eventbufferevent.html#EventBufferEvent::read)
        — Read buffer's data
    -   [EventBufferEvent::readBuffer](/class/eventbufferevent.html#EventBufferEvent::readBuffer)
        — Drains the entire contents of the input buffer and places them
        into buf
    -   [EventBufferEvent::setCallbacks](/class/eventbufferevent.html#EventBufferEvent::setCallbacks)
        — Assigns read, write and event(status) callbacks
    -   [EventBufferEvent::setPriority](/class/eventbufferevent.html#EventBufferEvent::setPriority)
        — Assign a priority to a bufferevent
    -   [EventBufferEvent::setTimeouts](/class/eventbufferevent.html#EventBufferEvent::setTimeouts)
        — Set the read and write timeout for a buffer event
    -   [EventBufferEvent::setWatermark](/class/eventbufferevent.html#EventBufferEvent::setWatermark)
        — Adjusts read and/or write watermarks
    -   [EventBufferEvent::sslError](/class/eventbufferevent.html#EventBufferEvent::sslError)
        — Returns most recent OpenSSL error reported on the buffer event
    -   [EventBufferEvent::sslFilter](/class/eventbufferevent.html#EventBufferEvent::sslFilter)
        — Create a new SSL buffer event to send its data over another
        buffer event
    -   [EventBufferEvent::sslGetCipherInfo](/class/eventbufferevent.html#EventBufferEvent::sslGetCipherInfo)
        — Returns a textual description of the cipher
    -   [EventBufferEvent::sslGetCipherName](/class/eventbufferevent.html#EventBufferEvent::sslGetCipherName)
        — Returns the current cipher name of the SSL connection
    -   [EventBufferEvent::sslGetCipherVersion](/class/eventbufferevent.html#EventBufferEvent::sslGetCipherVersion)
        — Returns version of cipher used by current SSL connection
    -   [EventBufferEvent::sslGetProtocol](/class/eventbufferevent.html#EventBufferEvent::sslGetProtocol)
        — Returns the name of the protocol used for current SSL
        connection
    -   [EventBufferEvent::sslRenegotiate](/class/eventbufferevent.html#EventBufferEvent::sslRenegotiate)
        — Tells a bufferevent to begin SSL renegotiation
    -   [EventBufferEvent::sslSocket](/class/eventbufferevent.html#EventBufferEvent::sslSocket)
        — Creates a new SSL buffer event to send its data over an SSL on
        a socket
    -   [EventBufferEvent::write](/class/eventbufferevent.html#EventBufferEvent::write)
        — Adds data to a buffer event's output buffer
    -   [EventBufferEvent::writeBuffer](/class/eventbufferevent.html#EventBufferEvent::writeBuffer)
        — Adds contents of the entire buffer to a buffer event's output
        buffer
-   [About buffer event
    callbacks](/eventbufferevent/about/callbacks.html)
-   [EventConfig](/class/eventconfig.html) — The EventConfig class
    -   [EventConfig::avoidMethod](/class/eventconfig.html#EventConfig::avoidMethod)
        — Tells libevent to avoid specific event method
    -   [EventConfig::\_\_construct](/class/eventconfig.html#EventConfig::__construct)
        — Constructs EventConfig object
    -   [EventConfig::requireFeatures](/class/eventconfig.html#EventConfig::requireFeatures)
        — Enters a required event method feature that the application
        demands
    -   [EventConfig::setMaxDispatchInterval](/class/eventconfig.html#EventConfig::setMaxDispatchInterval)
        — Prevents priority inversion
-   [EventDnsBase](/class/eventdnsbase.html) — The EventDnsBase class
    -   [EventDnsBase::addNameserverIp](/class/eventdnsbase.html#EventDnsBase::addNameserverIp)
        — Adds a nameserver to the DNS base
    -   [EventDnsBase::addSearch](/class/eventdnsbase.html#EventDnsBase::addSearch)
        — Adds a domain to the list of search domains
    -   [EventDnsBase::clearSearch](/class/eventdnsbase.html#EventDnsBase::clearSearch)
        — Removes all current search suffixes
    -   [EventDnsBase::\_\_construct](/class/eventdnsbase.html#EventDnsBase::__construct)
        — Constructs EventDnsBase object
    -   [EventDnsBase::countNameservers](/class/eventdnsbase.html#EventDnsBase::countNameservers)
        — Gets the number of configured nameservers
    -   [EventDnsBase::loadHosts](/class/eventdnsbase.html#EventDnsBase::loadHosts)
        — Loads a hosts file (in the same format as /etc/hosts) from
        hosts file
    -   [EventDnsBase::parseResolvConf](/class/eventdnsbase.html#EventDnsBase::parseResolvConf)
        — Scans the resolv.conf-formatted file
    -   [EventDnsBase::setOption](/class/eventdnsbase.html#EventDnsBase::setOption)
        — Set the value of a configuration option
    -   [EventDnsBase::setSearchNdots](/class/eventdnsbase.html#EventDnsBase::setSearchNdots)
        — Set the 'ndots' parameter for searches
-   [EventHttp](/class/eventhttp.html) — The EventHttp class
    -   [EventHttp::accept](/class/eventhttp.html#EventHttp::accept) —
        Makes an HTTP server accept connections on the specified socket
        stream or resource
    -   [EventHttp::addServerAlias](/class/eventhttp.html#EventHttp::addServerAlias)
        — Adds a server alias to the HTTP server object
    -   [EventHttp::bind](/class/eventhttp.html#EventHttp::bind) — Binds
        an HTTP server on the specified address and port
    -   [EventHttp::\_\_construct](/class/eventhttp.html#EventHttp::__construct)
        — Constructs EventHttp object(the HTTP server)
    -   [EventHttp::removeServerAlias](/class/eventhttp.html#EventHttp::removeServerAlias)
        — Removes server alias
    -   [EventHttp::setAllowedMethods](/class/eventhttp.html#EventHttp::setAllowedMethods)
        — Sets the what HTTP methods are supported in requests accepted
        by this server, and passed to user callbacks
    -   [EventHttp::setCallback](/class/eventhttp.html#EventHttp::setCallback)
        — Sets a callback for specified URI
    -   [EventHttp::setDefaultCallback](/class/eventhttp.html#EventHttp::setDefaultCallback)
        — Sets default callback to handle requests that are not caught
        by specific callbacks
    -   [EventHttp::setMaxBodySize](/class/eventhttp.html#EventHttp::setMaxBodySize)
        — Sets maximum request body size
    -   [EventHttp::setMaxHeadersSize](/class/eventhttp.html#EventHttp::setMaxHeadersSize)
        — Sets maximum HTTP header size
    -   [EventHttp::setTimeout](/class/eventhttp.html#EventHttp::setTimeout)
        — Sets the timeout for an HTTP request
-   [EventHttpConnection](/class/eventhttpconnection.html) — The
    EventHttpConnection class
    -   [EventHttpConnection::\_\_construct](/class/eventhttpconnection.html#EventHttpConnection::__construct)
        — Constructs EventHttpConnection object
    -   [EventHttpConnection::getBase](/class/eventhttpconnection.html#EventHttpConnection::getBase)
        — Returns event base associated with the connection
    -   [EventHttpConnection::getPeer](/class/eventhttpconnection.html#EventHttpConnection::getPeer)
        — Gets the remote address and port associated with the
        connection
    -   [EventHttpConnection::makeRequest](/class/eventhttpconnection.html#EventHttpConnection::makeRequest)
        — Makes an HTTP request over the specified connection
    -   [EventHttpConnection::setCloseCallback](/class/eventhttpconnection.html#EventHttpConnection::setCloseCallback)
        — Set callback for connection close
    -   [EventHttpConnection::setLocalAddress](/class/eventhttpconnection.html#EventHttpConnection::setLocalAddress)
        — Sets the IP address from which HTTP connections are made
    -   [EventHttpConnection::setLocalPort](/class/eventhttpconnection.html#EventHttpConnection::setLocalPort)
        — Sets the local port from which connections are made
    -   [EventHttpConnection::setMaxBodySize](/class/eventhttpconnection.html#EventHttpConnection::setMaxBodySize)
        — Sets maximum body size for the connection
    -   [EventHttpConnection::setMaxHeadersSize](/class/eventhttpconnection.html#EventHttpConnection::setMaxHeadersSize)
        — Sets maximum header size
    -   [EventHttpConnection::setRetries](/class/eventhttpconnection.html#EventHttpConnection::setRetries)
        — Sets the retry limit for the connection
    -   [EventHttpConnection::setTimeout](/class/eventhttpconnection.html#EventHttpConnection::setTimeout)
        — Sets the timeout for the connection
-   [EventHttpRequest](/class/eventhttprequest.html) — The
    EventHttpRequest class
    -   [EventHttpRequest::addHeader](/class/eventhttprequest.html#EventHttpRequest::addHeader)
        — Adds an HTTP header to the headers of the request
    -   [EventHttpRequest::cancel](/class/eventhttprequest.html#EventHttpRequest::cancel)
        — Cancels a pending HTTP request
    -   [EventHttpRequest::clearHeaders](/class/eventhttprequest.html#EventHttpRequest::clearHeaders)
        — Removes all output headers from the header list of the request
    -   [EventHttpRequest::closeConnection](/class/eventhttprequest.html#EventHttpRequest::closeConnection)
        — Closes associated HTTP connection
    -   [EventHttpRequest::\_\_construct](/class/eventhttprequest.html#EventHttpRequest::__construct)
        — Constructs EventHttpRequest object
    -   [EventHttpRequest::findHeader](/class/eventhttprequest.html#EventHttpRequest::findHeader)
        — Finds the value belonging a header
    -   [EventHttpRequest::free](/class/eventhttprequest.html#EventHttpRequest::free)
        — Frees the object and removes associated events
    -   [EventHttpRequest::getBufferEvent](/class/eventhttprequest.html#EventHttpRequest::getBufferEvent)
        — Returns EventBufferEvent object
    -   [EventHttpRequest::getCommand](/class/eventhttprequest.html#EventHttpRequest::getCommand)
        — Returns the request command(method)
    -   [EventHttpRequest::getConnection](/class/eventhttprequest.html#EventHttpRequest::getConnection)
        — Returns EventHttpConnection object
    -   [EventHttpRequest::getHost](/class/eventhttprequest.html#EventHttpRequest::getHost)
        — Returns the request host
    -   [EventHttpRequest::getInputBuffer](/class/eventhttprequest.html#EventHttpRequest::getInputBuffer)
        — Returns the input buffer
    -   [EventHttpRequest::getInputHeaders](/class/eventhttprequest.html#EventHttpRequest::getInputHeaders)
        — Returns associative array of the input headers
    -   [EventHttpRequest::getOutputBuffer](/class/eventhttprequest.html#EventHttpRequest::getOutputBuffer)
        — Returns the output buffer of the request
    -   [EventHttpRequest::getOutputHeaders](/class/eventhttprequest.html#EventHttpRequest::getOutputHeaders)
        — Returns associative array of the output headers
    -   [EventHttpRequest::getResponseCode](/class/eventhttprequest.html#EventHttpRequest::getResponseCode)
        — Returns the response code
    -   [EventHttpRequest::getUri](/class/eventhttprequest.html#EventHttpRequest::getUri)
        — Returns the request URI
    -   [EventHttpRequest::removeHeader](/class/eventhttprequest.html#EventHttpRequest::removeHeader)
        — Removes an HTTP header from the headers of the request
    -   [EventHttpRequest::sendError](/class/eventhttprequest.html#EventHttpRequest::sendError)
        — Send an HTML error message to the client
    -   [EventHttpRequest::sendReply](/class/eventhttprequest.html#EventHttpRequest::sendReply)
        — Send an HTML reply to the client
    -   [EventHttpRequest::sendReplyChunk](/class/eventhttprequest.html#EventHttpRequest::sendReplyChunk)
        — Send another data chunk as part of an ongoing chunked reply
    -   [EventHttpRequest::sendReplyEnd](/class/eventhttprequest.html#EventHttpRequest::sendReplyEnd)
        — Complete a chunked reply, freeing the request as appropriate
    -   [EventHttpRequest::sendReplyStart](/class/eventhttprequest.html#EventHttpRequest::sendReplyStart)
        — Initiate a chunked reply
-   [EventListener](/class/eventlistener.html) — The EventListener class
    -   [EventListener::\_\_construct](/class/eventlistener.html#EventListener::__construct)
        — Creates new connection listener associated with an event base
    -   [EventListener::disable](/class/eventlistener.html#EventListener::disable)
        — Disables an event connect listener object
    -   [EventListener::enable](/class/eventlistener.html#EventListener::enable)
        — Enables an event connect listener object
    -   [EventListener::getBase](/class/eventlistener.html#EventListener::getBase)
        — Returns event base associated with the event listener
    -   [EventListener::getSocketName](/class/eventlistener.html#EventListener::getSocketName)
        — Retreives the current address to which the listener's socket
        is bound
    -   [EventListener::setCallback](/class/eventlistener.html#EventListener::setCallback)
        — The setCallback purpose
    -   [EventListener::setErrorCallback](/class/eventlistener.html#EventListener::setErrorCallback)
        — Set event listener's error callback
-   [EventSslContext](/class/eventsslcontext.html) — The EventSslContext
    class
    -   [EventSslContext::\_\_construct](/class/eventsslcontext.html#EventSslContext::__construct)
        — Constructs an OpenSSL context for use with Event classes
-   [EventUtil](/class/eventutil.html) — The EventUtil class
    -   [EventUtil::\_\_construct](/class/eventutil.html#EventUtil::__construct)
        — The abstract constructor
    -   [EventUtil::getLastSocketErrno](/class/eventutil.html#EventUtil::getLastSocketErrno)
        — Returns the most recent socket error number
    -   [EventUtil::getLastSocketError](/class/eventutil.html#EventUtil::getLastSocketError)
        — Returns the most recent socket error
    -   [EventUtil::getSocketFd](/class/eventutil.html#EventUtil::getSocketFd)
        — Returns numeric file descriptor of a socket, or stream
    -   [EventUtil::getSocketName](/class/eventutil.html#EventUtil::getSocketName)
        — Retreives the current address to which the socket is bound
    -   [EventUtil::setSocketOption](/class/eventutil.html#EventUtil::setSocketOption)
        — Sets socket options
    -   [EventUtil::sslRandPoll](/class/eventutil.html#EventUtil::sslRandPoll)
        — Generates entropy by means of OpenSSL's RAND\_poll()

简介
----

<span class="classname">Event</span> class represents and event firing
on a file descriptor being ready to read from or write to; a file
descriptor becoming ready to read from or write to(edge-triggered I/O
only); a timeout expiring; a signal occuring; a user-triggered event.

Every event is associated with <span class="classname">EventBase</span>
. However, event will never fire until it is *added* (via <span
class="methodname">Event::add</span> ). An added event remains in
*pending* state until the registered event occurs, thus turning it to
*active* state. To handle events user may register a callback which is
called when event becomes active. If event is configured *persistent* ,
it remains pending. If it is not persistent, it stops being pending when
it's callback runs. <span class="methodname">Event::del</span> method
*deletes* event, thus making it non-pending. By means of <span
class="methodname">Event::add</span> method it could be added again.

类摘要
------

**Event**

<span class="ooclass"> <span class="modifier">final</span> class
**Event** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`Event::ET` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Event::PERSIST` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Event::READ` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Event::WRITE` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Event::SIGNAL` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`Event::TIMEOUT` <span class="initializer"> = 1</span> ;

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">bool</span>
`$pending` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> (\[ <span class="methodparam"> <span
class="type">float</span> `$timeout` </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addSignal</span> (\[ <span class="methodparam">
<span class="type">float</span> `$timeout` </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addTimer</span> (\[ <span class="methodparam">
<span class="type">float</span> `$timeout` </span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> ,
<span class="methodparam"> <span class="type">int</span> `$what` </span>
, <span class="methodparam"> <span class="type">callable</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` <span class="initializer"> = NULL</span> </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">del</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delSignal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delTimer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">free</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getSupportedMethods</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">pending</span> ( <span class="methodparam">
<span class="type">int</span> `$flags` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set</span> ( <span class="methodparam"> <span
class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$what` </span>
\[, <span class="methodparam"> <span class="type">callable</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` </span> \]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setPriority</span> ( <span class="methodparam">
<span class="type">int</span> `$priority` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimer</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">callable</span> `$cb` </span>
\[, <span class="methodparam"> <span class="type">mixed</span> `$arg`
</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Event</span> <span
class="methodname">signal</span> ( <span class="methodparam"> <span
class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">int</span> `$signum` </span> ,
<span class="methodparam"> <span class="type">callable</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` </span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Event</span> <span
class="methodname">timer</span> ( <span class="methodparam"> <span
class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">callable</span> `$cb` </span>
\[, <span class="methodparam"> <span class="type">mixed</span> `$arg`
</span> \] )

}

属性
----

`pending`  
Whether event is pending. See
<a href="/event/persistence.html" class="link">About event persistence</a>
.

预定义常量
----------

**`Event::ET`**  
Indicates that the event should be edge-triggered, if the underlying
event base backend supports edge-triggered events. This affects the
semantics of **`Event::READ`** and **`Event::WRITE`** .

**`Event::PERSIST`**  
Indicates that the event is persistent. See
<a href="/event/persistence.html" class="link">About event persistence</a>
.

**`Event::READ`**  
This flag indicates an event that becomes active when the provided file
descriptor(usually a stream resource, or socket) is ready for reading.

**`Event::WRITE`**  
This flag indicates an event that becomes active when the provided file
descriptor(usually a stream resource, or socket) is ready for reading.

**`Event::SIGNAL`**  
Used to implement signal detection. See "Constructing signal events"
below.

**`Event::TIMEOUT`**  
This flag indicates an event that becomes active after a timeout
elapses.

The **`Event::TIMEOUT`** flag is ignored when constructing an event: one
can either set a timeout when event is *added* , or not. It is set in
the *$what* argument to the callback function when a timeout has
occurred.

Event::add
==========

Makes event pending

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::add</span> (\[ <span
class="methodparam"> <span class="type">float</span> `$timeout` </span>
\] )

Marks event pending. Non-pending event will never occur, and the event
callback will never be called. In conjuction with <span
class="methodname">Event::del</span> an event could be re-scheduled by
user at any time.

If <span class="methodname">Event::add</span> is called on an already
pending event, libevent will leave it pending and re-schedule it with
the given timeout(if specified). If in this case timeout is not
specified, <span class="methodname">Event::add</span> has no effect.

### 参数

`timeout`  
Timeout in seconds.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**

### 参见

-   <span class="methodname">Event::addSignal</span>
-   <span class="methodname">Event::addTimer</span>
-   <span class="methodname">Event::del</span>

Event::addSignal
================

Makes signal event pending

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::addSignal</span> (\[ <span
class="methodparam"> <span class="type">float</span> `$timeout` </span>
\] )

<span class="methodname">Event::addSignal</span> is an alias of <span
class="methodname">Event::add</span>

### 范例

**示例 \#1 <span class="function">Event::addSignal</span> example**

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
        $this->ev->addSignal();
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

以上例程的输出类似于：

    Caught signal 15

### 参见

-   <span class="methodname">Event::add</span>
-   <span class="methodname">Event::del</span>
-   <span class="methodname">Event::delSignal</span>
-   <span class="methodname">Event::signal</span>

Event::addTimer
===============

Makes timer event pending

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::addTimer</span> (\[ <span
class="methodparam"> <span class="type">float</span> `$timeout` </span>
\] )

<span class="methodname">Event::addTimer</span> is an alias of <span
class="methodname">Event::add</span>

### 返回值

### 范例

**示例 \#1 <span class="function">Event::addTimer</span> example**

``` php
<?php
$base = new EventBase();
$n = 2;
$e = Event::timer($base, function($n) use (&$e) {
    echo "$n seconds elapsed\n";
    $e->delTimer();
}, $n);
$e->addTimer($n);
$base->loop();
?>
```

以上例程的输出类似于：

    2 seconds elapsed

### 参见

-   <span class="methodname">Event::add</span>
-   <span class="methodname">Event::del</span>
-   <span class="methodname">Event::delTimer</span>

Event::\_\_construct
====================

Constructs Event object

### 说明

<span class="modifier">public</span> <span
class="methodname">Event::\_\_construct</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">mixed</span> `$fd`
</span> , <span class="methodparam"> <span class="type">int</span>
`$what` </span> , <span class="methodparam"> <span
class="type">callable</span> `$cb` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$arg` <span
class="initializer"> = NULL</span> </span> \] )

Constructs Event object.

### 参数

`base`  
The event base to associate with.

`fd`  
stream resource, socket resource, or numeric file descriptor. For timer
events pass **`-1`** . For signal events pass the signal number, e.g.
**`SIGHUP`** .

`what`  
Event flags. See
<a href="/event/flags.html" class="link">Event flags</a> .

`cb`  
The event callback. See
<a href="/event/callbacks.html" class="link">Event callbacks</a> .

`arg`  
Custom data. If specified, it will be passed to the callback when event
triggers.

### 返回值

Returns Event object.

### 参见

-   <span class="methodname">Event::signal</span>
-   <span class="methodname">Event::timer</span>

Event::del
==========

Makes event non-pending

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::del</span> ( <span
class="methodparam">void</span> )

Removes an event from the set of monitored events, i.e. makes it
non-pending.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**

### 参见

-   <span class="methodname">Event::add</span>

Event::delSignal
================

Makes signal event non-pending

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::delSignal</span> ( <span
class="methodparam">void</span> )

<span class="methodname">Event::delSignal</span> is an alias of <span
class="methodname">Event::del</span>

### 参见

-   <span class="methodname">Event::del</span>

Event::delTimer
===============

Makes timer event non-pending

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::delTimer</span> ( <span
class="methodparam">void</span> )

<span class="methodname">Event::delTimer</span> is an alias of <span
class="methodname">Event::del</span> .

### 参见

-   <span class="methodname">Event::del</span>

Event::free
===========

Make event non-pending and free resources allocated for this event

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Event::free</span> ( <span
class="methodparam">void</span> )

Removes event from the list of events monitored by libevent, and free
resources allocated for the event.

**Warning**

The <span class="methodname">Event::free</span> method currently doesn't
destruct the object itself. To destruct the object completely call <span
class="function">unset</span> , or assign **`NULL`**.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">Event::\_\_construct</span>

Event::getSupportedMethods
==========================

Returns array with of the names of the methods supported in this version
of Libevent

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Event::getSupportedMethods</span> ( <span
class="methodparam">void</span> )

Returns array with of the names of the methods(backends) supported in
this version of Libevent.

### 参数

此函数没有参数。

### 返回值

Returns array.

### 参见

-   <span class="classname">EventConfig</span>

Event::pending
==============

Detects whether event is pending or scheduled

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::pending</span> ( <span
class="methodparam"> <span class="type">int</span> `$flags` </span> )

Detects whether event is pending or scheduled

### 参数

`flags`  
One of, or a composition of the following constants: **`Event::READ`** ,
**`Event::WRITE`** , **`Event::TIMEOUT`** , **`Event::SIGNAL`** .

### 返回值

Returns **`TRUE`** if event is pending or scheduled. Otherwise
**`FALSE`**.

Event::set
==========

Re-configures event

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::set</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$what` </span>
\[, <span class="methodparam"> <span class="type">callable</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` </span> \]\]\] )

Re-configures event. Note, this function doesn't invoke obsolete
libevent's event\_set. It calls event\_assign instead.

### 参数

`base`  
The event base to associate the event with.

`fd`  
Stream resource, socket resource, or numeric file descriptor. For timer
events pass **`-1`** . For signal events pass the signal number, e.g.
**`SIGHUP`** .

`what`  
See <a href="/event/flags.html" class="link">Event flags</a> .

`cb`  
The event callback. See
<a href="/event/callbacks.html" class="link">Event callbacks</a> .

`arg`  
Custom data associated with the event. It will be passed to the callback
when the event becomes active.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

Event::setPriority
==================

Set event priority

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::setPriority</span> ( <span
class="methodparam"> <span class="type">int</span> `$priority` </span> )

Set event priority.

### 参数

`priority`  
The event priority.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

Event::setTimer
===============

Re-configures timer event

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Event::setTimer</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">callable</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` </span> \] )

Re-configures timer event. Note, this function doesn't invoke obsolete
libevent's *event\_set* . It calls *event\_assign* instead.

### 参数

`base`  
The event base to associate with.

`cb`  
The timer event callback. See
<a href="/event/callbacks.html" class="link">Event callbacks</a> .

`arg`  
Custom data. If specified, it will be passed to the callback when event
triggers.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">Event::\_\_construct</span>
-   <span class="methodname">Event::timer</span>

Event::signal
=============

Constructs signal event object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Event</span> <span
class="methodname">Event::signal</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">int</span> `$signum` </span> ,
<span class="methodparam"> <span class="type">callable</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$arg` </span> \] )

Constructs signal event object. This is a straightforward method to
create a signal event. Note, the generic <span
class="methodname">Event::\_\_construct</span> method can contruct
signal event objects too.

### 参数

`base`  
The associated event base object.

`signum`  
The signal number.

`cb`  
The signal event callback. See
<a href="/event/callbacks.html" class="link">Event callbacks</a> .

`arg`  
Custom data. If specified, it will be passed to the callback when event
triggers.

### 返回值

Returns Event object on success. Otherwise **`FALSE`**.

### 参见

-   <a href="/event/constructing/signal/events.html" class="link">Constructing signal events</a>

Event::timer
============

Constructs timer event object

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">Event</span> <span
class="methodname">Event::timer</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">callable</span> `$cb` </span>
\[, <span class="methodparam"> <span class="type">mixed</span> `$arg`
</span> \] )

Constructs timer event object. This is a straightforward method to
create a timer event. Note, the generic <span
class="methodname">Event::\_\_construct</span> method can contruct
signal event objects too.

### 参数

`base`  
The associated event base object.

`cb`  
The signal event callback. See
<a href="/event/callbacks.html" class="link">Event callbacks</a> .

`arg`  
Custom data. If specified, it will be passed to the callback when event
triggers.

### 返回值

Returns Event object on success. Otherwise **`FALSE`**.

简介
----

<span class="classname">EventBase</span> class represents libevent's
event base structure. It holds a set of events and can poll to determine
which events are active.

Each event base has a *method* , or a *backend* that it uses to
determine which events are ready. The recognized methods are: *select* ,
*poll* , *epoll* , *kqueue* , *devpoll* , *evport* and *win32* .

To configure event base to use, or avoid specific backend <span
class="classname">EventConfig</span> class can be used.

**Warning**

Do *NOT* destroy the <span class="classname">EventBase</span> object as
long as resources of the associated *Event* objects are not released.
Otherwise, it will lead to unpredictable results!

类摘要
------

**EventBase**

<span class="ooclass"> <span class="modifier">final</span> class
**EventBase** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventBase::LOOP_ONCE` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBase::LOOP_NONBLOCK` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBase::NOLOCK` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBase::STARTUP_IOCP` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBase::NO_CACHE_TIME` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBase::EPOLL_USE_CHANGELIST` <span class="initializer"> = 16</span>
;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span class="methodparam">
<span class="type">EventConfig</span> `$cfg` </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dispatch</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exit</span> (\[ <span class="methodparam">
<span class="type">float</span> `$timeout` </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">free</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFeatures</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getMethod</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getTimeOfDayCached</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">gotExit</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">gotStop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">loop</span> (\[ <span class="methodparam">
<span class="type">int</span> `$flags` </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">priorityInit</span> ( <span
class="methodparam"> <span class="type">int</span> `$n_priorities`
</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">reInit</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stop</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`EventBase::LOOP_ONCE`**  
Flag used with <span class="methodname">EventBase::loop</span> method
which means: "block until libevent has an active event, then exit once
all active events have had their callbacks run".

**`EventBase::LOOP_NONBLOCK`**  
Flag used with <span class="methodname">EventBase::loop</span> method
which means: "do not block: see which events are ready now, run the
callbacks of the highest-priority ones, then exit".

**`EventBase::NOLOCK`**  
Configuration flag. Do not allocate a lock for the event base, even if
we have locking set up".

**`EventBase::STARTUP_IOCP`**  
Windows-only configuration flag. Enables the IOCP dispatcher at startup.

**`EventBase::NO_CACHE_TIME`**  
Configuration flag. Instead of checking the current time every time the
event loop is ready to run timeout callbacks, check after each timeout
callback.

**`EventBase::EPOLL_USE_CHANGELIST`**  
If we are using the *epoll* backend, this flag says that it is safe to
use Libevent's internal change-list code to batch up adds and deletes in
order to try to do as few syscalls as possible.

Setting this flag can make code run faster, but it may trigger a Linux
bug: it is not safe to use this flag if one has any fds cloned by dup(),
or its variants. Doing so will produce strange and hard-to-diagnose
bugs.

This flag can also be activated by settnig the
*EVENT\_EPOLL\_USE\_CHANGELIST* environment variable.

This flag has no effect if one winds up using a backend other than
*epoll* .

EventBase::\_\_construct
========================

Constructs EventBase object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventBase::\_\_construct</span> (\[ <span
class="methodparam"> <span class="type">EventConfig</span> `$cfg`
</span> \] )

Constructs EventBase object

### 参数

`cfg`  
Optional <span class="classname">EventConfig</span> object.

### 返回值

Returns EventBase object.

### 参见

-   <span class="classname">EventConfig</span>

EventBase::dispatch
===================

Dispatch pending events

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBase::dispatch</span> ( <span
class="methodparam">void</span> )

Wait for events to become active, and run their callbacks. The same as
<span class="methodname">EventBase::loop</span> with no flags set.

**Warning**

Do *NOT* destroy the <span class="classname">EventBase</span> object as
long as resources of the associated *Event* objects are not released.
Otherwise, it will lead to unpredictable results!

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBase::loop</span>

EventBase::exit
===============

Stop dispatching events

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::exit</span> (\[ <span
class="methodparam"> <span class="type">float</span> `$timeout` </span>
\] )

Tells event base to stop optionally after given number of seconds.

### 参数

`timeout`  
Optional number of seconds after which the event base should stop
dispatching events.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBase::stop</span>

EventBase::free
===============

Free resources allocated for this event base

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBase::free</span> ( <span
class="methodparam">void</span> )

Deallocates resources allocated by libevent for the <span
class="classname">EventBase</span> object.

**Warning**

The <span class="methodname">EventBase::free</span> method doesn't
destruct the object itself. To destruct the object completely call <span
class="function">unset</span> , or assign **`NULL`**.

This method does not deallocate or detach any of the events that are
currently associated with the <span class="classname">EventBase</span>
object, or close any of their sockets - beware.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventBase::\_\_construct</span>

EventBase::getFeatures
======================

Returns bitmask of features supported

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventBase::getFeatures</span> ( <span
class="methodparam">void</span> )

Returns bitmask of features supported.

### 参数

此函数没有参数。

### 返回值

Returns integer representing a bitmask of supported features. See
<a href="/class/eventconfig.html#预定义常量" class="link">EventConfig::FEATURE_* constants</a>
.

### 范例

**示例 \#1 <span class="function">EventBase::getFeatures</span>
example**

``` php
<?php
// Avoiding "select" method
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "`select' method avoided\n";
}

$base = new EventBase($cfg);

echo "Features:\n";
$features = $base->getFeatures();
($features & EventConfig::FEATURE_ET) and print("ET - edge-triggered IO\n");
($features & EventConfig::FEATURE_O1) and print("O1 - O(1) operation for adding/deletting events\n");
($features & EventConfig::FEATURE_FDS) and print("FDS - arbitrary file descriptor types, and not just sockets\n");
?>
```

### 参见

-   <span class="methodname">EventBase::getMethod</span>
-   <span class="classname">EventConfig</span>

EventBase::getMethod
====================

Returns event method in use

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBase::getMethod</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

String representing used event method(backend).

### 范例

**示例 \#1 <span class="function">EventBase::getMethod</span> example**

``` php
<?php
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "`select' method avoided\n";
}

// Create event_base associated with the config
$base = new EventBase($cfg);
echo "Event method used: ", $base->getMethod(), PHP_EOL;

?>
```

以上例程的输出类似于：

    `select' method avoided
    Event method used: epoll

### 参见

-   <span class="methodname">EventBase::getFeatures</span>

EventBase::getTimeOfDayCached
=============================

Returns the current event base time

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">EventBase::getTimeOfDayCached</span> ( <span
class="methodparam">void</span> )

On success returns the current time(as returned by *gettimeofday()* ),
looking at the cached value in *base* if possible, and calling
*gettimeofday()* or *clock\_gettime()* as appropriate if there is no
cached time.

### 参数

此函数没有参数。

### 返回值

Returns the current *event base* time. On failure returns **`NULL`**.

EventBase::gotExit
==================

Checks if the event loop was told to exit

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::gotExit</span> ( <span
class="methodparam">void</span> )

Checks if the event loop was told to exit by <span
class="methodname">EventBase::exit</span> .

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`**, event loop was told to exit by <span
class="methodname">EventBase::exit</span> . Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBase::exit</span>
-   <span class="methodname">EventBase::stop</span>
-   <span class="methodname">EventBase::gotStop</span>

EventBase::gotStop
==================

Checks if the event loop was told to exit

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::gotStop</span> ( <span
class="methodparam">void</span> )

Checks if the event loop was told to exit by <span
class="methodname">EventBase::stop</span> .

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`**, event loop was told to stop by <span
class="methodname">EventBase::stop</span> . Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBase::exit</span>
-   <span class="methodname">EventBase::stop</span>
-   <span class="methodname">EventBase::gotExit</span>

EventBase::loop
===============

Dispatch pending events

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::loop</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$flags` </span> \] )

Wait for events to become active, and run their callbacks.

**Warning**

Do *NOT* destroy the <span class="classname">EventBase</span> object as
long as resources of the associated *Event* objects are not released.
Otherwise, it will lead to unpredictable results!

### 参数

`flags`  
Optional flags. One of *EventBase::LOOP\_\** constants. See
<a href="/class/eventbase.html#预定义常量" class="link">EventBase constants</a>
.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBase::dispatch</span>

EventBase::priorityInit
=======================

Sets number of priorities per event base

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::priorityInit</span> ( <span
class="methodparam"> <span class="type">int</span> `$n_priorities`
</span> )

Sets number of priorities per event base.

### 参数

`n_priorities`  
The number of priorities per event base.

### 返回值

Returns **`TRUE`** on success, otherwise **`FALSE`**.

### 参见

-   <span class="methodname">Event::setPriority</span>

EventBase::reInit
=================

Re-initialize event base(after a fork)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::reInit</span> ( <span
class="methodparam">void</span> )

Re-initialize event base. Should be called after a fork.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventBase::stop
===============

Tells event\_base to stop dispatching events

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBase::stop</span> ( <span
class="methodparam">void</span> )

Tells event\_base to stop dispatching events

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBase::exit</span>
-   <span class="methodname">EventBase::gotStop</span>

简介
----

<span class="classname">EventBuffer</span> represents Libevent's
"evbuffer", an utility functionality for buffered I/O.

Event buffers are meant to be generally useful for doing the "buffer"
part of buffered network I/O.

类摘要
------

**EventBuffer**

<span class="ooclass"> class **EventBuffer** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventBuffer::EOL_ANY` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBuffer::EOL_CRLF` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBuffer::EOL_CRLF_STRICT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBuffer::EOL_LF` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBuffer::PTR_SET` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBuffer::PTR_ADD` <span class="initializer"> = 1</span> ;

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$length`
;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span>
`$contiguous_space` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">add</span> ( <span class="methodparam"> <span
class="type">string</span> `$data` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addBuffer</span> ( <span class="methodparam">
<span class="type">EventBuffer</span> `$buf` </span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">appendFrom</span> ( <span class="methodparam"> <span
class="type">EventBuffer</span> `$buf` </span> , <span
class="methodparam"> <span class="type">int</span> `$len` </span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">copyout</span> ( <span class="methodparam"> <span
class="type">string</span> `&$data` </span> , <span class="methodparam">
<span class="type">int</span> `$max_bytes` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">drain</span> ( <span class="methodparam"> <span
class="type">int</span> `$len` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">enableLocking</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">expand</span> ( <span class="methodparam">
<span class="type">int</span> `$len` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">freeze</span> ( <span class="methodparam">
<span class="type">bool</span> `$at_front` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">prepend</span> ( <span class="methodparam">
<span class="type">string</span> `$data` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">prependBuffer</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">pullup</span> ( <span class="methodparam">
<span class="type">int</span> `$size` </span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">read</span> ( <span class="methodparam"> <span
class="type">int</span> `$max_bytes` </span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">read</span> ( <span class="methodparam"> <span
class="type">mixed</span> `$fd` </span> , <span class="methodparam">
<span class="type">int</span> `$howmuch` </span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">readLine</span> ( <span class="methodparam">
<span class="type">int</span> `$eol_style` </span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">search</span> ( <span class="methodparam">
<span class="type">string</span> `$what` </span> \[, <span
class="methodparam"> <span class="type">int</span> `$start` <span
class="initializer"> = -1</span> </span> \[, <span class="methodparam">
<span class="type">int</span> `$end` <span class="initializer"> =
-1</span> </span> \]\] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">searchEol</span> (\[ <span class="methodparam">
<span class="type">int</span> `$start` <span class="initializer"> =
-1</span> </span> \[, <span class="methodparam"> <span
class="type">int</span> `$eol_style` <span class="initializer"> =
**`EventBuffer::EOL_ANY`** </span> </span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">substr</span> ( <span class="methodparam">
<span class="type">int</span> `$start` </span> \[, <span
class="methodparam"> <span class="type">int</span> `$length` </span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unfreeze</span> ( <span class="methodparam">
<span class="type">bool</span> `$at_front` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">write</span> ( <span class="methodparam"> <span
class="type">mixed</span> `$fd` </span> \[, <span class="methodparam">
<span class="type">int</span> `$howmuch` </span> \] )

}

属性
----

`length`  
The number of bytes stored in an event buffer.

`contiguous_space`  
The number of bytes stored contiguously at the front of the buffer. The
bytes in a buffer may be stored in multiple separate chunks of memory;
the property returns the number of bytes currently stored in the first
chunk.

预定义常量
----------

**`EventBuffer::EOL_ANY`**  
The end of line is any sequence of any number of carriage return and
linefeed characters. This format is not very useful; it exists mainly
for backward compatibility.

**`EventBuffer::EOL_CRLF`**  
The end of the line is an optional carriage return, followed by a
linefeed. (In other words, it is either a *"\\r\\n"* or a *"\\n"* .)
This format is useful in parsing text-based Internet protocols, since
the standards generally prescribe a *"\\r\\n"* line-terminator, but
nonconformant clients sometimes say just *"\\n"* .

**`EventBuffer::EOL_CRLF_STRICT`**  
The end of a line is a single carriage return, followed by a single
linefeed. (This is also known as *"\\r\\n"* . The ASCII values are
**`0x0D`** **`0x0A`** ).

**`EventBuffer::EOL_LF`**  
The end of a line is a single linefeed character. (This is also known as
*"\\n"* . It is ASCII value is **`0x0A`** .)

**`EventBuffer::PTR_SET`**  
Flag used as argument of <span
class="methodname">EventBuffer::setPosition</span> method. If this flag
specified, the position pointer is moved to an absolute position within
the buffer.

**`EventBuffer::PTR_ADD`**  
The same as **`EventBuffer::PTR_SET`** , except this flag causes <span
class="methodname">EventBuffer::setPosition</span> method to move
position forward up to the specified number of bytes(instead of setting
absolute position).

EventBuffer::add
================

Append data to the end of an event buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::add</span> ( <span
class="methodparam"> <span class="type">string</span> `$data` </span> )

Append data to the end of an event buffer.

### 参数

`data`  
String to be appended to the end of the buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::addBuffer</span>

EventBuffer::addBuffer
======================

Move all data from a buffer provided to the current instance of
EventBuffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::addBuffer</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

Move all data from the buffer provided in `buf` parameter to the end of
current <span class="classname">EventBuffer</span> . This is a
destructive add. The data from one buffer moves into the other buffer.
However, no unnecessary memory copies occur.

### 参数

`buf`  
The source EventBuffer object.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::add</span>

EventBuffer::appendFrom
=======================

Moves the specified number of bytes from a source buffer to the end of
the current buffer

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventBuffer::appendFrom</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> , <span class="methodparam"> <span class="type">int</span>
`$len` </span> )

Moves the specified number of bytes from a source buffer to the end of
the current buffer. If there are fewer number of bytes, it moves all the
bytes available from the source buffer.

### 参数

`buf`  
Source buffer.

`len`  

### 返回值

Returns the number of bytes read.

### 更新日志

| 版本             | 说明                                                                                                                                             |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL event 1.6.0 | Renamed <span class="methodname">EventBuffer::appendFrom</span>(the old method name) to <span class="methodname">EventBuffer::appendFrom</span>. |

### 参见

-   <span class="methodname">EventBuffer::copyout</span>
-   <span class="methodname">EventBuffer::drain</span>
-   <span class="methodname">EventBuffer::pullup</span>
-   <span class="methodname">EventBuffer::readLine</span>
-   <span class="methodname">EventBuffer::read</span>

EventBuffer::\_\_construct
==========================

Constructs EventBuffer object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventBuffer::\_\_construct</span> ( <span
class="methodparam">void</span> )

Constructs EventBuffer object

### 参数

此函数没有参数。

### 返回值

Returns EventBuffer object.

EventBuffer::copyout
====================

Copies out specified number of bytes from the front of the buffer

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventBuffer::copyout</span> ( <span
class="methodparam"> <span class="type">string</span> `&$data` </span> ,
<span class="methodparam"> <span class="type">int</span> `$max_bytes`
</span> )

Behaves just like <span class="methodname">EventBuffer::read</span> ,
but does not drain any data from the buffer. I.e. it copies the first
`max_bytes` bytes from the front of the buffer into `data` . If there
are fewer than `max_bytes` bytes available, the function copies all the
bytes there are.

### 参数

`data`  
Output string.

`max_bytes`  
The number of bytes to copy.

### 返回值

Returns the number of bytes copied, or **`-1`** on failure.

### 参见

-   <span class="methodname">EventBuffer::read</span>
-   <span class="methodname">EventBuffer::appendFrom</span>

EventBuffer::drain
==================

Removes specified number of bytes from the front of the buffer without
copying it anywhere

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::drain</span> ( <span
class="methodparam"> <span class="type">int</span> `$len` </span> )

Behaves as <span class="methodname">EventBuffer::read</span> , except
that it does not copy the data: it just removes it from the front of the
buffer.

### 参数

`len`  
The number of bytes to remove from the buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::read</span>
-   <span class="methodname">EventBuffer::appendFrom</span>

EventBuffer::enableLocking
==========================

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBuffer::enableLocking</span> ( <span
class="methodparam">void</span> )

Enable locking on an <span class="classname">EventBuffer</span> so that
it can safely be used by multiple threads at the same time. When locking
is enabled, the lock will be held when callbacks are invoked. This could
result in deadlock if you aren't careful. Plan accordingly!

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <a href="http://www.wangafu.net/~nickm/libevent-book/Ref7_evbuffer.html#_evbuffers_and_thread_safety" class="link external">» Evbuffers and Thread-safety</a>

EventBuffer::expand
===================

Reserves space in buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::expand</span> ( <span
class="methodparam"> <span class="type">int</span> `$len` </span> )

Alters the last chunk of memory in the buffer, or adds a new chunk, such
that the buffer is now large enough to contain `len` bytes without any
further allocations.

### 参数

`len`  
The number of bytes to reserve for the buffer

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventBuffer::freeze
===================

Prevent calls that modify an event buffer from succeeding

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::freeze</span> ( <span
class="methodparam"> <span class="type">bool</span> `$at_front` </span>
)

Prevent calls that modify an event buffer from succeeding

### 参数

`at_front`  
Whether to disable changes to the front or end of the buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::unfreeze</span>

EventBuffer::lock
=================

Acquires a lock on buffer

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBuffer::lock</span> ( <span
class="methodparam">void</span> )

Acquires a lock on buffer. Can be used in pair with <span
class="methodname">EventBuffer::unlock</span> to make a set of
operations atomic, i.e. thread-safe. Note, it is not needed to lock
buffers for *individual* operations. When locking is enabled(see <span
class="methodname">EventBuffer::enableLocking</span> ), individual
operations on event buffers are already atomic.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventBuffer::unlock</span>

EventBuffer::prepend
====================

Prepend data to the front of the buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::prepend</span> ( <span
class="methodparam"> <span class="type">string</span> `$data` </span> )

Prepend data to the front of the buffer.

### 参数

`data`  
String to be prepended to the front of the buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::prependBuffer</span>
-   <span class="methodname">EventBuffer::add</span>
-   <span class="methodname">EventBuffer::addBuffer</span>

EventBuffer::prependBuffer
==========================

Moves all data from source buffer to the front of current buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::prependBuffer</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

Behaves as <span class="methodname">EventBuffer::addBuffer</span> ,
except that it moves data to the front of the buffer.

### 参数

`buf`  
Source buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::add</span>
-   <span class="methodname">EventBuffer::addBuffer</span>
-   <span class="methodname">EventBuffer::prepend</span>

EventBuffer::pullup
===================

Linearizes data within buffer and returns it's contents as a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBuffer::pullup</span> ( <span
class="methodparam"> <span class="type">int</span> `$size` </span> )

"Linearizes" the first `size` bytes of the buffer, copying or moving
them as needed to ensure that they are all contiguous and occupying the
same chunk of memory. If size is negative, the function linearizes the
entire buffer.

**Warning**

Calling <span class="methodname">EventBuffer::pullup</span> with a large
size can be quite slow, since it potentially needs to copy the entire
buffer's contents.

### 参数

`size`  
The number of bytes required to be contiguous within the buffer.

### 返回值

If `size` is greater than the number of bytes in the buffer, the
function returns **`NULL`**. Otherwise, <span
class="methodname">EventBuffer::pullup</span> returns string.

### 参见

-   <span class="methodname">EventBuffer::copyout</span>
-   <span class="methodname">EventBuffer::drain</span>
-   <span class="methodname">EventBuffer::read</span>
-   <span class="methodname">EventBuffer::readLine</span>
-   <span class="methodname">EventBuffer::appendFrom</span>

EventBuffer::read
=================

Read data from an evbuffer and drain the bytes read

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBuffer::read</span> ( <span
class="methodparam"> <span class="type">int</span> `$max_bytes` </span>
)

Read the first `max_bytes` from the buffer and drain the bytes read. If
more `max_bytes` are requested than are available in the buffer, it only
extracts as many bytes as available.

### 参数

`max_bytes`  
Maxmimum number of bytes to read from the buffer.

### 返回值

Returns string read, or **`FALSE`** on failure.

### 更新日志

| 版本             | 说明                                                                                                                                                                                                                                                           |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL event 1.6.0 | Renamed <span class="methodname">EventBuffer::read</span>(the old method name) to <span class="methodname">EventBuffer::read</span>. <span class="methodname">EventBuffer::read</span> now takes only `max_bytes` argument; returns string instead of integer. |

### 参见

-   <span class="methodname">EventBuffer::copyout</span>
-   <span class="methodname">EventBuffer::drain</span>
-   <span class="methodname">EventBuffer::pullup</span>
-   <span class="methodname">EventBuffer::readLine</span>
-   <span class="methodname">EventBuffer::appendFrom</span>

EventBuffer::readFrom
=====================

Read data from a file onto the end of the buffer

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventBuffer::read</span> ( <span class="methodparam">
<span class="type">mixed</span> `$fd` </span> , <span
class="methodparam"> <span class="type">int</span> `$howmuch` </span> )

Read data from the file specified by `fd` onto the end of the buffer.

### 参数

`fd`  
Socket resource, stream, or numeric file descriptor.

`howmuch`  
Maxmimum number of bytes to read.

### 返回值

Returns the number of bytes read, or **`FALSE`** on failure.

### 参见

-   <span class="methodname">EventBuffer::copyout</span>
-   <span class="methodname">EventBuffer::drain</span>
-   <span class="methodname">EventBuffer::pullup</span>
-   <span class="methodname">EventBuffer::readLine</span>
-   <span class="methodname">EventBuffer::appendFrom</span>

EventBuffer::readLine
=====================

Extracts a line from the front of the buffer

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBuffer::readLine</span> ( <span
class="methodparam"> <span class="type">int</span> `$eol_style` </span>
)

Extracts a line from the front of the buffer and returns it in a newly
allocated string. If there is not a whole line to read, the function
returns **`NULL`**. The line terminator is not included in the copied
string.

### 参数

`eol_style`  
One of
<a href="/class/eventbuffer.html#预定义常量" class="link">EventBuffer:EOL_* constants</a>
.

### 返回值

On success returns the line read from the buffer, otherwise **`NULL`**.

### 参见

-   <span class="methodname">EventBuffer::copyout</span>
-   <span class="methodname">EventBuffer::drain</span>
-   <span class="methodname">EventBuffer::pullup</span>
-   <span class="methodname">EventBuffer::read</span>
-   <span class="methodname">EventBuffer::appendFrom</span>

EventBuffer::search
===================

Scans the buffer for an occurrence of a string

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">EventBuffer::search</span> ( <span
class="methodparam"> <span class="type">string</span> `$what` </span>
\[, <span class="methodparam"> <span class="type">int</span> `$start`
<span class="initializer"> = -1</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$end` <span
class="initializer"> = -1</span> </span> \]\] )

Scans the buffer for an occurrence of the string `what` . It returns
numeric position of the string, or **`FALSE`** if the string was not
found.

If the `start` argument is provided, it points to the position at which
the search should begin; otherwise, the search is performed from the
start of the string. If `end` argument provided, the search is performed
between start and end buffer positions.

### 参数

`what`  
String to search.

`start`  
Start search position.

`end`  
End search position.

### 返回值

Returns numeric position of the first occurance of the string in the
buffer, or **`FALSE`** if string is not found.

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 <span class="function">EventBuffer::search</span> example**

``` php
<?php
// Count total occurances of 'str' in 'buf'
function count_instances($buf, $str) {
    $total = 0;
    $p     = 0;
    $i     = 0;

    while (1) {
        $p = $buf->search($str, $p);
        if ($p === FALSE) {
            break;
        }
        ++$total;
        ++$p;
    }

    return $total;
}

$buf = new EventBuffer();
$buf->add("Some string within a string inside another string");
var_dump(count_instances($buf, "str"));
?>
```

以上例程的输出类似于：

    int(3)

### 参见

-   <span class="methodname">EventBuffer::searchEol</span>

EventBuffer::searchEol
======================

Scans the buffer for an occurrence of an end of line

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">EventBuffer::searchEol</span> (\[ <span
class="methodparam"> <span class="type">int</span> `$start` <span
class="initializer"> = -1</span> </span> \[, <span class="methodparam">
<span class="type">int</span> `$eol_style` <span class="initializer"> =
**`EventBuffer::EOL_ANY`** </span> </span> \]\] )

Scans the buffer for an occurrence of an end of line specified by
`eol_style` parameter . It returns numeric position of the string, or
**`FALSE`** if the string was not found.

If the `start` argument is provided, it represents the position at which
the search should begin; otherwise, the search is performed from the
start of the string. If `end` argument provided, the search is performed
between start and end buffer positions.

### 参数

`start`  
Start search position.

`eol_style`  
One of
<a href="/class/eventbuffer.html#预定义常量" class="link">EventBuffer:EOL_* constants</a>
.

### 返回值

Returns numeric position of the first occurance of end-of-line symbol in
the buffer, or **`FALSE`** if not found.

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 参见

-   <span class="methodname">EventBuffer::search</span>

EventBuffer::substr
===================

Substracts a portion of the buffer data

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBuffer::substr</span> ( <span
class="methodparam"> <span class="type">int</span> `$start` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$length`
</span> \] )

Substracts up to `length` bytes of the buffer data beginning at `start`
position.

### 参数

`start`  
The start position of data to be substracted.

`length`  
Maximum number of bytes to substract.

### 返回值

Returns the data substracted as a <span class="type">string</span> on
success, or **`FALSE`** on failure.

### 参见

-   <span class="methodname">EventBuffer::read</span>

EventBuffer::unfreeze
=====================

Re-enable calls that modify an event buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::unfreeze</span> ( <span
class="methodparam"> <span class="type">bool</span> `$at_front` </span>
)

Re-enable calls that modify an event buffer.

### 参数

`at_front`  
Whether to enable events at the front or at the end of the buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::freeze</span>

EventBuffer::unlock
===================

Releases lock acquired by EventBuffer::lock

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBuffer::unlock</span> ( <span
class="methodparam">void</span> )

Releases lock acquired by <span
class="methodname">EventBuffer::lock</span> .

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBuffer::lock</span>

EventBuffer::write
==================

Write contents of the buffer to a file or socket

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventBuffer::write</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$fd` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$howmuch`
</span> \] )

Write contents of the buffer to a file descriptor. The buffer will be
drained after the bytes have been successfully written.

### 参数

`fd`  
Socket resource, stream or numeric file descriptor associated normally
associated with a socket.

`howmuch`  
The maximum number of bytes to write.

### 返回值

Returns the number of bytes written, or **`FALSE`** on error.

### 参见

-   <span class="methodname">EventBuffer::read</span>

简介
----

Represents Libevent's buffer event.

Usually an application wants to perform some amount of data buffering in
addition to just responding to events. When we want to write data, for
example, the usual pattern looks like:

1.  Decide that we want to write some data to a connection; put that
    data in a buffer.

2.  Wait for the connection to become writable

3.  Write as much of the data as we can

4.  Remember how much we wrote, and if we still have more data to write,
    wait for the connection to become writable again.

This buffered I/O pattern is common enough that Libevent provides a
generic mechanism for it. A "buffer event" consists of an underlying
transport (like a socket), a read buffer, and a write buffer. Instead of
regular events, which give callbacks when the underlying transport is
ready to be read or written, a buffer event invokes its user-supplied
callbacks when it has read or written enough data.

类摘要
------

**EventBufferEvent**

<span class="ooclass"> <span class="modifier">final</span> class
**EventBufferEvent** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::READING` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::WRITING` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::EOF` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::ERROR` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::TIMEOUT` <span class="initializer"> = 64</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::CONNECTED` <span class="initializer"> = 128</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::OPT_CLOSE_ON_FREE` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::OPT_THREADSAFE` <span class="initializer"> = 2</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::OPT_DEFER_CALLBACKS` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::OPT_UNLOCK_CALLBACKS` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::SSL_OPEN` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::SSL_CONNECTING` <span class="initializer"> = 1</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventBufferEvent::SSL_ACCEPTING` <span class="initializer"> = 2</span>
;

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">integer</span>
`$fd` ;

<span class="modifier">public</span> <span class="type">integer</span>
`$priority` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">EventBuffer</span>
`$input` ;

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">EventBuffer</span>
`$output` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connect</span> ( <span class="methodparam">
<span class="type">string</span> `$addr` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connectHost</span> ( <span class="methodparam">
<span class="type">EventDnsBase</span> `$dns_base` </span> , <span
class="methodparam"> <span class="type">string</span> `$hostname`
</span> , <span class="methodparam"> <span class="type">int</span>
`$port` </span> \[, <span class="methodparam"> <span
class="type">int</span> `$family` <span class="initializer"> =
EventUtil::AF\_UNSPEC</span> </span> \] )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$socket` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$options` <span
class="initializer"> = 0</span> </span> \[, <span class="methodparam">
<span class="type">callable</span> `$readcb` <span class="initializer">
= **`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">callable</span> `$writecb` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">callable</span> `$eventcb` <span class="initializer"> =
**`NULL`**</span> </span> \]\]\]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">createPair</span> ( <span class="methodparam"> <span
class="type">EventBase</span> `$base` </span> \[, <span
class="methodparam"> <span class="type">int</span> `$options` <span
class="initializer"> = 0</span> </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disable</span> ( <span class="methodparam">
<span class="type">int</span> `$events` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">enable</span> ( <span class="methodparam">
<span class="type">int</span> `$events` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">free</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getDnsErrorString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getEnabled</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span class="methodname">getInput</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">getOutput</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">read</span> ( <span class="methodparam"> <span
class="type">int</span> `$size` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">readBuffer</span> ( <span class="methodparam">
<span class="type">EventBuffer</span> `$buf` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCallbacks</span> ( <span
class="methodparam"> <span class="type">callable</span> `$readcb`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$writecb` </span> , <span class="methodparam"> <span
class="type">callable</span> `$eventcb` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$arg` </span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setPriority</span> ( <span class="methodparam">
<span class="type">int</span> `$priority` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setTimeouts</span> ( <span class="methodparam">
<span class="type">float</span> `$timeout_read` </span> , <span
class="methodparam"> <span class="type">float</span> `$timeout_write`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setWatermark</span> ( <span
class="methodparam"> <span class="type">int</span> `$events` </span> ,
<span class="methodparam"> <span class="type">int</span> `$lowmark`
</span> , <span class="methodparam"> <span class="type">int</span>
`$highmark` </span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">sslError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">EventBufferEvent</span> <span
class="methodname">sslFilter</span> ( <span class="methodparam"> <span
class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">EventBufferEvent</span>
`$underlying` </span> , <span class="methodparam"> <span
class="type">EventSslContext</span> `$ctx` </span> , <span
class="methodparam"> <span class="type">int</span> `$state` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$options`
<span class="initializer"> = 0</span> </span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">sslGetCipherInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">sslGetCipherName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">sslGetCipherVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">sslGetProtocol</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sslRenegotiate</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">EventBufferEvent</span> <span
class="methodname">sslSocket</span> ( <span class="methodparam"> <span
class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span> ,
<span class="methodparam"> <span class="type">EventSslContext</span>
`$ctx` </span> , <span class="methodparam"> <span
class="type">int</span> `$state` </span> \[, <span class="methodparam">
<span class="type">int</span> `$options` </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">write</span> ( <span class="methodparam"> <span
class="type">string</span> `$data` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">writeBuffer</span> ( <span class="methodparam">
<span class="type">EventBuffer</span> `$buf` </span> )

}

属性
----

`fd`  
Numeric file descriptor associated with the buffer event. Normally
represents a bound socket. Equals to **`NULL`**, if there is no file
descriptor(socket) associated with the buffer event.

`priority`  
The priority of the events used to implement the buffer event.

`input`  
Underlying input buffer object( <span
class="classname">EventBuffer</span> )

`output`  
Underlying output buffer object( <span
class="classname">EventBuffer</span> )

预定义常量
----------

**`EventBufferEvent::READING`**  
An event occurred during a read operation on the bufferevent. See the
other flags for which event it was.

**`EventBufferEvent::WRITING`**  
An event occurred during a write operation on the bufferevent. See the
other flags for which event it was.

**`EventBufferEvent::EOF`**  
Got an end-of-file indication on the buffer event.

**`EventBufferEvent::ERROR`**  
An error occurred during a bufferevent operation. For more information
on what the error was, call <span
class="methodname">EventUtil::getLastSocketErrno</span> and/or <span
class="methodname">EventUtil::getLastSocketError</span> .

**`EventBufferEvent::TIMEOUT`**  

**`EventBufferEvent::CONNECTED`**  
Finished a requested connection on the bufferevent.

**`EventBufferEvent::OPT_CLOSE_ON_FREE`**  
When the buffer event is freed, close the underlying transport. This
will close an underlying socket, free an underlying buffer event, etc.

**`EventBufferEvent::OPT_THREADSAFE`**  
Automatically allocate locks for the bufferevent, so that it’s safe to
use from multiple threads.

**`EventBufferEvent::OPT_DEFER_CALLBACKS`**  
When this flag is set, the bufferevent defers all of its callbacks. See
<a href="http://www.wangafu.net/~nickm/libevent-book/Ref6_bufferevent.html#_deferred_callbacks" class="link external">» Fast portable non-blocking network programming with Libevent, Deferred callbacks</a>
.

**`EventBufferEvent::OPT_UNLOCK_CALLBACKS`**  
By default, when the bufferevent is set up to be threadsafe, the buffer
event’s locks are held whenever the any user-provided callback is
invoked. Setting this option makes Libevent release the buffer event’s
lock when it’s invoking the callbacks.

**`EventBufferEvent::SSL_OPEN`**  
The SSL handshake is done

**`EventBufferEvent::SSL_CONNECTING`**  
SSL is currently performing negotiation as a client

**`EventBufferEvent::SSL_ACCEPTING`**  
SSL is currently performing negotiation as a server

EventBufferEvent::close
=======================

Closes file descriptor associated with the current buffer event

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBufferEvent::close</span> ( <span
class="methodparam">void</span> )

Closes file descriptor associated with the current buffer event.

This method may be used in cases when the
**`EventBufferEvent::OPT_CLOSE_ON_FREE`** option is not appropriate.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventBufferEvent::connect
=========================

Connect buffer event's file descriptor to given address or UNIX socket

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::connect</span> ( <span
class="methodparam"> <span class="type">string</span> `$addr` </span> )

Connect buffer event's file descriptor to given address(optionally with
port), or a UNIX domain socket.

If socket is not assigned to the buffer event, this function allocates a
new socket and makes it non-blocking internally.

To resolve DNS names(asyncronously), use <span
class="methodname">EventBufferEvent::connectHost</span> method.

### 参数

`addr`  
Should contain an IP address with optional port number, or a path to
UNIX domain socket. Recognized formats are:

``` parameters
[IPv6Address]:port
[IPv6Address]
IPv6Address
IPv4Address:port
IPv4Address
unix:path
```

Note, *'unix:'* prefix is currently not case sensitive.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventBufferEvent::connect</span>
example**

``` php
<?php
/*
 * 1. Connect to 127.0.0.1 at port 80
 * by means of EventBufferEvent::connect().
 *
 * 2. Request /index.cphp via HTTP/1.0
 * using the output buffer.
 *
 * 3. Asyncronously read the response and print it to stdout.
 */

/* Read callback */
function readcb($bev, $base) {
    $input = $bev->getInput();

    while (($n = $input->remove($buf, 1024)) > 0) {
        echo $buf;
    }
}

/* Event callback */
function eventcb($bev, $events, $base) {
    if ($events & EventBufferEvent::CONNECTED) {
        echo "Connected.\n";
    } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {
        if ($events & EventBufferEvent::ERROR) {
            echo "DNS error: ", $bev->getDnsErrorString(), PHP_EOL;
        }

        echo "Closing\n";
        $base->exit();
        exit("Done\n");
    }
}

$base = new EventBase();

echo "step 1\n";
$bev = new EventBufferEvent($base, /* use internal socket */ NULL,
    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS);
if (!$bev) {
    exit("Failed creating bufferevent socket\n");
}

echo "step 2\n";
$bev->setCallbacks("readcb", /* writecb */ NULL, "eventcb", $base);
$bev->enable(Event::READ | Event::WRITE);

echo "step 3\n";
/* Send request */
$output = $bev->getOutput();
if (!$output->add(
    "GET /index.cphp HTTP/1.0\r\n".
    "Connection: Close\r\n\r\n"
)) {
    exit("Failed adding request to output buffer\n");
}

/* Connect to the host syncronously.
 * We know the IP, and don't need to resolve DNS. */
if (!$bev->connect("127.0.0.1:80")) {
    exit("Can't connect to host\n");
}

/* Dispatch pending events */
$base->dispatch();
```

以上例程的输出类似于：

    step 1
    step 2
    step 3
    Connected.
    HTTP/1.1 200 OK
    Server: nginx/1.2.6
    Date: Sat, 09 Mar 2013 10:06:58 GMT
    Content-Type: text/html; charset=utf-8
    Connection: close
    X-Powered-By: PHP/5.4.11--pl2-gentoo

    sdfsdfsf
    Closing
    Done

**示例 \#2 Connect to UNIX domain socket which presumably is served by a
server, read response from the server and output it to the console**

``` php
<?php
class MyUnixSocketClient {
    private $base, $bev;

    function __construct($base, $sock_path) {
        $this->base = $base;
        $this->bev = new EventBufferEvent($base, NULL, EventBufferEvent::OPT_CLOSE_ON_FREE,
            array ($this, "read_cb"), NULL, array ($this, "event_cb"));

        if (!$this->bev->connect("unix:$sock_path")) {
            trigger_error("Failed to connect to socket `$sock_path'", E_USER_ERROR);
        }

        $this->bev->enable(Event::READ);
    }

    function __destruct() {
        if ($this->bev) {
            $this->bev->free();
            $this->bev = NULL;
        }
    }

    function dispatch() {
        $this->base->dispatch();
    }

    function read_cb($bev, $unused) {
        $in = $bev->input;

        printf("Received %ld bytes\n", $in->length);
        printf("----- data ----\n");
        printf("%ld:\t%s\n", (int) $in->length, $in->pullup(-1));

        $this->bev->free();
        $this->bev = NULL;
        $this->base->exit(NULL);
    }

    function event_cb($bev, $events, $unused) {
        if ($events & EventBufferEvent::ERROR) {
            echo "Error from bufferevent\n";
        }

        if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {
            $bev->free();
            $bev = NULL;
        } elseif ($events & EventBufferEvent::CONNECTED) {
            $bev->output->add("test\n");
        }
    }
}

if ($argc <= 1) {
    exit("Socket path is not provided\n");
}
$sock_path = $argv[1];

$base = new EventBase();
$cl = new MyUnixSocketClient($base, $sock_path);
$cl->dispatch();
?>
```

以上例程的输出类似于：

    Received 5 bytes
    ----- data ----
    5:  test

### 参见

-   <span class="methodname">EventBufferEvent::connectHost</span>

EventBufferEvent::connectHost
=============================

Connects to a hostname with optionally asyncronous DNS resolving

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::connectHost</span> ( <span
class="methodparam"> <span class="type">EventDnsBase</span> `$dns_base`
</span> , <span class="methodparam"> <span class="type">string</span>
`$hostname` </span> , <span class="methodparam"> <span
class="type">int</span> `$port` </span> \[, <span class="methodparam">
<span class="type">int</span> `$family` <span class="initializer"> =
EventUtil::AF\_UNSPEC</span> </span> \] )

Resolves the DNS name hostname, looking for addresses of type `family` (
*EventUtil::AF\_\** constants). If the name resolution fails, it invokes
the event callback with an error event. If it succeeds, it launches a
connection attempt just as <span
class="methodname">EventBufferEvent::connect</span> would.

`dns_base` is optional. May be **`NULL`**, or an object created with
<span class="methodname">EventDnsBase::\_\_construct</span> . For
asyncronous hostname resolving pass a valid event dns base resource.
Otherwise the hostname resolving will block.

> **Note**:
>
> <span class="classname">EventDnsBase</span> is available only if
> *Event* configured **--with-event-extra** ( *event\_extra* library,
> *libevent protocol-specific functionality support including HTTP, DNS,
> and RPC* ).

> **Note**:
>
> <span class="methodname">EventBufferEvent::connectHost</span> requires
> *libevent-2.0.3-alpha* or greater.

### 参数

`dns_base`  
Object of <span class="classname">EventDnsBase</span> in case if DNS is
to be resolved asyncronously. Otherwise **`NULL`**.

`hostname`  
Hostname to connect to. Recognized formats are:

``` parameters
www.example.com (hostname)
 1.2.3.4 (ipv4address)
 ::1 (ipv6address)
[::1] ([ipv6address])
```

`port`  
Port number

`family`  
Address family. **`EventUtil::AF_UNSPEC`** , **`EventUtil::AF_INET`** ,
or **`EventUtil::AF_INET6`** . See
<a href="/class/eventutil.html#预定义常量" class="link">EventUtil constants</a>
.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventBufferEvent::connectHost</span>
example**

``` php
<?php
/* Read callback */
function readcb($bev, $base) {
    //$input = $bev->input; //$bev->getInput();

    //$pos = $input->search("TTP");
    $pos = $bev->input->search("TTP");

    while (($n = $bev->input->remove($buf, 1024)) > 0) {
        echo $buf;
    }
}

/* Event callback */
function eventcb($bev, $events, $base) {
    if ($events & EventBufferEvent::CONNECTED) {
        echo "Connected.\n";
    } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {
        if ($events & EventBufferEvent::ERROR) {
            echo "DNS error: ", $bev->getDnsErrorString(), PHP_EOL;
        }

        echo "Closing\n";
        $base->exit();
        exit("Done\n");
    }
}

$base = new EventBase();

$dns_base = new EventDnsBase($base, TRUE); // We'll use async DNS resolving
if (!$dns_base) {
    exit("Failed to init DNS Base\n");
}

$bev = new EventBufferEvent($base, /* use internal socket */ NULL,
    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS,
    "readcb", /* writecb */ NULL, "eventcb", $base
);
if (!$bev) {
    exit("Failed creating bufferevent socket\n");
}

//$bev->setCallbacks("readcb", /* writecb */ NULL, "eventcb", $base);
$bev->enable(Event::READ | Event::WRITE);

$output = $bev->output; //$bev->getOutput();
if (!$output->add(
    "GET {$argv[2]} HTTP/1.0\r\n".
    "Host: {$argv[1]}\r\n".
    "Connection: Close\r\n\r\n"
)) {
    exit("Failed adding request to output buffer\n");
}

if (!$bev->connectHost($dns_base, $argv[1], 80, EventUtil::AF_UNSPEC)) {
    exit("Can't connect to host {$argv[1]}\n");
}

$base->dispatch();
?>
```

以上例程的输出类似于：

    Connected.
    HTTP/1.0 301 Moved Permanently
    Location: http://www.google.co.uk/
    Content-Type: text/html; charset=UTF-8
    Date: Sat, 09 Mar 2013 12:21:19 GMT
    Expires: Mon, 08 Apr 2013 12:21:19 GMT
    Cache-Control: public, max-age=2592000
    Server: gws
    Content-Length: 221
    X-XSS-Protection: 1; mode=block
    X-Frame-Options: SAMEORIGIN

    <HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
    <TITLE>301 Moved</TITLE></HEAD><BODY>
    <H1>301 Moved</H1>
    The document has moved
    <A HREF="http://www.google.co.uk/">here</A>.
    </BODY></HTML>
    Closing
    Done

### 参见

-   <span class="methodname">EventBufferEvent::connect</span>

EventBufferEvent::\_\_construct
===============================

Constructs EventBufferEvent object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventBufferEvent::\_\_construct</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
\[, <span class="methodparam"> <span class="type">mixed</span> `$socket`
<span class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$options` <span
class="initializer"> = 0</span> </span> \[, <span class="methodparam">
<span class="type">callable</span> `$readcb` <span class="initializer">
= **`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">callable</span> `$writecb` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">callable</span> `$eventcb` <span class="initializer"> =
**`NULL`**</span> </span> \]\]\]\]\] )

Create a buffer event on a socket, stream or a file descriptor. Passing
**`NULL`** to `socket` means that the socket should be created later,
e.g. by means of <span
class="methodname">EventBufferEvent::connect</span> .

### 参数

`base`  
Event base that should be associated with the new buffer event.

`socket`  
May be created as a stream(not necessarily by means of *sockets*
extension)

`options`  
One of
<a href="/class/eventbufferevent.html#预定义常量" class="link">EventBufferEvent::OPT_* constants</a>
, or **`0`** .

`readcb`  
Read event callback. See
<a href="/eventbufferevent/about/callbacks.html" class="link">About buffer event callbacks</a>
.

`writecb`  
Write event callback. See
<a href="/eventbufferevent/about/callbacks.html" class="link">About buffer event callbacks</a>
.

`eventcb`  
Status-change event callback. See
<a href="/eventbufferevent/about/callbacks.html" class="link">About buffer event callbacks</a>
.

`arg`  
A variable that will be passed to all the callbacks.

### 返回值

Returns buffer event resource optionally associated with socket
resource. \*/

### 参见

-   <span class="methodname">EventBufferEvent::sslFilter</span>
-   <span class="methodname">EventBufferEvent::sslSocket</span>

EventBufferEvent::createPair
============================

Creates two buffer events connected to each other

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">EventBufferEvent::createPair</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
\[, <span class="methodparam"> <span class="type">int</span> `$options`
<span class="initializer"> = 0</span> </span> \] )

Returns array of two <span class="classname">EventBufferEvent</span>
objects connected to each other. All the usual options are supported,
except for **`EventBufferEvent::OPT_CLOSE_ON_FREE`** , which has no
effect, and **`EventBufferEvent::OPT_DEFER_CALLBACKS`** , which is
always on.

### 参数

`base`  
Associated event base

`options`  
<a href="" class="link">EventBufferEvent::OPT_* constants</a> combined
with bitwise *OR* operator.

### 返回值

Returns array of two <span class="classname">EventBufferEvent</span>
objects connected to each other.

### 更新日志

| 版本             | 说明                |
|------------------|---------------------|
| PECL event 1.9.0 | Method made static. |

EventBufferEvent::disable
=========================

Disable events read, write, or both on a buffer event

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::disable</span> ( <span
class="methodparam"> <span class="type">int</span> `$events` </span> )

Disable events **`Event::READ`** , **`Event::WRITE`** , or
**`Event::READ`** *\|* **`Event::WRITE`** on a buffer event.

### 参数

`events`  

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBufferEvent::enable</span>

EventBufferEvent::enable
========================

Enable events read, write, or both on a buffer event

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::enable</span> ( <span
class="methodparam"> <span class="type">int</span> `$events` </span> )

Enable events **`Event::READ`** , **`Event::WRITE`** , or
**`Event::READ`** *\|* **`Event::WRITE`** on a buffer event.

### 参数

`events`  
**`Event::READ`** , **`Event::WRITE`** , or **`Event::READ`** *\|*
**`Event::WRITE`** on a buffer event.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBufferEvent::disable</span>

EventBufferEvent::free
======================

Free a buffer event

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBufferEvent::free</span> ( <span
class="methodparam">void</span> )

Free resources allocated by buffer event.

Usually there is no need to call this method, since normally it is done
within internal object destructors. However, sometimes we have a
long-time script allocating lots of instances, or a script with a heavy
memory usage, where we need to free resources as soon as possible. In
such cases <span class="methodname">EventBufferEvent::free</span> may be
used to protect the script against running up to the *memory\_limit* .

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventBufferEvent::getDnsErrorString
===================================

Returns string describing the last failed DNS lookup attempt

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::getDnsErrorString</span> (
<span class="methodparam">void</span> )

Returns string describing the last failed DNS lookup attempt made by
<span class="methodname">EventBufferEvent::connectHost</span> , or an
empty string, if there is no DNS error detected.

### 参数

此函数没有参数。

### 返回值

Returns a string describing DNS lookup error, or an empty string for no
error.

### 参见

-   <span class="methodname">EventBufferEvent::connectHost</span>

EventBufferEvent::getEnabled
============================

Returns bitmask of events currently enabled on the buffer event

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventBufferEvent::getEnabled</span> ( <span
class="methodparam">void</span> )

Returns bitmask of events currently enabled on the buffer event

### 参数

此函数没有参数。

### 返回值

Returns integer representing a bitmask of events currently enabled on
the buffer event

### 参见

-   <span class="methodname">EventBufferEvent::enable</span>
-   <span class="methodname">EventBufferEvent::disable</span>

EventBufferEvent::getInput
==========================

Returns underlying input buffer associated with current buffer event

### 说明

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">EventBufferEvent::getInput</span> ( <span
class="methodparam">void</span> )

Returns underlying input buffer associated with current buffer event. An
input buffer is a storage for data to read.

Note, there is also
*<a href="/class/eventbufferevent.html#" class="link">input</a>*
property of <span class="classname">EventBufferEvent</span> class.

### 参数

此函数没有参数。

### 返回值

Returns instance of <span class="classname">EventBuffer</span> input
buffer associated with current buffer event.

### 范例

**示例 \#1 Buffer event's read callback**

``` php
<?php
function readcb($bev, $base) {
    $input = $bev->input; //$bev->getInput();

    while (($n = $input->remove($buf, 1024)) > 0) {
        echo $buf;
    }
}
?>
```

### 参见

-   <span class="methodname">EventBufferEvent::getOutput</span>

EventBufferEvent::getOutput
===========================

Returns underlying output buffer associated with current buffer event

### 说明

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">EventBufferEvent::getOutput</span> ( <span
class="methodparam">void</span> )

Returns underlying output buffer associated with current buffer event.
An output buffer is a storage for data to be written.

Note, there is also
*<a href="/class/eventbufferevent.html#" class="link">output</a>*
property of <span class="classname">EventBufferEvent</span> class.

### 参数

此函数没有参数。

### 返回值

Returns instance of <span class="classname">EventBuffer</span> output
buffer associated with current buffer event.

### 范例

**示例 \#1 <span class="function">EventBufferEvent::getOutput</span>
example**

``` php
<?php
$base = new EventBase();

$dns_base = new EventDnsBase($base, TRUE); // Use async DNS resolving
if (!$dns_base) {
    exit("Failed to init DNS Base\n");
}

$bev = new EventBufferEvent($base, /* use internal socket */ NULL,
    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS,
    "readcb", /* writecb */ NULL, "eventcb", $base
);
if (!$bev) {
    exit("Failed creating bufferevent socket\n");
}

$bev->enable(Event::READ | Event::WRITE);

$output = $bev->getOutput();
if (!$output->add(
    "GET {$argv[2]} HTTP/1.0\r\n".
    "Host: {$argv[1]}\r\n".
    "Connection: Close\r\n\r\n"
)) {
    exit("Failed adding request to output buffer\n");
}

/* ... */
?>
```

### 参见

-   <span class="methodname">EventBufferEvent::getInput</span>

EventBufferEvent::read
======================

Read buffer's data

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::read</span> ( <span
class="methodparam"> <span class="type">int</span> `$size` </span> )

Removes up to `size` bytes from the input buffer. Returns a string of
data read from the input buffer.

### 参数

`size`  
Maximum number of bytes to read

### 返回值

Returns string of data read from the input buffer.

### 参见

-   <span class="methodname">EventBufferEvent::readBuffer</span>

EventBufferEvent::readBuffer
============================

Drains the entire contents of the input buffer and places them into buf

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::readBuffer</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

Drains the entire contents of the input buffer and places them into
`buf` .

### 参数

`buf`  
Target buffer

### 返回值

Returns **`TRUE`** on success; Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBufferEvent::read</span>

EventBufferEvent::setCallbacks
==============================

Assigns read, write and event(status) callbacks

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBufferEvent::setCallbacks</span> ( <span
class="methodparam"> <span class="type">callable</span> `$readcb`
</span> , <span class="methodparam"> <span class="type">callable</span>
`$writecb` </span> , <span class="methodparam"> <span
class="type">callable</span> `$eventcb` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$arg` </span> \]
)

Assigns read, write and event(status) callbacks.

### 参数

`readcb`  
Read event callback. See
<a href="/eventbufferevent/about/callbacks.html" class="link">About buffer event callbacks</a>
.

`writecb`  
Write event callback. See
<a href="/eventbufferevent/about/callbacks.html" class="link">About buffer event callbacks</a>
.

`eventcb`  
Status-change event callback. See
<a href="/eventbufferevent/about/callbacks.html" class="link">About buffer event callbacks</a>
.

`arg`  
A variable that will be passed to all the callbacks.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventBufferEvent::\_\_construct</span>

EventBufferEvent::setPriority
=============================

Assign a priority to a bufferevent

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::setPriority</span> ( <span
class="methodparam"> <span class="type">int</span> `$priority` </span> )

Assign a priority to a bufferevent

**Warning**

Only supported for socket buffer events

### 参数

`priority`  
Priority value.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventBufferEvent::setTimeouts
=============================

Set the read and write timeout for a buffer event

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::setTimeouts</span> ( <span
class="methodparam"> <span class="type">float</span> `$timeout_read`
</span> , <span class="methodparam"> <span class="type">float</span>
`$timeout_write` </span> )

Set the read and write timeout for a buffer event

### 参数

`timeout_read`  
Read timeout

`timeout_write`  
Write timeout

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventBufferEvent::setWatermark
==============================

Adjusts read and/or write watermarks

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBufferEvent::setWatermark</span> ( <span
class="methodparam"> <span class="type">int</span> `$events` </span> ,
<span class="methodparam"> <span class="type">int</span> `$lowmark`
</span> , <span class="methodparam"> <span class="type">int</span>
`$highmark` </span> )

Adjusts the read watermarks, the write *watermarks* , or both, of a
single buffer event.

A buffer event watermark is an edge, a value specifying number of bytes
to be read or written before callback is invoked. By default every
read/write event triggers a callback invokation. See
<a href="http://www.wangafu.net/~nickm/libevent-book/Ref6_bufferevent.html#_callbacks_and_watermarks" class="link external">» Fast portable non-blocking network programming with Libevent: Callbacks and watermarks</a>

### 参数

`events`  
Bitmask of **`Event::READ`** , **`Event::WRITE`** , or both.

`lowmark`  
Minimum watermark value.

`highmark`  
Maximum watermark value. **`0`** means "unlimited".

### 返回值

没有返回值。

EventBufferEvent::sslError
==========================

Returns most recent OpenSSL error reported on the buffer event

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::sslError</span> ( <span
class="methodparam">void</span> )

Returns most recent OpenSSL error reported on the buffer event.

> **Note**:
>
> This function is available only if *Event* is compiled with OpenSSL
> support.

### 参数

此函数没有参数。

### 返回值

Returns OpenSSL error string reported on the buffer event, or
**`FALSE`**, if there is no more error to return.

### 范例

**示例 \#1 <span class="function">EventBufferEvent::sslError</span>
example**

``` php
<?php
// This callback is invoked when some even occurs on the event listener,
// e.g. connection closed, or an error occured
function ssl_event_cb($bev, $events, $ctx) {
    if ($events & EventBufferEvent::ERROR) {
        // Fetch errors from the SSL error stack
        while ($err = $bev->sslError()) {
            fprintf(STDERR, "Bufferevent error %s.\n", $err);
        }
    }

    if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {
        $bev->free();
    }
}
?>
```

### 参见

-   <span class="methodname">EventBufferEvent::sslRenegotiate</span>

EventBufferEvent::sslFilter
===========================

Create a new SSL buffer event to send its data over another buffer event

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">EventBufferEvent</span> <span
class="methodname">EventBufferEvent::sslFilter</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">EventBufferEvent</span>
`$underlying` </span> , <span class="methodparam"> <span
class="type">EventSslContext</span> `$ctx` </span> , <span
class="methodparam"> <span class="type">int</span> `$state` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$options`
<span class="initializer"> = 0</span> </span> \] )

Create a new SSL buffer event to send its data over another buffer event

> **Note**:
>
> This function is available only if *Event* is compiled with OpenSSL
> support.

### 参数

`base`  
Associated event base.

`underlying`  
A socket buffer event to use for this SSL.

`ctx`  
Object of <span class="classname">EventSslContext</span> class.

`state`  
The current state of SSL connection: **`EventBufferEvent::SSL_OPEN`** ,
**`EventBufferEvent::SSL_ACCEPTING`** or
**`EventBufferEvent::SSL_CONNECTING`** .

`options`  
One or more buffer event options.

### 返回值

Returns a new SSL <span class="classname">EventBufferEvent</span>
object.

### 范例

**示例 \#1 Simple SMTP server**

``` php
<?php
 /*
 * Author: Andrew Rose <hello at andrewrose dot co dot uk>
 *
 * Usage:
 * 1) Prepare cert.pem certificate and privkey.pem private key files.
 * 2) Launch the server script
 * 3) Open TLS connection, e.g.:
 *      $ openssl s_client -connect localhost:25 -starttls smtp -crlf
 * 4) Start testing the commands listed in `cmd` method below.
 */

class Handler {
    public $domainName = FALSE;
    public $connections = [];
    public $buffers = [];
    public $maxRead = 256000;

    public function __construct() {
        $this->ctx = new EventSslContext(EventSslContext::SSLv3_SERVER_METHOD, [
            EventSslContext::OPT_LOCAL_CERT  => 'cert.pem',
            EventSslContext::OPT_LOCAL_PK    => 'privkey.pem',
            //EventSslContext::OPT_PASSPHRASE  => '',
            EventSslContext::OPT_VERIFY_PEER => false, // change to true with authentic cert
            EventSslContext::OPT_ALLOW_SELF_SIGNED => true // change to false with authentic cert
        ]);

        $this->base = new EventBase();
        if (!$this->base) {
            exit("Couldn't open event base\n");
        }

        if (!$this->listener = new EventListener($this->base,
            [$this, 'ev_accept'],
            $this->ctx,
            EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE,
            -1,
            '0.0.0.0:25'))
        {
            exit("Couldn't create listener\n");
        }

        $this->listener->setErrorCallback([$this, 'ev_error']);
        $this->base->dispatch();
    }

    public function ev_accept($listener, $fd, $address, $ctx) {
        static $id = 0;
        $id += 1;

        $this->connections[$id]['clientData'] = '';
        $this->connections[$id]['cnx'] = new EventBufferEvent($this->base, $fd,
            EventBufferEvent::OPT_CLOSE_ON_FREE);

        if (!$this->connections[$id]['cnx']) {
            echo "Failed creating buffer\n";
            $this->base->exit(NULL);
            exit(1);
        }

        $this->connections[$id]['cnx']->setCallbacks([$this, "ev_read"], NULL,
            [$this, 'ev_error'], $id);
        $this->connections[$id]['cnx']->enable(Event::READ | Event::WRITE);

        $this->ev_write($id, '220 '.$this->domainName." wazzzap?\r\n");
    }

    function ev_error($listener, $ctx) {
        $errno = EventUtil::getLastSocketErrno();

        fprintf(STDERR, "Got an error %d (%s) on the listener. Shutting down.\n",
            $errno, EventUtil::getLastSocketError());

        if ($errno != 0) {
            $this->base->exit(NULL);
            exit();
        }
    }

    public function ev_close($id) {
        $this->connections[$id]['cnx']->disable(Event::READ | Event::WRITE);
        unset($this->connections[$id]);
    }

    protected function ev_write($id, $string) {
        echo 'S('.$id.'): '.$string;
        $this->connections[$id]['cnx']->write($string);
    }

    public function ev_read($buffer, $id) {
        while($buffer->input->length > 0) {
            $this->connections[$id]['clientData'] .= $buffer->input->read($this->maxRead);
            $clientDataLen = strlen($this->connections[$id]['clientData']);

            if($this->connections[$id]['clientData'][$clientDataLen-1] == "\n"
                && $this->connections[$id]['clientData'][$clientDataLen-2] == "\r")
            {
                // remove the trailing \r\n
                $line = substr($this->connections[$id]['clientData'], 0,
                    strlen($this->connections[$id]['clientData']) - 2);

                $this->connections[$id]['clientData'] = '';
                $this->cmd($buffer, $id, $line);
            }
        }
    }

    protected function cmd($buffer, $id, $line) {
        switch ($line) {
            case strncmp('EHLO ', $line, 4):
                $this->ev_write($id, "250-STARTTLS\r\n");
                $this->ev_write($id, "250 OK ehlo\r\n");
                break;

            case strncmp('HELO ', $line, 4):
                $this->ev_write($id, "250-STARTTLS\r\n");
                $this->ev_write($id, "250 OK helo\r\n");
                break;

            case strncmp('QUIT', $line, 3):
                $this->ev_write($id, "250 OK quit\r\n");
                $this->ev_close($id);
                break;

            case strncmp('STARTTLS', $line, 3):
                $this->ev_write($id, "220 Ready to start TLS\r\n");
                $this->connections[$id]['cnx'] = EventBufferEvent::sslFilter($this->base,
                    $this->connections[$id]['cnx'], $this->ctx,
                    EventBufferEvent::SSL_ACCEPTING,
                    EventBufferEvent::OPT_CLOSE_ON_FREE);
                $this->connections[$id]['cnx']->setCallbacks([$this, "ev_read"], NULL, [$this, 'ev_error'], $id);
                $this->connections[$id]['cnx']->enable(Event::READ | Event::WRITE);
                break;

            default:
                echo 'unknown command: '.$line."\n";
                break;
        }
    }
}

new Handler();
```

### 参见

-   <span class="methodname">EventBufferEvent::sslSocket</span>

EventBufferEvent::sslGetCipherInfo
==================================

Returns a textual description of the cipher

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::sslGetCipherInfo</span> (
<span class="methodparam">void</span> )

Retrieves description of the current cipher by means of the
*SSL\_CIPHER\_description* SSL API function (see
*SSL\_CIPHER\_get\_name(3)* man page).

> **Note**:
>
> This function is available only if *Event* is compiled with OpenSSL
> support.

### 参数

此函数没有参数。

### 返回值

Returns a textual description of the cipher on success, or **`FALSE`**
on error.

EventBufferEvent::sslGetCipherName
==================================

Returns the current cipher name of the SSL connection

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::sslGetCipherName</span> (
<span class="methodparam">void</span> )

Retrieves name of cipher used by current SSL connection.

> **Note**:
>
> This function is available only if *Event* is compiled with OpenSSL
> support.

### 参数

此函数没有参数。

### 返回值

Returns the current cipher name of the SSL connection, or **`FALSE`** on
error.

EventBufferEvent::sslGetCipherVersion
=====================================

Returns version of cipher used by current SSL connection

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::sslGetCipherVersion</span> (
<span class="methodparam">void</span> )

Retrieves version of cipher used by current SSL connection.

> **Note**:
>
> This function is available only if *Event* is compiled with OpenSSL
> support.

### 参数

此函数没有参数。

### 返回值

Returns the current cipher version of the SSL connection, or **`FALSE`**
on error.

EventBufferEvent::sslGetProtocol
================================

Returns the name of the protocol used for current SSL connection

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventBufferEvent::sslGetProtocol</span> ( <span
class="methodparam">void</span> )

Returns the name of the protocol used for current SSL connection.

> **Note**:
>
> This function is available only if *Event* is compiled with OpenSSL
> support.

### 参数

此函数没有参数。

### 返回值

Returns the name of the protocol used for current SSL connection.

EventBufferEvent::sslRenegotiate
================================

Tells a bufferevent to begin SSL renegotiation

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventBufferEvent::sslRenegotiate</span> ( <span
class="methodparam">void</span> )

Tells a bufferevent to begin SSL renegotiation.

**Warning**

Calling this function tells the SSL to renegotiate, and the buffer event
to invoke appropriate callbacks. This is an advanced topic; this should
be generally avoided unless one really knows what he/she does,
especially since many SSL versions have had known security issues
related to renegotiation.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventBufferEvent::sslSocket
===========================

Creates a new SSL buffer event to send its data over an SSL on a socket

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">EventBufferEvent</span> <span
class="methodname">EventBufferEvent::sslSocket</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">mixed</span> `$socket`
</span> , <span class="methodparam"> <span
class="type">EventSslContext</span> `$ctx` </span> , <span
class="methodparam"> <span class="type">int</span> `$state` </span> \[,
<span class="methodparam"> <span class="type">int</span> `$options`
</span> \] )

Creates a new SSL buffer event to send its data over an SSL on a socket.

### 参数

`base`  
Associated event base.

`socket`  
Socket to use for this SSL. Can be stream or socket resource, numeric
file descriptor, or **`NULL`**. If `socket` is **`NULL`**, it is assumed
that the file descriptor for the socket will be assigned later, for
instance, by means of <span
class="methodname">EventBufferEvent::connectHost</span> method.

`ctx`  
Object of <span class="classname">EventSslContext</span> class.

`state`  
The current state of SSL connection: **`EventBufferEvent::SSL_OPEN`** ,
**`EventBufferEvent::SSL_ACCEPTING`** or
**`EventBufferEvent::SSL_CONNECTING`** .

`options`  
The buffer event options.

### 返回值

Returns <span class="classname">EventBufferEvent</span> object.

### 参见

-   <span class="methodname">EventBufferEvent::sslFilter</span>

EventBufferEvent::write
=======================

Adds data to a buffer event's output buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::write</span> ( <span
class="methodparam"> <span class="type">string</span> `$data` </span> )

Adds `data` to a buffer event's output buffer

### 参数

`data`  
Data to be added to the underlying buffer.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBufferEvent::writeBuffer</span>

EventBufferEvent::writeBuffer
=============================

Adds contents of the entire buffer to a buffer event's output buffer

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventBufferEvent::writeBuffer</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

Adds contents of the entire buffer to a buffer event's output buffer

### 参数

`buf`  
Source <span class="classname">EventBuffer</span> object.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventBufferEvent::write</span>

简介
----

Represents configuration structure which could be used in construction
of the <span class="classname">EventBase</span> .

类摘要
------

**EventConfig**

<span class="ooclass"> <span class="modifier">final</span> class
**EventConfig** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventConfig::FEATURE_ET` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventConfig::FEATURE_O1` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventConfig::FEATURE_FDS` <span class="initializer"> = 4</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">avoidMethod</span> ( <span class="methodparam">
<span class="type">string</span> `$method` </span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">requireFeatures</span> ( <span
class="methodparam"> <span class="type">int</span> `$feature` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMaxDispatchInterval</span> ( <span
class="methodparam"> <span class="type">int</span> `$max_interval`
</span> , <span class="methodparam"> <span class="type">int</span>
`$max_callbacks` </span> , <span class="methodparam"> <span
class="type">int</span> `$min_priority` </span> )

}

预定义常量
----------

**`EventConfig::FEATURE_ET`**  
Requires a backend method that supports edge-triggered I/O.

**`EventConfig::FEATURE_O1`**  
Requires a backend method where adding or deleting a single event, or
having a single event become active, is an O(1) operation.

**`EventConfig::FEATURE_FDS`**  
Requires a backend method that can support arbitrary file descriptor
types, and not just sockets.

EventConfig::avoidMethod
========================

Tells libevent to avoid specific event method

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventConfig::avoidMethod</span> ( <span
class="methodparam"> <span class="type">string</span> `$method` </span>
)

Tells libevent to avoid specific event method(backend). See
<a href="http://www.wangafu.net/~nickm/libevent-book/Ref2_eventbase.html#_creating_an_event_base" class="link external">» Creating an event base</a>
.

### 参数

`method`  
The backend method to avoid. See
<a href="/class/eventconfig.html#预定义常量" class="link">EventConfig constants</a>
.

### 返回值

Returns **`TRUE`** on success, otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventConfig::avoidMethod</span>
example**

``` php
<?php
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "`select' method avoided\n";
}
?>
```

### 参见

-   <span class="methodname">EventBase::\_\_construct</span>

EventConfig::\_\_construct
==========================

Constructs EventConfig object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventConfig::\_\_construct</span> ( <span
class="methodparam">void</span> )

Constructs EventConfig object which could be passed to <span
class="methodname">EventBase::\_\_construct</span> constructor.

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">EventConfig</span> object.

### 范例

**示例 \#1 <span class="function">EventConfig::\_\_construct</span>
example**

``` php
<?php
// Avoiding "select" method
$cfg = new EventConfig();
if ($cfg->avoidMethod("select")) {
    echo "`select' method avoided\n";
}

// Create event_base associated with the config
$base = new EventBase($cfg);

/* Now $base is configured to avoid select backend(method) */
?>
```

### 参见

-   <span class="methodname">EventBase::\_\_construct</span>

EventConfig::requireFeatures
============================

Enters a required event method feature that the application demands

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventConfig::requireFeatures</span> ( <span
class="methodparam"> <span class="type">int</span> `$feature` </span> )

Enters a required event method feature that the application demands

### 参数

`feature`  
Bitmask of required features. See
<a href="/class/eventconfig.html#预定义常量" class="link"><em>EventConfig::FEATURE_*</em> constants</a>

### 返回值

### 范例

**示例 \#1 <span class="function">EventConfig::requireFeatures</span>
example**

``` php
<?php
$cfg = new EventConfig();

// Create event_base associated with the config
$base = new EventBase($cfg);

// Require FDS feature
if ($cfg->requireFeatures(EventConfig::FEATURE_FDS)) {
    echo "FDS feature is now requried\n";

    $base = new EventBase($cfg);
    ($base->getFeatures() & EventConfig::FEATURE_FDS)
        and print("FDS - arbitrary file descriptor types, and not just sockets\n");
}
?>
```

以上例程的输出类似于：

    FDS feature is now requried
    FDS - arbitrary file descriptor types, and not just sockets

### 参见

-   <span class="methodname">EventBase::getFeatures</span>

EventConfig::setMaxDispatchInterval
===================================

Prevents priority inversion

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventConfig::setMaxDispatchInterval</span> (
<span class="methodparam"> <span class="type">int</span> `$max_interval`
</span> , <span class="methodparam"> <span class="type">int</span>
`$max_callbacks` </span> , <span class="methodparam"> <span
class="type">int</span> `$min_priority` </span> )

Prevents priority inversion by limiting how many low-priority event
callbacks can be invoked before checking for more high-priority events.

> **Note**:
>
> Available since *libevent 2.1.0-alpha* .

### 参数

`max_interval`  
An interval after which Libevent should stop running callbacks and check
for more events, or **`0`** , if there should be no such interval.

`max_callbacks`  
A number of callbacks after which Libevent should stop running callbacks
and check for more events, or **`-1`** , if there should be no such
limit.

`min_priority`  
A priority below which `max_interval` and `max_callbacks` should not be
enforced. If this is set to **`0`** , they are enforced for events of
every priority; if it's set to **`1`** , they're enforced for events of
priority **`1`** and above, and so on.

### 返回值

Returns **`TRUE`** on success, otherwise **`FALSE`**.

简介
----

Represents Libevent's DNS base structure. Used to resolve DNS
asyncronously, parse configuration files like resolv.conf etc.

类摘要
------

**EventDnsBase**

<span class="ooclass"> <span class="modifier">final</span> class
**EventDnsBase** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventDnsBase::OPTION_SEARCH` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventDnsBase::OPTION_NAMESERVERS` <span class="initializer"> = 2</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventDnsBase::OPTION_MISC` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventDnsBase::OPTION_HOSTSFILE` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventDnsBase::OPTIONS_ALL` <span class="initializer"> = 15</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addNameserverIp</span> ( <span
class="methodparam"> <span class="type">string</span> `$ip` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addSearch</span> ( <span class="methodparam">
<span class="type">string</span> `$domain` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clearSearch</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">bool</span> `$initialize`
</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">countNameservers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">loadHosts</span> ( <span class="methodparam">
<span class="type">string</span> `$hosts` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">parseResolvConf</span> ( <span
class="methodparam"> <span class="type">int</span> `$flags` </span> ,
<span class="methodparam"> <span class="type">string</span> `$filename`
</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOption</span> ( <span class="methodparam">
<span class="type">string</span> `$option` </span> , <span
class="methodparam"> <span class="type">string</span> `$value` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSearchNdots</span> ( <span
class="methodparam"> <span class="type">int</span> `$ndots` </span> )

}

预定义常量
----------

**`EventDnsBase::OPTION_SEARCH`**  
Tells to read the domain and search fields from the *resolv.conf* file
and the *ndots* option, and use them to decide which domains(if any) to
search for hostnames that aren’t fully-qualified.

**`EventDnsBase::OPTION_NAMESERVERS`**  
Tells to learn the nameservers from the *resolv.conf* file.

**`EventDnsBase::OPTION_MISC`**  

**`EventDnsBase::OPTION_HOSTSFILE`**  
Tells to read a list of hosts from */etc/hosts* as part of loading the
*resolv.conf* file.

**`EventDnsBase::OPTIONS_ALL`**  
Tells to learn as much as it can from the *resolv.conf* file.

EventDnsBase::addNameserverIp
=============================

Adds a nameserver to the DNS base

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventDnsBase::addNameserverIp</span> ( <span
class="methodparam"> <span class="type">string</span> `$ip` </span> )

Adds a nameserver to the evdns\_base.

### 参数

`ip`  
The nameserver string, either as an IPv4 address, an IPv6 address, an
IPv4 address with a port ( *IPv4:Port* ), or an IPv6 address with a port
( *\[IPv6\]:Port* ).

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventDnsBase::addSearch
=======================

Adds a domain to the list of search domains

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventDnsBase::addSearch</span> ( <span
class="methodparam"> <span class="type">string</span> `$domain` </span>
)

Adds a domain to the list of search domains

### 参数

`domain`  
Search domain.

### 返回值

没有返回值。

EventDnsBase::clearSearch
=========================

Removes all current search suffixes

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventDnsBase::clearSearch</span> ( <span
class="methodparam">void</span> )

Removes all current search suffixes from the DNS base; the <span
class="methodname">EventDnsBase::addSearch</span> function adds a
suffix.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventDnsBase::addSearch</span>

EventDnsBase::\_\_construct
===========================

Constructs EventDnsBase object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventDnsBase::\_\_construct</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">bool</span>
`$initialize` </span> )

Constructs EventDnsBase object.

### 参数

`base`  
Event base.

`initialize`  
If the `initialize` argument is **`TRUE`**, it tries to configure the
DNS base sensibly given your operating system’s default. Otherwise, it
leaves the event DNS base empty, with no nameservers or options
configured. In the latter case DNS base should be configured manually,
e.g. with <span class="methodname">EventDnsBase::parseResolvConf</span>
.

### 返回值

Returns EventDnsBase object.

EventDnsBase::countNameservers
==============================

Gets the number of configured nameservers

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventDnsBase::countNameservers</span> ( <span
class="methodparam">void</span> )

Gets the number of configured nameservers

### 参数

此函数没有参数。

### 返回值

Returns the number of configured nameservers(not necessarily the number
of running nameservers). This is useful for double-checking whether our
calls to the various nameserver configuration functions have been
successful.

EventDnsBase::loadHosts
=======================

Loads a hosts file (in the same format as /etc/hosts) from hosts file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventDnsBase::loadHosts</span> ( <span
class="methodparam"> <span class="type">string</span> `$hosts` </span> )

Loads a hosts file (in the same format as */etc/hosts* ) from hosts
file.

### 参数

`hosts`  
Path to the hosts' file.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventDnsBase::parseResolvConf
=============================

Scans the resolv.conf-formatted file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventDnsBase::parseResolvConf</span> ( <span
class="methodparam"> <span class="type">int</span> `$flags` </span> ,
<span class="methodparam"> <span class="type">string</span> `$filename`
</span> )

Scans the resolv.conf-formatted file stored in filename, and read in all
the options from it that are listed in flags

### 参数

`flags`  
Determines what information is parsed from the *resolv.conf* file. See
the man page for *resolv.conf* for the format of this file.

The following directives are not parsed from the file: *sortlist,
rotate, no-check-names, inet6, debug* .

If this function encounters an error, the possible return values are:

-   **`1`** = failed to open file
-   **`2`** = failed to stat file
-   **`3`** = file too large
-   **`4`** = out of memory
-   **`5`** = short read from file
-   **`6`** = no nameservers listed in the file

`filename`  
Path to *resolv.conf* file.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventDnsBase::setOption
=======================

Set the value of a configuration option

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventDnsBase::setOption</span> ( <span
class="methodparam"> <span class="type">string</span> `$option` </span>
, <span class="methodparam"> <span class="type">string</span> `$value`
</span> )

Set the value of a configuration option.

### 参数

`option`  
The currently available configuration options are: *"ndots"* ,
*"timeout"* , *"max-timeouts"* , *"max-inflight"* , and *"attempts"* .

`value`  
Option value.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventDnsBase::setSearchNdots
============================

Set the 'ndots' parameter for searches

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventDnsBase::setSearchNdots</span> ( <span
class="methodparam"> <span class="type">int</span> `$ndots` </span> )

Set the **`'ndots'`** parameter for searches. Sets the number of dots
which, when found in a name, causes the first query to be without any
search domain.

### 参数

`ndots`  
The number of dots.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

简介
----

Represents HTTP server.

类摘要
------

**EventHttp**

<span class="ooclass"> <span class="modifier">final</span> class
**EventHttp** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">accept</span> ( <span class="methodparam">
<span class="type">mixed</span> `$socket` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addServerAlias</span> ( <span
class="methodparam"> <span class="type">string</span> `$alias` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">bind</span> ( <span class="methodparam"> <span
class="type">string</span> `$address` </span> , <span
class="methodparam"> <span class="type">int</span> `$port` </span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> \[, <span
class="methodparam"> <span class="type">EventSslContext</span> `$ctx`
<span class="initializer"> = **`NULL`**</span> </span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">removeServerAlias</span> ( <span
class="methodparam"> <span class="type">string</span> `$alias` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAllowedMethods</span> ( <span
class="methodparam"> <span class="type">int</span> `$methods` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCallback</span> ( <span class="methodparam">
<span class="type">string</span> `$path` </span> , <span
class="methodparam"> <span class="type">string</span> `$cb` </span> \[,
<span class="methodparam"> <span class="type">string</span> `$arg`
</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setDefaultCallback</span> ( <span
class="methodparam"> <span class="type">string</span> `$cb` </span> \[,
<span class="methodparam"> <span class="type">string</span> `$arg`
</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMaxBodySize</span> ( <span
class="methodparam"> <span class="type">int</span> `$value` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMaxHeadersSize</span> ( <span
class="methodparam"> <span class="type">int</span> `$value` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setTimeout</span> ( <span class="methodparam">
<span class="type">int</span> `$value` </span> )

}

EventHttp::accept
=================

Makes an HTTP server accept connections on the specified socket stream
or resource

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventHttp::accept</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span> )

Makes an HTTP server accept connections on the specified socket stream
or resource. The socket should be ready to accept connections.

Can be called multiple times to accept connections on different sockets.

> **Note**:
>
> To bind a socket, *listen* , and *accept* connections on the socket in
> s single call use <span class="methodname">EventHttp::bind</span> .
> <span class="methodname">EventHttp::accept</span> is needed only if
> one already has a socket ready to accept connections.

### 参数

`socket`  
Socket resource, stream or numeric file descriptor representing a socket
ready to accept connections.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventHttp::accept</span> example**

``` php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$addresses = array (
     8091 => "127.0.0.1",
     8092 => "127.0.0.2",
);
$i = 0;

$socket = array();

foreach ($addresses as $port => $ip) {
    echo $ip, " ", $port, PHP_EOL;
    $socket[$i] = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
    if (!socket_bind($socket[$i], $ip, $port)) {
        exit("socket_bind failed\n");
    }
    socket_listen($socket[$i], 0);
    socket_set_nonblock($socket[$i]);

    if (!$http->accept($socket[$i])) {
        echo "Accept failed\n";
        exit(1);
    }

    ++$i;
}

$http->setCallback("/some-page", function() {
 echo "(some-page)\n";
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
    echo "OK\n";
});

$http->setDefaultCallback(function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
    echo "OK\n";
});

$signal = Event::signal($base, SIGINT, function () use ($base) {
    echo "Caught SIGINT. Stopping...\n";
    $base->stop();
});
$signal->add();

$base->dispatch();
echo "END\n";
// We didn't close sockets, since Libevent already sets
// CLOSE_ON_FREE and CLOSE_ON_EXEC flags on the file 
// descriptor associated with the sockets.
?>
```

以上例程的输出类似于：

    Client:
    $ nc 127.0.0.1 8091
    GET /about HTTP/1.0
    Connection: close

    HTTP/1.0 200 OK
    Content-Type: text/html; charset=ISO-8859-1
    Connection: close

    Server:
    127.0.0.1 8091
    127.0.0.2 8092
    URI: /about
    OK

### 参见

-   <span class="methodname">EventHttp::bind</span>

EventHttp::addServerAlias
=========================

Adds a server alias to the HTTP server object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventHttp::addServerAlias</span> ( <span
class="methodparam"> <span class="type">string</span> `$alias` </span> )

Adds a server alias to the HTTP server object.

### 参数

`alias`  
The alias to add.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventHttp::addServerAlias</span>
example**

``` php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) failed\n");
};

if (!$http->addServerAlias("local.net")) {
    exit("Failed to add server alias\n");
}

$http->setCallback("/about", function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
});
$base->dispatch();
?>
```

### 参见

-   <span class="methodname">EventHttp::removeServerAlias</span>

EventHttp::bind
===============

Binds an HTTP server on the specified address and port

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::bind</span> ( <span
class="methodparam"> <span class="type">string</span> `$address` </span>
, <span class="methodparam"> <span class="type">int</span> `$port`
</span> )

Binds an HTTP server on the specified address and port.

Can be called multiple times to bind the same HTTP server to multiple
different ports.

### 参数

`address`  
A string containing the IP address to *listen(2)* on.

`port`  
The port number to listen on.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventHttp::bind</span> example**

``` php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) failed\n");
};
if (!$http->bind("127.0.0.1", 8089)) {
    exit("bind(2) failed\n");
};

$http->setCallback("/about", function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
    echo "OK\n";
});

$base->dispatch();
?>
```

以上例程的输出类似于：

    Client:

    $ nc 127.0.0.1 8088
    GET /about HTTP/1.0
    Connection: close

    HTTP/1.0 200 OK
    Content-Type: text/html; charset=ISO-8859-1
    Connection: close

    $ nc 127.0.0.1 8089
    GET /unknown HTTP/1.0
    Connection: close

    HTTP/1.1 404 Not Found
    Content-Type: text/html
    Date: Wed, 13 Mar 2013 04:14:41 GMT
    Content-Length: 149
    Connection: close

    <html><head><title>404 Not Found</title></head><body><h1>Not Found</h1><p>The requested URL /unknown was not found on this server.</p></body></html>

    Server:
    URI: /about
    OK

### 参见

-   <span class="methodname">EventHttp::accept</span>

EventHttp::\_\_construct
========================

Constructs EventHttp object(the HTTP server)

### 说明

<span class="modifier">public</span> <span
class="methodname">EventHttp::\_\_construct</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
\[, <span class="methodparam"> <span class="type">EventSslContext</span>
`$ctx` <span class="initializer"> = **`NULL`**</span> </span> \] )

Constructs the HTTP server object.

### 参数

`base`  
Associated event base.

`ctx`  
<span class="classname">EventSslContext</span> class object. Turns plain
HTTP server into HTTPS server. It means that if `ctx` is configured
correctly, then the underlying buffer events will be based on OpenSSL
sockets. Thus, all traffic will pass through the SSL or TLS.

> **Note**:
>
> This parameter is available only if *Event* is compiled with OpenSSL
> support and only with *Libevent 2.1.0-alpha* and higher.

### 返回值

Returns <span class="classname">EventHttp</span> object.

### 更新日志

| 版本             | 说明                           |
|------------------|--------------------------------|
| PECL event 1.9.0 | OpenSSL support (`ctx`) added. |

### 范例

**示例 \#1 Simple HTTP server**

``` php
<?php
/*
 * Simple HTTP server.
 *
 * To test it:
 * 1) Run it on a port of your choice, e.g.:
 * $ php examples/http.php 8010
 * 2) In another terminal connect to some address on this port
 * and make GET or POST request(others are turned off here), e.g.:
 * $ nc -t 127.0.0.1 8010
 * POST /about HTTP/1.0
 * Content-Type: text/plain
 * Content-Length: 4
 * Connection: close
 * (press Enter)
 *
 * It will output
 * a=12
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 *
 * $ nc -t 127.0.0.1 8010
 * GET /dump HTTP/1.0
 * Content-Type: text/plain
 * Content-Encoding: UTF-8
 * Connection: close
 * (press Enter)
 *
 * It will output:
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 * (press Enter)
 *
 * $ nc -t 127.0.0.1 8010
 * GET /unknown HTTP/1.0
 * Connection: close
 *
 * It will output:
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 *
 * 3) See what the server outputs on the previous terminal window.
 */

function _http_dump($req, $data) {
    static $counter      = 0;
    static $max_requests = 2;

    if (++$counter >= $max_requests)  {
        echo "Counter reached max requests $max_requests. Exiting\n";
        exit();
    }

    echo __METHOD__, " called\n";
    echo "request:"; var_dump($req);
    echo "data:"; var_dump($data);

    echo "\n===== DUMP =====\n";
    echo "Command:", $req->getCommand(), PHP_EOL;
    echo "URI:", $req->getUri(), PHP_EOL;
    echo "Input headers:"; var_dump($req->getInputHeaders());
    echo "Output headers:"; var_dump($req->getOutputHeaders());

    echo "\n >> Sending reply ...";
    $req->sendReply(200, "OK");
    echo "OK\n";

    echo "\n >> Reading input buffer ...\n";
    $buf = $req->getInputBuffer();
    while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
        echo $s, PHP_EOL;
    }
    echo "No more data in the buffer\n";
}

function _http_about($req) {
    echo __METHOD__, PHP_EOL;
    echo "URI: ", $req->getUri(), PHP_EOL;
    echo "\n >> Sending reply ...";
    $req->sendReply(200, "OK");
    echo "OK\n";
}

function _http_default($req, $data) {
    echo __METHOD__, PHP_EOL;
    echo "URI: ", $req->getUri(), PHP_EOL;
    echo "\n >> Sending reply ...";
    $req->sendReply(200, "OK");
    echo "OK\n";
}

$port = 8010;
if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Invalid port");
}

$base = new EventBase();
$http = new EventHttp($base);
$http->setAllowedMethods(EventHttpRequest::CMD_GET | EventHttpRequest::CMD_POST);

$http->setCallback("/dump", "_http_dump", array(4, 8));
$http->setCallback("/about", "_http_about");
$http->setDefaultCallback("_http_default", "custom data value");

$http->bind("0.0.0.0", 8010);
$base->loop();
?>
```

以上例程的输出类似于：

    a=12
    HTTP/1.0 200 OK
    Content-Type: text/html; charset=ISO-8859-1
    Connection: close

    HTTP/1.0 200 OK
    Content-Type: text/html; charset=ISO-8859-1
    Connection: close
    (press Enter)

    HTTP/1.0 200 OK
    Content-Type: text/html; charset=ISO-8859-1
    Connection: close

EventHttp::removeServerAlias
============================

Removes server alias

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventHttp::removeServerAlias</span> ( <span
class="methodparam"> <span class="type">string</span> `$alias` </span> )

Removes server alias added with <span
class="methodname">EventHttp::addServerAlias</span>

### 参数

`alias`  
The alias to remove.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventHttp::addServerAlias</span>

EventHttp::setAllowedMethods
============================

Sets the what HTTP methods are supported in requests accepted by this
server, and passed to user callbacks

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::setAllowedMethods</span> ( <span
class="methodparam"> <span class="type">int</span> `$methods` </span> )

Sets the what HTTP methods are supported in requests accepted by this
server, and passed to user callbacks

If not supported they will generate a *"405 Method not allowed"*
response.

By default this includes the following methods: *GET* , *POST* , *HEAD*
, *PUT* , *DELETE* . See *EventHttpRequest::CMD\_\** constants.

### 参数

`methods`  
A bit mask of
<a href="/class/eventhttprequest.html#预定义常量" class="link"><em>EventHttpRequest::CMD_*</em> constants</a>
.

### 返回值

没有返回值。

EventHttp::setCallback
======================

Sets a callback for specified URI

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::setCallback</span> ( <span
class="methodparam"> <span class="type">string</span> `$path` </span> ,
<span class="methodparam"> <span class="type">string</span> `$cb`
</span> \[, <span class="methodparam"> <span class="type">string</span>
`$arg` </span> \] )

Sets a callback for specified URI.

### 参数

`path`  
The path for which to invoke the callback.

`cb`  
The callback <span class="type">callable</span> that gets invoked on
requested `path` . It should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span
class="type">EventHttpRequest</span> `$req` <span class="initializer"> =
NULL</span> </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$arg` <span class="initializer"> =
NULL</span> </span> \]\] )

`req`  
<span class="classname">EventHttpRequest</span> object.

`arg`  
Custom data.

`arg`  
Custom data.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventHttp::setCallback</span>
example**

``` php
<?php
/*
 * Simple HTTP server.
 *
 * To test it:
 * 1) Run it on a port of your choice, e.g.:
 * $ php examples/http.php 8010
 * 2) In another terminal connect to some address on this port
 * and make GET or POST request(others are turned off here), e.g.:
 * $ nc -t 127.0.0.1 8010
 * POST /about HTTP/1.0
 * Content-Type: text/plain
 * Content-Length: 4
 * Connection: close
 * (press Enter)
 *
 * It will output
 * a=12
 * HTTP/1.0 200 OK
 * Content-Type: text/html; charset=ISO-8859-1
 * Connection: close
 *
 * 3) See what the server outputs on the previous terminal window.
 */

function _http_dump($req, $data) {
    static $counter      = 0;
    static $max_requests = 2;

    if (++$counter >= $max_requests)  {
        echo "Counter reached max requests $max_requests. Exiting\n";
        exit();
    }

    echo __METHOD__, " called\n";
    echo "request:"; var_dump($req);
    echo "data:"; var_dump($data);

    echo "\n===== DUMP =====\n";
    echo "Command:", $req->getCommand(), PHP_EOL;
    echo "URI:", $req->getUri(), PHP_EOL;
    echo "Input headers:"; var_dump($req->getInputHeaders());
    echo "Output headers:"; var_dump($req->getOutputHeaders());

    echo "\n >> Sending reply ...";
    $req->sendReply(200, "OK");
    echo "OK\n";

    echo "\n >> Reading input buffer ...\n";
    $buf = $req->getInputBuffer();
    while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
        echo $s, PHP_EOL;
    }
    echo "No more data in the buffer\n";
}

function _http_about($req) {
    echo __METHOD__, PHP_EOL;
    echo "URI: ", $req->getUri(), PHP_EOL;
    echo "\n >> Sending reply ...";
    $req->sendReply(200, "OK");
    echo "OK\n";
}

function _http_default($req, $data) {
    echo __METHOD__, PHP_EOL;
    echo "URI: ", $req->getUri(), PHP_EOL;
    echo "\n >> Sending reply ...";
    $req->sendReply(200, "OK");
    echo "OK\n";
}

$port = 8010;
if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Invalid port");
}

$base = new EventBase();
$http = new EventHttp($base);
$http->setAllowedMethods(EventHttpRequest::CMD_GET | EventHttpRequest::CMD_POST);

$http->setCallback("/dump", "_http_dump", array(4, 8));
$http->setCallback("/about", "_http_about");
$http->setDefaultCallback("_http_default", "custom data value");

$http->bind("0.0.0.0", 8010);
$base->loop();
?>
```

以上例程的输出类似于：

    a=12
    HTTP/1.0 200 OK
    Content-Type: text/html; charset=ISO-8859-1
    Connection: close

### 参见

-   <span class="methodname">EventHttp::setDefaultCallback</span>

EventHttp::setDefaultCallback
=============================

Sets default callback to handle requests that are not caught by specific
callbacks

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::setDefaultCallback</span> ( <span
class="methodparam"> <span class="type">string</span> `$cb` </span> \[,
<span class="methodparam"> <span class="type">string</span> `$arg`
</span> \] )

Sets default callback to handle requests that are not caught by specific
callbacks

### 参数

`cb`  
The callback <span class="type">callable</span> . It should match the
following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span
class="type">EventHttpRequest</span> `$req` <span class="initializer"> =
NULL</span> </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$arg` <span class="initializer"> =
NULL</span> </span> \]\] )

`req`  
<span class="classname">EventHttpRequest</span> object.

`arg`  
Custom data.

`arg`  
User custom data passed to the callback.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span class="function">EventHttp::setDefaultCallback</span>
example**

``` php
<?php
$base = new EventBase();
$http = new EventHttp($base);

$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);

if (!$http->bind("127.0.0.1", 8088)) {
    exit("bind(1) failed\n");
};

$http->setDefaultCallback(function($req) {
    echo "URI: ", $req->getUri(), PHP_EOL;
    $req->sendReply(200, "OK");
});

$base->dispatch();
?>
```

### 参见

-   <span class="methodname">EventHttp::setCallback</span>

EventHttp::setMaxBodySize
=========================

Sets maximum request body size

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::setMaxBodySize</span> ( <span
class="methodparam"> <span class="type">int</span> `$value` </span> )

Sets maximum request body size.

### 参数

`value`  
The body size in bytes.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttp::setMaxHeadersSize</span>

EventHttp::setMaxHeadersSize
============================

Sets maximum HTTP header size

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::setMaxHeadersSize</span> ( <span
class="methodparam"> <span class="type">int</span> `$value` </span> )

Sets maximum HTTP header size.

### 参数

`value`  
The header size in bytes.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttp::setMaxHeadersSize</span>

EventHttp::setTimeout
=====================

Sets the timeout for an HTTP request

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttp::setTimeout</span> ( <span
class="methodparam"> <span class="type">int</span> `$value` </span> )

Sets the timeout for an HTTP request.

### 参数

`value`  
The timeout in seconds.

### 返回值

没有返回值。

简介
----

Represents an HTTP connection.

类摘要
------

**EventHttpConnection**

<span class="ooclass"> class **EventHttpConnection** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">EventDnsBase</span> `$dns_base`
</span> , <span class="methodparam"> <span class="type">string</span>
`$address` </span> , <span class="methodparam"> <span
class="type">int</span> `$port` </span> \[, <span class="methodparam">
<span class="type">EventSslContext</span> `$ctx` <span
class="initializer"> = **`NULL`**</span> </span> \] )

<span class="modifier">public</span> <span class="type">EventBase</span>
<span class="methodname">getBase</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getPeer</span> ( <span class="methodparam">
<span class="type">string</span> `&$address` </span> , <span
class="methodparam"> <span class="type">int</span> `&$port` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">makeRequest</span> ( <span class="methodparam">
<span class="type">EventHttpRequest</span> `$req` </span> , <span
class="methodparam"> <span class="type">int</span> `$type` </span> ,
<span class="methodparam"> <span class="type">string</span> `$uri`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCloseCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setLocalAddress</span> ( <span
class="methodparam"> <span class="type">string</span> `$address` </span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setLocalPort</span> ( <span
class="methodparam"> <span class="type">int</span> `$port` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMaxBodySize</span> ( <span
class="methodparam"> <span class="type">string</span> `$max_size`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMaxHeadersSize</span> ( <span
class="methodparam"> <span class="type">string</span> `$max_size`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setRetries</span> ( <span class="methodparam">
<span class="type">int</span> `$retries` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setTimeout</span> ( <span class="methodparam">
<span class="type">int</span> `$timeout` </span> )

}

EventHttpConnection::\_\_construct
==================================

Constructs EventHttpConnection object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventHttpConnection::\_\_construct</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">EventDnsBase</span>
`$dns_base` </span> , <span class="methodparam"> <span
class="type">string</span> `$address` </span> , <span
class="methodparam"> <span class="type">int</span> `$port` </span> \[,
<span class="methodparam"> <span class="type">EventSslContext</span>
`$ctx` <span class="initializer"> = **`NULL`**</span> </span> \] )

Constructs EventHttpConnection object.

### 参数

`base`  
Associated event base.

`dns_base`  
If `dns_base` is **`NULL`**, hostname resolution will block.

`address`  
The address to connect to.

`port`  
The port to connect to.

`ctx`  
<span class="classname">EventSslContext</span> class object. Enables
OpenSSL.

> **Note**:
>
> This parameter is available only if *Event* is compiled with OpenSSL
> support and only with *Libevent 2.1.0-alpha* and higher.

### 返回值

Returns <span class="classname">EventHttpConnection</span> object.

### 更新日志

| 版本             | 说明                           |
|------------------|--------------------------------|
| PECL event 1.9.0 | OpenSSL support (`ctx`) added. |

EventHttpConnection::getBase
============================

Returns event base associated with the connection

### 说明

<span class="modifier">public</span> <span class="type">EventBase</span>
<span class="methodname">EventHttpConnection::getBase</span> ( <span
class="methodparam">void</span> )

Returns event base associated with the connection.

### 参数

此函数没有参数。

### 返回值

On success returns <span class="classname">EventBase</span> object
associated with the connection. Otherwise **`FALSE`**.

EventHttpConnection::getPeer
============================

Gets the remote address and port associated with the connection

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::getPeer</span> ( <span
class="methodparam"> <span class="type">string</span> `&$address`
</span> , <span class="methodparam"> <span class="type">int</span>
`&$port` </span> )

Gets the remote address and port associated with the connection

### 参数

`address`  
Address of the peer.

`port`  
Port of the peer.

### 返回值

没有返回值。

EventHttpConnection::makeRequest
================================

Makes an HTTP request over the specified connection

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventHttpConnection::makeRequest</span> ( <span
class="methodparam"> <span class="type">EventHttpRequest</span> `$req`
</span> , <span class="methodparam"> <span class="type">int</span>
`$type` </span> , <span class="methodparam"> <span
class="type">string</span> `$uri` </span> )

Makes an HTTP request over the specified connection. `type` is one of
*EventHttpRequest::CMD\_\** constants.

### 参数

`req`  
The connection object over which to send the request.

`type`  
One of
<a href="/class/eventhttprequest.html#预定义常量" class="link"><em>EventHttpRequest::CMD_*</em> constants</a>
.

`uri`  
The URI associated with the request.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 范例

**示例 \#1 <span
class="function">EventHttpConnection::makeRequest</span> example**

``` php
<?php
function _request_handler($req, $base) {
    echo __FUNCTION__, PHP_EOL;

    if (is_null($req)) {
        echo "Timed out\n";
    } else {
        $response_code = $req->getResponseCode();

        if ($response_code == 0) {
            echo "Connection refused\n";
        } elseif ($response_code != 200) {
            echo "Unexpected response: $response_code\n";
        } else {
            echo "Success: $response_code\n";
            $buf = $req->getInputBuffer();
            echo "Body:\n";
            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
                echo $s, PHP_EOL;
            }
        }
    }

    $base->exit(NULL);
}

$address = "127.0.0.1";
$port = 80;

$base = new EventBase();
$conn = new EventHttpConnection($base, NULL, $address, $port);
$conn->setTimeout(5);
$req = new EventHttpRequest("_request_handler", $base);

$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);
$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);
$conn->makeRequest($req, EventHttpRequest::CMD_GET, "/index.cphp");

$base->loop();
?>
```

以上例程的输出类似于：

    _request_handler
    Success: 200
    Body:
    PHP, date:
    2013-03-13T20:27:52+05:00

### 参见

-   <span class="methodname">EventHttpRequest::addHeader</span>

EventHttpConnection::setCloseCallback
=====================================

Set callback for connection close

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setCloseCallback</span> (
<span class="methodparam"> <span class="type">callable</span>
`$callback` </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$data` </span> \] )

Sets callback for connection close.

### 参数

`callback`  
Callback which is called when connection is closed. Should match the
following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span
class="type">EventHttpConnection</span> `$conn` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$arg` <span
class="initializer"> = **`NULL`**</span> </span> \]\] )

### 返回值

没有返回值。

### 范例

**示例 \#1 <span
class="methodname">EventHttpConnection::setCloseCallback</span>
example**

``` php
<?php
/*
 * Setting up close-connection callback
 *
 * The script handles closed connections using HTTP API.
 *
 * Usage:
 * 1) Launch the server:
 * $ php examples/http_closecb.php 4242
 *
 * 2) Launch a client in another terminal. Telnet-like
 * session should look like the following:
 *
 * $ nc -t 127.0.0.1 4242
 * GET / HTTP/1.0
 * Connection: close
 *
 * The server will output something similar to the following:
 *
 * HTTP/1.0 200 OK
 * Content-Type: multipart/x-mixed-replace;boundary=boundarydonotcross
 * Connection: close
 *
 * <html>
 *
 * 3) Terminate the client connection abruptly,
 * i.e. kill the process, or just press Ctrl-C.
 *
 * 4) Check if the server called _close_callback.
 * The script should output "_close_callback" string to standard output.
 *
 * 5) Check if the server's process has no orphaned connections,
 * e.g. with `lsof` utility.
 */

function _close_callback($conn)
{
    echo __FUNCTION__, PHP_EOL;
}

function _http_default($req, $dummy)
{
    $conn = $req->getConnection();
    $conn->setCloseCallback('_close_callback', NULL);

    /*
    By enabling Event::READ we protect the server against unclosed conections.
    This is a peculiarity of Libevent. The library disables Event::READ events
     on this connection, and the server is not notified about terminated
    connections.

    So each time client terminates connection abruptly, we get an orphaned
    connection. For instance, the following is a part of `lsof -p $PID | grep TCP`
    command after client has terminated connection:

    57-php     15057 ruslan  6u  unix 0xffff8802fb59c780   0t0  125187 socket
    58:php     15057 ruslan  7u  IPv4             125189   0t0     TCP *:4242 (LISTEN)
    59:php     15057 ruslan  8u  IPv4             124342   0t0     TCP localhost:4242->localhost:37375 (CLOSE_WAIT)

    where $PID is our process ID.

    The following block of code fixes such kind of orphaned connections.
     */
    $bev = $req->getBufferEvent();
    $bev->enable(Event::READ);
    // We have to free it explicitly. See
```

<span class="methodname">EventHttpRequest::getConnection</span>

``` php
$bev->free(); // we have to free it explicitly

    $req->addHeader(
        'Content-Type',
        'multipart/x-mixed-replace;boundary=boundarydonotcross',
        EventHttpRequest::OUTPUT_HEADER
    );

    $buf = new EventBuffer();
    $buf->add('<html>');

    $req->sendReply(200, "OK");
    $req->sendReplyChunk($buf);
}

$port = 4242;
if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Invalid port");
}

$base = new EventBase();
$http = new EventHttp($base);

$http->setDefaultCallback("_http_default", NULL);
$http->bind("0.0.0.0", $port);
$base->loop();

?>
```

EventHttpConnection::setLocalAddress
====================================

Sets the IP address from which HTTP connections are made

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setLocalAddress</span> (
<span class="methodparam"> <span class="type">string</span> `$address`
</span> )

Sets the IP address from which http connections are made.

### 参数

`address`  
The IP address from which HTTP connections are made.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpConnection::setLocalPort</span>

EventHttpConnection::setLocalPort
=================================

Sets the local port from which connections are made

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setLocalPort</span> (
<span class="methodparam"> <span class="type">int</span> `$port` </span>
)

Sets the local port from which connections are made.

### 参数

`port`  
The port number.

### 返回值

### 参见

-   <span class="methodname">EventHttpConnection::setLocalAddress</span>

EventHttpConnection::setMaxBodySize
===================================

Sets maximum body size for the connection

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setMaxBodySize</span> (
<span class="methodparam"> <span class="type">string</span> `$max_size`
</span> )

Sets maximum body size for the connection.

### 参数

`max_size`  
The maximum body size in bytes.

### 返回值

没有返回值。

### 参见

-   <span
    class="methodname">EventHttpConnection::setMaxHeadersSize</span>

EventHttpConnection::setMaxHeadersSize
======================================

Sets maximum header size

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setMaxHeadersSize</span> (
<span class="methodparam"> <span class="type">string</span> `$max_size`
</span> )

Sets maximum header size for the connection.

### 参数

`max_size`  
The maximum header size in bytes.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpConnection::setMaxBodySize</span>

EventHttpConnection::setRetries
===============================

Sets the retry limit for the connection

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setRetries</span> ( <span
class="methodparam"> <span class="type">int</span> `$retries` </span> )

Sets the retry limit for the connection

### 参数

`retries`  
The retry limit. **`-1`** means infinity.

### 返回值

没有返回值。

EventHttpConnection::setTimeout
===============================

Sets the timeout for the connection

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpConnection::setTimeout</span> ( <span
class="methodparam"> <span class="type">int</span> `$timeout` </span> )

Sets the timeout for the connection

### 参数

`timeout`  
Timeout in seconds.

### 返回值

没有返回值。

简介
----

Represents an HTTP request.

类摘要
------

**EventHttpRequest**

<span class="ooclass"> class **EventHttpRequest** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_GET` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_POST` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_HEAD` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_PUT` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_DELETE` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_OPTIONS` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_TRACE` <span class="initializer"> = 64</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_CONNECT` <span class="initializer"> = 128</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::CMD_PATCH` <span class="initializer"> = 256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::INPUT_HEADER` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventHttpRequest::OUTPUT_HEADER` <span class="initializer"> = 2</span>
;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addHeader</span> ( <span class="methodparam">
<span class="type">string</span> `$key` </span> , <span
class="methodparam"> <span class="type">string</span> `$value` </span> ,
<span class="methodparam"> <span class="type">int</span> `$type` </span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">cancel</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clearHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">closeConnection</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">callable</span> `$callback` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">findHeader</span> ( <span class="methodparam">
<span class="type">string</span> `$key` </span> , <span
class="methodparam"> <span class="type">string</span> `$type` </span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">free</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">EventBufferEvent</span> <span
class="methodname">closeConnection</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getCommand</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">EventHttpConnection</span> <span
class="methodname">closeConnection</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getHost</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">getInputBuffer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getInputHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">getOutputBuffer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getOutputHeaders</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getResponseCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getUri</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">removeHeader</span> ( <span
class="methodparam"> <span class="type">string</span> `$key` </span> ,
<span class="methodparam"> <span class="type">string</span> `$type`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sendError</span> ( <span class="methodparam">
<span class="type">int</span> `$error` </span> \[, <span
class="methodparam"> <span class="type">string</span> `$reason` <span
class="initializer"> = **`NULL`**</span> </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sendReply</span> ( <span class="methodparam">
<span class="type">int</span> `$code` </span> , <span
class="methodparam"> <span class="type">string</span> `$reason` </span>
\[, <span class="methodparam"> <span class="type">EventBuffer</span>
`$buf` </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sendReplyChunk</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sendReplyEnd</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sendReplyStart</span> ( <span
class="methodparam"> <span class="type">int</span> `$code` </span> ,
<span class="methodparam"> <span class="type">string</span> `$reason`
</span> )

}

预定义常量
----------

**`EventHttpRequest::CMD_GET`**  
GET method(command)

**`EventHttpRequest::CMD_POST`**  
POST method(command)

**`EventHttpRequest::CMD_HEAD`**  
HEAD method(command)

**`EventHttpRequest::CMD_PUT`**  
PUT method(command)

**`EventHttpRequest::CMD_DELETE`**  
DELETE command(method)

**`EventHttpRequest::CMD_OPTIONS`**  
OPTIONS method(command)

**`EventHttpRequest::CMD_TRACE`**  
TRACE method(command)

**`EventHttpRequest::CMD_CONNECT`**  
CONNECT method(command)

**`EventHttpRequest::CMD_PATCH`**  
PATCH method(command)

**`EventHttpRequest::INPUT_HEADER`**  
Request input header type.

**`EventHttpRequest::OUTPUT_HEADER`**  
Request output header type.

EventHttpRequest::addHeader
===========================

Adds an HTTP header to the headers of the request

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventHttpRequest::addHeader</span> ( <span
class="methodparam"> <span class="type">string</span> `$key` </span> ,
<span class="methodparam"> <span class="type">string</span> `$value`
</span> , <span class="methodparam"> <span class="type">int</span>
`$type` </span> )

Adds an HTTP header to the headers of the request.

### 参数

`key`  
Header name.

`value`  
Header value.

`type`  
One of
<a href="/class/eventhttprequest.html#预定义常量" class="link"><em>EventHttpRequest::*_HEADER</em> constants</a>
.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventHttpRequest::removeHeader</span>

EventHttpRequest::cancel
========================

Cancels a pending HTTP request

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::cancel</span> ( <span
class="methodparam">void</span> )

Cancels a pending HTTP request.

Cancels an ongoing HTTP request. The callback associated with this
request is not executed and the request object is freed. If the request
is currently being processed, e.g. it is ongoing, the corresponding
<span class="classname">EventHttpConnection</span> object is going to
get reset.

A request cannot be canceled if its callback has executed already. A
request may be canceled reentrantly from its chunked callback.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventHttpRequest::clearHeaders
==============================

Removes all output headers from the header list of the request

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::clearHeaders</span> ( <span
class="methodparam">void</span> )

Removes all output headers from the header list of the request.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpRequest::addHeader</span>

EventHttpRequest::closeConnection
=================================

Closes associated HTTP connection

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::closeConnection</span> (
<span class="methodparam">void</span> )

Closes HTTP connection associated with the request.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventHttpRequest::\_\_construct
===============================

Constructs EventHttpRequest object

### 说明

<span class="modifier">public</span> <span
class="methodname">EventHttpRequest::\_\_construct</span> ( <span
class="methodparam"> <span class="type">callable</span> `$callback`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`$data` <span class="initializer"> = **`NULL`**</span> </span> \] )

Constructs EventHttpRequest object.

### 参数

`callback`  
Gets invoked on requesting path. Should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span
class="type">EventHttpRequest</span> `$req` <span class="initializer"> =
**`NULL`**</span> </span> \[, <span class="methodparam"> <span
class="type">mixed</span> `$arg` <span class="initializer"> =
**`NULL`**</span> </span> \]\] )

`data`  
User custom data passed to the callback.

### 返回值

Returns EventHttpRequest object.

### 范例

**示例 \#1 <span class="function">EventHttpRequest::\_\_construct</span>
example**

``` php
<?php

function _request_handler($req, $base) {
    echo __FUNCTION__, PHP_EOL;

    if (is_null($req)) {
        echo "Timed out\n";
    } else {
        $response_code = $req->getResponseCode();

        if ($response_code == 0) {
            echo "Connection refused\n";
        } elseif ($response_code != 200) {
            echo "Unexpected response: $response_code\n";
        } else {
            echo "Success: $response_code\n";
            $buf = $req->getInputBuffer();
            echo "Body:\n";
            while ($s = $buf->readLine(EventBuffer::EOL_ANY)) {
                echo $s, PHP_EOL;
            }
        }
    }

    $base->exit(NULL);
}


$address = "127.0.0.1";
$port = 80;

$base = new EventBase();
$conn = new EventHttpConnection($base, NULL, $address, $port);
$conn->setTimeout(5);
$req = new EventHttpRequest("_request_handler", $base);

$req->addHeader("Host", $address, EventHttpRequest::OUTPUT_HEADER);
$req->addHeader("Content-Length", "0", EventHttpRequest::OUTPUT_HEADER);
$conn->makeRequest($req, EventHttpRequest::CMD_GET, "/index.cphp");

$base->loop();
?>
```

### 参见

-   <span class="methodname">EventHttpRequest::cancel</span>
-   <span class="methodname">EventHttpRequest::addHeader</span>

EventHttpRequest::findHeader
============================

Finds the value belonging a header

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::findHeader</span> ( <span
class="methodparam"> <span class="type">string</span> `$key` </span> ,
<span class="methodparam"> <span class="type">string</span> `$type`
</span> )

Finds the value belonging a header.

### 参数

`key`  
The header name.

`type`  
One of
<a href="/class/eventhttprequest.html#预定义常量" class="link"><em>EventHttpRequest::*_HEADER</em> constants</a>
.

### 返回值

Returns **`NULL`** if header not found.

### 参见

-   <span class="methodname">EventHttpRequest::addHeader</span>

EventHttpRequest::free
======================

Frees the object and removes associated events

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::free</span> ( <span
class="methodparam">void</span> )

Frees the object and removes associated events.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventHttpRequest::getBufferEvent
================================

Returns EventBufferEvent object

### 说明

<span class="modifier">public</span> <span
class="type">EventBufferEvent</span> <span
class="methodname">EventHttpRequest::closeConnection</span> ( <span
class="methodparam">void</span> )

Returns <span class="classname">EventBufferEvent</span> object which
represents buffer event that the connection is using.

**Warning**

The reference counter of the returned object will be incremented by one
to protect internal structures against premature destruction when the
method is called from a user callback. So the <span
class="classname">EventBufferEvent</span> object should be freed
explicitly with <span class="methodname">EventBufferEvent::free</span>
method. Otherwise memory will leak.

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">EventBufferEvent</span> object.

### 参见

-   <span class="methodname">EventHttpRequest::getConnection</span>

EventHttpRequest::getCommand
============================

Returns the request command(method)

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::getCommand</span> ( <span
class="methodparam">void</span> )

Returns the request command, one of
<a href="/class/eventhttprequest.html#预定义常量" class="link"><em>EventHttpRequest::CMD_*</em></a>
constants.

### 参数

此函数没有参数。

### 返回值

Returns the request command, one of
<a href="/class/eventhttprequest.html#预定义常量" class="link"><em>EventHttpRequest::CMD_*</em></a>
constants.

EventHttpRequest::getConnection
===============================

Returns EventHttpConnection object

### 说明

<span class="modifier">public</span> <span
class="type">EventHttpConnection</span> <span
class="methodname">EventHttpRequest::closeConnection</span> ( <span
class="methodparam">void</span> )

Returns <span class="classname">EventHttpConnection</span> object which
represents HTTP connection associated with the request.

**Warning**

Libevent API allows HTTP request objects to be not bound to any HTTP
connection. Therefore we can't unambiguously associate <span
class="classname">EventHttpRequest</span> with <span
class="classname">EventHttpConnection</span> . Thus, we construct <span
class="classname">EventHttpConnection</span> object on-the-fly. Having
no information about the event base, DNS base and connection-close
callback, we just leave these fields unset.

<span class="methodname">EventHttpRequest::getConnection</span> method
is usually useful when we need to set up a callback on connection close.
See <span
class="methodname">EventHttpConnection::setCloseCallback</span> .

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">EventHttpConnection</span> object.

### 参见

-   <span
    class="methodname">EventHttpConnection::setCloseCallback</span>
-   <span class="methodname">EventHttpRequest::getBufferEvent</span>

EventHttpRequest::getHost
=========================

Returns the request host

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventHttpRequest::getHost</span> ( <span
class="methodparam">void</span> )

Returns the request host.

### 参数

此函数没有参数。

### 返回值

Returns the request host.

### 参见

-   <span class="methodname">EventHttpRequest::getUri</span>
-   <span class="methodname">EventHttpRequest::getCommand</span>

EventHttpRequest::getInputBuffer
================================

Returns the input buffer

### 说明

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">EventHttpRequest::getInputBuffer</span> ( <span
class="methodparam">void</span> )

Returns the input buffer.

### 参数

此函数没有参数。

### 返回值

Returns the input buffer.

### 参见

-   <span class="methodname">EventHttpRequest::getOutputBuffer</span>

EventHttpRequest::getInputHeaders
=================================

Returns associative array of the input headers

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">EventHttpRequest::getInputHeaders</span> (
<span class="methodparam">void</span> )

Returns associative array of the input headers.

### 参数

此函数没有参数。

### 返回值

Returns associative array of the input headers.

### 参见

-   <span class="methodname">EventHttpRequest::getOutputHeaders</span>

EventHttpRequest::getOutputBuffer
=================================

Returns the output buffer of the request

### 说明

<span class="modifier">public</span> <span
class="type">EventBuffer</span> <span
class="methodname">EventHttpRequest::getOutputBuffer</span> ( <span
class="methodparam">void</span> )

Returns the output buffer of the request.

### 参数

此函数没有参数。

### 返回值

Returns the output buffer of the request.

### 参见

-   <span class="methodname">EventHttpRequest::getInputBuffer</span>

EventHttpRequest::getOutputHeaders
==================================

Returns associative array of the output headers

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::getOutputHeaders</span> (
<span class="methodparam">void</span> )

Returns associative array of the output headers.

### 参数

此函数没有参数。

### 返回值

### 参见

-   <span class="methodname">EventHttpRequest::getInputHeaders</span>

EventHttpRequest::getResponseCode
=================================

Returns the response code

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">EventHttpRequest::getResponseCode</span> ( <span
class="methodparam">void</span> )

Returns the response code.

### 参数

此函数没有参数。

### 返回值

Returns the response code of the request.

### 参见

-   <span class="methodname">EventHttpRequest::getCommand</span>
-   <span class="methodname">EventHttpRequest::getHost</span>
-   <span class="methodname">EventHttpRequest::getUri</span>

EventHttpRequest::getUri
========================

Returns the request URI

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">EventHttpRequest::getUri</span> ( <span
class="methodparam">void</span> )

Returns the request URI

### 参数

此函数没有参数。

### 返回值

Returns the request URI

### 参见

-   <span class="methodname">EventHttpRequest::getCommand</span>
-   <span class="methodname">EventHttpRequest::getHost</span>
-   <span class="methodname">EventHttpRequest::getResponseCode</span>

EventHttpRequest::removeHeader
==============================

Removes an HTTP header from the headers of the request

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::removeHeader</span> ( <span
class="methodparam"> <span class="type">string</span> `$key` </span> ,
<span class="methodparam"> <span class="type">string</span> `$type`
</span> )

Removes an HTTP header from the headers of the request.

### 参数

`key`  
The header name.

`type`  
`type` is one of *EventHttpRequest::\*\_HEADER* constants.

### 返回值

Removes an HTTP header from the headers of the request.

### 参见

-   <span class="methodname">EventHttpRequest::addHeader</span>

EventHttpRequest::sendError
===========================

Send an HTML error message to the client

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::sendError</span> ( <span
class="methodparam"> <span class="type">int</span> `$error` </span> \[,
<span class="methodparam"> <span class="type">string</span> `$reason`
<span class="initializer"> = **`NULL`**</span> </span> \] )

Send an HTML error message to the client.

### 参数

`error`  
The HTTP error code.

`reason`  
A brief explanation ofthe error. If **`NULL`**, the standard meaning of
the error code will be used.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">EventHttpRequest::sendError</span>
example**

``` php
<?php
function _http_400($req) {
    $req->sendError(400);
}

$base = new EventBase();
$http = new EventHttp($base);

$http->setCallback("/err400", "_http_400");

$http->bind("0.0.0.0", 8010);
$base->loop();
?>
```

### 参见

-   <span class="methodname">EventHttpRequest::sendReply</span>

EventHttpRequest::sendReply
===========================

Send an HTML reply to the client

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::sendReply</span> ( <span
class="methodparam"> <span class="type">int</span> `$code` </span> ,
<span class="methodparam"> <span class="type">string</span> `$reason`
</span> \[, <span class="methodparam"> <span
class="type">EventBuffer</span> `$buf` </span> \] )

Send an HTML reply to the client. The body of the reply consists of data
in optional `buf` parameter.

### 参数

`code`  
The HTTP response code to send.

`reason`  
A brief message to send with the response code.

`buf`  
The body of the response.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpRequest::sendError</span>
-   <span class="methodname">EventHttpRequest::sendReplyChunk</span>

EventHttpRequest::sendReplyChunk
================================

Send another data chunk as part of an ongoing chunked reply

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::sendReplyChunk</span> ( <span
class="methodparam"> <span class="type">EventBuffer</span> `$buf`
</span> )

Send another data chunk as part of an ongoing chunked reply. After
calling this method `buf` will be empty.

### 参数

`buf`  
The data chunk to send as part of the reply.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpRequest::sendReplyStart</span>
-   <span class="methodname">EventHttpRequest::sendReplyEnd</span>

EventHttpRequest::sendReplyEnd
==============================

Complete a chunked reply, freeing the request as appropriate

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::sendReplyEnd</span> ( <span
class="methodparam">void</span> )

Complete a chunked reply, freeing the request as appropriate.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpRequest::sendReplyStart</span>
-   <span class="methodname">EventHttpRequest::sendReplyChunk</span>

EventHttpRequest::sendReplyStart
================================

Initiate a chunked reply

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventHttpRequest::sendReplyStart</span> ( <span
class="methodparam"> <span class="type">int</span> `$code` </span> ,
<span class="methodparam"> <span class="type">string</span> `$reason`
</span> )

Initiate a reply that uses *Transfer-Encoding* *chunked* .

This allows the caller to stream the reply back to the client and is
useful when either not all of the reply data is immediately available or
when sending very large replies.

The caller needs to supply data chunks with <span
class="methodname">EventHttpRequest::sendReplyChunk</span> and complete
the reply by calling <span
class="methodname">EventHttpRequest::sendReplyEnd</span> .

### 参数

`code`  
The HTTP response code to send.

`reason`  
A brief message to send with the response code.

### 返回值

没有返回值。

### 参见

-   <span class="methodname">EventHttpRequest::sendReplyChunk</span>
-   <span class="methodname">EventHttpRequest::sendReplyEnd</span>

简介
----

Represents a connection listener.

类摘要
------

**EventListener**

<span class="ooclass"> <span class="modifier">final</span> class
**EventListener** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventListener::OPT_LEAVE_SOCKETS_BLOCKING` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventListener::OPT_CLOSE_ON_FREE` <span class="initializer"> = 2</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventListener::OPT_CLOSE_ON_EXEC` <span class="initializer"> = 4</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventListener::OPT_REUSEABLE` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventListener::OPT_THREADSAFE` <span class="initializer"> = 16</span> ;

/\* 属性 \*/

<span class="modifier">public</span> <span
class="modifier">readonly</span> <span class="type">int</span> `$fd` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">EventBase</span> `$base` </span> , <span
class="methodparam"> <span class="type">callable</span> `$cb` </span> ,
<span class="methodparam"> <span class="type">mixed</span> `$data`
</span> , <span class="methodparam"> <span class="type">int</span>
`$flags` </span> , <span class="methodparam"> <span
class="type">int</span> `$backlog` </span> , <span class="methodparam">
<span class="type">mixed</span> `$target` </span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">enable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getBase</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">getSocketName</span> ( <span class="methodparam">
<span class="type">string</span> `&$address` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `&$port` </span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCallback</span> ( <span class="methodparam">
<span class="type">callable</span> `$cb` </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$arg` <span
class="initializer"> = **`NULL`**</span> </span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setErrorCallback</span> ( <span
class="methodparam"> <span class="type">string</span> `$cb` </span> )

}

属性
----

`fd`  
Numeric file descriptor of the underlying socket. (Added in
*event-1.6.0* .)

预定义常量
----------

**`EventListener::OPT_LEAVE_SOCKETS_BLOCKING`**  
By default Libevent turns underlying file descriptors, or sockets, to
non-blocking mode. This flag tells Libevent to leave them in blocking
mode.

**`EventListener::OPT_CLOSE_ON_FREE`**  
If this option is set, the connection listener closes its underlying
socket when the <span class="classname">EventListener</span> object is
freed.

**`EventListener::OPT_CLOSE_ON_EXEC`**  
If this option is set, the connection listener sets the close-on-exec
flag on the underlying listener socket. See platform documentation for
*fcntl* and **`FD_CLOEXEC`** for more information.

**`EventListener::OPT_REUSEABLE`**  
By default on some platforms, once a listener socket is closed, no other
socket can bind to the same port until a while has passed. Setting this
option makes Libevent mark the socket as reusable, so that once it is
closed, another socket can be opened to listen on the same port.

**`EventListener::OPT_THREADSAFE`**  
Allocate locks for the listener, so that it’s safe to use it from
multiple threads.

EventListener::\_\_construct
============================

Creates new connection listener associated with an event base

### 说明

<span class="modifier">public</span> <span
class="methodname">EventListener::\_\_construct</span> ( <span
class="methodparam"> <span class="type">EventBase</span> `$base` </span>
, <span class="methodparam"> <span class="type">callable</span> `$cb`
</span> , <span class="methodparam"> <span class="type">mixed</span>
`$data` </span> , <span class="methodparam"> <span
class="type">int</span> `$flags` </span> , <span class="methodparam">
<span class="type">int</span> `$backlog` </span> , <span
class="methodparam"> <span class="type">mixed</span> `$target` </span> )

Creates new connection listener associated with an event base.

### 参数

`base`  
Associated event base.

`cb`  
A <span class="type">callable</span> that will be invoked when new
connection received.

`data`  
Custom user data attached to `cb` .

`flags`  
Bit mask of *EventListener::OPT\_\** constants. See
<a href="/class/eventlistener.html#预定义常量" class="link">EventListener constants</a>
.

`backlog`  
Controls the maximum number of pending connections that the network
stack should allow to wait in a not-yet-accepted state at any time; see
documentation for your system’s *listen* function for more details. If
`backlog` is negative, Libevent tries to pick a good value for the
`backlog` ; if it is zero, Event assumes that *listen* is already called
on the socket( `target` )

`target`  
May be string, socket resource, or a stream associated with a socket. In
case if `target` is a string, the string will be parsed as network
address. It will be interpreted as a UNIX domain socket path, if
prefixed with *'unix:'* , e.g. *'unix:/tmp/my.sock'* .

### 返回值

Returns <span class="classname">EventListener</span> object representing
the event connection listener.

### 更新日志

| 版本             | 说明                                |
|------------------|-------------------------------------|
| PECL event 1.5.0 | UNIX domain sockets' support added. |

### 范例

**示例 \#1 <span class="function">EventListener::\_\_construct</span>
example**

``` php
<?php
/*
 * Simple echo server based on libevent's connection listener.
 *
 * Usage:
 * 1) In one terminal window run:
 *
 * $ php listener.php 9881
 *
 * 2) In another terminal window open up connection, e.g.:
 *
 * $ nc 127.0.0.1 9881
 *
 * 3) start typing. The server should repeat the input.
 */

class MyListenerConnection {
    private $bev, $base;

    public function __destruct() {
        $this->bev->free();
    }

    public function __construct($base, $fd) {
        $this->base = $base;

        $this->bev = new EventBufferEvent($base, $fd, EventBufferEvent::OPT_CLOSE_ON_FREE);

        $this->bev->setCallbacks(array($this, "echoReadCallback"), NULL,
            array($this, "echoEventCallback"), NULL);

        if (!$this->bev->enable(Event::READ)) {
            echo "Failed to enable READ\n";
            return;
        }
    }

    public function echoReadCallback($bev, $ctx) {
        // Copy all the data from the input buffer to the output buffer
        
        // Variant #1
        $bev->output->addBuffer($bev->input);

        /* Variant #2 */
        /*
        $input    = $bev->getInput();
        $output = $bev->getOutput();
        $output->addBuffer($input);
        */
    }

    public function echoEventCallback($bev, $events, $ctx) {
        if ($events & EventBufferEvent::ERROR) {
            echo "Error from bufferevent\n";
        }

        if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {
            //$bev->free();
            $this->__destruct();
        }
    }
}

class MyListener {
    public $base,
        $listener,
        $socket;
    private $conn = array();

    public function __destruct() {
        foreach ($this->conn as &$c) $c = NULL;
    }

    public function __construct($port) {
        $this->base = new EventBase();
        if (!$this->base) {
            echo "Couldn't open event base";
            exit(1);
        }

        // Variant #1
        /*
        $this->socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
        if (!socket_bind($this->socket, '0.0.0.0', $port)) {
            echo "Unable to bind socket\n";
            exit(1);
        }
        $this->listener = new EventListener($this->base,
            array($this, "acceptConnCallback"), $this->base,
            EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE,
            -1, $this->socket);
         */

        // Variant #2
         $this->listener = new EventListener($this->base,
             array($this, "acceptConnCallback"), $this->base,
             EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE, -1,
             "0.0.0.0:$port");

        if (!$this->listener) {
            echo "Couldn't create listener";
            exit(1);
        }

        $this->listener->setErrorCallback(array($this, "accept_error_cb"));
    }

    public function dispatch() {
        $this->base->dispatch();
    }

    // This callback is invoked when there is data to read on $bev
    public function acceptConnCallback($listener, $fd, $address, $ctx) {
        // We got a new connection! Set up a bufferevent for it. */
        $base = $this->base;
        $this->conn[] = new MyListenerConnection($base, $fd);
    }

    public function accept_error_cb($listener, $ctx) {
        $base = $this->base;

        fprintf(STDERR, "Got an error %d (%s) on the listener. "
            ."Shutting down.\n",
            EventUtil::getLastSocketErrno(),
            EventUtil::getLastSocketError());

        $base->exit(NULL);
    }
}

$port = 9808;

if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Invalid port");
}

$l = new MyListener($port);
$l->dispatch();
?>
```

EventListener::disable
======================

Disables an event connect listener object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventListener::disable</span> ( <span
class="methodparam">void</span> )

Disables an event connect listener object

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventListener::enable</span>

EventListener::enable
=====================

Enables an event connect listener object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">EventListener::enable</span> ( <span
class="methodparam">void</span> )

Enables an event connect listener object

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="methodname">EventListener::disable</span>

EventListener::getBase
======================

Returns event base associated with the event listener

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventListener::getBase</span> ( <span
class="methodparam">void</span> )

Returns event base associated with the event listener.

### 参数

此函数没有参数。

### 返回值

Returns event base associated with the event listener.

EventListener::getSocketName
============================

Retreives the current address to which the listener's socket is bound

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">EventListener::getSocketName</span> ( <span
class="methodparam"> <span class="type">string</span> `&$address`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`&$port` </span> \] )

Retreives the current address to which the listener's socket is bound.

### 参数

`address`  
Output parameter. IP-address depending on the socket address family.

`port`  
Output parameter. The port the socket is bound to.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventListener::setCallback
==========================

The setCallback purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventListener::setCallback</span> ( <span
class="methodparam"> <span class="type">callable</span> `$cb` </span>
\[, <span class="methodparam"> <span class="type">mixed</span> `$arg`
<span class="initializer"> = **`NULL`**</span> </span> \] )

Adjust event connect listener's callback and optionally the callback
argument.

### 参数

`cb`  
The new callback for new connections. Ignored if **`NULL`**.

Should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span class="type">EventListener</span>
`$listener` <span class="initializer"> = **`NULL`**</span> </span> \[,
<span class="methodparam"> <span class="type">mixed</span> `$fd` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">array</span> `$address` <span
class="initializer"> = **`NULL`**</span> </span> \[, <span
class="methodparam"> <span class="type">mixed</span> `$arg` <span
class="initializer"> = **`NULL`**</span> </span> \]\]\]\] )

`listener`  
The <span class="classname">EventListener</span> object.

`fd`  
The file descriptor or a resource associated with the listener.

`address`  
Array of two elements: IP address and the *server* port.

`arg`  
User custom data attached to the callback.

`arg`  
Custom user data attached to the callback. Ignored if **`NULL`**.

### 返回值

没有返回值。

EventListener::setErrorCallback
===============================

Set event listener's error callback

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">EventListener::setErrorCallback</span> ( <span
class="methodparam"> <span class="type">string</span> `$cb` </span> )

Set event listener's error callback

### 参数

`cb`  
The error callback. Should match the following prototype:

<span class="type">void</span> <span class="methodname">callback</span>
(\[ <span class="methodparam"> <span class="type">EventListener</span>
`$listener` <span class="initializer"> = **`NULL`**</span> </span> \[,
<span class="methodparam"> <span class="type">mixed</span> `$data` <span
class="initializer"> = **`NULL`**</span> </span> \]\] )

`listener`  
The <span class="classname">EventListener</span> object.

`data`  
User custom data attached to the callback.

### 返回值

### 参见

-   <span class="methodname">EventListener::setCallback</span>

简介
----

Represents *SSL\_CTX* structure. Provides methods and properties to
configure the SSL context.

类摘要
------

**EventSslContext**

<span class="ooclass"> <span class="modifier">final</span> class
**EventSslContext** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::SSLv2_CLIENT_METHOD` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::SSLv3_CLIENT_METHOD` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::SSLv23_CLIENT_METHOD` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::TLS_CLIENT_METHOD` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::SSLv2_SERVER_METHOD` <span class="initializer"> =
5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::SSLv3_SERVER_METHOD` <span class="initializer"> =
6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::SSLv23_SERVER_METHOD` <span class="initializer"> =
7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::TLS_SERVER_METHOD` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_LOCAL_CERT` <span class="initializer"> = 1</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_LOCAL_PK` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_PASSPHRASE` <span class="initializer"> = 3</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_CA_FILE` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_CA_PATH` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_ALLOW_SELF_SIGNED` <span class="initializer"> =
6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_VERIFY_PEER` <span class="initializer"> = 7</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_VERIFY_DEPTH` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventSslContext::OPT_CIPHERS` <span class="initializer"> = 9</span> ;

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$local_cert` ;

<span class="modifier">public</span> <span class="type">string</span>
`$local_pk` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span class="methodparam">
<span class="type">string</span> `$method` </span> , <span
class="methodparam"> <span class="type">string</span> `$options` </span>
)

}

属性
----

`local_cert`  
Path to local certificate file on filesystem. It must be a PEM-encoded
file which contains certificate. It can optionally contain the
certificate chain of issuers.

`local_pk`  
Path to local private key file

预定义常量
----------

**`EventSslContext::SSLv2_CLIENT_METHOD`**  
SSLv2 client method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::SSLv3_CLIENT_METHOD`**  
SSLv3 client method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::SSLv23_CLIENT_METHOD`**  
SSLv23 client method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::TLS_CLIENT_METHOD`**  
TLS client method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::SSLv2_SERVER_METHOD`**  
SSLv2 server method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::SSLv3_SERVER_METHOD`**  
SSLv3 server method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::SSLv23_SERVER_METHOD`**  
SSLv23 server method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::TLS_SERVER_METHOD`**  
TLS server method. See *SSL\_CTX\_new(3)* man page.

**`EventSslContext::OPT_LOCAL_CERT`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . The option
points to path of local certificate.

**`EventSslContext::OPT_LOCAL_PK`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . The option
points to path of the private key.

**`EventSslContext::OPT_PASSPHRASE`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
passphrase of the certificate.

**`EventSslContext::OPT_CA_FILE`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
path of the certificate authority file.

**`EventSslContext::OPT_CA_PATH`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
path where the certificate authority file should be searched for.

**`EventSslContext::OPT_ALLOW_SELF_SIGNED`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
option that allows self-signed certificates.

**`EventSslContext::OPT_VERIFY_PEER`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
option that tells Event to verify peer.

**`EventSslContext::OPT_VERIFY_DEPTH`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
maximum depth for the certificate chain verification that shall be
allowed for the SSL context.

**`EventSslContext::OPT_CIPHERS`**  
Key for an item of the options' array used in <span
class="methodname">EventSslContext::\_\_construct</span> . Represents
the cipher list for the SSL context.

EventSslContext::\_\_construct
==============================

Constructs an OpenSSL context for use with Event classes

### 说明

<span class="modifier">public</span> <span
class="methodname">EventSslContext::\_\_construct</span> ( <span
class="methodparam"> <span class="type">string</span> `$method` </span>
, <span class="methodparam"> <span class="type">string</span> `$options`
</span> )

Creates SSL context holding pointer to *SSL\_CTX* (see the system
manual).

### 参数

`method`  
One of
<a href="/class/eventsslcontext.html#预定义常量" class="link"><em>EventSslContext::*_METHOD</em> constants</a>
.

`options`  
Associative array of SSL context options One of
<a href="/class/eventsslcontext.html#预定义常量" class="link"><em>EventSslContext::OPT_*</em> constants</a>
.

### 返回值

Returns <span class="classname">EventSslContext</span> object.

### 范例

**示例 \#1 <span class="function">EventSslContext::\_\_construct</span>
example**

``` php
<?php
$ctx = new EventSslContext(EventSslContext::SSLv3_SERVER_METHOD, array(
     EventSslContext::OPT_LOCAL_CERT        => $local_cert,
     EventSslContext::OPT_LOCAL_PK          => $local_pk,
     EventSslContext::OPT_PASSPHRASE        => "echo server",
     EventSslContext::OPT_VERIFY_PEER       => true,
     EventSslContext::OPT_ALLOW_SELF_SIGNED => false,
));
?>
```

简介
----

<span class="classname">EventUtil</span> is a singleton with
supplimentary methods and constants.

类摘要
------

**EventUtil**

<span class="ooclass"> <span class="modifier">final</span> class
**EventUtil** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::AF_INET` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::AF_INET6` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::AF_UNSPEC` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::LIBEVENT_VERSION_NUMBER` <span class="initializer"> =
33559808</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_DEBUG` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_REUSEADDR` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_KEEPALIVE` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_DONTROUTE` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_LINGER` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_BROADCAST` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_OOBINLINE` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_SNDBUF` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_RCVBUF` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_SNDLOWAT` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_RCVLOWAT` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_SNDTIMEO` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_RCVTIMEO` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_TYPE` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SO_ERROR` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SOL_SOCKET` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SOL_TCP` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::SOL_UDP` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::IPPROTO_IP` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`EventUtil::IPPROTO_IPV6` <span class="initializer"> = 41</span> ;

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getLastSocketErrno</span> (\[ <span
class="methodparam"> <span class="type">mixed</span> `$socket` <span
class="initializer"> = **`NULL`**</span> </span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getLastSocketError</span> (\[ <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span>
\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">getSocketFd</span> ( <span class="methodparam"> <span
class="type">mixed</span> `$socket` </span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">getSocketName</span> ( <span class="methodparam">
<span class="type">mixed</span> `$socket` </span> , <span
class="methodparam"> <span class="type">string</span> `&$address`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`&$port` </span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">setSocketOption</span> ( <span class="methodparam">
<span class="type">mixed</span> `$socket` </span> , <span
class="methodparam"> <span class="type">int</span> `$level` </span> ,
<span class="methodparam"> <span class="type">int</span> `$optname`
</span> , <span class="methodparam"> <span class="type">mixed</span>
`$optval` </span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">sslRandPoll</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`EventUtil::AF_INET`**  
IPv4 address family

**`EventUtil::AF_INET6`**  
IPv6 address family

**`EventUtil::AF_UNSPEC`**  
Unspecified IP address family

**`EventUtil::SO_DEBUG`**  
Socket option. Enable socket debugging. Only allowed for processes with
the *CAP\_NET\_ADMIN* capability or an effective user ID of **`0`** .
(Added in event-1.6.0.)

**`EventUtil::SO_REUSEADDR`**  
Socket option. Indicates that the rules used in validating addresses
supplied in a *bind(2)* call should allow reuse of local addresses. See
the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_KEEPALIVE`**  
Socket option. Enable sending of keep-alive messages on
connection-oriented sockets. Expects an integer boolean flag. See the
*socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_DONTROUTE`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_LINGER`**  
Socket option. When enabled, a *close(2)* or *shutdown(2)* will not
return until all queued messages for the socket have been successfully
sent or the linger timeout has been reached. Otherwise, the call returns
immediately and the closing is done in the background. See the
*socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_BROADCAST`**  
Socket option. Reports whether transmission of broadcast messages is
supported. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_OOBINLINE`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_SNDBUF`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_RCVBUF`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_SNDLOWAT`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_RCVLOWAT`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_SNDTIMEO`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_RCVTIMEO`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_TYPE`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SO_ERROR`**  
Socket option. See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::SOL_SOCKET`**  
Socket option level. See the *socket(7)* manual page. (Added in
event-1.6.0.)

**`EventUtil::SOL_TCP`**  
Socket option level. See the *socket(7)* manual page. (Added in
event-1.6.0.)

**`EventUtil::SOL_UDP`**  
Socket option level. See the *socket(7)* manual page. (Added in
event-1.6.0.)

**`EventUtil::IPPROTO_IP`**  
See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::IPPROTO_IPV6`**  
See the *socket(7)* manual page. (Added in event-1.6.0.)

**`EventUtil::LIBEVENT_VERSION_NUMBER`**  
Libevent' version number at the time when Event extension had been
compiled with the library.

EventUtil::\_\_construct
========================

The abstract constructor

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span
class="methodname">EventUtil::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="classname">EventUtil</span> is a singleton. Therefore the
constructor is abstract, and it is impossible to create objects based on
this class.

### 参数

此函数没有参数。

### 返回值

没有返回值。

EventUtil::getLastSocketErrno
=============================

Returns the most recent socket error number

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">EventUtil::getLastSocketErrno</span> (\[ <span
class="methodparam"> <span class="type">mixed</span> `$socket` <span
class="initializer"> = **`NULL`**</span> </span> \] )

Returns the most recent socket error number( *errno* ).

### 参数

`socket`  
Socket resource, stream or a file descriptor of a socket.

### 返回值

Returns the most recent socket error number( *errno* ).

### 参见

-   <span class="methodname">EventUtil::getLastSocketError</span>

EventUtil::getLastSocketError
=============================

Returns the most recent socket error

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">EventUtil::getLastSocketError</span> (\[ <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span>
\] )

Returns the most recent socket error.

### 参数

`socket`  
Socket resource, stream or a file descriptor of a socket.

### 返回值

Returns the most recent socket error.

### 参见

-   <span class="methodname">EventUtil::getLastSocketErrno</span>

EventUtil::getSocketFd
======================

Returns numeric file descriptor of a socket, or stream

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">EventUtil::getSocketFd</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span> )

Returns numeric file descriptor of a socket or stream specified by
`socket` argument just like the *Event* extension does it internally for
all methods accepting socket resource or stream.

### 参数

`socket`  
Socket resource or stream.

### 返回值

Returns numeric file descriptor of a socket, or stream. <span
class="methodname">EventUtil::getSocketFd</span> returns **`FALSE`** in
case if it is whether failed to recognize the type of the underlying
file, or detected that the file descriptor associated with `socket` is
not valid.

EventUtil::getSocketName
========================

Retreives the current address to which the socket is bound

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">EventUtil::getSocketName</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span> ,
<span class="methodparam"> <span class="type">string</span> `&$address`
</span> \[, <span class="methodparam"> <span class="type">mixed</span>
`&$port` </span> \] )

Retreives the current address to which the `socket` is bound.

### 参数

`socket`  
Socket resource, stream or a file descriptor of a socket.

`address`  
Output parameter. IP-address, or the UNIX domain socket path depending
on the socket address family.

`port`  
Output parameter. The port the socket is bound to. Has no meaning for
UNIX domain sockets.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

EventUtil::setSocketOption
==========================

Sets socket options

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">EventUtil::setSocketOption</span> ( <span
class="methodparam"> <span class="type">mixed</span> `$socket` </span> ,
<span class="methodparam"> <span class="type">int</span> `$level`
</span> , <span class="methodparam"> <span class="type">int</span>
`$optname` </span> , <span class="methodparam"> <span
class="type">mixed</span> `$optval` </span> )

Sets socket options.

### 参数

`socket`  
Socket resource, stream, or numeric file descriptor associated with the
socket.

`level`  
One of *EventUtil::SOL\_\** constants. Specifies the protocol level at
which the option resides. For example, to retrieve options at the socket
level, a `level` parameter of **`EventUtil::SOL_SOCKET`** would be used.
Other levels, such as TCP, can be used by specifying the protocol number
of that level. Protocol numbers can be found by using the <span
class="function">getprotobyname</span> function. See
<a href="/class/eventutil.html#预定义常量" class="link">EventUtil constants</a>
.

`optname`  
Option name(type). Has the same meaning as corresponding parameter of
<span class="function">socket\_get\_option</span> function. See
<a href="/class/eventutil.html#预定义常量" class="link">EventUtil constants</a>
.

`optval`  
Accepts the same values as `optval` parameter of the <span
class="function">socket\_get\_option</span> function.

### 返回值

Returns **`TRUE`** on success. Otherwise **`FALSE`**.

### 参见

-   <span class="function">socket\_get\_option</span>
-   <span class="function">socket\_set\_option</span>

EventUtil::sslRandPoll
======================

Generates entropy by means of OpenSSL's RAND\_poll()

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">EventUtil::sslRandPoll</span> ( <span
class="methodparam">void</span> )

Generates entropy by means of OpenSSL's *RAND\_poll()* (see the system
manual).

### 参数

此函数没有参数。

### 返回值

没有返回值。
