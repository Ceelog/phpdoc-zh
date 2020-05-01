安装／配置
==========

**目录**

-   [需求](/tidy/setup.html#需求)
-   [安装](/tidy/setup.html#安装)
-   [运行时配置](/tidy/setup.html#运行时配置)
-   [资源类型](/tidy/setup.html#资源类型)

需求
----

To use Tidy, you will need libtidy installed, available on the
<a href="http://tidy.sourceforge.net/" class="link external">» tidy homepage</a>.
As of PHP 7.1.0, the HTML5 aware successor
<a href="http://www.html-tidy.org/" class="link external">» libtidy5</a>
can be used alternatively. As of PHP 7.3.0, another option is to use
<a href="https://github.com/petdance/tidyp" class="link external">» libtidyp</a>.

安装
----

This extension is bundled with PHP 5 and greater, and is installed using
the **--with-tidy** configure option.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                             | 默认 | 可修改范围       | 更新日志                            |
|------------------------------------------------------------------|------|------------------|-------------------------------------|
| <a href="/tidy/setup.html#" class="link">tidy.default_config</a> | ""   | PHP\_INI\_SYSTEM |                                     |
| <a href="/tidy/setup.html#" class="link">tidy.clean_output</a>   | "0"  | PHP\_INI\_USER   | PHP\_INI\_PERDIR prior to PHP 5.4.0 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`tidy.default_config` <span class="type">string</span>  
Default path for tidy config file.

`tidy.clean_output` <span class="type">boolean</span>  
Turns on/off the output repairing by Tidy.

**Warning**
Do not turn on *tidy.clean\_output* if you are generating non-html
content such as dynamic images.

资源类型
--------

此扩展没有定义资源类型。
