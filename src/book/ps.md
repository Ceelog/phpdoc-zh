PostScript document creation
============================

**目录**

-   [简介](/intro/ps.html)
-   [安装／配置](/ps/setup.html)
    -   [需求](/ps/setup.html#需求)
    -   [安装](/ps/setup.html#安装)
    -   [运行时配置](/ps/setup.html#运行时配置)
    -   [资源类型](/ps/setup.html#资源类型)
-   [预定义常量](/ps/constants.html)
-   [PS 函数](/ref/ps.html)
    -   [ps\_add\_bookmark](/ref/ps.html#ps_add_bookmark) — Add bookmark
        to current page
    -   [ps\_add\_launchlink](/ref/ps.html#ps_add_launchlink) — Adds
        link which launches file
    -   [ps\_add\_locallink](/ref/ps.html#ps_add_locallink) — Adds link
        to a page in the same document
    -   [ps\_add\_note](/ref/ps.html#ps_add_note) — Adds note to current
        page
    -   [ps\_add\_pdflink](/ref/ps.html#ps_add_pdflink) — Adds link to a
        page in a second pdf document
    -   [ps\_add\_weblink](/ref/ps.html#ps_add_weblink) — Adds link to a
        web location
    -   [ps\_arc](/ref/ps.html#ps_arc) — Draws an arc counterclockwise
    -   [ps\_arcn](/ref/ps.html#ps_arcn) — Draws an arc clockwise
    -   [ps\_begin\_page](/ref/ps.html#ps_begin_page) — Start a new page
    -   [ps\_begin\_pattern](/ref/ps.html#ps_begin_pattern) — Start a
        new pattern
    -   [ps\_begin\_template](/ref/ps.html#ps_begin_template) — Start a
        new template
    -   [ps\_circle](/ref/ps.html#ps_circle) — Draws a circle
    -   [ps\_clip](/ref/ps.html#ps_clip) — Clips drawing to current path
    -   [ps\_close\_image](/ref/ps.html#ps_close_image) — Closes image
        and frees memory
    -   [ps\_close](/ref/ps.html#ps_close) — Closes a PostScript
        document
    -   [ps\_closepath\_stroke](/ref/ps.html#ps_closepath_stroke) —
        Closes and strokes path
    -   [ps\_closepath](/ref/ps.html#ps_closepath) — Closes path
    -   [ps\_continue\_text](/ref/ps.html#ps_continue_text) — Continue
        text in next line
    -   [ps\_curveto](/ref/ps.html#ps_curveto) — Draws a curve
    -   [ps\_delete](/ref/ps.html#ps_delete) — Deletes all resources of
        a PostScript document
    -   [ps\_end\_page](/ref/ps.html#ps_end_page) — End a page
    -   [ps\_end\_pattern](/ref/ps.html#ps_end_pattern) — End a pattern
    -   [ps\_end\_template](/ref/ps.html#ps_end_template) — End a
        template
    -   [ps\_fill\_stroke](/ref/ps.html#ps_fill_stroke) — Fills and
        strokes the current path
    -   [ps\_fill](/ref/ps.html#ps_fill) — Fills the current path
    -   [ps\_findfont](/ref/ps.html#ps_findfont) — Loads a font
    -   [ps\_get\_buffer](/ref/ps.html#ps_get_buffer) — Fetches the full
        buffer containig the generated PS data
    -   [ps\_get\_parameter](/ref/ps.html#ps_get_parameter) — Gets
        certain parameters
    -   [ps\_get\_value](/ref/ps.html#ps_get_value) — Gets certain
        values
    -   [ps\_hyphenate](/ref/ps.html#ps_hyphenate) — Hyphenates a word
    -   [ps\_include\_file](/ref/ps.html#ps_include_file) — Reads an
        external file with raw PostScript code
    -   [ps\_lineto](/ref/ps.html#ps_lineto) — Draws a line
    -   [ps\_makespotcolor](/ref/ps.html#ps_makespotcolor) — Create spot
        color
    -   [ps\_moveto](/ref/ps.html#ps_moveto) — Sets current point
    -   [ps\_new](/ref/ps.html#ps_new) — Creates a new PostScript
        document object
    -   [ps\_open\_file](/ref/ps.html#ps_open_file) — Opens a file for
        output
    -   [ps\_open\_image\_file](/ref/ps.html#ps_open_image_file) — Opens
        image from file
    -   [ps\_open\_image](/ref/ps.html#ps_open_image) — Reads an image
        for later placement
    -   [ps\_open\_memory\_image](/ref/ps.html#ps_open_memory_image) —
        Takes an GD image and returns an image for placement in a PS
        document
    -   [ps\_place\_image](/ref/ps.html#ps_place_image) — Places image
        on the page
    -   [ps\_rect](/ref/ps.html#ps_rect) — Draws a rectangle
    -   [ps\_restore](/ref/ps.html#ps_restore) — Restore previously save
        context
    -   [ps\_rotate](/ref/ps.html#ps_rotate) — Sets rotation factor
    -   [ps\_save](/ref/ps.html#ps_save) — Save current context
    -   [ps\_scale](/ref/ps.html#ps_scale) — Sets scaling factor
    -   [ps\_set\_border\_color](/ref/ps.html#ps_set_border_color) —
        Sets color of border for annotations
    -   [ps\_set\_border\_dash](/ref/ps.html#ps_set_border_dash) — Sets
        length of dashes for border of annotations
    -   [ps\_set\_border\_style](/ref/ps.html#ps_set_border_style) —
        Sets border style of annotations
    -   [ps\_set\_info](/ref/ps.html#ps_set_info) — Sets information
        fields of document
    -   [ps\_set\_parameter](/ref/ps.html#ps_set_parameter) — Sets
        certain parameters
    -   [ps\_set\_text\_pos](/ref/ps.html#ps_set_text_pos) — Sets
        position for text output
    -   [ps\_set\_value](/ref/ps.html#ps_set_value) — Sets certain
        values
    -   [ps\_setcolor](/ref/ps.html#ps_setcolor) — Sets current color
    -   [ps\_setdash](/ref/ps.html#ps_setdash) — Sets appearance of a
        dashed line
    -   [ps\_setflat](/ref/ps.html#ps_setflat) — Sets flatness
    -   [ps\_setfont](/ref/ps.html#ps_setfont) — Sets font to use for
        following output
    -   [ps\_setgray](/ref/ps.html#ps_setgray) — Sets gray value
    -   [ps\_setlinecap](/ref/ps.html#ps_setlinecap) — Sets appearance
        of line ends
    -   [ps\_setlinejoin](/ref/ps.html#ps_setlinejoin) — Sets how
        contected lines are joined
    -   [ps\_setlinewidth](/ref/ps.html#ps_setlinewidth) — Sets width of
        a line
    -   [ps\_setmiterlimit](/ref/ps.html#ps_setmiterlimit) — Sets the
        miter limit
    -   [ps\_setoverprintmode](/ref/ps.html#ps_setoverprintmode) — Sets
        overprint mode
    -   [ps\_setpolydash](/ref/ps.html#ps_setpolydash) — Sets appearance
        of a dashed line
    -   [ps\_shading\_pattern](/ref/ps.html#ps_shading_pattern) —
        Creates a pattern based on a shading
    -   [ps\_shading](/ref/ps.html#ps_shading) — Creates a shading for
        later use
    -   [ps\_shfill](/ref/ps.html#ps_shfill) — Fills an area with a
        shading
    -   [ps\_show\_boxed](/ref/ps.html#ps_show_boxed) — Output text in a
        box
    -   [ps\_show\_xy2](/ref/ps.html#ps_show_xy2) — Output text at
        position
    -   [ps\_show\_xy](/ref/ps.html#ps_show_xy) — Output text at given
        position
    -   [ps\_show2](/ref/ps.html#ps_show2) — Output a text at current
        position
    -   [ps\_show](/ref/ps.html#ps_show) — Output text
    -   [ps\_string\_geometry](/ref/ps.html#ps_string_geometry) — Gets
        geometry of a string
    -   [ps\_stringwidth](/ref/ps.html#ps_stringwidth) — Gets width of a
        string
    -   [ps\_stroke](/ref/ps.html#ps_stroke) — Draws the current path
    -   [ps\_symbol\_name](/ref/ps.html#ps_symbol_name) — Gets name of a
        glyph
    -   [ps\_symbol\_width](/ref/ps.html#ps_symbol_width) — Gets width
        of a glyph
    -   [ps\_symbol](/ref/ps.html#ps_symbol) — Output a glyph
    -   [ps\_translate](/ref/ps.html#ps_translate) — Sets translation
