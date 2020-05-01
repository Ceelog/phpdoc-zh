`php.ini` 配置段列表
--------------------

This list includes the `php.ini` sections you can set to configure your
PHP setup on a per Host or Path basis. These sections are optional.

These sections don't directly affect PHP. They are used to group other
`php.ini` directives together and to get them to act upon a particular
host or on a particular path.

These sections are used only in CGI/FastCGI mode and they can not set
<a href="/ini/core.html#ini.extension" class="link">extension</a> and
<a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>
directives.

| 名字                                                               | 可修改范围       | 更新日志              |
|--------------------------------------------------------------------|------------------|-----------------------|
| <a href="/ini/sections.html#ini.per-host" class="link">[HOST=]</a> | PHP\_INI\_SYSTEM | 在 PHP 5.3.0 时增加。 |
| <a href="/ini/sections.html#ini.per-path" class="link">[PATH=]</a> | PHP\_INI\_SYSTEM | 在 PHP 5.3.0 时增加。 |

这是配置指令的简短说明。

`[HOST=<host>]`  
This section allows you to define a set of `php.ini` directives that
will take effect on the named host.

**示例 \#1 Activate full on-screen error reporting for dev. domain**

``` php.ini
[HOST=dev.site.com]
error_reporting = E_ALL
display_errors = On
```

`[PATH=<path>]`  
This section allows you to define a set of `php.ini` directives that
will take effect when a script runs from the named path.

**示例 \#2 Add security script for protected areas**

``` php.ini
[PATH=/home/site/public/secure]
auto_prepend_file=security.php
```
