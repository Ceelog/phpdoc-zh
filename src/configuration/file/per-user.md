.user.ini 文件
--------------

自 PHP 5.3.0 起，PHP 支持基于每个目录的 .htaccess 风格的 INI
文件。此类文件*仅*被 CGI／FastCGI SAPI 处理。此功能使得 PECL 的
htscanner 扩展作废。如果使用 Apache，则用 `.htaccess` 文件有同样效果。

除了主 `php.ini` 之外，PHP 还会在每个目录下扫描 INI 文件，从被执行的 PHP
文件所在目录开始一直上升到 web 根目录（`$_SERVER['DOCUMENT_ROOT']`
所指定的）。如果被执行的 PHP 文件在 web 根目录之外，则只扫描该目录。

在 .user.ini 风格的 INI 文件中只有具有 **`PHP_INI_PERDIR`** 和
**`PHP_INI_USER`** 模式的 INI 设置可被识别。

两个新的 INI 指令，*user\_ini.filename* 和 *user\_ini.cache\_ttl*
控制着用户 INI 文件的使用。

*user\_ini.filename* 设定了 PHP
会在每个目录下搜寻的文件名；如果设定为空字符串则 PHP 不会搜寻。默认值是
*.user.ini*。

*user\_ini.cache\_ttl* 控制着重新读取用户 INI 文件的间隔时间。默认是 300
秒（5 分钟）。
