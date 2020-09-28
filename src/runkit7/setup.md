安装／配置
==========

**目录**

-   [需求](/runkit7/setup.html#需求)
-   [安装](/runkit7/setup.html#安装)
-   [运行时配置](/runkit7/setup.html#运行时配置)
-   [资源类型](/runkit7/setup.html#资源类型)

需求
----

*Modifying Constants, Functions, Classes, and Methods* as well as
*Custom Superglobals* works with all releases of PHP 7. No special
requirements are necessary.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/runkit7" class="link external">» https://pecl.php.net/package/runkit7</a>.

此扩展在 Windows 平台的二进制扩展 (DLL 文件) PECL 可以在 PECL
官方网站上下载。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                     | 默认 | 可修改范围       | 更新日志 |
|--------------------------------------------------------------------------|------|------------------|----------|
| <a href="/runkit7/setup.html#" class="link">runkit.superglobal</a>       | ""   | PHP\_INI\_PERDIR |          |
| <a href="/runkit7/setup.html#" class="link">runkit.internal_override</a> | "0"  | PHP\_INI\_SYSTEM |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`runkit.superglobal` <span class="type">string</span>  
<span class="simpara"> Comma-separated list of variable names to be
treated as superglobals. This value should be set in the systemwide
php.ini file, but may work in perdir configuration contexts depending on
your SAPI. </span>

**示例 \#1 Custom Superglobals with runkit.superglobal=\_FOO,\_BAR in
php.ini**

``` php
<?php
function show_values() {
  echo "Foo is $_FOO\n";
  echo "Bar is $_BAR\n";
  echo "Baz is $_BAZ\n";
}

$_FOO = 'foo';
$_BAR = 'bar';
$_BAZ = 'baz';

/* Displays foo and bar, but not baz */
show_values();
?>
```

`runkit.internal_override` <span class="type">boolean</span>  
<span class="simpara"> Enables ability to modify/rename/remove internal
functions. </span>

资源类型
--------

此扩展没有定义资源类型。
