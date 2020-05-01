Installation
============

parallel requires a build of PHP with ZTS (Zend Thread Safety) enabled (
--enable-maintainer-zts or --enable-zts on Windows )

**Caution**

Zend Thread Safety cannot be enabled post build; it is a build time
configuration option.

parallel should build anywhere there is a working Posix Threads header
(pthread.h) and ZTS build of PHP, including Windows (using the
pthread-w32 project from redhat).

parallel releases are hosted by PECL and the source code by
<a href="https://github.com/krakjoe/parallel" class="link external">» github</a>,
the easiest route to installation is the normal PECL route:
<a href="https://pecl.php.net/package/parallel" class="link external">» https://pecl.php.net/package/parallel</a>.

Windows users can download prebuilt release binaries from the
<a href="https://windows.php.net/downloads/pecl/releases/parallel" class="link external">» PECL</a>
website.

**Caution**

Windows users need to take the additional step of adding pthreadVC2.dll
(distributed with Windows releases) to their `PATH`.
