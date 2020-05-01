安装／配置
==========

**目录**

-   [需求](/apd/setup.html#需求)
-   [安装](/apd/setup.html#安装)
-   [Building on Win32](/apd/setup.html#Building%20on%20Win32)
-   [运行时配置](/apd/setup.html#运行时配置)
-   [资源类型](/apd/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/apd" class="link external">» https://pecl.php.net/package/apd</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

In your INI file, add the following lines:

``` php.ini
zend_extension = /absolute/path/to/apd.so
apd.dumpdir = /absolute/path/to/trace/directory
apd.statement_tracing = 0
```

Depending on your PHP build, the zend\_extension directive can be one of
the following:

``` script
zend_extension              (non ZTS, non debug build)
zend_extension_ts           (    ZTS, non debug build)
zend_extension_debug        (non ZTS,     debug build)
zend_extension_debug_ts     (    ZTS,     debug build)
```

Building on Win32
-----------------

To build APD under Windows you need a working PHP compilation
environment as described on http://php.net/ -- basically, it requires
you to have Microsoft Visual C++, win32build.zip, bison/flex, and some
know how to get it to work. Also ensure that adp.dsp has DOS line
endings; if it has unix line endings, Microsoft Visual C++ will complain
about it.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                              | 默认 | 可修改范围    | 更新日志 |
|-------------------------------------------------------------------|------|---------------|----------|
| <a href="/apd/setup.html#" class="link">apd.dumpdir</a>           | NULL | PHP\_INI\_ALL |          |
| <a href="/apd/setup.html#" class="link">apd.statement_tracing</a> | "0"  | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`apd.dumpdir` <span class="type">string</span>  
设定 APD 写入调试输出文件的目录。可以指定绝对路径或相对路径。

可以在 <span class="function">apd\_set\_pprof\_trace</span>
中以参数指定一个不同目录。

`apd.statement_tracing` <span class="type">boolean</span>  
指定是否进行每行的跟踪。将此项打开（设为 1）将影响到程序的性能。

资源类型
--------

此扩展没有定义资源类型。
