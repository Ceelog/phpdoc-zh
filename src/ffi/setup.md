安装／配置
==========

**目录**

-   [需求](/ffi/setup.html#需求)
-   [安装](/ffi/setup.html#安装)
-   [运行时配置](/ffi/setup.html#运行时配置)
-   [资源类型](/ffi/setup.html#资源类型)

需求
----

This extension requires the
<a href="https://sourceware.org/libffi/" class="link external">» libffi library</a>
to be installed.

安装
----

To enable the FFI extension, PHP has to be configured with
**--with-ffi**.

Windows users have to include `php_ffi.dll` into `php.ini` to enable the
FFI extension.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                    | 默认      | 可修改范围       | 更新日志 |
|---------------------------------------------------------|-----------|------------------|----------|
| <a href="/ffi/setup.html#" class="link">ffi.enable</a>  | "preload" | PHP\_INI\_SYSTEM |          |
| <a href="/ffi/setup.html#" class="link">ffi.preload</a> | ""        | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`ffi.enable` <span class="type">string</span>  
Allows enabling (*"true"*) or disabling (*"false"*) FFI API usage, or
restricting it only to the CLI SAPI and preloaded files (*"preload"*).

The FFI API restrictions only affect the <span
class="classname">FFI</span> class, but not overloaded functions of
<span class="classname">FFI\\CData</span> objects. This means that it is
possible to create some <span class="classname">FFI\\CData</span>
objects in preloaded files, and then to use these directly in PHP
scripts.

`ffi.preload` <span class="type">string</span>  
Allows preloading of FFI bindings during startup, which is not possible
with <span class="methodname">FFI::load</span> if
<a href="/opcache/setup.html#" class="link">opcache.preload_user</a> is
set. This directive accepts a **`DIRECTORY_SEPARATOR`** delimited list
of filenames. The preloaded bindings can be accessed by calling <span
class="methodname">FFI::scope</span>.

资源类型
--------

此扩展没有定义资源类型。
