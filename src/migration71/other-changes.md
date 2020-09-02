其它改动
--------

### 无效字符串计算的通知和警告

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

### 八进制转义序列溢出时发出警告

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

### *$this* 不一致的修正

Whilst *$this* is considered a special variable in PHP, it lacked proper
checks to ensure it wasn't used as a variable name or reassigned. This
has now been rectified to ensure that *$this* cannot be a user-defined
variable, reassigned to a different value, or be globalised.

### 无需散列即可生成 Session ID

Session ID 将不再在生成时进行哈希。这一变化，会导致以下四个 ini
设置不再使用：

-   <span class="simpara"> `session.entropy_file` </span>
-   <span class="simpara"> `session.entropy_length` </span>
-   <span class="simpara"> `session.hash_function` </span>
-   <span class="simpara"> `session.hash_bits_per_character` </span>

并增加以下两个 ini 设置：

-   <span class="simpara"> `session.sid_length` - 定义会话 ID
    的长度（为了向后兼容，默认为 32 个字符） </span>
-   <span class="simpara"> `session.sid_bits_per_character` -
    定义了每个字符的存储位数（即增加了会话 ID
    中可使用的字符范围），为了向后兼容，默认为 4 </span>

### INI 文件处理的变化

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
