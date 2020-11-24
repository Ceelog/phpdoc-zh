其他变更
--------

### Changes in SAPI Modules

#### Apache2Handler

The PHP module has been renamed from *php7\_module* to *php\_module*.

### Changed Functions

#### Reflection

<span class="methodname">ReflectionClass::getConstants</span> and <span
class="methodname">ReflectionClass::getReflectionConstants</span>
results can be now filtered via a new parameter `filter`. Three new
constants were added to be used with it:

-   **`ReflectionClassConstant::IS_PUBLIC`**
-   **`ReflectionClassConstant::IS_PROTECTED`**
-   **`ReflectionClassConstant::IS_PRIVATE`**

#### Zip

-   The <span class="methodname">ZipArchive::addGlob</span> and <span
    class="methodname">ZipArchive::addPattern</span> methods accept more
    values in the `options` array argument:

    -   *flags*
    -   *comp\_method*
    -   *comp\_flags*
    -   *env\_method*
    -   *enc\_password*

-   <span class="methodname">ZipArchive::addEmptyDir</span>, <span
    class="methodname">ZipArchive::addFile</span> and <span
    class="methodname">ZipArchive::addFromString</span> methods have a
    new `flags` argument. This allows managing name encoding
    (**`ZipArchive::FL_ENC_*`**) and entry replacement
    (**`ZipArchive::FL_OVERWRITE`**).

-   <span class="methodname">ZipArchive::extractTo</span> now restores
    the file modification time.

### Other Changes to Extensions

#### CURL

-   The CURL extension now requires at least libcurl 7.29.0.

-   The deprecated parameter `version` of <span
    class="function">curl\_version</span> has been removed.

#### Date and Time

<span class="classname">DatePeriod</span> now implements <span
class="interfacename">IteratorAggregate</span> (instead of <span
class="interfacename">Traversable</span>).

#### DOM

<span class="classname">DOMNamedNodeMap</span> and <span
class="classname">DOMNodeList</span> now implement <span
class="interfacename">IteratorAggregate</span> (instead of <span
class="interfacename">Traversable</span>).

#### Intl

<span class="classname">IntlBreakIterator</span> and <span
class="classname">ResourceBundle</span> now implement <span
class="interfacename">IteratorAggregate</span> (instead of <span
class="interfacename">Traversable</span>).

#### Enchant

The enchant extension now uses libenchant-2 by default when available.
libenchant version 1 is still supported but is deprecated and could be
removed in the future.

#### GD

-   The `num_points` parameter of <span
    class="function">imagepolygon</span>, <span
    class="function">imageopenpolygon</span> and <span
    class="function">imagefilledpolygon</span> is now optional, i.e.
    these functions may be called with either 3 or 4 arguments. If the
    argument is omitted, it is calculated as `count($points)/2`.

-   The function <span class="function">imagegetinterpolation</span> to
    get the current interpolation method has been added.

#### JSON

The JSON extension cannot be disabled anymore and is always an integral
part of any PHP build, similar to the date extension.

#### MBString

The Unicode data tables have been updated to version 13.0.0.

#### PDO

<span class="classname">PDOStatement</span> now implements <span
class="interfacename">IteratorAggregate</span> (instead of <span
class="interfacename">Traversable</span>).

#### LibXML

The minimum required libxml version is now 2.9.0. This means that
external entity loading is now guaranteed to be disabled by default, and
no extra steps need to be taken to protect against XXE attacks.

#### MySQLi / PDO MySQL

-   When mysqlnd is not used (which is the default and recommended
    option), the minimum supported libmysqlclient version is now 5.5.

-   <span class="classname">mysqli\_result</span> now implements <span
    class="interfacename">IteratorAggregate</span> (instead of <span
    class="interfacename">Traversable</span>).

#### PGSQL / PDO PGSQL

The PGSQL and PDO PGSQL extensions now require at least libpq 9.1.

#### Readline

Calling <span class="function">readline\_completion\_function</span>
before the interactive prompt starts (e.g. in
<a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a>)
will now override the default interactive prompt completion function.
Previously, <span class="function">readline\_completion\_function</span>
only worked when called after starting the interactive prompt.

#### SimpleXML

<span class="classname">SimpleXMLElement</span> now implements <span
class="interfacename">RecursiveIterator</span> and absorbed the
functionality of <span class="classname">SimpleXMLIterator</span>. <span
class="classname">SimpleXMLIterator</span> is an empty extension of
<span class="classname">SimpleXMLElement</span>.

### Changes to INI File Handling

-   com.dotnet\_version is a new INI directive to choose the version of
    the .NET framework to use for <span class="classname">dotnet</span>
    objects.

-   zend.exception\_string\_param\_max\_len is a new INI directive to
    set the maximum string length in an argument of a stringified stack
    strace.

### EBCDIC

EBCDIC targets are no longer supported, though it's unlikely that they
were still working in the first place.

### Performance

-   A Just-In-Time (JIT) compiler has been added to the opcache
    extension.

-   <span class="function">array\_slice</span> on an array without gaps
    will no longer scan the whole array to find the start offset. This
    may significantly reduce the runtime of the function with large
    offsets and small lengths.

-   <span class="function">strtolower</span> now uses a SIMD
    implementation when using the *"C"* **`LC_CTYPE`** locale (which is
    the default).
