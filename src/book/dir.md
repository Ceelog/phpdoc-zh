目录
====

**目录**

-   [安装／配置](/dir/setup.html)
    -   [需求](/dir/setup.html#需求)
    -   [安装](/dir/setup.html#安装)
    -   [运行时配置](/dir/setup.html#运行时配置)
    -   [资源类型](/dir/setup.html#资源类型)
-   [预定义常量](/dir/constants.html)
-   [Directory](/class/directory.html) — Directory 类
    -   [Directory::close](/class/directory.html#Directory::close) —
        释放目录句柄
    -   [Directory::read](/class/directory.html#Directory::read) —
        从目录句柄中读取条目
    -   [Directory::rewind](/class/directory.html#Directory::rewind) —
        倒回目录句柄
-   [目录函数函数](/ref/dir.html)
    -   [chdir](/ref/dir.html#chdir) — 改变目录
    -   [chroot](/ref/dir.html#chroot) — 改变根目录
    -   [closedir](/ref/dir.html#closedir) — 关闭目录句柄
    -   [dir](/ref/dir.html#dir) — 返回一个 Directory 类实例
    -   [getcwd](/ref/dir.html#getcwd) — 取得当前工作目录
    -   [opendir](/ref/dir.html#opendir) — 打开目录句柄
    -   [readdir](/ref/dir.html#readdir) — 从目录句柄中读取条目
    -   [rewinddir](/ref/dir.html#rewinddir) — 倒回目录句柄
    -   [scandir](/ref/dir.html#scandir) — 列出指定路径中的文件和目录

简介
----

<span class="classname">Directory</span> 实例是通过调用 <span
class="function">dir</span> 函数创建的，而不是
<a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
操作符。

类摘要
------

**Directory**

<span class="ooclass"> class **Directory** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">string</span>
`$path` ;

<span class="modifier">public</span> <span class="type">resource</span>
`$handle` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">read</span> (\[ <span class="methodparam"><span
class="type">resource</span> `$dir_handle`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rewind</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

}

属性
----

`path`  
被打开目录的地址

`handle`  
目录句柄。可以被其他的目录操作函数使用，例如 <span
class="function">readdir</span>, <span class="function">rewinddir</span>
and <span class="function">closedir</span>。

Directory::close
================

释放目录句柄

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Directory::close</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

与 <span class="function">closedir</span> 函数功能一样，只是
`    dir_handle` 默认为 `$this` 变量。

Directory::read
===============

从目录句柄中读取条目

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Directory::read</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

与 <span class="function">readdir</span> 函数功能一样, 只是
`    dir_handle` 默认为 `$this` 变量。

Directory::rewind
=================

倒回目录句柄

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Directory::rewind</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$dir_handle`</span> \] )

与 <span class="function">rewinddir</span> 函数功能一样, 只是
`    dir_handle` 默认为 `$this` 变量。
