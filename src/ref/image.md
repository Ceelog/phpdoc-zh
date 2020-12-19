gd\_info
========

取得当前安装的 GD 库的信息

### 说明

<span class="type">array</span> <span class="methodname">gd\_info</span>
( <span class="methodparam">void</span> )

返回一个关联数组描述了安装的 GD 库的版本和性能。

| 属性               | 含义                                                                                                                                                                                                 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GD Version         | <span class="type">string</span> 值描述了安装的 *libgd* 的版本。                                                                                                                                     |
| Freetype Support   | <span class="type">boolean</span> 值。如果安装了 Freetype 支持则为 **`true`**。                                                                                                                      |
| Freetype Linkage   | <span class="type">string</span> 值描述了 Freetype 连接的方法。取值可能为：'with freetype', 'with TTF library' 和 'with unknown library'。本单元仅在 *Freetype Support* 的值为 **`true`** 时有定义。 |
| T1Lib Support      | <span class="type">boolean</span> 值。如果包含有 *T1Lib* 支持则为 **`true`**。                                                                                                                       |
| GIF Read Support   | <span class="type">boolean</span> 值。如果包含有*读取* *GIF* 图像的支持则为 **`true`**。                                                                                                             |
| GIF Create Support | <span class="type">boolean</span> 值。如果包含有*创建* *GIF* 图像的支持则为 **`true`**。                                                                                                             |
| JPG Support        | <span class="type">boolean</span> 值。如果包含有 *JPG* 支持则为 **`true`**。                                                                                                                         |
| PNG Support        | <span class="type">boolean</span> 值。如果包含有 *PNG* 支持则为 **`true`**。                                                                                                                         |
| WBMP Support       | <span class="type">boolean</span> 值。如果包含有 *WBMP* 支持则为 **`true`**。                                                                                                                        |
| XBM Support        | <span class="type">boolean</span> 值。如果包含有 *XBM* 支持则为 **`true`**。                                                                                                                         |

**示例 \#1 使用 <span class="function">gd\_info</span>**

``` php
<?php
var_dump(gd_info());
?>
```

典型输出为：

    array(9) {
      ["GD Version"]=>
      string(24) "bundled (2.0 compatible)"
      ["FreeType Support"]=>
      bool(false)
      ["T1Lib Support"]=>
      bool(false)
      ["GIF Read Support"]=>
      bool(true)
      ["GIF Create Support"]=>
      bool(false)
      ["JPG Support"]=>
      bool(false)
      ["PNG Support"]=>
      bool(true)
      ["WBMP Support"]=>
      bool(true)
      ["XBM Support"]=>
      bool(false)
    }

参见 <span class="function">imagepng</span>，<span
class="function">imagejpeg</span>，<span
class="function">imagegif</span>，<span
class="function">imagewbmp</span> 和 <span
class="function">imagetypes</span>。

getimagesize
============

取得图像大小

### 说明

<span class="type">array</span> <span
class="methodname">getimagesize</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$imageinfo`</span>
\] )

<span class="function">getimagesize</span> 函数将测定任何
GIF，JPG，PNG，SWF，SWC，PSD，TIFF，BMP，IFF，JP2，JPX，JB2，JPC，XBM 或
WBMP 图像文件的大小并返回图像的尺寸以及文件类型和一个可以用于普通 HTML
文件中 `IMG` 标记中的 height/width 文本字符串。

如果不能访问 `filename` 指定的图像或者其不是有效的图像，<span
class="function">getimagesize</span> 将返回 **`false`** 并产生一条
`E_WARNING` 级的错误。

> **Note**:
>
> 对 JPC，JP2，JPX，JB2，XBM 和 WBMP 的支持自 PHP 4.3.2 起可用。对 SWC
> 的支持自 PHP 4.3.0 起可用。对 TIFF 的支持是 PHP 4.2.0 添加的。

> **Note**: <span class="simpara"> JPEG 2000 支持是 PHP 4.3.2
> 添加的。注意 JPC 和 JP2
> 可以有不同的色彩深度的成分。此情况下，“bits”的值是碰到的最高的位深度。此外，JP2
> 文件可能包含有多个 JPEG 2000 代码流，此情况下，<span
> class="function">getimagesize</span>
> 返回此文件顶层中碰到的第一个代码流的值。 </span>

> **Note**: <span class="simpara"> 本函数不需要 GD 图像库。 </span>

返回一个具有四个单元的数组。索引 0 包含图像宽度的像素值，索引 1
包含图像高度的像素值。索引 2 是图像类型的标记：1 = GIF，2 = JPG，3 =
PNG，4 = SWF，5 = PSD，6 = BMP，7 = TIFF(intel byte order)，8 =
TIFF(motorola byte order)，9 = JPC，10 = JP2，11 = JPX，12 = JB2，13 =
SWC，14 = IFF，15 = WBMP，16 = XBM。这些标记与 PHP 4.3.0 新加的
IMAGETYPE 常量对应。索引 3 是文本字符串，内容为“height="yyy"
width="xxx"”，可直接用于 IMG 标记。

**示例 \#1 getimagesize（文件）**

``` php
<?php
list($width, $height, $type, $attr) = getimagesize("img/flag.jpg");
echo "<img src=\"img/flag.jpg\" $attr>";
?>
```

URL 支持是 PHP 4.0.5 添加的。

**示例 \#2 getimagesize（URL）**

``` php
<?php
$size = getimagesize("http://www.example.com/gifs/logo.gif");

// if the file name has space in it, encode it properly
$size = getimagesize("http://www.example.com/gifs/lo%20go.gif");

?>
```

对于 JPG 图像，还会多返回两个索引：*channels* 和 *bits*。*channels* 对于
RGB 图像其值为 3，对于 CMYK 图像其值为 4。*bits* 是每种颜色的位数。

自 PHP 4.3.0 起，*bits* 和 *channels*
对于其它图像类型也存在。但是这些值可能会把人搞糊涂。例如，GIF
总是对每个像素使用 3 个 channel，但是对于动画 GIF
来说每个像素的位数无法通过全局颜色表计算出来。

某些格式可能不包含图像或者包含多个图像。此种情况下，<span
class="function">getimagesize</span>
可能不能用来准确测定图像的大小。此时 <span
class="function">getimagesize</span> 将返回零作为宽度和高度。

自 PHP 4.3.0 起，<span class="function">getimagesize</span>
还会返回额外的参数 *mime*，符合该图像的 MIME 类型。此信息可以用来在 HTTP
Content-type 头信息中发送正确的信息：

**示例 \#3 getimagesize() 和 MIME 类型**

``` php
<?php
$size = getimagesize($filename);
$fp=fopen($filename, "rb");
if ($size && $fp) {
  header("Content-type: {$size['mime']}");
  fpassthru($fp);
  exit;
} else {
  // error
}
?>
```

可选的 `imageinfo`
参数允许从图像文件中提取一些扩展信息。目前，这将以一个关联数组返回不同的
JPG APP 标识。某些程序用这些 APP
标识来在图像中嵌入文本信息。一个非常常见的是 APP13 标识中嵌入的 IPTC
<a href="http://www.iptc.org/" class="link external">» http://www.iptc.org/</a>
信息。可以用 <span class="function">iptcparse</span> 函数来将二进制的
APP13 标识解析为可读的信息。

**示例 \#4 getimagesize() 返回 IPTC**

``` php
<?php
$size = getimagesize("testimg.jpg", &$info);
if (isset($info["APP13"])) {
    $iptc = iptcparse($info["APP13"]);
    var_dump($iptc);
}
?>
```

参见 <span class="function">image\_type\_to\_mime\_type</span>，<span
class="function">exif\_imagetype</span>，<span
class="function">exif\_read\_data</span> 和 <span
class="function">exif\_thumbnail</span>。

### 参数

`filename`  
This parameter specifies the file you wish to retrieve information
about. It can reference a local file or (configuration permitting) a
remote file using one of the supported streams.

`imageinfo`  
This optional parameter allows you to extract some extended information
from the image file. Currently, this will return the different JPG APP
markers as an associative array. Some programs use these APP markers to
embed text information in images. A very common one is to embed
<a href="http://www.iptc.org/" class="link external">» IPTC</a>
information in the APP13 marker. You can use the <span
class="function">iptcparse</span> function to parse the binary APP13
marker into something readable.

### 返回值

Returns an array with 7 elements.

Index 0 and 1 contains respectively the width and the height of the
image.

> **Note**:
>
> Some formats may contain no image or may contain multiple images. In
> these cases, <span class="function">getimagesize</span> might not be
> able to properly determine the image size. <span
> class="function">getimagesize</span> will return zero for width and
> height in these cases.

Index 2 is one of the *IMAGETYPE\_XXX* constants indicating the type of
the image.

Index 3 is a text string with the correct *height="yyy" width="xxx"*
string that can be used directly in an IMG tag.

*mime* is the correspondant MIME type of the image. This information can
be used to deliver images with the correct HTTP *Content-type* header:

**示例 \#5 <span class="function">getimagesize</span> and MIME types**

``` php
<?php
$size = getimagesize($filename);
$fp = fopen($filename, "rb");
if ($size && $fp) {
    header("Content-type: {$size['mime']}");
    fpassthru($fp);
    exit;
} else {
    // error
}
?>
```

*channels* will be 3 for RGB pictures and 4 for CMYK pictures.

*bits* is the number of bits for each color.

For some image types, the presence of *channels* and *bits* values can
be a bit confusing. As an example, GIF always uses 3 channels per pixel,
but the number of bits per pixel cannot be calculated for an animated
GIF with a global color table.

On failure, **`false`** is returned.

### 错误／异常

If accessing the `filename` image is impossible, or if it isn't a valid
picture, <span class="function">getimagesize</span> will generate an
error of level **`E_WARNING`**. On read error, <span
class="function">getimagesize</span> will generate an error of level
**`E_NOTICE`**.

### 更新日志

| 版本  | 说明                                                                                      |
|-------|-------------------------------------------------------------------------------------------|
| 5.3.0 | Added icon support.                                                                       |
| 5.2.3 | Read errors generated by this function downgraded to **`E_NOTICE`** from **`E_WARNING`**. |
| 4.3.2 | Support for JPC, JP2, JPX, JB2, XBM, and WBMP became available.                           |
| 4.3.2 | JPEG 2000 support was added for the `imageinfo` parameter.                                |
| 4.3.0 | *bits* and *channels* are present for other image types, too.                             |
| 4.3.0 | *mime* was added.                                                                         |
| 4.3.0 | Support for SWC and IFF was added.                                                        |
| 4.2.0 | Support for TIFF was added.                                                               |
| 4.0.6 | Support for BMP and PSD was added.                                                        |
| 4.0.5 | URL support was added.                                                                    |

### 范例

**示例 \#6 <span class="function">getimagesize</span> example**

``` php
<?php
list($width, $height, $type, $attr) = getimagesize("img/flag.jpg");
echo "<img src=\"img/flag.jpg\" $attr alt=\"getimagesize() example\" />";
?>
```

**示例 \#7 getimagesize (URL)**

``` php
<?php
$size = getimagesize("http://www.example.com/gifs/logo.gif");

// if the file name has space in it, encode it properly
$size = getimagesize("http://www.example.com/gifs/lo%20go.gif");

?>
```

**示例 \#8 getimagesize() returning IPTC**

``` php
<?php
$size = getimagesize("testimg.jpg", $info);
if (isset($info["APP13"])) {
    $iptc = iptcparse($info["APP13"]);
    var_dump($iptc);
}
?>
```

### 注释

> **Note**:
>
> 此函数不需要 GD 图象库。

### 参见

-   <span class="function">image\_type\_to\_mime\_type</span>
-   <span class="function">exif\_imagetype</span>
-   <span class="function">exif\_read\_data</span>
-   <span class="function">exif\_thumbnail</span>

getimagesizefromstring
======================

从字符串中获取图像尺寸信息

### 说明

<span class="type">array</span> <span
class="methodname">getimagesizefromstring</span> ( <span
class="methodparam"><span class="type">string</span> `$imagedata`</span>
\[, <span class="methodparam"><span class="type">array</span>
`&$imageinfo`</span> \] )

同 <span class="function">getimagesize</span> 函数。 区别是 <span
class="function">getimagesizefromstring</span>
第一个参数是图像数据的字符串表达，而不是文件名。

关于本函数如何工作的更多信息请参见 <span
class="function">getimagesize</span> 函数。

### 参数

`imagedata`  
图像数据的字符串表示。

`imageinfo`  
参见 <span class="function">getimagesize</span> 函数。

### 返回值

参见 <span class="function">getimagesize</span> 函数。

### 范例

**示例 \#1 <span class="function">getimagesizefromstring</span>
函数例程**

``` php
<?php
$img = '/path/to/test.png';

// 以文件方式打开
$size_info1 = getimagesize($img);

// 以字符串格式打开
$data       = file_get_contents($img);
$size_info2 = getimagesizefromstring($data);
?>
```

### 参见

-   <span class="function">getimagesize</span>

image\_type\_to\_extension
==========================

取得图像类型的文件后缀

### 说明

<span class="type">string</span> <span
class="methodname">image\_type\_to\_extension</span> ( <span
class="methodparam"><span class="type">int</span> `$imagetype`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$include_dot`<span class="initializer"> = **`true`**</span></span> \] )

根据给定的常量 *IMAGETYPE\_XXX* 返回后缀名。

### 参数

`imagetype`  
*IMAGETYPE\_XXX* 系列常量之一。

`include_dot`  
是否在后缀名前加一个点。默认是 **`true`**。

### 返回值

根据指定的图像类型返回对应的后缀名。

### 范例

**示例 \#1 <span class="function">image\_type\_to\_extension</span>
例子**

``` php
<?php
// 创建图像实例
$im = imagecreatetruecolor(100, 100);

// 保存图像
imagepng($im, './test' . image_type_to_extension(IMAGETYPE_PNG));
imagedestroy($im);
?>
```

### 注释

> **Note**:
>
> 此函数不需要 GD 图象库。

image\_type\_to\_mime\_type
===========================

取得 getimagesize，exif\_read\_data，exif\_thumbnail，exif\_imagetype
所返回的图像类型的 MIME 类型

### 说明

<span class="type">string</span> <span
class="methodname">image\_type\_to\_mime\_type</span> ( <span
class="methodparam"><span class="type">int</span> `$imagetype`</span> )

<span class="function">image\_type\_to\_mime\_type</span>
函数可以判断一个 IMAGETYPE 常量的 MIME 类型。

**示例 \#1 image\_type\_to\_mime\_type (file)**

``` php
<?php
header("Content-type: " . image_type_to_mime_type(IMAGETYPE_PNG));
?>
```

返回值如下：

| 图像类型（`imagetype`）                       | 返回值                          |
|-----------------------------------------------|---------------------------------|
| **`IMAGETYPE_GIF`**                           | *image/gif*                     |
| **`IMAGETYPE_JPEG`**                          | *image/jpeg*                    |
| **`IMAGETYPE_PNG`**                           | *image/png*                     |
| **`IMAGETYPE_SWF`**                           | *application/x-shockwave-flash* |
| **`IMAGETYPE_PSD`**                           | *image/psd*                     |
| **`IMAGETYPE_BMP`**                           | *image/bmp*                     |
| **`IMAGETYPE_TIFF_II`** (intel byte order)    | *image/tiff*                    |
| **`IMAGETYPE_TIFF_MM`** (motorola byte order) | *image/tiff*                    |
| **`IMAGETYPE_JPC`**                           | *application/octet-stream*      |
| **`IMAGETYPE_JP2`**                           | *image/jp2*                     |
| **`IMAGETYPE_JPX`**                           | *application/octet-stream*      |
| **`IMAGETYPE_JB2`**                           | *application/octet-stream*      |
| **`IMAGETYPE_SWC`**                           | *application/x-shockwave-flash* |
| **`IMAGETYPE_IFF`**                           | *image/iff*                     |
| **`IMAGETYPE_WBMP`**                          | *image/vnd.wap.wbmp*            |
| **`IMAGETYPE_XBM`**                           | *image/xbm*                     |

> **Note**: <span class="simpara"> 本函数不需要 GD 库。 </span>

参见 <span class="function">getimagesize</span>，<span
class="function">exif\_imagetype</span>，<span
class="function">exif\_read\_data</span> 和 <span
class="function">exif\_thumbnail</span>。

image2wbmp
==========

以 WBMP 格式将图像输出到浏览器或文件

### 说明

<span class="type">int</span> <span class="methodname">image2wbmp</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$threshold`</span>
\]\] )

<span class="function">image2wbmp</span> 从 `image` 图像创建一个名为
`filename` 的 WBMP 文件。`image` 参数是某个图像创建函数的返回值，例如
<span class="function">imagecreatetruecolor</span>。

`filename` 参数是可选项，如果省略，则直接将原图像流输出。通过用 <span
class="function">header</span> 发送 image/vnd.wap.wbmp 的
Content-type，可以创建直接输出 WBMP 图像的 PHP 脚本。

**示例 \#1 <span class="function">image2wbmp</span> 例子**

``` php
<?php
$file = 'php.jpg';
$image = imagecreatefrompng($file);
header('Content-type: ' . image_type_to_mime(IMAGETYPE_WBMP));
image2wbmp($file); // output the stream directly
?>
```

> **Note**:
>
> WBMP 支持仅在 PHP 编译时加入了 GD-1.8 或更高版本时可用。

参见 <span class="function">imagewbmp</span>。

imageaffine
===========

返回经过仿射变换后的图像，剪切区域可选

### 说明

<span class="type">resource</span> <span
class="methodname">imageaffine</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">array</span> `$affine`</span> \[,
<span class="methodparam"><span class="type">array</span> `$clip`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`affine`  
数组，其中键为 0 至 5 的数字。

`clip`  
数组，其中键为 "x"，"y"，"width" 和 "height"。

### 返回值

成功则返回仿射变换后的图像， 或者在失败时返回 **`false`**.

imageaffinematrixconcat
=======================

Concatenate two affine transformation matrices

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">imageaffinematrixconcat</span> ( <span
class="methodparam"><span class="type">array</span> `$m1`</span> , <span
class="methodparam"><span class="type">array</span> `$m2`</span> )

Returns the concatenation of two affine transformation matrices, what is
useful if multiple transformations should be applied to the same image
in one go.

### 参数

`m1`  
An affine transformation matrix (an array with keys *0* to *5* and float
values).

`m2`  
An affine transformation matrix (an array with keys *0* to *5* and float
values).

### 返回值

An affine transformation matrix (an array with keys *0* to *5* and float
values) 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">imageaffinematrixconcat</span>
example**

``` php
<?php
$m1 = imageaffinematrixget(IMG_AFFINE_TRANSLATE, array('x' = 2, 'y' => 3));
$m2 = imageaffinematrixget(IMG_AFFINE_SCALE, array('x' = 4, 'y' => 5));
$matrix = imageaffinematrixconcat($m1, $m2);
print_r($matrix);
?>
```

以上例程会输出：

    Array
    (
        [0] => 4
        [1] => 0
        [2] => 0
        [3] => 5
        [4] => 8
        [5] => 15
    )

### 参见

-   <span class="function">imageaffine</span>
-   <span class="function">imageaffinematrixget</span>

imageaffinematrixget
====================

Get an affine transformation matrix

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">imageaffinematrixget</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$options`</span> \] )

Returns an affine transformation matrix.

### 参数

`type`  
One of the **`IMG_AFFINE_*`** constants.

`options`  
If `type` is **`IMG_AFFINE_TRANSLATE`** or **`IMG_AFFINE_SCALE`**,
`options` has to be an <span class="type">array</span> with keys *x* and
*y*, both having <span class="type">float</span> values.

If `type` is **`IMG_AFFINE_ROTATE`**, **`IMG_AFFINE_SHEAR_HORIZONTAL`**
or **`IMG_AFFINE_SHEAR_VERTICAL`**, `options` has to be a <span
class="type">float</span> specifying the angle.

### 返回值

An affine transformation matrix (an array with keys *0* to *5* and float
values) 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">imageaffinematrixget</span> example**

``` php
<?php
$matrix = imageaffinematrixget(IMG_AFFINE_TRANSLATE, array('x' = 2, 'y' => 3));
print_r($matrix);
?>
```

以上例程会输出：

    Array
    (
        [0] => 1
        [1] => 0
        [2] => 0
        [3] => 1
        [4] => 2
        [5] => 3
    )

### 参见

-   <span class="function">imageaffine</span>
-   <span class="function">imageaffinematrixconcat</span>

imagealphablending
==================

设定图像的混色模式

### 说明

<span class="type">bool</span> <span
class="methodname">imagealphablending</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$blendmode`</span> )

<span class="function">imagealphablending</span>
允许在真彩色图像上使用两种不同的绘画模式。在混色（blending）模式下，alpha
通道色彩成分提供给所有的绘画函数，例如 <span
class="function">imagesetpixel</span>
决定底层的颜色应在何种程度上被允许照射透过。作为结果，GD
自动将该点现有的颜色和画笔颜色混合，并将结果储存在图像中。结果的像素是不透明的。在非混色模式下，画笔颜色连同其
alpha
通道信息一起被拷贝，替换掉目标像素。混色模式在画调色板图像时不可用。如果
`blendmode` 为 **`true`**，则启用混色模式，否则关闭。成功时返回
**`true`**， 或者在失败时返回 **`false`**。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`blendmode`  
Whether to enable the blending mode or not. On true color images the
default value is **`true`** otherwise the default value is **`false`**

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagealphablending</span> usage
example**

``` php
<?php
// Create image
$im = imagecreatetruecolor(100, 100);

// Set alphablending to on
imagealphablending($im, true);

// Draw a square
imagefilledrectangle($im, 30, 30, 70, 70, imagecolorallocate($im, 255, 0, 0));

// Output
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### 注释

imageantialias
==============

是否使用抗锯齿（antialias）功能

### 说明

<span class="type">bool</span> <span
class="methodname">imageantialias</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$enabled`</span> )

对线段和多边形启用快速画图抗锯齿方法。不支持 alpha
部分。使用直接混色操作。仅用于真彩色图像。

不支持线宽和风格。

使用抗锯齿和透明背景色可能出现未预期的结果。混色方法把背景色当成任何其它颜色使用。缺乏
alpha 部分的支持导致不允许基于 alpha 抗锯齿方法。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`enabled`  
是否启用抗锯齿。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 A comparison of two lines, one with anti-aliasing switched
on**

``` php
<?php
// Setup an anti-aliased image and a normal image
$aa = imagecreatetruecolor(400, 100);
$normal = imagecreatetruecolor(200, 100);

// Switch antialiasing on for one image
imageantialias($aa, true);

// Allocate colors
$red = imagecolorallocate($normal, 255, 0, 0);
$red_aa = imagecolorallocate($aa, 255, 0, 0);

// Draw two lines, one with AA enabled
imageline($normal, 0, 0, 200, 100, $red);
imageline($aa, 0, 0, 200, 100, $red_aa);

// Merge the two images side by side for output (AA: left, Normal: Right)
imagecopymerge($aa, $normal, 200, 0, 0, 0, 200, 100, 100);

// Output image
header('Content-type: image/png');

imagepng($aa);
imagedestroy($aa);
imagedestroy($normal);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imageantialias.png" width="400" height="100" alt="Output of example : A comparison of two lines, one with anti-aliasing switched on" />

### 注释

### 参见

-   <span class="function">imagecreatetruecolor</span>

imagearc
========

画椭圆弧

### 说明

<span class="type">bool</span> <span class="methodname">imagearc</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> , <span class="methodparam"><span
class="type">int</span> `$cx`</span> , <span class="methodparam"><span
class="type">int</span> `$cy`</span> , <span class="methodparam"><span
class="type">int</span> `$w`</span> , <span class="methodparam"><span
class="type">int</span> `$h`</span> , <span class="methodparam"><span
class="type">int</span> `$s`</span> , <span class="methodparam"><span
class="type">int</span> `$e`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

<span class="function">imagearc</span> 以 `cx`，`cy`（图像左上角为 0,
0）为中心在 `image` 所代表的图像中画一个椭圆弧。`w` 和 `h`
分别指定了椭圆的宽度和高度，起始和结束点以 `s` 和 `e`
参数以角度指定。0°位于三点钟位置，以顺时针方向绘画。

**示例 \#1 用 <span class="function">imagearc</span> 画一个圆**

``` php
<?php
// 创建一个 200X200 的图像
$img = imagecreatetruecolor(200, 200);
// 分配颜色
$white = imagecolorallocate($img, 255, 255, 255);
$black = imagecolorallocate($img, 0, 0, 0);
// 画一个黑色的圆
imagearc($img, 100, 100, 150, 150, 0, 360, $black);
// 将图像输出到浏览器
header("Content-type: image/png");
imagepng($img);
// 释放内存
imagedestroy($img);
?>
```

参见 <span class="function">imageellipse</span>，<span
class="function">imagefilledellipse</span> 和 <span
class="function">imagefilledarc</span>。

imagebmp
========

Output a BMP image to browser or file

### 说明

<span class="type">bool</span> <span class="methodname">imagebmp</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$to`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$compressed`<span class="initializer"> =
**`true`**</span></span> \]\] )

Outputs or saves a BMP version of the given `image`.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`to`  
文件保存的路径，如果未设置或为 **`null`**，将会直接输出原始图象流。

> **Note**:
>
> **`null`** is invalid if the `compressed` arguments is not used.

`compressed`  
Whether the BMP should be compressed with run-length encoding (RLE), or
not.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

**Caution**

如果 libgd 输出图像失败，函数会返回 **`true`**。

### 范例

**示例 \#1 Saving a BMP file**

``` php
<?php
// Create a blank image and add some text
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);

imagestring($im, 1, 5, 5,  'BMP with PHP', $text_color);

// Save the image
imagebmp($im, 'php.bmp');

// Free up memory
imagedestroy($im);
?>
```

imagechar
=========

水平地画一个字符

### 说明

<span class="type">bool</span> <span class="methodname">imagechar</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> , <span class="methodparam"><span
class="type">int</span> `$font`</span> , <span class="methodparam"><span
class="type">int</span> `$x`</span> , <span class="methodparam"><span
class="type">int</span> `$y`</span> , <span class="methodparam"><span
class="type">string</span> `$c`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

<span class="function">imagechar</span> 将字符串 `c` 的第一个字符画在
`image` 指定的图像中，其左上角位于 `x`，`y`（图像左上角为 0, 0），颜色为
`color`。如果 `font` 是 1，2，3，4 或
5，则使用内置的字体（更大的数字对应于更大的字体）。

**示例 \#1 <span class="function">imagechar</span> 例子**

``` php
<?php

$im = imagecreate(100,100);

$string = 'PHP';

$bg = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// prints a black "P" in the top left corner
imagechar($im, 1, 0, 0, $string, $black);

header('Content-type: image/png');
imagepng($im);

?>
```

参见 <span class="function">imagecharup</span> 和 <span
class="function">imageloadfont</span>。

imagecharup
===========

垂直地画一个字符

### 说明

<span class="type">bool</span> <span
class="methodname">imagecharup</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">int</span> `$font`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">string</span> `$c`</span> , <span
class="methodparam"><span class="type">int</span> `$color`</span> )

<span class="function">imagecharup</span> 将字符 `c` 垂直地画在 `image`
指定的图像上，位于 `x`，`y`（图像左上角为 0, 0），颜色为 `color`。如果
`font` 为 1，2，3，4 或 5，则使用内置的字体。

**示例 \#1 <span class="function">imagecharup</span> 例子**

``` php
<?php

$im = imagecreate(100,100);

$string = 'Note that the first letter is a N';

$bg = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// prints a black "Z" on a white background
imagecharup($im, 3, 10, 10, $string, $black);

header('Content-type: image/png');
imagepng($im);

?>
```

参见 <span class="function">imagechar</span> 和 <span
class="function">imageloadfont</span>。

imagecolorallocate
==================

为一幅图像分配颜色

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorallocate</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
)

<span class="function">imagecolorallocate</span>
返回一个标识符，代表了由给定的 RGB 成分组成的颜色。`red`，`green` 和
`blue` 分别是所需要的颜色的红，绿，蓝成分。这些参数是 0 到 255
的整数或者十六进制的 0x00 到 0xFF。<span
class="function">imagecolorallocate</span> 必须被调用以创建每一种用在
`image` 所代表的图像中的颜色。

> **Note**:
>
> 第一次对 <span class="function">imagecolorallocate</span>
> 的调用会给基于调色板的图像填充背景色，即用 <span
> class="function">imagecreate</span> 建立的图像。

**示例 \#1 <span class="function">imagecolorallocate</span> 例子**

``` php
<?php
$im = imagecreate('example.jpg', 100, 100);
// 背景设为红色
$background = imagecolorallocate($im, 255, 0, 0);
// 设定一些颜色
$white = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);
// 十六进制方式
$white = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);
$black = imagecolorallocate($im, 0x00, 0x00, 0x00);
?>
```

如果分配失败则返回 -1。

参见 <span class="function">imagecolorallocatealpha</span> 和 <span
class="function">imagecolordeallocate</span>。

imagecolorallocatealpha
=======================

为一幅图像分配颜色 + alpha

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorallocatealpha</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
, <span class="methodparam"><span class="type">int</span>
`$alpha`</span> )

<span class="function">imagecolorallocatealpha</span> 的行为和 <span
class="function">imagecolorallocate</span>
相同，但多了一个额外的透明度参数 `alpha`，其值从 *0* 到 *127*。*0*
表示完全不透明，*127* 表示完全透明。

如果分配失败则返回 **`false`**。

**示例 \#1 使用 <span class="function">imagecolorallocatealpha</span>
的例子**

``` php
<?php
$size = 300;
$image=imagecreatetruecolor($size, $size);

// 用白色背景加黑色边框画个方框
$back = imagecolorallocate($image, 255, 255, 255);
$border = imagecolorallocate($image, 0, 0, 0);
imagefilledrectangle($image, 0, 0, $size - 1, $size - 1, $back);
imagerectangle($image, 0, 0, $size - 1, $size - 1, $border);

$yellow_x = 100;
$yellow_y = 75;
$red_x    = 120;
$red_y    = 165;
$blue_x   = 187;
$blue_y   = 125;
$radius   = 150;

// 用 alpha 值分配一些颜色
$yellow = imagecolorallocatealpha($image, 255, 255, 0, 75);
$red    = imagecolorallocatealpha($image, 255, 0, 0, 75);
$blue   = imagecolorallocatealpha($image, 0, 0, 255, 75);

// 画三个交迭的圆
imagefilledellipse($image, $yellow_x, $yellow_y, $radius, $radius, $yellow);
imagefilledellipse($image, $red_x, $red_y, $radius, $radius, $red);
imagefilledellipse($image, $blue_x, $blue_y, $radius, $radius, $blue);

// 不要忘记输出正确的 header！
header('Content-type: image/png');

// 最后输出结果
imagepng($image);
imagedestroy($image);
?>
```

参见 <span class="function">imagecolorallocate</span> 和 <span
class="function">imagecolordeallocate</span>。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`red`  
红色成分的值。

`green`  
绿色成分的值。

`blue`  
蓝色成分的值。

`alpha`  
A value between *0* and *127*. *0* indicates completely opaque while
*127* indicates completely transparent.

The colors parameters are integers between 0 and 255 or hexadecimals
between 0x00 and 0xFF.

### 返回值

A color identifier or **`false`** if the allocation failed.

**Warning**

此函数可能返回布尔值 **`false`**，但也可能返回等同于 **`false`**
的非布尔值。请阅读
<a href="/language/types/boolean.html" class="link">布尔类型</a>章节以获取更多信息。应使用
<a href="/language/operators/comparison.html" class="link">=== 运算符</a>来测试此函数的返回值。

### 更新日志

| 版本           | 说明                                 |
|----------------|--------------------------------------|
| Prior to 5.1.3 | Returns -1 if the allocation failed. |

### 范例

**示例 \#2 Example of using <span
class="function">imagecolorallocatealpha</span>**

``` php
<?php
$size = 300;
$image=imagecreatetruecolor($size, $size);

// something to get a white background with black border
$back = imagecolorallocate($image, 255, 255, 255);
$border = imagecolorallocate($image, 0, 0, 0);
imagefilledrectangle($image, 0, 0, $size - 1, $size - 1, $back);
imagerectangle($image, 0, 0, $size - 1, $size - 1, $border);

$yellow_x = 100;
$yellow_y = 75;
$red_x    = 120;
$red_y    = 165;
$blue_x   = 187;
$blue_y   = 125;
$radius   = 150;

// allocate colors with alpha values
$yellow = imagecolorallocatealpha($image, 255, 255, 0, 75);
$red    = imagecolorallocatealpha($image, 255, 0, 0, 75);
$blue   = imagecolorallocatealpha($image, 0, 0, 255, 75);

// drawing 3 overlapped circle
imagefilledellipse($image, $yellow_x, $yellow_y, $radius, $radius, $yellow);
imagefilledellipse($image, $red_x, $red_y, $radius, $radius, $red);
imagefilledellipse($image, $blue_x, $blue_y, $radius, $radius, $blue);

// don't forget to output a correct header!
header('Content-Type: image/png');

// and finally, output the result
imagepng($image);
imagedestroy($image);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecolorallocatealpha.png" width="300" height="300" alt="Output of example : Example of using imagecolorallocatealpha()" />

### 注释

### 参见

-   <span class="function">imagecolorallocate</span>
-   <span class="function">imagecolordeallocate</span>

imagecolorat
============

取得某像素的颜色索引值

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorat</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$y`</span> )

返回 `image` 所指定的图形中指定位置像素的颜色索引值。

如果 PHP 编译时加上了 GD 库 2.0
或更高的版本并且图像是真彩色图像，则本函数以整数返回该点的 RGB
值。用移位加掩码来取得红，绿，蓝各自成分的值：

**示例 \#1 取得各自的 RGB 值**

``` php
<?php
$im = ImageCreateFromPng("rockym.png");
$rgb = ImageColorAt($im, 100, 100);
$r = ($rgb >> 16) & 0xFF;
$g = ($rgb >> 8) & 0xFF;
$b = $rgb & 0xFF;
?>
```

参见 <span class="function">imagecolorset</span> 和 <span
class="function">imagecolorsforindex</span>。

imagecolorclosest
=================

取得与指定的颜色最接近的颜色的索引值

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorclosest</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
)

返回图像调色板中与指定的 RGB 值最“接近”的颜色。

指定的颜色与调色板中的每个颜色的“距离”的计算方法是把 RGB
值当成三维空间中点的坐标。

如果从文件创建了图像，只有图像中使用了的颜色会被辨析。仅出现在调色板中的颜色不会被辨析。

参见 <span class="function">imagecolorexact</span>。

imagecolorclosestalpha
======================

取得与指定的颜色加透明度最接近的颜色

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorclosestalpha</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
, <span class="methodparam"><span class="type">int</span>
`$alpha`</span> )

返回图像调色板中与指定的 RGB 值以及 `alpha` 深度最“接近”的颜色。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`red`  
红色成分的值。

`green`  
绿色成分的值。

`blue`  
蓝色成分的值。

`alpha`  
A value between *0* and *127*. *0* indicates completely opaque while
*127* indicates completely transparent.

The colors parameters are integers between 0 and 255 or hexadecimals
between 0x00 and 0xFF.

### 返回值

Returns the index of the closest color in the palette.

### 范例

**示例 \#1 Search for a set of colors in an image**

``` php
<?php
// Start with an image and convert it to a palette-based image
$im = imagecreatefrompng('figures/imagecolorclosest.png');
imagetruecolortopalette($im, false, 255);

// Search colors (RGB)
$colors = array(
    array(254, 145, 154, 50),
    array(153, 145, 188, 127),
    array(153, 90, 145, 0),
    array(255, 137, 92, 84)
);

// Loop through each search and find the closest color in the palette.
// Return the search number, the search RGB and the converted RGB match
foreach($colors as $id => $rgb)
{
    $result = imagecolorclosestalpha($im, $rgb[0], $rgb[1], $rgb[2], $rgb[3]);
    $result = imagecolorsforindex($im, $result);
    $result = "({$result['red']}, {$result['green']}, {$result['blue']}, {$result['alpha']})";

    echo "#$id: Search ($rgb[0], $rgb[1], $rgb[2], $rgb[3]); Closest match: $result.\n";
}

imagedestroy($im);
?>
```

以上例程的输出类似于：

    #0: Search (254, 145, 154, 50); Closest match: (252, 150, 148, 0).
    #1: Search (153, 145, 188, 127); Closest match: (148, 150, 196, 0).
    #2: Search (153, 90, 145, 0); Closest match: (148, 90, 156, 0).
    #3: Search (255, 137, 92, 84); Closest match: (252, 150, 92, 0).

### 注释

### 参见

-   <span class="function">imagecolorexactalpha</span>
-   <span class="function">imagecolorclosest</span>
-   <span class="function">imagecolorclosesthwb</span>

imagecolorclosesthwb
====================

取得与给定颜色最接近的色度的黑白色的索引

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorclosesthwb</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
)

取得与给定颜色最接近的色度的黑白色的索引。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`red`  
红色成分的值。

`green`  
绿色成分的值。

`blue`  
蓝色成分的值。

### 返回值

返回一个整数，是给定颜色最接近的色度的黑白色的索引。

### 范例

**示例 \#1 使用 <span class="function">imagecolorclosesthwb</span>
的例子**

``` php
<?php
$im = imagecreatefromgif('php.gif');

echo 'HWB: ' . imagecolorclosesthwb($im, 116, 115, 152);

imagedestroy($im);
?>
```

以上例程的输出类似于：

    HWB: 33

### 更新日志

| 版本  | 说明                  |
|-------|-----------------------|
| 5.3.0 | 在 Windows 平台上可用 |

### 参见

-   <span class="function">imagecolorclosest</span>

imagecolordeallocate
====================

取消图像颜色的分配

### 说明

<span class="type">bool</span> <span
class="methodname">imagecolordeallocate</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$color`</span>
)

<span class="function">imagecolordeallocate</span> 函数取消先前由 <span
class="function">imagecolorallocate</span> 或 <span
class="function">imagecolorallocatealpha</span> 分配的颜色。

``` php
<?php
$white = imagecolorallocate($im, 255, 255, 255);
imagecolordeallocate($im, $white);
?>
```

参见 <span class="function">imagecolorallocate</span> 和 <span
class="function">imagecolorallocatealpha</span>。

imagecolorexact
===============

取得指定颜色的索引值

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorexact</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
)

返回图像调色板中指定颜色的索引值。

如果颜色不在图像的调色板中，返回 -1。

如果从文件创建了图像，只有图像中使用了的颜色会被辨析。仅出现在调色板中的颜色不会被辨析。

参见 <span class="function">imagecolorclosest</span>。

imagecolorexactalpha
====================

取得指定的颜色加透明度的索引值

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorexactalpha</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
, <span class="methodparam"><span class="type">int</span>
`$alpha`</span> )

返回图像调色板中指定颜色加透明度的索引值。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`red`  
红色成分的值。

`green`  
绿色成分的值。

`blue`  
蓝色成分的值。

`alpha`  
A value between *0* and *127*. *0* indicates completely opaque while
*127* indicates completely transparent.

The colors parameters are integers between 0 and 255 or hexadecimals
between 0x00 and 0xFF.

### 返回值

返回图像调色板中指定颜色加透明度的索引值。
如果颜色不在图像的调色板中，返回 -1。

### 范例

**示例 \#1 Get colors from the GD logo**

``` php
<?php

// Setup an image
$im = imagecreatefrompng('./gdlogo.png');

$colors   = Array();
$colors[] = imagecolorexactalpha($im, 255, 0, 0, 0);
$colors[] = imagecolorexactalpha($im, 0, 0, 0, 127);
$colors[] = imagecolorexactalpha($im, 255, 255, 255, 55);
$colors[] = imagecolorexactalpha($im, 100, 255, 52, 20);

print_r($colors);

// Free from memory
imagedestroy($im);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => 16711680
        [1] => 2130706432
        [2] => 939524095
        [3] => 342163252
    )

### 注释

### 参见

-   <span class="function">imagecolorclosestalpha</span>

imagecolormatch
===============

使一个图像中调色板版本的颜色与真彩色版本更能匹配

### 说明

<span class="type">bool</span> <span
class="methodname">imagecolormatch</span> ( <span
class="methodparam"><span class="type">resource</span> `$image1`</span>
, <span class="methodparam"><span class="type">resource</span>
`$image2`</span> )

使一个图像中调色板版本的颜色与真彩色版本更能匹配。

### 参数

`image1`  
真彩色图像连接资源。

`image2`  
必须是调色板图像，而且和 `image1` 的大小必须相同。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagecolormatch</span> 例子**

``` php
<?php
// Setup the true color and palette images
$im1 = imagecreatefrompng('./gdlogo.png');
$im2 = imagecreate(imagesx($im1), imagesy($im1));

// Add some colors to $im2
$colors   = Array();
$colors[] = imagecolorallocate($im2, 255, 36, 74);
$colors[] = imagecolorallocate($im2, 40, 0, 240);
$colors[] = imagecolorallocate($im2, 82, 100, 255);
$colors[] = imagecolorallocate($im2, 84, 63, 44);

// Match these colors with the true color image
imagecolormatch($im1, $im2);

// Free from memory
imagedestroy($im1);
imagedestroy($im2);
?>
```

### 注释

### 参见

-   <span class="function">imagecreatetruecolor</span>

imagecolorresolve
=================

取得指定颜色的索引值或有可能得到的最接近的替代值

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorresolve</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
)

本函数可以保证对所请求的颜色返回一个颜色索引，要么是确切值要么是所能得到最接近的替代值。

如果从文件创建了图像，只有图像中使用了的颜色会被辨析。仅出现在调色板中的颜色不会被辨析。

参见 <span class="function">imagecolorclosest</span>。

imagecolorresolvealpha
======================

取得指定颜色 + alpha 的索引值或有可能得到的最接近的替代值

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorresolvealpha</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
, <span class="methodparam"><span class="type">int</span>
`$alpha`</span> )

本函数可以保证对所请求的颜色返回一个颜色索引，要么是确切值要么是所能得到最接近的替代值。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`red`  
红色成分的值。

`green`  
绿色成分的值。

`blue`  
蓝色成分的值。

`alpha`  
A value between *0* and *127*. *0* indicates completely opaque while
*127* indicates completely transparent.

The colors parameters are integers between 0 and 255 or hexadecimals
between 0x00 and 0xFF.

### 返回值

Returns a color index.

### 范例

**示例 \#1 Using <span class="function">imagecoloresolvealpha</span> to
get colors from an image**

``` php
<?php
// Load an image
$im = imagecreatefromgif('phplogo.gif');

// Get closest colors from the image
$colors = array();
$colors[] = imagecolorresolvealpha($im, 255, 255, 255, 0);
$colors[] = imagecolorresolvealpha($im, 0, 0, 200, 127);

// Output
print_r($colors);

imagedestroy($im);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => 89
        [1] => 85
    )

### 注释

### 参见

-   <span class="function">imagecolorclosestalpha</span>

imagecolorset
=============

给指定调色板索引设定颜色

### 说明

<span class="type">void</span> <span
class="methodname">imagecolorset</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$index`</span>
, <span class="methodparam"><span class="type">int</span> `$red`</span>
, <span class="methodparam"><span class="type">int</span>
`$green`</span> , <span class="methodparam"><span
class="type">int</span> `$blue`</span> )

本函数将调色板中指定的索引设定为指定的颜色。对于在调色板图像中创建类似区域填充（flood-fill）的效果很有用，免去了真的去填充的开销。

参见 <span class="function">imagecolorat</span>。

imagecolorsforindex
===================

取得某索引的颜色

### 说明

<span class="type">array</span> <span
class="methodname">imagecolorsforindex</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

本函数返回一个具有 red，green，blue 和 alpha
的键名的关联数组，包含了指定颜色索引的相应的值。

**示例 \#1 <span class="function">imagecolorsforindex</span> 例子**

``` php
<?php

// 打开一幅图像
$im = imagecreatefrompng('nexen.png');

// 取得一点的颜色
$start_x = 40;
$start_y = 50;
$color_index = imagecolorat($im, $start_x, $start_y);

// 使其可读
$color_tran = imagecolorsforindex($im, $color_index);

// 显示该颜色的值
echo '<pre>';
print_r($color_tran);
echo '</pre>';

?>
```

本例将输出：

    Array
    (
        [red] => 226
        [green] => 222
        [blue] => 252
        [alpha] => 0
    )

参见 <span class="function">imagecolorat</span> 和 <span
class="function">imagecolorexact</span>。

imagecolorstotal
================

取得一幅图像的调色板中颜色的数目

### 说明

<span class="type">int</span> <span
class="methodname">imagecolorstotal</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> )

本函数返回指定图像的调色板中的颜色数目。

参见 <span class="function">imagecolorat</span> 和 <span
class="function">imagecolorsforindex</span>。

imagecolortransparent
=====================

将某个颜色定义为透明色

### 说明

<span class="type">int</span> <span
class="methodname">imagecolortransparent</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$color`</span> \] )

<span class="function">imagecolortransparent</span> 将 `image`
图像中的透明色设定为 `color`。`image` 是 <span
class="function">imagecreatetruecolor</span> 返回的图像标识符，`color`
是 <span class="function">imagecolorallocate</span> 返回的颜色标识符。

> **Note**:
>
> 透明色是图像的一种属性，透明度不是颜色的属性。一旦设定了某个颜色为透明色，图像中之前画为该色的任何区域都成为透明的。

返回新透明色的标识符，如果省略 `color` 则返回当前透明色的标识符。

> **Note**:
>
> 透明度仅能通过 <span class="function">imagecopymerge</span>
> 和真彩色图像拷贝，不能用 <span class="function">imagecopy</span>
> 或调色板图像。

imageconvolution
================

用系数 div 和 offset 申请一个 3x3 的卷积矩阵

### 说明

<span class="type">bool</span> <span
class="methodname">imageconvolution</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">array</span>
`$matrix`</span> , <span class="methodparam"><span
class="type">float</span> `$div`</span> , <span
class="methodparam"><span class="type">float</span> `$offset`</span> )

Applies a convolution matrix on the image, using the given coefficient
and offset.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`matrix`  
A 3x3 matrix: an array of three arrays of three floats.

`div`  
The divisor of the result of the convolution, used for normalization.

`offset`  
Color offset.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Embossing the PHP.net logo**

``` php
<?php
$image = imagecreatefromgif('http://www.php.net/images/php.gif');

$emboss = array(array(2, 0, 0), array(0, -1, 0), array(0, 0, -1));
imageconvolution($image, $emboss, 1, 127);

header('Content-Type: image/png');
imagepng($image, null, 9);
?>
```

以上例程会输出：

<img src="images/21009b70229598c6a80eef8b45bf282b-imageconvolution_emboss.png" width="120" height="67" alt="Output of example : Embossing the PHP.net logo" />

**示例 \#2 Gaussian blur**

``` php
<?php
$image = imagecreatetruecolor(180,40);

// Writes the text and apply a gaussian blur on the image
imagestring($image, 5, 10, 8, 'Gaussian Blur Text', 0x00ff00);
$gaussian = array(array(1.0, 2.0, 1.0), array(2.0, 4.0, 2.0), array(1.0, 2.0, 1.0));
imageconvolution($image, $gaussian, 16, 0);

// Rewrites the text for comparison
imagestring($image, 5, 10, 18, 'Gaussian Blur Text', 0x00ff00);

header('Content-Type: image/png');
imagepng($image, null, 9);
?>
```

以上例程会输出：

<img src="images/21009b70229598c6a80eef8b45bf282b-imageconvolution_gaussian.png" width="180" height="40" alt="Output of example : Gaussian blur" />

### 注释

### 参见

-   <span class="function">imagefilter</span>

imagecopy
=========

拷贝图像的一部分

### 说明

<span class="type">bool</span> <span class="methodname">imagecopy</span>
( <span class="methodparam"><span class="type">resource</span>
`$dst_im`</span> , <span class="methodparam"><span
class="type">resource</span> `$src_im`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_x`</span> ,
<span class="methodparam"><span class="type">int</span> `$dst_y`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_x`</span> , <span class="methodparam"><span
class="type">int</span> `$src_y`</span> , <span
class="methodparam"><span class="type">int</span> `$src_w`</span> ,
<span class="methodparam"><span class="type">int</span> `$src_h`</span>
)

将 `src_im` 图像中坐标从 `src_x`，`src_y ` 开始，宽度为 `src_w`，高度为
`src_h` 的一部分拷贝到 `dst_im` 图像中坐标为 `dst_x` 和 `dst_y`
的位置上。

imagecopymerge
==============

拷贝并合并图像的一部分

### 说明

<span class="type">bool</span> <span
class="methodname">imagecopymerge</span> ( <span
class="methodparam"><span class="type">resource</span> `$dst_im`</span>
, <span class="methodparam"><span class="type">resource</span>
`$src_im`</span> , <span class="methodparam"><span
class="type">int</span> `$dst_x`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_y`</span> ,
<span class="methodparam"><span class="type">int</span> `$src_x`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_y`</span> , <span class="methodparam"><span
class="type">int</span> `$src_w`</span> , <span
class="methodparam"><span class="type">int</span> `$src_h`</span> ,
<span class="methodparam"><span class="type">int</span> `$pct`</span> )

将 `src_im` 图像中坐标从 `src_x`，`src_y ` 开始，宽度为 `src_w`，高度为
`src_h` 的一部分拷贝到 `dst_im` 图像中坐标为 `dst_x` 和 `dst_y`
的位置上。两图像将根据 `pct` 来决定合并程度，其值范围从 0 到 100。当
`pct` = 0 时，实际上什么也没做，当为 100 时对于调色板图像本函数和 <span
class="function">imagecopy</span> 完全一样，它对真彩色图像实现了 alpha
透明。

> **Note**:
>
> 本函数是 PHP 4.0.6 新加的。

imagecopymergegray
==================

用灰度拷贝并合并图像的一部分

### 说明

<span class="type">bool</span> <span
class="methodname">imagecopymergegray</span> ( <span
class="methodparam"><span class="type">resource</span> `$dst_im`</span>
, <span class="methodparam"><span class="type">resource</span>
`$src_im`</span> , <span class="methodparam"><span
class="type">int</span> `$dst_x`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_y`</span> ,
<span class="methodparam"><span class="type">int</span> `$src_x`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_y`</span> , <span class="methodparam"><span
class="type">int</span> `$src_w`</span> , <span
class="methodparam"><span class="type">int</span> `$src_h`</span> ,
<span class="methodparam"><span class="type">int</span> `$pct`</span> )

将 `src_im` 图像中坐标从 `src_x`，`src_y ` 开始，宽度为 `src_w`，高度为
`src_h` 的一部分拷贝到 `dst_im` 图像中坐标为 `dst_x` 和 `dst_y`
的位置上。两图像将根据 `pct` 来决定合并程度，其值范围从 0 到 100。当
`pct` = 0 时，实际上什么也没做，当为 100 时本函数和 <span
class="function">imagecopy</span> 完全一样。

本函数和 <span class="function">imagecopymerge</span>
完全一样只除了合并时通过在拷贝操作前将目标像素转换为灰度级来保留了原色度。

> **Note**:
>
> 本函数添加于 PHP 4.0.6。

imagecopyresampled
==================

重采样拷贝部分图像并调整大小

### 说明

<span class="type">bool</span> <span
class="methodname">imagecopyresampled</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dst_image`</span> , <span class="methodparam"><span
class="type">resource</span> `$src_image`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_x`</span> ,
<span class="methodparam"><span class="type">int</span> `$dst_y`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_x`</span> , <span class="methodparam"><span
class="type">int</span> `$src_y`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_w`</span> ,
<span class="methodparam"><span class="type">int</span> `$dst_h`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_w`</span> , <span class="methodparam"><span
class="type">int</span> `$src_h`</span> )

<span class="function">imagecopyresampled</span>
将一幅图像中的一块正方形区域拷贝到另一个图像中，平滑地插入像素值，因此，尤其是，减小了图像的大小而仍然保持了极大的清晰度。

In other words, <span class="function">imagecopyresampled</span> will
take a rectangular area from `src_image` of width `src_w` and height
`src_h` at position (`src_x`,`src_y`) and place it in a rectangular area
of `dst_image` of width `dst_w` and height `dst_h` at position
(`dst_x`,`dst_y`).

如果源和目标的宽度和高度不同，则会进行相应的图像收缩和拉伸。坐标指的是左上角。本函数可用来在同一幅图内部拷贝（如果
`dst_image` 和 `src_image`
相同的话）区域，但如果区域交迭的话则结果不可预知。

### 参数

`dst_image`  
目标图象资源。

`src_image`  
源图象资源。

`dst_x`  
目标 X 坐标点。

`dst_y`  
目标 Y 坐标点。

`src_x`  
源的 X 坐标点。

`src_y`  
源的 Y 坐标点。

`dst_w`  
目标宽度。

`dst_h`  
目标高度。

`src_w`  
源图象的宽度。

`src_h`  
源图象的高度。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 简单的例子**

这个例子会将图像调整为原有尺寸的一半。

``` php
<?php
// 这个文件
$filename = 'test.jpg';
$percent = 0.5;

// 内容类型
header('Content-Type: image/jpeg');

// 获取新的尺寸
list($width, $height) = getimagesize($filename);
$new_width = $width * $percent;
$new_height = $height * $percent;

// 重新取样
$image_p = imagecreatetruecolor($new_width, $new_height);
$image = imagecreatefromjpeg($filename);
imagecopyresampled($image_p, $image, 0, 0, 0, 0, $new_width, $new_height, $width, $height);

// 输出
imagejpeg($image_p, null, 100);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecopyresampled.jpg" width="47" height="25" alt="输出的例子：简单的例子" />

**示例 \#2 按比例对图像重新采样**

这个例子会以最大宽度高度为 200 像素显示一个图像。

``` php
<?php
// 源文件
$filename = 'test.jpg';

// 设置最大宽高
$width = 200;
$height = 200;

// Content type
header('Content-Type: image/jpeg');

// 获取新尺寸
list($width_orig, $height_orig) = getimagesize($filename);

$ratio_orig = $width_orig/$height_orig;

if ($width/$height > $ratio_orig) {
   $width = $height*$ratio_orig;
} else {
   $height = $width/$ratio_orig;
}

// 重新取样
$image_p = imagecreatetruecolor($width, $height);
$image = imagecreatefromjpeg($filename);
imagecopyresampled($image_p, $image, 0, 0, 0, 0, $width, $height, $width_orig, $height_orig);

// 输出
imagejpeg($image_p, null, 100);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecopyresampled_2.jpg" width="200" height="107" alt="输出例子：按比例对图像重新采样" />

### 注释

> **Note**:
>
> 因为调色板图像限制（255+1
> 种颜色）有个问题。重采样或过滤图像通常需要多于 255
> 种颜色，计算新的被重采样的像素及其颜色时采用了一种近似值。对调色板图像尝试分配一个新颜色时，如果失败我们选择了计算结果最接近（理论上）的颜色。这并不总是视觉上最接近的颜色。这可能会产生怪异的结果，例如空白（或者视觉上是空白）的图像。要跳过这个问题，请使用真彩色图像作为目标图像，例如用
> <span class="function">imagecreatetruecolor</span> 创建的。

### 参见

<span class="function">imagecopyresized</span>

imagecopyresized
================

拷贝部分图像并调整大小

### 说明

<span class="type">bool</span> <span
class="methodname">imagecopyresized</span> ( <span
class="methodparam"><span class="type">resource</span>
`$dst_image`</span> , <span class="methodparam"><span
class="type">resource</span> `$src_image`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_x`</span> ,
<span class="methodparam"><span class="type">int</span> `$dst_y`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_x`</span> , <span class="methodparam"><span
class="type">int</span> `$src_y`</span> , <span
class="methodparam"><span class="type">int</span> `$dst_w`</span> ,
<span class="methodparam"><span class="type">int</span> `$dst_h`</span>
, <span class="methodparam"><span class="type">int</span>
`$src_w`</span> , <span class="methodparam"><span
class="type">int</span> `$src_h`</span> )

<span class="function">imagecopyresized</span>
将一幅图像中的一块矩形区域拷贝到另一个图像中。`dst_image` 和 `src_image`
分别是目标图像和源图像的标识符。

In other words, <span class="function">imagecopyresized</span> will take
an rectangular area from `src_image` of width `src_w` and height `src_h`
at position (`src_x`,`src_y`) and place it in a rectangular area of
`dst_image` of width `dst_w` and height `dst_h` at position
(`dst_x`,`dst_y`).

如果源和目标的宽度和高度不同，则会进行相应的图像收缩和拉伸。坐标指的是左上角。本函数可用来在同一幅图内部拷贝（如果
`dst_image` 和 `src_image`
相同的话）区域，但如果区域交迭的话则结果不可预知。

### 参数

`dst_image`  
目标图象资源。

`src_image`  
源图象资源。

`dst_x`  
x-coordinate of destination point.

`dst_y`  
y-coordinate of destination point.

`src_x`  
x-coordinate of source point.

`src_y`  
y-coordinate of source point.

`dst_w`  
Destination width.

`dst_h`  
Destination height.

`src_w`  
源图象的宽度。

`src_h`  
源图象的高度。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Resizing an image**

这个例子会以一半的尺寸显示图片

``` php
<?php
// File and new size
$filename = 'test.jpg';
$percent = 0.5;

// Content type
header('Content-Type: image/jpeg');

// Get new sizes
list($width, $height) = getimagesize($filename);
$newwidth = $width * $percent;
$newheight = $height * $percent;

// Load
$thumb = imagecreatetruecolor($newwidth, $newheight);
$source = imagecreatefromjpeg($filename);

// Resize
imagecopyresized($thumb, $source, 0, 0, 0, 0, $newwidth, $newheight, $width, $height);

// Output
imagejpeg($thumb);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecopyresized.jpg" width="47" height="25" alt="Output of example : Resizing an image" />

The image will be output at half size, though better quality could be
obtained using <span class="function">imagecopyresampled</span>.

### 注释

> **Note**:
>
> 因为调色板图像限制（255+1
> 种颜色）有个问题。重采样或过滤图像通常需要多于 255
> 种颜色，计算新的被重采样的像素及其颜色时采用了一种近似值。对调色板图像尝试分配一个新颜色时，如果失败我们选择了计算结果最接近（理论上）的颜色。这并不总是视觉上最接近的颜色。这可能会产生怪异的结果，例如空白（或者视觉上是空白）的图像。要跳过这个问题，请使用真彩色图像作为目标图像，例如用
> <span class="function">imagecreatetruecolor</span> 创建的。

### 参见

<span class="function">imagecopyresampled</span>

imagecreate
===========

新建一个基于调色板的图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreate</span> ( <span class="methodparam"><span
class="type">int</span> `$x_size`</span> , <span
class="methodparam"><span class="type">int</span> `$y_size`</span> )

<span class="function">imagecreate</span>
返回一个图像标识符，代表了一幅大小为 `x_size` 和 `y_size` 的空白图像。

推荐使用 <span class="function">imagecreatetruecolor</span>。

**示例 \#1 新建一个新的 GD 图像流并输出图像**

``` php
<?php
header("Content-type: image/png");
$im = @imagecreate(100, 50)
    or die("Cannot Initialize new GD image stream");
$background_color = imagecolorallocate($im, 255, 255, 255);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  "A Simple Text String", $text_color);
imagepng($im);
imagedestroy($im);
?>
```

参见 <span class="function">imagedestroy</span> 和 <span
class="function">imagecreatetruecolor</span>。

imagecreatefrombmp
==================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefrombmp</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefrombmp</span> returns an image
identifier representing the image obtained from the given filename.

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
Path to the BMP image.

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 Convert an BMP image to a PNG image using <span
class="function">imagecreatefrombmp</span>**

``` php
<?php
// Load the BMP file
$im = imagecreatefrombmp('./example.bmp');

// Convert it to a PNG file with default settings
imagepng($im, './example.png');
imagedestroy($im);
?>
```

imagecreatefromgd2
==================

从 GD2 文件或 URL 新建一图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromgd2</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

从 GD2 文件或 URL 新建一图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
GD2 图像的路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagecreatefromgd2</span> 例子**

``` php
<?php
// 加载 gd2 图像
$im = imagecreatefromgd2('./test.gd2');


// 在图像上应用效果。
// 在这个例子中，如果版本为 PHP5+ 则反转图像颜色
if(function_exists('imagefilter'))
{
    imagefilter($im, IMG_FILTER_NEGATE);
}

// 保存图像
imagegd2($im, './test_updated.gd2');
imagedestroy($im);
?>
```

### 注释

imagecreatefromgd2part
======================

从给定的 GD2 文件或 URL 中的部分新建一图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromgd2part</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">int</span> `$srcX`</span>
, <span class="methodparam"><span class="type">int</span> `$srcY`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> , <span class="methodparam"><span
class="type">int</span> `$height`</span> )

Create a new image from a given part of GD2 file or URL.

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
Path to the GD2 image.

`srcX`  
x-coordinate of source point.

`srcY`  
y-coordinate of source point.

`width`  
源图象的宽度。

`height`  
源图象的高度。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagecreatefromgd2part</span>
example**

``` php
<?php
// For this example we need the image size before
$image = getimagesize('./test.gd2');

// Create the image instance now we got the image 
// sizes
$im = imagecreatefromgd2part('./test.gd2', 4, 4, ($image[0] / 2) - 6, ($image[1] / 2) - 6);

// Do an image operation, in this case we emboss the 
// image if PHP 5+
if(function_exists('imagefilter'))
{
    imagefilter($im, IMG_FILTER_EMBOSS);
}

// Save optimized image
imagegd2($im, './test_emboss.gd2');
imagedestroy($im);
?>
```

### 注释

imagecreatefromgd
=================

从 GD 文件或 URL 新建一图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromgd</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

从 GD 文件或 URL 新建一图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
GD 文件的路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagecreatefromgd</span> 例子**

``` php
<?php
// Load the gd image
$im = @imagecreatefromgd('./test.gd');

// Test if the image was loaded
if(!is_resource($im))
{
     die('Unable to load gd image!');
}

// Do image operations here

// Save the image
imagegd($im, './test_updated.gd');
imagedestroy($im);
?>
```

### 注释

imagecreatefromgif
==================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromgif</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefromgif</span>
返回一图像标识符，代表了从给定的文件名取得的图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
GIF 图像的路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 处理创建过程中的错误**

``` php
<?php
function LoadGif($imgname)
{
    /* Attempt to open */
    $im = @imagecreatefromgif($imgname);

    /* See if it failed */
    if(!$im)
    {
        /* Create a blank image */
        $im = imagecreatetruecolor (150, 30);
        $bgc = imagecolorallocate ($im, 255, 255, 255);
        $tc = imagecolorallocate ($im, 0, 0, 0);

        imagefilledrectangle ($im, 0, 0, 150, 30, $bgc);

        /* Output an error message */
        imagestring ($im, 1, 5, 5, 'Error loading ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/gif');

$img = LoadGif('bogus.image');

imagegif($img);
imagedestroy($img);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecreatefromgif.gif" width="150" height="30" alt="例子的输出： 处理创建 GIF 过程中的错误" />

### 注释

> **Note**:
>
> 自 GD 库 1.6 版起所有的 GIF 支持都移除了，又在 GD 库 2.0.28
> 版起又加了回来。如果使用二者之间版本的 GD 库时本函数不可用。

imagecreatefromjpeg
===================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromjpeg</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefromjpeg</span>
返回一图像标识符，代表了从给定的文件名取得的图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
JPEG 图像的路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 处理创建过程中的错误**

``` php
<?php
function LoadJpeg($imgname)
{
    /* 尝试打开 */
    $im = @imagecreatefromjpeg($imgname);

    /* See if it failed */
    if(!$im)
    {
        /* Create a black image */
        $im  = imagecreatetruecolor(150, 30);
        $bgc = imagecolorallocate($im, 255, 255, 255);
        $tc  = imagecolorallocate($im, 0, 0, 0);

        imagefilledrectangle($im, 0, 0, 150, 30, $bgc);

        /* Output an error message */
        imagestring($im, 1, 5, 5, 'Error loading ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/jpeg');

$img = LoadJpeg('bogus.image');

imagejpeg($img);
imagedestroy($img);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecreatefromjpeg.jpg" width="150" height="30" alt="例子输出：加载图片出现错误时的处理范例" />

### 注释

imagecreatefrompng
==================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefrompng</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefrompng</span>
返回一图像标识符，代表了从给定的文件名取得的图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
PNG 图像的路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 处理创建 PNG 过程中的错误**

``` php
<?php
function LoadPNG($imgname)
{
    /* Attempt to open */
    $im = @imagecreatefrompng($imgname);

    /* See if it failed */
    if(!$im)
    {
        /* Create a blank image */
        $im  = imagecreatetruecolor(150, 30);
        $bgc = imagecolorallocate($im, 255, 255, 255);
        $tc  = imagecolorallocate($im, 0, 0, 0);

        imagefilledrectangle($im, 0, 0, 150, 30, $bgc);

        /* Output an error message */
        imagestring($im, 1, 5, 5, 'Error loading ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/png');

$img = LoadPNG('bogus.image');

imagepng($img);
imagedestroy($img);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecreatefrompng.png" width="150" height="30" alt="imagecreatefrompng() 例子" />

### 注释

imagecreatefromstring
=====================

从字符串中的图像流新建一图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromstring</span> ( <span
class="methodparam"><span class="type">string</span> `$image`</span> )

<span class="function">imagecreatefromstring</span>
返回一个图像标识符，其表达了从给定字符串得来的图像。图像格式将自动检测，只要
PHP 支持：JPEG，PNG，GIF，WBMP 和 GD2。

### 参数

`image`  
A string containing the image data.

### 返回值

An image resource will be returned on success. **`false`** is returned
if the image type is unsupported, the data is not in a recognised
format, or the image is corrupt and cannot be loaded.

### 范例

**示例 \#1 <span class="function">imagecreatefromstring</span> example**

``` php
<?php
$data = 'iVBORw0KGgoAAAANSUhEUgAAABwAAAASCAMAAAB/2U7WAAAABl'
       . 'BMVEUAAAD///+l2Z/dAAAASUlEQVR4XqWQUQoAIAxC2/0vXZDr'
       . 'EX4IJTRkb7lobNUStXsB0jIXIAMSsQnWlsV+wULF4Avk9fLq2r'
       . '8a5HSE35Q3eO2XP1A1wQkZSgETvDtKdQAAAABJRU5ErkJggg==';
$data = base64_decode($data);

$im = imagecreatefromstring($data);
if ($im !== false) {
    header('Content-Type: image/png');
    imagepng($im);
    imagedestroy($im);
}
else {
    echo 'An error occurred.';
}
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecreatefromstring.png" width="28" height="18" alt="Output of example : imagecreatefromstring()" />

### 参见

-   <span class="function">imagecreatefromjpeg</span>
-   <span class="function">imagecreatefrompng</span>
-   <span class="function">imagecreatefromgif</span>
-   <span class="function">imagecreatetruecolor</span>

imagecreatefromwbmp
===================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromwbmp</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefromwbmp</span>
返回一图像标识符，代表了从给定的文件名取得的图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
WBMP 图像的路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 处理创建 WBMP 过程中的错误**

``` php
<?php
function LoadWBMP($imgname)
{
    /* Attempt to open */
    $im = @imagecreatefromwbmp($imgname);

    /* See if it failed */
    if(!$im)
    {
        /* Create a blank image */
        $im  = imagecreatetruecolor(150, 30);
        $bgc = imagecolorallocate($im, 255, 255, 255);
        $tc  = imagecolorallocate($im, 0, 0, 0);

        imagefilledrectangle($im, 0, 0, 150, 30, $bgc);

        /* Output an error message */
        imagestring($im, 1, 5, 5, 'Error loading ' . $imgname, $tc);
    }

    return $im;
}

header('Content-Type: image/vnd.wap.wbmp');

$img = LoadWBMP('bogus.image');

imagewbmp($img);
imagedestroy($img);
?>
```

### 注释

imagecreatefromwebp
===================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromwebp</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefromwebp</span>
返回从给定文件名创建的图像标示符。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
WebP 图像文件路径。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 Convert an WebP image to a jpeg image using <span
class="function">imagecreatefromwebp</span>**

``` php
<?php
// 加载 WebP 文件
$im = imagecreatefromwebp('./example.webp');

// 以 100% 的质量转换成 jpeg 格式
imagejpeg($im, './example.jpeg', 100);
imagedestroy($im);
?>
```

imagecreatefromxbm
==================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromxbm</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefromxbm</span>
返回一图像标识符，代表了从给定的文件名取得的图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

### 参数

`filename`  
Path to the XBM image.

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 Convert an XBM image to a png image using <span
class="function">imagecreatefromxbm</span>**

``` php
<?php
// Load the xbm file
$xbm = imagecreatefromxbm('./example.xbm');

// Convert it to a png file
imagepng($xbm, './example.png');
imagedestroy($xbm);
?>
```

### 注释

imagecreatefromxpm
==================

由文件或 URL 创建一个新图象。

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatefromxpm</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">imagecreatefromxpm</span>
返回一图像标识符，代表了从给定的文件名取得的图像。

**小贴士**

如已启用<a href="/filesystem/setup.html#" class="link">fopen 包装器</a>，在此函数中，
URL 可作为文件名。关于如何指定文件名详见 <span
class="function">fopen</span>。各种 wapper 的不同功能请参见
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>，注意其用法及其可提供的预定义变量。

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

### 参数

`filename`  
Path to the XPM image.

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 Creating an image instance using <span
class="function">imagecreatefromxpm</span>**

``` php
<?php
// Check for XPM support
if(!(imagetypes() & IMG_XPM))
{
    die('Support for xpm was not found!');
}

// Create the image instance
$xpm = imagecreatefromxpm('./example.xpm');

// Do image operations here

// PHP has no support for writing xpm images
// so in this case we save the image as a 
// jpeg file with 100% quality
imagejpeg($xpm, './example.jpg', 100);
imagedestroy($xpm);
?>
```

### 返回值

> **Note**: <span class="simpara">此函数未在 Windows 平台下实现。</span>

imagecreatetruecolor
====================

新建一个真彩色图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagecreatetruecolor</span> ( <span
class="methodparam"><span class="type">int</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span> `$height`</span>
)

<span class="function">imagecreatetruecolor</span>
返回一个图像标识符，代表了一幅大小为 `x_size` 和 `y_size` 的黑色图像。

是否定义了本函数取决于 PHP 和 GD 的版本。从 PHP 4.0.6 到 4.1.x
只要加载了 GD 模块本函数一直存在，但是在没有安装 GD2 的时候调用，PHP
将发出致命错误并退出。在 PHP 4.2.x
中此行为改为发出警告而不是错误。其它版本只在安装了正确的 GD
版本时定义了本函数。

### 参数

`width`  
图像宽度。

`height`  
图像高度。

### 返回值

成功后返回图象资源,失败后返回 **`false`**。

### 范例

**示例 \#1 新建一个新的 GD 图像流并输出图像**

``` php
<?php
header ('Content-Type: image/png');
$im = @imagecreatetruecolor(120, 20)
      or die('Cannot Initialize new GD image stream');
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);
imagepng($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagecreatetruecolor.png" width="120" height="20" alt="例子的输出： 新建一个新的 GD 图像流并输出图像" />

### 注释

### 参见

-   <span class="function">imagedestroy</span>
-   <span class="function">imagecreate</span>

imagecrop
=========

Crop an image to the given rectangle

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">imagecrop</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">array</span> `$rect`</span> )

Crops an image to the given rectangular area and returns the resulting
image. The given `image` is not modified.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`rect`  
The cropping rectangle as <span class="type">array</span> with keys *x*,
*y*, *width* and *height*.

### 返回值

Return cropped image resource on success 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 <span class="function">imagecrop</span> example**

This example shows how to crop an image to a square area.

``` php
<?php
$im = imagecreatefrompng('example.png');
$size = min(imagesx($im), imagesy($im));
$im2 = imagecrop($im, ['x' => 0, 'y' => 0, 'width' => $size, 'height' => $size]);
if ($im2 !== FALSE) {
    imagepng($im2, 'example-cropped.png');
    imagedestroy($im2);
}
imagedestroy($im);
?>
```

### 参见

-   <span class="function">imagecropauto</span>

imagecropauto
=============

Crop an image automatically using one of the available modes

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">imagecropauto</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = **`IMG_CROP_DEFAULT`**</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$threshold`<span
class="initializer"> = .5</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$color`<span
class="initializer"> = -1</span></span> \]\]\] )

Automatically crops an image according to the given `mode`.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`mode`  
One of the following constants:

**`IMG_CROP_DEFAULT`**  
<span class="simpara"> Same as **`IMG_CROP_TRANSPARENT`**. Before PHP
7.4.0, the bundled libgd fell back to **`IMG_CROP_SIDES`**, if the image
had no transparent color. </span>

**`IMG_CROP_TRANSPARENT`**  
<span class="simpara"> Crops out a transparent background. </span>

**`IMG_CROP_BLACK`**  
<span class="simpara"> Crops out a black background. </span>

**`IMG_CROP_WHITE`**  
<span class="simpara"> Crops out a white background. </span>

**`IMG_CROP_SIDES`**  
<span class="simpara"> Uses the 4 corners of the image to attempt to
detect the background to crop. </span>

**`IMG_CROP_THRESHOLD`**  
<span class="simpara"> Crops an image using the given `threshold` and
`color`. </span>

`threshold`  
Specifies the tolerance in percent to be used while comparing the image
color and the color to crop. The method used to calculate the color
difference is based on the color distance in the RGB(a) cube.

Used only in **`IMG_CROP_THRESHOLD`** mode.

> **Note**: <span class="simpara"> Before PHP 7.4.0, the bundled libgd
> used a somewhat different algorithm, so the same `threshold` yielded
> different results for system and bundled libgd. </span>

`color`  
Either an RGB color value or a palette index.

Used only in **`IMG_CROP_THRESHOLD`** mode.

### 返回值

Returns a cropped image resource on success 或者在失败时返回
**`false`**. If the complete image was cropped, <span
class="function">imagecrop</span> returns **`false`**.

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                    |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.4.0 | The behavior of imagecropauto() in the bundled libgd has been synced with that of system libgd: **`IMG_CROP_DEFAULT`** no longer falls back to **`IMG_CROP_SIDES`** and threshold-cropping now uses the same algorithm as system libgd. |
| 7.4.0 | The default value of `mode` has been changed to **`IMG_CROP_AUTO`**. Formerly, the default value has been *-1* which corresponds to **`IMG_CROP_DEFAULT`**, but passing *-1* is now deprecated.                                         |

### 范例

**示例 \#1 Proper handling of auto-cropping**

As noted in the return value section, <span
class="function">imagecropauto</span> returns **`false`** if the whole
image was cropped. In this example we have an image resource *$im* which
should be automatically cropped only if there is something to crop;
otherwise we want to proceed with the original image.

``` php
<?php
$cropped = imagecropauto($im, IMG_CROP_DEFAULT);
if ($cropped !== false) { // in case a new image resource was returned
    imagedestroy($im);    // we destroy the original image
    $im = $cropped;       // and assign the cropped image to $im
}
?>
```

### 参见

-   <span class="function">imagecrop</span>

imagedashedline
===============

画一虚线

### 说明

<span class="type">bool</span> <span
class="methodname">imagedashedline</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$x1`</span> ,
<span class="methodparam"><span class="type">int</span> `$y1`</span> ,
<span class="methodparam"><span class="type">int</span> `$x2`</span> ,
<span class="methodparam"><span class="type">int</span> `$y2`</span> ,
<span class="methodparam"><span class="type">int</span> `$color`</span>
)

反对使用本函数。应该用 <span class="function">imagesetstyle</span> 和
<span class="function">imageline</span> 的组合替代之。

imagedestroy
============

销毁一图像

### 说明

<span class="type">bool</span> <span
class="methodname">imagedestroy</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> )

<span class="function">imagedestroy</span> 释放与 `image`
关联的内存。`image` 是由图像创建函数返回的图像标识符，例如 <span
class="function">imagecreatetruecolor</span>。

imageellipse
============

画一个椭圆

### 说明

<span class="type">bool</span> <span
class="methodname">imageellipse</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">int</span> `$cx`</span> , <span
class="methodparam"><span class="type">int</span> `$cy`</span> , <span
class="methodparam"><span class="type">int</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span> `$height`</span>
, <span class="methodparam"><span class="type">int</span>
`$color`</span> )

在指定的坐标上画一个椭圆。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`cx`  
中间的 X 坐标。

`cy`  
中间的 Y 坐标。

`width`  
椭圆的宽度。

`height`  
椭圆的高度。

`color`  
椭圆的颜色。颜色标识符由 <span
class="function">imagecolorallocate</span> 创建。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imageellipse</span> 例子**

``` php
<?php

// 新建一个空白图像
$image = imagecreatetruecolor(400, 300);

// 填充背景色
$bg = imagecolorallocate($image, 0, 0, 0);

// 选择椭圆的颜色
$col_ellipse = imagecolorallocate($image, 255, 255, 255);

// 画一个椭圆
imageellipse($image, 200, 150, 300, 200, $col_ellipse);

// 输出图像
header("Content-type: image/png");
imagepng($image);


?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imageellipse.png" width="400" height="300" alt="例子输出： imageellipse()" />

### 注释

> **Note**:
>
> 本函数需要 GD 2.0.2 或更高版本。

### 参见

-   <span class="function">imagefilledellipse</span>
-   <span class="function">imagearc</span>

imagefill
=========

区域填充

### 说明

<span class="type">bool</span> <span class="methodname">imagefill</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> , <span class="methodparam"><span
class="type">int</span> `$x`</span> , <span class="methodparam"><span
class="type">int</span> `$y`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

<span class="function">imagefill</span> 在 `image` 图像的坐标
`x`，`y`（图像左上角为 0, 0）处用 `color` 颜色执行区域填充（即与 x, y
点颜色相同且相邻的点都会被填充）。

**示例 \#1 <span class="function">imagefill</span> 例子**

``` php
<?php

$im = imagecreatetruecolor(100, 100);

// 将背景设为红色
$red = imagecolorallocate($im, 255, 0, 0);
imagefill($im, 0, 0, $red);

header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

参见 <span class="function">imagecolorallocate</span>。

imagefilledarc
==============

画一椭圆弧且填充

### 说明

<span class="type">bool</span> <span
class="methodname">imagefilledarc</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$cx`</span> ,
<span class="methodparam"><span class="type">int</span> `$cy`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span>
`$height`</span> , <span class="methodparam"><span
class="type">int</span> `$start`</span> , <span
class="methodparam"><span class="type">int</span> `$end`</span> , <span
class="methodparam"><span class="type">int</span> `$color`</span> ,
<span class="methodparam"><span class="type">int</span> `$style`</span>
)

在指定的 `image` 上画一椭圆弧且填充。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`cx`  
中间的 x 坐标。

`cy`  
中间的 y 坐标。

`width`  
椭圆弧的宽度。

`height`  
椭圆弧的高度。

`start`  
起点角度。

`end`  
终点角度。 0° is located at the three-o'clock position, and the arc is
drawn clockwise.

`color`  
<span class="function">imagecolorallocate</span> 创建的颜色标识符。

`style`  
值可以是下列值的按位或（OR）：

1.  <span class="simpara">**`IMG_ARC_PIE`**</span>
2.  <span class="simpara">**`IMG_ARC_CHORD`**</span>
3.  <span class="simpara">**`IMG_ARC_NOFILL`**</span>
4.  <span class="simpara">**`IMG_ARC_EDGED`**</span>

**`IMG_ARC_PIE`** 和 **`IMG_ARC_CHORD`** 是互斥的；**`IMG_ARC_CHORD`**
只是用直线连接了起始和结束点，**`IMG_ARC_PIE`**
则产生圆形边界。**`IMG_ARC_NOFILL`**
指明弧或弦只有轮廓，不填充。**`IMG_ARC_EDGED`**
指明用直线将起始和结束点与中心点相连，和 **`IMG_ARC_NOFILL`**
一起使用是画饼状图轮廓的好方法（而不用填充）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 创建一 3D 效果的饼状图**

``` php
<?php

// 创建图像
$image = imagecreatetruecolor(100, 100);

// 分配一些颜色
$white    = imagecolorallocate($image, 0xFF, 0xFF, 0xFF);
$gray     = imagecolorallocate($image, 0xC0, 0xC0, 0xC0);
$darkgray = imagecolorallocate($image, 0x90, 0x90, 0x90);
$navy     = imagecolorallocate($image, 0x00, 0x00, 0x80);
$darknavy = imagecolorallocate($image, 0x00, 0x00, 0x50);
$red      = imagecolorallocate($image, 0xFF, 0x00, 0x00);
$darkred  = imagecolorallocate($image, 0x90, 0x00, 0x00);

// 创建 3D 效果
for ($i = 60; $i > 50; $i--) {
   imagefilledarc($image, 50, $i, 100, 50, 0, 45, $darknavy, IMG_ARC_PIE);
   imagefilledarc($image, 50, $i, 100, 50, 45, 75 , $darkgray, IMG_ARC_PIE);
   imagefilledarc($image, 50, $i, 100, 50, 75, 360 , $darkred, IMG_ARC_PIE);
}

imagefilledarc($image, 50, 50, 100, 50, 0, 45, $navy, IMG_ARC_PIE);
imagefilledarc($image, 50, 50, 100, 50, 45, 75 , $gray, IMG_ARC_PIE);
imagefilledarc($image, 50, 50, 100, 50, 75, 360 , $red, IMG_ARC_PIE);


// 输出图像
header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagefilledarc.png" width="100" height="100" alt="例子输出：创建一 3D 效果的饼状图" />

### 注释

imagefilledellipse
==================

画一椭圆并填充

### 说明

<span class="type">bool</span> <span
class="methodname">imagefilledellipse</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$cx`</span> ,
<span class="methodparam"><span class="type">int</span> `$cy`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span>
`$height`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

画一椭圆并填充到指定的 `image`。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`cx`  
中央的 x 坐标。

`cy`  
中央的 y 坐标。

`width`  
椭圆的宽度。

`height`  
椭圆的高度。

`color`  
要填充的颜色。颜色标识由函数 <span
class="function">imagecolorallocate</span> 创建。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagefilledellipse</span> 例子**

``` php
<?php

// create a blank image
$image = imagecreatetruecolor(400, 300);

// fill the background color
$bg = imagecolorallocate($image, 0, 0, 0);

// choose a color for the ellipse
$col_ellipse = imagecolorallocate($image, 255, 255, 255);

// draw the white ellipse
imagefilledellipse($image, 200, 150, 300, 200, $col_ellipse);

// output the picture
header("Content-type: image/png");
imagepng($image);

?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagefilledellipse.png" width="400" height="300" alt="例子输出： imagefilledellipse()" />

### 注释

### 参见

-   <span class="function">imageellipse</span>
-   <span class="function">imagefilledarc</span>

imagefilledpolygon
==================

画一多边形并填充

### 说明

<span class="type">bool</span> <span
class="methodname">imagefilledpolygon</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">array</span>
`$points`</span> , <span class="methodparam"><span
class="type">int</span> `$num_points`</span> , <span
class="methodparam"><span class="type">int</span> `$color`</span> )

<span class="function">imagefilledpolygon</span> 在 `image`
图像中画一个填充了的多边形。

`points` 参数是一个按顺序包含有多边形各顶点的 *x* 和 *y* 坐标的数组。

`num_points` 参数是顶点的总数，必须大于 3。

**示例 \#1 <span class="function">imagefilledpolygon</span> 例子**

``` php
<?php
// 建立多边形各顶点坐标的数组
$values = array(
            40,  50,  // Point 1 (x, y)
            20,  240, // Point 2 (x, y)
            60,  60,  // Point 3 (x, y)
            240, 20,  // Point 4 (x, y)
            50,  40,  // Point 5 (x, y)
            10,  10   // Point 6 (x, y)
            );

// 创建图像
$image = imagecreatetruecolor(250, 250);

// 设定颜色
$bg   = imagecolorallocate($image, 200, 200, 200);
$blue = imagecolorallocate($image, 0, 0, 255);

// 画一个多边形
imagefilledpolygon($image, $values, 6, $blue);

// 输出图像
header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

imagefilledrectangle
====================

画一矩形并填充

### 说明

<span class="type">bool</span> <span
class="methodname">imagefilledrectangle</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$x1`</span> ,
<span class="methodparam"><span class="type">int</span> `$y1`</span> ,
<span class="methodparam"><span class="type">int</span> `$x2`</span> ,
<span class="methodparam"><span class="type">int</span> `$y2`</span> ,
<span class="methodparam"><span class="type">int</span> `$color`</span>
)

<span class="function">imagefilledrectangle</span> 在 `image`
图像中画一个用 `color` 颜色填充了的矩形，其左上角坐标为
`x1`，`y1`，右下角坐标为 `x2`，`y2`。0, 0 是图像的最左上角。

imagefilltoborder
=================

区域填充到指定颜色的边界为止

### 说明

<span class="type">bool</span> <span
class="methodname">imagefilltoborder</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$x`</span> ,
<span class="methodparam"><span class="type">int</span> `$y`</span> ,
<span class="methodparam"><span class="type">int</span> `$border`</span>
, <span class="methodparam"><span class="type">int</span>
`$color`</span> )

<span class="function">imagefilltoborder</span> 从
`x`，`y`（图像左上角为 0, 0）点开始用 `color`
颜色执行区域填充，直到碰到颜色为 `border`
的边界为止。【注：边界内的所有颜色都会被填充。如果指定的边界色和该点颜色相同，则没有填充。如果图像中没有该边界色，则整幅图像都会被填充。】

imagefilter
===========

对图像使用过滤器

### 说明

<span class="type">bool</span> <span
class="methodname">imagefilter</span> ( <span class="methodparam"><span
class="type">resource</span> `$src_im`</span> , <span
class="methodparam"><span class="type">int</span> `$filtertype`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$arg1`</span> \[, <span class="methodparam"><span
class="type">int</span> `$arg2`</span> \[, <span
class="methodparam"><span class="type">int</span> `$arg3`</span> \]\]\]
)

<span class="function">imagefilter</span> 把过滤器 `filtertype`
应用到图像上，在需要时使用 `arg1`，`arg2` 和 `arg3`。

`filtertype` 可以是下列中的一个：

-   <span class="simpara"> `IMG_FILTER_NEGATE`：将图像中所有颜色反转。
    </span>
-   <span class="simpara"> `IMG_FILTER_GRAYSCALE`：将图像转换为灰度的。
    </span>
-   <span class="simpara"> `IMG_FILTER_BRIGHTNESS`：改变图像的亮度。用
    `arg1` 设定亮度级别。 </span>
-   <span class="simpara"> `IMG_FILTER_CONTRAST`：改变图像的对比度。用
    `arg1` 设定对比度级别。 </span>
-   <span class="simpara"> `IMG_FILTER_COLORIZE`：与
    `IMG_FILTER_GRAYSCALE` 类似，不过可以指定颜色。用 `arg1`，`arg2` 和
    `arg3` 分别指定 `red`，`blue` 和 `green`。每种颜色范围是 0 到 255。
    </span>
-   <span class="simpara">
    `IMG_FILTER_EDGEDETECT`：用边缘检测来突出图像的边缘。 </span>
-   <span class="simpara"> `IMG_FILTER_EMBOSS`：使图像浮雕化。 </span>
-   <span class="simpara">
    `IMG_FILTER_GAUSSIAN_BLUR`：用高斯算法模糊图像。 </span>
-   <span class="simpara"> `IMG_FILTER_SELECTIVE_BLUR`：模糊图像。
    </span>
-   <span class="simpara">
    `IMG_FILTER_MEAN_REMOVAL`：用平均移除法来达到轮廓效果。 </span>
-   <span class="simpara"> `IMG_FILTER_SMOOTH`：使图像更柔滑。用 `arg1`
    设定柔滑级别。 </span>

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

**示例 \#1 <span class="function">imagefilter</span> 灰度例子**

``` php
<?php
$im = imagecreatefrompng('dave.png');
if ($im && imagefilter($im, IMG_FILTER_GRAYSCALE)) {
    echo 'Image converted to grayscale.';
    imagepng($im, 'dave.png');
} else {
    echo 'Conversion to grayscale failed.';
}

imagedestroy($im);
?>
```

**示例 \#2 <span class="function">imagefilter</span> 亮度例子**

``` php
<?php
$im = imagecreatefrompng('sean.png');
if ($im && imagefilter($im, IMG_FILTER_BRIGHTNESS, 20)) {
    echo 'Image brightness changed.';
    imagepng($im, 'sean.png');
} else {
    echo 'Image brightness change failed.';
}

imagedestroy($im);
?>
```

**示例 \#3 <span class="function">imagefilter</span> 上彩例子**

``` php
<?php
$im = imagecreatefrompng('philip.png');

/* R, G, B, so 0, 255, 0 is green */
if ($im && imagefilter($im, IMG_FILTER_COLORIZE, 0, 255, 0)) {
    echo 'Image successfully shaded green.';
    imagepng($im, 'philip.png');
} else {
    echo 'Green shading failed.';
}

imagedestroy($im);
?>
```

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`filtertype`  
`filtertype` can be one of the following:

-   <span class="simpara"> **`IMG_FILTER_NEGATE`**: Reverses all colors
    of the image. </span>
-   <span class="simpara"> **`IMG_FILTER_GRAYSCALE`**: Converts the
    image into grayscale. </span>
-   <span class="simpara"> **`IMG_FILTER_BRIGHTNESS`**: Changes the
    brightness of the image. Use `arg1` to set the level of brightness.
    </span>
-   <span class="simpara"> **`IMG_FILTER_CONTRAST`**: Changes the
    contrast of the image. Use `arg1` to set the level of contrast.
    </span>
-   <span class="simpara"> **`IMG_FILTER_COLORIZE`**: Like
    **`IMG_FILTER_GRAYSCALE`**, except you can specify the color. Use
    `arg1`, `arg2` and `arg3` in the form of `red`, `blue`, `green` and
    `arg4` for the `alpha` channel. The range for each color is 0 to
    255. </span>
-   <span class="simpara"> **`IMG_FILTER_EDGEDETECT`**: Uses edge
    detection to highlight the edges in the image. </span>
-   <span class="simpara"> **`IMG_FILTER_EMBOSS`**: Embosses the image.
    </span>
-   <span class="simpara"> **`IMG_FILTER_GAUSSIAN_BLUR`**: Blurs the
    image using the Gaussian method. </span>
-   <span class="simpara"> **`IMG_FILTER_SELECTIVE_BLUR`**: Blurs the
    image. </span>
-   <span class="simpara"> **`IMG_FILTER_MEAN_REMOVAL`**: Uses mean
    removal to achieve a "sketchy" effect. </span>
-   <span class="simpara"> **`IMG_FILTER_SMOOTH`**: Makes the image
    smoother. Use `arg1` to set the level of smoothness. </span>
-   <span class="simpara"> **`IMG_FILTER_PIXELATE`**: Applies pixelation
    effect to the image, use `arg1` to set the block size and `arg2` to
    set the pixelation effect mode. </span>

`arg1`  
-   <span class="simpara"> **`IMG_FILTER_BRIGHTNESS`**: Brightness
    level. </span>
-   <span class="simpara"> **`IMG_FILTER_CONTRAST`**: Contrast level.
    </span>
-   <span class="simpara"> **`IMG_FILTER_COLORIZE`**: 红色成分的值。
    </span>
-   <span class="simpara"> **`IMG_FILTER_SMOOTH`**: Smoothness level.
    </span>
-   <span class="simpara"> **`IMG_FILTER_PIXELATE`**: Block size in
    pixels. </span>

`arg2`  
-   <span class="simpara"> **`IMG_FILTER_COLORIZE`**: 绿色成分的值。
    </span>
-   <span class="simpara"> **`IMG_FILTER_PIXELATE`**: Whether to use
    advanced pixelation effect or not (defaults to **`false`**). </span>

`arg3`  
-   <span class="simpara"> **`IMG_FILTER_COLORIZE`**: 蓝色成分的值。
    </span>

`arg4`  
-   <span class="simpara"> **`IMG_FILTER_COLORIZE`**: Alpha channel, A
    value between 0 and 127. 0 indicates completely opaque while 127
    indicates completely transparent. </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                      |
|-------|-----------------------------------------------------------|
| 5.3.0 | Pixelation support (**`IMG_FILTER_PIXELATE`**) was added. |
| 5.2.5 | Alpha support for **`IMG_FILTER_COLORIZE`** was added.    |

### 范例

**示例 \#4 <span class="function">imagefilter</span> grayscale example**

``` php
<?php
$im = imagecreatefrompng('dave.png');

if($im && imagefilter($im, IMG_FILTER_GRAYSCALE))
{
    echo 'Image converted to grayscale.';

    imagepng($im, 'dave.png');
}
else
{
    echo 'Conversion to grayscale failed.';
}

imagedestroy($im);
?>
```

**示例 \#5 <span class="function">imagefilter</span> brightness
example**

``` php
<?php
$im = imagecreatefrompng('sean.png');

if($im && imagefilter($im, IMG_FILTER_BRIGHTNESS, 20))
{
    echo 'Image brightness changed.';

    imagepng($im, 'sean.png');
    imagedestroy($im);
}
else
{
    echo 'Image brightness change failed.';
}
?>
```

**示例 \#6 <span class="function">imagefilter</span> colorize example**

``` php
<?php
$im = imagecreatefrompng('philip.png');

/* R, G, B, so 0, 255, 0 is green */
if($im && imagefilter($im, IMG_FILTER_COLORIZE, 0, 255, 0))
{
    echo 'Image successfully shaded green.';

    imagepng($im, 'philip.png');
    imagedestroy($im);
}
else
{
    echo 'Green shading failed.';
}
?>
```

**示例 \#7 <span class="function">imagefilter</span> negate example**

``` php
<?php
// Define our negate function so its portable for 
// php versions without imagefilter()
function negate($im)
{
    if(function_exists('imagefilter'))
    {
        return imagefilter($im, IMG_FILTER_NEGATE);
    }

    for($x = 0; $x < imagesx($im); ++$x)
    {
        for($y = 0; $y < imagesy($im); ++$y)
        {
            $index = imagecolorat($im, $x, $y);
            $rgb = imagecolorsforindex($index);
            $color = imagecolorallocate($im, 255 - $rgb['red'], 255 - $rgb['green'], 255 - $rgb['blue']);

            imagesetpixel($im, $x, $y, $color);
        }
    }

    return(true);
}

$im = imagecreatefromjpeg('kalle.jpg');

if($im && negate($im))
{
    echo 'Image successfully converted to negative colors.';

    imagejpeg($im, 'kalle.jpg', 100);
    imagedestroy($im);
}
else
{
    echo 'Converting to negative colors failed.';
}
?>
```

**示例 \#8 <span class="function">imagefilter</span> pixelate example**

``` php
<?php
// Load the PHP logo, we need to create two instances 
// to show the differences
$logo1 = imagecreatefrompng('./php.png');
$logo2 = imagecreatefrompng('./php.png');

// Create the image instance we want to show the 
// differences on
$output = imagecreatetruecolor(imagesx($logo1) * 2, imagesy($logo1));

// Apply pixelation to each instance, with a block 
// size of 3
imagefilter($logo1, IMG_FILTER_PIXELATE, 3);
imagefilter($logo2, IMG_FILTER_PIXELATE, 3, true);

// Merge the differences onto the output image
imagecopy($output, $logo1, 0, 0, 0, 0, imagesx($logo1) - 1, imagesy($logo1) - 1);
imagecopy($output, $logo2, imagesx($logo2), 0, 0, 0, imagesx($logo2) - 1, imagesy($logo2) - 1);
imagedestroy($logo1);
imagedestroy($logo2);

// Output the differences
header('Content-Type: image/png');
imagepng($output);
imagedestroy($output);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagefilterpixelate.png" width="190" height="51" alt="Output of example : imagefilter() pixelate" />

### 注释

### 参见

-   <span class="function">imageconvolution</span>

imageflip
=========

Flips an image using a given mode

### 说明

<span class="type">bool</span> <span class="methodname">imageflip</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> )

Flips the `image` image using the given `mode`.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`mode`  
Flip mode, this can be one of the **`IMG_FLIP_*`** constants:

| Constant                  | Meaning                                           |
|---------------------------|---------------------------------------------------|
| **`IMG_FLIP_HORIZONTAL`** | Flips the image horizontally.                     |
| **`IMG_FLIP_VERTICAL`**   | Flips the image vertically.                       |
| **`IMG_FLIP_BOTH`**       | Flips the image both horizontally and vertically. |

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Flips an image vertically**

This example uses the **`IMG_FLIP_VERTICAL`** constant.

``` php
<?php
// File
$filename = 'phplogo.png';

// Content type
header('Content-type: image/png');

// Load
$im = imagecreatefrompng($filename);

// Flip it vertically
imageflip($im, IMG_FLIP_VERTICAL);

// Output
imagejpeg($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imageflipvertical.png" width="120" height="67" alt="Output of example: Vertically flipped image" />

**示例 \#2 Flips the image horizontally**

This example uses the **`IMG_FLIP_HORIZONTAL`** constant.

``` php
<?php
// File
$filename = 'phplogo.png';

// Content type
header('Content-type: image/png');

// Load
$im = imagecreatefrompng($filename);

// Flip it horizontally
imageflip($im, IMG_FLIP_HORIZONTAL);

// Output
imagejpeg($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagefliphorizontal.png" width="120" height="67" alt="Output of example: Horizontally flipped image" />

imagefontheight
===============

取得字体高度

### 说明

<span class="type">int</span> <span
class="methodname">imagefontheight</span> ( <span
class="methodparam"><span class="type">int</span> `$font`</span> )

返回指定字体一个字符高度的像素值。

参见 <span class="function">imagefontwidth</span> 和 <span
class="function">imageloadfont</span>。

imagefontwidth
==============

取得字体宽度

### 说明

<span class="type">int</span> <span
class="methodname">imagefontwidth</span> ( <span
class="methodparam"><span class="type">int</span> `$font`</span> )

返回指定字体一个字符宽度的像素值。

参见 <span class="function">imagefontheight</span> 和 <span
class="function">imageloadfont</span>。

imageftbbox
===========

给出一个使用 FreeType 2 字体的文本框

### 说明

<span class="type">array</span> <span
class="methodname">imageftbbox</span> ( <span class="methodparam"><span
class="type">float</span> `$size`</span> , <span
class="methodparam"><span class="type">float</span> `$angle`</span> ,
<span class="methodparam"><span class="type">string</span>
`$fontfile`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> \[, <span
class="methodparam"><span class="type">array</span> `$extrainfo`</span>
\] )

This function calculates and returns the bounding box in pixels for a
FreeType text.

### 参数

`size`  
字体的尺寸，单位：点（磅）。

`angle`  
Angle in degrees in which `text` will be measured.

`fontfile`  
The name of the TrueType font file (can be a URL). Depending on which
version of the GD library that PHP is using, it may attempt to search
for files that do not begin with a leading '/' by appending '.ttf' to
the filename and searching along a library-defined font path.

`text`  
The string to be measured.

`extrainfo`  
| Key           | Type                            | Meaning                     |
|---------------|---------------------------------|-----------------------------|
| *linespacing* | <span class="type">float</span> | Defines drawing linespacing |

### 返回值

<span class="function">imageftbbox</span> returns an array with 8
elements representing four points making the bounding box of the text:

|     |                                |
|-----|--------------------------------|
| 0   | lower left corner, X position  |
| 1   | lower left corner, Y position  |
| 2   | lower right corner, X position |
| 3   | lower right corner, Y position |
| 4   | upper right corner, X position |
| 5   | upper right corner, Y position |
| 6   | upper left corner, X position  |
| 7   | upper left corner, Y position  |

The points are relative to the *text* regardless of the `angle`, so
"upper left" means in the top left-hand corner seeing the text
horizontally.

### 范例

**示例 \#1 <span class="function">imageftbbox</span> example**

``` php
<?php
// Create a 300x150 image
$im = imagecreatetruecolor(300, 150);
$black = imagecolorallocate($im, 0, 0, 0);
$white = imagecolorallocate($im, 255, 255, 255);

// Set the background to be white
imagefilledrectangle($im, 0, 0, 299, 299, $white);

// Path to our font file
$font = './arial.ttf';

// First we create our bounding box
$bbox = imageftbbox(10, 0, $font, 'The PHP Documentation Group');

// This is our cordinates for X and Y
$x = $bbox[0] + (imagesx($im) / 2) - ($bbox[4] / 2) - 5;
$y = $bbox[1] + (imagesy($im) / 2) - ($bbox[5] / 2) - 5;

imagefttext($im, 10, 0, $x, $y, $black, $font, 'The PHP Documentation Group');

// Output to browser
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### 注释

> **Note**: <span class="simpara">此函数仅在 PHP 编译时加入 freetype
> 支持时有效（**--with-freetype-dir=DIR**）。</span>

### 更新日志

| 版本  | 说明                           |
|-------|--------------------------------|
| 4.3.5 | `extrainfo` was made optional. |

imagefttext
===========

使用 FreeType 2 字体将文本写入图像

### 说明

<span class="type">array</span> <span
class="methodname">imagefttext</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">float</span> `$size`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle`</span> , <span class="methodparam"><span
class="type">int</span> `$x`</span> , <span class="methodparam"><span
class="type">int</span> `$y`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> , <span
class="methodparam"><span class="type">string</span> `$fontfile`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> \[, <span class="methodparam"><span
class="type">array</span> `$extrainfo`</span> \] )

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`size`  
The font size to use in points.

`angle`  
The angle in degrees, with 0 degrees being left-to-right reading text.
Higher values represent a counter-clockwise rotation. For example, a
value of 90 would result in bottom-to-top reading text.

`x`  
The coordinates given by `x` and `y` will define the basepoint of the
first character (roughly the lower-left corner of the character). This
is different from the <span class="function">imagestring</span>, where
`x` and `y` define the upper-left corner of the first character. For
example, "top left" is 0, 0.

`y`  
The y-ordinate. This sets the position of the fonts baseline, not the
very bottom of the character.

`color`  
The index of the desired color for the text, see <span
class="function">imagecolorexact</span>.

`fontfile`  
The path to the TrueType font you wish to use.

Depending on which version of the GD library PHP is using, *when
`fontfile` does not begin with a leading */* then *.ttf* will be
appended* to the filename and the library will attempt to search for
that filename along a library-defined font path.

When using versions of the GD library lower than 2.0.18, a *space*
character, rather than a semicolon, was used as the 'path separator' for
different font files. Unintentional use of this feature will result in
the warning message: *Warning: Could not find/open font*. For these
affected versions, the only solution is moving the font to a path which
does not contain spaces.

In many cases where a font resides in the same directory as the script
using it the following trick will alleviate any include problems.

``` php
<?php
// Set the enviroment variable for GD
putenv('GDFONTPATH=' . realpath('.'));

// Name the font to be used (note the lack of the .ttf extension)
$font = 'SomeFont';
?>
```

`text`  
Text to be inserted into image.

`extrainfo`  
| Key           | Type                            | Meaning                     |
|---------------|---------------------------------|-----------------------------|
| *linespacing* | <span class="type">float</span> | Defines drawing linespacing |

### 返回值

This function returns an array defining the four points of the box,
starting in the lower left and moving counter-clockwise:

|     |                          |
|-----|--------------------------|
| 0   | lower left x-coordinate  |
| 1   | lower left y-coordinate  |
| 2   | lower right x-coordinate |
| 3   | lower right y-coordinate |
| 4   | upper right x-coordinate |
| 5   | upper right y-coordinate |
| 6   | upper left x-coordinate  |
| 7   | upper left y-coordinate  |

### 范例

**示例 \#1 <span class="function">imagefttext</span> example**

``` php
<?php
// Create a 300x100 image
$im = imagecreatetruecolor(300, 100);
$red = imagecolorallocate($im, 0xFF, 0x00, 0x00);
$black = imagecolorallocate($im, 0x00, 0x00, 0x00);

// Make the background red
imagefilledrectangle($im, 0, 0, 299, 99, $red);

// Path to our ttf font file
$font_file = './arial.ttf';

// Draw the text 'PHP Manual' using font size 13
imagefttext($im, 13, 0, 105, 55, $black, $font_file, 'PHP Manual');

// Output image to the browser
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

### 注释

> **Note**: <span class="simpara">此函数仅在 PHP 编译时加入 freetype
> 支持时有效（**--with-freetype-dir=DIR**）。</span>

### 更新日志

| 版本  | 说明                           |
|-------|--------------------------------|
| 4.3.5 | `extrainfo` was made optional. |

imagegammacorrect
=================

对 GD 图像应用 gamma 修正

### 说明

<span class="type">bool</span> <span
class="methodname">imagegammacorrect</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">float</span>
`$inputgamma`</span> , <span class="methodparam"><span
class="type">float</span> `$outputgamma`</span> )

<span class="function">imagegammacorrect</span> 函数用给定的输入 gamma
值 `inputgamma` 和输出 gamma 值 `outputgamma` 对一幅 GD
图像流（`image`）应用 gamma 修正。

imagegd2
========

将 GD2 图像输出到浏览器或文件

### 说明

<span class="type">bool</span> <span class="methodname">imagegd2</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$chunk_size`</span>
\[, <span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = IMG\_GD2\_RAW</span></span> \]\]\] )

<span class="function">imagegd2</span> 将一个 GD 图像输出到
`filename`。`image`

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`filename`  
文件保存的路径，如果未设置或为 **`null`**，将会直接输出原始图象流。

`chunk_size`  
Chunk size.

`type`  
可以是 **`IMG_GD2_RAW`** 或 **`IMG_GD2_COMPRESSED`**。默认为
**`IMG_GD2_RAW`**。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 输出一个 GD2 图像**

``` php
<?php
// Create a blank image and add some text
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  "A Simple Text String", $text_color);

// Output the image
imagegd2($im);

// Free up memory
imagedestroy($im);
?>
```

**示例 \#2 保存 GD2 图像**

``` php
<?php
// Create a blank image and add some text
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  "A Simple Text String", $text_color);

// Save the gd2 image
// The file format for GD2 images is .gd2, see http://www.libgd.org/GdFileFormats
imagegd2($im, 'simple.gd2');

// Free up memory
imagedestroy($im);
?>
```

### 注释

> **Note**:
>
> GD2 格式一般是用来加载图像中的一部分时更快。注意 GD2
> 格式只能用于兼容于 GD2 的应用程序。

### 更新日志

| 版本  | 说明                                |
|-------|-------------------------------------|
| 4.3.2 | 添加了参数 `chunk_size` 和 `type`。 |

### 参见

-   <span class="function">imagegd</span>

imagegd
=======

将 GD 图像输出到浏览器或文件

### 说明

<span class="type">bool</span> <span class="methodname">imagegd</span> (
<span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \] )

<span class="function">imagegd</span> 将一个 GD 图像输出到
`filename`。`image` 参数是由 <span
class="function">imagecreatetruecolor</span> 函数返回的。

`filename` 参数为可选项，如果为空，则原始图像流会被直接输出。

> **Note**:
>
> GD 格式一般是用来加载图像中的一部分时更快。注意 GD 格式只能用于兼容于
> GD 的应用程序。

参见 <span class="function">imagegd2</span>。

imagegetclip
============

Get the clipping rectangle

### 说明

<span class="type">array</span> <span
class="methodname">imagegetclip</span> ( <span class="methodparam"><span
class="type">resource</span> `$im`</span> )

<span class="function">imagegetclip</span> retrieves the current
clipping rectangle, i.e. the area beyond which no pixels will be drawn.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

### 返回值

The function returns an indexed array with the coordinates of the
clipping rectangle which has the following entries:

-   <span class="simpara">x-coordinate of the upper left corner</span>
-   <span class="simpara">y-coordinate of the upper left corner</span>
-   <span class="simpara">x-coordinate of the lower right corner</span>
-   <span class="simpara">y-coordinate of the lower right corner</span>

### 范例

**示例 \#1 <span class="function">imagegetclip</span> example**

Setting and retrieving the clipping rectangle.

``` php
<?php
$im = imagecreate(100, 100);
imagesetclip($im, 10,10, 89,89);
print_r(imagegetclip($im));
```

以上例程会输出：

    Array
    (
        [0] => 10
        [1] => 10
        [2] => 89
        [3] => 89
    )

### 参见

-   <span class="function">imagesetclip</span>

imagegetinterpolation
=====================

Get the interpolation method

### 说明

<span class="type">int</span> <span
class="methodname">imagegetinterpolation</span> ( <span
class="methodparam"><span class="type">GdImage</span> `$image`</span> )

Gets the currently set interpolation method of the `image`.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

### 返回值

Returns the interpolation method.

### 参见

-   <span class="function">imagesetinterpolation</span>

imagegif
========

输出图象到浏览器或文件。

### 说明

<span class="type">bool</span> <span class="methodname">imagegif</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \] )

<span class="function">imagegif</span> 从 `image` 图像以 `filename`
为文件名创建一个 GIF 图像。`image` 参数是 <span
class="function">imagecreate</span> 或 *imagecreatefrom\**
函数的返回值。

图像格式为 GIF87a。如果用了 <span
class="function">imagecolortransparent</span> 使图像为透明，则其格式为
GIF89a。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`filename`  
文件保存的路径，如果未设置或为 **`null`**，将会直接输出原始图象流。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 使用 <span class="function">imagegif</span> 输出一个图像**

``` php
<?php
// 创建新的图像实例
$im = imagecreatetruecolor(100, 100);

// 设置背景为白色
imagefilledrectangle($im, 0, 0, 99, 99, 0xFFFFFF);

//在图像上写字
imagestring($im, 3, 40, 20, 'GD Library', 0xFFBA00);

// 输出图像到浏览器
header('Content-Type: image/gif');

imagegif($im);
imagedestroy($im);
?>
```

**示例 \#2 使用 <span class="function">imagegif</span> 将一个 PNG 转换成
GIF**

``` php
<?php

// 载入 PNG
$png = imagecreatefrompng('./php.png');

// 以 GIF 保存图像
imagegif($png, './php.gif');

// 释放内存
imagedestroy($png);

// 完工
echo 'Converted PNG image to GIF with success!';
?>
```

### 注释

> **Note**:
>
> 不过从 GD 库 1.6 起所有的 GIF 支持都移除了，并在版本 2.0.28
> 中加了回来。如果使用这些 版本之间的 GD 库时本函数不可用。 更多信息见
> <a href="http://www.libgd.org/" class="link external">» GD Project</a>
> 站点。
>
> 以下代码段通过自动检测 GD 支持的图像类型来写出移植性更好的 PHP
> 程序。用更灵活的代码替代了原来的 *header("Content-type: image/gif");
> imagegif($im);*：
>
> ``` php
> <?php
> // 创建新的图像实例
> $im = imagecreatetruecolor(100, 100);
>
> // 在这里对图像进行一些操作
>
> // 处理输出
> if(function_exists('imagegif'))
> {
>     // 针对 GIF
>     header('Content-Type: image/gif');
>
>     imagegif($im);
> }
> elseif(function_exists('imagejpeg'))
> {
>     // 针对 JPEG
>     header('Content-Type: image/jpeg');
>
>     imagejpeg($im, NULL, 100);
> }
> elseif(function_exists('imagepng'))
> {
>     // 针对 PNG
>     header('Content-Type: image/png');
>
>     imagepng($im);
> }
> elseif(function_exists('imagewbmp'))
> {
>     // 针对 WBMP
>     header('Content-Type: image/vnd.wap.wbmp');
>
>     imagewbmp($im);
> }
> else
> {
>     imagedestroy($im);
>
>     die('No image support in this PHP server');
> }
>
> // 如果发现图像是以上的格式之一，就从内存中释放
> if($im)
> {
>     imagedestroy($im);
> }
> ?>
> ```

> **Note**:
>
> 自 PHP 3.0.18 和 4.0.2 起可以用 <span
> class="function">imagetypes</span> 函数代替 <span
> class="function">function\_exists</span> 来检查是否支持某种图像格式：
>
> ``` php
> <?php
> if(imagetypes() & IMG_GIF)
> {
>     header('Content-Type: image/gif');
>     imagegif($im);
> }
> elseif(imagetypes() & IMG_JPG)
> {
>     /* ... etc. */
> }
> ?>
> ```

### 参见

-   <span class="function">imagepng</span>
-   <span class="function">imagewbmp</span>
-   <span class="function">imagejpeg</span>
-   <span class="function">imagetypes</span>

imagegrabscreen
===============

Captures the whole screen

### 说明

<span class="type">resource</span> <span
class="methodname">imagegrabscreen</span> ( <span
class="methodparam">void</span> )

Grabs a screenshot of the whole screen.

> **Note**:
>
> This function is only available on Windows.

### 返回值

Returns an image resource identifier on success, **`false`** on failure.

### 范例

**示例 \#1 <span class="function">imagegrabscreen</span> example**

This example demonstrates how to take a screenshot of the current screen
and save it as a png image.

``` php
<?php
$im = imagegrabscreen();
imagepng($im, "myscreenshot.png");
imagedestroy($im);
?>
```

### 参见

-   <span class="function">imagegrabwindow</span>

imagegrabwindow
===============

Captures a window

### 说明

<span class="type">resource</span> <span
class="methodname">imagegrabwindow</span> ( <span
class="methodparam"><span class="type">int</span>
`$window_handle`</span> \[, <span class="methodparam"><span
class="type">int</span> `$client_area`<span class="initializer"> =
0</span></span> \] )

Grabs a window or its client area using a windows handle (HWND property
in COM instance)

> **Note**:
>
> This function is only available on Windows.

### 参数

`window_handle`  
The HWND window ID.

`client_area`  
Include the client area of the application window.

### 返回值

Returns an image resource identifier on success, **`false`** on failure.

### 错误／异常

E\_NOTICE is issued if `window_handle` is invalid window handle.
E\_WARNING is issued if the Windows API is too old.

### 范例

**示例 \#1 <span class="function">imagegrabwindow</span> example**

Capture a window (IE for example)

``` php
<?php
$browser = new COM("InternetExplorer.Application");
$handle = $browser->HWND;
$browser->Visible = true;
$im = imagegrabwindow($handle);
$browser->Quit();
imagepng($im, "iesnap.png");
imagedestroy($im);
?>
```

Capture a window (IE for example) but with its content

``` php
<?php
$browser = new COM("InternetExplorer.Application");
$handle = $browser->HWND;
$browser->Visible = true;
$browser->Navigate("http://www.libgd.org");

/* Still working? */
while ($browser->Busy) {
    com_message_pump(4000);
}
$im = imagegrabwindow($handle, 0);
$browser->Quit();
imagepng($im, "iesnap.png");
imagedestroy($im);
?>
```

### 参见

-   <span class="function">imagegrabscreen</span>

imageinterlace
==============

激活或禁止隔行扫描

### 说明

<span class="type">int</span> <span
class="methodname">imageinterlace</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$interlace`</span> \] )

<span class="function">imageinterlace</span>
打开或关闭隔行扫描的比特标记。如果 `interlace` 为 1
则图像为隔行扫描的，如果 `interlace` 为 0 则图像为非隔行扫描的。

如果设定了隔行扫描比特标记而图像使用 JPEG 格式，则图像被创建为渐进式
JPEG。

本函数返回图像中是否设定了隔行扫描比特标记。

imageistruecolor
================

检查图像是否为真彩色图像

### 说明

<span class="type">bool</span> <span
class="methodname">imageistruecolor</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> )

<span class="function">imageistruecolor</span> 检查 `image`
图像是否为真彩色图像。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

### 返回值

如果 `image` 是真彩色图像返回 **`true`**，否则返回 **`false`**。

### 范例

**示例 \#1 Simple detection of true color image instances using <span
class="function">imageistruecolor</span>**

``` php
<?php
// $im is an image instance

// Check if image is a true color image or not
if(!imageistruecolor($im))
{
    // Create a new true color image instance
    $tc = imagecreatetruecolor(imagesx($im), imagesy($im));

    imagecopy($tc, $im, 0, 0, 0, 0, imagesx($im), imagesy($im));
    imagedestroy($im);

    $im = $tc;
    $tc = NULL;
}

// Continue working with image instance
?>
```

### 注释

### 参见

-   <span class="function">imagecreatetruecolor</span>

imagejpeg
=========

输出图象到浏览器或文件。

### 说明

<span class="type">bool</span> <span class="methodname">imagejpeg</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$quality`</span> \]\]
)

<span class="function">imagejpeg</span> 从 `image` 图像以 `filename`
为文件名创建一个 JPEG 图像。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`filename`  
文件保存的路径，如果未设置或为 **`null`**，将会直接输出原始图象流。

如果要省略这个参数而提供 `quality` 参数，使用NULL。

`quality`  
`quality` 为可选项，范围从 0（最差质量，文件更小）到
100（最佳质量，文件最大）。默认为 IJG 默认的质量值（大约 75）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 输出 JPEG 图像**

``` php
<?php
// 创键空白图像并添加一些文本
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// 设置内容类型标头 —— 这个例子里是 image/jpeg
header('Content-Type: image/jpeg');

// 输出图像
imagejpeg($im);

// 释放内存
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagejpeg.jpg" width="120" height="20" alt="例子的输出：输出 JPEG 图像" />

**示例 \#2 保存一副 JPEG 图像**

``` php
<?php
// 创键空白图像并添加一些文本
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// 保存图像为 'simpletext.jpg'
imagejpeg($im, 'simpletext.jpg');

// 释放内存
imagedestroy($im);
?>
```

**示例 \#3 以 75% 的图像质量输出图像**

``` php
<?php
// 创键空白图像并添加一些文本
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// 设置内容类型标头 —— 这个例子里是 image/jpeg
header('Content-Type: image/jpeg');

// 使用 NULL 跳过 filename 参数，并设置图像质量为 75%
imagejpeg($im, NULL, 75);

// 释放内存
imagedestroy($im);
?>
```

### 注释

> **Note**:
>
> 如果想输出渐进式 JPEG，需要用 <span
> class="function">imageinterlace</span> 函数将隔行扫描比特置位。

### 参见

-   <span class="function">imagepng</span>
-   <span class="function">imagegif</span>
-   <span class="function">imagewbmp</span>
-   <span class="function">imageinterlace</span>
-   <span class="function">imagetypes</span>

imagelayereffect
================

设定 alpha 混色标志以使用绑定的 libgd 分层效果

### 说明

<span class="type">bool</span> <span
class="methodname">imagelayereffect</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$effect`</span>
)

设定 alpha 混色标志以使用绑定的 libgd 分层效果。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`effect`  
One of the following constants:

**`IMG_EFFECT_REPLACE`**  
<span class="simpara"> Use pixel replacement (equivalent of passing
**`true`** to <span class="function">imagealphablending</span>) </span>

**`IMG_EFFECT_ALPHABLEND`**  
<span class="simpara"> Use normal pixel blending (equivalent of passing
**`false`** to <span class="function">imagealphablending</span>) </span>

**`IMG_EFFECT_NORMAL`**  
<span class="simpara"> Same as **`IMG_EFFECT_ALPHABLEND`**. </span>

**`IMG_EFFECT_OVERLAY`**  
<span class="simpara"> Overlay has the effect that black background
pixels will remain black, white background pixels will remain white, but
grey background pixels will take the colour of the foreground pixel.
</span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagelayereffect</span> example**

``` php
<?php
// Setup an image
$im = imagecreatetruecolor(100, 100);

// Set a background
imagefilledrectangle($im, 0, 0, 100, 100, imagecolorallocate($im, 220, 220, 220));

// Apply the overlay alpha blending flag
imagelayereffect($im, IMG_EFFECT_OVERLAY);

// Draw two grey ellipses
imagefilledellipse($im, 50, 50, 40, 40, imagecolorallocate($im, 100, 255, 100));
imagefilledellipse($im, 50, 50, 50, 80, imagecolorallocate($im, 100, 100, 255));
imagefilledellipse($im, 50, 50, 80, 50, imagecolorallocate($im, 255, 100, 100));

// Output
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagelayereffect.png" width="100" height="100" alt="Output of example : imagelayereffect()" />

### 注释

imageline
=========

画一条线段

### 说明

<span class="type">bool</span> <span class="methodname">imageline</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> , <span class="methodparam"><span
class="type">int</span> `$x1`</span> , <span class="methodparam"><span
class="type">int</span> `$y1`</span> , <span class="methodparam"><span
class="type">int</span> `$x2`</span> , <span class="methodparam"><span
class="type">int</span> `$y2`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

<span class="function">imageline</span> 用 `color` 颜色在图像 `image`
中从坐标 `x1`，`y1` 到 `x2`，`y2`（图像左上角为 0, 0）画一条线段。

**示例 \#1 画一条粗线**

``` php
<?php

function imagelinethick($image, $x1, $y1, $x2, $y2, $color, $thick = 1)
{
    /* 下面两行只在线段直角相交时好使
    imagesetthickness($image, $thick);
    return imageline($image, $x1, $y1, $x2, $y2, $color);
    */
    if ($thick == 1) {
        return imageline($image, $x1, $y1, $x2, $y2, $color);
    }
    $t = $thick / 2 - 0.5;
    if ($x1 == $x2 || $y1 == $y2) {
        return imagefilledrectangle($image, round(min($x1, $x2) - $t), round(min($y1, $y2) - $t), round(max($x1, $x2) + $t), round(max($y1, $y2) + $t), $color);
    }
    $k = ($y2 - $y1) / ($x2 - $x1); //y = kx + q
    $a = $t / sqrt(1 + pow($k, 2));
    $points = array(
        round($x1 - (1+$k)*$a), round($y1 + (1-$k)*$a),
        round($x1 - (1-$k)*$a), round($y1 - (1+$k)*$a),
        round($x2 + (1+$k)*$a), round($y2 - (1-$k)*$a),
        round($x2 + (1-$k)*$a), round($y2 + (1+$k)*$a),
    );
    imagefilledpolygon($image, $points, 4, $color);
    return imagepolygon($image, $points, 4, $color);
}

?>
```

参见 <span class="function">imagecreatetruecolor</span> 和 <span
class="function">imagecolorallocate</span>。

imageloadfont
=============

载入一新字体

### 说明

<span class="type">int</span> <span
class="methodname">imageloadfont</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

<span class="function">imageloadfont</span>
加载一个用户定义的位图字体并返回该字体的标识符（其值总是大于
5，因此不会和内置字体冲突）。 在产生错误的情况下，该函数返回 **`false`**
。

字体文件格式目前是二进制的且和平台有关。这意味着应该用和你运行 PHP
的机器相同类型 CPU 的机器生成字体。

| 字节位置   | C 数据类型 | 说明                                                                      |
|------------|------------|---------------------------------------------------------------------------|
| byte 0-3   | int        | 字体中的字符数目                                                          |
| byte 4-7   | int        | 字体中第一个字符的值（通常是 32 代表空格）                                |
| byte 8-11  | int        | 每个字符宽度的像素值                                                      |
| byte 12-15 | int        | 每个字符高度的像素值                                                      |
| byte 16-   | char       | 字符数据的数组，每字符中每像素一字节，一共 (nchars\*width\*height) 字节。 |

**示例 \#1 使用 imageloadfont**

``` php
<?php
header("Content-type: image/png");
$im = imagecreatetruecolor(50, 20);
$black = imagecolorallocate($im, 0, 0, 0);
$white = imagecolorallocate($im, 255, 255, 255);
imagefilledrectangle($im, 0, 0, 49, 19, $white);
$font = imageloadfont("04b.gdf");
imagestring($im, $font, 0, 0, "Hello", $black);
imagepng($im);
?>
```

参见 <span class="function">imagefontwidth</span> 和 <span
class="function">imagefontheight</span>。

imageopenpolygon
================

Draws an open polygon

### 说明

<span class="type">bool</span> <span
class="methodname">imageopenpolygon</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">array</span>
`$points`</span> , <span class="methodparam"><span
class="type">int</span> `$num_points`</span> , <span
class="methodparam"><span class="type">int</span> `$color`</span> )

Alternative signature (as of PHP 8.0.0)

<span class="type">bool</span> <span
class="methodname">imageopenpolygon</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">array</span>
`$points`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

<span class="function">imageopenpolygon</span> draws an open polygon on
the given `image`. Contrary to <span
class="function">imagepolygon</span>, no line is drawn between the last
and the first point.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`points`  
An array containing the polygon's vertices, e.g.:

|             |      |
|-------------|------|
| points\[0\] | = x0 |
| points\[1\] | = y0 |
| points\[2\] | = x1 |
| points\[3\] | = y1 |

`num_points`  
Total number of points (vertices), which must be at least 3.

<span class="simpara"> If this parameter is omitted as per the second
signature, `points` must have an even number of elements, and
`num_points` is assumed to be `count($points)/2`. </span>

`color`  
颜色标识符使用 <span class="function">imagecolorallocate</span> 创建。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imageopenpolygon</span> example**

``` php
<?php
// Create a blank image
$image = imagecreatetruecolor(400, 300);

// Allocate a color for the polygon
$col_poly = imagecolorallocate($image, 255, 255, 255);

// Draw the polygon
imageopenpolygon($image, array(
        0,   0,
        100, 200,
        300, 200
    ),
    3,
    $col_poly);

// Output the picture to the browser
header('Content-type: image/png');

imagepng($image);
imagedestroy($image);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imageopenpolygon.png" width="400" height="300" alt="Output of example : imageopenpolygon()" />

### 参见

-   <span class="function">imagepolygon</span>

imagepalettecopy
================

将调色板从一幅图像拷贝到另一幅

### 说明

<span class="type">void</span> <span
class="methodname">imagepalettecopy</span> ( <span
class="methodparam"><span class="type">resource</span>
`$destination`</span> , <span class="methodparam"><span
class="type">resource</span> `$source`</span> )

<span class="function">imagepalettecopy</span> 从 `source`
图像把调色板拷贝到 `destination` 图像。

imagepalettetotruecolor
=======================

Converts a palette based image to true color

### 说明

<span class="type">bool</span> <span
class="methodname">imagepalettetotruecolor</span> ( <span
class="methodparam"><span class="type">resource</span> `$src`</span> )

Converts a palette based image, created by functions like <span
class="function">imagecreate</span> to a true color image, like <span
class="function">imagecreatetruecolor</span>.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

### 返回值

Returns **`true`** if the convertion was complete, or if the source
image already is a true color image, otherwise **`false`** is returned.

### 范例

**示例 \#1 Converts any image resource to true color**

``` php
<?php
// Backwards compatiblity
if(!function_exists('imagepalettetotruecolor'))
{
    function imagepalettetotruecolor(&$src)
    {
        if(imageistruecolor($src))
        {
            return(true);
        }

        $dst = imagecreatetruecolor(imagesx($src), imagesy($src));

        imagecopy($dst, $src, 0, 0, 0, 0, imagesx($src), imagesy($src));
        imagedestroy($src);

        $src = $dst;

        return(true);
    }
}

// Helper closure
$typeof = function() use($im)
{
    echo 'typeof($im) = ' . (imageistruecolor($im) ? 'true color' : 'palette'), PHP_EOL;
};

// Create a palette based image
$im = imagecreate(100, 100);
$typeof();

// Convert it to true color
imagepalettetotruecolor($im);
$typeof();

// Free the memory
imagedestroy($im);
?>
```

以上例程会输出：

    typeof($im) = palette
    typeof($im) = true color

### 参见

-   <span class="function">imagecreatetruecolor</span>
-   <span class="function">imageistruecolor</span>

imagepng
========

以 PNG 格式将图像输出到浏览器或文件

### 说明

<span class="type">bool</span> <span class="methodname">imagepng</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \] )

<span class="function">imagepng</span> 将 GD 图像流（`image`）以 PNG
格式输出到标准输出（通常为浏览器），或者如果用 `filename`
给出了文件名则将其输出到该文件。

``` php
<?php
$im = imagecreatefrompng("test.png");
imagepng($im);
?>
```

参见 <span class="function">imagegif</span>，<span
class="function">imagewbmp</span>，<span
class="function">imagejpeg</span> 和 <span
class="function">imagetypes</span>。

imagepolygon
============

画一个多边形

### 说明

<span class="type">bool</span> <span
class="methodname">imagepolygon</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">array</span> `$points`</span> ,
<span class="methodparam"><span class="type">int</span>
`$num_points`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> )

<span class="function">imagepolygon</span>
在图像中创建一个多边形。`points` 是一个 PHP
数组，包含了多边形的各个顶点坐标，即 points\[0\] = x0，points\[1\] =
y0，points\[2\] = x1，points\[3\] = y1，以此类推。`num_points`
是顶点的总数。

**示例 \#1 <span class="function">imagepolygon</span> 例子**

``` php
<?php
// create a blank image
$image = imagecreatetruecolor(400, 300);

// fill the background color
$bg = imagecolorallocate($image, 0, 0, 0);

// choose a color for the polygon
$col_poly = imagecolorallocate($image, 255, 255, 255);

// draw the polygon
imagepolygon($image,
             array (
                    0, 0,
                    100, 200,
                    300, 200
             ),
             3,
             $col_poly);

// output the picture
header("Content-type: image/png");
imagepng($image);

?>
```

参见 <span class="function">imagecreate</span> 和 <span
class="function">imagecreatetruecolor</span>。

imagerectangle
==============

画一个矩形

### 说明

<span class="type">bool</span> <span
class="methodname">imagerectangle</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$x1`</span> ,
<span class="methodparam"><span class="type">int</span> `$y1`</span> ,
<span class="methodparam"><span class="type">int</span> `$x2`</span> ,
<span class="methodparam"><span class="type">int</span> `$y2`</span> ,
<span class="methodparam"><span class="type">int</span> `$col`</span> )

<span class="function">imagerectangle</span> 用 `col` 颜色在 `image`
图像中画一个矩形，其左上角坐标为 x1, y1，右下角坐标为 x2,
y2。图像的左上角坐标为 0, 0。

imageresolution
===============

Get or set the resolution of the image

### 说明

<span class="type">mixed</span> <span
class="methodname">imageresolution</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> )

<span class="type">mixed</span> <span
class="methodname">imageresolution</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$res_x`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$res_y`<span class="initializer"> = $res\_x</span></span> \] )

<span class="function">imageresolution</span> allows to set and get the
resolution of an image in DPI (dots per inch). If none of the optional
parameters is given, the current resolution is returned as indexed
array. If only `res_x` is given, the horizontal and vertical resolution
are set to this value. If both optional parameters are given, the
horizontal and vertical resolution are set to these values,
respectively.

The resolution is only used as meta information when images are read
from and written to formats supporting this kind of information
(curently PNG and JPEG). It does not affect any drawing operations. The
default resolution for new images is 96 DPI.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`res_x`  
The horizontal resolution in DPI.

`res_y`  
The vertical resolution in DPI.

### 返回值

When used as getter (first signature), it returns an indexed array of
the horizontal and vertical resolution on success, 或者在失败时返回
**`false`**. When used as setter (second signature), it returns
**`true`** on success, 或者在失败时返回 **`false`**.

### 范例

**示例 \#1 Setting and getting the resolution of an image**

``` php
<?php
$im = imagecreatetruecolor(100, 100);
imageresolution($im, 200);
print_r(imageresolution($im));
imageresolution($im, 300, 72);
print_r(imageresolution($im));
?>
```

以上例程会输出：

    Array
    (
        [0] => 200
        [1] => 200
    )
    Array
    (
        [0] => 300
        [1] => 72
    )

imagerotate
===========

用给定角度旋转图像

### 说明

<span class="type">resource</span> <span
class="methodname">imagerotate</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">float</span> `$angle`</span> ,
<span class="methodparam"><span class="type">int</span>
`$bgd_color`</span> \[, <span class="methodparam"><span
class="type">int</span> `$ignore_transparent`<span class="initializer">
= 0</span></span> \] )

将 `src_im` 图像用给定的 `angle` 角度旋转。`bgd_color`
指定了旋转后没有覆盖到的部分的颜色。

旋转的中心是图像的中心，旋转后的图像会按比例缩小以适合目标图像的大小——边缘不会被剪去。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`angle`  
Rotation angle, in degrees. The rotation angle is interpreted as the
number of degrees to rotate the image anticlockwise.

`bgd_color`  
Specifies the color of the uncovered zone after the rotation

`ignore_transparent`  
如果被设为非零值，则透明色会被忽略（否则会被保留）。

### 返回值

返回旋转后的图像资源， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                           |
|-------|--------------------------------|
| 5.1.0 | 新增： `ignore_transparent` 。 |

### 范例

**示例 \#1 将图像旋转 180 度**

本例将把一幅图像旋转 180 度——上下颠倒。

``` php
<?php
// File and rotation
$filename = 'test.jpg';
$degrees = 180;

// Content type
header('Content-type: image/jpeg');

// Load
$source = imagecreatefromjpeg($filename);

// Rotate
$rotate = imagerotate($source, $degrees, 0);

// Output
imagejpeg($rotate);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagerotate.jpg" width="95" height="51" alt="例子的输出：将图像旋转 180 度" />

### 注释

imagesavealpha
==============

设置标记以在保存 PNG 图像时保存完整的 alpha 通道信息（与单一透明色相反）

### 说明

<span class="type">bool</span> <span
class="methodname">imagesavealpha</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$saveflag`</span> )

<span class="function">imagesavealpha</span> 设置标记以在保存 PNG
图像时保存完整的 alpha 通道信息（与单一透明色相反）。

要使用本函数，必须将 alphablending 清位（*imagealphablending($im,
false)*）。

不是所有的浏览器都支持 alpha
通道，如果在你的浏览器上碰到问题，试着用兼容 alpha
通道的浏览器（例如最新版的 Mozilla）重新加载脚本。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`saveflag`  
是否保存透明（alpha）通道。 默认 **`false`**。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagesavealpha</span> 例子**

``` php
<?php
// 载入带 alpha 通道的 png 图像
$png = imagecreatefrompng('./alphachannel_example.png');

// 做些必须的操作

// 关闭 alpha 渲染并设置 alpha 标志
imagealphablending($png, false);
imagesavealpha($png, true);

// 输出图像到浏览器
header('Content-Type: image/png');

imagepng($png);
imagedestroy($png);
?>
```

### 注释

### 参见

-   <span class="function">imagealphablending</span>

imagescale
==========

Scale an image using the given new width and height

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">imagescale</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">int</span> `$new_width`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$new_height`<span class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = IMG\_BILINEAR\_FIXED</span></span> \]\] )

<span class="function">imagescale</span> scales an image using the given
interpolation algorithm.

> **Note**:
>
> Unlike many of other image functions, <span
> class="function">imagescale</span> does not modify the passed `image`;
> instead, a *new* image is returned.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`new_width`  
The width to scale the image to.

`new_height`  
The height to scale the image to. If omitted or negative, the aspect
ratio will be preserved.

`mode`  
One of **`IMG_NEAREST_NEIGHBOUR`**, **`IMG_BILINEAR_FIXED`**,
**`IMG_BICUBIC`**, **`IMG_BICUBIC_FIXED`** or anything else (will use
two pass).

> **Note**: <span class="simpara"> **`IMG_WEIGHTED4`** is not yet
> supported. </span>

### 返回值

Return the scaled image resource on success 或者在失败时返回
**`false`**.

### 参见

-   <span class="function">imagecopyresized</span>
-   <span class="function">imagecopyresampled</span>

imagesetbrush
=============

设定画线用的画笔图像

### 说明

<span class="type">bool</span> <span
class="methodname">imagesetbrush</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$brush`</span> )

当用特殊的颜色 *IMG\_COLOR\_BRUSHED* 或 *IMG\_COLOR\_STYLEDBRUSHED*
绘画时，<span class="function">imagesetbrush</span>
设定了所有画线的函数（例如 <span class="function">imageline</span> 和
<span
class="function">imagepolygon</span>）所使用的画笔图像。【注：使用画笔图像，所画的线是由
`brush` 所代表的图像构成的。请参考并尝试运行 <span
class="function">imagesetstyle</span> 中的例子以帮助理解。】

> **Note**:
>
> 使用完画笔图像后不需要采取什么特殊动作。但如果销毁了画笔图像，在设定一个新的画笔图像之前不能使用
> *IMG\_COLOR\_BRUSHED* 或 *IMG\_COLOR\_STYLEDBRUSHED*！

> **Note**:
>
> 本函数是 PHP 4.0.6 添加的。

imagesetclip
============

Set the clipping rectangle

### 说明

<span class="type">bool</span> <span
class="methodname">imagesetclip</span> ( <span class="methodparam"><span
class="type">resource</span> `$im`</span> , <span
class="methodparam"><span class="type">int</span> `$x1`</span> , <span
class="methodparam"><span class="type">int</span> `$y1`</span> , <span
class="methodparam"><span class="type">int</span> `$x2`</span> , <span
class="methodparam"><span class="type">int</span> `$y2`</span> )

<span class="function">imagesetclip</span> sets the current clipping
rectangle, i.e. the area beyond which no pixels will be drawn.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`x1`  
The x-coordinate of the upper left corner.

`y1`  
The y-coordinate of the upper left corner.

`x2`  
The x-coordinate of the lower right corner.

`y2`  
The y-coordinate of the lower right corner.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">imagegetclip</span>

imagesetinterpolation
=====================

Set the interpolation method

### 说明

<span class="type">bool</span> <span
class="methodname">imagesetinterpolation</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$method`<span class="initializer"> = IMG\_BILINEAR\_FIXED</span></span>
\] )

Sets the interpolation method, setting an interpolation method affects
the rendering of various functions in GD, such as the <span
class="function">imagerotate</span> function.

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`method`  
The interpolation method, which can be one of the following:

-   <span class="simpara"> **`IMG_BELL`**: Bell filter. </span>
-   <span class="simpara"> **`IMG_BESSEL`**: Bessel filter. </span>
-   <span class="simpara"> **`IMG_BICUBIC`**: Bicubic interpolation.
    </span>
-   <span class="simpara"> **`IMG_BICUBIC_FIXED`**: Fixed point
    implementation of the bicubic interpolation. </span>
-   <span class="simpara"> **`IMG_BILINEAR_FIXED`**: Fixed point
    implementation of the bilinear interpolation (*default (also on
    image creation)*). </span>
-   <span class="simpara"> **`IMG_BLACKMAN`**: Blackman window function.
    </span>
-   <span class="simpara"> **`IMG_BOX`**: Box blur filter. </span>
-   <span class="simpara"> **`IMG_BSPLINE`**: Spline interpolation.
    </span>
-   <span class="simpara"> **`IMG_CATMULLROM`**: Cubic Hermite spline
    interpolation. </span>
-   <span class="simpara"> **`IMG_GAUSSIAN`**: Gaussian function.
    </span>
-   <span class="simpara"> **`IMG_GENERALIZED_CUBIC`**: Generalized
    cubic spline fractal interpolation. </span>
-   <span class="simpara"> **`IMG_HERMITE`**: Hermite interpolation.
    </span>
-   <span class="simpara"> **`IMG_HAMMING`**: Hamming filter. </span>
-   <span class="simpara"> **`IMG_HANNING`**: Hanning filter. </span>
-   <span class="simpara"> **`IMG_MITCHELL`**: Mitchell filter. </span>
-   <span class="simpara"> **`IMG_POWER`**: Power interpolation. </span>
-   <span class="simpara"> **`IMG_QUADRATIC`**: Inverse quadratic
    interpolation. </span>
-   <span class="simpara"> **`IMG_SINC`**: Sinc function. </span>
-   <span class="simpara"> **`IMG_NEAREST_NEIGHBOUR`**: Nearest
    neighbour interpolation. </span>
-   <span class="simpara"> **`IMG_WEIGHTED4`**: Weighting filter.
    </span>
-   <span class="simpara"> **`IMG_TRIANGLE`**: Triangle interpolation.
    </span>

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagesetinterpolation</span> example**

``` php
<?php
// Load an image
$im = imagecreate(500, 500);

// By default interpolation is IMG_BILINEAR_FIXED, switch 
// to use the 'Mitchell' filter:
imagesetinterpolation($im, IMG_MITCHELL);

// Continue to work with $im ...
?>
```

### 注释

Changing the interpolation method affects the following functions when
rendering:

-   <span class="simpara"> <span class="function">imageaffine</span>
    </span>
-   <span class="simpara"> <span class="function">imagerotate</span>
    </span>

### 参见

-   <span class="function">imagegetinterpolation</span>

imagesetpixel
=============

画一个单一像素

### 说明

<span class="type">bool</span> <span
class="methodname">imagesetpixel</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$x`</span> ,
<span class="methodparam"><span class="type">int</span> `$y`</span> ,
<span class="methodparam"><span class="type">int</span> `$color`</span>
)

<span class="function">imagesetpixel</span> 在 `image` 图像中用 `color`
颜色在 `x`，`y` 坐标（图像左上角为 0，0）上画一个点。

参见 <span class="function">imagecreatetruecolor</span> 和 <span
class="function">imagecolorallocate</span>。

imagesetstyle
=============

设定画线的风格

### 说明

<span class="type">bool</span> <span
class="methodname">imagesetstyle</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">array</span>
`$style`</span> )

<span class="function">imagesetstyle</span> 设定所有画线的函数（例如
<span class="function">imageline</span> 和 <span
class="function">imagepolygon</span>）在使用特殊颜色
**`IMG_COLOR_STYLED`** 或者用 **`IMG_COLOR_STYLEDBRUSHED`**
画一行图像时所使用的风格。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`style`  
像素组成的数组。你可以通过常量 **`IMG_COLOR_TRANSPARENT`**
来添加一个透明像素。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

下面的示例脚本在画布上从左上角到右下角画一行虚线：

**示例 \#1 <span class="function">imagesetstyle</span> 例子**

``` php
<?php
header("Content-type: image/jpeg");
$im  = imagecreatetruecolor(100, 100);
$w   = imagecolorallocate($im, 255, 255, 255);
$red = imagecolorallocate($im, 255, 0, 0);

/* 画一条虚线，5 个红色像素，5 个白色像素 */
$style = array($red, $red, $red, $red, $red, $w, $w, $w, $w, $w);
imagesetstyle($im, $style);
imageline($im, 0, 0, 100, 100, IMG_COLOR_STYLED);

/* 用 imagesetbrush() 和 imagesetstyle 画一行笑脸 */
$style = array($w, $w, $w, $w, $w, $w, $w, $w, $w, $w, $w, $w, $red);
imagesetstyle($im, $style);

$brush = imagecreatefrompng("http://www.libpng.org/pub/png/images/smile.happy.png");
$w2 = imagecolorallocate($brush, 255, 255, 255);
imagecolortransparent($brush, $w2);
imagesetbrush($im, $brush);
imageline($im, 100, 0, 0, 100, IMG_COLOR_STYLEDBRUSHED);

imagejpeg($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagesetstyle.jpg" width="100" height="100" alt="Output of example : imagesetstyle()" />

### 参见

-   <span class="function">imagesetbrush</span>
-   <span class="function">imageline</span>

imagesetthickness
=================

设定画线的宽度

### 说明

<span class="type">bool</span> <span
class="methodname">imagesetthickness</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span>
`$thickness`</span> )

<span class="function">imagesetthickness</span>
把画矩形，多边形，椭圆等等时所用的线宽设为 `thickness`
个像素。成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`thickness`  
Thickness, in pixels.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">imagesetthickness</span> example**

``` php
<?php
// Create a 200x100 image
$im = imagecreatetruecolor(200, 100);
$white = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);
$black = imagecolorallocate($im, 0x00, 0x00, 0x00);

// Set the background to be white
imagefilledrectangle($im, 0, 0, 299, 99, $white);

// Set the line thickness to 5
imagesetthickness($im, 5);

// Draw the rectangle
imagerectangle($im, 14, 14, 185, 85, $black);

// Output image to the browser
header('Content-Type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagesetthickness.png" width="200" height="100" alt="Output of example : imagesetthickness()" />

### 注释

imagesettile
============

设定用于填充的贴图

### 说明

<span class="type">bool</span> <span
class="methodname">imagesettile</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">resource</span> `$tile`</span> )

<span class="function">imagesettile</span> 设定所有区域填充函数（例如
<span class="function">imagefill</span> 和 <span
class="function">imagefilledpolygon</span>）在使用特殊颜色
*IMG\_COLOR\_TILED* 填充时所使用的贴图。

贴图是指用重复的样式来填充一块区域所使用的图像。*任何* GD
图像都能用作贴图，并且通过使用 <span
class="function">imagecolortransparent</span>
来设定贴图的透明色，贴图可以使底层的特定区域透上来。

> **Note**:
>
> 使用完贴图后不需要采取什么特殊动作。但如果销毁了贴图，在设定一个新的贴图之前不能使用
> *IMG\_COLOR\_TILED*！

imagestring
===========

水平地画一行字符串

### 说明

<span class="type">bool</span> <span
class="methodname">imagestring</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">int</span> `$font`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">string</span> `$s`</span> , <span
class="methodparam"><span class="type">int</span> `$col`</span> )

<span class="function">imagestring</span> 用 `col` 颜色将字符串 `s` 画到
`image` 所代表的图像的 `x`，`y`
坐标处（这是字符串左上角坐标，整幅图像的左上角为 0，0）。如果 `font` 是
1，2，3，4 或 5，则使用内置字体。

**示例 \#1 <span class="function">imagestring</span> 例子**

``` php
<?php
// 建立一幅 100X30 的图像
$im = imagecreate(100, 30);

// 白色背景和蓝色文本
$bg = imagecolorallocate($im, 255, 255, 255);
$textcolor = imagecolorallocate($im, 0, 0, 255);

// 把字符串写在图像左上角
imagestring($im, 5, 0, 0, "Hello world!", $textcolor);

// 输出图像
header("Content-type: image/png");
imagepng($im);
?>
```

参见 <span class="function">imageloadfont</span> 和 <span
class="function">imagettftext</span>。

imagestringup
=============

垂直地画一行字符串

### 说明

<span class="type">bool</span> <span
class="methodname">imagestringup</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">int</span> `$font`</span> ,
<span class="methodparam"><span class="type">int</span> `$x`</span> ,
<span class="methodparam"><span class="type">int</span> `$y`</span> ,
<span class="methodparam"><span class="type">string</span> `$s`</span> ,
<span class="methodparam"><span class="type">int</span> `$col`</span> )

<span class="function">imagestring</span> 用 `col` 颜色将字符串 `s`
垂直地画到 `image` 所代表的图像的 `x`, `y` 座标处（图像的左上角为 0,
0）。如果 `font` 是 1，2，3，4 或 5，则使用内置字体。

参见 <span class="function">imageloadfont</span>。

imagesx
=======

取得图像宽度

### 说明

<span class="type">int</span> <span class="methodname">imagesx</span> (
<span class="methodparam"><span class="type">resource</span>
`$image`</span> )

<span class="function">imagesx</span> 返回 `image` 所代表的图像的宽度。

**示例 \#1 使用 <span class="function">imagesx</span>**

``` php
<?php

// create a 300*200 image
$img = imagecreatetruecolor(300, 200);

echo imagesx($img); // 300

?>
```

参见 <span class="function">imagecreatetruecolor</span>，<span
class="function">getimagesize</span> 和 <span
class="function">imagesy</span>。

imagesy
=======

取得图像高度

### 说明

<span class="type">int</span> <span class="methodname">imagesy</span> (
<span class="methodparam"><span class="type">resource</span>
`$image`</span> )

<span class="function">imagesy</span> 返回 `image` 所代表的图像的高度。

**示例 \#1 使用 <span class="function">imagesy</span>**

``` php
<?php

// create a 300*200 image
$img = imagecreatetruecolor(300, 200);

echo imagesy($img); // 200

?>
```

参见 <span class="function">imagecreatetruecolor</span>，<span
class="function">getimagesize</span> 和 <span
class="function">imagesx</span>。

imagetruecolortopalette
=======================

将真彩色图像转换为调色板图像

### 说明

<span class="type">bool</span> <span
class="methodname">imagetruecolortopalette</span> ( <span
class="methodparam"><span class="type">resource</span> `$image`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$dither`</span> , <span class="methodparam"><span
class="type">int</span> `$ncolors`</span> )

<span class="function">imagetruecolortopalette</span>
将一幅真彩色图像转换为调色板图像。本函数的代码原本是从独立的 JPEG
小组库代码中提取出来的，非常出色。此代码被修改以在结果调色板中保留尽可能多的
alpha
通道信息以及尽可能多的颜色。但并没有达到期望的效果。通常最好生成真彩色图像输出，这样可以保证得到最高的输出质量。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`dither`  
指明图像是否被抖动（dithered），如果为 **`true`**
则图像将被抖动使图像中的斑点更多但是颜色更接近。

`ncolors`  
设定调色板中被保留的颜色的最大数目。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 Converting a true color image to a palette-based image**

``` php
<?php
// Create a new true color image
$im = imagecreatetruecolor(100, 100);

// Convert to palette-based with no dithering and 255 colors
imagetruecolortopalette($im, false, 255);

// Save the image
imagepng($im, './paletteimage.png');
imagedestroy($im);
?>
```

### 注释

imagettfbbox
============

取得使用 TrueType 字体的文本的范围

### 说明

<span class="type">array</span> <span
class="methodname">imagettfbbox</span> ( <span class="methodparam"><span
class="type">float</span> `$size`</span> , <span
class="methodparam"><span class="type">float</span> `$angle`</span> ,
<span class="methodparam"><span class="type">string</span>
`$fontfile`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

本函数计算并返回一个包围着 TrueType 文本范围的虚拟方框的像素大小。

`size`  
<span class="simpara">像素单位的字体大小。</span>

`angle`  
<span class="simpara">`text` 将被度量的角度大小。</span>

`fontfile`  
<span class="simpara"> TrueType 字体文件的文件名（可以是 URL）。根据 PHP
所使用的 GD 库版本，可能尝试搜索那些不是以 '/' 开头的文件名并加上 '.ttf'
的后缀并搜索库定义的字体路径。 </span>

`text`  
<span class="simpara">要度量的字符串。</span>

<span class="function">imagettfbbox</span> 返回一个含有 8
个单元的数组表示了文本外框的四个角：

|     |               |
|-----|---------------|
| 0   | 左下角 X 位置 |
| 1   | 左下角 Y 位置 |
| 2   | 右下角 X 位置 |
| 3   | 右下角 Y 位置 |
| 4   | 右上角 X 位置 |
| 5   | 右上角 Y 位置 |
| 6   | 左上角 X 位置 |
| 7   | 左上角 Y 位置 |

这些点是相对于*文本*的而和角度无关，因此“左上角”指的是以水平方向看文字时其左上角。

本函数同时需要 GD 库和 FreeType 库。

参见 <span class="function">imagettftext</span>。

imagettftext
============

用 TrueType 字体向图像写入文本

### 说明

<span class="type">array</span> <span
class="methodname">imagettftext</span> ( <span class="methodparam"><span
class="type">resource</span> `$image`</span> , <span
class="methodparam"><span class="type">float</span> `$size`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle`</span> , <span class="methodparam"><span
class="type">int</span> `$x`</span> , <span class="methodparam"><span
class="type">int</span> `$y`</span> , <span class="methodparam"><span
class="type">int</span> `$color`</span> , <span
class="methodparam"><span class="type">string</span> `$fontfile`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> )

使用 TrueType 字体将 指定的 `text` 写入图像。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`size`  
字体的尺寸，单位：点（磅）。

`angle`  
角度制表示的角度，0 度为从左向右读的文本。更高数值表示逆时针旋转。例如
90 度表示从下向上读的文本。

`x`  
由 `x`，`y`
所表示的坐标定义了第一个字符的基本点（大概是字符的左下角）。这和 <span
class="function">imagestring</span> 不同，其 `x`，`y`
定义了第一个字符的左上角。例如 "top left" 为 0, 0。

`y`  
Y 坐标。它设定了字体基线的位置，不是字符的最底端。

`color`  
颜色索引。使用负的颜色索引值具有关闭防锯齿的效果。见 <span
class="function">imagecolorallocate</span>。

`fontfile`  
是想要使用的 TrueType 字体的路径。

根据 PHP 所使用的 GD 库的不同，*当 `fontfile` 没有以 */* 开头时则 *.ttf*
将被加到文件名之后*并且会在库定义字体路径中尝试搜索该文件名。

当使用的 GD 库版本低于 2.0.18 时，一个空格字符
而不是分号将被用来作为不同字体文件的“路径分隔符”。不小心使用了此特性将会导致一条警告信息：*Warning:
Could not find/open
font*。对受影响的版本来说唯一解决方案就是将字体移动到不包含空格的路径中去。

很多情况下字体都放在脚本的同一个目录下。下面的小技巧可以减轻包含的问题。

``` php
<?php
// Set the enviroment variable for GD
putenv('GDFONTPATH=' . realpath('.'));

// Name the font to be used (note the lack of the .ttf extension)
$font = 'SomeFont';
?>
```

`text`  
UTF-8 编码的文本字符串。

可以包含十进制数字化字符表示（形式为：&\#8364;）来访问字体中超过位置 127
的字符。UTF-8 编码的字符串可以直接传递。

命名实体，比如 &copy; 是不支持的。可以考虑使用 <span
class="function">html\_entity\_decode</span> 来解码命名实体为 UTF-8
字符。 （自 PHP 5.0.0 开始 html\_entity\_decode() 开始支持）

如果字符串中使用的某个字符不被字体支持，一个空心矩形将替换该字符。

### 返回值

返回一个含有 8
个单元的数组表示了文本外框的四个角，顺序为坐下角，右下角，右上角，左上角。这些点是相对于文本的而和角度无关，因此“左上角”指的是以水平方向看文字时其左上角。

### 更新日志

| 版本  | 说明                                                           |
|-------|----------------------------------------------------------------|
| 5.2.0 | It is now possible to specify an hexadecimal entity in `text`. |

### 范例

**示例 \#1 <span class="function">imagettftext</span> 例子**

本例中的脚本将生成一个白色的 400x30 像素 PNG
图像，其中有黑色（带灰色阴影）Arial 字体写的“Testing...”。

``` php
<?php
// Set the content-type
header('Content-Type: image/png');

// Create the image
$im = imagecreatetruecolor(400, 30);

// Create some colors
$white = imagecolorallocate($im, 255, 255, 255);
$grey = imagecolorallocate($im, 128, 128, 128);
$black = imagecolorallocate($im, 0, 0, 0);
imagefilledrectangle($im, 0, 0, 399, 29, $white);

// The text to draw
$text = 'Testing...';
// Replace path by your own font path
$font = 'arial.ttf';

// Add some shadow to the text
imagettftext($im, 20, 0, 11, 21, $grey, $font, $text);

// Add the text
imagettftext($im, 20, 0, 10, 20, $black, $font, $text);

// Using imagepng() results in clearer text compared with imagejpeg()
imagepng($im);
imagedestroy($im);
?>
```

以上例程的输出类似于：

<img src="images/21009b70229598c6a80eef8b45bf282b-imagettftext.png" width="400" height="30" alt="例子输出：imagettftext()" />

### 注释

> **Note**:
>
> 本函数同时需要 GD 库和
> <a href="http://www.freetype.org/" class="link external">» FreeType</a>
> 库。.

### 参见

-   <span class="function">imagettfbbox</span>

imagetypes
==========

返回当前 PHP 版本所支持的图像类型

### 说明

<span class="type">int</span> <span class="methodname">imagetypes</span>
( <span class="methodparam">void</span> )

本函数以比特字段方式返回与当前 PHP 版本关联的 GD
库所支持的图像格式。将返回以下结果，**`IMG_GIF`** \| **`IMG_JPG`** \|
**`IMG_PNG`** \| **`IMG_WBMP`**\| **`IMG_XPM`**。 例如要检查是否支持
PNG，这样做：

**示例 \#1 <span class="function">imagetypes</span> 例子**

``` php
<?php
if (imagetypes() & IMG_PNG) {
    echo "PNG Support is enabled";
}
?>
```

imagewbmp
=========

以 WBMP 格式将图像输出到浏览器或文件

### 说明

<span class="type">bool</span> <span class="methodname">imagewbmp</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$foreground`</span>
\]\] )

<span class="function">imagewbmp</span> 从 `image` 图像创建一个名为
`filename` 的 WBMP 文件。`image` 参数是 <span
class="function">imagecreatetruecolor</span> 的返回值。

`filename` 参数是可选项，如果省略，则直接将原图像流输出。通过用 <span
class="function">header</span> 发送 image/vnd.wap.wbmp 的
Content-type，可以创建直接输出 WBMP 图像的 PHP 脚本。

> **Note**:
>
> WBMP 支持仅能用于 PHP 编译时加入了 GD-1.8 或更高版本时。

用可选的 `foreground` 参数可以设定前景色，用 <span
class="function">imagecolorallocate</span>
函数返回的颜色标识符。默认前景色是黑色。

参见 <span class="function">image2wbmp</span>，<span
class="function">imagepng</span>，<span
class="function">imagegif</span>，<span
class="function">imagejpeg</span> 和 <span
class="function">imagetypes</span>。

imagewebp
=========

将 WebP 格式的图像输出到浏览器或文件

### 说明

<span class="type">bool</span> <span class="methodname">imagewebp</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$to`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$quality`<span class="initializer"> =
80</span></span> \]\] )

将 `image` 参数指定的图像以 WebP 格式输出到浏览器或者保存到文件。

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`to`  
文件保存的路径，如果未设置或为 **`null`**，将会直接输出原始图象流。

`quality`  
`quality` 范围从0（最低质量，最小文件体积）到100 （最好质量,
最大文件体积）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 更新日志

| 版本  | 说明                                                             |
|-------|------------------------------------------------------------------|
| 5.4.0 | 支持把 <span class="type">resource</span> 流作为 `to` 参数传入。 |

### 范例

**示例 \#1 保存为 WebP 图像文件**

``` php
<?php
// 创建一个空图像并在其上加入一些文字
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);

imagestring($im, 1, 5, 5,  'WebP with PHP', $text_color);

// 保存图像
imagewebp($im, 'php.webp');

// 释放内存
imagedestroy($im);
?>
```

imagexbm
========

将 XBM 图像输出到浏览器或文件

### 说明

<span class="type">bool</span> <span class="methodname">imagexbm</span>
( <span class="methodparam"><span class="type">resource</span>
`$image`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$foreground`</span>
\] )

将 XBM 图像 `image` 输出到浏览器或文件

### 参数

`image`  
由图象创建函数(例如<span
class="function">imagecreatetruecolor</span>)返回的图象资源。

`filename`  
文件保存的路径，如果未设置或为 **`null`**，将会直接输出原始图象流。

`foreground`  
你可以从 <span class="function">imagecolorallocate</span>
分配一个颜色，并设置为该前景色参数。 默认颜色是黑色。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 保存一个 XBM 文件**

``` php
<?php
// 创建空白图像并添加文字
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// 保存图像
imagexbm($im, 'simpletext.xbm');

// 释放内存
imagedestroy($im);
?>
```

**示例 \#2 以不同前景色保存一个 XBM 文件**

``` php
<?php
// 创建空白图像并添加文字
$im = imagecreatetruecolor(120, 20);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'A Simple Text String', $text_color);

// 设置替换的前景色
$foreground_color = imagecolorallocate($im, 255, 0, 0);

// 保存图像
imagexbm($im, NULL, $foreground_color);

// 释放内存
imagedestroy($im);
?>
```

### 注释

iptcembed
=========

将二进制 IPTC 数据嵌入到一幅 JPEG 图像中

### 说明

<span class="type">mixed</span> <span
class="methodname">iptcembed</span> ( <span class="methodparam"><span
class="type">string</span> `$iptcdata`</span> , <span
class="methodparam"><span class="type">string</span>
`$jpeg_file_name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$spool`</span> \] )

Embeds binary IPTC data into a JPEG image.

### 参数

`iptcdata`  
The data to be written.

`jpeg_file_name`  
Path to the JPEG image.

`spool`  
Spool flag. If the spool flag is over 2 then the JPEG will be returned
as a string.

### 返回值

If success and spool flag is lower than 2 then the JPEG will not be
returned as a string, **`false`** on errors.

### 范例

**示例 \#1 Embedding IPTC data into a JPEG**

``` php
<?php

// iptc_make_tag() function by Thies C. Arntzen
function iptc_make_tag($rec, $data, $value)
{
    $length = strlen($value);
    $retval = chr(0x1C) . chr($rec) . chr($data);

    if($length < 0x8000)
    {
        $retval .= chr($length >> 8) .  chr($length & 0xFF);
    }
    else
    {
        $retval .= chr(0x80) . 
                   chr(0x04) . 
                   chr(($length >> 24) & 0xFF) . 
                   chr(($length >> 16) & 0xFF) . 
                   chr(($length >> 8) & 0xFF) . 
                   chr($length & 0xFF);
    }

    return $retval . $value;
}

// Path to jpeg file
$path = './phplogo.jpg';

// We need to check if theres any IPTC data in the jpeg image. If there is then 
// bail out because we cannot embed any image that already has some IPTC data!
$image = getimagesize($path, $info);

if(isset($info['APP13']))
{
    die('Error: IPTC data found in source image, cannot continue');
}

// Set the IPTC tags
$iptc = array(
    '2#120' => 'Test image',
    '2#116' => 'Copyright 2008-2009, The PHP Group'
);

// Convert the IPTC tags into binary code
$data = '';

foreach($iptc as $tag => $string)
{
    $tag = substr($tag, 2);
    $data .= iptc_make_tag(2, $tag, $string);
}

// Embed the IPTC data
$content = iptcembed($data, $path);

// Write the new image data out to the file.
$fp = fopen($path, "wb");
fwrite($fp, $content);
fclose($fp);
?>
```

### 注释

> **Note**:
>
> 此函数不需要 GD 图象库。

iptcparse
=========

将二进制 IPTC 块解析为单个标记

### 说明

<span class="type">array</span> <span
class="methodname">iptcparse</span> ( <span class="methodparam"><span
class="type">string</span> `$iptcblock`</span> )

本函数将一个二进制的
<a href="http://www.iptc.org/" class="link external">» IPTC</a>
块解析为单个的标记。

### 参数

`iptcblock`  
二进制的 IPTC 块。

### 返回值

返回一个数组，用 tagmarker 作为索引，以其值为值。如果出错或未发现 IPTC
数据则返回 **`false`**。

### 范例

**示例 \#1 iptcparse() used together with <span
class="function">getimagesize</span>**

``` php
<?php
$size = getimagesize('./test.jpg', $info);
if(isset($info['APP13']))
{
    $iptc = iptcparse($info['APP13']);
    var_dump($iptc);
}
?>
```

### 注释

> **Note**:
>
> 此函数不需要 GD 图象库。

jpeg2wbmp
=========

将 JPEG 图像文件转换为 WBMP 图像文件

### 说明

<span class="type">bool</span> <span class="methodname">jpeg2wbmp</span>
( <span class="methodparam"><span class="type">string</span>
`$jpegname`</span> , <span class="methodparam"><span
class="type">string</span> `$wbmpname`</span> , <span
class="methodparam"><span class="type">int</span> `$dest_height`</span>
, <span class="methodparam"><span class="type">int</span>
`$dest_width`</span> , <span class="methodparam"><span
class="type">int</span> `$threshold`</span> )

将 JPEG 图像文件转换为 WBMP 图像文件。

### 参数

`jpegname`  
JPEG 文件的路径。

`wbmpname`  
目标 WBMP 文件的路径。

`dest_height`  
目标图像高度。

`dest_width`  
目标图像宽度。

`threshold`  
阈值，在 0 和 8 之间（含）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">jpeg2wbmp</span> 例子**

``` php
<?php
// 目标 jpeg 的路径
$path = './test.jpg';

// 获取图像尺寸
$image = getimagesize($path);

// 转换图像
jpeg2wbmp($path, './test.wbmp', $image[1], $image[0], 5);
?>
```

### 注释

### 参见

-   <span class="function">png2wbmp</span>

png2wbmp
========

将 PNG 图像文件转换为 WBMP 图像文件

### 说明

<span class="type">bool</span> <span class="methodname">png2wbmp</span>
( <span class="methodparam"><span class="type">string</span>
`$pngname`</span> , <span class="methodparam"><span
class="type">string</span> `$wbmpname`</span> , <span
class="methodparam"><span class="type">int</span> `$dest_height`</span>
, <span class="methodparam"><span class="type">int</span>
`$dest_width`</span> , <span class="methodparam"><span
class="type">int</span> `$threshold`</span> )

将名为 `pngname` 的 PNG 文件转换为 WBMP 格式，并存为 `wbmpname`。用
`d_height` 和 `d_width` 指定目标图像的高度和宽度。

### 参数

`pngname`  
PNG 文件的路径。

`wbmpname`  
目标 WBMP 文件的路径。

`dest_height`  
目标图像的高度。

`dest_width`  
目标图像的宽度。

`threshold`  
阈值，在 0 到 8 之间（含）。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">png2wbmp</span> 例子**

``` php
<?php
// Path to the target png
$path = './test.png';

// Get the image sizes
$image = getimagesize($path);

// Convert image
png2wbmp($path, './test.wbmp', $image[1], $image[0], 7);
?>
```

### 注释

### 参见

-   <span class="function">jpeg2wbmp</span>

**目录**

-   [gd\_info](/ref/image.html#gd_info) — 取得当前安装的 GD 库的信息
-   [getimagesize](/ref/image.html#getimagesize) — 取得图像大小
-   [getimagesizefromstring](/ref/image.html#getimagesizefromstring) —
    从字符串中获取图像尺寸信息
-   [image\_type\_to\_extension](/ref/image.html#image_type_to_extension)
    — 取得图像类型的文件后缀
-   [image\_type\_to\_mime\_type](/ref/image.html#image_type_to_mime_type)
    — 取得
    getimagesize，exif\_read\_data，exif\_thumbnail，exif\_imagetype
    所返回的图像类型的 MIME 类型
-   [image2wbmp](/ref/image.html#image2wbmp) — 以 WBMP
    格式将图像输出到浏览器或文件
-   [imageaffine](/ref/image.html#imageaffine) —
    返回经过仿射变换后的图像，剪切区域可选
-   [imageaffinematrixconcat](/ref/image.html#imageaffinematrixconcat) —
    Concatenate two affine transformation matrices
-   [imageaffinematrixget](/ref/image.html#imageaffinematrixget) — Get
    an affine transformation matrix
-   [imagealphablending](/ref/image.html#imagealphablending) —
    设定图像的混色模式
-   [imageantialias](/ref/image.html#imageantialias) —
    是否使用抗锯齿（antialias）功能
-   [imagearc](/ref/image.html#imagearc) — 画椭圆弧
-   [imagebmp](/ref/image.html#imagebmp) — Output a BMP image to browser
    or file
-   [imagechar](/ref/image.html#imagechar) — 水平地画一个字符
-   [imagecharup](/ref/image.html#imagecharup) — 垂直地画一个字符
-   [imagecolorallocate](/ref/image.html#imagecolorallocate) —
    为一幅图像分配颜色
-   [imagecolorallocatealpha](/ref/image.html#imagecolorallocatealpha) —
    为一幅图像分配颜色 + alpha
-   [imagecolorat](/ref/image.html#imagecolorat) —
    取得某像素的颜色索引值
-   [imagecolorclosest](/ref/image.html#imagecolorclosest) —
    取得与指定的颜色最接近的颜色的索引值
-   [imagecolorclosestalpha](/ref/image.html#imagecolorclosestalpha) —
    取得与指定的颜色加透明度最接近的颜色
-   [imagecolorclosesthwb](/ref/image.html#imagecolorclosesthwb) —
    取得与给定颜色最接近的色度的黑白色的索引
-   [imagecolordeallocate](/ref/image.html#imagecolordeallocate) —
    取消图像颜色的分配
-   [imagecolorexact](/ref/image.html#imagecolorexact) —
    取得指定颜色的索引值
-   [imagecolorexactalpha](/ref/image.html#imagecolorexactalpha) —
    取得指定的颜色加透明度的索引值
-   [imagecolormatch](/ref/image.html#imagecolormatch) —
    使一个图像中调色板版本的颜色与真彩色版本更能匹配
-   [imagecolorresolve](/ref/image.html#imagecolorresolve) —
    取得指定颜色的索引值或有可能得到的最接近的替代值
-   [imagecolorresolvealpha](/ref/image.html#imagecolorresolvealpha) —
    取得指定颜色 + alpha 的索引值或有可能得到的最接近的替代值
-   [imagecolorset](/ref/image.html#imagecolorset) —
    给指定调色板索引设定颜色
-   [imagecolorsforindex](/ref/image.html#imagecolorsforindex) —
    取得某索引的颜色
-   [imagecolorstotal](/ref/image.html#imagecolorstotal) —
    取得一幅图像的调色板中颜色的数目
-   [imagecolortransparent](/ref/image.html#imagecolortransparent) —
    将某个颜色定义为透明色
-   [imageconvolution](/ref/image.html#imageconvolution) — 用系数 div 和
    offset 申请一个 3x3 的卷积矩阵
-   [imagecopy](/ref/image.html#imagecopy) — 拷贝图像的一部分
-   [imagecopymerge](/ref/image.html#imagecopymerge) —
    拷贝并合并图像的一部分
-   [imagecopymergegray](/ref/image.html#imagecopymergegray) —
    用灰度拷贝并合并图像的一部分
-   [imagecopyresampled](/ref/image.html#imagecopyresampled) —
    重采样拷贝部分图像并调整大小
-   [imagecopyresized](/ref/image.html#imagecopyresized) —
    拷贝部分图像并调整大小
-   [imagecreate](/ref/image.html#imagecreate) —
    新建一个基于调色板的图像
-   [imagecreatefrombmp](/ref/image.html#imagecreatefrombmp) — 由文件或
    URL 创建一个新图象。
-   [imagecreatefromgd2](/ref/image.html#imagecreatefromgd2) — 从 GD2
    文件或 URL 新建一图像
-   [imagecreatefromgd2part](/ref/image.html#imagecreatefromgd2part) —
    从给定的 GD2 文件或 URL 中的部分新建一图像
-   [imagecreatefromgd](/ref/image.html#imagecreatefromgd) — 从 GD
    文件或 URL 新建一图像
-   [imagecreatefromgif](/ref/image.html#imagecreatefromgif) — 由文件或
    URL 创建一个新图象。
-   [imagecreatefromjpeg](/ref/image.html#imagecreatefromjpeg) —
    由文件或 URL 创建一个新图象。
-   [imagecreatefrompng](/ref/image.html#imagecreatefrompng) — 由文件或
    URL 创建一个新图象。
-   [imagecreatefromstring](/ref/image.html#imagecreatefromstring) —
    从字符串中的图像流新建一图像
-   [imagecreatefromwbmp](/ref/image.html#imagecreatefromwbmp) —
    由文件或 URL 创建一个新图象。
-   [imagecreatefromwebp](/ref/image.html#imagecreatefromwebp) —
    由文件或 URL 创建一个新图象。
-   [imagecreatefromxbm](/ref/image.html#imagecreatefromxbm) — 由文件或
    URL 创建一个新图象。
-   [imagecreatefromxpm](/ref/image.html#imagecreatefromxpm) — 由文件或
    URL 创建一个新图象。
-   [imagecreatetruecolor](/ref/image.html#imagecreatetruecolor) —
    新建一个真彩色图像
-   [imagecrop](/ref/image.html#imagecrop) — Crop an image to the given
    rectangle
-   [imagecropauto](/ref/image.html#imagecropauto) — Crop an image
    automatically using one of the available modes
-   [imagedashedline](/ref/image.html#imagedashedline) — 画一虚线
-   [imagedestroy](/ref/image.html#imagedestroy) — 销毁一图像
-   [imageellipse](/ref/image.html#imageellipse) — 画一个椭圆
-   [imagefill](/ref/image.html#imagefill) — 区域填充
-   [imagefilledarc](/ref/image.html#imagefilledarc) — 画一椭圆弧且填充
-   [imagefilledellipse](/ref/image.html#imagefilledellipse) —
    画一椭圆并填充
-   [imagefilledpolygon](/ref/image.html#imagefilledpolygon) —
    画一多边形并填充
-   [imagefilledrectangle](/ref/image.html#imagefilledrectangle) —
    画一矩形并填充
-   [imagefilltoborder](/ref/image.html#imagefilltoborder) —
    区域填充到指定颜色的边界为止
-   [imagefilter](/ref/image.html#imagefilter) — 对图像使用过滤器
-   [imageflip](/ref/image.html#imageflip) — Flips an image using a
    given mode
-   [imagefontheight](/ref/image.html#imagefontheight) — 取得字体高度
-   [imagefontwidth](/ref/image.html#imagefontwidth) — 取得字体宽度
-   [imageftbbox](/ref/image.html#imageftbbox) — 给出一个使用 FreeType 2
    字体的文本框
-   [imagefttext](/ref/image.html#imagefttext) — 使用 FreeType 2
    字体将文本写入图像
-   [imagegammacorrect](/ref/image.html#imagegammacorrect) — 对 GD
    图像应用 gamma 修正
-   [imagegd2](/ref/image.html#imagegd2) — 将 GD2 图像输出到浏览器或文件
-   [imagegd](/ref/image.html#imagegd) — 将 GD 图像输出到浏览器或文件
-   [imagegetclip](/ref/image.html#imagegetclip) — Get the clipping
    rectangle
-   [imagegetinterpolation](/ref/image.html#imagegetinterpolation) — Get
    the interpolation method
-   [imagegif](/ref/image.html#imagegif) — 输出图象到浏览器或文件。
-   [imagegrabscreen](/ref/image.html#imagegrabscreen) — Captures the
    whole screen
-   [imagegrabwindow](/ref/image.html#imagegrabwindow) — Captures a
    window
-   [imageinterlace](/ref/image.html#imageinterlace) —
    激活或禁止隔行扫描
-   [imageistruecolor](/ref/image.html#imageistruecolor) —
    检查图像是否为真彩色图像
-   [imagejpeg](/ref/image.html#imagejpeg) — 输出图象到浏览器或文件。
-   [imagelayereffect](/ref/image.html#imagelayereffect) — 设定 alpha
    混色标志以使用绑定的 libgd 分层效果
-   [imageline](/ref/image.html#imageline) — 画一条线段
-   [imageloadfont](/ref/image.html#imageloadfont) — 载入一新字体
-   [imageopenpolygon](/ref/image.html#imageopenpolygon) — Draws an open
    polygon
-   [imagepalettecopy](/ref/image.html#imagepalettecopy) —
    将调色板从一幅图像拷贝到另一幅
-   [imagepalettetotruecolor](/ref/image.html#imagepalettetotruecolor) —
    Converts a palette based image to true color
-   [imagepng](/ref/image.html#imagepng) — 以 PNG
    格式将图像输出到浏览器或文件
-   [imagepolygon](/ref/image.html#imagepolygon) — 画一个多边形
-   [imagerectangle](/ref/image.html#imagerectangle) — 画一个矩形
-   [imageresolution](/ref/image.html#imageresolution) — Get or set the
    resolution of the image
-   [imagerotate](/ref/image.html#imagerotate) — 用给定角度旋转图像
-   [imagesavealpha](/ref/image.html#imagesavealpha) — 设置标记以在保存
    PNG 图像时保存完整的 alpha 通道信息（与单一透明色相反）
-   [imagescale](/ref/image.html#imagescale) — Scale an image using the
    given new width and height
-   [imagesetbrush](/ref/image.html#imagesetbrush) —
    设定画线用的画笔图像
-   [imagesetclip](/ref/image.html#imagesetclip) — Set the clipping
    rectangle
-   [imagesetinterpolation](/ref/image.html#imagesetinterpolation) — Set
    the interpolation method
-   [imagesetpixel](/ref/image.html#imagesetpixel) — 画一个单一像素
-   [imagesetstyle](/ref/image.html#imagesetstyle) — 设定画线的风格
-   [imagesetthickness](/ref/image.html#imagesetthickness) —
    设定画线的宽度
-   [imagesettile](/ref/image.html#imagesettile) — 设定用于填充的贴图
-   [imagestring](/ref/image.html#imagestring) — 水平地画一行字符串
-   [imagestringup](/ref/image.html#imagestringup) — 垂直地画一行字符串
-   [imagesx](/ref/image.html#imagesx) — 取得图像宽度
-   [imagesy](/ref/image.html#imagesy) — 取得图像高度
-   [imagetruecolortopalette](/ref/image.html#imagetruecolortopalette) —
    将真彩色图像转换为调色板图像
-   [imagettfbbox](/ref/image.html#imagettfbbox) — 取得使用 TrueType
    字体的文本的范围
-   [imagettftext](/ref/image.html#imagettftext) — 用 TrueType
    字体向图像写入文本
-   [imagetypes](/ref/image.html#imagetypes) — 返回当前 PHP
    版本所支持的图像类型
-   [imagewbmp](/ref/image.html#imagewbmp) — 以 WBMP
    格式将图像输出到浏览器或文件
-   [imagewebp](/ref/image.html#imagewebp) — 将 WebP
    格式的图像输出到浏览器或文件
-   [imagexbm](/ref/image.html#imagexbm) — 将 XBM 图像输出到浏览器或文件
-   [iptcembed](/ref/image.html#iptcembed) — 将二进制 IPTC
    数据嵌入到一幅 JPEG 图像中
-   [iptcparse](/ref/image.html#iptcparse) — 将二进制 IPTC
    块解析为单个标记
-   [jpeg2wbmp](/ref/image.html#jpeg2wbmp) — 将 JPEG 图像文件转换为 WBMP
    图像文件
-   [png2wbmp](/ref/image.html#png2wbmp) — 将 PNG 图像文件转换为 WBMP
    图像文件
