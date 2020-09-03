在 Windows 上手动安装 PHP
-------------------------

### 选择 Web 服务器

#### IIS

IIS 是 Windows 内置的服务。在 Windows
服务器版本上，请使用服务器管理（Server Manager）来添加 IIS
规则。同时需要设置 CGI 角色规则。在 Windows
桌面版本上，需要使用控制面板中的 "添加/删除程序" 功能来添加
IIS。请参阅微软的官方文档的
<a href="https://docs.microsoft.com/en-us/previous-versions/ms181052(v=vs.80)" class="link external">» 详细说明</a>。
对于桌面 web app 开发者，你也可以选择 IIS/Express 或 PHP Desktop。

**示例 \#1 命令行下配置 IIS 和 PHP**


    @echo off

    REM download .ZIP file of PHP build from http://windows.php.net/downloads/

    REM path to directory you decompressed PHP .ZIP file into (no trailing \)
    set phppath=c:\php


    REM Clear current PHP handlers
    %windir%\system32\inetsrv\appcmd clear config /section:system.webServer/fastCGI
    REM The following command will generate an error message if PHP is not installed. This can be ignored.
    %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /-[name='PHP_via_FastCGI']

    REM Set up the PHP handler
    %windir%\system32\inetsrv\appcmd set config /section:system.webServer/fastCGI /+[fullPath='%phppath%\php-cgi.exe']
    %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /+[name='PHP_via_FastCGI',path='*.php',verb='*',modules='FastCgiModule',scriptProcessor='%phppath%\php-cgi.exe',resourceType='Unspecified']
    %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /accessPolicy:Read,Script

    REM Configure FastCGI Variables
    %windir%\system32\inetsrv\appcmd set config -section:system.webServer/fastCgi /[fullPath='%phppath%\php-cgi.exe'].instanceMaxRequests:10000
    %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi /+"[fullPath='%phppath%\php-cgi.exe'].environmentVariables.[name='PHP_FCGI_MAX_REQUESTS',value='10000']"
    %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi /+"[fullPath='%phppath%\php-cgi.exe'].environmentVariables.[name='PHPRC',value='%phppath%\php.ini']"

请参阅：<a href="/install/windows/legacy/index.html#install.windows.legacy.iis7" class="link">旧版本的 IIS 配置</a>。

#### Apache

There are several builds of Apache2 for Windows. The Apache builds of
ApacheLounge are recommended, but other options include XAMPP,
WampServer and BitNami, which provide automatic installer tools. PHP can
be used on Apache through mod\_php or mod\_fastcgi. mod\_php requires a
TS build of Apache built with same version of Visual C and same CPU (x86
or x64).
请参阅：<a href="/install/windows/legacy/index.html#install.windows.legacy.apache2" class="link">旧版本的 Apache 配置</a>。

### 选择编译版本

从 Windows 专用站点下载适合产品环境使用的 PHP 预编译版本：
<a href="http://windows.php.net/download/" class="link external">» http://windows.php.net/download/</a>。All
builds are optimized (PGO), and QA and GA releases are thoroughly
tested.

There are 4 types of PHP builds:

-   Thread-Safe(TS) - use for single process web servers, like Apache
    with mod\_php

-   Non-Thread-Safe(NTS) - use for IIS and other FastCGI web servers
    (Apache with mod\_fastcgi) and recommended for command-line scripts

-   x86 - production use of PHP 5.5 or 5.6 or 7.0.

-   x64 - production use of PHP 7.0+ unless its a 32-bit only version of
    Windows. 5.5 and 5.6 x64 are experimental.
