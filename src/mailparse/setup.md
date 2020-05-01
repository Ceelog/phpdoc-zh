安装／配置
==========

**目录**

-   [需求](/mailparse/setup.html#需求)
-   [安装](/mailparse/setup.html#安装)
-   [运行时配置](/mailparse/setup.html#运行时配置)
-   [资源类型](/mailparse/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/mailparse" class="link external">» https://pecl.php.net/package/mailparse</a>.

In order to use these functions you must compile PHP with mailparse
support by using the **--enable-mailparse** configure option.

Windows users will enable `php_mailparse.dll` inside of `php.ini` in
order to use these functions. PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

It is necessary that the
<a href="/ref/mbstring.html" class="link">mbstring</a> extension is
loaded before mailparse.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
