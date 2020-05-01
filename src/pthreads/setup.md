安装／配置
==========

**目录**

-   [需求](/pthreads/setup.html#需求)
-   [安装](/pthreads/setup.html#安装)
-   [运行时配置](/pthreads/setup.html#运行时配置)

需求
----

要使用 pthreads 扩展，需要构建 PHP 时启用 ZTS （Zend Thread
Safety）。（--enable-maintainer-zts 选项， Windows 平台为 --enable-zts）

**Caution**

ZTS 是构建期配置选项，只能通过构建时通过选项启用，无法在构建之后启用。

要构建 pthreads 扩展，你需要启用了 ZTS 的 PHP 以及 Posix Threads
头文件（pthread.h）。对于 Windows 平台，需要使用 redhat 的 pthread-w32
项目中的 pthread.h 头文件。

安装
----

pthreads 扩展由 PECL 主持，使用
<a href="https://github.com/krakjoe/pthreads" class="link external">» github</a>
管理源代码。 使用标准的 PECL
包安装方式就可以完成安装：<a href="https://pecl.php.net/package/pthreads" class="link external">» https://pecl.php.net/package/pthreads</a>。

Windows 用户可以从
<a href="https://windows.php.net/downloads/pecl/releases/pthreads" class="link external">» PECL</a>
下载已经构建的二进制发行包。

**Caution**

Windows 用户需要将 pthreadVC2.dll （包含在 Windows
版二进制发行包中）所在路径加入到 `PATH` 环境变量中。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。
