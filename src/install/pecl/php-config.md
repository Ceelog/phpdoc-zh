php-config
----------

php-config 是一个简单的命令行脚本用于获取所安装的 PHP 配置的信息。

在编译扩展时，如果安装有多个 PHP 版本，可以在配置时用
*--with-php-config* 选项来指定使用哪一个版本编译，该选项指定了相对应的
php-config 脚本的路径。

php-config 脚本在命令行所能使用的选项可以通过 **-h** 选项来显示：

    Usage: /usr/local/bin/php-config [OPTION]
    Options:
      --prefix            [...]
      --includes          [...]
      --ldflags           [...]
      --libs              [...]
      --extension-dir     [...]
      --include-dir       [...]
      --php-binary        [...]
      --php-sapis         [...]
      --configure-options [...]
      --version           [...]
      --vernum            [...]

| 选项                | 说明                                  |
|---------------------|---------------------------------------|
| --prefix            | PHP 所安装的路径前缀，例如 /usr/local |
| --includes          | 列出用 -I 选项包含的所有文件          |
| --ldflags           | PHP 编译时所使用的 LD 标志            |
| --libs              | PHP 编译时所附加的库                  |
| --extension-dir     | 扩展库的默认路径                      |
| --include-dir       | 头文件的默认路径前缀                  |
| --php-binary        | PHP CLI 或者 CGI 可执行文件的完整路径 |
| --php-sapis         | 列出所有可用的 SAPI 模块              |
| --configure-options | 重现当前 PHP 在编译时的配置选项       |
| --version           | PHP 版本号                            |
| --vernum            | PHP 版本号，以整数表示                |
