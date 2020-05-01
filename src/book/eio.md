Eio
===

**目录**

-   [简介](/intro/eio.html)
-   [安装／配置](/eio/setup.html)
    -   [需求](/eio/setup.html#需求)
    -   [安装](/eio/setup.html#安装)
    -   [运行时配置](/eio/setup.html#运行时配置)
    -   [资源类型](/eio/setup.html#资源类型)
-   [预定义常量](/eio/constants.html)
-   [范例](/eio/examples.html)
-   [Eio 函数](/ref/eio.html)
    -   [eio\_busy](/ref/eio.html#eio_busy) — Artificially increase
        load. Could be useful in tests, benchmarking
    -   [eio\_cancel](/ref/eio.html#eio_cancel) — Cancels a request
    -   [eio\_chmod](/ref/eio.html#eio_chmod) — Change file/directory
        permissions
    -   [eio\_chown](/ref/eio.html#eio_chown) — Change file/directory
        permissions
    -   [eio\_close](/ref/eio.html#eio_close) — Close file
    -   [eio\_custom](/ref/eio.html#eio_custom) — Execute custom request
        like any other eio\_\* call
    -   [eio\_dup2](/ref/eio.html#eio_dup2) — Duplicate a file
        descriptor
    -   [eio\_event\_loop](/ref/eio.html#eio_event_loop) — Polls libeio
        until all requests proceeded
    -   [eio\_fallocate](/ref/eio.html#eio_fallocate) — Allows the
        caller to directly manipulate the allocated disk space for a
        file
    -   [eio\_fchmod](/ref/eio.html#eio_fchmod) — Change file
        permissions
    -   [eio\_fchown](/ref/eio.html#eio_fchown) — Change file ownership
    -   [eio\_fdatasync](/ref/eio.html#eio_fdatasync) — Synchronize a
        file's in-core state with storage device
    -   [eio\_fstat](/ref/eio.html#eio_fstat) — Get file status
    -   [eio\_fstatvfs](/ref/eio.html#eio_fstatvfs) — Get file system
        statistics
    -   [eio\_fsync](/ref/eio.html#eio_fsync) — Synchronize a file's
        in-core state with storage device
    -   [eio\_ftruncate](/ref/eio.html#eio_ftruncate) — Truncate a file
    -   [eio\_futime](/ref/eio.html#eio_futime) — Change file last
        access and modification times
    -   [eio\_get\_event\_stream](/ref/eio.html#eio_get_event_stream) —
        Get stream representing a variable used in internal
        communications with libeio
    -   [eio\_get\_last\_error](/ref/eio.html#eio_get_last_error) —
        Returns string describing the last error associated with a
        request resource
    -   [eio\_grp\_add](/ref/eio.html#eio_grp_add) — Adds a request to
        the request group
    -   [eio\_grp\_cancel](/ref/eio.html#eio_grp_cancel) — Cancels a
        request group
    -   [eio\_grp\_limit](/ref/eio.html#eio_grp_limit) — Set group limit
    -   [eio\_grp](/ref/eio.html#eio_grp) — Creates a request group
    -   [eio\_init](/ref/eio.html#eio_init) — (Re-)initialize Eio
    -   [eio\_link](/ref/eio.html#eio_link) — Create a hardlink for file
    -   [eio\_lstat](/ref/eio.html#eio_lstat) — Get file status
    -   [eio\_mkdir](/ref/eio.html#eio_mkdir) — Create directory
    -   [eio\_mknod](/ref/eio.html#eio_mknod) — Create a special or
        ordinary file
    -   [eio\_nop](/ref/eio.html#eio_nop) — Does nothing, except go
        through the whole request cycle
    -   [eio\_npending](/ref/eio.html#eio_npending) — Returns number of
        finished, but unhandled requests
    -   [eio\_nready](/ref/eio.html#eio_nready) — Returns number of
        not-yet handled requests
    -   [eio\_nreqs](/ref/eio.html#eio_nreqs) — Returns number of
        requests to be processed
    -   [eio\_nthreads](/ref/eio.html#eio_nthreads) — Returns number of
        threads currently in use
    -   [eio\_open](/ref/eio.html#eio_open) — Opens a file
    -   [eio\_poll](/ref/eio.html#eio_poll) — Can be to be called
        whenever there are pending requests that need finishing
    -   [eio\_read](/ref/eio.html#eio_read) — Read from a file
        descriptor at given offset
    -   [eio\_readahead](/ref/eio.html#eio_readahead) — Perform file
        readahead into page cache
    -   [eio\_readdir](/ref/eio.html#eio_readdir) — Reads through a
        whole directory
    -   [eio\_readlink](/ref/eio.html#eio_readlink) — Read value of a
        symbolic link
    -   [eio\_realpath](/ref/eio.html#eio_realpath) — Get the
        canonicalized absolute pathname
    -   [eio\_rename](/ref/eio.html#eio_rename) — Change the name or
        location of a file
    -   [eio\_rmdir](/ref/eio.html#eio_rmdir) — Remove a directory
    -   [eio\_seek](/ref/eio.html#eio_seek) — Repositions the offset of
        the open file associated with the fd argument to the argument
        offset according to the directive whence
    -   [eio\_sendfile](/ref/eio.html#eio_sendfile) — Transfer data
        between file descriptors
    -   [eio\_set\_max\_idle](/ref/eio.html#eio_set_max_idle) — Set
        maximum number of idle threads
    -   [eio\_set\_max\_parallel](/ref/eio.html#eio_set_max_parallel) —
        Set maximum parallel threads
    -   [eio\_set\_max\_poll\_reqs](/ref/eio.html#eio_set_max_poll_reqs)
        — Set maximum number of requests processed in a poll
    -   [eio\_set\_max\_poll\_time](/ref/eio.html#eio_set_max_poll_time)
        — Set maximum poll time
    -   [eio\_set\_min\_parallel](/ref/eio.html#eio_set_min_parallel) —
        Set minimum parallel thread number
    -   [eio\_stat](/ref/eio.html#eio_stat) — Get file status
    -   [eio\_statvfs](/ref/eio.html#eio_statvfs) — Get file system
        statistics
    -   [eio\_symlink](/ref/eio.html#eio_symlink) — Create a symbolic
        link
    -   [eio\_sync\_file\_range](/ref/eio.html#eio_sync_file_range) —
        Sync a file segment with disk
    -   [eio\_sync](/ref/eio.html#eio_sync) — Commit buffer cache to
        disk
    -   [eio\_syncfs](/ref/eio.html#eio_syncfs) — Calls Linux' syncfs
        syscall, if available
    -   [eio\_truncate](/ref/eio.html#eio_truncate) — Truncate a file
    -   [eio\_unlink](/ref/eio.html#eio_unlink) — Delete a name and
        possibly the file it refers to
    -   [eio\_utime](/ref/eio.html#eio_utime) — Change file last access
        and modification times
    -   [eio\_write](/ref/eio.html#eio_write) — Write to file
