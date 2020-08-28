Unix系统下的LiteSpeed、OpenLiteSpeed服务
----------------------------------------

LiteSpeed PHP 是一个通过LiteSpeed
SAPI方式和LiteSpeed协同工作的PHP优化编译器。LSPHP有自己的进程和独立的二进制包，这样可以让LSPHP能够执行命令行中的命令。

LSAPI是一个高性能的API框架，它能够在LiteSpeed和第三方web服务之间很好的工作。它的原理和FCGI很像，但是它更加高效。

本文档将包含安装和配置PHP的LSAPI，并将LSAPI适用于LiteSpeed服务和OpenLiteSpeed服务。

本文档假定 LSWS 或者 OLS
安装在默认的路径和标记。这两个web服务的默认路径为：/usr/local/lsws，并且都可以从bin子目录下运行。

请注意：本文档中对版本号使用*x*替代，以确保本文档在将来保持正确，请根据需要替换对应的版本号。

1.  要获取和安装LiteSpeed服务或者OpenLiteSpeed服务，请访问LiteSpeed wiki
    <a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:installation" class="link external">» 安装页面</a>
    或者 OpenLiteSpeed wiki
    <a href="http://open.litespeedtech.com/mediawiki/index.php/Help:Install" class="link external">» 安装页面</a>.

2.  获取并且解压PHP源码：

        mkdir /home/php
        cd /home/php
        wget http://us1.php.net/get/php-x.x.x.tar.gz/from/this/mirror
        tar -zxvf php-x.x.x.tar.gz
        cd php-x.x.x

3.  配置和生成PHP。这里可以根据需要来定制PHP需要的功能，例如需要开启哪些扩展。执行
    ./configure --help
    可以获得可用的配置选项。在例子中，我们将使用LiteSpeed服务默认推荐的配置：

        ./configure ... '--with-litespeed'
        make
        sudo make install

4.  检查LSPHP是否安装正确

    检查LSPHP是否安装正确的一种最简单的方式是执行下面的命令：

        cd /usr/local/lsws/fcgi-bin/
        ./lsphp5 -v

    它将会返回新生成的PHP的版本信息：

        PHP 5.6.17 (litespeed) (built: Mar 22 2016 11:34:19)
        Copyright (c) 1997-2014 The PHP Group
        Zend Engine v2.6.0, Copyright (c) 1998-2015 Zend Technologies

    注意括号中的 *litespeed* 。 这表名PHP已经支持LSAPI服务。

按照上面的步骤，LiteSpeed / OpenLiteSpeed
已经作为PHP的SAPI扩展来运行。LSWS / OLS
和PHP更多的配置选项，请查看LiteSpeed wiki：
<a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:php" class="link external">» PHP</a>.

从命令行来使用LSPHP：

LSPHP(LSAPI + PHP)
命令行模式常用于远程服务器上不需要一个web服务但是又需要处理PHP程序。它常用于处理常驻在本地服务器的PHP程序（独立的）。这个设置适用于在远程服务器上PHP程序的扩展方式。

从命令行启动一个远程的LSPHP服务： LSPHP
是可执行文件，可以手动启动，通过参数 -b socket地址
来绑定到IPv4，IPv6，或者Unix套接字上。

例如：

LSPHP绑定到所有IPv4和IPv6地址的3000端口：

    /path/to/lsphp -b [::]:3000

LSPHP绑定到所有IPv4地址的3000端口：

    /path/to/lsphp -b *:3000

LSPHP绑定到IP地址为192.168.0.2的3000端口：

    /path/to/lsphp -b 192.168.0.2:3000

LSPHP通过Unix套接字*/tmp/lsphp\_manual.sock*接受请求：

    /path/to/lsphp -b /tmp/lsphp_manual.sock

在LSPHP执行前，可以设置环境变量：

    PHP_LSAPI_MAX_REQUESTS=500 PHP_LSAPI_CHILDREN=35 /path/to/lsphp -b IP_address:port

目前LiteSpeed PHP可适用于LiteSpeed服务，OpenLiteSpeed服务和Apache
mod\_lsapi。如果需要服务器端的配置方法，请参考相应的wiki页面：
<a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:php:configuring-lsws-for-php" class="link external">» LiteSpeed Web Server</a>
和
<a href="http://open.litespeedtech.com/mediawiki/index.php/Help:Default_PHP_Settings" class="link external">» OpenLiteSpeed</a>.

LSPHP也可以通过其它的方式来安装。

CentOS:
在CentOS系统中，LSPHP可以从LiteSpeed镜像或者Remi镜像中通过<a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:php:rpm" class="link external">» RPM</a>的方式安装。

Debian:
在Debian系统中，LSPHP可以从LiteSpeed镜像中通过<a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:php:apt" class="link external">» apt</a>的方式安装。

cPanel:
怎样通过cPanel和LSWS/OLS在EasyApache4中安装LSPHP，请参考各自的<a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:cpanel:easyapache4-config" class="link external">» wiki page</a>

Plesk:
Plesk可以在CentOS，CloudLinux，Debian和Ubuntu上使用LSPHP，想获取更多的信息，请参考对应的<a href="https://www.litespeedtech.com/support/wiki/doku.php/litespeed_wiki:plesk:php_guide" class="link external">» wiki page</a>
