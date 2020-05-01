安装／配置
==========

**目录**

-   [需求](/com/setup.html#需求)
-   [安装](/com/setup.html#安装)
-   [运行时配置](/com/setup.html#运行时配置)
-   [资源类型](/com/setup.html#资源类型)

需求
----

COM functions are only available for the Windows version of PHP.

.Net support requires the .Net runtime.

安装
----

As of PHP 5.3.15 / 5.4.5, this extension requires `php_com_dotnet.dll`
to be enabled inside of `php.ini` in order to use these functions.
Previous versions of PHP enabled these extensions by default.

You are responsible for installing support for the various COM objects
that you intend to use (such as MS Word); we don't and can't bundle all
of those with PHP.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                       | 默认 | 可修改范围       | 更新日志                                            |
|----------------------------------------------------------------------------|------|------------------|-----------------------------------------------------|
| <a href="/com/setup.html#" class="link">com.allow_dcom</a>                 | "0"  | PHP\_INI\_SYSTEM | 自 PHP 4.0.5 起可用                                 |
| <a href="/com/setup.html#" class="link">com.autoregister_typelib</a>       | "0"  | PHP\_INI\_ALL    | 在 PHP 4 中是 PHP\_INI\_SYSTEM。自 PHP 4.1.0 起可用 |
| <a href="/com/setup.html#" class="link">com.autoregister_verbose</a>       | "0"  | PHP\_INI\_ALL    | 在 PHP 4 中是 PHP\_INI\_SYSTEM。自 PHP 4.1.0 起可用 |
| <a href="/com/setup.html#" class="link">com.autoregister_casesensitive</a> | "1"  | PHP\_INI\_ALL    | 在 PHP 4 中是 PHP\_INI\_SYSTEM。自 PHP 4.1.0 起可用 |
| <a href="/com/setup.html#" class="link">com.code_page</a>                  | ""   | PHP\_INI\_ALL    | 自 PHP 5.0.0 起可用                                 |
| <a href="/com/setup.html#" class="link">com.typelib_file</a>               | ""   | PHP\_INI\_SYSTEM | 自 PHP 4.0.5 起可用                                 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`com.allow_dcom`  
如果打开此选项，PHP 将被允许以一个 D-COM（Distributed
COM）客户方式操作并允许 PHP 脚本在远程服务器上实例化 COM 对象。

`com.autoregister_typelib`  
When this is turned on, PHP will attempt to register constants from the
typelibrary of objects that it instantiates, if those objects implement
the interfaces required to obtain that information. The case sensitivity
of the constants it registers is controlled by the
<a href="/com/setup.html#" class="xref"></a> configuration directive.

`com.autoregister_verbose`  
When this is turned on, any problems with loading a typelibrary during
object instantiation will be reported using the PHP error mechanism. The
default is off, which does not emit any indication if there was an error
finding or loading the type library.

`com.autoregister_casesensitive`  
When this is turned on (the default), constants found in auto-loaded
type libraries will be registered case sensitively. See <span
class="function">com\_load\_typelib</span> for more details.

`com.code_page`  
It controls the default character set code-page to use when passing
strings to and from COM objects. If set to an empty string, PHP will
assume that you want **`CP_ACP`**, which is the default system ANSI code
page.

If the text in your scripts is encoded using a different
encoding/character set by default, setting this directive will save you
from having to pass the code page as a parameter to the
<a href="/class/com.html" class="xref">com</a> class constructor. Please
note that by using this directive (as with any PHP configuration
directive), your PHP script becomes less portable; you should use the
COM constructor parameter whenever possible.

> **Note**: <span class="simpara"> This configuration directive was
> introduced with PHP 5. </span>

`com.typelib_file`  
When set, this should hold the path to a file that contains a list of
typelibraries that should be loaded on startup. Each line of the file
will be treated as the type library name and loaded as though you had
called <span class="function">com\_load\_typelib</span>. The constants
will be registered persistently, so that the library only needs to be
loaded once. If a type library name ends with the string *\#cis* or
*\#case\_insensitive*, then the constants from that library will be
registered case insensitively.

资源类型
--------

此扩展没有定义资源类型。
