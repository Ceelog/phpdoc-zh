idn\_to\_ascii
==============

Convert domain name to IDNA ASCII form

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">idn\_to\_ascii</span> ( <span
class="methodparam"><span class="type">string</span> `$domain`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = IDNA\_DEFAULT</span></span> \[,
<span class="methodparam"><span class="type">int</span> `$variant`<span
class="initializer"> = INTL\_IDNA\_VARIANT\_UTS46</span></span> \[,
<span class="methodparam"><span class="type">array</span>
`&$idna_info`</span> \]\]\] )

This function converts a Unicode domain name to an IDNA ASCII-compatible
format.

### 参数

`domain`  
The domain to convert, which must be UTF-8 encoded.

`options`  
Conversion options - combination of IDNA\_\* constants (except
IDNA\_ERROR\_\* constants).

`variant`  
Either **`INTL_IDNA_VARIANT_2003`** (deprecated as of PHP 7.2.0) for
IDNA 2003 or **`INTL_IDNA_VARIANT_UTS46`** (only available as of ICU
4.6) for UTS \#46.

`idna_info`  
This parameter can be used only if **`INTL_IDNA_VARIANT_UTS46`** was
used for `variant`. In that case, it will be filled with an array with
the keys *'result'*, the possibly illegal result of the transformation,
*'isTransitionalDifferent'*, a boolean indicating whether the usage of
the transitional mechanisms of UTS \#46 either has or would have changed
the result and *'errors'*, which is an <span class="type">int</span>
representing a bitset of the error constants IDNA\_ERROR\_\*.

### 返回值

The domain name encoded in ASCII-compatible form, 或者在失败时返回
**`FALSE`**

### 更新日志

| 版本               | 说明                                                                                                                        |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 7.4.0              | The default value of `variant` is now **`INTL_IDNA_VARIANT_UTS46`** instead of the deprecated **`INTL_IDNA_VARIANT_2003`**. |
| 7.2.0              | **`INTL_IDNA_VARIANT_2003`** has been deprecated; use **`INTL_IDNA_VARIANT_UTS46`** instead.                                |
| 5.4.0/PECL 2.0.0b1 | Added the parameters `variant` and `idna_info`; UTS \#46 support (requires ICU ≥ 4.6).                                      |

### 范例

**示例 \#1 <span class="function">idn\_to\_ascii</span> example**

``` php
<?php

echo idn_to_ascii('täst.de'); 

?>
```

以上例程会输出：

    xn--tst-qla.de

### 参见

-   <span class="function">idn\_to\_utf8</span>

idn\_to\_utf8
=============

Convert domain name from IDNA ASCII to Unicode

### 说明

过程化风格

<span class="type">string</span> <span
class="methodname">idn\_to\_utf8</span> ( <span
class="methodparam"><span class="type">string</span> `$domain`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`<span class="initializer"> = IDNA\_DEFAULT</span></span> \[,
<span class="methodparam"><span class="type">int</span> `$variant`<span
class="initializer"> = INTL\_IDNA\_VARIANT\_UTS46</span></span> \[,
<span class="methodparam"><span class="type">array</span>
`&$idna_info`</span> \]\]\] )

This function converts a Unicode domain name from an IDNA
ASCII-compatible format to plain Unicode, encoded in UTF-8.

### 参数

`domain`  
Domain to convert in an IDNA ASCII-compatible format.

`options`  
Conversion options - combination of IDNA\_\* constants (except
IDNA\_ERROR\_\* constants).

`variant`  
Either **`INTL_IDNA_VARIANT_2003`** (deprecated as of PHP 7.2.0) for
IDNA 2003 or **`INTL_IDNA_VARIANT_UTS46`** (only available as of ICU
4.6) for UTS \#46.

`idna_info`  
This parameter can be used only if **`INTL_IDNA_VARIANT_UTS46`** was
used for `variant`. In that case, it will be filled with an array with
the keys *'result'*, the possibly illegal result of the transformation,
*'isTransitionalDifferent'*, a boolean indicating whether the usage of
the transitional mechanisms of UTS \#46 either has or would have changed
the result and *'errors'*, which is an <span class="type">int</span>
representing a bitset of the error constants IDNA\_ERROR\_\*.

### 返回值

The domain name in Unicode, encoded in UTF-8, 或者在失败时返回
**`FALSE`**

### 更新日志

| 版本               | 说明                                                                                                                        |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 7.4.0              | The default value of `variant` is now **`INTL_IDNA_VARIANT_UTS46`** instead of the deprecated **`INTL_IDNA_VARIANT_2003`**. |
| 7.2.0              | **`INTL_IDNA_VARIANT_2003`** has been deprecated; use **`INTL_IDNA_VARIANT_UTS46`** instead.                                |
| 5.4.0/PECL 2.0.0b1 | Added the parameters `variant` and `idna_info`; UTS \#46 support (requires ICU ≥ 4.6).                                      |

### 范例

**示例 \#1 <span class="function">idn\_to\_utf8</span> example**

``` php
<?php

echo idn_to_utf8('xn--tst-qla.de'); 

?>
```

以上例程会输出：

    täst.de

### 参见

-   <span class="function">idn\_to\_ascii</span>

**目录**

-   [idn\_to\_ascii](/ref/intl/idn.html#idn_to_ascii) — Convert domain
    name to IDNA ASCII form
-   [idn\_to\_utf8](/ref/intl/idn.html#idn_to_utf8) — Convert domain
    name from IDNA ASCII to Unicode
