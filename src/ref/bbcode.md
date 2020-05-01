bbcode\_add\_element
====================

Adds a bbcode element

### 说明

<span class="type">bool</span> <span
class="methodname">bbcode\_add\_element</span> ( <span
class="methodparam"><span class="type">resource</span>
`$bbcode_container`</span> , <span class="methodparam"><span
class="type">string</span> `$tag_name`</span> , <span
class="methodparam"><span class="type">array</span> `$tag_rules`</span>
)

Adds a tag to an existing BBCode\_Container tag\_set using tag\_rules.

### 参数

`bbcode_container`  
BBCode\_Container resource, returned by <span
class="function">bbcode\_create</span>.

`tag_name`  
The new tag to add to the BBCode\_Container tag\_set.

`tag_rules`  
An associative array containing the parsing rules; see <span
class="function">bbcode\_create</span> for the available keys.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

bbcode\_add\_smiley
===================

Adds a smiley to the parser

### 说明

<span class="type">bool</span> <span
class="methodname">bbcode\_add\_smiley</span> ( <span
class="methodparam"><span class="type">resource</span>
`$bbcode_container`</span> , <span class="methodparam"><span
class="type">string</span> `$smiley`</span> , <span
class="methodparam"><span class="type">string</span>
`$replace_by`</span> )

Adds a smiley to the parser

### 参数

`bbcode_container`  
BBCode\_Container resource, returned by <span
class="function">bbcode\_create</span>.

`smiley`  
The string that will be replaced when found.

`replace_by`  
The string that replace smiley when found.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bbcode\_add\_smiley</span> usage
example**

``` php
<?php
/*
 * Prepare the rule set 
 */
$arrayBBCode=array(
    ''=>         array('type'=>BBCODE_TYPE_ROOT,  
                       'childs'=>'!i'),
    'b'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<b>', 
                       'close_tag'=>'</b>'),
    'u'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<u>', 
                       'close_tag'=>'</u>', 
                       'flags'=>BBCODE_FLAGS_SMILEYS_OFF),
    'i'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<i>', 
                       'close_tag'=>'</i>', 
                       'childs'=>'b'),
);
/* 
 * Parsed Text
 */
$text=<<<EOF
[i] No parse Test [/i] :)
[b] Parsed, with smiley :( [/b]
[u] Parsed, with no smiley :D [/u]
EOF;
/*
 * Init the parser
 */
$BBHandler=bbcode_create($arrayBBCode);
/*
 * Add Smiley rules to parser
 */
bbcode_add_smiley($BBHandler, ":)", "<img src=\"smiley.gif\" alt=\":)\" />");
bbcode_add_smiley($BBHandler, ":(", "<img src=\"sad.gif\" alt=\":(\" />");
bbcode_add_smiley($BBHandler, ":D", "<img src=\"happy.gif\" alt=\":D\" />");
bbcode_add_smiley($BBHandler, ":p", "<img src=\"tong.gif\" alt=\":p\" />");
bbcode_add_smiley($BBHandler, ":|", "<img src=\"special.gif\" alt=\":|\" />");
bbcode_add_smiley($BBHandler, ":6:", "<img src=\"six.gif\" alt=\":6:\" />");
/*
 * Parse the text
 */
echo bbcode_parse($BBHandler,$text);
?>
```

以上例程会输出：

    <i> No parse Test </i> <img src="smiley.gif" alt=":)" />
    <b> Parsed, with smiley <img src="sad.gif" alt=":(" /> </b>
    <u> Parsed, with no smiley :D </u>

bbcode\_create
==============

Create a BBCode Resource

### 说明

<span class="type">resource</span> <span
class="methodname">bbcode\_create</span> (\[ <span
class="methodparam"><span class="type">array</span>
`$bbcode_initial_tags`<span class="initializer"> = NULL</span></span> \]
)

This function returns a new BBCode Resource used to parse BBCode
strings.

### 参数

`bbcode_initial_tags`  
An associative array containing the tag names as keys and parameters
required to correctly parse BBCode as their value. The following
key/value pairs are supported:

-   <span class="simpara"> `flags` optional - a flag set based on the
    BBCODE\_FLAGS\_\* constants. </span>
-   <span class="simpara"> `type` required - an int indicating the type
    of tag. Use the BBCODE\_TYPE\_\* constants. </span>
-   <span class="simpara"> `open_tag` required - the HTML replacement
    string for the open tag. </span>
-   <span class="simpara"> `close_tag` required - the HTML replacement
    string for the close tag. </span>
-   <span class="simpara"> `default_arg` optional - use this value as
    the default argument if none is provided and tag\_type is of type
    OPTARG. </span>
-   <span class="simpara"> `content_handling` optional - Gives the
    callback used for modification of the content. Object Oriented
    Notation supported only since 0.10.1 callback prototype is string
    name*(string $content, string $argument)* </span>
-   <span class="simpara"> `param_handling` optional - Gives the
    callback used for modification of the argument. Object Oriented
    Notation supported only since 0.10.1 callback prototype is string
    name*(string $content, string $argument)* </span>
-   <span class="simpara"> `childs` optional - List of accepted children
    for the tag. The format of the list is a comma separated string. If
    the list starts with ! it will be the list of rejected children for
    the tag. </span>
-   <span class="simpara"> `parent` optional - List of accepted parents
    for the tag. The format of the list is a comma separated string.
    </span>

### 返回值

Returns a BBCode\_Container

### 范例

**示例 \#1 <span class="function">bbcode\_create</span> example**

``` php
<?php
$arrayBBCode=array(
    ''=>         array('type'=>BBCODE_TYPE_ROOT,  'childs'=>'!i'),
    'i'=>        array('type'=>BBCODE_TYPE_NOARG, 'open_tag'=>'<i>',
                    'close_tag'=>'</i>', 'childs'=>'b'),
    'url'=>      array('type'=>BBCODE_TYPE_OPTARG,
                    'open_tag'=>'<a href="{PARAM}">', 'close_tag'=>'</a>',
                    'default_arg'=>'{CONTENT}',
                    'childs'=>'b,i'),
    'img'=>      array('type'=>BBCODE_TYPE_NOARG,
                    'open_tag'=>'<img src="', 'close_tag'=>'" />',
                    'childs'=>''),
    'b'=>        array('type'=>BBCODE_TYPE_NOARG, 'open_tag'=>'<b>',
                    'close_tag'=>'</b>'),
);
$text=<<<EOF
[b]Bold Text[/b]
[i]Italic Text[/i]
[url]http://www.php.net/[/url]
[url=http://pecl.php.net/][b]Content Text[/b][/url]
[img]http://static.php.net/www.php.net/images/php.gif[/img]
[url=http://www.php.net/]
[img]http://static.php.net/www.php.net/images/php.gif[/img]
[/url]
EOF;
$BBHandler=bbcode_create($arrayBBCode);
echo bbcode_parse($BBHandler,$text);
?>
```

以上例程会输出：

    <b>Bold Text</b>
    [i]Italic Text[/i]
    <a href="http://www.php.net/">http://www.php.net/</a>
    <a href="http://pecl.php.net/"><b>Content Text</b></a>
    <img src="http://static.php.net/www.php.net/images/php.gif" />
    <a href="http://www.php.net/">
    [img]http://static.php.net/www.php.net/images/php.gif[/img]
    </a>

bbcode\_destroy
===============

Close BBCode\_container resource

### 说明

<span class="type">bool</span> <span
class="methodname">bbcode\_destroy</span> ( <span
class="methodparam"><span class="type">resource</span>
`$bbcode_container`</span> )

This function closes the resource opened by <span
class="function">bbcode\_create</span>.

### 参数

`bbcode_container`  
BBCode\_Container resource returned by <span
class="function">bbcode\_create</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

bbcode\_parse
=============

Parse a string following a given rule set

### 说明

<span class="type">string</span> <span
class="methodname">bbcode\_parse</span> ( <span
class="methodparam"><span class="type">resource</span>
`$bbcode_container`</span> , <span class="methodparam"><span
class="type">string</span> `$to_parse`</span> )

This function parse the string to\_parse following the rules in the
bbcode\_container created by <span
class="function">bbcode\_create</span>

### 参数

`bbcode_container`  
BBCode\_Container resource returned by <span
class="function">bbcode\_create</span>.

`to_parse`  
The string we need to parse.

### 返回值

Returns the parsed string, 或者在失败时返回 **`FALSE`**.

bbcode\_set\_arg\_parser
========================

Attach another parser in order to use another rule set for argument
parsing

### 说明

<span class="type">bool</span> <span
class="methodname">bbcode\_set\_arg\_parser</span> ( <span
class="methodparam"><span class="type">resource</span>
`$bbcode_container`</span> , <span class="methodparam"><span
class="type">resource</span> `$bbcode_arg_parser`</span> )

Attaches another parser to the bbcode\_container. This parser is used
only when arguments must be parsed. If this function is not used, the
default argument parser is the parser itself.

### 参数

`bbcode_container`  
BBCode\_Container resource, returned by <span
class="function">bbcode\_create</span>.

`bbcode_arg_parser`  
BBCode\_Container resource, returned by <span
class="function">bbcode\_create</span>. It will be used only for parsed
arguments

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bbcode\_set\_arg\_parser</span> usage
example**

``` php
<?php
/*
 * Generating bbcode ruleset for main parser 
 */
$arrayBBCode=array(
    'quote'=>    array('type'=>BBCODE_TYPE_ARG,
                       'open_tag'=>'<quote><h4>Source: {PARAM}</h4>', 
                       'close_tag'=>'</quote>',
                       'flags'=>BBCODE_FLAGS_REMOVE_IF_EMPTY|BBCODE_FLAGS_ARG_PARSING),
    'b'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<b>', 'close_tag'=>'</b>', 
                       'flags'=>BBCODE_FLAGS_REMOVE_IF_EMPTY),
    'u'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<u>', 'close_tag'=>'</u>', 
                       'flags'=>BBCODE_FLAGS_SMILEYS_OFF | BBCODE_FLAGS_REMOVE_IF_EMPTY | BBCODE_FLAGS_SMILEYS_OFF),
    'i'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<i>', 'close_tag'=>'</i>', 
                       'flags'=>BBCODE_FLAGS_REMOVE_IF_EMPTY),
);
/*
 * Generating bbcode ruleset for argument parser 
 */
$arrayBBCode_arg=array(
    'b'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<b class="sub">', 'close_tag'=>'</b>', 
                       'flags'=>BBCODE_FLAGS_REMOVE_IF_EMPTY),
    'u'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<u>', 'close_tag'=>'</u>',
                       'flags'=>BBCODE_FLAGS_SMILEYS_OFF | BBCODE_FLAGS_REMOVE_IF_EMPTY | BBCODE_FLAGS_SMILEYS_OFF),
    'i'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<i>', 'close_tag'=>'</i>', 
                       'flags'=>BBCODE_FLAGS_REMOVE_IF_EMPTY),
);
/*
 * Text we are going to parse
 */
$text=<<<EOF
[quote="[b]Test[/b]"]
Foo :)
[/quote]
[b]Bar example :)[/b] :)
EOF;
/*
 * Init the two parsers
 */
$BBHandler=bbcode_create($arrayBBCode);
$BBArgHandler=bbcode_create($arrayBBCode_arg);
/*
 * Setting Flags on the parsers
 */
bbcode_set_flags($BBHandler,
                 BBCODE_CORRECT_REOPEN_TAGS|BBCODE_DEFAULT_SMILEYS_ON|BBCODE_ARG_DOUBLE_QUOTE|
                 BBCODE_ARG_SINGLE_QUOTE|BBCODE_ARG_HTML_QUOTE,BBCODE_SET_FLAGS_SET);
bbcode_set_flags($BBArgHandler,
                 BBCODE_CORRECT_REOPEN_TAGS|BBCODE_DEFAULT_SMILEYS_ON|BBCODE_ARG_DOUBLE_QUOTE|
                 BBCODE_ARG_SINGLE_QUOTE|BBCODE_ARG_HTML_QUOTE,BBCODE_SET_FLAGS_SET);
/*
 * Setting $BBArgHandler as the BBHandler argument parser
 */
bbcode_set_arg_parser($BBHandler,$BBArgHandler);
/*
 * Adding Smileys handling rules to Main parser
 */
bbcode_add_smiley($BBHandler, ":)", "<img src=\"smiley.gif\" alt=\":)\" />");
/*
 * Use the main parser to parse text
 */
echo bbcode_parse($BBHandler,$text);
?>
```

以上例程会输出：

    <quote><h4>Source: <b class="sub">Test</b></h4>
    Foo <img src="smiley.gif" alt=":)" />
    </quote>
    <b>Bar example :)</b> <img src="smiley.gif" alt=":)" />

bbcode\_set\_flags
==================

Set or alter parser options

### 说明

<span class="type">bool</span> <span
class="methodname">bbcode\_set\_flags</span> ( <span
class="methodparam"><span class="type">resource</span>
`$bbcode_container`</span> , <span class="methodparam"><span
class="type">int</span> `$flags`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = BBCODE\_SET\_FLAGS\_SET</span></span> \] )

Set or alter parser options

### 参数

`bbcode_container`  
BBCode\_Container resource, returned by <span
class="function">bbcode\_create</span>.

`flags`  
The flag set that must be applied to the bbcode\_container options

`mode`  
One of the BBCODE\_SET\_FLAGS\_\* constant to set, unset a specific flag
set or to replace the flag set by flags.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">bbcode\_set\_flags</span> usage
example**

``` php
<?php
/*
 * Preparing RuleSet
 */
$arrayBBCode=array(
    'b'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<b>', 'close_tag'=>'</b>'),
    'u'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<u>', 'close_tag'=>'</u>'),
    'i'=>        array('type'=>BBCODE_TYPE_NOARG, 
                       'open_tag'=>'<i>', 'close_tag'=>'</i>'),
);
/*
 * Paired incorrectly nested BBCode 
 */
$text="[i] Parser [b] Auto Correction [/i] at work [/b]\n";
$BBHandler=bbcode_create($arrayBBCode);
echo bbcode_parse($BBHandler,$text);
// Enabling reopening of automatically closed elements
bbcode_set_flags($BBHandler,BBCODE_CORRECT_REOPEN_TAGS, 
                 BBCODE_SET_FLAGS_SET);
echo bbcode_parse($BBHandler,$text);

/*
 * Unpaired incorrectly nested BBCode 
 */
$text="[i] Parser [b] Auto Correction [/i] at work\n";
echo bbcode_parse($BBHandler,$text);
// Enabling automatic close of pending tags
bbcode_set_flags($BBHandler,
                 BBCODE_CORRECT_REOPEN_TAGS|BBCODE_AUTO_CORRECT, 
                 BBCODE_SET_FLAGS_SET);
echo bbcode_parse($BBHandler,$text);
?>
```

以上例程会输出：

    <i> Parser <b> Auto Correction </b></i> at work 
    <i> Parser <b> Auto Correction </b></i><b> at work </b>
    <i> Parser [b] Auto Correction </i> at work
    <i> Parser <b> Auto Correction </b></i><b> at work
    </b>

**目录**

-   [bbcode\_add\_element](/ref/bbcode.html#bbcode_add_element) — Adds a
    bbcode element
-   [bbcode\_add\_smiley](/ref/bbcode.html#bbcode_add_smiley) — Adds a
    smiley to the parser
-   [bbcode\_create](/ref/bbcode.html#bbcode_create) — Create a BBCode
    Resource
-   [bbcode\_destroy](/ref/bbcode.html#bbcode_destroy) — Close
    BBCode\_container resource
-   [bbcode\_parse](/ref/bbcode.html#bbcode_parse) — Parse a string
    following a given rule set
-   [bbcode\_set\_arg\_parser](/ref/bbcode.html#bbcode_set_arg_parser) —
    Attach another parser in order to use another rule set for argument
    parsing
-   [bbcode\_set\_flags](/ref/bbcode.html#bbcode_set_flags) — Set or
    alter parser options
