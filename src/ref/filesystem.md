相关函数参见<a href="/ref/dir.html" class="link">目录</a>和<a href="/ref/exec.html" class="link">程序执行</a>章节。

远程文件能使用的 URL 包装器（ wrapper）列表和详细解释，可参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>。

basename
========

返回路径中的文件名部分

### 说明

<span class="type">string</span> <span
class="methodname">basename</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">string</span> `$suffix`</span> \]
)

给出一个包含有指向一个文件的全路径的字符串，本函数返回基本的文件名。

> **Note**:
>
> <span class="function">basename</span> 纯粹基于输入字符串操作，
> 它不会受实际文件系统和类似 "*..*" 的路径格式影响。

**Caution**

<span class="function">basename</span> 是本地化的，
所以如果要正确处理多字节字符的路径， 需要用 <span
class="function">setlocale</span> 正确设置匹配的 locale。

### 参数

`path`  
一个路径。

在 Windows
中，斜线（*/*）和反斜线（*\\*）都可以用作目录分隔符。在其它环境下是斜线（*/*）。

`suffix`  
如果文件名是以 `suffix` 结束的，那这一部分也会被去掉。

### 返回值

Returns the base name of the given `path`. 返回 `path` 的基本的文件名。

### 范例

**示例 \#1 <span class="function">basename</span> 例子**

``` php
<?php
echo "1) ".basename("/etc/sudoers.d", ".d").PHP_EOL;
echo "2) ".basename("/etc/sudoers.d").PHP_EOL;
echo "3) ".basename("/etc/passwd").PHP_EOL;
echo "4) ".basename("/etc/").PHP_EOL;
echo "5) ".basename(".").PHP_EOL;
echo "6) ".basename("/");
?>
```

以上例程会输出：

    1) sudoers
    2) sudoers.d
    3) passwd
    4) etc
    5) .
    6) 

### 参见

-   <span class="function">dirname</span>
-   <span class="function">pathinfo</span>

chgrp
=====

改变文件所属的组

### 说明

<span class="type">bool</span> <span class="methodname">chgrp</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">mixed</span> `$group`</span> )

尝试将文件 `filename` 所属的组改成 `group`（通过组名或组 ID 指定）。

只有超级用户可以任意修改文件的组，其它用户可能只能将文件的组改成该用户自己所在的组。

### 参数

`filename`  
文件的路径。

`group`  
组的名称或数字。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 改变文件所属的组**

``` php
<?php
$filename = 'shared_file.txt';
$format = "%s's Group ID @ %s: %d\n";
printf($format, $filename, date('r'), filegroup($filename));
chgrp($filename, 8);
clearstatcache(); // do not cache filegroup() results
printf($format, $filename, date('r'), filegroup($filename));
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

> **Note**: <span class="simpara"> On Windows, this function fails
> silently when applied on a regular file. </span>

### 参见

-   <span class="function">chown</span>
-   <span class="function">chmod</span>

chmod
=====

改变文件模式

### 说明

<span class="type">bool</span> <span class="methodname">chmod</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> )

尝试将 `filename` 所指定文件的模式改成 `mode` 所给定的。

### 参数

`filename`  
文件的路径。

`mode`  
注意 `mode` 不会被自动当成八进制数值，而且也不能用字符串（例如
"g+w"）。要确保正确操作，需要给 `mode` 前面加上 0：

``` php
<?php
chmod("/somedir/somefile", 755);   // 十进制数，可能不对
chmod("/somedir/somefile", "u+rwx,go+rx"); // 字符串，不对
chmod("/somedir/somefile", 0755);  // 八进制数，正确的 mode 值
?>
```

`mode`
参数包含三个八进制数按顺序分别指定了所有者、所有者所在的组以及所有人的访问限制。每一部分都可以通过加入所需的权限来计算出所要的权限。数字
1 表示使文件可执行，数字 2 表示使文件可写，数字 4
表示使文件可读。加入这些数字来制定所需要的权限。有关 UNIX
系统的文件权限可以阅读手册“**man 1 chmod**”和“**man 2 chmod**”。

``` php
<?php
// Read and write for owner, nothing for everybody else
chmod("/somedir/somefile", 0600);

// Read and write for owner, read for everybody else
chmod("/somedir/somefile", 0644);

// Everything for owner, read and execute for others
chmod("/somedir/somefile", 0755);

// Everything for owner, read and execute for owner's group
chmod("/somedir/somefile", 0750);
?>
```

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**:
>
> 当前用户指的是执行 PHP 的用户。很可能和通常的 shell 或者 FTP
> 用户不是同一个。在大多数系统下文件模式只能被文件所有者的用户改变。

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

### 参见

-   <span class="function">chown</span>
-   <span class="function">chgrp</span>
-   <span class="function">fileperms</span>
-   <span class="function">stat</span>

chown
=====

改变文件的所有者

### 说明

<span class="type">bool</span> <span class="methodname">chown</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">mixed</span> `$user`</span> )

尝试将文件 `filename` 的所有者改成用户 `user`（由用户名或用户 ID
指定）。 只有超级用户可以改变文件的所有者。

### 参数

`filename`  
文件路径。

`user`  
用户名或数字。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 简单的 <span class="function">chown</span> 用法**

``` php
<?php

// File name and username to use
$file_name= "foo.php";
$path = "/home/sites/php.net/public_html/sandbox/" . $file_name ;
$user_name = "root";

// Set the user
chown($path, $user_name);

// Check the result
$stat = stat($path);
print_r(posix_getpwuid($stat['uid']));

?>
```

以上例程的输出类似于：

    Array
    (
        [name] => root
        [passwd] => x
        [uid] => 0
        [gid] => 0
        [gecos] => root
        [dir] => /root
        [shell] => /bin/bash
    )

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

> **Note**: <span class="simpara"> 在 Windows
> 上对普通文件使用此函数会静默失败。 </span>

### 参见

-   <span class="function">chmod</span>
-   <span class="function">chgrp</span>

clearstatcache
==============

清除文件状态缓存

### 说明

<span class="type">void</span> <span
class="methodname">clearstatcache</span> (\[ <span
class="methodparam"><span class="type">bool</span>
`$clear_realpath_cache`<span class="initializer"> = false</span></span>
\[, <span class="methodparam"><span class="type">string</span>
`$filename`</span> \]\] )

当使用 <span class="function">stat</span>，<span
class="function">lstat</span>
或者任何列在受影响函数表（见下面）中的函数时，PHP
将缓存这些函数的返回信息以提供更快的性能。然而在某些情况下，你可能想清除被缓存的信息。例如如果在一个脚本中多次检查同一个文件，而该文件在此脚本执行期间有被删除或修改的危险时，你需要清除文件状态缓存。这种情况下，可以用
<span class="function">clearstatcache</span> 函数来清除被 PHP
缓存的该文件信息。

必须注意的是，对于不存在的文件，PHP 并不会缓存其信息。所以如果调用 <span
class="function">file\_exists</span>
来检查不存在的文件，在该文件没有被创建之前，它都会返回
**`FALSE`**。如果该文件被创建了，就算以后被删除，它都会返回 **`TRUE`**
函数 <span class="function">unlink</span> 会自动清除该缓存.

> **Note**:
>
> 本函数缓存特定文件名的信息，因此只在对同一个文件名进行多次操作并且需要该文件信息不被缓存时才需要调用
> <span class="function">clearstatcache</span>。

受影响的函数包括 <span class="function">stat</span>， <span
class="function">lstat</span>， <span
class="function">file\_exists</span>， <span
class="function">is\_writable</span>， <span
class="function">is\_readable</span>， <span
class="function">is\_executable</span>， <span
class="function">is\_file</span>， <span
class="function">is\_dir</span>， <span
class="function">is\_link</span>， <span
class="function">filectime</span>， <span
class="function">fileatime</span>， <span
class="function">filemtime</span>， <span
class="function">fileinode</span>， <span
class="function">filegroup</span>， <span
class="function">fileowner</span>， <span
class="function">filesize</span>， <span
class="function">filetype</span> 和 <span
class="function">fileperms</span>。

### 参数

`clear_realpath_cache`  
是否清除真实路径缓存

`filename`  
清除文件名指定的文件的真实路径缓存; 只在 `clear_realpath_cache` 为
**`TRUE`** 时启用

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                                                    |
|-------|---------------------------------------------------------|
| 5.3.0 | 增加了可选的 `clear_realpath_cache` 和 `filename` 参数. |

### 范例

**示例 \#1 <span class="function">clearstatcache</span> 例子**

``` php
<?php
$file = 'output_log.txt';

function get_owner($file)
{
    $stat = stat($file);
    $user = posix_getpwuid($stat['uid']);
    return $user['name'];
}

$format = "UID @ %s: %s\n";

printf($format, date('r'), get_owner($file));

chown($file, 'ross');
printf($format, date('r'), get_owner($file));

clearstatcache();
printf($format, date('r'), get_owner($file));
?>
```

以上例程的输出类似于：

    UID @ Sun, 12 Oct 2008 20:48:28 +0100: root
    UID @ Sun, 12 Oct 2008 20:48:28 +0100: root
    UID @ Sun, 12 Oct 2008 20:48:28 +0100: ross

copy
====

拷贝文件

### 说明

<span class="type">bool</span> <span class="methodname">copy</span> (
<span class="methodparam"><span class="type">string</span>
`$source`</span> , <span class="methodparam"><span
class="type">string</span> `$dest`</span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\] )

将文件从 `source` 拷贝到 `dest`。

如果要移动文件的话，请使用 <span class="function">rename</span> 函数。

### 参数

`source`  
源文件路径。

`dest`  
目标路径。如果 `dest` 是一个
URL，则如果封装协议不支持覆盖已有的文件时拷贝操作会失败。

**Warning**
如果目标文件已存在，将会被覆盖。

`context`  
A valid context resource created with <span
class="function">stream\_context\_create</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">copy</span> 例子**

``` php
<?php
$file = 'example.txt';
$newfile = 'example.txt.bak';

if (!copy($file, $newfile)) {
    echo "failed to copy $file...\n";
}
?>
```

### 参见

-   <span class="function">move\_uploaded\_file</span>
-   <span class="function">rename</span>
-   The section of the manual about
    <a href="/features/file-upload.html" class="link">handling file uploads</a>

delete
======

参见 <span class="function">unlink</span> 或 <span
class="function">unset</span>

### 说明

在 PHP 语言里，没有 delete
关键词或函数。在这里，你若要删除文件，可以使用 <span
class="function">unlink</span>。在本地作用域删除变量可使用 <span
class="function">unset</span>。

### 参见

-   <span class="function">unlink</span>
-   <span class="function">unset</span>

dirname
=======

返回路径中的目录部分

### 说明

<span class="type">string</span> <span class="methodname">dirname</span>
( <span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">int</span> `$levels`<span class="initializer"> =
1</span></span> \] )

给出一个包含有指向一个文件的全路径的字符串，本函数返回去掉文件名后的目录名，且目录深度为
`levels` 级。

> **Note**:
>
> <span class="function">dirname</span> 纯粹基于输入字符串操作，
> 它不会受实际文件系统和类似 "*..*" 的路径格式影响。

**Caution**

<span class="function">dirname</span>
是本地化的，所以如果要正确处理多字节字符的路径，需要用 <span
class="function">setlocale</span> 正确设置匹配的 locale。

### 参数

`path`  
一个路径。

在 Windows
中，斜线（*/*）和反斜线（*\\*）都可以用作目录分隔符。在其它环境下是斜线（*/*）。

`levels`  
要向上的父目录数量。

整型，必须大于 0。

### 返回值

返回 path 的父目录。 如果在 `path`
中没有斜线，则返回一个点（'*.*'），表示当前目录。否则返回的是把 `path`
中结尾的 */component*（最后一个斜线以及后面部分）去掉之后的字符串。

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 7.0.0 | 添加可选的 `levels` 参数。 |

### 范例

**示例 \#1 <span class="function">dirname</span> 例子**

``` php
<?php
echo dirname("/etc/passwd") . PHP_EOL;
echo dirname("/etc/") . PHP_EOL;
echo dirname(".") . PHP_EOL;
echo dirname("C:\\") . PHP_EOL;
echo dirname("/usr/local/lib", 2);
```

以上例程的输出类似于：

    /etc
    / (or \ on Windows)
    .
    C:\
    /usr

### 参见

-   <span class="function">basename</span>
-   <span class="function">pathinfo</span>
-   <span class="function">realpath</span>

disk\_free\_space
=================

返回目录中的可用空间

### 说明

<span class="type">float</span> <span
class="methodname">disk\_free\_space</span> ( <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

给出一个包含有一个目录的字符串，本函数将根据相应的文件系统或磁盘分区返回可用的字节数。

### 参数

`directory`  
文件系统目录或者磁盘分区。

> **Note**:
>
> 如果指定了文件名而不是文件目录，这个函数的行为将并不统一，会因操作系统和
> PHP 版本而异。

### 返回值

以浮点返回可用的字节数， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">disk\_free\_space</span> 例子**

``` php
<?php
// $df 包含根目录下可用的字节数
$df = disk_free_space("/");

//在 Windows 下:
$df_c = disk_free_space("C:");
$df_d = disk_free_space("D:");
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

### 参见

-   <span class="function">disk\_total\_space</span>

disk\_total\_space
==================

返回一个目录的磁盘总大小

### 说明

<span class="type">float</span> <span
class="methodname">disk\_total\_space</span> ( <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

给出一个包含有一个目录的字符串，本函数将根据相应的文件系统或磁盘分区返回所有的字节数。
【译者注】本函数返回的是该目录所在的磁盘分区的总大小，因此在给出同一个磁盘分区的不同目录作为参数所得到的结果完全相同。
在 Unix 和 Windows 200x/XP
中都支持将一个磁盘分区加载为一个子目录，这时正确使用本函数就很有意义。

### 参数

`directory`  
文件系统的目录或者磁盘分区。

### 返回值

以浮点返回一个目录的磁盘总大小字节数， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">disk\_total\_space</span> 例子**

``` php
<?php
// $df 包含 "/" 目录的磁盘大小
$ds = disk_total_space("/");

//在 Windows 下:
$ds = disk_total_space("C:");
$ds = disk_total_space("D:");
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

### 参见

-   <span class="function">disk\_free\_space</span>

diskfreespace
=============

<span class="function">disk\_free\_space</span> 的别名

### 说明

此函数是该函数的别名：<span class="function">disk\_free\_space</span>。

fclose
======

关闭一个已打开的文件指针

### 说明

<span class="type">bool</span> <span class="methodname">fclose</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

将 `handle` 指向的文件关闭。

### 参数

`handle`  
文件指针必须有效，并且是通过 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 一个简单 <span class="function">fclose</span> 例子**

``` php
<?php

$handle = fopen('somefile.txt', 'r');

fclose($handle);

?>
```

### 参见

-   <span class="function">fopen</span>
-   <span class="function">fsockopen</span>

feof
====

测试文件指针是否到了文件结束的位置

### 说明

<span class="type">bool</span> <span class="methodname">feof</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

测试文件指针是否到了文件结束的位。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

### 返回值

如果文件指针到了 EOF 或者出错时则返回 **`TRUE`**，否则返回一个错误（包括
socket 超时），其它情况则返回 **`FALSE`**。

### 注释

**Warning**

如果服务器没有关闭由 <span class="function">fsockopen</span>
所打开的连接，<span class="function">feof</span>
会一直等待直到超时。要解决这个问题可参见以下范例：

**示例 \#1 处理 <span class="function">feof</span> 的超时**

``` php
<?php
function safe_feof($fp, &$start = NULL) {
 $start = microtime(true);

 return feof($fp);
}

/* $fp 的赋值是由之前 fsockopen() 打开  */

$start = NULL;
$timeout = ini_get('default_socket_timeout');

while(!safe_feof($fp, $start) && (microtime(true) - $start) < $timeout)
{
 /* Handle */
}
?>
```

**Warning**

如果传递的文件指针无效可能会陷入无限循环中，因为 <span
class="function">feof</span> 不会返回 **`TRUE`**。

**示例 \#2 使用无效文件指针的 <span class="function">feof</span> 例子**

``` php
<?php
// 如果文件不可读取或者不存在，fopen 函数返回 FALSE
$file = @fopen("no_such_file", "r");

// 来自 fopen 的 FALSE 会发出一条警告信息并在这里陷入无限循环
while (!feof($file)) {
}

fclose($file);
?>
```

fflush
======

将缓冲内容输出到文件

### 说明

<span class="type">bool</span> <span class="methodname">fflush</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

本函数强制将所有缓冲的输出写入 `handle` 文件句柄所指向的资源。
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 File write example using <span
class="function">fflush</span>**

``` php
<?php
$filename = 'bar.txt';

$file = fopen($filename, 'r+');
rewind($file);
fwrite($file, 'Foo');
fflush($file);
ftruncate($file, ftell($file));
fclose($file);
?>
```

### 参见

-   <span class="function">clearstatcache</span>
-   <span class="function">fwrite</span>

fgetc
=====

从文件指针中读取字符

### 说明

<span class="type">string</span> <span class="methodname">fgetc</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

从文件句柄中获取一个字符。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

### 返回值

返回一个包含有一个字符的字符串，该字符从 `handle` 指向的文件中得到。
碰到 EOF 则返回 **`FALSE`**。

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 一个 <span class="function">fgetc</span> 例子**

``` php
<?php
$fp = fopen('somefile.txt', 'r');
if (!$fp) {
    echo 'Could not open file somefile.txt';
}
while (false !== ($char = fgetc($fp))) {
    echo "$char\n";
}
?>
```

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

### 参见

-   <span class="function">fread</span>
-   <span class="function">fopen</span>
-   <span class="function">popen</span>
-   <span class="function">fsockopen</span>
-   <span class="function">fgets</span>

fgetcsv
=======

从文件指针中读入一行并解析 CSV 字段

### 说明

<span class="type">array</span> <span class="methodname">fgetcsv</span>
( <span class="methodparam"><span class="type">resource</span>
`$handle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$delimiter`<span class="initializer"> =
','</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$enclosure`<span class="initializer"> =
'"'</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$escape`<span class="initializer"> =
'\\\\'</span></span> \]\]\]\] )

和 <span class="function">fgets</span> 类似，只除了 <span
class="function">fgetcsv</span> 解析读入的行并找出 CSV
格式的字段然后返回一个包含这些字段的数组。

### 参数

`handle`  
一个由 <span class="function">fopen</span>、<span
class="function">popen</span> 或 <span class="function">fsockopen</span>
产生的有效文件指针。

`length`  
必须大于 CVS 文件内最长的一行。在 PHP 5 中该参数是可选的。如果忽略（在
PHP 5.0.4 以后的版本中设为
0）该参数的话，那么长度就没有限制，不过可能会影响执行效率。

`delimiter`  
设置字段分界符（只允许一个字符）。

`enclosure`  
设置字段环绕符（只允许一个字符）。

`escape`  
设置转义字符（只允许一个字符），默认是一个反斜杠。

### 返回值

返回包含读取字段的索引数组。

> **Note**:
>
> CSV 文件中的空行将被返回为一个包含有单个 <span
> class="type">null</span> 字段的数组，不会被当成错误。

> **Note**: <span class="simpara">在读取在 Macintosh
> 电脑中或由其创建的文件时， 如果 PHP
> 不能正确的识别行结束符，启用运行时配置可选项
> <a href="/filesystem/setup.html#" class="link">auto_detect_line_endings</a>
> 也许可以解决此问题。</span>

如果提供了无效的文件指针，<span class="function">fgetcsv</span> 会返回
**`NULL`**。 其他错误，包括碰到文件结束时返回 **`FALSE`**，。

### 更新日志

| 版本  | 说明                                                                |
|-------|---------------------------------------------------------------------|
| 5.3.0 | 增加了 `escape` 参数。                                              |
| 4.3.5 | 现在起 <span class="function">fgetcsv</span> 的操作是二进制安全的。 |
| 4.3.0 | 增加了 `enclosure` 参数。                                           |

### 范例

**示例 \#1 读取并显示 CSV 文件的整个内容**

``` php
<?php
$row = 1;
if (($handle = fopen("test.csv", "r")) !== FALSE) {
    while (($data = fgetcsv($handle, 1000, ",")) !== FALSE) {
        $num = count($data);
        echo "<p> $num fields in line $row: <br /></p>\n";
        $row++;
        for ($c=0; $c < $num; $c++) {
            echo $data[$c] . "<br />\n";
        }
    }
    fclose($handle);
}
?>
```

### 注释

> **Note**:
>
> 该函数对区域设置是敏感的。比如说 `LANG` 设为 *en\_US.UTF-8*
> 的话，单字节编码的文件就会出现读取错误。

### 参见

-   <span class="function">str\_getcsv</span>
-   <span class="function">explode</span>
-   <span class="function">file</span>
-   <span class="function">pack</span>
-   <span class="function">fputcsv</span>

fgets
=====

从文件指针中读取一行

### 说明

<span class="type">string</span> <span class="methodname">fgets</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`</span> \] )

从文件指针中读取一行。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

`length`  
从 `handle` 指向的文件中读取一行并返回长度最多为 `length` - 1
字节的字符串。碰到换行符（包括在返回值中）、EOF 或者已经读取了 length -
1 字节后停止（看先碰到那一种情况）。如果没有指定 `length`，则默认为
1K，或者说 1024 字节。

### 返回值

从指针 `handle` 指向的文件中读取了 `length` - 1 字节后返回字符串。
如果文件指针中没有更多的数据了则返回 **`FALSE`**。

错误发生时返回 **`FALSE`**。

### 范例

**示例 \#1 逐行读取文件**

``` php
<?php
$handle = @fopen("/tmp/inputfile.txt", "r");
if ($handle) {
    while (($buffer = fgets($handle, 4096)) !== false) {
        echo $buffer;
    }
    if (!feof($handle)) {
        echo "Error: unexpected fgets() fail\n";
    }
    fclose($handle);
}
?>
```

### 注释

> **Note**: <span class="simpara">在读取在 Macintosh
> 电脑中或由其创建的文件时， 如果 PHP
> 不能正确的识别行结束符，启用运行时配置可选项
> <a href="/filesystem/setup.html#" class="link">auto_detect_line_endings</a>
> 也许可以解决此问题。</span>

> **Note**:
>
> 习惯了 C 语言中 <span class="function">fgets</span> 语法的人应该注意到
> *EOF* 是怎样被返回的。

### 参见

-   <span class="function">fgetss</span>
-   <span class="function">fread</span>
-   <span class="function">fgetc</span>
-   <span class="function">stream\_get\_line</span>
-   <span class="function">fopen</span>
-   <span class="function">popen</span>
-   <span class="function">fsockopen</span>
-   <span class="function">stream\_set\_timeout</span>

fgetss
======

从文件指针中读取一行并过滤掉 HTML 标记

### 说明

<span class="type">string</span> <span class="methodname">fgetss</span>
( <span class="methodparam"><span class="type">resource</span>
`$handle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$length`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$allowable_tags`</span> \]\] )

和 <span class="function">fgets</span> 相同，只除了 <span
class="function">fgetss</span> 尝试从读取的文本中去掉任何 HTML 和 PHP
标记。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

`length`  
取回该长度的数据。

`allowable_tags`  
可以用可选的第三个参数指定哪些标记不被去掉。

### 返回值

从 `handle` 指向的文件中大读取 `length` - 1 个字节的字符，并过滤了所有的
HTML 和 PHP 代码。

错误发生时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                          |
|-------|-------------------------------|
| 5.0.0 | 参数 `length` 从 此开始可选。 |

**示例 \#1 一行行读取一个 PHP 文件**

``` php
<?php
$str = <<<EOD
<html><body>
 <p>Welcome! Today is the <?php echo(date('jS')); ?> of <?= date('F'); ?>.</p>
</body></html>
Text outside of the HTML block.
EOD;
file_put_contents('sample.php', $str);

$handle = @fopen("sample.php", "r");
if ($handle) {
    while (!feof($handle)) {
        $buffer = fgetss($handle, 4096);
        echo $buffer;
    }
    fclose($handle);
}
?>
```

以上例程的输出类似于：

     Welcome! Today is the  of .

    Text outside of the HTML block.

### 注释

> **Note**: <span class="simpara">在读取在 Macintosh
> 电脑中或由其创建的文件时， 如果 PHP
> 不能正确的识别行结束符，启用运行时配置可选项
> <a href="/filesystem/setup.html#" class="link">auto_detect_line_endings</a>
> 也许可以解决此问题。</span>

### 参见

-   <span class="function">fgets</span>
-   <span class="function">fopen</span>
-   <span class="function">popen</span>
-   <span class="function">fsockopen</span>
-   <span class="function">strip\_tags</span>

file\_exists
============

检查文件或目录是否存在

### 说明

<span class="type">bool</span> <span
class="methodname">file\_exists</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

检查文件或目录是否存在。

### 参数

`filename`  
文件或目录的路径。

在 Windows 中要用 `//computername/share/filename` 或者
`\\computername\share\filename` 来检查网络中的共享文件。

### 返回值

如果由 `filename` 指定的文件或目录存在则返回 **`TRUE`**，否则返回
**`FALSE`**。

> **Note**:
>
> This function will return **`FALSE`** for symlinks pointing to
> non-existing files.

> **Note**:
>
> The check is done using the real UID/GID instead of the effective one.

> **Note**: <span class="simpara"> 因为 PHP
> 的整数类型是有符号整型而且很多平台使用 32 位整型，对 2GB
> 以上的文件，一些文件系统函数可能返回无法预期的结果。</span>

### 范例

**示例 \#1 测试一个文件是否存在**

``` php
<?php
$filename = '/path/to/foo.txt';

if (file_exists($filename)) {
    echo "The file $filename exists";
} else {
    echo "The file $filename does not exist";
}
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">is\_readable</span>
-   <span class="function">is\_writable</span>
-   <span class="function">is\_file</span>
-   <span class="function">file</span>

file\_get\_contents
===================

将整个文件读入一个字符串

### 说明

<span class="type">string</span> <span
class="methodname">file\_get\_contents</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">resource</span>
`$context`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
-1</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$maxlen`</span> \]\]\]\] )

和 <span class="function">file</span> 一样，只除了 <span
class="function">file\_get\_contents</span>
把文件读入一个字符串。将在参数 `offset` 所指定的位置开始读取长度为
`maxlen` 的内容。如果失败，<span
class="function">file\_get\_contents</span> 将返回 **`FALSE`**。

<span class="function">file\_get\_contents</span>
函数是用来将文件的内容读入到一个字符串中的首选方法。如果操作系统支持还会使用内存映射技术来增强性能。

> **Note**:
>
> 如果要打开有特殊字符的 URL （比如说有空格），就需要使用 <span
> class="function">urlencode</span> 进行 URL 编码。

### 参数

`filename`  
要读取的文件的名称。

`use_include_path`  
> **Note**:
>
> As of PHP 5 the **`FILE_USE_INCLUDE_PATH`** can be used to trigger
> <a href="/ini/core.html#ini.include-path" class="link">include path</a>
> search.

`context`  
A valid context resource created with <span
class="function">stream\_context\_create</span>. 如果你不需要自定义
context，可以用 **`NULL`** 来忽略。

`offset`  
The offset where the reading starts on the original stream.

Seeking (`offset`) is not supported with remote files. Attempting to
seek on non-local files may work with small offsets, but this is
unpredictable because it works on the buffered stream.

`maxlen`  
Maximum length of data read. The default is to read until end of file is
reached. Note that this parameter is applied to the stream processed by
the filters.

### 返回值

The function returns the read data 或者在失败时返回 **`FALSE`**.

### 错误／异常

An **`E_WARNING`** level error is generated if either `maxlength` is
less than zero, or if seeking to the specified `offset` in the stream
fails.

### 范例

**示例 \#1 Get and output the source of the homepage of a website**

``` php
<?php
$homepage = file_get_contents('http://www.example.com/');
echo $homepage;
?>
```

**示例 \#2 Searching within the include\_path**

``` php
<?php
// <= PHP 5
$file = file_get_contents('./people.txt', true);
// > PHP 5
$file = file_get_contents('./people.txt', FILE_USE_INCLUDE_PATH);
?>
```

**示例 \#3 Reading a section of a file**

``` php
<?php
// Read 14 characters starting from the 21st character
$section = file_get_contents('./people.txt', NULL, NULL, 20, 14);
var_dump($section);
?>
```

以上例程的输出类似于：

    string(14) "lle Bjori Ro" 

**示例 \#4 Using stream contexts**

``` php
<?php
// Create a stream
$opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar\r\n"
  )
);

$context = stream_context_create($opts);

// Open the file using the HTTP headers set above
$file = file_get_contents('http://www.example.com/', false, $context);
?>
```

### 更新日志

| 版本  | 说明                                        |
|-------|---------------------------------------------|
| 5.1.0 | Added the `offset` and `maxlen` parameters. |
| 5.0.0 | Added context support.                      |

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

**Warning**

使用 SSL 时，Microsoft IIS
会违反协议不发送*close\_notify*标记就关闭连接。PHP
会在到达数据尾端时报告“SSL: Fatal Protocol Error”。
要解决此问题，<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
应设定为降低级别至不包含警告。 PHP 4.3.7 及更高版本可以在使用 *https://*
包装器打开流时检测出有问题的 IIS 服务器软件 并抑制警告。在使用 <span
class="function">fsockopen</span> 创建 *ssl://* 套接字时,
开发者需检测并抑制此警告。

### 参见

-   <span class="function">file</span>
-   <span class="function">fgets</span>
-   <span class="function">fread</span>
-   <span class="function">readfile</span>
-   <span class="function">file\_put\_contents</span>
-   <span class="function">stream\_get\_contents</span>
-   <span class="function">stream\_context\_create</span>
-   <a href="/reserved/variables/httpresponseheader.html" class="link">$http_response_header</a>

file\_put\_contents
===================

将一个字符串写入文件

### 说明

<span class="type">int</span> <span
class="methodname">file\_put\_contents</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$data`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \]\] )

和依次调用 <span class="function">fopen</span>，<span
class="function">fwrite</span> 以及 <span class="function">fclose</span>
功能一样。

If `filename` does not exist, the file is created. Otherwise, the
existing file is overwritten, unless the **`FILE_APPEND`** flag is set.

### 参数

`filename`  
要被写入数据的文件名。

`data`  
要写入的数据。类型可以是 <span class="type">string</span>，<span
class="type">array</span> 或者是 <span class="type">stream</span>
资源（如上面所说的那样）。

如果 `data` 指定为 stream 资源，这里 stream
中所保存的缓存数据将被写入到指定文件中，这种用法就相似于使用 <span
class="function">stream\_copy\_to\_stream</span> 函数。

参数 `data` 可以是数组（但不能为多维数组），这就相当于
*file\_put\_contents($filename, join('', $array))*。

`flags`  
`flags` 的值可以是 以下 flag 使用 OR (*\|*) 运算符进行的组合。

| Flag                        | 描述                                                                                                                        |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **`FILE_USE_INCLUDE_PATH`** | 在 include 目录里搜索 `filename`。 更多信息可参见 <a href="/ini/core.html#ini.include-path" class="link">include_path</a>。 |
| **`FILE_APPEND`**           | 如果文件 `filename` 已经存在，追加数据而不是覆盖。                                                                          |
| **`LOCK_EX`**               | 在写入时获得一个独占锁。                                                                                                    |

`context`  
一个 context 资源。

### 返回值

该函数将返回写入到文件内数据的字节数，失败时返回**`FALSE`**

**Warning**

此函数可能返回布尔值 **`FALSE`**，但也可能返回等同于 **`FALSE`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 Simple usage example**

``` php
<?php
$file = 'people.txt';
// Open the file to get existing content
$current = file_get_contents($file);
// Append a new person to the file
$current .= "John Smith\n";
// Write the contents back to the file
file_put_contents($file, $current);
?>
```

**示例 \#2 Using flags**

``` php
<?php
$file = 'people.txt';
// The new person to add to the file
$person = "John Smith\n";
// Write the contents to the file, 
// using the FILE_APPEND flag to append the content to the end of the file
// and the LOCK_EX flag to prevent anyone else writing to the file at the same time
file_put_contents($file, $person, FILE_APPEND | LOCK_EX);
?>
```

### 更新日志

| 版本  | 说明                                                                |
|-------|---------------------------------------------------------------------|
| 5.0.0 | Added context support                                               |
| 5.1.0 | 添加了对 **`LOCK_EX`** 的支持和 `data` 参数处理 stream 资源的功能。 |

### 注释

> **Note**: <span class="simpara">此函数可安全用于二进制对象。</span>

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参见

-   <span class="function">fopen</span>
-   <span class="function">fwrite</span>
-   <span class="function">file\_get\_contents</span>
-   <span class="function">stream\_context\_create</span>

file
====

把整个文件读入一个数组中

### 说明

<span class="type">array</span> <span class="methodname">file</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \]\] )

把整个文件读入一个数组中。

> **Note**:
>
> 你可以通过 <span class="function">file\_get\_contents</span>
> 以字符串形式获取文件的内容。

### 参数

`filename`  
文件的路径。

**小贴士**
如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

`flags`  
可选参数 `flags` 可以是以下一个或多个常量：

**`FILE_USE_INCLUDE_PATH`**  
<span class="simpara"> 在
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
中查找文件。 </span>

**`FILE_IGNORE_NEW_LINES`**  
<span class="simpara"> 在数组每个元素的末尾不要添加换行符 </span>

**`FILE_SKIP_EMPTY_LINES`**  
<span class="simpara"> 跳过空行 </span>

`context`  
A context resource created with the <span
class="function">stream\_context\_create</span> function.

> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

Returns the file in an array. Each element of the array corresponds to a
line in the file, with the newline still attached. Upon failure, <span
class="function">file</span> returns **`FALSE`**.

> **Note**:
>
> Each line in the resulting array will include the line ending, unless
> **`FILE_IGNORE_NEW_LINES`** is used, so you still need to use <span
> class="function">rtrim</span> if you do not want the line ending
> present.

> **Note**: <span class="simpara">在读取在 Macintosh
> 电脑中或由其创建的文件时， 如果 PHP
> 不能正确的识别行结束符，启用运行时配置可选项
> <a href="/filesystem/setup.html#" class="link">auto_detect_line_endings</a>
> 也许可以解决此问题。</span>

### 更新日志

| 版本  | 说明                                                                                                                                                 |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.0.0 | 增加了参数 `context`                                                                                                                                 |
| 5.0.0 | Prior to PHP 5.0.0 the `flags` parameter only covered <a href="/ini/core.html#ini.include-path" class="link">include_path</a> and was enabled with 1 |
| 4.3.0 | <span class="function">file</span> 开始是二进制安全的                                                                                                |

### 范例

**示例 \#1 <span class="function">file</span> 例子**

``` php
<?php
// 将一个文件读入数组。本例中通过 HTTP 从 URL 中取得 HTML 源文件。

$lines = file('http://www.example.com/');

// 在数组中循环，显示 HTML 的源文件并加上行号。

foreach ($lines as $line_num => $line) {
    echo "Line #<b>{$line_num}</b> : " . htmlspecialchars($line) . "<br />\n";
}

// 另一个例子将 web 页面读入字符串。参见 file_get_contents()。

$html = implode('', file('http://www.example.com/'));

// 从 PHP 5 开始可以使用可选标记参数
$trimmed = file('somefile.txt', FILE_IGNORE_NEW_LINES | FILE_SKIP_EMPTY_LINES);
?>
```

### 注释

**Warning**

使用 SSL 时，Microsoft IIS
会违反协议不发送*close\_notify*标记就关闭连接。PHP
会在到达数据尾端时报告“SSL: Fatal Protocol Error”。
要解决此问题，<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
应设定为降低级别至不包含警告。 PHP 4.3.7 及更高版本可以在使用 *https://*
包装器打开流时检测出有问题的 IIS 服务器软件 并抑制警告。在使用 <span
class="function">fsockopen</span> 创建 *ssl://* 套接字时,
开发者需检测并抑制此警告。

### 参见

-   <span class="function">readfile</span>
-   <span class="function">fopen</span>
-   <span class="function">fsockopen</span>
-   <span class="function">popen</span>
-   <span class="function">file\_get\_contents</span>
-   <span class="function">include</span>
-   <span class="function">stream\_context\_create</span>

fileatime
=========

取得文件的上次访问时间

### 说明

<span class="type">int</span> <span class="methodname">fileatime</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得文件的上次访问时间。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件上次被访问的时间， 或者在失败时返回 **`FALSE`**。时间以 Unix
时间戳的方式返回。

### 范例

**示例 \#1 <span class="function">fileatime</span> 例子**

``` php
<?php

// 输出类似：somefile.txt was last accessed: December 29 2002 22:16:23.

$filename = 'somefile.txt';
if (file_exists($filename)) {
    echo "$filename was last accessed: " . date("F d Y H:i:s.", fileatime($filename));
}

?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**:
>
> 注意：一个文件的 atime
> 应该在不论何时读取了此文件中的数据块时被更改。当一个应用程序定期访问大量文件或目录时很影响性能。
>
> 有些 Unix 文件系统可以在加载时关闭 atime
> 的更新以提高这类程序的性能。USENET
> 新闻组假脱机是一个常见的例子。在这种文件系统下本函数没有用处。

> **Note**:
>
> 注意：不同文件系统对时间的判断方法可能是不相同的。

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">filemtime</span>
-   <span class="function">fileinode</span>
-   <span class="function">date</span>

filectime
=========

取得文件的 inode 修改时间

### 说明

<span class="type">int</span> <span class="methodname">filectime</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得文件的 inode 修改时间。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件上次 inode 被修改的时间， 或者在失败时返回 **`FALSE`**。 时间以
Unix 时间戳的方式返回。

### 范例

**示例 \#1 <span class="function">filectime</span> 例子**

``` php
<?php

// 输出类似：  somefile.txt was last changed: December 29 2002 22:16:23.

$filename = 'somefile.txt';
if (file_exists($filename)) {
    echo "$filename was last changed: " . date("F d Y H:i:s.", filectime($filename));
}

?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**:
>
> 注意：在大多数 Unix 文件系统中，当一个文件的 inode
> 数据被改变时则该文件被认为是修改了。也就是说，当文件的权限，所有者，所有组或其它
> inode 中的元数据被更新时。参见 <span
> class="function">filemtime</span>（这才是你想用于在 Web
> 页面中建立“最后更新时间”脚注的函数）和 <span
> class="function">fileatime</span>。

> **Note**:
>
> 注意某些 Unix 说明文本中把 ctime
> 说成是该文件建立的时间，这是错的。在大多数 Unix 文件系统中没有 Unix
> 文件的建立时间。

> **Note**:
>
> 注意：不同文件系统对时间的判断方法可能是不相同的。

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">filemtime</span>

filegroup
=========

取得文件的组

### 说明

<span class="type">int</span> <span class="methodname">filegroup</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得该文件所属组的 ID。组 ID 以数字格式返回，用 <span
class="function">posix\_getgrgid</span> 来将其解析为组名。

### 参数

`filename`  
文件的路径。

### 返回值

返回该文件所属组的 ID。或在错误时返回 **`FALSE`**。 组 ID
以数字格式返回，用 <span class="function">posix\_getgrgid</span>
来将其解析为组名。如果出错则返回 **`FALSE`**。

### 范例

**示例 \#1 查找文件所在的组**

``` php
<?php
$filename = 'index.php';
print_r(posix_getgrgid(filegroup($filename)));
?>
```

### 错误／异常

如果失败返回 **`FALSE`** 以及一个 **`E_WARNING`** 级别的错误。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">fileowner</span>
-   <span class="function">posix\_getgrgid</span>

fileinode
=========

取得文件的 inode

### 说明

<span class="type">int</span> <span class="methodname">fileinode</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得文件的 inode。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件的 inode 节点号， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 将某个文件和当前文件的 inode 进行对比**

``` php
<?php
$filename = 'index.php';
if (getmyinode() == fileinode($filename)) {
    echo 'You are checking the current file.';
}
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">getmyinode</span>
-   <span class="function">stat</span>

filemtime
=========

取得文件修改时间

### 说明

<span class="type">int</span> <span class="methodname">filemtime</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

本函数返回文件中的数据块上次被写入的时间，也就是说，文件的内容上次被修改的时间。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件上次被修改的时间， 或者在失败时返回 **`FALSE`**。时间以 Unix
时间戳的方式返回，可用于 <span class="function">date</span>。

### 范例

**示例 \#1 <span class="function">filemtime</span> 例子**

``` php
<?php
// outputs e.g.  somefile.txt was last modified: December 29 2002 22:16:23.

$filename = 'somefile.txt';
if (file_exists($filename)) {
    echo "$filename was last modified: " . date ("F d Y H:i:s.", filemtime($filename));
}
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**:
>
> 注意：不同文件系统对时间的判断方法可能是不相同的。

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">filectime</span>
-   <span class="function">stat</span>
-   <span class="function">touch</span>
-   <span class="function">getlastmod</span>

fileowner
=========

取得文件的所有者

### 说明

<span class="type">int</span> <span class="methodname">fileowner</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得文件的所有者。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件所有的用户 ID，如果出错则返回 **`FALSE`**。用户 ID
以数字格式返回，用 <span class="function">posix\_getpwuid</span>
来将其解析为用户名。

### 范例

**示例 \#1 找到文件的所有者**

``` php
<?php
$filename = 'index.php';
print_r(posix_getpwuid(fileowner($filename)));
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">filegroup</span>
-   <span class="function">stat</span>
-   <span class="function">posix\_getpwuid</span>

fileperms
=========

取得文件的权限

### 说明

<span class="type">int</span> <span class="methodname">fileperms</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得文件的权限。

### 参数

`filename`  
文件的路径。

### 返回值

以数字模式返回文件的访问权限。 Returns the file's permissions as a
numeric mode. Lower bits of this mode are the same as the permissions
expected by <span class="function">chmod</span>, however on most
platforms the return value will also include information on the type of
file given as `filename`. The examples below demonstrate how to test the
return value for specific permissions and file types on POSIX systems,
including Linux and Mac OS X.

For local files, the specific return value is that of the *st\_mode*
member of the structure returned by the C library's <span
class="function">stat</span> function. Exactly which bits are set can
vary from platform to platform, and looking up your specific platform's
documentation is recommended if parsing the non-permission bits of the
return value is required.

### 范例

**示例 \#1 以八进制的形式显示文件的权限**

``` php
<?php
echo substr(sprintf('%o', fileperms('/tmp')), -4);
echo substr(sprintf('%o', fileperms('/etc/passwd')), -4);
?>
```

以上例程会输出：

    1777
    0644

**示例 \#2 输出全部权限**

``` php
<?php
$perms = fileperms('/etc/passwd');

if (($perms & 0xC000) == 0xC000) {
    // Socket
    $info = 's';
} elseif (($perms & 0xA000) == 0xA000) {
    // Symbolic Link
    $info = 'l';
} elseif (($perms & 0x8000) == 0x8000) {
    // Regular
    $info = '-';
} elseif (($perms & 0x6000) == 0x6000) {
    // Block special
    $info = 'b';
} elseif (($perms & 0x4000) == 0x4000) {
    // Directory
    $info = 'd';
} elseif (($perms & 0x2000) == 0x2000) {
    // Character special
    $info = 'c';
} elseif (($perms & 0x1000) == 0x1000) {
    // FIFO pipe
    $info = 'p';
} else {
    // Unknown
    $info = 'u';
}

// Owner
$info .= (($perms & 0x0100) ? 'r' : '-');
$info .= (($perms & 0x0080) ? 'w' : '-');
$info .= (($perms & 0x0040) ?
            (($perms & 0x0800) ? 's' : 'x' ) :
            (($perms & 0x0800) ? 'S' : '-'));

// Group
$info .= (($perms & 0x0020) ? 'r' : '-');
$info .= (($perms & 0x0010) ? 'w' : '-');
$info .= (($perms & 0x0008) ?
            (($perms & 0x0400) ? 's' : 'x' ) :
            (($perms & 0x0400) ? 'S' : '-'));

// World
$info .= (($perms & 0x0004) ? 'r' : '-');
$info .= (($perms & 0x0002) ? 'w' : '-');
$info .= (($perms & 0x0001) ?
            (($perms & 0x0200) ? 't' : 'x' ) :
            (($perms & 0x0200) ? 'T' : '-'));

echo $info;
?>
```

以上例程会输出：

    -rw-r--r--

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">chmod</span>
-   <span class="function">is\_readable</span>
-   <span class="function">stat</span>

filesize
========

取得文件大小

### 说明

<span class="type">int</span> <span class="methodname">filesize</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

取得指定文件的大小。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件大小的字节数，如果出错返回 **`FALSE`** 并生成一条
**`E_WARNING`** 级的错误。

> **Note**: <span class="simpara"> 因为 PHP
> 的整数类型是有符号整型而且很多平台使用 32 位整型，对 2GB
> 以上的文件，一些文件系统函数可能返回无法预期的结果。</span>

### 范例

**示例 \#1 <span class="function">filesize</span> 例子**

``` php
<?php

// 输出类似：somefile.txt: 1024 bytes

$filename = 'somefile.txt';
echo $filename . ': ' . filesize($filename) . ' bytes';

?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">file\_exists</span>

filetype
========

取得文件类型

### 说明

<span class="type">string</span> <span
class="methodname">filetype</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

返回文件的类型。

### 参数

`filename`  
文件的路径。

### 返回值

返回文件的类型。 可能的值有 fifo，char，dir，block，link，file 和
unknown。

如果出错则返回 **`FALSE`**。如果 stat 调用失败或者文件类型未知的话 <span
class="function">filetype</span> 还会产生一个 **`E_NOTICE`** 消息。

### 范例

**示例 \#1 <span class="function">filetype</span> 例子**

``` php
<?php

echo filetype('/etc/passwd');  // file
echo filetype('/etc/');        // dir

?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">is\_file</span>
-   <span class="function">is\_link</span>
-   <span class="function">file\_exists</span>
-   <span class="function">mime\_content\_type</span>
-   <span class="function">pathinfo</span>
-   <span class="function">stat</span>

flock
=====

轻便的咨询文件锁定

### 说明

<span class="type">bool</span> <span class="methodname">flock</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">int</span> `$operation`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$wouldblock`</span>
\] )

<span class="function">flock</span>
允许执行一个简单的可以在任何平台中使用的读取/写入模型（包括大部分的 Unix
派生版和甚至是 Windows）。

在 PHP 5.3.2版本之前，锁也会被 <span class="function">fclose</span>
释放（在脚本结束后会自动调用）。

PHP 支持以咨询方式（也就是说所有访问程序必须使用同一方式锁定,
否则它不会工作）锁定全部文件的一种轻便方法。
默认情况下，这个函数会阻塞到获取锁；这可以通过下面文档中 **`LOCK_NB`**
选项来控制（在非 Windows 平台上）。

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

`operation`  
`operation` 可以是以下值之一：

-   <span class="simpara"> **`LOCK_SH`**取得共享锁定（读取的程序）。
    </span>
-   <span class="simpara"> **`LOCK_EX`** 取得独占锁定（写入的程序。
    </span>
-   <span class="simpara"> **`LOCK_UN`** 释放锁定（无论共享或独占）。
    </span>

如果不希望 <span class="function">flock</span> 在锁定时堵塞，则是
**`LOCK_NB`**（Windows 上还不支持）。

`wouldblock`  
如果锁定会堵塞的话（EWOULDBLOCK
错误码情况下），可选的第三个参数会被设置为 **`TRUE`**。（Windows
上不支持）

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                            |
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| 5.3.2 | 在文件资源句柄关闭时不再自动解锁。现在要解锁必须手动进行。                                                                      |
| 4.0.1 | 增加了常量 *LOCK\_XXX*。 之前你必须使用 1 代表 **`LOCK_SH`**，2 代表 **`LOCK_EX`**，3 代表**`LOCK_UN`**，4 代表 **`LOCK_NB`**。 |

### 范例

**示例 \#1 <span class="function">flock</span> 例子**

``` php
<?php

$fp = fopen("/tmp/lock.txt", "r+");

if (flock($fp, LOCK_EX)) {  // 进行排它型锁定
    ftruncate($fp, 0);      // truncate file
    fwrite($fp, "Write something here\n");
    fflush($fp);            // flush output before releasing the lock
    flock($fp, LOCK_UN);    // 释放锁定
} else {
    echo "Couldn't get the lock!";
}

fclose($fp);

?>
```

**示例 \#2 <span class="function">flock</span> 使用 **`LOCK_NB`** 选项**

``` php
<?php
$fp = fopen('/tmp/lock.txt', 'r+');

/* Activate the LOCK_NB option on an LOCK_EX operation */
if(!flock($fp, LOCK_EX | LOCK_NB)) {
    echo 'Unable to obtain lock';
    exit(-1);
}

/* ... */

fclose($fp);
?>
```

### 注释

> **Note**:
>
> <span class="function">flock</span> uses mandatory locking instead of
> advisory locking on Windows. Mandatory locking is also supported on
> Linux and System V based operating systems via the usual mechanism
> supported by the fcntl() system call: that is, if the file in question
> has the setgid permission bit set and the group execution bit cleared.
> On Linux, the file system will also need to be mounted with the mand
> option for this to work.

> **Note**:
>
> 由于 <span class="function">flock</span> 需要一个文件指针，
> 因此可能不得不用一个特殊的锁定文件来保护打算通过写模式打开的文件的访问（在
> <span class="function">fopen</span> 函数中加入 "w" 或 "w+"）。

> **Note**:
>
> May only be used on file pointers returned by <span
> class="function">fopen</span> for local files, or file pointers
> pointing to userspace streams that implement the <span
> class="function">streamWrapper::stream\_lock</span> method.

**Warning**

Assigning another value to `handle` argument in subsequent code will
release the lock.

**Warning**

在部分操作系统中 <span class="function">flock</span>
以进程级实现。当用一个多线程服务器 API（比如 ISAPI）时，可能不可以依靠
<span class="function">flock</span>
来保护文件，因为运行于同一服务器实例中其它并行线程的 PHP
脚本可以对该文件进行处理。

<span class="function">flock</span> 不支持旧的文件系统，如 *FAT*
以及它的派生系统。因此，此环境下总是返回 **`FALSE`**（尤其是对 Windows
98 用户来说）。

fnmatch
=======

用模式匹配文件名

### 说明

<span class="type">bool</span> <span class="methodname">fnmatch</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

<span class="function">fnmatch</span> 检查传入的 `string` 是否匹配给出的
shell 统配符 `pattern`。

### 参数

`pattern`  
shell 统配符。

`string`  
要检查的字符串。 此函数对于文件名尤其有用，但也可以用于普通的字符串。

普通用户可能习惯于 shell 模式或者至少其中最简单的形式 *'?'* 和 *'\*'*
通配符，因此使用 <span class="function">fnmatch</span> 来代替 <span
class="function">preg\_match</span>
来进行前端搜索表达式输入对于非程序员用户更加方便。

`flags`  
The value of `flags` can be any combination of the following flags,
joined with the
<a href="/language/operators/bitwise.html" class="link">binary OR (|) operator</a>.

| `Flag`             | Description                                                                      |
|--------------------|----------------------------------------------------------------------------------|
| **`FNM_NOESCAPE`** | Disable backslash escaping.                                                      |
| **`FNM_PATHNAME`** | Slash in string only matches slash in the given pattern.                         |
| **`FNM_PERIOD`**   | Leading period in string must be exactly matched by period in the given pattern. |
| **`FNM_CASEFOLD`** | Caseless match. Part of the GNU extension.                                       |

### 返回值

匹配则返回 **`TRUE`**，否则返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                              |
|-------|-----------------------------------|
| 5.3.0 | 此函数开始在 Windows 平台上生效。 |

### 范例

**示例 \#1 用 shell 中的通配符模式匹配来检查颜色名称**

``` php
<?php
if (fnmatch("*gr[ae]y", $color)) {
  echo "some form of gray ...";
}
?>
```

### 注释

**Warning**

目前该函数无法在 Windows 或其它非 POSIX 兼容的系统上使用。

### 参见

-   <span class="function">glob</span>
-   <span class="function">preg\_match</span>
-   <span class="function">sscanf</span>
-   <span class="function">printf</span>
-   <span class="function">sprintf</span>

fopen
=====

打开文件或者 URL

### 说明

<span class="type">resource</span> <span class="methodname">fopen</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">resource</span>
`$context`</span> \]\] )

<span class="function">fopen</span> 将 `filename`
指定的名字资源绑定到一个流上。

### 参数

`filename`  
如果 `filename` 是 "scheme://..." 的格式，则被当成一个 URL，PHP
将搜索协议处理器（也被称为封装协议）来处理此模式。如果该协议尚未注册封装协议，PHP
将发出一条消息来帮助检查脚本中潜在的问题并将 `filename`
当成一个普通的文件名继续执行下去。

如果 PHP 认为 `filename`
指定的是一个本地文件，将尝试在该文件上打开一个流。该文件必须是 PHP
可以访问的，因此需要确认文件访问权限允许该访问。如果激活了
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
则会应用进一步的限制。

如果 PHP 认为 `filename`
指定的是一个已注册的协议，而该协议被注册为一个网络 URL，PHP 将检查并确认
<a href="/filesystem/setup.html#" class="link">allow_url_fopen</a>
已被激活。如果关闭了，PHP 将发出一个警告，而 fopen 的调用则失败。

> **Note**:
>
> 所支持的协议列表见<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>。某些协议（也被称为
> *wrappers*）支持 *context* 和／或 `php.ini`
> 选项。参见相应的页面哪些选项可以被设定（例如 `php.ini` 中用于 *http*
> wrapper 的 *user\_agent* 值）。

On the Windows platform, be careful to escape any backslashes used in
the path to the file, or use forward slashes.

``` php
<?php
$handle = fopen("c:\\folder\\resource.txt", "r");
?>
```

`mode`  
`mode` 参数指定了所要求到该流的访问类型。可以是以下：

| `mode` | 说明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *'r'*  | 只读方式打开，将文件指针指向文件头。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *'r+'* | 读写方式打开，将文件指针指向文件头。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *'w'*  | 写入方式打开，将文件指针指向文件头并将文件大小截为零。如果文件不存在则尝试创建之。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| *'w+'* | 读写方式打开，将文件指针指向文件头并将文件大小截为零。如果文件不存在则尝试创建之。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| *'a'*  | 写入方式打开，将文件指针指向文件末尾。如果文件不存在则尝试创建之。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| *'a+'* | 读写方式打开，将文件指针指向文件末尾。如果文件不存在则尝试创建之。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| *'x'*  | 创建并以写入方式打开，将文件指针指向文件头。如果文件已存在，则 <span class="function">fopen</span> 调用失败并返回 **`FALSE`**，并生成一条 **`E_WARNING`** 级别的错误信息。如果文件不存在则尝试创建之。这和给 底层的 *open(2)* 系统调用指定 *O\_EXCL\|O\_CREAT* 标记是等价的。                                                                                                                                                                                                                                                                                                                     |
| *'x+'* | 创建并以读写方式打开，其他的行为和 *'x'* 一样。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *'c'*  | Open the file for writing only. If the file does not exist, it is created. If it exists, it is neither truncated (as opposed to *'w'*), nor the call to this function fails (as is the case with *'x'*). The file pointer is positioned on the beginning of the file. This may be useful if it's desired to get an advisory lock (see <span class="function">flock</span>) before attempting to modify the file, as using *'w'* could truncate the file before the lock was obtained (if truncation is desired, <span class="function">ftruncate</span> can be used after the lock is requested). |
| *'c+'* | Open the file for reading and writing; otherwise it has the same behavior as *'c'*.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

> **Note**:
>
> 不同的操作系统家族具有不同的行结束习惯。当写入一个文本文件并想插入一个新行时，需要使用符合操作系统的行结束符号。基于
> Unix 的系统使用 *\\n* 作为行结束字符，基于 Windows 的系统使用 *\\r\\n*
> 作为行结束字符，基于 Macintosh 的系统使用 *\\r* 作为行结束字符。
>
> 如果写入文件时使用了错误的行结束符号，则其它应用程序打开这些文件时可能会表现得很怪异。
>
> Windows 下提供了一个文本转换标记（*'t'*）可以透明地将 *\\n* 转换为
> *\\r\\n*。与此对应还可以使用 *'b'*
> 来强制使用二进制模式，这样就不会转换数据。要使用这些标记，要么用 *'b'*
> 或者用 *'t'* 作为 `mode` 参数的最后一个字符。
>
> 默认的转换模式依赖于 SAPI 和所使用的 PHP
> 版本，因此为了便于移植鼓励总是指定恰当的标记。如果是操作纯文本文件并在脚本中使用了
> *\\n* 作为行结束符，但还要期望这些文件可以被其它应用程序例如 Notepad
> 读取，则在 mode 中使用 *'t'*。在所有其它情况下使用 *'b'*。
>
> 在操作二进制文件时如果没有指定 *'b'*
> 标记，可能会碰到一些奇怪的问题，包括坏掉的图片文件以及关于 *\\r\\n*
> 字符的奇怪问题。

> **Note**:
>
> 为移植性考虑，强烈建议在用 <span class="function">fopen</span>
> 打开文件时总是使用 *'b'* 标记。

> **Note**:
>
> 再一次，为移植性考虑，强烈建议你重写那些依赖于 *'t'*
> 模式的代码使其使用正确的行结束符并改成 *'b'* 模式。

`use_include_path`  
如果也需要在
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
中搜寻文件的话，可以将可选的第三个参数 `use_include_path` 设为 '1' 或
**`TRUE`**。

`context`  
> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

成功时返回文件指针资源，如果打开失败，本函数返回 **`FALSE`**。

### 错误／异常

如果打开失败，会产生一个 **`E_WARNING`** 错误。可以通过
<a href="/language/operators/errorcontrol.html" class="link">@</a>
来屏蔽错误。

### 更新日志

| 版本  | 说明                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.3.2 | 自 PHP 4.3.2 起，对所有区别二进制和文本模式的平台默认模式都被设为二进制模式。如果在升级后脚本碰到问题，尝试暂时使用 *'t'* 标记，直到所有的脚本都照以下所说的改为更具移植性以后。 |
| 4.3.2 | 增加了选项 *'x'* 和 *'x+'*                                                                                                                                                       |
| 5.2.6 | 增加了选项 *'c'* 和 *'c+'*                                                                                                                                                       |

### 范例

**示例 \#1 <span class="function">fopen</span> 例子**

``` php
<?php
$handle = fopen("/home/rasmus/file.txt", "r");
$handle = fopen("/home/rasmus/file.gif", "wb");
$handle = fopen("http://www.example.com/", "r");
$handle = fopen("ftp://user:password@example.com/somefile.txt", "w");
?>
```

### 注释

**Warning**

使用 SSL 时，Microsoft IIS
会违反协议不发送*close\_notify*标记就关闭连接。PHP
会在到达数据尾端时报告“SSL: Fatal Protocol Error”。
要解决此问题，<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
应设定为降低级别至不包含警告。 PHP 4.3.7 及更高版本可以在使用 *https://*
包装器打开流时检测出有问题的 IIS 服务器软件 并抑制警告。在使用 <span
class="function">fsockopen</span> 创建 *ssl://* 套接字时,
开发者需检测并抑制此警告。

> **Note**:
>
> 如果在用服务器模块版本的 PHP
> 时在打开和写入文件上遇到问题，记住要确保所使用的文件和目录是服务器进程所能够访问的。

> **Note**:
>
> This function may also succeed when `filename` is a directory. If you
> are unsure whether `filename` is a file or a directory, you may need
> to use the <span class="function">is\_dir</span> function before
> calling <span class="function">fopen</span>.

### 参见

-   <a href="/wrappers.html" class="xref">支持的协议和封装协议</a>
-   <span class="function">fclose</span>
-   <span class="function">fgets</span>
-   <span class="function">fread</span>
-   <span class="function">fwrite</span>
-   <span class="function">fsockopen</span>
-   <span class="function">file</span>
-   <span class="function">file\_exists</span>
-   <span class="function">is\_readable</span>
-   <span class="function">stream\_set\_timeout</span>
-   <span class="function">popen</span>
-   <span class="function">stream\_context\_create</span>
-   <span class="function">umask</span>
-   <span class="classname">SplFileObject</span>

fpassthru
=========

输出文件指针处的所有剩余数据

### 说明

<span class="type">int</span> <span class="methodname">fpassthru</span>
( <span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

将给定的文件指针从当前的位置读取到 EOF 并把结果写到输出缓冲区。

如果已经向文件写入数据，就必须调用 <span class="function">rewind</span>
来将文件指针指向文件头。

如果既不修改文件也不在特定位置检索，只想将文件的内容下载到输出缓冲区，应该使用
<span class="function">readfile</span>，这样可以省去 <span
class="function">fopen</span> 调用。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

### 返回值

如果发生错误， <span class="function">fpassthru</span> 返回
**`FALSE`**。否则 <span class="function">fpassthru</span> 返回从
`handle` 读取并传递到输出的字符数目。

### 范例

**示例 \#1 对二进制文件使用 <span class="function">fpassthru</span>**

``` php
<?php

// 以二进制格式打开文件
$name = './img/ok.png';
$fp = fopen($name, 'rb');

// 发送合适的报头
header("Content-Type: image/png");
header("Content-Length: " . filesize($name));

// 发送图片并终止脚本
fpassthru($fp);
exit;

?>
```

### 注释

> **Note**:
>
> 当在 Windows 系统中将 <span class="function">fpassthru</span>
> 用于二进制文件，要确保在用 <span class="function">fopen</span>
> 打开文件时在 mode 中附加了 *b* 来将文件以二进制方式打开。
>
> 鼓励在处理二进制文件时使用 *b*
> 标志，即使系统并不需要，这样可以使脚本的移植性更好。

### 参见

-   <span class="function">readfile</span>
-   <span class="function">fopen</span>
-   <span class="function">popen</span>
-   <span class="function">fsockopen</span>

fputcsv
=======

将行格式化为 CSV 并写入文件指针

### 说明

<span class="type">int</span> <span class="methodname">fputcsv</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">array</span> `$fields`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = ','</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$enclosure`<span
class="initializer"> = '"'</span></span> \]\] )

<span class="function">fputcsv</span> 将一行（用 `fields`
数组传递）格式化为 CSV 格式并写入由 `handle` 指定的文件。

### 参数

`handle`  
文件指针必须是有效的，必须指向由 <span class="function">fopen</span> 或
<span class="function">fsockopen</span> 成功打开的文件(并还未由 <span
class="function">fclose</span> 关闭)。

`fields`  
值的一个数组。

`delimiter`  
可选的 `delimiter` 参数设定字段分界符（只允许一个字符）。

`enclosure`  
可选的 `enclosure` 参数设定字段字段环绕符（只允许一个字符）。

### 返回值

返回写入字符串的长度， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">fputcsv</span> 例子**

``` php
<?php

$list = array (
    array('aaa', 'bbb', 'ccc', 'dddd'),
    array('123', '456', '789'),
    array('"aaa"', '"bbb"')
);

$fp = fopen('file.csv', 'w');

foreach ($list as $fields) {
    fputcsv($fp, $fields);
}

fclose($fp);
?>
```

以上例子会写入以下的*file.csv*：

    aaa,bbb,ccc,dddd
    123,456,789
    """aaa""","""bbb"""

### 注释

> **Note**: <span class="simpara">在读取在 Macintosh
> 电脑中或由其创建的文件时， 如果 PHP
> 不能正确的识别行结束符，启用运行时配置可选项
> <a href="/filesystem/setup.html#" class="link">auto_detect_line_endings</a>
> 也许可以解决此问题。</span>

### 参见

-   <span class="function">fgetcsv</span>

fputs
=====

<span class="function">fwrite</span> 的别名

### 说明

此函数是该函数的别名：<span class="function">fwrite</span>。

fread
=====

读取文件（可安全用于二进制文件）

### 说明

<span class="type">string</span> <span class="methodname">fread</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">int</span> `$length`</span> )

<span class="function">fread</span> 从文件指针 `handle` 读取最多
`length` 个字节。 该函数在遇上以下几种情况时停止读取文件：

-   <span class="simpara"> 读取了 `length` 个字节 </span>
-   <span class="simpara"> 到达了文件末尾（EOF） </span>
-   <span class="simpara"> a packet becomes available or the
    <a href="/ref/network.html#socket_set_timeout" class="link">socket timeout</a>
    occurs (for network streams) </span>
-   <span class="simpara"> if the stream is read buffered and it does
    not represent a plain file, at most one read of up to a number of
    bytes equal to the chunk size (usually 8192) is made; depending on
    the previously buffered data, the size of the returned data may be
    larger than the chunk size. </span>

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

`length`  
最多读取 `length` 个字节。

### 返回值

返回所读取的字符串， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 一个简单的 <span class="function">fread</span> 例子**

``` php
<?php
// get contents of a file into a string
$filename = "/usr/local/something.txt";
$handle = fopen($filename, "r");
$contents = fread($handle, filesize($filename));
fclose($handle);
?>
```

**示例 \#2 Binary <span class="function">fread</span> example**

**Warning**

在区分二进制文件和文本文件的系统上（如 Windows）打开文件时，<span
class="function">fopen</span> 函数的 mode 参数要加上 'b'。

``` php
<?php
$filename = "c:\\files\\somepic.gif";
$handle = fopen($filename, "rb");
$contents = fread($handle, filesize($filename));
fclose($handle);
?>
```

**示例 \#3 Remote <span class="function">fread</span> examples**

**Warning**

当从任何不是普通本地文件读取时，例如在读取从<a href="/features/remote-files.html" class="link">远程文件</a>或
<span class="function">popen</span> 以及 <span
class="function">fsockopen</span>
返回的流时，读取会在一个包可用之后停止。这意味着应该如下例所示将数据收集起来合并成大块。

``` php
<?php
// 对 PHP 5 及更高版本
$handle = fopen("http://www.example.com/", "rb");
$contents = stream_get_contents($handle);
fclose($handle);
?>
```

``` php
<?php
$handle = fopen("http://www.example.com/", "rb");
$contents = '';
while (!feof($handle)) {
  $contents .= fread($handle, 8192);
}
fclose($handle);
?>
```

### 注释

> **Note**:
>
> 如果只是想将一个文件的内容读入到一个字符串中，用 <span
> class="function">file\_get\_contents</span>，它的性能比上面的代码好得多。

> **Note**:
>
> Note that <span class="function">fread</span> reads from the current
> position of the file pointer. Use <span class="function">ftell</span>
> to find the current position of the pointer and <span
> class="function">rewind</span> to rewind the pointer position.

### 参见

-   <span class="function">fwrite</span>
-   <span class="function">fopen</span>
-   <span class="function">fsockopen</span>
-   <span class="function">popen</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetss</span>
-   <span class="function">fscanf</span>
-   <span class="function">file</span>
-   <span class="function">fpassthru</span>
-   <span class="function">ftell</span>
-   <span class="function">rewind</span>

fscanf
======

从文件中格式化输入

### 说明

<span class="type">mixed</span> <span class="methodname">fscanf</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `&$...`</span> \] )

<span class="function">fscanf</span> 函数和 <span
class="function">sscanf</span> 相似，但是它从与 `handle`
关联的文件中接受输入并根据指定的 `format`（定义于 <span
class="function">sprintf</span> 的文档中）来解释输入。

格式字符串中的任何空白会与输入流中的任何空白匹配。这意味着甚至格式字符串中的制表符
*\\t* 也会与输入流中的一个空格字符匹配。

每次调用 <span class="function">fscanf</span> 都会从文件中读取一行。

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

`format`  
参数格式是 <span class="function">sprintf</span> 文档中所描述的格式。

`...`  
The optional assigned values.

### 返回值

如果只给此函数传递了两个参数，解析后的值会被作为数组返回。否则，如果提供了可选参数，此函数将返回被赋值的数目。
可选参数必须用引用传递。

### 更新日志

| 版本  | 说明                                                                                                                       |
|-------|----------------------------------------------------------------------------------------------------------------------------|
| 4.3.0 | 在 PHP 4.3.0 之前，从文件中读入的最大字符数是 512（或者第一个 \\n，看先碰到哪种情况）。从 PHP 4.3.0 起可以读取任意长的行。 |

### 范例

**示例 \#1 <span class="function">fscanf</span> 例子**

``` php
<?php
$handle = fopen("users.txt", "r");
while ($userinfo = fscanf($handle, "%s\t%s\t%s\n")) {
    list ($name, $profession, $countrycode) = $userinfo;
    //... do something with the values
}
fclose($handle);
?>
```

**示例 \#2 users.txt 的内容**

``` txt
javier  argonaut        pe
hiroshi sculptor        jp
robert  slacker us
luigi   florist it
```

### 参见

-   <span class="function">fread</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetss</span>
-   <span class="function">sscanf</span>
-   <span class="function">printf</span>
-   <span class="function">sprintf</span>

fseek
=====

在文件指针中定位

### 说明

<span class="type">int</span> <span class="methodname">fseek</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">int</span> `$offset`</span> \[, <span
class="methodparam"><span class="type">int</span> `$whence`<span
class="initializer"> = SEEK\_SET</span></span> \] )

在与 `handle` 关联的文件中设定文件指针位置。
新位置从文件头开始以字节数度量，是以 `whence` 指定的位置加上 `offset`。

In general, it is allowed to seek past the end-of-file; if data is then
written, reads in any unwritten region between the end-of-file and the
sought position will yield bytes with value 0. However, certain streams
may not support this behavior, especially when they have an underlying
fixed size storage.

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

`offset`  
偏移量。

要移动到文件尾之前的位置，需要给 `offset` 传递一个负值，并设置 `whence`
为 **`SEEK_END`**。

`whence`  
`whence` values are:

-   **`SEEK_SET`** - 设定位置等于 `offset` 字节。
-   **`SEEK_CUR`** - 设定位置为当前位置加上 `offset`。
-   **`SEEK_END`** - 设定位置为文件尾加上 `offset`。

### 返回值

成功则返回 0；否则返回 -1。注意移动到 EOF 之后的位置不算错误。

### 范例

**示例 \#1 <span class="function">fseek</span> 例子**

``` php
<?php

$fp = fopen('somefile.txt', 'r');

// read some data
$data = fgets($fp, 4096);

// move back to the beginning of the file
// same as rewind($fp);
fseek($fp, 0);

?>
```

### 注释

> **Note**:
>
> 如果使用附加模试（*a* 或
> *a+*），任何写入文件数据都会被附加上去，而文件的位置将会被忽略，调用
> <span class="function">fseek</span> 的结果尚未定义。

> **Note**:
>
> Not all streams support seeking. For those that do not support
> seeking, forward seeking from the current position is accomplished by
> reading and discarding data; other forms of seeking will fail.

### 参见

-   <span class="function">ftell</span>
-   <span class="function">rewind</span>

fstat
=====

通过已打开的文件指针取得文件信息

### 说明

<span class="type">array</span> <span class="methodname">fstat</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

获取由文件指针 `handle` 所打开文件的统计信息。本函数和 <span
class="function">stat</span>
函数相似，除了它是作用于已打开的文件指针而不是文件名。

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

### 返回值

返回一个数组具有该文件的统计信息，该数组的格式详细说明于手册中 <span
class="function">stat</span> 页面里。

### 范例

**示例 \#1 <span class="function">fstat</span> 例子**

``` php
<?php

// 打开文件
$fp = fopen("/etc/passwd", "r");

// 取得统计信息
$fstat = fstat($fp);

// 关闭文件
fclose($fp);

// 只显示关联数组部分
print_r(array_slice($fstat, 13));
?>
```

以上例程的输出类似于：

    Array
    (
        [dev] => 771
        [ino] => 488704
        [mode] => 33188
        [nlink] => 1
        [uid] => 0
        [gid] => 0
        [rdev] => 0
        [size] => 1114
        [atime] => 1061067181
        [mtime] => 1056136526
        [ctime] => 1056136526
        [blksize] => 4096
        [blocks] => 8
    )

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

ftell
=====

返回文件指针读/写的位置

### 说明

<span class="type">int</span> <span class="methodname">ftell</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

返回由 `handle` 指定的文件指针的位置，也就是文件流中的偏移量。

### 参数

`handle`  
文件指针必须是有效的，且必须指向一个通过 <span
class="function">fopen</span> 或 <span class="function">popen</span>
成功打开的文件。在附加模式（加参数 "a" 打开文件）中 <span
class="function">ftell</span> 会返回未定义错误。

### 返回值

Returns the position of the file pointer referenced by `handle` as an
integer; i.e., its offset into the file stream.

如果出错，返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftell</span> 例子**

``` php
<?php

// opens a file and read some data
$fp = fopen("/etc/passwd", "r");
$data = fgets($fp, 12);

// where are we ?
echo ftell($fp); // 11

fclose($fp);

?>
```

### 参见

-   <span class="function">fopen</span>
-   <span class="function">popen</span>
-   <span class="function">fseek</span>
-   <span class="function">rewind</span>

ftruncate
=========

将文件截断到给定的长度

### 说明

<span class="type">bool</span> <span class="methodname">ftruncate</span>
( <span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">int</span> `$size`</span> )

接受文件指针 `handle` 作为参数，并将文件大小截取为 `size`。

### 参数

`handle`  
文件指针。

> **Note**:
>
> The `handle` must be open for writing.

`size`  
The size to truncate to.

> **Note**:
>
> If `size` is larger than the file then the file is extended with null
> bytes.
>
> If `size` is smaller than the file then the file is truncated to that
> size.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                         |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.3.3 | 在 PHP 4.3.3 之前，<span class="function">ftruncate</span> 在成功时返回一个 <span class="type">integer</span> 值 1，而不是 <span class="type">boolean</span> 的 **`TRUE`**。 |

### 范例

**示例 \#1 File truncation example**

``` php
<?php
$filename = 'lorem_ipsum.txt';

$handle = fopen($filename, 'r+');
ftruncate($handle, rand(1, filesize($filename)));
rewind($handle);
echo fread($handle, filesize($filename));
fclose($handle);
?>
```

### 注释

> **Note**:
>
> The file pointer is *not* changed.

### 参见

-   <span class="function">fopen</span>
-   <span class="function">fseek</span>

fwrite
======

写入文件（可安全用于二进制文件）

### 说明

<span class="type">int</span> <span class="methodname">fwrite</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> , <span class="methodparam"><span
class="type">string</span> `$string`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

<span class="function">fwrite</span> 把 `string` 的内容写入 文件指针
`handle` 处。

### 参数

`handle`  
文件系统指针，是典型地由 <span class="function">fopen</span> 创建的
<span class="type">resource</span>(资源)。

`string`  
The string that is to be written.

`length`  
如果指定了 `length`，当写入了 `length` 个字节或者写完了 `string`
以后，写入就会停止，视乎先碰到哪种情况。

注意如果给出了 `length` 参数，则
<a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
配置选项将被忽略，而 `string` 中的斜线将不会被抽去。

### 返回值

<span class="function">fwrite</span> 返回写入的字符数，出现错误时则返回
**`FALSE`** 。

### 注释

> **Note**:
>
> Writing to a network stream may end before the whole string is
> written. Return value of <span class="function">fwrite</span> may be
> checked:
>
> ``` php
> <?php
> function fwrite_stream($fp, $string) {
>     for ($written = 0; $written < strlen($string); $written += $fwrite) {
>         $fwrite = fwrite($fp, substr($string, $written));
>         if ($fwrite === false) {
>             return $written;
>         }
>     }
>     return $written;
> }
> ?>
> ```

> **Note**:
>
> 在区分二进制文件和文本文件的系统上（如 Windows） 打开文件时，<span
> class="function">fopen</span> 函数的 mode 参数要加上 'b'。

> **Note**:
>
> If `handle` was <span class="function">fopen</span>ed in append mode,
> <span class="function">fwrite</span>s are atomic (unless the size of
> `string` exceeds the filesystem's block size, on some platforms, and
> as long as the file is on a local filesystem). That is, there is no
> need to <span class="function">flock</span> a resource before calling
> <span class="function">fwrite</span>; all of the data will be written
> without interruption.

> **Note**:
>
> If writing twice to the file pointer, then the data will be appended
> to the end of the file content:
>
> ``` php
> <?php
> $fp = fopen('data.txt', 'w');
> fwrite($fp, '1');
> fwrite($fp, '23');
> fclose($fp);
>
> // the content of 'data.txt' is now 123 and not 23!
> ?>
> ```

### 范例

**示例 \#1 一个简单的 <span class="function">fwrite</span> 例子**

``` php
<?php
$filename = 'test.txt';
$somecontent = "添加这些文字到文件\n";

// 首先我们要确定文件存在并且可写。
if (is_writable($filename)) {

    // 在这个例子里，我们将使用添加模式打开$filename，
    // 因此，文件指针将会在文件的末尾，
    // 那就是当我们使用fwrite()的时候，$somecontent将要写入的地方。
    if (!$handle = fopen($filename, 'a')) {
         echo "不能打开文件 $filename";
         exit;
    }

    // 将$somecontent写入到我们打开的文件中。
    if (fwrite($handle, $somecontent) === FALSE) {
        echo "不能写入到文件 $filename";
        exit;
    }

    echo "成功地将 $somecontent 写入到文件$filename";

    fclose($handle);

} else {
    echo "文件 $filename 不可写";
}
?>
```

### 参见

-   <span class="function">fread</span>
-   <span class="function">fopen</span>
-   <span class="function">fsockopen</span>
-   <span class="function">popen</span>
-   <span class="function">file\_get\_contents</span>

glob
====

寻找与模式匹配的文件路径

### 说明

<span class="type">array</span> <span class="methodname">glob</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \] )

<span class="function">glob</span> 函数依照 libc glob()
函数使用的规则寻找所有与 `pattern` 匹配的文件路径，类似于一般 shells
所用的规则一样。

### 参数

`pattern`  
匹配模式（pattern）。 不进行缩写扩展或参数替代。

特殊字符：

-   <span class="simpara"> *\** - 匹配零个或多个字符。 </span>
-   <span class="simpara"> *?* - 只匹配单个字符（任意字符）。 </span>
-   <span class="simpara"> *\[...\]* - 匹配一组字符中的一个字符。
    如果第一个字符是 *!*，则为否定模式，
    即匹配不在这组字符中的任意字符。 </span>
-   <span class="simpara"> *\\* - 只要没有使用 **`GLOB_NOESCAPE`**
    标记，该字符会转义后面的字符。 </span>

`flags`  
有效标记有：

-   <span class="simpara"> **`GLOB_MARK`** -
    在每个返回的项目中加一个斜线 </span>
-   <span class="simpara"> **`GLOB_NOSORT`** -
    按照文件在目录中出现的原始顺序返回（不排序） </span>
-   <span class="simpara"> **`GLOB_NOCHECK`** -
    如果没有文件匹配则返回用于搜索的模式 </span>
-   <span class="simpara"> **`GLOB_NOESCAPE`** - 反斜线不转义元字符
    </span>
-   <span class="simpara"> **`GLOB_BRACE`** - 扩充 {a,b,c} 来匹配
    'a'，'b' 或 'c' </span>
-   <span class="simpara"> **`GLOB_ONLYDIR`** - 仅返回与模式匹配的目录项
    </span>
-   <span class="simpara"> **`GLOB_ERR`** -
    停止并读取错误信息（比如说不可读的目录），默认的情况下忽略所有错误
    </span>

### 返回值

返回包含有匹配文件和目录的数组，没有匹配文件时返回空数组，出错返回
**`FALSE`**。

> **Note**:
>
> 在个别操作系统上，无法区分是否为空匹配或错误。

### 范例

**示例 \#1 怎样用 <span class="function">glob</span> 方便地替代 <span
class="function">opendir</span> 和相关函数**

``` php
<?php
foreach (glob("*.txt") as $filename) {
    echo "$filename size " . filesize($filename) . "\n";
}
?>
```

以上例程的输出类似于：

    funclist.txt size 44686
    funcsummary.txt size 267625
    quickref.txt size 137820

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

> **Note**: <span class="simpara">
> 此函数在一些系统上还不能工作（例如一些旧的 Sun OS）。 </span>

> **Note**: <span class="simpara"> **`GLOB_BRACE`** 在一些非 GNU
> 系统上无效，比如 Solaris。 </span>

### 参见

-   <span class="function">opendir</span>
-   <span class="function">readdir</span>
-   <span class="function">closedir</span>
-   <span class="function">fnmatch</span>

is\_dir
=======

判断给定文件名是否是一个目录

### 说明

<span class="type">bool</span> <span class="methodname">is\_dir</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

判断给定文件名是否是一个目录。

### 参数

`filename`  
如果文件名存在并且为目录则返回 **`TRUE`**。如果 `filename`
是一个相对路径，则按照当前工作目录检查其相对路径。 If `filename` is a
symbolic or hard link then the link will be resolved and checked.If you
have enabled
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
further restrictions may apply.

### 返回值

如果文件名存在，并且是个目录，返回 **`TRUE`**，否则返回**`FALSE`**。

### 范例

**示例 \#1 <span class="function">is\_dir</span> 例子**

``` php
<?php
var_dump(is_dir('a_file.txt'));
var_dump(is_dir('bogus_dir/abc'));

var_dump(is_dir('..')); //one dir up
?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(true)

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">chdir</span>
-   <span class="function">dir</span>
-   <span class="function">opendir</span>
-   <span class="function">is\_file</span>
-   <span class="function">is\_link</span>

is\_executable
==============

判断给定文件名是否可执行

### 说明

<span class="type">bool</span> <span
class="methodname">is\_executable</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

判断给定文件名是否可执行。

### 参数

`filename`  
文件的路径。

### 返回值

如果文件存在且可执行则返回 **`TRUE`**，错误时返回**`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                 |
|-------|------------------------------------------------------------------------------------------------------|
| 5.0.0 | <span class="function">is\_executable</span> 开始可用以于 <span class="productname">Windows</span>。 |

### 范例

**示例 \#1 <span class="function">is\_executable</span> 例子**

``` php
<?php

$file = '/home/vincent/somefile.sh';

if (is_executable($file)) {
    echo $file.' is executable';
} else {
    echo $file.' is not executable';
}

?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">is\_file</span>
-   <span class="function">is\_link</span>

is\_file
========

判断给定文件名是否为一个正常的文件

### 说明

<span class="type">bool</span> <span class="methodname">is\_file</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

判断给定文件名是否为一个正常的文件。

### 参数

`filename`  
文件的路径。

### 返回值

如果文件存在且为正常的文件则返回 **`TRUE`**，否则返回 **`FALSE`**。

> **Note**: <span class="simpara"> 因为 PHP
> 的整数类型是有符号整型而且很多平台使用 32 位整型，对 2GB
> 以上的文件，一些文件系统函数可能返回无法预期的结果。</span>

### 范例

**示例 \#1 <span class="function">is\_file</span> 例子**

``` php
<?php
var_dump(is_file('a_file.txt')) . "\n";
var_dump(is_file('/usr/bin/')) . "\n";
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">is\_link</span>

is\_link
========

判断给定文件名是否为一个符号连接

### 说明

<span class="type">bool</span> <span class="methodname">is\_link</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

判断给定文件名是否为一个符号连接。

### 参数

`filename`  
文件的路径。

### 返回值

如果文件存在并且是一个符号连接则返回 **`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 创建并确认一个文件是否为符号连接**

``` php
<?php
$link = 'uploads';

if (is_link($link)) {
    echo(readlink($link));
} else {
    symlink('uploads.php', $link);
}
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">is\_file</span>
-   <span class="function">readlink</span>

is\_readable
============

判断给定文件名是否可读

### 说明

<span class="type">bool</span> <span
class="methodname">is\_readable</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

判断给定文件名是否存在并且可读。

### 参数

`filename`  
文件的路径。

### 返回值

如果由 `filename` 指定的文件或目录存在并且可读则返回
**`TRUE`**，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">is\_readable</span> 例子**

``` php
<?php
$filename = 'test.txt';
if (is_readable($filename)) {
    echo 'The file is readable';
} else {
    echo 'The file is not readable';
}
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

记住 PHP 也许只能以运行 webserver 的用户名（通常为
'nobody'）来访问文件。不计入安全模式的限制。 Safe mode limitations are
not taken into account before PHP 5.1.5.

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

> **Note**:
>
> The check is done using the real UID/GID instead of the effective one.

对于目录这个函数可能会返回 **`TRUE`**。请使用 <span
class="function">is\_dir</span> 来区分文件和目录。

### 参见

-   <span class="function">is\_writable</span>
-   <span class="function">file\_exists</span>
-   <span class="function">fgets</span>

is\_uploaded\_file
==================

判断文件是否是通过 HTTP POST 上传的

### 说明

<span class="type">bool</span> <span
class="methodname">is\_uploaded\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

如果 `filename` 所给出的文件是通过 HTTP POST 上传的则返回
**`TRUE`**。这可以用来确保恶意的用户无法欺骗脚本去访问本不能访问的文件，例如
`/etc/passwd`。

这种检查显得格外重要，如果上传的文件有可能会造成对用户或本系统的其他用户显示其内容的话。

为了能使 <span class="function">is\_uploaded\_file</span>
函数正常工作，必段指定类似于 `$_FILES['userfile']['tmp_name']`
的变量，而在从客户端上传的文件名 `$_FILES['userfile']['name']`
不能正常运作。

### 参数

`filename`  
要检查的文件名。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">is\_uploaded\_file</span> 例子**

``` php
<?php

if (is_uploaded_file($_FILES['userfile']['tmp_name'])) {
   echo "File ". $_FILES['userfile']['name'] ." uploaded successfully.\n";
   echo "Displaying contents\n";
   readfile($_FILES['userfile']['tmp_name']);
} else {
   echo "Possible file upload attack: ";
   echo "filename '". $_FILES['userfile']['tmp_name'] . "'.";
}

?>
```

### 参见

-   <span class="function">move\_uploaded\_file</span>
-   `$_FILES`
-   关于用法的简单例子
    <a href="/features/file-upload.html" class="link">文件上传处理</a>

is\_writable
============

判断给定的文件名是否可写

### 说明

<span class="type">bool</span> <span
class="methodname">is\_writable</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

如果文件存在并且可写则返回 **`TRUE`**。`filename`
参数可以是一个允许进行是否可写检查的目录名。

记住 PHP 也许只能以运行 webserver 的用户名（通常为
'nobody'）来访问文件。不计入安全模式的限制。

### 参数

`filename`  
要检查的文件名称。

### 返回值

如果文件 `filename` 存在并且可写则返回 **`TRUE`**。

### 范例

**示例 \#1 <span class="function">is\_writable</span> 例子**

``` php
<?php
$filename = 'test.txt';
if (is_writable($filename)) {
    echo 'The file is writable';
} else {
    echo 'The file is not writable';
}
?>
```

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">is\_readable</span>
-   <span class="function">file\_exists</span>
-   <span class="function">fwrite</span>

is\_writeable
=============

<span class="function">is\_writable</span> 的别名

### 说明

此函数是该函数的别名：<span class="function">is\_writable</span>。

lchgrp
======

修改符号链接的所有组

### 说明

<span class="type">bool</span> <span class="methodname">lchgrp</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">mixed</span> `$group`</span> )

尝试修改符号链接 `filename` 的所有组 `group`

只有超级用户可以任意修改符号链接的所有组;其他用户可能需要有修改目标组的权限才能修改至目标所有组。

### 参数

`filename`  
符号链接路径

`group`  
所有组的名字或者编号

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 更改符号链接的所有组**

``` php
<?php
$target = 'output.php';
$link = 'output.html';
symlink($target, $link);

lchgrp($link, 8);
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

### 参见

-   <span class="function">chgrp</span>
-   <span class="function">lchown</span>
-   <span class="function">chown</span>
-   <span class="function">chmod</span>

lchown
======

修改符号链接的所有者

### 说明

<span class="type">bool</span> <span class="methodname">lchown</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">mixed</span> `$user`</span> )

尝试修改符号链接 `filename` 的 所有者 `user`

只有超级用户任意修改符号链接的所有者。

### 参数

`filename`  
文件路径。

`user`  
所有者名称或编号

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Changing the owner of a symbolic link**

``` php
<?php
$target = 'output.php';
$link = 'output.html';
symlink($target, $link);

lchown($link, 8);
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

### 参见

-   <span class="function">chown</span>
-   <span class="function">lchgrp</span>
-   <span class="function">chgrp</span>
-   <span class="function">chmod</span>

link
====

建立一个硬连接

### 说明

<span class="type">bool</span> <span class="methodname">link</span> (
<span class="methodparam"><span class="type">string</span>
`$target`</span> , <span class="methodparam"><span
class="type">string</span> `$link`</span> )

<span class="function">link</span> 建立一个硬连接。

### 参数

`target`  
要链接的目标。

`link`  
链接的名称。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

> **Note**: <span class="simpara"> Windows下：该功能需要以 elevated
> 模式运行，或者关闭 UAC。 </span>

### 更新日志

| 版本  | 说明                                                                |
|-------|---------------------------------------------------------------------|
| 5.3.0 | 该功能在 Windows 平台下开始有效（Vista、 Server 2008 或更高版本）。 |

### 范例

**示例 \#1 Creating a simple hard link**

``` php
<?php
$target = 'source.ext'; // This is the file that already exists
$link = 'newfile.ext'; // This the filename that you want to link it to

link($target, $link);
?>
```

### 注释

> **Note**: <span
> class="simpara">此函数不能作用于<a href="/features/remote-files.html" class="link">远程文件</a>，被检查的文件必须是可通过服务器的文件系统访问的。</span>

### 参见

-   <span class="function">symlink</span>
-   <span class="function">readlink</span>
-   <span class="function">linkinfo</span>

linkinfo
========

获取一个连接的信息

### 说明

<span class="type">int</span> <span class="methodname">linkinfo</span> (
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

获取一个连接的信息。

本函数用来验证一个连接（由 `path` 所指向的）是否确实存在（使用 `stat.h`
中的 S\_ISLNK 宏同样的方法）。

### 参数

`path`  
连接的路径。

### 返回值

<span class="function">linkinfo</span> 返回 *lstat* 系统调用所返回的
UNIX C stat 结构中的 *st\_dev* 字段。 如果出错则返回 0 或 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                      |
|-------|-----------------------------------------------------------|
| 5.3.0 | Windows 平台上开始可用（Vista、Server 2008 或更高版本）。 |

### 范例

**示例 \#1 <span class="function">linkinfo</span> 例子**

``` php
<?php

echo linkinfo('/vmlinuz'); // 835

?>
```

### 参见

-   <span class="function">symlink</span>
-   <span class="function">link</span>
-   <span class="function">readlink</span>

lstat
=====

给出一个文件或符号连接的信息

### 说明

<span class="type">array</span> <span class="methodname">lstat</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

获取由 `filename` 指定的文件或符号连接的统计信息。

### 参数

`filename`  
文件或符号连接的路径。

### 返回值

有关 <span class="function">lstat</span> 返回的数组结构见手册中 <span
class="function">stat</span> 函数的页面。 本函数和 <span
class="function">stat</span> 函数相同，只除了如果 `filename`
参数是符号连接的话，则该符号连接的状态被返回，而不是该符号连接所指向的文件的状态。

### 范例

**示例 \#1 <span class="function">stat</span> 和 <span
class="function">lstat</span> 的对照**

``` php
<?php
symlink('uploads.php', 'uploads');

// Contrast information for uploads.php and uploads
array_diff(stat('uploads'), lstat('uploads'));
?>
```

以上例程的输出类似于：

Information that differs between the two files.

    Array
    (
        [ino] => 97236376
        [mode] => 33188
        [size] => 34
        [atime] => 1223580003
        [mtime] => 1223581848
        [ctime] => 1223581848
        [blocks] => 8
    )

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 注释

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">stat</span>

mkdir
=====

新建目录

### 说明

<span class="type">bool</span> <span class="methodname">mkdir</span> (
<span class="methodparam"><span class="type">string</span>
`$pathname`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
0777</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$recursive`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \]\]\] )

尝试新建一个由 pathname 指定的目录。

### 参数

`pathname`  
目录的路径。

`mode`  
默认的 mode 是 0777，意味着最大可能的访问权。有关 mode 的更多信息请阅读
<span class="function">chmod</span> 页面。

> **Note**:
>
> `mode` 在 Windows 下被忽略。

注意也许想用八进制数指定模式，也就是说该数应以零打头。模式也会被当前的
umask 修改，可以用 <span class="function">umask</span> 来改变。

`recursive`  
允许递归创建由 `pathname` 所指定的多级嵌套目录。

`context`  
> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">mkdir</span> 例子**

``` php
<?php
mkdir("/path/to/my/dir", 0700);
?>
```

**示例 \#2 通过 `recursive` 参数使用 <span
class="function">mkdir</span>**

``` php
<?php
// Desired folder structure
$structure = './depth1/depth2/depth3/';

// To create the nested structure, the $recursive parameter 
// to mkdir() must be specified.

if (!mkdir($structure, 0777, true)) {
    die('Failed to create folders...');
}

// ...
?>
```

### 错误／异常

目录已存在时，产生 **`E_WARNING`**错误。

如果因为权限问题无法创建目录，导致 **`E_WARNING`**错误。

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">rmdir</span>

move\_uploaded\_file
====================

将上传的文件移动到新位置

### 说明

<span class="type">bool</span> <span
class="methodname">move\_uploaded\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$destination`</span> )

本函数检查并确保由 `filename` 指定的文件是合法的上传文件（即通过 PHP 的
HTTP POST 上传机制所上传的）。如果文件合法，则将其移动为由 `destination`
指定的文件。

这种检查显得格外重要，如果上传的文件有可能会造成对用户或本系统的其他用户显示其内容的话。

### 参数

`filename`  
上传的文件的文件名。

`destination`  
移动文件到这个位置。

### 返回值

成功时返回 **`TRUE`**。

如果 `filename` 不是合法的上传文件，不会出现任何操作，<span
class="function">move\_uploaded\_file</span> 将返回 **`FALSE`**。

如果 `filename`
是合法的上传文件，但出于某些原因无法移动，不会出现任何操作，<span
class="function">move\_uploaded\_file</span> 将返回
**`FALSE`**。此外还会发出一条警告。

### 范例

**示例 \#1 Uploading multiple files**

``` php
<?php
$uploads_dir = '/uploads';
foreach ($_FILES["pictures"]["error"] as $key => $error) {
    if ($error == UPLOAD_ERR_OK) {
        $tmp_name = $_FILES["pictures"]["tmp_name"][$key];
        $name = $_FILES["pictures"]["name"][$key];
        move_uploaded_file($tmp_name, "$uploads_dir/$name");
    }
}
?>
```

### 注释

> **Note**:
>
> <span class="function">move\_uploaded\_file</span> 对
> <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
> 是敏感的。不过，限制只针对 `destination`
> 路径，因为允许移动上传的文件名 `filename`
> 可能会与这些限制产生冲突。<span
> class="function">move\_uploaded\_file</span> 仅作用于通过 PHP
> 上传的文件以确保这个操作的安全性。

**Warning**

如果目标文件已经存在，将会被覆盖。

### 参见

-   <span class="function">is\_uploaded\_file</span>
-   <span class="function">rename</span>
-   参见<a href="/features/file-upload.html" class="link">文件上传处理</a>一章中的简单使用例子。

parse\_ini\_file
================

解析一个配置文件

### 说明

<span class="type">array</span> <span
class="methodname">parse\_ini\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$process_sections`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">int</span>
`$scanner_mode`<span class="initializer"> =
INI\_SCANNER\_NORMAL</span></span> \]\] )

<span class="function">parse\_ini\_file</span> 载入一个由 `filename`
指定的 ini 文件，并将其中的设置作为一个联合数组返回。

ini 文件的结构和 `php.ini` 的相似。

### 参数

`filename`  
要解析的 ini 文件的文件名。

`process_sections`  
如果将最后的 `process_sections` 参数设为
**`TRUE`**，将得到一个多维数组，包括了配置文件中每一节的名称和设置。`process_sections`
的默认值是 **`FALSE`**。

`scanner_mode`  
Can either be **`INI_SCANNER_NORMAL`** (default) or
**`INI_SCANNER_RAW`**. If **`INI_SCANNER_RAW`** is supplied, then option
values will not be parsed.

### 返回值

成功时以关联数组 <span class="type">array</span> 返回设置，失败时返回
**`FALSE`**。

### 范例

**示例 \#1 `sample.ini` 的内容**

    ; This is a sample configuration file
    ; Comments start with ';', as in php.ini

    [first_section]
    one = 1
    five = 5
    animal = BIRD

    [second_section]
    path = "/usr/local/bin"
    URL = "http://www.example.com/~username"

    [third_section]
    phpversion[] = "5.0"
    phpversion[] = "5.1"
    phpversion[] = "5.2"
    phpversion[] = "5.3"

**示例 \#2 <span class="function">parse\_ini\_file</span> 例子**

<a href="/language/constants.html" class="link">常量</a>也可以在 ini
文件中被解析，因此如果在运行 <span
class="function">parse\_ini\_file</span> 之前定义了常量作为 ini
的值，将会被集成到结果中去。只有 ini 的值会被求值。例如：

``` php
<?php

define('BIRD', 'Dodo bird');

// Parse without sections
$ini_array = parse_ini_file("sample.ini");
print_r($ini_array);

// Parse with sections
$ini_array = parse_ini_file("sample.ini", true);
print_r($ini_array);

?>
```

以上例程的输出类似于：

    Array
    (
        [one] => 1
        [five] => 5
        [animal] => Dodo bird
        [path] => /usr/local/bin
        [URL] => http://www.example.com/~username
        [phpversion] => Array
            (
                [0] => 5.0
                [1] => 5.1
                [2] => 5.2
                [3] => 5.3
            )

    )
    Array
    (
        [first_section] => Array
            (
                [one] => 1
                [five] => 5
                [animal] => Dodo bird
            )

        [second_section] => Array
            (
                [path] => /usr/local/bin
                [URL] => http://www.example.com/~username
            )

        [third_section] => Array
            (
                [phpversion] => Array
                    (
                        [0] => 5.0
                        [1] => 5.1
                        [2] => 5.2
                        [3] => 5.3
                    )

            )

    )

**示例 \#3 <span class="function">parse\_ini\_file</span> parsing a
php.ini file**

``` php
<?php
// A simple function used for comparing the results below
function yesno($expression)
{
    return($expression ? 'Yes' : 'No');
}

// Get the path to php.ini using the php_ini_loaded_file() 
// function available as of PHP 5.2.4
$ini_path = php_ini_loaded_file();

// Parse php.ini
$ini = parse_ini_file($ini_path);

// Print and compare the values, note that using get_cfg_var()
// will give the same results for parsed and loaded here
echo '(parsed) magic_quotes_gpc = ' . yesno($ini['magic_quotes_gpc']) . PHP_EOL;
echo '(loaded) magic_quotes_gpc = ' . yesno(get_cfg_var('magic_quotes_gpc')) . PHP_EOL;
?>
```

以上例程的输出类似于：

    (parsed) magic_quotes_gpc = Yes
    (loaded) magic_quotes_gpc = Yes

### 注释

> **Note**:
>
> 本函数和 `php.ini`
> 文件没有关系，该文件在运行脚本时就已经处理过了。本函数可以用来读取你自己的应用程序的配置文件。

> **Note**:
>
> 如果 ini
> 文件中的值包含任何非字母数字的字符，需要将其括在双引号中（"）。

> **Note**: <span class="simpara"> 有些保留字不能作为 ini
> 文件中的键名，包括：null，yes，no，true 和 false。值为 null，no 和
> false 等效于 ""，值为 yes 和 true 等效于 "1"。字符 *{}\|&\~!\[()"*
> 也不能用在键名的任何地方，而且这些字符在选项值中有着特殊的意义。
> </span>

### 参见

-   <span class="function">parse\_ini\_string</span>

parse\_ini\_string
==================

解析配置字符串

### 说明

<span class="type">array</span> <span
class="methodname">parse\_ini\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$ini`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$process_sections`<span class="initializer"> = false</span></span> \[,
<span class="methodparam"><span class="type">int</span>
`$scanner_mode`<span class="initializer"> =
INI\_SCANNER\_NORMAL</span></span> \]\] )

<span class="function">parse\_ini\_string</span> 返回 `ini`
字符串解析后的关联数组

ini 字符串的格式参考 `php.ini`

### 参数

`ini`  
ini 字符串内容

`process_sections`  
设置 `process_sections` 参数为
**`TRUE`**,得到一个多维数组,包含名称和设置。`process_sections` 默认为
**`FALSE`**

`scanner_mode`  
可以是 **`INI_SCANNER_NORMAL`** (默认)或 **`INI_SCANNER_RAW`** 。如果是
**`INI_SCANNER_RAW`**,那么选项值不会被解析。

As of PHP 5.6.1 can also be specified as **`INI_SCANNER_TYPED`**. In
this mode boolean, null and integer types are preserved when possible.
String values *"true"*, *"on"* and *"yes"* are converted to **`TRUE`**.
*"false"*, *"off"*, *"no"* and *"none"* are considered **`FALSE`**.
*"null"* is converted to **`NULL`** in typed mode. Also, all numeric
strings are converted to integer type if it is possible.

### 返回值

执行成功返回一个关联数组,返回 **`FALSE`** 为失败

### 注释

> **Note**: <span class="simpara"> 保留关键字不能作为 ini 的键，包括
> null, yes, no, true, false, on, off, none以及空值，off，no
> 和错误的结果集，值为 yes 和 正确的结果集。除非使用
> **`INI_SCANNER_TYPED`** 模式。 字符 *?{}\|&\~!\[()^"*
> 不能在任何地方使用作为键和有特殊意义的值。 </span>

### 参见

-   <span class="function">parse\_ini\_file</span>

pathinfo
========

返回文件路径的信息

### 说明

<span class="type">mixed</span> <span class="methodname">pathinfo</span>
( <span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`<span class="initializer"> =
PATHINFO\_DIRNAME \| PATHINFO\_BASENAME \| PATHINFO\_EXTENSION \|
PATHINFO\_FILENAME</span></span> \] )

<span class="function">pathinfo</span> 返回一个关联数组包含有 *path*
的信息。返回关联数组还是字符串取决于 `options`。

### 参数

`path`  
要解析的路径。

`options`  
如果指定了，将会返回指定元素；它们包括：**`PATHINFO_DIRNAME`**，**`PATHINFO_BASENAME`**
和 **`PATHINFO_EXTENSION`** 或 **`PATHINFO_FILENAME`**。

如果没有指定 `options` 默认是返回全部的单元。

### 返回值

如果没有传入 `options` ，将会返回包括以下单元的数组 <span
class="type">array</span>：*dirname*，*basename* 和
*extension*（如果有），以 及*filename*。

> **Note**:
>
> If the `path` does not have an extension, no *extension* element will
> be returned（以下第二个案例）。

If `options` is present, returns a <span class="type">string</span>
containing the requested element.

### 更新日志

| 版本  | 说明                                 |
|-------|--------------------------------------|
| 5.2.0 | 添加了常量 **`PATHINFO_FILENAME`**。 |

### 范例

**示例 \#1 <span class="function">pathinfo</span> 例子**

``` php
<?php
$path_parts = pathinfo('/www/htdocs/inc/lib.inc.php');

echo $path_parts['dirname'], "\n";
echo $path_parts['basename'], "\n";
echo $path_parts['extension'], "\n";
echo $path_parts['filename'], "\n"; // since PHP 5.2.0
?>
```

以上例程会输出：

    /www/htdocs/inc
    lib.inc.php
    php
    lib.inc

**示例 \#2 <span class="function">pathinfo</span> example showing
difference between null and no extension**

``` php
<?php
$path_parts = pathinfo('/path/emptyextension.');
var_dump($path_parts['extension']);

$path_parts = pathinfo('/path/noextension');
var_dump($path_parts['extension']);
?>
```

以上例程的输出类似于：

    string(0) ""

    Notice: Undefined index: extension in test.php on line 6
    NULL

### 注释

> **Note**:
>
> 有关取得当前路径信息的说明，请阅读<a href="/language/variables/predefined.html" class="link">预定义变量</a>一节。

> **Note**:
>
> <span class="function">pathinfo</span> is locale aware, so for it to
> parse a path containing multibyte characters correctly, the matching
> locale must be set using the <span class="function">setlocale</span>
> function.

### 参见

-   <span class="function">dirname</span>
-   <span class="function">basename</span>
-   <span class="function">parse\_url</span>
-   <span class="function">realpath</span>

pclose
======

关闭进程文件指针

### 说明

<span class="type">int</span> <span class="methodname">pclose</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

关闭用 <span class="function">popen</span> 打开的指向管道的文件指针。

### 参数

`handle`  
文件指针必须有效，且必须是成功调用 <span class="function">popen</span>
所返回的。

### 返回值

返回运行的进程的终止状态。发生错误时会返回 *-1*。

### 范例

**示例 \#1 <span class="function">pclose</span> 例子**

``` php
<?php
$handle = popen('/bin/ls', 'r');
pclose($handle);
?>
```

### 注释

> **Note**: **Unix Only:**  
>
> <span class="function">proc\_close</span> is internally implemented
> using the *waitpid(3)* system call. To obtain the real exit status
> code the <span class="function">pcntl\_wexitstatus</span> function
> should be used.

### 参见

-   <span class="function">popen</span>

popen
=====

打开进程文件指针

### 说明

<span class="type">resource</span> <span class="methodname">popen</span>
( <span class="methodparam"><span class="type">string</span>
`$command`</span> , <span class="methodparam"><span
class="type">string</span> `$mode`</span> )

打开一个指向进程的管道，该进程由派生给定的 command 命令执行而产生。

### 参数

`command`  
命令。

`mode`  
模式。

### 返回值

返回一个和 <span class="function">fopen</span>
所返回的相同的文件指针，只不过它是单向的（只能用于读或写）并且必须用
<span class="function">pclose</span> 来关闭。此指针可以用于 <span
class="function">fgets</span>，<span class="function">fgetss</span> 和
<span class="function">fwrite</span>。 当模式为
'r'，返回的文件指针等于命令的 STDOUT，当模式为
'w'，返回的文件指针等于命令的 STDIN。

如果出错返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">popen</span> 例子**

``` php
<?php
$handle = popen("/bin/ls", "r");
?>
```

如果未找到要执行的命令，会返回一个合法的资源。这看上去很怪，但有道理。它允许访问
shell 返回的任何错误信息：

**示例 \#2 <span class="function">popen</span> 例子**

``` php
<?php
error_reporting(E_ALL);

/* 加入重定向以得到标准错误输出 stderr。 */
$handle = popen('/path/to/executable 2>&1', 'r');
echo "'$handle'; " . gettype($handle) . "\n";
$read = fread($handle, 2096);
echo $read;
pclose($handle);
?>
```

### 注释

> **Note**:
>
> 如果需要双向支持，使用 <span class="function">proc\_open</span>。

### 参见

-   <span class="function">pclose</span>
-   <span class="function">fopen</span>
-   <span class="function">proc\_open</span>

readfile
========

输出文件

### 说明

<span class="type">int</span> <span class="methodname">readfile</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \]\] )

读取文件并写入到输出缓冲。

### 参数

`filename`  
要读取的文件名。

`use_include_path`  
想要在
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
中搜索文件，可使用这个可选的第二个参数，设为 **`TRUE`**。

`context`  
Stream 上下文（context） <span class="type">resource</span>。

### 返回值

成功时返回从文件中读入的字节数， 或者在失败时返回 **`FALSE`**

### 错误／异常

失败时抛出**`E_WARNING`**警告。

### 范例

**示例 \#1 使用 <span class="function">readfile</span> 强制下载**

``` php
<?php
$file = 'monkey.gif';

if (file_exists($file)) {
    header('Content-Description: File Transfer');
    header('Content-Type: application/octet-stream');
    header('Content-Disposition: attachment; filename="'.basename($file).'"');
    header('Expires: 0');
    header('Cache-Control: must-revalidate');
    header('Pragma: public');
    header('Content-Length: ' . filesize($file));
    readfile($file);
    exit;
}
?>
```

以上例程的输出类似于：

<img src="images/e88cefb5c3fca5060e2490b9763c4433-readfile.png" width="319" height="245" alt="打开 / 保存对话框" />

### 注释

> **Note**:
>
> <span class="function">readfile</span> 自身不会导致任何内存问题。
> 如果出现内存不足的错误，使用 <span
> class="function">ob\_get\_level</span> 确保输出缓存已经关闭。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 参见

-   <span class="function">fpassthru</span>
-   <span class="function">file</span>
-   <span class="function">fopen</span>
-   <span class="function">include</span>
-   <span class="function">require</span>
-   <span class="function">virtual</span>
-   <span class="function">file\_get\_contents</span>
-   <a href="/wrappers.html" class="xref">支持的协议和封装协议</a>

readlink
========

返回符号连接指向的目标

### 说明

<span class="type">string</span> <span
class="methodname">readlink</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> )

<span class="function">readlink</span> 和同名的 C
函数做同样的事，返回符号连接的内容。

### 参数

`path`  
链接符号的路径。

### 更新日志

| 版本  | 说明                                                           |
|-------|----------------------------------------------------------------|
| 5.3.0 | 此函数在 Windows 平台下可用（Vista、Server 2008 或更高版本）。 |

### 返回值

返回链接的路径内容，出错则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">readlink</span> 例**

``` php
<?php

// output e.g. /boot/vmlinux-2.4.20-xfs
echo readlink('/vmlinuz');

?>
```

### 参见

-   <span class="function">is\_link</span>
-   <span class="function">symlink</span>
-   <span class="function">linkinfo</span>

realpath\_cache\_get
====================

获取真实目录缓存的详情

### 说明

<span class="type">array</span> <span
class="methodname">realpath\_cache\_get</span> ( <span
class="methodparam">void</span> )

获得真实路径缓存的详情。

### 返回值

返回真实路径缓存详情的数组。键是原始路径以及值为具体信息数组，含有该解析的路径，过期时间以及其他的更多选项。

### 范例

**示例 \#1 <span class="function">realpath\_cache\_get</span> example**

``` php
<?php
var_dump(realpath_cache_get());
?>
```

以上例程的输出类似于：

    array(2) {
      ["/test"]=>
      array(4) {
        ["key"]=>
        int(123456789)
        ["is_dir"]=>
        bool(true)
        ["realpath"]=>
        string(5) "/test"
        ["expires"]=>
        int(1260318939)
      }
      ["/test/test.php"]=>
      array(4) {
        ["key"]=>
        int(987654321)
        ["is_dir"]=>
        bool(false)
        ["realpath"]=>
        string(12) "/root/test.php"
        ["expires"]=>
        int(1260318939)
      }
    }

### 参见

-   <span class="function">realpath\_cache\_size</span>

realpath\_cache\_size
=====================

获取真实路径缓冲区的大小

### 说明

<span class="type">int</span> <span
class="methodname">realpath\_cache\_size</span> ( <span
class="methodparam">void</span> )

获取真实路径缓存区大小在内存中的使用量。

### 返回值

返回真实路径缓存区使用内存的用量。

### 范例

**示例 \#1 <span class="function">realpath\_cache\_size</span> example**

``` php
<?php
var_dump(realpath_cache_size());
?>
```

以上例程的输出类似于：

    int(412)

### 参见

-   <span class="function">realpath\_cache\_get</span>
-   <a href="/ini/core.html#ini.realpath-cache-size" class="link">realpath_cache_size</a>
    方法的配置选项

realpath
========

返回规范化的绝对路径名

### 说明

<span class="type">string</span> <span
class="methodname">realpath</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> )

<span class="function">realpath</span> 扩展所有的符号连接并且处理输入的
`path` 中的 '/./', '/../' 以及多余的 '/'
并返回规范化后的绝对路径名。返回的路径中没有符号连接，'/./' 或 '/../'
成分。

### 参数

`path`  
要检查的路径。

> **Note**:
>
> Whilst a path must be supplied, the value can be blank or **`NULL`**
> In these cases, the value is interpreted as the current directory.

### 返回值

Returns the canonicalized absolute pathname on success. The resulting
path will have no symbolic link, '/./' or '/../' components.

<span class="function">realpath</span> 失败时返回
**`FALSE`**，比如说文件不存在的话。

> **Note**:
>
> The running script must have executable permissions on all directories
> in the hierarchy, otherwise <span class="function">realpath</span>
> will return **`FALSE`**.

> **Note**: <span class="simpara"> 因为 PHP
> 的整数类型是有符号整型而且很多平台使用 32 位整型，对 2GB
> 以上的文件，一些文件系统函数可能返回无法预期的结果。</span>

### 更新日志

| 版本  | 说明                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 在之前的版本中，在 \*BSD 系统上，如果仅仅是 `path` 不存在的话，<span class="function">realpath</span> 并不会像其它系统那样返回 **`FALSE`**。 |
| 5.0.0 | 在此之前的版本中，如果 `path` 传入了空或者 **`NULL`**，将导致 <span class="function">realpath</span> 返回脚本当前的目录。                    |

### 范例

**示例 \#1 <span class="function">realpath</span> 例子**

``` php
<?php
chdir('/var/www/');
echo realpath('./../../etc/passwd');
?>
```

以上例程会输出：

    /etc/passwd

**示例 \#2 Windows 上的 <span class="function">realpath</span>**

在 Windows 上，<span class="function">realpath</span> 会将 unix
风格的路径改成 Windows 风格的。

``` php
<?php
echo realpath('/windows/system32');
?>
```

以上例程会输出：

    C:\WINDOWS\System32

### 参见

-   <span class="function">basename</span>
-   <span class="function">dirname</span>
-   <span class="function">pathinfo</span>

rename
======

重命名一个文件或目录

### 说明

<span class="type">bool</span> <span class="methodname">rename</span> (
<span class="methodparam"><span class="type">string</span>
`$oldname`</span> , <span class="methodparam"><span
class="type">string</span> `$newname`</span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\] )

尝试把 `oldname` 重命名为 `newname`，必要时会在不同目录间移动。
如果重命名文件时 `newname` 已经存在，将会覆盖掉它。 如果重命名文件夹时
`newname` 已经存在，本函数将导致一个警告。

### 参数

`oldname`  
原名

> **Note**:
>
> 用于 `oldname` 中的封装协议*必须*和用于 `newname` 中的相匹配。

`newname`  
新的名字。

> **Note**: <span class="simpara"> 在 Windows 上如果 `newname`
> 已经存在，它必须被覆盖。否则 <span class="function">rename</span>
> 将失败并导致 **`E_WARNING`**。 </span>

`context`  
> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rename</span> 例子**

``` php
<?php
rename("/tmp/tmp_file.txt", "/home/user/login/docs/my_file.txt");
?>
```

### 参见

-   <span class="function">copy</span>
-   <span class="function">unlink</span>
-   <span class="function">move\_uploaded\_file</span>

rewind
======

倒回文件指针的位置

### 说明

<span class="type">bool</span> <span class="methodname">rewind</span> (
<span class="methodparam"><span class="type">resource</span>
`$handle`</span> )

将 `handle` 的文件位置指针设为文件流的开头。

> **Note**:
>
> 如果将文件以附加（"a" 或者
> "a+"）模式打开，写入文件的任何数据总是会被附加在后面，不管文件指针的位置。

### 参数

`handle`  
文件指针必须合法，并且指向由 <span class="function">fopen</span>
成功打开的文件。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rewind</span> overwriting example**

``` php
<?php
$handle = fopen('output.txt', 'r+');

fwrite($handle, 'Really long sentence.');
rewind($handle);
fwrite($handle, 'Foo');
rewind($handle);

echo fread($handle, filesize('output.txt'));

fclose($handle);
?>
```

以上例程的输出类似于：

    Foolly long sentence.

### 参见

-   <span class="function">fread</span>
-   <span class="function">fseek</span>
-   <span class="function">ftell</span>
-   <span class="function">fwrite</span>

rmdir
=====

删除目录

### 说明

<span class="type">bool</span> <span class="methodname">rmdir</span> (
<span class="methodparam"><span class="type">string</span>
`$dirname`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \] )

尝试删除 `dirname` 所指定的目录。 该目录必须是空的，而且要有相应的权限。
失败时会产生一个 **`E_WARNING`** 级别的错误。

### 参数

`dirname`  
目录的路径。

`context`  
> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rmdir</span> 例子**

``` php
<?php
if (!is_dir('examples')) {
    mkdir('examples');
}

rmdir('examples');
?>
```

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">mkdir</span>
-   <span class="function">unlink</span>

set\_file\_buffer
=================

<span class="function">stream\_set\_write\_buffer</span> 的别名

### 说明

此函数是该函数的别名：<span
class="function">stream\_set\_write\_buffer</span>。

stat
====

给出文件的信息

### 说明

<span class="type">array</span> <span class="methodname">stat</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

获取由 `filename` 指定的文件的统计信息。如果 `filename`
是符号连接，则统计信息是关于被连接文件本身的，而不是符号连接。

<span class="function">lstat</span> 和 <span
class="function">stat</span> 相同，只除了它会返回符号连接的状态。

### 参数

`filename`  
文件的路径。

### 返回值

| 数字下标 | 关联键名（自 PHP 4.0.6） | 说明                                                                     |
|----------|--------------------------|--------------------------------------------------------------------------|
| 0        | dev                      | device number - 设备名                                                   |
| 1        | ino                      | inode number - inode 号码                                                |
| 2        | mode                     | inode protection mode - inode 保护模式                                   |
| 3        | nlink                    | number of links - 被连接数目                                             |
| 4        | uid                      | userid of owner - 所有者的用户 id                                        |
| 5        | gid                      | groupid of owner- 所有者的组 id                                          |
| 6        | rdev                     | device type, if inode device \* - 设备类型，如果是 inode 设备的话        |
| 7        | size                     | size in bytes - 文件大小的字节数                                         |
| 8        | atime                    | time of last access (unix timestamp) - 上次访问时间（Unix 时间戳）       |
| 9        | mtime                    | time of last modification (unix timestamp) - 上次修改时间（Unix 时间戳） |
| 10       | ctime                    | time of last change (unix timestamp) - 上次改变时间（Unix 时间戳）       |
| 11       | blksize                  | blocksize of filesystem IO \* - 文件系统 IO 的块大小                     |
| 12       | blocks                   | number of blocks allocated - 所占据块的数目                              |

\* Windows 下总是 0。

\* - 仅在支持 st\_blksize 类型的系统下有效。其它系统（如 Windows）返回
-1。

如果出错，<span class="function">stat</span> 返回 **`FALSE`**。

> **Note**: <span class="simpara"> 因为 PHP
> 的整数类型是有符号整型而且很多平台使用 32 位整型，对 2GB
> 以上的文件，一些文件系统函数可能返回无法预期的结果。</span>

### 错误／异常

错误时会产生 **`E_WARNING`** 级别的错误。

### 更新日志

| 版本  | 说明                                                                                                                       |
|-------|----------------------------------------------------------------------------------------------------------------------------|
| 4.0.6 | 返回一个数组包含有文件的统计信息，该数组具有以下列出的单元，数组下标从零开始。除了数字索引之外自还可以通过关联索引来访问。 |

### 范例

**示例 \#1 <span class="function">stat</span> 例子**

``` php
<?php
/* Get file stat */
$stat = stat('C:\php\php.exe');

/*
 * Print file access time, this is the same 
 * as calling fileatime()
 */
echo 'Access time: ' . $stat['atime'];

/*
 * Print file modification time, this is the 
 * same as calling filemtime()
 */
echo 'Modification time: ' . $stat['mtime'];

/* Print the device number */
echo 'Device number: ' . $stat['dev'];
?>
```

**示例 \#2 Using <span class="function">stat</span> information together
with <span class="function">touch</span>**

``` php
<?php
/* Get file stat */
$stat = stat('C:\php\php.exe');

/* Did we failed to get stat information? */
if (!$stat) {
    echo 'stat() call failed...';
} else {
    /*
     * We want the access time to be 1 week 
     * after the current access time.
     */
    $atime = $stat['atime'] + 604800;

    /* Touch the file */
    if (!touch('some_file.txt', time(), $atime)) {
        echo 'Failed to touch file...';
    } else {
        echo 'touch() returned success...';
    }
}
?>
```

### 注释

> **Note**:
>
> 注意：不同文件系统对时间的判断方法可能是不相同的。

> **Note**: <span class="simpara">此函数的结果会被缓存。参见 <span
> class="function">clearstatcache</span> 以获得更多细节。</span>

**小贴士**

自 PHP 5.0.0 起, 此函数也用于*某些* URL 包装器。请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>以获得支持
<span class="function">stat</span> 系列函数功能的包装器列表。

### 参见

-   <span class="function">lstat</span>
-   <span class="function">fstat</span>
-   <span class="function">filemtime</span>
-   <span class="function">filegroup</span>

symlink
=======

建立符号连接

### 说明

<span class="type">bool</span> <span class="methodname">symlink</span> (
<span class="methodparam"><span class="type">string</span>
`$target`</span> , <span class="methodparam"><span
class="type">string</span> `$link`</span> )

<span class="function">symlink</span> 对于已有的 `target` 建立一个名为
`link` 的符号连接。

### 参数

`target`  
连接的目标。

`link`  
连接的名称。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                           |
|-------|----------------------------------------------------------------|
| 5.3.0 | 此函数在 Windows 平台上可用（Vista、Server 2008 或更高版本）。 |

### 范例

**示例 \#1 创建一个符号连接**

``` php
<?php
$target = 'uploads.php';
$link = 'uploads';
symlink($target, $link);

echo readlink($link);
?>
```

### 注释

> **Note**: <span class="simpara"> 仅针对 Windows：运行 PHP
> 于Vista、Server 2008 或更高版本才能正常使用。 之前版本的 Windows
> 不支持符号连接。 </span>

### 参见

-   <span class="function">link</span>
-   <span class="function">readlink</span>
-   <span class="function">linkinfo</span>

tempnam
=======

建立一个具有唯一文件名的文件

### 说明

<span class="type">string</span> <span class="methodname">tempnam</span>
( <span class="methodparam"><span class="type">string</span>
`$dir`</span> , <span class="methodparam"><span
class="type">string</span> `$prefix`</span> )

在指定目录中建立一个具有唯一文件名的文件。如果该目录不存在，<span
class="function">tempnam</span>
会在系统临时目录中生成一个文件，并返回其文件名。

### 参数

`dir`  
The directory where the temporary filename will be created.

`prefix`  
产生临时文件的前缀。

> **Note**: <span class="simpara"> Windows uses only the first three
> characters of prefix. </span>

### 返回值

返回新的临时文件名，出错返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                       |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.0.6 | 在 PHP 4.0.6 之前，<span class="function">tempnam</span> 函数的行为取决于系统。在 Windows 下 `TMP` 环境变量会越过 `dir` 参数，在 Linux 下 `TMPDIR` 环境变量优先，而在 SVR4 下总是使用 `dir` 参数，如果其指向的目录存在的话。如果有疑问请参考系统文档中的 tempnam(3) 函数。 |
| 4.0.3 | 本函数的行为在 4.0.3 版中改变了。也会建立一个临时文件以避免竞争情形，即有可能会在产生出作为文件名的字符串与脚本真正建立该文件之间会在文件系统中存在同名文件。注意，如果不再需要该文件则要删除此文件，不会自动删除的。                                                      |

### 范例

**示例 \#1 <span class="function">tempnam</span> 例子**

``` php
<?php
$tmpfname = tempnam("/tmp", "FOO");

$handle = fopen($tmpfname, "w");
fwrite($handle, "writing to tempfile");
fclose($handle);

// do here something

unlink($tmpfname);
?>
```

### 注释

> **Note**: <span class="simpara"> 如果 PHP 不能在指定的 `dir`
> 参数中创建文件，则退回到系统默认值。 在 NTFS
> 文件系统中，同样的情况也发生在 `dir` 中文件数超过 65534 个的时候。
> </span>

### 参见

-   <span class="function">tmpfile</span>
-   <span class="function">sys\_get\_temp\_dir</span>
-   <span class="function">unlink</span>

tmpfile
=======

建立一个临时文件

### 说明

<span class="type">resource</span> <span
class="methodname">tmpfile</span> ( <span
class="methodparam">void</span> )

以读写（w+）模式建立一个具有唯一文件名的临时文件，返回一个文件句柄。

文件会在关闭后（用 <span
class="function">fclose</span>）自动被删除，或当脚本结束后。

详细信息请参考系统手册中的 *tmpfile(3)* 函数，以及 `stdio.h` 头文件。

### 返回值

返回一个与 <span class="function">fopen</span>
所打开返回类似的新文件句柄， 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">tmpfile</span> 例子**

``` php
<?php
$temp = tmpfile();
fwrite($temp, "writing to tempfile");
fseek($temp, 0);
echo fread($temp, 1024);
fclose($temp); // this removes the file
?>
```

以上例程会输出：

    writing to tempfile

### 参见

-   <span class="function">tempnam</span>
-   <span class="function">sys\_get\_temp\_dir</span>

touch
=====

设定文件的访问和修改时间

### 说明

<span class="type">bool</span> <span class="methodname">touch</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">int</span> `$time`<span class="initializer"> =
time()</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$atime`</span> \]\] )

尝试将由 `filename` 给出的文件的访问和修改时间设定为给出的 `time`。
注意访问时间总是会被修改的，不论有几个参数。

如果文件不存在，则会被创建。

### 参数

`filename`  
要设定的文件名。

`time`  
要设定的时间。如果没有提供参数 `time` 则会使用当前系统的时间。

`atime`  
如果给出了这个参数，则给定文件的访问时间会被设为 `atime`，否则会设置
为`time`。如果没有给出这两个参数，则使用当前系统时间。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">touch</span> 例子**

``` php
<?php
if (touch($filename)) {
    echo $filename . ' modification time has been changed to present time';
} else {
    echo 'Sorry, could not change modification time of ' . $filename;
}
?>
```

**示例 \#2 使用 `time` 参数的 <span class="function">touch</span>**

``` php
<?php
// This is the touch time, we'll set it to one hour in the past.
$time = time() - 3600;

// Touch the file
if (!touch('some_file.txt', $time)) {
    echo 'Whoops, something went wrong...';
} else {
    echo 'Touched file with success';
}
?>
```

### 注释

> **Note**:
>
> 注意：不同文件系统对时间的判断方法可能是不相同的。

**Warning**

在 PHP 5.3.0 之前无法修改 Windows 下目录的最后修改时间。

umask
=====

改变当前的 umask

### 说明

<span class="type">int</span> <span class="methodname">umask</span> (\[
<span class="methodparam"><span class="type">int</span> `$mask`</span>
\] )

<span class="function">umask</span> 将 PHP 的 umask 设定为 `mask` & 0777
并返回原来的 umask。当 PHP 被作为服务器模块使用时，在每个请求结束后
umask 会被恢复。

### 参数

`mask`  
The new umask.

### 返回值

无参数调用 <span class="function">umask</span> 会返回当前的
umask，有参数则返回原来的 umask。

### 范例

**示例 \#1 <span class="function">umask</span> 例子**

``` php
<?php
$old = umask(0);
chmod("/path/some_dir/some_file.txt", 0755);
umask($old);

// Checking
if ($old != umask()) {
    die('An error occured while changing back the umask');
}
?>
```

### 注释

> **Note**:
>
> 在多线程的服务器上尽量避免使用这个函数。创建文件后要改变其权限最好还是使用
> <span class="function">chmod</span>。使用 <span
> class="function">umask</span>
> 会导致并发程序和服务器发生不可预知的情况，因为它们是使用相同的 umask
> 的。

unlink
======

删除文件

### 说明

<span class="type">bool</span> <span class="methodname">unlink</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \] )

删除 `filename`。和 Unix C 的 unlink() 函数相似。 发生错误时会产生一个
**`E_WARNING`** 级别的错误。

### 参数

`filename`  
文件的路径。

`context`  
> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                         |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.3.0 | 现在 Windows 也可以用 <span class="function">unlink</span> 删除文件句柄还在使用中的文件了，在此之前是无法删除的。 然而，还是无法重新创建文件，需要等到所有句柄都关闭才可以。 |

### 范例

**示例 \#1 基本的 <span class="function">unlink</span> 用法**

``` php
<?php
$fh = fopen('test.html', 'a');
fwrite($fh, '<h1>Hello world!</h1>');
fclose($fh);

unlink('test.html');
?>
```

### 参见

-   <span class="function">rmdir</span>

**目录**

-   [basename](/ref/filesystem.html#basename) — 返回路径中的文件名部分
-   [chgrp](/ref/filesystem.html#chgrp) — 改变文件所属的组
-   [chmod](/ref/filesystem.html#chmod) — 改变文件模式
-   [chown](/ref/filesystem.html#chown) — 改变文件的所有者
-   [clearstatcache](/ref/filesystem.html#clearstatcache) —
    清除文件状态缓存
-   [copy](/ref/filesystem.html#copy) — 拷贝文件
-   [delete](/ref/filesystem.html#delete) — 参见 unlink 或 unset
-   [dirname](/ref/filesystem.html#dirname) — 返回路径中的目录部分
-   [disk\_free\_space](/ref/filesystem.html#disk_free_space) —
    返回目录中的可用空间
-   [disk\_total\_space](/ref/filesystem.html#disk_total_space) —
    返回一个目录的磁盘总大小
-   [diskfreespace](/ref/filesystem.html#diskfreespace) —
    disk\_free\_space 的别名
-   [fclose](/ref/filesystem.html#fclose) — 关闭一个已打开的文件指针
-   [feof](/ref/filesystem.html#feof) —
    测试文件指针是否到了文件结束的位置
-   [fflush](/ref/filesystem.html#fflush) — 将缓冲内容输出到文件
-   [fgetc](/ref/filesystem.html#fgetc) — 从文件指针中读取字符
-   [fgetcsv](/ref/filesystem.html#fgetcsv) — 从文件指针中读入一行并解析
    CSV 字段
-   [fgets](/ref/filesystem.html#fgets) — 从文件指针中读取一行
-   [fgetss](/ref/filesystem.html#fgetss) — 从文件指针中读取一行并过滤掉
    HTML 标记
-   [file\_exists](/ref/filesystem.html#file_exists) —
    检查文件或目录是否存在
-   [file\_get\_contents](/ref/filesystem.html#file_get_contents) —
    将整个文件读入一个字符串
-   [file\_put\_contents](/ref/filesystem.html#file_put_contents) —
    将一个字符串写入文件
-   [file](/ref/filesystem.html#file) — 把整个文件读入一个数组中
-   [fileatime](/ref/filesystem.html#fileatime) — 取得文件的上次访问时间
-   [filectime](/ref/filesystem.html#filectime) — 取得文件的 inode
    修改时间
-   [filegroup](/ref/filesystem.html#filegroup) — 取得文件的组
-   [fileinode](/ref/filesystem.html#fileinode) — 取得文件的 inode
-   [filemtime](/ref/filesystem.html#filemtime) — 取得文件修改时间
-   [fileowner](/ref/filesystem.html#fileowner) — 取得文件的所有者
-   [fileperms](/ref/filesystem.html#fileperms) — 取得文件的权限
-   [filesize](/ref/filesystem.html#filesize) — 取得文件大小
-   [filetype](/ref/filesystem.html#filetype) — 取得文件类型
-   [flock](/ref/filesystem.html#flock) — 轻便的咨询文件锁定
-   [fnmatch](/ref/filesystem.html#fnmatch) — 用模式匹配文件名
-   [fopen](/ref/filesystem.html#fopen) — 打开文件或者 URL
-   [fpassthru](/ref/filesystem.html#fpassthru) —
    输出文件指针处的所有剩余数据
-   [fputcsv](/ref/filesystem.html#fputcsv) — 将行格式化为 CSV
    并写入文件指针
-   [fputs](/ref/filesystem.html#fputs) — fwrite 的别名
-   [fread](/ref/filesystem.html#fread) —
    读取文件（可安全用于二进制文件）
-   [fscanf](/ref/filesystem.html#fscanf) — 从文件中格式化输入
-   [fseek](/ref/filesystem.html#fseek) — 在文件指针中定位
-   [fstat](/ref/filesystem.html#fstat) —
    通过已打开的文件指针取得文件信息
-   [ftell](/ref/filesystem.html#ftell) — 返回文件指针读/写的位置
-   [ftruncate](/ref/filesystem.html#ftruncate) — 将文件截断到给定的长度
-   [fwrite](/ref/filesystem.html#fwrite) —
    写入文件（可安全用于二进制文件）
-   [glob](/ref/filesystem.html#glob) — 寻找与模式匹配的文件路径
-   [is\_dir](/ref/filesystem.html#is_dir) —
    判断给定文件名是否是一个目录
-   [is\_executable](/ref/filesystem.html#is_executable) —
    判断给定文件名是否可执行
-   [is\_file](/ref/filesystem.html#is_file) —
    判断给定文件名是否为一个正常的文件
-   [is\_link](/ref/filesystem.html#is_link) —
    判断给定文件名是否为一个符号连接
-   [is\_readable](/ref/filesystem.html#is_readable) —
    判断给定文件名是否可读
-   [is\_uploaded\_file](/ref/filesystem.html#is_uploaded_file) —
    判断文件是否是通过 HTTP POST 上传的
-   [is\_writable](/ref/filesystem.html#is_writable) —
    判断给定的文件名是否可写
-   [is\_writeable](/ref/filesystem.html#is_writeable) — is\_writable
    的别名
-   [lchgrp](/ref/filesystem.html#lchgrp) — 修改符号链接的所有组
-   [lchown](/ref/filesystem.html#lchown) — 修改符号链接的所有者
-   [link](/ref/filesystem.html#link) — 建立一个硬连接
-   [linkinfo](/ref/filesystem.html#linkinfo) — 获取一个连接的信息
-   [lstat](/ref/filesystem.html#lstat) — 给出一个文件或符号连接的信息
-   [mkdir](/ref/filesystem.html#mkdir) — 新建目录
-   [move\_uploaded\_file](/ref/filesystem.html#move_uploaded_file) —
    将上传的文件移动到新位置
-   [parse\_ini\_file](/ref/filesystem.html#parse_ini_file) —
    解析一个配置文件
-   [parse\_ini\_string](/ref/filesystem.html#parse_ini_string) —
    解析配置字符串
-   [pathinfo](/ref/filesystem.html#pathinfo) — 返回文件路径的信息
-   [pclose](/ref/filesystem.html#pclose) — 关闭进程文件指针
-   [popen](/ref/filesystem.html#popen) — 打开进程文件指针
-   [readfile](/ref/filesystem.html#readfile) — 输出文件
-   [readlink](/ref/filesystem.html#readlink) — 返回符号连接指向的目标
-   [realpath\_cache\_get](/ref/filesystem.html#realpath_cache_get) —
    获取真实目录缓存的详情
-   [realpath\_cache\_size](/ref/filesystem.html#realpath_cache_size) —
    获取真实路径缓冲区的大小
-   [realpath](/ref/filesystem.html#realpath) — 返回规范化的绝对路径名
-   [rename](/ref/filesystem.html#rename) — 重命名一个文件或目录
-   [rewind](/ref/filesystem.html#rewind) — 倒回文件指针的位置
-   [rmdir](/ref/filesystem.html#rmdir) — 删除目录
-   [set\_file\_buffer](/ref/filesystem.html#set_file_buffer) —
    stream\_set\_write\_buffer 的别名
-   [stat](/ref/filesystem.html#stat) — 给出文件的信息
-   [symlink](/ref/filesystem.html#symlink) — 建立符号连接
-   [tempnam](/ref/filesystem.html#tempnam) —
    建立一个具有唯一文件名的文件
-   [tmpfile](/ref/filesystem.html#tmpfile) — 建立一个临时文件
-   [touch](/ref/filesystem.html#touch) — 设定文件的访问和修改时间
-   [umask](/ref/filesystem.html#umask) — 改变当前的 umask
-   [unlink](/ref/filesystem.html#unlink) — 删除文件
