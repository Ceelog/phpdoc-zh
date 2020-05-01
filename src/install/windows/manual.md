Manual PHP Installation on Windows
----------------------------------

### Choose Web Server

-   IIS is builtin to Windows. On Windows Server, use Server Manager to
    add the IIS role. Be sure to include the CGI Role Feature. On
    Windows Desktop, use Control Panel's Add/Remove Programs to add IIS.
    See:
    <a href="https://msdn.microsoft.com/en-us/library/ms181052%28v=vs.80%29.aspx?f=255&amp;MSPPError=-2147217396" class="link external">» https://msdn.microsoft.com/en-us/library/ms181052%28v=vs.80%29.aspx?f=255&amp;MSPPError=-2147217396</a>
    For desktop web apps and web-development, you can also use
    IIS/Express or PHP Desktop

    **示例 \#1 Command line to configure IIS and PHP**


            @echo off

            REM download .ZIP file of PHP build from http://windows.php.net/downloads/
            REM
            REM path to directory you decompressed PHP .ZIP file into
        set phpdir=c:\php
        set phppath=php-5.6.19-nts-Win32-VC11-x86

        REM Clear current PHP handlers
        %windir%\system32\inetsrv\appcmd clear config /section:system.webServer/fastCGI
        %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /-[name='PHP_via_FastCGI']

        REM Set up the PHP handler
        %windir%\system32\inetsrv\appcmd set config /section:system.webServer/fastCGI /+[fullPath='%phpdir%\%phppath%\php-cgi.exe']
        %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /+[name='PHP_via_FastCGI',path='*.php',verb='*',modules='FastCgiModule',scriptProcessor='%phpdir%\%phppath%\php-cgi.exe',resourceType='Unspecified']
        %windir%\system32\inetsrv\appcmd set config /section:system.webServer/handlers /accessPolicy:Read,Script

        REM Configure FastCGI Variables
        %windir%\system32\inetsrv\appcmd set config -section:system.webServer/fastCgi /[fullPath='%phpdir%\%phppath%\php-cgi.exe'].instanceMaxRequests:10000
        %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi /+"[fullPath='%phpdir%\%phppath%\php-cgi.exe'].environmentVariables.[name='PHP_FCGI_MAX_REQUESTS',value='10000']"
        %windir%\system32\inetsrv\appcmd.exe set config -section:system.webServer/fastCgi /+"[fullPath='%phpdir%\%phppath%\php-cgi.exe'].environmentVariables.[name='PHPRC',value='%phpdir%\%phppath%\php.ini']"

    <a href="/install/windows/legacy/index.html#install.windows.legacy.iis7" class="link">How to manually configure IIS</a>

-   There are several builds of Apache2 for Windows. We support
    ApacheLounge, but other options include XAMPP, WampServer and
    BitNami, which provide automatic installer tools. You may use
    mod\_php or mod\_fastcgi to load PHP on Apache. If you use mod\_php,
    you MUST use a TS build of Apache built with same version of Visual
    C and same CPU (x86 or x64).
    <a href="/install/windows/legacy/index.html#install.windows.legacy.apache2" class="link">How to manually configure Apache2</a>

### Choose Build

Download PHP production releases from
<a href="http://windows.php.net/download/" class="link external">» http://windows.php.net/download/</a>.
A lot of testing and optimization is already done on the snapshot and qa
releases, but you are welcome to help us do more. There are 4 types of
PHP builds:

-   Thread-Safe(TS) - use for single process web servers, like Apache
    with mod\_php

-   Non-Thread-Safe(NTS) - use for IIS and other FastCGI web servers
    (Apache with mod\_fastcgi) and recommended for command-line scripts

-   x86 - production use of PHP 5.5 or 5.6 or 7.0.

-   x64 - production use of PHP 7.0+ unless its a 32-bit only version of
    Windows. 5.5 and 5.6 x64 are experimental.
