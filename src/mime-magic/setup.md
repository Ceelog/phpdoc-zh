安装／配置
==========

**目录**

-   [需求](/mime-magic/setup.html#需求)
-   [安装](/mime-magic/setup.html#安装)
-   [运行时配置](/mime-magic/setup.html#运行时配置)
-   [资源类型](/mime-magic/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

**Warning**

Mimetype extensions has been removed from PHP 5.3.0 in favor of
<a href="/book/fileinfo.html" class="link">Fileinfo</a>.

You must compile PHP with the configure switch **--with-mime-magic** to
get support for mime-type functions. The extension needs a copy of the
simplified `magic` file that is distributed with the Apache httpd.

> **Note**:
>
> This extension is not capable of handling the fully decorated `magic`
> file that generally comes with standard Linux distro's and is supposed
> to be used with recent versions of `file` command.

> **Note**: **Note to Win32 Users**  
>
> In order to use this module on a Windows environment, you must set the
> path to the bundled `magic.mime` file in your `php.ini`.
>
> **示例 \#1 Setting the path to `magic.mime`**
>
>     mime_magic.magicfile = "$PHP_INSTALL_DIR\magic.mime"
>
> Remember to substitute the `$PHP_INSTALL_DIR` for your actual path to
> PHP in the above example. e.g. `c:\php`

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                    | 默认                      | 可修改范围       | 更新日志                   |
|-------------------------------------------------------------------------|---------------------------|------------------|----------------------------|
| <a href="/mime-magic/setup.html#" class="link">mime_magic.debug</a>     | "0"                       | PHP\_INI\_SYSTEM | Available since PHP 5.0.0. |
| <a href="/mime-magic/setup.html#" class="link">mime_magic.magicfile</a> | "/path/to/php/magic.mime" | PHP\_INI\_SYSTEM | Available since PHP 4.3.0. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`mime_magic.debug` <span class="type">bool</span>  
Enable/disable debugging.

`mime_magic.magicfile` <span class="type">string</span>  
The path to the magic.mime file.

资源类型
--------

此扩展没有定义资源类型。
