安装／配置
==========

**目录**

-   [需求](/yac/setup.html#需求)
-   [安装](/yac/setup.html#安装)
-   [运行时配置](/yac/setup.html#运行时配置)
-   [资源类型](/yac/setup.html#资源类型)

需求
----

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/yac" class="link external">» https://pecl.php.net/package/yac</a>.

此扩展在 Windows 平台的二进制扩展 (DLL 文件) PECL 可以在 PECL
官方网站上下载。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                               | 默认 | 可修改范围       | 更新日志 |
|--------------------------------------------------------------------|------|------------------|----------|
| <a href="/yac/setup.html#" class="link">yac.compress_threshold</a> | -1   | PHP\_INI\_SYSTEM |          |
| <a href="/yac/setup.html#" class="link">yac.debug</a>              | 0    | PHP\_INI\_ALL    |          |
| <a href="/yac/setup.html#" class="link">yac.enable</a>             | 1    | PHP\_INI\_SYSTEM |          |
| <a href="/yac/setup.html#" class="link">yac.enable_cli</a>         | 0    | PHP\_INI\_SYSTEM |          |
| <a href="/yac/setup.html#" class="link">yac.keys_memory_size</a>   | 4M   | PHP\_INI\_SYSTEM |          |
| <a href="/yac/setup.html#" class="link">yac.serializer</a>         | php  | PHP\_INI\_SYSTEM |          |
| <a href="/yac/setup.html#" class="link">yac.values_memory_size</a> | 64M  | PHP\_INI\_SYSTEM |          |

这是配置指令的简短说明。

`yac.compress_threshold` <span class="type">int</span>  

`yac.debug` <span class="type">int</span>  

`yac.enable` <span class="type">int</span>  

`yac.enable_cli` <span class="type">int</span>  

`yac.keys_memory_size` <span class="type">string</span>  

`yac.serializer` <span class="type">string</span>  

`yac.values_memory_size` <span class="type">string</span>  

资源类型
--------
