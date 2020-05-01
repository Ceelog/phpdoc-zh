Backward incompatible changes
-----------------------------

### Prevent <span class="function">number\_format</span> from returning negative zero

Previously, it was possible for the <span
class="function">number\_format</span> function to return *-0*. Whilst
this is perfectly valid according to the IEEE 754 floating point
specification, this oddity was not desirable for displaying formatted
numbers in a human-readable form.

``` php
<?php

var_dump(number_format(-0.01)); // now outputs string(1) "0" instead of string(2) "-0"
```

### Convert numeric keys in object and array casts

Numeric keys are now better handled when casting arrays to objects and
objects to arrays (either from explicit casting or by <span
class="function">settype</span>).

This means that integer (or stringy integer) keys from arrays being
casted to objects are now accessible:

``` php
<?php

// array to object
$arr = [0 => 1];
$obj = (object)$arr;
var_dump(
    $obj,
    $obj->{'0'}, // now accessible
    $obj->{0} // now accessible
);
```

以上例程会输出：

    object(stdClass)#1 (1) {
      ["0"]=>    // string key now, rather than integer key
      int(1)
    }
    int(1)
    int(1)

And integer (or stringy integer) keys from objects being casted to
arrays are now accessible:

``` php
<?php

// object to array
$obj = new class {
    public function __construct()
    {
        $this->{0} = 1;
    }
};
$arr = (array)$obj;
var_dump(
    $arr,
    $arr[0], // now accessible
    $arr['0'] // now accessible
);
```

以上例程会输出：

    array(1) {
      [0]=>    // integer key now, rather than string key
      int(1)
    }
    int(1)
    int(1)

### Disallow passing **`NULL`** to <span class="function">get\_class</span>

Previously, passing **`NULL`** to the <span
class="function">get\_class</span> function would output the name of the
enclosing class. This behaviour has now been removed, where an
**`E_WARNING`** will be output instead. To achieve the same behaviour as
before, the argument should simply be omitted.

### Warn when counting non-countable types

An **`E_WARNING`** will now be emitted when attempting to <span
class="function">count</span> non-countable types (this includes the
<span class="function">sizeof</span> alias function).

``` php
<?php

var_dump(
    count(null), // NULL is not countable
    count(1), // integers are not countable
    count('abc'), // strings are not countable
    count(new stdclass), // objects not implementing the Countable interface are not countable
    count([1,2]) // arrays are countable
);
```

以上例程会输出：

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d
    int(0)
    int(1)
    int(1)
    int(1)
    int(2)

### Move ext/hash from resources to objects

As part of the long-term migration away from resources, the
<a href="/book/hash.html" class="link">Hash</a> extension has been
updated to use objects instead of resources. The change should be
seamless for PHP developers, except for where <span
class="function">is\_resource</span> checks have been made (which will
need updating to <span class="function">is\_object</span> instead).

### Improve SSL/TLS defaults

The following changes to the defaults have been made:

-   <span class="simpara"> *tls://* now defaults to TLSv1.0 or TLSv1.1
    or TLSv1.2 </span>
-   <span class="simpara"> *ssl://* an alias of *tls://* </span>
-   <span class="simpara"> *STREAM\_CRYPTO\_METHOD\_TLS\_\** constants
    default to TLSv1.0 or TLSv1.1 + TLSv1.2, instead of TLSv1.0 only
    </span>

### <span class="function">gettype</span> return value on closed resources

Previously, using <span class="function">gettype</span> on a closed
resource would return a string of *"unknown type"*. Now, a string of
*"resource (closed)"* will be returned.

### <span class="function">is\_object</span> and <span class="classname">\_\_PHP\_Incomplete\_Class</span>

Previously, using <span class="function">is\_object</span> on the <span
class="classname">\_\_PHP\_Incomplete\_Class</span> class would return
**`FALSE`**. Now, **`TRUE`** will be returned.

### Promote the error level of undefined constants

Unqualified references to undefined constants will now generate an
**`E_WARNING`** (instead of an **`E_NOTICE`**). In the next major
version of PHP, they will generate <span class="classname">Error</span>
exceptions.

### Windows support

The officially supported, minimum Windows versions are now Windows
7/Server 2008 R2.

### Checks on default property values of traits

Compatibility checks upon default trait property values will no longer
perform casting.

### *object* for class names

The *object* name was previously soft-reserved in PHP 7.0. This is now
hard-reserved, prohibiting it from being used as a class, trait, or
interface name.

### NetWare support

Support for NetWare has now been removed.

### <span class="function">array\_unique</span> with **`SORT_STRING`**

While <span class="function">array\_unique</span> with **`SORT_STRING`**
formerly copied the array and removed non-unique elements (without
packing the array afterwards), now a new array is built by adding the
unique elements. This can result in different numeric indexes.

### <span class="function">bcmod</span> changes with floats

The <span class="function">bcmod</span> function no longer truncates
fractional numbers to integers. As such, its behavior now follows <span
class="function">fmod</span>, rather than the *%* operator. For example
*bcmod('4', '3.5')* now returns *0.5* instead of *1*.

### Hashing functions and non-cryptographic hashes

The <span class="function">hash\_hmac</span>, <span
class="function">hash\_hmac\_file</span>, <span
class="function">hash\_pbkdf2</span>, and <span
class="function">hash\_init</span> (with **`HASH_HMAC`**) functions no
longer accept non-cryptographic hashes.

### <span class="function">json\_decode</span> function options

The <span class="function">json\_decode</span> function option,
**`JSON_OBJECT_AS_ARRAY`**, is now used if the second parameter (assoc)
is **`NULL`**. Previously, **`JSON_OBJECT_AS_ARRAY`** was always
ignored.

### <span class="function">rand</span> and <span class="function">mt\_rand</span> output

Sequences generated by <span class="function">rand</span> and <span
class="function">mt\_rand</span> for a specific seed may differ from PHP
7.1 on 64-bit machines (due to the fixing of a modulo bias bug in the
implementation).

### Removal of <a href="/ini/core.html#ini.sql.safe-mode" class="link"><code class="parameter">sql.safe_mode</code></a> ini setting

The `sql.safe_mode` ini setting has now been removed.

### Changes to <span class="function">date\_parse</span> and <span class="function">date\_parse\_from\_format</span>

The *zone* element of the array returned by <span
class="function">date\_parse</span> and <span
class="function">date\_parse\_from\_format</span> represents seconds
instead of minutes now, and its sign is inverted. For instance *-120* is
now *7200*.
