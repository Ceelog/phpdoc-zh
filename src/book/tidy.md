Tidy
====

**目录**

-   [简介](/intro/tidy.html)
-   [安装／配置](/tidy/setup.html)
    -   [需求](/tidy/setup.html#需求)
    -   [安装](/tidy/setup.html#安装)
    -   [运行时配置](/tidy/setup.html#运行时配置)
    -   [资源类型](/tidy/setup.html#资源类型)
-   [预定义常量](/tidy/constants.html)
-   [范例](/tidy/examples.html)
    -   [Tidy example](/tidy/examples.html#Tidy%20example)
-   [tidy](/class/tidy.html) — The tidy class
    -   [tidy::body](/class/tidy.html#tidy::body) — Returns a tidyNode
        object starting from the \<body\> tag of the tidy parse tree
    -   [tidy::cleanRepair](/class/tidy.html#tidy::cleanRepair) —
        Execute configured cleanup and repair operations on parsed
        markup
    -   [tidy::\_\_construct](/class/tidy.html#tidy::__construct) —
        Constructs a new tidy object
    -   [tidy::diagnose](/class/tidy.html#tidy::diagnose) — Run
        configured diagnostics on parsed and repaired markup
    -   [tidy::$errorBuffer](/class/tidy.html#tidy::$errorBuffer) —
        Return warnings and errors which occurred parsing the specified
        document
    -   [tidy::getConfig](/class/tidy.html#tidy::getConfig) — Get
        current Tidy configuration
    -   [tidy::getHtmlVer](/class/tidy.html#tidy::getHtmlVer) — Get the
        Detected HTML version for the specified document
    -   [tidy::getOpt](/class/tidy.html#tidy::getOpt) — Returns the
        value of the specified configuration option for the tidy
        document
    -   [tidy::getOptDoc](/class/tidy.html#tidy::getOptDoc) — Returns
        the documentation for the given option name
    -   [tidy::getRelease](/class/tidy.html#tidy::getRelease) — Get
        release date (version) for Tidy library
    -   [tidy::getStatus](/class/tidy.html#tidy::getStatus) — Get status
        of specified document
    -   [tidy::head](/class/tidy.html#tidy::head) — Returns a tidyNode
        object starting from the \<head\> tag of the tidy parse tree
    -   [tidy::html](/class/tidy.html#tidy::html) — Returns a tidyNode
        object starting from the \<html\> tag of the tidy parse tree
    -   [tidy::isXhtml](/class/tidy.html#tidy::isXhtml) — Indicates if
        the document is a XHTML document
    -   [tidy::isXml](/class/tidy.html#tidy::isXml) — Indicates if the
        document is a generic (non HTML/XHTML) XML document
    -   [tidy::parseFile](/class/tidy.html#tidy::parseFile) — Parse
        markup in file or URI
    -   [tidy::parseString](/class/tidy.html#tidy::parseString) — Parse
        a document stored in a string
    -   [tidy::repairFile](/class/tidy.html#tidy::repairFile) — Repair a
        file and return it as a string
    -   [tidy::repairString](/class/tidy.html#tidy::repairString) —
        Repair a string using an optionally provided configuration file
    -   [tidy::root](/class/tidy.html#tidy::root) — Returns a tidyNode
        object representing the root of the tidy parse tree
-   [tidyNode](/class/tidynode.html) — The tidyNode class
    -   [tidyNode::\_\_construct](/class/tidynode.html#tidyNode::__construct)
        — Private constructor to disallow direct instantiation
    -   [tidyNode::getParent](/class/tidynode.html#tidyNode::getParent)
        — Returns the parent node of the current node
    -   [tidyNode::hasChildren](/class/tidynode.html#tidyNode::hasChildren)
        — Checks if a node has children
    -   [tidyNode::hasSiblings](/class/tidynode.html#tidyNode::hasSiblings)
        — Checks if a node has siblings
    -   [tidyNode::isAsp](/class/tidynode.html#tidyNode::isAsp) — Checks
        if this node is ASP
    -   [tidyNode::isComment](/class/tidynode.html#tidyNode::isComment)
        — Checks if a node represents a comment
    -   [tidyNode::isHtml](/class/tidynode.html#tidyNode::isHtml) —
        Checks if a node is an element node
    -   [tidyNode::isJste](/class/tidynode.html#tidyNode::isJste) —
        Checks if this node is JSTE
    -   [tidyNode::isPhp](/class/tidynode.html#tidyNode::isPhp) — Checks
        if a node is PHP
    -   [tidyNode::isText](/class/tidynode.html#tidyNode::isText) —
        Checks if a node represents text (no markup)
-   [Tidy 函数](/ref/tidy.html)
    -   [ob\_tidyhandler](/ref/tidy.html#ob_tidyhandler) — ob\_start
        callback function to repair the buffer
    -   [tidy\_access\_count](/ref/tidy.html#tidy_access_count) —
        Returns the Number of Tidy accessibility warnings encountered
        for specified document
    -   [tidy\_config\_count](/ref/tidy.html#tidy_config_count) —
        Returns the Number of Tidy configuration errors encountered for
        specified document
    -   [tidy\_error\_count](/ref/tidy.html#tidy_error_count) — Returns
        the Number of Tidy errors encountered for specified document
    -   [tidy\_get\_output](/ref/tidy.html#tidy_get_output) — Return a
        string representing the parsed tidy markup
    -   [tidy\_warning\_count](/ref/tidy.html#tidy_warning_count) —
        Returns the Number of Tidy warnings encountered for specified
        document

简介
----

An HTML node in an HTML file, as detected by tidy.

类摘要
------

**tidy**

<span class="ooclass"> class **tidy** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="type">string</span>`$tidy->errorBuffer`;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">body</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">cleanRepair</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`</span> \]\]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">diagnose</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getConfig</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getHtmlVer</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getOpt</span> ( <span class="methodparam"><span
class="type">string</span> `$option`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getOptDoc</span> ( <span
class="methodparam"><span class="type">string</span> `$optname`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getRelease</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getStatus</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">head</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">html</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isXhtml</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isXml</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">parseFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">parseString</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">repairFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">repairString</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \]\] )

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">root</span> ( <span
class="methodparam">void</span> )

}

tidy::body
==========

tidy\_get\_body
===============

Returns a <span class="classname">tidyNode</span> object starting from
the \<body\> tag of the tidy parse tree

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">tidy::body</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">tidyNode</span> <span
class="methodname">tidy\_get\_body</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Returns a <span class="classname">tidyNode</span> object starting from
the \<body\> tag of the tidy parse tree.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns a <span class="classname">tidyNode</span> object starting from
the \<body\> tag of the tidy parse tree.

### 范例

**示例 \#1 <span class="function">tidy::getBody</span> example**

``` php
<?php
$html = '
<html>
  <head>
    <title>test</title>
  </head>
  <body>
    <p>paragraph</p>
  </body>
</html>';

$tidy = tidy_parse_string($html);

$body = $tidy->Body();
echo $body->value;
?>
```

以上例程会输出：

    <body>
    <p>paragraph</p>
    </body>

### 参见

-   <span class="function">tidy::head</span>
-   <span class="function">tidy::html</span>

tidy::cleanRepair
=================

tidy\_clean\_repair
===================

Execute configured cleanup and repair operations on parsed markup

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidy::cleanRepair</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">tidy\_clean\_repair</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

This function cleans and repairs the given tidy `object`.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">tidy::cleanrepair</span> example**

``` php
<?php
$html = '<p>test</I>';

$tidy = tidy_parse_string($html);
$tidy->cleanRepair();

echo $tidy;
?>
```

以上例程会输出：

    <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
    <html>
    <head>
    <title></title>
    </head>
    <body>
    <p>test</p>
    </body>
    </html>

### 参见

-   <span class="function">tidy::repairFile</span>
-   <span class="function">tidy::repairString</span>

tidy::\_\_construct
===================

Constructs a new <span class="classname">tidy</span> object

### 说明

<span class="modifier">public</span> <span
class="methodname">tidy::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`</span> \]\]\]\] )

Constructs a new <span class="classname">tidy</span> object.

### 参数

`filename`  
If the `filename` parameter is given, this function will also read that
file and initialize the object with the file, acting like <span
class="function">tidy\_parse\_file</span>.

`config`  
The config `config` can be passed either as an array or as a string. If
a string is passed, it is interpreted as the name of the configuration
file, otherwise, it is interpreted as the options themselves.

For an explanation about each option, visit
<a href="http://api.html-tidy.org/#quick-reference" class="link external">» http://api.html-tidy.org/#quick-reference</a>.

`encoding`  
The `encoding` parameter sets the encoding for input/output documents.
The possible values for encoding are: *ascii*, *latin0*, *latin1*,
*raw*, *utf8*, *iso2022*, *mac*, *win1252*, *ibm858*, *utf16*,
*utf16le*, *utf16be*, *big5*, and *shiftjis*.

`use_include_path`  
Search for the file in the
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>.

### 返回值

Returns the new <span class="classname">tidy</span> instance.

### 范例

**示例 \#1 <span class="function">tidy::\_\_construct</span> example**

``` php
<?php

$html = <<< HTML

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head><title>title</title></head>
<body>
<p>paragraph <bt />
text</p>
</body></html>

HTML;

$tidy = new tidy();
$tidy->ParseString($html);

$tidy->cleanRepair();

if ($tidy->errorBuffer) {
    echo "The following errors were detected:\n";
    echo $tidy->errorBuffer;
}

?>
```

以上例程会输出：

    The following errors were detected:
    line 8 column 14 - Error: <bt> is not recognized!
    line 8 column 14 - Warning: discarding unexpected <bt>

### 参见

-   <span class="function">tidy::parseFile</span>
-   <span class="function">tidy::parseString</span>

tidy::diagnose
==============

tidy\_diagnose
==============

Run configured diagnostics on parsed and repaired markup

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidy::diagnose</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">tidy\_diagnose</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Runs diagnostic tests on the given tidy `object`, adding some more
information about the document in the error buffer.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">tidy::diagnose</span> example**

``` php
<?php

$html = <<< HTML
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

<p>paragraph</p>
HTML;

$tidy = tidy_parse_string($html);
$tidy->cleanRepair();

// note the difference between the two outputs
echo $tidy->errorBuffer . "\n";

$tidy->diagnose();
echo $tidy->errorBuffer;

?>
```

以上例程会输出：

    line 4 column 1 - Warning: <p> isn't allowed in <head> elements
    line 4 column 1 - Warning: inserting missing 'title' element
    line 4 column 1 - Warning: <p> isn't allowed in <head> elements
    line 4 column 1 - Warning: inserting missing 'title' element
    Info: Doctype given is "-//W3C//DTD XHTML 1.0 Strict//EN"
    Info: Document content looks like XHTML 1.0 Strict
    2 warnings, 0 errors were found!

### 参见

-   <span class="function">tidy::errorBuffer</span>

tidy::$errorBuffer
==================

tidy\_get\_error\_buffer
========================

Return warnings and errors which occurred parsing the specified document

### 说明

面向对象风格 (property):

<span class="modifier">public</span> <span
class="type">string</span>`$tidy->errorBuffer`;

过程化风格:

<span class="type">string</span> <span
class="methodname">tidy\_get\_error\_buffer</span> ( <span
class="methodparam"><span class="type">tidy</span> `$tidy`</span> )

Returns warnings and errors which occurred parsing the specified
document.

### 参数

`tidy`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the error buffer as a string.

### 范例

**示例 \#1 <span class="function">tidy\_get\_error\_buffer</span>
example**

``` php
<?php
$html = '<p>paragraph</p>';

$tidy = tidy_parse_string($html);

echo tidy_get_error_buffer($tidy);
/* or in OO: */
echo $tidy->errorBuffer;
?>
```

以上例程会输出：

    line 1 column 1 - Warning: missing <!DOCTYPE> declaration
    line 1 column 1 - Warning: inserting missing 'title' element

### 参见

-   <span class="function">tidy\_access\_count</span>
-   <span class="function">tidy\_error\_count</span>
-   <span class="function">tidy\_warning\_count</span>

tidy::getConfig
===============

tidy\_get\_config
=================

Get current Tidy configuration

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">tidy::getConfig</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">tidy\_get\_config</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Gets the list of the configuration options in use by the given tidy
`object`.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns an array of configuration options.

For an explanation about each option, visit
<a href="http://api.html-tidy.org/#quick-reference" class="link external">» http://api.html-tidy.org/#quick-reference</a>.

### 范例

**示例 \#1 <span class="function">tidy::getConfig</span> example**

``` php
<?php
$html = '<p>test</p>';
$config = array('indent' => TRUE,
                'output-xhtml' => TRUE,
                'wrap' => 200);

$tidy = tidy_parse_string($html, $config);

print_r($tidy->getConfig());
?>
```

以上例程会输出：

    Array
    (
        [indent-spaces] => 2
        [wrap] => 200
        [tab-size] => 8
        [char-encoding] => 1
        [input-encoding] => 3
        [output-encoding] => 1
        [newline] => 1
        [doctype-mode] => 1
        [doctype] =>
        [repeated-attributes] => 1
        [alt-text] =>
        [slide-style] =>
        [error-file] =>
        [output-file] =>
        [write-back] =>
        [markup] => 1
        [show-warnings] => 1
        [quiet] =>
        [indent] => 1
        [hide-endtags] =>
        [input-xml] =>
        [output-xml] => 1
        [output-xhtml] => 1
        [output-html] =>
        [add-xml-decl] =>
        [uppercase-tags] =>
        [uppercase-attributes] =>
        [bare] =>
        [clean] =>
        [logical-emphasis] =>
        [drop-proprietary-attributes] =>
        [drop-font-tags] =>
        [drop-empty-paras] => 1
        [fix-bad-comments] => 1
        [break-before-br] =>
        [split] =>
        [numeric-entities] =>
        [quote-marks] =>
        [quote-nbsp] => 1
        [quote-ampersand] => 1
        [wrap-attributes] =>
        [wrap-script-literals] =>
        [wrap-sections] => 1
        [wrap-asp] => 1
        [wrap-jste] => 1
        [wrap-php] => 1
        [fix-backslash] => 1
        [indent-attributes] =>
        [assume-xml-procins] =>
        [add-xml-space] =>
        [enclose-text] =>
        [enclose-block-text] =>
        [keep-time] =>
        [word-2000] =>
        [tidy-mark] =>
        [gnu-emacs] =>
        [gnu-emacs-file] =>
        [literal-attributes] =>
        [show-body-only] =>
        [fix-uri] => 1
        [lower-literals] => 1
        [hide-comments] =>
        [indent-cdata] =>
        [force-output] => 1
        [show-errors] => 6
        [ascii-chars] => 1
        [join-classes] =>
        [join-styles] => 1
        [escape-cdata] =>
        [language] =>
        [ncr] => 1
        [output-bom] => 2
        [replace-color] =>
        [css-prefix] =>
        [new-inline-tags] =>
        [new-blocklevel-tags] =>
        [new-empty-tags] =>
        [new-pre-tags] =>
        [accessibility-check] => 0
        [vertical-space] =>
        [punctuation-wrap] =>
        [merge-divs] => 1
    )

### 参见

-   <span class="function">tidy\_reset\_config</span>
-   <span class="function">tidy\_save\_config</span>

tidy::getHtmlVer
================

tidy\_get\_html\_ver
====================

Get the Detected HTML version for the specified document

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">tidy::getHtmlVer</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">tidy\_get\_html\_ver</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Returns the detected HTML version for the specified tidy `object`.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the detected HTML version.

**Warning**

This function is not yet implemented in the Tidylib itself, so it always
return *0*.

tidy::getOpt
============

tidy\_getopt
============

Returns the value of the specified configuration option for the tidy
document

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">tidy::getOpt</span> ( <span
class="methodparam"><span class="type">string</span> `$option`</span> )

过程化风格

<span class="type">mixed</span> <span
class="methodname">tidy\_getopt</span> ( <span class="methodparam"><span
class="type">tidy</span> `$object`</span> , <span
class="methodparam"><span class="type">string</span> `$option`</span> )

Returns the value of the specified `option` for the specified tidy
`object`.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

`option`  
You will find a list with each configuration option and their types at:
<a href="http://api.html-tidy.org/#quick-reference" class="link external">» http://api.html-tidy.org/#quick-reference</a>.

### 返回值

Returns the value of the specified `option`. The return type depends on
the type of the specified one.

### 范例

**示例 \#1 <span class="function">tidy\_getopt</span> example**

``` php
<?php

$html ='<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html><head><title>Title</title></head>
<body>

<p><img src="img.png"></p>

</body></html>';

$config = array('accessibility-check' => 3,
                'alt-text' => 'some text');

$tidy = new tidy();
$tidy->parseString($html, $config);


var_dump($tidy->getOpt('accessibility-check')); //integer
var_dump($tidy->getOpt('lower-literals')); //boolean
var_dump($tidy->getOpt('alt-text')); //string

?>
```

以上例程会输出：

    int(3)
    bool(true)
    string(9) "some text"

tidy::getOptDoc
===============

tidy\_get\_opt\_doc
===================

Returns the documentation for the given option name

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">tidy::getOptDoc</span> ( <span
class="methodparam"><span class="type">string</span> `$optname`</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">tidy\_get\_opt\_doc</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> ,
<span class="methodparam"><span class="type">string</span>
`$optname`</span> )

<span class="function">tidy\_get\_opt\_doc</span> returns the
documentation for the given option name.

> **Note**:
>
> You need at least libtidy from 25 April, 2005 for this function be
> available.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

`optname`  
The option name

### 返回值

Returns a string if the option exists and has documentation available,
or **`FALSE`** otherwise.

### 范例

**示例 \#1 Print all options along with their documentation and default
value**

``` php
<?php

$tidy = new tidy;
$config = $tidy->getConfig();

ksort($config);

foreach ($config as $opt => $val) {

    if (!$doc = $tidy->getOptDoc($opt))
        $doc = 'no documentation available!';

    $val = ($tidy->getOpt($opt) === true)  ? 'true'  : $val;
    $val = ($tidy->getOpt($opt) === false) ? 'false' : $val;

    echo "<p><b>$opt</b> (default: '$val')<br />".
         "$doc</p><hr />\n";
}

?>
```

### 参见

-   <span class="function">tidy::getconfig</span>
-   <span class="function">tidy::getopt</span>

tidy::getRelease
================

tidy\_get\_release
==================

Get release date (version) for Tidy library

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">tidy::getRelease</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">string</span> <span
class="methodname">tidy\_get\_release</span> ( <span
class="methodparam">void</span> )

Gets the release date of the Tidy library.

### 返回值

Returns a string with the release date of the Tidy library, which may be
`'unknown'`.

tidy::getStatus
===============

tidy\_get\_status
=================

Get status of specified document

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">tidy::getStatus</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">int</span> <span
class="methodname">tidy\_get\_status</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Returns the status for the specified tidy `object`.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns 0 if no error/warning was raised, 1 for warnings or
accessibility errors, or 2 for errors.

### 范例

**示例 \#1 <span class="function">tidy::getStatus</span> example**

``` php
<?php
$html = '<p>paragraph</i>';
$tidy = new tidy();
$tidy->parseString($html);

$tidy2 = new tidy();
$html2 = '<bogus>test</bogus>';
$tidy2->parseString($html2);

echo $tidy->getStatus(); //1

echo $tidy2->getStatus(); //2
?>
```

tidy::head
==========

tidy\_get\_head
===============

Returns a <span class="classname">tidyNode</span> object starting from
the \<head\> tag of the tidy parse tree

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">tidy::head</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">tidyNode</span> <span
class="methodname">tidy\_get\_head</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Returns a <span class="classname">tidyNode</span> object starting from
the \<head\> tag of the tidy parse tree.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the <span class="classname">tidyNode</span> object.

### 范例

**示例 \#1 <span class="function">tidy::head</span> example**

``` php
<?php
$html = '
<html>
  <head>
    <title>test</title>
  </head>
  <body>
    <p>paragraph</p>
  </body>
</html>';

$tidy = tidy_parse_string($html);

$head = $tidy->head();
echo $head->value;
?>
```

以上例程会输出：

    <head>
    <title>test</title>
    </head>

### 参见

-   <span class="function">tidy::body</span>
-   <span class="function">tidy::html</span>

tidy::html
==========

tidy\_get\_html
===============

Returns a <span class="classname">tidyNode</span> object starting from
the \<html\> tag of the tidy parse tree

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">tidy::html</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">tidyNode</span> <span
class="methodname">tidy\_get\_html</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Returns a <span class="classname">tidyNode</span> object starting from
the \<html\> tag of the tidy parse tree.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the <span class="classname">tidyNode</span> object.

### 范例

**示例 \#1 <span class="function">tidy::html</span> example**

``` php
<?php
$html = '
<html>
  <head>
    <title>test</title>
  </head>
  <body>
    <p>paragraph</p>
  </body>
</html>';

$tidy = tidy_parse_string($html);

$html = $tidy->html();
echo $html->value;
?>
```

以上例程会输出：

    <html>
    <head>
    <title>test</title>
    </head>
    <body>
    <p>paragraph</p>
    </body>
    </html>

### 参见

-   <span class="function">tidy::body</span>
-   <span class="function">tidy::head</span>

tidy::isXhtml
=============

tidy\_is\_xhtml
===============

Indicates if the document is a XHTML document

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidy::isXhtml</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">tidy\_is\_xhtml</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Tells if the document is a XHTML document.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

This function returns **`TRUE`** if the specified tidy `object` is a
XHTML document, or **`FALSE`** otherwise.

**Warning**

This function is not yet implemented in the Tidylib itself, so it always
return **`FALSE`**.

tidy::isXml
===========

tidy\_is\_xml
=============

Indicates if the document is a generic (non HTML/XHTML) XML document

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidy::isXml</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">bool</span> <span
class="methodname">tidy\_is\_xml</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Tells if the document is a generic (non HTML/XHTML) XML document.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

This function returns **`TRUE`** if the specified tidy `object` is a
generic XML document (non HTML/XHTML), or **`FALSE`** otherwise.

**Warning**

This function is not yet implemented in the Tidylib itself, so it always
return **`FALSE`**.

tidy::parseFile
===============

tidy\_parse\_file
=================

Parse markup in file or URI

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidy::parseFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

过程化风格

<span class="type">tidy</span> <span
class="methodname">tidy\_parse\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

Parses the given file.

### 参数

`filename`  
If the `filename` parameter is given, this function will also read that
file and initialize the object with the file, acting like <span
class="function">tidy\_parse\_file</span>.

`config`  
The config `config` can be passed either as an array or as a string. If
a string is passed, it is interpreted as the name of the configuration
file, otherwise, it is interpreted as the options themselves.

For an explanation about each option, see
<a href="http://api.html-tidy.org/#quick-reference" class="link external">» http://api.html-tidy.org/#quick-reference</a>.

`encoding`  
The `encoding` parameter sets the encoding for input/output documents.
The possible values for encoding are: *ascii*, *latin0*, *latin1*,
*raw*, *utf8*, *iso2022*, *mac*, *win1252*, *ibm858*, *utf16*,
*utf16le*, *utf16be*, *big5*, and *shiftjis*.

`use_include_path`  
Search for the file in the
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">tidy::parseFile</span> example**

``` php
<?php
$tidy = new tidy();
$tidy->parseFile('file.html');

$tidy->cleanRepair();

if(!empty($tidy->errorBuffer)) {
    echo "The following errors or warnings occurred:\n";
    echo $tidy->errorBuffer;
}
?>
```

### 参见

-   <span class="function">tidy::parsestring</span>
-   <span class="function">tidy::repairfile</span>
-   <span class="function">tidy::repairstring</span>

tidy::parseString
=================

tidy\_parse\_string
===================

Parse a document stored in a string

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidy::parseString</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \]\] )

过程化风格

<span class="type">tidy</span> <span
class="methodname">tidy\_parse\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \]\] )

Parses a document stored in a string.

### 参数

`input`  
The data to be parsed.

`config`  
The config `config` can be passed either as an array or as a string. If
a string is passed, it is interpreted as the name of the configuration
file, otherwise, it is interpreted as the options themselves.

For an explanation about each option, visit
<a href="http://api.html-tidy.org/#quick-reference" class="link external">» http://api.html-tidy.org/#quick-reference</a>.

`encoding`  
The `encoding` parameter sets the encoding for input/output documents.
The possible values for encoding are: *ascii*, *latin0*, *latin1*,
*raw*, *utf8*, *iso2022*, *mac*, *win1252*, *ibm858*, *utf16*,
*utf16le*, *utf16be*, *big5*, and *shiftjis*.

### 返回值

Returns a new <span class="classname">tidy</span> instance.

### 范例

**示例 \#1 <span class="function">tidy::parseString</span> example**

``` php
<?php
ob_start();
?>

<html>
  <head>
   <title>test</title>
  </head>
  <body>
   <p>error<br>another line</i>
  </body>
</html>

<?php

$buffer = ob_get_clean();
$config = array('indent' => TRUE,
                'output-xhtml' => TRUE,
                'wrap' => 200);

$tidy = tidy_parse_string($buffer, $config, 'UTF8');

$tidy->cleanRepair();
echo $tidy;
?>
```

以上例程会输出：

    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml">
      <head>
        <title>
          test
        </title>
      </head>
      <body>
        <p>
          error<br />
          another line
        </p>
      </body>
    </html>

### 参见

-   <span class="function">tidy::parseFile</span>
-   <span class="function">tidy::repairFile</span>
-   <span class="function">tidy::repairString</span>

tidy::repairFile
================

tidy\_repair\_file
==================

Repair a file and return it as a string

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">tidy::repairFile</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

过程化风格

<span class="type">string</span> <span
class="methodname">tidy\_repair\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

Repairs the given file and returns it as a string.

### 参数

`filename`  
The file to be repaired.

`config`  
The config `config` can be passed either as an array or as a string. If
a string is passed, it is interpreted as the name of the configuration
file, otherwise, it is interpreted as the options themselves.

Check http://tidy.sourceforge.net/docs/quickref.html for an explanation
about each option.

`encoding`  
The `encoding` parameter sets the encoding for input/output documents.
The possible values for encoding are: *ascii*, *latin0*, *latin1*,
*raw*, *utf8*, *iso2022*, *mac*, *win1252*, *ibm858*, *utf16*,
*utf16le*, *utf16be*, *big5*, and *shiftjis*.

`use_include_path`  
Search for the file in the
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>.

### 返回值

Returns the repaired contents as a string.

### 范例

**示例 \#1 <span class="function">tidy::repairFile</span> example**

``` php
<?php
$file = 'file.html';

$tidy = new tidy();
$repaired = $tidy->repairfile($file);
rename($file, $file . '.bak');

file_put_contents($file, $repaired);
?>
```

### 参见

-   <span class="function">tidy::parseFile</span>
-   <span class="function">tidy::parseString</span>
-   <span class="function">tidy::repairString</span>

tidy::repairString
==================

tidy\_repair\_string
====================

Repair a string using an optionally provided configuration file

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">tidy::repairString</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \]\] )

过程化风格

<span class="type">string</span> <span
class="methodname">tidy\_repair\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \]\] )

Repairs the given string.

### 参数

`data`  
The data to be repaired.

`config`  
The config `config` can be passed either as an array or as a string. If
a string is passed, it is interpreted as the name of the configuration
file, otherwise, it is interpreted as the options themselves.

Check
<a href="http://api.html-tidy.org/#quick-reference" class="link external">» http://api.html-tidy.org/#quick-reference</a>
for an explanation about each option.

`encoding`  
The `encoding` parameter sets the encoding for input/output documents.
The possible values for encoding are: *ascii*, *latin0*, *latin1*,
*raw*, *utf8*, *iso2022*, *mac*, *win1252*, *ibm858*, *utf16*,
*utf16le*, *utf16be*, *big5*, and *shiftjis*.

### 返回值

Returns the repaired string.

### 范例

**示例 \#1 <span class="function">tidy::repairString</span> example**

``` php
<?php
ob_start();
?>

<html>
  <head>
    <title>test</title>
  </head>
  <body>
    <p>error</i>
  </body>
</html>

<?php

$buffer = ob_get_clean();
$tidy = new tidy();
$clean = $tidy->repairString($buffer);

echo $clean;
?>
```

以上例程会输出：

    <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
    <html>
    <head>
    <title>test</title>
    </head>
    <body>
    <p>error</p>
    </body>
    </html>

### 参见

-   <span class="function">tidy::parseFile</span>
-   <span class="function">tidy::parseString</span>
-   <span class="function">tidy::repairFile</span>

tidy::root
==========

tidy\_get\_root
===============

Returns a <span class="classname">tidyNode</span> object representing
the root of the tidy parse tree

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">tidy::root</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">tidyNode</span> <span
class="methodname">tidy\_get\_root</span> ( <span
class="methodparam"><span class="type">tidy</span> `$object`</span> )

Returns a <span class="classname">tidyNode</span> object representing
the root of the tidy parse tree.

### 参数

`object`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the <span class="classname">tidyNode</span> object.

### 范例

**示例 \#1 <span class="function">tidy::root</span> example**

``` php
<?php

$html = <<< HTML
<html><body>

<p>paragraph</p>
<br/>

</body></html>
HTML;

$tidy = tidy_parse_string($html);
dump_nodes($tidy->root(), 1);


function dump_nodes($node, $indent) {

    if($node->hasChildren()) {
        foreach($node->child as $child) {
            echo str_repeat('.', $indent*2) . ($child->name ? $child->name : '"'.$child->value.'"'). "\n";

            dump_nodes($child, $indent+1);
        }
    }
}
?>
```

以上例程会输出：

    ..html
    ....head
    ......title
    ....body
    ......p
    ........"paragraph"
    ......br

简介
----

An HTML node in an HTML file, as detected by tidy.

类摘要
------

<span class="modifier">final</span> **tidyNode**

<span class="ooclass"> class **tidyNode** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span
class="type">string</span>`$value`;

<span class="modifier">public</span> <span
class="type">string</span>`$name`;

<span class="modifier">public</span> <span
class="type">int</span>`$type`;

<span class="modifier">public</span> <span
class="type">int</span>`$line`;

<span class="modifier">public</span> <span
class="type">int</span>`$column`;

<span class="modifier">public</span> <span
class="type">bool</span>`$proprietary`;

<span class="modifier">public</span> <span class="type">int</span>`$id`;

<span class="modifier">public</span> <span
class="type">array</span>`$attribute`;

<span class="modifier">public</span> <span
class="type">array</span>`$child`;

/\* 方法 \*/

<span class="modifier">private</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">getParent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasChildren</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasSiblings</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isAsp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isComment</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isHtml</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isJste</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isPhp</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isText</span> ( <span
class="methodparam">void</span> )

}

属性
----

`value`  
The HTML representation of the node, including the surrounding tags.

`name`  
The name of the HTML node

`type`  
The type of the node (one of the
<a href="/tidy/constants.html#tidy%20nodetype%20constants" class="link">nodetype constants</a>,
e.g. **`TIDY_NODETYPE_PHP`**)

`line`  
The line number at which the tags is located in the file

`column`  
The column number at which the tags is located in the file

`proprietary`  
Indicates if the node is a proprietary tag

`id`  
The ID of the node (one of the
<a href="/tidy/constants.html#tidy%20tag%20constants" class="link">tag constants</a>,
e.g. **`TIDY_TAG_FRAME`**)

`attribute`  
An array of string, representing the attributes names (as keys) of the
current node.

`child`  
An array of <span class="classname">tidyNode</span>, representing the
children of the current node.

| 版本  | 说明                                          |
|-------|-----------------------------------------------|
| 5.1.0 | `line`, `column` and `proprietary` were added |

tidyNode::\_\_construct
=======================

Private constructor to disallow direct instantiation

### 说明

<span class="modifier">private</span> <span
class="methodname">tidyNode::\_\_construct</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

tidyNode::getParent
===================

Returns the parent node of the current node

### 说明

<span class="modifier">public</span> <span class="type">tidyNode</span>
<span class="methodname">tidyNode::getParent</span> ( <span
class="methodparam">void</span> )

Returns the parent node of the current node.

### 范例

**示例 \#1 <span class="function">tidyNode::hasChildren</span> example**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
 </head>
 <body>
 Hello World
 </body>
</html>

HTML;


$tidy = tidy_parse_string($html);
$num = 0;

$node = $tidy->html()->child[0]->child[0];

var_dump($node->getparent()->name);
?>
```

以上例程会输出：

    string(4) "head"

### 返回值

Returns a <span class="type">tidyNode</span> if the node has a parent,
or **`NULL`** otherwise.

tidyNode::hasChildren
=====================

Checks if a node has children

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::hasChildren</span> ( <span
class="methodparam">void</span> )

Tells if the node has children.

### 返回值

Returns **`TRUE`** if the node has children, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">tidyNode::hasChildren</span> example**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

// the head tag
var_dump($tidy->html()->child[0]->hasChildren());

// the php inside the head tag
var_dump($tidy->html()->child[0]->child[0]->hasChildren());

?>
```

以上例程会输出：

    bool(true)
    bool(false)

tidyNode::hasSiblings
=====================

Checks if a node has siblings

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::hasSiblings</span> ( <span
class="methodparam">void</span> )

Tells if the node has siblings.

### 返回值

Returns **`TRUE`** if the node has siblings, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">tidyNode::hasSiblings</span> example**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

// the html tag
var_dump($tidy->html()->hasSiblings());

// the head tag
var_dump($tidy->html()->child[0]->hasSiblings());

?>
```

以上例程会输出：

    bool(false)
    bool(true)

tidyNode::isAsp
===============

Checks if this node is ASP

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::isAsp</span> ( <span
class="methodparam">void</span> )

Tells whether the current node is ASP.

### 返回值

Returns **`TRUE`** if the node is ASP, **`FALSE`** otherwise.

### 范例

**示例 \#1 Extract ASP code from a mixed HTML document**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // check if the current node is of requested type
    if($node->isAsp()) {
        echo "\n\n# asp node #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // check if the current node has childrens
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

以上例程会输出：

    # asp node #1
    <%
      /* ASP code */
      response.write("Hello World!")
    %>

tidyNode::isComment
===================

Checks if a node represents a comment

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::isComment</span> ( <span
class="methodparam">void</span> )

Tells if the node is a comment.

### 返回值

Returns **`TRUE`** if the node is a comment, **`FALSE`** otherwise.

### 范例

**示例 \#1 Extract comments from a mixed HTML document**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // check if the current node is of requested type
    if($node->isComment()) {
        echo "\n\n# comment node #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // check if the current node has childrens
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

以上例程会输出：

    # comment node #1
    <!-- Comments -->

tidyNode::isHtml
================

Checks if a node is an element node

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::isHtml</span> ( <span
class="methodparam">void</span> )

Tells if the node is an element node, but not the root node of the
document.

### 返回值

Returns **`TRUE`** if the node is an element node, but not the root node
of the document, **`FALSE`** otherwise.

### 更新日志

| 版本           | 说明                                                                                                                      |
|----------------|---------------------------------------------------------------------------------------------------------------------------|
| 7.3.24, 7.4.12 | This function has been fixed to have reasonable behavior. Previously, almost any node was reported as being an HTML node. |

### 范例

**示例 \#1 Extract HTML code from a mixed HTML document**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {
    // check if the current node is of requested type
    if($node->isHtml()) {
        echo "\n\n# html node #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // check if the current node has childrens
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

以上例程会输出：

    # html node #1
    <html>
    <head>
    <?php echo '<title>title</title>'; ?><#
      /* JSTE code */
      alert('Hello World');
    #>
    <title></title>
    </head>
    <body>
    <?php
      // PHP code
      echo 'hello world!';
    ?><%
      /* ASP code */
      response.write("Hello World!")
    %><!-- Comments -->
    Hello WorldOutside HTML
    </body>
    </html>

    # html node #2
    <head>
    <?php echo '<title>title</title>'; ?><#
      /* JSTE code */
      alert('Hello World');
    #>
    <title></title>
    </head>


    # html node #3
    <title></title>


    # html node #4
    <body>
    <?php
      // PHP code
      echo 'hello world!';
    ?><%
      /* ASP code */
      response.write("Hello World!")
    %><!-- Comments -->
    Hello WorldOutside HTML
    </body>

tidyNode::isJste
================

Checks if this node is JSTE

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::isJste</span> ( <span
class="methodparam">void</span> )

Tells if the node is JSTE.

### 返回值

Returns **`TRUE`** if the node is JSTE, **`FALSE`** otherwise.

### 范例

**示例 \#1 Extract JSTE code from a mixed HTML document**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // check if the current node is of requested type
    if($node->isJste()) {
        echo "\n\n# jste node #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // check if the current node has childrens
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

以上例程会输出：

    # jste node #1
    <# 
      /* JSTE code */
      alert('Hello World'); 
    #>

tidyNode::isPhp
===============

Checks if a node is PHP

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::isPhp</span> ( <span
class="methodparam">void</span> )

Tells if the node is PHP.

### 返回值

Returns **`TRUE`** if the current node is PHP code, **`FALSE`**
otherwise.

### 范例

**示例 \#1 Extract PHP code from a mixed HTML document**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // check if the current node is of requested type
    if($node->isPhp()) {
        echo "\n\n# php node #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // check if the current node has childrens
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

以上例程会输出：

    # php node #1
    <?php echo '<title>title</title>'; ?>

    # php node #2
    <?php
      // PHP code
      echo 'hello world!';
    ?>

tidyNode::isText
================

Checks if a node represents text (no markup)

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">tidyNode::isText</span> ( <span
class="methodparam">void</span> )

Tells if the node represents a text (without any markup).

### 返回值

Returns **`TRUE`** if the node represent a text, **`FALSE`** otherwise.

### 范例

**示例 \#1 Extract text from a mixed HTML document**

``` php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>title</title>'; ?>
<# 
  /* JSTE code */
  alert('Hello World'); 
#>
</head>
<body>

<?php
  // PHP code
  echo 'hello world!';
?>

<%
  /* ASP code */
  response.write("Hello World!")
%>

<!-- Comments -->
Hello World
</body></html>
Outside HTML
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // check if the current node is of requested type
    if($node->isText()) {
        echo "\n\n# text node #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // check if the current node has childrens
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

以上例程会输出：

    # text node #1
    Hello World

    # text node #2
    Outside HTML
