shmop\_close
============

Close shared memory block

### 说明

<span class="type">void</span> <span
class="methodname">shmop\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$shmid`</span> )

<span class="function">shmop\_close</span> is used to close a shared
memory block.

### 参数

`shmid`  
The shared memory block resource created by <span
class="function">shmop\_open</span>

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 7.0.0 | The type of `shmid` has been changed from <span class="type">int</span> to <span class="type">resource</span>. |

### 范例

**示例 \#1 Closing shared memory block**

``` php
<?php
shmop_close($shm_id);
?>
```

This example will close shared memory block identified by *$shm\_id*.

### 参见

-   <span class="function">shmop\_open</span>

shmop\_delete
=============

Delete shared memory block

### 说明

<span class="type">bool</span> <span
class="methodname">shmop\_delete</span> ( <span
class="methodparam"><span class="type">resource</span> `$shmid`</span> )

<span class="function">shmop\_delete</span> is used to delete a shared
memory block.

### 参数

`shmid`  
The shared memory block resource created by <span
class="function">shmop\_open</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 7.0.0 | The type of `shmid` has been changed from <span class="type">int</span> to <span class="type">resource</span>. |

### 范例

**示例 \#1 Deleting shared memory block**

``` php
<?php
shmop_delete($shm_id);
?>
```

This example will delete shared memory block identified by *$shm\_id*.

shmop\_open
===========

Create or open shared memory block

### 说明

<span class="type">resource</span> <span
class="methodname">shmop\_open</span> ( <span class="methodparam"><span
class="type">int</span> `$key`</span> , <span class="methodparam"><span
class="type">string</span> `$flags`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> , <span
class="methodparam"><span class="type">int</span> `$size`</span> )

<span class="function">shmop\_open</span> can create or open a shared
memory block.

### 参数

`key`  
System's id for the shared memory block. Can be passed as a decimal or
hex.

`flags`  
The flags that you can use:

-   <span class="simpara"> "a" for access (sets SHM\_RDONLY for shmat)
    use this flag when you need to open an existing shared memory
    segment for read only </span>
-   <span class="simpara"> "c" for create (sets IPC\_CREATE) use this
    flag when you need to create a new shared memory segment or if a
    segment with the same key exists, try to open it for read and write
    </span>
-   <span class="simpara"> "w" for read & write access use this flag
    when you need to read and write to a shared memory segment, use this
    flag in most cases. </span>
-   <span class="simpara"> "n" create a new memory segment (sets
    IPC\_CREATE\|IPC\_EXCL) use this flag when you want to create a new
    shared memory segment but if one already exists with the same flag,
    fail. This is useful for security purposes, using this you can
    prevent race condition exploits. </span>

`mode`  
The permissions that you wish to assign to your memory segment, those
are the same as permission for a file. Permissions need to be passed in
octal form, like for example *0644*

`size`  
The size of the shared memory block you wish to create in bytes

> **Note**:
>
> Note: the 3rd and 4th should be entered as 0 if you are opening an
> existing memory segment.

### 返回值

On success <span class="function">shmop\_open</span> will return an
resource that you can use to access the shared memory segment you've
created. **`FALSE`** is returned on failure.

### 更新日志

| 版本  | 说明                                                                                                                                                    |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.0 | The return type of <span class="function">shmop\_open</span> has been changed from <span class="type">int</span> to <span class="type">resource</span>. |

### 范例

**示例 \#1 Create a new shared memory block**

``` php
<?php
$shm_key = ftok(__FILE__, 't');
$shm_id = shmop_open($shm_key, "c", 0644, 100);
?>
```

This example opened a shared memory block with a system id returned by
<span class="function">ftok</span>.

### 参见

-   <span class="function">shmop\_close</span>
-   <span class="function">shmop\_delete</span>

shmop\_read
===========

Read data from shared memory block

### 说明

<span class="type">string</span> <span
class="methodname">shmop\_read</span> ( <span class="methodparam"><span
class="type">resource</span> `$shmid`</span> , <span
class="methodparam"><span class="type">int</span> `$start`</span> ,
<span class="methodparam"><span class="type">int</span> `$count`</span>
)

<span class="function">shmop\_read</span> will read a string from shared
memory block.

### 参数

`shmid`  
The shared memory block identifier created by <span
class="function">shmop\_open</span>

`start`  
Offset from which to start reading

`count`  
The number of bytes to read. *0* reads `shmop_size($shmid) - $start`
bytes.

### 返回值

Returns the data 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 7.0.0 | The type of `shmid` has been changed from <span class="type">int</span> to <span class="type">resource</span>. |

### 范例

**示例 \#1 Reading shared memory block**

``` php
<?php
$shm_data = shmop_read($shm_id, 0, 50);
?>
```

This example will read 50 bytes from shared memory block and place the
data inside *$shm\_data*.

### 参见

-   <span class="function">shmop\_write</span>

shmop\_size
===========

Get size of shared memory block

### 说明

<span class="type">int</span> <span
class="methodname">shmop\_size</span> ( <span class="methodparam"><span
class="type">resource</span> `$shmid`</span> )

<span class="function">shmop\_size</span> is used to get the size, in
bytes of the shared memory block.

### 参数

`shmid`  
The shared memory block identifier created by <span
class="function">shmop\_open</span>

### 返回值

Returns an int, which represents the number of bytes the shared memory
block occupies.

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 7.0.0 | The type of `shmid` has been changed from <span class="type">int</span> to <span class="type">resource</span>. |

### 范例

**示例 \#1 Getting the size of the shared memory block**

``` php
<?php
$shm_size = shmop_size($shm_id);
?>
```

This example will put the size of shared memory block identified by
*$shm\_id* into *$shm\_size*.

shmop\_write
============

Write data into shared memory block

### 说明

<span class="type">int</span> <span
class="methodname">shmop\_write</span> ( <span class="methodparam"><span
class="type">resource</span> `$shmid`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$offset`</span>
)

<span class="function">shmop\_write</span> will write a string into
shared memory block.

### 参数

`shmid`  
The shared memory block identifier created by <span
class="function">shmop\_open</span>

`data`  
A string to write into shared memory block

`offset`  
Specifies where to start writing data inside the shared memory segment.

### 返回值

The size of the written `data`, or **`FALSE`** on failure.

### 更新日志

| 版本  | 说明                                                                                                           |
|-------|----------------------------------------------------------------------------------------------------------------|
| 7.0.0 | The type of `shmid` has been changed from <span class="type">int</span> to <span class="type">resource</span>. |

### 范例

**示例 \#1 Writing to shared memory block**

``` php
<?php
$shm_bytes_written = shmop_write($shm_id, $my_string, 0);
?>
```

This example will write data inside *$my\_string* into shared memory
block, *$shm\_bytes\_written* will contain the number of bytes written.

### 参见

-   <span class="function">shmop\_read</span>

**目录**

-   [shmop\_close](/ref/shmop.html#shmop_close) — Close shared memory
    block
-   [shmop\_delete](/ref/shmop.html#shmop_delete) — Delete shared memory
    block
-   [shmop\_open](/ref/shmop.html#shmop_open) — Create or open shared
    memory block
-   [shmop\_read](/ref/shmop.html#shmop_read) — Read data from shared
    memory block
-   [shmop\_size](/ref/shmop.html#shmop_size) — Get size of shared
    memory block
-   [shmop\_write](/ref/shmop.html#shmop_write) — Write data into shared
    memory block
