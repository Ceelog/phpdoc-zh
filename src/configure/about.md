核心配置选项列表
----------------

下面是 PHP 的 `configure` 脚本使用的部分选项的列表，用于类 Unix
环境的编译。大部分配置选项在扩展模块参考页面适当的位置列出，而不是在这里。要查看所有可用配置选项的列表，在运行
**autoconf** 命令后在 PHP 的源代码目录运行 **./configure
--help**（参见<a href="/install.html" class="link">安装与配置</a>一章）。也可以阅读
<a href="http://www.airs.com/ian/configure/" class="link external">» GNU configure</a>
文档以获得有关 **configure** 命令的更详细信息，例如 *--prefix=PREFIX*。

> **Note**:
>
> 这些选项只用在编译的时候。如果想要修改 PHP
> 的运行时配置，请阅读<a href="/configuration.html" class="link">运行时配置</a>。

-   <span class="simpara">
    <a href="/configure/about.html#configure.options.misc" class="link">杂项</a>
    </span>
-   <span class="simpara">
    <a href="/configure/about.html#configure.options.php" class="link">PHP 行为</a>
    </span>
-   <span class="simpara">
    <a href="/configure/about.html#configure.options.servers" class="link">服务器</a>
    </span>

### PHP 配置选项

#### 杂项选项

**--enable-debug**  
编译时加入调试符号。

**--with-layout=TYPE**  
设置被安装文件的布局。TYPE 是 PHP（默认）或 GNU。

**--with-pear=DIR**  
在 DIR（默认为 PREFIX/lib/php）中安装 PEAR。

**--without-pear**  
不安装 PEAR。

**--enable-sigchild**  
使用 PHP 自带的 SIGCHLD 处理器。

**--disable-rpath**  
禁用在搜索路径中传递其他运行库。

**--enable-libgcc**  
启用 libgcc 的精确链接。

**--enable-php-streams**  
包含试验性的 PHP 流。不要使用此选项，除非是要测试代码！

**--with-zlib-dir\[=DIR\]**  
定义 zlib 的安装目录。

**--with-tsrm-pthreads**  
使用 POSIX 线程（默认）。

**--enable-shared\[=PKGS\]**  
编译共享库 \[default=yes\]。

**--enable-static\[=PKGS\]**  
编译静态库 \[default=yes\]。

**--enable-fast-install\[=PKGS\]**  
为快速安装优化 \[default=yes\]。

**--with-gnu-ld**  
假设 C 编译器使用 GNU ld \[default=no\]。

**--disable-libtool-lock**  
避免锁死（可能破坏并联的编译）。

**--with-pic**  
尝试仅使用 PIC/非 PIC 对象 \[default=use both\]。

**--enable-memory-limit**  
编译内存限制支持功能。(自PHP 5.2.1开始不可用，默认enable)

**--disable-url-fopen-wrapper**  
禁用 URL 形式的 fopen 封装协议。该协议允许通过 HTTP 或者 FTP 访问文件。
（自PHP5.2.5开始不可用）

**--enable-versioning**  
仅导出必须的符号。查看 INSTALL 文件以获得更多信息。

#### PHP 选项

**--enable-maintainer-mode**  
对偶然安装一下的情形启用此选项，使得不检查编译规则和依赖关系。

**--with-config-file-path=PATH**  
设置 `php.ini` 的搜索路径。默认为 PREFIX/lib。

**--enable-safe-mode**  
默认启用安全模式。

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

**--with-exec-dir\[=DIR\]**  
在安全模式时仅允许在 DIR 目录中执行。默认目录为 /usr/local/php/bin。

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

**--enable-magic-quotes**  
默认启用 magic quotes。

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

**--disable-short-tags**  
默认禁用短形式的开始标签 \<? 。

**--enable-zend-multibyte**  
在词法与语法分析时允许多字节编码被执行。如果在编译PHP时使用了这个选项，就能够在
<a href="/control-structures/declare.html" class="link">declare</a>
结构中使用
<a href="/control-structures/declare.html#control-structures.declare.encoding" class="link">encoding</a>指令。

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

**--with-libdir**  
指定Uxin系统库文件目录用于构建 PHP。 对于64位系统, 需要指定 *lib64*
目录,比如*--with-libdir=lib64*

#### SAPI 选项

下面的列表包含 PHP 可用的SAPI（*服务器应用编程接口*）。

**--with-aolserver=DIR**  
指定 AOLserver 的安装路径。

**--with-apxs\[=FILE\]**  
编译共享的 Apache 模块。FILE 是可选的 Apache apxs 工具的路径，默认指向
apxs。请确认指定的 apxs 已经安装在服务器中，并且它不是 Apache
源码包中的那个 apxs。

**--with-apache\[=DIR\]**  
编译静态 Apache 模块。DIR 是 Apache 编译目录的顶层，默认为
`/usr/local/apache`。

**--with-mod\_charset**  
启用 mod\_charset 的转换表（俄文的 Apache 使用）。

**--with-apxs2\[=FILE\]**  
编译共享的 Apache 2.0 模块。FILE 是可选的 Apache apxs
工具的路径，默认指向 apxs。

**--with-caudium=DIR**  
为使用 Caudium 编译 PHP 为一个 Pike 模块。DIR 是 Caudium
服务器目录，默认为 `/usr/local/caudium/server`。

**--disable-cli**  
PHP 4.3.0 之后的版本有效。禁止编译 PHP 的 CLI 版本（使用它将同时强制使用
<a href="/configure/about.html#configure.without-pear" class="link">--without-pear</a>
选项）。更多信息请查考
<a href="/features/commandline.html" class="link">PHP 的命令行模式</a>。

**--enable-embed\[=TYPE\]**  
启用编译嵌入的 SAPI 库。TYPE 或者为 *shared* 或者为 *static*，默认为
*shared*。PHP 4.3.0 之后的版本有效。

**--with-fhttpd\[=DIR\]**  
编译 fhttpd 模块。DIR 是 fhttpd 源代码目录，默认为
`/usr/local/src/fhttpd`。PHP 4.3.0 及以后的版本此选项不再有效。

**--with-isapi=DIR**  
为 Zeus 服务器以 ISAPI 模块方式编译 PHP。

**--with-nsapi=DIR**  
指定 Netscape/iPlanet/SunONE 的安装目录。

**--with-phttpd=DIR**  
还没有信息。

**--with-pi3web=DIR**  
为 Pi3Web 服务器编译 PHP 模块。

**--with-roxen=DIR**  
以 Pike 模块方式编译 PHP。DIR 是 Roxen 的根目录，默认为
`/usr/local/roxen/server`。

**--enable-roxen-zts**  
使用 Zend 线程安全（ZTS）编译 Roxen 模块。

**--with-servlet\[=DIR\]**  
包含 servlet 支持。DIR 是 JSDK 的安装目录。此 SAPI 要求 java
扩展必须作为共享模块编译到 PHP 中。

**--with-thttpd=SRCDIR**  
编译 PHP 为 thttpd 模块。

**--with-tux=MODULEDIR**  
编译 PHP 为 TUX 模块（仅在 Linux 下有效）。

**--with-webjames=SRCDIR**  
编译 PHP 为 WebJames 模块（仅在 RISC 操作系统中有效）。

**--disable-cgi**  
禁止编译 CGI 版本的 PHP。PHP 4.3.0 之后的版本有效。

PHP5.3.0起，这个选项会启用FastCGI，而在以前，必须使用*--enable-fastcgi*启用FastCGI。

**--enable-force-cgi-redirect**  
启用内部服务器重定向的安全检测。如果在 Apache 下使用 CGI 版本的
PHP，请启用该选项。

PHP
5.3.0起，默认有效并不再存在。要禁用此功能,设置<a href="/ini/core.html#ini.cgi.force-redirect" class="link">cgi.force_redirect</a>
ini指令为 *0*.

**--enable-discard-path**  
如果启用该选项，PHP CGI 目录可以安全的放在 web
目录树的外面，人们无法避开 `.htaccess` 的安全限制。

PHP 5.3.0起，默认禁用并不在存在。要启用此功能，设置 cgi-redirect
ini指令为*1*。

**--enable-fastcgi**  
如果启用，CGI 模块将被编译为支持 FastCGI。PHP 4.3.0 之后的版本有效。

PHP 5.3.0起，此参数不再存在，并使用 *--enable-cgi*替代。

**--disable-path-info-check**  
如果该选项被禁用，例如 `/info.php/test?a=b` 形式的路径将不能工作。PHP
4.3.0 之后的版本有效。更多信息请参考
<a href="http://httpd.apache.org/docs/current/mod/core.html#acceptpathinfo" class="link external">» Apache 手册</a>。
