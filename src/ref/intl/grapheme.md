grapheme\_extract
=================

Function to extract a sequence of default grapheme clusters from a text
buffer, which must be encoded in UTF-8

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">grapheme\_extract</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">int</span> `$size`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$extract_type`</span> \[, <span class="methodparam"><span
class="type">int</span> `$start`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `&$next`</span> \]\]\] )

Function to extract a sequence of default grapheme clusters from a text
buffer, which must be encoded in UTF-8.

### 参数

`haystack`  
String to search.

`size`  
Maximum number items - based on the $extract\_type - to return.

`extract_type`  
Defines the type of units referred to by the $size parameter:

-   GRAPHEME\_EXTR\_COUNT (default) - $size is the number of default
    grapheme clusters to extract.
-   GRAPHEME\_EXTR\_MAXBYTES - $size is the maximum number of bytes
    returned.
-   GRAPHEME\_EXTR\_MAXCHARS - $size is the maximum number of UTF-8
    characters returned.

`start`  
Starting position in $haystack in bytes - if given, it must be zero or a
positive value that is less than or equal to the length of $haystack in
bytes, or a negative value that counts from the end of $haystack. If
$start does not point to the first byte of a UTF-8 character, the start
position is moved to the next character boundary.

`next`  
Reference to a value that will be set to the next starting position.
When the call returns, this may point to the first byte position past
the end of the string.

### 返回值

A string starting at offset $start and ending on a default grapheme
cluster boundary that conforms to the $size and $extract\_type
specified.

### 更新日志

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 7.1.0 | Support for negative `start`s has been added. |

### 范例

**示例 \#1 <span class="function">grapheme\_extract</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print urlencode(grapheme_extract( $char_a_ring_nfd . $char_o_diaeresis_nfd, 1, GRAPHEME_EXTR_COUNT, 2));

?>
```

以上例程会输出：

    o%CC%88

### 参见

-   <span class="function">grapheme\_substr</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_stripos
=================

Find position (in grapheme units) of first occurrence of a
case-insensitive string

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">grapheme\_stripos</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \] )

Find position (in grapheme units) of first occurrence of a
case-insensitive string

### 参数

`haystack`  
The string to look in. Must be valid UTF-8.

`needle`  
The string to look for. Must be valid UTF-8.

`offset`  
The optional $offset parameter allows you to specify where in haystack
to start searching as an offset in grapheme units (not bytes or
characters). If the offset is negative, it is treated relative to the
end of the string. The position returned is still relative to the
beginning of haystack regardless of the value of $offset.

### 返回值

Returns the position as an integer. If needle is not found,
grapheme\_stripos() will return boolean FALSE.

### 更新日志

| 版本  | 说明                                           |
|-------|------------------------------------------------|
| 7.1.0 | Support for negative `offset`s has been added. |

### 范例

**示例 \#1 <span class="function">grapheme\_stripos</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"
$char_O_diaeresis_nfd = "O\xCC\x88"; // 'LATIN CAPITAL LETTER O WITH DIAERESIS' (U+00D6) normalization form "D"

print grapheme_stripos( $char_a_ring_nfd . $char_a_ring_nfd . $char_o_diaeresis_nfd, $char_O_diaeresis_nfd);

?>
```

以上例程会输出：

    2

### 参见

-   <span class="function">grapheme\_stristr</span>
-   <span class="function">grapheme\_strpos</span>
-   <span class="function">grapheme\_strripos</span>
-   <span class="function">grapheme\_strrpos</span>
-   <span class="function">grapheme\_strstr</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_stristr
=================

Returns part of haystack string from the first occurrence of
case-insensitive needle to the end of haystack

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">grapheme\_stristr</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$before_needle`<span class="initializer"> =
**`false`**</span></span> \] )

Returns part of haystack string starting from and including the first
occurrence of case-insensitive needle to the end of haystack.

### 参数

`haystack`  
The input string. Must be valid UTF-8.

`needle`  
The string to look for. Must be valid UTF-8.

`before_needle`  
If **`true`**, grapheme\_strstr() returns the part of the haystack
before the first occurrence of the needle (excluding needle).

### 返回值

Returns the portion of $haystack, or FALSE if $needle is not found.

### 范例

**示例 \#1 <span class="function">grapheme\_stristr</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"
$char_O_diaeresis_nfd = "O\xCC\x88"; // 'LATIN CAPITAL LETTER O WITH DIAERESIS' (U+00D6) normalization form "D"

print urlencode(grapheme_stristr( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_a_ring_nfd, $char_O_diaeresis_nfd));

?>
```

以上例程会输出：

    o%CC%88a%CC%8A

### 参见

-   <span class="function">grapheme\_stripos</span>
-   <span class="function">grapheme\_strpos</span>
-   <span class="function">grapheme\_strripos</span>
-   <span class="function">grapheme\_strrpos</span>
-   <span class="function">grapheme\_strstr</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_strlen
================

Get string length in grapheme units

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">grapheme\_strlen</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> )

Get string length in grapheme units (not bytes or characters)

### 参数

`input`  
The string being measured for length. It must be a valid UTF-8 string.

### 返回值

The length of the string on success, and 0 if the string is empty.

### 范例

**示例 \#1 <span class="function">grapheme\_strlen</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print grapheme_strlen( 'abc' . $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_a_ring_nfd);

?>
```

以上例程会输出：

    6

### 参见

-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>
-   <span class="function">iconv\_strlen</span>
-   <span class="function">mb\_strlen</span>
-   <span class="function">strlen</span>

grapheme\_strpos
================

Find position (in grapheme units) of first occurrence of a string

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">grapheme\_strpos</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \] )

Find position (in grapheme units) of first occurrence of a string

### 参数

`haystack`  
The string to look in. Must be valid UTF-8.

`needle`  
The string to look for. Must be valid UTF-8.

`offset`  
The optional $offset parameter allows you to specify where in $haystack
to start searching as an offset in grapheme units (not bytes or
characters). If the offset is negative, it is treated relative to the
end of the string. The position returned is still relative to the
beginning of haystack regardless of the value of $offset.

### 返回值

Returns the position as an integer. If needle is not found,
grapheme\_strpos() will return boolean FALSE.

### 更新日志

| 版本  | 说明                                           |
|-------|------------------------------------------------|
| 7.1.0 | Support for negative `offset`s has been added. |

### 范例

**示例 \#1 <span class="function">grapheme\_strpos</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print grapheme_strpos( $char_a_ring_nfd . $char_a_ring_nfd . $char_o_diaeresis_nfd, $char_o_diaeresis_nfd);

?>
```

以上例程会输出：

    2

### 参见

-   <span class="function">grapheme\_stripos</span>
-   <span class="function">grapheme\_stristr</span>
-   <span class="function">grapheme\_strripos</span>
-   <span class="function">grapheme\_strrpos</span>
-   <span class="function">grapheme\_strstr</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_strripos
==================

Find position (in grapheme units) of last occurrence of a
case-insensitive string

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">grapheme\_strripos</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \] )

Find position (in grapheme units) of last occurrence of a
case-insensitive string

### 参数

`haystack`  
The string to look in. Must be valid UTF-8.

`needle`  
The string to look for. Must be valid UTF-8.

`offset`  
The optional $offset parameter allows you to specify where in $haystack
to start searching as an offset in grapheme units (not bytes or
characters). The position returned is still relative to the beginning of
haystack regardless of the value of $offset.

### 返回值

Returns the position as an integer. If needle is not found,
grapheme\_strripos() will return boolean FALSE.

### 范例

**示例 \#1 <span class="function">grapheme\_strripos</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"
$char_O_diaeresis_nfd = "O\xCC\x88"; // 'LATIN CAPITAL LETTER O WITH DIAERESIS' (U+00D6) normalization form "D"

print grapheme_strripos( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_o_diaeresis_nfd, $char_O_diaeresis_nfd);

?>
```

以上例程会输出：

    2

### 参见

-   <span class="function">grapheme\_stripos</span>
-   <span class="function">grapheme\_stristr</span>
-   <span class="function">grapheme\_strpos</span>
-   <span class="function">grapheme\_strrpos</span>
-   <span class="function">grapheme\_strstr</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_strrpos
=================

Find position (in grapheme units) of last occurrence of a string

### 说明

过程化风格

<span class="type">int</span> <span
class="methodname">grapheme\_strrpos</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$offset`<span class="initializer"> =
0</span></span> \] )

Find position (in grapheme units) of last occurrence of a string

### 参数

`haystack`  
The string to look in. Must be valid UTF-8.

`needle`  
The string to look for. Must be valid UTF-8.

`offset`  
The optional $offset parameter allows you to specify where in $haystack
to start searching as an offset in grapheme units (not bytes or
characters). The position returned is still relative to the beginning of
haystack regardless of the value of $offset.

### 返回值

Returns the position as an integer. If needle is not found,
grapheme\_strrpos() will return boolean FALSE.

### 范例

**示例 \#1 <span class="function">grapheme\_strrpos</span> example**

``` php
<?php
$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print grapheme_strrpos( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_o_diaeresis_nfd, $char_o_diaeresis_nfd);
?>
```

以上例程会输出：

    2

### 参见

-   <span class="function">grapheme\_stripos</span>
-   <span class="function">grapheme\_stristr</span>
-   <span class="function">grapheme\_strpos</span>
-   <span class="function">grapheme\_strripos</span>
-   <span class="function">grapheme\_strstr</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_strstr
================

Returns part of haystack string from the first occurrence of needle to
the end of haystack

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">grapheme\_strstr</span> ( <span
class="methodparam"><span class="type">string</span> `$haystack`</span>
, <span class="methodparam"><span class="type">string</span>
`$needle`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$before_needle`<span class="initializer"> =
**`false`**</span></span> \] )

Returns part of haystack string from the first occurrence of needle to
the end of haystack (including the needle).

### 参数

`haystack`  
The input string. Must be valid UTF-8.

`needle`  
The string to look for. Must be valid UTF-8.

`before_needle`  
If **`true`**, grapheme\_strstr() returns the part of the haystack
before the first occurrence of the needle (excluding the needle).

### 返回值

Returns the portion of string, or FALSE if needle is not found.

### 范例

**示例 \#1 <span class="function">grapheme\_strstr</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print urlencode(grapheme_stristr( $char_a_ring_nfd . $char_o_diaeresis_nfd . $char_a_ring_nfd, $char_o_diaeresis_nfd));

?>
```

以上例程会输出：

    o%CC%88a%CC%8A

### 参见

-   <span class="function">grapheme\_stristr</span>
-   <span class="function">grapheme\_stripos</span>
-   <span class="function">grapheme\_strpos</span>
-   <span class="function">grapheme\_strripos</span>
-   <span class="function">grapheme\_strrpos</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

grapheme\_substr
================

Return part of a string

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">grapheme\_substr</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> ,
<span class="methodparam"><span class="type">int</span> `$start`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$length`</span> \] )

Return part of a string

### 参数

`string`  
The input string. Must be valid UTF-8.

`start`  
Start position in default grapheme units. If $start is non-negative, the
returned string will start at the $start'th position in $string,
counting from zero. If $start is negative, the returned string will
start at the $start'th grapheme unit from the end of string.

`length`  
Length in grapheme units. If $length is given and is positive, the
string returned will contain at most $length grapheme units beginning
from $start (depending on the length of string). If $length is given and
is negative, then that many grapheme units will be omitted from the end
of string (after the start position has been calculated when a start is
negative). If $start denotes a position beyond this truncation,
**`false`** will be returned.

### 返回值

Returns the extracted part of $string.

### 范例

**示例 \#1 <span class="function">grapheme\_substr</span> example**

``` php
<?php

$char_a_ring_nfd = "a\xCC\x8A";  // 'LATIN SMALL LETTER A WITH RING ABOVE' (U+00E5) normalization form "D"
$char_o_diaeresis_nfd = "o\xCC\x88"; // 'LATIN SMALL LETTER O WITH DIAERESIS' (U+00F6) normalization form "D"

print urlencode(grapheme_substr( "ao" . $char_a_ring_nfd . "bc" . $char_o_diaeresis_nfd . "O", 2, -1 ));
?>
```

以上例程会输出：

    a%CC%8Abco%CC%88

### 参见

-   <span class="function">grapheme\_extract</span>
-   <a href="http://unicode.org/reports/tr29/#Grapheme_Cluster_Boundaries" class="link external">»  Unicode Text Segmentation: Grapheme Cluster Boundaries</a>

**目录**

-   [grapheme\_extract](/ref/intl/grapheme.html#grapheme_extract) —
    Function to extract a sequence of default grapheme clusters from a
    text buffer, which must be encoded in UTF-8
-   [grapheme\_stripos](/ref/intl/grapheme.html#grapheme_stripos) — Find
    position (in grapheme units) of first occurrence of a
    case-insensitive string
-   [grapheme\_stristr](/ref/intl/grapheme.html#grapheme_stristr) —
    Returns part of haystack string from the first occurrence of
    case-insensitive needle to the end of haystack
-   [grapheme\_strlen](/ref/intl/grapheme.html#grapheme_strlen) — Get
    string length in grapheme units
-   [grapheme\_strpos](/ref/intl/grapheme.html#grapheme_strpos) — Find
    position (in grapheme units) of first occurrence of a string
-   [grapheme\_strripos](/ref/intl/grapheme.html#grapheme_strripos) —
    Find position (in grapheme units) of last occurrence of a
    case-insensitive string
-   [grapheme\_strrpos](/ref/intl/grapheme.html#grapheme_strrpos) — Find
    position (in grapheme units) of last occurrence of a string
-   [grapheme\_strstr](/ref/intl/grapheme.html#grapheme_strstr) —
    Returns part of haystack string from the first occurrence of needle
    to the end of haystack
-   [grapheme\_substr](/ref/intl/grapheme.html#grapheme_substr) — Return
    part of a string
