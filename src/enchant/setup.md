安装／配置
==========

**目录**

-   [需求](/enchant/setup.html#需求)
-   [安装](/enchant/setup.html#安装)
-   [运行时配置](/enchant/setup.html#运行时配置)
-   [资源类型](/enchant/setup.html#资源类型)

需求
----

This version uses the functions of the
<a href="http://www.abisource.com/projects/enchant/" class="link external">» Enchant library</a>
by Dom Lachowicz. You need Enchant 1.2.4 or later. Enchant 2.0.0 or
later is not yet supported.

Enchant also requires
<a href="http://ftp.gnome.org/pub/gnome/sources/glib/" class="link external">» Glib 2.6</a>
or greater. Pre-compiled Windows libraries are available from
<a href="http://ftp.gnome.org/pub/gnome/binaries/win32/glib/" class="link external">» http://ftp.gnome.org/pub/gnome/binaries/win32/glib/</a>.

安装
----

This extension is bundled with PHP as of PHP 5.3.0. Before this time,
enchant was a PECL extension. Users of versions prior to 5.3.0 may use
the
<a href="https://pecl.php.net/package/enchant" class="link external">» PECL extension</a>.

Provided the
<a href="/enchant/setup.html#需求" class="link">required libraries</a>
are installed, users of PHP 5.3.0 or later may enable enchant by adding
the **--with-enchant\[=dir\]** option when compiling PHP.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

There are two types of resources in this extension. The first one is the
broker (backends manager) and the second is for the dictionary.
