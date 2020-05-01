安装／配置
==========

**目录**

-   [需求](/fann/setup.html#需求)
-   [安装](/fann/setup.html#安装)
-   [运行时配置](/fann/setup.html#运行时配置)
-   [资源类型](/fann/setup.html#资源类型)

需求
----

PHP \>= 5.2.0 and libfann \>= 2.1.0

安装
----

FANN PHP 扩展在所有的 Linux 系统都可以运行的。

-   <a href="/fann/setup.html#FANN%20库安装" class="xref"></a>
-   <a href="/fann/setup.html#PECL%20安装" class="xref"></a>
-   <a href="/fann/setup.html#手动安装" class="xref"></a>

FANN 库安装
-----------

在你安装扩展之前确认 *libfann* 库已经安装在你的系统上了。在大部分的
Linux 发行版本的源中都包含了这个库 (搜索 *fann*). 你需要安装开发版本。

如果 libfann
没安装，你得先安装它。随便你从<a href="http://leenissen.dk/fann/wp/" class="link external">» 官方网站</a>下载或者从你系统自带源中下载。比如在
Fedora 系统中：


    $ sudo yum install fann-devel

或者 Ubuntu 系统中：


    $ sudo apt-get install libfann-dev

如果该库被手动重装，在安装之前所有的老版本库文件应该先被删除，否则老版本的库还是会被连接。

PECL 安装
---------

在 PECL 库里这个扩展是可用的。 安装起来也很容易。只要运行：


    $ sudo pecl install fann

手动安装
--------

如果开发者和用户对最新的更改很感兴趣，你可以编译
<a href="https://github.com/bukka/php-fann" class="link external">» Github</a>
上最新的源代码。 前往 Github 点击 "Download ZIP" 按钮，然后运行:


    $ unzip php-fann-master.zip
    $ cd php-fann-master
    $ phpize
    $ ./configure
    $ make all
    $ sudo make install

在 php.ini 配置文件中做如下更改:

-   确认 *extension\_dir* 变量指向 *fann.so* 文件的目录.
    该扩展构建过程中，在控制台输出时将会显示这个模块的安装路径，比如：


        Installing '/usr/lib/php/extensions/no-debug-non-zts-20060613/fann.so'

    确认这个路径和 PHP 扩展是一致的，运行命令：


        $ php -i | grep extension_dir
          extension_dir => /usr/lib/php/extensions/no-debug-non-zts-20060613 =>
                           /usr/lib/php/extensions/no-debug-non-zts-20060613

    如果不是，更改 php.ini 文件的 *extension\_dir* 值或者移动 *fann.so*
    文件到相应的目录。

-   在 PHP 启动时添加该扩展，添加如下行代码：


        extension=fann.so

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------
