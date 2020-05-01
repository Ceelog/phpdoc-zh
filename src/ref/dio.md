dio\_close
==========

Closes the file descriptor given by fd

### 说明

<span class="type">void</span> <span
class="methodname">dio\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$fd`</span> )

The function <span class="function">dio\_close</span> closes the file
descriptor `fd`.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

### 返回值

没有返回值。

### 范例

**示例 \#1 Closing an open file descriptor**

``` php
<?php
$fd = dio_open('/dev/ttyS0', O_RDWR);

dio_close($fd);
?>
```

### 参见

-   <span class="function">dio\_open</span>

dio\_fcntl
==========

Performs a c library fcntl on fd

### 说明

<span class="type">mixed</span> <span
class="methodname">dio\_fcntl</span> ( <span class="methodparam"><span
class="type">resource</span> `$fd`</span> , <span
class="methodparam"><span class="type">int</span> `$cmd`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$args`</span>
\] )

The <span class="function">dio\_fcntl</span> function performs the
operation specified by `cmd` on the file descriptor `fd`. Some commands
require additional arguments `args` to be supplied.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

`cmd`  
Can be one of the following operations:

-   **`F_SETLK`** - Lock is set or cleared. If the lock is held by
    someone else <span class="function">dio\_fcntl</span> returns -1.

-   **`F_SETLKW`** - like **`F_SETLK`**, but in case the lock is held by
    someone else, <span class="function">dio\_fcntl</span> waits until
    the lock is released.

-   **`F_GETLK`** - <span class="function">dio\_fcntl</span> returns an
    associative array (as described below) if someone else prevents
    lock. If there is no obstruction key "type" will set to
    **`F_UNLCK`**.

-   **`F_DUPFD`** - finds the lowest numbered available file descriptor
    greater than or equal to `args` and returns them.

-   **`F_SETFL`** - Sets the file descriptors flags to the value
    specified by `args`, which can be **`O_APPEND`**, **`O_NONBLOCK`**
    or **`O_ASYNC`**. To use **`O_ASYNC`** you will need to use the
    <a href="/ref/pcntl.html" class="link">PCNTL</a> extension.

`args`  
`args` is an associative array, when `cmd` is **`F_SETLK`** or
**`F_SETLLW`**, with the following keys:

-   *start* - offset where lock begins

-   *length* - size of locked area. zero means to end of file

-   *whence* - Where l\_start is relative to: can be **`SEEK_SET`**,
    **`SEEK_END`** and **`SEEK_CUR`**

-   *type* - type of lock: can be **`F_RDLCK`** (read lock),
    **`F_WRLCK`** (write lock) or **`F_UNLCK`** (unlock)

### 返回值

Returns the result of the C call.

### 范例

**示例 \#1 Setting and clearing a lock**

``` php
<?php

$fd = dio_open('/dev/ttyS0', O_RDWR);

if (dio_fcntl($fd, F_SETLK, Array("type"=>F_WRLCK)) == -1) {
   // the file descriptor appears locked
   echo "The lock can not be cleared. It is held by someone else.";
} else {
   echo "Lock successfully set/cleared";
}

dio_close($fd);
?>
```

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

dio\_open
=========

Opens a file (creating it if necessary) at a lower level than the C
library input/ouput stream functions allow

### 说明

<span class="type">resource</span> <span
class="methodname">dio\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">int</span> `$flags`</span> \[,
<span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \] )

<span class="function">dio\_open</span> opens a file and returns a new
file descriptor for it.

### 参数

`filename`  
The pathname of the file to open.

`flags`  
The `flags` parameter is a bitwise-ORed value comprising flags from the
following list. This value *must* include one of **`O_RDONLY`**,
**`O_WRONLY`**, or **`O_RDWR`**. Additionally, it may include any
combination of the other flags from this list.

-   **`O_RDONLY`** - opens the file for read access.

-   **`O_WRONLY`** - opens the file for write access.

-   **`O_RDWR`** - opens the file for both reading and writing.

-   **`O_CREAT`** - creates the file, if it doesn't already exist.

-   **`O_EXCL`** - if both **`O_CREAT`** and **`O_EXCL`** are set and
    the file already exists, <span class="function">dio\_open</span>
    will fail.

-   **`O_TRUNC`** - if the file exists and is opened for write access,
    the file will be truncated to zero length.

-   **`O_APPEND`** - write operations write data at the end of the file.

-   **`O_NONBLOCK`** - sets non blocking mode.

-   **`O_NOCTTY`** - prevent the OS from assigning the opened file as
    the process's controlling terminal when opening a TTY device file.

`mode`  
If `flags` contains **`O_CREAT`**, `mode` will set the permissions of
the file (creation permissions). `mode` is required for correct
operation when **`O_CREAT`** is specified in `flags` and is ignored
otherwise.

The actual permissions assigned to the created file will be affected by
the process's *umask* setting as per usual.

### 返回值

A file descriptor or **`FALSE`** on error.

### 范例

**示例 \#1 Opening a file descriptor**

``` php
<?php

$fd = dio_open('/dev/ttyS0', O_RDWR | O_NOCTTY | O_NONBLOCK);

dio_close($fd);
?>
```

### 参见

-   <span class="function">dio\_close</span>

dio\_read
=========

Reads bytes from a file descriptor

### 说明

<span class="type">string</span> <span
class="methodname">dio\_read</span> ( <span class="methodparam"><span
class="type">resource</span> `$fd`</span> \[, <span
class="methodparam"><span class="type">int</span> `$len`<span
class="initializer"> = 1024</span></span> \] )

The function <span class="function">dio\_read</span> reads and returns
`len` bytes from file with descriptor `fd`.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

`len`  
The number of bytes to read. If not specified, <span
class="function">dio\_read</span> reads 1K sized block.

### 返回值

The bytes read from `fd`.

### 参见

-   <span class="function">dio\_write</span>

dio\_seek
=========

Seeks to pos on fd from whence

### 说明

<span class="type">int</span> <span class="methodname">dio\_seek</span>
( <span class="methodparam"><span class="type">resource</span>
`$fd`</span> , <span class="methodparam"><span class="type">int</span>
`$pos`</span> \[, <span class="methodparam"><span
class="type">int</span> `$whence`<span class="initializer"> =
SEEK\_SET</span></span> \] )

The function <span class="function">dio\_seek</span> is used to change
the file position of the given file descriptor.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

`pos`  
The new position.

`whence`  
Specifies how the position `pos` should be interpreted:

-   **`SEEK_SET`** (default) - specifies that `pos` is specified from
    the beginning of the file.

-   **`SEEK_CUR`** - Specifies that `pos` is a count of characters from
    the current file position. This count may be positive or negative.

-   **`SEEK_END`** - Specifies that `pos` is a count of characters from
    the end of the file. A negative count specifies a position within
    the current extent of the file; a positive count specifies a
    position past the current end. If you set the position past the
    current end, and actually write data, you will extend the file with
    zeros up to that position.

### 返回值

### 范例

**示例 \#1 Positioning in a file**

``` php
<?php

$fd = dio_open('/dev/ttyS0', O_RDWR);

dio_seek($fd, 10, SEEK_SET);
// position is now at 10 characters from the start of the file

dio_seek($fd, -2, SEEK_CUR);
// position is now at 8 characters from the start of the file

dio_seek($fd, -5, SEEK_END);
// position is now at 5 characters from the end of the file

dio_seek($fd, 10, SEEK_END);
// position is now at 10 characters past the end of the file. 
// The 10 characters between the end of the file and the current
// position are filled with zeros.

dio_close($fd);
?>
```

dio\_stat
=========

Gets stat information about the file descriptor fd

### 说明

<span class="type">array</span> <span
class="methodname">dio\_stat</span> ( <span class="methodparam"><span
class="type">resource</span> `$fd`</span> )

<span class="function">dio\_stat</span> returns information about the
given file descriptor.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

### 返回值

Returns an associative array with the following keys:

-   "device" - device

-   "inode" - inode

-   "mode" - mode

-   "nlink" - number of hard links

-   "uid" - user id

-   "gid" - group id

-   "device\_type" - device type (if inode device)

-   "size" - total size in bytes

-   "blocksize" - blocksize

-   "blocks" - number of blocks allocated

-   "atime" - time of last access

-   "mtime" - time of last modification

-   "ctime" - time of last change

On error <span class="function">dio\_stat</span> returns **`NULL`**.

dio\_tcsetattr
==============

Sets terminal attributes and baud rate for a serial port

### 说明

<span class="type">bool</span> <span
class="methodname">dio\_tcsetattr</span> ( <span
class="methodparam"><span class="type">resource</span> `$fd`</span> ,
<span class="methodparam"><span class="type">array</span>
`$options`</span> )

<span class="function">dio\_tcsetattr</span> sets the terminal
attributes and baud rate of the open `fd`.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

`options`  
The currently available options are:

-   'baud' - baud rate of the port - can be
    38400,19200,9600,4800,2400,1800, 1200,600,300,200,150,134,110,75 or
    50, default value is 9600.

-   'bits' - data bits - can be 8,7,6 or 5. Default value is 8.

-   'stop' - stop bits - can be 1 or 2. Default value is 1.

-   'parity' - can be 0,1 or 2. Default value is 0.

### 返回值

没有返回值。

### 范例

**示例 \#1 Setting the baud rate on a serial port**

``` php
<?php

$fd = dio_open('/dev/ttyS0', O_RDWR | O_NOCTTY | O_NONBLOCK);

dio_fcntl($fd, F_SETFL, O_SYNC);

dio_tcsetattr($fd, array(
  'baud' => 9600,
  'bits' => 8,
  'stop'  => 1,
  'parity' => 0
)); 

while (1) {

  $data = dio_read($fd, 256);

  if ($data) {
      echo $data;
  }
} 

?>
```

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

dio\_truncate
=============

Truncates file descriptor fd to offset bytes

### 说明

<span class="type">bool</span> <span
class="methodname">dio\_truncate</span> ( <span
class="methodparam"><span class="type">resource</span> `$fd`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

<span class="function">dio\_truncate</span> truncates a file to at most
`offset` bytes in size.

If the file previously was larger than this size, the extra data is
lost. If the file previously was shorter, it is unspecified whether the
file is left unchanged or is extended. In the latter case the extended
part reads as zero bytes.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

`offset`  
The offset in bytes.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

dio\_write
==========

Writes data to fd with optional truncation at length

### 说明

<span class="type">int</span> <span class="methodname">dio\_write</span>
( <span class="methodparam"><span class="type">resource</span>
`$fd`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> \[, <span
class="methodparam"><span class="type">int</span> `$len`<span
class="initializer"> = 0</span></span> \] )

<span class="function">dio\_write</span> writes up to `len` bytes from
`data` to file `fd`.

### 参数

`fd`  
The file descriptor returned by <span class="function">dio\_open</span>.

`data`  
The written data.

`len`  
The length of data to write in bytes. If not specified, the function
writes all the data to the specified file.

### 返回值

Returns the number of bytes written to `fd`.

### 参见

-   <span class="function">dio\_read</span>

**目录**

-   [dio\_close](/ref/dio.html#dio_close) — Closes the file descriptor
    given by fd
-   [dio\_fcntl](/ref/dio.html#dio_fcntl) — Performs a c library fcntl
    on fd
-   [dio\_open](/ref/dio.html#dio_open) — Opens a file (creating it if
    necessary) at a lower level than the C library input/ouput stream
    functions allow
-   [dio\_read](/ref/dio.html#dio_read) — Reads bytes from a file
    descriptor
-   [dio\_seek](/ref/dio.html#dio_seek) — Seeks to pos on fd from whence
-   [dio\_stat](/ref/dio.html#dio_stat) — Gets stat information about
    the file descriptor fd
-   [dio\_tcsetattr](/ref/dio.html#dio_tcsetattr) — Sets terminal
    attributes and baud rate for a serial port
-   [dio\_truncate](/ref/dio.html#dio_truncate) — Truncates file
    descriptor fd to offset bytes
-   [dio\_write](/ref/dio.html#dio_write) — Writes data to fd with
    optional truncation at length
