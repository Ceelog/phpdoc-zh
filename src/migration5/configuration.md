移植配置文件
------------

由于 ISAPI 模块的名字改了，从 php4xxx 改为
php5xxx，因此需要对配置文件作些修改。CLI 和 CGI
文件名也改了。更多信息请查看<a href="/migration5/cli-cgi.html" class="link">相应章节</a>。

移植 Apache 配置极其简单。照下面的例子来检查需要做的修改：

**示例 \#1 移植 Apache 配置文件到 PHP 5**

``` apache-conf
# 将下面这行：
LoadModule php4_module /php/sapi/php4apache2.dll

# 改成这一行：
LoadModule php5_module /php/php5apache2.dll
```

如果 web 服务器是以 CGI 模式运行 PHP 的，应该注意 CGI 版本的名字从
`php.exe` 改为了 `php-cgi.exe`。在 Apache 中，应该照这样改：

**示例 \#2 移植 Apache 配置文件到 PHP 5，CGI 模式**

``` apache-conf
# 将下面这行：
Action application/x-httpd-php "/php/php.exe"

# 改成这一行：
Action application/x-httpd-php "/php/php-cgi.exe"
```

其它的 web 服务器中，需要修改 CGI 或者 ISAPI 模块的名字。
