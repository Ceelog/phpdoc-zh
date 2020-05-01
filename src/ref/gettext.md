bind\_textdomain\_codeset
=========================

Specify the character encoding in which the messages from the DOMAIN
message catalog will be returned

### 说明

<span class="type">string</span> <span
class="methodname">bind\_textdomain\_codeset</span> ( <span
class="methodparam"><span class="type">string</span> `$domain`</span> ,
<span class="methodparam"><span class="type">string</span>
`$codeset`</span> )

With <span class="function">bind\_textdomain\_codeset</span>, you can
set in which encoding will be messages from `domain` returned by <span
class="function">gettext</span> and similar functions.

### 参数

`domain`  
The domain

`codeset`  
The code set

### 返回值

A <span class="type">string</span> on success.

bindtextdomain
==============

Sets the path for a domain

### 说明

<span class="type">string</span> <span
class="methodname">bindtextdomain</span> ( <span
class="methodparam"><span class="type">string</span> `$domain`</span> ,
<span class="methodparam"><span class="type">string</span>
`$directory`</span> )

The <span class="function">bindtextdomain</span> function sets the path
for a domain.

### 参数

`domain`  
The domain

`directory`  
The directory path

### 返回值

The full pathname for the `domain` currently being set.

### 范例

**示例 \#1 <span class="function">bindtextdomain</span> example**

``` php
<?php

$domain = 'myapp';
echo bindtextdomain($domain, '/usr/share/myapp/locale');

?>
```

以上例程会输出：

    /usr/share/myapp/locale

dcgettext
=========

Overrides the domain for a single lookup

### 说明

<span class="type">string</span> <span
class="methodname">dcgettext</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$message`</span> ,
<span class="methodparam"><span class="type">int</span>
`$category`</span> )

This function allows you to override the current domain for a single
message lookup.

### 参数

`domain`  
The domain

`message`  
The message

`category`  
The category

### 返回值

A <span class="type">string</span> on success.

### 参见

-   <span class="function">gettext</span>

dcngettext
==========

Plural version of dcgettext

### 说明

<span class="type">string</span> <span
class="methodname">dcngettext</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$msgid1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$msgid2`</span> , <span class="methodparam"><span
class="type">int</span> `$n`</span> , <span class="methodparam"><span
class="type">int</span> `$category`</span> )

This function allows you to override the current domain for a single
plural message lookup.

### 参数

`domain`  
The domain

`msgid1`  

`msgid2`  

`n`  

`category`  

### 返回值

A <span class="type">string</span> on success.

### 参见

-   <span class="function">ngettext</span>

dgettext
========

Override the current domain

### 说明

<span class="type">string</span> <span
class="methodname">dgettext</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$message`</span> )

The <span class="function">dgettext</span> function allows you to
override the current `domain` for a single message lookup.

### 参数

`domain`  
The domain

`message`  
The message

### 返回值

A <span class="type">string</span> on success.

### 参见

-   <span class="function">gettext</span>

dngettext
=========

Plural version of dgettext

### 说明

<span class="type">string</span> <span
class="methodname">dngettext</span> ( <span class="methodparam"><span
class="type">string</span> `$domain`</span> , <span
class="methodparam"><span class="type">string</span> `$msgid1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$msgid2`</span> , <span class="methodparam"><span
class="type">int</span> `$n`</span> )

The <span class="function">dngettext</span> function allows you to
override the current `domain` for a single plural message lookup.

### 参数

`domain`  
The domain

`msgid1`  

`msgid2`  

`n`  

### 返回值

A <span class="type">string</span> on success.

### 参见

-   <span class="function">ngettext</span>

gettext
=======

Lookup a message in the current domain

### 说明

<span class="type">string</span> <span class="methodname">gettext</span>
( <span class="methodparam"><span class="type">string</span>
`$message`</span> )

Looks up a message in the current domain.

### 参数

`message`  
The message being translated.

### 返回值

Returns a translated <span class="type">string</span> if one is found in
the translation table, or the submitted message if not found.

### 范例

**示例 \#1 <span class="function">gettext</span>-check**

``` php
<?php
// Set language to German
putenv('LC_ALL=de_DE');
setlocale(LC_ALL, 'de_DE');

// Specify location of translation tables
bindtextdomain("myPHPApp", "./locale");

// Choose domain
textdomain("myPHPApp");

// Translation is looking for in ./locale/de_DE/LC_MESSAGES/myPHPApp.mo now

// Print a test message
echo gettext("Welcome to My PHP Application");

// Or use the alias _() for gettext()
echo _("Have a nice day");
?>
```

### 注释

> **Note**:
>
> You may use the underscore character '\_' as an alias to this
> function.

> **Note**:
>
> Setting a language isn't enough for some systems and the <span
> class="function">putenv</span> should be used to define the current
> locale.

### 参见

-   <span class="function">setlocale</span>

ngettext
========

Plural version of gettext

### 说明

<span class="type">string</span> <span
class="methodname">ngettext</span> ( <span class="methodparam"><span
class="type">string</span> `$msgid1`</span> , <span
class="methodparam"><span class="type">string</span> `$msgid2`</span> ,
<span class="methodparam"><span class="type">int</span> `$n`</span> )

The plural version of <span class="function">gettext</span>. Some
languages have more than one form for plural messages dependent on the
count.

### 参数

`msgid1`  
The singular message ID.

`msgid2`  
The plural message ID.

`n`  
The number (e.g. item count) to determine the translation for the
respective grammatical number.

### 返回值

Returns correct plural form of message identified by `msgid1` and
`msgid2` for count `n`.

### 范例

**示例 \#1 <span class="function">ngettext</span> example**

``` php
<?php

setlocale(LC_ALL, 'cs_CZ');
printf(ngettext("%d window", "%d windows", 1), 1); // 1 okno
printf(ngettext("%d window", "%d windows", 2), 2); // 2 okna
printf(ngettext("%d window", "%d windows", 5), 5); // 5 oken

?>
```

textdomain
==========

Sets the default domain

### 说明

<span class="type">string</span> <span
class="methodname">textdomain</span> ( <span class="methodparam"><span
class="type">string</span> `$text_domain`<span class="initializer"> =
**`NULL`**</span></span> )

This function sets the domain to search within when calls are made to
<span class="function">gettext</span>, usually the named after an
application.

### 参数

`text_domain`  
The new message domain, or **`NULL`** to get the current setting without
changing it

### 返回值

If successful, this function returns the current message domain, after
possibly changing it.

**目录**

-   [bind\_textdomain\_codeset](/ref/gettext.html#bind_textdomain_codeset)
    — Specify the character encoding in which the messages from the
    DOMAIN message catalog will be returned
-   [bindtextdomain](/ref/gettext.html#bindtextdomain) — Sets the path
    for a domain
-   [dcgettext](/ref/gettext.html#dcgettext) — Overrides the domain for
    a single lookup
-   [dcngettext](/ref/gettext.html#dcngettext) — Plural version of
    dcgettext
-   [dgettext](/ref/gettext.html#dgettext) — Override the current domain
-   [dngettext](/ref/gettext.html#dngettext) — Plural version of
    dgettext
-   [gettext](/ref/gettext.html#gettext) — Lookup a message in the
    current domain
-   [ngettext](/ref/gettext.html#ngettext) — Plural version of gettext
-   [textdomain](/ref/gettext.html#textdomain) — Sets the default domain
