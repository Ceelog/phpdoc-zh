Unix 系统下的 Apache 2.x
------------------------

本节包括在 Unix 平台的 Apache 2.x 下安装 PHP 的说明和提示。

**Warning**

不推荐在使用 Apache 2 的产品中使用线程化 MPM。应使用预分支 MPM，Apache
2.0 和 2.2 默认的 MPM。其原因见 FAQ
中的相关条目<a href="/faq/installation.html#faq.installation.apache2" class="link">使用线程化 MPM 的 Apache2</a>。

推荐阅读
<a href="http://httpd.apache.org/docs/current/" class="link external">» Apache 文档</a>，了解一下
Apache 2.x 服务器，以及详细的安装参数。

可以从
<a href="http://httpd.apache.org/" class="link external">» Apache 下载站点</a>下载最新版本的Apache，并且根据上文选择合适版本的
PHP 下载。本向导仅包含最基础的内容，只能让 Apache 2.x 和 PHP
能够正常工作。更多信息请阅读
<a href="http://httpd.apache.org/docs/current/" class="link external">» Apache 文档</a>。这里省略所有的版本号，以保证本文的正确性。需要将本文的“NN”替换为相应的版本号。

当前 Apache 2.x 有两个流行的版本 -
2.0、2.2。虽然选择某个版本会有种种原因，但是如果可以考虑的话，我们还是建议使用最新的
Apache 2.2 版本。当然，以下的介绍同样适合 Apache 2.0 和 2.2。

1.  从上面列出的地方获取 Apache 源码包，然后解压：

        gzip -d httpd-2_x_NN.tar.gz
        tar -xf httpd-2_x_NN.tar

2.  同样，获取 PHP 源码包并解压：

        gunzip php-NN.tar.gz
        tar -xf php-NN.tar

3.  编译并安装 Apache。请参考 Apache 安装文档了解编译 Apache
    的更多细节。

        cd httpd-2_x_NN
        ./configure --enable-so
        make
        make install

4.  现在已经将 Apache 2.x.NN 安装在
    /usr/local/apache2。本安装支持可装载模块 和标准的 MPM
    prefork。之后，可以使用如下命令启动 Apache 服务器：

        /usr/local/apache2/bin/apachectl start

    如果成功，可以停止 Apache 服务器并继续安装 PHP：

        /usr/local/apache2/bin/apachectl stop

5.  现在需要配置并编译 PHP。在这里可以用各种各样的参数来自定义
    PHP，例如启动哪些扩展功能包的支持等。用 ./configure --help
    命令可以列出当前可用的所有参数。在此例中，将给出一个在有 MySQL
    支持的 Apache 2 上进行配置的范例。

    如果按照上面的说明从源代码编译了 Apache，下面的例子会正确匹配 apxs
    的路径。如果通过其他方式安装了 Apache，需要相应的调整 apxs
    的路径。注意，在有些发行版本中，可能将 apxs 更名为 apxs2。

        cd ../php-NN
        ./configure --with-apxs2=/usr/local/apache2/bin/apxs --with-mysql
        make
        make install

    如果决定在安装后改变配置选项，只需重复最后的三步
    configure，make，以及 make install，然后需要重新启动 Apache
    使新模块生效。Apache 不需要重新编译。

    请注意，除非明确有提示，否则“make install”命令将安装 PEAR、各种 PHP
    工具诸如 phpize，并安装 PHP CLI 等等。

6.  配置 php.ini

        cp php.ini-development /usr/local/lib/php.ini

    可以编辑 php.ini 来设置 PHP
    运行时的选项。如果想要把此文件放到另外的位置，需要在步骤 5 添加
    --with-config-file-path=/path 选项。

    如果选择了 php.ini-production，请务必阅读其中的变更列表，它们将影响
    PHP 的执行。

7.  编辑 httpd.conf 文件以调用 PHP 模块。LoadModule
    达式右边的路径必须指向系统中的 PHP 模块。以上的 make install
    命令可能已经完成了这些，但务必要检查。

    ``` apache-conf
    LoadModule php5_module modules/libphp5.so
    ```

8.  告知 Apache 将特定的扩展名解析成 PHP，例如，让 Apache 将扩展名 .php
    解析成 PHP。为了避免潜在的危险，例如上传或者创建类似 exploit.php.jpg
    的文件并被当做 PHP 执行，我们不再使用 Apache 的 AddType
    指令来设置。参考下面的例子，你可以简单的将需要的扩展名解释为
    PHP。我们演示为增加.php。

    ``` apache-conf
    <FilesMatch \.php$>
        SetHandler application/x-httpd-php
    </FilesMatch>
    ```

    或者，你也想将 .php，.php2，.php3，.php4，.php5，.php6，以及 .phtml
    文件都当做 PHP 来运行，我们无需额外的设置，仅需按照下面这样来：

    ``` apache-conf
    <FilesMatch "\.ph(p[2-6]?|tml)$">
        SetHandler application/x-httpd-php
    </FilesMatch>
    ```

    然后，可以将 .phps 文件由 PHP
    源码过滤器处理，使得其在显示时可以高亮源码，设置如下：

    ``` apache-conf
    <FilesMatch "\.phps$">
        SetHandler application/x-httpd-php-source
    </FilesMatch>
    ```

    mod\_rewrite 也有助于将那些不需要运行的 .php
    文件的源码高亮显示，而并不需要将他们更名为 .phps 文件：

    ``` apache-conf
    RewriteEngine On
    RewriteRule (.*\.php)s$ $1 [H=application/x-httpd-php-source]
    ```

    不要在正式生产运营的系统上启动 PHP
    源码过滤器，因为这可能泄露系统机密或者嵌入的代码中的敏感信息。

9.  按照通常的方式启动 Apache 服务：

        /usr/local/apache2/bin/apachectl start

    或者

        service httpd restart

按照上面的步骤便可以使 Apache 2.ｘ 将 PHP 作为 *SAPI* 模块了。当然
Apache 和 PHP 都还有很多配置选项，可以在相应的源代码目录中使用
**./configure --help** 获得更多信息。

假如要编译一个多线程版本的 Apache，可在编译时选择用 `worker` MPM
来替换标准的 `prefork` MPM。只需在上面的第 3 步使用：

  
--with-mpm=worker  

如果不是很明确这样做的后果并且大概理解其含义的话，最好不要进行这一步。更多信息请参考
Apache 文档中关于
<a href="http://httpd.apache.org/docs/current/mpm.html" class="link external">» MPM-Modules</a>
的部分。

> **Note**:
>
> <a href="/faq/installation.html#faq.installation.apache.multiviews" class="link">Apache MultiViews 常见问题</a>中讨论了在
> PHP 中使用 MultiViews。

> **Note**:
>
> 要编译多线程版本的 Apache，系统必须支持多线程。这也意味着需要将 PHP
> 编译为正处在试验阶段的 Zend Thread
> Safety（ZTS），因此并不是所有的扩展都可以使用了。推荐编译 Apache
> 使用标准的 `prefork` MPM-Module。
