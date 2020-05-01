安装／配置
==========

**目录**

-   [需求](/image/setup.html#需求)
-   [安装](/image/setup.html#安装)
-   [运行时配置](/image/setup.html#运行时配置)
-   [资源类型](/image/setup.html#资源类型)

需求
----

如果你有 GD 库（可从
<a href="http://www.libgd.org/" class="link external">» http://www.libgd.org/</a>
获得）， 你就可以创建 和处理图像。

可以处理的图像格式由你所使用的 GD 库版本 以及 GD
库可能需要的其他库决定。 在 gd-2.0.28 中，提供了对 GIF 格式的支持。

> **Note**: <span class="simpara"> 要求 libgd-2.0.4 或更高版本， PHP 5.5
> 要求 libgd-2.1.0 或更高版本。 你也可以使用 PHP 中绑定的 GD 库。
> </span>

你可能希望增强 GD 库以处理更多的图像格式。

| 图像格式 | 需要下载的库                                                                                                                                | 备注                                                                                                                                                                      |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *gif*    |                                                                                                                                             | 仅在 gd-2.0.28 及更高版本的 GD 库提供支持， 从 PHP 5.0.1 开始支持 *写入* 操作。                                                                                           |
| *jpeg*   | <a href="http://www.ijg.org/" class="link external">» http://www.ijg.org/</a>                                                               | 在构建 PHP 之前， 需要在配置步骤使用 **--enable-shared** 选项来构建 jpeg 库。 如果不使用此选项，那么在构建 PHP 时的配置环节， 会产生 *libjpeg.(a\|so) not found* 的错误。 |
| *png*    | <a href="http://www.libpng.org/pub/png/libpng.html" class="link external">» http://www.libpng.org/pub/png/libpng.html</a>                   |                                                                                                                                                                           |
| *xpm*    | <a href="ftp://metalab.unc.edu/pub/Linux/libs/X/!INDEX.html" class="link external">» ftp://metalab.unc.edu/pub/Linux/libs/X/!INDEX.html</a> | 如果你的系统中已经安装了 X 环境， 就已经包含这个库了。                                                                                                                    |

你可能希望增强 GD 库来使用不同的字体。 下列字体库是受支持的：

| 字体库         | 下载                                                                                                                                 | 备注                                                 |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| *FreeType 1.x* | <a href="http://www.freetype.org/" class="link external">» http://www.freetype.org/</a>                                              | 从 PHP 5.3.0 开始，不再提供对 FreeType 1.x 的支持。  |
| *FreeType 2*   | <a href="http://www.freetype.org/" class="link external">» http://www.freetype.org/</a>                                              |                                                      |
| *T1lib*        | <a href="ftp://sunsite.unc.edu/pub/Linux/libs/graphics/" class="link external">» ftp://sunsite.unc.edu/pub/Linux/libs/graphics/</a>) | 支持 Postscript Type 1 字体（在 PHP 7.0.0 中移除）。 |

安装
----

要激活 GD 支持，配置 PHP 时加上 **--with-gd\[=DIR\]**，DIR 是 GD
的基本安装目录。要使用推荐的绑定的 GD 库版本（首次绑定于 PHP
4.3.0），使用 **--with-gd**。要编译 GD 库，需要<span
class="productname">libpng</span> 和 <span
class="productname">libjpeg</span>。

在 Windows 中，需要将 GD2 的 DLL 文件 `php_gd2.dll` 作为一个扩展包含在
`php.ini` 中。GD1 的 DLL 文件 `php_gd.dll` 在 PHP 4.3.2
中被删除了。此外要注意首选的真彩色图像函数，例如 <span
class="function">imagecreatetruecolor</span>，需要 GD2。

> **Note**:
>
> 要在 Windows 下启用 exif，在 `php.ini` 中 php\_mbstring.dll 必须在
> php\_exif.dll 之前加载。

要在 *PHP 3* 中禁止 GD 支持，在配置时加上 **--without-gd**。

要增强 GD 的能力以处理更多的图像格式，在配置 PHP 时指定 *--with-XXXX*
的配置开关。

| 图像格式  | 配置开关                                                                                                                                                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *jpeg-6b* | 要激活 jpeg-6b 的支持，加上 **--with-jpeg-dir=DIR**.                                                                                                                              |
| *png*     | 要激活 png 的支持，加上 **--with-png-dir=DIR**。注意，libpng 需要 <a href="/zlib/setup.html#需求" class="link">zlib library</a>，因此配置中还要加上 **--with-zlib-dir\[=DIR\]**。 |
| *xpm*     | 要激活 xpm 的支持，加上 **--with-xpm-dir=DIR**。如果配置时提示找不到所需要的库，可以加上到 X11 库的路径。                                                                         |

> **Note**: <span class="simpara"> 当把 PHP 和 libpng
> 一起编译时，必须使用和 GD 库连接的同一个版本。 </span>

要增强 GD 的能力以处理更多的字体，在配置 PHP 时指定 *--with-XXXX*
的配置开关。

| 字库                       | 配置开关                                                                |
|----------------------------|-------------------------------------------------------------------------|
| *FreeType 1.x*             | 要激活 FreeType 1.x 的支持，加上 **--with-ttf\[=DIR\]**。               |
| *FreeType 2*               | 要激活 FreeType 2 的支持，加上 **--with-freetype-dir=DIR**。            |
| *T1lib*                    | 要激活 T1lib（Type 1 字体），加上 **--with-t1lib\[=DIR\]**。            |
| *本地 TrueType 字符串函数* | 要激活本地 TrueType 字符串函数的支持，加上 **--enable-gd-native-ttf**。 |

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                     | 默认 | 可修改范围    | Changelog                  |
|--------------------------|------|---------------|----------------------------|
| gd.jpeg\_ignore\_warning | "0"  | PHP\_INI\_ALL | Available since PHP 5.1.3. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`gd.jpeg_ignore_warning` <span class="type">bool</span>  
Ignore warnings created by <span class="function">jpeg2wbmp</span> and
<span class="function">imagecreatefromjpeg</span>

See also the <a href="/exif/setup.html#运行时配置" class="link">exif</a>
configuration directives.

**Warning**

Image functions are very memory intensive. Be sure to set
<a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>
high enough.

资源类型
--------

本扩展定义了 2 个资源类型：

| 名称             | 描述                                                                                    | 说明                    |
|------------------|-----------------------------------------------------------------------------------------|-------------------------|
| *gd*             | 图像资源，由 <span class="function">imagecreatefrompng</span> 等函数使用                |                         |
| *gd font*        | 由 <span class="function">imageloadfont</span> 函数内部创建的字体资源                   |                         |
| *gd PS font*     | PostScript Type 1 字体资源，由 <span class="function">imagepsloadfont</span> 函数返回   | 在 PHP 7.0.0 中被移除。 |
| *gd PS encoding* | PostScript Type 1 编码资源，由 <span class="function">imagepsencodefont</span> 函数返回 | 在 PHP 7.0.0 中被移除。 |
