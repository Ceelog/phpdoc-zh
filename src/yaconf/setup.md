安装／配置
==========

**目录**

-   [需求](/yaconf/setup.html#需求)
-   [安装](/yaconf/setup.html#安装)
-   [运行时配置](/yaconf/setup.html#运行时配置)
-   [资源类型](/yaconf/setup.html#资源类型)

需求
----

Yaconf requires PHP 7.0 and above.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/yaconf" class="link external">» https://pecl.php.net/package/yaconf</a>.

此扩展在 Windows 平台的二进制扩展 (DLL 文件) PECL 可以在 PECL
官方网站上下载。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                              | 默认       | 可修改范围       | 更新日志 |
|-------------------------------------------------------------------|------------|------------------|----------|
| <a href="/yaconf/setup.html#" class="link">yaconf.check_delay</a> | 300        | PHP\_INI\_SYSTEM |          |
| <a href="/yaconf/setup.html#" class="link">yaconf.directory</a>   | /tmp/conf/ | PHP\_INI\_SYSTEM |          |

这是配置指令的简短说明。

`yaconf.check_delay` <span class="type">integer</span>  
In which interval Yaconf will detect ini file's change(by directory's
mtime), if it is set to zero, you have to restart php to reloading
configurations.

`yaconf.directory` <span class="type">string</span>  
Path to directory which all INI configuration files are placed in.

资源类型
--------
