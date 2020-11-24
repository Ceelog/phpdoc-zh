不向后兼容的变更
----------------

### PHP 核心中不向后兼容的变更

#### String to Number Comparison

Non-strict comparisons between numbers and non-numeric strings now work
by casting the number to string and comparing the strings. Comparisons
between numbers and numeric strings continue to work as before. Notably,
this means that `0 == "not-a-number"` is considered false now.

| Comparison      | Before     | After       |
|-----------------|------------|-------------|
| `0 == "0"`      | **`TRUE`** | **`TRUE`**  |
| `0 == "0.0"`    | **`TRUE`** | **`TRUE`**  |
| `0 == "foo"`    | **`TRUE`** | **`FALSE`** |
| `0 == ""`       | **`TRUE`** | **`FALSE`** |
| `42 == "   42"` | **`TRUE`** | **`TRUE`**  |
| `42 == "42foo"` | **`TRUE`** | **`FALSE`** |

#### 其它不向后兼容的变更

-   *match* is now a reserved keyword.

-   Assertion failures now throw by default. If the old behavior is
    desired, `assert.exception=0` can be set in the INI settings.

-   Methods with the same name as the class are no longer interpreted as
    constructors. The
    <a href="/language/oop5/decon.html#object.construct" class="link">__construct()</a>
    method should be used instead.

-   The ability to call non-static methods statically has been removed.
    Thus <span class="function">is\_callable</span> will fail when
    checking for a non-static method with a classname (must check with
    an object instance).

-   The `(real)` and `(unset)` casts have been removed.

-   The <a href="/errorfunc/setup.html#" class="link">track_errors</a>
    ini directive has been removed. This means that `php_errormsg` is no
    longer available. The <span class="function">error\_get\_last</span>
    function may be used instead.

-   The ability to define case-insensitive constants has been removed.
    The third argument to <span class="function">define</span> may no
    longer be **`TRUE`**.

-   The ability to specify an autoloader using an <span
    class="function">\_\_autoload</span> function has been removed.
    <span class="function">spl\_autoload\_register</span> should be used
    instead.

-   The `errcontext` argument for custom error handlers has been
    removed.

-   <span class="function">create\_function</span> has been removed.
    Anonymous functions may be used instead.

-   <span class="function">each</span> has been removed.
    <a href="/control-structures/foreach.html" class="link">foreach</a>
    or <span class="classname">ArrayIterator</span> should be used
    instead.

-   The ability to unbind `this` from closures that were created from a
    method, using <span class="methodname">Closure::fromCallable</span>
    or <span class="methodname">ReflectionMethod::getClosure</span>, has
    been removed.

-   The ability to unbind `this` from proper closures that contain uses
    of `this` has also been removed.

-   The ability to use <span class="function">array\_key\_exists</span>
    with objects has been removed. <span class="function">isset</span>
    or <span class="function">property\_exists</span> may be used
    instead.

-   The behavior of <span class="function">array\_key\_exists</span>
    regarding the type of the `key` parameter has been made consistent
    with <span class="function">isset</span> and normal array access.
    All key types now use the usual coercions and array/object keys
    throw a <span class="classname">TypeError</span>.

-   Any array that has a number <span class="replaceable">n</span> as
    its first numeric key will use <span class="replaceable">n+1</span>
    for its next implicit key, even if <span
    class="replaceable">n</span> is negative.

-   The default error\_reporting level is now **`E_ALL`**. Previously it
    excluded **`E_NOTICE`** and **`E_DEPRECATED`**.

-   <a href="/errorfunc/setup.html#" class="link">display_startup_errors</a>
    is now enabled by default.

-   Using <span class="type">parent</span> inside a class that has no
    parent will now result in a fatal compile-time error.

-   The *@* operator will no longer silence fatal errors (**`E_ERROR`**,
    **`E_CORE_ERROR`**, **`E_COMPILE_ERROR`**, **`E_USER_ERROR`**,
    **`E_RECOVERABLE_ERROR`**, **`E_PARSE`**). Error handlers that
    expect error\_reporting to be *0* when *@* is used, should be
    adjusted to use a mask check instead:

    ``` php
    <?php
    // Replace
    function my_error_handler($err_no, $err_msg, $filename, $linenum) {
        if (error_reporting() == 0) {
            return; // Silenced
        }
        // ...
    }

    // With
    function my_error_handler($err_no, $err_msg, $filename, $linenum) {
        if (!(error_reporting() & $err_no)) {
            return; // Silenced
        }
        // ...
    }
    ?>
    ```

    Additionally, care should be taken that error messages are not
    displayed in production environments, which can result in
    information leaks. Please ensure that `display_errors=Off` is used
    in conjunction with error logging.

-   *\#\[* is no longer interpreted as the start of a comment, as this
    syntax is now used for attributes.

-   Inheritance errors due to incompatible method signatures (LSP
    violations) will now always generate a fatal error. Previously a
    warning was generated in some cases.

-   The precedence of the concatenation operator has changed relative to
    bitshifts and addition as well as subtraction.

    ``` php
    <?php
    echo "Sum: " . $a + $b;
    // was previously interpreted as:
    echo ("Sum: " . $a) + $b;
    // is now interpreted as:
    echo "Sum:" . ($a + $b);
    ?>
    ```

-   Arguments with a default value that resolves to **`NULL`** at
    runtime will no longer implicitly mark the argument type as
    nullable. Either an explicit nullable type, or an explicit
    **`NULL`** default value has to be used instead.

    ``` php
    <?php
    // Replace
    function test(int $arg = CONST_RESOLVING_TO_NULL) {}
    // With
    function test(?int $arg = CONST_RESOLVING_TO_NULL) {}
    // Or
    function test(int $arg = null) {}
    ?>
    ```

-   A number of warnings have been converted into <span
    class="classname">Error</span> exceptions:

    -   Attempting to write to a property of a non-object. Previously
        this implicitly created an stdClass object for null, false and
        empty strings.
    -   Attempting to append an element to an array for which the
        PHP\_INT\_MAX key is already used.
    -   Attempting to use an invalid type (array or object) as an array
        key or string offset.
    -   Attempting to write to an array index of a scalar value.
    -   Attempting to unpack a non-array/Traversable.
    -   Attempting to access unqualified constants which are undefined.
        Previously, unqualified constant accesses resulted in a warning
        and were interpreted as strings.

    A number of notices have been converted into warnings:

    -   Attempting to read an undefined variable.
    -   Attempting to read an undefined property.
    -   Attempting to read an undefined array key.
    -   Attempting to read a property of a non-object.
    -   Attempting to access an array index of a non-array.
    -   Attempting to convert an array to string.
    -   Attempting to use a resource as an array key.
    -   Attempting to use null, a boolean, or a float as a string
        offset.
    -   Attempting to read an out-of-bounds string offset.
    -   Attempting to assign an empty string to a string offset.

-   Attempting to assign multiple bytes to a string offset will now emit
    a warning.

-   Unexpected characters in source files (such as NUL bytes outside of
    strings) will now result in a <span
    class="classname">ParseError</span> exception instead of a compile
    warning.

-   Uncaught exceptions now go through "clean shutdown", which means
    that destructors will be called after an uncaught exception.

-   The compile time fatal error "Only variables can be passed by
    reference" has been delayed until runtime, and converted into an
    "Argument cannot be passed by reference" <span
    class="classname">Error</span> exception.

-   Some "Only variables should be passed by reference" notices have
    been converted to "Argument cannot be passed by reference"
    exception.

-   The generated name for anonymous classes has changed. It will now
    include the name of the first parent or interface:

    ``` php
    <?php
    new class extends ParentClass {};
    // -> ParentClass@anonymous
    new class implements FirstInterface, SecondInterface {};
    // -> FirstInterface@anonymous
    new class {};
    // -> class@anonymous
    ?>
    ```

    The name shown above is still followed by a NUL byte and a unique
    suffix.

-   Non-absolute trait method references in trait alias adaptations are
    now required to be unambiguous:

    ``` php
    <?php
    class X {
        use T1, T2 {
            func as otherFunc;
        }
        function func() {}
    }
    ?>
    ```

    If both `T1::func()` and `T2::func()` exist, this code was
    previously silently accepted, and func was assumed to refer to
    `T1::func`. Now it will generate a fatal error instead, and either
    `T1::func` or `T2::func` needs to be written explicitly.

-   The signature of abstract methods defined in traits is now checked
    against the implementing class method:

    ``` php
    <?php
    trait MyTrait {
        abstract private function neededByTrait(): string;
    }

    class MyClass {
        use MyTrait;

        // Error, because of return type mismatch.
        private function neededByTrait(): int { return 42; }
    }
    ?>
    ```

-   Disabled functions are now treated exactly like non-existent
    functions. Calling a disabled function will report it as unknown,
    and redefining a disabled function is now possible.

-   *data://* stream wrappers are no longer writable, which matches the
    documented behavior.

-   The arithmetic and bitwise operators *+*, *-*, *\**, */*, *\*\**,
    *%*, *\<\<*, *\>\>*, *&*, *\|*, *^*, *\~*, *++*, *--* will now
    consistently throw a <span class="classname">TypeError</span> when
    one of the operands is an <span class="type">array</span>,
    <a href="/language/types/resource.html" class="link">资源(resource)</a>
    or non-overloaded <span class="type">object</span>. The only
    exception to this is the array *+* array merge operation, which
    remains supported.

-   Float to string casting will now always behave locale-independently.

        <?php
        setlocale(LC_ALL, "de_DE");
        $f = 3.14;
        echo $f, "\n";
        // Previously: 3,14
        // Now:        3.14
        ?>

    See <span class="function">printf</span>, <span
    class="function">number\_format</span> and <span
    class="methodname">NumberFormatter</span> for ways to customize
    number formatting.

-   Support for deprecated curly braces for offset access has been
    removed.

        <?php
        // Instead of:
        $array{0};
        $array{"key"};
        // Write:
        $array[0];
        $array["key"];
        ?>

-   Applying the final modifier on a private method will now produce a
    warning unless that method is the constructor.

-   If an object constructor <span class="function">exit</span>s, the
    object destructor will no longer be called. This matches the
    behavior when the constructor throws.

-   Namespaced names can no longer contain whitespace: While `Foo\Bar`
    will be recognized as a namespaced name, `Foo \ Bar` will not.
    Conversely, reserved keywords are now permitted as namespace
    segments, which may also change the interpretation of code: `new\x`
    is now the same as `constant('new\x')`, not `new \x()`.

-   Nested ternaries now require explicit parentheses.

-   <span class="function">debug\_backtrace</span> and <span
    class="methodname">Exception::getTrace</span> will no longer provide
    references to arguments. It will not be possible to change function
    arguments through the backtrace.

-   Numeric string handling has been altered to be more intuitive and
    less error-prone. Trailing whitespace is now allowed in numeric
    strings for consistency with how leading whitespace is treated. This
    mostly affects:

    -   The <span class="function">is\_numeric</span> function
    -   String-to-string comparisons
    -   Type declarations
    -   Increment and decrement operations

    The concept of a "leading-numeric string" has been mostly dropped;
    the cases where this remains exist in order to ease migration.
    Strings which emitted an **`E_NOTICE`** "A non well-formed numeric
    value encountered" will now emit an **`E_WARNING`** "A non-numeric
    value encountered" and all strings which emitted an **`E_WARNING`**
    "A non-numeric value encountered" will now throw a <span
    class="classname">TypeError</span>. This mostly affects:

    -   Arithmetic operations
    -   Bitwise operations

    This **`E_WARNING`** to <span class="classname">TypeError</span>
    change also affects the **`E_WARNING`** "Illegal string offset
    'string'" for illegal string offsets. The behavior of explicit casts
    to int/float from strings has not been changed.

-   Magic Methods will now have their arguments and return types checked
    if they have them declared. The signatures should match the
    following list:

    -   `__call(string $name, array $arguments): mixed`
    -   `__callStatic(string $name, array $arguments): mixed`
    -   `__clone(): void`
    -   `__debugInfo(): ?array`
    -   `__get(string $name): mixed`
    -   `__invoke(mixed $arguments): mixed`
    -   `__isset(string $name): bool`
    -   `__serialize(): array`
    -   `__set(string $name, mixed $value): void`
    -   `__set_state(array $properties): object`
    -   `__sleep(): array`
    -   `__unserialize(array $data): void`
    -   `__unset(string $name): void`
    -   `__wakeup(): void`

-   <span class="function">call\_user\_func\_array</span> array keys
    will now be interpreted as parameter names, instead of being
    silently ignored.

-   Declaring a function called *assert()* inside a namespace is no
    longer allowed, and issues **`E_COMPILE_ERROR`**. The <span
    class="function">assert</span> function is subject to special
    handling by the engine, which may lead to inconsistent behavior when
    defining a namespaced function with the same name.

### Resource to Object Migration

Several
<a href="/language/types/resource.html" class="link">资源(resource)</a>s
have been migrated to <span class="type">object</span>s. Return value
checks using <span class="function">is\_resource</span> should be
replaced with checks for **`FALSE`**.

-   <span class="function">curl\_init</span> will now return a <span
    class="classname">CurlHandle</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">curl\_close</span> function no longer has
    an effect, instead the <span class="classname">CurlHandle</span>
    instance is automatically destroyed if it is no longer referenced.

-   <span class="function">curl\_multi\_init</span> will now return a
    <span class="classname">CurlMultiHandle</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">curl\_multi\_close</span> function no
    longer has an effect, instead the <span
    class="classname">CurlMultiHandle</span> instance is automatically
    destroyed if it is no longer referenced.

-   <span class="function">curl\_share\_init</span> will now return a
    <span class="classname">CurlShareHandle</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">curl\_share\_close</span> function no
    longer has an effect, instead the <span
    class="classname">CurlShareHandle</span> instance is automatically
    destroyed if it is no longer referenced.

-   <span class="function">enchant\_broker\_init</span> will now return
    an <span class="classname">EnchantBroker</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   <span class="function">enchant\_broker\_request\_dict</span> and
    <span class="function">enchant\_broker\_request\_pwl\_dict</span>
    will now return an <span class="classname">EnchantDictionary</span>
    object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   The GD extension now uses <span class="classname">GdImage</span>
    objects as the underlying data structure for images, rather than
    <a href="/language/types/resource.html" class="link">资源(resource)</a>s.
    The <span class="function">imagedestroy</span> function no longer
    has an effect; instead the <span class="classname">GdImage</span>
    instance is automatically destroyed if it is no longer referenced.

-   <span class="function">openssl\_x509\_read</span> and <span
    class="function">openssl\_csr\_sign</span> will now return an <span
    class="classname">OpenSSLCertificate</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">openssl\_x509\_free</span> function is
    deprecated and no longer has an effect, instead the <span
    class="classname">OpenSSLCertificate</span> instance is
    automatically destroyed if it is no longer referenced.

-   <span class="function">openssl\_csr\_new</span> will now return an
    <span class="classname">OpenSSLCertificateSigningRequest</span>
    object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   <span class="function">openssl\_pkey\_new</span> will now return an
    <span class="classname">OpenSSLAsymmetricKey</span> object rather
    than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">openssl\_pkey\_free</span> function is
    deprecated and no longer has an effect, instead the <span
    class="classname">OpenSSLAsymmetricKey</span> instance is
    automatically destroyed if it is no longer referenced.

-   <span class="function">shmop\_open</span> will now return a <span
    class="classname">Shmop</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">shmop\_close</span> function no longer
    has an effect, and is deprecated; instead the <span
    class="classname">Shmop</span> instance is automatically destroyed
    if it is no longer referenced.

-   <span class="function">socket\_create</span>, <span
    class="function">socket\_create\_listen</span>, <span
    class="function">socket\_accept</span>, <span
    class="function">socket\_import\_stream</span>, <span
    class="function">socket\_addrinfo\_connect</span>, <span
    class="function">socket\_addrinfo\_bind</span>, and <span
    class="function">socket\_wsaprotocol\_info\_import</span> will now
    return a <span class="classname">Socket</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    <span class="function">socket\_addrinfo\_lookup</span> will now
    return an array of <span class="classname">AddressInfo</span>
    objects rather than
    <a href="/language/types/resource.html" class="link">资源(resource)</a>s.

-   <span class="function">msg\_get\_queue</span> will now return an
    <span class="classname">SysvMessageQueue</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   <span class="function">sem\_get</span> will now return an <span
    class="classname">SysvSemaphore</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   <span class="function">shm\_attach</span> will now return an <span
    class="classname">SysvSharedMemory</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   <span class="function">xml\_parser\_create</span> and <span
    class="function">xml\_parser\_create\_ns</span> will now return an
    <span class="classname">XmlParser</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.
    The <span class="function">xml\_parser\_free</span> function no
    longer has an effect, instead the XmlParser instance is
    automatically destroyed if it is no longer referenced.

-   The
    <a href="/ref/xmlwriter.html" class="link">XMLWriter functions</a>
    now accept and return, respectively, <span
    class="classname">XMLWriter</span> objects instead of
    <a href="/language/types/resource.html" class="link">资源(resource)</a>s.

-   <span class="function">inflate\_init</span> will now return an <span
    class="classname">InflateContext</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

-   <span class="function">deflate\_init</span> will now return a <span
    class="classname">DeflateContext</span> object rather than a
    <a href="/language/types/resource.html" class="link">资源(resource)</a>.

### COM and .Net (Windows)

The ability to import case-insensitive constants from type libraries has
been removed. The second argument to <span
class="function">com\_load\_typelib</span> may no longer be false;
<a href="/com/setup.html#" class="link">com.autoregister_casesensitive</a>
may no longer be disabled; case-insensitive markers in
<a href="/com/setup.html#" class="link">com.typelib_file</a> are
ignored.

### CURL

**`CURLOPT_POSTFIELDS`** no longer accepts objects as arrays. To
interpret an object as an array, perform an explicit `(array)` cast. The
same applies to other options accepting arrays as well.

### Date and Time

<span class="function">mktime</span> and <span
class="function">gmmktime</span> now require at least one argument.
<span class="function">time</span> can be used to get the current
timestamp.

### DOM

Unimplemented classes from the DOM extension that had no behavior and
contained test data have been removed. These classes have also been
removed in the latest version of the DOM standard:

-   DOMNameList
-   DomImplementationList
-   DOMConfiguration
-   DomError
-   DomErrorHandler
-   DOMImplementationSource
-   DOMLocator
-   DOMUserDataHandler
-   DOMTypeInfo

### Enchant

-   <span class="function">enchant\_broker\_list\_dicts</span>, <span
    class="function">enchant\_broker\_describe</span> and <span
    class="function">enchant\_dict\_suggest</span> will now return an
    empty array instead of **`NULL`**.

### Exif

<span class="function">read\_exif\_data</span> has been removed; <span
class="function">exif\_read\_data</span> should be used instead.

### Filter

-   The **`FILTER_FLAG_SCHEME_REQUIRED`** and
    **`FILTER_FLAG_HOST_REQUIRED`** flags for the
    **`FILTER_VALIDATE_URL`** filter have been removed. The *scheme* and
    *host* are (and have been) always required.

-   The **`INPUT_REQUEST`** and **`INPUT_SESSION`** source for <span
    class="function">filter\_input</span> etc. have been removed. These
    were never implemented and their use always generated a warning.

### GD

-   The deprecated functions <span class="function">image2wbmp</span>
    has been removed.

-   The deprecated functions <span class="function">png2wbmp</span> and
    <span class="function">jpeg2wbmp</span> have been removed.

-   The default `mode` parameter of <span
    class="function">imagecropauto</span> no longer accepts *-1*.
    **`IMG_CROP_DEFAULT`** should be used instead.

-   On Windows, `php_gd2.dll` has been renamed to `php_gd.dll`.

### GMP

<span class="function">gmp\_random</span> has been removed. One of <span
class="function">gmp\_random\_range</span> or <span
class="function">gmp\_random\_bits</span> should be used instead.

### Iconv

iconv implementations which do not properly set `errno` in case of
errors are no longer supported.

### IMAP

-   The unused `default_host` argument of <span
    class="function">imap\_headerinfo</span> has been removed.

-   The <span class="function">imap\_header</span> function which is an
    alias of <span class="function">imap\_headerinfo</span> has been
    removed.

### Internationalization Functions

-   The deprecated constant **`INTL_IDNA_VARIANT_2003`** has been
    removed.

-   The deprecated **`Normalizer::NONE`** constant has been removed.

### LDAP

-   The deprecated functions <span class="function">ldap\_sort</span>,
    <span class="function">ldap\_control\_paged\_result</span> and <span
    class="function">ldap\_control\_paged\_result\_response</span> have
    been removed.

-   The interface of <span
    class="function">ldap\_set\_rebind\_proc</span> has changed; the
    `callback` parameter does not accept empty strings anymore;
    **`NULL`** should be used instead.

### MBString

-   The
    <a href="/mbstring/setup.html#" class="link">mbstring.func_overload</a>
    directive has been removed. The related **`MB_OVERLOAD_MAIL`**,
    **`MB_OVERLOAD_STRING`**, and **`MB_OVERLOAD_REGEX`** constants have
    also been removed. Finally, the *"func\_overload"* and
    *"func\_overload\_list"* entries in <span
    class="function">mb\_get\_info</span> have been removed.

-   <span class="function">mb\_parse\_str</span> can no longer be used
    without specifying a result array.

-   A number of deprecated mbregex aliases have been removed. See the
    following list for which functions should be used instead:

    -   <span class="function">mbregex\_encoding</span> → <span
        class="function">mb\_regex\_encoding</span>
    -   <span class="function">mbereg</span> → <span
        class="function">mb\_ereg</span>
    -   <span class="function">mberegi</span> → <span
        class="function">mb\_eregi</span>
    -   <span class="function">mbereg\_replace</span> → <span
        class="function">mb\_ereg\_replace</span>
    -   <span class="function">mberegi\_replace</span> → <span
        class="function">mb\_eregi\_replace</span>
    -   <span class="function">mbsplit</span> → <span
        class="function">mb\_split</span>
    -   <span class="function">mbereg\_match</span> → <span
        class="function">mb\_ereg\_match</span>
    -   <span class="function">mbereg\_search</span> → <span
        class="function">mb\_ereg\_search</span>
    -   <span class="function">mbereg\_search\_pos</span> → <span
        class="function">mb\_ereg\_search\_pos</span>
    -   <span class="function">mbereg\_search\_regs</span> → <span
        class="function">mb\_ereg\_search\_regs</span>
    -   <span class="function">mbereg\_search\_init</span> → <span
        class="function">mb\_ereg\_search\_init</span>
    -   <span class="function">mbereg\_search\_getregs</span> → <span
        class="function">mb\_ereg\_search\_getregs</span>
    -   <span class="function">mbereg\_search\_getpos</span> → <span
        class="function">mb\_ereg\_search\_getpos</span>
    -   <span class="function">mbereg\_search\_setpos</span> → <span
        class="function">mb\_ereg\_search\_setpos</span>

-   The *e* modifier for <span class="function">mb\_ereg\_replace</span>
    has been removed. <span
    class="function">mb\_ereg\_replace\_callback</span> should be used
    instead.

-   A non-string pattern argument to <span
    class="function">mb\_ereg\_replace</span> will now be interpreted as
    a string instead of an ASCII codepoint. The previous behavior may be
    restored with an explicit call to <span class="function">chr</span>.

-   The `needle` argument for <span class="function">mb\_strpos</span>,
    <span class="function">mb\_strrpos</span>, <span
    class="function">mb\_stripos</span>, <span
    class="function">mb\_strripos</span>, <span
    class="function">mb\_strstr</span>, <span
    class="function">mb\_stristr</span>, <span
    class="function">mb\_strrchr</span> and <span
    class="function">mb\_strrichr</span> can now be empty.

-   The `is_hex` parameter, which was not used internally, has been
    removed from <span
    class="function">mb\_decode\_numericentity</span>.

-   The legacy behavior of passing the encoding as the third argument
    instead of an offset for the <span
    class="function">mb\_strrpos</span> function has been removed; an
    explicit *0* offset with the encoding should be provided as the
    fourth argument instead.

-   The *ISO\_8859-\** character encoding aliases have been replaced by
    *ISO8859-\** aliases for better interoperability with the iconv
    extension. The mbregex ISO 8859 aliases with underscores
    (*ISO\_8859\_\** and *ISO8859\_\**) have also been removed.

-   <span class="function">mb\_ereg</span> and <span
    class="function">mb\_eregi</span> will now return boolean **`TRUE`**
    on a successfuly match. Previously they returned integer *1* if
    `matches` was not passed, or `max(1, strlen($matches[0]))` if
    `matches` was passed.

### OCI8

-   The <span class="classname">OCI-Lob</span> class is now called <span
    class="classname">OCILob</span>, and the <span
    class="classname">OCI-Collection</span> class is now called <span
    class="classname">OCICollection</span> for name compliance enforced
    by PHP 8 arginfo type annotation tooling.

-   Several alias functions have been marked as deprecated.

-   <span class="function">oci\_internal\_debug</span> and its alias
    <span class="function">ociinternaldebug</span> have been removed.

### ODBC

-   <span class="function">odbc\_connect</span> no longer reuses
    connections.

-   The unused `flags` parameter of <span
    class="function">odbc\_exec</span> has been removed.

### OpenSSL

-   <span class="function">openssl\_seal</span> and <span
    class="function">openssl\_open</span> now require `method` to be
    passed, as the previous default of *"RC4"* is considered insecure.

### Regular Expressions (Perl-Compatible)

When passing invalid escape sequences they are no longer interpreted as
literals. This behavior previously required the *X* modifier – which is
now ignored.

### PHP Data Objects

-   The default error handling mode has been changed from "silent" to
    "exceptions". See
    <a href="/book/pdo.html#错误与错误处理" class="link">Errors and error handling</a>
    for details.

-   The signatures of some PDO methods have changed:

    -   `PDO::query(string $query, ?int $fetchMode  = null, mixed  ...$fetchModeArgs)`
    -   `PDOStatement::setFetchMode(int $mode, mixed ...$args)`

### PDO ODBC

The `php.ini` directive
<a href="/book/pdo.html#" class="link">pdo_odbc.db2_instance_name</a>
has been removed.

### PostgreSQL

-   The deprecated <span class="function">pg\_connect</span> syntax
    using multiple parameters instead of a connection string is no
    longer supported.

-   The deprecated <span class="function">pg\_lo\_import</span> and
    <span class="function">pg\_lo\_export</span> signature that passes
    the connection as the last argument is no longer supported. The
    connection should be passed as first argument instead.

-   <span class="function">pg\_fetch\_all</span> will now return an
    empty array instead of **`FALSE`** for result sets with zero rows.

### Phar

Metadata associated with a phar will no longer be automatically
unserialized, to fix potential security vulnerabilities due to object
instantiation, autoloading, etc.

### Reflection

-   The method signatures

    -   `ReflectionClass::newInstance($args)`
    -   `ReflectionFunction::invoke($args)`
    -   `ReflectionMethod::invoke($object, $args)`

    have been changed to:

    -   `ReflectionClass::newInstance(...$args)`
    -   `ReflectionFunction::invoke(...$args)`
    -   `ReflectionMethod::invoke($object, ...$args)`

    Code that must be compatible with both PHP 7 and PHP 8 can use the
    following signatures to be compatible with both versions:

    -   `ReflectionClass::newInstance($arg = null, ...$args)`
    -   `ReflectionFunction::invoke($arg = null, ...$args)`
    -   `ReflectionMethod::invoke($object, $arg = null, ...$args)`

-   The <span class="methodname">ReflectionType::\_\_toString</span>
    method will now return a complete debug representation of the type,
    and is no longer deprecated. In particular the result will include a
    nullability indicator for nullable types. The format of the return
    value is not stable and may change between PHP versions.

-   Reflection export() methods have been removed. Instead reflection
    objects can be cast to string.

-   <span class="methodname">ReflectionMethod::isConstructor</span> and
    <span class="methodname">ReflectionMethod::isDestructor</span> now
    also return **`TRUE`** for
    <a href="/language/oop5/decon.html#object.construct" class="link">__construct()</a>
    and
    <a href="/language/oop5/decon.html#object.destruct" class="link">__destruct()</a>
    methods of interfaces. Previously, this would only be true for
    methods of classes and traits.

-   <span class="methodname">ReflectionType::isBuiltin</span> method has
    been moved to <span class="classname">ReflectionNamedType</span>.
    <span class="classname">ReflectionUnionType</span> does not have it.

### Sockets

-   The deprecated **`AI_IDN_ALLOW_UNASSIGNED`** and
    **`AI_IDN_USE_STD3_ASCII_RULES`** `flags` for <span
    class="function">socket\_addrinfo\_lookup</span> have been removed.

### Standard PHP Library (SPL)

-   <span class="methodname">SplFileObject::fgetss</span> has been
    removed.

-   <span class="methodname">SplHeap::compare</span> now specifies a
    method signature. Inheriting classes implementing this method will
    now have to use a compatible method signature.

-   <span class="methodname">SplDoublyLinkedList::push</span>, <span
    class="methodname">SplDoublyLinkedList::unshift</span> and <span
    class="methodname">SplQueue::enqueue</span> now return <span
    class="type">void</span> instead of **`TRUE`**.

-   <span class="function">spl\_autoload\_register</span> will now
    always throw a <span class="classname">TypeError</span> on invalid
    arguments, therefore the second argument `do_throw` is ignored and a
    notice will be emitted if it is set to **`FALSE`**.

-   <span class="classname">SplFixedArray</span> is now an <span
    class="interfacename">IteratorAggregate</span> and not an <span
    class="interfacename">Iterator</span>. <span
    class="methodname">SplFixedArray::rewind</span>, <span
    class="methodname">SplFixedArray::current</span>, <span
    class="methodname">SplFixedArray::key</span>, <span
    class="methodname">SplFixedArray::next</span>, and <span
    class="methodname">SplFixedArray::valid</span> have been removed. In
    their place, <span
    class="methodname">SplFixedArray::getIterator</span> has been added.
    Any code which uses explicit iteration over SplFixedArray must now
    obtain an <span class="interfacename">Iterator</span> through <span
    class="methodname">SplFixedArray::getIterator</span>. This means
    that <span class="classname">SplFixedArray</span> is now safe to use
    in nested loops.

### Standard Library

-   <span class="function">assert</span> will no longer evaluate string
    arguments, instead they will be treated like any other argument.
    `assert($a == $b)` should be used instead of `assert('$a == $b')`.
    The <a href="/info/setup.html#" class="link">assert.quiet_eval</a>
    ini directive and the **`ASSERT_QUIET_EVAL`** constant have also
    been removed, as they would no longer have any effect.

-   <span class="function">parse\_str</span> can no longer be used
    without specifying a result array.

-   The
    <a href="/filters/string/strip_tags.html" class="link">string.strip_tags</a>
    filter has been removed.

-   The `needle` argument of <span class="function">strpos</span>, <span
    class="function">strrpos</span>, <span
    class="function">stripos</span>, <span
    class="function">strripos</span>, <span
    class="function">strstr</span>, <span
    class="function">strchr</span>, <span
    class="function">strrchr</span>, and <span
    class="function">stristr</span> will now always be interpreted as a
    string. Previously non-string needles were interpreted as an ASCII
    code point. An explicit call to <span class="function">chr</span>
    can be used to restore the previous behavior.

-   The `needle` argument for <span class="function">strpos</span>,
    <span class="function">strrpos</span>, <span
    class="function">stripos</span>, <span
    class="function">strripos</span>, <span
    class="function">strstr</span>, <span
    class="function">stristr</span> and <span
    class="function">strrchr</span> can now be empty.

-   The `length` argument for <span class="function">substr</span>,
    <span class="function">substr\_count</span>, <span
    class="function">substr\_compare</span>, and <span
    class="function">iconv\_substr</span> can now be **`NULL`**.
    **`NULL`** values will behave as if no length argument was provided
    and will therefore return the remainder of the string instead of an
    empty string.

-   The `length` argument for <span
    class="function">array\_splice</span> can now be **`NULL`**.
    **`NULL`** values will behave identically to omitting the argument,
    thus removing everything from the `offset` to the end of the array.

-   The `args` argument of <span class="function">vsprintf</span>, <span
    class="function">vfprintf</span>, and <span
    class="function">vprintf</span> must now be an array. Previously any
    type was accepted.

-   The *'salt'* option of <span class="function">password\_hash</span>
    is no longer supported. If the *'salt'* option is used a warning is
    generated, the provided salt is ignored, and a generated salt is
    used instead.

-   The <span class="function">quotemeta</span> function will now return
    an empty string if an empty string was passed. Previously
    **`FALSE`** was returned.

-   The following functions have been removed:

    -   <span class="function">hebrevc</span>
    -   <span class="function">convert\_cyr\_string</span>
    -   <span class="function">money\_format</span>
    -   <span class="function">ezmlm\_hash</span>
    -   <span class="function">restore\_include\_path</span>
    -   <span class="function">get\_magic\_quotes\_gpc</span>
    -   <span class="function">get\_magic\_quotes\_runtime</span>
    -   <span class="function">fgetss</span>

-   **`FILTER_SANITIZE_MAGIC_QUOTES`** has been removed.

-   Calling <span class="function">implode</span> with parameters in a
    reverse order `($pieces,      $glue)` is no longer supported.

-   <span class="function">parse\_url</span> will now distinguish absent
    and empty queries and fragments:

    -   `http://example.com/foo → query = null, fragment = null`
    -   `http://example.com/foo? → query = "",   fragment = null`
    -   `http://example.com/foo# → query = null, fragment = ""`
    -   `http://example.com/foo?# → query = "",   fragment = ""`

    Previously all cases resulted in query and fragment being
    **`NULL`**.

-   <span class="function">var\_dump</span> and <span
    class="function">debug\_zval\_dump</span> will now print
    floating-point numbers using
    <a href="/ini/core.html#ini.serialize-precision" class="link">serialize_precision</a>
    rather than
    <a href="/ini/core.html#ini.precision" class="link">precision</a>.
    In a default configuration, this means that floating-point numbers
    are now printed with full accuracy by these debugging functions.

-   If the array returned by
    <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
    contains non-existing properties, these are now silently ignored.
    Previously, such properties would have been serialized as if they
    had the value **`NULL`**.

-   The default locale on startup is now always *"C"*. No locales are
    inherited from the environment by default. Previously, **`LC_ALL`**
    was set to *"C"*, while **`LC_CTYPE`** was inherited from the
    environment. However, some functions did not respect the inherited
    locale without an explicit <span class="function">setlocale</span>
    call. An explicit <span class="function">setlocale</span> call is
    now always required if a locale component should be changed from the
    default.

-   The deprecated DES fallback in <span class="function">crypt</span>
    has been removed. If an unknown salt format is passed to <span
    class="function">crypt</span>, the function will fail with *\*0*
    instead of falling back to a weak DES hash now.

-   Specifying out of range rounds for SHA256/SHA512 <span
    class="function">crypt</span> will now fail with *\*0* instead of
    clamping to the closest limit. This matches glibc behavior.

-   The result of sorting functions may have changed, if the array
    contains elements that compare as equal.

-   Any functions accepting callbacks that are not explicitly specified
    to accept parameters by reference will now warn if a callback with
    reference parameters is used. Examples include <span
    class="function">array\_filter</span> and <span
    class="function">array\_reduce</span>. This was already the case for
    most, but not all, functions previously.

-   The HTTP stream wrapper as used by functions like <span
    class="function">file\_get\_contents</span> now advertises HTTP/1.1
    rather than HTTP/1.0 by default. This does not change the behavior
    of the client, but may cause servers to respond differently. To
    retain the old behavior, set the *'protocol\_version'* stream
    context option, e.g.

    ``` php
    <?php
    $ctx = stream_context_create(['http' => ['protocol_version' => '1.0']]);
    echo file_get_contents('http://example.org', false, $ctx);
    ?>
    ```

-   Calling <span class="function">crypt</span> without an explicit salt
    is no longer supported. If you would like to produce a strong hash
    with an auto-generated salt, use <span
    class="function">password\_hash</span> instead.

-   <span class="function">substr</span>, <span
    class="function">mb\_substr</span>, <span
    class="function">iconv\_substr</span> and <span
    class="function">grapheme\_substr</span> now consistently clamp
    out-of-bounds offsets to the string boundary. Previously,
    **`FALSE`** was returned instead of the empty string in some cases.

-   On Windows, the program execution functions (<span
    class="function">proc\_open</span>, <span
    class="function">exec</span>, <span class="function">popen</span>
    etc.) using the shell, now consistently execute **%comspec% /s /c
    "$commandline"**, which has the same effect as executing
    **$commandline** (without additional quotes).

### Sysvsem

-   The `auto_release` parameter of <span
    class="function">sem\_get</span> was changed to accept bool values
    rather than int.

### Tidy

-   The `use_include_path` parameter, which was not used internally, has
    been removed from <span
    class="function">tidy\_repair\_string</span>.

-   <span class="methodname">tidy::repairString</span> and <span
    class="methodname">tidy::repairFile</span> became static methods.

### Tokenizer

-   *T\_COMMENT* tokens will no longer include a trailing newline. The
    newline will instead be part of a following *T\_WHITESPACE* token.
    It should be noted that *T\_COMMENT* is not always followed by
    whitespace, it may also be followed by *T\_CLOSE\_TAG* or
    end-of-file.

-   Namespaced names are now represented using the *T\_NAME\_QUALIFIED*
    (`Foo\Bar`), *T\_NAME\_FULLY\_QUALIFIED* (`\Foo\Bar`) and
    *T\_NAME\_RELATIVE* (`namespace\Foo\Bar`) tokens. *T\_NS\_SEPARATOR*
    is only used for standalone namespace separators, and only
    syntactially valid in conjunction with group use declarations.

### XMLReader

<span class="methodname">XMLReader::open</span> and <span
class="methodname">XMLReader::xml</span> are now static methods. They
can still be called as instance methods, but inheriting classes need to
declare them as static if they override these methods.

### XML-RPC

The XML-RPC extension has been moved to PECL and is no longer part of
the PHP distribution.

### Zip

**`ZipArchive::OPSYS_Z_CPM`** has been removed (this name was a typo).
Use **`ZipArchive::OPSYS_CPM`** instead.

### Zlib

-   <span class="function">gzgetss</span> has been removed.

-   <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>
    is no longer automatically disabled for *Content-Type: image/\**.

### Windows PHP Test Packs

The test runner has been renamed from `run-test.php` to `run-tests.php`,
to match its name in php-src.
