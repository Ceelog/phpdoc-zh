Recommended Configuration on Windows systems
--------------------------------------------

### OpCache

Highly Recommended that you enable OpCache. This extension is included
with PHP for Windows. It compiles and optimizes PHP scripts and caches
them in memory so that they aren't compiled every time the page is
loaded.

In your php.ini, set

**示例 \#1 Recommended OpCache configuration**

    zend_extension=php_opcache.dll
    opcache.enable=On
    opcache.enable_cli=On

And restart your web server. For more info, see:
<a href="/opcache/setup.html#运行时配置" class="link">OpCache Configuration</a>

### WinCache

Recommended that you use WinCache if using IIS, especially if in a
shared web hosting environment or using networked file storage (NAS).
All PHP Applications automatically benefit from WinCache's file cache
feature. File system operations are cached in memory. WinCache also can
cache user objects in memory and share them between `php.exe` or
`php-cgi.exe` processes (share objects between requests). Many major web
applications have a plugin or extension or configuration option to make
use of the WinCache user object cache. If you need high performance, you
should use the object cache in your applications. See:
<a href="http://pecl.php.net/package/WinCache" class="link external">» http://pecl.php.net/package/WinCache</a>
to download a WinCache DLL (or tgz) to your PHP extensions directory
(extensions\_dir in your php.ini). In your php.ini, set

**示例 \#2 Recommended WinCache configuration**


    extension=php_wincache.dll
    wincache.fcenabled=1
    wincache.ocenabled=1 ; removed as of wincache 2.0.0.0

For more info, see:
<a href="http://php.net/manual/en/wincache.configuration.php" class="link external">» http://php.net/manual/en/wincache.configuration.php</a>

### IIS Configuration

In IIS Manager, Install FastCGI module and add a handler mapping for
`` `.php` `` to the path to `PHP-CGI.exe` (not `PHP.exe`)

You may use the APPCMD command line tool to script IIS configuration.

### Database

You'll probably need a Database Server. Popular databases provide PHP
extensions to use them. If your web site doesn't get a lot of traffic,
you can run your database server on the same server as your web server.
Many popular database servers run on Windows.

PHP includes mysqli and pdo\_mysql extensions. PHP 5.5 and 5.6 include
mysql extension (deprecated in 7.0).

See
<a href="https://dev.mysql.com/downloads/windows/" class="link external">» https://dev.mysql.com/downloads/windows/</a>
