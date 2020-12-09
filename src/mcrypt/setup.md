安装／配置
==========

**目录**

-   [需求](/mcrypt/setup.html#需求)
-   [安装](/mcrypt/setup.html#安装)
-   [运行时配置](/mcrypt/setup.html#运行时配置)
-   [资源类型](/mcrypt/setup.html#资源类型)

需求
----

这些函数需要使用
<a href="http://mcrypt.sourceforge.net/" class="link external">» mcrypt</a>
库。 请从
<a href="http://mcrypt.sourceforge.net/" class="link external">» http://mcrypt.sourceforge.net/</a>
下载 `libmcrypt-x.x.tar.gz`， 并按以下指导完成安装。

你需要使用 libmcrypt 2.5.6 或更高版本。

PHP 5.2 的 Windows 二进制发行版中已经包含了本库。 PHP 5.3 的 Windows
二进制发行版中开始使用 MCrypt 静态库， 所以不再需要 DLL。

如果使用 libmcrypt 2.4.x 或更高版本链接编译
PHP，支持以下附加的分组加密算法：
CAST，LOKI97，RIJNDAEL，SAFERPLUS，SERPENT，
以及以下流密码：ENIGMA（加密）， PANAMA，RC4 和 WAKE。 如果使用
libmcrypt 2.4.x 或更高版本，那么还支持 nOFB 密码模式。

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/mcrypt" class="link external">» https://pecl.php.net/package/mcrypt</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                 | 默认       | 可修改范围    | 更新日志 |
|----------------------------------------------------------------------|------------|---------------|----------|
| <a href="/mcrypt/setup.html#" class="link">mcrypt.algorithms_dir</a> | **`null`** | PHP\_INI\_ALL |          |
| <a href="/mcrypt/setup.html#" class="link">mcrypt.modes_dir</a>      | **`null`** | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`mcrypt.algorithms_dir` <span class="type">string</span>  
包含算法的目录。 默认情况向是 libmcrypt 的编译目录， 通常是
*/usr/local/lib/libmcrypt*。 更多信息请参见 <span
class="function">mcrypt\_list\_algorithms</span>。

`mcrypt.modes_dir` <span class="type">string</span>  
包含模式的目录。 默认情况向是 libmcrypt 的编译目录， 通常是
*/usr/local/lib/libmcrypt*。 更多信息请参见 <span
class="function">mcrypt\_list\_modes</span>。

资源类型
--------

<span class="function">mcrypt\_module\_open</span> 返回加密描述符。
