将 PECL 扩展库静态编译入 PHP
----------------------------

有时可能需要将扩展库静态编译到 PHP 中。这需要将扩展库源程序放入
`php-src/ext/` 目录中去并告诉 PHP 编译系统来生成其配置脚本。

    $ cd /your/phpsrcdir/ext
    $ pecl download extname
    $ gzip -d < extname.tgz | tar -xvf -
    $ mv extname-x.x.x extname

这将产生以下目录：

  
/your/phpsrcdir/ext/extname  

此时强制 PHP 重新生成配置脚本，然后正常编译 PHP：

  
$ cd /your/phpsrcdir  
$ rm configure  
$ ./buildconf --force  
$ ./configure --help  
$ ./configure --with-extname --enable-someotherext --with-foobar  
$ make  
$ make install  

> **Note**: <span class="simpara"> 要运行“buildconf”脚本，需要 autoconf
> 2.13 和 automake 1.4+（更新版本的 autoconf 也许能工作，但不被支持）。
> </span>

是否用 *--enable-extname* 或 *--with-extname*
取决于扩展库。通常不需要外部库文件的扩展库使用
*--enable*。要确认的话，在 buildconf 之后运行：

  
$ ./configure --help \| grep extname  
