安装／配置
==========

**目录**

-   [需求](/imagick/setup.html#需求)
-   [安装](/imagick/setup.html#安装)
-   [运行时配置](/imagick/setup.html#运行时配置)
-   [资源类型](/imagick/setup.html#资源类型)

需求
----

Installation requirements on Windows
------------------------------------

Version information does not differ from that above. There are binaries
available from http://www.imagemagick.org/ so that you can load this
extension on *Windows* without need for a compiler.

Installation requirements on other platforms
--------------------------------------------

PHP \>= 5.1.3 and ImageMagick \>= 6.2.4 is required. The amount of file
formats supported by Imagick depends entirely upon the amount of formats
supported by your ImageMagick installation. For example, Imagemagick
requires ghostscript to conduct PDF operations.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/imagick" class="link external">» https://pecl.php.net/package/imagick</a>.

> **Note**: <span class="simpara">The official name of this extension is
> *imagick*.</span>

Windows users can download prebuilt DLL from the
<a href="https://windows.php.net/downloads/pecl/releases/imagick" class="link external">» PECL</a>
website.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                       | 默认        | 可修改范围       | 更新日志                      |
|----------------------------------------------------------------------------|-------------|------------------|-------------------------------|
| <a href="/imagick/setup.html#" class="link">imagick.locale_fix</a>         | **`false`** | PHP\_INI\_ALL    | Available since Imagick 2.1.0 |
| <a href="/imagick/setup.html#" class="link">imagick.progress_monitor</a>   | **`false`** | PHP\_INI\_SYSTEM | Available since Imagick 2.2.2 |
| <a href="/imagick/setup.html#" class="link">imagick.skip_version_check</a> | **`false`** | PHP\_INI\_SYSTEM | Available since Imagick 3.3.0 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`imagick.locale_fix` <span class="type">bool</span>  
Fixes a drawing bug with locales that use '*,*' as float separators.

`imagick.progress_monitor` <span class="type">bool</span>  
Used to enable the image progress monitor.

`imagick.skip_version_check` <span class="type">bool</span>  
When Imagick is loaded, it checks the version number of ImageMagick that
it was compiled against, with the version number that is currently being
used and will give a warning if they don't match. This warning can be
suppressed by enabling this ini setting.

Using a version of Imagick that was compiled against a different version
of ImageMagick than the one being used is not recommended. Although it
may appear to work, it can lead to random crashes or other undefined
behaviour.

资源类型
--------

此扩展没有定义资源类型。
