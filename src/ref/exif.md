exif\_imagetype
===============

判断一个图像的类型

### 说明

<span class="type">int</span> <span
class="methodname">exif\_imagetype</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">exif\_imagetype</span>
读取一个图像的第一个字节并检查其签名。

本函数可用来避免调用其它 <a href="/ref/exif.html" class="link">exif</a>
函数用到了不支持的文件类型上或和 `$_SERVER['HTTP_ACCEPT']`
结合使用来检查浏览器是否可以显示某个指定的图像。

### 参数

`filename`  
<span class="simpara"> 被检查的图像文件名。 </span>

### 返回值

如果发现了恰当的签名则返回一个对应的常量，否则返回 **`false`**。返回值和
<span class="function">getimagesize</span> 返回的数组中的索引 2
的值是一样的，但本函数快得多。

### 更新日志

| 版本  | 说明                                   |
|-------|----------------------------------------|
| 4.3.2 | 支持 JPC，JP2，JPX，JB2，XBM 以及 WBMP |
| 4.3.0 | 支持 SWC                               |

### 预定义常量

定义有以下常量，并代表了 <span class="function">exif\_imagetype</span>
可能的返回值：

| 值  | 常量                                         |
|-----|----------------------------------------------|
| 1   | **`IMAGETYPE_GIF`**                          |
| 2   | **`IMAGETYPE_JPEG`**                         |
| 3   | **`IMAGETYPE_PNG`**                          |
| 4   | **`IMAGETYPE_SWF`**                          |
| 5   | **`IMAGETYPE_PSD`**                          |
| 6   | **`IMAGETYPE_BMP`**                          |
| 7   | **`IMAGETYPE_TIFF_II`**（Intel 字节顺序）    |
| 8   | **`IMAGETYPE_TIFF_MM`**（Motorola 字节顺序） |
| 9   | **`IMAGETYPE_JPC`**                          |
| 10  | **`IMAGETYPE_JP2`**                          |
| 11  | **`IMAGETYPE_JPX`**                          |
| 12  | **`IMAGETYPE_JB2`**                          |
| 13  | **`IMAGETYPE_SWC`**                          |
| 14  | **`IMAGETYPE_IFF`**                          |
| 15  | **`IMAGETYPE_WBMP`**                         |
| 16  | **`IMAGETYPE_XBM`**                          |

### 范例

**示例 \#1 <span class="function">exif\_imagetype</span> 例子**

``` php
<?php

if (exif_imagetype("image.gif") != IMAGETYPE_GIF) {
    echo "The picture is not a gif";
}

?>
```

### 参见

-   <span class="function">getimagesize</span>

exif\_read\_data
================

从 JPEG 或 TIFF 文件中读取 EXIF 头信息

### 说明

<span class="type">array</span> <span
class="methodname">exif\_read\_data</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$sections`<span class="initializer"> = **`null`**</span></span> \[,
<span class="methodparam"><span class="type">bool</span> `$arrays`<span
class="initializer"> = false</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$thumbnail`<span
class="initializer"> = false</span></span> \]\]\] )

<span class="function">exif\_read\_data</span> 函数从 JPEG 或 TIFF
图像文件中读取 EXIF 头信息。这样就可以读取数码相机产生的元数据。

EXIF 头信息往往存在于数码相机生成的 JPEG/TIFF
图像中，但不幸的是每个数码相机制造商的标记都不同，因此（编写代码时）不能依赖于某个特定的
Exif 头信息。

Height 和 Width 是用和 <span class="function">getimagesize</span>
一样的方法计算的，因此它们的值不能是任何返回的头信息的部分。此外 html
是一个 height/width 的文本字符串可以用于普通的 HTML 中。

当一个 Exif 头信息包含有一个 Copyright
时注意它本身可以包含两个值。解决方案和 Exif 2.10 标准不一致，COMPUTED
区段会同时返回 Copyright.Photographer 和 Copyright.Editor，但是 IFD0
区段则包含有一个字节数组用 NULL
字符分隔开两个项目。或者只有第一项如果数据类型错误的话（Exif
的正常行为）。COMPUTED 也会包含
Copyright，要么是原始的版权字符串，要么是逗号分隔的摄像与编辑的版权信息。

UserComment 标记和 Copyright
有同样的问题。它也可以存储两个值，第一个是使用的编码方式，第二个是其值本身。如果这样则
IFD0 区段仅包含编码方式或者一个字节数组。COMPUTED 区段将存储两个值到
UserCommentEncoding 和 UserComment。UserComment
在两种情况下都可用因此应该优先使用它而不是 IFD0 区段中的该值。

<span class="function">exif\_read\_data</span> 还会根据 EXIF
规范（<a href="http://exif.org/Exif2-2.PDF" class="link external">» http://exif.org/Exif2-2.PDF</a>，第
20 页）来验证 EXIF 数据。

> **Note**:
>
> Windows ME/XP 在连接到数码相机时能清除掉 Exif 头信息。

### 参数

`filename`  
被读取的图像文件名。不能是 URL。

`sections`  
是需要存在于文件中的逗号分隔的区段列表用来产生结果数组。如果未找到所请求的区段则返回值为
**`false`**。

|           |                                                                                                                                                                                                                                                  |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILE      | FileName, FileSize, FileDateTime, SectionsFound                                                                                                                                                                                                  |
| COMPUTED  | html，Width，Height，IsColor，可能有更多其它的。Height 和 Width 是用和 <span class="function">getimagesize</span> 一样的方法计算的，因此它们的值不能是任何返回的头信息的部分。此外 html 是一个 height/width 的文本字符串可以用于普通的 HTML 中。 |
| ANY\_TAG  | 任何包含有标记的信息，例如 IFD0，EXIF，...                                                                                                                                                                                                       |
| IFD0      | 所有 IFD0 的标记数据。在标准的图像文件中这包含了图像大小及其它。                                                                                                                                                                                 |
| THUMBNAIL | 如果有第二个 IFD，文件应该包含有缩略图。所有有关嵌入缩略图的标记信息都存储在本区。                                                                                                                                                               |
| COMMENT   | JPEG 图像的注释头信息。                                                                                                                                                                                                                          |
| EXIF      | EXIF 区段是 IFDO 的子区，包含有图像的更多详细信息。大多数内容都是数码相机相关的。                                                                                                                                                                |

`arrays`  
指定了是否每个区段都成为一个数组。`sections` *COMPUTED*，*THUMBNAIL*
和*COMMENT* 区段总是成为数组，因为它们里面包含的名字和其它区段冲突。

`thumbnail`  
当设定为 **`true`** 时，读取缩略图本身。否则只读取标记数据。

### 返回值

返回一个关联数组，键名是头信息名，值为与其相应的值。如果没有可供返回的数据，<span
class="function">exif\_read\_data</span> 将返回 **`false`**。

### 更新日志

| 版本  | 说明                                                                                                                                                                                                                                             |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.3.0 | 可以读取所有嵌入的 IFD 数据，包括数组（也返回数组）。此外嵌入的缩略图的大小包括在 THUMBNAIL 子数组中并且 <span class="function">exif\_read\_data</span> 可以将缩略图按照 TIFF 格式返回。最后，不再有返回值最大长度的限制了（直到达到内存限定）。 |
| 4.3.0 | 如果 PHP 有 <a href="/ref/mbstring.html" class="link">mbstring</a> 支持，则用户注释可以自动改变编码。此外，如果用户注释使用 Unicode 或 JIS 编码，将会根据 EXIF 在 `php.ini` 中的 设置被自动改变。                                                |
| 4.3.0 | 如果图像包含任何 IFD0 数据，则 COMPUTED 会包含有一项 ByteOrderMotorola，对于 little-endian (intel) 字节顺序，其值为 0，对于 big-endian (motorola) 字节顺序，其值为 1。此外，COMPUTED 和 UserComment 在数据类型出错时也不再仅包含第一个版权条目。 |

### 范例

**示例 \#1 <span class="function">exif\_read\_data</span> 例子**

``` php
<?php
echo "test1.jpg:<br />\n";
$exif = exif_read_data('tests/test1.jpg', 'IFD0');
echo $exif===false ? "No header data found.<br />\n" : "Image contains headers<br />\n";

$exif = exif_read_data('tests/test2.jpg', 0, true);
echo "test2.jpg:<br />\n";
foreach ($exif as $key => $section) {
    foreach ($section as $name => $val) {
        echo "$key.$name: $val<br />\n";
    }
}
?>
```

第一个调用失败了，因为图像没有头信息。

以上例程的输出类似于：

    test1.jpg:
    No header data found.
    test2.jpg:
    FILE.FileName: test2.jpg
    FILE.FileDateTime: 1017666176
    FILE.FileSize: 1240
    FILE.FileType: 2
    FILE.SectionsFound: ANY_TAG, IFD0, THUMBNAIL, COMMENT
    COMPUTED.html: width="1" height="1"
    COMPUTED.Height: 1
    COMPUTED.Width: 1
    COMPUTED.IsColor: 1
    COMPUTED.ByteOrderMotorola: 1
    COMPUTED.UserComment: Exif test image.
    COMPUTED.UserCommentEncoding: ASCII
    COMPUTED.Copyright: Photo (c) M.Boerger, Edited by M.Boerger.
    COMPUTED.Copyright.Photographer: Photo (c) M.Boerger
    COMPUTED.Copyright.Editor: Edited by M.Boerger.
    IFD0.Copyright: Photo (c) M.Boerger
    IFD0.UserComment: ASCII
    THUMBNAIL.JPEGInterchangeFormat: 134
    THUMBNAIL.JPEGInterchangeFormatLength: 523
    COMMENT.0: Comment #1.
    COMMENT.1: Comment #2.
    COMMENT.2: Comment #3end
    THUMBNAIL.JPEGInterchangeFormat: 134
    THUMBNAIL.Thumbnail.Height: 1
    THUMBNAIL.Thumbnail.Height: 1

### 参见

-   <span class="function">exif\_thumbnail</span>
-   <span class="function">getimagesize</span>

exif\_tagname
=============

获取指定索引的头名称

### 说明

<span class="type">string</span> <span
class="methodname">exif\_tagname</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

### 参数

`index`  
要查找的标签名称的 ID。

### 返回值

返回头名称。 如果 `index` 参数不是预定义的 EXIF 标签 id，则返回
**`false`**

### 范例

**示例 \#1 <span class="function">exif\_tagname</span> 函数例程**

``` php
<?php
echo "256: ".exif_tagname(256).PHP_EOL;
echo "257: ".exif_tagname(257).PHP_EOL;
?>
```

以上例程会输出：

    256: ImageWidth
    257: ImageLength

### 参见

-   <span class="function">exif\_imagetype</span>
-   <a href="http://exif.org/Exif2-2.PDF" class="link external">» EXIF 规范</a>
-   <a href="http://www.sno.phy.queensu.ca/~phil/exiftool/TagNames/EXIF.html" class="link external">» EXIF 标签</a>

exif\_thumbnail
===============

取得嵌入在 TIFF 或 JPEG 图像中的缩略图

### 说明

<span class="type">string</span> <span
class="methodname">exif\_thumbnail</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`&$width`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$height`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$imagetype`</span>
\]\]\] )

<span class="function">exif\_thumbnail</span> 读取 TIFF 或 JPEG
图像中的嵌入缩略图。如果图像不包含缩略图则返回 **`false`**。

If you want to deliver thumbnails through this function, you should send
the mimetype information using the <span class="function">header</span>
function.

It is possible that <span class="function">exif\_thumbnail</span> cannot
create an image but can determine its size. In this case, the return
value is **`false`** but `width` and `height` are set.

### 参数

`filename`  
The name of the image file being read. This image contains an embedded
thumbnail.

`width`  
The return width of the returned thumbnail.

`height`  
The returned height of the returned thumbnail.

`imagetype`  
The returned image type of the returned thumbnail. This is either TIFF
or JPEG.

### 返回值

Returns the embedded thumbnail, or **`false`** if the image contains no
thumbnail.

### 更新日志

| 版本  | 说明                                                                             |
|-------|----------------------------------------------------------------------------------|
| 4.3.0 | The optional parameters `width`, `height`, and `imagetype` all became available. |
| 4.3.0 | May return thumbnails in the TIFF format.                                        |

### 范例

**示例 \#1 <span class="function">exif\_thumbnail</span> 例子**

``` php
<?php
if (array_key_exists('file',$_REQUEST)) {
    $image = exif_thumbnail($_REQUEST['file'], $width, $height, $type);
} else {
    $image = false;
}
if ($image!==false) {
    header("Content-type: ".image_type_to_mime_type($type));
    echo $image;
    exit;
} else {
    // no thumbnail available, handle the error here
    echo "No thumbnail available";
}
?>
```

### 参见

-   <span class="function">exif\_read\_data</span>
-   <span class="function">image\_type\_to\_mime\_type</span>

read\_exif\_data
================

别名 <span class="function">exif\_read\_data</span>

### 说明

此函数是该函数的别名： <span class="function">exif\_read\_data</span>.

**目录**

-   [exif\_imagetype](/ref/exif.html#exif_imagetype) —
    判断一个图像的类型
-   [exif\_read\_data](/ref/exif.html#exif_read_data) — 从 JPEG 或 TIFF
    文件中读取 EXIF 头信息
-   [exif\_tagname](/ref/exif.html#exif_tagname) — 获取指定索引的头名称
-   [exif\_thumbnail](/ref/exif.html#exif_thumbnail) — 取得嵌入在 TIFF
    或 JPEG 图像中的缩略图
-   [read\_exif\_data](/ref/exif.html#read_exif_data) — 别名
    exif\_read\_data
