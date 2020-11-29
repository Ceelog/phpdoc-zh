安装／配置
==========

**目录**

-   [需求](/win32service/setup.html#需求)
-   [安装](/win32service/setup.html#安装)
-   [运行时配置](/win32service/setup.html#运行时配置)
-   [资源类型](/win32service/setup.html#资源类型)
-   [Security
    consideration](/win32service/setup.html#Security%20consideration)

需求
----

The versions of Windows supported are the same as the Visual C++
redistributable package used to build PHP.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/win32service" class="link external">» https://pecl.php.net/package/win32service</a>

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。

Security consideration
----------------------

This extension needs administrator privileges for some actions such as
<a href="/ref/win32service.html#win32_create_service" class="link">create</a>,
<a href="/ref/win32service.html#win32_delete_service" class="link">delete</a>,
<a href="/ref/win32service.html#win32_start_service" class="link">start</a>,
<a href="/ref/win32service.html#win32_stop_service" class="link">stop</a>,
<a href="/ref/win32service.html#win32_pause_service" class="link">pause</a>
and
<a href="/ref/win32service.html#win32_continue_service" class="link">continue</a>.
This requirement can cause an elevation of privileges if the service
control is available from the web interface or remote control.

You can set the ACL on the service after adding it into SCM to delegate
the current administration tasks to an non administrator account or
service account. For further instructions, see the
<a href="https://support.microsoft.com/en-us/help/914392/best-practices-and-guidance-for-writers-of-service-discretionary-acces" class="link external">» Microsoft Knowledge Base</a>.
