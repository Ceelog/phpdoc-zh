Windows 支持
------------

### **configure** flags

**configure** 命令现在支持 *CFLAGS* 和 *LDFLAGS* 环境变量。

### CTRL handling

CTRL+C and CTRL+BREAK on console can be caught by setting a handler
function with <span
class="function">sapi\_windows\_set\_ctrl\_handler</span>.

<span class="function">proc\_open</span> on Windows can be passed a
"create\_process\_group" option. It is required if the child process is
supposed to handle CTRL events.

### OPcache

OPcache now supports an arbitrary number of separate caches per user via
the the INI directive *opcache.cache\_id*. All processes with the same
cache ID and user share an OPcache instance.

### stat

The stat implementation has been refactored.

-   <span class="simpara"> An inode number is delivered and is based on
    the NTFS file index. </span>
-   <span class="simpara"> The device number is now based on the volume
    serial number. </span>

Note that both values are derived from the system and provided as-is on
64-bit systems. On 32-bit systems, these values might overflow the
32-bit integer in PHP, so they're fake.

### libsqlite3

libsqlite3 is no longer compiled statically into `php_sqlite3.dll` and
`php_pdo_sqlite.dll`, but rather available as `libsqlite3.dll`. Refer to
the installation instructions for
<a href="/book/sqlite3.html#安装" class="link">SQLite3</a> and
<a href="/book/pdo.html#安装" class="link">PDO_SQLITE</a>, respectively.
