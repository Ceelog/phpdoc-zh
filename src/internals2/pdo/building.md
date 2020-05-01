Building
--------

The build process is designed to work with PEAR (see
<a href="https://pear.php.net/" class="link external">» https://pear.php.net/</a>
for more information about PEAR). There are two files that are used to
assist in configuring your package for building. The first is config.m4
which is the **autoconf** configuration file for all platforms except
Win32. The second is config.w32 which is a build configuration file for
use on Win32. Skeleton files for these are built for you when you first
set up your project. You then need to customize them to fit the needs of
your project. Once you've customized your config files, you can build
your driver using the following sequence of commands:

Before first build:

    $ sudo pecl install PDO

For each build:

    $ cd pdo_SKEL
    $ phpize
    $ ./configure
    $ make
    $ sudo make install

The process can then be repeated as necessary during the development
process.
