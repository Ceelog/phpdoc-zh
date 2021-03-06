安装前需要考虑的事项
====================

安装前，首先需要知道想用 PHP 来做什么。PHP 主要用在三个领域，分别在
<a href="/intro-whatcando.html" class="link">PHP 能做什么</a>
一节中进行了描述：

-   <span class="simpara">网站和 web 应用程序（服务器端脚本）</span>
-   <span class="simpara">命令行脚本</span>
-   <span class="simpara">桌面（GUI）应用程序</span>

在通常情况下，需要三样东西：PHP 自身、一个 web 服务器和一个 web
浏览器。通常你已经拥有了一个 web
浏览器，并且在你使用的操作系统中，也可能已经内置了 web 服务器（例如
Linux 和 macOS 下的 Apache；Windows 下的 IIS）。也许在某个公司租用了 web
空间（虚拟主机、VPS 等），这样，自己无需设置任何东西，仅需要编写 PHP
脚本，并上传到租用的空间中，然后在浏览器中查看结果。

如果需要自己配置服务器和 PHP，有两个方法将 PHP
连接到服务器上。对于很多服务器，PHP 均有一个直接的模块接口（也叫做
SAPI）。这些服务器包括 Apache、Microsoft Internet Information
Server、Netscape 和 iPlanet 等服务器。如果你使用的 web 服务器不支持 PHP
模块接口，还可以将其作为 CGI 或 FastCGI 处理器来使用。这意味着可以使用
PHP 的 CGI 可执行程序来处理所有服务器上的 PHP 文件请求。

如果你对 PHP
命令行脚本感兴趣（例如在离线状态下，根据传递给脚本的参数，自动生成一些图片，或处理一些文本文件），可以参考
<a href="/features/commandline.html" class="link">PHP 在命令行模式下的使用</a>
章节。在这种情况下，不再需要 web 服务器和 web 浏览器支持。

还可以用 PHP 的 PHP-GTK 扩展来编写桌面图形界面应用程序。这与编写 web
页面完全不同，因为无需输出任何 HTML，而要管理窗口和窗口中的对象。关于
PHP-GTK 的更多信息，请访问
<a href="http://gtk.php.net/" class="link external">» PHP-GTK 扩展官网</a>。PHP-GTK
没有包含在官方发布的 PHP 中。

本节开始介绍如何在 Unix 和 Windows 的 web 服务器中配置服务器模块接口和
CGI 可执行程序。也将在下面几节中了解到有关命令行可执行程序安装的信息。

PHP 源代码包和二进制包可以在以下链接获取
<a href="https://www.php.net/downloads.php" class="link external">» https://www.php.net/downloads.php</a>。
