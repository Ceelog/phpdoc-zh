Rar Archiving
=============

**目录**

-   [简介](/intro/rar.html)
-   [安装／配置](/rar/setup.html)
    -   [需求](/rar/setup.html#需求)
    -   [安装](/rar/setup.html#安装)
    -   [运行时配置](/rar/setup.html#运行时配置)
    -   [资源类型](/rar/setup.html#资源类型)
-   [预定义常量](/rar/constants.html)
-   [范例](/rar/examples.html)
-   [Rar 函数](/ref/rar.html)
    -   [rar\_wrapper\_cache\_stats](/ref/rar.html#rar_wrapper_cache_stats)
        — Cache hits and misses for the URL wrapper
-   [RarArchive](/class/rararchive.html) — The RarArchive class
    -   [RarArchive::close](/class/rararchive.html#RarArchive::close) —
        Close RAR archive and free all resources
    -   [RarArchive::getComment](/class/rararchive.html#RarArchive::getComment)
        — Get comment text from the RAR archive
    -   [RarArchive::getEntries](/class/rararchive.html#RarArchive::getEntries)
        — Get full list of entries from the RAR archive
    -   [RarArchive::getEntry](/class/rararchive.html#RarArchive::getEntry)
        — Get entry object from the RAR archive
    -   [RarArchive::isBroken](/class/rararchive.html#RarArchive::isBroken)
        — Test whether an archive is broken (incomplete)
    -   [RarArchive::isSolid](/class/rararchive.html#RarArchive::isSolid)
        — Check whether the RAR archive is solid
    -   [RarArchive::open](/class/rararchive.html#RarArchive::open) —
        Open RAR archive
    -   [RarArchive::setAllowBroken](/class/rararchive.html#RarArchive::setAllowBroken)
        — Whether opening broken archives is allowed
    -   [RarArchive::\_\_toString](/class/rararchive.html#RarArchive::__toString)
        — Get text representation
-   [RarEntry](/class/rarentry.html) — The RarEntry class
    -   [RarEntry::extract](/class/rarentry.html#RarEntry::extract) —
        Extract entry from the archive
    -   [RarEntry::getAttr](/class/rarentry.html#RarEntry::getAttr) —
        Get attributes of the entry
    -   [RarEntry::getCrc](/class/rarentry.html#RarEntry::getCrc) — Get
        CRC of the entry
    -   [RarEntry::getFileTime](/class/rarentry.html#RarEntry::getFileTime)
        — Get entry last modification time
    -   [RarEntry::getHostOs](/class/rarentry.html#RarEntry::getHostOs)
        — Get entry host OS
    -   [RarEntry::getMethod](/class/rarentry.html#RarEntry::getMethod)
        — Get pack method of the entry
    -   [RarEntry::getName](/class/rarentry.html#RarEntry::getName) —
        Get name of the entry
    -   [RarEntry::getPackedSize](/class/rarentry.html#RarEntry::getPackedSize)
        — Get packed size of the entry
    -   [RarEntry::getStream](/class/rarentry.html#RarEntry::getStream)
        — Get file handler for entry
    -   [RarEntry::getUnpackedSize](/class/rarentry.html#RarEntry::getUnpackedSize)
        — Get unpacked size of the entry
    -   [RarEntry::getVersion](/class/rarentry.html#RarEntry::getVersion)
        — Get minimum version of RAR program required to unpack the
        entry
    -   [RarEntry::isDirectory](/class/rarentry.html#RarEntry::isDirectory)
        — Test whether an entry represents a directory
    -   [RarEntry::isEncrypted](/class/rarentry.html#RarEntry::isEncrypted)
        — Test whether an entry is encrypted
    -   [RarEntry::\_\_toString](/class/rarentry.html#RarEntry::__toString)
        — Get text representation of entry
-   [RarException](/class/rarexception.html) — The RarException class
    -   [RarException::isUsingExceptions](/class/rarexception.html#RarException::isUsingExceptions)
        — Check whether error handling with exceptions is in use
    -   [RarException::setUsingExceptions](/class/rarexception.html#RarException::setUsingExceptions)
        — Activate and deactivate error handling with exceptions

简介
----

This class represents a RAR archive, which may be formed by several
volumes (parts) and which contains a number of RAR entries (i.e., files,
directories and other special objects such as symbolic links).

Objects of this class can be traversed, yielding the entries stored in
the respective RAR archive. Those entries can also be obtained through
<span class="methodname">RarArchive::getEntry</span> and <span
class="methodname">RarArchive::getEntries</span>.

类摘要
------

**RarArchive**

<span class="ooclass"> <span class="modifier">final</span> class
**RarArchive** </span> <span class="oointerface">implements <span
class="interfacename">Traversable</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getEntries</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">RarEntry</span>
<span class="methodname">getEntry</span> ( <span
class="methodparam"><span class="type">string</span> `$entryname`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isBroken</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isSolid</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">RarArchive</span>
<span class="methodname">open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">callable</span>
`$volume_callback`<span class="initializer"> = NULL</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setAllowBroken</span> ( <span
class="methodparam"><span class="type">bool</span>
`$allow_broken`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

RarArchive::close
=================

rar\_close
==========

Close RAR archive and free all resources

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarArchive::close</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">rar\_close</span> ( <span class="methodparam"><span
class="type">RarArchive</span> `$rarfile`</span> )

Close RAR archive and free all allocated resources.

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本           | 说明                                                                                                                                                                                                                                                                                  |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL rar 2.0.0 | The RAR entries returned by <span class="methodname">RarArchive::getEntry</span> and <span class="methodname">RarArchive::getEntries</span> are now invalidated when calling this method. This means that all instance methods called for such entries and not guaranteed to succeed. |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$rar_arch = RarArchive::open('latest_winrar.rar');
echo $rar_arch."\n";
$rar_arch->close();
echo $rar_arch."\n";
?>
```

以上例程的输出类似于：

    RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar"
    RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar" (closed)

**示例 \#2 过程化风格**

``` php
<?php
$rar_arch = rar_open('latest_winrar.rar');
echo $rar_arch."\n";
rar_close($rar_arch);
echo $rar_arch."\n";
?>
```

RarArchive::getComment
======================

rar\_comment\_get
=================

Get comment text from the RAR archive

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RarArchive::getComment</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">rar\_comment\_get</span> ( <span
class="methodparam"><span class="type">RarArchive</span>
`$rarfile`</span> )

Get the (global) comment stored in the RAR archive. It may be up to 64
KiB long.

> **Note**:
>
> This extension does not support comments at the entry level.

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

### 返回值

Returns the comment or **`NULL`** if there is none.

> **Note**:
>
> RAR has currently no support for unicode comments. The encoding of the
> result of this function is not specified, but it will probably be
> Windows-1252.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$rar_arch = RarArchive::open('commented.rar'); 
echo $rar_arch->getComment();
?>
```

以上例程的输出类似于：

    This is the comment of the file commented.rar.

**示例 \#2 过程化风格**

``` php
<?php
$rar_arch = rar_open('commented.rar'); 
echo rar_comment_get($rar_arch);
?>
```

RarArchive::getEntries
======================

rar\_list
=========

Get full list of entries from the RAR archive

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">RarArchive::getEntries</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">rar\_list</span> ( <span class="methodparam"><span
class="type">RarArchive</span> `$rarfile`</span> )

Get entries list (files and directories) from the RAR archive.

> **Note**:
>
> If the archive has entries with the same name, this method, together
> with <span class="type">RarArchive</span> *foreach* iteration and
> array-like access with numeric indexes, are the only ones to access
> all the entries (i.e., <span
> class="methodname">RarArchive::getEntry</span> and the
> <a href="/wrappers/rar.html" class="link"><em>rar://</em> wrapper</a>
> are insufficient).

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

### 返回值

<span class="function">rar\_list</span> returns array of <span
class="type">RarEntry</span> objects 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本           | 说明                                                                       |
|----------------|----------------------------------------------------------------------------|
| PECL rar 3.0.0 | Support for RAR archives with repeated entry names is no longer defective. |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$rar_arch = RarArchive::open('solid.rar');
if ($rar_arch === FALSE)
    die("Could not open RAR archive.");

$rar_entries = $rar_arch->getEntries();
if ($rar_entries === FALSE)
    die("Could not retrieve entries.");

echo "Found " . count($rar_entries) . " entries.\n";

foreach ($rar_entries as $e) {
    echo $e;
    echo "\n";
}
$rar_arch->close();
?>
```

以上例程的输出类似于：

    Found 2 entries.
    RarEntry for file "tese.txt" (23b93a7a)
    RarEntry for file "unrardll.txt" (2ed64b6e)

**示例 \#2 过程化风格**

``` php
<?php
$rar_arch = rar_open('solid.rar');
if ($rar_arch === FALSE)
    die("Could not open RAR archive.");

$rar_entries = rar_list($rar_arch);
if ($rar_entries === FALSE)
    die("Could retrieve entries.");

echo "Found " . count($rar_entries) . " entries.\n";

foreach ($rar_entries as $e) {
    echo $e;
    echo "\n";
}
rar_close($rar_arch);
?>
```

### 参见

-   <span class="methodname">RarArchive::getEntry</span>
-   <a href="/wrappers/rar.html" class="link"><em>rar://</em> wrapper</a>

RarArchive::getEntry
====================

rar\_entry\_get
===============

Get entry object from the RAR archive

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">RarEntry</span>
<span class="methodname">RarArchive::getEntry</span> ( <span
class="methodparam"><span class="type">string</span> `$entryname`</span>
)

过程化风格:

<span class="type">RarEntry</span> <span
class="methodname">rar\_entry\_get</span> ( <span
class="methodparam"><span class="type">RarArchive</span>
`$rarfile`</span> , <span class="methodparam"><span
class="type">string</span> `$entryname`</span> )

Get entry object (file or directory) from the RAR archive.

> **Note**:
>
> You can also get entry objects using <span
> class="methodname">RarArchive::getEntries</span>.
>
> Note that a RAR archive can have multiple entries with the same name;
> this method will retrieve only the first.

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

`entryname`  
Path to the entry within the RAR archive.

> **Note**:
>
> The path must be the same returned by <span
> class="methodname">RarEntry::getName</span>.

### 返回值

Returns the matching <span class="type">RarEntry</span> object
或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$rar_arch = RarArchive::open('solid.rar');
if ($rar_arch === FALSE)
    die("Could not open RAR archive.");
$rar_entry = $rar_arch->getEntry('tese.txt');
if ($rar_entry === FALSE)
    die("Could not get such entry");
echo get_class($rar_entry)."\n";
echo $rar_entry;
$rar_arch->close();
?>
```

以上例程的输出类似于：

    RarEntry
    RarEntry for file "tese.txt" (23b93a7a)

**示例 \#2 过程化风格**

``` php
<?php
$rar_arch = rar_open('solid.rar');
if ($rar_arch === FALSE)
    die("Could not open RAR archive.");
$rar_entry = rar_entry_get($rar_arch, 'tese.txt');
if ($rar_entry === FALSE)
    die("Could not get such entry");
echo get_class($rar_entry)."\n";
echo $rar_entry;
rar_close($rar_arch);
?>
```

### 参见

-   <span class="methodname">RarArchive::getEntries</span>
-   <a href="/wrappers/rar.html" class="link"><em>rar://</em> wrapper</a>

RarArchive::isBroken
====================

rar\_broken\_is
===============

Test whether an archive is broken (incomplete)

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarArchive::isBroken</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">rar\_broken\_is</span> ( <span
class="methodparam"><span class="type">RarArchive</span>
`$rarfile`</span> )

This function determines whether an archive is incomplete, i.e., if a
volume is missing or a volume is truncated.

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

### 返回值

Returns **`TRUE`** if the archive is broken, **`FALSE`** otherwise. This
function may also return **`FALSE`** if the passed file has already been
closed. The only way to tell the two cases apart is to enable exceptions
with <span class="methodname">RarException::setUsingExceptions</span>;
however, this should be unnecessary as a program should not operate on
closed files.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* Third argument is used to omit notice */
$arch = RarArchive::open($file, null, 'retnull');
var_dump($arch->isBroken());
?>
```

以上例程的输出类似于：

    bool(true)

**示例 \#2 过程化风格**

``` php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* Third argument is used to omit notice */
$arch = rar_open($file, null, 'retnull');
var_dump(rar_broken_is($arch));
?>
```

### 参见

-   <span class="methodname">RarArchive::setAllowBroken</span>

RarArchive::isSolid
===================

rar\_solid\_is
==============

Check whether the RAR archive is solid

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarArchive::isSolid</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">rar\_solid\_is</span> ( <span
class="methodparam"><span class="type">RarArchive</span>
`$rarfile`</span> )

Check whether the RAR archive is solid. Individual file extraction is
slower on solid archives.

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

### 返回值

Returns **`TRUE`** if the archive is solid, **`FALSE`** otherwise.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$arch1 = RarArchive::open("store_method.rar");
$arch2 = RarArchive::open("solid.rar");
echo "$arch1: " . ($arch1->isSolid()?'yes':'no') ."\n";
echo "$arch2: " . ($arch2->isSolid()?'yes':'no') . "\n";
?>
```

以上例程的输出类似于：

    RAR Archive "C:\php_rar\trunk\tests\store_method.rar": no
    RAR Archive "C:\php_rar\trunk\tests\solid.rar": yes

**示例 \#2 过程化风格**

``` php
<?php
$arch1 = rar_open("store_method.rar");
$arch2 = rar_open("solid.rar");
echo "$arch1: " . (rar_solid_is($arch1)?'yes':'no') ."\n";
echo "$arch2: " . (rar_solid_is($arch2)?'yes':'no') . "\n";
?>
```

RarArchive::open
================

rar\_open
=========

Open RAR archive

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">RarArchive</span>
<span class="methodname">RarArchive::open</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$password`<span class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">callable</span>
`$volume_callback`<span class="initializer"> = NULL</span></span> \]\] )

过程化风格:

<span class="type">RarArchive</span> <span
class="methodname">rar\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">callable</span>
`$volume_callback`<span class="initializer"> = NULL</span></span> \]\] )

Open specified RAR archive and return <span
class="type">RarArchive</span> instance representing it.

> **Note**:
>
> If opening a multi-volume archive, the path of the first volume should
> be passed as the first parameter. Otherwise, not all files will be
> shown. This is by design.

### 参数

`filename`  
Path to the Rar archive.

`password`  
A plain password, if needed to decrypt the headers. It will also be used
by default if encrypted files are found. Note that the files may have
different passwords in respect to the headers and among them.

`volume_callback`  
A function that receives one parameter – the path of the volume that was
not found – and returns a string with the correct path for such volume
or **`NULL`** if such volume does not exist or is not known. The
programmer should ensure the passed function doesn't cause loops as this
function is called repeatedly if the path returned in a previous call
did not correspond to the needed volume. Specifying this parameter omits
the notice that would otherwise be emitted whenever a volume is not
found; an implementation that only returns **`NULL`** can therefore be
used to merely omit such notices.

**Warning**

Prior to version 2.0.0, this function would not handle relative paths
correctly. Use <span class="function">realpath</span> as a workaround.

### 返回值

Returns the requested <span class="type">RarArchive</span> instance
或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本           | 说明                         |
|----------------|------------------------------|
| PECL rar 3.0.0 | `volume_callback` was added. |

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$rar_arch = RarArchive::open('encrypted_headers.rar', 'samplepassword');
if ($rar_arch === FALSE)
    die("Failed opening file");
    
$entries = $rar_arch->getEntries();
if ($entries === FALSE)
    die("Failed fetching entries");

echo "Found " . count($entries) . " files.\n";

if (empty($entries))
    die("No valid entries found.");
    
$stream = reset($entries)->getStream();
if ($stream === FALSE)
    die("Failed opening first file");

$rar_arch->close();

echo "Content of first one follows:\n";
echo stream_get_contents($stream);

fclose($stream);
?>
```

以上例程的输出类似于：

    Found 2 files.
    Content of first one follows:
    Encrypted file 1 contents.

**示例 \#2 过程化风格**

``` php
<?php
$rar_arch = rar_open('encrypted_headers.rar', 'samplepassword');
if ($rar_arch === FALSE)
    die("Failed opening file");
    
$entries = rar_list($rar_arch);
if ($entries === FALSE)
    die("Failed fetching entries");

echo "Found " . count($entries) . " files.\n";

if (empty($entries))
    die("No valid entries found.");
    
$stream = reset($entries)->getStream();
if ($stream === FALSE)
    die("Failed opening first file");

rar_close($rar_arch);

echo "Content of first one follows:\n";
echo stream_get_contents($stream);

fclose($stream);
?>
```

**示例 \#3 Volume Callback**

``` php
<?php
/* In this example, there's a volume named multi_broken.part1.rar
 * whose next volume is named multi.part2.rar */
function resolve($vol) {
    if (preg_match('/_broken/', $vol))
        return str_replace('_broken', '', $vol);
    else
        return null;
}
$rar_file1 = rar_open(dirname(__FILE__).'/multi_broken.part1.rar', null, 'resolve');
$entry = $rar_file1->getEntry('file2.txt');
$entry->extract(null, dirname(__FILE__) . "/temp_file2.txt");
?>
```

### 参见

-   <a href="/wrappers/rar.html" class="link"><em>rar://</em> wrapper</a>

RarArchive::setAllowBroken
==========================

Whether opening broken archives is allowed

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarArchive::setAllowBroken</span> ( <span
class="methodparam"><span class="type">bool</span>
`$allow_broken`</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">rar\_allow\_broken\_set</span> ( <span
class="methodparam"><span class="type">RarArchive</span>
`$rarfile`</span> , <span class="methodparam"><span
class="type">bool</span> `$allow_broken`</span> )

This method defines whether broken archives can be read or all the
operations that attempt to extract the archive entries will fail. Broken
archives are archives for which no error is detected when the file is
opened but an error occurs when reading the entries.

### 参数

`rarfile`  
A <span class="type">RarArchive</span> object, opened with <span
class="function">rar\_open</span>.

`allow_broken`  
Whether to allow reading broken files (**`TRUE`**) or not (**`FALSE`**).

### 返回值

Returns **`TRUE`** 或者在失败时返回 **`FALSE`**. It will only fail if
the file has already been closed.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* Third argument omits "volume not found" message */
$a = RarArchive::open($file, null, 'retnull');
$a->setAllowBroken(true);
foreach ($a->getEntries() as $e) {
    echo "$e\n";
}
var_dump(count($a));
?>
```

以上例程的输出类似于：

    RarEntry for file "file1.txt" (52b28202)
    int(1)

**示例 \#2 过程化风格**

``` php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* Third argument omits "volume not found" message */
$a = rar_open($file, null, 'retnull');
rar_allow_broken_set($a, true);
foreach (rar_list($a) as $e) {
    echo "$e\n";
}
var_dump(count($a));
?>
```

### 参见

-   <span class="methodname">RarArchive::isBroken</span>

RarArchive::\_\_toString
========================

Get text representation

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RarArchive::\_\_toString</span> ( <span
class="methodparam">void</span> )

Provides a string representation for this <span
class="type">RarArchive</span> object. It currently shows the full path
name of the archive volume that was opened and whether the resource is
valid or was already closed through a call to <span
class="methodname">RarArchive::close</span>.

This method may be used only for debugging purposes, as there are no
guarantees as to which information the result contains or how it is
formatted.

### 参数

此函数没有参数。

### 返回值

A textual representation of this <span class="type">RarArchive</span>
object. The content of this representation is unspecified.

### 范例

**示例 \#1 <span class="methodname">RarArchive::\_\_toString</span>
example**

``` php
<?php
$rar_arch = RarArchive::open('latest_winrar.rar');
echo $rar_arch."\n";
$rar_arch->close();
echo $rar_arch."\n";
?>
```

以上例程的输出类似于：

    RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar"
    RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar" (closed)

简介
----

A RAR entry, representing a directory or a compressed file inside a RAR
archive.

类摘要
------

**RarEntry**

<span class="ooclass"> <span class="modifier">final</span> class
**RarEntry** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::HOST_MSDOS` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::HOST_OS2` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::HOST_WIN32` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::HOST_UNIX` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::HOST_MACOS` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::HOST_BEOS` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_READONLY` <span class="initializer"> = 1</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_HIDDEN` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_SYSTEM` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_DIRECTORY` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_ARCHIVE` <span class="initializer"> = 32</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_DEVICE` <span class="initializer"> = 64</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_NORMAL` <span class="initializer"> = 128</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_TEMPORARY` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_SPARSE_FILE` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_REPARSE_POINT` <span class="initializer"> =
1024</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_COMPRESSED` <span class="initializer"> =
2048</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_OFFLINE` <span class="initializer"> =
4096</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_NOT_CONTENT_INDEXED` <span class="initializer">
= 8192</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_ENCRYPTED` <span class="initializer"> =
16384</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_WIN_VIRTUAL` <span class="initializer"> =
65536</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_WORLD_EXECUTE` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_WORLD_WRITE` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_WORLD_READ` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_GROUP_EXECUTE` <span class="initializer"> =
8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_GROUP_WRITE` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_GROUP_READ` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_OWNER_EXECUTE` <span class="initializer"> =
64</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_OWNER_WRITE` <span class="initializer"> =
128</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_OWNER_READ` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_STICKY` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_SETGID` <span class="initializer"> =
1024</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_SETUID` <span class="initializer"> =
2048</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET` <span class="initializer"> =
61440</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_FIFO` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_CHAR_DEV` <span class="initializer"> =
8192</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_DIRECTORY` <span class="initializer"> =
16384</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_BLOCK_DEV` <span class="initializer"> =
24576</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_REGULAR_FILE` <span class="initializer"> =
32768</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_SYM_LINK` <span class="initializer"> =
40960</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`RarEntry::ATTRIBUTE_UNIX_SOCKET` <span class="initializer"> =
49152</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">extract</span> ( <span
class="methodparam"><span class="type">string</span> `$dir`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$filepath`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$extended_data`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getAttr</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getCrc</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getFileTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getHostOs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getMethod</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPackedSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">getStream</span> (\[ <span
class="methodparam"><span class="type">string</span> `$password`</span>
\] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getUnpackedSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isDirectory</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEncrypted</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`RarEntry::HOST_MSDOS`**  
If the return value of <span
class="methodname">RarEntry::getHostOs</span> equals this constant,
MS-DOS was used to add this entry. Use instead of **`RAR_HOST_MSDOS`**.

**`RarEntry::HOST_OS2`**  
If the return value of <span
class="methodname">RarEntry::getHostOs</span> equals this constant, OS/2
was used to add this entry. Intended to replace **`RAR_HOST_OS2`**.

**`RarEntry::HOST_WIN32`**  
If the return value of <span
class="methodname">RarEntry::getHostOs</span> equals this constant,
Microsoft Windows was used to add this entry. Intended to replace
**`RAR_HOST_WIN32`**.

**`RarEntry::HOST_UNIX`**  
If the return value of <span
class="methodname">RarEntry::getHostOs</span> equals this constant, an
unspecified UNIX OS was used to add this entry. Intended to replace
**`RAR_HOST_UNIX`**.

**`RarEntry::HOST_MACOS`**  
If the return value of <span
class="methodname">RarEntry::getHostOs</span> equals this constant, Mac
OS was used to add this entry.

**`RarEntry::HOST_BEOS`**  
If the return value of <span
class="methodname">RarEntry::getHostOs</span> equals this constant, BeOS
was used to add this entry. Intended to replace **`RAR_HOST_BEOS`**.

**`RarEntry::ATTRIBUTE_WIN_READONLY`**  
Bit that represents a Windows entry with a read-only attribute. To be
used with <span class="methodname">RarEntry::getAttr</span> on entries
whose host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_HIDDEN`**  
Bit that represents a Windows entry with a hidden attribute. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_SYSTEM`**  
Bit that represents a Windows entry with a system attribute. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_DIRECTORY`**  
Bit that represents a Windows entry with a directory attribute (entry is
a directory). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
Microsoft Windows. See also <span
class="methodname">RarEntry::isDirectory</span>, which also works with
entries that were not added in WinRAR.

**`RarEntry::ATTRIBUTE_WIN_ARCHIVE`**  
Bit that represents a Windows entry with an archive attribute. To be
used with <span class="methodname">RarEntry::getAttr</span> on entries
whose host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_DEVICE`**  
Bit that represents a Windows entry with a device attribute. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_NORMAL`**  
Bit that represents a Windows entry with a normal file attribute (entry
is NOT a directory). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
Microsoft Windows. See also <span
class="methodname">RarEntry::isDirectory</span>, which also works with
entries that were not added in WinRAR.

**`RarEntry::ATTRIBUTE_WIN_TEMPORARY`**  
Bit that represents a Windows entry with a temporary attribute. To be
used with <span class="methodname">RarEntry::getAttr</span> on entries
whose host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_SPARSE_FILE`**  
Bit that represents a Windows entry with a sparse file attribute (file
is an NTFS sparse file). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_REPARSE_POINT`**  
Bit that represents a Windows entry with a reparse point attribute
(entry is an NTFS reparse point, e.g. a directory junction or a mount
file system). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_COMPRESSED`**  
Bit that represents a Windows entry with a compressed attribute (NTFS
only). To be used with <span class="methodname">RarEntry::getAttr</span>
on entries whose host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_OFFLINE`**  
Bit that represents a Windows entry with an offline attribute (entry is
offline and not accessible). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_NOT_CONTENT_INDEXED`**  
Bit that represents a Windows entry with a not content indexed attribute
(entry is to be indexed). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_ENCRYPTED`**  
Bit that represents a Windows entry with an encrypted attribute (NTFS
only). To be used with <span class="methodname">RarEntry::getAttr</span>
on entries whose host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_WIN_VIRTUAL`**  
Bit that represents a Windows entry with a virtual attribute. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is Microsoft Windows.

**`RarEntry::ATTRIBUTE_UNIX_WORLD_EXECUTE`**  
Bit that represents a UNIX entry that is world executable. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_WORLD_WRITE`**  
Bit that represents a UNIX entry that is world writable. To be used with
<span class="methodname">RarEntry::getAttr</span> on entries whose host
OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_WORLD_READ`**  
Bit that represents a UNIX entry that is world readable. To be used with
<span class="methodname">RarEntry::getAttr</span> on entries whose host
OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_GROUP_EXECUTE`**  
Bit that represents a UNIX entry that is group executable. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_GROUP_WRITE`**  
Bit that represents a UNIX entry that is group writable. To be used with
<span class="methodname">RarEntry::getAttr</span> on entries whose host
OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_GROUP_READ`**  
Bit that represents a UNIX entry that is group readable. To be used with
<span class="methodname">RarEntry::getAttr</span> on entries whose host
OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_OWNER_EXECUTE`**  
Bit that represents a UNIX entry that is owner executable. To be used
with <span class="methodname">RarEntry::getAttr</span> on entries whose
host OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_OWNER_WRITE`**  
Bit that represents a UNIX entry that is owner writable. To be used with
<span class="methodname">RarEntry::getAttr</span> on entries whose host
OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_OWNER_READ`**  
Bit that represents a UNIX entry that is owner readable. To be used with
<span class="methodname">RarEntry::getAttr</span> on entries whose host
OS is UNIX.

**`RarEntry::ATTRIBUTE_UNIX_STICKY`**  
Bit that represents the UNIX sticky bit. To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
UNIX.

**`RarEntry::ATTRIBUTE_UNIX_SETGID`**  
Bit that represents the UNIX setgid attribute. To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
UNIX.

**`RarEntry::ATTRIBUTE_UNIX_SETUID`**  
Bit that represents the UNIX setuid attribute. To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
UNIX.

**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**  
Mask to isolate the last four bits (nibble) of UNIX attributes
(\_S\_IFMT, the type of file mask). To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
UNIX and with the constants
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FIFO</code></strong></a>,
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_CHAR_DEV</code></strong></a>,
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_DIRECTORY</code></strong></a>,
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_BLOCK_DEV</code></strong></a>,
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_REGULAR_FILE</code></strong></a>,
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_SYM_LINK</code></strong></a>
and
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_SOCKET</code></strong></a>.

**`RarEntry::ATTRIBUTE_UNIX_FIFO`**  
Unix FIFOs will have attributes whose last four bits have this value. To
be used with <span class="methodname">RarEntry::getAttr</span> on
entries whose host OS is UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.

**`RarEntry::ATTRIBUTE_UNIX_CHAR_DEV`**  
Unix character devices will have attributes whose last four bits have
this value. To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.

**`RarEntry::ATTRIBUTE_UNIX_DIRECTORY`**  
Unix directories will have attributes whose last four bits have this
value. To be used with <span class="methodname">RarEntry::getAttr</span>
on entries whose host OS is UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.
See also <span class="methodname">RarEntry::isDirectory</span>, which
also works with entries that were added in other operating systems.

**`RarEntry::ATTRIBUTE_UNIX_BLOCK_DEV`**  
Unix block devices will have attributes whose last four bits have this
value. To be used with <span class="methodname">RarEntry::getAttr</span>
on entries whose host OS is UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.

**`RarEntry::ATTRIBUTE_UNIX_REGULAR_FILE`**  
Unix regular files (not directories) will have attributes whose last
four bits have this value. To be used with <span
class="methodname">RarEntry::getAttr</span> on entries whose host OS is
UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.
See also <span class="methodname">RarEntry::isDirectory</span>, which
also works with entries that were added in other operating systems.

**`RarEntry::ATTRIBUTE_UNIX_SYM_LINK`**  
Unix symbolic links will have attributes whose last four bits have this
value. To be used with <span class="methodname">RarEntry::getAttr</span>
on entries whose host OS is UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.

**`RarEntry::ATTRIBUTE_UNIX_SOCKET`**  
Unix sockets will have attributes whose last four bits have this value.
To be used with <span class="methodname">RarEntry::getAttr</span> on
entries whose host OS is UNIX and with the constant
<a href="/class/rarentry.html#" class="link"><strong><code>RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET</code></strong></a>.

RarEntry::extract
=================

Extract entry from the archive

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarEntry::extract</span> ( <span
class="methodparam"><span class="type">string</span> `$dir`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$filepath`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$password`<span
class="initializer"> = NULL</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$extended_data`<span
class="initializer"> = **`FALSE`**</span></span> \]\]\] )

<span class="methodname">RarEntry::extract</span> extracts the entry's
data. It will create new file in the specified `dir` with the name
identical to the entry's name, unless the second argument is specified.
See below for more information.

### 参数

`dir`  
Path to the directory where files should be extracted. This parameter is
considered if and only if `filepath` is not. If both parameters are
empty an extraction to the current directory will be attempted.

`filepath`  
Path (relative or absolute) containing the directory and filename of the
extracted file. This parameter overrides both the parameter `dir` and
the original file name.

`password`  
The password used to encrypt this entry. If the entry is not encrypted,
this value will not be used and can be omitted. If this parameter is
omitted and the entry is encrypted, the password given to <span
class="function">rar\_open</span>, if any, will be used. If a wrong
password is given, either explicitly or implicitly via <span
class="function">rar\_open</span>, CRC checking will fail and this
method will fail and return **`FALSE`**. If no password is given and one
is required, this method will fail and return **`FALSE`**. You can check
whether an entry is encrypted with <span
class="methodname">RarEntry::isEncrypted</span>.

`extended_data`  
If **`TRUE`**, extended information such as NTFS ACLs and Unix owner
information will be set in the extract files, as long as it's present in
the archive.

**Warning**

Prior to version 2.0.0, this function would not handle relative paths
correctly. Use <span class="function">realpath</span> as a workaround.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本           | 说明                                                                       |
|----------------|----------------------------------------------------------------------------|
| PECL rar 3.0.0 | `extended_data` was added.                                                 |
| PECL rar 3.0.0 | Support for RAR archives with repeated entry names is no longer defective. |

### 范例

**示例 \#1 <span class="methodname">RarEntry::extract</span> example**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

$entry->extract('/dir/to'); // create /dir/to/Dir/file.txt
$entry->extract(false, '/dir/to/new_name.txt'); // create /dir/to/new_name.txt

?>
```

**示例 \#2 How to extract all files in archive:**

``` php
<?php

/* example by Erik Jenssen aka erix */

$filename = "foobar.rar";
$filepath = "/home/foo/bar/";

$rar_file = rar_open($filepath.$filename);
$list = rar_list($rar_file);
foreach($list as $file) {
    $entry = rar_entry_get($rar_file, $file);
    $entry->extract("."); // extract to the current dir
}
rar_close($rar_file);

?>
```

### 参见

-   <span class="methodname">RarEntry::getStream</span>
-   <a href="/wrappers/rar.html" class="link"><em>rar://</em> wrapper</a>

RarEntry::getAttr
=================

Get attributes of the entry

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RarEntry::getAttr</span> ( <span
class="methodparam">void</span> )

Returns the OS-dependent attributes of the archive entry.

### 参数

此函数没有参数。

### 返回值

Returns the attributes or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="methodname">RarEntry::getAttr</span> example**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Can't open Rar archive");

$entry = rar_entry_get($rar_file, 'dir/in/the/archive') or die("Can't find such entry");

$host_os = $entry->getHostOs();
$attr = $entry->getAttr();

switch($host_os) {
    case RAR_HOST_MSDOS:
    case RAR_HOST_OS2:
    case RAR_HOST_WIN32:
    case RAR_HOST_MACOS:
        printf("%c%c%c%c%c%c\n",
                ($attr & 0x08) ? 'V' : '.',
                ($attr & 0x10) ? 'D' : '.',
                ($attr & 0x01) ? 'R' : '.',
                ($attr & 0x02) ? 'H' : '.',
                ($attr & 0x04) ? 'S' : '.',
                ($attr & 0x20) ? 'A' : '.');
        break;
    case RAR_HOST_UNIX:
    case RAR_HOST_BEOS:
        switch ($attr & 0xF000)
        {
            case 0x4000:
                printf("d");
                break;
            case 0xA000:
                printf("l");
                break;
            default:
                printf("-");
                break;
        }
        printf("%c%c%c%c%c%c%c%c%c\n",
                ($attr & 0x0100) ? 'r' : '-',
                ($attr & 0x0080) ? 'w' : '-',
                ($attr & 0x0040) ? (($attr & 0x0800) ? 's':'x'):(($attr & 0x0800) ? 'S':'-'),
                ($attr & 0x0020) ? 'r' : '-',
                ($attr & 0x0010) ? 'w' : '-',
                ($attr & 0x0008) ? (($attr & 0x0400) ? 's':'x'):(($attr & 0x0400) ? 'S':'-'),
                ($attr & 0x0004) ? 'r' : '-',
                ($attr & 0x0002) ? 'w' : '-',
                ($attr & 0x0001) ? 'x' : '-');
        break;
}

rar_close($rar_file);

?>
```

### 参见

-   <span class="methodname">RarEntry::getHostOs</span>
-   The constants in <span class="classname">RarEntry</span>

RarEntry::getCrc
================

Get CRC of the entry

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RarEntry::getCrc</span> ( <span
class="methodparam">void</span> )

Returns an hexadecimal string representation of the CRC of the archive
entry.

### 参数

此函数没有参数。

### 返回值

Returns the CRC of the archive entry or **`FALSE`** on error.

### 更新日志

| 版本           | 说明                                                                 |
|----------------|----------------------------------------------------------------------|
| PECL rar 2.0.0 | This method now returns correct values for multiple volume archives. |

RarEntry::getFileTime
=====================

Get entry last modification time

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RarEntry::getFileTime</span> ( <span
class="methodparam">void</span> )

Gets entry last modification time.

### 参数

此函数没有参数。

### 返回值

Returns entry last modification time as string in format *YYYY-MM-DD
HH:II:SS*, or **`FALSE`** on error.

RarEntry::getHostOs
===================

Get entry host OS

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RarEntry::getHostOs</span> ( <span
class="methodparam">void</span> )

Returns the code of the host OS of the archive entry.

### 参数

此函数没有参数。

### 返回值

Returns the code of the host OS, or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="methodname">RarEntry::getHostOs</span> example
(version \>= 2.0.0)**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

switch ($entry->getHostOs()) {
    case RarEntry::HOST_MSDOS:
        echo "MS-DOS\n";
        break;
    case RarEntry::HOST_OS2:
        echo "OS2\n";
        break;
    case RarEntry::HOST_WIN32:
        echo "Win32\n";
        break;
    case RarEntry::HOST_MACOS:
        echo "MacOS\n";
        break;
    case RarEntry::HOST_UNIX:
        echo "Unix/Linux\n";
        break;
    case RarEntry::HOST_BEOS:
        echo "BeOS\n";
        break;
}

?>
```

**示例 \#2 <span class="methodname">RarEntry::getHostOs</span> example
(version \<= 1.0.0)**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

switch ($entry->getHostOs()) {
    case RAR_HOST_MSDOS:
        echo "MS-DOS\n";
        break;
    case RAR_HOST_OS2:
        echo "OS2\n";
        break;
    case RAR_HOST_WIN32:
        echo "Win32\n";
        break;
    case RAR_HOST_MACOS:
        echo "MacOS\n";
        break;
    case RAR_HOST_UNIX:
        echo "Unix/Linux\n";
        break;
    case RAR_HOST_BEOS:
        echo "BeOS\n";
        break;
}

?>
```

### 参见

-   <span class="methodname">RarEntry::extract</span>

RarEntry::getMethod
===================

Get pack method of the entry

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RarEntry::getMethod</span> ( <span
class="methodparam">void</span> )

<span class="methodname">RarEntry::getMethod</span> returns number of
the method used when adding current archive entry.

### 参数

此函数没有参数。

### 返回值

Returns the method number or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="methodname">RarEntry::getMethod</span> example**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

echo "Method number: " . $entry->getMethod();

?>
```

RarEntry::getName
=================

Get name of the entry

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RarEntry::getName</span> ( <span
class="methodparam">void</span> )

Returns the name (with path) of the archive entry.

### 参数

此函数没有参数。

### 返回值

Returns the entry name as a string, or **`FALSE`** on error.

### 更新日志

| 版本           | 说明                                                                  |
|----------------|-----------------------------------------------------------------------|
| PECL rar 2.0.0 | As of version 2.0.0, the returned string is encoded in Unicode/UTF-8. |

### 范例

**示例 \#1 <span class="methodname">RarEntry::getName</span> example**

``` php
<?php

//this example is safe even in pages not encoded in UTF-8
//for those encoded in UTF-8, the call to mb_convert_encoding is unnecessary

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

echo "Entry name: " . mb_convert_encoding(
    htmlentities(
        $entry->getName(),
        ENT_COMPAT,
        "UTF-8"
    ),
    "HTML-ENTITIES",
    "UTF-8"
);

?>
```

RarEntry::getPackedSize
=======================

Get packed size of the entry

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RarEntry::getPackedSize</span> ( <span
class="methodparam">void</span> )

Get packed size of the archive entry.

> **Note**:
>
> Note that on platforms with 32-bit longs (that includes Windows x64),
> the maximum size returned is capped at 2 GiB. Check the constant
> **`PHP_INT_MAX`**.

### 参数

此函数没有参数。

### 返回值

Returns the packed size, or **`FALSE`** on error.

### 更新日志

| 版本           | 说明                                                                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL rar 2.0.0 | This method now returns correct values of packed sizes bigger than 2 GiB on platforms with 64-bit <span class="type">integer</span>s and never returns negative values on other platforms. |

### 范例

**示例 \#1 <span class="methodname">RarEntry::getPackedSize</span>
example**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

echo "Packed size of " . $entry->getName() . " = " . $entry->getPackedSize() . " bytes";

?>
```

RarEntry::getStream
===================

Get file handler for entry

### 说明

<span class="modifier">public</span> <span class="type">resource</span>
<span class="methodname">RarEntry::getStream</span> (\[ <span
class="methodparam"><span class="type">string</span> `$password`</span>
\] )

Returns a file handler that supports read operations. This handler
provides on-the-fly decompression for this entry.

The handler is not invalidated by calling <span
class="function">rar\_close</span>.

**Warning**

The resulting stream has no integrity verification. In particular, file
corruption and decryption with a wrong a key will not be detected. It is
the programmer's responsability to use the entry's CRC to check for
integrity, if he so wishes.

### 参数

`password`  
The password used to encrypt this entry. If the entry is not encrypted,
this value will not be used and can be omitted. If this parameter is
omitted and the entry is encrypted, the password given to <span
class="function">rar\_open</span>, if any, will be used. If a wrong
password is given, either explicitly or implicitly via <span
class="function">rar\_open</span>, this method's resulting stream will
produce wrong output. If no password is given and one is required, this
method will fail and return **`FALSE`**. You can check whether an entry
is encrypted with <span class="methodname">RarEntry::isEncrypted</span>.

### 返回值

The file handler 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本           | 说明                                                                       |
|----------------|----------------------------------------------------------------------------|
| PECL rar 3.0.0 | Support for RAR archives with repeated entry names is no longer defective. |

### 范例

**示例 \#1 <span class="methodname">RarEntry::getStream</span> example**

``` php
<?php

$rar_file = rar_open('example.rar');
if ($rar_file === false)
    die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt');
if ($entry === false)
    die("Failed to find such entry");

$stream = $entry->getStream();
if ($stream === false)
    die("Failed to obtain stream.");

rar_close($rar_file); //stream is independent from file

while (!feof($stream)) {
    $buff = fread($stream, 8192);
    if ($buff !== false)
        echo $buff;
    else
        break; //fread error
}

fclose($stream);

?>
```

### 参见

-   <span class="methodname">RarEntry::extract</span>
-   <a href="/wrappers/rar.html" class="link"><em>rar://</em> wrapper</a>

RarEntry::getUnpackedSize
=========================

Get unpacked size of the entry

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RarEntry::getUnpackedSize</span> ( <span
class="methodparam">void</span> )

Get unpacked size of the archive entry.

> **Note**:
>
> Note that on platforms with 32-bit longs (that includes Windows x64),
> the maximum size returned is capped at 2 GiB. Check the constant
> **`PHP_INT_MAX`**.

### 参数

此函数没有参数。

### 返回值

Returns the unpacked size, or **`FALSE`** on error.

### 更新日志

| 版本           | 说明                                                                                                                                                                                         |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL rar 2.0.0 | This method now returns correct values of unpacked sizes bigger than 2 GiB on platforms with 64-bit <span class="type">integer</span>s and never returns negative values on other platforms. |

### 返回值

**示例 \#1 <span class="methodname">RarEntry::getUnpackedSize</span>
example**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

echo "Unpacked size of " . $entry->getName() . " = " . $entry->getPackedSize() . " bytes";

?>
```

RarEntry::getVersion
====================

Get minimum version of RAR program required to unpack the entry

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">RarEntry::getVersion</span> ( <span
class="methodparam">void</span> )

Returns minimum version of RAR program (e.g. WinRAR) required to unpack
the entry. It is encoded as 10 \* major version + minor version.

### 参数

此函数没有参数。

### 返回值

Returns the version or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="methodname">RarEntry::getVersion</span>
example**

``` php
<?php

$rar_file = rar_open('example.rar') or die("Failed to open Rar archive");

$entry = rar_entry_get($rar_file, 'Dir/file.txt') or die("Failed to find such entry");

echo "Rar version required for unpacking: " . $entry->getVersion();

?>
```

RarEntry::isDirectory
=====================

Test whether an entry represents a directory

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarEntry::isDirectory</span> ( <span
class="methodparam">void</span> )

Tests whether the current entry is a directory.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this entry is a directory and **`FALSE`**
otherwise.

### 注释

This function is only available starting with version 2.0.0, but one can
also test whether an entry is a directory by checking the entry
attributes, like this (only works for files compressed in RAR for
Windows or Unix):

``` php
<?php
//...
//Open file, get entry and store in variable $e...
//...

$isDirectory = (bool) ((($e->getHostOs() == RAR_HOST_WIN32) && ($e->getAttr() & 0x10)) ||
    (($e->getHostOs() == RAR_HOST_UNIX) && (($e->getAttr() & 0xf000) == 0x4000)));
?>
```

RarEntry::isEncrypted
=====================

Test whether an entry is encrypted

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RarEntry::isEncrypted</span> ( <span
class="methodparam">void</span> )

Tests whether the current entry contents are encrypted.

> **Note**:
>
> The password used may differ between files inside the same RAR
> archive.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the current entry is encrypted and **`FALSE`**
otherwise.

RarEntry::\_\_toString
======================

Get text representation of entry

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">RarEntry::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="methodname">RarEntry::\_\_toString</span> returns a textual
representation for this entry. It includes whether the entry is a file
or a directory (symbolic links and other special objects will be treated
as files), the UTF-8 name of the entry and its CRC. The form and content
of this representation may be changed in the future, so they cannot be
relied upon.

### 参数

此函数没有参数。

### 返回值

A textual representation for the entry.

简介
----

This class serves two purposes: it is the type of the exceptions thrown
by the RAR extension functions and methods and it allows, through static
methods to query and define the error behaviour of the extension, i.e.,
whether exceptions are thrown or only warnings are emitted.

The following error codes are used:

-   <span class="simpara"> -1 - error outside UnRAR library </span>
-   <span class="simpara"> 11 - insufficient memory </span>
-   <span class="simpara"> 12 - bad data </span>
-   <span class="simpara"> 13 - bad archive </span>
-   <span class="simpara"> 14 - unknown format </span>
-   <span class="simpara"> 15 - file open error </span>
-   <span class="simpara"> 16 - file create error </span>
-   <span class="simpara"> 17 - file close error </span>
-   <span class="simpara"> 18 - read error </span>
-   <span class="simpara"> 19 - write error </span>
-   <span class="simpara"> 20 - buffer too small </span>
-   <span class="simpara"> 21 - unknown RAR error </span>
-   <span class="simpara"> 22 - password required but not given </span>

类摘要
------

**RarException**

<span class="ooclass"> <span class="modifier">final</span> class
**RarException** </span> <span class="ooclass"> <span
class="modifier">extends</span> **Exception** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">isUsingExceptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">setUsingExceptions</span> ( <span
class="methodparam"><span class="type">bool</span>
`$using_exceptions`</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

RarException::isUsingExceptions
===============================

Check whether error handling with exceptions is in use

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">RarException::isUsingExceptions</span> ( <span
class="methodparam">void</span> )

Checks whether the RAR functions will emit warnings and return error
values or whether they will throw exceptions in most of the
circumstances (does not include some programmatic errors such as passing
the wrong type of arguments).

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if exceptions are being used, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">RarException::isUsingExceptions</span>
example**

``` php
<?php
//The default is not to use exceptions
var_dump(RarException::isUsingExceptions());
?>
```

以上例程的输出类似于：

    bool(false)

### 参见

-   <span class="methodname">RarException::setUsingExceptions</span>

RarException::setUsingExceptions
================================

Activate and deactivate error handling with exceptions

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">RarException::setUsingExceptions</span> ( <span
class="methodparam"><span class="type">bool</span>
`$using_exceptions`</span> )

If and only if the argument is **`TRUE`**, then, instead of emitting
warnings and returning a special value indicating error when the UnRAR
library encounters an error, an exception of type <span
class="type">RarException</span> will be thrown.

Exceptions will also be thrown for the following errors, which occur
outside the library (their error code will be -1):

-   <span class="simpara"> attempting some operations on a closed <span
    class="type">RarArchive</span> object or a <span
    class="type">RarEntry</span> object relative to the first; </span>
-   <span class="simpara"> attempting to get an entry that does not
    exist with <span class="methodname">RarArchive::getEntry</span>.
    </span>

### 参数

`using_exceptions`  
Should be **`TRUE`** to activate exception throwing, **`FALSE`** to
deactivate (the default).

### 范例

**示例 \#1 <span
class="function">RarException::setUsingExceptions</span> example**

``` php
<?php
var_dump(RarException::isUsingExceptions());
$arch = RarArchive::open("does_not_exist.rar");
var_dump($arch);

RarException::setUsingExceptions(true);
var_dump(RarException::isUsingExceptions());
$arch = RarArchive::open("does_not_exist.rar");
var_dump($arch); //not reached
?>
```

以上例程的输出类似于：

    bool(false)

    Warning: RarArchive::open(): Failed to open does_not_exist.rar: ERAR_EOPEN (file open error) in C:\php_rar\trunk\tests\test.php on line 3
    bool(false)
    bool(true)

    Fatal error: Uncaught exception 'RarException' with message 'unRAR internal error: Failed to open does_not_exist.rar: ERAR_EOPEN (file open error)' in C:\php_rar\trunk\tests\test.php:8
    Stack trace:
    #0 C:\php_rar\trunk\tests\test.php(8): RarArchive::open('does_not_exist....')
    #1 {main}
      thrown in C:\php_rar\trunk\tests\test.php on line 8

### 参见

-   <span class="methodname">RarException::isUsingExceptions</span>
