关闭魔术引号
------------

<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
指令只能在系统级关闭，不能在运行时。也就是说不能用 <span
class="function">ini\_set</span>。

**示例 \#1 在服务器端关闭魔术引号**

下面是一个通过 `php.ini` 文件把这些选项设为 *Off*
的范例。更多信息请参见本手册的<a href="/configuration/changes.html" class="link">怎样修改配置设定</a>。

    ; Magic quotes
    ;

    ; Magic quotes for incoming GET/POST/Cookie data.
    magic_quotes_gpc = Off

    ; Magic quotes for runtime-generated data, e.g. data from SQL, from exec(), etc.
    magic_quotes_runtime = Off

    ; Use Sybase-style magic quotes (escape ' with '' instead of \').
    magic_quotes_sybase = Off

如果不能修改服务器端的配置文件，使用 `.htaccess` 也可以。范例如下：

    php_flag magic_quotes_gpc Off

为了能写出移植性较强的代码（可以运行于任何环境），例如不能修改服务器配置的情况，下面的例子可以在运行时关闭
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>。但是这样做比较低效，适当的修改配置才是更好的办法。

**示例 \#2 在运行时关闭魔术引号**

``` php
<?php
if (get_magic_quotes_gpc()) {
    function stripslashes_deep($value)
    {
        $value = is_array($value) ?
                    array_map('stripslashes_deep', $value) :
                    stripslashes($value);

        return $value;
    }

    $_POST = array_map('stripslashes_deep', $_POST);
    $_GET = array_map('stripslashes_deep', $_GET);
    $_COOKIE = array_map('stripslashes_deep', $_COOKIE);
    $_REQUEST = array_map('stripslashes_deep', $_REQUEST);
}
?>
```
