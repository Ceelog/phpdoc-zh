New Features
------------

### PHP Core

#### More Flexible Heredoc and Nowdoc Syntax

The closing marker for doc strings is no longer required to be followed
by a semicolon or newline. Additionally the closing marker may be
indented, in which case the indentation will be stripped from all lines
in the doc string.

#### Array Destructuring supports Reference Assignments

Array destructuring now supports reference assignments using the syntax
*\[&$a, \[$b, &$c\]\] = $d*. The same is also supported for <span
class="function">list</span>.

#### Instanceof Operator accepts Literals

*instanceof* now allows literals as the first operand, in which case the
result is always **`FALSE`**.

#### CompileError Exception instead of some Compilation Errors

A new <span class="classname">CompileError</span> exception has been
added, from which <span class="classname">ParseError</span> inherits. A
small number of compilation errors will now throw a <span
class="classname">CompileError</span> instead of generating a fatal
error. Currently this only affects compilation errors that may be thrown
by <span class="function">token\_get\_all</span> in **`TOKEN_PARSE`**
mode, but more errors may be converted in the future.

#### Trailing Commas are allowed in Calls

Trailing commas in function and method calls are now allowed.

#### Argon2id Support

The **--with-password-argon2\[=dir\]** configure argument now provides
support for both Argon2i and Argon2id hashes in the <span
class="function">password\_hash</span>, <span
class="function">password\_verify</span>, <span
class="function">password\_get\_info</span>, and <span
class="function">password\_needs\_rehash</span> functions. Passwords may
be hashed and verified using the **`PASSWORD_ARGON2ID`** constant.
Support for both Argon2i and Argon2id in the <span
class="function">password\_\*</span> functions now requires PHP be
linked against libargon2 reference library ≥ 20161029.

### FastCGI Process Manager

New options have been added to customize the FPM logging:

*log\_limit*  
<span class="simpara"> This global option can be used for setting the
log limit for the logged line which allows to log messages longer than
1024 characters without wrapping. It also fixes various wrapping issues.
</span>

*log\_buffering*  
<span class="simpara"> This global option allows an experimental logging
without extra buffering. </span>

*decorate\_workers\_output*  
<span class="simpara"> This pool option allows to disable the output
decoration for workers output when *catch\_workers\_output* is enabled.
</span>

### BC Math Functions

<span class="function">bcscale</span> can now also be used as getter to
retrieve the current scale in use.

### Lightweight Directory Access Protocol

Full support for LDAP Controls has been added to the
<a href="/book/ldap.html" class="link">LDAP</a> querying functions and
<span class="function">ldap\_parse\_result</span>:

-   <span class="simpara"> A *$serverctrls* parameter to send controls
    to the server in <span class="function">ldap\_add</span>, <span
    class="function">ldap\_mod\_replace</span>, <span
    class="function">ldap\_mod\_add</span>, <span
    class="function">ldap\_mod\_del</span>, <span
    class="function">ldap\_rename</span>, <span
    class="function">ldap\_compare</span>, <span
    class="function">ldap\_delete</span>, <span
    class="function">ldap\_modify\_batch</span>, <span
    class="function">ldap\_search</span>, <span
    class="function">ldap\_list</span> and <span
    class="function">ldap\_read</span> has been added. </span>
-   <span class="simpara"> The out parameter *$serverctrls* to get
    controls from the server in <span
    class="function">ldap\_parse\_result</span> has been added. </span>
-   <span class="simpara"> Support for **`LDAP_OPT_SERVER_CONTROLS`**
    and **`LDAP_OPT_CLIENT_CONTROLS`** in <span
    class="function">ldap\_get\_option</span> and <span
    class="function">ldap\_set\_option</span> has been fixed. </span>

### Multibyte String Functions

#### Full Case-Mapping and Case-Folding Support

Support for full case-mapping and case-folding has been added. Unlike
simple case-mapping, full case-mapping may change the length of the
string. For example:

``` php
<?php
mb_strtoupper("Straße");
// Produces STRAßE on PHP 7.2
// Produces STRASSE on PHP 7.3
?>
```

The different casing mapping and folding modes are available through
<span class="function">mb\_convert\_case</span>:

-   <span class="simpara"> **`MB_CASE_LOWER`** (used by <span
    class="function">mb\_strtolower</span>) </span>
-   <span class="simpara"> **`MB_CASE_UPPER`** (used by <span
    class="function">mb\_strtoupper</span>) </span>
-   <span class="simpara"> **`MB_CASE_TITLE`** </span>
-   <span class="simpara"> **`MB_CASE_FOLD`** </span>
-   <span class="simpara"> **`MB_CASE_LOWER_SIMPLE`** </span>
-   <span class="simpara"> **`MB_CASE_UPPER_SIMPLE`** </span>
-   <span class="simpara"> **`MB_CASE_TITLE_SIMPLE`** </span>
-   <span class="simpara"> **`MB_CASE_FOLD_SIMPLE`** (used by
    case-insensitive operations) </span>

Only unconditional, language agnostic full case-mapping is performed.

#### Case-Insensitive String Operations use Case-Folding

Case-insensitive string operations now use case-folding instead of case-
mapping during comparisons. This means that more characters will be
considered (case insensitively) equal now.

#### MB\_CASE\_TITLE performs Title-Case Conversion

<span class="function">mb\_convert\_case</span> with **`MB_CASE_TITLE`**
now performs title-case conversion based on the Cased and CaseIgnorable
derived Unicode properties. In particular this also improves handling of
quotes and apostrophes.

#### Unicode 11 Support

The <a href="/book/mbstring.html" class="link">Multibyte String</a> data
tables have been updated for Unicode 11.

#### Long String Support

The
<a href="/ref/mbstring.html" class="link">Multibyte String Functions</a>
now correctly support strings larger than 2GB.

#### Performance Improvements

Performance of the
<a href="/book/mbstring.html" class="link">Multibyte String</a>
extension has been significantly improved across the board. The largest
improvements are in case conversion functions.

#### Named Captures Support

The *mb\_ereg\_\** functions now support named captures. Matching
functions like <span class="function">mb\_ereg</span> will now return
named captures both using their group number and their name, similar to
PCRE:

``` php
<?php
mb_ereg('(?<word>\w+)', '国', $matches);
// => [0 => "国", 1 => "国", "word" => "国"];
?>
```

Additionally, <span class="function">mb\_ereg\_replace</span> now
supports the `\k<>` and `\k''` notations to reference named captures in
the replacement string:

``` php
<?php
mb_ereg_replace('\s*(?<word>\w+)\s*', "_\k<word>_\k'word'_", ' foo ');
// => "_foo_foo_"
?>
```

`\k<>` and `\k''` can also be used for numbered references, which also
works with group numbers greater than 9.

### Readline

Support for the *completion\_append\_character* and
*completion\_suppress\_append* options has been added to <span
class="function">readline\_info</span>. These options are only available
if PHP is linked against libreadline (rather than libedit).
