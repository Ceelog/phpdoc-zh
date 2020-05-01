安装／配置
==========

**目录**

-   [需求](/geoip/setup.html#需求)
-   [安装](/geoip/setup.html#安装)
-   [运行时配置](/geoip/setup.html#运行时配置)
-   [资源类型](/geoip/setup.html#资源类型)

需求
----

这个扩展要求系统安装了 GeoIP C 语言库的1.4.0及以上版本。可通过以下链接
<a href="http://www.maxmind.com/app/c" class="link external">» http://www.maxmind.com/app/c</a>
下载编译该库。

默认情况下只能使用免费的 GeoIP Country 或者 GeoLite City
的数据库。然而这个模块可以使用其他类型的数据库，但必须从以下链接购买商业许可
<a href="http://www.maxmind.com/" class="link external">» Maxmind</a>.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/geoip" class="link external">» https://pecl.php.net/package/geoip</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                 | 默认 | 可修改范围    | 更新日志 |
|----------------------------------------------------------------------|------|---------------|----------|
| <a href="/geoip/setup.html#" class="link">geoip.custom_directory</a> | ""   | PHP\_INI\_ALL |          |

这是配置指令的简短说明。

`geoip.custom_directory` <span class="type">string</span>  
默认为空，但是可以设置一个不同的数据库来覆盖该扩展自带的数据库。

资源类型
--------

此扩展没有定义资源类型。
