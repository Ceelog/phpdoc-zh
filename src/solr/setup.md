安装／配置
==========

**目录**

-   [需求](/solr/setup.html#需求)
-   [安装](/solr/setup.html#安装)
-   [运行时配置](/solr/setup.html#运行时配置)
-   [资源类型](/solr/setup.html#资源类型)

需求
----

PHP version 5.2.11 or later is required.

The libxml and curl extensions must also be enabled for the Apache Solr
extension to be available.

libxml2 2.6.31 or later is required.

libcurl 7.18.0 or later is also required.

The above library versions are required and attempting to hack the code
to make it compile is strongly discouraged. It will fail, possibly with
errors that could be hard to debug

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/solr" class="link external">» https://pecl.php.net/package/solr</a>.

For help and support, please visit the extension google group.
<a href="https://groups.google.com/forum/#!forum/php-solr" class="link external">» Apache Solr PHP Extension</a>

此扩展在 Windows 平台的二进制扩展 (DLL 文件) PECL 可以在 PECL
官方网站上下载。

> **Note**:
>
> The solr module can be compiled in debug mode by passing the
> --enable-solr-debug flag to configure
>
> When building manually, be sure to include curl and libxml support
> within the build.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
