在本教程中，假设用户的服务器已经安装并运行了 PHP，所有以 `.php`
结尾的文件都将由 PHP 来处理。在大部分的服务器上， 这是 PHP
的默认扩展名，不过，也请询问服务器管理员以确认。如果服务器支持 PHP
，则不需要做任何事情。只用建立 `.php` 文件，并把它们放置 到 web
目录中，服务器将神奇地自动解析这些文件。不用编译任何东西，也不用安装
任何其它的工具，仅仅只需把这些使用了 PHP 的文件想象成简单的 HTML
文件，其中 只不过多了一种新的标识符，在这里可以做各种各样的事情。

假设用户希望在本地机器开发以节约宝贵的带宽。在这种情况下，需要安装一个诸如
<a href="http://httpd.apache.org/" class="link external">» Apache</a> 的
web 服务器，当然还有
<a href="https://www.php.net/downloads.php" class="link external">» PHP</a>。可能还希望安装一个数据库，例如
<a href="http://dev.mysql.com/doc/" class="link external">» MySQL</a>。

可以一个个的安装它们或选择一个更简单的方法。可以参考本手册中
<a href="/install.html" class="link">PHP 安装说明</a>的相关章节（假设已经配置好了某个
web 服务器）。若在自己安装 PHP
时出现了问题，建议在<a href="https://www.php.net/mailing-lists.php" class="link external">» 安装邮件列表</a>中询问。如果想使用更简便的方法安装
PHP，那么可以考虑<a href="http://wikipedia.org/wiki/List_of_AMP_packages" class="link external">» 获取一个预先配置的安装包</a>，用这个安装包，只用点击几下鼠标，就可以自动地安装所有这些系统。在任何操作系统下建立有
PHP 支持的 web 服务器都十分简单，包括 MacOSX、Linux 和 Windows。在 Linux
下，会发现
<a href="http://www.rpmfind.net/" class="link external">» rpmfind</a> 和
<a href="http://rpm.pbone.net/" class="link external">» PBone</a>
能够在获取 RPM 时提供帮助。也可以使用
<a href="https://packages.debian.org/index" class="link external">» apt-get</a>
搜索 Debian 的相关软件包。
