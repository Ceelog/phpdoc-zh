安装／配置
==========

**目录**

-   [需求](/fam/setup.html#需求)
-   [安装](/fam/setup.html#安装)
-   [运行时配置](/fam/setup.html#运行时配置)
-   [资源类型](/fam/setup.html#资源类型)

需求
----

This extension uses the functions of the
<a href="https://web.archive.org/web/20050806075734/http://oss.sgi.com:80/projects/fam/download.html" class="link external">»  FAM</a>
library, developed by SGI. Therefore you have to download and install
the FAM library.

安装
----

此扩展被认为已无人维护及已消亡。然而，此扩展的源代码还可在 PECL SVN
找到：
<a href="https://svn.php.net/viewvc/pecl/fam" class="link external">» https://svn.php.net/viewvc/pecl/fam</a>.

此扩展已被移至
<a href="https://pecl.php.net/" class="link external">» PECL</a>
资源库且不再与 PHP 捆绑。5.1.0

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

There are two resource types used in the FAM module. The first one is
the connection to the FAM service returned by <span
class="function">fam\_open</span>, the second a monitoring resource
returned by the *fam\_monitor\_XXX* functions.
