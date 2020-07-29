Other Changes
-------------

### Performance Improvements

#### PHP Core

A specialized VM opcode for the <span
class="function">array\_key\_exists</span> function has been added,
which improves performance of this function if it can be statically
resolved. In namespaced code, this may require writing
*\\array\_key\_exists()* or explicitly importing the function.

#### Regular Expressions (Perl-Compatible)

When <span class="function">preg\_match</span> in UTF-8 mode (*"u"*
modifier) is repeatedly called on the same string (but possibly
different offsets), it will only be checked for UTF-8 validity once.

### Changes to INI File Handling

<a href="/ini/core.html#ini.zend.exception-ignore-args" class="link">zend.exception_ignore_args</a>
is a new INI directive for including or excluding arguments from stack
traces generated from exceptions.

<a href="/opcache/setup.html#" class="link">opcache.preload_user</a> is
a new INI directive for specifying the user account under which
preloading code is execute if it would otherwise be run as root (which
is not allowed for security reasons).

### Migration to pkg-config

A number of extensions have been migrated to exclusively use pkg-config
for the detection of library dependencies. Generally, this means that
instead of using **--with-foo-dir=DIR** or similar only **--with-foo**
is used. Custom library paths can be specified either by adding
additional directories to *PKG\_CONFIG\_PATH* or by explicitly
specifying compilation options through *FOO\_CFLAGS* and *FOO\_LIBS*.

The following extensions and SAPIs are affected:

-   <span class="simpara">CURL:</span>
    -   <span class="simpara"> **--with-curl** no longer accepts a
        directory. </span>
-   <span class="simpara">Enchant:</span>
    -   <span class="simpara"> **--with-enchant** no longer accepts a
        directory. </span>
-   <span class="simpara">FPM:</span>
    -   <span class="simpara"> **--with-fpm-systemd** now uses only
        pkg-config for libsystem checks. The libsystemd minimum required
        version is 209. </span>
-   <span class="simpara">GD:</span>
    -   <span class="simpara"> **--with-gd** becomes **--enable-gd**
        (whether to enable the extension at all) and
        **--with-external-gd** (to opt into using an external libgd,
        rather than the bundled one). </span>
    -   <span class="simpara"> **--with-png-dir** has been removed.
        libpng is required. </span>
    -   <span class="simpara"> **--with-zlib-dir** has been removed.
        zlib is required. </span>
    -   <span class="simpara"> **--with-freetype-dir** becomes
        **--with-freetype** </span>
    -   <span class="simpara"> **--with-jpeg-dir** becomes
        **--with-jpeg** </span>
    -   <span class="simpara"> **--with-webp-dir** becomes
        **--with-webp** </span>
    -   <span class="simpara"> **--with-xpm-dir** becomes **--with-xpm**
        </span>
-   <span class="simpara">IMAP:</span>
    -   <span class="simpara"> **--with-kerberos-systemd** no longer
        accepts a directory. </span>
-   <span class="simpara">Intl:</span>
    -   <span class="simpara"> **--with-icu-dir** has been removed. If
        **--enable-intl** is passed, then libicu is always required.
        </span>
-   <span class="simpara">LDAP:</span>
    -   <span class="simpara"> **--with-ldap-sasl** no longer accepts a
        directory. </span>
-   <span class="simpara">Libxml:</span>
    -   <span class="simpara"> **--with-libxml-dir** has been removed.
        </span>
    -   <span class="simpara"> **--enable-libxml** becomes
        **--with-libxml**. </span>
    -   <span class="simpara"> **--with-libexpat-dir** has been renamed
        to **--with-expat** and no longer accepts a directory. </span>
-   <span class="simpara">Litespeed:</span>
    -   <span class="simpara"> **--with-litespeed** becomes
        **--enable-litespeed**. </span>
-   <span class="simpara">Mbstring:</span>
    -   <span class="simpara"> **--with-onig** has been removed. Unless
        **--disable-mbregex** has been passed, libonig is required.
        </span>
-   <span class="simpara">ODBC:</span>
    -   <span class="simpara"> **--with-iodbc** no longer accepts a
        directory. </span>
    -   <span class="simpara"> **--with-unixODBC** without a directory
        now uses pkg-config (preferred). Directory is still accepted for
        old versions without libodbc.pc. </span>
-   <span class="simpara">OpenSSL:</span>
    -   <span class="simpara"> **--with-openssl** no longer accepts a
        directory. </span>
-   <span class="simpara">PCRE:</span>
    -   <span class="simpara"> **--with-pcre-regex** has been removed.
        Instead **--with-external-pcre** is provided to opt into using
        an external PCRE library, rather than the bundled one. </span>
-   <span class="simpara">PDO\_SQLite:</span>
    -   <span class="simpara"> **--with-pdo-sqlite** no longer accepts a
        directory. </span>
-   <span class="simpara">Readline:</span>
    -   <span class="simpara"> **--with-libedit** no longer accepts a
        directory. </span>
-   <span class="simpara">Sodium:</span>
    -   <span class="simpara"> **--with-sodium** no longer accepts a
        directory. </span>
-   <span class="simpara">SQLite3:</span>
    -   <span class="simpara"> **--with-sqlite3** no longer accepts a
        directory. </span>
-   <span class="simpara">XSL:</span>
    -   <span class="simpara"> **--with-xsl** no longer accepts a
        directory. </span>
-   <span class="simpara">Zip:</span>
    -   <span class="simpara"> **--with-libzip** has been removed.
        </span>
    -   <span class="simpara"> **--enable-zip** becomes **--with-zip**.
        </span>

### CSV escaping

<span class="function">fputcsv</span>, <span
class="function">fgetcsv</span>, <span
class="methodname">SplFileObject::fputcsv</span>, <span
class="methodname">SplFileObject::fgetcsv</span>, and <span
class="methodname">SplFileObject::setCsvControl</span> now accept an
empty string as *$escape* argument, which disables the proprietary PHP
escaping mechanism.

The behavior of <span class="function">str\_getcsv</span> has been
adjusted accordingly (formerly, an empty string was identical to using
the default).

<span class="methodname">SplFileObject::getCsvControl</span> now may
also return an empty string for the third array element, accordingly.

### Data Filtering

The <a href="/book/filter.html" class="link">filter</a> extension no
longer exposes **--with-pcre-dir** for Unix builds and can now reliably
be built as shared when using **./configure**

### GD

The behavior of <span class="function">imagecropauto</span> in the
bundled libgd has been synced with that of system libgd:

-   <span class="simpara"> **`IMG_CROP_DEFAULT`** is no longer falling
    back to **`IMG_CROP_SIDES`** </span>
-   <span class="simpara"> Threshold-cropping now uses the algorithm of
    system libgd </span>

The default *$mode* parameter of <span
class="function">imagecropauto</span> has been changed to
**`IMG_CROP_DEFAULT`**; passing *-1* is now deprecated.

<span class="function">imagescale</span> now supports aspect ratio
preserving scaling to a fixed height by passing *-1* as *$new\_width*.

### HASH Message Digest Framework

The <a href="/book/hash.html" class="link">hash</a> extension cannot be
disabled anymore and is always an integral part of any PHP build,
similar to the <a href="/book/datetime.html" class="link">date</a>
extension.

### Intl

The <a href="/book/intl.html" class="link">intl</a> extension now
requires at least ICU 50.1.

<span class="classname">ResourceBundle</span> now implements <span
class="interfacename">Countable</span>.

### Lightweight Directory Access Protocol

Support for nsldap and umich\_ldap has been removed.

### Libxml

All libxml-based extensions now require libxml 2.7.6 or newer.

### Multibyte String

The oniguruma library is no longer bundled with PHP, instead libonig
needs to be available on the system. Alternatively **--disable-mbregex**
can be used to disable the mbregex component.

### OPcache

The **--disable-opcache-file** and **--enable-opcache-file** configure
options have been removed in favor of the
<a href="/opcache/setup.html#" class="link">opcache.file_cache</a> INI
directive.

### Password Hashing

The <span class="function">password\_hash</span> and <span
class="function"></span> functions now accept nullable <span
class="type">string</span> and <span class="type">integer</span> for
*$algo* argument.

### PEAR

Installation of PEAR (including PECL) is no longer enabled by default.
It can be explicitly enabled using **--with-pear**. This option is
deprecated and may be removed in the future.

### Reflection

The numeric values of the modifier constants (*IS\_ABSTRACT*,
*IS\_DEPRECATED*, *IS\_EXPLICIT\_ABSTRACT*, *IS\_FINAL*,
*IS\_IMPLICIT\_ABSTRACT*, *IS\_PRIVATE*, *IS\_PROTECTED*, *IS\_PUBLIC*,
and *IS\_STATIC*) on the <span class="classname">ReflectionClass</span>,
<span class="classname">ReflectionFunction</span>, <span
class="classname">ReflectionMethod</span>, <span
class="classname">ReflectionObject</span>, and <span
class="classname">ReflectionProperty</span> classes have changed.

### SimpleXML

<span class="classname">SimpleXMLElement</span> now implements <span
class="interfacename">Countable</span>.

### SQLite3

The bundled libsqlite has been removed. To build the
<a href="/book/sqlite3.html" class="link">SQLite3</a> extension a system
libsqlite3 ≥ 3.7.4 is now required. To build the
<a href="/book/pdo.html#SQLite%20(PDO)" class="link">PDO_SQLite</a>
extension a system libsqlite3 ≥ 3.5.0 is now required.

Serialization and unserialization of <span
class="classname">SQLite3</span>, <span
class="classname">SQLite3Stmt</span> and <span
class="classname">SQLite3Result</span> is now explicitly forbidden.
Formerly, serialization of instances of these classes was possible, but
unserialization yielded unusable objects.

The *@param* notation can now also be used to denote SQL query
parameters.

### Zip

The bundled libzip library has been removed. A system libzip \>= 0.11 is
now necessary to build the <a href="/book/zip.html" class="link">zip</a>
extension.
