配置文件
--------

配置文件（`php.ini`）在 PHP 启动时被读取。对于服务器模块版本的 PHP，仅在
web 服务器启动时读取一次。对于 CGI 和 CLI 版本，每次调用都会读取。

`php.ini` 的搜索路径如下（按顺序）：

-   <span class="simpara"> SAPI 模块所指定的位置（Apache 2 中的
    *PHPIniDir* 指令，CGI 和 CLI 中的 *-c* 命令行选项，NSAPI 中的
    *php\_ini* 参数，THTTPD 中的 *PHP\_INI\_PATH* 环境变量）。 </span>
-   <span class="simpara"> `PHPRC` 环境变量。在 PHP 5.2.0
    之前，其顺序在以下提及的注册表键值之后。 </span>
-   <span class="simpara"> 自 PHP 5.2.0 起，可以为不同版本的 PHP
    指定不同的 *php.ini*
    文件位置。将以下面的顺序检查注册表目录：*\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\\x.y.z\]*，*\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\\x.y\]*
    和 *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\\x\]*，其中的 x，y 和 z
    指的是 PHP 主版本号，次版本号和发行批次。如果在其中任何目录下的
    *IniFilePath* 有键值，则第一个值将被用作 *php.ini* 的位置（仅适用于
    windows）。 </span>
-   <span class="simpara"> *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\]* 内
    *IniFilePath* 的值（Windows 注册表位置）。 </span>
-   <span class="simpara"> 当前工作目录（对于 CLI）。 </span>
-   <span class="simpara"> web 服务器目录（对于 SAPI 模块）或 PHP
    所在目录（Windows 下其它情况）。 </span>
-   <span class="simpara"> Windows 目录（`C:\windows` 或
    `C:\winnt`），或 *--with-config-file-path* 编译时选项指定的位置。
    </span>

如果存在 `php-SAPI.ini`（SAPI 是当前所用的 SAPI 名称，因此实际文件名为
`php-cli.ini` 或 `php-apache.ini` 等），则会用它替代 `php.ini`。SAPI
的名称可以用 <span class="function">php\_sapi\_name</span> 来测定。

> **Note**:
>
> Apache web 服务器在启动时会把目录转到根目录，这将导致 PHP
> 尝试在根目录下读取 `php.ini`，如果存在的话。

> **Note**:
>
> 在 `php.ini` 中可以使用环境变量。

由扩展库处理的 `php.ini`
指令，其文档分别在各扩展库的页面。<a href="/ini.html" class="link">内核配置选项</a>见附录。不过也许不是所有的
PHP 指令都在手册中有文档说明。要得到自己的 PHP
版本中的配置指令完整列表，请阅读 `php.ini`
文件，其中都有注释。此外，也许从 Git
得到的<a href="https://git.php.net/?p=php-src.git;a=blob;f=php.ini-production;hb=HEAD" class="link external">» 最新版 <var class="filename">php.ini</var></a>
也有帮助。

**示例 \#1 `php.ini` 例子**

``` ini
; any text on a line after an unquoted semicolon (;) is ignored
[php] ; section markers (text within square brackets) are also ignored
; Boolean values can be set to either:
;    true, on, yes
; or false, off, no, none
register_globals = off
track_errors = yes

; you can enclose strings in double-quotes
include_path = ".:/usr/local/lib/php"

; backslashes are treated the same as any other character
include_path = ".;c:\php\lib"
```

自 PHP 5.1.0 起，有可能在 .ini 文件内引用已存在的 .ini
变量。例如：*open\_basedir = ${open\_basedir} ":/new/dir"*。
