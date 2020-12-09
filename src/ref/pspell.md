pspell\_add\_to\_personal
=========================

Add the word to a personal wordlist

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_add\_to\_personal</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> ,
<span class="methodparam"><span class="type">string</span>
`$word`</span> )

<span class="function">pspell\_add\_to\_personal</span> adds a word to
the personal wordlist. If you used <span
class="function">pspell\_new\_config</span> with <span
class="function">pspell\_config\_personal</span> to open the dictionary,
you can save the wordlist later with <span
class="function">pspell\_save\_wordlist</span>.

### 参数

`dictionary`  

`word`  
The added word.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_add\_to\_personal</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell_link = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell_link, "Vlad");
pspell_save_wordlist($pspell_link);
?>
```

### 注释

> **Note**:
>
> This function will not work unless you have pspell .11.2 and aspell
> .32.5 or later.

pspell\_add\_to\_session
========================

Add the word to the wordlist in the current session

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_add\_to\_session</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> ,
<span class="methodparam"><span class="type">string</span>
`$word`</span> )

<span class="function">pspell\_add\_to\_session</span> adds a word to
the wordlist associated with the current session. It is very similar to
<span class="function">pspell\_add\_to\_personal</span>

### 参数

`dictionary`  

`word`  
The added word.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

pspell\_check
=============

Check a word

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_check</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> ,
<span class="methodparam"><span class="type">string</span>
`$word`</span> )

<span class="function">pspell\_check</span> checks the spelling of a
word.

### 参数

`dictionary`  

`word`  
The tested word.

### 返回值

Returns **`true`** if the spelling is correct, **`false`** if not.

### 范例

**示例 \#1 <span class="function">pspell\_check</span> Example**

``` php
<?php
$pspell_link = pspell_new("en");

if (pspell_check($pspell_link, "testt")) {
    echo "This is a valid spelling";
} else {
    echo "Sorry, wrong spelling";
}
?>
```

pspell\_clear\_session
======================

Clear the current session

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_clear\_session</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> )

<span class="function">pspell\_clear\_session</span> clears the current
session. The current wordlist becomes blank, and, for example, if you
try to save it with <span
class="function">pspell\_save\_wordlist</span>, nothing happens.

### 参数

`dictionary`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_add\_to\_personal</span>
Example**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell_link = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell_link, "Vlad");
pspell_clear_session($pspell_link);
pspell_save_wordlist($pspell_link);    //"Vlad" will not be saved
?>
```

pspell\_config\_create
======================

Create a config used to open a dictionary

### 说明

<span class="type">int</span> <span
class="methodname">pspell\_config\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$language`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$spelling`<span class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$jargon`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = ""</span></span> \]\]\] )

Create a config used to open a dictionary.

<span class="function">pspell\_config\_create</span> has a very similar
syntax to <span class="function">pspell\_new</span>. In fact, using
<span class="function">pspell\_config\_create</span> immediately
followed by <span class="function">pspell\_new\_config</span> will
produce the exact same result. However, after creating a new config, you
can also use <span class="function">pspell\_config\_\*</span> functions
before calling <span class="function">pspell\_new\_config</span> to take
advantage of some advanced functionality.

For more information and examples, check out inline manual pspell
website:<a href="http://aspell.net/" class="link external">» http://aspell.net/</a>.

### 参数

`language`  
The language parameter is the language code which consists of the two
letter ISO 639 language code and an optional two letter ISO 3166 country
code after a dash or underscore.

`spelling`  
The spelling parameter is the requested spelling for languages with more
than one spelling such as English. Known values are 'american',
'british', and 'canadian'.

`jargon`  
The jargon parameter contains extra information to distinguish two
different words lists that have the same language and spelling
parameters.

`encoding`  
The encoding parameter is the encoding that words are expected to be in.
Valid values are 'utf-8', 'iso8859-\*', 'koi8-r', 'viscii', 'cp1252',
'machine unsigned 16', 'machine unsigned 32'. This parameter is largely
untested, so be careful when using.

### 返回值

Returns a pspell config identifier, or **`false`** on error.

### 范例

**示例 \#1 <span class="function">pspell\_config\_create</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell_link = pspell_new_personal($pspell_config, "en");
?>
```

pspell\_config\_data\_dir
=========================

Location of language data files

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_data\_dir</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

pspell\_config\_dict\_dir
=========================

Location of the main word list

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_dict\_dir</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

pspell\_config\_ignore
======================

Ignore words less than N characters long

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_ignore</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">int</span>
`$min_length`</span> )

<span class="function">pspell\_config\_ignore</span> should be used on a
config before calling <span class="function">pspell\_new\_config</span>.
This function allows short words to be skipped by the spell checker.

### 参数

`config`  

`min_length`  
Words less than `min_length` characters will be skipped.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_config\_ignore</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_ignore($pspell_config, 5);
$pspell_link = pspell_new_config($pspell_config);
pspell_check($pspell_link, "abcd");    //will not result in an error
?>
```

pspell\_config\_mode
====================

Change the mode number of suggestions returned

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_mode</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="function">pspell\_config\_mode</span> should be used on a
config before calling <span class="function">pspell\_new\_config</span>.
This function determines how many suggestions will be returned by <span
class="function">pspell\_suggest</span>.

### 参数

`config`  

`mode`  
The mode parameter is the mode in which spellchecker will work. There
are several modes available:

-   <span class="simpara"> **`PSPELL_FAST`** - Fast mode (least number
    of suggestions) </span>
-   <span class="simpara"> **`PSPELL_NORMAL`** - Normal mode (more
    suggestions) </span>
-   <span class="simpara"> **`PSPELL_BAD_SPELLERS`** - Slow mode (a lot
    of suggestions) </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_config\_mode</span> Example**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_mode($pspell_config, PSPELL_FAST);
$pspell_link = pspell_new_config($pspell_config);
pspell_check($pspell_link, "thecat");
?>
```

pspell\_config\_personal
========================

Set a file that contains personal wordlist

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_personal</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Set a file that contains personal wordlist. The personal wordlist will
be loaded and used in addition to the standard one after you call <span
class="function">pspell\_new\_config</span>. The file is also the file
where <span class="function">pspell\_save\_wordlist</span> will save
personal wordlist to.

<span class="function">pspell\_config\_personal</span> should be used on
a config before calling <span
class="function">pspell\_new\_config</span>.

### 参数

`config`  

`filename`  
The personal wordlist. If the file does not exist, it will be created.
The file should be writable by whoever PHP runs as (e.g. nobody).

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_config\_personal</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
$pspell_link = pspell_new_config($pspell_config);
pspell_check($pspell_link, "thecat");
?>
```

### 注释

> **Note**:
>
> This function will not work unless you have pspell .11.2 and aspell
> .32.5 or later.

pspell\_config\_repl
====================

Set a file that contains replacement pairs

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_repl</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Set a file that contains replacement pairs.

The replacement pairs improve the quality of the spellchecker. When a
word is misspelled, and a proper suggestion was not found in the list,
<span class="function">pspell\_store\_replacement</span> can be used to
store a replacement pair and then <span
class="function">pspell\_save\_wordlist</span> to save the wordlist
along with the replacement pairs.

<span class="function">pspell\_config\_repl</span> should be used on a
config before calling <span class="function">pspell\_new\_config</span>.

### 参数

`config`  

`filename`  
The file should be writable by whoever PHP runs as (e.g. nobody).

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_config\_repl</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell_link = pspell_new_config($pspell_config);
pspell_check($pspell_link, "thecat");
?>
```

### 注释

> **Note**:
>
> This function will not work unless you have pspell .11.2 and aspell
> .32.5 or later.

pspell\_config\_runtogether
===========================

Consider run-together words as valid compounds

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_runtogether</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">bool</span> `$allow`</span>
)

This function determines whether run-together words will be treated as
legal compounds. That is, "thecat" will be a legal compound, although
there should be a space between the two words. Changing this setting
only affects the results returned by <span
class="function">pspell\_check</span>; <span
class="function">pspell\_suggest</span> will still return suggestions.

<span class="function">pspell\_config\_runtogether</span> should be used
on a config before calling <span
class="function">pspell\_new\_config</span>.

### 参数

`config`  

`allow`  
**`true`** if run-together words should be treated as legal compounds,
**`false`** otherwise.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_config\_runtogether</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_runtogether($pspell_config, true);
$pspell_link = pspell_new_config($pspell_config);
pspell_check($pspell_link, "thecat");
?>
```

pspell\_config\_save\_repl
==========================

Determine whether to save a replacement pairs list along with the
wordlist

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_config\_save\_repl</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> ,
<span class="methodparam"><span class="type">bool</span> `$save`</span>
)

<span class="function">pspell\_config\_save\_repl</span> determines
whether <span class="function">pspell\_save\_wordlist</span> will save
the replacement pairs along with the wordlist. Usually there is no need
to use this function because if <span
class="function">pspell\_config\_repl</span> is used, the replacement
pairs will be saved by <span
class="function">pspell\_save\_wordlist</span> anyway, and if it is not,
the replacement pairs will not be saved.

<span class="function">pspell\_config\_save\_repl</span> should be used
on a config before calling <span
class="function">pspell\_new\_config</span>.

### 参数

`config`  

`save`  
**`true`** if replacement pairs should be saved, **`false`** otherwise.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 注释

> **Note**:
>
> This function will not work unless you have pspell .11.2 and aspell
> .32.5 or later.

pspell\_new\_config
===================

Load a new dictionary with settings based on a given config

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">pspell\_new\_config</span> ( <span
class="methodparam"><span class="type">int</span> `$config`</span> )

<span class="function">pspell\_new\_config</span> opens up a new
dictionary with settings specified in a config, created with <span
class="function">pspell\_config\_create</span> and modified with <span
class="function">pspell\_config\_\*</span> functions. This method
provides you with the most flexibility and has all the functionality
provided by <span class="function">pspell\_new</span> and <span
class="function">pspell\_new\_personal</span>.

### 参数

`config`  
The `config` parameter is the one returned by <span
class="function">pspell\_config\_create</span> when the config was
created.

### 返回值

Returns a dictionary link identifier on success, 或者在失败时返回
**`false`**.

### 范例

**示例 \#1 <span class="function">pspell\_new\_config</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell_link = pspell_new_config($pspell_config);
?>
```

pspell\_new\_personal
=====================

Load a new dictionary with personal wordlist

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">pspell\_new\_personal</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$language`</span> \[, <span class="methodparam"><span
class="type">string</span> `$spelling`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$jargon`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
0</span></span> \]\]\]\] )

<span class="function">pspell\_new\_personal</span> opens up a new
dictionary with a personal wordlist. The wordlist can be modified and
saved with <span class="function">pspell\_save\_wordlist</span>, if
desired. However, the replacement pairs are not saved. In order to save
replacement pairs, you should create a config using <span
class="function">pspell\_config\_create</span>, set the personal
wordlist file with <span
class="function">pspell\_config\_personal</span>, set the file for
replacement pairs with <span
class="function">pspell\_config\_repl</span>, and open a new dictionary
with <span class="function">pspell\_new\_config</span>.

For more information and examples, check out inline manual pspell
website:<a href="http://aspell.net/" class="link external">» http://aspell.net/</a>.

### 参数

`filename`  
The file where words added to the personal list will be stored. It
should be an absolute filename beginning with '/' because otherwise it
will be relative to $HOME, which is "/root" for most systems, and is
probably not what you want.

`language`  
The language code which consists of the two letter ISO 639 language code
and an optional two letter ISO 3166 country code after a dash or
underscore.

`spelling`  
The requested spelling for languages with more than one spelling such as
English. Known values are 'american', 'british', and 'canadian'.

`jargon`  
Extra information to distinguish two different words lists that have the
same language and spelling parameters.

`encoding`  
The encoding that words are expected to be in. Valid values are *utf-8*,
*iso8859-\**, *koi8-r*, *viscii*, *cp1252*, *machine unsigned 16*,
*machine unsigned 32*.

`mode`  
The mode in which spellchecker will work. There are several modes
available:

-   <span class="simpara"> **`PSPELL_FAST`** - Fast mode (least number
    of suggestions) </span>
-   <span class="simpara"> **`PSPELL_NORMAL`** - Normal mode (more
    suggestions) </span>
-   <span class="simpara"> **`PSPELL_BAD_SPELLERS`** - Slow mode (a lot
    of suggestions) </span>
-   <span class="simpara"> **`PSPELL_RUN_TOGETHER`** - Consider
    run-together words as legal compounds. That is, "thecat" will be a
    legal compound, although there should be a space between the two
    words. Changing this setting only affects the results returned by
    <span class="function">pspell\_check</span>; <span
    class="function">pspell\_suggest</span> will still return
    suggestions. </span>

Mode is a bitmask constructed from different constants listed above.
However, **`PSPELL_FAST`**, **`PSPELL_NORMAL`** and
**`PSPELL_BAD_SPELLERS`** are mutually exclusive, so you should select
only one of them.

### 返回值

Returns the dictionary link identifier for use in other pspell
functions.

### 范例

**示例 \#1 <span class="function">pspell\_new\_personal</span>**

``` php
<?php
$pspell_link = pspell_new_personal ("/var/dictionaries/custom.pws",
        "en", "", "", "", PSPELL_FAST|PSPELL_RUN_TOGETHER);
?>
```

pspell\_new
===========

Load a new dictionary

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">pspell\_new</span> ( <span class="methodparam"><span
class="type">string</span> `$language`</span> \[, <span
class="methodparam"><span class="type">string</span> `$spelling`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$jargon`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$encoding`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = 0</span></span> \]\]\]\] )

<span class="function">pspell\_new</span> opens up a new dictionary and
returns the dictionary link identifier for use in other pspell
functions.

For more information and examples, check out inline manual pspell
website:<a href="http://aspell.net/" class="link external">» http://aspell.net/</a>.

### 参数

`language`  
The language parameter is the language code which consists of the two
letter ISO 639 language code and an optional two letter ISO 3166 country
code after a dash or underscore.

`spelling`  
The spelling parameter is the requested spelling for languages with more
than one spelling such as English. Known values are 'american',
'british', and 'canadian'.

`jargon`  
The jargon parameter contains extra information to distinguish two
different words lists that have the same language and spelling
parameters.

`encoding`  
The encoding parameter is the encoding that words are expected to be in.
Valid values are 'utf-8', 'iso8859-\*', 'koi8-r', 'viscii', 'cp1252',
'machine unsigned 16', 'machine unsigned 32'. This parameter is largely
untested, so be careful when using.

`mode`  
The mode parameter is the mode in which spellchecker will work. There
are several modes available:

-   <span class="simpara"> **`PSPELL_FAST`** - Fast mode (least number
    of suggestions) </span>
-   <span class="simpara"> **`PSPELL_NORMAL`** - Normal mode (more
    suggestions) </span>
-   <span class="simpara"> **`PSPELL_BAD_SPELLERS`** - Slow mode (a lot
    of suggestions) </span>
-   <span class="simpara"> **`PSPELL_RUN_TOGETHER`** - Consider
    run-together words as legal compounds. That is, "thecat" will be a
    legal compound, although there should be a space between the two
    words. Changing this setting only affects the results returned by
    <span class="function">pspell\_check</span>; <span
    class="function">pspell\_suggest</span> will still return
    suggestions. </span>

Mode is a bitmask constructed from different constants listed above.
However, **`PSPELL_FAST`**, **`PSPELL_NORMAL`** and
**`PSPELL_BAD_SPELLERS`** are mutually exclusive, so you should select
only one of them.

### 返回值

Returns the dictionary link identifier on success 或者在失败时返回
**`false`**.

### 范例

**示例 \#1 <span class="function">pspell\_new</span>**

``` php
<?php
$pspell_link = pspell_new("en", "", "", "",
                           (PSPELL_FAST|PSPELL_RUN_TOGETHER));
?>
```

pspell\_save\_wordlist
======================

Save the personal wordlist to a file

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_save\_wordlist</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> )

<span class="function">pspell\_save\_wordlist</span> saves the personal
wordlist from the current session. The location of files to be saved
specified with <span class="function">pspell\_config\_personal</span>
and (optionally) <span class="function">pspell\_config\_repl</span>.

### 参数

`dictionary`  
A dictionary link identifier opened with <span
class="function">pspell\_new\_personal</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_add\_to\_personal</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/tmp/dicts/newdict");
$pspell_link = pspell_new_config($pspell_config);

pspell_add_to_personal($pspell_link, "Vlad");
pspell_save_wordlist($pspell_link);
?>
```

### 注释

> **Note**:
>
> This function will not work unless you have pspell .11.2 and aspell
> .32.5 or later.

pspell\_store\_replacement
==========================

Store a replacement pair for a word

### 说明

<span class="type">bool</span> <span
class="methodname">pspell\_store\_replacement</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> ,
<span class="methodparam"><span class="type">string</span>
`$misspelled`</span> , <span class="methodparam"><span
class="type">string</span> `$correct`</span> )

<span class="function">pspell\_store\_replacement</span> stores a
replacement pair for a word, so that replacement can be returned by
<span class="function">pspell\_suggest</span> later. In order to be able
to take advantage of this function, you have to use <span
class="function">pspell\_new\_personal</span> to open the dictionary. In
order to permanently save the replacement pair, you have to use <span
class="function">pspell\_config\_personal</span> and <span
class="function">pspell\_config\_repl</span> to set the path where to
save your custom wordlists, and then use <span
class="function">pspell\_save\_wordlist</span> for the changes to be
written to disk.

### 参数

`dictionary`  
A dictionary link identifier, opened with <span
class="function">pspell\_new\_personal</span>

`misspelled`  
The misspelled word.

`correct`  
The fixed spelling for the `misspelled` word.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">pspell\_store\_replacement</span>**

``` php
<?php
$pspell_config = pspell_config_create("en");
pspell_config_personal($pspell_config, "/var/dictionaries/custom.pws");
pspell_config_repl($pspell_config, "/var/dictionaries/custom.repl");
$pspell_link = pspell_new_config($pspell_config);

pspell_store_replacement($pspell_link, $misspelled, $correct);
pspell_save_wordlist($pspell_link);
?>
```

### 注释

> **Note**:
>
> This function will not work unless you have pspell .11.2 and aspell
> .32.5 or later.

pspell\_suggest
===============

Suggest spellings of a word

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">pspell\_suggest</span> ( <span
class="methodparam"><span class="type">int</span> `$dictionary`</span> ,
<span class="methodparam"><span class="type">string</span>
`$word`</span> )

<span class="function">pspell\_suggest</span> returns an array of
possible spellings for the given word.

### 参数

`dictionary`  

`word`  
The tested word.

### 返回值

Returns an array of possible spellings.

### 范例

**示例 \#1 <span class="function">pspell\_suggest</span> example**

``` php
<?php
$pspell_link = pspell_new("en");

if (!pspell_check($pspell_link, "testt")) {
    $suggestions = pspell_suggest($pspell_link, "testt");

    foreach ($suggestions as $suggestion) {
        echo "Possible spelling: $suggestion<br />";
    }
}
?>
```

**目录**

-   [pspell\_add\_to\_personal](/ref/pspell.html#pspell_add_to_personal)
    — Add the word to a personal wordlist
-   [pspell\_add\_to\_session](/ref/pspell.html#pspell_add_to_session) —
    Add the word to the wordlist in the current session
-   [pspell\_check](/ref/pspell.html#pspell_check) — Check a word
-   [pspell\_clear\_session](/ref/pspell.html#pspell_clear_session) —
    Clear the current session
-   [pspell\_config\_create](/ref/pspell.html#pspell_config_create) —
    Create a config used to open a dictionary
-   [pspell\_config\_data\_dir](/ref/pspell.html#pspell_config_data_dir)
    — Location of language data files
-   [pspell\_config\_dict\_dir](/ref/pspell.html#pspell_config_dict_dir)
    — Location of the main word list
-   [pspell\_config\_ignore](/ref/pspell.html#pspell_config_ignore) —
    Ignore words less than N characters long
-   [pspell\_config\_mode](/ref/pspell.html#pspell_config_mode) — Change
    the mode number of suggestions returned
-   [pspell\_config\_personal](/ref/pspell.html#pspell_config_personal)
    — Set a file that contains personal wordlist
-   [pspell\_config\_repl](/ref/pspell.html#pspell_config_repl) — Set a
    file that contains replacement pairs
-   [pspell\_config\_runtogether](/ref/pspell.html#pspell_config_runtogether)
    — Consider run-together words as valid compounds
-   [pspell\_config\_save\_repl](/ref/pspell.html#pspell_config_save_repl)
    — Determine whether to save a replacement pairs list along with the
    wordlist
-   [pspell\_new\_config](/ref/pspell.html#pspell_new_config) — Load a
    new dictionary with settings based on a given config
-   [pspell\_new\_personal](/ref/pspell.html#pspell_new_personal) — Load
    a new dictionary with personal wordlist
-   [pspell\_new](/ref/pspell.html#pspell_new) — Load a new dictionary
-   [pspell\_save\_wordlist](/ref/pspell.html#pspell_save_wordlist) —
    Save the personal wordlist to a file
-   [pspell\_store\_replacement](/ref/pspell.html#pspell_store_replacement)
    — Store a replacement pair for a word
-   [pspell\_suggest](/ref/pspell.html#pspell_suggest) — Suggest
    spellings of a word
