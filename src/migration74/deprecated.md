Deprecated Features
-------------------

### PHP Core

#### Nested ternary operators without explicit parentheses

Nested ternary operations must explicitly use parentheses to dictate the
order of the operations. Previously, when used without parentheses, the
left-associativity would not result in the expected behaviour in most
cases.

``` php
<?php
1 ? 2 : 3 ? 4 : 5;   // deprecated
(1 ? 2 : 3) ? 4 : 5; // ok
1 ? 2 : (3 ? 4 : 5); // ok
?>
```

#### Array and string offset access using curly braces

The array and string offset access syntax using curly braces is
deprecated. Use *$var\[$idx\]* instead of *$var{$idx}*.

#### (real) cast and <span class="function">is\_real</span> function

The *(real)* cast is deprecated, use *(float)* instead.

The <span class="function">is\_real</span> function is also deprecated,
use <span class="function">is\_float</span> instead.

#### Unbinding *$this* when *$this* is used

Unbinding *$this* of a non-static closure that uses *$this* is
deprecated.

#### *parent* keyword without parent class

Using *parent* inside a class without a parent is deprecated, and will
throw a compile-time error in the future. Currently an error will only
be generated if/when the parent is accessed at run-time.

#### allow\_url\_include INI option

The <a href="/filesystem/setup.html#" class="link">allow_url_include</a>
ini directive is deprecated. Enabling it will generate a deprecation
notice at startup.

#### Invalid characters in base conversion functions

Passing invalid characters to <span
class="function">base\_convert</span>, <span
class="function">bindec</span>, <span class="function">octdec</span> and
<span class="function">hexdec</span> will now generate a deprecation
notice. The result will still be computed as if the invalid characters
did not exist. Leading and trailing whitespace, as well as prefixes of
type 0x (depending on base) continue to be allowed.

#### Using <span class="function">array\_key\_exists</span> on objects

Using <span class="function">array\_key\_exists</span> on objects is
deprecated. Instead either <span class="function">isset</span> or <span
class="function">property\_exists</span> should be used.

#### Magic quotes functions

The <span class="function">get\_magic\_quotes\_gpc</span> and <span
class="function">get\_magic\_quotes\_runtime</span> functions are
deprecated. They always return **`FALSE`**.

#### <span class="function">hebrevc</span> function

The <span class="function">hebrevc</span> function is deprecated. It can
be replaced with *nl2br(hebrev($str))* or, preferably, the use of
Unicode RTL support.

#### <span class="function">convert\_cyr\_string</span> function

The <span class="function">convert\_cyr\_string</span> function is
deprecated. It can be replaced by one of <span
class="function">mb\_convert\_string</span>, <span
class="function">iconv</span> or <span
class="classname">UConverter</span>.

#### <span class="function">money\_format</span> function

The <span class="function">money\_format</span> function is deprecated.
It can be replaced by the intl <span
class="classname">NumberFormatter</span> functionality.

#### <span class="function">ezmlm\_hash</span> function

The <span class="function">ezmlm\_hash</span> function is deprecated.

#### <span class="function">restore\_include\_path</span> function

The <span class="function">restore\_include\_path</span> function is
deprecated. It can be replaced by *ini\_restore('include\_path')*.

#### Implode with historical parameter order

Passing parameters to <span class="function">implode</span> in reverse
order is deprecated, use *implode($glue, $parts)* instead of
*implode($parts, $glue)*.

### COM

Importing type libraries with case-insensitive constant registering has
been deprecated.

### Filter

**`FILTER_SANITIZE_MAGIC_QUOTES`** is deprecated, use
**`FILTER_SANITIZE_ADD_SLASHES`** instead.

### Multibyte String

Passing a non-string pattern to <span
class="function">mb\_ereg\_replace</span> is deprecated. Currently,
non-string patterns are interpreted as ASCII codepoints. In PHP 8, the
pattern will be interpreted as a string instead.

Passing the encoding as 3rd parameter to <span
class="function">mb\_strrpos</span> is deprecated. Instead pass a 0
offset, and encoding as 4th parameter.

### Lightweight Directory Access Protocol

<span class="function">ldap\_control\_paged\_result\_response</span> and
<span class="function">ldap\_control\_paged\_result</span> are
deprecated. Pagination controls can be sent along with <span
class="function">ldap\_search</span> instead.

### Reflection

Calls to <span class="methodname">ReflectionType::\_\_toString</span>
now generate a deprecation notice. This method has been deprecated in
favor of <span class="methodname">ReflectionNamedType::getName</span> in
the documentation since PHP 7.1, but did not throw a deprecation notice
for technical reasons.

The *export()* methods on all <span class="classname">Reflection</span>
classes are deprecated. Construct a <span
class="classname">Reflection</span> object and convert it to string
instead:

``` php
<?php
// ReflectionClass::export(Foo::class, false) is:
echo new ReflectionClass(Foo::class), "\n";

// $str = ReflectionClass::export(Foo::class, true) is:
$str = (string) new ReflectionClass(Foo::class);
?>
```

### Socket

The **`AI_IDN_ALLOW_UNASSIGNED`** and **`AI_IDN_USE_STD3_ASCII_RULES`**
flags for <span class="function">socket\_addrinfo\_lookup</span> are
deprecated, due to an upstream deprecation in glibc.
