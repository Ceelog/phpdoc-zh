安装／配置
==========

**目录**

-   [需求](/stomp/setup.html#需求)
-   [安装](/stomp/setup.html#安装)
-   [运行时配置](/stomp/setup.html#运行时配置)
-   [资源类型](/stomp/setup.html#资源类型)

需求
----

PECL/stomp requires PHP 5.2.2 or newer.

The
<a href="http://www.openssl.org/" class="link external">» OpenSSL</a>
package \>= 0.9.6 and the
<a href="/book/openssl.html" class="link">openssl</a> extension may also
be required to use stomp over SSL.

安装
----

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/stomp" class="link external">» https://pecl.php.net/package/stomp</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                                | 默认                  | 可修改范围    | 更新日志 |
|-------------------------------------------------------------------------------------|-----------------------|---------------|----------|
| <a href="/stomp/setup.html#" class="link">stomp.default_broker</a>                  | tcp://localhost:61613 | PHP\_INI\_ALL |          |
| <a href="/stomp/setup.html#" class="link">stomp.default_connection_timeout_sec</a>  | 2                     | PHP\_INI\_ALL |          |
| <a href="/stomp/setup.html#" class="link">stomp.default_connection_timeout_usec</a> | 0                     | PHP\_INI\_ALL |          |
| <a href="/stomp/setup.html#" class="link">stomp.default_read_timeout_sec</a>        | 2                     | PHP\_INI\_ALL |          |
| <a href="/stomp/setup.html#" class="link">stomp.default_read_timeout_usec</a>       | 0                     | PHP\_INI\_ALL |          |

这是配置指令的简短说明。

`stomp.default_broker` <span class="type">string</span>  
The default broker URI to use when connecting to the message broker if
no other URI is specified.

`stomp.default_connection_timeout_sec` <span class="type">int</span>  
The seconds part of the default connection timeout.

`stomp.default_connection_timeout_usec` <span class="type">int</span>  
The microseconds part of the default connection timeout.

`stomp.default_read_timeout_sec` <span class="type">int</span>  
The seconds part of the default reading timeout.

`stomp.default_read_timeout_usec` <span class="type">int</span>  
The microseconds part of the default reading timeout.

资源类型
--------

There is only one resource type used in the stomp extension - it's the
link identifier for a stomp connection.
