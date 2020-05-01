random\_bytes
=============

Generates cryptographically secure pseudo-random bytes

### 说明

<span class="type">string</span> <span
class="methodname">random\_bytes</span> ( <span
class="methodparam"><span class="type">int</span> `$length`</span> )

Generates an arbitrary length string of cryptographic random bytes that
are suitable for cryptographic use, such as when generating salts, keys
or initialization vectors.

The sources of randomness used for this function are as follows:

-   <span class="simpara"> On Windows,
    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa379942(v=vs.85).aspx" class="link external">» <span class="function">CryptGenRandom</span></a>
    will always be used. As of PHP 7.2.0, the
    <a href="https://docs.microsoft.com/en-us/windows/desktop/SecCNG/cng-portal" class="link external">» CNG-API</a>
    will always be used instead. </span>
-   <span class="simpara"> On Linux, the
    <a href="http://man7.org/linux/man-pages/man2/getrandom.2.html" class="link external">» getrandom(2)</a>
    syscall will be used if available. </span>
-   <span class="simpara"> On other platforms, `/dev/urandom` will be
    used. </span>
-   <span class="simpara"> If none of the aforementioned sources are
    available, then an <span class="classname">Exception</span> will be
    thrown. </span>

> **Note**: <span class="simpara"> Although this function was added to
> PHP in PHP 7.0, a
> <a href="https://github.com/paragonie/random_compat" class="link external">» userland implementation</a>
> is available for PHP 5.2 to 5.6, inclusive. </span>

### 参数

`length`  
The length of the random string that should be returned in bytes.

### 返回值

Returns a string containing the requested number of cryptographically
secure random bytes.

### 错误／异常

-   <span class="simpara"> If an appropriate source of randomness cannot
    be found, an <span class="classname">Exception</span> will be
    thrown. </span>
-   <span class="simpara"> If invalid parameters are given, a <span
    class="classname">TypeError</span> will be thrown. </span>
-   <span class="simpara"> If an invalid `length` of bytes is given, an
    <span class="classname">Error</span> will be thrown. </span>

### 范例

**示例 \#1 <span class="function">random\_bytes</span> example**

``` php
<?php
$bytes = random_bytes(5);
var_dump(bin2hex($bytes));
?>
```

以上例程的输出类似于：

    string(10) "385e33f741"

### 参见

-   <span class="function">random\_int</span>
-   <span class="function">openssl\_random\_pseudo\_bytes</span>
-   <span class="function">bin2hex</span>

random\_int
===========

Generates cryptographically secure pseudo-random integers

### 说明

<span class="type">int</span> <span
class="methodname">random\_int</span> ( <span class="methodparam"><span
class="type">int</span> `$min`</span> , <span class="methodparam"><span
class="type">int</span> `$max`</span> )

Generates cryptographic random integers that are suitable for use where
unbiased results are critical, such as when shuffling a deck of cards
for a poker game.

The sources of randomness used for this function are as follows:

-   <span class="simpara"> On Windows,
    <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa379942(v=vs.85).aspx" class="link external">» <span class="function">CryptGenRandom</span></a>
    will always be used. As of PHP 7.2.0, the
    <a href="https://docs.microsoft.com/en-us/windows/desktop/SecCNG/cng-portal" class="link external">» CNG-API</a>
    will always be used instead. </span>
-   <span class="simpara"> On Linux, the
    <a href="http://man7.org/linux/man-pages/man2/getrandom.2.html" class="link external">» getrandom(2)</a>
    syscall will be used if available. </span>
-   <span class="simpara"> On other platforms, `/dev/urandom` will be
    used. </span>
-   <span class="simpara"> If none of the aforementioned sources are
    available, then an <span class="classname">Exception</span> will be
    thrown. </span>

> **Note**: <span class="simpara"> Although this function was added to
> PHP in PHP 7.0, a
> <a href="https://github.com/paragonie/random_compat" class="link external">» userland implementation</a>
> is available for PHP 5.2 to 5.6, inclusive. </span>

### 参数

`min`  
The lowest value to be returned, which must be **`PHP_INT_MIN`** or
higher.

`max`  
The highest value to be returned, which must be less than or equal to
**`PHP_INT_MAX`**.

### 返回值

Returns a cryptographically secure random integer in the range `min` to
`max`, inclusive.

### 错误／异常

-   <span class="simpara"> If an appropriate source of randomness cannot
    be found, an <span class="classname">Exception</span> will be
    thrown. </span>
-   <span class="simpara"> If invalid parameters are given, a <span
    class="classname">TypeError</span> will be thrown. </span>
-   <span class="simpara"> If `max` is less than `min`, an <span
    class="classname">Error</span> will be thrown. </span>

### 范例

**示例 \#1 <span class="function">random\_int</span> example**

``` php
<?php
var_dump(random_int(100, 999));
var_dump(random_int(-1000, 0));
?>
```

以上例程的输出类似于：

    int(248)
    int(-898)

### 参见

-   <span class="function">random\_bytes</span>

**目录**

-   [random\_bytes](/ref/csprng.html#random_bytes) — Generates
    cryptographically secure pseudo-random bytes
-   [random\_int](/ref/csprng.html#random_int) — Generates
    cryptographically secure pseudo-random integers
