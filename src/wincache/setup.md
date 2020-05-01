安装／配置
==========

**目录**

-   [需求](/wincache/setup.html#需求)
-   [安装](/wincache/setup.html#安装)
-   [运行时配置](/wincache/setup.html#运行时配置)
-   [WinCache Statistics
    Script](/wincache/setup.html#WinCache%20Statistics%20Script)
-   [WinCache Session
    Handler](/wincache/setup.html#WinCache%20Session%20Handler)
-   [WinCache Functions
    Reroutes](/wincache/setup.html#WinCache%20Functions%20Reroutes)
-   [资源类型](/wincache/setup.html#资源类型)

需求
----

The extension is currently supported only on the following
configurations:

Windows OS:

-   <span class="simpara">Windows XP SP3 with IIS 5.1 and
    <a href="http://www.iis.net/extensions/fastcgi" class="link external">» FastCGI Extension</a></span>
-   <span class="simpara">Windows Server 2003 with IIS 6.0 and
    <a href="http://www.iis.net/extensions/fastcgi" class="link external">» FastCGI Extension</a></span>
-   <span class="simpara">Windows Vista SP1 with IIS 7.0 and FastCGI
    Module</span>
-   <span class="simpara">Windows Server 2008 with IIS 7.0 and FastCGI
    Module</span>
-   <span class="simpara">Windows 7 with IIS 7.5 and FastCGI
    Module</span>
-   <span class="simpara">Windows Server 2008 R2 with IIS 7.5 and
    FastCGI Module</span>

PHP:

-   <span class="simpara">PHP 5.2.X, Non-thread-safe build</span>
-   <span class="simpara">PHP 5.3 X86, Non-thread-safe VC9 build</span>

> **Note**: <span class="simpara"> The WinCache Extension can only be
> used when IIS is configured to run PHP via FastCGI. </span>

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/wincache" class="link external">» https://pecl.php.net/package/wincache</a>.

There are two packages for this extension: one package is for PHP
versions 5.2.X, and the other package is for PHP 5.3.X. Select the
package that is appropriate for the PHP version being used.

To install and enable the extension, follow these steps:

1.  Unpack the package into some temporary location.

2.  Copy the `php_wincache.dll` file into the PHP extensions folder.
    Typically this folder is called "ext" and it is located in the same
    folder with all PHP binary files. For example:
    `C:\Program Files\PHP\ext`.

3.  Using a text editor, open the php.ini file, which is usually located
    in the same folder where all PHP binary files are. For example:
    `C:\Program Files\PHP\php.ini`.

4.  Add the following line at the end of the php.ini file: *extension =
    php\_wincache.dll*.

5.  Save and close the `php.ini` file.

6.  Recycle the IIS Application Pools for PHP to pick up the
    configuration changes. To check that the extension has been enabled,
    create a file called `phpinfo.php` with a PHP code that calls
    <a href="/ref/info.html#phpinfo" class="link">phpinfo</a> function.

7.  Save the `phpinfo.php` file in the root folder of a IIS web site
    that uses PHP, then open a browser and make a request to
    http://localhost/phpinfo.php. Search within the returned web page
    for a section called *wincache*. If the extension is enabled, then
    the <a href="/ref/info.html#phpinfo" class="link">phpinfo</a> output
    will list the configuration settings provided by the WinCache.

> **Note**: <span class="simpara"> Do not forget to remove `phpinfo.php`
> file from the web site's root folder after verifying that extension
> has been enabled. </span>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

The following table lists and explains the configuration settings
provided by the WinCache extension:

| 名字                                                                      | 默认   | Minimum | Maximum | 可修改范围                           | 更新日志                                                |
|---------------------------------------------------------------------------|--------|---------|---------|--------------------------------------|---------------------------------------------------------|
| <a href="/wincache/setup.html#" class="link">wincache.fcenabled</a>       | "1"    | "0"     | "1"     | PHP\_INI\_ALL                        | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.fcenabledfilter</a> | "NULL" | "NULL"  | "NULL"  | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.fcachesize</a>      | "24"   | "5"     | "255"   | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.fcndetect</a>       | "1"    | "0"     | "1"     | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.1.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.maxfilesize</a>     | "256"  | "10"    | "2048"  | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.ocenabled</a>       | "1"    | "0"     | "1"     | PHP\_INI\_ALL                        | Available as of WinCache 1.0.0. Removed as of 2.0.0.0   |
| <a href="/wincache/setup.html#" class="link">wincache.ocenabledfilter</a> | "NULL" | "NULL"  | "NULL"  | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0. Removed as of 2.0.0.0   |
| <a href="/wincache/setup.html#" class="link">wincache.ocachesize</a>      | "96"   | "15"    | "255"   | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0. Removed as of 2.0.0.0   |
| <a href="/wincache/setup.html#" class="link">wincache.filecount</a>       | "4096" | "1024"  | "16384" | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.chkinterval</a>     | "30"   | "0"     | "300"   | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.ttlmax</a>          | "1200" | "0"     | "7200"  | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.enablecli</a>       | 0      | 0       | 1       | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.ignorelist</a>      | NULL   | NULL    | NULL    | PHP\_INI\_ALL                        | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.namesalt</a>        | NULL   | NULL    | NULL    | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.0.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.ucenabled</a>       | 1      | 0       | 1       | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.1.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.ucachesize</a>      | 8      | 5       | 85      | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.1.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.scachesize</a>      | 8      | 5       | 85      | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.1.0                          |
| <a href="/wincache/setup.html#" class="link">wincache.rerouteini</a>      | NULL   | NULL    | NULL    | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.2.0. Removed as of 1.3.7     |
| <a href="/wincache/setup.html#" class="link">wincache.reroute_enabled</a> | 1      | 0       | 1       | PHP\_INI\_SYSTEM \| PHP\_INI\_PERDIR | Available as of WinCache 1.3.7                          |
| <a href="/wincache/setup.html#" class="link">wincache.srwlocks</a>        | 1      | 0       | 1       | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.3.6.3. Removed as of 2.0.0.0 |
| <a href="/wincache/setup.html#" class="link">wincache.filemapdir</a>      | NULL   | NULL    | NULL    | PHP\_INI\_SYSTEM                     | Available as of WinCache 1.3.7.4                        |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`wincache.fcenabled` <span class="type">boolean</span>  
<span class="simpara">Enables or disables the file cache
functionality.</span>

`wincache.fcenabledfilter` <span class="type">string</span>  
<span class="simpara"> Defines a comma-separated list of IIS web site
identifiers where file cache should be enabled or disabled. This setting
works in conjunction with *wincache.fcenabled*: if *wincache.fcenabled*
is set to 1, then the sites listed in the *wincache.fcenabledfilter*
will have the file cache turned off; if *wincache.fcenabled* is set to
0, then the sites listed in the *wincache.fcenabledfilter* will have the
file cache turned on. </span>

`wincache.fcachesize` <span class="type">integer</span>  
<span class="simpara"> Defines the maximum memory size (in megabytes)
that is allocated for the file cache. If the total size of all the
cached files exceeds the value specified in this setting, then most
stale files will be removed from the file cache. </span>

`wincache.fcndetect` <span class="type">boolean</span>  
<span class="simpara"> Enables or disables the file change notification
detection functionality. If file change notification is supported then
it will be used to refresh the opcode and file cache entries as soon as
the corresponding files are modified on a file system. If file change
notification is not supported, for example when using network file
shares, then wincache will poll for file changes at regular time
intervals specified by *wincache.chkinterval*. </span>

`wincache.maxfilesize` <span class="type">integer</span>  
<span class="simpara"> Defines the maximum allowed size (in kilobytes)
for a single file to be cached. If a file size exceeds the specified
value, the file will not be cached. This setting applies to the file
cache only. </span>

`wincache.ocenabled` <span class="type">boolean</span>  
**Warning**
This option has been *REMOVED* as of 2.0.0.0

<span class="simpara">Enables or disables the opcode cache
functionality</span>

`wincache.ocenabledfilter` <span class="type">string</span>  
**Warning**
This option has been *REMOVED* as of 2.0.0.0

<span class="simpara"> Defines a comma-separated list of IIS web site
identifiers where opcode cache should be enabled or disabled. This
setting works in conjunction with *wincache.ocenabled*: if
*wincache.ocenabled* is set to 1, then the sites listed in the
*wincache.ocenabledfilter* will have the opcode cache turned off; if
*wincache.ocenabled* is set to 0, then the sites listed in the
*wincache.ocenabledfilter* will have the opcode cache turned on. </span>

`wincache.ocachesize` <span class="type">integer</span>  
**Warning**
This option has been *REMOVED* as of 2.0.0.0

<span class="simpara"> Defines the maximum memory size (in megabytes)
that is allocated for the opcode cache. If the cached opcode size
exceeds the specified value, then most stale opcode will be removed from
the cache. Note that the opcode cache size must be at least 3 times
bigger than file cache size. If that is not the case the opcode cache
size will be automatically increased. </span>

`wincache.filecount` <span class="type">integer</span>  
<span class="simpara"> Defines how many files are expected to be cached
by the extension, so that appropriate memory size is allocated at the
startup time. If the number of files exceeds the specified value, the
WinCache will re-allocate more memory as needed. </span>

`wincache.chkinterval` <span class="type">integer</span>  
<span class="simpara"> Defines how often (in seconds) the extension
checks for file changes in order to refresh the cache. Setting it to 0
will disable the refreshing of the cache. The file changes will not be
reflected in the cache unless the cache entry for that file is removed
by scavenger or IIS application pool is recycled or
wincache\_refresh\_if\_changed function is called. </span>

`wincache.ttlmax` <span class="type">integer</span>  
<span class="simpara"> Defines the maximum time to live (in seconds) for
a cached entry without being used. Setting it to 0 will disable the
cache scavenger, so the cached entries will never be removed from the
cache during the lifetime of the IIS worker process. </span>

`wincache.enablecli` <span class="type">boolean</span>  
<span class="simpara"> Defines if caching is enabled when PHP is running
in command line (CLI) mode. </span>

`wincache.ignorelist` <span class="type">string</span>  
Defines a list of files that should not be cached by the extension. The
files list is specified by using file names only, separated by the pipe
symbol - "\|".

**示例 \#1 *wincache.ignorelist* example**

``` ini
wincache.ignorelist = "index.php|misc.php|admin.php"
```

`wincache.namesalt` <span class="type">string</span>  
<span class="simpara"> Defines a string that will be used when naming
the extension specific objects that are stored in shared memory. This is
used to avoid conflicts that may be caused if other applications within
an IIS worker process tries to access shared memory. The length of the
namesalt string cannot exceed 8 characters. </span>

`wincache.ucenabled` <span class="type">boolean</span>  
<span class="simpara"> Enables or disables the user cache functionality.
</span>

`wincache.ucachesize` <span class="type">integer</span>  
<span class="simpara"> Defines the maximum memory size in megabytes that
is allocated for the user cache. If the total size of variables stored
in the user cache exceeds the specified value, then the most stale
variables will be removed from the cache. </span>

`wincache.scachesize` <span class="type">integer</span>  
<span class="simpara"> Defines the maximum memory size in megabytes that
is allocated for the session cache. If the total size of data stored in
the session cache exceeds the specified value, then the most stale data
will be removed from the cache. </span>

`wincache.rerouteini` <span class="type">string</span>  
**Warning**
This option has been *REMOVED* as of 1.3.7. See
*wincache.reroute\_enabled* for similar functionality as of 1.3.7.

<span class="simpara"> Specifies an absolute or a relateve path to the
reroute.ini file that contains the list of PHP functions whose
implementation should be replaced with the WinCache function
equivalents. If a relative path is specified then it is assumed to be
relative to the location of php-cgi.exe file. </span>

`wincache.reroute_enabled` <span class="type">boolean</span>  
<span class="simpara"> Enables or disables the rerouting of certain file
I/O functions through the file cache. </span>

`wincache.srwlocks` <span class="type">boolean</span>  
**Warning**
This option has been *REMOVED* as of 2.0.0.0

<span class="simpara"> Enables or disables the use of shared
reader/writer locks. Disabling is useful when troubleshooting deadlock
conditions in WinCache. </span>

`wincache.filemapdir` <span class="type">string</span>  
<span class="simpara"> Specifies an absolute path to a directory where
WinCache will store the temporary files used for shared memory segments.
</span> <span class="simpara"> This directory must be on the local
machine and not on a networked file system. </span> <span
class="simpara"> If the directory is not specified, WinCache will use
the Windows System Page File for all shared memory segments. </span>

WinCache Statistics Script
--------------------------

The installation package for WinCache includes a PHP script,
`wincache.php`, that can be used to obtain cache information and
statistics.

If the WinCache extension was installed via the Microsoft Web Platform
Installer, then this script is located in
`%SystemDrive%\Program Files\IIS\Windows Cache for PHP\`. On a 64-bit
version of the Windows Server operating system, the script is located in
`%SystemDrive%\Program Files (x86)\IIS\Windows Cache for PHP`. If the
extension was installed manually, then the `wincache.php` will be
located in the same folder from which the content of the installation
package was extracted.

To use `wincache.php`, copy it into a root folder of a Web site or into
any subfolder. To protect the script, open it in any text editor and
replace the values for *USERNAME* and *PASSWORD* constants. If any other
IIS authentication is enabled on the server, then follow the
instructions in the comments:

**示例 \#1 Authentication configuration for `wincache.php`**

``` php
<?php
/**
 * ======================== CONFIGURATION SETTINGS ==============================
 * If you do not want to use authentication for this page, set USE_AUTHENTICATION to 0.
 * If you use authentication then replace the default password.
 */
define('USE_AUTHENTICATION', 1);
define('USERNAME', 'wincache');
define('PASSWORD', 'wincache');

/**
 * The Basic PHP authentication will work only when IIS is configured to support 
 * Anonymous Authentication' and nothing else. If IIS is configured to support/use
 * any other kind of authentication like Basic/Negotiate/Digest etc, this will not work.
 * In that case use the array below to define the names of users in your 
 * domain/network/workgroup which you want to grant access to.
 */
$user_allowed = array('DOMAIN\user1', 'DOMAIN\user2', 'DOMAIN\user3');

/**
 * If the array contains string 'all', then all the users authenticated by IIS
 * will have access to the page. Uncomment the below line and comment above line
 * to grant access to all users who gets authenticated by IIS.
 */
/* $user_allowed = array('all'); */

/** ===================== END OF CONFIGURATION SETTINGS ========================== */
?>
```

> **Note**: <span class="simpara"> Always protect the `wincache.php`
> script by using either the built-in authentication or the server's
> authentication mechanism. Leaving this script unprotected may
> compromise the security of your web application and web server.
> </span>

WinCache Session Handler
------------------------

The WinCache session handler (available since WinCache 1.1.0) can be
used to configure PHP to store the session data in shared memory session
cache. Using shared memory instead of the default file session storage
helps improve performance of PHP applications that store large amount of
data in session objects. Wincache session cache uses file-backed shared
memory, which ensures that the session data is not lost during recycling
of IIS application pools.

To configure PHP to use WinCache session handler set the `php.ini`
setting
<a href="/session/setup.html#" class="link">session.save_handler</a> to
*wincache*. By default the Windows temporary file location is used for
storing the session data. To change the location of the session file use
<a href="/session/setup.html#" class="link">session.save_path</a>
directive.

**示例 \#1 Enabling WinCache session handler**

``` php.ini
session.save_handler = wincache
session.save_path = C:\inetpub\temp\session\
```

WinCache Functions Reroutes
---------------------------

*NOTE:*
<a href="/wincache/setup.html#" class="link">wincache.rerouteini</a> was
removed as of WinCache 1.3.7.0. It has been replaced with automatic
function reroutes. See:
<a href="/wincache/setup.html#" class="link">wincache.reroute_enabled</a>.

The WinCache functions reroutes (available since WinCache 1.2.0, removed
since WinCache 1.3.7.0) can be used to replace built-in PHP functions
with their equivalents that are optimized for a particular purpose.
WinCache extension includes Windows-optimized implementation of PHP file
functions that may improve performance of PHP applications in cases when
PHP has to access files on network shares. The optimized implementation
is provided for the following functions:

-   <span class="simpara">
    <a href="/ref/filesystem.html#file_exists" class="link">file_exists</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#file_get_contents" class="link">file_get_contents</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#readfile" class="link">readfile</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#is_readable" class="link">is_readable</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#is_writable" class="link">is_writable</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#is_dir" class="link">is_dir</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#realpath" class="link">realpath</a>
    </span>
-   <span class="simpara">
    <a href="/ref/filesystem.html#filesize" class="link">filesize</a>
    </span>

To configure WinCache to use the functions reroutes use the file
`reroute.ini` that is included in WinCache installation package. Copy
this file into the same directory where `php.ini` file is located. After
that add the wincache.rerouteini setting in `php.ini` and specify an
absolute or relative path to the `reroute.ini` file.

**示例 \#1 Enabling WinCache functions reroutes**

``` php.ini
wincache.rerouteini = C:\PHP\reroute.ini
```

> **Note**: <span class="simpara"> If WinCache functions reroutes are
> enabled it is recommended to increase the WinCache file cache size.
> This can be done by using
> <a href="/wincache/setup.html#" class="link">wincache.fcachesize</a>
> setting. </span>

The `reroute.ini` file contains the mappings between the native PHP
functions and their equivalents in WinCache. Each line in the file
defines a mapping by using the following syntax:

*\<PHP function name\>:\[\<number of function parameters\>\]=\<wincache
function name\>*

The example of the file is shown below. In this example the calls to PHP
function <span class="function">file\_get\_contents</span> will be
replaced with calls to <span
class="function">wincache\_file\_get\_contents</span> only if the number
of parameters passed to the function is less than or equals to 2.
Specifying the number of parameters is useful when replacement function
does not handle all the function's parameters.

**示例 \#2 Reroute.ini file content**

``` php.ini
[FunctionRerouteList]
file_exists=wincache_file_exists
file_get_contents:2=wincache_file_get_contents
readfile:2=wincache_readfile
is_readable=wincache_is_readable
is_writable=wincache_is_writable
is_writeable=wincache_is_writable
is_file=wincache_is_file
is_dir=wincache_is_dir
realpath=wincache_realpath
filesize=wincache_filesize
```

资源类型
--------

此扩展没有定义资源类型。
