安装／配置
==========

**目录**

-   [需求](/hwapi/setup.html#需求)
-   [安装](/hwapi/setup.html#安装)
-   [运行时配置](/hwapi/setup.html#运行时配置)
-   [资源类型](/hwapi/setup.html#资源类型)

需求
----

Since 2001 there is a Hyperwave SDK available. It supports Java,
JavaScript and C++. This PHP Extension is based on the C++ interface. In
order to activate the hwapi support in PHP you will have to install the
Hyperwave SDK first.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/hwapi" class="link external">» https://pecl.php.net/package/hwapi</a>.

此扩展已被移至
<a href="https://pecl.php.net/" class="link external">» PECL</a>
资源库且不再与 PHP 捆绑。5.2.0

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                    | 默认 | 可修改范围       | 更新日志 |
|-------------------------|------|------------------|----------|
| hwapi.allow\_persistent | "0"  | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

资源类型
--------

此扩展没有定义资源类型。
