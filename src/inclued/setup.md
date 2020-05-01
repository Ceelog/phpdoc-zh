安装／配置
==========

**目录**

-   [需求](/inclued/setup.html#需求)
-   [安装](/inclued/setup.html#安装)
-   [运行时配置](/inclued/setup.html#运行时配置)
-   [资源类型](/inclued/setup.html#资源类型)

需求
----

PHP version 5.1.0 or greater.

The included `gengraph.php` file utilizes the
<a href="http://www.graphviz.org/" class="link external">» graphviz</a>
library, however, this is not required.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/inclued" class="link external">» https://pecl.php.net/package/inclued</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                            | 默认       | 可修改范围       | 更新日志 |
|-----------------------------------------------------------------|------------|------------------|----------|
| <a href="/inclued/setup.html#" class="link">inclued.enabled</a> | Off        | PHP\_INI\_SYSTEM |          |
| <a href="/inclued/setup.html#" class="link">inclued.dumpdir</a> | **`NULL`** | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`inclued.enabled` <span class="type">bool</span>  
Whether or not to enable inclued.

`inclued.dumpdir` <span class="type">string</span>  
Location (path) to the directory that stores inclued files. If set, each
PHP request will create a file. These files are serialized versions of
what <span class="function">inclued\_get\_data</span> would produce, so
may be unserialized with <span class="function">unserialize</span>.

**Caution**
Because every request creates a file, this directory may fill up fast!

资源类型
--------

此扩展没有定义资源类型。
