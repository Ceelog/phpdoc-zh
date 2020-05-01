ming\_keypress
==============

Returns the action flag for keyPress(char)

### 说明

<span class="type">int</span> <span
class="methodname">ming\_keypress</span> ( <span
class="methodparam"><span class="type">string</span> `$char`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ming\_setcubicthreshold
=======================

Set cubic threshold

### 说明

<span class="type">void</span> <span
class="methodname">ming\_setcubicthreshold</span> ( <span
class="methodparam"><span class="type">int</span> `$threshold`</span> )

Sets the threshold error for drawing cubic beziers.

### 参数

`threshold`  
The Threshold. Lower is more accurate, hence larger file size.

### 返回值

没有返回值。

ming\_setscale
==============

Set the global scaling factor

### 说明

<span class="type">void</span> <span
class="methodname">ming\_setscale</span> ( <span
class="methodparam"><span class="type">float</span> `$scale`</span> )

Sets the scale of the output SWF. Inside the SWF file, coordinates are
measured in TWIPS, rather than PIXELS. There are 20 TWIPS in 1 pixel.

### 参数

`scale`  
The scale to be set.

### 返回值

没有返回值。

ming\_setswfcompression
=======================

Sets the SWF output compression

### 说明

<span class="type">void</span> <span
class="methodname">ming\_setswfcompression</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

Sets the SWF output compression level.

### 参数

`level`  
The new compression level. Should be a value between 1 and 9 inclusive.

### 返回值

没有返回值。

ming\_useconstants
==================

Use constant pool

### 说明

<span class="type">void</span> <span
class="methodname">ming\_useconstants</span> ( <span
class="methodparam"><span class="type">int</span> `$use`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

ming\_useswfversion
===================

Sets the SWF version

### 说明

<span class="type">void</span> <span
class="methodname">ming\_useswfversion</span> ( <span
class="methodparam"><span class="type">int</span> `$version`</span> )

Sets the SWF version to be used in the movie. This affect the bahaviour
of Action Script.

### 参数

`version`  
SWF version to use.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">ming\_useswfversion</span> example**

``` php
<?php

$movie = new SWFMovie();
ming_useswfversion(4); // Flash 4

?>
```

**目录**

-   [ming\_keypress](/ref/ming.html#ming_keypress) — Returns the action
    flag for keyPress(char)
-   [ming\_setcubicthreshold](/ref/ming.html#ming_setcubicthreshold) —
    Set cubic threshold
-   [ming\_setscale](/ref/ming.html#ming_setscale) — Set the global
    scaling factor
-   [ming\_setswfcompression](/ref/ming.html#ming_setswfcompression) —
    Sets the SWF output compression
-   [ming\_useconstants](/ref/ming.html#ming_useconstants) — Use
    constant pool
-   [ming\_useswfversion](/ref/ming.html#ming_useswfversion) — Sets the
    SWF version
