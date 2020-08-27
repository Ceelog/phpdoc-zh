安装／配置
==========

**目录**

-   [需求](/fdf/setup.html#需求)
-   [安装](/fdf/setup.html#安装)
-   [运行时配置](/fdf/setup.html#运行时配置)
-   [资源类型](/fdf/setup.html#资源类型)

需求
----

You need the FDF toolkit SDK available from
<a href="http://www.adobe.com/devnet/acrobat/fdftoolkit.html" class="link external">» http://www.adobe.com/devnet/acrobat/fdftoolkit.html</a>.
As of PHP 4.3.0 you need at least SDK version 5.0. The FDF toolkit
library is available in binary form only, platforms supported by Adobe
are Win32, Linux, Solaris and AIX.

安装
----

此扩展被认为已无人维护及已消亡。然而，此扩展的源代码还可在 PECL SVN
找到：
<a href="https://svn.php.net/viewvc/pecl/fdf" class="link external">» https://svn.php.net/viewvc/pecl/fdf</a>.

This extension is no longer bundled with PHP as of PHP 5.3.0.

> **Note**: <span class="simpara"> If you run into problems configuring
> PHP with fdftk support, check whether the header file `fdftk.h` and
> the library `libfdftk.so` are at the right place. The **configure**
> script supports both the directory structure of the FDF SDK
> distribution and the usual `DIR/include` / `DIR/lib` layout, so you
> can point it either directly to the unpacked distribution directory or
> put the header file and the appropriate library for your platform into
> e.g. `/usr/local/include` and `/usr/local/lib` and configure with
> **--with-fdftk=/usr/local**. </span>

> **Note**: **Note to Win32 Users**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `fdftk.dll`

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

Most fdf functions require a `fdf` resource as their first parameter. A
`fdf` resource is a handle to an opened fdf file. `fdf` resources may be
obtained using <span class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> and <span
class="function">fdf\_open\_string</span>.
