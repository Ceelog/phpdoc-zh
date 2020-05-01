安装／配置
==========

**目录**

-   [需求](/mcve/setup.html#需求)
-   [安装](/mcve/setup.html#安装)
-   [运行时配置](/mcve/setup.html#运行时配置)
-   [资源类型](/mcve/setup.html#资源类型)

需求
----

The LibMonetra (formerly libmcve) library.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/mcve" class="link external">» https://pecl.php.net/package/mcve</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

If installing without specifying the libmonetra path, PHP will attempt
to look in the default LibMonetra Install location (`/usr/local`). If
Monetra (MCVE) is in a non-standard location, run configure with:
**--with-mcve=$mcve\_path**, where $mcve\_path is the path to your
MCVE/Monetra installation. Please note that MCVE/Monetra support
requires that $mcve\_path/lib and $mcve\_path/include exist, and include
`mcve.h` or `monetra.h` under the include directory and `libmcve.so`
and/or `libmcve.a` and/or `libmonetra.so` and/or `libmonetra.a` under
the lib directory.

Since MCVE/Monetra has true server/client separation, there are no
additional requirements for running PHP with MCVE support. To test your
MCVE/Monetra extension in PHP, you may connect to testbox.monetra.com on
port 8333 for IP, or port 8444 for SSL using the MCVE/Monetra PHP API.
Use 'vitale' for your username, and 'test' for your password. Additional
information about test facilities are available at
<a href="http://www.mainstreetsoftworks.com/" class="link external">» http://www.mainstreetsoftworks.com/</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines a MCVE\_CONN resource returned by <span
class="function">m\_initconn</span>.
