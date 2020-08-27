安装／配置
==========

**目录**

-   [需求](/xattr/setup.html#需求)
-   [安装](/xattr/setup.html#安装)
-   [运行时配置](/xattr/setup.html#运行时配置)
-   [资源类型](/xattr/setup.html#资源类型)

需求
----

To use xattr, you will need libattr installed. It is available at
<a href="http://savannah.nongnu.org/projects/attr/" class="link external">» http://savannah.nongnu.org/projects/attr/</a>.

> **Note**:
>
> These functions only work on filesystems that support extended
> attributes, and have them enabled at mount time. Some common
> filesystems that support extended attributes are ext2, ext3, reiserfs,
> jfs, and xfs.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/xattr" class="link external">» https://pecl.php.net/package/xattr</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
