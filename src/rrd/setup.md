安装／配置
==========

**目录**

-   [需求](/rrd/setup.html#需求)
-   [安装](/rrd/setup.html#安装)
-   [运行时配置](/rrd/setup.html#运行时配置)
-   [资源类型](/rrd/setup.html#资源类型)

需求
----

You need to install librrd first to be able to use PECL/rrd. Most common
option is using of librrd-dev package from your favourite linux distro.
PECL/rrd is tested with librrd 1.4.3, older or newer versions might or
might not work for you. PECL/rrd installation is tested with PHP 5.3.2
or newer.

**Warning**

Librrd and hence extension itself aren't mostly thread safe. There are
many global and shared states in librrd. It can be dangerous use this
extension in multi threaded environments like Apache2 mpm worker. If
there are many parallel requests, one request can change some global
librrd state of other runnig requests.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/rrd" class="link external">» https://pecl.php.net/package/rrd</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
