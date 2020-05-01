安装／配置
==========

**目录**

-   [需求](/swoole/setup.html#需求)
-   [安装](/swoole/setup.html#安装)
-   [运行时配置](/swoole/setup.html#运行时配置)
-   [资源类型](/swoole/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

Use **--with-swoole\[=DIR\]** when compiling PHP.

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/swoole" class="link external">» https://pecl.php.net/package/swoole</a>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                       | 默认    | 可修改范围       | 更新日志 |
|----------------------------------------------------------------------------|---------|------------------|----------|
| <a href="/swoole/setup.html#" class="link">swoole.aio_thread_num</a>       | 2       | PHP\_INI\_ALL    |          |
| <a href="/swoole/setup.html#" class="link">swoole.display_errors</a>       | On      | PHP\_INI\_ALL    |          |
| <a href="/swoole/setup.html#" class="link">swoole.fast_serialize</a>       | Off     | PHP\_INI\_ALL    |          |
| <a href="/swoole/setup.html#" class="link">swoole.unixsock_buffer_size</a> | 8388608 | PHP\_INI\_ALL    |          |
| <a href="/swoole/setup.html#" class="link">swoole.use_namespace</a>        | On      | PHP\_INI\_SYSTEM |          |

这是配置指令的简短说明。

`swoole.aio_thread_num` <span class="type">integer</span>  
POSIX asynchronous I/O thread number

`swoole.display_errors` <span class="type">string</span>  
This determines whether Swoole errors should be printed to the screen.

`swoole.fast_serialize` <span class="type">string</span>  
Whether to enable Swoole fast\_serialize.

`swoole.unixsock_buffer_size` <span class="type">integer</span>  
Buffer size of Unix socket.

`swoole.use_namespace` <span class="type">string</span>  
Whether to use PHP namespaces

资源类型
--------

此扩展没有定义资源类型。
