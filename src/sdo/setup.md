安装／配置
==========

**目录**

-   [需求](/sdo/setup.html#需求)
-   [安装](/sdo/setup.html#安装)
-   [运行时配置](/sdo/setup.html#运行时配置)
-   [资源类型](/sdo/setup.html#资源类型)

需求
----

The SDO extension requires PHP 5.1.0 or higher. It also requires the
libxml2 library. Normally libxml2 will already be installed, but if not,
it can be downloaded from
<a href="http://www.xmlsoft.org/" class="link external">» http://www.xmlsoft.org/</a>.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/sca_sdo" class="link external">» https://pecl.php.net/package/sca_sdo</a>.

> **Note**:
>
> Earlier versions of the SDO extension required a separate shared
> library for the XML DAS. This is now obsolete and any references to
> `php_sdo_das_xml.dll` or `sdo_das_xml.so` should be removed from your
> `php.ini`.

**Unix systems**

1.  The three SDO components - the SDO core, the XML DAS and the
    Relational DAS - are packaged together with *Service Component
    Architecture (SCA)* into one PECL project, SCA\_SDO, so you can
    download SCA and all three parts of SDO with the command:

        pecl install SCA_SDO

    This command will build the SDO shared library as well as installing
    the PHP files that make up SCA and the SDO Relational DAS.

    If you want to use the latest beta version, then instead run:

        pecl install SCA_SDO-beta

2.  The **pecl** command automatically installs the SDO module into your
    PHP extensions directory. To enable the SDO extension you must add
    the following line to `php.ini`:

        extension=sdo.so

    For more information about building PECL packages, consult the
    <a href="/install/pecl.html" class="link">PECL installation</a>
    section of the manual.

**Building SDO on Linux**

This section describes how to build the SDO core and XML DAS on Linux.
You would only need to know how to do this if you wish to build a recent
version that you have checked out of SVN.

1.  Change to the main extension directory: **cd \< wherever your sdo
    code is \>**

2.  Run **phpize**, which will set up the environment to compile SDO.

3.  Next, run **./configure; make; make install**. Please note, you may
    need to login as root to install the extension.

4.  Make sure that the module is loaded by PHP, by adding
    `extension=sdo.so` to your `php.ini` file.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
