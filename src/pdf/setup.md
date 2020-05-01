安装／配置
==========

**目录**

-   [需求](/pdf/setup.html#需求)
-   [安装](/pdf/setup.html#安装)
-   [运行时配置](/pdf/setup.html#运行时配置)
-   [资源类型](/pdf/setup.html#资源类型)

需求
----

PDFlib Lite is available as open source. However, the PDFlib Lite
license allows free use only under certain conditions. PDFlib Lite
supports a subset of PDFlib's functionality; please see the PDFlib web
site for details. The full version of PDFlib is available for download
at
<a href="http://www.pdflib.com/products/pdflib-family/" class="link external">» http://www.pdflib.com/products/pdflib-family/</a>,
but requires that you purchase a license for commercial use.

Issues with older versions of PDFlib
------------------------------------

Any version of PHP 4 after March 9, 2000 does not support versions of
PDFlib older than 3.0.

PDFlib 4.0 or greater is supported by PHP 4.3.0 and later.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/pdflib" class="link external">» https://pecl.php.net/package/pdflib</a>.

To get these functions to work in PHP \< 4.3.9, you have to compile PHP
with **--with-pdflib\[=DIR\]**. DIR is the PDFlib base install
directory, defaults to `/usr/local`.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

<span class="function">PDF\_new</span> creates a new PDFlib object
required by most PDF functions.
