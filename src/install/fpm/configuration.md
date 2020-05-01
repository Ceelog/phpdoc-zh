配置
----

FPM 使用类似 `php.ini` 语法的 `php-fpm.conf` 和进程池配置文件。

### `php-fpm.conf` 全局配置段

`pid` <span class="type">string</span>  
PID 文件的位置。默认为空。

`error_log` <span class="type">string</span>  
错误日志的位置。默认：*\#INSTALL\_PREFIX\#/log/php-fpm.log*。 如果设置为
"syslog"，日志将不会写入本地文件，而是发送到 syslogd。

`log_level` <span class="type">string</span>  
错误级别。可用级别为：alert（必须立即处理），error（错误情况），warning（警告情况），notice（一般重要信息），debug（调试信息）。默认：notice。

`syslog.facility` <span class="type">string</span>  
设置何种程序记录消息，默认值：daemon。

`syslog.ident` <span class="type">string</span>  
为每条信息添加前缀。 如果在同一台服务器上运行了多个 FPM
实例，可以修改此默认值来满足需求。默认值：php-fpm。

`emergency_restart_threshold` <span class="type">int</span>  
如果子进程在 *emergency\_restart\_interval*
设定的时间内收到该参数设定次数的 SIGSEGV 或者
SIGBUS退出信息号，则FPM会重新启动。0
表示“关闭该功能”。默认值：0（关闭）。

`emergency_restart_interval` <span class="type">mixed</span>  
*emergency\_restart\_interval*
用于设定平滑重启的间隔时间。这么做有助于解决加速器中共享内存的使用问题。可用单位：s（秒），m（分），h（小时）或者
d（天）。默认单位：s（秒）。默认值：0（关闭）。

`process_control_timeout` <span class="type">mixed</span>  
设置子进程接受主进程复用信号的超时时间。可用单位：s（秒），m（分），h（小时）或者
d（天）。默认单位：s（秒）。默认值：0（关闭）。

`process.max` <span class="type">int</span>  
Fork 的最大 FPM
进程数。使用动态管理进程数时，此设计可以控制在一个进程池内的全局进程数量。
使用需谨慎。默认值：0。

`process.priority` <span class="type">int</span>  
设置 master 进程的 nice(2) 优先级（如果设置了此值）。 可以是
-19（最高优先级）到 20 （更低优先级）。 默认值：不设置。

`daemonize` <span class="type">boolean</span>  
设置 FPM 在后台运行。设置“no”将 FPM
保持在前台运行用于调试。默认值：yes。

`rlimit_files` <span class="type">int</span>  
设置 master 进程的打开文件描述符 rlimit 数。

`rlimit_core` <span class="type">int</span>  
设置 master 进程最大 core 的 rlimit 尺寸。 默认值：0。

`events.mechanism` <span class="type">string</span>  
设置 FPM 使用的事件机制。 可用以下选项：select、pool、epoll、kqueue
(\*BSD)、port (Solaris)。 默认值：不设置（自动检测）

`systemd_interval` <span class="type">int</span>  
使用 systemd 集成的 FPM 时，设置间歇秒数，报告健在通知给 systemd。
设置为 0 表示禁用。默认值：10。

### 运行配置区段

在FPM中，可以使用不同的设置来运行多个进程池。
这些设置可以针对每个进程池单独设置。

`listen` <span class="type">string</span>  
设置接受 FastCGI
请求的地址。可用格式为：'ip:port'，'port'，'/path/to/unix/socket'。每个进程池都需要设置。

`listen.backlog` <span class="type">int</span>  
设置 listen(2) 的 backlog 最大值。“-1”表示无限制。默认值：-1。

`listen.allowed_clients` <span class="type">string</span>  
设置允许连接到 FastCGI 的服务器 IPV4 地址。等同于 PHP FastCGI (5.2.2+)
中的 FCGI\_WEB\_SERVER\_ADDRS 环境变量。仅对 TCP
监听起作用。每个地址是用逗号分隔，如果没有设置或者为空，则允许任何服务器请求连接。默认值：any。
PHP 5.5.20 和 5.6.4起，开始支持 IPv6 地址。

`listen.owner` <span class="type">string</span>  
如果使用了 Unix 套接字，表示它的权限。在 Linux
中必须设置读/写权限，以便用于 WEB 服务器连接。 在很多 BSD
派生的系统中可以忽略权限允许自由连接。
默认值：运行所使用的用户和组，权限为 0660。

`listen.group` <span class="type">string</span>  
参见 *listen.owner*。

`listen.mode` <span class="type">string</span>  
参见 *listen.owner*。

`listen.acl_users` <span class="type">string</span>  
当系统支持 POSIX ACL（Access Control Lists）时，可以设置使用此选项。
当设置了的时候，将会忽略 *listen.owner* 和 *listen.group*。
值是逗号分割的用户名列表。 PHP 5.6.5 起可用。

`listen.acl_groups` <span class="type">string</span>  
参见 *listen.acl\_users*。 值是逗号分割的用户组名称列表。 PHP 5.6.5
起可用。

`user` <span class="type">string</span>  
FPM 进程运行的Unix用户。必须设置。

`group` <span class="type">string</span>  
FPM 进程运行的 Unix 用户组。如果不设置，就使用默认用户的用户组。

`pm` <span class="type">string</span>  
设置进程管理器如何管理子进程。可用值：*static*，*ondemand*，*dynamic*。必须设置。

*static* - 子进程的数量是固定的（*pm.max\_children*）。

*ondemand* - 进程在有需求时才产生（当请求时才启动。与 dynamic
相反，在服务启动时 *pm.start\_servers* 就启动了。

*dynamic* -
子进程的数量在下面配置的基础上动态设置：*pm.max\_children*，*pm.start\_servers*，*pm.min\_spare\_servers*，*pm.max\_spare\_servers*。

`pm.max_children` <span class="type">int</span>  
*pm* 设置为 *static* 时表示创建的子进程的数量，*pm* 设置为 *dynamic*
时表示最大可创建的子进程的数量。必须设置。

该选项设置可以同时提供服务的请求数限制。类似 Apache 的 mpm\_prefork 中
MaxClients 的设置和 普通PHP FastCGI中的 `PHP_FCGI_CHILDREN` 环境变量。

`pm.start_servers` <span class="type">in</span>  
设置启动时创建的子进程数目。仅在 *pm* 设置为 *dynamic*
时使用。默认值：min\_spare\_servers + (max\_spare\_servers -
min\_spare\_servers) / 2。

`pm.min_spare_servers` <span class="type">int</span>  
设置空闲服务进程的最低数目。仅在 *pm* 设置为 *dynamic*
时使用。必须设置。

`pm.max_spare_servers` <span class="type">int</span>  
设置空闲服务进程的最大数目。仅在 *pm* 设置为 *dynamic*
时使用。必须设置。

`pm.process_idle_timeout` <span class="type">mixed</span>  
秒数，多久之后结束空闲进程。 仅当设置 *pm* 为 *ondemand*。
可用单位：s（秒），m（分），h（小时）或者 d（天）。默认单位：10s。

`pm.max_requests` <span class="type">int</span>  
设置每个子进程重生之前服务的请求数。对于可能存在内存泄漏的第三方模块来说是非常有用的。如果设置为
'0' 则一直接受请求，等同于 `PHP_FCGI_MAX_REQUESTS` 环境变量。默认值：0。

`pm.status_path` <span class="type">string</span>  
FPM 状态页面的网址。如果没有设置，则无法访问状态页面，默认值：无。

`ping.path` <span class="type">string</span>  
FPM 监控页面的 ping 网址。如果没有设置，则无法访问 ping
页面。该页面用于外部检测 FPM
是否存活并且可以响应请求。请注意必须以斜线开头（/）。

`ping.response` <span class="type">string</span>  
用于定义 ping 请求的返回响应。返回为 HTTP 200 的 text/plain
格式文本。默认值：pong。

`process.priority` <span class="type">int</span>  
设置 worker 的 nice(2)优先级（如果设置了的话）。 该值从
-19（最高优先级） 到 20（更低优先级）。 默认值：不设置

`prefix` <span class="type">string</span>  
检测路径时使用的前缀。

`request_terminate_timeout` <span class="type">mixed</span>  
设置单个请求的超时中止时间。该选项可能会对 php.ini 设置中的
'max\_execution\_time' 因为某些特殊原因没有中止运行的脚本有用。设置为
'0' 表示 'Off'。可用单位：s（秒），m（分），h（小时）或者
d（天）。默认单位：s（秒）。默认值：0（关闭）。

`request_slowlog_timeout` <span class="type">mixed</span>  
当一个请求该设置的超时时间后，就会将对应的 PHP
调用堆栈信息完整写入到慢日志中。设置为 '0' 表示
'Off'。可用单位：s（秒），m（分），h（小时）或者
d（天）。默认单位：s（秒）。默认值：0（关闭）。

`slowlog` <span class="type">string</span>  
慢请求的记录日志。默认值：*\#INSTALL\_PREFIX\#/log/php-fpm.log.slow*。

`rlimit_files` <span class="type">int</span>  
设置文件打开描述符的 rlimit 限制。默认值：系统定义值。

`rlimit_core` <span class="type">int</span>  
设置核心 rlimit 最大限制值。可用值：'unlimited'，0
或者正整数。默认值：系统定义值。

`chroot` <span class="type">string</span>  
启动时的 Chroot 目录。所定义的目录需要是绝对路径。如果没有设置，则
chroot 不被使用。

`chdir` <span class="type">string</span>  
设置启动目录，启动时会自动 Chdir
到该目录。所定义的目录需要是绝对路径。默认值：当前目录，或者根目录（chroot时）。

`catch_workers_output` <span class="type">boolean</span>  
重定向运行过程中的 stdout 和 stderr
到主要的错误日志文件中。如果没有设置，stdout 和 stderr 将会根据 FastCGI
的规则被重定向到 /dev/null。默认值：无。

`clear_env` <span class="type">boolean</span>  
为 FPM worker 进程清除环境变量。
在进程池配置文件里设置环境变量前，阻止任意系统的环境变量进入 FPM worker
进程。 自 PHP 5.4.27、 5.5.11 和 5.6.0 起。 默认值: Yes

`security.limit_extensions` <span class="type">string</span>  
限制 FPM 允许解析的脚本扩展名。 此设置可以预防 web 服务器配置的错误。
应当限制 FPM 仅仅解析 .php 扩展名，阻止恶意用户使用其他扩展名运行 php
代码。 默认值： .php .phar

`access.log` <span class="type">string</span>  
Access log 文件。 默认值：不设置

`access.format` <span class="type">string</span>  
access log 的格式。 默认值: "%R - %u %t \\"%m %r\\" %s"

还可以在为一个运行池传递附加的环境变量，或者更新 PHP
的配置值。可以在进程池配置文件中如下面的配置参数来做到：

**示例 \#1 给运行池传递环境变量和设置 PHP 的配置值**

``` ini
env[HOSTNAME] = $HOSTNAME
       env[PATH] = /usr/local/bin:/usr/bin:/bin
       env[TMP] = /tmp
       env[TMPDIR] = /tmp
       env[TEMP] = /tmp

       php_admin_value[sendmail_path] = /usr/sbin/sendmail -t -i -f www@my.domain.com
       php_flag[display_errors] = off
       php_admin_value[error_log] = /var/log/fpm-php.www.log
       php_admin_flag[log_errors] = on
       php_admin_value[memory_limit] = 32M
```

PHP配置值通过 *php\_value* 或者 *php\_flag*
设置，并且会覆盖以前的值。请注意
<a href="/ini/core.html#ini.disable-functions" class="link">disable_functions</a>
或者
<a href="/ini/core.html#ini.disable-classes" class="link">disable_classes</a>
在 `php.ini`
之中定义的值不会被覆盖掉，但是会将新的设置附加在原有值的后面。

使用 *php\_admin\_value* 或者 *php\_admin\_flag* 定义的值，不能被 PHP
代码中的 <span class="function">ini\_set</span> 覆盖。

自 5.3.3 起，也可以通过 web 服务器设置 PHP 的设定。

**示例 \#2 在 nginx.conf 中设定 PHP**

``` ini
set $php_value "pcre.backtrack_limit=424242";
set $php_value "$php_value \n pcre.recursion_limit=99999";
fastcgi_param  PHP_VALUE $php_value;

fastcgi_param  PHP_ADMIN_VALUE "open_basedir=/var/www/htdocs";
```

**Caution**

由于这些设定是以 FastCGI 标头传递给 php-fpm，php-fpm
不应绑定到外部网可以访问的地址上，否则任何人都能修改 PHP
的配置选项了。参见
<a href="/install/fpm/configuration.html#listen-allowed-clients" class="link">listen.allowed_clients</a>。
