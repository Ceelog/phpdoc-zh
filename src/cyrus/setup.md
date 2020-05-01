安装／配置
==========

**目录**

-   [需求](/cyrus/setup.html#需求)
-   [安装](/cyrus/setup.html#安装)
-   [运行时配置](/cyrus/setup.html#运行时配置)
-   [资源类型](/cyrus/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

To enable Cyrus IMAP support and to use these functions you have to
compile PHP with the **--with-cyrus** option.

**Warning**

<a href="/book/imap.html" class="link">IMAP</a>，<a href="/book/recode.html" class="link">recode</a>，<a href="/book/yaz.html" class="link">YAZ</a>
和 <a href="/book/cyrus.html" class="link">Cyrus</a>
扩展不能同时使用，因为它们共享了相同 的内部符号。注意：Yaz 2.0
及以上版本不存在此问题。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines a Cyrus IMAP connection identifier returned by
<span class="function">cyrus\_connect</span>.
