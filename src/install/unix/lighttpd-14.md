Unix 平台的 Lighttpd 1.4
------------------------

本节包括在 Unix 平台的 Lighttpd 1.4 下安装 PHP 的说明和提示。

推荐阅读
<a href="http://trac.lighttpd.net/trac/" class="link external">» Lighttpd trac</a>
了解一下正确安装 Lighttpd 然后继续。

推荐使用 Fastcgi 作为 SAPI 模块来连接 PHP 和 Lighttpd。在 PHP 5.3
中自动激活了 Fastcgi，对于旧版本则在配置时使用 --enable-fastcgi。要确认
PHP 已激活 Fastcgi 可以使用命令 *php -v*，应该显示 *PHP 5.2.5
(cgi-fcgi)*。在 PHP 5.2.3 之前，Fastcgi 是包含在 php 可执行文件中（没有
php-cgi 文件）。

### 使 Lighttpd 产生 php 进程

要配置 Lighttpd 连接到 php 并产生 fastcgi 进程，编辑
lighttpd.conf。推荐使用套接字在本机连接 fastcgi 进程。

**示例 \#1 Partial lighttpd.conf**

    server.modules += ( "mod_fastcgi" )

    fastcgi.server = ( ".php" =>
      ((
        "socket" => "/tmp/php.socket",
        "bin-path" => "/usr/local/bin/php-cgi",
        "bin-environment" => (
          "PHP_FCGI_CHILDREN" => "16",
          "PHP_FCGI_MAX_REQUESTS" => "10000"
        ),
        "min-procs" => 1,
        "max-procs" => 1,
        "idle-timeout" => 20
      ))
    )

bin-path 指令允许 lighttpd 动态产生 fastcgi 进程。PHP 会根据
PHP\_FCGI\_CHILDREN
环境变量产生子进程。“bin-environment”指令设定了所产生的进行的环境。PHP
会在达到 PHP\_FCGI\_MAX\_REQUESTS 所指定的请求数目之后杀死一个子进程。在
PHP 中通常应避免“min-procs”和“max-procs”指令。PHP
自己管理其子进程，并且例如 APC 之类的 opcode 缓存仅在 PHP
管理下的子进程之间共享。如果“min-procs”被设定成某个大于 1 的值，则 PHP
应答器的总数目为该值乘以 PHP\_FCGI\_CHILDREN（如 min-procs 为
2，PHP\_FCGI\_CHILDREN 为 16 则会产生 32 个应答器）。

### 通过 spawn-fcgi 产生进程

Lighttpd 提供一个名为 spawn-fcgi 的程序来简化产生 fastcgi 进程的手续。

### 产生 php-cgi

有可能不通过 spawn-fcgi 来产生进程，但需要做些工作。设定
PHP\_FCGI\_CHILDREN 环境变量控制了 PHP 产生多少个子进程来处理请求。设定
PHP\_FCGI\_MAX\_REQUESTS
将决定每个子进程存活多久（以请求数目决定）。以下为一个简单的 bash
脚本来帮助产生 php 应答器。

**示例 \#2 产生 FastCGI 应答器**

    #!/bin/sh

    # Location of the php-cgi binary
    PHP=/usr/local/bin/php-cgi

    # PID File location
    PHP_PID=/tmp/php.pid

    # Binding to an address
    #FCGI_BIND_ADDRESS=10.0.1.1:10000
    # Binding to a domain socket
    FCGI_BIND_ADDRESS=/tmp/php.sock

    PHP_FCGI_CHILDREN=16
    PHP_FCGI_MAX_REQUESTS=10000

    env -i PHP_FCGI_CHILDREN=$PHP_FCGI_CHILDREN \
           PHP_FCGI_MAX_REQUESTS=$PHP_FCGI_MAX_REQUESTS \
           $PHP -b $FCGI_BIND_ADDRESS &

    echo $! > "$PHP_PID"

### 连接远程 FCGI 实例

Fastcgi 实例可被产生于多个远程机器以分散应用程序。

**示例 \#3 连接远程 php-fastcgi 实例**

    fastcgi.server = ( ".php" =>
       (( "host" => "10.0.0.2", "port" => 1030 ),
        ( "host" => "10.0.0.3", "port" => 1030 ))
    )
