安装／配置
==========

**目录**

-   [需求](/sdodasrel/setup.html#需求)
-   [安装](/sdodasrel/setup.html#安装)
-   [运行时配置](/sdodasrel/setup.html#运行时配置)
-   [资源类型](/sdodasrel/setup.html#资源类型)

需求
----

The Relational DAS requires that the SDO extension be installed. The SDO
extension requires a version of PHP 5.1, and the Relational DAS requires
a recent version that contains an important fix for PDO. The most
up-to-date information about required levels of PHP should be found in
the changelog for the package on PECL. At the time of writing, though,
the Relational DAS requires the most recent beta level of PHP 5.1, that
is PHP 5.1.0.

The Relational DAS uses PDO to access the relational database, and so
should run with a variety of different relational databases. At the time
of writing it has been tested in the following configurations

-   MySQL 4.1.14, on Windows. The Relational DAS operates correctly with
    the php\_pdo\_mysql driver that comes with the pre-built binaries
    for PHP 5.1.0.

-   MySQL 4.1.13, on Linux. It is necessary to have the most up-to-date
    PDO driver for MySQL, which comes built in to PHP 5.1.0. It may be
    necessary to uninstall the usual driver that would have come from
    PECL using **pear uninstall pdo\_mysql**. You will need to configure
    PHP with the **--with-pdo-mysql** option.

-   DB2 8.2 Personal Edition, on Windows. The Relational DAS operates
    correctly with the php\_pdo\_odbc driver that comes with the
    pre-built binaries for PHP 5.1.0.

-   DB2 8.2 Personal Developer's Edition, on Linux. The Developer's
    Edition is needed because it contains the include files needed when
    PHP is configured and built. You will need to configure PHP with the
    **--with-pdo-odbc=ibm-db2** option.

The Relational DAS applies changes to the database within a
user-delimited transaction: that is, it issues a call to <span
class="function">PDO::beginTransaction</span> before beginning to apply
changes, and <span class="function">PDO::commit</span> or <span
class="function">PDO::rollback</span> on completion. Whichever database
is chosen, the database and the PDO driver for the database must support
these calls.

安装
----

The installation instructions for all the SDO components are in the SDO
<a href="/sdo/setup.html#安装" class="link">install</a> section of the
SDO documentation.

In any case, the essential facts are that the Relational DAS is written
in PHP and it should be placed somewhere on the PHP
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>.

Your application will of course need to include the Relational DAS with
a statement like this:

``` php
<?php
require_once 'SDO/DAS/Relational.php';
?>
```

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

Tracing
-------

You may be interested in seeing the SQL statements that are generated in
order to apply changes back to the database. At the top of the
`SDO/DAS/Relational.php` you will find a number of constants which
control whether the process of constructing and executing the SQL
statements is to be traced. Try setting `DEBUG_EXECUTE_PLAN` to
**`true`** to see the generated SQL statements.

资源类型
--------

此扩展没有定义资源类型。
