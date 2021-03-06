ftok
====

Convert a pathname and a project identifier to a System V IPC key

### 说明

<span class="type">int</span> <span class="methodname">ftok</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$project_id`</span> )

The function converts the `filename` of an existing accessible file and
a project identifier into an *integer* for use with for example <span
class="function">shmop\_open</span> and other System V IPC keys.

### 参数

`filename`  
Path to an accessible file.

`project_id`  
Project identifier. This must be a one character string.

### 返回值

On success the return value will be the created key value, otherwise
*-1* is returned.

### 参见

-   <span class="function">shmop\_open</span>
-   <span class="function">sem\_get</span>

msg\_get\_queue
===============

Create or attach to a message queue

### 说明

<span class="type"><span class="type">SysvMessageQueue</span><span
class="type">false</span></span> <span
class="methodname">msg\_get\_queue</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$permissions`<span class="initializer"> = 0666</span></span> \] )

<span class="function">msg\_get\_queue</span> returns an id that can be
used to access the System V message queue with the given `key`. The
first call creates the message queue with the optional `permissions`. A
second call to <span class="function">msg\_get\_queue</span> for the
same `key` will return a different message queue identifier, but both
identifiers access the same underlying message queue.

### 参数

`key`  
Message queue numeric ID

`permissions`  
Queue permissions. Default to 0666. If the message queue already exists,
the `permissions` will be ignored.

### 返回值

Returns <span class="classname">SysvMessageQueue</span> instance that
can be used to access the System V message queue, 或者在失败时返回
**`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                             |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | On success, this function returns a <span class="classname">SysvMessageQueue</span> instance now; previously, a <span class="type">resource</span> was returned. |

### 参见

-   <span class="function">msg\_remove\_queue</span>
-   <span class="function">msg\_receive</span>
-   <span class="function">msg\_send</span>
-   <span class="function">msg\_stat\_queue</span>
-   <span class="function">msg\_set\_queue</span>

msg\_queue\_exists
==================

Check whether a message queue exists

### 说明

<span class="type">bool</span> <span
class="methodname">msg\_queue\_exists</span> ( <span
class="methodparam"><span class="type">int</span> `$key`</span> )

Checks whether the message queue `key` exists.

### 参数

`key`  
Queue key.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">msg\_remove\_queue</span>
-   <span class="function">msg\_receive</span>
-   <span class="function">msg\_stat\_queue</span>

msg\_receive
============

Receive a message from a message queue

### 说明

<span class="type">bool</span> <span
class="methodname">msg\_receive</span> ( <span class="methodparam"><span
class="type">SysvMessageQueue</span> `$queue`</span> , <span
class="methodparam"><span class="type">int</span>
`$desired_message_type`</span> , <span class="methodparam"><span
class="type">int</span> `&$received_message_type`</span> , <span
class="methodparam"><span class="type">int</span>
`$max_message_size`</span> , <span class="methodparam"><span
class="type">mixed</span> `&$message`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$unserialize`<span
class="initializer"> = **`true`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$error_code`<span
class="initializer"> = **`null`**</span></span> \]\]\] )

<span class="function">msg\_receive</span> will receive the first
message from the specified `queue` of the type specified by
`desired_message_type`.

### 参数

`queue`  
The message queue.

`desired_message_type`  
If `desired_message_type` is 0, the message from the front of the queue
is returned. If `desired_message_type` is greater than 0, then the first
message of that type is returned. If `desired_message_type` is less than
0, the first message on the queue with a type less than or equal to the
absolute value of `desired_message_type` will be read. If no messages
match the criteria, your script will wait until a suitable message
arrives on the queue. You can prevent the script from blocking by
specifying **`MSG_IPC_NOWAIT`** in the `flags` parameter.

`received_message_type`  
The type of the message that was received will be stored in this
parameter.

`max_message_size`  
The maximum size of message to be accepted is specified by the
`max_message_size`; if the message in the queue is larger than this size
the function will fail (unless you set `flags` as described below).

`message`  
The received message will be stored in `message`, unless there were
errors receiving the message.

`unserialize`  
If set to **`true`**, the message is treated as though it was serialized
using the same mechanism as the session module. The message will be
unserialized and then returned to your script. This allows you to easily
receive arrays or complex object structures from other PHP scripts, or
if you are using the WDDX serializer, from any WDDX compatible source.

If `unserialize` is **`false`**, the message will be returned as a
binary-safe string.

`flags`  
The optional `flags` allows you to pass flags to the low-level msgrcv
system call. It defaults to 0, but you may specify one or more of the
following values (by adding or ORing them together).

|                      |                                                                                                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`MSG_IPC_NOWAIT`** | If there are no messages of the `desired_message_type`, return immediately and do not wait. The function will fail and return an integer value corresponding to **`MSG_ENOMSG`**. |
| **`MSG_EXCEPT`**     | Using this flag in combination with a `desired_message_type` greater than 0 will cause the function to receive the first message that is not equal to `desired_message_type`.     |
| **`MSG_NOERROR`**    | If the message is longer than `max_message_size`, setting this flag will truncate the message to `max_message_size` and will not signal an error.                                 |

`error_code`  
If the function fails, the optional `error_code` will be set to the
value of the system errno variable.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

Upon successful completion the message queue data structure is updated
as follows: *msg\_lrpid* is set to the process-ID of the calling
process, *msg\_qnum* is decremented by 1 and *msg\_rtime* is set to the
current time.

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `queue` expects a <span class="classname">SysvMessageQueue</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">msg\_remove\_queue</span>
-   <span class="function">msg\_send</span>
-   <span class="function">msg\_stat\_queue</span>
-   <span class="function">msg\_set\_queue</span>

msg\_remove\_queue
==================

Destroy a message queue

### 说明

<span class="type">bool</span> <span
class="methodname">msg\_remove\_queue</span> ( <span
class="methodparam"><span class="type">SysvMessageQueue</span>
`$queue`</span> )

<span class="function">msg\_remove\_queue</span> destroys the message
queue specified by the `queue`. Only use this function when all
processes have finished working with the message queue and you need to
release the system resources held by it.

### 参数

`queue`  
The message queue.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `queue` expects a <span class="classname">SysvMessageQueue</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">msg\_get\_queue</span>
-   <span class="function">msg\_receive</span>
-   <span class="function">msg\_stat\_queue</span>
-   <span class="function">msg\_set\_queue</span>

msg\_send
=========

Send a message to a message queue

### 说明

<span class="type">bool</span> <span class="methodname">msg\_send</span>
( <span class="methodparam"><span class="type">SysvMessageQueue</span>
`$queue`</span> , <span class="methodparam"><span
class="type">int</span> `$message_type`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">int</span><span
class="type">float</span><span class="type">bool</span></span>
`$message`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$serialize`<span class="initializer"> =
**`true`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$blocking`<span class="initializer"> =
**`true`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `&$error_code`<span class="initializer"> =
**`null`**</span></span> \]\]\] )

<span class="function">msg\_send</span> sends a `message` of type
`message_type` (which MUST be greater than 0) to the message queue
specified by `queue`.

### 参数

`queue`  
The message queue.

`message_type`  
The type of the message (MUST be greater than 0)

`message`  
The body of the message.

> **Note**:
>
> If `serialize` set to **`false`** is supplied, MUST be of type: <span
> class="type">string</span>, <span class="type">int</span>, <span
> class="type">float</span> or <span class="type">bool</span>. In other
> case a warning will be issued.

`serialize`  
The optional `serialize` controls how the `message` is sent. `serialize`
defaults to **`true`** which means that the `message` is serialized
using the same mechanism as the session module before being sent to the
queue. This allows complex arrays and objects to be sent to other PHP
scripts, or if you are using the WDDX serializer, to any WDDX compatible
client.

`blocking`  
If the message is too large to fit in the queue, your script will wait
until another process reads messages from the queue and frees enough
space for your message to be sent. This is called blocking; you can
prevent blocking by setting the optional `blocking` parameter to
**`false`**, in which case <span class="function">msg\_send</span> will
immediately return **`false`** if the message is too big for the queue,
and set the optional `error_code` to **`MSG_EAGAIN`**, indicating that
you should try to send your message again a little later on.

`error_code`  
If the function fails, the optional errorcode will be set to the value
of the system errno variable.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

Upon successful completion the message queue data structure is updated
as follows: `msg_lspid` is set to the process-ID of the calling process,
`msg_qnum` is incremented by 1 and `msg_stime` is set to the current
time.

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `queue` expects a <span class="classname">SysvMessageQueue</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">msg\_remove\_queue</span>
-   <span class="function">msg\_receive</span>
-   <span class="function">msg\_stat\_queue</span>
-   <span class="function">msg\_set\_queue</span>

msg\_set\_queue
===============

Set information in the message queue data structure

### 说明

<span class="type">bool</span> <span
class="methodname">msg\_set\_queue</span> ( <span
class="methodparam"><span class="type">SysvMessageQueue</span>
`$queue`</span> , <span class="methodparam"><span
class="type">array</span> `$data`</span> )

<span class="function">msg\_set\_queue</span> allows you to change the
values of the msg\_perm.uid, msg\_perm.gid, msg\_perm.mode and
msg\_qbytes fields of the underlying message queue data structure.

Changing the data structure will require that PHP be running as the same
user that created the queue, owns the queue (as determined by the
existing msg\_perm.xxx fields), or be running with root privileges. root
privileges are required to raise the msg\_qbytes values above the system
defined limit.

### 参数

`queue`  
The message queue.

`data`  
You specify the values you require by setting the value of the keys that
you require in the `data` array.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `queue` expects a <span class="classname">SysvMessageQueue</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">msg\_remove\_queue</span>
-   <span class="function">msg\_receive</span>
-   <span class="function">msg\_stat\_queue</span>
-   <span class="function">msg\_get\_queue</span>

msg\_stat\_queue
================

Returns information from the message queue data structure

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">msg\_stat\_queue</span> ( <span
class="methodparam"><span class="type">SysvMessageQueue</span>
`$queue`</span> )

<span class="function">msg\_stat\_queue</span> returns the message queue
meta data for the message queue specified by the `queue`. This is
useful, for example, to determine which process sent the message that
was just received.

### 参数

`queue`  
The message queue.

### 返回值

On success, the return value is an array whose keys and values have the
following meanings:

|                  |                                                                                                                                        |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| *msg\_perm.uid*  | The uid of the owner of the queue.                                                                                                     |
| *msg\_perm.gid*  | The gid of the owner of the queue.                                                                                                     |
| *msg\_perm.mode* | The file access mode of the queue.                                                                                                     |
| *msg\_stime*     | The time that the last message was sent to the queue.                                                                                  |
| *msg\_rtime*     | The time that the last message was received from the queue.                                                                            |
| *msg\_ctime*     | The time that the queue was last changed.                                                                                              |
| *msg\_qnum*      | The number of messages waiting to be read from the queue.                                                                              |
| *msg\_qbytes*    | The maximum number of bytes allowed in one message queue. On Linux, this value may be read and modified via `/proc/sys/kernel/msgmnb`. |
| *msg\_lspid*     | The pid of the process that sent the last message to the queue.                                                                        |
| *msg\_lrpid*     | The pid of the process that received the last message from the queue.                                                                  |

Returns **`false`** on failure.

### 更新日志

| 版本  | 说明                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `queue` expects a <span class="classname">SysvMessageQueue</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">msg\_remove\_queue</span>
-   <span class="function">msg\_receive</span>
-   <span class="function">msg\_get\_queue</span>
-   <span class="function">msg\_set\_queue</span>

sem\_acquire
============

Acquire a semaphore

### 说明

<span class="type">bool</span> <span
class="methodname">sem\_acquire</span> ( <span class="methodparam"><span
class="type">SysvSemaphore</span> `$semaphore`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$non_blocking`<span
class="initializer"> = **`false`**</span></span> \] )

<span class="function">sem\_acquire</span> by default blocks (if
necessary) until the semaphore can be acquired. A process attempting to
acquire a semaphore which it has already acquired will block forever if
acquiring the semaphore would cause its maximum number of semaphore to
be exceeded.

After processing a request, any semaphores acquired by the process but
not explicitly released will be released automatically and a warning
will be generated.

### 参数

`semaphore`  
`semaphore` is a semaphore obtained from <span
class="function">sem\_get</span>.

`non_blocking`  
Specifies if the process shouldn't wait for the semaphore to be
acquired. If set to *true*, the call will return *false* immediately if
a semaphore cannot be immediately acquired.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `semaphore` expects a <span class="classname">SysvSemaphore</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">sem\_get</span>
-   <span class="function">sem\_release</span>

sem\_get
========

Get a semaphore id

### 说明

<span class="type"><span class="type">SysvSemaphore</span><span
class="type">false</span></span> <span
class="methodname">sem\_get</span> ( <span class="methodparam"><span
class="type">int</span> `$key`</span> \[, <span
class="methodparam"><span class="type">int</span> `$max_acquire`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$permissions`<span
class="initializer"> = 0666</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$auto_release`<span
class="initializer"> = **`true`**</span></span> \]\]\] )

<span class="function">sem\_get</span> returns an id that can be used to
access the System V semaphore with the given `key`.

A second call to <span class="function">sem\_get</span> for the same key
will return a different semaphore identifier, but both identifiers
access the same underlying semaphore.

If `key` is *0*, a new private semaphore is created for each call to
<span class="function">sem\_get</span>.

### 参数

`key`  

`max_acquire`  
The number of processes that can acquire the semaphore simultaneously is
set to `max_acquire`.

`permissions`  
The semaphore permissions. Actually this value is set only if the
process finds it is the only process currently attached to the
semaphore.

`auto_release`  
Specifies if the semaphore should be automatically released on request
shutdown.

### 返回值

Returns a positive semaphore identifier on success, or **`false`** on
error.

### 更新日志

| 版本  | 说明                                                                                                                                                          |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | On success, this function returns a <span class="classname">SysvSemaphore</span> instance now; previously, a <span class="type">resource</span> was returned. |
| 8.0.0 | The type of `auto_release` has been changed from <span class="type">int</span> to <span class="type">bool</span>.                                             |

### 注释

**Warning**

When using <span class="function">sem\_get</span> to access a semaphore
created outside PHP, note that the semaphore must have been created as a
set of 3 semaphores (for example, by specifying 3 as the *nsems*
parameter when calling the C *semget()* function), otherwise PHP will be
unable to access the semaphore.

### 参见

-   <span class="function">sem\_acquire</span>
-   <span class="function">sem\_release</span>
-   <span class="function">ftok</span>

sem\_release
============

Release a semaphore

### 说明

<span class="type">bool</span> <span
class="methodname">sem\_release</span> ( <span class="methodparam"><span
class="type">SysvSemaphore</span> `$semaphore`</span> )

<span class="function">sem\_release</span> releases the semaphore if it
is currently acquired by the calling process, otherwise a warning is
generated.

After releasing the semaphore, <span
class="function">sem\_acquire</span> may be called to re-acquire it.

### 参数

`semaphore`  
A Semaphore as returned by <span class="function">sem\_get</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `semaphore` expects a <span class="classname">SysvSemaphore</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">sem\_get</span>
-   <span class="function">sem\_acquire</span>

sem\_remove
===========

Remove a semaphore

### 说明

<span class="type">bool</span> <span
class="methodname">sem\_remove</span> ( <span class="methodparam"><span
class="type">SysvSemaphore</span> `$semaphore`</span> )

<span class="function">sem\_remove</span> removes the given semaphore.

After removing the semaphore, it is no longer accessible.

### 参数

`semaphore`  
A semaphore as returned by <span class="function">sem\_get</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `semaphore` expects a <span class="classname">SysvSemaphore</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">sem\_get</span>
-   <span class="function">sem\_release</span>
-   <span class="function">sem\_acquire</span>

shm\_attach
===========

Creates or open a shared memory segment

### 说明

<span class="type"><span class="type">SysvSharedMemory</span><span
class="type">false</span></span> <span
class="methodname">shm\_attach</span> ( <span class="methodparam"><span
class="type">int</span> `$key`</span> \[, <span
class="methodparam"><span class="type"><span
class="type">int</span><span class="type">null</span></span>
`$size`<span class="initializer"> = **`null`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$permissions`<span
class="initializer"> = 0666</span></span> \]\] )

<span class="function">shm\_attach</span> returns an id that can be used
to access the System V shared memory with the given `key`, the first
call creates the shared memory segment with `size` and the optional
perm-bits `permissions`.

A second call to <span class="function">shm\_attach</span> for the same
`key` will return a different <span
class="classname">SysvSharedMemory</span> instance, but both instances
access the same underlying shared memory. `size` and `permissions` will
be ignored.

### 参数

`key`  
A numeric shared memory segment ID

`size`  
The memory size. If not provided, default to the *sysvshm.init\_mem* in
the `php.ini`, otherwise 10000 bytes.

`permissions`  
The optional permission bits. Default to 0666.

### 返回值

Returns a <span class="classname">SysvSharedMemory</span> instance on
success, 或者在失败时返回 **`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                              |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | On success, this function returns an <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was returned. |
| 8.0.0 | `size` is nullable now.                                                                                                                                           |

### 参见

-   <span class="function">shm\_detach</span>
-   <span class="function">ftok</span>

shm\_detach
===========

Disconnects from shared memory segment

### 说明

<span class="type">bool</span> <span
class="methodname">shm\_detach</span> ( <span class="methodparam"><span
class="type">SysvSharedMemory</span> `$shm`</span> )

<span class="function">shm\_detach</span> disconnects from the shared
memory given by the `shm` created by <span
class="function">shm\_attach</span>. Remember, that shared memory still
exist in the Unix system and the data is still present.

### 参数

`shm`  
A shared memory segment obtained from <span
class="function">shm\_attach</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `shm` expects a <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">shm\_attach</span>
-   <span class="function">shm\_remove</span>
-   <span class="function">shm\_remove\_var</span>

shm\_get\_var
=============

Returns a variable from shared memory

### 说明

<span class="type">mixed</span> <span
class="methodname">shm\_get\_var</span> ( <span
class="methodparam"><span class="type">SysvSharedMemory</span>
`$shm`</span> , <span class="methodparam"><span class="type">int</span>
`$key`</span> )

<span class="function">shm\_get\_var</span> returns the variable with a
given `key`, in the given shared memory segment. The variable is still
present in the shared memory.

### 参数

`shm`  
A shared memory segment obtained from <span
class="function">shm\_attach</span>.

`key`  
The variable key.

### 返回值

Returns the variable with the given key.

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `shm` expects a <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">shm\_has\_var</span>
-   <span class="function">shm\_put\_var</span>

shm\_has\_var
=============

Check whether a specific entry exists

### 说明

<span class="type">bool</span> <span
class="methodname">shm\_has\_var</span> ( <span
class="methodparam"><span class="type">SysvSharedMemory</span>
`$shm`</span> , <span class="methodparam"><span class="type">int</span>
`$key`</span> )

Checks whether a specific key exists inside a shared memory segment.

### 参数

`shm`  
A shared memory segment obtained from <span
class="function">shm\_attach</span>.

`key`  
The variable key.

### 返回值

Returns **`true`** if the entry exists, otherwise **`false`**

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `shm` expects a <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">shm\_get\_var</span>
-   <span class="function">shm\_put\_var</span>

shm\_put\_var
=============

Inserts or updates a variable in shared memory

### 说明

<span class="type">bool</span> <span
class="methodname">shm\_put\_var</span> ( <span
class="methodparam"><span class="type">SysvSharedMemory</span>
`$shm`</span> , <span class="methodparam"><span class="type">int</span>
`$key`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="function">shm\_put\_var</span> inserts or updates the
`value` with the given `key`.

Warnings (**`E_WARNING`** level) will be issued if `shm` is not a valid
SysV shared memory index or if there was not enough shared memory
remaining to complete your request.

### 参数

`shm`  
A shared memory segment obtained from <span
class="function">shm\_attach</span>.

`key`  
The variable key.

`value`  
The variable. All
<a href="/language/types.html" class="link">variable types</a> that
<span class="function">serialize</span> supports may be used: generally
this means all types except for resources and some internal objects that
cannot be serialized.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `shm` expects a <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">shm\_get\_var</span>
-   <span class="function">shm\_has\_var</span>

shm\_remove\_var
================

Removes a variable from shared memory

### 说明

<span class="type">bool</span> <span
class="methodname">shm\_remove\_var</span> ( <span
class="methodparam"><span class="type">SysvSharedMemory</span>
`$shm`</span> , <span class="methodparam"><span class="type">int</span>
`$key`</span> )

Removes a variable with a given `key` and frees the occupied memory.

### 参数

`shm`  
A shared memory segment obtained from <span
class="function">shm\_attach</span>.

`key`  
The variable key.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `shm` expects a <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">shm\_remove</span>

shm\_remove
===========

Removes shared memory from Unix systems

### 说明

<span class="type">bool</span> <span
class="methodname">shm\_remove</span> ( <span class="methodparam"><span
class="type">SysvSharedMemory</span> `$shm`</span> )

<span class="function">shm\_remove</span> removes the shared memory
`shm`. All data will be destroyed.

### 参数

`shm`  
A shared memory segment obtained from <span
class="function">shm\_attach</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `shm` expects a <span class="classname">SysvSharedMemory</span> instance now; previously, a <span class="type">resource</span> was expected. |

### 参见

-   <span class="function">shm\_remove\_var</span>

**目录**

-   [ftok](/ref/sem.html#ftok) — Convert a pathname and a project
    identifier to a System V IPC key
-   [msg\_get\_queue](/ref/sem.html#msg_get_queue) — Create or attach to
    a message queue
-   [msg\_queue\_exists](/ref/sem.html#msg_queue_exists) — Check whether
    a message queue exists
-   [msg\_receive](/ref/sem.html#msg_receive) — Receive a message from a
    message queue
-   [msg\_remove\_queue](/ref/sem.html#msg_remove_queue) — Destroy a
    message queue
-   [msg\_send](/ref/sem.html#msg_send) — Send a message to a message
    queue
-   [msg\_set\_queue](/ref/sem.html#msg_set_queue) — Set information in
    the message queue data structure
-   [msg\_stat\_queue](/ref/sem.html#msg_stat_queue) — Returns
    information from the message queue data structure
-   [sem\_acquire](/ref/sem.html#sem_acquire) — Acquire a semaphore
-   [sem\_get](/ref/sem.html#sem_get) — Get a semaphore id
-   [sem\_release](/ref/sem.html#sem_release) — Release a semaphore
-   [sem\_remove](/ref/sem.html#sem_remove) — Remove a semaphore
-   [shm\_attach](/ref/sem.html#shm_attach) — Creates or open a shared
    memory segment
-   [shm\_detach](/ref/sem.html#shm_detach) — Disconnects from shared
    memory segment
-   [shm\_get\_var](/ref/sem.html#shm_get_var) — Returns a variable from
    shared memory
-   [shm\_has\_var](/ref/sem.html#shm_has_var) — Check whether a
    specific entry exists
-   [shm\_put\_var](/ref/sem.html#shm_put_var) — Inserts or updates a
    variable in shared memory
-   [shm\_remove\_var](/ref/sem.html#shm_remove_var) — Removes a
    variable from shared memory
-   [shm\_remove](/ref/sem.html#shm_remove) — Removes shared memory from
    Unix systems
