安装／配置
==========

**目录**

-   [需求](/ds/setup.html#需求)
-   [安装](/ds/setup.html#安装)

需求
----

PHP 7 is required by both the extension and the compatibility polyfill.

安装
----

The easiest way to install the extension is via
<a href="https://pecl.php.net/package/ds" class="link external">» PECL</a>

    pecl install ds

You can also build directly from source:

    # Dependencies you might need to install
    # sudo apt-get install git build-essential php7.0-dev

    git clone https://github.com/php-ds/extension "php-ds"
    cd php-ds

    # Build and install the extension
    phpize
    ./configure
    make
    make install

    # Clean up the build files
    make clean
    phpize --clean

If you're on Windows, you can
<a href="https://pecl.php.net/package/ds" class="link external">» download a compiled .dll on PECL</a>

> **Note**:
>
> If you're using Composer, it's highly recommended that you include
> <a href="https://packagist.org/packages/php-ds/php-ds" class="link external">» php-ds/php-ds</a>
> in your project so that your code is still functional in an
> environment where the extension is not installed. The extension will
> take priority if installed.
