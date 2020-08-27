安装／配置
==========

**目录**

-   [需求](/ssh2/setup.html#需求)
-   [安装](/ssh2/setup.html#安装)
-   [运行时配置](/ssh2/setup.html#运行时配置)
-   [资源类型](/ssh2/setup.html#资源类型)

需求
----

The
<a href="http://www.openssl.org/" class="link external">» OpenSSL</a>
and <a href="http://libssh2.org/" class="link external">» libssh2</a>
libraries are required. Ensure that the development libraries are
installed, where a typical package name might be *openssl-dev*.

Version 1.2 or newer of the libssh2 library is required, although it's
possible newer releases of pecl/ssh2 may require newer versions (see the
release notes).

The <span class="function">ssh2\_auth\_agent</span> function will only
be available with libssh \>= 1.2.3.

support for <span class="function">stream\_set\_timeout</span> to
channel streams will only be available with libssh \>= 1.2.9.

Libssh2 comes in two flavours: gcrypt or openssl. Some linux
distributions build libssh2 with the gcrypt library, some use openssl.
Libssh2 has some issues when compiled with gcrypt, please use openssl.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/ssh2" class="link external">» https://pecl.php.net/package/ssh2</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
