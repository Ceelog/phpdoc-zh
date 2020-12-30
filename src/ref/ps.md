Contact Information
-------------------

If you have comments, bugfixes, enhancements for either this extension
or pslib then please drop me a mail
<a href="mailto:steinm@php.net" class="link external">» steinm@php.net</a>.
Any help is very welcome.

ps\_add\_bookmark
=================

Add bookmark to current page

### 说明

<span class="type">int</span> <span
class="methodname">ps\_add\_bookmark</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> \[, <span class="methodparam"><span
class="type">int</span> `$parent`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$open`<span class="initializer"> =
0</span></span> \]\] )

Adds a bookmark for the current page. Bookmarks usually appear in
PDF-Viewers left of the page in a hierarchical tree. Clicking on a
bookmark will jump to the given page.

此说明在文档被打印或显示时不可见，只在文档用 Acrobat Distiller 或
Ghostview 转换成 PDF 时显示。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text used for displaying the bookmark.

`parent`  
A bookmark previously created by this function which is used as the
parent of the new bookmark.

`open`  
If `open` is unequal to zero the bookmark will be shown open by the pdf
viewer.

### 返回值

The returned value is a reference for the bookmark. It is only used if
the bookmark shall be used as a parent. The value is greater zero if the
function succeeds. In case of an error zero will be returned.

### 参见

-   <span class="function">ps\_add\_launchlink</span>
-   <span class="function">ps\_add\_pdflink</span>
-   <span class="function">ps\_add\_weblink</span>

ps\_add\_launchlink
===================

Adds link which launches file

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_add\_launchlink</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$llx`</span>
, <span class="methodparam"><span class="type">float</span>
`$lly`</span> , <span class="methodparam"><span
class="type">float</span> `$urx`</span> , <span
class="methodparam"><span class="type">float</span> `$ury`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Places a hyperlink at the given position pointing to a file program
which is being started when clicked on. The hyperlink's source position
is a rectangle with its lower left corner at (llx, lly) and its upper
right corner at (urx, ury). The rectangle has by default a thin blue
border.

此说明在文档被打印或显示时不可见，只在文档用 Acrobat Distiller 或
Ghostview 转换成 PDF 时显示。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`llx`  
The x-coordinate of the lower left corner.

`lly`  
The y-coordinate of the lower left corner.

`urx`  
The x-coordinate of the upper right corner.

`ury`  
The y-coordinate of the upper right corner.

`filename`  
The path of the program to be started, when the link is clicked on.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_add\_locallink</span>
-   <span class="function">ps\_add\_pdflink</span>
-   <span class="function">ps\_add\_weblink</span>

ps\_add\_locallink
==================

Adds link to a page in the same document

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_add\_locallink</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$llx`</span>
, <span class="methodparam"><span class="type">float</span>
`$lly`</span> , <span class="methodparam"><span
class="type">float</span> `$urx`</span> , <span
class="methodparam"><span class="type">float</span> `$ury`</span> ,
<span class="methodparam"><span class="type">int</span> `$page`</span> ,
<span class="methodparam"><span class="type">string</span>
`$dest`</span> )

Places a hyperlink at the given position pointing to a page in the same
document. Clicking on the link will jump to the given page. The first
page in a document has number 1.

The hyperlink's source position is a rectangle with its lower left
corner at (`llx`, `lly`) and its upper right corner at (`urx`, `ury`).
The rectangle has by default a thin blue border.

此说明在文档被打印或显示时不可见，只在文档用 Acrobat Distiller 或
Ghostview 转换成 PDF 时显示。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`llx`  
The x-coordinate of the lower left corner.

`lly`  
The y-coordinate of the lower left corner.

`urx`  
The x-coordinate of the upper right corner.

`ury`  
The y-coordinate of the upper right corner.

`page`  
The number of the page displayed when clicking on the link.

`dest`  
The parameter `dest` determines how the document is being viewed. It can
be *fitpage*, *fitwidth*, *fitheight*, or *fitbbox*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_add\_launchlink</span>
-   <span class="function">ps\_add\_pdflink</span>
-   <span class="function">ps\_add\_weblink</span>

ps\_add\_note
=============

Adds note to current page

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_add\_note</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$llx`</span>
, <span class="methodparam"><span class="type">float</span>
`$lly`</span> , <span class="methodparam"><span
class="type">float</span> `$urx`</span> , <span
class="methodparam"><span class="type">float</span> `$ury`</span> ,
<span class="methodparam"><span class="type">string</span>
`$contents`</span> , <span class="methodparam"><span
class="type">string</span> `$title`</span> , <span
class="methodparam"><span class="type">string</span> `$icon`</span> ,
<span class="methodparam"><span class="type">int</span> `$open`</span> )

Adds a note at a certain position on the page. Notes are like little
rectangular sheets with text on it, which can be placed anywhere on a
page. They are shown either folded or unfolded. If folded, the specified
icon is used as a placeholder.

此说明在文档被打印或显示时不可见，只在文档用 Acrobat Distiller 或
Ghostview 转换成 PDF 时显示。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`llx`  
The x-coordinate of the lower left corner.

`lly`  
The y-coordinate of the lower left corner.

`urx`  
The x-coordinate of the upper right corner.

`ury`  
The y-coordinate of the upper right corner.

`contents`  
The text of the note.

`title`  
The title of the note as displayed in the header of the note.

`icon`  
The icon shown if the note is folded. This parameter can be set to
*comment*, *insert*, *note*, *paragraph*, *newparagraph*, *key*, or
*help*.

`open`  
If `open` is unequal to zero the note will be shown unfolded after
opening the document with a pdf viewer.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_add\_pdflink</span>
-   <span class="function">ps\_add\_launchlink</span>
-   <span class="function">ps\_add\_locallink</span>
-   <span class="function">ps\_add\_weblink</span>

ps\_add\_pdflink
================

Adds link to a page in a second pdf document

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_add\_pdflink</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$llx`</span>
, <span class="methodparam"><span class="type">float</span>
`$lly`</span> , <span class="methodparam"><span
class="type">float</span> `$urx`</span> , <span
class="methodparam"><span class="type">float</span> `$ury`</span> ,
<span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">int</span> `$page`</span> , <span class="methodparam"><span
class="type">string</span> `$dest`</span> )

Places a hyperlink at the given position pointing to a second pdf
document. Clicking on the link will branch to the document at the given
page. The first page in a document has number 1.

The hyperlink's source position is a rectangle with its lower left
corner at (`llx`, `lly`) and its upper right corner at (`urx`, `ury`).
The rectangle has by default a thin blue border.

此说明在文档被打印或显示时不可见，只在文档用 Acrobat Distiller 或
Ghostview 转换成 PDF 时显示。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`llx`  
The x-coordinate of the lower left corner.

`lly`  
The y-coordinate of the lower left corner.

`urx`  
The x-coordinate of the upper right corner.

`ury`  
The y-coordinate of the upper right corner.

`filename`  
The name of the pdf document to be opened when clicking on this link.

`page`  
The page number of the destination pdf document

`dest`  
The parameter `dest` determines how the document is being viewed. It can
be *fitpage*, *fitwidth*, *fitheight*, or *fitbbox*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_add\_launchlink</span>
-   <span class="function">ps\_add\_locallink</span>
-   <span class="function">ps\_add\_weblink</span>

ps\_add\_weblink
================

Adds link to a web location

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_add\_weblink</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$llx`</span>
, <span class="methodparam"><span class="type">float</span>
`$lly`</span> , <span class="methodparam"><span
class="type">float</span> `$urx`</span> , <span
class="methodparam"><span class="type">float</span> `$ury`</span> ,
<span class="methodparam"><span class="type">string</span> `$url`</span>
)

Places a hyperlink at the given position pointing to a web page. The
hyperlink's source position is a rectangle with its lower left corner at
(`llx`, `lly`) and its upper right corner at (`urx`, `ury`). The
rectangle has by default a thin blue border.

此说明在文档被打印或显示时不可见，只在文档用 Acrobat Distiller 或
Ghostview 转换成 PDF 时显示。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`llx`  
The x-coordinate of the lower left corner.

`lly`  
The y-coordinate of the lower left corner.

`urx`  
The x-coordinate of the upper right corner.

`ury`  
The y-coordinate of the upper right corner.

`url`  
The url of the hyperlink to be opened when clicking on this link, e.g.
*http://www.php.net*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_add\_launchlink</span>
-   <span class="function">ps\_add\_locallink</span>
-   <span class="function">ps\_add\_pdflink</span>

ps\_arc
=======

Draws an arc counterclockwise

### 说明

<span class="type">bool</span> <span class="methodname">ps\_arc</span> (
<span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$radius`</span> , <span
class="methodparam"><span class="type">float</span> `$alpha`</span> ,
<span class="methodparam"><span class="type">float</span> `$beta`</span>
)

Draws a portion of a circle with at middle point at (`x`, `y`). The arc
starts at an angle of `alpha` and ends at an angle of `beta`. It is
drawn counterclockwise (use <span class="function">ps\_arcn</span> to
draw clockwise). The subpath added to the current path starts on the arc
at angle `alpha` and ends on the arc at angle `beta`.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
The x-coordinate of the circle's middle point.

`y`  
The y-coordinate of the circle's middle point.

`radius`  
The radius of the circle

`alpha`  
The start angle given in degrees.

`beta`  
The end angle given in degrees.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_arcn</span>

ps\_arcn
========

Draws an arc clockwise

### 说明

<span class="type">bool</span> <span class="methodname">ps\_arcn</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$radius`</span> , <span
class="methodparam"><span class="type">float</span> `$alpha`</span> ,
<span class="methodparam"><span class="type">float</span> `$beta`</span>
)

Draws a portion of a circle with at middle point at (`x`, `y`). The arc
starts at an angle of `alpha` and ends at an angle of `beta`. It is
drawn clockwise (use <span class="function">ps\_arc</span> to draw
counterclockwise). The subpath added to the current path starts on the
arc at angle `beta` and ends on the arc at angle `alpha`.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
The x-coordinate of the circle's middle point.

`y`  
The y-coordinate of the circle's middle point.

`radius`  
The radius of the circle

`alpha`  
The starting angle given in degrees.

`beta`  
The end angle given in degrees.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_arc</span>

ps\_begin\_page
===============

Start a new page

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_begin\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

Starts a new page. Although the parameters `width` and `height` imply a
different page size for each page, this is not possible in PostScript.
The first call of <span class="function">ps\_begin\_page</span> will set
the page size for the whole document. Consecutive calls will have no
effect, except for creating a new page. The situation is different if
you intent to convert the PostScript document into PDF. This function
places pdfmarks into the document which can set the size for each page
indiviually. The resulting PDF document will have different page sizes.

Though PostScript does not know different page sizes, pslib places a
bounding box for each page into the document. This size is evaluated by
some PostScript viewers and will have precedence over the BoundingBox in
the Header of the document. This can lead to unexpected results when you
set a BoundingBox whose lower left corner is not (0, 0), because the
bounding box of the page will always have a lower left corner (0, 0) and
overwrites the global setting.

Each page is encapsulated into save/restore. This means, that most of
the settings made on one page will not be retained on the next page.

If there is up to the first call of <span
class="function">ps\_begin\_page</span> no call of <span
class="function">ps\_findfont</span>, then the header of the PostScript
document will be output and the bounding box will be set to the size of
the first page. The lower left corner of the bounding box is set to (0,
0). If <span class="function">ps\_findfont</span> was called before,
then the header has been output already, and the document will not have
a valid bounding box. In order to prevent this, one should call <span
class="function">ps\_set\_info</span> to set the info field
*BoundingBox* and possibly *Orientation* before any <span
class="function">ps\_findfont</span> or <span
class="function">ps\_begin\_page</span> calls.

> **Note**:
>
> Up to version 0.2.6 of pslib, this function will always overwrite the
> BoundingBox and Orientation, if it has been set before with <span
> class="function">ps\_set\_info</span> and <span
> class="function">ps\_findfont</span> has not been called before.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`width`  
The width of the page in pixel, e.g. 596 for A4 format.

`height`  
The height of the page in pixel, e.g. 842 for A4 format.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_end\_page</span>
-   <span class="function">ps\_findfont</span>
-   <span class="function">ps\_set\_info</span>

ps\_begin\_pattern
==================

Start a new pattern

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">ps\_begin\_pattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> , <span
class="methodparam"><span class="type">float</span> `$xstep`</span> ,
<span class="methodparam"><span class="type">float</span>
`$ystep`</span> , <span class="methodparam"><span
class="type">int</span> `$painttype`</span> )

Starts a new pattern. A pattern is like a page containing e.g. a drawing
which can be used for filling areas. It is used like a color by calling
<span class="function">ps\_setcolor</span> and setting the color space
to *pattern*.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`width`  
The width of the pattern in pixel.

`height`  
The height of the pattern in pixel.

`x-step`  
The distance in pixel of placements of the pattern in horizontal
direction.

`y-step`  
The distance in pixel of placements of the pattern in vertical
direction.

`painttype`  
Must be 1 or 2.

### 返回值

The identifier of the pattern 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 Creating and using a pattern**

``` php
<?php
$ps = ps_new();

if (!ps_open_file($ps, "pattern.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_parameter($ps, "warning", "true");
ps_set_info($ps, "Creator", "pattern.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Pattern example");


$pspattern = ps_begin_pattern($ps, 10.0, 10.0, 10.0, 10.0, 1);
ps_setlinewidth($ps, 0.2);
ps_setcolor($ps, "stroke", "rgb", 0.0, 0.0, 1.0, 0.0);
ps_moveto($ps, 0, 0);
ps_lineto($ps, 7, 7);
ps_stroke($ps);
ps_moveto($ps, 0, 7);
ps_lineto($ps, 7, 0);
ps_stroke($ps);
ps_end_pattern($ps);

ps_begin_page($ps, 596, 842);
ps_setcolor($ps, "both", "pattern", $pspattern, 0.0, 0.0, 0.0);
ps_rect($ps, 50, 400, 200, 200);
ps_fill($ps);
ps_end_page($ps);

ps_close($ps);
ps_delete($ps);
?>
```

### 参见

-   <span class="function">ps\_end\_pattern</span>
-   <span class="function">ps\_setcolor</span>
-   <span class="function">ps\_shading\_pattern</span>

ps\_begin\_template
===================

Start a new template

### 说明

<span class="type">int</span> <span
class="methodname">ps\_begin\_template</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

Starts a new template. A template is called a form in the postscript
language. It is created similar to a pattern but used like an image.
Templates are often used for drawings which are placed several times
through out the document, e.g. like a company logo. All drawing
functions may be used within a template. The template will not be drawn
until it is placed by <span class="function">ps\_place\_image</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`width`  
The width of the template in pixel.

`height`  
The height of the template in pixel.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Creating and using a template**

``` php
<?php
$ps = ps_new();

if (!ps_open_file($ps, "template.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_parameter($ps, "warning", "true");
ps_set_info($ps, "Creator", "template.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Template example");

$pstemplate = ps_begin_template($ps, 30.0, 30.0);
ps_moveto($ps, 0, 0);
ps_lineto($ps, 30, 30);
ps_moveto($ps, 0, 30);
ps_lineto($ps, 30, 0);
ps_stroke($ps);
ps_end_template($ps);

ps_begin_page($ps, 596, 842);
ps_place_image($ps, $pstemplate, 20.0, 20.0, 1.0);
ps_place_image($ps, $pstemplate, 50.0, 30.0, 0.5);
ps_place_image($ps, $pstemplate, 70.0, 70.0, 0.6);
ps_place_image($ps, $pstemplate, 30.0, 50.0, 1.3);
ps_end_page($ps);

ps_close($ps);
ps_delete($ps);
?>
```

### 参见

-   <span class="function">ps\_end\_template</span>

ps\_circle
==========

Draws a circle

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_circle</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$radius`</span> )

Draws a circle with its middle point at (`x`, `y`). The circle starts
and ends at position (`x`+`radius`, `y`). If this function is called
outside a path it will start a new path. If it is called within a path
it will add the circle as a subpath. If the last drawing operation does
not end in point (`x`+`radius`, `y`) then there will be a gap in the
path.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
The x-coordinate of the circle's middle point.

`y`  
The y-coordinate of the circle's middle point.

`radius`  
The radius of the circle

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_arc</span>
-   <span class="function">ps\_arcn</span>

ps\_clip
========

Clips drawing to current path

### 说明

<span class="type">bool</span> <span class="methodname">ps\_clip</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> )

Takes the current path and uses it to define the border of a clipping
area. Everything drawn outside of that area will not be visible.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_closepath</span>

ps\_close\_image
================

Closes image and frees memory

### 说明

<span class="type"><span class="type">void</span><span
class="type">false</span></span> <span
class="methodname">ps\_close\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span>
`$imageid`</span> )

Closes an image and frees its resources. Once an image is closed it
cannot be used anymore.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`imageid`  
Resource identifier of the image as returned by <span
class="function">ps\_open\_image</span> or <span
class="function">ps\_open\_image\_file</span>.

### 返回值

Returns **`null`** on success 或者在失败时返回 **`false`**.

### 参见

-   <span class="function">ps\_open\_image</span>
-   <span class="function">ps\_open\_image\_file</span>

ps\_close
=========

Closes a PostScript document

### 说明

<span class="type">bool</span> <span class="methodname">ps\_close</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> )

Closes the PostScript document.

This function writes the trailer of the PostScript document. It also
writes the bookmark tree. <span class="function">ps\_close</span> does
not free any resources, which is done by <span
class="function">ps\_delete</span>.

This function is also called by <span class="function">ps\_delete</span>
if it has not been called before.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_open\_file</span>
-   <span class="function">ps\_delete</span>

ps\_closepath\_stroke
=====================

Closes and strokes path

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_closepath\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

Connects the last point with first point of a path and draws the
resulting closed line.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_closepath</span>

ps\_closepath
=============

Closes path

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_closepath</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

Connects the last point with the first point of a path. The resulting
path can be used for stroking, filling, clipping, etc..

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_clip</span>
-   <span class="function">ps\_closepath\_stroke</span>

ps\_continue\_text
==================

Continue text in next line

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_continue\_text</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

Output a text one line below the last line. The line spacing is taken
from the value "leading" which must be set with <span
class="function">ps\_set\_value</span>. The actual position of the text
is determined by the values "textx" and "texty" which can be requested
with <span class="function">ps\_get\_value</span>

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text to output.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_show</span>
-   <span class="function">ps\_show\_xy</span>
-   <span class="function">ps\_show\_boxed</span>

ps\_curveto
===========

Draws a curve

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_curveto</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

Add a section of a cubic Bézier curve described by the three given
control points to the current path.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x1`  
x-coordinate of first control point.

`y1`  
y-coordinate of first control point.

`x2`  
x-coordinate of second control point.

`y2`  
y-coordinate of second control point.

`x3`  
x-coordinate of third control point.

`y3`  
y-coordinate of third control point.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_lineto</span>

ps\_delete
==========

Deletes all resources of a PostScript document

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> )

Mainly frees memory used by the document. Also closes a file, if it was
not closed before with <span class="function">ps\_close</span>. You
should in any case close the file with <span
class="function">ps\_close</span> before, because <span
class="function">ps\_close</span> not just closes the file but also
outputs a trailor containing PostScript comments like the number of
pages in the document and adding the bookmark hierarchy.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_close</span>

ps\_end\_page
=============

End a page

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_end\_page</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

Ends a page which was started with <span
class="function">ps\_begin\_page</span>. Ending a page will leave the
current drawing context, which e.g. requires to reload fonts if they
were loading within the page, and to set many other drawing parameters
like the line width, or color.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_begin\_page</span>

ps\_end\_pattern
================

End a pattern

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_end\_pattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

Ends a pattern which was started with <span
class="function">ps\_begin\_pattern</span>. Once a pattern has been
ended, it can be used like a color to fill areas.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_begin\_pattern</span>

ps\_end\_template
=================

End a template

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_end\_template</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

Ends a template which was started with <span
class="function">ps\_begin\_template</span>. Once a template has been
ended, it can be used like an image.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_begin\_template</span>

ps\_fill\_stroke
================

Fills and strokes the current path

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_fill\_stroke</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

Fills and draws the path constructed with previously called drawing
functions like <span class="function">ps\_lineto</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_fill</span>
-   <span class="function">ps\_stroke</span>

ps\_fill
========

Fills the current path

### 说明

<span class="type">bool</span> <span class="methodname">ps\_fill</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> )

Fills the path constructed with previously called drawing functions like
<span class="function">ps\_lineto</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_fill\_stroke</span>
-   <span class="function">ps\_stroke</span>

ps\_findfont
============

Loads a font

### 说明

<span class="type">int</span> <span
class="methodname">ps\_findfont</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">string</span> `$fontname`</span>
, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$embed`<span class="initializer"> =
**`false`**</span></span> \] )

Loads a font for later use. Before text is output with a loaded font it
must be set with <span class="function">ps\_setfont</span>. This
function needs the adobe font metric file in order to calculate the
space used up by the characters. A font which is loaded within a page
will only be available on that page. Fonts which are to be used in the
complete document have to be loaded before the first call of <span
class="function">ps\_begin\_page</span>. Calling <span
class="function">ps\_findfont</span> between pages will make that font
available for all following pages.

The name of the afm file must be `fontname`*.afm*. If the font shall be
embedded the file `fontname`*.pfb* containing the font outline must be
present as well.

Calling <span class="function">ps\_findfont</span> before the first page
requires to output the postscript header which includes the BoundingBox
for the whole document. Usually the BoundingBox is set with the first
call of <span class="function">ps\_begin\_page</span> which now comes
after <span class="function">ps\_findfont</span>. Consequently the
BoundingBox has not been set and a warning will be issued when <span
class="function">ps\_findfont</span> is called. In order to prevent this
situation, one should call <span
class="function">ps\_set\_parameter</span> to set the BoundingBox before
<span class="function">ps\_findfont</span> is called.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`fontname`  
The name of the font.

`encoding`  
<span class="function">ps\_findfont</span> will try to load the file
passed in the parameter `encoding`. Encoding files are of the same
syntax as those used by **dvips(1)**. They contain a font encoding
vector (which is currently not used but must be present) and a list of
extra ligatures to extend the list of ligatures derived from the afm
file.

`encoding` can be **`null`** or the empty string if the default encoding
(TeXBase1) shall be used.

If the encoding is set to *builtin* then there will be no reencoding and
the font specific encoding will be used. This is very useful with symbol
fonts.

`embed`  
If set to a value \>0 the font will be embedded into the document. This
requires the font outline (.pfb file) to be present.

### 返回值

Returns the identifier of the font or zero in case of an error. The
identifier is a positive number.

### 参见

-   <span class="function">ps\_begin\_page</span>
-   <span class="function">ps\_setfont</span>

ps\_get\_buffer
===============

Fetches the full buffer containig the generated PS data

### 说明

<span class="type">string</span> <span
class="methodname">ps\_get\_buffer</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> )

This function is not implemented yet. It will always return an empty
string. The idea for a later implementation is to write the contents of
the postscript file into an internal buffer if in memory creation is
requested, and retrieve the buffer content with this function.
Currently, documents created in memory are send to the browser without
buffering.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 参见

-   <span class="function">ps\_open\_file</span>

ps\_get\_parameter
==================

Gets certain parameters

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">ps\_get\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">float</span> `$modifier`</span> \] )

Gets several parameters which were directly set by <span
class="function">ps\_set\_parameter</span> or indirectly by one of the
other functions. Parameters are by definition string values. This
function cannot be used to retrieve resources which were also set by
<span class="function">ps\_set\_parameter</span>.

The parameter `name` can have the following values.

*fontname*  
The name of the currently active font or the font whose identifier is
passed in parameter `modifier`.

*fontencoding*  
The encoding of the currently active font.

*dottedversion*  
The version of the underlying pslib library in the format
\<major\>.\<minor\>.\<subminor\>

*scope*  
The current drawing scope. Can be object, document, null, page, pattern,
path, template, prolog, font, glyph.

*ligaturedisolvechar*  
The character which dissolves a ligature. If your are using a font which
contains the ligature \`ff' and \`\|' is the char to dissolve the
ligature, then \`f\|f' will result in two \`f' instead of the ligature
\`ff'.

*imageencoding*  
The encoding used for encoding images. Can be either *hex* or *85*. hex
encoding uses two bytes in the postscript file each byte in the image.
85 stand for Ascii85 encoding.

*linenumbermode*  
Set to *paragraph* if lines are numbered within a paragraph or *box* if
they are numbered within the surrounding box.

*linebreak*  
Only used if text is output with <span
class="function">ps\_show\_boxed</span>. If set to **`true`** a carriage
return will add a line break.

*parbreak*  
Only used if text is output with <span
class="function">ps\_show\_boxed</span>. If set to **`true`** a carriage
return will start a new paragraph.

*hyphenation*  
Only used if text is output with <span
class="function">ps\_show\_boxed</span>. If set to **`true`** the
paragraph will be hyphenated if a hypen dictionary is set and exists.

*hyphendict*  
Filename of the dictionary used for hyphenation pattern.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`name`  
Name of the parameter.

`modifier`  
An identifier needed if a parameter of a resource is requested, e.g. the
size of an image. In such a case the resource id is passed.

### 返回值

Returns the value of the parameter 或者在失败时返回 **`false`**.

### 参见

-   <span class="function">ps\_set\_parameter</span>

ps\_get\_value
==============

Gets certain values

### 说明

<span class="type">float</span> <span
class="methodname">ps\_get\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">float</span> `$modifier`</span> \] )

Gets several values which were set by <span
class="function">ps\_set\_value</span>. Values are by definition float
values.

The parameter `name` can have the following values.

*fontsize*  
The size of the currently active font or the font whose identifier is
passed in parameter `modifier`.

*font*  
The currently active font itself.

*imagewidth*  
The width of the image whose id is passed in the parameter `modifier`.

*imageheight*  
The height of the image whose id is passed in the parameter `modifier`.

*capheight*  
The height of a capital M in the currently active font or the font whose
identifier is passed in parameter `modifier`.

*ascender*  
The ascender of the currently active font or the font whose identifier
is passed in parameter `modifier`.

*descender*  
The descender of the currently active font or the font whose identifier
is passed in parameter `modifier`.

*italicangle*  
The italicangle of the currently active font or the font whose
identifier is passed in parameter `modifier`.

*underlineposition*  
The underlineposition of the currently active font or the font whose
identifier is passed in parameter `modifier`.

*underlinethickness*  
The underlinethickness of the currently active font or the font whose
identifier is passed in parameter `modifier`.

*textx*  
The current x-position for text output.

*texty*  
The current y-position for text output.

*textrendering*  
The current mode for text rendering.

*textrise*  
The space by which text is risen above the base line.

*leading*  
The distance between text lines in points.

*wordspacing*  
The space between words as a multiple of the width of a space char.

*charspacing*  
The space between chars. If charspacing is != 0.0 ligatures will always
be dissolved.

*hyphenminchars*  
Minimum number of chars hyphenated at the end of a word.

*parindent*  
Indention of the first n line in a paragraph.

*numindentlines*  
Number of line in a paragraph to indent if parindent != 0.0.

*parskip*  
Distance between paragraphs.

*linenumberspace*  
Overall space in front of each line for the line number.

*linenumbersep*  
Space between the line and the line number.

*major*  
The major version number of pslib.

*minor*  
The minor version number of pslib.

*subminor*, *revision*  
The subminor version number of pslib.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`name`  
Name of the value.

`modifier`  
The parameter `modifier` specifies the resource for which the value is
to be retrieved. This can be the id of a font or an image.

### 返回值

Returns the value of the parameter or **`false`**.

### 参见

-   <span class="function">ps\_set\_value</span>

ps\_hyphenate
=============

Hyphenates a word

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">ps\_hyphenate</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

Hyphenates the passed word. <span class="function">ps\_hyphenate</span>
evaluates the value hyphenminchars (set by <span
class="function">ps\_set\_value</span>) and the parameter hyphendict
(set by <span class="function">ps\_set\_parameter</span>). hyphendict
must be set before calling this function.

This function requires the locale category LC\_CTYPE to be set properly.
This is done when the extension is initialized by using the environment
variables. On Unix systems read the man page of locale for more
information.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
`text` should not contain any non alpha characters. Possible positions
for breaks are returned in an array of interger numbers. Each number is
the position of the char in `text` after which a hyphenation can take
place.

### 返回值

An array of integers indicating the position of possible breaks in the
text 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 Hyphennate a text**

``` php
<?php
$word = "Koordinatensystem";
$psdoc = ps_new();
ps_set_parameter($psdoc, "hyphendict", "hyph_de.dic");
$hyphens = ps_hyphenate($psdoc, $word);
for($i=0; $i<strlen($word); $i++) {
  echo $word[$i];
  if(in_array($i, $hyphens))
    echo "-";
}
ps_delete($psdoc);
?>
```

以上例程会输出：

    Ko-ordi-na-ten-sys-tem

### 参见

-   <span class="function">ps\_show\_boxed</span>
-   locale(1)

ps\_include\_file
=================

Reads an external file with raw PostScript code

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_include\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$file`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`file`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ps\_lineto
==========

Draws a line

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_lineto</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Adds a straight line from the current point to the given coordinates to
the current path. Use <span class="function">ps\_moveto</span> to set
the starting point of the line.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
x-coordinate of the end point of the line.

`y`  
y-coordinate of the end point of the line.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Drawing a rectangle**

``` php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "rectangle.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_info($ps, "Creator", "rectangle.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Lineto example");

ps_begin_page($ps, 596, 842);
ps_moveto($ps, 100, 100);
ps_lineto($ps, 100, 200);
ps_lineto($ps, 200, 200);
ps_lineto($ps, 200, 100);
ps_lineto($ps, 100, 100);
ps_stroke($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

### 参见

-   <span class="function">ps\_moveto</span>

ps\_makespotcolor
=================

Create spot color

### 说明

<span class="type">int</span> <span
class="methodname">ps\_makespotcolor</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$reserved`<span class="initializer"> =
0</span></span> \] )

Creates a spot color from the current fill color. The fill color must be
defined in rgb, cmyk or gray colorspace. The spot color name can be an
arbitrary name. A spot color can be set as any color with <span
class="function">ps\_setcolor</span>. When the document is not printed
but displayed by an postscript viewer the given color in the specified
color space is use.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`name`  
Name of the spot color, e.g. Pantone 5565.

### 返回值

The id of the new spot color or 0 in case of an error.

### 范例

**示例 \#1 Creating and using a spot color**

``` php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "spotcolor.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_info($ps, "Creator", "spotcolor.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Spot color example");

ps_begin_page($ps, 596, 842);
ps_setcolor($ps, "fill", "cmyk", 0.37, 0.0, 0.34, 0.34);
$spotcolor = ps_makespotcolor($ps, "PANTONE 5565 C", 0);
ps_setcolor($ps, "fill", "spot", $spotcolor, 0.5, 0.0, 0.0);
ps_moveto($ps, 100, 100);
ps_lineto($ps, 100, 200);
ps_lineto($ps, 200, 200);
ps_lineto($ps, 200, 100);
ps_lineto($ps, 100, 100);
ps_fill($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

This example creates the spot color "PANTONE 5565 C" which is a darker
green (olive) and fills a rectangle with 50% intensity.

### 参见

-   <span class="function">ps\_setcolor</span>

ps\_moveto
==========

Sets current point

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_moveto</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Sets the current point to new coordinates. If this is the first call of
<span class="function">ps\_moveto</span> after a previous path has been
ended then it will start a new path. If this function is called in the
middle of a path it will just set the current point and start a subpath.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
x-coordinate of the point to move to.

`y`  
y-coordinate of the point to move to.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_lineto</span>

ps\_new
=======

Creates a new PostScript document object

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span class="methodname">ps\_new</span>
( <span class="methodparam">void</span> )

Creates a new document instance. It does not create the file on disk or
in memory, it just sets up everything. <span
class="function">ps\_new</span> is usually followed by a call of <span
class="function">ps\_open\_file</span> to actually create the postscript
document.

### 返回值

Resource of PostScript document 或者在失败时返回 **`false`**. The return
value is passed to all other functions as the first argument.

### 参见

-   <span class="function">ps\_delete</span>

ps\_open\_file
==============

Opens a file for output

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_open\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$filename`</span> \] )

Creates a new file on disk and writes the PostScript document into it.
The file will be closed when <span class="function">ps\_close</span> is
called.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`filename`  
The name of the postscript file. If `filename` is not passed the
document will be created in memory and all output will go straight to
the browser.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_close</span>

ps\_open\_image\_file
=====================

Opens image from file

### 说明

<span class="type">int</span> <span
class="methodname">ps\_open\_image\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$type`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$stringparam`</span> \[, <span class="methodparam"><span
class="type">int</span> `$intparam`<span class="initializer"> =
0</span></span> \]\] )

Loads an image for later use.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`type`  
The type of the image. Possible values are *png*, *jpeg*, or *eps*.

`filename`  
The name of the file containing the image data.

`stringparam`  
Not used.

`intparam`  
Not used.

### 返回值

Returns identifier of image or zero in case of an error. The identifier
is a positive number greater than 0.

### 参见

-   <span class="function">ps\_open\_image</span>
-   <span class="function">ps\_place\_image</span>
-   <span class="function">ps\_close\_image</span>

ps\_open\_image
===============

Reads an image for later placement

### 说明

<span class="type">int</span> <span
class="methodname">ps\_open\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$type`</span> , <span class="methodparam"><span
class="type">string</span> `$source`</span> , <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$lenght`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> , <span class="methodparam"><span
class="type">int</span> `$height`</span> , <span
class="methodparam"><span class="type">int</span> `$components`</span> ,
<span class="methodparam"><span class="type">int</span> `$bpc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$params`</span> )

Reads an image which is already available in memory. The parameter
`source` is currently not evaluated and assumed to be *memory*. The
image data is a sequence of pixels starting in th upper left corner and
ending in the lower right corner. Each pixel consists of `components`
color components, and each component has `bpc` bits.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`type`  
The type of the image. Possible values are *png*, *jpeg*, or *eps*.

`source`  
Not used.

`data`  
The image data.

`length`  
The length of the image data.

`width`  
The width of the image.

`height`  
The height of the image.

`components`  
The number of components for each pixel. This can be 1 (gray scale
images), 3 (rgb images), or 4 (cmyk, rgba images).

`bpc`  
Number of bits per component (quite often 8).

`params`  

### 返回值

Returns identifier of image or zero in case of an error. The identifier
is a positive number greater than 0.

### 参见

-   <span class="function">ps\_open\_image\_file</span>
-   <span class="function">ps\_place\_image</span>
-   <span class="function">ps\_close\_image</span>

ps\_open\_memory\_image
=======================

Takes an GD image and returns an image for placement in a PS document

### 说明

<span class="type">int</span> <span
class="methodname">ps\_open\_memory\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$gd`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`gd`  

ps\_place\_image
================

Places image on the page

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_place\_image</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span>
`$imageid`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$scale`</span> )

Places a formerly loaded image on the page. The image can be scaled. If
the image shall be rotated as well, you will have to rotate the
coordinate system before with <span class="function">ps\_rotate</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`imageid`  
The resource identifier of the image as returned by <span
class="function">ps\_open\_image</span> or <span
class="function">ps\_open\_image\_file</span>.

`x`  
x-coordinate of the lower left corner of the image.

`y`  
y-coordinate of the lower left corner of the image.

`scale`  
The scaling factor for the image. A scale of 1.0 will result in a
resolution of 72 dpi, because each pixel is equivalent to 1 point.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_open\_image</span>
-   <span class="function">ps\_open\_image\_file</span>

ps\_rect
========

Draws a rectangle

### 说明

<span class="type">bool</span> <span class="methodname">ps\_rect</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$width`</span> , <span
class="methodparam"><span class="type">float</span> `$height`</span> )

Draws a rectangle with its lower left corner at (`x`, `y`). The
rectangle starts and ends in its lower left corner. If this function is
called outside a path it will start a new path. If it is called within a
path it will add the rectangle as a subpath. If the last drawing
operation does not end in the lower left corner then there will be a gap
in the path.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
x-coordinate of the lower left corner of the rectangle.

`y`  
y-coordinate of the lower left corner of the rectangle.

`width`  
The width of the image.

`height`  
The height of the image.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_arc</span>
-   <span class="function">ps\_cirle</span>
-   <span class="function">ps\_lineto</span>

ps\_restore
===========

Restore previously save context

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_restore</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> )

Restores a previously saved graphics context. Any call of <span
class="function">ps\_save</span> must be accompanied by a call to <span
class="function">ps\_restore</span>. All coordinate transformations,
line style settings, color settings, etc. are being restored to the
state before the call of <span class="function">ps\_save</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_save</span>

ps\_rotate
==========

Sets rotation factor

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_rotate</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$rot`</span> )

Sets the rotation of the coordinate system.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`rot`  
Angle of rotation in degree.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Rotation of the coordinate system**

``` php
<?php
function rectangle($ps) {
    ps_moveto($ps, 0, 0);
    ps_lineto($ps, 0, 50);
    ps_lineto($ps, 50, 50);
    ps_lineto($ps, 50, 0);
    ps_lineto($ps, 0, 0);
    ps_stroke($ps);
}

$ps = ps_new();
if (!ps_open_file($ps, "rotation.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_info($ps, "Creator", "rotation.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Rotation example");
ps_set_info($ps, "BoundingBox", "0 0 596 842");

$psfont = ps_findfont($ps, "Helvetica", "", 0);

ps_begin_page($ps, 596, 842);
ps_set_text_pos($ps, 100, 100);
ps_save($ps);
ps_translate($ps, 100, 100);
ps_rotate($ps, 45);
rectangle($ps);
ps_restore($ps);
ps_setfont($ps, $psfont, 8.0);
ps_show($ps, "Text without rotation");
ps_end_page($ps);

ps_delete($ps);
?>
```

The above example illustrates a very common way of rotating a graphic
(in this case just a rectangle) by simply rotating the coordinate
system. Since the graphic's coordinate system assumes (0,0) to be the
origin, the page coordinate system is also translated to place the
graphics not on the edge of the page. Pay attention to the order of
<span class="function">ps\_translate</span> and <span
class="function">ps\_rotate</span>. In the above case the rectancle is
rotated around the point (100, 100) in the untranslated coordinate
system. Switching the two statements has a completely different result.

In order to output the following text at the original position, all
modifications of the coordinate system are encapsulated in <span
class="function">ps\_save</span> and <span
class="function">ps\_restore</span>.

### 参见

-   <span class="function">ps\_scale</span>
-   <span class="function">ps\_translate</span>

ps\_save
========

Save current context

### 说明

<span class="type">bool</span> <span class="methodname">ps\_save</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> )

Saves the current graphics context, containing colors, translation and
rotation settings and some more. A saved context can be restored with
<span class="function">ps\_restore</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_restore</span>

ps\_scale
=========

Sets scaling factor

### 说明

<span class="type">bool</span> <span class="methodname">ps\_scale</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Sets horizontal and vertical scaling of the coordinate system.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
Scaling factor in horizontal direction.

`y`  
Scaling factor in vertical direction.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_rotate</span>
-   <span class="function">ps\_translate</span>

ps\_set\_border\_color
======================

Sets color of border for annotations

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_border\_color</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

Links added with one of the functions <span
class="function">ps\_add\_weblink</span>, <span
class="function">ps\_add\_pdflink</span>, etc. will be displayed with a
surounded rectangle when the postscript document is converted to pdf and
viewed in a pdf viewer. This rectangle is not visible in the postscript
document. This function sets the color of the rectangle's border line.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`red`  
The red component of the border color.

`green`  
The green component of the border color.

`blue`  
The blue component of the border color.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_set\_border\_dash</span>
-   <span class="function">ps\_set\_border\_style</span>

ps\_set\_border\_dash
=====================

Sets length of dashes for border of annotations

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_border\_dash</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$black`</span> , <span class="methodparam"><span
class="type">float</span> `$white`</span> )

Links added with one of the functions <span
class="function">ps\_add\_weblink</span>, <span
class="function">ps\_add\_pdflink</span>, etc. will be displayed with a
surounded rectangle when the postscript document is converted to pdf and
viewed in a pdf viewer. This rectangle is not visible in the postscript
document. This function sets the length of the black and white portion
of a dashed border line.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`black`  
The length of the dash.

`white`  
The length of the gap between dashes.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_set\_border\_color</span>
-   <span class="function">ps\_set\_border\_style</span>

ps\_set\_border\_style
======================

Sets border style of annotations

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_border\_style</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$style`</span> , <span class="methodparam"><span
class="type">float</span> `$width`</span> )

Links added with one of the functions <span
class="function">ps\_add\_weblink</span>, <span
class="function">ps\_add\_pdflink</span>, etc. will be displayed with a
surounded rectangle when the postscript document is converted to pdf and
viewed in a pdf viewer. This rectangle is not visible in the postscript
document. This function sets the appearance and width of the border
line.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`style`  
`style` can be *solid* or *dashed*.

`width`  
The line width of the border.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_set\_border\_color</span>
-   <span class="function">ps\_set\_border\_dash</span>

ps\_set\_info
=============

Sets information fields of document

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_info</span> ( <span
class="methodparam"><span class="type">resource</span> `$p`</span> ,
<span class="methodparam"><span class="type">string</span> `$key`</span>
, <span class="methodparam"><span class="type">string</span>
`$val`</span> )

Sets certain information fields of the document. This fields will be
shown as a comment in the header of the PostScript file. If the document
is converted to pdf this fields will also be used for the document
information.

The *BoundingBox* is usually set to the value given to the first page.
This only works if <span class="function">ps\_findfont</span> has not
been called before. In such cases the BoundingBox would be left unset
unless you set it explicitly with this function.

This function will have no effect anymore when the header of the
postscript file has been already written. It must be called before the
first page or the first call of <span
class="function">ps\_findfont</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`key`  
The name of the information field to set. The values which can be set
are *Keywords*, *Subject*, *Title*, *Creator*, *Author*, *BoundingBox*,
and *Orientation*. Be aware that some of them has a meaning to
PostScript viewers.

`value`  
The value of the information field. The field *Orientation* can be set
to either *Portrait* or *Landscape*. The *BoundingBox* is a string
consisting of four numbers. The first two numbers are the coordinates of
the lower left corner of the page. The last two numbers are the
coordinates of the upper right corner.

> **Note**:
>
> Up to version 0.2.6 of pslib, the BoundingBox and Orientation will be
> overwritten by <span class="function">ps\_begin\_page</span>, unless
> <span class="function">ps\_findfont</span> has been called before.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_findfont</span>
-   <span class="function">ps\_begin\_page</span>

ps\_set\_parameter
==================

Sets certain parameters

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_parameter</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

Sets several parameters which are used by many functions. Parameters are
by definition string values.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`name`  
For a list of possible names see <span
class="function">ps\_get\_parameter</span>.

`value`  
The value of the parameter.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_get\_parameters</span>
-   <span class="function">ps\_set\_value</span>

ps\_set\_text\_pos
==================

Sets position for text output

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_text\_pos</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

Set the position for the next text output. You may alternatively set the
x and y value separately by calling <span
class="function">ps\_set\_value</span> and choosing *textx* respectively
*texty* as the value name.

If you want to output text at a certain position it is more convenient
to use <span class="function">ps\_show\_xy</span> instead of setting the
text position and calling <span class="function">ps\_show</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
x-coordinate of the new text position.

`y`  
y-coordinate of the new text position.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Placing text at a given position**

``` php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "text.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_info($ps, "Creator", "rectangle.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Text placement example");

ps_begin_page($ps, 596, 842);
$psfont = ps_findfont($ps, "Helvetica", "", 0);
ps_setfont($ps, $psfont, 8.0);
ps_show_xy($ps, "Some text at (100, 100)", 100, 100);

ps_set_value($ps, "textx", 100);
ps_set_value($ps, "texty", 120);
ps_show($ps, "Some text at (100, 120)");
ps_end_page($ps);

ps_delete($ps);
?>
```

### 参见

-   <span class="function">ps\_set\_value</span>
-   <span class="function">ps\_show</span>

ps\_set\_value
==============

Sets certain values

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_set\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">float</span> `$value`</span> )

Sets several values which are used by many functions. Parameters are by
definition float values.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`name`  
The `name` can be one of the following:

textrendering  
The way how text is shown.

textx  
The x coordinate for text output.

texty  
The y coordinate for text output.

wordspacing  
The distance between words relative to the width of a space.

leading  
The distance between lines in pixels.

`value`  
The value of the parameter.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_get\_value</span>
-   <span class="function">ps\_set\_parameter</span>

ps\_setcolor
============

Sets current color

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setcolor</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">string</span> `$type`</span> ,
<span class="methodparam"><span class="type">string</span>
`$colorspace`</span> , <span class="methodparam"><span
class="type">float</span> `$c1`</span> , <span class="methodparam"><span
class="type">float</span> `$c2`</span> , <span class="methodparam"><span
class="type">float</span> `$c3`</span> , <span class="methodparam"><span
class="type">float</span> `$c4`</span> )

Sets the color for drawing, filling, or both.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`type`  
The parameter `type` can be *both*, *fill*, or *fillstroke*.

`colorspace`  
The colorspace should be one of *gray*, *rgb*, *cmyk*, *spot*,
*pattern*. Depending on the colorspace either only the first, the first
three or all parameters will be used.

`c1`  
Depending on the colorspace this is either the red component (rgb), the
cyan component (cmyk), the gray value (gray), the identifier of the spot
color or the identifier of the pattern.

`c2`  
Depending on the colorspace this is either the green component (rgb),
the magenta component (cmyk).

`c3`  
Depending on the colorspace this is either the blue component (rgb), the
yellow component (cmyk).

`c4`  
This must only be set in cmyk colorspace and specifies the black
component.

### Bugs

The second parameter is currently not always evaluated. The color is
sometimes set for filling and drawing just as if *fillstroke* were
passed.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ps\_setdash
===========

Sets appearance of a dashed line

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setdash</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$on`</span> , <span
class="methodparam"><span class="type">float</span> `$off`</span> )

Sets the length of the black and white portions of a dashed line.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`on`  
The length of the dash.

`off`  
The length of the gap between dashes.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_setpolydash</span>

ps\_setflat
===========

Sets flatness

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setflat</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`value`  
The `value` must be between 0.2 and 1.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ps\_setfont
===========

Sets font to use for following output

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setfont</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">int</span> `$fontid`</span> ,
<span class="methodparam"><span class="type">float</span> `$size`</span>
)

Sets a font, which has to be loaded before with <span
class="function">ps\_findfont</span>. Outputting text without setting a
font results in an error.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`fontid`  
The font identifier as returned by <span
class="function">ps\_findfont</span>.

`size`  
The size of the font.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_findfont</span>
-   <span class="function">ps\_set\_text\_pos</span> for an example.

ps\_setgray
===========

Sets gray value

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setgray</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">float</span> `$gray`</span> )

Sets the gray value for all following drawing operations.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`gray`  
The value must be between 0 (white) and 1 (black).

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_setcolor</span>

ps\_setlinecap
==============

Sets appearance of line ends

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setlinecap</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> )

Sets how line ends look like.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`type`  
The type of line ends. Possible values are *PS\_LINECAP\_BUTT*,
*PS\_LINECAP\_ROUND*, or *PS\_LINECAP\_SQUARED*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_setlinejoin</span>
-   <span class="function">ps\_setlinewidth</span>
-   <span class="function">ps\_setmiterlimit</span>

ps\_setlinejoin
===============

Sets how contected lines are joined

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setlinejoin</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> )

Sets how lines are joined.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`type`  
The way lines are joined. Possible values are *PS\_LINEJOIN\_MITER*,
*PS\_LINEJOIN\_ROUND*, or *PS\_LINEJOIN\_BEVEL*.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_setlinecap</span>
-   <span class="function">ps\_setlinewidth</span>
-   <span class="function">ps\_setmiterlimit</span>

ps\_setlinewidth
================

Sets width of a line

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setlinewidth</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> )

Sets the line width for all following drawing operations.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`width`  
The width of lines in points.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_setlinecap</span>
-   <span class="function">ps\_setlinejoin</span>
-   <span class="function">ps\_setmiterlimit</span>

ps\_setmiterlimit
=================

Sets the miter limit

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setmiterlimit</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span>
`$value`</span> )

If two lines join in a small angle and the line join is set to
*PS\_LINEJOIN\_MITER*, then the resulting spike will be very long. The
miter limit is the maximum ratio of the miter length (the length of the
spike) and the line width.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`value`  
The maximum ratio between the miter length and the line width. Larger
values (\> 10) will result in very long spikes when two lines meet in a
small angle. Keep the default unless you know what you are doing.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_setlinecap</span>
-   <span class="function">ps\_setlinejoin</span>
-   <span class="function">ps\_setlinewidth</span>

ps\_setoverprintmode
====================

Sets overprint mode

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setoverprintmode</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$mode`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`mode`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ps\_setpolydash
===============

Sets appearance of a dashed line

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_setpolydash</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$arr`</span>
)

Sets the length of the black and white portions of a dashed line. <span
class="function">ps\_setpolydash</span> is used to set more complicated
dash patterns.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`arr`  
`arr` is a list of length elements alternately for the black and white
portion.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Drawing a dashed line**

``` php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "polydash.ps")) {
   print "Cannot open PostScript file\n";
     exit;
}

ps_set_info($ps, "Creator", "polydash.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Poly dash example");

ps_begin_page($ps, 596, 842);
ps_setpolydash($ps, array(10, 5, 2, 5));
ps_moveto($ps, 100, 100);
ps_lineto($ps, 200, 200);
ps_stroke($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

This example draws a line with a 10 and 2 points long line, and gaps of
5 points inbetween.

### 参见

-   <span class="function">ps\_setdash</span>

ps\_shading\_pattern
====================

Creates a pattern based on a shading

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">ps\_shading\_pattern</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span>
`$shadingid`</span> , <span class="methodparam"><span
class="type">string</span> `$optlist`</span> )

Creates a pattern based on a shading, which has to be created before
with <span class="function">ps\_shading</span>. Shading patterns can be
used like regular patterns.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`shadingid`  
The identifier of a shading previously created with <span
class="function">ps\_shading</span>.

`optlist`  
This argument is not currently used.

### 返回值

The identifier of the pattern 或者在失败时返回 **`false`**.

### 参见

-   <span class="function">ps\_shading</span>
-   <span class="function">ps\_shfill</span>

ps\_shading
===========

Creates a shading for later use

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">ps\_shading</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">string</span> `$type`</span> ,
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

Creates a shading, which can be used by <span
class="function">ps\_shfill</span> or <span
class="function">ps\_shading\_pattern</span>.

The color of the shading can be in any color space except for *pattern*.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`type`  
The type of shading can be either *radial* or *axial*. Each shading
starts with the current fill color and ends with the given color values
passed in the parameters `c1` to `c4` (see <span
class="function">ps\_setcolor</span> for their meaning).

`x0, x1, y0, y1`  
The coordinates `x0`, `y0`, `x1`, `y1` are the start and end point of
the shading. If the type of shading is *radial* the two points are the
middle points of a starting and ending circle.

`c1, c2, c3, c4`  
See <span class="function">ps\_setcolor</span> for their meaning.

`optlist`  
If the shading is of type *radial* the `optlist` must also contain the
parameters *r0* and *r1* with the radius of the start and end circle.

### 返回值

Returns the identifier of the pattern 或者在失败时返回 **`false`**.

### 参见

-   <span class="function">ps\_shading\_pattern</span>
-   <span class="function">ps\_shfill</span>

ps\_shfill
==========

Fills an area with a shading

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_shfill</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">int</span> `$shadingid`</span> )

Fills an area with a shading, which has to be created before with <span
class="function">ps\_shading</span>. This is an alternative way to
creating a pattern from a shading <span
class="function">ps\_shading\_pattern</span> and using the pattern as
the filling color.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`shadingid`  
The identifier of a shading previously created with <span
class="function">ps\_shading</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_shading</span>
-   <span class="function">ps\_shading\_pattern</span>

ps\_show\_boxed
===============

Output text in a box

### 说明

<span class="type">int</span> <span
class="methodname">ps\_show\_boxed</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">float</span> `$left`</span> , <span
class="methodparam"><span class="type">float</span> `$bottom`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> , <span
class="methodparam"><span class="type">string</span> `$hmode`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$feature`</span> \] )

Outputs a text in a given box. The lower left corner of the box is at
(`left`, `bottom`). Line breaks will be inserted where needed. Multiple
spaces are treated as one. Tabulators are treated as spaces.

The text will be hyphenated if the parameter `hyphenation` is set to
**`true`** and the parameter `hyphendict` contains a valid filename for
a hyphenation file. The line spacing is taken from the value *leading*.
Paragraphs can be separated by an empty line just like in TeX. If the
value *parindent* is set to value \> 0.0 then the first n lines will be
indented. The number n of lines is set by the parameter
*numindentlines*. In order to prevent indenting of the first m
paragraphs set the value *parindentskip* to a positive number.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text to be output into the given box.

`left`  
x-coordinate of the lower left corner of the box.

`bottom`  
y-coordinate of the lower left corner of the box.

`width`  
Width of the box.

`height`  
Height of the box.

`hmode`  
The parameter `hmode` can be "justify", "fulljustify", "right", "left",
or "center". The difference of "justify" and "fulljustify" just affects
the last line of the box. In fulljustify mode the last line will be left
and right justified unless this is also the last line of paragraph. In
justify mode it will always be left justified.

`feature`  

### Used parameters

The output of <span class="function">ps\_show\_boxed</span> can be
configured with several parameters and values which must be set with
either <span class="function">ps\_set\_parameter</span> or <span
class="function">ps\_set\_value</span>. Beside the parameters and values
which affect text output, the following parameters and values are
evaluated.

leading (value)  
Distance between baselines of two consecutive lines.

linebreak (parameter)  
Set to "true" if you want a carriage return to start a new line instead
of treating it as a space. Defaults to "false".

parbreak (parameter)  
Set to "true" if you want a carriage return on a single line to start a
new paragraph instead of treating it as a space. Defaults to "true".

hyphenation (parameter)  
Set to "true" in order to turn hyphenation on. This requires a
dictionary to be set with the parameter "hyphendict". Defaults to
"false".

hyphendict (parameter)  
Filename of the dictionary used for hyphenation pattern (see below).

hyphenminchar (value)  
The number of chars which must at least be left over before or after the
hyphen. This implies that only words of at least two times this value
will be hyphenated. The default value is three. Setting a value of zero
will result in the default value.

parindent (value)  
Set the amount of space in pixel for indenting the first m lines of a
paragraph. m can be set with the value "numindentlines".

parskip (value)  
Set the amount of extra space in pixel between paragraphs. Defaults to 0
which will result in a normal line distance.

numindentlines (value)  
Number of lines from the start of the paragraph which will be indented.
Defaults to 1.

parindentskip (value)  
Number of paragraphs in the box whose first lines will not be indented.
This defaults to 0. This is useful for paragraphs right after a section
heading or text being continued in a second box. In both case one would
set this to 1.

linenumbermode (parameter)  
Set how lines are to be numbered. Possible values are "box" for
numbering lines in the whole box or "paragraph" to number lines within
each paragraph.

linenumberspace (value)  
The space for the column left of the numbered line containing the line
number. The line number will be right justified into this column.
Defaults to 20.

linenumbersep (value)  
The space between the column with line numbers and the line itself.
Defaults to 5.

### Hyphenation

Text is hyphenated if the parameter *hyphenation* is set to true and a
valid hyphenation dictionary is set. pslib does not ship its own
hyphenation dictionary but uses one from openoffice, scribus or koffice.
You can find their dictionaries for different languages in one of the
following directories if the software is installed:

-   `/usr/share/apps/koffice/hyphdicts/`
-   `/usr/lib/scribus/dicts/`
-   `/usr/lib/openoffice/share/dict/ooo/`

Currently scribus appears to have the most complete hyphenation
dictionaries.

### 返回值

Number of characters that could not be written.

### 参见

-   <span class="function">ps\_continue\_text</span>

ps\_show\_xy2
=============

Output text at position

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_show\_xy2</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span class="type">int</span>
`$len`</span> , <span class="methodparam"><span
class="type">float</span> `$xcoor`</span> , <span
class="methodparam"><span class="type">float</span> `$ycoor`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ps\_show\_xy
============

Output text at given position

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_show\_xy</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

Output a text at the given text position.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text to be output.

`x`  
x-coordinate of the lower left corner of the box surrounding the text.

`y`  
y-coordinate of the lower left corner of the box surrounding the text.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_continue\_text</span>
-   <span class="function">ps\_show</span>

ps\_show2
=========

Output a text at current position

### 说明

<span class="type">bool</span> <span class="methodname">ps\_show2</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">int</span> `$len`</span> )

Output text at the current position. Do not print more than `len`
characters.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text to be output.

`len`  
The maximum number of characters to print.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ps\_show
========

Output text

### 说明

<span class="type">bool</span> <span class="methodname">ps\_show</span>
( <span class="methodparam"><span class="type">resource</span>
`$psdoc`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

Output a text at the current text position. The text position can be set
by storing the x and y coordinates into the values *textx* and *texty*
with the function <span class="function">ps\_set\_value</span>. The
function will issue an error if a font was not set before with <span
class="function">ps\_setfont</span>.

<span class="function">ps\_show</span> evaluates the following
parameters and values as set by <span
class="function">ps\_set\_parameter</span> and <span
class="function">ps\_set\_value</span>.

charspacing (value)  
Distance between two consecutive glyphs. If this value is unequal to
zero then all ligatures will be resolved. Values less than zero are
allowed.

kerning (parameter)  
Setting this parameter to "false" will turn off kerning. Kerning is
turned on by default.

ligatures (parameter)  
Setting this parameter to "false" will turn off the use of ligatures.
Ligatures are turned on by default.

underline (parameter)  
Setting this parameter to "true" will turn on underlining. Underlining
is turned off by default.

overline (parameter)  
Setting this parameter to "true" will turn on overlining. Overlining is
turned off by default.

strikeout (parameter)  
Setting this parameter to "true" will turn on striking out. Striking out
is turned off by default.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text to be output.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_continue\_text</span>
-   <span class="function">ps\_show\_xy</span>
-   <span class="function">ps\_setfont</span>

ps\_string\_geometry
====================

Gets geometry of a string

### 说明

<span class="type">array</span> <span
class="methodname">ps\_string\_geometry</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> \[, <span class="methodparam"><span
class="type">int</span> `$fontid`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">float</span> `$size`<span class="initializer"> =
0.0</span></span> \]\] )

This function is similar to <span
class="function">ps\_stringwidth</span> but returns an array of
dimensions containing the width, ascender, and descender of the text.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text for which the geometry is to be calculated.

`fontid`  
The identifier of the font to be used. If not font is specified the
current font will be used.

`size`  
The size of the font. If no size is specified the current size is used.

### 返回值

An array of the dimensions of a string. The element 'width' contains the
width of the string as returned by <span
class="function">ps\_stringwidth</span>. The element 'descender'
contains the maximum descender and 'ascender' the maximum ascender of
the string.

### 参见

-   <span class="function">ps\_continue\_text</span>
-   <span class="function">ps\_stringwidth</span>

ps\_stringwidth
===============

Gets width of a string

### 说明

<span class="type">float</span> <span
class="methodname">ps\_stringwidth</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> \[, <span class="methodparam"><span
class="type">int</span> `$fontid`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">float</span> `$size`<span class="initializer"> =
0.0</span></span> \]\] )

Calculates the width of a string in points if it was output in the given
font and font size. This function needs an Adobe font metrics file to
calculate the precise width. If kerning is turned on, it will be taken
into account.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`text`  
The text for which the width is to be calculated.

`fontid`  
The identifier of the font to be used. If not font is specified the
current font will be used.

`size`  
The size of the font. If no size is specified the current size is used.

### 返回值

Width of a string in points.

### 参见

-   <span class="function">ps\_string\_geometry</span>

ps\_stroke
==========

Draws the current path

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_stroke</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> )

Draws the path constructed with previously called drawing functions like
<span class="function">ps\_lineto</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_closepath\_stroke</span>
-   <span class="function">ps\_fill</span>
-   <span class="function">ps\_fill\_stroke</span>

ps\_symbol\_name
================

Gets name of a glyph

### 说明

<span class="type">string</span> <span
class="methodname">ps\_symbol\_name</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$ord`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$fontid`<span class="initializer"> = 0</span></span> \] )

This function needs an Adobe font metrics file to know which glyphs are
available.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`ord`  
The parameter `ord` is the position of the glyph in the font encoding
vector.

`fontid`  
The identifier of the font to be used. If not font is specified the
current font will be used.

### 返回值

The name of a glyph in the given font.

### 参见

-   <span class="function">ps\_symbol</span>
-   <span class="function">ps\_symbol\_width</span>

ps\_symbol\_width
=================

Gets width of a glyph

### 说明

<span class="type">float</span> <span
class="methodname">ps\_symbol\_width</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">int</span> `$ord`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$fontid`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$size`<span
class="initializer"> = 0.0</span></span> \]\] )

Calculates the width of a glyph in points if it was output in the given
font and font size. This function needs an Adobe font metrics file to
calculate the precise width.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`ord`  
The position of the glyph in the font encoding vector.

`fontid`  
The identifier of the font to be used. If not font is specified the
current font will be used.

`size`  
The size of the font. If no size is specified the current size is used.

### 返回值

The width of a glyph in points.

### 参见

-   <span class="function">ps\_symbol</span>
-   <span class="function">ps\_symbol\_name</span>

ps\_symbol
==========

Output a glyph

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_symbol</span> ( <span class="methodparam"><span
class="type">resource</span> `$psdoc`</span> , <span
class="methodparam"><span class="type">int</span> `$ord`</span> )

Output the glyph at position `ord` in the font encoding vector of the
current font. The font encoding for a font can be set when loading the
font with <span class="function">ps\_findfont</span>.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`ord`  
The position of the glyph in the font encoding vector.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ps\_symbol\_name</span>
-   <span class="function">ps\_symbol\_width</span>

ps\_translate
=============

Sets translation

### 说明

<span class="type">bool</span> <span
class="methodname">ps\_translate</span> ( <span
class="methodparam"><span class="type">resource</span> `$psdoc`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

Sets a new initial point of the coordinate system.

### 参数

`psdoc`  
Resource identifier of the postscript file as returned by <span
class="function">ps\_new</span>.

`x`  
x-coordinate of the origin of the translated coordinate system.

`y`  
y-coordinate of the origin of the translated coordinate system.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Translation of the coordinate system**

``` php
<?php
function rectangle($ps) {
    ps_moveto($ps, 0, 0);
    ps_lineto($ps, 0, 50);
    ps_lineto($ps, 50, 50);
    ps_lineto($ps, 50, 0);
    ps_lineto($ps, 0, 0);
    ps_stroke($ps);
}

$ps = ps_new();
if (!ps_open_file($ps, "translate.ps")) {
  print "Cannot open PostScript file\n";
  exit;
}

ps_set_info($ps, "Creator", "translate.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Translated example");
ps_set_info($ps, "BoundingBox", "0 0 596 842");

$psfont = ps_findfont($ps, "Helvetica", "", 0);

ps_begin_page($ps, 596, 842);
ps_set_text_pos($ps, 100, 100);
ps_translate($ps, 500, 750);
rectangle($ps);
ps_translate($ps, -500, -750);
ps_setfont($ps, $psfont, 8.0);
ps_show($ps, "Text at initial position");
ps_end_page($ps);

ps_begin_page($ps, 596, 842);
ps_set_text_pos($ps, 100, 100);
ps_save($ps);
ps_translate($ps, 500, 750);
rectangle($ps);
ps_restore($ps);
ps_setfont($ps, $psfont, 8.0);
ps_show($ps, "Text at initial position");
ps_end_page($ps);

ps_delete($ps);
?>
```

The above example demonstrates two possible ways to place a graphic (in
this case just a rectangle) at any position on the page, while the
graphic itself uses its own coordinate system. The trick is to change
the origin of the current coordinate system before drawing the
rectangle. The translation has to be undone after the graphic has been
drawn.

On the second page a slightly different and more elegant approach is
applied. Instead of undoing the translation with a second call of <span
class="function">ps\_translate</span> the graphics context is saved
before modifying the coordinate system and restored after drawing the
rectangle.

### 参见

-   <span class="function">ps\_scale</span>
-   <span class="function">ps\_rotate</span>

**目录**

-   [ps\_add\_bookmark](/ref/ps.html#ps_add_bookmark) — Add bookmark to
    current page
-   [ps\_add\_launchlink](/ref/ps.html#ps_add_launchlink) — Adds link
    which launches file
-   [ps\_add\_locallink](/ref/ps.html#ps_add_locallink) — Adds link to a
    page in the same document
-   [ps\_add\_note](/ref/ps.html#ps_add_note) — Adds note to current
    page
-   [ps\_add\_pdflink](/ref/ps.html#ps_add_pdflink) — Adds link to a
    page in a second pdf document
-   [ps\_add\_weblink](/ref/ps.html#ps_add_weblink) — Adds link to a web
    location
-   [ps\_arc](/ref/ps.html#ps_arc) — Draws an arc counterclockwise
-   [ps\_arcn](/ref/ps.html#ps_arcn) — Draws an arc clockwise
-   [ps\_begin\_page](/ref/ps.html#ps_begin_page) — Start a new page
-   [ps\_begin\_pattern](/ref/ps.html#ps_begin_pattern) — Start a new
    pattern
-   [ps\_begin\_template](/ref/ps.html#ps_begin_template) — Start a new
    template
-   [ps\_circle](/ref/ps.html#ps_circle) — Draws a circle
-   [ps\_clip](/ref/ps.html#ps_clip) — Clips drawing to current path
-   [ps\_close\_image](/ref/ps.html#ps_close_image) — Closes image and
    frees memory
-   [ps\_close](/ref/ps.html#ps_close) — Closes a PostScript document
-   [ps\_closepath\_stroke](/ref/ps.html#ps_closepath_stroke) — Closes
    and strokes path
-   [ps\_closepath](/ref/ps.html#ps_closepath) — Closes path
-   [ps\_continue\_text](/ref/ps.html#ps_continue_text) — Continue text
    in next line
-   [ps\_curveto](/ref/ps.html#ps_curveto) — Draws a curve
-   [ps\_delete](/ref/ps.html#ps_delete) — Deletes all resources of a
    PostScript document
-   [ps\_end\_page](/ref/ps.html#ps_end_page) — End a page
-   [ps\_end\_pattern](/ref/ps.html#ps_end_pattern) — End a pattern
-   [ps\_end\_template](/ref/ps.html#ps_end_template) — End a template
-   [ps\_fill\_stroke](/ref/ps.html#ps_fill_stroke) — Fills and strokes
    the current path
-   [ps\_fill](/ref/ps.html#ps_fill) — Fills the current path
-   [ps\_findfont](/ref/ps.html#ps_findfont) — Loads a font
-   [ps\_get\_buffer](/ref/ps.html#ps_get_buffer) — Fetches the full
    buffer containig the generated PS data
-   [ps\_get\_parameter](/ref/ps.html#ps_get_parameter) — Gets certain
    parameters
-   [ps\_get\_value](/ref/ps.html#ps_get_value) — Gets certain values
-   [ps\_hyphenate](/ref/ps.html#ps_hyphenate) — Hyphenates a word
-   [ps\_include\_file](/ref/ps.html#ps_include_file) — Reads an
    external file with raw PostScript code
-   [ps\_lineto](/ref/ps.html#ps_lineto) — Draws a line
-   [ps\_makespotcolor](/ref/ps.html#ps_makespotcolor) — Create spot
    color
-   [ps\_moveto](/ref/ps.html#ps_moveto) — Sets current point
-   [ps\_new](/ref/ps.html#ps_new) — Creates a new PostScript document
    object
-   [ps\_open\_file](/ref/ps.html#ps_open_file) — Opens a file for
    output
-   [ps\_open\_image\_file](/ref/ps.html#ps_open_image_file) — Opens
    image from file
-   [ps\_open\_image](/ref/ps.html#ps_open_image) — Reads an image for
    later placement
-   [ps\_open\_memory\_image](/ref/ps.html#ps_open_memory_image) — Takes
    an GD image and returns an image for placement in a PS document
-   [ps\_place\_image](/ref/ps.html#ps_place_image) — Places image on
    the page
-   [ps\_rect](/ref/ps.html#ps_rect) — Draws a rectangle
-   [ps\_restore](/ref/ps.html#ps_restore) — Restore previously save
    context
-   [ps\_rotate](/ref/ps.html#ps_rotate) — Sets rotation factor
-   [ps\_save](/ref/ps.html#ps_save) — Save current context
-   [ps\_scale](/ref/ps.html#ps_scale) — Sets scaling factor
-   [ps\_set\_border\_color](/ref/ps.html#ps_set_border_color) — Sets
    color of border for annotations
-   [ps\_set\_border\_dash](/ref/ps.html#ps_set_border_dash) — Sets
    length of dashes for border of annotations
-   [ps\_set\_border\_style](/ref/ps.html#ps_set_border_style) — Sets
    border style of annotations
-   [ps\_set\_info](/ref/ps.html#ps_set_info) — Sets information fields
    of document
-   [ps\_set\_parameter](/ref/ps.html#ps_set_parameter) — Sets certain
    parameters
-   [ps\_set\_text\_pos](/ref/ps.html#ps_set_text_pos) — Sets position
    for text output
-   [ps\_set\_value](/ref/ps.html#ps_set_value) — Sets certain values
-   [ps\_setcolor](/ref/ps.html#ps_setcolor) — Sets current color
-   [ps\_setdash](/ref/ps.html#ps_setdash) — Sets appearance of a dashed
    line
-   [ps\_setflat](/ref/ps.html#ps_setflat) — Sets flatness
-   [ps\_setfont](/ref/ps.html#ps_setfont) — Sets font to use for
    following output
-   [ps\_setgray](/ref/ps.html#ps_setgray) — Sets gray value
-   [ps\_setlinecap](/ref/ps.html#ps_setlinecap) — Sets appearance of
    line ends
-   [ps\_setlinejoin](/ref/ps.html#ps_setlinejoin) — Sets how contected
    lines are joined
-   [ps\_setlinewidth](/ref/ps.html#ps_setlinewidth) — Sets width of a
    line
-   [ps\_setmiterlimit](/ref/ps.html#ps_setmiterlimit) — Sets the miter
    limit
-   [ps\_setoverprintmode](/ref/ps.html#ps_setoverprintmode) — Sets
    overprint mode
-   [ps\_setpolydash](/ref/ps.html#ps_setpolydash) — Sets appearance of
    a dashed line
-   [ps\_shading\_pattern](/ref/ps.html#ps_shading_pattern) — Creates a
    pattern based on a shading
-   [ps\_shading](/ref/ps.html#ps_shading) — Creates a shading for later
    use
-   [ps\_shfill](/ref/ps.html#ps_shfill) — Fills an area with a shading
-   [ps\_show\_boxed](/ref/ps.html#ps_show_boxed) — Output text in a box
-   [ps\_show\_xy2](/ref/ps.html#ps_show_xy2) — Output text at position
-   [ps\_show\_xy](/ref/ps.html#ps_show_xy) — Output text at given
    position
-   [ps\_show2](/ref/ps.html#ps_show2) — Output a text at current
    position
-   [ps\_show](/ref/ps.html#ps_show) — Output text
-   [ps\_string\_geometry](/ref/ps.html#ps_string_geometry) — Gets
    geometry of a string
-   [ps\_stringwidth](/ref/ps.html#ps_stringwidth) — Gets width of a
    string
-   [ps\_stroke](/ref/ps.html#ps_stroke) — Draws the current path
-   [ps\_symbol\_name](/ref/ps.html#ps_symbol_name) — Gets name of a
    glyph
-   [ps\_symbol\_width](/ref/ps.html#ps_symbol_width) — Gets width of a
    glyph
-   [ps\_symbol](/ref/ps.html#ps_symbol) — Output a glyph
-   [ps\_translate](/ref/ps.html#ps_translate) — Sets translation
