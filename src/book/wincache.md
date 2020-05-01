Windows Cache for PHP
=====================

**目录**

-   [简介](/intro/wincache.html)
-   [安装／配置](/wincache/setup.html)
    -   [需求](/wincache/setup.html#需求)
    -   [安装](/wincache/setup.html#安装)
    -   [运行时配置](/wincache/setup.html#运行时配置)
    -   [WinCache Statistics
        Script](/wincache/setup.html#WinCache%20Statistics%20Script)
    -   [WinCache Session
        Handler](/wincache/setup.html#WinCache%20Session%20Handler)
    -   [WinCache Functions
        Reroutes](/wincache/setup.html#WinCache%20Functions%20Reroutes)
    -   [资源类型](/wincache/setup.html#资源类型)
-   [预定义常量](/wincache/constants.html)
-   [WinCache 函数](/ref/wincache.html)
    -   [wincache\_fcache\_fileinfo](/ref/wincache.html#wincache_fcache_fileinfo)
        — Retrieves information about files cached in the file cache
    -   [wincache\_fcache\_meminfo](/ref/wincache.html#wincache_fcache_meminfo)
        — Retrieves information about file cache memory usage
    -   [wincache\_lock](/ref/wincache.html#wincache_lock) — Acquires an
        exclusive lock on a given key
    -   [wincache\_ocache\_fileinfo](/ref/wincache.html#wincache_ocache_fileinfo)
        — Retrieves information about files cached in the opcode cache
    -   [wincache\_ocache\_meminfo](/ref/wincache.html#wincache_ocache_meminfo)
        — Retrieves information about opcode cache memory usage
    -   [wincache\_refresh\_if\_changed](/ref/wincache.html#wincache_refresh_if_changed)
        — Refreshes the cache entries for the cached files
    -   [wincache\_rplist\_fileinfo](/ref/wincache.html#wincache_rplist_fileinfo)
        — Retrieves information about resolve file path cache
    -   [wincache\_rplist\_meminfo](/ref/wincache.html#wincache_rplist_meminfo)
        — Retrieves information about memory usage by the resolve file
        path cache
    -   [wincache\_scache\_info](/ref/wincache.html#wincache_scache_info)
        — Retrieves information about files cached in the session cache
    -   [wincache\_scache\_meminfo](/ref/wincache.html#wincache_scache_meminfo)
        — Retrieves information about session cache memory usage
    -   [wincache\_ucache\_add](/ref/wincache.html#wincache_ucache_add)
        — Adds a variable in user cache only if variable does not
        already exist in the cache
    -   [wincache\_ucache\_cas](/ref/wincache.html#wincache_ucache_cas)
        — Compares the variable with old value and assigns new value to
        it
    -   [wincache\_ucache\_clear](/ref/wincache.html#wincache_ucache_clear)
        — Deletes entire content of the user cache
    -   [wincache\_ucache\_dec](/ref/wincache.html#wincache_ucache_dec)
        — Decrements the value associated with the key
    -   [wincache\_ucache\_delete](/ref/wincache.html#wincache_ucache_delete)
        — Deletes variables from the user cache
    -   [wincache\_ucache\_exists](/ref/wincache.html#wincache_ucache_exists)
        — Checks if a variable exists in the user cache
    -   [wincache\_ucache\_get](/ref/wincache.html#wincache_ucache_get)
        — Gets a variable stored in the user cache
    -   [wincache\_ucache\_inc](/ref/wincache.html#wincache_ucache_inc)
        — Increments the value associated with the key
    -   [wincache\_ucache\_info](/ref/wincache.html#wincache_ucache_info)
        — Retrieves information about data stored in the user cache
    -   [wincache\_ucache\_meminfo](/ref/wincache.html#wincache_ucache_meminfo)
        — Retrieves information about user cache memory usage
    -   [wincache\_ucache\_set](/ref/wincache.html#wincache_ucache_set)
        — Adds a variable in user cache and overwrites a variable if it
        already exists in the cache
    -   [wincache\_unlock](/ref/wincache.html#wincache_unlock) —
        Releases an exclusive lock on a given key
-   [Building for Windows](/wincache/win32build.html)
    -   [Prerequisites](/wincache/win32build.html#Prerequisites)
    -   [Compiling and
        building](/wincache/win32build.html#Compiling%20and%20building)
    -   [Verifying the
        build](/wincache/win32build.html#Verifying%20the%20build)
