Unix 系统下的 Nginx 1.4.x
-------------------------

本文档包括使用 PHP-FPM 为 Nginx 1.4.x HTTP 服务器安装和配置 PHP
的说明和提示。

本指南假定您已经从源代码成功构建 Nginx，并且其二进制文件和配置文件都位于
*/usr/local/nginx*。 如果您使用其他方式获取的 Nginx，请参考
<a href="http://wiki.nginx.org/Main" class="link external">» Nginx Wiki</a>
并对照本文档完成安装。

本文档仅包含 Nginx 服务器的基本配置，它将通过 80 端口提供 PHP
应用的处理能力。 如果您需要超出本文档范围的安装配置指导，建议您查阅
Nginx 和 PHP-FPM 的文档。

需要注意的是，本文档一律使用 'x' 来表示版本号，请根据实际情况将 'x'
替换为对应的版本号。

1.  建议您访问 Nginx Wiki
    <a href="http://wiki.nginx.org/Install" class="link external">» 安装</a>
    页面以获取并在您的系统上安装 Nginx。

2.  获取并解压 PHP 源代码:

        tar zxf php-x.x.x

3.  配置并构建 PHP。在此步骤您可以使用很多选项自定义
    PHP，例如启用某些扩展等。 运行 ./configure --help
    命令来获得完整的可用选项清单。 在本示例中，我们仅进行包含 PHP-FPM 和
    MySQL 支持的简单配置。

        cd ../php-x.x.x
        ./configure --enable-fpm --with-mysql
        make
        sudo make install

4.  创建配置文件，并将其复制到正确的位置。

        cp php.ini-development /usr/local/php/php.ini
        cp /usr/local/etc/php-fpm.d/www.conf.default /usr/local/etc/php-fpm.d/www.conf
        cp sapi/fpm/php-fpm /usr/local/bin

5.  需要着重提醒的是，如果文件不存在，则阻止 Nginx 将请求发送到后端的
    PHP-FPM 模块， 以避免遭受恶意脚本注入的攻击。

    将 php.ini 文件中的配置项
    <a href="/ini/core.html#ini.cgi.fix-pathinfo" class="link">cgi.fix_pathinfo</a>
    设置为 *0* 。

    打开 php.ini:

        vim /usr/local/php/php.ini

    定位到 *cgi.fix\_pathinfo=* 并将其修改为如下所示：

        cgi.fix_pathinfo=0

6.  在启动服务之前，需要修改 php-fpm.conf 配置文件，确保 php-fpm
    模块使用 www-data 用户和 www-data 用户组的身份运行。

        vim /usr/local/etc/php-fpm.d/www.conf

    找到以下内容并修改：

        ; Unix user/group of processes
        ; Note: The user is mandatory. If the group is not set, the default user's group
        ;       will be used.
        user = www-data
        group = www-data

    然后启动 php-fpm 服务：

        /usr/local/bin/php-fpm

    本文档未涵盖对 php-fpm
    进行进一步配置的信息，如果您需要更多信息，请查阅相关文档。

7.  配置 Nginx 使其支持 PHP 应用：

        vim /usr/local/nginx/conf/nginx.conf

    修改默认的 location 块，使其支持 .php 文件：

    ``` nginx-conf
    location / {
        root   html;
        index  index.php index.html index.htm;
    }
    ```

    下一步配置来保证对于 .php 文件的请求将被传送到后端的 PHP-FPM 模块，
    取消默认的 PHP 配置块的注释，并修改为下面的内容：

    ``` nginx-conf
    location ~* \.php$ {
        fastcgi_index   index.php;
        fastcgi_pass    127.0.0.1:9000;
        include         fastcgi_params;
        fastcgi_param   SCRIPT_FILENAME    $document_root$fastcgi_script_name;
        fastcgi_param   SCRIPT_NAME        $fastcgi_script_name;
    }
    ```

    重启 Nginx。

        sudo /usr/local/nginx/sbin/nginx -s stop
        sudo /usr/local/nginx/sbin/nginx

8.  创建测试文件。

        rm /usr/local/nginx/html/index.html
        echo "<?php phpinfo(); ?>" >> /usr/local/nginx/html/index.php

    打开浏览器，访问 http://localhost，将会显示 phpinfo() 。

通过以上步骤的配置，Nginx 服务器现在可以以 *SAPI* *SAPI* 模块的方式支持
PHP 应用了。 当然，对于 Nginx 和 PHP 的配置，还有很多可用的选项，
请在对应的源代码目录执行 **./configure --help** 来查阅更多配置选项。
