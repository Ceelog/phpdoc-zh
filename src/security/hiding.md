隐藏 PHP
========

一般而言，通过隐藏的手段提高安全性被认为是作用不大的做法。但某些情况下，尽可能的多增加一份安全性都是值得的。

一些简单的方法可以帮助隐藏
PHP，这样做可以提高攻击者发现系统弱点的难度。在 `php.ini` 文件里设置
expose\_php = off ，可以减少他们能获得的有用信息。

另一个策略就是让 web 服务器用 PHP 解析不同扩展名。无论是通过 `.htaccess`
文件还是 Apache 的配置文件，都可以设置能误导攻击者的文件扩展名：

**示例 \#1 把 PHP 隐藏为另一种语言**

``` apache-conf
# 使PHP看上去像其它的编程语言
AddType application/x-httpd-php .asp .py .pl
```

或者干脆彻底隐藏它：

**示例 \#2 使用未知的扩展名作为 PHP 的扩展名**

``` apache-conf
# 使 PHP 看上去像未知的文件类型
AddType application/x-httpd-php .bop .foo .133t
```

或者把它隐藏为 HTML 页面，这样所有的 HTML 文件都会通过 PHP
引擎，会为服务器增加一些负担：

**示例 \#3 用 HTML 做 PHP 的文件后缀**

``` apache-conf
# 使 PHP 代码看上去像 HTML 页面
AddType application/x-httpd-php .htm .html
```

要让此方法生效，必须把 PHP
文件的扩展名改为以上的扩展名。这样就通过隐藏来提高了安全性，虽然防御能力很低而且有些缺点。
