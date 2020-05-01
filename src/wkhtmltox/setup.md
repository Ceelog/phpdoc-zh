安装／配置
==========

**目录**

-   [需求](/wkhtmltox/setup.html#需求)
-   [安装](/wkhtmltox/setup.html#安装)
-   [运行时配置](/wkhtmltox/setup.html#运行时配置)

需求
----

libwkhtmltox source and binary releases are distributed at
<a href="http://wkhtmltopdf.org" class="link external">» wkhtmltopdf.org</a>.

**Caution**

Windows users need to take the additional step of adding `wkhtmltox.dll`
to their `PATH`.

安装
----

The source code of this extension, and binaries for Windows are hosted
by
<a href="https://github.com/krakjoe/wkhtmltox" class="link external">» github</a>,

Fetching the source code and building the extension:

    git clone https://github.com/krakjoe/wkhtmltox
    cd wkhtmltox
    phpize
    ./configure --with-wkhtmltox=/path/to/wkhtmltox/installation
    make
    sudo make install
       

Fetching updates and rebuilding the extension:

    cd wkhtmltox
    phpize --clean
    git pull origin master
    phpize
    ./configure --with-wkhtmltox=/path/to/wkhtmltox/installation
    make
    sudo make install
       

运行时配置
----------

| Name               | Description                        | Default | Stage                                | Changelog |
|--------------------|------------------------------------|---------|--------------------------------------|-----------|
| wkhtmltox.graphics | allow libwkhtmltox to use graphics | Off     | PHP\_INI\_SYSTEM \| PHP\_INI\_PERDIR | \>= 0.3.2 |
