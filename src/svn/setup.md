安装／配置
==========

**目录**

-   [需求](/svn/setup.html#需求)
-   [安装](/svn/setup.html#安装)
-   [运行时配置](/svn/setup.html#运行时配置)
-   [资源类型](/svn/setup.html#资源类型)

需求
----

The Subversion binaries are not necessary to use this extension.
However, when compiling the extension, libsvn (the Subversion headers)
must be available.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/svn" class="link external">» https://pecl.php.net/package/svn</a>

If `./configure` is having trouble finding the SVN files (for example,
Subversion was installed with a different prefix directory), use
**`./configure --with-svn=$USR_PATH`** to specify the directory where
the `include/subversion-1/` folder is located.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

**Warning**

If the extension is compiled against libsvn 1.3, functions that work
with working copies will fail when used on working copies created by
Subversion 1.4.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
