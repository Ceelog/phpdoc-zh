预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`BBCODE_TYPE_NOARG`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode tag does not accept any arguments.
</span>

**`BBCODE_TYPE_SINGLE`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode tag does not have a corresponding
close tag. </span>

**`BBCODE_TYPE_ARG`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode tag need an argument. </span>

**`BBCODE_TYPE_OPTARG`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode tag accept an optional argument.
</span>

**`BBCODE_TYPE_ROOT`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode tag is the special tag root (nesting
level 0). </span>

**`BBCODE_FLAGS_ARG_PARSING`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode tag require argument sub-parsing (the
argument is also parsed by the BBCode extension). As Of 0.10.2 another
parser can be used as argument parser. </span>

**`BBCODE_FLAGS_CDATA_NOT_ALLOWED`** (<span class="type">integer</span>)  
<span class="simpara"> This BBCode Tag does not accept content (it voids
it automatically). </span>

**`BBCODE_FLAGS_SMILEYS_ON`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This BBCode Tag accepts smileys. </span>

**`BBCODE_FLAGS_SMILEYS_OFF`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This BBCode Tag does not accept smileys. </span>

**`BBCODE_FLAGS_ONE_OPEN_PER_LEVEL`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This BBCode Tag automatically closes if another
tag of the same type is found at the same nesting level. </span>

**`BBCODE_FLAGS_REMOVE_IF_EMPTY`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This BBCode Tag is automatically removed if
content is empty it allows to produce lighter HTML. </span>

**`BBCODE_FLAGS_DENY_REOPEN_CHILD`** (<span class="type">integer</span>) - since 0.10.3  
<span class="simpara"> This BBCode Tag does not allow unclosed children
to reopen when automatically closed. </span>

**`BBCODE_ARG_DOUBLE_QUOTE`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option allowing argument quoting
with double quotes (*"*) </span>

**`BBCODE_ARG_SINGLE_QUOTE`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option allowing argument quoting
with single quotes (*'*) </span>

**`BBCODE_ARG_HTML_QUOTE`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option allowing argument quoting
with HTML version of double quotes (*&quot;*) </span>

**`BBCODE_ARG_QUOTE_ESCAPING`** (<span class="type">integer</span>) - since 1.0.2  
<span class="simpara"> This is a parser option allowing argument quotes
to be escaped this permit the quote delimiter to be found in the string
escaping character is \\ it can escape any quoting character or itself,
if found in front of a non escapable character, it will be dropped.
Default behaviour is not to use escaping. </span>

**`BBCODE_AUTO_CORRECT`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option changing the way errors
are treated. It automatically closes tag in the order they are opened.
And treat tags with only an open tag as if there were a close tag
present. </span>

**`BBCODE_CORRECT_REOPEN_TAGS`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option changing the way errors
are treated. It automatically reopens tag if close tags are not in the
good order. </span>

**`BBCODE_DISABLE_TREE_BUILD`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option disabling the BBCode
parsing it can be useful if only the "smiley" replacement must be used.
</span>

**`BBCODE_DEFAULT_SMILEYS_ON`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option setting smileys to ON if
no flag is given at tag level. </span>

**`BBCODE_DEFAULT_SMILEYS_OFF`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option setting smileys to OFF if
no flag is given at tag level. </span>

**`BBCODE_FORCE_SMILEYS_OFF`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This is a parser option disabling completely the
smileys parsing. </span>

**`BBCODE_SMILEYS_CASE_INSENSITIVE`** (<span class="type">integer</span>) - since 0.10.3  
<span class="simpara"> Use a case insensitive Detection for smileys
instead of a simple binary search. </span>

**`BBCODE_SET_FLAGS_SET`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This permits to SET the complete flag set on a
parser. </span>

**`BBCODE_SET_FLAGS_ADD`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This permits to switch a flag set ON on a parser.
</span>

**`BBCODE_SET_FLAGS_REMOVE`** (<span class="type">integer</span>) - since 0.10.2  
<span class="simpara"> This permits to switch a flag set OFF on a
parser. </span>
