wincache\_fcache\_fileinfo
==========================

Retrieves information about files cached in the file cache

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_fcache\_fileinfo</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$summaryonly`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieves information about file cache content and its usage.

### 参数

`summaryonly`  
Controls whether the returned array will contain information about
individual cache entries along with the file cache summary.

### 返回值

Array of meta data about file cache 或者在失败时返回 **`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *total\_cache\_uptime* - total time in
    seconds that the file cache has been active </span>

-   <span class="simpara"> *total\_file\_count* - total number of files
    that are currently in the file cache </span>

-   <span class="simpara"> *total\_hit\_count* - number of times the
    files have been served from the file cache </span>

-   <span class="simpara"> *total\_miss\_count* - number of times the
    files have not been found in the file cache </span>

-   *file\_entries* - an array that contains the information about all
    the cached files:

    -   <span class="simpara"> *file\_name* - absolute file name of the
        cached file </span>
    -   <span class="simpara"> *add\_time* - time in seconds since the
        file has been added to the file cache </span>
    -   <span class="simpara"> *use\_time* - time in seconds since the
        file has been accessed in the file cache </span>
    -   <span class="simpara"> *last\_check* - time in seconds since the
        file has been checked for modifications </span>
    -   <span class="simpara"> *hit\_count* - number of times the file
        has been served from the cache </span>
    -   <span class="simpara"> *file\_size* - size of the cached file in
        bytes </span>

### 范例

**示例 \#1 A <span class="function">wincache\_fcache\_fileinfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_fcache_fileinfo());
?>
</pre>
```

以上例程会输出：

    Array
    (   [total_cache_uptime] => 3234
        [total_file_count] => 5
        [total_hit_count] => 0
        [total_miss_count] => 1
        [file_entries] => Array
            (
                [1] => Array
                    (
                        [file_name] => c:\inetpub\wwwroot\checkcache.php
                        [add_time] => 1
                        [use_time] => 0
                        [last_check] => 1
                        [hit_count] => 1
                        [file_size] => 2435
                    )
                [2] => Array (...iterates for each cached file)
            )
    )

### 参见

-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_fcache\_meminfo
=========================

Retrieves information about file cache memory usage

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_fcache\_meminfo</span> ( <span
class="methodparam">void</span> )

Retrieves information about memory usage by file cache.

### 返回值

Array of meta data about file cache memory usage 或者在失败时返回
**`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *memory\_total* - amount of memory in bytes
    allocated for the file cache </span>
-   <span class="simpara"> *memory\_free* - amount of free memory in
    bytes available for the file cache </span>
-   <span class="simpara"> *num\_used\_blks* - number of memory blocks
    used by the file cache </span>
-   <span class="simpara"> *num\_free\_blks* - number of free memory
    blocks available for the file cache </span>
-   <span class="simpara"> *memory\_overhead* - amount of memory in
    bytes used for the file cache internal structures </span>

### 范例

**示例 \#1 A <span class="function">wincache\_fcache\_meminfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_fcache_meminfo());
?>
</pre>
```

以上例程会输出：

    Array
    (
        [memory_total] => 134217728
        [memory_free] => 131339120
        [num_used_blks] => 361
        [num_free_blks] => 3
        [memory_overhead] => 5856
    )

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_lock
==============

Acquires an exclusive lock on a given key

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_lock</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$isglobal`<span class="initializer"> = **`FALSE`**</span></span> \] )

Obtains an exclusive lock on a given key. The execution of the current
script will be blocked until the lock can be obtained. Once the lock is
obtained, the other scripts that try to request the lock by using the
same key will be blocked, until the current script releases the lock by
using <span class="function">wincache\_unlock</span>.

**Warning**

Using of the <span class="function">wincache\_lock</span> and <span
class="function">wincache\_unlock</span> can cause deadlocks when
executing PHP scripts in a multi-process environment like FastCGI. Do
not use these functions unless you are absolutely sure you need to use
them. For the majority of the operations on the user cache it is not
necessary to use these functions.

### 参数

`key`  
Name of the key in the cache to get the lock on.

`isglobal`  
Controls whether the scope of the lock is system-wide or local. Local
locks are scoped to the application pool in IIS FastCGI case or to all
php processes that have the same parent process identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Using <span class="function">wincache\_lock</span>**

``` php
<?php
$fp = fopen("/tmp/lock.txt", "r+");
if (wincache_lock(“lock_txt_lock”)) { // do an exclusive lock
    ftruncate($fp, 0); // truncate file
    fwrite($fp, "Write something here\n");
    wincache_unlock(“lock_txt_lock”); // release the lock
} else {
    echo "Couldn't get the lock!";
}
fclose($fp);
?>
```

### 参见

-   <span class="function">wincache\_unlock</span>
-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>

wincache\_ocache\_fileinfo
==========================

Retrieves information about files cached in the opcode cache

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_ocache\_fileinfo</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$summaryonly`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieves information about opcode cache content and its usage.

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 参数

`summaryonly`  
Controls whether the returned array will contain information about
individual cache entries along with the opcode cache summary.

### 返回值

Array of meta data about opcode cache 或者在失败时返回 **`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *total\_cache\_uptime* - total time in
    seconds that the opcode cache has been active </span>

-   <span class="simpara"> *total\_file\_count* - total number of files
    that are currently in the opcode cache </span>

-   <span class="simpara"> *total\_hit\_count* - number of times the
    compiled opcode have been served from the cache </span>

-   <span class="simpara"> *total\_miss\_count* - number of times the
    compiled opcode have not been found in the cache </span>

-   <span class="simpara"> *is\_local\_cache* - true is the cache
    metadata is for a local cache instance, false if the metadata is for
    the global cache </span>

-   *file\_entries* - an array that contains the information about all
    the cached files:

    -   <span class="simpara"> *file\_name* - absolute file name of the
        cached file </span>
    -   <span class="simpara"> *add\_time* - time in seconds since the
        file has been added to the opcode cache </span>
    -   <span class="simpara"> *use\_time* - time in seconds since the
        file has been accessed in the opcode cache </span>
    -   <span class="simpara"> *last\_check* - time in seconds since the
        file has been checked for modifications </span>
    -   <span class="simpara"> *hit\_count* - number of times the file
        has been served from the cache </span>
    -   <span class="simpara"> *function\_count* - number of functions
        in the cached file </span>
    -   <span class="simpara"> *class\_count* - number of classes in the
        cached file </span>

### 范例

**示例 \#1 A <span class="function">wincache\_ocache\_fileinfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_ocache_fileinfo());
?>
</pre>
```

以上例程会输出：

    Array
    (
        [total_cache_uptime] => 17357
        [total_file_count] => 121
        [total_hit_count] => 36562
        [total_miss_count] => 201
        [file_entries] => Array
            (
                [1] => Array
                    (
                        [file_name] => c:\inetpub\wwwroot\checkcache.php
                        [add_time] => 17356
                        [use_time] => 7
                        [last_check] => 10
                        [hit_count] => 454
                        [function_count] => 0
                        [class_count] => 1
                    )
                [2] => Array (...iterates for each cached file)
            )
    )

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_ocache\_meminfo
=========================

Retrieves information about opcode cache memory usage

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_ocache\_meminfo</span> ( <span
class="methodparam">void</span> )

Retrieves information about memory usage by opcode cache.

### 返回值

Array of meta data about opcode cache memory usage 或者在失败时返回
**`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *memory\_total* - amount of memory in bytes
    allocated for the opcode cache </span>
-   <span class="simpara"> *memory\_free* - amount of free memory in
    bytes available for the opcode cache </span>
-   <span class="simpara"> *num\_used\_blks* - number of memory blocks
    used by the opcode cache </span>
-   <span class="simpara"> *num\_free\_blks* - number of free memory
    blocks available for the opcode cache </span>
-   <span class="simpara"> *memory\_overhead* - amount of memory in
    bytes used for the opcode cache internal structures </span>

**Warning**

This function was *REMOVED* in PHP 7.0.0.

### 范例

**示例 \#1 A <span class="function">wincache\_ocache\_meminfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_ocache_meminfo());
?>
</pre>
```

以上例程会输出：

    Array
    (
        [memory_total] => 134217728
        [memory_free] => 112106972
        [num_used_blks] => 15469
        [num_free_blks] => 4
        [memory_overhead] => 247600
    )

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_refresh\_if\_changed
==============================

Refreshes the cache entries for the cached files

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_refresh\_if\_changed</span> (\[ <span
class="methodparam"><span class="type">array</span> `$files`<span
class="initializer"> = NULL</span></span> \] )

Refreshes the cache entries for the files, whose names were passed in
the input argument. If no argument is specified then refreshes all the
entries in the cache.

### 参数

`files`  
An array of file names for files that need to be refreshed. An absolute
or relative file paths can be used.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

WinCache performs regular checks on the cached files to ensure that if
any file has changed then the corresponding entry in the cache is
updated. By default this check is performed every 30 seconds. If, for
example, a PHP script updates another PHP script where the application's
configuration settings are stored, then it may happen that after the
configuration settings have been saved to a file, the application is
still using old settings for some time until the cache is refreshed. In
those cases it may be preferrable to refresh the cache right after the
file has been changed. The following example shows how this can be done.

**示例 \#1 A <span
class="function">wincache\_refresh\_if\_changed</span> example**

``` php
<?php 
$filename = 'C:\inetpub\wwwroot\config.php';
$handle = fopen($filename, 'w+');
if ($handle === FALSE) die('Failed to open file '.$filename.' for writing');
fwrite($handle, '<?php $setting=something; ?>');
fclose($handle);
wincache_refresh_if_changed(array($filename));
?>
```

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>

wincache\_rplist\_fileinfo
==========================

Retrieves information about resolve file path cache

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_rplist\_fileinfo</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$summaryonly`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieves information about cached mappings between relative file paths
and corresponding absolute file paths.

### 返回值

Array of meta data about the resolve file path cache 或者在失败时返回
**`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *total\_file\_count* - total number of file
    path mappings stored in the cache </span>

-   *rplist\_entries* - an array that contains the information about all
    the cached file paths:

    -   <span class="simpara"> *resolve\_path* - path to a file </span>
    -   <span class="simpara"> *subkey\_data* - corresponding absolute
        path to a file </span>

### 范例

**示例 \#1 A <span class="function">wincache\_rplist\_fileinfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_rplist_fileinfo());
?>
</pre>
```

以上例程会输出：

    Array
    (
        [total_file_count] => 5
        [rplist_entries] => Array
            (
                [1] => Array
                    (
                        [resolve_path] => checkcache.php
                        [subkey_data] => c:\inetpub\wwwroot|c:\inetpub\wwwroot\checkcache.php
                    )

                [2] => Array (...iterates for each cached file)
            )
    )

### 参见

-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_rplist\_meminfo
=========================

Retrieves information about memory usage by the resolve file path cache

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_rplist\_meminfo</span> ( <span
class="methodparam">void</span> )

Retrieves information about memory usage by resolve file path cache.

### 返回值

Array of meta data that describes memory usage by resolve file path
cache. 或者在失败时返回 **`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *memory\_total* - amount of memory in bytes
    allocated for the resolve file path cache </span>
-   <span class="simpara"> *memory\_free* - amount of free memory in
    bytes available for the resolve file path cache </span>
-   <span class="simpara"> *num\_used\_blks* - number of memory blocks
    used by the resolve file path cache </span>
-   <span class="simpara"> *num\_free\_blks* - number of free memory
    blocks available for the resolve file path cache </span>
-   <span class="simpara"> *memory\_overhead* - amount of memory in
    bytes used for the internal structures of resolve file path cache
    </span>

### 范例

**示例 \#1 A <span class="function">wincache\_rplist\_meminfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_rplist_meminfo());
?>
</pre>
```

以上例程会输出：

    Array
    (
        [memory_total] => 9437184
        [memory_free] => 9416744
        [num_used_blks] => 23
        [num_free_blks] => 1
        [memory_overhead] => 416
    )

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_scache\_info
======================

Retrieves information about files cached in the session cache

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_scache\_info</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$summaryonly`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieves information about session cache content and its usage.

### 参数

`summaryonly`  
Controls whether the returned array will contain information about
individual cache entries along with the session cache summary.

### 返回值

Array of meta data about session cache 或者在失败时返回 **`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *total\_cache\_uptime* - total time in
    seconds that the session cache has been active </span>

-   <span class="simpara"> *total\_item\_count* - total number of
    elements that are currently in the session cache </span>

-   <span class="simpara"> *is\_local\_cache* - true is the cache
    metadata is for a local cache instance, false if the metadata is for
    the global cache </span>

-   <span class="simpara"> *total\_hit\_count* - number of times the
    data has been served from the cache </span>

-   <span class="simpara"> *total\_miss\_count* - number of times the
    data has not been found in the cache </span>

-   *scache\_entries* - an array that contains the information about all
    the cached items:

    -   <span class="simpara"> *key\_name* - name of the key which is
        used to store the data </span>
    -   <span class="simpara"> *value\_type* - type of value stored by
        the key </span>
    -   <span class="simpara"> *use\_time* - time in seconds since the
        file has been accessed in the opcode cache </span>
    -   <span class="simpara"> *last\_check* - time in seconds since the
        file has been checked for modifications </span>
    -   <span class="simpara"> *ttl\_seconds* - time remaining for the
        data to live in the cache, 0 meaning infinite </span>
    -   <span class="simpara"> *age\_seconds* - time elapsed from the
        time data has been added in the cache </span>
    -   <span class="simpara"> *hitcount* - number of times data has
        been served from the cache </span>

### 范例

**示例 \#1 A <span class="function">wincache\_scache\_info</span>
example**

``` php
<pre>
<?php
print_r(wincache_scache_info());
?>
</pre>
```

以上例程会输出：

    Array
    (
        [total_cache_uptime] => 17357
        [total_file_count] => 121
        [total_hit_count] => 36562
        [total_miss_count] => 201
        [scache_entries] => Array
            (
                [1] => Array
                    (
                        [file_name] => c:\inetpub\wwwroot\checkcache.php
                        [add_time] => 17356
                        [use_time] => 7
                        [last_check] => 10
                        [hit_count] => 454
                        [function_count] => 0
                        [class_count] => 1
                    )
                [2] => Array (...iterates for each cached file)
            )
    )

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_scache\_meminfo
=========================

Retrieves information about session cache memory usage

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_scache\_meminfo</span> ( <span
class="methodparam">void</span> )

Retrieves information about memory usage by session cache.

### 返回值

Array of meta data about session cache memory usage 或者在失败时返回
**`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *memory\_total* - amount of memory in bytes
    allocated for the session cache </span>
-   <span class="simpara"> *memory\_free* - amount of free memory in
    bytes available for the session cache </span>
-   <span class="simpara"> *num\_used\_blks* - number of memory blocks
    used by the session cache </span>
-   <span class="simpara"> *num\_free\_blks* - number of free memory
    blocks available for the session cache </span>
-   <span class="simpara"> *memory\_overhead* - amount of memory in
    bytes used for the session cache internal structures </span>

### 范例

**示例 \#1 A <span class="function">wincache\_scache\_meminfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_scache_meminfo());
?>
</pre>
```

以上例程会输出：

    Array 
    ( 
        [memory_total] => 5242880 
        [memory_free] => 5215056 
        [num_used_blks] => 6 
        [num_free_blks] => 3 
        [memory_overhead] => 176
    ) 

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>

wincache\_ucache\_add
=====================

Adds a variable in user cache only if variable does not already exist in
the cache

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_add</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$ttl`<span class="initializer"> =
0</span></span> \] )

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_add</span> ( <span
class="methodparam"><span class="type">array</span> `$values`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$unused`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \]\] )

Adds a variable in user cache, only if this variable doesn't already
exist in the cache. The added variable remains in the user cache unless
its time to live expires or it is deleted by using <span
class="function">wincache\_ucache\_delete</span> or <span
class="function">wincache\_ucache\_clear</span> functions.

### 参数

`key`  
Store the variable using this `key` name. If a variable with same key is
already present the function will fail and return **`FALSE`**. `key` is
case sensitive. To override the value even if `key` is present use <span
class="function">wincache\_ucache\_set</span> function instad. `key` can
also take array of name =\> value pairs where names will be used as
keys. This can be used to add multiple values in the cache in one
operation, thus avoiding race condition.

`value`  
Value of a variable to store. `Value` supports all data types except
resources, such as file handles. This paramter is ignored if first
argument is an array. A general guidance is to pass **`NULL`** as
`value` while using array as `key`. If `value` is an object, or an array
containing objects, then the objects will be serialized. See
<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
for details on serializing objects.

`values`  
Associative array of keys and values.

`ttl`  
Time for the variable to live in the cache in seconds. After the value
specified in `ttl` has passed the stored variable will be deleted from
the cache. This parameter takes a default value of *0* which means the
variable will stay in the cache unless explicitly deleted by using <span
class="function">wincache\_ucache\_delete</span> or <span
class="function">wincache\_ucache\_clear</span> functions.

### 返回值

If `key` is string, the function returns **`TRUE`** on success and
**`FALSE`** on failure.

If `key` is an array, the function returns:

-   <span class="simpara"> If all the name =\> value pairs in the array
    can be set, function returns an empty array; </span>
-   <span class="simpara"> If all the name =\> value pairs in the array
    cannot be set, function returns **`FALSE`**; </span>
-   <span class="simpara"> If some can be set while others cannot,
    function returns an array with name=\>value pair for which the
    addition failed in the user cache. </span>

### 范例

**示例 \#1 <span class="function">wincache\_ucache\_add</span> with
`key` as a string**

``` php
<?php
$bar = 'BAR';
var_dump(wincache_ucache_add('foo', $bar));
var_dump(wincache_ucache_add('foo', $bar));
var_dump(wincache_ucache_get('foo'));
?>
```

以上例程会输出：

    bool(true)
    bool(false)
    string(3) "BAR" 

**示例 \#2 <span class="function">wincache\_ucache\_add</span> with
`key` as an array**

``` php
<?php
$colors_array = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
var_dump(wincache_ucache_add($colors_array));
var_dump(wincache_ucache_add($colors_array));
var_dump(wincache_ucache_get('Blue'));
?>
```

以上例程会输出：

    array(0) { } 
    array(4) { 
      ["green"]=> int(-1) 
      ["Blue"]=> int(-1) 
      ["yellow"]=> int(-1) 
      ["cyan"]=> int(-1) 
    } 
    string(1) "6"

### 参见

-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>

wincache\_ucache\_cas
=====================

Compares the variable with old value and assigns new value to it

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_cas</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">int</span>
`$old_value`</span> , <span class="methodparam"><span
class="type">int</span> `$new_value`</span> )

Compares the variable associated with the `key` with `old_value` and if
it matches then assigns the `new_value` to it.

### 参数

`key`  
The `key` that is used to store the variable in the cache. `key` is case
sensitive.

`old_value`  
Old value of the variable pointed by `key` in the user cache. The value
should be of type *long*, otherwise the function returns **`FALSE`**.

`new_value`  
New value which will get assigned to variable pointer by `key` if a
match is found. The value should be of type *long*, otherwise the
function returns **`FALSE`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Using <span class="function">wincache\_ucache\_cas</span>**

``` php
<?php
wincache_ucache_set('counter', 2922);
var_dump(wincache_ucache_cas('counter', 2922, 1));
var_dump(wincache_ucache_get('counter'));
?>
```

以上例程会输出：

    bool(true) 
    int(1)

### 参见

-   <span class="function">wincache\_ucache\_inc</span>
-   <span class="function">wincache\_ucache\_dec</span>

wincache\_ucache\_clear
=======================

Deletes entire content of the user cache

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_clear</span> ( <span
class="methodparam">void</span> )

Clears/deletes all the values stored in the user cache.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 using <span class="function">wincache\_ucache\_clear</span>**

``` php
<?php
wincache_ucache_set('green', 1);
wincache_ucache_set('red', 2);
wincache_ucache_set('orange', 4);
wincache_ucache_set('blue', 8);
wincache_ucache_set('cyan', 16);
$array1 = array('green', 'red', 'orange', 'blue', 'cyan');
var_dump(wincache_ucache_get($array1));
var_dump(wincache_ucache_clear());
var_dump(wincache_ucache_get($array1));
?>
```

以上例程会输出：

    array(5) { ["green"]=> int(1) 
               ["red"]=> int(2) 
               ["orange"]=> int(4) 
               ["blue"]=> int(8) 
               ["cyan"]=> int(16) } 
    bool(true) 
    bool(false) 

### 参见

-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_add</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>

wincache\_ucache\_dec
=====================

Decrements the value associated with the key

### 说明

<span class="type">mixed</span> <span
class="methodname">wincache\_ucache\_dec</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$dec_by`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `&$success`</span>
\]\] )

Decrements the value associated with the `key` by 1 or as specified by
`dec_by`.

### 参数

`key`  
The `key` that was used to store the variable in the cache. `key` is
case sensitive.

`dec_by`  
The value by which the variable associated with the `key` will get
decremented. If the argument is a floating point number it will be
truncated to nearest integer. The variable associated with the `key`
should be of type *long*, otherwise the function fails and returns
**`FALSE`**.

`success`  
Will be set to **`TRUE`** on success and **`FALSE`** on failure.

### 返回值

Returns the decremented value on success and **`FALSE`** on failure.

### 范例

**示例 \#1 Using <span class="function">wincache\_ucache\_dec</span>**

``` php
<?php
wincache_ucache_set('counter', 1);
var_dump(wincache_ucache_dec('counter', 2923, $success));
var_dump($success);
?>
```

以上例程会输出：

    int(2922) 
    bool(true)

### 参见

-   <span class="function">wincache\_ucache\_inc</span>
-   <span class="function">wincache\_ucache\_cas</span>

wincache\_ucache\_delete
========================

Deletes variables from the user cache

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_delete</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> )

Deletes the elements in the user cache pointed by `key`.

### 参数

`key`  
The `key` that was used to store the variable in the cache. `key` is
case sensitive. `key` can be an array of keys.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

If `key` is an array then the function returns **`FALSE`** if every
element of the array fails to get deleted from the user cache, otherwise
returns an array which consists of all the keys that are deleted.

### 范例

**示例 \#1 Using <span class="function">wincache\_ucache\_delete</span>
with `key` as a string**

``` php
<?php
wincache_ucache_set('foo', 'bar');
var_dump(wincache_ucache_delete('foo'));
var_dump(wincache_ucache_exists('foo'));
?>
```

以上例程会输出：

    bool(true)
    bool(false)

**示例 \#2 Using<span class="function">wincache\_ucache\_delete</span>
with `key` as an array**

``` php
<?php
$array1 = array('green' => '5', 'blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('green', 'blue', 'yellow', 'cyan');
var_dump(wincache_ucache_delete($array2));
?>
```

以上例程会输出：

    array(4) { [0]=> string(5) "green" 
               [1]=> string(4) "Blue" 
               [2]=> string(6) "yellow" 
               [3]=> string(4) "cyan" } 

**示例 \#3 Using <span class="function">wincache\_ucache\_delete</span>
with `key` as an array where some elements cannot be deleted**

``` php
<?php
$array1 = array('green' => '5', 'blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('orange', 'red', 'yellow', 'cyan');
var_dump(wincache_ucache_delete($array2));
?>
```

以上例程会输出：

    array(2) { [0]=> string(6) "yellow" 
               [1]=> string(4) "cyan" }

### 参见

-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_add</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>

wincache\_ucache\_exists
========================

Checks if a variable exists in the user cache

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_exists</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Checks if a variable with the `key` exists in the user cache or not.

### 参数

`key`  
The `key` that was used to store the variable in the cache. `key` is
case sensitive.

### 返回值

Returns **`TRUE`** if variable with the `key` exitsts, otherwise returns
**`FALSE`**.

### 范例

**示例 \#1 Using <span
class="function">wincache\_ucache\_exists</span>**

``` php
<?php
if (!wincache_ucache_exists('green'))
    wincache_ucache_set('green', 1);
var_dump(wincache_ucache_exists('green'));
?>
```

以上例程会输出：

    bool(true)

### 参见

-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_add</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>

wincache\_ucache\_get
=====================

Gets a variable stored in the user cache

### 说明

<span class="type">mixed</span> <span
class="methodname">wincache\_ucache\_get</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`&$success`</span> \] )

Gets a variable stored in the user cache.

### 参数

`key`  
The `key` that was used to store the variable in the cache. `key` is
case sensitive. `key` can be an array of keys. In this case the return
value will be an array of values of each element in the `key` array. If
an object, or an array containing objects, is returned, then the objects
will be unserialized. See
<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
for details on unserializing objects.

`success`  
Will be set to **`TRUE`** on success and **`FALSE`** on failure.

### 返回值

If `key` is a string, the function returns the value of the variable
stored with that key. The `success` is set to **`TRUE`** on success and
to **`FALSE`** on failure.

The `key` is an array, the parameter `success` is always set to
**`TRUE`**. The returned array (name =\> value pairs) will contain only
those name =\> value pairs for which the get operation in user cache was
successful. If none of the keys in the key array finds a match in the
user cache an empty array will be returned.

### 范例

**示例 \#1 <span class="function">wincache\_ucache\_get</span> with
`key` as a string**

``` php
<?php
wincache_ucache_add('color', 'blue');
var_dump(wincache_ucache_get('color', $success));
var_dump($success);
?>
```

以上例程会输出：

    string(4) "blue"
    bool(true)

**示例 \#2 <span class="function">wincache\_ucache\_get</span> with
`key` as an array**

``` php
<?php
$array1 = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
wincache_ucache_set($array1);
$array2 = array('green', 'Blue', 'yellow', 'cyan');
var_dump(wincache_ucache_get($array2, $success));
var_dump($success);
?>
```

以上例程会输出：

    array(4) { ["green"]=> string(1) "5" 
               ["Blue"]=> string(1) "6" 
               ["yellow"]=> string(1) "7" 
               ["cyan"]=> string(1) "8" } 
    bool(true) 

### 参见

-   <span class="function">wincache\_ucache\_add</span>
-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>

wincache\_ucache\_inc
=====================

Increments the value associated with the key

### 说明

<span class="type">mixed</span> <span
class="methodname">wincache\_ucache\_inc</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">int</span> `$inc_by`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `&$success`</span>
\]\] )

Increments the value associated with the `key` by 1 or as specified by
`inc_by`.

### 参数

`key`  
The `key` that was used to store the variable in the cache. `key` is
case sensitive.

`inc_by`  
The value by which the variable associated with the `key` will get
incremented. If the argument is a floating point number it will be
truncated to nearest integer. The variable associated with the `key`
should be of type *long*, otherwise the function fails and returns
**`FALSE`**.

`success`  
Will be set to **`TRUE`** on success and **`FALSE`** on failure.

### 返回值

Returns the incremented value on success and **`FALSE`** on failure.

### 范例

**示例 \#1 Using <span class="function">wincache\_ucache\_inc</span>**

``` php
<?php
wincache_ucache_set('counter', 1);
var_dump(wincache_ucache_inc('counter', 2921, $success));
var_dump($success);
?>
```

以上例程会输出：

    int(2922) 
    bool(true)

### 参见

-   <span class="function">wincache\_ucache\_dec</span>
-   <span class="function">wincache\_ucache\_cas</span>

wincache\_ucache\_info
======================

Retrieves information about data stored in the user cache

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_ucache\_info</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$summaryonly`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$key`<span
class="initializer"> = NULL</span></span> \]\] )

Retrieves information about data stored in the user cache.

### 参数

`summaryonly`  
Controls whether the returned array will contain information about
individual cache entries along with the user cache summary.

`key`  
The key of an entry in the user cache. If specified then the returned
array will contain information only about that cache entry. If not
specified and `summaryonly` is set to **`FALSE`** then the returned
array will contain information about all entries in the cache.

### 返回值

Array of meta data about user cache 或者在失败时返回 **`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *total\_cache\_uptime* - total time in
    seconds that the user cache has been active </span>

-   <span class="simpara"> *total\_item\_count* - total number of
    elements that are currently in the user cache </span>

-   <span class="simpara"> *is\_local\_cache* - true is the cache
    metadata is for a local cache instance, false if the metadata is for
    the global cache </span>

-   <span class="simpara"> *total\_hit\_count* - number of times the
    data has been served from the cache </span>

-   <span class="simpara"> *total\_miss\_count* - number of times the
    data has not been found in the cache </span>

-   *ucache\_entries* - an array that contains the information about all
    the cached items:

    -   <span class="simpara"> *key\_name* - name of the key which is
        used to store the data </span>
    -   <span class="simpara"> *value\_type* - type of value stored by
        the key </span>
    -   <span class="simpara"> *use\_time* - time in seconds since the
        file has been accessed in the opcode cache </span>
    -   <span class="simpara"> *last\_check* - time in seconds since the
        file has been checked for modifications </span>
    -   <span class="simpara"> *is\_session* - indicates if the data is
        a session variable </span>
    -   <span class="simpara"> *ttl\_seconds* - time remaining for the
        data to live in the cache, 0 meaning infinite </span>
    -   <span class="simpara"> *age\_seconds* - time elapsed from the
        time data has been added in the cache </span>
    -   <span class="simpara"> *hitcount* - number of times data has
        been served from the cache </span>

### 范例

**示例 \#1 Using <span class="function">wincache\_ucache\_info</span>**

``` php
<?php
wincache_ucache_get('green');
wincache_ucache_set('green', 2922);
wincache_ucache_get('green');
wincache_ucache_get('green');
wincache_ucache_get('green');
print_r(wincache_ucache_info());
?>
```

以上例程会输出：

    Array 
    ( ["total_cache_uptime"] => int(0)
      ["is_local_cache"] => bool(false)
      ["total_item_count"] => int(1) 
      ["total_hit_count"] => int(3) 
      ["total_miss_count"] => int(1) 
      ["ucache_entries"] => Array(1) 
        ( [1] => Array(6)
          ( 
            ["key_name"] => string(5) "green"
            ["value_type"] => string(4) "long" 
            ["is_session"] => int(0) 
            ["ttl_seconds"] => int(0)
            ["age_seconds"] => int(0)
            ["hitcount"] => int(3) 
           ) 
        ) 
    )

### 参见

-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_ocache\_meminfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_ucache\_meminfo
=========================

Retrieves information about user cache memory usage

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">wincache\_ucache\_meminfo</span> ( <span
class="methodparam">void</span> )

Retrieves information about memory usage by user cache.

### 返回值

Array of meta data about user cache memory usage 或者在失败时返回
**`FALSE`**

The array returned by this function contains the following elements:

-   <span class="simpara"> *memory\_total* - amount of memory in bytes
    allocated for the user cache </span>
-   <span class="simpara"> *memory\_free* - amount of free memory in
    bytes available for the user cache </span>
-   <span class="simpara"> *num\_used\_blks* - number of memory blocks
    used by the user cache </span>
-   <span class="simpara"> *num\_free\_blks* - number of free memory
    blocks available for the user cache </span>
-   <span class="simpara"> *memory\_overhead* - amount of memory in
    bytes used for the user cache internal structures </span>

### 范例

**示例 \#1 A <span class="function">wincache\_ucache\_meminfo</span>
example**

``` php
<pre>
<?php
print_r(wincache_ucache_meminfo());
?>
</pre>
```

以上例程会输出：

    Array 
    ( 
        [memory_total] => 5242880 
        [memory_free] => 5215056 
        [num_used_blks] => 6 
        [num_free_blks] => 3 
        [memory_overhead] => 176
    ) 

### 参见

-   <span class="function">wincache\_fcache\_fileinfo</span>
-   <span class="function">wincache\_fcache\_meminfo</span>
-   <span class="function">wincache\_ocache\_fileinfo</span>
-   <span class="function">wincache\_rplist\_fileinfo</span>
-   <span class="function">wincache\_rplist\_meminfo</span>
-   <span class="function">wincache\_refresh\_if\_changed</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>
-   <span class="function">wincache\_scache\_meminfo</span>

wincache\_ucache\_set
=====================

Adds a variable in user cache and overwrites a variable if it already
exists in the cache

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_set</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$ttl`<span class="initializer"> =
0</span></span> \] )

<span class="type">bool</span> <span
class="methodname">wincache\_ucache\_set</span> ( <span
class="methodparam"><span class="type">array</span> `$values`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$unused`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \]\] )

Adds a variable in user cache. Overwrites a variable if it already
exists in the cache. The added or updated variable remains in the user
cache unless its time to live expires or it is deleted by using <span
class="function">wincache\_ucache\_delete</span> or <span
class="function">wincache\_ucache\_clear</span> functions.

### 参数

`key`  
Store the variable using this `key` name. If a variable with same `key`
is already present the function will overwrite the previous value with
the new one. `key` is case sensitive. `key` can also take array of name
=\> value pairs where names will be used as keys. This can be used to
add multiple values in the cache in one operation, thus avoiding race
condition.

`value`  
Value of a variable to store. `Value` supports all data types except
resources, such as file handles. This paramter is ignored if first
argument is an array. A general guidance is to pass **`NULL`** as
`value` while using array as `key`. If `value` is an object, or an array
containing objects, then the objects will be serialized. See
<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
for details on serializing objects.

`values`  
Associative array of keys and values.

`ttl`  
Time for the variable to live in the cache in seconds. After the value
specified in `ttl` has passed the stored variable will be deleted from
the cache. This parameter takes a default value of *0* which means the
variable will stay in the cache unless explicitly deleted by using <span
class="function">wincache\_ucache\_delete</span> or <span
class="function">wincache\_ucache\_clear</span> functions.

### 返回值

If `key` is string, the function returns **`TRUE`** on success and
**`FALSE`** on failure.

If `key` is an array, the function returns:

-   <span class="simpara"> If all the name =\> value pairs in the array
    can be set, function returns an empty array; </span>
-   <span class="simpara"> If all the name =\> value pairs in the array
    cannot be set, function returns **`FALSE`**; </span>
-   <span class="simpara"> If some can be set while others cannot,
    function returns an array with name=\>value pair for which the
    addition failed in the user cache. </span>

### 范例

**示例 \#1 <span class="function">wincache\_ucache\_set</span> with
`key` as a string**

``` php
<?php
$bar = 'BAR';
var_dump(wincache_ucache_set('foo', $bar));
var_dump(wincache_ucache_get('foo'));
$bar1 = 'BAR1';
var_dump(wincache_ucache_set('foo', $bar1));
var_dump(wincache_ucache_get('foo'));
?>
```

以上例程会输出：

    bool(true)
    string(3) "BAR"
    bool(true)
    string(3) "BAR1"

**示例 \#2 <span class="function">wincache\_ucache\_set</span> with
`key` as an array**

``` php
<?php
$colors_array = array('green' => '5', 'Blue' => '6', 'yellow' => '7', 'cyan' => '8');
var_dump(wincache_ucache_set($colors_array));
var_dump(wincache_ucache_set($colors_array));
var_dump(wincache_ucache_get('Blue'));
?>
```

以上例程会输出：

    array(0) {}
    array(0) {}
    string(1) "6"

### 参见

-   <span class="function">wincache\_ucache\_add</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>

wincache\_unlock
================

Releases an exclusive lock on a given key

### 说明

<span class="type">bool</span> <span
class="methodname">wincache\_unlock</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Releases an exclusive lock that was obtained on a given key by using
<span class="function">wincache\_lock</span>. If any other process was
blocked waiting for the lock on this key, that process will be able to
obtain the lock.

**Warning**

Using of the <span class="function">wincache\_lock</span> and <span
class="function">wincache\_unlock</span> can cause deadlocks when
executing PHP scripts in a multi-process environment like FastCGI. Do
not use these functions unless you are absolutely sure you need to use
them. For the majority of the operations on the user cache it is not
necessary to use these functions.

### 参数

`key`  
Name of the key in the cache to release the lock on.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Using <span class="function">wincache\_unlock</span>**

``` php
<?php
$fp = fopen("/tmp/lock.txt", "r+");
if (wincache_lock(“lock_txt_lock”)) { // do an exclusive lock
    ftruncate($fp, 0); // truncate file
    fwrite($fp, "Write something here\n");
    wincache_unlock(“lock_txt_lock”); // release the lock
} else {
    echo "Couldn't get the lock!";
}
fclose($fp);
?>
```

### 参见

-   <span class="function">wincache\_lock</span>
-   <span class="function">wincache\_ucache\_set</span>
-   <span class="function">wincache\_ucache\_get</span>
-   <span class="function">wincache\_ucache\_delete</span>
-   <span class="function">wincache\_ucache\_clear</span>
-   <span class="function">wincache\_ucache\_exists</span>
-   <span class="function">wincache\_ucache\_meminfo</span>
-   <span class="function">wincache\_ucache\_info</span>
-   <span class="function">wincache\_scache\_info</span>

**目录**

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
    — Retrieves information about memory usage by the resolve file path
    cache
-   [wincache\_scache\_info](/ref/wincache.html#wincache_scache_info) —
    Retrieves information about files cached in the session cache
-   [wincache\_scache\_meminfo](/ref/wincache.html#wincache_scache_meminfo)
    — Retrieves information about session cache memory usage
-   [wincache\_ucache\_add](/ref/wincache.html#wincache_ucache_add) —
    Adds a variable in user cache only if variable does not already
    exist in the cache
-   [wincache\_ucache\_cas](/ref/wincache.html#wincache_ucache_cas) —
    Compares the variable with old value and assigns new value to it
-   [wincache\_ucache\_clear](/ref/wincache.html#wincache_ucache_clear)
    — Deletes entire content of the user cache
-   [wincache\_ucache\_dec](/ref/wincache.html#wincache_ucache_dec) —
    Decrements the value associated with the key
-   [wincache\_ucache\_delete](/ref/wincache.html#wincache_ucache_delete)
    — Deletes variables from the user cache
-   [wincache\_ucache\_exists](/ref/wincache.html#wincache_ucache_exists)
    — Checks if a variable exists in the user cache
-   [wincache\_ucache\_get](/ref/wincache.html#wincache_ucache_get) —
    Gets a variable stored in the user cache
-   [wincache\_ucache\_inc](/ref/wincache.html#wincache_ucache_inc) —
    Increments the value associated with the key
-   [wincache\_ucache\_info](/ref/wincache.html#wincache_ucache_info) —
    Retrieves information about data stored in the user cache
-   [wincache\_ucache\_meminfo](/ref/wincache.html#wincache_ucache_meminfo)
    — Retrieves information about user cache memory usage
-   [wincache\_ucache\_set](/ref/wincache.html#wincache_ucache_set) —
    Adds a variable in user cache and overwrites a variable if it
    already exists in the cache
-   [wincache\_unlock](/ref/wincache.html#wincache_unlock) — Releases an
    exclusive lock on a given key
