Other Changes
-------------

### PHP Core

#### Set(raw)cookie accepts $option Argument

<span class="function">setcookie</span> and <span
class="function">setrawcookie</span> now also support the following
signature:

<span class="type">bool</span> <span class="methodname">setcookie</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$value`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">array</span> `$options`<span class="initializer"> =
\[\]</span></span> \]\] )

where *$options* is an associative array which may have any of the keys
*"expires"*, *"path"*, *"domain"*, *"secure"*, *"httponly"* and
*"samesite"*.

#### New Syslog ini Directives

The following ini Directives have been added to customize logging, if
<a href="/errorfunc/setup.html#" class="link">error_log</a> is set to
*syslog*:

<a href="/errorfunc/setup.html#" class="link">syslog.facility</a>  
<span class="simpara"> Specifies what type of program is logging the
message. </span>

<a href="/errorfunc/setup.html#" class="link">syslog.filter</a>  
<span class="simpara"> Specifies the filter type to filter the logged
messages. There are three supported filter types - *all*, *no-ctrl* and
*ascii*. </span>

<a href="/errorfunc/setup.html#" class="link">syslog.ident</a>  
<span class="simpara"> Specifies the ident string which is prepended to
every message. </span>

#### Garbage Collection

The
<a href="/features/gc/collecting-cycles.html" class="link">cyclic GC</a>
has been enhanced, which may result in considerable performance
improvements.

#### Miscellaneous

<span class="function">var\_export</span> now exports <span
class="classname">stdClass</span> objects as an array cast to an object
(`(object) array( ... )`), rather than using the nonexistent method
<span class="methodname">stdClass::\_\_setState</span>.

<span class="function">debug\_zval\_dump</span> was changed to display
recursive arrays and objects in the same way as <span
class="function">var\_dump</span>. Now, it doesn't display them twice.

<span class="function">array\_push</span> and <span
class="function">array\_unshift</span> can now also be called with a
single argument, which is particularly convenient wrt. the spread
operator.

### Interactive PHP Debugger

The unused constants **`PHPDBG_FILE`**, **`PHPDBG_METHOD`**,
**`PHPDBG_LINENO`** and **`PHPDBG_FUNC`** have been removed.

### FastCGI Process Manager

The <span class="function">getallheaders</span> function is now also
available.

### Client URL Library

libcurl ≥ 7.15.5 is now required.

### Data Filtering

**`FILTER_VALIDATE_FLOAT`** now also supports a *thousand* option, which
defines the set of allowed thousand separator chars. The default
(`"',."`) is fully backward compatible with former PHP versions.

**`FILTER_SANITIZE_ADD_SLASHES`** has been added as an alias of the
*magic\_quotes* filter (**`FILTER_SANITIZE_MAGIC_QUOTES`**). The
*magic\_quotes* filter is subject to removal in future versions of PHP.

### FTP

The default transfer mode has been changed to *binary*.

### Internationalization Functions

**`Normalizer::NONE`** is deprecated, when PHP is linked with ICU ≥ 56.

Introduced **`Normalizer::FORM_KC_CF`** as <span
class="methodname">Normalizer::normalize</span> argument for
*NFKC\_Casefold* normalization; available when linked with ICU ≥ 56.

### JavaScript Object Notation

A new flag has been added, **`JSON_THROW_ON_ERROR`**, which can be used
with <span class="function">json\_decode</span> or <span
class="function">json\_encode</span> and causes these functions to throw
the new <span class="classname">JsonException</span> upon an error,
instead of setting the global error state that is retrieved with <span
class="function">json\_last\_error</span> and <span
class="function">json\_last\_error\_msg</span>.
**`JSON_PARTIAL_OUTPUT_ON_ERROR`** takes precedence over
**`JSON_THROW_ON_ERROR`**.

### Multibyte String

The configuration option **--with-libmbfl** is no longer available.

### ODBC (Unified)

Support for *ODBCRouter* and *Birdstep* including the
*birdstep.max\_links* ini directive has been removed.

### OPcache

The *opcache.inherited\_hack* ini directive has been removed. The value
has already been ignored since PHP 5.3.0.

### OpenSSL

The *min\_proto\_version* and *max\_proto\_version* ssl stream options
as well as related constants for possible TLS protocol values have been
added.

### Regular Expressions (Perl-Compatible)

The <a href="/book/pcre.html" class="link">PCRE extension</a> has been
upgraded to PCRE2, which may cause minor behavioral changes (for
instance, character ranges in classes are now more strictly
interpreted), and augments the existing regular expression syntax.

<span class="function">preg\_quote</span> now also escapes the *'\#'*
character.

### Microsoft SQL Server and Sybase Functions (PDO\_DBLIB)

The attribute **`PDO::DBLIB_ATTR_SKIP_EMPTY_ROWSETS`** to enable
automatic skipping of empty rowsets has been added.

The **`PDO::DBLIB_ATTR_TDS_VERSION`** attribute which exposes the TDS
version has been added.

DATETIME2 columns are now treated like DATETIME columns.

### SQLite Functions (PDO\_SQLITE)

SQLite3 databases can now be opened in read-only mode by setting the new
**`PDO::SQLITE_ATTR_OPEN_FLAGS`** attribute to
**`PDO::SQLITE_OPEN_READONLY`**.

### Session Handling

<span class="function">session\_set\_cookie\_params</span> now also
supports the following signature:

<span class="type">bool</span> <span
class="methodname">session\_set\_cookie\_params</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

where *$options* is an associative array which may have any of the keys
*"lifetime"*, *"path"*, *"domain"*, *"secure"*, *"httponly"* and
*"samesite"*. Accordingly, the return value of <span
class="function">session\_get\_cookie\_params</span> now also has an
element with the key *"samesite"*. Furthermore, the new
*session.cookie\_samesite* ini option to set the default of the SameSite
directive for cookies has been added. It defaults to *""* (empty
string), so no SameSite directive is set. Can be set to *"Lax"* or
*"Strict"*, which sets the respective SameSite directive.

### Tidy

Building against
<a href="https://github.com/petdance/tidyp" class="link external">» tidyp</a>
is now also supported transparently. Since tidyp offers no API to get
the release date, <span class="function">tidy\_get\_release</span> and
<span class="methodname">tidy::getRelease</span> return *'unknown'* in
this case.

### XML Parser

The return value of the <span
class="function">xml\_set\_external\_entity\_ref\_handler</span>
callback is no longer ignored if the extension has been built against
libxml. Formerly, the return value has been ignored, and parsing did
never stop.

### Zip

Building against the bundled libzip is discouraged, but still possible
by adding **--without-libzip** to the configuration.

### Zlib Compression

The zlib/level context option for the
<a href="/wrappers/compression.html" class="link">compress.zlib wrapper</a>
to facilitate setting the desired compression level has been added.
