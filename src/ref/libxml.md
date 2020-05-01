libxml\_clear\_errors
=====================

Clear libxml error buffer

### 说明

<span class="type">void</span> <span
class="methodname">libxml\_clear\_errors</span> ( <span
class="methodparam">void</span> )

<span class="function">libxml\_clear\_errors</span> clears the libxml
error buffer.

### 返回值

没有返回值。

### 参见

-   <span class="function">libxml\_get\_errors</span>
-   <span class="function">libxml\_get\_last\_error</span>

libxml\_disable\_entity\_loader
===============================

Disable the ability to load external entities

### 说明

<span class="type">bool</span> <span
class="methodname">libxml\_disable\_entity\_loader</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$disable`<span
class="initializer"> = **`TRUE`**</span></span> \] )

Disable/enable the ability to load external entities.

### 参数

`disable`  
Disable (**`TRUE`**) or enable (**`FALSE`**) libxml extensions (such as
<a href="/book/dom.html" class="xref">DOM</a>,
<a href="/book/xmlwriter.html" class="xref">XMLWriter</a> and
<a href="/book/xmlreader.html" class="xref">XMLReader</a>) to load
external entities.

### 返回值

Returns the previous value.

### 参见

-   <span class="function">libxml\_use\_internal\_errors</span>
-   <a href="/libxml/constants.html" class="link">The <strong><code>LIBXML_NONET</code></strong> constant</a>

libxml\_get\_errors
===================

Retrieve array of errors

### 说明

<span class="type">array</span> <span
class="methodname">libxml\_get\_errors</span> ( <span
class="methodparam">void</span> )

Retrieve array of errors.

### 返回值

Returns an array with <span class="type">LibXMLError</span> objects if
there are any errors in the buffer, or an empty array otherwise.

### 范例

**示例 \#1 A <span class="function">libxml\_get\_errors</span> example**

This example demonstrates how to build a simple libxml error handler.

``` php
<?php

libxml_use_internal_errors(true);

$xmlstr = <<< XML
<?xml version='1.0' standalone='yes'?>
<movies>
 <movie>
  <titles>PHP: Behind the Parser</title>
 </movie>
</movies>
XML;

$doc = simplexml_load_string($xmlstr);
$xml = explode("\n", $xmlstr);

if ($doc === false) {
    $errors = libxml_get_errors();

    foreach ($errors as $error) {
        echo display_xml_error($error, $xml);
    }

    libxml_clear_errors();
}


function display_xml_error($error, $xml)
{
    $return  = $xml[$error->line - 1] . "\n";
    $return .= str_repeat('-', $error->column) . "^\n";

    switch ($error->level) {
        case LIBXML_ERR_WARNING:
            $return .= "Warning $error->code: ";
            break;
         case LIBXML_ERR_ERROR:
            $return .= "Error $error->code: ";
            break;
        case LIBXML_ERR_FATAL:
            $return .= "Fatal Error $error->code: ";
            break;
    }

    $return .= trim($error->message) .
               "\n  Line: $error->line" .
               "\n  Column: $error->column";

    if ($error->file) {
        $return .= "\n  File: $error->file";
    }

    return "$return\n\n--------------------------------------------\n\n";
}

?>
```

以上例程会输出：

      <titles>PHP: Behind the Parser</title>
    ----------------------------------------------^
    Fatal Error 76: Opening and ending tag mismatch: titles line 4 and title
      Line: 4
      Column: 46

    --------------------------------------------

### 参见

-   <span class="function">libxml\_get\_last\_error</span>
-   <span class="function">libxml\_clear\_errors</span>

libxml\_get\_last\_error
========================

Retrieve last error from libxml

### 说明

<span class="type">LibXMLError</span> <span
class="methodname">libxml\_get\_last\_error</span> ( <span
class="methodparam">void</span> )

Retrieve last error from libxml.

### 返回值

Returns a <span class="type">LibXMLError</span> object if there is any
error in the buffer, **`FALSE`** otherwise.

### 参见

-   <span class="function">libxml\_get\_errors</span>
-   <span class="function">libxml\_clear\_errors</span>

libxml\_set\_external\_entity\_loader
=====================================

Changes the default external entity loader

### 说明

<span class="type">bool</span> <span
class="methodname">libxml\_set\_external\_entity\_loader</span> ( <span
class="methodparam"><span class="type">callable</span>
`$resolver_function`</span> )

Changes the default external entity loader.

### 参数

`resolver_function`  
A <span class="type">callable</span> that takes three arguments. Two
strings, a public id and system id, and a context (an array with four
keys) as the third argument. This callback should return a resource, a
string from which a resource can be opened, or **`NULL`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="function">libxml\_set\_external\_entity\_loader</span> example**

``` php
<?php
$xml = <<<XML
<!DOCTYPE foo PUBLIC "-//FOO/BAR" "http://example.com/foobar">
<foo>bar</foo>
XML;

$dtd = <<<DTD
<!ELEMENT foo (#PCDATA)>
DTD;

libxml_set_external_entity_loader(
    function ($public, $system, $context) use($dtd) {
        var_dump($public);
        var_dump($system);
        var_dump($context);
        $f = fopen("php://temp", "r+");
        fwrite($f, $dtd);
        rewind($f);
        return $f;
    }
);

$dd = new DOMDocument;
$r  = $dd->loadXML($xml);

var_dump($dd->validate());
?>
```

以上例程会输出：

    string(10) "-//FOO/BAR"
    string(25) "http://example.com/foobar"
    array(4) {
        ["directory"]    => NULL
        ["intSubName"]   => NULL
        ["extSubURI"]    => NULL
        ["extSubSystem"] => NULL
    }
    bool(true)

### 参见

-   <span class="function">libxml\_disable\_entity\_loader</span>

libxml\_set\_streams\_context
=============================

Set the streams context for the next libxml document load or write

### 说明

<span class="type">void</span> <span
class="methodname">libxml\_set\_streams\_context</span> ( <span
class="methodparam"><span class="type">resource</span>
`$streams_context`</span> )

Sets the streams context for the next libxml document load or write.

### 参数

`streams_context`  
The stream context resource (created with <span
class="function">stream\_context\_create</span>)

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">libxml\_set\_streams\_context</span>
example**

``` php
<?php

$opts = array(
    'http' => array(
        'user_agent' => 'PHP libxml agent',
    )
);

$context = stream_context_create($opts);
libxml_set_streams_context($context);

// request a file through HTTP
$doc = DOMDocument::load('http://www.example.com/file.xml');

?>
```

### 参见

-   <span class="function">stream\_context\_create</span>

libxml\_use\_internal\_errors
=============================

Disable libxml errors and allow user to fetch error information as
needed

### 说明

<span class="type">bool</span> <span
class="methodname">libxml\_use\_internal\_errors</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$use_errors`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="function">libxml\_use\_internal\_errors</span> allows you
to disable standard libxml errors and enable user error handling.

### 参数

`use_errors`  
Enable (**`TRUE`**) user error handling or disable (**`FALSE`**) user
error handling. Disabling will also clear any existing libxml errors.

### 返回值

This function returns the previous value of `use_errors`.

### 范例

**示例 \#1 A <span class="function">libxml\_use\_internal\_errors</span>
example**

This example demonstrates the basic usage of libxml errors and the value
returned by this function.

``` php
<?php

// enable user error handling
var_dump(libxml_use_internal_errors(true));

// load the document
$doc = new DOMDocument;

if (!$doc->load('file.xml')) {
    foreach (libxml_get_errors() as $error) {
        // handle errors here
    }

    libxml_clear_errors();
}

?>
```

以上例程会输出：

    bool(false)

### 参见

-   <span class="function">libxml\_clear\_errors</span>
-   <span class="function">libxml\_get\_errors</span>

**目录**

-   [libxml\_clear\_errors](/ref/libxml.html#libxml_clear_errors) —
    Clear libxml error buffer
-   [libxml\_disable\_entity\_loader](/ref/libxml.html#libxml_disable_entity_loader)
    — Disable the ability to load external entities
-   [libxml\_get\_errors](/ref/libxml.html#libxml_get_errors) — Retrieve
    array of errors
-   [libxml\_get\_last\_error](/ref/libxml.html#libxml_get_last_error) —
    Retrieve last error from libxml
-   [libxml\_set\_external\_entity\_loader](/ref/libxml.html#libxml_set_external_entity_loader)
    — Changes the default external entity loader
-   [libxml\_set\_streams\_context](/ref/libxml.html#libxml_set_streams_context)
    — Set the streams context for the next libxml document load or write
-   [libxml\_use\_internal\_errors](/ref/libxml.html#libxml_use_internal_errors)
    — Disable libxml errors and allow user to fetch error information as
    needed
