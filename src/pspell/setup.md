安装／配置
==========

**目录**

-   [需求](/pspell/setup.html#需求)
-   [安装](/pspell/setup.html#安装)
-   [运行时配置](/pspell/setup.html#运行时配置)
-   [资源类型](/pspell/setup.html#资源类型)

需求
----

To compile PHP with pspell support, you need the aspell library,
available from
<a href="http://aspell.net/" class="link external">» http://aspell.net/</a>.

安装
----

If you have the libraries needed add the **--with-pspell\[=dir\]**
option when compiling PHP.

> **Note**: **Note to Win32 Users**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `aspell-15.dll` from the `bin`
> folder of the aspell installation.
>
> Win32 support requires at least aspell version 0.50.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
