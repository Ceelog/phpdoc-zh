预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`imagick::COLOR_BLACK`** (<span class="type">int</span>)  
<span class="simpara"> Black color </span>

**`imagick::COLOR_BLUE`** (<span class="type">int</span>)  
<span class="simpara"> Blue color </span>

**`imagick::COLOR_CYAN`** (<span class="type">int</span>)  
<span class="simpara"> Cyan color </span>

**`imagick::COLOR_GREEN`** (<span class="type">int</span>)  
<span class="simpara"> Green color </span>

**`imagick::COLOR_RED`** (<span class="type">int</span>)  
<span class="simpara"> Red color </span>

**`imagick::COLOR_YELLOW`** (<span class="type">int</span>)  
<span class="simpara"> Yellow color </span>

**`imagick::COLOR_MAGENTA`** (<span class="type">int</span>)  
<span class="simpara"> Magenta color </span>

**`imagick::COLOR_OPACITY`** (<span class="type">int</span>)  
<span class="simpara"> Color's opacity </span>

**`imagick::COLOR_ALPHA`** (<span class="type">int</span>)  
<span class="simpara"> Color's alpha </span>

**`imagick::COLOR_FUZZ`** (<span class="type">int</span>)  
<span class="simpara"> Color's fuzz </span>

<!-- -->

**`imagick::DISPOSE_UNRECOGNIZED`** (<span class="type">int</span>)  
<span class="simpara"> Unrecognized dispose type </span>

**`imagick::DISPOSE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> Undefined dispose type </span>

**`imagick::DISPOSE_NONE`** (<span class="type">int</span>)  
<span class="simpara"> No dispose type defined </span>

**`imagick::DISPOSE_BACKGROUND`** (<span class="type">int</span>)  
<span class="simpara"> Dispose background </span>

**`imagick::DISPOSE_PREVIOUS`** (<span class="type">int</span>)  
<span class="simpara"> Dispose previous </span>

<!-- -->

**`imagick::COMPOSITE_DEFAULT`** (<span class="type">int</span>)  
<span class="simpara"> The default composite operator </span>

**`imagick::COMPOSITE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> Undefined composite operator </span>

**`imagick::COMPOSITE_NO`** (<span class="type">int</span>)  
<span class="simpara"> No composite operator defined </span>

**`imagick::COMPOSITE_ADD`** (<span class="type">int</span>)  
<span class="simpara"> The result of image + image </span>

**`imagick::COMPOSITE_ATOP`** (<span class="type">int</span>)  
<span class="simpara"> The result is the same shape as image, with
composite image obscuring image where the image shapes overlap </span>

**`imagick::COMPOSITE_BLEND`** (<span class="type">int</span>)  
<span class="simpara"> Blends the image </span>

**`imagick::COMPOSITE_BUMPMAP`** (<span class="type">int</span>)  
<span class="simpara"> The same as COMPOSITE\_MULTIPLY, except the
source is converted to grayscale first. </span>

**`imagick::COMPOSITE_CLEAR`** (<span class="type">int</span>)  
<span class="simpara"> Makes the target image transparent </span>

**`imagick::COMPOSITE_COLORBURN`** (<span class="type">int</span>)  
<span class="simpara"> Darkens the destination image to reflect the
source image </span>

**`imagick::COMPOSITE_COLORDODGE`** (<span class="type">int</span>)  
<span class="simpara"> Brightens the destination image to reflect the
source image </span>

**`imagick::COMPOSITE_COLORIZE`** (<span class="type">int</span>)  
<span class="simpara"> Colorizes the target image using the composite
image </span>

**`imagick::COMPOSITE_COPYBLACK`** (<span class="type">int</span>)  
<span class="simpara"> Copies black from the source to target </span>

**`imagick::COMPOSITE_COPYBLUE`** (<span class="type">int</span>)  
<span class="simpara"> Copies blue from the source to target </span>

**`imagick::COMPOSITE_COPY`** (<span class="type">int</span>)  
<span class="simpara"> Copies the source image on the target image
</span>

**`imagick::COMPOSITE_COPYCYAN`** (<span class="type">int</span>)  
<span class="simpara"> Copies cyan from the source to target </span>

**`imagick::COMPOSITE_COPYGREEN`** (<span class="type">int</span>)  
<span class="simpara"> Copies green from the source to target </span>

**`imagick::COMPOSITE_COPYMAGENTA`** (<span class="type">int</span>)  
<span class="simpara"> Copies magenta from the source to target </span>

**`imagick::COMPOSITE_COPYOPACITY`** (<span class="type">int</span>)  
<span class="simpara"> Copies opacity from the source to target </span>

**`imagick::COMPOSITE_COPYRED`** (<span class="type">int</span>)  
<span class="simpara"> Copies red from the source to target </span>

**`imagick::COMPOSITE_COPYYELLOW`** (<span class="type">int</span>)  
<span class="simpara"> Copies yellow from the source to target </span>

**`imagick::COMPOSITE_DARKEN`** (<span class="type">int</span>)  
<span class="simpara"> Darkens the target image </span>

**`imagick::COMPOSITE_DSTATOP`** (<span class="type">int</span>)  
<span class="simpara"> The part of the destination lying inside of the
source is composited over the source and replaces the destination
</span>

**`imagick::COMPOSITE_DST`** (<span class="type">int</span>)  
<span class="simpara"> The target is left untouched </span>

**`imagick::COMPOSITE_DSTIN`** (<span class="type">int</span>)  
<span class="simpara"> The parts inside the source replace the target
</span>

**`imagick::COMPOSITE_DSTOUT`** (<span class="type">int</span>)  
<span class="simpara"> The parts outside the source replace the target
</span>

**`imagick::COMPOSITE_DSTOVER`** (<span class="type">int</span>)  
<span class="simpara"> Target replaces the source </span>

**`imagick::COMPOSITE_DIFFERENCE`** (<span class="type">int</span>)  
<span class="simpara"> Subtracts the darker of the two constituent
colors from the lighter </span>

**`imagick::COMPOSITE_DISPLACE`** (<span class="type">int</span>)  
<span class="simpara"> Shifts target image pixels as defined by the
source </span>

**`imagick::COMPOSITE_DISSOLVE`** (<span class="type">int</span>)  
<span class="simpara"> Dissolves the source in to the target </span>

**`imagick::COMPOSITE_EXCLUSION`** (<span class="type">int</span>)  
<span class="simpara"> Produces an effect similar to that of
imagick::COMPOSITE\_DIFFERENCE, but appears as lower contrast </span>

**`imagick::COMPOSITE_HARDLIGHT`** (<span class="type">int</span>)  
<span class="simpara"> Multiplies or screens the colors, dependent on
the source color value </span>

**`imagick::COMPOSITE_HUE`** (<span class="type">int</span>)  
<span class="simpara"> Modifies the hue of the target as defined by
source </span>

**`imagick::COMPOSITE_IN`** (<span class="type">int</span>)  
<span class="simpara"> Composites source into the target </span>

**`imagick::COMPOSITE_LIGHTEN`** (<span class="type">int</span>)  
<span class="simpara"> Lightens the target as defined by source </span>

**`imagick::COMPOSITE_LUMINIZE`** (<span class="type">int</span>)  
<span class="simpara"> Luminizes the target as defined by source </span>

**`imagick::COMPOSITE_MINUS`** (<span class="type">int</span>)  
<span class="simpara"> Subtracts the source from the target </span>

**`imagick::COMPOSITE_MODULATE`** (<span class="type">int</span>)  
<span class="simpara"> Modulates the target brightness, saturation and
hue as defined by source </span>

**`imagick::COMPOSITE_MULTIPLY`** (<span class="type">int</span>)  
<span class="simpara"> Multiplies the target to the source </span>

**`imagick::COMPOSITE_OUT`** (<span class="type">int</span>)  
<span class="simpara"> Composites outer parts of the source on the
target </span>

**`imagick::COMPOSITE_OVER`** (<span class="type">int</span>)  
<span class="simpara"> Composites source over the target </span>

**`imagick::COMPOSITE_OVERLAY`** (<span class="type">int</span>)  
<span class="simpara"> Overlays the source on the target </span>

**`imagick::COMPOSITE_PLUS`** (<span class="type">int</span>)  
<span class="simpara"> Adds the source to the target </span>

**`imagick::COMPOSITE_REPLACE`** (<span class="type">int</span>)  
<span class="simpara"> Replaces the target with the source </span>

**`imagick::COMPOSITE_SATURATE`** (<span class="type">int</span>)  
<span class="simpara"> Saturates the target as defined by the source
</span>

**`imagick::COMPOSITE_SCREEN`** (<span class="type">int</span>)  
<span class="simpara"> The source and destination are complemented and
then multiplied and then replace the destination </span>

**`imagick::COMPOSITE_SOFTLIGHT`** (<span class="type">int</span>)  
<span class="simpara"> Darkens or lightens the colors, dependent on the
source </span>

**`imagick::COMPOSITE_SRCATOP`** (<span class="type">int</span>)  
<span class="simpara"> The part of the source lying inside of the
destination is composited onto the destination </span>

**`imagick::COMPOSITE_SRC`** (<span class="type">int</span>)  
<span class="simpara"> The source is copied to the destination </span>

**`imagick::COMPOSITE_SRCIN`** (<span class="type">int</span>)  
<span class="simpara"> The part of the source lying inside of the
destination replaces the destination </span>

**`imagick::COMPOSITE_SRCOUT`** (<span class="type">int</span>)  
<span class="simpara"> The part of the source lying outside of the
destination replaces the destination </span>

**`imagick::COMPOSITE_SRCOVER`** (<span class="type">int</span>)  
<span class="simpara"> The source replaces the destination </span>

**`imagick::COMPOSITE_SUBTRACT`** (<span class="type">int</span>)  
<span class="simpara"> Subtract the colors in the source image from the
destination image </span>

**`imagick::COMPOSITE_THRESHOLD`** (<span class="type">int</span>)  
<span class="simpara"> The source is composited on the target as defined
by source threshold </span>

**`imagick::COMPOSITE_XOR`** (<span class="type">int</span>)  
<span class="simpara"> The part of the source that lies outside of the
destination is combined with the part of the destination that lies
outside of the source </span>

<!-- -->

**`imagick::MONTAGEMODE_FRAME`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::MONTAGEMODE_UNFRAME`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::MONTAGEMODE_CONCATENATE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::STYLE_NORMAL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STYLE_ITALIC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STYLE_OBLIQUE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STYLE_ANY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::FILTER_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_POINT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_BOX`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_TRIANGLE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_HERMITE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_HANNING`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_HAMMING`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_BLACKMAN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_GAUSSIAN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_QUADRATIC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_CUBIC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_CATROM`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_MITCHELL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_LANCZOS`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_BESSEL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILTER_SINC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::IMGTYPE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_BILEVEL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_GRAYSCALE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_GRAYSCALEMATTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_PALETTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_PALETTEMATTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_TRUECOLOR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_TRUECOLORMATTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_COLORSEPARATION`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_COLORSEPARATIONMATTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::IMGTYPE_OPTIMIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::RESOLUTION_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RESOLUTION_PIXELSPERINCH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RESOLUTION_PIXELSPERCENTIMETER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::COMPRESSION_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_NO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_BZIP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_FAX`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_GROUP4`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_JPEG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_JPEG2000`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_LOSSLESSJPEG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_LZW`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_RLE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_ZIP`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COMPRESSION_DXT1`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.0
or higher. </span>

**`imagick::COMPRESSION_DXT3`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.0
or higher. </span>

**`imagick::COMPRESSION_DXT5`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.0
or higher. </span>

<!-- -->

**`imagick::PAINT_POINT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PAINT_REPLACE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PAINT_FLOODFILL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PAINT_FILLTOBORDER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PAINT_RESET`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::GRAVITY_NORTHWEST`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_NORTH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_NORTHEAST`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_WEST`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_CENTER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_EAST`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_SOUTHWEST`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_SOUTH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::GRAVITY_SOUTHEAST`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::STRETCH_NORMAL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_ULTRACONDENSED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_CONDENSED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_SEMICONDENSED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_SEMIEXPANDED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_EXPANDED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_EXTRAEXPANDED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_ULTRAEXPANDED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::STRETCH_ANY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::ALIGN_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::ALIGN_LEFT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::ALIGN_CENTER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::ALIGN_RIGHT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::DECORATION_NO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::DECORATION_UNDERLINE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::DECORATION_OVERLINE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::DECORATION_LINETROUGH`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::NOISE_UNIFORM`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::NOISE_GAUSSIAN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::NOISE_MULTIPLICATIVEGAUSSIAN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::NOISE_IMPULSE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::NOISE_LAPLACIAN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::NOISE_POISSON`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::NOISE_RANDOM`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

<!-- -->

**`imagick::CHANNEL_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_RED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_GRAY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_CYAN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_GREEN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_MAGENTA`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_BLUE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_YELLOW`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_ALPHA`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_OPACITY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_MATTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_BLACK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_INDEX`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_ALL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::CHANNEL_DEFAULT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::METRIC_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::METRIC_MEANABSOLUTEERROR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::METRIC_MEANSQUAREERROR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::METRIC_PEAKABSOLUTEERROR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::METRIC_PEAKSIGNALTONOISERATIO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::METRIC_ROOTMEANSQUAREDERROR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::PIXEL_CHAR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PIXEL_DOUBLE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PIXEL_FLOAT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PIXEL_INTEGER`** (<span class="type">int</span>)  
<span class="simpara"> Only available for ImageMagick \< 7. </span>

**`imagick::PIXEL_LONG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PIXEL_QUANTUM`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PIXEL_SHORT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::EVALUATE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_ADD`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_AND`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_DIVIDE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_LEFTSHIFT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_MAX`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_MIN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_MULTIPLY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_OR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_RIGHTSHIFT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_SET`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_SUBTRACT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_XOR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::EVALUATE_POW`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_LOG`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_THRESHOLD`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_THRESHOLDBLACK`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_THRESHOLDWHITE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_GAUSSIANNOISE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_IMPULSENOISE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_LAPLACIANNOISE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_MULTIPLICATIVENOISE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_POISSONNOISE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_UNIFORMNOISE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_COSINE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_SINE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

**`imagick::EVALUATE_ADDMODULUS`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.4
or higher. </span>

<!-- -->

**`imagick::COLORSPACE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_RGB`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_GRAY`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_TRANSPARENT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_OHTA`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_LAB`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_XYZ`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_YCBCR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_YCC`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_YIQ`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_YPBPR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_YUV`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_CMYK`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_SRGB`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_HSB`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_HSL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_HWB`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_REC601LUMA`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_REC709LUMA`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_LOG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::COLORSPACE_CMY`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.2
or higher. </span>

<!-- -->

**`imagick::VIRTUALPIXELMETHOD_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_BACKGROUND`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_CONSTANT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_EDGE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_MIRROR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_TILE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_TRANSPARENT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::VIRTUALPIXELMETHOD_MASK`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.2
or higher. </span>

**`imagick::VIRTUALPIXELMETHOD_BLACK`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.2
or higher. </span>

**`imagick::VIRTUALPIXELMETHOD_GRAY`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.2
or higher. </span>

**`imagick::VIRTUALPIXELMETHOD_WHITE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.2
or higher. </span>

**`imagick::VIRTUALPIXELMETHOD_HORIZONTALTILE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.3
or higher. </span>

**`imagick::VIRTUALPIXELMETHOD_VERTICALTILE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.3
or higher. </span>

<!-- -->

**`imagick::PREVIEW_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_ROTATE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SHEAR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_ROLL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_HUE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SATURATION`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_BRIGHTNESS`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_GAMMA`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SPIFF`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_DULL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_GRAYSCALE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_QUANTIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_DESPECKLE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_REDUCENOISE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_ADDNOISE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SHARPEN`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_BLUR`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_THRESHOLD`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_EDGEDETECT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SPREAD`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SOLARIZE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SHADE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_RAISE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SEGMENT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_SWIRL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_IMPLODE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_WAVE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_OILPAINT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_CHARCOALDRAWING`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PREVIEW_JPEG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::RENDERINGINTENT_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RENDERINGINTENT_SATURATION`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RENDERINGINTENT_PERCEPTUAL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RENDERINGINTENT_ABSOLUTE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RENDERINGINTENT_RELATIVE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::INTERLACE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::INTERLACE_NO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::INTERLACE_LINE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::INTERLACE_PLANE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::INTERLACE_PARTITION`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::INTERLACE_GIF`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.4
or higher. </span>

**`imagick::INTERLACE_JPEG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::INTERLACE_PNG`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::FILLRULE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILLRULE_EVENODD`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::FILLRULE_NONZERO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::PATHUNITS_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PATHUNITS_USERSPACE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PATHUNITS_USERSPACEONUSE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::PATHUNITS_OBJECTBOUNDINGBOX`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::LINECAP_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::LINECAP_BUTT`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::LINECAP_ROUND`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::LINECAP_SQUARE`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::LINEJOIN_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::LINEJOIN_MITER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::LINEJOIN_ROUND`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::LINEJOIN_BEVEL`** (<span class="type">int</span>)  
<span class="simpara"> </span>

<!-- -->

**`imagick::RESOURCETYPE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`imagick::RESOURCETYPE_AREA`** (<span class="type">int</span>)  
<span class="simpara"> Set the maximum width \* height of an image that
can reside in the pixel cache memory. </span>

**`imagick::RESOURCETYPE_DISK`** (<span class="type">int</span>)  
<span class="simpara"> Set maximum amount of disk space in bytes
permitted for use by the pixel cache. </span>

**`imagick::RESOURCETYPE_FILE`** (<span class="type">int</span>)  
<span class="simpara"> Set maximum number of open pixel cache files.
</span>

**`imagick::RESOURCETYPE_MAP`** (<span class="type">int</span>)  
<span class="simpara"> Set maximum amount of memory map in bytes to
allocate for the pixel cache. </span>

**`imagick::RESOURCETYPE_MEMORY`** (<span class="type">int</span>)  
<span class="simpara"> Set maximum amount of memory in bytes to allocate
for the pixel cache from the heap. </span>

**`imagick::RESOURCETYPE_THREAD`** (<span class="type">int</span>)  
<span class="simpara"> Set maximum parallel threads.
此常量可用仅当Imagick编译于ImageMagick版本 6.7.8 or higher. </span>

<!-- -->

**`imagick::LAYERMETHOD_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_COALESCE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_COMPAREANY`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_COMPARECLEAR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_COMPAREOVERLAY`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_DISPOSE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_OPTIMIZE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_OPTIMIZEPLUS`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.2.9
or higher. </span>

**`imagick::LAYERMETHOD_OPTIMIZEIMAGE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::LAYERMETHOD_OPTIMIZETRANS`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::LAYERMETHOD_REMOVEDUPS`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::LAYERMETHOD_REMOVEZERO`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::LAYERMETHOD_COMPOSITE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::LAYERMETHOD_MERGE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.7
or higher. </span>

**`imagick::LAYERMETHOD_FLATTEN`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.7
or higher. </span>

**`imagick::LAYERMETHOD_MOSAIC`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.7
or higher. </span>

<!-- -->

**`imagick::ORIENTATION_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_TOPLEFT`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_TOPRIGHT`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_BOTTOMRIGHT`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_BOTTOMLEFT`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_LEFTTOP`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_RIGHTTOP`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_RIGHTBOTTOM`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

**`imagick::ORIENTATION_LEFTBOTTOM`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.0
or higher. </span>

<!-- -->

**`imagick::DISTORTION_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_AFFINE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_AFFINEPROJECTION`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_ARC`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_BILINEAR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_PERSPECTIVE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_PERSPECTIVEPROJECTION`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_SCALEROTATETRANSLATE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.6
or higher. </span>

**`imagick::DISTORTION_POLYNOMIAL`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DISTORTION_POLAR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DISTORTION_DEPOLAR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DISTORTION_BARREL`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DISTORTION_BARRELINVERSE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DISTORTION_SHEPARDS`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DISTORTION_SENTINEL`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

<!-- -->

**`imagick::ALPHACHANNEL_ACTIVATE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.8
or higher. </span>

**`imagick::ALPHACHANNEL_DEACTIVATE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.8
or higher. </span>

**`imagick::ALPHACHANNEL_RESET`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.8
or higher. </span>

**`imagick::ALPHACHANNEL_SET`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.8
or higher. </span>

**`imagick::ALPHACHANNEL_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::ALPHACHANNEL_COPY`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::ALPHACHANNEL_EXTRACT`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::ALPHACHANNEL_OPAQUE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::ALPHACHANNEL_SHAPE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::ALPHACHANNEL_TRANSPARENT`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

<!-- -->

**`imagick::SPARSECOLORMETHOD_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::SPARSECOLORMETHOD_BARYCENTRIC`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::SPARSECOLORMETHOD_BILINEAR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::SPARSECOLORMETHOD_POLYNOMIAL`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::SPARSECOLORMETHOD_SPEPARDS`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::SPARSECOLORMETHOD_VORONOI`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

<!-- -->

**`imagick::FUNCTION_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.9
or higher. </span>

**`imagick::FUNCTION_POLYNOMIAL`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.9
or higher. </span>

**`imagick::FUNCTION_SINUSOID`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.9
or higher. </span>

<!-- -->

**`imagick::INTERPOLATE_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_AVERAGE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_BICUBIC`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_BILINEAR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_FILTER`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_INTEGER`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_MESH`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_NEARESTNEIGHBOR`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.2
or higher. </span>

**`imagick::INTERPOLATE_SPLINE`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.3.4
or higher. </span>

<!-- -->

**`imagick::DITHERMETHOD_UNDEFINED`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DITHERMETHOD_NO`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DITHERMETHOD_RIEMERSMA`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>

**`imagick::DITHERMETHOD_FLOYDSTEINBERG`** (<span class="type">int</span>)  
<span class="simpara"> 此常量可用仅当Imagick编译于ImageMagick版本 6.4.6
or higher. </span>
