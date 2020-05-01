安装／配置
==========

**目录**

-   [需求](/session-pgsql/setup.html#需求)
-   [安装](/session-pgsql/setup.html#安装)
-   [运行时配置](/session-pgsql/setup.html#运行时配置)
-   [资源类型](/session-pgsql/setup.html#资源类型)

需求
----

You need at least PHP \>= 4.3.0, and PostgreSQL \>=7.2.0 as database
server. *libpq* that comes with PostgreSQL 7.2.0 or later (and header
files to build) and
<a href="http://www.ossp.org/pkg/lib/mm/" class="link external">» libmm</a>
(and header files).

安装
----

此扩展被认为已无人维护及已消亡。然而，此扩展的源代码还可在 PECL SVN
找到：
<a href="https://svn.php.net/viewvc/pecl/session_pgsql" class="link external">» https://svn.php.net/viewvc/pecl/session_pgsql</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

PostgreSQL session save handler is still under development. Refer to the
`README` file in the source distribution for configuration details.

资源类型
--------

此扩展没有定义资源类型。
