预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`GD_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> PHP 编译所依据的 GD 版本。 （PHP 5.2.4 可用）
</span>

**`GD_MAJOR_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 编译所依据的 GD 大版本。 （PHP 5.2.4 可用）
</span>

**`GD_MINOR_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 编译所依据的 GD 小版本。 （PHP 5.2.4 可用）
</span>

**`GD_RELEASE_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> PHP 编译所依据的 GD 发布版本。 （PHP 5.2.4 可用）
</span>

**`GD_EXTRA_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> PHP 编译所依据的 GD 扩展版本（beta/rc..）。 （PHP
5.2.4 可用） </span>

**`GD_BUNDLED`** (<span class="type">integer</span>)  
<span class="simpara"> 当使用绑定版本的 GD 时，此值为 1， 反之为 0。
</span>

**`IMG_BMP`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

**`IMG_GIF`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

**`IMG_JPG`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

**`IMG_JPEG`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

> **Note**:
>
> 本常量值同 **`IMG_JPG`**

**`IMG_PNG`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

**`IMG_WBMP`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

**`IMG_XPM`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span>

**`IMG_WEBP`** (<span class="type">integer</span>)  
<span class="simpara"> Used as a return value by <span
class="function">imagetypes</span> </span> <span class="simpara"> PHP
5.6.25 和 PHP 7.0.10 版本中都可用。 </span>

**`IMG_COLOR_TILED`** (<span class="type">integer</span>)  
<span class="simpara"> Special color option which can be used instead of
a color allocated with <span class="function">imagecolorallocate</span>
or <span class="function">imagecolorallocatealpha</span>. </span>

**`IMG_COLOR_STYLED`** (<span class="type">integer</span>)  
<span class="simpara"> Special color option which can be used instead of
a color allocated with <span class="function">imagecolorallocate</span>
or <span class="function">imagecolorallocatealpha</span>. </span>

**`IMG_COLOR_BRUSHED`** (<span class="type">integer</span>)  
<span class="simpara"> Special color option which can be used instead of
a color allocated with <span class="function">imagecolorallocate</span>
or <span class="function">imagecolorallocatealpha</span>. </span>

**`IMG_COLOR_STYLEDBRUSHED`** (<span class="type">integer</span>)  
<span class="simpara"> Special color option which can be used instead of
a color allocated with <span class="function">imagecolorallocate</span>
or <span class="function">imagecolorallocatealpha</span>. </span>

**`IMG_COLOR_TRANSPARENT`** (<span class="type">integer</span>)  
<span class="simpara"> Special color option which can be used instead of
a color allocated with <span class="function">imagecolorallocate</span>
or <span class="function">imagecolorallocatealpha</span>. </span>

**`IMG_AFFINE_TRANSLATE`** (<span class="type">integer</span>)  
<span class="simpara"> An affine transformation type constant used by
the <span class="function">imageaffinematrixget</span> function. </span>

**`IMG_AFFINE_SCALE`** (<span class="type">integer</span>)  
<span class="simpara"> An affine transformation type constant used by
the <span class="function">imageaffinematrixget</span> function. </span>

**`IMG_AFFINE_ROTATE`** (<span class="type">integer</span>)  
<span class="simpara"> An affine transformation type constant used by
the <span class="function">imageaffinematrixget</span> function. </span>

**`IMG_AFFINE_SHEAR_HORIZONTAL`** (<span class="type">integer</span>)  
<span class="simpara"> An affine transformation type constant used by
the <span class="function">imageaffinematrixget</span> function. </span>

**`IMG_AFFINE_SHEAR_VERTICAL`** (<span class="type">integer</span>)  
<span class="simpara"> An affine transformation type constant used by
the <span class="function">imageaffinematrixget</span> function. </span>

**`IMG_ARC_ROUNDED`** (<span class="type">integer</span>)  
<span class="simpara"> A style constant used by the <span
class="function">imagefilledarc</span> function. </span>

> **Note**:
>
> 此常量值同 **`IMG_ARC_PIE`**

**`IMG_ARC_PIE`** (<span class="type">integer</span>)  
<span class="simpara"> A style constant used by the <span
class="function">imagefilledarc</span> function. </span>

**`IMG_ARC_CHORD`** (<span class="type">integer</span>)  
<span class="simpara"> A style constant used by the <span
class="function">imagefilledarc</span> function. </span>

**`IMG_ARC_NOFILL`** (<span class="type">integer</span>)  
<span class="simpara"> A style constant used by the <span
class="function">imagefilledarc</span> function. </span>

**`IMG_ARC_EDGED`** (<span class="type">integer</span>)  
<span class="simpara"> A style constant used by the <span
class="function">imagefilledarc</span> function. </span>

**`IMG_GD2_RAW`** (<span class="type">integer</span>)  
<span class="simpara"> A type constant used by the <span
class="function">imagegd2</span> function. </span>

**`IMG_GD2_COMPRESSED`** (<span class="type">integer</span>)  
<span class="simpara"> A type constant used by the <span
class="function">imagegd2</span> function. </span>

**`IMG_EFFECT_REPLACE`** (<span class="type">integer</span>)  
<span class="simpara"> Alpha blending effect used by the <span
class="function">imagelayereffect</span> function. </span>

**`IMG_EFFECT_ALPHABLEND`** (<span class="type">integer</span>)  
<span class="simpara"> Alpha blending effect used by the <span
class="function">imagelayereffect</span> function. </span>

**`IMG_EFFECT_NORMAL`** (<span class="type">integer</span>)  
<span class="simpara"> Alpha blending effect used by the <span
class="function">imagelayereffect</span> function. </span>

**`IMG_EFFECT_OVERLAY`** (<span class="type">integer</span>)  
<span class="simpara"> Alpha blending effect used by the <span
class="function">imagelayereffect</span> function. </span>

**`IMG_EFFECT_MULTIPLY`** (<span class="type">integer</span>)  
<span class="simpara"> Alpha blending effect used by the <span
class="function">imagelayereffect</span> function. </span>

**`IMG_FILTER_NEGATE`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_GRAYSCALE`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_BRIGHTNESS`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_CONTRAST`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_COLORIZE`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_EDGEDETECT`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_GAUSSIAN_BLUR`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_SELECTIVE_BLUR`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_EMBOSS`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_MEAN_REMOVAL`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_SMOOTH`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span>

**`IMG_FILTER_PIXELATE`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span> <span
class="simpara"> （PHP 5.3.0 可用） </span>

**`IMG_FILTER_SCATTER`** (<span class="type">integer</span>)  
<span class="simpara"> Special GD filter used by the <span
class="function">imagefilter</span> function. </span> <span
class="simpara"> （自 PHP 7.4.0 版本可用） </span>

**`IMAGETYPE_GIF`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_JPEG`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_JPEG2000`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_PNG`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_SWF`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_PSD`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_BMP`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_WBMP`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_XBM`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_TIFF_II`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_TIFF_MM`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_IFF`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_JB2`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_JPC`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_JP2`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_JPX`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_SWC`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>

**`IMAGETYPE_ICO`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>
<span class="simpara"> (自 PHP 5.3.0 开始支持) </span>

**`IMAGETYPE_WEBP`** (<span class="type">integer</span>)  
<span class="simpara"> Image type constant used by the <span
class="function">image\_type\_to\_mime\_type</span> and <span
class="function">image\_type\_to\_extension</span> functions. </span>
<span class="simpara"> (从 PHP 7.1.0 开始支持) </span>

**`PNG_NO_FILTER`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`PNG_FILTER_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`PNG_FILTER_SUB`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`PNG_FILTER_UP`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`PNG_FILTER_AVG`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`PNG_FILTER_PAETH`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`PNG_ALL_FILTERS`** (<span class="type">integer</span>)  
<span class="simpara"> A special PNG filter, used by the <span
class="function">imagepng</span> function. </span>

**`IMG_FLIP_VERTICAL`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imageflip</span>, available as of PHP 5.5.0. </span>

**`IMG_FLIP_HORIZONTAL`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imageflip</span>, available as of PHP 5.5.0. </span>

**`IMG_FLIP_BOTH`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imageflip</span>, available as of PHP 5.5.0. </span>

**`IMG_BELL`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BESSEL`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BILINEAR_FIXED`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BICUBIC`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BICUBIC`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BLACKMAN`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BOX`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_BSPLINE`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_CATMULLROM`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_GAUSSIAN`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_GENERALIZED_CUBIC`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_HERMITE`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_HAMMING`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_HANNING`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_MITCHELL`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_POWER`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_QUADRATIC`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_SINC`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_NEAREST_NEIGHBOUR`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_WEIGHTED4`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>

**`IMG_TRIANGLE`** (<span class="type">int</span>)  
<span class="simpara"> Used together with <span
class="function">imagesetinterpolation</span>, available as of PHP
5.5.0. </span>
