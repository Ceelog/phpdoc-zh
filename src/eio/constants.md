预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Request priority constants:

**`EIO_PRI_MIN`** (<span class="type">int</span>)  
<span class="simpara"> Request minimal prioriry </span>

**`EIO_PRI_DEFAULT`** (<span class="type">int</span>)  
<span class="simpara"> Request default prioriry </span>

**`EIO_PRI_MAX`** (<span class="type">int</span>)  
<span class="simpara"> Request maximal prioriry </span>

<span class="function">eio\_seek</span> `whence` argument:

**`EIO_SEEK_SET`** (<span class="type">int</span>)  
<span class="simpara"> The offset is set to specified number of
bytes(`offset`). </span>

**`EIO_SEEK_CUR`** (<span class="type">int</span>)  
<span class="simpara"> The offset is set to its current location plus
`offset` bytes. </span>

**`EIO_SEEK_END`** (<span class="type">int</span>)  
<span class="simpara"> The offset is set to the size of the file plus
`offset` bytes. </span>

Flags used with <span class="function">eio\_readdir</span>:

**`EIO_READDIR_DENTS`** (<span class="type">int</span>)  
<span class="simpara"> <span class="function">eio\_readdir</span> flag.
If specified, the result argument of the callback becomes an array with
the following keys: *'names'* - array of directory names *'dents'* -
array of *struct eio\_dirent*-like arrays having the following keys
each: *'name'* - the directory name; *'type'* - one of *EIO\_DT\_\**
constants; *'inode'* - the inode number, if available, otherwise
unspecified; </span>

**`EIO_READDIR_DIRS_FIRST`** (<span class="type">int</span>)  
<span class="simpara"> When this flag is specified, the names will be
returned in an order where likely directories come first, in optimal
stat order. </span>

**`EIO_READDIR_STAT_ORDER`** (<span class="type">int</span>)  
<span class="simpara"> When this flag is specified, then the names will
be returned in an order suitable for *stat*'ing each one. When planning
to <span class="function">stat</span> all files in the given directory,
the returned order will likely be fastest. </span>

**`EIO_READDIR_FOUND_UNKNOWN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_DT_UNKNOWN`** (<span class="type">int</span>)  
<span class="simpara"> Unknown node type(very common). Further <span
class="function">stat</span> needed. </span>

**`EIO_DT_FIFO`** (<span class="type">int</span>)  
<span class="simpara"> FIFO node type </span>

**`EIO_DT_CHR`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_MPC`** (<span class="type">int</span>)  
<span class="simpara"> Multiplexed char device (v7+coherent) node type
</span>

**`EIO_DT_DIR`** (<span class="type">int</span>)  
<span class="simpara"> Directory node type </span>

**`EIO_DT_NAM`** (<span class="type">int</span>)  
<span class="simpara"> Xenix special named file node type </span>

**`EIO_DT_BLK`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_MPB`** (<span class="type">int</span>)  
<span class="simpara"> Multiplexed block device (v7+coherent) </span>

**`EIO_DT_REG`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_NWK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_DT_CMP`** (<span class="type">int</span>)  
<span class="simpara"> HP-UX network special node type </span>

**`EIO_DT_LNK`** (<span class="type">int</span>)  
<span class="simpara"> Link node type </span>

**`EIO_DT_SOCK`** (<span class="type">int</span>)  
<span class="simpara"> Socket node type </span>

**`EIO_DT_DOOR`** (<span class="type">int</span>)  
<span class="simpara"> Solaris door node type </span>

**`EIO_DT_WHT`** (<span class="type">int</span>)  
<span class="simpara"> Node type </span>

**`EIO_DT_MAX`** (<span class="type">int</span>)  
<span class="simpara"> Highest node type value </span>

Access modes for <span class="function">eio\_open</span> `flags`
argument:

**`EIO_O_RDONLY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_WRONLY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_RDWR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_NONBLOCK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_APPEND`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_CREAT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_TRUNC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_EXCL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_O_FSYNC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

`mode` argument flags for <span class="function">eio\_open</span>:

**`EIO_S_IRUSR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IWUSR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IXUSR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IRGRP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IWGRP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IXGRP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IROTH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IWOTH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IXOTH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IFREG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IFCHR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IFBLK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IFIFO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_S_IFSOCK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<span class="function">eio\_sync\_file\_range</span> flags:

**`EIO_SYNC_FILE_RANGE_WAIT_BEFORE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_SYNC_FILE_RANGE_WRITE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`EIO_SYNC_FILE_RANGE_WAIT_AFTER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<span class="function">eio\_fallocate</span> flags:

**`EIO_FALLOC_FL_KEEP_SIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

> **Note**:
>
> *EIO\_S\_I\** constants have the same meaning as their *S\_I\** POSIX
> counterparts.

> **Note**:
>
> *EIO\_SYNC\_FILE\_\** constants have the same meaning as their
> *SYNC\_FILE\_\*\** counterparts.

> **Note**:
>
> *EIO\_O\_\** constants have the same meaning as their *O\_\** POSIX
> counterparts.
