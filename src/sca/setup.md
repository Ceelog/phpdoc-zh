安装／配置
==========

**目录**

-   [需求](/sca/setup.html#需求)
-   [安装](/sca/setup.html#安装)
-   [运行时配置](/sca/setup.html#运行时配置)
-   [资源类型](/sca/setup.html#资源类型)

需求
----

If you want to use SCA to consume or produce Web services then you need
PHP 5.2.0 or later, built with the soap extension enabled. If you just
want to use local components, and do not wish to use the Web service
bindings, then this version of SCA for PHP will also run with PHP 5.1.6.

SCA is packaged along with SDO in one combined package on PECL. See
http://www.php.net/sdo\#sdo.installation for installing the SCA\_SDO
package from PECL. The SCA code must be on the include path of your PHP
installation, for example if it is installed as /usr/local/lib/php/SCA,
the include\_path directive must include /usr/local/lib/php

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/sca" class="link external">» https://pecl.php.net/package/sca</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
