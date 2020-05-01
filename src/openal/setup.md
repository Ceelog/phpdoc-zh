安装／配置
==========

**目录**

-   [需求](/openal/setup.html#需求)
-   [安装](/openal/setup.html#安装)
-   [运行时配置](/openal/setup.html#运行时配置)
-   [资源类型](/openal/setup.html#资源类型)

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
<a href="https://pecl.php.net/package/openal" class="link external">» https://pecl.php.net/package/openal</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension defines four resource types: *Open AL(Device)* - Returned
by <span class="function">openal\_device\_open</span>, *Open
AL(Context)* - Returned by <span
class="function">openal\_context\_create</span>, *Open AL(Buffer)* -
Returned by <span class="function">openal\_buffer\_create</span>, and
*Open AL(Source)* - Returned by <span
class="function">openal\_source\_create</span>.
