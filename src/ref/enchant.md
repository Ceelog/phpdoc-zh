enchant\_broker\_describe
=========================

Enumerates the Enchant providers

### 说明

<span class="type">array</span> <span
class="methodname">enchant\_broker\_describe</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> )

Enumerates the Enchant providers and tells you some rudimentary
information about them. The same info is provided through phpinfo().

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

### 返回值

Returns an <span class="type">array</span> of available Enchant
providers with their details.

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |
| 8.0.0 | Prior to this version, the function returned **`false`** on failure.                                                                                                               |

### 范例

**示例 \#1 List the backends provided by the given broker**

``` php
<?php
$r = enchant_broker_init();
$bprovides = enchant_broker_describe($r);
echo "Current broker provides the following backend(s):\n";
print_r($bprovides);

?>
```

以上例程的输出类似于：

    Current broker provides the following backend(s):
    Array
    (
        [0] => Array
            (
                [name] => aspell
                [desc] => Aspell Provider
                [file] => /usr/lib/enchant/libenchant_aspell.so
            )

        [1] => Array
            (
                [name] => hspell
                [desc] => Hspell Provider
                [file] => /usr/lib/enchant/libenchant_hspell.so
            )

        [2] => Array
            (
                [name] => ispell
                [desc] => Ispell Provider
                [file] => /usr/lib/enchant/libenchant_ispell.so
            )

        [3] => Array
            (
                [name] => myspell
                [desc] => Myspell Provider
                [file] => /usr/lib/enchant/libenchant_myspell.so
            )

    )

enchant\_broker\_dict\_exists
=============================

Whether a dictionary exists or not. Using non-empty tag

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_broker\_dict\_exists</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> , <span class="methodparam"><span
class="type">string</span> `$tag`</span> )

Tells if a dictionary exists or not, using a non-empty tags

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

`tag`  
non-empty tag in the LOCALE format, ex: us\_US, ch\_DE, etc.

### 返回值

Returns **`true`** when the tag exist or **`false`** when not.

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 范例

**示例 \#1 A <span class="function">enchant\_broker\_dict\_exists</span>
example**

``` php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
if (enchant_broker_dict_exists($r,$tag)) {
    echo $tag . " dictionary found.\n";
}
?>
```

### 参见

-   <span class="function">enchant\_broker\_describe</span>

enchant\_broker\_free\_dict
===========================

Free a dictionary resource

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_broker\_free\_dict</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> )

Free a dictionary resource.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects a <span class="classname">EnchantDictionary</span> now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 参见

-   <span class="function">enchant\_broker\_request\_dict</span>
-   <span class="function">enchant\_broker\_request\_pwl\_dict</span>

enchant\_broker\_free
=====================

Free the broker resource and its dictionaries

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_broker\_free</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> )

Free a broker resource with all its dictionaries.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 参见

-   <span class="function">enchant\_broker\_init</span>

enchant\_broker\_get\_dict\_path
================================

Get the directory path for a given backend

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">enchant\_broker\_get\_dict\_path</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> )

Get the directory path for a given backend.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

`type`  
The type of the dictionaries, i.e. **`ENCHANT_MYSPELL`** or
**`ENCHANT_ISPELL`**.

### 返回值

Returns the path of the dictionary directory on success 或者在失败时返回
**`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 参见

-   <span class="function">enchant\_broker\_set\_dict\_path</span>

enchant\_broker\_get\_error
===========================

Returns the last error of the broker

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">enchant\_broker\_get\_error</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> )

Returns the last error which occurred in this broker.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

### 返回值

Return the msg string if an error was found or **`false`**

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

enchant\_broker\_init
=====================

Create a new broker object capable of requesting

### 说明

<span class="type"><span class="type">EnchantBroker</span><span
class="type">false</span></span> <span
class="methodname">enchant\_broker\_init</span> ( <span
class="methodparam">void</span> )

### 参数

### 返回值

Returns a broker resource on success or **`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                                               |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | On success, this function returns an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was retured. |

### 参见

-   <span class="function">enchant\_broker\_free</span>

enchant\_broker\_list\_dicts
============================

Returns a list of available dictionaries

### 说明

<span class="type">array</span> <span
class="methodname">enchant\_broker\_list\_dicts</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> )

Returns a list of available dictionaries with their details.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

### 返回值

Returns an <span class="type">array</span> of available dictionaries
with their details.

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |
| 8.0.0 | Prior to this version, the function returned **`false`** on failure.                                                                                                               |

### 范例

**示例 \#1 List all available dictionaries for one broker**

``` php
<?php
$r = enchant_broker_init();
$dicts = enchant_broker_list_dicts($r);
print_r($dicts);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
            (
                [lang_tag] => de
                [provider_name] => aspell
                [provider_desc] => Aspell Provider
                [provider_file] => /usr/lib/enchant/libenchant_aspell.so
            )

        [1] => Array
            (
                [lang_tag] => de_DE
                [provider_name] => aspell
                [provider_desc] => Aspell Provider
                [provider_file] => /usr/lib/enchant/libenchant_aspell.so
            )

        [3] => Array
            (
                [lang_tag] => en
                [provider_name] => aspell
                [provider_desc] => Aspell Provider
                [provider_file] => /usr/lib/enchant/libenchant_aspell.so
            )

        [4] => Array
            (
                [lang_tag] => en_GB
                [provider_name] => aspell
                [provider_desc] => Aspell Provider
                [provider_file] => /usr/lib/enchant/libenchant_aspell.so
            )

        [5] => Array
            (
                [lang_tag] => en_US
                [provider_name] => aspell
                [provider_desc] => Aspell Provider
                [provider_file] => /usr/lib/enchant/libenchant_aspell.so
            )

        [6] => Array
            (
                [lang_tag] => hi_IN
                [provider_name] => myspell
                [provider_desc] => Myspell Provider
                [provider_file] => /usr/lib/enchant/libenchant_myspell.so
            )

    )

### 参见

-   <span class="function">enchant\_broker\_describe</span>

enchant\_broker\_request\_dict
==============================

Create a new dictionary using a tag

### 说明

<span class="type"><span class="type">EnchantDictionary</span><span
class="type">false</span></span> <span
class="methodname">enchant\_broker\_request\_dict</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> , <span class="methodparam"><span
class="type">string</span> `$tag`</span> )

create a new dictionary using tag, the non-empty language tag you wish
to request a dictionary for ("en\_US", "de\_DE", ...)

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

`tag`  
A tag describing the locale, for example en\_US, de\_DE

### 返回值

Returns a dictionary resource on success 或者在失败时返回 **`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                   |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected.                     |
| 8.0.0 | On success, this function returns an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was retured. |

### 范例

**示例 \#1 A <span
class="function">enchant\_broker\_request\_dict</span> example**

Check if a dictionary exists using <span
class="function">enchant\_broker\_dict\_exists</span> and request it.

``` php
<?php
$tag = 'en_US';
$broker = enchant_broker_init();
if (enchant_broker_dict_exists($broker,$tag)) {
    $dict = enchant_broker_request_dict($r, $tag);
}
?>
```

### 参见

-   <span class="function">enchant\_dict\_describe</span>
-   <span class="function">enchant\_broker\_dict\_exists</span>
-   <span class="function">enchant\_broker\_free\_dict</span>

enchant\_broker\_request\_pwl\_dict
===================================

Creates a dictionary using a PWL file

### 说明

<span class="type"><span class="type">EnchantDictionary</span><span
class="type">false</span></span> <span
class="methodname">enchant\_broker\_request\_pwl\_dict</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

Creates a dictionary using a PWL file. A PWL file is personal word file
one word per line.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

`filename`  
Path to the PWL file. If there is no such file, a new one will be
created if possible.

### 返回值

Returns a dictionary resource on success 或者在失败时返回 **`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                   |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected.                     |
| 8.0.0 | On success, this function returns an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was retured. |

### 参见

-   <span class="function">enchant\_dict\_describe</span>
-   <span class="function">enchant\_broker\_dict\_exists</span>
-   <span class="function">enchant\_broker\_free\_dict</span>

enchant\_broker\_set\_dict\_path
================================

Set the directory path for a given backend

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_broker\_set\_dict\_path</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> , <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">string</span> `$path`</span> )

Set the directory path for a given backend.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

`type`  
The type of the dictionaries, i.e. **`ENCHANT_MYSPELL`** or
**`ENCHANT_ISPELL`**.

`path`  
The path of the dictionary directory.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 参见

-   <span class="function">enchant\_broker\_get\_dict\_path</span>

enchant\_broker\_set\_ordering
==============================

Declares a preference of dictionaries to use for the language

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_broker\_set\_ordering</span> ( <span
class="methodparam"><span class="type">EnchantBroker</span>
`$broker`</span> , <span class="methodparam"><span
class="type">string</span> `$tag`</span> , <span
class="methodparam"><span class="type">string</span> `$ordering`</span>
)

Declares a preference of dictionaries to use for the language
described/referred to by 'tag'. The ordering is a comma delimited list
of provider names. As a special exception, the "\*" tag can be used as a
language tag to declare a default ordering for any language that does
not explicitly declare an ordering.

### 参数

`broker`  
An Enchant broker returned by <span
class="function">enchant\_broker\_init</span>.

`tag`  
Language tag. The special "\*" tag can be used as a language tag to
declare a default ordering for any language that does not explicitly
declare an ordering.

`ordering`  
Comma delimited list of provider names

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `broker` expects an <span class="classname">EnchantBroker</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

enchant\_dict\_add\_to\_personal
================================

Add a word to personal word list

### 说明

<span class="type">void</span> <span
class="methodname">enchant\_dict\_add\_to\_personal</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$word`</span> )

Add a word to personal word list of the given dictionary.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`word`  
The word to add

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

**示例 \#1 Adding a word to a PWL**

``` php
<?php

$filename = './my_word_list.pwl';
$word = 'Supercalifragilisticexpialidocious';

$broker = enchant_broker_init();
$dict = enchant_broker_request_pwl_dict($broker, $filename);

enchant_dict_add_to_personal($dict, $word);

enchant_broker_free($broker);

?>
```

### 参见

-   <span class="function">enchant\_broker\_request\_pwl\_dict</span>
-   <span class="function">enchant\_broker\_request\_dict</span>

enchant\_dict\_add\_to\_session
===============================

Add 'word' to this spell-checking session

### 说明

<span class="type">void</span> <span
class="methodname">enchant\_dict\_add\_to\_session</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$word`</span> )

Add a word to the given dictionary. It will be added only for the active
spell-checking session.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`word`  
The word to add

### 返回值

没有返回值。

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 参见

-   <span class="function">enchant\_broker\_request\_dict</span>

enchant\_dict\_check
====================

Check whether a word is correctly spelled or not

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_dict\_check</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$word`</span> )

If the word is correctly spelled return **`true`**, otherwise return
**`false`**

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`word`  
The word to check

### 返回值

Returns **`true`** if the word is spelled correctly, **`false`** if not.

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

enchant\_dict\_describe
=======================

Describes an individual dictionary

### 说明

<span class="type">array</span> <span
class="methodname">enchant\_dict\_describe</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> )

Returns the details of the dictionary.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |
| 8.0.0 | Prior to this version, the function returned **`false`** on failure.                                                                                                                       |

### 范例

**示例 \#1 A <span class="function">enchant\_dict\_describe</span>
example**

Check if a dictionary exists using <span
class="function">enchant\_broker\_dict\_exists</span> and show the
detail of it.

``` php
<?php
$tag = 'en_US';
$broker = enchant_broker_init();
if (enchant_broker_dict_exists($broker,$tag)) {
    $dict = enchant_broker_request_dict($r, $tag);
    $dict_details = enchant_dict_describe($dict);
    print_r($dict_details);
}
?>
```

以上例程的输出类似于：

    Array
    (
        [lang] => en_US
        [name] => aspell
        [desc] => Aspell Provider
        [file] => /usr/lib/enchant/libenchant_aspell.so
    )

enchant\_dict\_get\_error
=========================

Returns the last error of the current spelling-session

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">enchant\_dict\_get\_error</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> )

Returns the last error of the current spelling-session

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

### 返回值

Returns the error message as string or **`false`** if no error occurred.

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

enchant\_dict\_is\_in\_session
==============================

Whether or not 'word' exists in this spelling-session

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_dict\_is\_in\_session</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$word`</span> )

Tells whether or not a word already exists in the current session.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`word`  
The word to lookup

### 返回值

Returns **`true`** if the word exists or **`false`**

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 参见

-   <span class="function">enchant\_dict\_add\_to\_session</span>

enchant\_dict\_quick\_check
===========================

Check the word is correctly spelled and provide suggestions

### 说明

<span class="type">bool</span> <span
class="methodname">enchant\_dict\_quick\_check</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$word`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$suggestions`<span
class="initializer"> = **`null`**</span></span> \] )

If the word is correctly spelled return **`true`**, otherwise return
**`false`**, if suggestions variable is provided, fill it with spelling
alternatives.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`word`  
The word to check

`suggestions`  
If the word is not correctly spelled, this variable will contain an
array of suggestions.

### 返回值

Returns **`true`** if the word is correctly spelled or **`false`**

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 范例

**示例 \#1 A <span class="function">enchant\_dict\_quick\_check</span>
example**

``` php
<?php
$tag = 'en_US';
$r = enchant_broker_init();

if (enchant_broker_dict_exists($r,$tag)) {
    $d = enchant_broker_request_dict($r, $tag);
    enchant_dict_quick_check($d, 'soong', $suggs);
    print_r($suggs);
}
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => song
        [1] => snog
        [2] => soon
        [3] => Sang
        [4] => Sung
        [5] => sang
        [6] => sung
        [7] => sponge
        [8] => spongy
        [9] => snag
        [10] => snug
        [11] => sonic
        [12] => sing
        [13] => songs
        [14] => Son
        [15] => Sonja
        [16] => Synge
        [17] => son
        [18] => Sejong
        [19] => sarong
        [20] => sooner
        [21] => Sony
        [22] => sown
        [23] => scone
        [24] => song's
    )

### 参见

-   <span class="function">enchant\_dict\_check</span>
-   <span class="function">enchant\_dict\_suggest</span>

enchant\_dict\_store\_replacement
=================================

Add a correction for a word

### 说明

<span class="type">void</span> <span
class="methodname">enchant\_dict\_store\_replacement</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$misspelled`</span> , <span
class="methodparam"><span class="type">string</span> `$correct`</span> )

Add a correction for 'mis' using 'cor'. Notes that you replaced @mis
with @cor, so it's possibly more likely that future occurrences of @mis
will be replaced with @cor. So it might bump @cor up in the suggestion
list.

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`misspelled`  
The work to fix

`correct`  
The correct word

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

enchant\_dict\_suggest
======================

Will return a list of values if any of those pre-conditions are not met

### 说明

<span class="type">array</span> <span
class="methodname">enchant\_dict\_suggest</span> ( <span
class="methodparam"><span class="type">EnchantDictionary</span>
`$dictionary`</span> , <span class="methodparam"><span
class="type">string</span> `$word`</span> )

### 参数

`dictionary`  
An Enchant dictionary returned by <span
class="function">enchant\_broker\_request\_dict</span> or <span
class="function">enchant\_broker\_request\_pwl\_dict</span>.

`word`  
Word to use for the suggestions.

### 返回值

Will returns an array of suggestions if the word is bad spelled.

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0 | `dictionary` expects an <span class="classname">EnchantDictionary</span> instance now; previoulsy, a <a href="/language/types/resource.html" class="link">资源(resource)</a> was expected. |

### 范例

**示例 \#1 A <span class="function">enchant\_dict\_suggest</span>
example**

``` php
<?php
$tag = 'en_US';
$r = enchant_broker_init();
if (enchant_broker_dict_exists($r,$tag)) {
    $d = enchant_broker_request_dict($r, $tag);

    $wordcorrect = enchant_dict_check($d, "soong");
    if (!$wordcorrect) {
        $suggs = enchant_dict_suggest($d, "soong");
        echo "Suggestions for 'soong':";
        print_r($suggs);
    }
    enchant_broker_free_dict($d);
}
enchant_broker_free($r);
?>
```

### 参见

-   <span class="function">enchant\_dict\_check</span>
-   <span class="function">enchant\_dict\_quick\_check</span>

**目录**

-   [enchant\_broker\_describe](/ref/enchant.html#enchant_broker_describe)
    — Enumerates the Enchant providers
-   [enchant\_broker\_dict\_exists](/ref/enchant.html#enchant_broker_dict_exists)
    — Whether a dictionary exists or not. Using non-empty tag
-   [enchant\_broker\_free\_dict](/ref/enchant.html#enchant_broker_free_dict)
    — Free a dictionary resource
-   [enchant\_broker\_free](/ref/enchant.html#enchant_broker_free) —
    Free the broker resource and its dictionaries
-   [enchant\_broker\_get\_dict\_path](/ref/enchant.html#enchant_broker_get_dict_path)
    — Get the directory path for a given backend
-   [enchant\_broker\_get\_error](/ref/enchant.html#enchant_broker_get_error)
    — Returns the last error of the broker
-   [enchant\_broker\_init](/ref/enchant.html#enchant_broker_init) —
    Create a new broker object capable of requesting
-   [enchant\_broker\_list\_dicts](/ref/enchant.html#enchant_broker_list_dicts)
    — Returns a list of available dictionaries
-   [enchant\_broker\_request\_dict](/ref/enchant.html#enchant_broker_request_dict)
    — Create a new dictionary using a tag
-   [enchant\_broker\_request\_pwl\_dict](/ref/enchant.html#enchant_broker_request_pwl_dict)
    — Creates a dictionary using a PWL file
-   [enchant\_broker\_set\_dict\_path](/ref/enchant.html#enchant_broker_set_dict_path)
    — Set the directory path for a given backend
-   [enchant\_broker\_set\_ordering](/ref/enchant.html#enchant_broker_set_ordering)
    — Declares a preference of dictionaries to use for the language
-   [enchant\_dict\_add\_to\_personal](/ref/enchant.html#enchant_dict_add_to_personal)
    — Add a word to personal word list
-   [enchant\_dict\_add\_to\_session](/ref/enchant.html#enchant_dict_add_to_session)
    — Add 'word' to this spell-checking session
-   [enchant\_dict\_check](/ref/enchant.html#enchant_dict_check) — Check
    whether a word is correctly spelled or not
-   [enchant\_dict\_describe](/ref/enchant.html#enchant_dict_describe) —
    Describes an individual dictionary
-   [enchant\_dict\_get\_error](/ref/enchant.html#enchant_dict_get_error)
    — Returns the last error of the current spelling-session
-   [enchant\_dict\_is\_in\_session](/ref/enchant.html#enchant_dict_is_in_session)
    — Whether or not 'word' exists in this spelling-session
-   [enchant\_dict\_quick\_check](/ref/enchant.html#enchant_dict_quick_check)
    — Check the word is correctly spelled and provide suggestions
-   [enchant\_dict\_store\_replacement](/ref/enchant.html#enchant_dict_store_replacement)
    — Add a correction for a word
-   [enchant\_dict\_suggest](/ref/enchant.html#enchant_dict_suggest) —
    Will return a list of values if any of those pre-conditions are not
    met
