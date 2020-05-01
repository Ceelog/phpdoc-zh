安装／配置
==========

**目录**

-   [需求](/judy/setup.html#需求)
-   [安装](/judy/setup.html#安装)
-   [运行时配置](/judy/setup.html#运行时配置)
-   [资源类型](/judy/setup.html#资源类型)

需求
----

This extension require the
<a href="http://judy.sourceforge.net" class="link external">» Judy C library</a>.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/judy" class="link external">» https://pecl.php.net/package/judy</a>

Installation on Linux Systems
-----------------------------

From sources
------------

Download and install
<a href="http://judy.sourceforge.net" class="link external">» libJudy</a>,
then :

         phpize
         ./configure --with-judy[=DIR]
         make
         make test
         make install
        

Ubuntu/Debian
-------------

libJudy can be installed with apt-get :

        apt-get install libjudydebian1 libjudy-dev
        

Then by installing the Judy extension from PECL or from the sources.

Installation on Windows Systems
-------------------------------

Download
<a href="http://judy.sourceforge.net" class="link external">» libJudy</a>,
then extract the sources and open the Visual Studio command prompt and
navigate to the source directory. Then execute :

    build

This creates "Judy.lib", copy this into the php-sdk library folder and
name it "libJudy.lib" Then copy the include file "judy.h" into the
php-sdk includes folder.

Next, the PHP Judy extension can be installed from PECL or from the
sources by extracting the pecl/judy into your build folder where the
build scripts will be able to pick it up, e.g.:

        C:\php\pecl\judy\
       

If your source of PHP is located in:

        C:\php\src\
       

The rest of the steps is pretty straight forward, like any other
external extension:

        buildconf
        configure --with-judy=shared
        nmake
       

Installation on macOS
---------------------

Download and install
<a href="http://judy.sourceforge.net" class="link external">» libJudy</a>.
Then install the Judy extension from PECL or from the sources.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
