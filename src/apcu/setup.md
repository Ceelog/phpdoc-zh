安装／配置
==========

**目录**

-   [需求](/apcu/setup.html#需求)
-   [安装](/apcu/setup.html#安装)
-   [运行时配置](/apcu/setup.html#运行时配置)
-   [资源类型](/apcu/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

If backward compatibility with the applicable parts of APC is required,
APCu must be configured with the option --enable-apcu-bc.

**Warning**

PHP 7 has a separate module
(<a href="https://pecl.php.net/apcu_bc" class="link external">» apc.so</a>)
for backwards compatibility with APC.

In backward compatibility mode, APCu registers the applicable APC
functions with backward compatible prototypes.

Where an APC function accepted `cache_type`, it is simply ignored by the
backward compatible version, and omitted from the prototype for the APCu
version.

> **Note**: <span class="simpara"> On Windows, APCu needs a temp path to
> exist, and be writable by the web server. It checks the TMP, TEMP and
> USERPROFILE environment variables in that order and finally tries the
> WINDOWS directory if none of those are set. </span>

> **Note**: <span class="simpara"> For more in-depth, highly technical
> implementation details, see the
> <a href="https://git.php.net/?p=pecl/caching/apc.git;a=blob;f=TECHNOTES.txt" class="link external">»  developer-supplied TECHNOTES file</a>
> . </span>

APCu sources can be found
<a href="https://github.com/krakjoe/apcu" class="link external">» here</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

Although the default APCu settings are fine for many installations,
serious users should consider tuning the following parameters.

There is one decision to be made configuring APCu. How much memory is
going to be allocated to APCu. The ini directive that controls this is
*apc.shm\_size* Read the sections on this carefully below.

Once the server is running, the *apc.php* script that is bundled with
the extension should be copied somewhere into the docroot and viewed
with a browser as it provides a detailed analysis of the internal
workings of APCu. If GD is enabled in PHP, it will even display some
interesting graphs. If APCu is working, the *Cache full count* number
(on the left) will display the number of times the cache has reached
maximum capacity and has had to forcefully clean any entries that
haven't been accessed in the last *apc.ttl* seconds. This number is
minimized in a well-configured cache. If the cache is constantly being
filled, and thusly forcefully freed, the resulting churning will have
disparaging effects on script performance. The easiest way to minimize
this number is to allocate more memory for APCu.

When APCu is compiled with mmap support (Memory Mapping), it will use
only one memory segment, unlike when APCu is built with SHM (SysV Shared
Memory) support that uses multiple memory segments. MMAP does not have a
maximum limit like SHM does in */proc/sys/kernel/shmmax*. In general
MMAP support is recommended because it will reclaim the memory faster
when the webserver is restarted and all in all reduces memory allocation
impact at startup.

| 名字                                                              | 默认      | 可修改范围       | 更新日志 |
|-------------------------------------------------------------------|-----------|------------------|----------|
| <a href="/apcu/setup.html#" class="link">apc.enabled</a>          | "1"       | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.shm_segments</a>     | "1"       | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.shm_size</a>         | "32M"     | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.entries_hint</a>     | "4096"    | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.ttl</a>              | "0"       | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.gc_ttl</a>           | "3600"    | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.mmap_file_mask</a>   | NULL      | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.slam_defense</a>     | "1"       | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.enable_cli</a>       | "0"       | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.use_request_time</a> | "1"       | PHP\_INI\_ALL    |          |
| <a href="/apcu/setup.html#" class="link">apc.serializer</a>       | "default" | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.coredump_unmap</a>   | "0"       | PHP\_INI\_SYSTEM |          |
| <a href="/apcu/setup.html#" class="link">apc.preload_path</a>     | NULL      | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`apc.enabled` <span class="type">boolean</span>  
*apc.enabled* can be set to 0 to disable APC. This is primarily useful
when APC is statically compiled into PHP, since there is no other way to
disable it (when compiled as a DSO, the *extension* line in *php.ini*
can just be commented-out).

`apc.shm_segments` <span class="type">integer</span>  
The number of shared memory segments to allocate for the compiler cache.
If APC is running out of shared memory but *apc.shm\_size* is set as
high as the system allows, raising this value might prevent APC from
exhausting its memory.

`apc.shm_size` <span class="type">string</span>  
The size of each shared memory segment given by a shorthand notation as
described in
<a href="/faq/using.html#faq.using.shorthandbytes" class="link">this FAQ</a>.
By default, some systems (including most BSD variants) have very low
limits on the size of a shared memory segment.

`apc.entries_hint` <span class="type">integer</span>  
A "hint" about the number of distinct variables that might be stored.
Set to zero or omit if not sure.

`apc.ttl` <span class="type">integer</span>  
The number of seconds a cache entry is allowed to idle in a slot in case
this cache entry slot is needed by another entry. Leaving this at zero
means that APC's cache could potentially fill up with stale entries
while newer entries won't be cached. In the event of a cache running out
of available memory, the cache will be completely expunged if ttl is
equal to 0. Otherwise, if the ttl is greater than 0, APC will attempt to
remove expired entries.

`apc.gc_ttl` <span class="type">integer</span>  
The number of seconds that a cache entry may remain on the
garbage-collection list. This value provides a fail-safe in the event
that a server process dies while executing a cached source file; if that
source file is modified, the memory allocated for the old version will
not be reclaimed until this TTL reached. Set to zero to disable this
feature.

`apc.mmap_file_mask` <span class="type">string</span>  
If compiled with MMAP support by using *--enable-mmap* this is the
mktemp-style file\_mask to pass to the mmap module for determining
whether your mmap'ed memory region is going to be file-backed or shared
memory backed. For straight file-backed mmap, set it to something like
*/tmp/apc.XXXXXX* (exactly 6 *X*s). To use POSIX-style shm\_open/mmap
put a *.shm* somewhere in your mask. e.g. */apc.shm.XXXXXX* You can also
set it to */dev/zero* to use your kernel's */dev/zero* interface to
anonymous mmap'ed memory. Leaving it undefined will force an anonymous
mmap.

`apc.slam_defense` <span class="type">integer</span>  
On very busy servers whenever you start the server or modify files you
can create a race of many processes all trying to cache the same file at
the same time. This option sets the percentage of processes that will
skip trying to cache an uncached file. Or think of it as the probability
of a single process to skip caching. For example, setting
*apc.slam\_defense* to *75* would mean that there is a 75% chance that
the process will not cache an uncached file. So, the higher the setting
the greater the defense against cache slams. Setting this to *0*
disables this feature.

`apc.enable_cli` <span class="type">integer</span>  
Mostly for testing and debugging. Setting this enables APC for the CLI
version of PHP. Under normal circumstances, it is not ideal to create,
populate and destroy the APC cache on every CLI request, but for various
test scenarios it is useful to be able to enable APC for the CLI version
of PHP easily.

`apc.serializer` <span class="type">string</span>  
Used to configure APC to use a third party serializer.

`apc.coredump_unmap` <span class="type">boolean</span>  
Enables APC handling of signals, such as SIGSEGV, that write core files
when signaled. When these signals are received, APC will attempt to
unmap the shared memory segment in order to exclude it from the core
file. This setting may improve system stability when fatal signals are
received and a large APC shared memory segment is configured.

**Warning**
This feature is potentially dangerous. Unmapping the shared memory
segment in a fatal signal handler may cause undefined behaviour if a
fatal error occurs.

> **Note**:
>
> Although some kernels may provide a facility to ignore various types
> of shared memory when generating a core dump file, these
> implementations may also ignore important shared memory segments such
> as the Apache scoreboard.

`apc.preload_path` <span class="type">string</span>  
Optionally, set a path to the directory that APC will load cache data at
startup.

`apc.use_request_time` <span class="type">bool</span>  
Use the SAPI request start time for TTL.

资源类型
--------

此扩展没有定义资源类型。
