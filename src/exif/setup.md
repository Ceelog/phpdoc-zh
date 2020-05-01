安装／配置
==========

**目录**

-   [需求](/exif/setup.html#需求)
-   [安装](/exif/setup.html#安装)
-   [运行时配置](/exif/setup.html#运行时配置)
-   [资源类型](/exif/setup.html#资源类型)

需求
----

必须使用 *--enable-exif* 选项编译 PHP。 如果要提供对 EXIF
标签中元数据的多字节文字支持，需要通过使用 *--enable-mbstring* 选项编译
PHP 来启用 <a href="/ref/mbstring.html" class="link">mbstring</a> 扩展。
exif 不需要其他额外的 PHP 库就可以直接使用。

Windows 平台：必须启用
<a href="/ref/mbstring.html" class="link">mbstring</a> 扩展。 并且，在
`php.ini` 文件中，
<a href="/ref/mbstring.html" class="link">mbstring</a> 必须先于 EXIF
加载。

安装
----

使用 **--enable-exif** 选项 配置 PHP 来启用 exif 支持。

Windows 用户必须在 `php.ini` 中启用 `php_mbstring.dll` 和 `php_exif.dll`
扩展。 请确保在 `php.ini` 中保持正确的顺序： `php_mbstring.dll` 必须在
`php_exif.dll` *之前* 加载。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

当 <a href="/ref/mbstring.html" class="link">mbstring</a>
模块可用时，exif 支持用户注释中的 Unicode 和 JIS
字符编码的自动转换。这是通过先用指定字符集将注释解码，把结果再用另一个符合你的
*HTTP* 输出的字符集编码来实现的。

| 名字                                                                      | 默认          | 可修改范围    | 更新日志              |
|---------------------------------------------------------------------------|---------------|---------------|-----------------------|
| <a href="/exif/setup.html#" class="link">exif.encode_unicode</a>          | "ISO-8859-15" | PHP\_INI\_ALL | 自 PHP 4.3.0 起可用。 |
| <a href="/exif/setup.html#" class="link">exif.decode_unicode_motorola</a> | "UCS-2BE"     | PHP\_INI\_ALL | 自 PHP 4.3.0 起可用。 |
| <a href="/exif/setup.html#" class="link">exif.decode_unicode_intel</a>    | "UCS-2LE"     | PHP\_INI\_ALL | 自 PHP 4.3.0 起可用。 |
| <a href="/exif/setup.html#" class="link">exif.encode_jis</a>              | ""            | PHP\_INI\_ALL | 自 PHP 4.3.0 起可用。 |
| <a href="/exif/setup.html#" class="link">exif.decode_jis_motorola</a>     | "JIS"         | PHP\_INI\_ALL | 自 PHP 4.3.0 起可用。 |
| <a href="/exif/setup.html#" class="link">exif.decode_jis_intel</a>        | "JIS"         | PHP\_INI\_ALL | 自 PHP 4.3.0 起可用。 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`exif.encode_unicode` <span class="type">string</span>  
*exif.encode\_unicode* 定义了 UNICODE 用户注释被处理的字符集。默认为
ISO-8859-15，可用于大多数非亚洲国家。本设置可以为空或者必须为一个
mbstring 所支持的编码。如果为空，则使用当前 mbstring 内部使用的编码。

`exif.decode_unicode_motorola` <span class="type">string</span>  
*exif.decode\_unicode\_motorola* 定义了 Unicode
编码的用户注释的图像内部字符集，如果图像是摩托罗拉字节顺序（big-endian）的话。本设置不能为空但可以指定一个
mbstring 支持的编码列表。默认为 UCS-2BE。

`exif.decode_unicode_intel` <span class="type">string</span>  
*exif.decode\_unicode\_intel* 定义了 Unicode
编码的用户注释的图像内部字符集，如果图像是英特尔字节顺序（little-endian）的话。本设置不能为空但可以指定一个
mbstring 支持的编码列表。默认为 UCS-2LE。

`exif.encode_jis` <span class="type">string</span>  
*exif.encode\_jis* 定义了 JIS
用户注释被处理的字符集。默认为空值，迫使函数使用当前 mbstring
使用的内部编码。

`exif.decode_jis_motorola` <span class="type">string</span>  
*exif.decode\_jis\_motorola* 定义了 JIS
编码的用户注释的图像内部字符集，如果图像是摩托罗拉字节顺序（big-endian）的话。本设置不能为空但可以指定一个
mbstring 支持的编码列表。默认为 JIS。

`exif.decode_jis_intel` <span class="type">string</span>  
*exif.decode\_jis\_intel* 定义了 JIS
编码的用户注释的图像内部字符集，如果图像是英特尔字节顺序（litle-endian）的话。本设置不能为空但可以指定一个
mbstring 支持的编码列表。默认为 JIS。

资源类型
--------

此扩展没有定义资源类型。
