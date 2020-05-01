Debian GNU/Linux 安装说明
-------------------------

本节包含了在
<a href="http://www.debian.org/" class="link external">» Debian GNU/Linux</a>
下安装 PHP 的说明和提示。

**Warning**

这里不支持非官方的第三方发行包。任何错误应报告给 Debian
开发组，除非该错误在使用从官方<a href="https://www.php.net/downloads.php" class="link external">» 下载</a>的最新版时仍能重现。

尽管在 Unix 下编译 PHP 的指示也适用于
Debian，本节包含有一些特定信息，例如使用 *apt-get* 或者 *aptitude*
命令。本节中这两条命令可以互换。

### 使用 APT

首先，注意其它有关的包可能需要 *libapache2-mod-php5* 集成入 Apache
2，以及 PEAR 的 *php-pear*。

其次，在安装一个包之前，最好先确定该包是最新版。通常可以运行命令
**apt-get update**。

**示例 \#1 Debian 下将 PHP 安装入 Apache 2 的例子**

``` shell
# apt-get install php5-common libapache2-mod-php5 php5-cli
```

APT 将自动安装 Apache 2 的 PHP 5 模块以及所有依赖的库并激活之。应重启动
Apache 以使更改生效，例如：

**示例 \#2 安装完 PHP 后停止并启动 Apache**

``` shell
# /etc/init.d/apache2 stop
# /etc/init.d/apache2 start
```

### 更好地控制配置

上一节中 PHP 仅安装了核心模块。很可能还需要更多模块，例如
<a href="/set/mysqlinfo.html#Mysql（原始）" class="link">MySQL</a>，<a href="/book/curl.html" class="link">cURL</a>，<a href="/book/image.html" class="link">GD</a>
等。这些模块也可以通过 *apt-get* 命令安装。

**示例 \#3 取得 PHP 附加软件包的列表**

``` shell
# apt-cache search php5
# aptitude search php5
# aptitude search php5 |grep -i mysql
```

以上命令的输出中列出了很多的包，其中有几个针对 PHP 的模块例如
php5-cgi，php5-cli 以及 php5-dev。决定好要安装哪些之后可以用 *apt-get*
或者 *aptitude* 来安装。Debian 会进行倚赖性检查，会给出提示，例如安装
MySQL 和 cURL：

**示例 \#4 安装 PHP 的 MySQL 和 cURL 支持**

``` shell
# apt-get install php5-mysql php5-curl
```

APT 会自动把适当的行添加到不同的 `php.ini` 相关文件中去，例如
`/etc/php5/apache2/php.ini`，`/etc/php5/conf.d/pdo.ini`
等，并且根据扩展，还会添加类似 *extension=foo.so*
的内容。不过还是需要重新启动 web 服务器（例如 Apache）以使这些改动生效。

### 常见问题

-   <span class="simpara"> 如果 PHP 脚本没有通过 web
    服务器被解析，则有可能是 PHP 没有被加入到 web 服务器的配置文件中，在
    Debian 中可能是 `/etc/apache2/apache2.conf` 或类似文件。具体内容参见
    Debian 手册。 </span>
-   <span class="simpara">
    如果某扩展貌似已经安装，但其函数却又未定义，确保合适的 ini
    文件已被加载并且 web 服务器在安装后重新启动过。 </span>
-   <span class="simpara"> 在 Debian（以及其它 Linux
    变种）下有两个基本命令来安装包：*apt-get* 和
    *aptitude*。不过要解释这两个命令的细微区别已超出本手册范围。 </span>
