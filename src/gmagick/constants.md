预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`Gmagick::COLOR_BLACK`** (<span class="type">integer</span>)  
<span class="simpara"> Black </span>

**`Gmagick::COLOR_BLUE`** (<span class="type">integer</span>)  
<span class="simpara"> Blue </span>

**`Gmagick::COLOR_CYAN`** (<span class="type">integer</span>)  
<span class="simpara"> Cyan </span>

**`Gmagick::COLOR_GREEN`** (<span class="type">integer</span>)  
<span class="simpara"> Green </span>

**`Gmagick::COLOR_RED`** (<span class="type">integer</span>)  
<span class="simpara"> Red </span>

**`Gmagick::COLOR_YELLOW`** (<span class="type">integer</span>)  
<span class="simpara"> Yellow </span>

**`Gmagick::COLOR_MAGENTA`** (<span class="type">integer</span>)  
<span class="simpara"> Magenta </span>

**`Gmagick::COLOR_OPACITY`** (<span class="type">integer</span>)  
<span class="simpara"> Opacity </span>

**`Gmagick::COLOR_ALPHA`** (<span class="type">integer</span>)  
<span class="simpara"> Alpha </span>

**`Gmagick::COLOR_FUZZ`** (<span class="type">integer</span>)  
<span class="simpara"> Fuzz </span>

<!-- -->

**`Gmagick::COMPOSITE_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> The default composite operator </span>

**`Gmagick::COMPOSITE_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> Undefined composite operator </span>

**`Gmagick::COMPOSITE_NO`** (<span class="type">integer</span>)  
<span class="simpara"> No composite operator defined </span>

**`Gmagick::COMPOSITE_ADD`** (<span class="type">integer</span>)  
<span class="simpara"> The result of image + image </span>

**`Gmagick::COMPOSITE_ATOP`** (<span class="type">integer</span>)  
<span class="simpara"> The result is the same shape as image, with
composite image obscuring image where the image shapes overlap </span>

**`Gmagick::COMPOSITE_BLEND`** (<span class="type">integer</span>)  
<span class="simpara"> Blends the image </span>

**`Gmagick::COMPOSITE_BUMPMAP`** (<span class="type">integer</span>)  
<span class="simpara"> The same as COMPOSITE\_MULTIPLY, except the
source is converted to grayscale first. </span>

**`Gmagick::COMPOSITE_CLEAR`** (<span class="type">integer</span>)  
<span class="simpara"> Makes the target image transparent </span>

**`Gmagick::COMPOSITE_COLORBURN`** (<span class="type">integer</span>)  
<span class="simpara"> Darkens the destination image to reflect the
source image </span>

**`Gmagick::COMPOSITE_COLORDODGE`** (<span class="type">integer</span>)  
<span class="simpara"> Brightens the destination image to reflect the
source image </span>

**`Gmagick::COMPOSITE_COLORIZE`** (<span class="type">integer</span>)  
<span class="simpara"> Colorizes the target image using the composite
image </span>

**`Gmagick::COMPOSITE_COPYBLACK`** (<span class="type">integer</span>)  
<span class="simpara"> Copies black from the source to target </span>

**`Gmagick::COMPOSITE_COPYBLUE`** (<span class="type">integer</span>)  
<span class="simpara"> Copies blue from the source to target </span>

**`Gmagick::COMPOSITE_COPY`** (<span class="type">integer</span>)  
<span class="simpara"> Copies the source image on the target image
</span>

**`Gmagick::COMPOSITE_COPYCYAN`** (<span class="type">integer</span>)  
<span class="simpara"> Copies cyan from the source to target </span>

**`Gmagick::COMPOSITE_COPYGREEN`** (<span class="type">integer</span>)  
<span class="simpara"> Copies green from the source to target </span>

**`Gmagick::COMPOSITE_COPYMAGENTA`** (<span class="type">integer</span>)  
<span class="simpara"> Copies magenta from the source to target </span>

**`Gmagick::COMPOSITE_COPYOPACITY`** (<span class="type">integer</span>)  
<span class="simpara"> Copies opacity from the source to target </span>

**`Gmagick::COMPOSITE_COPYRED`** (<span class="type">integer</span>)  
<span class="simpara"> Copies red from the source to target </span>

**`Gmagick::COMPOSITE_COPYYELLOW`** (<span class="type">integer</span>)  
<span class="simpara"> Copies yellow from the source to target </span>

**`Gmagick::COMPOSITE_DARKEN`** (<span class="type">integer</span>)  
<span class="simpara"> Darkens the target image </span>

**`Gmagick::COMPOSITE_DSTATOP`** (<span class="type">integer</span>)  
<span class="simpara"> The part of the destination lying inside of the
source is composited over the source and replaces the destination
</span>

**`Gmagick::COMPOSITE_DST`** (<span class="type">integer</span>)  
<span class="simpara"> The target is left untouched </span>

**`Gmagick::COMPOSITE_DSTIN`** (<span class="type">integer</span>)  
<span class="simpara"> The parts inside the source replace the target
</span>

**`Gmagick::COMPOSITE_DSTOUT`** (<span class="type">integer</span>)  
<span class="simpara"> The parts outside the source replace the target
</span>

**`Gmagick::COMPOSITE_DSTOVER`** (<span class="type">integer</span>)  
<span class="simpara"> Target replaces the source </span>

**`Gmagick::COMPOSITE_DIFFERENCE`** (<span class="type">integer</span>)  
<span class="simpara"> Subtracts the darker of the two constituent
colors from the lighter </span>

**`Gmagick::COMPOSITE_DISPLACE`** (<span class="type">integer</span>)  
<span class="simpara"> Shifts target image pixels as defined by the
source </span>

**`Gmagick::COMPOSITE_DISSOLVE`** (<span class="type">integer</span>)  
<span class="simpara"> Dissolves the source in to the target </span>

**`Gmagick::COMPOSITE_EXCLUSION`** (<span class="type">integer</span>)  
<span class="simpara"> Produces an effect similar to that of
Gmagick::COMPOSITE\_DIFFERENCE, but appears as lower contrast </span>

**`Gmagick::COMPOSITE_HARDLIGHT`** (<span class="type">integer</span>)  
<span class="simpara"> Multiplies or screens the colors, dependent on
the source color value </span>

**`Gmagick::COMPOSITE_HUE`** (<span class="type">integer</span>)  
<span class="simpara"> Modifies the hue of the target as defined by
source </span>

**`Gmagick::COMPOSITE_IN`** (<span class="type">integer</span>)  
<span class="simpara"> Composites source into the target </span>

**`Gmagick::COMPOSITE_LIGHTEN`** (<span class="type">integer</span>)  
<span class="simpara"> Lightens the target as defined by source </span>

**`Gmagick::COMPOSITE_LUMINIZE`** (<span class="type">integer</span>)  
<span class="simpara"> Luminizes the target as defined by source </span>

**`Gmagick::COMPOSITE_MINUS`** (<span class="type">integer</span>)  
<span class="simpara"> Subtracts the source from the target </span>

**`Gmagick::COMPOSITE_MODULATE`** (<span class="type">integer</span>)  
<span class="simpara"> Modulates the target brightness, saturation and
hue as defined by source </span>

**`Gmagick::COMPOSITE_MULTIPLY`** (<span class="type">integer</span>)  
<span class="simpara"> Multiplies the target to the source </span>

**`Gmagick::COMPOSITE_OUT`** (<span class="type">integer</span>)  
<span class="simpara"> Composites outer parts of the source on the
target </span>

**`Gmagick::COMPOSITE_OVER`** (<span class="type">integer</span>)  
<span class="simpara"> Composites source over the target </span>

**`Gmagick::COMPOSITE_OVERLAY`** (<span class="type">integer</span>)  
<span class="simpara"> Overlays the source on the target </span>

**`Gmagick::COMPOSITE_PLUS`** (<span class="type">integer</span>)  
<span class="simpara"> Adds the source to the target </span>

**`Gmagick::COMPOSITE_REPLACE`** (<span class="type">integer</span>)  
<span class="simpara"> Replaces the target with the source </span>

**`Gmagick::COMPOSITE_SATURATE`** (<span class="type">integer</span>)  
<span class="simpara"> Saturates the target as defined by the source
</span>

**`Gmagick::COMPOSITE_SCREEN`** (<span class="type">integer</span>)  
<span class="simpara"> The source and destination are complemented and
then multiplied and then replace the destination </span>

**`Gmagick::COMPOSITE_SOFTLIGHT`** (<span class="type">integer</span>)  
<span class="simpara"> Darkens or lightens the colors, dependent on the
source </span>

**`Gmagick::COMPOSITE_SRCATOP`** (<span class="type">integer</span>)  
<span class="simpara"> The part of the source lying inside of the
destination is composited onto the destination </span>

**`Gmagick::COMPOSITE_SRC`** (<span class="type">integer</span>)  
<span class="simpara"> The source is copied to the destination </span>

**`Gmagick::COMPOSITE_SRCIN`** (<span class="type">integer</span>)  
<span class="simpara"> The part of the source lying inside of the
destination replaces the destination </span>

**`Gmagick::COMPOSITE_SRCOUT`** (<span class="type">integer</span>)  
<span class="simpara"> The part of the source lying outside of the
destination replaces the destination </span>

**`Gmagick::COMPOSITE_SRCOVER`** (<span class="type">integer</span>)  
<span class="simpara"> The source replaces the destination </span>

**`Gmagick::COMPOSITE_SUBTRACT`** (<span class="type">integer</span>)  
<span class="simpara"> Subtract the colors in the source image from the
destination image </span>

**`Gmagick::COMPOSITE_THRESHOLD`** (<span class="type">integer</span>)  
<span class="simpara"> The source is composited on the target as defined
by source threshold </span>

**`Gmagick::COMPOSITE_XOR`** (<span class="type">integer</span>)  
<span class="simpara"> The part of the source that lies outside of the
destination is combined with the part of the destination that lies
outside of the source </span>

<!-- -->

**`Gmagick::MONTAGEMODE_FRAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::MONTAGEMODE_UNFRAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::MONTAGEMODE_CONCATENATE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::STYLE_NORMAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STYLE_ITALIC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STYLE_OBLIQUE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STYLE_ANY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::FILTER_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_POINT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_BOX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_TRIANGLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_HERMITE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_HANNING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_HAMMING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_BLACKMAN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_GAUSSIAN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_QUADRATIC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_CUBIC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_CATROM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_MITCHELL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_LANCZOS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_BESSEL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILTER_SINC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::IMGTYPE_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_BILEVEL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_GRAYSCALE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_GRAYSCALEMATTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_PALETTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_PALETTEMATTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_TRUECOLOR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_TRUECOLORMATTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_COLORSEPARATION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_COLORSEPARATIONMATTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::IMGTYPE_OPTIMIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::RESOLUTION_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOLUTION_PIXELSPERINCH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOLUTION_PIXELSPERCENTIMETER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::COMPRESSION_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_NO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_BZIP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_FAX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_GROUP4`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_JPEG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_JPEG2000`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_LOSSLESSJPEG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_LZW`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_RLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COMPRESSION_ZIP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::PAINT_POINT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PAINT_REPLACE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PAINT_FLOODFILL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PAINT_FILLTOBORDER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PAINT_RESET`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::GRAVITY_NORTHWEST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_NORTH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_NORTHEAST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_WEST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_CENTER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_EAST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_SOUTHWEST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_SOUTH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::GRAVITY_SOUTHEAST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::STRETCH_NORMAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_ULTRACONDENSED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_CONDENSED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_SEMICONDENSED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_SEMIEXPANDED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_EXPANDED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_EXTRAEXPANDED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_ULTRAEXPANDED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::STRETCH_ANY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::ALIGN_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ALIGN_LEFT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ALIGN_CENTER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ALIGN_RIGHT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::DECORATION_NO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::DECORATION_UNDERLINE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::DECORATION_OVERLINE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::DECORATION_LINETROUGH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::NOISE_UNIFORM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::NOISE_GAUSSIAN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::NOISE_MULTIPLICATIVEGAUSSIAN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::NOISE_IMPULSE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::NOISE_LAPLACIAN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::NOISE_POISSON`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::CHANNEL_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_RED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_GRAY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_CYAN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_GREEN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_MAGENTA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_BLUE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_YELLOW`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_ALPHA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_OPACITY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_MATTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_BLACK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_INDEX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::CHANNEL_ALL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::METRIC_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::METRIC_MEANABSOLUTEERROR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::METRIC_MEANSQUAREERROR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::METRIC_PEAKABSOLUTEERROR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::METRIC_PEAKSIGNALTONOISERATIO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::METRIC_ROOTMEANSQUAREDERROR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::PIXEL_CHAR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PIXEL_DOUBLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PIXEL_FLOAT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PIXEL_INTEGER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PIXEL_LONG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PIXEL_QUANTUM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PIXEL_SHORT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::COLORSPACE_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_RGB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_GRAY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_TRANSPARENT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_OHTA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_LAB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_XYZ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_YCBCR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_YCC`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_YIQ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_YPBPR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_YUV`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_CMYK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_SRGB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_HSB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_HSL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_HWB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_REC601LUMA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_REC709LUMA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::COLORSPACE_LOG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::VIRTUALPIXELMETHOD_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::VIRTUALPIXELMETHOD_BACKGROUND`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::VIRTUALPIXELMETHOD_CONSTANT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::VIRTUALPIXELMETHOD_EDGE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::VIRTUALPIXELMETHOD_MIRROR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::VIRTUALPIXELMETHOD_TILE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::VIRTUALPIXELMETHOD_TRANSPARENT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::PREVIEW_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_ROTATE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SHEAR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_ROLL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_HUE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SATURATION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_BRIGHTNESS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_GAMMA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SPIFF`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_DULL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_GRAYSCALE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_QUANTIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_DESPECKLE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_REDUCENOISE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_ADDNOISE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SHARPEN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_BLUR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_THRESHOLD`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_EDGEDETECT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SPREAD`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SOLARIZE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SHADE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_RAISE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SEGMENT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_SWIRL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_IMPLODE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_WAVE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_OILPAINT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_CHARCOALDRAWING`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PREVIEW_JPEG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::RENDERINGINTENT_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RENDERINGINTENT_SATURATION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RENDERINGINTENT_PERCEPTUAL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RENDERINGINTENT_ABSOLUTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RENDERINGINTENT_RELATIVE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::FILLRULE_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILLRULE_EVENODD`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::FILLRULE_NONZERO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::PATHUNITS_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PATHUNITS_USERSPACE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PATHUNITS_USERSPACEONUSE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::PATHUNITS_OBJECTBOUNDINGBOX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::LINECAP_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::LINECAP_BUTT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::LINECAP_ROUND`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::LINECAP_SQUARE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::LINEJOIN_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::LINEJOIN_MITER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::LINEJOIN_ROUND`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::LINEJOIN_BEVEL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::RESOURCETYPE_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOURCETYPE_AREA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOURCETYPE_DISK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOURCETYPE_FILE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOURCETYPE_MAP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::RESOURCETYPE_MEMORY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

<!-- -->

**`Gmagick::ORIENTATION_UNDEFINED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_TOPLEFT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_TOPRIGHT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_BOTTOMRIGHT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_BOTTOMLEFT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_LEFTTOP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_RIGHTTOP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_RIGHTBOTTOM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`Gmagick::ORIENTATION_LEFTBOTTOM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>
