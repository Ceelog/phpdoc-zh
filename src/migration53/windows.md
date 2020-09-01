Windows 支持改变
----------------

Windows 发行版的改变：

-   <span class="simpara"> 最小的 Windows 支持版本是 Windows XP
    SP3；Windows 98，ME，2000 和 NT4 将不再被支持。 </span>
-   <span class="simpara"> Windows 二进制版支持 i586 以上版本。i386 和
    i486 不再被支持。 </span>
-   <span class="simpara"> Windows 上的 PHP x64 版本的支持是实验性的。
    </span>
-   <span class="simpara"> 通过使用 Visual Studio 2008，编译器现在支持
    Visual C++ 9 (VC9)。基于 VC9 的快照和发行版均可用。旧的使用 VC6
    的二进制版本仍然会与 VC9 版本同时被支持和发行. </span>
-   <span class="simpara">
    <a href="/book/pdo.html#Oracle%20(PDO)" class="link">PDO_OCI</a>
    *php\_pdo\_oci8.dll* 库 (配合 Oracle version 8 客户端库使用)
    已经不会被内建。作为替代，使用 *php\_pdo\_oci.dll* (注意没有 '8')
    配合 Oracle 10 或 11 客户端库。仍然支持其他数据库版本的连接. </span>
-   <span class="simpara"> 对于
    <a href="/book/oci8.html" class="link">OCI8</a> 扩展而言，除了
    *php\_oci8.dll* 之外，一个新的库 *php\_oci8\_11g.dll*
    可用。但仅仅只能同时打开一个库。配合 Oracle 10.2 客户端库使用
    *php\_oci8.dll*。配合 Oracle 11 客户端库使用
    *php\_oci8\_11g.dll*。仍然支持其他数据库版本的连接. </span>

新增了如下这些 Windows 支持函数：

-   <span class="simpara"> <span class="function">checkdnsrr</span>
    </span>
-   <span class="simpara"> <span
    class="function">dns\_get\_record</span> </span>
-   <span class="simpara"> <span class="function">fnmatch</span> </span>
-   <span class="simpara"> <span class="function">getmxrr</span> </span>
-   <span class="simpara"> <span class="function">getopt</span> </span>
-   <span class="simpara"> <span
    class="function">imagecolorclosesthwb</span> </span>
-   <span class="simpara"> <span class="function">inet\_ntop</span>
    </span>
-   <span class="simpara"> <span class="function">inet\_pton</span>
    </span>
-   <span class="simpara"> <span class="function">link</span> </span>
-   <span class="simpara"> <span class="function">linkinfo</span>
    </span>
-   <span class="simpara"> <span
    class="function">mcrypt\_create\_iv</span> </span>
-   <span class="simpara"> <span class="function">readlink</span>
    </span>
-   <span class="simpara"> <span
    class="function">socket\_create\_pair</span> - 该函数之前就可以在
    Windows 平台使用，但是自 PHP 4.3.0 起就因为一个 Bug 的原因而关闭了.
    </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_pair</span> </span>
-   <span class="simpara"> <span class="function">symlink</span> </span>
-   <span class="simpara"> <span class="function">time\_nanosleep</span>
    </span>
-   <span class="simpara"> <span
    class="function">time\_sleep\_until</span> </span>

其它改变:

-   <span class="simpara"> 改进了 <span
    class="function">stat</span>，<span
    class="function">touch</span>，<span
    class="function">filemtime</span>，<span
    class="function">filesize</span> 等相关函数的移植性
    (对于可用数据100%可移植)。 </span>
-   <span class="simpara"> 现在可以使用 <span
    class="function">link</span> 函数来在 Windows
    平台上创建硬链接，创建符号链接则使用 <span
    class="function">symlink</span> 函数。硬链接自 Windows 2000
    起可用，符号链接则自 Windows Vista 起可用。 </span>
-   <span class="simpara"> Windows 版本的 PHP 包含一组以
    *PHP\_WINDOWS\_\** 为前缀的常量。这些常量的列表可以在
    <a href="/info/constants.html" class="xref">预定义常量</a>找到。
    </span>

**Warning**

丢弃 ISAPI 模块支持。使用改进的 FastCGI SAPI 模块替代。

> **Note**: <span class="simpara"> 一个新的专注于 PHP on Windows
> 的站点可用，包括下载，发布候选版本，和各种快照
> (thread-safe/not-thread-safe，VC6/VC9，x86/x64)。网站的地址是
> <a href="https://windows.php.net/" class="link external">» https://windows.php.net/</a>。
> </span>
