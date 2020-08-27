安装／配置
==========

**目录**

-   [需求](/taint/setup.html#需求)
-   [安装](/taint/setup.html#安装)
-   [运行时配置](/taint/setup.html#运行时配置)
-   [资源类型](/taint/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/taint" class="link external">» https://pecl.php.net/package/taint</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                            | 默认       | 可修改范围       | 更新日志 |
|-----------------------------------------------------------------|------------|------------------|----------|
| <a href="/taint/setup.html#" class="link">taint.enable</a>      | 0          | PHP\_INI\_SYSTEM |          |
| <a href="/taint/setup.html#" class="link">taint.error_level</a> | E\_WARNING | PHP\_INI\_ALL    |          |

这是配置指令的简短说明。

`taint.enable` <span class="type">integer</span>  
Whether enable the taint.

`taint.error_level` <span class="type">integer</span>  
the error type which taint will report as when taint find a tainted
string.

资源类型
--------

此扩展没有定义资源类型。
