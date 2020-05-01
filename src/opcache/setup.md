安装／配置
==========

**目录**

-   [需求](/opcache/setup.html#需求)
-   [安装](/opcache/setup.html#安装)
-   [运行时配置](/opcache/setup.html#运行时配置)
-   [资源类型](/opcache/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

安装 OPcache 的过程根据所用的 PHP 版本有所不同。
请参考以下小节中适用的内容。

> **Note**:
>
> 如果需要将
> <a href="http://xdebug.org/" class="link external">» Xdebug</a> 扩展和
> OPcache 一起使用，必须在 Xdebug 扩展之前加载 OPcache 扩展。

### PHP 5.5.0 及后续版本

OPcache 只能编译为共享扩展。 如果你使用 **--disable-all** 参数
禁用了默认扩展的构建， 那么必须使用 **--enable-opcache** 选项来开启
OPcache。

编译之后，就可以使用
<a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>
指令来将 OPcache 扩展加载到 PHP 中。在非 Windows 平台使用
*zend\_extension=/full/path/to/opcache.so*， Windows 平台使用
*zend\_extension=C:\\path\\to\\php\_opcache.dll*。

### PHP 5.2, 5.3 和 5.4 版本

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/ZendOpcache" class="link external">» https://pecl.php.net/package/ZendOpcache</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

### 推荐的 php.ini 设置

使用下列推荐设置来获得较好的 性能：

    opcache.memory_consumption=128
    opcache.interned_strings_buffer=8
    opcache.max_accelerated_files=4000
    opcache.revalidate_freq=60
    opcache.fast_shutdown=1
    opcache.enable_cli=1

你也可以禁用
<a href="/opcache/setup.html#" class="link">opcache.save_comments</a>
并且启用
<a href="/opcache/setup.html#" class="link">opcache.enable_file_override</a>。
需要提醒的是，在生产环境中使用上述配置之前，必须经过严格测试。
因为上述配置存在一个已知问题，它会引发一些框架和应用的异常，
尤其是在存在文档使用了备注注解的时候。

<a href="/opcache/setup.html#运行时配置" class="link">这里</a>是 OPcache
可用的配置指令完整列表。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                                  | 默认         | 可修改范围       | 更新日志                                                  |
|---------------------------------------------------------------------------------------|--------------|------------------|-----------------------------------------------------------|
| <a href="/opcache/setup.html#" class="link">opcache.enable</a>                        | "1"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.enable_cli</a>                    | "0"          | PHP\_INI\_SYSTEM | 在 PHP 7.1.2 至 7.1.6 （含）的版本，默认值是"1"           |
| <a href="/opcache/setup.html#" class="link">opcache.memory_consumption</a>            | "128"        | PHP\_INI\_SYSTEM | 在 PHP 7.0.0 之前，默认值是 "64"                          |
| <a href="/opcache/setup.html#" class="link">opcache.interned_strings_buffer</a>       | "8"          | PHP\_INI\_SYSTEM | 在 PHP 7.0.0 之前，默认值是 "4"                           |
| <a href="/opcache/setup.html#" class="link">opcache.max_accelerated_files</a>         | "10000"      | PHP\_INI\_SYSTEM | 在 PHP 7.0.0 之前，默认值是 "2000"                        |
| <a href="/opcache/setup.html#" class="link">opcache.max_wasted_percentage</a>         | "5"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.use_cwd</a>                       | "1"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.validate_timestamps</a>           | "1"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.revalidate_freq</a>               | "2"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.revalidate_path</a>               | "0"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.save_comments</a>                 | "1"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.load_comments</a>                 | "1"          | PHP\_INI\_ALL    | 从 PHP 7.0.0 开始被移除                                   |
| <a href="/opcache/setup.html#" class="link">opcache.fast_shutdown</a>                 | "0"          | PHP\_INI\_SYSTEM | 从 PHP 7.2.0 开始被移除                                   |
| <a href="/opcache/setup.html#" class="link">opcache.enable_file_override</a>          | "0"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.optimization_level</a>            | "0x7FFFBFFF" | PHP\_INI\_SYSTEM | 从 PHP 5.6.18 开始，默认值从 0xFFFFFFFF 修改为 0x7FFFBFFF |
| <a href="/opcache/setup.html#" class="link">opcache.inherited_hack</a>                | "1"          | PHP\_INI\_SYSTEM | 自 PHP 7.3.0 被移除                                       |
| <a href="/opcache/setup.html#" class="link">opcache.dups_fix</a>                      | "0"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.blacklist_filename</a>            | ""           | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.max_file_size</a>                 | "0"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.consistency_checks</a>            | "0"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.force_restart_timeout</a>         | "180"        | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.error_log</a>                     | ""           | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.log_verbosity_level</a>           | "1"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.preferred_memory_model</a>        | ""           | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.protect_memory</a>                | "0"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.mmap_base</a>                     | **`NULL`**   | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.restrict_api</a>                  | ""           | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.file_update_protection</a>        | "2"          | PHP\_INI\_ALL    |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.huge_code_pages</a>               | "0"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.lockfile_path</a>                 | "/tmp"       | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.opt_debug_level</a>               | "0"          | PHP\_INI\_SYSTEM |                                                           |
| <a href="/opcache/setup.html#" class="link">opcache.file_cache</a>                    | NULL         | PHP\_INI\_SYSTEM | 从 PHP 7.0.0 开始支持                                     |
| <a href="/opcache/setup.html#" class="link">opcache.file_cache_only</a>               | "0"          | PHP\_INI\_SYSTEM | 从 PHP 7.0.0 开始支持                                     |
| <a href="/opcache/setup.html#" class="link">opcache.file_cache_consistency_checks</a> | "1"          | PHP\_INI\_SYSTEM | 从 PHP 7.0.0 开始支持                                     |
| <a href="/opcache/setup.html#" class="link">opcache.file_cache_fallback</a>           | "1"          | PHP\_INI\_SYSTEM | 从 PHP 7.0.0 开始支持，仅适用于 Windows 平台              |
| <a href="/opcache/setup.html#" class="link">opcache.validate_permission</a>           | "0"          | PHP\_INI\_SYSTEM | 从 PHP 7.0.14 开始支持                                    |
| <a href="/opcache/setup.html#" class="link">opcache.validate_root</a>                 | "0"          | PHP\_INI\_SYSTEM | 从 PHP 7.0.14 开始支持                                    |
| <a href="/opcache/setup.html#" class="link">opcache.preload</a>                       | ""           | PHP\_INI\_SYSTEM | 从 PHP 7.4.0 开始支持                                     |
| <a href="/opcache/setup.html#" class="link">opcache.preload_user</a>                  | ""           | PHP\_INI\_SYSTEM | 从 PHP 7.4.0 开始支持                                     |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`opcache.enable` <span class="type">boolean</span>  
启用操作码缓存。如果禁用此选项，则不会优化和缓存代码。 在运行期使用
<span class="function">ini\_set</span> 函数只能禁用 *opcache.enable*
设置，不可以启用此设置。 如果在脚本中尝试启用此设置项会产生警告。

`opcache.enable_cli` <span class="type">boolean</span>  
仅针对 CLI 版本的 PHP 启用操作码缓存。 通常被用来测试和调试。

`opcache.memory_consumption` <span class="type">integer</span>  
OPcache 的共享内存大小，以兆字节为单位。

`opcache.interned_strings_buffer` <span class="type">integer</span>  
用来存储预留字符串的内存大小，以兆字节为单位。 PHP 5.3.0
之前的版本会忽略此配置指令。

`opcache.max_accelerated_files` <span class="type">integer</span>  
OPcache 哈希表中可存储的脚本文件数量上限。 真实的取值是在质数集合 *{
223, 463, 983, 1979, 3907, 7963, 16229, 32531, 65407, 130987 }*
中找到的第一个大于等于设置值的质数。 设置值取值范围最小值是
200，最大值在 PHP 5.5.6 之前是 100000，PHP 5.5.6 及之后是 1000000。

`opcache.max_wasted_percentage` <span class="type">integer</span>  
浪费内存的上限，以百分比计。 如果达到此上限，那么 OPcache
将产生重新启动续发事件。

`opcache.use_cwd` <span class="type">boolean</span>  
如果启用，OPcache 将在哈希表的脚本键之后附加改脚本的工作目录，
以避免同名脚本冲突的问题。
禁用此选项可以提高性能，但是可能会导致应用崩溃。

`opcache.validate_timestamps` <span class="type">boolean</span>  
如果启用，那么 OPcache 会每隔
<a href="/opcache/setup.html#" class="link">opcache.revalidate_freq</a>
设定的秒数 检查脚本是否更新。 如果禁用此选项，你必须使用 <span
class="function">opcache\_reset</span> 或者 <span
class="function">opcache\_invalidate</span> 函数来手动重置
OPcache，也可以 通过重启 Web 服务器来使文件系统更改生效。

`opcache.revalidate_freq` <span class="type">integer</span>  
检查脚本时间戳是否有更新的周期，以秒为单位。 设置为 *0*
会导致针对每个请求， OPcache 都会检查脚本更新。

如果
<a href="/opcache/setup.html#" class="link">opcache.validate_timestamps</a>
配置指令设置为禁用，那么此设置项将会被忽略。

`opcache.revalidate_path` <span class="type">boolean</span>  
如果禁用此选项，在同一个
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
已存在的缓存文件会被重用。 因此，将无法找到不在包含路径下的同名文件。

`opcache.save_comments` <span class="type">boolean</span>  
如果禁用，脚本文件中的注释内容将不会被包含到操作码缓存文件，
这样可以有效减小优化后的文件体积。
禁用此配置指令可能会导致一些依赖注释或注解的 应用或框架无法正常工作，
比如： Doctrine， Zend Framework 2 以及 PHPUnit。

`opcache.load_comments` <span class="type">boolean</span>  
如果禁用，则即使文件中包含注释，也不会加载这些注释内容。 本选项可以和
<a href="/opcache/setup.html#" class="link">opcache.save_comments</a>
一起使用，以实现按需加载注释内容。

`opcache.fast_shutdown` <span class="type">boolean</span>  
如果启用，则会使用快速停止续发事件。 所谓快速停止续发事件是指依赖 Zend
引擎的内存管理模块
一次释放全部请求变量的内存，而不是依次释放每一个已分配的内存块。

从 PHP 7.2.0 开始，此配置指令被移除。 快速停止的续发事件的处理已经集成到
PHP 中， 只要有可能，PHP 会自动处理这些续发事件。

`opcache.enable_file_override` <span class="type">boolean</span>  
如果启用，则在调用函数 <span class="function">file\_exists</span>，
<span class="function">is\_file</span> 以及 <span
class="function">is\_readable</span> 的时候，
都会检查操作码缓存，无论文件是否已经被缓存。 如果应用中包含检查 PHP
脚本存在性和可读性的功能，这样可以提升性能。 但是如果禁用了
<a href="/opcache/setup.html#" class="link">opcache.validate_timestamps</a>
选项， 可能存在返回过时数据的风险。

`opcache.optimization_level` <span class="type">integer</span>  
控制优化级别的二进制位掩码。

`opcache.inherited_hack` <span class="type">boolean</span>  
在 PHP 5.3 之前的版本，OPcache 会存储代码中使用
<a href="/internals2/opcodes/declare-class.html" class="link">DECLARE_CLASS</a>
操作码 来实现继承的位置。当文件被加载之后，OPcache
会尝试使用当前环境来绑定被继承的类。 由于当前脚本中可能并不需要
DECLARE\_CLASS 操作码，如果这样的脚本需要对应的操作码被定义时，
可能无法运行。

在 PHP 5.3 及后续版本中，此配置指令会被忽略。

`opcache.dups_fix` <span class="type">boolean</span>  
仅作为针对 “不可重定义类”错误的一种解决方案。

`opcache.blacklist_filename` <span class="type">string</span>  
OPcache 黑名单文件位置。
黑名单文件为文本文件，包含了不进行预编译优化的文件名，每行一个文件名。
黑名单中的文件名可以使用通配符，也可以使用前缀。
此文件中以分号（;）开头的行将被视为注释。

简单的黑名单文件可能如下所示：

    ; 将特定文件加入到黑名单
    /var/www/broken.php
    ; 以字符 x 文件打头的文件
    /var/www/x
    ; 通配符匹配
    /var/www/*-broken.php

`opcache.max_file_size` <span class="type">integer</span>  
以字节为单位的缓存的文件大小上限。设置为 *0* 表示缓存全部文件。

`opcache.consistency_checks` <span class="type">integer</span>  
如果是非 0 值，OPcache 将会每隔 N 次请求检查缓存校验和。 N
即为此配置指令的设置值。
由于此选项对于性能有较大影响，请尽在调试环境使用。

`opcache.force_restart_timeout` <span class="type">integer</span>  
如果缓存处于非激活状态，等待多少秒之后计划重启。 如果超出了设定时间，则
OPcache 模块将杀除持有缓存锁的进程， 并进行重启。

如果选项
<a href="/opcache/setup.html#" class="link">opcache.log_verbosity_level</a>
设置为 2 或者 2 以上的数值，当发生重启时将在日志中记录一条警告信息。

`opcache.error_log` <span class="type">string</span>  
OPcache 模块的错误日志文件。 如果留空，则视为 *stderr*，
错误日志将被送往标准错误输出 （通常情况下是 Web 服务器的错误日志文件）。

`opcache.log_verbosity_level` <span class="type">integer</span>  
OPcache 模块的日志级别。
默认情况下，仅有致命级别（0）及错误级别（1）的日志会被记录。
其他可用的级别有：警告（2），信息（3）和调试（4）。

`opcache.preferred_memory_model` <span class="type">string</span>  
OPcache 首选的内存模块。 如果留空，OPcache 会选择适用的模块，
通常情况下，自动选择就可以满足需求。

可选值包括： *mmap*，*shm*, *posix* 以及 *win32*。

`opcache.protect_memory` <span class="type">boolean</span>  
保护共享内存，以避免执行脚本时发生非预期的写入。 仅用于内部调试。

`opcache.mmap_base` <span class="type">string</span>  
在 Windows 平台上共享内存段的基地址。 所有的 PHP
进程都将共享内存映射到同样的地址空间。
使用此配置指令避免“无法重新附加到基地址”的错误。

`opcache.restrict_api` <span class="type">string</span>  
仅允许路径是以指定字符串开始的 PHP 脚本调用 OPcache API 函数。
默认值为空字符串 ""，表示不做限制。

`opcache.file_update_protection` <span class="type">string</span>  
如果文件的最后修改时间距现在不足此项配置指令所设定的秒数，那么这个文件不会进入到缓存中。
这是为了防止尚未完全修改完毕的文件进入到缓存。
如果你的应用中不存在部分修改文件的情况，把此项设置为 0 可以提高性能。

`opcache.huge_code_pages` <span class="type">string</span>  
启用或者禁用将 PHP 代码（文本段）拷贝到 HUGE PAGES 中。
此项配置指令可以提高性能，但是需要在 OS 层面进行对应的配置。

`opcache.lockfile_path` <span class="type">string</span>  
用来存储共享锁文件的绝对路径（仅适用于 \*nix 操作系统）。

`opcache.opt_debug_level` <span class="type">string</span>  
出于对不同阶段的优化情况进行调试的目的，生成操作码转储。 设置为 0x10000
会在进行优化之前输出编译器编译后的操作码， 设置为 0x20000
会输出优化后的操作码。

`opcache.file_cache` <span class="type">string</span>  
配置二级缓存目录并启用二级缓存。 启用二级缓存可以在 SHM
内存满了、服务器重启或者重置 SHM 的时候提高性能。 默认值为空字符串
""，表示禁用基于文件的缓存。

`opcache.file_cache_only` <span class="type">boolean</span>  
启用或禁用在共享内存中的 opcode 缓存。

`opcache.file_cache_consistency_checks` <span class="type">boolean</span>  
当从文件缓存中加载脚本的时候，是否对文件的校验和进行验证。

`opcache.file_cache_fallback` <span class="type">boolean</span>  
在 Windows 平台上，当一个进程无法附加到共享内存的时候，
使用基于文件的缓存，也即：opcache.file\_cache\_only=1。
需要显示的启用文件缓存。

**Caution**
不鼓励禁用此配置项， 禁用它可能会导致进程无法启动。

`opcache.validate_permission` <span class="type">boolean</span>  
针对当前用户，验证缓存文件的访问权限。

`opcache.validate_root` <span class="type">boolean</span>  
在 chroot 的环境中避免命名冲突。 为了防止进程访问到 chroot
环境之外的文件，应该在 chroot 的情况下启用这个选项。

`opcache.preload` <span class="type">string</span>  
指定要在服务器启动时期进行编译和缓存的 PHP 脚本文件， 这些文件也可能通过
<span class="function">include</span> 或者 <span
class="function">opcache\_compile\_file</span> 函数 来预加载其他文件。
所有这些文件中包含的实体，包括函数、类等，在服务器启动的时候就被加载和缓存，
对于用户代码来讲是“开箱可用”的。

`opcache.preload_user` <span class="type">string</span>  
考虑到安全因素，禁止以 root 用户预加载代码。该指令方便以其他用户预加载。

资源类型
--------

此扩展没有定义资源类型。
