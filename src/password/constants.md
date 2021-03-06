预定义常量
==========

下列常量作为 PHP 核心的一部分总是可用的。

**`PASSWORD_BCRYPT`** (<span class="type">string</span>)  
**`PASSWORD_BCRYPT`** is used to create new password hashes using the
**`CRYPT_BLOWFISH`** algorithm.

This will always result in a hash using the "$2y$" crypt format, which
is always 60 characters wide.

Supported Options:

-   *salt* (<span class="type">string</span>) - to manually provide a
    salt to use when hashing the password. Note that this will override
    and prevent a salt from being automatically generated.

    If omitted, a random salt will be generated by <span
    class="function">password\_hash</span> for each password hashed.
    This is the intended mode of operation and as of PHP 7.0.0 the salt
    option has been deprecated.

-   *cost* (<span class="type">int</span>) - which denotes the
    algorithmic cost that should be used. Examples of these values can
    be found on the <span class="function">crypt</span> page.

    If omitted, a default value of *10* will be used. This is a good
    baseline cost, but you may want to consider increasing it depending
    on your hardware.

**`PASSWORD_ARGON2I`** (<span class="type">string</span>)  
**`PASSWORD_ARGON2I`** is used to create new password hashes using the
Argon2i algorithm.

Supported Options:

-   *memory\_cost* (<span class="type">int</span>) - Maximum memory (in
    bytes) that may be used to compute the Argon2 hash. Defaults to
    **`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`**.

-   *time\_cost* (<span class="type">int</span>) - Maximum amount of
    time it may take to compute the Argon2 hash. Defaults to
    **`PASSWORD_ARGON2_DEFAULT_TIME_COST`**.

-   *threads* (<span class="type">int</span>) - Number of threads to use
    for computing the Argon2 hash. Defaults to
    **`PASSWORD_ARGON2_DEFAULT_THREADS`**.

Available as of PHP 7.2.0.

**`PASSWORD_ARGON2ID`** (<span class="type">string</span>)  
**`PASSWORD_ARGON2ID`** is used to create new password hashes using the
Argon2id algorithm. It supports the same options as
<a href="/password/constants.html#" class="link"><strong><code>PASSWORD_ARGON2I</code></strong></a>.

Available as of PHP 7.3.0.

**`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`** (<span class="type">int</span>)  
Default amount of memory in bytes that Argon2lib will use while trying
to compute a hash.

Available as of PHP 7.2.0.

**`PASSWORD_ARGON2_DEFAULT_TIME_COST`** (<span class="type">int</span>)  
Default amount of time that Argon2lib will spend trying to compute a
hash.

Available as of PHP 7.2.0.

**`PASSWORD_ARGON2_DEFAULT_THREADS`** (<span class="type">int</span>)  
Default number of threads that Argon2lib will use.

Available as of PHP 7.2.0.

**`PASSWORD_DEFAULT`** (<span class="type">mixed</span>)  
The default algorithm to use for hashing if no algorithm is provided.
This may change in newer PHP releases when newer, stronger hashing
algorithms are supported.

It is worth noting that over time this constant can (and likely will)
change. Therefore you should be aware that the length of the resulting
hash can change. Therefore, if you use **`PASSWORD_DEFAULT`** you should
store the resulting hash in a way that can store more than 60 characters
(255 is the recommended width).

Values for this constant:

-   <span class="simpara"> PHP 5.5.0 - **`PASSWORD_BCRYPT`** </span>

##### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.4.0 | The values of the password algo IDs (**`PASSWORD_BCRYPT`**, **`PASSWORD_ARGON2I`**, **`PASSWORD_ARGON2ID`** and **`PASSWORD_DEFAULT`**) are now <span class="type">string</span>s. Previously, they have been <span class="type">int</span>s. |
