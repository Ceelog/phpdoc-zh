Database (dbm-style) Abstraction Layer
======================================

**目录**

-   [简介](/book/dba.html#简介)
-   [安装／配置](/book/dba.html#安装／配置)
    -   [需求](/book/dba.html#需求)
    -   [安装](/book/dba.html#安装)
    -   [运行时配置](/book/dba.html#运行时配置)
    -   [资源类型](/book/dba.html#资源类型)
-   [预定义常量](/book/dba.html#预定义常量)
-   [范例](/book/dba.html#范例)
    -   [Basic usage](/book/dba.html#Basic%20usage)
-   [DBA 函数](/book/dba.html#DBA%20函数)
    -   [dba\_close](/book/dba.html#dba_close) — Close a DBA database
    -   [dba\_delete](/book/dba.html#dba_delete) — Delete DBA entry
        specified by key
    -   [dba\_exists](/book/dba.html#dba_exists) — Check whether key
        exists
    -   [dba\_fetch](/book/dba.html#dba_fetch) — Fetch data specified by
        key
    -   [dba\_firstkey](/book/dba.html#dba_firstkey) — Fetch first key
    -   [dba\_handlers](/book/dba.html#dba_handlers) — List all the
        handlers available
    -   [dba\_insert](/book/dba.html#dba_insert) — Insert entry
    -   [dba\_key\_split](/book/dba.html#dba_key_split) — Splits a key
        in string representation into array representation
    -   [dba\_list](/book/dba.html#dba_list) — List all open database
        files
    -   [dba\_nextkey](/book/dba.html#dba_nextkey) — Fetch next key
    -   [dba\_open](/book/dba.html#dba_open) — Open database
    -   [dba\_optimize](/book/dba.html#dba_optimize) — Optimize database
    -   [dba\_popen](/book/dba.html#dba_popen) — Open database
        persistently
    -   [dba\_replace](/book/dba.html#dba_replace) — Replace or insert
        entry
    -   [dba\_sync](/book/dba.html#dba_sync) — Synchronize database

These functions build the foundation for accessing Berkeley DB style
databases.

This is a general abstraction layer for several file-based databases. As
such, functionality is limited to a common subset of features supported
by modern databases such as
<a href="https://www.oracle.com/database/berkeley-db/db.html" class="link external">» Oracle Berkeley DB</a>.

安装／配置
==========

**目录**

-   [需求](/book/dba.html#需求)
-   [安装](/book/dba.html#安装)
-   [运行时配置](/book/dba.html#运行时配置)
-   [资源类型](/book/dba.html#资源类型)

需求
----

The behaviour of various aspects depends on the implementation of the
underlying database. Functions such as <span
class="function">dba\_optimize</span> and <span
class="function">dba\_sync</span> will do what they promise for one
database and will do nothing for others. You have to download and
install supported dba-Handlers.

| Handler     | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dbm*       | Dbm is the oldest (original) type of Berkeley DB style databases. You should avoid it, if possible. We do not support the compatibility functions built into DB2 and gdbm, because they are only compatible on the source code level, but cannot handle the original dbm format.                                                                                                                                                                                                                                                                                |
| *ndbm*      | Ndbm is a newer type and more flexible than dbm. It still has most of the arbitrary limits of dbm (therefore it is deprecated).                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *gdbm*      | Gdbm is the <a href="ftp://ftp.gnu.org/pub/gnu/gdbm/" class="link external">» GNU database manager</a>.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *db2*       | DB2 is for <a href="http://www.sleepycat.com/" class="link external">» Oracle Berkeley DB 2</a>. It is described as "a programmatic toolkit that provides high-performance built-in database support for both standalone and client/server applications."                                                                                                                                                                                                                                                                                                       |
| *db3*       | DB3 is for <a href="http://www.sleepycat.com/" class="link external">» Oracle Berkeley DB 3</a>.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| *db4*       | DB4 is for <a href="http://www.sleepycat.com/" class="link external">» Oracle Berkeley DB 4 or 5</a>. This option can be used with BDB 5 as of PHP 5.3.3.                                                                                                                                                                                                                                                                                                                                                                                                       |
| *cdb*       | Cdb is "a fast, reliable, lightweight package for creating and reading constant databases." It is from the author of qmail and can be found at <a href="http://cr.yp.to/cdb.html" class="link external">» http://cr.yp.to/cdb.html</a>. Since it is constant, we support only reading operations. We support writing (not updating) through the internal cdb library.                                                                                                                                                                                           |
| *cdb\_make* | We support creation (not updating) of cdb files when the bundled cdb library is used.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *flatfile*  | This is available for compatibility with the deprecated *dbm* extension only and should be avoided. However you may use this where files were created in this format. That happens when configure could not find any external library.                                                                                                                                                                                                                                                                                                                          |
| *inifile*   | This is available to be able to modify php.ini files from within PHP scripts. When working with ini files you can pass arrays of the form array(0=\>group,1=\>value\_name) or strings of the form "\[group\]value\_name" where group is optional. As the functions <span class="function">dba\_firstkey</span> and <span class="function">dba\_nextkey</span> return string representations of the key there is the function <span class="function">dba\_key\_split</span> which allows to convert the string keys into array keys without loosing **`FALSE`**. |
| *qdbm*      | The qdbm library can be downloaded from <a href="http://fallabs.com/qdbm/index.html" class="link external">» http://fallabs.com/qdbm/index.html</a>.                                                                                                                                                                                                                                                                                                                                                                                                            |
| *tcadb*     | This is available since PHP 5.4.0. The Tokyo Cabinet library can be downloaded from <a href="http://fallabs.com/tokyocabinet/" class="link external">» http://fallabs.com/tokyocabinet/</a>.                                                                                                                                                                                                                                                                                                                                                                    |
| *lmdb*      | This is available since PHP 7.2.0. The Lightning Memory-Mapped Database library can be downloaded from <a href="https://symas.com/lmdb/" class="link external">» https://symas.com/lmdb/</a>.                                                                                                                                                                                                                                                                                                                                                                   |

When invoking the <span class="function">dba\_open</span> or <span
class="function">dba\_popen</span> functions, one of the handler names
must be supplied as an argument. The actually available list of handlers
is displayed by invoking <span class="function">phpinfo</span> or <span
class="function">dba\_handlers</span>.

安装
----

By using the **--enable-dba=shared** configuration option you can build
a dynamic loadable module to enable PHP for basic support of dbm-style
databases. You also have to add support for at least one of the
following handlers by specifying the **--with-XXXX** or
**--enable-XXXX** configure switch to your PHP configure line.

**Warning**

After configuring and compiling PHP you must execute the following test
from commandline: *php run-tests.php ext/dba*. This shows whether your
combination of handlers works. Most problematic are *dbm* and *ndbm*
which conflict with many installations. The reason for this is that on
several systems these libraries are part of more than one other library.
The configuration test only prevents you from configuring malfunctioning
single handlers but not combinations.

<table>
<caption><strong>Supported DBA handlers</strong></caption>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Handler</th>
<th>Configure Switch</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>dbm</em></td>
<td><p>To enable support for dbm add <strong>--with-dbm[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>dbm normally is a wrapper which often results in failures. This means you should only use dbm if you are sure it works and if you really need this format.</p>
</blockquote></td>
</tr>
<tr class="even">
<td><em>ndbm</em></td>
<td><p>To enable support for ndbm add <strong>--with-ndbm[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>ndbm normally is a wrapper which often results in failures. This means you should only use ndbm if you are sure it works and if you really need this format.</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><em>gdbm</em></td>
<td>To enable support for gdbm add <strong>--with-gdbm[=DIR]</strong>.</td>
</tr>
<tr class="even">
<td><em>db2</em></td>
<td><p>To enable support for Oracle Berkeley DB 2 add <strong>--with-db2[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>db2 conflicts with db3 and db4.</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><em>db3</em></td>
<td><p>To enable support for Oracle Berkeley DB 3 add <strong>--with-db3[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>db3 conflicts with db2 and db4.</p>
</blockquote></td>
</tr>
<tr class="even">
<td><em>db4</em></td>
<td><p>To enable support for Oracle Berkeley DB 4 or 5 add <strong>--with-db4[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>db4 conflicts with db2 and db3.</p>
</blockquote>
<blockquote>
<p><strong>Note</strong>:</p>
<p>The db libraries with versions 4.1 through 4.1.24 cannot be used in any PHP version.</p>
<p>Support for BDB 5 was added in PHP 5.3.3.</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><em>cdb</em></td>
<td><p>To enable support for cdb add <strong>--with-cdb[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>You can omit DIR to use the bundled cdb library that adds the cdb_make handler which allows creation of cdb files and allows to access cdb files on the network using PHP's streams.</p>
</blockquote></td>
</tr>
<tr class="even">
<td><em>flatfile</em></td>
<td><p>To enable support for flatfile add <strong>--enable-flatfile</strong>. Before PHP 5.2.1 the <strong>--with-flatfile</strong> had to be used instead.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>This was added to add compatibility with deprecated <em>dbm</em> extension. Use this handler only when you cannot install one of the libraries required by the other handlers and when you cannot use bundled cdb handler.</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><em>inifile</em></td>
<td><p>To enable support for <em>inifile</em> add <strong>--enable-inifile</strong>. Before PHP 5.2.1 the <strong>--with-inifile</strong> had to be used instead.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>This was added to allow to read and set microsoft style <var class="filename">.ini</var> files (like the <var class="filename">php.ini</var> file).</p>
</blockquote></td>
</tr>
<tr class="even">
<td><em>qdbm</em></td>
<td><p>To enable support for qdbm add <strong>--with-qdbm[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>qdbm conflicts with dbm and gdbm.</p>
</blockquote>
<blockquote>
<p><strong>Note</strong>:</p>
<p>The qdbm library can be downloaded from <a href="http://fallabs.com/qdbm/index.html" class="link external">» http://fallabs.com/qdbm/index.html</a>.</p>
</blockquote></td>
</tr>
<tr class="odd">
<td><em>tcadb</em></td>
<td><p>To enable support for Tokyo Cabinet add <strong>--with-tcadb[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>This was added in PHP 5.4.0. The Tokyo Cabinet library can be downloaded from <a href="http://fallabs.com/tokyocabinet/" class="link external">» http://fallabs.com/tokyocabinet/</a>.</p>
</blockquote></td>
</tr>
<tr class="even">
<td><em>lmdb</em></td>
<td><p>To enable support for the Lightning Memory-Mapped Database add <strong>--with-lmdb[=DIR]</strong>.</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>This was added in PHP 7.2.0. The Lightning Memory-Mapped Database library can be downloaded from <a href="https://symas.com/lmdb/" class="link external">» https://symas.com/lmdb/</a>.</p>
</blockquote></td>
</tr>
</tbody>
</table>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                           | 默认         | 可修改范围    | 更新日志 |
|----------------------------------------------------------------|--------------|---------------|----------|
| <a href="/book/dba.html#" class="link">dba.default_handler</a> | DBA\_DEFAULT | PHP\_INI\_ALL |          |

这是配置指令的简短说明。

`dba.default_handler` <span class="type">string</span>  
The name of the default handler

资源类型
--------

The functions <span class="function">dba\_open</span> and <span
class="function">dba\_popen</span> return a handle to the specified
database file to access which is used by all other dba-function calls.

预定义常量
==========

此扩展没有定义常量。

范例
====

**目录**

-   [Basic usage](/book/dba.html#Basic%20usage)

Basic usage
-----------

**示例 \#1 DBA example**

``` php
<?php

$id = dba_open("/tmp/test.db", "n", "db2");

if (!$id) {
    echo "dba_open failed\n";
    exit;
}

dba_replace("key", "This is an example!", $id);

if (dba_exists("key", $id)) {
    echo dba_fetch("key", $id);
    dba_delete("key", $id);
}

dba_close($id);
?>
```

DBA is binary safe and does not have any arbitrary limits. However, it
inherits all limits set by the underlying database implementation.

All file-based databases must provide a way of setting the file mode of
a new created database, if that is possible at all. The file mode is
commonly passed as the fourth argument to <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

You can access all entries of a database in a linear way by using the
<span class="function">dba\_firstkey</span> and <span
class="function">dba\_nextkey</span> functions. You may not change the
database while traversing it.

**示例 \#2 Traversing a database**

``` php
<?php

// ...open database...

$key = dba_firstkey($id);

while ($key !== false) {
    if (true) {          // remember the key to perform some action later
        $handle_later[] = $key;
    }
    $key = dba_nextkey($id);
}

foreach ($handle_later as $val) {
    dba_delete($val, $id);
}

?>
```

dba\_close
==========

Close a DBA database

### 说明

<span class="type">void</span> <span
class="methodname">dba\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> )

<span class="function">dba\_close</span> closes the established database
and frees all resources of the specified database handle.

### 参数

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">dba\_open</span>
-   <span class="function">dba\_popen</span>

dba\_delete
===========

Delete DBA entry specified by key

### 说明

<span class="type">bool</span> <span
class="methodname">dba\_delete</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="function">dba\_delete</span> deletes the specified entry
from the database.

### 参数

`key`  
The key of the entry which is deleted.

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">dba\_exists</span>
-   <span class="function">dba\_fetch</span>
-   <span class="function">dba\_insert</span>
-   <span class="function">dba\_replace</span>

dba\_exists
===========

Check whether key exists

### 说明

<span class="type">bool</span> <span
class="methodname">dba\_exists</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="function">dba\_exists</span> checks whether the specified
`key` exists in the database.

### 参数

`key`  
The key the check is performed for.

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

Returns **`TRUE`** if the key exists, **`FALSE`** otherwise.

### 参见

-   <span class="function">dba\_delete</span>
-   <span class="function">dba\_fetch</span>
-   <span class="function">dba\_insert</span>
-   <span class="function">dba\_replace</span>

dba\_fetch
==========

Fetch data specified by key

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">dba\_fetch</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">dba\_fetch</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">int</span> `$skip`</span> , <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="function">dba\_fetch</span> fetches the data specified by
`key` from the database specified with `handle`.

### 参数

`key`  
The key the data is specified by.

> **Note**:
>
> When working with inifiles this function accepts arrays as keys where
> index 0 is the group and index 1 is the value name. See: <span
> class="function">dba\_key\_split</span>.

`skip`  
The number of key-value pairs to ignore when using cdb databases. This
value is ignored for all other databases which do not support multiple
keys with the same name.

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

Returns the associated string if the key/data pair is found, **`FALSE`**
otherwise.

### 参见

-   <span class="function">dba\_exists</span>
-   <span class="function">dba\_delete</span>
-   <span class="function">dba\_insert</span>
-   <span class="function">dba\_replace</span>
-   <span class="function">dba\_key\_split</span>

dba\_firstkey
=============

Fetch first key

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">dba\_firstkey</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="function">dba\_firstkey</span> returns the first key of the
database and resets the internal key pointer. This permits a linear
search through the whole database.

### 参数

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

Returns the key on success 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">dba\_nextkey</span>
-   <span class="function">dba\_key\_split</span>
-   Example 2 in the
    <a href="/book/dba.html#范例" class="link">DBA examples</a>

dba\_handlers
=============

List all the handlers available

### 说明

<span class="type">array</span> <span
class="methodname">dba\_handlers</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$full_info`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="function">dba\_handlers</span> list all the handlers
supported by this extension.

### 参数

`full_info`  
Turns on/off full information display in the result.

### 返回值

Returns an array of database handlers. If `full_info` is set to
**`TRUE`**, the array will be associative with the handlers names as
keys, and their version information as value. Otherwise, the result will
be an indexed array of handlers names.

> **Note**:
>
> When the internal cdb library is used you will see *cdb* and
> *cdb\_make*.

### 范例

**示例 \#1 <span class="function">dba\_handlers</span> Example**

``` php
<?php

echo "Available DBA handlers:\n";
foreach (dba_handlers(true) as $handler_name => $handler_version) {
  // clean the versions
  $handler_version = str_replace('$', '', $handler_version);
  echo " - $handler_name: $handler_version\n";
}

?>
```

以上例程的输出类似于：

    Available DBA handlers:
     - cdb: 0.75, Revision: 1.3.2.3 
     - cdb_make: 0.75, Revision: 1.2.2.4 
     - db2: Sleepycat Software: Berkeley DB 2.7.7: (08/20/99)
     - inifile: 1.0, Revision: 1.6.2.3 
     - flatfile: 1.0, Revision: 1.5.2.4 

dba\_insert
===========

Insert entry

### 说明

<span class="type">bool</span> <span
class="methodname">dba\_insert</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

<span class="function">dba\_insert</span> inserts the entry described
with `key` and `value` into the database.

### 参数

`key`  
The key of the entry to be inserted. If this key already exist in the
database, this function will fail. Use <span
class="function">dba\_replace</span> if you need to replace an existent
key.

`value`  
The value to be inserted.

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">dba\_exists</span>
-   <span class="function">dba\_delete</span>
-   <span class="function">dba\_fetch</span>
-   <span class="function">dba\_replace</span>

dba\_key\_split
===============

Splits a key in string representation into array representation

### 说明

<span class="type">mixed</span> <span
class="methodname">dba\_key\_split</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> )

<span class="function">dba\_key\_split</span> splits a key (string
representation) into an array representation.

### 参数

`key`  
The key in string representation.

### 返回值

Returns an array of the form *array(0 =\> group, 1 =\> value\_name)*.
This function will return **`FALSE`** if `key` is **`NULL`** or
**`FALSE`**.

### 参见

-   <span class="function">dba\_firstkey</span>
-   <span class="function">dba\_nextkey</span>
-   <span class="function">dba\_fetch</span>

dba\_list
=========

List all open database files

### 说明

<span class="type">array</span> <span
class="methodname">dba\_list</span> ( <span
class="methodparam">void</span> )

<span class="function">dba\_list</span> list all open database files.

### 返回值

An associative array, in the form *resourceid =\> filename*.

dba\_nextkey
============

Fetch next key

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">dba\_nextkey</span> ( <span class="methodparam"><span
class="type">resource</span> `$handle`</span> )

<span class="function">dba\_nextkey</span> returns the next key of the
database and advances the internal key pointer.

### 参数

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

Returns the key on success 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">dba\_firstkey</span>
-   <span class="function">dba\_key\_split</span>
-   Example 2 in the
    <a href="/book/dba.html#范例" class="link">DBA examples</a>

dba\_open
=========

Open database

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">dba\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$handler`</span> \], <span class="methodparam"><span
class="type">string</span> `$args`</span> )

<span class="function">dba\_open</span> establishes a database instance
for `path` with `mode` using `handler`.

### 参数

`path`  
Commonly a regular path in your filesystem.

`mode`  
It is *r* for read access, *w* for read/write access to an already
existing database, *c* for read/write access and database creation if it
doesn't currently exist, and *n* for create, truncate and read/write
access. The database is created in BTree mode, other modes (like Hash or
Queue) are not supported.

Additionally you can set the database lock method with the next char.
Use *l* to lock the database with a `.lck` file or *d* to lock the
databasefile itself. It is important that all of your applications do
this consistently.

If you want to test the access and do not want to wait for the lock you
can add *t* as third character. When you are absolutely sure that you do
not require database locking you can do so by using *-* instead of *l*
or *d*. When none of *d*, *l* or *-* is used, dba will lock on the
database file as it would with *d*.

> **Note**:
>
> There can only be one writer for one database file. When you use dba
> on a web server and more than one request requires write operations
> they can only be done one after another. Also read during write is not
> allowed. The dba extension uses locks to prevent this. See the
> following table:
>
> | already open  | `mode` = "rl" | `mode` = "rlt" | `mode` = "wl" | `mode` = "wlt" | `mode` = "rd" | `mode` = "rdt" | `mode` = "wd" | `mode` = "wdt" |
> |---------------|---------------|----------------|---------------|----------------|---------------|----------------|---------------|----------------|
> | not open      | ok            | ok             | ok            | ok             | ok            | ok             | ok            | ok             |
> | `mode` = "rl" | ok            | ok             | wait          | false          | illegal       | illegal        | illegal       | illegal        |
> | `mode` = "wl" | wait          | false          | wait          | false          | illegal       | illegal        | illegal       | illegal        |
> | `mode` = "rd" | illegal       | illegal        | illegal       | illegal        | ok            | ok             | wait          | false          |
> | `mode` = "wd" | illegal       | illegal        | illegal       | illegal        | wait          | false          | wait          | false          |
>
> -   ok: the second call will be successfull.
> -   wait: the second call waits until <span
>     class="function">dba\_close</span> is called for the first.
> -   false: the second call returns false.
> -   illegal: you must not mix *"l"* and *"d"* modifiers for `mode`
>     parameter.

`handler`  
The name of the <a href="/book/dba.html#需求" class="link">handler</a>
which shall be used for accessing `path`. It is passed all optional
parameters given to <span class="function">dba\_open</span> and can act
on behalf of them.

`args`  
Optional <span class="type">string</span> parameters which are passed to
the driver.

The *cdb*, *cdb\_make*, *flatfile*, *inifile*, *qdbm* and *tcadb*
drivers do not support additional parameters.

The *db1*, *db2*, *db3*, *db4*, *dbm*, *gdbm*, and *ndbm* drivers
supports a single additional parameter *$filemode*, which has the same
meaning as the *$mode* parameter of <span class="function">chmod</span>,
and defaults to *0644*.

The *lmdb* driver accepts two additional parameters. The first allows to
specify the *$filemode* (see description above), and the second to
specify the *$mapsize*, where the value should be a multiple of the page
size of the OS, or zero, to use the default mapsize. The *$mapsize*
parameter is supported as of PHP 7.3.14 and 7.4.2, respectively.

### 返回值

Returns a positive handle on success 或者在失败时返回 **`FALSE`**.

### 更新日志

| 版本          | 说明                                                               |
|---------------|--------------------------------------------------------------------|
| 7.3.14, 7.4.2 | The *lmdb* driver now supports an additional *$mapsize* parameter. |

### 参见

-   <span class="function">dba\_popen</span>
-   <span class="function">dba\_close</span>

dba\_optimize
=============

Optimize database

### 说明

<span class="type">bool</span> <span
class="methodname">dba\_optimize</span> ( <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
)

<span class="function">dba\_optimize</span> optimizes the underlying
database.

### 参数

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">dba\_sync</span>

dba\_popen
==========

Open database persistently

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">dba\_popen</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$handler`</span> \], <span class="methodparam"><span
class="type">mixed</span> `$args`</span> )

<span class="function">dba\_popen</span> establishes a persistent
database instance for `path` with `mode` using `handler`.

### 参数

`path`  
Commonly a regular path in your filesystem.

`mode`  
It is *r* for read access, *w* for read/write access to an already
existing database, *c* for read/write access and database creation if it
doesn't currently exist, and *n* for create, truncate and read/write
access.

`handler`  
The name of the <a href="/book/dba.html#需求" class="link">handler</a>
which shall be used for accessing `path`. It is passed all optional
parameters given to <span class="function">dba\_popen</span> and can act
on behalf of them.

`args`  
Optional <span class="type">string</span> parameters which are passed to
the driver.

The *cdb*, *cdb\_make*, *flatfile*, *inifile*, *qdbm* and *tcadb*
drivers do not support additional parameters.

The *db1*, *db2*, *db3*, *db4*, *dbm*, *gdbm*, and *ndbm* drivers
supports a single additional parameter *$filemode*, which has the same
meaning as the *$mode* parameter of <span class="function">chmod</span>,
and defaults to *0644*.

The *lmdb* driver accepts two additional parameters. The first allows to
specify the *$filemode* (see description above), and the second to
specify the *$mapsize*, where the value should be a multiple of the page
size of the OS, or zero, to use the default mapsize. The *$mapsize*
parameter is supported as of PHP 7.3.14 and 7.4.2, respectively.

### 返回值

Returns a positive handle on success 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">dba\_open</span>
-   <span class="function">dba\_close</span>

dba\_replace
============

Replace or insert entry

### 说明

<span class="type">bool</span> <span
class="methodname">dba\_replace</span> ( <span class="methodparam"><span
class="type">string</span> `$key`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

<span class="function">dba\_replace</span> replaces or inserts the entry
described with `key` and `value` into the database specified by
`handle`.

### 参数

`key`  
The key of the entry to be replaced.

`value`  
The value to be replaced.

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">dba\_exists</span>
-   <span class="function">dba\_delete</span>
-   <span class="function">dba\_fetch</span>
-   <span class="function">dba\_insert</span>

dba\_sync
=========

Synchronize database

### 说明

<span class="type">bool</span> <span class="methodname">dba\_sync</span>
( <span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

<span class="function">dba\_sync</span> synchronizes the database. This
will probably trigger a physical write to the disk, if supported.

### 参数

`handle`  
The database handler, returned by <span
class="function">dba\_open</span> or <span
class="function">dba\_popen</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">dba\_optimize</span>

**目录**

-   [dba\_close](/book/dba.html#dba_close) — Close a DBA database
-   [dba\_delete](/book/dba.html#dba_delete) — Delete DBA entry
    specified by key
-   [dba\_exists](/book/dba.html#dba_exists) — Check whether key exists
-   [dba\_fetch](/book/dba.html#dba_fetch) — Fetch data specified by key
-   [dba\_firstkey](/book/dba.html#dba_firstkey) — Fetch first key
-   [dba\_handlers](/book/dba.html#dba_handlers) — List all the handlers
    available
-   [dba\_insert](/book/dba.html#dba_insert) — Insert entry
-   [dba\_key\_split](/book/dba.html#dba_key_split) — Splits a key in
    string representation into array representation
-   [dba\_list](/book/dba.html#dba_list) — List all open database files
-   [dba\_nextkey](/book/dba.html#dba_nextkey) — Fetch next key
-   [dba\_open](/book/dba.html#dba_open) — Open database
-   [dba\_optimize](/book/dba.html#dba_optimize) — Optimize database
-   [dba\_popen](/book/dba.html#dba_popen) — Open database persistently
-   [dba\_replace](/book/dba.html#dba_replace) — Replace or insert entry
-   [dba\_sync](/book/dba.html#dba_sync) — Synchronize database
