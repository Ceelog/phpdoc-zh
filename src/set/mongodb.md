MongoDB driver
==============

**目录**

-   [安装／配置](/set/mongodb.html#安装／配置)
    -   [需求](/set/mongodb.html#需求)
    -   [安装](/set/mongodb.html#安装)
    -   [运行时配置](/set/mongodb.html#运行时配置)
    -   [预定义常量](/set/mongodb.html#预定义常量)
-   [Tutorials](/set/mongodb.html#Tutorials) — Tutorials
    -   [Using the PHP Library for MongoDB
        (PHPLIB)](/set/mongodb.html#Using%20the%20PHP%20Library%20for%20MongoDB%20(PHPLIB))
    -   [Application Performance Monitoring
        (APM)](/set/mongodb.html#Application%20Performance%20Monitoring%20(APM))
-   [Driver Architecture and
    Internals](/set/mongodb.html#Driver%20Architecture%20and%20Internals)
    — Explains the driver architecture, and special features
    -   [Architecture](/set/mongodb.html#Architecture) — Architecture
        Overview
    -   [Connections](/set/mongodb.html#Connections) — Connection
        handling and persistence
    -   [Persisting Data](/set/mongodb.html#Persisting%20Data) —
        Serialization and deserialization of PHP variables into MongoDB
-   [Security](/set/mongodb.html#Security)
    -   [Request Injection
        Attacks](/set/mongodb.html#Request%20Injection%20Attacks)
    -   [Script Injection
        Attacks](/set/mongodb.html#Script%20Injection%20Attacks)
-   [MongoDB\\Driver](/set/mongodb.html#MongoDB\Driver) — MongoDB 驱动类
    -   [MongoDB\\Driver\\Manager](/set/mongodb.html#MongoDB\Driver\Manager)
        — The MongoDB\\Driver\\Manager class
    -   [MongoDB\\Driver\\Command](/set/mongodb.html#MongoDB\Driver\Command)
        — The MongoDB\\Driver\\Command class
    -   [MongoDB\\Driver\\Query](/set/mongodb.html#MongoDB\Driver\Query)
        — The MongoDB\\Driver\\Query class
    -   [MongoDB\\Driver\\BulkWrite](/set/mongodb.html#MongoDB\Driver\BulkWrite)
        — The MongoDB\\Driver\\BulkWrite class
    -   [MongoDB\\Driver\\WriteConcern](/set/mongodb.html#MongoDB\Driver\WriteConcern)
        — The MongoDB\\Driver\\WriteConcern class
    -   [MongoDB\\Driver\\ReadPreference](/set/mongodb.html#MongoDB\Driver\ReadPreference)
        — The MongoDB\\Driver\\ReadPreference class
    -   [MongoDB\\Driver\\ReadConcern](/set/mongodb.html#MongoDB\Driver\ReadConcern)
        — The MongoDB\\Driver\\ReadConcern class
    -   [MongoDB\\Driver\\Cursor](/set/mongodb.html#MongoDB\Driver\Cursor)
        — The MongoDB\\Driver\\Cursor class
    -   [MongoDB\\Driver\\CursorId](/set/mongodb.html#MongoDB\Driver\CursorId)
        — The MongoDB\\Driver\\CursorId class
    -   [MongoDB\\Driver\\Server](/set/mongodb.html#MongoDB\Driver\Server)
        — The MongoDB\\Driver\\Server class
    -   [MongoDB\\Driver\\WriteConcernError](/set/mongodb.html#MongoDB\Driver\WriteConcernError)
        — The MongoDB\\Driver\\WriteConcernError class
    -   [MongoDB\\Driver\\WriteError](/set/mongodb.html#MongoDB\Driver\WriteError)
        — The MongoDB\\Driver\\WriteError class
    -   [MongoDB\\Driver\\WriteResult](/set/mongodb.html#MongoDB\Driver\WriteResult)
        — The MongoDB\\Driver\\WriteResult class
-   [MongoDB\\BSON](/set/mongodb.html#MongoDB\BSON) — BSON type classes
    and serialization functions
    -   [函数](/set/mongodb.html#函数)
    -   [MongoDB\\BSON\\Binary](/set/mongodb.html#MongoDB\BSON\Binary) —
        The MongoDB\\BSON\\Binary class
    -   [MongoDB\\BSON\\Decimal128](/set/mongodb.html#MongoDB\BSON\Decimal128)
        — The MongoDB\\BSON\\Decimal128 class
    -   [MongoDB\\BSON\\Javascript](/set/mongodb.html#MongoDB\BSON\Javascript)
        — The MongoDB\\BSON\\Javascript class
    -   [MongoDB\\BSON\\MaxKey](/set/mongodb.html#MongoDB\BSON\MaxKey) —
        The MongoDB\\BSON\\MaxKey class
    -   [MongoDB\\BSON\\MinKey](/set/mongodb.html#MongoDB\BSON\MinKey) —
        The MongoDB\\BSON\\MinKey class
    -   [MongoDB\\BSON\\ObjectId](/set/mongodb.html#MongoDB\BSON\ObjectId)
        — The MongoDB\\BSON\\ObjectId class
    -   [MongoDB\\BSON\\Regex](/set/mongodb.html#MongoDB\BSON\Regex) —
        The MongoDB\\BSON\\Regex class
    -   [MongoDB\\BSON\\Timestamp](/set/mongodb.html#MongoDB\BSON\Timestamp)
        — The MongoDB\\BSON\\Timestamp class
    -   [MongoDB\\BSON\\UTCDateTime](/set/mongodb.html#MongoDB\BSON\UTCDateTime)
        — The MongoDB\\BSON\\UTCDateTime class
    -   [MongoDB\\BSON\\Type](/set/mongodb.html#MongoDB\BSON\Type) — The
        MongoDB\\BSON\\Type interface
    -   [MongoDB\\BSON\\Persistable](/set/mongodb.html#MongoDB\BSON\Persistable)
        — The MongoDB\\BSON\\Persistable interface
    -   [MongoDB\\BSON\\Serializable](/set/mongodb.html#MongoDB\BSON\Serializable)
        — The MongoDB\\BSON\\Serializable interface
    -   [MongoDB\\BSON\\Unserializable](/set/mongodb.html#MongoDB\BSON\Unserializable)
        — The MongoDB\\BSON\\Unserializable interface
    -   [MongoDB\\BSON\\BinaryInterface](/set/mongodb.html#MongoDB\BSON\BinaryInterface)
        — The MongoDB\\BSON\\BinaryInterface interface
    -   [MongoDB\\BSON\\Decimal128Interface](/set/mongodb.html#MongoDB\BSON\Decimal128Interface)
        — The MongoDB\\BSON\\Decimal128Interface interface
    -   [MongoDB\\BSON\\JavascriptInterface](/set/mongodb.html#MongoDB\BSON\JavascriptInterface)
        — The MongoDB\\BSON\\JavascriptInterface interface
    -   [MongoDB\\BSON\\MaxKeyInterface](/set/mongodb.html#MongoDB\BSON\MaxKeyInterface)
        — The MongoDB\\BSON\\MaxKeyInterface interface
    -   [MongoDB\\BSON\\MinKeyInterface](/set/mongodb.html#MongoDB\BSON\MinKeyInterface)
        — The MongoDB\\BSON\\MinKeyInterface interface
    -   [MongoDB\\BSON\\ObjectIdInterface](/set/mongodb.html#MongoDB\BSON\ObjectIdInterface)
        — The MongoDB\\BSON\\ObjectIdInterface interface
    -   [MongoDB\\BSON\\RegexInterface](/set/mongodb.html#MongoDB\BSON\RegexInterface)
        — The MongoDB\\BSON\\RegexInterface interface
    -   [MongoDB\\BSON\\TimestampInterface](/set/mongodb.html#MongoDB\BSON\TimestampInterface)
        — The MongoDB\\BSON\\TimestampInterface interface
    -   [MongoDB\\BSON\\UTCDateTimeInterface](/set/mongodb.html#MongoDB\BSON\UTCDateTimeInterface)
        — The MongoDB\\BSON\\UTCDateTimeInterface interface
    -   [MongoDB\\BSON\\DBPointer](/set/mongodb.html#MongoDB\BSON\DBPointer)
        — The MongoDB\\BSON\\DBPointer class (deprecated)
    -   [MongoDB\\BSON\\Int64](/set/mongodb.html#MongoDB\BSON\Int64) —
        The MongoDB\\BSON\\Int64 class
    -   [MongoDB\\BSON\\Symbol](/set/mongodb.html#MongoDB\BSON\Symbol) —
        The MongoDB\\BSON\\Symbol class (deprecated)
    -   [MongoDB\\BSON\\Undefined](/set/mongodb.html#MongoDB\BSON\Undefined)
        — The MongoDB\\BSON\\Undefined class (deprecated)
-   [MongoDB\\Driver\\Monitoring](/set/mongodb.html#MongoDB\Driver\Monitoring)
    — Monitoring classes and subscriber functions
    -   [函数](/set/mongodb.html#函数)
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent)
        — The MongoDB\\Driver\\Monitoring\\CommandFailedEvent class
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent)
        — The MongoDB\\Driver\\Monitoring\\CommandStartedEvent class
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent)
        — The MongoDB\\Driver\\Monitoring\\CommandSucceededEvent class
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSubscriber)
        — The MongoDB\\Driver\\Monitoring\\CommandSubscriber interface
    -   [MongoDB\\Driver\\Monitoring\\Subscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\Subscriber)
        — The MongoDB\\Driver\\Monitoring\\Subscriber interface
-   [MongoDB\\Driver\\Exception](/set/mongodb.html#MongoDB\Driver\Exception)
    — Exception 类
    -   [MongoDB\\Driver\\Exception\\AuthenticationException](/set/mongodb.html#MongoDB\Driver\Exception\AuthenticationException)
        — The MongoDB\\Driver\\Exception\\AuthenticationException class
    -   [MongoDB\\Driver\\Exception\\BulkWriteException](/set/mongodb.html#MongoDB\Driver\Exception\BulkWriteException)
        — The MongoDB\\Driver\\Exception\\BulkWriteException class
    -   [MongoDB\\Driver\\Exception\\ConnectionException](/set/mongodb.html#MongoDB\Driver\Exception\ConnectionException)
        — The MongoDB\\Driver\\Exception\\ConnectionException class
    -   [MongoDB\\Driver\\Exception\\ConnectionTimeoutException](/set/mongodb.html#MongoDB\Driver\Exception\ConnectionTimeoutException)
        — The MongoDB\\Driver\\Exception\\ConnectionTimeoutException
        class
    -   [MongoDB\\Driver\\Exception\\Exception](/set/mongodb.html#MongoDB\Driver\Exception\Exception)
        — The MongoDB\\Driver\\Exception\\Exception interface
    -   [MongoDB\\Driver\\Exception\\ExecutionTimeoutException](/set/mongodb.html#MongoDB\Driver\Exception\ExecutionTimeoutException)
        — The MongoDB\\Driver\\Exception\\ExecutionTimeoutException
        class
    -   [MongoDB\\Driver\\Exception\\InvalidArgumentException](/set/mongodb.html#MongoDB\Driver\Exception\InvalidArgumentException)
        — The MongoDB\\Driver\\Exception\\InvalidArgumentException class
    -   [MongoDB\\Driver\\Exception\\LogicException](/set/mongodb.html#MongoDB\Driver\Exception\LogicException)
        — The MongoDB\\Driver\\Exception\\LogicException class
    -   [MongoDB\\Driver\\Exception\\RuntimeException](/set/mongodb.html#MongoDB\Driver\Exception\RuntimeException)
        — The MongoDB\\Driver\\Exception\\RuntimeException class
    -   [MongoDB\\Driver\\Exception\\SSLConnectionException](/set/mongodb.html#MongoDB\Driver\Exception\SSLConnectionException)
        — The MongoDB\\Driver\\Exception\\SSLConnectionException class
        (deprecated)
    -   [MongoDB\\Driver\\Exception\\UnexpectedValueException](/set/mongodb.html#MongoDB\Driver\Exception\UnexpectedValueException)
        — The MongoDB\\Driver\\Exception\\UnexpectedValueException class
    -   [MongoDB\\Driver\\Exception\\WriteException](/set/mongodb.html#MongoDB\Driver\Exception\WriteException)
        — The MongoDB\\Driver\\Exception\\WriteException class

Unlike the <a href="/book/mongo.html" class="link">mongo</a> extension,
this extension is developed atop the
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
and
<a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
libraries. It provides a minimal API for core driver functionality:
<a href="/set/mongodb.html#MongoDB\Driver\Command" class="link">commands</a>,
<a href="/set/mongodb.html#MongoDB\Driver\Query" class="link">queries</a>,
<a href="/set/mongodb.html#MongoDB\Driver\BulkWrite" class="link">writes</a>,
<a href="/set/mongodb.html#MongoDB\Driver\Manager" class="link">connection management</a>,
and
<a href="/set/mongodb.html#MongoDB\BSON" class="link">BSON serialization</a>.

Userland PHP libraries that depend on this extension may provide higher
level APIs, such as query builders, individual command helper methods,
and GridFS. Application developers should consider using this extension
in conjunction with the
<a href="https://github.com/mongodb/mongo-php-library" class="link external">» MongoDB PHP library</a>,
which implements the same higher level APIs found in MongoDB drivers for
other languages. This separation of concerns allows the driver to focus
on essential features for which an extension implementation is paramount
for performance.

安装／配置
==========

**目录**

-   [需求](/set/mongodb.html#需求)
-   [安装](/set/mongodb.html#安装)
    -   [Installing the MongoDB PHP Driver with
        PECL](/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20with%20PECL)
    -   [Installing the MongoDB PHP Driver on macOS with
        Homebrew](/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20on%20macOS%20with%20Homebrew)
    -   [Installing the MongoDB PHP Driver on
        Windows](/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20on%20Windows)
    -   [Building the MongoDB PHP Driver from
        source](/set/mongodb.html#Building%20the%20MongoDB%20PHP%20Driver%20from%20source)
-   [运行时配置](/set/mongodb.html#运行时配置)
-   [预定义常量](/set/mongodb.html#预定义常量)

需求
====

As of version 1.8.0, the driver requires PHP 7.0 or higher. Previous
versions of the driver allow compatibility with older PHP versions.

The driver requires
<a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
and
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>,
and will use bundled versions of both libraries by default. System
libraries may also be used, as discussed in the
<a href="/set/mongodb.html#Building%20the%20MongoDB%20PHP%20Driver%20from%20source" class="link">manual installation</a>
documentation.

The driver, via libmongoc, optionally depends on a TLS library (e.g.
OpenSSL) and will use it if available. If the build process fails to
find a TLS library, users should check that the appropriate development
package (e.g. *libssl-dev*) and
<a href="https://en.wikipedia.org/wiki/Pkg-config" class="link external">» pkg-config</a>
are both installed. The process for detecting and configuring TLS
libraries is discussed in more detail in the
<a href="/set/mongodb.html#Building%20the%20MongoDB%20PHP%20Driver%20from%20source" class="link">manual installation</a>
documentation.

<a href="http://cyrusimap.org/" class="link external">» Cyrus SASL</a>
is an optional dependency to support Kerberos authentication and will be
used if available.

> **Note**: <span class="simpara"> Due to potential problems
> representing 64-bit integers on 32-bit platforms, users are advised to
> use 64-bit environments. When using a 32-bit platform, be aware that
> any 64-bit integer read from the database will be returned as a <span
> class="classname">MongoDB\\BSON\\Int64</span> instance instead of a
> PHP integer type. </span>

安装
====

**目录**

-   [Installing the MongoDB PHP Driver with
    PECL](/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20with%20PECL)
-   [Installing the MongoDB PHP Driver on macOS with
    Homebrew](/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20on%20macOS%20with%20Homebrew)
-   [Installing the MongoDB PHP Driver on
    Windows](/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20on%20Windows)
-   [Building the MongoDB PHP Driver from
    source](/set/mongodb.html#Building%20the%20MongoDB%20PHP%20Driver%20from%20source)

Installing the MongoDB PHP Driver with PECL
-------------------------------------------

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/mongodb" class="link external">» https://pecl.php.net/package/mongodb</a>

Linux, Unix, and macOS users may run the following command to install
the driver:

``` shell
$ sudo pecl install mongodb
```

If your system has multiple version of PHP installed (e.g. macOS
default, Homebrew,
<a href="https://www.apachefriends.org/" class="link external">» XAMPP</a>),
note that that each version of PHP has its own
<a href="/install/pecl.html" class="link">pecl</a> command and `php.ini`
file.

Installing the driver via PECL will use bundled versions of
<a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
and
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
and attempt to automatically configure them.

> **Note**: <span class="simpara"> If the build process fails to find an
> SSL library, check that the development packages (e.g. *libssl-dev*)
> and
> <a href="https://en.wikipedia.org/wiki/Pkg-config" class="link external">» pkg-config</a>
> are both installed. If that does not resolve the problem, consider
> using the
> <a href="/set/mongodb.html#Building%20the%20MongoDB%20PHP%20Driver%20from%20source" class="link">manual installation</a>
> process. </span>

Finally, add the following line to your `php.ini` file:

``` ini
extension=mongodb.so
```

Installing the MongoDB PHP Driver on macOS with Homebrew
--------------------------------------------------------

<a href="https://brew.sh/2018/01/19/homebrew-1.5.0/" class="link external">» Homebrew 1.5.0</a>
deprecated the
<a href="https://github.com/Homebrew/homebrew-php" class="link external">» Homebrew/php tap</a>
and removed formulae for individual PHP extensions. Going forward, macOS
users are advised to install the
<a href="https://formulae.brew.sh/formula/php" class="link external">» php</a>
formula and follow the standard
<a href="/set/mongodb.html#Installing%20the%20MongoDB%20PHP%20Driver%20with%20PECL" class="link">PECL installation instructions</a>
using the <a href="/install/pecl.html" class="link">pecl</a> command
provided by the Homebrew PHP installation.

Installing the MongoDB PHP Driver on Windows
--------------------------------------------

Precompiled binaries for each release are available from
<a href="https://pecl.php.net/package/mongodb" class="link external">» PECL</a>
for a variety of combinations of versions, thread safety, and VC
libraries. Extract the archive and put `php_mongodb.dll` in your PHP
extension directory ("ext" by default).

Add the following line to your `php.ini` file:

``` ini
extension=php_mongodb.dll
```

> **Note**: **Additional DLL dependencies for Windows Users**  
>
> 为了使此扩展生效， DLL 文件必须能在 Windows 系统的 `PATH`
> 指示的路径下找到。如何操作的信息，请参见题为“<a href="/faq/installation.html#faq.installation.addtopath" class="link">如何在 Windows 中将 PHP 目录加到 PATH 中</a>”的FAQ。虽然将
> DLL 文件从 PHP 文件夹复制到 Windows 系统目录也行，但不建议这样做。
> *此扩展需要下列文件在 `PATH` 路径中：* `libsasl.dll`

Building the MongoDB PHP Driver from source
-------------------------------------------

For driver developers and people interested in the latest bugfixes, you
can compile the driver from the latest source code on
<a href="https://github.com/mongodb/mongo-php-driver-legacy" class="link external">» Github</a>.
Run the following commands to clone and build the project:

``` shell
$ git clone https://github.com/mongodb/mongo-php-driver.git
$ cd mongo-php-driver
$ git submodule update --init
$ phpize
$ ./configure
$ make all
$ sudo make install
```

If your system has multiple version of PHP installed (e.g. macOS default
*and*
<a href="https://www.apachefriends.org/" class="link external">» XAMPP</a>),
note that each version of PHP has its own
<a href="/install/pecl/phpize.html" class="link">phpize</a> command and
`php.ini` file.

By default, the driver will use bundled versions of
<a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>,
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>,
and
<a href="https://github.com/mongodb/libmongocrypt" class="link external">» libmongocrypt</a>
and attempt to configure them on its own. If these libraries are already
installed as system libraries, you can instruct the driver to utilize
them by specifying *--with-libbson=yes --with--libmongoc=yes* as
arguments to *configure*. Starting with version 1.7.0 of the extension,
these arguments are deprecated and you should use
*--with-mongodb-system-libs=yes* instead.

For a complete list of *configure* options, run **configure --help**.

When using bundled versions of libbson and libmongoc, the driver will
also attempt to select an SSL library according to the
*--with-mongodb-ssl* option for *configure*. The default value is
*--with-mongodb-ssl=auto*, which will search for Secure Transport (macOS
only), OpenSSL, and LibreSSL, in that order. Additionally, you may
specify *openssl*, *libressl*, or *darwin* to force selection of a
particular library, respectively.

> **Note**:
>
> If the build process fails to find an SSL library, check that the
> development packages (e.g. *libssl-dev*) and
> <a href="https://en.wikipedia.org/wiki/Pkg-config" class="link external">» pkg-config</a>
> are both installed.
>
> When using Homebrew on macOS, it is common for a system to have
> multiple versions of OpenSSL installed. To ensure that the desired
> version of OpenSSL is selected, the *PKG\_CONFIG\_PATH* environment
> variable may be used to control the search path for *pkg-config*. If
> *pkg-config* is not used, *configure* also supports a
> *--with-openssl-dir=DIR* argument, which can be used to specify a
> manual search path (for OpenSSL only).

The final build step, **make install**, will report where `mongodb.so`
has been installed, similar to:

``` txt
Installing shared extensions:     /usr/lib/php/extensions/debug-non-zts-20151012/
```

Ensure that the
<a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>
option in `php.ini` points to the directory where `mongodb.so` was
installed. You can query for the option by running:

``` shell
$ php -i | grep extension_dir
  extension_dir => /usr/lib/php/extensions/debug-non-zts-20151012 =>
                   /usr/lib/php/extensions/debug-non-zts-20151012
```

If the directories differ, either change
<a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>
in `php.ini` or manually move `mongodb.so` to the correct directory.

Finally, add the following line to your `php.ini` file:

``` ini
extension=mongodb.so
```

运行时配置
==========

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                        | 默认 | 可修改范围    | 更新日志 | Comments |
|-------------------------------------------------------------|------|---------------|----------|----------|
| <a href="/set/mongodb.html#" class="link">mongodb.debug</a> | ""   | PHP\_INI\_ALL |          |          |

这是配置指令的简短说明。

`mongodb.debug` <span class="type">string</span>  
Store full activity debug log in this directory or stream. The special
value "stderr" can be provided to write to STDERR.

> **Note**:
>
> Please note that the debug log can contain sensitive information, such
> as credentials to the MongoDB server and full documents written to or
> read from the server. Please review any debug logs before sharing them
> with other people.

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`MONGODB_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> x.y.z style version number of the extension
</span>

**`MONGODB_STABILITY`** (<span class="type">string</span>)  
<span class="simpara"> Current stability (alpha/beta/stable) </span>

Tutorials
=========

**目录**

-   [Using the PHP Library for MongoDB
    (PHPLIB)](/set/mongodb.html#Using%20the%20PHP%20Library%20for%20MongoDB%20(PHPLIB))
-   [Application Performance Monitoring
    (APM)](/set/mongodb.html#Application%20Performance%20Monitoring%20(APM))

In this section you will find several tutorials on how to use the
MongoDB driver for PHP.

Using the PHP Library for MongoDB (PHPLIB)
==========================================

After the initial driver set-up, we will continue explaining how to get
started with the MongoDB driver and corresponding userland library to
write our first project.

Installing the PHP Library with Composer
----------------------------------------

The last thing we still need to install to get started on the
application itself, is the PHP library.

The library needs to be installed with
<a href="https://getcomposer.org/" class="link external">» Composer</a>,
a package manager for PHP. Instructions for installing Composer on
various platforms may be found on its website.

Install the library by running:

``` shell
$ composer require mongodb/mongodb
```

It will output something akin to:

``` text
./composer.json has been created
Loading composer repositories with package information
Updating dependencies (including require-dev)
  - Installing mongodb/mongodb (1.0.0)
    Downloading: 100%         

Writing lock file
Generating autoload files
```

Composer will create several files: `composer.json`, `composer.lock`,
and a `vendor` directory that will contain the library and any other
dependencies your project might require.

Using the PHP Library
---------------------

In addition to managing your dependencies, Composer will also provide
you with an autoloader (for those dependencies' classes). Ensure that it
is included at the start of your script or in your application's
bootstrap code:

``` php
<?php
// This path should point to Composer's autoloader
require 'vendor/autoload.php';
```

With this done, you can now use any of the functionality as described in
the
<a href="https://docs.mongodb.com/php-library" class="link external">» library documentation</a>.

If you have previously used the old driver (i.e. `mongo` extension), the
library's API should look familiar. It contains a
<a href="https://docs.mongodb.com/php-library/master/reference/class/MongoDBClient/" class="link external">» Client</a>
class for connecting to MongoDB, and
<a href="https://docs.mongodb.com/php-library/master/reference/class/MongoDBDatabase/" class="link external">» Database</a>
class for database-level operations (e.g. commands, collection
management) and a
<a href="https://docs.mongodb.com/php-library/master/reference/class/MongoDBCollection" class="link external">» Collection</a>
class for collection-level operations (e.g.
<a href="https://en.wikipedia.org/wiki/Create,_read,_update_and_delete" class="link external">» CRUD</a>
methods, index management). Various Collection methods have been renamed
for clarity, and to be in accordance with a new language-agnostic
<a href="https://github.com/mongodb/specifications/blob/master/source/crud/crud.rst" class="link external">» specification</a>.

As an example, this is how you insert a document into the *beers*
collection of the *demo* database:

``` php
<?php
require 'vendor/autoload.php'; // include Composer's autoloader

$client = new MongoDB\Client("mongodb://localhost:27017");
$collection = $client->demo->beers;

$result = $collection->insertOne( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );

echo "Inserted with Object ID '{$result->getInsertedId()}'";
?>
```

Instead of injecting the generated `_id` field into the input document
(as was done in the old driver), it is now made available through the
result object returned by the `insertOne` method.

After insertion, you can of course also query the data that you have
just inserted. For that, you use the `find` method, which returns an
iterable cursor:

``` php
<?php
require 'vendor/autoload.php'; // include Composer's autoloader

$client = new MongoDB\Client("mongodb://localhost:27017");
$collection = $client->demo->beers;

$result = $collection->find( [ 'name' => 'Hinterland', 'brewery' => 'BrewDog' ] );

foreach ($result as $entry) {
    echo $entry['_id'], ': ', $entry['name'], "\n";
}
?>
```

While it may not be apparent in the examples, BSON documents and arrays
are unserialized as type classes in the library by default. These
classes ensure that values preserve their type when being serialized
back into BSON, which avoids a caveat in the old driver where arrays
might turn into documents, and vice versa. Additionally, the classes
extend <span class="classname">ArrayObject</span> for enhanced
usability. You can find more information on how serialization and
deserialization between PHP variables and BSON is handled by the driver
and library by reading the
<a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>
specification.

Application Performance Monitoring (APM)
========================================

Since version 1.3, the MongoDB driver contains an API for performance
monitoring. This API allows you to find out how long specific operations
take by setting up subscribers. Each subscriber is required to implement
one or more interfaces under the *MongoDB\\Driver\\Monitoring*
namespace. Currently, only the <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandSubscriber</span>
interface is available.

The <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandSubscriber</span>
interface defines three methods: *commandStarted*, *commandSucceeded*,
and *commandFailed*. Each of these three methods accept a single `event`
argument of a specific class for the respective event. For example, the
*commandSucceeded*'s `$event` argument is a <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>
object.

In this tutorial we will implement a subscriber that creates a list of
all the query profiles and the average time they took.

Subscriber Class Scaffolding
----------------------------

We start with the framework for our subscriber:

``` php
<?php

class QueryTimeCollector implements \MongoDB\Driver\Monitoring\CommandSubscriber
{
    public function commandStarted( \MongoDB\Driver\Monitoring\CommandStartedEvent $event )
    {
    }

    public function commandSucceeded( \MongoDB\Driver\Monitoring\CommandSucceededEvent $event )
    {
    }

    public function commandFailed( \MongoDB\Driver\Monitoring\CommandFailedEvent $event )
    {
    }
}

?>
```

Registering the Subscriber
--------------------------

Once a subscriber object is instantiated, it needs to be registered with
the driver's monitoring system. This is done by calling <span
class="methodname">MongoDB\\Driver\\Monitoring\\addSubscriber</span>.

``` php
<?php

\MongoDB\Driver\Monitoring\addSubscriber( new QueryTimeCollector() );

?>
```

Implementing the Logic
----------------------

With the object registered, the only thing left is to implement the
logic in the subscriber class. To correlate the two events that make up
a successfully executed command (commandStarted and commandSucceeded),
each event object exposes a *requestId* field.

To record the average time per query shape, we will start by checking
for a *find* command in the commandStarted event. We will then add an
item to the *pendingCommands* property indexed by its *requestId* and
with its value representing the query shape.

If we receive a corresponding commandSucceeded event with the same
*requestId*, we add the duration of the event (from *durationMicros*) to
the total time and increment the operation count.

If a corresponding commandFailed event is encountered, we just remove
the entry from the *pendingCommands* property.

``` php
<?php

class QueryTimeCollector implements \MongoDB\Driver\Monitoring\CommandSubscriber
{
    private $pendingCommands = [];
    private $queryShapeStats = [];

    /* Creates a query shape out of the filter argument. Right now it only
     * takes the top level fields into account */
    private function createQueryShape( array $filter )
    {
        return json_encode( array_keys( $filter ) );
    }

    public function commandStarted( \MongoDB\Driver\Monitoring\CommandStartedEvent $event )
    {
        if ( array_key_exists( 'find', (array) $event->getCommand() ) )
        {
            $queryShape = $this->createQueryShape( (array) $event->getCommand()->filter );
            $this->pendingCommands[$event->getRequestId()] = $queryShape;
        }
    }

    public function commandSucceeded( \MongoDB\Driver\Monitoring\CommandSucceededEvent $event )
    {
        $requestId = $event->getRequestId();
        if ( array_key_exists( $requestId, $this->pendingCommands ) )
        {
            $this->queryShapeStats[$this->pendingCommands[$requestId]]['count']++;
            $this->queryShapeStats[$this->pendingCommands[$requestId]]['duration'] += $event->getDurationMicros();
            unset( $this->pendingCommands[$requestId] );
        }
    }

    public function commandFailed( \MongoDB\Driver\Monitoring\CommandFailedEvent $event )
    {
        if ( array_key_exists( $event->getRequestId(), $this->pendingCommands ) )
        {
            unset( $this->pendingCommands[$event->getRequestId()] );
        }
    }

    public function __destruct()
    {
        foreach( $this->queryShapeStats as $shape => $stats )
        {
            echo "Shape: ", $shape, " (", $stats['count'], ")\n  ",
                $stats['duration'] / $stats['count'], "µs\n\n";
        }
    }
}

$m = new \MongoDB\Driver\Manager( 'mongodb://localhost:27016' );

/* Add the subscriber */
\MongoDB\Driver\Monitoring\addSubscriber( new QueryTimeCollector() );

/* Do a bunch of queries */
$query = new \MongoDB\Driver\Query( [
    'region_slug' => 'scotland-highlands', 'age' => [ '$gte' => 20 ]
] );
$cursor = $m->executeQuery( 'dramio.whisky', $query );

$query = new \MongoDB\Driver\Query( [
    'region_slug' => 'scotland-lowlands', 'age' => [ '$gte' => 15 ]
] );
$cursor = $m->executeQuery( 'dramio.whisky', $query );

$query = new \MongoDB\Driver\Query( [ 'region_slug' => 'scotland-lowlands' ] );
$cursor = $m->executeQuery( 'dramio.whisky', $query );

?>
```

Explains the driver architecture, and special features
======================================================

**目录**

-   [Architecture](/set/mongodb.html#Architecture) — Architecture
    Overview
-   [Connections](/set/mongodb.html#Connections) — Connection handling
    and persistence
-   [Persisting Data](/set/mongodb.html#Persisting%20Data) —
    Serialization and deserialization of PHP variables into MongoDB
    -   [Serialization to
        BSON](/set/mongodb.html#Serialization%20to%20BSON)
    -   [Deserialization from
        BSON](/set/mongodb.html#Deserialization%20from%20BSON)

Architecture Overview
=====================

This section explains how all the different parts of the driver fit
together. From the different language runtimes, through the extension
and to the PHP libraries on top. This new architecture has replaced the
old <a href="/book/mongo.html" class="link">mongo</a> extension. We
refer to the new one as the *mongodb* extension.

<img src="images/f3bc48edf40d5e3e09a166c7fadc7efb-driver_arch.png" width="625" height="450" alt="Architecture Diagram" />

At the top of this stack sits a pure
<a href="https://github.com/mongodb/mongo-php-library" class="link external">» PHP library</a>,
which we will distribute as a Composer package. This library will
provide an API similar to what users have come to expect from the old
mongo driver (e.g. CRUD methods, database and collection objects,
command helpers) and we expect it to be a common dependency for most
applications built with MongoDB. This library will also implement common
<a href="https://github.com/mongodb/specifications" class="link external">» specifications</a>,
in the interest of improving API consistency across all of the
<a href="https://docs.mongodb.com/ecosystem/drivers/" class="link external">» drivers</a>
maintained by MongoDB (and hopefully some community drivers, too).

Sitting below that library we have the lower level driver. This
extension will effectively form the glue between PHP and our system
libraries
(<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
and
<a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>).
This extension will expose an identical public API for the most
essential and performance-sensitive functionality:

-   Connection management
-   BSON encoding and decoding
-   Object document serialization (to support ODM libraries)
-   Executing commands and write operations
-   Handling queries and cursors

By decoupling the driver internals and a high-level API into an
extension and PHP libraries, respectively, we hope to reduce our
maintainence burden and allow for faster iteration on new features. As a
welcome side effect, this also makes it easier for anyone to contribute
to the driver. Additionally, an identical public API will make it that
much easier to port an application across PHP runtimes, whether the
application uses the low-level driver directly or a higher-level PHP
library.

<a href="https://docs.mongodb.com/manual/core/gridfs/" class="link external">» GridFS</a>
is a great example of why we chose this direction. Although we
implemented GridFS in C for our old mongo driver, it is actually quite a
high-level specification. Its API is just an abstraction for accessing
two collections: files (i.e. metadata) and chunks (i.e. blocks of data).
Likewise, all of the syntactic sugar found in the old mongo driver, such
as processing uploaded files or exposing GridFS files as PHP streams,
can be implemented in pure PHP. Provided we have performant methods for
reading from and writing to GridFS' collections – and thanks to our low
level extensions, we will – shifting this API to PHP is win-win.

Earlier I mentioned that we expect the PHP library to be a common
dependency for *most* applications, but not *all*. Some users may prefer
to stick to the no-frills API offered by the extensions, or create their
own high-level abstraction (akin to
<a href="https://github.com/doctrine/mongodb" class="link external">» Doctrine MongoDB</a>
for the old mongo driver). Future libraries could include a PHP library
geared for MongoDB administration, which provides an API for various
user management and ops commands. The next major version of
<a href="https://github.com/doctrine/mongodb-odm" class="link external">» Doctrine MongoDB ODM</a>
will likely also sit directly atop the extensions.

While we will continue to maintain and support the old mongo driver and
its users for the foreseeable future, we invite everyone to use the
next-generation driver and consider it for any new projects going
forward. You can find all of the essential components across GitHub and
JIRA:

| Project                         | GitHub                                                                                                       | JIRA                                                                                |
|---------------------------------|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| PHP Library                     | <a href="https://github.com/mongodb/mongo-php-library" class="link external">» mongodb/mongo-php-library</a> | <a href="https://jira.mongodb.org/browse/PHPLIB" class="link external">» PHPLIB</a> |
| PHP 5 and PHP 7 Driver (phongo) | <a href="https://github.com/mongodb/mongo-php-driver" class="link external">» mongodb/mongo-php-driver</a>   | <a href="https://jira.mongodb.org/browse/PHPC" class="link external">» PHPC</a>     |

The existing
<a href="https://jira.mongodb.org/browse/PHP" class="link external">» PHP</a>
project in JIRA will remain open for reporting bugs against the old
mongo driver, but we would ask that you use the new projects above for
anything pertaining to our next-generation drivers.

Connection handling and persistence
===================================

> **Note**: <span class="simpara"> On Unix platforms, the MongoDB driver
> is sensitive to scripts that use the fork() system call without also
> calling exec(). Users are advised not to re-use <span
> class="classname">MongoDB\\Driver\\Manager</span> instances in a
> forked child process. </span>

Connection and topology persistence (PHP version since 1.2.0)
-------------------------------------------------------------

All versions of the driver since 1.2.0 persist the
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
client object in the PHP worker process, which allows it to re-use
database connections, authentication states, *and* topology information
across multiple requests.

When <span
class="methodname">MongoDB\\Driver\\Manager::\_\_construct</span> is
invoked, a hash is created from its arguments (i.e. URI string and array
options). The driver will attempt to find a previously persisted
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
client object for that hash. If an existing client cannot be found for
the hash, a new client will be created (and persisted for future use).

Each client contains its own database connections and a view of the
server topology (e.g. standalone, replica set, shard cluster). By
persisting the client between PHP requests, the driver is able to re-use
established database connections and remove the need for
<a href="https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst" class="link external">» discovering the server topology</a>
on each request.

Consider the following example:

``` php
<?php

$managers = [
    new MongoDB\Driver\Manager('mongodb://127.0.0.1'),
    new MongoDB\Driver\Manager('mongodb://127.0.0.1'),
    new MongoDB\Driver\Manager('mongodb://127.0.0.1:27017'),
    new MongoDB\Driver\Manager('mongodb://rs1.example.com,rs2.example.com/', ['replicaSet' => 'myReplicaSet']),
];

foreach ($managers as $manager) {
    $manager->executeCommand('test', new MongoDB\Driver\Command(['ping' => 1]));
}

?>
```

The first two Manager objects will share the same
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
client since their constructor arguments are identical. The third and
fourth objects will each use their own client. In total, three clients
will be created and the PHP worker executing this script will open two
connections to *127.0.0.1* and one connection to each of
*rs1.example.com* and *rs2.example.com*. If the driver discovers
additional members of the replica set after issuing *isMaster* commands,
it will open additional connections to those servers as well.

If the same worker executes the script again in a second request, the
three clients will be re-used and no new connections should be made.
Depending on how long ago the previous request was served, the driver
may need to issue additional *isMaster* commands to update its view of
the topologies.

Socket persistence (PHP versions before 1.2.0)
----------------------------------------------

Versions of the PHP driver before 1.2.0 utilize PHP's Streams API for
database connections, using an API within
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>
to designate custom handlers for socket communication; however, a new
libmongoc client is created for each <span
class="classname">MongoDB\\Driver\\Manager</span>. As a result, the
driver persists individual database connections but not authentication
state or topology information. This means that the driver needs to issue
commands at the start of each request to authenticate and
<a href="https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst" class="link external">» discover the server topology</a>.

Database connections are persisted by a hash derived from the server's
host, port, and the URI string used to construct the <span
class="classname">MongoDB\\Driver\\Manager</span>. The constructor's
array options are not included in this hash.

> **Note**: <span class="simpara"> Versions of the driver \>= 1.1.8 and
> \< 1.2.0 do not persist sockets for SSL connections. See
> <a href="https://jira.mongodb.org/browse/PHPC-720" class="link external">» PHPC-720</a>
> for additional information. </span>

Despite its shortcomings with persisting SSL connections when and
topology information, this version of the driver supports all
<a href="/context/ssl.html" class="link">SSL context options</a> since
it uses PHP's Streams API.

Serialization and deserialization of PHP variables into MongoDB
===============================================================

**目录**

-   [Serialization to BSON](/set/mongodb.html#Serialization%20to%20BSON)
-   [Deserialization from
    BSON](/set/mongodb.html#Deserialization%20from%20BSON)

This document discusses the methods how compound structures (documents,
arrays, objects) are persisted through the drivers. And how they are
brought back into PHP land.

Serialization to BSON
---------------------

Arrays
------

If an array is a *packed array* — i.e. the keys start at 0 and are
sequential without gaps: *BSON array*.

If the array is not packed — i.e. having associative (string) keys, the
keys don't start at 0, or when there are gaps:: *BSON object*

A top-level (root) document, *always* serializes as a BSON document.

Examples
--------

These serialize as a BSON array:

``` text
[ 8, 5, 2, 3 ] => [ 8, 5, 2, 3 ]
[ 0 => 4, 1 => 9 ] => [ 4, 9 ]
```

These serialize as a BSON document:

``` text
[ 0 => 1, 2 => 8, 3 => 12 ] => { "0" : 1, "2" : 8, "3" : 12 }
[ "foo" => 42 ] => { "foo" : 42 }
[ 1 => 9, 0 => 10 ] => { "1" : 9, "0" : 10 }
```

Note that the five examples are *extracts* of a full document, and
represent only *one* value inside a document.

Objects
-------

If an object is of the <span class="classname">stdClass</span> class,
serialize as a *BSON document*.

If an object is a supported class that implements <span
class="interfacename">MongoDB\\BSON\\Type</span>, then use the BSON
serialization logic for that specific type. <span
class="interfacename">MongoDB\\BSON\\Type</span> instances (excluding
<span class="interfacename">MongoDB\\BSON\\Serializable</span> may only
be serialized as a document field value. Attempting to serialize such an
object as a root document will throw a <span
class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>

If an object is of an unknown class implementing the <span
class="interfacename">MongoDB\\BSON\\Type</span> interface, then throw a
<span
class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>

If an object is of any other class, without implementing any special
interface, serialize as a *BSON document*. Keep only *public*
properties, and ignore *protected* and *private* properties.

If an object is of a class that implements the <span
class="interfacename">MongoDB\\BSON\\Serializable</span> interface, call
<span
class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span> and
use the returned array or <span class="classname">stdClass</span> to
serialize as a BSON document or array. The BSON type will be determined
by the following:

1.  Root documents must be serialized as a BSON document.

2.  <span class="interfacename">MongoDB\\BSON\\Persistable</span>
    objects must be serialized as a BSON document.

3.  If <span
    class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
    returns a packed array, serialize as a BSON array.

4.  If <span
    class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
    returns a non-packed array or <span
    class="classname">stdClass</span>, serialize as a BSON document.

5.  If <span
    class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
    did not return an array or <span class="classname">stdClass</span>,
    throw an <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    exception.

If an object is of a class that implements the <span
class="interfacename">MongoDB\\BSON\\Persistable</span> interface (which
implies <span class="interfacename">MongoDB\\BSON\\Serializable</span>),
obtain the properties in a similar way as in the previous paragraphs,
but *also* add an additional property <span
class="property">\_\_pclass</span> as a Binary value, with subtype
*0x80* and data bearing the fully qualified class name of the object
that is being serialized.

The <span class="property">\_\_pclass</span> property is added to the
array or object returned by <span
class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>,
which means it will overwrite any <span
class="property">\_\_pclass</span> key/property in the <span
class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
return value. If you want to avoid this behaviour and set your own <span
class="property">\_\_pclass</span> value, you must *not* implement <span
class="interfacename">MongoDB\\BSON\\Persistable</span> and should
instead implement <span
class="interfacename">MongoDB\\BSON\\Serializable</span> directly.

Examples
--------

``` php
<?php

class stdClass {
  public $foo = 42;
} // => { "foo" : 42 }

class MyClass {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
} // => { "foo" : 42 }

class AnotherClass1 implements MongoDB\BSON\Serializable {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
  function bsonSerialize() {
      return [ 'foo' => $this->foo, 'prot' => $this->prot ];
  }
} // => { "foo" : 42, "prot" : "wine" }

class AnotherClass2 implements MongoDB\BSON\Serializable {
  public $foo = 42;
  function bsonSerialize() {
      return $this;
  }
} // => MongoDB\Driver\Exception\UnexpectedValueException("bsonSerialize() did not return an array or stdClass")

class AnotherClass3 implements MongoDB\BSON\Serializable {
  private $elements = [ 'foo', 'bar' ];
  function bsonSerialize() {
      return $this->elements;
  }
} // => { "0" : "foo", "1" : "bar" }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass4 implements MongoDB\BSON\Serializable {
    private $elements = [ 0 => 'foo', 2 => 'bar' ];
    function bsonSerialize() {
      return $this->elements;
    }
  }
  function bsonSerialize() {
      return [ 'things' => $this->things ];
  }
} // => { "things" : { "0" : "foo", "2" : "bar" } }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass5 implements MongoDB\BSON\Serializable {
    private $elements = [ 0 => 'foo', 2 => 'bar' ];
    function bsonSerialize() {
      return array_values($this->elements);
    }
  }
  function bsonSerialize() {
      return [ 'things' => $this->things ];
  }
} // => { "things" : [ "foo", "bar" ] }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass6 implements MongoDB\BSON\Serializable {
    private $elements = [ 'foo', 'bar' ];
    function bsonSerialize() {
      return (object) $this->elements;
    }
  }
  function bsonSerialize() {
      return [ 'things' => $this->things ];
  }
} // => { "things" : { "0" : "foo", "1" : "bar" } }

class UpperClass implements MongoDB\BSON\Persistable {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
  function bsonSerialize() {
      return [ 'foo' => $this->foo, 'prot' => $this->prot ];
  }
} // => { "foo" : 42, "prot" : "wine", "__pclass" : { "$type" : "80", "$binary" : "VXBwZXJDbGFzcw==" } }
```

Deserialization from BSON
-------------------------

The legacy <a href="/book/mongo.html" class="link">mongo</a> extension
deserialized both BSON documents and arrays as PHP arrays. While PHP
arrays are convenient to work with, this behavior was problematic
because different BSON types could deserialize to the same PHP value
(e.g. *{"0": "foo"}* and *\["foo"\]*) and make it impossible to infer
the original BSON type. By default, the current driver addresses this
concern by ensuring that BSON arrays and documents are converted to PHP
arrays and objects, respectively.

For compound types, there are three data types:

root  
refers to the top-level BSON document *only*

document  
refers to embedded BSON documents *only*

array  
refers to a BSON array

Besides the three collective types, it is also possible to configure
specific fields in your document to map to the data types mentioned
below. As an example, the following type map allows you to map each
embedded document within an *"addresses"* array to an <span
class="classname">Address</span> class *and* each *"city"* field within
those embedded address documents to a <span
class="classname">City</span> class:

``` text
[
    'fieldPaths' => [
        'addresses.$' => 'MyProject\Address',
        'addresses.$.city' => 'MyProject\City',
    ],
]
```

Each of those three data types, as well as the field specific mappings,
can be mapped against different PHP types. The possible mapping values
are:

*not set* or <span class="type">NULL</span> (default)  
-   A BSON array will be deserialized as a PHP <span
    class="type">array</span>.

-   A BSON document (root or embedded) without a <span
    class="property">\_\_pclass</span> property
    <a href="#fnidmongodb.pclass" id="fnmongodb.pclass"><sup>[1]</sup></a>
    becomes a PHP <span class="classname">stdClass</span> object, with
    each BSON document key set as a public <span
    class="classname">stdClass</span> property.

-   A BSON document (root or embedded) with a <span
    class="property">\_\_pclass</span> property
    [<sup>\[1\]</sup>](#fnidmongodb.pclass) becomes a PHP object of the
    class name as defined by the <span
    class="property">\_\_pclass</span> property.

    If the named class implements the <span
    class="interfacename">MongoDB\\BSON\\Persistable</span> interface,
    then the properties of the BSON document, including the <span
    class="property">\_\_pclass</span> property, are sent as an
    associative array to the <span
    class="methodname">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
    function to initialise the object's properties.

    If the named class does not exist or does not implement the <span
    class="interfacename">MongoDB\\BSON\\Persistable</span> interface,
    <span class="classname">stdClass</span> will be used and each BSON
    document key (including <span class="property">\_\_pclass</span>)
    will be set as a public <span class="classname">stdClass</span>
    property.

    The <span class="property">\_\_pclass</span> functionality relies on
    the property being part of a retrieved MongoDB document. If you use
    a
    <a href="/set/mongodb.html#queryOptions" class="link">projection</a>
    when querying for documents, you need to include the <span
    class="property">\_\_pclass</span> field in the projection for this
    functionality to work.

*"array"*  
Turns a BSON array or BSON document into a PHP array. There will be no
special treatment of a <span class="property">\_\_pclass</span> property
[<sup>\[1\]</sup>](#fnidmongodb.pclass), but it may be set as an element
in the returned array if it was present in the BSON document.

*"object"* or *"stdClass"*  
Turns a BSON array or BSON document into a <span
class="classname">stdClass</span> object. There will be no special
treatment of a <span class="property">\_\_pclass</span> property
[<sup>\[1\]</sup>](#fnidmongodb.pclass), but it may be set as a public
property in the returned object if it was present in the BSON document.

any other string  
Defines the class name that the BSON array or BSON object should be
deserialized as. For BSON objects that include <span
class="property">\_\_pclass</span> properties, that class will take
priority.

If the named class does not exist, is not concrete (i.e. it is abstract
or an interface), or does not implement <span
class="interfacename">MongoDB\\BSON\\Unserializable</span> then an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
exception is thrown.

If the BSON object has a <span class="property">\_\_pclass</span>
property and that class exists and implements <span
class="interfacename">MongoDB\\BSON\\Persistable</span> it will
supersede the class provided in the type map.

The properties of the BSON document, *including* the <span
class="property">\_\_pclass</span> property if it exists, will be sent
as an associative array to the <span
class="methodname">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
function to initialise the object's properties.

TypeMaps
--------

TypeMaps can be set through the <span
class="methodname">MongoDB\\Driver\\Cursor::setTypeMap</span> method on
a <span class="classname">MongoDB\\Driver\\Cursor</span> object, or the
*$typeMap* argument of <span
class="function">MongoDB\\BSON\\toPHP</span>. Each of the three classes
(*root*, *document*, and *array*) can be individually set, in addition
to the field specific types.

If the value in the map is <span class="type">NULL</span>, it means the
same as the *default* value for that item.

Examples
--------

These examples use the following classes:

MyClass  
which does *not* implement any interface

YourClass  
which implements <span
class="interfacename">MongoDB\\BSON\\Unserializable</span>

OurClass  
which implements <span
class="interfacename">MongoDB\\BSON\\Persistable</span>

TheirClass  
which extends OurClass

The <span
class="methodname">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
method of YourClass, OurClass, TheirClass iterate over the array and set
the properties without modifications. It *also* sets the *$unserialized*
property to *true*:

``` php
<?php

function bsonUnserialize( array $map )
{
    foreach ( $map as $k => $value )
    {
        $this->$k = $value;
    }
    $this->unserialized = true;
}
```

``` text
/* typemap: [] (all defaults) */
{ "foo": "yes", "bar" : false }
  -> stdClass { $foo => 'yes', $bar => false }

{ "foo": "no", "array" : [ 5, 6 ] }
  -> stdClass { $foo => 'no', $array => [ 5, 6 ] }

{ "foo": "no", "obj" : { "embedded" : 3.14 } }
  -> stdClass { $foo => 'no', $obj => stdClass { $embedded => 3.14 } }

{ "foo": "yes", "__pclass": "MyClass" }
  -> stdClass { $foo => 'yes', $__pclass => 'MyClass' }

{ "foo": "yes", "__pclass": { "$type" : "80", "$binary" : "MyClass" } }
  -> stdClass { $foo => 'yes', $__pclass => Binary(0x80, 'MyClass') }

{ "foo": "yes", "__pclass": { "$type" : "80", "$binary" : "YourClass") }
  -> stdClass { $foo => 'yes', $__pclass => Binary(0x80, 'YourClass') }

{ "foo": "yes", "__pclass": { "$type" : "80", "$binary" : "OurClass") }
  -> OurClass { $foo => 'yes', $__pclass => Binary(0x80, 'OurClass'), $unserialized => true }

{ "foo": "yes", "__pclass": { "$type" : "44", "$binary" : "YourClass") }
  -> stdClass { $foo => 'yes', $__pclass => Binary(0x44, 'YourClass') }
```

``` text
/* typemap: [ "root" => "MissingClass" ] */
{ "foo": "yes" }
  -> MongoDB\Driver\Exception\InvalidArgumentException("MissingClass does not exist")

/* typemap: [ "root" => "MyClass" ] */
{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "MyClass" } }
  -> MongoDB\Driver\Exception\InvalidArgumentException("MyClass does not implement Unserializable interface")

/* typemap: [ "root" => "MongoDB\BSON\Unserializable" ] */
{ "foo": "yes" }
  -> MongoDB\Driver\Exception\InvalidArgumentException("Unserializable is not a concrete class")

/* typemap: [ "root" => "YourClass" ] */
{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "MongoDB\BSON\Unserializable" } }
  -> YourClass { $foo => "yes", $__pclass => Binary(0x80, "MongoDB\BSON\Unserializable"), $unserialized => true }

/* typemap: [ "root" => "YourClass" ] */
{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "MyClass" } }
  -> YourClass { $foo => "yes", $__pclass => Binary(0x80, "MyClass"), $unserialized => true }

/* typemap: [ "root" => "YourClass" ] */
{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "OurClass" } }
  -> OurClass { $foo => "yes", $__pclass => Binary(0x80, "OurClass"), $unserialized => true }

/* typemap: [ "root" => "YourClass" ] */
{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "TheirClass" } }
  -> TheirClass { $foo => "yes", $__pclass => Binary(0x80, "TheirClass"), $unserialized => true }

/* typemap: [ "root" => "OurClass" ] */
{ foo: "yes", "__pclass" : { "$type": "80", "$binary": "TheirClass" } }
  -> TheirClass { $foo => "yes", $__pclass => Binary(0x80, "TheirClass"), $unserialized => true }
```

``` text
/* typemap: [ 'root' => 'YourClass' ] */
{ foo: "yes", "__pclass" : { "$type": "80", "$binary": "YourClass" } }
  -> YourClass { $foo => 'yes', $__pclass => Binary(0x80, 'YourClass'), $unserialized => true }
```

``` text
/* typemap: [ 'root' => 'array', 'document' => 'array' ] */
{ "foo": "yes", "bar" : false }
  -> [ "foo" => "yes", "bar" => false ]

{ "foo": "no", "array" : [ 5, 6 ] }
  -> [ "foo" => "no", "array" => [ 5, 6 ] ]

{ "foo": "no", "obj" : { "embedded" : 3.14 } }
  -> [ "foo" => "no", "obj" => [ "embedded => 3.14 ] ]

{ "foo": "yes", "__pclass": "MyClass" }
  -> [ "foo" => "yes", "__pclass" => "MyClass" ]

{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "MyClass" } }
  -> [ "foo" => "yes", "__pclass" => Binary(0x80, "MyClass") ]

{ "foo": "yes", "__pclass" : { "$type": "80", "$binary": "OurClass" } }
  -> [ "foo" => "yes", "__pclass" => Binary(0x80, "OurClass") ]
```

``` text
/* typemap: [ 'root' => 'object', 'document' => 'object' ] */
{ "foo": "yes", "__pclass": { "$type": "80", "$binary": "MyClass" } }
  -> stdClass { $foo => "yes", "__pclass" => Binary(0x80, "MyClass") }
```

<a href="#fnmongodb.pclass" id="fnidmongodb.pclass"><sup>[1]</sup></a><span
class="para footnote"> A \_\_pclass property is only deemed to exist if
there exists a property with that name, and it is a Binary value, and
the sub-type of the Binary value is 0x80. If any of these three
conditions is not met, the \_\_pclass property does not exist and should
be treated as any other normal property. </span>

Security
========

**目录**

-   [Request Injection
    Attacks](/set/mongodb.html#Request%20Injection%20Attacks)
-   [Script Injection
    Attacks](/set/mongodb.html#Script%20Injection%20Attacks)

Request Injection Attacks
=========================

If you are passing *$\_GET* (or *$\_POST*) parameters to your queries,
make sure that they are cast to strings first. Users can insert
associative arrays in GET and POST requests, which could then become
unwanted $-queries.

A fairly innocuous example: suppose you are looking up a user's
information with the request *http://www.example.com?username=bob*. Your
application creates the query *$q = new \\MongoDB\\Driver\\Query( \[
'username' =\> $\_GET\['username'\] \])*.

Someone could subvert this by getting
*http://www.example.com?username\[$ne\]=foo*, which PHP will magically
turn into an associative array, turning your query into *$q = new
\\MongoDB\\Driver\\Query( \[ 'username' =\> \[ '$ne' =\> 'foo' \] \] )*,
which will return all users not named "foo" (all of your users,
probably).

This is a fairly easy attack to defend against: make sure $\_GET and
$\_POST parameters are the type you expect before you send them to the
database. PHP has the <span class="function">filter\_var</span> function
to assist with this.

Note that this type of attack can be used with any database interaction
that locates a document, including updates, upserts, deletes, and
findAndModify commands.

See
<a href="https://docs.mongodb.com/manual/security/" class="link external">» the main documentation</a>
for more information about SQL-injection-like issues with MongoDB.

Script Injection Attacks
========================

If you are using JavaScript, make sure that any variables that cross the
PHP- to-JavaScript boundry are passed in the *scope* field of <span
class="classname">MongoDB\\BSON\\Javascript</span>, not interpolated
into the JavaScript string. This can come up when using *$where* clauses
in queries, mapReduce and group commands, and any other time you may
pass JavaScript into the database.

For example, suppose we have some JavaScript to greet a user in the
database logs. We could do:

``` php
<?php
$m = new MongoDB\Driver\Manager;

// Don't do this!!!
$username = $_GET['field']; 

$cmd = new \MongoDB\Driver\Command( [
    'eval' => "print('Hello, $username!');"
] );

$r = $m->executeCommand( 'dramio', $cmd );
?>
```

However, what if a malicious user passes in some JavaScript?

``` php
<?php
$m = new MongoDB\Driver\Manager;

// Don't do this!!!
$username = $_GET['field']; 
// $username is set to "'); db.users.drop(); print('"

$cmd = new \MongoDB\Driver\Command( [
    'eval' => "print('Hello, $username!');"
] );

$r = $m->executeCommand( 'dramio', $cmd );
?>
```

Now MongoDB executes the JavaScript string *"print('Hello, ');
db.users.drop(); print('!');"*. This attack is easy to avoid: use *args*
to pass variables from PHP to JavaScript:

``` php
<?php
$m = new MongoDB\Driver\Manager;

$_GET['field'] = 'derick';
$args = [ $_GET['field'] ];

$cmd = new \MongoDB\Driver\Command( [
    'eval' => "function greet(username) { print('Hello, ' + username + '!'); }",
    'args' => $args,
] );

$r = $m->executeCommand( 'dramio', $cmd );
?>
```

This adds an argument to the JavaScript scope, which gets used as
argument for the *greet* function. Now if someone tries to send
malicious code, MongoDB will harmlessly print *Hello, ');
db.dropDatabase(); print('!*.

Using arguments helps to prevent malicious input from being executed by
the database. However, you must make sure that your code does not turn
around and execute the input anyway! It is best to avoid executing *any*
JavaScript on the server in the first place.

You are strongly recommended to stay clear of the
<a href="https://docs.mongodb.com/manual/reference/operator/query/where/#considerations" class="link external">» $where clause</a>
with queries, as it impacts performance significantly. Where possible,
use either normal query operators, or the
<a href="https://docs.mongodb.com/manual/core/aggregation-pipeline" class="link external">» Aggregation Framework</a>.

As alternative to
<a href="https://docs.mongodb.com/manual/core/map-reduce/" class="link external">» MapReduce</a>,
which uses JavaScript, consider using the
<a href="https://docs.mongodb.com/manual/core/aggregation-pipeline" class="link external">» Aggregation Framework</a>.
Unlike Map/Reduce, it uses an idiomatic language to construct queries,
without having to write, and use, the slower JavaScript approach that
Map/Reduce requires.

The
<a href="https://docs.mongodb.com/manual/reference/command/eval/" class="link external">» eval command</a>
has been deprecated since MongoDB 3.0, and should also be avoided.

MongoDB 驱动类
==============

**目录**

-   [MongoDB\\Driver\\Manager](/set/mongodb.html#MongoDB\Driver\Manager)
    — The MongoDB\\Driver\\Manager class
    -   [MongoDB\\Driver\\Manager::\_\_construct](/set/mongodb.html#MongoDB\Driver\Manager::__construct)
        — Create new MongoDB Manager
    -   [MongoDB\\Driver\\Manager::createClientEncryption](/set/mongodb.html#MongoDB\Driver\Manager::createClientEncryption)
        — Create a new ClientEncryption object
    -   [MongoDB\\Driver\\Manager::executeBulkWrite](/set/mongodb.html#MongoDB\Driver\Manager::executeBulkWrite)
        — Execute one or more write operations
    -   [MongoDB\\Driver\\Manager::executeCommand](/set/mongodb.html#MongoDB\Driver\Manager::executeCommand)
        — Execute a database command
    -   [MongoDB\\Driver\\Manager::executeQuery](/set/mongodb.html#MongoDB\Driver\Manager::executeQuery)
        — Execute a database query
    -   [MongoDB\\Driver\\Manager::executeReadCommand](/set/mongodb.html#MongoDB\Driver\Manager::executeReadCommand)
        — Execute a database command that reads
    -   [MongoDB\\Driver\\Manager::executeReadWriteCommand](/set/mongodb.html#MongoDB\Driver\Manager::executeReadWriteCommand)
        — Execute a database command that reads and writes
    -   [MongoDB\\Driver\\Manager::executeWriteCommand](/set/mongodb.html#MongoDB\Driver\Manager::executeWriteCommand)
        — Execute a database command that writes
    -   [MongoDB\\Driver\\Manager::getReadConcern](/set/mongodb.html#MongoDB\Driver\Manager::getReadConcern)
        — Return the ReadConcern for the Manager
    -   [MongoDB\\Driver\\Manager::getReadPreference](/set/mongodb.html#MongoDB\Driver\Manager::getReadPreference)
        — Return the ReadPreference for the Manager
    -   [MongoDB\\Driver\\Manager::getServers](/set/mongodb.html#MongoDB\Driver\Manager::getServers)
        — Return the servers to which this manager is connected
    -   [MongoDB\\Driver\\Manager::getWriteConcern](/set/mongodb.html#MongoDB\Driver\Manager::getWriteConcern)
        — Return the WriteConcern for the Manager
    -   [MongoDB\\Driver\\Manager::selectServer](/set/mongodb.html#MongoDB\Driver\Manager::selectServer)
        — Select a server matching a read preference
    -   [MongoDB\\Driver\\Manager::startSession](/set/mongodb.html#MongoDB\Driver\Manager::startSession)
        — Start a new client session for use with this client
-   [MongoDB\\Driver\\Command](/set/mongodb.html#MongoDB\Driver\Command)
    — The MongoDB\\Driver\\Command class
    -   [MongoDB\\Driver\\Command::\_\_construct](/set/mongodb.html#MongoDB\Driver\Command::__construct)
        — Create a new Command
-   [MongoDB\\Driver\\Query](/set/mongodb.html#MongoDB\Driver\Query) —
    The MongoDB\\Driver\\Query class
    -   [MongoDB\\Driver\\Query::\_\_construct](/set/mongodb.html#MongoDB\Driver\Query::__construct)
        — Create a new Query
-   [MongoDB\\Driver\\BulkWrite](/set/mongodb.html#MongoDB\Driver\BulkWrite)
    — The MongoDB\\Driver\\BulkWrite class
    -   [MongoDB\\Driver\\BulkWrite::\_\_construct](/set/mongodb.html#MongoDB\Driver\BulkWrite::__construct)
        — Create a new BulkWrite
    -   [MongoDB\\Driver\\BulkWrite::count](/set/mongodb.html#MongoDB\Driver\BulkWrite::count)
        — Count number of write operations in the bulk
    -   [MongoDB\\Driver\\BulkWrite::delete](/set/mongodb.html#MongoDB\Driver\BulkWrite::delete)
        — Add a delete operation to the bulk
    -   [MongoDB\\Driver\\BulkWrite::insert](/set/mongodb.html#MongoDB\Driver\BulkWrite::insert)
        — Add an insert operation to the bulk
    -   [MongoDB\\Driver\\BulkWrite::update](/set/mongodb.html#MongoDB\Driver\BulkWrite::update)
        — Add an update operation to the bulk
-   [MongoDB\\Driver\\WriteConcern](/set/mongodb.html#MongoDB\Driver\WriteConcern)
    — The MongoDB\\Driver\\WriteConcern class
    -   [MongoDB\\Driver\\WriteConcern::bsonSerialize](/set/mongodb.html#MongoDB\Driver\WriteConcern::bsonSerialize)
        — Returns an object for BSON serialization
    -   [MongoDB\\Driver\\WriteConcern::\_\_construct](/set/mongodb.html#MongoDB\Driver\WriteConcern::__construct)
        — Create a new WriteConcern
    -   [MongoDB\\Driver\\WriteConcern::getJournal](/set/mongodb.html#MongoDB\Driver\WriteConcern::getJournal)
        — Returns the WriteConcern's "journal" option
    -   [MongoDB\\Driver\\WriteConcern::getW](/set/mongodb.html#MongoDB\Driver\WriteConcern::getW)
        — Returns the WriteConcern's "w" option
    -   [MongoDB\\Driver\\WriteConcern::getWtimeout](/set/mongodb.html#MongoDB\Driver\WriteConcern::getWtimeout)
        — Returns the WriteConcern's "wtimeout" option
    -   [MongoDB\\Driver\\WriteConcern::isDefault](/set/mongodb.html#MongoDB\Driver\WriteConcern::isDefault)
        — Checks if this is the default write concern
    -   [MongoDB\\Driver\\WriteConcern::serialize](/set/mongodb.html#MongoDB\Driver\WriteConcern::serialize)
        — Serialize a WriteConcern
    -   [MongoDB\\Driver\\WriteConcern::unserialize](/set/mongodb.html#MongoDB\Driver\WriteConcern::unserialize)
        — Unserialize a WriteConcern
-   [MongoDB\\Driver\\ReadPreference](/set/mongodb.html#MongoDB\Driver\ReadPreference)
    — The MongoDB\\Driver\\ReadPreference class
    -   [MongoDB\\Driver\\ReadPreference::bsonSerialize](/set/mongodb.html#MongoDB\Driver\ReadPreference::bsonSerialize)
        — Returns an object for BSON serialization
    -   [MongoDB\\Driver\\ReadPreference::\_\_construct](/set/mongodb.html#MongoDB\Driver\ReadPreference::__construct)
        — Create a new ReadPreference
    -   [MongoDB\\Driver\\ReadPreference::getHedge](/set/mongodb.html#MongoDB\Driver\ReadPreference::getHedge)
        — Returns the ReadPreference's "hedge" option
    -   [MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds](/set/mongodb.html#MongoDB\Driver\ReadPreference::getMaxStalenessSeconds)
        — Returns the ReadPreference's "maxStalenessSeconds" option
    -   [MongoDB\\Driver\\ReadPreference::getMode](/set/mongodb.html#MongoDB\Driver\ReadPreference::getMode)
        — Returns the ReadPreference's "mode" option
    -   [MongoDB\\Driver\\ReadPreference::getModeString](/set/mongodb.html#MongoDB\Driver\ReadPreference::getModeString)
        — Returns the ReadPreference's "mode" option as a string
    -   [MongoDB\\Driver\\ReadPreference::getTagSets](/set/mongodb.html#MongoDB\Driver\ReadPreference::getTagSets)
        — Returns the ReadPreference's "tagSets" option
    -   [MongoDB\\Driver\\ReadPreference::serialize](/set/mongodb.html#MongoDB\Driver\ReadPreference::serialize)
        — Serialize a ReadPreference
    -   [MongoDB\\Driver\\ReadPreference::unserialize](/set/mongodb.html#MongoDB\Driver\ReadPreference::unserialize)
        — Unserialize a ReadPreference
-   [MongoDB\\Driver\\ReadConcern](/set/mongodb.html#MongoDB\Driver\ReadConcern)
    — The MongoDB\\Driver\\ReadConcern class
    -   [MongoDB\\Driver\\ReadConcern::bsonSerialize](/set/mongodb.html#MongoDB\Driver\ReadConcern::bsonSerialize)
        — Returns an object for BSON serialization
    -   [MongoDB\\Driver\\ReadConcern::\_\_construct](/set/mongodb.html#MongoDB\Driver\ReadConcern::__construct)
        — Create a new ReadConcern
    -   [MongoDB\\Driver\\ReadConcern::getLevel](/set/mongodb.html#MongoDB\Driver\ReadConcern::getLevel)
        — Returns the ReadConcern's "level" option
    -   [MongoDB\\Driver\\ReadConcern::isDefault](/set/mongodb.html#MongoDB\Driver\ReadConcern::isDefault)
        — Checks if this is the default read concern
    -   [MongoDB\\Driver\\ReadConcern::serialize](/set/mongodb.html#MongoDB\Driver\ReadConcern::serialize)
        — Serialize a ReadConcern
    -   [MongoDB\\Driver\\ReadConcern::unserialize](/set/mongodb.html#MongoDB\Driver\ReadConcern::unserialize)
        — Unserialize a ReadConcern
-   [MongoDB\\Driver\\Cursor](/set/mongodb.html#MongoDB\Driver\Cursor) —
    The MongoDB\\Driver\\Cursor class
    -   [MongoDB\\Driver\\Cursor::\_\_construct](/set/mongodb.html#MongoDB\Driver\Cursor::__construct)
        — Create a new Cursor (not used)
    -   [MongoDB\\Driver\\Cursor::getId](/set/mongodb.html#MongoDB\Driver\Cursor::getId)
        — Returns the ID for this cursor
    -   [MongoDB\\Driver\\Cursor::getServer](/set/mongodb.html#MongoDB\Driver\Cursor::getServer)
        — Returns the server associated with this cursor
    -   [MongoDB\\Driver\\Cursor::isDead](/set/mongodb.html#MongoDB\Driver\Cursor::isDead)
        — Checks if the cursor is exhausted or may have additional
        results
    -   [MongoDB\\Driver\\Cursor::setTypeMap](/set/mongodb.html#MongoDB\Driver\Cursor::setTypeMap)
        — Sets a type map to use for BSON unserialization
    -   [MongoDB\\Driver\\Cursor::toArray](/set/mongodb.html#MongoDB\Driver\Cursor::toArray)
        — Returns an array containing all results for this cursor
-   [MongoDB\\Driver\\CursorId](/set/mongodb.html#MongoDB\Driver\CursorId)
    — The MongoDB\\Driver\\CursorId class
    -   [MongoDB\\Driver\\CursorId::\_\_construct](/set/mongodb.html#MongoDB\Driver\CursorId::__construct)
        — Create a new CursorId (not used)
    -   [MongoDB\\Driver\\CursorId::serialize](/set/mongodb.html#MongoDB\Driver\CursorId::serialize)
        — Serialize a CursorId
    -   [MongoDB\\Driver\\CursorId::\_\_toString](/set/mongodb.html#MongoDB\Driver\CursorId::__toString)
        — String representation of the cursor ID
    -   [MongoDB\\Driver\\CursorId::unserialize](/set/mongodb.html#MongoDB\Driver\CursorId::unserialize)
        — Unserialize a CursorId
-   [MongoDB\\Driver\\Server](/set/mongodb.html#MongoDB\Driver\Server) —
    The MongoDB\\Driver\\Server class
    -   [MongoDB\\Driver\\Server::\_\_construct](/set/mongodb.html#MongoDB\Driver\Server::__construct)
        — Create a new Server (not used)
    -   [MongoDB\\Driver\\Server::executeBulkWrite](/set/mongodb.html#MongoDB\Driver\Server::executeBulkWrite)
        — Execute one or more write operations on this server
    -   [MongoDB\\Driver\\Server::executeCommand](/set/mongodb.html#MongoDB\Driver\Server::executeCommand)
        — Execute a database command on this server
    -   [MongoDB\\Driver\\Server::executeQuery](/set/mongodb.html#MongoDB\Driver\Server::executeQuery)
        — Execute a database query on this server
    -   [MongoDB\\Driver\\Server::executeReadCommand](/set/mongodb.html#MongoDB\Driver\Server::executeReadCommand)
        — Execute a database command that reads on this server
    -   [MongoDB\\Driver\\Server::executeReadWriteCommand](/set/mongodb.html#MongoDB\Driver\Server::executeReadWriteCommand)
        — Execute a database command that reads and writes on this
        server
    -   [MongoDB\\Driver\\Server::executeWriteCommand](/set/mongodb.html#MongoDB\Driver\Server::executeWriteCommand)
        — Execute a database command that writes on this server
    -   [MongoDB\\Driver\\Server::getHost](/set/mongodb.html#MongoDB\Driver\Server::getHost)
        — Returns the hostname of this server
    -   [MongoDB\\Driver\\Server::getInfo](/set/mongodb.html#MongoDB\Driver\Server::getInfo)
        — Returns an array of information about this server
    -   [MongoDB\\Driver\\Server::getLatency](/set/mongodb.html#MongoDB\Driver\Server::getLatency)
        — Returns the latency of this server
    -   [MongoDB\\Driver\\Server::getPort](/set/mongodb.html#MongoDB\Driver\Server::getPort)
        — Returns the port on which this server is listening
    -   [MongoDB\\Driver\\Server::getTags](/set/mongodb.html#MongoDB\Driver\Server::getTags)
        — Returns an array of tags describing this server in a replica
        set
    -   [MongoDB\\Driver\\Server::getType](/set/mongodb.html#MongoDB\Driver\Server::getType)
        — Returns an integer denoting the type of this server
    -   [MongoDB\\Driver\\Server::isArbiter](/set/mongodb.html#MongoDB\Driver\Server::isArbiter)
        — Checks if this server is an arbiter member of a replica set
    -   [MongoDB\\Driver\\Server::isHidden](/set/mongodb.html#MongoDB\Driver\Server::isHidden)
        — Checks if this server is a hidden member of a replica set
    -   [MongoDB\\Driver\\Server::isPassive](/set/mongodb.html#MongoDB\Driver\Server::isPassive)
        — Checks if this server is a passive member of a replica set
    -   [MongoDB\\Driver\\Server::isPrimary](/set/mongodb.html#MongoDB\Driver\Server::isPrimary)
        — Checks if this server is a primary member of a replica set
    -   [MongoDB\\Driver\\Server::isSecondary](/set/mongodb.html#MongoDB\Driver\Server::isSecondary)
        — Checks if this server is a secondary member of a replica set
-   [MongoDB\\Driver\\WriteConcernError](/set/mongodb.html#MongoDB\Driver\WriteConcernError)
    — The MongoDB\\Driver\\WriteConcernError class
    -   [MongoDB\\Driver\\WriteConcernError::getCode](/set/mongodb.html#MongoDB\Driver\WriteConcernError::getCode)
        — Returns the WriteConcernError's error code
    -   [MongoDB\\Driver\\WriteConcernError::getInfo](/set/mongodb.html#MongoDB\Driver\WriteConcernError::getInfo)
        — Returns metadata document for the WriteConcernError
    -   [MongoDB\\Driver\\WriteConcernError::getMessage](/set/mongodb.html#MongoDB\Driver\WriteConcernError::getMessage)
        — Returns the WriteConcernError's error message
-   [MongoDB\\Driver\\WriteError](/set/mongodb.html#MongoDB\Driver\WriteError)
    — The MongoDB\\Driver\\WriteError class
    -   [MongoDB\\Driver\\WriteError::getCode](/set/mongodb.html#MongoDB\Driver\WriteError::getCode)
        — Returns the WriteError's error code
    -   [MongoDB\\Driver\\WriteError::getIndex](/set/mongodb.html#MongoDB\Driver\WriteError::getIndex)
        — Returns the index of the write operation corresponding to this
        WriteError
    -   [MongoDB\\Driver\\WriteError::getInfo](/set/mongodb.html#MongoDB\Driver\WriteError::getInfo)
        — Returns metadata document for the WriteError
    -   [MongoDB\\Driver\\WriteError::getMessage](/set/mongodb.html#MongoDB\Driver\WriteError::getMessage)
        — Returns the WriteError's error message
-   [MongoDB\\Driver\\WriteResult](/set/mongodb.html#MongoDB\Driver\WriteResult)
    — The MongoDB\\Driver\\WriteResult class
    -   [MongoDB\\Driver\\WriteResult::getDeletedCount](/set/mongodb.html#MongoDB\Driver\WriteResult::getDeletedCount)
        — Returns the number of documents deleted
    -   [MongoDB\\Driver\\WriteResult::getInsertedCount](/set/mongodb.html#MongoDB\Driver\WriteResult::getInsertedCount)
        — Returns the number of documents inserted (excluding upserts)
    -   [MongoDB\\Driver\\WriteResult::getMatchedCount](/set/mongodb.html#MongoDB\Driver\WriteResult::getMatchedCount)
        — Returns the number of documents selected for update
    -   [MongoDB\\Driver\\WriteResult::getModifiedCount](/set/mongodb.html#MongoDB\Driver\WriteResult::getModifiedCount)
        — Returns the number of existing documents updated
    -   [MongoDB\\Driver\\WriteResult::getServer](/set/mongodb.html#MongoDB\Driver\WriteResult::getServer)
        — Returns the server associated with this write result
    -   [MongoDB\\Driver\\WriteResult::getUpsertedCount](/set/mongodb.html#MongoDB\Driver\WriteResult::getUpsertedCount)
        — Returns the number of documents inserted by an upsert
    -   [MongoDB\\Driver\\WriteResult::getUpsertedIds](/set/mongodb.html#MongoDB\Driver\WriteResult::getUpsertedIds)
        — Returns an array of identifiers for upserted documents
    -   [MongoDB\\Driver\\WriteResult::getWriteConcernError](/set/mongodb.html#MongoDB\Driver\WriteResult::getWriteConcernError)
        — Returns any write concern error that occurred
    -   [MongoDB\\Driver\\WriteResult::getWriteErrors](/set/mongodb.html#MongoDB\Driver\WriteResult::getWriteErrors)
        — Returns any write errors that occurred
    -   [MongoDB\\Driver\\WriteResult::isAcknowledged](/set/mongodb.html#MongoDB\Driver\WriteResult::isAcknowledged)
        — Returns whether the write was acknowledged

简介
----

The <span class="classname">MongoDB\\Driver\\Manager</span> is the main
entry point to the extension. It is responsible for maintaining
connections to MongoDB (be it standalone server, replica set, or sharded
cluster).

No connection to MongoDB is made upon instantiating the Manager. This
means the <span class="classname">MongoDB\\Driver\\Manager</span> can
always be constructed, even though one or more MongoDB servers are down.

Any write or query can throw connection exceptions as connections are
created lazily. A MongoDB server may also become unavailable during the
life time of the script. It is therefore important that all actions on
the Manager to be wrapped in try/catch statements.

类摘要
------

**MongoDB\\Driver\\Manager**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Manager** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$uri`<span
class="initializer"> = "mongodb://127.0.0.1/"</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$uriOptions`<span
class="initializer"> = array()</span></span> \[, <span
class="methodparam"><span class="type">array</span>
`$driverOptions`<span class="initializer"> = array()</span></span>
\]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\ClientEncryption</span> <span
class="methodname">createClientEncryption</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">executeBulkWrite</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\BulkWrite</span> `$bulk`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeQuery</span> ( <span class="methodparam"><span
class="type">string</span> `$namespace`</span> , <span
class="methodparam"><span class="type">MongoDB\\Driver\\Query</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeReadCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeReadWriteCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeWriteCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\ReadConcern</span> <span
class="methodname">getReadConcern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\ReadPreference</span> <span
class="methodname">getReadPreference</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">getServers</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteConcern</span> <span
class="methodname">getWriteConcern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">selectServer</span> ( <span class="methodparam"><span
class="type">MongoDB\\Driver\\ReadPreference</span>
`$readPreference`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Session</span> <span
class="methodname">startSession</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

}

范例
----

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::\_\_construct</span> basic
example**

<span class="function">var\_dump</span>ing a <span
class="classname">MongoDB\\Driver\\Manager</span> will print out various
details about the manager that are otherwise not normally exposed. This
can be useful to debug how the driver views your MongoDB setup, and
which options are used.

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
var_dump($manager);

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\Manager)#1 (3) {
      ["request_id"]=>
      int(1714636915)
      ["uri"]=>
      string(25) "mongodb://localhost:27017"
      ["cluster"]=>
      array(13) {
        ["mode"]=>
        string(6) "direct"
        ["state"]=>
        string(4) "born"
        ["request_id"]=>
        int(0)
        ["sockettimeoutms"]=>
        int(300000)
        ["last_reconnect"]=>
        int(0)
        ["uri"]=>
        string(25) "mongodb://localhost:27017"
        ["requires_auth"]=>
        int(0)
        ["nodes"]=>
        array(...)
        ["max_bson_size"]=>
        int(16777216)
        ["max_msg_size"]=>
        int(50331648)
        ["sec_latency_ms"]=>
        int(15)
        ["peers"]=>
        array(0) {
        }
        ["replSet"]=>
        NULL
      }
    }

MongoDB\\Driver\\Manager::\_\_construct
=======================================

Create new MongoDB Manager

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\Driver\\Manager::\_\_construct</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$uri`<span class="initializer"> = "mongodb://127.0.0.1/"</span></span>
\[, <span class="methodparam"><span class="type">array</span>
`$uriOptions`<span class="initializer"> = array()</span></span> \[,
<span class="methodparam"><span class="type">array</span>
`$driverOptions`<span class="initializer"> = array()</span></span>
\]\]\] )

Constructs a new <span class="classname">MongoDB\\Driver\\Manager</span>
object with the specified options.

> **Note**: <span class="simpara"> Per the
> <a href="https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#single-threaded-client-construction" class="link external">» Server Discovery and Monitoring Specification</a>,
> this constructor performs no I/O. Connections will be initialized on
> demand, when the first operation is executed. </span>

> **Note**: <span class="simpara"> When specifying any SSL or TLS URI
> options via the connection string or `uriOptions` parameter, the
> driver will implicitly enable TLS for its connections. To avoid this,
> either explicitly disable the *tls* option or don't specify any TLS
> options. </span>

> **Note**: <span class="simpara"> On Unix platforms, the MongoDB driver
> is sensitive to scripts that use the fork() system call without also
> calling exec(). Users are advised not to re-use <span
> class="classname">MongoDB\\Driver\\Manager</span> instances in a
> forked child process. </span>

### 参数

`uri`  
A
<a href="https://docs.mongodb.com/manual/reference/connection-string/" class="link external">» mongodb://</a>
connection URI:

``` txt
mongodb://[username:password@]host1[:port1][,host2[:port2],...[,hostN[:portN]]][/[defaultAuthDb][?options]]
```

For details on supported URI options, see
<a href="https://docs.mongodb.com/manual/reference/connection-string/#connections-connection-options" class="link external">» Connection String Options</a>
in the MongoDB manual.
<a href="https://docs.mongodb.com/manual/reference/connection-string/#connection-pool-options" class="link external">» Connection pool options</a>
are not supported, as the PHP driver does not implement connection
pools.

The `uri` is a URL, hence any special characters in its components need
to be URL encoded according to
<a href="http://www.faqs.org/rfcs/rfc3986" class="link external">» RFC 3986</a>.
This is particularly relevant to the username and password, which can
often include special characters such as *@*, *:*, or *%*. When
connecting via a Unix domain socket, the socket path may contain special
characters such as slashes and must be encoded. The <span
class="function">rawurlencode</span> function may be used to encode
constituent parts of the URI.

The *defaultAuthDb* component may be used to specify the database name
associated with the user's credentials; however the *authSource* URI
option will take priority if specified. If neither *defaultAuthDb* nor
*authSource* are specified, the *admin* database will be used by
default. The *defaultAuthDb* component has no effect in the absence of
user credentials.

`uriOptions`  
Additional
<a href="https://docs.mongodb.com/manual/reference/connection-string/#connections-connection-options" class="link external">» connection string options</a>,
which will overwrite any options with the same name in the `uri`
parameter.

<table>
<caption><strong>uriOptions</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>appname</td>
<td><span class="type">string</span></td>
<td><p>MongoDB 3.4+ has the ability to annotate connections with metadata provided by the connecting client. This metadata is included in the server's logs upon establishing a connection and also recorded in slow query logs when database profiling is enabled.</p>
<p>This option may be used to specify an application name, which will be included in the metadata. The value cannot exceed 128 characters in length.</p></td>
</tr>
<tr class="even">
<td>authMechanism</td>
<td><span class="type">string</span></td>
<td><p>The authentication mechanism that MongoDB will use to authenticate the connection. For additional details and a list of supported values, see <a href="https://docs.mongodb.com/manual/reference/connection-string/#urioption.authMechanism" class="link external">» Authentication Options</a> in the MongoDB manual.</p></td>
</tr>
<tr class="odd">
<td>authMechanismProperties</td>
<td><span class="type">array</span></td>
<td><p>Properties for the selected authentication mechanism. For additional details and a list of supported properties, see the <a href="https://github.com/mongodb/specifications/blob/master/source/auth/auth.rst#auth-related-options" class="link external">» Driver Authentication Specification</a>.</p>
<blockquote>
<p><strong>Note</strong>: <span class="simpara"> When not specified in the URI string, this option is expressed as an array of key/value pairs. The keys and values in this array should be strings. </span></p>
</blockquote></td>
</tr>
<tr class="even">
<td>authSource</td>
<td><span class="type">string</span></td>
<td><p>The database name associated with the user's credentials. Defaults to the database component of the connection URI, or the <em>admin</em> database if both are unspecified.</p>
<p>For authentication mechanisms that delegate credential storage to other services (e.g. GSSAPI), this should be <em>"$external"</em>.</p></td>
</tr>
<tr class="odd">
<td>canonicalizeHostname</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, the driver will resolve the real hostname for the server IP address before authenticating via SASL. Some underlying GSSAPI layers already do this, but the functionality may be disabled in their config (e.g. <em>krb.conf</em>). Defaults to <strong><code>FALSE</code></strong>.</p>
<p>This option is a deprecated alias for the <em>"CANONICALIZE_HOST_NAME"</em> property of the <em>"authMechanismProperties"</em> URI option.</p></td>
</tr>
<tr class="even">
<td>compressors</td>
<td><span class="type">string</span></td>
<td><p>A prioritized, comma-delimited list of compressors that the client wants to use. Messages are only compressed if the client and server share any compressors in common, and the compressor used in each direction will depend on the individual configuration of the server or driver. See the <a href="https://github.com/mongodb/specifications/blob/master/source/compression/OP_COMPRESSED.rst#compressors" class="link external">» Driver Compression Specification</a> for more information.</p></td>
</tr>
<tr class="odd">
<td>connectTimeoutMS</td>
<td><span class="type">integer</span></td>
<td><p>The time in milliseconds to attempt a connection before timing out. Defaults to 10,000 milliseconds.</p></td>
</tr>
<tr class="even">
<td>directConnection</td>
<td><span class="type">boolean</span></td>
<td><p>This option can be used to control replica set discovery behavior when only a single host is provided in the connection string. By default, providing a single member in the connection string will establish a direct connection or discover additional members depending on whether the <em>"replicaSet"</em> URI option is omitted or present, respectively. Specify <strong><code>FALSE</code></strong> to force discovery to occur (if <em>"replicaSet"</em> is omitted) or specify <strong><code>TRUE</code></strong> to force a direct connection (if <em>"replicaSet"</em> is present).</p></td>
</tr>
<tr class="odd">
<td>gssapiServiceName</td>
<td><span class="type">string</span></td>
<td><p>Set the Kerberos service name when connecting to Kerberized MongoDB instances. This value must match the service name set on MongoDB instances (i.e. <a href="https://docs.mongodb.com/manual/reference/parameters/#param.saslServiceName" class="link external">» saslServiceName</a> server parameter). Defaults to <em>"mongodb"</em>.</p>
<p>This option is a deprecated alias for the <em>"SERVICE_NAME"</em> property of the <em>"authMechanismProperties"</em> URI option.</p></td>
</tr>
<tr class="even">
<td>heartbeatFrequencyMS</td>
<td><span class="type">integer</span></td>
<td><p>Specifies the interval in milliseconds between the driver's checks of the MongoDB topology, counted from the end of the previous check until the beginning of the next one. Defaults to 60,000 milliseconds.</p>
<p>Per the <a href="https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#heartbeatfrequencyms" class="link external">» Server Discovery and Monitoring Specification</a>, this value cannot be less than 500 milliseconds.</p></td>
</tr>
<tr class="odd">
<td>journal</td>
<td><span class="type">boolean</span></td>
<td><p>Corresponds to the default write concern's <code class="parameter">journal</code> parameter. If <strong><code>TRUE</code></strong>, writes will require acknowledgement from MongoDB that the operation has been written to the journal. For details, see <span class="classname">MongoDB\Driver\WriteConcern</span>.</p></td>
</tr>
<tr class="even">
<td>localThresholdMS</td>
<td><span class="type">integer</span></td>
<td><p>The size in milliseconds of the latency window for selecting among multiple suitable MongoDB instances while resolving a read preference. Defaults to 15 milliseconds.</p></td>
</tr>
<tr class="odd">
<td>maxStalenessSeconds</td>
<td><span class="type">integer</span></td>
<td><p>Corresponds to the read preference's <em>"maxStalenessSeconds"</em>. Specifies, in seconds, how stale a secondary can be before the client stops using it for read operations. By default, there is no maximum staleness and clients will not consider a secondary’s lag when choosing where to direct a read operation. For details, see <span class="classname">MongoDB\Driver\ReadPreference</span>.</p>
<p>If specified, the max staleness must be a signed 32-bit integer greater than or equal to <strong><code>MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS</code></strong> (i.e. 90 seconds).</p></td>
</tr>
<tr class="even">
<td>password</td>
<td><span class="type">string</span></td>
<td>The password for the user being authenticated. This option is useful if the password contains special characters, which would otherwise need to be URL encoded for the connection URI.</td>
</tr>
<tr class="odd">
<td>readConcernLevel</td>
<td><span class="type">string</span></td>
<td>Corresponds to the read concern's <code class="parameter">level</code> parameter. Specifies the level of read isolation. For details, see <span class="classname">MongoDB\Driver\ReadConcern</span>.</td>
</tr>
<tr class="even">
<td>readPreference</td>
<td><span class="type">string</span></td>
<td><p>Corresponds to the read preference's <code class="parameter">mode</code> parameter. Defaults to <em>"primary"</em>. For details, see <span class="classname">MongoDB\Driver\ReadPreference</span>.</p></td>
</tr>
<tr class="odd">
<td>readPreferenceTags</td>
<td><span class="type">array</span></td>
<td><p>Corresponds to the read preference's <code class="parameter">tagSets</code> parameter. Tag sets allow you to target read operations to specific members of a replica set. For details, see <span class="classname">MongoDB\Driver\ReadPreference</span>.</p>
<blockquote>
<p><strong>Note</strong>: <span class="simpara"> When not specified in the URI string, this option is expressed as an array consistent with the format expected by <span class="function">MongoDB\Driver\ReadPreference::__construct</span>. </span></p>
</blockquote></td>
</tr>
<tr class="even">
<td>replicaSet</td>
<td><span class="type">string</span></td>
<td><p>Specifies the name of the replica set.</p></td>
</tr>
<tr class="odd">
<td>retryReads</td>
<td><span class="type">boolean</span></td>
<td><p>Specifies whether or not the driver should automatically retry certain read operations that fail due to transient network errors or replica set elections. This functionality requires MongoDB 3.6+. Defaults to <strong><code>TRUE</code></strong>.</p>
<p>See the <a href="https://github.com/mongodb/specifications/blob/master/source/retryable-reads/retryable-reads.rst" class="link external">» Retryable Reads Specification</a> for more information.</p></td>
</tr>
<tr class="even">
<td>retryWrites</td>
<td><span class="type">boolean</span></td>
<td><p>Specifies whether or not the driver should automatically retry certain write operations that fail due to transient network errors or replica set elections. This functionality requires MongoDB 3.6+. Defaults to <strong><code>TRUE</code></strong>.</p>
<p>See <a href="https://docs.mongodb.com/manual/core/retryable-writes/" class="link external">» Retryable Writes</a> in the MongoDB manual for more information.</p></td>
</tr>
<tr class="odd">
<td>safe</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, specifies <em>1</em> for the default write concern's <code class="parameter">w</code> parameter. If <strong><code>FALSE</code></strong>, <em>0</em> is specified. For details, see <span class="classname">MongoDB\Driver\WriteConcern</span>.</p>
<p>This option is deprecated and should not be used.</p></td>
</tr>
<tr class="even">
<td>serverSelectionTimeoutMS</td>
<td><span class="type">integer</span></td>
<td><p>Specifies how long in milliseconds to block for server selection before throwing an exception. Defaults to 30,000 milliseconds.</p></td>
</tr>
<tr class="odd">
<td>serverSelectionTryOnce</td>
<td><span class="type">boolean</span></td>
<td><p>When <strong><code>TRUE</code></strong>, instructs the driver to scan the MongoDB deployment exactly once after server selection fails and then either select a server or raise an error. When <strong><code>FALSE</code></strong>, the driver blocks and searches for a server up to the <em>"serverSelectionTimeoutMS"</em> value. Defaults to <strong><code>TRUE</code></strong>.</p></td>
</tr>
<tr class="even">
<td>slaveOk</td>
<td><span class="type">boolean</span></td>
<td><p>Specifies <em>"secondaryPreferred"</em> for the read preference mode if <strong><code>TRUE</code></strong>. For details, see <span class="classname">MongoDB\Driver\ReadPreference</span>.</p>
<p>This option is deprecated and should not be used.</p></td>
</tr>
<tr class="odd">
<td>socketCheckIntervalMS</td>
<td><span class="type">integer</span></td>
<td><p>If a socket has not been used recently, the driver must check it via an <em>isMaster</em> command before using it for any operation. Defaults to 5,000 milliseconds.</p></td>
</tr>
<tr class="even">
<td>socketTimeoutMS</td>
<td><span class="type">integer</span></td>
<td><p>The time in milliseconds to attempt a send or receive on a socket before timing out. Defaults to 300,000 milliseconds (i.e. five minutes).</p></td>
</tr>
<tr class="odd">
<td>ssl</td>
<td><span class="type">boolean</span></td>
<td><p>Initiates the connection with TLS/SSL if <strong><code>TRUE</code></strong>. Defaults to <strong><code>FALSE</code></strong>.</p>
<p>This option is a deprecated alias for the <em>"tls"</em> URI option.</p></td>
</tr>
<tr class="even">
<td>tls</td>
<td><span class="type">boolean</span></td>
<td><p>Initiates the connection with TLS/SSL if <strong><code>TRUE</code></strong>. Defaults to <strong><code>FALSE</code></strong>.</p></td>
</tr>
<tr class="odd">
<td>tlsAllowInvalidCertificates</td>
<td><span class="type">boolean</span></td>
<td><p>Specifies whether or not the driver should error when the server's TLS certificate is invalid. Defaults to <strong><code>FALSE</code></strong>.</p>
<div class="warning">
<strong>Warning</strong>
<p>Disabling certificate validation creates a vulnerability.</p>
</div></td>
</tr>
<tr class="even">
<td>tlsAllowInvalidHostnames</td>
<td><span class="type">boolean</span></td>
<td><p>Specifies whether or not the driver should error when there is a mismatch between the server's hostname and the hostname specified by the TLS certificate. Defaults to <strong><code>FALSE</code></strong>.</p>
<div class="warning">
<strong>Warning</strong>
<p>Disabling certificate validation creates a vulnerability. Allowing invalid hostnames may expose the driver to a <a href="https://en.wikipedia.org/wiki/Man-in-the-middle_attack" class="link external">» man-in-the-middle attack</a>.</p>
</div></td>
</tr>
<tr class="odd">
<td>tlsCAFile</td>
<td><span class="type">string</span></td>
<td><p>Path to file with either a single or bundle of certificate authorities to be considered trusted when making a TLS connection. The system certificate store will be used by default.</p></td>
</tr>
<tr class="even">
<td>tlsCertificateKeyFile</td>
<td><span class="type">string</span></td>
<td><p>Path to the client certificate file or the client private key file; in the case that they both are needed, the files should be concatenated.</p></td>
</tr>
<tr class="odd">
<td>tlsCertificateKeyFilePassword</td>
<td><span class="type">string</span></td>
<td><p>Password to decrypt the client private key (i.e. <em>"tlsCertificateKeyFile"</em> URI option) to be used for TLS connections.</p></td>
</tr>
<tr class="even">
<td>tlsDisableCertificateRevocationCheck</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, the driver will not attempt to check certificate revocation status (e.g. OCSP, CRL). Defaults to <strong><code>FALSE</code></strong>.</p></td>
</tr>
<tr class="odd">
<td>tlsDisableOCSPEndpointCheck</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, the driver will not attempt to contact an OCSP responder endpoint if needed (i.e. an OCSP response is not stapled). Defaults to <strong><code>FALSE</code></strong>.</p></td>
</tr>
<tr class="even">
<td>tlsInsecure</td>
<td><span class="type">boolean</span></td>
<td><p>Relax TLS constraints as much as possible. Specifying <strong><code>TRUE</code></strong> for this option has the same effect as specifying <strong><code>TRUE</code></strong> for both the <em>"tlsAllowInvalidCertificates"</em> and <em>"tlsAllowInvalidHostnames"</em> URI options. Defaults to <strong><code>FALSE</code></strong>.</p>
<div class="warning">
<strong>Warning</strong>
<p>Disabling certificate validation creates a vulnerability. Allowing invalid hostnames may expose the driver to a <a href="https://en.wikipedia.org/wiki/Man-in-the-middle_attack" class="link external">» man-in-the-middle attack</a>.</p>
</div></td>
</tr>
<tr class="odd">
<td>username</td>
<td><span class="type">string</span></td>
<td>The username for the user being authenticated. This option is useful if the username contains special characters, which would otherwise need to be URL encoded for the connection URI.</td>
</tr>
<tr class="even">
<td>w</td>
<td><span class="type">integer|string</span></td>
<td><p>Corresponds to the default write concern's <code class="parameter">w</code> parameter. For details, see <span class="classname">MongoDB\Driver\WriteConcern</span>.</p></td>
</tr>
<tr class="odd">
<td>wTimeoutMS</td>
<td><span class="type">integer|string</span></td>
<td><p>Corresponds to the default write concern's <code class="parameter">wtimeout</code> parameter. Specifies a time limit, in milliseconds, for the write concern. For details, see <span class="classname">MongoDB\Driver\WriteConcern</span>.</p>
<p>If specified, <em>wTimeoutMS</em> must be a signed 32-bit integer greater than or equal to zero.</p></td>
</tr>
<tr class="even">
<td>zlibCompressionLevel</td>
<td><span class="type">integer</span></td>
<td><p>Specifies the compression level to use for the zlib compressor. This option has no effect if <em>zlib</em> is not included in the <em>"compressors"</em> URI option. See the <a href="https://github.com/mongodb/specifications/blob/master/source/compression/OP_COMPRESSED.rst#zlibcompressionlevel" class="link external">» Driver Compression Specification</a> for more information.</p></td>
</tr>
</tbody>
</table>

`driverOptions`  
<table>
<caption><strong>driverOptions</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>allow_invalid_hostname</td>
<td><span class="type">boolean</span></td>
<td><p>Disables hostname validation if <strong><code>TRUE</code></strong>. Defaults to <strong><code>FALSE</code></strong>.</p>
<p>Allowing invalid hostnames may expose the driver to a <a href="https://en.wikipedia.org/wiki/Man-in-the-middle_attack" class="link external">» man-in-the-middle attack</a>.</p>
<p>This option is a deprecated alias for the <em>"tlsAllowInvalidHostnames"</em> URI option.</p></td>
</tr>
<tr class="even">
<td>autoEncryption</td>
<td><span class="type">array</span></td>
<td><p>Provides options to enable automatic client-side field level encryption. The following options are supported:</p>
<table>
<caption><strong>Options for automatic encryption</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>keyVaultClient</td>
<td><span class="classname">MongoDB\Driver\Manager</span></td>
<td>The Manager used to route data key queries to a separate MongoDB cluster. By default, the current Manager and cluster is used.</td>
</tr>
<tr class="even">
<td>keyVaultNamespace</td>
<td><span class="type">string</span></td>
<td>A fully qualified namespace (e.g. <em>"databaseName.collectionName"</em>) denoting the collection that contains all data keys used for encryption and decryption.</td>
</tr>
<tr class="odd">
<td>kmsProviders</td>
<td><span class="type">array</span></td>
<td><p>A document containing the configuration for one or more KMS providers, which are used to encrypt data keys. Currently <em>aws</em> or <em>local</em>are supported and at least one must be specified.</p>
<p>The format for <em>aws</em> is as follows:</p>
<div class="example-contents">
<div class="javascriptcode">
<div class="sourceCode" id="cb1"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span id="cb1-1"><a href="#cb1-1"></a>aws<span class="op">:</span> {</span>
<span id="cb1-2"><a href="#cb1-2"></a>    <span class="dt">accessKeyId</span><span class="op">:</span> <span class="op">&lt;</span>string<span class="op">&gt;,</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>    <span class="dt">secretAccessKey</span><span class="op">:</span> <span class="op">&lt;</span>string<span class="op">&gt;</span></span>
<span id="cb1-4"><a href="#cb1-4"></a>}</span></code></pre></div>
</div>
</div>
<p>The format for <em>local</em> is as follows:</p>
<div class="example-contents">
<div class="javascriptcode">
<div class="sourceCode" id="cb2"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span id="cb2-1"><a href="#cb2-1"></a>local<span class="op">:</span> {</span>
<span id="cb2-2"><a href="#cb2-2"></a>    <span class="co">// The master key used to encrypt/decrypt data keys</span></span>
<span id="cb2-3"><a href="#cb2-3"></a>    <span class="dt">key</span><span class="op">:</span> <span class="op">&lt;</span><span class="dv">96</span><span class="op">-</span>byte MongoDB\BSON\Binary <span class="cf">with</span> subtype <span class="dv">0</span><span class="op">&gt;</span></span>
<span id="cb2-4"><a href="#cb2-4"></a>}</span></code></pre></div>
</div>
</div></td>
</tr>
<tr class="even">
<td>schemaMap</td>
<td><span class="type">array</span></td>
<td><p>Allows specifying a local JSON schema that is used to configure encryption.</p>
<blockquote>
<p><strong>Note</strong>: <span class="simpara"> Supplying a <em>schemaMap</em> provides more security than relying on JSON schemas obtained from the server. It protects against a malicious server advertising a false JSON schema, which could trick the client into sending unencrypted data that should be encrypted. </span></p>
</blockquote>
<blockquote>
<p><strong>Note</strong>: <span class="simpara"> Schemas supplied in the <em>schemaMap</em> only apply to configuring automatic encryption for client side encryption. Other validation rules in the JSON schema will not be enforced by the driver and will result in an error. </span></p>
</blockquote></td>
</tr>
<tr class="odd">
<td>bypassAutoEncryption</td>
<td><span class="type">boolean</span></td>
<td>With this option set to <strong><code>TRUE</code></strong>, <em>mongocryptd</em> will not be spawned automatically. This is used to disable automatic encryption.</td>
</tr>
<tr class="even">
<td>extraOptions</td>
<td><span class="type">array</span></td>
<td>The <em>extraOptions</em> relate to the <em>mongocryptd</em> process. See the <a href="https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#extraoptions" class="link external">» Client-Side Encryption Specification</a> for more information.</td>
</tr>
</tbody>
</table>
<blockquote>
<p><strong>Note</strong>: <span class="simpara"> Automatic encryption is an enterprise only feature that only applies to operations on a collection. Automatic encryption is not supported for operations on a database or view, and operations that are not bypassed will result in error. To bypass automatic encryption for all operations, set <em>bypassAutoEncryption=true</em> in <em>autoEncryption</em>. For more information on whitelisted operations, see the <a href="https://github.com/mongodb/specifications/blob/master/source/client-side-encryption/client-side-encryption.rst#libmongocrypt-auto-encryption-whitelist" class="link external">» Client-Side Encryption Specification</a>. </span></p>
</blockquote></td>
</tr>
<tr class="odd">
<td>ca_dir</td>
<td><span class="type">string</span></td>
<td><p>Path to a correctly hashed certificate directory. The system certificate store will be used by default.</p></td>
</tr>
<tr class="even">
<td>ca_file</td>
<td><span class="type">string</span></td>
<td><p>Path to file with either a single or bundle of certificate authorities to be considered trusted when making a TLS connection. The system certificate store will be used by default.</p>
<p>This option is a deprecated alias for the <em>"tlsCAFile"</em> URI option.</p></td>
</tr>
<tr class="odd">
<td>context</td>
<td><span class="type">resource</span></td>
<td><p><a href="/context/ssl.html" class="link">SSL context options</a> to be used as fallbacks if a driver option or its equivalent URI option, if any, is not specified. Note that the driver does not consult the default stream context (i.e. <span class="function">stream_context_get_default</span>). The following context options are supported:</p>
<table>
<caption><strong>SSL context option fallbacks</strong></caption>
<thead>
<tr class="header">
<th>Driver option</th>
<th>Context option (fallback)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ca_dir</td>
<td>capath</td>
</tr>
<tr class="even">
<td>ca_file</td>
<td>cafile</td>
</tr>
<tr class="odd">
<td>pem_file</td>
<td>local_cert</td>
</tr>
<tr class="even">
<td>pem_pwd</td>
<td>passphrase</td>
</tr>
<tr class="odd">
<td>weak_cert_validation</td>
<td>allow_self_signed</td>
</tr>
</tbody>
</table>
<p>This option is supported for backwards compatibility, but should be considered deprecated.</p></td>
</tr>
<tr class="even">
<td>crl_file</td>
<td><span class="type">string</span></td>
<td>Path to a certificate revocation list file.</td>
</tr>
<tr class="odd">
<td>driver</td>
<td><span class="type">array</span></td>
<td><p>Allows custom drivers to append their own metadata to the server handshake. By default, the driver submits its own name, version, and platform (i.e. PHP version) in the handshake. Custom drivers can specify strings for the <em>"name"</em>, <em>"version"</em>, and <em>"platform"</em> keys of this array, which will be appended to the respective field(s) in the handshake document.</p>
<blockquote>
<p><strong>Note</strong>: <span class="simpara"> Handshake information is limited to 512 bytes. The driver will truncate handshake data to fit within this 512-byte string. Drivers and ODMs are encouraged to keep their own metadata concise. </span></p>
</blockquote></td>
</tr>
<tr class="even">
<td>pem_file</td>
<td><span class="type">string</span></td>
<td><p>Path to a PEM encoded certificate to use for client authentication.</p>
<p>This option is a deprecated alias for the <em>"tlsCertificateKeyFile"</em> URI option.</p></td>
</tr>
<tr class="odd">
<td>pem_pwd</td>
<td><span class="type">string</span></td>
<td><p>Passphrase for the PEM encoded certificate (if applicable).</p>
<p>This option is a deprecated alias for the <em>"tlsCertificateKeyFilePassword"</em> URI option.</p></td>
</tr>
<tr class="even">
<td>weak_cert_validation</td>
<td><span class="type">boolean</span></td>
<td><p>Disables certificate validation if <strong><code>TRUE</code></strong>. Defaults to <strong><code>FALSE</code></strong></p>
<p>This option is a deprecated alias for the <em>"tlsAllowInvalidHostnames"</em> URI option.</p></td>
</tr>
</tbody>
</table>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    if the `uri` format is invalid

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.8.0</td>
<td><p>Added the <em>"directConnection"</em>, <em>"tlsDisableCertificateRevocationCheck"</em>, and <em>"tlsDisableOCSPEndpointCheck"</em> URI options.</p>
<p>Added the <em>"driver"</em> driver option.</p></td>
</tr>
<tr class="even">
<td>1.7.0</td>
<td><p>Added the <em>"autoEncryption"</em> driver option.</p>
<p>Specifying any SSL or TLS option via the <code class="parameter">driverOptions</code> parameter will now implicitly enable TLS, as is done for the corresponding URI options.</p></td>
</tr>
<tr class="odd">
<td>1.6.0</td>
<td><p>Added the <em>"retryReads"</em>, <em>"tls"</em>, <em>"tlsAllowInvalidCertificates"</em>, <em>"tlsAllowInvalidHostnames"</em>, <em>"tlsCAFile"</em>, <em>"tlsCertificateKeyFile"</em>, <em>"tlsCertificateKeyFilePassword"</em>, and <em>"tlsInsecure"</em> URI options.</p>
<p>The <em>"retryWrites"</em> URI option defaults to <strong><code>TRUE</code></strong>.</p>
<p>Specifying any SSL or TLS URI option via the connection string or <code class="parameter">uriOptions</code> parameter will now implicitly enable TLS unless <em>ssl</em> or <em>tls</em> is <strong><code>FALSE</code></strong>. TLS is <em>not</em> implicitly enabled for any options in the <code class="parameter">driverOptions</code> parameter, which is unchanged from previous versions.</p></td>
</tr>
<tr class="even">
<td>1.5.0</td>
<td><p><em>"wtimeoutMS"</em> is now always validated and applied to the write concern. Previously, the option was ignored if <em>"w"</em> was &lt;= 1, since the timeout only applies to replication.</p></td>
</tr>
<tr class="odd">
<td>1.4.0</td>
<td><p>Added the <em>"compressors"</em>, <em>"retryWrites"</em>, and <em>"zlibCompressionLevel"</em> URI options.</p></td>
</tr>
<tr class="even">
<td>1.3.0</td>
<td><p>The <code class="parameter">uriOptions</code> argument now accepts <em>"authMechanism"</em> and <em>"authMechanismProperties"</em> options. Previously, these options were only supported in the <code class="parameter">uri</code> argument.</p></td>
</tr>
<tr class="odd">
<td>1.2.0</td>
<td><p>The <code class="parameter">uri</code> argument defaults to <em>"mongodb://127.0.0.1/"</em>. The default port remains <em>27017</em>.</p>
<p>Added the <em>"appname"</em> URI option.</p>
<p>Added the <em>"allow_invalid_hostname"</em>, <em>"ca_file"</em>, <em>"ca_dir"</em>, <em>"clr_file"</em>, <em>"pem_file"</em>, <em>"pem_pwd"</em>, and <em>"weak_cert_validation"</em> driver options.</p>
<p>The PHP Streams API is no longer used for socket communication. The <em>"connectTimeoutMS"</em> URI option now defaults to 10 seconds instead of <a href="/filesystem/setup.html#" class="link">default_socket_timeout</a> in previous versions. Additionally, the driver no longer supports all <a href="/context/ssl.html" class="link">SSL context options</a> via the <em>"context"</em> driver option.</p></td>
</tr>
<tr class="even">
<td>1.1.0</td>
<td><p>The <code class="parameter">uri</code> argument is optional and defaults to <em>"mongodb://localhost:27017/"</em>.</p></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::\_\_construct</span> basic
examples**

Connecting to standalone MongoDB node:

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://example.com:27017");

?>
```

Connecting to standalone MongoDB node via a Unix domain socket. The
socket path may include special characters such as slashes and should be
encoded with <span class="function">rawurlencode</span>.

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://" . rawurlencode("/tmp/mongodb-27017.sock"));

?>
```

Connecting to a replica set:

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

?>
```

Connecting to a sharded cluster (i.e. one or more mongos instances):

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://mongos1.example.com,mongos2.example.com/");

?>
```

Connecting to MongoDB with authentication credentials for a particular
user and database:

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://myusername:mypassword@example.com/?authSource=databaseName");

?>
```

Connecting to MongoDB with authentication credentials for a particular
user and database, where the username or password includes special
characters (e.g. *@*, *:*, *%*). In the following example, the password
string *myp@ss:w%rd* has been manually escaped; however, <span
class="function">rawurlencode</span> may also be used to escape URI
components that may contain special characters.

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://myusername:myp%40ss%3Aw%25rd@example.com/?authSource=databaseName");

?>
```

Connecting to MongoDB with X509 authentication:

``` php
<?php

$manager = new MongoDB\Driver\Manager(
    "mongodb://example.com/?ssl=true&authMechanism=MONGODB-X509",
    [],
    [
        "pem_file" => "/path/to/client.pem",
    ]
);
?>
```

### 参见

-   <a href="/set/mongodb.html#Connections" class="link">Connection handling and persistence</a>
-   <a href="https://docs.mongodb.com/manual/reference/connection-string/" class="link external">» MongoDB Connection String Format</a>

MongoDB\\Driver\\Manager::createClientEncryption
================================================

Create a new ClientEncryption object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\ClientEncryption</span> <span
class="methodname">MongoDB\\Driver\\Manager::createClientEncryption</span>
( <span class="methodparam"><span class="type">array</span>
`$options`</span> )

Constructs a new <span
class="classname">MongoDB\\Driver\\ClientEncryption</span> object with
the specified options.

### 参数

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>keyVaultClient</td>
<td><span class="classname">MongoDB\Driver\Manager</span></td>
<td>The Manager used to route data key queries to a separate MongoDB cluster. By default, the current Manager and cluster is used.</td>
</tr>
<tr class="even">
<td>keyVaultNamespace</td>
<td><span class="type">string</span></td>
<td>A fully qualified namespace (e.g. <em>"databaseName.collectionName"</em>) denoting the collection that contains all data keys used for encryption and decryption.</td>
</tr>
<tr class="odd">
<td>kmsProviders</td>
<td><span class="type">array</span></td>
<td><p>A document containing the configuration for one or more KMS providers, which are used to encrypt data keys. Currently <em>aws</em> or <em>local</em>are supported and at least one must be specified.</p>
<p>The format for <em>aws</em> is as follows:</p>
<div class="example-contents">
<div class="javascriptcode">
<div class="sourceCode" id="cb1"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span id="cb1-1"><a href="#cb1-1"></a>aws<span class="op">:</span> {</span>
<span id="cb1-2"><a href="#cb1-2"></a>    <span class="dt">accessKeyId</span><span class="op">:</span> <span class="op">&lt;</span>string<span class="op">&gt;,</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>    <span class="dt">secretAccessKey</span><span class="op">:</span> <span class="op">&lt;</span>string<span class="op">&gt;</span></span>
<span id="cb1-4"><a href="#cb1-4"></a>}</span></code></pre></div>
</div>
</div>
<p>The format for <em>local</em> is as follows:</p>
<div class="example-contents">
<div class="javascriptcode">
<div class="sourceCode" id="cb2"><pre class="sourceCode javascript"><code class="sourceCode javascript"><span id="cb2-1"><a href="#cb2-1"></a>local<span class="op">:</span> {</span>
<span id="cb2-2"><a href="#cb2-2"></a>    <span class="co">// The master key used to encrypt/decrypt data keys</span></span>
<span id="cb2-3"><a href="#cb2-3"></a>    <span class="dt">key</span><span class="op">:</span> <span class="op">&lt;</span><span class="dv">96</span><span class="op">-</span>byte MongoDB\BSON\Binary <span class="cf">with</span> subtype <span class="dv">0</span><span class="op">&gt;</span></span>
<span id="cb2-4"><a href="#cb2-4"></a>}</span></code></pre></div>
</div>
</div></td>
</tr>
</tbody>
</table>

### 返回值

Returns a new <span
class="classname">MongoDB\\Driver\\ClientEncryption</span> instance.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    if the extension was compiled without libmongocrypt support

### 参见

-   <span class="classname">MongoDB\\Driver\\ClientEncryption</span>
-   <a href="https://docs.mongodb.com/manual/core/security-explicit-client-side-encryption/" class="link external">» Explicit (Manual) Client-Side Field Level Encryption</a>
    in the MongoDB manual

MongoDB\\Driver\\Manager::executeBulkWrite
==========================================

Execute one or more write operations

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span> (
<span class="methodparam"><span class="type">string</span>
`$namespace`</span> , <span class="methodparam"><span
class="type">MongoDB\\Driver\\BulkWrite</span> `$bulk`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes one or more write operations on the primary server.

A <span class="classname">MongoDB\\Driver\\BulkWrite</span> can be
constructed with one or more write operations of varying types (e.g.
updates, deletes, and inserts). The driver will attempt to send
operations of the same type to the server in as few requests as possible
to optimize round trips.

### 参数

`namespace` (<span class="type">string</span>)  
A fully qualified namespace (e.g. *"databaseName.collectionName"*).

`bulk` (<span class="classname">MongoDB\\Driver\\BulkWrite</span>)  
The write(s) to execute.

`options`  
| Option       | Type                                                         | Description                                |
|--------------|--------------------------------------------------------------|--------------------------------------------|
| session      | <span class="classname">MongoDB\\Driver\\Session</span>      | A session to associate with the operation. |
| writeConcern | <span class="classname">MongoDB\\Driver\\WriteConcern</span> | A write concern to apply to the operation. |

### 返回值

Returns <span class="classname">MongoDB\\Driver\\WriteResult</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `bulk` does not contain any write operations.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `bulk` has already been executed. <span
    class="classname">MongoDB\\Driver\\BulkWrite</span> objects may not
    be executed multiple times.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\BulkWriteException</span>
    on any write failure (e.g. write error, failure to apply a write
    concern)
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                       |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern.                                                                  |
| 1.4.0 | The third parameter is now an `options` array. For backwards compatibility, this paramater will still accept a <span class="classname">MongoDB\\Driver\\WriteConcern</span> object.                                                                        |
| 1.3.0 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> is now thrown if `bulk` does not contain any write operations. Previously, a <span class="classname">MongoDB\\Driver\\Exception\\BulkWriteException</span> was thrown. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::executeBulkWrite</span>
example**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite();

$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);

$bulk->update(['x' => 2], ['$set' => ['x' => 1]], ['multi' => false, 'upsert' => false]);
$bulk->update(['x' => 3], ['$set' => ['x' => 3]], ['multi' => false, 'upsert' => true]);
$bulk->update(['_id' => 3], ['$set' => ['x' => 3]], ['multi' => false, 'upsert' => true]);

$bulk->insert(['_id' => 4, 'x' => 2]);

$bulk->delete(['x' => 1], ['limit' => 1]);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 100);
$result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);

printf("Inserted %d document(s)\n", $result->getInsertedCount());
printf("Matched  %d document(s)\n", $result->getMatchedCount());
printf("Updated  %d document(s)\n", $result->getModifiedCount());
printf("Upserted %d document(s)\n", $result->getUpsertedCount());
printf("Deleted  %d document(s)\n", $result->getDeletedCount());

foreach ($result->getUpsertedIds() as $index => $id) {
    printf('upsertedId[%d]: ', $index);
    var_dump($id);
}

/* If the WriteConcern could not be fulfilled */
if ($writeConcernError = $result->getWriteConcernError()) {
    printf("%s (%d): %s\n", $writeConcernError->getMessage(), $writeConcernError->getCode(), var_export($writeConcernError->getInfo(), true));
}

/* If a write could not happen at all */
foreach ($result->getWriteErrors() as $writeError) {
    printf("Operation#%d: %s (%d)\n", $writeError->getIndex(), $writeError->getMessage(), $writeError->getCode());
}
?>
```

以上例程的输出类似于：

    Inserted 3 document(s)
    Matched  1 document(s)
    Updated  1 document(s)
    Upserted 2 document(s)
    Deleted  1 document(s)
    upsertedId[3]: object(MongoDB\BSON\ObjectId)#5 (1) {
      ["oid"]=>
      string(24) "54d3adc3ce7a792f4d703756"
    }
    upsertedId[4]: int(3)

### 参见

-   <span class="classname">MongoDB\\Driver\\BulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>
-   <span class="classname">MongoDB\\Driver\\WriteConcern</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeBulkWrite</span>

MongoDB\\Driver\\Manager::executeCommand
========================================

Execute a database command

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Manager::executeCommand</span> (
<span class="methodparam"><span class="type">string</span> `$db`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Selects a server according to the *"readPreference"* option and executes
the command on that server. By default, the read preference from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>
will be used.

This method applies no special logic to the command. Although this
method accepts *"readConcern"* and *"writeConcern"* options, which will
be incorporated into the command document, those options will not
default to corresponding values from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a> nor
will the MongoDB server version be taken into account. Users are
therefore encouraged to use specific read and/or write command methods
if possible.

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>readPreference</td>
<td><span class="classname">MongoDB\Driver\ReadPreference</span></td>
<td><p>A read preference to use for selecting a server for the operation.</p></td>
</tr>
<tr class="odd">
<td>session</td>
<td><span class="classname">MongoDB\Driver\Session</span></td>
<td><p>A session to associate with the operation.</p></td>
</tr>
<tr class="even">
<td>writeConcern</td>
<td><span class="classname">MongoDB\Driver\WriteConcern</span></td>
<td><p>A write concern to apply to the operation.</p></td>
</tr>
</tbody>
</table>

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command, issuing a write command to a
    secondary).

### 更新日志

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern. |
| 1.4.0 | The third parameter is now an `options` array. For backwards compatibility, this paramater will still accept a <span class="classname">MongoDB\\Driver\\ReadPreference</span> object.     |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::executeCommand</span> with a
command returning a single result document**

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$command = new MongoDB\Driver\Command(['ping' => 1]);

try {
    $cursor = $manager->executeCommand('admin', $command);
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}

/* The ping command returns a single result document, so we need to access the
 * first result in the cursor. */
$response = $cursor->toArray()[0];

var_dump($response);

?>
```

以上例程会输出：

    array(1) {
      ["ok"]=>
      float(1)
    }

**示例 \#2 <span
class="function">MongoDB\\Driver\\Manager::executeCommand</span> with a
command returning a cursor**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1, 'y' => 'foo']);
$bulk->insert(['x' => 2, 'y' => 'bar']);
$bulk->insert(['x' => 3, 'y' => 'bar']);
$manager->executeBulkWrite('db.collection', $bulk);

$command = new MongoDB\Driver\Command([
    'aggregate' => 'collection',
    'pipeline' => [
        ['$group' => ['_id' => '$y', 'sum' => ['$sum' => '$x']]],
    ],
    'cursor' => new stdClass,
]);
$cursor = $manager->executeCommand('db', $command);

/* The aggregate command can optionally return its results in a cursor instead
 * of a single result document. In this case, we can iterate on the cursor
 * directly to access those results. */
foreach ($cursor as $document) {
    var_dump($document);
}

?>
```

以上例程会输出：

    object(stdClass)#6 (2) {
      ["_id"]=>
      string(3) "bar"
      ["sum"]=>
      int(10)
    }
    object(stdClass)#7 (2) {
      ["_id"]=>
      string(3) "foo"
      ["sum"]=>
      int(2)
    }

**示例 \#3 Limiting execution time for a command**

The execution time of a command may be limited by specifying a value for
*"maxTimeMS"* in the <span
class="classname">MongoDB\\Driver\\Command</span> document. Note that
this time limit is enforced on the server side and does not take network
latency into account. See
<a href="https://docs.mongodb.com/manual/tutorial/terminate-running-operations/#maxtimems" class="link external">» Terminate Running Operations</a>
in the MongoDB manual for more information.

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');

$command = new MongoDB\Driver\Command([
    'count' => 'collection',
    'query' => ['x' => ['$gt' => 1]],
    'maxTimeMS' => 1000,
]);

$cursor = $manager->executeCommand('db', $command);

var_dump($cursor->toArray()[0]);

?>
```

If the command fails to complete after one second of execution time on
the server, a <span
class="classname">MongoDB\\Driver\\Exception\\ExecutionTimeoutException</span>
will be thrown.

### 注释

> **Note**: <span class="simpara"> If a secondary `readPreference` is
> used, it is the caller's responsibility to ensure that the `command`
> can be executed on a secondary. No validation is done by the driver.
> </span>

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeCommand</span>

MongoDB\\Driver\\Manager::executeQuery
======================================

Execute a database query

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Manager::executeQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Query</span> `$query`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Selects a server according to the *"readPreference"* option and executes
the query on that server. By default, the read preference from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>
will be used.

### 参数

`namespace` (<span class="type">string</span>)  
A fully qualified namespace (e.g. *"databaseName.collectionName"*).

`query` (<span class="classname">MongoDB\\Driver\\Query</span>)  
The query to execute.

`options`  
| Option         | Type                                                           | Description                                                        |
|----------------|----------------------------------------------------------------|--------------------------------------------------------------------|
| readPreference | <span class="classname">MongoDB\\Driver\\ReadPreference</span> | A read preference to use for selecting a server for the operation. |
| session        | <span class="classname">MongoDB\\Driver\\Session</span>        | A session to associate with the operation.                         |

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid query operators).

### 更新日志

| 版本  | 说明                                                                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.0 | The third parameter is now an `options` array. For backwards compatibility, this paramater will still accept a <span class="classname">MongoDB\\Driver\\ReadPreference</span> object. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::executeQuery</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$filter = ['x' => ['$gt' => 1]];
$options = [
    'projection' => ['_id' => 0],
    'sort' => ['x' => -1],
];

$query = new MongoDB\Driver\Query($filter, $options);
$cursor = $manager->executeQuery('db.collection', $query);

foreach ($cursor as $document) {
    var_dump($document);
}

?>
```

以上例程会输出：

    object(stdClass)#6 (1) {
      ["x"]=>
      int(3)
    }
    object(stdClass)#7 (1) {
      ["x"]=>
      int(2)
    }

**示例 \#2 Limiting execution time for a query**

The *"maxTimeMS"* <span class="classname">MongoDB\\Driver\\Query</span>
option may be used to limit the execution time of a query. Note that
this time limit is enforced on the server side and does not take network
latency into account. See
<a href="https://docs.mongodb.com/manual/tutorial/terminate-running-operations/#maxtimems" class="link external">» Terminate Running Operations</a>
in the MongoDB manual for more information.

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');

$filter = ['x' => ['$gt' => 1]];
$options = [
    'maxTimeMS' => 1000,
];

$query = new MongoDB\Driver\Query($filter, $options);
$cursor = $manager->executeQuery('db.collection', $query);

foreach ($cursor as $document) {
    var_dump($document);
}

?>
```

If the query fails to complete after one second of execution time on the
server, a <span
class="classname">MongoDB\\Driver\\Exception\\ExecutionTimeoutException</span>
will be thrown.

### 参见

-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span class="classname">MongoDB\\Driver\\Query</span>
-   <span class="classname">MongoDB\\Driver\\ReadPreference</span>
-   <span class="function">MongoDB\\Driver\\Server::executeQuery</span>

MongoDB\\Driver\\Manager::executeReadCommand
============================================

Execute a database command that reads

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Manager::executeReadCommand</span> (
<span class="methodparam"><span class="type">string</span> `$db`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Selects a server according to the *"readPreference"* option and executes
the command on that server. By default, the read preference from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>
will be used.

This method will apply logic that is specific to commands that read
(e.g.
<a href="https://docs.mongodb.com/manual/reference/command/count/" class="link external">» count</a>)
and take the MongoDB server version into account. The *"readConcern"*
option will default to the corresponding value from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>.

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>readPreference</td>
<td><span class="classname">MongoDB\Driver\ReadPreference</span></td>
<td><p>A read preference to use for selecting a server for the operation.</p></td>
</tr>
<tr class="odd">
<td>session</td>
<td><span class="classname">MongoDB\Driver\Session</span></td>
<td><p>A session to associate with the operation.</p></td>
</tr>
</tbody>
</table>

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command).

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadCommand</span>

MongoDB\\Driver\\Manager::executeReadWriteCommand
=================================================

Execute a database command that reads and writes

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Manager::executeReadWriteCommand</span>
( <span class="methodparam"><span class="type">string</span>
`$db`</span> , <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the command on the primary server.

This method will apply logic that is specific to commands that read and
write (e.g.
<a href="https://docs.mongodb.com/manual/reference/command/aggregate/" class="link external">» aggregate</a>)
and take the MongoDB server version into account. The *"readConcern"*
and *"writeConcern"* options will default to the corresponding values
from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>.

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>session</td>
<td><span class="classname">MongoDB\Driver\Session</span></td>
<td><p>A session to associate with the operation.</p></td>
</tr>
<tr class="odd">
<td>writeConcern</td>
<td><span class="classname">MongoDB\Driver\WriteConcern</span></td>
<td><p>A write concern to apply to the operation.</p></td>
</tr>
</tbody>
</table>

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command).

### 更新日志

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern. |

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadWriteCommand</span>

MongoDB\\Driver\\Manager::executeWriteCommand
=============================================

Execute a database command that writes

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Manager::executeWriteCommand</span>
( <span class="methodparam"><span class="type">string</span>
`$db`</span> , <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the command on the primary server.

This method will apply logic that is specific to commands that write
(e.g.
<a href="https://docs.mongodb.com/manual/reference/command/drop/" class="link external">» drop</a>)
and take the MongoDB server version into account. The *"writeConcern"*
option will default to the corresponding value from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>.

> **Note**: <span class="simpara"> This method is not intended to be
> used to execute
> <a href="https://docs.mongodb.com/manual/reference/command/insert/" class="link external">» insert</a>,
> <a href="https://docs.mongodb.com/manual/reference/command/update/" class="link external">» update</a>,
> or
> <a href="https://docs.mongodb.com/manual/reference/command/delete/" class="link external">» delete</a>
> commands. Users are encouraged to use <span
> class="function">MongoDB\\Driver\\Manager::executeBulkWrite</span> for
> those commands. </span>

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
| Option       | Type                                                         | Description                                |
|--------------|--------------------------------------------------------------|--------------------------------------------|
| session      | <span class="classname">MongoDB\\Driver\\Session</span>      | A session to associate with the operation. |
| writeConcern | <span class="classname">MongoDB\\Driver\\WriteConcern</span> | A write concern to apply to the operation. |

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command).

### 更新日志

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern. |

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeWriteCommand</span>

MongoDB\\Driver\\Manager::getReadConcern
========================================

Return the ReadConcern for the Manager

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\ReadConcern</span> <span
class="methodname">MongoDB\\Driver\\Manager::getReadConcern</span> (
<span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\ReadConcern</span>
for the Manager, which is derived from its URI options. This is the
default read concern for queries and commands executed on the Manager.

### 参数

此函数没有参数。

### 返回值

The <span class="classname">MongoDB\\Driver\\ReadConcern</span> for the
Manager.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::getReadConcern</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readConcernLevel=local');
var_dump($manager->getReadConcern());

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\ReadConcern)#2 (0) {
    }
    object(MongoDB\Driver\ReadConcern)#1 (1) {
      ["level"]=>
      string(5) "local"
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\ReadConcern</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::\_\_construct</span>

MongoDB\\Driver\\Manager::getReadPreference
===========================================

Return the ReadPreference for the Manager

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\ReadPreference</span> <span
class="methodname">MongoDB\\Driver\\Manager::getReadPreference</span> (
<span class="methodparam">void</span> )

Returns the <span
class="classname">MongoDB\\Driver\\ReadPreference</span> for the
Manager, which is derived from its URI options. This is the default read
preference for queries and commands executed on the Manager.

### 参数

此函数没有参数。

### 返回值

The <span class="classname">MongoDB\\Driver\\ReadPreference</span> for
the Manager.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::getReadPreference</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getReadPreference());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?readPreference=secondaryPreferred&readPreferenceTags=dc:ny,rack:1&readPreferenceTags=dc:ny&readPreferenceTags=');
var_dump($manager->getReadPreference());

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\ReadPreference)#2 (1) {
      ["mode"]=>
      string(7) "primary"
    }
    object(MongoDB\Driver\ReadPreference)#1 (2) {
      ["mode"]=>
      string(18) "secondaryPreferred"
      ["tags"]=>
      array(3) {
        [0]=>
        object(stdClass)#3 (2) {
          ["dc"]=>
          string(2) "ny"
          ["rack"]=>
          string(1) "1"
        }
        [1]=>
        object(stdClass)#4 (1) {
          ["dc"]=>
          string(2) "ny"
        }
        [2]=>
        object(stdClass)#5 (0) {
        }
      }
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\ReadPreference</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::\_\_construct</span>

MongoDB\\Driver\\Manager::getServers
====================================

Return the servers to which this manager is connected

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\Manager::getServers</span> ( <span
class="methodparam">void</span> )

Returns an <span class="type">array</span> of <span
class="classname">MongoDB\\Driver\\Server</span> instances to which this
manager is connected.

> **Note**: <span class="simpara"> Since the driver connects to the
> database lazily, this method may return an empty <span
> class="type">array</span> if called before executing an operation on
> the <span class="classname">MongoDB\\Driver\\Manager</span>. </span>

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">array</span> of <span
class="classname">MongoDB\\Driver\\Server</span> instances to which this
manager is connected.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::getServers</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

/* The driver connects to the database server lazily, so Manager::getServers()
 * may initially return an empty array. */
var_dump($manager->getServers());

$command = new MongoDB\Driver\Command(['ping' => 1]);
$manager->executeCommand('db', $command);

var_dump($manager->getServers());

?>
```

以上例程的输出类似于：

    array(0) {
    }
    array(1) {
      [0]=>
      object(MongoDB\Driver\Server)#3 (10) {
        ["host"]=>
        string(9) "localhost"
        ["port"]=>
        int(27017)
        ["type"]=>
        int(1)
        ["is_primary"]=>
        bool(false)
        ["is_secondary"]=>
        bool(false)
        ["is_arbiter"]=>
        bool(false)
        ["is_hidden"]=>
        bool(false)
        ["is_passive"]=>
        bool(false)
        ["last_is_master"]=>
        array(8) {
          ["ismaster"]=>
          bool(true)
          ["maxBsonObjectSize"]=>
          int(16777216)
          ["maxMessageSizeBytes"]=>
          int(48000000)
          ["maxWriteBatchSize"]=>
          int(1000)
          ["localTime"]=>
          object(MongoDB\BSON\UTCDateTime)#4 (1) {
            ["milliseconds"]=>
            int(1447267964517)
          }
          ["maxWireVersion"]=>
          int(3)
          ["minWireVersion"]=>
          int(0)
          ["ok"]=>
          float(1)
        }
        ["round_trip_time"]=>
        int(554)
      }
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\Server</span>
-   <span class="function">MongoDB\\Driver\\Manager::selectServer</span>

MongoDB\\Driver\\Manager::getWriteConcern
=========================================

Return the WriteConcern for the Manager

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteConcern</span> <span
class="methodname">MongoDB\\Driver\\Manager::getWriteConcern</span> (
<span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\WriteConcern</span>
for the Manager, which is derived from its URI options. This is the
default write concern for writes and commands executed on the Manager.

### 参数

此函数没有参数。

### 返回值

The <span class="classname">MongoDB\\Driver\\WriteConcern</span> for the
Manager.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Manager::getWriteConcern</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
var_dump($manager->getWriteConcern());

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017/?w=majority&wtimeoutMS=2000');
var_dump($manager->getWriteConcern());

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\WriteConcern)#2 (0) {
    }
    object(MongoDB\Driver\WriteConcern)#1 (2) {
      ["w"]=>
      string(8) "majority"
      ["wtimeout"]=>
      int(2000)
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\WriteConcern</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::\_\_construct</span>

MongoDB\\Driver\\Manager::selectServer
======================================

Select a server matching a read preference

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">MongoDB\\Driver\\Manager::selectServer</span> ( <span
class="methodparam"><span
class="type">MongoDB\\Driver\\ReadPreference</span>
`$readPreference`</span> )

Selects a <span class="classname">MongoDB\\Driver\\Server</span>
matching `readPreference`. This may be used to preselect a server in
order to perform version checking before executing an operation.

> **Note**: <span class="simpara"> Unlike <span
> class="function">MongoDB\\Driver\\Manager::getServers</span>, this
> method will initialize database connections and perform server
> discovery if necessary. See the
> <a href="https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst#single-threaded-server-selection" class="link external">» Server Selection Specification</a>
> for additional information. </span>

### 参数

`readPreference` (<span class="classname">MongoDB\\Driver\\ReadPreference</span>)  
The read preference to use for selecting a server.

### 返回值

Returns a <span class="classname">MongoDB\\Driver\\Server</span>
matching the read preference.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    if a server matching the read preference could not be found.

### 参见

-   <span class="classname">MongoDB\\Driver\\Server</span>
-   <span class="function">MongoDB\\Driver\\Manager::getServers</span>
-   <a href="https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst" class="link external">» Server Selection Specification</a>

MongoDB\\Driver\\Manager::startSession
======================================

Start a new client session for use with this client

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Session</span> <span
class="methodname">MongoDB\\Driver\\Manager::startSession</span> (\[
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

Creates a <span class="classname">MongoDB\\Driver\\Session</span> for
the given options. The session may then be specified when executing
commands, queries, and write operations.

> **Note**: <span class="simpara"> A <span
> class="classname">MongoDB\\Driver\\Session</span> can only be used
> with the <span class="classname">MongoDB\\Driver\\Manager</span> from
> which it was created. </span>

### 参数

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
<th>Default</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>causalConsistency</td>
<td><span class="type">boolean</span></td>
<td><p>Configure causal consistency in a session. If <strong><code>TRUE</code></strong>, each operation in the session will be causally ordered after the previous read or write operation. Set to <strong><code>FALSE</code></strong> to disable causal consistency.</p>
<p>See <a href="https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#causal-consistency" class="link external">» Casual Consistency</a> in the MongoDB manual for more information.</p></td>
<td><strong><code>TRUE</code></strong></td>
</tr>
<tr class="even">
<td>defaultTransactionOptions</td>
<td><span class="type">array</span></td>
<td><p>Default options to apply to newly created transactions. These options are used unless they are overridden when a transaction is started with different value for each option.</p>
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>maxCommitTimeMS</td>
<td>integer</td>
<td><p>The maximum amount of time in milliseconds to allow a single <em>commitTransaction</em> command to run.</p>
<p>If specified, <em>maxCommitTimeMS</em> must be a signed 32-bit integer greater than or equal to zero.</p></td>
</tr>
<tr class="even">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="odd">
<td>readPreference</td>
<td><span class="classname">MongoDB\Driver\ReadPreference</span></td>
<td><p>A read preference to use for selecting a server for the operation.</p></td>
</tr>
<tr class="even">
<td>writeConcern</td>
<td><span class="classname">MongoDB\Driver\WriteConcern</span></td>
<td><p>A write concern to apply to the operation.</p></td>
</tr>
</tbody>
</table>
<p>This option is available in MongoDB 4.0+.</p></td>
<td><em>[]</em></td>
</tr>
</tbody>
</table>

### 返回值

Returns a <span class="classname">MongoDB\\Driver\\Session</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    if the session could not be created (e.g. libmongoc does not support
    crypto).

### 更新日志

| 版本  | 说明                                                                       |
|-------|----------------------------------------------------------------------------|
| 1.6.0 | The *"maxCommitTimeMS"* option was added to *"defaultTransactionOptions"*. |
| 1.5.0 | The *"defaultTransactionOptions"* option was added.                        |

### 参见

-   <span class="classname">MongoDB\\Driver\\Session</span>
-   <a href="https://docs.mongodb.com/manual/core/read-isolation-consistency-recency/#causal-consistency" class="link external">» Casual Consistency</a>
    in the MongoDB manual

简介
----

The <span class="classname">MongoDB\\Driver\\Command</span> class is a
value object that represents a database command.

To provide “Command Helpers” the <span
class="classname">MongoDB\\Driver\\Command</span> object should be
composed.

类摘要
------

**MongoDB\\Driver\\Command**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Command** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">array\|object</span>
`$document`</span> \[, <span class="methodparam"><span
class="type">array</span> `$commandOptions`</span> \] )

}

范例
----

**示例 \#1 Composing <span
class="classname">MongoDB\\Driver\\Command</span> to provide a helper to
create collections**

``` php
<?php
class CreateCollection {
    protected $cmd = array();

    function __construct($collectionName) {
        $this->cmd["create"] = (string)$collectionName;
    }
    function setCappedCollection($maxBytes, $maxDocuments = false) {
        $this->cmd["capped"] = true;
        $this->cmd["size"]   = (int)$maxBytes;

        if ($maxDocuments) {
            $this->cmd["max"] = (int)$maxDocuments;
        }
    }
    function usePowerOf2Sizes($bool) {
        if ($bool) {
            $this->cmd["flags"] = 1;
        } else {
            $this->cmd["flags"] = 0;
        }
    }
    function setFlags($flags) {
        $this->cmd["flags"] = (int)$flags;
    }
    function getCommand() {
        return new MongoDB\Driver\Command($this->cmd);
    }
    function getCollectionName() {
        return $this->cmd["create"];
    }
}


$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$createCollection = new CreateCollection("cappedCollection");
$createCollection->setCappedCollection(64 * 1024);

try {
    $command = $createCollection->getCommand();
    $cursor = $manager->executeCommand("databaseName", $command);
    $response = $cursor->toArray()[0];
    var_dump($response);

    $collstats = ["collstats" => $createCollection->getCollectionName()];
    $cursor = $manager->executeCommand("databaseName", new MongoDB\Driver\Command($collstats));
    $response = $cursor->toArray()[0];
    var_dump($response);
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}

?>
```

以上例程会输出：

    object(MongoDB\Driver\Command)#3 (1) {
      ["command"]=>
      array(3) {
        ["create"]=>
        string(16) "cappedCollection"
        ["capped"]=>
        bool(true)
        ["size"]=>
        int(65536)
      }
    }
    array(1) {
      ["ok"]=>
      float(1)
    }
    array(16) {
      ["ns"]=>
      string(29) "databaseName.cappedCollection"
      ["count"]=>
      int(0)
      ["size"]=>
      int(0)
      ["numExtents"]=>
      int(1)
      ["storageSize"]=>
      int(65536)
      ["nindexes"]=>
      int(1)
      ["lastExtentSize"]=>
      float(65536)
      ["paddingFactor"]=>
      float(1)
      ["paddingFactorNote"]=>
      string(101) "paddingFactor is unused and unmaintained in 2.8. It remains hard coded to 1.0 for compatibility only."
      ["userFlags"]=>
      int(0)
      ["capped"]=>
      bool(true)
      ["max"]=>
      int(9223372036854775807)
      ["maxSize"]=>
      int(65536)
      ["totalIndexSize"]=>
      int(8176)
      ["indexSizes"]=>
      object(stdClass)#4 (1) {
        ["_id_"]=>
        int(8176)
      }
      ["ok"]=>
      float(1)
    }

MongoDB\\Driver\\Command::\_\_construct
=======================================

Create a new Command

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\Driver\\Command::\_\_construct</span>
( <span class="methodparam"><span class="type">array\|object</span>
`$document`</span> \[, <span class="methodparam"><span
class="type">array</span> `$commandOptions`</span> \] )

Constructs a new <span
class="classname">MongoDB\\Driver\\Command</span>, which is an immutable
value object that represents a database command. The command may then be
executed with <span
class="methodname">MongoDB\\Driver\\Manager::executeCommand</span>.

The complete command document, which includes the command name and its
options, should be expressed in the `document` parameter. The
`commandOptions` parameter is only used to specify options related to
the execution of the command and the resulting <span
class="classname">MongoDB\\Driver\\Cursor</span>.

### 参数

`document`  
The complete command document, which will be sent to the server.

`commandOptions`  
> **Note**: <span class="simpara"> Do not use this parameter to specify
> options described in the command's reference in the MongoDB manual.
> This parameter should only be used for the options explicitly listed
> below. </span>

| Option         | Type                              | Description                                                                                                                                                                                                                                                                                                                          |
|----------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| maxAwaitTimeMS | <span class="type">integer</span> | Positive integer denoting the time limit in milliseconds for the server to block a getMore operation if no data is available. This option should only be used in conjunction with commands that return a tailable cursor (e.g. <a href="https://docs.mongodb.com/manual/changeStreams/" class="link external">» Change Streams</a>). |

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                                                                    |
|-------|-----------------------------------------------------------------------------------------|
| 1.4.0 | Added a second `commandOptions` argument, which supports the *"maxAwaitTimeMS"* option. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Command::\_\_construct</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$command = new MongoDB\Driver\Command(array("buildinfo" => 1));

try {
    $cursor = $manager->executeCommand("admin", $command);
    $response = $cursor->toArray()[0];
} catch(MongoDB\Driver\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}
var_dump($response);

?>
```

以上例程的输出类似于：


    array(13) {
      ["version"]=>
      string(14) "2.8.0-rc2-pre-"
      ["gitVersion"]=>
      string(62) "b743d7158f7642f4da6b7eac8320374b3b88dc2e modules: subscription"
      ["OpenSSLVersion"]=>
      string(25) "OpenSSL 1.0.1f 6 Jan 2014"
      ["sysInfo"]=>
      string(104) "Linux infant 3.16.0-24-generic #32-Ubuntu SMP Tue Oct 28 13:07:32 UTC 2014 x86_64 BOOST_LIB_VERSION=1_49"
      ["loaderFlags"]=>
      string(91) "-fPIC -pthread -Wl,-z,now -rdynamic -Wl,-Bsymbolic-functions -Wl,-z,relro -Wl,-z,now -Wl,-E"
      ["compilerFlags"]=>
      string(301) "-Wnon-virtual-dtor -Woverloaded-virtual -std=c++11 -fPIC -fno-strict-aliasing -ggdb -pthread -Wall -Wsign-compare -Wno-unknown-pragmas -Winvalid-pch -pipe -Werror -O3 -Wno-unused-local-typedefs -Wno-unused-function -Wno-deprecated-declarations -Wno-unused-but-set-variable -fno-builtin-memcmp -std=c99"
      ["allocator"]=>
      string(8) "tcmalloc"
      ["versionArray"]=>
      array(4) {
        [0]=>
        int(2)
        [1]=>
        int(8)
        [2]=>
        int(0)
        [3]=>
        int(-8)
      }
      ["javascriptEngine"]=>
      string(2) "V8"
      ["bits"]=>
      int(64)
      ["debug"]=>
      bool(false)
      ["maxBsonObjectSize"]=>
      int(16777216)
      ["ok"]=>
      float(1)
    }

**示例 \#2 <span
class="function">MongoDB\\Driver\\Command::\_\_construct</span>
example**

Commands can accept options as well, as part of the normal structure
that you create to send to the server. For example, the *maxTimeMS*
option can be passed with most commands to restrict the amount of time a
specific command can run for on the server.

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$command = new MongoDB\Driver\Command(
    array(
        "distinct" => "beer",
        "key" => "beer_name",
        "maxTimeMS" => 10,
    )
);

try {
    $cursor = $manager->executeCommand("beerdb", $command);
    $response = $cursor->toArray()[0];
} catch(MongoDB\Driver\Exception\Exception $e) {
    echo $e->getMessage(), "\n";
    exit;
}
var_dump($response);

?>
```

以上例程的输出类似于：

  
operation exceeded time limit  

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeCommand</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>

简介
----

The <span class="classname">MongoDB\\Driver\\Query</span> class is a
value object that represents a database query.

类摘要
------

**MongoDB\\Driver\\Query**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Query** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">array\|object</span>
`$filter`</span> \[, <span class="methodparam"><span
class="type">array</span> `$queryOptions`</span> \] )

}

MongoDB\\Driver\\Query::\_\_construct
=====================================

Create a new Query

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\Driver\\Query::\_\_construct</span> (
<span class="methodparam"><span class="type">array\|object</span>
`$filter`</span> \[, <span class="methodparam"><span
class="type">array</span> `$queryOptions`</span> \] )

Constructs a new <span class="classname">MongoDB\\Driver\\Query</span>,
which is an immutable value object that represents a database query. The
query may then be executed with <span
class="methodname">MongoDB\\Driver\\Manager::executeQuery</span>.

### 参数

`filter` (<span class="type">array\|object</span>)  
The
<a href="https://docs.mongodb.com/manual/tutorial/query-documents/" class="link external">» query predicate</a>.
An empty predicate will match all documents in the collection.

> **Note**: <span class="simpara"> When evaluating query criteria,
> MongoDB compares types and values according to its own
> <a href="https://docs.mongodb.com/manual/reference/bson-type-comparison-order/" class="link external">» comparison rules for BSON types</a>,
> which differs from PHP's
> <a href="/types/comparisons.html" class="link">comparison</a> and
> <a href="/language/types/type-juggling.html" class="link">type juggling</a>
> rules. When matching a special BSON type the query criteria should use
> the respective
> <a href="/set/mongodb.html#MongoDB\BSON" class="link">BSON class</a>
> (e.g. use <span class="classname">MongoDB\\BSON\\ObjectId</span> to
> match an
> <a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ObjectId</a>).
> </span>

`queryOptions`  
<table>
<caption><strong>queryOptions</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>allowDiskUse</td>
<td><span class="type">boolean</span></td>
<td><p>Allows MongoDB to use temporary disk files to store data exceeding the 100 megabyte system memory limit while processing a blocking sort operation.</p></td>
</tr>
<tr class="even">
<td>allowPartialResults</td>
<td><span class="type">boolean</span></td>
<td><p>For queries against a sharded collection, returns partial results from the mongos if some shards are unavailable instead of throwing an error.</p>
<p>Falls back to the deprecated <em>"partial"</em> option if not specified.</p></td>
</tr>
<tr class="odd">
<td>awaitData</td>
<td><span class="type">boolean</span></td>
<td>Use in conjunction with the <em>"tailable"</em> option to block a getMore operation on the cursor temporarily if at the end of data rather than returning no data. After a timeout period, the query returns as normal.</td>
</tr>
<tr class="even">
<td>batchSize</td>
<td><span class="type">integer</span></td>
<td><p>The number of documents to return in the first batch. Defaults to 101. A batch size of 0 means that the cursor will be established, but no documents will be returned in the first batch.</p>
<p>In versions of MongoDB before 3.2, where queries use the legacy wire protocol OP_QUERY, a batch size of 1 will close the cursor irrespective of the number of matched documents.</p></td>
</tr>
<tr class="odd">
<td>collation</td>
<td><span class="type">array|object</span></td>
<td><p><a href="https://docs.mongodb.com/master/reference/collation/" class="link external">» Collation</a> allows users to specify language-specific rules for string comparison, such as rules for lettercase and accent marks. When specifying collation, the <em>"locale"</em> field is mandatory; all other collation fields are optional. For descriptions of the fields, see <a href="https://docs.mongodb.com/master/reference/collation/#collation-document" class="link external">» Collation Document</a>.</p>
<p>If the collation is unspecified but the collection has a default collation, the operation uses the collation specified for the collection. If no collation is specified for the collection or for the operation, MongoDB uses the simple binary comparison used in prior versions for string comparisons.</p>
<p>This option is available in MongoDB 3.4+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>comment</td>
<td><span class="type">string</span></td>
<td><p>A comment to attach to the query to help interpret and trace query profile data.</p>
<p>Falls back to the deprecated <em>"$comment"</em> modifier if not specified.</p></td>
</tr>
<tr class="odd">
<td>exhaust</td>
<td><span class="type">boolean</span></td>
<td><p>Stream the data down full blast in multiple "more" packages, on the assumption that the client will fully read all data queried. Faster when you are pulling a lot of data and know you want to pull it all down. Note: the client is not allowed to not read all the data unless it closes the connection.</p>
<p>This option is not supported by the find command in MongoDB 3.2+ and will force the driver to use the legacy wire protocol version (i.e. OP_QUERY).</p></td>
</tr>
<tr class="even">
<td>explain</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, the returned <span class="classname">MongoDB\Driver\Cursor</span> will contain a single document that describes the process and indexes used to return the query.</p>
<p>Falls back to the deprecated <em>"$explain"</em> modifier if not specified.</p>
<p>This option is not supported by the find command in MongoDB 3.2+ and will only be respected when using the legacy wire protocol version (i.e. OP_QUERY). The <a href="https://docs.mongodb.com/manual/reference/command/explain/" class="link external">» explain</a> command should be used on MongoDB 3.0+.</p></td>
</tr>
<tr class="odd">
<td>hint</td>
<td><span class="type">string|array|object</span></td>
<td><p>Index specification. Specify either the index name as a string or the index key pattern. If specified, then the query system will only consider plans using the hinted index.</p>
<p>Falls back to the deprecated <em>"hint"</em> option if not specified.</p></td>
</tr>
<tr class="even">
<td>limit</td>
<td><span class="type">integer</span></td>
<td><p>The maximum number of documents to return. If unspecified, then defaults to no limit. A limit of 0 is equivalent to setting no limit.</p>
<p>A negative limit is will be interpreted as a positive limit with the <em>"singleBatch"</em> option set to <strong><code>TRUE</code></strong>. This behavior is supported for backwards compatibility, but should be considered deprecated.</p></td>
</tr>
<tr class="odd">
<td>max</td>
<td><span class="type">array|object</span></td>
<td><p>The <em>exclusive</em> upper bound for a specific index.</p>
<p>Falls back to the deprecated <em>"$max"</em> modifier if not specified.</p></td>
</tr>
<tr class="even">
<td>maxAwaitTimeMS</td>
<td><span class="type">integer</span></td>
<td><p>Positive integer denoting the time limit in milliseconds for the server to block a getMore operation if no data is available. This option should only be used in conjunction with the <em>"tailable"</em> and <em>"awaitData"</em> options.</p></td>
</tr>
<tr class="odd">
<td>maxScan</td>
<td><span class="type">integer</span></td>
<td><div class="warning">
<strong>Warning</strong>
<p>This option is deprecated and should not be used.</p>
</div>
<p>Positive integer denoting the maximum number of documents or index keys to scan when executing the query.</p>
<p>Falls back to the deprecated <em>"$maxScan"</em> modifier if not specified.</p></td>
</tr>
<tr class="even">
<td>maxTimeMS</td>
<td><span class="type">integer</span></td>
<td><p>The cumulative time limit in milliseconds for processing operations on the cursor. MongoDB aborts the operation at the earliest following interrupt point.</p>
<p>Falls back to the deprecated <em>"$maxTimeMS"</em> modifier if not specified.</p></td>
</tr>
<tr class="odd">
<td>min</td>
<td><span class="type">array|object</span></td>
<td><p>The <em>inclusive</em> lower bound for a specific index.</p>
<p>Falls back to the deprecated <em>"$min"</em> modifier if not specified.</p></td>
</tr>
<tr class="even">
<td>modifiers</td>
<td><span class="type">array</span></td>
<td><a href="https://docs.mongodb.com/manual/reference/operator/query-modifier/" class="link external">» Meta operators</a> modifying the output or behavior of a query. Use of these operators is deprecated in favor of named options.</td>
</tr>
<tr class="odd">
<td>noCursorTimeout</td>
<td><span class="type">boolean</span></td>
<td>Prevents the server from timing out idle cursors after an inactivity period (10 minutes).</td>
</tr>
<tr class="even">
<td>oplogReplay</td>
<td><span class="type">boolean</span></td>
<td><p>Internal use for replica sets. To use oplogReplay, you must include the following condition in the filter:</p>
<div class="example-contents">
<div class="textcode">
<pre class="text"><code>[ &#39;ts&#39; =&gt; [ &#39;$gte&#39; =&gt; &lt;timestamp&gt; ] ]</code></pre>
</div>
</div>
<blockquote>
<p><strong>Note</strong>: <span class="simpara">This option is deprecated as of the 1.8.0 release.</span></p>
</blockquote></td>
</tr>
<tr class="odd">
<td>projection</td>
<td><span class="type">array|object</span></td>
<td><p>The <a href="https://docs.mongodb.com/manual/tutorial/project-fields-from-query-results/" class="link external">» projection specification</a> to determine which fields to include in the returned documents.</p>
<p>If you are using the <a href="/set/mongodb.html#Deserialization%20from%20BSON" class="link">ODM functionality</a> to deserialise documents as their original PHP class, make sure that you include the <span class="property">__pclass</span> field in the projection. This is required for the deserialization to work and without it, the driver will return (by default) a <span class="classname">stdClass</span> object instead.</p></td>
</tr>
<tr class="even">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation. By default, the read concern from the <a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a> will be used.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="odd">
<td>returnKey</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, returns only the index keys in the resulting documents. Default value is <strong><code>FALSE</code></strong>. If <strong><code>TRUE</code></strong> and the find command does not use an index, the returned documents will be empty.</p>
<p>Falls back to the deprecated <em>"$returnKey"</em> modifier if not specified.</p></td>
</tr>
<tr class="even">
<td>showRecordId</td>
<td><span class="type">boolean</span></td>
<td><p>Determines whether to return the record identifier for each document. If <strong><code>TRUE</code></strong>, adds a top-level <em>"$recordId"</em> field to the returned documents.</p>
<p>Falls back to the deprecated <em>"$showDiskLoc"</em> modifier if not specified.</p></td>
</tr>
<tr class="odd">
<td>singleBatch</td>
<td><span class="type">boolean</span></td>
<td>Determines whether to close the cursor after the first batch. Defaults to <strong><code>FALSE</code></strong>.</td>
</tr>
<tr class="even">
<td>skip</td>
<td><span class="type">integer</span></td>
<td>Number of documents to skip. Defaults to 0.</td>
</tr>
<tr class="odd">
<td>slaveOk</td>
<td><span class="type">boolean</span></td>
<td>Allow query of replica set secondaries</td>
</tr>
<tr class="even">
<td>snapshot</td>
<td><span class="type">boolean</span></td>
<td><div class="warning">
<strong>Warning</strong>
<p>This option is deprecated and should not be used.</p>
</div>
<p>Prevents the cursor from returning a document more than once because of an intervening write operation.</p>
<p>Falls back to the deprecated <em>"$snapshot"</em> modifier if not specified.</p></td>
</tr>
<tr class="odd">
<td>sort</td>
<td><span class="type">array|object</span></td>
<td><p>The sort specification for the ordering of the results.</p>
<p>Falls back to the deprecated <em>"$orderby"</em> modifier if not specified.</p></td>
</tr>
<tr class="even">
<td>tailable</td>
<td><span class="type">boolean</span></td>
<td>Returns a tailable cursor for a capped collection.</td>
</tr>
</tbody>
</table>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.8.0</td>
<td><p>Added the <em>"allowDiskUse"</em> option.</p>
<p>The <em>"oplogReplay"</em> option is deprecated.</p></td>
</tr>
<tr class="even">
<td>1.5.0</td>
<td><p>The <em>"maxScan"</em> and <em>"snapshot"</em> options are deprecated.</p></td>
</tr>
<tr class="odd">
<td>1.3.0</td>
<td><p>Added the <em>"maxAwaitTimeMS"</em> option.</p></td>
</tr>
<tr class="even">
<td>1.2.0</td>
<td><p>Added the <em>"allowPartialResults"</em>, <em>"collation"</em>, <em>"comment"</em>, <em>"hint"</em>, <em>"max"</em>, <em>"maxScan"</em>, <em>"maxTimeMS"</em>, <em>"min"</em>, <em>"returnKey"</em>, <em>"showRecordId"</em>, and <em>"snapshot"</em> options.</p>
<p>Renamed the <em>"partial"</em> option to <em>"allowPartialResults"</em>. For backwards compatibility, <em>"partial"</em> will still be read if <em>"allowPartialResults"</em> is not specified.</p>
<p>Removed the <em>"slaveOk"</em> option, which is obsolete. For queries using the legacy wire protocol OP_QUERY, the driver will set the <em>slaveOk</em> bit as needed in accordance with the <a href="https://github.com/mongodb/specifications/blob/master/source/server-selection/server-selection.rst" class="link external">» Server Selection Specification</a>.</p></td>
</tr>
<tr class="odd">
<td>1.1.0</td>
<td>Added the <em>"readConcern"</em> option.</td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Query::\_\_construct</span> example**

``` php
<?php
/* Select only documents authord by "bjori" with at least 100 views */
$filter = [
    'author' => 'bjori',
    'views' => [
        '$gte' => 100,
    ],
];

$options = [
    /* Only return the following fields in the matching documents */
    'projection' => [
        'title' => 1,
        'article' => 1,
    ],
    /* Return the documents in descending order of views */
    'sort' => [
        'views' => -1
    ],
];

$query = new MongoDB\Driver\Query($filter, $options);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$readPreference = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$cursor = $manager->executeQuery('databaseName.collectionName', $query, $readPreference);

foreach($cursor as $document) {
    var_dump($document);
}

?>
```

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeQuery</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>

简介
----

The <span class="classname">MongoDB\\Driver\\BulkWrite</span> collects
one or more write operations that should be sent to the server. After
adding any number of insert, update, and delete operations, the
collection may be executed via <span
class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>.

Write operations may either be ordered (default) or unordered. Ordered
write operations are sent to the server, in the order provided, for
serial execution. If a write fails, any remaining operations will be
aborted. Unordered operations are sent to the server in an arbitrary
order where they may be executed in parallel. Any errors that occur are
reported after all operations have been attempted.

类摘要
------

**MongoDB\\Driver\\BulkWrite**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\BulkWrite** </span> <span
class="oointerface">implements <span
class="interfacename">Countable</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`</span> \]
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">delete</span> ( <span class="methodparam"><span
class="type">array\|object</span> `$filter`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$deleteOptions`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">insert</span> ( <span class="methodparam"><span
class="type">array\|object</span> `$document`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">update</span> ( <span class="methodparam"><span
class="type">array\|object</span> `$filter`</span> , <span
class="methodparam"><span class="type">array\|object</span>
`$newObj`</span> \[, <span class="methodparam"><span
class="type">array</span> `$updateOptions`</span> \] )

}

范例
----

**示例 \#1 Mixed write operations are grouped by type**

Mixed write operations (i.e. inserts, updates, and deletes) will be
assembled into typed write commands to be sent sequentially to the
server.

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(['x' => 2], ['$set' => ['x' => 1]]);
$bulk->insert(['_id' => 3, 'x' => 3]);
$bulk->delete(['x' => 1]);

?>
```

Will result in four write commands (i.e. roundtrips) being executed.
Since the operations are ordered, the third insertion cannot be sent
until the preceding update is executed.

**示例 \#2 Ordered write operations causing an error**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->delete([]);
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 3, 'hello' => 'world']);
$bulk->update(['_id' => 3], ['$set' => ['hello' => 'earth']]);
$bulk->insert(['_id' => 4, 'hello' => 'pluto']);
$bulk->update(['_id' => 4], ['$set' => ['hello' => 'moon']]);
$bulk->insert(['_id' => 3]);
$bulk->insert(['_id' => 4]);
$bulk->insert(['_id' => 5]);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 1000);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    $result = $e->getWriteResult();

    // Check if the write concern could not be fulfilled
    if ($writeConcernError = $result->getWriteConcernError()) {
        printf("%s (%d): %s\n",
            $writeConcernError->getMessage(),
            $writeConcernError->getCode(),
            var_export($writeConcernError->getInfo(), true)
        );
    }

    // Check if any write operations did not complete at all
    foreach ($result->getWriteErrors() as $writeError) {
        printf("Operation#%d: %s (%d)\n",
            $writeError->getIndex(),
            $writeError->getMessage(),
            $writeError->getCode()
        );
    }
} catch (MongoDB\Driver\Exception\Exception $e) {
    printf("Other error: %s\n", $e->getMessage());
    exit;
}

printf("Inserted %d document(s)\n", $result->getInsertedCount());
printf("Updated  %d document(s)\n", $result->getModifiedCount());

?>
```

以上例程会输出：

    Operation#7: E11000 duplicate key error index: db.collection.$_id_ dup key: { : 3 } (11000)
    Inserted 4 document(s)
    Updated  2 document(s)

If the write concern could not be fullfilled, the example above would
output something like:

    waiting for replication timed out (64): array (
      'wtimeout' => true,
    )
    Operation#7: E11000 duplicate key error index: databaseName.collectionName.$_id_ dup key: { : 3 } (11000)
    Inserted 4 document(s)
    Updated  2 document(s)

If we execute the example above, but allow for unordered writes:

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => false]);
/* ... */

?>
```

以上例程会输出：

    Operation#7: E11000 duplicate key error index: db.collection.$_id_ dup key: { : 3 } (11000)
    Operation#8: E11000 duplicate key error index: db.collection.$_id_ dup key: { : 4 } (11000)
    Inserted 5 document(s)
    Updated  2 document(s)

参见
----

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>
-   <span class="classname">MongoDB\\Driver\\WriteConcern</span>
-   <span class="classname">MongoDB\\Driver\\WriteConcernError</span>
-   <span class="classname">MongoDB\\Driver\\WriteError</span>

MongoDB\\Driver\\BulkWrite::\_\_construct
=========================================

Create a new BulkWrite

### 说明

<span class="modifier">public</span> <span
class="methodname">MongoDB\\Driver\\BulkWrite::\_\_construct</span> (\[
<span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

Constructs a new <span
class="classname">MongoDB\\Driver\\BulkWrite</span>, which is a mutable
object to which one or more write operations may be added. The write(s)
may then be executed with <span
class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>.

### 参数

`options` (<span class="type">array</span>)  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
<th>Default</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>bypassDocumentValidation</td>
<td><span class="type">boolean</span></td>
<td><p>If <strong><code>TRUE</code></strong>, allows insert and update operations to circumvent document level validation.</p>
<p>This option is available in MongoDB 3.2+ and is ignored for older server versions, which do not support document level validation.</p></td>
<td><strong><code>FALSE</code></strong></td>
</tr>
<tr class="even">
<td>ordered</td>
<td><span class="type">boolean</span></td>
<td>Ordered operations (<strong><code>TRUE</code></strong>) are executed serially on the MongoDB server, while unordered operations (<strong><code>FALSE</code></strong>) are sent to the server in an arbitrary order and may be executed in parallel.</td>
<td><strong><code>TRUE</code></strong></td>
</tr>
</tbody>
</table>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                           |
|-------|------------------------------------------------|
| 1.1.0 | Added the *"bypassDocumentValidation"* option. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\BulkWrite::\_\_construct</span>
example**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite(['ordered' => true]);
$bulk->delete([]);
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(
    ['x' => 2],
    ['$set' => ['x' => 1]],
    ['limit' => 1, 'upsert' => false]
);
$bulk->delete(['x' => 1], ['limit' => 1]);
$bulk->update(
    ['_id' => 3],
    ['$set' => ['x' => 3]],
    ['limit' => 1, 'upsert' => true]
);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$writeConcern = new MongoDB\Driver\WriteConcern(1);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    $result = $e->getWriteResult();

    // Check if the write concern could not be fulfilled
    if ($writeConcernError = $result->getWriteConcernError()) {
        printf("%s (%d): %s\n",
            $writeConcernError->getMessage(),
            $writeConcernError->getCode(),
            var_export($writeConcernError->getInfo(), true)
        );
    }

    // Check if any write operations did not complete at all
    foreach ($result->getWriteErrors() as $writeError) {
        printf("Operation#%d: %s (%d)\n",
            $writeError->getIndex(),
            $writeError->getMessage(),
            $writeError->getCode()
        );
    }
} catch (MongoDB\Driver\Exception\Exception $e) {
    printf("Other error: %s\n", $e->getMessage());
    exit;
}

printf("Inserted %d document(s)\n", $result->getInsertedCount());
printf("Updated  %d document(s)\n", $result->getModifiedCount());
printf("Upserted %d document(s)\n", $result->getUpsertedCount());
printf("Deleted  %d document(s)\n", $result->getDeletedCount());

?>
```

以上例程会输出：

    Inserted 2 document(s)
    Updated  1 document(s)
    Upserted 1 document(s)
    Deleted  1 document(s)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>

MongoDB\\Driver\\BulkWrite::count
=================================

Count number of write operations in the bulk

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\BulkWrite::count</span> ( <span
class="methodparam">void</span> )

Returns the number of write operations added to the <span
class="classname">MongoDB\\Driver\\BulkWrite</span> object.

### 参数

此函数没有参数。

### 返回值

Returns number of write operations added to the <span
class="classname">MongoDB\\Driver\\BulkWrite</span> object.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.0 | Returns the number of write operations added to the <span class="classname">MongoDB\\Driver\\BulkWrite</span> object. Earlier versions returned the expected number of client-to-server roundtrips required to execute all write operations. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\BulkWrite::count</span> example**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1, 'x' => 1]);
$bulk->insert(['_id' => 2, 'x' => 2]);
$bulk->update(['x' => 2], ['$set' => ['x' => 1]]);
$bulk->delete(['x' => 1]);

var_dump(count($bulk));

?>
```

以上例程会输出：

    int(4)

MongoDB\\Driver\\BulkWrite::delete
==================================

Add a delete operation to the bulk

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MongoDB\\Driver\\BulkWrite::delete</span> (
<span class="methodparam"><span class="type">array\|object</span>
`$filter`</span> \[, <span class="methodparam"><span
class="type">array</span> `$deleteOptions`</span> \] )

Adds a delete operation to the <span
class="classname">MongoDB\\Driver\\BulkWrite</span>.

### 参数

`filter` (<span class="type">array\|object</span>)  
The
<a href="https://docs.mongodb.com/manual/tutorial/query-documents/" class="link external">» query predicate</a>.
An empty predicate will match all documents in the collection.

> **Note**: <span class="simpara"> When evaluating query criteria,
> MongoDB compares types and values according to its own
> <a href="https://docs.mongodb.com/manual/reference/bson-type-comparison-order/" class="link external">» comparison rules for BSON types</a>,
> which differs from PHP's
> <a href="/types/comparisons.html" class="link">comparison</a> and
> <a href="/language/types/type-juggling.html" class="link">type juggling</a>
> rules. When matching a special BSON type the query criteria should use
> the respective
> <a href="/set/mongodb.html#MongoDB\BSON" class="link">BSON class</a>
> (e.g. use <span class="classname">MongoDB\\BSON\\ObjectId</span> to
> match an
> <a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ObjectId</a>).
> </span>

`deleteOptions`  
<table>
<caption><strong>deleteOptions</strong></caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
<th>Default</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>collation</td>
<td><span class="type">array|object</span></td>
<td><p><a href="https://docs.mongodb.com/master/reference/collation/" class="link external">» Collation</a> allows users to specify language-specific rules for string comparison, such as rules for lettercase and accent marks. When specifying collation, the <em>"locale"</em> field is mandatory; all other collation fields are optional. For descriptions of the fields, see <a href="https://docs.mongodb.com/master/reference/collation/#collation-document" class="link external">» Collation Document</a>.</p>
<p>If the collation is unspecified but the collection has a default collation, the operation uses the collation specified for the collection. If no collation is specified for the collection or for the operation, MongoDB uses the simple binary comparison used in prior versions for string comparisons.</p>
<p>This option is available in MongoDB 3.4+ and will result in an exception at execution time if specified for an older server version.</p></td>
<td></td>
</tr>
<tr class="even">
<td>hint</td>
<td><span class="type">string|array|object</span></td>
<td><p>Index specification. Specify either the index name as a string or the index key pattern. If specified, then the query system will only consider plans using the hinted index.</p>
<p>This option is available in MongoDB 4.4+ and will result in an exception at execution time if specified for an older server version.</p></td>
<td></td>
</tr>
<tr class="odd">
<td>limit</td>
<td><span class="type">boolean</span></td>
<td>Delete all matching documents (<strong><code>FALSE</code></strong>), or only the first matching document (<strong><code>TRUE</code></strong>)</td>
<td><strong><code>FALSE</code></strong></td>
</tr>
</tbody>
</table>

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                            |
|-------|---------------------------------|
| 1.8.0 | Added the *"hint"* option.      |
| 1.2.0 | Added the *"collation"* option. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\BulkWrite::delete</span> example**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->delete(['x' => 1], ['limit' => 1]);
$bulk->delete(['x' => 2], ['limit' => 0]);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>

MongoDB\\Driver\\BulkWrite::insert
==================================

Add an insert operation to the bulk

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">MongoDB\\Driver\\BulkWrite::insert</span> (
<span class="methodparam"><span class="type">array\|object</span>
`$document`</span> )

Adds an insert operation to the <span
class="classname">MongoDB\\Driver\\BulkWrite</span>.

### 参数

`document` (<span class="type">array\|object</span>)  
A document to insert.

### 返回值

Returns the *\_id* of the inserted document. If the `document` did not
have an *\_id*, the <span
class="classname">MongoDB\\BSON\\ObjectId</span> generated for the
insert will be returned.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                            |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | The *\_id* of the inserted document is always returned. Previously, the method only returned a value if a <span class="classname">MongoDB\\BSON\\ObjectId</span> was generated. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\BulkWrite::insert</span> example**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite;

$document1 = ['title' => 'one'];
$document2 = ['_id' => 'custom ID', 'title' => 'two'];
$document3 = ['_id' => new MongoDB\BSON\ObjectId, 'title' => 'three'];

$_id1 = $bulk->insert($document1);
$_id2 = $bulk->insert($document2);
$_id3 = $bulk->insert($document3);

var_dump($_id1, $_id2, $_id3);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

以上例程的输出类似于：

    object(MongoDB\BSON\ObjectId)#3 (1) {
      ["oid"]=>
      string(24) "54d51146bd21b91405401d92"
    }
    NULL
    NULL

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>
-   <span class="classname">MongoDB\\BSON\\ObjectId</span>
-   <span class="interfacename">MongoDB\\BSON\\Persistable</span>

MongoDB\\Driver\\BulkWrite::update
==================================

Add an update operation to the bulk

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">MongoDB\\Driver\\BulkWrite::update</span> (
<span class="methodparam"><span class="type">array\|object</span>
`$filter`</span> , <span class="methodparam"><span
class="type">array\|object</span> `$newObj`</span> \[, <span
class="methodparam"><span class="type">array</span>
`$updateOptions`</span> \] )

Adds an update operation to the <span
class="classname">MongoDB\\Driver\\BulkWrite</span>.

### 参数

`filter` (<span class="type">array\|object</span>)  
The
<a href="https://docs.mongodb.com/manual/tutorial/query-documents/" class="link external">» query predicate</a>.
An empty predicate will match all documents in the collection.

> **Note**: <span class="simpara"> When evaluating query criteria,
> MongoDB compares types and values according to its own
> <a href="https://docs.mongodb.com/manual/reference/bson-type-comparison-order/" class="link external">» comparison rules for BSON types</a>,
> which differs from PHP's
> <a href="/types/comparisons.html" class="link">comparison</a> and
> <a href="/language/types/type-juggling.html" class="link">type juggling</a>
> rules. When matching a special BSON type the query criteria should use
> the respective
> <a href="/set/mongodb.html#MongoDB\BSON" class="link">BSON class</a>
> (e.g. use <span class="classname">MongoDB\\BSON\\ObjectId</span> to
> match an
> <a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ObjectId</a>).
> </span>

`newObj` (<span class="type">array\|object</span>)  
A document containing either update operators (e.g. *$set*), a
replacement document (i.e. *only* *field:value* expressions), or an
<a href="https://docs.mongodb.com/manual/reference/command/update/#update-with-an-aggregation-pipeline" class="link external">» aggregation pipeline</a>.

`updateOptions`  
<table>
<caption><strong>updateOptions</strong></caption>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
<th>Default</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>arrayFilters</td>
<td><span class="type">array</span></td>
<td><p>An array of filter documents that determines which array elements to modify for an update operation on an array field. See <a href="https://docs.mongodb.com/manual/reference/command/update/#update-command-arrayfilters" class="link external">» Specify arrayFilters for Array Update Operations</a> in the MongoDB manual for more information.</p>
<p>This option is available in MongoDB 3.6+ and will result in an exception at execution time if specified for an older server version.</p></td>
<td></td>
</tr>
<tr class="even">
<td>collation</td>
<td><span class="type">array|object</span></td>
<td><p><a href="https://docs.mongodb.com/master/reference/collation/" class="link external">» Collation</a> allows users to specify language-specific rules for string comparison, such as rules for lettercase and accent marks. When specifying collation, the <em>"locale"</em> field is mandatory; all other collation fields are optional. For descriptions of the fields, see <a href="https://docs.mongodb.com/master/reference/collation/#collation-document" class="link external">» Collation Document</a>.</p>
<p>If the collation is unspecified but the collection has a default collation, the operation uses the collation specified for the collection. If no collation is specified for the collection or for the operation, MongoDB uses the simple binary comparison used in prior versions for string comparisons.</p>
<p>This option is available in MongoDB 3.4+ and will result in an exception at execution time if specified for an older server version.</p></td>
<td></td>
</tr>
<tr class="odd">
<td>hint</td>
<td><span class="type">string|array|object</span></td>
<td><p>Index specification. Specify either the index name as a string or the index key pattern. If specified, then the query system will only consider plans using the hinted index.</p>
<p>This option is available in MongoDB 4.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
<td></td>
</tr>
<tr class="even">
<td>multi</td>
<td><span class="type">boolean</span></td>
<td>Update only the first matching document if <strong><code>FALSE</code></strong>, or all matching documents <strong><code>TRUE</code></strong>. This option cannot be <strong><code>TRUE</code></strong> if <code class="parameter">newObj</code> is a replacement document.</td>
<td><strong><code>FALSE</code></strong></td>
</tr>
<tr class="odd">
<td>upsert</td>
<td><span class="type">boolean</span></td>
<td>If <code class="parameter">filter</code> does not match an existing document, insert a <em>single</em> document. The document will be created from <code class="parameter">newObj</code> if it is a replacement document (i.e. no update operators); otherwise, the operators in <code class="parameter">newObj</code> will be applied to <code class="parameter">filter</code> to create the new document.</td>
<td><strong><code>FALSE</code></strong></td>
</tr>
</tbody>
</table>

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.7.0 | Added the *"hint"* option.                                                                                                                                                                   |
| 1.6.0 | The `newObj` parameter now accepts an aggregation pipeline. This feature requires MongoDB 4.2+ and will result in an exception at execution time if specified for an older server version.   |
| 1.5.0 | Using the *"arrayFilters"* option will result in an exception at execution time if unsupported by the server. Previously, no exception would be thrown and the option may have been ignored. |
| 1.4.0 | Added the *"arrayFilters"* option.                                                                                                                                                           |
| 1.2.0 | Added the *"collation"* option.                                                                                                                                                              |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\BulkWrite::update</span> example**

``` php
<?php

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->update(
    ['x' => 2],
    ['$set' => ['y' => 3]],
    ['multi' => false, 'upsert' => false]
);

$manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
$result = $manager->executeBulkWrite('db.collection', $bulk);

?>
```

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>

简介
----

<span class="classname">MongoDB\\Driver\\WriteConcern</span> describes
the level of acknowledgement requested from MongoDB for write operations
to a standalone *mongod* or to replica sets or to sharded clusters. In
sharded clusters, *mongos* instances will pass the write concern on to
the shards.

类摘要
------

**MongoDB\\Driver\\WriteConcern**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\WriteConcern** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Serializable</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\WriteConcern::MAJORITY` <span class="initializer"> =
"majority"</span> ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">bsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string\|integer</span>
`$w`</span> \[, <span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$journal`</span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">boolean\|null</span> <span
class="methodname">getJournal</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string\|integer\|null</span> <span
class="methodname">getW</span> ( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int\|MongoDB\\BSON\\Int64</span> <span
class="methodname">getWtimeout</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isDefault</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

预定义常量
----------

**`MongoDB\Driver\WriteConcern::MAJORITY`**  
Majority of all the members in the set; arbiters, non-voting members,
passive members, hidden members and delayed members are all included in
the definition of majority write concern.

更新日志
--------

| 版本  | 说明                                                                       |
|-------|----------------------------------------------------------------------------|
| 1.7.0 | Implements <span class="interfacename">Serializable</span>.                |
| 1.2.0 | Implements <span class="interfacename">MongoDB\\BSON\\Serializable</span>. |

MongoDB\\Driver\\WriteConcern::bsonSerialize
============================================

Returns an object for BSON serialization

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::bsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an object for serializing the WriteConcern as BSON.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcern::bsonSerialize</span>
with majority write concern**

``` php
<?php

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY);
var_dump($wc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($wc));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (1) {
      ["w"]=>
      string(8) "majority"
    }

    { "w" : "majority" }

**示例 \#2 <span
class="function">MongoDB\\Driver\\WriteConcern::bsonSerialize</span>
with wtimeout and journal**

``` php
<?php

$wc = new MongoDB\Driver\WriteConcern(2, 1000, true);
var_dump($wc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($wc));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (3) {
      ["w"]=>
      int(2)
      ["j"]=>
      bool(true)
      ["wtimeout"]=>
      int(1000)
    }

    { "w" : 2, "j" : true, "wtimeout" : 1000 }

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcern::\_\_construct
============================================

Create a new WriteConcern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span
class="methodname">MongoDB\\Driver\\WriteConcern::\_\_construct</span> (
<span class="methodparam"><span class="type">string\|integer</span>
`$w`</span> \[, <span class="methodparam"><span class="type">int</span>
`$wtimeout`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$journal`</span> \]\] )

Constructs a new <span
class="classname">MongoDB\\Driver\\WriteConcern</span>, which is an
immutable value object.

### 参数

`w`  
<table>
<caption><strong>Write concern</strong></caption>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Requests acknowledgement that the write operation has propagated to the standalone <em>mongod</em> or the primary in a replica set. This is the default write concern for MongoDB.</td>
</tr>
<tr class="even">
<td>0</td>
<td>Requests no acknowledgment of the write operation. However, this may return information about socket exceptions and networking errors to the application.</td>
</tr>
<tr class="odd">
<td>&lt;integer greater than 1&gt;</td>
<td>Numbers greater than 1 are valid only for replica sets to request acknowledgement from specified number of members, including the primary.</td>
</tr>
<tr class="even">
<td><strong><code>MongoDB\Driver\WriteConcern::MAJORITY</code></strong></td>
<td><p>Requests acknowledgment that write operations have propagated to the majority of voting nodes, including the primary, and have been written to the on-disk journal for these nodes.</p>
<p>Prior to MongoDB 3.0, this refers to the majority of replica set members (not just voting nodes).</p></td>
</tr>
<tr class="odd">
<td>string</td>
<td>A string value is interpereted as a tag set. Requests acknowledgement that the write operations have propagated to a replica set member with the specified tag.</td>
</tr>
</tbody>
</table>

`wtimeout`  
How long to wait (in milliseconds) for secondaries before failing.

*wtimeout* causes write operations to return with an error (<span
class="classname">WriteConcernError</span>) after the specified limit,
even if the required write concern will eventually succeed. When these
write operations return, MongoDB does not undo successful data
modifications performed before the write concern exceeded the *wtimeout*
time limit.

If specified, *wtimeout* must be a signed 64-bit integer greater than or
equal to zero.

| Value                      | Description                              |
|----------------------------|------------------------------------------|
| 0                          | Block indefinitely. This is the default. |
| \<integer greater than 0\> | Milliseconds to wait until returning.    |

`journal`  
Wait until mongod has applied the write to the journal.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `w` is invalid or `wtimeout` is either negative or greater than
    the bounds of a signed 32-bit integer.

### 更新日志

| 版本  | 说明                                                |
|-------|-----------------------------------------------------|
| 1.7.0 | The `wTimeout` parameter now accepts 64-bit values. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcern::\_\_construct</span>
example**

``` php
<?php

/* Request write acknowledgement from the majority of the replica set nodes */
$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 500);

/* Request write acknowledgement from a node configured with the "MultipleDC" tag */
$wc = new MongoDB\Driver\WriteConcern("MultipleDC", 500);

?>
```

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcern::getJournal
=========================================

Returns the WriteConcern's "journal" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">boolean\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::getJournal</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteConcern's "journal" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcern::getJournal</span>
example**

``` php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getJournal());

$wc = new MongoDB\Driver\WriteConcern(1, 0, true);
var_dump($wc->getJournal());

$wc = new MongoDB\Driver\WriteConcern(1, 0, false);
var_dump($wc->getJournal());

?>
```

以上例程会输出：

    NULL
    bool(true)
    bool(false)

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcern::getW
===================================

Returns the WriteConcern's "w" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string\|integer\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::getW</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteConcern's "w" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcern::getW</span> example**

``` php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getW());

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY);
var_dump($wc->getW());

?>
```

以上例程会输出：

    int(1)
    string(8) "majority"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcern::getWtimeout
==========================================

Returns the WriteConcern's "wtimeout" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int\|MongoDB\\BSON\\Int64</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::getWtimeout</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteConcern's "wtimeout" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.7.0 | On 32-bit systems, this method will return a <span class="classname">MongoDB\\BSON\\Int64</span> instance if the WriteConcern object was created with a *wTimeout* that exceeds the 32-bit range. On 64-bit systems, this method will always return an integer value. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcern::getWtimeout</span>
example**

``` php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->getWtimeout());

$wc = new MongoDB\Driver\WriteConcern(MongoDB\Driver\WriteConcern::MAJORITY, 3000);
var_dump($wc->getWtimeout());

?>
```

以上例程会输出：

    int(0)
    int(3000)

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcern::isDefault
========================================

Checks if this is the default write concern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::isDefault</span> (
<span class="methodparam">void</span> )

Returns whether this is the default write concern (i.e. no options are
specified). This method is primarily intended to be used in conjunction
with <span
class="methodname">MongoDB\\Driver\\Manager::getWriteConcern</span> to
determine whether the Manager has been constructed without any write
concern options.

The driver will not include a default write concern in its write
operations (e.g. <span
class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>) in
order to allow the server to apply its own default, which may have been
<a href="https://docs.mongodb.com/manual/core/replica-set-write-concern/#modify-default-write-concern" class="link external">» modified</a>.
Libraries that access the Manager's write concern to include it in their
own write commands should use this method to ensure that default write
concerns are left unset.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this is the default write concern and **`FALSE`**
otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcern::isDefault</span>
example**

``` php
<?php

$wc = new MongoDB\Driver\WriteConcern(1);
var_dump($wc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/?w=majority');
$wc = $manager->getWriteConcern();
var_dump($wc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/');
$wc = $manager->getWriteConcern();
var_dump($wc->isDefault());

?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(true)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::getWriteConcern</span>
-   <a href="https://docs.mongodb.com/manual/core/replica-set-write-concern/#modify-default-write-concern" class="link external">» Modify Default Write Concern</a>
    in the MongoDB manual
-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcern::serialize
========================================

Serialize a WriteConcern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::serialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\Driver\\WriteConcern</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteConcern::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\Driver\\WriteConcern::unserialize
==========================================

Unserialize a WriteConcern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\WriteConcern::unserialize</span> (
<span class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span
class="classname">MongoDB\\Driver\\WriteConcern</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\Driver\\WriteConcern</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteConcern::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

类摘要
------

**MongoDB\\Driver\\ReadPreference**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\ReadPreference** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Serializable</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::RP_PRIMARY` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED` <span
class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::RP_SECONDARY` <span class="initializer">
= 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED` <span
class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::RP_NEAREST` <span class="initializer"> =
10</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadPreference::PRIMARY` <span class="initializer"> =
primary</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED` <span
class="initializer"> = primaryPreferred</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadPreference::SECONDARY` <span class="initializer"> =
secondary</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED` <span
class="initializer"> = secondaryPreferred</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadPreference::NEAREST` <span class="initializer"> =
nearest</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS` <span
class="initializer"> = -1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS` <span
class="initializer"> = 90</span> ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">bsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string\|integer</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tagSets`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">getHedge</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getMaxStalenessSeconds</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getMode</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getModeString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">getTagSets</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

预定义常量
----------

**`MongoDB\Driver\ReadPreference::RP_PRIMARY`**  
All operations read from the current replica set primary. This is the
default read preference for MongoDB.

**`MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED`**  
In most situations, operations read from the primary but if it is
unavailable, operations read from secondary members.

**`MongoDB\Driver\ReadPreference::RP_SECONDARY`**  
All operations read from the secondary members of the replica set.

**`MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED`**  
In most situations, operations read from secondary members but if no
secondary members are available, operations read from the primary.

**`MongoDB\Driver\ReadPreference::RP_NEAREST`**  
Operations read from member of the replica set with the least network
latency, irrespective of the member's type.

**`MongoDB\Driver\ReadPreference::PRIMARY`**  
All operations read from the current replica set primary. This is the
default read preference for MongoDB.

**`MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED`**  
In most situations, operations read from the primary but if it is
unavailable, operations read from secondary members.

**`MongoDB\Driver\ReadPreference::SECONDARY`**  
All operations read from the secondary members of the replica set.

**`MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED`**  
In most situations, operations read from secondary members but if no
secondary members are available, operations read from the primary.

**`MongoDB\Driver\ReadPreference::NEAREST`**  
Operations read from member of the replica set with the least network
latency, irrespective of the member's type.

**`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`**  
The default value for the *"maxStalenessSeconds"* option is to specify
no limit on maximum staleness, which means that the driver will not
consider a secondary's lag when choosing where to direct a read
operation.

**`MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS`**  
The minimum value for the *"maxStalenessSeconds"* option is 90 seconds.
The driver estimates secondaries' staleness by periodically checking the
latest write date of each replica set member. Since these checks are
infrequent, the staleness estimate is coarse. Thus, the driver cannot
enforce a max staleness value of less than 90 seconds.

更新日志
--------

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.7.0</td>
<td><p>Added the <strong><code>MongoDB\Driver\ReadPreference::PRIMARY</code></strong>, <strong><code>MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED</code></strong>, <strong><code>MongoDB\Driver\ReadPreference::SECONDARY</code></strong>, <strong><code>MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED</code></strong>, <strong><code>MongoDB\Driver\ReadPreference::NEAREST</code></strong> constants.</p>
<p>Implements <span class="interfacename">Serializable</span>.</p></td>
</tr>
<tr class="even">
<td>1.2.0</td>
<td><p>Added the <strong><code>MongoDB\Driver\ReadPreference::NO_MAX_STALENESS</code></strong> and <strong><code>MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS</code></strong> constants.</p>
<p>Implements <span class="interfacename">MongoDB\BSON\Serializable</span>.</p></td>
</tr>
</tbody>
</table>

MongoDB\\Driver\\ReadPreference::bsonSerialize
==============================================

Returns an object for BSON serialization

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::bsonSerialize</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an object for serializing the ReadPreference as BSON.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadPreference::bsonSerialize</span>
with primary read preference**

``` php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
var_dump($rp->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rp));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (1) {
      ["mode"]=>
      string(7) "primary"
    }

    { "mode" : "primary" }

**示例 \#2 <span
class="function">MongoDB\\Driver\\ReadPreference::bsonSerialize</span>
with secondary read preference and tag sets**

``` php
<?php

$rp = new MongoDB\Driver\ReadPreference(
    MongoDB\Driver\ReadPreference::RP_SECONDARY,
    [
        ['dc' => 'ny'],
        ['dc' => 'sf', 'use' => 'reporting'],
        []
    ]
);
var_dump($rp->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rp));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (2) {
      ["mode"]=>
      string(9) "secondary"
      ["tags"]=>
      array(3) {
        [0]=>
        object(stdClass)#1 (1) {
          ["dc"]=>
          string(2) "ny"
        }
        [1]=>
        object(stdClass)#5 (2) {
          ["dc"]=>
          string(2) "sf"
          ["use"]=>
          string(9) "reporting"
        }
        [2]=>
        object(stdClass)#4 (0) {
        }
      }
    }

    { "mode" : "secondary", "tags" : [ { "dc" : "ny" }, { "dc" : "sf", "use" : "reporting" }, {  } ] }

**示例 \#3 <span
class="function">MongoDB\\Driver\\ReadPreference::bsonSerialize</span>
with secondary read preference and max staleness**

``` php
<?php

$rp = new MongoDB\Driver\ReadPreference(
    MongoDB\Driver\ReadPreference::RP_SECONDARY,
    null,
    ['maxStalenessSeconds' => 120]
);
var_dump($rp->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rp));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (2) {
      ["mode"]=>
      string(9) "secondary"
      ["maxStalenessSeconds"]=>
      int(120)
    }

    { "mode" : "secondary", "maxStalenessSeconds" : 120 }

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::\_\_construct
==============================================

Create a new ReadPreference

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span
class="methodname">MongoDB\\Driver\\ReadPreference::\_\_construct</span>
( <span class="methodparam"><span class="type">string\|integer</span>
`$mode`</span> \[, <span class="methodparam"><span
class="type">array</span> `$tagSets`<span class="initializer"> =
**`NULL`**</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \]\] )

Constructs a new <span
class="classname">MongoDB\\Driver\\ReadPreference</span>, which is an
immutable value object.

### 参数

`mode`  
| Value                                                                                 | Description                                                                                                                             |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **`MongoDB\Driver\ReadPreference::RP_PRIMARY`** or *"primary"*                        | All operations read from the current replica set primary. This is the default read preference for MongoDB.                              |
| **`MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED`** or *"primaryPreferred"*     | In most situations, operations read from the primary but if it is unavailable, operations read from secondary members.                  |
| **`MongoDB\Driver\ReadPreference::RP_SECONDARY`** or *"secondary"*                    | All operations read from the secondary members of the replica set.                                                                      |
| **`MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED`** or *"secondaryPreferred"* | In most situations, operations read from secondary members but if no secondary members are available, operations read from the primary. |
| **`MongoDB\Driver\ReadPreference::RP_NEAREST`** or *"nearest"*                        | Operations read from member of the replica set with the least network latency, irrespective of the member's type.                       |

`tagSets`  
Tag sets allow you to target read operations to specific members of a
replica set. This parameter should be an array of associative arrays,
each of which contain zero or more key/value pairs. When selecting a
server for a read operation, the driver attempt to select a node having
all tags in a set (i.e. the associative array of key/value pairs). If
selection fails, the driver will attempt subsequent sets. An empty tag
set (*array()*) will match any node and may be used as a fallback.

Tags are not compatible with the
**`MongoDB\Driver\ReadPreference::RP_PRIMARY`** mode and, in general,
only apply when selecting a secondary member of a set for a read
operation. However, the **`MongoDB\Driver\ReadPreference::RP_NEAREST`**
mode, when combined with a tag set, selects the matching member with the
lowest network latency. This member may be a primary or secondary.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>hedge</td>
<td><span class="type">object|array</span></td>
<td><p>Specifies whether to use <a href="https://docs.mongodb.com/manual/core/sharded-cluster-query-router/#mongos-hedged-reads" class="link external">» hedged reads</a>, which are supported by MongoDB 4.4+ for sharded queries.</p>
<p>Server hedged reads are available for all non-primary read preferences and are enabled by default when using the <em>"nearest"</em> mode. This option allows explicitly enabling server hedged reads for non-primary read preferences by specifying <em>['enabled' =&gt; true]</em>, or explicitly disabling server hedged reads for the <em>"nearest"</em> read preference by specifying <em>['enabled' =&gt; false]</em>.</p></td>
</tr>
<tr class="even">
<td>maxStalenessSeconds</td>
<td><span class="type">integer</span></td>
<td><p>Specifies a maximum replication lag, or "staleness", for reads from secondaries. When a secondary's estimated staleness exceeds this value, the driver stops using it for read operations.</p>
<p>If specified, the max staleness must be a signed 32-bit integer greater than or equal to <strong><code>MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS</code></strong>.</p>
<p>Defaults to <strong><code>MongoDB\Driver\ReadPreference::NO_MAX_STALENESS</code></strong>, which means that the driver will not consider a secondary's lag when choosing where to direct a read operation.</p>
<p>This option is not compatible with the <strong><code>MongoDB\Driver\ReadPreference::RP_PRIMARY</code></strong> mode. Specifying a max staleness also requires all MongoDB instances in the deployment to be using MongoDB 3.4+. An exception will be thrown at execution time if any MongoDB instances in the deployment are of an older server version.</p></td>
</tr>
</tbody>
</table>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `mode` is invalid.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `tagSets` is provided for a primary read preference or is
    malformed (i.e. not an array of zero or more documents).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"maxStalenessSeconds"* option is provided for a primary read
    preference or is out of range.

### 更新日志

| 版本  | 说明                                                                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.8.0 | Added the *"hedge"* option.                                                                                                                                                           |
| 1.3.0 | The `mode` argument now accepts a string value, which is consistent with the *"readPreference"* URI option for <span class="function">MongoDB\\Driver\\Manager::\_\_construct</span>. |
| 1.2.0 | Added a third `options` argument, which supports the *"maxStalenessSeconds"* option.                                                                                                  |

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadPreference::\_\_construct</span>
example**

``` php
<?php

/* Prefer a secondary node but fall back to a primary. */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED));

/* Prefer a node in the New York data center with lowest latency. */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_NEAREST, [['dc' => 'ny']]));

/* Require a secondary node whose replication lag is within two minutes of the primary */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, ['maxStalenessSeconds' => 120]));

/* Explicitly enable server hedged reads */
var_dump(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, ['hedge' => ['enabled' => true]]));

?>
```

以上例程会输出：

    object(MongoDB\Driver\ReadPreference)#1 (1) {
      ["mode"]=>
      string(18) "secondaryPreferred"
    }
    object(MongoDB\Driver\ReadPreference)#1 (2) {
      ["mode"]=>
      string(7) "nearest"
      ["tags"]=>
      array(1) {
        [0]=>
        object(stdClass)#2 (1) {
          ["dc"]=>
          string(2) "ny"
        }
      }
    }
    object(MongoDB\Driver\ReadPreference)#1 (2) {
      ["mode"]=>
      string(9) "secondary"
      ["maxStalenessSeconds"]=>
      int(120)
    }
    object(MongoDB\Driver\ReadPreference)#1 (2) {
      ["mode"]=>
      string(9) "secondary"
      ["hedge"]=>
      object(stdClass)#1 (1) {
        ["enabled"]=>
        bool(true)
      }
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::getHedge
=========================================

Returns the ReadPreference's "hedge" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::getHedge</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the ReadPreference's "hedge" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds
=======================================================

Returns the ReadPreference's "maxStalenessSeconds" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the ReadPreference's "maxStalenessSeconds" option. If no max
staleness has been specified,
**`MongoDB\Driver\ReadPreference::NO_MAX_STALENESS`** will be returned.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds</span>
example**

``` php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => MongoDB\Driver\ReadPreference::NO_MAX_STALENESS,
]);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => MongoDB\Driver\ReadPreference::SMALLEST_MAX_STALENESS_SECONDS,
]);
var_dump($rp->getMaxStalenessSeconds());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY, null, [
    'maxStalenessSeconds' => 1000,
]);
var_dump($rp->getMaxStalenessSeconds());

?>
```

以上例程会输出：

    int(-1)
    int(-1)
    int(90)
    int(1000)

### 参见

-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::getMode
========================================

Returns the ReadPreference's "mode" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::getMode</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the ReadPreference's "mode" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadPreference::getMode</span>
example**

``` php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY_PREFERRED);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED);
var_dump($rp->getMode());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_NEAREST);
var_dump($rp->getMode());

?>
```

以上例程会输出：

    int(1)
    int(5)
    int(2)
    int(6)
    int(10)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\ReadPreference::getModeString</span>
-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::getModeString
==============================================

Returns the ReadPreference's "mode" option as a string

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::getModeString</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the ReadPreference's "mode" option as a string.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadPreference::getModeString</span>
example**

``` php
<?php

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::PRIMARY);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::PRIMARY_PREFERRED);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::SECONDARY);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::SECONDARY_PREFERRED);
var_dump($rp->getModeString());

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::NEAREST);
var_dump($rp->getModeString());

?>
```

以上例程会输出：

    string(7) "primary"
    string(16) "primaryPreferred"
    string(9) "secondary"
    string(18) "secondaryPreferred"
    string(7) "nearest"

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\ReadPreference::getMode</span>
-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::getTagSets
===========================================

Returns the ReadPreference's "tagSets" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::getTagSets</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the ReadPreference's "tagSets" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadPreference::getTagSets</span>
example**

``` php
<?php

$mode = MongoDB\Driver\ReadPreference::RP_SECONDARY_PREFERRED;

/* Null and an empty array both denote no tag set preference. */
$rp = new MongoDB\Driver\ReadPreference($mode, null);
var_dump($rp->getTagSets());

$rp = new MongoDB\Driver\ReadPreference($mode, []);
var_dump($rp->getTagSets());

/* Prefer a node in New York, but fall back to any available node. */
$rp = new MongoDB\Driver\ReadPreference($mode, [['dc' => 'ny']]);
var_dump($rp->getTagSets());

/* Prefer a node in the New York, followed by a node in San Francisco that is
   labeled for reporting usage, and finally fall back to any available node. */
$rp = new MongoDB\Driver\ReadPreference($mode, [
  ['dc' => 'ny'],
  ['dc' => 'sf', 'use' => 'reporting'],
  [],
]);
var_dump($rp->getTagSets());

?>
```

以上例程会输出：

    array(0) {
    }
    array(0) {
    }
    array(2) {
      [0]=>
      array(1) {
        ["dc"]=>
        string(2) "ny"
      }
      [1]=>
      array(0) {
      }
    }
    array(3) {
      [0]=>
      array(1) {
        ["dc"]=>
        string(2) "ny"
      }
      [1]=>
      array(2) {
        ["dc"]=>
        string(2) "sf"
        ["use"]=>
        string(9) "reporting"
      }
      [2]=>
      array(0) {
      }
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/core/read-preference/" class="link external">» Read Preference reference</a>

MongoDB\\Driver\\ReadPreference::serialize
==========================================

Serialize a ReadPreference

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::serialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\Driver\\ReadPreference</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\ReadPreference::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\Driver\\ReadPreference::unserialize
============================================

Unserialize a ReadPreference

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\ReadPreference::unserialize</span> (
<span class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span
class="classname">MongoDB\\Driver\\ReadPreference</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\Driver\\ReadPreference</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\ReadPreference::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

<span class="classname">MongoDB\\Driver\\ReadConcern</span> controls the
level of isolation for read operations for replica sets and replica set
shards. This option requires MongoDB 3.2 or later.

类摘要
------

**MongoDB\\Driver\\ReadConcern**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\ReadConcern** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Serializable</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadConcern::AVAILABLE` <span class="initializer"> =
"available"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadConcern::LINEARIZABLE` <span class="initializer"> =
"linearizable"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadConcern::LOCAL` <span class="initializer"> =
"local"</span> ;

<span class="modifier">const</span> <span class="type">string</span>
`MongoDB\Driver\ReadConcern::MAJORITY` <span class="initializer"> =
"majority"</span> ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">bsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$level`</span> \]
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string\|null</span> <span
class="methodname">getLevel</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isDefault</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

预定义常量
----------

**`MongoDB\Driver\ReadConcern::AVAILABLE`**  
Default for reads against secondaries when *afterClusterTime*and *level*
are unspecified.

The query returns the instance's most recent data. Provides no guarantee
that the data has been written to a majority of the replica set members
(i.e. may be rolled back).

For unsharded collections (including collections in a standalone
deployment or a replica set deployment), *"local"* and *"available"*
read concerns behave identically.

For a sharded cluster, *"available"* read concern provides greater
tolerance for partitions since it does not wait to ensure consistency
guarantees. However, a query with *"available"* read concern may return
orphan documents if the shard is undergoing chunk migrations since the
*"available"* read concern, unlike *"local"* read concern, does not
contact the shard's primary nor the config servers for updated metadata.

**`MongoDB\Driver\ReadConcern::LINEARIZABLE`**  
The query returns data that reflects all successful writes issued with a
write concern of *"majority"* *and* acknowledged prior to the start of
the read operation. For replica sets that run with
*writeConcernMajorityJournalDefault* set to **`TRUE`**, linearizable
read concern returns data that will never be rolled back.

With *writeConcernMajorityJournalDefault* set to **`FALSE`**, MongoDB
will not wait for *w: "majority"* writes to be durable before
acknowledging the writes. As such, *"majority"* write operations could
possibly roll back in the event of a loss of a replica set member.

You can specify linearizable read concern for read operations on the
primary only.

Linearizable read concern guarantees only apply if read operations
specify a query filter that uniquely identifies a single document.

**小贴士**
Always use *maxTimeMS* with linearizable read concern in case a majority
of data bearing members are unavailable. *maxTimeMS* ensures that the
operation does not block indefinitely and instead ensures that the
operation returns an error if the read concern cannot be fulfilled.

Linearizable read concern requires MongoDB 3.4.

**`MongoDB\Driver\ReadConcern::LOCAL`**  
Default for reads against primary if *level* is unspecified and for
reads against secondaries if *level* is unspecified but
*afterClusterTime* is specified.

The query returns the instance's most recent data. Provides no guarantee
that the data has been written to a majority of the replica set members
(i.e. may be rolled back).

**`MongoDB\Driver\ReadConcern::MAJORITY`**  
The query returns the instance's most recent data acknowledged as having
been written to a majority of members in the replica set.

To use read concern level of *"majority"*, replica sets must use
WiredTiger storage engine and election protocol version 1.

更新日志
--------

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.7.0</td>
<td>Implements <span class="interfacename">Serializable</span>.</td>
</tr>
<tr class="even">
<td>1.4.0</td>
<td><p>Added the <strong><code>MongoDB\Driver\ReadConcern::AVAILABLE</code></strong> constant.</p></td>
</tr>
<tr class="odd">
<td>1.2.0</td>
<td><p>Added the <strong><code>MongoDB\Driver\ReadConcern::LINEARIZABLE</code></strong> constant.</p>
<p>Implements <span class="interfacename">MongoDB\BSON\Serializable</span>.</p></td>
</tr>
</tbody>
</table>

参见
----

-   <a href="https://docs.mongodb.com/manual/reference/read-concern/" class="link external">» Read Concern reference</a>

MongoDB\\Driver\\ReadConcern::bsonSerialize
===========================================

Returns an object for BSON serialization

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">MongoDB\\Driver\\ReadConcern::bsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an object for serializing the ReadConcern as BSON.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadConcern::bsonSerialize</span> with
empty read concern**

``` php
<?php

$rc = new MongoDB\Driver\ReadConcern;
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (0) {
    }

    { }

**示例 \#2 <span
class="function">MongoDB\\Driver\\ReadConcern::bsonSerialize</span> with
local read concern**

``` php
<?php

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->bsonSerialize());

echo "\n", MongoDB\BSON\toJSON(MongoDB\BSON\fromPHP($rc));

?>
```

以上例程的输出类似于：

    object(stdClass)#2 (1) {
      ["level"]=>
      string(5) "local"
    }

    { "level" : "local" }

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span>
-   <a href="https://docs.mongodb.com/manual/reference/read-concern/" class="link external">» Read Concern reference</a>

MongoDB\\Driver\\ReadConcern::\_\_construct
===========================================

Create a new ReadConcern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span
class="methodname">MongoDB\\Driver\\ReadConcern::\_\_construct</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$level`</span> \] )

Constructs a new <span
class="classname">MongoDB\\Driver\\ReadConcern</span>, which is an
immutable value object.

### 参数

`level`  
The
<a href="https://docs.mongodb.com/manual/reference/read-concern/#read-concern-levels" class="link external">» read concern level</a>.
You may use, but are not limited to, one of the
<a href="/set/mongodb.html#预定义常量" class="link">class constants</a>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadConcern::\_\_construct</span>
example**

``` php
<?php

/* Unspecified read isolation level (uses the server's default behavior) */
$rc = new MongoDB\Driver\ReadConcern();

/* Request read isolation from a single replica set node */
$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);

/* Request read isolation from a majority of the replica set nodes */
$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);

?>
```

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/read-concern/" class="link external">» Read Concern reference</a>

MongoDB\\Driver\\ReadConcern::getLevel
======================================

Returns the ReadConcern's "level" option

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string\|null</span> <span
class="methodname">MongoDB\\Driver\\ReadConcern::getLevel</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the ReadConcern's "level" option.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadConcern::getLevel</span> example**

``` php
<?php

$rc = new MongoDB\Driver\ReadConcern();
var_dump($rc->getLevel());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::LOCAL);
var_dump($rc->getLevel());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);
var_dump($rc->getLevel());

?>
```

以上例程会输出：

    NULL
    string(5) "local"
    string(8) "majority"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/read-concern/" class="link external">» Read Concern reference</a>

MongoDB\\Driver\\ReadConcern::isDefault
=======================================

Checks if this is the default read concern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\ReadConcern::isDefault</span> (
<span class="methodparam">void</span> )

Returns whether this is the default read concern (i.e. no options are
specified). This method is primarily intended to be used in conjunction
with <span
class="methodname">MongoDB\\Driver\\Manager::getReadConcern</span> to
determine whether the Manager has been constructed without any read
concern options.

The driver will not include a default read concern in its read
operations (e.g. <span
class="methodname">MongoDB\\Driver\\Manager::executeQuery</span>) in
order order to allow the server to apply its own default. Libraries that
access the Manager's read concern to include it in their own read
commands should use this method to ensure that default read concerns are
left unset.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this is the default read concern and **`FALSE`**
otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\ReadConcern::isDefault</span>
example**

``` php
<?php

$rc = new MongoDB\Driver\ReadConcern(null);
var_dump($rc->isDefault());

$rc = new MongoDB\Driver\ReadConcern(MongoDB\Driver\ReadConcern::MAJORITY);
var_dump($rc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/?readConcernLevel=majority');
$rc = $manager->getReadConcern();
var_dump($rc->isDefault());

$manager = new MongoDB\Driver\Manager('mongodb://127.0.0.1/');
$rc = $manager->getReadConcern();
var_dump($rc->isDefault());

?>
```

以上例程会输出：

    bool(true)
    bool(false)
    bool(false)
    bool(true)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Manager::getReadConcern</span>
-   <a href="https://docs.mongodb.com/manual/reference/read-concern/" class="link external">» Read Concern reference</a>

MongoDB\\Driver\\ReadConcern::serialize
=======================================

Serialize a ReadConcern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\ReadConcern::serialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\Driver\\ReadConcern</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\ReadConcern::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\Driver\\ReadConcern::unserialize
=========================================

Unserialize a ReadConcern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\ReadConcern::unserialize</span> (
<span class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span
class="classname">MongoDB\\Driver\\ReadConcern</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\Driver\\ReadConcern</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\ReadConcern::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

The <span class="classname">MongoDB\\Driver\\Cursor</span> class
encapsulates the results of a MongoDB command or query and may be
returned by <span
class="methodname">MongoDB\\Driver\\Manager::executeCommand</span> or
<span class="methodname">MongoDB\\Driver\\Manager::executeQuery</span>,
respectively.

类摘要
------

**MongoDB\\Driver\\Cursor**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Cursor** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\Driver\\CursorInterface</span>
</span> {

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\CursorId</span> <span
class="methodname">getId</span> ( <span class="methodparam">void</span>
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">getServer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isDead</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">setTypeMap</span> ( <span class="methodparam"><span
class="type">array</span> `$typemap`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span class="methodname">toArray</span>
( <span class="methodparam">void</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 1.6.0 | Implements <span class="interfacename">MongoDB\\Driver\\CursorInterface</span>, which extends <span class="interfacename">Traversable</span>. |

范例
----

**示例 \#1 Reading a result set**

<span class="methodname">MongoDB\\Driver\\Manager::executeCommand</span>
and <span
class="methodname">MongoDB\\Driver\\Manager::executeQuery</span> both
return their result(s) as a <span
class="classname">MongoDB\\Driver\\Cursor</span> object. This object can
be used to iterate over the result set of the command or query.

Because <span class="classname">MongoDB\\Driver\\Cursor</span>
implements the <span class="interfacename">Traversable</span> interface,
you can simply iterate over the result set with
<a href="/control-structures/foreach.html" class="link"><em>foreach</em></a>.

``` php
<?php

$manager = new MongoDB\Driver\Manager();

/* Insert some documents so that our query returns information */
$bulkWrite = new MongoDB\Driver\BulkWrite;
$bulkWrite->insert(['name' => 'Ceres', 'size' => 946, 'distance' => 2.766]);
$bulkWrite->insert(['name' => 'Vesta', 'size' => 525, 'distance' => 2.362]);
$manager->executeBulkWrite("test.asteroids", $bulkWrite);

/* Query for all the items in the collection */
$query = new MongoDB\Driver\Query( [] );

/* Query the "asteroids" collection of the "test" database */
$cursor = $manager->executeQuery("test.asteroids", $query);

/* $cursor now contains an object that wraps around the result set. Use
 * foreach() to iterate over all the result */
foreach($cursor as $document) {
    print_r($document);
}

?>
```

以上例程的输出类似于：

    stdClass Object
    (
        [_id] => MongoDB\BSON\ObjectId Object
            (
                [oid] => 5a4cff2f122d3321565d8cc2
            )

        [name] => Ceres
        [size] => 946
        [distance] => 2.766
    )
    stdClass Object
    (
        [_id] => MongoDB\BSON\ObjectId Object
            (
                [oid] => 5a4cff2f122d3321565d8cc3
            )

        [name] => Vesta
        [size] => 525
        [distance] => 2.362
    }

**示例 \#2 Reading a result set for a tailable cursor**

<a href="https://docs.mongodb.com/manual/core/tailable-cursors" class="link external">» Tailable cursors</a>
are a special type of MongoDB cursor that allows the client to read some
results and then wait until more documents become available. These
cursors are primarily used with
<a href="https://docs.mongodb.com/manual/core/capped-collections" class="link external">» Capped Collections</a>
and
<a href="https://docs.mongodb.com/manual/changeStreams" class="link external">» Change Streams</a>.

While normal cursors can be iterated once with *foreach*, that approach
will not work with tailable cursors. When *foreach* is used with a
tailable cursor, the loop will stop upon reaching the end of the initial
result set. Attempting to continue iteration on the cursor with a second
*foreach* would throw an exception, since PHP attempts to rewind the
cursor. Similar to result objects in other database drivers, cursors in
MongoDB only support forward iteration, which means they cannot be
rewound.

In order to continuously read from a tailable cursor, the Cursor object
must be wrapped with an <span class="classname">IteratorIterator</span>.
This allows the application to directly control the cursor's iteration,
avoid inadvertently rewinding the cursor, and decide when to wait for
new results or stop iteration entirely.

In order to demonstrate a tailable cursor in action, two scripts will be
used: a "producer" and a "consumer". The producer script will create a
new capped collection using the
<a href="https://docs.mongodb.com/manual/reference/command/create" class="link external">» create</a>
command and proceed to insert a new document into that collection each
second.

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$manager->executeCommand('test', new MongoDB\Driver\Command([
    'create' => 'asteroids',
    'capped' => true,
    'size' => 1048576,
]));

while (true) {
    $bulkWrite = new MongoDB\Driver\BulkWrite;
    $bulkWrite->insert(['createdAt' => new MongoDB\BSON\UTCDateTime]);
    $manager->executeBulkWrite('test.asteroids', $bulkWrite);

    sleep(1);
}

?>
```

With the producer script still running, a second consumer script may be
executed to read the inserted documents using a tailable cursor,
indicated by the *tailable* and *awaitData* options to <span
class="function">MongoDB\\Driver\\Query::\_\_construct</span>.

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$query = new MongoDB\Driver\Query([], [
    'tailable' => true,
    'awaitData' => true,
]);

$cursor = $manager->executeQuery('test.asteroids', $query);

$iterator = new IteratorIterator($cursor);

$iterator->rewind();

while (true) {
    if ($iterator->valid()) {
        $document = $iterator->current();
        printf("Consumed document created at: %s\n", $document->createdAt);
    }

    $iterator->next();
}

?>
```

The consumer script will start by quickly printing all available
documents in the capped collection (as if *foreach* had been used);
however, it will not terminate upon reaching the end of the initial
result set. Since the cursor is tailable, calling <span
class="function">IteratorIterator::next</span> will block and wait for
additional results. <span
class="function">IteratorIterator::valid</span> is also used to check if
there is actually data available to read at each step.

> **Note**: <span class="simpara"> This example uses the *awaitData*
> query option to instruct the server to block for a short period (e.g.
> one second) at the end of the result set before returning a response
> to the driver. This is used to prevent the driver from aggressively
> polling the server when there are no results available. The
> *maxAwaitTimeMS* option may be used in conjunction with *tailable* and
> *awaitData* to specify the amount of time that the server should block
> when it reaches the end of the result set. </span>

错误／异常
----------

When iterating over the cursor object, BSON data is converted into PHP
variables. This iteration can cause the following Exceptions:

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if a class in the type map cannot be instantiated or does not
    implement <span
    class="interfacename">MongoDB\\BSON\\Unserializable</span>.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the input did not contain exactly one BSON document. Possible
    reasons include, but are not limited to, invalid BSON, extra data
    (after reading one BSON document), or an unexpected
    <a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
    error.

MongoDB\\Driver\\Cursor::\_\_construct
======================================

Create a new Cursor (not used)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\Driver\\Cursor::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="classname">MongoDB\\Driver\\Cursor</span> objects are
returned as the result of an executed command or query and cannot be
constructed directly.

### 参数

此函数没有参数。

### 参见

-   <span
    class="function">MongoDB\\Driver\\Manager::executeCommand</span>
-   <span class="function">MongoDB\\Driver\\Manager::executeQuery</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeCommand</span>
-   <span class="function">MongoDB\\Driver\\Server::executeQuery</span>

MongoDB\\Driver\\Cursor::getId
==============================

Returns the ID for this cursor

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\CursorId</span> <span
class="methodname">MongoDB\\Driver\\Cursor::getId</span> ( <span
class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\CursorId</span>
associated with this cursor. A cursor ID uniquely identifies the cursor
on the server.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">MongoDB\\Driver\\CursorId</span> for
this cursor.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span class="function">MongoDB\\Driver\\Cursor::getId</span>
example**

``` php
<?php

/* In this example, we insert several documents into the collection and specify
 * a smaller batchSize to ensure that the first batch contains only a subset of
 * our results and the cursor remains open on the server. */
$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump($cursor->getId());

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\CursorId)#5 (1) {
      ["id"]=>
      int(94810124093)
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\CursorId</span>
-   <span
    class="function">MongoDB\\Driver\\CursorId::\_\_toString</span>

MongoDB\\Driver\\Cursor::getServer
==================================

Returns the server associated with this cursor

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">MongoDB\\Driver\\Cursor::getServer</span> ( <span
class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\Server</span>
associated with this cursor. This is the server that executed the <span
class="classname">MongoDB\\Driver\\Query</span> or <span
class="classname">MongoDB\\Driver\\Command</span>.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">MongoDB\\Driver\\Server</span>
associated with this cursor.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Cursor::getServer</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump($cursor->getServer());

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\Server)#5 (10) {
      ["host"]=>
      string(9) "localhost"
      ["port"]=>
      int(27017)
      ["type"]=>
      int(1)
      ["is_primary"]=>
      bool(false)
      ["is_secondary"]=>
      bool(false)
      ["is_arbiter"]=>
      bool(false)
      ["is_hidden"]=>
      bool(false)
      ["is_passive"]=>
      bool(false)
      ["last_is_master"]=>
      array(8) {
        ["ismaster"]=>
        bool(true)
        ["maxBsonObjectSize"]=>
        int(16777216)
        ["maxMessageSizeBytes"]=>
        int(48000000)
        ["maxWriteBatchSize"]=>
        int(1000)
        ["localTime"]=>
        object(MongoDB\BSON\UTCDateTime)#6 (1) {
          ["milliseconds"]=>
          int(1446505367907)
        }
        ["maxWireVersion"]=>
        int(3)
        ["minWireVersion"]=>
        int(0)
        ["ok"]=>
        float(1)
      }
      ["round_trip_time"]=>
      int(584)
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\Server</span>

MongoDB\\Driver\\Cursor::isDead
===============================

Checks if the cursor is exhausted or may have additional results

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Cursor::isDead</span> ( <span
class="methodparam">void</span> )

Checks whether there are definitely no additional results available on
the cursor. This method is similar to the
<a href="https://docs.mongodb.com/manual/reference/method/cursor.isExhausted/" class="link external">» cursor.isExhausted()</a>
method in the MongoDB shell and is primarily useful when iterating
<a href="https://docs.mongodb.com/manual/core/tailable-cursors/" class="link external">» tailable cursors</a>.

A cursor has no additional results and is considered "dead" when one of
the following is true:

-   The current batch has been fully iterated *and* the cursor ID is
    zero (i.e. a
    <a href="https://docs.mongodb.com/manual/reference/command/getMore/" class="link external">» getMore</a>
    cannot be issued).
-   An error was encountered while iterating the cursor.
-   The cursor reached its configured limit.

By design, it is not possible to always determine whether a cursor has
additional results. The cases where a cursor *may* have more data
available is as follows:

-   There are additional documents in the current batch, which are
    buffered on the client side. Iterating will fetch a document from
    the local buffer.
-   There are no additional documents in the current batch (i.e. local
    buffer), but the cursor ID is non-zero. Iterating will request more
    documents from the server via a
    <a href="https://docs.mongodb.com/manual/reference/command/getMore/" class="link external">» getMore</a>
    operation, which may or may not return additional results and/or
    indicate that the cursor has been closed on the server by returning
    zero for its ID.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if there are definitely no additional results
available on the cursor, and **`FALSE`** otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span class="function">MongoDB\\Driver\\Cursor::isDead</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);

$iterator = new IteratorIterator($cursor);

$iterator->rewind();
var_dump($cursor->isDead());

$iterator->next();
var_dump($cursor->isDead());

$iterator->next();
var_dump($cursor->isDead());

$iterator->next();
var_dump($cursor->isDead());

?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(false)
    bool(true)

### 参见

-   <a href="https://docs.mongodb.com/manual/core/tailable-cursors/" class="link external">» Tailable Cursors</a>
    in the MongoDB manual
-   <a href="https://docs.mongodb.com/manual/reference/method/cursor.isExhausted/" class="link external">» cursor.isExhausted()</a>
    in the MongoDB manual

MongoDB\\Driver\\Cursor::setTypeMap
===================================

Sets a type map to use for BSON unserialization

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\Cursor::setTypeMap</span> ( <span
class="methodparam"><span class="type">array</span> `$typemap`</span> )

Sets the
<a href="/set/mongodb.html#TypeMaps" class="link">type map configuration</a>
to use when unserializing the BSON results into PHP values.

### 参数

`typeMap` (<span class="type">array</span>)  
<a href="/set/mongodb.html#TypeMaps" class="link">Type map configuration</a>.

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

When iterating over the cursor, the following exceptions can also be
thrown due to an incorrect type map configuration:

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if a class in the type map cannot be instantiated or does not
    implement <span
    class="interfacename">MongoDB\\BSON\\Unserializable</span>.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Cursor::setTypeMap</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$id = $bulk->insert(['x' => 1]);
$manager->executeBulkWrite('db.collection', $bulk);

$query = new MongoDB\Driver\Query(['_id' => $id]);
$cursor = $manager->executeQuery('db.collection', $query);
$cursor->setTypeMap(['root' => 'array']);

foreach ($cursor as $document) {
    var_dump($document);
}

?>
```

以上例程的输出类似于：

    array(2) {
      ["_id"]=>
      object(MongoDB\BSON\ObjectId)#6 (1) {
        ["oid"]=>
        string(24) "56424fb76118fd3267180741"
      }
      ["x"]=>
      int(1)
    }

### 参见

-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

MongoDB\\Driver\\Cursor::toArray
================================

Returns an array containing all results for this cursor

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\Cursor::toArray</span> ( <span
class="methodparam">void</span> )

Iterates the cursor and returns its results in an array. <span
class="function">MongoDB\\Driver\\Cursor::setTypeMap</span> may be used
to control how documents are unserialized into PHP values.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">array</span> containing all results for
this cursor.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Cursor::toArray</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$query = new MongoDB\Driver\Query([]);
$cursor = $manager->executeQuery('db.collection', $query);

var_dump($cursor->toArray());

?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      object(stdClass)#6 (2) {
        ["_id"]=>
        object(MongoDB\BSON\ObjectId)#5 (1) {
          ["oid"]=>
          string(24) "564259a96118fd40b41bcf61"
        }
        ["x"]=>
        int(1)
      }
      [1]=>
      object(stdClass)#8 (2) {
        ["_id"]=>
        object(MongoDB\BSON\ObjectId)#7 (1) {
          ["oid"]=>
          string(24) "564259a96118fd40b41bcf62"
        }
        ["x"]=>
        int(2)
      }
      [2]=>
      object(stdClass)#10 (2) {
        ["_id"]=>
        object(MongoDB\BSON\ObjectId)#9 (1) {
          ["oid"]=>
          string(24) "564259a96118fd40b41bcf63"
        }
        ["x"]=>
        int(3)
      }
    }

### 参见

-   <span class="function">MongoDB\\Driver\\Cursor::setTypeMap</span>

简介
----

The <span class="classname">MongoDB\\Driver\\CursorID</span> class is a
value object that represents a cursor ID. Instances of this class are
returned by <span
class="function">MongoDB\\Driver\\Cursor::getId</span>.

类摘要
------

**MongoDB\\Driver\\CursorId**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\CursorId** </span> <span
class="oointerface">implements <span
class="interfacename">Serializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                        |
|-------|-------------------------------------------------------------|
| 1.7.0 | Implements <span class="interfacename">Serializable</span>. |

MongoDB\\Driver\\CursorId::\_\_construct
========================================

Create a new CursorId (not used)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\Driver\\CursorId::\_\_construct</span> (
<span class="methodparam">void</span> )

<span class="classname">MongoDB\\Driver\\CursorId</span> objects are
returned from <span
class="function">MongoDB\\Driver\\Cursor::getId</span> and cannot be
constructed directly.

### 参数

此函数没有参数。

### 参见

-   <span class="function">MongoDB\\Driver\\Cursor::getId</span>

MongoDB\\Driver\\CursorId::serialize
====================================

Serialize a CursorId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\CursorId::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\Driver\\CursorId</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\CursorId::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\Driver\\CursorId::\_\_toString
=======================================

String representation of the cursor ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\CursorId::\_\_toString</span> (
<span class="methodparam">void</span> )

Returns the <span class="type">string</span> representation of the
cursor ID.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="type">string</span> representation of the
cursor ID.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\CursorId::\_\_toString</span>
example**

``` php
<?php

/* In this example, we insert several documents into the collection and specify
 * a smaller batchSize to ensure that the first batch contains only a subset of
 * our results and the cursor remains open on the server. */
$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([], ['batchSize' => 2]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);
var_dump((string) $cursor->getId());

?>
```

以上例程的输出类似于：

    string(11) "98061641158"

### 参见

-   <span class="function">MongoDB\\Driver\\Cursor::getId</span>

MongoDB\\Driver\\CursorId::unserialize
======================================

Unserialize a CursorId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\CursorId::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\Driver\\CursorId</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\Driver\\CursorId</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\Driver\\CursorId::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

类摘要
------

**MongoDB\\Driver\\Server**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Server** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_UNKNOWN` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_STANDALONE` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_MONGOS` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_POSSIBLE_PRIMARY` <span
class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_RS_PRIMARY` <span class="initializer"> =
4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_RS_SECONDARY` <span class="initializer"> =
5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_RS_ARBITER` <span class="initializer"> =
6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_RS_OTHER` <span class="initializer"> =
7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\Driver\Server::TYPE_RS_GHOST` <span class="initializer"> =
8</span> ;

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">executeBulkWrite</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\BulkWrite</span> `$bulk`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeQuery</span> ( <span class="methodparam"><span
class="type">string</span> `$namespace`</span> , <span
class="methodparam"><span class="type">MongoDB\\Driver\\Query</span>
`$query`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeReadCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeReadWriteCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">executeWriteCommand</span> ( <span
class="methodparam"><span class="type">string</span> `$db`</span> ,
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span class="methodname">getHost</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span class="methodname">getInfo</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getLatency</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getPort</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span class="methodname">getTags</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getType</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isArbiter</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isHidden</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isPassive</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span class="methodname">isPrimary</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">isSecondary</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`MongoDB\Driver\Server::TYPE_UNKNOWN`**  
Unknown server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

**`MongoDB\Driver\Server::TYPE_STANDALONE`**  
Standalone server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

**`MongoDB\Driver\Server::TYPE_MONGOS`**  
Mongos server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

**`MongoDB\Driver\Server::TYPE_POSSIBLE_PRIMARY`**  
Replica set possible primary server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

A server may be identified as a possible primary if it has not yet been
checked but another memory of the replica set thinks it is the primary.

**`MongoDB\Driver\Server::TYPE_RS_PRIMARY`**  
Replica set primary server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

**`MongoDB\Driver\Server::TYPE_RS_SECONDARY`**  
Replica set secondary server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

**`MongoDB\Driver\Server::TYPE_RS_ARBITER`**  
Replica set arbiter server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

**`MongoDB\Driver\Server::TYPE_RS_OTHER`**  
Replica set other server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

Such servers may be hidden, starting up, or recovering. They cannot be
queried, but their hosts lists are useful for discovering the current
replica set configuration.

**`MongoDB\Driver\Server::TYPE_RS_GHOST`**  
Replica set ghost server type, returned by <span
class="methodname">MongoDB\\Driver\\Server::getType</span>.

Servers may be identified as such in at least three situations: briefly
during server startup; in an uninitialized replica set; or when the
server is shunned (i.e. removed from the replica set config). They
cannot be queried, nor can their host list be used to discover the
current replica set configuration; however, the client may monitor this
server in hope that it transitions to a more useful state.

MongoDB\\Driver\\Server::\_\_construct
======================================

Create a new Server (not used)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\Driver\\Server::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="classname">MongoDB\\Driver\\Server</span> objects are
created internally by <span
class="classname">MongoDB\\Driver\\Manager</span> when a database
connection is established and may be returned by <span
class="function">MongoDB\\Driver\\Manager::getServers</span> and <span
class="function">MongoDB\\Driver\\Manager::selectServer</span>.

### 参数

此函数没有参数。

### 参见

-   <span class="function">MongoDB\\Driver\\Manager::getServers</span>
-   <span class="function">MongoDB\\Driver\\Manager::selectServer</span>

MongoDB\\Driver\\Server::executeBulkWrite
=========================================

Execute one or more write operations on this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">MongoDB\\Driver\\Server::executeBulkWrite</span> (
<span class="methodparam"><span class="type">string</span>
`$namespace`</span> , <span class="methodparam"><span
class="type">MongoDB\\Driver\\BulkWrite</span> `$bulk`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes one or more write operations on this server.

A <span class="classname">MongoDB\\Driver\\BulkWrite</span> can be
constructed with one or more write operations of varying types (e.g.
updates, deletes, and inserts). The driver will attempt to send
operations of the same type to the server in as few requests as possible
to optimize round trips.

### 参数

`namespace` (<span class="type">string</span>)  
A fully qualified namespace (e.g. *"databaseName.collectionName"*).

`bulk` (<span class="classname">MongoDB\\Driver\\BulkWrite</span>)  
The write(s) to execute.

`options`  
| Option       | Type                                                         | Description                                |
|--------------|--------------------------------------------------------------|--------------------------------------------|
| session      | <span class="classname">MongoDB\\Driver\\Session</span>      | A session to associate with the operation. |
| writeConcern | <span class="classname">MongoDB\\Driver\\WriteConcern</span> | A write concern to apply to the operation. |

### 返回值

Returns <span class="classname">MongoDB\\Driver\\WriteResult</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `bulk` does not contain any write operations.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `bulk` has already been executed. <span
    class="classname">MongoDB\\Driver\\BulkWrite</span> objects may not
    be executed multiple times.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\BulkWriteException</span>
    on any write failure (e.g. write error, failure to apply a write
    concern)
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                       |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern.                                                                  |
| 1.4.0 | The third parameter is now an `options` array. For backwards compatibility, this paramater will still accept a <span class="classname">MongoDB\\Driver\\WriteConcern</span> object.                                                                        |
| 1.3.0 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> is now thrown if `bulk` does not contain any write operations. Previously, a <span class="classname">MongoDB\\Driver\\Exception\\BulkWriteException</span> was thrown. |

### 注释

> **Note**: <span class="simpara"> It is the caller's responsibility to
> ensure that the server is capable of executing the write operation.
> For example, executing a write operation on a secondary (excluding its
> "local" database) will fail. </span>

### 参见

-   <span class="classname">MongoDB\\Driver\\BulkWrite</span>
-   <span class="classname">MongoDB\\Driver\\WriteResult</span>
-   <span class="classname">MongoDB\\Driver\\WriteConcern</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeBulkWrite</span>

MongoDB\\Driver\\Server::executeCommand
=======================================

Execute a database command on this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Server::executeCommand</span> (
<span class="methodparam"><span class="type">string</span> `$db`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the command on this server.

This method applies no special logic to the command. Although this
method accepts *"readConcern"* and *"writeConcern"* options, which will
be incorporated into the command document, those options will not
default to corresponding values from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a> nor
will the MongoDB server version be taken into account. Users are
therefore encouraged to use specific read and/or write command methods
if possible.

> **Note**: <span class="simpara"> The *"readPreference"* option does
> not control the server to which the driver issues the operation; it
> will always be executed on this server object. Instead, it may be used
> when issuing the operation to a secondary (from a replica set
> connection, not standalone) or mongos node to ensure that the driver
> sets the wire protocol accordingly or adds the read preference to the
> operation, respectively. </span>

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>readPreference</td>
<td><span class="classname">MongoDB\Driver\ReadPreference</span></td>
<td><p>A read preference to use for selecting a server for the operation.</p></td>
</tr>
<tr class="odd">
<td>session</td>
<td><span class="classname">MongoDB\Driver\Session</span></td>
<td><p>A session to associate with the operation.</p></td>
</tr>
<tr class="even">
<td>writeConcern</td>
<td><span class="classname">MongoDB\Driver\WriteConcern</span></td>
<td><p>A write concern to apply to the operation.</p></td>
</tr>
</tbody>
</table>

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command, issuing a write command to a
    secondary).

### 更新日志

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern. |
| 1.4.0 | The third parameter is now an `options` array. For backwards compatibility, this paramater will still accept a <span class="classname">MongoDB\\Driver\\ReadPreference</span> object.     |

### 注释

> **Note**: <span class="simpara"> It is the caller's responsibility to
> ensure that the server is capable of executing the write operation.
> For example, executing a write operation on a secondary (excluding its
> "local" database) will fail. </span>

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeCommand</span>

MongoDB\\Driver\\Server::executeQuery
=====================================

Execute a database query on this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Server::executeQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$namespace`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Query</span> `$query`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the query on this server.

> **Note**: <span class="simpara"> The *"readPreference"* option does
> not control the server to which the driver issues the operation; it
> will always be executed on this server object. Instead, it may be used
> when issuing the operation to a secondary (from a replica set
> connection, not standalone) or mongos node to ensure that the driver
> sets the wire protocol accordingly or adds the read preference to the
> operation, respectively. </span>

### 参数

`namespace` (<span class="type">string</span>)  
A fully qualified namespace (e.g. *"databaseName.collectionName"*).

`query` (<span class="classname">MongoDB\\Driver\\Query</span>)  
The query to execute.

`options`  
| Option         | Type                                                           | Description                                                        |
|----------------|----------------------------------------------------------------|--------------------------------------------------------------------|
| readPreference | <span class="classname">MongoDB\\Driver\\ReadPreference</span> | A read preference to use for selecting a server for the operation. |
| session        | <span class="classname">MongoDB\\Driver\\Session</span>        | A session to associate with the operation.                         |

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid query operators).

### 更新日志

| 版本  | 说明                                                                                                                                                                                  |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.0 | The third parameter is now an `options` array. For backwards compatibility, this paramater will still accept a <span class="classname">MongoDB\\Driver\\ReadPreference</span> object. |

### 参见

-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span class="classname">MongoDB\\Driver\\Query</span>
-   <span class="classname">MongoDB\\Driver\\ReadPreference</span>
-   <span class="function">MongoDB\\Driver\\Manager::executeQuery</span>

MongoDB\\Driver\\Server::executeReadCommand
===========================================

Execute a database command that reads on this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Server::executeReadCommand</span> (
<span class="methodparam"><span class="type">string</span> `$db`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the command on this server.

This method will apply logic that is specific to commands that read
(e.g.
<a href="https://docs.mongodb.com/manual/reference/command/count/" class="link external">» count</a>)
and take the MongoDB server version into account. The *"readConcern"*
option will default to the corresponding value from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>.

> **Note**: <span class="simpara"> The *"readPreference"* option does
> not control the server to which the driver issues the operation; it
> will always be executed on this server object. Instead, it may be used
> when issuing the operation to a secondary (from a replica set
> connection, not standalone) or mongos node to ensure that the driver
> sets the wire protocol accordingly or adds the read preference to the
> operation, respectively. </span>

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>readPreference</td>
<td><span class="classname">MongoDB\Driver\ReadPreference</span></td>
<td><p>A read preference to use for selecting a server for the operation.</p></td>
</tr>
<tr class="odd">
<td>session</td>
<td><span class="classname">MongoDB\Driver\Session</span></td>
<td><p>A session to associate with the operation.</p></td>
</tr>
</tbody>
</table>

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command).

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadCommand</span>

MongoDB\\Driver\\Server::executeReadWriteCommand
================================================

Execute a database command that reads and writes on this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Server::executeReadWriteCommand</span>
( <span class="methodparam"><span class="type">string</span>
`$db`</span> , <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the command on this server.

This method will apply logic that is specific to commands that read and
write (e.g.
<a href="https://docs.mongodb.com/manual/reference/command/aggregate/" class="link external">» aggregate</a>)
and take the MongoDB server version into account. The *"readConcern"*
and *"writeConcern"* options will default to the corresponding values
from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>.

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
<table>
<caption><strong>options</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>readConcern</td>
<td><span class="classname">MongoDB\Driver\ReadConcern</span></td>
<td><p>A read concern to apply to the operation.</p>
<p>This option is available in MongoDB 3.2+ and will result in an exception at execution time if specified for an older server version.</p></td>
</tr>
<tr class="even">
<td>session</td>
<td><span class="classname">MongoDB\Driver\Session</span></td>
<td><p>A session to associate with the operation.</p></td>
</tr>
<tr class="odd">
<td>writeConcern</td>
<td><span class="classname">MongoDB\Driver\WriteConcern</span></td>
<td><p>A write concern to apply to the operation.</p></td>
</tr>
</tbody>
</table>

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command).

### 更新日志

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern. |

### 注释

> **Note**: <span class="simpara"> It is the caller's responsibility to
> ensure that the server is capable of executing the write operation.
> For example, executing a write operation on a secondary (excluding its
> "local" database) will fail. </span>

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeReadWriteCommand</span>

MongoDB\\Driver\\Server::executeWriteCommand
============================================

Execute a database command that writes on this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Cursor</span> <span
class="methodname">MongoDB\\Driver\\Server::executeWriteCommand</span> (
<span class="methodparam"><span class="type">string</span> `$db`</span>
, <span class="methodparam"><span
class="type">MongoDB\\Driver\\Command</span> `$command`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = array()</span></span> \] )

Executes the command on this server.

This method will apply logic that is specific to commands that write
(e.g.
<a href="https://docs.mongodb.com/manual/reference/command/drop/" class="link external">» drop</a>)
and take the MongoDB server version into account. The *"writeConcern"*
option will default to the corresponding value from the
<a href="/set/mongodb.html#" class="link">MongoDB Connection URI</a>.

> **Note**: <span class="simpara"> This method is not intended to be
> used to execute
> <a href="https://docs.mongodb.com/manual/reference/command/insert/" class="link external">» insert</a>,
> <a href="https://docs.mongodb.com/manual/reference/command/update/" class="link external">» update</a>,
> or
> <a href="https://docs.mongodb.com/manual/reference/command/delete/" class="link external">» delete</a>
> commands. Users are encouraged to use <span
> class="function">MongoDB\\Driver\\Server::executeBulkWrite</span> for
> those commands. </span>

### 参数

`db` (<span class="type">string</span>)  
The name of the database on which to execute the command.

`command` (<span class="classname">MongoDB\\Driver\\Command</span>)  
The command to execute.

`options`  
| Option       | Type                                                         | Description                                |
|--------------|--------------------------------------------------------------|--------------------------------------------|
| session      | <span class="classname">MongoDB\\Driver\\Session</span>      | A session to associate with the operation. |
| writeConcern | <span class="classname">MongoDB\\Driver\\WriteConcern</span> | A write concern to apply to the operation. |

**Warning**
If you are using a *"session"* which has a transaction in progress, you
cannot specify a *"readConcern"* or *"writeConcern"* option. This will
result in an <span
class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
being thrown. Instead, you should set these two options when you create
the transaction with <span
class="methodname">MongoDB\\Driver\\Session::startTransaction</span>.

### 返回值

Returns <span class="classname">MongoDB\\Driver\\Cursor</span> on
success.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used with an associated transaction in
    combination with a *"readConcern"* or *"writeConcern"* option.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the *"session"* option is used in combination with an
    unacknowledged write concern.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\ConnectionException</span>
    if connection to the server fails (for reasons other than
    authentication).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\AuthenticationException</span>
    if authentication is needed and fails.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>
    on other errors (e.g. invalid command).

### 更新日志

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.4 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> will be thrown if the *"session"* option is used in combination with an unacknowledged write concern. |

### 注释

> **Note**: <span class="simpara"> It is the caller's responsibility to
> ensure that the server is capable of executing the write operation.
> For example, executing a write operation on a secondary (excluding its
> "local" database) will fail. </span>

### 参见

-   <span class="classname">MongoDB\\Driver\\Command</span>
-   <span class="classname">MongoDB\\Driver\\Cursor</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Server::executeReadWriteCommand</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeWriteCommand</span>

MongoDB\\Driver\\Server::getHost
================================

Returns the hostname of this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Server::getHost</span> ( <span
class="methodparam">void</span> )

Returns the hostname of this server.

### 参数

此函数没有参数。

### 返回值

Returns the hostname of this server.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Server::getHost</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getHost());

?>
```

以上例程会输出：

    string(9) "localhost"

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::getInfo
================================

Returns an array of information about this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\Server::getInfo</span> ( <span
class="methodparam">void</span> )

Returns an array of information about this server.

### 参数

此函数没有参数。

### 返回值

Returns an array of information about this server.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Server::getInfo</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getInfo());

?>
```

以上例程的输出类似于：

    array(8) {
      ["ismaster"]=>
      bool(true)
      ["maxBsonObjectSize"]=>
      int(16777216)
      ["maxMessageSizeBytes"]=>
      int(48000000)
      ["maxWriteBatchSize"]=>
      int(1000)
      ["localTime"]=>
      object(MongoDB\BSON\UTCDateTime)#4 (1) {
        ["milliseconds"]=>
        int(1447276242774)
      }
      ["maxWireVersion"]=>
      int(3)
      ["minWireVersion"]=>
      int(0)
      ["ok"]=>
      float(1)
    }

MongoDB\\Driver\\Server::getLatency
===================================

Returns the latency of this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Server::getLatency</span> ( <span
class="methodparam">void</span> )

Returns the latency of this server (i.e. the client's measured
<a href="https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst#round-trip-time" class="link external">» round trip time</a>
of an *ismaster* command).

### 参数

此函数没有参数。

### 返回值

Returns the latency of this server.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Server::getLatency</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getLatency());

?>
```

以上例程的输出类似于：

    int(592)

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>
-   <a href="https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst" class="link external">» Server Discovery and Monitoring Specification</a>

MongoDB\\Driver\\Server::getPort
================================

Returns the port on which this server is listening

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\Server::getPort</span> ( <span
class="methodparam">void</span> )

Returns the port on which this server is listening.

### 参数

此函数没有参数。

### 返回值

Returns the port on which this server is listening.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Server::getPort</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017/");

$rp = new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY);
$server = $manager->selectServer($rp);

var_dump($server->getPort());

?>
```

以上例程会输出：

    int(27017)

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::getTags
================================

Returns an array of tags describing this server in a replica set

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\Server::getTags</span> ( <span
class="methodparam">void</span> )

Returns an <span class="type">array</span> of
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-tag" class="link external">» tags</a>
used to describe this server in a replica set. The array will contain
zero or more <span class="type">string</span> key and value pairs.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">array</span> of tags used to describe this
server in a replica set.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::getType
================================

Returns an integer denoting the type of this server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\Server::getType</span> ( <span
class="methodparam">void</span> )

Returns an <span class="type">integer</span> denoting the type of this
server. The value will correlate with a <span
class="classname">MongoDB\\Driver\\Server</span> constant.

### 参数

此函数没有参数。

### 返回值

Returns an <span class="type">integer</span> denoting the type of this
server.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::isArbiter
==================================

Checks if this server is an arbiter member of a replica set

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Server::isArbiter</span> ( <span
class="methodparam">void</span> )

Returns whether this server is an
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-arbiter" class="link external">» arbiter member</a>
of a replica set.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this server is an arbiter member of a replica set,
and **`FALSE`** otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::isHidden
=================================

Checks if this server is a hidden member of a replica set

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Server::isHidden</span> ( <span
class="methodparam">void</span> )

Returns whether this server is a
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-hidden-member" class="link external">» hidden member</a>
of a replica set.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this server is a hidden member of a replica set,
and **`FALSE`** otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::isPassive
==================================

Checks if this server is a passive member of a replica set

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Server::isPassive</span> ( <span
class="methodparam">void</span> )

Returns whether this server is a
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-passive-member" class="link external">» passive member</a>
of a replica set (i.e. its priority is *0*).

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this server is a passive member of a replica set,
and **`FALSE`** otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::isPrimary
==================================

Checks if this server is a primary member of a replica set

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Server::isPrimary</span> ( <span
class="methodparam">void</span> )

Returns whether this server is a
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-primary" class="link external">» primary member</a>
of a replica set.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this server is a primary member of a replica set,
and **`FALSE`** otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

MongoDB\\Driver\\Server::isSecondary
====================================

Checks if this server is a secondary member of a replica set

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Server::isSecondary</span> ( <span
class="methodparam">void</span> )

Returns whether this server is a
<a href="https://docs.mongodb.com/manual/reference/glossary/#term-secondary" class="link external">» secondary member</a>
of a replica set.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if this server is a secondary member of a replica
set, and **`FALSE`** otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="function">MongoDB\\Driver\\Server::getInfo</span>

简介
----

The <span class="classname">MongoDB\\Driver\\WriteConcernError</span>
class encapsulates information about a write concern error and may be
returned by <span
class="methodname">MongoDB\\Driver\\WriteResult::getWriteConcernError</span>.

类摘要
------

**MongoDB\\Driver\\WriteConcernError**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\WriteConcernError** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getCode</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">getInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getMessage</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\Driver\\WriteConcernError::getCode
===========================================

Returns the WriteConcernError's error code

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\WriteConcernError::getCode</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteConcernError's error code.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcernError::getCode</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getCode());
}

?>
```

以上例程的输出类似于：

    int(64)

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcernError::getInfo
===========================================

Returns metadata document for the WriteConcernError

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteConcernError::getInfo</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the metadata document for the WriteConcernError, or **`NULL`**
if no metadata is available.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcernError::getInfo</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getInfo());
}

?>
```

以上例程的输出类似于：

    object(stdClass)#1 (1) {
      ["wtimeout"]=>
      bool(true)
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteConcernError::getMessage
==============================================

Returns the WriteConcernError's error message

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\WriteConcernError::getMessage</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteConcernError's error message.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteConcernError::getMessage</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError()->getMessage());
}

?>
```

以上例程的输出类似于：

    string(33) "waiting for replication timed out"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

简介
----

The <span class="classname">MongoDB\\Driver\\WriteError</span> class
encapsulates information about a write error and may be returned as an
array element from <span
class="methodname">MongoDB\\Driver\\WriteResult::getWriteErrors</span>.

类摘要
------

**MongoDB\\Driver\\WriteError**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\WriteError** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getCode</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getIndex</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">getInfo</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getMessage</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\Driver\\WriteError::getCode
====================================

Returns the WriteError's error code

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\WriteError::getCode</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteError's error code.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteError::getCode</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getCode());
}

?>
```

以上例程的输出类似于：

    int(11000)

MongoDB\\Driver\\WriteError::getIndex
=====================================

Returns the index of the write operation corresponding to this
WriteError

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\WriteError::getIndex</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the index of the write operation (from <span
class="classname">MongoDB\\Driver\\BulkWrite</span>) corresponding to
this WriteError.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteError::getIndex</span> example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getIndex());
}

?>
```

以上例程的输出类似于：

    int(1)

### 参见

-   <span class="classname">MongoDB\\Driver\\BulkWrite</span>

MongoDB\\Driver\\WriteError::getInfo
====================================

Returns metadata document for the WriteError

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteError::getInfo</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the metadata document for the WriteError, or **`NULL`** if no
metadata is available.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

MongoDB\\Driver\\WriteError::getMessage
=======================================

Returns the WriteError's error message

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\WriteError::getMessage</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the WriteError's error message.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteError::getMessage</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors()[0]->getMessage());
}

?>
```

以上例程的输出类似于：

    string(70) "E11000 duplicate key error index: db.collection.$_id_ dup key: { : 1 }"

简介
----

The <span class="classname">MongoDB\\Driver\\WriteResult</span> class
encapsulates information about an executed <span
class="classname">MongoDB\\Driver\\BulkWrite</span> and may be returned
by <span
class="methodname">MongoDB\\Driver\\Manager::executeBulkWrite</span>.

类摘要
------

**MongoDB\\Driver\\WriteResult**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\WriteResult** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">getDeletedCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">getInsertedCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">getMatchedCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">getModifiedCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">getServer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">getUpsertedCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">getUpsertedIds</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteConcernError\|null</span> <span
class="methodname">getWriteConcernError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">getWriteErrors</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">isAcknowledged</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\Driver\\WriteResult::getDeletedCount
=============================================

Returns the number of documents deleted

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getDeletedCount</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the number of documents deleted, or **`NULL`** if the write was
not acknowledged.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getDeletedCount</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getDeletedCount());

?>
```

以上例程会输出：

    int(1)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span>

MongoDB\\Driver\\WriteResult::getInsertedCount
==============================================

Returns the number of documents inserted (excluding upserts)

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getInsertedCount</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the number of documents inserted (excluding upserts), or
**`NULL`** if the write was not acknowledged.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getInsertedCount</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getInsertedCount());

?>
```

以上例程会输出：

    int(1)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span>

MongoDB\\Driver\\WriteResult::getMatchedCount
=============================================

Returns the number of documents selected for update

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getMatchedCount</span>
( <span class="methodparam">void</span> )

If the update operation results in no change to the document (e.g.
setting the value of a field to its current value), the matched count
may be greater than the value returned by <span
class="methodname">MongoDB\\Driver\\WriteResult::getModifiedCount</span>.

### 参数

此函数没有参数。

### 返回值

Returns the number of documents selected for update, or **`NULL`** if
the write was not acknowledged.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getMatchedCount</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getMatchedCount());

?>
```

以上例程会输出：

    int(1)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::getModifiedCount</span>
-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span>

MongoDB\\Driver\\WriteResult::getModifiedCount
==============================================

Returns the number of existing documents updated

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getModifiedCount</span>
( <span class="methodparam">void</span> )

If the update operation results in no change to the document (e.g.
setting the value of a field to its current value), the modified count
may be less than the value returned by <span
class="methodname">MongoDB\\Driver\\WriteResult::getMatchedCount</span>.

### 参数

此函数没有参数。

### 返回值

Returns the number of existing documents updated, or **`NULL`** if the
write was not acknowledged.

The modified count is not available on versions of MongoDB before 2.6,
which used the legacy wire protocol version (i.e. OP\_UPDATE). If this
is the case, the modified count will also be **`NULL`**.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getModifiedCount</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getModifiedCount());

?>
```

以上例程会输出：

    int(1)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::getMatchedCount</span>
-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span>

MongoDB\\Driver\\WriteResult::getServer
=======================================

Returns the server associated with this write result

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getServer</span> (
<span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\Server</span>
associated with this write result. This is the server that executed the
<span class="classname">MongoDB\\Driver\\BulkWrite</span>.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">MongoDB\\Driver\\Server</span>
associated with this write result.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getServer</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;
$server = $manager->selectServer(new MongoDB\Driver\ReadPreference(MongoDB\Driver\ReadPreference::RP_PRIMARY));

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $server->executeBulkWrite('db.collection', $bulk);

var_dump($result->getServer() == $server);

?>
```

以上例程会输出：

    bool(true)

### 参见

-   <span class="classname">MongoDB\\Driver\\Server</span>

MongoDB\\Driver\\WriteResult::getUpsertedCount
==============================================

Returns the number of documents inserted by an upsert

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">integer\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getUpsertedCount</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the number of documents inserted by an upsert.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getUpsertedCount</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getUpsertedCount());

?>
```

以上例程会输出：

    int(2)

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::getUpsertedIds</span>
-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span>

MongoDB\\Driver\\WriteResult::getUpsertedIds
============================================

Returns an array of identifiers for upserted documents

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getUpsertedIds</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an array of identifiers (i.e. *"\_id"* field values) for
upserted documents. The array keys will correspond to the index of the
write operation (from <span
class="classname">MongoDB\\Driver\\BulkWrite</span>) responsible for the
upsert.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getUpsertedIds</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->update(['x' => 1], ['$set' => ['y' => 3]]);
$bulk->update(['x' => 2], ['$set' => ['y' => 1]], ['upsert' => true]);
$bulk->update(['x' => 3], ['$set' => ['y' => 2]], ['upsert' => true]);
$bulk->delete(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->getUpsertedIds());

?>
```

以上例程的输出类似于：

    array(2) {
      [2]=>
      object(MongoDB\BSON\ObjectId)#4 (1) {
        ["oid"]=>
        string(24) "580e62a224f2302f191b880b"
      }
      [3]=>
      object(MongoDB\BSON\ObjectId)#5 (1) {
        ["oid"]=>
        string(24) "580e62a224f2302f191b880c"
      }
    }

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::getUpsertedCount</span>
-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span>

MongoDB\\Driver\\WriteResult::getWriteConcernError
==================================================

Returns any write concern error that occurred

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteConcernError\|null</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getWriteConcernError</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns a <span
class="classname">MongoDB\\Driver\\WriteConcernError</span> if a write
concern error was encountered during the write operation, and **`NULL`**
otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getWriteConcernError</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://rs1.example.com,rs2.example.com/?replicaSet=myReplicaSet");

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$writeConcern = new MongoDB\Driver\WriteConcern(2, 1);

try {
    $manager->executeBulkWrite('db.collection', $bulk, $writeConcern);
} catch(MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteConcernError());
}

?>
```

以上例程的输出类似于：

    object(MongoDB\Driver\WriteConcernError)#6 (3) {
      ["message"]=>
      string(33) "waiting for replication timed out"
      ["code"]=>
      int(64)
      ["info"]=>
      object(stdClass)#7 (1) {
        ["wtimeout"]=>
        bool(true)
      }
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\WriteConcern</span>
-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

MongoDB\\Driver\\WriteResult::getWriteErrors
============================================

Returns any write errors that occurred

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::getWriteErrors</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an array of <span
class="classname">MongoDB\\Driver\\WriteError</span> objects for any
write errors encountered during the write operation. The array will be
empty if no write errors occurred.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::getWriteErrors</span>
with a single error**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

/* By default, bulk write operations are executed serially in order and
 * execution will stop after the first error.
 */
$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 3]);
$bulk->insert(['_id' => 4]);
$bulk->insert(['_id' => 4]);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors());
}

?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      object(MongoDB\Driver\WriteError)#5 (4) {
        ["message"]=>
        string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 2 }"
        ["code"]=>
        int(11000)
        ["index"]=>
        int(2)
        ["info"]=>
        NULL
      }
    }

**示例 \#2 <span
class="function">MongoDB\\Driver\\WriteResult::getWriteErrors</span>
with multiple errors**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

/* The "ordered" option may be used to allow bulk write operations to continue
 * executing after the first error is encountered.
 */
$bulk = new MongoDB\Driver\BulkWrite(['ordered' => false]);
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 2]);
$bulk->insert(['_id' => 3]);
$bulk->insert(['_id' => 4]);
$bulk->insert(['_id' => 4]);

try {
    $result = $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\BulkWriteException $e) {
    var_dump($e->getWriteResult()->getWriteErrors());
}

?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      object(MongoDB\Driver\WriteError)#5 (4) {
        ["message"]=>
        string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 2 }"
        ["code"]=>
        int(11000)
        ["index"]=>
        int(2)
        ["info"]=>
        NULL
      }
      [1]=>
      object(MongoDB\Driver\WriteError)#6 (4) {
        ["message"]=>
        string(81) "E11000 duplicate key error collection: db.collection index: _id_ dup key: { : 4 }"
        ["code"]=>
        int(11000)
        ["index"]=>
        int(5)
        ["info"]=>
        NULL
      }
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\WriteError</span>

MongoDB\\Driver\\WriteResult::isAcknowledged
============================================

Returns whether the write was acknowledged

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\WriteResult::isAcknowledged</span> (
<span class="methodparam">void</span> )

If the write is acknowledged, other count fields will be available on
the <span class="classname">MongoDB\\Driver\\WriteResult</span> object.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the write was acknowledged, and **`FALSE`**
otherwise.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\WriteResult::isAcknowledged</span>
with acknowledged write concern**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk);

var_dump($result->isAcknowledged());

?>
```

以上例程会输出：

    bool(true)

**示例 \#2 <span
class="function">MongoDB\\Driver\\WriteResult::isAcknowledged</span>
with unacknowledged write concern**

``` php
<?php

$manager = new MongoDB\Driver\Manager;

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);

$result = $manager->executeBulkWrite('db.collection', $bulk, new MongoDB\Driver\WriteConcern(0));

var_dump($result->isAcknowledged());

?>
```

以上例程会输出：

    bool(false)

### 参见

-   <span class="classname">MongoDB\\Driver\\WriteConcern</span>
-   <a href="https://docs.mongodb.com/manual/reference/write-concern/" class="link external">» Write Concern reference</a>

BSON type classes and serialization functions
=============================================

**目录**

-   [函数](/set/mongodb.html#函数)
    -   [MongoDB\\BSON\\fromJSON](/set/mongodb.html#MongoDB\BSON\fromJSON)
        — Returns the BSON representation of a JSON value
    -   [MongoDB\\BSON\\fromPHP](/set/mongodb.html#MongoDB\BSON\fromPHP)
        — Returns the BSON representation of a PHP value
    -   [MongoDB\\BSON\\toCanonicalExtendedJSON](/set/mongodb.html#MongoDB\BSON\toCanonicalExtendedJSON)
        — Returns the Canonical Extended JSON representation of a BSON
        value
    -   [MongoDB\\BSON\\toJSON](/set/mongodb.html#MongoDB\BSON\toJSON) —
        Returns the Legacy Extended JSON representation of a BSON value
    -   [MongoDB\\BSON\\toPHP](/set/mongodb.html#MongoDB\BSON\toPHP) —
        Returns the PHP representation of a BSON value
    -   [MongoDB\\BSON\\toRelaxedExtendedJSON](/set/mongodb.html#MongoDB\BSON\toRelaxedExtendedJSON)
        — Returns the Relaxed Extended JSON representation of a BSON
        value
-   [MongoDB\\BSON\\Binary](/set/mongodb.html#MongoDB\BSON\Binary) — The
    MongoDB\\BSON\\Binary class
    -   [MongoDB\\BSON\\Binary::\_\_construct](/set/mongodb.html#MongoDB\BSON\Binary::__construct)
        — Construct a new Binary
    -   [MongoDB\\BSON\\Binary::getData](/set/mongodb.html#MongoDB\BSON\Binary::getData)
        — Returns the Binary's data
    -   [MongoDB\\BSON\\Binary::getType](/set/mongodb.html#MongoDB\BSON\Binary::getType)
        — Returns the Binary's type
    -   [MongoDB\\BSON\\Binary::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Binary::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Binary::serialize](/set/mongodb.html#MongoDB\BSON\Binary::serialize)
        — Serialize a Binary
    -   [MongoDB\\BSON\\Binary::\_\_toString](/set/mongodb.html#MongoDB\BSON\Binary::__toString)
        — Returns the Binary's data
    -   [MongoDB\\BSON\\Binary::unserialize](/set/mongodb.html#MongoDB\BSON\Binary::unserialize)
        — Unserialize a Binary
-   [MongoDB\\BSON\\Decimal128](/set/mongodb.html#MongoDB\BSON\Decimal128)
    — The MongoDB\\BSON\\Decimal128 class
    -   [MongoDB\\BSON\\Decimal128::\_\_construct](/set/mongodb.html#MongoDB\BSON\Decimal128::__construct)
        — Construct a new Decimal128
    -   [MongoDB\\BSON\\Decimal128::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Decimal128::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Decimal128::serialize](/set/mongodb.html#MongoDB\BSON\Decimal128::serialize)
        — Serialize a Decimal128
    -   [MongoDB\\BSON\\Decimal128::\_\_toString](/set/mongodb.html#MongoDB\BSON\Decimal128::__toString)
        — Returns the string representation of this Decimal128
    -   [MongoDB\\BSON\\Decimal128::unserialize](/set/mongodb.html#MongoDB\BSON\Decimal128::unserialize)
        — Unserialize a Decimal128
-   [MongoDB\\BSON\\Javascript](/set/mongodb.html#MongoDB\BSON\Javascript)
    — The MongoDB\\BSON\\Javascript class
    -   [MongoDB\\BSON\\Javascript::\_\_construct](/set/mongodb.html#MongoDB\BSON\Javascript::__construct)
        — Construct a new Javascript
    -   [MongoDB\\BSON\\Javascript::getCode](/set/mongodb.html#MongoDB\BSON\Javascript::getCode)
        — Returns the Javascript's code
    -   [MongoDB\\BSON\\Javascript::getScope](/set/mongodb.html#MongoDB\BSON\Javascript::getScope)
        — Returns the Javascript's scope document
    -   [MongoDB\\BSON\\Javascript::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Javascript::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Javascript::serialize](/set/mongodb.html#MongoDB\BSON\Javascript::serialize)
        — Serialize a Javascript
    -   [MongoDB\\BSON\\Javascript::\_\_toString](/set/mongodb.html#MongoDB\BSON\Javascript::__toString)
        — Returns the Javascript's code
    -   [MongoDB\\BSON\\Javascript::unserialize](/set/mongodb.html#MongoDB\BSON\Javascript::unserialize)
        — Unserialize a Javascript
-   [MongoDB\\BSON\\MaxKey](/set/mongodb.html#MongoDB\BSON\MaxKey) — The
    MongoDB\\BSON\\MaxKey class
    -   [MongoDB\\BSON\\MaxKey::\_\_construct](/set/mongodb.html#MongoDB\BSON\MaxKey::__construct)
        — Construct a new MaxKey
    -   [MongoDB\\BSON\\MaxKey::jsonSerialize](/set/mongodb.html#MongoDB\BSON\MaxKey::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\MaxKey::serialize](/set/mongodb.html#MongoDB\BSON\MaxKey::serialize)
        — Serialize a MaxKey
    -   [MongoDB\\BSON\\MaxKey::unserialize](/set/mongodb.html#MongoDB\BSON\MaxKey::unserialize)
        — Unserialize a MaxKey
-   [MongoDB\\BSON\\MinKey](/set/mongodb.html#MongoDB\BSON\MinKey) — The
    MongoDB\\BSON\\MinKey class
    -   [MongoDB\\BSON\\MinKey::\_\_construct](/set/mongodb.html#MongoDB\BSON\MinKey::__construct)
        — Construct a new MinKey
    -   [MongoDB\\BSON\\MinKey::jsonSerialize](/set/mongodb.html#MongoDB\BSON\MinKey::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\MinKey::serialize](/set/mongodb.html#MongoDB\BSON\MinKey::serialize)
        — Serialize a MinKey
    -   [MongoDB\\BSON\\MinKey::unserialize](/set/mongodb.html#MongoDB\BSON\MinKey::unserialize)
        — Unserialize a MinKey
-   [MongoDB\\BSON\\ObjectId](/set/mongodb.html#MongoDB\BSON\ObjectId) —
    The MongoDB\\BSON\\ObjectId class
    -   [MongoDB\\BSON\\ObjectId::\_\_construct](/set/mongodb.html#MongoDB\BSON\ObjectId::__construct)
        — Construct a new ObjectId
    -   [MongoDB\\BSON\\ObjectId::getTimestamp](/set/mongodb.html#MongoDB\BSON\ObjectId::getTimestamp)
        — Returns the timestamp component of this ObjectId
    -   [MongoDB\\BSON\\ObjectId::jsonSerialize](/set/mongodb.html#MongoDB\BSON\ObjectId::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\ObjectId::serialize](/set/mongodb.html#MongoDB\BSON\ObjectId::serialize)
        — Serialize an ObjectId
    -   [MongoDB\\BSON\\ObjectId::\_\_toString](/set/mongodb.html#MongoDB\BSON\ObjectId::__toString)
        — Returns the hexidecimal representation of this ObjectId
    -   [MongoDB\\BSON\\ObjectId::unserialize](/set/mongodb.html#MongoDB\BSON\ObjectId::unserialize)
        — Unserialize an ObjectId
-   [MongoDB\\BSON\\Regex](/set/mongodb.html#MongoDB\BSON\Regex) — The
    MongoDB\\BSON\\Regex class
    -   [MongoDB\\BSON\\Regex::\_\_construct](/set/mongodb.html#MongoDB\BSON\Regex::__construct)
        — Construct a new Regex
    -   [MongoDB\\BSON\\Regex::getFlags](/set/mongodb.html#MongoDB\BSON\Regex::getFlags)
        — Returns the Regex's flags
    -   [MongoDB\\BSON\\Regex::getPattern](/set/mongodb.html#MongoDB\BSON\Regex::getPattern)
        — Returns the Regex's pattern
    -   [MongoDB\\BSON\\Regex::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Regex::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Regex::serialize](/set/mongodb.html#MongoDB\BSON\Regex::serialize)
        — Serialize a Regex
    -   [MongoDB\\BSON\\Regex::\_\_toString](/set/mongodb.html#MongoDB\BSON\Regex::__toString)
        — Returns the string representation of this Regex
    -   [MongoDB\\BSON\\Regex::unserialize](/set/mongodb.html#MongoDB\BSON\Regex::unserialize)
        — Unserialize a Regex
-   [MongoDB\\BSON\\Timestamp](/set/mongodb.html#MongoDB\BSON\Timestamp)
    — The MongoDB\\BSON\\Timestamp class
    -   [MongoDB\\BSON\\Timestamp::\_\_construct](/set/mongodb.html#MongoDB\BSON\Timestamp::__construct)
        — Construct a new Timestamp
    -   [MongoDB\\BSON\\Timestamp::getIncrement](/set/mongodb.html#MongoDB\BSON\Timestamp::getIncrement)
        — Returns the increment component of this Timestamp
    -   [MongoDB\\BSON\\Timestamp::getTimestamp](/set/mongodb.html#MongoDB\BSON\Timestamp::getTimestamp)
        — Returns the timestamp component of this Timestamp
    -   [MongoDB\\BSON\\Timestamp::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Timestamp::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Timestamp::serialize](/set/mongodb.html#MongoDB\BSON\Timestamp::serialize)
        — Serialize a Timestamp
    -   [MongoDB\\BSON\\Timestamp::\_\_toString](/set/mongodb.html#MongoDB\BSON\Timestamp::__toString)
        — Returns the string representation of this Timestamp
    -   [MongoDB\\BSON\\Timestamp::unserialize](/set/mongodb.html#MongoDB\BSON\Timestamp::unserialize)
        — Unserialize a Timestamp
-   [MongoDB\\BSON\\UTCDateTime](/set/mongodb.html#MongoDB\BSON\UTCDateTime)
    — The MongoDB\\BSON\\UTCDateTime class
    -   [MongoDB\\BSON\\UTCDateTime::\_\_construct](/set/mongodb.html#MongoDB\BSON\UTCDateTime::__construct)
        — Construct a new UTCDateTime
    -   [MongoDB\\BSON\\UTCDateTime::jsonSerialize](/set/mongodb.html#MongoDB\BSON\UTCDateTime::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\UTCDateTime::serialize](/set/mongodb.html#MongoDB\BSON\UTCDateTime::serialize)
        — Serialize a UTCDateTime
    -   [MongoDB\\BSON\\UTCDateTime::toDateTime](/set/mongodb.html#MongoDB\BSON\UTCDateTime::toDateTime)
        — Returns the DateTime representation of this UTCDateTime
    -   [MongoDB\\BSON\\UTCDateTime::\_\_toString](/set/mongodb.html#MongoDB\BSON\UTCDateTime::__toString)
        — Returns the string representation of this UTCDateTime
    -   [MongoDB\\BSON\\UTCDateTime::unserialize](/set/mongodb.html#MongoDB\BSON\UTCDateTime::unserialize)
        — Unserialize a UTCDateTime
-   [MongoDB\\BSON\\Type](/set/mongodb.html#MongoDB\BSON\Type) — The
    MongoDB\\BSON\\Type interface
-   [MongoDB\\BSON\\Persistable](/set/mongodb.html#MongoDB\BSON\Persistable)
    — The MongoDB\\BSON\\Persistable interface
-   [MongoDB\\BSON\\Serializable](/set/mongodb.html#MongoDB\BSON\Serializable)
    — The MongoDB\\BSON\\Serializable interface
    -   [MongoDB\\BSON\\Serializable::bsonSerialize](/set/mongodb.html#MongoDB\BSON\Serializable::bsonSerialize)
        — Provides an array or document to serialize as BSON
-   [MongoDB\\BSON\\Unserializable](/set/mongodb.html#MongoDB\BSON\Unserializable)
    — The MongoDB\\BSON\\Unserializable interface
    -   [MongoDB\\BSON\\Unserializable::bsonUnserialize](/set/mongodb.html#MongoDB\BSON\Unserializable::bsonUnserialize)
        — Constructs the object from a BSON array or document
-   [MongoDB\\BSON\\BinaryInterface](/set/mongodb.html#MongoDB\BSON\BinaryInterface)
    — The MongoDB\\BSON\\BinaryInterface interface
    -   [MongoDB\\BSON\\BinaryInterface::getData](/set/mongodb.html#MongoDB\BSON\BinaryInterface::getData)
        — Returns the BinaryInterface's data
    -   [MongoDB\\BSON\\BinaryInterface::getType](/set/mongodb.html#MongoDB\BSON\BinaryInterface::getType)
        — Returns the BinaryInterface's type
    -   [MongoDB\\BSON\\BinaryInterface::\_\_toString](/set/mongodb.html#MongoDB\BSON\BinaryInterface::__toString)
        — Returns the BinaryInterface's data
-   [MongoDB\\BSON\\Decimal128Interface](/set/mongodb.html#MongoDB\BSON\Decimal128Interface)
    — The MongoDB\\BSON\\Decimal128Interface interface
    -   [MongoDB\\BSON\\Decimal128Interface::\_\_toString](/set/mongodb.html#MongoDB\BSON\Decimal128Interface::__toString)
        — Returns the string representation of this Decimal128Interface
-   [MongoDB\\BSON\\JavascriptInterface](/set/mongodb.html#MongoDB\BSON\JavascriptInterface)
    — The MongoDB\\BSON\\JavascriptInterface interface
    -   [MongoDB\\BSON\\JavascriptInterface::getCode](/set/mongodb.html#MongoDB\BSON\JavascriptInterface::getCode)
        — Returns the JavascriptInterface's code
    -   [MongoDB\\BSON\\JavascriptInterface::getScope](/set/mongodb.html#MongoDB\BSON\JavascriptInterface::getScope)
        — Returns the JavascriptInterface's scope document
    -   [MongoDB\\BSON\\JavascriptInterface::\_\_toString](/set/mongodb.html#MongoDB\BSON\JavascriptInterface::__toString)
        — Returns the JavascriptInterface's code
-   [MongoDB\\BSON\\MaxKeyInterface](/set/mongodb.html#MongoDB\BSON\MaxKeyInterface)
    — The MongoDB\\BSON\\MaxKeyInterface interface
-   [MongoDB\\BSON\\MinKeyInterface](/set/mongodb.html#MongoDB\BSON\MinKeyInterface)
    — The MongoDB\\BSON\\MinKeyInterface interface
-   [MongoDB\\BSON\\ObjectIdInterface](/set/mongodb.html#MongoDB\BSON\ObjectIdInterface)
    — The MongoDB\\BSON\\ObjectIdInterface interface
    -   [MongoDB\\BSON\\ObjectIdInterface::getTimestamp](/set/mongodb.html#MongoDB\BSON\ObjectIdInterface::getTimestamp)
        — Returns the timestamp component of this ObjectIdInterface
    -   [MongoDB\\BSON\\ObjectIdInterface::\_\_toString](/set/mongodb.html#MongoDB\BSON\ObjectIdInterface::__toString)
        — Returns the hexidecimal representation of this
        ObjectIdInterface
-   [MongoDB\\BSON\\RegexInterface](/set/mongodb.html#MongoDB\BSON\RegexInterface)
    — The MongoDB\\BSON\\RegexInterface interface
    -   [MongoDB\\BSON\\RegexInterface::getFlags](/set/mongodb.html#MongoDB\BSON\RegexInterface::getFlags)
        — Returns the RegexInterface's flags
    -   [MongoDB\\BSON\\RegexInterface::getPattern](/set/mongodb.html#MongoDB\BSON\RegexInterface::getPattern)
        — Returns the RegexInterface's pattern
    -   [MongoDB\\BSON\\RegexInterface::\_\_toString](/set/mongodb.html#MongoDB\BSON\RegexInterface::__toString)
        — Returns the string representation of this RegexInterface
-   [MongoDB\\BSON\\TimestampInterface](/set/mongodb.html#MongoDB\BSON\TimestampInterface)
    — The MongoDB\\BSON\\TimestampInterface interface
    -   [MongoDB\\BSON\\TimestampInterface::getIncrement](/set/mongodb.html#MongoDB\BSON\TimestampInterface::getIncrement)
        — Returns the increment component of this TimestampInterface
    -   [MongoDB\\BSON\\TimestampInterface::getTimestamp](/set/mongodb.html#MongoDB\BSON\TimestampInterface::getTimestamp)
        — Returns the timestamp component of this TimestampInterface
    -   [MongoDB\\BSON\\TimestampInterface::\_\_toString](/set/mongodb.html#MongoDB\BSON\TimestampInterface::__toString)
        — Returns the string representation of this TimestampInterface
-   [MongoDB\\BSON\\UTCDateTimeInterface](/set/mongodb.html#MongoDB\BSON\UTCDateTimeInterface)
    — The MongoDB\\BSON\\UTCDateTimeInterface interface
    -   [MongoDB\\BSON\\UTCDateTimeInterface::toDateTime](/set/mongodb.html#MongoDB\BSON\UTCDateTimeInterface::toDateTime)
        — Returns the DateTime representation of this
        UTCDateTimeInterface
    -   [MongoDB\\BSON\\UTCDateTimeInterface::\_\_toString](/set/mongodb.html#MongoDB\BSON\UTCDateTimeInterface::__toString)
        — Returns the string representation of this UTCDateTimeInterface
-   [MongoDB\\BSON\\DBPointer](/set/mongodb.html#MongoDB\BSON\DBPointer)
    — The MongoDB\\BSON\\DBPointer class (deprecated)
    -   [MongoDB\\BSON\\DBPointer::\_\_construct](/set/mongodb.html#MongoDB\BSON\DBPointer::__construct)
        — Construct a new DBPointer (unused)
    -   [MongoDB\\BSON\\DBPointer::jsonSerialize](/set/mongodb.html#MongoDB\BSON\DBPointer::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\DBPointer::serialize](/set/mongodb.html#MongoDB\BSON\DBPointer::serialize)
        — Serialize a DBPointer
    -   [MongoDB\\BSON\\DBPointer::\_\_toString](/set/mongodb.html#MongoDB\BSON\DBPointer::__toString)
        — Returns an empty string
    -   [MongoDB\\BSON\\DBPointer::unserialize](/set/mongodb.html#MongoDB\BSON\DBPointer::unserialize)
        — Unserialize a DBPointer
-   [MongoDB\\BSON\\Int64](/set/mongodb.html#MongoDB\BSON\Int64) — The
    MongoDB\\BSON\\Int64 class
    -   [MongoDB\\BSON\\Int64::\_\_construct](/set/mongodb.html#MongoDB\BSON\Int64::__construct)
        — Construct a new Int64 (unused)
    -   [MongoDB\\BSON\\Int64::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Int64::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Int64::serialize](/set/mongodb.html#MongoDB\BSON\Int64::serialize)
        — Serialize an Int64
    -   [MongoDB\\BSON\\Int64::\_\_toString](/set/mongodb.html#MongoDB\BSON\Int64::__toString)
        — Returns the string representation of this Int64
    -   [MongoDB\\BSON\\Int64::unserialize](/set/mongodb.html#MongoDB\BSON\Int64::unserialize)
        — Unserialize an Int64
-   [MongoDB\\BSON\\Symbol](/set/mongodb.html#MongoDB\BSON\Symbol) — The
    MongoDB\\BSON\\Symbol class (deprecated)
    -   [MongoDB\\BSON\\Symbol::\_\_construct](/set/mongodb.html#MongoDB\BSON\Symbol::__construct)
        — Construct a new Symbol (unused)
    -   [MongoDB\\BSON\\Symbol::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Symbol::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Symbol::serialize](/set/mongodb.html#MongoDB\BSON\Symbol::serialize)
        — Serialize a Symbol
    -   [MongoDB\\BSON\\Symbol::\_\_toString](/set/mongodb.html#MongoDB\BSON\Symbol::__toString)
        — Returns the Symbol as a string
    -   [MongoDB\\BSON\\Symbol::unserialize](/set/mongodb.html#MongoDB\BSON\Symbol::unserialize)
        — Unserialize a Symbol
-   [MongoDB\\BSON\\Undefined](/set/mongodb.html#MongoDB\BSON\Undefined)
    — The MongoDB\\BSON\\Undefined class (deprecated)
    -   [MongoDB\\BSON\\Undefined::\_\_construct](/set/mongodb.html#MongoDB\BSON\Undefined::__construct)
        — Construct a new Undefined (unused)
    -   [MongoDB\\BSON\\Undefined::jsonSerialize](/set/mongodb.html#MongoDB\BSON\Undefined::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [MongoDB\\BSON\\Undefined::serialize](/set/mongodb.html#MongoDB\BSON\Undefined::serialize)
        — Serialize a Undefined
    -   [MongoDB\\BSON\\Undefined::\_\_toString](/set/mongodb.html#MongoDB\BSON\Undefined::__toString)
        — Returns an empty string
    -   [MongoDB\\BSON\\Undefined::unserialize](/set/mongodb.html#MongoDB\BSON\Undefined::unserialize)
        — Unserialize a Undefined

MongoDB\\BSON\\fromJSON
=======================

Returns the BSON representation of a JSON value

### 说明

<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\fromJSON</span> ( <span
class="methodparam"><span class="type">string</span> `$json`</span> )

Converts an
<a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» extended JSON</a>
string to its BSON representation.

### 参数

`json` (<span class="type">string</span>)  
JSON value to be converted.

### 返回值

The serialized BSON document as a binary string.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the JSON value cannot be converted to BSON (e.g. due to a syntax
    error).

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\fromJSON</span>
example**

``` php
<?php

$json = '{ "_id": { "$oid": "563143b280d2387c91807965" } }';
$bson = MongoDB\BSON\fromJSON($json);
$value = MongoDB\BSON\toPHP($bson);
var_dump($value);

?>
```

以上例程会输出：

    object(stdClass)#2 (1) {
      ["_id"]=>
      object(MongoDB\BSON\ObjectId)#1 (1) {
        ["oid"]=>
        string(24) "563143b280d2387c91807965"
      }
    }

### 参见

-   <span class="function">MongoDB\\BSON\\toJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» MongoDB BSON</a>

MongoDB\\BSON\\fromPHP
======================

Returns the BSON representation of a PHP value

### 说明

<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\fromPHP</span> ( <span
class="methodparam"><span class="type">array\|object</span>
`$value`</span> )

Serializes a PHP array or object (e.g. document) to its
<a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON</a>
representation. The returned binary string will describe a BSON
document.

### 参数

`value` (<span class="type">array\|object</span>)  
PHP value to be serialized.

### 返回值

The serialized BSON document as a binary string.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the PHP value cannot be converted to BSON. Possible reasons
    include, but are not limited to, encountering an unexpected <span
    class="interfacename">MongoDB\\BSON\\Type</span> instance or <span
    class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
    failing to return an <span class="type">array</span> or <span
    class="classname">stdClass</span>.

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\fromPHP</span>
example**

``` php
<?php

$bson = MongoDB\BSON\fromPHP(['foo' => 1]);
echo bin2hex($bson), "\n";

?>
```

以上例程会输出：

    0e00000010666f6f000100000000cat 

### 参见

-   <span class="function">MongoDB\\BSON\\toPHP</span>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» MongoDB BSON</a>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

MongoDB\\BSON\\toCanonicalExtendedJSON
======================================

Returns the Canonical Extended JSON representation of a BSON value

### 说明

<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\toCanonicalExtendedJSON</span> ( <span
class="methodparam"><span class="type">string</span> `$bson`</span> )

Converts a BSON string to its
<a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» Canonical Extended JSON</a>
representation. The canonical format prefers type fidelity at the
expense of concise output and is most suited for producing output that
can be converted back to BSON without any loss of type information (e.g.
numeric types will remain differentiated).

### 参数

`bson` (<span class="type">string</span>)  
BSON value to be converted.

### 返回值

The converted JSON value.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the input did not contain exactly one BSON document. Possible
    reasons include, but are not limited to, invalid BSON, extra data
    (after reading one BSON document), or an unexpected
    <a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
    error.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span> example**

``` php
<?php

$documents = [
    [ 'null' => null ],
    [ 'boolean' => true ],
    [ 'string' => 'foo' ],
    [ 'int32' => 123 ],
    [ 'int64' => 4294967295 ],
    [ 'double' => 1.0, ],
    [ 'nan' => NAN ],
    [ 'pos_inf' => INF ],
    [ 'neg_inf' => -INF ],
    [ 'array' => [ 'foo', 'bar' ]],
    [ 'document' => [ 'foo' => 'bar' ]],
    [ 'oid' => new MongoDB\BSON\ObjectId('56315a7c6118fd1b920270b1') ],
    [ 'dec128' => new MongoDB\BSON\Decimal128('1234.5678') ],
    [ 'binary' => new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC) ],
    [ 'date' => new MongoDB\BSON\UTCDateTime(1445990400000) ],
    [ 'timestamp' => new MongoDB\BSON\Timestamp(1234, 5678) ],
    [ 'regex' => new MongoDB\BSON\Regex('pattern', 'i') ],
    [ 'code' => new MongoDB\BSON\Javascript('function() { return 1; }') ],
    [ 'code_ws' => new MongoDB\BSON\Javascript('function() { return a; }', ['a' => 1]) ],
    [ 'minkey' => new MongoDB\BSON\MinKey ],
    [ 'maxkey' => new MongoDB\BSON\MaxKey ],
];

foreach ($documents as $document) {
    $bson = MongoDB\BSON\fromPHP($document);
    echo MongoDB\BSON\toCanonicalExtendedJSON($bson), "\n";
}

?>
```

以上例程会输出：

    { "null" : null }
    { "boolean" : true }
    { "string" : "foo" }
    { "int32" : { "$numberInt" : "123" } }
    { "int64" : { "$numberLong" : "4294967295"} }
    { "double" : { "$numberDouble" : "1.0" } }
    { "nan" : { "$numberDouble" : "NaN" } }
    { "pos_inf" : { "$numberDouble" : "Infinity" } }
    { "neg_inf" : { "$numberDouble" : "-Infinity" } }
    { "array" : [ "foo", "bar" ] }
    { "document" : { "foo" : "bar" } }
    { "oid" : { "$oid" : "56315a7c6118fd1b920270b1" } }
    { "dec128" : { "$numberDecimal" : "1234.5678" } }
    { "binary" : { "$binary" : { "base64": "Zm9v", "subType" : "00" } } }
    { "date" : { "$date" : { "$numberLong" : "1445990400000" } } }
    { "timestamp" : { "$timestamp" : { "t" : 5678, "i" : 1234 } } }
    { "regex" : { "$regularExpression" : { "pattern" : "pattern", "options" : "i" } } }
    { "code" : { "$code" : "function() { return 1; }" } }
    { "code_ws" : { "$code" : "function() { return a; }", "$scope" : { "a" : { "$numberInt" : "1" } } } }
    { "minkey" : { "$minKey" : 1 } }
    { "maxkey" : { "$maxKey" : 1 } }

### 参见

-   <span class="function">MongoDB\\BSON\\fromJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst" class="link external">» Extended JSON Specification</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» MongoDB BSON</a>

MongoDB\\BSON\\toJSON
=====================

Returns the Legacy Extended JSON representation of a BSON value

### 说明

<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\toJSON</span> ( <span
class="methodparam"><span class="type">string</span> `$bson`</span> )

Converts a BSON string to its
<a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» Legacy Extended JSON</a>
representation.

> **Note**: <span class="simpara"> There exist several JSON formats for
> representing BSON. This function implements the "strict mode" defined
> in
> <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>,
> which has been superseded by the canonical and relaxed formats defined
> in the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst" class="link external">» Extended JSON Specification</a>
> and implemented by <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span> and
> <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>,
> respectively. </span>

**Warning**

<a href="http://www.json.org/" class="link external">» JSON</a> does not
support
<a href="/language/types/float.html#language.types.float.nan" class="link"><strong><code>NAN</code></strong></a>
and
<a href="/ref/math.html#is_infinite" class="link"><strong><code>INF</code></strong></a>
and MongoDB's Legacy Extended JSON format does not define an alternative
representation for these values
(<a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
will output *nan* and *inf* literals, which may not be parsed as valid
JSON). If you are working with BSON that may contain non-finite numbers,
please use <span
class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span> or <span
class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>.

### 参数

`bson` (<span class="type">string</span>)  
BSON value to be converted.

### 返回值

The converted JSON value.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the input did not contain exactly one BSON document. Possible
    reasons include, but are not limited to, invalid BSON, extra data
    (after reading one BSON document), or an unexpected
    <a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
    error.

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\toJSON</span> example**

``` php
<?php

$documents = [
    [ 'null' => null ],
    [ 'boolean' => true ],
    [ 'string' => 'foo' ],
    [ 'int32' => 123 ],
    [ 'int64' => 4294967295 ],
    [ 'double' => 1.0, ],
    [ 'nan' => NAN ],
    [ 'pos_inf' => INF ],
    [ 'neg_inf' => -INF ],
    [ 'array' => [ 'foo', 'bar' ]],
    [ 'document' => [ 'foo' => 'bar' ]],
    [ 'oid' => new MongoDB\BSON\ObjectId('56315a7c6118fd1b920270b1') ],
    [ 'dec128' => new MongoDB\BSON\Decimal128('1234.5678') ],
    [ 'binary' => new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC) ],
    [ 'date' => new MongoDB\BSON\UTCDateTime(1445990400000) ],
    [ 'timestamp' => new MongoDB\BSON\Timestamp(1234, 5678) ],
    [ 'regex' => new MongoDB\BSON\Regex('pattern', 'i') ],
    [ 'code' => new MongoDB\BSON\Javascript('function() { return 1; }') ],
    [ 'code_ws' => new MongoDB\BSON\Javascript('function() { return a; }', ['a' => 1]) ],
    [ 'minkey' => new MongoDB\BSON\MinKey ],
    [ 'maxkey' => new MongoDB\BSON\MaxKey ],
];

foreach ($documents as $document) {
    $bson = MongoDB\BSON\fromPHP($document);
    echo MongoDB\BSON\toJSON($bson), "\n";
}

?>
```

以上例程会输出：

    { "null" : null }
    { "boolean" : true }
    { "string" : "foo" }
    { "int32" : 123 }
    { "int64" : 4294967295 }
    { "double" : 1.0 }
    { "nan" : nan }
    { "pos_inf" : inf }
    { "neg_inf" : -inf }
    { "array" : [ "foo", "bar" ] }
    { "document" : { "foo" : "bar" } }
    { "oid" : { "$oid" : "56315a7c6118fd1b920270b1" } }
    { "dec128" : { "$numberDecimal" : "1234.5678" } }
    { "binary" : { "$binary" : "Zm9v", "$type" : "00" } }
    { "date" : { "$date" : 1445990400000 } }
    { "timestamp" : { "$timestamp" : { "t" : 5678, "i" : 1234 } } }
    { "regex" : { "$regex" : "pattern", "$options" : "i" } }
    { "code" : { "$code" : "function() { return 1; }" } }
    { "code_ws" : { "$code" : "function() { return a; }", "$scope" : { "a" : 1 } } }
    { "minkey" : { "$minKey" : 1 } }
    { "maxkey" : { "$maxKey" : 1 } }

### 参见

-   <span class="function">MongoDB\\BSON\\fromJSON</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» MongoDB BSON</a>

MongoDB\\BSON\\toPHP
====================

Returns the PHP representation of a BSON value

### 说明

<span class="type">array\|object</span> <span
class="methodname">MongoDB\\BSON\\toPHP</span> ( <span
class="methodparam"><span class="type">string</span> `$bson`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$typeMap`<span class="initializer"> = array()</span></span> \] )

Unserializes a BSON document (i.e. binary string) to its PHP
representation. The `typeMap` paramater may be used to control the PHP
types used for converting BSON arrays and documents (both root and
embedded).

**Warning**

Fields containing deprecated BSON types (i.e. undefined, symbol,
DBPointer) are represented only by bare-bones objects of the classes
<span class="classname">MongoDB\\BSON\\Undefined</span>, <span
class="classname">MongoDB\\BSON\\Symbol</span>, and <span
class="classname">MongoDB\\BSON\\DBPointer</span>, when converting BSON
to PHP. These objects are created from BSON data and used for storing
these types back into the database, but can not be instantiated as they
have a private constructor.

### 参数

`bson` (<span class="type">string</span>)  
BSON value to be unserialized.

`typeMap` (<span class="type">array</span>)  
<a href="/set/mongodb.html#TypeMaps" class="link">Type map configuration</a>.

### 返回值

The unserialized PHP value.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if a class in the type map cannot be instantiated or does not
    implement <span
    class="interfacename">MongoDB\\BSON\\Unserializable</span>.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the input did not contain exactly one BSON document. Possible
    reasons include, but are not limited to, invalid BSON, extra data
    (after reading one BSON document), or an unexpected
    <a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
    error.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                                    |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.4.0 | If the input contains an unsupported, deprecated BSON type, the driver will now no longer log a warning to the debug log, but instead will create an object representing this type.                                                                                                                                                                                     |
| 1.3.2 | <span class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span> is no longer thrown if the input contains an unsupported, deprecated BSON type. Such types will be ignored (as they were in versions before 1.3.0), although the driver will now log a warning to the debug log (see: <a href="/set/mongodb.html#" class="link">mongodb.debug</a>). |
| 1.3.0 | <span class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span> is thrown if the input contains an unsupported, deprecated BSON type. Previously, such types were ignored.                                                                                                                                                                          |

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\toPHP</span> example**

``` php
<?php

$bson = hex2bin('0e00000010666f6f000100000000');
$value = MongoDB\BSON\toPHP($bson);
var_dump($value);

?>
```

以上例程会输出：

    object(stdClass)#1 (1) {
      ["foo"]=>
      int(1)
    }

### 参见

-   <span class="function">MongoDB\\BSON\\fromPHP</span>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» MongoDB BSON</a>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

MongoDB\\BSON\\toRelaxedExtendedJSON
====================================

Returns the Relaxed Extended JSON representation of a BSON value

### 说明

<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\toRelaxedExtendedJSON</span> ( <span
class="methodparam"><span class="type">string</span> `$bson`</span> )

Converts a BSON string to its
<a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» Relaxed Extended JSON</a>
representation. The relaxed format prefers use of JSON type primitives
at the expense of type fidelity and is most suited for producing output
that can be easily consumed by web APIs and humans.

### 参数

`bson` (<span class="type">string</span>)  
BSON value to be converted.

### 返回值

The converted JSON value.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the input did not contain exactly one BSON document. Possible
    reasons include, but are not limited to, invalid BSON, extra data
    (after reading one BSON document), or an unexpected
    <a href="https://github.com/mongodb/libbson" class="link external">» libbson</a>
    error.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> example**

``` php
<?php

$documents = [
    [ 'null' => null ],
    [ 'boolean' => true ],
    [ 'string' => 'foo' ],
    [ 'int32' => 123 ],
    [ 'int64' => 4294967295 ],
    [ 'double' => 1.0, ],
    [ 'nan' => NAN ],
    [ 'pos_inf' => INF ],
    [ 'neg_inf' => -INF ],
    [ 'array' => [ 'foo', 'bar' ]],
    [ 'document' => [ 'foo' => 'bar' ]],
    [ 'oid' => new MongoDB\BSON\ObjectId('56315a7c6118fd1b920270b1') ],
    [ 'dec128' => new MongoDB\BSON\Decimal128('1234.5678') ],
    [ 'binary' => new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC) ],
    [ 'date' => new MongoDB\BSON\UTCDateTime(1445990400000) ],
    [ 'timestamp' => new MongoDB\BSON\Timestamp(1234, 5678) ],
    [ 'regex' => new MongoDB\BSON\Regex('pattern', 'i') ],
    [ 'code' => new MongoDB\BSON\Javascript('function() { return 1; }') ],
    [ 'code_ws' => new MongoDB\BSON\Javascript('function() { return a; }', ['a' => 1]) ],
    [ 'minkey' => new MongoDB\BSON\MinKey ],
    [ 'maxkey' => new MongoDB\BSON\MaxKey ],
];

foreach ($documents as $document) {
    $bson = MongoDB\BSON\fromPHP($document);
    echo MongoDB\BSON\toRelaxedExtendedJSON($bson), "\n";
}

?>
```

以上例程会输出：

    { "null" : null }
    { "boolean" : true }
    { "string" : "foo" }
    { "int32" : 123 }
    { "int64" : 4294967295 }
    { "double" : 1.0 }
    { "nan" : { "$numberDouble" : "NaN" } }
    { "pos_inf" : { "$numberDouble" : "Infinity" } }
    { "neg_inf" : { "$numberDouble" : "-Infinity" } }
    { "array" : [ "foo", "bar" ] }
    { "document" : { "foo" : "bar" } }
    { "oid" : { "$oid" : "56315a7c6118fd1b920270b1" } }
    { "dec128" : { "$numberDecimal" : "1234.5678" } }
    { "binary" : { "$binary" : { "base64": "Zm9v", "subType" : "00" } } }
    { "date" : { "$date" : "2015-10-28T00:00:00Z" } }
    { "timestamp" : { "$timestamp" : { "t" : 5678, "i" : 1234 } } }
    { "regex" : { "$regularExpression" : { "pattern" : "pattern", "options" : "i" } } }
    { "code" : { "$code" : "function() { return 1; }" } }
    { "code_ws" : { "$code" : "function() { return a; }", "$scope" : { "a" : 1 } } }
    { "minkey" : { "$minKey" : 1 } }
    { "maxkey" : { "$maxKey" : 1 } }

### 参见

-   <span class="function">MongoDB\\BSON\\fromJSON</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst" class="link external">» Extended JSON</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» MongoDB BSON</a>

**目录**

-   [MongoDB\\BSON\\fromJSON](/set/mongodb.html#MongoDB\BSON\fromJSON) —
    Returns the BSON representation of a JSON value
-   [MongoDB\\BSON\\fromPHP](/set/mongodb.html#MongoDB\BSON\fromPHP) —
    Returns the BSON representation of a PHP value
-   [MongoDB\\BSON\\toCanonicalExtendedJSON](/set/mongodb.html#MongoDB\BSON\toCanonicalExtendedJSON)
    — Returns the Canonical Extended JSON representation of a BSON value
-   [MongoDB\\BSON\\toJSON](/set/mongodb.html#MongoDB\BSON\toJSON) —
    Returns the Legacy Extended JSON representation of a BSON value
-   [MongoDB\\BSON\\toPHP](/set/mongodb.html#MongoDB\BSON\toPHP) —
    Returns the PHP representation of a BSON value
-   [MongoDB\\BSON\\toRelaxedExtendedJSON](/set/mongodb.html#MongoDB\BSON\toRelaxedExtendedJSON)
    — Returns the Relaxed Extended JSON representation of a BSON value

简介
----

BSON type for binary data (i.e. array of bytes). Binary values also have
a subtype, which is used to indicate what kind of data is in the byte
array. Subtypes from zero to 127 are predefined or reserved. Subtypes
from 128-255 are user-defined.

类摘要
------

**MongoDB\\BSON\\Binary**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Binary** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\BinaryInterface</span>
</span> <span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_GENERIC` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_FUNCTION` <span class="initializer"> =
1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_OLD_BINARY` <span class="initializer"> =
2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_OLD_UUID` <span class="initializer"> =
3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_UUID` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_MD5` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_ENCRYPTED` <span class="initializer"> =
6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`MongoDB\BSON\Binary::TYPE_USER_DEFINED` <span class="initializer"> =
128</span> ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span class="methodname">getData</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getType</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

预定义常量
----------

**`MongoDB\BSON\Binary::TYPE_GENERIC`**  
Generic binary data.

**`MongoDB\BSON\Binary::TYPE_FUNCTION`**  
Function.

**`MongoDB\BSON\Binary::TYPE_OLD_BINARY`**  
Generic binary data (deprecated in favor of
**`MongoDB\BSON\Binary::TYPE_GENERIC`**).

**`MongoDB\BSON\Binary::TYPE_OLD_UUID`**  
Universally unique identifier (deprecated in favor of
**`MongoDB\BSON\Binary::TYPE_UUID`**). When using this type, the
Binary's data should be 16 bytes in length.

Historically, other drivers encoded values with this type based on their
language conventions (e.g. varying endianness), which makes it
non-portable. The PHP driver applies no special handling for encoding or
decoding data with this type.

**`MongoDB\BSON\Binary::TYPE_UUID`**  
Universally unique identifier. When using this type, the Binary's data
should be 16 bytes in length and encoded according to
<a href="http://www.faqs.org/rfcs/rfc4122" class="link external">» RFC 4122</a>.

**`MongoDB\BSON\Binary::TYPE_MD5`**  
MD5 hash. When using this type, the Binary's data should be 16 bytes in
length.

**`MongoDB\BSON\Binary::TYPE_ENCRYPTED`**  
Encrypted value. This subtype is used for client-side encryption.

**`MongoDB\BSON\Binary::TYPE_USER_DEFINED`**  
User-defined type. While types between 0 and 127 are predefined or
reserved, types between 128 and 255 are user-defined and may be used for
anything.

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\BinaryInterface</span>.                                       |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\Binary::\_\_construct
====================================

Construct a new Binary

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\Binary::\_\_construct</span> (
<span class="methodparam"><span class="type">string</span>
`$data`</span> , <span class="methodparam"><span class="type">int</span>
`$type`</span> )

### 参数

`data` (<span class="type">string</span>)  
Binary data.

`type` (<span class="type">integer</span>)  
Unsigned 8-bit integer denoting the data's type.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `type` is not an unsigned 8-bit integer.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `type` is **`MongoDB\BSON\Binary::TYPE_UUID`** or
    **`MongoDB\BSON\Binary::TYPE_OLD_UUID`** and `data` is not exactly
    16 bytes in length.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> is thrown if `type` is **`MongoDB\BSON\Binary::TYPE_UUID`** or **`MongoDB\BSON\Binary::TYPE_OLD_UUID`** and `data` is not exactly 16 bytes in length. |
| 1.1.3 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> is thrown if `type` is not an unsigned 8-bit integer.                                                                                                 |

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Binary::\_\_construct</span> example**

``` php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary);

?>
```

以上例程会输出：

    object(MongoDB\BSON\Binary)#1 (2) {
      ["data"]=>
      string(3) "foo"
      ["type"]=>
      int(0)
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Binary::getData
==============================

Returns the Binary's data

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Binary::getData</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the Binary's data.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\Binary::getData</span>
example**

``` php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getData());

?>
```

以上例程会输出：

    string(3) "foo"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Binary::getType
==============================

Returns the Binary's type

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\Binary::getType</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the Binary's type.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\Binary::getType</span>
example**

``` php
<?php

$binary = new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC);
var_dump($binary->getType());

?>
```

以上例程会输出：

    int(0)

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Binary::jsonSerialize
====================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Binary::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Binary</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Binary::serialize
================================

Serialize a Binary

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Binary::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Binary</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Binary::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Binary::\_\_toString
===================================

Returns the Binary's data

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Binary::\_\_toString</span> ( <span
class="methodparam">void</span> )

此方法是该方法的别名： <span
class="methodname">MongoDB\\BSON\\Binary::getData</span>.

### 参数

此函数没有参数。

### 返回值

Returns the Binary's data.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Binary::\_\_toString</span> example**

``` php
<?php

var_dump((string) new MongoDB\BSON\Binary('foo', MongoDB\BSON\Binary::TYPE_GENERIC));

?>
```

以上例程会输出：

    string(3) "foo"

### 参见

-   <span class="methodname">MongoDB\\BSON\\Binary::getData</span>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Binary::unserialize
==================================

Unserialize a Binary

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Binary::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Binary</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Binary</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\Binary::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for the
<a href="https://en.wikipedia.org/wiki/Decimal128_floating-point_format" class="link external">» Decimal128 floating-point format</a>,
which supports numbers with up to 34 decimal digits (i.e. significant
digits) and an exponent range of −6143 to +6144.

Unlike the double BSON type (i.e. <span class="type">float</span> in
PHP), which only stores an approximation of the decimal values, the
decimal data type stores the exact value. For example,
*MongoDB\\BSON\\Decimal128('9.99')* has a precise value of 9.99 where as
a double 9.99 would have an approximate value of
9.9900000000000002131628….

> **Note**: <span class="simpara"> <span
> class="classname">MongoDB\\BSON\\Decimal128</span> is only compatible
> with MongoDB 3.4+. Attempting to use the BSON type with an earlier
> version of MongoDB will result in an error. </span>

类摘要
------

**MongoDB\\BSON\\Decimal128**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Decimal128** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Decimal128Interface</span> </span>
<span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$value`</span> \]
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\Decimal128Interface</span>.                                   |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\Decimal128::\_\_construct
========================================

Construct a new Decimal128

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\Decimal128::\_\_construct</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$value`</span> \] )

> **Note**: <span class="simpara"> <span
> class="classname">MongoDB\\BSON\\Decimal128</span> is only compatible
> with MongoDB 3.4+. Attempting to use the BSON type with an earlier
> version of MongoDB will result in an error. </span>

### 参数

`value` (<span class="type">string</span>)  
A decimal string.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `value` is not a valid decimal string.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Decimal128::\_\_construct</span>
example**

``` php
<?php

var_dump(new MongoDB\BSON\Decimal128(1234.5678));
var_dump(new MongoDB\BSON\Decimal128(NAN));
var_dump(new MongoDB\BSON\Decimal128(INF));

?>
```

以上例程的输出类似于：

    object(MongoDB\BSON\Decimal128)#1 (1) {
      ["dec"]=>
      string(9) "1234.5678"
    }
    object(MongoDB\BSON\Decimal128)#1 (1) {
      ["dec"]=>
      string(3) "NaN"
    }
    object(MongoDB\BSON\Decimal128)#1 (1) {
      ["dec"]=>
      string(8) "Infinity"
    }

### 参见

-   <a href="https://en.wikipedia.org/wiki/Decimal128_floating-point_format" class="link external">» Decimal128 floating-point format</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Decimal128::jsonSerialize
========================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Decimal128::jsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Decimal128</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Decimal128::serialize
====================================

Serialize a Decimal128

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Decimal128::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Decimal128</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Decimal128::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Decimal128::\_\_toString
=======================================

Returns the string representation of this Decimal128

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Decimal128::\_\_toString</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this Decimal128.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Decimal128::\_\_toString</span>
example**

``` php
<?php

var_dump((string) new MongoDB\BSON\Decimal128(1234.5678));
var_dump((string) new MongoDB\BSON\Decimal128(NAN));
var_dump((string) new MongoDB\BSON\Decimal128(INF));

?>
```

以上例程的输出类似于：

    string(9) "1234.5678"
    string(3) "NaN"
    string(8) "Infinity"

### 参见

-   <a href="https://en.wikipedia.org/wiki/Decimal128_floating-point_format" class="link external">» Decimal128 floating-point format</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Decimal128::unserialize
======================================

Unserialize a Decimal128

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Decimal128::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Decimal128</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Decimal128</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\Decimal128::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for Javascript code. An optional scope document may be
specified that maps identifiers to values and defines the scope in which
the code should be evaluated by the server.

> **Note**: <span class="simpara"> This BSON type is mainly used when
> executing database commands that take a Javascript function as a
> parameter, such as
> <a href="https://docs.mongodb.com/manual/reference/command/mapReduce/" class="link external">» mapReduce</a>.
> </span>

类摘要
------

**MongoDB\\BSON\\Javascript**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Javascript** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\JavascriptInterface</span> </span>
<span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">array\|object</span>
`$scope`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span class="methodname">getCode</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">getScope</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\JavascriptInterface</span>.                                   |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\Javascript::\_\_construct
========================================

Construct a new Javascript

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\Javascript::\_\_construct</span>
( <span class="methodparam"><span class="type">string</span>
`$code`</span> \[, <span class="methodparam"><span
class="type">array\|object</span> `$scope`</span> \] )

### 参数

`code` (<span class="type">string</span>)  
Javascript code.

`scope` (<span class="type">array\|object</span>)  
Javascript scope.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `code` contains null bytes.

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.0 | <span class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span> is thrown if `code` contains null bytes. Previously, values would be truncated at the first null byte. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Javascript::\_\_construct</span>
example**

``` php
<?php

$code = new MongoDB\BSON\Javascript('function() { return 1; }');
var_dump($code);

$codews = new MongoDB\BSON\Javascript('function() { return foo; }', ['foo' => 'bar']);
var_dump($codews);

?>
```

以上例程会输出：

    object(MongoDB\BSON\Javascript)#1 (2) {
      ["javascript"]=>
      string(24) "function() { return 1; }"
      ["scope"]=>
      object(stdClass)#2 (0) {
      }
    }
    object(MongoDB\BSON\Javascript)#2 (2) {
      ["javascript"]=>
      string(26) "function() { return foo; }"
      ["scope"]=>
      object(stdClass)#1 (1) {
        ["foo"]=>
        string(3) "bar"
      }
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Javascript::getCode
==================================

Returns the Javascript's code

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Javascript::getCode</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the Javascript's code.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Javascript::getCode</span> example**

``` php
<?php

$js = new MongoDB\BSON\Javascript('function foo(bar) { return bar; }');
var_dump($js->getCode());

?>
```

以上例程会输出：

    string(33) "function foo(bar) { return bar; }"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Javascript::getScope
===================================

Returns the Javascript's scope document

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object\|null</span> <span
class="methodname">MongoDB\\BSON\\Javascript::getScope</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the Javascript's scope document, or **`NULL`** if the is no
scope.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Javascript::getScope</span> example**

``` php
<?php

$js = new MongoDB\BSON\Javascript('function foo(bar) { return bar; }');
var_dump($js->getScope());

$js = new MongoDB\BSON\Javascript('function foo() { return foo; }', ['foo' => 42]);
var_dump($js->getScope());

?>
```

以上例程会输出：

    NULL
    object(stdClass)#1 (1) {
      ["foo"]=>
      int(42)
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Javascript::jsonSerialize
========================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Javascript::jsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Javascript</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Javascript::serialize
====================================

Serialize a Javascript

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Javascript::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Javascript</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Javascript::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Javascript::\_\_toString
=======================================

Returns the Javascript's code

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Javascript::\_\_toString</span> (
<span class="methodparam">void</span> )

此方法是该方法的别名： <span
class="methodname">MongoDB\\BSON\\Javascript::getCode</span>.

### 参数

此函数没有参数。

### 返回值

Returns the Javascript's code.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Javascript::\_\_toString</span>
example**

``` php
<?php

var_dump((string) new MongoDB\BSON\Javascript('function foo(bar) { return bar; }'));

?>
```

以上例程会输出：

    string(33) "function foo(bar) { return bar; }"

### 参见

-   <span class="methodname">MongoDB\\BSON\\Javascript::getCode</span>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Javascript::unserialize
======================================

Unserialize a Javascript

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Javascript::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Javascript</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Javascript</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\Javascript::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

Special BSON type which compares higher than all other possible BSON
element values.

> **Note**: <span class="simpara"> This is an internal MongoDB type used
> for indexing and sharding. </span>

类摘要
------

**MongoDB\\BSON\\MaxKey**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\MaxKey** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\MaxKeyInterface</span>
</span> <span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\MaxKeyInterface</span>.                                       |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\MaxKey::\_\_construct
====================================

Construct a new MaxKey

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\MaxKey::\_\_construct</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\MaxKey::\_\_construct</span> example**

``` php
<?php

var_dump(new MongoDB\BSON\MaxKey());

?>
```

以上例程会输出：

    object(MongoDB\BSON\MaxKey)#1 (0) {
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\MaxKey::jsonSerialize
====================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\MaxKey::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\MaxKey</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\MaxKey::serialize
================================

Serialize a MaxKey

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\MaxKey::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\MaxKey</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\MaxKey::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\MaxKey::unserialize
==================================

Unserialize a MaxKey

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\MaxKey::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\MaxKey</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\MaxKey</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\MaxKey::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

Special BSON type which compares lower than all other possible BSON
element values.

> **Note**: <span class="simpara"> This is an internal MongoDB type used
> for indexing and sharding. </span>

类摘要
------

**MongoDB\\BSON\\MinKey**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\MinKey** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\MinKeyInterface</span>
</span> <span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\MinKeyInterface</span>.                                       |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\MinKey::\_\_construct
====================================

Construct a new MinKey

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\MinKey::\_\_construct</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\MinKey::\_\_construct</span> example**

``` php
<?php

var_dump(new MongoDB\BSON\MinKey());

?>
```

以上例程会输出：

    object(MongoDB\BSON\MinKey)#1 (0) {
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\MinKey::jsonSerialize
====================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\MinKey::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\MinKey</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\MinKey::serialize
================================

Serialize a MinKey

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\MinKey::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\MinKey</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\MinKey::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\MinKey::unserialize
==================================

Unserialize a MinKey

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\MinKey::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\MinKey</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\MinKey</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\MinKey::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for an
<a href="https://docs.mongodb.com/manual/reference/bson-types/#objectid" class="link external">» ObjectId</a>.
The value consists of 12 bytes, where the first four bytes are a
timestamp that reflect the ObjectId's creation. Specifically, the value
consists of:

-   <span class="simpara">a 4-byte value representing the seconds since
    the Unix epoch,</span>
-   <span class="simpara">a 5-byte random number unique to a machine and
    process, and</span>
-   <span class="simpara">a 3-byte counter, starting with a random
    value.</span>

In MongoDB, each document stored in a collection requires a unique
*\_id* field that acts as a primary key. If an inserted document omits
the *\_id* field, the driver automatically generates an ObjectId for the
*\_id* field.

Using ObjectIds for the *\_id* field provides the following additional
benefits:

-   <span class="simpara">The creation time of the ObjectId may be
    accessed using the <span
    class="methodname">MongoDB\\BSON\\ObjectId::getTimestamp</span>
    method.</span>
-   <span class="simpara">Sorting on an *\_id* field that stores
    ObjectId values is roughly equivalent to sorting by creation
    time.</span>

类摘要
------

**MongoDB\\BSON\\ObjectId**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\ObjectId** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\ObjectIdInterface</span>
</span> <span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$id`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.3.0</td>
<td><p>Renamed from <em>MongoDB\BSON\ObjectID</em> to <em>MongoDB\BSON\ObjectId</em>.</p>
<p>Implements <span class="interfacename">MongoDB\BSON\ObjectIdInterface</span>.</p></td>
</tr>
<tr class="even">
<td>1.2.0</td>
<td>Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>.</td>
</tr>
</tbody>
</table>

MongoDB\\BSON\\ObjectId::\_\_construct
======================================

Construct a new ObjectId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\ObjectId::\_\_construct</span>
(\[ <span class="methodparam"><span class="type">string</span>
`$id`</span> \] )

### 参数

`id` (<span class="type">string</span>)  
A 24-character hexadecimal string. If not provided, the driver will
generate an ObjectId.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `id` is not a 24-character hexadecimal string.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\ObjectId::\_\_construct</span> example**

``` php
<?php

var_dump(new MongoDB\BSON\ObjectId());

var_dump(new MongoDB\BSON\ObjectId('000000000000000000000001'));

?>
```

以上例程的输出类似于：

    object(MongoDB\BSON\ObjectId)#1 (1) {
      ["oid"]=>
      string(24) "56732d3dda14d81214634921"
    }
    object(MongoDB\BSON\ObjectId)#1 (1) {
      ["oid"]=>
      string(24) "000000000000000000000001"
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ObjectId Reference</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#objectid" class="link external">» BSON Types: ObjectId</a>

MongoDB\\BSON\\ObjectId::getTimestamp
=====================================

Returns the timestamp component of this ObjectId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\ObjectId::getTimestamp</span> ( <span
class="methodparam">void</span> )

The timestamp component of an ObjectId is its most significant 32 bits,
which denotes the number of seconds since the Unix epoch. This value is
read as an unsigned 32-bit integer with big-endian byte order.

> **Note**: <span class="simpara"> Because PHP's integer type is signed,
> some values returned by this method may appear as negative integers on
> 32-bit platforms. The *"%u"* formatter of <span
> class="function">sprintf</span> may be used to obtain a string
> representation of the unsigned decimal value. </span>

### 参数

此函数没有参数。

### 返回值

Returns the timestamp component of this ObjectId.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\ObjectId::getTimestamp</span> example**

``` php
<?php

var_dump((new MongoDB\BSON\ObjectId())->getTimestamp());

var_dump((new MongoDB\BSON\ObjectId('0000002a0000000000000000'))->getTimestamp());

?>
```

以上例程的输出类似于：

    integer(1484854719)
    integer(42)

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ObjectId Reference</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#objectid" class="link external">» BSON Types: ObjectId</a>

MongoDB\\BSON\\ObjectId::jsonSerialize
======================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\ObjectId::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\ObjectId</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\ObjectId::serialize
==================================

Serialize an ObjectId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\ObjectId::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\ObjectId</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\ObjectId::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\ObjectId::\_\_toString
=====================================

Returns the hexidecimal representation of this ObjectId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\ObjectId::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the hexidecimal representation of this ObjectId.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\ObjectId::\_\_toString</span> example**

``` php
<?php

var_dump((string) new MongoDB\BSON\ObjectId());
var_dump((string) new MongoDB\BSON\ObjectId('000000000000000000000001'));

?>
```

以上例程的输出类似于：

    string(24) "56731b49da14d8747d701211"
    string(24) "000000000000000000000001"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/object-id/" class="link external">» ObjectId Reference</a>
-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#objectid" class="link external">» BSON Types: ObjectId</a>

MongoDB\\BSON\\ObjectId::unserialize
====================================

Unserialize an ObjectId

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\ObjectId::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\ObjectId</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\ObjectId</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\ObjectId::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for a regular expression pattern and optional
<a href="https://docs.mongodb.com/manual/reference/operator/query/regex/#op._S_options" class="link external">» flags</a>.

> **Note**: <span class="simpara"> This BSON type is mainly used when
> querying the database. Alternatively, the
> <a href="https://docs.mongodb.com/manual/reference/operator/query/regex" class="link external">» $regex</a>
> query operator may be used. </span>

类摘要
------

**MongoDB\\BSON\\Regex**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Regex** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\RegexInterface</span> </span>
<span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$pattern`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$flags`<span class="initializer"> = ""</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getPattern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\RegexInterface</span>.                                        |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\Regex::\_\_construct
===================================

Construct a new Regex

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\Regex::\_\_construct</span> (
<span class="methodparam"><span class="type">string</span>
`$pattern`</span> \[, <span class="methodparam"><span
class="type">string</span> `$flags`<span class="initializer"> =
""</span></span> \] )

### 参数

`pattern` (<span class="type">string</span>)  
The regular expression pattern.

> **Note**: <span class="simpara"> The pattern should not be wrapped
> with delimiter characters. </span>

`flags` (<span class="type">string</span>)  
The
<a href="https://docs.mongodb.com/manual/reference/operator/query/regex/#op._S_options" class="link external">» regular expression flags</a>.
Characters in this argument will be sorted alphabetically.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if `pattern` or `flags` contain null bytes.

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1.2.0</td>
<td><p>The <code class="parameter">flags</code> argument is optional and defaults to an empty string.</p>
<p>Characters in the <code class="parameter">flags</code> argument will be sorted alphabetically when a Regex is constructed. Previously, the characters were stored in the order provided.</p>
<p><span class="classname">MongoDB\Driver\Exception\InvalidArgumentException</span> is thrown if <code class="parameter">pattern</code> or <code class="parameter">flags</code> contain null bytes. Previously, values would be truncated at the first null byte.</p></td>
</tr>
</tbody>
</table>

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Regex::\_\_construct</span> example**

``` php
<?php

$regex = new MongoDB\BSON\Regex('^foo', 'i');
var_dump($regex);

?>
```

以上例程会输出：

    object(MongoDB\BSON\Regex)#1 (2) {
      ["pattern"]=>
      string(4) "^foo"
      ["flags"]=>
      string(1) "i"
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>
-   <a href="https://docs.mongodb.com/manual/reference/operator/query/regex/#op._S_options" class="link external">» Supported regular expression flags</a>

MongoDB\\BSON\\Regex::getFlags
==============================

Returns the Regex's flags

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Regex::getFlags</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the Regex's flags.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span class="function">MongoDB\\BSON\\Regex::getFlags</span>
example**

``` php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump($regex->getFlags());

?>
```

以上例程的输出类似于：

    string(1) "i"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>
-   <a href="https://docs.mongodb.com/manual/reference/operator/query/regex/#op._S_options" class="link external">» Supported regular expression flags</a>

MongoDB\\BSON\\Regex::getPattern
================================

Returns the Regex's pattern

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Regex::getPattern</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the Regex's pattern.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Regex::getPattern</span> example**

``` php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump($regex->getPattern());

?>
```

以上例程的输出类似于：

    string(5) "regex"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Regex::jsonSerialize
===================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Regex::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Regex</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Regex::serialize
===============================

Serialize a Regex

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Regex::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Regex</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Regex::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Regex::\_\_toString
==================================

Returns the string representation of this Regex

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Regex::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this Regex.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Regex::\_\_toString</span> example**

``` php
<?php

$regex = new MongoDB\BSON\Regex('regex', 'i');
var_dump((string) $regex);

?>
```

以上例程会输出：

    string(8) "/regex/i"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Regex::unserialize
=================================

Unserialize a Regex

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Regex::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Regex</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Regex</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\Regex::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

Represents a
<a href="https://docs.mongodb.com/manual/reference/bson-types/#timestamps" class="link external">» BSON timestamp</a>,
The value consists of a 4-byte timestamp (i.e. seconds since the epoch)
and a 4-byte increment.

> **Note**: <span class="simpara"> This is an internal MongoDB type used
> for replication and sharding. It is not intended for general date
> storage (<span class="classname">MongoDB\\BSON\\UTCDateTime</span>
> should be used instead). </span>

类摘要
------

**MongoDB\\BSON\\Timestamp**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Timestamp** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\TimestampInterface</span> </span>
<span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$increment`</span> ,
<span class="methodparam"><span class="type">int</span>
`$timestamp`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getIncrement</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\TimestampInterface</span>.                                    |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\Timestamp::\_\_construct
=======================================

Construct a new Timestamp

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">MongoDB\\BSON\\Timestamp::\_\_construct</span>
( <span class="methodparam"><span class="type">int</span>
`$increment`</span> , <span class="methodparam"><span
class="type">int</span> `$timestamp`</span> )

### 参数

`increment` (<span class="type">integer</span>)  
32-bit integer denoting the incrementing ordinal for operations within a
given second.

`timestamp` (<span class="type">integer</span>)  
32-bit integer denoting seconds since the Unix epoch.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Timestamp::\_\_construct</span>
example**

``` php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);

?>
```

以上例程会输出：

    object(MongoDB\BSON\Timestamp)#1 (2) {
      ["increment"]=>
      int(1234)
      ["timestamp"]=>
      int(5678)
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#timestamps" class="link external">» BSON Types: Timestamps</a>

MongoDB\\BSON\\Timestamp::getIncrement
======================================

Returns the increment component of this Timestamp

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\Timestamp::getIncrement</span> ( <span
class="methodparam">void</span> )

The increment component of a Timestamp is its least significant 32 bits,
whichs denotes the incrementing ordinal for operations within a given
second. This value is read as an unsigned 32-bit integer with big-endian
byte order.

> **Note**: <span class="simpara"> Because PHP's integer type is signed,
> some values returned by this method may appear as negative integers on
> 32-bit platforms. The *"%u"* formatter of <span
> class="function">sprintf</span> may be used to obtain a string
> representation of the unsigned decimal value. </span>

### 参数

此函数没有参数。

### 返回值

Returns the increment component of this Timestamp.

**Warning**

On 32-bit systems this method may return a negative number. Although the
increment and timestamp parts of the BSON timestamp type consists of two
unsigned 32-bit values, PHP can not represent these on 32-bit platforms.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#timestamps" class="link external">» BSON Types: Timestamps</a>

MongoDB\\BSON\\Timestamp::getTimestamp
======================================

Returns the timestamp component of this Timestamp

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\Timestamp::getTimestamp</span> ( <span
class="methodparam">void</span> )

The timestamp component of a Timestamp is its most significant 32 bits,
which denotes the number of seconds since the Unix epoch. This value is
read as an unsigned 32-bit integer with big-endian byte order.

> **Note**: <span class="simpara"> Because PHP's integer type is signed,
> some values returned by this method may appear as negative integers on
> 32-bit platforms. The *"%u"* formatter of <span
> class="function">sprintf</span> may be used to obtain a string
> representation of the unsigned decimal value. </span>

### 参数

此函数没有参数。

### 返回值

Returns the timestamp component of this Timestamp.

**Warning**

On 32-bit systems this method may return a negative number. Although the
increment and timestamp parts of the BSON timestamp type consists of two
unsigned 32-bit values, PHP can not represent these on 32-bit platforms.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#timestamps" class="link external">» BSON Types: Timestamps</a>

MongoDB\\BSON\\Timestamp::jsonSerialize
=======================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Timestamp::jsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Timestamp</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Timestamp::serialize
===================================

Serialize a Timestamp

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Timestamp::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Timestamp</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Timestamp::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Timestamp::\_\_toString
======================================

Returns the string representation of this Timestamp

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Timestamp::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this Timestamp.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Timestamp::\_\_toString</span> example**

``` php
<?php

$timestamp = new MongoDB\BSON\Timestamp(1234, 5678);
var_dump((string) $timestamp);

?>
```

以上例程的输出类似于：

    string(11) "[1234:5678]"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#timestamps" class="link external">» BSON Types: Timestamps</a>

MongoDB\\BSON\\Timestamp::unserialize
=====================================

Unserialize a Timestamp

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Timestamp::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Timestamp</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Timestamp</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\Timestamp::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

Represents a
<a href="https://docs.mongodb.com/manual/reference/bson-types/#date" class="link external">» BSON date</a>.
The value is a 64-bit integer that represents the number of milliseconds
since the Unix epoch (Jan 1, 1970). Negative values represent dates
before 1970.

类摘要
------

**MongoDB\\BSON\\UTCDateTime**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\UTCDateTime** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\UTCDateTimeInterface</span> </span>
<span class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span
class="type">integer\|float\|string\|DateTimeInterface</span>
`$milliseconds`<span class="initializer"> = **`NULL`**</span></span> \]
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">DateTime</span> <span
class="methodname">toDateTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------|
| 1.3.0 | Implements <span class="interfacename">MongoDB\\BSON\\UTCDateTimeInterface</span>.                                  |
| 1.2.0 | Implements <span class="interfacename">Serializable</span> and <span class="interfacename">JsonSerializable</span>. |

MongoDB\\BSON\\UTCDateTime::\_\_construct
=========================================

Construct a new UTCDateTime

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span
class="methodname">MongoDB\\BSON\\UTCDateTime::\_\_construct</span> (\[
<span class="methodparam"><span
class="type">integer\|float\|string\|DateTimeInterface</span>
`$milliseconds`<span class="initializer"> = **`NULL`**</span></span> \]
)

### 参数

`milliseconds` (<span class="type">integer\|float\|string\|DateTimeInterface</span>)  
Number of milliseconds since the Unix epoch (Jan 1, 1970). Negative
values represent dates before 1970. This value may be provided as a
64-bit <span class="type">integer</span>. For compatibility on 32-bit
systems, this parameter may also be provided as a <span
class="type">float</span> or <span class="type">string</span>.

If the argument is a <span class="classname">DateTimeInterface</span>,
the number of milliseconds since the Unix epoch will be derived from
that value. Note that in versions of PHP versions before 7.1.0, <span
class="classname">DateTime</span> and <span
class="classname">DateTimeImmutable</span> objects constructed from the
current time
<a href="/migration71/incompatible.html#migration71.incompatible.datetime-microseconds" class="link">did not incorporate sub-second precision</a>.

If this argument is **`NULL`**, the current time will be used by
default.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                                                                                                                                                                              |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.0 | The `milliseconds` argument is optional and defaults to **`NULL`** (i.e. current time). The argument also accepts a <span class="classname">DateTimeInterface</span>, which may be used to derive the number of milliseconds since the Unix epoch. Previously, only <span class="type">integer</span>, <span class="type">float</span>, and <span class="type">string</span> types were accepted. |

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\UTCDateTime::\_\_construct</span>
example**

``` php
<?php

var_dump(new MongoDB\BSON\UTCDateTime);

var_dump(new MongoDB\BSON\UTCDateTime(new DateTime));

var_dump(new MongoDB\BSON\UTCDateTime(1416445411987));

?>
```

以上例程的输出类似于：

    object(MongoDB\BSON\UTCDateTime)#1 (1) {
      ["milliseconds"]=>
      string(13) "1484852905560"
    }
    object(MongoDB\BSON\UTCDateTime)#1 (1) {
      ["milliseconds"]=>
      string(13) "1484852905560"
    }
    object(MongoDB\BSON\UTCDateTime)#1 (1) {
      ["milliseconds"]=>
      string(13) "1416445411987"
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#date" class="link external">» BSON Types: Date</a>

MongoDB\\BSON\\UTCDateTime::jsonSerialize
=========================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTime::jsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\UTCDateTime</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\UTCDateTime::serialize
=====================================

Serialize a UTCDateTime

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTime::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\UTCDateTime</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\UTCDateTime::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\UTCDateTime::toDateTime
======================================

Returns the DateTime representation of this UTCDateTime

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">DateTime</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTime::toDateTime</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">DateTime</span> representation of
this UTCDateTime. The returned <span class="classname">DateTime</span>
will use the UTC time zone.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\UTCDatetime::toDateTime</span> example**

``` php
<?php

$utcdatetime = new MongoDB\BSON\UTCDateTime(1416445411987);
$datetime = $utcdatetime->toDateTime();
var_dump($datetime->format('r'));
var_dump($datetime->format('U.u'));
var_dump($datetime->getTimezone());

?>
```

以上例程的输出类似于：

    string(31) "Thu, 20 Nov 2014 01:03:31 +0000"
    string(17) "1416445411.987000"
    object(DateTimeZone)#3 (2) {
      ["timezone_type"]=>
      int(1)
      ["timezone"]=>
      string(6) "+00:00"
    }

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#date" class="link external">» BSON Types: Date</a>

MongoDB\\BSON\\UTCDateTime::\_\_toString
========================================

Returns the string representation of this UTCDateTime

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTime::\_\_toString</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this UTCDateTime.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\UTCDateTime::\_\_toString</span>
example**

``` php
<?php

$utcdatetime = new MongoDB\BSON\UTCDateTime(1416445411987);
var_dump((string) $utcdatetime);

?>
```

以上例程会输出：

    string(13) "1416445411987"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/#date" class="link external">» BSON Types: Date</a>

MongoDB\\BSON\\UTCDateTime::unserialize
=======================================

Unserialize a UTCDateTime

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTime::unserialize</span> (
<span class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span
class="classname">MongoDB\\BSON\\UTCDateTime</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\UTCDateTime</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\UTCDateTime::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

Abstract base interface that should not be implemented directly.

接口摘要
--------

**MongoDB\\BSON\\Type**

<span class="ooclass"> class **MongoDB\\BSON\\Type** </span> {

}

This interface has no methods. Its only purpose is to be the base
interface for all BSON type classes.

简介
----

Classes may implement this interface to take advantage of automatic ODM
(object document mapping) behavior in the driver. During serialization,
the driver will inject a <span class="property">\_\_pclass</span>
property containing the PHP class name into the data returned by <span
class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>.
During unserialization, the same <span
class="property">\_\_pclass</span> property will then be used to infer
the PHP class (independent of any
<a href="/set/mongodb.html#TypeMaps" class="link">type map</a>
configuration) to be constructed before <span
class="function">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
is invoked. See
<a href="/set/mongodb.html#Persisting%20Data" class="xref"></a> for
additional information.

> **Note**: <span class="simpara"> Even if <span
> class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
> would return a sequential array, injection of the <span
> class="property">\_\_pclass</span> property will cause the object to
> be serialized as a BSON document. </span>

接口摘要
--------

**MongoDB\\BSON\\Persistable**

<span class="ooclass"> class **MongoDB\\BSON\\Persistable** </span>
<span class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Unserializable</span> </span> <span
class="oointerface">, <span
class="interfacename">MongoDB\\BSON\\Serializable</span> </span> {

/\* 继承的方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array\|object</span>
<span
class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span> (
<span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
( <span class="methodparam"><span class="type">array</span>
`$data`</span> )

}

简介
----

Classes that implement this interface may return data to be serialized
as a BSON array or document in lieu of the object's public properties.

接口摘要
--------

**MongoDB\\BSON\\Serializable**

<span class="ooclass"> class **MongoDB\\BSON\\Serializable** </span>
<span class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array\|object</span>
<span class="methodname">bsonSerialize</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\Serializable::bsonSerialize
==========================================

Provides an array or document to serialize as BSON

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array\|object</span>
<span
class="methodname">MongoDB\\BSON\\Serializable::bsonSerialize</span> (
<span class="methodparam">void</span> )

Called during serialization of the object to BSON. The method must
return an <span class="type">array</span> or <span
class="classname">stdClass</span>.

Root documents (e.g. a <span
class="interfacename">MongoDB\\BSON\\Serializable</span> passed to <span
class="function">MongoDB\\BSON\\fromPHP</span>) will always be
serialized as a BSON document. For field values, associative arrays and
<span class="classname">stdClass</span> instances will be serialized as
a BSON document and sequential arrays (i.e. sequential, numeric indexes
starting at *0*) will be serialized as a BSON array.

Users are encouraged to include an <span class="property">\_id</span>
property (e.g. a <span class="classname">MongoDB\\BSON\\ObjectId</span>
initialized in your constructor) when returning data for a BSON root
document; otherwise, the driver or database will need to generate a
<span class="classname">MongoDB\\BSON\\ObjectId</span> when inserting or
upserting the document, respectively.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> or <span
class="classname">stdClass</span> to be serialized as a BSON array or
document.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
returning an associative array for root document**

``` php
<?php

class MyDocument implements MongoDB\BSON\Serializable
{
    private $id;

    function __construct()
    {
        $this->id = new MongoDB\BSON\ObjectId;
    }

    function bsonSerialize()
    {
        return ['_id' => $this->id, 'foo' => 'bar'];
    }
}

$bson = MongoDB\BSON\fromPHP(new MyDocument);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

以上例程的输出类似于：

    { "_id" : { "$oid" : "56cccdcada14d8755a58c591" }, "foo" : "bar" }

**示例 \#2 <span
class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
returning a sequential array for root document**

``` php
<?php

class MyArray implements MongoDB\BSON\Serializable
{
    function bsonSerialize()
    {
        return [1, 2, 3];
    }
}

$bson = MongoDB\BSON\fromPHP(new MyArray);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

以上例程会输出：

    { "0" : 1, "1" : 2, "2" : 3 }

**示例 \#3 <span
class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
returning an associative array for document field**

``` php
<?php

class MyDocument implements MongoDB\BSON\Serializable
{
    function bsonSerialize()
    {
        return ['foo' => 'bar'];
    }
}

$value = ['document' => new MyDocument];
$bson = MongoDB\BSON\fromPHP($value);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

以上例程会输出：

    { "document" : { "foo" : "bar" } }

**示例 \#4 <span
class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
returning a sequential array for document field**

``` php
<?php

class MyArray implements MongoDB\BSON\Serializable
{
    function bsonSerialize()
    {
        return [1, 2, 3];
    }
}

$value = ['array' => new MyArray];
$bson = MongoDB\BSON\fromPHP($value);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

以上例程会输出：

    { "array" : [ 1, 2, 3 ] }

### 参见

-   <span
    class="function">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
-   <span class="interfacename">MongoDB\\BSON\\Persistable</span>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

简介
----

Classes that implement this interface may be specified in a
<a href="/set/mongodb.html#TypeMaps" class="link">type map</a> for
unserializing BSON arrays and documents (both root and embedded).

接口摘要
--------

**MongoDB\\BSON\\Unserializable**

<span class="ooclass"> class **MongoDB\\BSON\\Unserializable** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">bsonUnserialize</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

}

MongoDB\\BSON\\Unserializable::bsonUnserialize
==============================================

Constructs the object from a BSON array or document

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
( <span class="methodparam"><span class="type">array</span>
`$data`</span> )

Called during unserialization of the object from BSON. The properties of
the BSON array or document will be passed to the method as an <span
class="type">array</span>.

Remember to check for an <span class="property">\_id</span> property
when handling data from a BSON document.

> **Note**: <span class="simpara"> This method acts as the
> <a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">constructor</a>
> of the object. The
> <a href="/language/oop5/decon.html#object.construct" class="link">__construct()</a>
> method will *not* be called after this method. </span>

### 参数

`data` (<span class="type">array</span>)  
Properties within the BSON array or document.

### 返回值

The return value from this method is ignored.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Unserializable::bsonUnserialize</span>
example**

``` php
<?php

class MyDocument implements MongoDB\BSON\Unserializable
{
    private $data = [];

    function bsonUnserialize(array $data)
    {
        $this->data = $data;
    }
}

$bson = MongoDB\BSON\fromJSON('{ "foo": "bar" }');
$value = MongoDB\BSON\toPHP($bson, ['root' => 'MyDocument']);
var_dump($value);

?>
```

以上例程会输出：

    object(MyDocument)#1 (1) {
      ["data":"MyDocument":private]=>
      array(1) {
        ["foo"]=>
        string(3) "bar"
      }
    }

### 参见

-   <span
    class="function">MongoDB\\BSON\\Serializable::bsonSerialize</span>
-   <span class="interfacename">MongoDB\\BSON\\Persistable</span>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\Binary</span> but may also be used for
type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\BinaryInterface**

<span class="ooclass"> class **MongoDB\\BSON\\BinaryInterface** </span>
{

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">getData</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\BinaryInterface::getData
=======================================

Returns the BinaryInterface's data

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\BinaryInterface::getData</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the BinaryInterface's data.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Binary::getData</span>

MongoDB\\BSON\\BinaryInterface::getType
=======================================

Returns the BinaryInterface's type

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\BinaryInterface::getType</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the BinaryInterface's type.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Binary::getType</span>

MongoDB\\BSON\\BinaryInterface::\_\_toString
============================================

Returns the BinaryInterface's data

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\BinaryInterface::\_\_toString</span> (
<span class="methodparam">void</span> )

此方法是该方法的别名： <span
class="methodname">MongoDB\\BSON\\BinaryInterface::getData</span>.

### 参数

此函数没有参数。

### 返回值

Returns the BinaryInterface's data.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\BinaryInterface::getData</span>
-   <span class="methodname">MongoDB\\BSON\\Binary::\_\_toString</span>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\Decimal128</span> but may also be used
for type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\Decimal128Interface**

<span class="ooclass"> class **MongoDB\\BSON\\Decimal128Interface**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\Decimal128Interface::\_\_toString
================================================

Returns the string representation of this Decimal128Interface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Decimal128Interface::\_\_toString</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this Decimal128Interface.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Decimal128::\_\_toString</span>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\Javascript</span> but may also be used
for type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\JavascriptInterface**

<span class="ooclass"> class **MongoDB\\BSON\\JavascriptInterface**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">object\|null</span>
<span class="methodname">getScope</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\JavascriptInterface::getCode
===========================================

Returns the JavascriptInterface's code

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\JavascriptInterface::getCode</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the JavascriptInterface's code.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Javascript::getCode</span>

MongoDB\\BSON\\JavascriptInterface::getScope
============================================

Returns the JavascriptInterface's scope document

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">object\|null</span>
<span
class="methodname">MongoDB\\BSON\\JavascriptInterface::getScope</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the JavascriptInterface's scope document.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Javascript::getScope</span>

MongoDB\\BSON\\JavascriptInterface::\_\_toString
================================================

Returns the JavascriptInterface's code

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\JavascriptInterface::\_\_toString</span>
( <span class="methodparam">void</span> )

此方法是该方法的别名： <span
class="methodname">MongoDB\\BSON\\JavascriptInterface::getCode</span>.

### 参数

此函数没有参数。

### 返回值

Returns the JavascriptInterface's code.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\JavascriptInterface::getCode</span>
-   <span
    class="methodname">MongoDB\\BSON\\Javascript::\_\_toString</span>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\MaxKey</span> but may also be used for
type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\MaxKeyInterface**

<span class="ooclass"> class **MongoDB\\BSON\\MaxKeyInterface** </span>
{

}

This interface has no methods.

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\MinKey</span> but may also be used for
type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\MinKeyInterface**

<span class="ooclass"> class **MongoDB\\BSON\\MinKeyInterface** </span>
{

}

This interface has no methods.

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\ObjectId</span> but may also be used
for type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\ObjectIdInterface**

<span class="ooclass"> class **MongoDB\\BSON\\ObjectIdInterface**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\ObjectIdInterface::getTimestamp
==============================================

Returns the timestamp component of this ObjectIdInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\ObjectIdInterface::getTimestamp</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the timestamp component of this ObjectIdInterface.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\ObjectId::getTimestamp</span>

MongoDB\\BSON\\ObjectIdInterface::\_\_toString
==============================================

Returns the hexidecimal representation of this ObjectIdInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\ObjectIdInterface::\_\_toString</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the hexidecimal representation of this ObjectIdInterface.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\ObjectId::\_\_toString</span>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\Regex</span> but may also be used for
type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\RegexInterface**

<span class="ooclass"> class **MongoDB\\BSON\\RegexInterface** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">getFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">getPattern</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\RegexInterface::getFlags
=======================================

Returns the RegexInterface's flags

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\RegexInterface::getFlags</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the RegexInterface's flags.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Regex::getFlags</span>

MongoDB\\BSON\\RegexInterface::getPattern
=========================================

Returns the RegexInterface's pattern

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\RegexInterface::getPattern</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the RegexInterface's pattern.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Regex::getPattern</span>

MongoDB\\BSON\\RegexInterface::\_\_toString
===========================================

Returns the string representation of this RegexInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\RegexInterface::\_\_toString</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this RegexInterface.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Regex::\_\_toString</span>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\Timestamp</span> but may also be used
for type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\TimestampInterface**

<span class="ooclass"> class **MongoDB\\BSON\\TimestampInterface**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getIncrement</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getTimestamp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\TimestampInterface::getIncrement
===============================================

Returns the increment component of this TimestampInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\TimestampInterface::getIncrement</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the increment component of this TimestampInterface.

**Warning**

On 32-bit systems this method may return a negative number. Although the
increment and timestamp parts of the BSON timestamp type consists of two
unsigned 32-bit values, PHP can not represent these on 32-bit platforms.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Timestamp::getIncrement</span>

MongoDB\\BSON\\TimestampInterface::getTimestamp
===============================================

Returns the timestamp component of this TimestampInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">MongoDB\\BSON\\TimestampInterface::getTimestamp</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the timestamp component of this TimestampInterface.

**Warning**

On 32-bit systems this method may return a negative number. Although the
increment and timestamp parts of the BSON timestamp type consists of two
unsigned 32-bit values, PHP can not represent these on 32-bit platforms.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Timestamp::getTimestamp</span>

MongoDB\\BSON\\TimestampInterface::\_\_toString
===============================================

Returns the string representation of this TimestampInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\TimestampInterface::\_\_toString</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this TimestampInterface.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Timestamp::\_\_toString</span>

简介
----

This interface is implemented by <span
class="classname">MongoDB\\BSON\\UTCDateTime</span> but may also be used
for type-hinting and userland classes.

类摘要
------

**MongoDB\\BSON\\UTCDateTimeInterface**

<span class="ooclass"> class **MongoDB\\BSON\\UTCDateTimeInterface**
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">DateTime</span> <span
class="methodname">toDateTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\BSON\\UTCDateTimeInterface::toDateTime
===============================================

Returns the DateTime representation of this UTCDateTimeInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">DateTime</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTimeInterface::toDateTime</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">DateTime</span> representation of
this UTCDateTimeInterface. The returned <span
class="classname">DateTime</span> should use the UTC time zone.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\UTCDateTime::toDateTime</span>

MongoDB\\BSON\\UTCDateTimeInterface::\_\_toString
=================================================

Returns the string representation of this UTCDateTimeInterface

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\UTCDateTimeInterface::\_\_toString</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this UTCDateTimeInterface.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\UTCDateTime::\_\_toString</span>

简介
----

BSON type for the "DBPointer" type. This BSON type is deprecated, and
this class can not be instantiated. It will be created from a BSON
DBPointer type while converting BSON to PHP, and can also be converted
back into BSON while storing documents in the database.

类摘要
------

**MongoDB\\BSON\\DBPointer**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\DBPointer** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

MongoDB\\BSON\\DBPointer::\_\_construct
=======================================

Construct a new DBPointer (unused)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\BSON\\DBPointer::\_\_construct</span> (
<span class="methodparam">void</span> )

<span class="classname">MongoDB\\BSON\\DBPointer</span> objects are
created through conversion from a deprecated BSON type and cannot be
constructed directly.

### 参数

此函数没有参数。

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\DBPointer::jsonSerialize
=======================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\DBPointer::jsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\DBPointer</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\DBPointer::serialize
===================================

Serialize a DBPointer

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\DBPointer::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\DBPointer</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\DBPointer::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\DBPointer::\_\_toString
======================================

Returns an empty string

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\DBPointer::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an empty string.

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\DBPointer::unserialize
=====================================

Unserialize a DBPointer

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\DBPointer::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\DBPointer</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\DBPointer</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\DBPointer::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for a 64-bit integer. This class cannot be instantiated and is
only created during BSON decoding when a 64-bit integer cannot be
represented as a PHP integer on a 32-bit platform. Versions of the
driver before 1.5.0 would throw an exception when attempting to decode a
64-bit integer on a 32-bit platform.

During BSON encoding, objects of this class will convert back to a
64-bit integer type. This allows 64-bit integers to be roundtripped
through a 32-bit PHP environment without any loss of precision. The
<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
method allows the 64-bit integer value to be accessed as a string.

> **Note**: <span class="simpara"> This class exists purely for 32-bit
> platforms. Applications on 64-bit platforms (i.e.
> <a href="/reserved/constants.html#constant.php-int-size" class="link"><strong><code>PHP_INT_SIZE</code></strong></a>
> is 8) should never encounter this class during normal operation.
> </span>

类摘要
------

**MongoDB\\BSON\\Int64**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Int64** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

MongoDB\\BSON\\Int64::\_\_construct
===================================

Construct a new Int64 (unused)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\BSON\\Int64::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="classname">MongoDB\\BSON\\Int64</span> objects are created
through conversion from a 64-bit integer BSON type on a 32-bit platform
and cannot be constructed directly.

### 参数

此函数没有参数。

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Int64::jsonSerialize
===================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Int64::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Int64</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
> function, which uses the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON format. This differs from other BSON classes, which use
> the driver-specific legacy extended JSON format (<span
> class="function">MongoDB\\BSON\\toJSON</span>), in order to ensure
> that the 64-bit integer value is correctly represented on 32-bit
> platforms. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Int64::serialize
===============================

Serialize an Int64

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Int64::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Int64</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Int64::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Int64::\_\_toString
==================================

Returns the string representation of this Int64

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Int64::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this Int64.

### 范例

**示例 \#1 <span
class="function">MongoDB\\BSON\\Int64::\_\_toString</span> example**

``` php
<?php

$int64 = unserialize('C:18:"MongoDB\BSON\Int64":47:{a:1:{s:7:"integer";s:19:"9223372036854775807";}}');

var_dump((string) $int64);

?>
```

以上例程的输出类似于：

    string(19) "9223372036854775807"

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Int64::unserialize
=================================

Unserialize an Int64

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Int64::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Int64</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Int64</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\UnexpectedValueException</span>
    if the properties cannot be unserialized (i.e. `serialized` was
    malformed).
-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    if the properties are invalid (e.g. missing fields or invalid
    values).

### 参见

-   <span class="methodname">MongoDB\\BSON\\Int64::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for the "Symbol" type. This BSON type is deprecated, and this
class can not be instantiated. It will be created from a BSON symbol
type while converting BSON to PHP, and can also be converted back into
BSON while storing documents in the database.

类摘要
------

**MongoDB\\BSON\\Symbol**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Symbol** </span> <span class="oointerface">implements
<span class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

MongoDB\\BSON\\Symbol::\_\_construct
====================================

Construct a new Symbol (unused)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\BSON\\Symbol::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="classname">MongoDB\\BSON\\Symbol</span> objects are created
through conversion from a deprecated BSON type and cannot be constructed
directly.

### 参数

此函数没有参数。

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Symbol::jsonSerialize
====================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Symbol::jsonSerialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Symbol</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Symbol::serialize
================================

Serialize a Symbol

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Symbol::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Symbol</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Symbol::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Symbol::\_\_toString
===================================

Returns the Symbol as a string

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Symbol::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the string representation of this Symbol.

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Symbol::unserialize
==================================

Unserialize a Symbol

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Symbol::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Symbol</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Symbol</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Symbol::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

简介
----

BSON type for the "Undefined" type. This BSON type is deprecated, and
this class can not be instantiated. It will be created from a BSON
undefined type while converting BSON to PHP, and can also be converted
back into BSON while storing documents in the database.

类摘要
------

**MongoDB\\BSON\\Undefined**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\BSON\\Undefined** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\BSON\\Type</span> </span> <span
class="oointerface">, <span class="interfacename">Serializable</span>
</span> <span class="oointerface">, <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">unserialize</span> ( <span class="methodparam"><span
class="type">string</span> `$serialized`</span> )

}

MongoDB\\BSON\\Undefined::\_\_construct
=======================================

Construct a new Undefined (unused)

### 说明

<span class="modifier">final</span> <span
class="modifier">private</span> <span
class="methodname">MongoDB\\BSON\\Undefined::\_\_construct</span> (
<span class="methodparam">void</span> )

<span class="classname">MongoDB\\BSON\\Undefined</span> objects are
created through conversion from a deprecated BSON type and cannot be
constructed directly.

### 参数

此函数没有参数。

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Undefined::jsonSerialize
=======================================

Returns a representation that can be converted to JSON

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">MongoDB\\BSON\\Undefined::jsonSerialize</span> (
<span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns data which can be serialized by <span
class="function">json\_encode</span> to produce an extended JSON
representation of the <span
class="classname">MongoDB\\BSON\\Undefined</span>.

> **Note**: <span class="simpara"> The output is consistent with the
> <span class="function">MongoDB\\BSON\\toJSON</span> function, which
> uses the driver-specific legacy extended JSON format. This does not
> necessarily match the
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#relaxed-extended-json-example" class="link external">» relaxed</a>
> or
> <a href="https://github.com/mongodb/specifications/blob/master/source/extended-json.rst#canonical-extended-json-example" class="link external">» canonical</a>
> extended JSON representations used by <span
> class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span> and <span
> class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>,
> respectively. </span>

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">JsonSerializable::jsonSerialize</span>
-   <span class="function">json\_encode</span>
-   <span class="function">MongoDB\\BSON\\toCanonicalExtendedJSON</span>
-   <span class="function">MongoDB\\BSON\\toRelaxedExtendedJSON</span>
-   <a href="https://docs.mongodb.com/manual/reference/mongodb-extended-json/" class="link external">» MongoDB Extended JSON</a>

MongoDB\\BSON\\Undefined::serialize
===================================

Serialize a Undefined

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Undefined::serialize</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the serialized representation of the <span
class="classname">MongoDB\\BSON\\Undefined</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\BSON\\Undefined::unserialize</span>
-   <span class="function">serialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

MongoDB\\BSON\\Undefined::\_\_toString
======================================

Returns an empty string

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\BSON\\Undefined::\_\_toString</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an empty string.

### 参见

-   <a href="https://docs.mongodb.com/manual/reference/bson-types/" class="link external">» BSON Types</a>

MongoDB\\BSON\\Undefined::unserialize
=====================================

Unserialize a Undefined

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">void</span> <span
class="methodname">MongoDB\\BSON\\Undefined::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

### 参数

`serialized`  
The serialized <span class="classname">MongoDB\\BSON\\Undefined</span>.

### 返回值

Returns the unserialized <span
class="classname">MongoDB\\BSON\\Undefined</span>.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span class="methodname">MongoDB\\BSON\\Undefined::serialize</span>
-   <span class="function">unserialize</span>
-   <a href="/language/oop5/serialization.html" class="link">Serializing Objects</a>

Monitoring classes and subscriber functions
===========================================

**目录**

-   [函数](/set/mongodb.html#函数)
    -   [MongoDB\\Driver\\Monitoring\\addSubscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\addSubscriber)
        — Registers a new monitoring event subscriber
    -   [MongoDB\\Driver\\Monitoring\\removeSubscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\removeSubscriber)
        — Unregisters an existing monitoring event subscriber
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent)
    — The MongoDB\\Driver\\Monitoring\\CommandFailedEvent class
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getCommandName)
        — Returns the command name
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getDurationMicros)
        — Returns the command's duration in microseconds
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getError)
        — Returns the Exception associated with the failed command
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getOperationId)
        — Returns the command's operation ID
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getReply)
        — Returns the command reply document
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getRequestId)
        — Returns the command's request ID
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandFailedEvent::getServer)
        — Returns the Server on which the command was executed
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent)
    — The MongoDB\\Driver\\Monitoring\\CommandStartedEvent class
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent::getCommand)
        — Returns the command document
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent::getCommandName)
        — Returns the command name
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent::getDatabaseName)
        — Returns the database on which the command was executed
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent::getOperationId)
        — Returns the command's operation ID
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent::getRequestId)
        — Returns the command's request ID
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandStartedEvent::getServer)
        — Returns the Server on which the command was executed
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent)
    — The MongoDB\\Driver\\Monitoring\\CommandSucceededEvent class
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent::getCommandName)
        — Returns the command name
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent::getDurationMicros)
        — Returns the command's duration in microseconds
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent::getOperationId)
        — Returns the command's operation ID
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent::getReply)
        — Returns the command reply document
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent::getRequestId)
        — Returns the command's request ID
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSucceededEvent::getServer)
        — Returns the Server on which the command was executed
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSubscriber)
    — The MongoDB\\Driver\\Monitoring\\CommandSubscriber interface
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSubscriber::commandFailed)
        — Notification method for a failed command
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSubscriber::commandStarted)
        — Notification method for a started command
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded](/set/mongodb.html#MongoDB\Driver\Monitoring\CommandSubscriber::commandSucceeded)
        — Notification method for a successful command
-   [MongoDB\\Driver\\Monitoring\\Subscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\Subscriber)
    — The MongoDB\\Driver\\Monitoring\\Subscriber interface

MongoDB\\Driver\\Monitoring\\addSubscriber
==========================================

Registers a new monitoring event subscriber

### 说明

<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\addSubscriber</span> (
<span class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\Subscriber</span>
`$subscriber`</span> )

Registers a new monitoring event subscriber with the driver. Registered
subscribers will be notified of monitoring events through specific
methods.

> **Note**: <span class="simpara"> If the object is already registered,
> this function is a no-op. </span>

### 参数

`subscriber` (<span class="type">MongoDB\\Driver\\Monitoring\\Subscriber</span>)  
A monitoring event subscriber object to register.

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="interfacename">MongoDB\\Driver\\Monitoring\\Subscriber</span>
-   <span
    class="interfacename">MongoDB\\Driver\\Monitoring\\CommandSubscriber</span>
-   <span
    class="function">MongoDB\\Driver\\Monitoring\\removeSubscriber</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\removeSubscriber
=============================================

Unregisters an existing monitoring event subscriber

### 说明

<span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\removeSubscriber</span>
( <span class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\Subscriber</span>
`$subscriber`</span> )

Unregisters an existing monitoring event subscriber from the driver.
Unregistered subscribers will no longer be notified of monitoring
events.

> **Note**: <span class="simpara"> If the object is not registered, this
> function is a no-op. </span>

### 参数

`subscriber` (<span class="type">MongoDB\\Driver\\Monitoring\\Subscriber</span>)  
A monitoring event subscriber object to unregister.

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="interfacename">MongoDB\\Driver\\Monitoring\\Subscriber</span>
-   <span
    class="interfacename">MongoDB\\Driver\\Monitoring\\CommandSubscriber</span>
-   <span
    class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

**目录**

-   [MongoDB\\Driver\\Monitoring\\addSubscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\addSubscriber)
    — Registers a new monitoring event subscriber
-   [MongoDB\\Driver\\Monitoring\\removeSubscriber](/set/mongodb.html#MongoDB\Driver\Monitoring\removeSubscriber)
    — Unregisters an existing monitoring event subscriber

简介
----

The <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>
class encapsulates information about a failed command.

类摘要
------

**MongoDB\\Driver\\Monitoring\\CommandFailedEvent**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Monitoring\\CommandFailedEvent** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getCommandName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getDurationMicros</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Exception</span> <span
class="methodname">getError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getOperationId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">getReply</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getRequestId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">getServer</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName
===============================================================

Returns the command name

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName</span>
( <span class="methodparam">void</span> )

Returns the command name (e.g. *"find"*, *"aggregate"*).

### 参数

此函数没有参数。

### 返回值

Returns the command name.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros
==================================================================

Returns the command's duration in microseconds

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros</span>
( <span class="methodparam">void</span> )

The command's duration is a calculated value that includes the time to
send the message and receive the reply from the server.

### 参数

此函数没有参数。

### 返回值

Returns the command's duration in microseconds.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError
=========================================================

Returns the Exception associated with the failed command

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Exception</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">Exception</span> associated with the
failed command.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId
===============================================================

Returns the command's operation ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId</span>
( <span class="methodparam">void</span> )

The operation ID is generated by the driver and may be used to link
events together such as bulk write operations, which may have been split
across several commands at the protocol level.

> **Note**: <span class="simpara"> Since multiple commands may share the
> same operation ID, it is not reliable to use this value to associate
> event objects with each other. The request ID returned by <span
> class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId</span>
> should be used instead. </span>

### 参数

此函数没有参数。

### 返回值

Returns the command's operation ID.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId</span>
-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply
=========================================================

Returns the command reply document

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply</span>
( <span class="methodparam">void</span> )

The reply document will be converted from BSON to PHP using the default
<a href="/set/mongodb.html#Deserialization%20from%20BSON" class="link">deserialization</a>
rules (e.g. BSON documents will be converted to <span
class="type">stdClass</span>).

### 参数

此函数没有参数。

### 返回值

Returns the command reply document as a <span
class="classname">stdClass</span> object.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId
=============================================================

Returns the command's request ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId</span>
( <span class="methodparam">void</span> )

The request ID is generated by the driver and may be used to associate
this <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>
with a previous <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>.

### 参数

此函数没有参数。

### 返回值

Returns the command's request ID.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer
==========================================================

Returns the Server on which the command was executed

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer</span>
( <span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\Server</span> on
which the command was executed.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">MongoDB\\Driver\\Server</span> on
which the command was executed.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

简介
----

The <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>
class encapsulates information about a started command.

类摘要
------

**MongoDB\\Driver\\Monitoring\\CommandStartedEvent**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Monitoring\\CommandStartedEvent** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">getCommand</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getCommandName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getDatabaseName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getOperationId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getRequestId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">getServer</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand
============================================================

Returns the command document

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand</span>
( <span class="methodparam">void</span> )

The reply document will be converted from BSON to PHP using the default
<a href="/set/mongodb.html#Deserialization%20from%20BSON" class="link">deserialization</a>
rules (e.g. BSON documents will be converted to <span
class="type">stdClass</span>).

### 参数

此函数没有参数。

### 返回值

Returns the command document as a <span
class="classname">stdClass</span> object.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName
================================================================

Returns the command name

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName</span>
( <span class="methodparam">void</span> )

Returns the command name (e.g. *"find"*, *"aggregate"*).

### 参数

此函数没有参数。

### 返回值

Returns the command name.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName
=================================================================

Returns the database on which the command was executed

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName</span>
( <span class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the database on which the command was executed.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId
================================================================

Returns the command's operation ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId</span>
( <span class="methodparam">void</span> )

The operation ID is generated by the driver and may be used to link
events together such as bulk write operations, which may have been split
across several commands at the protocol level.

> **Note**: <span class="simpara"> Since multiple commands may share the
> same operation ID, it is not reliable to use this value to associate
> event objects with each other. The request ID returned by <span
> class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId</span>
> should be used instead. </span>

### 参数

此函数没有参数。

### 返回值

Returns the command's operation ID.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId</span>
-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId</span>
-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId
==============================================================

Returns the command's request ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId</span>
( <span class="methodparam">void</span> )

The request ID is generated by the driver and may be used to associate
this <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>
with a later <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>
or <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>.

### 参数

此函数没有参数。

### 返回值

Returns the command's request ID.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId</span>
-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer
===========================================================

Returns the Server on which the command was executed

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer</span>
( <span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\Server</span> on
which the command was executed.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">MongoDB\\Driver\\Server</span> on
which the command was executed.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer</span>
-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

简介
----

The <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>
class encapsulates information about a successful command.

类摘要
------

**MongoDB\\Driver\\Monitoring\\CommandSucceededEvent**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Monitoring\\CommandSucceededEvent** </span> {

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getCommandName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getDurationMicros</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getOperationId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">getReply</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getRequestId</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">getServer</span> ( <span
class="methodparam">void</span> )

}

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName
==================================================================

Returns the command name

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName</span>
( <span class="methodparam">void</span> )

Returns the command name (e.g. *"find"*, *"aggregate"*).

### 参数

此函数没有参数。

### 返回值

Returns the command name.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros
=====================================================================

Returns the command's duration in microseconds

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros</span>
( <span class="methodparam">void</span> )

The command's duration is a calculated value that includes the time to
send the message and receive the reply from the server.

### 参数

此函数没有参数。

### 返回值

Returns the command's duration in microseconds.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId
==================================================================

Returns the command's operation ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId</span>
( <span class="methodparam">void</span> )

The operation ID is generated by the driver and may be used to link
events together such as bulk write operations, which may have been split
across several commands at the protocol level.

> **Note**: <span class="simpara"> Since multiple commands may share the
> same operation ID, it is not reliable to use this value to associate
> event objects with each other. The request ID returned by <span
> class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId</span>
> should be used instead. </span>

### 参数

此函数没有参数。

### 返回值

Returns the command's operation ID.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId</span>
-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply
============================================================

Returns the command reply document

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">object</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply</span>
( <span class="methodparam">void</span> )

The reply document will be converted from BSON to PHP using the default
<a href="/set/mongodb.html#Deserialization%20from%20BSON" class="link">deserialization</a>
rules (e.g. BSON documents will be converted to <span
class="type">stdClass</span>).

### 参数

此函数没有参数。

### 返回值

Returns the command reply document as a <span
class="classname">stdClass</span> object.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>
-   <a href="/set/mongodb.html#Persisting%20Data" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId
================================================================

Returns the command's request ID

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId</span>
( <span class="methodparam">void</span> )

The request ID is generated by the driver and may be used to associate
this <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>
with a previous <span
class="classname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>.

### 参数

此函数没有参数。

### 返回值

Returns the command's request ID.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer
=============================================================

Returns the Server on which the command was executed

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\Server</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer</span>
( <span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\Server</span> on
which the command was executed.

### 参数

此函数没有参数。

### 返回值

Returns the <span class="classname">MongoDB\\Driver\\Server</span> on
which the command was executed.

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="methodname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer</span>
-   <span class="methodname">MongoDB\\Driver\\Cursor::getServer</span>
-   <span
    class="methodname">MongoDB\\Driver\\WriteResult::getServer</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

简介
----

Classes may implement this interface to register an event subscriber
that is notified for each started, successful, and failed command event.
See
<a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>
for additional information.

接口摘要
--------

**MongoDB\\Driver\\Monitoring\\CommandSubscriber**

<span class="ooclass"> class
**MongoDB\\Driver\\Monitoring\\CommandSubscriber** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Monitoring\\Subscriber</span>
</span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">commandFailed</span> ( <span
class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>
`$event`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">commandStarted</span> ( <span
class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>
`$event`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">commandSucceeded</span> ( <span
class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>
`$event`</span> )

}

MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed
=============================================================

Notification method for a failed command

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed</span>
( <span class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>
`$event`</span> )

If the subscriber has been registered with <span
class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>, the
driver will call this method when a command has failed.

### 参数

`event` (<span class="type">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>)  
An event object encapsulating information about the failed command.

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="classname">MongoDB\\Driver\\Monitoring\\CommandFailedEvent</span>
-   <span
    class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted
==============================================================

Notification method for a started command

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted</span>
( <span class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>
`$event`</span> )

If the subscriber has been registered with <span
class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>, the
driver will call this method when a command has started.

### 参数

`event` (<span class="type">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>)  
An event object encapsulating information about the started command.

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="classname">MongoDB\\Driver\\Monitoring\\CommandStartedEvent</span>
-   <span
    class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded
================================================================

Notification method for a successful command

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded</span>
( <span class="methodparam"><span
class="type">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>
`$event`</span> )

If the subscriber has been registered with <span
class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>, the
driver will call this method when a command has succeeded.

### 参数

`event` (<span class="type">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>)  
An event object encapsulating information about the successful command.

### 返回值

没有返回值。

### 错误／异常

-   Throws <span
    class="classname">MongoDB\\Driver\\Exception\\InvalidArgumentException</span>
    on argument parsing errors.

### 参见

-   <span
    class="classname">MongoDB\\Driver\\Monitoring\\CommandSucceededEvent</span>
-   <span
    class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>
-   <a href="/set/mongodb.html#Application%20Performance%20Monitoring%20(APM)" class="xref"></a>

简介
----

Base interface for event subscribers. This is used for type-hinting
<span class="function">MongoDB\\Driver\\Monitoring\\addSubscriber</span>
and <span
class="function">MongoDB\\Driver\\Monitoring\\removeSubscriber</span>
and should not be implemented directly.

接口摘要
--------

**MongoDB\\Driver\\Monitoring\\Subscriber**

<span class="ooclass"> class **MongoDB\\Driver\\Monitoring\\Subscriber**
</span> {

}

This interface has no methods. Its only purpose is to be the base
interface for all event subscribers.

Exception 类
============

**目录**

-   [MongoDB\\Driver\\Exception\\AuthenticationException](/set/mongodb.html#MongoDB\Driver\Exception\AuthenticationException)
    — The MongoDB\\Driver\\Exception\\AuthenticationException class
-   [MongoDB\\Driver\\Exception\\BulkWriteException](/set/mongodb.html#MongoDB\Driver\Exception\BulkWriteException)
    — The MongoDB\\Driver\\Exception\\BulkWriteException class
-   [MongoDB\\Driver\\Exception\\ConnectionException](/set/mongodb.html#MongoDB\Driver\Exception\ConnectionException)
    — The MongoDB\\Driver\\Exception\\ConnectionException class
-   [MongoDB\\Driver\\Exception\\ConnectionTimeoutException](/set/mongodb.html#MongoDB\Driver\Exception\ConnectionTimeoutException)
    — The MongoDB\\Driver\\Exception\\ConnectionTimeoutException class
-   [MongoDB\\Driver\\Exception\\Exception](/set/mongodb.html#MongoDB\Driver\Exception\Exception)
    — The MongoDB\\Driver\\Exception\\Exception interface
-   [MongoDB\\Driver\\Exception\\ExecutionTimeoutException](/set/mongodb.html#MongoDB\Driver\Exception\ExecutionTimeoutException)
    — The MongoDB\\Driver\\Exception\\ExecutionTimeoutException class
-   [MongoDB\\Driver\\Exception\\InvalidArgumentException](/set/mongodb.html#MongoDB\Driver\Exception\InvalidArgumentException)
    — The MongoDB\\Driver\\Exception\\InvalidArgumentException class
-   [MongoDB\\Driver\\Exception\\LogicException](/set/mongodb.html#MongoDB\Driver\Exception\LogicException)
    — The MongoDB\\Driver\\Exception\\LogicException class
-   [MongoDB\\Driver\\Exception\\RuntimeException](/set/mongodb.html#MongoDB\Driver\Exception\RuntimeException)
    — The MongoDB\\Driver\\Exception\\RuntimeException class
    -   [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel](/set/mongodb.html#MongoDB\Driver\Exception\RuntimeException::hasErrorLabel)
        — Returns whether an error label is associated with an exception
-   [MongoDB\\Driver\\Exception\\SSLConnectionException](/set/mongodb.html#MongoDB\Driver\Exception\SSLConnectionException)
    — The MongoDB\\Driver\\Exception\\SSLConnectionException class
    (deprecated)
-   [MongoDB\\Driver\\Exception\\UnexpectedValueException](/set/mongodb.html#MongoDB\Driver\Exception\UnexpectedValueException)
    — The MongoDB\\Driver\\Exception\\UnexpectedValueException class
-   [MongoDB\\Driver\\Exception\\WriteException](/set/mongodb.html#MongoDB\Driver\Exception\WriteException)
    — The MongoDB\\Driver\\Exception\\WriteException class
    -   [MongoDB\\Driver\\Exception\\WriteException::getWriteResult](/set/mongodb.html#MongoDB\Driver\Exception\WriteException::getWriteResult)
        — Returns the WriteResult for the failed write operation

简介
----

Thrown when the driver fails to authenticate with the server.

类摘要
------

**MongoDB\\Driver\\Exception\\AuthenticationException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\AuthenticationException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\ConnectionException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Thrown when a bulk write operation fails.

类摘要
------

**MongoDB\\Driver\\Exception\\BulkWriteException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\BulkWriteException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\WriteException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">MongoDB\\Driver\\WriteResult</span> `$writeResult` ;

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">MongoDB\\Driver\\Exception\\WriteException::getWriteResult</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Base class for exceptions thrown when the driver fails to establish a
database connection.

类摘要
------

**MongoDB\\Driver\\Exception\\ConnectionException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\ConnectionException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\RuntimeException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Thrown when the driver fails to establish a database connection within a
specified time limit
(<a href="/set/mongodb.html#uriOptions" class="link">connectTimeoutMS</a>)
or server selection fails
(<a href="/set/mongodb.html#uriOptions" class="link">serverSelectionTimeoutMS</a>).

类摘要
------

**MongoDB\\Driver\\Exception\\ConnectionTimeoutException**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Exception\\ConnectionTimeoutException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\ConnectionException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Common interface for all driver exceptions. This may be used to catch
only exceptions originating from the driver itself.

类摘要
------

**MongoDB\\Driver\\Exception\\Exception**

<span class="ooclass"> class **MongoDB\\Driver\\Exception\\Exception**
</span> {

}

简介
----

Thrown when a query or command fails to complete within a specified time
limit (e.g.
<a href="https://docs.mongodb.com/manual/tutorial/terminate-running-operations/#maxtimems" class="link external">» maxTimeMS</a>).

类摘要
------

**MongoDB\\Driver\\Exception\\ExecutionTimeoutException**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Exception\\ExecutionTimeoutException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\ServerException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

更新日志
--------

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.5.0 | This class now extends <span class="classname">MongoDB\\Driver\\Exception\\ServerException</span> instead of <span class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>. |

简介
----

Thrown when a driver method is given invalid arguments (e.g. invalid
option types).

类摘要
------

**MongoDB\\Driver\\Exception\\InvalidArgumentException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\InvalidArgumentException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**InvalidArgumentException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Thrown when the driver is incorrectly used (e.g. rewinding a cursor).

类摘要
------

**MongoDB\\Driver\\Exception\\LogicException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\LogicException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**LogicException** </span> <span class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Thrown when the driver encounters a runtime error (e.g. internal error
from
<a href="https://github.com/mongodb/mongo-c-driver" class="link external">» libmongoc</a>).

类摘要
------

**MongoDB\\Driver\\Exception\\RuntimeException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\RuntimeException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**RuntimeException** </span> <span class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">hasErrorLabel</span> ( <span
class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`errorLabels`  
Contains an array of error labels to go with an exception. For example,
error labels can be used to detect whether a transaction can be retried
safely if the *TransientTransactionError* label is present. The
existence of a specific error label should be tested for with the <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>,
instead of interpreting this *errorLabels* property manually.

更新日志
--------

| 版本  | 说明                                                                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.6.0 | The <span class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span> method and <a href="/set/mongodb.html#" class="link">MongoDB\Driver\Exception\RuntimeException::errorLabels</a> property have been added. |

MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel
===========================================================

Returns whether an error label is associated with an exception

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

Returns whether the `errorLabel` has been set for this exception. Error
labels are set by either the server or the driver to indicated specific
situations on which you might want to decide on how you want to handle a
specific exception. A common situation might be to find out whether you
can safely retry a transaction that failed due to a transient error
(like a networking issue, or a transaction conflict). Examples of error
labels are *TransientTransactionError* and
*UnknownTransactionCommitResult*.

### 参数

`errorLabel`  
The name of the *errorLabel* to test for.

### 返回值

Whether the given *errorLabel* is associated with this exception.

### 参见

-   <span
    class="function">MongoDB\\Driver\\Session::commitTransaction</span>
-   <a href="https://docs.mongodb.com/manual/core/transactions/" class="link external">» MongoDB documentation on transactions</a>

**Warning**

This exception class is deprecated and may be removed in a future major
version. The driver has never thrown this exception.

简介
----

Thrown when the driver fails to establish an SSL connection with the
server.

类摘要
------

**MongoDB\\Driver\\Exception\\SSLConnectionException**

<span class="modifier">final</span> <span class="ooclass"> class
**MongoDB\\Driver\\Exception\\SSLConnectionException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\ConnectionException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Thrown when the driver encounters an unexpected value (e.g. during BSON
serialization or deserialization).

类摘要
------

**MongoDB\\Driver\\Exception\\UnexpectedValueException**

<span class="ooclass"> class
**MongoDB\\Driver\\Exception\\UnexpectedValueException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**UnexpectedValueException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Base class for exceptions thrown by a failed write operation. The
exception encapsulates a <span
class="classname">MongoDB\\Driver\\WriteResult</span> object.

类摘要
------

**MongoDB\\Driver\\Exception\\WriteException**

<span class="ooclass"> <span class="modifier">abstract</span> class
**MongoDB\\Driver\\Exception\\WriteException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**MongoDB\\Driver\\Exception\\ServerException** </span> <span
class="oointerface">implements <span
class="interfacename">MongoDB\\Driver\\Exception\\Exception</span>
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span
class="type">MongoDB\\Driver\\WriteResult</span> `$writeResult` ;

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span
class="type">array\|null</span> `$errorLabels` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">getWriteResult</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">bool</span> <span
class="methodname">MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel</span>
( <span class="methodparam"><span class="type">string</span>
`$errorLabel`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`writeResult`  
The <span class="classname">MongoDB\\Driver\\WriteResult</span>
associated with the failed write operation.

更新日志
--------

| 版本  | 说明                                                                                                                                                                                      |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.5.0 | This class now extends <span class="classname">MongoDB\\Driver\\Exception\\ServerException</span> instead of <span class="classname">MongoDB\\Driver\\Exception\\RuntimeException</span>. |

MongoDB\\Driver\\Exception\\WriteException::getWriteResult
==========================================================

Returns the WriteResult for the failed write operation

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">MongoDB\\Driver\\WriteResult</span> <span
class="methodname">MongoDB\\Driver\\Exception\\WriteException::getWriteResult</span>
( <span class="methodparam">void</span> )

Returns the <span class="classname">MongoDB\\Driver\\WriteResult</span>
for the failed write operation. The <span
class="function">MongoDB\\Driver\\WriteResult::getWriteErrors</span> and
<span
class="function">MongoDB\\Driver\\WriteResult::getWriteConcernError</span>
methods may be used to get more details about the failure.

### 参数

此函数没有参数。

### 返回值

The <span class="classname">MongoDB\\Driver\\WriteResult</span> for the
failed write operation.

### 范例

**示例 \#1 <span
class="function">MongoDB\\Driver\\Exception\\WriteException::getWriteResult</span>
example**

``` php
<?php

$manager = new MongoDB\Driver\Manager('mongodb://localhost');
$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['_id' => 1]);
$bulk->insert(['_id' => 1]);

try {
    $manager->executeBulkWrite('db.collection', $bulk);
} catch (MongoDB\Driver\Exception\WriteException $e) {
    $writeResult = $e->getWriteResult();

    if ($writeConcernError = $writeResult->getWriteConcernError()) {
        var_dump($writeConcernError);
    }

    if ($writeErrors = $writeResult->getWriteErrors()) {
        var_dump($writeErrors);
    }
}

?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      object(MongoDB\Driver\WriteError)#5 (4) {
        ["message"]=>
        string(70) "E11000 duplicate key error index: db.collection.$_id_ dup key: { : 1 }"
        ["code"]=>
        int(11000)
        ["index"]=>
        int(1)
        ["info"]=>
        NULL
      }
    }

### 参见

-   <span class="classname">MongoDB\\Driver\\WriteResult</span>
-   <span
    class="function">MongoDB\\Driver\\Manager::executeBulkWrite</span>
