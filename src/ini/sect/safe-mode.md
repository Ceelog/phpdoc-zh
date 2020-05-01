保安措施和安全模式
------------------

| 名字                                                                                                              | 默认                | 可修改范围       | 更新日志                                   |
|-------------------------------------------------------------------------------------------------------------------|---------------------|------------------|--------------------------------------------|
| <a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>                                       | "0"                 | PHP\_INI\_SYSTEM |                                            |
| <a href="/ini/sect/safe-mode.html#ini.safe-mode-gid" class="link">safe_mode_gid</a>                               | "0"                 | PHP\_INI\_SYSTEM | 自 PHP 4.1.0 起可用，在 PHP 5.4.0 中移除。 |
| <a href="/ini/sect/safe-mode.html#ini.safe-mode-include-dir" class="link">safe_mode_include_dir</a>               | NULL                | PHP\_INI\_SYSTEM | 自 PHP 4.1.0 起可用                        |
| <a href="/ini/sect/safe-mode.html#ini.safe-mode-exec-dir" class="link">safe_mode_exec_dir</a>                     | ""                  | PHP\_INI\_SYSTEM |                                            |
| <a href="/ini/sect/safe-mode.html#ini.safe-mode-allowed-env-vars" class="link">safe_mode_allowed_env_vars</a>     | "PHP\_"             | PHP\_INI\_SYSTEM |                                            |
| <a href="/ini/sect/safe-mode.html#ini.safe-mode-protected-env-vars" class="link">safe_mode_protected_env_vars</a> | "LD\_LIBRARY\_PATH" | PHP\_INI\_SYSTEM |                                            |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`safe_mode` <span class="type">boolean</span>  
是否启用 PHP 的安全模式。

`safe_mode_gid` <span class="type">boolean</span>  
默认情况下，安全模式在打开文件时会做 UID 比较检查。如果想将其放宽到 GID
比较，则打开 safe\_mode\_gid。是否在文件访问时使用
*UID*（**`FALSE`**）或者 *GID*（**`TRUE`**）来做检查。

`safe_mode_include_dir` <span class="type">string</span>  
当从此目录及其子目录（目录必须在
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
中或者用完整路径来包含）包含文件时越过 *UID*/*GID* 检查。

<span class="simpara"> 从 PHP 4.2.0 开始，本指令可以接受和
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
指令类似的风格用冒号（Windows 中是分号）隔开的路径，而不只是一个目录。
</span> <span class="simpara">
指定的限制实际上是一个前缀，而非一个目录名。这也就是说“safe\_mode\_include\_dir
=
/dir/incl”将允许访问“/dir/include”和“/dir/incls”，如果它们存在的话。如果希望将访问控制在一个指定的目录，那么请在结尾加上一个斜线，例如：“safe\_mode\_include\_dir
= /dir/incl/”。 </span> <span class="simpara"> 如果本指令的值为空，在
PHP 4.2.3 中以及 PHP 4.3.3 起具有不同 *UID*/*GID*
的文件将不能被包含。在较早版本中，所有文件都能被包含。 </span>

`safe_mode_exec_dir` <span class="type">string</span>  
如果 PHP 使用了安全模式，<span class="function">system</span>
和其它<a href="/ref/exec.html" class="link">程序执行函数</a>将拒绝启动不在此目录中的程序。必须使用
*/* 作为目录分隔符，包括 Windows 中。

`safe_mode_allowed_env_vars` <span class="type">string</span>  
设置某些环境变量可能是潜在的安全缺口。本指令包含有一个逗号分隔的前缀列表。在安全模式下，用户只能改变那些名字具有在这里提供的前缀的环境变量。默认情况下，用户只能设置以
PHP\_ 开头的环境变量（例如 PHP\_FOO = BAR）。

> **Note**:
>
> 如果本指令为空，PHP 将使用户可以修改任何环境变量！

`safe_mode_protected_env_vars` <span class="type">string</span>  
本指令包含有一个逗号分隔的环境变量的列表，最终用户不能用 <span
class="function">putenv</span> 来改变这些环境变量。甚至在
safe\_mode\_allowed\_env\_vars 中设置了允许修改时也不能改变这些变量。

参见
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>、
<a href="/ini/core.html#ini.disable-functions" class="link">disable_functions</a>、
<a href="/ini/core.html#ini.disable-classes" class="link">disable_classes</a>、
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>、
<a href="/errorfunc/setup.html#" class="link">display_errors</a> 和
<a href="/errorfunc/setup.html#" class="link">log_errors</a>。

当
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>
设置为 on，PHP
将通过文件函数或其目录检查当前脚本的拥有者是否和将被操作的文件的拥有者相匹配。例如：

``` ls
-rw-rw-r--    1 rasmus   rasmus       33 Jul  1 19:20 script.php
-rw-r--r--    1 root     root       1116 May 26 18:01 /etc/passwd
```

运行 `script.php`

``` php
<?php
 readfile('/etc/passwd');
?>
```

如果安全模式被激活，则将会导致以下错误：

    Warning: SAFE MODE Restriction in effect. The script whose uid is 500 is not
    allowed to access /etc/passwd owned by uid 0 in /docroot/script.php on line 2

同时，或许会存在这样的环境，在该环境下，宽松的 *GID*
检查已经足够，但严格的 *UID* 检查反而是不适合的。可以用
<a href="/ini/sect/safe-mode.html#ini.safe-mode-gid" class="link">safe_mode_gid</a>
选项来控制这种检查。如果设置为 *On* 则进行宽松的 *GID* 检查；设置为
*Off*（默认值）则进行 *UID* 检查。

除了
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>
以外，如果设置了
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
选项，则所有的文件操作将被限制在指定的目录下。例如：

``` ini
<Directory /docroot>
  php_admin_value open_basedir /docroot
</Directory>
```

如果在设置了
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
选项后运行同样的 `script.php`，则其结果会是：

    Warning: open_basedir restriction in effect. File is in wrong directory in
    /docroot/script.php on line 2

也可以单独地屏蔽某些函数。请注意
<a href="/ini/core.html#ini.disable-functions" class="link">disable_functions</a>
选项不能在 `php.ini` 文件外部使用，也就是说无法在 `httpd.conf`
文件的按不同虚拟主机或不同目录的方式来屏蔽函数。如果将如下内容加入到
`php.ini` 文件：

``` ini
disable_functions readfile,system
```

则会得到如下的输出：

    Warning: readfile() has been disabled for security reasons in
    /docroot/script.php on line 2

**Warning**

当然，这些 PHP 限制不适用于可执行文件。
