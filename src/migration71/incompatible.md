不向后兼容的变更
----------------

### 当传递参数过少时将抛出错误

在过去如果我们调用一个用户定义的函数时，提供的参数不足，那么将会产生一个警告(warning)。
现在，这个警告被提升为一个错误异常(Error
exception)。这个变更仅对用户定义的函数生效， 并不包含内置函数。例如：

``` php
<?php
function test($param){}
test();
```

以上例程在 PHP 5.5 中的输出：

    Uncaught Error: Too few arguments to function test(), 0 passed in %s on line %d and exactly 1 expected in %s:%d

### Forbid dynamic calls to scope introspection functions

Dynamic calls for certain functions have been forbidden (in the form of
*$func()* or *array\_map('extract', ...)*, etc). These functions either
inspect or modify another scope, and present with them ambiguous and
unreliable behavior. The functions are as follows:

-   <span class="simpara"> <span class="function">assert</span> - with a
    string as the first argument </span>
-   <span class="simpara"> <span class="function">compact</span> </span>
-   <span class="simpara"> <span class="function">extract</span> </span>
-   <span class="simpara"> <span class="function">func\_get\_args</span>
    </span>
-   <span class="simpara"> <span class="function">func\_get\_arg</span>
    </span>
-   <span class="simpara"> <span class="function">func\_num\_args</span>
    </span>
-   <span class="simpara"> <span
    class="function">get\_defined\_vars</span> </span>
-   <span class="simpara"> <span
    class="function">mb\_parse\_str</span> - with one arg </span>
-   <span class="simpara"> <span class="function">parse\_str</span> -
    with one arg </span>

``` php
<?php
(function () {
    'func_num_args'();
})();
```

以上例程会输出：

    Warning: Cannot call func_num_args() dynamically in %s on line %d

### Invalid class, interface, and trait names

The following names cannot be used to name classes, interfaces, or
traits:

-   <span class="simpara"><span class="type">void</span></span>
-   <span class="simpara"><span class="type">iterable</span></span>

### Numerical string conversions now respect scientific notation

Integer operations and conversions on numerical strings now respect
scientific notation. This also includes the *(int)* cast operation, and
the following functions: <span class="function">intval</span> (where the
base is 10), <span class="function">settype</span>, <span
class="function">decbin</span>, <span class="function">decoct</span>,
and <span class="function">dechex</span>.

### Fixes to <span class="function">mt\_rand</span> algorithm

<span class="function">mt\_rand</span> will now default to using the
fixed version of the Mersenne Twister algorithm. If deterministic output
from <span class="function">mt\_srand</span> was relied upon, then the
**`MT_RAND_PHP`** with the ability to preserve the old (incorrect)
implementation via an additional optional second parameter to <span
class="function">mt\_srand</span>.

### <span class="function">rand</span> aliased to <span class="function">mt\_rand</span> and <span class="function">srand</span> aliased to <span class="function">mt\_srand</span>

<span class="function">rand</span> and <span
class="function">srand</span> have now been made aliases to <span
class="function">mt\_rand</span> and <span
class="function">mt\_srand</span>, respectively. This means that the
output for the following functions have changes: <span
class="function">rand</span>, <span class="function">shuffle</span>,
<span class="function">str\_shuffle</span>, and <span
class="function">array\_rand</span>.

### Disallow the ASCII delete control character in identifiers

The ASCII delete control character (*0x7F*) can no longer be used in
identifiers that are not quoted.

### `error_log` changes with *syslog* value

If the `error_log` ini setting is set to *syslog*, the PHP error levels
are mapped to the syslog error levels. This brings finer differentiation
in the error logs in contrary to the previous approach where all the
errors are logged with the notice level only.

### 在不完整的对象上不再调用析构方法

析构方法在一个不完整的对象（例如在构造方法中抛出一个异常）上将不再会被调用。

### <span class="function">call\_user\_func</span>不再支持对传址的函数的调用

<span class="function">call\_user\_func</span>
现在在调用一个以引用作为参数的函数时将始终失败。

### 字符串不再支持空索引操作符 The empty index operator is not supported for strings anymore

对字符串使用一个空索引操作符（例如*$str\[\] =
$x*）将会抛出一个致命错误， 而不是静默地将其转为一个数组。

### ini配置项移除

下列ini配置项已经被移除：

-   <span class="simpara"> `session.entropy_file` </span>
-   <span class="simpara"> `session.entropy_length` </span>
-   <span class="simpara"> `session.hash_function` </span>
-   <span class="simpara"> `session.hash_bits_per_character` </span>

### Array ordering when elements are automatically created during by reference assignments has changed

The order of the elements in an array has changed when those elements
have been automatically created by referencing them in a by reference
assignment. For example:

``` php
<?php
$array = [];
$array["a"] =& $array["b"];
$array["b"] = 1;
var_dump($array);
?>
```

以上例程在 PHP 7.0 中的输出：

    array(2) {
      ["a"]=>
      &int(1)
      ["b"]=>
      &int(1)
    }

以上例程在 PHP 7.1 中的输出：

    array(2) {
      ["b"]=>
      &int(1)
      ["a"]=>
      &int(1)
    }

### Sort order of equal elements

The internal sorting algorithm has been improved, what may result in
different sort order of elements, which compare as equal, than before.

> **Note**:
>
> Don't rely on the order of elements which compare as equal; it might
> change anytime.

### Error message for E\_RECOVERABLE errors

The error message for E\_RECOVERABLE errors has been changed from
"Catchable fatal error" to "Recoverable fatal error".

### $options parameter of unserialize()

The *allowed\_classes* element of the $options parameter of <span
class="function">unserialize</span> is now strictly typed, i.e. if
anything other than an <span class="type">array</span> or a <span
class="type">boolean</span> is given, unserialize() returns **`FALSE`**
and issues an **`E_WARNING`**.

### DateTime constructor incorporates microseconds

<span class="classname">DateTime</span> and <span
class="classname">DateTimeImmutable</span> now properly incorporate
microseconds when constructed from the current time, either explicitly
or with a relative string (e.g. *"first day of next month"*). This means
that naive comparisons of two newly created instances will now more
likely return **`FALSE`** instead of **`TRUE`**:

``` php
<?php
new DateTime() == new DateTime();
?>
```

### Fatal errors to <span class="classname">Error</span> exceptions conversions

In the Date extension, invalid serialization data for <span
class="classname">DateTime</span> or <span
class="classname">DatePeriod</span> classes, or timezone initialization
failure from serialized data, will now throw an <span
class="classname">Error</span> exception from the <span
class="methodname">\_\_wakeup</span> or <span
class="methodname">\_\_set\_state</span> methods, instead of resulting
in a fatal error.

In the DBA extension, data modification functions (such as <span
class="function">dba\_insert</span>) will now throw an <span
class="classname">Error</span> exception instead of triggering a
catchable fatal error if the key does not contain exactly two elements.

In the DOM extension, invalid schema or RelaxNG validation contexts will
now throw an <span class="classname">Error</span> exception instead of
resulting in a fatal error. Similarly, attempting to register a node
class that does not extend the appropriate base class, or attempting to
read an invalid property or write to a readonly property, will also now
throw an <span class="classname">Error</span> exception.

In the IMAP extension, email addresses longer than 16385 bytes will
throw an <span class="classname">Error</span> exception instead of
resulting in a fatal error.

In the Intl extension, failing to call the parent constructor in a class
extending <span class="classname">Collator</span> before invoking the
parent methods will now throw an <span class="classname">Error</span>
instead of resulting in a recoverable fatal error. Also, cloning a <span
class="classname">Transliterator</span> object will now throw an <span
class="classname">Error</span> exception on failure to clone the
internal transliterator instead of resulting in a fatal error.

In the LDAP extension, providing an unknown modification type to <span
class="function">ldap\_batch\_modify</span> will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error.

In the mbstring extension, the <span class="function">mb\_ereg</span>
and <span class="function">mb\_eregi</span> functions will now throw a
<span class="classname">ParseError</span> exception if an invalid PHP
expression is provided and the 'e' option is used.

In the Mcrypt extension, the <span
class="function">mcrypt\_encrypt</span> and <span
class="function">mcrypt\_decrypt</span> will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error if mcrypt cannot be initialized.

In the mysqli extension, attempting to read an invalid property or write
to a readonly property will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error.

In the Reflection extension, failing to retrieve a reflection object or
retrieve an object property will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error.

In the Session extension, custom session handlers that do not return
strings for session IDs will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error when a function is called that must generate a session ID.

In the SimpleXML extension, creating an unnamed or duplicate attribute
will now throw an <span class="classname">Error</span> exception instead
of resulting in a fatal error.

In the SPL extension, attempting to clone an <span
class="classname">SplDirectory</span> object will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error. Similarly, calling <span
class="methodname">ArrayIterator::append</span> when iterating over an
object will also now throw an <span class="classname">Error</span>
exception.

In the standard extension, the <span class="function">assert</span>
function, when provided with a string argument as its first parameter,
will now throw a <span class="classname">ParseError</span> exception
instead of resulting in a catchable fatal error if the PHP code is
invalid. Similarly, calling <span
class="function">forward\_static\_call</span> outside of a class scope
will now throw an <span class="classname">Error</span> exception.

In the Tidy extension, creating a <span
class="classname">tidyNode</span> manually will now throw an <span
class="classname">Error</span> exception instead of resulting in a fatal
error.

In the WDDX extension, a circular reference when serializing will now
throw an <span class="classname">Error</span> exception instead of
resulting in a fatal error.

In the XML-RPC extension, a circular reference when serializing will now
throw an instance of <span class="classname">Error</span> exception
instead of resulting in a fatal error.

In the Zip extension, the <span
class="methodname">ZipArchive::addGlob</span> method will now throw an
<span class="classname">Error</span> exception instead of resulting in a
fatal error if glob support is not available.

### Lexically bound variables cannot reuse names

Variables bound to a
<a href="/functions/anonymous.html" class="link">closure</a> via the
*use* construct cannot use the same name as any
<a href="/language/variables/predefined.html" class="link">superglobals</a>,
`$this`, or any parameter. For example, all of these function definition
will result in a fatal error:

``` php
<?php
$f = function () use ($_SERVER) {};
$f = function () use ($this) {};
$f = function ($param) use ($param) {};
```

### JSON encoding and decoding

The `serialize_precision` ini setting now controls the serialization
precision when encoding doubles.

Decoding an empty key now results in an empty property name, rather than
*\_empty\_* as a property name.

``` php
<?php
var_dump(json_decode(json_encode(['' => 1])));
```

以上例程的输出类似于：

    object(stdClass)#1 (1) {
      [""]=>
      int(1)
    }

When supplying the **`JSON_UNESCAPED_UNICODE`** flag to <span
class="function">json\_encode</span>, the sequences U+2028 and U+2029
are now escaped.

### Changes to <span class="function">mb\_ereg</span> and <span class="function">mb\_eregi</span> parameter semantics

The third paramter to the <span class="function">mb\_ereg</span> and
<span class="function">mb\_eregi</span> functions (`regs`) will now be
set to an empty array if nothing was matched. Formely, the parameter
would not have been modified.

### Drop support for the sslv2 stream

The sslv2 stream has now been dropped in OpenSSL.
