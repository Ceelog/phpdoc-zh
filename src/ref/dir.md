相关函数，例如：<span class="function">dirname</span>、 <span
class="function">is\_dir</span>、 <span class="function">mkdir</span> 和
<span class="function">rmdir</span>，
请查看<a href="/ref/filesystem.html" class="link">文件系统</a>章节。

chdir
=====

改变目录

### 说明

<span class="type">bool</span> <span class="methodname">chdir</span> (
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

将 PHP 的当前目录改为 `directory`。

### 参数

`directory`  
新的当前目录

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws an error of level **`E_WARNING`** on failure.

### 范例

**示例 \#1 <span class="function">chdir</span> 例子**

``` php
<?php

// current directory
echo getcwd() . "\n";

chdir('public_html');

// current directory
echo getcwd() . "\n";

?>
```

以上例程的输出类似于：

    /home/vincent
    /home/vincent/public_html

### 注释

**Caution**

If the PHP interpreter has been built with ZTS (Zend Thread Safety)
enabled, any changes to the current directory made through <span
class="function">chdir</span> will be invisible to the operating system.
All built-in PHP functions will still respect the change in current
directory; but external library functions called using
<a href="/book/ffi.html" class="link">FFI</a> will not. You can tell
whether your copy of PHP was built with ZTS enabled using **php -i** or
the built-in constant **`PHP_ZTS`**.

### 参见

-   <span class="function">getcwd</span>

chroot
======

改变根目录

### 说明

<span class="type">bool</span> <span class="methodname">chroot</span> (
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

将当前进程的根目录改变为 `directory`。

本函数仅在系统支持且运行于 CLI，CGI 或嵌入 SAPI
版本时才能正确工作。此外本函数还需要 root 权限。

### 参数

`directory`  
新目录

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">chroot</span> example**

``` php
<?php
chroot("/path/to/your/chroot/");
echo getcwd();
?>
```

以上例程会输出：

    /

### 注释

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

closedir
========

关闭目录句柄

### 说明

<span class="type">void</span> <span class="methodname">closedir</span>
(\[ <span class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

关闭由 `dir_handle` 指定的目录流。流必须之前被 <span
class="function">opendir</span> 所打开。

### 参数

`dir_handle`  
目录句柄的 <span class="type">resource</span>，之前由 <span
class="function">opendir</span>
所打开的。如果目录句柄没有指定，那么会假定为是<span
class="function">opendir</span>所打开的最后一个句柄。

### 范例

**示例 \#1 <span class="function">closedir</span> 例子**

``` php
<?php
$dir = "/etc/php5/";

// Open a known directory, read directory into variable and then close
if (is_dir($dir)) {
    if ($dh = opendir($dir)) {
        $directory = readdir($dh);
        closedir($dh);
    }
}
?>
```

dir
===

返回一个 Directory 类实例

### 说明

<span class="type">Directory</span> <span class="methodname">dir</span>
( <span class="methodparam"><span class="type">string</span>
`$directory`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`</span> \] )

以面向对象的方式访问目录。打开 `directory` 参数指定的目录。

### 参数

`directory`  
被打开的目录

`context`  
> **Note**: <span class="simpara">在 PHP 5.0.0
> 中增加了对上下文（Context）的支持。有关*上下文（Context）*的说明参见
> <a href="/book/stream.html" class="xref">Streams</a>。</span>

### 返回值

成功的话，返回一个 <span class="classname">Directory</span> 类实例,
参数错误的情况下返回 **`null`** ， 其它错误情况返回 **`false`** 。

### 范例

**示例 \#1 <span class="function">dir</span> 示例**

请特别注意下面示例中 <span class="function">Directory::read</span>
函数返回值的判断方式。 我们严格测试（值相等，并且类型相同，请参考
<a href="/language/operators/comparison.html" class="link">比较运算符</a>
）返回值等于 **`false`** ，因为有些情况下，目录名可能"等于" **`false`**
，导致 跳出循环。

``` php
<?php
$d = dir("/etc/php5");
echo "Handle: " . $d->handle . "\n";
echo "Path: " . $d->path . "\n";
while (false !== ($entry = $d->read())) {
   echo $entry."\n";
}
$d->close();
?>
```

以上例程的输出类似于：

    Handle: Resource id #2
    Path: /etc/php5
    .
    ..
    apache
    cgi
    cli

### 注释

> **Note**:
>
> 目录条目返回的顺序依赖于系统。

getcwd
======

取得当前工作目录

### 说明

<span class="type">string</span> <span class="methodname">getcwd</span>
( <span class="methodparam">void</span> )

取得当前工作目录。

### 返回值

成功则返回当前工作目录，失败返回 **`false`**。

在某些 Unix
的变种下，如果任何父目录没有设定可读或搜索模式，即使当前目录设定了，<span
class="function">getcwd</span> 还是会返回
**`false`**。有关模式与权限的更多信息见 <span
class="function">chmod</span>。

### 范例

**示例 \#1 <span class="function">getcwd</span> 例子**

``` php
<?php

// current directory
echo getcwd() . "\n";

chdir('cvs');

// current directory
echo getcwd() . "\n";

?>
```

以上例程的输出类似于：

    /home/didou
    /home/didou/cvs

### 参见

-   <span class="function">chdir</span>
-   <span class="function">chmod</span>

opendir
=======

打开目录句柄

### 说明

<span class="type">resource</span> <span
class="methodname">opendir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\] )

打开一个目录句柄，可用于之后的 <span
class="function">closedir</span>，<span class="function">readdir</span>
和 <span class="function">rewinddir</span> 调用中。

### 参数

`path`  
要打开的目录路径

`context`  
`context` 参数的说明见手册中的
<a href="/ref/stream.html" class="link">Streams API</a> 一章。

### 返回值

如果成功则返回目录句柄的 <span class="type">resource</span>，失败则返回
**`false`**。

如果 `path`
不是一个合法的目录或者因为权限限制或文件系统错误而不能打开目录，<span
class="function">opendir</span> 返回 **`false`** 并产生一个
<a href="/errorfunc/constants.html" class="link">E_WARNING</a> 级别的
PHP 错误信息。可以在 <span class="function">opendir</span>
前面加上“<a href="/language/operators/errorcontrol.html" class="link">@</a>”符号来抑制错误信息的输出。

### 更新日志

| 版本  | 说明                                                                                      |
|-------|-------------------------------------------------------------------------------------------|
| 5.0.0 | `path` 支持 *ftp://* URL wrapper                                                          |
| 4.3.0 | `path` 可以是任何支持目录列表的 URL，不过在 PHP 4 中只有 *file://* URL wrapper 支持此功能 |

### 范例

**示例 \#1 <span class="function">opendir</span> 例子**

``` php
<?php
$dir = "/etc/php5/";

// Open a known directory, and proceed to read its contents
if (is_dir($dir)) {
    if ($dh = opendir($dir)) {
        while (($file = readdir($dh)) !== false) {
            echo "filename: $file : filetype: " . filetype($dir . $file) . "\n";
        }
        closedir($dh);
    }
}
?>
```

以上例程的输出类似于：

    filename: . : filetype: dir
    filename: .. : filetype: dir
    filename: apache : filetype: dir
    filename: cgi : filetype: dir
    filename: cli : filetype: dir

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">readdir</span>
-   <span class="function">dir</span>

readdir
=======

从目录句柄中读取条目

### 说明

<span class="type">string</span> <span class="methodname">readdir</span>
(\[ <span class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

返回目录中下一个文件的文件名。文件名以在文件系统中的排序返回。

### 参数

`dir_handle`  
目录句柄的 <span class="type">resource</span>，之前由 <span
class="function">opendir</span> 打开

### 返回值

成功则返回文件名 或者在失败时返回 **`false`**

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 范例

**示例 \#1 列出目录中的所有文件**

请留意下面例子中检查 <span class="function">readdir</span>
返回值的风格。这里明确地测试返回值是否全等于（值和类型都相同——更多信息参见<a href="/language/operators/comparison.html" class="link">比较运算符</a>）**`false`**，否则任何目录项的名称求值为
**`false`** 的都会导致循环停止（例如一个目录名为“0”）。

``` php
<?php
// 注意在 4.0.0-RC2 之前不存在 !== 运算符

if ($handle = opendir('/path/to/files')) {
    echo "Directory handle: $handle\n";
    echo "Files:\n";

    /* 这是正确地遍历目录方法 */
    while (false !== ($file = readdir($handle))) {
        echo "$file\n";
    }

    /* 这是错误地遍历目录的方法 */
    while ($file = readdir($handle)) {
        echo "$file\n";
    }

    closedir($handle);
}
?>
```

**示例 \#2 列出当前目录的所有文件并去掉 *.* 和 *..***

``` php
<?php
if ($handle = opendir('.')) {
    while (false !== ($file = readdir($handle))) {
        if ($file != "." && $file != "..") {
            echo "$file\n";
        }
    }
    closedir($handle);
}
?>
```

### 参见

-   <span class="function">is\_dir</span>
-   <span class="function">glob</span>
-   <span class="function">opendir</span>
-   <span class="function">scandir</span>

rewinddir
=========

倒回目录句柄

### 说明

<span class="type">void</span> <span class="methodname">rewinddir</span>
( <span class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> )

将 `dir_handle` 指定的目录流重置到目录的开头。

### 参数

`dir_handle`  
目录句柄的 <span class="type">resource</span>，之前由 <span
class="function">opendir</span> 打开

scandir
=======

列出指定路径中的文件和目录

### 说明

<span class="type">array</span> <span class="methodname">scandir</span>
( <span class="methodparam"><span class="type">string</span>
`$directory`</span> \[, <span class="methodparam"><span
class="type">int</span> `$sorting_order`</span> \[, <span
class="methodparam"><span class="type">resource</span> `$context`</span>
\]\] )

返回一个 <span class="type">array</span>，包含有 `directory`
中的文件和目录。

### 参数

`directory`  
要被浏览的目录

`sorting_order`  
默认的排序顺序是按字母升序排列。如果使用了可选参数 `sorting_order`（设为
1），则排序顺序是按字母降序排列。

`context`  
`context` 参数的说明见手册中的
<a href="/ref/stream.html" class="link">Streams API</a> 一章。

### 返回值

成功则返回包含有文件名的 <span class="type">array</span>，如果失败则返回
**`false`**。如果 `directory` 不是个目录，则返回布尔值 **`false`**
并生成一条 **`E_WARNING`** 级的错误。

### 更新日志

| 版本  | 说明                                                                                                   |
|-------|--------------------------------------------------------------------------------------------------------|
| 5.4.0 | `sorting_order` now accepts constants. Any nonzero value caused descending order in previous versions. |

### 范例

**示例 \#1 一个简单的 <span class="function">scandir</span> 例子**

``` php
<?php
$dir    = '/tmp';
$files1 = scandir($dir);
$files2 = scandir($dir, 1);

print_r($files1);
print_r($files2);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => .
        [1] => ..
        [2] => bar.php
        [3] => foo.txt
        [4] => somedir
    )
    Array
    (
        [0] => somedir
        [1] => foo.txt
        [2] => bar.php
        [3] => ..
        [4] => .
    )

**示例 \#2 <span class="function">scandir</span> 在 PHP 4 中的实现**

``` php
<?php
$dir = "/tmp";
$dh  = opendir($dir);
while (false !== ($filename = readdir($dh))) {
    $files[] = $filename;
}

sort($files);

print_r($files);

rsort($files);

print_r($files);

?>
```

以上例程的输出类似于：

    Array
    (
        [0] => .
        [1] => ..
        [2] => bar.php
        [3] => foo.txt
        [4] => somedir
    )
    Array
    (
        [0] => somedir
        [1] => foo.txt
        [2] => bar.php
        [3] => ..
        [4] => .
    )

### 注释

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参见

-   <span class="function">opendir</span>
-   <span class="function">readdir</span>
-   <span class="function">glob</span>
-   <span class="function">is\_dir</span>
-   <span class="function">sort</span>

**目录**

-   [chdir](/ref/dir.html#chdir) — 改变目录
-   [chroot](/ref/dir.html#chroot) — 改变根目录
-   [closedir](/ref/dir.html#closedir) — 关闭目录句柄
-   [dir](/ref/dir.html#dir) — 返回一个 Directory 类实例
-   [getcwd](/ref/dir.html#getcwd) — 取得当前工作目录
-   [opendir](/ref/dir.html#opendir) — 打开目录句柄
-   [readdir](/ref/dir.html#readdir) — 从目录句柄中读取条目
-   [rewinddir](/ref/dir.html#rewinddir) — 倒回目录句柄
-   [scandir](/ref/dir.html#scandir) — 列出指定路径中的文件和目录
