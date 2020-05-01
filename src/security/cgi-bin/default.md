情形一：只运行公开的文件
------------------------

如果 web 服务器中所有内容都受到密码或 IP
地址的访问限制，就不需要设置这些选项。如果 web 服务器不支持重定向，或者
web 服务器不能和 PHP 通信而使访问请求变得更为安全，可以在 configure
脚本中指定
<a href="/configure/about.html#configure.enable-force-cgi-redirect" class="link">--enable-force-cgi-redirect</a>
选项。除此之外，还要确认 PHP 程序不依赖其它方式调用，比如通过直接的
`http://my.host/cgi-bin/php/dir/script.php` 访问或通过重定向访问
`http://my.host/dir/script.php`。

在Apache中，重定向可以使用 AddHandler 和 Action 语句来设置，请看下一节。
