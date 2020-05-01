安装／配置
==========

**目录**

-   [需求](/htscanner/setup.html#需求)
-   [安装](/htscanner/setup.html#安装)
-   [运行时配置](/htscanner/setup.html#运行时配置)
-   [资源类型](/htscanner/setup.html#资源类型)

需求
----

PHP version 5.2.0 or greater.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/htscanner" class="link external">» https://pecl.php.net/package/htscanner</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                        | 默认         | 可修改范围       | Changelog |
|-----------------------------------------------------------------------------|--------------|------------------|-----------|
| <a href="/htscanner/setup.html#" class="link">htscanner.config_file</a>     | ".htscanner" | PHP\_INI\_SYSTEM |           |
| <a href="/htscanner/setup.html#" class="link">htscanner.default_docroot</a> | "/"          | PHP\_INI\_SYSTEM |           |
| <a href="/htscanner/setup.html#" class="link">htscanner.default_ttl</a>     | "300"        | PHP\_INI\_SYSTEM |           |
| <a href="/htscanner/setup.html#" class="link">htscanner.stop_on_error</a>   | "Off"        | PHP\_INI\_SYSTEM |           |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`htscanner.config_file` <span class="type">string</span>  
Filename to use as configuration file.

`htscanner.default_docroot` <span class="type">string</span>  
Default document root.

`htscanner.default_ttl` <span class="type">int</span>  
Cache time out for the configuration data, in seconds.

`htscanner.stop_on_error` <span class="type">int</span>  
Stop on error (parse error, cannot set an ini setting).

资源类型
--------

此扩展没有定义资源类型。
