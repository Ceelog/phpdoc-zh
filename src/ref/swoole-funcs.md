swoole\_async\_dns\_lookup
==========================

Async and non-blocking hostname to IP lookup

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_async\_dns\_lookup</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

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

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_async\_read
===================

Read file stream asynchronously

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_async\_read</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$chunk_size`<span class="initializer"> =
65536</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \]\] )

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
The content readed from the file stream.

`chunk_size`  
The chunk length.

`offset`  
The offset.

### 返回值

Whether the read is succeed.

swoole\_async\_readfile
=======================

Read a file asynchronously

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_async\_readfile</span> ( <span
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

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_async\_set
==================

Update the async I/O options

### 说明

<span class="type">void</span> <span
class="methodname">swoole\_async\_set</span> ( <span
class="methodparam"><span class="type">array</span> `$settings`</span> )

### 参数

`settings`  

swoole\_async\_write
====================

Write data to a file stream asynchronously

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_async\_write</span> ( <span
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

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_async\_writefile
========================

Write data to a file asynchronously

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_async\_writefile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$content`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

### 参数

`filename`  
The filename being written.

`content`  
The content writing to the file.

`callback`  

`flags`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_client\_select
======================

Get the file description which are ready to read/write or error

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_client\_select</span> ( <span
class="methodparam"><span class="type">array</span>
`&$read_array`</span> , <span class="methodparam"><span
class="type">array</span> `&$write_array`</span> , <span
class="methodparam"><span class="type">array</span>
`&$error_array`</span> \[, <span class="methodparam"><span
class="type">float</span> `$timeout`<span class="initializer"> =
0.5</span></span> \] )

### 参数

`read_array`  

`write_array`  

`error_array`  

`timeout`  

### 返回值

swoole\_cpu\_num
================

Get the number of CPU

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_cpu\_num</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The number of CPU.

swoole\_errno
=============

Get the error code of the latest system call

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_errno</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

swoole\_event\_add
==================

Add new callback functions of a socket into the EventLoop

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_event\_add</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$read_callback`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$write_callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$events`<span
class="initializer"> = 0</span></span> \]\]\] )

### 参数

`fd`  

`read_callback`  

`write_callback`  

`events`  

### 返回值

swoole\_event\_defer
====================

Add callback function to the next event loop

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_event\_defer</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

### 参数

`callback`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_event\_del
==================

Remove all event callback functions of a socket

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_event\_del</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

### 参数

`fd`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_event\_exit
===================

Exit the eventloop, only available at the client side

### 说明

<span class="type">void</span> <span
class="methodname">swoole\_event\_exit</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

swoole\_event\_set
==================

Update the event callback functions of a socket

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_event\_set</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$read_callback`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$write_callback`</span> \[, <span
class="methodparam"><span class="type">int</span> `$events`<span
class="initializer"> = 0</span></span> \]\]\] )

### 参数

`fd`  

`read_callback`  

`write_callback`  

`events`  

### 返回值

swoole\_event\_wait
===================

Start the event loop

### 说明

<span class="type">void</span> <span
class="methodname">swoole\_event\_wait</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

swoole\_event\_write
====================

Write data to a socket

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_event\_write</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> )

### 参数

`fd`  

`data`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

swoole\_get\_local\_ip
======================

Get the IPv4 IP addresses of each NIC on the machine

### 说明

<span class="type">array</span> <span
class="methodname">swoole\_get\_local\_ip</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

swoole\_last\_error
===================

Get the lastest error message

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_last\_error</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

swoole\_load\_module
====================

Load a swoole extension

### 说明

<span class="type">mixed</span> <span
class="methodname">swoole\_load\_module</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

### 参数

此函数没有参数。

### 返回值

swoole\_select
==============

Select the file descriptions which are ready to read/write or error in
the eventloop

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_select</span> ( <span
class="methodparam"><span class="type">array</span>
`&$read_array`</span> , <span class="methodparam"><span
class="type">array</span> `&$write_array`</span> , <span
class="methodparam"><span class="type">array</span>
`&$error_array`</span> \[, <span class="methodparam"><span
class="type">float</span> `$timeout`</span> \] )

### 参数

`read_array`  

`write_array`  

`error_array`  

`timeout`  

### 返回值

swoole\_set\_process\_name
==========================

Set the process name

### 说明

<span class="type">void</span> <span
class="methodname">swoole\_set\_process\_name</span> ( <span
class="methodparam"><span class="type">string</span>
`$process_name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$size`<span class="initializer"> =
128</span></span> \] )

### 参数

`process_name`  

### 返回值

swoole\_strerror
================

Convert the Errno into error messages

### 说明

<span class="type">string</span> <span
class="methodname">swoole\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errno`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$error_type`<span class="initializer"> = 0</span></span> \] )

### 参数

`errno`  

### 返回值

swoole\_timer\_after
====================

Trigger a one time callback function in the future

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_timer\_after</span> ( <span
class="methodparam"><span class="type">int</span> `$ms`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$param`</span> \] )

### 参数

`ms`  

`callback`  

`param`  

### 返回值

swoole\_timer\_exists
=====================

Check if a timer callback function is existed

### 说明

<span class="type">bool</span> <span
class="methodname">swoole\_timer\_exists</span> ( <span
class="methodparam"><span class="type">int</span> `$timer_id`</span> )

### 参数

`timer_id`  

### 返回值

swoole\_timer\_tick
===================

Trigger a timer tick callback function by time interval

### 说明

<span class="type">int</span> <span
class="methodname">swoole\_timer\_tick</span> ( <span
class="methodparam"><span class="type">int</span> `$ms`</span> , <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$param`</span> \] )

### 参数

`ms`  

`callback`  

### 返回值

swoole\_version
===============

Get the version of Swoole

### 说明

<span class="type">string</span> <span
class="methodname">swoole\_version</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

The version of Swoole.

**目录**

-   [swoole\_async\_dns\_lookup](/ref/swoole-funcs.html#swoole_async_dns_lookup)
    — Async and non-blocking hostname to IP lookup
-   [swoole\_async\_read](/ref/swoole-funcs.html#swoole_async_read) —
    Read file stream asynchronously
-   [swoole\_async\_readfile](/ref/swoole-funcs.html#swoole_async_readfile)
    — Read a file asynchronously
-   [swoole\_async\_set](/ref/swoole-funcs.html#swoole_async_set) —
    Update the async I/O options
-   [swoole\_async\_write](/ref/swoole-funcs.html#swoole_async_write) —
    Write data to a file stream asynchronously
-   [swoole\_async\_writefile](/ref/swoole-funcs.html#swoole_async_writefile)
    — Write data to a file asynchronously
-   [swoole\_client\_select](/ref/swoole-funcs.html#swoole_client_select)
    — Get the file description which are ready to read/write or error
-   [swoole\_cpu\_num](/ref/swoole-funcs.html#swoole_cpu_num) — Get the
    number of CPU
-   [swoole\_errno](/ref/swoole-funcs.html#swoole_errno) — Get the error
    code of the latest system call
-   [swoole\_event\_add](/ref/swoole-funcs.html#swoole_event_add) — Add
    new callback functions of a socket into the EventLoop
-   [swoole\_event\_defer](/ref/swoole-funcs.html#swoole_event_defer) —
    Add callback function to the next event loop
-   [swoole\_event\_del](/ref/swoole-funcs.html#swoole_event_del) —
    Remove all event callback functions of a socket
-   [swoole\_event\_exit](/ref/swoole-funcs.html#swoole_event_exit) —
    Exit the eventloop, only available at the client side
-   [swoole\_event\_set](/ref/swoole-funcs.html#swoole_event_set) —
    Update the event callback functions of a socket
-   [swoole\_event\_wait](/ref/swoole-funcs.html#swoole_event_wait) —
    Start the event loop
-   [swoole\_event\_write](/ref/swoole-funcs.html#swoole_event_write) —
    Write data to a socket
-   [swoole\_get\_local\_ip](/ref/swoole-funcs.html#swoole_get_local_ip)
    — Get the IPv4 IP addresses of each NIC on the machine
-   [swoole\_last\_error](/ref/swoole-funcs.html#swoole_last_error) —
    Get the lastest error message
-   [swoole\_load\_module](/ref/swoole-funcs.html#swoole_load_module) —
    Load a swoole extension
-   [swoole\_select](/ref/swoole-funcs.html#swoole_select) — Select the
    file descriptions which are ready to read/write or error in the
    eventloop
-   [swoole\_set\_process\_name](/ref/swoole-funcs.html#swoole_set_process_name)
    — Set the process name
-   [swoole\_strerror](/ref/swoole-funcs.html#swoole_strerror) — Convert
    the Errno into error messages
-   [swoole\_timer\_after](/ref/swoole-funcs.html#swoole_timer_after) —
    Trigger a one time callback function in the future
-   [swoole\_timer\_exists](/ref/swoole-funcs.html#swoole_timer_exists)
    — Check if a timer callback function is existed
-   [swoole\_timer\_tick](/ref/swoole-funcs.html#swoole_timer_tick) —
    Trigger a timer tick callback function by time interval
-   [swoole\_version](/ref/swoole-funcs.html#swoole_version) — Get the
    version of Swoole
