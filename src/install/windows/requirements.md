环境要求
--------

PHP 5.5+ 至少需要 Windows 2008/Vista，或 2008r2、2012、2012r2、2016 或
7、8、8.1、10。32 位或 64 位（也就是 X86 或 X64。PHP 不能在 Windows
RT/WOA/ARM上运行）。

PHP 需要 Visual C
运行时（CRT）。许多应用程序需要它，所以它可能已经被安装。

PHP 5.5 和 5.6 需要 VC CRT 11（Visual Studio 2012）。请参阅
<a href="https://www.microsoft.com/en-us/download/details.aspx?id=30679" class="link external">» https://www.microsoft.com/en-us/download/details.aspx?id=30679</a>

PHP 7.0 和 7.1 需要 VC CRT 14（Visual Studio 2015）。 PHP 7.2, 7.3 and
7.4 需要 VC CRT 15 (Visual Studio 2017)。 微软的开发环境 Visual Studio
2019 包含了编译 PHP 的全部环境要求，请参阅
<a href="https://visualstudio.microsoft.com/downloads/" class="link external">» https://visualstudio.microsoft.com/downloads/</a>。

你需要下载 x86 版本的 CRT 来编译 x86 版本的 PHP。同理，编译 x64 版本的
PHP 需要 x64 版本的 CRT。

如果系统已经安装了 CRT，安装程序会提示你，而不会改变任何东西。

CRT 安装程序支持 /quiet 和 /norestart
命令行开关，所以你可以用脚本运行它。

VC11 CRT DLLs 可以从您的本地机器复制到远程机器（"复制部署"
安装），而不是在远程机器上运行安装程序（例如您有限制访问的 Web
服务器）。参见：http://www.sitepoint.com/install-php53-windows/

VC14 CRT 不支持 "复制部署" 安装。VC14 CRT 有更多的 DLL (大部分以 api-\*
开头的文件中)。如果你能找到它们并复制它们，它也会工作（尝试使用
"Resource Hacker" 这样的工具来获得所有要复制的 DLL 的列表）。
