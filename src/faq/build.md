编译问题
========

本节汇集了大多数编译时出现的常见错误。

1.  [我用匿名 GIT 服务得到了最新版的 PHP，但是里面没有 configure
    脚本！](#faq.build.configure)
2.  [我在配置 PHP 和 Apache 一起工作时遇到了问题。说没找到
    httpd.h，但这个文件明明就在那里！](#faq.build.configuring)
3.  [当运行 PHP 配置时（ ./configure），遇到类似如下的问题： checking
    lex output file root... ./configure: lex: command not found
    configure: error: cannot find output from lex; giving
    up](#faq.build.lex)
4.  [当试图启动 Apache 时，得到类似如下错误信息： fatal: relocation
    error: file /path/to/libphp4.so: symbol ap\_block\_alarms:
    referenced symbol not found](#faq.build.apache-sharedcore)
5.  [当运行 configure 时，报告说找不到头文件或 GD 库或
    gdbm，或其它的什么包！](#faq.build.not-found)
6.  [当编译 language-parser.tab.c文件时，报错说 yytname
    undeclared。](#faq.build.yytname)
7.  [当我运行
    make时，看上去一切正常，可当连接最后的程序时报告说找不到某些文件而失败了。](#faq.build.link)
8.  [当连接 PHP 时，报告说有一些未定义的引用。](#faq.build.undefined)
9.  [我不知道怎样把 PHP 和 Apache 1.3 一起编译。](#faq.build.apache)
10. [我按照所有的步骤在 UNIX 下安装了PHP 的 Apache 模块版本，但我的 PHP
    脚本被显示在浏览器中或者提示保存此文件。](#faq.build.not-running)
11. [说要用：
    --activate-module=src/modules/php4/libphp4.a，但是此文件根本不存在，于是我改成了
    --activate-module=src/modules/php4/libmodphp4.a，结果不行。怎么回事？](#faq.build.activate-module)
12. [当我用 --activate-module=src/modules/php4/libphp4.a试着把 PHP
    编译成 Apache 的静态模块时，报告说我的编译器不服从 ANSI
    标准。](#faq.build.ansi)
13. [当我用 --with-apxs编译 PHP 时得到奇怪的错误信息。](#faq.build.apxs)
14. [在 make的过程中，在 microtime 中出错，还有很多
    RUSAGE\_之类的东西。](#faq.build.microtime)
15. [当带 MySQL 编译 PHP 时，可以正确地运行configure，但是在
    make的过程中出现了类似以下的错误信息： ext/mysql/ libmysqlclient
    /my\_tempnam.o(.text+0x46): In function my\_tempnam':
    /php4/ext/mysql/ libmysqlclient /my\_tempnam.c:103: the use of
    tempnam' is dangerous, better use
    mkstemp'，这是怎么回事](#faq.build.mysql.tempnam)
16. [我想升级我的 PHP。上哪里找到我用来配置目前的 PHP 的
    ./configure的参数呢？](#faq.build.upgrade)
17. [和 GD 库一起编译 PHP
    时，要么给出一个奇怪的编译错误，要么在运行时出现
    segfaults。](#faq.build.gdlibs)
18. [当编译 PHP 时我看到一些随机的错误，好像死了。我用的是
    Solaris，不知道有没有关系。](#faq.installation.needgnu)

**我用匿名 GIT 服务得到了最新版的 PHP，但是里面没有 configure 脚本！**  
你必须安装有 GNU autoconf 包，这样才可以从 `configure.in`生成 configure
脚本。从 GIT 服务中得到源程序后只要在最高层的目录中运行
**./buildconf**即可。（同时要注意，除非你用了
*--enable-maintainer-mode*选项来运行 **configure**，否则即使
`configure.in`文件更新了，configure 脚本也不会自动重新生成。所以当你发现
`configure.in`文件更新了时要确保手工重新生成 configure
脚本。有一个症状是在 configure 之后或者运行 `config.status`时在 Makefile
中寻找类似 @VARIABLE@ 的东西。）

<!-- -->

**我在配置 PHP 和 Apache 一起工作时遇到了问题。说没找到 `httpd.h`，但这个文件明明就在那里！**  
你需要告诉 configure/setup 脚本你的 Apache
源程序最上层的目录位置。这意味着你需要这样指定
**--with-apache=/path/to/apache**而 *不是*这样
**--with-apache=/path/to/apache/src**。

**当运行 PHP 配置时（ *./configure*），遇到类似如下的问题：**

checking lex output file root... ./configure: lex: command not found
configure: error: cannot find output from lex; giving up

请认真阅读 PHP 的
<a href="/install/unix.html" class="link">安装</a>说明，并注意要编译 PHP
需要同时安装 flex 和 bison。根据设置的不同，可以从源代码编译 bison 和
flex，要么通过已编译好的发行包，例如 RPM。

**当试图启动 Apache 时，得到类似如下错误信息：**

fatal: relocation error: file /path/to/libphp4.so: symbol
ap\_block\_alarms: referenced symbol not found

该错误通常在 Apache 的核心程序被编译为共享用途的 DSO
库时发生。请尝试重新配置 Apache，确保至少使用了如下参数：

--enable-shared=max --enable-rule=SHARED\_CORE

更多信息，请阅读 Apache 顶层目录的 `INSTALL`文件或者 Apache 的
<a href="http://httpd.apache.org/docs/current/dso.html" class="link external">» DSO 手册</a>。

**当运行 configure 时，报告说找不到头文件或 GD 库或 gdbm，或其它的什么包！**  
可以通过指定附加的选项让 configure
脚本在非标准的路径中寻找头文件和库并传递给 C 预处理器和连接器，例如：

        CPPFLAGS=-I/path/to/include LDFLAGS=-L/path/to/library ./configure

如果用 csh 的变种作为你的登录 shell（为什么？），那就是：

        env CPPFLAGS=-I/path/to/include LDFLAGS=-L/path/to/library ./configure

<!-- -->

**当编译 `language-parser.tab.c`文件时，报错说 *yytname undeclared*。**  
需要更新 Bison 的版本。最新版本在
<a href="http://www.gnu.org/software/bison/bison.html" class="link external">» http://www.gnu.org/software/bison/bison.html</a>。

<!-- -->

**当我运行 **make**时，看上去一切正常，可当连接最后的程序时报告说找不到某些文件而失败了。**  
一些旧版本的 make 没有正确将 functions
目录下编译后的文件放到同一个目录下。试试运行 **cp \*.o
functions**然后再运行
**make**看看有没有什么帮助。如果成功了，那你确实需要更新到最新版的 GNU
make。

<!-- -->

**当连接 PHP 时，报告说有一些未定义的引用。**  
看看连接的这一行命令，确认所有适当的库都包括在最后了。通常可能漏掉了“-ldl”和你包括的任何数据库支持所需要的库。

一些人也报告说在和 Apache 连接时他们不得不紧接着
`libphp4.a`之后加上“-ldl”。

<!-- -->

**我不知道怎样把 PHP 和 Apache 1.3 一起编译。**  
这其实很简单。小心地照着以下步骤来：

-   <span class="simpara">从
    <a href="http://httpd.apache.org/download.cgi" class="link external">» http://httpd.apache.org/download.cgi</a>下载最新版的
    Apache 1.3。</span>
-   <span class="simpara">解压缩到某处，例如
    `/usr/local/src/apache-1.3`。</span>
-   <span class="simpara">编译 PHP，先运行 **./configure
    --with-apache=/\<path\>/apache-1.3**（用你 apache-1.3
    所在的真实路径替换掉 \<path\>。）</span>
-   <span class="simpara">输入 **make**接着是 **make install**来编译 PHP
    并把必要的文件拷贝到 Apache 的源程序目录树中。</span>
-   <span class="simpara">改变当前目录到
    `/<path>/apache-1.3/src`目录并编辑 `Configuration`文件。添加这一行：
    *AddModule modules/php4/libphp4.a*。</span>
-   <span class="simpara">输入 **./configure**接着是 *make*。</span>
-   <span class="simpara">你现在应该有一个包括 PHP 支持的 httpd
    可执行程序了！</span>

*注意：*也可以用新的 Apache *./configure*脚本。参见 Apache 发行包中
*README.configure*文件中的说明。也看看 PHP 发行包中的 `INSTALL`文件。

<!-- -->

**我按照所有的步骤在 UNIX 下安装了PHP 的 Apache 模块版本，但我的 PHP 脚本被显示在浏览器中或者提示保存此文件。**  
这说明 PHP 模块出于某些原因没有被调用。在寻求更多帮助前先检查三件事：

-   <span class="simpara">确认你运行的 httpd 程序就是你刚刚编译的新
    httpd 程序。运行： */path/to/binary/httpd -l*</span> <span
    class="simpara">如果你没看到
    `mod_php4.c`被列出来那你就没有运行对程序。找到并正确安装程序。</span>
-   <span class="simpara">确认你在 *Apache .conf*文件中加入了正确的 Mime
    类型。应该是： *AddType application/x-httpd-php .php* </span> <span
    class="simpara">也确认 AddType 这一行没有隐藏在 \<Virtualhost\> 或者
    \<Directory\>
    块中，这可能会造成你的测试脚本所在位置没有被应用到此设置。</span>
-   <span class="simpara">最后，Apache 1.2 和 Apache 1.3
    之间默认配置文件的位置改变了。你要确认你添加 AddType
    行的文件就是实际上用的。你可以在你的 `httpd.conf`
    中添加一个明显的语法错误或者其它明显修改，这可以告诉你是否读取了正确的文件。</span>

<!-- -->

**说要用： *--activate-module=src/modules/php4/libphp4.a*，但是此文件根本不存在，于是我改成了 *--activate-module=src/modules/php4/libmodphp4.a*，结果不行。怎么回事？**  
注意 `libphp4.a`文件本来就不该存在，apache 进程将创建它！

<!-- -->

**当我用 *--activate-module=src/modules/php4/libphp4.a*试着把 PHP 编译成 Apache 的静态模块时，报告说我的编译器不服从 ANSI 标准。**  
这是一个 Apache 误报的错误信息，在新的版本中已经修正了。

<!-- -->

**当我用 **--with-apxs**编译 PHP 时得到奇怪的错误信息。**  
这里要检查三件事。首先，出于某些原因当 Apache 生成 apxs Perl
脚本时，有时没有正确的编译和标记变量就结束了。找到你的 apxs 脚本（用命令
**which apxs**），有时会在 `/usr/local/apache/bin/apxs`或者
`/usr/sbin/apxs`。打开并检查类似如下的行：

    my $CFG_CFLAGS_SHLIB  = ' ';          # substituted via Makefile.tmpl
    my $CFG_LD_SHLIB      = ' ';          # substituted via Makefile.tmpl
    my $CFG_LDFLAGS_SHLIB = ' ';          # substituted via Makefile.tmpl

如果你看到这几行，那问题就在这里。它们可能包含了仅仅空格或者其它不正确的值，例如“q()”。改成这样：

    my $CFG_CFLAGS_SHLIB  = '-fpic -DSHARED_MODULE'; # substituted via Makefile.tmpl
    my $CFG_LD_SHLIB      = 'gcc';                   # substituted via Makefile.tmpl
    my $CFG_LDFLAGS_SHLIB = q(-shared);              # substituted via Makefile.tmpl

第二个可能的问题仅可能在在 Red Hat 6.1 和 6.2 中发生。Red Hat 发行的
apxs 脚本坏了。查找这一行：

    my $CFG_LIBEXECDIR    = 'modules';         # substituted via APACI install

如果你看到上面这一行，改成这样：

    my $CFG_LIBEXECDIR    = '/usr/lib/apache'; # substituted via APACI install

最后，如果你重新配置或者重装了 Apache，在 **./configure**之后和
**make**之前增加一个 **make clean**命令。

<!-- -->

**在 **make**的过程中，在 microtime 中出错，还有很多 *RUSAGE\_*之类的东西。**  
如果 **make**时遇到类似这样的问题：

    microtime.c: In function `php_if_getrusage':
    microtime.c:94: storage size of `usg' isn't known
    microtime.c:97: `RUSAGE_SELF' undeclared (first use in this function)
    microtime.c:97: (Each undeclared identifier is reported only once
    microtime.c:97: for each function it appears in.)
    microtime.c:103: `RUSAGE_CHILDREN' undeclared (first use in this function)
    make[3]: *** [microtime.lo] Error 1
    make[3]: Leaving directory `/home/master/php-4.0.1/ext/standard'
    make[2]: *** [all-recursive] Error 1
    make[2]: Leaving directory `/home/master/php-4.0.1/ext/standard'
    make[1]: *** [all-recursive] Error 1
    make[1]: Leaving directory `/home/master/php-4.0.1/ext'
    make: *** [all-recursive] Error 1

你的系统坏了。你需要安装一个符合你的 glibc 的 glibc-devel 包来修复
`/usr/include`中的文件。这和 PHP
绝对没有任何关系。要证实这一点，试试这个简单的测试：

    $ cat >test.c <<X
    #include <sys/resource.h>
    X
    $ gcc -E test.c >/dev/null

如果出现错误，那你就知道头文件坏了。

<!-- -->

**当带 MySQL 编译 PHP 时，可以正确地运行configure，但是在 *make*的过程中出现了类似以下的错误信息： *ext/mysql/ libmysqlclient /my\_tempnam.o(.text+0x46): In function my\_tempnam': /php4/ext/mysql/ libmysqlclient /my\_tempnam.c:103: the use of tempnam' is dangerous, better use mkstemp'*，这是怎么回事**  
首先，我们需要认识到这只是个 *警告*，而非致命错误。由于这条信息通常是在
*make*的最后输出的，所以看起来它可能像是一个致命错误，但实际上不是。当然，如果将编译器设置成遇见警告信息时停止，则这也可以算是致命错误。另外值得一提的是，MySQL
的支持是默认打开的。

> **Note**:
>
> 自 PHP 4.3.2 起，你将在编译（make）结束后看到下面的文字：
>
>   
> Build complete.  
> (It is safe to ignore warnings about tempnam and tmpnam).  

<!-- -->

**我想升级我的 PHP。上哪里找到我用来配置目前的 PHP 的 **./configure**的参数呢？**  
要么在你用来编译当前的 PHP 的源码树中查看 config.nice
文件，如果没有，只要运行此脚本：

``` php
<?php phpinfo(); ?>
```

在输出的顶端显示了用来配置此 PHP 的 **./configure**参数。

<!-- -->

**和 GD 库一起编译 PHP 时，要么给出一个奇怪的编译错误，要么在运行时出现 segfaults。**  
确保你的 GD 库和 PHP 在连接时使用了用同样的支持库（例如 libpng）。

<!-- -->

**当编译 PHP 时我看到一些随机的错误，好像死了。我用的是 Solaris，不知道有没有关系。**  
当编译 PHP 时使用非 GNU 的工具会导致问题。确保使用 GNU
工具来确保能够正确编译 PHP。例如，在 Solaris 下面不论使用 SunOS BSD
兼容或者 Solaris 版本的 *sed*都不行，但是使用 GNU 或者 Sun POSIX (xpg4)
版本的 *sed*就可以。相关连接：
<a href="http://www.gnu.org/software/sed/sed.html" class="link external">» GNU sed</a>，
<a href="http://www.gnu.org/software/flex/flex.html" class="link external">» GNU flex</a>，
<a href="http://www.gnu.org/software/bison/bison.html" class="link external">» GNU bison</a>。
