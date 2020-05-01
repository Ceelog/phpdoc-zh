安装／配置
==========

**目录**

-   [需求](/luasandbox/setup.html#需求)
-   [安装](/luasandbox/setup.html#安装)
-   [运行时配置](/luasandbox/setup.html#运行时配置)
-   [资源类型](/luasandbox/setup.html#资源类型)

需求
----

To use this extension, Lua 5.1 will need to be installed, available on
the
<a href="http://www.lua.org/" class="link external">» Lua homepage</a>.

To make full use of the timer features, LuaSandbox should be installed
on Linux.

If FreeBSD or Mac OS X is used, only real (wall-clock) time is
supported, the functions purporting to return CPU time will actually
return wall clock time.

If Windows is used, no timer functions will be supported. The time
limits will be inoperable.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/luasandbox" class="link external">» https://pecl.php.net/package/luasandbox</a>.

If the operating system is Debian 9 or later, or Ubuntu 18.04 or later,
then LuaSandbox should typically be installed from the package
*php-luasandbox*:

    sudo apt-get install php-luasandbox

Debian 9 users may need to add

    deb http://ftp.debian.org/debian stretch-backports main

to their
<a href="https://manpages.debian.org/stretch/apt/sources.list.5.en.html" class="link external">» sources.list</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
