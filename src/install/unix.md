Unix 系统下的安装
=================

**目录**

-   [Unix 系统下的 Apache 1.3.x](/install/unix/apache.html)
-   [Unix 系统下的 Apache 2.x](/install/unix/apache2.html)
-   [Unix 系统下的 Nginx 1.4.x](/install/unix/nginx.html)
-   [Unix 平台的 Lighttpd 1.4](/install/unix/lighttpd-14.html)
-   [Sun Solaris 上的 Sun、iPlanet 和 Netscape
    服务器](/install/unix/sun.html)
-   [Unix系统下的LiteSpeed、OpenLiteSpeed服务](/install/unix/litespeed.html)
-   [CGI 和命令行设置](/install/unix/commandline.html)
-   [针对 HP-UX 平台的安装提示](/install/unix/hpux.html)
-   [在 OpenBSD 系统下的安装](/install/unix/openbsd.html)
-   [针对 Solaris 的安装提示](/install/unix/solaris.html)
-   [Debian GNU/Linux 安装说明](/install/unix/debian.html)

本节将指导如何在 Unix 系统下安装和配置
PHP。在开始安装之前，请务必研究自己使用的系统和 web 服务器的相关章节。

在<a href="/install/general.html" class="link">安装前需要考虑的事项</a>一节提到，在本节主要以
web 为中心介绍 PHP 的设置。不过本节也会覆盖一些 PHP
命令行用法的设置方法。

在 Unix 平台下安装 PHP
有几种方法：使用配置和编译过程，或是使用各种预编译的包。本文主要针对配置和编译
PHP 的过程。很多 Unix
类系统都有包安装系统，可以用它来设置一个有着标准配置的
PHP。但是若需要与标准配置不同的功能（例如一个安全服务器，或者不同的数据库驱动扩展模块），可能需要编译
PHP 和／或 web
服务器。如果不熟悉编译软件，可以考虑搜索一下是否有人已经编译了包含所需要功能的预编译包。

编译所需的知识和软件：

-   <span class="simpara">基础的 Unix 技能（有能力操作“make”和一种 C
    语言编译器）</span>
-   <span class="simpara">一个 ANSI C 语言编译器</span>
-   <span class="simpara">一个 web 服务器</span>
-   <span class="simpara">任何模块特需的组件（例如 GD 和 PDF
    库等)</span>

直接从 Git 源文件或者自己修改过的包编译时可能需要：

-   <span class="simpara"> autoconf: 2.13+ (for PHP \< 5.4.0), 2.59+
    (for PHP \>= 5.4.0), 2.64+ (for PHP \>= 7.2.0) </span>
-   <span class="simpara"> automake: 1.4+ </span>
-   <span class="simpara"> libtool: 1.4.x+（除了 1.4.2） </span>
-   <span class="simpara"> re2c: 版本 0.13.4 或更高 </span>
-   <span class="simpara"> flex: 版本 2.5.4（PHP \<= 5.2） </span>
-   <span class="simpara"> bison: </span>
    -   <span class="simpara"> PHP 5.4: 1.28, 1.35, 1.75, 1.875, 2.0,
        2.1, 2.2, 2.3, 2.4, 2.4.1, 2.4.2, 2.4.3, 2.5, 2.5.1, 2.6, 2.6.1,
        2.6.2, 2.6.4 </span>
    -   <span class="simpara"> PHP 5.5: 2.4, 2.4.1, 2.4.2, 2.4.3, 2.5,
        2.5.1, 2.6, 2.6.1, 2.6.2, 2.6.3, 2.6.4, 2.6.5, 2.7 </span>
    -   <span class="simpara"> PHP 5.6: \>= 2.4, \< 3.0 </span>
    -   <span class="simpara"> PHP 7.0 - 7.3: 2.4 或更高 (包含 Bison
        3.x) </span>
    -   <span class="simpara"> PHP 7.4: \> 3.0 </span>

PHP 初始的配置和安装过程被 **configure**
脚本中一系列命令行选项控制。可以通过 **./configure --help** 命令了解 PHP
所有可用的编译选项及简短解释。本手册是分开对这些选项编写文档的。可在附录中找到
<a href="/configure/about.html" class="link">核心配置选项</a>，而扩展模块特定的配置选项分别在其函数参考页面中描述。

配置好 PHP 后，便可以开始编译模块和／或可执行文件。**make**
命令用来做这一工作。如果该命令执行失败而找不到原因，请参考
<a href="/install/problems.html" class="link">安装问题</a> 一节。

> **Note**:
>
> 某些 Unix 系统（类似 OpenBSD 和
> SELinux）出于安全考虑，可能不允许同时设置文件的写和执行的权限，又称为
> "PaX MPROTECT" 或 "W^X violation" 保护。但是 PCRE's JIT
> 又要求不能这么做，所以安装时可以参考
> <a href="/pcre/setup.html#安装" class="link">关闭 PCRE's JIT 支持</a>，或者在系统中将相关的二进制文件加入保护白名单。

> **Note**: <span class="simpara"> 目前还不支持 ARM 与 Android
> 工具链的交叉编译。 </span>
