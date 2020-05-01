安装／配置
==========

**目录**

-   [需求](/yaf/setup.html#需求)
-   [安装](/yaf/setup.html#安装)
-   [运行时配置](/yaf/setup.html#运行时配置)
-   [资源类型](/yaf/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/yaf" class="link external">» https://pecl.php.net/package/yaf</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                             | 默认    | 可修改范围                 | 更新日志 |
|------------------------------------------------------------------|---------|----------------------------|----------|
| <a href="/yaf/setup.html#" class="link">yaf.library</a>          |         | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.action_prefer</a>    | 0       | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.lowcase_path</a>     | 0       | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.use_spl_autoload</a> | 0       | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.forward_limit</a>    | 5       | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.name_suffix</a>      | 1       | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.name_separator</a>   |         | its PHP\_INI\_ALL value    |          |
| <a href="/yaf/setup.html#" class="link">yaf.cache_config</a>     | 0       | its PHP\_INI\_SYSTEM value |          |
| <a href="/yaf/setup.html#" class="link">yaf.environ</a>          | product | its PHP\_INI\_SYSTEM value |          |
| <a href="/yaf/setup.html#" class="link">yaf.use_namespace</a>    | 0       | its PHP\_INI\_SYSTEM value |          |

这是配置指令的简短说明。

`yaf.library` <span class="type">string</span>  
The global library path, Yaf\_loader will search global library in this
directory.

`yaf.action_prefer` <span class="type">integer</span>  
If there is only one part in PATH\_INFO, should it consider as a
controller or action.

If this configure On, it will be considered as a Action name.

`yaf.lowcase_path` <span class="type">integer</span>  
Whether lowercase all the path during the class autoloading.

`yaf.use_spl_autoload` <span class="type">integer</span>  
When this value is On, if <span class="classname">Yaf\_Loader</span> can
not find a class, it will return FALSE, then give chance to other auto
load function to be called.

When this value is Off(default), <span
class="methodname">Yaf\_Loader::autoload</span> will always return TRUE.

`yaf.forward_limit` <span class="type">integer</span>  
The max forward count, default is 5. that means you can have a max value
of 5 in the forward stack.

This is a protection for prevent recursive <span
class="methodname">Yaf\_Controller\_Abstract::forward</span>.

`yaf.name_suffix` <span class="type">integer</span>  
When this On, Yaf\_Loader will identify a class by it's suffix to decide
whether it is a MVC Class.

When this Off, Yaf\_Loader will look at the prefix of the class name.

`yaf.name_separator` <span class="type">string</span>  
When this is not empty, Yaf\_Loader will identify the class suffix and
string value of this.

For example, when this value is "\_", Yaf\_Loader will take
Index\_Controller as a Controller Class, IndexController as a normal
class.

`yaf.cache_config` <span class="type">integer</span>  
If this is On, and in the meantime you are using ini config file as the
parameter of <span class="methodname">Yaf\_Application</span>, the
compiling result of the ini config file will be cached in the PHP
process.

> **Note**:
>
> Yaf examine the mtime of the ini file, if it was changed since last
> compiling, Yaf will reload it.

**Warning**
Yaf use the ini file path as the cache entry key, so do use the absolute
path in ini file path, otherwise there might be some conflicts if two
application use the same relative path of ini config.

`yaf.environ` <span class="type">string</span>  
This value is "product" by default, used for Yaf to fetch the config
section of a ini config file.

That is, if this value is "product", Yaf will use the section named
"product" in the ini config file(the first parameter of the <span
class="classname">Yaf\_Application</span>) as the final config of the
<span class="classname">Yaf\_Application</span>.

`yaf.use_namespace` <span class="type">integer</span>  
Only works as of PHP 5.3, if this value is On, All class of Yaf will
named in namespace style.

For example, Yaf\_Route\_Rewrite =\> \\Yaf\\Route\\Rewrite,
Yaf\_Controller\_Abstract =\> \\Yaf\\Controller\_Abstract (Abstract is
the keyword, can not used as a class name)

资源类型
--------

此扩展没有定义资源类型。
