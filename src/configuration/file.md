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
    指定不同的 *php.ini* 文件位置。注册表目录所在的位置取决于你的系统是
    32 位还是 64 位。32-bit 的 PHP 运行在 32-bit 的系统或 64-bit 的 PHP
    运行在 64-bit 系统时使用 *\[(HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\]*
    32-bit 的 PHP 运行在 64-bit 的系统上时，则使用
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\WOW6432Node\\PHP\]*\] 替代。
    系统版本跟 PHP 版本架构一致时，会按以下顺序依次进行检查：
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\\x.y.z\]*，
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\\x.y\]* 和
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\PHP\\x\]*，其中的 x，y 和 z
    指的是 PHP 主版本号，次版本号和发行批次。 对于 32 bit 版本的 PHP
    运行在 64 bit 系统上的情况，则会按以下顺序依次进行检查：
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\WOW6421Node\\PHP\\x.y.z\]*，
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\WOW6421Node\\PHP\\x.y\]* 和
    *\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\WOW6421Node\\PHP\\x\]*，其中的
    x，y 和 z 指的是 PHP
    主版本号，次版本号和发行批次。如果在其中任何目录下的 *IniFilePath*
    有键值，则第一个值将被用作 *php.ini* 的位置（仅适用于 Windows）。
    </span>
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

在 `php.ini` 中可以使用环境变量，如下示例：

**示例 \#1 `php.ini` 中的环境变量**

``` ini
; PHP_MEMORY_LIMIT 来自于环境变量的值
memory_limit = ${PHP_MEMORY_LIMIT}
```

由扩展库处理的 `php.ini`
指令，其文档分别在各扩展库的页面。<a href="/ini.html" class="link">内核配置选项</a>见附录。不过也许不是所有的
PHP 指令都在手册中有文档说明。要得到自己的 PHP
版本中的配置指令完整列表，请阅读 `php.ini`
文件，其中都有注释。此外，也许从 Git
得到的<a href="https://git.php.net/?p=php-src.git;a=blob;f=php.ini-production;hb=HEAD" class="link external">» 最新版 <var class="filename">php.ini</var></a>
也有帮助。

**示例 \#2 `php.ini` 例子**

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

### 扫描路径配置

可以通过配置，让 PHP 在读完 `php.ini` 后，扫描指定路径中的附加 .ini
配置文件。编译时通过 **--with-config-file-scan-dir**
参数来指定要扫描的目录。自 PHP 5.2.0 起，扫描路径也可以通过环境变量
`PHP_INI_SCAN_DIR` 来设置。

通过在扫描路径配置中加入特定系统的目录分隔符（Windows、NetWare 和 RISC
OS 下是 *;*；其它操作系统下是 *:*；该值可以通过 PHP 常量
**`PATH_SEPARATOR`** 获取），还可以设置多个扫描路径。如果
`PHP_INI_SCAN_DIR` 为空，PHP 一样会扫描在编译时指定的
**--with-config-file-scan-dir** 此路径。

对于每个目录而言，PHP 会以首字符顺序为优先级，扫描该目录下所有的 *.ini*
结尾的配置文件。所有被截入的配置文件，可以通过 <span
class="function">php\_ini\_scanned\_files</span>
函数来获取列表，也可以通过 PHP 命令行加入 **--ini** 参数来查看。

    以下假设 PHP 配置为 --with-config-file-scan-dir=/etc/php.d
    并且目录分隔符为 :

    $ php
      PHP 会加载 /etc/php.d/*.ini 全部配置文件。

    $ PHP_INI_SCAN_DIR=/usr/local/etc/php.d php
      PHP 会加载 /usr/local/etc/php.d/*.ini 全部配置文件。

    $ PHP_INI_SCAN_DIR=:/usr/local/etc/php.d php
      PHP 会加载 /etc/php.d/*.ini 下的全部配置文件，然后加载
      /usr/local/etc/php.d/*.ini 下的全部配置文件。

    $ PHP_INI_SCAN_DIR=/usr/local/etc/php.d: php
      PHP 会加载 /usr/local/etc/php.d/*.ini 下的全部配置文件，然后加载
      /etc/php.d/*.ini 下的全部配置文件。

### 更新日志

| 版本  | 说明                                                                       |
|-------|----------------------------------------------------------------------------|
| 7.0.0 | Hash 符号 (*\#*) 不再被当做注释。                                          |
| 5.3.0 | Hash 符号 (*\#*) 不应该被用于注释用，如果使用的话会抛出一个 warning 提醒。 |
| 5.2.0 | 允许设置 `PHP_INI_SCAN_DIR` 系统变量，来覆盖编译时指定的 "扫描路径" 配置。 |
| 5.1.0 | 可以从 .ini 文件中引用现有的 .ini 变量。                                   |
