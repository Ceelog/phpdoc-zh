wkhtmltox
=========

**目录**

-   [简介](/intro/wkhtmltox.html)
-   [安装／配置](/wkhtmltox/setup.html)
    -   [需求](/wkhtmltox/setup.html#需求)
    -   [安装](/wkhtmltox/setup.html#安装)
    -   [运行时配置](/wkhtmltox/setup.html#运行时配置)
-   [wkhtmltox\\PDF\\Converter](/class/wkhtmltox-pdf-converter.html) —
    The wkhtmltox\\PDF\\Converter class
    -   [wkhtmltox\\PDF\\Converter::add](/class/wkhtmltox-pdf-converter.html#wkhtmltox\PDF\Converter::add)
        — Add an object for conversion
    -   [wkhtmltox\\PDF\\Converter::\_\_construct](/class/wkhtmltox-pdf-converter.html#wkhtmltox\PDF\Converter::__construct)
        — Create a new PDF converter
    -   [wkhtmltox\\PDF\\Converter::convert](/class/wkhtmltox-pdf-converter.html#wkhtmltox\PDF\Converter::convert)
        — Perform PDF conversion
    -   [wkhtmltox\\PDF\\Converter::getVersion](/class/wkhtmltox-pdf-converter.html#wkhtmltox\PDF\Converter::getVersion)
        — Determine version of Converter
-   [wkhtmltox\\PDF\\Object](/class/wkhtmltox-pdf-object.html) — The
    wkhtmltox\\PDF\\Object class
    -   [wkhtmltox\\PDF\\Object::\_\_construct](/class/wkhtmltox-pdf-object.html#wkhtmltox\PDF\Object::__construct)
        — Create a new PDF Object
-   [wkhtmltox\\Image\\Converter](/class/wkhtmltox-image-converter.html)
    — The wkhtmltox\\Image\\Converter class
    -   [wkhtmltox\\Image\\Converter::\_\_construct](/class/wkhtmltox-image-converter.html#wkhtmltox\Image\Converter::__construct)
        — Create a new Image converter
    -   [wkhtmltox\\Image\\Converter::convert](/class/wkhtmltox-image-converter.html#wkhtmltox\Image\Converter::convert)
        — Perform Image conversion
    -   [wkhtmltox\\Image\\Converter::getVersion](/class/wkhtmltox-image-converter.html#wkhtmltox\Image\Converter::getVersion)
        — Determine version of Converter

简介
----

Converts an HTML input, or set of HTML inputs, into PDF output

类摘要
------

**wkhtmltox\\PDF\\Converter**

<span class="ooclass"> class **wkhtmltox\\PDF\\Converter** </span> {

/\* Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$settings`</span>
\] )

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">add</span> ( <span class="methodparam"><span
class="type">wkhtmltox\\PDF\\Object</span> `$object`</span> )

<span class="modifier">public</span> <span class="type">?string</span>
<span class="methodname">convert</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

}

wkhtmltox\\PDF\\Converter::add
==============================

Add an object for conversion

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">wkhtmltox\\PDF\\Converter::add</span> ( <span
class="methodparam"><span class="type">wkhtmltox\\PDF\\Object</span>
`$object`</span> )

Adds the given object to conversion

### 参数

`object`  
The object to add

wkhtmltox\\PDF\\Converter::\_\_construct
========================================

Create a new PDF converter

### 说明

<span class="modifier">public</span> <span
class="methodname">wkhtmltox\\PDF\\Converter::\_\_construct</span> (\[
<span class="methodparam"><span class="type">array</span>
`$settings`</span> \] )

Creates a PDF converter, using optional configuration settings

### 参数

`settings`  
<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
<th>Values</th>
<th>Changelog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>size.pageSize</td>
<td>paper size of output document</td>
<td>A4</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>size.width</td>
<td>with of the output document</td>
<td>210mm</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>size.height</td>
<td>height of the output document</td>
<td>297mm</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>orientation</td>
<td>orientation of the output document</td>
<td><table>
<tbody>
<tr class="odd">
<td>Landscape</td>
</tr>
<tr class="even">
<td>Portrait</td>
</tr>
</tbody>
</table></td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>colorMode</td>
<td>color mode of the output document</td>
<td><table>
<tbody>
<tr class="odd">
<td>Color</td>
</tr>
<tr class="even">
<td>Greyscale</td>
</tr>
</tbody>
</table></td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>resolution</td>
<td>resoluition of the output document</td>
<td>most likely has no effect</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>dpi</td>
<td>dpi to use while printing</td>
<td>80</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>pageOffset</td>
<td>integer added to page numbers generating headers, footers, and toc</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>copies</td>
<td> </td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>collate</td>
<td>collate copies</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>outline</td>
<td>generate PDF outline</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>outlineDepth</td>
<td>maximum depth of outline</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>dumpOutline</td>
<td>path of file to dump outline XML</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>out</td>
<td>path of output file, if "-" stdout is used</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>documentTitle</td>
<td>title for the output document</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>useCompression</td>
<td>enable or disable lossless compression</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>margin.top</td>
<td>size of the top margin</td>
<td>2cm</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>margin.bottom</td>
<td>size of the bottom margin</td>
<td>2cm</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>margin.left</td>
<td>size of the left margin</td>
<td>2cm</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>margin.right</td>
<td>size of the right margin</td>
<td>2cm</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>imageDPI</td>
<td>maximum DPI for images in the output document</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>imageQuality</td>
<td>the jpeg compression factor for images in the output document</td>
<td>94</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.cookieJar</td>
<td>path of file used to load and store cookies</td>
<td>/tmp/cookies.txt</td>
<td>&gt;= 0.1.0</td>
</tr>
</tbody>
</table>

wkhtmltox\\PDF\\Converter::convert
==================================

Perform PDF conversion

### 说明

<span class="modifier">public</span> <span class="type">?string</span>
<span class="methodname">wkhtmltox\\PDF\\Converter::convert</span> (
<span class="methodparam">void</span> )

Performs conversion of all previously added Objects

### 参数

此函数没有参数。

### 返回值

Where the return value is used, it will be populated with the contents
of the conversion buffer

wkhtmltox\\PDF\\Converter::getVersion
=====================================

Determine version of Converter

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">wkhtmltox\\PDF\\Converter::getVersion</span> (
<span class="methodparam">void</span> )

Determines the version of Converter as reported by libwkhtmltox

### 参数

此函数没有参数。

### 返回值

Returns a version string

简介
----

Represents an HTML document, input to PDF converter

类摘要
------

**wkhtmltox\\PDF\\Object**

<span class="ooclass"> class **wkhtmltox\\PDF\\Object** </span> {

/\* Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$buffer`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$settings`</span> \] )

}

wkhtmltox\\PDF\\Object::\_\_construct
=====================================

Create a new PDF Object

### 说明

<span class="modifier">public</span> <span
class="methodname">wkhtmltox\\PDF\\Object::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$buffer`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$settings`</span> \] )

Creates a new PDF Object from the given buffer and optional
configuration settings

### 参数

`buffer`  
HTML

`settings`  
<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
<th>Values</th>
<th>Changelog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>page</td>
<td>URL or path of the HTML to convert</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>useExternalLinks</td>
<td>set true to convert external links in the input into external PDF links in the output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>useLocalLinks</td>
<td>set true to convert internal links in the input into internal PDF links in the output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>produceForms</td>
<td>set true to turn HTML forms into PDF forms</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>replacements</td>
<td>undocumented</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>includeInOutline</td>
<td>set true to include sections from this object in the outline and toc</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>pagesCount</td>
<td>set true to make page count in toc inclusive of the number of pages in this object</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>tocXsl</td>
<td>set to style sheet to convert this object into a toc object</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>toc.useDottedLines</td>
<td>set true to use dotted lines in toc</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>toc.captionText</td>
<td>the caption text for toc</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>toc.forwardLinks</td>
<td>set true to create links from toc to content</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>toc.backLinks</td>
<td>set true to create links from content to toc</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>toc.indentation</td>
<td>indentation for toc</td>
<td>2em</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>toc.fontScale</td>
<td>the factor to scale down the font at every toc level</td>
<td>0.8</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>header.fontSize</td>
<td>font size for use in header</td>
<td>13</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>header.fontName</td>
<td>name of font for use in header</td>
<td>times</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>header.left</td>
<td>text for left of header</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>header.center</td>
<td>text for center of header</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>header.right</td>
<td>text for right of header</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>header.line</td>
<td>enable or disable horizontal rule under header</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>header.spacing</td>
<td>space between header and content</td>
<td>1.8</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>header.htmlUrl</td>
<td>URL or path of HTML to use in header</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>footer.fontSize</td>
<td>font size for use in footer</td>
<td>13</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>footer.fontName</td>
<td>name of font for use in footer</td>
<td>times</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>footer.left</td>
<td>text for left of footer</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>footer.center</td>
<td>text for center of footer</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>footer.right</td>
<td>text for right of footer</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>footer.line</td>
<td>enable or disable horizontal rule under footer</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>footer.spacing</td>
<td>space between footer and content</td>
<td>1.8</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>footer.htmlUrl</td>
<td>URL or path of HTML to use in footer</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.username</td>
<td>user name to use when loging into a website</td>
<td>bart</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.password</td>
<td>the password to used when logging into a website</td>
<td>elbarto</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.jsdelay</td>
<td>the amount of time in milliseconds to wait after a page is loaded until it is captured</td>
<td>1200</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.zoomFactor</td>
<td>how much zoom should be applied to the content</td>
<td>2.2</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.customHeaders</td>
<td>custom headers to send when requesting the main web page</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.repertCustomHeaders</td>
<td>set true to send with all requests</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.cookies</td>
<td>cookie string to send when requesting the main web page</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.post</td>
<td>post string to send when requesting the main web page</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.blockLocalFileAccess</td>
<td>disallow local and piped files to access other local files</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.stopSlowScript</td>
<td>stop slow running javascript</td>
<td>boolean</td>
<td> </td>
</tr>
<tr class="odd">
<td>load.debugJavascript</td>
<td>allow javascript to raise warnings</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.loadErrorHandling</td>
<td>set error handling strategy</td>
<td><table>
<tbody>
<tr class="odd">
<td>abort</td>
<td>abort the convertion process</td>
</tr>
<tr class="even">
<td>skip</td>
<td>do not add the object to the final output</td>
</tr>
<tr class="odd">
<td>ignore</td>
<td>try to add the object to the final output</td>
</tr>
</tbody>
</table></td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.proxy</td>
<td> </td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.background</td>
<td>include background image in output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.loadImages</td>
<td>include images in output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.enableJavascript</td>
<td>enable or disable javascript</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.enableIntelligentShrinking</td>
<td>enable to attempt to fit more content on page, only applies to PDF output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.minimumFontSize</td>
<td>the minimum font size allowed</td>
<td>9</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.printMediaType</td>
<td>print content using print media type instead of screen media type</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.defaultEncoding</td>
<td>content to use where no encoding is specified</td>
<td>utf-8</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.userStyleSheet</td>
<td>URL or path to a user specified style sheet</td>
<td>/path/to/style.css</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.enablePlugins</td>
<td>enable or disable NS plugins</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
</tbody>
</table>

简介
----

Converts an HTML input into various image formats

类摘要
------

**wkhtmltox\\Image\\Converter**

<span class="ooclass"> class **wkhtmltox\\Image\\Converter** </span> {

/\* Constructor \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$buffer`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$settings`</span> \]\] )

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">?string</span>
<span class="methodname">convert</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

}

wkhtmltox\\Image\\Converter::\_\_construct
==========================================

Create a new Image converter

### 说明

<span class="modifier">public</span> <span
class="methodname">wkhtmltox\\Image\\Converter::\_\_construct</span> (\[
<span class="methodparam"><span class="type">string</span>
`$buffer`</span> \[, <span class="methodparam"><span
class="type">array</span> `$settings`</span> \]\] )

Creates an Image converter, optionally taking an input buffer and
configuration settings

### 参数

`buffer`  
HTML

`settings`  
<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Description</th>
<th>Values</th>
<th>Changelog</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>in</td>
<td>URL or path of the input file, if "-" stdin is used</td>
<td>/path/to/markup.html</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>out</td>
<td>path of output file, if "-" stdout is used, by default an internal buffer is used</td>
<td>/path/to/output.png</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>fmt</td>
<td>output format to use</td>
<td><table>
<tbody>
<tr class="odd">
<td>""</td>
<td>default</td>
</tr>
<tr class="even">
<td>jpg</td>
<td>output as JPEG</td>
</tr>
<tr class="odd">
<td>png</td>
<td>output as PNG</td>
</tr>
<tr class="even">
<td>bmp</td>
<td>output as bitmap</td>
</tr>
<tr class="odd">
<td>svg</td>
<td>output as SVG</td>
</tr>
</tbody>
</table></td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>transparent</td>
<td>when outputting a PNG or SVG, make the white background transparent</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>screenWidth</td>
<td>the with of the screen used to render in pixels</td>
<td>800</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>smartWidth</td>
<td>when true, screenWidth is expanded to the content width</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>quality</td>
<td>compression factor to use when outputting a JPEG image</td>
<td>94</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>crop.left</td>
<td>left/x coordinate of the window to capture in pixels</td>
<td>200</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>crop.top</td>
<td>top/y coordinate of the window to capture in pixels</td>
<td>200</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>crop.width</td>
<td>width of the window to capture in pixels</td>
<td>200</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>crop.height</td>
<td>height of the window to capture in pixels</td>
<td>200</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.cookieJar</td>
<td>path of file used to load and store cookies</td>
<td>/tmp/cookies.txt</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.username</td>
<td>user name to use when loging into a website</td>
<td>bart</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.password</td>
<td>the password to used when logging into a website</td>
<td>elbarto</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.jsdelay</td>
<td>the amount of time in milliseconds to wait after a page is loaded until it is captured</td>
<td>1200</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.zoomFactor</td>
<td>how much zoom should be applied to the content</td>
<td>2.2</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.customHeaders</td>
<td>custom headers to send when requesting the main web page</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.repertCustomHeaders</td>
<td>set true to send with all requests</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.cookies</td>
<td>cookie string to send when requesting the main web page</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.post</td>
<td>post string to send when requesting the main web page</td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.blockLocalFileAccess</td>
<td>disallow local and piped files to access other local files</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.stopSlowScript</td>
<td>stop slow running javascript</td>
<td>boolean</td>
<td> </td>
</tr>
<tr class="odd">
<td>load.debugJavascript</td>
<td>allow javascript to raise warnings</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>load.loadErrorHandling</td>
<td>set error handling strategy</td>
<td><table>
<tbody>
<tr class="odd">
<td>abort</td>
<td>abort the convertion process</td>
</tr>
<tr class="even">
<td>skip</td>
<td>do not add the object to the final output</td>
</tr>
<tr class="odd">
<td>ignore</td>
<td>try to add the object to the final output</td>
</tr>
</tbody>
</table></td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>load.proxy</td>
<td> </td>
<td> </td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.background</td>
<td>include background image in output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.loadImages</td>
<td>include images in output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.enableJavascript</td>
<td>enable or disable javascript</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.enableIntelligentShrinking</td>
<td>enable to attempt to fit more content on page, only applies to PDF output</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.minimumFontSize</td>
<td>the minimum font size allowed</td>
<td>9</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.printMediaType</td>
<td>print content using print media type instead of screen media type</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.defaultEncoding</td>
<td>content to use where no encoding is specified</td>
<td>utf-8</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="odd">
<td>web.userStyleSheet</td>
<td>URL or path to a user specified style sheet</td>
<td>/path/to/style.css</td>
<td>&gt;= 0.1.0</td>
</tr>
<tr class="even">
<td>web.enablePlugins</td>
<td>enable or disable NS plugins</td>
<td>boolean</td>
<td>&gt;= 0.1.0</td>
</tr>
</tbody>
</table>

wkhtmltox\\Image\\Converter::convert
====================================

Perform Image conversion

### 说明

<span class="modifier">public</span> <span class="type">?string</span>
<span class="methodname">wkhtmltox\\Image\\Converter::convert</span> (
<span class="methodparam">void</span> )

Performs conversion of the input buffer

### 参数

此函数没有参数。

### 返回值

Where the return value is used, it will be populated with the contents
of the conversion buffer

wkhtmltox\\Image\\Converter::getVersion
=======================================

Determine version of Converter

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">wkhtmltox\\Image\\Converter::getVersion</span>
( <span class="methodparam">void</span> )

Determines the version of Converter as reported by libwkhtmltox

### 参数

此函数没有参数。

### 返回值

Returns a version string

**Warning**

This is not yet implemented by libwkhtmltox
