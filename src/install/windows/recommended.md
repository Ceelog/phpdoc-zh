Windows 系统下的推荐配置
------------------------

### OpCache

强烈建议开启 OpCache。此扩展默认已经包含到 PHP Windows
版本中。它会自动编译和优化 PHP
脚本，并将它们缓存在内存中，这样就不会在每次加载页面时动态编译它们。

在 php.ini 配置中，设置

**示例 \#1 推荐的 OpCache 配置**

    zend_extension=php_opcache.dll
    opcache.enable=On
    opcache.enable_cli=On

然后重新启动你的 WEB
服务器。更多信息，请参阅：<a href="/opcache/setup.html#运行时配置" class="link">OpCache 配置</a>
章节。

### WinCache

WinCache 推荐在 IIS
下使用，尤其是在共享虚拟主机环境中或使用网络文件存储（NAS）时。所有 PHP
应用程序都会自动受益于 WinCache
的文件缓存功能。文件系统操作被缓存在内存中。 WinCache
还可以缓存内存中的用户对象，并在 `php.exe` 或 `php-cgi.exe`
进程之间共享它们（在请求之间共享对象）。许多主流的
Web应用程序都有一个插件或扩展或配置选项来使用 WinCache
用户对象缓存。如果你需要高性能，你应该在你的应用程序中使用对象缓存。请参阅：<a href="http://pecl.php.net/package/WinCache" class="link external">» http://pecl.php.net/package/WinCache</a>
to download a WinCache DLL (or tgz) to your PHP extensions directory
(extensions\_dir in your php.ini)。 在 php.ini 配置中，设置

**示例 \#2 推荐的 WinCache 配置**


    extension=php_wincache.dll
    wincache.fcenabled=1
    wincache.ocenabled=1 ; removed as of wincache 2.0.0.0

更多信息，请参阅：<a href="http://php.net/manual/en/wincache.configuration.php" class="link external">» http://php.net/manual/en/wincache.configuration.php</a>

### IIS 配置

在 IIS 管理器中，安装 FastCGI 模块，并将 `` `.php` `` 后缀映射到
`PHP-CGI.exe` 文件的真实路径 (注意：不是 `PHP.exe`)

你可以使用 APPCMD 命令行工具来编写 IIS 配置脚本。

### 数据库

如果你需要一个数据库服务器，PHP
提供了对应的扩展来使用它们。如果你的网站没有太多的流量，你可以将数据库服务器与你的
Web 服务器运行在同一台服务器上。世面上流行的数据库，基本都会提供运行在
Windows 上的版本。

PHP 内置了 mysqli 和 pdo\_mysql 扩展。PHP 5.5 和 5.6 内置了 mysql
扩展(7.0 版本中被废弃)。

参见
<a href="https://dev.mysql.com/downloads/windows/" class="link external">» https://dev.mysql.com/downloads/windows/</a>
