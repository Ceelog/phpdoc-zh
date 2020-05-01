CLI 和 CGI
----------

PHP 5 中对 CLI 和 CGI 文件名作了些改变。PHP 5 中，CGI 版本被改名为
`php-cgi.exe`（以前是 `php.exe`），现在主目录中的是 CLI 版本（之前是
`cli/php.exe`）。

PHP 5 中引进了一种新模式：`php-win.exe`。这和 CLI 版本相同，只除了
php-win 不输出任何内容，因此不会提供控制台（屏幕上不会闪过“dos
窗口”）。此行为类似 php-gtk。

PHP 5 中，CLI 版本总会产生全局变量 `$argv` 和 `$argc` 而不管 `php.ini`
是怎么设的。即使将
<a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a>
设为 *off* 也不影响 CLI。

参见<a href="/features/commandline.html" class="link">命令行模式</a>。
