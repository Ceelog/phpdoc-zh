配置可被设定范围
----------------

这些模式决定着一个 PHP
的指令在何时何地，是否能够被设定。手册中的每个指令都有其所属的模式。例如有些指令可以在
PHP 脚本中用 <span class="function">ini\_set</span>
来设定，而有些则只能在 `php.ini` 或 `httpd.conf` 中。

例如 <a href="/outcontrol/setup.html#" class="link">output_buffering</a>
指令是属于 *PHP\_INI\_PERDIR*，因而就不能用 <span
class="function">ini\_set</span> 来设定。但是
<a href="/errorfunc/setup.html#" class="link">display_errors</a>
指令是属于 *PHP\_INI\_ALL* 因而就可以在任何地方被设定，包括 <span
class="function">ini\_set</span>。

| 模式               | 含义                                                                                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PHP\_INI\_USER*   | 可在用户脚本（例如 <span class="function">ini\_set</span>）或 <a href="/configuration/changes.html#configuration.changes.windows" class="link">Windows 注册表</a>（自 PHP 5.3 起）以及 `.user.ini` 中设定 |
| *PHP\_INI\_PERDIR* | 可在 `php.ini`，`.htaccess` 或 `httpd.conf` 中设定                                                                                                                                                        |
| *PHP\_INI\_SYSTEM* | 可在 `php.ini` 或 `httpd.conf` 中设定                                                                                                                                                                     |
| *PHP\_INI\_ALL*    | 可在任何地方设定                                                                                                                                                                                          |
