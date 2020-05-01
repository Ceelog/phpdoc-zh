Sun Solaris 上的 Sun、iPlanet 和 Netscape 服务器
------------------------------------------------

本节包含了在 Sun Solaris 平台的 Sun Java System web Server、Sun ONE web
Server、iPlanet 和 Netscape 下安装 PHP 的说明和提示。

从 PHP 4.3.3 起，可以使用基于
<a href="/ref/nsapi.html" class="link">NSAPI</a>模块 PHP
脚本来<a href="/install/unix/sun.html#install.unix.sun.specialpages" class="link">生成自定义目录列表和错误页面</a>。更多与
Apache 兼容的功能也可以使用。要了解如何在当前的 web
服务器中支持此功能，请阅读<a href="/install/unix/sun.html#install.unix.sun.notes" class="link">关于子请求（subrequests）的注释</a>。

可以在下面的链接中了解更多关于在 Netscape Enterprise Server（NES）中设置
PHP
的信息：<a href="http://benoit.noss.free.fr/php/install-php4.html" class="link external">» http://benoit.noss.free.fr/php/install-php4.html</a>。

要在 Sun JSWS/Sun ONE WS/iPlanet/Netscape web 服务器中编译 PHP，请为
<a href="/configure/about.html#configure.with-nsapi" class="link">--with-nsapi=[DIR]</a>
输入合适的安装目录。默认的目录通常是
`/opt/netscape/suitespot/`。还可以阅读
`/php-xxx-version/sapi/nsapi/nsapi-readme.txt`。

1.  从
    <a href="http://www.sunfreeware.com/" class="link external">» http://www.sunfreeware.com/</a>
    或其它下载站点安装下面的软件包：

    -   `autoconf-2.13`
    -   `automake-1.4`
    -   `bison-1_25-sol26-sparc-local`
    -   `flex-2_5_4a-sol26-sparc-local`
    -   `gcc-2_95_2-sol26-sparc-local`
    -   `gzip-1.2.4-sol26-sparc-local`
    -   `m4-1_4-sol26-sparc-local`
    -   `make-3_76_1-sol26-sparc-local`
    -   `mysql-3.23.24-beta`（如果想要 mysql 支持）
    -   `perl-5_005_03-sol26-sparc-local`
    -   `tar-1.13`(GNU tar)

2.  <span class="simpara"> 请确认 PATH 变量包含适当的目录
    *PATH=.:/usr/local/bin:/usr/sbin:/usr/bin:/usr/ccs/bin*，并使用
    **`export PATH`**命令将其导出为环境变量。 </span>

3.  <span class="simpara"> **`gunzip php-x.x.x.tar.gz`**（如果使用 `.gz`
    版本，否则跳到 4） </span>

4.  <span class="simpara"> **`tar xvf php-x.x.x.tar`** </span>

5.  <span class="simpara">进入 PHP 解压缩后的目录：
    **`cd ../php-x.x.x`** </span>

6.  在下面的步骤中，请确认 Netscape 服务器安装在
    `/opt/netscape/suitespot/`
    目录中。否则，将下面命令中的该路径修改为正确的路径并运行：

    ``` shell
    ./configure --with-mysql=/usr/local/mysql \
    --with-nsapi=/opt/netscape/suitespot/ \
    --enable-libgcc
    ```

7.  <span class="simpara"> 运行 **make**，然后运行 **make install**。
    </span>

在执行了基础的安装并阅读相应的 Readme
文件后，还需要执行一些额外的配置步骤。

##### Sun/iPlanet/Netscape 的配置说明

首先需要为 `LD_LIBRARY_PATH`
环境变量添加一些路径，以便服务器找到所需的共享库。可以使用 web
服务器的启动脚本很好的完成这一工作。启动脚本通常位于：`/path/to/server/https-servername/start`。或许需要编辑其配置文件，它位于：`/path/to/server/https-servername/config/`。

1.  添加下面一行到 `mime.types`（可以在管理服务器中添加）：

        type=magnus-internal/x-httpd-php exts=php

2.  编辑 `magnus.conf`（若服务器 \>= 6）或 `obj.conf`（若服务器 \<
    6）并添加下述内容。shlib 的值根据系统的配置会有所不同。它可能类似于
    `/opt/netscape/suitespot/bin/libphp4.so`。应该在 *mime types
    init*后添加如下两行内容：

        Init fn="load-modules" funcs="php4_init,php4_execute,php4_auth_trans" shlib="/opt/netscape/suitespot/bin/libphp4.so"
        Init fn="php4_init" LateInit="yes" errorString="Failed to initialize PHP!" [php_ini="/path/to/php.ini"]

    （PHP \>= 4.3.3）*php\_ini* 参数是可选的。但是若使用它，便可以将
    `php.ini` 放到 web 服务器的配置目录中去。

3.  在 `obj.conf` 中配置默认对象（对于虚拟服务器的类 \[版本 6.0+\] 是在
    `vserver.obj.conf`中）：

        <Object name="default">
        .
        .
        .
        .#注意 下面一行添加在所有“ObjectType”之后，所有“AddLog”之前
        Service fn="php4_execute" type="magnus-internal/x-httpd-php" [inikey=value inikey=value ...]
        .
        .
        </Object>

    （PHP \>= 4.3.3）作为附加的参数，可以在 `php.ini`
    中添加一些特别的配置选项。例如可以设置 *docroot="/path/to/docroot"*
    指向 *php4\_execute* 被调用的上下文（context）。对于布尔 ini
    键值，请使用 0/1 作为其值，而不是 *"On"、"Off"*
    等（它们是无效的），例如，使用
    *zlib.output\_compression=1*，而不应使用
    *zlib.output\_compression="On"*。

4.  本步骤仅在需要配置一个由 PHP 脚本组成的目录时由必要执行（类似于一个
    `cgi-bin`目录）：

        <Object name="x-httpd-php">
        ObjectType fn="force-type" type="magnus-internal/x-httpd-php"
        Service fn=php4_execute [inikey=value inikey=value ...]
        </Object>

    之后，可以在管理服务器中配置一个目录，分配给它 *x-httpd-php*
    风格（style）。这样在该目录中的所有文件都会被当作 PHP
    来执行。这样就能很方便的将 PHP 文件更名为 `.html`以隐藏 PHP。

5.  认证的设置：PHP
    认证不能与其它任何类型的认证一起工作。所有认证被传递到 PHP
    脚本。要为整个服务器配置 PHP 认证，在默认对象中添加下面一行：

        <Object name="default">
        AuthTrans fn=php4_auth_trans
        .
        .
        .
        </Object>

6.  要在单一目录使用 PHP 认证，添加如下内容：

        <Object ppath="d:\path\to\authenticated\dir\*">
        AuthTrans fn=php4_auth_trans
        </Object>

> **Note**:
>
> PHP 使用的堆栈大小取决于 web 服务器的配置。如果运行很大的 PHP
> 脚本时程序崩溃，推荐在 Admin Server（在“MAGNUS
> EDITOR”一节）中增大此项。

### CGI 环境和对 php.ini 推荐的修改

当编写 PHP 脚本时，应特别注意 Sun JSWS/Sun ONE WS/iPlanet/Netscape
是一个多线程 web 服务器。因此，所有请求都运行在相同的进程空间（Web
服务器自己的空间），该空间仅有一套环境变量。如果想获得 CGI 变量，例如
*PATH\_INFO*、*HTTP\_HOST* 等，使用原有的 PHP 3.x 的方式（<span
class="function">getenv</span>），或使用类似的方式（注册全局变量到环境变量，`$_ENV`），都是不可行的。只能获得运行中的
web 服务器的环境变量，而不能获得任何有效的 CGI 变量！

> **Note**:
>
> 为什么在环境中存在（无效的）CGI 变量？
>
> 答：这是因为从管理服务器中启动 web 服务器进程时，运行了 web
> 服务器的启动脚本，它事实上是一个 CGI 脚本（管理服务器中的一个 CGI
> 脚本！）。这便是为什么启动的 web 服务器包含一些 CGI
> 变量。可以尝试不从管理服务器启动 web 服务器，用 root
> 用户登录使用命令行手动启动它，会发现这些 CGI 形式的变量不复存在。

要在 PHP 4.x 中正确获得 CGI 变量，仅需修改脚本使用超级全局变量
`$_SERVER`。如果老脚本中使用了 `$HTTP_HOST` 等变量，应该在 `php.ini`
中打开 *register\_globals*，并且要修改变量顺序（注意：从中删除
*"E"*，因为不需要这里的环境变量）：

    variables_order = "GPCS"
    register_globals = On

### 错误页面及自造目录列表的特别使用 (PHP \>= 4.3.3)

可以使用 PHP 为 *"404 Not Found"*
或类似的错误代码生成错误页面。将下面几行添加到 `obj.conf`
中以覆盖默认的错误页面：

    Error fn="php4_execute" code=XXX script="/path/to/script.php" [inikey=value inikey=value...]

*XXX* 是 HTTP 错误代码。请删除任何可能干扰 *Error*
设置的指令。如果想为所有可能存在的错误提供一个页面，则将 *code*
参数删除。脚本可以通过 `$_SERVER['ERROR_TYPE']` 获得 HTTP 状态代码。

另一种可能是生成自造目录列表。只要创建一个 PHP 脚本，来显示目录列表 并在
`obj.conf` 中为 *type="magnus-internal/directory"* 将相应的默认
*Service* 行替换为：

    Service fn="php4_execute" type="magnus-internal/directory" script="/path/to/script.php" [inikey=value inikey=value...]

错误和目录列表页面中，原始的 URI 和翻译的 URI 均被分别储存在
`$_SERVER['PATH_INFO']` 和 `$_SERVER['PATH_TRANSLATED']` 变量中。

### 关于 <span class="function">nsapi\_virtual</span>和子请求的注意事项（PHP \>= 4.3.3）

NSAPI 模块现在支持 <span class="function">nsapi\_virtual</span>
函数（别名： <span class="function">virtual</span>），用来在 web
服务器上创建子请求（subrequests）和在 web
页面插入请求的结果。此函数使用了一些 NSAPI 中还没有文档说明的函数。在
Unix 下，该模块自动查找需要的函数，若它们存在则使用它们。若不存在，函数
<span class="function">nsapi\_virtual</span> 被禁用。

> **Note**:
>
> 但是要注意，对 <span class="function">nsapi\_virtual</span>
> 的支持是试验性质的！
