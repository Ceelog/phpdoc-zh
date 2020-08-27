安装／配置
==========

**目录**

-   [需求](/wddx/setup.html#需求)
-   [安装](/wddx/setup.html#安装)
-   [运行时配置](/wddx/setup.html#运行时配置)
-   [资源类型](/wddx/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--with-libxml**，或在 PHP 7.4 之前的版本中使用
**--enable-libxml**， 尽管这将隐式完成因为 libxml 是缺省开启的。

In order to use WDDX, you will need to install the expat library (which
comes with Apache 1.3.7 or higher).

安装
----

PHP 7.4
-------

此扩展已被移至
<a href="https://pecl.php.net/" class="link external">» PECL</a>
资源库且不再与 PHP 捆绑。7.4.0

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/wddx" class="link external">» https://pecl.php.net/package/wddx</a>.

PHP \< 7.4
----------

After installing the required expat library, compile PHP with
**--enable-wddx**, and use **--with-libexpat-dir** for expat.

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines a WDDX packet identifier returned by <span
class="function">wddx\_packet\_start</span>.
