安装／配置
==========

**目录**

-   [需求](/v8js/setup.html#需求)
-   [安装](/v8js/setup.html#安装)
-   [运行时配置](/v8js/setup.html#运行时配置)
-   [资源类型](/v8js/setup.html#资源类型)

需求
----

PHP 5.3.3+ and V8 library and headers installed in proper paths.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/v8js" class="link external">» https://pecl.php.net/package/v8js</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                    | 默认 | 可修改范围    | 更新日志 |
|-------------------------------------------------------------------------|------|---------------|----------|
| <a href="/v8js/setup.html#" class="link">v8js.max_disposed_contexts</a> | 25   | PHP\_INI\_ALL |          |
| <a href="/v8js/setup.html#" class="link">v8js.flags</a>                 |      | PHP\_INI\_ALL |          |

这是配置指令的简短说明。

`v8js.max_disposed_contexts` <span class="type">int</span>  
Sets limit for disposed contexts before forcing V8 to do garbage
collection.

`v8js.flags` <span class="type">string</span>  
Sets V8 command line flags. The list of available flags can be obtained
in CLI mode by setting this parameter to *--help*. Example:

    $ php -r 'ini_set("v8js.flags", "--help"); new V8Js;' | less

> **Note**:
>
> For these flags to be effective in runtime the ini\_set() call has to
> be done before any V8Js objects are instantiated!

资源类型
--------

此扩展没有定义资源类型。
