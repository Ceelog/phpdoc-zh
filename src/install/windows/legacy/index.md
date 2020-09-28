旧版本 Windows 支持
-------------------

本节适用于 Windows 98/Me 和 Windows NT/2000/XP/2003。PHP 不能在 16
位平台上工作，如 Windows 3.1，有时我们将支持的 Windows 平台为 Win32。

> **Note**:
>
> 从 PHP 5.5.0 开始不再支持 Windows XP/2003。

> **Note**:
>
> 从 PHP 5.3.0 开始，不再支持 Windows 98/Me/NT4/2000。

> **Note**:
>
> 从 PHP 4.3.0 开始不再支持 Windows 95。

如果你有微软 Visual Studio 这样的开发环境，你也可以从原始源码中构建
PHP。

在 Windows 系统上安装 PHP 后，如果还想加载各种扩展来增加功能，请参考
<a href="/install/windows/legacy/index.html#install.windows.legacy.extensions" class="link">这里</a>。

### 手工安装步骤

本章包含有在 Microsoft Windows 中手工安装和配置 PHP 的指示。

#### 选择和下载 PHP 发行包

从
<a href="https://windows.php.net/download/" class="link external">» PHP for Windows: Binaries and Sources</a>
页面下载 PHP 的 zip 二进制发行包。有几个不同版本，根据所用 web
服务器选择合适的版本： follow the detailed guide on the
<a href="https://windows.php.net/download/" class="link external">» download page</a>.

#### PHP 压缩包的结构和内容

将 zip 包解压缩到自己选择的目录，例如
C:\\PHP\\。此目录和文件结构类似于：

**示例 \#1 PHP 5 压缩包的结构**


    c:\php
       |
       +--dev
       |  |
       |  |-php5ts.lib                 -- php5.lib 的非线程安全版本
       |
       +--ext                          -- PHP 扩展库的 DLL 文件目录
       |  |
       |  |-php_bz2.dll
       |  |
       |  |-php_cpdf.dll
       |  |
       |  |-...
       |
       +--extras                       -- 空 
       |
       +--pear                         -- PEAR 的初始版本
       |
       |
       |-go-pear.bat                   -- PEAR 安装脚本
       |
       |-...
       |
       |-php-cgi.exe                   -- CGI 可执行文件
       |
       |-php-win.exe                   -- 无窗口执行脚本的可执行文件
       |
       |-php.exe                       -- PHP 命令行可执行文件（CLI）
       |
       |-...
       |
       |-php.ini-development           -- 默认的 php.ini 设置
       |
       |-php.ini-production            -- 推荐的 php.ini 设置
       |
       |-php5apache2_2.dll             -- 非线程安全版本中无此文件
       |
       |-php5apache2_2_filter.dll      -- 非线程安全版本中无此文件
       |
       |-...
       |
       |-php5ts.dll                    -- PHP 核心 DLL（php5.dll 的非线程安全版本）
       | 
       |-...

以下是 PHP zip 包中包含的模块和可执行文件列表：

-   `go-pear.bat` - PEAR
    安装脚本。更多内容参见<a href="https://pear.php.net/manual/en/installation.php" class="link external">» 安装 PEAR</a>。

-   `php-cgi.exe` - CGI 可执行文件，可用于 IIS 上以 CGI 或者 FastCGI
    方式运行 PHP。

-   `php-win.exe` - PHP 可执行文件，可运行 PHP
    脚本而不打开命令行窗口（例如使用 Windows 图形界面的 PHP 程序）。

-   `php.exe` - PHP 可执行文件，用于命令行界面运行 PHP 脚本（CLI）。

-   `php5apache2_2.dll` - Apache 2.2.X 模块。

-   `php5apache2_2_filter.dll` - Apache 2.2.X 过滤器。

#### 修改 `php.ini` 文件

解压缩 PHP 的包之后，将 `php.ini-production` 拷贝为 同一目录下的
`php.ini`。如有必要，也可以将 `php.ini`
放到其它地方，但是需要更多配置步骤，具体见<a href="/configuration/file.html" class="link">配置文件</a>。

`php.ini` 文件决定 PHP 如何配置自身以及如何在其工作环境下运行。以下
`php.ini` 文件中的配置指令有助于使 PHP 更好地运行于 Windows
之中。有一些是可选项。还有很多其它指令也可能与用户环境有关，更多信息见
<a href="/ini/list.html" class="link">php.ini 配置选项列表</a>。

必须的指令：

-   `extension_dir` = *\<指向扩展库目录的路径\>* - `extension_dir`
    需要指向存放 PHP 扩展库文件的目录。可以是绝对路径（如
    "C:\\PHP\\ext"）或相对路径（如 ".\\ext"）。在 `php.ini`
    文件中要加载的扩展库都必须在 `extension_dir` 所指定的目录之中。

-   `extension` = *xxxxx.dll* - 对每个需要激活的扩展，都需要一行相应的
    "extension=" 语句来说明 PHP 启动时加载 `extension_dir`
    目录下的哪些扩展。

-   `log_errors` = *On* - PHP
    有错误日志的功能可以将错误报告发送到一个文件中，或者系统服务中（例如系统日志），与下面的
    `error_log` 指令配合工作。在 IIS 下运行时，`log_errors`
    应被激活，并且配合有效的 `error_log`。

-   `error_log` = *\<指向错误日志文件的路径\>* - error\_log
    需要指向一个具有绝对或相对路径的文件名用于记录 PHP 的错误日志。Web
    服务器需要对此文件有可写权限。最常用的位置是各种临时目录，例如
    "C:\\inetpub\\temp\\php-errors.log"。

-   `cgi.force_redirect` = *0* - 在 IIS
    下运行时需要关闭此项指令。这是个在许多其它 web
    服务器中都需要激活的目录安全功能，但是在 IIS 下如果激活则会导致 PHP
    引擎在 Windows 中出错。

-   `cgi.fix_pathinfo` = *1* - 此指令可以允许 PHP 遵从 CGI
    规则访问真实路径信息。IIS 的 FastCGI 实现需要激活此指令。

-   `fastcgi.impersonate` = *1* - IIS 下的 FastCGI
    支持模拟呼叫用户方安全令牌的能力。这使得 IIS
    可以定义请求方的安全上下文。

-   `fastcgi.logging` = *0* - FastCGI 日志在 IIS
    下应被关闭。如果激活，则任何类的任何消息都被 FastCGI
    视为错误条件从而导致 IIS 产生 HTTP 500 错误。

可选指令：

-   `max_execution_time` = *\#\#* -
    此指令设定任何脚本所能够运行的最长时间。默认值是 30 秒。如果 PHP
    程序需要更多时间运行则增大此值。

-   `memory_limit` = *\#\#\#M* - PHP
    进程能够占用的内存，单位为兆字节。默认值是
    128M，对大多数程序都够用了。某些复杂程序可能需要更多。

-   `display_errors` = *Off* - 此指令设定 PHP
    是否将任何错误信息包含在返回给 web 服务器的数据流中。如果设定为
    "On"，则 PHP 将任何由 `error_reporting`
    指令所定义的错误信息作为错误数据流发给 web
    服务器。为安全起见，建议对在线服务器设为 "Off"
    以避免泄露任何可能包含在错误消息中的安全敏感信息。

-   `open_basedir` = *\<指向目录的路径，由分号分隔\>* - 例如
    openbasedir="C:\\inetpub\\wwwroot;C:\\inetpub\\temp"。此指令指定了允许
    PHP
    进行文件系统操作的目录。任何对这些目录之外的文件操作都会导致错误。此指令在共享主机环境中特别有用，可以阻止
    PHP 脚本访问任何其网站根目录之外的文件。

-   `upload_max_filesize` = *\#\#\#M* 和 `post_max_size` = *\#\#\#M* -
    分别是上传文件的最大大小和 POST 方法提交数据的最大大小。如果 PHP
    程序需要上传大型数据例如照片和视频文件，则应提高这两项的值。

至此已在系统中安装了 PHP。下一步是选择一种 web 服务器并且使其能够运行
PHP。在目录中选择 web 服务器。

除了可在 web 服务器中运行 PHP 之外，PHP 还可以在命令行运行，如同 *.BAT*
批处理脚本一样。详见
<a href="/install/windows/legacy/index.html#install.windows.legacy.commandline" class="link">Windows 下的 PHP 命令行方式</a>。

### Microsoft IIS

本部分将具体指导如何在微软 Internet 信息服务（IIS）上安装 PHP。

-   <span class="simpara">
    <a href="/install/windows/legacy/index.html#install.windows.legacy.iis6" class="link">在 IIS 5.1 和 IIS 6.0 上手工安装 PHP</a>
    </span>
-   <span class="simpara">
    <a href="/install/windows/legacy/index.html#install.windows.legacy.iis7" class="link">在 IIS 7.0 及更高版本上手工安装 PHP</a>
    </span>

### Microsoft IIS 5.1 和 IIS 6.0

本章包含有在 Windows XP 和 Windows Server 2003 下的 Internet
信息服务（IIS）5.1 和 IIS 6.0 中安装 PHP 的指南。有关在 Windows
Vista，Windows Server 2008，Windows 7 以及 Windows Server 2008 R2 下的
IIS 7.0 以及更高版本中安装 PHP 的指南见
<a href="/install/windows/legacy/index.html#install.windows.legacy.iis7" class="link">Microsoft IIS 7.0 及更高版本</a>一章。

#### 配置 IIS 以处理 PHP 请求

根据<a href="/install/windows/legacy/index.html#install.windows.legacy.manual" class="link">手工安装步骤</a>的说明下载和安装
PHP。

> **Note**:
>
> 在使用 IIS 时推荐使用非线程安全的 PHP。可以在
> <a href="https://windows.php.net/download/" class="link external">» PHP for Windows: Binaries and Sources Releases</a>
> 下载。

按以下示例在 `php.ini` 文件中配置 针对 CGI- 和 FastCGI- 的指令：

**示例 \#2 `php.ini` 中的 CGI 和 FastCGI 设定**

``` ini
fastcgi.impersonate = 1
fastcgi.logging = 0
cgi.fix_pathinfo=1
cgi.force_redirect = 0
```

下载并安装
<a href="http://www.iis.net/extensions/fastcgi" class="link external">» FastCGI for IIS</a>。有
32 位和 64 位平台的，根据用户平台选择相应的下载。

用以下命令配置 FastCGI 扩展处理 PHP 请求。用指向 `php-cgi.exe`
文件的绝对路径替换其中的 "-path" 的参数。

**示例 \#3 配置 FastCGI 扩展以处理 PHP 请求**

    cscript %windir%\system32\inetsrv\fcgiconfig.js -add -section:"PHP" ^
    -extension:php -path:"C:\PHP\php-cgi.exe"

此命令将创建对应于 \*.php 文件后缀的 IIS 脚本映射，则所有以 \*.php
结尾的 URL 都会被 FastCGI 扩展处理。此外还配置了 FastCGI 扩展使用
`php-cgi.exe` 可执行文件来处理 PHP 请求。

> **Note**:
>
> 至此所需的安装和配置步骤就完成了。以下剩余的指示是可选项，但是强烈推荐以使得在
> IIS 上达到最佳的 PHP 功能和性能。

#### 角色扮演及文件系统访问

在 IIS 中使用 PHP 建议激活 FastCGI 的角色扮演功能。此功能在 `php.ini`
中由 `fastcgi.impersonate` 指令控制。激活角色扮演后，PHP 将以 IIS
所认证的用户帐号身份进行所有的文件系统操作。这将确保即使在（同一个主机）不同的
IIS 网站下使用了同一个 PHP 进程，只要每个网站使用了不同的用户帐号作为
IIS 身份认证，则这些网站的 PHP 脚本将不能访问彼此的文件。

例如在 IIS 5.1 和 IIS 6.0 中，默认配置下的匿名认证将使用内置的用户帐号
IUSR\_\<MACHINE\_NAME\> 作为默认身份。这意味着要使得 IIS 能够运行 PHP
脚本，至少要将这些脚本的读取权限授予 IUSR\_\<MACHINE\_NAME\> 帐号。如果
PHP 程序需要对某些文件或文件夹进行写入操作，那 IUSR\_\<MACHINE\_NAME\>
帐号也需要有相对应的写入权限。

要查看哪个用户帐号被用作 IIS 匿名认证的身份，使用以下步骤：

1.  在 Windows 开始菜单中选择“运行...”，输入“inetmgr”并点击“确定”；

2.  在树形视图下展开“网站”节点，右键点击要使用的网站并选择“属性”；

3.  点击“目录安全”面板；

4.  记录下在“认证方式”对话框中的“用户名”字段。

<img src="images/b4cf2bb34e3c20eebcf8f9e8e7949efd-iis6anonauth.png" width="654" height="461" alt="IIS 5.1 和 IIS 6.0 的匿名认证" />

要修改文件及文件夹的权限，使用 Windows 资源管理器或者 `icacls` 命令行。

**示例 \#4 配置文件访问权限**

    icacls C:\inetpub\wwwroot\upload /grant IUSR:(OI)(CI)(M)

#### 在 IIS 中把 `index.php` 设定为默认文档

IIS 的默认文档用于没有指定文件名的 HTTP 请求。对于 PHP
应用来说默认文档通常为 `index.php`。要将 `index.php` 添加到 IIS
的默认文档列表中，使用以下步骤：

1.  在 Windows 开始菜单中选择“运行...”，输入“inetmgr”并点击“确定”；

2.  在树形视图下展开“网站”节点，右键点击要使用的网站并选择“属性”；

3.  点击“文档”面板；

4.  点击“添加...”按钮并在“默认内容页面”中输入“index.php”。

<img src="images/b4cf2bb34e3c20eebcf8f9e8e7949efd-iis6defaultdoc.png" width="659" height="465" alt="将 index.php 设为 IIS 的默认文档" />

#### FastCGI 和 PHP 回收配置

用以下命令配置 IIS FastCGI 对于 PHP 进程的回收设定。FastCGI 的设置
`instanceMaxRequests` 控制了单一的 `php-cgi.exe`
进程处理多少个请求之后会被 IIS 关闭。PHP 环境变量
`PHP_FCGI_MAX_REQUESTS` 控制了一个 `php-cgi.exe`
进程处理多少个请求之后会被自我回收。要确保 FastCGI 中
`InstanceMaxRequests` 的值小于或等于 `PHP_FCGI_MAX_REQUESTS` 的值。

**示例 \#5 配置 FastCGI 和 PHP 的回收**

    cscript %windir%\system32\inetsrv\fcgiconfig.js -set -section:"PHP" ^
    -InstanceMaxRequests:10000

    cscript %windir%\system32\inetsrv\fcgiconfig.js -set -section:"PHP" ^
    -EnvironmentVars:PHP_FCGI_MAX_REQUESTS:10000

#### FastCGI 超时设定

如果会有一些需时较长的 PHP
脚本运行，则增加超时的设定值。有两个控制超时的指令 `activityTimeout` 和
`requestTimeout`。有关这些设定的更多信息参见
<a href="http://learn.iis.net/page.aspx/248/configuring-fastcgi-extension-for-iis-60/" class="link external">» Configuring FastCGI Extension for IIS 6.0</a>。

**示例 \#6 配置 FastCGI 超时设定**

    cscript %windir%\system32\inetsrv\fcgiconfig.js -set -section:"PHP" ^
    -ActivityTimeout:90

    cscript %windir%\system32\inetsrv\fcgiconfig.js -set -section:"PHP" ^
    -RequestTimeout:90

#### 改变 `php.ini` 文件的位置

PHP
在几个位置搜索<a href="/configuration/file.html" class="link">配置文件</a>
`php.ini`，可以通过环境变量 `PHPRC` 来改变 `php.ini` 的默认位置。要使得
PHP 从用户指定的位置加载配置文件，使用以下命令。指向 `php.ini`
文件的绝对路径应作为环境变量 `PHPRC` 的值。

**示例 \#7 改变 `php.ini` 文件的位置**

    cscript %windir%\system32\inetsrv\fcgiconfig.js -set -section:"PHP" ^
    -EnvironmentVars:PHPRC:"C:\Some\Directory\"

### Microsoft IIS 7.0 及更高版本

本章包含有在 Windows Vista SP1，Windows 7，Windows Server 2008 以及
Windows Server 2008 R2下的 IIS 7.0 以及更高版本中手工安装 PHP
的指南。有关在 Windows XP 和 Windows Server 2003 下的 IIS 5.1 和 IIS 6.0
中安装 PHP 的指南见
<a href="/install/windows/legacy/index.html#install.windows.legacy.iis6" class="link">Microsoft IIS 5.1 和 IIS 6.0</a>
一章。

#### 在 IIS 中激活 FastCGI 支持

默认安装的 IIS 中 FastCGI 模块被关闭。要激活其的步骤在不同版本的 Windows
下不同。

要在 Windows Vista SP1 和 Windows 7 中激活 FastCGI 支持：

1.  在 Windows
    开始菜单中选择“运行...”（或在搜索框内），输入“optionalfeatures.exe”并按“确定”（或敲回车键）；

2.  在“Windows 功能”对话框中展开“Internet
    信息服务”，“万维网服务”，“应用程序开发功能”，并选中“CGI”的选择框；

3.  点击确定按钮并等待安装完成。

<img src="images/b4cf2bb34e3c20eebcf8f9e8e7949efd-iis7vistacgi.png" width="429" height="375" alt="在 Windows Vista SP1 和 Windows 7 中激活 FastCGI 支持" />

要在 Windows Server 2008 和 Windows Server 2008 R2 中激活 FastCGI 支持：

1.  在 Windows 开始菜单中选择 "Run:"，输入 "CompMgmtLauncher" 并点击
    "Ok"；

2.  如果在 "Roles" 节点下没有 "Web Server (IIS)" role，则点击 "Add
    Roles" 添加之；

3.  如果存在 "Web Server (IIS)" role，则点击 "Add Role Services" 并激活
    "Application Development" 组之下的 "CGI" 选择框；

4.  点击 "Next" 及 "Install"，等待安装完成。

<img src="images/b4cf2bb34e3c20eebcf8f9e8e7949efd-iis7w2k8cgi.png" width="546" height="411" alt="在 Windows Server 2008 和 Windows Server 2008 R2 中激活 FastCGI 支持" />

#### 配置 IIS 以处理 PHP 请求

根据<a href="/install/windows/manual.html" class="link">手工安装步骤</a>的说明下载和安装
PHP。

> **Note**:
>
> 在使用 IIS 时推荐使用非线程安全的 PHP。可以在
> <a href="https://windows.php.net/download/" class="link external">» PHP for Windows: Binaries and Sources Releases</a>
> 下载。

按以下示例在 `php.ini` 文件中配置 针对 CGI- 和 FastCGI- 的指令：

**示例 \#8 `php.ini` 中的 CGI 和 FastCGI 设定**

``` ini
fastcgi.impersonate = 1
fastcgi.logging = 0
cgi.fix_pathinfo=1
cgi.force_redirect = 0
```

通过 IIS 管理界面或者命令行工具配置对应于 PHP 的 IIS 程序映射。

##### 使用 IIS 管理界面来创建 PHP 的程序映射

按照以下步骤在 IIS 管理界面中创建 PHP 的程序映射：

1.  在 Windows 开始菜单中选择“运行...”，输入“inetmgr”并点击“确定”；

2.  在 IIS 管理器中左边面板“连接”下面的树状图中选择该服务器的节点；

3.  在中间面板下方的“功能视图”页面打开“处理程序映射”功能；

    <img src="images/b4cf2bb34e3c20eebcf8f9e8e7949efd-iis7handlericon.png" width="708" height="515" alt="创建 PHP 的程序映射：处理程序映射的位置" />

4.  在右边“操作”面板中点击“添加模块映射...”；

5.  在“添加模块映射”对话框中输入以下内容：

    -   <span class="simpara">请求路径(P)：\*.php</span>
    -   <span class="simpara">模块(M)：FastCgiModule</span>
    -   <span class="simpara">可执行文件(可选)(E)：C:\\\[Path to PHP
        installation\]\\php-cgi.exe</span>
    -   <span class="simpara">名称(N)：PHP\_via\_FastCGI</span>

6.  点击“请求限制(R)...”按钮并选中“仅当请求映射至以下内容时才调用处理程序(I)：”然后选择“文件或文件夹(O)”；

7.  在所有对话框中点击确定以保存配置。

<img src="images/b4cf2bb34e3c20eebcf8f9e8e7949efd-iis7handlermap.png" width="705" height="512" alt="创建 PHP 的程序映射：添加程序映射" />

##### 使用命令行工具创建 PHP 的程序映射

用以下命令创建一个 IIS FastCGI 处理池以使 `php-cgi.exe` 可执行文件来处理
PHP 请求。用自己系统上指向 `php-cgi.exe` 文件的绝对路径来替代 `fullPath`
参数的值。

**示例 \#9 创建 IIS FastCGI 处理池**

    %windir%\system32\inetsrv\appcmd set config /section:system.webServer/fastCGI ^
    /+[fullPath='c:\PHP\php-cgi.exe']

用以下命令配置 IIS 处理针对 PHP 的请求。用自己系统上指向 `php-cgi.exe`
文件的绝对路径来替代 `scriptProcessor` 参数的值。

**示例 \#10 创建对应于 PHP 请求的处理程序映射**

    %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers ^
    /+[name='PHP_via_FastCGI', path='*.php',verb='*',modules='FastCgiModule',^
    scriptProcessor='c:\PHP\php-cgi.exe',resourceType='Either']

此命令创建了一个对于 \*.php 文件后缀的处理程序映射，使得所有以 .php
结尾的 URL 都会被 FastCGI 模块处理。

> **Note**:
>
> 至此所需的安装和配置步骤就完成了。以下剩余的指示是可选项，但是强烈推荐以使得在
> IIS 上达到最佳的 PHP 功能和性能。

#### 角色扮演及文件系统访问

在 IIS 中使用 PHP 建议激活 FastCGI 的角色扮演功能。此功能在 `php.ini`
中由 `fastcgi.impersonate` 指令控制。激活角色扮演后，PHP 将以 IIS
所认证的用户帐号身份进行所有的文件系统操作。这将确保即使在（同一个主机）不同的
IIS 网站下使用了同一个 PHP 进程，只要每个网站使用了不同的用户帐号作为
IIS 身份认证，则这些网站的 PHP 脚本将不能访问彼此的文件。

例如在 IIS 7 中，默认配置下的匿名认证将使用内置的用户帐号 IUSR
作为默认身份。这意味着要使得 IIS 能够运行 PHP
脚本，至少要将这些脚本的读取权限授予 IUSR 帐号。如果 PHP
程序需要对某些文件或文件夹进行写入操作，那 IUSER
帐号也需要有相对应的写入权限。

在 IIS 7
中要查看哪个用户帐号被用作匿名认证的身份，使用以下命令。将其中的
"Default Web Site" 替换为自己使用的网站名。在输出的 XML 配置单元中查找
`userName` 属性。（注意：要以管理员身份运行此命令行）

**示例 \#11 确定用于 IIS 匿名认证的用户帐号**

    %windir%\system32\inetsrv\appcmd.exe list config "Default Web Site" ^
    /section:anonymousAuthentication

    <system.webServer>
      <security>
        <authentication>
          <anonymousAuthentication enabled="true" userName="IUSR" />
        </authentication>
       </security>
    </system.webServer>

> **Note**:
>
> 如果在 `anonymousAuthentication` 单元中没有显示 `userName`
> 属性，或者其值为一个空字符串，那意味着应用程序池的身份被用于该网站的匿名身份。

要修改文件及文件夹的权限，使用 Windows 资源管理器或者 `icacls` 命令行。

**示例 \#12 配置文件访问权限**

    icacls C:\inetpub\wwwroot\upload /grant IUSR:(OI)(CI)(M)

#### 在 IIS 中把 `index.php` 设定为默认文档

IIS 的默认文档用于没有指定文件名的 HTTP 请求。对于 PHP
应用来说默认文档通常为 `index.php`。要将 `index.php` 添加到 IIS
的默认文档列表中，使用此命令：

**示例 \#13 将 `index.php` 设为 IIS 的默认文档**

    %windir%\system32\inetsrv\appcmd.exe set config ^
    -section:system.webServer/defaultDocument /+"files.[value='index.php']" ^
    /commit:apphost

#### FastCGI 和 PHP 回收配置

用以下命令配置 IIS FastCGI 对于 PHP 进程的回收设定。FastCGI 的设置
`instanceMaxRequests` 控制了单一的 `php-cgi.exe`
进程处理多少个请求之后会被 IIS 关闭。PHP 环境变量
`PHP_FCGI_MAX_REQUESTS` 控制了一个 `php-cgi.exe`
进程处理多少个请求之后会被自我回收。要确保 FastCGI 中
`InstanceMaxRequests` 的值小于或等于 `PHP_FCGI_MAX_REQUESTS` 的值。

**示例 \#14 配置 FastCGI 和 PHP 的回收**

    %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi ^
    /[fullPath='c:\php\php-cgi.exe'].instanceMaxRequests:10000

    %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi ^
    /+"[fullPath='C:\{php_folder}\php-cgi.exe'].environmentVariables.^
    [name='PHP_FCGI_MAX_REQUESTS',value='10000']"

#### FastCGI 超时设定

如果会有一些需时较长的 PHP
脚本运行，则增加超时的设定值。有两个控制超时的指令 `activityTimeout` 和
`requestTimeout`。用以下命令修改超时设定。确保在 `fullPath`
的参数中使用自己系统上的 `php-cgi.exe` 的绝对路径。

**示例 \#15 配置 FastCGI 超时设定**

    %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi ^
    /[fullPath='C:\php\php-cgi.exe',arguments=''].activityTimeout:"90"  /commit:apphost

    %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi ^
    /[fullPath='C:\php\php-cgi.exe',arguments=''].requestTimeout:"90"  /commit:apphost

#### 改变 `php.ini` 文件的位置

PHP
在几个位置搜索<a href="/configuration/file.html" class="link">配置文件</a>
`php.ini`，可以通过环境变量 `PHPRC` 来改变 `php.ini` 的默认位置。要使得
PHP 从用户指定的位置加载配置文件，使用以下命令。指向 `php.ini`
文件的绝对路径应作为环境变量 `PHPRC` 的值。

**示例 \#16 改变 `php.ini` 文件的位置**

    appcmd.exe set config  -section:system.webServer/fastCgi ^
    /+"[fullPath='C:\php\php.exe',arguments=''].environmentVariables.^
    [name='PHPRC',value='C:\Some\Directory\']" /commit:apphost

### Microsoft Windows 下的 Apache 1.3.x

本节包括在 Microsoft Windows 平台的 Apache 下安装 PHP
的说明和提示。在另外的页面也有
<a href="/install/windows/legacy/index.html#install.windows.legacy.apache2" class="link">Apache 2 的安装和说明</a>。

> **Note**:
>
> 请先阅读<a href="/install/windows/legacy/index.html#install.windows.legacy.manual" class="link">手动安装步骤</a>！

有两种方式让 PHP 工作在 Windows 下的 Apache 1.3.x 中。首先是使用 CGI
可执行程序（PHP 4 下为 `php.exe`，PHP 5 下为
`php-cgi.exe`），另外一种方式是使用 Apache 模块
DLL。无论是那种方式，都需要修改 `httpd.conf` 来配置 Apache，使 PHP
能够在其上运行，然后都需要重启服务。

值得注意的是，现在 Windows 下的 SAPI
模块已经稳定得多，我们建议首先考虑使用 SAPI 而不要使用 CGI
可执行程序。因为 SAPI 更加透明和安全。

虽然还有些其它的方法来在 Apache 下配置
PHP，下面介绍的方法是最简单并适用于新手的。请参考 Apache
的文档以获得更多的配置参数。

在修改完配置文件后，请记得重启 Apache 服务。例如，如果把 Apache 作为
Windows 的一个服务来运行，那么在命令提示行下使用 **NET STOP
APACHE**命令然后再使用 **NET START
APACHE**命令便可重启服务。也可以使用重启 Apache 服务的快捷方式来重启。

> **Note**: <span class="simpara">记住当在 Windows 环境下的 Apache
> 配置文件中添加路径值时，所有的反斜线，如
> `c:\directory\file.ext`，应转换为正斜线：
> `c:/directory/file.ext`。对目录来说，也必须由斜线结尾。</span>

#### 作为 Apache 的模块安装

应该将下面几行加入 Apache 的 `httpd.conf` 文件：

**示例 \#17 PHP 作为 Apache 1.3.x 的一个模块**

这里假设 PHP 安装在 `c:\php`。如果不是这样请根据情况修改路径。

对于 PHP 4：

``` apache-conf
# 在 LoadModule 一节的末尾添加
# 不要忘记将该文件从 sapi 复制出来
LoadModule php4_module "C:/php/php4apache.dll"

# 在 AddModule 一节的末尾添加
AddModule mod_php4.c
```

对于 PHP 5：

``` apache-conf
# 在 LoadModule 一节的末尾添加
LoadModule php5_module "C:/php/php5apache.dll"

# 在 AddModule 一节的末尾添加
AddModule mod_php5.c
```

两个 PHP 版本都需要添加的内容：

``` apache-conf
# 将下面这行添加到 <IfModule mod_mime.c> 条件块中
AddType application/x-httpd-php .php

# 如果要使用语法高亮的 .phps 文件，需要添加
AddType application/x-httpd-php-source .phps
```

#### 作为 CGI 可执行文件的安装

如果按照<a href="/install/windows/manual.html" class="link">手工安装步骤</a>将
PHP 解压到 `C:\php\`，需要在 Apache 的配置文件中添加如下内容以使 PHP
按照 CGI 方式运行:

**示例 \#18 PHP 以 CGI 方式运行在 Apache 1.3.x**

``` apache-conf
ScriptAlias /php/ "c:/php/"
AddType application/x-httpd-php .php

# 对于 PHP 4
Action application/x-httpd-php "/php/php.exe"

# 对于 PHP 5
Action application/x-httpd-php "/php/php-cgi.exe"

# 指定 php.ini 所在目录
SetEnv PHPRC C:/php
```

请注意第二行的配置可以在默认的 `httpd.conf`
中找到，但是是被注释掉的。也请记得将 `c:/php/`替换为 PHP
所在的真实路径。

**Warning**

服务器使用 CGI 方式进行部署可能存在几个公开的缺陷。请阅读
<a href="/security/cgi-bin.html" class="link">CGI 安全</a>一章 以学习
如何抵御这些攻击。

如果想发布语法高亮的 php 文件，没有类似于模块方式下 PHP
那种方便的方法。如果选择了 CGI 方式运行 PHP，需要使用 <span
class="function">highlight\_file</span> 函数来进行语法高亮。创建一个 PHP
文件，加入下述代码即可：*\<?php
highlight\_file('some\_php\_script.php'); ?\>*。

### Microsoft Windows 下的 Apache 2.x

本节包括在 Microsoft Windows 系统中针对 Apache 2.x 安装 PHP
的指导与说明。在其它页面也有
<a href="/install/windows/legacy/index.html#install.windows.legacy.apache1" class="link">Apache 1.3.x 用户指导与说明</a>。

> **Note**:
>
> 应该先阅读<a href="/install/windows/legacy/index.html#install.windows.legacy.manual" class="link">手工安装步骤</a>！

> **Note**: **Apache 2.2 支持**  
>
> Apache 2.2 用户应留意对于 Apache 2.2 的 DLL 文件名是
> `php5apache2_2.dll` 而不是 `php5apache2.dll`，并且只在 PHP 5.2.0
> 以及更高版本中出现。参见 \[broken link\]。

强烈建议阅读
<a href="http://httpd.apache.org/docs/current/" class="link external">» Apache 文档</a>来加深对
Apache 2.x 服务器的基本理解。此外在继续下去之前考虑先阅读一下 Apache 2.x
的
<a href="http://httpd.apache.org/docs/current/platform/windows.html" class="link external">» Windows 下使用说明</a>。

Apache 2.x 被设计运行于 Windows 版的服务器平台下，例如 Windows NT
4.0，Windows 2000，Windows XP 或 Windows 7。虽然 Apache 2.x 可以在
Windows 9x
下勉强运行，但对此平台的支持尚未完成，某些功能无法正确工作。对此并无补救计划。

下载最新版本的
<a href="http://httpd.apache.org/" class="link external">» Apache 2.x</a>
以及适合的 PHP
版本。先完成<a href="/install/windows/manual.html" class="link">手工安装步骤</a>后再回来继续将
PHP 集成入 Apache。

Windows 下有三种方法使 PHP 工作于 Apache 2.x 之中。可以以
handler，CGI，或者 FastCGI 方式运行 PHP。

> **Note**: <span class="simpara">记住当在 Windows 环境下的 Apache
> 配置文件中添加路径值时，所有的反斜线，如
> `c:\directory\file.ext`，应转换为正斜线：
> `c:/directory/file.ext`。对目录来说，也必须由斜线结尾。</span>

#### 以 Apache handler 方式安装

需要将以下几行加入到 Apache 的 `httpd.conf` 配置文件中以加载 Apache 2.x
的 PHP 模块：

**示例 \#19 PHP 在 Apache 2.x 中作为 handler**

``` apache-conf
# 
LoadModule php5_module "c:/php/php5apache2.dll"
AddHandler application/x-httpd-php .php

# 配置 php.ini 的路径
PHPIniDir "C:/php"
```

> **Note**: <span class="simpara"> 记得用自己 PHP
> 实际所在的路径替换掉上例中的 `c:/php/`。要留意在 LoadModule
> 指令中使用了 `php5apache2.dll` 或者
> `php5apache2_2.dll`，并且该文件确实位于所指定的位置。 </span>

以上配置将使 PHP 处理任何具有 .php
后缀的文件，即使该文件还有其它的文件后缀。例如一个名为 `example.php.txt`
的文件将被作为 PHP 文件运行。要确保只有以 `.php`
*结尾*的文件才被执行，则用以下配置替换上面的：

``` apache-conf
<FilesMatch \.php$>
      SetHandler application/x-httpd-php
 </FilesMatch>
```

#### 以 CGI 方式运行 PHP

要更好地理解在 Apache 下运行 CGI，请参阅
<a href="http://httpd.apache.org/docs/current/howto/cgi.html" class="link external">» Apache CGI 文档</a>。

要将 PHP 以 CGI 方式运行，需要将 php-cgi 文件放入到用 ScriptAlias
指令所指定的 CGI 目录中。

然后需要给 PHP 文件中添加一 \#! 的行来指明 PHP 可执行文件的位置：

**示例 \#20 Apache 2.x 下 CGI 方式的 PHP**

    #!C:/php/php.exe
    <?php
      phpinfo();
    ?>

**Warning**

服务器使用 CGI 方式进行部署可能存在几个公开的缺陷。请阅读
<a href="/security/cgi-bin.html" class="link">CGI 安全</a>一章 以学习
如何抵御这些攻击。

#### 以 FastCGI 方式运行 PHP

以 FastCGI 方式运行 PHP 比起 CGI 方式有很多优点。设定的方式很直接：

从
<a href="http://httpd.apache.org/mod_fcgid/" class="link external">» http://httpd.apache.org/mod_fcgid/</a>
取得 mod\_fcgid，该站点有 Win32
可执行文件的下载。按照下载文件中的指示安装此模块。

按以下方法配置 web 服务器，注意用自己系统上的路径替换其中相应的内容：

**示例 \#21 配置 Apache 以 FastCGI 方式运行 PHP**

    LoadModule fcgid_module modules/mod_fcgid.so  

    # Where is your php.ini file?
    FcgidInitialEnv PHPRC        "c:/php" 

    AddHandler fcgid-script .php  
    FcgidWrapper "c:/php/php-cgi.exe" .php  

此时具有 .php 后缀的文件将被 PHP FastCGI 所解析执行。

### Microsoft Windows 下的 Sun，iPlanet 和 Netscape 服务器

本节包含针对在 Windows 下 Sun Java System web 服务器，Sun ONE web
服务器，iPlanet 和 Netscape 服务器的 PHP 安装说明与提示。

自 PHP 4.3.3 起可以通过
<a href="/ref/nsapi.html" class="link">NSAPI 模块</a>使用 PHP
脚本来<a href="/install/windows/legacy/index.html#install.windows.legacy.sun.specialpages" class="link">产生定制目录列表于错误页面</a>。也可以使用为兼容
Apache 的附加函数。目前使用的 web
服务器的支持请阅读<a href="/install/windows/legacy/index.html#install.windows.legacy.sun.notes" class="link">有关子请求的说明</a>。

#### Sun，iPlanet 和 Netscape 服务器的 CGI 方式安装

要将 PHP 安装为 CGI 处理器，按以下步骤进行：

-   <span class="simpara"> 将 `php4ts.dll` 拷贝到 systemroot（即 Windows
    的安装目录）； </span>

-   在命令行做文件关联，输入以下两行命令：

    ``` shell
    assoc .php=PHPScript
    ftype PHPScript=c:\php\php.exe %1 %*
    ```

-   <span class="simpara"> 在 Netscape Enterprise Administration Server
    中建一个空的 shellcgi 目录并随即删除（此步骤在 obj.conf 中新建了 5
    行重要指令以允许 web 服务器处理 shellcgi 脚本）； </span>

-   <span class="simpara"> 在 Netscape Enterprise Administration Server
    中新建一个新的 MIME 类型（Category: type，Content-Type:
    magnus-internal/shellcgi，File Suffix: php）； </span>

-   <span class="simpara"> 对每个要运行 PHP 的 web
    服务器实例都进行以上步骤。 </span>

更多将 PHP 设置为 CGI
可执行程序的内容见：<a href="http://benoit.noss.free.fr/php/install-php.html" class="link external">» http://benoit.noss.free.fr/php/install-php.html</a>。

#### Sun，iPlanet 和 Netscape 服务器的 NSAPI 方式

要将 PHP 以 NSAPI 方式安装，按以下步骤进行：

-   <span class="simpara"> 将 `php4ts.dll`拷贝到 systemroot（即 Windows
    的安装目录）； </span>

-   在命令行做文件关联，输入以下两行命令：

    ``` shell
    assoc .php=PHPScript
    ftype PHPScript=c:\php\php.exe %1 %*
    ```

-   <span class="simpara"> 在 Netscape Enterprise Administration Server
    中新建一个新的 MIME 类型（Category: type，Content-Type:
    magnus-internal/x-httpd-php，File Suffix: php）； </span>

-   编辑 `magnus.conf`（服务器版本 \>= 6）或 `obj.conf`（服务器版本 \<
    6）并加入下面两行；要将新行放在 *mime types init*之后：

        Init fn="load-modules" funcs="php4_init,php4_execute,php4_auth_trans" shlib="c:/php/sapi/php4nsapi.dll"
        Init fn="php4_init" LateInit="yes" errorString="Failed to initialise PHP!" [php_ini="c:/path/to/php.ini"]

    （PHP \>= 4.3.3）*php\_ini* 参数为可选项，但加上后就可以把 `php.ini`
    放到 web 服务器的配置目录中去；

-   在 `obj.conf` 中配置默认对象（对于虚拟服务器类 \[Sun web Server
    6.0+\] 是 `vserver.obj.conf`文件）：在 *\<Object name="default"\>*
    一节，在所有的“ObjectType”行之后和所有的“AddLog”行之前加上这一行：

        Service fn="php4_execute" type="magnus-internal/x-httpd-php" [inikey=value inikey=value ...]

    （PHP \>= 4.3.3）作为附加参数可以加入一些特殊的 `php.ini`
    值，例如可以在调用 *php4\_execute* 时设定专门的
    *docroot="/path/to/docroot"*。对于布尔的 ini 选项请用 0/1
    作为值，而不是 *"On","Off",...*（这样不能正确工作），例如要用
    *zlib.output\_compression=1* 而不是
    *zlib.output\_compression="On"*；

-   这几行仅在想要配置一个只有 PHP 脚本的目录时需要（类似 cgi-bin
    目录）：

        <Object name="x-httpd-php">
        ObjectType fn="force-type" type="magnus-internal/x-httpd-php"
        Service fn=php4_execute [inikey=value inikey=value ...]
        </Object>

    在此之后可以在管理服务器中配置目录并将其类型设为
    *x-httpd-php*。其中的所有文件都将作为 PHP 执行。这样可以隐藏 PHP
    的使用，文件名还保留为 `.html`；

-   <span class="simpara"> 重启动 web 服务使改动生效； </span>

-   <span class="simpara"> 对每个要运行 PHP 的 web
    服务器实例都进行以上步骤。 </span>

> **Note**:
>
> 更多将 PHP 设置为
> NSAPI内容见：<a href="http://benoit.noss.free.fr/php/install-php4.html" class="link external">» http://benoit.noss.free.fr/php/install-php4.html</a>。

> **Note**:
>
> PHP 使用的堆栈大小（stacksize）依赖于 web
> 服务器的配置。如果在运行很大的 PHP
> 脚本时死掉，建议在管理服务器中增大此值（在 "MAGNUS EDITOR" 一节中）。

#### CGI 环境以及推荐在 php.ini 中进行的修改

在写 PHP 脚本时很重要一点是 Sun JSWS/Sun ONE WS/iPlanet/Netscape
是多线程 web 服务器。因此所有的请求都运行于同一个进程空间（即 web
服务器自己的空间）而此空间只有一个环境。如果想取得 CGI 变量例如
*PATH\_INFO*，*HTTP\_HOST* 等时不能用老的 PHP 3.x 的方式 <span
class="function">getenv</span>
或者类似手段（*$\_ENV*）进行。只能取得运行的 web
服务器的环境变量而没有任何有效的 CGI 变量！

> **Note**:
>
> 为什么环境中有一些（无效的）CGI 变量？
>
> 解答：这是因为从管理服务器启动了 web 服务器进程，这将运行 web
> 服务器的启动脚本，而你想要启动的是 CGI 脚本（CGI
> 脚本在管理服务器内部！）。这是为什么 web 服务器启动的环境中有一些 CGI
> 环境变量的原因。可以不从管理服务器启动 web
> 服务器来试验一下。用管理员用户从命令行手工启动——这样就不会看到类似 CGI
> 的环境变量了。

PHP 4.x 中取得 CGI 变量的正确方式是使用超全局变量
`$_SERVER`。如果有一些老的脚本用了 `$HTTP_HOST` 等，那应该在 `php.ini`
中打开 *register\_globals* 选项并改变变量顺序（重要提示：去掉
*"E"*，因为这里不需要环境变量）：

    variables_order = "GPCS"
    register_globals = On

#### 错误页面的特殊使用或定制目录列表（PHP \>= 4.3.3）

可以用 PHP 来为 *"404 Not Found"*
或类似的错误提示生成错误页面。对每个想要覆盖的错误页面在 `obj.conf`
中的对象里加入下面这行：

    Error fn="php4_execute" code=XXX script="/path/to/script.php" [inikey=value inikey=value...]

其中的 *XXX* 是 HTTP 错误代码。删除掉可能干扰到自己设置的任何其它
*Error* 指令。如果对所有可能出现的错误都用同一个脚本处理，不要 *code*
参数即可。脚本里可以用 `$_SERVER['ERROR_TYPE']` 取得 HTTP 状态代码。

还可以生成自己定制的目录列表。只要创建一个显示目录列表的 PHP
脚本并用下面一行在 `obj.conf` 中替换掉相应
*type="magnus-internal/directory"* 默认的 Service 设置：

    Service fn="php4_execute" type="magnus-internal/directory" script="/path/to/script.php" [inikey=value inikey=value...]

对于错误和目录列表页面，原始的 URI 和转换后的 URI 都在变量
`$_SERVER['PATH_INFO']` 和 `$_SERVER['PATH_TRANSLATED']` 中。

#### 有关 <span class="function">nsapi\_virtual</span>和子请求（PHP \>= 4.3.3）的说明

NSAPI 模块现在支持 <span class="function">nsapi\_virtual</span>
函数（别名：<span
class="function">virtual</span>）来进行子请求并将结果插入到 web
页面里。问题是，此函数用到了一些 NSAPI 库中没有文档说明的特性。

在 Unix
下这不是问题，因为模块会自动寻找所需的函数并使用。如果找不到，<span
class="function">nsapi\_virtual</span> 被禁用。

在 Windows 下 DLL 处理的局限性需要使用最新的 `ns-httpdXX.dll`
文件中的自动检测功能。这已在版本 6.1
及以下的服务器中测试过。如果用了更高版本的 Sun 服务器，检测会失败并禁用
<span class="function">nsapi\_virtual</span>。

在这种情况下，试试下面的方法。在 `magnus.conf`/`obj.conf` 中的
*php4\_init* 里加入下面的参数：

    Init fn=php4_init ... server_lib="ns-httpdXX.dll"

其中 *XX* 是正确的 DLL 版本号。在 server-root 目录下去找合适的 DLL
的名字。文件大小最大的 DLL 就是了。

可以用 <span class="function">phpinfo</span> 函数来检查状态。

> **Note**:
>
> 但要注意：对 <span class="function">nsapi\_virtual</span>
> 的支持是试验性质的！

### Microsoft Windows 下的 Sambar 服务器

本节包含针对 Windows 下的
<a href="http://www.sambar.com/" class="link external">» Sambar 服务器</a>的说明和提示。

> **Note**:
>
> 应该首先阅读<a href="/install/windows/manual.html" class="link">手工安装步骤</a>！

下面列出了怎样在 Windows 下设置 Sambar 服务器的 ISAPI 模块。

-   在 Sambar 安装目录中找到 `mappings.ini`文件（在 config 目录中）；

-   打开 `mappings.ini` 并在 *\[ISAPI\]* 部分加入下面一行：

    **示例 \#22 Sambar 的 ISAPI 设置**

        #对 PHP 4
        *.php = c:\php\php4isapi.dll

        #对 PHP 5
        *.php = c:\php\php5isapi.dll

    （上面假定 PHP 安装在 `c:\php`。）

-   重启动 Sambar 服务器以使改动生效。

> **Note**:
>
> 如果想要用 PHP 与分布于网络中不同的主机上的资源通讯，则需要改变 Sambar
> 服务器的服务进程所使用的帐号。Sambar 服务进程使用的默认帐号是
> LocalSystem，没有远程资源的访问许可。可以通过 Windows
> 控制面板中的“管理工具”里面的“服务”来修改此帐号。

### Microsoft Windows 下的 Xitami

本节包含针对 Windows 下的
<a href="http://www.xitami.com/" class="link external">» Xitami</a>
的说明与提示。

> **Note**:
>
> 应该首先阅读<a href="/install/windows/manual.html" class="link">手工安装步骤</a>！

下面列出了怎样在 Windows 下在 Xitami 中设置 PHP 的 CGI 方式。

> **Note**: **CGI 用户重要提示**  
>
> 请阅读
> <a href="/faq/installation.html#faq.installation.forceredirect" class="link">FAQ：cgi.force_redirect</a>
> 中的重要细节。此选项需要被设为 *0*。如果想要使用
> *$\_SERVER\['PHP\_SELF'\]*，还必须激活
> <a href="/ini/core.html#ini.cgi.fix-pathinfo" class="link">cgi.fix_pathinfo</a>选项。

**Warning**

服务器使用 CGI 方式进行部署可能存在几个公开的缺陷。请阅读
<a href="/security/cgi-bin.html" class="link">CGI 安全</a>一章 以学习
如何抵御这些攻击。

-   确保 web 服务器在运行，在浏览器中打开 Xitami 的管理控制台（通常是
    *http://127.0.0.1/admin*），并点击 Configuration；

-   找到 Filters，在 File extensions（.xxx）字段中加入想要 PHP
    解析的后缀名（例如 .php）；

-   在 Filter command 或 script 中输入 PHP 的 CGI 可执行文件名，例如 PHP
    4 是 `C:\php\php.exe`，PHP 5 是 `C:\php\php-cgi.exe`；

-   点击“Save”图标；

-   重启动服务器以使改动生效。

### 从源程序编译

本章讲述了在 Windows 下如何使用 Microsoft 的工具编译 PHP。要在 CygWin
中编译 PHP，请参考
<a href="/install/unix.html" class="xref">Unix 系统下的安装</a> 一章。

具体内容见：<a href="https://wiki.php.net/internals/windows/stepbystepbuild" class="link external">» https://wiki.php.net/internals/windows/stepbystepbuild</a>。

### Windows 下安装扩展库

在 Windows 下安装完 PHP 和 web
服务器之后，可能想要安装一些扩展库来获得更多功能。可以通过修改 `php.ini`
来选择当 PHP 启动时加载哪些扩展库。也可以在脚本中通过使用 <span
class="function">dl</span>来动态加载。

PHP 扩展库的 DLL 文件都具有 *php\_* 前缀。

很多扩展库都 *内置于* Windows 版的 PHP
之中。这意味着要加载这些扩展库，额外的 DLL 文件和
<a href="/ini/core.html#ini.extension" class="link">extension</a>
配置指令都 *不需要*。Windows 下的
<a href="/install/windows/legacy/index.html#install.windows.legacy.extensions.overview" class="link">PHP 扩展库</a>
列表列出了需要或曾经需要额外 PHP DLL
文件的扩展库。下面是内置的扩展库列表（截止到 PHP 5.0.4）：
<a href="/book/bc.html" class="link">BCMath</a>,
<a href="/book/calendar.html" class="link">Calendar</a>,
<a href="/book/com.html" class="link">COM</a>,
<a href="/book/ctype.html" class="link">Ctype</a>,
<a href="/book/dom.html" class="link">DOM</a>,
<a href="/book/ftp.html" class="link">FTP</a>,
<a href="/book/libxml.html" class="link">LibXML</a>,
<a href="/book/iconv.html" class="link">Iconv</a>,
<a href="/book/uodbc.html" class="link">ODBC</a>,
<a href="/book/pcre.html" class="link">PCRE</a>,
<a href="/book/session.html" class="link">Session</a>,
<a href="/book/simplexml.html" class="link">SimpleXML</a>,
<a href="/book/spl.html" class="link">SPL</a>,
<a href="/book/sqlite.html" class="link">SQLite</a>,
<a href="/book/wddx.html" class="link">WDDX</a>,
<a href="/book/xml.html" class="link">XML</a> 和
<a href="/book/zlib.html" class="link">Zlib</a>.

PHP 搜索扩展库的默认位置在 `C:\php5`。要修改此项以符合用户自己的 PHP
设置，需要编辑 `php.ini` 文件：

-   需要修改
    <a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>
    设置以指向用户放置扩展库的目录或者说放置 `php_*.dll`
    文件的位置。例如：

    ``` ini
    extension_dir = C:\php\extensions
    ```

-   要在 `php.ini` 中启用某扩展库，需要去掉 `php.ini` 文件中该行
    *extension=php\_\*.dll*
    前的注释符号，将想要加载的扩展库前的分号（;）删除即可。

    **示例 \#23 在 Windows 下启用
    <a href="/book/bzip2.html" class="link">Bzip2</a> 扩展库**

    ``` ini
    // 将这一行
    ;extension=php_bz2.dll

    // 改成这样
    extension=php_bz2.dll
    ```

-   有些扩展库需要额外的 DLL
    才能工作。其中一部分包括在发行包里，在主目录下可以找到。但还有一些，例如
    Oracle（`php_oci8.dll`）所需要的 DLL 没有绑定在发行包里。别忘了将
    `C:\php` 放到系统路径 `PATH` 中去（此过程在另外的
    <a href="/faq/installation.html#faq.installation.addtopath" class="link">FAQ 条目</a>中有说明）。

-   某些 DLL 没有绑定在 PHP 发行包中，详情见每个扩展库的文档页。此外有关
    PECL 的说明见手册页
    <a href="/install/pecl.html" class="link">PECL 扩展库安装</a>。在
    PECL 中有日益增加数目巨大的 PHP 扩展库，这些扩展库需要
    <a href="/install/pecl/downloads.html" class="link">单独下载</a>。

> **Note**: <span class="simpara"> 如果运行服务器模块版的 PHP，在修改了
> `php.ini` 之后别忘了重新启动 web 服务器以使其改动生效。 </span>

下表说明了哪些扩展库需要额外的 DLL。

| 扩展库               | 说明                                                                              | 注解                                                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| php\_bz2.dll         | <a href="/book/bzip2.html" class="link">bzip2</a> 压缩函数                        | 无                                                                                                                                             |
| php\_calendar.dll    | <a href="/book/calendar.html" class="link">Calendar</a> 日历转换函数              | 无                                                                                                                                             |
| php\_ctype.dll       | <a href="/book/ctype.html" class="link">ctype</a> 家族函数                        | 无                                                                                                                                             |
| php\_curl.dll        | <a href="/book/curl.html" class="link">CURL</a>，客户端 URL 库函数                | 需要：`libeay32.dll`，`ssleay32.dll`（已附带），在 OpenSSL 1.1 版本里需要：`libcrypto-*.dll` and `libssl-*.dll` (已附带)                       |
| php\_dba.dll         | <a href="/book/dba.html" class="link">DBA</a>：数据库（dbm 风格）抽象层函数       | 无                                                                                                                                             |
| php\_dbase.dll       | <a href="/book/dbase.html" class="link">dBase</a> 函数                            | 无                                                                                                                                             |
| php\_dbx.dll         | <a href="/book/dbx.html" class="link">dbx</a> 函数                                | 无                                                                                                                                             |
| php\_exif.dll        | <a href="/book/exif.html" class="link">EXIF</a> 函数                              | 需要 <a href="/book/mbstring.html" class="link">php_mbstring.dll</a>。并且在 `php.ini` 中，`php_exif.dll` 必须在 `php_mbstring.dll` *之后*加载 |
| php\_fbsql.dll       | <a href="/book/fbsql.html" class="link">FrontBase</a> 函数                        | 无                                                                                                                                             |
| php\_fdf.dll         | <a href="/book/fdf.html" class="link">FDF</a>：表单数据格式化函数                 | 需要：`fdftk.dll`（已附带）                                                                                                                    |
| php\_filepro.dll     | <a href="/book/filepro.html" class="link">filePro</a> 函数                        | 只读访问                                                                                                                                       |
| php\_ftp.dll         | <a href="/book/ftp.html" class="link">FTP</a> 函数                                | 无                                                                                                                                             |
| php\_gd2.dll         | <a href="/book/image.html" class="link">GD</a> 库图像函数                         | GD2                                                                                                                                            |
| php\_gettext.dll     | <a href="/book/gettext.html" class="link">Gettext</a> 函数                        | PHP \<= 4.2.0 需要 `gnu_gettext.dll`（已附带），PHP \>= 4.2.3 需要 `libintl-1.dll`， `iconv.dll`（已附带）                                     |
| php\_hyperwave.dll   | HyperWave 函数                                                                    | 无                                                                                                                                             |
| php\_iconv.dll       | <a href="/book/iconv.html" class="link">ICONV</a> 字符集转换                      | 需要：`iconv-1.3.dll`（已附带），`iconv.dll`                                                                                                   |
| php\_ifx.dll         | <a href="/book/ifx.html" class="link">Informix</a> 函数                           | 需要：Informix 库                                                                                                                              |
| php\_iisfunc.dll     | IIS 管理函数库                                                                    | 无                                                                                                                                             |
| php\_imap.dll        | <a href="/book/imap.html" class="link">IMAP</a>，POP3 和 NNTP 函数                | 无                                                                                                                                             |
| php\_ingres.dll      | <a href="/book/ingres.html" class="link">Ingres II</a> 函数                       | 需要：Ingres II 库                                                                                                                             |
| php\_interbase.dll   | <a href="/book/ibase.html" class="link">InterBase</a> 函数                        | 需要：`gds32.dll`（已附带）                                                                                                                    |
| php\_ldap.dll        | <a href="/book/ldap.html" class="link">LDAP</a> 函数                              | 需要 ： `libeay32.dll`，`ssleay32.dll`（已附带）。在 OpenSSL 1.1 里需要： `libcrypto-*.dll` 和 `libssl-*.dll` (已附带)                         |
| php\_mbstring.dll    | <a href="/book/mbstring.html" class="link">Multi-Byte String</a> 多字节字符串函数 | 无                                                                                                                                             |
| php\_mcrypt.dll      | <a href="/book/mcrypt.html" class="link">Mcrypt 加密</a>函数                      | 需要：`libmcrypt.dll`                                                                                                                          |
| php\_mhash.dll       | <a href="/book/mhash.html" class="link">Mhash</a> 函数                            | 需要：`libmhash.dll`（已附带）                                                                                                                 |
| php\_mime\_magic.dll | <a href="/book/mime-magic.html" class="link">Mimetype</a> 函数                    | 需要：`magic.mime`（已附带）                                                                                                                   |
| php\_msql.dll        | <a href="/book/msql.html" class="link">mSQL</a> 函数                              | 需要：`msql.dll`（已附带）                                                                                                                     |
| php\_mysql.dll       | <a href="/set/mysqlinfo.html#Mysql（原始）" class="link">MySQL</a> 函数           | 需要：`libmysql.dll`（已附带）                                                                                                                 |
| php\_mysqli.dll      | <a href="/set/mysqlinfo.html#Mysqli" class="link">MySQLi</a> 函数                 | 需要：`libmysql.dll`（PHP \<= 5.0.2 中是 `libmysqli.dll`）（已附带）                                                                           |
| php\_oci8.dll        | <a href="/book/oci8.html" class="link">Oracle 8</a> 函数                          | 需要：Oracle 8.1+ 客户端库                                                                                                                     |
| php\_openssl.dll     | <a href="/book/openssl.html" class="link">OpenSSL</a> 函数                        | 需要：`libeay32.dll`（已附带）                                                                                                                 |
| php\_pdf.dll         | <a href="/book/pdf.html" class="link">PDF</a> 函数                                | 无                                                                                                                                             |
| php\_pgsql.dll       | <a href="/book/pgsql.html" class="link">PostgreSQL</a> 函数                       | 无                                                                                                                                             |
| php\_shmop.dll       | <a href="/book/shmop.html" class="link">Shared Memory</a> 共享内存函数            | 无                                                                                                                                             |
| php\_snmp.dll        | <a href="/book/snmp.html" class="link">SNMP</a> 函数                              | 仅用于 Windows NT！                                                                                                                            |
| php\_soap.dll        | <a href="/book/soap.html" class="link">SOAP</a> 函数                              | 无                                                                                                                                             |
| php\_sockets.dll     | <a href="/book/sockets.html" class="link">Socket</a> 函数                         | 无                                                                                                                                             |
| php\_tidy.dll        | <a href="/book/tidy.html" class="link">Tidy</a> 函数                              | 无                                                                                                                                             |
| php\_tokenizer.dll   | <a href="/book/tokenizer.html" class="link">Tokenizer</a> 函数                    | 无                                                                                                                                             |
| php\_w32api.dll      | W32api 函数                                                                       | 无                                                                                                                                             |
| php\_xmlrpc.dll      | <a href="/book/xmlrpc.html" class="link">XML-RPC</a> 函数                         | 需要：`iconv.dll`（已附带）                                                                                                                    |
| php\_xslt.dll        | XSLT 函数                                                                         | 需要：`sablot.dll`，`expat.dll`， `iconv.dll`（已附带）。                                                                                      |
| php\_yaz.dll         | <a href="/book/yaz.html" class="link">YAZ</a> 函数                                | 需要：`yaz.dll`（已附带）                                                                                                                      |
| php\_zip.dll         | <a href="/book/zip.html" class="link">Zip 文件</a>函数                            | 只读访问                                                                                                                                       |
| php\_zlib.dll        | <a href="/book/zlib.html" class="link">ZLib</a> 压缩函数                          | 无                                                                                                                                             |

### PHP 在 Microsoft Windows 下的命令行方式

本章包含有针对在 Windows 下以命令行运行 PHP 的说明与提示。

> **Note**:
>
> 应该先阅读<a href="/install/windows/legacy/index.html#install.windows.legacy.manual" class="link">手工安装步骤</a>！

要在命令行下运行 PHP，可以无需对 Windows 做任何改动。

    C:\PHP5\php.exe -f "C:\PHP Scripts\script.php" -- -arg1 -arg2 -arg3

但是有几个很容易的步骤可以使其更加简便。某些步骤可能已经在之前完成了，不过还是在这里重复说明以便提供一个完整的步骤序列。

-   将 PHP 可执行文件（`php.exe`，`php-win.exe` 或者
    `php-cli.exe`）的路径添加到 `PATH` 环境变量中去。如何将 PHP
    目录添加到 `PATH`
    中请参阅<a href="/faq/installation.html#faq.installation.addtopath" class="link">与之相关的常见问题</a>。

-   将 *.PHP* 后缀添加到 `PATHEXT` 环境变量中去。可以在修改 `PATH`
    环境变量时同时进行。跟<a href="/faq/installation.html#faq.installation.addtopath" class="link">常见问题</a>中说明的步骤一样，不要要修改的是
    `PATHEXT` 环境变量而不是 `PATH` 环境变量。

    > **Note**:
    >
    > 把 *.PHP* 放置到什么位置将决定具有相同文件名时运行的优先级。例如将
    > *.PHP* 放到 *.BAT* 之前将导致如果有同名的 PHP 脚本和批处理文件，则
    > PHP 脚本会运行。

-   将 *.PHP* 后缀关联为一种文件类型，用以下命令完成：

        assoc .php=phpfile

-   将 *phpfile* 文件类型关联到适当的 PHP 可执行文件，用以下命令完成：

        ftype phpfile="C:\PHP5\php.exe" -f "%1" -- %~2

按照以上步骤将使 PHP 脚本可以在任何目录下运行，不需要输入 PHP
可执行文件名以及 *.PHP* 后缀，并且所有参数都会被传递给脚本来处理。

以下例子说明了可以手工修改的注册表项目变化。

**示例 \#24 注册表变化**

    Windows Registry Editor Version 5.00

    [HKEY_LOCAL_MACHINE\SOFTWARE\Classes\.php]
    @="phpfile"
    "Content Type"="application/php"

    [HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile]
    @="PHP Script"
    "EditFlags"=dword:00000000
    "BrowserFlags"=dword:00000008
    "AlwaysShowExt"=""

    [HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\DefaultIcon]
    @="C:\\PHP5\\php-win.exe,0"

    [HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\shell]
    @="Open"

    [HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\shell\Open]
    @="&Open"

    [HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\shell\Open\command]
    @="\"C:\\PHP5\\php.exe\" -f \"%1\" -- %~2"

有了这些改变之后，本页顶端第一个例子中的命令可以写成这样：

    "C:\PHP Scripts\script" -arg1 -arg2 -arg3

或者如果 *"C:\\PHP Scripts"* 路径位于 *PATH* 环境变量中的话：

    script -arg1 -arg2 -arg3

> **Note**:
>
> 不过如果想要通过此技巧将 PHP
> 脚本作为命令行管道过滤器的话，有个小问题。例如以下例子：
>
>     dir | "C:\PHP Scripts\script" -arg1 -arg2 -arg3
>
> 或者
>
>     dir | script -arg1 -arg2 -arg3
>
> 此时脚本会死掉，没有输出任何内容。要解决此问题，还需要做一个注册表修改。
>
>     Windows Registry Editor Version 5.00
>
>     [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\policies\Explorer]
>     "InheritConsoleHandles"=dword:00000001
>
> 有关此问题的更多信息见<a href="http://support.microsoft.com/default.aspx?scid=kb;en-us;321788" class="link external">» 微软知识库文章：321788</a>。
