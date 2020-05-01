安装常见问题
============

本章包括了安装 PHP 的常见问题。PHP 可以用于几乎任何操作系统（可能除了 OS
X 之前的 MacOS 之外），以及几乎任何 web 服务器。

要安装 PHP，请按照
<a href="/install.html" class="link">安装与配置</a>一章中的指示进行。

1.  [为什么不应该在实际运作环境中的 Apache2 中使用线程化的
    MPM？](#faq.installation.apache2)
2.  [Unix/Windows：应该上哪儿去找我的 php.ini
    文件？](#faq.installation.phpini)
3.  [Unix：我安装了 PHP，但每次我打开一个页面时，只得到一条“Document
    Contains No Data”消息！这是怎么回事？](#faq.installation.nodata)
4.  [Unix：我从 RPMS 安装了 PHP，但是 Apache 不处理 PHP
    页面！这是怎么回事？](#faq.installation.processing)
5.  [Unix：我从 RPMS 安装了 PHP
    3，但它没有把我需要的数据库支持编译进去！这是怎么回事？](#faq.installation.compile)
6.  [Unix：我给 Apache 加上了 FrontPage extensions 补丁，结果 PHP
    突然不工作了。PHP 和 Apache FrontPage extensions
    兼容吗？](#faq.installation.frontpage)
7.  [Unix/Windows：我已经安装了 PHP，但当我试着通过浏览器访问 PHP
    脚本时，得到了一个空白页面。](#faq.installation.blankscreen)
8.  [Unix/Windows：我已经安装了 PHP，但当我试着通过浏览器访问 PHP
    脚本时，得到了一个服务器的 500 错误。](#faq.installation.500error)
9.  [某些操作系统：我已经在不出错的情况下安装了 PHP，但当我试着启动
    Apache 时得到了一个未定义符号错误： \[mybox:user /src/php4\] root\#
    apachectl configtest apachectl: /usr/local/apache/bin/httpd
    Undefined symbols: \_compress
    \_uncompress](#faq.installation.undefinedsyms)
10. [Windows：我已经安装了 PHP，但当我试着通过浏览器访问 PHP
    脚本时，得到如下错误： cgi error: The specified CGI application
    misbehaved by not returning a complete set of HTTP headers. The
    headers it did return are:](#faq.installation.cgierror)
11. [Windows：我已经照着所有的说明做了，但还是不能让 PHP 和 IIS
    一起工作！](#faq.installation.phpandiis)
12. [当在 IIS，PWS，OmniHTTPD 或者 Xitami 中以 CGI 方式运行 PHP
    时，出现如下错误： Security Alert! PHP CGI cannot be accessed
    directly..](#faq.installation.forceredirect)
13. [怎样得知我的 php.ini
    是否被找到和应用了？似乎我做的修改都没有生效。](#faq.installation.findphpini)
14. [怎样将 PHP 目录加入到 Windows 路径
    PATH中去？](#faq.installation.addtopath)
15. [怎样使 php.ini 文件在 Windows 下被 PHP
    所用？](#faq.installation.phprc)
16. [有可能使 PHP 运作于 Apache 的 content negotiation（MultiViews
    选项）吗？](#faq.installation.apache.multiviews)
17. [PHP 是否仅限于处理 GET 和 POST
    请求方法？](#faq.installation.requestmethods)

**为什么不应该在实际运作环境中的 Apache2 中使用线程化的 MPM？**  
PHP 是粘合剂。它将几十种第三方的库粘合到一起来创建很酷的 web
应用，并通过很直观且易于学习的语言界面使其看上去好像一个整体。PHP
的灵活与强大依赖于底层平台的稳定与耐用。起码需要将一个可运作的操作系统，一个可运作的
web 服务器以及可运作的第三方库粘合起来。其中任何一方不运作了，PHP
都需要有方法来识别出问题并且快速解决。如果没有完全独立的执行线程，完全独立的内存单元和稳定的空间对付每个请求，那底层架构就太复杂以至于不稳定因素更容易进入到
PHP 系统中。

如果必须要用线程化的 MPM，看看 FastCGI 配置，使 PHP
运行于自己独立的内存空间中。

最后需要指出，不使用线程化 MPM 的警告在 Windows 系统中没那么强烈，因为
Windows 中的大多数库都理应在多线程下安全运行。

<!-- -->

**Unix/Windows：应该上哪儿去找我的 `php.ini` 文件？**  
UNIX 中默认在 `/usr/local/lib`目录中，也就是
`<install-path>/lib`。很多人会在编译时通过
<a href="/configure/about.html#configure.with-config-file-path" class="link">--with-config-file-path</a>标记来改变路径。例如可以将路径设为：

``` shell
--with-config-file-path=/etc
```

然后从发行包中将 `php.ini-dist`拷贝为
`/etc/php.ini`并编辑它来作出想要的修改。

``` shell
--with-config-file-scan-dir=PATH
```

Windows 中 `php.ini` 文件的默认路径在 Windows 目录下。如果使用的是
Apache 服务器，则会首先在 Apache 的安装目录中寻找 `php.ini`，例如
`C:\Program Files\Apache Group\Apache`。这样同一台机器上不同版本的
Apache 就可以有不同的 `php.ini` 文件。

参见 <a href="/configuration/file.html" class="link">配置文件</a>。

<!-- -->

**Unix：我安装了 PHP，但每次我打开一个页面时，只得到一条“Document Contains No Data”消息！这是怎么回事？**  
这可能意味着 PHP 发生了某类错误而导致了 core
dump。查看服务器的错误日志看看是不是这样，再用一个小的测试例子试着重现此问题。如果你会用“gdb”的话，那么在
bug 报告中提供回溯跟踪很有助于帮开发人员查明问题。如果你用 Apache
的模块方式使用 PHP，试着这么做：

-   停止 httpd 进程

-   gdb httpd

-   停止 httpd 进程

-   \> run -X -f /path/to/httpd.conf

-   然后在你的浏览器中访问导致错误的 URL

-   \> run -X -f /path/to/httpd.conf

-   如果你遇到 core dump，gdb 此时就会通知你

-   输入：bt

-   你应该在 bug 报告中包括回溯追踪记录。应该提交到
    <a href="https://bugs.php.net/" class="link external">» https://bugs.php.net/</a>

如果你的脚本使用了正则表达式函数（ <span
class="function">ereg</span>等），应该确认在编译 PHP 和 Apache
时使用了同一个正则表达式包。在 PHP 和 Apache 1.3.x 中应该自动就是这样。

<!-- -->

**Unix：我从 RPMS 安装了 PHP，但是 Apache 不处理 PHP 页面！这是怎么回事？**  
假定你的 Apache 和 PHP 都是从 RPM 包中安装的，你需要在 `httpd.conf`
文件中取消以下部分或所有行的注释，或者把它们添加到该文件中：

``` apache-conf
# Extra Modules
AddModule mod_php.c
AddModule mod_php3.c
AddModule mod_perl.c

# Extra Modules
LoadModule php_module         modules/mod_php.so
LoadModule php3_module        modules/libphp3.so     # for PHP 3
LoadModule php4_module        modules/libphp4.so     # for PHP 4
LoadModule perl_module        modules/libperl.so
```

并且把：

``` apache-conf
AddType application/x-httpd-php3 .php3    # for PHP 3
AddType application/x-httpd-php .php      # for PHP 4
```

添加到全局属性中，或者添加到你希望加入 PHP 支持的虚拟域中。

<!-- -->

**Unix：我从 RPMS 安装了 PHP 3，但它没有把我需要的数据库支持编译进去！这是怎么回事？**  
由于 PHP 3 构造的原因，不容易编译出一个完全灵活的 PHP RPM
包来。这个问题在 PHP 4 中解决了。对于 PHP 3 来说，我们目前建议你用 PHP
发行包中 INSTALL.REDHAT 文件中所描述的机制。如果你坚持要用 PHP 3 的 RPM
版本，请接着往下看。

为了简化安装 *以及*由于 RPMS 使用了 /usr/ 而不是标准的 /usr/local/
目录来存放文件，制作 RPM 包的人设定 RPMS
不安装任何数据库支持。你需要告诉 RPM
说明文件，你想要支持哪个数据库以及你的数据库服务器最高层路径。

下面的例子解说了如何在用模块安装下的 Apache 中加入流行的 MySQL
数据库服务器支持的过程。

当然这些信息可以调整用于任何 PHP
支持的数据库服务器。本例中我们也假定你从 RPMS 中完整安装了 MySQL 和
Apache。

-   先去掉 mod\_php3：

    ``` shell
    rpm -e mod_php3
    ```

-   然后取得源文件的 rpm 包并安装它，而不是编译它。

    ``` shell
    rpm -Uvh mod_php3-3.0.5-2.src.rpm
    ```

-   接着编辑 `/usr/src/redhat/SPECS/mod_php3.spec`文件

    在 %build 一节加入你想要的数据库支持，以及路径。

    对应于 MySQL 你应该加入 **--with-mysql=/usr**。则 %build
    一节看上去将类似这样：

    ``` shell
    ./configure --prefix=/usr \ --with-apxs=/usr/sbin/apxs \ --with-config-file-path=/usr/lib \ --enable-debug=no \ --enable-safe-mode \ --with-exec-dir=/usr/bin \ --with-mysql=/usr \ --with-system-regex
    ```

-   一旦完成了这个修改，就这样建立二进制程序的 rpm 包：

    ``` shell
    rpm -bb /usr/src/redhat/SPECS/mod_php3.spec
    ```

-   然后安装 rpm

        rpm -ivh /usr/src/redhat/RPMS/i386/mod_php3-3.0.5-2.i386.rpm

确认重新启动了 Apache，这下你就有了用 RPM 安装的并且带 MySQL 支持的 PHP
3 了。注意按照 PHP 3 发行包中
`INSTALL.REDHAT`文件的说明来编译其实也许更容易一些。

<!-- -->

**Unix：我给 Apache 加上了 FrontPage extensions 补丁，结果 PHP 突然不工作了。PHP 和 Apache FrontPage extensions 兼容吗？**  
兼容的。PHP 可以和 FrontPage extensions 一起工作，问题是 FrontPage
补丁修改了几个 PHP 依赖的 Apache 构造。在 FrontPage
补丁安装之后之后重新编译 PHP（用“make clean ; make”）可以解决此问题。

<!-- -->

**Unix/Windows：我已经安装了 PHP，但当我试着通过浏览器访问 PHP 脚本时，得到了一个空白页面。**  
用浏览器中的“查看源文件”，你可能会发现能看到 PHP 脚本的源程序。这意味着
web 服务器没有把脚本发送给 PHP 解释。服务器配置在某处有问题，请对照 PHP
安装说明仔细检查服务器配置。

<!-- -->

**Unix/Windows：我已经安装了 PHP，但当我试着通过浏览器访问 PHP 脚本时，得到了一个服务器的 500 错误。**  
当服务器尝试运行 PHP 时出了错。要想看到有意义的错误信息，在命令行中转到
PHP 可执行程序（Windows 中是 `php.exe`）所在目录下并运行 **php
-i**。如果 PHP
运行有任何问题，那么会显示相应的错误信息，这将给你下一步要做什么的线索。如果你得到满屏幕
HTML 代码（ <span class="function">phpinfo</span>函数的输出）的话说明
PHP 本身工作正常，你的问题可能和你的服务器配置有关，要仔细检查。

**某些操作系统：我已经在不出错的情况下安装了 PHP，但当我试着启动 Apache
时得到了一个未定义符号错误：**

``` shell
[mybox:user /src/php4] root# apachectl configtest apachectl: /usr/local/apache/bin/httpd Undefined symbols: _compress _uncompress
```

这实际上和 PHP 没有关系，而和 MySQL 的客户端库有关。有的需要
**--with-zlib**，有的不需要。这个问题也包括在 MySQL 的 FAQ 中。

**Windows：我已经安装了 PHP，但当我试着通过浏览器访问 PHP
脚本时，得到如下错误：**

cgi error: The specified CGI application misbehaved by not returning a
complete set of HTTP headers. The headers it did return are:

这个错误信息意味着 PHP
根本就不能产生任何输出。要想看到有意义的错误信息，在命令行中转到 PHP
可执行程序（Windows 中是 `php.exe`）所在目录下并运行 **php -i**。如果
PHP
运行有任何问题，那么会显示相应的错误信息，这将给你下一步要做什么的线索。如果你得到满屏幕
HTML 代码（ <span class="function">phpinfo</span>函数的输出）的话说明
PHP 本身工作正常。

一旦 PHP
在命令行中工作正常，试着通过浏览器再次访问脚本。如果还失败的话那可能是如下原因之一：

-   <span class="simpara">文件权限问题，你的 PHP 脚本， `php.exe`，
    `php4ts.dll`，`php.ini` 或任何你要加载的 PHP 扩展库是匿名 internet
    用户 *ISUR\_\<machinename\>*无权访问的。</span>
-   <span
    class="simpara">脚本文件不存在（或者有可能不在你以为的地方，注意 web
    文档的目录）。注意在 IIS 中通过 Internet
    服务管理器设定脚本映射时选中“检查文件是否存在”可以捕捉到此错误。这样一来如果脚本文件不存在的话服务器就会返回一个
    404 错误信息。还有一个额外的好处就是 IIS 会基于 NTLanMan
    权限来替你对脚本文件做任何所需要的认证。</span>

**Windows：我已经照着所有的说明做了，但还是不能让 PHP 和 IIS 一起工作！**  
确认需要运行 PHP 脚本的任何用户有权限运行 `php.exe`！IIS
使用了一个在安装 IIS 时添加的匿名用户，这个用户需要有访问
`php.exe`的权限。同样任何认证用户也需要执行 `php.exe`的权限。在 IIS4
中你还需要告诉它 PHP 是一个脚本引擎。此外，你可能还需要阅读
<a href="/faq/installation.html#faq.installation.forceredirect" class="link">此常见问题</a>。

<!-- -->

**当在 IIS，PWS，OmniHTTPD 或者 Xitami 中以 CGI 方式运行 PHP 时，出现如下错误： *Security Alert! PHP CGI cannot be accessed directly.*.**  
必须将
<a href="/ini/core.html#ini.cgi.force-redirect" class="link">cgi.force_redirect</a>选项设为
*0*。 默认值为 *1*，因此要确认此选项没有被注释掉（用
*;*）。和其它选项一样，是在 `php.ini` 中设定的。

因为默认值是 *1*，因此你必须百分之百确认使用了正确的 `php.ini`
文件。详细信息请阅读
<a href="/faq/installation.html#faq.installation.findphpini" class="link">此常见问题</a>。

<!-- -->

**怎样得知我的 `php.ini` 是否被找到和应用了？似乎我做的修改都没有生效。**  
要确认你的 `php.ini` 被 PHP 使用了，调用 <span
class="function">phpinfo</span>，在接近开头的位置有一项叫做
*Configuration File (php.ini)*。这里将告诉你 PHP 在哪里找到了 `php.ini`
并且是否使用了。如果只显示一个目录则 没有使用任何 `php.ini`
文件，你应将你的 `php.ini` 文件放到该目录中。如果 `php.ini`
包括在该路径中则它已被应用了。

如果 `php.ini` 被使用了并且你是以模块方式运行 PHP 的，确保在修改了
`php.ini` 之后重新启动你的 web server。

<!-- -->

**怎样将 PHP 目录加入到 Windows 路径 `PATH`中去？**  
在 Windows NT，2000，XP 和 2003 下：

-   进入控制面板并打开“系统”图标（开始 -\> 设置 -\> 控制面板 -\>
    系统，Windows XP/2003 中是：开始 -\> 控制面板 -\> 系统）

-   选择“高级”标签页

-   点击“环境变量”按钮

-   在“系统变量”栏中

-   找到 Path 这一项（可能需要向下滚动才能找到）

-   鼠标双击 Path 这一项

-   在最后加入你的 PHP 目录，包括前面的“;”（例如： *;C:\\php*）

-   点击“确定”并重新启动电脑

在 Windows 98/Me 中需要编辑 `autoexec.bat`文件：

-   打开记事本（开始 -\> 运行，然后输入 notepad 并点确定）

-   打开 `C:\autoexec.bat`文件

-   找到这么一行：PATH=C:\\WINDOWS;C:\\WINDOWS\\COMMAND;.....
    并在最后加上 *;C:\\php*

-   保存文件并重新启动电脑

> **Note**: <span class="simpara">记住在上述修改之后重新启动，以确保对
> `PATH`的改变生效。</span>

PHP 手册过去提倡把文件拷贝到 Windows 系统目录中去，这是因为该目录（
`C:\Windows`， `C:\WINNT`，等等）默认就在系统路径中。但是把文件拷贝到
Windows 系统目录中这一方式早已不被提倡，还可能造成问题。

<!-- -->

**怎样使 `php.ini` 文件在 Windows 下被 PHP 所用？**  
有几种方法。如果使用 Apache，阅读专门的安装指示（
<a href="/install/windows/legacy/index.html#install.windows.legacy.apache1" class="link">Apache 1</a>，
<a href="/install/windows/legacy/index.html#install.windows.legacy.apache2" class="link">Apache 2</a>），否则就必须设定
`PHPRC`环境变量：

在 Windows NT，2000，XP 和 2003 种：

-   进入控制面板并打开“系统”图标（开始 -\> 设置 -\> 控制面板 -\>
    系统，Windows XP/2003 中是：开始 -\> 控制面板 -\> 系统）

-   选择“高级”标签页

-   点击“环境变量”按钮

-   在“系统变量”栏中

-   点击“新建”按钮并在“变量名”中输入“PHPRC”，在“变量值”中输入 `php.ini`
    文件所在的目录（例如： *C:\\php*）

-   点击“确定”并重新启动电脑

在 Windows 98/Me 中需要编辑 `autoexec.bat`文件：

-   打开记事本（开始 -\> 运行，然后输入 notepad 并点确定）

-   打开 `C:\autoexec.bat`文件

-   在文件结尾处加入一行： *set PHPRC=C:\\php*（将 *C:\\php*替换为你的
    `php.ini` 实际存在的目录）。注意路径中不能包含空格。例如将 PHP
    安装到了 `C:\Program Files\PHP`中，你需要输入
    `C:\PROGRA~1\PHP`替代之

-   保存文件并重新启动电脑

<!-- -->

**有可能使 PHP 运作于 Apache 的 content negotiation（MultiViews 选项）吗？**  
如果到 PHP 文件的连接包含扩展名，一切都运行完美。本解答只针对到 PHP
文件的连接不包含扩展名时，而希望通过 content negotiation
来从不包含扩展名的 URL 来选择 PHP 文件的情况。在此种情况下，将 *AddType
application/x-httpd-php .php*替换为：

``` apache-conf
# PHP 4
AddHandler php-script php
AddType text/html php

# PHP 5
AddHandler php5-script php
AddType text/html php
```

此方案对于 Apache 1 不适用，因为 PHP 模块不捕获 *php-script*。

<!-- -->

**PHP 是否仅限于处理 GET 和 POST 请求方法？**  
不是，PHP 有可能处理任何请求方法，例如 CONNECT。适当的回应状态可以用
<span class="function">header</span>发送。如果仅需要处理 GET 和 POST
方法，可以通过如下的 Apache 配置实现：

``` apache-conf
<LimitExcept GET POST>
Deny from all
</LimitExcept>
```
