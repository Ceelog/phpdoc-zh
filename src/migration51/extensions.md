Extensions
----------

-   <a href="/migration51/extensions.html#migration51.extensions-gone" class="link">Extensions that are gone from the PHP core</a>

-   <a href="/migration51/extensions.html#migration51.extensions-constants" class="link">Class constants in new PHP 5.1.x extensions</a>

Extensions that are gone from the PHP core
------------------------------------------

One of the first things you're likely to notice when you download PHP
5.1.x is that several of the older extensions have disappeared. Those
extensions that are still actively maintained are available in the PHP
Extension Community Library (PECL), at
<a href="https://pecl.php.net/" class="link external">» https://pecl.php.net/</a>.

| Extension                                                                | Alternative/Status                                                                                                                      |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| ext/cpdf                                                                 | pecl/pdflib                                                                                                                             |
| <a href="/book/dbx.html#dbx%20函数" class="link">ext/dbx</a>             | pecl/dbx                                                                                                                                |
| <a href="/ref/dio.html" class="link">ext/dio</a>                         | pecl/dio                                                                                                                                |
| ext/fam                                                                  | Not actively maintained                                                                                                                 |
| <a href="/book/ingres.html#Ingres%20函数" class="link">ext/ingres_ii</a> | pecl/ingres                                                                                                                             |
| ext/ircg                                                                 | Not actively maintained                                                                                                                 |
| ext/mcve                                                                 | pecl/mcve                                                                                                                               |
| ext/mnogosearch                                                          | Not actively maintained                                                                                                                 |
| ext/oracle                                                               | <a href="/book/oci8.html#OCI8%20函数" class="link">ext/oci8</a> or <a href="/book/pdo.html#Oracle%20(PDO)" class="link">ext/pdo_oci</a> |
| ext/ovrimos                                                              | Not actively maintained                                                                                                                 |
| ext/pfpro                                                                | Not actively maintained                                                                                                                 |
| ext/w32api                                                               | <a href="https://pecl.php.net/package/ffi" class="link external">» pecl/ffi</a>                                                         |
| ext/yp                                                                   | Not actively maintained                                                                                                                 |
| ext/activescript                                                         | <a href="https://pecl.php.net/package/activescript" class="link external">» pecl/activescript</a>                                       |

Modules in PECL that are not actively maintained (i.e. have not been
supported for some time, have no active maintainer working on them
currently, and do not have any PECL package releases), are still
available in SVN at
<a href="https://svn.php.net/viewvc/pecl" class="link external">» https://svn.php.net/viewvc/pecl</a>.
However, unreleased PHP modules are by their nature unsupported, and
your mileage may vary when attempting to install or use them.

Class constants in new PHP 5.1.x extensions
-------------------------------------------

The Zend Engine 2.1 API allows extension developers to declare class
constants in object oriented extensions. New extensions written for PHP
5.1.x, including <a href="/ref/spl.html" class="link">SPL</a>,
<a href="/book/pdo.html#简介" class="link">PDO</a>,
<a href="/book/xmlreader.html" class="link">XMLReader</a> and
<a href="/ref/datetime.html" class="link">date</a>, have their constants
in the format **`PDO::CLASS_CONSTANT`** rather than in the C format
**`PDO_CLASS_CONSTANT`** in order to minimise pollution of the global
namespace in PHP.
