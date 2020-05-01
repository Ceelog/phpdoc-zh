安装／配置
==========

**目录**

-   [需求](/inotify/setup.html#需求)
-   [安装／配置](/inotify/setup.html#安装／配置)
-   [运行时配置](/inotify/setup.html#运行时配置)
-   [资源类型](/inotify/setup.html#资源类型)

需求
----

This extension requires Linux 2.6.13 or newer, and a recent libC.

安装／配置
----------

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/inotify" class="link external">» https://pecl.php.net/package/inotify</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines a stream resource returned by <span
class="function">inotify\_init</span>.
