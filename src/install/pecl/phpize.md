用 phpize 编译共享 PECL 扩展库
------------------------------

有时候不能用 *pecl*
安装命令。这可能是因为在防火墙后面，或者是因为想要安装的扩展库还没有
PECL 兼容的包，例如 SVN
中尚未发布的扩展库。如果要编译这种扩展库，可以用更底层的编译工具来手工进行编译。

*phpize* 命令是用来准备 PHP
扩展库的编译环境的。下面例子中，扩展库的源程序位于 `extname` 目录中：

    $ cd extname
    $ phpize
    $ ./configure
    $ make
    # make install

成功的安装将创建 `extname.so` 并放置于 PHP
的<a href="/ini/core.html#ini.extension-dir" class="link">扩展库目录</a>中。需要调整
`php.ini`，加入 *extension=extname.so* 这一行之后才能使用此扩展库。

如果系统中没有 *phpize* 命令并且使用了预编译的包（例如 RPM），那要安装
PHP 包相应的开发版本，此版本通常包含了 *phpize* 命令以及相应的用于编译
PHP 及其扩展库的头文件。

使用 **phpize --help** 命令可以显示此命令用法。
