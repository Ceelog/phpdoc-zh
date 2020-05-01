在 OpenBSD 系统下的安装
-----------------------

本章节的内容和提示仅限于将 PHP 安装到
<a href="http://www.openbsd.org/" class="link external">» OpenBSD 3.6</a>
系统上。

### 使用二进制包安装

使用二进制包安装 PHP 到 OpenBSD
系统上是被推荐的同时也是最简单的方法。PHP
核心包已经从其他模块中分离出来了并且每个模块可以被独立的安装／卸载而不影响其他模块。所有这些安装
PHP 需要的文件可以在 OpenBSD 光盘或者在 FTP 站点上找到。

需要安装的 PHP 核心包的文件是
`php4-core-4.3.8.tgz`，它包含了基本的引擎（包括 gettext 和
iconv）。其次，可能还需要安装一些模块包，如：`php4-mysql-4.3.8.tgz` 或
`php4-imap-4.3.8.tgz`。需要使用命令 **phpxs** 去激活它，并且再通过修改
`php.ini` 文件来屏蔽他们。

**示例 \#1 在 OpenBSD 系统下的软件包的安装示例**

    # pkg_add php4-core-4.3.8.tgz
    # /usr/local/sbin/phpxs -s
    # cp /usr/local/share/doc/php4/php.ini-recommended /var/www/conf/php.ini
      （加入 mysql 包）
    # pkg_add php4-mysql-4.3.8.tgz
    # /usr/local/sbin/phpxs -a mysql
      （加入 imap 包）
    # pkg_add php4-imap-4.3.8.tgz
    # /usr/local/sbin/phpxs -a imap
      （测试一下删除 mysql 包）
    # pkg_delete php4-mysql-4.3.8
    # /usr/local/sbin/phpxs -r mysql
      （安装 PEAR 库）
    # pkg_add php4-pear-4.3.8.tgz

阅读用户手册中的
<a href="http://www.openbsd.org/cgi-bin/man.cgi?query=packages" class="link external">» packages(7)</a>
部分，可以得到更多 OpenBSD 系统下有关二进制软件包的信息。

### 使用软件包

同样可以使用<a href="http://www.openbsd.org/faq/ports/ports.html" class="link external">» 软件包目录（ports tree）</a>来编译
PHP 的源代码。然而，这样的安装方式仅仅是建议对 OpenBSD
非常熟悉的高级用户去做。PHP4 的软件包被分别分为了两个子目录：core 和
extensions。其中 extensions 目录产生了所有 PHP
所支持的子模块。如果不希望创建并且使用这些模块中的某些模块，请使用
FLAVOR **no\_\*** 参数。例如，如果希望跳过编译 imap 模块，设置 FLAVOR 为
**no\_imap**即可。

### 常见问题

-   <span class="simpara"> 默认安装的 Apache 运行于
    <a href="http://www.openbsd.org/cgi-bin/man.cgi?query=chroot" class="link external">» chroot(2) jail</a>
    内，将限制 PHP 脚本只能访问 `/var/www`下面的文件。需要建立
    `/var/www/tmp` 目录来存放 PHP session 文件，或使用其它的 session
    后端。此外，数据库套接字需要被放入 jail 或者侦听
    `localhost`接口。如果使用网络函数，某些 `/etc` 下面的文件例如
    `/etc/resolv.conf` 和 `/etc/services` 需要被移动到 `/var/www/etc`
    中去。OpenBSD PEAR 包会自动安装到正确的 chroot
    目录中，因此不需要作特殊改动。有关 OpenBSD Apache 的更多信息见
    OpenBSD FAQ。 </span>
-   <span class="simpara"> 对应于
    <a href="http://www.libgd.org/" class="link external">» gd</a>
    扩展的 OpenBSD 3.6 包需要预先安装 XFree86。如果不想使用那些需要 X11
    的字体特性，则安装 `php4-gd-4.3.8-no_x11.tgz` 包来替代之。 </span>

### 早期发布版本

早期的 OpenBSD 系统使用 FLAVORS 系统把 PHP
连接为静态模式。自从使用这种方法编译就造成了问题：很难制作二进制软件包。仍然可以使用早期稳定的
ports trees，但这种方式已经不被 OpenBSD
小组所支持。如果对此有任何建议和意见，软件包当前的维护人是 Anil
Madhavapeddy（avsm at openbsd dot org）。
