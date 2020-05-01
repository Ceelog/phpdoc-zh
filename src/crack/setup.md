安装／配置
==========

**目录**

-   [需求](/crack/setup.html#需求)
-   [安装](/crack/setup.html#安装)
-   [运行时配置](/crack/setup.html#运行时配置)
-   [资源类型](/crack/setup.html#资源类型)

需求
----

More information regarding CrackLib along with the library can be found
at
<a href="http://sourceforge.net/projects/cracklib" class="link external">» http://sourceforge.net/projects/cracklib</a>.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。 安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/crack" class="link external">» https://pecl.php.net/package/crack</a>.

In order to use these functions you must compile PHP with Crack support
by using the **--with-crack\[=DIR\]** configuration option.

Windows users will enable `php_crack.dll` inside of `php.ini` in order
to use these functions. PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

The CrackLib extension defines a dictionary resource identifier returned
by <span class="function">crack\_opendict</span>.
