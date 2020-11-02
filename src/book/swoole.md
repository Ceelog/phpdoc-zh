Swoole
======

**目录**

-   [简介](/intro/swoole.html)
-   [安装／配置](/swoole/setup.html)
    -   [需求](/swoole/setup.html#需求)
    -   [安装](/swoole/setup.html#安装)
    -   [运行时配置](/swoole/setup.html#运行时配置)
    -   [资源类型](/swoole/setup.html#资源类型)
-   [预定义常量](/swoole/constants.html)
-   [Swoole 函数](/ref/swoole-funcs.html)
    -   [swoole\_async\_dns\_lookup](/ref/swoole-funcs.html#swoole_async_dns_lookup)
        — Async and non-blocking hostname to IP lookup
    -   [swoole\_async\_read](/ref/swoole-funcs.html#swoole_async_read)
        — Read file stream asynchronously
    -   [swoole\_async\_readfile](/ref/swoole-funcs.html#swoole_async_readfile)
        — Read a file asynchronously
    -   [swoole\_async\_set](/ref/swoole-funcs.html#swoole_async_set) —
        Update the async I/O options
    -   [swoole\_async\_write](/ref/swoole-funcs.html#swoole_async_write)
        — Write data to a file stream asynchronously
    -   [swoole\_async\_writefile](/ref/swoole-funcs.html#swoole_async_writefile)
        — Write data to a file asynchronously
    -   [swoole\_client\_select](/ref/swoole-funcs.html#swoole_client_select)
        — Get the file description which are ready to read/write or
        error
    -   [swoole\_cpu\_num](/ref/swoole-funcs.html#swoole_cpu_num) — Get
        the number of CPU
    -   [swoole\_errno](/ref/swoole-funcs.html#swoole_errno) — Get the
        error code of the latest system call
    -   [swoole\_event\_add](/ref/swoole-funcs.html#swoole_event_add) —
        Add new callback functions of a socket into the EventLoop
    -   [swoole\_event\_defer](/ref/swoole-funcs.html#swoole_event_defer)
        — Add callback function to the next event loop
    -   [swoole\_event\_del](/ref/swoole-funcs.html#swoole_event_del) —
        Remove all event callback functions of a socket
    -   [swoole\_event\_exit](/ref/swoole-funcs.html#swoole_event_exit)
        — Exit the eventloop, only available at the client side
    -   [swoole\_event\_set](/ref/swoole-funcs.html#swoole_event_set) —
        Update the event callback functions of a socket
    -   [swoole\_event\_wait](/ref/swoole-funcs.html#swoole_event_wait)
        — Start the event loop
    -   [swoole\_event\_write](/ref/swoole-funcs.html#swoole_event_write)
        — Write data to a socket
    -   [swoole\_get\_local\_ip](/ref/swoole-funcs.html#swoole_get_local_ip)
        — Get the IPv4 IP addresses of each NIC on the machine
    -   [swoole\_last\_error](/ref/swoole-funcs.html#swoole_last_error)
        — Get the lastest error message
    -   [swoole\_load\_module](/ref/swoole-funcs.html#swoole_load_module)
        — Load a swoole extension
    -   [swoole\_select](/ref/swoole-funcs.html#swoole_select) — Select
        the file descriptions which are ready to read/write or error in
        the eventloop
    -   [swoole\_set\_process\_name](/ref/swoole-funcs.html#swoole_set_process_name)
        — Set the process name
    -   [swoole\_strerror](/ref/swoole-funcs.html#swoole_strerror) —
        Convert the Errno into error messages
    -   [swoole\_timer\_after](/ref/swoole-funcs.html#swoole_timer_after)
        — Trigger a one time callback function in the future
    -   [swoole\_timer\_exists](/ref/swoole-funcs.html#swoole_timer_exists)
        — Check if a timer callback function is existed
    -   [swoole\_timer\_tick](/ref/swoole-funcs.html#swoole_timer_tick)
        — Trigger a timer tick callback function by time interval
    -   [swoole\_version](/ref/swoole-funcs.html#swoole_version) — Get
        the version of Swoole
-   [Swoole\\Async](/class/swoole-async.html) — The Swoole\\Async class
    -   [Swoole\\Async::dnsLookup](/class/swoole-async.html#Swoole\Async::dnsLookup)
        — Async and non-blocking hostname to IP lookup.
    -   [Swoole\\Async::read](/class/swoole-async.html#Swoole\Async::read)
        — Read file stream asynchronously.
    -   [Swoole\\Async::readFile](/class/swoole-async.html#Swoole\Async::readFile)
        — Read a file asynchronously.
    -   [Swoole\\Async::set](/class/swoole-async.html#Swoole\Async::set)
        — Update the async I/O options.
    -   [Swoole\\Async::write](/class/swoole-async.html#Swoole\Async::write)
        — Write data to a file stream asynchronously.
    -   [Swoole\\Async::writeFile](/class/swoole-async.html#Swoole\Async::writeFile)
        — Description
-   [Swoole\\Atomic](/class/swoole-atomic.html) — The Swoole\\Atomic
    class
    -   [Swoole\\Atomic::add](/class/swoole-atomic.html#Swoole\Atomic::add)
        — Add a number to the value to the atomic object.
    -   [Swoole\\Atomic::cmpset](/class/swoole-atomic.html#Swoole\Atomic::cmpset)
        — Compare and set the value of the atomic object.
    -   [Swoole\\Atomic::\_\_construct](/class/swoole-atomic.html#Swoole\Atomic::__construct)
        — Construct a swoole atomic object.
    -   [Swoole\\Atomic::get](/class/swoole-atomic.html#Swoole\Atomic::get)
        — Get the current value of the atomic object.
    -   [Swoole\\Atomic::set](/class/swoole-atomic.html#Swoole\Atomic::set)
        — Set a new value to the atomic object.
    -   [Swoole\\Atomic::sub](/class/swoole-atomic.html#Swoole\Atomic::sub)
        — Subtract a number to the value of the atomic object.
-   [Swoole\\Buffer](/class/swoole-buffer.html) — The Swoole\\Buffer
    class
    -   [Swoole\\Buffer::append](/class/swoole-buffer.html#Swoole\Buffer::append)
        — Append the string or binary data at the end of the memory
        buffer and return the new size of memory allocated.
    -   [Swoole\\Buffer::clear](/class/swoole-buffer.html#Swoole\Buffer::clear)
        — Reset the memory buffer.
    -   [Swoole\\Buffer::\_\_construct](/class/swoole-buffer.html#Swoole\Buffer::__construct)
        — Fixed size memory blocks allocation.
    -   [Swoole\\Buffer::\_\_destruct](/class/swoole-buffer.html#Swoole\Buffer::__destruct)
        — Destruct the Swoole memory buffer.
    -   [Swoole\\Buffer::expand](/class/swoole-buffer.html#Swoole\Buffer::expand)
        — Expand the size of memory buffer.
    -   [Swoole\\Buffer::read](/class/swoole-buffer.html#Swoole\Buffer::read)
        — Read data from the memory buffer based on offset and length.
    -   [Swoole\\Buffer::recycle](/class/swoole-buffer.html#Swoole\Buffer::recycle)
        — Release the memory to OS which is not used by the memory
        buffer.
    -   [Swoole\\Buffer::substr](/class/swoole-buffer.html#Swoole\Buffer::substr)
        — Read data from the memory buffer based on offset and length.
        Or remove data from the memory buffer.
    -   [Swoole\\Buffer::\_\_toString](/class/swoole-buffer.html#Swoole\Buffer::__toString)
        — Get the string value of the memory buffer.
    -   [Swoole\\Buffer::write](/class/swoole-buffer.html#Swoole\Buffer::write)
        — Write data to the memory buffer. The memory allocated for the
        buffer will not be changed.
-   [Swoole\\Channel](/class/swoole-channel.html) — The Swoole\\Channel
    class
    -   [Swoole\\Channel::\_\_construct](/class/swoole-channel.html#Swoole\Channel::__construct)
        — Construct a Swoole Channel
    -   [Swoole\\Channel::\_\_destruct](/class/swoole-channel.html#Swoole\Channel::__destruct)
        — Destruct a Swoole channel.
    -   [Swoole\\Channel::pop](/class/swoole-channel.html#Swoole\Channel::pop)
        — Read and pop data from swoole channel.
    -   [Swoole\\Channel::push](/class/swoole-channel.html#Swoole\Channel::push)
        — Write and push data into Swoole channel.
    -   [Swoole\\Channel::stats](/class/swoole-channel.html#Swoole\Channel::stats)
        — Get stats of swoole channel.
-   [Swoole\\Client](/class/swoole-client.html) — The Swoole\\Client
    class
    -   [Swoole\\Client::close](/class/swoole-client.html#Swoole\Client::close)
        — Close the connection established.
    -   [Swoole\\Client::connect](/class/swoole-client.html#Swoole\Client::connect)
        — Connect to the remote TCP or UDP port.
    -   [Swoole\\Client::\_\_construct](/class/swoole-client.html#Swoole\Client::__construct)
        — Create Swoole sync or async TCP/UDP client, with or without
        SSL.
    -   [Swoole\\Client::\_\_destruct](/class/swoole-client.html#Swoole\Client::__destruct)
        — Destruct the Swoole client.
    -   [Swoole\\Client::getpeername](/class/swoole-client.html#Swoole\Client::getpeername)
        — Get the remote socket name of the connection.
    -   [Swoole\\Client::getsockname](/class/swoole-client.html#Swoole\Client::getsockname)
        — Get the local socket name of the connection.
    -   [Swoole\\Client::isConnected](/class/swoole-client.html#Swoole\Client::isConnected)
        — Check if the connection is established.
    -   [Swoole\\Client::on](/class/swoole-client.html#Swoole\Client::on)
        — Add callback functions triggered by events.
    -   [Swoole\\Client::pause](/class/swoole-client.html#Swoole\Client::pause)
        — Pause receiving data.
    -   [Swoole\\Client::pipe](/class/swoole-client.html#Swoole\Client::pipe)
        — Redirect the data to another file descriptor.
    -   [Swoole\\Client::recv](/class/swoole-client.html#Swoole\Client::recv)
        — Receive data from the remote socket.
    -   [Swoole\\Client::resume](/class/swoole-client.html#Swoole\Client::resume)
        — Resume receiving data.
    -   [Swoole\\Client::send](/class/swoole-client.html#Swoole\Client::send)
        — Send data to the remote TCP socket.
    -   [Swoole\\Client::sendfile](/class/swoole-client.html#Swoole\Client::sendfile)
        — Send file to the remote TCP socket.
    -   [Swoole\\Client::sendto](/class/swoole-client.html#Swoole\Client::sendto)
        — Send data to the remote UDP address.
    -   [Swoole\\Client::set](/class/swoole-client.html#Swoole\Client::set)
        — Set the Swoole client parameters before the connection is
        established.
    -   [Swoole\\Client::sleep](/class/swoole-client.html#Swoole\Client::sleep)
        — Remove the TCP client from system event loop.
    -   [Swoole\\Client::wakeup](/class/swoole-client.html#Swoole\Client::wakeup)
        — Add the TCP client back into the system event loop.
-   [Swoole\\Connection\\Iterator](/class/swoole-connection-iterator.html)
    — The Swoole\\Connection\\Iterator class
    -   [Swoole\\Connection\\Iterator::count](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::count)
        — Count connections.
    -   [Swoole\\Connection\\Iterator::current](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::current)
        — Return current connection entry.
    -   [Swoole\\Connection\\Iterator::key](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::key)
        — Return key of the current connection.
    -   [Swoole\\Connection\\Iterator::next](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::next)
        — Move to the next connection.
    -   [Swoole\\Connection\\Iterator::offsetExists](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::offsetExists)
        — Check if offet exists.
    -   [Swoole\\Connection\\Iterator::offsetGet](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::offsetGet)
        — Offset to retrieve.
    -   [Swoole\\Connection\\Iterator::offsetSet](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::offsetSet)
        — Assign a Connection to the specified offset.
    -   [Swoole\\Connection\\Iterator::offsetUnset](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::offsetUnset)
        — Unset an offset.
    -   [Swoole\\Connection\\Iterator::rewind](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::rewind)
        — Rewinds iterator
    -   [Swoole\\Connection\\Iterator::valid](/class/swoole-connection-iterator.html#Swoole\Connection\Iterator::valid)
        — Check if current position is valid.
-   [Swoole\\Coroutine](/class/swoole-coroutine.html) — The
    Swoole\\Coroutine class
    -   [Swoole\\Coroutine::call\_user\_func\_array](/class/swoole-coroutine.html#Swoole\Coroutine::call_user_func_array)
        — Call a callback with an array of parameters
    -   [Swoole\\Coroutine::call\_user\_func](/class/swoole-coroutine.html#Swoole\Coroutine::call_user_func)
        — Call a callback given by the first parameter
    -   [Swoole\\Coroutine::cli\_wait](/class/swoole-coroutine.html#Swoole\Coroutine::cli_wait)
        — Description
    -   [Swoole\\Coroutine::create](/class/swoole-coroutine.html#Swoole\Coroutine::create)
        — Description
    -   [Swoole\\Coroutine::getuid](/class/swoole-coroutine.html#Swoole\Coroutine::getuid)
        — Description
    -   [Swoole\\Coroutine::resume](/class/swoole-coroutine.html#Swoole\Coroutine::resume)
        — Description
    -   [Swoole\\Coroutine::suspend](/class/swoole-coroutine.html#Swoole\Coroutine::suspend)
        — Description
-   [Swoole\\Event](/class/swoole-event.html) — The Swoole\\Event class
    -   [Swoole\\Event::add](/class/swoole-event.html#Swoole\Event::add)
        — Add new callback functions of a socket into the EventLoop.
    -   [Swoole\\Event::defer](/class/swoole-event.html#Swoole\Event::defer)
        — Add a callback function to the next event loop.
    -   [Swoole\\Event::del](/class/swoole-event.html#Swoole\Event::del)
        — Remove all event callback functions of a socket.
    -   [Swoole\\Event::exit](/class/swoole-event.html#Swoole\Event::exit)
        — Exit the eventloop, only available at client side.
    -   [Swoole\\Event::set](/class/swoole-event.html#Swoole\Event::set)
        — Update the event callback functions of a socket.
    -   [Swoole\\Event::wait](/class/swoole-event.html#Swoole\Event::wait)
        — Description
    -   [Swoole\\Event::write](/class/swoole-event.html#Swoole\Event::write)
        — Write data to the socket.
-   [Swoole\\Exception](/class/swoole-exception.html) — The
    Swoole\\Exception class
-   [Swoole\\Http\\Client](/class/swoole-http-client.html) — The
    Swoole\\Http\\Client class
    -   [Swoole\\Http\\Client::addFile](/class/swoole-http-client.html#Swoole\Http\Client::addFile)
        — Add a file to the post form.
    -   [Swoole\\Http\\Client::close](/class/swoole-http-client.html#Swoole\Http\Client::close)
        — Close the http connection.
    -   [Swoole\\Http\\Client::\_\_construct](/class/swoole-http-client.html#Swoole\Http\Client::__construct)
        — Construct the async HTTP client.
    -   [Swoole\\Http\\Client::\_\_destruct](/class/swoole-http-client.html#Swoole\Http\Client::__destruct)
        — Destruct the HTTP client.
    -   [Swoole\\Http\\Client::download](/class/swoole-http-client.html#Swoole\Http\Client::download)
        — Download a file from the remote server.
    -   [Swoole\\Http\\Client::execute](/class/swoole-http-client.html#Swoole\Http\Client::execute)
        — Send the HTTP request after setting the parameters.
    -   [Swoole\\Http\\Client::get](/class/swoole-http-client.html#Swoole\Http\Client::get)
        — Send GET http request to the remote server.
    -   [Swoole\\Http\\Client::isConnected](/class/swoole-http-client.html#Swoole\Http\Client::isConnected)
        — Check if the HTTP connection is connected.
    -   [Swoole\\Http\\Client::on](/class/swoole-http-client.html#Swoole\Http\Client::on)
        — Register callback function by event name.
    -   [Swoole\\Http\\Client::post](/class/swoole-http-client.html#Swoole\Http\Client::post)
        — Send POST http request to the remote server.
    -   [Swoole\\Http\\Client::push](/class/swoole-http-client.html#Swoole\Http\Client::push)
        — Push data to websocket client.
    -   [Swoole\\Http\\Client::set](/class/swoole-http-client.html#Swoole\Http\Client::set)
        — Update the HTTP client paramters.
    -   [Swoole\\Http\\Client::setCookies](/class/swoole-http-client.html#Swoole\Http\Client::setCookies)
        — Set the http request cookies.
    -   [Swoole\\Http\\Client::setData](/class/swoole-http-client.html#Swoole\Http\Client::setData)
        — Set the HTTP request body data.
    -   [Swoole\\Http\\Client::setHeaders](/class/swoole-http-client.html#Swoole\Http\Client::setHeaders)
        — Set the HTTP request headers.
    -   [Swoole\\Http\\Client::setMethod](/class/swoole-http-client.html#Swoole\Http\Client::setMethod)
        — Set the HTTP request method.
    -   [Swoole\\Http\\Client::upgrade](/class/swoole-http-client.html#Swoole\Http\Client::upgrade)
        — Upgrade to websocket protocol.
-   [Swoole\\Http\\Request](/class/swoole-http-request.html) — The
    Swoole\\Http\\Request class
    -   [Swoole\\Http\\Request::\_\_destruct](/class/swoole-http-request.html#Swoole\Http\Request::__destruct)
        — Destruct the HTTP request.
    -   [Swoole\\Http\\Request::rawcontent](/class/swoole-http-request.html#Swoole\Http\Request::rawcontent)
        — Get the raw HTTP POST body.
-   [Swoole\\Http\\Response](/class/swoole-http-response.html) — The
    Swoole\\Http\\Response class
    -   [Swoole\\Http\\Response::cookie](/class/swoole-http-response.html#Swoole\Http\Response::cookie)
        — Set the cookies of the HTTP response.
    -   [Swoole\\Http\\Response::\_\_destruct](/class/swoole-http-response.html#Swoole\Http\Response::__destruct)
        — Destruct the HTTP response.
    -   [Swoole\\Http\\Response::end](/class/swoole-http-response.html#Swoole\Http\Response::end)
        — Send data for the HTTP request and finish the response.
    -   [Swoole\\Http\\Response::gzip](/class/swoole-http-response.html#Swoole\Http\Response::gzip)
        — Enable the gzip of response content.
    -   [Swoole\\Http\\Response::header](/class/swoole-http-response.html#Swoole\Http\Response::header)
        — Set the HTTP response headers.
    -   [Swoole\\Http\\Response::initHeader](/class/swoole-http-response.html#Swoole\Http\Response::initHeader)
        — Init the HTTP response header.
    -   [Swoole\\Http\\Response::rawcookie](/class/swoole-http-response.html#Swoole\Http\Response::rawcookie)
        — Set the raw cookies to the HTTP response.
    -   [Swoole\\Http\\Response::sendfile](/class/swoole-http-response.html#Swoole\Http\Response::sendfile)
        — Send file through the HTTP response.
    -   [Swoole\\Http\\Response::status](/class/swoole-http-response.html#Swoole\Http\Response::status)
        — Set the status code of the HTTP response.
    -   [Swoole\\Http\\Response::write](/class/swoole-http-response.html#Swoole\Http\Response::write)
        — Append HTTP body content to the HTTP response.
-   [Swoole\\Http\\Server](/class/swoole-http-server.html) — The
    Swoole\\Http\\Server class
    -   [Swoole\\Http\\Server::on](/class/swoole-http-server.html#Swoole\Http\Server::on)
        — Bind callback function to HTTP server by event name.
    -   [Swoole\\Http\\Server::start](/class/swoole-http-server.html#Swoole\Http\Server::start)
        — Start the swoole http server.
-   [Swoole\\Lock](/class/swoole-lock.html) — The Swoole\\Lock class
    -   [Swoole\\Lock::\_\_construct](/class/swoole-lock.html#Swoole\Lock::__construct)
        — Construct a memory lock.
    -   [Swoole\\Lock::\_\_destruct](/class/swoole-lock.html#Swoole\Lock::__destruct)
        — Destory a Swoole memory lock.
    -   [Swoole\\Lock::lock\_read](/class/swoole-lock.html#Swoole\Lock::lock_read)
        — Lock a read-write lock for reading.
    -   [Swoole\\Lock::lock](/class/swoole-lock.html#Swoole\Lock::lock)
        — Try to acquire the lock. It will block if the lock is not
        available.
    -   [Swoole\\Lock::trylock\_read](/class/swoole-lock.html#Swoole\Lock::trylock_read)
        — Try to lock a read-write lock for reading and return straight
        away even the lock is not available.
    -   [Swoole\\Lock::trylock](/class/swoole-lock.html#Swoole\Lock::trylock)
        — Try to acquire the lock and return straight away even the lock
        is not available.
    -   [Swoole\\Lock::unlock](/class/swoole-lock.html#Swoole\Lock::unlock)
        — Release the lock.
-   [Swoole\\Mmap](/class/swoole-mmap.html) — The Swoole\\Mmap class
    -   [Swoole\\Mmap::open](/class/swoole-mmap.html#Swoole\Mmap::open)
        — Map a file into memory and return the stream resource which
        can be used by PHP stream operations.
-   [Swoole\\MySQL](/class/swoole-mysql.html) — The Swoole\\MySQL class
    -   [Swoole\\MySQL::close](/class/swoole-mysql.html#Swoole\MySQL::close)
        — Close the async MySQL connection.
    -   [Swoole\\MySQL::connect](/class/swoole-mysql.html#Swoole\MySQL::connect)
        — Connect to the remote MySQL server.
    -   [Swoole\\MySQL::\_\_construct](/class/swoole-mysql.html#Swoole\MySQL::__construct)
        — Construct an async MySQL client.
    -   [Swoole\\MySQL::\_\_destruct](/class/swoole-mysql.html#Swoole\MySQL::__destruct)
        — Destory the async MySQL client.
    -   [Swoole\\MySQL::getBuffer](/class/swoole-mysql.html#Swoole\MySQL::getBuffer)
        — Description
    -   [Swoole\\MySQL::on](/class/swoole-mysql.html#Swoole\MySQL::on) —
        Register callback function based on event name.
    -   [Swoole\\MySQL::query](/class/swoole-mysql.html#Swoole\MySQL::query)
        — Run the SQL query.
-   [Swoole\\MySQL\\Exception](/class/swoole-mysql-exception.html) — The
    Swoole\\MySQL\\Exception class
-   [Swoole\\Process](/class/swoole-process.html) — The Swoole\\Process
    class
    -   [Swoole\\Process::alarm](/class/swoole-process.html#Swoole\Process::alarm)
        — High precision timer which triggers signal with fixed
        interval.
    -   [Swoole\\Process::close](/class/swoole-process.html#Swoole\Process::close)
        — Close the pipe to the child process.
    -   [Swoole\\Process::\_\_construct](/class/swoole-process.html#Swoole\Process::__construct)
        — Construct a process.
    -   [Swoole\\Process::daemon](/class/swoole-process.html#Swoole\Process::daemon)
        — Change the process to be a daemon process.
    -   [Swoole\\Process::\_\_destruct](/class/swoole-process.html#Swoole\Process::__destruct)
        — Destory the process.
    -   [Swoole\\Process::exec](/class/swoole-process.html#Swoole\Process::exec)
        — Execute system commands.
    -   [Swoole\\Process::exit](/class/swoole-process.html#Swoole\Process::exit)
        — Stop the child processes.
    -   [Swoole\\Process::freeQueue](/class/swoole-process.html#Swoole\Process::freeQueue)
        — Destroy the message queue created by
        swoole\_process::useQueue.
    -   [Swoole\\Process::kill](/class/swoole-process.html#Swoole\Process::kill)
        — Send signal to the child process.
    -   [Swoole\\Process::name](/class/swoole-process.html#Swoole\Process::name)
        — Set name of the process.
    -   [Swoole\\Process::pop](/class/swoole-process.html#Swoole\Process::pop)
        — Read and pop data from the message queue.
    -   [Swoole\\Process::push](/class/swoole-process.html#Swoole\Process::push)
        — Write and push data into the message queue.
    -   [Swoole\\Process::read](/class/swoole-process.html#Swoole\Process::read)
        — Read data sending to the process.
    -   [Swoole\\Process::signal](/class/swoole-process.html#Swoole\Process::signal)
        — Send signal to the child processes.
    -   [Swoole\\Process::start](/class/swoole-process.html#Swoole\Process::start)
        — Start the process.
    -   [Swoole\\Process::statQueue](/class/swoole-process.html#Swoole\Process::statQueue)
        — Get the stats of the message queue used as the communication
        method between processes.
    -   [Swoole\\Process::useQueue](/class/swoole-process.html#Swoole\Process::useQueue)
        — Create a message queue as the communication method between the
        parent process and child processes.
    -   [Swoole\\Process::wait](/class/swoole-process.html#Swoole\Process::wait)
        — Wait for the events of child processes.
    -   [Swoole\\Process::write](/class/swoole-process.html#Swoole\Process::write)
        — Write data into the pipe and communicate with the parent
        process or child processes.
-   [Swoole\\Redis\\Server](/class/swoole-redis-server.html) — The
    Swoole\\Redis\\Server class
    -   [Swoole\\Redis\\Server::format](/class/swoole-redis-server.html#Swoole\Redis\Server::format)
        — Description
    -   [Swoole\\Redis\\Server::setHandler](/class/swoole-redis-server.html#Swoole\Redis\Server::setHandler)
        — Description
    -   [Swoole\\Redis\\Server::start](/class/swoole-redis-server.html#Swoole\Redis\Server::start)
        — Description
-   [Swoole\\Serialize](/class/swoole-serialize.html) — The
    Swoole\\Serialize class
    -   [Swoole\\Serialize::pack](/class/swoole-serialize.html#Swoole\Serialize::pack)
        — Serialize the data.
    -   [Swoole\\Serialize::unpack](/class/swoole-serialize.html#Swoole\Serialize::unpack)
        — Unserialize the data.
-   [Swoole\\Server](/class/swoole-server.html) — The Swoole\\Server
    class
    -   [Swoole\\Server::addlistener](/class/swoole-server.html#Swoole\Server::addlistener)
        — Add a new listener to the server.
    -   [Swoole\\Server::addProcess](/class/swoole-server.html#Swoole\Server::addProcess)
        — Add a user defined swoole\_process to the server.
    -   [Swoole\\Server::after](/class/swoole-server.html#Swoole\Server::after)
        — Trigger a callback function after a period of time.
    -   [Swoole\\Server::bind](/class/swoole-server.html#Swoole\Server::bind)
        — Bind the connection to a user defined user ID.
    -   [Swoole\\Server::clearTimer](/class/swoole-server.html#Swoole\Server::clearTimer)
        — Stop and destory a timer.
    -   [Swoole\\Server::close](/class/swoole-server.html#Swoole\Server::close)
        — Close a connection to the client.
    -   [Swoole\\Server::confirm](/class/swoole-server.html#Swoole\Server::confirm)
        — Check status of the connection.
    -   [Swoole\\Server::connection\_info](/class/swoole-server.html#Swoole\Server::connection_info)
        — Get the connection info by file description.
    -   [Swoole\\Server::connection\_list](/class/swoole-server.html#Swoole\Server::connection_list)
        — Get all of the established connections.
    -   [Swoole\\Server::\_\_construct](/class/swoole-server.html#Swoole\Server::__construct)
        — Construct a Swoole server.
    -   [Swoole\\Server::defer](/class/swoole-server.html#Swoole\Server::defer)
        — Delay execution of the callback function at the end of current
        EventLoop.
    -   [Swoole\\Server::exist](/class/swoole-server.html#Swoole\Server::exist)
        — Check if the connection is existed.
    -   [Swoole\\Server::finish](/class/swoole-server.html#Swoole\Server::finish)
        — Used in task process for sending result to the worker process
        when the task is finished.
    -   [Swoole\\Server::getClientInfo](/class/swoole-server.html#Swoole\Server::getClientInfo)
        — Get the connection info by file description.
    -   [Swoole\\Server::getClientList](/class/swoole-server.html#Swoole\Server::getClientList)
        — Get all of the established connections.
    -   [Swoole\\Server::getLastError](/class/swoole-server.html#Swoole\Server::getLastError)
        — Get the error code of the most recent error.
    -   [Swoole\\Server::heartbeat](/class/swoole-server.html#Swoole\Server::heartbeat)
        — Check all the connections on the server.
    -   [Swoole\\Server::listen](/class/swoole-server.html#Swoole\Server::listen)
        — Listen on the given IP and port, socket type.
    -   [Swoole\\Server::on](/class/swoole-server.html#Swoole\Server::on)
        — Register a callback function by event name.
    -   [Swoole\\Server::pause](/class/swoole-server.html#Swoole\Server::pause)
        — Stop receiving data from the connection.
    -   [Swoole\\Server::protect](/class/swoole-server.html#Swoole\Server::protect)
        — Set the connection to be protected mode.
    -   [Swoole\\Server::reload](/class/swoole-server.html#Swoole\Server::reload)
        — Restart all the worker process.
    -   [Swoole\\Server::resume](/class/swoole-server.html#Swoole\Server::resume)
        — Start receving data from the connection.
    -   [Swoole\\Server::send](/class/swoole-server.html#Swoole\Server::send)
        — Send data to the client.
    -   [Swoole\\Server::sendfile](/class/swoole-server.html#Swoole\Server::sendfile)
        — Send file to the connection.
    -   [Swoole\\Server::sendMessage](/class/swoole-server.html#Swoole\Server::sendMessage)
        — Send message to worker processes by ID.
    -   [Swoole\\Server::sendto](/class/swoole-server.html#Swoole\Server::sendto)
        — Send data to the remote UDP address.
    -   [Swoole\\Server::sendwait](/class/swoole-server.html#Swoole\Server::sendwait)
        — Send data to the remote socket in the blocking way.
    -   [Swoole\\Server::set](/class/swoole-server.html#Swoole\Server::set)
        — Set the runtime settings of the swoole server.
    -   [Swoole\\Server::shutdown](/class/swoole-server.html#Swoole\Server::shutdown)
        — Shutdown the master server process, this function can be
        called in worker processes.
    -   [Swoole\\Server::start](/class/swoole-server.html#Swoole\Server::start)
        — Start the Swoole server.
    -   [Swoole\\Server::stats](/class/swoole-server.html#Swoole\Server::stats)
        — Get the stats of the Swoole server.
    -   [Swoole\\Server::stop](/class/swoole-server.html#Swoole\Server::stop)
        — Stop the Swoole server.
    -   [Swoole\\Server::task](/class/swoole-server.html#Swoole\Server::task)
        — Send data to the task worker processes.
    -   [Swoole\\Server::taskwait](/class/swoole-server.html#Swoole\Server::taskwait)
        — Send data to the task worker processes in blocking way.
    -   [Swoole\\Server::taskWaitMulti](/class/swoole-server.html#Swoole\Server::taskWaitMulti)
        — Execute multiple tasks concurrently.
    -   [Swoole\\Server::tick](/class/swoole-server.html#Swoole\Server::tick)
        — Repeats a given function at every given time-interval.
-   [Swoole\\Table](/class/swoole-table.html) — The Swoole\\Table class
    -   [Swoole\\Table::column](/class/swoole-table.html#Swoole\Table::column)
        — Set the data type and size of the columns.
    -   [Swoole\\Table::\_\_construct](/class/swoole-table.html#Swoole\Table::__construct)
        — Construct a Swoole memory table with fixed size.
    -   [Swoole\\Table::count](/class/swoole-table.html#Swoole\Table::count)
        — Count the rows in the table, or count all the elements in the
        table if $mode = 1.
    -   [Swoole\\Table::create](/class/swoole-table.html#Swoole\Table::create)
        — Create the swoole memory table.
    -   [Swoole\\Table::current](/class/swoole-table.html#Swoole\Table::current)
        — Get the current row.
    -   [Swoole\\Table::decr](/class/swoole-table.html#Swoole\Table::decr)
        — Decrement the value in the Swoole table by $row\_key and
        $column\_key.
    -   [Swoole\\Table::del](/class/swoole-table.html#Swoole\Table::del)
        — Delete a row in the Swoole table by $row\_key.
    -   [Swoole\\Table::destroy](/class/swoole-table.html#Swoole\Table::destroy)
        — Destroy the Swoole table.
    -   [Swoole\\Table::exist](/class/swoole-table.html#Swoole\Table::exist)
        — Check if a row is existed by $row\_key.
    -   [Swoole\\Table::get](/class/swoole-table.html#Swoole\Table::get)
        — Get the value in the Swoole table by $row\_key and
        $column\_key.
    -   [Swoole\\Table::incr](/class/swoole-table.html#Swoole\Table::incr)
        — Increment the value by $row\_key and $column\_key.
    -   [Swoole\\Table::key](/class/swoole-table.html#Swoole\Table::key)
        — Get the key of current row.
    -   [Swoole\\Table::next](/class/swoole-table.html#Swoole\Table::next)
        — Iterator the next row.
    -   [Swoole\\Table::rewind](/class/swoole-table.html#Swoole\Table::rewind)
        — Rewind the iterator.
    -   [Swoole\\Table::set](/class/swoole-table.html#Swoole\Table::set)
        — Update a row of the table by $row\_key.
    -   [Swoole\\Table::valid](/class/swoole-table.html#Swoole\Table::valid)
        — Check current if the current row is valid.
-   [Swoole\\Timer](/class/swoole-timer.html) — The Swoole\\Timer class
    -   [Swoole\\Timer::after](/class/swoole-timer.html#Swoole\Timer::after)
        — Trigger a callback function after a period of time.
    -   [Swoole\\Timer::clear](/class/swoole-timer.html#Swoole\Timer::clear)
        — Delete a timer by timer ID.
    -   [Swoole\\Timer::exists](/class/swoole-timer.html#Swoole\Timer::exists)
        — Check if a timer is existed.
    -   [Swoole\\Timer::tick](/class/swoole-timer.html#Swoole\Timer::tick)
        — Repeats a given function at every given time-interval.
-   [Swoole\\WebSocket\\Frame](/class/swoole-websocket-frame.html) — The
    Swoole\\WebSocket\\Frame class
-   [Swoole\\WebSocket\\Server](/class/swoole-websocket-server.html) —
    The Swoole\\WebSocket\\Server class
    -   [Swoole\\WebSocket\\Server::exist](/class/swoole-websocket-server.html#Swoole\WebSocket\Server::exist)
        — Check if the file descriptor exists.
    -   [Swoole\\WebSocket\\Server::on](/class/swoole-websocket-server.html#Swoole\WebSocket\Server::on)
        — Register event callback function
    -   [Swoole\\WebSocket\\Server::pack](/class/swoole-websocket-server.html#Swoole\WebSocket\Server::pack)
        — Get a pack of binary data to send in a single frame.
    -   [Swoole\\WebSocket\\Server::push](/class/swoole-websocket-server.html#Swoole\WebSocket\Server::push)
        — Push data to the remote client.
    -   [Swoole\\WebSocket\\Server::unpack](/class/swoole-websocket-server.html#Swoole\WebSocket\Server::unpack)
        — Unpack the binary data received from the client.

简介
----

类摘要
------

**Swoole\\Async**

<span class="ooclass"> class **Swoole\\Async** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">dnsLookup</span> ( <span class="methodparam"><span
class="type">string</span> `$hostname`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">read</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$chunk_size`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`</span> \]\]
)

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">readFile</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">set</span> ( <span class="methodparam"><span
class="type">array</span> `$settings`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">write</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">writeFile</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$flags`</span> \]\] )

}

Swoole\\Async::dnsLookup
========================

Async and non-blocking hostname to IP lookup.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Async::dnsLookup</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`hostname`  
The host name.

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
, <span class="methodparam"><span class="type">string</span>
`$ip`</span> )

`hostname`  
The host name.

`IP`  
The IP address.

Swoole\\Async::read
===================

Read file stream asynchronously.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Swoole\\Async::read</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$chunk_size`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`</span> \]\]
)

### 参数

`filename`  
The name of the file.

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> )

`filename`  
The name of the file.

`content`  
The content readed from the file stream.

`chunk_size`  
The chunk length.

`offset`  
The offset.

### 返回值

Whether the read is succeed.

Swoole\\Async::readFile
=======================

Read a file asynchronously.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Async::readFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`filename`  
The filename of the file being read.

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> )

`filename`  
The name of the file.

`content`  
The content readed from the file.

Swoole\\Async::set
==================

Update the async I/O options.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Async::set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

### 参数

`settings`  

Swoole\\Async::write
====================

Write data to a file stream asynchronously.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Async::write</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \]\] )

### 参数

`filename`  
The filename being written.

`content`  
The content writing to the file.

`offset`  
The offset.

`callback`  

Swoole\\Async::writeFile
========================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Async::writeFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$flags`</span>
\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filename`  
The filename being written.

`content`  
The content writing to the file.

`callback`  

`flags`  

简介
----

类摘要
------

**Swoole\\Atomic**

<span class="ooclass"> class **Swoole\\Atomic** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">add</span> (\[ <span class="methodparam"><span
class="type">int</span> `$add_value`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">cmpset</span> ( <span class="methodparam"><span
class="type">int</span> `$cmp_value`</span> , <span
class="methodparam"><span class="type">int</span> `$new_value`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">get</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">sub</span> (\[ <span class="methodparam"><span
class="type">int</span> `$sub_value`</span> \] )

}

Swoole\\Atomic::add
===================

Add a number to the value to the atomic object.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Atomic::add</span> (\[ <span
class="methodparam"><span class="type">int</span> `$add_value`</span> \]
)

Add a number to the value to the atomic object.

### 参数

`add_value`  
The value which will be added to the current value.

### 返回值

The new value of the atomic object.

Swoole\\Atomic::cmpset
======================

Compare and set the value of the atomic object.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Atomic::cmpset</span> ( <span
class="methodparam"><span class="type">int</span> `$cmp_value`</span> ,
<span class="methodparam"><span class="type">int</span>
`$new_value`</span> )

### 参数

`cmp_value`  
The value to compare with the current value of the atomic object.

`new_value`  
The value to set to the atomic object if the cmp\_value is the same as
the current value of the atomic object.

### 返回值

The new value of the atomic object.

Swoole\\Atomic::\_\_construct
=============================

Construct a swoole atomic object.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Atomic::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$value`</span> \] )

Swoole atomic object is a integer variable allows any processor to
atomically test and modify. It is implemented based on CPU atomic
instructions. The Swoole atomic variables have to defined before
swoole\_server-\>start.

Compare-and-swap (CAS) is an atomic instruction used in multithreading
to achieve synchronization. It compares the content of a memory location
with a given value and, only if they are the same, modifies the content
of that memory location to a new given value.

### 参数

`value`  
The value of the atomic object.

Swoole\\Atomic::get
===================

Get the current value of the atomic object.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Atomic::get</span> ( <span
class="methodparam">void</span> )

Get the current value of the atomic object.

### 参数

此函数没有参数。

### 返回值

The current value of the atomic object.

Swoole\\Atomic::set
===================

Set a new value to the atomic object.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Atomic::set</span> ( <span
class="methodparam"><span class="type">int</span> `$value`</span> )

Set a new value to the atomic object.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`value`  
The value to set to the atomic object.

### 返回值

The current value of the atomic object.

Swoole\\Atomic::sub
===================

Subtract a number to the value of the atomic object.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Atomic::sub</span> (\[ <span
class="methodparam"><span class="type">int</span> `$sub_value`</span> \]
)

Subtract a number to the value of the atomic object.

### 参数

`sub_value`  
The value which will be subtracted to the current value.

### 返回值

The current value of the atomic object.

简介
----

类摘要
------

**Swoole\\Buffer**

<span class="ooclass"> class **Swoole\\Buffer** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">append</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">expand</span> ( <span class="methodparam"><span
class="type">int</span> `$size`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">read</span> ( <span class="methodparam"><span
class="type">int</span> `$offset`</span> , <span
class="methodparam"><span class="type">int</span> `$length`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">recycle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">substr</span> ( <span class="methodparam"><span
class="type">int</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$remove`</span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">write</span> ( <span class="methodparam"><span
class="type">int</span> `$offset`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

}

Swoole\\Buffer::append
======================

Append the string or binary data at the end of the memory buffer and
return the new size of memory allocated.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Buffer::append</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 参数

`data`  
The string or binary data to append at the end of the memory buffer.

### 返回值

The new size of the memory buffer.

Swoole\\Buffer::clear
=====================

Reset the memory buffer.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Buffer::clear</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

Swoole\\Buffer::\_\_construct
=============================

Fixed size memory blocks allocation.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Buffer::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$size`</span> \] )

### 参数

`size`  
The size of the memory to allocate.

Swoole\\Buffer::\_\_destruct
============================

Destruct the Swoole memory buffer.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Buffer::\_\_destruct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

Swoole\\Buffer::expand
======================

Expand the size of memory buffer.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Buffer::expand</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> )

### 参数

`size`  
The new size of the memory buffer.

### 返回值

The new size of the memory buffer.

Swoole\\Buffer::read
====================

Read data from the memory buffer based on offset and length.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Buffer::read</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$length`</span>
)

### 参数

`offset`  
The offset.

`length`  
The length.

### 返回值

The data readed from the memory buffer.

Swoole\\Buffer::recycle
=======================

Release the memory to OS which is not used by the memory buffer.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Buffer::recycle</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

Swoole\\Buffer::substr
======================

Read data from the memory buffer based on offset and length. Or remove
data from the memory buffer.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Buffer::substr</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$remove`</span> \]\] )

If $remove is set to be true and $offset is set to be 0, the data will
be removed from the buffer. The memory for storing the data will be
released when the buffer object is deconstructed.

### 参数

`offset`  
The offset.

`length`  
The length.

`remove`  
Whether to remove the data from the memory buffer.

### 返回值

The data or string readed from the memory buffer.

Swoole\\Buffer::\_\_toString
============================

Get the string value of the memory buffer.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Buffer::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The string value of the memory buffer.

Swoole\\Buffer::write
=====================

Write data to the memory buffer. The memory allocated for the buffer
will not be changed.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Buffer::write</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

### 参数

`offset`  
The offset.

`data`  
The data to write to the memory buffer.

### 返回值

简介
----

类摘要
------

**Swoole\\Channel**

<span class="ooclass"> class **Swoole\\Channel** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">stats</span> ( <span
class="methodparam">void</span> )

}

Swoole\\Channel::\_\_construct
==============================

Construct a Swoole Channel

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Channel::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$size`</span> )

Swoole channel is memory data structure works like Chan in Golang,
implemented based on shared memory and mutex locks. It can be used as
high performance message queue in memory. Construct a swoole channel
with a fixed size. The minimum size of a swoole channel is 64KB.
Exceptions will be thrown if there is not enough memory.

### 参数

`size`  
The size of the Swoole channel.

Swoole\\Channel::\_\_destruct
=============================

Destruct a Swoole channel.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Channel::\_\_destruct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

Swoole\\Channel::pop
====================

Read and pop data from swoole channel.

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Channel::pop</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

If the channel is empty, the function will return false, or return the
unserialized data.

Swoole\\Channel::push
=====================

Write and push data into Swoole channel.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Channel::push</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

Data can be any non-empty PHP variable, the variable will be serialized
if it is not string type.

If size of the data is more than 8KB, swoole channel will use temp files
storage.

The function will return true if the write operation is succeeded, or
return false if there is not enough space.

### 参数

`data`  
The data to push into the Swoole channel.

### 返回值

Wheter the data is pushed into he Swoole channel.

Swoole\\Channel::stats
======================

Get stats of swoole channel.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Channel::stats</span> ( <span
class="methodparam">void</span> )

Get the numbers of queued elements and total size of the memory used by
the queue.

### 参数

此函数没有参数。

### 返回值

The stats of the Swoole channel.

简介
----

类摘要
------

**Swoole\\Client**

<span class="ooclass"> class **Swoole\\Client** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Client::MSG_OOB` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Client::MSG_PEEK` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Client::MSG_DONTWAIT` <span class="initializer"> = 128</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Client::MSG_WAITALL` <span class="initializer"> = 64</span> ;

/\* 属性 \*/

<span class="modifier">public</span> `$errCode` ;

<span class="modifier">public</span> `$sock` ;

<span class="modifier">public</span> `$reuse` ;

<span class="modifier">public</span> `$reuseCount` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$force`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flag`</span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getpeername</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getsockname</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isConnected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">on</span> ( <span class="methodparam"><span
class="type">string</span> `$event`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pause</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pipe</span> ( <span class="methodparam"><span
class="type">string</span> `$socket`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">recv</span> (\[ <span class="methodparam"><span
class="type">string</span> `$size`</span> \[, <span
class="methodparam"><span class="type">string</span> `$flag`</span> \]\]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resume</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">send</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">string</span> `$flag`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendfile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendto</span> ( <span class="methodparam"><span
class="type">string</span> `$ip`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">array</span> `$settings`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sleep</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">wakeup</span> ( <span
class="methodparam">void</span> )

}

属性
----

`errCode`  

`sock`  

`reuse`  

`reuseCount`  

预定义常量
----------

**`Swoole\Client::MSG_OOB`**  

**`Swoole\Client::MSG_PEEK`**  

**`Swoole\Client::MSG_DONTWAIT`**  

**`Swoole\Client::MSG_WAITALL`**  

Swoole\\Client::close
=====================

Close the connection established.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Client::close</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$force`</span> \] )

### 参数

`force`  
Whether force to close the connection.

### 返回值

Whether the connection is closed.

Swoole\\Client::connect
=======================

Connect to the remote TCP or UDP port.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Client::connect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flag`</span> \]\]\] )

### 参数

`host`  
The host name of the remote address.

`port`  
The port number of the remote address.

`timeout`  
The timeout(second) of connect/send/recv, the dafault value is 0.1s

`flag`  
If the type of client is UDP, the $flag means if to enable the
configuration udp\_connect. If the configuration udp\_connect is
enabled, the client will only receive the data from specified ip:port.
If the type of client is TCP and the $flag is set to 1, it must use
swoole\_client\_select to check the connection status before send/recv.

### 返回值

Whether the connection is established.

Swoole\\Client::\_\_construct
=============================

Create Swoole sync or async TCP/UDP client, with or without SSL.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Client::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$sock_type`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$is_async`</span> \] )

### 参数

`sock_type`  
The type of socket: SWOOLE\_TCP, SWOOLE\_UDP, SWOOLE\_ASYNC,
SWOOLE\_SSL, SWOOLE\_KEEP.

`is_async`  
Synchronous or asynchronous client.

Swoole\\Client::\_\_destruct
============================

Destruct the Swoole client.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::\_\_destruct</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

Swoole\\Client::getpeername
===========================

Get the remote socket name of the connection.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Client::getpeername</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The host and port of the remote socket.

Swoole\\Client::getsockname
===========================

Get the local socket name of the connection.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Client::getsockname</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The host and port of the local socket.

Swoole\\Client::isConnected
===========================

Check if the connection is established.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Client::isConnected</span> ( <span
class="methodparam">void</span> )

This method returns the connection status of application layer.

### 参数

此函数没有参数。

### 返回值

Whether the connection is established.

Swoole\\Client::on
==================

Add callback functions triggered by events.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::on</span> ( <span
class="methodparam"><span class="type">string</span> `$event`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`event`  

`callback`  

Swoole\\Client::pause
=====================

Pause receiving data.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::pause</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

Swoole\\Client::pipe
====================

Redirect the data to another file descriptor.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::pipe</span> ( <span
class="methodparam"><span class="type">string</span> `$socket`</span> )

### 参数

`socket`  

Swoole\\Client::recv
====================

Receive data from the remote socket.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::recv</span> (\[ <span
class="methodparam"><span class="type">string</span> `$size`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$flag`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`size`  

`flag`  

### 返回值

Swoole\\Client::resume
======================

Resume receiving data.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::resume</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

Swoole\\Client::send
====================

Send data to the remote TCP socket.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Client::send</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$flag`</span> \] )

### 参数

`data`  
The data to send which can be string or binary

`flag`  

### 返回值

If the client sends data successfully, it returns the length of data
sent. Or it returns false and sets $swoole\_client-\>errCode. For sync
client, there is no limit for the data to send. For async client, The
limit for the data to send is socket\_buffer\_size.

Swoole\\Client::sendfile
========================

Send file to the remote TCP socket.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Client::sendfile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

This is a wrapper of the Linux sendfile system call.

### 参数

`filename`  
File path of the file to send.

`offset`  
Offset of the file to send

### 返回值

Swoole\\Client::sendto
======================

Send data to the remote UDP address.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Client::sendto</span> ( <span
class="methodparam"><span class="type">string</span> `$ip`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

The swoole client should be type of SWOOLE\_SOCK\_UDP or
SWOOLE\_SOCK\_UDP6.

### 参数

`ip`  
The IP address of remote host, IPv4 or IPv6.

`port`  
The port number of remote host.

`data`  
The data to send which should be less-than 64K.

### 返回值

Swoole\\Client::set
===================

Set the Swoole client parameters before the connection is established.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

### 参数

`settings`  

### 返回值

Swoole\\Client::sleep
=====================

Remove the TCP client from system event loop.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::sleep</span> ( <span
class="methodparam">void</span> )

Remove the TCP client from system event loop.

### 参数

此函数没有参数。

### 返回值

Swoole\\Client::wakeup
======================

Add the TCP client back into the system event loop.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Client::wakeup</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Connection\\Iterator**

<span class="ooclass"> class **Swoole\\Connection\\Iterator** </span>
<span class="oointerface">implements <span
class="interfacename">Iterator</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> <span class="oointerface">, <span
class="interfacename">ArrayAccess</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span
class="type">Connection</span> <span class="methodname">current</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">key</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Connection</span> <span class="methodname">next</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span
class="type">Connection</span> <span class="methodname">offsetGet</span>
( <span class="methodparam"><span class="type">string</span>
`$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$connection`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

Swoole\\Connection\\Iterator::count
===================================

Count connections.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Connection\\Iterator::count</span> ( <span
class="methodparam">void</span> )

Gets the number of connections.

### 参数

此函数没有参数。

### 返回值

The number of connections.

Swoole\\Connection\\Iterator::current
=====================================

Return current connection entry.

### 说明

<span class="modifier">public</span> <span
class="type">Connection</span> <span
class="methodname">Swoole\\Connection\\Iterator::current</span> ( <span
class="methodparam">void</span> )

Get current connection entry.

### 参数

此函数没有参数。

### 返回值

The current connection entry.

Swoole\\Connection\\Iterator::key
=================================

Return key of the current connection.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Connection\\Iterator::key</span> ( <span
class="methodparam">void</span> )

This function returns key of the current connection.

### 参数

此函数没有参数。

### 返回值

Key of the current connection.

Swoole\\Connection\\Iterator::next
==================================

Move to the next connection.

### 说明

<span class="modifier">public</span> <span
class="type">Connection</span> <span
class="methodname">Swoole\\Connection\\Iterator::next</span> ( <span
class="methodparam">void</span> )

The iterator to the next connection.

### 参数

此函数没有参数。

### 返回值

Swoole\\Connection\\Iterator::offsetExists
==========================================

Check if offet exists.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span
class="methodname">Swoole\\Connection\\Iterator::offsetExists</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

Check if offset exists.

### 参数

`index`  
The offset being checked.

### 返回值

Returns TRUE if the offset exists, otherwise FALSE.

Swoole\\Connection\\Iterator::offsetGet
=======================================

Offset to retrieve.

### 说明

<span class="modifier">public</span> <span
class="type">Connection</span> <span
class="methodname">Swoole\\Connection\\Iterator::offsetGet</span> (
<span class="methodparam"><span class="type">string</span>
`$index`</span> )

Return the connection at specified offset.

### 参数

`index`  
The offset to retrieve.

### 返回值

Swoole\\Connection\\Iterator::offsetSet
=======================================

Assign a Connection to the specified offset.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Connection\\Iterator::offsetSet</span>
( <span class="methodparam"><span class="type">int</span>
`$offset`</span> , <span class="methodparam"><span
class="type">mixed</span> `$connection`</span> )

Assign a Connection to the specified offset.

### 参数

`offset`  
The offset to assign the Connection to.

`connection`  
The connection to set.

### 返回值

Swoole\\Connection\\Iterator::offsetUnset
=========================================

Unset an offset.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span
class="methodname">Swoole\\Connection\\Iterator::offsetUnset</span> (
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

Unsets an offset.

### 参数

`offset`  
The offset to unset.

### 返回值

Swoole\\Connection\\Iterator::rewind
====================================

Rewinds iterator

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Connection\\Iterator::rewind</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Connection\\Iterator::valid
===================================

Check if current position is valid.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Connection\\Iterator::valid</span> (
<span class="methodparam">void</span> )

Checks if the current position is valid.

### 参数

此函数没有参数。

### 返回值

Returns TRUE if the current iterator position is valid, otherwise FALSE.

简介
----

类摘要
------

**Swoole\\Coroutine**

<span class="ooclass"> class **Swoole\\Coroutine** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">call\_user\_func\_array</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">array</span> `$param_array`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">call\_user\_func</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">mixed</span> `$args`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">cli\_wait</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">create</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">getuid</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">resume</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">suspend</span> ( <span
class="methodparam">void</span> )

}

Swoole\\Coroutine::call\_user\_func\_array
==========================================

Call a callback with an array of parameters

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">Swoole\\Coroutine::call\_user\_func\_array</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">array</span> `$param_array`</span> )

Calls the callback given by the first parameter with the parameters in
param\_array.

### 参数

`callback`  
The <span class="type">callable</span> to be called.

`param_array`  
Zero or more parameters in the array to be passed to the callback.

### 返回值

Swoole\\Coroutine::call\_user\_func
===================================

Call a callback given by the first parameter

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">mixed</span> <span
class="methodname">Swoole\\Coroutine::call\_user\_func</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> , <span class="methodparam"><span
class="type">mixed</span> `$args`</span> )

Calls the `callback` given by the first parameter and passes the
remaining parameters as arguments.

### 参数

`callback`  
The <span class="type">callable</span> to be called.

`args`  
Zero or more parameters to be passed to the callback.

### 返回值

Swoole\\Coroutine::cli\_wait
============================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Coroutine::cli\_wait</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Coroutine::create
=========================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Coroutine::create</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Swoole\\Coroutine::getuid
=========================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Coroutine::getuid</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Swoole\\Coroutine::resume
=========================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Coroutine::resume</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Swoole\\Coroutine::suspend
==========================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Coroutine::suspend</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Event**

<span class="ooclass"> class **Swoole\\Event** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">add</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> , <span class="methodparam"><span
class="type">callable</span> `$read_callback`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$write_callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$events`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">defer</span> ( <span class="methodparam"><span
class="type">mixed</span> `$callback`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">del</span> ( <span class="methodparam"><span
class="type">string</span> `$fd`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">exit</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> \[, <span class="methodparam"><span
class="type">string</span> `$read_callback`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$write_callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$events`</span> \]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">wait</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">write</span> ( <span class="methodparam"><span
class="type">string</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

}

Swoole\\Event::add
==================

Add new callback functions of a socket into the EventLoop.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Swoole\\Event::add</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">callable</span>
`$read_callback`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$write_callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$events`</span>
\]\] )

### 参数

`fd`  

`read_callback`  

`write_callback`  

`events`  

### 返回值

Swoole\\Event::defer
====================

Add a callback function to the next event loop.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Event::defer</span> ( <span
class="methodparam"><span class="type">mixed</span> `$callback`</span> )

### 参数

`callback`  

### 返回值

Swoole\\Event::del
==================

Remove all event callback functions of a socket.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Swoole\\Event::del</span> ( <span
class="methodparam"><span class="type">string</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

Swoole\\Event::exit
===================

Exit the eventloop, only available at client side.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Event::exit</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Event::set
==================

Update the event callback functions of a socket.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Swoole\\Event::set</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$read_callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$write_callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$events`</span>
\]\]\] )

### 参数

`fd`  

`read_callback`  

`write_callback`  

`events`  

### 返回值

Swoole\\Event::wait
===================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Event::wait</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Swoole\\Event::write
====================

Write data to the socket.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Event::write</span> ( <span
class="methodparam"><span class="type">string</span> `$fd`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

### 参数

`fd`  

`data`  

### 返回值

简介
----

类摘要
------

**Swoole\\Exception**

<span class="ooclass"> class **Swoole\\Exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> <span class="oointerface">implements <span
class="interfacename">Throwable</span> </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

}

简介
----

类摘要
------

**Swoole\\Http\\Client**

<span class="ooclass"> class **Swoole\\Http\\Client** </span> {

/\* 属性 \*/

<span class="modifier">public</span> `$errCode` ;

<span class="modifier">public</span> `$sock` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$type`</span> \[, <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$offset`</span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">download</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$file`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">execute</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isConnected</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">on</span> ( <span class="methodparam"><span
class="type">string</span> `$event_name`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">post</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">string</span> `$opcode`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$finish`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">array</span> `$settings`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCookies</span> ( <span
class="methodparam"><span class="type">array</span> `$cookies`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">setData</span> (
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setHeaders</span> ( <span
class="methodparam"><span class="type">array</span> `$headers`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$method`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">upgrade</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$callback`</span> )

}

属性
----

`errCode`  

`sock`  

Swoole\\Http\\Client::addFile
=============================

Add a file to the post form.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$type`</span> \[, <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$offset`</span> \]\]\] )

### 参数

`path`  

`name`  

`type`  

`filename`  

`offset`  

### 返回值

Swoole\\Http\\Client::close
===========================

Close the http connection.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::close</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Http\\Client::\_\_construct
===================================

Construct the async HTTP client.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Http\\Client::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$port`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$ssl`</span> \]\] )

### 参数

`host`  
The hostname of the remote host.

`port`  
The port number of the remote host.

`ssl`  
Whether to enable SSL.

Swoole\\Http\\Client::\_\_destruct
==================================

Destruct the HTTP client.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::\_\_destruct</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Http\\Client::download
==============================

Download a file from the remote server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::download</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$file`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$offset`</span> \] )

### 参数

`path`  

`file`  

`callback`  

`offset`  

### 返回值

Swoole\\Http\\Client::execute
=============================

Send the HTTP request after setting the parameters.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::execute</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$callback`</span> )

### 参数

`path`  

`callback`  

### 返回值

Swoole\\Http\\Client::get
=========================

Send GET http request to the remote server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::get</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`path`  

`callback`  

### 返回值

Swoole\\Http\\Client::isConnected
=================================

Check if the HTTP connection is connected.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Http\\Client::isConnected</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Http\\Client::on
========================

Register callback function by event name.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

### 参数

`event_name`  

`callback`  

### 返回值

Swoole\\Http\\Client::post
==========================

Send POST http request to the remote server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::post</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

### 参数

`path`  

`data`  

`callback`  

### 返回值

Swoole\\Http\\Client::push
==========================

Push data to websocket client.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::push</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$opcode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$finish`</span> \]\] )

### 参数

`data`  

`opcode`  

`finish`  

### 返回值

Swoole\\Http\\Client::set
=========================

Update the HTTP client paramters.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

### 参数

`settings`  

### 返回值

Swoole\\Http\\Client::setCookies
================================

Set the http request cookies.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::setCookies</span> ( <span
class="methodparam"><span class="type">array</span> `$cookies`</span> )

### 参数

`cookies`  

### 返回值

Swoole\\Http\\Client::setData
=============================

Set the HTTP request body data.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Http\\Client::setData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

The HTTP method will be changed to be POST.

### 参数

`data`  

### 返回值

Swoole\\Http\\Client::setHeaders
================================

Set the HTTP request headers.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::setHeaders</span> ( <span
class="methodparam"><span class="type">array</span> `$headers`</span> )

### 参数

`headers`  

### 返回值

Swoole\\Http\\Client::setMethod
===============================

Set the HTTP request method.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::setMethod</span> ( <span
class="methodparam"><span class="type">string</span> `$method`</span> )

### 参数

`method`  

### 返回值

Swoole\\Http\\Client::upgrade
=============================

Upgrade to websocket protocol.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Client::upgrade</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$callback`</span> )

### 参数

`path`  

`callback`  

### 返回值

简介
----

类摘要
------

**Swoole\\Http\\Request**

<span class="ooclass"> class **Swoole\\Http\\Request** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">rawcontent</span> ( <span
class="methodparam">void</span> )

}

Swoole\\Http\\Request::\_\_destruct
===================================

Destruct the HTTP request.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Request::\_\_destruct</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Http\\Request::rawcontent
=================================

Get the raw HTTP POST body.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Http\\Request::rawcontent</span> (
<span class="methodparam">void</span> )

This method is used for the POST data which isn't in the form of
\`application/x-www-form-urlencoded\`.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Http\\Response**

<span class="ooclass"> class **Swoole\\Http\\Response** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">cookie</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$expires`</span> \[, <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">string</span> `$domain`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$secure`</span> \[, <span class="methodparam"><span
class="type">string</span> `$httponly`</span> \]\]\]\]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">end</span> (\[ <span class="methodparam"><span
class="type">string</span> `$content`</span> \] )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">gzip</span> (\[
<span class="methodparam"><span class="type">string</span>
`$compress_level`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">header</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$ucwords`</span> \] )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">initHeader</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">rawcookie</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$value`</span> \[, <span
class="methodparam"><span class="type">string</span> `$expires`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">string</span> `$domain`</span> \[, <span
class="methodparam"><span class="type">string</span> `$secure`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$httponly`</span> \]\]\]\]\]\] )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">sendfile</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`</span> \] )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">status</span> (
<span class="methodparam"><span class="type">string</span>
`$http_code`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">write</span> ( <span class="methodparam"><span
class="type">string</span> `$content`</span> )

}

Swoole\\Http\\Response::cookie
==============================

Set the cookies of the HTTP response.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Http\\Response::cookie</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$expires`</span> \[, <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$domain`</span> \[, <span class="methodparam"><span
class="type">string</span> `$secure`</span> \[, <span
class="methodparam"><span class="type">string</span> `$httponly`</span>
\]\]\]\]\]\] )

### 参数

`name`  

`value`  

`expires`  

`path`  

`domain`  

`secure`  

`httponly`  

### 返回值

Swoole\\Http\\Response::\_\_destruct
====================================

Destruct the HTTP response.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Response::\_\_destruct</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Http\\Response::end
===========================

Send data for the HTTP request and finish the response.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Response::end</span> (\[ <span
class="methodparam"><span class="type">string</span> `$content`</span>
\] )

### 参数

`content`  

### 返回值

Swoole\\Http\\Response::gzip
============================

Enable the gzip of response content.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Http\\Response::gzip</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$compress_level`</span> \] )

The header about Content-Encoding will be added automatically.

### 参数

`compress_level`  

### 返回值

Swoole\\Http\\Response::header
==============================

Set the HTTP response headers.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Response::header</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$ucwords`</span> \] )

### 参数

`key`  

`value`  

`ucwords`  

### 返回值

Swoole\\Http\\Response::initHeader
==================================

Init the HTTP response header.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Http\\Response::initHeader</span> ( <span
class="methodparam">void</span> )

Init the HTTP response header.

### 参数

此函数没有参数。

### 返回值

Swoole\\Http\\Response::rawcookie
=================================

Set the raw cookies to the HTTP response.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Http\\Response::rawcookie</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$expires`</span> \[, <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$domain`</span> \[, <span class="methodparam"><span
class="type">string</span> `$secure`</span> \[, <span
class="methodparam"><span class="type">string</span> `$httponly`</span>
\]\]\]\]\]\] )

### 参数

`name`  

`value`  

`expires`  

`path`  

`domain`  

`secure`  

`httponly`  

### 返回值

Swoole\\Http\\Response::sendfile
================================

Send file through the HTTP response.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Http\\Response::sendfile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

Send file through the HTTP response.

### 参数

`filename`  

`offset`  

### 返回值

Swoole\\Http\\Response::status
==============================

Set the status code of the HTTP response.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Http\\Response::status</span> ( <span
class="methodparam"><span class="type">string</span> `$http_code`</span>
)

Set the status code of the HTTP response.

### 参数

`http_code`  

### 返回值

Swoole\\Http\\Response::write
=============================

Append HTTP body content to the HTTP response.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Response::write</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span> )

Append HTTP body content to the HTTP response.

### 参数

`content`  

### 返回值

简介
----

类摘要
------

**Swoole\\Http\\Server**

<span class="ooclass"> class **Swoole\\Http\\Server** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Swoole\\Server** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">on</span> ( <span class="methodparam"><span
class="type">string</span> `$event_name`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::addlistener</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::addProcess</span> ( <span
class="methodparam"><span class="type">swoole\_process</span>
`$process`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::after</span> ( <span
class="methodparam"><span class="type">int</span>
`$after_time_ms`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$param`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::bind</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::clearTimer</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

<span class="type">void</span> <span
class="methodname">swoole\_timer\_clear</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::close</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$reset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::confirm</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::connection\_info</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::connection\_list</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::defer</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::exist</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::finish</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::getClientInfo</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::getClientList</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Server::getLastError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Server::heartbeat</span> ( <span
class="methodparam"><span class="type">bool</span>
`$if_close_connection`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::listen</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::pause</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::protect</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$is_protected`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::reload</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::resume</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::send</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$reactor_id`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendfile</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendMessage</span> ( <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendto</span> ( <span
class="methodparam"><span class="type">string</span> `$ip`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">string</span> `$server_socket`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendwait</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::shutdown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::stats</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::stop</span> (\[ <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> \]
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Server::task</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dst_worker_id`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::taskwait</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$worker_id`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::taskWaitMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$tasks`</span> \[,
<span class="methodparam"><span class="type">double</span>
`$timeout_ms`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::tick</span> ( <span
class="methodparam"><span class="type">int</span> `$interval_ms`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

}

Swoole\\Http\\Server::on
========================

Bind callback function to HTTP server by event name.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Server::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

Bind callback function to HTTP server by event name.

### 参数

`event_name`  

`callback`  

### 返回值

Swoole\\Http\\Server::start
===========================

Start the swoole http server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Server::start</span> ( <span
class="methodparam">void</span> )

Start the swoole http server.

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Lock**

<span class="ooclass"> class **Swoole\\Lock** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock\_read</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">trylock\_read</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">trylock</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unlock</span> ( <span
class="methodparam">void</span> )

}

Swoole\\Lock::\_\_construct
===========================

Construct a memory lock.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Lock::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$type`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$file_lock_location`</span> \]\] )

Swoole lock is used for data synchronization between multiple theads or
processes.

### 参数

`type`  

`file_lock_location`  

Swoole\\Lock::\_\_destruct
==========================

Destory a Swoole memory lock.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Lock::\_\_destruct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Lock::lock\_read
========================

Lock a read-write lock for reading.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Lock::lock\_read</span> ( <span
class="methodparam">void</span> )

Lock a read-write lock for reading.

### 参数

此函数没有参数。

### 返回值

Swoole\\Lock::lock
==================

Try to acquire the lock. It will block if the lock is not available.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Lock::lock</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Lock::trylock\_read
===========================

Try to lock a read-write lock for reading and return straight away even
the lock is not available.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Lock::trylock\_read</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Lock::trylock
=====================

Try to acquire the lock and return straight away even the lock is not
available.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Lock::trylock</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Lock::unlock
====================

Release the lock.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Lock::unlock</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Mmap**

<span class="ooclass"> class **Swoole\\Mmap** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">string</span> `$size`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$offset`</span> \]\] )

}

Swoole\\Mmap::open
==================

Map a file into memory and return the stream resource which can be used
by PHP stream operations.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Mmap::open</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$size`</span> \[, <span class="methodparam"><span
class="type">string</span> `$offset`</span> \]\] )

### 参数

`filename`  

`size`  

`offset`  

### 返回值

简介
----

类摘要
------

**Swoole\\MySQL**

<span class="ooclass"> class **Swoole\\MySQL** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">connect</span> ( <span
class="methodparam"><span class="type">array</span>
`$server_config`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">getBuffer</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">on</span> ( <span class="methodparam"><span
class="type">string</span> `$event_name`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">query</span> (
<span class="methodparam"><span class="type">string</span> `$sql`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

}

Swoole\\MySQL::close
====================

Close the async MySQL connection.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\MySQL::close</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\MySQL::connect
======================

Connect to the remote MySQL server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\MySQL::connect</span> ( <span
class="methodparam"><span class="type">array</span>
`$server_config`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

Connect to the remote MySQL server.

### 参数

`server_config`  

`callback`  

### 返回值

Swoole\\MySQL::\_\_construct
============================

Construct an async MySQL client.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\MySQL::\_\_construct</span> ( <span
class="methodparam">void</span> )

Construct an async MySQL client.

### 参数

此函数没有参数。

Swoole\\MySQL::\_\_destruct
===========================

Destory the async MySQL client.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\MySQL::\_\_destruct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\MySQL::getBuffer
========================

Description

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\MySQL::getBuffer</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Swoole\\MySQL::on
=================

Register callback function based on event name.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\MySQL::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

Register callback function based on event name, current only 'close'
event is supported.

### 参数

`event_name`  

`callback`  

### 返回值

Swoole\\MySQL::query
====================

Run the SQL query.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\MySQL::query</span> ( <span
class="methodparam"><span class="type">string</span> `$sql`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`sql`  

`callback`  

### 返回值

简介
----

类摘要
------

**Swoole\\MySQL\\Exception**

<span class="ooclass"> class **Swoole\\MySQL\\Exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> <span class="oointerface">implements <span
class="interfacename">Throwable</span> </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

}

简介
----

类摘要
------

**Swoole\\Process**

<span class="ooclass"> class **Swoole\\Process** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Process::IPC_NOWAIT` <span class="initializer"> = 256</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">alarm</span> ( <span class="methodparam"><span
class="type">int</span> `$interval_usec`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">daemon</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$nochdir`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$noclose`</span>
\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_destruct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">exec</span> (
<span class="methodparam"><span class="type">string</span>
`$exec_file`</span> , <span class="methodparam"><span
class="type">string</span> `$args`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">exit</span> (\[ <span class="methodparam"><span
class="type">string</span> `$exit_code`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">freeQueue</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">kill</span> ( <span class="methodparam"><span
class="type">int</span> `$pid`</span> \[, <span
class="methodparam"><span class="type">string</span> `$signal_no`</span>
\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">name</span> ( <span class="methodparam"><span
class="type">string</span> `$process_name`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> (\[ <span class="methodparam"><span
class="type">int</span> `$maxsize`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">read</span> (\[ <span class="methodparam"><span
class="type">int</span> `$maxsize`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">signal</span> ( <span class="methodparam"><span
class="type">string</span> `$signal_no`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">statQueue</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">useQueue</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$mode`</span>
\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">wait</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$blocking`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">write</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

}

预定义常量
----------

**`Swoole\Process::IPC_NOWAIT`**  

Swoole\\Process::alarm
======================

High precision timer which triggers signal with fixed interval.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Process::alarm</span> ( <span
class="methodparam"><span class="type">int</span>
`$interval_usec`</span> )

### 参数

`interval_usec`  

### 返回值

Swoole\\Process::close
======================

Close the pipe to the child process.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Process::close</span> ( <span
class="methodparam">void</span> )

Close the pipe to the child process.

### 参数

此函数没有参数。

### 返回值

Swoole\\Process::\_\_construct
==============================

Construct a process.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Process::\_\_construct</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$redirect_stdin_and_stdout`</span> \[, <span
class="methodparam"><span class="type">int</span> `$pipe_type`</span>
\]\] )

### 参数

`callback`  

`redirect_stdin_and_stdout`  

`pipe_type`  

Swoole\\Process::daemon
=======================

Change the process to be a daemon process.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Process::daemon</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$nochdir`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$noclose`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`nochdir`  

`noclose`  

### 返回值

Swoole\\Process::\_\_destruct
=============================

Destory the process.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Process::\_\_destruct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Process::exec
=====================

Execute system commands.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Process::exec</span> ( <span
class="methodparam"><span class="type">string</span> `$exec_file`</span>
, <span class="methodparam"><span class="type">string</span>
`$args`</span> )

The process will be replaced to be the system command process, but the
pipe to the parent process will be kept.

### 参数

`exec_file`  

`args`  

### 返回值

Swoole\\Process::exit
=====================

Stop the child processes.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Process::exit</span> (\[ <span
class="methodparam"><span class="type">string</span> `$exit_code`</span>
\] )

### 参数

`exit_code`  

### 返回值

Swoole\\Process::freeQueue
==========================

Destroy the message queue created by swoole\_process::useQueue.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Process::freeQueue</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Process::kill
=====================

Send signal to the child process.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Process::kill</span> ( <span
class="methodparam"><span class="type">int</span> `$pid`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$signal_no`</span> \] )

Send signal to the child process.

### 参数

`pid`  

`signal_no`  

### 返回值

Swoole\\Process::name
=====================

Set name of the process.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Process::name</span> ( <span
class="methodparam"><span class="type">string</span>
`$process_name`</span> )

### 参数

`process_name`  

### 返回值

Swoole\\Process::pop
====================

Read and pop data from the message queue.

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Process::pop</span> (\[ <span
class="methodparam"><span class="type">int</span> `$maxsize`</span> \] )

### 参数

`maxsize`  

### 返回值

Swoole\\Process::push
=====================

Write and push data into the message queue.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Process::push</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 参数

`data`  

### 返回值

Swoole\\Process::read
=====================

Read data sending to the process.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Process::read</span> (\[ <span
class="methodparam"><span class="type">int</span> `$maxsize`</span> \] )

### 参数

`maxsize`  

### 返回值

Swoole\\Process::signal
=======================

Send signal to the child processes.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Process::signal</span> ( <span
class="methodparam"><span class="type">string</span> `$signal_no`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`signal_no`  

`callback`  

### 返回值

If signal sent successfully, it returns TRUE, otherwise it returns
FALSE.

Swoole\\Process::start
======================

Start the process.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Process::start</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Process::statQueue
==========================

Get the stats of the message queue used as the communication method
between processes.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Process::statQueue</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The array of status of the message queue.

Swoole\\Process::useQueue
=========================

Create a message queue as the communication method between the parent
process and child processes.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Process::useQueue</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$mode`</span>
\] )

### 参数

`key`  

`mode`  

### 返回值

Swoole\\Process::wait
=====================

Wait for the events of child processes.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Swoole\\Process::wait</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$blocking`</span> \]
)

### 参数

`blocking`  

### 返回值

Swoole\\Process::write
======================

Write data into the pipe and communicate with the parent process or
child processes.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Process::write</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 参数

`data`  

### 返回值

简介
----

类摘要
------

**Swoole\\Redis\\Server**

<span class="ooclass"> class **Swoole\\Redis\\Server** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Swoole\\Server** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::NIL` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::ERROR` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::STATUS` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::INT` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::STRING` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::SET` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Redis\Server::MAP` <span class="initializer"> = 6</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">format</span> ( <span class="methodparam"><span
class="type">string</span> `$type`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">setHandler</span> ( <span class="methodparam"><span
class="type">string</span> `$command`</span> , <span
class="methodparam"><span class="type">string</span> `$callback`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$number_of_string_param`</span> \[, <span class="methodparam"><span
class="type">string</span> `$type_of_array_param`</span> \]\] )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">start</span> (
<span class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::addlistener</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::addProcess</span> ( <span
class="methodparam"><span class="type">swoole\_process</span>
`$process`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::after</span> ( <span
class="methodparam"><span class="type">int</span>
`$after_time_ms`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$param`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::bind</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::clearTimer</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

<span class="type">void</span> <span
class="methodname">swoole\_timer\_clear</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::close</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$reset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::confirm</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::connection\_info</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::connection\_list</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::defer</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::exist</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::finish</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::getClientInfo</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::getClientList</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Server::getLastError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Server::heartbeat</span> ( <span
class="methodparam"><span class="type">bool</span>
`$if_close_connection`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::listen</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::pause</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::protect</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$is_protected`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::reload</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::resume</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::send</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$reactor_id`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendfile</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendMessage</span> ( <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendto</span> ( <span
class="methodparam"><span class="type">string</span> `$ip`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">string</span> `$server_socket`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendwait</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::shutdown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::stats</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::stop</span> (\[ <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> \]
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Server::task</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dst_worker_id`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::taskwait</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$worker_id`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::taskWaitMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$tasks`</span> \[,
<span class="methodparam"><span class="type">double</span>
`$timeout_ms`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::tick</span> ( <span
class="methodparam"><span class="type">int</span> `$interval_ms`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

}

预定义常量
----------

**`Swoole\Redis\Server::NIL`**  

**`Swoole\Redis\Server::ERROR`**  

**`Swoole\Redis\Server::STATUS`**  

**`Swoole\Redis\Server::INT`**  

**`Swoole\Redis\Server::STRING`**  

**`Swoole\Redis\Server::SET`**  

**`Swoole\Redis\Server::MAP`**  

Swoole\\Redis\\Server::format
=============================

Description

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Redis\\Server::format</span> ( <span
class="methodparam"><span class="type">string</span> `$type`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`type`  

`value`  

### 返回值

Swoole\\Redis\\Server::setHandler
=================================

Description

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Redis\\Server::setHandler</span> ( <span
class="methodparam"><span class="type">string</span> `$command`</span> ,
<span class="methodparam"><span class="type">string</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$number_of_string_param`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$type_of_array_param`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`command`  

`callback`  

`number_of_string_param`  

`type_of_array_param`  

### 返回值

Swoole\\Redis\\Server::start
============================

Description

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Redis\\Server::start</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Serialize**

<span class="ooclass"> class **Swoole\\Serialize** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">pack</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$is_fast`</span> \] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">unpack</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">string</span> `$args`</span> \] )

}

Swoole\\Serialize::pack
=======================

Serialize the data.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Serialize::pack</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$is_fast`</span> \] )

Swoole provides a fast and high performance serialization module.

### 参数

`data`  

`is_fast`  

### 返回值

Swoole\\Serialize::unpack
=========================

Unserialize the data.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">ReturnType</span>
<span class="methodname">Swoole\\Serialize::unpack</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$args`</span> \] )

Unserialize the data.

### 参数

`string`  

`args`  

### 返回值

简介
----

类摘要
------

**Swoole\\Server**

<span class="ooclass"> class **Swoole\\Server** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addlistener</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">addProcess</span> ( <span
class="methodparam"><span class="type">swoole\_process</span>
`$process`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">after</span> (
<span class="methodparam"><span class="type">int</span>
`$after_time_ms`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$param`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">bind</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> , <span class="methodparam"><span
class="type">int</span> `$uid`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clearTimer</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

<span class="type">void</span> <span
class="methodname">swoole\_timer\_clear</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$reset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">confirm</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">connection\_info</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">connection\_list</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">defer</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exist</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">finish</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">getClientInfo</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getClientList</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLastError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">heartbeat</span> ( <span
class="methodparam"><span class="type">bool</span>
`$if_close_connection`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">listen</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">on</span> ( <span class="methodparam"><span
class="type">string</span> `$event_name`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pause</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">protect</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$is_protected`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">reload</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resume</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">send</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendfile</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendMessage</span> ( <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendto</span> ( <span class="methodparam"><span
class="type">string</span> `$ip`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$server_socket`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">sendwait</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">set</span> (
<span class="methodparam"><span class="type">array</span>
`$settings`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">shutdown</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">start</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">stats</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">stop</span> (\[ <span class="methodparam"><span
class="type">int</span> `$worker_id`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">task</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span>
`$dst_worker_id`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">taskwait</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$worker_id`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">taskWaitMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$tasks`</span> \[,
<span class="methodparam"><span class="type">double</span>
`$timeout_ms`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">tick</span> ( <span class="methodparam"><span
class="type">int</span> `$interval_ms`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

}

Swoole\\Server::addlistener
===========================

Add a new listener to the server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::addlistener</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

### 参数

`host`  

`port`  

`socket_type`  

### 返回值

Swoole\\Server::addProcess
==========================

Add a user defined swoole\_process to the server.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::addProcess</span> ( <span
class="methodparam"><span class="type">swoole\_process</span>
`$process`</span> )

### 参数

`process`  

### 返回值

Swoole\\Server::after
=====================

Trigger a callback function after a period of time.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::after</span> ( <span
class="methodparam"><span class="type">int</span>
`$after_time_ms`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">string</span> `$param`</span> \]
)

### 参数

`after_time_ms`  

`callback`  

`param`  

### 返回值

Swoole\\Server::bind
====================

Bind the connection to a user defined user ID.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::bind</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

### 参数

`fd`  

`uid`  

### 返回值

Swoole\\Server::clearTimer
==========================

swoole\_timer\_clear
====================

Stop and destory a timer.

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::clearTimer</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">swoole\_timer\_clear</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

Stop and destory a timer

### 参数

`timer_id`  

### 返回值

Swoole\\Server::close
=====================

Close a connection to the client.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::close</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$reset`</span> \] )

### 参数

`fd`  

`reset`  

### 返回值

Swoole\\Server::confirm
=======================

Check status of the connection.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::confirm</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

Swoole\\Server::connection\_info
================================

Get the connection info by file description.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::connection\_info</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

### 参数

`fd`  

`reactor_id`  

### 返回值

Swoole\\Server::connection\_list
================================

Get all of the established connections.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::connection\_list</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

### 参数

`start_fd`  

`pagesize`  

### 返回值

Swoole\\Server::\_\_construct
=============================

Construct a Swoole server.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Server::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`</span>
\[, <span class="methodparam"><span class="type">integr</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sock_type`</span> \]\]\] )

### 参数

`host`  

`port`  

`mode`  

`sock_type`  

Swoole\\Server::defer
=====================

Delay execution of the callback function at the end of current
EventLoop.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::defer</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`callback`  

### 返回值

Swoole\\Server::exist
=====================

Check if the connection is existed.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::exist</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

Swoole\\Server::finish
======================

Used in task process for sending result to the worker process when the
task is finished.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::finish</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 参数

`data`  

### 返回值

Swoole\\Server::getClientInfo
=============================

Get the connection info by file description.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::getClientInfo</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$reactor_id`</span>
\] )

### 参数

`fd`  

`reactor_id`  

### 返回值

Swoole\\Server::getClientList
=============================

Get all of the established connections.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::getClientList</span> ( <span
class="methodparam"><span class="type">int</span> `$start_fd`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$pagesize`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`start_fd`  

`pagesize`  

### 返回值

Swoole\\Server::getLastError
============================

Get the error code of the most recent error.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Server::getLastError</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Server::heartbeat
=========================

Check all the connections on the server.

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Server::heartbeat</span> ( <span
class="methodparam"><span class="type">bool</span>
`$if_close_connection`</span> )

### 参数

`if_close_connection`  

### 返回值

Swoole\\Server::listen
======================

Listen on the given IP and port, socket type.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::listen</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$socket_type`</span> )

### 参数

`host`  

`port`  

`socket_type`  

### 返回值

Swoole\\Server::on
==================

Register a callback function by event name.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

### 参数

`event_name`  

`callback`  

### 返回值

Swoole\\Server::pause
=====================

Stop receiving data from the connection.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::pause</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

Swoole\\Server::protect
=======================

Set the connection to be protected mode.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::protect</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$is_protected`</span> \] )

### 参数

`fd`  

`is_protected`  

### 返回值

Swoole\\Server::reload
======================

Restart all the worker process.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::reload</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Server::resume
======================

Start receving data from the connection.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::resume</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

Swoole\\Server::send
====================

Send data to the client.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::send</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$reactor_id`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`fd`  

`data`  

`reactor_id`  

### 返回值

Swoole\\Server::sendfile
========================

Send file to the connection.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendfile</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$offset`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`fd`  

`filename`  

`offset`  

### 返回值

Swoole\\Server::sendMessage
===========================

Send message to worker processes by ID.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendMessage</span> ( <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> )

### 参数

`dst_worker_id`  

`data`  

### 返回值

Swoole\\Server::sendto
======================

Send data to the remote UDP address.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendto</span> ( <span
class="methodparam"><span class="type">string</span> `$ip`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">string</span> `$server_socket`</span> \] )

### 参数

`ip`  

`port`  

`data`  

`server_socket`  

### 返回值

Swoole\\Server::sendwait
========================

Send data to the remote socket in the blocking way.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::sendwait</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`fd`  

`data`  

### 返回值

Swoole\\Server::set
===================

Set the runtime settings of the swoole server.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Server::set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

Set the runtime settings of the swoole server. The settings can be
accessed by $server-\>setting when the swoole server has started.

### 参数

`settings`  

### 返回值

Swoole\\Server::shutdown
========================

Shutdown the master server process, this function can be called in
worker processes.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::shutdown</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Server::start
=====================

Start the Swoole server.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::start</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Server::stats
=====================

Get the stats of the Swoole server.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Server::stats</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Server::stop
====================

Stop the Swoole server.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Server::stop</span> (\[ <span
class="methodparam"><span class="type">int</span> `$worker_id`</span> \]
)

### 参数

`worker_id`  

### 返回值

Swoole\\Server::task
====================

Send data to the task worker processes.

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Swoole\\Server::task</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dst_worker_id`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`data`  

`dst_worker_id`  

`callback`  

### 返回值

Swoole\\Server::taskwait
========================

Send data to the task worker processes in blocking way.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::taskwait</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$worker_id`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`data`  

`timeout`  

`worker_id`  

### 返回值

Swoole\\Server::taskWaitMulti
=============================

Execute multiple tasks concurrently.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::taskWaitMulti</span> ( <span
class="methodparam"><span class="type">array</span> `$tasks`</span> \[,
<span class="methodparam"><span class="type">double</span>
`$timeout_ms`</span> \] )

### 参数

`tasks`  

`timeout_ms`  

### 返回值

Swoole\\Server::tick
====================

Repeats a given function at every given time-interval.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Server::tick</span> ( <span
class="methodparam"><span class="type">int</span> `$interval_ms`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`interval_ms`  

`callback`  

### 返回值

简介
----

类摘要
------

**Swoole\\Table**

<span class="ooclass"> class **Swoole\\Table** </span> <span
class="oointerface">implements <span
class="interfacename">Iterator</span> </span> <span
class="oointerface">, <span class="interfacename">Countable</span>
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Table::TYPE_INT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Table::TYPE_STRING` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`Swoole\Table::TYPE_FLOAT` <span class="initializer"> = 6</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">column</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$type`</span> \[, <span
class="methodparam"><span class="type">int</span> `$size`</span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">create</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">current</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">decr</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$column`</span> \[, <span class="methodparam"><span
class="type">int</span> `$decrby`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">del</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">destroy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exist</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">string</span> `$row_key`</span> , <span
class="methodparam"><span class="type">string</span>
`$column_key`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">incr</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$column`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$incrby`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">key</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">next</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">VOID</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">array</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">valid</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`Swoole\Table::TYPE_INT`**  

**`Swoole\Table::TYPE_STRING`**  

**`Swoole\Table::TYPE_FLOAT`**  

Swoole\\Table::column
=====================

Set the data type and size of the columns.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Table::column</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$type`</span> \[, <span class="methodparam"><span
class="type">int</span> `$size`</span> \] )

### 参数

`name`  

`type`  

`size`  

### 返回值

Swoole\\Table::\_\_construct
============================

Construct a Swoole memory table with fixed size.

### 说明

<span class="modifier">public</span> <span
class="methodname">Swoole\\Table::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$table_size`</span> )

### 参数

`table_size`  

Swoole\\Table::count
====================

Count the rows in the table, or count all the elements in the table if
$mode = 1.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Table::count</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::create
=====================

Create the swoole memory table.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Table::create</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::current
======================

Get the current row.

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Swoole\\Table::current</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::decr
===================

Decrement the value in the Swoole table by $row\_key and $column\_key.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Table::decr</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column`</span> \[, <span class="methodparam"><span
class="type">int</span> `$decrby`</span> \] )

### 参数

`key`  

`column`  

`decrby`  

### 返回值

Swoole\\Table::del
==================

Delete a row in the Swoole table by $row\_key.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Table::del</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

### 参数

`key`  

### 返回值

Swoole\\Table::destroy
======================

Destroy the Swoole table.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Table::destroy</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::exist
====================

Check if a row is existed by $row\_key.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Table::exist</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

### 参数

`key`  

### 返回值

Swoole\\Table::get
==================

Get the value in the Swoole table by $row\_key and $column\_key.

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Swoole\\Table::get</span> ( <span
class="methodparam"><span class="type">string</span> `$row_key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column_key`</span> )

### 参数

`row_key`  

`column_key`  

### 返回值

Swoole\\Table::incr
===================

Increment the value by $row\_key and $column\_key.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Table::incr</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$column`</span> \[, <span class="methodparam"><span
class="type">int</span> `$incrby`</span> \] )

### 参数

`key`  

`column`  

`incrby`  

### 返回值

Swoole\\Table::key
==================

Get the key of current row.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Swoole\\Table::key</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::next
===================

Iterator the next row.

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\Table::next</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::rewind
=====================

Rewind the iterator.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Table::rewind</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Swoole\\Table::set
==================

Update a row of the table by $row\_key.

### 说明

<span class="modifier">public</span> <span class="type">VOID</span>
<span class="methodname">Swoole\\Table::set</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">array</span>
`$value`</span> )

### 参数

`key`  

`value`  

### 返回值

Swoole\\Table::valid
====================

Check current if the current row is valid.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\Table::valid</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

简介
----

类摘要
------

**Swoole\\Timer**

<span class="ooclass"> class **Swoole\\Timer** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">after</span> ( <span class="methodparam"><span
class="type">int</span> `$after_time_ms`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">clear</span> ( <span class="methodparam"><span
class="type">int</span> `$timer_id`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">exists</span> ( <span class="methodparam"><span
class="type">int</span> `$timer_id`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">tick</span> ( <span class="methodparam"><span
class="type">int</span> `$interval_ms`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$param`</span> \] )

}

Swoole\\Timer::after
====================

Trigger a callback function after a period of time.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Timer::after</span> ( <span
class="methodparam"><span class="type">int</span>
`$after_time_ms`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

Trigger a callback function after a period of time.

### 参数

`after_time_ms`  

`callback`  

### 返回值

Swoole\\Timer::clear
====================

Delete a timer by timer ID.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Timer::clear</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

Delete a timer by timer ID.

### 参数

`timer_id`  

### 返回值

Swoole\\Timer::exists
=====================

Check if a timer is existed.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Swoole\\Timer::exists</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

Check if a timer is existed.

### 参数

`timer_id`  

### 返回值

Swoole\\Timer::tick
===================

Repeats a given function at every given time-interval.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">Swoole\\Timer::tick</span> ( <span
class="methodparam"><span class="type">int</span> `$interval_ms`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">string</span> `$param`</span> \] )

### 参数

`interval_ms`  

`callback`  

`param`  

### 返回值

简介
----

类摘要
------

**Swoole\\WebSocket\\Frame**

<span class="ooclass"> class **Swoole\\WebSocket\\Frame** </span> {

/\* 方法 \*/

}

简介
----

类摘要
------

**Swoole\\WebSocket\\Server**

<span class="ooclass"> class **Swoole\\WebSocket\\Server** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**Swoole\\Http\\Server** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">exist</span> ( <span class="methodparam"><span
class="type">int</span> `$fd`</span> )

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span class="methodname">on</span> (
<span class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">binary</span> <span
class="methodname">pack</span> ( <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">string</span> `$opcode`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$finish`</span> \[, <span class="methodparam"><span
class="type">string</span> `$mask`</span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">string</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$opcode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$finish`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">unpack</span> ( <span class="methodparam"><span
class="type">binary</span> `$data`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Server::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\Http\\Server::start</span> ( <span
class="methodparam">void</span> )

}

Swoole\\WebSocket\\Server::exist
================================

Check if the file descriptor exists.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Swoole\\WebSocket\\Server::exist</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

Swoole\\WebSocket\\Server::on
=============================

Register event callback function

### 说明

<span class="modifier">public</span> <span
class="type">ReturnType</span> <span
class="methodname">Swoole\\WebSocket\\Server::on</span> ( <span
class="methodparam"><span class="type">string</span>
`$event_name`</span> , <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

Register event callback function

### 参数

`event_name`  

`callback`  

### 返回值

Swoole\\WebSocket\\Server::pack
===============================

Get a pack of binary data to send in a single frame.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">binary</span> <span
class="methodname">Swoole\\WebSocket\\Server::pack</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$opcode`</span> \[, <span class="methodparam"><span
class="type">string</span> `$finish`</span> \[, <span
class="methodparam"><span class="type">string</span> `$mask`</span>
\]\]\] )

### 参数

`data`  

`opcode`  

`finish`  

`mask`  

### 返回值

Swoole\\WebSocket\\Server::push
===============================

Push data to the remote client.

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Swoole\\WebSocket\\Server::push</span> ( <span
class="methodparam"><span class="type">string</span> `$fd`</span> ,
<span class="methodparam"><span class="type">string</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">string</span> `$opcode`</span> \[, <span
class="methodparam"><span class="type">string</span> `$finish`</span>
\]\] )

### 参数

`fd`  

`data`  

`opcode`  

`finish`  

### 返回值

Swoole\\WebSocket\\Server::unpack
=================================

Unpack the binary data received from the client.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Swoole\\WebSocket\\Server::unpack</span> ( <span
class="methodparam"><span class="type">binary</span> `$data`</span> )

### 参数

`data`  

### 返回值
