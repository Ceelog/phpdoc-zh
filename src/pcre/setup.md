安装／配置
==========

**目录**

-   [需求](/pcre/setup.html#需求)
-   [安装](/pcre/setup.html#安装)
-   [运行时配置](/pcre/setup.html#运行时配置)
-   [资源类型](/pcre/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

PCRE 是 PHP 核心扩展，所以总是启用的。 默认情况下，该扩展使用内置的 PCRE
library。或者，也可以通过指定 configure 选项 **--with-pcre-regex=DIR**
设置外部 PCRE library 目录，*DIR* 是 PCRE 的 include 和 library
文件位置。 PHP 5.6/7.0 推荐使用 PCRE 8.10 或更高版本。

PHP 7.0.0 起 PCRE 默认支持 JIT（just-in-time）编译技术，PHP 7.0.12
起可以通过 **--without-pcre-jit** 禁用 PCRE 的 JIT 功能。

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

> **Note**:
>
> PHP 5.3.0 的之前版本，可通过 **--without-pcre-regex**
> 配置选项禁用此扩展。

PCRE 是一个活跃的项目，作为它的一个演变，PHP功能依赖于它。 php
文档的某些部分 可能会过期, 因为它可能不包括 PCRE 提供的一些新功能.
关于修正的清单，请查阅
<a href="http://www.pcre.org/original/changelog.txt" class="link external">» PCRE library changelog</a>，
下面是绑定的 PCRE 库的历史记录：

| PHP 版本                        | Updated PCRE 版本 | Notes                                                                                                                              |
|---------------------------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------|
| 7.0.3 / 5.6.18 / 5.5.32         | 8.38              | 参见 CVE-2015-8383、 CVE-2015-8386、 CVE-2015-8387、 CVE-2015-8389、 CVE-2015-8390、 CVE-2015-8391、 CVE-2015-8393、 CVE-2015-8394 |
| 7.0.0 / 5.6.9 / 5.5.26 / 5.4.41 | 8.37              | See CVE-2015-2325, CVE-2015-2326                                                                                                   |
| 5.6.0 / 5.5.10                  | 8.34              |                                                                                                                                    |
| 5.5.0 / 5.4.14 / 5.3.24         | 8.32              |                                                                                                                                    |
| 5.4.9 / 5.3.19                  | 8.31              |                                                                                                                                    |
| 5.3.7                           | 8.12              |                                                                                                                                    |
| 5.3.6                           | 8.11              |                                                                                                                                    |
| 5.3.4                           | 8.10              |                                                                                                                                    |
| 5.3.3 / 5.2.14                  | 8.02              |                                                                                                                                    |
| 5.3.2                           | 8.00              |                                                                                                                                    |
| 5.3.0 / 5.2.13                  | 7.9               |                                                                                                                                    |
| 5.2.7                           | 7.8               |                                                                                                                                    |
| 5.2.6                           | 7.6               |                                                                                                                                    |
| 5.2.5                           | 7.3               |                                                                                                                                    |
| 5.2.4                           | 7.2               |                                                                                                                                    |
| 5.2.2                           | 7.0               |                                                                                                                                    |
| 5.2.0                           | 6.7               |                                                                                                                                    |
| 5.1.3                           | 6.6               |                                                                                                                                    |
| 5.1.0                           | 6.2               |                                                                                                                                    |
| 5.0.5                           | 5.0               |                                                                                                                                    |
| 5.0.0                           | 4.5               |                                                                                                                                    |
| 4.4.7                           | 7.7               |                                                                                                                                    |

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                              | 默认     | 可修改范围    | 更新日志           |
|-------------------------------------------------------------------|----------|---------------|--------------------|
| <a href="/pcre/setup.html#" class="link">pcre.backtrack_limit</a> | "100000" | PHP\_INI\_ALL | php 5.2.0 起可用。 |
| <a href="/pcre/setup.html#" class="link">pcre.recursion_limit</a> | "100000" | PHP\_INI\_ALL | php 5.2.0 起可用。 |
| <a href="/pcre/setup.html#" class="link">pcre.jit</a>             | "1"      | PHP\_INI\_ALL | PHP 7.0.0 起可用   |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`pcre.backtrack_limit` <span class="type">integer</span>  
PCRE的回溯限制.

`pcre.recursion_limit` <span class="type">integer</span>  
PCRE的递归限制. 请注意, 如果 讲这个值设置为一个很大的数字,
你可能会消耗掉 所有的进程可用堆栈,
最终导致php崩溃(直到达到系统限制的堆栈大小).

`pcre.jit` <span class="type">boolean</span>  
是否使用 PCRE 的 JIT 编译.

资源类型
--------

此扩展没有定义资源类型。
