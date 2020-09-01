crack\_check
============

用给定的密码来进行破解测试

### 说明

<span class="type">bool</span> <span
class="methodname">crack\_check</span> ( <span class="methodparam"><span
class="type">resource</span> `$dictionary`</span> , <span
class="methodparam"><span class="type">string</span> `$password`</span>
)

<span class="type">bool</span> <span
class="methodname">crack\_check</span> ( <span class="methodparam"><span
class="type">string</span> `$password`</span> , <span
class="methodparam"><span class="type">string</span> `$username`<span
class="initializer"> = ""</span></span> , <span
class="methodparam"><span class="type">string</span> `$gecos`<span
class="initializer"> = ""</span></span> , <span
class="methodparam"><span class="type">resource</span>
`$dictionary`<span class="initializer"> = **`NULL`**</span></span> )

使用特定字典中给定的密码来进行密码强度检测。可供选择的特征(The
alternative signature )还考虑用户名和GECOS信息。

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`dictionary`  
破解库所使用的字典，如果没有指定，则使用最后一次打开的字典。

`password`  
需要检查的密码。

`username`  
用于密码检测的这个账户的用户名。

`gecos`  
用户账户的 GECOS 信息。

### 返回值

返回 **`TRUE`** 如果 `password` 足够安全, 或者返回 **`FALSE`**
表示可能需要进一步的操作.

### 更新日志

| 版本 | 说明                                                                                          |
|------|-----------------------------------------------------------------------------------------------|
| 0.3  | `username`、`gecos` 和 `dictionary` 字段被添加到了可供选择的特征（alternative signature）中。 |

crack\_closedict
================

Closes an open CrackLib dictionary

### 说明

<span class="type">bool</span> <span
class="methodname">crack\_closedict</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$dictionary`</span> \] )

<span class="function">crack\_closedict</span> closes the specified
`dictionary` identifier.

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参数

`dictionary`  
The dictionary to close. If not specified, the current dictionary is
closed.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">crack\_opendict</span>

crack\_getlastmessage
=====================

Returns the message from the last obscure check

### 说明

<span class="type">string</span> <span
class="methodname">crack\_getlastmessage</span> ( <span
class="methodparam">void</span> )

<span class="function">crack\_getlastmessage</span> returns the message
from the last obscure check.

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 返回值

The message from the last obscure check or **`FALSE`** if there was no
obscure checks made so far.

The returned message is one of:

-   <span class="simpara"> *it's WAY too short* </span>
-   <span class="simpara"> *it is too short* </span>
-   <span class="simpara"> *it does not contain enough DIFFERENT
    characters* </span>
-   <span class="simpara"> *it is all whitespace* </span>
-   <span class="simpara"> *it is too simplistic/systematic* </span>
-   <span class="simpara"> *it looks like a National Insurance number.*
    </span>
-   <span class="simpara"> *it is based on a dictionary word* </span>
-   <span class="simpara"> *it is based on a (reversed) dictionary word*
    </span>
-   <span class="simpara"> *strong password* </span>

### 参见

-   <span class="function">crack\_check</span>

crack\_opendict
===============

Opens a new CrackLib dictionary

### 说明

<span class="type">resource</span> <span
class="methodname">crack\_opendict</span> ( <span
class="methodparam"><span class="type">string</span>
`$dictionary`</span> )

<span class="function">crack\_opendict</span> opens the specified
CrackLib `dictionary` for use with <span
class="function">crack\_check</span>.

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

> **Note**:
>
> Only one dictionary may be open at a time.

### 参数

`dictionary`  
The path to the Cracklib dictionary.

### 返回值

Returns a dictionary resource identifier on success 或者在失败时返回
**`FALSE`**.

### 参见

-   <span class="function">crack\_check</span>
-   <span class="function">crack\_closedict</span>

**目录**

-   [crack\_check](/ref/crack.html#crack_check) —
    用给定的密码来进行破解测试
-   [crack\_closedict](/ref/crack.html#crack_closedict) — Closes an open
    CrackLib dictionary
-   [crack\_getlastmessage](/ref/crack.html#crack_getlastmessage) —
    Returns the message from the last obscure check
-   [crack\_opendict](/ref/crack.html#crack_opendict) — Opens a new
    CrackLib dictionary
