Starting with PHP 4.0.5, the PHP extension for PDFlib is officially
supported by PDFlib GmbH. This means that all the functions described in
the PDFlib Reference Manual are supported by PHP 4 with exactly the same
meaning and the same parameters. However, with PDFlib Version 5.0.4 or
higher all parameters have to be specified. For compatibility reasons,
this binding for PDFlib still supports most of the deprecated functions,
but they should be replaced by their new versions. PDFlib GmbH will not
support any problems arising from the use of these deprecated functions.
The documentation in this section indicates old functions as
"Deprecated" and gives the replacement function to be used instead.

PDF\_activate\_item
===================

Activate structure element or other content item

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_activate\_item</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$id`</span> )

Activates a previously created structure element or other content item.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_add\_annotation
====================

Add annotation \[deprecated\]

### 说明

This function is deprecated, use <span
class="function">PDF\_create\_annotation</span> with `type=Text`
instead.

PDF\_add\_bookmark
==================

Add bookmark for current page \[deprecated\]

### 说明

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_bookmark</span> instead.

PDF\_add\_launchlink
====================

Add launch annotation for current page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_launchlink</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$llx`</span> , <span class="methodparam"><span
class="type">float</span> `$lly`</span> , <span
class="methodparam"><span class="type">float</span> `$urx`</span> ,
<span class="methodparam"><span class="type">float</span> `$ury`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Adds a link to a web resource.

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_action</span> with `type=Launch` and <span
class="function">PDF\_create\_annotation</span> with `type=Link`
instead.

PDF\_add\_locallink
===================

Add link annotation for current page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_locallink</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$lowerleftx`</span> , <span class="methodparam"><span
class="type">float</span> `$lowerlefty`</span> , <span
class="methodparam"><span class="type">float</span>
`$upperrightx`</span> , <span class="methodparam"><span
class="type">float</span> `$upperrighty`</span> , <span
class="methodparam"><span class="type">int</span> `$page`</span> , <span
class="methodparam"><span class="type">string</span> `$dest`</span> )

Add a link annotation to a target within the current PDF file.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_action</span> with `type=GoTo` and <span
class="function">PDF\_create\_annotation</span> with `type=Link`
instead.

PDF\_add\_nameddest
===================

Create named destination

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_nameddest</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a named destination on an arbitrary page in the current
document. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_add\_note
==============

Set annotation for current page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_note</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$llx`</span> , <span class="methodparam"><span
class="type">float</span> `$lly`</span> , <span
class="methodparam"><span class="type">float</span> `$urx`</span> ,
<span class="methodparam"><span class="type">float</span> `$ury`</span>
, <span class="methodparam"><span class="type">string</span>
`$contents`</span> , <span class="methodparam"><span
class="type">string</span> `$title`</span> , <span
class="methodparam"><span class="type">string</span> `$icon`</span> ,
<span class="methodparam"><span class="type">int</span> `$open`</span> )

Sets an annotation for the current page. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_annotation</span> with `type=Text`
instead.

PDF\_add\_outline
=================

Add bookmark for current page \[deprecated\]

### 说明

This function is deprecated, use <span
class="function">PDF\_create\_bookmark</span> instead.

PDF\_add\_pdflink
=================

Add file link annotation for current page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_pdflink</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$bottom_left_x`</span> , <span class="methodparam"><span
class="type">float</span> `$bottom_left_y`</span> , <span
class="methodparam"><span class="type">float</span> `$up_right_x`</span>
, <span class="methodparam"><span class="type">float</span>
`$up_right_y`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">int</span> `$page`</span> , <span
class="methodparam"><span class="type">string</span> `$dest`</span> )

Add a file link annotation to a PDF target. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_action</span> with `type=GoToR` and <span
class="function">PDF\_create\_annotation</span> with `type=Link`
instead.

PDF\_add\_table\_cell
=====================

Add a cell to a new or existing table

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_add\_table\_cell</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$table`</span> , <span class="methodparam"><span
class="type">int</span> `$column`</span> , <span
class="methodparam"><span class="type">int</span> `$row`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Adds a cell to a new or existing table.

PDF\_add\_textflow
==================

Create Textflow or add text to existing Textflow

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_add\_textflow</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$textflow`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Creates a Textflow object, or adds text and explicit options to an
existing Textflow.

PDF\_add\_thumbnail
===================

Add thumbnail for current page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_thumbnail</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$image`</span> )

Adds an existing image as thumbnail for the current page. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_add\_weblink
=================

Add weblink for current page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_add\_weblink</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$lowerleftx`</span> , <span class="methodparam"><span
class="type">float</span> `$lowerlefty`</span> , <span
class="methodparam"><span class="type">float</span>
`$upperrightx`</span> , <span class="methodparam"><span
class="type">float</span> `$upperrighty`</span> , <span
class="methodparam"><span class="type">string</span> `$url`</span> )

Adds a weblink annotation to a target `url` on the Web. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_action</span> with `type=URI` and <span
class="function">PDF\_create\_annotation</span> with `type=Link`
instead.

PDF\_arc
========

Draw a counterclockwise circular arc segment

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_arc</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> , <span class="methodparam"><span class="type">float</span>
`$x`</span> , <span class="methodparam"><span class="type">float</span>
`$y`</span> , <span class="methodparam"><span class="type">float</span>
`$r`</span> , <span class="methodparam"><span class="type">float</span>
`$alpha`</span> , <span class="methodparam"><span
class="type">float</span> `$beta`</span> )

Adds a counterclockwise circular arc.

PDF\_arcn
=========

Draw a clockwise circular arc segment

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_arcn</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> , <span class="methodparam"><span class="type">float</span>
`$x`</span> , <span class="methodparam"><span class="type">float</span>
`$y`</span> , <span class="methodparam"><span class="type">float</span>
`$r`</span> , <span class="methodparam"><span class="type">float</span>
`$alpha`</span> , <span class="methodparam"><span
class="type">float</span> `$beta`</span> )

Except for the drawing direction, this function behaves exactly like
<span class="function">PDF\_arc</span>.

PDF\_attach\_file
=================

Add file attachment for current page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_attach\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$llx`</span> , <span class="methodparam"><span
class="type">float</span> `$lly`</span> , <span
class="methodparam"><span class="type">float</span> `$urx`</span> ,
<span class="methodparam"><span class="type">float</span> `$ury`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$description`</span> , <span
class="methodparam"><span class="type">string</span> `$author`</span> ,
<span class="methodparam"><span class="type">string</span>
`$mimetype`</span> , <span class="methodparam"><span
class="type">string</span> `$icon`</span> )

Adds a file attachment annotation. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_create\_annotation</span> with
`type=FileAttachment` instead.

PDF\_begin\_document
====================

Create new PDF file

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_begin\_document</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a new PDF file subject to various options.

PDF\_begin\_font
================

Start a Type 3 font definition

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_begin\_font</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">float</span> `$a`</span> , <span class="methodparam"><span
class="type">float</span> `$b`</span> , <span class="methodparam"><span
class="type">float</span> `$c`</span> , <span class="methodparam"><span
class="type">float</span> `$d`</span> , <span class="methodparam"><span
class="type">float</span> `$e`</span> , <span class="methodparam"><span
class="type">float</span> `$f`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Starts a Type 3 font definition.

PDF\_begin\_glyph
=================

Start glyph definition for Type 3 font

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_begin\_glyph</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$glyphname`</span> , <span class="methodparam"><span
class="type">float</span> `$wx`</span> , <span class="methodparam"><span
class="type">float</span> `$llx`</span> , <span
class="methodparam"><span class="type">float</span> `$lly`</span> ,
<span class="methodparam"><span class="type">float</span> `$urx`</span>
, <span class="methodparam"><span class="type">float</span>
`$ury`</span> )

Starts a glyph definition for a Type 3 font.

PDF\_begin\_item
================

Open structure element or other content item

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_begin\_item</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$tag`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Opens a structure element or other content item with attributes supplied
as options.

PDF\_begin\_layer
=================

Start layer

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_begin\_layer</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$layer`</span> )

Starts a layer for subsequent output on the page. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function requires PDF 1.5.

PDF\_begin\_page\_ext
=====================

Start new page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_begin\_page\_ext</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Adds a new page to the document, and specifies various options. The
parameters `width` and `height` are the dimensions of the new page in
points. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

| name                | size        |
|---------------------|-------------|
| A0                  | 2380 x 3368 |
| A1                  | 1684 x 2380 |
| A2                  | 1190 x 1684 |
| A3                  | 842 x 1190  |
| A4                  | 595 x 842   |
| A5                  | 421 x 595   |
| A6                  | 297 x 421   |
| B5                  | 501 x 709   |
| letter (8.5" x 11") | 612 x 792   |
| legal (8.5" x 14")  | 612 x 1008  |
| ledger (17" x 11")  | 1224 x 792  |
| 11" x 17"           | 792 x 1224  |

PDF\_begin\_page
================

Start new page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_begin\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

Adds a new page to the document. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_begin\_page\_ext</span> instead.

PDF\_begin\_pattern
===================

Start pattern definition

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_begin\_pattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> , <span
class="methodparam"><span class="type">float</span> `$xstep`</span> ,
<span class="methodparam"><span class="type">float</span>
`$ystep`</span> , <span class="methodparam"><span
class="type">int</span> `$painttype`</span> )

Starts a new pattern definition.

PDF\_begin\_template\_ext
=========================

Start template definition

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_begin\_template\_ext</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Starts a new template definition.

PDF\_begin\_template
====================

Start template definition \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_begin\_template</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

Starts a new template definition.

This function is deprecated since PDFlib version 7, use <span
class="function">PDF\_begin\_template\_ext</span> instead.

PDF\_circle
===========

Draw a circle

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_circle</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$r`</span> )

Adds a circle. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_clip
=========

Clip to current path

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_clip</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> )

Uses the current path as clipping path, and terminate the path.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_close\_image
=================

Close image

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_close\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$image`</span>
)

Closes an `image` retrieved with the <span
class="function">PDF\_open\_image</span> function.

PDF\_close\_pdi\_page
=====================

Close the page handle

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_close\_pdi\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$page`</span> )

Closes the page handle, and frees all page-related resources. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_close\_pdi
===============

Close the input PDF document \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_close\_pdi</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$doc`</span> )

Closes all open page handles, and closes the input PDF document.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 7, use <span
class="function">PDF\_close\_pdi\_document</span> instead.

PDF\_close
==========

Close pdf resource \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> )

Closes the generated PDF file, and frees all document-related resources.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_end\_document</span> instead.

PDF\_closepath\_fill\_stroke
============================

Close, fill and stroke current path

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_closepath\_fill\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Closes the path, fills, and strokes it. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_closepath\_stroke
======================

Close and stroke path

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_closepath\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Closes the path, and strokes it. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_closepath
==============

Close current path

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_closepath</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Closes the current path. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_concat
===========

Concatenate a matrix to the CTM

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_concat</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> , <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$d`</span> , <span
class="methodparam"><span class="type">float</span> `$e`</span> , <span
class="methodparam"><span class="type">float</span> `$f`</span> )

Concatenates a matrix to the current transformation matrix (CTM).
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_continue\_text
===================

Output text in next line

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_continue\_text</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

Prints `text` at the next line. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_create\_3dview
===================

Create 3D view

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_create\_3dview</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$username`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a 3D view.

This function requires PDF 1.6.

PDF\_create\_action
===================

Create action for objects or events

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_create\_action</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$type`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates an action which can be applied to various objects and events.

PDF\_create\_annotation
=======================

Create rectangular annotation

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_create\_annotation</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$llx`</span> , <span class="methodparam"><span
class="type">float</span> `$lly`</span> , <span
class="methodparam"><span class="type">float</span> `$urx`</span> ,
<span class="methodparam"><span class="type">float</span> `$ury`</span>
, <span class="methodparam"><span class="type">string</span>
`$type`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a rectangular annotation on the current page.

PDF\_create\_bookmark
=====================

Create bookmark

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_create\_bookmark</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a bookmark subject to various options.

PDF\_create\_field
==================

Create form field

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_create\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$llx`</span> , <span class="methodparam"><span
class="type">float</span> `$lly`</span> , <span
class="methodparam"><span class="type">float</span> `$urx`</span> ,
<span class="methodparam"><span class="type">float</span> `$ury`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Creates a form field on the current page subject to various options.

PDF\_create\_fieldgroup
=======================

Create form field group

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_create\_fieldgroup</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a form field group subject to various options.

PDF\_create\_gstate
===================

Create graphics state object

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_create\_gstate</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Creates a graphics state object subject to various options.

PDF\_create\_pvf
================

Create PDFlib virtual file

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_create\_pvf</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$data`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Creates a named virtual read-only file from data provided in memory.

PDF\_create\_textflow
=====================

Create textflow object

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_create\_textflow</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Preprocesses text for later formatting and creates a textflow object.

PDF\_curveto
============

Draw Bezier curve

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_curveto</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

Draws a Bezier curve from the current point, using 3 more control
points. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_define\_layer
==================

Create layer definition

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_define\_layer</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a new layer definition.

This function requires PDF 1.5.

PDF\_delete\_pvf
================

Delete PDFlib virtual file

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_delete\_pvf</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Deletes a named virtual file and frees its data structures (but not the
contents).

PDF\_delete\_table
==================

Delete table object

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_delete\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$table`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Deletes a table and all associated data structures.

PDF\_delete\_textflow
=====================

Delete textflow object

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_delete\_textflow</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$textflow`</span> )

Deletes a textflow and the associated data structures.

PDF\_delete
===========

Delete PDFlib object

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> )

Deletes a PDFlib object, and frees all internal resources. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_encoding\_set\_char
========================

Add glyph name and/or Unicode value

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_encoding\_set\_char</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> , <span class="methodparam"><span
class="type">int</span> `$slot`</span> , <span class="methodparam"><span
class="type">string</span> `$glyphname`</span> , <span
class="methodparam"><span class="type">int</span> `$uv`</span> )

Adds a glyph name and/or Unicode value to a custom encoding.

PDF\_end\_document
==================

关闭 PDF 文件

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_document</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

使用指定的选项，关闭生成的 PDF 文件。

PDF\_end\_font
==============

Terminate Type 3 font definition

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_font</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
)

Terminates a Type 3 font definition.

PDF\_end\_glyph
===============

Terminate glyph definition for Type 3 font

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_glyph</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
)

Terminates a glyph definition for a Type 3 font.

PDF\_end\_item
==============

Close structure element or other content item

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_item</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$id`</span> )

Closes a structure element or other content item.

PDF\_end\_layer
===============

Deactivate all active layers

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_layer</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
)

Deactivates all active layers. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

This function requires PDF 1.5.

PDF\_end\_page\_ext
===================

Finish page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_page\_ext</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Finishes a page, and applies various options. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_end\_page
==============

Finish page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Finishes the page. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_end\_pattern
=================

Finish pattern

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_pattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Finishes the pattern definition. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_end\_template
==================

Finish template

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_end\_template</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Finishes a template definition. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_endpath
============

End current path

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_endpath</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> )

Ends the current path without filling or stroking it.

PDF\_fill\_imageblock
=====================

Fill image block with variable data

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_fill\_imageblock</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">string</span>
`$blockname`</span> , <span class="methodparam"><span
class="type">int</span> `$image`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Fills an image block with variable data according to its properties.

This function is only available in the PDFlib Personalization Server
(PPS).

PDF\_fill\_pdfblock
===================

Fill PDF block with variable data

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_fill\_pdfblock</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">string</span>
`$blockname`</span> , <span class="methodparam"><span
class="type">int</span> `$contents`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Fills a PDF block with variable data according to its properties.

This function is only available in the PDFlib Personalization Server
(PPS).

PDF\_fill\_stroke
=================

Fill and stroke path

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_fill\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Fills and strokes the current path with the current fill and stroke
color. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_fill\_textblock
====================

Fill text block with variable data

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_fill\_textblock</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">string</span>
`$blockname`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Fills a text block with variable data according to its properties.

This function is only available in the PDFlib Personalization Server
(PPS).

PDF\_fill
=========

Fill current path

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_fill</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> )

Fills the interior of the current path with the current fill color.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_findfont
=============

Prepare font for later use \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_findfont</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$fontname`</span> , <span class="methodparam"><span
class="type">string</span> `$encoding`</span> , <span
class="methodparam"><span class="type">int</span> `$embed`</span> )

Search for a font and prepare it for later use with <span
class="function">PDF\_setfont</span>. The metrics will be loaded, and if
`embed` is nonzero, the font file will be checked, but not yet used.
`encoding` is one of *builtin*, *macroman*, *winansi*, *host*, a
user-defined encoding name or the name of a CMap. Parameter `embed` is
optional before PHP 4.3.5 or with PDFlib less than 5.

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_load\_font</span> instead.

PDF\_fit\_image
===============

Place image or template

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_fit\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$image`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Places an image or template on the page, subject to various options.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_fit\_pdi\_page
===================

Place imported PDF page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_fit\_pdi\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">float</span> `$x`</span>
, <span class="methodparam"><span class="type">float</span> `$y`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Places an imported PDF page on the page, subject to various options.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_fit\_table
===============

Place table on page

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_fit\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$table`</span> , <span class="methodparam"><span
class="type">float</span> `$llx`</span> , <span
class="methodparam"><span class="type">float</span> `$lly`</span> ,
<span class="methodparam"><span class="type">float</span> `$urx`</span>
, <span class="methodparam"><span class="type">float</span>
`$ury`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Places a table on the page fully or partially.

PDF\_fit\_textflow
==================

Format textflow in rectangular area

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_fit\_textflow</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$textflow`</span> , <span class="methodparam"><span
class="type">float</span> `$llx`</span> , <span
class="methodparam"><span class="type">float</span> `$lly`</span> ,
<span class="methodparam"><span class="type">float</span> `$urx`</span>
, <span class="methodparam"><span class="type">float</span>
`$ury`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Formats the next portion of a textflow into a rectangular area.

PDF\_fit\_textline
==================

Place single line of text

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_fit\_textline</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Places a single line of text on the page, subject to various options.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_get\_apiname
=================

Get name of unsuccessfull API function

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_get\_apiname</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
)

Gets the name of the API function which threw the last exception or
failed.

PDF\_get\_buffer
================

Get PDF output buffer

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_get\_buffer</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Fetches the buffer containing the generated PDF data.

PDF\_get\_errmsg
================

Get error text

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_get\_errmsg</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
)

Gets the text of the last thrown exception or the reason for a failed
function call.

PDF\_get\_errnum
================

Get error number

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_get\_errnum</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
)

Gets the number of the last thrown exception or the reason for a failed
function call.

PDF\_get\_font
==============

Get font \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_get\_value</span> with the parameter `font`
instead.

PDF\_get\_fontname
==================

Get font name \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_get\_parameter</span> with the parameter
`fontname` instead.

PDF\_get\_fontsize
==================

Font handling \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_get\_value</span> with the parameter
`fontsize`instead.

PDF\_get\_image\_height
=======================

Get image height \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_get\_value</span> with the parameter `imageheight`
instead.

PDF\_get\_image\_width
======================

Get image width \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_get\_value</span> with the parameter `imagewidth`
instead.

PDF\_get\_majorversion
======================

Get major version number \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_get\_majorversion</span> ( <span
class="methodparam">void</span> )

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_get\_value</span> with the parameter `major`
instead.

PDF\_get\_minorversion
======================

Get minor version number \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_get\_minorversion</span> ( <span
class="methodparam">void</span> )

Returns the minor version number of the PDFlib version.

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_get\_value</span> with the parameter `minor`
instead.

PDF\_get\_parameter
===================

Get string parameter

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_get\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">float</span>
`$modifier`</span> )

Gets the contents of some PDFlib parameter with string type.

PDF\_get\_pdi\_parameter
========================

Get PDI string parameter \[deprecated\]

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_get\_pdi\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">int</span> `$doc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">int</span>
`$reserved`</span> )

Gets the contents of a PDI document parameter with string type.

This function is deprecated since PDFlib version 7, use <span
class="function">PDF\_pcos\_get\_string</span> instead.

PDF\_get\_pdi\_value
====================

Get PDI numerical parameter \[deprecated\]

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_get\_pdi\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">int</span> `$doc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">int</span>
`$reserved`</span> )

Gets the contents of a PDI document parameter with numerical type.

This function is deprecated since PDFlib version 7, use <span
class="function">PDF\_pcos\_get\_number</span> instead.

PDF\_get\_value
===============

Get numerical parameter

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_get\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">float</span>
`$modifier`</span> )

Gets the value of some PDFlib parameter with numerical type.

PDF\_info\_font
===============

Query detailed information about a loaded font

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_info\_font</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$font`</span>
, <span class="methodparam"><span class="type">string</span>
`$keyword`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Queries detailed information about a loaded font.

PDF\_info\_matchbox
===================

Query matchbox information

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_info\_matchbox</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$boxname`</span> , <span class="methodparam"><span
class="type">int</span> `$num`</span> , <span class="methodparam"><span
class="type">string</span> `$keyword`</span> )

Queries information about a matchbox on the current page.

PDF\_info\_table
================

Retrieve table information

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_info\_table</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$table`</span> , <span class="methodparam"><span
class="type">string</span> `$keyword`</span> )

Retrieves table information related to the most recently placed table
instance.

PDF\_info\_textflow
===================

Query textflow state

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_info\_textflow</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$textflow`</span> , <span class="methodparam"><span
class="type">string</span> `$keyword`</span> )

Queries the current state of a textflow.

PDF\_info\_textline
===================

Perform textline formatting and query metrics

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_info\_textline</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">string</span> `$keyword`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Performs textline formatting and queries the resulting metrics.

PDF\_initgraphics
=================

Reset graphic state

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_initgraphics</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> )

Reset all color and graphics state parameters to their defaults.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_lineto
===========

Draw a line

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_lineto</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Draws a line from the current point to another point. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_load\_3ddata
=================

Load 3D model

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_load\_3ddata</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Loads a 3D model from a disk-based or virtual file.

This function requires PDF 1.6.

PDF\_load\_font
===============

Search and prepare font

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_load\_font</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$fontname`</span> , <span class="methodparam"><span
class="type">string</span> `$encoding`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

Searches for a font and prepares it for later use.

PDF\_load\_iccprofile
=====================

Search and prepare ICC profile

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_load\_iccprofile</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$profilename`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Searches for an ICC profile, and prepares it for later use.

PDF\_load\_image
================

打开一个图像文件

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_load\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$imagetype`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">string</span> `$optlist`</span> )

使用指定选项，打开一个基于磁盘的或虚拟的图像文件。

PDF\_makespotcolor
==================

Make spot color

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_makespotcolor</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$spotname`</span> )

Finds a built-in spot color name, or makes a named spot color from the
current fill color. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_moveto
===========

Set current point

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_moveto</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Sets the current point for graphics output. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_new
========

Create PDFlib object

### 说明

<span class="type">resource</span> <span
class="methodname">PDF\_new</span> ( <span
class="methodparam">void</span> )

Creates a new PDFlib object with default settings.

PDF\_open\_ccitt
================

Open raw CCITT image \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_ccitt</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">int</span> `$width`</span> , <span
class="methodparam"><span class="type">int</span> `$height`</span> ,
<span class="methodparam"><span class="type">int</span>
`$BitReverse`</span> , <span class="methodparam"><span
class="type">int</span> `$k`</span> , <span class="methodparam"><span
class="type">int</span> `$Blackls1`</span> )

Opens a raw CCITT image.

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_load\_image</span> instead.

PDF\_open\_file
===============

Create PDF file \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_open\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Creates a new PDF file using the supplied file name. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_begin\_document</span> instead.

PDF\_open\_gif
==============

Open GIF image \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_load\_image</span> instead.

PDF\_open\_image\_file
======================

Read image from file \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_image\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$imagetype`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">string</span>
`$stringparam`</span> , <span class="methodparam"><span
class="type">int</span> `$intparam`</span> )

Opens an image file.

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_load\_image</span> with the colorize, ignoremask,
invert, mask, masked, and page options instead.

PDF\_open\_image
================

Use image data \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$imagetype`</span> , <span class="methodparam"><span
class="type">string</span> `$source`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$length`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> , <span class="methodparam"><span
class="type">int</span> `$height`</span> , <span
class="methodparam"><span class="type">int</span> `$components`</span> ,
<span class="methodparam"><span class="type">int</span> `$bpc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$params`</span> )

Uses image data from a variety of data sources.

This function is deprecated since PDFlib version 5, use virtual files
and <span class="function">PDF\_load\_image</span> instead.

PDF\_open\_jpeg
===============

Open JPEG image \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_load\_image</span> instead.

PDF\_open\_memory\_image
========================

Open image created with PHP's image functions \[not supported\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_memory\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$image`</span> )

This function is not supported by PDFlib GmbH.

PDF\_open\_pdi\_document
========================

Prepare a pdi document

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_pdi\_document</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Open a disk-based or virtual PDF document and prepare it for later use.

PDF\_open\_pdi\_page
====================

Prepare a page

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_pdi\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$doc`</span> ,
<span class="methodparam"><span class="type">int</span>
`$pagenumber`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Prepares a page for later use with <span
class="function">PDF\_fit\_pdi\_page</span>.

PDF\_open\_pdi
==============

Open PDF file \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_open\_pdi</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> , <span
class="methodparam"><span class="type">int</span> `$len`</span> )

Opens a disk-based or virtual PDF document and prepares it for later
use.

This function is deprecated since PDFlib version 7, use <span
class="function">PDF\_open\_pdi\_document</span> instead.

PDF\_open\_tiff
===============

Open TIFF image \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_load\_image</span> instead.

PDF\_pcos\_get\_number
======================

Get value of pCOS path with type number or boolean

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_pcos\_get\_number</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$doc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

Gets the value of a pCOS path with type number or boolean.

PDF\_pcos\_get\_stream
======================

Get contents of pCOS path with type stream, fstream, or string

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_pcos\_get\_stream</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$doc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$optlist`</span> , <span class="methodparam"><span
class="type">string</span> `$path`</span> )

Gets the contents of a pCOS path with type stream, fstream, or string.

PDF\_pcos\_get\_string
======================

Get value of pCOS path with type name, string, or boolean

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_pcos\_get\_string</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$doc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

Gets the value of a pCOS path with type name, string, or boolean.

PDF\_place\_image
=================

Place image on the page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_place\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$image`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$scale`</span> )

Places an image and scales it. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_fit\_image</span> instead.

PDF\_place\_pdi\_page
=====================

Place PDF page \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_place\_pdi\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">float</span> `$x`</span>
, <span class="methodparam"><span class="type">float</span> `$y`</span>
, <span class="methodparam"><span class="type">float</span> `$sx`</span>
, <span class="methodparam"><span class="type">float</span> `$sy`</span>
)

Places a PDF page and scales it. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_fit\_pdi\_page</span> instead.

PDF\_process\_pdi
=================

Process imported PDF document

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_process\_pdi</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span> `$doc`</span>
, <span class="methodparam"><span class="type">int</span> `$page`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Processes certain elements of an imported PDF document.

PDF\_rect
=========

Draw rectangle

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_rect</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> , <span class="methodparam"><span class="type">float</span>
`$x`</span> , <span class="methodparam"><span class="type">float</span>
`$y`</span> , <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

Draws a rectangle. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_restore
============

Restore graphics state

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_restore</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> )

Restores the most recently saved graphics state. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_resume\_page
=================

Resume page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_resume\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Resumes a page to add more content to it.

PDF\_rotate
===========

Rotate coordinate system

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_rotate</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$phi`</span> )

Rotates the coordinate system. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_save
=========

Save graphics state

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_save</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> )

Saves the current graphics state. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_scale
==========

Scale coordinate system

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_scale</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$sx`</span> , <span
class="methodparam"><span class="type">float</span> `$sy`</span> )

Scales the coordinate system. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_set\_border\_color
=======================

Set border color of annotations \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_border\_color</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

Sets the border color for all kinds of annotations. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use the option
`annotcolor` in <span class="function">PDF\_create\_annotation</span>
instead.

PDF\_set\_border\_dash
======================

Set border dash style of annotations \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_border\_dash</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$black`</span> , <span class="methodparam"><span
class="type">float</span> `$white`</span> )

Sets the border dash style for all kinds of annotations. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use the option
`dasharray` in <span class="function">PDF\_create\_annotation</span>
instead.

PDF\_set\_border\_style
=======================

Set border style of annotations \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_border\_style</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$style`</span> , <span class="methodparam"><span
class="type">float</span> `$width`</span> )

Sets the border style for all kinds of annotations. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 6, use the options
`borderstyle` and `linewidth` in <span
class="function">PDF\_create\_annotation</span> instead.

PDF\_set\_char\_spacing
=======================

Set character spacing \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_value</span> with parameter `charspacing`
instead.

PDF\_set\_duration
==================

Set duration between pages \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use the `duration`
option in <span class="function">PDF\_begin\_page\_ext</span> or <span
class="function">PDF\_end\_page\_ext</span> instead.

PDF\_set\_gstate
================

Activate graphics state object

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_gstate</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$gstate`</span> )

Activates a graphics state object.

PDF\_set\_horiz\_scaling
========================

Set horizontal text scaling \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_value</span> with parameter `horizscaling`
instead.

PDF\_set\_info\_author
======================

Fill the author document info field \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_info</span> instead.

PDF\_set\_info\_creator
=======================

Fill the creator document info field \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_info</span> instead.

PDF\_set\_info\_keywords
========================

Fill the keywords document info field \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_info</span> instead.

PDF\_set\_info\_subject
=======================

Fill the subject document info field \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_info</span> instead.

PDF\_set\_info\_title
=====================

Fill the title document info field \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_info</span> instead.

PDF\_set\_info
==============

Fill document info field

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$value`</span> )

Fill document information field `key` with `value`. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_set\_layer\_dependency
===========================

Define relationships among layers

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_layer\_dependency</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$type`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Defines hierarchical and group relationships among layers. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function requires PDF 1.5.

PDF\_set\_leading
=================

Set distance between text lines \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_value</span> with the parameter `leading`
instead.

PDF\_set\_parameter
===================

Set string parameter

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$value`</span> )

Sets some PDFlib parameter with string type. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_set\_text\_matrix
======================

Set text matrix \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_scale</span>, <span
class="function">PDF\_translate</span>, <span
class="function">PDF\_rotate</span>, or <span
class="function">PDF\_skew</span> instead.

PDF\_set\_text\_pos
===================

Set text position

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_text\_pos</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

Sets the position for text output on the page. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_set\_text\_rendering
=========================

Determine text rendering \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_value</span> with the `textrendering`
parameter instead.

PDF\_set\_text\_rise
====================

Set text rise \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_value</span> with the `textrise` parameter
instead.

PDF\_set\_value
===============

Set numerical parameter

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_set\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">float</span>
`$value`</span> )

Sets the value of some PDFlib parameter with numerical type. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_set\_word\_spacing
=======================

Set spacing between words \[deprecated\]

### 说明

This function is deprecated since PDFlib version 3, use <span
class="function">PDF\_set\_value</span> with the `wordspacing` parameter
instead.

PDF\_setcolor
=============

Set fill and stroke color

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setcolor</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$fstype`</span> , <span class="methodparam"><span
class="type">string</span> `$colorspace`</span> , <span
class="methodparam"><span class="type">float</span> `$c1`</span> , <span
class="methodparam"><span class="type">float</span> `$c2`</span> , <span
class="methodparam"><span class="type">float</span> `$c3`</span> , <span
class="methodparam"><span class="type">float</span> `$c4`</span> )

Sets the current color space and color. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_setdash
============

Set simple dash pattern

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setdash</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> , <span
class="methodparam"><span class="type">float</span> `$w`</span> )

Sets the current dash pattern to `b` black and `w` white units.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_setdashpattern
===================

Set dash pattern

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setdashpattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Sets a dash pattern defined by an option list. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_setflat
============

Set flatness

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setflat</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$flatness`</span> )

Sets the flatness parameter. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_setfont
============

Set font

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setfont</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> , <span
class="methodparam"><span class="type">int</span> `$font`</span> , <span
class="methodparam"><span class="type">float</span> `$fontsize`</span> )

Sets the current font in the specified `fontsize`, using a `font` handle
returned by <span class="function">PDF\_load\_font</span>. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_setgray\_fill
==================

Set fill color to gray \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setgray\_fill</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$g`</span> )

Sets the current fill color to a gray value between 0 and 1 inclusive.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 4, use <span
class="function">PDF\_setcolor</span> instead.

PDF\_setgray\_stroke
====================

Set stroke color to gray \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setgray\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$g`</span> )

Sets the current stroke color to a gray value between 0 and 1 inclusive.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 4, use <span
class="function">PDF\_setcolor</span> instead.

PDF\_setgray
============

Set color to gray \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setgray</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> , <span
class="methodparam"><span class="type">float</span> `$g`</span> )

Sets the current fill and stroke color to a gray value between 0 and 1
inclusive. 成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 4, use <span
class="function">PDF\_setcolor</span> instead.

PDF\_setlinecap
===============

Set linecap parameter

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setlinecap</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span>
`$linecap`</span> )

Sets the `linecap` parameter to control the shape at the end of a path
with respect to stroking.

PDF\_setlinejoin
================

Set linejoin parameter

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setlinejoin</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">int</span> `$value`</span>
)

Sets the `linejoin` parameter to specify the shape at the corners of
paths that are stroked. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_setlinewidth
=================

Set line width

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setlinewidth</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> )

Sets the current line width. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_setmatrix
==============

Set current transformation matrix

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setmatrix</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$a`</span> ,
<span class="methodparam"><span class="type">float</span> `$b`</span> ,
<span class="methodparam"><span class="type">float</span> `$c`</span> ,
<span class="methodparam"><span class="type">float</span> `$d`</span> ,
<span class="methodparam"><span class="type">float</span> `$e`</span> ,
<span class="methodparam"><span class="type">float</span> `$f`</span> )

Explicitly sets the current transformation matrix. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_setmiterlimit
==================

Set miter limit

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setmiterlimit</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">float</span>
`$miter`</span> )

Sets the miter limit.成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_setpolydash
================

Set complicated dash pattern \[deprecated\]

### 说明

This function is deprecated since PDFlib version 5, use <span
class="function">PDF\_setdashpattern</span> instead.

PDF\_setrgbcolor\_fill
======================

Set fill rgb color values \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setrgbcolor\_fill</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

Sets the current fill color to the supplied RGB values. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 4, use <span
class="function">PDF\_setcolor</span> instead.

PDF\_setrgbcolor\_stroke
========================

Set stroke rgb color values \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setrgbcolor\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

Sets the current stroke color to the supplied RGB values. 成功时返回
**`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 4, use <span
class="function">PDF\_setcolor</span> instead.

PDF\_setrgbcolor
================

Set fill and stroke rgb color values \[deprecated\]

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_setrgbcolor</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

Sets the current fill and stroke color to the supplied RGB values.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

This function is deprecated since PDFlib version 4, use <span
class="function">PDF\_setcolor</span> instead.

PDF\_shading\_pattern
=====================

Define shading pattern

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_shading\_pattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">int</span>
`$shading`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Defines a shading pattern using a shading object.

This function requires PDF 1.4 or above.

PDF\_shading
============

Define blend

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_shading</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> , <span
class="methodparam"><span class="type">string</span> `$shtype`</span> ,
<span class="methodparam"><span class="type">float</span> `$x0`</span> ,
<span class="methodparam"><span class="type">float</span> `$y0`</span> ,
<span class="methodparam"><span class="type">float</span> `$x1`</span> ,
<span class="methodparam"><span class="type">float</span> `$y1`</span> ,
<span class="methodparam"><span class="type">float</span> `$c1`</span> ,
<span class="methodparam"><span class="type">float</span> `$c2`</span> ,
<span class="methodparam"><span class="type">float</span> `$c3`</span> ,
<span class="methodparam"><span class="type">float</span> `$c4`</span> ,
<span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Defines a blend from the current fill color to another color.

This function requires PDF 1.4 or above.

PDF\_shfill
===========

Fill area with shading

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_shfill</span> ( <span class="methodparam"><span
class="type">resource</span> `$pdfdoc`</span> , <span
class="methodparam"><span class="type">int</span> `$shading`</span> )

Fills an area with a shading, based on a shading object.

This function requires PDF 1.4 or above.

PDF\_show\_boxed
================

Output text in a box \[deprecated\]

### 说明

<span class="type">int</span> <span
class="methodname">PDF\_show\_boxed</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">float</span> `$left`</span> , <span
class="methodparam"><span class="type">float</span> `$top`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> , <span
class="methodparam"><span class="type">string</span> `$mode`</span> ,
<span class="methodparam"><span class="type">string</span>
`$feature`</span> )

This function is deprecated since PDFlib version 6, use <span
class="function">PDF\_fit\_textline</span> for single lines, or the
<span class="function">PDF\_\*\_textflow</span> functions for multi-line
formatting instead.

PDF\_show\_xy
=============

Output text at given position

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_show\_xy</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Prints `text` in the current font. 成功时返回 **`TRUE`**，
或者在失败时返回 **`FALSE`**。

PDF\_show
=========

Output text at current position

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_show</span>
( <span class="methodparam"><span class="type">resource</span>
`$pdfdoc`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

Prints `text` in the current font and size at the current position.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_skew
=========

Skew the coordinate system

### 说明

<span class="type">bool</span> <span class="methodname">PDF\_skew</span>
( <span class="methodparam"><span class="type">resource</span>
`$p`</span> , <span class="methodparam"><span class="type">float</span>
`$alpha`</span> , <span class="methodparam"><span
class="type">float</span> `$beta`</span> )

Skews the coordinate system in x and y direction by `alpha` and `beta`
degrees, respectively. 成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。

PDF\_stringwidth
================

Return width of text

### 说明

<span class="type">float</span> <span
class="methodname">PDF\_stringwidth</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span class="type">int</span>
`$font`</span> , <span class="methodparam"><span
class="type">float</span> `$fontsize`</span> )

Returns the width of `text` in an arbitrary font.

PDF\_stroke
===========

Stroke path

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_stroke</span> ( <span class="methodparam"><span
class="type">resource</span> `$p`</span> )

Strokes the path with the current color and line width, and clear it.
成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

PDF\_suspend\_page
==================

Suspend page

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_suspend\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$optlist`</span> )

Suspends the current page so that it can later be resumed with <span
class="function">PDF\_resume\_page</span>.

PDF\_translate
==============

Set origin of coordinate system

### 说明

<span class="type">bool</span> <span
class="methodname">PDF\_translate</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">float</span> `$tx`</span> ,
<span class="methodparam"><span class="type">float</span> `$ty`</span> )

Translates the origin of the coordinate system.

PDF\_utf16\_to\_utf8
====================

Convert string from UTF-16 to UTF-8

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_utf16\_to\_utf8</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$utf16string`</span> )

Converts a string from UTF-16 format to UTF-8.

PDF\_utf32\_to\_utf16
=====================

Convert string from UTF-32 to UTF-16

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_utf32\_to\_utf16</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$utf32string`</span> , <span class="methodparam"><span
class="type">string</span> `$ordering`</span> )

Converts a string from UTF-32 format to UTF-16.

PDF\_utf8\_to\_utf16
====================

Convert string from UTF-8 to UTF-16

### 说明

<span class="type">string</span> <span
class="methodname">PDF\_utf8\_to\_utf16</span> ( <span
class="methodparam"><span class="type">resource</span> `$pdfdoc`</span>
, <span class="methodparam"><span class="type">string</span>
`$utf8string`</span> , <span class="methodparam"><span
class="type">string</span> `$ordering`</span> )

Converts a string from UTF-8 format to UTF-16.

**目录**

-   [PDF\_activate\_item](/ref/pdf.html#PDF_activate_item) — Activate
    structure element or other content item
-   [PDF\_add\_annotation](/ref/pdf.html#PDF_add_annotation) — Add
    annotation \[deprecated\]
-   [PDF\_add\_bookmark](/ref/pdf.html#PDF_add_bookmark) — Add bookmark
    for current page \[deprecated\]
-   [PDF\_add\_launchlink](/ref/pdf.html#PDF_add_launchlink) — Add
    launch annotation for current page \[deprecated\]
-   [PDF\_add\_locallink](/ref/pdf.html#PDF_add_locallink) — Add link
    annotation for current page \[deprecated\]
-   [PDF\_add\_nameddest](/ref/pdf.html#PDF_add_nameddest) — Create
    named destination
-   [PDF\_add\_note](/ref/pdf.html#PDF_add_note) — Set annotation for
    current page \[deprecated\]
-   [PDF\_add\_outline](/ref/pdf.html#PDF_add_outline) — Add bookmark
    for current page \[deprecated\]
-   [PDF\_add\_pdflink](/ref/pdf.html#PDF_add_pdflink) — Add file link
    annotation for current page \[deprecated\]
-   [PDF\_add\_table\_cell](/ref/pdf.html#PDF_add_table_cell) — Add a
    cell to a new or existing table
-   [PDF\_add\_textflow](/ref/pdf.html#PDF_add_textflow) — Create
    Textflow or add text to existing Textflow
-   [PDF\_add\_thumbnail](/ref/pdf.html#PDF_add_thumbnail) — Add
    thumbnail for current page
-   [PDF\_add\_weblink](/ref/pdf.html#PDF_add_weblink) — Add weblink for
    current page \[deprecated\]
-   [PDF\_arc](/ref/pdf.html#PDF_arc) — Draw a counterclockwise circular
    arc segment
-   [PDF\_arcn](/ref/pdf.html#PDF_arcn) — Draw a clockwise circular arc
    segment
-   [PDF\_attach\_file](/ref/pdf.html#PDF_attach_file) — Add file
    attachment for current page \[deprecated\]
-   [PDF\_begin\_document](/ref/pdf.html#PDF_begin_document) — Create
    new PDF file
-   [PDF\_begin\_font](/ref/pdf.html#PDF_begin_font) — Start a Type 3
    font definition
-   [PDF\_begin\_glyph](/ref/pdf.html#PDF_begin_glyph) — Start glyph
    definition for Type 3 font
-   [PDF\_begin\_item](/ref/pdf.html#PDF_begin_item) — Open structure
    element or other content item
-   [PDF\_begin\_layer](/ref/pdf.html#PDF_begin_layer) — Start layer
-   [PDF\_begin\_page\_ext](/ref/pdf.html#PDF_begin_page_ext) — Start
    new page
-   [PDF\_begin\_page](/ref/pdf.html#PDF_begin_page) — Start new page
    \[deprecated\]
-   [PDF\_begin\_pattern](/ref/pdf.html#PDF_begin_pattern) — Start
    pattern definition
-   [PDF\_begin\_template\_ext](/ref/pdf.html#PDF_begin_template_ext) —
    Start template definition
-   [PDF\_begin\_template](/ref/pdf.html#PDF_begin_template) — Start
    template definition \[deprecated\]
-   [PDF\_circle](/ref/pdf.html#PDF_circle) — Draw a circle
-   [PDF\_clip](/ref/pdf.html#PDF_clip) — Clip to current path
-   [PDF\_close\_image](/ref/pdf.html#PDF_close_image) — Close image
-   [PDF\_close\_pdi\_page](/ref/pdf.html#PDF_close_pdi_page) — Close
    the page handle
-   [PDF\_close\_pdi](/ref/pdf.html#PDF_close_pdi) — Close the input PDF
    document \[deprecated\]
-   [PDF\_close](/ref/pdf.html#PDF_close) — Close pdf resource
    \[deprecated\]
-   [PDF\_closepath\_fill\_stroke](/ref/pdf.html#PDF_closepath_fill_stroke)
    — Close, fill and stroke current path
-   [PDF\_closepath\_stroke](/ref/pdf.html#PDF_closepath_stroke) — Close
    and stroke path
-   [PDF\_closepath](/ref/pdf.html#PDF_closepath) — Close current path
-   [PDF\_concat](/ref/pdf.html#PDF_concat) — Concatenate a matrix to
    the CTM
-   [PDF\_continue\_text](/ref/pdf.html#PDF_continue_text) — Output text
    in next line
-   [PDF\_create\_3dview](/ref/pdf.html#PDF_create_3dview) — Create 3D
    view
-   [PDF\_create\_action](/ref/pdf.html#PDF_create_action) — Create
    action for objects or events
-   [PDF\_create\_annotation](/ref/pdf.html#PDF_create_annotation) —
    Create rectangular annotation
-   [PDF\_create\_bookmark](/ref/pdf.html#PDF_create_bookmark) — Create
    bookmark
-   [PDF\_create\_field](/ref/pdf.html#PDF_create_field) — Create form
    field
-   [PDF\_create\_fieldgroup](/ref/pdf.html#PDF_create_fieldgroup) —
    Create form field group
-   [PDF\_create\_gstate](/ref/pdf.html#PDF_create_gstate) — Create
    graphics state object
-   [PDF\_create\_pvf](/ref/pdf.html#PDF_create_pvf) — Create PDFlib
    virtual file
-   [PDF\_create\_textflow](/ref/pdf.html#PDF_create_textflow) — Create
    textflow object
-   [PDF\_curveto](/ref/pdf.html#PDF_curveto) — Draw Bezier curve
-   [PDF\_define\_layer](/ref/pdf.html#PDF_define_layer) — Create layer
    definition
-   [PDF\_delete\_pvf](/ref/pdf.html#PDF_delete_pvf) — Delete PDFlib
    virtual file
-   [PDF\_delete\_table](/ref/pdf.html#PDF_delete_table) — Delete table
    object
-   [PDF\_delete\_textflow](/ref/pdf.html#PDF_delete_textflow) — Delete
    textflow object
-   [PDF\_delete](/ref/pdf.html#PDF_delete) — Delete PDFlib object
-   [PDF\_encoding\_set\_char](/ref/pdf.html#PDF_encoding_set_char) —
    Add glyph name and/or Unicode value
-   [PDF\_end\_document](/ref/pdf.html#PDF_end_document) — 关闭 PDF 文件
-   [PDF\_end\_font](/ref/pdf.html#PDF_end_font) — Terminate Type 3 font
    definition
-   [PDF\_end\_glyph](/ref/pdf.html#PDF_end_glyph) — Terminate glyph
    definition for Type 3 font
-   [PDF\_end\_item](/ref/pdf.html#PDF_end_item) — Close structure
    element or other content item
-   [PDF\_end\_layer](/ref/pdf.html#PDF_end_layer) — Deactivate all
    active layers
-   [PDF\_end\_page\_ext](/ref/pdf.html#PDF_end_page_ext) — Finish page
-   [PDF\_end\_page](/ref/pdf.html#PDF_end_page) — Finish page
-   [PDF\_end\_pattern](/ref/pdf.html#PDF_end_pattern) — Finish pattern
-   [PDF\_end\_template](/ref/pdf.html#PDF_end_template) — Finish
    template
-   [PDF\_endpath](/ref/pdf.html#PDF_endpath) — End current path
-   [PDF\_fill\_imageblock](/ref/pdf.html#PDF_fill_imageblock) — Fill
    image block with variable data
-   [PDF\_fill\_pdfblock](/ref/pdf.html#PDF_fill_pdfblock) — Fill PDF
    block with variable data
-   [PDF\_fill\_stroke](/ref/pdf.html#PDF_fill_stroke) — Fill and stroke
    path
-   [PDF\_fill\_textblock](/ref/pdf.html#PDF_fill_textblock) — Fill text
    block with variable data
-   [PDF\_fill](/ref/pdf.html#PDF_fill) — Fill current path
-   [PDF\_findfont](/ref/pdf.html#PDF_findfont) — Prepare font for later
    use \[deprecated\]
-   [PDF\_fit\_image](/ref/pdf.html#PDF_fit_image) — Place image or
    template
-   [PDF\_fit\_pdi\_page](/ref/pdf.html#PDF_fit_pdi_page) — Place
    imported PDF page
-   [PDF\_fit\_table](/ref/pdf.html#PDF_fit_table) — Place table on page
-   [PDF\_fit\_textflow](/ref/pdf.html#PDF_fit_textflow) — Format
    textflow in rectangular area
-   [PDF\_fit\_textline](/ref/pdf.html#PDF_fit_textline) — Place single
    line of text
-   [PDF\_get\_apiname](/ref/pdf.html#PDF_get_apiname) — Get name of
    unsuccessfull API function
-   [PDF\_get\_buffer](/ref/pdf.html#PDF_get_buffer) — Get PDF output
    buffer
-   [PDF\_get\_errmsg](/ref/pdf.html#PDF_get_errmsg) — Get error text
-   [PDF\_get\_errnum](/ref/pdf.html#PDF_get_errnum) — Get error number
-   [PDF\_get\_font](/ref/pdf.html#PDF_get_font) — Get font
    \[deprecated\]
-   [PDF\_get\_fontname](/ref/pdf.html#PDF_get_fontname) — Get font name
    \[deprecated\]
-   [PDF\_get\_fontsize](/ref/pdf.html#PDF_get_fontsize) — Font handling
    \[deprecated\]
-   [PDF\_get\_image\_height](/ref/pdf.html#PDF_get_image_height) — Get
    image height \[deprecated\]
-   [PDF\_get\_image\_width](/ref/pdf.html#PDF_get_image_width) — Get
    image width \[deprecated\]
-   [PDF\_get\_majorversion](/ref/pdf.html#PDF_get_majorversion) — Get
    major version number \[deprecated\]
-   [PDF\_get\_minorversion](/ref/pdf.html#PDF_get_minorversion) — Get
    minor version number \[deprecated\]
-   [PDF\_get\_parameter](/ref/pdf.html#PDF_get_parameter) — Get string
    parameter
-   [PDF\_get\_pdi\_parameter](/ref/pdf.html#PDF_get_pdi_parameter) —
    Get PDI string parameter \[deprecated\]
-   [PDF\_get\_pdi\_value](/ref/pdf.html#PDF_get_pdi_value) — Get PDI
    numerical parameter \[deprecated\]
-   [PDF\_get\_value](/ref/pdf.html#PDF_get_value) — Get numerical
    parameter
-   [PDF\_info\_font](/ref/pdf.html#PDF_info_font) — Query detailed
    information about a loaded font
-   [PDF\_info\_matchbox](/ref/pdf.html#PDF_info_matchbox) — Query
    matchbox information
-   [PDF\_info\_table](/ref/pdf.html#PDF_info_table) — Retrieve table
    information
-   [PDF\_info\_textflow](/ref/pdf.html#PDF_info_textflow) — Query
    textflow state
-   [PDF\_info\_textline](/ref/pdf.html#PDF_info_textline) — Perform
    textline formatting and query metrics
-   [PDF\_initgraphics](/ref/pdf.html#PDF_initgraphics) — Reset graphic
    state
-   [PDF\_lineto](/ref/pdf.html#PDF_lineto) — Draw a line
-   [PDF\_load\_3ddata](/ref/pdf.html#PDF_load_3ddata) — Load 3D model
-   [PDF\_load\_font](/ref/pdf.html#PDF_load_font) — Search and prepare
    font
-   [PDF\_load\_iccprofile](/ref/pdf.html#PDF_load_iccprofile) — Search
    and prepare ICC profile
-   [PDF\_load\_image](/ref/pdf.html#PDF_load_image) — 打开一个图像文件
-   [PDF\_makespotcolor](/ref/pdf.html#PDF_makespotcolor) — Make spot
    color
-   [PDF\_moveto](/ref/pdf.html#PDF_moveto) — Set current point
-   [PDF\_new](/ref/pdf.html#PDF_new) — Create PDFlib object
-   [PDF\_open\_ccitt](/ref/pdf.html#PDF_open_ccitt) — Open raw CCITT
    image \[deprecated\]
-   [PDF\_open\_file](/ref/pdf.html#PDF_open_file) — Create PDF file
    \[deprecated\]
-   [PDF\_open\_gif](/ref/pdf.html#PDF_open_gif) — Open GIF image
    \[deprecated\]
-   [PDF\_open\_image\_file](/ref/pdf.html#PDF_open_image_file) — Read
    image from file \[deprecated\]
-   [PDF\_open\_image](/ref/pdf.html#PDF_open_image) — Use image data
    \[deprecated\]
-   [PDF\_open\_jpeg](/ref/pdf.html#PDF_open_jpeg) — Open JPEG image
    \[deprecated\]
-   [PDF\_open\_memory\_image](/ref/pdf.html#PDF_open_memory_image) —
    Open image created with PHP's image functions \[not supported\]
-   [PDF\_open\_pdi\_document](/ref/pdf.html#PDF_open_pdi_document) —
    Prepare a pdi document
-   [PDF\_open\_pdi\_page](/ref/pdf.html#PDF_open_pdi_page) — Prepare a
    page
-   [PDF\_open\_pdi](/ref/pdf.html#PDF_open_pdi) — Open PDF file
    \[deprecated\]
-   [PDF\_open\_tiff](/ref/pdf.html#PDF_open_tiff) — Open TIFF image
    \[deprecated\]
-   [PDF\_pcos\_get\_number](/ref/pdf.html#PDF_pcos_get_number) — Get
    value of pCOS path with type number or boolean
-   [PDF\_pcos\_get\_stream](/ref/pdf.html#PDF_pcos_get_stream) — Get
    contents of pCOS path with type stream, fstream, or string
-   [PDF\_pcos\_get\_string](/ref/pdf.html#PDF_pcos_get_string) — Get
    value of pCOS path with type name, string, or boolean
-   [PDF\_place\_image](/ref/pdf.html#PDF_place_image) — Place image on
    the page \[deprecated\]
-   [PDF\_place\_pdi\_page](/ref/pdf.html#PDF_place_pdi_page) — Place
    PDF page \[deprecated\]
-   [PDF\_process\_pdi](/ref/pdf.html#PDF_process_pdi) — Process
    imported PDF document
-   [PDF\_rect](/ref/pdf.html#PDF_rect) — Draw rectangle
-   [PDF\_restore](/ref/pdf.html#PDF_restore) — Restore graphics state
-   [PDF\_resume\_page](/ref/pdf.html#PDF_resume_page) — Resume page
-   [PDF\_rotate](/ref/pdf.html#PDF_rotate) — Rotate coordinate system
-   [PDF\_save](/ref/pdf.html#PDF_save) — Save graphics state
-   [PDF\_scale](/ref/pdf.html#PDF_scale) — Scale coordinate system
-   [PDF\_set\_border\_color](/ref/pdf.html#PDF_set_border_color) — Set
    border color of annotations \[deprecated\]
-   [PDF\_set\_border\_dash](/ref/pdf.html#PDF_set_border_dash) — Set
    border dash style of annotations \[deprecated\]
-   [PDF\_set\_border\_style](/ref/pdf.html#PDF_set_border_style) — Set
    border style of annotations \[deprecated\]
-   [PDF\_set\_char\_spacing](/ref/pdf.html#PDF_set_char_spacing) — Set
    character spacing \[deprecated\]
-   [PDF\_set\_duration](/ref/pdf.html#PDF_set_duration) — Set duration
    between pages \[deprecated\]
-   [PDF\_set\_gstate](/ref/pdf.html#PDF_set_gstate) — Activate graphics
    state object
-   [PDF\_set\_horiz\_scaling](/ref/pdf.html#PDF_set_horiz_scaling) —
    Set horizontal text scaling \[deprecated\]
-   [PDF\_set\_info\_author](/ref/pdf.html#PDF_set_info_author) — Fill
    the author document info field \[deprecated\]
-   [PDF\_set\_info\_creator](/ref/pdf.html#PDF_set_info_creator) — Fill
    the creator document info field \[deprecated\]
-   [PDF\_set\_info\_keywords](/ref/pdf.html#PDF_set_info_keywords) —
    Fill the keywords document info field \[deprecated\]
-   [PDF\_set\_info\_subject](/ref/pdf.html#PDF_set_info_subject) — Fill
    the subject document info field \[deprecated\]
-   [PDF\_set\_info\_title](/ref/pdf.html#PDF_set_info_title) — Fill the
    title document info field \[deprecated\]
-   [PDF\_set\_info](/ref/pdf.html#PDF_set_info) — Fill document info
    field
-   [PDF\_set\_layer\_dependency](/ref/pdf.html#PDF_set_layer_dependency)
    — Define relationships among layers
-   [PDF\_set\_leading](/ref/pdf.html#PDF_set_leading) — Set distance
    between text lines \[deprecated\]
-   [PDF\_set\_parameter](/ref/pdf.html#PDF_set_parameter) — Set string
    parameter
-   [PDF\_set\_text\_matrix](/ref/pdf.html#PDF_set_text_matrix) — Set
    text matrix \[deprecated\]
-   [PDF\_set\_text\_pos](/ref/pdf.html#PDF_set_text_pos) — Set text
    position
-   [PDF\_set\_text\_rendering](/ref/pdf.html#PDF_set_text_rendering) —
    Determine text rendering \[deprecated\]
-   [PDF\_set\_text\_rise](/ref/pdf.html#PDF_set_text_rise) — Set text
    rise \[deprecated\]
-   [PDF\_set\_value](/ref/pdf.html#PDF_set_value) — Set numerical
    parameter
-   [PDF\_set\_word\_spacing](/ref/pdf.html#PDF_set_word_spacing) — Set
    spacing between words \[deprecated\]
-   [PDF\_setcolor](/ref/pdf.html#PDF_setcolor) — Set fill and stroke
    color
-   [PDF\_setdash](/ref/pdf.html#PDF_setdash) — Set simple dash pattern
-   [PDF\_setdashpattern](/ref/pdf.html#PDF_setdashpattern) — Set dash
    pattern
-   [PDF\_setflat](/ref/pdf.html#PDF_setflat) — Set flatness
-   [PDF\_setfont](/ref/pdf.html#PDF_setfont) — Set font
-   [PDF\_setgray\_fill](/ref/pdf.html#PDF_setgray_fill) — Set fill
    color to gray \[deprecated\]
-   [PDF\_setgray\_stroke](/ref/pdf.html#PDF_setgray_stroke) — Set
    stroke color to gray \[deprecated\]
-   [PDF\_setgray](/ref/pdf.html#PDF_setgray) — Set color to gray
    \[deprecated\]
-   [PDF\_setlinecap](/ref/pdf.html#PDF_setlinecap) — Set linecap
    parameter
-   [PDF\_setlinejoin](/ref/pdf.html#PDF_setlinejoin) — Set linejoin
    parameter
-   [PDF\_setlinewidth](/ref/pdf.html#PDF_setlinewidth) — Set line width
-   [PDF\_setmatrix](/ref/pdf.html#PDF_setmatrix) — Set current
    transformation matrix
-   [PDF\_setmiterlimit](/ref/pdf.html#PDF_setmiterlimit) — Set miter
    limit
-   [PDF\_setpolydash](/ref/pdf.html#PDF_setpolydash) — Set complicated
    dash pattern \[deprecated\]
-   [PDF\_setrgbcolor\_fill](/ref/pdf.html#PDF_setrgbcolor_fill) — Set
    fill rgb color values \[deprecated\]
-   [PDF\_setrgbcolor\_stroke](/ref/pdf.html#PDF_setrgbcolor_stroke) —
    Set stroke rgb color values \[deprecated\]
-   [PDF\_setrgbcolor](/ref/pdf.html#PDF_setrgbcolor) — Set fill and
    stroke rgb color values \[deprecated\]
-   [PDF\_shading\_pattern](/ref/pdf.html#PDF_shading_pattern) — Define
    shading pattern
-   [PDF\_shading](/ref/pdf.html#PDF_shading) — Define blend
-   [PDF\_shfill](/ref/pdf.html#PDF_shfill) — Fill area with shading
-   [PDF\_show\_boxed](/ref/pdf.html#PDF_show_boxed) — Output text in a
    box \[deprecated\]
-   [PDF\_show\_xy](/ref/pdf.html#PDF_show_xy) — Output text at given
    position
-   [PDF\_show](/ref/pdf.html#PDF_show) — Output text at current
    position
-   [PDF\_skew](/ref/pdf.html#PDF_skew) — Skew the coordinate system
-   [PDF\_stringwidth](/ref/pdf.html#PDF_stringwidth) — Return width of
    text
-   [PDF\_stroke](/ref/pdf.html#PDF_stroke) — Stroke path
-   [PDF\_suspend\_page](/ref/pdf.html#PDF_suspend_page) — Suspend page
-   [PDF\_translate](/ref/pdf.html#PDF_translate) — Set origin of
    coordinate system
-   [PDF\_utf16\_to\_utf8](/ref/pdf.html#PDF_utf16_to_utf8) — Convert
    string from UTF-16 to UTF-8
-   [PDF\_utf32\_to\_utf16](/ref/pdf.html#PDF_utf32_to_utf16) — Convert
    string from UTF-32 to UTF-16
-   [PDF\_utf8\_to\_utf16](/ref/pdf.html#PDF_utf8_to_utf16) — Convert
    string from UTF-8 to UTF-16
