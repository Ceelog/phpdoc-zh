安装／配置
==========

**目录**

-   [需求](/gupnp/setup.html#需求)
-   [安装](/gupnp/setup.html#安装)
-   [运行时配置](/gupnp/setup.html#运行时配置)
-   [资源类型](/gupnp/setup.html#资源类型)

需求
----

In order to use PECL/Gupnp functions you need to install the
<a href="http://www.gupnp.org/" class="link external">» gUPnP library</a>
version 0.12.7 or greater. It also requires glib-2.0, gssdp-1.0,
libsoup-2.4 or greater for all of them.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/gupnp" class="link external">» https://pecl.php.net/package/gupnp</a>

> **Note**: <span class="simpara"> If `./configure` is having trouble
> finding the libgupnp files (for example, it was installed into a
> custom prefix directory), use
> **`./configure      --with-gupnp=$PREFIX`**, where $PREFIX is
> installation prefix of libgupnp. </span>

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
