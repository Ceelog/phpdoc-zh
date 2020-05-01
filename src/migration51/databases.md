Changes in database support
---------------------------

-   <a href="/migration51/databases.html#migration51.databases-pdo" class="link">PDO overview</a>

-   <a href="/migration51/databases.html#migration51.databases-mysql" class="link">Changes in MySQL support</a>

-   <a href="/migration51/databases.html#migration51.databases-sqlite" class="link">Changes in SQLite support</a>

PDO overview
------------

<a href="/book/pdo.html#简介" class="link">PHP Data Objects (PDO)</a>
were introduced as a PECL extension under PHP 5.0, and became part of
the core PHP distribution in PHP 5.1.x. The PDO extension provides a
consistent interface for database access, and is used alongside
database-specific PDO drivers. Each driver may also have
database-specific functions of its own, but basic data access
functionality such as issuing queries and fetching data is covered by
PDO functions, using the driver named in <span
class="function">PDO::\_\_construct</span>.

Note that the PDO extension, and its drivers, are intended to be built
as shared extensions. This will enable straightforward driver upgrades
from PECL, without forcing you to rebuild all of PHP.

At the point of the PHP 5.1.x release, PDO is more than ready for
widespread testing and could be adopted in most situations. However, it
is important to understand that PDO and its drivers are comparatively
young and may be missing certain database-specific features; evaluate
PDO carefully before you use it in new projects.

Legacy code will generally rely on the pre-existing database extensions,
which are still maintained.

Changes in MySQL support
------------------------

In PHP 4, MySQL 3 support was built-in. With the release of PHP 5.0
there were two MySQL extensions, named 'mysql' and 'mysqli', which were
designed to support MySQL \< 4.1 and MySQL 4.1 and up, respectively.
With the introduction of PDO, which provides a very fast interface to
all the database APIs supported by PHP, the PDO\_MYSQL driver can
support any of the current versions (MySQL 3, 4 or 5) in PHP code
written for PDO, depending on the MySQL library version used during
compilation. The older MySQL extensions remain in place for reasons of
back compatibility, but are not enabled by default.

Changes in SQLite support
-------------------------

In PHP 5.0.x, SQLite 2 support was provided by the built-in sqlite
extension, which was also available as a PECL extension in PHP 4.3 and
PHP 4.4. With the introduction of PDO, the sqlite extension doubles up
to act as a 'sqlite2' driver for PDO; it is due to this that the sqlite
extension in PHP 5.1.x has a dependency upon the PDO extension.

PHP 5.1.x ships with a number of alternative interfaces to sqlite:

The sqlite extension provides the "classic" sqlite procedural/OO API
that you may have used in prior versions of PHP. It also provides the
PDO 'sqlite2' driver, which allows you to access legacy SQLite 2
databases using the PDO API.

PDO\_SQLITE provides the 'sqlite' version 3 driver. SQLite version 3 is
vastly superior to SQLite version 2, but the file formats of the two
versions are not compatible.

If your SQLite-based project is already written and working against
earlier PHP versions, then you can continue to use ext/sqlite without
problems, but will need to explicitly enable both PDO and sqlite. New
projects should use PDO and the 'sqlite' (version 3) driver, as this is
faster than SQLite 2, has improved locking concurrency, and supports
both prepared statements and binary columns natively.

You must enable PDO to use the SQLite extension. If you want to build
the PDO extension as a shared extension, then the SQLite extension must
also be built shared. The same holds true for any extension that
provides a PDO driver
