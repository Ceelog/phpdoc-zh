安装／配置
==========

**目录**

-   [需求](/mqseries/setup.html#需求)
-   [安装](/mqseries/setup.html#安装)
-   [运行时配置](/mqseries/setup.html#运行时配置)
-   [资源类型](/mqseries/setup.html#资源类型)

需求
----

A working IBM WebSphere MQ installation. If building the extension the
SDK for IBM WebSphere MQ is also required.

> **Note**: <span class="simpara"> Be aware that when running against a
> IBM WebSphere MQ Client installation some methods are not available.
> This is not a problem of the extension but just the way the WebSphere
> MQ Client Interface works. </span>

Installation requirements on non windows platforms
--------------------------------------------------

Build the extension and put it in the PHP extension directory.

Installation requirements on Windows
------------------------------------

No additional requirements.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/mqseries" class="link external">» https://pecl.php.net/package/mqseries</a>.

> **Note**: <span class="simpara"> The official name of this extension
> is *mqseries*. </span>

There are two ways to connect to a queue manager. These depend on the
way the extension is compiled and linked.

-   First one and also the default one is using the mqic libraries.
    Compiling and linking the extension against these IBM WebSphere
    MQSeries libraries allows the extension to connect to the Queue
    manager using the client interface. Remote connections are possible
    this way.

-   The other way is to compile and link against the mqm libraries.
    Using these libraries it is possible to make use of the transaction
    management of a queue manager.

Currently selecting the libraries to use is done by changing the
`config.m4` file.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

There are no extra configuration parameters.

资源类型
--------

This extension defines a connection and object\_handle resources.

The <span class="function">mqseries\_conn</span> and <span
class="function">mqseries\_connx</span> define the connectionn handles.

The <span class="function">mqseries\_open</span> defines the object
handle.
