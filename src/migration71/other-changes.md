Other changes
-------------

### Notices and warnings on arithmetic with invalid strings

New **`E_WARNING`** and **`E_NOTICE`** errors have been introduced when
invalid strings are coerced using operators expecting numbers (*+* *-*
*\** */* *\*\** *%* *\<\<* *\>\>* *\|* *&* *^*) or their assignment
equivalents. An **`E_NOTICE`** is emitted when the string begins with a
numeric value but contains trailing non-numeric characters, and an
**`E_WARNING`** is emitted when the string does not contain a numeric
value.

``` php
<?php
'1b' + 'something';
```

以上例程会输出：

    Notice: A non well formed numeric value encountered in %s on line %d
    Warning: A non-numeric value encountered in %s on line %d

### Warn on octal escape sequence overflow

Previously, 3-octet octal string escape sequences would overflow
silently. Now, they will still overflow, but **`E_WARNING`** will be
emitted.

``` php
<?php
var_dump("\500");
```

以上例程会输出：

    Warning: Octal escape sequence overflow \500 is greater than \377 in %s on line %d
    string(1) "@"

### Inconsistency fixes to *$this*

Whilst *$this* is considered a special variable in PHP, it lacked proper
checks to ensure it wasn't used as a variable name or reassigned. This
has now been rectified to ensure that *$this* cannot be a user-defined
variable, reassigned to a different value, or be globalised.

### Session ID generation without hashing

Session IDs will no longer be hashed upon generation. With this change
brings about the removal of the following four ini settings:

-   <span class="simpara"> `session.entropy_file` </span>
-   <span class="simpara"> `session.entropy_length` </span>
-   <span class="simpara"> `session.hash_function` </span>
-   <span class="simpara"> `session.hash_bits_per_character` </span>

And the addition of the following two ini settings:

-   <span class="simpara"> `session.sid_length` - defines the length of
    the session ID, defaulting to 32 characters for backwards
    compatibility) </span>
-   <span class="simpara"> `session.sid_bits_per_character` - defines
    the number of bits to be stored per character (i.e. increases the
    range of characters that can be used in the session ID), defaulting
    to 4 for backwards compatibility </span>

### Changes to INI file handling

`precision`  
If the value is set to -1, then the dtoa mode 0 is used. The default
value is still 14.

`serialize_precision`  
If the value is set to -1, then the dtoa mode 0 is used. The value -1 is
now used by default.

`gd.jpeg_ignore_warning`  
The default of this `php.ini` setting has been changed to 1, so by
default libjpeg warnings are ignored.

`opcache.enable_cli`  
The default of this `php.ini` setting has been changed to 1 (enabled) in
PHP 7.1.2, and back to 0 (disabled) in PHP 7.1.7.

### Session ID generation with a CSPRNG only

Session IDs will now only be generated with a CSPRNG.

### More informative <span class="classname">TypeError</span> messages when **`NULL`** is allowed

<span class="classname">TypeError</span> exceptions for arg\_info type
checks will now provide more informative error messages. If the
parameter type or return type accepts **`NULL`** (by either having a
default value of **`NULL`** or being a nullable type), then the error
message will now mention this with a message of "must be ... or null" or
"must ... or be null."
