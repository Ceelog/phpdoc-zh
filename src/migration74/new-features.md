New Features
------------

### PHP Core

#### Typed properties

Class properties now support type declarations.

``` php
<?php
class User {
    public int $id;
    public string $name;
}
?>
```

The above example will enforce that *$user-\>id* can only be assigned
<span class="type">integer</span> values and *$user-\>name* can only be
assigned <span class="type">string</span> values.

#### Arrow functions

<a href="/functions/arrow.html" class="link">Arrow functions</a> provide
a shorthand syntax for defining functions with implicit by-value scope
binding.

``` php
<?php
$factor = 10;
$nums = array_map(fn($n) => $n * $factor, [1, 2, 3, 4]);
// $nums = array(10, 20, 30, 40);
?>
```

#### Limited return type covariance and argument type contravariance

The following code will now work:

``` php
<?php
class A {}
class B extends A {}

class Producer {
    public function method(): A {}
}
class ChildProducer extends Producer {
    public function method(): B {}
}
?>
```

Full variance support is only available if autoloading is used. Inside a
single file only non-cyclic type references are possible, because all
classes need to be available before they are referenced.

#### Null coalescing assignment operator

``` php
<?php
$array['key'] ??= computeDefault();
// is roughly equivalent to
if (!isset($array['key'])) {
    $array['key'] = computeDefault();
}
?>
```

#### Unpacking inside arrays

``` php
<?php
$parts = ['apple', 'pear'];
$fruits = ['banana', 'orange', ...$parts, 'watermelon'];
// ['banana', 'orange', 'apple', 'pear', 'watermelon'];
?>
```

#### Numeric literal separator

Numeric literals can contain underscores between digits.

``` php
<?php
6.674_083e-11; // float
299_792_458;   // decimal
0xCAFE_F00D;   // hexadecimal
0b0101_1111;   // binary
?>
```

#### Weak references

Weak references allow the programmer to retain a reference to an object
that does not prevent the object from being destroyed.

#### Allow exceptions from \_\_toString()

Throwing exceptions from
<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
is now permitted. Previously this resulted in a fatal error. Existing
recoverable fatal errors in string conversions have been converted to
<span class="classname">Error</span> exceptions.

### CURL

<span class="classname">CURLFile</span> now supports stream wrappers in
addition to plain file names, if the extension has been built against
libcurl \>= 7.56.0.

### Filter

The **`FILTER_VALIDATE_FLOAT`** filter now supports the *min\_range* and
*max\_range* options, with the same semantics as
**`FILTER_VALIDATE_INT`**.

### FFI

FFI is a new extension, which provides a simple way to call native
functions, access native variables, and create/access data structures
defined in C libraries.

### GD

Added the **`IMG_FILTER_SCATTER`** image filter to apply a scatter
filter to images.

### Hash

Added *crc32c* hash using Castagnoli's polynomial. This CRC32 variant is
used by storage systems, such as iSCSI, SCTP, Btrfs and ext4.

### Multibyte String

Added the <span class="function">mb\_str\_split</span> function, which
provides the same functionality as <span
class="function">str\_split</span>, but operating on code points rather
than bytes.

### OPcache

Support for preloading code has been added.

### Regular Expressions (Perl-Compatible)

The <span class="function">preg\_replace\_callback</span> and <span
class="function">preg\_replace\_callback\_array</span> functions now
accept an additional `flags` argument, with support for the
**`PREG_OFFSET_CAPTURE`** and **`PREG_UNMATCHED_AS_NULL`** flags. This
influences the format of the matches array passed to to the callback
function.

### PDO

The username and password can now be specified as part of the PDO DSN
for the mysql, mssql, sybase, dblib, firebird and oci drivers.
Previously this was only supported by the pgsql driver. If a
username/password is specified both in the constructor and the DSN, the
constructor takes precedence.

It is now possible to escape question marks in SQL queries to avoid them
being interpreted as parameter placeholders. Writing *??* allows sending
a single question mark to the database and e.g. use the PostgreSQL JSON
key exists (*?*) operator.

### PDO\_OCI

<span class="methodname">PDOStatement::getColumnMeta</span> is now
available.

### PDO\_SQLite

*PDOStatement::getAttribute(PDO::SQLITE\_ATTR\_READONLY\_STATEMENT)*
allows checking whether the statement is read-only, i.e. if it doesn't
modify the database.

*PDO::setAttribute(PDO::SQLITE\_ATTR\_EXTENDED\_RESULT\_CODES, true)*
enables the use of SQLite3 extended result codes in <span
class="function">PDO::errorInfo</span> and <span
class="function">PDOStatement::errorInfo</span>.

### SQLite3

Added <span class="methodname">SQLite3::lastExtendedErrorCode</span> to
fetch the last extended result code.

Added *SQLite3::enableExtendedResultCodes($enable = true)*, which will
make <span class="methodname">SQLite3::lastErrorCode</span> return
extended result codes.

### Standard

#### strip\_tags() with array of tag names

<span class="function">strip\_tags</span> now also accepts an array of
allowed tags: instead of *strip\_tags($str, '\<a\>\<p\>')* you can now
write *strip\_tags($str, \['a', 'p'\])*.

#### Custom object serialization

A new mechanism for custom object serialization has been added, which
uses two new magic methods: *\_\_serialize* and *\_\_unserialize*.

``` php
<?php
// Returns array containing all the necessary state of the object.
public function __serialize(): array;

// Restores the object state from the given data array.
public function __unserialize(array $data): void;
?>
```

The new serialization mechanism supersedes the <span
class="interfacename">Serializable</span> interface, which will be
deprecated in the future.

#### Array merge functions without arguments

<span class="function">array\_merge</span> and <span
class="function">array\_merge\_recursive</span> may now be called
without any arguments, in which case they will return an empty array.
This is useful in conjunction with the spread operator, e.g.
*array\_merge(...$arrays)*.

#### <span class="function">proc\_open</span> function

<span class="function">proc\_open</span> now accepts an array instead of
a string for the command. In this case the process will be opened
directly (without going through a shell) and PHP will take care of any
necessary argument escaping.

``` php
<?php
proc_open(['php', '-r', 'echo "Hello World\n";'], $descriptors, $pipes);
?>
```

<span class="function">proc\_open</span> now supports *redirect* and
*null* descriptors.

``` php
<?php
// Like 2>&1 on the shell
proc_open($cmd, [1 => ['pipe', 'w'], 2 => ['redirect', 1]], $pipes);
// Like 2>/dev/null or 2>nul on the shell
proc_open($cmd, [1 => ['pipe', 'w'], 2 => ['null']], $pipes);
?>
```

#### argon2i(d) without libargon

<span class="function">password\_hash</span> now has the argon2i and
argon2id implementations from the sodium extension when PHP is built
without libargon.
