安装／配置
==========

**目录**

-   [需求](/svm/setup.html#需求)
-   [安装](/svm/setup.html#安装)
-   [运行时配置](/svm/setup.html#运行时配置)
-   [资源类型](/svm/setup.html#资源类型)

需求
----

Libsvm itself is required, and is available through some package
management - libsvm-devel for RPM based system or libsvm-dev for Debian
based ones. Alternatively it is available direct from the website. If
installing from the
<a href="http://www.csie.ntu.edu.tw/~cjlin/libsvm" class="link external">» official website</a>
then some steps will need to be taken as the package does not install
automatically. For example, assuming the latest version is 3.1:

    wget http://www.csie.ntu.edu.tw/~cjlin/cgi-bin/libsvm.cgi?+http://www.csie.ntu.edu.tw/~cjlin/libsvm+tar.gz 
    tar xvzf libsvm-3.1.tar.gz 
    cd libsvm-3.1
    make lib 
    cp libsvm.so.1 /usr/lib 
    ln -s libsvm.so.1 libsvm.so 
    ldconfig 
    ldconfig --print | grep libsvm

This last step should show libsvm is installed.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/svm" class="link external">» https://pecl.php.net/package/svm</a>

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
