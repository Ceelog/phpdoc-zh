ob\_tidyhandler
===============

ob\_start callback function to repair the buffer

### 说明

<span class="type">string</span> <span
class="methodname">ob\_tidyhandler</span> ( <span
class="methodparam"><span class="type">string</span> `$input`</span> \[,
<span class="methodparam"><span class="type">int</span> `$mode`</span>
\] )

Callback function for <span class="function">ob\_start</span> to repair
the buffer.

### 参数

`input`  
The buffer.

`mode`  
The buffer mode.

### 返回值

Returns the modified buffer.

### 范例

**示例 \#1 <span class="function">ob\_tidyhandler</span> example**

``` php
<?php
ob_start('ob_tidyhandler');

echo '<p>test</i>';
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

-   <span class="function">ob\_start</span>

tidy\_access\_count
===================

Returns the Number of Tidy accessibility warnings encountered for
specified document

### 说明

<span class="type">int</span> <span
class="methodname">tidy\_access\_count</span> ( <span
class="methodparam"><span class="type">tidy</span> `$tidy`</span> )

<span class="function">tidy\_access\_count</span> returns the number of
accessibility warnings found for the specified document.

### 参数

`tidy`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the number of warnings.

### 范例

**示例 \#1 <span class="function">tidy\_access\_count</span> example**

``` php
<?php

$html ='<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html><head><title>Title</title></head>
<body>

<p><img src="img.png"></p>

</body></html>';


// select the accessibility check level: 1, 2 or 3
$config = array('accessibility-check' => 3);

$tidy = new tidy();
$tidy->parseString($html, $config);
$tidy->cleanRepair();

/* Never forget to call this! */
$tidy->diagnose();

echo tidy_access_count($tidy); //5

?>
```

### 注释

> **Note**:
>
> Due to the design of the TidyLib, you must call <span
> class="function">tidy\_diagnose</span> before <span
> class="function">tidy\_access\_count</span> or it will return always
> *0*. You must also need to enable the *accessibility-check* option.

### 参见

-   <span class="function">tidy\_error\_count</span>
-   <span class="function">tidy\_warning\_count</span>

tidy\_config\_count
===================

Returns the Number of Tidy configuration errors encountered for
specified document

### 说明

<span class="type">int</span> <span
class="methodname">tidy\_config\_count</span> ( <span
class="methodparam"><span class="type">tidy</span> `$tidy`</span> )

Returns the number of errors encountered in the configuration of the
specified tidy `tidy`.

### 参数

`tidy`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the number of errors.

### 范例

**示例 \#1 <span class="function">tidy\_config\_count</span> example**

``` php
<?php
$html = '<p>test</I>';

$config = array('doctype' => 'bogus');

$tidy = tidy_parse_string($html, $config);

/* This outputs 1, because 'bogus' isn't a valid doctype */
echo tidy_config_count($tidy);
?>
```

tidy\_error\_count
==================

Returns the Number of Tidy errors encountered for specified document

### 说明

<span class="type">int</span> <span
class="methodname">tidy\_error\_count</span> ( <span
class="methodparam"><span class="type">tidy</span> `$tidy`</span> )

Returns the number of Tidy errors encountered for the specified
document.

### 参数

`tidy`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the number of errors.

### 范例

**示例 \#1 <span class="function">tidy\_error\_count</span> example**

``` php
<?php
$html = '<p>test</i>
<bogustag>bogus</bogustag>';

$tidy = tidy_parse_string($html);

echo tidy_error_count($tidy) . "\n"; //1

echo $tidy->errorBuffer;
?>
```

以上例程会输出：

    1
    line 1 column 1 - Warning: missing <!DOCTYPE> declaration
    line 1 column 8 - Warning: discarding unexpected </i>
    line 2 column 1 - Error: <bogustag> is not recognized!
    line 2 column 1 - Warning: discarding unexpected <bogustag>
    line 2 column 16 - Warning: discarding unexpected </bogustag>
    line 1 column 1 - Warning: inserting missing 'title' element

### 参见

-   <span class="function">tidy\_access\_count</span>
-   <span class="function">tidy\_warning\_count</span>

tidy\_get\_output
=================

Return a string representing the parsed tidy markup

### 说明

<span class="type">string</span> <span
class="methodname">tidy\_get\_output</span> ( <span
class="methodparam"><span class="type">tidy</span> `$tidy`</span> )

Gets a string with the repaired html.

### 参数

`tidy`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the parsed tidy markup.

### 范例

**示例 \#1 <span class="function">tidy\_get\_output</span> example**

``` php
<?php

$html = '<p>paragraph</i>';
$tidy = tidy_parse_string($html);

$tidy->cleanRepair();

echo tidy_get_output($tidy);
?>
```

以上例程会输出：

    <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
    <html>
    <head>
    <title></title>
    </head>
    <body>
    <p>paragraph</p>
    </body>
    </html>

tidy\_warning\_count
====================

Returns the Number of Tidy warnings encountered for specified document

### 说明

<span class="type">int</span> <span
class="methodname">tidy\_warning\_count</span> ( <span
class="methodparam"><span class="type">tidy</span> `$tidy`</span> )

Returns the number of Tidy warnings encountered for the specified
document.

### 参数

`tidy`  
The <span class="classname">Tidy</span> 对象。

### 返回值

Returns the number of warnings.

### 范例

**示例 \#1 <span class="function">tidy\_warning\_count</span> example**

``` php
<?php
$html = '<p>test</i>
<bogustag>bogus</bogustag>';

$tidy = tidy_parse_string($html);

echo tidy_error_count($tidy) . "\n"; //1
echo tidy_warning_count($tidy) . "\n"; //5
?>
```

### 参见

-   <span class="function">tidy\_error\_count</span>
-   <span class="function">tidy\_access\_count</span>

**目录**

-   [ob\_tidyhandler](/ref/tidy.html#ob_tidyhandler) — ob\_start
    callback function to repair the buffer
-   [tidy\_access\_count](/ref/tidy.html#tidy_access_count) — Returns
    the Number of Tidy accessibility warnings encountered for specified
    document
-   [tidy\_config\_count](/ref/tidy.html#tidy_config_count) — Returns
    the Number of Tidy configuration errors encountered for specified
    document
-   [tidy\_error\_count](/ref/tidy.html#tidy_error_count) — Returns the
    Number of Tidy errors encountered for specified document
-   [tidy\_get\_output](/ref/tidy.html#tidy_get_output) — Return a
    string representing the parsed tidy markup
-   [tidy\_warning\_count](/ref/tidy.html#tidy_warning_count) — Returns
    the Number of Tidy warnings encountered for specified document
