获取 PHP
========

本章包括 PHP 下载地址以及操作系统相关问题的详细资料。

1.  [PHP 可以从哪里得到？](#faq.obtaining.where)
2.  [有预先编译好的可执行版本吗？](#faq.obtaining.precompiled)
3.  [编译一些可选的 PHP
    扩展库所需的库文件可以从哪里得到？](#faq.obtaining.optional)
4.  [怎样使这些库起作用？](#faq.obtaining.how)
5.  [我在 Windows 机器中从 SVN 里得到了最新版的 PHP
    源代码，需要什么去编译它？](#faq.obtaining.compileNT)
6.  [哪里可以找到 browscap.ini 文件？](#faq.obtaining.browscap)

**PHP 可以从哪里得到？**  
可以从任何一个 PHP 网络成员的站点下载 PHP。这些信息在
<a href="https://www.php.net/" class="link external">» https://www.php.net/</a>。还可以通过匿名
SVN 得到绝对是最新版的源程序。更多信息请访问 \[broken link\]。

<!-- -->

**有预先编译好的可执行版本吗？**  
我们只为 Windows 系统提供了预编译的可执行文件，因为我们没法为每个主流的
Linux/Unix 平台编译每一种扩展库组和的 PHP。同样注意，如今很多 Linux
的发行版本已经内置了 PHP。Windows 可执行文件可以从我们的
<a href="https://www.php.net/downloads.php" class="link external">» 下载</a>页面下载，至于
Linux 可执行文件，请访问你的 Linux 发布商的站点。

<!-- -->

**编译一些可选的 PHP 扩展库所需的库文件可以从哪里得到？**  
> **Note**: <span class="simpara">有 \*
> 号标记的不是多线程的库，不应该用作多线程 Windows web
> 服务器（IIS，Netscape）的服务器模块。不过这在 Unix 环境下没有关系。
> </span>

-   <span class="simpara">
    <a href="ftp://ftp.openldap.org/pub/OpenLDAP/openldap-stable/" class="link external">» LDAP (Unix)</a>
    </span>
-   <span class="simpara">
    <a href="https://wiki.mozilla.org/LDAP_C_SDK" class="link external">» LDAP (Unix/Win)</a>:
    Mozilla Directory (LDAP) SDK</span>
-   <span class="simpara">
    <a href="http://www.bind9.net/download-openldap/" class="link external">» 免费 LDAP 服务器</a>
    </span>
-   <span class="simpara">
    <a href="http://www.sleepycat.com/" class="link external">» Berkeley DB2 (Unix/Win)</a>:
    http://www.sleepycat.com/.</span>
-   <span class="simpara">
    <a href="http://www.net-snmp.org/" class="link external">» SNMP* (Unix):</a>
    </span>
-   <span class="simpara">
    <a href="http://www.libgd.org/" class="link external">» GD* (Unix/Win)</a>
    </span>
-   <span class="simpara">
    <a href="http://www.hughes.com.au/" class="link external">» mSQL* (Unix)</a>
    </span>
-   <span class="simpara">
    <a href="http://www.postgresql.org/" class="link external">» PostgreSQL (Unix)</a>
    </span>
-   <span class="simpara">
    <a href="https://www.washington.edu/imap/" class="link external">» IMAP* (Win/Unix)</a>
    </span>
-   <span class="simpara">
    <a href="http://www.sybase.com/" class="link external">» Sybase-CT* (Linux, libc5)</a>：内置</span>
-   <span class="simpara">
    <a href="http://www.freetype.org/" class="link external">» FreeType (libttf):</a>
    </span>
-   <span class="simpara">
    <a href="http://www.zlib.net/" class="link external">» ZLib (Unix/Win32)</a>
    </span>
-   <span class="simpara">
    <a href="http://www.jclark.com/xml/expat.html" class="link external">» expat XML parser (Unix/Win32)</a>
    </span>
-   <span class="simpara">
    <a href="http://www.pdflib.com/products/pdflib-family/" class="link external">» PDFLib</a>
    </span>
-   <span class="simpara">
    <a href="http://mcrypt.sourceforge.net/" class="link external">» mcrypt</a>
    </span>
-   <span class="simpara">
    <a href="http://mhash.sourceforge.net/" class="link external">» mhash</a>
    </span>
-   <span class="simpara">
    <a href="ftp://sunsite.unc.edu/pub/Linux/libs/graphics/" class="link external">» t1lib</a>
    </span>
-   <span class="simpara">
    <a href="http://dmalloc.com/" class="link external">» dmalloc</a>
    </span>
-   <span class="simpara">
    <a href="http://aspell.net/" class="link external">» aspell</a>
    </span>
-   <span class="simpara">
    <a href="http://cnswww.cns.cwru.edu/~chet/readline/rltop.html" class="link external">» readline</a>
    </span>

<!-- -->

**怎样使这些库起作用？**  
需要按照这些库提供的说明进行。一些库可以在运行 PHP
的“configure”时自动检测到（例如 GD 库），其它的必需用“
*--with-EXTENSION*”选项来激活。运行“ *configure
--help*”来得到完整的列表。

<!-- -->

**我在 Windows 机器中从 SVN 里得到了最新版的 PHP 源代码，需要什么去编译它？**  
首先，需要 Microsoft Visual C++ v6（v5 也许也行，不过我们是用 v6
编译的），此外还需要一些支持文件。参见手册中的
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 下编译 PHP 源代码</a>一节。

<!-- -->

**哪里可以找到 browscap.ini 文件？**  
可以从
<a href="http://browscap.org/" class="link external">» http://browscap.org/</a>得到一个
`browscap.ini`文件。
