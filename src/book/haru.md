Haru PDF
========

**目录**

-   [简介](/intro/haru.html)
-   [安装／配置](/haru/setup.html)
    -   [需求](/haru/setup.html#需求)
    -   [安装](/haru/setup.html#安装)
    -   [运行时配置](/haru/setup.html#运行时配置)
    -   [资源类型](/haru/setup.html#资源类型)
-   [预定义常量](/haru/constants.html)
-   [范例](/haru/examples.html)
    -   [Basic PECL/haru
        example](/haru/examples.html#Basic%20PECL/haru%20example)
-   [Builtin Fonts And Encodings](/haru/builtin.html)
    -   [Builtin Fonts](/haru/builtin.html#Builtin%20Fonts)
    -   [Builtin Encodings](/haru/builtin.html#Builtin%20Encodings)
-   [HaruException](/class/haruexception.html) — The HaruException class
-   [HaruDoc](/class/harudoc.html) — The HaruDoc class
    -   [HaruDoc::addPage](/class/harudoc.html#HaruDoc::addPage) — Add
        new page to the document
    -   [HaruDoc::addPageLabel](/class/harudoc.html#HaruDoc::addPageLabel)
        — Set the numbering style for the specified range of pages
    -   [HaruDoc::\_\_construct](/class/harudoc.html#HaruDoc::__construct)
        — Construct new HaruDoc instance
    -   [HaruDoc::createOutline](/class/harudoc.html#HaruDoc::createOutline)
        — Create a HaruOutline instance
    -   [HaruDoc::getCurrentEncoder](/class/harudoc.html#HaruDoc::getCurrentEncoder)
        — Get HaruEncoder currently used in the document
    -   [HaruDoc::getCurrentPage](/class/harudoc.html#HaruDoc::getCurrentPage)
        — Return current page of the document
    -   [HaruDoc::getEncoder](/class/harudoc.html#HaruDoc::getEncoder) —
        Get HaruEncoder instance for the specified encoding
    -   [HaruDoc::getFont](/class/harudoc.html#HaruDoc::getFont) — Get
        HaruFont instance
    -   [HaruDoc::getInfoAttr](/class/harudoc.html#HaruDoc::getInfoAttr)
        — Get current value of the specified document attribute
    -   [HaruDoc::getPageLayout](/class/harudoc.html#HaruDoc::getPageLayout)
        — Get current page layout
    -   [HaruDoc::getPageMode](/class/harudoc.html#HaruDoc::getPageMode)
        — Get current page mode
    -   [HaruDoc::getStreamSize](/class/harudoc.html#HaruDoc::getStreamSize)
        — Get the size of the temporary stream
    -   [HaruDoc::insertPage](/class/harudoc.html#HaruDoc::insertPage) —
        Insert new page just before the specified page
    -   [HaruDoc::loadJPEG](/class/harudoc.html#HaruDoc::loadJPEG) —
        Load a JPEG image
    -   [HaruDoc::loadPNG](/class/harudoc.html#HaruDoc::loadPNG) — Load
        PNG image and return HaruImage instance
    -   [HaruDoc::loadRaw](/class/harudoc.html#HaruDoc::loadRaw) — Load
        a RAW image
    -   [HaruDoc::loadTTC](/class/harudoc.html#HaruDoc::loadTTC) — Load
        the font with the specified index from TTC file
    -   [HaruDoc::loadTTF](/class/harudoc.html#HaruDoc::loadTTF) — Load
        TTF font file
    -   [HaruDoc::loadType1](/class/harudoc.html#HaruDoc::loadType1) —
        Load Type1 font
    -   [HaruDoc::output](/class/harudoc.html#HaruDoc::output) — Write
        the document data to the output buffer
    -   [HaruDoc::readFromStream](/class/harudoc.html#HaruDoc::readFromStream)
        — Read data from the temporary stream
    -   [HaruDoc::resetError](/class/harudoc.html#HaruDoc::resetError) —
        Reset error state of the document handle
    -   [HaruDoc::resetStream](/class/harudoc.html#HaruDoc::resetStream)
        — Rewind the temporary stream
    -   [HaruDoc::save](/class/harudoc.html#HaruDoc::save) — Save the
        document into the specified file
    -   [HaruDoc::saveToStream](/class/harudoc.html#HaruDoc::saveToStream)
        — Save the document into a temporary stream
    -   [HaruDoc::setCompressionMode](/class/harudoc.html#HaruDoc::setCompressionMode)
        — Set compression mode for the document
    -   [HaruDoc::setCurrentEncoder](/class/harudoc.html#HaruDoc::setCurrentEncoder)
        — Set the current encoder for the document
    -   [HaruDoc::setEncryptionMode](/class/harudoc.html#HaruDoc::setEncryptionMode)
        — Set encryption mode for the document
    -   [HaruDoc::setInfoAttr](/class/harudoc.html#HaruDoc::setInfoAttr)
        — Set the info attribute of the document
    -   [HaruDoc::setInfoDateAttr](/class/harudoc.html#HaruDoc::setInfoDateAttr)
        — Set the datetime info attributes of the document
    -   [HaruDoc::setOpenAction](/class/harudoc.html#HaruDoc::setOpenAction)
        — Define which page is shown when the document is opened
    -   [HaruDoc::setPageLayout](/class/harudoc.html#HaruDoc::setPageLayout)
        — Set how pages should be displayed
    -   [HaruDoc::setPageMode](/class/harudoc.html#HaruDoc::setPageMode)
        — Set how the document should be displayed
    -   [HaruDoc::setPagesConfiguration](/class/harudoc.html#HaruDoc::setPagesConfiguration)
        — Set the number of pages per set of pages
    -   [HaruDoc::setPassword](/class/harudoc.html#HaruDoc::setPassword)
        — Set owner and user passwords for the document
    -   [HaruDoc::setPermission](/class/harudoc.html#HaruDoc::setPermission)
        — Set permissions for the document
    -   [HaruDoc::useCNSEncodings](/class/harudoc.html#HaruDoc::useCNSEncodings)
        — Enable Chinese simplified encodings
    -   [HaruDoc::useCNSFonts](/class/harudoc.html#HaruDoc::useCNSFonts)
        — Enable builtin Chinese simplified fonts
    -   [HaruDoc::useCNTEncodings](/class/harudoc.html#HaruDoc::useCNTEncodings)
        — Enable Chinese traditional encodings
    -   [HaruDoc::useCNTFonts](/class/harudoc.html#HaruDoc::useCNTFonts)
        — Enable builtin Chinese traditional fonts
    -   [HaruDoc::useJPEncodings](/class/harudoc.html#HaruDoc::useJPEncodings)
        — Enable Japanese encodings
    -   [HaruDoc::useJPFonts](/class/harudoc.html#HaruDoc::useJPFonts) —
        Enable builtin Japanese fonts
    -   [HaruDoc::useKREncodings](/class/harudoc.html#HaruDoc::useKREncodings)
        — Enable Korean encodings
    -   [HaruDoc::useKRFonts](/class/harudoc.html#HaruDoc::useKRFonts) —
        Enable builtin Korean fonts
-   [HaruPage](/class/harupage.html) — The HaruPage class
    -   [HaruPage::arc](/class/harupage.html#HaruPage::arc) — Append an
        arc to the current path
    -   [HaruPage::beginText](/class/harupage.html#HaruPage::beginText)
        — Begin a text object and set the current text position to (0,0)
    -   [HaruPage::circle](/class/harupage.html#HaruPage::circle) —
        Append a circle to the current path
    -   [HaruPage::closePath](/class/harupage.html#HaruPage::closePath)
        — Append a straight line from the current point to the start
        point of the path
    -   [HaruPage::concat](/class/harupage.html#HaruPage::concat) —
        Concatenate current transformation matrix of the page and the
        specified matrix
    -   [HaruPage::createDestination](/class/harupage.html#HaruPage::createDestination)
        — Create new HaruDestination instance
    -   [HaruPage::createLinkAnnotation](/class/harupage.html#HaruPage::createLinkAnnotation)
        — Create new HaruAnnotation instance
    -   [HaruPage::createTextAnnotation](/class/harupage.html#HaruPage::createTextAnnotation)
        — Create new HaruAnnotation instance
    -   [HaruPage::createURLAnnotation](/class/harupage.html#HaruPage::createURLAnnotation)
        — Create and return new HaruAnnotation instance
    -   [HaruPage::curveTo2](/class/harupage.html#HaruPage::curveTo2) —
        Append a Bezier curve to the current path
    -   [HaruPage::curveTo3](/class/harupage.html#HaruPage::curveTo3) —
        Append a Bezier curve to the current path
    -   [HaruPage::curveTo](/class/harupage.html#HaruPage::curveTo) —
        Append a Bezier curve to the current path
    -   [HaruPage::drawImage](/class/harupage.html#HaruPage::drawImage)
        — Show image at the page
    -   [HaruPage::ellipse](/class/harupage.html#HaruPage::ellipse) —
        Append an ellipse to the current path
    -   [HaruPage::endPath](/class/harupage.html#HaruPage::endPath) —
        End current path object without filling and painting operations
    -   [HaruPage::endText](/class/harupage.html#HaruPage::endText) —
        End current text object
    -   [HaruPage::eofill](/class/harupage.html#HaruPage::eofill) — Fill
        current path using even-odd rule
    -   [HaruPage::eoFillStroke](/class/harupage.html#HaruPage::eoFillStroke)
        — Fill current path using even-odd rule, then paint the path
    -   [HaruPage::fill](/class/harupage.html#HaruPage::fill) — Fill
        current path using nonzero winding number rule
    -   [HaruPage::fillStroke](/class/harupage.html#HaruPage::fillStroke)
        — Fill current path using nonzero winding number rule, then
        paint the path
    -   [HaruPage::getCharSpace](/class/harupage.html#HaruPage::getCharSpace)
        — Get the current value of character spacing
    -   [HaruPage::getCMYKFill](/class/harupage.html#HaruPage::getCMYKFill)
        — Get the current filling color
    -   [HaruPage::getCMYKStroke](/class/harupage.html#HaruPage::getCMYKStroke)
        — Get the current stroking color
    -   [HaruPage::getCurrentFont](/class/harupage.html#HaruPage::getCurrentFont)
        — Get the currently used font
    -   [HaruPage::getCurrentFontSize](/class/harupage.html#HaruPage::getCurrentFontSize)
        — Get the current font size
    -   [HaruPage::getCurrentPos](/class/harupage.html#HaruPage::getCurrentPos)
        — Get the current position for path painting
    -   [HaruPage::getCurrentTextPos](/class/harupage.html#HaruPage::getCurrentTextPos)
        — Get the current position for text printing
    -   [HaruPage::getDash](/class/harupage.html#HaruPage::getDash) —
        Get the current dash pattern
    -   [HaruPage::getFillingColorSpace](/class/harupage.html#HaruPage::getFillingColorSpace)
        — Get the current filling color space
    -   [HaruPage::getFlatness](/class/harupage.html#HaruPage::getFlatness)
        — Get the flatness of the page
    -   [HaruPage::getGMode](/class/harupage.html#HaruPage::getGMode) —
        Get the current graphics mode
    -   [HaruPage::getGrayFill](/class/harupage.html#HaruPage::getGrayFill)
        — Get the current filling color
    -   [HaruPage::getGrayStroke](/class/harupage.html#HaruPage::getGrayStroke)
        — Get the current stroking color
    -   [HaruPage::getHeight](/class/harupage.html#HaruPage::getHeight)
        — Get the height of the page
    -   [HaruPage::getHorizontalScaling](/class/harupage.html#HaruPage::getHorizontalScaling)
        — Get the current value of horizontal scaling
    -   [HaruPage::getLineCap](/class/harupage.html#HaruPage::getLineCap)
        — Get the current line cap style
    -   [HaruPage::getLineJoin](/class/harupage.html#HaruPage::getLineJoin)
        — Get the current line join style
    -   [HaruPage::getLineWidth](/class/harupage.html#HaruPage::getLineWidth)
        — Get the current line width
    -   [HaruPage::getMiterLimit](/class/harupage.html#HaruPage::getMiterLimit)
        — Get the value of miter limit
    -   [HaruPage::getRGBFill](/class/harupage.html#HaruPage::getRGBFill)
        — Get the current filling color
    -   [HaruPage::getRGBStroke](/class/harupage.html#HaruPage::getRGBStroke)
        — Get the current stroking color
    -   [HaruPage::getStrokingColorSpace](/class/harupage.html#HaruPage::getStrokingColorSpace)
        — Get the current stroking color space
    -   [HaruPage::getTextLeading](/class/harupage.html#HaruPage::getTextLeading)
        — Get the current value of line spacing
    -   [HaruPage::getTextMatrix](/class/harupage.html#HaruPage::getTextMatrix)
        — Get the current text transformation matrix of the page
    -   [HaruPage::getTextRenderingMode](/class/harupage.html#HaruPage::getTextRenderingMode)
        — Get the current text rendering mode
    -   [HaruPage::getTextRise](/class/harupage.html#HaruPage::getTextRise)
        — Get the current value of text rising
    -   [HaruPage::getTextWidth](/class/harupage.html#HaruPage::getTextWidth)
        — Get the width of the text using current fontsize, character
        spacing and word spacing
    -   [HaruPage::getTransMatrix](/class/harupage.html#HaruPage::getTransMatrix)
        — Get the current transformation matrix of the page
    -   [HaruPage::getWidth](/class/harupage.html#HaruPage::getWidth) —
        Get the width of the page
    -   [HaruPage::getWordSpace](/class/harupage.html#HaruPage::getWordSpace)
        — Get the current value of word spacing
    -   [HaruPage::lineTo](/class/harupage.html#HaruPage::lineTo) — Draw
        a line from the current point to the specified point
    -   [HaruPage::measureText](/class/harupage.html#HaruPage::measureText)
        — Calculate the byte length of characters which can be included
        on one line of the specified width
    -   [HaruPage::moveTextPos](/class/harupage.html#HaruPage::moveTextPos)
        — Move text position to the specified offset
    -   [HaruPage::moveTo](/class/harupage.html#HaruPage::moveTo) — Set
        starting point for new drawing path
    -   [HaruPage::moveToNextLine](/class/harupage.html#HaruPage::moveToNextLine)
        — Move text position to the start of the next line
    -   [HaruPage::rectangle](/class/harupage.html#HaruPage::rectangle)
        — Append a rectangle to the current path
    -   [HaruPage::setCharSpace](/class/harupage.html#HaruPage::setCharSpace)
        — Set character spacing for the page
    -   [HaruPage::setCMYKFill](/class/harupage.html#HaruPage::setCMYKFill)
        — Set filling color for the page
    -   [HaruPage::setCMYKStroke](/class/harupage.html#HaruPage::setCMYKStroke)
        — Set stroking color for the page
    -   [HaruPage::setDash](/class/harupage.html#HaruPage::setDash) —
        Set the dash pattern for the page
    -   [HaruPage::setFlatness](/class/harupage.html#HaruPage::setFlatness)
        — Set flatness for the page
    -   [HaruPage::setFontAndSize](/class/harupage.html#HaruPage::setFontAndSize)
        — Set font and fontsize for the page
    -   [HaruPage::setGrayFill](/class/harupage.html#HaruPage::setGrayFill)
        — Set filling color for the page
    -   [HaruPage::setGrayStroke](/class/harupage.html#HaruPage::setGrayStroke)
        — Sets stroking color for the page
    -   [HaruPage::setHeight](/class/harupage.html#HaruPage::setHeight)
        — Set height of the page
    -   [HaruPage::setHorizontalScaling](/class/harupage.html#HaruPage::setHorizontalScaling)
        — Set horizontal scaling for the page
    -   [HaruPage::setLineCap](/class/harupage.html#HaruPage::setLineCap)
        — Set the shape to be used at the ends of lines
    -   [HaruPage::setLineJoin](/class/harupage.html#HaruPage::setLineJoin)
        — Set line join style for the page
    -   [HaruPage::setLineWidth](/class/harupage.html#HaruPage::setLineWidth)
        — Set line width for the page
    -   [HaruPage::setMiterLimit](/class/harupage.html#HaruPage::setMiterLimit)
        — Set the current value of the miter limit of the page
    -   [HaruPage::setRGBFill](/class/harupage.html#HaruPage::setRGBFill)
        — Set filling color for the page
    -   [HaruPage::setRGBStroke](/class/harupage.html#HaruPage::setRGBStroke)
        — Set stroking color for the page
    -   [HaruPage::setRotate](/class/harupage.html#HaruPage::setRotate)
        — Set rotation angle of the page
    -   [HaruPage::setSize](/class/harupage.html#HaruPage::setSize) —
        Set size and direction of the page
    -   [HaruPage::setSlideShow](/class/harupage.html#HaruPage::setSlideShow)
        — Set transition style for the page
    -   [HaruPage::setTextLeading](/class/harupage.html#HaruPage::setTextLeading)
        — Set text leading (line spacing) for the page
    -   [HaruPage::setTextMatrix](/class/harupage.html#HaruPage::setTextMatrix)
        — Set the current text transformation matrix of the page
    -   [HaruPage::setTextRenderingMode](/class/harupage.html#HaruPage::setTextRenderingMode)
        — Set text rendering mode for the page
    -   [HaruPage::setTextRise](/class/harupage.html#HaruPage::setTextRise)
        — Set the current value of text rising
    -   [HaruPage::setWidth](/class/harupage.html#HaruPage::setWidth) —
        Set width of the page
    -   [HaruPage::setWordSpace](/class/harupage.html#HaruPage::setWordSpace)
        — Set word spacing for the page
    -   [HaruPage::showText](/class/harupage.html#HaruPage::showText) —
        Print text at the current position of the page
    -   [HaruPage::showTextNextLine](/class/harupage.html#HaruPage::showTextNextLine)
        — Move the current position to the start of the next line and
        print the text
    -   [HaruPage::stroke](/class/harupage.html#HaruPage::stroke) —
        Paint current path
    -   [HaruPage::textOut](/class/harupage.html#HaruPage::textOut) —
        Print the text on the specified position
    -   [HaruPage::textRect](/class/harupage.html#HaruPage::textRect) —
        Print the text inside the specified region
-   [HaruFont](/class/harufont.html) — The HaruFont class
    -   [HaruFont::getAscent](/class/harufont.html#HaruFont::getAscent)
        — Get the vertical ascent of the font
    -   [HaruFont::getCapHeight](/class/harufont.html#HaruFont::getCapHeight)
        — Get the distance from the baseline of uppercase letters
    -   [HaruFont::getDescent](/class/harufont.html#HaruFont::getDescent)
        — Get the vertical descent of the font
    -   [HaruFont::getEncodingName](/class/harufont.html#HaruFont::getEncodingName)
        — Get the name of the encoding
    -   [HaruFont::getFontName](/class/harufont.html#HaruFont::getFontName)
        — Get the name of the font
    -   [HaruFont::getTextWidth](/class/harufont.html#HaruFont::getTextWidth)
        — Get the total width of the text, number of characters, number
        of words and number of spaces
    -   [HaruFont::getUnicodeWidth](/class/harufont.html#HaruFont::getUnicodeWidth)
        — Get the width of the character in the font
    -   [HaruFont::getXHeight](/class/harufont.html#HaruFont::getXHeight)
        — Get the distance from the baseline of lowercase letters
    -   [HaruFont::measureText](/class/harufont.html#HaruFont::measureText)
        — Calculate the number of characters which can be included
        within the specified width
-   [HaruImage](/class/haruimage.html) — The HaruImage class
    -   [HaruImage::getBitsPerComponent](/class/haruimage.html#HaruImage::getBitsPerComponent)
        — Get the number of bits used to describe each color component
        of the image
    -   [HaruImage::getColorSpace](/class/haruimage.html#HaruImage::getColorSpace)
        — Get the name of the color space
    -   [HaruImage::getHeight](/class/haruimage.html#HaruImage::getHeight)
        — Get the height of the image
    -   [HaruImage::getSize](/class/haruimage.html#HaruImage::getSize) —
        Get size of the image
    -   [HaruImage::getWidth](/class/haruimage.html#HaruImage::getWidth)
        — Get the width of the image
    -   [HaruImage::setColorMask](/class/haruimage.html#HaruImage::setColorMask)
        — Set the color mask of the image
    -   [HaruImage::setMaskImage](/class/haruimage.html#HaruImage::setMaskImage)
        — Set the image mask
-   [HaruEncoder](/class/haruencoder.html) — The HaruEncoder class
    -   [HaruEncoder::getByteType](/class/haruencoder.html#HaruEncoder::getByteType)
        — Get the type of the byte in the text
    -   [HaruEncoder::getType](/class/haruencoder.html#HaruEncoder::getType)
        — Get the type of the encoder
    -   [HaruEncoder::getUnicode](/class/haruencoder.html#HaruEncoder::getUnicode)
        — Convert the specified character to unicode
    -   [HaruEncoder::getWritingMode](/class/haruencoder.html#HaruEncoder::getWritingMode)
        — Get the writing mode of the encoder
-   [HaruOutline](/class/haruoutline.html) — The HaruOutline class
    -   [HaruOutline::setDestination](/class/haruoutline.html#HaruOutline::setDestination)
        — Set the destination for the outline
    -   [HaruOutline::setOpened](/class/haruoutline.html#HaruOutline::setOpened)
        — Set the initial state of the outline
-   [HaruAnnotation](/class/haruannotation.html) — The HaruAnnotation
    class
    -   [HaruAnnotation::setBorderStyle](/class/haruannotation.html#HaruAnnotation::setBorderStyle)
        — Set the border style of the annotation
    -   [HaruAnnotation::setHighlightMode](/class/haruannotation.html#HaruAnnotation::setHighlightMode)
        — Set the highlighting mode of the annotation
    -   [HaruAnnotation::setIcon](/class/haruannotation.html#HaruAnnotation::setIcon)
        — Set the icon style of the annotation
    -   [HaruAnnotation::setOpened](/class/haruannotation.html#HaruAnnotation::setOpened)
        — Set the initial state of the annotation
-   [HaruDestination](/class/harudestination.html) — The HaruDestination
    class
    -   [HaruDestination::setFit](/class/harudestination.html#HaruDestination::setFit)
        — Set the appearance of the page to fit the window
    -   [HaruDestination::setFitB](/class/harudestination.html#HaruDestination::setFitB)
        — Set the appearance of the page to fit the bounding box of the
        page within the window
    -   [HaruDestination::setFitBH](/class/harudestination.html#HaruDestination::setFitBH)
        — Set the appearance of the page to fit the width of the
        bounding box
    -   [HaruDestination::setFitBV](/class/harudestination.html#HaruDestination::setFitBV)
        — Set the appearance of the page to fit the height of the
        boudning box
    -   [HaruDestination::setFitH](/class/harudestination.html#HaruDestination::setFitH)
        — Set the appearance of the page to fit the window width
    -   [HaruDestination::setFitR](/class/harudestination.html#HaruDestination::setFitR)
        — Set the appearance of the page to fit the specified rectangle
    -   [HaruDestination::setFitV](/class/harudestination.html#HaruDestination::setFitV)
        — Set the appearance of the page to fit the window height
    -   [HaruDestination::setXYZ](/class/harudestination.html#HaruDestination::setXYZ)
        — Set the appearance of the page

简介
----

Haru PDF Exception Class.

类摘要
------

**HaruException**

<span class="ooclass"> class **HaruException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* Inherits \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

Haru PDF Document Class.

类摘要
------

**HaruDoc**

<span class="ooclass"> class **HaruDoc** </span> {

/\* 方法 \*/

<span class="type">object</span> <span class="methodname">addPage</span>
( <span class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">addPageLabel</span> ( <span class="methodparam"><span
class="type">int</span> `$first_page`</span> , <span
class="methodparam"><span class="type">int</span> `$style`</span> ,
<span class="methodparam"><span class="type">int</span>
`$first_num`</span> \[, <span class="methodparam"><span
class="type">string</span> `$prefix`<span class="initializer"> =
""</span></span> \] )

<span class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="type">object</span> <span
class="methodname">createOutline</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> \[,
<span class="methodparam"><span class="type">object</span>
`$parent_outline`</span> \[, <span class="methodparam"><span
class="type">object</span> `$encoder`</span> \]\] )

<span class="type">object</span> <span
class="methodname">getCurrentEncoder</span> ( <span
class="methodparam">void</span> )

<span class="type">object</span> <span
class="methodname">getCurrentPage</span> ( <span
class="methodparam">void</span> )

<span class="type">object</span> <span
class="methodname">getEncoder</span> ( <span class="methodparam"><span
class="type">string</span> `$encoding`</span> )

<span class="type">object</span> <span class="methodname">getFont</span>
( <span class="methodparam"><span class="type">string</span>
`$fontname`</span> \[, <span class="methodparam"><span
class="type">string</span> `$encoding`</span> \] )

<span class="type">string</span> <span
class="methodname">getInfoAttr</span> ( <span class="methodparam"><span
class="type">int</span> `$type`</span> )

<span class="type">int</span> <span
class="methodname">getPageLayout</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getPageMode</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getStreamSize</span> ( <span
class="methodparam">void</span> )

<span class="type">object</span> <span
class="methodname">insertPage</span> ( <span class="methodparam"><span
class="type">object</span> `$page`</span> )

<span class="type">object</span> <span
class="methodname">loadJPEG</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

<span class="type">object</span> <span class="methodname">loadPNG</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$deferred`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="type">object</span> <span class="methodname">loadRaw</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">int</span> `$width`</span> , <span
class="methodparam"><span class="type">int</span> `$height`</span> ,
<span class="methodparam"><span class="type">int</span>
`$color_space`</span> )

<span class="type">string</span> <span class="methodname">loadTTC</span>
( <span class="methodparam"><span class="type">string</span>
`$fontfile`</span> , <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$embed`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="type">string</span> <span class="methodname">loadTTF</span>
( <span class="methodparam"><span class="type">string</span>
`$fontfile`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$embed`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="type">string</span> <span
class="methodname">loadType1</span> ( <span class="methodparam"><span
class="type">string</span> `$afmfile`</span> \[, <span
class="methodparam"><span class="type">string</span> `$pfmfile`</span>
\] )

<span class="type">bool</span> <span class="methodname">output</span> (
<span class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">readFromStream</span> ( <span
class="methodparam"><span class="type">int</span> `$bytes`</span> )

<span class="type">bool</span> <span
class="methodname">resetError</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">resetStream</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">save</span> (
<span class="methodparam"><span class="type">string</span>
`$file`</span> )

<span class="type">bool</span> <span
class="methodname">saveToStream</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">setCompressionMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="type">bool</span> <span
class="methodname">setCurrentEncoder</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

<span class="type">bool</span> <span
class="methodname">setEncryptionMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">int</span> `$key_len`<span
class="initializer"> = 5</span></span> \] )

<span class="type">bool</span> <span
class="methodname">setInfoAttr</span> ( <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">string</span> `$info`</span> )

<span class="type">bool</span> <span
class="methodname">setInfoDateAttr</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> ,
<span class="methodparam"><span class="type">int</span> `$hour`</span> ,
<span class="methodparam"><span class="type">int</span> `$min`</span> ,
<span class="methodparam"><span class="type">int</span> `$sec`</span> ,
<span class="methodparam"><span class="type">string</span> `$ind`</span>
, <span class="methodparam"><span class="type">int</span>
`$off_hour`</span> , <span class="methodparam"><span
class="type">int</span> `$off_min`</span> )

<span class="type">bool</span> <span
class="methodname">setOpenAction</span> ( <span
class="methodparam"><span class="type">object</span>
`$destination`</span> )

<span class="type">bool</span> <span
class="methodname">setPageLayout</span> ( <span
class="methodparam"><span class="type">int</span> `$layout`</span> )

<span class="type">bool</span> <span
class="methodname">setPageMode</span> ( <span class="methodparam"><span
class="type">int</span> `$mode`</span> )

<span class="type">bool</span> <span
class="methodname">setPagesConfiguration</span> ( <span
class="methodparam"><span class="type">int</span>
`$page_per_pages`</span> )

<span class="type">bool</span> <span
class="methodname">setPassword</span> ( <span class="methodparam"><span
class="type">string</span> `$owner_password`</span> , <span
class="methodparam"><span class="type">string</span>
`$user_password`</span> )

<span class="type">bool</span> <span
class="methodname">setPermission</span> ( <span
class="methodparam"><span class="type">int</span> `$permission`</span> )

<span class="type">bool</span> <span
class="methodname">useCNSEncodings</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useCNSFonts</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useCNTEncodings</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useCNTFonts</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useJPEncodings</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useJPFonts</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useKREncodings</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">useKRFonts</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

| Type | Name                                      | Description |
|------|-------------------------------------------|-------------|
| int  | HaruDoc::CS\_DEVICE\_GRAY                 |             |
| int  | HaruDoc::CS\_DEVICE\_RGB                  |             |
| int  | HaruDoc::CS\_DEVICE\_CMYK                 |             |
| int  | HaruDoc::CS\_CAL\_GRAY                    |             |
| int  | HaruDoc::CS\_CAL\_RGB                     |             |
| int  | HaruDoc::CS\_LAB                          |             |
| int  | HaruDoc::CS\_ICC\_BASED                   |             |
| int  | HaruDoc::CS\_SEPARATION                   |             |
| int  | HaruDoc::CS\_DEVICE\_N                    |             |
| int  | HaruDoc::CS\_INDEXED                      |             |
| int  | HaruDoc::CS\_PATTERN                      |             |
| int  | HaruDoc::ENABLE\_READ                     |             |
| int  | HaruDoc::ENABLE\_PRINT                    |             |
| int  | HaruDoc::ENABLE\_EDIT\_ALL                |             |
| int  | HaruDoc::ENABLE\_COPY                     |             |
| int  | HaruDoc::ENABLE\_EDIT                     |             |
| int  | HaruDoc::ENCRYPT\_R2                      |             |
| int  | HaruDoc::ENCRYPT\_R3                      |             |
| int  | HaruDoc::INFO\_AUTHOR                     |             |
| int  | HaruDoc::INFO\_CREATOR                    |             |
| int  | HaruDoc::INFO\_TITLE                      |             |
| int  | HaruDoc::INFO\_SUBJECT                    |             |
| int  | HaruDoc::INFO\_KEYWORDS                   |             |
| int  | HaruDoc::INFO\_CREATION\_DATE             |             |
| int  | HaruDoc::INFO\_MOD\_DATE                  |             |
| int  | HaruDoc::COMP\_NONE                       |             |
| int  | HaruDoc::COMP\_TEXT                       |             |
| int  | HaruDoc::COMP\_IMAGE                      |             |
| int  | HaruDoc::COMP\_METADATA                   |             |
| int  | HaruDoc::COMP\_ALL                        |             |
| int  | HaruDoc::PAGE\_LAYOUT\_SINGLE             |             |
| int  | HaruDoc::PAGE\_LAYOUT\_ONE\_COLUMN        |             |
| int  | HaruDoc::PAGE\_LAYOUT\_TWO\_COLUMN\_LEFT  |             |
| int  | HaruDoc::PAGE\_LAYOUT\_TWO\_COLUMN\_RIGHT |             |
| int  | HaruDoc::PAGE\_MODE\_USE\_NONE            |             |
| int  | HaruDoc::PAGE\_MODE\_USE\_OUTLINE         |             |
| int  | HaruDoc::PAGE\_MODE\_USE\_THUMBS          |             |
| int  | HaruDoc::PAGE\_MODE\_FULL\_SCREEN         |             |

HaruDoc::addPage
================

Add new page to the document

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::addPage</span> ( <span
class="methodparam">void</span> )

Adds a new page to the document.

### 参数

此函数没有参数。

### 返回值

Returns a new <span class="classname">HaruPage</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::insertPage</span>

HaruDoc::addPageLabel
=====================

Set the numbering style for the specified range of pages

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::addPageLabel</span> ( <span
class="methodparam"><span class="type">int</span> `$first_page`</span> ,
<span class="methodparam"><span class="type">int</span> `$style`</span>
, <span class="methodparam"><span class="type">int</span>
`$first_num`</span> \[, <span class="methodparam"><span
class="type">string</span> `$prefix`<span class="initializer"> =
""</span></span> \] )

Set the numbering style for the specified range of pages.

### 参数

`first_page`  
The first page included into the labeling range.

`style`  
The numbering style. The following values are allowed:

-   **`HaruPage::NUM_STYLE_DECIMAL`** - page label is displayed using
    decimal numerals.
-   **`HaruPage::NUM_STYLE_UPPER_ROMAN`** - page label is displayed
    using uppercase Roman numerals.
-   **`HaruPage::NUM_STYLE_LOWER_ROMAN`** - page label is displayed
    using lowercase Roman numerals.
-   **`HaruPage::NUM_STYLE_UPPER_LETTER`** - page label is displayed
    using uppercase letters (from A to Z).
-   **`HaruPage::NUM_STYLE_LOWER_LETTERS`** - page label is displayed
    using lowercase letters (from a to z).

`first_num`  
The first page number in this range.

`prefix`  
The prefix for the page label.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::\_\_construct
======================

Construct new <span class="classname">HaruDoc</span> instance

### 说明

<span class="methodname">HaruDoc::\_\_construct</span> ( <span
class="methodparam">void</span> )

Constructs new HaruDoc instance.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::createOutline
======================

Create a <span class="classname">HaruOutline</span> instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::createOutline</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> \[,
<span class="methodparam"><span class="type">object</span>
`$parent_outline`</span> \[, <span class="methodparam"><span
class="type">object</span> `$encoder`</span> \]\] )

Create a <span class="classname">HaruOutline</span> instance.

### 参数

`title`  
The caption of new outline object.

`parent_outline`  
A valid <span class="classname">HaruOutline</span> instance or
**`NULL`**.

`encoder`  
A valid <span class="classname">HaruEncoder</span> instance or
**`NULL`**.

### 返回值

Returns a new <span class="classname">HaruOutline</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::getCurrentEncoder
==========================

Get <span class="classname">HaruEncoder</span> currently used in the
document

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::getCurrentEncoder</span> ( <span
class="methodparam">void</span> )

Get the <span class="classname">HaruEncoder</span> currently used in the
document.

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">HaruEncoder</span> currently used in the
document or **`FALSE`** if encoder is not set.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setCurrentEncoder</span>

HaruDoc::getCurrentPage
=======================

Return current page of the document

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::getCurrentPage</span> ( <span
class="methodparam">void</span> )

Get current page of the document.

### 参数

此函数没有参数。

### 返回值

Returns <span class="classname">HaruPage</span> instance on success or
**`FALSE`** if there is no current page at the moment.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::getEncoder
===================

Get <span class="classname">HaruEncoder</span> instance for the
specified encoding

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::getEncoder</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

Get the <span class="classname">HaruEncoder</span> instance for the
specified encoding.

### 参数

`encoding`  
The encoding name. See
<a href="/haru/builtin.html#Builtin%20Encodings" class="link">Builtin Encodings</a>
for the list of allowed values.

### 返回值

Returns a <span class="classname">HaruEncoder</span> instance for the
specified encoding.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setCurrentEncoder</span>
-   <span class="methodname">HaruDoc::getCurrentEncoder</span>

HaruDoc::getFont
================

Get <span class="classname">HaruFont</span> instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::getFont</span> ( <span
class="methodparam"><span class="type">string</span> `$fontname`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$encoding`</span> \] )

Get a <span class="classname">HaruFont</span> instance.

### 参数

`fontname`  
The name of the font. See
<a href="/haru/builtin.html#Builtin%20Fonts" class="link">Builtin Fonts</a>
for the list of builtin fonts. You can also use the name of a font
loaded via <span class="methodname">HaruDoc::loadTTF</span>, <span
class="methodname">HaruDoc::loadTTC</span> and <span
class="methodname">HaruDoc::loadType1</span>.

`encoding`  
The encoding to use. See
<a href="/haru/builtin.html#Builtin%20Encodings" class="link">Builtin Encodings</a>
for the list of supported encodings.

### 返回值

Returns a <span class="classname">HaruFont</span> instance with the
specified `fontname` and `encoding`.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setFontAndSize</span>
-   <span class="methodname">HaruPage::setCurrentFont</span>

HaruDoc::getInfoAttr
====================

Get current value of the specified document attribute

### 说明

<span class="type">string</span> <span
class="methodname">HaruDoc::getInfoAttr</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> )

Get the current value of the specified document attribute.

### 参数

`type`  
The type of the attribute. The following values are available:

-   **`HaruDoc::INFO_AUTHOR`**
-   **`HaruDoc::INFO_CREATOR`**
-   **`HaruDoc::INFO_TITLE`**
-   **`HaruDoc::INFO_SUBJECT`**
-   **`HaruDoc::INFO_KEYWORDS`**
-   **`HaruDoc::INFO_CREATION_DATE`**
-   **`HaruDoc::INFO_MOD_DATE`**

### 返回值

Returns the <span class="type">string</span> value of the specified
document attribute.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setInfoAttr</span>
-   <span class="methodname">HaruDoc::setInfoDateAttr</span>

HaruDoc::getPageLayout
======================

Get current page layout

### 说明

<span class="type">int</span> <span
class="methodname">HaruDoc::getPageLayout</span> ( <span
class="methodparam">void</span> )

Get the current page layout. See <span
class="methodname">HaruDoc::setPageLayout</span> for the list of
possible values.

### 参数

此函数没有参数。

### 返回值

Returns the page layout currently set in the document or **`FALSE`** if
page layout was not set. See <span
class="methodname">HaruDoc::setPageLayout</span> for the list of
possible values.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setPageLayout</span>

HaruDoc::getPageMode
====================

Get current page mode

### 说明

<span class="type">int</span> <span
class="methodname">HaruDoc::getPageMode</span> ( <span
class="methodparam">void</span> )

Get the current page mode. See <span
class="methodname">HaruDoc::setPageMode</span> for the list of possible
values.

### 参数

此函数没有参数。

### 返回值

Returns the page mode currently set in the document. See <span
class="methodname">HaruDoc::setPageMode</span> for the list of possible
values.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setPageMode</span>

HaruDoc::getStreamSize
======================

Get the size of the temporary stream

### 说明

<span class="type">int</span> <span
class="methodname">HaruDoc::getStreamSize</span> ( <span
class="methodparam">void</span> )

Get the size of the temporary stream.

### 参数

此函数没有参数。

### 返回值

Returns the size of the data in the temporary stream of the document.
The size is zero if the document was not saved to the temporary stream.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::saveToStream</span>
-   <span class="methodname">HaruDoc::resetStream</span>
-   <span class="methodname">HaruDoc::readFromStream</span>

HaruDoc::insertPage
===================

Insert new page just before the specified page

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::insertPage</span> ( <span
class="methodparam"><span class="type">object</span> `$page`</span> )

Creates a new page and inserts just before the specified page.

### 参数

`page`  
A valid <span class="classname">HaruPage</span> instance.

### 返回值

Returns a new <span class="classname">HaruPage</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::addPage</span>

HaruDoc::loadJPEG
=================

Load a JPEG image

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::loadJPEG</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Loads the specified JPEG image.

### 参数

`filename`  
A valid JPEG image file.

### 返回值

Returns a new <span class="classname">HaruImage</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::loadPNG</span>
-   <span class="methodname">HaruDoc::loadRAW</span>

HaruDoc::loadPNG
================

Load PNG image and return <span class="classname">HaruImage</span>
instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::loadPNG</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$deferred`<span class="initializer"> = **`FALSE`**</span></span> \] )

Loads a PNG image.

Libharu might be built without libpng support, in this case each call to
this function would result in exception.

### 参数

`filename`  
The name of a PNG image file.

`deferred`  
Do not load data immediately. You can set `deferred` parameter to
**`TRUE`** for deferred data loading, in this case only size and color
are loaded immediately.

### 返回值

Returns a <span class="classname">HaruImage</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::loadJPEG</span>
-   <span class="methodname">HaruDoc::loadRAW</span>

HaruDoc::loadRaw
================

Load a RAW image

### 说明

<span class="type">object</span> <span
class="methodname">HaruDoc::loadRaw</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> , <span class="methodparam"><span
class="type">int</span> `$height`</span> , <span
class="methodparam"><span class="type">int</span> `$color_space`</span>
)

Loads a RAW image.

### 参数

`filename`  
The name of a RAW image file.

`width`  
The width of the image.

`height`  
The height of the image.

`color_space`  
The color space of the image. Can be one of the following values:

-   **`HaruDoc::CS_DEVICE_GRAY`**
-   **`HaruDoc::CS_DEVICE_RGB`**
-   **`HaruDoc::CS_DEVICE_CMYK`**

### 返回值

Returns a <span class="classname">HaruImage</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::loadJPEG</span>
-   <span class="methodname">HaruDoc::loadPNG</span>

HaruDoc::loadTTC
================

Load the font with the specified index from TTC file

### 说明

<span class="type">string</span> <span
class="methodname">HaruDoc::loadTTC</span> ( <span
class="methodparam"><span class="type">string</span> `$fontfile`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$embed`<span class="initializer"> =
**`FALSE`**</span></span> \] )

Loads the TrueType font with the specified index from a TrueType
collection file.

### 参数

`fontfile`  
The TrueType collection file.

`index`  
The index of the font in the collection file.

`embed`  
When set to **`TRUE`**, the glyph data of the font is embedded into the
PDF file, otherwise only the matrix data is included.

### 返回值

Returns the name of the loaded font on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::loadTTF</span>
-   <span class="methodname">HaruDoc::loadType1</span>

HaruDoc::loadTTF
================

Load TTF font file

### 说明

<span class="type">string</span> <span
class="methodname">HaruDoc::loadTTF</span> ( <span
class="methodparam"><span class="type">string</span> `$fontfile`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$embed`<span class="initializer"> = **`FALSE`**</span></span> \] )

Loads the given TTF file and (optionally) embed its data into the
document.

### 参数

`fontfile`  
The TTF file to load.

`embed`  
When set to **`TRUE`**, the glyph data of the font is embedded into the
PDF file, otherwise only the matrix data is included.

### 返回值

Returns the name of the loaded font on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::loadTTC</span>
-   <span class="methodname">HaruDoc::loadType1</span>

HaruDoc::loadType1
==================

Load Type1 font

### 说明

<span class="type">string</span> <span
class="methodname">HaruDoc::loadType1</span> ( <span
class="methodparam"><span class="type">string</span> `$afmfile`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$pfmfile`</span> \] )

Loads Type1 font from the given file and registers it in the PDF
document.

### 参数

`afmfile`  
Path to an AFM file.

`pfmfile`  
Path to a PFA/PFB file, optional. If it's not set only the glyph data of
the font is embedded into the PDF document.

### 返回值

Returns the name of the loaded font on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::loadTTC</span>
-   <span class="methodname">HaruDoc::loadTTF</span>

HaruDoc::output
===============

Write the document data to the output buffer

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::output</span> ( <span
class="methodparam">void</span> )

Writes the document data into standard output.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::save</span>

HaruDoc::readFromStream
=======================

Read data from the temporary stream

### 说明

<span class="type">string</span> <span
class="methodname">HaruDoc::readFromStream</span> ( <span
class="methodparam"><span class="type">int</span> `$bytes`</span> )

Read data from the temporary stream.

### 参数

`bytes`  
The `bytes` parameter specifies how many bytes to read, though the
stream may contain less bytes than requested.

### 返回值

Returns data from the temporary stream.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::saveToStream</span>
-   <span class="methodname">HaruDoc::resetStream</span>
-   <span class="methodname">HaruDoc::getStreamSize</span>

HaruDoc::resetError
===================

Reset error state of the document handle

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::resetError</span> ( <span
class="methodparam">void</span> )

Once an error code is set, most of the operations, including I/O
processing functions cannot be performed. In case if you want to
continue after the cause of the error has been fixed, you have to invoke
this function in order to reset the document error state.

### 参数

此函数没有参数。

### 返回值

Always succeeds and returns **`TRUE`**.

HaruDoc::resetStream
====================

Rewind the temporary stream

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::resetStream</span> ( <span
class="methodparam">void</span> )

Rewinds the temporary stream of the document.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::saveToStream</span>
-   <span class="methodname">HaruDoc::getStreamSize</span>
-   <span class="methodname">HaruDoc::readFromStream</span>

HaruDoc::save
=============

Save the document into the specified file

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::save</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

Saves the document into the specified file.

### 参数

`file`  
The file to save the document to.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::output</span>

HaruDoc::saveToStream
=====================

Save the document into a temporary stream

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::saveToStream</span> ( <span
class="methodparam">void</span> )

Saves the document data into a temporary stream.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::resetStream</span>
-   <span class="methodname">HaruDoc::getStreamSize</span>
-   <span class="methodname">HaruDoc::readFromStream</span>

HaruDoc::setCompressionMode
===========================

Set compression mode for the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setCompressionMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

Defines compression mode for the document. In case when libharu was
compiled without Zlib support this function will always throw <span
class="classname">HaruException</span>.

### 参数

`mode`  
The compression mode to use. The value is a combination of the following
flags:

-   **`HaruDoc::COMP_NONE`** - all contents is not compressed.
-   **`HaruDoc::COMP_TEXT`** - compress the text data.
-   **`HaruDoc::COMP_IMAGE`** - compress the image data.
-   **`HaruDoc::COMP_METADATA`** - compress other data (fonts, cmaps).
-   **`HaruDoc::COMP_ALL`** - compress all data.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::setCurrentEncoder
==========================

Set the current encoder for the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setCurrentEncoder</span> ( <span
class="methodparam"><span class="type">string</span> `$encoding`</span>
)

Defines the encoder currently used in the document.

### 参数

`encoding`  
The name of the encoding to use. See
<a href="/haru/builtin.html#Builtin%20Encodings" class="link">Builtin Encodings</a>
for the list of allowed values.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::setEncryptionMode
==========================

Set encryption mode for the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setEncryptionMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">int</span> `$key_len`<span
class="initializer"> = 5</span></span> \] )

Defines encryption mode for the document. The encryption mode cannot be
set before setting the password.

### 参数

`mode`  
The encryption mode to use. Can be one of the following:

-   **`HaruDoc::ENCRYPT_R2`** - use "revision2" algorithm.
-   **`HaruDoc::ENCRYPT_R3`** - use "revision3" algorithm. Using this
    value bumps the version of PDF to 1.4.

`key_len`  
The encryption key length in bytes. This parameter is optional and used
only when mode is **`HaruDoc::ENCRYPT_R3`**. The default value is 5
(40bit).

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setPassword</span>
-   <span class="methodname">HaruDoc::setPermission</span>

HaruDoc::setInfoAttr
====================

Set the info attribute of the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setInfoAttr</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$info`</span> )

Defines an info attribute. Uses the current encoding of the document.

### 参数

`type`  
The type of the attribute. Can be one of the following:

-   **`HaruDoc::INFO_AUTHOR`**
-   **`HaruDoc::INFO_CREATOR`**
-   **`HaruDoc::INFO_TITLE`**
-   **`HaruDoc::INFO_SUBJECT`**
-   **`HaruDoc::INFO_KEYWORDS`**

`info`  
The value of the attribute.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setInfoDateAttr</span>

HaruDoc::setInfoDateAttr
========================

Set the datetime info attributes of the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setInfoDateAttr</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">int</span> `$year`</span> , <span
class="methodparam"><span class="type">int</span> `$month`</span> ,
<span class="methodparam"><span class="type">int</span> `$day`</span> ,
<span class="methodparam"><span class="type">int</span> `$hour`</span> ,
<span class="methodparam"><span class="type">int</span> `$min`</span> ,
<span class="methodparam"><span class="type">int</span> `$sec`</span> ,
<span class="methodparam"><span class="type">string</span> `$ind`</span>
, <span class="methodparam"><span class="type">int</span>
`$off_hour`</span> , <span class="methodparam"><span
class="type">int</span> `$off_min`</span> )

Sets the datetime info attributes of the document.

### 参数

`type`  
The type of the attribute. Can be one of the following:

-   **`HaruDoc::INFO_CREATION_DATE`**
-   **`HaruDoc::INFO_MOD_DATE`**

`year`  

`month`  
Between 1 and 12.

`day`  
Between 1 and 31, 30, 29 or 28 (different for each month).

`hour`  
Between 0 and 23.

`min`  
Between 0 and 59.

`sec`  
Between 0 and 59.

`ind`  
The timezone relation to UTC, can be "", " ", "+", "-" and "Z".

`off_hour`  
If `ind` is not " " or "", values between 0 and 23 are valid. Otherwise,
this parameter is ignored.

`off_min`  
If `ind` is not " " or "", values between 0 and 59 are valid. Otherwise,
this parameter is ignored.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setInfoAttr</span>

HaruDoc::setOpenAction
======================

Define which page is shown when the document is opened

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setOpenAction</span> ( <span
class="methodparam"><span class="type">object</span>
`$destination`</span> )

Defines which page should be shown when the document is opened.

### 参数

`destination`  
A valid <span class="classname">HaruDestination</span> instance.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::setPageLayout
======================

Set how pages should be displayed

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setPageLayout</span> ( <span
class="methodparam"><span class="type">int</span> `$layout`</span> )

Defines how pages should be displayed.

### 参数

`layout`  
The following values are accepted:

-   **`HaruDoc::PAGE_LAYOUT_SINGLE`** - only one page is displayed.
-   **`HaruDoc::PAGE_LAYOUT_ONE_COLUMN`** - display the pages in one
    column.
-   **`HaruDoc::PAGE_LAYOUT_TWO_COLUMN_LEFT`** - display pages in two
    columns, first page left.
-   **`HaruDoc::PAGE_LAYOUT_TWO_COLUMN_RIGHT`** - display pages in two
    columns, first page right.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::getPageLayout</span>

HaruDoc::setPageMode
====================

Set how the document should be displayed

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setPageMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

Defines how the document should be displayed.

### 参数

`mode`  
The following values are accepted:

-   **`HaruDoc::PAGE_MODE_USE_NONE`** - display the document with
    neither outline nor thumbnail.
-   **`HaruDoc::PAGE_MODE_USE_OUTLINE`** - display the document with
    outline pane.
-   **`HaruDoc::PAGE_MODE_USE_THUMBS`** - display the document with
    thumbnail pane.
-   **`HaruDoc::PAGE_MODE_FULL_SCREEN`** - display the document with
    full screen mode.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::getPageMode</span>

HaruDoc::setPagesConfiguration
==============================

Set the number of pages per set of pages

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setPagesConfiguration</span> ( <span
class="methodparam"><span class="type">int</span>
`$page_per_pages`</span> )

By default the document has one pages object as a root for all pages.
All page objects are create as branches of this object. One pages object
can contain only 8191, therefore the maximum number of pages per
document is 8191. But you can change that fact by setting
`page_per_pages` parameter, so that the root pages object contains 8191
more pages (not page) objects, which in turn contain 8191 pages each. So
the maximum number of pages in the document becomes
8191\*`page_per_pages`.

### 参数

`page_per_pages`  
The numbers of pages that a pages object can contain.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDoc::setPassword
====================

Set owner and user passwords for the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setPassword</span> ( <span
class="methodparam"><span class="type">string</span>
`$owner_password`</span> , <span class="methodparam"><span
class="type">string</span> `$user_password`</span> )

Defines owner and user passwords for the document. Setting the passwords
makes the document contents encrypted.

### 参数

`owner_password`  
The password of the owner, which can change permissions of the document.
Empty password is not accepted. Owner's password cannot be the same as
the user's password.

`user_password`  
The password of the user. Can be empty.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setEncryptionMode</span>
-   <span class="methodname">HaruDoc::setPermission</span>

HaruDoc::setPermission
======================

Set permissions for the document

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::setPermission</span> ( <span
class="methodparam"><span class="type">int</span> `$permission`</span> )

Defines permissions for the document.

### 参数

`permission`  
The values is a combination of these flags:

-   **`HaruDoc::ENABLE_READ`** - user can read the document.
-   **`HaruDoc::ENABLE_PRINT`** - user can print the document.
-   **`HaruDoc::ENABLE_EDIT_ALL`** - user can edit the contents of the
    document other than annotations and form fields.
-   **`HaruDoc::ENABLE_COPY`** - user can copy the text and the graphics
    of the document.
-   **`HaruDoc::ENABLE_EDIT`** - user can add or modify the annotations
    and form fields of the document.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::setPassword</span>
-   <span class="methodname">HaruDoc::setEncryptionMode</span>

HaruDoc::useCNSEncodings
========================

Enable Chinese simplified encodings

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useCNSEncodings</span> ( <span
class="methodparam">void</span> )

Enables Chinese simplified encodings.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useCNSFonts</span>

HaruDoc::useCNSFonts
====================

Enable builtin Chinese simplified fonts

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useCNSFonts</span> ( <span
class="methodparam">void</span> )

Enables builtin Chinese simplified fonts.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useCNSEncodings</span>

HaruDoc::useCNTEncodings
========================

Enable Chinese traditional encodings

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useCNTEncodings</span> ( <span
class="methodparam">void</span> )

Enables Chinese traditional encodings.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useCNTFonts</span>

HaruDoc::useCNTFonts
====================

Enable builtin Chinese traditional fonts

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useCNTFonts</span> ( <span
class="methodparam">void</span> )

Enables builtin Chinese traditional fonts.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useCNTEncodings</span>

HaruDoc::useJPEncodings
=======================

Enable Japanese encodings

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useJPEncodings</span> ( <span
class="methodparam">void</span> )

Enables Japanese encodings.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useJPFonts</span>

HaruDoc::useJPFonts
===================

Enable builtin Japanese fonts

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useJPFonts</span> ( <span
class="methodparam">void</span> )

Enables builtin Japanese fonts.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useJPEncodings</span>

HaruDoc::useKREncodings
=======================

Enable Korean encodings

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useKREncodings</span> ( <span
class="methodparam">void</span> )

Enables Korean encodings.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useKRFonts</span>

HaruDoc::useKRFonts
===================

Enable builtin Korean fonts

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDoc::useKRFonts</span> ( <span
class="methodparam">void</span> )

Enables builtin Korean fonts.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::useKREncodings</span>

简介
----

Haru PDF Page Class.

类摘要
------

**HaruPage**

<span class="ooclass"> class **HaruPage** </span> {

/\* 方法 \*/

<span class="type">bool</span> <span class="methodname">arc</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> ,
<span class="methodparam"><span class="type">float</span> `$ray`</span>
, <span class="methodparam"><span class="type">float</span>
`$ang1`</span> , <span class="methodparam"><span
class="type">float</span> `$ang2`</span> )

<span class="type">bool</span> <span class="methodname">beginText</span>
( <span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">circle</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> ,
<span class="methodparam"><span class="type">float</span> `$ray`</span>
)

<span class="type">bool</span> <span class="methodname">closePath</span>
( <span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">concat</span> (
<span class="methodparam"><span class="type">float</span> `$a`</span> ,
<span class="methodparam"><span class="type">float</span> `$b`</span> ,
<span class="methodparam"><span class="type">float</span> `$c`</span> ,
<span class="methodparam"><span class="type">float</span> `$d`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">object</span> <span
class="methodname">createDestination</span> ( <span
class="methodparam">void</span> )

<span class="type">object</span> <span
class="methodname">createLinkAnnotation</span> ( <span
class="methodparam"><span class="type">array</span> `$rectangle`</span>
, <span class="methodparam"><span class="type">object</span>
`$destination`</span> )

<span class="type">object</span> <span
class="methodname">createTextAnnotation</span> ( <span
class="methodparam"><span class="type">array</span> `$rectangle`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> \[, <span class="methodparam"><span
class="type">object</span> `$encoder`</span> \] )

<span class="type">object</span> <span
class="methodname">createURLAnnotation</span> ( <span
class="methodparam"><span class="type">array</span> `$rectangle`</span>
, <span class="methodparam"><span class="type">string</span>
`$url`</span> )

<span class="type">bool</span> <span class="methodname">curveTo2</span>
( <span class="methodparam"><span class="type">float</span> `$x2`</span>
, <span class="methodparam"><span class="type">float</span> `$y2`</span>
, <span class="methodparam"><span class="type">float</span> `$x3`</span>
, <span class="methodparam"><span class="type">float</span> `$y3`</span>
)

<span class="type">bool</span> <span class="methodname">curveTo3</span>
( <span class="methodparam"><span class="type">float</span> `$x1`</span>
, <span class="methodparam"><span class="type">float</span> `$y1`</span>
, <span class="methodparam"><span class="type">float</span> `$x3`</span>
, <span class="methodparam"><span class="type">float</span> `$y3`</span>
)

<span class="type">bool</span> <span class="methodname">curveTo</span> (
<span class="methodparam"><span class="type">float</span> `$x1`</span> ,
<span class="methodparam"><span class="type">float</span> `$y1`</span> ,
<span class="methodparam"><span class="type">float</span> `$x2`</span> ,
<span class="methodparam"><span class="type">float</span> `$y2`</span> ,
<span class="methodparam"><span class="type">float</span> `$x3`</span> ,
<span class="methodparam"><span class="type">float</span> `$y3`</span> )

<span class="type">bool</span> <span class="methodname">drawImage</span>
( <span class="methodparam"><span class="type">object</span>
`$image`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$width`</span> , <span
class="methodparam"><span class="type">float</span> `$height`</span> )

<span class="type">bool</span> <span class="methodname">ellipse</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> ,
<span class="methodparam"><span class="type">float</span> `$xray`</span>
, <span class="methodparam"><span class="type">float</span>
`$yray`</span> )

<span class="type">bool</span> <span class="methodname">endPath</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">endText</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">eofill</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">eoFillStroke</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$close_path`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="type">bool</span> <span class="methodname">fill</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">fillStroke</span> (\[ <span class="methodparam"><span
class="type">bool</span> `$close_path`<span class="initializer"> =
**`FALSE`**</span></span> \] )

<span class="type">float</span> <span
class="methodname">getCharSpace</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getCMYKFill</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getCMYKStroke</span> ( <span
class="methodparam">void</span> )

<span class="type">object</span> <span
class="methodname">getCurrentFont</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getCurrentFontSize</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getCurrentPos</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getCurrentTextPos</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span class="methodname">getDash</span>
( <span class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getFillingColorSpace</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getFlatness</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">getGMode</span> (
<span class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getGrayFill</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getGrayStroke</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getHeight</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getHorizontalScaling</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">getLineCap</span>
( <span class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getLineJoin</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getLineWidth</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getMiterLimit</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getRGBFill</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getRGBStroke</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getStrokingColorSpace</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getTextLeading</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getTextMatrix</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getTextRenderingMode</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getTextRise</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getTextWidth</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

<span class="type">array</span> <span
class="methodname">getTransMatrix</span> ( <span
class="methodparam">void</span> )

<span class="type">float</span> <span class="methodname">getWidth</span>
( <span class="methodparam">void</span> )

<span class="type">float</span> <span
class="methodname">getWordSpace</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">lineTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">int</span> <span
class="methodname">measureText</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$wordwrap`<span class="initializer"> = **`FALSE`**</span></span> \] )

<span class="type">bool</span> <span
class="methodname">moveTextPos</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$set_leading`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="type">bool</span> <span class="methodname">moveTo</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">bool</span> <span
class="methodname">moveToNextLine</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">rectangle</span>
( <span class="methodparam"><span class="type">float</span> `$x`</span>
, <span class="methodparam"><span class="type">float</span> `$y`</span>
, <span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

<span class="type">bool</span> <span
class="methodname">setCharSpace</span> ( <span class="methodparam"><span
class="type">float</span> `$char_space`</span> )

<span class="type">bool</span> <span
class="methodname">setCMYKFill</span> ( <span class="methodparam"><span
class="type">float</span> `$c`</span> , <span class="methodparam"><span
class="type">float</span> `$m`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$k`</span> )

<span class="type">bool</span> <span
class="methodname">setCMYKStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$m`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$k`</span> )

<span class="type">bool</span> <span class="methodname">setDash</span> (
<span class="methodparam"><span class="type">array</span>
`$pattern`</span> , <span class="methodparam"><span
class="type">int</span> `$phase`</span> )

<span class="type">bool</span> <span
class="methodname">setFlatness</span> ( <span class="methodparam"><span
class="type">float</span> `$flatness`</span> )

<span class="type">bool</span> <span
class="methodname">setFontAndSize</span> ( <span
class="methodparam"><span class="type">object</span> `$font`</span> ,
<span class="methodparam"><span class="type">float</span> `$size`</span>
)

<span class="type">bool</span> <span
class="methodname">setGrayFill</span> ( <span class="methodparam"><span
class="type">float</span> `$value`</span> )

<span class="type">bool</span> <span
class="methodname">setGrayStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$value`</span> )

<span class="type">bool</span> <span class="methodname">setHeight</span>
( <span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="type">bool</span> <span
class="methodname">setHorizontalScaling</span> ( <span
class="methodparam"><span class="type">float</span> `$scaling`</span> )

<span class="type">bool</span> <span
class="methodname">setLineCap</span> ( <span class="methodparam"><span
class="type">int</span> `$cap`</span> )

<span class="type">bool</span> <span
class="methodname">setLineJoin</span> ( <span class="methodparam"><span
class="type">int</span> `$join`</span> )

<span class="type">bool</span> <span
class="methodname">setLineWidth</span> ( <span class="methodparam"><span
class="type">float</span> `$width`</span> )

<span class="type">bool</span> <span
class="methodname">setMiterLimit</span> ( <span
class="methodparam"><span class="type">float</span> `$limit`</span> )

<span class="type">bool</span> <span
class="methodname">setRGBFill</span> ( <span class="methodparam"><span
class="type">float</span> `$r`</span> , <span class="methodparam"><span
class="type">float</span> `$g`</span> , <span class="methodparam"><span
class="type">float</span> `$b`</span> )

<span class="type">bool</span> <span
class="methodname">setRGBStroke</span> ( <span class="methodparam"><span
class="type">float</span> `$r`</span> , <span class="methodparam"><span
class="type">float</span> `$g`</span> , <span class="methodparam"><span
class="type">float</span> `$b`</span> )

<span class="type">bool</span> <span class="methodname">setRotate</span>
( <span class="methodparam"><span class="type">int</span>
`$angle`</span> )

<span class="type">bool</span> <span class="methodname">setSize</span> (
<span class="methodparam"><span class="type">int</span> `$size`</span> ,
<span class="methodparam"><span class="type">int</span>
`$direction`</span> )

<span class="type">bool</span> <span
class="methodname">setSlideShow</span> ( <span class="methodparam"><span
class="type">int</span> `$type`</span> , <span class="methodparam"><span
class="type">float</span> `$disp_time`</span> , <span
class="methodparam"><span class="type">float</span> `$trans_time`</span>
)

<span class="type">bool</span> <span
class="methodname">setTextLeading</span> ( <span
class="methodparam"><span class="type">float</span>
`$text_leading`</span> )

<span class="type">bool</span> <span
class="methodname">setTextMatrix</span> ( <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> , <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$d`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="type">bool</span> <span
class="methodname">setTextRenderingMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="type">bool</span> <span
class="methodname">setTextRise</span> ( <span class="methodparam"><span
class="type">float</span> `$rise`</span> )

<span class="type">bool</span> <span class="methodname">setWidth</span>
( <span class="methodparam"><span class="type">float</span>
`$width`</span> )

<span class="type">bool</span> <span
class="methodname">setWordSpace</span> ( <span class="methodparam"><span
class="type">float</span> `$word_space`</span> )

<span class="type">bool</span> <span class="methodname">showText</span>
( <span class="methodparam"><span class="type">string</span>
`$text`</span> )

<span class="type">bool</span> <span
class="methodname">showTextNextLine</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$word_space`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$char_space`<span
class="initializer"> = 0</span></span> \]\] )

<span class="type">bool</span> <span class="methodname">stroke</span>
(\[ <span class="methodparam"><span class="type">bool</span>
`$close_path`<span class="initializer"> = **`FALSE`**</span></span> \] )

<span class="type">bool</span> <span class="methodname">textOut</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

<span class="type">bool</span> <span class="methodname">textRect</span>
( <span class="methodparam"><span class="type">float</span>
`$left`</span> , <span class="methodparam"><span
class="type">float</span> `$top`</span> , <span
class="methodparam"><span class="type">float</span> `$right`</span> ,
<span class="methodparam"><span class="type">float</span>
`$bottom`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> \[, <span
class="methodparam"><span class="type">int</span> `$align`<span
class="initializer"> = HaruPage::TALIGN\_LEFT</span></span> \] )

}

预定义常量
----------

| Type | Name                                                | Description |
|------|-----------------------------------------------------|-------------|
| int  | HaruPage::GMODE\_PAGE\_DESCRIPTION                  |             |
| int  | HaruPage::GMODE\_TEXT\_OBJECT                       |             |
| int  | HaruPage::GMODE\_PATH\_OBJECT                       |             |
| int  | HaruPage::GMODE\_CLIPPING\_PATH                     |             |
| int  | HaruPage::GMODE\_SHADING                            |             |
| int  | HaruPage::GMODE\_INLINE\_IMAGE                      |             |
| int  | HaruPage::GMODE\_EXTERNAL\_OBJECT                   |             |
| int  | HaruPage::BUTT\_END                                 |             |
| int  | HaruPage::ROUND\_END                                |             |
| int  | HaruPage::PROJECTING\_SCUARE\_END                   |             |
| int  | HaruPage::MITER\_JOIN                               |             |
| int  | HaruPage::ROUND\_JOIN                               |             |
| int  | HaruPage::BEVEL\_JOIN                               |             |
| int  | HaruPage::FILL                                      |             |
| int  | HaruPage::STROKE                                    |             |
| int  | HaruPage::FILL\_THEN\_STROKE                        |             |
| int  | HaruPage::INVISIBLE                                 |             |
| int  | HaruPage::FILL\_CLIPPING                            |             |
| int  | HaruPage::STROKE\_CLIPPING                          |             |
| int  | HaruPage::FILL\_STROKE\_CLIPPING                    |             |
| int  | HaruPage::CLIPPING                                  |             |
| int  | HaruPage::TALIGN\_LEFT                              |             |
| int  | HaruPage::TALIGN\_RIGHT                             |             |
| int  | HaruPage::TALIGN\_CENTER                            |             |
| int  | HaruPage::TALIGN\_JUSTIFY                           |             |
| int  | HaruPage::SIZE\_LETTER                              |             |
| int  | HaruPage::SIZE\_LEGAL                               |             |
| int  | HaruPage::SIZE\_A3                                  |             |
| int  | HaruPage::SIZE\_A4                                  |             |
| int  | HaruPage::SIZE\_A5                                  |             |
| int  | HaruPage::SIZE\_B4                                  |             |
| int  | HaruPage::SIZE\_B5                                  |             |
| int  | HaruPage::SIZE\_EXECUTIVE                           |             |
| int  | HaruPage::SIZE\_US4x6                               |             |
| int  | HaruPage::SIZE\_US4x8                               |             |
| int  | HaruPage::SIZE\_US5x7                               |             |
| int  | HaruPage::SIZE\_COMM10                              |             |
| int  | HaruPage::PORTRAIT                                  |             |
| int  | HaruPage::LANDSCAPE                                 |             |
| int  | HaruPage::TS\_WIPE\_LIGHT                           |             |
| int  | HaruPage::TS\_WIPE\_UP                              |             |
| int  | HaruPage::TS\_WIPE\_LEFT                            |             |
| int  | HaruPage::TS\_WIPE\_DOWN                            |             |
| int  | HaruPage::TS\_BARN\_DOORS\_HORIZONTAL\_OUT          |             |
| int  | HaruPage::TS\_BARN\_DOORS\_HORIZONTAL\_IN           |             |
| int  | HaruPage::TS\_BARN\_DOORS\_VERTICAL\_OUT            |             |
| int  | HaruPage::TS\_BARN\_DOORS\_VERTICAL\_IN             |             |
| int  | HaruPage::TS\_BOX\_OUT                              |             |
| int  | HaruPage::TS\_BOX\_IN                               |             |
| int  | HaruPage::TS\_BLINDS\_HORIZONTAL                    |             |
| int  | HaruPage::TS\_BLINDS\_VERTICAL                      |             |
| int  | HaruPage::TS\_DISSOLVE                              |             |
| int  | HaruPage::TS\_GLITTER\_RIGHT                        |             |
| int  | HaruPage::TS\_GLITTER\_DOWN                         |             |
| int  | HaruPage::TS\_GLITTER\_TOP\_LEFT\_TO\_BOTTOM\_RIGHT |             |
| int  | HaruPage::TS\_REPLACE                               |             |
| int  | HaruPage::NUM\_STYLE\_DECIMAL                       |             |
| int  | HaruPage::NUM\_STYLE\_UPPER\_ROMAN                  |             |
| int  | HaruPage::NUM\_STYLE\_LOWER\_ROMAN                  |             |
| int  | HaruPage::NUM\_STYLE\_UPPER\_LETTERS                |             |
| int  | HaruPage::NUM\_STYLE\_LOWER\_LETTERS                |             |

HaruPage::arc
=============

Append an arc to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::arc</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$ray`</span> ,
<span class="methodparam"><span class="type">float</span> `$ang1`</span>
, <span class="methodparam"><span class="type">float</span>
`$ang2`</span> )

Appends an arc to the current path.

### 参数

`x`  
Horizontal coordinate of the center.

`y`  
Vertical coordinate of the center.

`ray`  
The ray of the arc.

`ang1`  
The angle of the beginning.

`ang2`  
The angle of the end. Must be greater than `ang1`.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::beginText
===================

Begin a text object and set the current text position to (0,0)

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::beginText</span> ( <span
class="methodparam">void</span> )

Begins new text object and sets the current text position to (0,0).

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::circle
================

Append a circle to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::circle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$ray`</span> )

Appends a circle to the current path.

### 参数

`x`  
Horizontal coordinate of the center point.

`y`  
Vertical coordinate of the center point.

`ray`  
The ray of the circle.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::closePath
===================

Append a straight line from the current point to the start point of the
path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::closePath</span> ( <span
class="methodparam">void</span> )

Appends a straight line from the current point to the start point of the
path.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::concat
================

Concatenate current transformation matrix of the page and the specified
matrix

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::concat</span> ( <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> , <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$d`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Concatenates current transformation matrix of the page and the specified
matrix.

### 参数

`a`  

`b`  

`c`  

`d`  

`x`  

`y`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::createDestination
===========================

Create new <span class="classname">HaruDestination</span> instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruPage::createDestination</span> ( <span
class="methodparam">void</span> )

Create a new <span class="classname">HaruDestination</span> instance.

### 参数

此函数没有参数。

### 返回值

Returns a new <span class="classname">HaruDestination</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::createLinkAnnotation
==============================

Create new <span class="classname">HaruAnnotation</span> instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruPage::createLinkAnnotation</span> ( <span
class="methodparam"><span class="type">array</span> `$rectangle`</span>
, <span class="methodparam"><span class="type">object</span>
`$destination`</span> )

Creates a new <span class="classname">HaruAnnotation</span> instance.

### 参数

`rectangle`  
An array with 4 coordinates of the clickable area.

`destination`  
Valid <span class="classname">HaruDestination</span> instance.

### 返回值

Returns a new <span class="classname">HaruAnnotation</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::createTextAnnotation
==============================

Create new <span class="classname">HaruAnnotation</span> instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruPage::createTextAnnotation</span> ( <span
class="methodparam"><span class="type">array</span> `$rectangle`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> \[, <span class="methodparam"><span
class="type">object</span> `$encoder`</span> \] )

Creates a new <span class="classname">HaruAnnotation</span> instance.

### 参数

`rectangle`  
An array with 4 coordinates of the annotation area.

`text`  
The text to be displayed.

`encoder`  
Optional <span class="classname">HaruEncoder</span> instance.

### 返回值

Returns a new <span class="classname">HaruAnnotation</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::createURLAnnotation
=============================

Create and return new <span class="classname">HaruAnnotation</span>
instance

### 说明

<span class="type">object</span> <span
class="methodname">HaruPage::createURLAnnotation</span> ( <span
class="methodparam"><span class="type">array</span> `$rectangle`</span>
, <span class="methodparam"><span class="type">string</span>
`$url`</span> )

Creates a new <span class="classname">HaruAnnotation</span> instance.

### 参数

`rectangle`  
An array with 4 coordinates of the clickable area.

`url`  
The URL to open.

### 返回值

Returns a new <span class="classname">HaruAnnotation</span> instance.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::curveTo2
==================

Append a Bezier curve to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::curveTo2</span> ( <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

Appends a Bezier curve to the current path. The current point and the
point (x2, y2) are used as the control points for the Bezier curve and
current point is moved to the point (x3, y3).

### 参数

`x2`  
A Bezier curve control point.

`y2`  
A Bezier curve control point.

`x3`  
The current point moves here.

`x3`  
The current point moves here.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::curveTo3
==================

Append a Bezier curve to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::curveTo3</span> ( <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

Appends a Bezier curve to the current path. The point (x1, y1) and the
point (x3, y3) are used as the control points for a Bezier curve and
current point is moved to the point (x3, y3).

### 参数

`x1`  
A Bezier curve control point.

`y1`  
A Bezier curve control point.

`x3`  
The current point moves here.

`x3`  
The current point moves here.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::curveTo
=================

Append a Bezier curve to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::curveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

Append a Bezier curve to the current path. The point (x1, y1) and the
point (x2, y2) are used as the control points for a Bezier curve and
current point is moved to the point (x3, y3).

### 参数

`x1`  
A Bezier curve control point.

`y1`  
A Bezier curve control point.

`x2`  
A Bezier curve control point.

`y2`  
A Bezier curve control point.

`x3`  
The current point moves here.

`x3`  
The current point moves here.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::drawImage
===================

Show image at the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::drawImage</span> ( <span
class="methodparam"><span class="type">object</span> `$image`</span> ,
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

Show image at the page.

### 参数

`image`  
Valid <span class="classname">HaruImage</span> instance.

`x`  
The left border of the area where the image is displayed.

`y`  
The lower border of the area where the image is displayed.

`width`  
The width of the image area.

`height`  
The height of the image area.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::ellipse
=================

Append an ellipse to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::ellipse</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$xray`</span> ,
<span class="methodparam"><span class="type">float</span> `$yray`</span>
)

Appends an ellipse to the current path.

### 参数

`x`  
Horizontal coordinate of the center.

`y`  
Vertical coordinate of the center.

`xray`  
The ray of the ellipse in the x direction.

`yray`  
The ray of the ellipse in the y direction.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::endPath
=================

End current path object without filling and painting operations

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::endPath</span> ( <span
class="methodparam">void</span> )

Ends current path object without performing filling and painting
operations.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::endText
=================

End current text object

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::endText</span> ( <span
class="methodparam">void</span> )

Finalizes current text object.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::eofill
================

Fill current path using even-odd rule

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::eofill</span> ( <span
class="methodparam">void</span> )

Fills current path using even-odd rule.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::eoFillStroke
======================

Fill current path using even-odd rule, then paint the path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::eoFillStroke</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$close_path`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Fills current path using even-odd rule, then paints the path.

### 参数

`close_path`  
Optional parameter. When set to **`TRUE`**, the function closes the
current path. Default to **`FALSE`**.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::fill
==============

Fill current path using nonzero winding number rule

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::fill</span> ( <span
class="methodparam">void</span> )

Fills current path using nonzero winding number rule.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::fillStroke
====================

Fill current path using nonzero winding number rule, then paint the path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::fillStroke</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$close_path`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Fills current path using nonzero winding number rule, then paints the
path.

### 参数

`close_path`  
Optional parameter. When set to **`TRUE`**, the function closes the
current path. Default to **`FALSE`**.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCharSpace
======================

Get the current value of character spacing

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getCharSpace</span> ( <span
class="methodparam">void</span> )

Get the current value of character spacing.

### 参数

此函数没有参数。

### 返回值

Returns the current value of character spacing.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCMYKFill
=====================

Get the current filling color

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getCMYKFill</span> ( <span
class="methodparam">void</span> )

Returns the current filling color.

### 参数

此函数没有参数。

### 返回值

Returns the current filling color as an array with 4 elements ("c", "m",
"y" and "k").

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCMYKStroke
=======================

Get the current stroking color

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getCMYKStroke</span> ( <span
class="methodparam">void</span> )

Get the current stroking color.

### 参数

此函数没有参数。

### 返回值

Returns the current stroking color as an array with 4 elements ("c",
"m", "y" and "k").

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCurrentFont
========================

Get the currently used font

### 说明

<span class="type">object</span> <span
class="methodname">HaruPage::getCurrentFont</span> ( <span
class="methodparam">void</span> )

Get the currently used font.

### 参数

此函数没有参数。

### 返回值

Returns the currently used font as an instance of <span
class="classname">HaruFont</span>.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCurrentFontSize
============================

Get the current font size

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getCurrentFontSize</span> ( <span
class="methodparam">void</span> )

Get the current font size.

### 参数

此函数没有参数。

### 返回值

Returns the current font size.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCurrentPos
=======================

Get the current position for path painting

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getCurrentPos</span> ( <span
class="methodparam">void</span> )

Get the current position for path painting.

### 参数

此函数没有参数。

### 返回值

Returns the current position for path painting as an array of with two
elements - "x" and "y".

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getCurrentTextPos
===========================

Get the current position for text printing

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getCurrentTextPos</span> ( <span
class="methodparam">void</span> )

Get the current position for text printing.

### 参数

此函数没有参数。

### 返回值

Returns the current position for text printing as an array with 2
elements - "x" and "y".

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getDash
=================

Get the current dash pattern

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getDash</span> ( <span
class="methodparam">void</span> )

Get the current dash pattern. See <span
class="methodname">HaruPage::setDash</span> for more information on dash
patterns.

### 参数

此函数没有参数。

### 返回值

Returns the current dash pattern as an array of two elements - "pattern"
and "phase" or **`FALSE`** if dash pattern was not set.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setDash</span>

HaruPage::getFillingColorSpace
==============================

Get the current filling color space

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::getFillingColorSpace</span> ( <span
class="methodparam">void</span> )

Get the current filling color space.

### 参数

此函数没有参数。

### 返回值

Returns the current filling color space. The result value is one of the
following:

-   **`HaruDoc::CS_DEVICE_GRAY`**
-   **`HaruDoc::CS_DEVICE_RGB`**
-   **`HaruDoc::CS_DEVICE_CMYK`**
-   **`HaruDoc::CS_CAL_GRAY`**
-   **`HaruDoc::CS_CAL_RGB`**
-   **`HaruDoc::CS_LAB`**
-   **`HaruDoc::CS_ICC_BASED`**
-   **`HaruDoc::CS_SEPARATION`**
-   **`HaruDoc::CS_DEVICE_N`**
-   **`HaruDoc::CS_INDEXED`**
-   **`HaruDoc::CS_PATTERN`**

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getFlatness
=====================

Get the flatness of the page

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getFlatness</span> ( <span
class="methodparam">void</span> )

Get the flatness of the page.

### 参数

此函数没有参数。

### 返回值

Returns the flatness of the page.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setFlatness</span>

HaruPage::getGMode
==================

Get the current graphics mode

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::getGMode</span> ( <span
class="methodparam">void</span> )

Get the current graphics mode.

### 参数

此函数没有参数。

### 返回值

Returns the current graphics mode. The result value is one of the
following:

-   **`HaruPage::GMODE_PAGE_DESCRIPTION`**
-   **`HaruPage::GMODE_TEXT_OBJECT`**
-   **`HaruPage::GMODE_PATH_OBJECT`**
-   **`HaruPage::GMODE_CLIPPING_PATH`**
-   **`HaruPage::GMODE_SHADING`**
-   **`HaruPage::GMODE_INLINE_IMAGE`**
-   **`HaruPage::GMODE_EXTERNAL_OBJECT`**

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::getGrayFill
=====================

Get the current filling color

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getGrayFill</span> ( <span
class="methodparam">void</span> )

Get the current filling color.

### 参数

此函数没有参数。

### 返回值

Returns the current filling color.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setGrayFill</span>

HaruPage::getGrayStroke
=======================

Get the current stroking color

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getGrayStroke</span> ( <span
class="methodparam">void</span> )

Get the current stroking color.

### 参数

此函数没有参数。

### 返回值

Returns the current stroking color.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setGrayStroke</span>

HaruPage::getHeight
===================

Get the height of the page

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getHeight</span> ( <span
class="methodparam">void</span> )

Get the height of the page.

### 参数

此函数没有参数。

### 返回值

Returns the height of the page.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setHeight</span>

HaruPage::getHorizontalScaling
==============================

Get the current value of horizontal scaling

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getHorizontalScaling</span> ( <span
class="methodparam">void</span> )

Get the current value of the horizontal scaling.

### 参数

此函数没有参数。

### 返回值

Returns the current value of horizontal scaling.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setHorizontalScaling</span>

HaruPage::getLineCap
====================

Get the current line cap style

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::getLineCap</span> ( <span
class="methodparam">void</span> )

Get the current line cap style.

### 参数

此函数没有参数。

### 返回值

Returns the current line cap style. The result value is one of the
following:

-   **`HaruPage::BUTT_END`** - the line is squared off at the endpoint
    of the path.
-   **`HaruPage::ROUND_END`** - the end of the line becomes a semicircle
    with center in the end point of the path.
-   **`HaruPage::PROJECTING_SCUARE_END`** - the line continues to the
    point that exceeds half of the stroke width the end point.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setLineCap</span>

HaruPage::getLineJoin
=====================

Get the current line join style

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::getLineJoin</span> ( <span
class="methodparam">void</span> )

Get the current line join style.

### 参数

此函数没有参数。

### 返回值

Returns the current line join style. The result value is one of the
following:

-   **`HaruPage::MITER_JOIN`**
-   **`HaruPage::ROUND_JOIN`**
-   **`HaruPage::BEVEL_JOIN`**

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setLineJoin</span>

HaruPage::getLineWidth
======================

Get the current line width

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getLineWidth</span> ( <span
class="methodparam">void</span> )

Get the current line width.

### 参数

此函数没有参数。

### 返回值

Returns the current line width.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setLineWidth</span>

HaruPage::getMiterLimit
=======================

Get the value of miter limit

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getMiterLimit</span> ( <span
class="methodparam">void</span> )

Get the value of the miter limit.

### 参数

此函数没有参数。

### 返回值

Returns the value of the miter limit.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setMiterLimit</span>

HaruPage::getRGBFill
====================

Get the current filling color

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getRGBFill</span> ( <span
class="methodparam">void</span> )

Get the current filling color.

### 参数

此函数没有参数。

### 返回值

Returns the current filling color as an array with 3 elements: "r", "g"
and "b".

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setRGBFill</span>

HaruPage::getRGBStroke
======================

Get the current stroking color

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getRGBStroke</span> ( <span
class="methodparam">void</span> )

Get the current stroking color.

### 参数

此函数没有参数。

### 返回值

Returns the current stroking color.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setRGBStroke</span>

HaruPage::getStrokingColorSpace
===============================

Get the current stroking color space

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::getStrokingColorSpace</span> ( <span
class="methodparam">void</span> )

Get the current stroking color space.

### 参数

此函数没有参数。

### 返回值

Returns the current stroking color space. The list of return values is
the same as for <span
class="methodname">HaruPage::getFillingColorSpace</span>

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getFillingColorSpace</span>

HaruPage::getTextLeading
========================

Get the current value of line spacing

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getTextLeading</span> ( <span
class="methodparam">void</span> )

Get the current value of line spacing.

### 参数

此函数没有参数。

### 返回值

Returns the current value of line spacing.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setTextLeading</span>

HaruPage::getTextMatrix
=======================

Get the current text transformation matrix of the page

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getTextMatrix</span> ( <span
class="methodparam">void</span> )

Get the current text transformation matrix of the page.

### 返回值

Returns the current text transformation matrix of the page as an array
of 6 elements: "a", "b", "c", "d", "x" and "y".

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setTextMatrix</span>

HaruPage::getTextRenderingMode
==============================

Get the current text rendering mode

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::getTextRenderingMode</span> ( <span
class="methodparam">void</span> )

Get the current text rendering mode.

### 参数

此函数没有参数。

### 返回值

Returns the current text rendering mode. The result value is one of the
following:

-   **`HaruPage::FILL`**
-   **`HaruPage::STROKE`**
-   **`HaruPage::FILL_THEN_STROKE`**
-   **`HaruPage::INVISIBLE`**
-   **`HaruPage::FILL_CLIPPING`**
-   **`HaruPage::STROKE_CLIPPING`**
-   **`HaruPage::FILL_STROKE_CLIPPING`**
-   **`HaruPage::CLIPPING`**

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setTextRenderingMode</span>

HaruPage::getTextRise
=====================

Get the current value of text rising

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getTextRise</span> ( <span
class="methodparam">void</span> )

Get the current value of text rising.

### 参数

此函数没有参数。

### 返回值

Returns the current value of text rising.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setTextRise</span>

HaruPage::getTextWidth
======================

Get the width of the text using current fontsize, character spacing and
word spacing

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getTextWidth</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Get the width of the text using current fontsize, character spacing and
word spacing

### 参数

`text`  
The text to measure.

### 返回值

Returns the width of the text using current fontsize, character spacing
and word spacing.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::measureText</span>

HaruPage::getTransMatrix
========================

Get the current transformation matrix of the page

### 说明

<span class="type">array</span> <span
class="methodname">HaruPage::getTransMatrix</span> ( <span
class="methodparam">void</span> )

Get the current transformation matrix of the page.

### 参数

此函数没有参数。

### 返回值

Returns the current transformation matrix of the page as an array of 6
elements: "a", "b", "c", "d", "x" and "y".

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::concat</span>

HaruPage::getWidth
==================

Get the width of the page

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getWidth</span> ( <span
class="methodparam">void</span> )

Get the width of the page.

### 参数

此函数没有参数。

### 返回值

Returns the width of the page.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setWidth</span>

HaruPage::getWordSpace
======================

Get the current value of word spacing

### 说明

<span class="type">float</span> <span
class="methodname">HaruPage::getWordSpace</span> ( <span
class="methodparam">void</span> )

Get the current value of word spacing.

### 参数

此函数没有参数。

### 返回值

Returns the current value of word spacing.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setWordSpace</span>

HaruPage::lineTo
================

Draw a line from the current point to the specified point

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::lineTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Draws a line from the current point to the specified point.

### 参数

`x`  

`y`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::curveTo</span>
-   <span class="methodname">HaruPage::curveTo2</span>
-   <span class="methodname">HaruPage::curveTo3</span>

HaruPage::measureText
=====================

Calculate the byte length of characters which can be included on one
line of the specified width

### 说明

<span class="type">int</span> <span
class="methodname">HaruPage::measureText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$wordwrap`<span class="initializer"> =
**`FALSE`**</span></span> \] )

Get the byte length of characters which can be included on one line of
the specified width.

### 参数

`text`  
The text to measure.

`width`  
The width of the line.

`wordwrap`  
When this parameter is set to **`TRUE`** the function "emulates" word
wrapping by stopping after the last full word (delimited by whitespace)
that can fit on the line.

### 返回值

Returns the byte length of characters which can be included within the
specified width. For single-byte encodings, this is equal to the number
of characters. For multi-byte encodings, this is not necessarily the
case.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruFont::measureText</span>

HaruPage::moveTextPos
=====================

Move text position to the specified offset

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::moveTextPos</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> \[,
<span class="methodparam"><span class="type">bool</span>
`$set_leading`<span class="initializer"> = **`FALSE`**</span></span> \]
)

Moves text position to the specified offset. If the start position of
the current line is (x1, y1), the start of the next line is (x1 + `x`,
y1 + `y`).

### 参数

`x`  
The specified text position offset.

`y`  
The specified text position offset.

`set_leading`  
If set to **`TRUE`**, the function sets the text leading to -`y`.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::moveToNextLine</span>

HaruPage::moveTo
================

Set starting point for new drawing path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::moveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Defines starting point for new drawing path.

### 参数

`x`  
A new starting point coordinate.

`y`  
A new starting point coordinate.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::moveToNextLine
========================

Move text position to the start of the next line

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::moveToNextLine</span> ( <span
class="methodparam">void</span> )

Moves text position to the start of the next line.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::moveTextPos</span>

HaruPage::rectangle
===================

Append a rectangle to the current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::rectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

Appends a rectangle to the current drawing path.

### 参数

`x`  
The left border of the rectangle.

`y`  
The lower border of the rectangle.

`width`  
The width of the rectangle.

`height`  
The height of the rectangle.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::setCharSpace
======================

Set character spacing for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setCharSpace</span> ( <span
class="methodparam"><span class="type">float</span> `$char_space`</span>
)

Defines character spacing for the page.

### 参数

`char_space`  
The new character spacing for the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getCharSpace</span>

HaruPage::setCMYKFill
=====================

Set filling color for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setCMYKFill</span> ( <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$m`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$k`</span> )

Defines filling color for the page.

### 参数

`c`  

`m`  

`y`  

`k`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getCMYKFill</span>

HaruPage::setCMYKStroke
=======================

Set stroking color for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setCMYKStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$m`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$k`</span> )

Defines stroking color for the page.

### 参数

`c`  

`m`  

`y`  

`k`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getCMYKStroke</span>

HaruPage::setDash
=================

Set the dash pattern for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setDash</span> ( <span
class="methodparam"><span class="type">array</span> `$pattern`</span> ,
<span class="methodparam"><span class="type">int</span> `$phase`</span>
)

Defines the dash pattern for the page.

### 参数

`pattern`  
An array (8 elements max) which contains a pattern of dashes and gaps
used for lines on the page.

`phase`  
The phase on which the pattern begins.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getDash</span>

HaruPage::setFlatness
=====================

Set flatness for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setFlatness</span> ( <span
class="methodparam"><span class="type">float</span> `$flatness`</span> )

Defines flatness for the page.

### 参数

`flatness`  
The defined flatness for the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getFlatness</span>

HaruPage::setFontAndSize
========================

Set font and fontsize for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setFontAndSize</span> ( <span
class="methodparam"><span class="type">object</span> `$font`</span> ,
<span class="methodparam"><span class="type">float</span> `$size`</span>
)

Defines current font and its size for the page.

### 参数

`font`  
A valid <span class="classname">HaruFont</span> instance.

`size`  
The size of the font.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruDoc::getFont</span>

HaruPage::setGrayFill
=====================

Set filling color for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setGrayFill</span> ( <span
class="methodparam"><span class="type">float</span> `$value`</span> )

Defines filling color for the page.

### 参数

`value`  
The value of gray level between 0 and 1.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getGrayFill</span>

HaruPage::setGrayStroke
=======================

Sets stroking color for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setGrayStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$value`</span> )

Defines stroking color for the page.

### 参数

`value`  
The value of gray level between 0 and 1.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getGrayStroke</span>

HaruPage::setHeight
===================

Set height of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setHeight</span> ( <span
class="methodparam"><span class="type">float</span> `$height`</span> )

Defines height of the page.

### 参数

`height`  
The defined height for the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getHeight</span>

HaruPage::setHorizontalScaling
==============================

Set horizontal scaling for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setHorizontalScaling</span> ( <span
class="methodparam"><span class="type">float</span> `$scaling`</span> )

Set the horizontal scaling for the page.

### 参数

`scaling`  
The horizontal scaling for text showing on the page. The initial value
is 100.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getHorizontalScaling</span>

HaruPage::setLineCap
====================

Set the shape to be used at the ends of lines

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setLineCap</span> ( <span
class="methodparam"><span class="type">int</span> `$cap`</span> )

Defines the shape to be used at the ends of lines.

### 参数

`cap`  
Must be one of the following values:

-   **`HaruPage::BUTT_END`** - the line is squared off at the endpoint
    of the path.
-   **`HaruPage::ROUND_END`** - the end of the line becomes a semicircle
    with center in the end point of the path.
-   **`HaruPage::PROJECTING_SCUARE_END`** - the line continues to the
    point that exceeds half of the stroke width the end point.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getLineCap</span>

HaruPage::setLineJoin
=====================

Set line join style for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setLineJoin</span> ( <span
class="methodparam"><span class="type">int</span> `$join`</span> )

Defines line join style for the page.

### 参数

`join`  
Must be one of the following values:

-   **`HaruPage::MITER_JOIN`**
-   **`HaruPage::ROUND_JOIN`**
-   **`HaruPage::BEVEL_JOIN`**

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getLineJoin</span>

HaruPage::setLineWidth
======================

Set line width for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setLineWidth</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

Defines line width for the page.

### 参数

`width`  
The defined line width for the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getLineWidth</span>

HaruPage::setMiterLimit
=======================

Set the current value of the miter limit of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setMiterLimit</span> ( <span
class="methodparam"><span class="type">float</span> `$limit`</span> )

Set the current value of the miter limit of the page.

### 参数

`limit`  
Defines the current value of the miter limit of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getMiterLimit</span>

HaruPage::setRGBFill
====================

Set filling color for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setRGBFill</span> ( <span
class="methodparam"><span class="type">float</span> `$r`</span> , <span
class="methodparam"><span class="type">float</span> `$g`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> )

Defines filling color for the page. All values must be between 0 and 1.

### 参数

`r`  

`g`  

`b`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getRGBFill</span>

HaruPage::setRGBStroke
======================

Set stroking color for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setRGBStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$r`</span> , <span
class="methodparam"><span class="type">float</span> `$g`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> )

Defines stroking color for the page. All values must be between 0 and 1.

### 参数

`r`  

`g`  

`b`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getRGBStroke</span>

HaruPage::setRotate
===================

Set rotation angle of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setRotate</span> ( <span
class="methodparam"><span class="type">int</span> `$angle`</span> )

Defines rotation angle of the page.

### 参数

`angle`  
Must be a multiple of 90 degrees.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::setSize
=================

Set size and direction of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setSize</span> ( <span
class="methodparam"><span class="type">int</span> `$size`</span> , <span
class="methodparam"><span class="type">int</span> `$direction`</span> )

Changes size and direction of the page to a predefined format.

### 参数

`size`  
Must be one of the following values:

-   **`HaruPage::SIZE_LETTER`**
-   **`HaruPage::SIZE_LEGAL`**
-   **`HaruPage::SIZE_A3`**
-   **`HaruPage::SIZE_A4`**
-   **`HaruPage::SIZE_A5`**
-   **`HaruPage::SIZE_B4`**
-   **`HaruPage::SIZE_B5`**
-   **`HaruPage::SIZE_EXECUTIVE`**
-   **`HaruPage::SIZE_US4x6`**
-   **`HaruPage::SIZE_US4x8`**
-   **`HaruPage::SIZE_US5x7`**
-   **`HaruPage::SIZE_COMM10`**

`direction`  
Must be one of the following values:

-   **`HaruPage::PORTRAIT`**
-   **`HaruPage::LANDSCAPE`**

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::setWidth</span>
-   <span class="methodname">HaruPage::setHeight</span>

HaruPage::setSlideShow
======================

Set transition style for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setSlideShow</span> ( <span
class="methodparam"><span class="type">int</span> `$type`</span> , <span
class="methodparam"><span class="type">float</span> `$disp_time`</span>
, <span class="methodparam"><span class="type">float</span>
`$trans_time`</span> )

Defines transition style for the page.

### 参数

`type`  
Must be one of the following values:

-   **`HaruPage::TS_WIPE_RIGHT`**
-   **`HaruPage::TS_WIPE_LEFT`**
-   **`HaruPage::TS_WIPE_UP`**
-   **`HaruPage::TS_WIPE_DOWN`**
-   **`HaruPage::TS_BARN_DOORS_HORIZONTAL_OUT`**
-   **`HaruPage::TS_BARN_DOORS_HORIZONTAL_IN`**
-   **`HaruPage::TS_BARN_DOORS_VERTICAL_OUT`**
-   **`HaruPage::TS_BARN_DOORS_VERTICAL_IN`**
-   **`HaruPage::TS_BOX_OUT`**
-   **`HaruPage::TS_BOX_IN`**
-   **`HaruPage::TS_BLINDS_HORIZONTAL`**
-   **`HaruPage::TS_BLINDS_VERTICAL`**
-   **`HaruPage::TS_DISSOLVE`**
-   **`HaruPage::TS_GLITTER_RIGHT`**
-   **`HaruPage::TS_GLITTER_DOWN`**
-   **`HaruPage::TS_GLITTER_TOP_LEFT_TO_BOTTOM_RIGHT`**
-   **`HaruPage::TS_REPLACE`**

`disp_time`  
The display duration of the page in seconds.

`trans_time`  
The duration of the transition effect in seconds.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::setTextLeading
========================

Set text leading (line spacing) for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setTextLeading</span> ( <span
class="methodparam"><span class="type">float</span>
`$text_leading`</span> )

Set the text leading (line spacing) for the page.

### 参数

`text_leading`  
Defines line spacing for the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getTextLeading</span>

HaruPage::setTextMatrix
=======================

Set the current text transformation matrix of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setTextMatrix</span> ( <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> , <span
class="methodparam"><span class="type">float</span> `$c`</span> , <span
class="methodparam"><span class="type">float</span> `$d`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Defines the text transformation matrix of the page.

### 参数

`a`  
Width multiplier.

`b`  
Vertical skew in radians.

`c`  
Horizontal skew in radians.

`d`  
Height multiplier.

`x`  
Horizontal position for text.

`y`  
Vertical position for text.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getTextMatrix</span>

HaruPage::setTextRenderingMode
==============================

Set text rendering mode for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setTextRenderingMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

Defines text rendering mode for the page.

### 参数

`mode`  
Must be one of the following values:

-   **`HaruPage::FILL`**
-   **`HaruPage::STROKE`**
-   **`HaruPage::FILL_THEN_STROKE`**
-   **`HaruPage::INVISIBLE`**
-   **`HaruPage::FILL_CLIPPING`**
-   **`HaruPage::STROKE_CLIPPING`**
-   **`HaruPage::FILL_STROKE_CLIPPING`**
-   **`HaruPage::CLIPPING`**

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getTextRenderingMode</span>

HaruPage::setTextRise
=====================

Set the current value of text rising

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setTextRise</span> ( <span
class="methodparam"><span class="type">float</span> `$rise`</span> )

Set the current value of text rising.

### 参数

`rise`  
Defines the current value of text rising.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getTextRise</span>

HaruPage::setWidth
==================

Set width of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setWidth</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

Set the width of the page.

### 参数

`width`  
Defines width of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getWidth</span>

HaruPage::setWordSpace
======================

Set word spacing for the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::setWordSpace</span> ( <span
class="methodparam"><span class="type">float</span> `$word_space`</span>
)

Set the word spacing for the page.

### 参数

`word_space`  
Defines word spacing for the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::getWordSpace</span>

HaruPage::showText
==================

Print text at the current position of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::showText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Prints out the text at the current position of the page.

### 参数

`text`  
The text to show.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::showTextNextLine</span>
-   <span class="methodname">HaruPage::textOut</span>

HaruPage::showTextNextLine
==========================

Move the current position to the start of the next line and print the
text

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::showTextNextLine</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$word_space`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$char_space`<span
class="initializer"> = 0</span></span> \]\] )

Moves the current position to the start of the next line and print out
the text.

### 参数

`text`  
The text to show.

`word_space`  
The word spacing.

`char_space`  
The character spacing.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::showText</span>
-   <span class="methodname">HaruPage::textOut</span>

HaruPage::stroke
================

Paint current path

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::stroke</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$close_path`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Paints the current path.

### 参数

`close_path`  
Closes the current path if set to **`TRUE`**.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruPage::textOut
=================

Print the text on the specified position

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::textOut</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Prints the text on the specified position.

### 参数

`x`  

`y`  

`text`  

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::showTextNextLine</span>
-   <span class="methodname">HaruPage::showText</span>

HaruPage::textRect
==================

Print the text inside the specified region

### 说明

<span class="type">bool</span> <span
class="methodname">HaruPage::textRect</span> ( <span
class="methodparam"><span class="type">float</span> `$left`</span> ,
<span class="methodparam"><span class="type">float</span> `$top`</span>
, <span class="methodparam"><span class="type">float</span>
`$right`</span> , <span class="methodparam"><span
class="type">float</span> `$bottom`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">int</span> `$align`<span
class="initializer"> = HaruPage::TALIGN\_LEFT</span></span> \] )

Prints the text inside the specified region.

### 参数

`left`  
Left border of the text area.

`top`  
Top border of the text area.

`right`  
Right border of the text area.

`bottom`  
Lower border of the text area.

`text`  
The text to print.

`align`  
Text alignment. Must be one of the following values:

-   **`HaruPage::TALIGN_LEFT`**
-   **`HaruPage::TALIGN_RIGHT`**
-   **`HaruPage::TALIGN_CENTER`**
-   **`HaruPage::TALIGN_JUSTIFY`**

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

### 参见

-   <span class="methodname">HaruPage::showTextNextLine</span>
-   <span class="methodname">HaruPage::showText</span>
-   <span class="methodname">HaruPage::textOut</span>

简介
----

Haru PDF Font Class.

类摘要
------

**HaruFont**

<span class="ooclass"> class **HaruFont** </span> {

/\* 方法 \*/

<span class="type">int</span> <span class="methodname">getAscent</span>
( <span class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">getCapHeight</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">getDescent</span>
( <span class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">getEncodingName</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">getFontName</span> ( <span
class="methodparam">void</span> )

<span class="type">array</span> <span
class="methodname">getTextWidth</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> )

<span class="type">int</span> <span
class="methodname">getUnicodeWidth</span> ( <span
class="methodparam"><span class="type">int</span> `$character`</span> )

<span class="type">int</span> <span class="methodname">getXHeight</span>
( <span class="methodparam">void</span> )

<span class="type">int</span> <span
class="methodname">measureText</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$font_size`</span> , <span class="methodparam"><span
class="type">float</span> `$char_space`</span> , <span
class="methodparam"><span class="type">float</span> `$word_space`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$word_wrap`<span class="initializer"> = **`FALSE`**</span></span> \] )

}

HaruFont::getAscent
===================

Get the vertical ascent of the font

### 说明

<span class="type">int</span> <span
class="methodname">HaruFont::getAscent</span> ( <span
class="methodparam">void</span> )

Get the vertical ascent of the font.

### 参数

此函数没有参数。

### 返回值

Returns the vertical ascent of the font.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getCapHeight
======================

Get the distance from the baseline of uppercase letters

### 说明

<span class="type">int</span> <span
class="methodname">HaruFont::getCapHeight</span> ( <span
class="methodparam">void</span> )

Get the distance from the baseline of uppercase letters.

### 参数

此函数没有参数。

### 返回值

Returns the distance from the baseline of uppercase letters.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getDescent
====================

Get the vertical descent of the font

### 说明

<span class="type">int</span> <span
class="methodname">HaruFont::getDescent</span> ( <span
class="methodparam">void</span> )

Get the vertical descent of the font.

### 参数

此函数没有参数。

### 返回值

Return the vertical descent of the font.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getEncodingName
=========================

Get the name of the encoding

### 说明

<span class="type">string</span> <span
class="methodname">HaruFont::getEncodingName</span> ( <span
class="methodparam">void</span> )

Get the name of the font encoding.

### 参数

此函数没有参数。

### 返回值

Returns the name of the font encoding.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getFontName
=====================

Get the name of the font

### 说明

<span class="type">string</span> <span
class="methodname">HaruFont::getFontName</span> ( <span
class="methodparam">void</span> )

Get the name of the font.

### 参数

此函数没有参数。

### 返回值

Returns the name of the font.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getTextWidth
======================

Get the total width of the text, number of characters, number of words
and number of spaces

### 说明

<span class="type">array</span> <span
class="methodname">HaruFont::getTextWidth</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Get the total width of the text, number of characters, number of words
and number of spaces.

### 参数

`text`  
The text to measure.

### 返回值

Returns the total width of the text, number of characters, number of
words and number of spaces in the given text.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getUnicodeWidth
=========================

Get the width of the character in the font

### 说明

<span class="type">int</span> <span
class="methodname">HaruFont::getUnicodeWidth</span> ( <span
class="methodparam"><span class="type">int</span> `$character`</span> )

Get the width of the character in the font.

### 参数

`character`  
The code of the character.

### 返回值

Returns the width of the character in the font.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::getXHeight
====================

Get the distance from the baseline of lowercase letters

### 说明

<span class="type">int</span> <span
class="methodname">HaruFont::getXHeight</span> ( <span
class="methodparam">void</span> )

Gets the distance from the baseline of lowercase letters.

### 参数

此函数没有参数。

### 返回值

Returns the distance from the baseline of lowercase letters.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruFont::measureText
=====================

Calculate the number of characters which can be included within the
specified width

### 说明

<span class="type">int</span> <span
class="methodname">HaruFont::measureText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$font_size`</span> , <span
class="methodparam"><span class="type">float</span> `$char_space`</span>
, <span class="methodparam"><span class="type">float</span>
`$word_space`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$word_wrap`<span class="initializer"> =
**`FALSE`**</span></span> \] )

Calculate the number of characters which can be included within the
specified width.

### 参数

`text`  
The text to fit the width.

`width`  
The width of the area to put the text to.

`font_size`  
The size of the font.

`char_space`  
The character spacing.

`word_space`  
The word spacing.

`word_wrap`  
When this parameter is set to **`TRUE`** the function "emulates" word
wrapping and doesn't include the part of the current word if reached the
end of the area.

### 返回值

Returns the number of characters which can be included within the
specified width.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

简介
----

Haru PDF Image Class.

类摘要
------

**HaruImage**

<span class="ooclass"> class **HaruImage** </span> {

/\* 方法 \*/

<span class="type">int</span> <span
class="methodname">getBitsPerComponent</span> ( <span
class="methodparam">void</span> )

<span class="type">string</span> <span
class="methodname">getColorSpace</span> ( <span
class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">getHeight</span>
( <span class="methodparam">void</span> )

<span class="type">array</span> <span class="methodname">getSize</span>
( <span class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">getWidth</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">setColorMask</span> ( <span class="methodparam"><span
class="type">int</span> `$rmin`</span> , <span class="methodparam"><span
class="type">int</span> `$rmax`</span> , <span class="methodparam"><span
class="type">int</span> `$gmin`</span> , <span class="methodparam"><span
class="type">int</span> `$gmax`</span> , <span class="methodparam"><span
class="type">int</span> `$bmin`</span> , <span class="methodparam"><span
class="type">int</span> `$bmax`</span> )

<span class="type">bool</span> <span
class="methodname">setMaskImage</span> ( <span class="methodparam"><span
class="type">object</span> `$mask_image`</span> )

}

HaruImage::getBitsPerComponent
==============================

Get the number of bits used to describe each color component of the
image

### 说明

<span class="type">int</span> <span
class="methodname">HaruImage::getBitsPerComponent</span> ( <span
class="methodparam">void</span> )

Gets the number of bits used to describe each color component of the
image.

### 参数

此函数没有参数。

### 返回值

Returns the number of bits used to describe each color component of the
image.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruImage::getColorSpace
========================

Get the name of the color space

### 说明

<span class="type">string</span> <span
class="methodname">HaruImage::getColorSpace</span> ( <span
class="methodparam">void</span> )

Get the name of the color space.

### 参数

此函数没有参数。

### 返回值

Returns the name of the color space of the image. The name is one of the
following values:

-   "DeviceGray"
-   "DeviceRGB"
-   "DeviceCMYK"
-   "Indexed"

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruImage::getHeight
====================

Get the height of the image

### 说明

<span class="type">int</span> <span
class="methodname">HaruImage::getHeight</span> ( <span
class="methodparam">void</span> )

Get the height of the image.

### 参数

此函数没有参数。

### 返回值

Returns the height of the image.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruImage::getSize
==================

Get size of the image

### 说明

<span class="type">array</span> <span
class="methodname">HaruImage::getSize</span> ( <span
class="methodparam">void</span> )

Get the size of the image.

### 参数

此函数没有参数。

### 返回值

Returns an array with two elements: width and height, which contain
appropriate dimensions of the image.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruImage::getWidth
===================

Get the width of the image

### 说明

<span class="type">int</span> <span
class="methodname">HaruImage::getWidth</span> ( <span
class="methodparam">void</span> )

Get the width of the image.

### 参数

此函数没有参数。

### 返回值

Returns the width of the image.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruImage::setColorMask
=======================

Set the color mask of the image

### 说明

<span class="type">bool</span> <span
class="methodname">HaruImage::setColorMask</span> ( <span
class="methodparam"><span class="type">int</span> `$rmin`</span> , <span
class="methodparam"><span class="type">int</span> `$rmax`</span> , <span
class="methodparam"><span class="type">int</span> `$gmin`</span> , <span
class="methodparam"><span class="type">int</span> `$gmax`</span> , <span
class="methodparam"><span class="type">int</span> `$bmin`</span> , <span
class="methodparam"><span class="type">int</span> `$bmax`</span> )

Defines the transparent color of the image using the RGB range values.
The color within the range is displayed as a transparent color. The
color space of the image must be RGB.

### 参数

`rmin`  
The lower limit of red. Must be between 0 and 255.

`rmax`  
The upper limit of red. Must be between 0 and 255.

`gmin`  
The lower limit of green. Must be between 0 and 255.

`gmax`  
The upper limit of green. Must be between 0 and 255.

`bmin`  
The lower limit of blue. Must be between 0 and 255.

`bmax`  
The upper limit of blue. Must be between 0 and 255.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruImage::setMaskImage
=======================

Set the image mask

### 说明

<span class="type">bool</span> <span
class="methodname">HaruImage::setMaskImage</span> ( <span
class="methodparam"><span class="type">object</span>
`$mask_image`</span> )

Sets the image used as image-mask. It must be 1bit gray-scale color
image.

### 参数

`mask_image`  
A valid <span class="classname">HaruImage</span> instance.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

简介
----

Haru PDF Encoder Class.

类摘要
------

**HaruEncoder**

<span class="ooclass"> class **HaruEncoder** </span> {

/\* 方法 \*/

<span class="type">int</span> <span
class="methodname">getByteType</span> ( <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">int</span> `$index`</span> )

<span class="type">int</span> <span class="methodname">getType</span> (
<span class="methodparam">void</span> )

<span class="type">int</span> <span class="methodname">getUnicode</span>
( <span class="methodparam"><span class="type">int</span>
`$character`</span> )

<span class="type">int</span> <span
class="methodname">getWritingMode</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

| Type | Name                             | Description |
|------|----------------------------------|-------------|
| int  | HaruEncoder::TYPE\_SINGLE\_BYTE  |             |
| int  | HaruEncoder::TYPE\_DOUBLE\_BYTE  |             |
| int  | HaruEncoder::TYPE\_UNINITIALIZED |             |
| int  | HaruEncoder::UNKNOWN             |             |
| int  | HaruEncoder::WMODE\_HORIZONTAL   |             |
| int  | HaruEncoder::WMODE\_VERTICAL     |             |
| int  | HaruEncoder::BYTE\_TYPE\_SINGLE  |             |
| int  | HaruEncoder::BYTE\_TYPE\_LEAD    |             |
| int  | HaruEncoder::BYTE\_TYPE\_TRAIL   |             |
| int  | HaruEncoder::BYTE\_TYPE\_UNKNOWN |             |

HaruEncoder::getByteType
========================

Get the type of the byte in the text

### 说明

<span class="type">int</span> <span
class="methodname">HaruEncoder::getByteType</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

Get the type of the byte in the text.

### 参数

`text`  
The text.

`index`  
The position in the text.

### 返回值

Returns the type of the byte in the text on the specified position. The
result is one of the following values:

-   **`HaruEncoder::BYTE_TYPE_SINGLE`** - single byte character.
-   **`HaruEncoder::BYTE_TYPE_LEAD`** - lead byte of a double-byte
    character.
-   **`HaruEncoder::BYTE_TYPE_TRAIL`** - trailing byte of a double-byte
    character.
-   **`HaruEncoder::BYTE_TYPE_UNKNOWN`** - invalid encoder or cannot
    detect the byte type.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruEncoder::getType
====================

Get the type of the encoder

### 说明

<span class="type">int</span> <span
class="methodname">HaruEncoder::getType</span> ( <span
class="methodparam">void</span> )

Get the type of the encoder.

### 参数

此函数没有参数。

### 返回值

Returns the type of the encoder. The result is one of the following
values:

-   **`HaruEncoder::TYPE_SINGLE_BYTE`** - the encoder is for single byte
    characters.
-   **`HaruEncoder::TYPE_DOUBLE_BYTE`** - the encoder is for multibyte
    characters.
-   **`HaruEncoder::TYPE_UNINITIALIZED`** - the encoder is not
    initialized.
-   **`HaruEncoder::UNKNOWN`** - the encoder is invalid.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruEncoder::getUnicode
=======================

Convert the specified character to unicode

### 说明

<span class="type">int</span> <span
class="methodname">HaruEncoder::getUnicode</span> ( <span
class="methodparam"><span class="type">int</span> `$character`</span> )

Converts the specified character to unicode.

### 参数

`character`  
The character code to convert.

### 返回值

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruEncoder::getWritingMode
===========================

Get the writing mode of the encoder

### 说明

<span class="type">int</span> <span
class="methodname">HaruEncoder::getWritingMode</span> ( <span
class="methodparam">void</span> )

Get the writing mode of the encoder.

### 参数

此函数没有参数。

### 返回值

Returns the writing mode of the encoder. The result value is on of the
following:

-   **`HaruEncoder::WMODE_HORIZONTAL`** - horizontal writing mode.
-   **`HaruEncoder::WMODE_VERTICAL`** - vertical writing mode.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

简介
----

Haru PDF Outline Class.

类摘要
------

**HaruOutline**

<span class="ooclass"> class **HaruOutline** </span> {

/\* 方法 \*/

<span class="type">bool</span> <span
class="methodname">setDestination</span> ( <span
class="methodparam"><span class="type">object</span>
`$destination`</span> )

<span class="type">bool</span> <span class="methodname">setOpened</span>
( <span class="methodparam"><span class="type">bool</span>
`$opened`</span> )

}

HaruOutline::setDestination
===========================

Set the destination for the outline

### 说明

<span class="type">bool</span> <span
class="methodname">HaruOutline::setDestination</span> ( <span
class="methodparam"><span class="type">object</span>
`$destination`</span> )

Sets a destination object which becomes a target to jump to when the
outline is clicked.

### 参数

`destination`  
A valid <span class="classname">HaruDestination</span> instance.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruOutline::setOpened
======================

Set the initial state of the outline

### 说明

<span class="type">bool</span> <span
class="methodname">HaruOutline::setOpened</span> ( <span
class="methodparam"><span class="type">bool</span> `$opened`</span> )

Defines whether this node is opened or not when the outline is displayed
for the first time.

### 参数

`opened`  
**`TRUE`** means open, **`FALSE`** - closed.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

简介
----

Haru PDF Annotation Class.

类摘要
------

**HaruAnnotation**

<span class="ooclass"> class **HaruAnnotation** </span> {

/\* 方法 \*/

<span class="type">bool</span> <span
class="methodname">setBorderStyle</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span>
`$dash_on`</span> , <span class="methodparam"><span
class="type">int</span> `$dash_off`</span> )

<span class="type">bool</span> <span
class="methodname">setHighlightMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="type">bool</span> <span class="methodname">setIcon</span> (
<span class="methodparam"><span class="type">int</span> `$icon`</span> )

<span class="type">bool</span> <span class="methodname">setOpened</span>
( <span class="methodparam"><span class="type">bool</span>
`$opened`</span> )

}

预定义常量
----------

| Type | Name                                 | Description |
|------|--------------------------------------|-------------|
| int  | HaruAnnotation::NO\_HIGHLIGHT        |             |
| int  | HaruAnnotation::INVERT\_BOX          |             |
| int  | HaruAnnotation::INVERT\_BORDER       |             |
| int  | HaruAnnotation::DOWN\_APPEARANCE     |             |
| int  | HaruAnnotation::ICON\_COMMENT        |             |
| int  | HaruAnnotation::ICON\_KEY            |             |
| int  | HaruAnnotation::ICON\_NOTE           |             |
| int  | HaruAnnotation::ICON\_HELP           |             |
| int  | HaruAnnotation::ICON\_NEW\_PARAGRAPH |             |
| int  | HaruAnnotation::ICON\_PARAGRAPH      |             |
| int  | HaruAnnotation::ICON\_INSERT         |             |

HaruAnnotation::setBorderStyle
==============================

Set the border style of the annotation

### 说明

<span class="type">bool</span> <span
class="methodname">HaruAnnotation::setBorderStyle</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span>
`$dash_on`</span> , <span class="methodparam"><span
class="type">int</span> `$dash_off`</span> )

Defines the style of the border of the annotation. This function may be
used with link annotations only.

### 参数

`width`  
The width of the border line.

`dash_on`  
The dash style.

`dash_off`  
The dash style.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruAnnotation::setHighlightMode
================================

Set the highlighting mode of the annotation

### 说明

<span class="type">bool</span> <span
class="methodname">HaruAnnotation::setHighlightMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

Defines the appearance of the annotation when clicked. This function may
be used with link annotations only.

### 参数

`mode`  
The highlighting mode of the annotation. Can take only these values:

-   **`HaruAnnotation::NO_HIGHLIGHT`** - no highlighting.
-   **`HaruAnnotation::INVERT_BOX`** - invert the contents of the
    annotation.
-   **`HaruAnnotation::INVERT_BORDER`** - invert the border of the
    annotation.
-   **`HaruAnnotation::DOWN_APPEARANCE`** - dent the annotation.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruAnnotation::setIcon
=======================

Set the icon style of the annotation

### 说明

<span class="type">bool</span> <span
class="methodname">HaruAnnotation::setIcon</span> ( <span
class="methodparam"><span class="type">int</span> `$icon`</span> )

Defines the style of the annotation icon. This function may be used with
text annotations only.

### 参数

`icon`  
The style of the icon. Can take only these values:

-   **`HaruAnnotation::ICON_COMMENT`**
-   **`HaruAnnotation::ICON_KEY`**
-   **`HaruAnnotation::ICON_NOTE`**
-   **`HaruAnnotation::ICON_HELP`**
-   **`HaruAnnotation::ICON_NEW_PARAGRAPH`**
-   **`HaruAnnotation::ICON_PARAGRAPH`**
-   **`HaruAnnotation::ICON_INSERT`**

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruAnnotation::setOpened
=========================

Set the initial state of the annotation

### 说明

<span class="type">bool</span> <span
class="methodname">HaruAnnotation::setOpened</span> ( <span
class="methodparam"><span class="type">bool</span> `$opened`</span> )

Defines whether the annotation is initially displayed open. This
function may be used with text annotations only.

### 参数

`opened`  
**`TRUE`** means the annotation is initially displayed open, **`FALSE`**
- means it's closed.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

简介
----

Haru PDF Destination Class.

类摘要
------

**HaruDestination**

<span class="ooclass"> class **HaruDestination** </span> {

/\* 方法 \*/

<span class="type">bool</span> <span class="methodname">setFit</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">setFitB</span> (
<span class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">setFitBH</span>
( <span class="methodparam"><span class="type">float</span>
`$top`</span> )

<span class="type">bool</span> <span class="methodname">setFitBV</span>
( <span class="methodparam"><span class="type">float</span>
`$left`</span> )

<span class="type">bool</span> <span class="methodname">setFitH</span> (
<span class="methodparam"><span class="type">float</span> `$top`</span>
)

<span class="type">bool</span> <span class="methodname">setFitR</span> (
<span class="methodparam"><span class="type">float</span> `$left`</span>
, <span class="methodparam"><span class="type">float</span>
`$bottom`</span> , <span class="methodparam"><span
class="type">float</span> `$right`</span> , <span
class="methodparam"><span class="type">float</span> `$top`</span> )

<span class="type">bool</span> <span class="methodname">setFitV</span> (
<span class="methodparam"><span class="type">float</span> `$left`</span>
)

<span class="type">bool</span> <span class="methodname">setXYZ</span> (
<span class="methodparam"><span class="type">float</span> `$left`</span>
, <span class="methodparam"><span class="type">float</span>
`$top`</span> , <span class="methodparam"><span
class="type">float</span> `$zoom`</span> )

}

HaruDestination::setFit
=======================

Set the appearance of the page to fit the window

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFit</span> ( <span
class="methodparam">void</span> )

Defines the appearance of the page to fit the window.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setFitB
========================

Set the appearance of the page to fit the bounding box of the page
within the window

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFitB</span> ( <span
class="methodparam">void</span> )

Defines the appearance of the page to fit the bounding box of the page
within the window.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setFitBH
=========================

Set the appearance of the page to fit the width of the bounding box

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFitBH</span> ( <span
class="methodparam"><span class="type">float</span> `$top`</span> )

Defines the appearance of the page to magnifying to fit the width of the
bounding box and setting the top position of the page to the value of
`top`.

### 参数

`top`  
The top coordinates of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setFitBV
=========================

Set the appearance of the page to fit the height of the boudning box

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFitBV</span> ( <span
class="methodparam"><span class="type">float</span> `$left`</span> )

Defines the appearance of the page to magnifying to fit the height of
the bounding box and setting the left position of the page to the value
of `left`.

### 参数

`left`  
The left coordinates of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setFitH
========================

Set the appearance of the page to fit the window width

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFitH</span> ( <span
class="methodparam"><span class="type">float</span> `$top`</span> )

Defines the appearance of the page to fit the window width and sets the
top position of the page to the value of `top`.

### 参数

`top`  
The top position of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setFitR
========================

Set the appearance of the page to fit the specified rectangle

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFitR</span> ( <span
class="methodparam"><span class="type">float</span> `$left`</span> ,
<span class="methodparam"><span class="type">float</span>
`$bottom`</span> , <span class="methodparam"><span
class="type">float</span> `$right`</span> , <span
class="methodparam"><span class="type">float</span> `$top`</span> )

Defines the appearance of the page to fit the rectangle by the
parameters.

### 参数

`left`  
The left coordinates of the page.

`bottom`  
The bottom coordinates of the page.

`right`  
The right coordinates of the page.

`top`  
The top coordinates of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setFitV
========================

Set the appearance of the page to fit the window height

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setFitV</span> ( <span
class="methodparam"><span class="type">float</span> `$left`</span> )

Defines the appearance of the page to fit the window height.

### 参数

`left`  
The left position of the page.

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。

HaruDestination::setXYZ
=======================

Set the appearance of the page

### 说明

<span class="type">bool</span> <span
class="methodname">HaruDestination::setXYZ</span> ( <span
class="methodparam"><span class="type">float</span> `$left`</span> ,
<span class="methodparam"><span class="type">float</span> `$top`</span>
, <span class="methodparam"><span class="type">float</span>
`$zoom`</span> )

Defines the appearance of the page using three parameters: `left`, `top`
and `zoom`.

### 参数

`left`  
The left position of the page.

`top`  
The top position of the page.

`zoom`  
The magnification factor. The value must be between 0.08 (8%) and 32
(3200%).

### 返回值

Returns **`TRUE`** on success.

### 错误／异常

发生错误时抛出 <span class="classname">HaruException</span> 异常。
