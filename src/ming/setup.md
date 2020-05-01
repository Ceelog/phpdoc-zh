安装／配置
==========

**目录**

-   [需求](/ming/setup.html#需求)
-   [安装](/ming/setup.html#安装)
-   [运行时配置](/ming/setup.html#运行时配置)
-   [资源类型](/ming/setup.html#资源类型)

需求
----

To use Ming with PHP, you first need to build and install the Ming
library. Source code and installation instructions are available at the
Ming home page:
<a href="http://www.libming.org/" class="link external">» http://www.libming.org/</a>
along with examples, a small tutorial, and the latest news.

Download the ming archive. Unpack the archive. Go in the Ming directory.
make. make install.

This will build `libming.so` and install it into `/usr/lib/`, and copy
`ming.h` into `/usr/include/`. Edit the *PREFIX=* line in the `Makefile`
to change the installation directory.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/ming" class="link external">» https://pecl.php.net/package/ming</a>.

此扩展已被移至
<a href="https://pecl.php.net/" class="link external">» PECL</a>
资源库且不再与 PHP 捆绑。5.3.0

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
