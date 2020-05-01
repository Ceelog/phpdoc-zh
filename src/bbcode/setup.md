安装／配置
==========

**目录**

-   [需求](/bbcode/setup.html#需求)
-   [安装](/bbcode/setup.html#安装)
-   [运行时配置](/bbcode/setup.html#运行时配置)
-   [资源类型](/bbcode/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/bbcode" class="link external">» https://pecl.php.net/package/bbcode</a>

An alternative solution, written in PHP, is the PEAR package
<a href="https://pear.php.net/package/HTML_BBCodeParser" class="link external">» HTML_BBCodeParser</a>.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

One resource is used in the BBCode extension: a BBCode\_Container
returned by <span class="function">bbcode\_create</span>.
