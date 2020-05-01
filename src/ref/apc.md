apc\_add
========

缓存一个变量到数据存储

### 说明

<span class="type">bool</span> <span class="methodname">apc\_add</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> , <span class="methodparam"><span
class="type">mixed</span> `$var`</span> \[, <span
class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \] )

<span class="type">array</span> <span class="methodname">apc\_add</span>
( <span class="methodparam"><span class="type">array</span>
`$values`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$unused`<span class="initializer"> =
NULL</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$ttl`<span class="initializer"> =
0</span></span> \]\] )

仅仅在缓存变量不存在的情况下缓存变量到数据存储中

> **Note**: <span class="simpara"> 与PHP中其他的机制不同，使用<span
> class="function">apc\_add</span> 存储变量
> 在不同的请求之间一直持久存在（直到从缓存系统中移除） </span>

### 参数

`key`  
存储缓存变量使用的名称`key`s 是唯一的， 所以试图使用 <span
class="function">apc\_add</span> 去添加一个名称已经存在的缓存，
将不会覆盖现有的缓存的值, 并且返回 **`FALSE`**. (这个是 <span
class="function">apc\_add</span> 和 <span
class="function">apc\_store</span>之间唯一的不同.)

`var`  
存储的变量

`ttl`  
生存时间;在缓存中存储`var`共`ttl`秒,
在`ttl`秒过去后,存储的变量将会从缓存中擦除(在下一次请求时),
如果没有设置`ttl`(或者`ttl`是*0*),
变量将一直存活到被手动移除为止,除此之外不在缓存中的可能原因是，缓存系统使用clear，或者restart等

`values`  
Names in key, variables in value.

### 返回值

Returns TRUE if something has effectively been added into the cache,
FALSE otherwise. Second syntax returns array with error keys.

### 范例

**示例 \#1 <span class="function">apc\_add</span> 例子**

``` php
<?php
$bar = 'BAR';
apc_add('foo', $bar);
var_dump(apc_fetch('foo'));
echo "\n";
$bar = 'NEVER GETS SET';
apc_add('foo', $bar);
var_dump(apc_fetch('foo'));
echo "\n";
?>
```

以上例程会输出：

    string(3) "BAR"
    string(3) "BAR"

### 参见

-   <span class="function">apc\_store</span>
-   <span class="function">apc\_fetch</span>
-   <span class="function">apc\_delete</span>

apc\_bin\_dump
==============

获取给定文件和变量的二进制文件转储。

### 说明

<span class="type">string</span> <span
class="methodname">apc\_bin\_dump</span> (\[ <span
class="methodparam"><span class="type">array</span> `$files`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$user_vars`<span
class="initializer"> = NULL</span></span> \]\] )

从 APC 缓存中返回给定文件和用户变量的二进制打印。 一个 **`NULL`**
给文件或者用户变量符号表示每个条目的打印，而
array（）则不会转储任何内容。

### 参数

`files`  
文件，在 **`NULL`**传入<span class="function">array</span>
时传递每个条目的转储都不会转储任何内容。

`user_vars`  
用户变量，在**`NULL`**传入<span
class="function">array</span>时传递每个条目的转储信号都不会转储任何内容。

### 返回值

**`FALSE`** 如果 APC 未启用，或者**`NULL`** 遇到未知错误，则返回 APC
缓存中给定文件和用户变量的二进制转储。

### 参见

-   <span class="function">apc\_bin\_dumpfile</span>
-   <span class="function">apc\_bin\_load</span>

apc\_bin\_dumpfile
==================

Output a binary dump of cached files and user variables to a file

### 说明

<span class="type">int</span> <span
class="methodname">apc\_bin\_dumpfile</span> ( <span
class="methodparam"><span class="type">array</span> `$files`</span> ,
<span class="methodparam"><span class="type">array</span>
`$user_vars`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`<span
class="initializer"> = NULL</span></span> \]\] )

Outputs a binary dump of the given files and user variables from the APC
cache to the named file.

### 参数

`files`  
The file names being dumped.

`user_vars`  
The user variables being dumped.

`filename`  
The filename where the dump is being saved.

`flags`  
Flags passed to the `filename` stream. See the <span
class="function">file\_put\_contents</span> documentation for details.

`context`  
The context passed to the `filename` stream. See the <span
class="function">file\_put\_contents</span> documentation for details.

### 返回值

The number of bytes written to the file, otherwise **`FALSE`** if APC is
not enabled, `filename` is an invalid file name, `filename` can't be
opened, the file dump can't be completed (e.g., the hard drive is out of
disk space), or an unknown error was encountered.

### 参见

-   <span class="function">apc\_bin\_dump</span>
-   <span class="function">apc\_bin\_load</span>

apc\_bin\_load
==============

Load a binary dump into the APC file/user cache

### 说明

<span class="type">bool</span> <span
class="methodname">apc\_bin\_load</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

Loads the given binary dump into the APC file/user cache.

### 参数

`data`  
The binary dump being loaded, likely from <span
class="function">apc\_bin\_dump</span>.

`flags`  
Either **`APC_BIN_VERIFY_CRC32`**, **`APC_BIN_VERIFY_MD5`**, or both.

### 返回值

Returns **`TRUE`** if the binary dump `data` was loaded with success,
otherwise **`FALSE`** is returned. **`FALSE`** is returned if APC is not
enabled, or if the `data` is not a valid APC binary dump (e.g.,
unexpected size).

### 范例

**示例 \#1 <span class="function">apc\_bin\_load</span> example**

``` php
<?php
$data = apc_bin_dump(NULL, NULL);
apc_bin_load($data, APC_BIN_VERIFY_MD5 | APC_BIN_VERIFY_CRC32);
?>
```

### 参见

-   <span class="function">apc\_bin\_dump</span>
-   <span class="function">apc\_bin\_loadfile</span>

apc\_bin\_loadfile
==================

Load a binary dump from a file into the APC file/user cache

### 说明

<span class="type">bool</span> <span
class="methodname">apc\_bin\_loadfile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">resource</span>
`$context`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

Loads a binary dump from a file into the APC file/user cache.

### 参数

`filename`  
The file name containing the dump, likely from <span
class="function">apc\_bin\_dumpfile</span>.

`context`  
The files context.

`flags`  
Either **`APC_BIN_VERIFY_CRC32`**, **`APC_BIN_VERIFY_MD5`**, or both.

### 返回值

Returns **`TRUE`** on success, otherwise **`FALSE`** Reasons it may
return **`FALSE`** include APC is not enabled, `filename` is an invalid
file name or empty, `filename` can't be opened, the file dump can't be
completed, or if the `data` is not a valid APC binary dump (e.g.,
unexpected size).

### 参见

-   <span class="function">apc\_bin\_dumpfile</span>
-   <span class="function">apc\_bin\_load</span>

apc\_cache\_info
================

Retrieves cached information from APC's data store

### 说明

<span class="type">array</span> <span
class="methodname">apc\_cache\_info</span> (\[ <span
class="methodparam"><span class="type">string</span> `$cache_type`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$limited`<span
class="initializer"> = **`FALSE`**</span></span> \]\] )

Retrieves cached information and meta-data from APC's data store.

### 参数

`cache_type`  
If `cache_type` is "*user*", information about the user cache will be
returned.

If `cache_type` is "*filehits*", information about which files have been
served from the bytecode cache for the current request will be returned.
This feature must be enabled at compile time using
**--enable-filehits**.

If an invalid or no `cache_type` is specified, information about the
system cache (cached files) will be returned.

`limited`  
If `limited` is **`TRUE`**, the return value will exclude the individual
list of cache entries. This is useful when trying to optimize calls for
statistics gathering.

### 返回值

Array of cached data (and meta-data) 或者在失败时返回 **`FALSE`**

> **Note**: <span class="simpara"> <span
> class="function">apc\_cache\_info</span> will raise a warning if it is
> unable to retrieve APC cache data. This typically occurs when APC is
> not enabled. </span>

### 更新日志

| 版本   | 说明                                                                   |
|--------|------------------------------------------------------------------------|
| 3.0.11 | The `limited` parameter was introduced.                                |
| 3.0.16 | The "*filehits*" option for the `cache_type` parameter was introduced. |

### 范例

**示例 \#1 A <span class="function">apc\_cache\_info</span> example**

``` php
<?php
print_r(apc_cache_info());
?>
```

以上例程的输出类似于：

    Array
    (
        [num_slots] => 2000
        [ttl] => 0
        [num_hits] => 9
        [num_misses] => 3
        [start_time] => 1123958803
        [cache_list] => Array
            (
                [0] => Array
                    (
                        [filename] => /path/to/apc_test.php
                        [device] => 29954
                        [inode] => 1130511
                        [type] => file
                        [num_hits] => 1
                        [mtime] => 1123960686
                        [creation_time] => 1123960696
                        [deletion_time] => 0
                        [access_time] => 1123962864
                        [ref_count] => 1
                        [mem_size] => 677
                    )
                [1] => Array (...iterates for each cached file)
    )

### 参见

-   <a href="/apc/setup.html#运行时配置" class="link">APC configuration directives</a>
-   <span class="methodname">APCIterator::getTotalSize</span>
-   <span class="methodname">APCIterator::getTotalHits</span>
-   <span class="methodname">APCIterator::getTotalCount</span>

apc\_cas
========

用新值更新旧值

### 说明

<span class="type">bool</span> <span class="methodname">apc\_cas</span>
( <span class="methodparam"><span class="type">string</span>
`$key`</span> , <span class="methodparam"><span class="type">int</span>
`$old`</span> , <span class="methodparam"><span class="type">int</span>
`$new`</span> )

<span class="function">apc\_cas</span>
如果key存在，并且key当前存储的整数等于 `old`，就使用 `new`
更新key当前存储的整数。

### 参数

`key`  
需要被更新的 key。

`old`  
key当前值。

`new`  
指定的更新值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">apc\_cas</span> 示例**

``` php
<?php
apc_store('foobar', 2);
echo '$foobar = 2', PHP_EOL;
echo '$foobar == 1 ? 2 : 1 = ', (apc_cas('foobar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;
echo '$foobar == 2 ? 1 : 2 = ', (apc_cas('foobar', 2, 1) ? 'ok' : 'fail'), PHP_EOL;

echo '$foobar = ', apc_fetch('foobar'), PHP_EOL;

echo '$f__bar == 1 ? 2 : 1 = ', (apc_cas('f__bar', 1, 2) ? 'ok' : 'fail'), PHP_EOL;

apc_store('perfection', 'xyz');
echo '$perfection == 2 ? 1 : 2 = ', (apc_cas('perfection', 2, 1) ? 'ok' : 'epic fail'), PHP_EOL;

echo '$foobar = ', apc_fetch('foobar'), PHP_EOL;
?>
```

以上例程的输出类似于：

    $foobar = 2
    $foobar == 1 ? 2 : 1 = fail
    $foobar == 2 ? 1 : 2 = ok
    $foobar = 1
    $f__bar == 1 ? 2 : 1 = fail
    $perfection == 2 ? 1 : 2 = epic fail
    $foobar = 1

### 参见

-   <span class="function">apc\_dec</span>
-   <span class="function">apc\_store</span>

apc\_clear\_cache
=================

清除APC缓存

### 说明

<span class="type">bool</span> <span
class="methodname">apc\_clear\_cache</span> (\[ <span
class="methodparam"><span class="type">string</span> `$cache_type`<span
class="initializer"> = ""</span></span> \] )

清除用户或者系统缓存

### 参数

`cache_type`  
如果 `cache_type` 是 "*user*", 用户 的缓存将被清除;
否则系统缓存(缓存文件)将被清除。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">apc\_cache\_info</span>

apc\_compile\_file
==================

Stores a file in the bytecode cache, bypassing all filters

### 说明

<span class="type">mixed</span> <span
class="methodname">apc\_compile\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$atomic`<span class="initializer"> = **`TRUE`**</span></span> \] )

Stores a file in the bytecode cache, bypassing all filters.

### 参数

`filename`  
Full or relative path to a PHP file that will be compiled and stored in
the bytecode cache.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">apc\_bin\_dumpfile</span>
-   <span class="function">apc\_bin\_loadfile</span>

apc\_dec
========

Decrease a stored number

### 说明

<span class="type">int</span> <span class="methodname">apc\_dec</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
\[, <span class="methodparam"><span class="type">int</span> `$step`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `&$success`</span>
\]\] )

Decreases a stored integer value.

### 参数

`key`  
The key of the value being decreased.

`step`  
The step, or value to decrease.

`success`  
Optionally pass the success or fail boolean value to this referenced
variable.

### 返回值

Returns the current value of `key`'s value on success, 或者在失败时返回
**`FALSE`**

### 范例

**示例 \#1 <span class="function">apc\_dec</span> example**

``` php
<?php
echo "Let's do something with success", PHP_EOL;

apc_store('anumber', 42);

echo apc_fetch('anumber'), PHP_EOL;

echo apc_dec('anumber'), PHP_EOL;
echo apc_dec('anumber', 10), PHP_EOL;
echo apc_dec('anumber', 10, $success), PHP_EOL;

var_dump($success);

echo "Now, let's fail", PHP_EOL, PHP_EOL;

apc_store('astring', 'foo');

$ret = apc_dec('astring', 1, $fail);

var_dump($ret);
var_dump($fail);
?>
```

以上例程的输出类似于：

    Let's do something with success
    42
    41
    31
    21
    bool(true)

    Now, let's fail
    bool(false)
    bool(false)

### 参见

-   <span class="function">apc\_inc</span>

apc\_define\_constants
======================

Defines a set of constants for retrieval and mass-definition

### 说明

<span class="type">bool</span> <span
class="methodname">apc\_define\_constants</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">array</span>
`$constants`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$case_sensitive`<span class="initializer"> =
**`TRUE`**</span></span> \] )

<span class="function">define</span> is notoriously slow. Since the main
benefit of APC is to increase the performance of scripts/applications,
this mechanism is provided to streamline the process of mass constant
definition. However, this function does not perform as well as
anticipated.

For a better-performing solution, try the
<a href="https://pecl.php.net/package/hidef" class="link external">» hidef</a>
extension from PECL.

> **Note**: <span class="simpara"> To remove a set of stored constants
> (without clearing the entire cache), an empty array may be passed as
> the `constants` parameter, effectively clearing the stored value(s).
> </span>

### 参数

`key`  
The `key` serves as the name of the constant set being stored. This
`key` is used to retrieve the stored constants in <span
class="function">apc\_load\_constants</span>.

`constants`  
An associative array of *constant\_name =\> value* pairs. The
*constant\_name* must follow the normal
<a href="/language/constants.html" class="link">constant</a> naming
rules. *value* must evaluate to a scalar value.

`case_sensitive`  
The default behaviour for constants is to be declared case-sensitive;
i.e. *CONSTANT* and *Constant* represent different values. If this
parameter evaluates to **`FALSE`** the constants will be declared as
case-insensitive symbols.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">apc\_define\_constants</span>
example**

``` php
<?php
$constants = array(
    'ONE'   => 1,
    'TWO'   => 2,
    'THREE' => 3,
);
apc_define_constants('numbers', $constants);
echo ONE, TWO, THREE;
?>
```

以上例程会输出：

    123

### 参见

-   <span class="function">apc\_load\_constants</span>
-   <span class="function">define</span>
-   <span class="function">constant</span>
-   Or
    <a href="/language/constants.html" class="link">the PHP constants reference</a>

apc\_delete\_file
=================

Deletes files from the opcode cache

### 说明

<span class="type">mixed</span> <span
class="methodname">apc\_delete\_file</span> ( <span
class="methodparam"><span class="type">mixed</span> `$keys`</span> )

Deletes the given files from the opcode cache.

### 参数

`keys`  
The files to be deleted. Accepts a <span class="type">string</span>,
<span class="type">array</span> of strings, or an <span
class="classname">APCIterator</span> <span class="type">object</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Or if `keys` is
an <span class="type">array</span>, then an empty array is returned on
success, or an array of failed files is returned.

### 范例

**示例 \#1 <span class="function">apc\_delete\_file</span> example**

``` php
<?php
$filename = 'file.php';

if (apc_compile_file($filename)) {

    if (apc_delete_file($filename)) {
        echo "Successfully deleted file $filename from APC cache.", PHP_EOL;
    }
}

if (apc_compile_file($filename)) {

    if ($good = apc_delete_file(array($filename, 'donotexist.php'))) {
        var_dump($good);
    }
}

$bad = apc_delete_file('donotexist.php');
var_dump($bad);
?>
```

以上例程的输出类似于：

    Successfully deleted file file.php from APC cache.
    [Mon May 24 09:30:33 2010] [apc-warning] Could not stat file donotexist.php, unable to delete from cache. in /tmp/test.php on line 13.
    array(1) {
      [0]=>
      string(14) "donotexist.php"
    }
    [Mon May 24 09:30:33 2010] [apc-warning] Could not stat file donotexist.php, unable to delete from cache. in /tmp/test.php on line 18.
    bool(false)

### 参见

-   <span class="function">apc\_clear\_cache</span>
-   <span class="function">apc\_delete</span>
-   <span class="function">apc\_exists</span>

apc\_delete
===========

从用户缓存中删除某个变量

### 说明

<span class="type">mixed</span> <span
class="methodname">apc\_delete</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> )

从数据存储里删除某个变量。

### 参数

`key`  
`key` 即是你用 <span class="function">apc\_store</span>
存储数据时所设定的标记名称。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 A <span class="function">apc\_delete</span> 范例**

``` php
<?php
$bar = 'BAR';
apc_store('foo', $bar);
apc_delete('foo');
// this is obviously useless in this form
?>
```

### 参见

-   <span class="function">apc\_store</span>
-   <span class="function">apc\_fetch</span>

apc\_exists
===========

检查APC中是否存在某个或者某些key

### 说明

<span class="type">mixed</span> <span
class="methodname">apc\_exists</span> ( <span class="methodparam"><span
class="type">mixed</span> `$keys`</span> )

检查是否有一个或者多个APC键名存在

### 参数

`keys`  
<span class="type">string</span>，或者包含键的 <span
class="type">array</span>，元素是字符串。

### 返回值

如果Key存在的话返回 **`TRUE`** , 否则返回 **`FALSE`** 如果参数
`keys`是一个<span class="type">array</span> ，
将返回一个包含所有存在的key的数组，假如数组中的key一个都不存在的话，
就返回空的数组。

### 范例

**示例 \#1 <span class="function">apc\_exists</span> 例子**

``` php
<?php
$fruit  = 'apple';
$veggie = 'carrot';

apc_store('foo', $fruit);
apc_store('bar', $veggie);

if (apc_exists('foo')) {
    echo "Foo exists: ";
    echo apc_fetch('foo');
} else {
    echo "Foo does not exist";
}

echo PHP_EOL;
if (apc_exists('baz')) {
    echo "Baz exists.";
} else {
    echo "Baz does not exist";
}

echo PHP_EOL;

$ret = apc_exists(array('foo', 'donotexist', 'bar'));
var_dump($ret);

?>
```

以上例程的输出类似于：

    Foo exists: apple
    Baz does not exist
    array(2) {
      ["foo"]=>
      bool(true)
      ["bar"]=>
      bool(true)
    }

### 参见

-   <span class="function">apc\_cache\_info</span>
-   <span class="function">apc\_fetch</span>

apc\_fetch
==========

从缓存中取出存储的变量

### 说明

<span class="type">mixed</span> <span
class="methodname">apc\_fetch</span> ( <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">bool</span> `&$success`</span> \]
)

从缓存中取出存储的变量

### 参数

`key`  
`key` 是使用 <span class="function">apc\_store</span> 存储的键名。
如果传递的是一个数组，则数组中的每个元素的值都被返回

`success`  
成功时为 **`TRUE`** 失败时 **`FALSE`**。

### 返回值

存储一个变量或者一个数组失败时返回; **`FALSE`**

### 范例

**示例 \#1 <span class="function">apc\_fetch</span> 范例**

``` php
<?php
$bar = 'BAR';
apc_store('foo', $bar);
var_dump(apc_fetch('foo'));
?>
```

以上例程会输出：

    string(3) "BAR"

### 更新日志

| 版本   | 说明                               |
|--------|------------------------------------|
| 3.0.17 | The `success` parameter was added. |

### 参见

-   <span class="function">apc\_store</span>
-   <span class="function">apc\_delete</span>
-   <span class="classname">APCIterator</span>

apc\_inc
========

递增一个储存的数字

### 说明

<span class="type">int</span> <span class="methodname">apc\_inc</span> (
<span class="methodparam"><span class="type">string</span> `$key`</span>
\[, <span class="methodparam"><span class="type">int</span> `$step`<span
class="initializer"> = 1</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `&$success`</span>
\]\] )

递增一个储存的数字。

### 参数

`key`  
该键内的值被增加。

`step`  
步长，或者需要增加的值。

`success`  
可选，用于传递函数成功或失败到该引用变量里。

### 返回值

成功时返回 `key` 的当前值， 或者在失败时返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">apc\_inc</span> 范例**

``` php
<?php
echo "Let's do something with success", PHP_EOL;

apc_store('anumber', 42);

echo apc_fetch('anumber'), PHP_EOL;

echo apc_inc('anumber'), PHP_EOL;
echo apc_inc('anumber', 10), PHP_EOL;
echo apc_inc('anumber', 10, $success), PHP_EOL;

var_dump($success);

echo "Now, let's fail", PHP_EOL, PHP_EOL;

apc_store('astring', 'foo');

$ret = apc_inc('astring', 1, $fail);

var_dump($ret);
var_dump($fail);
?>
```

以上例程的输出类似于：

    42
    43
    53
    63
    bool(true)
    Now, let's fail

    bool(false)
    bool(false)

### 参见

-   <span class="function">apc\_dec</span>

apc\_load\_constants
====================

Loads a set of constants from the cache

### 说明

<span class="type">bool</span> <span
class="methodname">apc\_load\_constants</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$case_sensitive`<span class="initializer"> = **`TRUE`**</span></span>
\] )

Loads a set of constants from the cache.

### 参数

`key`  
The name of the constant set (that was stored with <span
class="function">apc\_define\_constants</span>) to be retrieved.

`case_sensitive`  
The default behaviour for constants is to be declared case-sensitive;
i.e. *CONSTANT* and *Constant* represent different values. If this
parameter evaluates to **`FALSE`** the constants will be declared as
case-insensitive symbols.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">apc\_load\_constants</span> example**

``` php
<?php
$constants = array(
    'ONE'   => 1,
    'TWO'   => 2,
    'THREE' => 3,
);
apc_define_constants('numbers', $constants);
apc_load_constants('numbers');
echo ONE, TWO, THREE;
?>
```

以上例程会输出：

    123

### 参见

-   <span class="function">apc\_define\_constants</span>
-   <span class="function">define</span>
-   <span class="function">constant</span>
-   Or
    <a href="/language/constants.html" class="link">the PHP constants reference</a>

apc\_sma\_info
==============

Retrieves APC's Shared Memory Allocation information

### 说明

<span class="type">array</span> <span
class="methodname">apc\_sma\_info</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$limited`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Retrieves APC's Shared Memory Allocation information.

### 参数

`limited`  
When set to **`FALSE`** (default) <span
class="function">apc\_sma\_info</span> will return a detailed
information about each segment.

### 返回值

Array of Shared Memory Allocation data; **`FALSE`** on failure.

### 范例

**示例 \#1 A <span class="function">apc\_sma\_info</span> example**

``` php
<?php
print_r(apc_sma_info());
?>
```

以上例程的输出类似于：

    Array
    (
        [num_seg] => 1
        [seg_size] => 31457280
        [avail_mem] => 31448408
        [block_lists] => Array
            (
                [0] => Array
                    (
                        [0] => Array
                            (
                                [size] => 31448408
                                [offset] => 8864
                            )

                    )

            )

    )

### 参见

-   <a href="/apc/setup.html#运行时配置" class="link">APC configuration directives</a>

apc\_store
==========

Cache a variable in the data store

### 说明

<span class="type">bool</span> <span
class="methodname">apc\_store</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$var`</span> \[,
<span class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \] )

<span class="type">array</span> <span
class="methodname">apc\_store</span> ( <span class="methodparam"><span
class="type">array</span> `$values`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$unused`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$ttl`<span
class="initializer"> = 0</span></span> \]\] )

缓存一个变量到APC中

> **Note**: <span class="simpara"> 与PHP中其他的机制不同，使用<span
> class="function">apc\_store</span> 存储的变量
> 在不同的请求之间一直持久存在（直到从缓存系统中移除）。 </span>

### 参数

`key`  
存储缓存变量使用的名称.`key`是唯一的，所以 两个值使用同一个
`key`，原来的将被新的值覆盖。

`var`  
The variable to store

`ttl`  
生存时间;在缓存中存储`var`共`ttl`秒,
在`ttl`秒过去后,存储的变量将会从缓存中擦除(在下一次请求时),
如果没有设置`ttl`(或者`ttl`是*0*),
变量将一直存活到被手动移除为止,除此之外不在缓存中的可能原因是，
缓存系统使用clear，或者restart等。

`values`  
Names in key, variables in value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 Second syntax
returns array with error keys.

### 范例

**示例 \#1 <span class="function">apc\_store</span> 例子**

``` php
<?php
$bar = 'BAR';
apc_store('foo', $bar);
var_dump(apc_fetch('foo'));
?>
```

以上例程会输出：

    string(3) "BAR"

### 参见

-   <span class="function">apc\_add</span>
-   <span class="function">apc\_fetch</span>
-   <span class="function">apc\_delete</span>

**目录**

-   [apc\_add](/ref/apc.html#apc_add) — 缓存一个变量到数据存储
-   [apc\_bin\_dump](/ref/apc.html#apc_bin_dump) —
    获取给定文件和变量的二进制文件转储。
-   [apc\_bin\_dumpfile](/ref/apc.html#apc_bin_dumpfile) — Output a
    binary dump of cached files and user variables to a file
-   [apc\_bin\_load](/ref/apc.html#apc_bin_load) — Load a binary dump
    into the APC file/user cache
-   [apc\_bin\_loadfile](/ref/apc.html#apc_bin_loadfile) — Load a binary
    dump from a file into the APC file/user cache
-   [apc\_cache\_info](/ref/apc.html#apc_cache_info) — Retrieves cached
    information from APC's data store
-   [apc\_cas](/ref/apc.html#apc_cas) — 用新值更新旧值
-   [apc\_clear\_cache](/ref/apc.html#apc_clear_cache) — 清除APC缓存
-   [apc\_compile\_file](/ref/apc.html#apc_compile_file) — Stores a file
    in the bytecode cache, bypassing all filters
-   [apc\_dec](/ref/apc.html#apc_dec) — Decrease a stored number
-   [apc\_define\_constants](/ref/apc.html#apc_define_constants) —
    Defines a set of constants for retrieval and mass-definition
-   [apc\_delete\_file](/ref/apc.html#apc_delete_file) — Deletes files
    from the opcode cache
-   [apc\_delete](/ref/apc.html#apc_delete) — 从用户缓存中删除某个变量
-   [apc\_exists](/ref/apc.html#apc_exists) —
    检查APC中是否存在某个或者某些key
-   [apc\_fetch](/ref/apc.html#apc_fetch) — 从缓存中取出存储的变量
-   [apc\_inc](/ref/apc.html#apc_inc) — 递增一个储存的数字
-   [apc\_load\_constants](/ref/apc.html#apc_load_constants) — Loads a
    set of constants from the cache
-   [apc\_sma\_info](/ref/apc.html#apc_sma_info) — Retrieves APC's
    Shared Memory Allocation information
-   [apc\_store](/ref/apc.html#apc_store) — Cache a variable in the data
    store
