Ming (flash)
============

**目录**

-   [简介](/intro/ming.html)
-   [安装／配置](/ming/setup.html)
    -   [需求](/ming/setup.html#需求)
    -   [安装](/ming/setup.html#安装)
    -   [运行时配置](/ming/setup.html#运行时配置)
    -   [资源类型](/ming/setup.html#资源类型)
-   [预定义常量](/ming/constants.html)
-   [范例](/ming/examples.html)
    -   [SWFAction Examples](/ming/examples.html#SWFAction%20Examples)
    -   [SWFSPrite basic
        examples](/ming/examples.html#SWFSPrite%20basic%20examples)
-   [Ming 函数](/ref/ming.html)
    -   [ming\_keypress](/ref/ming.html#ming_keypress) — Returns the
        action flag for keyPress(char)
    -   [ming\_setcubicthreshold](/ref/ming.html#ming_setcubicthreshold)
        — Set cubic threshold
    -   [ming\_setscale](/ref/ming.html#ming_setscale) — Set the global
        scaling factor
    -   [ming\_setswfcompression](/ref/ming.html#ming_setswfcompression)
        — Sets the SWF output compression
    -   [ming\_useconstants](/ref/ming.html#ming_useconstants) — Use
        constant pool
    -   [ming\_useswfversion](/ref/ming.html#ming_useswfversion) — Sets
        the SWF version
-   [SWFAction](/class/swfaction.html) — The SWFAction class
    -   [SWFAction::\_\_construct](/class/swfaction.html#SWFAction::__construct)
        — Creates a new SWFAction
-   [SWFBitmap](/class/swfbitmap.html) — The SWFBitmap class
    -   [SWFBitmap::\_\_construct](/class/swfbitmap.html#SWFBitmap::__construct)
        — Loads Bitmap object
    -   [SWFBitmap::getHeight](/class/swfbitmap.html#SWFBitmap::getHeight)
        — Returns the bitmap's height
    -   [SWFBitmap::getWidth](/class/swfbitmap.html#SWFBitmap::getWidth)
        — Returns the bitmap's width
-   [SWFButton](/class/swfbutton.html) — The SWFButton class
    -   [SWFButton::addAction](/class/swfbutton.html#SWFButton::addAction)
        — Adds an action
    -   [SWFButton::addASound](/class/swfbutton.html#SWFButton::addASound)
        — Associates a sound with a button transition
    -   [SWFButton::addShape](/class/swfbutton.html#SWFButton::addShape)
        — Adds a shape to a button
    -   [SWFButton::\_\_construct](/class/swfbutton.html#SWFButton::__construct)
        — Creates a new Button
    -   [SWFButton::setAction](/class/swfbutton.html#SWFButton::setAction)
        — Sets the action
    -   [SWFButton::setDown](/class/swfbutton.html#SWFButton::setDown) —
        Alias for addShape(shape, SWFBUTTON\_DOWN)
    -   [SWFButton::setHit](/class/swfbutton.html#SWFButton::setHit) —
        Alias for addShape(shape, SWFBUTTON\_HIT)
    -   [SWFButton::setMenu](/class/swfbutton.html#SWFButton::setMenu) —
        Enable track as menu button behaviour
    -   [SWFButton::setOver](/class/swfbutton.html#SWFButton::setOver) —
        Alias for addShape(shape, SWFBUTTON\_OVER)
    -   [SWFButton::setUp](/class/swfbutton.html#SWFButton::setUp) —
        Alias for addShape(shape, SWFBUTTON\_UP)
-   [SWFDisplayItem](/class/swfdisplayitem.html) — The SWFDisplayItem
    class
    -   [SWFDisplayItem::addAction](/class/swfdisplayitem.html#SWFDisplayItem::addAction)
        — Adds this SWFAction to the given SWFSprite instance
    -   [SWFDisplayItem::addColor](/class/swfdisplayitem.html#SWFDisplayItem::addColor)
        — Adds the given color to this item's color transform
    -   [SWFDisplayItem::endMask](/class/swfdisplayitem.html#SWFDisplayItem::endMask)
        — Another way of defining a MASK layer
    -   [SWFDisplayItem::getRot](/class/swfdisplayitem.html#SWFDisplayItem::getRot)
        — 说明
    -   [SWFDisplayItem::getX](/class/swfdisplayitem.html#SWFDisplayItem::getX)
        — 说明
    -   [SWFDisplayItem::getXScale](/class/swfdisplayitem.html#SWFDisplayItem::getXScale)
        — 说明
    -   [SWFDisplayItem::getXSkew](/class/swfdisplayitem.html#SWFDisplayItem::getXSkew)
        — 说明
    -   [SWFDisplayItem::getY](/class/swfdisplayitem.html#SWFDisplayItem::getY)
        — 说明
    -   [SWFDisplayItem::getYScale](/class/swfdisplayitem.html#SWFDisplayItem::getYScale)
        — 说明
    -   [SWFDisplayItem::getYSkew](/class/swfdisplayitem.html#SWFDisplayItem::getYSkew)
        — 说明
    -   [SWFDisplayItem::move](/class/swfdisplayitem.html#SWFDisplayItem::move)
        — Moves object in relative coordinates
    -   [SWFDisplayItem::moveTo](/class/swfdisplayitem.html#SWFDisplayItem::moveTo)
        — Moves object in global coordinates
    -   [SWFDisplayItem::multColor](/class/swfdisplayitem.html#SWFDisplayItem::multColor)
        — Multiplies the item's color transform
    -   [SWFDisplayItem::remove](/class/swfdisplayitem.html#SWFDisplayItem::remove)
        — Removes the object from the movie
    -   [SWFDisplayItem::rotate](/class/swfdisplayitem.html#SWFDisplayItem::rotate)
        — Rotates in relative coordinates
    -   [SWFDisplayItem::rotateTo](/class/swfdisplayitem.html#SWFDisplayItem::rotateTo)
        — Rotates the object in global coordinates
    -   [SWFDisplayItem::scale](/class/swfdisplayitem.html#SWFDisplayItem::scale)
        — Scales the object in relative coordinates
    -   [SWFDisplayItem::scaleTo](/class/swfdisplayitem.html#SWFDisplayItem::scaleTo)
        — Scales the object in global coordinates
    -   [SWFDisplayItem::setDepth](/class/swfdisplayitem.html#SWFDisplayItem::setDepth)
        — Sets z-order
    -   [SWFDisplayItem::setMaskLevel](/class/swfdisplayitem.html#SWFDisplayItem::setMaskLevel)
        — Defines a MASK layer at level
    -   [SWFDisplayItem::setMatrix](/class/swfdisplayitem.html#SWFDisplayItem::setMatrix)
        — Sets the item's transform matrix
    -   [SWFDisplayItem::setName](/class/swfdisplayitem.html#SWFDisplayItem::setName)
        — Sets the object's name
    -   [SWFDisplayItem::setRatio](/class/swfdisplayitem.html#SWFDisplayItem::setRatio)
        — Sets the object's ratio
    -   [SWFDisplayItem::skewX](/class/swfdisplayitem.html#SWFDisplayItem::skewX)
        — Sets the X-skew
    -   [SWFDisplayItem::skewXTo](/class/swfdisplayitem.html#SWFDisplayItem::skewXTo)
        — Sets the X-skew
    -   [SWFDisplayItem::skewY](/class/swfdisplayitem.html#SWFDisplayItem::skewY)
        — Sets the Y-skew
    -   [SWFDisplayItem::skewYTo](/class/swfdisplayitem.html#SWFDisplayItem::skewYTo)
        — Sets the Y-skew
-   [SWFFill](/class/swffill.html) — The SWFFill class
    -   [SWFFill::moveTo](/class/swffill.html#SWFFill::moveTo) — Moves
        fill origin
    -   [SWFFill::rotateTo](/class/swffill.html#SWFFill::rotateTo) —
        Sets fill's rotation
    -   [SWFFill::scaleTo](/class/swffill.html#SWFFill::scaleTo) — Sets
        fill's scale
    -   [SWFFill::skewXTo](/class/swffill.html#SWFFill::skewXTo) — Sets
        fill x-skew
    -   [SWFFill::skewYTo](/class/swffill.html#SWFFill::skewYTo) — Sets
        fill y-skew
-   [SWFFont](/class/swffont.html) — The SWFFont class
    -   [SWFFont::\_\_construct](/class/swffont.html#SWFFont::__construct)
        — Loads a font definition
    -   [SWFFont::getAscent](/class/swffont.html#SWFFont::getAscent) —
        Returns the ascent of the font, or 0 if not available
    -   [SWFFont::getDescent](/class/swffont.html#SWFFont::getDescent) —
        Returns the descent of the font, or 0 if not available
    -   [SWFFont::getLeading](/class/swffont.html#SWFFont::getLeading) —
        Returns the leading of the font, or 0 if not available
    -   [SWFFont::getShape](/class/swffont.html#SWFFont::getShape) —
        Returns the glyph shape of a char as a text string
    -   [SWFFont::getUTF8Width](/class/swffont.html#SWFFont::getUTF8Width)
        — Calculates the width of the given string in this font at full
        height
    -   [SWFFont::getWidth](/class/swffont.html#SWFFont::getWidth) —
        Returns the string's width
-   [SWFFontChar](/class/swffontchar.html) — The SWFFontChar class
    -   [SWFFontChar::addChars](/class/swffontchar.html#SWFFontChar::addChars)
        — Adds characters to a font for exporting font
    -   [SWFFontChar::addUTF8Chars](/class/swffontchar.html#SWFFontChar::addUTF8Chars)
        — Adds characters to a font for exporting font
-   [SWFGradient](/class/swfgradient.html) — The SWFGradient class
    -   [SWFGradient::addEntry](/class/swfgradient.html#SWFGradient::addEntry)
        — Adds an entry to the gradient list
    -   [SWFGradient::\_\_construct](/class/swfgradient.html#SWFGradient::__construct)
        — Creates a gradient object
-   [SWFMorph](/class/swfmorph.html) — The SWFMorph class
    -   [SWFMorph::\_\_construct](/class/swfmorph.html#SWFMorph::__construct)
        — Creates a new SWFMorph object
    -   [SWFMorph::getShape1](/class/swfmorph.html#SWFMorph::getShape1)
        — Gets a handle to the starting shape
    -   [SWFMorph::getShape2](/class/swfmorph.html#SWFMorph::getShape2)
        — Gets a handle to the ending shape
-   [SWFMovie](/class/swfmovie.html) — The SWFMovie class
    -   [SWFMovie::add](/class/swfmovie.html#SWFMovie::add) — Adds any
        type of data to a movie
    -   [SWFMovie::addExport](/class/swfmovie.html#SWFMovie::addExport)
        — 说明
    -   [SWFMovie::addFont](/class/swfmovie.html#SWFMovie::addFont) —
        说明
    -   [SWFMovie::\_\_construct](/class/swfmovie.html#SWFMovie::__construct)
        — Creates a new movie object, representing an SWF version 4
        movie
    -   [SWFMovie::importChar](/class/swfmovie.html#SWFMovie::importChar)
        — 说明
    -   [SWFMovie::importFont](/class/swfmovie.html#SWFMovie::importFont)
        — 说明
    -   [SWFMovie::labelFrame](/class/swfmovie.html#SWFMovie::labelFrame)
        — Labels a frame
    -   [SWFMovie::nextFrame](/class/swfmovie.html#SWFMovie::nextFrame)
        — Moves to the next frame of the animation
    -   [SWFMovie::output](/class/swfmovie.html#SWFMovie::output) —
        Dumps your lovingly prepared movie out
    -   [SWFMovie::remove](/class/swfmovie.html#SWFMovie::remove) —
        Removes the object instance from the display list
    -   [SWFMovie::save](/class/swfmovie.html#SWFMovie::save) — Saves
        the SWF movie in a file
    -   [SWFMovie::saveToFile](/class/swfmovie.html#SWFMovie::saveToFile)
        — 说明
    -   [SWFMovie::setbackground](/class/swfmovie.html#SWFMovie::setbackground)
        — Sets the background color
    -   [SWFMovie::setDimension](/class/swfmovie.html#SWFMovie::setDimension)
        — Sets the movie's width and height
    -   [SWFMovie::setFrames](/class/swfmovie.html#SWFMovie::setFrames)
        — Sets the total number of frames in the animation
    -   [SWFMovie::setRate](/class/swfmovie.html#SWFMovie::setRate) —
        Sets the animation's frame rate
    -   [SWFMovie::startSound](/class/swfmovie.html#SWFMovie::startSound)
        — 说明
    -   [SWFMovie::stopSound](/class/swfmovie.html#SWFMovie::stopSound)
        — 说明
    -   [SWFMovie::streamMP3](/class/swfmovie.html#SWFMovie::streamMP3)
        — Streams a MP3 file
    -   [SWFMovie::writeExports](/class/swfmovie.html#SWFMovie::writeExports)
        — 说明
-   [SWFPrebuiltClip](/class/swfprebuiltclip.html) — The SWFPrebuiltClip
    class
    -   [SWFPrebuiltClip::\_\_construct](/class/swfprebuiltclip.html#SWFPrebuiltClip::__construct)
        — Returns a SWFPrebuiltClip object
-   [SWFShape](/class/swfshape.html) — The SWFShape class
    -   [SWFShape::addFill](/class/swfshape.html#SWFShape::addFill) —
        Adds a solid fill to the shape
    -   [SWFShape::\_\_construct](/class/swfshape.html#SWFShape::__construct)
        — Creates a new shape object
    -   [SWFShape::drawArc](/class/swfshape.html#SWFShape::drawArc) —
        Draws an arc of radius r centered at the current location, from
        angle startAngle to angle endAngle measured clockwise from 12
        o'clock
    -   [SWFShape::drawCircle](/class/swfshape.html#SWFShape::drawCircle)
        — Draws a circle of radius r centered at the current location,
        in a counter-clockwise fashion
    -   [SWFShape::drawCubic](/class/swfshape.html#SWFShape::drawCubic)
        — Draws a cubic bezier curve using the current position and the
        three given points as control points
    -   [SWFShape::drawCubicTo](/class/swfshape.html#SWFShape::drawCubicTo)
        — Draws a cubic bezier curve using the current position and the
        three given points as control points
    -   [SWFShape::drawCurve](/class/swfshape.html#SWFShape::drawCurve)
        — Draws a curve (relative)
    -   [SWFShape::drawCurveTo](/class/swfshape.html#SWFShape::drawCurveTo)
        — Draws a curve
    -   [SWFShape::drawGlyph](/class/swfshape.html#SWFShape::drawGlyph)
        — Draws the first character in the given string into the shape
        using the glyph definition from the given font
    -   [SWFShape::drawLine](/class/swfshape.html#SWFShape::drawLine) —
        Draws a line (relative)
    -   [SWFShape::drawLineTo](/class/swfshape.html#SWFShape::drawLineTo)
        — Draws a line
    -   [SWFShape::movePen](/class/swfshape.html#SWFShape::movePen) —
        Moves the shape's pen (relative)
    -   [SWFShape::movePenTo](/class/swfshape.html#SWFShape::movePenTo)
        — Moves the shape's pen
    -   [SWFShape::setLeftFill](/class/swfshape.html#SWFShape::setLeftFill)
        — Sets left rasterizing color
    -   [SWFShape::setLine](/class/swfshape.html#SWFShape::setLine) —
        Sets the shape's line style
    -   [SWFShape::setRightFill](/class/swfshape.html#SWFShape::setRightFill)
        — Sets right rasterizing color
-   [SWFSound](/class/swfsound.html) — The SWFSound class
    -   [SWFSound::\_\_construct](/class/swfsound.html#SWFSound::__construct)
        — Returns a new SWFSound object from given file
-   [SWFSoundInstance](/class/swfsoundinstance.html) — The
    SWFSoundInstance class
    -   [SWFSoundInstance::loopCount](/class/swfsoundinstance.html#SWFSoundInstance::loopCount)
        — 说明
    -   [SWFSoundInstance::loopInPoint](/class/swfsoundinstance.html#SWFSoundInstance::loopInPoint)
        — 说明
    -   [SWFSoundInstance::loopOutPoint](/class/swfsoundinstance.html#SWFSoundInstance::loopOutPoint)
        — 说明
    -   [SWFSoundInstance::noMultiple](/class/swfsoundinstance.html#SWFSoundInstance::noMultiple)
        — 说明
-   [SWFSprite](/class/swfsprite.html) — The SWFSprite class
    -   [SWFSprite::add](/class/swfsprite.html#SWFSprite::add) — Adds an
        object to a sprite
    -   [SWFSprite::\_\_construct](/class/swfsprite.html#SWFSprite::__construct)
        — Creates a movie clip (a sprite)
    -   [SWFSprite::labelFrame](/class/swfsprite.html#SWFSprite::labelFrame)
        — Labels frame
    -   [SWFSprite::nextFrame](/class/swfsprite.html#SWFSprite::nextFrame)
        — Moves to the next frame of the animation
    -   [SWFSprite::remove](/class/swfsprite.html#SWFSprite::remove) —
        Removes an object to a sprite
    -   [SWFSprite::setFrames](/class/swfsprite.html#SWFSprite::setFrames)
        — Sets the total number of frames in the animation
    -   [SWFSprite::startSound](/class/swfsprite.html#SWFSprite::startSound)
        — 说明
    -   [SWFSprite::stopSound](/class/swfsprite.html#SWFSprite::stopSound)
        — 说明
-   [SWFText](/class/swftext.html) — The SWFText class
    -   [SWFText::addString](/class/swftext.html#SWFText::addString) —
        Draws a string
    -   [SWFText::addUTF8String](/class/swftext.html#SWFText::addUTF8String)
        — Writes the given text into this SWFText object at the current
        pen position, using the current font, height, spacing, and color
    -   [SWFText::\_\_construct](/class/swftext.html#SWFText::__construct)
        — Creates a new SWFText object
    -   [SWFText::getAscent](/class/swftext.html#SWFText::getAscent) —
        Returns the ascent of the current font at its current size, or 0
        if not available
    -   [SWFText::getDescent](/class/swftext.html#SWFText::getDescent) —
        Returns the descent of the current font at its current size, or
        0 if not available
    -   [SWFText::getLeading](/class/swftext.html#SWFText::getLeading) —
        Returns the leading of the current font at its current size, or
        0 if not available
    -   [SWFText::getUTF8Width](/class/swftext.html#SWFText::getUTF8Width)
        — Calculates the width of the given string in this text objects
        current font and size
    -   [SWFText::getWidth](/class/swftext.html#SWFText::getWidth) —
        Computes string's width
    -   [SWFText::moveTo](/class/swftext.html#SWFText::moveTo) — Moves
        the pen
    -   [SWFText::setColor](/class/swftext.html#SWFText::setColor) —
        Sets the current text color
    -   [SWFText::setFont](/class/swftext.html#SWFText::setFont) — Sets
        the current font
    -   [SWFText::setHeight](/class/swftext.html#SWFText::setHeight) —
        Sets the current font height
    -   [SWFText::setSpacing](/class/swftext.html#SWFText::setSpacing) —
        Sets the current font spacing
-   [SWFTextField](/class/swftextfield.html) — The SWFTextField class
    -   [SWFTextField::addChars](/class/swftextfield.html#SWFTextField::addChars)
        — Adds characters to a font that will be available within a
        textfield
    -   [SWFTextField::addString](/class/swftextfield.html#SWFTextField::addString)
        — Concatenates the given string to the text field
    -   [SWFTextField::align](/class/swftextfield.html#SWFTextField::align)
        — Sets the text field alignment
    -   [SWFTextField::\_\_construct](/class/swftextfield.html#SWFTextField::__construct)
        — Creates a text field object
    -   [SWFTextField::setBounds](/class/swftextfield.html#SWFTextField::setBounds)
        — Sets the text field width and height
    -   [SWFTextField::setColor](/class/swftextfield.html#SWFTextField::setColor)
        — Sets the color of the text field
    -   [SWFTextField::setFont](/class/swftextfield.html#SWFTextField::setFont)
        — Sets the text field font
    -   [SWFTextField::setHeight](/class/swftextfield.html#SWFTextField::setHeight)
        — Sets the font height of this text field font
    -   [SWFTextField::setIndentation](/class/swftextfield.html#SWFTextField::setIndentation)
        — Sets the indentation of the first line
    -   [SWFTextField::setLeftMargin](/class/swftextfield.html#SWFTextField::setLeftMargin)
        — Sets the left margin width of the text field
    -   [SWFTextField::setLineSpacing](/class/swftextfield.html#SWFTextField::setLineSpacing)
        — Sets the line spacing of the text field
    -   [SWFTextField::setMargins](/class/swftextfield.html#SWFTextField::setMargins)
        — Sets the margins width of the text field
    -   [SWFTextField::setName](/class/swftextfield.html#SWFTextField::setName)
        — Sets the variable name
    -   [SWFTextField::setPadding](/class/swftextfield.html#SWFTextField::setPadding)
        — Sets the padding of this textfield
    -   [SWFTextField::setRightMargin](/class/swftextfield.html#SWFTextField::setRightMargin)
        — Sets the right margin width of the text field
-   [SWFVideoStream](/class/swfvideostream.html) — The SWFVideoStream
    class
    -   [SWFVideoStream::\_\_construct](/class/swfvideostream.html#SWFVideoStream::__construct)
        — Returns a SWFVideoStream object
    -   [SWFVideoStream::getNumFrames](/class/swfvideostream.html#SWFVideoStream::getNumFrames)
        — Returns the number of frames in the video
    -   [SWFVideoStream::setDimension](/class/swfvideostream.html#SWFVideoStream::setDimension)
        — Sets video dimension

简介
----

SWFAction.

类摘要
------

**SWFAction**

<span class="ooclass"> class **SWFAction** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$script`</span> )

}

说明
----

The script syntax is based on the C language, but with a lot taken out-
the SWF bytecode machine is just too simpleminded to do a lot of things
we might like. For instance, we can't implement function calls without a
tremendous amount of hackery because the jump bytecode has a hardcoded
offset value. No pushing your calling address to the stack and
returning- every function would have to know exactly where to return to.

So what's left? The compiler recognises the following tokens:

-   <span class="simpara"> break </span>
-   <span class="simpara"> for </span>
-   <span class="simpara"> continue </span>
-   <span class="simpara"> if </span>
-   <span class="simpara"> else </span>
-   <span class="simpara"> do </span>
-   <span class="simpara"> while </span>

There is no typed data; all values in the SWF action machine are stored
as strings. The following functions can be used in expressions:

time()  
<span class="simpara"> Returns the number of milliseconds (?) elapsed
since the movie started. </span>

random(seed)  
<span class="simpara"> Returns a pseudo-random number in the range
0-seed. </span>

length(expr)  
<span class="simpara"> Returns the length of the given expression.
</span>

int(number)  
<span class="simpara"> Returns the given number rounded down to the
nearest integer. </span>

concat(expr, expr)  
<span class="simpara"> Returns the concatenation of the given
expressions. </span>

ord(expr)  
<span class="simpara"> Returns the ASCII code for the given character
</span>

chr(num)  
<span class="simpara"> Returns the character for the given ASCII code
</span>

substr(string, location, length)  
<span class="simpara"> Returns the substring of length `length` at
location `location` of the given string `string`. </span>

Additionally, the following commands may be used:

duplicateClip(clip, name, depth)  
<span class="simpara"> Duplicate the named movie `clip` (aka sprite).
The new movie clip has name `name` and is at depth `depth`. </span>

removeClip(expr)  
<span class="simpara"> Removes the named movie clip. </span>

trace(expr)  
<span class="simpara"> Write the given expression to the trace log.
Doubtful that the browser plugin does anything with this. </span>

startDrag(target, lock, \[left, top, right, bottom\])  
<span class="simpara"> Start dragging the movie clip `target`. The
`lock` argument indicates whether to lock the mouse (?)- use 0
(**`FALSE`**) or 1 (**`TRUE`**). Optional parameters define a bounding
area for the dragging. </span>

stopDrag()  
<span class="simpara"> Stop dragging my heart around. And this movie
clip, too. </span>

callFrame(expr)  
<span class="simpara"> Call the named frame as a function. </span>

getURL(url, target, \[method\])  
<span class="simpara"> Load the given URL into the named target. The
`target` argument corresponds to HTML document targets (such as "\_top"
or "\_blank"). The optional `method` argument can be POST or GET if you
want to submit variables back to the server. </span>

loadMovie(url, target)  
<span class="simpara"> Load the given URL into the named target. The
`target` argument can be a frame name (I think), or one of the magical
values "\_level0" (replaces current movie) or "\_level1" (loads new
movie on top of current movie). </span>

nextFrame()  
<span class="simpara"> Go to the next frame. </span>

prevFrame()  
<span class="simpara"> Go to the last (or, rather, previous) frame.
</span>

play()  
<span class="simpara"> Start playing the movie. </span>

stop()  
<span class="simpara"> Stop playing the movie. </span>

toggleQuality()  
<span class="simpara"> Toggle between high and low quality. </span>

stopSounds()  
<span class="simpara"> Stop playing all sounds. </span>

gotoFrame(num)  
<span class="simpara"> Go to frame number `num`. Frame numbers start at
0. </span>

gotoFrame(name)  
<span class="simpara"> Go to the frame named `name`. Which does a lot of
good, since I haven't added frame labels yet. </span>

setTarget(expr)  
<span class="simpara"> Sets the context for action. Or so they say- I
really have no idea what this does. </span>

And there's one weird extra thing. The expression frameLoaded(num) can
be used in if statements and while loops to check if the given frame
number has been loaded yet. Well, it's supposed to, anyway, but I've
never tested it and I seriously doubt it actually works. You can just
use /:framesLoaded instead.

Movie clips (all together now- aka sprites) have properties. You can
read all of them (or can you?), you can set some of them, and here they
are:

-   <span class="simpara"> x </span>
-   <span class="simpara"> y </span>
-   <span class="simpara"> xScale </span>
-   <span class="simpara"> yScale </span>
-   <span class="simpara"> currentFrame - (read-only) </span>
-   <span class="simpara"> totalFrames - (read-only) </span>
-   <span class="simpara"> alpha - transparency level </span>
-   <span class="simpara"> visible - 1=on, 0=off (?) </span>
-   <span class="simpara"> width - (read-only) </span>
-   <span class="simpara"> height - (read-only) </span>
-   <span class="simpara"> rotation </span>
-   <span class="simpara"> target - (read-only) (???) </span>
-   <span class="simpara"> framesLoaded - (read-only) </span>
-   <span class="simpara"> name </span>
-   <span class="simpara"> dropTarget - (read-only) (???) </span>
-   <span class="simpara"> url - (read-only) (???) </span>
-   <span class="simpara"> highQuality - 1=high, 0=low (?) </span>
-   <span class="simpara"> focusRect - (???) </span>
-   <span class="simpara"> soundBufTime - (???) </span>

So, setting a sprite's x position is as simple as */box.x = 100;*. Why
the slash in front of the box, though? That's how flash keeps track of
the sprites in the movie, just like a Unix filesystem- here it shows
that box is at the top level. If the sprite named box had another sprite
named biff inside of it, you'd set its x position with /box/biff.x =
100;. At least, I think so; correct me if I'm wrong here.

SWFAction::\_\_construct
========================

Creates a new SWFAction

### 说明

<span class="methodname">SWFAction::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$script`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new SWFAction and compiles the given `script` in it.

### 参数

`script`  
An ActionScript snippet to associate with the SWFAction. See
<a href="/class/swfaction.html" class="xref">SWFAction</a> for more
details.

简介
----

SWFBitmap.

类摘要
------

**SWFBitmap**

<span class="ooclass"> class **SWFBitmap** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$file`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$alphafile`</span> \] )

<span class="type">float</span> <span
class="methodname">getHeight</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getWidth</span>
( <span class="methodparam">void</span> )

}

SWFBitmap::\_\_construct
========================

Loads Bitmap object

### 说明

<span class="methodname">SWFBitmap::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$file`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$alphafile`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates the new <span class="classname">SWFBitmap</span> object from the
given `file`.

### 参数

For both parameters you can provide a file pointer returned by <span
class="function">fopen</span> or the image data, as a binary string.

`file`  
> **Note**:
>
> We can only deal with baseline (frame 0) jpegs, no baseline optimized
> or progressive scan jpegs!

You can't import png images directly, though- have to use the png2dbl
utility to make a dbl ("define bits lossless") file from the png. The
reason for this is that I don't want a dependency on the png library in
ming- autoconf should solve this, but that's not set up yet.

`alphafile`  
An MSK file to be used as an alpha mask for a JPEG image.

### 范例

**示例 \#1 Importing a DBL file**

``` php
<?php
$s = new SWFShape();
$f = $s->addFill(new SWFBitmap(file_get_contents("image.dbl")));
$s->setRightFill($f);

$s->drawLine(32, 0);
$s->drawLine(0, 32);
$s->drawLine(-32, 0);
$s->drawLine(0, -32);

$m = new SWFMovie();
$m->setDimension(32, 32);
$m->add($s);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

**示例 \#2 Using an alpha mask**

``` php
<?php

$s = new SWFShape();

// .msk file generated with "gif2mask" utility
$f = $s->addFill(new SWFBitmap(file_get_contents("alphafill.jpg"), file_get_contents("alphafill.msk")));
$s->setRightFill($f);

$s->drawLine(640, 0);
$s->drawLine(0, 480);
$s->drawLine(-640, 0);
$s->drawLine(0, -480);

$c = new SWFShape();
$c->setRightFill($c->addFill(0x99, 0x99, 0x99));
$c->drawLine(40, 0);
$c->drawLine(0, 40);
$c->drawLine(-40, 0);
$c->drawLine(0, -40);

$m = new SWFMovie();
$m->setDimension(640, 480);
$m->setBackground(0xcc, 0xcc, 0xcc);

// draw checkerboard background
for ($y=0; $y<480; $y+=40) {
  for ($x=0; $x<640; $x+=80) {
    $i = $m->add($c);
    $i->moveTo($x, $y);
  }

  $y+=40;

  for ($x=40; $x<640; $x+=80) {
    $i = $m->add($c);
    $i->moveTo($x, $y);
  }
}

$m->add($s);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFBitmap::getHeight
====================

Returns the bitmap's height

### 说明

<span class="type">float</span> <span
class="methodname">SWFBitmap::getHeight</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the bitmap's height.

### 返回值

Returns the bitmap height in pixels.

### 参见

-   <span class="function">SWFBitmap::getWidth</span>

SWFBitmap::getWidth
===================

Returns the bitmap's width

### 说明

<span class="type">float</span> <span
class="methodname">SWFBitmap::getWidth</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the bitmap's width.

### 返回值

Returns the bitmap width in pixels.

### 参见

-   <span class="function">SWFBitmap::getHeight</span>

简介
----

SWFButton.

类摘要
------

**SWFButton**

<span class="ooclass"> class **SWFButton** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">addAction</span>
( <span class="methodparam"><span class="type">SWFAction</span>
`$action`</span> , <span class="methodparam"><span
class="type">int</span> `$flags`</span> )

<span class="type">SWFSoundInstance</span> <span
class="methodname">addASound</span> ( <span class="methodparam"><span
class="type">SWFSound</span> `$sound`</span> , <span
class="methodparam"><span class="type">int</span> `$flags`</span> )

<span class="type">void</span> <span class="methodname">addShape</span>
( <span class="methodparam"><span class="type">SWFShape</span>
`$shape`</span> , <span class="methodparam"><span
class="type">int</span> `$flags`</span> )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">setAction</span>
( <span class="methodparam"><span class="type">SWFAction</span>
`$action`</span> )

<span class="type">void</span> <span class="methodname">setDown</span> (
<span class="methodparam"><span class="type">SWFShape</span>
`$shape`</span> )

<span class="type">void</span> <span class="methodname">setHit</span> (
<span class="methodparam"><span class="type">SWFShape</span>
`$shape`</span> )

<span class="type">void</span> <span class="methodname">setMenu</span> (
<span class="methodparam"><span class="type">int</span> `$flag`</span> )

<span class="type">void</span> <span class="methodname">setOver</span> (
<span class="methodparam"><span class="type">SWFShape</span>
`$shape`</span> )

<span class="type">void</span> <span class="methodname">setUp</span> (
<span class="methodparam"><span class="type">SWFShape</span>
`$shape`</span> )

}

SWFButton::addAction
====================

Adds an action

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::addAction</span> ( <span
class="methodparam"><span class="type">SWFAction</span> `$action`</span>
, <span class="methodparam"><span class="type">int</span>
`$flags`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Adds the given `action` to the button for the given conditions.

### 参数

`action`  
An <span class="classname">SWFAction</span>, returned by <span
class="function">SWFAction::\_\_construct</span>.

`flags`  
The following `flags` are valid: **`SWFBUTTON_MOUSEOVER`**,
**`SWFBUTTON_MOUSEOUT`**, **`SWFBUTTON_MOUSEUP`**,
**`SWFBUTTON_MOUSEUPOUTSIDE`**, **`SWFBUTTON_MOUSEDOWN`**,
**`SWFBUTTON_DRAGOUT`** and **`SWFBUTTON_DRAGOVER`**.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFButton::addShape</span>
-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

SWFButton::addASound
====================

Associates a sound with a button transition

### 说明

<span class="type">SWFSoundInstance</span> <span
class="methodname">SWFButton::addASound</span> ( <span
class="methodparam"><span class="type">SWFSound</span> `$sound`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

SWFButton::addShape
===================

Adds a shape to a button

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::addShape</span> ( <span
class="methodparam"><span class="type">SWFShape</span> `$shape`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Adds the given `shape` to the button.

### 参数

`shape`  
An <span class="classname">SWFShape</span> instance

`flags`  
The following `flags` are valid: **`SWFBUTTON_UP`**,
**`SWFBUTTON_OVER`**, **`SWFBUTTON_DOWN`** and **`SWFBUTTON_HIT`**.

**`SWFBUTTON_HIT`** isn't ever displayed, it defines the hit region for
the button. That is, everywhere the hit shape would be drawn is
considered a "touchable" part of the button.

### 返回值

没有返回值。

SWFButton::\_\_construct
========================

Creates a new Button

### 说明

<span class="methodname">SWFButton::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new Button.

### 范例

This simple example will show your usual interactions with buttons :
rollover, rollon, mouseup, mousedown, noaction.

**示例 \#1 Usual interactions with buttons**

``` php
<?php

$f = new SWFFont("_serif");

$p = new SWFSprite();

function label($string) 
{
  global $f;

  $t = new SWFTextField();
  $t->setFont($f);
  $t->addString($string);
  $t->setHeight(200);
  $t->setBounds(3200, 200);
  return $t;
}

function addLabel($string) 
{
  global $p;

  $i = $p->add(label($string));
  $p->nextFrame();
  $p->remove($i);
}

$p->add(new SWFAction("stop();"));
addLabel("NO ACTION");
addLabel("SWFBUTTON_MOUSEUP");
addLabel("SWFBUTTON_MOUSEDOWN");
addLabel("SWFBUTTON_MOUSEOVER");
addLabel("SWFBUTTON_MOUSEOUT");
addLabel("SWFBUTTON_MOUSEUPOUTSIDE");
addLabel("SWFBUTTON_DRAGOVER");
addLabel("SWFBUTTON_DRAGOUT");

function rect($r, $g, $b) 
{
  $s = new SWFShape();
  $s->setRightFill($s->addFill($r, $g, $b));
  $s->drawLine(600, 0);
  $s->drawLine(0, 600);
  $s->drawLine(-600, 0);
  $s->drawLine(0, -600);

  return $s;
}

$b = new SWFButton();
$b->addShape(rect(0xff, 0, 0), SWFBUTTON_UP | SWFBUTTON_HIT);
$b->addShape(rect(0, 0xff, 0), SWFBUTTON_OVER);
$b->addShape(rect(0, 0, 0xff), SWFBUTTON_DOWN);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(1);"),
          SWFBUTTON_MOUSEUP);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(2);"),
      SWFBUTTON_MOUSEDOWN);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(3);"),
      SWFBUTTON_MOUSEOVER);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(4);"),
      SWFBUTTON_MOUSEOUT);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(5);"),
      SWFBUTTON_MOUSEUPOUTSIDE);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(6);"),
      SWFBUTTON_DRAGOVER);

$b->addAction(new SWFAction("setTarget('/label'); gotoFrame(7);"),
      SWFBUTTON_DRAGOUT);

$m = new SWFMovie();
$m->setDimension(4000, 3000);

$i = $m->add($p);
$i->setName("label");
$i->moveTo(400, 1900);

$i = $m->add($b);
$i->moveTo(400, 900);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

This simple example will enables you to drag draw a big red button on
the windows. No drag-and-drop, just moving around.

**示例 \#2 Drag example**

``` php
<?php

$s = new SWFShape();
$s->setRightFill($s->addFill(0xff, 0, 0));
$s->drawLine(1000,0);
$s->drawLine(0,1000);
$s->drawLine(-1000,0);
$s->drawLine(0,-1000);

$b = new SWFButton();
$b->addShape($s, SWFBUTTON_HIT | SWFBUTTON_UP | SWFBUTTON_DOWN | SWFBUTTON_OVER);

$b->addAction(new SWFAction("startDrag('/test', 0);"), // '0' means don't lock to mouse
      SWFBUTTON_MOUSEDOWN);

$b->addAction(new SWFAction("stopDrag();"),
      SWFBUTTON_MOUSEUP | SWFBUTTON_MOUSEUPOUTSIDE);

$p = new SWFSprite();
$p->add($b);
$p->nextFrame();

$m = new SWFMovie();
$i = $m->add($p);
$i->setName('test');
$i->moveTo(1000,1000);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFButton::setAction
====================

Sets the action

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::setAction</span> ( <span
class="methodparam"><span class="type">SWFAction</span> `$action`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the action to be performed when the button is clicked.

This is a shortcut for <span
class="function">SWFButton::addAction</span> called with the
**`SWFBUTTON_MOUSEUP`** flag.

### 参数

`action`  
An <span class="classname">SWFAction</span>, returned by <span
class="function">SWFAction::\_\_construct</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFButton::addAction</span>
-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

SWFButton::setDown
==================

Alias for addShape(shape, SWFBUTTON\_DOWN)

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::setDown</span> ( <span
class="methodparam"><span class="type">SWFShape</span> `$shape`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfbutton::setdown</span> alias for
addShape(shape, SWFBUTTON\_DOWN).

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFButton::addShape</span>
-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

SWFButton::setHit
=================

Alias for addShape(shape, SWFBUTTON\_HIT)

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::setHit</span> ( <span
class="methodparam"><span class="type">SWFShape</span> `$shape`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfbutton::sethit</span> alias for
addShape(shape, SWFBUTTON\_HIT).

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFButton::addShape</span>
-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

SWFButton::setMenu
==================

Enable track as menu button behaviour

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::setMenu</span> ( <span
class="methodparam"><span class="type">int</span> `$flag`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`flag`  
This parameter can be used for a slight different behavior of buttons.
You can set it to 0 (off) or 1 (on).

### 返回值

没有返回值。

SWFButton::setOver
==================

Alias for addShape(shape, SWFBUTTON\_OVER)

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::setOver</span> ( <span
class="methodparam"><span class="type">SWFShape</span> `$shape`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfbutton::setover</span> alias for
addShape(shape, SWFBUTTON\_OVER).

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFButton::addShape</span>
-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

SWFButton::setUp
================

Alias for addShape(shape, SWFBUTTON\_UP)

### 说明

<span class="type">void</span> <span
class="methodname">SWFButton::setUp</span> ( <span
class="methodparam"><span class="type">SWFShape</span> `$shape`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfbutton::setup</span> alias for addShape(shape,
SWFBUTTON\_UP).

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFButton::addShape</span>
-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

简介
----

SWFDisplayItem.

类摘要
------

**SWFDisplayItem**

<span class="ooclass"> class **SWFDisplayItem** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">addAction</span>
( <span class="methodparam"><span class="type">SWFAction</span>
`$action`</span> , <span class="methodparam"><span
class="type">int</span> `$flags`</span> )

<span class="type">void</span> <span class="methodname">addColor</span>
( <span class="methodparam"><span class="type">int</span> `$red`</span>
, <span class="methodparam"><span class="type">int</span>
`$green`</span> , <span class="methodparam"><span
class="type">int</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">int</span> `$a`</span> \] )

<span class="type">void</span> <span class="methodname">endMask</span> (
<span class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getRot</span> (
<span class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getX</span> (
<span class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getXScale</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getXSkew</span>
( <span class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getY</span> (
<span class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getYScale</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getYSkew</span>
( <span class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">move</span> (
<span class="methodparam"><span class="type">float</span> `$dx`</span> ,
<span class="methodparam"><span class="type">float</span> `$dy`</span> )

<span class="type">void</span> <span class="methodname">moveTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">void</span> <span class="methodname">multColor</span>
( <span class="methodparam"><span class="type">float</span>
`$red`</span> , <span class="methodparam"><span
class="type">float</span> `$green`</span> , <span
class="methodparam"><span class="type">float</span> `$blue`</span> \[,
<span class="methodparam"><span class="type">float</span> `$a`</span> \]
)

<span class="type">void</span> <span class="methodname">remove</span> (
<span class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">rotate</span> (
<span class="methodparam"><span class="type">float</span>
`$angle`</span> )

<span class="type">void</span> <span class="methodname">rotateTo</span>
( <span class="methodparam"><span class="type">float</span>
`$angle`</span> )

<span class="type">void</span> <span class="methodname">scale</span> (
<span class="methodparam"><span class="type">float</span> `$dx`</span> ,
<span class="methodparam"><span class="type">float</span> `$dy`</span> )

<span class="type">void</span> <span class="methodname">scaleTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$y`</span> \] )

<span class="type">void</span> <span class="methodname">setDepth</span>
( <span class="methodparam"><span class="type">int</span>
`$depth`</span> )

<span class="type">void</span> <span
class="methodname">setMaskLevel</span> ( <span class="methodparam"><span
class="type">int</span> `$level`</span> )

<span class="type">void</span> <span class="methodname">setMatrix</span>
( <span class="methodparam"><span class="type">float</span> `$a`</span>
, <span class="methodparam"><span class="type">float</span> `$b`</span>
, <span class="methodparam"><span class="type">float</span> `$c`</span>
, <span class="methodparam"><span class="type">float</span> `$d`</span>
, <span class="methodparam"><span class="type">float</span> `$x`</span>
, <span class="methodparam"><span class="type">float</span> `$y`</span>
)

<span class="type">void</span> <span class="methodname">setName</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="type">void</span> <span class="methodname">setRatio</span>
( <span class="methodparam"><span class="type">float</span>
`$ratio`</span> )

<span class="type">void</span> <span class="methodname">skewX</span> (
<span class="methodparam"><span class="type">float</span>
`$ddegrees`</span> )

<span class="type">void</span> <span class="methodname">skewXTo</span> (
<span class="methodparam"><span class="type">float</span>
`$degrees`</span> )

<span class="type">void</span> <span class="methodname">skewY</span> (
<span class="methodparam"><span class="type">float</span>
`$ddegrees`</span> )

<span class="type">void</span> <span class="methodname">skewYTo</span> (
<span class="methodparam"><span class="type">float</span>
`$degrees`</span> )

}

SWFDisplayItem::addAction
=========================

Adds this SWFAction to the given SWFSprite instance

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::addAction</span> ( <span
class="methodparam"><span class="type">SWFAction</span> `$action`</span>
, <span class="methodparam"><span class="type">int</span>
`$flags`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`action`  
An <span class="classname">SWFAction</span>, returned by <span
class="function">SWFAction::\_\_construct</span>.

`flags`  

### 返回值

没有返回值。

### 参见

-   <a href="/class/swfaction.html" class="xref">SWFAction</a>

SWFDisplayItem::addColor
========================

Adds the given color to this item's color transform

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::addColor</span> ( <span
class="methodparam"><span class="type">int</span> `$red`</span> , <span
class="methodparam"><span class="type">int</span> `$green`</span> ,
<span class="methodparam"><span class="type">int</span> `$blue`</span>
\[, <span class="methodparam"><span class="type">int</span> `$a`</span>
\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::addcolor</span> adds the color to
this item's color transform. The color is given in its RGB form.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 返回值

没有返回值。

SWFDisplayItem::endMask
=======================

Another way of defining a MASK layer

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::endMask</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFDisplayItem::getRot
======================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getRot</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

SWFDisplayItem::getX
====================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getX</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFDisplayItem::getY</span>

SWFDisplayItem::getXScale
=========================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getXScale</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFDisplayItem::getYScale</span>

SWFDisplayItem::getXSkew
========================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getXSkew</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFDisplayItem::getYSkew</span>

SWFDisplayItem::getY
====================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getY</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFDisplayItem::getX</span>

SWFDisplayItem::getYScale
=========================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getYScale</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFDisplayItem::getXScale</span>

SWFDisplayItem::getYSkew
========================

### 说明

<span class="type">float</span> <span
class="methodname">SWFDisplayItem::getYSkew</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFDisplayItem::getXSkew</span>

SWFDisplayItem::move
====================

Moves object in relative coordinates

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::move</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::move</span> moves the current
object by (`dx`,`dy`) from its current position.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::moveTo</span>

SWFDisplayItem::moveTo
======================

Moves object in global coordinates

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::moveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::moveto</span> moves the current
object to (`x`,`y`) in global coordinates.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::move</span>

SWFDisplayItem::multColor
=========================

Multiplies the item's color transform

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::multColor</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">float</span> `$a`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::multcolor</span> multiplies the
item's color transform by the given values.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 参数

These parameters are floats between 0.0 and 1.0:

`red`  
Value of red component

`green`  
Value of green component

`blue`  
Value of blue component

`a`  
Value of alpha component

### 返回值

没有返回值。

### 范例

This simple example will modify your picture's atmosphere to Halloween
(use a landscape or bright picture).

**示例 \#1 <span class="function">swfdisplayitem::multcolor</span>
example**

``` php
<?php

$b = new SWFBitmap(file_get_contents("backyard.jpg"));
// note use your own picture :-)
$s = new SWFShape();
$s->setRightFill($s->addFill($b));
$s->drawLine($b->getWidth(), 0);
$s->drawLine(0, $b->getHeight());
$s->drawLine(-$b->getWidth(), 0);
$s->drawLine(0, -$b->getHeight());

$m = new SWFMovie();
$m->setDimension($b->getWidth(), $b->getHeight());

$i = $m->add($s);

for ($n=0; $n<=20; ++$n) {
  $i->multColor(1.0-$n/10, 1.0, 1.0);
  $i->addColor(0xff*$n/20, 0, 0);
  $m->nextFrame();
}

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFDisplayItem::remove
======================

Removes the object from the movie

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::remove</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::remove</span> removes this object
from the movie's display list.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFMovie::add</span>

SWFDisplayItem::rotate
======================

Rotates in relative coordinates

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::rotate</span> ( <span
class="methodparam"><span class="type">float</span> `$angle`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::rotate</span> rotates the current
object by `angle` degrees from its current rotation.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::rotateTo</span>

SWFDisplayItem::rotateTo
========================

Rotates the object in global coordinates

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::rotateTo</span> ( <span
class="methodparam"><span class="type">float</span> `$angle`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::rotateto</span> set the current
object rotation to `angle` degrees in global coordinates.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 范例

This example bring three rotating string from the background to the
foreground. Pretty nice.

**示例 \#1 <span class="function">swfdisplayitem::rotateto</span>
example**

``` php
<?php
$thetext =  "ming!";

$f = new SWFFont("Bauhaus 93.fdb");

$m = new SWFMovie();
$m->setRate(24.0);
$m->setDimension(2400, 1600);
$m->setBackground(0xff, 0xff, 0xff);

// functions with huge numbers of arbitrary
// arguments are always a good idea!  Really!

function text($r, $g, $b, $a, $rot, $x, $y, $scale, $string) 
{
  global $f, $m;

  $t = new SWFText();
  $t->setFont($f);
  $t->setColor($r, $g, $b, $a);
  $t->setHeight(960);
  $t->moveTo(-($f->getWidth($string))/2, $f->getAscent()/2);
  $t->addString($string);

  // we can add properties just like a normal PHP var,
  // as long as the names aren't already used.
  // e.g., we can't set $i->scale, because that's a function

  $i = $m->add($t);
  $i->x = $x;
  $i->y = $y;
  $i->rot = $rot;
  $i->s = $scale;
  $i->rotateTo($rot);
  $i->scale($scale, $scale);

  // but the changes are local to the function, so we have to
  // return the changed object.  kinda weird..

  return $i;
}

function step($i) 
{
  $oldrot = $i->rot;
  $i->rot = 19*$i->rot/20;
  $i->x = (19*$i->x + 1200)/20;
  $i->y = (19*$i->y + 800)/20;
  $i->s = (19*$i->s + 1.0)/20;

  $i->rotateTo($i->rot);
  $i->scaleTo($i->s, $i->s);
  $i->moveTo($i->x, $i->y);

  return $i;
}

// see?  it sure paid off in legibility:

$i1 = text(0xff, 0x33, 0x33, 0xff, 900, 1200, 800, 0.03, $thetext);
$i2 = text(0x00, 0x33, 0xff, 0x7f, -560, 1200, 800, 0.04, $thetext);
$i3 = text(0xff, 0xff, 0xff, 0x9f, 180, 1200, 800, 0.001, $thetext);

for ($i=1; $i<=100; ++$i) {
  $i1 = step($i1);
  $i2 = step($i2);
  $i3 = step($i3);

  $m->nextFrame();
}

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

### 参见

-   <span class="function">SWFDisplayItem::rotate</span>

SWFDisplayItem::scale
=====================

Scales the object in relative coordinates

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::scale</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::scale</span> scales the current
object by (`dx`,`dy`) from its current size.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::scaleTo</span>

SWFDisplayItem::scaleTo
=======================

Scales the object in global coordinates

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::scaleTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> \[,
<span class="methodparam"><span class="type">float</span> `$y`</span> \]
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::scaleto</span> scales the current
object to (`x`,`y`) in global coordinates.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::scale</span>

SWFDisplayItem::setDepth
========================

Sets z-order

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::setDepth</span> ( <span
class="methodparam"><span class="type">int</span> `$depth`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::setdepth</span> sets the object's
z-order to `depth`. Depth defaults to the order in which instances are
created (by adding a shape/text to a movie)- newer ones are on top of
older ones. If two objects are given the same depth, only the
later-defined one can be moved.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

SWFDisplayItem::setMaskLevel
============================

Defines a MASK layer at level

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::setMaskLevel</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFDisplayItem::setMatrix
=========================

Sets the item's transform matrix

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::setMatrix</span> ( <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> , <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$d`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFDisplayItem::setName
=======================

Sets the object's name

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::setName</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::setname</span> sets the object's
name to `name`, for targetting with action script. Only useful on
sprites.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

SWFDisplayItem::setRatio
========================

Sets the object's ratio

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::setRatio</span> ( <span
class="methodparam"><span class="type">float</span> `$ratio`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::setratio</span> sets the object's
ratio to `ratio`. Obviously only useful for morphs.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 范例

This simple example will morph nicely three concentric circles.

**示例 \#1 <span class="function">swfdisplayitem::setname</span>
example**

``` php
<?php

$p = new SWFMorph();

$g = new SWFGradient();
$g->addEntry(0.0, 0, 0, 0);
$g->addEntry(0.16, 0xff, 0xff, 0xff);
$g->addEntry(0.32, 0, 0, 0);
$g->addEntry(0.48, 0xff, 0xff, 0xff);
$g->addEntry(0.64, 0, 0, 0);
$g->addEntry(0.80, 0xff, 0xff, 0xff);
$g->addEntry(1.00, 0, 0, 0);

$s = $p->getShape1();
$f = $s->addFill($g, SWFFILL_RADIAL_GRADIENT);
$f->scaleTo(0.05);
$s->setLeftFill($f);
$s->movePenTo(-160, -120);
$s->drawLine(320, 0);
$s->drawLine(0, 240);
$s->drawLine(-320, 0);
$s->drawLine(0, -240);

$g = new SWFGradient();
$g->addEntry(0.0, 0, 0, 0);
$g->addEntry(0.16, 0xff, 0, 0);
$g->addEntry(0.32, 0, 0, 0);
$g->addEntry(0.48, 0, 0xff, 0);
$g->addEntry(0.64, 0, 0, 0);
$g->addEntry(0.80, 0, 0, 0xff);
$g->addEntry(1.00, 0, 0, 0);

$s = $p->getShape2();
$f = $s->addFill($g, SWFFILL_RADIAL_GRADIENT);
$f->scaleTo(0.05);
$f->skewXTo(1.0);
$s->setLeftFill($f);
$s->movePenTo(-160, -120);
$s->drawLine(320, 0);
$s->drawLine(0, 240);
$s->drawLine(-320, 0);
$s->drawLine(0, -240);

$m = new SWFMovie();
$m->setDimension(320, 240);
$i = $m->add($p);
$i->moveTo(160, 120);

for ($n=0; $n<=1.001; $n+=0.01) {
    $i->setRatio($n);
    $m->nextFrame();
}

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFDisplayItem::skewX
=====================

Sets the X-skew

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::skewX</span> ( <span
class="methodparam"><span class="type">float</span> `$ddegrees`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::skewx</span> adds `ddegrees` to
current x-skew.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::skewXTo</span>
-   <span class="function">SWFDisplayItem::skewY</span>
-   <span class="function">SWFDisplayItem::skewYTo</span>

SWFDisplayItem::skewXTo
=======================

Sets the X-skew

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::skewXTo</span> ( <span
class="methodparam"><span class="type">float</span> `$degrees`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::skewxto</span> sets the x-skew to
`degrees`. For `degrees` is 1.0, it means a 45-degree forward slant.
More is more forward, less is more backward.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::skewX</span>
-   <span class="function">SWFDisplayItem::skewY</span>
-   <span class="function">SWFDisplayItem::skewYTo</span>

SWFDisplayItem::skewY
=====================

Sets the Y-skew

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::skewY</span> ( <span
class="methodparam"><span class="type">float</span> `$ddegrees`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::skewy</span> adds `ddegrees` to
current y-skew.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::skewYTo</span>
-   <span class="function">SWFDisplayItem::skewX</span>
-   <span class="function">SWFDisplayItem::skewXTo</span>

SWFDisplayItem::skewYTo
=======================

Sets the Y-skew

### 说明

<span class="type">void</span> <span
class="methodname">SWFDisplayItem::skewYTo</span> ( <span
class="methodparam"><span class="type">float</span> `$degrees`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfdisplayitem::skewyto</span> sets the y-skew to
`degrees`. For `degrees` is 1.0, it means a 45-degree forward slant.
More is more upward, less is more downward.

The object may be a <span class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span> or a <span
class="function">swfsprite</span> object. It must have been added using
the <span class="function">swfmovie::add</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFDisplayItem::skewY</span>
-   <span class="function">SWFDisplayItem::skewX</span>
-   <span class="function">SWFDisplayItem::skewXTo</span>

简介
----

The <span class="classname">SWFFill</span> object allows you to
transform (scale, skew, rotate) bitmap and gradient fills.

<span class="classname">swffill</span> objects are created by the <span
class="function">SWFShape::addFill</span> method.

类摘要
------

**SWFFill**

<span class="ooclass"> class **SWFFill** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">moveTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">void</span> <span class="methodname">rotateTo</span>
( <span class="methodparam"><span class="type">float</span>
`$angle`</span> )

<span class="type">void</span> <span class="methodname">scaleTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$y`</span> \] )

<span class="type">void</span> <span class="methodname">skewXTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> )

<span class="type">void</span> <span class="methodname">skewYTo</span> (
<span class="methodparam"><span class="type">float</span> `$y`</span> )

}

SWFFill::moveTo
===============

Moves fill origin

### 说明

<span class="type">void</span> <span
class="methodname">SWFFill::moveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Moves the fill origin to the given global coordinates.

### 参数

`x`  
X-coordinate

`y`  
Y-coordinate

### 返回值

没有返回值。

SWFFill::rotateTo
=================

Sets fill's rotation

### 说明

<span class="type">void</span> <span
class="methodname">SWFFill::rotateTo</span> ( <span
class="methodparam"><span class="type">float</span> `$angle`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the fill rotation to the given `angle`.

### 参数

`angle`  
The rotation angle, in degrees.

### 返回值

没有返回值。

SWFFill::scaleTo
================

Sets fill's scale

### 说明

<span class="type">void</span> <span
class="methodname">SWFFill::scaleTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> \[,
<span class="methodparam"><span class="type">float</span> `$y`</span> \]
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the fill scale to the given coordinates.

### 参数

`x`  
X-coordinate

`y`  
Y-coordinate

### 返回值

没有返回值。

SWFFill::skewXTo
================

Sets fill x-skew

### 说明

<span class="type">void</span> <span
class="methodname">SWFFill::skewXTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the fill x-skew to `x`.

### 参数

`x`  
When `x` is 1.0, it is a 45-degree forward slant. More is more forward,
less is more backward.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFFill::skewYTo</span>

SWFFill::skewYTo
================

Sets fill y-skew

### 说明

<span class="type">void</span> <span
class="methodname">SWFFill::skewYTo</span> ( <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the fill y-skew to `y`.

### 参数

`y`  
When `y` is 1.0, it is a 45-degree upward slant. More is more upward,
less is more downward.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFFill::skewXTo</span>

简介
----

The <span class="classname">SWFFont</span> object represent a reference
to the font definition, for us with <span
class="function">SWFText::setFont</span> and <span
class="function">SWFTextField::setFont</span>.

类摘要
------

**SWFFont**

<span class="ooclass"> class **SWFFont** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="type">float</span> <span
class="methodname">getAscent</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getDescent</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getLeading</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">getShape</span> ( <span class="methodparam"><span
class="type">int</span> `$code`</span> )

<span class="type">float</span> <span
class="methodname">getUTF8Width</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

<span class="type">float</span> <span class="methodname">getWidth</span>
( <span class="methodparam"><span class="type">string</span>
`$string`</span> )

}

SWFFont::\_\_construct
======================

Loads a font definition

### 说明

<span class="methodname">SWFFont::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

If `filename` is the name of an FDB file (i.e., it ends in ".fdb"), load
the font definition found in said file. Otherwise, create a
browser-defined font reference.

FDB ("font definition block") is a very simple wrapper for the SWF
DefineFont2 block which contains a full description of a font. One may
create FDB files from SWT Generator template files with the included
makefdb utility- look in the util directory off the main ming
distribution directory.

Browser-defined fonts don't contain any information about the font other
than its name. It is assumed that the font definition will be provided
by the movie player. The fonts \_serif, \_sans, and \_typewriter should
always be available. For example:

``` php
<?php
$f = newSWFFont("_sans"); 
?>
```

will give you the standard sans-serif font, probably the same as what
you'd get with *\<font name="sans-serif"\>* in HTML.

SWFFont::getAscent
==================

Returns the ascent of the font, or 0 if not available

### 说明

<span class="type">float</span> <span
class="methodname">SWFFont::getAscent</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFFont::getDescent</span>

SWFFont::getDescent
===================

Returns the descent of the font, or 0 if not available

### 说明

<span class="type">float</span> <span
class="methodname">SWFFont::getDescent</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFFont::getAscent</span>

SWFFont::getLeading
===================

Returns the leading of the font, or 0 if not available

### 说明

<span class="type">float</span> <span
class="methodname">SWFFont::getLeading</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

SWFFont::getShape
=================

Returns the glyph shape of a char as a text string

### 说明

<span class="type">string</span> <span
class="methodname">SWFFont::getShape</span> ( <span
class="methodparam"><span class="type">int</span> `$code`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

SWFFont::getUTF8Width
=====================

Calculates the width of the given string in this font at full height

### 说明

<span class="type">float</span> <span
class="methodname">SWFFont::getUTF8Width</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFFont::getWidth</span>

SWFFont::getWidth
=================

Returns the string's width

### 说明

<span class="type">float</span> <span
class="methodname">SWFFont::getWidth</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swffont::getwidth</span> returns the string
`string`'s width, using font's default scaling. You'll probably want to
use the <span class="function">swftext</span> version of this method
which uses the text object's scale.

### 参见

-   <span class="function">SWFFont::getUTF8Width</span>

简介
----

SWFFontChar.

类摘要
------

**SWFFontChar**

<span class="ooclass"> class **SWFFontChar** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">addChars</span>
( <span class="methodparam"><span class="type">string</span>
`$char`</span> )

<span class="type">void</span> <span
class="methodname">addUTF8Chars</span> ( <span class="methodparam"><span
class="type">string</span> `$char`</span> )

}

SWFFontChar::addChars
=====================

Adds characters to a font for exporting font

### 说明

<span class="type">void</span> <span
class="methodname">SWFFontChar::addChars</span> ( <span
class="methodparam"><span class="type">string</span> `$char`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFFontChar::addUTF8Chars</span>

SWFFontChar::addUTF8Chars
=========================

Adds characters to a font for exporting font

### 说明

<span class="type">void</span> <span
class="methodname">SWFFontChar::addUTF8Chars</span> ( <span
class="methodparam"><span class="type">string</span> `$char`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFFontChar::addChars</span>

简介
----

SWFGradient.

类摘要
------

**SWFGradient**

<span class="ooclass"> class **SWFGradient** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">addEntry</span>
( <span class="methodparam"><span class="type">float</span>
`$ratio`</span> , <span class="methodparam"><span
class="type">int</span> `$red`</span> , <span class="methodparam"><span
class="type">int</span> `$green`</span> , <span
class="methodparam"><span class="type">int</span> `$blue`</span> \[,
<span class="methodparam"><span class="type">int</span> `$alpha`<span
class="initializer"> = 255</span></span> \] )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

}

SWFGradient::addEntry
=====================

Adds an entry to the gradient list

### 说明

<span class="type">void</span> <span
class="methodname">SWFGradient::addEntry</span> ( <span
class="methodparam"><span class="type">float</span> `$ratio`</span> ,
<span class="methodparam"><span class="type">int</span> `$red`</span> ,
<span class="methodparam"><span class="type">int</span> `$green`</span>
, <span class="methodparam"><span class="type">int</span> `$blue`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$alpha`<span class="initializer"> = 255</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfgradient::addentry</span> adds an entry to the
gradient list. `ratio` is a number between 0 and 1 indicating where in
the gradient this color appears. Thou shalt add entries in order of
increasing ratio.

`red`, `green`, `blue` is a color (RGB mode).

### 返回值

没有返回值。

SWFGradient::\_\_construct
==========================

Creates a gradient object

### 说明

<span class="methodname">SWFGradient::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfgradient</span> creates a new SWFGradient
object.

After you've added the entries to your gradient, you can use the
gradient in a shape fill with the <span
class="function">swfshape::addfill</span> method.

SWFGradient has the following methods : <span
class="function">swfgradient::addentry</span>.

This simple example will draw a big black-to-white gradient as
background, and a reddish disc in its center.

**示例 \#1 <span class="function">swfgradient</span> example**

``` php
<?php

  $m = new SWFMovie();
  $m->setDimension(320, 240);

  $s = new SWFShape();

  // first gradient- black to white
  $g = new SWFGradient();
  $g->addEntry(0.0, 0, 0, 0);
  $g->addEntry(1.0, 0xff, 0xff, 0xff);

  $f = $s->addFill($g, SWFFILL_LINEAR_GRADIENT);
  $f->scaleTo(0.01);
  $f->moveTo(160, 120);
  $s->setRightFill($f);
  $s->drawLine(320, 0);
  $s->drawLine(0, 240);
  $s->drawLine(-320, 0);
  $s->drawLine(0, -240);

  $m->add($s);

  $s = new SWFShape();

  // second gradient- radial gradient from red to transparent
  $g = new SWFGradient();
  $g->addEntry(0.0, 0xff, 0, 0, 0xff);
  $g->addEntry(1.0, 0xff, 0, 0, 0);

  $f = $s->addFill($g, SWFFILL_RADIAL_GRADIENT);
  $f->scaleTo(0.005);
  $f->moveTo(160, 120);
  $s->setRightFill($f);
  $s->drawLine(320, 0);
  $s->drawLine(0, 240);
  $s->drawLine(-320, 0);
  $s->drawLine(0, -240);

  $m->add($s);

  header('Content-type: application/x-shockwave-flash');
  $m->output();
?>
```

简介
----

The methods here are sort of weird. It would make more sense to just
have newSWFMorph(shape1, shape2);, but as things are now, shape2 needs
to know that it's the second part of a morph. (This, because it starts
writing its output as soon as it gets drawing commands- if it kept its
own description of its shapes and wrote on completion this and some
other things would be much easier.)

类摘要
------

**SWFMorph**

<span class="ooclass"> class **SWFMorph** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="type">SWFShape</span> <span
class="methodname">getShape1</span> ( <span
class="methodparam">void</span> )

<span class="type">SWFShape</span> <span
class="methodname">getShape2</span> ( <span
class="methodparam">void</span> )

}

SWFMorph::\_\_construct
=======================

Creates a new SWFMorph object

### 说明

<span class="methodname">SWFMorph::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new <span class="classname">SWFMorph</span> object.

Also called a "shape tween". This thing lets you make those tacky
twisting things that make your computer choke. Oh, joy!

### 范例

This simple example will morph a big red square into a smaller blue
black-bordered square.

**示例 \#1 <span class="function">swfmorph</span> example**

``` php
<?php
  $p = new SWFMorph();

  $s = $p->getShape1();
  $s->setLine(0, 0, 0, 0);

  /* Note that this is backwards from normal shapes (left instead of right).
     I have no idea why, but this seems to work.. */

  $s->setLeftFill($s->addFill(0xff, 0, 0));
  $s->movePenTo(-1000,-1000);
  $s->drawLine(2000,0);
  $s->drawLine(0,2000);
  $s->drawLine(-2000,0);
  $s->drawLine(0,-2000);

  $s = $p->getShape2();
  $s->setLine(60,0,0,0);
  $s->setLeftFill($s->addFill(0, 0, 0xff));
  $s->movePenTo(0,-1000);
  $s->drawLine(1000,1000);
  $s->drawLine(-1000,1000);
  $s->drawLine(-1000,-1000);
  $s->drawLine(1000,-1000);

  $m = new SWFMovie();
  $m->setDimension(3000,2000);
  $m->setBackground(0xff, 0xff, 0xff);

  $i = $m->add($p);
  $i->moveTo(1500,1000);

  for ($r=0.0; $r<=1.0; $r+=0.1) {
    $i->setRatio($r);
    $m->nextFrame();
  }

  header('Content-type: application/x-shockwave-flash');
  $m->output();
?>
```

SWFMorph::getShape1
===================

Gets a handle to the starting shape

### 说明

<span class="type">SWFShape</span> <span
class="methodname">SWFMorph::getShape1</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Gets the morph's starting shape.

### 返回值

Returns a <a href="/class/swfshape.html" class="xref">SWFShape</a>
object.

### 参见

-   <span class="function">SWFMorph::getShape2</span>

SWFMorph::getShape2
===================

Gets a handle to the ending shape

### 说明

<span class="type">SWFShape</span> <span
class="methodname">SWFMorph::getShape2</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Gets the morph's ending shape.

### 返回值

Returns a <a href="/class/swfshape.html" class="xref">SWFShape</a>
object.

### 参见

-   <span class="function">SWFMorph::getShape1</span>

简介
----

<span class="classname">SWFMovie</span> is a movie object representing
an SWF movie.

类摘要
------

**SWFMovie**

<span class="ooclass"> class **SWFMovie** </span> {

/\* 方法 \*/

<span class="type">mixed</span> <span class="methodname">add</span> (
<span class="methodparam"><span class="type">object</span>
`$instance`</span> )

<span class="type">void</span> <span class="methodname">addExport</span>
( <span class="methodparam"><span class="type">SWFCharacter</span>
`$char`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> )

<span class="type">mixed</span> <span class="methodname">addFont</span>
( <span class="methodparam"><span class="type">SWFFont</span>
`$font`</span> )

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$version`</span> \] )

<span class="type">SWFSprite</span> <span
class="methodname">importChar</span> ( <span class="methodparam"><span
class="type">string</span> `$libswf`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="type">SWFFontChar</span> <span
class="methodname">importFont</span> ( <span class="methodparam"><span
class="type">string</span> `$libswf`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="type">void</span> <span
class="methodname">labelFrame</span> ( <span class="methodparam"><span
class="type">string</span> `$label`</span> )

<span class="type">void</span> <span class="methodname">nextFrame</span>
( <span class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">output</span> (\[
<span class="methodparam"><span class="type">int</span>
`$compression`</span> \] )

<span class="type">void</span> <span class="methodname">remove</span> (
<span class="methodparam"><span class="type">object</span>
`$instance`</span> )

<span class="type">int</span> <span class="methodname">save</span> (
<span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">int</span> `$compression`<span class="initializer"> =
-1</span></span> \] )

<span class="type">int</span> <span class="methodname">saveToFile</span>
( <span class="methodparam"><span class="type">resource</span>
`$x`</span> \[, <span class="methodparam"><span class="type">int</span>
`$compression`<span class="initializer"> = -1</span></span> \] )

<span class="type">void</span> <span
class="methodname">setbackground</span> ( <span
class="methodparam"><span class="type">int</span> `$red`</span> , <span
class="methodparam"><span class="type">int</span> `$green`</span> ,
<span class="methodparam"><span class="type">int</span> `$blue`</span> )

<span class="type">void</span> <span
class="methodname">setDimension</span> ( <span class="methodparam"><span
class="type">float</span> `$width`</span> , <span
class="methodparam"><span class="type">float</span> `$height`</span> )

<span class="type">void</span> <span class="methodname">setFrames</span>
( <span class="methodparam"><span class="type">int</span>
`$number`</span> )

<span class="type">void</span> <span class="methodname">setRate</span> (
<span class="methodparam"><span class="type">float</span> `$rate`</span>
)

<span class="type">SWFSoundInstance</span> <span
class="methodname">startSound</span> ( <span class="methodparam"><span
class="type">SWFSound</span> `$sound`</span> )

<span class="type">void</span> <span class="methodname">stopSound</span>
( <span class="methodparam"><span class="type">SWFSound</span>
`$sound`</span> )

<span class="type">int</span> <span class="methodname">streamMP3</span>
( <span class="methodparam"><span class="type">mixed</span>
`$mp3file`</span> \[, <span class="methodparam"><span
class="type">float</span> `$skip`<span class="initializer"> =
0</span></span> \] )

<span class="type">void</span> <span
class="methodname">writeExports</span> ( <span
class="methodparam">void</span> )

}

SWFMovie::add
=============

Adds any type of data to a movie

### 说明

<span class="type">mixed</span> <span
class="methodname">SWFMovie::add</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Adds an SWF object `instance` to the current movie.

### 参数

`instance`  
Any type of object instance, like
<a href="/class/swfshape.html" class="xref">SWFShape</a>,
<a href="/class/swftext.html" class="xref">SWFText</a>,
<a href="/class/swffont.html" class="xref">SWFFont</a>.

### 返回值

For displayable types (shape, text, button, sprite), this returns an
<a href="/class/swfdisplayitem.html" class="xref">SWFDisplayItem</a>, a
handle to the object in a display list. Thus, you can add the same shape
to a movie multiple times and get separate handles back for each
separate instance.

### 参见

-   <span class="function">SWFMovie::remove</span>

SWFMovie::addExport
===================

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::addExport</span> ( <span
class="methodparam"><span class="type">SWFCharacter</span>
`$char`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFMovie::addFont
=================

### 说明

<span class="type">mixed</span> <span
class="methodname">SWFMovie::addFont</span> ( <span
class="methodparam"><span class="type">SWFFont</span> `$font`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFMovie::\_\_construct
=======================

Creates a new movie object, representing an SWF version 4 movie

### 说明

<span class="methodname">SWFMovie::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$version`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new movie object, representing an SWF movie.

### 参数

`version`  
The desired SWF version. Default is 4.

SWFMovie::importChar
====================

### 说明

<span class="type">SWFSprite</span> <span
class="methodname">SWFMovie::importChar</span> ( <span
class="methodparam"><span class="type">string</span> `$libswf`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFMovie::importFont</span>

SWFMovie::importFont
====================

### 说明

<span class="type">SWFFontChar</span> <span
class="methodname">SWFMovie::importFont</span> ( <span
class="methodparam"><span class="type">string</span> `$libswf`</span> ,
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFMovie::importChar</span>

SWFMovie::labelFrame
====================

Labels a frame

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::labelFrame</span> ( <span
class="methodparam"><span class="type">string</span> `$label`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFMovie::nextFrame
===================

Moves to the next frame of the animation

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::nextFrame</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Moves to the next frame of the animation.

### 返回值

没有返回值。

SWFMovie::output
================

Dumps your lovingly prepared movie out

### 说明

<span class="type">int</span> <span
class="methodname">SWFMovie::output</span> (\[ <span
class="methodparam"><span class="type">int</span> `$compression`</span>
\] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Dumps the <span class="classname">SWFMovie</span>.

Don't forget to send the *Content-Type* HTTP header file before using
this function, in order to display the movie in a browser.

### 参数

`compression`  
The compression level can be a value between 0 and 9, defining the SWF
compression similar to gzip compression.

This parameter is only available as of Flash MX (6).

### 返回值

Return the number of bytes written or **`FALSE`** on error.

### 范例

**示例 \#1 Displaying your $movie in a browser**

``` php
<?php
header('Content-type: application/x-shockwave-flash'); 
$movie->output();
?>
```

### 参见

-   <span class="function">SWFMovie::save</span>
-   <span class="function">SWFMovie::saveToFile</span>

SWFMovie::remove
================

Removes the object instance from the display list

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::remove</span> ( <span
class="methodparam"><span class="type">object</span> `$instance`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Removes the given object `instance` from the display list.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFMovie::add</span>

SWFMovie::save
==============

Saves the SWF movie in a file

### 说明

<span class="type">int</span> <span
class="methodname">SWFMovie::save</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$compression`<span class="initializer"> = -1</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Saves the SWF movie to the specified `filename`.

### 参数

`filename`  
The path to the saved SWF document.

`compression`  
The compression level can be a value between 0 and 9, defining the SWF
compression similar to gzip compression.

This parameter is only available as of Flash MX (6).

### 返回值

Return the number of bytes written or **`FALSE`** on error.

### 参见

-   <span class="function">SWFMovie::output</span>
-   <span class="function">SWFMovie::saveToFile</span>

SWFMovie::saveToFile
====================

### 说明

<span class="type">int</span> <span
class="methodname">SWFMovie::saveToFile</span> ( <span
class="methodparam"><span class="type">resource</span> `$x`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$compression`<span class="initializer"> = -1</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`X`  

`compression`  
The compression level can be a value between 0 and 9, defining the SWF
compression similar to gzip compression.

This parameter is only available as of Flash MX (6).

### 返回值

Return the number of bytes written or **`FALSE`** on error.

### 参见

-   <span class="function">SWFMovie::output</span>
-   <span class="function">SWFMovie::save</span>

SWFMovie::setbackground
=======================

Sets the background color

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::setbackground</span> ( <span
class="methodparam"><span class="type">int</span> `$red`</span> , <span
class="methodparam"><span class="type">int</span> `$green`</span> ,
<span class="methodparam"><span class="type">int</span> `$blue`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the background color.

Why is there no rgba version? Think about it, you might want to let the
HTML background show through. There's a way to do that, but it only
works on IE4. Search the
<a href="http://www.macromedia.com/" class="link external">» http://www.macromedia.com/</a>
site for details.

### 参数

These parameters are integers between 0 and 255 or hexadecimals between
*0x00* and *0xFF*:

`red`  
Value of red component

`green`  
Value of green component

`blue`  
Value of blue component

### 返回值

没有返回值。

SWFMovie::setDimension
======================

Sets the movie's width and height

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::setDimension</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the movie's dimension to the specified `width` and `height`.

### 参数

`width`  
The movie width.

`height`  
The movie height.

### 返回值

没有返回值。

SWFMovie::setFrames
===================

Sets the total number of frames in the animation

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::setFrames</span> ( <span
class="methodparam"><span class="type">int</span> `$number`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the total number of frames in the animation to the given `number`.

### 参数

`number`  
The number of frames.

### 返回值

没有返回值。

SWFMovie::setRate
=================

Sets the animation's frame rate

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::setRate</span> ( <span
class="methodparam"><span class="type">float</span> `$rate`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets the frame rate to the specified `rate`.

Animation will slow down if the player can't render frames fast enough-
unless there's a streaming sound, in which case display frames are
sacrificed to keep sound from skipping.

### 参数

`rate`  
The frame rate, in frame per seconds.

### 返回值

没有返回值。

SWFMovie::startSound
====================

### 说明

<span class="type">SWFSoundInstance</span> <span
class="methodname">SWFMovie::startSound</span> ( <span
class="methodparam"><span class="type">SWFSound</span> `$sound`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFMovie::stopSound</span>

SWFMovie::stopSound
===================

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::stopSound</span> ( <span
class="methodparam"><span class="type">SWFSound</span> `$sound`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFMovie::startSound</span>

SWFMovie::streamMP3
===================

Streams a MP3 file

### 说明

<span class="type">int</span> <span
class="methodname">SWFMovie::streamMP3</span> ( <span
class="methodparam"><span class="type">mixed</span> `$mp3file`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$skip`<span class="initializer"> = 0</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Streams the given MP3 file `mp3file`.

This method is not very robust in dealing with oddities (can skip over
an initial ID3 tag, but that's about it).

Note that the movie isn't smart enough to put enough frames in to
contain the entire mp3 stream- you'll have to add (length of song \*
frames per second) frames to get the entire stream in.

### 参数

`mp3file`  
Can be a file pointer returned by <span class="function">fopen</span> or
the MP3 data, as a binary string.

`skip`  
Number of seconds to skip.

### 返回值

Return number of frames.

### 更新日志

| 版本  | 说明         |
|-------|--------------|
| 5.2.0 | `skip` added |

### 范例

**示例 \#1 Streaming example**

``` php
<?php
$m = new SWFMovie();
$m->setRate(12.0);
$m->streamMp3(file_get_contents("distortobass.mp3"));
// use your own MP3

// The file is 11.85 seconds at 12.0 fps = 142 frames
$m->setFrames(142);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFMovie::writeExports
======================

### 说明

<span class="type">void</span> <span
class="methodname">SWFMovie::writeExports</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

简介
----

SWFPrebuiltClip.

类摘要
------

**SWFPrebuiltClip**

<span class="ooclass"> class **SWFPrebuiltClip** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$file`</span> )

}

SWFPrebuiltClip::\_\_construct
==============================

Returns a SWFPrebuiltClip object

### 说明

<span class="methodname">SWFPrebuiltClip::\_\_construct</span> ( <span
class="methodparam"><span class="type">mixed</span> `$file`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

简介
----

SWFShape.

类摘要
------

**SWFShape**

<span class="ooclass"> class **SWFShape** </span> {

/\* 方法 \*/

<span class="type">SWFFill</span> <span
class="methodname">addFill</span> ( <span class="methodparam"><span
class="type">int</span> `$red`</span> , <span class="methodparam"><span
class="type">int</span> `$green`</span> , <span
class="methodparam"><span class="type">int</span> `$blue`</span> \[,
<span class="methodparam"><span class="type">int</span> `$alpha`<span
class="initializer"> = 255</span></span> \] )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">drawArc</span> (
<span class="methodparam"><span class="type">float</span> `$r`</span> ,
<span class="methodparam"><span class="type">float</span>
`$startAngle`</span> , <span class="methodparam"><span
class="type">float</span> `$endAngle`</span> )

<span class="type">void</span> <span
class="methodname">drawCircle</span> ( <span class="methodparam"><span
class="type">float</span> `$r`</span> )

<span class="type">int</span> <span class="methodname">drawCubic</span>
( <span class="methodparam"><span class="type">float</span> `$bx`</span>
, <span class="methodparam"><span class="type">float</span> `$by`</span>
, <span class="methodparam"><span class="type">float</span> `$cx`</span>
, <span class="methodparam"><span class="type">float</span> `$cy`</span>
, <span class="methodparam"><span class="type">float</span> `$dx`</span>
, <span class="methodparam"><span class="type">float</span> `$dy`</span>
)

<span class="type">int</span> <span
class="methodname">drawCubicTo</span> ( <span class="methodparam"><span
class="type">float</span> `$bx`</span> , <span class="methodparam"><span
class="type">float</span> `$by`</span> , <span class="methodparam"><span
class="type">float</span> `$cx`</span> , <span class="methodparam"><span
class="type">float</span> `$cy`</span> , <span class="methodparam"><span
class="type">float</span> `$dx`</span> , <span class="methodparam"><span
class="type">float</span> `$dy`</span> )

<span class="type">int</span> <span class="methodname">drawCurve</span>
( <span class="methodparam"><span class="type">float</span>
`$controldx`</span> , <span class="methodparam"><span
class="type">float</span> `$controldy`</span> , <span
class="methodparam"><span class="type">float</span> `$anchordx`</span> ,
<span class="methodparam"><span class="type">float</span>
`$anchordy`</span> \[, <span class="methodparam"><span
class="type">float</span> `$targetdx`</span> \], <span
class="methodparam"><span class="type">float</span> `$targetdy`</span> )

<span class="type">int</span> <span
class="methodname">drawCurveTo</span> ( <span class="methodparam"><span
class="type">float</span> `$controlx`</span> , <span
class="methodparam"><span class="type">float</span> `$controly`</span> ,
<span class="methodparam"><span class="type">float</span>
`$anchorx`</span> , <span class="methodparam"><span
class="type">float</span> `$anchory`</span> \[, <span
class="methodparam"><span class="type">float</span> `$targetx`</span>
\], <span class="methodparam"><span class="type">float</span>
`$targety`</span> )

<span class="type">void</span> <span class="methodname">drawGlyph</span>
( <span class="methodparam"><span class="type">SWFFont</span>
`$font`</span> , <span class="methodparam"><span
class="type">string</span> `$character`</span> \[, <span
class="methodparam"><span class="type">int</span> `$size`</span> \] )

<span class="type">void</span> <span class="methodname">drawLine</span>
( <span class="methodparam"><span class="type">float</span> `$dx`</span>
, <span class="methodparam"><span class="type">float</span> `$dy`</span>
)

<span class="type">void</span> <span
class="methodname">drawLineTo</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

<span class="type">void</span> <span class="methodname">movePen</span> (
<span class="methodparam"><span class="type">float</span> `$dx`</span> ,
<span class="methodparam"><span class="type">float</span> `$dy`</span> )

<span class="type">void</span> <span class="methodname">movePenTo</span>
( <span class="methodparam"><span class="type">float</span> `$x`</span>
, <span class="methodparam"><span class="type">float</span> `$y`</span>
)

<span class="type">void</span> <span
class="methodname">setLeftFill</span> ( <span class="methodparam"><span
class="type">SWFGradient</span> `$fill`</span> )

<span class="type">void</span> <span class="methodname">setLine</span> (
<span class="methodparam"><span class="type">SWFShape</span>
`$shape`</span> )

<span class="type">void</span> <span
class="methodname">setRightFill</span> ( <span class="methodparam"><span
class="type">SWFGradient</span> `$fill`</span> )

}

SWFShape::addFill
=================

Adds a solid fill to the shape

### 说明

<span class="type">SWFFill</span> <span
class="methodname">SWFShape::addFill</span> ( <span
class="methodparam"><span class="type">int</span> `$red`</span> , <span
class="methodparam"><span class="type">int</span> `$green`</span> ,
<span class="methodparam"><span class="type">int</span> `$blue`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$alpha`<span class="initializer"> = 255</span></span> \] )

<span class="type">SWFFill</span> <span
class="methodname">addFill</span> ( <span class="methodparam"><span
class="type">SWFBitmap</span> `$bitmap`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

<span class="type">SWFFill</span> <span
class="methodname">addFill</span> ( <span class="methodparam"><span
class="type">SWFGradient</span> `$gradient`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">SWFShape::addFill</span> adds a solid fill to the
shape's list of fill styles. <span
class="function">SWFShape::addFill</span> accepts three different types
of arguments.

`red`, `green`, `blue` is a color (RGB mode).

The `bitmap` argument is an <span class="function">SWFBitmap</span>
object. The `flags` argument can be one of the following values:
SWFFILL\_CLIPPED\_BITMAP, SWFFILL\_TILED\_BITMAP,
SWFFILL\_LINEAR\_GRADIENT or SWFFILL\_RADIAL\_GRADIENT. Default is
SWFFILL\_TILED\_BITMAP for SWFBitmap and SWFFILL\_LINEAR\_GRADIENT for
SWFGradient.

The `gradient` argument is an <span class="function">SWFGradient</span>
object. The flags argument can be one of the following values :
SWFFILL\_RADIAL\_GRADIENT or SWFFILL\_LINEAR\_GRADIENT. Default is
SWFFILL\_LINEAR\_GRADIENT. I'm sure about this one. Really.

<span class="function">SWFShape::addFill</span> returns an <span
class="function">SWFFill</span> object for use with the <span
class="function">SWFShape::setLeftFill</span> and <span
class="function">SWFShape::setRightFill</span> functions described
below.

### 范例

This simple example will draw a frame on a bitmap. Ah, here's another
buglet in the flash player- it doesn't seem to care about the second
shape's bitmap's transformation in a morph. According to spec, the
bitmap should stretch along with the shape in this example..

**示例 \#1 <span class="function">SWFShape::addFill</span> example**

``` php
<?php

$p = new SWFMorph();

$b = new SWFBitmap(file_get_contents("alphafill.jpg"));
// use your own bitmap
$width = $b->getWidth();
$height = $b->getHeight();

$s = $p->getShape1();
$f = $s->addFill($b, SWFFILL_TILED_BITMAP);
$f->moveTo(-$width/2, -$height/4);
$f->scaleTo(1.0, 0.5);
$s->setLeftFill($f);
$s->movePenTo(-$width/2, -$height/4);
$s->drawLine($width, 0);
$s->drawLine(0, $height/2);
$s->drawLine(-$width, 0);
$s->drawLine(0, -$height/2);

$s = $p->getShape2();
$f = $s->addFill($b, SWFFILL_TILED_BITMAP);

// these two have no effect!
$f->moveTo(-$width/4, -$height/2);
$f->scaleTo(0.5, 1.0);

$s->setLeftFill($f);
$s->movePenTo(-$width/4, -$height/2);
$s->drawLine($width/2, 0);
$s->drawLine(0, $height);
$s->drawLine(-$width/2, 0);
$s->drawLine(0, -$height);

$m = new SWFMovie();
$m->setDimension($width, $height);
$i = $m->add($p);
$i->moveTo($width/2, $height/2);

for ($n=0; $n<1.001; $n+=0.03) {
    $i->setRatio($n);
    $m->nextFrame();
}

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

### 参见

-   <span class="function">SWFShape::setLeftFill</span>
-   <span class="function">SWFShape::setRightFill</span>

SWFShape::\_\_construct
=======================

Creates a new shape object

### 说明

<span class="methodname">SWFShape::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Created a new <span class="classname">SWFShape</span> object.

### 范例

This simple example will draw a big red elliptic quadrant.

**示例 \#1 <span class="function">swfshape</span> example**

``` php
<?php
$s = new SWFShape();
$s->setLine(40, 0x7f, 0, 0);
$s->setRightFill($s->addFill(0xff, 0, 0));
$s->movePenTo(200, 200);
$s->drawLineTo(6200, 200);
$s->drawLineTo(6200, 4600);
$s->drawCurveTo(200, 4600, 200, 200);

$m = new SWFMovie();
$m->setDimension(6400, 4800);
$m->setRate(12.0);
$m->add($s);
$m->nextFrame();

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFShape::drawArc
=================

Draws an arc of radius r centered at the current location, from angle
startAngle to angle endAngle measured clockwise from 12 o'clock

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::drawArc</span> ( <span
class="methodparam"><span class="type">float</span> `$r`</span> , <span
class="methodparam"><span class="type">float</span> `$startAngle`</span>
, <span class="methodparam"><span class="type">float</span>
`$endAngle`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::drawCircle</span>

SWFShape::drawCircle
====================

Draws a circle of radius r centered at the current location, in a
counter-clockwise fashion

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::drawCircle</span> ( <span
class="methodparam"><span class="type">float</span> `$r`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFShape::drawCubic
===================

Draws a cubic bezier curve using the current position and the three
given points as control points

### 说明

<span class="type">int</span> <span
class="methodname">SWFShape::drawCubic</span> ( <span
class="methodparam"><span class="type">float</span> `$bx`</span> , <span
class="methodparam"><span class="type">float</span> `$by`</span> , <span
class="methodparam"><span class="type">float</span> `$cx`</span> , <span
class="methodparam"><span class="type">float</span> `$cy`</span> , <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFShape::drawCubicTo</span>

SWFShape::drawCubicTo
=====================

Draws a cubic bezier curve using the current position and the three
given points as control points

### 说明

<span class="type">int</span> <span
class="methodname">SWFShape::drawCubicTo</span> ( <span
class="methodparam"><span class="type">float</span> `$bx`</span> , <span
class="methodparam"><span class="type">float</span> `$by`</span> , <span
class="methodparam"><span class="type">float</span> `$cx`</span> , <span
class="methodparam"><span class="type">float</span> `$cy`</span> , <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFShape::drawCubic</span>

SWFShape::drawCurve
===================

Draws a curve (relative)

### 说明

<span class="type">int</span> <span
class="methodname">SWFShape::drawCurve</span> ( <span
class="methodparam"><span class="type">float</span> `$controldx`</span>
, <span class="methodparam"><span class="type">float</span>
`$controldy`</span> , <span class="methodparam"><span
class="type">float</span> `$anchordx`</span> , <span
class="methodparam"><span class="type">float</span> `$anchordy`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$targetdx`</span> \], <span class="methodparam"><span
class="type">float</span> `$targetdy`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::drawcurve</span> draws a quadratic
curve (using the current line style,set by <span
class="function">swfshape::setline</span>) from the current pen position
to the relative position (`anchorx`,`anchory`) using relative control
point (`controlx`,`controly`). That is, head towards the control point,
then smoothly turn to the anchor point.

With 6 parameters, it draws a cubic bezier to point (x+`targetdx`,
x+`targetdy`) with control points (x+`controldx`, y+`controldy`) and
(x+`anchordx`, y+`anchordy`).

### 参见

-   <span class="function">SWFShape::drawCurve</span>

SWFShape::drawCurveTo
=====================

Draws a curve

### 说明

<span class="type">int</span> <span
class="methodname">SWFShape::drawCurveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$controlx`</span> ,
<span class="methodparam"><span class="type">float</span>
`$controly`</span> , <span class="methodparam"><span
class="type">float</span> `$anchorx`</span> , <span
class="methodparam"><span class="type">float</span> `$anchory`</span>
\[, <span class="methodparam"><span class="type">float</span>
`$targetx`</span> \], <span class="methodparam"><span
class="type">float</span> `$targety`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::drawcurveto</span> draws a quadratic
curve (using the current line style, set by <span
class="function">swfshape::setline</span>) from the current pen position
to (`anchorx`,`anchory`) using (`controlx`,`controly`) as a control
point. That is, head towards the control point, then smoothly turn to
the anchor point.

With 6 parameters, it draws a cubic bezier to point (`targetx`,
`targety`) with control points (`controlx`, `controly`) and (`anchorx`,
`anchory`).

### 参见

-   <span class="function">SWFShape::drawCurveTo</span>

SWFShape::drawGlyph
===================

Draws the first character in the given string into the shape using the
glyph definition from the given font

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::drawGlyph</span> ( <span
class="methodparam"><span class="type">SWFFont</span> `$font`</span> ,
<span class="methodparam"><span class="type">string</span>
`$character`</span> \[, <span class="methodparam"><span
class="type">int</span> `$size`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFShape::drawLine
==================

Draws a line (relative)

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::drawLine</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::drawline</span> draws a line (using the
current line style set by <span
class="function">swfshape::setline</span>) from the current pen position
to displacement (`dx`,`dy`).

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::drawLineTo</span>

SWFShape::drawLineTo
====================

Draws a line

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::drawLineTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::setrightfill</span> draws a line (using
the current line style, set by <span
class="function">swfshape::setline</span>) from the current pen position
to point (`x`,`y`) in the shape's coordinate space.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::drawLine</span>

SWFShape::movePen
=================

Moves the shape's pen (relative)

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::movePen</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::setrightfill</span> move the shape's
pen from coordinates (current x,current y) to (current x + `dx`, current
y + `dy`) in the shape's coordinate space.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::movePenTo</span>

SWFShape::movePenTo
===================

Moves the shape's pen

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::movePenTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::setrightfill</span> move the shape's
pen to (`x`,`y`) in the shape's coordinate space.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::movePen</span>

SWFShape::setLeftFill
=====================

Sets left rasterizing color

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::setLeftFill</span> ( <span
class="methodparam"><span class="type">SWFGradient</span> `$fill`</span>
)

<span class="type">void</span> <span
class="methodname">setLeftFill</span> ( <span class="methodparam"><span
class="type">int</span> `$red`</span> , <span class="methodparam"><span
class="type">int</span> `$green`</span> , <span
class="methodparam"><span class="type">int</span> `$blue`</span> \[,
<span class="methodparam"><span class="type">int</span> `$a`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

What this nonsense is about is, every edge segment borders at most two
fills. When rasterizing the object, it's pretty handy to know what those
fills are ahead of time, so the swf format requires these to be
specified.

<span class="function">swfshape::setleftfill</span> sets the fill on the
left side of the edge- that is, on the interior if you're defining the
outline of the shape in a counter-clockwise fashion. The fill object is
an SWFFill object returned from one of the addFill functions above.

This seems to be reversed when you're defining a shape in a morph,
though. If your browser crashes, just try setting the fill on the other
side.

Shortcut for *$swfshape-\>setleftfill($s-\>addfill($r, $g, $b \[,
$a\]));*.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::setRightFill</span>

SWFShape::setLine
=================

Sets the shape's line style

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::setLine</span> ( <span
class="methodparam"><span class="type">SWFShape</span> `$shape`</span> )

<span class="type">void</span> <span class="methodname">setLine</span> (
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span> `$red`</span>
, <span class="methodparam"><span class="type">int</span>
`$green`</span> , <span class="methodparam"><span
class="type">int</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">int</span> `$a`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfshape::setline</span> sets the shape's line
style. `width` is the line's width. If `width` is 0, the line's style is
removed (then, all other arguments are ignored). If `width` \> 0, then
line's color is set to `red`, `green`, `blue`. Last parameter `a` is
optional.

You must declare all line styles before you use them (see example).

### 返回值

没有返回值。

### 范例

This simple example will draw a big "!\#%\*@", in funny colors and
gracious style.

**示例 \#1 <span class="function">swfshape::setline</span> example**

``` php
<?php
$s = new SWFShape();
$f1 = $s->addFill(0xff, 0, 0);
$f2 = $s->addFill(0xff, 0x7f, 0);
$f3 = $s->addFill(0xff, 0xff, 0);
$f4 = $s->addFill(0, 0xff, 0);
$f5 = $s->addFill(0, 0, 0xff);

// bug: have to declare all line styles before you use them
$s->setLine(40, 0x7f, 0, 0);
$s->setLine(40, 0x7f, 0x3f, 0);
$s->setLine(40, 0x7f, 0x7f, 0);
$s->setLine(40, 0, 0x7f, 0);
$s->setLine(40, 0, 0, 0x7f);

$f = new SWFFont('Techno.fdb');

$s->setRightFill($f1);
$s->setLine(40, 0x7f, 0, 0);
$s->drawGlyph($f, '!');
$s->movePen($f->getWidth('!'), 0);

$s->setRightFill($f2);
$s->setLine(40, 0x7f, 0x3f, 0);
$s->drawGlyph($f, '#');
$s->movePen($f->getWidth('#'), 0);

$s->setRightFill($f3);
$s->setLine(40, 0x7f, 0x7f, 0);
$s->drawGlyph($f, '%');
$s->movePen($f->getWidth('%'), 0);

$s->setRightFill($f4);
$s->setLine(40, 0, 0x7f, 0);
$s->drawGlyph($f, '*');
$s->movePen($f->getWidth('*'), 0);

$s->setRightFill($f5);
$s->setLine(40, 0, 0, 0x7f);
$s->drawGlyph($f, '@');

$m = new SWFMovie();
$m->setDimension(3000,2000);
$m->setRate(12.0);
$i = $m->add($s);
$i->moveTo(1500-$f->getWidth("!#%*@")/2, 1000+$f->getAscent()/2);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

### 返回值

没有返回值。

SWFShape::setRightFill
======================

Sets right rasterizing color

### 说明

<span class="type">void</span> <span
class="methodname">SWFShape::setRightFill</span> ( <span
class="methodparam"><span class="type">SWFGradient</span> `$fill`</span>
)

<span class="type">void</span> <span
class="methodname">setRightFill</span> ( <span class="methodparam"><span
class="type">int</span> `$red`</span> , <span class="methodparam"><span
class="type">int</span> `$green`</span> , <span
class="methodparam"><span class="type">int</span> `$blue`</span> \[,
<span class="methodparam"><span class="type">int</span> `$a`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Shortcut for *$swfshape-\>setrightfill($s-\>addfill($r, $g, $b \[,
$a\]));*.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFShape::setLeftFill</span>

简介
----

SWFSound.

类摘要
------

**SWFSound**

<span class="ooclass"> class **SWFSound** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = 0</span></span> \] )

}

SWFSound::\_\_construct
=======================

Returns a new SWFSound object from given file

### 说明

<span class="methodname">SWFSound::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = 0</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

简介
----

<span class="classname">SWFSoundInstance</span> objects are returned by
the <span class="function">SWFSprite::startSound</span> and <span
class="function">SWFMovie::startSound</span> methods.

类摘要
------

**SWFSoundInstance**

<span class="ooclass"> class **SWFSoundInstance** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">loopCount</span>
( <span class="methodparam"><span class="type">int</span>
`$point`</span> )

<span class="type">void</span> <span
class="methodname">loopInPoint</span> ( <span class="methodparam"><span
class="type">int</span> `$point`</span> )

<span class="type">void</span> <span
class="methodname">loopOutPoint</span> ( <span class="methodparam"><span
class="type">int</span> `$point`</span> )

<span class="type">void</span> <span
class="methodname">noMultiple</span> ( <span
class="methodparam">void</span> )

}

SWFSoundInstance::loopCount
===========================

### 说明

<span class="type">void</span> <span
class="methodname">SWFSoundInstance::loopCount</span> ( <span
class="methodparam"><span class="type">int</span> `$point`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`point`  

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFSoundInstance::loopOutPoint</span>

SWFSoundInstance::loopInPoint
=============================

### 说明

<span class="type">void</span> <span
class="methodname">SWFSoundInstance::loopInPoint</span> ( <span
class="methodparam"><span class="type">int</span> `$point`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`point`  

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFSoundInstance::loopOutPoint</span>

SWFSoundInstance::loopOutPoint
==============================

### 说明

<span class="type">void</span> <span
class="methodname">SWFSoundInstance::loopOutPoint</span> ( <span
class="methodparam"><span class="type">int</span> `$point`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`point`  

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFSoundInstance::loopInPoint</span>

SWFSoundInstance::noMultiple
============================

### 说明

<span class="type">void</span> <span
class="methodname">SWFSoundInstance::noMultiple</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

简介
----

An <span class="classname">SWFSprite</span> is also known as a "movie
clip", this allows one to create objects which are animated in their own
timelines. Hence, the sprite has most of the same methods as the movie.

类摘要
------

**SWFSprite**

<span class="ooclass"> class **SWFSprite** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">add</span> (
<span class="methodparam"><span class="type">object</span>
`$object`</span> )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="type">void</span> <span
class="methodname">labelFrame</span> ( <span class="methodparam"><span
class="type">string</span> `$label`</span> )

<span class="type">void</span> <span class="methodname">nextFrame</span>
( <span class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">remove</span> (
<span class="methodparam"><span class="type">object</span>
`$object`</span> )

<span class="type">void</span> <span class="methodname">setFrames</span>
( <span class="methodparam"><span class="type">int</span>
`$number`</span> )

<span class="type">SWFSoundInstance</span> <span
class="methodname">startSound</span> ( <span class="methodparam"><span
class="type">SWFSound</span> `$sount`</span> )

<span class="type">void</span> <span class="methodname">stopSound</span>
( <span class="methodparam"><span class="type">SWFSound</span>
`$sount`</span> )

}

SWFSprite::add
==============

Adds an object to a sprite

### 说明

<span class="type">void</span> <span
class="methodname">SWFSprite::add</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfsprite::add</span> adds a <span
class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span>, a <span
class="function">swfaction</span> or a <span
class="function">swfsprite</span> object.

For displayable types (<span class="function">swfshape</span>, <span
class="function">swfbutton</span>, <span
class="function">swftext</span>, <span class="function">swfaction</span>
or <span class="function">swfsprite</span>), this returns a handle to
the object in a display list.

### 返回值

没有返回值。

SWFSprite::\_\_construct
========================

Creates a movie clip (a sprite)

### 说明

<span class="methodname">SWFSprite::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new <span class="classname">SWFSprite</span> object.

SWFSprite::labelFrame
=====================

Labels frame

### 说明

<span class="type">void</span> <span
class="methodname">SWFSprite::labelFrame</span> ( <span
class="methodparam"><span class="type">string</span> `$label`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFSprite::nextFrame
====================

Moves to the next frame of the animation

### 说明

<span class="type">void</span> <span
class="methodname">SWFSprite::nextFrame</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfsprite::setframes</span> moves to the next
frame of the animation.

### 返回值

没有返回值。

SWFSprite::remove
=================

Removes an object to a sprite

### 说明

<span class="type">void</span> <span
class="methodname">SWFSprite::remove</span> ( <span
class="methodparam"><span class="type">object</span> `$object`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfsprite::remove</span> remove a <span
class="function">swfshape</span>, a <span
class="function">swfbutton</span>, a <span
class="function">swftext</span>, a <span
class="function">swfaction</span> or a <span
class="function">swfsprite</span> object from the sprite.

### 返回值

没有返回值。

SWFSprite::setFrames
====================

Sets the total number of frames in the animation

### 说明

<span class="type">void</span> <span
class="methodname">SWFSprite::setFrames</span> ( <span
class="methodparam"><span class="type">int</span> `$number`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swfsprite::setframes</span> sets the total number
of frames in the animation to `numberofframes`.

### 返回值

没有返回值。

SWFSprite::startSound
=====================

### 说明

<span class="type">SWFSoundInstance</span> <span
class="methodname">SWFSprite::startSound</span> ( <span
class="methodparam"><span class="type">SWFSound</span> `$sount`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFSprite::stopSound</span>

SWFSprite::stopSound
====================

### 说明

<span class="type">void</span> <span
class="methodname">SWFSprite::stopSound</span> ( <span
class="methodparam"><span class="type">SWFSound</span> `$sount`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFSprite::startSound</span>

简介
----

SWFText.

类摘要
------

**SWFText**

<span class="ooclass"> class **SWFText** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">addString</span>
( <span class="methodparam"><span class="type">string</span>
`$string`</span> )

<span class="type">void</span> <span
class="methodname">addUTF8String</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getAscent</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getDescent</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getLeading</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getUTF8Width</span> ( <span class="methodparam"><span
class="type">string</span> `$string`</span> )

<span class="type">float</span> <span class="methodname">getWidth</span>
( <span class="methodparam"><span class="type">string</span>
`$string`</span> )

<span class="type">void</span> <span class="methodname">moveTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">void</span> <span class="methodname">setColor</span>
( <span class="methodparam"><span class="type">int</span> `$red`</span>
, <span class="methodparam"><span class="type">int</span>
`$green`</span> , <span class="methodparam"><span
class="type">int</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">int</span> `$a`<span
class="initializer"> = 255</span></span> \] )

<span class="type">void</span> <span class="methodname">setFont</span> (
<span class="methodparam"><span class="type">SWFFont</span>
`$font`</span> )

<span class="type">void</span> <span class="methodname">setHeight</span>
( <span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="type">void</span> <span
class="methodname">setSpacing</span> ( <span class="methodparam"><span
class="type">float</span> `$spacing`</span> )

}

SWFText::addString
==================

Draws a string

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::addString</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftext::addstring</span> draws the string
`string` at the current pen (cursor) location. Pen is at the baseline of
the text; i.e., ascending text is in the -y direction.

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFText::addUTF8String</span>

SWFText::addUTF8String
======================

Writes the given text into this SWFText object at the current pen
position, using the current font, height, spacing, and color

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::addUTF8String</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFText::addString</span>

SWFText::\_\_construct
======================

Creates a new SWFText object

### 说明

<span class="methodname">SWFText::\_\_construct</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new <span class="classname">SWFText</span> object, fresh for
manipulating.

### 范例

This simple example will draw a big yellow "PHP generates Flash with
Ming" text, on white background.

**示例 \#1 <span class="function">swftext</span> example**

``` php
<?php
$f = new SWFFont("Techno.fdb");
$t = new SWFText();
$t->setFont($f);
$t->moveTo(200, 2400);
$t->setColor(0xff, 0xff, 0);
$t->setHeight(1200);
$t->addString("PHP generates Flash with Ming!!");

$m = new SWFMovie();
$m->setDimension(5400, 3600);

$m->add($t);

header('Content-type: application/x-shockwave-flash');
$m->output();
?>
```

SWFText::getAscent
==================

Returns the ascent of the current font at its current size, or 0 if not
available

### 说明

<span class="type">float</span> <span
class="methodname">SWFText::getAscent</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFText::getDescent</span>

SWFText::getDescent
===================

Returns the descent of the current font at its current size, or 0 if not
available

### 说明

<span class="type">float</span> <span
class="methodname">SWFText::getDescent</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFText::getAscent</span>

SWFText::getLeading
===================

Returns the leading of the current font at its current size, or 0 if not
available

### 说明

<span class="type">float</span> <span
class="methodname">SWFText::getLeading</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

SWFText::getUTF8Width
=====================

Calculates the width of the given string in this text objects current
font and size

### 说明

<span class="type">float</span> <span
class="methodname">SWFText::getUTF8Width</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参见

-   <span class="function">SWFText::getWidth</span>

SWFText::getWidth
=================

Computes string's width

### 说明

<span class="type">float</span> <span
class="methodname">SWFText::getWidth</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the rendered width of the `string` at the text object's current
font, scale, and spacing settings.

### 参见

-   <span class="function">SWFText::getUTF8Width</span>

SWFText::moveTo
===============

Moves the pen

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::moveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftext::moveto</span> moves the pen (or cursor,
if that makes more sense) to (`x`,`y`) in text object's coordinate
space. If either is zero, though, value in that dimension stays the
same. Annoying, should be fixed.

### 返回值

没有返回值。

SWFText::setColor
=================

Sets the current text color

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::setColor</span> ( <span
class="methodparam"><span class="type">int</span> `$red`</span> , <span
class="methodparam"><span class="type">int</span> `$green`</span> ,
<span class="methodparam"><span class="type">int</span> `$blue`</span>
\[, <span class="methodparam"><span class="type">int</span> `$a`<span
class="initializer"> = 255</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Changes the current text color.

### 参数

These parameters are integers between 0 and 255 or hexadecimals between
*0x00* and *0xFF*:

`red`  
Value of red component

`green`  
Value of green component

`blue`  
Value of blue component

`a`  
Value of alpha component

### 返回值

没有返回值。

SWFText::setFont
================

Sets the current font

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::setFont</span> ( <span
class="methodparam"><span class="type">SWFFont</span> `$font`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftext::setfont</span> sets the current font to
`font`.

### 返回值

没有返回值。

SWFText::setHeight
==================

Sets the current font height

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::setHeight</span> ( <span
class="methodparam"><span class="type">float</span> `$height`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftext::setheight</span> sets the current font
height to `height`. Default is 240.

### 返回值

没有返回值。

SWFText::setSpacing
===================

Sets the current font spacing

### 说明

<span class="type">void</span> <span
class="methodname">SWFText::setSpacing</span> ( <span
class="methodparam"><span class="type">float</span> `$spacing`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftext::setspacing</span> sets the current font
spacing to `spacing`. Default is 1.0. 0 is all of the letters written at
the same point. This doesn't really work that well because it inflates
the advance across the letter, doesn't add the same amount of spacing
between the letters. I should try and explain that better, prolly. Or
just fix the damn thing to do constant spacing. This was really just a
way to figure out how letter advances work, anyway.. So nyah.

### 返回值

没有返回值。

简介
----

SWFTextField.

类摘要
------

**SWFTextField**

<span class="ooclass"> class **SWFTextField** </span> {

/\* 方法 \*/

<span class="type">void</span> <span class="methodname">addChars</span>
( <span class="methodparam"><span class="type">string</span>
`$chars`</span> )

<span class="type">void</span> <span class="methodname">addString</span>
( <span class="methodparam"><span class="type">string</span>
`$string`</span> )

<span class="type">void</span> <span class="methodname">align</span> (
<span class="methodparam"><span class="type">int</span>
`$alignement`</span> )

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

<span class="type">void</span> <span class="methodname">setBounds</span>
( <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

<span class="type">void</span> <span class="methodname">setColor</span>
( <span class="methodparam"><span class="type">int</span> `$red`</span>
, <span class="methodparam"><span class="type">int</span>
`$green`</span> , <span class="methodparam"><span
class="type">int</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">int</span> `$a`<span
class="initializer"> = 255</span></span> \] )

<span class="type">void</span> <span class="methodname">setFont</span> (
<span class="methodparam"><span class="type">SWFFont</span>
`$font`</span> )

<span class="type">void</span> <span class="methodname">setHeight</span>
( <span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="type">void</span> <span
class="methodname">setIndentation</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

<span class="type">void</span> <span
class="methodname">setLeftMargin</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

<span class="type">void</span> <span
class="methodname">setLineSpacing</span> ( <span
class="methodparam"><span class="type">float</span> `$height`</span> )

<span class="type">void</span> <span
class="methodname">setMargins</span> ( <span class="methodparam"><span
class="type">float</span> `$left`</span> , <span
class="methodparam"><span class="type">float</span> `$right`</span> )

<span class="type">void</span> <span class="methodname">setName</span> (
<span class="methodparam"><span class="type">string</span>
`$name`</span> )

<span class="type">void</span> <span
class="methodname">setPadding</span> ( <span class="methodparam"><span
class="type">float</span> `$padding`</span> )

<span class="type">void</span> <span
class="methodname">setRightMargin</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

}

SWFTextField::addChars
======================

Adds characters to a font that will be available within a textfield

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::addChars</span> ( <span
class="methodparam"><span class="type">string</span> `$chars`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

### 参见

-   <span class="function">SWFTextField::addString</span>

SWFTextField::addString
=======================

Concatenates the given string to the text field

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::addString</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setname</span> concatenates the
string `string` to the text field.

### 返回值

没有返回值。

SWFTextField::align
===================

Sets the text field alignment

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::align</span> ( <span
class="methodparam"><span class="type">int</span> `$alignement`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::align</span> sets the text field
alignment to `alignement`. Valid values for `alignement` are :
SWFTEXTFIELD\_ALIGN\_LEFT, SWFTEXTFIELD\_ALIGN\_RIGHT,
SWFTEXTFIELD\_ALIGN\_CENTER and SWFTEXTFIELD\_ALIGN\_JUSTIFY.

### 返回值

没有返回值。

SWFTextField::\_\_construct
===========================

Creates a text field object

### 说明

<span class="methodname">SWFTextField::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield</span> creates a new text field
object. Text Fields are less flexible than <span
class="function">swftext</span> objects- they can't be rotated, scaled
non-proportionally, or skewed, but they can be used as form entries, and
they can use browser-defined fonts.

The optional flags change the text field's behavior. It has the
following possibles values :

-   <span class="simpara"> SWFTEXTFIELD\_DRAWBOX draws the outline of
    the textfield </span>
-   <span class="simpara"> SWFTEXTFIELD\_HASLENGTH </span>
-   <span class="simpara"> SWFTEXTFIELD\_HTML allows text markup using
    HTML-tags </span>
-   <span class="simpara"> SWFTEXTFIELD\_MULTILINE allows multiple lines
    </span>
-   <span class="simpara"> SWFTEXTFIELD\_NOEDIT indicates that the field
    shouldn't be user-editable </span>
-   <span class="simpara"> SWFTEXTFIELD\_NOSELECT makes the field
    non-selectable </span>
-   <span class="simpara"> SWFTEXTFIELD\_PASSWORD obscures the data
    entry </span>
-   <span class="simpara"> SWFTEXTFIELD\_WORDWRAP allows text to wrap
    </span>

Flags are combined with the bitwise
<a href="/language/operators/bitwise.html" class="link">OR</a>
operation. For example,

``` php
<?php
$t = newSWFTextField(SWFTEXTFIELD_PASSWORD | SWFTEXTFIELD_NOEDIT); 
?>
```

creates a totally useless non-editable password field.

SWFTextField has the following methods : <span
class="function">swftextfield::setfont</span>, <span
class="function">swftextfield::setbounds</span>, <span
class="function">swftextfield::align</span>, <span
class="function">swftextfield::setheight</span>, <span
class="function">swftextfield::setleftmargin</span>, <span
class="function">swftextfield::setrightmargin</span>, <span
class="function">swftextfield::setmargins</span>, <span
class="function">swftextfield::setindentation</span>, <span
class="function">swftextfield::setlinespacing</span>, <span
class="function">swftextfield::setcolor</span>, <span
class="function">swftextfield::setname</span> and <span
class="function">swftextfield::addstring</span>.

SWFTextField::setBounds
=======================

Sets the text field width and height

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setBounds</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setbounds</span> sets the text
field width to `width` and height to `height`. If you don't set the
bounds yourself, Ming makes a poor guess at what the bounds are.

### 返回值

没有返回值。

SWFTextField::setColor
======================

Sets the color of the text field

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setColor</span> ( <span
class="methodparam"><span class="type">int</span> `$red`</span> , <span
class="methodparam"><span class="type">int</span> `$green`</span> ,
<span class="methodparam"><span class="type">int</span> `$blue`</span>
\[, <span class="methodparam"><span class="type">int</span> `$a`<span
class="initializer"> = 255</span></span> \] )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setcolor</span> sets the color of
the text field. Default is fully opaque black. Color is represented
using RGB system.

### 参数

These parameters are integers between 0 and 255 or hexadecimals between
*0x00* and *0xFF*:

`red`  
Value of red component

`green`  
Value of green component

`blue`  
Value of blue component

`a`  
Value of alpha component

### 返回值

没有返回值。

SWFTextField::setFont
=====================

Sets the text field font

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setFont</span> ( <span
class="methodparam"><span class="type">SWFFont</span> `$font`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setfont</span> sets the text field
font to the \[browser-defined?\] `font` font.

### 返回值

没有返回值。

SWFTextField::setHeight
=======================

Sets the font height of this text field font

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setHeight</span> ( <span
class="methodparam"><span class="type">float</span> `$height`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setheight</span> sets the font
height of this text field font to the given height `height`. Default is
240.

### 返回值

没有返回值。

SWFTextField::setIndentation
============================

Sets the indentation of the first line

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setIndentation</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setindentation</span> sets the
indentation of the first line in the text field, to `width`.

### 返回值

没有返回值。

SWFTextField::setLeftMargin
===========================

Sets the left margin width of the text field

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setLeftMargin</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setleftmargin</span> sets the left
margin width of the text field to `width`. Default is 0.

### 返回值

没有返回值。

SWFTextField::setLineSpacing
============================

Sets the line spacing of the text field

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setLineSpacing</span> ( <span
class="methodparam"><span class="type">float</span> `$height`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setlinespacing</span> sets the line
spacing of the text field to the height of `height`. Default is 40.

### 返回值

没有返回值。

SWFTextField::setMargins
========================

Sets the margins width of the text field

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setMargins</span> ( <span
class="methodparam"><span class="type">float</span> `$left`</span> ,
<span class="methodparam"><span class="type">float</span>
`$right`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setmargins</span> set both margins
at once, for the man on the go.

### 返回值

没有返回值。

SWFTextField::setName
=====================

Sets the variable name

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setName</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setname</span> sets the variable
name of this text field to `name`, for form posting and action scripting
purposes.

### 返回值

没有返回值。

SWFTextField::setPadding
========================

Sets the padding of this textfield

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setPadding</span> ( <span
class="methodparam"><span class="type">float</span> `$padding`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

SWFTextField::setRightMargin
============================

Sets the right margin width of the text field

### 说明

<span class="type">void</span> <span
class="methodname">SWFTextField::setRightMargin</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">swftextfield::setrightmargin</span> sets the
right margin width of the text field to `width`. Default is 0.

### 返回值

没有返回值。

简介
----

SWFVideoStream.

类摘要
------

**SWFVideoStream**

<span class="ooclass"> class **SWFVideoStream** </span> {

/\* 方法 \*/

<span class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$file`</span> \] )

<span class="type">int</span> <span
class="methodname">getNumFrames</span> ( <span
class="methodparam">void</span> )

<span class="type">void</span> <span
class="methodname">setDimension</span> ( <span class="methodparam"><span
class="type">int</span> `$x`</span> , <span class="methodparam"><span
class="type">int</span> `$y`</span> )

}

SWFVideoStream::\_\_construct
=============================

Returns a SWFVideoStream object

### 说明

<span class="methodname">SWFVideoStream::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$file`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

SWFVideoStream::getNumFrames
============================

Returns the number of frames in the video

### 说明

<span class="type">int</span> <span
class="methodname">SWFVideoStream::getNumFrames</span> ( <span
class="methodparam">void</span> )

This function returns the number of video-frames of a SWFVideoStream.

### 返回值

Returns the number of frames, as an integer

SWFVideoStream::setDimension
============================

Sets video dimension

### 说明

<span class="type">void</span> <span
class="methodname">SWFVideoStream::setDimension</span> ( <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$y`</span> )

Sets the width and height for streamed videos.

### 参数

`x`  
Width in pixels.

`y`  
Height in pixels.

### 返回值

没有返回值。
