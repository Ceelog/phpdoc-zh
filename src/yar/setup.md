安装／配置
==========

**目录**

-   [需求](/yar/setup.html#需求)
-   [安装](/yar/setup.html#安装)
-   [运行时配置](/yar/setup.html#运行时配置)
-   [资源类型](/yar/setup.html#资源类型)

需求
----

如果需要使用Msgpack作为打包协议,
则需要在configure的时候加上--enable-msgpack,
并且要保证Msgpack扩展也安装到PHP内.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/yar" class="link external">» https://pecl.php.net/package/yar</a>.

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                            | 默认 | 可修改范围       | 更新日志 |
|-----------------------------------------------------------------|------|------------------|----------|
| <a href="/yar/setup.html#" class="link">yar.packager</a>        | php  | PHP\_INI\_SYSTEM |          |
| <a href="/yar/setup.html#" class="link">yar.debug</a>           | Off  | PHP\_INI\_ALL    |          |
| <a href="/yar/setup.html#" class="link">yar.connect_timeout</a> | 1000 | PHP\_INI\_ALL    |          |
| <a href="/yar/setup.html#" class="link">yar.timeout</a>         | 5000 | PHP\_INI\_ALL    |          |
| <a href="/yar/setup.html#" class="link">yar.expose_info</a>     | On   | PHP\_INI\_SYS    |          |

这是配置指令的简短说明。

`yar.packager` <span class="type">string</span>  
设置Yar的打包工具, 可以是PHP(serialize), JSON,
Msgpack(这个需要编译的时候指定--enable-msgpack).

`yar.debug` <span class="type">string</span>  
打开的时候, Yar会把请求过程的日志都打印出来(到stderr).

`yar.connect_timeout` <span class="type">integer</span>  
连接超时(毫秒为单位)

`yar.timeout` <span class="type">integer</span>  
处理超时(毫秒为单位)

`yar.expose_info` <span class="type">bool</span>  
如果关闭, 则当通过浏览器访问Server的时候, 不会出现Server Info信息.

资源类型
--------
