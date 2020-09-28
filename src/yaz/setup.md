安装／配置
==========

**目录**

-   [需求](/yaz/setup.html#需求)
-   [安装](/yaz/setup.html#安装)
-   [运行时配置](/yaz/setup.html#运行时配置)
-   [资源类型](/yaz/setup.html#资源类型)

需求
----

Obtain YAZ (ANSI/NISO Z39.50 support) and install it. YAZ can be fetched
in source or in various prebuilt packages from the
<a href="http://ftp.indexdata.dk/pub/yaz/" class="link external">» YAZ archive</a>.
Systems such as Debian GNU/Linux, Suse Linux, FreeBSD also has YAZ as
part of their distribution.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/yaz" class="link external">» https://pecl.php.net/package/yaz</a>

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

> **Note**: **Information specific to Windows users**  
>
> `php_yaz.dll` depends on `yaz.dll`. The `yaz.dll` is part of the Win32
> ZIP from the PHP site. It is also part of the Windows YAZ install
> available from the
> <a href="http://ftp.indexdata.dk/pub/yaz/win32/" class="link external">» YAZ WIN32 area</a>.
>
> On windows, don't forget to add the PHP directory to the `PATH`, so
> that the `yaz.dll` file can be found by the system.

**Warning**

<a href="/book/imap.html" class="link">IMAP</a>，<a href="/book/recode.html" class="link">recode</a>，和
<a href="/book/yaz.html" class="link">YAZ</a>
扩展不能同时使用，因为它们共享了相同 的内部符号。注意：Yaz 2.0
及以上版本不存在此问题。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
