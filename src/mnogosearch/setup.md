安装／配置
==========

**目录**

-   [需求](/mnogosearch/setup.html#需求)
-   [安装](/mnogosearch/setup.html#安装)
-   [运行时配置](/mnogosearch/setup.html#运行时配置)
-   [资源类型](/mnogosearch/setup.html#资源类型)

需求
----

Download mnoGosearch from
<a href="http://www.mnogosearch.org/" class="link external">» http://www.mnogosearch.org/</a>
and install it on your system. You need at least version 3.1.10 of
mnoGoSearch installed to use these functions.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/mnogosearch" class="link external">» https://pecl.php.net/package/mnogosearch</a>.

此扩展已被移至
<a href="https://pecl.php.net/" class="link external">» PECL</a>
资源库且不再与 PHP 捆绑。5.1.0

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

> **Note**:
>
> PHP contains built-in MySQL access library, which can be used to
> access MySQL. It is known that mnoGoSearch is not compatible with this
> built-in library and can work only with generic MySQL libraries. Thus,
> if you use mnoGoSearch with MySQL, during PHP configuration you have
> to indicate the directory of your MySQL installation, that was used
> during mnoGoSearch configuration, i.e. for example:
> **--with-mnogosearch --with-mysql=/usr**.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
