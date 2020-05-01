安装／配置
==========

**目录**

-   [需求](/apc/setup.html#需求)
-   [安装](/apc/setup.html#安装)
-   [运行时配置](/apc/setup.html#运行时配置)
-   [资源类型](/apc/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/apc" class="link external">» https://pecl.php.net/package/apc</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

> **Note**: <span class="simpara">
> 在Windows上，APC需要一个临时目录，并且Web服务器对这个目录可写，APC会检测TMP,TEMP,USERPROFILE这些Windows的环境变量，如果这些都没有，会检查系统文件夹下的WINDOWS目录。
> </span>

> **Note**: <span class="simpara">
> 更深层次，更高级别的技术实现细节,请参阅
> <a href="https://git.php.net/?p=pecl/caching/apc.git;a=blob;f=TECHNOTES.txt" class="link external">»  开发人员提供的 TECHNOTES 文件</a>
> . </span>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

尽管默认的 APC
设定对于大多数安装已经没问题，但专业人员应考虑调整以下参数。

APC有两个主要的配置选项。第一，多少内存将被分配给APC;第二，每次请求APC是否检查文件修改。两个ini选项分别控制这些设置
*apc.shm\_size* 和*apc.stat*.就这两项配置仔细阅读下面的章节。

一旦服务器运行起来了, *apc.php*
脚本可以拷贝到一个可以通过浏览器访问到的Web目录中，通过浏览器访问这个脚本会得到APC工作状态的详细分析，如果在PHP中启用了GD扩展，它甚至会显示一些有趣的图表。当然，首要的事情是要确保真的缓存了文件。
如果APC运行了， *缓存完全统计* 数目
(在左上角)将显示缓存的命中率并且清除在最后 *apc.ttl*
秒内没有被访问的缓存。
这个数字使缓存的最小化的很好配置。如果缓存不断的被填充和清除，这将影响缓存的效果和脚本的性能。减少这个数字的最好方式就是给APC分配足够多的内存。除此之外,
可以通过 *apc.filters* 缓存更少的脚本。

| 名字                                                                   | 默认                    | 可修改范围       | 更新日志                                                       |
|------------------------------------------------------------------------|-------------------------|------------------|----------------------------------------------------------------|
| <a href="/apc/setup.html#" class="link">apc.enabled</a>                | "1"                     | PHP\_INI\_SYSTEM | PHP\_INI\_SYSTEM in APC 2. PHP\_INI\_ALL in APC \<= 3.0.12.    |
| <a href="/apc/setup.html#" class="link">apc.shm_segments</a>           | "1"                     | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.shm_size</a>               | "30"                    | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.optimization</a>           | "0"                     | PHP\_INI\_ALL    | PHP\_INI\_SYSTEM in APC 2. Removed in APC 3.0.13.              |
| <a href="/apc/setup.html#" class="link">apc.num_files_hint</a>         | "1000"                  | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.user_entries_hint</a>      | "4096"                  | PHP\_INI\_SYSTEM | Available since APC 3.0.0.                                     |
| <a href="/apc/setup.html#" class="link">apc.ttl</a>                    | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.0.                                     |
| <a href="/apc/setup.html#" class="link">apc.user_ttl</a>               | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.0.                                     |
| <a href="/apc/setup.html#" class="link">apc.gc_ttl</a>                 | "3600"                  | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.cache_by_default</a>       | "1"                     | PHP\_INI\_ALL    | PHP\_INI\_SYSTEM in APC \<= 3.0.12. Available since APC 3.0.0. |
| <a href="/apc/setup.html#" class="link">apc.filters</a>                | NULL                    | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.mmap_file_mask</a>         | NULL                    | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.slam_defense</a>           | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.0.                                     |
| <a href="/apc/setup.html#" class="link">apc.file_update_protection</a> | "2"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.6.                                     |
| <a href="/apc/setup.html#" class="link">apc.enable_cli</a>             | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.7.                                     |
| <a href="/apc/setup.html#" class="link">apc.max_file_size</a>          | "1M"                    | PHP\_INI\_SYSTEM | Available since APC 3.0.7.                                     |
| <a href="/apc/setup.html#" class="link">apc.use_request_time</a>       | "1"                     | PHP\_INI\_ALL    | Available since APC 3.1.3.                                     |
| <a href="/apc/setup.html#" class="link">apc.stat</a>                   | "1"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.10.                                    |
| <a href="/apc/setup.html#" class="link">apc.write_lock</a>             | "1"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.11.                                    |
| <a href="/apc/setup.html#" class="link">apc.report_autofilter</a>      | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.11.                                    |
| <a href="/apc/setup.html#" class="link">apc.include_once_override</a>  | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.12.                                    |
| <a href="/apc/setup.html#" class="link">apc.rfc1867</a>                | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.13.                                    |
| <a href="/apc/setup.html#" class="link">apc.rfc1867_prefix</a>         | "upload\_"              | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.rfc1867_name</a>           | "APC\_UPLOAD\_PROGRESS" | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.rfc1867_freq</a>           | "0"                     | PHP\_INI\_SYSTEM |                                                                |
| <a href="/apc/setup.html#" class="link">apc.rfc1867_ttl</a>            | "3600"                  | PHP\_INI\_SYSTEM | Available since APC 3.1.1.                                     |
| <a href="/apc/setup.html#" class="link">apc.localcache</a>             | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.14.                                    |
| <a href="/apc/setup.html#" class="link">apc.localcache.size</a>        | "512"                   | PHP\_INI\_SYSTEM | Available since APC 3.0.14.                                    |
| <a href="/apc/setup.html#" class="link">apc.coredump_unmap</a>         | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.16.                                    |
| <a href="/apc/setup.html#" class="link">apc.stat_ctime</a>             | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.0.13.                                    |
| <a href="/apc/setup.html#" class="link">apc.preload_path</a>           | NULL                    | PHP\_INI\_SYSTEM | Available since APC 3.1.1.                                     |
| <a href="/apc/setup.html#" class="link">apc.file_md5</a>               | "0"                     | PHP\_INI\_SYSTEM | Available since APC 3.1.1.                                     |
| <a href="/apc/setup.html#" class="link">apc.canonicalize</a>           | "1"                     | PHP\_INI\_SYSTEM | Available since APC 3.1.1.                                     |
| apc.lazy\_functions                                                    | 0                       | PHP\_INI\_SYSTEM | Available since APC 3.1.3.                                     |
| apc.lazy\_classes                                                      | 0                       | PHP\_INI\_SYSTEM | Available since APC 3.1.3.                                     |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`apc.enabled` <span class="type">boolean</span>  
*apc.enabled* 可以设成 0 来禁用 APC.主要是用在当 APC 被静态编译入 PHP
时，因为没有其它方法来禁用了(编译为 DSO ,
的时候，可以将*php.ini*中的*extension* 行注释掉)。

`apc.shm_segments` <span class="type">integer</span>  
编译器缓存要分配的共享内存块的数目。如果 APC 用光了共享内存但是已经将
*apc.shm\_size* 设为了系统所能允许的最大值，可以尝试增大此值。

`apc.shm_size` <span class="type">integer</span>  
以 MB 为单位的每个共享内存块的大小。默认时，有些系统（包括大多数 BSD
变种）的共享内存块大小非常低。

`apc.optimization` <span class="type">integer</span>  
优化级别。设为 0
则禁用优化器，更高的值则使用更主动的优化。期望非常有限的速度提升。尚在试验中。

`apc.num_files_hint` <span class="type">integer</span>  
Web
服务器上的被包含或被请求的不同源文件的数目的大概估计。如果不确定则设为 0
或去掉此项；此设定主要用在有数千个源文件的站点。

`apc.user_entries_hint` <span class="type">integer</span>  
与<a href="/apc/setup.html#" class="link">apc.num_files_hint</a>类似,
根据唯一用户数来存储缓存变量。 如果不能确定则设置为0或或去掉此项。

`apc.ttl` <span class="type">integer</span>  
缓存条目在缓冲区中允许逗留的秒数。0 表示永不超时。建议值为7200\~86400
设为 0 意味着缓冲区有可能被旧的缓存条目填满，从而导致无法缓存新条目。

`apc.user_ttl` <span class="type">integer</span>  
类似于apc.ttl，只是针对每个用户而言，建议值为7200\~86400。 设为 0
意味着缓冲区有可能被旧的缓存条目填满，从而导致无法缓存新条目。
如果大于0，APC将尝试删除过期条目。

`apc.gc_ttl` <span class="type">integer</span>  
缓存条目在垃圾回收表中能够存在的秒数。此值提供了一个安全措施，即在服务器进程在执行缓存的源文件时，如果该文件被修改则旧版本将不会被回收，直到达到此
TTL 为止。设为零将禁用此特性。

`apc.cache_by_default` <span class="type">boolean</span>  
默认为 on，但可以设为 off 并和加号开头的 *apc.filters*
一起用，则文件仅在匹配过滤器时被缓存。

`apc.filters` <span class="type">string</span>  
一个以逗号分隔的 POSIX
扩展正则表达式的列表。如果任一个模式匹配源文件名，则该文件不被缓存。注意用来匹配的文件名是传递给
include/require
的文件名，而不是绝对路径。如果正则表达式的第一个字符是*+*
t则意味着任何匹配表达式的文件会被缓存，如果第一个字符是 *-*
则任何匹配项都不会被缓存。 *-*是默认值，可以省略掉。

`apc.mmap_file_mask` <span class="type">string</span>  
如果使用 *--enable-mmap*(默认启用)为APC编译了MMAP支持，
这里的值就是传递给mmap模块的mktemp风格的文件掩码(建议值为"
*/tmp/apc.XXXXXX*")。
该掩码用于决定内存映射区域是否要被file-backed或者shared memory backed。
对于直接的file-backed内存映射，要设置成"/tmp/apc.XXXXXX"的样子(恰好6个X)。
要使用POSIX风格的shm\_open/mmap就需要设置成"/apc.shm.XXXXXX"的样子。
你还可以设为"/dev/zero"来为匿名映射的内存使用内核的"/dev/zero"接口。
不定义此指令则表示强制使用匿名映射。

`apc.slam_defense` <span class="type">integer</span>  
在非常繁忙的服务器上，无论是启动服务还是修改文件，
都可能由于多个进程企图同时缓存一个文件而导致竞争条件。
这个选项用于设置进程在处理未被缓存的文件时跳过缓存步骤的百分率。
比如设为*75*表示在遇到未被缓存的文件时有*75*%的概率不进行缓存，从而减少碰撞几率。
反对使用该指令，鼓励设为
*0*来禁用这个特性。建议该用apc.write\_lock指令。

Deprecated by
<a href="/apc/setup.html#" class="link">apc.write_lock</a>.

`apc.file_update_protection` <span class="type">integer</span>  
当你在一个运行中的服务器上修改文件时，你应当执行原子操作。
也就是先写进一个临时文件，然后将该文件重命名(*mv*)到最终的名字。
文本编辑器以及 **cp**, **tar**
等程序却并不是这样操作的，从而导致有可能缓冲了残缺的文件。 默认值 2
表示在访问文件时如果发现修改时间距离访问时间小于 2 秒则不做缓冲。
那个不幸的访问者可能得到残缺的内容，但是这种坏影响却不会通过缓存扩大化。
如果你能确保所有的更新操作都是原子操作，那么可以用 0 关闭此特性。
如果你的系统由于大量的IO操作导致更新缓慢，你就需要增大此值。

`apc.enable_cli` <span class="type">integer</span>  
是否为CLI版本启用APC功能，仅用于测试和调试目的才打开此选项。
在正常情况下不是理想的创建、 填充和销毁 CLI 的每个请求上的 APC
缓存，但各种测试方案很有用，能够轻松地使 CLI 版本的 PHP APC

`apc.max_file_size` <span class="type">integer</span>  
Prevent files larger than this value from getting cached. Defaults to
1M.

`apc.stat` <span class="type">integer</span>  
是否启用脚本更新检查。 改变这个指令值要非常小心。 默认值 On
表示APC在每次请求脚本时都检查脚本是否被更新，
如果被更新则自动重新编译和缓存编译后的内容。但这样做对性能有不利影响。
如果设为 Off 则表示不进行检查，从而使性能得到大幅提高。
但是为了使更新的内容生效，你必须重启Web服务器(译者注：如果采用cgi/fcgi类似的，需重启cgi/fcgi进程)。
生产服务器上脚本文件很少更改, 可以通过禁用本选项获得显著的性能提升。

这个指令对于include/require的文件同样有效。但是需要注意的是，
如果你使用的是相对路径，APC就必须在每一次include/require时都进行检查以定位文件。
而使用绝对路径则可以跳过检查，所以鼓励你使用绝对路径进行include/require操作。

`apc.write_lock` <span class="type">boolean</span>  
在繁忙的服务器上，Web服务器第一次被启动，或者很多文件在同一时间被修改，APC可能会多次编译同一个文件，写锁保证只有一个进程将尝试编译并缓存未缓存的脚本。其他进程试图使用该脚本将不使用opcode缓存，而不是锁定和等待缓存生成。

`apc.report_autofilter` <span class="type">boolean</span>  
是否记录所有由于early/late binding原因而自动未被缓存的脚本。

`apc.include_once_override` <span class="type">boolean</span>  
优化<span class="function">include\_once</span>和<span
class="function">require\_once</span>函数以避免执行额外的系统调用。

`apc.rfc1867` <span class="type">boolean</span>  
RFC1867 File Upload Progress hook handler is only available if APC was
compiled against PHP 5.2.0 or later. When enabled, any file uploads
which includes a field called *APC\_UPLOAD\_PROGRESS* before the file
field in an upload form will cause APC to automatically create an
upload\_*key* user cache entry where *key* is the value of the
*APC\_UPLOAD\_PROGRESS* form entry.

Note that the hidden field specified by *APC\_UPLOAD\_PROGRESS* must
come before the file field, otherwise the upload progress will not work
correctly.

Note that the file upload tracking is not threadsafe at this point, so
new uploads that happen while a previous one is still going will disable
the tracking for the previous.

**示例 \#1 An apc.rfc1867 example**

``` php
<?php
print_r(apc_fetch("upload_$_POST[APC_UPLOAD_PROGRESS]"));
?>
```

以上例程的输出类似于：

    Array
    (
        [total] => 1142543
        [current] => 1142543
        [rate] => 1828068.8
        [filename] => test
        [name] => file
        [temp_filename] => /tmp/php8F
        [cancel_upload] => 0
        [done] => 1
    )

`apc.rfc1867_prefix` <span class="type">string</span>  
用于上传文件的缓冲项条目名称前缀

`apc.rfc1867_name` <span class="type">string</span>  
需要由APC处理的上传文件的隐藏表单项名称

`apc.rfc1867_freq` <span class="type">string</span>  
用户上传文件缓存项的更新频率。 取值可以是总文件大小的百分比，或者以
*"k"*, *"m"*, or *"g"* kilobytes, megabytes, or gigabytes 结尾的绝对尺寸
(大小写不敏感). 0 表示尽可能快的更新，不过这样可能会导致上传速度下降。

`apc.rfc1867_ttl` <span class="type">bool</span>  
TTL for rfc1867 entries.

`apc.localcache` <span class="type">boolean</span>  
使用非锁定本地进程shadow-cache
，它可以减少了向缓冲区写入时锁之间的竞争。

`apc.localcache.size` <span class="type">integer</span>  
The size of the local process shadow-cache, should be set to a
sufficiently large value, approximately half of
<a href="/apc/setup.html#" class="link">apc.num_files_hint</a>.

`apc.coredump_unmap` <span class="type">boolean</span>  
启用APC的信号句柄，例如SIGSEGV信号，当信号写入核心文件。当这些信号被接收，APC将试图取消映射的共享内存段，从核心文件中排除它。此设置可以提高系统的稳定性,当接受到致命的信号或者采用APC的大型共享内存段配置方式。

**Warning**
此功能是潜在的危险。如果发生致命错误取消映射一个共享内存段致命的信号句柄，
可能会导致不可预知的结果。

> **Note**:
>
> 虽然有些内核可能会提供了便利，忽略各类共享内存时生成核心转储文件，这些实现可能也忽略了重要的共享内存段，比如
> Apache scoreboard。

`apc.stat_ctime` <span class="type">integer</span>  
验证ctime(创建时间)可以避免SVN或者rsync带来的问题，确保自上次统计inode没有改变。APC通常只检查mtime(修改时间)。

`apc.canonicalize` <span class="type">bool</span>  
如果设置为on，则在no-state
模式（不检查文件更新）时会将相对路径改为绝对路径。

`apc.preload_path` <span class="type">string</span>  

`apc.use_request_time` <span class="type">bool</span>  
Use the SAPI request start time for TTL.

`apc.file_md5` <span class="type">bool</span>  
记录文件的md5值

`apc.lazy_functions` <span class="type">integer</span>  
启用函数延迟加载

`apc.lazy_classes` <span class="type">integer</span>  
启用类延迟加载

资源类型
--------

此扩展没有定义资源类型。
