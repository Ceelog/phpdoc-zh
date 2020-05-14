安装／配置
==========

**目录**

-   [需求](/recode/setup.html#需求)
-   [安装](/recode/setup.html#安装)
-   [运行时配置](/recode/setup.html#运行时配置)
-   [资源类型](/recode/setup.html#资源类型)

需求
----

You must have GNU Recode 3.5 or higher installed on your system. You can
download the package from
<a href="http://directory.fsf.org/All_GNU_Packages/recode.html" class="link external">» http://directory.fsf.org/All_GNU_Packages/recode.html</a>.

**Warning**

The Recode library version 3.6 adds weird characters behind converted
strings under certain circumstances. Thus it's safer to use Recode v3.5
or one of the available alternatives like the
<a href="/ref/iconv.html" class="link">iconv</a> or
<a href="/ref/mbstring.html" class="link">mbstring</a> extension.

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
<a href="https://pecl.php.net/package/recode" class="link external">» https://pecl.php.net/package/recode</a>.

PHP \< 7.4
----------

To be able to use the functions defined in this module you must compile
your PHP interpreter using the **--with-recode\[=DIR\]** option.

**Warning**

Crashes and startup problems of PHP may be encountered when loading the
recode as extension *after* loading any extension of
<a href="/set/mysqlinfo.html#MySQL%20函数" class="link">mysql</a> or
<a href="/ref/imap.html" class="link">imap</a>. Loading the recode
before those extension has proved to fix the problem. This is due a
technical problem that both the c-client library used by imap and recode
have their own *hash\_lookup()* function and both mysql and recode have
their own *hash\_insert* function.

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

此扩展没有定义资源类型。
