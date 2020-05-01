安装／配置
==========

**目录**

-   [需求](/xhprof/setup.html#需求)
-   [安装](/xhprof/setup.html#安装)
-   [运行时配置](/xhprof/setup.html#运行时配置)
-   [资源类型](/xhprof/setup.html#资源类型)

需求
----

虽然不是必需的，xhprof 包含了一个用 PHP 写的用户界面。
它是一个用来保存分析后的数据、并用浏览器显示的实用办法。 因此一个启用了
PHP 的 web 服务器将使人更能体验到 xhprof 的用处。

在
<a href="http://github.com/preinheimer/xhprof" class="link external">» http://github.com/preinheimer/xhprof</a>
也有一个 GUI 的分支。

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/xhprof" class="link external">» https://pecl.php.net/package/xhprof</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                             | 默认 | 可修改范围        | 更新日志 |
|------------------------------------------------------------------|------|-------------------|----------|
| <a href="/xhprof/setup.html#" class="link">xhprof.output_dir</a> | ""   | **`PHP_INI_ALL`** |          |

这是配置指令的简短说明。

`xhprof.output_dir` <span class="type">string</span>  
储存 XHProf 运行数据的默认目录，用于接口 iXHProfRuns(即
XHProfRuns\_Default 类)。

资源类型
--------

此扩展没有定义资源类型。
