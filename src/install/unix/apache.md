Unix 系统下的 Apache 1.3.x
--------------------------

本节包括在 Unix 平台的 Apache 下安装 PHP
的说明和提示。我们在另外的页面也有
<a href="/install/unix/apache2.html" class="link">Apache 2 的安装和说明</a>。

可以从<a href="/configure.html" class="link">核心配置选项列表</a>以及位于手册对应部分的特定扩展配置选项中选择参数并在安装步骤第
10 步将它们添加到 **configure**
命令中。版本号在这里被省略了以保证此说明的正确性。需要将这里的“xxx”替换为自己使用的文件的正确值。

**示例 \#1 PHP 的 Apache 共享模块版本安装说明**

    1.  gunzip apache_xxx.tar.gz
    2.  tar -xvf apache_xxx.tar
    3.  gunzip php-xxx.tar.gz
    4.  tar -xvf php-xxx.tar
    5.  cd apache_xxx
    6.  ./configure --prefix=/www --enable-module=so
    7.  make
    8.  make install
    9.  cd ../php-xxx

    10. 现在，配置 PHP。这是定制 PHP 的不同选项的时候，例如要加载哪些扩展库。使用
          ./configure --help
        来列出可用的选项。在下面的示例中只是简单地配置 Apache 1 和 MySQL 支持。
        用户的 apxs 的路径可能和此示例中的不同。

          ./configure --with-mysql --with-apxs=/www/bin/apxs

    11. make
    12. make install

        如果在安装之后决定修改配置选项，那么只需重复以上最后三步。只须重新启动
        Apache 就可以使新模块生效。不需要重新编译 Apache。
        
        注意除非特别指出，“make install”总是会安装 PEAR，各种 PHP 工具例如 phpize，
        PHP CLI 以及其它。

    13. 建立 php.ini 文件。

          cp php.ini-dist /usr/local/lib/php.ini

        可以编辑 php.ini 来设置 PHP 选项。如果想把 php.ini 放在其它目录，在第
        10 步加上以下选项：

          --with-config-file-path=/path

        如果选择了  php.ini-production，确保阅读一下其中的变更说明，因为这些会
        影响到 PHP 的行为。

    14. 编辑 httpd.conf 来加载 PHP 模块。在 LoadModule 语句右边的路径必须指向系统中
        PHP 模块所在的路径。上面的 make install 步骤可能已经添加了，但还是检查确认一下。

          LoadModule php5_module        libexec/libphp5.so

    15. 在 httpd.conf 中加入 AddModule 部分，在 ClearModuleList 下面的某处，加上这一句：

          AddModule mod_php5.c

    16. 告诉 Apache 将哪些后缀作为 PHP 解析。例如，让 Apache 把 .php 后缀的文件解析为
        PHP。可以将任何后缀的文件解析为 PHP，只要在以下语句中加入并用空格分开。这里以
        添加一个 .phtml 来示例。

          AddType application/x-httpd-php .php .phtml

        为了将 .phps 作为 PHP 的源文件进行语法高亮显示，还可以加上：

          AddType application/x-httpd-php-source .phps

    17. 用通常的过程启动 Apache（必须完全停止 Apache 再重新启动，而不是用 HUP 或者
        USR1 信号使 Apache 重新加载）。

也可以将 PHP 作为静态对象来安装：

**示例 \#2 PHP 的 Apache 静态模块版本安装说明**

    1.  gunzip -c apache_1.3.x.tar.gz | tar xf -
    2.  cd apache_1.3.x
    3.  ./configure
    4.  cd ..

    5.  gunzip -c php-5.x.y.tar.gz | tar xf -
    6.  cd php-5.x.y
    7.  ./configure --with-mysql --with-apache=../apache_1.3.x
    8.  make
    9.  make install

    10. cd ../apache_1.3.x

    11. ./configure --prefix=/www --activate-module=src/modules/php5/libphp5.a
        （上面一行是正确的！是的，我们知道 libphp5.a 尚不存在，还不到时候，
          它会在之后被创建。）

    12. make
        （现在应该有一个 httpd 二进制文件，可以将它复制到 Apache bin 目录。如果这是
          第一次安装，还要“make install”。)

    13. cd ../php-5.x.y
    14. cp php.ini-development /usr/local/lib/php.ini

    15. 可以编辑 /usr/local/lib/php.ini 文件以设置 PHP 选项。编辑 httpd.conf 或
        srm.conf 文件，添加：
        AddType application/x-httpd-php .php

根据 Unix 系统和 Apache 安装方法的不同，有很多方法停止和重启动
Apache。以下是一些不同的 Apache／UNIX 下重启动 Apache 的典型命令。需要把
*/path/to/*替换成自己系统上的确切路径。

**示例 \#3 重启动 Apache 的示例命令**

``` shell
1. 在一些 Linux 和 SysV 的变种下：
/etc/rc.d/init.d/httpd restart

2. 使用 apachectl 脚本：
/path/to/apachectl stop
/path/to/apachectl start

3. httpdctl 和 httpsdctl（使用了 OpenSSL），类似 apachectl：
/path/to/httpsdctl stop
/path/to/httpsdctl start

4. 使用了 mod_ssl，或其他 SSL 服务器，可能需要手工重启动：
/path/to/apachectl stop
/path/to/apachectl startssl
```

apachectl 和 http(s)dctl
程序所在的路径在不同系统中通常不一样。如果系统中有 *locate* 或者
*whereis* 或者 *which* 命令，那么可以帮助找到这些控制程序。

编译 PHP 和 Apache 的不同例子还有：

``` shell
./configure --with-apxs --with-pgsql
```

此配置将生成在 Apache 的 `httpd.conf` 文件中用 LoadModule 加载的
`libphp5.so` 共享库。而 PostgreSQL 支持将嵌入到此共享库中。

``` shell
./configure --with-apxs --with-pgsql=shared
```

此配置将生成 Apache 的 `libphp5.so` 共享库，并且还生成 `pgsql.so`
共享库，可以在 `php.ini` 文件中用 extension 指令加载，或者在 PHP
脚本中用 <span class="function">dl</span> 函数明确地加载。

``` shell
./configure --with-apache=/path/to/apache_source --with-pgsql
```

此配置将生成一个 `libmodphp5.a` 库，一个 `mod_php5.c`
和一些相关的文件并且拷贝到 Apache 源程序目录中的
*src/modules/php5*目录下。然后用
*--activate-module=src/modules/php5/libphp5.a* 编译 Apache，Apache
编译系统会生成 `libphp5.a` 并且将其静态地连接到 `httpd`
程序中。PostgreSQL 支持也直接包括在这个 `httpd`
程序中了，因此最终结果是单一的一个包括了所有 Apache 和 PHP 支持的
`httpd` 可执行文件。

``` shell
./configure --with-apache=/path/to/apache_source --with-pgsql=shared
```

此配置和上面一样——除了没有在最后的 `httpd` 可执行文件中包括 PostgreSQL
的支持以及生成了一个 `pgsql.so` 共享库以外。该共享库可以在 `php.ini`
文件中或者用 <span class="function">dl</span> 函数加载。

当选择不同的方法编译 PHP
时，需要考虑每种方法的优势和缺点。用共享对象方式编译 PHP
意味着可以单独编译 Apache，并且不用在添加或修改了 PHP
的时候重新编译所有程序。用内置方法编译 PHP（静态方式）意味着 PHP
可以加载和运行得更快。更多信息见 Apache 的
<a href="http://httpd.apache.org/docs/current/dso.html" class="link external">» DSO 支持页面</a>。

> **Note**:
>
> Apache 默认的 `httpd.conf` 文件中目前包括类似如下的内容：
>
> ``` apache-conf
> User nobody
> Group "#-1"
> ```
>
> 除非把它修改成“Group nogroup”或者其它类似的（“Group
> daemon”也很通用），PHP 将不能打开文件。

> **Note**:
>
> 确认在使用 **--with-apxs=/path/to/apxs** 时指向 Apache
> 安装后的目录中的 apxs。绝对不能用 Apache 源程序中的 apxs
> 而要用安装后的 apxs。
