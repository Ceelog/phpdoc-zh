安装／配置
==========

**目录**

-   [需求](/sphinx/setup.html#需求)
-   [安装](/sphinx/setup.html#安装)
-   [运行时配置](/sphinx/setup.html#运行时配置)
-   [资源类型](/sphinx/setup.html#资源类型)

需求
----

PECL/sphinx requires PHP 5.2.2 or newer.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/sphinx" class="link external">» https://pecl.php.net/package/sphinx</a>.

如果 `./configure` 不能正确找到 libsphinxclient 文件 (例如,
他被安装在用户自己定义的目录中), 使用
**`./configure    --with-sphinx=$PREFIX`**来制定libsphinxclient的具体位置（$PREFIX是libsphinxclient的安装位置）.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
