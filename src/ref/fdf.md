fdf\_add\_doc\_javascript
=========================

Adds javascript code to the FDF document

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_add\_doc\_javascript</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$script_name`</span> , <span
class="methodparam"><span class="type">string</span>
`$script_code`</span> )

Adds a script to the FDF, which Acrobat then adds to the doc-level
scripts of a document, once the FDF is imported into it.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`script_name`  
The script name.

`script_code`  
The script code. It is strongly suggested to use *\\r* for linebreaks
within the script code.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Adding JavaScript code to a FDF**

``` php
<?php
$fdf = fdf_create();
fdf_add_doc_javascript($fdf, "PlusOne", "function PlusOne(x)\r{\r  return x+1;\r}\r");
fdf_save($fdf);
?>
```

will create a FDF like this:

    %FDF-1.2
    %âãÏÓ
    1 0 obj
    <<
    /FDF << /JavaScript << /Doc [ (PlusOne)(function PlusOne\(x\)\r{\r  return x+1;\r}\r)] >> >>
    >>
    endobj
    trailer
    <<
    /Root 1 0 R

    >>
    %%EOF

fdf\_add\_template
==================

Adds a template into the FDF document

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_add\_template</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">int</span> `$newpage`</span> , <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$template`</span> , <span class="methodparam"><span
class="type">int</span> `$rename`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

fdf\_close
==========

Close an FDF document

### 说明

<span class="type">void</span> <span
class="methodname">fdf\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$fdf_document`</span> )

Closes the FDF document.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">fdf\_open</span>

fdf\_create
===========

Create a new FDF document

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">fdf\_create</span> ( <span
class="methodparam">void</span> )

Creates a new FDF document.

This function is needed if one would like to populate input fields in a
PDF document with data.

### 返回值

Returns a FDF document handle, or **`FALSE`** on error.

### 范例

**示例 \#1 Populating a PDF document**

``` php
<?php
$outfdf = fdf_create();
fdf_set_value($outfdf, "volume", $volume, 0);

fdf_set_file($outfdf, "http:/testfdf/resultlabel.pdf");
fdf_save($outfdf, "outtest.fdf");
fdf_close($outfdf);
Header("Content-type: application/vnd.fdf");
$fp = fopen("outtest.fdf", "r");
fpassthru($fp);
unlink("outtest.fdf");
?>
```

### 参见

-   <span class="function">fdf\_close</span>
-   <span class="function">fdf\_save</span>
-   <span class="function">fdf\_open</span>

fdf\_enum\_values
=================

Call a user defined function for each document value

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_enum\_values</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">callable</span> `$function`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$userdata`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

fdf\_errno
==========

Return error code for last fdf operation

### 说明

<span class="type">int</span> <span class="methodname">fdf\_errno</span>
( <span class="methodparam">void</span> )

Gets the error code set by the last FDF function call.

A textual description of the error may be obtained using with <span
class="function">fdf\_error</span>.

### 返回值

Returns the error code as an integer, or zero if there was no errors.

### 参见

-   <span class="function">fdf\_error</span>

fdf\_error
==========

Return error description for FDF error code

### 说明

<span class="type">string</span> <span
class="methodname">fdf\_error</span> (\[ <span class="methodparam"><span
class="type">int</span> `$error_code`<span class="initializer"> =
-1</span></span> \] )

Gets a textual description for the FDF error code given in `error_code`.

### 参数

`error_code`  
An error code obtained with <span class="function">fdf\_errno</span>. If
not provided, this function uses the internal error code set by the last
operation.

### 返回值

Returns the error message as a string, or the string *no error* if
nothing went wrong.

### 参见

-   <span class="function">fdf\_errno</span>

fdf\_get\_ap
============

Get the appearance of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_get\_ap</span> ( <span class="methodparam"><span
class="type">resource</span> `$fdf_document`</span> , <span
class="methodparam"><span class="type">string</span> `$field`</span> ,
<span class="methodparam"><span class="type">int</span> `$face`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Gets the appearance of a `field` (i.e. the value of the /AP key) and
stores it in a file.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`field`  

`face`  
The possible values are **`FDFNormalAP`**, **`FDFRolloverAP`** and
**`FDFDownAP`**.

`filename`  
The appearance will be stored in this parameter.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

fdf\_get\_attachment
====================

Extracts uploaded file embedded in the FDF

### 说明

<span class="type">array</span> <span
class="methodname">fdf\_get\_attachment</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">string</span> `$savepath`</span>
)

Extracts a file uploaded by means of the "file selection" field
`fieldname` and stores it under `savepath`.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  

`savepath`  
May be the name of a plain file or an existing directory in which the
file is to be created under its original name. Any existing file under
the same name will be overwritten.

> **Note**:
>
> There seems to be no other way to find out the original filename but
> to store the file using a directory as `savepath` and check for the
> basename it was stored under.

### 返回值

The returned array contains the following fields:

-   <span class="simpara">`path` - path were the file got stored</span>
-   <span class="simpara">`size` - size of the stored file in
    bytes</span>
-   <span class="simpara">`type` - mimetype if given in the FDF</span>

### 范例

**示例 \#1 Storing an uploaded file**

``` php
<?php
  $fdf = fdf_open_string($HTTP_FDF_DATA);
  $data = fdf_get_attachment($fdf, "filename", "/tmpdir");
  echo "The uploaded file is stored in $data[path]";
?>
```

fdf\_get\_encoding
==================

Get the value of the /Encoding key

### 说明

<span class="type">string</span> <span
class="methodname">fdf\_get\_encoding</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> )

Gets the value of the */Encoding* key.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

### 返回值

Returns the encoding as a string. An empty string is returned if the
default *PDFDocEncoding/Unicode* scheme is used.

### 参见

-   <span class="function">fdf\_set\_encoding</span>

fdf\_get\_file
==============

Get the value of the /F key

### 说明

<span class="type">string</span> <span
class="methodname">fdf\_get\_file</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> )

Gets the value of the */F* key.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

### 返回值

Returns the key value, as a string.

### 参见

-   <span class="function">fdf\_set\_file</span>

fdf\_get\_flags
===============

Gets the flags of a field

### 说明

<span class="type">int</span> <span
class="methodname">fdf\_get\_flags</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">int</span> `$whichflags`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

fdf\_get\_opt
=============

Gets a value from the opt array of a field

### 说明

<span class="type">mixed</span> <span
class="methodname">fdf\_get\_opt</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> \[, <span
class="methodparam"><span class="type">int</span> `$element`<span
class="initializer"> = -1</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

fdf\_get\_status
================

Get the value of the /STATUS key

### 说明

<span class="type">string</span> <span
class="methodname">fdf\_get\_status</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> )

Gets the value of the */STATUS* key.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

### 返回值

Returns the key value, as a string.

### 参见

-   <span class="function">fdf\_set\_status</span>

fdf\_get\_value
===============

Get the value of a field

### 说明

<span class="type">mixed</span> <span
class="methodname">fdf\_get\_value</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> \[, <span
class="methodparam"><span class="type">int</span> `$which`<span
class="initializer"> = -1</span></span> \] )

Gets the value for the requested field.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string.

`which`  
Elements of an array field can be retrieved by passing this optional
parameter, starting at zero. For non-array fields, this parameter will
be ignored.

### 返回值

Returns the field value.

### 更新日志

| 版本  | 说明                                                     |
|-------|----------------------------------------------------------|
| 4.3.0 | Support for arrays and the `which` parameter were added. |

### 参见

-   <span class="function">fdf\_set\_value</span>

fdf\_get\_version
=================

Gets version number for FDF API or file

### 说明

<span class="type">string</span> <span
class="methodname">fdf\_get\_version</span> (\[ <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> \] )

Return the FDF version for the given document, or the toolkit API
version number if no parameter is given.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

### 返回值

Returns the version as a string. For the current FDF toolkit 5.0 the API
version number is *5.0* and the document version number is either *1.2*,
*1.3* or *1.4*.

### 参见

-   <span class="function">fdf\_set\_version</span>

fdf\_header
===========

Sets FDF-specific output headers

### 说明

<span class="type">void</span> <span
class="methodname">fdf\_header</span> ( <span
class="methodparam">void</span> )

This is a convenience function to set appropriate HTTP headers for FDF
output. It sets the *Content-type:* to *application/vnd.fdf*.

### 返回值

没有返回值。

fdf\_next\_field\_name
======================

Get the next field name

### 说明

<span class="type">string</span> <span
class="methodname">fdf\_next\_field\_name</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> \[, <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> \] )

Gets the name of the field after the given field. This name can be used
with several functions.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string. If not given, the first field will
be assumed.

### 返回值

Returns the field name as a string.

### 范例

**示例 \#1 Detecting all fieldnames in a FDF**

``` php
<?php
$fdf = fdf_open($HTTP_FDF_DATA);
for ($field = fdf_next_field_name($fdf);
    $field != "";
    $field = fdf_next_field_name($fdf, $field)) {
    echo "field: $field\n";
}
?>
```

### 参见

-   <span class="function">fdf\_get\_value</span>

fdf\_open\_string
=================

Read a FDF document from a string

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">fdf\_open\_string</span> ( <span
class="methodparam"><span class="type">string</span> `$fdf_data`</span>
)

Reads form data from a string.

You can use <span class="function">fdf\_open\_string</span> together
with `$HTTP_FDF_DATA` to process FDF form input from a remote client.

### 参数

`fdf_data`  
The data as returned from a PDF form or created using <span
class="function">fdf\_create</span> and <span
class="function">fdf\_save\_string</span>.

### 返回值

Returns a FDF document handle, or **`FALSE`** on error.

### 范例

**示例 \#1 Accessing the form data**

``` php
<?php
$fdf = fdf_open_string($HTTP_FDF_DATA);
/* ... */
fdf_close($fdf);
?>
```

### 参见

-   <span class="function">fdf\_open</span>
-   <span class="function">fdf\_close</span>
-   <span class="function">fdf\_create</span>
-   <span class="function">fdf\_save\_string</span>

fdf\_open
=========

Open a FDF document

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">fdf\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

Opens a file with form data.

You can also use <span class="function">fdf\_open\_string</span> to
process the results of a PDF form POST request.

### 参数

`filename`  
Path to the FDF file. This file must contain the data as returned from a
PDF form or created using <span class="function">fdf\_create</span> and
<span class="function">fdf\_save</span>.

### 返回值

Returns a FDF document handle, or **`FALSE`** on error.

### 范例

**示例 \#1 Accessing the form data**

``` php
<?php
// Save the FDF data into a temp file
$fdffp = fopen("test.fdf", "w");
fwrite($fdffp, $HTTP_FDF_DATA, strlen($HTTP_FDF_DATA));
fclose($fdffp);

// Open temp file and evaluate data
$fdf = fdf_open("test.fdf");
/* ... */
fdf_close($fdf);
?>
```

### 参见

-   <span class="function">fdf\_open\_string</span>
-   <span class="function">fdf\_close</span>
-   <span class="function">fdf\_create</span>
-   <span class="function">fdf\_save</span>

fdf\_remove\_item
=================

Sets target frame for form

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_remove\_item</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">int</span> `$item`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

fdf\_save\_string
=================

Returns the FDF document as a string

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">fdf\_save\_string</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> )

Returns the FDF document as a string.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

### 返回值

Returns the document as a string, or **`FALSE`** on error.

### 范例

**示例 \#1 Retrieving FDF as a string**

``` php
<?php
$fdf = fdf_create();
fdf_set_value($fdf, "foo", "bar");
$str = fdf_save_string($fdf);
fdf_close($fdf);
echo $str;
?>
```

以上例程会输出：

    %FDF-1.2
    %âãÏÓ
    1 0 obj
    <<
    /FDF << /Fields 2 0 R >>
    >>
    endobj
    2 0 obj
    [
    << /T (foo)/V (bar)>>
    ]
    endobj
    trailer
    <<
    /Root 1 0 R

    >>
    %%EOF

### 参见

-   <span class="function">fdf\_open\_string</span>
-   <span class="function">fdf\_close</span>
-   <span class="function">fdf\_create</span>
-   <span class="function">fdf\_save</span>

fdf\_save
=========

Save a FDF document

### 说明

<span class="type">bool</span> <span class="methodname">fdf\_save</span>
( <span class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \] )

Saves a FDF document.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`filename`  
If provided, the resulting FDF will be written in this parameter.
Otherwise, this function will write the FDF to the default PHP output
stream.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_close</span>
-   <span class="function">fdf\_create</span>
-   <span class="function">fdf\_save\_string</span>

fdf\_set\_ap
============

Set the appearance of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_ap</span> ( <span class="methodparam"><span
class="type">resource</span> `$fdf_document`</span> , <span
class="methodparam"><span class="type">string</span>
`$field_name`</span> , <span class="methodparam"><span
class="type">int</span> `$face`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">int</span> `$page_number`</span>
)

Sets the appearance of a field (i.e. the value of the */AP* key).

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`field_name`  

`face`  
The possible values **`FDFNormalAP`**, **`FDFRolloverAP`** and
**`FDFDownAP`**.

`filename`  

`page_number`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

fdf\_set\_encoding
==================

Sets FDF character encoding

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_encoding</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$encoding`</span> )

Sets the character encoding for the FDF document.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`encoding`  
The encoding name. The following values are supported: "*Shift-JIS*",
"*UHC*", "*GBK*" and "*BigFive*".

An empty string resets the encoding to the default
*PDFDocEncoding/Unicode* scheme.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

fdf\_set\_file
==============

Set PDF document to display FDF data in

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_file</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$url`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$target_frame`</span> \] )

Selects a different PDF document to display the form results in then the
form it originated from.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`url`  
Should be given as an absolute URL.

`target_frame`  
Use this parameter to specify the frame in which the document will be
displayed. You can also set the default value for this parameter using
<span class="function">fdf\_set\_target\_frame</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Passing FDF data to a second form**

``` php
<?php
  /* set content type for Adobe FDF */
  fdf_header();

  /* start new fdf */
  $fdf = fdf_create();

  /* set field "foo" to value "bar" */
  fdf_set_value($fdf, "foo", "bar");

  /* tell client to display FDF data using "fdf_form.pdf" */
  fdf_set_file($fdf, "http://www.example.com/fdf_form.pdf");

  /* output fdf */
  fdf_save($fdf);

  /* clean up */
  fdf_close($fdf);
?>
```

### 参见

-   <span class="function">fdf\_get\_file</span>
-   <span class="function">fdf\_set\_target\_frame</span>

fdf\_set\_flags
===============

Sets a flag of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_flags</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">int</span> `$whichFlags`</span> ,
<span class="methodparam"><span class="type">int</span>
`$newFlags`</span> )

Sets certain flags of the given field.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string.

`whichFlags`  

`newFlags`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_set\_opt</span>

fdf\_set\_javascript\_action
============================

Sets an javascript action of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_javascript\_action</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">int</span> `$trigger`</span> ,
<span class="methodparam"><span class="type">string</span>
`$script`</span> )

Sets a javascript action for the given field.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string.

`trigger`  

`script`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_set\_submit\_form\_action</span>

fdf\_set\_on\_import\_javascript
================================

Adds javascript code to be executed when Acrobat opens the FDF

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_on\_import\_javascript</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$script`</span> , <span
class="methodparam"><span class="type">bool</span>
`$before_data_import`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">fdf\_add\_doc\_javascript</span>
-   <span class="function">fdf\_set\_javascript\_action</span>

fdf\_set\_opt
=============

Sets an option of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_opt</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">int</span> `$element`</span> ,
<span class="methodparam"><span class="type">string</span>
`$str1`</span> , <span class="methodparam"><span
class="type">string</span> `$str2`</span> )

Sets options of the given field.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string.

`element`  

`str1`  

`str2`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_set\_flags</span>

fdf\_set\_status
================

Set the value of the /STATUS key

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_status</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$status`</span> )

Sets the value of the */STATUS* key. When a client receives a FDF with a
status set it will present the value in an alert box.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`status`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_get\_status</span>

fdf\_set\_submit\_form\_action
==============================

Sets a submit form action of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_submit\_form\_action</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">int</span> `$trigger`</span> ,
<span class="methodparam"><span class="type">string</span>
`$script`</span> , <span class="methodparam"><span
class="type">int</span> `$flags`</span> )

Sets a submit form action for the given field.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string.

`trigger`  

`script`  

`flags`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_set\_javascript\_action</span>

fdf\_set\_target\_frame
=======================

Set target frame for form display

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_target\_frame</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$frame_name`</span> )

Sets the target frame to display a result PDF defined with <span
class="function">fdf\_save\_file</span> in.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`frame_name`  
The frame name, as a string.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_save\_file</span>

fdf\_set\_value
===============

Set the value of a field

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_value</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$fieldname`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$isName`</span>
\] )

Sets the `value` for the given field.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`fieldname`  
Name of the FDF field, as a string.

`value`  
This parameter will be stored as a string unless it is an array. In this
case all array elements will be stored as a value array.

`isName`  
> **Note**:
>
> In older versions of the FDF toolkit last parameter determined if the
> field value was to be converted to a PDF Name (= 1) or set to a PDF
> String (= 0).
>
> The value is no longer used in the current toolkit version 5.0. For
> compatibility reasons it is still supported as an optional parameter
> beginning with PHP 4.3, but ignored internally.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                   |
|-------|--------------------------------------------------------|
| 4.3.0 | Support for arrays in the `value` parameter was added. |

### 参见

-   <span class="function">fdf\_get\_value</span>
-   <span class="function">fdf\_remove\_item</span>

fdf\_set\_version
=================

Sets version number for a FDF file

### 说明

<span class="type">bool</span> <span
class="methodname">fdf\_set\_version</span> ( <span
class="methodparam"><span class="type">resource</span>
`$fdf_document`</span> , <span class="methodparam"><span
class="type">string</span> `$version`</span> )

Sets the FDF `version` for the given document.

Some features supported by this extension are only available in newer
FDF versions.

### 参数

`fdf_document`  
The FDF document handle, returned by <span
class="function">fdf\_create</span>, <span
class="function">fdf\_open</span> or <span
class="function">fdf\_open\_string</span>.

`version`  
The version number. For the current FDF toolkit 5.0, this may be either
*1.2*, *1.3* or *1.4*.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">fdf\_get\_version</span>

**目录**

-   [fdf\_add\_doc\_javascript](/ref/fdf.html#fdf_add_doc_javascript) —
    Adds javascript code to the FDF document
-   [fdf\_add\_template](/ref/fdf.html#fdf_add_template) — Adds a
    template into the FDF document
-   [fdf\_close](/ref/fdf.html#fdf_close) — Close an FDF document
-   [fdf\_create](/ref/fdf.html#fdf_create) — Create a new FDF document
-   [fdf\_enum\_values](/ref/fdf.html#fdf_enum_values) — Call a user
    defined function for each document value
-   [fdf\_errno](/ref/fdf.html#fdf_errno) — Return error code for last
    fdf operation
-   [fdf\_error](/ref/fdf.html#fdf_error) — Return error description for
    FDF error code
-   [fdf\_get\_ap](/ref/fdf.html#fdf_get_ap) — Get the appearance of a
    field
-   [fdf\_get\_attachment](/ref/fdf.html#fdf_get_attachment) — Extracts
    uploaded file embedded in the FDF
-   [fdf\_get\_encoding](/ref/fdf.html#fdf_get_encoding) — Get the value
    of the /Encoding key
-   [fdf\_get\_file](/ref/fdf.html#fdf_get_file) — Get the value of the
    /F key
-   [fdf\_get\_flags](/ref/fdf.html#fdf_get_flags) — Gets the flags of a
    field
-   [fdf\_get\_opt](/ref/fdf.html#fdf_get_opt) — Gets a value from the
    opt array of a field
-   [fdf\_get\_status](/ref/fdf.html#fdf_get_status) — Get the value of
    the /STATUS key
-   [fdf\_get\_value](/ref/fdf.html#fdf_get_value) — Get the value of a
    field
-   [fdf\_get\_version](/ref/fdf.html#fdf_get_version) — Gets version
    number for FDF API or file
-   [fdf\_header](/ref/fdf.html#fdf_header) — Sets FDF-specific output
    headers
-   [fdf\_next\_field\_name](/ref/fdf.html#fdf_next_field_name) — Get
    the next field name
-   [fdf\_open\_string](/ref/fdf.html#fdf_open_string) — Read a FDF
    document from a string
-   [fdf\_open](/ref/fdf.html#fdf_open) — Open a FDF document
-   [fdf\_remove\_item](/ref/fdf.html#fdf_remove_item) — Sets target
    frame for form
-   [fdf\_save\_string](/ref/fdf.html#fdf_save_string) — Returns the FDF
    document as a string
-   [fdf\_save](/ref/fdf.html#fdf_save) — Save a FDF document
-   [fdf\_set\_ap](/ref/fdf.html#fdf_set_ap) — Set the appearance of a
    field
-   [fdf\_set\_encoding](/ref/fdf.html#fdf_set_encoding) — Sets FDF
    character encoding
-   [fdf\_set\_file](/ref/fdf.html#fdf_set_file) — Set PDF document to
    display FDF data in
-   [fdf\_set\_flags](/ref/fdf.html#fdf_set_flags) — Sets a flag of a
    field
-   [fdf\_set\_javascript\_action](/ref/fdf.html#fdf_set_javascript_action)
    — Sets an javascript action of a field
-   [fdf\_set\_on\_import\_javascript](/ref/fdf.html#fdf_set_on_import_javascript)
    — Adds javascript code to be executed when Acrobat opens the FDF
-   [fdf\_set\_opt](/ref/fdf.html#fdf_set_opt) — Sets an option of a
    field
-   [fdf\_set\_status](/ref/fdf.html#fdf_set_status) — Set the value of
    the /STATUS key
-   [fdf\_set\_submit\_form\_action](/ref/fdf.html#fdf_set_submit_form_action)
    — Sets a submit form action of a field
-   [fdf\_set\_target\_frame](/ref/fdf.html#fdf_set_target_frame) — Set
    target frame for form display
-   [fdf\_set\_value](/ref/fdf.html#fdf_set_value) — Set the value of a
    field
-   [fdf\_set\_version](/ref/fdf.html#fdf_set_version) — Sets version
    number for a FDF file
