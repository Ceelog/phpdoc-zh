安装／配置
==========

**目录**

-   [需求](/blenc/setup.html#需求)
-   [安装](/blenc/setup.html#安装)
-   [运行时配置](/blenc/setup.html#运行时配置)
-   [资源类型](/blenc/setup.html#资源类型)

需求
----

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/blenc" class="link external">» https://pecl.php.net/package/blenc</a>

It's strongly recommended to install BLENC from sources without 'pecl'
command. In this way you can:

-   Specify your personal encryption key used to create redistributable
    keys. Your sourcecode will be more difficult to decrypt also for
    users that can read your key\_file on webserver.
-   Specify a expiration date for the BLENC module. With expiration date
    you can decide that BLENC module on target system will work until a
    date. After that BLENC will not decrypt any files.

All these configuration options are stored into header file:
blenc\_protect.h

Please read the content of blenc\_protect.h in sources of BLENC to know
how set these hardcoded options.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                         | 默认                     | 可修改范围    | 更新日志 |
|--------------------------------------------------------------|--------------------------|---------------|----------|
| <a href="/blenc/setup.html#" class="link">blenc.key_file</a> | /usr/local/etc/blenckeys | PHP\_INI\_ALL |          |

这是配置指令的简短说明。

`blenc.key_file` <span class="type">string</span>  
It's the location where BLENC can find the file containing a list of
available decryption keys. This file must be readable by webserver.

资源类型
--------
