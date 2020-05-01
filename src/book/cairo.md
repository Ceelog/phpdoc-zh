Cairo
=====

**目录**

-   [简介](/intro/cairo.html)
-   [安装／配置](/cairo/setup.html)
    -   [需求](/cairo/setup.html#需求)
    -   [安装](/cairo/setup.html#安装)
    -   [运行时配置](/cairo/setup.html#运行时配置)
    -   [资源类型](/cairo/setup.html#资源类型)
-   [预定义常量](/cairo/constants.html)
-   [范例](/cairo/examples.html)
-   [Cairo 函数](/ref/cairo.html)
    -   [cairo\_create](/ref/cairo.html#cairo_create) — Returns a new
        CairoContext object on the requested surface
    -   [cairo\_font\_options\_create](/ref/cairo.html#cairo_font_options_create)
        — Description
    -   [cairo\_font\_options\_equal](/ref/cairo.html#cairo_font_options_equal)
        — Description
    -   [cairo\_font\_options\_get\_antialias](/ref/cairo.html#cairo_font_options_get_antialias)
        — Description
    -   [cairo\_font\_options\_get\_hint\_metrics](/ref/cairo.html#cairo_font_options_get_hint_metrics)
        — Description
    -   [cairo\_font\_options\_get\_hint\_style](/ref/cairo.html#cairo_font_options_get_hint_style)
        — Description
    -   [cairo\_font\_options\_get\_subpixel\_order](/ref/cairo.html#cairo_font_options_get_subpixel_order)
        — Description
    -   [cairo\_font\_options\_hash](/ref/cairo.html#cairo_font_options_hash)
        — Description
    -   [cairo\_font\_options\_merge](/ref/cairo.html#cairo_font_options_merge)
        — Description
    -   [cairo\_font\_options\_set\_antialias](/ref/cairo.html#cairo_font_options_set_antialias)
        — Description
    -   [cairo\_font\_options\_set\_hint\_metrics](/ref/cairo.html#cairo_font_options_set_hint_metrics)
        — Description
    -   [cairo\_font\_options\_set\_hint\_style](/ref/cairo.html#cairo_font_options_set_hint_style)
        — Description
    -   [cairo\_font\_options\_set\_subpixel\_order](/ref/cairo.html#cairo_font_options_set_subpixel_order)
        — Description
    -   [cairo\_font\_options\_status](/ref/cairo.html#cairo_font_options_status)
        — Description
    -   [cairo\_format\_stride\_for\_width](/ref/cairo.html#cairo_format_stride_for_width)
        — Description
    -   [cairo\_image\_surface\_create\_for\_data](/ref/cairo.html#cairo_image_surface_create_for_data)
        — Description
    -   [cairo\_image\_surface\_create\_from\_png](/ref/cairo.html#cairo_image_surface_create_from_png)
        — Description
    -   [cairo\_image\_surface\_create](/ref/cairo.html#cairo_image_surface_create)
        — Description
    -   [cairo\_image\_surface\_get\_data](/ref/cairo.html#cairo_image_surface_get_data)
        — Description
    -   [cairo\_image\_surface\_get\_format](/ref/cairo.html#cairo_image_surface_get_format)
        — Description
    -   [cairo\_image\_surface\_get\_height](/ref/cairo.html#cairo_image_surface_get_height)
        — Description
    -   [cairo\_image\_surface\_get\_stride](/ref/cairo.html#cairo_image_surface_get_stride)
        — Description
    -   [cairo\_image\_surface\_get\_width](/ref/cairo.html#cairo_image_surface_get_width)
        — Description
    -   [cairo\_matrix\_create\_scale](/ref/cairo.html#cairo_matrix_create_scale)
        — 别名 CairoMatrix::initScale
    -   [cairo\_matrix\_create\_translate](/ref/cairo.html#cairo_matrix_create_translate)
        — 别名 CairoMatrix::initTranslate
    -   [cairo\_matrix\_invert](/ref/cairo.html#cairo_matrix_invert) —
        Description
    -   [cairo\_matrix\_multiply](/ref/cairo.html#cairo_matrix_multiply)
        — Description
    -   [cairo\_matrix\_transform\_distance](/ref/cairo.html#cairo_matrix_transform_distance)
        — Description
    -   [cairo\_matrix\_transform\_point](/ref/cairo.html#cairo_matrix_transform_point)
        — Description
    -   [cairo\_matrix\_translate](/ref/cairo.html#cairo_matrix_translate)
        — Description
    -   [cairo\_pattern\_add\_color\_stop\_rgb](/ref/cairo.html#cairo_pattern_add_color_stop_rgb)
        — Description
    -   [cairo\_pattern\_add\_color\_stop\_rgba](/ref/cairo.html#cairo_pattern_add_color_stop_rgba)
        — Description
    -   [cairo\_pattern\_create\_for\_surface](/ref/cairo.html#cairo_pattern_create_for_surface)
        — Description
    -   [cairo\_pattern\_create\_linear](/ref/cairo.html#cairo_pattern_create_linear)
        — Description
    -   [cairo\_pattern\_create\_radial](/ref/cairo.html#cairo_pattern_create_radial)
        — Description
    -   [cairo\_pattern\_create\_rgb](/ref/cairo.html#cairo_pattern_create_rgb)
        — Description
    -   [cairo\_pattern\_create\_rgba](/ref/cairo.html#cairo_pattern_create_rgba)
        — Description
    -   [cairo\_pattern\_get\_color\_stop\_count](/ref/cairo.html#cairo_pattern_get_color_stop_count)
        — Description
    -   [cairo\_pattern\_get\_color\_stop\_rgba](/ref/cairo.html#cairo_pattern_get_color_stop_rgba)
        — Description
    -   [cairo\_pattern\_get\_extend](/ref/cairo.html#cairo_pattern_get_extend)
        — Description
    -   [cairo\_pattern\_get\_filter](/ref/cairo.html#cairo_pattern_get_filter)
        — Description
    -   [cairo\_pattern\_get\_linear\_points](/ref/cairo.html#cairo_pattern_get_linear_points)
        — Description
    -   [cairo\_pattern\_get\_matrix](/ref/cairo.html#cairo_pattern_get_matrix)
        — Description
    -   [cairo\_pattern\_get\_radial\_circles](/ref/cairo.html#cairo_pattern_get_radial_circles)
        — Description
    -   [cairo\_pattern\_get\_rgba](/ref/cairo.html#cairo_pattern_get_rgba)
        — Description
    -   [cairo\_pattern\_get\_surface](/ref/cairo.html#cairo_pattern_get_surface)
        — Description
    -   [cairo\_pattern\_get\_type](/ref/cairo.html#cairo_pattern_get_type)
        — Description
    -   [cairo\_pattern\_set\_extend](/ref/cairo.html#cairo_pattern_set_extend)
        — Description
    -   [cairo\_pattern\_set\_filter](/ref/cairo.html#cairo_pattern_set_filter)
        — Description
    -   [cairo\_pattern\_set\_matrix](/ref/cairo.html#cairo_pattern_set_matrix)
        — Description
    -   [cairo\_pattern\_status](/ref/cairo.html#cairo_pattern_status) —
        Description
    -   [cairo\_pdf\_surface\_create](/ref/cairo.html#cairo_pdf_surface_create)
        — Description
    -   [cairo\_pdf\_surface\_set\_size](/ref/cairo.html#cairo_pdf_surface_set_size)
        — Description
    -   [cairo\_ps\_get\_levels](/ref/cairo.html#cairo_ps_get_levels) —
        Description
    -   [cairo\_ps\_level\_to\_string](/ref/cairo.html#cairo_ps_level_to_string)
        — Description
    -   [cairo\_ps\_surface\_create](/ref/cairo.html#cairo_ps_surface_create)
        — Description
    -   [cairo\_ps\_surface\_dsc\_begin\_page\_setup](/ref/cairo.html#cairo_ps_surface_dsc_begin_page_setup)
        — Description
    -   [cairo\_ps\_surface\_dsc\_begin\_setup](/ref/cairo.html#cairo_ps_surface_dsc_begin_setup)
        — Description
    -   [cairo\_ps\_surface\_dsc\_comment](/ref/cairo.html#cairo_ps_surface_dsc_comment)
        — Description
    -   [cairo\_ps\_surface\_get\_eps](/ref/cairo.html#cairo_ps_surface_get_eps)
        — Description
    -   [cairo\_ps\_surface\_restrict\_to\_level](/ref/cairo.html#cairo_ps_surface_restrict_to_level)
        — Description
    -   [cairo\_ps\_surface\_set\_eps](/ref/cairo.html#cairo_ps_surface_set_eps)
        — Description
    -   [cairo\_ps\_surface\_set\_size](/ref/cairo.html#cairo_ps_surface_set_size)
        — Description
    -   [cairo\_scaled\_font\_create](/ref/cairo.html#cairo_scaled_font_create)
        — Description
    -   [cairo\_scaled\_font\_extents](/ref/cairo.html#cairo_scaled_font_extents)
        — Description
    -   [cairo\_scaled\_font\_get\_ctm](/ref/cairo.html#cairo_scaled_font_get_ctm)
        — Description
    -   [cairo\_scaled\_font\_get\_font\_face](/ref/cairo.html#cairo_scaled_font_get_font_face)
        — Description
    -   [cairo\_scaled\_font\_get\_font\_matrix](/ref/cairo.html#cairo_scaled_font_get_font_matrix)
        — Description
    -   [cairo\_scaled\_font\_get\_font\_options](/ref/cairo.html#cairo_scaled_font_get_font_options)
        — Description
    -   [cairo\_scaled\_font\_get\_scale\_matrix](/ref/cairo.html#cairo_scaled_font_get_scale_matrix)
        — Description
    -   [cairo\_scaled\_font\_get\_type](/ref/cairo.html#cairo_scaled_font_get_type)
        — Description
    -   [cairo\_scaled\_font\_glyph\_extents](/ref/cairo.html#cairo_scaled_font_glyph_extents)
        — Description
    -   [cairo\_scaled\_font\_status](/ref/cairo.html#cairo_scaled_font_status)
        — Description
    -   [cairo\_scaled\_font\_text\_extents](/ref/cairo.html#cairo_scaled_font_text_extents)
        — Description
    -   [cairo\_surface\_copy\_page](/ref/cairo.html#cairo_surface_copy_page)
        — Description
    -   [cairo\_surface\_create\_similar](/ref/cairo.html#cairo_surface_create_similar)
        — Description
    -   [cairo\_surface\_finish](/ref/cairo.html#cairo_surface_finish) —
        Description
    -   [cairo\_surface\_flush](/ref/cairo.html#cairo_surface_flush) —
        Description
    -   [cairo\_surface\_get\_content](/ref/cairo.html#cairo_surface_get_content)
        — Description
    -   [cairo\_surface\_get\_device\_offset](/ref/cairo.html#cairo_surface_get_device_offset)
        — Description
    -   [cairo\_surface\_get\_font\_options](/ref/cairo.html#cairo_surface_get_font_options)
        — Description
    -   [cairo\_surface\_get\_type](/ref/cairo.html#cairo_surface_get_type)
        — Description
    -   [cairo\_surface\_mark\_dirty\_rectangle](/ref/cairo.html#cairo_surface_mark_dirty_rectangle)
        — Description
    -   [cairo\_surface\_mark\_dirty](/ref/cairo.html#cairo_surface_mark_dirty)
        — Description
    -   [cairo\_surface\_set\_device\_offset](/ref/cairo.html#cairo_surface_set_device_offset)
        — Description
    -   [cairo\_surface\_set\_fallback\_resolution](/ref/cairo.html#cairo_surface_set_fallback_resolution)
        — Description
    -   [cairo\_surface\_show\_page](/ref/cairo.html#cairo_surface_show_page)
        — Description
    -   [cairo\_surface\_status](/ref/cairo.html#cairo_surface_status) —
        Description
    -   [cairo\_surface\_write\_to\_png](/ref/cairo.html#cairo_surface_write_to_png)
        — Description
    -   [cairo\_svg\_surface\_create](/ref/cairo.html#cairo_svg_surface_create)
        — Description
    -   [cairo\_svg\_surface\_restrict\_to\_version](/ref/cairo.html#cairo_svg_surface_restrict_to_version)
        — Description
    -   [cairo\_svg\_version\_to\_string](/ref/cairo.html#cairo_svg_version_to_string)
        — Description
-   [Cairo](/class/cairo.html) — The Cairo class
    -   [Cairo::availableFonts](/class/cairo.html#Cairo::availableFonts)
        — Retrieves the availables font types
    -   [Cairo::availableSurfaces](/class/cairo.html#Cairo::availableSurfaces)
        — Retrieves all available surfaces
    -   [Cairo::statusToString](/class/cairo.html#Cairo::statusToString)
        — Retrieves the current status as string
    -   [Cairo::version](/class/cairo.html#Cairo::version) — Retrieves
        cairo's library version
    -   [Cairo::versionString](/class/cairo.html#Cairo::versionString) —
        Retrieves cairo version as string
-   [CairoContext](/class/cairocontext.html) — The CairoContext class
    -   [CairoContext::appendPath](/class/cairocontext.html#CairoContext::appendPath)
        — Appends a path to current path
    -   [CairoContext::arc](/class/cairocontext.html#CairoContext::arc)
        — Adds a circular arc
    -   [CairoContext::arcNegative](/class/cairocontext.html#CairoContext::arcNegative)
        — Adds a negative arc
    -   [CairoContext::clip](/class/cairocontext.html#CairoContext::clip)
        — Establishes a new clip region
    -   [CairoContext::clipExtents](/class/cairocontext.html#CairoContext::clipExtents)
        — Computes the area inside the current clip
    -   [CairoContext::clipPreserve](/class/cairocontext.html#CairoContext::clipPreserve)
        — Establishes a new clip region from the current clip
    -   [CairoContext::clipRectangleList](/class/cairocontext.html#CairoContext::clipRectangleList)
        — Retrieves the current clip as a list of rectangles
    -   [CairoContext::closePath](/class/cairocontext.html#CairoContext::closePath)
        — Closes the current path
    -   [CairoContext::\_\_construct](/class/cairocontext.html#CairoContext::__construct)
        — Creates a new CairoContext
    -   [CairoContext::copyPage](/class/cairocontext.html#CairoContext::copyPage)
        — Emits the current page
    -   [CairoContext::copyPath](/class/cairocontext.html#CairoContext::copyPath)
        — Creates a copy of the current path
    -   [CairoContext::copyPathFlat](/class/cairocontext.html#CairoContext::copyPathFlat)
        — Gets a flattened copy of the current path
    -   [CairoContext::curveTo](/class/cairocontext.html#CairoContext::curveTo)
        — Adds a curve
    -   [CairoContext::deviceToUser](/class/cairocontext.html#CairoContext::deviceToUser)
        — Transform a coordinate
    -   [CairoContext::deviceToUserDistance](/class/cairocontext.html#CairoContext::deviceToUserDistance)
        — Transform a distance
    -   [CairoContext::fill](/class/cairocontext.html#CairoContext::fill)
        — Fills the current path
    -   [CairoContext::fillExtents](/class/cairocontext.html#CairoContext::fillExtents)
        — Computes the filled area
    -   [CairoContext::fillPreserve](/class/cairocontext.html#CairoContext::fillPreserve)
        — Fills and preserve the current path
    -   [CairoContext::fontExtents](/class/cairocontext.html#CairoContext::fontExtents)
        — Get the font extents
    -   [CairoContext::getAntialias](/class/cairocontext.html#CairoContext::getAntialias)
        — Retrieves the current antialias mode
    -   [CairoContext::getCurrentPoint](/class/cairocontext.html#CairoContext::getCurrentPoint)
        — The getCurrentPoint purpose
    -   [CairoContext::getDash](/class/cairocontext.html#CairoContext::getDash)
        — The getDash purpose
    -   [CairoContext::getDashCount](/class/cairocontext.html#CairoContext::getDashCount)
        — The getDashCount purpose
    -   [CairoContext::getFillRule](/class/cairocontext.html#CairoContext::getFillRule)
        — The getFillRule purpose
    -   [CairoContext::getFontFace](/class/cairocontext.html#CairoContext::getFontFace)
        — The getFontFace purpose
    -   [CairoContext::getFontMatrix](/class/cairocontext.html#CairoContext::getFontMatrix)
        — The getFontMatrix purpose
    -   [CairoContext::getFontOptions](/class/cairocontext.html#CairoContext::getFontOptions)
        — The getFontOptions purpose
    -   [CairoContext::getGroupTarget](/class/cairocontext.html#CairoContext::getGroupTarget)
        — The getGroupTarget purpose
    -   [CairoContext::getLineCap](/class/cairocontext.html#CairoContext::getLineCap)
        — The getLineCap purpose
    -   [CairoContext::getLineJoin](/class/cairocontext.html#CairoContext::getLineJoin)
        — The getLineJoin purpose
    -   [CairoContext::getLineWidth](/class/cairocontext.html#CairoContext::getLineWidth)
        — The getLineWidth purpose
    -   [CairoContext::getMatrix](/class/cairocontext.html#CairoContext::getMatrix)
        — The getMatrix purpose
    -   [CairoContext::getMiterLimit](/class/cairocontext.html#CairoContext::getMiterLimit)
        — The getMiterLimit purpose
    -   [CairoContext::getOperator](/class/cairocontext.html#CairoContext::getOperator)
        — The getOperator purpose
    -   [CairoContext::getScaledFont](/class/cairocontext.html#CairoContext::getScaledFont)
        — The getScaledFont purpose
    -   [CairoContext::getSource](/class/cairocontext.html#CairoContext::getSource)
        — The getSource purpose
    -   [CairoContext::getTarget](/class/cairocontext.html#CairoContext::getTarget)
        — The getTarget purpose
    -   [CairoContext::getTolerance](/class/cairocontext.html#CairoContext::getTolerance)
        — The getTolerance purpose
    -   [CairoContext::glyphPath](/class/cairocontext.html#CairoContext::glyphPath)
        — The glyphPath purpose
    -   [CairoContext::hasCurrentPoint](/class/cairocontext.html#CairoContext::hasCurrentPoint)
        — The hasCurrentPoint purpose
    -   [CairoContext::identityMatrix](/class/cairocontext.html#CairoContext::identityMatrix)
        — The identityMatrix purpose
    -   [CairoContext::inFill](/class/cairocontext.html#CairoContext::inFill)
        — The inFill purpose
    -   [CairoContext::inStroke](/class/cairocontext.html#CairoContext::inStroke)
        — The inStroke purpose
    -   [CairoContext::lineTo](/class/cairocontext.html#CairoContext::lineTo)
        — The lineTo purpose
    -   [CairoContext::mask](/class/cairocontext.html#CairoContext::mask)
        — The mask purpose
    -   [CairoContext::maskSurface](/class/cairocontext.html#CairoContext::maskSurface)
        — The maskSurface purpose
    -   [CairoContext::moveTo](/class/cairocontext.html#CairoContext::moveTo)
        — The moveTo purpose
    -   [CairoContext::newPath](/class/cairocontext.html#CairoContext::newPath)
        — The newPath purpose
    -   [CairoContext::newSubPath](/class/cairocontext.html#CairoContext::newSubPath)
        — The newSubPath purpose
    -   [CairoContext::paint](/class/cairocontext.html#CairoContext::paint)
        — The paint purpose
    -   [CairoContext::paintWithAlpha](/class/cairocontext.html#CairoContext::paintWithAlpha)
        — The paintWithAlpha purpose
    -   [CairoContext::pathExtents](/class/cairocontext.html#CairoContext::pathExtents)
        — The pathExtents purpose
    -   [CairoContext::popGroup](/class/cairocontext.html#CairoContext::popGroup)
        — The popGroup purpose
    -   [CairoContext::popGroupToSource](/class/cairocontext.html#CairoContext::popGroupToSource)
        — The popGroupToSource purpose
    -   [CairoContext::pushGroup](/class/cairocontext.html#CairoContext::pushGroup)
        — The pushGroup purpose
    -   [CairoContext::pushGroupWithContent](/class/cairocontext.html#CairoContext::pushGroupWithContent)
        — The pushGroupWithContent purpose
    -   [CairoContext::rectangle](/class/cairocontext.html#CairoContext::rectangle)
        — The rectangle purpose
    -   [CairoContext::relCurveTo](/class/cairocontext.html#CairoContext::relCurveTo)
        — The relCurveTo purpose
    -   [CairoContext::relLineTo](/class/cairocontext.html#CairoContext::relLineTo)
        — The relLineTo purpose
    -   [CairoContext::relMoveTo](/class/cairocontext.html#CairoContext::relMoveTo)
        — The relMoveTo purpose
    -   [CairoContext::resetClip](/class/cairocontext.html#CairoContext::resetClip)
        — The resetClip purpose
    -   [CairoContext::restore](/class/cairocontext.html#CairoContext::restore)
        — The restore purpose
    -   [CairoContext::rotate](/class/cairocontext.html#CairoContext::rotate)
        — The rotate purpose
    -   [CairoContext::save](/class/cairocontext.html#CairoContext::save)
        — The save purpose
    -   [CairoContext::scale](/class/cairocontext.html#CairoContext::scale)
        — The scale purpose
    -   [CairoContext::selectFontFace](/class/cairocontext.html#CairoContext::selectFontFace)
        — The selectFontFace purpose
    -   [CairoContext::setAntialias](/class/cairocontext.html#CairoContext::setAntialias)
        — The setAntialias purpose
    -   [CairoContext::setDash](/class/cairocontext.html#CairoContext::setDash)
        — The setDash purpose
    -   [CairoContext::setFillRule](/class/cairocontext.html#CairoContext::setFillRule)
        — The setFillRule purpose
    -   [CairoContext::setFontFace](/class/cairocontext.html#CairoContext::setFontFace)
        — The setFontFace purpose
    -   [CairoContext::setFontMatrix](/class/cairocontext.html#CairoContext::setFontMatrix)
        — The setFontMatrix purpose
    -   [CairoContext::setFontOptions](/class/cairocontext.html#CairoContext::setFontOptions)
        — The setFontOptions purpose
    -   [CairoContext::setFontSize](/class/cairocontext.html#CairoContext::setFontSize)
        — The setFontSize purpose
    -   [CairoContext::setLineCap](/class/cairocontext.html#CairoContext::setLineCap)
        — The setLineCap purpose
    -   [CairoContext::setLineJoin](/class/cairocontext.html#CairoContext::setLineJoin)
        — The setLineJoin purpose
    -   [CairoContext::setLineWidth](/class/cairocontext.html#CairoContext::setLineWidth)
        — The setLineWidth purpose
    -   [CairoContext::setMatrix](/class/cairocontext.html#CairoContext::setMatrix)
        — The setMatrix purpose
    -   [CairoContext::setMiterLimit](/class/cairocontext.html#CairoContext::setMiterLimit)
        — The setMiterLimit purpose
    -   [CairoContext::setOperator](/class/cairocontext.html#CairoContext::setOperator)
        — The setOperator purpose
    -   [CairoContext::setScaledFont](/class/cairocontext.html#CairoContext::setScaledFont)
        — The setScaledFont purpose
    -   [CairoContext::setSource](/class/cairocontext.html#CairoContext::setSource)
        — The setSource purpose
    -   [CairoContext::setSourceRGB](/class/cairocontext.html#CairoContext::setSourceRGB)
        — The setSourceRGB purpose
    -   [CairoContext::setSourceRGBA](/class/cairocontext.html#CairoContext::setSourceRGBA)
        — The setSourceRGBA purpose
    -   [CairoContext::setSourceSurface](/class/cairocontext.html#CairoContext::setSourceSurface)
        — The setSourceSurface purpose
    -   [CairoContext::setTolerance](/class/cairocontext.html#CairoContext::setTolerance)
        — The setTolerance purpose
    -   [CairoContext::showPage](/class/cairocontext.html#CairoContext::showPage)
        — The showPage purpose
    -   [CairoContext::showText](/class/cairocontext.html#CairoContext::showText)
        — The showText purpose
    -   [CairoContext::status](/class/cairocontext.html#CairoContext::status)
        — The status purpose
    -   [CairoContext::stroke](/class/cairocontext.html#CairoContext::stroke)
        — The stroke purpose
    -   [CairoContext::strokeExtents](/class/cairocontext.html#CairoContext::strokeExtents)
        — The strokeExtents purpose
    -   [CairoContext::strokePreserve](/class/cairocontext.html#CairoContext::strokePreserve)
        — The strokePreserve purpose
    -   [CairoContext::textExtents](/class/cairocontext.html#CairoContext::textExtents)
        — The textExtents purpose
    -   [CairoContext::textPath](/class/cairocontext.html#CairoContext::textPath)
        — The textPath purpose
    -   [CairoContext::transform](/class/cairocontext.html#CairoContext::transform)
        — The transform purpose
    -   [CairoContext::translate](/class/cairocontext.html#CairoContext::translate)
        — The translate purpose
    -   [CairoContext::userToDevice](/class/cairocontext.html#CairoContext::userToDevice)
        — The userToDevice purpose
    -   [CairoContext::userToDeviceDistance](/class/cairocontext.html#CairoContext::userToDeviceDistance)
        — The userToDeviceDistance purpose
-   [CairoException](/class/cairoexception.html) — The CairoException
    class
-   [CairoStatus](/class/cairostatus.html) — The CairoStatus class
-   [CairoSurface](/class/cairosurface.html) — The CairoSurface class
    -   [CairoSurface::\_\_construct](/class/cairosurface.html#CairoSurface::__construct)
        — The \_\_construct purpose
    -   [CairoSurface::copyPage](/class/cairosurface.html#CairoSurface::copyPage)
        — The copyPage purpose
    -   [CairoSurface::createSimilar](/class/cairosurface.html#CairoSurface::createSimilar)
        — The createSimilar purpose
    -   [CairoSurface::finish](/class/cairosurface.html#CairoSurface::finish)
        — The finish purpose
    -   [CairoSurface::flush](/class/cairosurface.html#CairoSurface::flush)
        — The flush purpose
    -   [CairoSurface::getContent](/class/cairosurface.html#CairoSurface::getContent)
        — The getContent purpose
    -   [CairoSurface::getDeviceOffset](/class/cairosurface.html#CairoSurface::getDeviceOffset)
        — The getDeviceOffset purpose
    -   [CairoSurface::getFontOptions](/class/cairosurface.html#CairoSurface::getFontOptions)
        — The getFontOptions purpose
    -   [CairoSurface::getType](/class/cairosurface.html#CairoSurface::getType)
        — The getType purpose
    -   [CairoSurface::markDirty](/class/cairosurface.html#CairoSurface::markDirty)
        — The markDirty purpose
    -   [CairoSurface::markDirtyRectangle](/class/cairosurface.html#CairoSurface::markDirtyRectangle)
        — The markDirtyRectangle purpose
    -   [CairoSurface::setDeviceOffset](/class/cairosurface.html#CairoSurface::setDeviceOffset)
        — The setDeviceOffset purpose
    -   [CairoSurface::setFallbackResolution](/class/cairosurface.html#CairoSurface::setFallbackResolution)
        — The setFallbackResolution purpose
    -   [CairoSurface::showPage](/class/cairosurface.html#CairoSurface::showPage)
        — The showPage purpose
    -   [CairoSurface::status](/class/cairosurface.html#CairoSurface::status)
        — The status purpose
    -   [CairoSurface::writeToPng](/class/cairosurface.html#CairoSurface::writeToPng)
        — The writeToPng purpose
-   [CairoSvgSurface](/class/cairosvgsurface.html) — Svg Surface Backend
    -   [CairoSvgSurface::\_\_construct](/class/cairosvgsurface.html#CairoSvgSurface::__construct)
        — The \_\_construct purpose
    -   [CairoSvgSurface::getVersions](/class/cairosvgsurface.html#CairoSvgSurface::getVersions)
        — Used to retrieve a list of supported SVG versions
    -   [CairoSvgSurface::restrictToVersion](/class/cairosvgsurface.html#CairoSvgSurface::restrictToVersion)
        — The restrictToVersion purpose
    -   [CairoSvgSurface::versionToString](/class/cairosvgsurface.html#CairoSvgSurface::versionToString)
        — The versionToString purpose
-   [CairoImageSurface](/class/cairoimagesurface.html) — The
    CairoImageSurface class
    -   [CairoImageSurface::\_\_construct](/class/cairoimagesurface.html#CairoImageSurface::__construct)
        — Creates a new CairoImageSurface
    -   [CairoImageSurface::createForData](/class/cairoimagesurface.html#CairoImageSurface::createForData)
        — The createForData purpose
    -   [CairoImageSurface::createFromPng](/class/cairoimagesurface.html#CairoImageSurface::createFromPng)
        — Creates a new CairoImageSurface form a png image file
    -   [CairoImageSurface::getData](/class/cairoimagesurface.html#CairoImageSurface::getData)
        — Gets the image data as string
    -   [CairoImageSurface::getFormat](/class/cairoimagesurface.html#CairoImageSurface::getFormat)
        — Get the image format
    -   [CairoImageSurface::getHeight](/class/cairoimagesurface.html#CairoImageSurface::getHeight)
        — Retrieves the height of the CairoImageSurface
    -   [CairoImageSurface::getStride](/class/cairoimagesurface.html#CairoImageSurface::getStride)
        — The getStride purpose
    -   [CairoImageSurface::getWidth](/class/cairoimagesurface.html#CairoImageSurface::getWidth)
        — Retrieves the width of the CairoImageSurface
-   [CairoPdfSurface](/class/cairopdfsurface.html) — The CairoPdfSurface
    class
    -   [CairoPdfSurface::\_\_construct](/class/cairopdfsurface.html#CairoPdfSurface::__construct)
        — The \_\_construct purpose
    -   [CairoPdfSurface::setSize](/class/cairopdfsurface.html#CairoPdfSurface::setSize)
        — The setSize purpose
-   [CairoPsSurface](/class/cairopssurface.html) — The CairoPsSurface
    class
    -   [CairoPsSurface::\_\_construct](/class/cairopssurface.html#CairoPsSurface::__construct)
        — The \_\_construct purpose
    -   [CairoPsSurface::dscBeginPageSetup](/class/cairopssurface.html#CairoPsSurface::dscBeginPageSetup)
        — The dscBeginPageSetup purpose
    -   [CairoPsSurface::dscBeginSetup](/class/cairopssurface.html#CairoPsSurface::dscBeginSetup)
        — The dscBeginSetup purpose
    -   [CairoPsSurface::dscComment](/class/cairopssurface.html#CairoPsSurface::dscComment)
        — The dscComment purpose
    -   [CairoPsSurface::getEps](/class/cairopssurface.html#CairoPsSurface::getEps)
        — The getEps purpose
    -   [CairoPsSurface::getLevels](/class/cairopssurface.html#CairoPsSurface::getLevels)
        — The getLevels purpose
    -   [CairoPsSurface::levelToString](/class/cairopssurface.html#CairoPsSurface::levelToString)
        — The levelToString purpose
    -   [CairoPsSurface::restrictToLevel](/class/cairopssurface.html#CairoPsSurface::restrictToLevel)
        — The restrictToLevel purpose
    -   [CairoPsSurface::setEps](/class/cairopssurface.html#CairoPsSurface::setEps)
        — The setEps purpose
    -   [CairoPsSurface::setSize](/class/cairopssurface.html#CairoPsSurface::setSize)
        — The setSize purpose
-   [CairoSurfaceType](/class/cairosurfacetype.html) — The
    CairoSurfaceType class
-   [CairoFontFace](/class/cairofontface.html) — The CairoFontFace class
    -   [CairoFontFace::\_\_construct](/class/cairofontface.html#CairoFontFace::__construct)
        — Creates a new CairoFontFace object
    -   [CairoFontFace::getType](/class/cairofontface.html#CairoFontFace::getType)
        — Retrieves the font face type
    -   [CairoFontFace::status](/class/cairofontface.html#CairoFontFace::status)
        — Check for CairoFontFace errors
-   [CairoFontOptions](/class/cairofontoptions.html) — The
    CairoFontOptions class
    -   [CairoFontOptions::\_\_construct](/class/cairofontoptions.html#CairoFontOptions::__construct)
        — The \_\_construct purpose
    -   [CairoFontOptions::equal](/class/cairofontoptions.html#CairoFontOptions::equal)
        — The equal purpose
    -   [CairoFontOptions::getAntialias](/class/cairofontoptions.html#CairoFontOptions::getAntialias)
        — The getAntialias purpose
    -   [CairoFontOptions::getHintMetrics](/class/cairofontoptions.html#CairoFontOptions::getHintMetrics)
        — The getHintMetrics purpose
    -   [CairoFontOptions::getHintStyle](/class/cairofontoptions.html#CairoFontOptions::getHintStyle)
        — The getHintStyle purpose
    -   [CairoFontOptions::getSubpixelOrder](/class/cairofontoptions.html#CairoFontOptions::getSubpixelOrder)
        — The getSubpixelOrder purpose
    -   [CairoFontOptions::hash](/class/cairofontoptions.html#CairoFontOptions::hash)
        — The hash purpose
    -   [CairoFontOptions::merge](/class/cairofontoptions.html#CairoFontOptions::merge)
        — The merge purpose
    -   [CairoFontOptions::setAntialias](/class/cairofontoptions.html#CairoFontOptions::setAntialias)
        — The setAntialias purpose
    -   [CairoFontOptions::setHintMetrics](/class/cairofontoptions.html#CairoFontOptions::setHintMetrics)
        — The setHintMetrics purpose
    -   [CairoFontOptions::setHintStyle](/class/cairofontoptions.html#CairoFontOptions::setHintStyle)
        — The setHintStyle purpose
    -   [CairoFontOptions::setSubpixelOrder](/class/cairofontoptions.html#CairoFontOptions::setSubpixelOrder)
        — The setSubpixelOrder purpose
    -   [CairoFontOptions::status](/class/cairofontoptions.html#CairoFontOptions::status)
        — The status purpose
-   [CairoFontSlant](/class/cairofontslant.html) — The CairoFontSlant
    class
-   [CairoFontType](/class/cairofonttype.html) — The CairoFontType class
-   [CairoFontWeight](/class/cairofontweight.html) — The CairoFontWeight
    class
-   [CairoScaledFont](/class/cairoscaledfont.html) — The CairoScaledFont
    class
    -   [CairoScaledFont::\_\_construct](/class/cairoscaledfont.html#CairoScaledFont::__construct)
        — The \_\_construct purpose
    -   [CairoScaledFont::extents](/class/cairoscaledfont.html#CairoScaledFont::extents)
        — The extents purpose
    -   [CairoScaledFont::getCtm](/class/cairoscaledfont.html#CairoScaledFont::getCtm)
        — The getCtm purpose
    -   [CairoScaledFont::getFontFace](/class/cairoscaledfont.html#CairoScaledFont::getFontFace)
        — The getFontFace purpose
    -   [CairoScaledFont::getFontMatrix](/class/cairoscaledfont.html#CairoScaledFont::getFontMatrix)
        — The getFontMatrix purpose
    -   [CairoScaledFont::getFontOptions](/class/cairoscaledfont.html#CairoScaledFont::getFontOptions)
        — The getFontOptions purpose
    -   [CairoScaledFont::getScaleMatrix](/class/cairoscaledfont.html#CairoScaledFont::getScaleMatrix)
        — The getScaleMatrix purpose
    -   [CairoScaledFont::getType](/class/cairoscaledfont.html#CairoScaledFont::getType)
        — The getType purpose
    -   [CairoScaledFont::glyphExtents](/class/cairoscaledfont.html#CairoScaledFont::glyphExtents)
        — The glyphExtents purpose
    -   [CairoScaledFont::status](/class/cairoscaledfont.html#CairoScaledFont::status)
        — The status purpose
    -   [CairoScaledFont::textExtents](/class/cairoscaledfont.html#CairoScaledFont::textExtents)
        — The textExtents purpose
-   [CairoToyFontFace](/class/cairotoyfontface.html) — The
    CairoToyFontFace class
-   [CairoPatternType](/class/cairopatterntype.html) — The
    CairoPatternType class
-   [CairoPattern](/class/cairopattern.html) — The CairoPattern class
    -   [CairoPattern::\_\_construct](/class/cairopattern.html#CairoPattern::__construct)
        — The \_\_construct purpose
    -   [CairoPattern::getMatrix](/class/cairopattern.html#CairoPattern::getMatrix)
        — The getMatrix purpose
    -   [CairoPattern::getType](/class/cairopattern.html#CairoPattern::getType)
        — The getType purpose
    -   [CairoPattern::setMatrix](/class/cairopattern.html#CairoPattern::setMatrix)
        — The setMatrix purpose
    -   [CairoPattern::status](/class/cairopattern.html#CairoPattern::status)
        — The status purpose
-   [CairoGradientPattern](/class/cairogradientpattern.html) — The
    CairoGradientPattern class
    -   [CairoGradientPattern::addColorStopRgb](/class/cairogradientpattern.html#CairoGradientPattern::addColorStopRgb)
        — The addColorStopRgb purpose
    -   [CairoGradientPattern::addColorStopRgba](/class/cairogradientpattern.html#CairoGradientPattern::addColorStopRgba)
        — The addColorStopRgba purpose
    -   [CairoGradientPattern::getColorStopCount](/class/cairogradientpattern.html#CairoGradientPattern::getColorStopCount)
        — The getColorStopCount purpose
    -   [CairoGradientPattern::getColorStopRgba](/class/cairogradientpattern.html#CairoGradientPattern::getColorStopRgba)
        — The getColorStopRgba purpose
    -   [CairoGradientPattern::getExtend](/class/cairogradientpattern.html#CairoGradientPattern::getExtend)
        — The getExtend purpose
    -   [CairoGradientPattern::setExtend](/class/cairogradientpattern.html#CairoGradientPattern::setExtend)
        — The setExtend purpose
-   [CairoSolidPattern](/class/cairosolidpattern.html) — The
    CairoSolidPattern class
    -   [CairoSolidPattern::\_\_construct](/class/cairosolidpattern.html#CairoSolidPattern::__construct)
        — The \_\_construct purpose
    -   [CairoSolidPattern::getRgba](/class/cairosolidpattern.html#CairoSolidPattern::getRgba)
        — The getRgba purpose
-   [CairoSurfacePattern](/class/cairosurfacepattern.html) — The
    CairoSurfacePattern class
    -   [CairoSurfacePattern::\_\_construct](/class/cairosurfacepattern.html#CairoSurfacePattern::__construct)
        — The \_\_construct purpose
    -   [CairoSurfacePattern::getExtend](/class/cairosurfacepattern.html#CairoSurfacePattern::getExtend)
        — The getExtend purpose
    -   [CairoSurfacePattern::getFilter](/class/cairosurfacepattern.html#CairoSurfacePattern::getFilter)
        — The getFilter purpose
    -   [CairoSurfacePattern::getSurface](/class/cairosurfacepattern.html#CairoSurfacePattern::getSurface)
        — The getSurface purpose
    -   [CairoSurfacePattern::setExtend](/class/cairosurfacepattern.html#CairoSurfacePattern::setExtend)
        — The setExtend purpose
    -   [CairoSurfacePattern::setFilter](/class/cairosurfacepattern.html#CairoSurfacePattern::setFilter)
        — The setFilter purpose
-   [CairoLinearGradient](/class/cairolineargradient.html) — The
    CairoLinearGradient class
    -   [CairoLinearGradient::\_\_construct](/class/cairolineargradient.html#CairoLinearGradient::__construct)
        — The \_\_construct purpose
    -   [CairoLinearGradient::getPoints](/class/cairolineargradient.html#CairoLinearGradient::getPoints)
        — The getPoints purpose
-   [CairoRadialGradient](/class/cairoradialgradient.html) — The
    CairoRadialGradient class
    -   [CairoRadialGradient::\_\_construct](/class/cairoradialgradient.html#CairoRadialGradient::__construct)
        — The \_\_construct purpose
    -   [CairoRadialGradient::getCircles](/class/cairoradialgradient.html#CairoRadialGradient::getCircles)
        — The getCircles purpose
-   [CairoAntialias](/class/cairoantialias.html) — The CairoAntialias
    class
-   [CairoContent](/class/cairocontent.html) — The CairoContent class
-   [CairoExtend](/class/cairoextend.html) — The CairoExtend class
-   [CairoFormat](/class/cairoformat.html) — The CairoFormat class
    -   [CairoFormat::strideForWidth](/class/cairoformat.html#CairoFormat::strideForWidth)
        — Provides an appropriate stride to use
-   [CairoFillRule](/class/cairofillrule.html) — The CairoFillRule class
-   [CairoFilter](/class/cairofilter.html) — The CairoFilter class
-   [CairoHintMetrics](/class/cairohintmetrics.html) — The
    CairoHintMetrics class
-   [CairoHintStyle](/class/cairohintstyle.html) — The CairoHintStyle
    class
-   [CairoLineCap](/class/cairolinecap.html) — The CairoLineCap class
-   [CairoLineJoin](/class/cairolinejoin.html) — The CairoLineJoin class
-   [CairoMatrix](/class/cairomatrix.html) — The CairoMatrix class
    -   [CairoMatrix::\_\_construct](/class/cairomatrix.html#CairoMatrix::__construct)
        — Creates a new CairoMatrix object
    -   [CairoMatrix::initIdentity](/class/cairomatrix.html#CairoMatrix::initIdentity)
        — Creates a new identity matrix
    -   [CairoMatrix::initRotate](/class/cairomatrix.html#CairoMatrix::initRotate)
        — Creates a new rotated matrix
    -   [CairoMatrix::initScale](/class/cairomatrix.html#CairoMatrix::initScale)
        — Creates a new scaling matrix
    -   [CairoMatrix::initTranslate](/class/cairomatrix.html#CairoMatrix::initTranslate)
        — Creates a new translation matrix
    -   [CairoMatrix::invert](/class/cairomatrix.html#CairoMatrix::invert)
        — The invert purpose
    -   [CairoMatrix::multiply](/class/cairomatrix.html#CairoMatrix::multiply)
        — The multiply purpose
    -   [CairoMatrix::rotate](/class/cairomatrix.html#CairoMatrix::rotate)
        — The rotate purpose
    -   [CairoMatrix::scale](/class/cairomatrix.html#CairoMatrix::scale)
        — Applies scaling to a matrix
    -   [CairoMatrix::transformDistance](/class/cairomatrix.html#CairoMatrix::transformDistance)
        — The transformDistance purpose
    -   [CairoMatrix::transformPoint](/class/cairomatrix.html#CairoMatrix::transformPoint)
        — The transformPoint purpose
    -   [CairoMatrix::translate](/class/cairomatrix.html#CairoMatrix::translate)
        — The translate purpose
-   [CairoOperator](/class/cairooperator.html) — The CairoOperator class
-   [CairoPath](/class/cairopath.html) — The CairoPath class
-   [CairoPsLevel](/class/cairopslevel.html) — The CairoPsLevel class
-   [CairoSubpixelOrder](/class/cairosubpixelorder.html) — The
    CairoSubpixelOrder class
-   [CairoSvgVersion](/class/cairosvgversion.html) — The CairoSvgVersion
    class

简介
----

Simple class with some static helper methods.

类摘要
------

**Cairo**

<span class="ooclass"> class **Cairo** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">availableFonts</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">availableSurfaces</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">statusToString</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">version</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">versionString</span> ( <span
class="methodparam">void</span> )

}

Cairo::availableFonts
=====================

cairo\_available\_fonts
=======================

Retrieves the availables font types

### 说明

面向对象风格:

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Cairo::availableFonts</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_available\_fonts</span> ( <span
class="methodparam">void</span> )

Returns an array with the available font backends

### 参数

此函数没有参数。

### 返回值

A list-type array with all available font backends.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* Object Oriented Style */
var_dump(Cairo::availableFonts());

?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      string(5) "WIN32"
      [1]=>
      string(4) "USER"
    }

**示例 \#2 过程化风格**

``` php
<?php

/* Procedural style */
var_dump(cairo_available_fonts());

?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      string(5) "WIN32"
      [1]=>
      string(4) "USER"
    }

### 参见

-   <span class="methodname">Cairo::availableSurfaces</span>

Cairo::availableSurfaces
========================

cairo\_available\_surfaces
==========================

Retrieves all available surfaces

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Cairo::availableSurfaces</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_available\_surfaces</span> ( <span
class="methodparam">void</span> )

Returns an array with the available surface backends

### 参数

此函数没有参数。

### 返回值

A list-type array with all available surface backends.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

/* Object Oriented style */
var_dump(Cairo::availableSurfaces());

?>
```

以上例程的输出类似于：

    array(6) {
      [0]=>
      string(5) "IMAGE"
      [1]=>
      string(3) "PNG"
      [2]=>
      string(3) "PDF"
      [3]=>
      string(2) "PS"
      [4]=>
      string(3) "SVG"
      [5]=>
      string(5) "WIN32"
    }

**示例 \#2 过程化风格**

``` php
<?php

/* Procedural style */
var_dump(cairo_available_surfaces());

?>
```

以上例程的输出类似于：

    array(6) {
      [0]=>
      string(5) "IMAGE"
      [1]=>
      string(3) "PNG"
      [2]=>
      string(3) "PDF"
      [3]=>
      string(2) "PS"
      [4]=>
      string(3) "SVG"
      [5]=>
      string(5) "WIN32"
    }

### 参见

-   <span class="methodname">Cairo::availableFonts</span>

Cairo::statusToString
=====================

cairo\_status\_to\_string
=========================

Retrieves the current status as string

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Cairo::statusToString</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">cairo\_status\_to\_string</span> ( <span
class="methodparam"><span class="type">int</span> `$status`</span> )

Retrieves the current status as a readable string

### 参数

`status`  
A valid status code given by <span class="function">cairo\_status</span>
or <span class="methodname">CairoContext::status</span>

### 返回值

A string containing the current status of a <span
class="classname">CairoContext</span> object

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);
$context = new CairoContext($surface);

var_dump(Cairo::statusToString($context->status()));
?>
```

以上例程的输出类似于：

    string(7) "success"

**示例 \#2 过程化风格**

``` php
<?php
$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);
$context = cairo_create($surface);

var_dump(cairo_status_to_string(cairo_status($context)));
?>
```

以上例程的输出类似于：

    string(7) "success"

### 参见

-   <span class="methodname">CairoContext::status</span>

Cairo::version
==============

cairo\_version
==============

Retrieves cairo's library version

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Cairo::version</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_version</span> ( <span
class="methodparam">void</span> )

Retrieves the current version of the cairo library as an integer value

### 参数

此函数没有参数。

### 返回值

Current Cairo library version integer

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
var_dump(Cairo::version());
?>
```

以上例程的输出类似于：

    int(10808)

**示例 \#2 过程化风格**

``` php
<?php
var_dump(cairo_version());
?>
```

以上例程的输出类似于：

    int(10808)

### 参见

-   <span class="methodname">Cairo::versionString</span>

Cairo::versionString
====================

cairo\_version\_string
======================

Retrieves cairo version as string

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">Cairo::versionString</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">string</span> <span
class="methodname">cairo\_version\_string</span> ( <span
class="methodparam">void</span> )

Retrieves the current cairo library version as a string.

### 参数

此函数没有参数。

### 返回值

Current Cairo library version string

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

var_dump(Cairo::versionString());

?>
```

以上例程的输出类似于：

    string(5) "1.8.8"

**示例 \#2 过程化风格**

``` php
<?php

var_dump(cairo_version_string());

?>
```

以上例程的输出类似于：

    string(5) "1.8.8"

### 参见

-   <span class="methodname">Cairo::version</span>

简介
----

Context is the main object used when drawing with cairo. To draw with
cairo, you create a <span class="classname">CairoContext</span>, set the
target <span class="classname">CairoSurface</span>, and drawing options
for the <span class="classname">CairoContext</span>, create shapes with
functions . like <span class="methodname">CairoContext::moveTo</span>
and <span class="methodname">CairoContext::lineTo</span>, and then draw
shapes with <span class="methodname">CairoContext::stroke</span> or
<span class="methodname">CairoContext::fill</span>. Contexts can be
pushed to a stack via <span
class="methodname">CairoContext::save</span>. They may then safely be
changed, without losing the current state. Use <span
class="methodname">CairoContext::restore</span> to restore to the saved
state.

类摘要
------

**CairoContext**

<span class="ooclass"> class **CairoContext** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">appendPath</span> ( <span
class="methodparam"><span class="type">CairoPath</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">arc</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$radius`</span> , <span
class="methodparam"><span class="type">float</span> `$angle1`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle2`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">arcNegative</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$radius`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle1`</span> , <span class="methodparam"><span
class="type">float</span> `$angle2`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clip</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">clipExtents</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clipPreserve</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">clipRectangleList</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">closePath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">copyPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">CairoPath</span>
<span class="methodname">copyPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">CairoPath</span>
<span class="methodname">copyPathFlat</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">curveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">deviceToUser</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">deviceToUserDistance</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">fill</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">fillExtents</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">fillPreserve</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">fontExtents</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getAntialias</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getCurrentPoint</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDash</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getDashCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFillRule</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontFace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getGroupTarget</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLineCap</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getLineJoin</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getLineWidth</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getMiterLimit</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getOperator</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getScaledFont</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getSource</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getTarget</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getTolerance</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">glyphPath</span> ( <span
class="methodparam"><span class="type">array</span> `$glyphs`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasCurrentPoint</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">identityMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">inFill</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">inStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">lineTo</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">mask</span> ( <span class="methodparam"><span
class="type">CairoPattern</span> `$pattern`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">maskSurface</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> \[, <span class="methodparam"><span
class="type">float</span> `$x`</span> \[, <span
class="methodparam"><span class="type">float</span> `$y`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">moveTo</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">newPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">newSubPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">paint</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">paintWithAlpha</span> ( <span
class="methodparam"><span class="type">float</span> `$alpha`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">pathExtents</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">popGroup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">popGroupToSource</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pushGroup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">pushGroupWithContent</span> ( <span
class="methodparam"><span class="type">int</span> `$content`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">relCurveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">relLineTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">relMoveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resetClip</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">restore</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rotate</span> ( <span class="methodparam"><span
class="type">float</span> `$angle`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">save</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">scale</span> ( <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">selectFontFace</span> ( <span
class="methodparam"><span class="type">string</span> `$family`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slant`</span> \[, <span class="methodparam"><span
class="type">int</span> `$weight`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAntialias</span> (\[ <span
class="methodparam"><span class="type">int</span> `$antialias`</span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setDash</span> ( <span
class="methodparam"><span class="type">array</span> `$dashes`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$offset`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFillRule</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFontFace</span> ( <span
class="methodparam"><span class="type">CairoFontFace</span>
`$fontface`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFontMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFontOptions</span> ( <span
class="methodparam"><span class="type">CairoFontOptions</span>
`$fontoptions`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFontSize</span> ( <span
class="methodparam"><span class="type">float</span> `$size`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setLineCap</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setLineJoin</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setLineWidth</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMiterLimit</span> ( <span
class="methodparam"><span class="type">float</span> `$limit`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setOperator</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setScaledFont</span> ( <span
class="methodparam"><span class="type">CairoScaledFont</span>
`$scaledfont`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSource</span> ( <span
class="methodparam"><span class="type">CairoPattern</span>
`$pattern`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSourceRGB</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSourceRGBA</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> , <span
class="methodparam"><span class="type">float</span> `$alpha`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSourceSurface</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> \[, <span class="methodparam"><span
class="type">float</span> `$x`</span> \[, <span
class="methodparam"><span class="type">float</span> `$y`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setTolerance</span> ( <span
class="methodparam"><span class="type">float</span> `$tolerance`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">showPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">showText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">stroke</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">strokeExtents</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">strokePreserve</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">textExtents</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">textPath</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">transform</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">translate</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">userToDevice</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">userToDeviceDistance</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

}

CairoContext::appendPath
========================

cairo\_append\_path
===================

Appends a path to current path

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::appendPath</span> ( <span
class="methodparam"><span class="type">CairoPath</span> `$path`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_append\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoPath</span> `$path`</span> )

Appends the `path` onto the current path. The `path` may be either the
return value from one of <span
class="methodname">CairoContext::copyPath</span> or <span
class="methodname">CairoContext::copyPathFlat</span>;

if `path` is not a valid <span class="classname">CairoPath</span>
instance a <span class="classname">CairoException</span> will be thrown

### 参数

`context`  
CairoContext object

`path`  
CairoPath object

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

$path = $context->copyPath();

$context->appendPath($path);

?>
```

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

$path = cairo_copy_path($context);

cairo_append_path($context, $path);

?>
```

### 参见

-   <span class="classname">CairoPath</span>
-   <span class="methodname">CairoContext::copyPath</span>
-   <span class="methodname">CairoContext::copyPathFlat</span>

CairoContext::arc
=================

cairo\_arc
==========

Adds a circular arc

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::arc</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$radius`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle1`</span> , <span class="methodparam"><span
class="type">float</span> `$angle2`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_arc</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$radius`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle1`</span> , <span class="methodparam"><span
class="type">float</span> `$angle2`</span> )

Adds a circular arc of the given radius to the current path. The arc is
centered at (`x`, `y`), begins at `angle1` and proceeds in the direction
of increasing angles to end at `angle2`. If `angle2` is less than
`angle1` it will be progressively increased by 2\*M\_PI until it is
greater than `angle1`. If there is a current point, an initial line
segment will be added to the path to connect the current point to the
beginning of the arc. If this initial line is undesired, it can be
avoided by calling <span
class="methodname">CairoContext::newSubPath</span> or procedural <span
class="function">cairo\_new\_sub\_path</span> before calling <span
class="methodname">CairoContext::arc</span> or <span
class="function">cairo\_arc</span>. Angles are measured in radians. An
angle of 0.0 is in the direction of the positive X axis (in user space).
An angle of M\_PI/2.0 radians (90 degrees) is in the direction of the
positive Y axis (in user space). Angles increase in the direction from
the positive X axis toward the positive Y axis. So with the default
transformation matrix, angles increase in a clockwise direction. (To
convert from degrees to radians, use degrees \* (M\_PI / 180.).) This
function gives the arc in the direction of increasing angles; see <span
class="methodname">CairoContext::arcNegative</span> or <span
class="function">cairo\_arc\_negative</span> to get the arc in the
direction of decreasing angles.

### 参数

`context`  
A valid CairoContext object

`x`  
x position

`y`  
y position

`radius`  
Radius of the arc

`angle1`  
start angle

`angle2`  
end angle

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);

$c->setSourceRgb(0, 0, 0);
$c->paint();

$c->setLineWidth(1);
$c->setSourceRgb(1, 1, 1);

for ($r = 50; $r > 0; $r -= 10) {
 $c->arc(50, 50, $r, 0, 2 * M_PI);
 $c->stroke();
 $c->fill();
}

$s->writeToPng(dirname(__FILE__) . '/CairoContext__arc.png');
?>
```

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

cairo_set_source_rgb($c, 0, 0, 0);
cairo_paint($c);

cairo_set_source_rgb($c, 1, 1, 1);
cairo_set_line_width($c, 1);

for ($r = 50; $r > 0; $r -= 10) {
 cairo_arc($c, 50, 50, $r, 0, 2 * M_PI);
 cairo_stroke($c);
 cairo_fill($c);
}

cairo_surface_write_to_png($s, dirname(__FILE__) . '/cairo_arc.png');
?>
```

### 参见

-   <span class="methodname">CairoContext::arcNegative</span>

CairoContext::arcNegative
=========================

cairo\_arc\_negative
====================

Adds a negative arc

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::arcNegative</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$radius`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle1`</span> , <span class="methodparam"><span
class="type">float</span> `$angle2`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_arc\_negative</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$radius`</span> , <span
class="methodparam"><span class="type">float</span> `$angle1`</span> ,
<span class="methodparam"><span class="type">float</span>
`$angle2`</span> )

Adds a circular arc of the given `radius` to the current path. The arc
is centered at (`x`, `y`), begins at `angle1` and proceeds in the
direction of decreasing angles to end at `angle2`. If `angle2` is
greater than `angle1` it will be progressively decreased by 2\*M\_PI
until it is less than `angle1`. See <span
class="methodname">CairoContext::arc</span> or <span
class="function">cairo\_arc</span> for more details. This function
differs only in the direction of the arc between the two angles.

### 参数

`context`  
A valid CairoContext object

`x`  
double x position

`y`  
double y position

`radius`  
The radius of the desired negative arc

`angle1`  
Start angle of the arc

`angle2`  
End angle of the arc

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);

$c->setSourceRgb(0, 0, 0);
$c->paint();

$c->setLineWidth(1);
$c->setSourceRgb(1, 1, 1);

for ($r = 50; $r > 0; $r -= 10) {
 $c->arcNegative(50, 50, $r, 2 * M_PI, 0);
 $c->stroke();
 $c->fill();
}

$s->writeToPng(dirname(__FILE__) . '/CairoContext__arcNegative.png');
?>
```

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

cairo_set_source_rgb($c, 0, 0, 0);
cairo_paint($c);

cairo_set_source_rgb($c, 1, 1, 1);
cairo_set_line_width($c, 1);

for ($r = 50; $r > 0; $r -= 10) {
 cairo_arc_negative($c, 50, 50, $r, 2 * M_PI, 0);
 cairo_stroke($c);
 cairo_fill($c);
}

cairo_surface_write_to_png($s, dirname(__FILE__) . '/cairo_arc_negative.png');
?>
```

### 参见

-   <span class="methodname">CairoContext::arc</span>

CairoContext::clip
==================

cairo\_clip
===========

Establishes a new clip region

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::clip</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_clip</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> )

Establishes a new clip region by intersecting the current clip region
with the current path as it would be filled by <span
class="methodname">CairoContext::fill</span> or <span
class="function">cairo\_fill</span> and according to the current fill
rule (see <span class="methodname">CairoContext::setFillRule</span> or
<span class="function">cairo\_set\_fill\_rule</span>).

After <span class="methodname">CairoContext::clip</span> or <span
class="function">cairo\_clip</span>, the current path will be cleared
from the cairo context.

The current clip region affects all drawing operations by effectively
masking out any changes to the surface that are outside the current clip
region.

Calling <span class="methodname">CairoContext::clip</span> or <span
class="function">cairo\_clip</span> can only make the clip region
smaller, never larger. But the current clip is part of the graphics
state, so a temporary restriction of the clip region can be achieved by
calling <span class="methodname">CairoContext::clip</span> or <span
class="function">cairo\_clip</span> within a <span
class="methodname">CairoContext::save</span>/ <span
class="methodname">CairoContext::restore</span> or <span
class="function">cairo\_save</span>/<span
class="function">cairo\_restore</span> pair. The only other means of
increasing the size of the clip region is <span
class="methodname">CairoContext::resetClip</span> or procedural <span
class="function">cairo\_reset\_clip</span>.

### 参数

`context`  
A valid CairoContext object

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

$context->clip();

?>
```

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

cairo_clip($context);

?>
```

### 参见

-   <span class="methodname">CairoContext::resetClip</span>
-   <span class="function">cairo\_reset\_clip</span>

CairoContext::clipExtents
=========================

cairo\_clip\_extents
====================

Computes the area inside the current clip

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::clipExtents</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_clip\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Computes a bounding box in user coordinates covering the area inside the
current clip.

### 参数

`context`  
A valid CairoContext object

### 返回值

An array containing the (float)x1, (float)y1, (float)x2, (float)y2,
coordinates covering the area inside the current clip

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

var_dump($context->clipExtents());
?>
```

以上例程的输出类似于：

    array(4) {
      [0]=>
      float(0)
      [1]=>
      float(0)
      [2]=>
      float(50)
      [3]=>
      float(50)
    }

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

var_dump(cairo_clip_extents($context));

?>
```

以上例程的输出类似于：

    array(4) {
      [0]=>
      float(0)
      [1]=>
      float(0)
      [2]=>
      float(50)
      [3]=>
      float(50)
    }

### 参见

-   <span class="methodname">CairoContext::clip</span>

CairoContext::clipPreserve
==========================

cairo\_clip\_preserve
=====================

Establishes a new clip region from the current clip

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::clipPreserve</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_clip\_preserve</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Establishes a new clip region by intersecting the current clip region
with the current path as it would be filled by <span
class="methodname">Context.fill</span> and according to the current FILL
RULE (see <span class="methodname">CairoContext::setFillRule</span> or
<span class="function">cairo\_set\_fill\_rule</span>).

Unlike <span class="methodname">CairoContext::clip</span>, <span
class="methodname">CairoContext::clipPreserve</span> preserves the path
within the Context. The current clip region affects all drawing
operations by effectively masking out any changes to the surface that
are outside the current clip region.

Calling <span class="methodname">CairoContext::clipPreserve</span> can
only make the clip region smaller, never larger. But the current clip is
part of the graphics state, so a temporary restriction of the clip
region can be achieved by calling <span
class="methodname">CairoContext::clipPreserve</span> within a <span
class="methodname">CairoContext::save</span>/ <span
class="methodname">CairoContext::restore</span> pair. The only other
means of increasing the size of the clip region is <span
class="methodname">CairoContext::resetClip</span>.

### 参数

`context`  
A valid CairoContext object

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

$context->clipPreserve();

?>
```

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

cairo_clip_preserve($context);

?>
```

### 参见

-   <span class="methodname">CairoContext::save</span>
-   <span class="methodname">CairoContext::restore</span>
-   <span class="methodname">CairoContext::resetClip</span>

CairoContext::clipRectangleList
===============================

cairo\_clip\_rectangle\_list
============================

Retrieves the current clip as a list of rectangles

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::clipRectangleList</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_clip\_rectangle\_list</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Returns a list-type array with the current clip region as a list of
rectangles in user coordinates

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

An array of user-space represented rectangles for the current clip

(The status in the list may be CAIRO\_STATUS\_CLIP\_NOT\_REPRESENTABLE
to indicate that the clip region cannot be represented as a list of
user-space rectangles. The status may have other values to indicate
other errors.)

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

var_dump($context->clipRectangleList());

?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      array(4) {
        ["x"]=>
        float(0)
        ["y"]=>
        float(0)
        ["width"]=>
        float(50)
        ["height"]=>
        float(50)
      }
    }

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

var_dump(cairo_clip_rectangle_list($context));

?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      array(4) {
        ["x"]=>
        float(0)
        ["y"]=>
        float(0)
        ["width"]=>
        float(50)
        ["height"]=>
        float(50)
      }
    }

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::closePath
=======================

cairo\_close\_path
==================

Closes the current path

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::closePath</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_close\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Adds a line segment to the path from the current point to the beginning
of the current sub-path, (the most recent point passed to <span
class="methodname">CairoContext::moveTo</span>), and closes this
sub-path. After this call the current point will be at the joined
endpoint of the sub-path.

The behavior of close\_path() is distinct from simply calling <span
class="methodname">CairoContext::lineTo</span> with the equivalent
coordinate in the case of stroking. When a closed sub-path is stroked,
there are no caps on the ends of the sub-path. Instead, there is a line
join connecting the final and initial segments of the sub-path.

If there is no current point before the call to <span
class="methodname">CairoContext::closePath</span>, this function will
have no effect.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

$context->closePath();

?>
```

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

cairo_close_path($context);

?>
```

### 参见

-   <span class="methodname">CairoContext::copyPath</span>

CairoContext::\_\_construct
===========================

Creates a new CairoContext

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoContext::\_\_construct</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> )

Creates a new CairoContext object to draw

### 参数

`surface`  
A valid <span class="classname">CairoSurface</span> like <span
class="classname">CairoImageSurface</span> or <span
class="classname">CairoPdfSurface</span>

### 返回值

A <span class="classname">CairoContext</span>

### 范例

**示例 \#1 <span class="methodname">CairoContext::\_\_construct</span>
example**

``` php
<?php
// The surface to work on
$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

// Create a new CairoContext for the CairoSurface
$context = new CairoContext($surface);

?>
```

### 参见

-   <span class="methodname">Cairo::Method</span>

CairoContext::copyPage
======================

cairo\_copy\_page
=================

Emits the current page

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::copyPage</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_copy\_page</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Emits the current page for backends that support multiple pages, but
doesn’t clear it, so, the contents of the current page will be retained
for the next page too. Use <span
class="methodname">CairoContext::showPage</span> if you want to get an
empty page after the emission.

This is a convenience function that simply calls <span
class="methodname">CairoSurface::copyPage</span> on <span
class="classname">CairoContext</span>’s target.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

$context->copyPage();

?>
```

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

cairo_copy_page($context);

?>
```

### 参见

-   <span class="methodname">CairoContext::showPage</span>
-   <span class="methodname">CairoSurface::copyPage</span>

CairoContext::copyPath
======================

cairo\_copy\_path
=================

Creates a copy of the current path

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">CairoPath</span>
<span class="methodname">CairoContext::copyPath</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">CairoPath</span> <span
class="methodname">cairo\_copy\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Creates a copy of the current path and returns it to the user as a <span
class="classname">CairoPath</span>. See <span
class="classname">CairoPath</span> for hints on how to iterate over the
returned data structure.

This function will always return a valid <span
class="classname">CairoPath</span> object, but the result will have no
data, if either of the following conditions hold:

-   1\. If there is insufficient memory to copy the path. In this case
    CairoPath-\>status will be set to CAIRO\_STATUS\_NO\_MEMORY.
-   2\. If `context` is already in an error state. In this case
    CairoPath-\>status will contain the same status that would be
    returned by <span class="function">cairo\_status</span>.

In either case, CairoPath-\>status will be set to
CAIRO\_STATUS\_NO\_MEMORY (regardless of what the error status in cr
might have been).

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

A copy of the current <span class="classname">CairoPath</span> in the
context

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

var_dump($context->copyPath())

?>
```

以上例程的输出类似于：

    object(CairoPath)#3 (0) {
    }

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

var_dump(cairo_copy_path($context));

?>
```

以上例程的输出类似于：

    object(CairoPath)#3 (0) {
    }

### 参见

-   <span class="methodname">CairoContext::closePath</span>

CairoContext::copyPathFlat
==========================

cairo\_copy\_path\_flat
=======================

Gets a flattened copy of the current path

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">CairoPath</span>
<span class="methodname">CairoContext::copyPathFlat</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">CairoPath</span> <span
class="methodname">cairo\_copy\_path\_flat</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Gets a flattened copy of the current path and returns it to the user as
a <span class="classname">CairoPath</span>.

This function is like <span
class="methodname">CairoContext::copyPath</span> except that any curves
in the path will be approximated with piecewise-linear approximations,
(accurate to within the current tolerance value). That is, the result is
guaranteed to not have any elements of type CAIRO\_PATH\_CURVE\_TO which
will instead be replaced by a series of CAIRO\_PATH\_LINE\_TO elements.

### 参数

`context`  
A CairoContext object

### 返回值

A copy of the current path

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

$context = new CairoContext($surface);

var_dump($context->copyPathFlat());

?>
```

以上例程的输出类似于：

    object(CairoPath)#3 (0) {
    }

**示例 \#2 过程化风格**

``` php
<?php

$surface = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);

$context = cairo_create($surface);

var_dump(cairo_copy_path_flat($context));

?>
```

以上例程的输出类似于：

    object(CairoPath)#3 (0) {
    }

### 参见

-   <span class="methodname">CairoContext::copyPath</span>
-   <span class="methodname">CairoContext::closePath</span>

CairoContext::curveTo
=====================

cairo\_curve\_to
================

Adds a curve

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::curveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_curve\_to</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x1`</span> , <span class="methodparam"><span
class="type">float</span> `$y1`</span> , <span class="methodparam"><span
class="type">float</span> `$x2`</span> , <span class="methodparam"><span
class="type">float</span> `$y2`</span> , <span class="methodparam"><span
class="type">float</span> `$x3`</span> , <span class="methodparam"><span
class="type">float</span> `$y3`</span> )

Adds a cubic Bezier spline to the path from the current point to
position `x3` ,`y3` in user-space coordinates, using `x1`, `y1` and
`x2`, `y2` as the control points. After this call the current point will
be `x3`, `y3`.

If there is no current point before the call to <span
class="methodname">CairoContext::curveTo</span> this function will
behave as if preceded by a call to <span
class="methodname">CairoContext::moveTo</span> (`x1`, `y1`).

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

`x1`  
First control point in the x axis for the curve

`y1`  
First control point in the y axis for the curve

`x2`  
Second control point in x axis for the curve

`y2`  
Second control point in y axis for the curve

`x3`  
Final point in the x axis for the curve

`y3`  
Final point in the y axis for the curve

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);

$c->setSourceRgb(0, 0, 0);

$c->paint();

$c->moveTo(10, 50); 
$c->setLineWidth(5);
$c->setSourceRgb(.1, 0, 1);
$c->curveTo(20, 80, 80, 20, 90, 50); 
$c->stroke();

$s->writeToPng(dirname(__FILE__) . '/curveTo.png');
?>
```

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

cairo_set_source_rgb($c, 0, 0, 0);

cairo_paint($c);

cairo_move_to($c, 10, 50);
cairo_set_line_width($c, 5);
cairo_set_source_rgb($c, .1, 0, 1);
cairo_curve_to($c, 20, 80, 80, 20, 90, 50);
cairo_stroke($c);

cairo_surface_write_to_png($s, dirname(__FILE__) . '/curve_to.png');
?>
```

### 参见

-   <span class="methodname">CairoContext::moveTo</span>

CairoContext::deviceToUser
==========================

cairo\_device\_to\_user
=======================

Transform a coordinate

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::deviceToUser</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_device\_to\_user</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Transform a coordinate from device space to user space by multiplying
the given point by the inverse of the current transformation matrix
(CTM).

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

`x`  
x value of the coordinate

`y`  
y value of the coordinate

### 返回值

An array containing the x and y coordinates in the user-space

### 参见

-   <span class="methodname">CairoContext::deviceToUserDistance</span>

CairoContext::deviceToUserDistance
==================================

cairo\_device\_to\_user\_distance
=================================

Transform a distance

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::deviceToUserDistance</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_device\_to\_user\_distance</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Transform a distance vector from device space to user space. This
function is similar to <span
class="methodname">CairoContext::deviceToUser</span> or <span
class="function">cairo\_device\_to\_user</span> except that the
translation components of the inverse Cairo Transformation Matrix will
be ignored when transforming (`x`,`y`).

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

`x`  
X component of a distance vector

`y`  
Y component of a distance vector

### 返回值

Returns an array with the x and y values of a distance vector in the
user-space

### 参见

-   <span class="methodname">CairoContext::deviceToUser</span>

CairoContext::fill
==================

cairo\_fill
===========

Fills the current path

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::fill</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_fill</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> )

A drawing operator that fills the current path according to the current
<span class="classname">CairoFillRule</span>, (each sub-path is
implicitly closed before being filled). After <span
class="methodname">CairoContext::fill</span> or <span
class="function">cairo\_fill</span>, the current path will be cleared
from the <span class="classname">CairoContext</span>.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);
 
$c->setSourceRgb(0, 0, 0);
$c->paint();

$c->setSourceRgb(1, 1, 1);
$c->rectangle(0, 0, 50, 50);
$c->fill();
$c->setSourceRgb(0, 1, 0);
$c->rectangle(50, 50, 50, 50);
$c->fill();

$s->writeToPng(dirname(__FILE__) . '/CairoContext_fill.png');

?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

cairo_set_source_rgb($c, 0, 0, 0);
cairo_paint($c);

cairo_set_source_rgb($c, 1, 1, 1);
cairo_rectangle($c, 0, 0, 50, 50);
cairo_fill($c);
cairo_set_source_rgb($c, 0, 1, 0);
cairo_rectangle($c, 50, 50, 50, 50);
cairo_fill($c);

cairo_surface_write_to_png($s, dirname(__FILE__) . '/cairo_fill.png');

?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">CairoContext::setFillRule</span>
-   <span class="methodname">ContextContext::fillPreserve</span>
-   <span class="classname">CairoFillRule</span>

CairoContext::fillExtents
=========================

cairo\_fill\_extents
====================

Computes the filled area

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::fillExtents</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_fill\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Computes a bounding box in user coordinates covering the area that would
be affected, (the “inked” area), by a <span
class="methodname">CairoContext::fill</span> operation given the current
path and fill parameters. If the current path is empty, returns an empty
rectangle (0,0,0,0). Surface dimensions and clipping are not taken into
account.

Contrast with <span class="methodname">CairoContext::pathExtents</span>,
which is similar, but returns non-zero extents for some paths with no
inked area, (such as a simple line segment).

Note that <span class="methodname">CairoContext::fillExtents</span> must
necessarily do more work to compute the precise inked areas in light of
the fill rule, so <span
class="methodname">CairoContext::pathExtents</span> may be more
desirable for sake of performance if the non-inked path extents are
desired.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

An array with the coordinates of the afected area

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">CairoContext::fill</span>
-   <span class="methodname">CairoContext::setFillRule</span>
-   <span class="methodname">CairoContext::fillPreserve</span>

CairoContext::fillPreserve
==========================

cairo\_fill\_preserve
=====================

Fills and preserve the current path

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::fillPreserve</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_fill\_preserve</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

A drawing operator that fills the current path according to the current
<span class="classname">CairoFillRule</span>, (each sub-path is
implicitly closed before being filled). Unlike <span
class="methodname">CairoContext::fill</span>, <span
class="methodname">CairoContext::fillPreserve</span> (Procedural <span
class="function">cairo\_fill</span>, <span
class="function">cairo\_fill\_preserve</span>, respectively) preserves
the path within the Context.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">CairoContext::setFillRule</span>
-   <span class="methodname">CairoContext::fill</span>

CairoContext::fontExtents
=========================

cairo\_font\_extents
====================

Get the font extents

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::fontExtents</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_font\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Gets the font extents for the currently selected font.

### 参数

`context`  
Description...

### 返回值

An array containing the font extents for the current font.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$sur = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);
$con = new CairoContext($sur);

var_dump($con->fontExtents());

?>
```

以上例程的输出类似于：

    array(5) {
      ["ascent"]=>
      float(10)
      ["descent"]=>
      float(3)
      ["height"]=>
      float(13.3125)
      ["max_x_advance"]=>
      float(26.65625)
      ["max_y_advance"]=>
      float(0)
    }

**示例 \#2 过程化风格**

``` php
<?php

$sur = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);
$con = cairo_create($sur);

var_dump(cairo_font_extents($con));

?>
```

以上例程的输出类似于：

    array(5) {
      ["ascent"]=>
      float(10)
      ["descent"]=>
      float(3)
      ["height"]=>
      float(13.3125)
      ["max_x_advance"]=>
      float(26.65625)
      ["max_y_advance"]=>
      float(0)
    }

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getAntialias
==========================

cairo\_get\_antialias
=====================

Retrieves the current antialias mode

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::getAntialias</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_antialias</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Returns the current <span class="classname">CairoAntialias</span> mode,
as set by <span class="methodname">CairoContext::setAntialias</span>.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object created with
<span class="methodname">CairoContext::\_\_construct</span> or <span
class="function">cairo\_create</span>

### 返回值

The current <span class="classname">CairoAntialias</span> mode.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);
$context = new CairoContext($surface);

$context->setAntialias(CairoAntialias::MODE_SUBPIXEL);

var_dump($context->getAntialias());

?>
```

以上例程的输出类似于：

    int(3)

**示例 \#2 过程化风格**

``` php
<?php

$sur = cairo_image_surface_create(CAIRO_FORMAT_ARGB32, 50, 50);
$con = cairo_create($sur);

cairo_set_antialias($con, CAIRO_ANTIALIAS_SUBPIXEL);

var_dump(cairo_get_antialias($con));

?>
```

以上例程的输出类似于：

    int(3)

### 参见

-   <span class="methodname">CairoContext::setAntialias</span>
-   <span class="classname">CairoAntialias</span>

CairoContext::getCurrentPoint
=============================

cairo\_get\_current\_point
==========================

The getCurrentPoint purpose

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::getCurrentPoint</span> ( <span
class="methodparam">void</span> )

过程化风格

<span class="type">array</span> <span
class="methodname">cairo\_get\_current\_point</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Gets the current point of the current path, which is conceptually the
final point reached by the path so far.

The current point is returned in the user-space coordinate system. If
there is no defined current point or if cr is in an error status, x and
y will both be set to 0.0. It is possible to check this in advance with
<span class="methodname">CairoContext::hasCurrentPoint</span>.

Most path construction functions alter the current point. See the
following for details on how they affect the current point: <span
class="methodname">CairoContext::newPath</span>, <span
class="methodname">CairoContext::newSubPath</span>, <span
class="methodname">CairoContext::appendPath</span>, <span
class="methodname">CairoContext::closePath</span>, <span
class="methodname">CairoContext::moveTo</span>, <span
class="methodname">CairoContext::lineTo</span>, <span
class="methodname">CairoContext::curveTo</span>, <span
class="methodname">CairoContext::relMoveTo</span>, <span
class="methodname">CairoContext::relLineTo</span>, <span
class="methodname">CairoContext::relCurveTo</span>, <span
class="methodname">CairoContext::arc</span>, <span
class="methodname">CairoContext::arcNegative</span>, <span
class="methodname">CairoContext::rectangle</span>, <span
class="methodname">CairoContext::textPath</span>, <span
class="methodname">CairoContext::glyphPath</span>.

Some functions use and alter the current point but do not otherwise
change current path: <span
class="methodname">CairoContext::showText</span>.

Some functions unset the current path and as a result, current point:
<span class="methodname">CairoContext::fill</span>, <span
class="methodname">CairoContext::stroke</span>.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object.

### 返回值

An array containing the x (index 0) and y (index 1) coordinates of the
current point.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);

$c->moveTo(10, 10);

var_dump($c->getCurrentPoint());

?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      float(10)
      [1]=>
      float(10)
    }

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

cairo_move_to($c, 10, 10);

var_dump(cairo_get_current_point($c));

?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      float(10)
      [1]=>
      float(10)
    }

### 参见

-   <span class="methodname">CairoContext::moveTo</span>
-   <span class="methodname">CairoContext::hasCurrentPoint</span>

CairoContext::getDash
=====================

cairo\_get\_dash
================

The getDash purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::getDash</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_get\_dash</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getDashCount
==========================

cairo\_get\_dash\_count
=======================

The getDashCount purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::getDashCount</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_dash\_count</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getFillRule
=========================

cairo\_get\_fill\_rule
======================

The getFillRule purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::getFillRule</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_fill\_rule</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getFontFace
=========================

cairo\_get\_font\_face
======================

The getFontFace purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getFontFace</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_face</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getFontMatrix
===========================

cairo\_get\_font\_matrix
========================

The getFontMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getFontMatrix</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getFontOptions
============================

cairo\_get\_font\_options
=========================

The getFontOptions purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getFontOptions</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_options</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getGroupTarget
============================

cairo\_get\_group\_target
=========================

The getGroupTarget purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getGroupTarget</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_group\_target</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getLineCap
========================

cairo\_get\_line\_cap
=====================

The getLineCap purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::getLineCap</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_line\_cap</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getLineJoin
=========================

cairo\_get\_line\_join
======================

The getLineJoin purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::getLineJoin</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_line\_join</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getLineWidth
==========================

cairo\_get\_line\_width
=======================

The getLineWidth purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">CairoContext::getLineWidth</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">float</span> <span
class="methodname">cairo\_get\_line\_width</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getMatrix
=======================

cairo\_get\_matrix
==================

The getMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getMatrix</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getMiterLimit
===========================

cairo\_get\_miter\_limit
========================

The getMiterLimit purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">CairoContext::getMiterLimit</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">float</span> <span
class="methodname">cairo\_get\_miter\_limit</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getOperator
=========================

cairo\_get\_operator
====================

The getOperator purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::getOperator</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_operator</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getScaledFont
===========================

cairo\_get\_scaled\_font
========================

The getScaledFont purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getScaledFont</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_scaled\_font</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getSource
=======================

cairo\_get\_source
==================

The getSource purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getSource</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_source</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getTarget
=======================

cairo\_get\_target
==================

The getTarget purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::getTarget</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_target</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::getTolerance
==========================

cairo\_get\_tolerance
=====================

The getTolerance purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">CairoContext::getTolerance</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">float</span> <span
class="methodname">cairo\_get\_tolerance</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::glyphPath
=======================

cairo\_glyph\_path
==================

The glyphPath purpose

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::glyphPath</span> ( <span
class="methodparam"><span class="type">array</span> `$glyphs`</span> )

过程化风格

<span class="type">void</span> <span
class="methodname">cairo\_glyph\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">array</span> `$glyphs`</span> )

Adds closed paths for the glyphs to the current path. The generated path
if filled, achieves an effect similar to that of <span
class="methodname">CairoContext::showGlyphs</span>.

### 参数

`context`  
A <span class="classname">CairoContext</span> object

`glyphs`  
Array of glyphs

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

CairoContext::hasCurrentPoint
=============================

cairo\_has\_current\_point
==========================

The hasCurrentPoint purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CairoContext::hasCurrentPoint</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">cairo\_has\_current\_point</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Returns whether a current point is defined on the current path. See
<span class="methodname">CairoContext::getCurrentPoint</span> for
details on the current point.

### 参数

`context`  
A valid <span class="classname">CairoContext</span> object.

### 返回值

Whether a current point is defined

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);

var_dump($c->hasCurrentPoint());

$c->moveTo(10, 10);

var_dump($c->hasCurrentPoint());

?>
```

以上例程会输出：

    bool(false)
    bool(true)

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

var_dump(cairo_has_current_point($c));

cairo_move_to($c, 10, 10);

var_dump(cairo_has_current_point($c));

?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">CairoContext::getCurrentPoint</span>

CairoContext::identityMatrix
============================

cairo\_identity\_matrix
=======================

The identityMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::identityMatrix</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_identity\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::inFill
====================

cairo\_in\_fill
===============

The inFill purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CairoContext::inFill</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">cairo\_in\_fill</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::inStroke
======================

cairo\_in\_stroke
=================

The inStroke purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CairoContext::inStroke</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">bool</span> <span
class="methodname">cairo\_in\_stroke</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::lineTo
====================

cairo\_line\_to
===============

The lineTo purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::lineTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_line\_to</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::mask
==================

cairo\_mask
===========

The mask purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::mask</span> ( <span
class="methodparam"><span class="type">CairoPattern</span>
`$pattern`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_mask</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> , <span
class="methodparam"><span class="type">CairoPattern</span>
`$pattern`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`pattern`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::maskSurface
=========================

cairo\_mask\_surface
====================

The maskSurface purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::maskSurface</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> \[, <span class="methodparam"><span
class="type">float</span> `$x`</span> \[, <span
class="methodparam"><span class="type">float</span> `$y`</span> \]\] )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_mask\_surface</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoSurface</span> `$surface`</span> \[, <span
class="methodparam"><span class="type">float</span> `$x`</span> \[,
<span class="methodparam"><span class="type">float</span> `$y`</span>
\]\] )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`surface`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::moveTo
====================

cairo\_move\_to
===============

The moveTo purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::moveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_move\_to</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Begin a new sub-path. After this call the current point will be (x, y).

### 参数

`context`  
A valid CairoContext object.

`x`  
The x coordinate of the new position.

`y`  
The y coordinate of the new position

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

$s = new CairoImageSurface(CairoFormat::ARGB32, 100, 100);
$c = new CairoContext($s);

$c->setSourceRgb(0, 0, 0);
$c->paint();

// Move 10 pixels across, and 10 pixels down
$c->moveTo(10, 10);
$c->lineTo(90, 90);
$c->setLineWidth(2);
$c->setSourceRgb(1, 1, 1);
$c->stroke();

// Move 90 pixels across, and 10 pixels down
$c->moveTo(90, 10);
$c->lineTo(10, 90);
$c->setLineWidth(2);
$c->setSourceRgb(1, 1, 1);
$c->stroke();

$s->writeToPng(dirname(__FILE__) . '/CairoContext_moveTo.png');
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php

$s = cairo_image_surface_create(CAIRO_SURFACE_TYPE_IMAGE, 100, 100);
$c = cairo_create($s);

cairo_set_source_rgb($c, 0, 0, 0);
cairo_paint($c);

// Move 10 pixels across, and 10 pixels down
cairo_move_to($c, 10, 10);
cairo_line_to($c, 90, 90);
cairo_set_line_width($c, 2);
cairo_set_source_rgb($c, 1, 1, 1);
cairo_stroke($c);

// Move 90 pixels across, and 10 pixels down
cairo_move_to($c, 90, 10);
cairo_line_to($c, 10, 90);
cairo_set_line_width($c, 2);
cairo_set_source_rgb($c, 1, 1, 1);
cairo_stroke($c);

cairo_surface_write_to_png($s, dirname(__FILE__) . '/cairo_move_to.png');
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::newPath
=====================

cairo\_new\_path
================

The newPath purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::newPath</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_new\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Clears the current path. After this call there will be no path and no
current point.

### 参数

`context`  
A valid CairoContext object.

### 返回值

没有返回值。

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
// [...]
CairoContext::newPath();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
// [...]
cairo_new_path($context);
?>
```

### 参见

-   <span class="methodname">CairoContext::appendPath</span>
-   <span class="methodname">CairoContext::closePath</span>

CairoContext::newSubPath
========================

cairo\_new\_sub\_path
=====================

The newSubPath purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::newSubPath</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_new\_sub\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::paint
===================

cairo\_paint
============

The paint purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::paint</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_paint</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::paintWithAlpha
============================

cairo\_paint\_with\_alpha
=========================

The paintWithAlpha purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::paintWithAlpha</span> ( <span
class="methodparam"><span class="type">float</span> `$alpha`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_paint\_with\_alpha</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$alpha`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`alpha`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::pathExtents
=========================

cairo\_path\_extents
====================

The pathExtents purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::pathExtents</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_path\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::popGroup
======================

cairo\_pop\_group
=================

The popGroup purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::popGroup</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_pop\_group</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::popGroupToSource
==============================

cairo\_pop\_group\_to\_source
=============================

The popGroupToSource purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::popGroupToSource</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_pop\_group\_to\_source</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::pushGroup
=======================

cairo\_push\_group
==================

The pushGroup purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::pushGroup</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_push\_group</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::pushGroupWithContent
==================================

cairo\_push\_group\_with\_content
=================================

The pushGroupWithContent purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::pushGroupWithContent</span> (
<span class="methodparam"><span class="type">int</span>
`$content`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_push\_group\_with\_content</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`content`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::rectangle
=======================

cairo\_rectangle
================

The rectangle purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::rectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_rectangle</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> , <span class="methodparam"><span
class="type">float</span> `$width`</span> , <span
class="methodparam"><span class="type">float</span> `$height`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::relCurveTo
========================

cairo\_rel\_curve\_to
=====================

The relCurveTo purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::relCurveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$x2`</span> , <span
class="methodparam"><span class="type">float</span> `$y2`</span> , <span
class="methodparam"><span class="type">float</span> `$x3`</span> , <span
class="methodparam"><span class="type">float</span> `$y3`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_rel\_curve\_to</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x1`</span> , <span class="methodparam"><span
class="type">float</span> `$y1`</span> , <span class="methodparam"><span
class="type">float</span> `$x2`</span> , <span class="methodparam"><span
class="type">float</span> `$y2`</span> , <span class="methodparam"><span
class="type">float</span> `$x3`</span> , <span class="methodparam"><span
class="type">float</span> `$y3`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x1`  
Description...

`y1`  
Description...

`x2`  
Description...

`y2`  
Description...

`x3`  
Description...

`y3`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::relLineTo
=======================

cairo\_rel\_line\_to
====================

The relLineTo purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::relLineTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_rel\_line\_to</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::relMoveTo
=======================

cairo\_rel\_move\_to
====================

The relMoveTo purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::relMoveTo</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_rel\_move\_to</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::resetClip
=======================

cairo\_reset\_clip
==================

The resetClip purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::resetClip</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_reset\_clip</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::restore
=====================

cairo\_restore
==============

The restore purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::restore</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_restore</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::rotate
====================

cairo\_rotate
=============

The rotate purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::rotate</span> ( <span
class="methodparam"><span class="type">float</span> `$angle`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_rotate</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$angle`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`angle`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::save
==================

cairo\_save
===========

The save purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::save</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_save</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::scale
===================

cairo\_scale
============

The scale purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::scale</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_scale</span> ( <span class="methodparam"><span
class="type">CairoContext</span> `$context`</span> , <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::selectFontFace
============================

cairo\_select\_font\_face
=========================

The selectFontFace purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::selectFontFace</span> ( <span
class="methodparam"><span class="type">string</span> `$family`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$slant`</span> \[, <span class="methodparam"><span
class="type">int</span> `$weight`</span> \]\] )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_select\_font\_face</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">string</span> `$family`</span> \[, <span
class="methodparam"><span class="type">int</span> `$slant`</span> \[,
<span class="methodparam"><span class="type">int</span> `$weight`</span>
\]\] )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`family`  
Description...

`slant`  
Description...

`weight`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setAntialias
==========================

cairo\_set\_antialias
=====================

The setAntialias purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setAntialias</span> (\[ <span
class="methodparam"><span class="type">int</span> `$antialias`</span> \]
)

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_antialias</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> \[, <span class="methodparam"><span
class="type">int</span> `$antialias`</span> \] )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`antialias`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setDash
=====================

cairo\_set\_dash
================

The setDash purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setDash</span> ( <span
class="methodparam"><span class="type">array</span> `$dashes`</span> \[,
<span class="methodparam"><span class="type">float</span>
`$offset`</span> \] )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_dash</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">array</span> `$dashes`</span> \[, <span
class="methodparam"><span class="type">float</span> `$offset`</span> \]
)

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`dashes`  
Description...

`offset`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setFillRule
=========================

cairo\_set\_fill\_rule
======================

The setFillRule purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setFillRule</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_fill\_rule</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$setting`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`setting`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setFontFace
=========================

cairo\_set\_font\_face
======================

The setFontFace purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setFontFace</span> ( <span
class="methodparam"><span class="type">CairoFontFace</span>
`$fontface`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_font\_face</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoFontFace</span> `$fontface`</span> )

Sets the font-face for a given context.

### 参数

`context`  
A CairoContext object to change the font-face for.

`fontface`  
A CairoFontFace object

### 返回值

No value is returned

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
// New surface with white background
$s = new CairoImageSurface(CairoFormat::ARGB32, 300, 100);
$c = new CairoContext($s);
$c->setSourceRgb(1, 1, 1);
$c->paint();

// Draw some text
$c->setSourceRgb(0, 0, 0);
$c->moveTo(10, 60);
// Create a new font face
$f = new CairoToyFontFace("sans-serif", CairoFontSlant::NORMAL, CairoFontWeight::NORMAL);
$c->setFontFace($f);
$c->setFontSize(30);
$c->showText('Hello, World!');
$s->writeToPng(dirname(__FILE__) . '/setFontFace.png');
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

### 参见

-   <span class="methodname">CairoContext::setFontSize</span>
-   <span class="methodname">CairoContext::showText</span>

CairoContext::setFontMatrix
===========================

cairo\_set\_font\_matrix
========================

The setFontMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setFontMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_font\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`matrix`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setFontOptions
============================

cairo\_set\_font\_options
=========================

The setFontOptions purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setFontOptions</span> ( <span
class="methodparam"><span class="type">CairoFontOptions</span>
`$fontoptions`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_font\_options</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoFontOptions</span> `$fontoptions`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`fontoptions`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setFontSize
=========================

cairo\_set\_font\_size
======================

The setFontSize purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setFontSize</span> ( <span
class="methodparam"><span class="type">float</span> `$size`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_font\_size</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$size`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`size`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setLineCap
========================

cairo\_set\_line\_cap
=====================

The setLineCap purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setLineCap</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_line\_cap</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$setting`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`setting`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setLineJoin
=========================

cairo\_set\_line\_join
======================

The setLineJoin purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setLineJoin</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_line\_join</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$setting`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`setting`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setLineWidth
==========================

cairo\_set\_line\_width
=======================

The setLineWidth purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setLineWidth</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_line\_width</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$width`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`width`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setMatrix
=======================

cairo\_set\_matrix
==================

The setMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`matrix`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setMiterLimit
===========================

cairo\_set\_miter\_limit
========================

The setMiterLimit purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setMiterLimit</span> ( <span
class="methodparam"><span class="type">float</span> `$limit`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_miter\_limit</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$limit`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`limit`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setOperator
=========================

cairo\_set\_operator
====================

The setOperator purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setOperator</span> ( <span
class="methodparam"><span class="type">int</span> `$setting`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_operator</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">int</span> `$setting`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`setting`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setScaledFont
===========================

cairo\_set\_scaled\_font
========================

The setScaledFont purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setScaledFont</span> ( <span
class="methodparam"><span class="type">CairoScaledFont</span>
`$scaledfont`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_scaled\_font</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoScaledFont</span> `$scaledfont`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`scaledfont`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setSource
=======================

cairo\_set\_source
==================

The setSource purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setSource</span> ( <span
class="methodparam"><span class="type">CairoPattern</span>
`$pattern`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_source</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoPattern</span> `$pattern`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`pattern`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setSourceRGB
==========================

cairo\_set\_source
==================

The setSourceRGB purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setSourceRGB</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_source</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
)

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`red`  
Description...

`green`  
Description...

`blue`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setSourceRGBA
===========================

cairo\_set\_source
==================

The setSourceRGBA purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setSourceRGBA</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> , <span
class="methodparam"><span class="type">float</span> `$alpha`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_source</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
, <span class="methodparam"><span class="type">float</span>
`$alpha`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`red`  
Description...

`green`  
Description...

`blue`  
Description...

`alpha`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setSourceSurface
==============================

cairo\_set\_source\_surface
===========================

The setSourceSurface purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setSourceSurface</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> \[, <span class="methodparam"><span
class="type">float</span> `$x`</span> \[, <span
class="methodparam"><span class="type">float</span> `$y`</span> \]\] )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_source\_surface</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoSurface</span> `$surface`</span> \[, <span
class="methodparam"><span class="type">float</span> `$x`</span> \[,
<span class="methodparam"><span class="type">float</span> `$y`</span>
\]\] )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`surface`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::setTolerance
==========================

cairo\_set\_tolerance
=====================

The setTolerance purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::setTolerance</span> ( <span
class="methodparam"><span class="type">float</span> `$tolerance`</span>
)

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_tolerance</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$tolerance`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`tolerance`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::showPage
======================

cairo\_show\_page
=================

The showPage purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::showPage</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_show\_page</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::showText
======================

cairo\_show\_text
=================

The showText purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::showText</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_show\_text</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`text`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::status
====================

cairo\_status
=============

The status purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoContext::status</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_status</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::stroke
====================

cairo\_stroke
=============

The stroke purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::stroke</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_stroke</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::strokeExtents
===========================

cairo\_stroke\_extents
======================

The strokeExtents purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::strokeExtents</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_stroke\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::strokePreserve
============================

cairo\_stroke\_preserve
=======================

The strokePreserve purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::strokePreserve</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_stroke\_preserve</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::textExtents
=========================

cairo\_text\_extents
====================

The textExtents purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::textExtents</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_text\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`text`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::textPath
======================

cairo\_text\_path
=================

The textPath purpose

### 说明

面向对象风格

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::textPath</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

过程化风格

<span class="type">void</span> <span
class="methodname">cairo\_text\_path</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

Adds closed paths for text to the current path. The generated path, if
filled, achieves an effect similar to that of <span
class="methodname">CairoContext::showText</span>.

Text conversion and positioning is done similar to <span
class="methodname">CairoContext::showText</span>.

Like <span class="methodname">CairoContext::showText</span>, after this
call the current point is moved to the origin of where the next glyph
would be placed in this same progression. That is, the current point
will be at the origin of the final glyph offset by its advance values.
This allows for chaining multiple calls to <span
class="methodname">CairoContext::showText</span> without having to set
current point in between.

Note: The <span class="methodname">CairoContext::textPath</span>
function call is part of what the cairo designers call the "toy" text
API. It is convenient for short demos and simple programs, but it is not
expected to be adequate for serious text-using applications. See <span
class="methodname">CairoContext::glyphPath</span> for the "real" text
path API in cairo.

### 参数

`context`  
A <span class="classname">CairoContext</span> object

`text`  
Description...

`string`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::transform
=======================

cairo\_transform
================

The transform purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::transform</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_transform</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`matrix`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::translate
=======================

cairo\_translate
================

The translate purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoContext::translate</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_translate</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::userToDevice
==========================

cairo\_user\_to\_device
=======================

The userToDevice purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::userToDevice</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_user\_to\_device</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoContext::userToDeviceDistance
==================================

cairo\_user\_to\_device\_distance
=================================

The userToDeviceDistance purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoContext::userToDeviceDistance</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_user\_to\_device\_distance</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

<span class="classname">Exception</span> class thrown by <span
class="classname">Cairo</span> functions and methods

类摘要
------

**CairoException**

<span class="ooclass"> class **CairoException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

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

<span class="classname">CairoStatus</span> is used to indicate errors
that can occur when using Cairo. In some cases it is returned directly
by functions. but when using <span
class="classname">CairoContext</span>, the last error, if any, is stored
in the object and can be retrieved with <span
class="methodname">CairoContext::status</span> or <span
class="function">cairo\_status</span>. New entries may be added in
future versions.

Use <span class="methodname">Cairo::statusToString</span> or <span
class="function">cairo\_status\_to\_string</span> to get a
human-readable representation of an error message.

类摘要
------

**CairoStatus**

<span class="ooclass"> class **CairoStatus** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::SUCCESS` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::NO_MEMORY` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_RESTORE` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_POP_GROUP` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::NO_CURRENT_POINT` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_MATRIX` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_STATUS` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::NULL_POINTER` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_STRING` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_PATH_DATA` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::READ_ERROR` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::WRITE_ERROR` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::SURFACE_FINISHED` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::SURFACE_TYPE_MISMATCH` <span class="initializer"> =
13</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::PATTERN_TYPE_MISMATCH` <span class="initializer"> =
14</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_CONTENT` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_FORMAT` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_VISUAL` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::FILE_NOT_FOUND` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_DASH` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_DSC_COMMENT` <span class="initializer"> =
20</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_INDEX` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::CLIP_NOT_REPRESENTABLE` <span class="initializer"> =
22</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::TEMP_FILE_ERROR` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoStatus::INVALID_STRIDE` <span class="initializer"> = 24</span> ;

}

预定义常量
----------

**`CairoStatus::SUCCESS`**  
No error has occurred

**`CairoStatus::NO_MEMORY`**  
Out of memory

**`CairoStatus::INVALID_RESTORE`**  
<span class="function">cairo\_restore</span> called without matching
<span class="function">cairo\_save</span>

**`CairoStatus::INVALID_POP_GROUP`**  
No saved group to pop

**`CairoStatus::NO_CURRENT_POINT`**  
No current point defined

**`CairoStatus::INVALID_MATRIX`**  
Invalid matrix (not invertible)

**`CairoStatus::INVALID_STATUS`**  
Invalid value for an input CairoStatus\>

**`CairoStatus::NULL_POINTER`**  
Null pointer

**`CairoStatus::INVALID_STRING`**  
Input string not valid UTF-8 string

**`CairoStatus::INVALID_PATH_DATA`**  
Input path data not valid

**`CairoStatus::READ_ERROR`**  
Error while reading from input stream

**`CairoStatus::WRITE_ERROR`**  
Error while writing to output stream

**`CairoStatus::SURFACE_FINISHED`**  
Target surface has been finished

**`CairoStatus::SURFACE_TYPE_MISMATCH`**  
The surface type is not appropriate for the operation

**`CairoStatus::PATTERN_TYPE_MISMATCH`**  
The pattern type is not appropriate for the operation

**`CairoStatus::INVALID_CONTENT`**  
Invalid value for an input <span class="classname">CairoContent</span>

**`CairoStatus::INVALID_FORMAT`**  
Invalid value for an input <span class="classname">CairoFormat</span>

**`CairoStatus::INVALID_VISUAL`**  
Invalid value for an input Visual

**`CairoStatus::FILE_NOT_FOUND`**  
File not found

**`CairoStatus::INVALID_DASH`**  
Invalid value for a dash setting

**`CairoStatus::INVALID_DSC_COMMENT`**  
Invalid value for a DSC comment

**`CairoStatus::INVALID_INDEX`**  
Invalid index passed to getter

**`CairoStatus::CLIP_NOT_REPRESENTABLE`**  
Clip region not representable in desired format

**`CairoStatus::TEMP_FILE_ERROR`**  
Error creating or writing to a temporary file

**`CairoStatus::INVALID_STRIDE`**  
Invalid value for <span class="classname">CairoStride</span>

简介
----

This is the base-class for all other Surface types. CairoSurface is the
abstract type representing all different drawing targets that cairo can
render to. The actual drawings are performed using a CairoContext.

类摘要
------

**CairoSurface**

<span class="ooclass"> class **CairoSurface** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">copyPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">createSimilar</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$other`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> , <span
class="methodparam"><span class="type">string</span> `$width`</span> ,
<span class="methodparam"><span class="type">string</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">finish</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getDeviceOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">markDirty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">markDirtyRectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setDeviceOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFallbackResolution</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">showPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">writeToPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

}

CairoSurface::\_\_construct
===========================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoSurface::\_\_construct</span> ( <span
class="methodparam">void</span> )

CairoSurface is an abstract type and, as such, should not be
instantiated in your PHP scripts.

### 参数

此函数没有参数。

### 返回值

No return value

### 注释

> **Note**:
>
> If you're using a PHP version before 5.3, you must destroy the <span
> class="classname">CairoContext</span> associated with a <span
> class="classname">CairoSurface</span> *after* you destroy the
> CairoSurface. Otherwise, you're left with a Circular-reference memory
> leak.

### 参见

-   <span class="methodname">CairoImageSurface::\_\_construct</span>

CairoSurface::copyPage
======================

cairo\_copy\_page
=================

The copyPage purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::copyPage</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_copy\_page</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Emits the current page for backends that support multiple pages, but
doesn't clear it, so that the contents of the current page will be
retained for the next page. Use CairoSurface::showPage() if you want to
get an empty page after the emission.

### 参数

`context`  
A CairoContext object

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::createSimilar
===========================

The createSimilar purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::createSimilar</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$other`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> , <span
class="methodparam"><span class="type">string</span> `$width`</span> ,
<span class="methodparam"><span class="type">string</span>
`$height`</span> )

Create a new surface that is as compatible as possible with an existing
surface. For example the new surface will have the same fallback
resolution and font options as other. Generally, the new surface will
also use the same backend as other, unless that is not possible for some
reason. The type of the returned surface may be examined with
CairoSurface::getType(). Initially the surface contents are all 0
(transparent if contents have transparency, black otherwise.)

### 参数

`other`  
An existing surface used to select the backend of the new surface

`content`  
The content for the new surface. See the CairoContent class for possible
values.

`width`  
Width of the new surface, (in device-space units).

`height`  
Height of the new surface, (in device-space units).

### 返回值

A new CairoSurface

### 范例

**示例 \#1 <span class="methodname">CairoSurface::createSimilar</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">CairoContent</span>

CairoSurface::finish
====================

The finish purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::finish</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::finish</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::flush
===================

The flush purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::flush</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::flush</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::getContent
========================

The getContent purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getContent</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::getContent</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::getDeviceOffset
=============================

The getDeviceOffset purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoSurface::getDeviceOffset</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::getDeviceOffset</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::getFontOptions
============================

cairo\_get\_font\_options
=========================

The getFontOptions purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::getFontOptions</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_options</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::getType
=====================

The getType purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getType</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::getType</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::markDirty
=======================

The markDirty purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirty</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::markDirty</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::markDirtyRectangle
================================

The markDirtyRectangle purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirtyRectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`x`  
Description...

`y`  
Description...

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurface::markDirtyRectangle</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::setDeviceOffset
=============================

The setDeviceOffset purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setDeviceOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::setDeviceOffset</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::setFallbackResolution
===================================

The setFallbackResolution purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setFallbackResolution</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`x`  
Description...

`y`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurface::setFallbackResolution</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::showPage
======================

cairo\_show\_page
=================

The showPage purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::showPage</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_show\_page</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::status
====================

cairo\_status
=============

The status purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::status</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_status</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurface::writeToPng
========================

The writeToPng purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::writeToPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`file`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSurface::writeToPng</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

Svg specific surface class, uses the SVG (standard vector graphics)
surface backend.

类摘要
------

**CairoSvgSurface**

<span class="ooclass"> class **CairoSvgSurface** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoSurface**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getVersions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">restrictToVersion</span> ( <span
class="methodparam"><span class="type">int</span> `$version`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">versionToString</span> ( <span
class="methodparam"><span class="type">int</span> `$version`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoSurface::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::copyPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::createSimilar</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$other`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> , <span
class="methodparam"><span class="type">string</span> `$width`</span> ,
<span class="methodparam"><span class="type">string</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::finish</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoSurface::getDeviceOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirtyRectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setDeviceOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setFallbackResolution</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::showPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::status</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::writeToPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

}

CairoSvgSurface::\_\_construct
==============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoSvgSurface::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`file`  
Description...

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSvgSurface::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSvgSurface::getVersions
============================

cairo\_svg\_surface\_get\_versions
==================================

Used to retrieve a list of supported SVG versions

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">CairoSvgSurface::getVersions</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_svg\_get\_versions</span> ( <span
class="methodparam">void</span> )

Returns a numerically indexed array of currently available <span
class="classname">CairoSvgVersion</span> constants. In order to retrieve
the string values for each item, use <span
class="methodname">CairoSvgSurface::versionToString</span>.

### 参数

此函数没有参数。

### 返回值

Returns a numerically indexed array of integer values.

### 范例

**示例 \#1 <span class="methodname">CairoSvgSurface::getVersions</span>
example**

``` php
<?php
/* Grab our list of versions */
$versions = CairoSvgSurface::getVersions();
var_dump($versions);

/* echo the string name of each version */
foreach($versions as $id) {
    echo CairoSvgSurface::versionToString($id), PHP_EOL;
}
?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      int(0)
      [1]=>
      int(1)
    }
    SVG 1.1
    SVG 1.2

**示例 \#2 过程化风格**

``` php
<?php
/* Grab our list of versions */
$versions = cairo_svg_surface_get_versions();
var_dump($versions);

/* echo the string name of each version */
foreach($versions as $id) {
    echo cairo_svg_surface_version_to_string($id), PHP_EOL;
}
?>
```

以上例程的输出类似于：

    array(2) {
      [0]=>
      int(0)
      [1]=>
      int(1)
    }
    SVG 1.1
    SVG 1.2

### 参见

-   <span class="methodname">CairoSvgSurface::versionToString</span>

CairoSvgSurface::restrictToVersion
==================================

The restrictToVersion purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSvgSurface::restrictToVersion</span> (
<span class="methodparam"><span class="type">int</span>
`$version`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`version`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSvgSurface::restrictToVersion</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSvgSurface::versionToString
================================

The versionToString purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">CairoSvgSurface::versionToString</span> ( <span
class="methodparam"><span class="type">int</span> `$version`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`version`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSvgSurface::versionToString</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

CairoImageSurface provide the ability to render to memory buffers either
allocated by cairo or by the calling code. The supported image formats
are those defined in <span class="classname">CairoFormat</span>.

类摘要
------

**CairoImageSurface**

<span class="ooclass"> class **CairoImageSurface** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoSurface**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span>
`$height`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">createForData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$format`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> , <span class="methodparam"><span
class="type">int</span> `$height`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">CairoImageSurface</span> <span
class="methodname">createFromPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getData</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFormat</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getHeight</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getStride</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getWidth</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoSurface::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::copyPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::createSimilar</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$other`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> , <span
class="methodparam"><span class="type">string</span> `$width`</span> ,
<span class="methodparam"><span class="type">string</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::finish</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoSurface::getDeviceOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirtyRectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setDeviceOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setFallbackResolution</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::showPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::status</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::writeToPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

}

CairoImageSurface::\_\_construct
================================

Creates a new CairoImageSurface

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoImageSurface::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span>
`$height`</span> )

Creates a new CairoImageSuface object of type `format`

### 参数

`format`  
Can be any defined in <span class="classname">CairoFormat</span>

`width`  
The width of the image surface

`height`  
The height of the image surface

### 返回值

A new CairoImageSurface

### 范例

**示例 \#1 <span
class="methodname">CairoImageSurface::\_\_construct</span> example**

``` php
<?php

// Creates a image with ARGB32 format of 50 width and 50 height
$surface = new CairoImageSurface(CairoFormat::ARGB32, 50,50);

?>
```

### 参见

-   <span class="methodname">CairoContext::\_\_construct</span>

CairoImageSurface::createForData
================================

The createForData purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">CairoImageSurface::createForData</span> ( <span
class="methodparam"><span class="type">string</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$format`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> , <span class="methodparam"><span
class="type">int</span> `$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`data`  
Description...

`format`  
Description...

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoImageSurface::createForData</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoImageSurface::createFromPng
================================

Creates a new CairoImageSurface form a png image file

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span
class="type">CairoImageSurface</span> <span
class="methodname">CairoImageSurface::createFromPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

Creates a new CairoImageSurface form a png image file

This method should be called static

### 参数

`file`  
Path to PNG image file

### 返回值

<span class="classname">CairoImageSurface</span> object

### 范例

**示例 \#1 <span
class="methodname">CairoImageSurface::createFromPng</span> example**

``` php
<?php

$surface = CairoImageSurface::createFromPng('/path/to/image/file.png');

?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">CairoImageSurface::\_\_construct</span>

CairoImageSurface::getData
==========================

Gets the image data as string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">CairoImageSurface::getData</span> ( <span
class="methodparam">void</span> )

Returns the image data of this surface or NULL if surface is not an
image surface, or if <span
class="methodname">CairoContext::finish</span>, procedural : <span
class="function">cairo\_surface\_finish</span>, has been called.

### 参数

此函数没有参数。

### 返回值

The image data as string

### 范例

**示例 \#1 <span class="methodname">CairoImageSurface::getData</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">CairoImageSurface::getStride</span>

CairoImageSurface::getFormat
============================

Get the image format

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoImageSurface::getFormat</span> ( <span
class="methodparam">void</span> )

Retrieves the image format, as one of the <span
class="classname">CairoFormat</span> defined

### 参数

此函数没有参数。

### 返回值

One of the <span class="classname">CairoFormat</span> enums

### 范例

**示例 \#1 <span class="methodname">CairoImageSurface::getFormat</span>
example**

``` php
<?php

$surface = new CairoImageSurface(CairoFormat::ARGB32, 50, 50);

var_dump($surface->getFormat()); // 0

$surface2 = new CairoImageSurface(CairoFormat::A8, 50, 50);

var_dump($surface2->getFormat()); // 2

?>
```

以上例程的输出类似于：

    int(0)
    int(2)

### 参见

-   <span class="methodname">CairoImageSurface::getHeight</span>
-   <span class="methodname">CairoImageSurface::getWidth</span>

CairoImageSurface::getHeight
============================

Retrieves the height of the CairoImageSurface

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoImageSurface::getHeight</span> ( <span
class="methodparam">void</span> )

This methods returns the <span
class="classname">CairoImageSurface</span> height.

### 参数

此函数没有参数。

### 返回值

CairoImageSurface object height

### 范例

**示例 \#1 <span class="methodname">CairoImageSurface::getHeight</span>
example**

``` php
<?php
// creates a new image surface
$surface = new CairoImageSurface(CairoFormat::ARGB32, 80, 50);

//gets the height
var_dump($surface->getHeight());

?>
```

以上例程的输出类似于：

    int(50)

### 参见

-   <span class="methodname">CairoImageSurface::getWidth</span>

CairoImageSurface::getStride
============================

The getStride purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoImageSurface::getStride</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoImageSurface::getStride</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoImageSurface::getWidth
===========================

Retrieves the width of the CairoImageSurface

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoImageSurface::getWidth</span> ( <span
class="methodparam">void</span> )

Gets the width of the <span class="classname">CairoImageSurface</span>

### 参数

此函数没有参数。

### 返回值

Returns the width of the CairoImageSurface object

### 范例

**示例 \#1 <span class="methodname">CairoImageSurface::getWidth</span>
example**

``` php
<?php
// creates a new image surface
$surface = new CairoImageSurface(CairoFormat::ARGB32, 80, 50);

//gets the width
var_dump($surface->getWidth());

?>
```

以上例程的输出类似于：

    int(80)

### 参见

-   <span class="methodname">CairoImageSurface::getHeight</span>

简介
----

类摘要
------

**CairoPdfSurface**

<span class="ooclass"> class **CairoPdfSurface** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoSurface**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSize</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoSurface::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::copyPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::createSimilar</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$other`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> , <span
class="methodparam"><span class="type">string</span> `$width`</span> ,
<span class="methodparam"><span class="type">string</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::finish</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoSurface::getDeviceOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirtyRectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setDeviceOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setFallbackResolution</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::showPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::status</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::writeToPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

}

CairoPdfSurface::\_\_construct
==============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoPdfSurface::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`file`  
Description...

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoPdfSurface::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPdfSurface::setSize
========================

The setSize purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPdfSurface::setSize</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPdfSurface::setSize</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

类摘要
------

**CairoPsSurface**

<span class="ooclass"> class **CairoPsSurface** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoSurface**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dscBeginPageSetup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dscBeginSetup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">dscComment</span> ( <span
class="methodparam"><span class="type">string</span> `$comment`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getEps</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">getLevels</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">levelToString</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">restrictToLevel</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setEps</span> ( <span class="methodparam"><span
class="type">bool</span> `$level`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSize</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoSurface::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::copyPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::createSimilar</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$other`</span> , <span class="methodparam"><span
class="type">int</span> `$content`</span> , <span
class="methodparam"><span class="type">string</span> `$width`</span> ,
<span class="methodparam"><span class="type">string</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::finish</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::flush</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoSurface::getDeviceOffset</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::markDirtyRectangle</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> , <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setDeviceOffset</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::setFallbackResolution</span> (
<span class="methodparam"><span class="type">float</span> `$x`</span> ,
<span class="methodparam"><span class="type">float</span> `$y`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::showPage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurface::status</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurface::writeToPng</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

}

CairoPsSurface::\_\_construct
=============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoPsSurface::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">float</span>
`$width`</span> , <span class="methodparam"><span
class="type">float</span> `$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`file`  
Description...

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::\_\_construct</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::dscBeginPageSetup
=================================

The dscBeginPageSetup purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPsSurface::dscBeginPageSetup</span> (
<span class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoPsSurface::dscBeginPageSetup</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::dscBeginSetup
=============================

The dscBeginSetup purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPsSurface::dscBeginSetup</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::dscBeginSetup</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::dscComment
==========================

The dscComment purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPsSurface::dscComment</span> ( <span
class="methodparam"><span class="type">string</span> `$comment`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`comment`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::dscComment</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::getEps
======================

The getEps purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CairoPsSurface::getEps</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::getEps</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::getLevels
=========================

The getLevels purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">CairoPsSurface::getLevels</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::getLevels</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::levelToString
=============================

The levelToString purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">CairoPsSurface::levelToString</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`level`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::levelToString</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::restrictToLevel
===============================

The restrictToLevel purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPsSurface::restrictToLevel</span> ( <span
class="methodparam"><span class="type">int</span> `$level`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`level`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoPsSurface::restrictToLevel</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::setEps
======================

The setEps purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPsSurface::setEps</span> ( <span
class="methodparam"><span class="type">bool</span> `$level`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`level`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::setEps</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPsSurface::setSize
=======================

The setSize purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPsSurface::setSize</span> ( <span
class="methodparam"><span class="type">float</span> `$width`</span> ,
<span class="methodparam"><span class="type">float</span>
`$height`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`width`  
Description...

`height`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPsSurface::setSize</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

类摘要
------

**CairoSurfaceType**

<span class="ooclass"> class **CairoSurfaceType** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::IMAGE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::PDF` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::PS` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::XLIB` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::XCB` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::GLITZ` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::QUARTZ` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::WIN32` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::BEOS` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::DIRECTFB` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::SVG` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::OS2` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::WIN32_PRINTING` <span class="initializer"> =
12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSurfaceType::QUARTZ_IMAGE` <span class="initializer"> = 13</span>
;

}

预定义常量
----------

**`CairoSurfaceType::IMAGE`**  
Description here...

**`CairoSurfaceType::PDF`**  
Description here...

**`CairoSurfaceType::PS`**  
Description here...

**`CairoSurfaceType::XLIB`**  
Description here...

**`CairoSurfaceType::XCB`**  
Description here...

**`CairoSurfaceType::GLITZ`**  
Description here...

**`CairoSurfaceType::QUARTZ`**  
Description here...

**`CairoSurfaceType::WIN32`**  
Description here...

**`CairoSurfaceType::BEOS`**  
Description here...

**`CairoSurfaceType::DIRECTFB`**  
Description here...

**`CairoSurfaceType::SVG`**  
Description here...

**`CairoSurfaceType::OS2`**  
Description here...

**`CairoSurfaceType::WIN32_PRINTING`**  
Description here...

**`CairoSurfaceType::QUARTZ_IMAGE`**  
Description here...

简介
----

CairoFontFace abstract class represents a particular font at a
particular weight, slant, and other characteristic but no transformation
or size.

Note: This class can not be instantiated directly, it is created by
<span class="methodname">CairoContext::getFontFace</span> or <span
class="function">cairo\_scaled\_font\_get\_font\_face</span>.

类摘要
------

**CairoFontFace**

<span class="ooclass"> class **CairoFontFace** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

}

CairoFontFace::\_\_construct
============================

Creates a new CairoFontFace object

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoFontFace::\_\_construct</span> ( <span
class="methodparam">void</span> )

CairoFontFace class represents a particular font at a particular weight,
slant, and other characteristic but no transformation or size.

Note: This class can't be instantiated directly it is created by <span
class="methodname">CairoContext::getFontFace</span> or <span
class="function">cairo\_scaled\_font\_get\_font\_face</span>

### 参数

此函数没有参数。

### 返回值

<span class="classname">CairoFontFace</span>

### 范例

**示例 \#1 <span class="methodname">CairoFontFace::\_\_construct</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Class::Method</span>

CairoFontFace::getType
======================

cairo\_font\_face\_get\_type
============================

Retrieves the font face type

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontFace::getType</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_font\_face\_get\_type</span> ( <span
class="methodparam"><span class="type">CairoFontFace</span>
`$fontface`</span> )

This function returns the type of the backend used to create a font
face. See <span class="classname">CairoFontType</span> class constants
for available types.

### 参数

此函数没有参数。

### 返回值

A font type that can be any one defined in <span
class="classname">CairoFontType</span>

### 范例

**示例 \#1 <span class="methodname">CairoFontFace::getType</span>
example**

``` php
<?php

// Creates the font face
$fontface = new CairoToyFontFace('sans-serif');

// Get the font face type
var_dump($fontface->getType());

?>
```

以上例程的输出类似于：

    int(0)

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontFace::status
=====================

cairo\_font\_face\_status
=========================

Check for CairoFontFace errors

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontFace::status</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_font\_face\_status</span> ( <span
class="methodparam"><span class="type">CairoFontFace</span>
`$fontface`</span> )

Checks whether an error has previously occurred for this font face

### 参数

`fontface`  
A valid CairoFontFace object

### 返回值

CAIRO\_STATUS\_SUCCESS or another error such as
CAIRO\_STATUS\_NO\_MEMORY.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php

// Creates the font face
$fontface = new CairoToyFontFace('sans-serif');

// Get the font face status
var_dump($fontface->status()); // should be the value of CAIRO_STATUS_SUCCESS

?>
```

以上例程的输出类似于：

    int(0)

**示例 \#2 过程化风格**

``` php
<?php

// Creates the font face
$fontface = new CairoToyFontFace('sans-serif');

// Get the font face status
var_dump(cairo_font_face_status($fontface)); // should be the value of CAIRO_STATUS_SUCCESS

?>
```

以上例程的输出类似于：

    int(0)

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

An opaque structure holding all options that are used when rendering
fonts.

Individual features of a cairo\_font\_options\_t can be set or accessed
using functions named cairo\_font\_options\_set\_feature\_name and
cairo\_font\_options\_get\_feature\_name, like
cairo\_font\_options\_set\_antialias() and
cairo\_font\_options\_get\_antialias().

New features may be added to <span
class="classname">CairoFontOptions</span> in the future. For this reason
<span class="methodname">CairoFontOptions::copy</span>, <span
class="methodname">CairoFontOptions::equal</span>, <span
class="methodname">CairoFontOptions::merge</span>, <span
class="methodname">CairoFontOptions::hash</span>
(cairo\_font\_options\_copy(), cairo\_font\_options\_equal(),
cairo\_font\_options\_merge(), and cairo\_font\_options\_hash() in
procedural way) should be used to copy, check for equality, merge, or
compute a hash value of <span class="classname">CairoFontOptions</span>
objects.

类摘要
------

**CairoFontOptions**

<span class="ooclass"> class **CairoFontOptions** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">equal</span> ( <span class="methodparam"><span
class="type">CairoFontOptions</span> `$other`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getAntialias</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getHintMetrics</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getHintStyle</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSubpixelOrder</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">hash</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">CairoFontOptions</span> `$other`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setAntialias</span> ( <span
class="methodparam"><span class="type">int</span> `$antialias`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setHintMetrics</span> ( <span
class="methodparam"><span class="type">int</span> `$hint_metrics`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setHintStyle</span> ( <span
class="methodparam"><span class="type">int</span> `$hint_style`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSubpixelOrder</span> ( <span
class="methodparam"><span class="type">int</span>
`$subpixel_order`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

}

CairoFontOptions::\_\_construct
===============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoFontOptions::\_\_construct</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::equal
=======================

The equal purpose

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">CairoFontOptions::equal</span> ( <span
class="methodparam"><span class="type">CairoFontOptions</span>
`$other`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`other`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoFontOptions::equal</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::getAntialias
==============================

cairo\_get\_antialias
=====================

The getAntialias purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontOptions::getAntialias</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_get\_antialias</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::getHintMetrics
================================

The getHintMetrics purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontOptions::getHintMetrics</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::getHintMetrics</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::getHintStyle
==============================

The getHintStyle purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontOptions::getHintStyle</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::getHintStyle</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::getSubpixelOrder
==================================

The getSubpixelOrder purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontOptions::getSubpixelOrder</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::getSubpixelOrder</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::hash
======================

The hash purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontOptions::hash</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoFontOptions::hash</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::merge
=======================

The merge purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoFontOptions::merge</span> ( <span
class="methodparam"><span class="type">CairoFontOptions</span>
`$other`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`other`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoFontOptions::merge</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::setAntialias
==============================

cairo\_set\_antialias
=====================

The setAntialias purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoFontOptions::setAntialias</span> ( <span
class="methodparam"><span class="type">int</span> `$antialias`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_antialias</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> \[, <span class="methodparam"><span
class="type">int</span> `$antialias`</span> \] )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`antialias`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::setHintMetrics
================================

The setHintMetrics purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoFontOptions::setHintMetrics</span> ( <span
class="methodparam"><span class="type">int</span> `$hint_metrics`</span>
)

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`hint_metrics`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::setHintMetrics</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::setHintStyle
==============================

The setHintStyle purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoFontOptions::setHintStyle</span> ( <span
class="methodparam"><span class="type">int</span> `$hint_style`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`hint_style`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::setHintStyle</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::setSubpixelOrder
==================================

The setSubpixelOrder purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoFontOptions::setSubpixelOrder</span> (
<span class="methodparam"><span class="type">int</span>
`$subpixel_order`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`subpixel_order`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoFontOptions::setSubpixelOrder</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoFontOptions::status
========================

cairo\_status
=============

The status purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoFontOptions::status</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_status</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

Specifies variants of a font face based on their slant.

类摘要
------

**CairoFontSlant**

<span class="ooclass"> class **CairoFontSlant** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontSlant::NORMAL` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontSlant::ITALIC` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontSlant::OBLIQUE` <span class="initializer"> = 2</span> ;

}

预定义常量
----------

**`CairoFontSlant::NORMAL`**  
Upright font style

**`CairoFontSlant::ITALIC`**  
Italic font style

**`CairoFontSlant::OBLIQUE`**  
Oblique font style

简介
----

CairoFontType class is an abstract final class that contains constants
used to describe the type of a given <span
class="classname">CairoFontFace</span> or <span
class="classname">CairoScaledFont</span>. The font types are also known
as "font backends" within cairo.

The type of a CairoFontFace is determined by the how it is created, an
example would be the <span
class="methodname">CairoToyFontFace::\_\_construct</span>. The <span
class="classname">CairoFontFace</span> type can be queried with <span
class="methodname">CairoFontFace::getType</span> or <span
class="function">cairo\_font\_face\_get\_type</span>

The various <span class="classname">CairoFontFace</span> functions can
be used with a font face of any type.

The type of a <span class="classname">CairoScaledFont</span> is
determined by the type of the <span
class="classname">CairoFontFace</span> passed to <span
class="methodname">CairoScaledFont::\_\_construct</span> or <span
class="function">cairo\_scaled\_font\_create</span>. The scaled font
type can be queried with <span
class="methodname">CairoScaledFont::getType</span> or <span
class="function">cairo\_scaled\_font\_get\_type</span>.

类摘要
------

**CairoFontType**

<span class="ooclass"> class **CairoFontType** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontType::TOY` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontType::FT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontType::WIN32` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontType::QUARTZ` <span class="initializer"> = 3</span> ;

}

预定义常量
----------

**`CairoFontType::TOY`**  
The font was created using <span class="classname">CairoToyFont</span>
api

**`CairoFontType::FT`**  
The font is of type <span class="classname">CairoFreeType</span>

**`CairoFontType::WIN32`**  
The font is of type Win32

**`CairoFontType::QUARTZ`**  
The font is of type Quartz

**`CairoFontType::USER`**  
The font was create using cairo's user font api

简介
----

Specifies variants of a font face based on their weight.

类摘要
------

**CairoFontWeight**

<span class="ooclass"> class **CairoFontWeight** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontWeight::NORMAL` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFontWeight::BOLD` <span class="initializer"> = 1</span> ;

}

预定义常量
----------

**`CairoFontWeight::NORMAL`**  
Normal font weight

**`CairoFontWeight::BOLD`**  
Bold font weight

简介
----

类摘要
------

**CairoScaledFont**

<span class="ooclass"> class **CairoScaledFont** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">CairoFontFace</span>
`$font_face`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix`</span> , <span
class="methodparam"><span class="type">CairoMatrix</span> `$ctm`</span>
, <span class="methodparam"><span class="type">CairoFontOptions</span>
`$options`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">extents</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">CairoMatrix</span> <span class="methodname">getCtm</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontFace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getFontOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getScaleMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">glyphExtents</span> ( <span
class="methodparam"><span class="type">array</span> `$glyphs`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">textExtents</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

}

CairoScaledFont::\_\_construct
==============================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoScaledFont::\_\_construct</span> ( <span
class="methodparam"><span class="type">CairoFontFace</span>
`$font_face`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix`</span> , <span
class="methodparam"><span class="type">CairoMatrix</span> `$ctm`</span>
, <span class="methodparam"><span class="type">CairoFontOptions</span>
`$options`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`font_face`  
Description...

`matrix`  
Description...

`ctm`  
Description...

`options`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoScaledFont::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::extents
========================

The extents purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoScaledFont::extents</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoScaledFont::extents</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::getCtm
=======================

The getCtm purpose

### 说明

<span class="modifier">public</span> <span
class="type">CairoMatrix</span> <span
class="methodname">CairoScaledFont::getCtm</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoScaledFont::getCtm</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::getFontFace
============================

cairo\_get\_font\_face
======================

The getFontFace purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoScaledFont::getFontFace</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_face</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::getFontMatrix
==============================

cairo\_get\_font\_matrix
========================

The getFontMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoScaledFont::getFontMatrix</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::getFontOptions
===============================

cairo\_get\_font\_options
=========================

The getFontOptions purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoScaledFont::getFontOptions</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_font\_options</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::getScaleMatrix
===============================

The getScaleMatrix purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoScaledFont::getScaleMatrix</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoScaledFont::getScaleMatrix</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::getType
========================

The getType purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoScaledFont::getType</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoScaledFont::getType</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::glyphExtents
=============================

The glyphExtents purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoScaledFont::glyphExtents</span> ( <span
class="methodparam"><span class="type">array</span> `$glyphs`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`glyphs`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoScaledFont::glyphExtents</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::status
=======================

cairo\_status
=============

The status purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoScaledFont::status</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_status</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoScaledFont::textExtents
============================

cairo\_text\_extents
====================

The textExtents purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoScaledFont::textExtents</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

过程化风格:

<span class="type">array</span> <span
class="methodname">cairo\_text\_extents</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`text`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

The <span class="classname">CairoToyFontFace</span> class can be used
instead of <span class="methodname">CairoContext::selectFontFace</span>
to create a toy font independently of a context.

类摘要
------

**CairoToyFontFace**

<span class="ooclass"> class **CairoToyFontFace** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoFontFace**
</span> {

/\* 继承的方法 \*/

}

简介
----

<span class="classname">CairoPatternType</span> is used to describe the
type of a given pattern.

The type of a pattern is determined by the function used to create it.
The <span class="function">cairo\_pattern\_create\_rgb</span> and <span
class="function">cairo\_pattern\_create\_rgba</span> functions create
**`CairoPatternType::SOLID`** patterns. The remaining
cairo\_pattern\_create\_\* functions map to pattern types in obvious
ways.

类摘要
------

**CairoPatternType**

<span class="ooclass"> class **CairoPatternType** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoPatternType::SOLID` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoPatternType::SURFACE` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoPatternType::LINEAR` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoPatternType::RADIAL` <span class="initializer"> = 3</span> ;

}

预定义常量
----------

**`CairoPatternType::SOLID`**  
The pattern is a solid (uniform) color. It may be opaque or translucent.

**`CairoPatternType::SURFACE`**  
The pattern is a based on a surface (an image).

**`CairoPatternType::LINEAR`**  
The pattern is a linear gradient.

**`CairoPatternType::RADIAL`**  
The pattern is a radial gradient.

简介
----

<span class="classname">CairoPattern</span> is the abstract base class
from which all the other pattern classes derive. It cannot be
instantiated directly

类摘要
------

**CairoPattern**

<span class="ooclass"> class **CairoPattern** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

}

CairoPattern::\_\_construct
===========================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoPattern::\_\_construct</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPattern::\_\_construct</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPattern::getMatrix
=======================

cairo\_get\_matrix
==================

The getMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::getMatrix</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_get\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPattern::getType
=====================

The getType purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::getType</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoPattern::getType</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPattern::setMatrix
=======================

cairo\_set\_matrix
==================

The setMatrix purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_set\_matrix</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`matrix`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoPattern::status
====================

cairo\_status
=============

The status purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::status</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">int</span> <span
class="methodname">cairo\_status</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

<span class="classname">CairoGradientPattern</span> is an abstract base
class from which other Pattern classes derive. It cannot be instantiated
directly.

类摘要
------

**CairoGradientPattern**

<span class="ooclass"> class **CairoGradientPattern** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoPattern**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addColorStopRgb</span> ( <span
class="methodparam"><span class="type">float</span> `$offset`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addColorStopRgba</span> ( <span
class="methodparam"><span class="type">float</span> `$offset`</span> ,
<span class="methodparam"><span class="type">float</span> `$red`</span>
, <span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> , <span
class="methodparam"><span class="type">float</span> `$alpha`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getColorStopCount</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getColorStopRgba</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getExtend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setExtend</span> ( <span
class="methodparam"><span class="type">int</span> `$extend`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoPattern::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::getMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::status</span> ( <span
class="methodparam">void</span> )

}

CairoGradientPattern::addColorStopRgb
=====================================

The addColorStopRgb purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::addColorStopRgb</span> (
<span class="methodparam"><span class="type">float</span>
`$offset`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
)

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`offset`  
Description...

`red`  
Description...

`green`  
Description...

`blue`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoGradientPattern::addColorStopRgb</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoGradientPattern::addColorStopRgba
======================================

The addColorStopRgba purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::addColorStopRgba</span> (
<span class="methodparam"><span class="type">float</span>
`$offset`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
, <span class="methodparam"><span class="type">float</span>
`$alpha`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`offset`  
Description...

`red`  
Description...

`green`  
Description...

`blue`  
Description...

`alpha`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoGradientPattern::addColorStopRgba</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoGradientPattern::getColorStopCount
=======================================

The getColorStopCount purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoGradientPattern::getColorStopCount</span> (
<span class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoGradientPattern::getColorStopCount</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoGradientPattern::getColorStopRgba
======================================

The getColorStopRgba purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoGradientPattern::getColorStopRgba</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`index`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoGradientPattern::getColorStopRgba</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoGradientPattern::getExtend
===============================

The getExtend purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoGradientPattern::getExtend</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoGradientPattern::getExtend</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoGradientPattern::setExtend
===============================

The setExtend purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::setExtend</span> ( <span
class="methodparam"><span class="type">int</span> `$extend`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`extend`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoGradientPattern::setExtend</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

类摘要
------

**CairoSolidPattern**

<span class="ooclass"> class **CairoSolidPattern** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoPattern**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">float</span> `$alpha`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getRgba</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoPattern::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::getMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::status</span> ( <span
class="methodparam">void</span> )

}

CairoSolidPattern::\_\_construct
================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoSolidPattern::\_\_construct</span> ( <span
class="methodparam"><span class="type">float</span> `$red`</span> ,
<span class="methodparam"><span class="type">float</span>
`$green`</span> , <span class="methodparam"><span
class="type">float</span> `$blue`</span> \[, <span
class="methodparam"><span class="type">float</span> `$alpha`<span
class="initializer"> = 0</span></span> \] )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`red`  
Description...

`green`  
Description...

`blue`  
Description...

`alpha`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSolidPattern::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSolidPattern::getRgba
==========================

The getRgba purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoSolidPattern::getRgba</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoSolidPattern::getRgba</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

类摘要
------

**CairoSurfacePattern**

<span class="ooclass"> class **CairoSurfacePattern** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CairoPattern**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getExtend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getFilter</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getSurface</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setExtend</span> ( <span
class="methodparam"><span class="type">int</span> `$extend`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setFilter</span> ( <span
class="methodparam"><span class="type">int</span> `$filter`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span
class="methodname">CairoPattern::\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::getMatrix</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoPattern::setMatrix</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoPattern::status</span> ( <span
class="methodparam">void</span> )

}

CairoSurfacePattern::\_\_construct
==================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoSurfacePattern::\_\_construct</span> ( <span
class="methodparam"><span class="type">CairoSurface</span>
`$surface`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`surface`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurfacePattern::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurfacePattern::getExtend
==============================

The getExtend purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurfacePattern::getExtend</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurfacePattern::getExtend</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurfacePattern::getFilter
==============================

The getFilter purpose

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoSurfacePattern::getFilter</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurfacePattern::getFilter</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurfacePattern::getSurface
===============================

The getSurface purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurfacePattern::getSurface</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurfacePattern::getSurface</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurfacePattern::setExtend
==============================

The setExtend purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurfacePattern::setExtend</span> ( <span
class="methodparam"><span class="type">int</span> `$extend`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`extend`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurfacePattern::setExtend</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoSurfacePattern::setFilter
==============================

The setFilter purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoSurfacePattern::setFilter</span> ( <span
class="methodparam"><span class="type">int</span> `$filter`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filter`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoSurfacePattern::setFilter</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

Create a new CairoLinearGradient along the line defined

类摘要
------

**CairoLinearGradient**

<span class="ooclass"> class **CairoLinearGradient** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**CairoGradientPattern** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">float</span> `$x0`</span> , <span
class="methodparam"><span class="type">float</span> `$y0`</span> , <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getPoints</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::addColorStopRgb</span> (
<span class="methodparam"><span class="type">float</span>
`$offset`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::addColorStopRgba</span> (
<span class="methodparam"><span class="type">float</span>
`$offset`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
, <span class="methodparam"><span class="type">float</span>
`$alpha`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoGradientPattern::getColorStopCount</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoGradientPattern::getColorStopRgba</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoGradientPattern::getExtend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::setExtend</span> ( <span
class="methodparam"><span class="type">int</span> `$extend`</span> )

}

CairoLinearGradient::\_\_construct
==================================

The \_\_construct purpose

### 说明

<span class="modifier">public</span> <span
class="methodname">CairoLinearGradient::\_\_construct</span> ( <span
class="methodparam"><span class="type">float</span> `$x0`</span> , <span
class="methodparam"><span class="type">float</span> `$y0`</span> , <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`x0`  
Description...

`y0`  
Description...

`x1`  
Description...

`y1`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoLinearGradient::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoLinearGradient::getPoints
==============================

The getPoints purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoLinearGradient::getPoints</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoLinearGradient::getPoints</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

类摘要
------

**CairoRadialGradient**

<span class="ooclass"> class **CairoRadialGradient** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**CairoGradientPattern** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">float</span> `$x0`</span> , <span
class="methodparam"><span class="type">float</span> `$y0`</span> , <span
class="methodparam"><span class="type">float</span> `$r0`</span> , <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$r1`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getCircles</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::addColorStopRgb</span> (
<span class="methodparam"><span class="type">float</span>
`$offset`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::addColorStopRgba</span> (
<span class="methodparam"><span class="type">float</span>
`$offset`</span> , <span class="methodparam"><span
class="type">float</span> `$red`</span> , <span
class="methodparam"><span class="type">float</span> `$green`</span> ,
<span class="methodparam"><span class="type">float</span> `$blue`</span>
, <span class="methodparam"><span class="type">float</span>
`$alpha`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoGradientPattern::getColorStopCount</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoGradientPattern::getColorStopRgba</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">CairoGradientPattern::getExtend</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoGradientPattern::setExtend</span> ( <span
class="methodparam"><span class="type">int</span> `$extend`</span> )

}

CairoRadialGradient::\_\_construct
==================================

The \_\_construct purpose

### 说明

面向对象风格:

<span class="modifier">public</span> <span
class="methodname">CairoRadialGradient::\_\_construct</span> ( <span
class="methodparam"><span class="type">float</span> `$x0`</span> , <span
class="methodparam"><span class="type">float</span> `$y0`</span> , <span
class="methodparam"><span class="type">float</span> `$r0`</span> , <span
class="methodparam"><span class="type">float</span> `$x1`</span> , <span
class="methodparam"><span class="type">float</span> `$y1`</span> , <span
class="methodparam"><span class="type">float</span> `$r1`</span> )

过程化风格:

Creates a new radial gradient <span class="type">CairoPattern</span>
between the two circles defined by (x0, y0, r0) and (x1, y1, r1). Before
using the gradient pattern, a number of color stops should be defined
using <span
class="methodname">CairoRadialGradient::addColorStopRgb</span> or <span
class="methodname">CairoRadialGradient::addColorStopRgba</span>.

Note: The coordinates here are in pattern space. For a new pattern,
pattern space is identical to user space, but the relationship between
the spaces can be changed with <span
class="methodname">CairoRadialGradient::setMatrix</span>.

### 参数

`x0`  
x coordinate for the center of the start circle.

`y0`  
y coordinate for the center of the start circle.

`r0`  
radius of the start circle.

`x1`  
x coordinate for the center of the end circle.

`y1`  
y coordinate for the center of the end circle.

`r1`  
radius of the end circle.

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoRadialGradient::\_\_construct</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoRadialGradient::getCircles
===============================

The getCircles purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoRadialGradient::getCircles</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoRadialGradient::getCircles</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

Enum class that specifies the type of antialiasing to do when rendering
text or shapes.

类摘要
------

**CairoAntialias**

<span class="ooclass"> class **CairoAntialias** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoAntialias::MODE_DEFAULT` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoAntialias::MODE_NONE` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoAntialias::MODE_GRAY` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoAntialias::MODE_SUBPIXEL` <span class="initializer"> = 3</span> ;

}

预定义常量
----------

**`CairoAntialias::MODE_DEFAULT`**  
Use the default antialiasing for the subsystem and target device

**`CairoAntialias::MODE_NONE`**  
Use a bilevel alpha mask

**`CairoAntialias::MODE_GRAY`**  
Perform single-color antialiasing (using shades of gray for black text
on a white background, for example).

**`CairoAntialias::MODE_SUBPIXEL`**  
Perform antialiasing by taking advantage of the order of subpixel
elements on devices such as LCD panels.

简介
----

<span class="classname">CairoContent</span> is used to describe the
content that a surface will contain, whether color information, alpha
information (translucence vs. opacity), or both.

Note: The large values here are designed to keep <span
class="classname">CairoContent</span> values distinct from <span
class="classname">CairoContent</span> values so that the implementation
can detect the error if users confuse the two types.

类摘要
------

**CairoContent**

<span class="ooclass"> class **CairoContent** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoContent::COLOR` <span class="initializer"> = 4096</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoContent::ALPHA` <span class="initializer"> = 8192</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoContent::COLOR_ALPHA` <span class="initializer"> = 12288</span> ;

}

预定义常量
----------

**`CairoContent::COLOR`**  
The surface will hold color content only.

**`CairoContent::ALPHA`**  
The surface will hold alpha content only.

**`CairoContent::COLOR_ALPHA`**  
The surface will hold color and alpha content.

简介
----

类摘要
------

**CairoExtend**

<span class="ooclass"> class **CairoExtend** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoExtend::NONE` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoExtend::REPEAT` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoExtend::REFLECT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoExtend::PAD` <span class="initializer"> = 3</span> ;

}

预定义常量
----------

**`CairoExtend::NONE`**  
Description here...

**`CairoExtend::REPEAT`**  
Description here...

**`CairoExtend::REFLECT`**  
Description here...

**`CairoExtend::PAD`**  
Description here...

简介
----

CairoFormat enums are used to identify the memory format of the image
data.

类摘要
------

**CairoFormat**

<span class="ooclass"> class **CairoFormat** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFormat::ARGB32` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFormat::RGB24` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFormat::A8` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFormat::A1` <span class="initializer"> = 3</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">strideForWidth</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
)

}

预定义常量
----------

**`CairoFormat::ARGB32`**  
Each pixel is a 32-bit quantity, with alpha in the upper 8 bits, then
red, then green, then blue. The 32-bit quantities are stored
native-endian. Pre-multiplied alpha is used. (That is, 50% transparent
red is 0x80800000, not 0x80ff0000.)

**`CairoFormat::RGB24`**  
Each pixel is a 32-bit quantity, with the upper 8 bits unused. Red,
Green, and Blue are stored in the remaining 24 bits in that order.

**`CairoFormat::A8`**  
Each pixel is a 8-bit quantity holding an alpha value.

**`CairoFormat::A1`**  
Each pixel is a 1-bit quantity holding an alpha value. Pixels are packed
together into 32-bit quantities. The ordering of the bits matches the
endianness of the platform. On a big-endian machine, the first pixel is
in the uppermost bit, on a little-endian machine the first pixel is in
the least-significant bit.

CairoFormat::strideForWidth
===========================

Provides an appropriate stride to use

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">CairoFormat::strideForWidth</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
)

This method provides a stride value that will respect all alignment
requirements of the accelerated image-rendering code within cairo.

### 参数

`format`  
The desired <span class="classname">CairoFormat</span> to use

`width`  
The width of the image

### 返回值

The appropriate stride to use given the desired format and width, or -1
if either the format is invalid or the width too large.

### 范例

**示例 \#1 <span class="methodname">CairoFormat::strideForWidth</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

A <span class="classname">CairoFillRule</span> is used to select how
paths are filled. For both fill rules, whether or not a point is
included in the fill is determined by taking a ray from that point to
infinity and looking at intersections with the path. The ray can be in
any direction, as long as it doesn't pass through the end point of a
segment or have a tricky intersection such as intersecting tangent to
the path. (Note that filling is not actually implemented in this way.
This is just a description of the rule that is applied.)

The default fill rule is **`CairoFillRule::WINDING`**.

类摘要
------

**CairoFillRule**

<span class="ooclass"> class **CairoFillRule** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFillRule::WINDING` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFillRule::EVEN_ODD` <span class="initializer"> = 1</span> ;

}

预定义常量
----------

**`CairoFillRule::WINDING`**  
If the path crosses the ray from left-to-right, counts +1. If the path
crosses the ray from right to left, counts -1. (Left and right are
determined from the perspective of looking along the ray from the
starting point.) If the total count is non-zero, the point will be
filled.

**`CairoFillRule::EVEN_ODD`**  
Counts the total number of intersections, without regard to the
orientation of the contour. If the total number of intersections is odd,
the point will be filled.

简介
----

A <span class="classname">CairoFilter</span> is used to indicate what
filtering should be applied when reading pixel values from patterns. See
<span class="methodname">CairoPattern::setSource</span> or <span
class="function">cairo\_pattern\_set\_source</span> for indicating the
desired filter to be used with a particular pattern.

类摘要
------

**CairoFilter**

<span class="ooclass"> class **CairoFilter** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFilter::FAST` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFilter::GOOD` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFilter::BEST` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFilter::NEAREST` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFilter::BILINEAR` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoFilter::GAUSSIAN` <span class="initializer"> = 5</span> ;

}

预定义常量
----------

**`CairoFilter::FAST`**  
A high-performance filter, with quality similar to
**`CairoFilter::NEAREST`**

**`CairoFilter::GOOD`**  
A reasonable-performance filter, with quality similar to
**`CairoFilter::BILINEAR`**

**`CairoFilter::BEST`**  
The highest-quality available, performance may not be suitable for
interactive use.

**`CairoFilter::NEAREST`**  
Nearest-neighbor filtering

**`CairoFilter::BILINEAR`**  
Linear interpolation in two dimensions

**`CairoFilter::GAUSSIAN`**  
This filter value is currently unimplemented, and should not be used in
current code.

简介
----

Specifies whether to hint font metrics; hinting font metrics means
quantizing them so that they are integer values in device space. Doing
this improves the consistency of letter and line spacing, however it
also means that text will be laid out differently at different zoom
factors.

类摘要
------

**CairoHintMetrics**

<span class="ooclass"> class **CairoHintMetrics** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintMetrics::METRICS_DEFAULT` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintMetrics::METRICS_OFF` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintMetrics::METRICS_ON` <span class="initializer"> = 2</span> ;

}

预定义常量
----------

**`CairoHintMetrics::METRICS_DEFAULT`**  
Hint metrics in the default manner for the font backend and target
device

**`CairoHintMetrics::METRICS_OFF`**  
Do not hint font metrics

**`CairoHintMetrics::METRICS_ON`**  
Hint font metrics

简介
----

Specifies the type of hinting to do on font outlines. Hinting is the
process of fitting outlines to the pixel grid in order to improve the
appearance of the result. Since hinting outlines involves distorting
them, it also reduces the faithfulness to the original outline shapes.
Not all of the outline hinting styles are supported by all font
backends.

类摘要
------

**CairoHintStyle**

<span class="ooclass"> class **CairoHintStyle** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintStyle::STYLE_DEFAULT` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintStyle::STYLE_NONE` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintStyle::STYLE_SLIGHT` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintStyle::STYLE_MEDIUM` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoHintStyle::STYLE_FULL` <span class="initializer"> = 4</span> ;

}

预定义常量
----------

**`CairoHintStyle::STYLE_DEFAULT`**  
Use the default hint style for font backend and target device

**`CairoHintStyle::STYLE_NONE`**  
Do not hint outlines

**`CairoHintStyle::STYLE_SLIGHT`**  
Hint outlines slightly to improve contrast while retaining good fidelity
to the original shapes.

**`CairoHintStyle::STYLE_MEDIUM`**  
Hint outlines with medium strength giving a compromise between fidelity
to the original shapes and contrast

**`CairoHintStyle::STYLE_FULL`**  
Hint outlines to maximize contrast

简介
----

Specifies how to render the endpoints of the path when stroking.

The default line cap style is **`CairoLineCap::BUTT`**.

类摘要
------

**CairoLineCap**

<span class="ooclass"> class **CairoLineCap** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoLineCap::BUTT` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoLineCap::ROUND` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoLineCap::SQUARE` <span class="initializer"> = 2</span> ;

}

预定义常量
----------

**`CairoLineCap::BUTT`**  
Start(stop) the line exactly at the start(end) point

**`CairoLineCap::ROUND`**  
Use a round ending, the center of the circle is the end point

**`CairoLineCap::SQUARE`**  
Use squared ending, the center of the square is the end point

简介
----

类摘要
------

**CairoLineJoin**

<span class="ooclass"> class **CairoLineJoin** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoLineJoin::MITER` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoLineJoin::ROUND` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoLineJoin::BEVEL` <span class="initializer"> = 2</span> ;

}

预定义常量
----------

**`CairoLineJoin::MITER`**  
Description here...

**`CairoLineJoin::ROUND`**  
Description here...

**`CairoLineJoin::BEVEL`**  
Description here...

简介
----

Matrices are used throughout cairo to convert between different
coordinate spaces.

类摘要
------

**CairoMatrix**

<span class="ooclass"> class **CairoMatrix** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">float</span> `$xx`<span
class="initializer"> = 1.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$yx`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$xy`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$yy`<span
class="initializer"> = 1.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$x0`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$y0`<span
class="initializer"> = 0.0</span></span> \]\]\]\]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">initIdentity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">initRotate</span> ( <span class="methodparam"><span
class="type">float</span> `$radians`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">initScale</span> ( <span class="methodparam"><span
class="type">float</span> `$sx`</span> , <span class="methodparam"><span
class="type">float</span> `$sy`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">initTranslate</span> ( <span
class="methodparam"><span class="type">float</span> `$tx`</span> , <span
class="methodparam"><span class="type">float</span> `$ty`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">invert</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">CairoMatrix</span>
<span class="methodname">multiply</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix1`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix2`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rotate</span> ( <span class="methodparam"><span
class="type">float</span> `$radians`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">scale</span> ( <span class="methodparam"><span
class="type">float</span> `$sx`</span> , <span class="methodparam"><span
class="type">float</span> `$sy`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">transformDistance</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">transformPoint</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">translate</span> ( <span
class="methodparam"><span class="type">float</span> `$tx`</span> , <span
class="methodparam"><span class="type">float</span> `$ty`</span> )

}

CairoMatrix::\_\_construct
==========================

cairo\_matrix\_init
===================

Creates a new CairoMatrix object

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="methodname">CairoMatrix::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">float</span> `$xx`<span
class="initializer"> = 1.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$yx`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$xy`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$yy`<span
class="initializer"> = 1.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$x0`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$y0`<span
class="initializer"> = 0.0</span></span> \]\]\]\]\]\] )

过程化风格:

<span class="type">object</span> <span
class="methodname">cairo\_matrix\_init</span> (\[ <span
class="methodparam"><span class="type">float</span> `$xx`<span
class="initializer"> = 1.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$yx`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$xy`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$yy`<span
class="initializer"> = 1.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$x0`<span
class="initializer"> = 0.0</span></span> \[, <span
class="methodparam"><span class="type">float</span> `$y0`<span
class="initializer"> = 0.0</span></span> \]\]\]\]\]\] )

Returns new CairoMatrix object. Matrices are used throughout cairo to
convert between different coordinate spaces. Sets matrix to be the
affine transformation given by xx, yx, xy, yy, x0, y0. The
transformation is given by: x\_new = xx \* x + xy \* y + x0; and y\_new
= yx \* x + yy \* y + y0;

### 参数

`xx`  
xx component of the affine transformation

`yx`  
yx component of the affine transformation

`xy`  
xy component of the affine transformation

`yy`  
yy component of the affine transformation

`x0`  
X translation component of the affine transformation

`y0`  
Y translation component of the affine transformation

### 返回值

Returns a new CairoMatrix object that can be used with surfaces,
contexts, and patterns.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Create a new Matrix */
$matrix = new CairoMatrix(1.0, 0.5, 0.0, 1.0, 0.0, 0.0);
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Create a new Matrix */
$matrix = cairo_matrix_init(1.0, 0.5, 0.0, 1.0, 0.0, 0.0);
?>
```

### 参见

-   <span class="methodname">CairoMatrix::initIdentity</span>
-   <span class="methodname">CairoMatrix::initRotate</span>
-   <span class="methodname">CairoMatrix::initScale</span>
-   <span class="methodname">CairoMatrix::initTranslate</span>

CairoMatrix::initIdentity
=========================

cairo\_matrix\_init\_identity
=============================

Creates a new identity matrix

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">CairoMatrix::initIdentity</span> ( <span
class="methodparam">void</span> )

过程化风格:

<span class="type">object</span> <span
class="methodname">cairo\_matrix\_init\_identity</span> ( <span
class="methodparam">void</span> )

Creates a new matrix that is an identity transformation. An identity
transformation means the source data is copied into the destination data
without change

### 参数

此函数没有参数。

### 返回值

Returns a new CairoMatrix object that can be used with surfaces,
contexts, and patterns.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Create a new Matrix */
$matrix = CairoMatrix::initIdentity();
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Create a new Matrix */
$matrix = cairo_matrix_init_identity();
?>
```

### 参见

-   <span class="methodname">CairoMatrix::\_\_construct</span>
-   <span class="methodname">CairoMatrix::initRotate</span>
-   <span class="methodname">CairoMatrix::initScale</span>
-   <span class="methodname">CairoMatrix::initTranslate</span>

CairoMatrix::initRotate
=======================

cairo\_matrix\_init\_rotate
===========================

Creates a new rotated matrix

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">CairoMatrix::initRotate</span> ( <span
class="methodparam"><span class="type">float</span> `$radians`</span> )

过程化风格:

<span class="type">object</span> <span
class="methodname">cairo\_matrix\_init\_rotate</span> ( <span
class="methodparam"><span class="type">float</span> `$radians`</span> )

Creates a new matrix to a transformation that rotates by radians
provided

### 参数

`radians`  
angle of rotation, in radians. The direction of rotation is defined such
that positive angles rotate in the direction from the positive X axis
toward the positive Y axis. With the default axis orientation of cairo,
positive angles rotate in a clockwise direction.

### 返回值

Returns a new CairoMatrix object that can be used with surfaces,
contexts, and patterns.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Create a new Matrix */
$matrix = CairoMatrix::initRotate(0.3);
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Create a new Matrix */
$matrix = cairo_matrix_init_rotate(0.3);
?>
```

### 参见

-   <span class="methodname">CairoMatrix::\_\_construct</span>
-   <span class="methodname">CairoMatrix::initIdentity</span>
-   <span class="methodname">CairoMatrix::initScale</span>
-   <span class="methodname">CairoMatrix::initTranslate</span>

CairoMatrix::initScale
======================

cairo\_matrix\_init\_scale
==========================

Creates a new scaling matrix

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">CairoMatrix::initScale</span> ( <span
class="methodparam"><span class="type">float</span> `$sx`</span> , <span
class="methodparam"><span class="type">float</span> `$sy`</span> )

过程化风格:

<span class="type">object</span> <span
class="methodname">cairo\_matrix\_init\_scale</span> ( <span
class="methodparam"><span class="type">float</span> `$sx`</span> , <span
class="methodparam"><span class="type">float</span> `$sy`</span> )

Creates a new matrix to a transformation that scales by sx and sy in the
X and Y dimensions, respectively.

### 参数

`sx`  
scale factor in the X direction

`sy`  
scale factor in the Y direction

### 返回值

Returns a new CairoMatrix object that can be used with surfaces,
contexts, and patterns.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Create a new Matrix */
$matrix = CairoMatrix::initScale(1.0, 2.0);
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Create a new Matrix */
$matrix = cairo_matrix_init_scale(1.0, 2.0);
?>
```

### 参见

-   <span class="methodname">CairoMatrix::\_\_construct</span>
-   <span class="methodname">CairoMatrix::initIdentity</span>
-   <span class="methodname">CairoMatrix::initRotate</span>
-   <span class="methodname">CairoMatrix::initTranslate</span>

CairoMatrix::initTranslate
==========================

cairo\_matrix\_init\_translate
==============================

Creates a new translation matrix

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">void</span> <span
class="methodname">CairoMatrix::initTranslate</span> ( <span
class="methodparam"><span class="type">float</span> `$tx`</span> , <span
class="methodparam"><span class="type">float</span> `$ty`</span> )

过程化风格:

<span class="type">object</span> <span
class="methodname">cairo\_matrix\_init\_translate</span> ( <span
class="methodparam"><span class="type">float</span> `$tx`</span> , <span
class="methodparam"><span class="type">float</span> `$ty`</span> )

Creates a new matrix to a transformation that translates by tx and ty in
the X and Y dimensions, respectively.

### 参数

`tx`  
amount to translate in the X direction

`ty`  
amount to translate in the Y direction

### 返回值

Returns a new CairoMatrix object that can be used with surfaces,
contexts, and patterns.

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Create a new Matrix */
$matrix = CairoMatrix::initTranslate(1.0, 2.0);
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Create a new Matrix */
$matrix = cairo_matrix_init_translate(1.0, 2.0);
?>
```

### 参见

-   <span class="methodname">CairoMatrix::\_\_construct</span>
-   <span class="methodname">CairoMatrix::initIdentity</span>
-   <span class="methodname">CairoMatrix::initRotate</span>
-   <span class="methodname">CairoMatrix::initScale</span>

CairoMatrix::invert
===================

The invert purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoMatrix::invert</span> ( <span
class="methodparam">void</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoMatrix::invert</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoMatrix::multiply
=====================

The multiply purpose

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">CairoMatrix</span>
<span class="methodname">CairoMatrix::multiply</span> ( <span
class="methodparam"><span class="type">CairoMatrix</span>
`$matrix1`</span> , <span class="methodparam"><span
class="type">CairoMatrix</span> `$matrix2`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`matrix1`  
Description...

`matrix2`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoMatrix::multiply</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoMatrix::rotate
===================

cairo\_matrix\_rotate
=====================

The rotate purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoMatrix::rotate</span> ( <span
class="methodparam"><span class="type">float</span> `$radians`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_matrix\_rotate</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">string</span> `$radians`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`radians`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoMatrix::scale
==================

cairo\_matrix\_scale
====================

Applies scaling to a matrix

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoMatrix::scale</span> ( <span
class="methodparam"><span class="type">float</span> `$sx`</span> , <span
class="methodparam"><span class="type">float</span> `$sy`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_matrix\_scale</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$sx`</span> , <span class="methodparam"><span
class="type">float</span> `$sy`</span> )

Applies scaling by sx, sy to the transformation in the matrix. The
effect of the new transformation is to first scale the coordinates by sx
and sy, then apply the original transformation to the coordinates.

### 参数

`matrix`  
Procedural only - CairoMatrix instance

`sx`  
scale factor in the X direction

`sy`  
scale factor in the Y direction

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* Apply scaling to a matrix */
$matrix = new CairoMatrix(1.0, 0.5, 0.0, 1.0, 0.0, 0.0);
$matrix->scale(0.2, 2.0);
?>
```

**示例 \#2 过程化风格**

``` php
<?php
/* Apply scaling to a matrix */
$matrix = cairo_matrix_init(1.0, 0.5, 0.0, 1.0, 0.0, 0.0);
cairo_matrix_scale($matrix, 0.2, 2.0);
?>
```

### 参见

-   <span class="methodname">CairoMatrix::initScale</span>

CairoMatrix::transformDistance
==============================

The transformDistance purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoMatrix::transformDistance</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`dx`  
Description...

`dy`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span
class="methodname">CairoMatrix::transformDistance</span> example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoMatrix::transformPoint
===========================

The transformPoint purpose

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">CairoMatrix::transformPoint</span> ( <span
class="methodparam"><span class="type">float</span> `$dx`</span> , <span
class="methodparam"><span class="type">float</span> `$dy`</span> )

The method description goes here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`dx`  
Description...

`dy`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 <span class="methodname">CairoMatrix::transformPoint</span>
example**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

CairoMatrix::translate
======================

cairo\_translate
================

The translate purpose

### 说明

面向对象风格 (method):

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CairoMatrix::translate</span> ( <span
class="methodparam"><span class="type">float</span> `$tx`</span> , <span
class="methodparam"><span class="type">float</span> `$ty`</span> )

过程化风格:

<span class="type">void</span> <span
class="methodname">cairo\_translate</span> ( <span
class="methodparam"><span class="type">CairoContext</span>
`$context`</span> , <span class="methodparam"><span
class="type">float</span> `$x`</span> , <span class="methodparam"><span
class="type">float</span> `$y`</span> )

Description here.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  
Description...

`x`  
Description...

`y`  
Description...

`tx`  
Description...

`ty`  
Description...

### 返回值

Description...

### 范例

**示例 \#1 面向对象风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

**示例 \#2 过程化风格**

``` php
<?php
/* ... */
?>
```

以上例程的输出类似于：

    ...

### 参见

-   <span class="methodname">Classname::Method</span>

简介
----

This is used to set the compositing operator for all cairo drawing
operations.

The default operator is **`CairoOperator::OVER`**

The operators marked as unbounded modify their destination even outside
of the mask layer (that is, their effect is not bound by the mask
layer). However, their effect can still be limited by way of clipping.

To keep things simple, the operator descriptions here document the
behavior for when both source and destination are either fully
transparent or fully opaque. The actual implementation works for
translucent layers too. For a more detailed explanation of the effects
of each operator, including the mathematical definitions, see
http://cairographics.org/operators/.

类摘要
------

**CairoOperator**

<span class="ooclass"> class **CairoOperator** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::CLEAR` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::SOURCE` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::OVER` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::IN` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::OUT` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::ATOP` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::DEST` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::DEST_OVER` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::DEST_IN` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::DEST_OUT` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::DEST_ATOP` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::XOR` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::ADD` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoOperator::SATURATE` <span class="initializer"> = 13</span> ;

}

预定义常量
----------

**`CairoOperator::CLEAR`**  
Clear destination layer (bounded)

**`CairoOperator::SOURCE`**  
Replace destination layer (bounded)

**`CairoOperator::OVER`**  
Draw source layer on top of destination layer (bounded)

**`CairoOperator::IN`**  
Draw source where there was destination content (unbounded)

**`CairoOperator::OUT`**  
Draw source where there was no destination content (unbounded)

**`CairoOperator::ATOP`**  
Draw source on top of destination content and only there

**`CairoOperator::DEST`**  
Ignore the source

**`CairoOperator::DEST_OVER`**  
Draw destination on top of source

**`CairoOperator::DEST_IN`**  
Leave destination only where there was source content (unbounded)

**`CairoOperator::DEST_OUT`**  
Leave destination only where there was no source content

**`CairoOperator::DEST_ATOP`**  
Leave destination on top of source content and only there (unbounded)

**`CairoOperator::XOR`**  
Source and destination are shown where there is only one of them

**`CairoOperator::ADD`**  
Source and destination layers are accumulated

**`CairoOperator::SATURATE`**  
Like **`CairoOperator::OVER`**, but assuming source and dest are
disjoint geometries

简介
----

Note: CairoPath class cannot be instantiated directly, doing so will
result in Fatal Error if used or passed

类摘要
------

**CairoPath**

<span class="ooclass"> class **CairoPath** </span> {

}

简介
----

类摘要
------

**CairoPsLevel**

<span class="ooclass"> class **CairoPsLevel** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoPsLevel::LEVEL_2` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoPsLevel::LEVEL_3` <span class="initializer"> = 1</span> ;

}

预定义常量
----------

**`CairoPsLevel::LEVEL_2`**  
Description here...

**`CairoPsLevel::LEVEL_3`**  
Description here...

简介
----

类摘要
------

**CairoSubpixelOrder**

<span class="ooclass"> class **CairoSubpixelOrder** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSubpixelOrder::ORDER_DEFAULT` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSubpixelOrder::ORDER_RGB` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSubpixelOrder::ORDER_BGR` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSubpixelOrder::ORDER_VRGB` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSubpixelOrder::ORDER_VBGR` <span class="initializer"> = 4</span> ;

}

预定义常量
----------

**`CairoSubpixelOrder::ORDER_DEFAULT`**  
Description here...

**`CairoSubpixelOrder::ORDER_RGB`**  
Description here...

**`CairoSubpixelOrder::ORDER_BGR`**  
Description here...

**`CairoSubpixelOrder::ORDER_VRGB`**  
Description here...

**`CairoSubpixelOrder::ORDER_VBGR`**  
Description here...

简介
----

类摘要
------

**CairoSvgVersion**

<span class="ooclass"> class **CairoSvgVersion** </span> {

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSvgVersion::VERSION_1_1` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">integer</span>
`CairoSvgVersion::VERSION_1_2` <span class="initializer"> = 1</span> ;

}

预定义常量
----------

**`CairoSvgVersion::VERSION_1_1`**  
Description here...

**`CairoSvgVersion::VERSION_1_2`**  
Description here...
