预定义常量
==========

**目录**

-   [posix\_access
    constants](/posix/constants.html#posix_access%20constants)
-   [posix\_mknod
    constants](/posix/constants.html#posix_mknod%20constants)
-   [posix\_setrlimit
    constants](/posix/constants.html#posix_setrlimit%20constants)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

<span class="function">posix\_access</span> constants
-----------------------------------------------------

> **Note**:
>
> These constants are available starting with PHP 5.1.0. Please note
> that some of them may not be available on your system.

**`POSIX_F_OK`** (<span class="type">int</span>)  
<span class="simpara"> Check whether the file exists. </span>

**`POSIX_R_OK`** (<span class="type">int</span>)  
<span class="simpara"> Check whether the file exists and has read
permissions. </span>

**`POSIX_W_OK`** (<span class="type">int</span>)  
<span class="simpara"> Check whether the file exists and has write
permissions. </span>

**`POSIX_X_OK`** (<span class="type">int</span>)  
<span class="simpara"> Check whether the file exists and has execute
permissions. </span>

<span class="function">posix\_mknod</span> constants
----------------------------------------------------

> **Note**:
>
> These constants are available starting with PHP 5.1.0. Please note
> that some of them may not be available on your system.

**`POSIX_S_IFBLK`** (<span class="type">int</span>)  
<span class="simpara"> Block special file </span>

**`POSIX_S_IFCHR`** (<span class="type">int</span>)  
<span class="simpara"> Character special file </span>

**`POSIX_S_IFIFO`** (<span class="type">int</span>)  
<span class="simpara"> FIFO (named pipe) special file </span>

**`POSIX_S_IFREG`** (<span class="type">int</span>)  
<span class="simpara"> Normal file </span>

**`POSIX_S_IFSOCK`** (<span class="type">int</span>)  
<span class="simpara"> Socket </span>

<span class="function">posix\_setrlimit</span> constants
--------------------------------------------------------

> **Note**:
>
> These constants are available starting with PHP 7.0.0. Please note
> that some of them may not be available on your system.

> **Note**:
>
> You may wish to read the below notes in conjunction with the manpage
> for <span class="function">setrlimit</span> on your specific operating
> system, as there is variance in how these limits are interpreted, even
> across operating systems that claim to implement POSIX in full.

**`POSIX_RLIMIT_AS`** (<span class="type">int</span>)  
<span class="simpara"> The maximum size of the process's address space
in bytes. See also PHP's
<a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>
configuration directive. </span>

**`POSIX_RLIMIT_CORE`** (<span class="type">int</span>)  
<span class="simpara"> The maximum size of a core file. If the limit is
set to 0, no core file will be generated. </span>

**`POSIX_RLIMIT_CPU`** (<span class="type">int</span>)  
<span class="simpara"> The maximum amount of CPU time that the process
can use, in seconds. When the soft limit is hit, a *SIGXCPU* signal will
be sent, which can be caught with <span
class="function">pcntl\_signal</span>. Depending on the operating
system, additional *SIGXCPU* signals may be sent each second until the
hard limit is hit, at which point an uncatchable *SIGKILL* signal is
sent. </span> <span class="simpara"> See also <span
class="function">set\_time\_limit</span>. </span>

**`POSIX_RLIMIT_DATA`** (<span class="type">int</span>)  
<span class="simpara"> The maximum size of the process's data segment,
in bytes. It is extremely unlikely that this will have any effect on the
execution of PHP unless an extension is in use that calls <span
class="function">brk</span> or <span class="function">sbrk</span>.
</span>

**`POSIX_RLIMIT_FSIZE`** (<span class="type">int</span>)  
<span class="simpara"> The maximum size of files that the process can
create, in bytes. </span>

**`POSIX_RLIMIT_LOCKS`** (<span class="type">int</span>)  
<span class="simpara"> The maximum number of locks that the process can
create. This is only supported on extremely old Linux kernels. </span>

**`POSIX_RLIMIT_MEMLOCK`** (<span class="type">int</span>)  
<span class="simpara"> The maximum number of bytes that can be locked
into memory. </span>

**`POSIX_RLIMIT_MSGQUEUE`** (<span class="type">int</span>)  
<span class="simpara"> The maximum number of bytes that can be allocated
for POSIX message queues. PHP does not ship with support for POSIX
message queues, so this limit will not have any effect unless you are
using an extension that implements that support. </span>

**`POSIX_RLIMIT_NICE`** (<span class="type">int</span>)  
<span class="simpara"> The maximum value to which the process can be
<a href="/ref/pcntl.html#pcntl_setpriority" class="link">reniced</a> to.
The value that will be used will be *20 - limit*, as resource limit
values cannot be negative. </span>

**`POSIX_RLIMIT_NOFILE`** (<span class="type">int</span>)  
<span class="simpara"> A value one greater than the maximum file
descriptor number that can be opened by this process. </span>

**`POSIX_RLIMIT_NPROC`** (<span class="type">int</span>)  
<span class="simpara"> The maximum number of processes (and/or threads,
on some operating systems) that can be created for the real user ID of
the process. </span>

**`POSIX_RLIMIT_RSS`** (<span class="type">int</span>)  
<span class="simpara"> The maximum size of the process's resident set,
in pages. </span>

**`POSIX_RLIMIT_RTPRIO`** (<span class="type">int</span>)  
<span class="simpara"> The maximum real time priority that can be set
via the <span class="function">sched\_setscheduler</span> and <span
class="function">sched\_setparam</span> system calls. </span>

**`POSIX_RLIMIT_RTTIME`** (<span class="type">int</span>)  
<span class="simpara"> The maximum amount of CPU time, in microseconds,
that the process can consume without making a blocking system call if it
is using real time scheduling. </span>

**`POSIX_RLIMIT_SIGPENDING`** (<span class="type">int</span>)  
<span class="simpara"> The maximum number of signals that can be queued
for the real user ID of the process. </span>

**`POSIX_RLIMIT_STACK`** (<span class="type">int</span>)  
<span class="simpara"> The maximum size of the process stack, in bytes.
</span>

**`POSIX_RLIMIT_INFINITY`** (<span class="type">int</span>)  
<span class="simpara"> Used to indicate an infinite value for a resource
limit. </span>
