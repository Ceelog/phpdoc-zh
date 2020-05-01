情形二：使用 --enable-force-cgi-redirect 选项
---------------------------------------------

此编译选项可以防止任何人通过如
`http://my.host/cgi-bin/php/secretdir/script.php` 这样的 URL 直接调用
PHP。PHP 在此模式下只会解析已经通过了 web 服务器的重定向规则的 URL。

通常 Apache 中的重定向设置可以通过以下指令完成：

``` apache-conf
Action php-script /cgi-bin/php
AddHandler php-script .php
```

此选项只在 Apache 下进行过测试，并且要依赖于 Apache
在重定向操作中所设置的非标准 CGI 环境变量 `REDIRECT_STATUS`。如果 web
服务器不支持任何方式能够判断请求是直接的还是重定向的，就不能使用这个选项，而应该用其它方法。请看下一节。
