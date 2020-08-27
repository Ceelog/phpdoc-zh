安装／配置
==========

**目录**

-   [需求](/ldap/setup.html#需求)
-   [安装](/ldap/setup.html#安装)
-   [运行时配置](/ldap/setup.html#运行时配置)
-   [资源类型](/ldap/setup.html#资源类型)

需求
----

You will need to get and compile LDAP client libraries from either
<a href="ftp://ftp.openldap.org/pub/OpenLDAP/openldap-stable/" class="link external">» OpenLDAP</a>
or
<a href="http://www.bind9.net/download-openldap/" class="link external">» Bind9.net</a>
in order to compile PHP with LDAP support. For PHP 5.6 or newer you will
need OpenLDAP 2.4 or newer.

安装
----

LDAP support in PHP is not enabled by default. You will need to use the
**--with-ldap\[=DIR\]** configuration option when compiling PHP to
enable LDAP support. DIR is the LDAP base install directory. To enable
SASL support, be sure **--with-ldap-sasl\[=DIR\]** is used, and that
`sasl.h` exists on the system.

> **Note**: **Note to Win32 Users**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `libeay32.dll` and
> `ssleay32.dll`, or, as of OpenSSL 1.1 `libcrypto-*.dll` and
> `libssl-*.dll`

In order to use Oracle LDAP libraries, proper
<a href="/book/oci8.html#需求" class="link">Oracle environment</a> has
to be set.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                        | 默认 | 可修改范围       | 更新日志 |
|-------------------------------------------------------------|------|------------------|----------|
| <a href="/ldap/setup.html#" class="link">ldap.max_links</a> | "-1" | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`ldap.max_links` <span class="type">integer</span>  
The maximum number of LDAP connections per process.

资源类型
--------

Most LDAP functions operate on or return resources (e.g. <span
class="function">ldap\_connect</span> returns a positive LDAP link
identifier required by most LDAP functions).
